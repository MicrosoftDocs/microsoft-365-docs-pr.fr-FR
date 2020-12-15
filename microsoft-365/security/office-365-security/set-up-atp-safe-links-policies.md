---
title: Configurer des stratégies de liens fiables dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: how-to
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à afficher, créer, modifier et supprimer des stratégies de liens fiables et des paramètres globaux de liens fiables dans Microsoft Defender pour Office 365.
ms.openlocfilehash: 7a00b73855302f5046afa0605fd7188007394ed7
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49683162"
---
# <a name="set-up-safe-links-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="0407d-103">Configurer des stratégies de liens fiables dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="0407d-103">Set up Safe Links policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!IMPORTANT]
> <span data-ttu-id="0407d-104">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-104">This article is intended for business customers who have [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="0407d-105">Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur Safelinks dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="0407d-105">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="0407d-106">La fonctionnalité liens fiables est une fonctionnalité de [Microsoft Defender pour Office 365](office-365-atp.md) qui permet d’analyser les messages électroniques entrants dans le flux de messagerie et de cliquer sur vérification des URL et des liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="0407d-106">Safe Links is a feature in [Microsoft Defender for Office 365](office-365-atp.md) that provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="0407d-107">Pour plus d’informations, reportez-vous à [liens fiables dans Microsoft Defender pour Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-107">For more information, see [Safe Links in Microsoft Defender for Office 365](atp-safe-links.md).</span></span>

<span data-ttu-id="0407d-108">Il n’existe pas de stratégie de liens de sécurité intégrée ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="0407d-108">There's no built-in or default Safe Links policy.</span></span> <span data-ttu-id="0407d-109">Pour obtenir des liens fiables sur l’analyse des URL, vous devez créer une ou plusieurs stratégies de liens fiables, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0407d-109">To get Safe Links scanning of URLs, you need to create one or more Safe Links policies as described in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="0407d-110">Vous configurez les paramètres globaux pour la protection des liens fiables **en dehors** des stratégies de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-110">You configure the global settings for Safe Links protection **outside** of Safe Links policies.</span></span> <span data-ttu-id="0407d-111">Pour obtenir des instructions, consultez la rubrique [configure Global Settings for Safe Links in Microsoft Defender for Office 365](configure-global-settings-for-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-111">For instructions, see [Configure global settings for Safe Links in Microsoft Defender for Office 365](configure-global-settings-for-safe-links.md).</span></span>

<span data-ttu-id="0407d-112">Vous pouvez configurer des stratégies de liens fiables dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome EOP pour les organisations sans boîtes aux lettres Exchange Online, mais avec Microsoft Defender for Office 365 compléments d’abonnement).</span><span class="sxs-lookup"><span data-stu-id="0407d-112">You can configure Safe Links policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Microsoft Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="0407d-113">Les éléments de base d’une stratégie de liens fiables sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0407d-113">The basic elements of a Safe Links policy are:</span></span>

- <span data-ttu-id="0407d-114">**Stratégie de liens fiables**: activer la protection des liens fiables, activer l’analyse des URL en temps réel, spécifier s’il faut attendre la fin de l’analyse en temps réel avant de remettre le message, activer l’analyse des messages internes, spécifier s’il faut effectuer le suivi des clics des utilisateurs sur les URL et spécifier si les utilisateurs peuvent cliquer sur le bac à l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="0407d-114">**The safe links policy**: Turn on Safe Links protection, turn on real-time URL scanning, specify whether to wait for real-time scanning to complete before delivering the message, turn on scanning for internal messages, specify whether to track user clicks on URLs, and specify whether to allow users to click trough to the original URL.</span></span>
- <span data-ttu-id="0407d-115">**La règle de liens fiables**: spécifie la priorité et les filtres de destinataire (auxquels la stratégie s’applique).</span><span class="sxs-lookup"><span data-stu-id="0407d-115">**The safe links rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="0407d-116">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez des stratégies de liens fiables dans le centre de sécurité & Compliance Center :</span><span class="sxs-lookup"><span data-stu-id="0407d-116">The difference between these two elements isn't obvious when you manage Safe Links polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="0407d-117">Lorsque vous créez une stratégie de liens fiables, vous créez en réalité une règle de liens fiables et la stratégie de liens approuvés associée en même temps en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="0407d-117">When you create a Safe Links policy, you're actually creating a safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="0407d-118">Lorsque vous modifiez une stratégie de liens fiables, les paramètres associés aux filtres nom, priorité, activé ou désactivé et filtre de destinataires modifient la règle de liens approuvés.</span><span class="sxs-lookup"><span data-stu-id="0407d-118">When you modify a Safe Links policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe links rule.</span></span> <span data-ttu-id="0407d-119">Tous les autres paramètres modifient la stratégie de liens approuvés associée.</span><span class="sxs-lookup"><span data-stu-id="0407d-119">All other settings modify the associated safe links policy.</span></span>
- <span data-ttu-id="0407d-120">Lorsque vous supprimez une stratégie de liens fiables, la règle de liens fiables et la stratégie de liens approuvés associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="0407d-120">When you remove a Safe Links policy, the safe links rule and the associated safe links policy are removed.</span></span>

<span data-ttu-id="0407d-121">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="0407d-121">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="0407d-122">Pour plus d’informations, reportez-vous à la section [utiliser Exchange Online PowerShell or standalone EOP PowerShell pour configurer les stratégies de liens fiables](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0407d-122">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) section later in this article.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0407d-123">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0407d-123">What do you need to know before you begin?</span></span>

- <span data-ttu-id="0407d-124">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="0407d-124">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="0407d-125">Pour accéder directement à la page **liens approuvés** , utilisez <https://protection.office.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="0407d-125">To go directly to the **Safe Links** page, use <https://protection.office.com/safelinksv2>.</span></span>

- <span data-ttu-id="0407d-126">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="0407d-126">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="0407d-127">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="0407d-127">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="0407d-128">Pour pouvoir utiliser ce cmdlet, vous devez disposer des autorisations dans le centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="0407d-128">You need to be assigned permissions in the Security & Compliance Center before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="0407d-129">Pour créer, modifier et supprimer des stratégies de liens approuvés, vous devez être membre des groupes de rôles gestion de l' **organisation** ou **administrateur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="0407d-129">To create, modify, and delete Safe Links policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="0407d-130">Pour un accès en lecture seule aux stratégies de liens fiables, vous devez être membre des groupes de rôles **lecteur global** ou **lecteur de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="0407d-130">For read-only access to Safe Links policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="0407d-131">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-131">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

  <span data-ttu-id="0407d-132">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="0407d-132">**Notes**:</span></span>

  - <span data-ttu-id="0407d-133">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0407d-133">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="0407d-134">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="0407d-134">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  - <span data-ttu-id="0407d-135">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0407d-135">The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="0407d-136">Pour connaître les paramètres recommandés pour les stratégies de liens fiables, consultez la rubrique [Safe Links Policy Settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="0407d-136">For our recommended settings for Safe Links policies, see [Safe Links policy settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span></span>

- <span data-ttu-id="0407d-137">Autoriser jusqu’à 30 minutes pour l’application d’une stratégie nouvelle ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0407d-137">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="0407d-138">De [nouvelles fonctionnalités sont continuellement ajoutées à Microsoft Defender pour Office 365](office-365-atp.md#new-features-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="0407d-138">[New features are continually being added to Microsoft Defender for Office 365](office-365-atp.md#new-features-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="0407d-139">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements aux stratégies de liens fiables existantes.</span><span class="sxs-lookup"><span data-stu-id="0407d-139">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="use-the-security--compliance-center-to-create-safe-links-policies"></a><span data-ttu-id="0407d-140">Utiliser le centre de sécurité & conformité pour créer des stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-140">Use the Security & Compliance Center to create Safe Links policies</span></span>

<span data-ttu-id="0407d-141">La création d’une stratégie de liens fiables personnalisée dans le centre de sécurité & conformité crée simultanément la règle de liens fiables et la stratégie de liens approuvés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="0407d-141">Creating a custom Safe Links policy in the Security & Compliance Center creates the safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="0407d-142">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-142">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-143">Sur la page **liens approuvés** , cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="0407d-143">On the **Safe Links** page, click **Create**.</span></span>

3. <span data-ttu-id="0407d-144">L’Assistant **nouvelle stratégie de liens fiables** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="0407d-144">The **New Safe Links policy** wizard opens.</span></span> <span data-ttu-id="0407d-145">Sur la page **nommer votre stratégie** , configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="0407d-145">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="0407d-146">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0407d-146">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="0407d-147">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0407d-147">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="0407d-148">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0407d-148">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="0407d-149">Sur la page **paramètres** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="0407d-149">On the **Settings** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="0407d-150">**Sélectionnez l’action pour les URL potentiellement malveillantes dans les messages**: sélectionnez **activé** pour activer la protection des liens fiables dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0407d-150">**Select the action for unknown potentially malicious URLs in messages**: Select **On** to enable Safe Links protection for links in email messages.</span></span>

   - <span data-ttu-id="0407d-151">**Sélectionnez l’action pour les URL inconnues ou potentiellement malveillantes dans Microsoft teams**: sélectionnez **activé** pour activer la protection des liens fiables dans Teams.</span><span class="sxs-lookup"><span data-stu-id="0407d-151">**Select the action for unknown or potentially malicious URLs within Microsoft Teams**: Select **On** to enable Safe Links protection for links in Teams.</span></span>

   - <span data-ttu-id="0407d-152">**Application de l’analyse des URL en temps réel pour les liens suspects et les liens pointant vers des fichiers**: sélectionnez ce paramètre pour activer l’analyse en temps réel des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0407d-152">**Apply real-time URL scanning for suspicious links and links that point to files**: Select this setting to enable real-time scanning of links in email messages.</span></span>

   - <span data-ttu-id="0407d-153">**Patientez jusqu’à la fin de l’analyse des URL avant de remettre le message**: sélectionnez ce paramètre pour attendre la fin de l’analyse des URL en temps réel avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="0407d-153">**Wait for URL scanning to complete before delivering the message**: Select this setting to wait for real-time URL scanning to complete before delivering the message.</span></span>

   - <span data-ttu-id="0407d-154">**Appliquer des liens fiables aux messages électroniques envoyés au sein de l’organisation**: sélectionnez ce paramètre pour appliquer la stratégie de liens fiables aux messages entre les expéditeurs internes et les destinataires internes.</span><span class="sxs-lookup"><span data-stu-id="0407d-154">**Apply Safe Links to email messages sent within the organization**: Select this setting to apply the Safe Links policy to messages between internal senders and internal recipients.</span></span>

   - <span data-ttu-id="0407d-155">**Ne pas suivre les clics des utilisateurs**: laissez ce paramètre non sélectionné pour permettre au suivi de cliquer sur les URL dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0407d-155">**Do not track user clicks**: Leave this setting unselected to enable the tracking user clicks on URLs in email messages.</span></span>

   - <span data-ttu-id="0407d-156">**Ne pas autoriser les utilisateurs à cliquer vers l’URL d’origine**: sélectionnez ce paramètre pour empêcher les utilisateurs de cliquer sur l’URL d’origine dans les [pages d’avertissement](atp-safe-links.md#warning-pages-from-safe-links).</span><span class="sxs-lookup"><span data-stu-id="0407d-156">**Do not allow users to click through to original URL**: Select this setting to block users from clicking through to the original URL in [warning pages](atp-safe-links.md#warning-pages-from-safe-links).</span></span>

   - <span data-ttu-id="0407d-157">**Ne réécrivez pas les URL suivantes**: permet d’accéder aux URL spécifiées qui seraient sinon bloquées par les liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-157">**Do not rewrite the following URLs**: Allows access the specified URLs that would otherwise be blocked by Safe Links.</span></span>

     <span data-ttu-id="0407d-158">Dans la zone, tapez l’URL ou la valeur souhaitée, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="0407d-158">In the box, type the URL or value that you want, and then click</span></span> ![Icône Ajouter un bouton](../../media/ITPro-EAC-AddIcon.png)<span data-ttu-id="0407d-160">.</span><span class="sxs-lookup"><span data-stu-id="0407d-160">.</span></span>

     <span data-ttu-id="0407d-161">Pour supprimer une entrée existante, sélectionnez-la, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="0407d-161">To remove an existing entry, select it and then click</span></span> ![Icône de bouton supprimer](../../media/ITPro-EAC-DeleteIcon.png)<span data-ttu-id="0407d-163">.</span><span class="sxs-lookup"><span data-stu-id="0407d-163">.</span></span>

     <span data-ttu-id="0407d-164">Pour la syntaxe d’entrée, consultez [la syntaxe d’entrée pour la liste « ne pas réécrire les URL suivantes »](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span><span class="sxs-lookup"><span data-stu-id="0407d-164">For entry syntax, see [Entry syntax for the "Do not rewrite the following URLs" list](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>

   <span data-ttu-id="0407d-165">Pour plus d’informations sur ces paramètres, consultez les [rubriques paramètres de liens approuvés pour les messages électroniques](atp-safe-links.md#safe-links-settings-for-email-messages) et les [paramètres de liens fiables pour Microsoft teams](atp-safe-links.md#safe-links-settings-for-microsoft-teams).</span><span class="sxs-lookup"><span data-stu-id="0407d-165">For detailed information about these settings, see [Safe Links settings for email messages](atp-safe-links.md#safe-links-settings-for-email-messages) and [Safe Links settings for Microsoft Teams](atp-safe-links.md#safe-links-settings-for-microsoft-teams).</span></span>

   <span data-ttu-id="0407d-166">Pour plus d’informations sur les valeurs recommandées pour les paramètres de stratégie standard et stricte, consultez la rubrique [Safe Links Policy Settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span><span class="sxs-lookup"><span data-stu-id="0407d-166">For more the recommended values for Standard and Strict policy settings, see [Safe Links policy settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span></span>

   <span data-ttu-id="0407d-167">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0407d-167">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="0407d-168">Sur la page **appliqué à** qui s’affiche, identifiez les destinataires internes auxquels s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="0407d-168">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="0407d-169">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="0407d-169">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="0407d-170">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="0407d-170">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="0407d-171">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="0407d-171">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="0407d-172">Cliquez sur **Ajouter une condition**.</span><span class="sxs-lookup"><span data-stu-id="0407d-172">Click **Add a condition**.</span></span> <span data-ttu-id="0407d-173">Dans la liste déroulante qui apparaît, sélectionnez une condition sous **appliqué si**:</span><span class="sxs-lookup"><span data-stu-id="0407d-173">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="0407d-174">**Le destinataire est**: spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0407d-174">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="0407d-175">**Le destinataire est membre de**: spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0407d-175">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="0407d-176">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0407d-176">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="0407d-177">Une fois que vous avez sélectionné la condition, une liste déroulante correspondante apparaît avec **une case à** cocher.</span><span class="sxs-lookup"><span data-stu-id="0407d-177">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="0407d-178">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="0407d-178">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="0407d-179">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="0407d-179">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="0407d-180">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide de la zone.</span><span class="sxs-lookup"><span data-stu-id="0407d-180">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="0407d-181">Pour supprimer des entrées individuelles, cliquez sur **supprimer** ![ ](../../media/scc-remove-icon.png) l’icône de suppression sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="0407d-181">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="0407d-182">Pour supprimer l’ensemble de la condition, cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/scc-remove-icon.png) dans la condition.</span><span class="sxs-lookup"><span data-stu-id="0407d-182">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="0407d-183">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous **appliqué**.</span><span class="sxs-lookup"><span data-stu-id="0407d-183">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="0407d-184">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous **sauf si**.</span><span class="sxs-lookup"><span data-stu-id="0407d-184">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="0407d-185">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="0407d-185">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="0407d-186">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0407d-186">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="0407d-187">Sur la page **vérifier vos paramètres** qui s’affiche, vérifiez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="0407d-187">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="0407d-188">Vous pouvez cliquer sur **modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="0407d-188">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="0407d-189">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="0407d-189">When you're finished, click **Finish**.</span></span>

## <a name="use-the-security--compliance-center-to-view-safe-links-policies"></a><span data-ttu-id="0407d-190">Utiliser le centre de sécurité & conformité pour afficher les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-190">Use the Security & Compliance Center to view Safe Links policies</span></span>

1. <span data-ttu-id="0407d-191">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-191">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-192">Sur la page **liens approuvés** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="0407d-192">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

   <span data-ttu-id="0407d-193">Les détails de la stratégie apparaissent dans un survol</span><span class="sxs-lookup"><span data-stu-id="0407d-193">The policy details appear in a fly out</span></span>

## <a name="use-the-security--compliance-center-to-modify-safe-links-policies"></a><span data-ttu-id="0407d-194">Utiliser le centre de sécurité & conformité pour modifier les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-194">Use the Security & Compliance Center to modify Safe Links policies</span></span>

1. <span data-ttu-id="0407d-195">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-195">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-196">Sur la page **liens approuvés** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="0407d-196">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="0407d-197">Dans le volet Détails de la stratégie, cliquez sur **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="0407d-197">In the policy details fly out that appears, click **Edit policy**.</span></span>

<span data-ttu-id="0407d-198">Les paramètres disponibles dans le survol qui s’affiche sont identiques à ceux décrits dans la section [utiliser le centre de sécurité & conformité pour créer des stratégies de liens fiables](#use-the-security--compliance-center-to-create-safe-links-policies) .</span><span class="sxs-lookup"><span data-stu-id="0407d-198">The available settings in the fly out that appears are identical to those described in the [Use the Security & Compliance Center to create Safe Links policies](#use-the-security--compliance-center-to-create-safe-links-policies) section.</span></span>

<span data-ttu-id="0407d-199">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité des stratégies, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0407d-199">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-links-policies"></a><span data-ttu-id="0407d-200">Activer ou désactiver les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-200">Enable or disable Safe Links policies</span></span>

1. <span data-ttu-id="0407d-201">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-201">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-202">Notez la valeur dans la colonne **État** :</span><span class="sxs-lookup"><span data-stu-id="0407d-202">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="0407d-203">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="0407d-203">Move the toggle to the left to disable the policy:</span></span> ![Désactiver la stratégie](../../media/scc-toggle-off.png)<span data-ttu-id="0407d-205">.</span><span class="sxs-lookup"><span data-stu-id="0407d-205">.</span></span>

   - <span data-ttu-id="0407d-206">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="0407d-206">Move the toggle to the right to enable the policy:</span></span> ![Activer la stratégie](../../media/scc-toggle-on.png)<span data-ttu-id="0407d-208">.</span><span class="sxs-lookup"><span data-stu-id="0407d-208">.</span></span>

### <a name="set-the-priority-of-safe-links-policies"></a><span data-ttu-id="0407d-209">Définir la priorité des stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-209">Set the priority of Safe Links policies</span></span>

<span data-ttu-id="0407d-210">Par défaut, les stratégies de liens fiables reçoivent une priorité basée sur l’ordre dans lequel elles ont été créées (les stratégies plus récentes sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="0407d-210">By default, Safe Links policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="0407d-211">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="0407d-211">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="0407d-212">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="0407d-212">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="0407d-213">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-213">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="0407d-214">Les stratégies de liens fiables sont affichées dans l’ordre dans lequel elles sont traitées (la première stratégie a la valeur de **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="0407d-214">Safe Links policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

<span data-ttu-id="0407d-215">**Remarque**: dans le centre de sécurité & conformité, vous pouvez uniquement modifier la priorité de la stratégie de liens fiables une fois que vous l’avez créée.</span><span class="sxs-lookup"><span data-stu-id="0407d-215">**Note**: In the Security & Compliance Center, you can only change the priority of the Safe Links policy after you create it.</span></span> <span data-ttu-id="0407d-216">Dans PowerShell, vous pouvez remplacer la priorité par défaut lors de la création de la règle de liens fiables (ce qui peut avoir une incidence sur la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="0407d-216">In PowerShell, you can override the default priority when you create the safe links rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="0407d-217">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="0407d-217">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="0407d-218">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-218">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-219">Sur la page **liens approuvés** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="0407d-219">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="0407d-220">Dans le volet Détails de la stratégie, cliquez sur le bouton priorité disponible :</span><span class="sxs-lookup"><span data-stu-id="0407d-220">In the policy details fly out that appears, click the available priority button:</span></span>

   - <span data-ttu-id="0407d-221">La stratégie de liens fiables avec la valeur de **priorité** **0** a uniquement le bouton **diminuer la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="0407d-221">The Safe Links policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="0407d-222">La stratégie de liens fiables avec la valeur de **priorité** la plus faible (par exemple, **3**) n’a que le bouton **augmenter la priorité** disponible.</span><span class="sxs-lookup"><span data-stu-id="0407d-222">The Safe Links policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="0407d-223">Si vous avez trois stratégies de liens fiables ou plus, les stratégies entre les valeurs de priorité la plus élevée et la plus faible ont les deux boutons **augmenter la priorité** et **diminuer la priorité** .</span><span class="sxs-lookup"><span data-stu-id="0407d-223">If you have three or more Safe Links policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="0407d-224">Cliquez sur **augmenter** la priorité ou sur **diminuer la priorité** pour modifier la valeur de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="0407d-224">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="0407d-225">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0407d-225">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-safe-links-policies"></a><span data-ttu-id="0407d-226">Utiliser le centre de sécurité & conformité pour supprimer des stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-226">Use the Security & Compliance Center to remove Safe Links policies</span></span>

1. <span data-ttu-id="0407d-227">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-227">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="0407d-228">Sur la page **liens approuvés** , sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="0407d-228">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="0407d-229">Dans la boîte de dialogue détails de la stratégie, cliquez sur **Supprimer la stratégie**, puis cliquez sur **Oui** dans la boîte de dialogue d’avertissement qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0407d-229">In the policy details fly out that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies"></a><span data-ttu-id="0407d-230">Utiliser Exchange Online PowerShell ou l’environnement de ligne de commande Exchange EOP PowerShell autonome pour configurer les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-230">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies</span></span>

<span data-ttu-id="0407d-231">Comme décrit précédemment, une stratégie de liens fiables est constituée d’une stratégie de liens fiables et d’une règle de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-231">As previously described, a Safe Links policy consists of a safe links policy and a safe links rule.</span></span>

<span data-ttu-id="0407d-232">Dans PowerShell, la différence entre les stratégies de liens fiables et les règles de liens fiables est apparente.</span><span class="sxs-lookup"><span data-stu-id="0407d-232">In PowerShell, the difference between safe links policies and safe links rules is apparent.</span></span> <span data-ttu-id="0407d-233">Vous pouvez gérer les stratégies de liens fiables à l’aide des cmdlets **\* -safelinkspolicy permet** et gérer les règles de liens fiables à l’aide des cmdlets **\* -safelinksrule permet** .</span><span class="sxs-lookup"><span data-stu-id="0407d-233">You manage safe links policies by using the **\*-SafeLinksPolicy** cmdlets, and you manage safe links rules by using the **\*-SafeLinksRule** cmdlets.</span></span>

- <span data-ttu-id="0407d-234">Dans PowerShell, vous devez d’abord créer la stratégie de liens fiables, puis créer la règle de liens fiables qui identifie la stratégie à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="0407d-234">In PowerShell, you create the safe links policy first, then you create the safe links rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="0407d-235">Dans PowerShell, vous pouvez modifier séparément les paramètres de la stratégie de liens fiables et de la règle de liens approuvés.</span><span class="sxs-lookup"><span data-stu-id="0407d-235">In PowerShell, you modify the settings in the safe links policy and the safe links rule separately.</span></span>
- <span data-ttu-id="0407d-236">Lorsque vous supprimez une stratégie de liens fiables de PowerShell, la règle de liens approuvés correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="0407d-236">When you remove a safe links policy from PowerShell, the corresponding safe links rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-links-policies"></a><span data-ttu-id="0407d-237">Utiliser PowerShell pour créer des stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-237">Use PowerShell to create Safe Links policies</span></span>

<span data-ttu-id="0407d-238">La création d’une stratégie de liens fiables dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="0407d-238">Creating a Safe Links policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="0407d-239">Créez la stratégie de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-239">Create the safe links policy.</span></span>
2. <span data-ttu-id="0407d-240">Créer la règle de liens fiables qui spécifie la stratégie de liens approuvés à laquelle la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="0407d-240">Create the safe links rule that specifies the safe links policy that the rule applies to.</span></span>

 <span data-ttu-id="0407d-241">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="0407d-241">**Notes**:</span></span>

- <span data-ttu-id="0407d-242">Vous pouvez créer une règle de liens fiables et lui affecter une stratégie de liens approuvés existante non associée.</span><span class="sxs-lookup"><span data-stu-id="0407d-242">You can create a new safe links rule and assign an existing, unassociated safe links policy to it.</span></span> <span data-ttu-id="0407d-243">Une règle de liens fiables ne peut pas être associée à plusieurs stratégies de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-243">A safe links rule can't be associated with more than one safe links policy.</span></span>

- <span data-ttu-id="0407d-244">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de liens fiables dans PowerShell qui ne sont pas disponibles dans le centre de sécurité & de conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="0407d-244">You can configure the following settings on new safe links policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>

  - <span data-ttu-id="0407d-245">Créez la nouvelle stratégie comme désactivé (_activé_ `$false` sur la cmdlet **New-safelinksrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="0407d-245">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeLinksRule** cmdlet).</span></span>
  - <span data-ttu-id="0407d-246">Définir la priorité de la stratégie lors de la création (_priorité_ _\<Number\>_ ) sur la cmdlet **New-safelinksrule permet** ).</span><span class="sxs-lookup"><span data-stu-id="0407d-246">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeLinksRule** cmdlet).</span></span>

- <span data-ttu-id="0407d-247">Une nouvelle stratégie de liens approuvés que vous créez dans PowerShell n’est pas visible dans le centre de sécurité &, tant que vous n’avez pas affecté la stratégie à une règle de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-247">A new safe links policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a safe links rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-links-policy"></a><span data-ttu-id="0407d-248">Étape 1 : utiliser PowerShell pour créer une stratégie de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-248">Step 1: Use PowerShell to create a safe links policy</span></span>

<span data-ttu-id="0407d-249">Pour créer une stratégie de liens fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-249">To create a safe links policy, use this syntax:</span></span>

```PowerShell
New-SafeLinksPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-IsEnabled <$true | $false>] [-EnableSafeLinksForTeams <$true | $false>] [-ScanUrls <$true | $false>] [-DeliverMessageAfterScan <$true | $false>] [-EnableForInternalSenders <$true | $false>] [-DoNotAllowClickThrough <$true | $false>] [-DoNotTrackUserClicks <$true | $false>] [-DoNotRewriteUrls "Entry1","Entry2",..."EntryN"]
```

<span data-ttu-id="0407d-250">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="0407d-250">**Notes**:</span></span>

- <span data-ttu-id="0407d-251">Pour plus d’informations sur la syntaxe d’entrée à utiliser pour le paramètre _DoNotRewriteUrls_ , voir [entrée Syntax pour la liste « ne pas réécrire les URL suivantes »](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span><span class="sxs-lookup"><span data-stu-id="0407d-251">For details about the entry syntax to use for the _DoNotRewriteUrls_ parameter, see [Entry syntax for the "Do not rewrite the following URLs" list](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>

- <span data-ttu-id="0407d-252">Pour obtenir une syntaxe supplémentaire que vous pouvez utiliser pour le paramètre _DoNotRewriteUrls_ lorsque vous modifiez des stratégies de liens fiables existantes à l’aide de l’applet de commande **Set-safelinkspolicy permet** , voir la section [Utiliser PowerShell pour modifier les stratégies de liens approuvés](#use-powershell-to-modify-safe-links-policies) plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0407d-252">For additional syntax that you can use for the _DoNotRewriteUrls_ parameter when you modify existing safe links policies by using the **Set-SafeLinksPolicy** cmdlet, see the [Use PowerShell to modify safe links policies](#use-powershell-to-modify-safe-links-policies) section later in this article.</span></span>

<span data-ttu-id="0407d-253">Cet exemple crée une stratégie de liens fiables nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0407d-253">This example creates a safe links policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="0407d-254">Activer l’analyse et la réécriture d’URL dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0407d-254">Turn on URL scanning and rewriting in email messages.</span></span>
- <span data-ttu-id="0407d-255">Activer l’analyse des URL dans Teams (appuyez sur Aperçu uniquement).</span><span class="sxs-lookup"><span data-stu-id="0407d-255">Turn on URL scanning in Teams (TAP Preview only).</span></span>
- <span data-ttu-id="0407d-256">Activer l’analyse en temps réel des URL cliquées, y compris les liens sur lesquels pointent vers des fichiers.</span><span class="sxs-lookup"><span data-stu-id="0407d-256">Turn on real-time scanning of clicked URLs, including clicked links that point to files.</span></span>
- <span data-ttu-id="0407d-257">Patientez jusqu’à la fin de l’analyse des URL avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="0407d-257">Wait for URL scanning to complete before delivering the message.</span></span>
- <span data-ttu-id="0407d-258">Activez l’analyse des URL et la réécriture pour les messages internes.</span><span class="sxs-lookup"><span data-stu-id="0407d-258">Turn on URL scanning and rewriting for internal messages.</span></span>
- <span data-ttu-id="0407d-259">Suivi des clics d’utilisateur liés à la protection des liens fiables (nous n’utilisons pas le paramètre _DoNotTrackUserClicks_ et la valeur par défaut est $false, ce qui signifie que les clics utilisateur font l’élément d’un suivi).</span><span class="sxs-lookup"><span data-stu-id="0407d-259">Track user clicks related to Safe Links protection (we aren't using the _DoNotTrackUserClicks_ parameter, and the default value is $false, which means user clicks are tracked).</span></span>
- <span data-ttu-id="0407d-260">Ne pas autoriser les utilisateurs à cliquer à travers l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="0407d-260">Do not allow users to click through to the original URL.</span></span>

```PowerShell
New-SafeLinksPolicy -Name "Contoso All" -IsEnabled $true -EnableSafeLinksForTeams $true -ScanUrls $true -DeliverMessageAfterScan $true -EnableForInternalSenders $true -DoNotAllowClickThrough $true
```

<span data-ttu-id="0407d-261">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-safelinkspolicy permet](https://docs.microsoft.com/powershell/module/exchange/new-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="0407d-261">For detailed syntax and parameter information, see [New-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/new-safelinkspolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-links-rule"></a><span data-ttu-id="0407d-262">Étape 2 : utiliser PowerShell pour créer une règle de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-262">Step 2: Use PowerShell to create a safe links rule</span></span>

<span data-ttu-id="0407d-263">Pour créer une règle de liens fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-263">To create a safe links rule, use this syntax:</span></span>

```PowerShell
New-SafeLinksRule -Name "<RuleName>" -SafeLinksPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="0407d-264">Cet exemple crée une règle de liens fiables nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0407d-264">This example creates a safe links rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="0407d-265">La règle est associée à la stratégie de liens approuvés nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="0407d-265">The rule is associated with the safe links policy named Contoso All.</span></span>
- <span data-ttu-id="0407d-266">La règle s’applique à tous les destinataires dans le domaine contoso.com.</span><span class="sxs-lookup"><span data-stu-id="0407d-266">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="0407d-267">Étant donné que nous n’utilisons pas le paramètre _Priority_ , la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="0407d-267">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="0407d-268">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="0407d-268">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeLinksRule -Name "Contoso All" -SafeLinksPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="0407d-269">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [New-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/new-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-269">For detailed syntax and parameter information, see [New-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/new-safelinksrule).</span></span>

### <a name="use-powershell-to-view-safe-links-policies"></a><span data-ttu-id="0407d-270">Utiliser PowerShell pour afficher les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-270">Use PowerShell to view safe links policies</span></span>

<span data-ttu-id="0407d-271">Pour afficher les stratégies de liens fiables existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-271">To view existing safe links policies, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="0407d-272">Cet exemple renvoie la liste récapitulative de toutes les stratégies de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-272">This example returns a summary list of all safe links policies.</span></span>

```PowerShell
Get-SafeLinksPolicy | Format-Table Name
```

<span data-ttu-id="0407d-273">Cet exemple renvoie des informations détaillées sur la stratégie de liens approuvés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="0407d-273">This example returns detailed information for the safe links policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksPolicy -Identity "Contoso Executives"
```

<span data-ttu-id="0407d-274">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-safelinkspolicy permet](https://docs.microsoft.com/powershell/module/exchange/get-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="0407d-274">For detailed syntax and parameter information, see [Get-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/get-safelinkspolicy).</span></span>

### <a name="use-powershell-to-view-safe-links-rules"></a><span data-ttu-id="0407d-275">Utiliser PowerShell pour afficher les règles de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-275">Use PowerShell to view safe links rules</span></span>

<span data-ttu-id="0407d-276">Pour afficher les règles de liens fiables existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-276">To view existing safe links rules, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="0407d-277">Cet exemple renvoie la liste récapitulative de toutes les règles de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-277">This example returns a summary list of all safe links rules.</span></span>

```PowerShell
Get-SafeLinksRule | Format-Table Name,State
```

<span data-ttu-id="0407d-278">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0407d-278">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeLinksRule -State Disabled
```

```PowerShell
Get-SafeLinksRule -State Enabled
```

<span data-ttu-id="0407d-279">Cet exemple renvoie des informations détaillées sur la règle de liens approuvés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="0407d-279">This example returns detailed information for the safe links rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksRule -Identity "Contoso Executives"
```

<span data-ttu-id="0407d-280">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/get-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-280">For detailed syntax and parameter information, see [Get-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/get-safelinksrule).</span></span>

### <a name="use-powershell-to-modify-safe-links-policies"></a><span data-ttu-id="0407d-281">Utiliser PowerShell pour modifier les stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-281">Use PowerShell to modify safe links policies</span></span>

<span data-ttu-id="0407d-282">Vous ne pouvez pas renommer une stratégie de liens fiables dans PowerShell (l’applet de commande **Set-safelinkspolicy permet** n’a pas de paramètre _Name_ ).</span><span class="sxs-lookup"><span data-stu-id="0407d-282">You can't rename a safe links policy in PowerShell (the **Set-SafeLinksPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="0407d-283">Lorsque vous renommez une stratégie de liens fiables dans le centre de sécurité & conformité, vous renommez uniquement la _règle_ de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="0407d-283">When you rename a Safe Links policy in the Security & Compliance Center, you're only renaming the safe links _rule_.</span></span>

<span data-ttu-id="0407d-284">La seule considération supplémentaire pour la modification des stratégies de liens fiables dans PowerShell est la syntaxe disponible pour le paramètre _DoNotRewriteUrls_ (la [liste « ne pas réécrire les URL suivantes »](atp-safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)) :</span><span class="sxs-lookup"><span data-stu-id="0407d-284">The only additional consideration for modifying safe links policies in PowerShell is the available syntax for the _DoNotRewriteUrls_ parameter (the ["Do not rewrite the following URLs" list](atp-safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)):</span></span>

- <span data-ttu-id="0407d-285">Pour ajouter des valeurs qui remplaceront toutes les entrées existantes, utilisez la syntaxe suivante : `"Entry1","Entry2,..."EntryN"` .</span><span class="sxs-lookup"><span data-stu-id="0407d-285">To add values that will replace any existing entries, use the following syntax: `"Entry1","Entry2,..."EntryN"`.</span></span>
- <span data-ttu-id="0407d-286">Pour ajouter ou supprimer des valeurs sans affecter les entrées existantes, utilisez la syntaxe suivante : `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span><span class="sxs-lookup"><span data-stu-id="0407d-286">To add or remove values without affecting other existing entries, use the following syntax: `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span></span>

<span data-ttu-id="0407d-287">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de liens fiables, comme décrit dans la section [étape 1 : utiliser PowerShell pour créer une stratégie de liens fiables](#step-1-use-powershell-to-create-a-safe-links-policy) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0407d-287">Otherwise, the same settings are available when you create a safe links policy as described in the [Step 1: Use PowerShell to create a safe links policy](#step-1-use-powershell-to-create-a-safe-links-policy) section earlier in this article.</span></span>

<span data-ttu-id="0407d-288">Pour modifier une stratégie de liens fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-288">To modify a safe links policy, use this syntax:</span></span>

```PowerShell
Set-SafeLinksPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="0407d-289">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safelinkspolicy permet](https://docs.microsoft.com/powershell/module/exchange/set-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="0407d-289">For detailed syntax and parameter information, see [Set-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/set-safelinkspolicy).</span></span>

### <a name="use-powershell-to-modify-safe-links-rules"></a><span data-ttu-id="0407d-290">Utiliser PowerShell pour modifier les règles de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-290">Use PowerShell to modify safe links rules</span></span>

<span data-ttu-id="0407d-291">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de liens fiables dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="0407d-291">The only setting that's not available when you modify a safe links rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="0407d-292">Pour activer ou désactiver les règles de liens approuvés existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="0407d-292">To enable or disable existing safe links rules, see the next section.</span></span>

<span data-ttu-id="0407d-293">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle, comme décrit dans la section [étape 2 : utiliser PowerShell pour créer une règle de liens fiables](#step-2-use-powershell-to-create-a-safe-links-rule) plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0407d-293">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe links rule](#step-2-use-powershell-to-create-a-safe-links-rule) section earlier in this article.</span></span>

<span data-ttu-id="0407d-294">Pour modifier une règle de liens fiables, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-294">To modify a safe links rule, use this syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="0407d-295">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-295">For detailed syntax and parameter information, see [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-links-rules"></a><span data-ttu-id="0407d-296">Utiliser PowerShell pour activer ou désactiver les règles de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-296">Use PowerShell to enable or disable safe links rules</span></span>

<span data-ttu-id="0407d-297">L’activation ou la désactivation d’une règle de liens fiables dans PowerShell active ou désactive la stratégie de liens fiables entières (la règle de liens fiables et la stratégie de liens fiables affectés).</span><span class="sxs-lookup"><span data-stu-id="0407d-297">Enabling or disabling a safe links rule in PowerShell enables or disables the whole Safe Links policy (the safe links rule and the assigned safe links policy).</span></span>

<span data-ttu-id="0407d-298">Pour activer ou désactiver une règle de liens fiables dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-298">To enable or disable a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeLinksRule | Disable-SafeLinksRule> -Identity "<RuleName>"
```

<span data-ttu-id="0407d-299">Cet exemple désactive la règle de liens approuvés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0407d-299">This example disables the safe links rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="0407d-300">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="0407d-300">This example enables same rule.</span></span>

```PowerShell
Enable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="0407d-301">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/enable-safelinksrule) et [Disable-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/disable-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-301">For detailed syntax and parameter information, see [Enable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/enable-safelinksrule) and [Disable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/disable-safelinksrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-links-rules"></a><span data-ttu-id="0407d-302">Utiliser PowerShell pour définir la priorité des règles de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-302">Use PowerShell to set the priority of safe links rules</span></span>

<span data-ttu-id="0407d-303">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="0407d-303">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="0407d-304">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="0407d-304">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="0407d-305">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="0407d-305">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="0407d-306">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="0407d-306">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="0407d-307">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="0407d-307">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="0407d-308">Pour définir la priorité d’une règle de liens fiables dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-308">To set the priority of a safe links rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="0407d-p123">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="0407d-p123">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeLinksRule -Identity "Marketing Department" -Priority 2
```

<span data-ttu-id="0407d-311">**Remarque**: pour définir la priorité d’une nouvelle règle lors de sa création, utilisez plutôt le paramètre _Priority_ sur la cmdlet **New-safelinksrule permet** .</span><span class="sxs-lookup"><span data-stu-id="0407d-311">**Note**: To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeLinksRule** cmdlet instead.</span></span>

<span data-ttu-id="0407d-312">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-312">For detailed syntax and parameter information, see [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-remove-safe-links-policies"></a><span data-ttu-id="0407d-313">Utiliser PowerShell pour supprimer des stratégies de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-313">Use PowerShell to remove safe links policies</span></span>

<span data-ttu-id="0407d-314">Lorsque vous utilisez PowerShell pour supprimer une stratégie de liens fiables, la règle de liens fiables correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="0407d-314">When you use PowerShell to remove a safe links policy, the corresponding safe links rule isn't removed.</span></span>

<span data-ttu-id="0407d-315">Pour supprimer une stratégie de liens fiables dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-315">To remove a safe links policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="0407d-316">Cet exemple supprime la stratégie de liens approuvés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0407d-316">This example removes the safe links policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "Marketing Department"
```

<span data-ttu-id="0407d-317">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-safelinkspolicy permet](https://docs.microsoft.com/powershell/module/exchange/remove-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="0407d-317">For detailed syntax and parameter information, see [Remove-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-safelinkspolicy).</span></span>

### <a name="use-powershell-to-remove-safe-links-rules"></a><span data-ttu-id="0407d-318">Utiliser PowerShell pour supprimer des règles de liens fiables</span><span class="sxs-lookup"><span data-stu-id="0407d-318">Use PowerShell to remove safe links rules</span></span>

<span data-ttu-id="0407d-319">Lorsque vous utilisez PowerShell pour supprimer une règle de liens fiables, la stratégie de liens fiables correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="0407d-319">When you use PowerShell to remove a safe links rule, the corresponding safe links policy isn't removed.</span></span>

<span data-ttu-id="0407d-320">Pour supprimer une règle de liens fiables dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0407d-320">To remove a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "<PolicyName>"
```

<span data-ttu-id="0407d-321">Cet exemple supprime la règle de liens approuvés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="0407d-321">This example removes the safe links rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="0407d-322">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Remove-safelinksrule permet](https://docs.microsoft.com/powershell/module/exchange/remove-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="0407d-322">For detailed syntax and parameter information, see [Remove-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/remove-safelinksrule).</span></span>

<span data-ttu-id="0407d-323">Pour vérifier que les liens fiables analysent les messages, consultez les rapports Microsoft Defender pour Office 365 disponibles.</span><span class="sxs-lookup"><span data-stu-id="0407d-323">To verify that Safe Links is scanning messages, check the available Microsoft Defender for Office 365 reports.</span></span> <span data-ttu-id="0407d-324">Pour plus d’informations, consultez la rubrique [afficher les rapports pour Defender pour Office 365](view-reports-for-atp.md) et [utiliser l’Explorateur dans le centre de sécurité & conformité](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="0407d-324">For more information, see [View reports for Defender for Office 365](view-reports-for-atp.md) and [Use Explorer in the Security & Compliance Center](threat-explorer.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="0407d-325">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="0407d-325">How do you know these procedures worked?</span></span>

<span data-ttu-id="0407d-326">Pour vérifier que vous avez bien créé, modifié ou supprimé des stratégies de liens fiables, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0407d-326">To verify that you've successfully created, modified, or removed Safe Links policies, do any of the following steps:</span></span>

- <span data-ttu-id="0407d-327">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \>  \> **liens fiables ATP**.</span><span class="sxs-lookup"><span data-stu-id="0407d-327">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span> <span data-ttu-id="0407d-328">Vérifiez la liste des stratégies, leurs valeurs d' **État** et leurs valeurs de **priorité** .</span><span class="sxs-lookup"><span data-stu-id="0407d-328">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="0407d-329">Pour afficher plus de détails, sélectionnez la stratégie dans la liste, puis affichez les détails dans le survol.</span><span class="sxs-lookup"><span data-stu-id="0407d-329">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="0407d-330">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez \<Name\> par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="0407d-330">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeLinksPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-SafeLinksRule -Identity "<Name>"
  ```
