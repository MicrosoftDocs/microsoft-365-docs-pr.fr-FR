---
title: Soumissions de l’administrateur, soumission, problème de courrier indésirable faux négatif, soumettre un courrier indésirable, envoyer un message électronique pour analyse, courrier suspect dans Office 365, analyser un courrier électronique, demander à Microsoft d’analyser les messages hameçons, vérifier le courrier indésirable, envoyer des messages électroniques, envoyer des courriers électroniques à Microsoft, signaler des messages frauduleux à Microsoft, signaler des courriers électroniques à Microsoft, signaler des messages frauduleux à Microsoft , signaler un programme malveillant à Microsoft, courrier indésirable dans la boîte aux lettres, virus dans le courrier électronique
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Découvrez comment envoyer des e-mails suspects, des courriers électroniques de hameçonnage suspects, du courrier indésirable, ainsi que d’autres messages, URL et fichiers potentiellement dangereux de votre entreprise à Microsoft pour analyse.
ms.openlocfilehash: 2d86555854f9babd202764f1bad8b548daf52c70
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631380"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="3ccd6-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3ccd6-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

<span data-ttu-id="3ccd6-104">Si vous êtes administrateur dans une organisation Microsoft 365 avec des boîtes aux lettres dans Exchange Online, vous pouvez utiliser le portail d’envoi du centre de sécurité & conformité pour soumettre des messages électroniques, des URL et des pièces jointes à Microsoft à des fins d’analyse.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-104">If you're an admin in a Microsoft 365 organization with mailboxes in Exchange Online, you can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="3ccd6-105">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="3ccd6-106">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client, telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="3ccd6-107">Pour d’autres façons d’envoyer des messages électroniques, des URL et des pièces jointes à Microsoft, consultez la rubrique</span><span class="sxs-lookup"><span data-stu-id="3ccd6-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see</span></span> 

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="3ccd6-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3ccd6-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="3ccd6-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="3ccd6-110">Pour accéder directement à la page d' **envoi** , <https://protection.office.com/reportsubmission>utilisez.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="3ccd6-111">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="3ccd6-112">Pour vous connecter à un service Exchange Online Protection autonome, voir [Se connecter à PowerShell d’Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-112">To connect to standalone Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="3ccd6-113">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-113">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="3ccd6-114">Pour ajouter, modifier et supprimer des stratégies de blocage du courrier indésirable, vous devez être membre des groupes de rôles gestion de l' **organisation**, administrateur de la **sécurité**ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="3ccd6-114">To add, modify, and delete anti-spam policies, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Reader** role groups.</span></span> <span data-ttu-id="3ccd6-115">Pour plus d’informations sur les groupes de rôles dans le centre de sécurité & conformité, consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-115">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="3ccd6-116">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-116">For more information about how users can submit messages and files to Microsoft see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="how-to-direct-suspicious-content-to-microsoft-scanning"></a><span data-ttu-id="3ccd6-117">Comment diriger le contenu suspect vers l’analyse Microsoft</span><span class="sxs-lookup"><span data-stu-id="3ccd6-117">How to direct suspicious content to Microsoft scanning</span></span>

<span data-ttu-id="3ccd6-118">Pour envoyer du contenu à Microsoft, cliquez sur le bouton **nouvelle soumission** dans la partie supérieure gauche de la page soumissions.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-118">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="3ccd6-119">Un menu volant sur le côté droit de la page apparaît avec la possibilité d’envoyer un message électronique, une URL ou un fichier.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-119">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="3ccd6-120">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3ccd6-120">Submit a questionable email to Microsoft</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-flyout-email.PNG)

1. <span data-ttu-id="3ccd6-122">Pour envoyer un message électronique, sélectionnez **courrier électronique** et spécifiez l' **ID de message réseau** de messagerie ou téléchargez le fichier de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-122">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span>

2. <span data-ttu-id="3ccd6-123">Spécifiez le ou les destinataires sur lesquels vous souhaitez exécuter la vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-123">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="3ccd6-124">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de niveau utilisateur ou client.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-124">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span>

3. <span data-ttu-id="3ccd6-125">Indiquez si l’e-mail doit avoir été bloqué ou non.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-125">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="3ccd6-126">Si la messagerie doit avoir été bloquée, indiquez si elle doit être bloquée en tant que courrier indésirable, hameçonnage ou programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-126">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="3ccd6-127">Si vous n’êtes pas sûr de son type, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-127">If you are not sure what type it might be, use your best judgment.</span></span>

   - <span data-ttu-id="3ccd6-128">Si le filtre a été contourné en raison de stratégies lors de l’envoi, vous verrez des informations sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-128">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

   - <span data-ttu-id="3ccd6-129">Si le filtre n’a pas été contourné en raison d’une ou de plusieurs stratégies, l’analyse se terminera en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-129">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="3ccd6-130">Vous verrez des informations supplémentaires sur l’envoi en cliquant sur le lien État.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-130">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="3ccd6-131">Cela inclut les résultats de la vérification de stratégie et le verdict de nouvelle analyse.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-131">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="3ccd6-132">Remarque cela n’exécute pas de nouveau le courrier électronique via la pile de filtrage complet DAV d’Office 365 mais exécute une nouvelle analyse partielle en fonction de certains attributs de l’e-mail, de l’URL ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-132">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span>

4. <span data-ttu-id="3ccd6-133">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="3ccd6-133">Click the **Submit** button.</span></span>

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="3ccd6-134">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3ccd6-134">Send a suspect URL to Microsoft</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-url-flyout.png)

1. <span data-ttu-id="3ccd6-136">Pour soumettre une URL, sélectionnez **URL** dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-136">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="3ccd6-137">Tapez l’URL complète, y compris le protocole (**https://**).</span><span class="sxs-lookup"><span data-stu-id="3ccd6-137">Type in the full URL including the protocol (**https://**).</span></span>

   <span data-ttu-id="3ccd6-138">Si vous avez sélectionné **doit avoir été filtré**, spécifiez si l’URL est un hameçonnage ou un programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-138">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="3ccd6-139">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="3ccd6-139">Click the **Submit** button.</span></span>

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="3ccd6-140">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3ccd6-140">Submit a suspected file to Microsoft</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-file-flyout.PNG)

1. <span data-ttu-id="3ccd6-142">Pour soumettre un fichier, sélectionnez **fichier** dans le menu volant et téléchargez le fichier que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="3ccd6-142">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span>

2. <span data-ttu-id="3ccd6-143">Cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="3ccd6-143">Click the **Submit** button.</span></span>
