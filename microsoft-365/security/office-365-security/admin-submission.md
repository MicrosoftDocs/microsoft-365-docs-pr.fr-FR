---
title: Soumissions d’administrateur
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
description: Les administrateurs peuvent apprendre à utiliser le portail Soumissions dans le Centre de sécurité & conformité pour soumettre des messages suspects, des messages de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement dangereux, des URL et des fichiers à Microsoft pour analyse.
ms.openlocfilehash: 432a245530d7906ae8babbc54176480d36315351
ms.sourcegitcommit: cc354fd54400be0ff0401f60bbe68ed975b69cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "49864947"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="a62b7-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="a62b7-104">Dans les organisations Microsoft 365 ayant des boîtes aux lettres dans Exchange Online, les administrateurs peuvent utiliser le portail Soumissions dans le Centre de sécurité & conformité pour envoyer des messages électroniques, des URL et des pièces jointes à Microsoft à des titres d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a62b7-104">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="a62b7-105">Lorsque vous envoyez un e-mail, vous obtenez des informations sur les stratégies qui ont autorisé le courrier entrant dans votre client, ainsi que l’examen des URL et pièces jointes dans le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a62b7-105">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="a62b7-106">Les stratégies qui ont autorisé un courrier incluent la liste des expéditeurs autorisés d’un utilisateur individuel, ainsi que les stratégies au niveau du client telles que les règles de flux de messagerie Exchange (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="a62b7-106">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as Exchange mail flow rules (also known as transport rules).</span></span>

<span data-ttu-id="a62b7-107">Pour d’autres façons de soumettre des messages électroniques, des URL et des pièces jointes à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a62b7-107">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a62b7-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a62b7-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a62b7-109">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="a62b7-109">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="a62b7-110">Pour aller directement à la page **soumission,** utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="a62b7-110">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="a62b7-111">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="a62b7-111">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="a62b7-112">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a62b7-112">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  - <span data-ttu-id="a62b7-113">**Gestion de l’organisation** [dans Exchange Online.](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups)</span><span class="sxs-lookup"><span data-stu-id="a62b7-113">**Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="a62b7-114">Notez que l’appartenance à ce groupe de rôles est nécessaire pour afficher les [soumissions](#view-user-submissions-to-the-custom-mailbox) d’utilisateurs à la boîte aux lettres personnalisée, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a62b7-114">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this article.</span></span>

- <span data-ttu-id="a62b7-115">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, voir Signaler des messages et [des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a62b7-115">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="a62b7-116">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-116">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="a62b7-117">Dans le Centre de sécurité &  conformité, allez aux soumissions de gestion des menaces, vérifiez que vous êtes sous \> l’onglet **Soumissions** d’administrateur, puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-117">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

2. <span data-ttu-id="a62b7-118">Utilisez **le nouveau volant** de soumission qui apparaît pour envoyer le message, l’URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a62b7-118">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="a62b7-119">Envoyer un e-mail douteux à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-119">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="a62b7-120">Dans la section **Type d’objet,** sélectionnez **Courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-120">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="a62b7-121">Dans la section **Format de** soumission, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-121">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="a62b7-122">**ID** de message réseau : il s’agit d’une valeur GUID disponible dans l’en-tête **X-MS-Exchange-Organization-Network-Message-Id** du message ou dans l’en-tête **X-MS-Office365-Filtering-Correlation-Id** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a62b7-122">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message, or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>

   - <span data-ttu-id="a62b7-123">**Fichier**: cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-123">**File**: Click **Choose file**.</span></span> <span data-ttu-id="a62b7-124">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier .eml ou .msg, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="a62b7-124">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a62b7-125">Les administrateurs avec Defender pour Office 365 Plan 1 ou Plan 2 peuvent envoyer des messages de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a62b7-125">Admins with Defender for Office 365 Plan 1 or Plan 2 are able to submit messages as old as 30 days.</span></span> <span data-ttu-id="a62b7-126">Les autres administrateurs ne pourront revenir qu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="a62b7-126">Other admins will only be able to go back 7 days.</span></span>

2. <span data-ttu-id="a62b7-127">Dans la section **Destinataires,** spécifiez un ou plusieurs destinataires pour qui vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="a62b7-127">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="a62b7-128">La vérification de stratégie détermine si le courrier électronique a contourné l’analyse en raison des stratégies utilisateur ou organisation.</span><span class="sxs-lookup"><span data-stu-id="a62b7-128">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="a62b7-129">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-129">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a62b7-130">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a62b7-130">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a62b7-131">**Doit avoir été bloqué :** sélectionner le courrier **indésirable,** **le hameçonnage** ou les programmes **malveillants.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-131">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="a62b7-132">Si vous n’êtes pas sûr, faites votre meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="a62b7-132">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="a62b7-133">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a62b7-133">When you're finished, click the **Submit** button.</span></span>

![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="a62b7-135">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-135">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="a62b7-136">Dans la section **Type d’objet,** sélectionnez **URL.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-136">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="a62b7-137">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="a62b7-137">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="a62b7-138">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-138">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a62b7-139">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a62b7-139">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a62b7-140">**Doit avoir été bloqué :** sélectionnez **Hameçonnage** ou **Programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-140">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="a62b7-141">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a62b7-141">When you're finished, click the **Submit** button.</span></span>

![Exemple d’envoi de courrier électronique](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="a62b7-143">Soumettre un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-143">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="a62b7-144">Dans la section **Type d’objet,** sélectionnez **Pièce jointe.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-144">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="a62b7-145">Cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-145">Click **Choose File**.</span></span> <span data-ttu-id="a62b7-146">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-146">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="a62b7-147">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-147">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="a62b7-148">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="a62b7-148">**Should not have been blocked**</span></span>

   - <span data-ttu-id="a62b7-149">**Doit avoir été bloqué :** un **programme** malveillant est le seul choix et est automatiquement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="a62b7-149">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="a62b7-150">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="a62b7-150">When you're finished, click the **Submit** button.</span></span>

![Exemple d’envoi de pièce jointe](../../media/submission-file-flyout.PNG)

## <a name="view-admin-submissions"></a><span data-ttu-id="a62b7-152">Afficher les soumissions d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a62b7-152">View admin submissions</span></span>

<span data-ttu-id="a62b7-153">Dans le Centre de sécurité &  conformité, allez aux soumissions de gestion des menaces, vérifiez que vous êtes sous \> l’onglet **Soumissions** d’administrateur, puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-153">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="a62b7-154">Dans la partie supérieure de la page, vous pouvez entrer une date de début, une date de fin et (par défaut) vous pouvez filtrer par **ID** de soumission (une valeur GUID affectée à chaque soumission) en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a62b7-154">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a62b7-155">Update</span><span class="sxs-lookup"><span data-stu-id="a62b7-155">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a62b7-156">Pour modifier les critères de filtre, cliquez sur le bouton **ID** de soumission et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-156">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="a62b7-157">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a62b7-157">**Sender**</span></span>
- <span data-ttu-id="a62b7-158">**Objet/URL/Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="a62b7-158">**Subject/URL/File name**</span></span>
- <span data-ttu-id="a62b7-159">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="a62b7-159">**Submitted by**</span></span>
- <span data-ttu-id="a62b7-160">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-160">**Submission type**</span></span>
- <span data-ttu-id="a62b7-161">**État**</span><span class="sxs-lookup"><span data-stu-id="a62b7-161">**Status**</span></span>

![Options de filtrage pour les soumissions d’administrateurs](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="a62b7-163">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-163">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a62b7-164">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a62b7-164">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="a62b7-165">Sous le graphique, il y a trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-165">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="a62b7-166">Afficher les envois de courriers électroniques d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a62b7-166">View admin email submissions</span></span>

<span data-ttu-id="a62b7-167">Cliquez sur **l’onglet** Courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="a62b7-167">Click the **Email** tab.</span></span>

<span data-ttu-id="a62b7-168">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a62b7-168">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a62b7-169">**Date**</span><span class="sxs-lookup"><span data-stu-id="a62b7-169">**Date**</span></span>
- <span data-ttu-id="a62b7-170">**ID de soumission**: valeur GUID attribuée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="a62b7-170">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="a62b7-171">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-171">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-172">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-172">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-173">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a62b7-173">**Sender**</span></span>
- <span data-ttu-id="a62b7-174">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-174">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-175">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-175">**Submission type**</span></span>
- <span data-ttu-id="a62b7-176">**Raison de la remise**</span><span class="sxs-lookup"><span data-stu-id="a62b7-176">**Delivery reason**</span></span>
- <span data-ttu-id="a62b7-177">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-177">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a62b7-178"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a62b7-178"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

#### <a name="admin-submission-rescan-details"></a><span data-ttu-id="a62b7-179">Détails de la rescan de soumission de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="a62b7-179">Admin submission rescan details</span></span>

<span data-ttu-id="a62b7-180">Les messages envoyés dans les soumissions d’administrateur sont réassurés et les résultats sont affichés dans le volant de détails :</span><span class="sxs-lookup"><span data-stu-id="a62b7-180">Messages that are submitted in admin submissions are rescanned and results shown in the details flyout:</span></span>

- <span data-ttu-id="a62b7-181">En cas d’échec de l’authentification de messagerie de l’expéditeur au moment de la remise.</span><span class="sxs-lookup"><span data-stu-id="a62b7-181">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="a62b7-182">Informations sur les occurrences de stratégie qui auraient pu avoir affecté ou inttérable le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="a62b7-182">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="a62b7-183">Résultats actuels de la détonation pour voir si les URL ou les fichiers contenus dans le message sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="a62b7-183">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="a62b7-184">Commentaires des élèves.</span><span class="sxs-lookup"><span data-stu-id="a62b7-184">Feedback from graders.</span></span>

<span data-ttu-id="a62b7-185">Si une substitution a été trouvée, la rescan doit se terminer en quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="a62b7-185">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="a62b7-186">S’il n’y a pas de problème dans l’authentification ou la remise du courrier électronique n’a pas été affecté par une substitution, les commentaires des élèves peuvent prendre jusqu’à un jour.</span><span class="sxs-lookup"><span data-stu-id="a62b7-186">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="a62b7-187">Afficher les soumissions d’URL d’administration</span><span class="sxs-lookup"><span data-stu-id="a62b7-187">View admin URL submissions</span></span>

<span data-ttu-id="a62b7-188">Cliquez sur **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-188">Click the **URL** tab.</span></span>

<span data-ttu-id="a62b7-189">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a62b7-189">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a62b7-190">**Date**</span><span class="sxs-lookup"><span data-stu-id="a62b7-190">**Date**</span></span>
- <span data-ttu-id="a62b7-191">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-191">**Submission ID**</span></span>
- <span data-ttu-id="a62b7-192">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-192">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-193">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-193">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-194">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-194">**Submission type**</span></span>
- <span data-ttu-id="a62b7-195">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-195">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a62b7-196"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a62b7-196"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="a62b7-197">Afficher les soumissions de pièces jointes d’administrateur</span><span class="sxs-lookup"><span data-stu-id="a62b7-197">View admin attachment submissions</span></span>

<span data-ttu-id="a62b7-198">Cliquez sur **l’onglet Pièces jointes.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-198">Click the **Attachments** tab.</span></span>

<span data-ttu-id="a62b7-199">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a62b7-199">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a62b7-200">**Date**</span><span class="sxs-lookup"><span data-stu-id="a62b7-200">**Date**</span></span>
- <span data-ttu-id="a62b7-201">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-201">**Submission ID**</span></span>
- <span data-ttu-id="a62b7-202">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-202">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-203">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-203">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-204">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-204">**Submission type**</span></span>
- <span data-ttu-id="a62b7-205">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-205">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="a62b7-206"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a62b7-206"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="a62b7-207">Afficher les soumissions d’utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="a62b7-207">View user submissions to Microsoft</span></span>

<span data-ttu-id="a62b7-208">Si vous avez déployé le [add-in](enable-the-report-message-add-in.md) [](enable-the-report-phish-add-in.md)Signaler un message, le module de signalement du hameçonnage ou que des personnes utilisent les rapports intégrés dans [Outlook sur le web,](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)vous pouvez voir ce que les utilisateurs signalent sous l’onglet Soumissions des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-208">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), the [Report Phishing add-in](enable-the-report-phish-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="a62b7-209">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-209">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="a62b7-210">Sélectionnez **l’onglet Soumissions utilisateur,** puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-210">Select the **User submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="a62b7-211">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a62b7-211">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a62b7-212">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="a62b7-212">**Submitted on**</span></span>
- <span data-ttu-id="a62b7-213">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-213">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-214">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-214">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-215">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a62b7-215">**Sender**</span></span>
- <span data-ttu-id="a62b7-216">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-216">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-217">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-217">**Submission type**</span></span>

<span data-ttu-id="a62b7-218"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="a62b7-218"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="a62b7-219">Dans la zone supérieure de la page, vous pouvez entrer une date de  début, une date de fin et (par défaut) vous pouvez filtrer par expéditeur en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a62b7-219">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a62b7-220">Update</span><span class="sxs-lookup"><span data-stu-id="a62b7-220">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a62b7-221">Pour modifier les critères de filtre, cliquez sur le bouton **Expéditeur** et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-221">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="a62b7-222">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a62b7-222">**Sender domain**</span></span>
- <span data-ttu-id="a62b7-223">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a62b7-223">**Subject**</span></span>
- <span data-ttu-id="a62b7-224">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="a62b7-224">**Submitted by**</span></span>
- <span data-ttu-id="a62b7-225">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-225">**Submission type**</span></span>
- <span data-ttu-id="a62b7-226">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="a62b7-226">**Sender IP**</span></span>

![Options de filtrage pour les envois d’utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="a62b7-228">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-228">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a62b7-229">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a62b7-229">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="a62b7-230">Afficher les envois d’utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="a62b7-230">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="a62b7-231">**Si** vous avez configuré [une](user-submission.md) boîte aux lettres personnalisée pour recevoir les messages signalés par l’utilisateur, vous pouvez afficher et envoyer des messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="a62b7-231">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="a62b7-232">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-232">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="a62b7-233">Sélectionnez **l’onglet Boîte aux lettres** personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a62b7-233">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="a62b7-234">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="a62b7-234">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="a62b7-235">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="a62b7-235">**Submitted on**</span></span>
- <span data-ttu-id="a62b7-236">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-236">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-237">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-237">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-238">**Sender**</span><span class="sxs-lookup"><span data-stu-id="a62b7-238">**Sender**</span></span>
- <span data-ttu-id="a62b7-239">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a62b7-239">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="a62b7-240">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="a62b7-240">**Submission type**</span></span>

<span data-ttu-id="a62b7-241">Dans la zone supérieure de la page, vous pouvez entrer une  date de début, une date de fin et vous pouvez filtrer en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="a62b7-241">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="a62b7-242">Update</span><span class="sxs-lookup"><span data-stu-id="a62b7-242">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="a62b7-243">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="a62b7-243">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="a62b7-244">Dans la boîte de dialogue qui s’affiche, enregistrez le fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="a62b7-244">In the dialog that appears, save the .csv file.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="a62b7-245">Annuler les soumissions d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a62b7-245">Undo user submissions</span></span>

<span data-ttu-id="a62b7-246">Lorsqu’un utilisateur envoie un message suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler la soumission.</span><span class="sxs-lookup"><span data-stu-id="a62b7-246">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="a62b7-247">Si l’utilisateur souhaite récupérer le courrier électronique, il sera disponible pour la récupération dans les dossiers Éléments supprimés ou Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a62b7-247">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="a62b7-248">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="a62b7-248">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="a62b7-249">Si vous avez configuré la boîte aux lettres personnalisée pour intercepter les messages signalés par l’utilisateur sans les envoyer à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="a62b7-249">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="a62b7-250">Cela déplace efficacement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a62b7-250">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="a62b7-251">Sous **l’onglet Boîte** aux lettres personnalisée, sélectionnez un message dans la liste, cliquez sur le bouton **Action** et faites l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="a62b7-251">On the **Custom mailbox** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="a62b7-252">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="a62b7-252">**Report clean**</span></span>
- <span data-ttu-id="a62b7-253">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="a62b7-253">**Report phishing**</span></span>
- <span data-ttu-id="a62b7-254">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="a62b7-254">**Report malware**</span></span>
- <span data-ttu-id="a62b7-255">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="a62b7-255">**Report spam**</span></span>

![Options sur le bouton Action](../../media/user-submission-custom-mailbox-action-button.png)
