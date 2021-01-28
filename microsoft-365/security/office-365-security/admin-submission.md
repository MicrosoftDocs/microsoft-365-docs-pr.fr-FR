---
title: Soumissions d’administrateur
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le portail Soumissions dans le Centre de sécurité & conformité pour soumettre des messages suspects, des messages de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement dangereux, des URL et des fichiers à Microsoft pour analyse.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ed417db93bc2f3efa6b85b0ef97c10b5941cd8eb
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029513"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="a1323-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="a1323-104">Dans les organisations Microsoft 365 ayant des boîtes aux lettres dans Exchange Online, les administrateurs peuvent utiliser le portail Soumissions dans le Centre de sécurité & conformité pour envoyer des messages électroniques, des URL et des pièces jointes à Microsoft à des titres d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a1323-104">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="a1323-105">Lorsque vous envoyez un message électronique, vous recevez les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="a1323-105">When you submit an email message, you will get:</span></span>

1. <span data-ttu-id="a1323-106">**Vérification de l’authentification du** courrier électronique : détails sur la réussi ou l’échec de l’authentification de messagerie lors de sa livraison.</span><span class="sxs-lookup"><span data-stu-id="a1323-106">**Email authentication check**: Details on whether email authentication passed or failed when it was delivered.</span></span>
2. <span data-ttu-id="a1323-107">**Accès aux** stratégies : informations sur les stratégies qui ont autorisé ou bloqué le courrier entrant dans votre client, en remplacement de nos verdicts de filtre de service.</span><span class="sxs-lookup"><span data-stu-id="a1323-107">**Policy hits**: Information about any policies that may have allowed or blocked the incoming email into your tenant, overriding our service filter verdicts.</span></span>
3. <span data-ttu-id="a1323-108">**Réputation/détonation de la charge utile**: examen des URL et pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="a1323-108">**Payload reputation/detonation**: Examination of any URLs and attachments in the message.</span></span>
4. <span data-ttu-id="a1323-109">**Analyse du gradeur**: révision effectuée par des élèves humains afin de confirmer si les messages sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="a1323-109">**Grader analysis**: Review done by human graders in order to confirm whether or not messages are malicious.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1323-110">L’analyse de réputation/détonation et de grader de la charge utile n’est pas effectuée dans tous les locataires.</span><span class="sxs-lookup"><span data-stu-id="a1323-110">Payload reputation/detonation and grader analysis are not done in all tenants.</span></span> <span data-ttu-id="a1323-111">Les informations ne peuvent pas sortir de l’organisation lorsque les données ne sont pas supposées quitter la limite du client à des fins de conformité.</span><span class="sxs-lookup"><span data-stu-id="a1323-111">Information is blocked from going outside the organization when data is not supposed to leave the tenant boundary for compliance purposes.</span></span>

<span data-ttu-id="a1323-112">Pour d’autres façons de soumettre des messages électroniques, des URL et des pièces jointes à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a1323-112">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a1323-113">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a1323-113">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a1323-114">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="a1323-114">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="a1323-115">Pour aller directement à la page **soumission,** utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="a1323-115">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="a1323-116">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="a1323-116">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="a1323-117">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a1323-117">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  - <span data-ttu-id="a1323-118">**Gestion de l’organisation** [dans Exchange Online.](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups)</span><span class="sxs-lookup"><span data-stu-id="a1323-118">**Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="a1323-119">Notez que l’appartenance à ce groupe de rôles est nécessaire pour afficher les [soumissions](#view-user-submissions-to-the-custom-mailbox) d’utilisateurs à la boîte aux lettres personnalisée, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a1323-119">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this article.</span></span>

- <span data-ttu-id="a1323-120">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a1323-120">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="a1323-121">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-121">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="a1323-122">Dans le Centre de sécurité &  conformité, allez aux soumissions de gestion des menaces, vérifiez que vous êtes sous \> l’onglet **Soumissions** d’administrateur, puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a1323-122">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

2. <span data-ttu-id="a1323-123">Utilisez **le nouveau volant** de soumission qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a1323-123">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="a1323-124">Envoyer un e-mail douteux à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-124">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="a1323-125">Dans la section **Type d’objet,** sélectionnez **Courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="a1323-125">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="a1323-126">Dans la section **Format de** soumission, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-126">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="a1323-127">**ID** de message réseau : il s’agit d’une valeur GUID disponible dans l’en-tête **X-MS-Exchange-Organization-Network-Message-Id** du message ou dans l’en-tête **X-MS-Office365-Filtering-Correlation-Id** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a1323-127">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message, or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>

   - <span data-ttu-id="a1323-128">**Fichier**: cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="a1323-128">**File**: Click **Choose file**.</span></span> <span data-ttu-id="a1323-129">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier .eml ou .msg, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="a1323-129">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a1323-130">Les administrateurs avec Defender pour Office 365 Plan 1 ou Plan 2 peuvent envoyer des messages de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a1323-130">Admins with Defender for Office 365 Plan 1 or Plan 2 are able to submit messages as old as 30 days.</span></span> <span data-ttu-id="a1323-131">Les autres administrateurs ne pourront revenir qu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="a1323-131">Other admins will only be able to go back 7 days.</span></span>

2. <span data-ttu-id="a1323-132">Dans la section **Destinataires,** spécifiez un ou plusieurs destinataires pour qui vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="a1323-132">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="a1323-133">La vérification de stratégie détermine si le courrier électronique a contourné l’analyse en raison des stratégies utilisateur ou organisation.</span><span class="sxs-lookup"><span data-stu-id="a1323-133">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="a1323-134">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-134">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a1323-135">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a1323-135">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a1323-136">**Doit avoir été bloqué :** sélectionner le courrier **indésirable,** **le hameçonnage** ou les programmes **malveillants.**</span><span class="sxs-lookup"><span data-stu-id="a1323-136">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="a1323-137">Si vous n’êtes pas sûr, faites votre meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="a1323-137">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="a1323-138">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a1323-138">When you're finished, click the **Submit** button.</span></span>

   ![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="a1323-140">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-140">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="a1323-141">Dans la section **Type d’objet,** sélectionnez **URL.**</span><span class="sxs-lookup"><span data-stu-id="a1323-141">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="a1323-142">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="a1323-142">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="a1323-143">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-143">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a1323-144">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a1323-144">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a1323-145">**Doit avoir été bloqué :** sélectionnez **Hameçonnage** ou **Programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="a1323-145">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="a1323-146">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a1323-146">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d’envoi de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="a1323-148">Soumettre un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-148">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="a1323-149">Dans la section **Type d’objet,** sélectionnez **Pièce jointe.**</span><span class="sxs-lookup"><span data-stu-id="a1323-149">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="a1323-150">Cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="a1323-150">Click **Choose File**.</span></span> <span data-ttu-id="a1323-151">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="a1323-151">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="a1323-152">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-152">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a1323-153">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a1323-153">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a1323-154">**Doit avoir été bloqué :** un **programme** malveillant est le seul choix et est automatiquement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a1323-154">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="a1323-155">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a1323-155">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d’envoi de pièce jointe](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="a1323-157">Afficher les soumissions d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a1323-157">View admin submissions</span></span>

<span data-ttu-id="a1323-158">Dans le Centre de sécurité &  conformité, allez aux soumissions de gestion des menaces, vérifiez que vous êtes sous \> l’onglet **Soumissions** d’administrateur, puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a1323-158">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="a1323-159">Près du haut de la page, vous pouvez entrer une date de début, une date de fin et (par défaut) vous pouvez filtrer par **ID** de soumission (une valeur GUID affectée à chaque soumission) en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a1323-159">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a1323-160">Update</span><span class="sxs-lookup"><span data-stu-id="a1323-160">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a1323-161">Pour modifier les critères de filtre, cliquez sur le bouton **ID** de soumission et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-161">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="a1323-162">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a1323-162">**Sender**</span></span>
- <span data-ttu-id="a1323-163">**Objet/URL/Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="a1323-163">**Subject/URL/File name**</span></span>
- <span data-ttu-id="a1323-164">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="a1323-164">**Submitted by**</span></span>
- <span data-ttu-id="a1323-165">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-165">**Submission type**</span></span>
- <span data-ttu-id="a1323-166">**État**</span><span class="sxs-lookup"><span data-stu-id="a1323-166">**Status**</span></span>

![Options de filtrage pour les soumissions d’administrateurs](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="a1323-168">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a1323-168">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a1323-169">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a1323-169">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="a1323-170">Sous le graphique, il y a trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe**.</span><span class="sxs-lookup"><span data-stu-id="a1323-170">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="a1323-171">Afficher les envois de courriers électroniques d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a1323-171">View admin email submissions</span></span>

<span data-ttu-id="a1323-172">Cliquez sur **l’onglet** Courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a1323-172">Click the **Email** tab.</span></span>

<span data-ttu-id="a1323-173">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a1323-173">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a1323-174">**Date**</span><span class="sxs-lookup"><span data-stu-id="a1323-174">**Date**</span></span>
- <span data-ttu-id="a1323-175">**ID de soumission**: valeur GUID attribuée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="a1323-175">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="a1323-176">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-176">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-177">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-177">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-178">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a1323-178">**Sender**</span></span>
- <span data-ttu-id="a1323-179">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-179">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-180">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-180">**Submission type**</span></span>
- <span data-ttu-id="a1323-181">**Raison de la remise**</span><span class="sxs-lookup"><span data-stu-id="a1323-181">**Delivery reason**</span></span>
- <span data-ttu-id="a1323-182">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-182">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a1323-183"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a1323-183"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

#### <a name="admin-submission-rescan-details"></a><span data-ttu-id="a1323-184">Détails de la rescan de soumission de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="a1323-184">Admin submission rescan details</span></span>

<span data-ttu-id="a1323-185">Les messages envoyés dans les soumissions d’administrateur sont réassurés et les résultats sont affichés dans le volant de détails :</span><span class="sxs-lookup"><span data-stu-id="a1323-185">Messages that are submitted in admin submissions are rescanned and results shown in the details flyout:</span></span>

- <span data-ttu-id="a1323-186">En cas d’échec de l’authentification de messagerie de l’expéditeur au moment de la remise.</span><span class="sxs-lookup"><span data-stu-id="a1323-186">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="a1323-187">Informations sur les occurrences de stratégie qui auraient pu avoir affecté ou inttérable le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="a1323-187">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="a1323-188">Résultats actuels de la détonation pour voir si les URL ou les fichiers contenus dans le message sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="a1323-188">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="a1323-189">Commentaires des élèves.</span><span class="sxs-lookup"><span data-stu-id="a1323-189">Feedback from graders.</span></span>

<span data-ttu-id="a1323-190">Si une substitution a été trouvée, la rescan doit se terminer en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a1323-190">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="a1323-191">S’il n’y a pas de problème dans l’authentification ou la remise du courrier électronique n’a pas été affecté par une substitution, les commentaires des élèves peuvent prendre jusqu’à un jour.</span><span class="sxs-lookup"><span data-stu-id="a1323-191">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="a1323-192">Afficher les soumissions d’URL d’administration</span><span class="sxs-lookup"><span data-stu-id="a1323-192">View admin URL submissions</span></span>

<span data-ttu-id="a1323-193">Cliquez sur **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="a1323-193">Click the **URL** tab.</span></span>

<span data-ttu-id="a1323-194">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a1323-194">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a1323-195">**Date**</span><span class="sxs-lookup"><span data-stu-id="a1323-195">**Date**</span></span>
- <span data-ttu-id="a1323-196">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-196">**Submission ID**</span></span>
- <span data-ttu-id="a1323-197">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-197">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-198">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-198">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-199">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-199">**Submission type**</span></span>
- <span data-ttu-id="a1323-200">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-200">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a1323-201"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a1323-201"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="a1323-202">Afficher les soumissions de pièces jointes d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a1323-202">View admin attachment submissions</span></span>

<span data-ttu-id="a1323-203">Cliquez sur **l’onglet Pièces jointes.**</span><span class="sxs-lookup"><span data-stu-id="a1323-203">Click the **Attachments** tab.</span></span>

<span data-ttu-id="a1323-204">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a1323-204">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a1323-205">**Date**</span><span class="sxs-lookup"><span data-stu-id="a1323-205">**Date**</span></span>
- <span data-ttu-id="a1323-206">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-206">**Submission ID**</span></span>
- <span data-ttu-id="a1323-207">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-207">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-208">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-208">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-209">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-209">**Submission type**</span></span>
- <span data-ttu-id="a1323-210">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-210">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a1323-211"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a1323-211"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="a1323-212">Afficher les soumissions d’utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a1323-212">View user submissions to Microsoft</span></span>

<span data-ttu-id="a1323-213">Si vous avez déployé le [add-in](enable-the-report-message-add-in.md) [](enable-the-report-phish-add-in.md)Signaler un message, le module de signalement du hameçonnage ou que des personnes utilisent les rapports intégrés dans [Outlook sur le web,](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)vous pouvez voir ce que les utilisateurs signalent sous l’onglet Soumissions des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="a1323-213">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), the [Report Phishing add-in](enable-the-report-phish-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="a1323-214">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="a1323-214">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="a1323-215">Sélectionnez **l’onglet Soumissions utilisateur,** puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a1323-215">Select the **User submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="a1323-216">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a1323-216">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a1323-217">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="a1323-217">**Submitted on**</span></span>
- <span data-ttu-id="a1323-218">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-218">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-219">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-219">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-220">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a1323-220">**Sender**</span></span>
- <span data-ttu-id="a1323-221">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-221">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-222">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-222">**Submission type**</span></span>

<span data-ttu-id="a1323-223"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a1323-223"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="a1323-224">En haut de la page, vous pouvez entrer une date de début, une  date de fin et (par défaut) vous pouvez filtrer par expéditeur en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a1323-224">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a1323-225">Update</span><span class="sxs-lookup"><span data-stu-id="a1323-225">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a1323-226">Pour modifier les critères de filtre, cliquez sur le bouton **Expéditeur** et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-226">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="a1323-227">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a1323-227">**Sender domain**</span></span>
- <span data-ttu-id="a1323-228">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a1323-228">**Subject**</span></span>
- <span data-ttu-id="a1323-229">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="a1323-229">**Submitted by**</span></span>
- <span data-ttu-id="a1323-230">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-230">**Submission type**</span></span>
- <span data-ttu-id="a1323-231">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a1323-231">**Sender IP**</span></span>

![Options de filtrage pour les envois d’utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="a1323-233">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a1323-233">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a1323-234">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a1323-234">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="a1323-235">Afficher les envois d’utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="a1323-235">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="a1323-236">**Si** vous avez configuré [une](user-submission.md) boîte aux lettres personnalisée pour recevoir les messages signalés par l’utilisateur, vous pouvez afficher et envoyer des messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="a1323-236">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="a1323-237">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="a1323-237">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="a1323-238">Sélectionnez **l’onglet Boîte aux lettres** personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a1323-238">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="a1323-239">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a1323-239">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a1323-240">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="a1323-240">**Submitted on**</span></span>
- <span data-ttu-id="a1323-241">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-241">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-242">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-242">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-243">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a1323-243">**Sender**</span></span>
- <span data-ttu-id="a1323-244">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a1323-244">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a1323-245">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a1323-245">**Submission type**</span></span>

<span data-ttu-id="a1323-246">Dans la zone supérieure de la page, vous pouvez entrer une  date de début, une date de fin et vous pouvez filtrer en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a1323-246">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a1323-247">Update</span><span class="sxs-lookup"><span data-stu-id="a1323-247">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a1323-248">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a1323-248">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a1323-249">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a1323-249">In the dialog that appears, save the .csv file.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="a1323-250">Annuler les soumissions d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a1323-250">Undo user submissions</span></span>

<span data-ttu-id="a1323-251">Lorsqu’un utilisateur envoie un message suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler la soumission.</span><span class="sxs-lookup"><span data-stu-id="a1323-251">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="a1323-252">Si l’utilisateur souhaite récupérer le courrier électronique, il sera disponible pour la récupération dans les dossiers Éléments supprimés ou Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a1323-252">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="a1323-253">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="a1323-253">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="a1323-254">Si vous avez configuré la boîte aux lettres personnalisée pour intercepter les messages signalés par l’utilisateur sans les envoyer à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="a1323-254">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="a1323-255">Cela déplace efficacement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a1323-255">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="a1323-256">Sous **l’onglet Boîte** aux lettres personnalisée, sélectionnez un message dans la liste, cliquez sur le bouton **Action** et faites l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1323-256">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="a1323-257">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="a1323-257">**Report clean**</span></span>
- <span data-ttu-id="a1323-258">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a1323-258">**Report phishing**</span></span>
- <span data-ttu-id="a1323-259">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="a1323-259">**Report malware**</span></span>
- <span data-ttu-id="a1323-260">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a1323-260">**Report spam**</span></span>

![Options sur le bouton Action](../../media/user-submission-custom-mailbox-action-button.png)
