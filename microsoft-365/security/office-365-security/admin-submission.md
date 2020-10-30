---
title: Soumissions de l’administrateur
f1.keywords:
- NOCSH
ms.author: chrisda
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
ms.openlocfilehash: 5d4123acaf3c9891f9aeb8028173f3071c260935
ms.sourcegitcommit: 04a43a146cb62a10b1a4555ec3bed49eb08fbb99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "48806759"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="f9bfb-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="f9bfb-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, les administrateurs peuvent utiliser le portail d’envoi du centre de sécurité & conformité pour soumettre des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-104">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="f9bfb-105">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="f9bfb-106">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client, telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="f9bfb-107">Pour d’autres façons d’envoyer des messages électroniques, des URL et des pièces jointes à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f9bfb-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f9bfb-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="f9bfb-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="f9bfb-110">Pour accéder directement à la page d' **envoi** , utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="f9bfb-111">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-111">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="f9bfb-112">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-112">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  - <span data-ttu-id="f9bfb-113">**Gestion** de l’organisation dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-113">**Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="f9bfb-114">Notez que l’appartenance à ce groupe de rôles est requise pour [afficher les soumissions de l’utilisateur à la boîte aux lettres personnalisée](#view-user-submissions-to-the-custom-mailbox) , comme décrit plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-114">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this topic.</span></span>

- <span data-ttu-id="f9bfb-115">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-115">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="f9bfb-116">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-116">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="f9bfb-117">Dans le centre de sécurité & conformité, accédez à envois de **gestion des menaces** \> **Submissions** , vérifiez que vous êtes sous l’onglet **soumissions administrateur** , puis cliquez sur **nouvelle soumission** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-117">In the Security & Compliance Center, go to **Threat management** \> **Submissions** , verify that you're on the **Admin submissions** tab, and then click **New submission** .</span></span>

2. <span data-ttu-id="f9bfb-118">Utilisez le menu volant **nouvelle soumission** qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-118">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="f9bfb-119">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-119">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="f9bfb-120">Dans la section **type d’objet** , sélectionnez **courrier électronique** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-120">In the **Object type** section, select **Email** .</span></span> <span data-ttu-id="f9bfb-121">Dans la section **format de soumission** , utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-121">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="f9bfb-122">**ID de message réseau** : il s’agit d’une valeur GUID qui est disponible dans l’en-tête **X-MS-Exchange-Organization-Network-message-ID** du message.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-122">**Network Message ID** : This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message.</span></span>

   - <span data-ttu-id="f9bfb-123">**Fichier** : cliquez sur **choisir un fichier** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-123">**File** : Click **Choose file** .</span></span> <span data-ttu-id="f9bfb-124">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier. eml ou. MSG, puis cliquez sur **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-124">In the dialog that opens, find and select the .eml or .msg file, and then click **Open** .</span></span>

2. <span data-ttu-id="f9bfb-125">Dans la section **destinataires** , spécifiez un ou plusieurs destinataires sur lesquels vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-125">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="f9bfb-126">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de l’utilisateur ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-126">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="f9bfb-127">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-127">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="f9bfb-128">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-128">**Should not have been blocked**</span></span>

   - <span data-ttu-id="f9bfb-129">**Doit avoir été bloqué** : sélectionnez **courrier indésirable** , **hameçonnage** ou **programme malveillant** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-129">**Should have been blocked** : Select **Spam** , **Phishing** , or **Malware** .</span></span> <span data-ttu-id="f9bfb-130">Si vous n’êtes pas sûr, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-130">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="f9bfb-131">Si le filtre a été contourné en raison de stratégies lors de l’envoi, vous verrez des informations sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-131">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

   <span data-ttu-id="f9bfb-132">Si le filtre n’a pas été contourné en raison d’une ou de plusieurs stratégies, l’analyse se terminera en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-132">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="f9bfb-133">Vous verrez des informations supplémentaires sur l’envoi en cliquant sur le lien État.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-133">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="f9bfb-134">Cela inclut les résultats de la vérification de stratégie et le verdict de nouvelle analyse.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-134">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="f9bfb-135">Remarque cela n’exécute pas de nouveau le courrier électronique via la pile de filtrage complet DAV d’Office 365 mais exécute une nouvelle analyse partielle en fonction de certains attributs de l’e-mail, de l’URL ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-135">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span>

5. <span data-ttu-id="f9bfb-136">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-136">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="f9bfb-138">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-138">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="f9bfb-139">Dans la section **type d’objet** , sélectionnez **URL** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-139">In the **Object type** section, select **URL** .</span></span> <span data-ttu-id="f9bfb-140">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="f9bfb-140">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="f9bfb-141">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-141">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="f9bfb-142">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-142">**Should not have been blocked**</span></span>

   - <span data-ttu-id="f9bfb-143">**Doit avoir été bloqué** : sélectionnez **hameçonnage** ou **programme malveillant** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-143">**Should have been blocked** : Select **Phishing** or **Malware** .</span></span>

3. <span data-ttu-id="f9bfb-144">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-144">When you're finished, click the **Submit** button.</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="f9bfb-146">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-146">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="f9bfb-147">Dans la section **type d’objet** , sélectionnez **pièce jointe** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-147">In the **Object type** section, select **Attachment** .</span></span>

2. <span data-ttu-id="f9bfb-148">Cliquez sur **choisir un fichier** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-148">Click **Choose File** .</span></span> <span data-ttu-id="f9bfb-149">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **ouvrir** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-149">In the dialog that opens, find and select the file, and then click **Open** .</span></span>

3. <span data-ttu-id="f9bfb-150">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-150">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="f9bfb-151">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-151">**Should not have been blocked**</span></span>

   - <span data-ttu-id="f9bfb-152">**Doit avoir été bloqué** : le **programme malveillant** est le seul choix et est automatiquement sélectionné..</span><span class="sxs-lookup"><span data-stu-id="f9bfb-152">**Should have been blocked** : **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="f9bfb-153">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-153">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission de pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="f9bfb-155">Afficher les soumissions de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="f9bfb-155">View admin submissions</span></span>

<span data-ttu-id="f9bfb-156">Dans le centre de sécurité & conformité, accédez à envois de **gestion des menaces** \> **Submissions** , vérifiez que vous êtes sous l’onglet **soumissions administrateur** , puis cliquez sur **nouvelle soumission** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-156">In the Security & Compliance Center, go to **Threat management** \> **Submissions** , verify that you're on the **Admin submissions** tab, and then click **New submission** .</span></span>

<span data-ttu-id="f9bfb-157">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **ID de soumission** (valeur Guid affectée à chaque envoi) en entrant une valeur dans la zone et en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-157">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="f9bfb-158">Update</span><span class="sxs-lookup"><span data-stu-id="f9bfb-158">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="f9bfb-159">Pour modifier les critères de filtre, cliquez sur le bouton **ID de soumission** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-159">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="f9bfb-160">**Sender**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-160">**Sender**</span></span>
- <span data-ttu-id="f9bfb-161">**Subject/URL/nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-161">**Subject/URL/File name**</span></span>
- <span data-ttu-id="f9bfb-162">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-162">**Submitted by**</span></span>
- <span data-ttu-id="f9bfb-163">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-163">**Submission type**</span></span>
- <span data-ttu-id="f9bfb-164">**Status**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-164">**Status**</span></span>

![Options de filtrage pour les soumissions d’administration](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="f9bfb-166">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-166">To export the results, click **Export** near the top of the page and select **Chart data** or **Table** .</span></span> <span data-ttu-id="f9bfb-167">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-167">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="f9bfb-168">Sous le graphique, il existe trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-168">Below the graph, there are three tabs: **Email** (default), **URL** , and **Attachment** .</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="f9bfb-169">Afficher les envois de courrier de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="f9bfb-169">View admin email submissions</span></span>

<span data-ttu-id="f9bfb-170">Cliquez sur l’onglet **e-mail** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-170">Click the **Email** tab.</span></span>

<span data-ttu-id="f9bfb-171">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-171">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="f9bfb-172">**Date**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-172">**Date**</span></span>
- <span data-ttu-id="f9bfb-173">**ID de soumission** : valeur Guid assignée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-173">**Submission ID** : A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="f9bfb-174">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-174">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-175">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-175">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-176">**Sender**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-176">**Sender**</span></span>
- <span data-ttu-id="f9bfb-177">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-177">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-178">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-178">**Submission type**</span></span>
- <span data-ttu-id="f9bfb-179">**Motif de remise**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-179">**Delivery reason**</span></span>
- <span data-ttu-id="f9bfb-180">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-180">**Status**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-181">**Type de contrôle**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-181">**Control type**</span></span>
- <span data-ttu-id="f9bfb-182">**Source du contrôle**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-182">**Control source**</span></span>

  <span data-ttu-id="f9bfb-183"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-183"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="f9bfb-184">Afficher les envois d’URL d’administrateur</span><span class="sxs-lookup"><span data-stu-id="f9bfb-184">View admin URL submissions</span></span>

<span data-ttu-id="f9bfb-185">Cliquez sur l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-185">Click the **URL** tab.</span></span>

<span data-ttu-id="f9bfb-186">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-186">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="f9bfb-187">**Date**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-187">**Date**</span></span>
- <span data-ttu-id="f9bfb-188">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-188">**Submission ID**</span></span>
- <span data-ttu-id="f9bfb-189">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-189">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-190">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-190">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-191">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-191">**Submission type**</span></span>
- <span data-ttu-id="f9bfb-192">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-192">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="f9bfb-193"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-193"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="f9bfb-194">Afficher les envois de pièces jointes admin</span><span class="sxs-lookup"><span data-stu-id="f9bfb-194">View admin attachment submissions</span></span>

<span data-ttu-id="f9bfb-195">Cliquez sur l’onglet **pièces jointes** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-195">Click the **Attachments** tab.</span></span>

<span data-ttu-id="f9bfb-196">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-196">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="f9bfb-197">**Date**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-197">**Date**</span></span>
- <span data-ttu-id="f9bfb-198">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-198">**Submission ID**</span></span>
- <span data-ttu-id="f9bfb-199">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-199">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-200">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-200">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-201">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-201">**Submission type**</span></span>
- <span data-ttu-id="f9bfb-202">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-202">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="f9bfb-203"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-203"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="f9bfb-204">Afficher les soumissions des utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9bfb-204">View user submissions to Microsoft</span></span>

<span data-ttu-id="f9bfb-205">Si vous avez déployé le [complément de rapport de message](enable-the-report-message-add-in.md)ou que les utilisateurs utilisent la [création de rapports intégrée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), vous pouvez voir ce que les utilisateurs signalent sous l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-205">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="f9bfb-206">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **envois** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-206">In the Security & Compliance Center, go to **Threat management** \> **Submissions** .</span></span>

2. <span data-ttu-id="f9bfb-207">Sélectionnez l’onglet **soumissions utilisateur** , puis cliquez sur **nouvelle soumission** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-207">Select the **User submissions** tab, and then click **New submission** .</span></span>

<span data-ttu-id="f9bfb-208">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-208">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="f9bfb-209">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-209">**Submitted on**</span></span>
- <span data-ttu-id="f9bfb-210">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-210">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-211">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-211">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-212">**Sender**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-212">**Sender**</span></span>
- <span data-ttu-id="f9bfb-213">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-213">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-214">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-214">**Submission type**</span></span>

<span data-ttu-id="f9bfb-215"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-215"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="f9bfb-216">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **expéditeur** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-216">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="f9bfb-217">Update</span><span class="sxs-lookup"><span data-stu-id="f9bfb-217">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="f9bfb-218">Pour modifier les critères de filtre, cliquez sur le bouton **expéditeur** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-218">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="f9bfb-219">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-219">**Sender domain**</span></span>
- <span data-ttu-id="f9bfb-220">**Subject**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-220">**Subject**</span></span>
- <span data-ttu-id="f9bfb-221">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-221">**Submitted by**</span></span>
- <span data-ttu-id="f9bfb-222">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-222">**Submission type**</span></span>
- <span data-ttu-id="f9bfb-223">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-223">**Sender IP**</span></span>

![Options de filtrage pour les soumissions des utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="f9bfb-225">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-225">To export the results, click **Export** near the top of the page and select **Chart data** or **Table** .</span></span> <span data-ttu-id="f9bfb-226">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-226">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="f9bfb-227">Afficher les soumissions des utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="f9bfb-227">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="f9bfb-228">**Si** vous avez [configuré une boîte aux lettres personnalisée](user-submission.md) pour recevoir des messages signalés par l’utilisateur, vous pouvez afficher et envoyer également les messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-228">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="f9bfb-229">Dans le centre de sécurité & conformité, accédez **Threat management** à \> **envois** de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-229">In the Security & Compliance Center, go to **Threat management** \> **Submissions** .</span></span>

2. <span data-ttu-id="f9bfb-230">Sélectionnez l’onglet **boîte aux lettres personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-230">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="f9bfb-231">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-231">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="f9bfb-232">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-232">**Submitted on**</span></span>
- <span data-ttu-id="f9bfb-233">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-233">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-234">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-234">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-235">**Sender**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-235">**Sender**</span></span>
- <span data-ttu-id="f9bfb-236">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9bfb-236">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="f9bfb-237">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-237">**Submission type**</span></span>

<span data-ttu-id="f9bfb-238">En haut de la page, vous pouvez entrer une date de début, une date de fin et un filtre par **envoyé par** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-238">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="f9bfb-239">Update</span><span class="sxs-lookup"><span data-stu-id="f9bfb-239">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="f9bfb-240">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau** .</span><span class="sxs-lookup"><span data-stu-id="f9bfb-240">To export the results, click **Export** near the top of the page and select **Chart data** or **Table** .</span></span> <span data-ttu-id="f9bfb-241">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-241">In the dialog that appears, save the .csv file.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="f9bfb-242">Annuler les soumissions de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f9bfb-242">Undo user submissions</span></span>

<span data-ttu-id="f9bfb-243">Une fois qu’un utilisateur envoie un e-mail suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler l’envoi.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-243">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="f9bfb-244">Si l’utilisateur souhaite récupérer le courrier, il sera disponible pour la récupération dans les dossiers éléments supprimés ou courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-244">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span> 

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="f9bfb-245">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="f9bfb-245">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="f9bfb-246">Si vous avez configuré la boîte aux lettres personnalisée de sorte qu’elle intercepte les messages signalés par l’utilisateur sans envoyer les messages à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-246">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="f9bfb-247">Cela déplace effectivement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f9bfb-247">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="f9bfb-248">Sous l’onglet **boîte aux lettres personnalisée** , sélectionnez un message dans la liste, cliquez sur le bouton d' **action** , puis effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bfb-248">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="f9bfb-249">**État de la notification**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-249">**Report clean**</span></span>
- <span data-ttu-id="f9bfb-250">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-250">**Report phishing**</span></span>
- <span data-ttu-id="f9bfb-251">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-251">**Report malware**</span></span>
- <span data-ttu-id="f9bfb-252">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f9bfb-252">**Report spam**</span></span>

![Options du bouton d’action](../../media/user-submission-custom-mailbox-action-button.png)
