---
title: Envois d’administrateur dans Office 365
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
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment envoyer des e-mails suspects, des courriers électroniques de hameçonnage suspects, du courrier indésirable, ainsi que d’autres messages, URL et fichiers potentiellement dangereux de votre entreprise à Microsoft pour analyse.
ms.openlocfilehash: 79f200963655e5fb07a04b686c1dd8cc3bbd0873
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034199"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="38fe1-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

<span data-ttu-id="38fe1-104">Si vous êtes administrateur dans une organisation Microsoft 365 avec des boîtes aux lettres dans Exchange Online, vous pouvez utiliser le portail d’envoi du centre de sécurité & conformité pour soumettre des messages électroniques, des URL et des pièces jointes à Microsoft à des fins d’analyse.</span><span class="sxs-lookup"><span data-stu-id="38fe1-104">If you're an admin in a Microsoft 365 organization with mailboxes in Exchange Online, you can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="38fe1-105">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="38fe1-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="38fe1-106">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client, telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="38fe1-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="38fe1-107">Pour d’autres façons d’envoyer des messages électroniques, des URL et des pièces jointes à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="38fe1-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="38fe1-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="38fe1-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="38fe1-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="38fe1-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="38fe1-110">Pour accéder directement à la page d' **envoi** , <https://protection.office.com/reportsubmission>utilisez.</span><span class="sxs-lookup"><span data-stu-id="38fe1-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="38fe1-111">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="38fe1-111">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="38fe1-112">Pour ajouter, modifier et supprimer des stratégies de blocage du courrier indésirable, vous devez être membre des groupes de rôles gestion de l' **organisation**, administrateur de la **sécurité**ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-112">To add, modify, and delete anti-spam policies, you need to be a member of the **Organization Management**, **Security Administrator**, or **Security Reader** role groups.</span></span> <span data-ttu-id="38fe1-113">Pour des informations supplémentaires sur les groupes de rôles dans le Centre de sécurité et conformité, voir [Autorisations dans le Centre de sécurité et conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="38fe1-113">For more information about role groups in the Security & Compliance Center, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

- <span data-ttu-id="38fe1-114">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="38fe1-114">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="38fe1-115">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-115">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="38fe1-116">Dans le centre de sécurité & conformité, accédez **à gestion** \> des menaces- **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-116">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="38fe1-117">Sur la page des **envois** qui s’affiche, cliquez sur le bouton **nouvelle soumission** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-117">On the **Submissions** page that appears, click the **New submission** button.</span></span>

3. <span data-ttu-id="38fe1-118">Utilisez le menu volant **nouvelle soumission** qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="38fe1-118">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="38fe1-119">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-119">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="38fe1-120">Dans la section **type d’objet** , sélectionnez **courrier électronique**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-120">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="38fe1-121">Dans la section **format de soumission** , utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-121">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="38fe1-122">**ID de message réseau**: il s’agit d’une valeur GUID qui est disponible dans l’en-tête **X-MS-Exchange-Organization-Network-message-ID** du message.</span><span class="sxs-lookup"><span data-stu-id="38fe1-122">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message.</span></span>

   - <span data-ttu-id="38fe1-123">**Fichier**: cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-123">**File**: Click **Choose file**.</span></span> <span data-ttu-id="38fe1-124">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier. eml ou. MSG, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-124">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

2. <span data-ttu-id="38fe1-125">Dans la section **destinataires** , spécifiez un ou plusieurs destinataires sur lesquels vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="38fe1-125">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="38fe1-126">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de l’utilisateur ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="38fe1-126">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="38fe1-127">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-127">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="38fe1-128">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="38fe1-128">**Should not have been blocked**</span></span>

   - <span data-ttu-id="38fe1-129">**Doit avoir été bloqué**: sélectionnez **courrier indésirable**, **hameçonnage**ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-129">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="38fe1-130">Si vous n’êtes pas sûr, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="38fe1-130">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="38fe1-131">Si le filtre a été contourné en raison de stratégies lors de l’envoi, vous verrez des informations sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="38fe1-131">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

   <span data-ttu-id="38fe1-132">Si le filtre n’a pas été contourné en raison d’une ou de plusieurs stratégies, l’analyse se terminera en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="38fe1-132">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="38fe1-133">Vous verrez des informations supplémentaires sur l’envoi en cliquant sur le lien État.</span><span class="sxs-lookup"><span data-stu-id="38fe1-133">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="38fe1-134">Cela inclut les résultats de la vérification de stratégie et le verdict de nouvelle analyse.</span><span class="sxs-lookup"><span data-stu-id="38fe1-134">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="38fe1-135">Remarque cela n’exécute pas de nouveau le courrier électronique via la pile de filtrage complet DAV d’Office 365 mais exécute une nouvelle analyse partielle en fonction de certains attributs de l’e-mail, de l’URL ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="38fe1-135">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span>

5. <span data-ttu-id="38fe1-136">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-136">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="38fe1-138">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-138">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="38fe1-139">Dans la section **type d’objet** , sélectionnez **URL**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-139">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="38fe1-140">Dans la zone qui s’affiche, entrez l’URL complète (par exemple <https://www.fabrikam.com/marketing.html>,).</span><span class="sxs-lookup"><span data-stu-id="38fe1-140">In the box that appears, enter the full URL (for example, <https://www.fabrikam.com/marketing.html>).</span></span>

2. <span data-ttu-id="38fe1-141">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-141">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="38fe1-142">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="38fe1-142">**Should not have been blocked**</span></span>

   - <span data-ttu-id="38fe1-143">**Doit avoir été bloqué**: sélectionnez **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-143">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="38fe1-144">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-144">When you're finished, click the **Submit** button.</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="38fe1-146">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-146">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="38fe1-147">Dans la section **type d’objet** , sélectionnez **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-147">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="38fe1-148">Cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-148">Click **Choose File**.</span></span> <span data-ttu-id="38fe1-149">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-149">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="38fe1-150">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-150">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="38fe1-151">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="38fe1-151">**Should not have been blocked**</span></span>

   - <span data-ttu-id="38fe1-152">**Doit avoir été bloqué**: le **programme malveillant** est le seul choix et est automatiquement sélectionné..</span><span class="sxs-lookup"><span data-stu-id="38fe1-152">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="38fe1-153">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-153">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission de pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="38fe1-155">Afficher les soumissions de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="38fe1-155">View admin submissions</span></span>

1. <span data-ttu-id="38fe1-156">Dans le centre de sécurité & conformité, accédez **à gestion** \> des menaces- **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-156">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="38fe1-157">Sur la page des **envois** qui s’affiche, vérifiez que l’onglet **soumissions** de l’administrateur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="38fe1-157">On the **Submissions** page that appears, verify that the **Admin submissions** tab is selected.</span></span>

<span data-ttu-id="38fe1-158">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **ID de soumission** en entrant une valeur dans la zone, ![puis en](../../media/scc-quarantine-refresh.png)cliquant sur le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="38fe1-158">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="38fe1-159">Update</span><span class="sxs-lookup"><span data-stu-id="38fe1-159">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="38fe1-160">Pour modifier les critères de filtre, cliquez sur le bouton **ID de soumission** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-160">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="38fe1-161">**Sender**</span><span class="sxs-lookup"><span data-stu-id="38fe1-161">**Sender**</span></span>
- <span data-ttu-id="38fe1-162">**Subject/URL/nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="38fe1-162">**Subject/URL/File name**</span></span>
- <span data-ttu-id="38fe1-163">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="38fe1-163">**Submitted by**</span></span>
- <span data-ttu-id="38fe1-164">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-164">**Submission type**</span></span>
- <span data-ttu-id="38fe1-165">**État**</span><span class="sxs-lookup"><span data-stu-id="38fe1-165">**Status**</span></span>

![Options de filtrage pour les soumissions d’administration](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="38fe1-167">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-167">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="38fe1-168">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="38fe1-168">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="38fe1-169">Sous le graphique, il existe trois onglets : **e-mail** (par défaut), **URL**et **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-169">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="38fe1-170">Afficher les envois de courrier de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="38fe1-170">View admin email submissions</span></span>

<span data-ttu-id="38fe1-171">Cliquez sur l’onglet **e-mail** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-171">Click the **Email** tab.</span></span>

<span data-ttu-id="38fe1-172">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="38fe1-172">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="38fe1-173">**Date**</span><span class="sxs-lookup"><span data-stu-id="38fe1-173">**Date**</span></span>
- <span data-ttu-id="38fe1-174">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="38fe1-174">**Submission ID**</span></span>
- <span data-ttu-id="38fe1-175">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-175">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-176">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-176">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-177">**Sender**</span><span class="sxs-lookup"><span data-stu-id="38fe1-177">**Sender**</span></span>
- <span data-ttu-id="38fe1-178">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-178">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-179">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-179">**Submission type**</span></span>
- <span data-ttu-id="38fe1-180">**Motif de remise**</span><span class="sxs-lookup"><span data-stu-id="38fe1-180">**Delivery reason**</span></span>
- <span data-ttu-id="38fe1-181">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-181">**Status**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-182">**Type de contrôle**</span><span class="sxs-lookup"><span data-stu-id="38fe1-182">**Control type**</span></span>
- <span data-ttu-id="38fe1-183">**Source du contrôle**</span><span class="sxs-lookup"><span data-stu-id="38fe1-183">**Control source**</span></span>

  <span data-ttu-id="38fe1-184"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-184"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="38fe1-185">Afficher les envois d’URL d’administrateur</span><span class="sxs-lookup"><span data-stu-id="38fe1-185">View admin URL submissions</span></span>

<span data-ttu-id="38fe1-186">Cliquez sur l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-186">Click the **URL** tab.</span></span>

<span data-ttu-id="38fe1-187">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="38fe1-187">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="38fe1-188">**Date**</span><span class="sxs-lookup"><span data-stu-id="38fe1-188">**Date**</span></span>
- <span data-ttu-id="38fe1-189">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="38fe1-189">**Submission ID**</span></span>
- <span data-ttu-id="38fe1-190">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-190">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-191">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-191">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-192">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-192">**Submission type**</span></span>
- <span data-ttu-id="38fe1-193">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-193">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="38fe1-194"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-194"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="38fe1-195">Afficher les envois de pièces jointes admin</span><span class="sxs-lookup"><span data-stu-id="38fe1-195">View admin attachment submissions</span></span>

<span data-ttu-id="38fe1-196">Cliquez sur l’onglet **pièces jointes** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-196">Click the **Attachments** tab.</span></span>

<span data-ttu-id="38fe1-197">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="38fe1-197">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="38fe1-198">**Date**</span><span class="sxs-lookup"><span data-stu-id="38fe1-198">**Date**</span></span>
- <span data-ttu-id="38fe1-199">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="38fe1-199">**Submission ID**</span></span>
- <span data-ttu-id="38fe1-200">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-200">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-201">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-201">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-202">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-202">**Submission type**</span></span>
- <span data-ttu-id="38fe1-203">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-203">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="38fe1-204"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-204"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="38fe1-205">Afficher les soumissions des utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="38fe1-205">View user submissions to Microsoft</span></span>

<span data-ttu-id="38fe1-206">Si vous avez déployé le [complément de rapport de message](enable-the-report-message-add-in.md)ou que les utilisateurs utilisent la [création de rapports intégrée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), vous pouvez voir ce que les utilisateurs signalent sous l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-206">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="38fe1-207">Dans le centre de sécurité & conformité, accédez **à gestion** \> des menaces- **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-207">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="38fe1-208">Sur la page des **envois** qui s’affiche, cliquez sur l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-208">On the **Submissions** page that appears, click the **User submissions** tab.</span></span>

<span data-ttu-id="38fe1-209">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="38fe1-209">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="38fe1-210">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="38fe1-210">**Submitted on**</span></span>
- <span data-ttu-id="38fe1-211">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-211">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-212">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-212">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-213">**Sender**</span><span class="sxs-lookup"><span data-stu-id="38fe1-213">**Sender**</span></span>
- <span data-ttu-id="38fe1-214">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-214">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-215">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-215">**Submission type**</span></span>

<span data-ttu-id="38fe1-216"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-216"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="38fe1-217">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **expéditeur** en entrant une valeur dans la zone, puis en ![cliquant sur](../../media/scc-quarantine-refresh.png)le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="38fe1-217">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="38fe1-218">Update</span><span class="sxs-lookup"><span data-stu-id="38fe1-218">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="38fe1-219">Pour modifier les critères de filtre, cliquez sur le bouton **expéditeur** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-219">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="38fe1-220">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="38fe1-220">**Sender domain**</span></span>
- <span data-ttu-id="38fe1-221">**Subject**</span><span class="sxs-lookup"><span data-stu-id="38fe1-221">**Subject**</span></span>
- <span data-ttu-id="38fe1-222">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="38fe1-222">**Submitted by**</span></span>
- <span data-ttu-id="38fe1-223">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-223">**Submission type**</span></span>
- <span data-ttu-id="38fe1-224">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="38fe1-224">**Sender IP**</span></span>

![Options de filtrage pour les soumissions des utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="38fe1-226">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-226">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="38fe1-227">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="38fe1-227">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="38fe1-228">Afficher les soumissions des utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="38fe1-228">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="38fe1-229">Si vous avez [configuré une boîte aux lettres personnalisée](user-submission.md) pour recevoir des messages signalés par l’utilisateur, vous pouvez afficher et envoyer également les messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="38fe1-229">If you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="38fe1-230">Dans le centre de sécurité & conformité, accédez **à gestion** \> des menaces- **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-230">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="38fe1-231">Sur la page des **envois** qui s’affiche, cliquez sur l’onglet **boîte aux lettres personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="38fe1-231">On the **Submissions** page that appears, click the **Custom mailbox** tab.</span></span>

<span data-ttu-id="38fe1-232">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="38fe1-232">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="38fe1-233">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="38fe1-233">**Submitted on**</span></span>
- <span data-ttu-id="38fe1-234">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-234">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-235">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-235">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-236">**Sender**</span><span class="sxs-lookup"><span data-stu-id="38fe1-236">**Sender**</span></span>
- <span data-ttu-id="38fe1-237">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="38fe1-237">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="38fe1-238">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="38fe1-238">**Submission type**</span></span>

<span data-ttu-id="38fe1-239">En haut de la page, vous pouvez entrer une date de début, une date de fin et un filtre par **envoyé par** en entrant une valeur dans la zone, puis en ![cliquant sur](../../media/scc-quarantine-refresh.png)le bouton Actualiser.</span><span class="sxs-lookup"><span data-stu-id="38fe1-239">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="38fe1-240">Update</span><span class="sxs-lookup"><span data-stu-id="38fe1-240">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="38fe1-241">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="38fe1-241">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="38fe1-242">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="38fe1-242">In the dialog that appears, save the .csv file.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="38fe1-243">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="38fe1-243">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="38fe1-244">Si vous avez configuré la boîte aux lettres personnalisée de sorte qu’elle intercepte les messages signalés par l’utilisateur sans envoyer les messages à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="38fe1-244">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="38fe1-245">Cela déplace effectivement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="38fe1-245">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="38fe1-246">Sous l’onglet **boîte aux lettres personnalisée** , sélectionnez un message dans la liste, cliquez sur le bouton d' **action** , puis effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="38fe1-246">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="38fe1-247">**État de la notification**</span><span class="sxs-lookup"><span data-stu-id="38fe1-247">**Report clean**</span></span>
- <span data-ttu-id="38fe1-248">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="38fe1-248">**Report phishing**</span></span>
- <span data-ttu-id="38fe1-249">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="38fe1-249">**Report malware**</span></span>
- <span data-ttu-id="38fe1-250">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="38fe1-250">**Report spam**</span></span>

![Options du bouton d’action](../../media/user-submission-custom-mailbox-action-button.png)
