---
title: Envoyer un message électronique chiffré
f1.keywords:
- NOCSH
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
- m365solution-smb
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
ms.openlocfilehash: af34d632ead2ae1e6ed81845c56b95b95af1dc51
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50911977"
---
# <a name="encrypt-or-label-your-sensitive-email"></a><span data-ttu-id="4e180-103">Chiffrer ou étiqueter votre courrier électronique sensible</span><span class="sxs-lookup"><span data-stu-id="4e180-103">Encrypt or label your sensitive email</span></span>

<span data-ttu-id="4e180-104">Vos données et informations de campagne sont importantes et souvent confidentielles.</span><span class="sxs-lookup"><span data-stu-id="4e180-104">Your data and campaign information is important and often confidential.</span></span> <span data-ttu-id="4e180-105">Protégez ces informations sensibles à l’aide d’étiquettes de chiffrement et de sensibilité afin que vos destinataires et vous-même traitiez les informations avec le niveau de sensibilité dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="4e180-105">Help protect this sensitive information by using encryption and sensitivity labels so you and your email recipients treat the information with the sensitivity it requires.</span></span>

## <a name="best-practices"></a><span data-ttu-id="4e180-106">Les bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="4e180-106">Best practices</span></span>

<span data-ttu-id="4e180-107">Avant d’envoyer des messages électroniques avec des informations confidentielles ou sensibles, envisagez d’allumer :</span><span class="sxs-lookup"><span data-stu-id="4e180-107">Before you send email with confidential or sensitive information, consider turning on:</span></span>

- <span data-ttu-id="4e180-108">**Chiffrement :** Vous pouvez chiffrer votre courrier électronique pour protéger la confidentialité des informations dans le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="4e180-108">**Encryption:** You can encrypt your email to protect the privacy of the information in the email.</span></span> <span data-ttu-id="4e180-109">Lorsque vous chiffrez un message électronique, il est converti du texte simple lisible en texte chiffré.</span><span class="sxs-lookup"><span data-stu-id="4e180-109">When you encrypt an email message, it's converted from readable plain text into scrambled cypher text.</span></span> <span data-ttu-id="4e180-110">Seul le destinataire qui possède la clé privée qui correspond à la clé publique utilisée pour chiffrer le message peut déchiffrer le message en lecture.</span><span class="sxs-lookup"><span data-stu-id="4e180-110">Only the recipient who has the private key that matches the public key used to encrypt the message can decipher the message for reading.</span></span> <span data-ttu-id="4e180-111">Toutefois, tout destinataire sans la clé privée correspondante voit un texte indéchiffrable.</span><span class="sxs-lookup"><span data-stu-id="4e180-111">Any recipient without the corresponding private key, however, sees indecipherable text.</span></span> <span data-ttu-id="4e180-112">Votre administrateur peut définir des règles pour chiffrer automatiquement les messages qui répondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="4e180-112">Your admin can define rules to automatically encrypt messages that meet certain criteria.</span></span> <span data-ttu-id="4e180-113">Par exemple, votre administrateur peut créer une règle qui chiffre tous les messages envoyés à l’extérieur de votre organisation ou tous les messages mentionnant des mots ou des expressions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4e180-113">For instance, your admin can create a rule that encrypts all messages sent outside your organization or all messages that mention specific words or phrases.</span></span> <span data-ttu-id="4e180-114">Toutes les règles de chiffrement seront appliquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4e180-114">Any encryption rules will be applied automatically.</span></span>
- <span data-ttu-id="4e180-115">**Étiquettes de sensibilité :** Votre campagne peut également configurer des étiquettes de confidentialité que vous pouvez appliquer à vos fichiers et courriers électroniques pour les maintenir conformes aux stratégies de protection des informations de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="4e180-115">**Sensitivity labels:** Your campaign can also set up sensitivity labels that you can apply to your files and email to keep them compliant with your campaign's information protection policies.</span></span> <span data-ttu-id="4e180-116">Lorsque vous définissez une étiquette, l’étiquette est persistante avec votre courrier électronique, même lorsqu’il est envoyé( par exemple, en apparaissant en tant qu’en-tête dans votre message.</span><span class="sxs-lookup"><span data-stu-id="4e180-116">When you set a label, the label persists with your email, even when it's sent - for example, by appearing as a header to your message.</span></span>

![Diagramme d’un e-mail avec des callouts pour les étiquettes et le chiffrement](../media/m365-campaign-email-encrypt.png)

## <a name="set-it-up"></a><span data-ttu-id="4e180-118">Configuration</span><span class="sxs-lookup"><span data-stu-id="4e180-118">Set it up</span></span>

<span data-ttu-id="4e180-119">Si vous souhaitez chiffrer un message qui ne répond pas à une règle prédéfinie ou si votre administrateur n’a pas défini de règles, vous pouvez appliquer différentes règles de chiffrement avant d’envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="4e180-119">If you want to encrypt a message that doesn't meet a pre-defined rule or your admin hasn't set up any rules, you can apply a variety of different encryption rules before you send the message.</span></span> <span data-ttu-id="4e180-120">Pour envoyer un message chiffré à partir d’Outlook 2013 ou 2016 ou d’Outlook 2016 pour Mac, sélectionnez **Options > Autorisations,** puis sélectionnez l’option de protection dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="4e180-120">To send an encrypted message from Outlook 2013 or 2016, or Outlook 2016 for Mac, select **Options > Permissions**, then select the protection option you need.</span></span> <span data-ttu-id="4e180-121">Vous pouvez également envoyer un message  chiffré en sélectionnant le bouton Protéger dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="4e180-121">You can also send an encrypted message by selecting the **Protect** button in Outlook on the web.</span></span> <span data-ttu-id="4e180-122">Pour plus d’informations, voir Envoyer, afficher et répondre à des messages chiffrés [dans Outlook pour PC.](https://support.microsoft.com/en-us/office/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)</span><span class="sxs-lookup"><span data-stu-id="4e180-122">For more information, see [Send, view, and reply to encrypted messages in Outlook for PC](https://support.microsoft.com/en-us/office/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980).</span></span>

## <a name="admin-settings"></a><span data-ttu-id="4e180-123">Paramètres d’administration</span><span class="sxs-lookup"><span data-stu-id="4e180-123">Admin settings</span></span>

<span data-ttu-id="4e180-124">Vous pouvez en savoir plus sur la configuration du chiffrement des e-mails sur le chiffrement de [courrier électronique dans Microsoft 365.](../compliance/email-encryption.md)</span><span class="sxs-lookup"><span data-stu-id="4e180-124">You can learn all about setting up email encryption at [Email encryption in Microsoft 365](../compliance/email-encryption.md).</span></span>

### <a name="automatically-encrypt-email-messages"></a><span data-ttu-id="4e180-125">Chiffrer automatiquement les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="4e180-125">Automatically encrypt email messages</span></span>

<span data-ttu-id="4e180-126">Les administrateurs peuvent créer des règles de flux de messagerie pour protéger automatiquement les messages électroniques envoyés et reçus à partir de votre campagne.</span><span class="sxs-lookup"><span data-stu-id="4e180-126">Admins can create mail flow rules to automatically protect email messages that are sent and received from your campaign.</span></span> <span data-ttu-id="4e180-127">Configurer des règles pour chiffrer les messages électroniques sortants et supprimer le chiffrement des messages chiffrés provenant de l’intérieur de votre organisation ou des réponses aux messages chiffrés envoyés à partir de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e180-127">Set up rules to encrypt any outgoing email messages, and remove encryption from encrypted messages coming from inside your organization or from replies to encrypted messages sent from your organization.</span></span>

<span data-ttu-id="4e180-128">Vous créez des règles de flux de messagerie pour chiffrer les messages électroniques avec les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME).</span><span class="sxs-lookup"><span data-stu-id="4e180-128">You create mail flow rules to encrypt email messages with the new Office 365 Message Encryption (OME) capabilities.</span></span> <span data-ttu-id="4e180-129">Définir des règles de flux de messagerie pour déclencher le chiffrement des messages avec les nouvelles fonctionnalités OME à l’aide du Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="4e180-129">Define mail flow rules for triggering message encryption with the new OME capabilities by using the Exchange Admin Center (EAC).</span></span> 

1. <span data-ttu-id="4e180-130">Dans un navigateur web, à l’aide d’un compte scolaire ou scolaire qui a reçu des autorisations d’administrateur général, connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="4e180-130">In a web browser, using a work or school account that has been granted global administrator permissions, sign in.</span></span>
2. <span data-ttu-id="4e180-131">Choisissez la vignette Administrateur.</span><span class="sxs-lookup"><span data-stu-id="4e180-131">Choose the Admin tile.</span></span>
3. <span data-ttu-id="4e180-132">Dans le Centre d’administration, **sélectionnez Centres d’administration > Exchange.**</span><span class="sxs-lookup"><span data-stu-id="4e180-132">In the admin center, choose **Admin centers > Exchange**.</span></span>

<span data-ttu-id="4e180-133">Pour plus d’informations, voir [Définir des règles de flux de messagerie pour chiffrer les messages électroniques.](../compliance/define-mail-flow-rules-to-encrypt-email.md)</span><span class="sxs-lookup"><span data-stu-id="4e180-133">For more information, see [Define mail flow rules to encrypt email messages](../compliance/define-mail-flow-rules-to-encrypt-email.md).</span></span>

### <a name="brand-your-encryption-messages"></a><span data-ttu-id="4e180-134">Brand your encryption messages</span><span class="sxs-lookup"><span data-stu-id="4e180-134">Brand your encryption messages</span></span>

<span data-ttu-id="4e180-135">Vous pouvez également appliquer la personnalisation de votre campagne pour personnaliser l’apparence et le texte des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="4e180-135">You can also apply your campaign branding to customize the look and the text in the email messages.</span></span> <span data-ttu-id="4e180-136">Pour plus d’informations, voir Ajouter la marque de votre organisation [à vos messages chiffrés.](../compliance/email-encryption.md)</span><span class="sxs-lookup"><span data-stu-id="4e180-136">For more information, see [Add your organization's brand to your encrypted messages](../compliance/email-encryption.md).</span></span>