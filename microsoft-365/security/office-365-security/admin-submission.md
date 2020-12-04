---
title: Soumissions de l’administrateur
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le portail d’envoi du centre de sécurité & conformité pour envoyer des e-mails suspects, des courriers électroniques de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement nuisibles, des URL et des fichiers à Microsoft à des fins d’analyse.
ms.openlocfilehash: 0c01afff2e9e5a656099192f3867bb3a6f1cee23
ms.sourcegitcommit: 7e003ee0a06f61bfb9f80441c3479fa3148afafe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/03/2020
ms.locfileid: "49568589"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="2cf32-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="2cf32-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, les administrateurs peuvent utiliser le portail d’envoi du centre de sécurité & conformité pour soumettre des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="2cf32-104">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="2cf32-105">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="2cf32-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="2cf32-106">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client, telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="2cf32-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="2cf32-107">Pour d’autres façons d’envoyer des messages électroniques, des URL et des pièces jointes à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="2cf32-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="2cf32-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2cf32-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="2cf32-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="2cf32-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="2cf32-110">Pour accéder directement à la page d' **envoi** , utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="2cf32-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="2cf32-111">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="2cf32-111">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="2cf32-112">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2cf32-112">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  - <span data-ttu-id="2cf32-113">**Gestion** de l’organisation dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="2cf32-113">**Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="2cf32-114">Notez que l’appartenance à ce groupe de rôles est requise pour [afficher les soumissions de l’utilisateur à la boîte aux lettres personnalisée](#view-user-submissions-to-the-custom-mailbox) , comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2cf32-114">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this topic.</span></span>

- <span data-ttu-id="2cf32-115">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="2cf32-115">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="2cf32-116">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-116">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="2cf32-117">Dans le centre de sécurité & conformité, accédez à envois de **gestion des menaces** \> **Submissions**, vérifiez que vous êtes sous l’onglet **soumissions administrateur** , puis cliquez sur **nouvelle soumission**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-117">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

2. <span data-ttu-id="2cf32-118">Utilisez le menu volant **nouvelle soumission** qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2cf32-118">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="2cf32-119">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-119">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="2cf32-120">Dans la section **type d’objet** , sélectionnez **courrier électronique**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-120">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="2cf32-121">Dans la section **format de soumission** , utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-121">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="2cf32-122">**ID de message réseau**: il s’agit d’une valeur GUID qui est disponible dans l’en-tête **x-MS-Exchange-Organization-Network-message-ID** dans le message ou dans l’en-tête **x-MS-Office 365-Filtering-correlation-ID** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="2cf32-122">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message, or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>

   - <span data-ttu-id="2cf32-123">**Fichier**: cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-123">**File**: Click **Choose file**.</span></span> <span data-ttu-id="2cf32-124">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier. eml ou. MSG, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-124">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2cf32-125">Les administrateurs disposant de Defender pour Office 365 plan 1 ou plan 2 peuvent envoyer des messages datant de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="2cf32-125">Admins with Defender for Office 365 Plan 1 or Plan 2 are able to submit messages as old as 30 days.</span></span> <span data-ttu-id="2cf32-126">Les autres administrateurs ne pourront revenir qu’à plus de 7 jours.</span><span class="sxs-lookup"><span data-stu-id="2cf32-126">Other admins will only be able to go back 7 days.</span></span>

2. <span data-ttu-id="2cf32-127">Dans la section **destinataires** , spécifiez un ou plusieurs destinataires sur lesquels vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="2cf32-127">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="2cf32-128">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de l’utilisateur ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2cf32-128">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="2cf32-129">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-129">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="2cf32-130">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="2cf32-130">**Should not have been blocked**</span></span>

   - <span data-ttu-id="2cf32-131">**Doit avoir été bloqué**: sélectionnez **courrier indésirable**, **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-131">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="2cf32-132">Si vous n’êtes pas sûr, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="2cf32-132">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="2cf32-133">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-133">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="2cf32-135">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-135">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="2cf32-136">Dans la section **type d’objet** , sélectionnez **URL**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-136">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="2cf32-137">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="2cf32-137">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="2cf32-138">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-138">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="2cf32-139">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="2cf32-139">**Should not have been blocked**</span></span>

   - <span data-ttu-id="2cf32-140">**Doit avoir été bloqué**: sélectionnez **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-140">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="2cf32-141">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-141">When you're finished, click the **Submit** button.</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="2cf32-143">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-143">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="2cf32-144">Dans la section **type d’objet** , sélectionnez **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-144">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="2cf32-145">Cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-145">Click **Choose File**.</span></span> <span data-ttu-id="2cf32-146">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-146">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="2cf32-147">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-147">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="2cf32-148">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="2cf32-148">**Should not have been blocked**</span></span>

   - <span data-ttu-id="2cf32-149">**Doit avoir été bloqué**: le **programme malveillant** est le seul choix et est automatiquement sélectionné..</span><span class="sxs-lookup"><span data-stu-id="2cf32-149">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="2cf32-150">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-150">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission de pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="2cf32-152">Afficher les soumissions de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="2cf32-152">View admin submissions</span></span>

<span data-ttu-id="2cf32-153">Dans le centre de sécurité & conformité, accédez à envois de **gestion des menaces** \> **Submissions**, vérifiez que vous êtes sous l’onglet **soumissions administrateur** , puis cliquez sur **nouvelle soumission**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-153">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="2cf32-154">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **ID de soumission** (valeur Guid affectée à chaque envoi) en entrant une valeur dans la zone et en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="2cf32-154">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="2cf32-155">Update</span><span class="sxs-lookup"><span data-stu-id="2cf32-155">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="2cf32-156">Pour modifier les critères de filtre, cliquez sur le bouton **ID de soumission** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-156">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="2cf32-157">**Sender**</span><span class="sxs-lookup"><span data-stu-id="2cf32-157">**Sender**</span></span>
- <span data-ttu-id="2cf32-158">**Subject/URL/nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="2cf32-158">**Subject/URL/File name**</span></span>
- <span data-ttu-id="2cf32-159">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="2cf32-159">**Submitted by**</span></span>
- <span data-ttu-id="2cf32-160">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-160">**Submission type**</span></span>
- <span data-ttu-id="2cf32-161">**Status**</span><span class="sxs-lookup"><span data-stu-id="2cf32-161">**Status**</span></span>

![Options de filtrage pour les soumissions d’administration](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="2cf32-163">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-163">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="2cf32-164">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="2cf32-164">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="2cf32-165">Sous le graphique, il existe trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-165">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="2cf32-166">Afficher les envois de courrier de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="2cf32-166">View admin email submissions</span></span>

<span data-ttu-id="2cf32-167">Cliquez sur l’onglet **e-mail** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-167">Click the **Email** tab.</span></span>

<span data-ttu-id="2cf32-168">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="2cf32-168">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="2cf32-169">**Date**</span><span class="sxs-lookup"><span data-stu-id="2cf32-169">**Date**</span></span>
- <span data-ttu-id="2cf32-170">**ID de soumission**: valeur Guid assignée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="2cf32-170">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="2cf32-171">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-171">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-172">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-172">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-173">**Sender**</span><span class="sxs-lookup"><span data-stu-id="2cf32-173">**Sender**</span></span>
- <span data-ttu-id="2cf32-174">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-174">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-175">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-175">**Submission type**</span></span>
- <span data-ttu-id="2cf32-176">**Motif de remise**</span><span class="sxs-lookup"><span data-stu-id="2cf32-176">**Delivery reason**</span></span>
- <span data-ttu-id="2cf32-177">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-177">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="2cf32-178"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-178"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

#### <a name="admin-submission-rescan-details"></a><span data-ttu-id="2cf32-179">Détails de la nouvelle analyse de l’envoi administrateur</span><span class="sxs-lookup"><span data-stu-id="2cf32-179">Admin submission rescan details</span></span>

<span data-ttu-id="2cf32-180">Les messages envoyés dans les soumissions de l’administrateur sont de nouveau analysés et les résultats sont affichés dans la fenêtre d’affichage des détails :</span><span class="sxs-lookup"><span data-stu-id="2cf32-180">Messages that are submitted in admin submissions are rescanned and results shown in the details flyout:</span></span>

- <span data-ttu-id="2cf32-181">En cas de défaillance de l’authentification de l’expéditeur au moment de la remise.</span><span class="sxs-lookup"><span data-stu-id="2cf32-181">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="2cf32-182">Informations sur les accès à une stratégie qui auraient pu affecter ou remplacer le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="2cf32-182">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="2cf32-183">Les résultats de la détonation actuelle permettent de déterminer si les URL ou les fichiers contenus dans le message étaient malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="2cf32-183">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="2cf32-184">Commentaires des classeurs.</span><span class="sxs-lookup"><span data-stu-id="2cf32-184">Feedback from graders.</span></span>

<span data-ttu-id="2cf32-185">Si un remplacement a été trouvé, la nouvelle analyse doit se terminer en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="2cf32-185">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="2cf32-186">S’il n’y a pas eu de problème dans l’authentification de messagerie ou si la remise n’a pas été affectée par un remplacement, les commentaires des classeurs peuvent prendre jusqu’à une journée.</span><span class="sxs-lookup"><span data-stu-id="2cf32-186">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="2cf32-187">Afficher les envois d’URL d’administrateur</span><span class="sxs-lookup"><span data-stu-id="2cf32-187">View admin URL submissions</span></span>

<span data-ttu-id="2cf32-188">Cliquez sur l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-188">Click the **URL** tab.</span></span>

<span data-ttu-id="2cf32-189">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="2cf32-189">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="2cf32-190">**Date**</span><span class="sxs-lookup"><span data-stu-id="2cf32-190">**Date**</span></span>
- <span data-ttu-id="2cf32-191">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="2cf32-191">**Submission ID**</span></span>
- <span data-ttu-id="2cf32-192">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-192">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-193">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-193">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-194">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-194">**Submission type**</span></span>
- <span data-ttu-id="2cf32-195">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-195">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="2cf32-196"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-196"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="2cf32-197">Afficher les envois de pièces jointes admin</span><span class="sxs-lookup"><span data-stu-id="2cf32-197">View admin attachment submissions</span></span>

<span data-ttu-id="2cf32-198">Cliquez sur l’onglet **pièces jointes** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-198">Click the **Attachments** tab.</span></span>

<span data-ttu-id="2cf32-199">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="2cf32-199">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="2cf32-200">**Date**</span><span class="sxs-lookup"><span data-stu-id="2cf32-200">**Date**</span></span>
- <span data-ttu-id="2cf32-201">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="2cf32-201">**Submission ID**</span></span>
- <span data-ttu-id="2cf32-202">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-202">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-203">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-203">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-204">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-204">**Submission type**</span></span>
- <span data-ttu-id="2cf32-205">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-205">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="2cf32-206"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-206"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="2cf32-207">Afficher les soumissions des utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="2cf32-207">View user submissions to Microsoft</span></span>

<span data-ttu-id="2cf32-208">Si vous avez déployé le [complément de rapport de message](enable-the-report-message-add-in.md)ou que les utilisateurs utilisent la [création de rapports intégrée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), vous pouvez voir ce que les utilisateurs signalent sous l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-208">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="2cf32-209">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **envois** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2cf32-209">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="2cf32-210">Sélectionnez l’onglet **soumissions utilisateur** , puis cliquez sur **nouvelle soumission**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-210">Select the **User submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="2cf32-211">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="2cf32-211">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="2cf32-212">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="2cf32-212">**Submitted on**</span></span>
- <span data-ttu-id="2cf32-213">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-213">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-214">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-214">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-215">**Sender**</span><span class="sxs-lookup"><span data-stu-id="2cf32-215">**Sender**</span></span>
- <span data-ttu-id="2cf32-216">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-216">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-217">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-217">**Submission type**</span></span>

<span data-ttu-id="2cf32-218"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-218"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="2cf32-219">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **expéditeur** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="2cf32-219">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="2cf32-220">Update</span><span class="sxs-lookup"><span data-stu-id="2cf32-220">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="2cf32-221">Pour modifier les critères de filtre, cliquez sur le bouton **expéditeur** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-221">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="2cf32-222">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="2cf32-222">**Sender domain**</span></span>
- <span data-ttu-id="2cf32-223">**Subject**</span><span class="sxs-lookup"><span data-stu-id="2cf32-223">**Subject**</span></span>
- <span data-ttu-id="2cf32-224">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="2cf32-224">**Submitted by**</span></span>
- <span data-ttu-id="2cf32-225">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-225">**Submission type**</span></span>
- <span data-ttu-id="2cf32-226">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="2cf32-226">**Sender IP**</span></span>

![Options de filtrage pour les soumissions des utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="2cf32-228">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-228">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="2cf32-229">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="2cf32-229">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="2cf32-230">Afficher les soumissions des utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="2cf32-230">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="2cf32-231">**Si** vous avez [configuré une boîte aux lettres personnalisée](user-submission.md) pour recevoir des messages signalés par l’utilisateur, vous pouvez afficher et envoyer également les messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="2cf32-231">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="2cf32-232">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **envois** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2cf32-232">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="2cf32-233">Sélectionnez l’onglet **boîte aux lettres personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="2cf32-233">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="2cf32-234">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="2cf32-234">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="2cf32-235">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="2cf32-235">**Submitted on**</span></span>
- <span data-ttu-id="2cf32-236">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-236">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-237">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-237">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-238">**Sender**</span><span class="sxs-lookup"><span data-stu-id="2cf32-238">**Sender**</span></span>
- <span data-ttu-id="2cf32-239">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="2cf32-239">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="2cf32-240">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="2cf32-240">**Submission type**</span></span>

<span data-ttu-id="2cf32-241">En haut de la page, vous pouvez entrer une date de début, une date de fin et un filtre par **envoyé par** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="2cf32-241">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="2cf32-242">Update</span><span class="sxs-lookup"><span data-stu-id="2cf32-242">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="2cf32-243">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="2cf32-243">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="2cf32-244">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="2cf32-244">In the dialog that appears, save the .csv file.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="2cf32-245">Annuler les soumissions de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2cf32-245">Undo user submissions</span></span>

<span data-ttu-id="2cf32-246">Une fois qu’un utilisateur envoie un e-mail suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler l’envoi.</span><span class="sxs-lookup"><span data-stu-id="2cf32-246">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="2cf32-247">Si l’utilisateur souhaite récupérer le courrier, il sera disponible pour la récupération dans les dossiers éléments supprimés ou courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="2cf32-247">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="2cf32-248">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="2cf32-248">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="2cf32-249">Si vous avez configuré la boîte aux lettres personnalisée de sorte qu’elle intercepte les messages signalés par l’utilisateur sans envoyer les messages à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="2cf32-249">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="2cf32-250">Cela déplace effectivement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2cf32-250">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="2cf32-251">Sous l’onglet **boîte aux lettres personnalisée** , sélectionnez un message dans la liste, cliquez sur le bouton d' **action** , puis effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cf32-251">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="2cf32-252">**État de la notification**</span><span class="sxs-lookup"><span data-stu-id="2cf32-252">**Report clean**</span></span>
- <span data-ttu-id="2cf32-253">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="2cf32-253">**Report phishing**</span></span>
- <span data-ttu-id="2cf32-254">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="2cf32-254">**Report malware**</span></span>
- <span data-ttu-id="2cf32-255">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="2cf32-255">**Report spam**</span></span>

![Options du bouton d’action](../../media/user-submission-custom-mailbox-action-button.png)
