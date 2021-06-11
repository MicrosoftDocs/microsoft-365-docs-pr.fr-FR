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
description: Les administrateurs peuvent apprendre à utiliser le portail Soumissions dans le Centre de sécurité Microsoft 365 pour soumettre à Microsoft des messages suspects, des messages de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement dangereux, des URL et des pièces jointes de courrier électronique à Microsoft pour une rescannation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6de6a018a96407a5690249bea15e90c2f5a0d1ed
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52878687"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="3eac7-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="3eac7-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3eac7-104">**Applies to**</span></span>
- [<span data-ttu-id="3eac7-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="3eac7-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="3eac7-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="3eac7-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)


<span data-ttu-id="3eac7-107">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online, les administrateurs peuvent utiliser le portail Soumissions dans le Centre de sécurité & conformité pour envoyer des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="3eac7-107">In Microsoft 365 organizations with mailboxes in Exchange Online, admins can use the Submissions portal in the Security & Compliance Center to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="3eac7-108">Lorsque vous envoyez un message électronique, vous recevez les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="3eac7-108">When you submit an email message, you will get:</span></span>

1. <span data-ttu-id="3eac7-109">**Vérification de l’authentification du** courrier électronique : détails sur la réussi ou l’échec de l’authentification de messagerie lors de sa livraison.</span><span class="sxs-lookup"><span data-stu-id="3eac7-109">**Email authentication check**: Details on whether email authentication passed or failed when it was delivered.</span></span>
2. <span data-ttu-id="3eac7-110">**Accès aux** stratégies : informations sur les stratégies qui ont autorisé ou bloqué le courrier entrant dans votre client, en remplacement de nos verdicts de filtre de service.</span><span class="sxs-lookup"><span data-stu-id="3eac7-110">**Policy hits**: Information about any policies that may have allowed or blocked the incoming email into your tenant, overriding our service filter verdicts.</span></span>
3. <span data-ttu-id="3eac7-111">**Réputation/détonation de la charge utile**: examen des URL et pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="3eac7-111">**Payload reputation/detonation**: Examination of any URLs and attachments in the message.</span></span>
4. <span data-ttu-id="3eac7-112">**Analyse du gradeur**: révision effectuée par des élèves humains afin de confirmer si les messages sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="3eac7-112">**Grader analysis**: Review done by human graders in order to confirm whether or not messages are malicious.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3eac7-113">L’analyse de réputation/détonation et de grader de la charge utile n’est pas effectuée dans tous les locataires.</span><span class="sxs-lookup"><span data-stu-id="3eac7-113">Payload reputation/detonation and grader analysis are not done in all tenants.</span></span> <span data-ttu-id="3eac7-114">Les informations ne peuvent pas sortir de l’organisation lorsque les données ne sont pas supposées quitter la limite du client à des fins de conformité.</span><span class="sxs-lookup"><span data-stu-id="3eac7-114">Information is blocked from going outside the organization when data is not supposed to leave the tenant boundary for compliance purposes.</span></span>

<span data-ttu-id="3eac7-115">Pour d’autres façons de soumettre des messages électroniques, des URL et des pièces jointes à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="3eac7-115">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="3eac7-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3eac7-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="3eac7-117">Vous ouvrez le centre Microsoft 365 sécurité sur <https://security.microsoft.com/> .</span><span class="sxs-lookup"><span data-stu-id="3eac7-117">You open the Microsoft 365 security center at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="3eac7-118">Pour aller directement à la page **Soumissions,** utilisez <https://security.microsoft.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="3eac7-118">To go directly to the **Submissions** page, use <https://security.microsoft.com/reportsubmission>.</span></span>

- <span data-ttu-id="3eac7-119">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="3eac7-119">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="3eac7-120">**Lecteur Gestion de l’organisation** **ou Sécurité** dans [le centre Microsoft 365 sécurité.](permissions-microsoft-365-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="3eac7-120">**Organization Management** or **Security Reader** in the [Microsoft 365 security center](permissions-microsoft-365-security-center.md).</span></span>

  - <span data-ttu-id="3eac7-121">**Gestion de l’organisation** [dans Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="3eac7-121">**Organization Management** in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="3eac7-122">Notez que l’appartenance à ce groupe de rôles est nécessaire pour afficher les [soumissions](#view-user-submissions-to-the-custom-mailbox) d’utilisateurs à la boîte aux lettres personnalisée, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3eac7-122">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-the-custom-mailbox) as described later in this article.</span></span>

- <span data-ttu-id="3eac7-123">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, voir Signaler des messages et [des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="3eac7-123">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="3eac7-124">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-124">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="3eac7-125">Dans le centre [Microsoft 365](../defender/overview-security-center.md)de sécurité, allez à **Soumissions**  et vérifiez que vous êtes sous l’onglet Soumis pour analyse, puis cliquez sur Envoyer à Microsoft pour **révision.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-125">In the [Microsoft 365 security center](../defender/overview-security-center.md), go to **Submissions** and verify that you're on the **Submitted for analysis** tab, and then click **Submit to Microsoft for review**.</span></span>

2. <span data-ttu-id="3eac7-126">Utilisez le **volant Envoyer à Microsoft** pour révision qui apparaît pour envoyer le message, l’URL ou la pièce jointe d’un e-mail, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3eac7-126">Use the **Submit to Microsoft for review** flyout that appears to submit the message, URL, or email attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="3eac7-127">Envoyer un e-mail douteux à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-127">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="3eac7-128">Dans la section **Sélectionner le type de** soumission, sélectionnez Courrier **électronique.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-128">In the **Select the submission type** section, select **Email**.</span></span> <span data-ttu-id="3eac7-129">Dans la section **Ajouter l’ID de message** réseau ou télécharger le fichier de courrier électronique, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-129">In the **Add the network message ID or upload the email file** section, use one of the following options:</span></span>

   - <span data-ttu-id="3eac7-130">Ajoutez **l’ID** du message réseau de messagerie : il s’agit d’une valeur GUID disponible dans l’en-tête **X-MS-Exchange-Organization-Network-Message-Id** dans le message ou dans l’en-tête **X-MS-Office365-Filtering-Correlation-Id** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="3eac7-130">**Add the email network message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>

   - <span data-ttu-id="3eac7-131">**Télécharger fichier de courrier électronique :** cliquez sur Parcourir les **fichiers.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-131">**Upload the email file**: Click **Browse files**.</span></span> <span data-ttu-id="3eac7-132">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier .eml ou .msg, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="3eac7-132">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3eac7-133">La possibilité de soumettre des messages depuis 30 jours a été temporairement suspendue pour Defender pour Office 365 clients.</span><span class="sxs-lookup"><span data-stu-id="3eac7-133">The ability to submit messages as old as 30 days has been temporarily suspended for Defender for Office 365 customers.</span></span> <span data-ttu-id="3eac7-134">Les administrateurs ne pourront revenir qu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="3eac7-134">Admins will only be able to go back 7 days.</span></span>

2. <span data-ttu-id="3eac7-135">Dans la section **Choisir un destinataire qui a eu un problème,** spécifiez le destinataire sur qui vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="3eac7-135">In the **Choose a recipient who had an issue** section, specify the recipient that you would like to run a policy check against.</span></span> <span data-ttu-id="3eac7-136">La vérification de stratégie détermine si le courrier électronique a contourné l’analyse en raison des stratégies utilisateur ou organisation.</span><span class="sxs-lookup"><span data-stu-id="3eac7-136">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

3. <span data-ttu-id="3eac7-137">Dans la section **Sélectionner une raison d’envoyer à Microsoft,** sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-137">In the **Select a reason for submitting to Microsoft** section, select one of the following options:</span></span>

   - <span data-ttu-id="3eac7-138">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="3eac7-138">**Should not have been blocked**</span></span>

   - <span data-ttu-id="3eac7-139">**Doit avoir été bloqué :** sélectionner le courrier **indésirable,** **le hameçonnage** ou les programmes **malveillants.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-139">**Should have been blocked**: Select **Spam**, **Phishing**, or **Malware**.</span></span> <span data-ttu-id="3eac7-140">Si vous n’êtes pas sûr, faites votre meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="3eac7-140">If you're not sure, use your best judgment.</span></span>

4. <span data-ttu-id="3eac7-141">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="3eac7-141">When you're finished, click the **Submit** button.</span></span>

   ![Exemple de soumission d’URL](../../media/submission-flyout-email.PNG)

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="3eac7-143">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-143">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="3eac7-144">Dans la section **Sélectionner le type de** soumission, sélectionnez **URL.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-144">In the **Select the submission type** section, select **URL**.</span></span> <span data-ttu-id="3eac7-145">Dans la zone qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="3eac7-145">In the box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

2. <span data-ttu-id="3eac7-146">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-146">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="3eac7-147">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="3eac7-147">**Should not have been blocked**</span></span>

   - <span data-ttu-id="3eac7-148">**Doit avoir été bloqué :** sélectionnez **Hameçonnage** ou **Programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-148">**Should have been blocked**: Select **Phishing** or **Malware**.</span></span>

3. <span data-ttu-id="3eac7-149">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="3eac7-149">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d’envoi de nouveaux e-mails](../../media/submission-url-flyout.png)

### <a name="submit-a-suspected-email-attachment-to-microsoft"></a><span data-ttu-id="3eac7-151">Envoyer une pièce jointe suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-151">Submit a suspected email attachment to Microsoft</span></span>

1. <span data-ttu-id="3eac7-152">Dans la section **Sélectionner le type de** soumission, sélectionnez Pièce **jointe.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-152">In the **Select the submission type** section, select **Email attachment**.</span></span>

2. <span data-ttu-id="3eac7-153">Cliquez **sur Choisir un fichier.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-153">Click **Choose File**.</span></span> <span data-ttu-id="3eac7-154">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-154">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="3eac7-155">Dans la section **Raison de la** soumission, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-155">In the **Reason for submission** section, select one of the following options:</span></span>

   - <span data-ttu-id="3eac7-156">**Ne doit pas avoir été bloqué**</span><span class="sxs-lookup"><span data-stu-id="3eac7-156">**Should not have been blocked**</span></span>

   - <span data-ttu-id="3eac7-157">**Doit avoir été bloqué :** un **programme** malveillant est le seul choix et est automatiquement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3eac7-157">**Should have been blocked**: **Malware** is the only choice, and is automatically selected.</span></span>

4. <span data-ttu-id="3eac7-158">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="3eac7-158">When you're finished, click the **Submit** button.</span></span>

   ![Exemple d’envoi de nouvelles pièces jointes](../../media/submission-file-flyout.PNG)

## <a name="view-items-submitted-for-analysis"></a><span data-ttu-id="3eac7-160">Afficher les éléments envoyés pour analyse</span><span class="sxs-lookup"><span data-stu-id="3eac7-160">View items Submitted for analysis</span></span>

<span data-ttu-id="3eac7-161">Dans le centre Microsoft 365 de sécurité, allez à **Soumissions** et vérifiez que vous êtes sous l’onglet Soumis **pour** analyse</span><span class="sxs-lookup"><span data-stu-id="3eac7-161">In the Microsoft 365 security center, go to **Submissions**, and verify that you're on the **Submitted for analysis** tab</span></span>

<span data-ttu-id="3eac7-162">Dans la barre de commandes au milieu de la page, vous pouvez entrer une date de début, une date de fin et (par défaut) vous pouvez filtrer par **ID** de soumission (une valeur GUID affectée à chaque soumission) en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="3eac7-162">In the command bar in the middle of the page, you can enter a start date, an end date, and (by default) you can filter by **Submission ID** (a GUID value that's assigned to every submission) by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="3eac7-163">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3eac7-163">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="3eac7-164">Pour modifier les critères de filtre, cliquez sur le bouton **Filtrer** et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-164">To change the filter criteria, click the **Filter** button and choose one of the following values:</span></span>

- <span data-ttu-id="3eac7-165">**Sender**</span><span class="sxs-lookup"><span data-stu-id="3eac7-165">**Sender**</span></span>
- <span data-ttu-id="3eac7-166">**Objet/URL/Nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="3eac7-166">**Subject/URL/File name**</span></span>
- <span data-ttu-id="3eac7-167">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="3eac7-167">**Submitted by**</span></span>
- <span data-ttu-id="3eac7-168">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-168">**Submission type**</span></span>
- <span data-ttu-id="3eac7-169">**État**</span><span class="sxs-lookup"><span data-stu-id="3eac7-169">**Status**</span></span>

![Nouvelles options de filtre pour les soumissions d’administrateurs](../../media/admin-submission-email-filter-options.png)

<span data-ttu-id="3eac7-171">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-171">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="3eac7-172">Dans la boîte de dialogue qui s’affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="3eac7-172">In the dialog that appears, save the .csv file.</span></span>

<span data-ttu-id="3eac7-173">Sous le graphique, il y a trois onglets : **e-mail** (par défaut), **URL** et **pièce jointe de l’e-mail.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-173">Below the graph, there are three tabs: **Email** (default), **URL**, and **Email attachment**.</span></span>

### <a name="view-admin-email-submissions"></a><span data-ttu-id="3eac7-174">Afficher les envois de courriers électroniques d’administrateur</span><span class="sxs-lookup"><span data-stu-id="3eac7-174">View admin email submissions</span></span>

<span data-ttu-id="3eac7-175">Vous pouvez cliquer sur le bouton Personnaliser **les** colonnes en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="3eac7-175">You can click the **Customize columns** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="3eac7-176">**Date**</span><span class="sxs-lookup"><span data-stu-id="3eac7-176">**Date**</span></span>
- <span data-ttu-id="3eac7-177">**ID de soumission**: valeur GUID attribuée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="3eac7-177">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
- <span data-ttu-id="3eac7-178">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-178">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-179">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-179">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-180">**Sender**</span><span class="sxs-lookup"><span data-stu-id="3eac7-180">**Sender**</span></span>
- <span data-ttu-id="3eac7-181">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-181">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-182">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-182">**Submission type**</span></span>
- <span data-ttu-id="3eac7-183">**Raison de la remise**</span><span class="sxs-lookup"><span data-stu-id="3eac7-183">**Delivery reason**</span></span>
- <span data-ttu-id="3eac7-184">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-184">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="3eac7-185"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="3eac7-185"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

#### <a name="admin-submission-rescan-details"></a><span data-ttu-id="3eac7-186">Détails de la rescan de soumission de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="3eac7-186">Admin submission rescan details</span></span>

<span data-ttu-id="3eac7-187">Les messages envoyés dans les soumissions d’administrateur sont réassurés et les résultats sont affichés dans le flyout détaillé des soumissions :</span><span class="sxs-lookup"><span data-stu-id="3eac7-187">Messages that are submitted in admin submissions are rescanned and results shown in the submissions detail flyout:</span></span>

- <span data-ttu-id="3eac7-188">En cas d’échec de l’authentification des e-mails de l’expéditeur au moment de la livraison.</span><span class="sxs-lookup"><span data-stu-id="3eac7-188">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="3eac7-189">Informations sur les accès à la stratégie qui auraient pu affecter ou écraser le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="3eac7-189">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="3eac7-190">Résultats actuels de la détonation pour savoir si les URL ou fichiers contenus dans le message étaient malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="3eac7-190">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="3eac7-191">Commentaires des élèves.</span><span class="sxs-lookup"><span data-stu-id="3eac7-191">Feedback from graders.</span></span>

<span data-ttu-id="3eac7-192">Si le programme a trouvé un remplacement, la nouvelle analyse doit se terminer après plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="3eac7-192">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="3eac7-193">S’il n’y a pas de problème dans l’authentification ou la remise du courrier électronique n’a pas été affecté par une substitution, les commentaires des élèves peuvent prendre jusqu’à un jour.</span><span class="sxs-lookup"><span data-stu-id="3eac7-193">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

### <a name="view-admin-url-submissions"></a><span data-ttu-id="3eac7-194">Afficher les soumissions d’URL d’administration</span><span class="sxs-lookup"><span data-stu-id="3eac7-194">View admin URL submissions</span></span>

<span data-ttu-id="3eac7-195">Cliquez sur **l’onglet URL.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-195">Click the **URL** tab.</span></span>

<span data-ttu-id="3eac7-196">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="3eac7-196">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="3eac7-197">**Date**</span><span class="sxs-lookup"><span data-stu-id="3eac7-197">**Date**</span></span>
- <span data-ttu-id="3eac7-198">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-198">**Submission ID**</span></span>
- <span data-ttu-id="3eac7-199">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-199">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-200">**URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-200">**URL**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-201">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-201">**Submission type**</span></span>
- <span data-ttu-id="3eac7-202">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-202">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="3eac7-203"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="3eac7-203"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

### <a name="view-email-attachment-submissions"></a><span data-ttu-id="3eac7-204">Afficher les envois de pièces jointes par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="3eac7-204">View email attachment submissions</span></span>

<span data-ttu-id="3eac7-205">Cliquez sur **l’onglet Pièces jointes.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-205">Click the **Attachments** tab.</span></span>

<span data-ttu-id="3eac7-206">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="3eac7-206">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="3eac7-207">**Date**</span><span class="sxs-lookup"><span data-stu-id="3eac7-207">**Date**</span></span>
- <span data-ttu-id="3eac7-208">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-208">**Submission ID**</span></span>
- <span data-ttu-id="3eac7-209">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-209">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-210">**Nom de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-210">**File name**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-211">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-211">**Submission type**</span></span>
- <span data-ttu-id="3eac7-212">**État**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-212">**Status**<sup>\*</sup></span></span>

  <span data-ttu-id="3eac7-213"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="3eac7-213"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="3eac7-214">Afficher les soumissions d’utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eac7-214">View user submissions to Microsoft</span></span>

<span data-ttu-id="3eac7-215">Si vous avez déployé le [add-in](enable-the-report-message-add-in.md) [](enable-the-report-phish-add-in.md)Signaler un message, le module de signalement du hameçonnage ou que des personnes utilisent les rapports intégrés dans Outlook sur [le web,](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)vous pouvez voir ce que les utilisateurs signalent sous l’onglet Soumissions des **utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-215">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), the [Report Phishing add-in](enable-the-report-phish-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User submissions** tab.</span></span>

1. <span data-ttu-id="3eac7-216">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-216">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="3eac7-217">Sélectionnez **l’onglet Soumissions utilisateur,** puis cliquez sur **Nouvelle soumission.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-217">Select the **User submissions** tab, and then click **New submission**.</span></span>

<span data-ttu-id="3eac7-218">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="3eac7-218">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="3eac7-219">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="3eac7-219">**Submitted on**</span></span>
- <span data-ttu-id="3eac7-220">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-220">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-221">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-221">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-222">**Sender**</span><span class="sxs-lookup"><span data-stu-id="3eac7-222">**Sender**</span></span>
- <span data-ttu-id="3eac7-223">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-223">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-224">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-224">**Submission type**</span></span>

<span data-ttu-id="3eac7-225"><sup>\*</sup> Si vous cliquez sur cette valeur, des informations détaillées s’affichent dans un volant.</span><span class="sxs-lookup"><span data-stu-id="3eac7-225"><sup>\*</sup> If you click this value, detailed information is displayed in a flyout.</span></span>

<span data-ttu-id="3eac7-226">Dans la zone supérieure de la page, vous pouvez entrer une date de  début, une date de fin et (par défaut) vous pouvez filtrer par expéditeur en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="3eac7-226">Near the top of the page, you can enter a start date, an end date, and (by default) you can filter by **Sender** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="3eac7-227">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3eac7-227">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="3eac7-228">Pour modifier les critères de filtre, cliquez sur le bouton **Expéditeur** et choisissez l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-228">To change the filter criteria, click the **Sender** button and choose one of the following values:</span></span>

- <span data-ttu-id="3eac7-229">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="3eac7-229">**Sender domain**</span></span>
- <span data-ttu-id="3eac7-230">**Subject**</span><span class="sxs-lookup"><span data-stu-id="3eac7-230">**Subject**</span></span>
- <span data-ttu-id="3eac7-231">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="3eac7-231">**Submitted by**</span></span>
- <span data-ttu-id="3eac7-232">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-232">**Submission type**</span></span>
- <span data-ttu-id="3eac7-233">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="3eac7-233">**Sender IP**</span></span>

![Nouvelles options de filtre pour les envois d’utilisateurs](../../media/user-submissions-filter-options.png)

<span data-ttu-id="3eac7-235">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-235">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="3eac7-236">Dans la boîte de dialogue qui s’affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="3eac7-236">In the dialog that appears, save the .csv file.</span></span>

## <a name="view-user-submissions-to-the-custom-mailbox"></a><span data-ttu-id="3eac7-237">Afficher les envois d’utilisateurs à la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="3eac7-237">View user submissions to the custom mailbox</span></span>

<span data-ttu-id="3eac7-238">**Si** vous avez configuré [une](user-submission.md) boîte aux lettres personnalisée pour recevoir les messages signalés par l’utilisateur, vous pouvez afficher et envoyer des messages qui ont été remis à la boîte aux lettres de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="3eac7-238">**If** you've [configured a custom mailbox](user-submission.md) to receive user reported messages, you can view and also submit messages that were delivered to the reporting mailbox.</span></span>

1. <span data-ttu-id="3eac7-239">Dans le Centre de sécurité & conformité, allez aux soumissions **de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-239">In the Security & Compliance Center, go to **Threat management** \> **Submissions**.</span></span>

2. <span data-ttu-id="3eac7-240">Sélectionnez **l’onglet Boîte aux lettres** personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3eac7-240">Select the **Custom mailbox** tab.</span></span>

<span data-ttu-id="3eac7-241">Vous pouvez cliquer sur le **bouton Options** de colonne en bas de la page pour ajouter ou supprimer des colonnes de l’affichage :</span><span class="sxs-lookup"><span data-stu-id="3eac7-241">You can click the **Column options** button near the bottom of the page to add or remove columns from the view:</span></span>

- <span data-ttu-id="3eac7-242">**Envoyé le**</span><span class="sxs-lookup"><span data-stu-id="3eac7-242">**Submitted on**</span></span>
- <span data-ttu-id="3eac7-243">**Soumis par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-243">**Submitted by**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-244">**Sujet**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-244">**Subject**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-245">**Sender**</span><span class="sxs-lookup"><span data-stu-id="3eac7-245">**Sender**</span></span>
- <span data-ttu-id="3eac7-246">**IP de l’expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="3eac7-246">**Sender IP**<sup>\*</sup></span></span>
- <span data-ttu-id="3eac7-247">**Type de soumission**</span><span class="sxs-lookup"><span data-stu-id="3eac7-247">**Submission type**</span></span>

<span data-ttu-id="3eac7-248">Dans la zone supérieure de la page, vous pouvez entrer une  date de début, une date de fin et vous pouvez filtrer en entrant une valeur dans la zone et en cliquant sur le bouton ![ ](../../media/scc-quarantine-refresh.png) Actualiser.</span><span class="sxs-lookup"><span data-stu-id="3eac7-248">Near the top of the page, you can enter a start date, an end date, and you can filter by **Submitted by** by entering a value in the box and clicking ![Refresh button](../../media/scc-quarantine-refresh.png).</span></span> <span data-ttu-id="3eac7-249">Vous pouvez entrer plusieurs valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3eac7-249">You can enter multiple values separated by commas.</span></span>

<span data-ttu-id="3eac7-250">Pour exporter les résultats, cliquez sur **Exporter** en haut de la page et sélectionnez **Données du graphique** ou **Tableau.**</span><span class="sxs-lookup"><span data-stu-id="3eac7-250">To export the results, click **Export** near the top of the page and select **Chart data** or **Table**.</span></span> <span data-ttu-id="3eac7-251">Dans la boîte de dialogue qui s’affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="3eac7-251">In the dialog that appears, save the .csv file.</span></span>

> [!NOTE]
> <span data-ttu-id="3eac7-252">Si les organisations sont configurées pour envoyer des messages à une boîte aux lettres personnalisée uniquement, les messages signalés ne seront pas envoyés pour réascaner et les résultats dans le portail Des messages signalés par l’utilisateur seront toujours vides.</span><span class="sxs-lookup"><span data-stu-id="3eac7-252">If organizations are configured to send to custom mailbox only, reported messages will not be sent for rescan and results in the User reported messages portal will always be empty.</span></span>

## <a name="undo-user-submissions"></a><span data-ttu-id="3eac7-253">Annuler les soumissions d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="3eac7-253">Undo user submissions</span></span>

<span data-ttu-id="3eac7-254">Lorsqu’un utilisateur envoie un message suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler la soumission.</span><span class="sxs-lookup"><span data-stu-id="3eac7-254">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="3eac7-255">Si l’utilisateur souhaite récupérer le courrier électronique, il pourra être récupéré dans les dossiers Éléments supprimés ou Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="3eac7-255">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="3eac7-256">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="3eac7-256">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="3eac7-257">Si vous avez configuré la boîte aux lettres personnalisée pour intercepter les messages signalés par l’utilisateur sans les envoyer à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="3eac7-257">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="3eac7-258">Cela déplace efficacement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="3eac7-258">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="3eac7-259">Sous **l’onglet Messages signalés** par l’utilisateur, sélectionnez un message dans la liste, cliquez sur le bouton **Action** et faites l’une des sélections suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eac7-259">On the **User reported messages** tab, select a message in the list, click the **Action** button, and make one of the following selections:</span></span>

- <span data-ttu-id="3eac7-260">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="3eac7-260">**Report clean**</span></span>
- <span data-ttu-id="3eac7-261">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="3eac7-261">**Report phishing**</span></span>
- <span data-ttu-id="3eac7-262">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="3eac7-262">**Report malware**</span></span>
- <span data-ttu-id="3eac7-263">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="3eac7-263">**Report spam**</span></span>

![Nouvelles options sur le bouton Action](../../media/user-submission-custom-mailbox-action-button.png)
