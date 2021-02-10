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
description: Les administrateurs peuvent en savoir plus sur les options intégrées de signalement du courrier indésirable, non indésirable et du hameçonnage dans Outlook sur le web (Outlook Web App) dans Exchange Online, et comment désactiver ces options de rapport pour les utilisateurs.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: bd22e7f08ae420adf2923d4da731494a0f6af3e3
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166734"
---
# <a name="report-junk-and-phishing-email-in-outlook-on-the-web-in-exchange-online"></a><span data-ttu-id="8891a-103">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8891a-103">Report junk and phishing email in Outlook on the web in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8891a-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8891a-104">**Applies to**</span></span>
- [<span data-ttu-id="8891a-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8891a-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="8891a-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="8891a-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="8891a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8891a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="8891a-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online, vous pouvez utiliser les options de rapport intégrées dans Outlook sur le web (anciennement Outlook Web App) pour envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="8891a-108">In Microsoft 365 organizations with mailboxes in Exchange Online, you can use the built-in reporting options in Outlook on the web (formerly known as Outlook Web App) to submit false positives (good email marked as spam), false negatives (bad email allowed) and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8891a-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8891a-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8891a-110">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="8891a-110">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="8891a-111">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="8891a-111">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="8891a-112">Les administrateurs peuvent désactiver ou activer la possibilité pour les utilisateurs de signaler des messages à Microsoft dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="8891a-112">Admins can disable or enable the ability for users to report messages to Microsoft in Outlook on the web.</span></span> <span data-ttu-id="8891a-113">Pour plus d’informations, voir la section Désactiver ou activer la signalement du courrier indésirable [dans Outlook sur](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) le web plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="8891a-113">For details, see the [Disable or enable junk email reporting in Outlook on the web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) section later in this article.</span></span>

- <span data-ttu-id="8891a-114">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="8891a-114">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="8891a-115">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="8891a-115">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="8891a-116">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="8891a-116">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-on-the-web"></a><span data-ttu-id="8891a-117">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="8891a-117">Report spam and phishing messages in Outlook on the web</span></span>

1. <span data-ttu-id="8891a-118">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez l’une des méthodes suivantes pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="8891a-118">For messages in the Inbox or any other email folder except Junk Email, use either of the following methods to report spam and phishing messages:</span></span>

   - <span data-ttu-id="8891a-119">Sélectionnez le message, cliquez **sur Courrier** indésirable dans la barre d’outils, puis **sélectionnez** Courrier indésirable ou **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="8891a-119">Select the message, click **Junk** on the toolbar, and then select **Junk** or **Phishing**.</span></span>

     ![Signaler le courrier indésirable ou le hameçonnage à partir du ruban](../../media/owa-report-junk.png)

   - <span data-ttu-id="8891a-121">Sélectionnez un ou plusieurs messages, cliquez avec le bouton droit, puis **sélectionnez Marquer comme courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="8891a-121">Select one or more messages, right-click, and then select **Mark as junk**.</span></span>

2. <span data-ttu-id="8891a-122">Dans la boîte de dialogue qui s’affiche, cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="8891a-122">In the dialog that appears, click **Report**.</span></span> <span data-ttu-id="8891a-123">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="8891a-123">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="8891a-124">Courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8891a-124">Junk</span></span>|<span data-ttu-id="8891a-125">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8891a-125">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue Signaler comme courrier indésirable](../../media/owa-report-as-junk-dialog.png)|![Boîte de dialogue Signaler comme hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="8891a-128">Les messages sélectionnés sont envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="8891a-128">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="8891a-129">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="8891a-129">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="report-non-spam-and-phishing-messages-from-the-junk-email-folder-in-outlook-on-the-web"></a><span data-ttu-id="8891a-130">Signaler les messages de courrier non indésirable et de hameçonnage à partir du dossier Courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="8891a-130">Report non-spam and phishing messages from the Junk Email folder in Outlook on the web</span></span>

1. <span data-ttu-id="8891a-131">Dans le dossier Courrier indésirable, utilisez l’une des méthodes suivantes pour signaler les faux positifs du courrier indésirable ou les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="8891a-131">In the Junk Email folder, use either of the following methods to report spam false positives or phishing messages:</span></span>

   - <span data-ttu-id="8891a-132">Sélectionnez le message, cliquez **sur Ne** pas courrier indésirable dans la barre d’outils, puis sélectionnez Ne pas être indésirable **ou** **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="8891a-132">Select the message, click **Not Junk** on the toolbar, and then select **Not Junk** or **Phishing**.</span></span>

     ![Signaler le courrier électronique non indésirable ou non de hameçonnage à partir du ruban](../../media/owa-report-not-junk.png)

   - <span data-ttu-id="8891a-134">Sélectionnez un ou plusieurs messages, cliquez avec le bouton droit, puis **sélectionnez Marquer comme courrier indésirable.**</span><span class="sxs-lookup"><span data-stu-id="8891a-134">Select one or more messages, right-click, and then select **Mark as not junk**.</span></span>

2. <span data-ttu-id="8891a-135">Dans la boîte de dialogue qui s’affiche, lisez les informations et cliquez sur **Rapport.**</span><span class="sxs-lookup"><span data-stu-id="8891a-135">In the dialog that appears, read the information and click **Report**.</span></span> <span data-ttu-id="8891a-136">Si vous changez d’avis, cliquez sur **Ne pas signaler.**</span><span class="sxs-lookup"><span data-stu-id="8891a-136">If you change your mind, click **Don't Report**.</span></span>

   |<span data-ttu-id="8891a-137">Non indésirable</span><span class="sxs-lookup"><span data-stu-id="8891a-137">Not Junk</span></span>|<span data-ttu-id="8891a-138">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="8891a-138">Phishing</span></span>|
   |:---:|:---:|
   |![Boîte de dialogue Signaler comme courrier indésirable](../../media/owa-report-as-not-junk-dialog.png)|![Boîte de dialogue Signaler comme hameçonnage](../../media/owa-report-as-phishing-dialog.png)|

3. <span data-ttu-id="8891a-141">Les messages sélectionnés sont envoyés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="8891a-141">The selected messages will be sent to Microsoft for analysis.</span></span> <span data-ttu-id="8891a-142">Pour confirmer que les messages ont été envoyés, ouvrez le dossier **Éléments envoyés** pour afficher les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="8891a-142">To confirm that the messages have been submitted, open your **Sent Items** folder to view the submitted messages.</span></span>

## <a name="disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="8891a-143">Désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="8891a-143">Disable or enable junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="8891a-144">Par défaut, les utilisateurs peuvent signaler des faux positifs, des faux négatifs et des messages de hameçonnage à Microsoft pour analyse dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="8891a-144">By default, users can report spam false positives, false negatives, and phishing messages to Microsoft for analysis in Outlook on the web.</span></span> <span data-ttu-id="8891a-145">Les administrateurs peuvent configurer des stratégies de boîte aux lettres Outlook sur le web dans Exchange Online PowerShell pour empêcher les utilisateurs de signaler des faux positifs et des faux négatifs de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8891a-145">Admins can configure Outlook on the web mailbox policies in Exchange Online PowerShell to prevent users from reporting spam false positives and spam false negatives to Microsoft.</span></span> <span data-ttu-id="8891a-146">Vous ne pouvez pas désactiver la possibilité pour les utilisateurs de signaler des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8891a-146">You can't disable the ability for users to report phishing messages to Microsoft.</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8891a-147">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="8891a-147">What do you need to know before you begin?</span></span>

- <span data-ttu-id="8891a-148">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="8891a-148">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="8891a-149">Des autorisations doivent vous être attribuées dans Exchange Online avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="8891a-149">You need to be assigned permissions in Exchange Online before you can do the procedures in this article.</span></span> <span data-ttu-id="8891a-150">Plus précisément,  vous avez besoin des **rôles Stratégies** des  destinataires ou Destinataires de messagerie, qui sont attribués par défaut aux groupes de rôles Gestion de l’organisation et Gestion des destinataires. </span><span class="sxs-lookup"><span data-stu-id="8891a-150">Specifically you need the **Recipient Policies** or **Mail Recipients** roles, which are assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="8891a-151">Pour plus d’informations sur les groupes de rôles dans Exchange Online, voir [Autorisations dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) et Modifier des groupes de [rôles dans Exchange Online.](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups)</span><span class="sxs-lookup"><span data-stu-id="8891a-151">For more information about role groups in Exchange Online, see [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo) and [Modify role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups).</span></span>

- <span data-ttu-id="8891a-152">Chaque organisation possède une stratégie par défaut nommée OwaMailboxPolicy-Default, mais vous pouvez créer des stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8891a-152">Every organization has a default policy named OwaMailboxPolicy-Default, but you can create custom policies.</span></span> <span data-ttu-id="8891a-153">Les stratégies personnalisées sont appliquées aux utilisateurs d’étendue avant la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="8891a-153">Custom policies are applied to scoped users before the default policy.</span></span> <span data-ttu-id="8891a-154">Pour plus d’informations sur les stratégies de boîte aux lettres Outlook sur le web, consultez stratégies de boîte aux lettres [Outlook sur le web dans Exchange Online.](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies)</span><span class="sxs-lookup"><span data-stu-id="8891a-154">For more information about Outlook on the web mailbox policies, see [Outlook on the web mailbox policies in Exchange Online](https://docs.microsoft.com/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span></span>

- <span data-ttu-id="8891a-155">La désactivation de la signalement du courrier indésirable ne supprime pas la possibilité de marquer un message comme courrier indésirable ou non indésirable dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="8891a-155">Disabling junk email reporting doesn't remove the ability to mark a message as junk or not junk in Outlook on the web.</span></span> <span data-ttu-id="8891a-156">La sélection d’un message dans  le dossier Courrier indésirable et le fait de cliquer sur Ne pas courrier indésirable déplace toujours le \>  message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="8891a-156">Selecting a message in the Junk email folder and clicking **Not junk** \> **Not junk** still moves the message back into the Inbox.</span></span> <span data-ttu-id="8891a-157">La sélection d’un message dans  un autre dossier de courrier électronique et le fait de cliquer sur Courrier indésirable déplace toujours le message dans le \>  dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="8891a-157">Selecting a message in any other email folder and clicking **Junk** \> **Junk** still moves the message into the Junk Email folder.</span></span> <span data-ttu-id="8891a-158">Ce qui n’est plus disponible, c’est la possibilité de signaler le message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8891a-158">What's no longer available is the option to report the message to Microsoft.</span></span>

### <a name="use-exchange-online-powershell-to-disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="8891a-159">Utiliser Exchange Online PowerShell pour désactiver ou activer la signalement du courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="8891a-159">Use Exchange Online PowerShell to disable or enable junk email reporting in Outlook on the web</span></span>

1. <span data-ttu-id="8891a-160">Pour rechercher vos stratégies de boîte aux lettres Outlook sur le web existantes et l’état des rapports de courrier indésirable, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8891a-160">To find your existing Outlook on the web mailbox policies and the status of junk email reporting, run the following command:</span></span>

   ```powershell
   Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
   ```

2. <span data-ttu-id="8891a-161">Pour désactiver ou activer la signalement du courrier indésirable dans Outlook sur le web, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="8891a-161">To disable or enable junk email reporting in Outlook on the web, use the following syntax:</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
   ```

   <span data-ttu-id="8891a-162">Cet exemple désactive le signalement du courrier indésirable dans la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="8891a-162">This example disables junk email reporting in the default policy.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
   ```

   <span data-ttu-id="8891a-163">Cet exemple active la création de rapports de courrier indésirable dans la stratégie personnalisée nommée Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="8891a-163">This example enables junk email reporting in the custom policy named Contoso Managers.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "Contoso Managers" -ReportJunkEmailEnabled $true
   ```

<span data-ttu-id="8891a-164">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) et [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="8891a-164">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/get-owamailboxpolicy) and [Set-OwaMailboxPolicy](https://docs.microsoft.com/powershell/module/exchange/set-owamailboxpolicy).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="8891a-165">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="8891a-165">How do you know this worked?</span></span>

<span data-ttu-id="8891a-166">Pour vérifier que vous avez bien activé ou désactivé le signalement du courrier indésirable dans Outlook sur le web, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8891a-166">To verify that you've successfully enabled or disabled junk email reporting in Outlook on the web, use any of the following steps:</span></span>

- <span data-ttu-id="8891a-167">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez la valeur de la propriété **ReportJunkEmailEnabled** :</span><span class="sxs-lookup"><span data-stu-id="8891a-167">In Exchange Online PowerShell, run the following command and verify the **ReportJunkEmailEnabled** property value:</span></span>

  ```powershell
  Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
  ```

- <span data-ttu-id="8891a-168">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans la boîte de réception, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est \>  pas affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8891a-168">Open an affected user's mailbox in Outlook on the web, select a message in the Inbox, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

- <span data-ttu-id="8891a-169">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans le dossier Courrier indésirable, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est pas \>  affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="8891a-169">Open an affected user's mailbox in Outlook on the web, select a message in the Junk Email folder, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

<span data-ttu-id="8891a-170"><sup>\*</sup> Les utilisateurs peuvent masquer l’invite de signalement du message tout en le signalant.</span><span class="sxs-lookup"><span data-stu-id="8891a-170"><sup>\*</sup> Users can hide the prompt to report the message while still reporting the message.</span></span> <span data-ttu-id="8891a-171">Pour vérifier ce paramètre dans Outlook sur le web :</span><span class="sxs-lookup"><span data-stu-id="8891a-171">To check this setting in Outlook on the web:</span></span>

1. <span data-ttu-id="8891a-172">Cliquez **sur l’icône Paramètres** ![ Outlook sur le web Icône Afficher tous les ](../../media/owa-settings-icon.png) \> **paramètres Outlook Courrier** \> **indésirable.**</span><span class="sxs-lookup"><span data-stu-id="8891a-172">Click **Settings** ![Outlook on the web settings icon](../../media/owa-settings-icon.png) \> **View all Outlook settings** \> **Junk email**.</span></span>
2. <span data-ttu-id="8891a-173">Dans la section **Création de** rapports, vérifiez la valeur : **Demandez-moi avant d’envoyer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="8891a-173">In the **Reporting** section, verify the value: **Ask me before sending a report**.</span></span>

   ![Paramètres de création de rapports de courrier indésirable Outlook sur le web](../../media/owa-junk-email-reporting-options.png)
