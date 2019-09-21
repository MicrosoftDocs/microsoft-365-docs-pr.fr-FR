---
title: Dépannage et informations relatives au support
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5d9f75f5-bb7f-458c-ad30-5c8eae0b0e4e
ms.collection:
- M365-security-compliance
description: Cette rubrique décrit les étapes de résolution des problèmes pour les utilisateurs finaux et les administrateurs, et fournit des informations sur la manière de contacter le support technique pour obtenir de l'aide.
ms.openlocfilehash: 2a8019ed58bfb88183d20a8292bd5a30d9b43f13
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080395"
---
# <a name="troubleshooting-and-support-information"></a><span data-ttu-id="46123-103">Dépannage et informations relatives au support</span><span class="sxs-lookup"><span data-stu-id="46123-103">Troubleshooting and support information</span></span>

<span data-ttu-id="46123-104">Cette rubrique décrit les étapes de résolution des problèmes pour les utilisateurs finaux et les administrateurs, et fournit des informations sur la manière de contacter le support technique pour obtenir de l'aide.</span><span class="sxs-lookup"><span data-stu-id="46123-104">This topic describes troubleshooting steps for end users and administrators, and provides information about how to contact technical support for assistance.</span></span>
  
## <a name="troubleshooting-for-users"></a><span data-ttu-id="46123-105">Résolution des problèmes pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="46123-105">Troubleshooting for Users</span></span>

<span data-ttu-id="46123-p101">Parfois, vous pouvez rencontrez des difficultés après l'ajout du complément Junk Email Reporting (signalement des courriers indésirables) dans Microsoft Office Outlook. Voici certains problèmes que vous pouvez rencontrer ainsi que des conseils pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="46123-p101">Occasionally, you may experience trouble with Microsoft Office Outlook after adding the Junk Email Reporting Add-In. Following are problems that you may encounter, along with tips for resolving these issues.</span></span> 
  
- <span data-ttu-id="46123-108">Rien ne se passe quand vous cliquez sur **Signaler le courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="46123-108">Nothing happens when you click **Report Junk**</span></span>
    
- <span data-ttu-id="46123-109">Outlook cesse de répondre après avoir sélectionné un message électronique</span><span class="sxs-lookup"><span data-stu-id="46123-109">Outlook stops responding after you select an email message</span></span>
    
- <span data-ttu-id="46123-110">Le courrier indésirable signalé ne peut pas être remis en raison d'une réponse « Non remis ».</span><span class="sxs-lookup"><span data-stu-id="46123-110">Reported junk mail cannot be delivered due to an "undeliverable" reply</span></span>
    
### <a name="troubleshooting-tip"></a><span data-ttu-id="46123-111">Conseil de dépannage</span><span class="sxs-lookup"><span data-stu-id="46123-111">Troubleshooting tip</span></span>

1. <span data-ttu-id="46123-112">Fermez et redémarrez Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="46123-112">Close and restart Microsoft Office Outlook.</span></span>
    
2. <span data-ttu-id="46123-p102">Vérifiez que vous êtes en mesure de créer et d'envoyer un message de test. Pour ce faire, vous pouvez envoyer un message de test à un autre compte de messagerie que vous gérez, puis vérifiez que ce message électronique vous est remis.</span><span class="sxs-lookup"><span data-stu-id="46123-p102">Verify that you are able to create and send a test message. To do this, you can send a test message to another email account that you are responsible for, and then verify that the email message is received.</span></span>
    
<span data-ttu-id="46123-115">Si le problème persiste, contactez votre administrateur informatique.</span><span class="sxs-lookup"><span data-stu-id="46123-115">If the problem persists, contact your IT administrator.</span></span>
  
> [!TIP]
> <span data-ttu-id="46123-p103">Vous pouvez également envoyer directement des messages de courrier indésirable à Microsoft, à l'adresse électronique [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com), et des messages faux positifs à l'adresse électronique [not_junk@office365.microsoft.com](mailto: not_junk@office365.microsoft.com). Pour plus d'informations, consultez la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="46123-p103">You can also submit spam messages directly to Microsoft by using the [junk@office365.microsoft.com](mailto:junk@office365.microsoft.com) email address, and false positive messages by using the [not_junk@office365.microsoft.com](mailto: not_junk@office365.microsoft.com) email address. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
## <a name="troubleshooting-for-administrators"></a><span data-ttu-id="46123-118">Résolution des problèmes pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="46123-118">Troubleshooting for Administrators</span></span>

<span data-ttu-id="46123-p104">En tant qu'administrateur, vous pouvez rencontrer des problèmes avec des utilisateurs qui se servent du complément Junk Email Reporting (signalement des courriers indésirables) pour Microsoft Office Outlook. Voici quelques conseils pour résoudre les problèmes que vous pourriez rencontrer.</span><span class="sxs-lookup"><span data-stu-id="46123-p104">As an administrator, you might experience issues with users using the Junk Email Reporting Add-in for Microsoft Office Outlook. Following are some tips for resolving problems that you might encounter.</span></span> 
  
 <span data-ttu-id="46123-121">**Problème :** un message d'erreur demandant aux utilisateurs de contacter leur administrateur système apparaît sans cesse.</span><span class="sxs-lookup"><span data-stu-id="46123-121">**Problem:** An error message asking users to contact their system administrator continually appears.</span></span> 
  
### <a name="troubleshooting-tip"></a><span data-ttu-id="46123-122">Conseil de dépannage</span><span class="sxs-lookup"><span data-stu-id="46123-122">Troubleshooting tip</span></span>

1. <span data-ttu-id="46123-123">Définissez la valeur de la clé de Registre suivante sur « Verbose » :</span><span class="sxs-lookup"><span data-stu-id="46123-123">Set the following registry key value to "Verbose":</span></span>
    
  - <span data-ttu-id="46123-124">**Outlook 32 bits installé sur un système d'exploitation 32 bits :**</span><span class="sxs-lookup"><span data-stu-id="46123-124">**32 bit Outlook installed on a 32 bit operating system:**</span></span>
    
    <span data-ttu-id="46123-125">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span><span class="sxs-lookup"><span data-stu-id="46123-125">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span></span>
    
  - <span data-ttu-id="46123-126">**Outlook 32 bits installé sur un système d'exploitation 64 bits :**</span><span class="sxs-lookup"><span data-stu-id="46123-126">**32 bit Outlook installed on a 64 bit operating system:**</span></span>
    
    <span data-ttu-id="46123-127">HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span><span class="sxs-lookup"><span data-stu-id="46123-127">HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span></span>
    
  - <span data-ttu-id="46123-128">**Outlook 64 bits (toujours installé sur un système d'exploitation 64 bits) :**</span><span class="sxs-lookup"><span data-stu-id="46123-128">**64 bit Outlook (always installed on a 64 bit operating system):**</span></span>
    
    <span data-ttu-id="46123-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span><span class="sxs-lookup"><span data-stu-id="46123-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Junk Email Reporting\Addins\LoggingLevel</span></span>
    
2. <span data-ttu-id="46123-130">Redémarrez Microsoft Office Outlook et demandez aux utilisateurs de vous avertir dès qu'ils reçoivent le message d'erreur.</span><span class="sxs-lookup"><span data-stu-id="46123-130">Restart Microsoft Office Outlook and ask users to report back when they see the error message.</span></span>
    
3. <span data-ttu-id="46123-131">Collectez les informations de journal se trouvant à l'emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="46123-131">Collect the log information found at the following location:</span></span> 
    
    <span data-ttu-id="46123-132">%LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt</span><span class="sxs-lookup"><span data-stu-id="46123-132">%LOCALAPPDATA%\Microsoft\Junk Email Reporting Add-in\SpamReporterAddinLog.txt</span></span>
    
4. <span data-ttu-id="46123-133">Contactez les techniciens du support Exchange Online Protection et fournissez-leur les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="46123-133">Contact Exchange Online Protection Technical Support and provide them with the log information.</span></span> 
    
 <span data-ttu-id="46123-134">**Problème :** les utilisateurs décident de ne pas recevoir de confirmation quand ils signalent un message électronique comme courrier indésirable, mais ils souhaitent maintenant réactiver cette option.</span><span class="sxs-lookup"><span data-stu-id="46123-134">**Problem:** Users choose not to receive a confirmation when they submit an email as junk and now they want the option back.</span></span> 
  
### <a name="troubleshooting-tip"></a><span data-ttu-id="46123-135">Conseil de dépannage</span><span class="sxs-lookup"><span data-stu-id="46123-135">Troubleshooting tip</span></span>

1. <span data-ttu-id="46123-136">Définissez la valeur de la clé de Registre suivante sur « True » : HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences\ConfirmReportJunk</span><span class="sxs-lookup"><span data-stu-id="46123-136">Set the following registry key value to "True": HKEY_CURRENT_USER\Software\Microsoft\Junk E-mail Reporting\Preferences\ConfirmReportJunk</span></span>
    
2. <span data-ttu-id="46123-137">Redémarrez Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="46123-137">Restart Microsoft Office Outlook.</span></span>
    
## <a name="support-information"></a><span data-ttu-id="46123-138">Informations concernant le support</span><span class="sxs-lookup"><span data-stu-id="46123-138">Support Information</span></span>

<span data-ttu-id="46123-139">Si vous avez besoin d’aide pour l’installation, la configuration ou la désinstallation du complément, veuillez contacter le support technique à l’aide du lien nouvelle demande de service sur la page support dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="46123-139">If you need help with the installation, configuration, or uninstallation of the add-in, please contact technical support using the new service request link on the support page in the Microsoft 365 admin center.</span></span> <span data-ttu-id="46123-140">Pour obtenir des options supplémentaires, notamment la soumission d’une demande de service via les options de téléphone et d’auto-assistance, consultez [l’aide et le support pour EOP](help-and-support-for-eop.md).</span><span class="sxs-lookup"><span data-stu-id="46123-140">For additional options including submitting a service request via the telephone and self-support options, see [Help and support for EOP](help-and-support-for-eop.md).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="46123-141">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="46123-141">For more information</span></span>

[<span data-ttu-id="46123-142">Activer le complément Signaler le message</span><span class="sxs-lookup"><span data-stu-id="46123-142">Enable the Report Message add-in</span></span>](https://support.office.com/article/4250c4bc-6102-420b-9e0a-a95064837676)
  
[<span data-ttu-id="46123-143">Signaler les messages de courrier indésirable à Microsoft</span><span class="sxs-lookup"><span data-stu-id="46123-143">Report junk email messages to Microsoft</span></span>](report-junk-email-messages-to-microsoft.md)
  

