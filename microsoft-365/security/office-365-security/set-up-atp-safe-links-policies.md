---
title: Configurer des stratégies de liens sécurisés dans Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: how-to
ms.date: ''
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir comment afficher, créer, modifier et supprimer des stratégies de liens sécurisés et des paramètres globaux de liens sécurisés dans Microsoft Defender pour Office 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 71ea33f1f6fbebf6d87a4b42ad3bd96a60597b90
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166266"
---
# <a name="set-up-safe-links-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="1f845-103">Configurer des stratégies de liens sécurisés dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1f845-103">Set up Safe Links policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1f845-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1f845-104">**Applies to**</span></span>
- [<span data-ttu-id="1f845-105">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="1f845-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="1f845-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1f845-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!IMPORTANT]
> <span data-ttu-id="1f845-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="1f845-107">This article is intended for business customers who have [Microsoft Defender for Office 365](office-365-atp.md).</span></span> <span data-ttu-id="1f845-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur Safelinks dans Outlook, voir [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="1f845-108">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="1f845-109">La fonctionnalité Liens sécurisés de Microsoft Defender pour [Office 365](office-365-atp.md) permet d’analyser les URL des messages électroniques entrants dans le flux de messagerie, ainsi que l’heure de vérification des URL et des liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="1f845-109">Safe Links is a feature in [Microsoft Defender for Office 365](office-365-atp.md) that provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="1f845-110">Pour plus d’informations, [voir Liens sécurisés dans Microsoft Defender pour Office 365.](atp-safe-links.md)</span><span class="sxs-lookup"><span data-stu-id="1f845-110">For more information, see [Safe Links in Microsoft Defender for Office 365](atp-safe-links.md).</span></span>

<span data-ttu-id="1f845-111">Il n’existe aucune stratégie de liens sécurisés intégrée ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f845-111">There's no built-in or default Safe Links policy.</span></span> <span data-ttu-id="1f845-112">Pour obtenir l’analyse des URL par des liens sécurisés, vous devez créer une ou plusieurs stratégies de liens sécurisés, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1f845-112">To get Safe Links scanning of URLs, you need to create one or more Safe Links policies as described in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="1f845-113">Vous configurez les paramètres globaux pour la **protection** des liens sécurisés en dehors des stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-113">You configure the global settings for Safe Links protection **outside** of Safe Links policies.</span></span> <span data-ttu-id="1f845-114">Pour obtenir des instructions, voir Configurer les paramètres globaux pour les liens [sécurisés dans Microsoft Defender pour Office 365.](configure-global-settings-for-safe-links.md)</span><span class="sxs-lookup"><span data-stu-id="1f845-114">For instructions, see [Configure global settings for Safe Links in Microsoft Defender for Office 365](configure-global-settings-for-safe-links.md).</span></span>

<span data-ttu-id="1f845-115">Vous pouvez configurer des stratégies de liens sécurisés dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres dans Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec des abonnements de modules supplémentaires Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="1f845-115">You can configure Safe Links policies in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Microsoft Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="1f845-116">Les éléments de base d’une stratégie de liens sécurisés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1f845-116">The basic elements of a Safe Links policy are:</span></span>

- <span data-ttu-id="1f845-117">La stratégie de liens sécurisés : activer la protection contre les liens sécurisés, activer l’analyse des URL en temps réel, spécifier s’il faut attendre la fin de l’analyse en temps réel avant de remettre le message, activer l’analyse des messages internes, spécifier s’il faut suivre les clics des utilisateurs sur les URL et spécifier s’il faut autoriser les utilisateurs à cliquer sur l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="1f845-117">**The safe links policy**: Turn on Safe Links protection, turn on real-time URL scanning, specify whether to wait for real-time scanning to complete before delivering the message, turn on scanning for internal messages, specify whether to track user clicks on URLs, and specify whether to allow users to click trough to the original URL.</span></span>
- <span data-ttu-id="1f845-118">**La règle de liens sécurisés**: spécifie la priorité et les filtres de destinataires (à qui s’applique la stratégie).</span><span class="sxs-lookup"><span data-stu-id="1f845-118">**The safe links rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

<span data-ttu-id="1f845-119">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez les polices de liens sécurisés dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="1f845-119">The difference between these two elements isn't obvious when you manage Safe Links polices in the Security & Compliance Center:</span></span>

- <span data-ttu-id="1f845-120">Lorsque vous créez une stratégie de liens sécurisés, vous créez en même temps une règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="1f845-120">When you create a Safe Links policy, you're actually creating a safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="1f845-121">Lorsque vous modifiez une stratégie de liens sécurisés, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-121">When you modify a Safe Links policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe links rule.</span></span> <span data-ttu-id="1f845-122">Tous les autres paramètres modifient la stratégie de liens sécurisés associée.</span><span class="sxs-lookup"><span data-stu-id="1f845-122">All other settings modify the associated safe links policy.</span></span>
- <span data-ttu-id="1f845-123">Lorsque vous supprimez une stratégie de liens sécurisés, la règle de liens sécurisés et la stratégie de liens sécurisés associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="1f845-123">When you remove a Safe Links policy, the safe links rule and the associated safe links policy are removed.</span></span>

<span data-ttu-id="1f845-124">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="1f845-124">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="1f845-125">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou [EOP PowerShell](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) autonome pour configurer des stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1f845-125">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) section later in this article.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="1f845-126">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1f845-126">What do you need to know before you begin?</span></span>

- <span data-ttu-id="1f845-127">Vous ouvrez le Centre de sécurité et conformité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="1f845-127">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="1f845-128">Pour aller directement à la page **Liens sécurisés,** utilisez <https://protection.office.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="1f845-128">To go directly to the **Safe Links** page, use <https://protection.office.com/safelinksv2>.</span></span>

- <span data-ttu-id="1f845-129">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="1f845-129">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="1f845-130">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="1f845-130">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="1f845-131">Des autorisations doivent vous être attribuées avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="1f845-131">You need to be assigned permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="1f845-132">Pour créer, modifier et supprimer des stratégies de liens  sécurisés, vous devez être membre des groupes  de rôles  Gestion de l’organisation ou Administrateur de la sécurité dans le Centre de sécurité & conformité et membre du groupe de rôles Gestion de l’organisation dans Exchange Online. </span><span class="sxs-lookup"><span data-stu-id="1f845-132">To create, modify, and delete Safe Links policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Security & Compliance Center **and** a member of the **Organization Management** role group in Exchange Online.</span></span>
  - <span data-ttu-id="1f845-133">Pour accéder en lecture seule aux stratégies de liens  sécurisés, vous devez être membre des groupes de rôles Lecteur global ou Lecteur **de** sécurité.</span><span class="sxs-lookup"><span data-stu-id="1f845-133">For read-only access to Safe Links policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="1f845-134">Pour plus d’informations, [voir Autorisations](permissions-in-the-security-and-compliance-center.md) dans le Centre de sécurité & conformité et [autorisations dans Exchange Online.](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo)</span><span class="sxs-lookup"><span data-stu-id="1f845-134">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) and [Permissions in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  > 
  > - <span data-ttu-id="1f845-135">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1f845-135">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1f845-136">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="1f845-136">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>
  <span data-ttu-id="1f845-137">.</span><span class="sxs-lookup"><span data-stu-id="1f845-137">.</span></span> <span data-ttu-id="1f845-138">- Le **groupe de rôles** Gestion de l’organisation en affichage seul dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1f845-138">- The **View-Only Organization Management** role group in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="1f845-139">Pour obtenir nos paramètres recommandés pour les stratégies de liens sécurisés, consultez les [paramètres de stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="1f845-139">For our recommended settings for Safe Links policies, see [Safe Links policy settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span></span>

- <span data-ttu-id="1f845-140">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="1f845-140">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="1f845-141">[De nouvelles fonctionnalités sont continuellement ajoutées à Microsoft Defender pour Office 365.](office-365-atp.md#new-features-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="1f845-141">[New features are continually being added to Microsoft Defender for Office 365](office-365-atp.md#new-features-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="1f845-142">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements à vos stratégies de liens sécurisés existantes.</span><span class="sxs-lookup"><span data-stu-id="1f845-142">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="use-the-security--compliance-center-to-create-safe-links-policies"></a><span data-ttu-id="1f845-143">Utiliser le Centre de sécurité & conformité pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-143">Use the Security & Compliance Center to create Safe Links policies</span></span>

<span data-ttu-id="1f845-144">La création d’une stratégie de liens sécurisés personnalisée dans le Centre de sécurité & conformité crée la règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="1f845-144">Creating a custom Safe Links policy in the Security & Compliance Center creates the safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="1f845-145">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-145">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-146">Dans la page **Liens sécurisés,** cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="1f845-146">On the **Safe Links** page, click **Create**.</span></span>

3. <span data-ttu-id="1f845-147">**L’Assistant Nouvelle stratégie de liens sécurisés** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="1f845-147">The **New Safe Links policy** wizard opens.</span></span> <span data-ttu-id="1f845-148">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1f845-148">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="1f845-149">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f845-149">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="1f845-150">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f845-150">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="1f845-151">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f845-151">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="1f845-152">Dans la page **Paramètres** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="1f845-152">On the **Settings** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="1f845-153">**Sélectionnez l’action pour les URL potentiellement malveillantes inconnues** dans les messages : sélectionnez **Activé** pour activer la protection des liens vers des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="1f845-153">**Select the action for unknown potentially malicious URLs in messages**: Select **On** to enable Safe Links protection for links in email messages.</span></span>

   - <span data-ttu-id="1f845-154">**Sélectionnez l’action pour les** URL inconnues ou potentiellement malveillantes dans Microsoft Teams : sélectionnez **Activé** pour activer la protection des liens sécurisés pour les liens dans Teams.</span><span class="sxs-lookup"><span data-stu-id="1f845-154">**Select the action for unknown or potentially malicious URLs within Microsoft Teams**: Select **On** to enable Safe Links protection for links in Teams.</span></span>

   - <span data-ttu-id="1f845-155">**Appliquez l’analyse** des URL en temps réel pour les liens suspects et les liens pointant vers des fichiers : sélectionnez ce paramètre pour activer l’analyse en temps réel des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="1f845-155">**Apply real-time URL scanning for suspicious links and links that point to files**: Select this setting to enable real-time scanning of links in email messages.</span></span>

   - <span data-ttu-id="1f845-156">**Attendez que l’analyse des URL** se termine avant de remettre le message : sélectionnez ce paramètre pour attendre la fin de l’analyse de l’URL en temps réel avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="1f845-156">**Wait for URL scanning to complete before delivering the message**: Select this setting to wait for real-time URL scanning to complete before delivering the message.</span></span>

   - <span data-ttu-id="1f845-157">**Appliquer des liens sûrs** aux messages électroniques envoyés au sein de l’organisation : sélectionnez ce paramètre pour appliquer la stratégie de liens sécurisés aux messages entre les expéditeurs internes et les destinataires internes.</span><span class="sxs-lookup"><span data-stu-id="1f845-157">**Apply Safe Links to email messages sent within the organization**: Select this setting to apply the Safe Links policy to messages between internal senders and internal recipients.</span></span>

   - <span data-ttu-id="1f845-158">**Ne pas suivre les clics** de l’utilisateur : laissez ce paramètre désélectionnés pour activer les clics de l’utilisateur de suivi sur les URL des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="1f845-158">**Do not track user clicks**: Leave this setting unselected to enable the tracking user clicks on URLs in email messages.</span></span>

   - <span data-ttu-id="1f845-159">**N’autorisez pas** les utilisateurs à cliquer sur l’URL d’origine : sélectionnez ce paramètre pour empêcher les utilisateurs de cliquer jusqu’à l’URL d’origine dans les [pages d’avertissement.](atp-safe-links.md#warning-pages-from-safe-links)</span><span class="sxs-lookup"><span data-stu-id="1f845-159">**Do not allow users to click through to original URL**: Select this setting to block users from clicking through to the original URL in [warning pages](atp-safe-links.md#warning-pages-from-safe-links).</span></span>

   - <span data-ttu-id="1f845-160">**Ne réécrivez pas les** URL suivantes : permet d’accéder aux URL spécifiées qui seraient autrement bloquées par les liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-160">**Do not rewrite the following URLs**: Allows access the specified URLs that would otherwise be blocked by Safe Links.</span></span>

     <span data-ttu-id="1f845-161">Dans la zone, tapez l’URL ou la valeur de votre souhaitez, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="1f845-161">In the box, type the URL or value that you want, and then click</span></span> ![Icône Ajouter un bouton](../../media/ITPro-EAC-AddIcon.png)<span data-ttu-id="1f845-163">.</span><span class="sxs-lookup"><span data-stu-id="1f845-163">.</span></span>

     <span data-ttu-id="1f845-164">Pour supprimer une entrée existante, sélectionnez-la, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="1f845-164">To remove an existing entry, select it and then click</span></span> ![Icône Supprimer le bouton](../../media/ITPro-EAC-DeleteIcon.png)<span data-ttu-id="1f845-166">.</span><span class="sxs-lookup"><span data-stu-id="1f845-166">.</span></span>

     <span data-ttu-id="1f845-167">Pour la syntaxe d’entrée, voir [syntaxe d’entrée pour la](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="1f845-167">For entry syntax, see [Entry syntax for the "Do not rewrite the following URLs" list](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>

   <span data-ttu-id="1f845-168">Pour plus d’informations sur ces paramètres, voir Les [paramètres](atp-safe-links.md#safe-links-settings-for-email-messages) de liens sécurisés pour les messages électroniques et les paramètres de liens [sécurisés pour Microsoft Teams.](atp-safe-links.md#safe-links-settings-for-microsoft-teams)</span><span class="sxs-lookup"><span data-stu-id="1f845-168">For detailed information about these settings, see [Safe Links settings for email messages](atp-safe-links.md#safe-links-settings-for-email-messages) and [Safe Links settings for Microsoft Teams](atp-safe-links.md#safe-links-settings-for-microsoft-teams).</span></span>

   <span data-ttu-id="1f845-169">Pour plus d’informations sur les valeurs recommandées pour les paramètres de stratégie Standard et Strict, voir Paramètres de [stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="1f845-169">For more the recommended values for Standard and Strict policy settings, see [Safe Links policy settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-policy-settings).</span></span>

   <span data-ttu-id="1f845-170">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f845-170">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="1f845-171">Dans la page **Appliqué à** qui s’affiche, identifiez les destinataires internes à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f845-171">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="1f845-172">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="1f845-172">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="1f845-173">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="1f845-173">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="1f845-174">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="1f845-174">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="1f845-175">Cliquez **sur Ajouter une condition.**</span><span class="sxs-lookup"><span data-stu-id="1f845-175">Click **Add a condition**.</span></span> <span data-ttu-id="1f845-176">Dans ladown qui s’affiche, sélectionnez une condition sous **Applied si**:</span><span class="sxs-lookup"><span data-stu-id="1f845-176">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="1f845-177">**Le destinataire est**: Spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f845-177">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="1f845-178">**Le destinataire est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f845-178">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="1f845-179">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1f845-179">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="1f845-180">Une fois que vous avez sélectionné la condition, une zone « Tout » apparaît dans la zone « **Tout le** monde ».</span><span class="sxs-lookup"><span data-stu-id="1f845-180">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="1f845-181">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="1f845-181">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="1f845-182">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="1f845-182">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="1f845-183">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="1f845-183">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="1f845-184">Pour supprimer des entrées individuelles, cliquez **sur Supprimer** ![ ](../../media/scc-remove-icon.png) l’icône sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="1f845-184">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="1f845-185">Pour supprimer la condition entière, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la condition.</span><span class="sxs-lookup"><span data-stu-id="1f845-185">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="1f845-186">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous Appliqué **si**.</span><span class="sxs-lookup"><span data-stu-id="1f845-186">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="1f845-187">Pour ajouter des exceptions, cliquez sur **Ajouter une condition** et sélectionnez une exception sous Sauf **si**.</span><span class="sxs-lookup"><span data-stu-id="1f845-187">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="1f845-188">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="1f845-188">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="1f845-189">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1f845-189">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="1f845-190">Dans la page **Examiner vos paramètres** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="1f845-190">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="1f845-191">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="1f845-191">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="1f845-192">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="1f845-192">When you're finished, click **Finish**.</span></span>

## <a name="use-the-security--compliance-center-to-view-safe-links-policies"></a><span data-ttu-id="1f845-193">Utiliser le Centre de sécurité & conformité pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-193">Use the Security & Compliance Center to view Safe Links policies</span></span>

1. <span data-ttu-id="1f845-194">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-194">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-195">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="1f845-195">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

   <span data-ttu-id="1f845-196">Les détails de la stratégie apparaissent dans un volant</span><span class="sxs-lookup"><span data-stu-id="1f845-196">The policy details appear in a fly out</span></span>

## <a name="use-the-security--compliance-center-to-modify-safe-links-policies"></a><span data-ttu-id="1f845-197">Utiliser le Centre de sécurité & conformité pour modifier les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-197">Use the Security & Compliance Center to modify Safe Links policies</span></span>

1. <span data-ttu-id="1f845-198">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-198">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-199">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="1f845-199">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="1f845-200">Dans le volant des détails de stratégie qui s’affiche, cliquez **sur Modifier la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="1f845-200">In the policy details fly out that appears, click **Edit policy**.</span></span>

<span data-ttu-id="1f845-201">Les paramètres disponibles dans le volant qui s’affiche sont identiques à ceux décrits dans la section Utiliser le Centre de sécurité & conformité pour créer des stratégies de [liens sécurisés.](#use-the-security--compliance-center-to-create-safe-links-policies)</span><span class="sxs-lookup"><span data-stu-id="1f845-201">The available settings in the fly out that appears are identical to those described in the [Use the Security & Compliance Center to create Safe Links policies](#use-the-security--compliance-center-to-create-safe-links-policies) section.</span></span>

<span data-ttu-id="1f845-202">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1f845-202">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-links-policies"></a><span data-ttu-id="1f845-203">Activer ou désactiver les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-203">Enable or disable Safe Links policies</span></span>

1. <span data-ttu-id="1f845-204">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-204">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-205">Notez la valeur dans la **colonne État** :</span><span class="sxs-lookup"><span data-stu-id="1f845-205">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="1f845-206">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="1f845-206">Move the toggle to the left to disable the policy:</span></span> ![Désactiver la stratégie](../../media/scc-toggle-off.png)<span data-ttu-id="1f845-208">.</span><span class="sxs-lookup"><span data-stu-id="1f845-208">.</span></span>

   - <span data-ttu-id="1f845-209">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="1f845-209">Move the toggle to the right to enable the policy:</span></span> ![Activer la stratégie](../../media/scc-toggle-on.png)<span data-ttu-id="1f845-211">.</span><span class="sxs-lookup"><span data-stu-id="1f845-211">.</span></span>

### <a name="set-the-priority-of-safe-links-policies"></a><span data-ttu-id="1f845-212">Définir la priorité des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-212">Set the priority of Safe Links policies</span></span>

<span data-ttu-id="1f845-213">Par défaut, les stratégies de liens sécurisés ont une priorité qui est basée sur l’ordre dans quoi elles ont été créées (les stratégies les plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="1f845-213">By default, Safe Links policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="1f845-214">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="1f845-214">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="1f845-215">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="1f845-215">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="1f845-216">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="1f845-216">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="1f845-217">Les stratégies de liens sécurisés sont affichées dans l’ordre de traitement (la première stratégie a la valeur De **priorité** 0).</span><span class="sxs-lookup"><span data-stu-id="1f845-217">Safe Links policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

> [!NOTE]
> <span data-ttu-id="1f845-218">Dans le Centre de sécurité & conformité, vous ne pouvez modifier la priorité de la stratégie de liens sécurisés qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="1f845-218">In the Security & Compliance Center, you can only change the priority of the Safe Links policy after you create it.</span></span> <span data-ttu-id="1f845-219">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle de liens sécurisés (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="1f845-219">In PowerShell, you can override the default priority when you create the safe links rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="1f845-220">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de **priorité** dans le Centre de sécurité & conformité).</span><span class="sxs-lookup"><span data-stu-id="1f845-220">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Security & Compliance Center).</span></span>

1. <span data-ttu-id="1f845-221">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-221">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-222">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="1f845-222">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="1f845-223">Dans le volant des détails de stratégie qui s’affiche, cliquez sur le bouton de priorité disponible :</span><span class="sxs-lookup"><span data-stu-id="1f845-223">In the policy details fly out that appears, click the available priority button:</span></span>

   - <span data-ttu-id="1f845-224">La stratégie de liens sécurisés avec la valeur **de** priorité **0** ne dispose que **du** bouton Diminuer la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="1f845-224">The Safe Links policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="1f845-225">La stratégie de liens sécurisés avec la valeur **de** priorité la plus faible **(par** exemple, 3 ) ne dispose que du bouton **Augmenter** la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="1f845-225">The Safe Links policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="1f845-226">Si vous disposez de trois stratégies de liens sécurisés ou  plus,  les stratégies entre les valeurs de priorité les plus élevées et les plus faibles disposent à la fois des boutons Augmenter la priorité et Diminuer la priorité.</span><span class="sxs-lookup"><span data-stu-id="1f845-226">If you have three or more Safe Links policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="1f845-227">Cliquez **sur Augmenter la priorité** ou Diminuer la **priorité** pour modifier la **valeur** Priorité.</span><span class="sxs-lookup"><span data-stu-id="1f845-227">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="1f845-228">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1f845-228">When you're finished, click **Close**.</span></span>

## <a name="use-the-security--compliance-center-to-remove-safe-links-policies"></a><span data-ttu-id="1f845-229">Utiliser le Centre de sécurité & conformité pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-229">Use the Security & Compliance Center to remove Safe Links policies</span></span>

1. <span data-ttu-id="1f845-230">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-230">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span>

2. <span data-ttu-id="1f845-231">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="1f845-231">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="1f845-232">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur Supprimer la **stratégie,** puis cliquez sur **Oui.**</span><span class="sxs-lookup"><span data-stu-id="1f845-232">In the policy details fly out that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies"></a><span data-ttu-id="1f845-233">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-233">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies</span></span>

<span data-ttu-id="1f845-234">Comme décrit précédemment, une stratégie de liens sécurisés se compose d’une stratégie de liens sécurisés et d’une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-234">As previously described, a Safe Links policy consists of a safe links policy and a safe links rule.</span></span>

<span data-ttu-id="1f845-235">Dans PowerShell, la différence entre les stratégies de liens sécurisés et les règles de liens sécurisés est évidente.</span><span class="sxs-lookup"><span data-stu-id="1f845-235">In PowerShell, the difference between safe links policies and safe links rules is apparent.</span></span> <span data-ttu-id="1f845-236">Vous gérez les stratégies de liens sécurisés à l’aide des cmdlets **\* -SafeLinksPolicy** et vous gérez les règles de liens sécurisés à l’aide des cmdlets **\* -SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="1f845-236">You manage safe links policies by using the **\*-SafeLinksPolicy** cmdlets, and you manage safe links rules by using the **\*-SafeLinksRule** cmdlets.</span></span>

- <span data-ttu-id="1f845-237">Dans PowerShell, vous créez d’abord la stratégie de liens sécurisés, puis vous créez la règle de liens sécurisés qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="1f845-237">In PowerShell, you create the safe links policy first, then you create the safe links rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="1f845-238">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de liens sécurisés et de la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-238">In PowerShell, you modify the settings in the safe links policy and the safe links rule separately.</span></span>
- <span data-ttu-id="1f845-239">Lorsque vous supprimez une stratégie de liens sécurisés de PowerShell, la règle de liens sécurisés correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="1f845-239">When you remove a safe links policy from PowerShell, the corresponding safe links rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-links-policies"></a><span data-ttu-id="1f845-240">Utiliser PowerShell pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-240">Use PowerShell to create Safe Links policies</span></span>

<span data-ttu-id="1f845-241">La création d’une stratégie de liens sécurisés dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="1f845-241">Creating a Safe Links policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="1f845-242">Créez la stratégie de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-242">Create the safe links policy.</span></span>
2. <span data-ttu-id="1f845-243">Créez la règle de liens sécurisés qui spécifie la stratégie de liens sécurisés à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="1f845-243">Create the safe links rule that specifies the safe links policy that the rule applies to.</span></span>

> [!NOTE]
> 
> - <span data-ttu-id="1f845-244">Vous pouvez créer une règle de liens sécurisés et lui attribuer une stratégie de liens sécurisés non associés existante.</span><span class="sxs-lookup"><span data-stu-id="1f845-244">You can create a new safe links rule and assign an existing, unassociated safe links policy to it.</span></span> <span data-ttu-id="1f845-245">Une règle de liens sécurisés ne peut pas être associée à plusieurs stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-245">A safe links rule can't be associated with more than one safe links policy.</span></span>
> 
> - <span data-ttu-id="1f845-246">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de liens sécurisés dans PowerShell qui ne sont pas disponibles dans le Centre de sécurité & conformité tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="1f845-246">You can configure the following settings on new safe links policies in PowerShell that aren't available in the Security & Compliance Center until after you create the policy:</span></span>
> 
>   - <span data-ttu-id="1f845-247">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="1f845-247">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeLinksRule** cmdlet).</span></span>
>   - <span data-ttu-id="1f845-248">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="1f845-248">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeLinksRule** cmdlet).</span></span>
> 
> - <span data-ttu-id="1f845-249">Une nouvelle stratégie de liens sécurisés que vous créez dans PowerShell n’est pas visible dans le Centre de sécurité & conformité tant que vous n’avez pas attribué la stratégie à une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-249">A new safe links policy that you create in PowerShell isn't visible in the Security & Compliance Center until you assign the policy to a safe links rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-links-policy"></a><span data-ttu-id="1f845-250">Étape 1 : Utiliser PowerShell pour créer une stratégie de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-250">Step 1: Use PowerShell to create a safe links policy</span></span>

<span data-ttu-id="1f845-251">Pour créer une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-251">To create a safe links policy, use this syntax:</span></span>

```PowerShell
New-SafeLinksPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-IsEnabled <$true | $false>] [-EnableSafeLinksForTeams <$true | $false>] [-ScanUrls <$true | $false>] [-DeliverMessageAfterScan <$true | $false>] [-EnableForInternalSenders <$true | $false>] [-DoNotAllowClickThrough <$true | $false>] [-DoNotTrackUserClicks <$true | $false>] [-DoNotRewriteUrls "Entry1","Entry2",..."EntryN"]
```

> [!NOTE]
> 
> - <span data-ttu-id="1f845-252">Pour plus d’informations sur la syntaxe d’entrée à utiliser pour le paramètre _DoNotRewriteUrls,_ voir la [syntaxe d’entrée](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)pour la liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="1f845-252">For details about the entry syntax to use for the _DoNotRewriteUrls_ parameter, see [Entry syntax for the "Do not rewrite the following URLs" list](atp-safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>
> 
> - <span data-ttu-id="1f845-253">Pour obtenir une syntaxe supplémentaire que vous pouvez utiliser pour le paramètre _DoNotRewriteUrls_ lorsque vous modifiez des stratégies de liens sécurisés existantes à l’aide de la cmdlet **Set-SafeLinksPolicy,** consultez la section Utiliser [PowerShell](#use-powershell-to-modify-safe-links-policies) pour modifier les stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1f845-253">For additional syntax that you can use for the _DoNotRewriteUrls_ parameter when you modify existing safe links policies by using the **Set-SafeLinksPolicy** cmdlet, see the [Use PowerShell to modify safe links policies](#use-powershell-to-modify-safe-links-policies) section later in this article.</span></span>

<span data-ttu-id="1f845-254">Cet exemple crée une stratégie de liens sécurisés nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f845-254">This example creates a safe links policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="1f845-255">Activer l’analyse et la réécriture d’URL dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="1f845-255">Turn on URL scanning and rewriting in email messages.</span></span>
- <span data-ttu-id="1f845-256">Activer l’analyse des URL dans Teams (aperçu TAP uniquement).</span><span class="sxs-lookup"><span data-stu-id="1f845-256">Turn on URL scanning in Teams (TAP Preview only).</span></span>
- <span data-ttu-id="1f845-257">Activer l’analyse en temps réel des URL sur lesquelles vous avez cliqué, y compris les liens sur lesquels vous avez cliqué et qui pointent vers des fichiers.</span><span class="sxs-lookup"><span data-stu-id="1f845-257">Turn on real-time scanning of clicked URLs, including clicked links that point to files.</span></span>
- <span data-ttu-id="1f845-258">Attendez que l’analyse des URL soit terminée avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="1f845-258">Wait for URL scanning to complete before delivering the message.</span></span>
- <span data-ttu-id="1f845-259">Activer l’analyse et la réécriture d’URL pour les messages internes.</span><span class="sxs-lookup"><span data-stu-id="1f845-259">Turn on URL scanning and rewriting for internal messages.</span></span>
- <span data-ttu-id="1f845-260">Suivez les clics des utilisateurs liés à la protection contre les liens sécurisés (nous n’utilisons pas le paramètre _DoNotTrackUserClicks,_ et la valeur par défaut est $false, ce qui signifie que les clics utilisateur sont suivis).</span><span class="sxs-lookup"><span data-stu-id="1f845-260">Track user clicks related to Safe Links protection (we aren't using the _DoNotTrackUserClicks_ parameter, and the default value is $false, which means user clicks are tracked).</span></span>
- <span data-ttu-id="1f845-261">N’autorisez pas les utilisateurs à accéder à l’URL d’origine en cliquant.</span><span class="sxs-lookup"><span data-stu-id="1f845-261">Do not allow users to click through to the original URL.</span></span>

```PowerShell
New-SafeLinksPolicy -Name "Contoso All" -IsEnabled $true -EnableSafeLinksForTeams $true -ScanUrls $true -DeliverMessageAfterScan $true -EnableForInternalSenders $true -DoNotAllowClickThrough $true
```

<span data-ttu-id="1f845-262">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/new-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="1f845-262">For detailed syntax and parameter information, see [New-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/new-safelinkspolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-links-rule"></a><span data-ttu-id="1f845-263">Étape 2 : Utiliser PowerShell pour créer une règle de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-263">Step 2: Use PowerShell to create a safe links rule</span></span>

<span data-ttu-id="1f845-264">Pour créer une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-264">To create a safe links rule, use this syntax:</span></span>

```PowerShell
New-SafeLinksRule -Name "<RuleName>" -SafeLinksPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="1f845-265">Cet exemple crée une règle de liens sécurisés nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f845-265">This example creates a safe links rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="1f845-266">La règle est associée à la stratégie de liens sécurisés nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="1f845-266">The rule is associated with the safe links policy named Contoso All.</span></span>
- <span data-ttu-id="1f845-267">La règle s’applique à tous les destinataires du contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="1f845-267">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="1f845-268">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1f845-268">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="1f845-269">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="1f845-269">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeLinksRule -Name "Contoso All" -SafeLinksPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="1f845-270">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/new-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-270">For detailed syntax and parameter information, see [New-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/new-safelinksrule).</span></span>

### <a name="use-powershell-to-view-safe-links-policies"></a><span data-ttu-id="1f845-271">Utiliser PowerShell pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-271">Use PowerShell to view safe links policies</span></span>

<span data-ttu-id="1f845-272">Pour afficher les stratégies de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-272">To view existing safe links policies, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="1f845-273">Cet exemple renvoie une liste récapitulatif de toutes les stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-273">This example returns a summary list of all safe links policies.</span></span>

```PowerShell
Get-SafeLinksPolicy | Format-Table Name
```

<span data-ttu-id="1f845-274">Cet exemple renvoie des informations détaillées sur la stratégie de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="1f845-274">This example returns detailed information for the safe links policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksPolicy -Identity "Contoso Executives"
```

<span data-ttu-id="1f845-275">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/get-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="1f845-275">For detailed syntax and parameter information, see [Get-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/get-safelinkspolicy).</span></span>

### <a name="use-powershell-to-view-safe-links-rules"></a><span data-ttu-id="1f845-276">Utiliser PowerShell pour afficher les règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-276">Use PowerShell to view safe links rules</span></span>

<span data-ttu-id="1f845-277">Pour afficher les règles de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-277">To view existing safe links rules, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="1f845-278">Cet exemple renvoie une liste récapitulatif de toutes les règles de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1f845-278">This example returns a summary list of all safe links rules.</span></span>

```PowerShell
Get-SafeLinksRule | Format-Table Name,State
```

<span data-ttu-id="1f845-279">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f845-279">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeLinksRule -State Disabled
```

```PowerShell
Get-SafeLinksRule -State Enabled
```

<span data-ttu-id="1f845-280">Cet exemple renvoie des informations détaillées sur la règle de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="1f845-280">This example returns detailed information for the safe links rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksRule -Identity "Contoso Executives"
```

<span data-ttu-id="1f845-281">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/get-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-281">For detailed syntax and parameter information, see [Get-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/get-safelinksrule).</span></span>

### <a name="use-powershell-to-modify-safe-links-policies"></a><span data-ttu-id="1f845-282">Utiliser PowerShell pour modifier des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-282">Use PowerShell to modify safe links policies</span></span>

<span data-ttu-id="1f845-283">Vous ne pouvez pas renommer une stratégie de liens sécurisés dans PowerShell (la cmdlet **Set-SafeLinksPolicy** n’a pas _de paramètre_ Name).</span><span class="sxs-lookup"><span data-stu-id="1f845-283">You can't rename a safe links policy in PowerShell (the **Set-SafeLinksPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="1f845-284">Lorsque vous renommez une stratégie de liens sécurisés dans le Centre de sécurité & conformité, vous renommez uniquement la règle de liens _sécurisés._</span><span class="sxs-lookup"><span data-stu-id="1f845-284">When you rename a Safe Links policy in the Security & Compliance Center, you're only renaming the safe links _rule_.</span></span>

<span data-ttu-id="1f845-285">La seule considération supplémentaire pour modifier les stratégies de liens sécurisés dans PowerShell est la syntaxe disponible pour le paramètre _DoNotRewriteUrls_ (la liste « Ne pas réécrire les URL [suivantes](atp-safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)» ) :</span><span class="sxs-lookup"><span data-stu-id="1f845-285">The only additional consideration for modifying safe links policies in PowerShell is the available syntax for the _DoNotRewriteUrls_ parameter (the ["Do not rewrite the following URLs" list](atp-safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)):</span></span>

- <span data-ttu-id="1f845-286">Pour ajouter des valeurs qui remplaceront les entrées existantes, utilisez la syntaxe suivante `"Entry1","Entry2,..."EntryN"` :</span><span class="sxs-lookup"><span data-stu-id="1f845-286">To add values that will replace any existing entries, use the following syntax: `"Entry1","Entry2,..."EntryN"`.</span></span>
- <span data-ttu-id="1f845-287">Pour ajouter ou supprimer des valeurs sans affecter les autres entrées existantes, utilisez la syntaxe suivante : `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span><span class="sxs-lookup"><span data-stu-id="1f845-287">To add or remove values without affecting other existing entries, use the following syntax: `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span></span>

<span data-ttu-id="1f845-288">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de liens sécurisés, comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-a-safe-links-policy) pour créer une section de stratégie de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1f845-288">Otherwise, the same settings are available when you create a safe links policy as described in the [Step 1: Use PowerShell to create a safe links policy](#step-1-use-powershell-to-create-a-safe-links-policy) section earlier in this article.</span></span>

<span data-ttu-id="1f845-289">Pour modifier une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-289">To modify a safe links policy, use this syntax:</span></span>

```PowerShell
Set-SafeLinksPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="1f845-290">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/set-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="1f845-290">For detailed syntax and parameter information, see [Set-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/set-safelinkspolicy).</span></span>

### <a name="use-powershell-to-modify-safe-links-rules"></a><span data-ttu-id="1f845-291">Utiliser PowerShell pour modifier des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-291">Use PowerShell to modify safe links rules</span></span>

<span data-ttu-id="1f845-292">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de liens sécurisés dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="1f845-292">The only setting that's not available when you modify a safe links rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="1f845-293">Pour activer ou désactiver des règles de liens sécurisés existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="1f845-293">To enable or disable existing safe links rules, see the next section.</span></span>

<span data-ttu-id="1f845-294">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-a-safe-links-rule) pour créer une section de règle de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="1f845-294">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe links rule](#step-2-use-powershell-to-create-a-safe-links-rule) section earlier in this article.</span></span>

<span data-ttu-id="1f845-295">Pour modifier une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-295">To modify a safe links rule, use this syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="1f845-296">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-296">For detailed syntax and parameter information, see [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-links-rules"></a><span data-ttu-id="1f845-297">Utiliser PowerShell pour activer ou désactiver des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-297">Use PowerShell to enable or disable safe links rules</span></span>

<span data-ttu-id="1f845-298">L’activation ou la désactivation d’une règle de liens sécurisés dans PowerShell active ou désactive l’ensemble de la stratégie de liens sécurisés (la règle de liens sécurisés et la stratégie de liens sécurisés affectée).</span><span class="sxs-lookup"><span data-stu-id="1f845-298">Enabling or disabling a safe links rule in PowerShell enables or disables the whole Safe Links policy (the safe links rule and the assigned safe links policy).</span></span>

<span data-ttu-id="1f845-299">Pour activer ou désactiver une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-299">To enable or disable a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeLinksRule | Disable-SafeLinksRule> -Identity "<RuleName>"
```

<span data-ttu-id="1f845-300">Cet exemple désactive la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="1f845-300">This example disables the safe links rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="1f845-301">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="1f845-301">This example enables same rule.</span></span>

```PowerShell
Enable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="1f845-302">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/enable-safelinksrule) et [Disable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/disable-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-302">For detailed syntax and parameter information, see [Enable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/enable-safelinksrule) and [Disable-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/disable-safelinksrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-links-rules"></a><span data-ttu-id="1f845-303">Utiliser PowerShell pour définir la priorité des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-303">Use PowerShell to set the priority of safe links rules</span></span>

<span data-ttu-id="1f845-304">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle.</span><span class="sxs-lookup"><span data-stu-id="1f845-304">The highest priority value you can set on a rule is 0.</span></span> <span data-ttu-id="1f845-305">La valeur la plus basse que vous pouvez définir dépend du nombre de règles.</span><span class="sxs-lookup"><span data-stu-id="1f845-305">The lowest value you can set depends on the number of rules.</span></span> <span data-ttu-id="1f845-306">Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4.</span><span class="sxs-lookup"><span data-stu-id="1f845-306">For example, if you have five rules, you can use the priority values 0 through 4.</span></span> <span data-ttu-id="1f845-307">Tout changement de priorité d’une règle existante peut avoir un effet en cascade sur les autres règles.</span><span class="sxs-lookup"><span data-stu-id="1f845-307">Changing the priority of an existing rule can have a cascading effect on other rules.</span></span> <span data-ttu-id="1f845-308">Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="1f845-308">For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="1f845-309">Pour définir la priorité d’une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-309">To set the priority of a safe links rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="1f845-p123">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="1f845-p123">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeLinksRule -Identity "Marketing Department" -Priority 2
```

> [!NOTE]
> <span data-ttu-id="1f845-312">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="1f845-312">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeLinksRule** cmdlet instead.</span></span>

<span data-ttu-id="1f845-313">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-313">For detailed syntax and parameter information, see [Set-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-remove-safe-links-policies"></a><span data-ttu-id="1f845-314">Utiliser PowerShell pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-314">Use PowerShell to remove safe links policies</span></span>

<span data-ttu-id="1f845-315">Lorsque vous utilisez PowerShell pour supprimer une stratégie de liens sécurisés, la règle de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="1f845-315">When you use PowerShell to remove a safe links policy, the corresponding safe links rule isn't removed.</span></span>

<span data-ttu-id="1f845-316">Pour supprimer une stratégie de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-316">To remove a safe links policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="1f845-317">Cet exemple supprime la stratégie de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="1f845-317">This example removes the safe links policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "Marketing Department"
```

<span data-ttu-id="1f845-318">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="1f845-318">For detailed syntax and parameter information, see [Remove-SafeLinksPolicy](https://docs.microsoft.com/powershell/module/exchange/remove-safelinkspolicy).</span></span>

### <a name="use-powershell-to-remove-safe-links-rules"></a><span data-ttu-id="1f845-319">Utiliser PowerShell pour supprimer des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="1f845-319">Use PowerShell to remove safe links rules</span></span>

<span data-ttu-id="1f845-320">Lorsque vous utilisez PowerShell pour supprimer une règle de liens sécurisés, la stratégie de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="1f845-320">When you use PowerShell to remove a safe links rule, the corresponding safe links policy isn't removed.</span></span>

<span data-ttu-id="1f845-321">Pour supprimer une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="1f845-321">To remove a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "<PolicyName>"
```

<span data-ttu-id="1f845-322">Cet exemple supprime la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="1f845-322">This example removes the safe links rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="1f845-323">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/remove-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="1f845-323">For detailed syntax and parameter information, see [Remove-SafeLinksRule](https://docs.microsoft.com/powershell/module/exchange/remove-safelinksrule).</span></span>

<span data-ttu-id="1f845-324">Pour vérifier que la fonction Liens sécurisés analyse les messages, consultez les rapports Microsoft Defender pour Office 365 disponibles.</span><span class="sxs-lookup"><span data-stu-id="1f845-324">To verify that Safe Links is scanning messages, check the available Microsoft Defender for Office 365 reports.</span></span> <span data-ttu-id="1f845-325">Pour plus d’informations, voir Afficher les rapports pour Defender pour [Office 365](view-reports-for-atp.md) et Utiliser l’Explorateur dans le Centre de sécurité [& conformité.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="1f845-325">For more information, see [View reports for Defender for Office 365](view-reports-for-atp.md) and [Use Explorer in the Security & Compliance Center](threat-explorer.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="1f845-326">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="1f845-326">How do you know these procedures worked?</span></span>

<span data-ttu-id="1f845-327">Pour vérifier que vous avez correctement créé, modifié ou supprimé des stratégies de liens sécurisés, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f845-327">To verify that you've successfully created, modified, or removed Safe Links policies, do any of the following steps:</span></span>

- <span data-ttu-id="1f845-328">Dans le Centre de sécurité & conformité, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span><span class="sxs-lookup"><span data-stu-id="1f845-328">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**.</span></span> <span data-ttu-id="1f845-329">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="1f845-329">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="1f845-330">Pour afficher plus de détails, sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="1f845-330">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="1f845-331">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez \<Name\> les paramètres :</span><span class="sxs-lookup"><span data-stu-id="1f845-331">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeLinksPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-SafeLinksRule -Identity "<Name>"
  ```
