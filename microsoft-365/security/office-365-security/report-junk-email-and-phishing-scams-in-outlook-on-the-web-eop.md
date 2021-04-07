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
ms.openlocfilehash: 933387dd32a6c1ca1e27ee11e4a9384615e8fdec
ms.sourcegitcommit: 0ff6edbf52562138a69c6675cb0274ec984986c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "51615209"
---
# <a name="report-junk-and-phishing-email-in-outlook-on-the-web-in-exchange-online"></a><span data-ttu-id="a2e8b-103">Signaler le courrier indésirable et le hameçonnage dans Outlook sur le web dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a2e8b-103">Report junk and phishing email in Outlook on the web in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a2e8b-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a2e8b-104">**Applies to**</span></span>
- [<span data-ttu-id="a2e8b-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="a2e8b-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="a2e8b-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="a2e8b-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="a2e8b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a2e8b-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="a2e8b-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne [hybride,](../../enterprise/hybrid-modern-auth-overview.md)vous pouvez envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="a2e8b-108">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](../../enterprise/hybrid-modern-auth-overview.md), you can submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a2e8b-109">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a2e8b-109">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a2e8b-110">Pour une expérience de soumission d’utilisateurs de premier choix, nous vous recommandons d’utiliser les add-ins Message de rapport et Hameçonnage de rapport. Pour [plus d’informations,](./enable-the-report-message-add-in.md) voir Activer le add-in Message de rapport et Activer le module [de](./enable-the-report-phish-add-in.md) signalement de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-110">For the best user submission experience we recommend using the Report Message and the Report Phishing add-ins. See [Enable the Report Message add-in](./enable-the-report-message-add-in.md) and [Enable the Report Phishing add-in](./enable-the-report-phish-add-in.md) for more information.</span></span>

- <span data-ttu-id="a2e8b-111">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-111">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="a2e8b-112">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-112">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="a2e8b-113">Les administrateurs peuvent désactiver ou activer la possibilité pour les utilisateurs de signaler des messages à Microsoft dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-113">Admins can disable or enable the ability for users to report messages to Microsoft in Outlook on the web.</span></span> <span data-ttu-id="a2e8b-114">Pour plus d’informations, voir la section Désactiver ou activer le signalement du courrier indésirable [dans Outlook sur](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) le web plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-114">For details, see the [Disable or enable junk email reporting in Outlook on the web](#disable-or-enable-junk-email-reporting-in-outlook-on-the-web) section later in this article.</span></span>

- <span data-ttu-id="a2e8b-115">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-115">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="a2e8b-116">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-116">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="a2e8b-117">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-117">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="a2e8b-118">Désactiver ou activer les rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="a2e8b-118">Disable or enable junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="a2e8b-119">Par défaut, les utilisateurs peuvent signaler à Microsoft des faux positifs de courrier indésirable, des faux négatifs et des messages de hameçonnage pour analyse dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-119">By default, users can report spam false positives, false negatives, and phishing messages to Microsoft for analysis in Outlook on the web.</span></span> <span data-ttu-id="a2e8b-120">Les administrateurs peuvent configurer des stratégies de boîte aux lettres Outlook sur le web dans Exchange Online PowerShell pour empêcher les utilisateurs de signaler des faux positifs et des faux négatifs de courrier indésirable à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-120">Admins can configure Outlook on the web mailbox policies in Exchange Online PowerShell to prevent users from reporting spam false positives and spam false negatives to Microsoft.</span></span> <span data-ttu-id="a2e8b-121">Vous ne pouvez pas désactiver la possibilité pour les utilisateurs de signaler des messages de hameçonnage à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-121">You can't disable the ability for users to report phishing messages to Microsoft.</span></span>

### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a2e8b-122">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a2e8b-122">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a2e8b-123">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="a2e8b-123">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

- <span data-ttu-id="a2e8b-124">Des autorisations doivent vous être attribuées dans Exchange Online avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-124">You need to be assigned permissions in Exchange Online before you can do the procedures in this article.</span></span> <span data-ttu-id="a2e8b-125">Plus précisément,  vous avez besoin des **rôles Stratégies** des  destinataires ou Destinataires de messagerie, qui sont attribués par défaut aux groupes de rôles Gestion de l’organisation et Gestion des destinataires. </span><span class="sxs-lookup"><span data-stu-id="a2e8b-125">Specifically you need the **Recipient Policies** or **Mail Recipients** roles, which are assigned to the **Organization Management** and **Recipient Management** role groups by default.</span></span> <span data-ttu-id="a2e8b-126">Pour plus d’informations sur les groupes de rôles dans Exchange Online, voir [Autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo) et Modifier des groupes de [rôles dans Exchange Online.](/Exchange/permissions-exo/role-groups#modify-role-groups)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-126">For more information about role groups in Exchange Online, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo) and [Modify role groups in Exchange Online](/Exchange/permissions-exo/role-groups#modify-role-groups).</span></span>

- <span data-ttu-id="a2e8b-127">Chaque organisation possède une stratégie par défaut nommée OwaMailboxPolicy-Default, mais vous pouvez créer des stratégies personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-127">Every organization has a default policy named OwaMailboxPolicy-Default, but you can create custom policies.</span></span> <span data-ttu-id="a2e8b-128">Les stratégies personnalisées sont appliquées aux utilisateurs d’étendue avant la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-128">Custom policies are applied to scoped users before the default policy.</span></span> <span data-ttu-id="a2e8b-129">Pour plus d’informations sur les stratégies de boîte aux lettres Outlook sur le web, consultez stratégies de boîte aux lettres [Outlook sur le web dans Exchange Online.](/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies)</span><span class="sxs-lookup"><span data-stu-id="a2e8b-129">For more information about Outlook on the web mailbox policies, see [Outlook on the web mailbox policies in Exchange Online](/Exchange/clients-and-mobile-in-exchange-online/outlook-on-the-web/outlook-web-app-mailbox-policies).</span></span>

- <span data-ttu-id="a2e8b-130">La désactivation de la signalement du courrier indésirable ne supprime pas la possibilité de marquer un message comme courrier indésirable ou non indésirable dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-130">Disabling junk email reporting doesn't remove the ability to mark a message as junk or not junk in Outlook on the web.</span></span> <span data-ttu-id="a2e8b-131">La sélection d’un message dans  le dossier Courrier indésirable et le fait de cliquer sur Ne pas courrier indésirable déplace toujours le \>  message dans la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-131">Selecting a message in the Junk email folder and clicking **Not junk** \> **Not junk** still moves the message back into the Inbox.</span></span> <span data-ttu-id="a2e8b-132">La sélection d’un message dans  un autre dossier de courrier électronique et le fait de cliquer sur Courrier indésirable déplace toujours le message dans le \>  dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-132">Selecting a message in any other email folder and clicking **Junk** \> **Junk** still moves the message into the Junk Email folder.</span></span> <span data-ttu-id="a2e8b-133">Ce qui n’est plus disponible, c’est la possibilité de signaler le message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-133">What's no longer available is the option to report the message to Microsoft.</span></span>

### <a name="use-exchange-online-powershell-to-disable-or-enable-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="a2e8b-134">Utiliser Exchange Online PowerShell pour désactiver ou activer la signalement du courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="a2e8b-134">Use Exchange Online PowerShell to disable or enable junk email reporting in Outlook on the web</span></span>

1. <span data-ttu-id="a2e8b-135">Pour rechercher vos stratégies de boîte aux lettres Outlook sur le web existantes et l’état des rapports de courrier indésirable, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a2e8b-135">To find your existing Outlook on the web mailbox policies and the status of junk email reporting, run the following command:</span></span>

   ```powershell
   Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
   ```

2. <span data-ttu-id="a2e8b-136">Pour désactiver ou activer la signalement du courrier indésirable dans Outlook sur le web, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a2e8b-136">To disable or enable junk email reporting in Outlook on the web, use the following syntax:</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
   ```

   <span data-ttu-id="a2e8b-137">Cet exemple désactive le signalement du courrier indésirable dans la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-137">This example disables junk email reporting in the default policy.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
   ```

   <span data-ttu-id="a2e8b-138">Cet exemple active la création de rapports de courrier indésirable dans la stratégie personnalisée nommée Responsables Contoso.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-138">This example enables junk email reporting in the custom policy named Contoso Managers.</span></span>

   ```powershell
   Set-OwaMailboxPolicy -Identity "Contoso Managers" -ReportJunkEmailEnabled $true
   ```

<span data-ttu-id="a2e8b-139">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](/powershell/module/exchange/get-owamailboxpolicy) et [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span><span class="sxs-lookup"><span data-stu-id="a2e8b-139">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](/powershell/module/exchange/get-owamailboxpolicy) and [Set-OwaMailboxPolicy](/powershell/module/exchange/set-owamailboxpolicy).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="a2e8b-140">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="a2e8b-140">How do you know this worked?</span></span>

<span data-ttu-id="a2e8b-141">Pour vérifier que vous avez bien activé ou désactivé le signalement du courrier indésirable dans Outlook sur le web, utilisez l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2e8b-141">To verify that you've successfully enabled or disabled junk email reporting in Outlook on the web, use any of the following steps:</span></span>

- <span data-ttu-id="a2e8b-142">Dans Exchange Online PowerShell, exécutez la commande suivante et vérifiez la valeur de la propriété **ReportJunkEmailEnabled** :</span><span class="sxs-lookup"><span data-stu-id="a2e8b-142">In Exchange Online PowerShell, run the following command and verify the **ReportJunkEmailEnabled** property value:</span></span>

  ```powershell
  Get-OwaMailboxPolicy | Format-Table Name,ReportJunkEmailEnabled
  ```

- <span data-ttu-id="a2e8b-143">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans la boîte de réception, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est \>  pas affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a2e8b-143">Open an affected user's mailbox in Outlook on the web, select a message in the Inbox, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

- <span data-ttu-id="a2e8b-144">Ouvrez la boîte aux lettres d’un utilisateur affecté dans Outlook  sur le web, sélectionnez un message dans le dossier Courrier indésirable, cliquez sur Courrier indésirable et vérifiez que l’invite de signalement du message à Microsoft est ou n’est pas \>  affichée.<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="a2e8b-144">Open an affected user's mailbox in Outlook on the web, select a message in the Junk Email folder, click **Junk** \> **Junk** and verify the prompt to report the message to Microsoft is or is not displayed.<sup>\*</sup></span></span>

<span data-ttu-id="a2e8b-145"><sup>\*</sup> Les utilisateurs peuvent masquer l’invite de signalement du message tout en le signalant.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-145"><sup>\*</sup> Users can hide the prompt to report the message while still reporting the message.</span></span> <span data-ttu-id="a2e8b-146">Pour vérifier ce paramètre dans Outlook sur le web :</span><span class="sxs-lookup"><span data-stu-id="a2e8b-146">To check this setting in Outlook on the web:</span></span>

1. <span data-ttu-id="a2e8b-147">Cliquez **sur Paramètres** ![ d’Outlook sur le web icône Afficher tous les ](../../media/owa-settings-icon.png) \> **paramètres Outlook Courrier** \> **indésirable**.</span><span class="sxs-lookup"><span data-stu-id="a2e8b-147">Click **Settings** ![Outlook on the web settings icon](../../media/owa-settings-icon.png) \> **View all Outlook settings** \> **Junk email**.</span></span>
2. <span data-ttu-id="a2e8b-148">Dans la section **Création de** rapports, vérifiez la valeur : **Demandez-moi avant d’envoyer un rapport.**</span><span class="sxs-lookup"><span data-stu-id="a2e8b-148">In the **Reporting** section, verify the value: **Ask me before sending a report**.</span></span>

   ![Paramètres de création de rapports de courrier indésirable Outlook sur le web](../../media/owa-junk-email-reporting-options.png)