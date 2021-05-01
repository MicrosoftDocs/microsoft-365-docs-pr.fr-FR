---
title: Soumissions d'administrateur
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
description: Les administrateurs peuvent apprendre à utiliser le portail Soumissions dans le Centre de sécurité & conformité pour soumettre des messages suspects, des messages de hameçonnage suspects, du courrier indésirable et d'autres messages potentiellement dangereux, des URL et des fichiers à Microsoft pour analyse.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d0b91808aa9008f467f66b8200f2c05a120fbcd9
ms.sourcegitcommit: 794f9767aaebe13ab1aead830b214ea674289d19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52107229"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="7872a-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="7872a-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7872a-104">**Applies to**</span></span>
- [<span data-ttu-id="7872a-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="7872a-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="7872a-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="7872a-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)


<span data-ttu-id="7872a-107">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online, les administrateurs peuvent utiliser le portail Soumissions dans le Centre de sécurité & conformité pour envoyer des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="7872a-107">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="7872a-108">Lorsque vous envoyez un message électronique, vous recevez les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="7872a-108">When you submit an email message, you will get:</span></span>

1. <span data-ttu-id="7872a-109">**Vérification de l'authentification du** courrier électronique : détails sur la réussi ou l'échec de l'authentification de messagerie lors de sa livraison.</span><span class="sxs-lookup"><span data-stu-id="7872a-109">**Email authentication check**: Details on whether email authentication passed or failed when it was delivered.</span></span>
2. <span data-ttu-id="7872a-110">**Accès aux** stratégies : informations sur les stratégies qui ont autorisé ou bloqué le courrier entrant dans votre client, en remplacement de nos verdicts de filtre de service.</span><span class="sxs-lookup"><span data-stu-id="7872a-110">**Policy hits**: Information about any policies that may have allowed or blocked the incoming email into your tenant, overriding our service filter verdicts.</span></span>
3. <span data-ttu-id="7872a-111">**Réputation/détonation de la charge utile**: examen des URL et pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="7872a-111">**Payload reputation/detonation**: Examination of any URLs and attachments in the message.</span></span>
4. <span data-ttu-id="7872a-112">**Analyse du gradeur**: révision effectuée par des élèves humains afin de confirmer si les messages sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="7872a-112">**Grader analysis**: Review done by human graders in order to confirm whether or not messages are malicious.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7872a-113">L'analyse de réputation/détonation et de grader de la charge utile n'est pas effectuée dans tous les locataires.</span><span class="sxs-lookup"><span data-stu-id="7872a-113">Payload reputation/detonation and grader analysis are not done in all tenants.</span></span> <span data-ttu-id="7872a-114">Les informations ne peuvent pas sortir de l'organisation lorsque les données ne sont pas supposées quitter la limite du client à des fins de conformité.</span><span class="sxs-lookup"><span data-stu-id="7872a-114">Information is blocked from going outside the organization when data is not supposed to leave the tenant boundary for compliance purposes.</span></span>

<span data-ttu-id="7872a-115">Pour d'autres façons de soumettre des messages électroniques, des URL et des pièces jointes à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="7872a-115">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7872a-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7872a-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7872a-117">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="7872a-117">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="7872a-118">Pour aller directement à la page **soumission,** utilisez <https://protection.office.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="7872a-118">To go directly to the **Submission** page, use <https://protection.office.com/reportsubmission>.</span></span>

- <span data-ttu-id="7872a-119">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l'un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="7872a-119">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="7872a-120">**Lecteur Gestion de l'organisation** **ou Sécurité** dans le [Centre de sécurité & conformité.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="7872a-120">**Organization Management** or **Security Reader** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  - <span data-ttu-id="7872a-121">**Gestion de l'organisation** [dans Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="7872a-121">**Organization Management** in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="7872a-122">Notez que l'appartenance à ce groupe de rôles est nécessaire pour afficher les [soumissions](#view-user-submissions-to-the-custom-mailbox) d'utilisateurs à la boîte aux lettres personnalisée, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7872a-122">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this article.</span></span>

- <span data-ttu-id="7872a-123">Pour plus d'informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, voir Signaler des messages et [des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="7872a-123">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="7872a-124">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-124">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="7872a-125">Dans le Centre de sécurité &  conformité, allez à Soumissions de gestion des menaces, vérifiez que vous êtes sous \> l'onglet **Soumissions** d'administrateur, puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="7872a-125">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Admin submissions** tab, and then click **New submission**.</span></span>

2. <span data-ttu-id="7872a-126">Utilisez **le nouveau volant** de soumission qui apparaît pour envoyer le message, l'URL ou la pièce jointe, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7872a-126">Use **New submission** flyout that appears to submit the message, URL, or attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="7872a-127">Envoyer un e-mail douteux à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-127">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="7872a-128">Dans la section **Type d'objet,** sélectionnez **Courrier électronique.**</span><span class="sxs-lookup"><span data-stu-id="7872a-128">In the **Object type** section, select **Email**.</span></span> <span data-ttu-id="7872a-129">Dans la section **Format de** soumission, utilisez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-129">In the **Submission format** section, use one of the following options:</span></span>

   - <span data-ttu-id="7872a-130">**ID** de message réseau : il s'agit d'une valeur GUID disponible dans l'en-tête **X-MS-Exchange-Organization-Network-Message-Id** dans le message, ou dans l'en-tête **X-MS-Office365-Filtering-Correlation-Id** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="7872a-130">**Network Message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message, or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>

   - <span data-ttu-id="7872a-131">**Fichier**: cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="7872a-131">**File**: Click **Choose file**.</span></span> <span data-ttu-id="7872a-132">Dans la boîte de dialogue qui s'ouvre, recherchez et sélectionnez le fichier .eml ou .msg, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="7872a-132">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="7872a-133">La possibilité de soumettre des messages depuis 30 jours a été temporairement suspendue pour Defender pour Office 365 clients.</span><span class="sxs-lookup"><span data-stu-id="7872a-133">The ability to submit messages as old as 30 days has been temporarily suspended for Defender for Office 365 customers.</span></span> <span data-ttu-id="7872a-134">Les administrateurs ne pourront revenir qu'à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="7872a-134">Admins will only be able to go back 7 days.</span></span>

2. <span data-ttu-id="7872a-135">Dans la section **Destinataires,** spécifiez un ou plusieurs destinataires pour qui vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="7872a-135">In the **Recipients** section, specify one or more recipients that you would like to run a policy check against.</span></span> <span data-ttu-id="7872a-136">La vérification de stratégie détermine si le courrier électronique a contourné l'analyse en raison des stratégies utilisateur ou organisation.</span><span class="sxs-lookup"><span data-stu-id="7872a-136">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="7872a-137">Dans la section **Raison de la** soumission, sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-137">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="7872a-138">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="7872a-138">**Should not have been blocked**</span></span>

   - <span data-ttu-id="7872a-139">**Doit avoir été bloqué :** sélectionner le courrier **indésirable,** **le hameçonnage** ou les programmes **malveillants.**</span><span class="sxs-lookup"><span data-stu-id="7872a-139">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="7872a-140">Si vous n'êtes pas sûr, faites votre meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="7872a-140">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="7872a-141">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="7872a-141">When you're finished, click the **Submit** button.</span></span>

   ![Exemple de soumission d'URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="7872a-143">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-143">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="7872a-144">Dans la section **Type d'objet,** sélectionnez **URL.**</span><span class="sxs-lookup"><span data-stu-id="7872a-144">In the **Object type** section, select **URL**.</span></span> <span data-ttu-id="7872a-145">Dans la zone qui s'affiche, entrez l'URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="7872a-145">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="7872a-146">Dans la section **Raison de la** soumission, sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-146">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="7872a-147">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="7872a-147">**Should not have been blocked**</span></span>

   - <span data-ttu-id="7872a-148">**Doit avoir été bloqué :** sélectionnez **Hameçonnage** ou **Programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="7872a-148">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="7872a-149">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="7872a-149">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d'envoi de nouveaux e-mails](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-file-to-microsoft"></a><span data-ttu-id="7872a-151">Soumettre un fichier suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-151">Submit a suspected file to Microsoft</span></span>

1. <span data-ttu-id="7872a-152">Dans la section **Type d'objet,** sélectionnez **Pièce jointe.**</span><span class="sxs-lookup"><span data-stu-id="7872a-152">In the **Object type** section, select **Attachment**.</span></span>

2. <span data-ttu-id="7872a-153">Cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="7872a-153">Click **Choose File**.</span></span> <span data-ttu-id="7872a-154">Dans la boîte de dialogue qui s'ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="7872a-154">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="7872a-155">Dans la section **Raison de la** soumission, sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-155">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="7872a-156">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="7872a-156">**Should not have been blocked**</span></span>

   - <span data-ttu-id="7872a-157">**Doit avoir été bloqué :** un **programme** malveillant est le seul choix et est automatiquement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7872a-157">**Should have been blocked**: **Malware** is the only choice, and is automatically selected..</span></span>

4. <span data-ttu-id="7872a-158">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="7872a-158">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d'envoi de nouvelles pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-items-submitted-for-analysis"></a><span data-ttu-id="7872a-160">Afficher les éléments envoyés pour analyse</span><span class="sxs-lookup"><span data-stu-id="7872a-160">View items Submitted for analysis</span></span>

<span data-ttu-id="7872a-161">Dans le Centre de sécurité &  conformité, allez aux soumissions de gestion des \> **menaces,** vérifiez que vous êtes sous l'onglet Soumis **pour analyse**</span><span class="sxs-lookup"><span data-stu-id="7872a-161">In the Security & Compliance Center, go to **Threat management** \> **Submissions**, verify that you're on the **Submitted for analysis** tab</span></span>

<span data-ttu-id="7872a-162">Dans la partie supérieure de la page, vous pouvez entrer une date de début, une date de fin et (par défaut) vous pouvez filtrer par **ID** de soumission (une valeur GUID affectée à chaque soumission) en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="7872a-162">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="7872a-163">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7872a-163">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="7872a-164">Pour modifier les critères de filtre, cliquez sur le bouton **ID** de soumission et choisissez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-164">To change the filter criteria, click the **Submission ID** button and choose one of the following values:</span></span>

- <span data-ttu-id="7872a-165">**Sender**</span><span class="sxs-lookup"><span data-stu-id="7872a-165">**Sender**</span></span>
- <span data-ttu-id="7872a-166">**Objet/URL/Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="7872a-166">**Subject/URL/File name**</span></span>
- <span data-ttu-id="7872a-167">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="7872a-167">**Submitted by**</span></span>
- <span data-ttu-id="7872a-168">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-168">**Submission type**</span></span>
- <span data-ttu-id="7872a-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="7872a-169">**Status**</span></span>

![Nouvelles options de filtre pour les soumissions d'administrateur](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="7872a-171">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="7872a-171">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="7872a-172">Dans la boîte de dialogue qui s'affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="7872a-172">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="7872a-173">Sous le graphique, il y a trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe.**</span><span class="sxs-lookup"><span data-stu-id="7872a-173">Below the graph, there are three tabs: **Email** (default), **URL**, and **Attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="7872a-174">Afficher les envois de courriers électroniques d'administrateur</span><span class="sxs-lookup"><span data-stu-id="7872a-174">View admin email submissions</span></span>

<span data-ttu-id="7872a-175">Cliquez sur **l'onglet** Courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="7872a-175">Click the **Email** tab.</span></span>

<span data-ttu-id="7872a-176">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l'affichage :</span><span class="sxs-lookup"><span data-stu-id="7872a-176">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="7872a-177">**Date**</span><span class="sxs-lookup"><span data-stu-id="7872a-177">**Date**</span></span>
- <span data-ttu-id="7872a-178">**ID de soumission**: valeur GUID attribuée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="7872a-178">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="7872a-179">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-179">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-180">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-180">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-181">**Sender**</span><span class="sxs-lookup"><span data-stu-id="7872a-181">**Sender**</span></span>
- <span data-ttu-id="7872a-182">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-182">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-183">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-183">**Submission type**</span></span>
- <span data-ttu-id="7872a-184">**Raison de la remise**</span><span class="sxs-lookup"><span data-stu-id="7872a-184">**Delivery reason**</span></span>
- <span data-ttu-id="7872a-185">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-185">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="7872a-186"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s'affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="7872a-186"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

#### <a name="admin-submission-rescan-details"></a><span data-ttu-id="7872a-187">Détails de la rescan de soumission de l'administrateur</span><span class="sxs-lookup"><span data-stu-id="7872a-187">Admin submission rescan details</span></span>

<span data-ttu-id="7872a-188">Les messages envoyés dans les soumissions d'administrateur sont réassurés et les résultats sont affichés dans le volant de détails :</span><span class="sxs-lookup"><span data-stu-id="7872a-188">Messages that are submitted in admin submissions are rescanned and results shown in the details flyout:</span></span>

- <span data-ttu-id="7872a-189">En cas d’échec de l’authentification des e-mails de l’expéditeur au moment de la livraison.</span><span class="sxs-lookup"><span data-stu-id="7872a-189">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="7872a-190">Informations sur les accès à la stratégie qui auraient pu affecter ou écraser le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="7872a-190">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="7872a-191">Résultats actuels de la détonation pour savoir si les URL ou fichiers contenus dans le message étaient malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="7872a-191">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="7872a-192">Commentaires des élèves.</span><span class="sxs-lookup"><span data-stu-id="7872a-192">Feedback from graders.</span></span>

<span data-ttu-id="7872a-193">Si le programme a trouvé un remplacement, la nouvelle analyse doit se terminer après plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="7872a-193">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="7872a-194">S'il n'y a pas de problème dans l'authentification ou la remise du courrier électronique n'a pas été affecté par une substitution, les commentaires des élèves peuvent prendre jusqu'à un jour.</span><span class="sxs-lookup"><span data-stu-id="7872a-194">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="7872a-195">Afficher les soumissions d'URL d'administration</span><span class="sxs-lookup"><span data-stu-id="7872a-195">View admin URL submissions</span></span>

<span data-ttu-id="7872a-196">Cliquez sur **l'onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="7872a-196">Click the **URL** tab.</span></span>

<span data-ttu-id="7872a-197">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l'affichage :</span><span class="sxs-lookup"><span data-stu-id="7872a-197">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="7872a-198">**Date**</span><span class="sxs-lookup"><span data-stu-id="7872a-198">**Date**</span></span>
- <span data-ttu-id="7872a-199">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-199">**Submission ID**</span></span>
- <span data-ttu-id="7872a-200">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-200">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-201">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-201">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-202">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-202">**Submission type**</span></span>
- <span data-ttu-id="7872a-203">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-203">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="7872a-204"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s'affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="7872a-204"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-admin-attachment-submissions"></a><span data-ttu-id="7872a-205">Afficher les soumissions de pièces jointes d'administrateur</span><span class="sxs-lookup"><span data-stu-id="7872a-205">View admin attachment submissions</span></span>

<span data-ttu-id="7872a-206">Cliquez sur **l'onglet Pièces jointes.**</span><span class="sxs-lookup"><span data-stu-id="7872a-206">Click the **Attachments** tab.</span></span>

<span data-ttu-id="7872a-207">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l'affichage :</span><span class="sxs-lookup"><span data-stu-id="7872a-207">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="7872a-208">**Date**</span><span class="sxs-lookup"><span data-stu-id="7872a-208">**Date**</span></span>
- <span data-ttu-id="7872a-209">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-209">**Submission ID**</span></span>
- <span data-ttu-id="7872a-210">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-210">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-211">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-211">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-212">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-212">**Submission type**</span></span>
- <span data-ttu-id="7872a-213">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-213">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="7872a-214"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s'affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="7872a-214"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="7872a-215">Afficher les soumissions d'utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="7872a-215">View user submissions to Microsoft</span></span>

<span data-ttu-id="7872a-216">Si vous avez déployé le [add-in](enable-the-report-message-add-in.md) [](enable-the-report-phish-add-in.md)Signaler un message, le module de signalement du hameçonnage ou que des personnes utilisent les rapports intégrés dans Outlook sur [le web,](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)vous pouvez voir ce que les utilisateurs signalent sous l'onglet Soumissions des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="7872a-216">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), the [Report Phishing add-in](enable-the-report-phish-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="7872a-217">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="7872a-217">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="7872a-218">Sélectionnez **l'onglet Soumissions utilisateur,** puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="7872a-218">Select the **User submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="7872a-219">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l'affichage :</span><span class="sxs-lookup"><span data-stu-id="7872a-219">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="7872a-220">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="7872a-220">**Submitted on**</span></span>
- <span data-ttu-id="7872a-221">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-221">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-222">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-222">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-223">**Sender**</span><span class="sxs-lookup"><span data-stu-id="7872a-223">**Sender**</span></span>
- <span data-ttu-id="7872a-224">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-224">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-225">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-225">**Submission type**</span></span>

<span data-ttu-id="7872a-226"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s'affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="7872a-226"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="7872a-227">Dans la zone supérieure de la page, vous pouvez entrer une date de  début, une date de fin et (par défaut) vous pouvez filtrer par expéditeur en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="7872a-227">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="7872a-228">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7872a-228">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="7872a-229">Pour modifier les critères de filtre, cliquez sur le bouton **Expéditeur** et choisissez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-229">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="7872a-230">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="7872a-230">**Sender domain**</span></span>
- <span data-ttu-id="7872a-231">**Subject**</span><span class="sxs-lookup"><span data-stu-id="7872a-231">**Subject**</span></span>
- <span data-ttu-id="7872a-232">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="7872a-232">**Submitted by**</span></span>
- <span data-ttu-id="7872a-233">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-233">**Submission type**</span></span>
- <span data-ttu-id="7872a-234">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="7872a-234">**Sender IP**</span></span>

![Nouvelles options de filtre pour les soumissions d'utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="7872a-236">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="7872a-236">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="7872a-237">Dans la boîte de dialogue qui s'affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="7872a-237">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="7872a-238">Afficher les envois d'utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="7872a-238">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="7872a-239">**Si** vous avez configuré [une](user-submission.md) boîte aux lettres personnalisée pour recevoir les messages signalés par l'utilisateur, vous pouvez afficher et envoyer des messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="7872a-239">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="7872a-240">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="7872a-240">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="7872a-241">Sélectionnez **l'onglet Boîte aux lettres** personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7872a-241">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="7872a-242">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l'affichage :</span><span class="sxs-lookup"><span data-stu-id="7872a-242">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="7872a-243">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="7872a-243">**Submitted on**</span></span>
- <span data-ttu-id="7872a-244">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-244">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-245">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-245">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-246">**Sender**</span><span class="sxs-lookup"><span data-stu-id="7872a-246">**Sender**</span></span>
- <span data-ttu-id="7872a-247">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7872a-247">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="7872a-248">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="7872a-248">**Submission type**</span></span>

<span data-ttu-id="7872a-249">Dans la zone supérieure de la page, vous pouvez entrer une  date de début, une date de fin et vous pouvez filtrer en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="7872a-249">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="7872a-250">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7872a-250">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="7872a-251">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="7872a-251">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="7872a-252">Dans la boîte de dialogue qui s'affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="7872a-252">In the dialog that appears, save the .csv file.</span></span>

> [!NOTE]
> <span data-ttu-id="7872a-253">Si les organisations sont configurées pour envoyer des messages à une boîte aux lettres personnalisée uniquement, les messages signalés ne seront pas envoyés pour réascaner et les résultats dans le portail Des messages signalés par l'utilisateur seront toujours vides.</span><span class="sxs-lookup"><span data-stu-id="7872a-253">If organizations are configured to send to custom mailbox only, reported messages will not be sent for rescan and results in the User reported messages portal will always be empty.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="7872a-254">Annuler les soumissions d'utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7872a-254">Undo user submissions</span></span>

<span data-ttu-id="7872a-255">Lorsqu'un utilisateur envoie un message suspect à la boîte aux lettres personnalisée, l'utilisateur et l'administrateur n'ont pas la possibilité d'annuler la soumission.</span><span class="sxs-lookup"><span data-stu-id="7872a-255">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="7872a-256">Si l'utilisateur souhaite récupérer le courrier électronique, il pourra être récupéré dans les dossiers Éléments supprimés ou Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7872a-256">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="7872a-257">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="7872a-257">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="7872a-258">Si vous avez configuré la boîte aux lettres personnalisée pour intercepter les messages signalés par l'utilisateur sans les envoyer à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="7872a-258">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="7872a-259">Cela déplace efficacement une soumission d'utilisateur vers une soumission d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="7872a-259">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="7872a-260">Sous **l'onglet Messages signalés** par l'utilisateur, sélectionnez un message dans la liste, cliquez sur le bouton **Action** et sélectionnez l'une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="7872a-260">On the **User reported messages** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="7872a-261">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="7872a-261">**Report clean**</span></span>
- <span data-ttu-id="7872a-262">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="7872a-262">**Report phishing**</span></span>
- <span data-ttu-id="7872a-263">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="7872a-263">**Report malware**</span></span>
- <span data-ttu-id="7872a-264">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="7872a-264">**Report spam**</span></span>

![Nouvelles options sur le bouton Action](../../media/user-submission-custom-mailbox-action-button.png)
