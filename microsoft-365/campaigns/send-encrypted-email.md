---
title: Envoyer un message électronique chiffré
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.date: 9/20/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-Campaigns
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 496e690b-b75d-4ff5-bf34-cc32905d0364
description: Découvrez comment envoyer des messages chiffrés à l’aide d’Outlook.
ms.openlocfilehash: e58a69c25c00a0482d3837d9bde626ec0a54936f
ms.sourcegitcommit: 75b97d1ff617bc4b1b0ef9135dfe6a8842ea1b52
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35772321"
---
# <a name="encrypt-or-label-your-sensitive-email"></a><span data-ttu-id="bd966-103">Chiffrer ou étiqueter votre courrier électronique sensible</span><span class="sxs-lookup"><span data-stu-id="bd966-103">Encrypt or label your sensitive email</span></span>

<span data-ttu-id="bd966-104">Les données et les informations de votre campagne sont importantes et souvent confidentielles.</span><span class="sxs-lookup"><span data-stu-id="bd966-104">Your data and campaign information is important and often confidential.</span></span> <span data-ttu-id="bd966-105">Protégez ces informations sensibles en utilisant des étiquettes de chiffrement et de confidentialité pour que vous et vos destinataires de courrier traitent les informations dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="bd966-105">Help protect this sensitive information by using encryption and sensitivity labels so you and your email recipients treat the information with the sensitivity it requires.</span></span>


## <a name="best-practices"></a><span data-ttu-id="bd966-106">Meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="bd966-106">Best practices</span></span>

<span data-ttu-id="bd966-107">Avant d’envoyer un courrier électronique avec des informations confidentielles ou sensibles, envisagez d’activer:</span><span class="sxs-lookup"><span data-stu-id="bd966-107">Before you send email with confidential or sensitive information, consider turning on:</span></span>

- <span data-ttu-id="bd966-108">**Chiffrement:** Vous pouvez chiffrer votre courrier électronique pour protéger la confidentialité des informations contenues dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="bd966-108">**Encryption:** You can encrypt your email to protect the privacy of the information in the email.</span></span> <span data-ttu-id="bd966-109">Lorsque vous chiffrez un message électronique, il est converti du texte brut lisible en texte Cypher brouillé.</span><span class="sxs-lookup"><span data-stu-id="bd966-109">When you encrypt an email message, it's converted from readable plain text into scrambled cypher text.</span></span> <span data-ttu-id="bd966-110">Seul le destinataire qui dispose de la clé privée correspondant à la clé publique utilisée pour chiffrer le message peut déchiffrer le message en lecture.</span><span class="sxs-lookup"><span data-stu-id="bd966-110">Only the recipient who has the private key that matches the public key used to encrypt the message can decipher the message for reading.</span></span> <span data-ttu-id="bd966-111">Tout destinataire sans clé privée correspondante voit le texte indéchiffrable.</span><span class="sxs-lookup"><span data-stu-id="bd966-111">Any recipient without the corresponding private key, however, sees indecipherable text.</span></span> <span data-ttu-id="bd966-112">Votre administrateur peut définir des règles pour chiffrer automatiquement les messages qui répondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="bd966-112">Your admin can define rules to automatically encrypt messages that meet certain criteria.</span></span> <span data-ttu-id="bd966-113">Par exemple, votre administrateur peut créer une règle qui chiffre tous les messages envoyés en dehors de votre organisation ou tous les messages qui mentionnent des mots ou des expressions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="bd966-113">For instance, your admin can create a rule that encrypts all messages sent outside your organization or all messages that mention specific words or phrases.</span></span> <span data-ttu-id="bd966-114">Toutes les règles de chiffrement seront appliquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="bd966-114">Any encryption rules will be applied automatically.</span></span>
- <span data-ttu-id="bd966-115">**Étiquettes de sensibilité:** Votre campagne peut également configurer des étiquettes de confidentialité que vous pouvez appliquer à vos fichiers et à vos courriers électroniques pour les garder en conformité avec les stratégies de protection des informations de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="bd966-115">**Sensitivity labels:** Your campaign can also set up sensitivity labels that you can apply to your files and email to keep them compliant with your campaign's information protection policies.</span></span> <span data-ttu-id="bd966-116">Lorsque vous définissez une étiquette, celle-ci est conservée dans votre courrier électronique, même si elle est envoyée, par exemple, en apparaissant comme en-tête de votre message.</span><span class="sxs-lookup"><span data-stu-id="bd966-116">When you set a label, the label persists with your email, even when it's sent - for example, by appearing as a header to your message.</span></span>

![Diagramme d’un message avec des légendes pour les étiquettes et le chiffrement](media/m365-campaign-email-encrypt.png)


## <a name="set-it-up"></a><span data-ttu-id="bd966-118">Configuration</span><span class="sxs-lookup"><span data-stu-id="bd966-118">Set it up</span></span>

<span data-ttu-id="bd966-119">Si vous souhaitez chiffrer un message qui ne correspond pas à une règle prédéfinie ou que votre administrateur n’a pas défini de règles, vous pouvez appliquer diverses règles de chiffrement avant d’envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="bd966-119">If you want to encrypt a message that doesn't meet a pre-defined rule or your admin hasn't set up any rules, you can apply a variety of different encryption rules before you send the message.</span></span> <span data-ttu-id="bd966-120">Pour envoyer un message chiffré à partir d’Outlook 2013 ou 2016, ou Outlook 2016 pour Mac, sélectionnez **Options > autorisations**, puis sélectionnez l’option de protection dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="bd966-120">To send an encrypted message from Outlook 2013 or 2016, or Outlook 2016 for Mac, select **Options > Permissions**, then select the protection option you need.</span></span> <span data-ttu-id="bd966-121">Vous pouvez également envoyer un message chiffré en sélectionnant le bouton **protéger** dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="bd966-121">You can also send an encrypted message by selecting the **Protect** button in Outlook on the web.</span></span> <span data-ttu-id="bd966-122">Pour plus d’informations, consultez la rubrique [Envoyer, afficher et répondre à des messages chiffrés dans Outlook pour PC](https://support.office.com/en-us/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="bd966-122">For more information, see [Send, view, and reply to encrypted messages in Outlook for PC](https://support.office.com/en-us/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980?ui=en-US&rs=en-US&ad=US).</span></span>

## <a name="admin-settings"></a><span data-ttu-id="bd966-123">Paramètres d’administration</span><span class="sxs-lookup"><span data-stu-id="bd966-123">Admin settings</span></span>

<span data-ttu-id="bd966-124">Vous pouvez en savoir plus sur la configuration du chiffrement du courrier électronique à [l’adresse de chiffrement de courrier électronique dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/email-encryption).</span><span class="sxs-lookup"><span data-stu-id="bd966-124">You can learn all about setting up email encryption at [Email encryption in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/email-encryption).</span></span>

### <a name="automatically-encrypt-email-messages"></a><span data-ttu-id="bd966-125">Chiffrer automatiquement les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="bd966-125">Automatically encrypt email messages</span></span>

<span data-ttu-id="bd966-126">Les administrateurs peuvent créer des règles de flux de messagerie pour protéger automatiquement les messages électroniques qui sont envoyés et reçus de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="bd966-126">Admins can create mail flow rules to automatically protect email messages that are sent and received from your campaign.</span></span> <span data-ttu-id="bd966-127">Configurez des règles pour chiffrer les messages électroniques sortants et supprimez le chiffrement des messages chiffrés provenant de votre organisation ou des réponses aux messages chiffrés envoyés par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bd966-127">Set up rules to encrypt any outgoing email messages, and remove encryption from encrypted messages coming from inside your organization or from replies to encrypted messages sent from your organization.</span></span> 

<span data-ttu-id="bd966-128">Vous créez des règles de flux de messagerie pour chiffrer les messages électroniques avec les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME).</span><span class="sxs-lookup"><span data-stu-id="bd966-128">You create mail flow rules to encrypt email messages with the new Office 365 Message Encryption (OME) capabilities.</span></span> <span data-ttu-id="bd966-129">Définir des règles de flux de messagerie pour déclencher le chiffrement des messages avec les nouvelles fonctionnalités de OME à l’aide du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd966-129">Define mail flow rules for triggering message encryption with the new OME capabilities by using the Exchange Admin Center (EAC).</span></span> 

1. <span data-ttu-id="bd966-130">Dans un navigateur Web, à l’aide d’un compte professionnel ou scolaire auquel des autorisations d’administrateur général ont été accordées, connectez-vous à Office 365.</span><span class="sxs-lookup"><span data-stu-id="bd966-130">In a web browser, using a work or school account that has been granted global administrator permissions, sign in to Office 365.</span></span> 
2. <span data-ttu-id="bd966-131">Sélectionnez la vignette admin.</span><span class="sxs-lookup"><span data-stu-id="bd966-131">Choose the Admin tile.</span></span> 
3. <span data-ttu-id="bd966-132">Dans le centre d’administration Office 365, sélectionnez **centres d’administration > Exchange**.</span><span class="sxs-lookup"><span data-stu-id="bd966-132">In the Office 365 admin center, choose **Admin centers > Exchange**.</span></span> 

<span data-ttu-id="bd966-133">Pour plus d’informations, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/define-mail-flow-rules-to-encrypt-email).</span><span class="sxs-lookup"><span data-stu-id="bd966-133">For more information, see [Define mail flow rules to encrypt email messages in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/define-mail-flow-rules-to-encrypt-email).</span></span>

### <a name="brand-your-encryption-messages"></a><span data-ttu-id="bd966-134">Personnaliser vos messages de chiffrement</span><span class="sxs-lookup"><span data-stu-id="bd966-134">Brand your encryption messages</span></span>

<span data-ttu-id="bd966-135">Vous pouvez également appliquer votre personnalisation de campagne pour personnaliser l’apparence et le texte dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="bd966-135">You can also apply your campaign branding to customize the look and the text in the email messages.</span></span> <span data-ttu-id="bd966-136">Pour plus d’informations, reportez-vous à la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés](https://docs.microsoft.com/en-us/office365/securitycompliance/email-encryption).</span><span class="sxs-lookup"><span data-stu-id="bd966-136">For more information, see [Add your organization's brand to your encrypted messages](https://docs.microsoft.com/en-us/office365/securitycompliance/email-encryption).</span></span>

