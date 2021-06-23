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
description: Les administrateurs peuvent apprendre à utiliser le portail Soumissions dans le portail Microsoft 365 Defender pour soumettre à Microsoft des messages suspects, des messages de hameçonnage suspects, du courrier indésirable et d’autres messages potentiellement dangereux, des URL et des pièces jointes de courrier électronique à Microsoft pour la réessuration.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ab25757c79b7978400e98fa36d48163e1681e7c1
ms.sourcegitcommit: d34cac68537d6e1c65be757956646e73dea6e1ab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53061999"
---
# <a name="use-admin-submission-to-submit-suspected-spam-phish-urls-and-files-to-microsoft"></a><span data-ttu-id="58a43-103">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-103">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="58a43-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="58a43-104">**Applies to**</span></span>
- [<span data-ttu-id="58a43-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="58a43-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="58a43-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="58a43-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)


<span data-ttu-id="58a43-107">Dans Microsoft 365 organisations ayant des boîtes aux lettres Exchange Online, les administrateurs peuvent utiliser le portail Soumissions dans le portail Microsoft 365 Defender pour envoyer des messages électroniques, des URL et des pièces jointes à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="58a43-107">In Microsoft 365 organizations with Exchange Online mailboxes, admins can use the Submissions portal in the Microsoft 365 Defender portal to submit email messages, URLs, and attachments to Microsoft for scanning.</span></span>

<span data-ttu-id="58a43-108">Lorsque vous envoyez un message électronique, vous recevez les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="58a43-108">When you submit an email message, you will get:</span></span>

- <span data-ttu-id="58a43-109">**Vérification de l’authentification du** courrier électronique : détails sur la réussi ou l’échec de l’authentification de messagerie lors de sa livraison.</span><span class="sxs-lookup"><span data-stu-id="58a43-109">**Email authentication check**: Details on whether email authentication passed or failed when it was delivered.</span></span>
- <span data-ttu-id="58a43-110">**Accès aux** stratégies : informations sur les stratégies qui ont autorisé ou bloqué le courrier entrant dans votre client, en remplacement de nos verdicts de filtre de service.</span><span class="sxs-lookup"><span data-stu-id="58a43-110">**Policy hits**: Information about any policies that may have allowed or blocked the incoming email into your tenant, overriding our service filter verdicts.</span></span>
- <span data-ttu-id="58a43-111">**Réputation/détonation de la charge utile**: examen des URL et pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="58a43-111">**Payload reputation/detonation**: Examination of any URLs and attachments in the message.</span></span>
- <span data-ttu-id="58a43-112">**Analyse du gradeur**: révision effectuée par des élèves humains afin de confirmer si les messages sont malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="58a43-112">**Grader analysis**: Review done by human graders in order to confirm whether or not messages are malicious.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58a43-113">L’analyse de réputation/détonation et de grader de la charge utile n’est pas effectuée dans tous les locataires.</span><span class="sxs-lookup"><span data-stu-id="58a43-113">Payload reputation/detonation and grader analysis are not done in all tenants.</span></span> <span data-ttu-id="58a43-114">Les informations ne peuvent pas sortir de l’organisation lorsque les données ne sont pas supposées quitter la limite du client à des fins de conformité.</span><span class="sxs-lookup"><span data-stu-id="58a43-114">Information is blocked from going outside the organization when data is not supposed to leave the tenant boundary for compliance purposes.</span></span>

<span data-ttu-id="58a43-115">Pour d’autres façons de soumettre des messages électroniques, des URL et des pièces jointes à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="58a43-115">For other ways to submit email messages, URLs, and attachments to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="58a43-116">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="58a43-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="58a43-117">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="58a43-117">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="58a43-118">Pour aller directement à la page **Soumissions,** utilisez <https://security.microsoft.com/reportsubmission> .</span><span class="sxs-lookup"><span data-stu-id="58a43-118">To go directly to the **Submissions** page, use <https://security.microsoft.com/reportsubmission>.</span></span>

- <span data-ttu-id="58a43-119">Pour envoyer des messages et des fichiers à Microsoft, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="58a43-119">To submit messages and files to Microsoft, you need to be a member of one of the following role groups:</span></span>
  - <span data-ttu-id="58a43-120">**Lecteur Gestion de l’organisation** **ou Sécurité** dans [le portail Microsoft 365 Defender.](permissions-microsoft-365-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="58a43-120">**Organization Management** or **Security Reader** in the [Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>
  - <span data-ttu-id="58a43-121">**Gestion de l’organisation** [dans Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="58a43-121">**Organization Management** in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

    <span data-ttu-id="58a43-122">Notez que l’appartenance à ce groupe de rôles est nécessaire pour afficher les [soumissions](#view-user-submissions-to-microsoft) d’utilisateurs à la boîte aux lettres personnalisée, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="58a43-122">Note that membership in this role group is required to [View user submissions to the custom mailbox](#view-user-submissions-to-microsoft) as described later in this article.</span></span>

- <span data-ttu-id="58a43-123">Pour plus d’informations sur la façon dont les utilisateurs peuvent envoyer des messages et des fichiers à Microsoft, voir Signaler des messages et [des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="58a43-123">For more information about how users can submit messages and files to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-suspicious-content-to-microsoft"></a><span data-ttu-id="58a43-124">Signaler du contenu suspect à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-124">Report suspicious content to Microsoft</span></span>

1. <span data-ttu-id="58a43-125">Dans le portail Microsoft 365 Defender, go to **Email & collaboration** \> **Submissions**.</span><span class="sxs-lookup"><span data-stu-id="58a43-125">In the Microsoft 365 Defender portal, go to **Email & collaboration** \> **Submissions**.</span></span>

2. <span data-ttu-id="58a43-126">Dans la page **Soumissions,** vérifiez que l’onglet Soumis pour analyse est sélectionné, puis cliquez sur Icône Annonce Envoyer à Microsoft pour  ![ ](../../media/m365-cc-sc-create-icon.png) **analyse.**</span><span class="sxs-lookup"><span data-stu-id="58a43-126">On the **Submissions** page, verify that the **Submitted for analysis** tab is selected, and then click ![Ad icon](../../media/m365-cc-sc-create-icon.png) **Submit to Microsoft for analysis**.</span></span>

3. <span data-ttu-id="58a43-127">Utilisez le **volant Envoyer à Microsoft** pour révision qui apparaît pour envoyer le message, l’URL ou la pièce jointe d’un e-mail, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="58a43-127">Use the **Submit to Microsoft for review** flyout that appears to submit the message, URL, or email attachment as described in the following sections.</span></span>

### <a name="submit-a-questionable-email-to-microsoft"></a><span data-ttu-id="58a43-128">Envoyer un e-mail douteux à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-128">Submit a questionable email to Microsoft</span></span>

1. <span data-ttu-id="58a43-129">Dans la **zone Sélectionner le type de** soumission, vérifiez que l’e-mail est sélectionné dans la liste de listes. </span><span class="sxs-lookup"><span data-stu-id="58a43-129">In the **Select the submission type** box, verify that **Email** is selected in the drop down list.</span></span>

2. <span data-ttu-id="58a43-130">Dans la section **Ajouter l’ID de message** réseau ou télécharger le fichier de courrier électronique, utilisez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="58a43-130">In the **Add the network message ID or upload the email file** section, use one of the following options:</span></span>
   - <span data-ttu-id="58a43-131">Ajoutez **l’ID** du message réseau de messagerie : il s’agit d’une valeur GUID disponible dans l’en-tête **X-MS-Exchange-Organization-Network-Message-Id** dans le message ou dans l’en-tête **X-MS-Office365-Filtering-Correlation-Id** dans les messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="58a43-131">**Add the email network message ID**: This is a GUID value that's available in the **X-MS-Exchange-Organization-Network-Message-Id** header in the message or in the **X-MS-Office365-Filtering-Correlation-Id** header in quarantined messages.</span></span>
   - <span data-ttu-id="58a43-132">**Télécharger fichier e-mail (.msg ou .eml)**: cliquez **sur Parcourir les fichiers.**</span><span class="sxs-lookup"><span data-stu-id="58a43-132">**Upload the email file (.msg or .eml)**: Click **Browse files**.</span></span> <span data-ttu-id="58a43-133">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier .eml ou .msg, puis cliquez sur **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="58a43-133">In the dialog that opens, find and select the .eml or .msg file, and then click **Open**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="58a43-134">La possibilité de soumettre des messages depuis 30 jours a été temporairement suspendue pour Defender pour Office 365 clients.</span><span class="sxs-lookup"><span data-stu-id="58a43-134">The ability to submit messages as old as 30 days has been temporarily suspended for Defender for Office 365 customers.</span></span> <span data-ttu-id="58a43-135">Les administrateurs ne pourront revenir qu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="58a43-135">Admins will only be able to go back 7 days.</span></span>

3. <span data-ttu-id="58a43-136">Dans la **zone Choisir un destinataire qui a eu** un problème, spécifiez le destinataire sur qui vous souhaitez exécuter une vérification de stratégie.</span><span class="sxs-lookup"><span data-stu-id="58a43-136">In the **Choose a recipient who had an issue** box, specify the recipient that you would like to run a policy check against.</span></span> <span data-ttu-id="58a43-137">La vérification de stratégie détermine si le courrier électronique a contourné l’analyse en raison des stratégies utilisateur ou organisation.</span><span class="sxs-lookup"><span data-stu-id="58a43-137">The policy check will determine if the email bypassed scanning due to user or organization policies.</span></span>

4. <span data-ttu-id="58a43-138">Dans la section **Sélectionner une raison d’envoyer à Microsoft,** sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="58a43-138">In the **Select a reason for submitting to Microsoft** section, select one of the following options:</span></span>
   - <span data-ttu-id="58a43-139">**Ne doit pas avoir été bloqué (faux positif)**</span><span class="sxs-lookup"><span data-stu-id="58a43-139">**Should not have been blocked (false positive)**</span></span>
   - <span data-ttu-id="58a43-140">**Doit avoir été bloqué**: dans l’e-mail doit avoir été catégorisé en tant que **section** qui s’affiche, sélectionnez l’une des valeurs suivantes (si vous n’êtes pas sûr, utilisez votre meilleur résultat) :</span><span class="sxs-lookup"><span data-stu-id="58a43-140">**Should have been blocked**: In the **The email should have been categorized as** section that appears, select one of the following values (if you're not sure, use your best judgement):</span></span>
     - <span data-ttu-id="58a43-141">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="58a43-141">**Phish**</span></span>
     - <span data-ttu-id="58a43-142">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="58a43-142">**Spam**</span></span>
     - <span data-ttu-id="58a43-143">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="58a43-143">**Malware**</span></span>

5. <span data-ttu-id="58a43-144">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="58a43-144">When you're finished, click the **Submit** button.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="58a43-145">![Exemple de soumission d’URL](../../media/submission-flyout-email.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-145">![New URL submission example](../../media/submission-flyout-email.png)</span></span>

### <a name="send-a-suspect-url-to-microsoft"></a><span data-ttu-id="58a43-146">Envoyer une URL suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-146">Send a suspect URL to Microsoft</span></span>

1. <span data-ttu-id="58a43-147">Dans la **zone Sélectionner le type de** soumission, sélectionnez **l’URL** dans la liste bas.</span><span class="sxs-lookup"><span data-stu-id="58a43-147">In the **Select the submission type** box, select **URL** from the drop down list.</span></span>

2. <span data-ttu-id="58a43-148">Dans la **zone URL** qui s’affiche, entrez l’URL complète (par exemple, `https://www.fabrikam.com/marketing.html` ).</span><span class="sxs-lookup"><span data-stu-id="58a43-148">In the **URL** box that appears, enter the full URL (for example, `https://www.fabrikam.com/marketing.html`).</span></span>

3. <span data-ttu-id="58a43-149">Dans la section **Sélectionner une raison d’envoyer à Microsoft,** sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="58a43-149">In the **Select a reason for submitting to Microsoft** section, select one of the following options:</span></span>
   - <span data-ttu-id="58a43-150">**Ne doit pas avoir été bloqué (faux positif)**</span><span class="sxs-lookup"><span data-stu-id="58a43-150">**Should not have been blocked (false positive)**</span></span>
   - <span data-ttu-id="58a43-151">**Doit avoir été bloqué :** dans l’URL, cette URL doit **avoir** été classée en tant que section qui s’affiche, sélectionnez **Hameçonnage** ou **Programme malveillant**.</span><span class="sxs-lookup"><span data-stu-id="58a43-151">**Should have been blocked**: In the **This URL should have been categorized as** section that appears, select **Phish** or **Malware**.</span></span>

4. <span data-ttu-id="58a43-152">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="58a43-152">When you're finished, click the **Submit** button.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="58a43-153">![Exemple d’envoi de nouveaux e-mails](../../media/submission-url-flyout.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-153">![New Email submission example](../../media/submission-url-flyout.png)</span></span>

### <a name="submit-a-suspected-email-attachment-to-microsoft"></a><span data-ttu-id="58a43-154">Envoyer une pièce jointe suspecte à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-154">Submit a suspected email attachment to Microsoft</span></span>

1. <span data-ttu-id="58a43-155">Dans la **zone Sélectionner le type de** soumission, **sélectionnez Fichier** dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="58a43-155">In the **Select the submission type** box, select **File** from the drop down list.</span></span>

2. <span data-ttu-id="58a43-156">Dans la section **Fichier** qui s’affiche, cliquez **sur Parcourir les fichiers.**</span><span class="sxs-lookup"><span data-stu-id="58a43-156">In the **File** section that appears, click **Browse files**.</span></span> <span data-ttu-id="58a43-157">Dans la boîte de dialogue qui s’ouvre, recherchez et sélectionnez le fichier, puis cliquez sur **Ouvrir.**</span><span class="sxs-lookup"><span data-stu-id="58a43-157">In the dialog that opens, find and select the file, and then click **Open**.</span></span>

3. <span data-ttu-id="58a43-158">Dans la section **Sélectionner une raison d’envoyer à Microsoft,** sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="58a43-158">In the **Select a reason for submitting to Microsoft** section, select one of the following options:</span></span>
   - <span data-ttu-id="58a43-159">**Ne doit pas avoir été bloqué (faux positif)**</span><span class="sxs-lookup"><span data-stu-id="58a43-159">**Should not have been blocked (false positive)**</span></span>
   - <span data-ttu-id="58a43-160">**Doit avoir été bloqué**: dans l’URL qui s’affiche, le programme malveillant est le seul choix et est automatiquement sélectionné.  </span><span class="sxs-lookup"><span data-stu-id="58a43-160">**Should have been blocked**: In the **This URL should have been categorized as** section that appears, **Malware** is the only choice, and is automatically selected.</span></span>

4. <span data-ttu-id="58a43-161">Lorsque vous avez terminé, cliquez sur le **bouton** Envoyer.</span><span class="sxs-lookup"><span data-stu-id="58a43-161">When you're finished, click the **Submit** button.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="58a43-162">![Exemple d’envoi de nouvelles pièces jointes](../../media/submission-file-flyout.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-162">![New Attachment submission example](../../media/submission-file-flyout.png)</span></span>

## <a name="view-admin-submissions-to-microsoft"></a><span data-ttu-id="58a43-163">Afficher les soumissions d’administrateur à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-163">View admin submissions to Microsoft</span></span>

1. <span data-ttu-id="58a43-164">Dans le portail Microsoft 365 Defender, go to **Email & collaboration** \> **Submissions**.</span><span class="sxs-lookup"><span data-stu-id="58a43-164">In the Microsoft 365 Defender portal, go to **Email & collaboration** \> **Submissions**.</span></span>

2. <span data-ttu-id="58a43-165">Dans la page **Soumissions,** vérifiez que l’onglet Soumis **pour** analyse est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="58a43-165">On the **Submissions** page, verify that the **Submitted for analysis** tab is selected.</span></span>

   - <span data-ttu-id="58a43-166">Vous pouvez trier les entrées en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="58a43-166">You can sort the entries by clicking on an available column header.</span></span> <span data-ttu-id="58a43-167">Cliquez **sur Personnaliser les colonnes** pour afficher un maximum de sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="58a43-167">Click **Customize columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="58a43-168">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="58a43-168">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>
     - <span data-ttu-id="58a43-169">**Nom de la soumission**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-169">**Submission name**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-170">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-170">**Sender**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-171">**Date d’soumise**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-171">**Date submitted**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-172">**Type de soumission**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-172">**Submission type**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-173">**Raison de l’envoi**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-173">**Reason for submitting**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-174">**État rescan**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-174">**Rescan status**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-175">**Résultat rescan**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-175">**Rescan result**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-176">**Verdict du filtre**</span><span class="sxs-lookup"><span data-stu-id="58a43-176">**Filter verdict**</span></span>
     - <span data-ttu-id="58a43-177">**Raison de la remise/du blocage**</span><span class="sxs-lookup"><span data-stu-id="58a43-177">**Delivery/Block reason**</span></span>
     - <span data-ttu-id="58a43-178">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="58a43-178">**Submission ID**</span></span>
     - <span data-ttu-id="58a43-179">**ID de message réseau/ID d’objet**</span><span class="sxs-lookup"><span data-stu-id="58a43-179">**Network Message ID/Object ID**</span></span>
     - <span data-ttu-id="58a43-180">**Direction**</span><span class="sxs-lookup"><span data-stu-id="58a43-180">**Direction**</span></span>
     - <span data-ttu-id="58a43-181">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="58a43-181">**Sender IP**</span></span>
     - <span data-ttu-id="58a43-182">**Niveau de conformité en bloc (BCL)**</span><span class="sxs-lookup"><span data-stu-id="58a43-182">**Bulk compliant level (BCL)**</span></span>
     - <span data-ttu-id="58a43-183">**Destination**</span><span class="sxs-lookup"><span data-stu-id="58a43-183">**Destination**</span></span>
     - <span data-ttu-id="58a43-184">**Action de stratégie**</span><span class="sxs-lookup"><span data-stu-id="58a43-184">**Policy action**</span></span>
     - <span data-ttu-id="58a43-185">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="58a43-185">**Submitted by**</span></span>

     <span data-ttu-id="58a43-186">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-186">When you're finished, click **Apply**.</span></span>

   - <span data-ttu-id="58a43-187">Pour filtrer les entrées, cliquez sur **Filtrer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-187">To filter the entries, click **Filter**.</span></span> <span data-ttu-id="58a43-188">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="58a43-188">The available filters are:</span></span>
     - <span data-ttu-id="58a43-189">**Date envoyée**: **date de début** et date de **fin.**</span><span class="sxs-lookup"><span data-stu-id="58a43-189">**Date submitted**: **Start date** and **End date**.</span></span>
     - <span data-ttu-id="58a43-190">**Type de soumission**: **e-mail,** **URL** ou **fichier**.</span><span class="sxs-lookup"><span data-stu-id="58a43-190">**Submission type**: **Email**, **URL**, or **File**.</span></span>
     - <span data-ttu-id="58a43-191">**ID de soumission**: valeur GUID attribuée à chaque soumission.</span><span class="sxs-lookup"><span data-stu-id="58a43-191">**Submission ID**: A GUID value that's assigned to every submission.</span></span>
     - <span data-ttu-id="58a43-192">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="58a43-192">**Network Message ID**</span></span>
     - <span data-ttu-id="58a43-193">**Sender**</span><span class="sxs-lookup"><span data-stu-id="58a43-193">**Sender**</span></span>

     <span data-ttu-id="58a43-194">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-194">When you're finished, click **Apply**.</span></span>

     > [!div class="mx-imgBorder"]
     > <span data-ttu-id="58a43-195">![Nouvelles options de filtre pour les soumissions d’administrateur](../../media/admin-submission-filters.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-195">![New Filter options for admin submissions](../../media/admin-submission-filters.png)</span></span>

   - <span data-ttu-id="58a43-196">Pour grouper les entrées, cliquez sur **Grouper** et sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="58a43-196">To group the entries, click **Group** and select one of the following values from the drop down list:</span></span>
     - <span data-ttu-id="58a43-197">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="58a43-197">**None**</span></span>
     - <span data-ttu-id="58a43-198">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="58a43-198">**Type**</span></span>
     - <span data-ttu-id="58a43-199">**Raison**</span><span class="sxs-lookup"><span data-stu-id="58a43-199">**Reason**</span></span>
     - <span data-ttu-id="58a43-200">**État**</span><span class="sxs-lookup"><span data-stu-id="58a43-200">**Status**</span></span>
     - <span data-ttu-id="58a43-201">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="58a43-201">**Rescan result**</span></span>

   - <span data-ttu-id="58a43-202">Pour exporter les entrées, cliquez sur **Exporter.**</span><span class="sxs-lookup"><span data-stu-id="58a43-202">To export the entries, click **Export**.</span></span> <span data-ttu-id="58a43-203">Dans la boîte de dialogue qui s’affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="58a43-203">In the dialog that appears, save the .csv file.</span></span>

### <a name="admin-submission-rescan-details"></a><span data-ttu-id="58a43-204">Détails de la rescan de soumission de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="58a43-204">Admin submission rescan details</span></span>

<span data-ttu-id="58a43-205">Les messages envoyés dans les soumissions d’administrateur sont examinés et les résultats sont affichés dans le flyout détaillé des soumissions :</span><span class="sxs-lookup"><span data-stu-id="58a43-205">Messages that are submitted in admin submissions are reviewed and results shown in the submissions detail flyout:</span></span>

- <span data-ttu-id="58a43-206">En cas d’échec de l’authentification des e-mails de l’expéditeur au moment de la livraison.</span><span class="sxs-lookup"><span data-stu-id="58a43-206">If there was a failure in the sender's email authentication at the time of delivery.</span></span>
- <span data-ttu-id="58a43-207">Informations sur les accès à la stratégie qui auraient pu affecter ou écraser le verdict d’un message.</span><span class="sxs-lookup"><span data-stu-id="58a43-207">Information about any policy hits that could have affected or overridden the verdict of a message.</span></span>
- <span data-ttu-id="58a43-208">Résultats actuels de la détonation pour savoir si les URL ou fichiers contenus dans le message étaient malveillants ou non.</span><span class="sxs-lookup"><span data-stu-id="58a43-208">Current detonation results to see if the URLs or files contained in the message were malicious or not.</span></span>
- <span data-ttu-id="58a43-209">Commentaires des élèves.</span><span class="sxs-lookup"><span data-stu-id="58a43-209">Feedback from graders.</span></span>

<span data-ttu-id="58a43-210">Si le programme a trouvé un remplacement, la nouvelle analyse doit se terminer après plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="58a43-210">If an override was found, the rescan should complete in several minutes.</span></span> <span data-ttu-id="58a43-211">S’il n’y a pas de problème dans l’authentification ou la remise du courrier électronique n’a pas été affecté par une substitution, les commentaires des élèves peuvent prendre jusqu’à un jour.</span><span class="sxs-lookup"><span data-stu-id="58a43-211">If there wasn't a problem in email authentication or delivery wasn't affected by an override, then the feedback from graders could take up to a day.</span></span>

## <a name="view-user-submissions-to-microsoft"></a><span data-ttu-id="58a43-212">Afficher les soumissions d’utilisateurs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="58a43-212">View user submissions to Microsoft</span></span>

<span data-ttu-id="58a43-213">Si vous avez déployé le [add-in](enable-the-report-message-add-in.md) [](enable-the-report-phish-add-in.md)Signaler un message, le module de signalement du hameçonnage ou que des personnes utilisent les rapports intégrés dans  [Outlook sur le web,](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)vous pouvez voir les utilisateurs qui signalent dans l’onglet Message signalé par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58a43-213">If you've deployed the [Report Message add-in](enable-the-report-message-add-in.md), the [Report Phishing add-in](enable-the-report-phish-add-in.md), or people use the [built-in reporting in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md), you can see what users are reporting on the **User reported message** tab.</span></span>

1. <span data-ttu-id="58a43-214">Dans le portail Microsoft 365 Defender, go to **Email & collaboration** \> **Submissions**.</span><span class="sxs-lookup"><span data-stu-id="58a43-214">In the Microsoft 365 Defender portal, go to **Email & collaboration** \> **Submissions**.</span></span>

2. <span data-ttu-id="58a43-215">Dans la page **Soumissions,** sélectionnez **l’onglet Messages signalés par l’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="58a43-215">On the **Submissions** page, select the **User reported messages** tab.</span></span>

   - <span data-ttu-id="58a43-216">Vous pouvez trier les entrées en cliquant sur un en-tête de colonne disponible.</span><span class="sxs-lookup"><span data-stu-id="58a43-216">You can sort the entries by clicking on an available column header.</span></span> <span data-ttu-id="58a43-217">Cliquez **sur Personnaliser les colonnes** pour afficher un maximum de sept colonnes.</span><span class="sxs-lookup"><span data-stu-id="58a43-217">Click **Customize columns** to show a maximum of seven columns.</span></span> <span data-ttu-id="58a43-218">Les valeurs par défaut sont marquées d'un astérisque (<sup>\*</sup>) :</span><span class="sxs-lookup"><span data-stu-id="58a43-218">The default values are marked with an asterisk (<sup>\*</sup>):</span></span>

     - <span data-ttu-id="58a43-219">**Objet de l’e-mail**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-219">**Email subject**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-220">**Signalé par**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-220">**Reported by**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-221">**Date de rapport**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-221">**Date reported**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-222">**Expéditeur**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-222">**Sender**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-223">**Raison signalée**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-223">**Reported reason**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-224">**Résultat rescan**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="58a43-224">**Rescan result**<sup>\*</sup></span></span>
     - <span data-ttu-id="58a43-225">**ID de message signalé**</span><span class="sxs-lookup"><span data-stu-id="58a43-225">**Message reported ID**</span></span>
     - <span data-ttu-id="58a43-226">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="58a43-226">**Network Message ID**</span></span>
     - <span data-ttu-id="58a43-227">**IP de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="58a43-227">**Sender IP**</span></span>
     - <span data-ttu-id="58a43-228">**Simulation de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="58a43-228">**Phish simulation**</span></span>

     <span data-ttu-id="58a43-229">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-229">When you're finished, click **Apply**.</span></span>

   - <span data-ttu-id="58a43-230">Pour filtrer les entrées, cliquez sur **Filtrer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-230">To filter the entries, click **Filter**.</span></span> <span data-ttu-id="58a43-231">Les filtres disponibles sont :</span><span class="sxs-lookup"><span data-stu-id="58a43-231">The available filters are:</span></span>
     - <span data-ttu-id="58a43-232">**Date signalée**: **date de début** et date de **fin.**</span><span class="sxs-lookup"><span data-stu-id="58a43-232">**Date reported**: **Start date** and **End date**.</span></span>
     - <span data-ttu-id="58a43-233">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="58a43-233">**Reported by**</span></span>
     - <span data-ttu-id="58a43-234">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="58a43-234">**Email subject**</span></span>
     - <span data-ttu-id="58a43-235">**ID de message signalé**</span><span class="sxs-lookup"><span data-stu-id="58a43-235">**Message reported ID**</span></span>
     - <span data-ttu-id="58a43-236">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="58a43-236">**Network Message ID**</span></span>
     - <span data-ttu-id="58a43-237">**Sender**</span><span class="sxs-lookup"><span data-stu-id="58a43-237">**Sender**</span></span>
     - <span data-ttu-id="58a43-238">**Raison signalée :** **pas de courrier indésirable,** **de hameçonnage** ou de **courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="58a43-238">**Reported reason**: **Not junk**, **Phish**, or **Spam**.</span></span>
     - <span data-ttu-id="58a43-239">**Simulation de hameçonnage**: **Oui** ou **Non**</span><span class="sxs-lookup"><span data-stu-id="58a43-239">**Phish simulation**: **Yes** or **No**</span></span>

     <span data-ttu-id="58a43-240">Lorsque vous avez terminé, cliquez sur **Appliquer.**</span><span class="sxs-lookup"><span data-stu-id="58a43-240">When you're finished, click **Apply**.</span></span>

     > [!div class="mx-imgBorder"]
     > <span data-ttu-id="58a43-241">![Nouvelles options de filtre pour les soumissions d’utilisateurs](../../media/admin-submission-reported-messages.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-241">![New Filter options for user submissions](../../media/admin-submission-reported-messages.png)</span></span>

   - <span data-ttu-id="58a43-242">Pour grouper les entrées, cliquez sur **Grouper** et sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="58a43-242">To group the entries, click **Group** and select one of the following values from the drop down list:</span></span>
     - <span data-ttu-id="58a43-243">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="58a43-243">**None**</span></span>
     - <span data-ttu-id="58a43-244">**Raison**</span><span class="sxs-lookup"><span data-stu-id="58a43-244">**Reason**</span></span>
     - <span data-ttu-id="58a43-245">**Sender**</span><span class="sxs-lookup"><span data-stu-id="58a43-245">**Sender**</span></span>
     - <span data-ttu-id="58a43-246">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="58a43-246">**Reported by**</span></span>
     - <span data-ttu-id="58a43-247">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="58a43-247">**Rescan result**</span></span>
     - <span data-ttu-id="58a43-248">**Simulation de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="58a43-248">**Phish simulation**</span></span>

   - <span data-ttu-id="58a43-249">Pour exporter les entrées, cliquez sur **Exporter.**</span><span class="sxs-lookup"><span data-stu-id="58a43-249">To export the entries, click **Export**.</span></span> <span data-ttu-id="58a43-250">Dans la boîte de dialogue qui s’affiche, enregistrez .csv fichier.</span><span class="sxs-lookup"><span data-stu-id="58a43-250">In the dialog that appears, save the .csv file.</span></span>

> [!NOTE]
> <span data-ttu-id="58a43-251">Si les organisations sont configurées pour envoyer des messages signalés par l’utilisateur à la boîte aux lettres personnalisée uniquement, les messages signalés ne seront pas envoyés pour réascan et les résultats dans les **messages** signalés par l’utilisateur seront toujours vides.</span><span class="sxs-lookup"><span data-stu-id="58a43-251">If organizations are configured to send user reported messages to the custom mailbox only, reported messages will not be sent for rescan and the results in **User reported messages** will always be empty.</span></span>

### <a name="undo-user-submissions"></a><span data-ttu-id="58a43-252">Annuler les soumissions d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="58a43-252">Undo user submissions</span></span>

<span data-ttu-id="58a43-253">Lorsqu’un utilisateur envoie un message suspect à la boîte aux lettres personnalisée, l’utilisateur et l’administrateur n’ont pas la possibilité d’annuler la soumission.</span><span class="sxs-lookup"><span data-stu-id="58a43-253">Once a user submits a suspicious email to the custom mailbox, the user and admin don't have an option to undo the submission.</span></span> <span data-ttu-id="58a43-254">Si l’utilisateur souhaite récupérer le courrier électronique, il pourra être récupéré dans les dossiers Éléments supprimés ou Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="58a43-254">If the user would like to recover the email, it will be available for recovery in the Deleted Items or Junk Email folders.</span></span>

### <a name="submit-messages-to-microsoft-from-the-custom-mailbox"></a><span data-ttu-id="58a43-255">Envoyer des messages à Microsoft à partir de la boîte aux lettres personnalisée</span><span class="sxs-lookup"><span data-stu-id="58a43-255">Submit messages to Microsoft from the custom mailbox</span></span>

<span data-ttu-id="58a43-256">Si vous avez configuré la boîte aux lettres personnalisée pour intercepter les messages signalés par l’utilisateur sans les envoyer à Microsoft, vous pouvez rechercher et envoyer des messages spécifiques à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="58a43-256">If you've configured the custom mailbox to intercept user-reported messages without sending the messages to Microsoft, you can find and send specific messages to Microsoft for analysis.</span></span> <span data-ttu-id="58a43-257">Cela déplace efficacement une soumission d’utilisateur vers une soumission d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="58a43-257">This effectively moves a user submission to an admin submission.</span></span>

<span data-ttu-id="58a43-258">Sous **l’onglet Messages** signalés par l’utilisateur, sélectionnez un message dans la liste, cliquez sur Envoyer à **Microsoft** pour analyse, puis sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="58a43-258">On the **User reported messages** tab, select a message in the list, click **Submit to Microsoft for analysis**, and then select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="58a43-259">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="58a43-259">**Report clean**</span></span>
- <span data-ttu-id="58a43-260">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="58a43-260">**Report phishing**</span></span>
- <span data-ttu-id="58a43-261">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="58a43-261">**Report malware**</span></span>
- <span data-ttu-id="58a43-262">**Signaler le courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="58a43-262">**Report spam**</span></span>
- <span data-ttu-id="58a43-263">**Déclencher l’examen**</span><span class="sxs-lookup"><span data-stu-id="58a43-263">**Trigger investigation**</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="58a43-264">![Nouvelles options sur le bouton Action](../../media/admin-submission-main-action-button.png)</span><span class="sxs-lookup"><span data-stu-id="58a43-264">![New Options on the Action button](../../media/admin-submission-main-action-button.png)</span></span>
