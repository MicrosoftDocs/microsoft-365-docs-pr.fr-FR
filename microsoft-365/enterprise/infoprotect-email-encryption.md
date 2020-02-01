---
title: 'Étape 6 : Configurer le chiffrement des e-mails'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.custom: ''
description: Familiarisez-vous avec la gestion des accès privilégiés pour Office 365 et apprenez à la configurer.
ms.openlocfilehash: 252a5f76197deb1034d200553308a281ef079957
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600921"
---
# <a name="step-6-configure-email-encryption"></a><span data-ttu-id="783e4-103">Étape 6 : Configurer le chiffrement des e-mails</span><span class="sxs-lookup"><span data-stu-id="783e4-103">Step 6: Configure email encryption</span></span>

<span data-ttu-id="783e4-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="783e4-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : Protection des informations](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="783e4-106">Il existe trois types de chiffrement de courrier électronique dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="783e4-106">There are three types of email encryption in Microsoft 365.</span></span>

|||
|:-------|:-----|
| <span data-ttu-id="783e4-107">Chiffrement des messages Office (OME)</span><span class="sxs-lookup"><span data-stu-id="783e4-107">Office Message Encryption (OME)</span></span> | <span data-ttu-id="783e4-108">Chiffrement pour le courrier électronique Exchange Online envoyé à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="783e4-108">Encryption for Exchange Online email sent outside your organization.</span></span> |
| <span data-ttu-id="783e4-109">Gestion des droits relatifs à l'information (IRM)</span><span class="sxs-lookup"><span data-stu-id="783e4-109">Information Rights Management (IRM)</span></span> | <span data-ttu-id="783e4-110">Le chiffrement et les autorisations qui transitent avec le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="783e4-110">Encryption and permissions that travel with the email.</span></span> |
| <span data-ttu-id="783e4-111">S/MIME (Secure/Multipurpose Internet Mail Extension)</span><span class="sxs-lookup"><span data-stu-id="783e4-111">Secure/Multipurpose Internet Mail Extensions (S/MIME)</span></span> | <span data-ttu-id="783e4-112">Protection de la messagerie avec chiffrement et signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="783e4-112">Email protection with encryption and digital signatures.</span></span> |
|||

## <a name="office-365-message-encryption"></a><span data-ttu-id="783e4-113">Chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="783e4-113">Office 365 Message Encryption</span></span>

<span data-ttu-id="783e4-114">Avec OME, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l’intérieur et à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="783e4-114">With OME, your organization can send and receive encrypted email messages between people inside and outside your organization.</span></span> <span data-ttu-id="783e4-115">OME fonctionne avec Outlook.com, Yahoo !, Gmail et d’autres services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="783e4-115">OME works with Outlook.com, Yahoo!, Gmail, and other email services.</span></span> <span data-ttu-id="783e4-116">Le chiffrement des messages électroniques permet de s’assurer que seuls les destinataires prévus peuvent afficher le message.</span><span class="sxs-lookup"><span data-stu-id="783e4-116">Email message encryption helps ensure that only intended recipients can view the message.</span></span>

![Chiffrement des messages électroniques OME](./media/infoprotect-email-encryption/ome-encryption.png)

<span data-ttu-id="783e4-118">Vous configurez des règles de transport qui définissent les conditions de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="783e4-118">You set up transport rules that define the conditions for encryption.</span></span> <span data-ttu-id="783e4-119">Lorsqu’un utilisateur envoie un message qui correspond à une règle, le chiffrement est automatiquement appliqué.</span><span class="sxs-lookup"><span data-stu-id="783e4-119">When a user sends a message that matches a rule, encryption is applied automatically.</span></span>

<span data-ttu-id="783e4-120">Pour afficher les messages chiffrés, les destinataires peuvent obtenir un code secret à usage unique, se connecter avec un compte Microsoft ou se connecter avec un compte professionnel ou scolaire associé à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="783e4-120">To view encrypted messages, recipients can either get a one-time passcode, sign in with a Microsoft account, or sign in with a work or school account associated with Microsoft 365.</span></span> <span data-ttu-id="783e4-121">Les destinataires peuvent également envoyer des réponses chiffrées.</span><span class="sxs-lookup"><span data-stu-id="783e4-121">Recipients can also send encrypted replies.</span></span> <span data-ttu-id="783e4-122">Ils n’ont pas besoin de leur propre abonnement Microsoft 365 pour afficher les messages chiffrés ou envoyer des réponses chiffrées.</span><span class="sxs-lookup"><span data-stu-id="783e4-122">They don't need their own Microsoft 365 subscription to view encrypted messages or send encrypted replies.</span></span>

<span data-ttu-id="783e4-123">Pour plus d'informations, consultez la rubrique [Chiffrement dans Office 365](https://docs.microsoft.com/Office365/SecurityCompliance/ome).</span><span class="sxs-lookup"><span data-stu-id="783e4-123">For more information, see [Office 365 Message Encryption](https://docs.microsoft.com/Office365/SecurityCompliance/ome).</span></span>

## <a name="irm"></a><span data-ttu-id="783e4-124">IRM</span><span class="sxs-lookup"><span data-stu-id="783e4-124">IRM</span></span>

<span data-ttu-id="783e4-125">La gestion des droits relatifs à l’information (IRM) dans Microsoft 365 vous aide à sécuriser vos informations avec un chiffrement supplémentaire et à appliquer une stratégie intelligente qui indique qui a accès à ce qu’ils peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="783e4-125">IRM in Microsoft 365 helps you secure your information with additional encryption and by applying an intelligent policy that specifies who has access what they can do.</span></span> <span data-ttu-id="783e4-126">Pour les messages électroniques, vous pouvez utiliser IRM pour le chiffrement et appliquer des restrictions d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="783e4-126">For email messages, you can use IRM for encryption and to apply usage restrictions.</span></span> <span data-ttu-id="783e4-127">Par exemple, vous pouvez spécifier que certains destinataires disposent de toutes les capacités pour gérer le courrier électronique et que d’autres n’ont pas la possibilité d’imprimer ou de transférer le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="783e4-127">For example, you can specify that some recipients have all abilities to manage the email and some do not have the ability to print or forward the email.</span></span> 

<span data-ttu-id="783e4-128">Les stratégies IRM sont configurées dans Microsoft 365 et peuvent s’appliquer à des documents dans SharePoint Online et des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="783e4-128">IRM policies are configured within Microsoft 365 and can apply to documents in SharePoint Online and email messages.</span></span> <span data-ttu-id="783e4-129">Un message électronique protégé par IRM inclut les paramètres de stratégie appliqués et en voyage avec.</span><span class="sxs-lookup"><span data-stu-id="783e4-129">An IRM-protected email includes the applied policy settings applied and travel with it.</span></span> 

![Protection IRM des messages électroniques](./media/infoprotect-email-encryption/irm-protection.png)

<span data-ttu-id="783e4-131">Lorsque le destinataire ouvre le courrier électronique avec la stratégie incluse, les paramètres de stratégie sont utilisés pour déchiffrer le message et déterminer ce que le destinataire peut faire avec.</span><span class="sxs-lookup"><span data-stu-id="783e4-131">When the recipient opens the email with the included policy, the policy settings are used to decrypt the message and determine what the recipient can do with it.</span></span> 

<span data-ttu-id="783e4-132">Pour plus d'informations, consultez la rubrique [Gestion des droits relatifs à l'information (IRM) dans Exchange Online]( https://docs.microsoft.com/office365/SecurityCompliance/information-rights-management-in-exchange-online).</span><span class="sxs-lookup"><span data-stu-id="783e4-132">For more information, see [Information Rights Management in Exchange Online]( https://docs.microsoft.com/office365/SecurityCompliance/information-rights-management-in-exchange-online).</span></span>

## <a name="smime"></a><span data-ttu-id="783e4-133">S/MIME</span><span class="sxs-lookup"><span data-stu-id="783e4-133">S/MIME</span></span>

<span data-ttu-id="783e4-134">S/MIME est une solution de protection de messagerie numérique basée sur des certificats, qui vous permet de chiffrer et de signer numériquement un message.</span><span class="sxs-lookup"><span data-stu-id="783e4-134">S/MIME is a digital certificate-based email-based protection solution that allows you to both encrypt and digitally sign a message.</span></span> <span data-ttu-id="783e4-135">Le chiffrement des messages permet de garantir que seul le destinataire prévu puisse ouvrir et lire le message.</span><span class="sxs-lookup"><span data-stu-id="783e4-135">The message encryption helps ensure that only the intended recipient can open and read the message.</span></span> <span data-ttu-id="783e4-136">Une signature numérique permet au destinataire de valider l’identité de l’expéditeur et de déterminer que seul l’expéditeur aurait pu l’envoyer.</span><span class="sxs-lookup"><span data-stu-id="783e4-136">A digital signature helps the recipient validate the identity of the sender and determine that only the sender could have sent it.</span></span>

![Protection S/MIME des messages électroniques](./media/infoprotect-email-encryption/smime-protection.png)

<span data-ttu-id="783e4-138">S/MIME peut être utilisé pour envoyer des courriers électroniques à d’autres boîtes aux lettres dans votre abonnement Microsoft 365 ou à des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="783e4-138">S/MIME can be used for email to other mailboxes in your Microsoft 365 subscription or to external users.</span></span>
<span data-ttu-id="783e4-139">Le chiffrement de messages et les signatures numériques sont rendus possibles grâce à l’utilisation de certificats numériques qui contiennent les clés publique et privée pour le chiffrement ou le déchiffrement des messages, ainsi que la création et la vérification des signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="783e4-139">Both message encryption and digital signatures are made possible through the use of digital certificates that contain the public and private keys for encrypting or decrypting messages and creating and verifying digital signatures.</span></span>
<span data-ttu-id="783e4-140">Pour utiliser S/MIME, vous devez disposer des clés publiques pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="783e4-140">To use S/MIME, you must have the public keys for each recipient.</span></span> <span data-ttu-id="783e4-141">Les destinataires conservent leurs propres clés privées, qui doivent rester sécurisées.</span><span class="sxs-lookup"><span data-stu-id="783e4-141">Recipients maintain their own private keys, which must remain secure.</span></span> <span data-ttu-id="783e4-142">Si votre clé privée est compromise, vous devez obtenir un nouveau certificat numérique et redistribuer les clés publiques à tous les expéditeurs potentiels.</span><span class="sxs-lookup"><span data-stu-id="783e4-142">If your private key is compromised, you need to get a new digital certificate and redistribute public keys to all potential senders.</span></span>

<span data-ttu-id="783e4-143">Pour plus d'informations, reportez-vous à la rubrique [S/MIME pour la signature et le chiffrement des messages](https://docs.microsoft.com/Exchange/policy-and-compliance/smime).</span><span class="sxs-lookup"><span data-stu-id="783e4-143">For more information, see [S/MIME for message signing and encryption](https://docs.microsoft.com/Exchange/policy-and-compliance/smime).</span></span>


<span data-ttu-id="783e4-144">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step6) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="783e4-144">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step6) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="783e4-145">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="783e4-145">Next step</span></span>

|||
|:-------|:-----|
|![Étape 7](./media/stepnumbers/Step7.png)|[<span data-ttu-id="783e4-147">Configurez la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="783e4-147">Configure privileged access management for Office 365</span></span>](infoprotect-configure-privileged-access-management.md)|
