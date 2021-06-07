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
ms.openlocfilehash: 1139871f5929ff9fef29e980b7614e5bc7b92570
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52788306"
---
# <a name="report-junk-and-phishing-email-in-outlook-on-the-web-in-exchange-online"></a><span data-ttu-id="06c87-103">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="06c87-103">Report junk and phishing email in Outlook on the web in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="06c87-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="06c87-104">**Applies to**</span></span>
- [<span data-ttu-id="06c87-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="06c87-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="06c87-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="06c87-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="06c87-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="06c87-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="06c87-108">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne [hybride,](../../enterprise/hybrid-modern-auth-overview.md)vous pouvez envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="06c87-108">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](../../enterprise/hybrid-modern-auth-overview.md), you can submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="06c87-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="06c87-109">What do you need to know before you begin?</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06c87-110">Nous recommandons le module de signalement du message ou le module de signalement du hameçonnage pour les soumissions d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="06c87-110">We recommend the Report Message add-in or the Report Phishing add-in for user submissions.</span></span> <span data-ttu-id="06c87-111">Pour plus d’informations, voir [Enable the Report Message or the Report Phishing add-ins](./enable-the-report-message-add-in.md). Nous vous déconseillons d’utiliser l’expérience de rapport intégrée dans Outlook car elle ne peut pas utiliser la stratégie de [soumission d’utilisateur.](./user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="06c87-111">For more information, see [Enable the Report Message or the Report Phishing add-ins](./enable-the-report-message-add-in.md). We don't recommend the built-in reporting experience in Outlook because it can't use the [user submission policy](./user-submission.md).</span></span>

- <span data-ttu-id="06c87-112">Si vous êtes un administrateur d’une organisation Exchange Online boîtes aux lettres, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="06c87-112">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="06c87-113">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="06c87-113">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="06c87-114">Les administrateurs peuvent désactiver ou activer la possibilité pour les utilisateurs de signaler des messages à Microsoft Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="06c87-114">Admins can disable or enable the ability for users to report messages to Microsoft in Outlook on the web.</span></span> <span data-ttu-id="06c87-115">Pour plus d’informations, voir la section Désactiver ou activer le signalement du courrier indésirable Outlook sur [le web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="06c87-115">For details, see the [Disable or enable junk email reporting in Outlook on the web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) section later in this article.</span></span>

- <span data-ttu-id="06c87-116">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="06c87-116">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="06c87-117">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="06c87-117">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="06c87-118">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="06c87-118">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="06c87-119">Désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="06c87-119">Disable or enable junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="06c87-120">Par défaut, les utilisateurs peuvent signaler à Microsoft des faux positifs de courrier indésirable, des faux négatifs et des messages de hameçonnage pour analyse dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="06c87-120">By default, users can report spam false positives, false negatives, and phishing messages to Microsoft for analysis in Outlook on the web.</span></span> <span data-ttu-id="06c87-121">Les administrateurs peuvent configurer Outlook stratégies de boîte aux lettres web dans Exchange Online PowerShell pour empêcher les utilisateurs de signaler des faux positifs et des faux négatifs de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06c87-121">Admins can configure Outlook on the web mailbox policies in Exchange Online PowerShell to prevent users from reporting spam false positives and spam false negatives to Microsoft.</span></span> <span data-ttu-id="06c87-122">Vous ne pouvez pas désactiver la possibilité pour les utilisateurs de signaler des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06c87-122">You can't disable the ability for users to report phishing messages to Microsoft.</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="06c87-123">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="06c87-123">What do you need to know before you begin?</span></span>

- <span data-ttu-id="06c87-124">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="06c87-124">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="06c87-125">Des autorisations doivent vous être attribuées Exchange Online avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="06c87-125">You need to be assigned permissions in Exchange Online before you can do the procedures in this article.</span></span> <span data-ttu-id="06c87-126">Plus précisément,  vous avez besoin des **rôles Stratégies** des  destinataires ou Destinataires de messagerie, qui sont attribués par défaut aux groupes de rôles Gestion de l’organisation et Gestion des destinataires. </span><span class="sxs-lookup"><span data-stu-id="06c87-126">Specifically you need the **Recipient Policies** or **Mail Recipients** roles, which are assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="06c87-127">Pour plus d’informations sur les groupes de rôles dans Exchange Online, voir [Autorisations](/exchange/permissions-exo/permissions-exo) dans Exchange Online et Modifier les groupes de rôles [dans Exchange Online](/Exchange/permissions-exo/role-groups#modify-role-groups).</span><span class="sxs-lookup"><span data-stu-id="06c87-127">For more information about role groups in Exchange Online, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo) and [Modify role groups in Exchange Online](/Exchange/permissions-exo/role-groups#modify-role-groups).</span></span>

- <span data-ttu-id="06c87-128">Chaque organisation possède une stratégie par défaut nommée OwaMailboxPolicy-Default, mais vous pouvez créer des stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="06c87-128">Every organization has a default policy named OwaMailboxPolicy-Default, but you can create custom policies.</span></span> <span data-ttu-id="06c87-129">Les stratégies personnalisées sont appliquées aux utilisateurs d’étendue avant la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="06c87-129">Custom policies are applied to scoped users before the default policy.</span></span> <span data-ttu-id="06c87-130">Pour plus d’informations Outlook sur les stratégies de boîte aux lettres web, voir Outlook [stratégies](/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies)de boîte aux lettres web dans Exchange Online .</span><span class="sxs-lookup"><span data-stu-id="06c87-130">For more information about Outlook on the web mailbox policies, see [Outlook on the web mailbox policies in Exchange Online](/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span></span>

- <span data-ttu-id="06c87-131">La désactivation de la signalement du courrier indésirable ne supprime pas la possibilité de marquer un message comme courrier indésirable ou non indésirable dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="06c87-131">Disabling junk email reporting doesn't remove the ability to mark a message as junk or not junk in Outlook on the web.</span></span> <span data-ttu-id="06c87-132">La sélection d’un message dans  le dossier Courrier indésirable et le fait de cliquer sur Ne pas courrier indésirable déplace toujours le \>  message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="06c87-132">Selecting a message in the Junk email folder and clicking **Not junk** \> **Not junk** still moves the message back into the Inbox.</span></span> <span data-ttu-id="06c87-133">La sélection d’un message dans  un autre dossier de courrier électronique et le fait de cliquer sur Courrier indésirable déplace toujours le message dans le \>  dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="06c87-133">Selecting a message in any other email folder and clicking **Junk** \> **Junk** still moves the message into the Junk Email folder.</span></span> <span data-ttu-id="06c87-134">Ce qui n’est plus disponible, c’est la possibilité de signaler le message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06c87-134">What's no longer available is the option to report the message to Microsoft.</span></span>

### <a name="use-exchange-online-powershell-to-disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="06c87-135">Utiliser Exchange Online PowerShell pour désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="06c87-135">Use Exchange Online PowerShell to disable or enable junk email reporting in Outlook on the web</span></span>

1. <span data-ttu-id="06c87-136">Pour rechercher vos stratégies de boîte aux lettres Outlook sur le web et l’état du signalement du courrier indésirable, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="06c87-136">To find your existing Outlook on the web mailbox policies and the status of junk email reporting, run the following command:</span></span>

   ```powershell
   Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
   ```

2. <span data-ttu-id="06c87-137">Pour désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="06c87-137">To disable or enable junk email reporting in Outlook on the web, use the following syntax:</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
   ```

   <span data-ttu-id="06c87-138">Cet exemple désactive le signalement du courrier indésirable dans la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="06c87-138">This example disables junk email reporting in the default policy.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
   ```

   <span data-ttu-id="06c87-139">Cet exemple active la création de rapports de courrier indésirable dans la stratégie personnalisée nommée Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="06c87-139">This example enables junk email reporting in the custom policy named Contoso Managers.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "Contoso Managers" -ReportJunkEmailEnabled $true
   ```

<span data-ttu-id="06c87-140">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](/powershell/module/exchange/get-owamailboxpolicy) et [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="06c87-140">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](/powershell/module/exchange/get-owamailboxpolicy) and [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="06c87-141">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="06c87-141">How do you know this worked?</span></span>

<span data-ttu-id="06c87-142">Pour vérifier que vous avez bien activé ou désactivé le signalement du courrier indésirable dans Outlook sur le web, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="06c87-142">To verify that you've successfully enabled or disabled junk email reporting in Outlook on the web, use any of the following steps:</span></span>

- <span data-ttu-id="06c87-143">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez la valeur de la propriété **ReportJunkEmailEnabled** :</span><span class="sxs-lookup"><span data-stu-id="06c87-143">In Exchange Online PowerShell, run the following command and verify the **ReportJunkEmailEnabled** property value:</span></span>

  ```powershell
  Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
  ```

- <span data-ttu-id="06c87-144">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook sur  le web, sélectionnez un message dans la boîte de réception, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft s’affiche ou \>  non.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="06c87-144">Open an affected user's mailbox in Outlook on the web, select a message in the Inbox, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

- <span data-ttu-id="06c87-145">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook sur le  web, sélectionnez un message dans le dossier Courrier indésirable, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft s’affiche ou \>  non.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="06c87-145">Open an affected user's mailbox in Outlook on the web, select a message in the Junk Email folder, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

<span data-ttu-id="06c87-146"><sup>\*</sup> Les utilisateurs peuvent masquer l’invite de signalement du message tout en le signalant.</span><span class="sxs-lookup"><span data-stu-id="06c87-146"><sup>\*</sup> Users can hide the prompt to report the message while still reporting the message.</span></span> <span data-ttu-id="06c87-147">Pour vérifier ce paramètre dans Outlook sur le web :</span><span class="sxs-lookup"><span data-stu-id="06c87-147">To check this setting in Outlook on the web:</span></span>

1. <span data-ttu-id="06c87-148">Cliquez **Paramètres** Outlook sur l’icône paramètres web Afficher tous ![ les ](../../media/owa-settings-icon.png) \> **paramètres Outlook courrier** \> **indésirable.**</span><span class="sxs-lookup"><span data-stu-id="06c87-148">Click **Settings** ![Outlook on the web settings icon](../../media/owa-settings-icon.png) \> **View all Outlook settings** \> **Junk email**.</span></span>
2. <span data-ttu-id="06c87-149">Dans la section **Création de** rapports, vérifiez la valeur : **Demandez-moi avant d’envoyer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="06c87-149">In the **Reporting** section, verify the value: **Ask me before sending a report**.</span></span>

   ![Outlook de création de rapports de courrier indésirable sur le web](../../media/owa-junk-email-reporting-options.png)
