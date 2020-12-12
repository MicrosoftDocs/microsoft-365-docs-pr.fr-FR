---
title: Signaler les messages de courrier indésirable et de hameçonnage dans Outlook sur le Web
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
ms.assetid: 758822b5-0126-463a-9d08-7366bb2a807d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir les options de notification de courrier indésirable, non légitime et de hameçonnage dans Outlook sur le Web (Outlook Web App) dans Exchange Online et comment désactiver ces options de création de rapports pour les utilisateurs.
ms.openlocfilehash: 0032e807961aed60128d6863899ae0de32d1a627
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49659308"
---
# <a name="report-junk-and-phishing-email-in-outlook-on-the-web-in-exchange-online"></a><span data-ttu-id="7a4cc-103">Signaler le courrier indésirable et de hameçonnage dans Outlook sur le Web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7a4cc-103">Report junk and phishing email in Outlook on the web in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="7a4cc-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, vous pouvez utiliser les options de création de rapports intégrées dans Outlook sur le Web (anciennement Outlook Web App) pour soumettre des faux positifs (courrier électronique marqué comme courrier indésirable), des faux négatifs (courrier incorrect autorisé) et des messages de hameçonnage vers Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-104">In Microsoft 365 organizations with mailboxes in Exchange Online, you can use the built-in reporting options in Outlook on the web (formerly known as Outlook Web App) to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7a4cc-105">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7a4cc-105">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7a4cc-106">Si vous êtes administrateur d’une organisation avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail d’envoi du centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-106">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="7a4cc-107">Pour plus d’informations, consultez la rubrique [utiliser la soumission de l’administrateur pour envoyer des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-107">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="7a4cc-108">Les administrateurs peuvent désactiver ou activer la possibilité pour les utilisateurs de signaler des messages à Microsoft dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-108">Admins can disable or enable the ability for users to report messages to Microsoft in Outlook on the web.</span></span> <span data-ttu-id="7a4cc-109">Pour plus d’informations, consultez la section [désactiver ou activer la création de rapports de courrier indésirable dans Outlook sur le Web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-109">For details, see the [Disable or enable junk email reporting in Outlook on the web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) section later in this article.</span></span>

- <span data-ttu-id="7a4cc-110">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-110">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="7a4cc-111">Pour plus d’informations, consultez la rubrique [User submissions Policies](user-submission.md).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-111">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="7a4cc-112">Pour plus d’informations sur la création de rapports de messages à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-112">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-on-the-web"></a><span data-ttu-id="7a4cc-113">Signaler les messages de courrier indésirable et de hameçonnage dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7a4cc-113">Report spam and phishing messages in Outlook on the web</span></span>

1. <span data-ttu-id="7a4cc-114">Pour les messages de la boîte de réception ou de tout autre dossier de messagerie, à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les messages de courrier indésirable et de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-114">For messages in the Inbox or any other email folder except Junk Email, use either of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="7a4cc-115">Sélectionnez le message, cliquez sur **courrier indésirable** dans la barre d’outils, puis sélectionnez **courrier indésirable** ou **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-115">Select the message, click **Junk** on the toolbar, and then select **Junk** or **Phishing**.</span></span>

     ![Signaler le courrier indésirable ou de hameçonnage à partir du ruban](../../media/owa-report-junk.png)

   - <span data-ttu-id="7a4cc-117">Sélectionnez un ou plusieurs messages, cliquez dessus avec le bouton droit, puis sélectionnez **marquer comme courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-117">Select one or more messages, right-click, and then select **Mark as junk**.</span></span>

2. <span data-ttu-id="7a4cc-118">Dans la boîte de dialogue qui s’affiche, cliquez sur **rapport**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-118">In the dialog that appears, click **Report**.</span></span> <span data-ttu-id="7a4cc-119">Si vous changez d’avis, cliquez sur **ne pas signaler**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-119">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="7a4cc-120">Filtre</span><span class="sxs-lookup"><span data-stu-id="7a4cc-120">Junk</span></span>|<span data-ttu-id="7a4cc-121">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="7a4cc-121">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue signaler comme courrier indésirable](../../media/owa-report-as-junk-dialog.png)|![Boîte de dialogue signaler en tant que hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="7a4cc-124">Les messages sélectionnés seront envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-124">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="7a4cc-125">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-125">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="report-non-spam-and-phishing-messages-from-the-junk-email-folder-in-outlook-on-the-web"></a><span data-ttu-id="7a4cc-126">Signaler les messages de courrier indésirable et de hameçonnage dans le dossier courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7a4cc-126">Report non-spam and phishing messages from the Junk Email folder in Outlook on the web</span></span>

1. <span data-ttu-id="7a4cc-127">Dans le dossier courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les fausses alertes de courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-127">In the Junk Email folder, use either of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="7a4cc-128">Sélectionnez le message, cliquez sur **légitime** dans la barre d’outils, puis sélectionnez **pas de courrier indésirable** ou de **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-128">Select the message, click **Not Junk** on the toolbar, and then select **Not Junk** or **Phishing**.</span></span>

     ![Signaler le courrier indésirable ou ne pas faire de hameçonnage à partir du ruban](../../media/owa-report-not-junk.png)

   - <span data-ttu-id="7a4cc-130">Sélectionnez un ou plusieurs messages, cliquez dessus avec le bouton droit, puis sélectionnez **marquer comme légitime**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-130">Select one or more messages, right-click, and then select **Mark as not junk**.</span></span>

2. <span data-ttu-id="7a4cc-131">Dans la boîte de dialogue qui s’affiche, lisez les informations, puis cliquez sur **rapport**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-131">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="7a4cc-132">Si vous changez d’avis, cliquez sur **ne pas signaler**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-132">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="7a4cc-133">Courrier légitime</span><span class="sxs-lookup"><span data-stu-id="7a4cc-133">Not Junk</span></span>|<span data-ttu-id="7a4cc-134">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="7a4cc-134">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue signaler comme légitime](../../media/owa-report-as-not-junk-dialog.png)|![Boîte de dialogue signaler en tant que hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="7a4cc-137">Les messages sélectionnés seront envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-137">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="7a4cc-138">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-138">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="7a4cc-139">Désactiver ou activer la création de rapports de courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7a4cc-139">Disable or enable junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="7a4cc-140">Par défaut, les utilisateurs peuvent signaler des faux positifs de courrier indésirable, des faux négatifs et des messages de hameçonnage à Microsoft pour analyse dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-140">By default, users can report spam false positives, false negatives, and phishing messages to Microsoft for analysis in Outlook on the web.</span></span> <span data-ttu-id="7a4cc-141">Les administrateurs peuvent configurer les stratégies de boîte aux lettres Outlook sur le Web dans Exchange Online PowerShell pour empêcher les utilisateurs de signaler les faux positifs de courrier indésirable et les faux négatifs de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-141">Admins can configure Outlook on the web mailbox policies in Exchange Online PowerShell to prevent users from reporting spam false positives and spam false negatives to Microsoft.</span></span> <span data-ttu-id="7a4cc-142">Vous ne pouvez pas désactiver la possibilité pour les utilisateurs de signaler les messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-142">You can't disable the ability for users to report phishing messages to Microsoft.</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="7a4cc-143">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="7a4cc-143">What do you need to know before you begin?</span></span>

- <span data-ttu-id="7a4cc-144">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-144">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="7a4cc-145">Pour pouvoir effectuer les procédures décrites dans cet article, vous devez disposer d’autorisations dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-145">You need to be assigned permissions in Exchange Online before you can do the procedures in this article.</span></span> <span data-ttu-id="7a4cc-146">Vous avez spécifiquement besoin des rôles **stratégies de destinataire** ou **destinataires de messagerie** , qui sont affectés par défaut aux groupes de rôles gestion de l' **organisation** et **gestion des destinataires** .</span><span class="sxs-lookup"><span data-stu-id="7a4cc-146">Specifically you need the **Recipient Policies** or **Mail Recipients** roles, which are assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="7a4cc-147">Pour plus d’informations sur les groupes de rôles dans Exchange Online, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) et [modifier les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-147">For more information about role groups in Exchange Online, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) and [Modify role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups).</span></span>

- <span data-ttu-id="7a4cc-148">Chaque organisation a une stratégie par défaut nommée OwaMailboxPolicy-default, mais vous pouvez créer des stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-148">Every organization has a default policy named OwaMailboxPolicy-Default, but you can create custom policies.</span></span> <span data-ttu-id="7a4cc-149">Les stratégies personnalisées sont appliquées aux utilisateurs délimités avant la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-149">Custom policies are applied to scoped users before the default policy.</span></span> <span data-ttu-id="7a4cc-150">Pour plus d’informations sur les stratégies de boîte aux lettres Outlook sur le Web, consultez [la rubrique relative aux stratégies de boîte aux lettres Outlook sur le Web dans Exchange Online](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-150">For more information about Outlook on the web mailbox policies, see [Outlook on the web mailbox policies in Exchange Online](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span></span>

- <span data-ttu-id="7a4cc-151">La désactivation de la création de rapports de courrier indésirable ne supprime pas la possibilité de marquer un message comme indésirable ou légitime dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-151">Disabling junk email reporting doesn't remove the ability to mark a message as junk or not junk in Outlook on the web.</span></span> <span data-ttu-id="7a4cc-152">Si vous sélectionnez un message dans le dossier courrier indésirable et que vous cliquez sur **légitime** , le \>  message est renvoyé dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-152">Selecting a message in the Junk email folder and clicking **Not junk** \> **Not junk** still moves the message back into the Inbox.</span></span> <span data-ttu-id="7a4cc-153">Le fait de sélectionner un message dans un autre dossier de messagerie et **de cliquer sur courrier** indésirable \>  déplace le message dans le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-153">Selecting a message in any other email folder and clicking **Junk** \> **Junk** still moves the message into the Junk Email folder.</span></span> <span data-ttu-id="7a4cc-154">Ce qui n’est plus disponible est la possibilité de signaler le message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-154">What's no longer available is the option to report the message to Microsoft.</span></span>

### <a name="use-exchange-online-powershell-to-disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="7a4cc-155">Utiliser Exchange Online PowerShell pour désactiver ou activer la création de rapports de courrier indésirable dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="7a4cc-155">Use Exchange Online PowerShell to disable or enable junk email reporting in Outlook on the web</span></span>

1. <span data-ttu-id="7a4cc-156">Pour rechercher vos stratégies de boîte aux lettres Outlook sur le Web et l’état de la création de rapports de courrier indésirable, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-156">To find your existing Outlook on the web mailbox policies and the status of junk email reporting, run the following command:</span></span>

   ```powershell
   Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
   ```

2. <span data-ttu-id="7a4cc-157">Pour désactiver ou activer la création de rapports de courrier indésirable dans Outlook sur le Web, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-157">To disable or enable junk email reporting in Outlook on the web, use the following syntax:</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
   ```

   <span data-ttu-id="7a4cc-158">Cet exemple désactive la création de rapports de courrier indésirable dans la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-158">This example disables junk email reporting in the default policy.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
   ```

   <span data-ttu-id="7a4cc-159">Cet exemple active la création de rapports de courrier indésirable dans la stratégie personnalisée nommée Contoso managers.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-159">This example enables junk email reporting in the custom policy named Contoso Managers.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "Contoso Managers" -ReportJunkEmailEnabled $true
   ```

<span data-ttu-id="7a4cc-160">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) et [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="7a4cc-160">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) and [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="7a4cc-161">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="7a4cc-161">How do you know this worked?</span></span>

<span data-ttu-id="7a4cc-162">Pour vérifier que vous avez bien activé ou désactivé la création de rapports de courrier indésirable dans Outlook sur le Web, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-162">To verify that you've successfully enabled or disabled junk email reporting in Outlook on the web, use any of the following steps:</span></span>

- <span data-ttu-id="7a4cc-163">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez la valeur de la propriété **ReportJunkEmailEnabled** :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-163">In Exchange Online PowerShell, run the following command and verify the **ReportJunkEmailEnabled** property value:</span></span>

  ```powershell
  Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
  ```

- <span data-ttu-id="7a4cc-164">Ouvrez la boîte aux lettres d’un utilisateur concerné dans Outlook sur le Web, sélectionnez un message dans la boîte de réception **, cliquez sur** \> **courrier indésirable** et vérifiez que l’invite de signalement du message à Microsoft est ou non affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7a4cc-164">Open an affected user's mailbox in Outlook on the web, select a message in the Inbox, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

- <span data-ttu-id="7a4cc-165">Ouvrez la boîte aux lettres d’un utilisateur concerné dans Outlook sur le Web, sélectionnez un message dans le dossier courrier indésirable **, cliquez sur courrier indésirable** \>  et vérifiez que l’invite de signalement du message à Microsoft est ou non affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="7a4cc-165">Open an affected user's mailbox in Outlook on the web, select a message in the Junk Email folder, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

<span data-ttu-id="7a4cc-166"><sup>\*</sup> Les utilisateurs peuvent masquer l’invite de signalement du message tout en continuant à signaler le message.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-166"><sup>\*</sup> Users can hide the prompt to report the message while still reporting the message.</span></span> <span data-ttu-id="7a4cc-167">Pour vérifier ce paramètre dans Outlook sur le Web, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7a4cc-167">To check this setting in Outlook on the web:</span></span>

1. <span data-ttu-id="7a4cc-168">Cliquez sur **paramètres** ![ Outlook sur l’icône Paramètres du site Web ](../../media/owa-settings-icon.png) \> **Afficher tous les paramètres Outlook** \> **courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-168">Click **Settings** ![Outlook on the web settings icon](../../media/owa-settings-icon.png) \> **View all Outlook settings** \> **Junk email**.</span></span>
2. <span data-ttu-id="7a4cc-169">Dans la section **création de rapports** , vérifiez la valeur : **me demander avant d’envoyer un rapport**.</span><span class="sxs-lookup"><span data-stu-id="7a4cc-169">In the **Reporting** section, verify the value: **Ask me before sending a report**.</span></span>

   ![Paramètres Outlook sur le courrier indésirable pour le courrier indésirable](../../media/owa-junk-email-reporting-options.png)
