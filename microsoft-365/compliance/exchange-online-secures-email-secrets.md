---
title: Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 07/01/2019
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Outre le Centre de gestion de la confidentialité Office 365 qui fournit des informations sur la sécurité, la confidentialité et la conformité pour Microsoft 365, vous voudrez peut-être savoir comment Microsoft contribue à protéger les secrets que vous stockez dans ses centres de données. Nous utilisons une technologie appelée Gestionnaire de clés distribuées (DKM).
ms.openlocfilehash: 2f6e51b7fe9cd75cbd265c3135050a08130f34d8
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50906960"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="7d970-104">Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7d970-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="7d970-105">Cet article décrit la façon dont Microsoft protège les informations confidentielles figurant dans vos courriers électroniques dans ses centres de données.</span><span class="sxs-lookup"><span data-stu-id="7d970-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="7d970-106">Comment sécurisons-nous les informations confidentielles que vous indiquez ?</span><span class="sxs-lookup"><span data-stu-id="7d970-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="7d970-107">Outre le Centre de gestion de la confidentialité Office 365 qui fournit des informations de sécurité, de confidentialité et de conformité pour [Office 365,](./get-started-with-service-trust-portal.md)vous souhaitez peut-être savoir comment Microsoft contribue à protéger les secrets que vous fournissez dans ses centres de données.</span><span class="sxs-lookup"><span data-stu-id="7d970-107">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](./get-started-with-service-trust-portal.md), you might want to know how Microsoft helps protects secrets you provide in its datacenters.</span></span> <span data-ttu-id="7d970-108">Nous utilisons une technologie appelée Gestionnaire de clés distribuées (DKM).</span><span class="sxs-lookup"><span data-stu-id="7d970-108">We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="7d970-109">[Le Gestionnaire de clés](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) distribuées (DKM) est une fonctionnalité côté client qui utilise un ensemble de clés secrètes pour chiffrer et déchiffrer des informations.</span><span class="sxs-lookup"><span data-stu-id="7d970-109">[Distributed Key Manager](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information.</span></span> <span data-ttu-id="7d970-110">Seuls les membres d’un groupe de sécurité spécifiques dans les services de domaine Active Directory peuvent accéder à ces clés dans le but de déchiffrer les données chiffrées par le Gestionnaire de clés distribuées.</span><span class="sxs-lookup"><span data-stu-id="7d970-110">Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM.</span></span> <span data-ttu-id="7d970-111">Dans Exchange Online, seuls certains comptes de service sous lesquels les processus Exchange sont exécutés font partie de ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7d970-111">In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group.</span></span> <span data-ttu-id="7d970-112">Dans le cadre de la procédure opérationnelle standard dans le centre de données, les informations d’identification qui font partie de ce groupe de sécurité ne sont communiquées à aucun être humain, et par conséquent aucun être humain n’a accès aux clés qui peuvent déchiffrer les informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="7d970-112">As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="7d970-p104">À des fins de débogage, de résolution des problèmes ou d’audit, un administrateur de centre de données doit demander un accès élevé pour obtenir des informations d’identification temporaires qui font partie du groupe de sécurité. Ce processus requiert plusieurs niveaux d’approbation juridique. Si l’accès est accordé, toutes les activités font l’objet d’une journalisation et d’un audit. En outre, l’accès est accordé uniquement pour un intervalle de temps défini suite auquel il expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d970-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="7d970-p105">Pour une protection supplémentaire, la technologie DKM inclut l’archivage et la substitution de clé automatisés. Ainsi, vous pouvez continuer à accéder à votre contenu plus ancien sans devoir utiliser la même clé indéfiniment.
</span><span class="sxs-lookup"><span data-stu-id="7d970-p105">For extra protection, DKM technology includes automated key rollover and archiving. This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="7d970-119">Où le Gestionnaire de clés distribuées est-il utilisé dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="7d970-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="7d970-120">Microsoft utilise [le Gestionnaire de clés](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) distribuées pour chiffrer vos secrets dans Exchange Online centres de données.</span><span class="sxs-lookup"><span data-stu-id="7d970-120">Microsoft uses [Distributed Key Manager](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) to encrypt your secrets in Exchange Online datacenters.</span></span> <span data-ttu-id="7d970-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7d970-121">For example:</span></span>
  
- <span data-ttu-id="7d970-p107">Les informations d’identification de compte de messagerie pour les comptes connectés. Les comptes connectés sont des comptes tiers, tels que les comptes de messagerie Hotmail, Gmail et Yahoo!.</span><span class="sxs-lookup"><span data-stu-id="7d970-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>

- <span data-ttu-id="7d970-125">Clé client.</span><span class="sxs-lookup"><span data-stu-id="7d970-125">Customer key.</span></span> <span data-ttu-id="7d970-126">Si vous utilisez le [chiffrement de service avec](customer-key-overview.md)la clé client, vous utiliserez [Azure Key Vault](/azure/key-vault/key-vault-whatis) pour protéger vos secrets.</span><span class="sxs-lookup"><span data-stu-id="7d970-126">If you are using [Service encryption with Customer Key](customer-key-overview.md), you'll use [Azure Key Vault](/azure/key-vault/key-vault-whatis) to safeguard your secrets.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d970-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d970-127">Related topics</span></span>

[<span data-ttu-id="7d970-128">Chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="7d970-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="7d970-129">Détails techniques de référence sur le chiffrement</span><span class="sxs-lookup"><span data-stu-id="7d970-129">Technical reference details about encryption</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="7d970-130">Assurance de service dans le Centre de &amp; conformité de la sécurité</span><span class="sxs-lookup"><span data-stu-id="7d970-130">Service assurance in the Security &amp; Compliance Center</span></span>](./service-assurance.md)
