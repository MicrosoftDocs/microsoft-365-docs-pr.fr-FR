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
description: En plus du centre de gestion de la confidentialité Office 365 qui fournit des informations sur la sécurité, la confidentialité et la conformité pour Office 365, vous souhaiterez peut-être savoir comment Office 365 protège les secrets que vous fournissez dans ses centres de données. Nous utilisons une technologie appelée Distributed Key Manager (DKM).
ms.openlocfilehash: 6ba60616ee72a4457d81f3f9c2049007afdcbb1d
ms.sourcegitcommit: 5ff1dc62e8855be155cb2de45cf4ee5a02c321fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2020
ms.locfileid: "41800074"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="b4e56-104">Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b4e56-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="b4e56-105">Cet article décrit la façon dont Microsoft protège les informations confidentielles figurant dans vos courriers électroniques dans ses centres de données.</span><span class="sxs-lookup"><span data-stu-id="b4e56-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="b4e56-106">Comment sécurisons-nous les informations confidentielles que vous indiquez ?</span><span class="sxs-lookup"><span data-stu-id="b4e56-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="b4e56-107">En plus du centre de gestion de la confidentialité Office 365 qui fournit [des informations sur la sécurité, la confidentialité et la conformité pour office 365](https://go.microsoft.com/fwlink/?linkid=874644), vous souhaiterez peut-être savoir comment Office 365 protège les secrets que vous fournissez dans ses centres de données.</span><span class="sxs-lookup"><span data-stu-id="b4e56-107">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters.</span></span> <span data-ttu-id="b4e56-108">Nous utilisons une technologie appelée Distributed Key Manager (DKM).</span><span class="sxs-lookup"><span data-stu-id="b4e56-108">We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="b4e56-109">Le [Gestionnaire de clés distribuées](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) (DKM) est une fonctionnalité côté client qui utilise un ensemble de clés secrètes pour chiffrer et déchiffrer les informations.</span><span class="sxs-lookup"><span data-stu-id="b4e56-109">[Distributed Key Manager](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information.</span></span> <span data-ttu-id="b4e56-110">Seuls les membres d’un groupe de sécurité spécifiques dans les services de domaine Active Directory peuvent accéder à ces clés dans le but de déchiffrer les données chiffrées par le Gestionnaire de clés distribuées.</span><span class="sxs-lookup"><span data-stu-id="b4e56-110">Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM.</span></span> <span data-ttu-id="b4e56-111">Dans Exchange Online, seuls certains comptes de service sous lesquels les processus Exchange sont exécutés font partie de ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b4e56-111">In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group.</span></span> <span data-ttu-id="b4e56-112">Dans le cadre de la procédure opérationnelle standard dans le centre de données, les informations d’identification qui font partie de ce groupe de sécurité ne sont communiquées à aucun être humain, et par conséquent aucun être humain n’a accès aux clés qui peuvent déchiffrer les informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="b4e56-112">As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="b4e56-p104">À des fins de débogage, de résolution des problèmes ou d’audit, un administrateur de centre de données doit demander un accès élevé pour obtenir des informations d’identification temporaires qui font partie du groupe de sécurité. Ce processus requiert plusieurs niveaux d’approbation juridique. Si l’accès est accordé, toutes les activités font l’objet d’une journalisation et d’un audit. En outre, l’accès est accordé uniquement pour un intervalle de temps défini suite auquel il expire automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b4e56-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="b4e56-117">Pour une protection supplémentaire, la technologie DKM inclut l’archivage et la substitution de clé automatisés.</span><span class="sxs-lookup"><span data-stu-id="b4e56-117">For extra protection, DKM technology includes automated key rollover and archiving.</span></span> <span data-ttu-id="b4e56-118">Ainsi, vous pouvez continuer à accéder à votre contenu plus ancien sans devoir utiliser la même clé indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="b4e56-118">This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="b4e56-119">Où le Gestionnaire de clés distribuées est-il utilisé dans Exchange Online ?</span><span class="sxs-lookup"><span data-stu-id="b4e56-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="b4e56-120">Microsoft utilise le [Gestionnaire de clés distribuées](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) pour chiffrer vos secrets dans les centres de distribution Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b4e56-120">Microsoft uses [Distributed Key Manager](office-365-bitlocker-and-distributed-key-manager-for-encryption.md) to encrypt your secrets in Exchange Online datacenters.</span></span> <span data-ttu-id="b4e56-121">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b4e56-121">For example:</span></span>
  
- <span data-ttu-id="b4e56-122">Informations d’identification du compte de messagerie pour les comptes connectés.</span><span class="sxs-lookup"><span data-stu-id="b4e56-122">Email account credentials for connected accounts.</span></span> <span data-ttu-id="b4e56-123">Les comptes connectés sont des comptes tiers, tels que Hotmail, Gmail et Yahoo !.</span><span class="sxs-lookup"><span data-stu-id="b4e56-123">Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo!</span></span> <span data-ttu-id="b4e56-124">comptes de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b4e56-124">mail accounts.</span></span>

- <span data-ttu-id="b4e56-125">Clé client.</span><span class="sxs-lookup"><span data-stu-id="b4e56-125">Customer key.</span></span> <span data-ttu-id="b4e56-126">Si vous utilisez le [chiffrement de service avec la clé client dans Office 365](customer-key-overview.md), vous utiliserez [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) pour protéger vos secrets.</span><span class="sxs-lookup"><span data-stu-id="b4e56-126">If you are using [Service encryption with Customer Key in Office 365](customer-key-overview.md), you'll use [Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-whatis) to safeguard your secrets.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4e56-127">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="b4e56-127">Related topics</span></span>

[<span data-ttu-id="b4e56-128">Chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b4e56-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="b4e56-129">Détails techniques de référence sur le chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b4e56-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="b4e56-130">Garantie de service dans le centre de &amp; sécurité conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="b4e56-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  

