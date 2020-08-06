---
title: Soumissions de l’administrateur
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
description: Les administrateurs peuvent apprendre à utiliser le portail d’envoi du centre de sécurité & conformité pour envoyer des e-mails suspects, des courriers électroniques de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement nuisibles, des URL et des fichiers à Microsoft à des fins d’analyse.
ms.openlocfilehash: 4d0737d881334db9cc4aeda43037ab89d7444618
ms.sourcegitcommit: c04f1207cfaddac2a9abef38967c17d689756a96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2020
ms.locfileid: "46577869"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="8722f-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

<span data-ttu-id="8722f-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, les administrateurs peuvent utiliser le portail d’envoi du centre de sécurité & conformité pour soumettre des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="8722f-104">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="8722f-105">Lorsque vous soumettez un message électronique, vous obtenez des informations sur les stratégies susceptibles d’avoir autorisé le courrier entrant dans votre client, ainsi que sur l’examen de toutes les URL et pièces jointes du courrier.</span><span class="sxs-lookup"><span data-stu-id="8722f-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="8722f-106">Les stratégies pouvant avoir autorisé un courrier incluent la liste des expéditeurs approuvés d’un utilisateur individuel, ainsi que des stratégies au niveau du client, telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="8722f-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="8722f-107">Pour d’autres façons d’envoyer des messages électroniques, des URL et des pièces jointes à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="8722f-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8722f-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8722f-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8722f-109">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="8722f-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="8722f-110">Pour accéder directement à la page d' **envoi** , utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="8722f-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="8722f-111">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures. décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="8722f-111">You need to be assigned permissions before you can do the procedures in this topic:</span></span>

  - <span data-ttu-id="8722f-112">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="8722f-112">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="8722f-113">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8722f-113">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="8722f-114">**Gestion de l’organisation** ou **Gestion de l’hygiène** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="8722f-114">**Organization Management** or **Hygiene Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

  - <span data-ttu-id="8722f-115">Pour un accès en lecture seule au portail des soumissions, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="8722f-115">For read-only access to the Submissions portal, you need to be a member of one of the following role groups:</span></span>

    - <span data-ttu-id="8722f-116">**Lecteur de sécurité** dans le [Centre de conformité et sécurité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8722f-116">**Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    - <span data-ttu-id="8722f-117">**Gestion de l’organisation en affichage seul** dans[Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="8722f-117">**View-Only Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="8722f-118">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="8722f-118">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="8722f-119">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-119">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="8722f-120">Dans le centre de sécurité & conformité, accédez à **gestion des menaces** - \> **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-120">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="8722f-121">Sur la page des **envois** qui s’affiche, cliquez sur le bouton **nouvelle soumission** .</span><span class="sxs-lookup"><span data-stu-id="8722f-121">On the **Submissions** page that appears, click the **New submission** button.</span></span>

3. <span data-ttu-id="8722f-122">Utilisez le menu volant **nouvelle soumission** qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8722f-122">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="8722f-123">Envoyer un courrier électronique en question à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-123">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="8722f-124">Dans la section **type d’objet** , sélectionnez **courrier électronique**.</span><span class="sxs-lookup"><span data-stu-id="8722f-124">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="8722f-125">Dans la section **format de soumission** , utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-125">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="8722f-126">**ID de message réseau**: il s’agit d’une valeur GUID qui est disponible dans l’en-tête **X-MS-Exchange-Organization-Network-message-ID** du message.</span><span class="sxs-lookup"><span data-stu-id="8722f-126">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message.</span></span>

   - <span data-ttu-id="8722f-127">**Fichier**: cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="8722f-127">**File**: Click **Choose file**.</span></span> <span data-ttu-id="8722f-128">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier. eml ou. MSG, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="8722f-128">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

2. <span data-ttu-id="8722f-129">Dans la section **destinataires** , spécifiez un ou plusieurs destinataires sur lesquels vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="8722f-129">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="8722f-130">La vérification de stratégie détermine si l’analyse du courrier électronique a contourné les messages en raison des stratégies de l’utilisateur ou de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="8722f-130">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="8722f-131">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-131">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="8722f-132">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="8722f-132">**Should not have been blocked**</span></span>

   - <span data-ttu-id="8722f-133">**Doit avoir été bloqué**: sélectionnez **courrier indésirable**, **hameçonnage**ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="8722f-133">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="8722f-134">Si vous n’êtes pas sûr, utilisez votre meilleure appréciation.</span><span class="sxs-lookup"><span data-stu-id="8722f-134">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="8722f-135">Si le filtre a été contourné en raison de stratégies lors de l’envoi, vous verrez des informations sur cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="8722f-135">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

   <span data-ttu-id="8722f-136">Si le filtre n’a pas été contourné en raison d’une ou de plusieurs stratégies, l’analyse se terminera en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="8722f-136">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="8722f-137">Vous verrez des informations supplémentaires sur l’envoi en cliquant sur le lien État.</span><span class="sxs-lookup"><span data-stu-id="8722f-137">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="8722f-138">Cela inclut les résultats de la vérification de stratégie et le verdict de nouvelle analyse.</span><span class="sxs-lookup"><span data-stu-id="8722f-138">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="8722f-139">Remarque cela n’exécute pas de nouveau le courrier électronique via la pile de filtrage complet DAV d’Office 365 mais exécute une nouvelle analyse partielle en fonction de certains attributs de l’e-mail, de l’URL ou du fichier.</span><span class="sxs-lookup"><span data-stu-id="8722f-139">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span>

5. <span data-ttu-id="8722f-140">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="8722f-140">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="8722f-142">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-142">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="8722f-143">Dans la section **type d’objet** , sélectionnez **URL**.</span><span class="sxs-lookup"><span data-stu-id="8722f-143">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="8722f-144">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, <https://www.fabrikam.com/marketing.html> ).</span><span class="sxs-lookup"><span data-stu-id="8722f-144">In the box that appears, enter the full URL (for example, <https://www.fabrikam.com/marketing.html>).</span></span>

2. <span data-ttu-id="8722f-145">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-145">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="8722f-146">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="8722f-146">**Should not have been blocked**</span></span>

   - <span data-ttu-id="8722f-147">**Doit avoir été bloqué**: sélectionnez **hameçonnage** ou **programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="8722f-147">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="8722f-148">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="8722f-148">When you're finished, click the **Submit** button.</span></span>

![Exemple de dépôt de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="8722f-150">Envoyer un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-150">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="8722f-151">Dans la section **type d’objet** , sélectionnez **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="8722f-151">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="8722f-152">Cliquez sur **choisir un fichier**.</span><span class="sxs-lookup"><span data-stu-id="8722f-152">Click **Choose File**.</span></span> <span data-ttu-id="8722f-153">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="8722f-153">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="8722f-154">Dans la section **raison de l’envoi** , sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-154">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="8722f-155">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="8722f-155">**Should not have been blocked**</span></span>

   - <span data-ttu-id="8722f-156">**Doit avoir été bloqué**: le **programme malveillant** est le seul choix et est automatiquement sélectionné..</span><span class="sxs-lookup"><span data-stu-id="8722f-156">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="8722f-157">Lorsque vous avez terminé, cliquez sur le bouton **Envoyer** .</span><span class="sxs-lookup"><span data-stu-id="8722f-157">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission de pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="8722f-159">Afficher les soumissions de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="8722f-159">View admin submissions</span></span>

1. <span data-ttu-id="8722f-160">Dans le centre de sécurité & conformité, accédez à **gestion des menaces** - \> **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-160">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="8722f-161">Sur la page des **envois** qui s’affiche, vérifiez que l’onglet **soumissions** de l’administrateur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8722f-161">On the **Submissions** page that appears, verify that the **Admin submissions** tab is selected.</span></span>

<span data-ttu-id="8722f-162">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **ID de soumission** (valeur Guid affectée à chaque envoi) en entrant une valeur dans la zone et en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="8722f-162">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="8722f-163">Update</span><span class="sxs-lookup"><span data-stu-id="8722f-163">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="8722f-164">Pour modifier les critères de filtre, cliquez sur le bouton **ID de soumission** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-164">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="8722f-165">**Sender**</span><span class="sxs-lookup"><span data-stu-id="8722f-165">**Sender**</span></span>
- <span data-ttu-id="8722f-166">**Subject/URL/nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="8722f-166">**Subject/URL/File name**</span></span>
- <span data-ttu-id="8722f-167">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="8722f-167">**Submitted by**</span></span>
- <span data-ttu-id="8722f-168">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-168">**Submission type**</span></span>
- <span data-ttu-id="8722f-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="8722f-169">**Status**</span></span>

![Options de filtrage pour les soumissions d’administration](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="8722f-171">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="8722f-171">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="8722f-172">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="8722f-172">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="8722f-173">Sous le graphique, il existe trois onglets : **e-mail** (par défaut), **URL**et **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="8722f-173">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="8722f-174">Afficher les envois de courrier de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="8722f-174">View admin email submissions</span></span>

<span data-ttu-id="8722f-175">Cliquez sur l’onglet **e-mail** .</span><span class="sxs-lookup"><span data-stu-id="8722f-175">Click the **Email** tab.</span></span>

<span data-ttu-id="8722f-176">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="8722f-176">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="8722f-177">**Date**</span><span class="sxs-lookup"><span data-stu-id="8722f-177">**Date**</span></span>
- <span data-ttu-id="8722f-178">**ID de soumission**: valeur Guid assignée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="8722f-178">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="8722f-179">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-179">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-180">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-180">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-181">**Sender**</span><span class="sxs-lookup"><span data-stu-id="8722f-181">**Sender**</span></span>
- <span data-ttu-id="8722f-182">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-182">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-183">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-183">**Submission type**</span></span>
- <span data-ttu-id="8722f-184">**Motif de remise**</span><span class="sxs-lookup"><span data-stu-id="8722f-184">**Delivery reason**</span></span>
- <span data-ttu-id="8722f-185">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-185">**Status**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-186">**Type de contrôle**</span><span class="sxs-lookup"><span data-stu-id="8722f-186">**Control type**</span></span>
- <span data-ttu-id="8722f-187">**Source du contrôle**</span><span class="sxs-lookup"><span data-stu-id="8722f-187">**Control source**</span></span>

  <span data-ttu-id="8722f-188"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="8722f-188"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="8722f-189">Afficher les envois d’URL d’administrateur</span><span class="sxs-lookup"><span data-stu-id="8722f-189">View admin URL submissions</span></span>

<span data-ttu-id="8722f-190">Cliquez sur l’onglet **URL** .</span><span class="sxs-lookup"><span data-stu-id="8722f-190">Click the **URL** tab.</span></span>

<span data-ttu-id="8722f-191">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="8722f-191">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="8722f-192">**Date**</span><span class="sxs-lookup"><span data-stu-id="8722f-192">**Date**</span></span>
- <span data-ttu-id="8722f-193">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="8722f-193">**Submission ID**</span></span>
- <span data-ttu-id="8722f-194">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-194">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-195">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-195">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-196">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-196">**Submission type**</span></span>
- <span data-ttu-id="8722f-197">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-197">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="8722f-198"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="8722f-198"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="8722f-199">Afficher les envois de pièces jointes admin</span><span class="sxs-lookup"><span data-stu-id="8722f-199">View admin attachment submissions</span></span>

<span data-ttu-id="8722f-200">Cliquez sur l’onglet **pièces jointes** .</span><span class="sxs-lookup"><span data-stu-id="8722f-200">Click the **Attachments** tab.</span></span>

<span data-ttu-id="8722f-201">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="8722f-201">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="8722f-202">**Date**</span><span class="sxs-lookup"><span data-stu-id="8722f-202">**Date**</span></span>
- <span data-ttu-id="8722f-203">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="8722f-203">**Submission ID**</span></span>
- <span data-ttu-id="8722f-204">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-204">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-205">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-205">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-206">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-206">**Submission type**</span></span>
- <span data-ttu-id="8722f-207">**Originaire**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-207">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="8722f-208"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="8722f-208"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="8722f-209">Afficher les soumissions des utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="8722f-209">View user submissions to Microsoft</span></span>

<span data-ttu-id="8722f-210">Si vous avez déployé le [complément de rapport de message](enable-the-report-message-add-in.md)ou que les utilisateurs utilisent la [création de rapports intégrée dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), vous pouvez voir ce que les utilisateurs signalent sous l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-210">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="8722f-211">Dans le centre de sécurité & conformité, accédez à **gestion des menaces** - \> **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-211">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="8722f-212">Sur la page des **envois** qui s’affiche, cliquez sur l’onglet **soumissions** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-212">On the **Submissions** page that appears, click the **User submissions** tab.</span></span>

<span data-ttu-id="8722f-213">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="8722f-213">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="8722f-214">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="8722f-214">**Submitted on**</span></span>
- <span data-ttu-id="8722f-215">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-215">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-216">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-216">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-217">**Sender**</span><span class="sxs-lookup"><span data-stu-id="8722f-217">**Sender**</span></span>
- <span data-ttu-id="8722f-218">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-218">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-219">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-219">**Submission type**</span></span>

<span data-ttu-id="8722f-220"><sup>\*</sup>Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un lanceur.</span><span class="sxs-lookup"><span data-stu-id="8722f-220"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="8722f-221">En haut de la page, vous pouvez entrer une date de début, une date de fin et, par défaut, vous pouvez filtrer par **expéditeur** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="8722f-221">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="8722f-222">Update</span><span class="sxs-lookup"><span data-stu-id="8722f-222">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="8722f-223">Pour modifier les critères de filtre, cliquez sur le bouton **expéditeur** , puis choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-223">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="8722f-224">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8722f-224">**Sender domain**</span></span>
- <span data-ttu-id="8722f-225">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8722f-225">**Subject**</span></span>
- <span data-ttu-id="8722f-226">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="8722f-226">**Submitted by**</span></span>
- <span data-ttu-id="8722f-227">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-227">**Submission type**</span></span>
- <span data-ttu-id="8722f-228">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8722f-228">**Sender IP**</span></span>

![Options de filtrage pour les soumissions des utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="8722f-230">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="8722f-230">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="8722f-231">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="8722f-231">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="8722f-232">Afficher les soumissions des utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="8722f-232">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="8722f-233">Si vous avez [configuré une boîte aux lettres personnalisée](user-submission.md) pour recevoir des messages signalés par l’utilisateur, vous pouvez afficher et envoyer également les messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="8722f-233">If you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="8722f-234">Dans le centre de sécurité & conformité, accédez à **gestion des menaces** - \> **vérifier** \> **les messages d’envoi**de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-234">In the Security & Compliance Center, go to **Threat management** \> **Review** \> **Admin submission messages**.</span></span>

2. <span data-ttu-id="8722f-235">Sur la page des **envois** qui s’affiche, cliquez sur l’onglet **boîte aux lettres personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="8722f-235">On the **Submissions** page that appears, click the **Custom mailbox** tab.</span></span>

<span data-ttu-id="8722f-236">Vous pouvez cliquer sur le bouton **options de colonne** dans la partie inférieure de la page pour ajouter ou supprimer des colonnes dans l’affichage :</span><span class="sxs-lookup"><span data-stu-id="8722f-236">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="8722f-237">**Soumis le**</span><span class="sxs-lookup"><span data-stu-id="8722f-237">**Submitted on**</span></span>
- <span data-ttu-id="8722f-238">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-238">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-239">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-239">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-240">**Sender**</span><span class="sxs-lookup"><span data-stu-id="8722f-240">**Sender**</span></span>
- <span data-ttu-id="8722f-241">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8722f-241">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="8722f-242">**Type d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8722f-242">**Submission type**</span></span>

<span data-ttu-id="8722f-243">En haut de la page, vous pouvez entrer une date de début, une date de fin et un filtre par **envoyé par** en entrant une valeur dans la zone, puis en cliquant sur le ![ bouton actualiser ](../../media/scc-quarantine-refresh.png) .</span><span class="sxs-lookup"><span data-stu-id="8722f-243">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="8722f-244">Update</span><span class="sxs-lookup"><span data-stu-id="8722f-244">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="8722f-245">Pour exporter les résultats, cliquez sur **Exporter** vers le haut de la page, puis sélectionnez **données de graphique** ou **tableau**.</span><span class="sxs-lookup"><span data-stu-id="8722f-245">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="8722f-246">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="8722f-246">In the dialog that appears, save the .csv file.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="8722f-247">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="8722f-247">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="8722f-248">Si vous avez configuré la boîte aux lettres personnalisée de sorte qu’elle intercepte les messages signalés par l’utilisateur sans envoyer les messages à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="8722f-248">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="8722f-249">Cela déplace effectivement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8722f-249">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="8722f-250">Sous l’onglet **boîte aux lettres personnalisée** , sélectionnez un message dans la liste, cliquez sur le bouton d' **action** , puis effectuez l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="8722f-250">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="8722f-251">**État de la notification**</span><span class="sxs-lookup"><span data-stu-id="8722f-251">**Report clean**</span></span>
- <span data-ttu-id="8722f-252">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="8722f-252">**Report phishing**</span></span>
- <span data-ttu-id="8722f-253">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="8722f-253">**Report malware**</span></span>
- <span data-ttu-id="8722f-254">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8722f-254">**Report spam**</span></span>

![Options du bouton d’action](../../media/user-submission-custom-mailbox-action-button.png)
