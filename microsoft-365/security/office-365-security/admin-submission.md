---
title: Soumissions d’administration dans Office 365, O365 envois, Office 365 courrier indésirable, O365 false negative, Submit phishing in Office 365, Submit e-mail for Scanning, suspect email in Office 365, Scan a mail, Microsoft Scan for hameçon, demandez à Microsoft d’analyser les courriers indésirables, envoyer courrier électronique, envoi de messages électroniques, courrier électronique Dodgy, messages d’acteur incorrects, courrier suspect non approuvé
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 08/06/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Découvrez comment envoyer des e-mails suspects, des courriers électroniques de hameçonnage suspects, du courrier indésirable et d’autres messages, URL et fichiers potentiellement dangereux de votre client Office 365 à Microsoft pour analyse.
ms.openlocfilehash: 3d53c8270e84cd6f6298b9b39cc7e37262aed7b0
ms.sourcegitcommit: 9c9044885eb9754ce69f2f08afdcc13c782ce2f9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "39915215"
---
# <a name="how-to-submit-suspected-spam-phish-urls-and-files-to-microsoft-for-office-365-scanning"></a><span data-ttu-id="bbfb4-103">Procédure d’envoi de courrier indésirable, hameçon, URL et fichiers suspects à Microsoft pour l’analyse Office 365</span><span class="sxs-lookup"><span data-stu-id="bbfb4-103">How to submit suspected spam, phish, URLs, and files to Microsoft for Office 365 scanning</span></span>

<span data-ttu-id="bbfb4-104">Les administrateurs peuvent envoyer des courriers électroniques à l’aide de l’ID de message réseau, des URL et des fichiers pour l’analyse par Microsoft dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-104">Admins can send emails by using file or network message ID, URLs, and files for scanning by Microsoft in Office 365.</span></span> <span data-ttu-id="bbfb4-105">La section soumissions mises à jour inclut toujours les messages signalés par l’utilisateur et disponibles pour tous les clients utilisant EOP.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-105">The updated submissions section still includes user reported messages and available to all customers using EOP.</span></span>

<span data-ttu-id="bbfb4-106">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-106">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="bbfb4-107">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client telles que les règles ETR.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-107">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as ETR rules.</span></span> 

## <a name="how-to-direct-suspicious-content-to-microsoft-for-office-365-scanning"></a><span data-ttu-id="bbfb4-108">Comment faire pour diriger du contenu suspect vers Microsoft pour Office 365, analyse</span><span class="sxs-lookup"><span data-stu-id="bbfb4-108">How to direct suspicious content to Microsoft for Office 365 scanning</span></span>

<span data-ttu-id="bbfb4-109">Pour envoyer du contenu à Microsoft, cliquez sur le bouton **nouvelle soumission** dans la partie supérieure gauche de la page soumissions.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-109">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="bbfb4-110">Un menu volant sur le côté droit de la page apparaît avec la possibilité d’envoyer un message électronique, une URL ou un fichier.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-110">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span> 

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="bbfb4-111">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="bbfb4-111">Submit a questionable email to Microsoft</span></span>
![Exemple de dépôt de courrier électronique](../media/submission-flyout-email.PNG)
1. <span data-ttu-id="bbfb4-113">Pour envoyer un message électronique, sélectionnez **courrier électronique** et spécifiez l' **ID de message réseau** de messagerie ou téléchargez le fichier de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-113">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span> 

2. <span data-ttu-id="bbfb4-114">Spécifiez le ou les destinataires sur lesquels vous souhaitez exécuter la vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-114">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="bbfb4-115">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de niveau utilisateur ou client.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-115">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span> 

3. <span data-ttu-id="bbfb4-116">Indiquez si l’e-mail doit avoir été bloqué ou non.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-116">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="bbfb4-117">Si la messagerie doit avoir été bloquée, indiquez si elle doit être bloquée en tant que courrier indésirable, hameçonnage ou programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-117">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="bbfb4-118">Si vous n’êtes pas certain de son type, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-118">If you are not sure what type it might be, use your best judgement.</span></span>  

* <span data-ttu-id="bbfb4-119">Si le filtre a été contourné en raison de stratégies lors de l’envoi, vous verrez des informations sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-119">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

* <span data-ttu-id="bbfb4-120">Si le filtre n’a pas été contourné en raison d’une ou de plusieurs stratégies, l’analyse se terminera en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-120">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="bbfb4-121">Vous verrez des informations supplémentaires sur l’envoi en cliquant sur le lien État.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-121">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="bbfb4-122">Cela inclut les résultats de la vérification de stratégie et le verdict de nouvelle analyse.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-122">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="bbfb4-123">Remarque cela n’exécute pas de nouveau le courrier électronique via la pile de filtrage complet DAV d’Office 365 mais exécute une nouvelle analyse partielle en fonction de certains attributs de l’e-mail, de l’URL ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-123">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span> 

4. <span data-ttu-id="bbfb4-124">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="bbfb4-124">Click the **Submit** button.</span></span>

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="bbfb4-125">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="bbfb4-125">Send a suspect URL to Microsoft</span></span>
![Exemple de dépôt de courrier électronique](../media/submission-url-flyout.png)
1. <span data-ttu-id="bbfb4-127">Pour soumettre une URL, sélectionnez **URL** dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-127">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="bbfb4-128">Tapez l’URL complète, y compris le protocole (**https://**).</span><span class="sxs-lookup"><span data-stu-id="bbfb4-128">Type in the full URL including the protocol (**https://**).</span></span> 

* <span data-ttu-id="bbfb4-129">Si vous avez sélectionné **doit avoir été filtré**, spécifiez si l’URL est un hameçonnage ou un programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-129">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="bbfb4-130">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="bbfb4-130">Click the **Submit** button.</span></span> 


### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="bbfb4-131">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="bbfb4-131">Submit a suspected file to Microsoft</span></span>
![Exemple de dépôt de courrier électronique](../media/submission-file-flyout.PNG)
1. <span data-ttu-id="bbfb4-133">Pour soumettre un fichier, sélectionnez **fichier** dans le menu volant et téléchargez le fichier que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="bbfb4-133">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span> 

2. <span data-ttu-id="bbfb4-134">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="bbfb4-134">Click the **Submit** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="bbfb4-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="bbfb4-135">Related topics</span></span>

[<span data-ttu-id="bbfb4-136">Plan 2 de protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="bbfb4-136">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="bbfb4-137">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="bbfb4-137">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="bbfb4-138">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="bbfb4-138">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

