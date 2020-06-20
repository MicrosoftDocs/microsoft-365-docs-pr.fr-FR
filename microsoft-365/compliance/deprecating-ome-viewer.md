---
title: Dépréciation de l’application visionneuse de chiffrement de messages
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6336cabb-b06e-402f-9e85-8bb9eb4ce68f
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: L’application visionneuse Office 365 message Encryption (OME) a été supprimée des magasins Android et Apple dans 2018.
ms.openlocfilehash: 9aca6fa2c0e9b276b666ffa187e3d18f061e7224
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817863"
---
# <a name="deprecating-message-encryption-viewer-app"></a><span data-ttu-id="4bca4-103">Dépréciation de l’application visionneuse de chiffrement de messages</span><span class="sxs-lookup"><span data-stu-id="4bca4-103">Deprecating Message Encryption Viewer App</span></span>

<span data-ttu-id="4bca4-104">Le 15 août 2018, nous avons supprimé l’application mobile Office 365 message Encryption (OME) dans les magasins Android et Apple.</span><span class="sxs-lookup"><span data-stu-id="4bca4-104">On August 15, 2018, we removed the Office 365 Message Encryption (OME) Viewer mobile app from Android and Apple stores.</span></span> <span data-ttu-id="4bca4-105">L’application mobile Office 365 message Encryption Viewer était nécessaire pour lire les messages électroniques et les pièces jointes chiffrés avec la version précédente de OME sur les téléphones Apple et Android.</span><span class="sxs-lookup"><span data-stu-id="4bca4-105">The Office 365 Message Encryption Viewer mobile app was required to read email messages and attachments that were encrypted with the previous version of OME on Apple and Android phones.</span></span> <span data-ttu-id="4bca4-106">Hormis la suppression de l’application de la visionneuse OME, nous n’avons aucune autre modification apportée à la version précédente de OME.</span><span class="sxs-lookup"><span data-stu-id="4bca4-106">Apart from removing the OME Viewer app, we are not making any other changes to the previous version of OME.</span></span>
  
## <a name="changes-from-august-2018"></a><span data-ttu-id="4bca4-107">Modifications du 2018 août</span><span class="sxs-lookup"><span data-stu-id="4bca4-107">Changes from August 2018</span></span>

<span data-ttu-id="4bca4-108">Comme annoncé en septembre 2017, nous avons publié une nouvelle version d' [Office 365 le chiffrement de messages](https://aka.ms/ome2017) pour permettre aux utilisateurs d’envoyer des messages chiffrés et protégés à des personnes à l’intérieur ou à l’extérieur de l’organisation sans qu’il soit nécessaire de l’application mobile.</span><span class="sxs-lookup"><span data-stu-id="4bca4-108">As announced September 2017, we have released a new version of [Office 365 Message Encryption](https://aka.ms/ome2017) so that users can send encrypted and protected messages to anyone inside or outside the organization without the requirement of the mobile app.</span></span> <span data-ttu-id="4bca4-109">Depuis, nous avons ajouté des fonctionnalités supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="4bca4-109">Since then, we've added additional capabilities:</span></span>
  
- [<span data-ttu-id="4bca4-110">Modèle de chiffrement uniquement</span><span class="sxs-lookup"><span data-stu-id="4bca4-110">Encrypt-only template</span></span>](https://aka.ms/encryptonly)

- [<span data-ttu-id="4bca4-111">Contrôle de déchiffrement des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="4bca4-111">Control to decrypt attachments</span></span>](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Admin-control-for-attachments-now-available-in-Office-365/ba-p/204007)
    
<span data-ttu-id="4bca4-112">Avec cette modification, les utilisateurs ne pourront plus télécharger l’application mobile Office 365 message Encryption Viewer depuis le 1er août.</span><span class="sxs-lookup"><span data-stu-id="4bca4-112">With this change, users will no longer be able to download the Office 365 Message Encryption Viewer mobile app beginning August 1.</span></span> <span data-ttu-id="4bca4-113">Par conséquent, les destinataires de messagerie peuvent ne pas être en mesure de lire les messages chiffrés avec la version précédente de OME sur certains appareils Android et Apple Mobile.</span><span class="sxs-lookup"><span data-stu-id="4bca4-113">As a result, mail recipients may not be able to read messages encrypted with the previous version of OME on some Android and Apple mobile devices.</span></span> <span data-ttu-id="4bca4-114">Toutefois, ils pourront toujours lire ces messages sur des ordinateurs personnels (via des navigateurs de bureau).</span><span class="sxs-lookup"><span data-stu-id="4bca4-114">However, they will still be able to read these messages on personal computers (via desktop browsers).</span></span> <span data-ttu-id="4bca4-115">Les utilisateurs qui ont déjà téléchargé l’application continueront à pouvoir l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4bca4-115">Users who have already downloaded the app will continue to be able to use it.</span></span>
  
## <a name="why-this-change-was-made"></a><span data-ttu-id="4bca4-116">Pourquoi cette modification a été effectuée ?</span><span class="sxs-lookup"><span data-stu-id="4bca4-116">Why this change was made</span></span>

<span data-ttu-id="4bca4-117">La nouvelle version de OME ne nécessite plus d’application mobile pour lire des messages électroniques protégés et des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="4bca4-117">The new version of OME no longer requires a mobile app to read protected email messages and attachments.</span></span> <span data-ttu-id="4bca4-118">Les clients qui utilisent les nouvelles fonctionnalités de OME peuvent afficher le message protégé dans Outlook Mobile et les non-clients peuvent afficher les messages protégés dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="4bca4-118">Customers using the new OME capabilities can view the protected message in Outlook mobile and non-customers can view protected messages in a browser.</span></span>
  
<span data-ttu-id="4bca4-119">Demander aux utilisateurs de télécharger une application mobile est un autre obstacle pour que les clients puissent afficher les messages protégés.</span><span class="sxs-lookup"><span data-stu-id="4bca4-119">Requiring users to download a mobile app is another hurdle for customers to view protected messages.</span></span> <span data-ttu-id="4bca4-120">Les nouvelles fonctionnalités de chiffrement des messages Office 365 offrent une meilleure expérience mobile.</span><span class="sxs-lookup"><span data-stu-id="4bca4-120">The new Office 365 Message Encryption capabilities provide a better mobile experience.</span></span>
  
## <a name="can-i-still-use-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="4bca4-121">Puis-je toujours utiliser la version précédente d’Office 365 de chiffrement de messages</span><span class="sxs-lookup"><span data-stu-id="4bca4-121">Can I still use the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="4bca4-122">La version précédente d’Office 365 le chiffrement de messages ne sera pas désapprouvée pour le moment, mais nous avons apporté des améliorations significatives à la nouvelle version du chiffrement de messages d’Office 365, ce qui facilite le chiffrement et la protection des données sensibles à quiconque et sur n’importe quel appareil, y compris la possibilité pour les utilisateurs de lire les messages protégés directement dans Outlook et Web).</span><span class="sxs-lookup"><span data-stu-id="4bca4-122">The previous version of Office 365 Message Encryption will not be deprecated at this time, however, we have made significant enhancements to the new version of Office 365 Message Encryption, which make it easier to encrypt and rights protect sensitive data to anyone and on any device - including the ability for users to read protected messages directly in Outlook (desktop, mobile, and web).</span></span> 
  
## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="4bca4-123">Que dois-je faire pour préparer cette modification ?</span><span class="sxs-lookup"><span data-stu-id="4bca4-123">What do I need to do to prepare for this change</span></span>

<span data-ttu-id="4bca4-124">Si votre organisation envoie actuellement des pièces jointes chiffrées aux destinataires qui nécessitent l’application de la visionneuse OME, vous devez mettre à jour votre documentation et les ressources de formation.</span><span class="sxs-lookup"><span data-stu-id="4bca4-124">If your organization currently sends encrypted attachments to recipients that require the OME Viewer app, you should update your documentation and training resources.</span></span>
  
<span data-ttu-id="4bca4-125">Nous vous recommandons de mettre à jour les règles de flux de messagerie Exchange existantes afin d’utiliser la version actuelle de OME afin que votre organisation puisse tirer parti des fonctionnalités nouvelles et améliorées.</span><span class="sxs-lookup"><span data-stu-id="4bca4-125">We recommend updating existing Exchange mail flow rules to use the current version of OME so that your organization can take advantage of the new and improved capabilities.</span></span> <span data-ttu-id="4bca4-126">Une fois que vous avez configuré les nouvelles fonctionnalités de OME, les destinataires n’ont pas besoin de l’application visionneuse OME pour lire les messages chiffrés sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4bca4-126">Once you have set up the new OME capabilities, recipients won't need the OME Viewer app to read encrypted messages on mobile devices.</span></span>
  
<span data-ttu-id="4bca4-127">Microsoft vous recommande de planifier la migration vers les nouvelles fonctionnalités de OME dès que cela est raisonnable pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4bca4-127">Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization.</span></span> <span data-ttu-id="4bca4-128">Pour obtenir des instructions, consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="4bca4-128">For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md).</span></span> <span data-ttu-id="4bca4-129">Si vous souhaitez en savoir plus sur la façon dont les nouvelles fonctionnalités fonctionnent en premier, consultez la rubrique [Office 365 message Encryption](ome.md).</span><span class="sxs-lookup"><span data-stu-id="4bca4-129">If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md).</span></span>
  

