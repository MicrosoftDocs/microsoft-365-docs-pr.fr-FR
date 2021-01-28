---
title: Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web
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
ms.assetid: 758822b5-0126-463a-9d08-7366bb2a807d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les options intégrées de signalement de courrier indésirable, non indésirable et de hameçonnage dans Outlook sur le web (Outlook Web App) dans Exchange Online, et comment désactiver ces options de rapport pour les utilisateurs.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 0af57aceed608ae80e72e3ae18724925c1168e26
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029209"
---
# <a name="report-junk-and-phishing-email-in-outlook-on-the-web-in-exchange-online"></a><span data-ttu-id="55155-103">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="55155-103">Report junk and phishing email in Outlook on the web in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="55155-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, vous pouvez utiliser les options de rapport intégrées dans Outlook sur le web (anciennement Outlook Web App) pour envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="55155-104">In Microsoft 365 organizations with mailboxes in Exchange Online, you can use the built-in reporting options in Outlook on the web (formerly known as Outlook Web App) to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="55155-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="55155-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="55155-106">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="55155-106">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="55155-107">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="55155-107">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="55155-108">Les administrateurs peuvent désactiver ou activer la possibilité pour les utilisateurs de signaler des messages à Microsoft dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="55155-108">Admins can disable or enable the ability for users to report messages to Microsoft in Outlook on the web.</span></span> <span data-ttu-id="55155-109">Pour plus d’informations, voir la section Désactiver ou activer la signalement du courrier indésirable [dans Outlook sur](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) le web plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="55155-109">For details, see the [Disable or enable junk email reporting in Outlook on the web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) section later in this article.</span></span>

- <span data-ttu-id="55155-110">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="55155-110">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="55155-111">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="55155-111">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="55155-112">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="55155-112">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-on-the-web"></a><span data-ttu-id="55155-113">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="55155-113">Report spam and phishing messages in Outlook on the web</span></span>

1. <span data-ttu-id="55155-114">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="55155-114">For messages in the Inbox or any other email folder except Junk Email, use either of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="55155-115">Sélectionnez le message, cliquez **sur Courrier** indésirable dans la barre d’outils, puis **sélectionnez** Courrier indésirable ou **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="55155-115">Select the message, click **Junk** on the toolbar, and then select **Junk** or **Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/owa-report-junk.png)

   - <span data-ttu-id="55155-117">Sélectionnez un ou plusieurs messages, cliquez avec le bouton droit, puis **sélectionnez Marquer comme courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="55155-117">Select one or more messages, right-click, and then select **Mark as junk**.</span></span>

2. <span data-ttu-id="55155-118">Dans la boîte de dialogue qui s’affiche, cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="55155-118">In the dialog that appears, click **Report**.</span></span> <span data-ttu-id="55155-119">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="55155-119">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="55155-120">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="55155-120">Junk</span></span>|<span data-ttu-id="55155-121">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="55155-121">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue Signaler comme courrier indésirable](../../media/owa-report-as-junk-dialog.png)|![Boîte de dialogue Signaler comme hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="55155-124">Les messages sélectionnés sont envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="55155-124">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="55155-125">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="55155-125">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="report-non-spam-and-phishing-messages-from-the-junk-email-folder-in-outlook-on-the-web"></a><span data-ttu-id="55155-126">Signaler les messages de courrier non indésirable et de hameçonnage à partir du dossier Courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="55155-126">Report non-spam and phishing messages from the Junk Email folder in Outlook on the web</span></span>

1. <span data-ttu-id="55155-127">Dans le dossier Courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les faux positifs du courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="55155-127">In the Junk Email folder, use either of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="55155-128">Sélectionnez le message, cliquez **sur Ne** pas courrier indésirable dans la barre d’outils, puis sélectionnez Ne pas être indésirable **ou** **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="55155-128">Select the message, click **Not Junk** on the toolbar, and then select **Not Junk** or **Phishing**.</span></span>

     ![Signaler le courrier électronique non indésirable ou non de hameçonnage à partir du ruban](../../media/owa-report-not-junk.png)

   - <span data-ttu-id="55155-130">Sélectionnez un ou plusieurs messages, cliquez avec le bouton droit, puis **sélectionnez Marquer comme courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="55155-130">Select one or more messages, right-click, and then select **Mark as not junk**.</span></span>

2. <span data-ttu-id="55155-131">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="55155-131">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="55155-132">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="55155-132">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="55155-133">Non indésirable</span><span class="sxs-lookup"><span data-stu-id="55155-133">Not Junk</span></span>|<span data-ttu-id="55155-134">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="55155-134">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue Signaler comme courrier indésirable](../../media/owa-report-as-not-junk-dialog.png)|![Boîte de dialogue Signaler comme hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="55155-137">Les messages sélectionnés sont envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="55155-137">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="55155-138">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="55155-138">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="55155-139">Désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="55155-139">Disable or enable junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="55155-140">Par défaut, les utilisateurs peuvent signaler des faux positifs, des faux négatifs et des messages de hameçonnage à Microsoft pour analyse dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="55155-140">By default, users can report spam false positives, false negatives, and phishing messages to Microsoft for analysis in Outlook on the web.</span></span> <span data-ttu-id="55155-141">Les administrateurs peuvent configurer des stratégies de boîte aux lettres Outlook sur le web dans Exchange Online PowerShell pour empêcher les utilisateurs de signaler des faux positifs et des faux négatifs de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="55155-141">Admins can configure Outlook on the web mailbox policies in Exchange Online PowerShell to prevent users from reporting spam false positives and spam false negatives to Microsoft.</span></span> <span data-ttu-id="55155-142">Vous ne pouvez pas désactiver la possibilité pour les utilisateurs de signaler des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="55155-142">You can't disable the ability for users to report phishing messages to Microsoft.</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="55155-143">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="55155-143">What do you need to know before you begin?</span></span>

- <span data-ttu-id="55155-144">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="55155-144">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="55155-145">Des autorisations doivent vous être attribuées dans Exchange Online avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="55155-145">You need to be assigned permissions in Exchange Online before you can do the procedures in this article.</span></span> <span data-ttu-id="55155-146">Plus précisément,  vous avez besoin des **rôles Stratégies** des  destinataires ou Destinataires de messagerie, qui sont attribués par défaut aux groupes de rôles Gestion de l’organisation et Gestion des destinataires. </span><span class="sxs-lookup"><span data-stu-id="55155-146">Specifically you need the **Recipient Policies** or **Mail Recipients** roles, which are assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="55155-147">Pour plus d’informations sur les groupes de rôles dans Exchange Online, voir [Autorisations dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) et Modifier les groupes de [rôles dans Exchange Online.](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups)</span><span class="sxs-lookup"><span data-stu-id="55155-147">For more information about role groups in Exchange Online, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) and [Modify role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups).</span></span>

- <span data-ttu-id="55155-148">Chaque organisation possède une stratégie par défaut nommée OwaMailboxPolicy-Default, mais vous pouvez créer des stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="55155-148">Every organization has a default policy named OwaMailboxPolicy-Default, but you can create custom policies.</span></span> <span data-ttu-id="55155-149">Les stratégies personnalisées sont appliquées aux utilisateurs d’étendue avant la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="55155-149">Custom policies are applied to scoped users before the default policy.</span></span> <span data-ttu-id="55155-150">Pour plus d’informations sur les stratégies de boîte aux lettres Outlook sur le web, consultez stratégies de boîte aux lettres [Outlook sur le web dans Exchange Online.](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies)</span><span class="sxs-lookup"><span data-stu-id="55155-150">For more information about Outlook on the web mailbox policies, see [Outlook on the web mailbox policies in Exchange Online](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span></span>

- <span data-ttu-id="55155-151">La désactivation de la signalement du courrier indésirable ne supprime pas la possibilité de marquer un message comme courrier indésirable ou non indésirable dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="55155-151">Disabling junk email reporting doesn't remove the ability to mark a message as junk or not junk in Outlook on the web.</span></span> <span data-ttu-id="55155-152">La sélection d’un message dans  le dossier Courrier indésirable et le fait de cliquer sur Ne pas courrier indésirable déplace toujours le \>  message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="55155-152">Selecting a message in the Junk email folder and clicking **Not junk** \> **Not junk** still moves the message back into the Inbox.</span></span> <span data-ttu-id="55155-153">La sélection d’un message dans  un autre dossier de courrier électronique et le fait de cliquer sur Courrier indésirable déplace toujours le message dans le \>  dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="55155-153">Selecting a message in any other email folder and clicking **Junk** \> **Junk** still moves the message into the Junk Email folder.</span></span> <span data-ttu-id="55155-154">Ce qui n’est plus disponible, c’est la possibilité de signaler le message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="55155-154">What's no longer available is the option to report the message to Microsoft.</span></span>

### <a name="use-exchange-online-powershell-to-disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="55155-155">Utiliser Exchange Online PowerShell pour désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="55155-155">Use Exchange Online PowerShell to disable or enable junk email reporting in Outlook on the web</span></span>

1. <span data-ttu-id="55155-156">Pour rechercher vos stratégies de boîte aux lettres Outlook sur le web existantes et l’état des rapports de courrier indésirable, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="55155-156">To find your existing Outlook on the web mailbox policies and the status of junk email reporting, run the following command:</span></span>

   ```powershell
   Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
   ```

2. <span data-ttu-id="55155-157">Pour désactiver ou activer la signalement du courrier indésirable dans Outlook sur le web, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="55155-157">To disable or enable junk email reporting in Outlook on the web, use the following syntax:</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
   ```

   <span data-ttu-id="55155-158">Cet exemple désactive le signalement du courrier indésirable dans la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="55155-158">This example disables junk email reporting in the default policy.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
   ```

   <span data-ttu-id="55155-159">Cet exemple active la création de rapports de courrier indésirable dans la stratégie personnalisée nommée Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="55155-159">This example enables junk email reporting in the custom policy named Contoso Managers.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "Contoso Managers" -ReportJunkEmailEnabled $true
   ```

<span data-ttu-id="55155-160">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) et [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="55155-160">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) and [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="55155-161">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="55155-161">How do you know this worked?</span></span>

<span data-ttu-id="55155-162">Pour vérifier que vous avez bien activé ou désactivé le signalement du courrier indésirable dans Outlook sur le web, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="55155-162">To verify that you've successfully enabled or disabled junk email reporting in Outlook on the web, use any of the following steps:</span></span>

- <span data-ttu-id="55155-163">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez la valeur de la propriété **ReportJunkEmailEnabled** :</span><span class="sxs-lookup"><span data-stu-id="55155-163">In Exchange Online PowerShell, run the following command and verify the **ReportJunkEmailEnabled** property value:</span></span>

  ```powershell
  Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
  ```

- <span data-ttu-id="55155-164">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans la boîte de réception, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est \>  pas affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="55155-164">Open an affected user's mailbox in Outlook on the web, select a message in the Inbox, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

- <span data-ttu-id="55155-165">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans le dossier Courrier indésirable, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est \>  pas affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="55155-165">Open an affected user's mailbox in Outlook on the web, select a message in the Junk Email folder, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

<span data-ttu-id="55155-166"><sup>\*</sup> Les utilisateurs peuvent masquer l’invite de signalement du message tout en le signalant.</span><span class="sxs-lookup"><span data-stu-id="55155-166"><sup>\*</sup> Users can hide the prompt to report the message while still reporting the message.</span></span> <span data-ttu-id="55155-167">Pour vérifier ce paramètre dans Outlook sur le web :</span><span class="sxs-lookup"><span data-stu-id="55155-167">To check this setting in Outlook on the web:</span></span>

1. <span data-ttu-id="55155-168">Cliquez **sur l’icône Paramètres** ![ Outlook sur le web Icône Afficher tous les ](../../media/owa-settings-icon.png) \> **paramètres Outlook Courrier** \> **indésirable.**</span><span class="sxs-lookup"><span data-stu-id="55155-168">Click **Settings** ![Outlook on the web settings icon](../../media/owa-settings-icon.png) \> **View all Outlook settings** \> **Junk email**.</span></span>
2. <span data-ttu-id="55155-169">Dans la section **Création de** rapports, vérifiez la valeur : **Demandez-moi avant d’envoyer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="55155-169">In the **Reporting** section, verify the value: **Ask me before sending a report**.</span></span>

   ![Paramètres de création de rapports de courrier indésirable Outlook sur le web](../../media/owa-junk-email-reporting-options.png)
