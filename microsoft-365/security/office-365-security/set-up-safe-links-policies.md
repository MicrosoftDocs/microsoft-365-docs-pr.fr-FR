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
ms.openlocfilehash: 40ae52cfce53c3fa14253a94e72f1a2bccda9a86
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52929826"
---
# <a name="set-up-safe-links-policies-in-microsoft-defender-for-office-365"></a><span data-ttu-id="a40c2-103">Configurer des stratégies de liens sécurisés dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="a40c2-103">Set up Safe Links policies in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a40c2-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a40c2-104">**Applies to**</span></span>
- [<span data-ttu-id="a40c2-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="a40c2-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="a40c2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a40c2-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!IMPORTANT]
> <span data-ttu-id="a40c2-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="a40c2-107">This article is intended for business customers who have [Microsoft Defender for Office 365](defender-for-office-365.md).</span></span> <span data-ttu-id="a40c2-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur les liens sécurisés dans Outlook, voir [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="a40c2-108">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="a40c2-109">La fonctionnalité Liens sécurisés de [Microsoft Defender](defender-for-office-365.md) pour Office 365 permet d’analyser les URL des messages électroniques entrants dans le flux de messagerie et de vérifier en un clic les URL et les liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="a40c2-109">Safe Links is a feature in [Microsoft Defender for Office 365](defender-for-office-365.md) that provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="a40c2-110">Pour plus d’informations, [voir Liens sécurisés dans Microsoft Defender pour Office 365](safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="a40c2-110">For more information, see [Safe Links in Microsoft Defender for Office 365](safe-links.md).</span></span>

<span data-ttu-id="a40c2-111">Il n’existe aucune stratégie de liens sécurisés intégrée ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="a40c2-111">There's no built-in or default Safe Links policy.</span></span> <span data-ttu-id="a40c2-112">Pour obtenir l’analyse des URL par des liens sécurisés, vous devez créer une ou plusieurs stratégies de liens sécurisés, comme décrit dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a40c2-112">To get Safe Links scanning of URLs, you need to create one or more Safe Links policies as described in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="a40c2-113">Vous configurez les paramètres globaux pour la **protection** des liens sécurisés en dehors des stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-113">You configure the global settings for Safe Links protection **outside** of Safe Links policies.</span></span> <span data-ttu-id="a40c2-114">Pour obtenir des instructions, voir [Configurer les paramètres globaux](configure-global-settings-for-safe-links.md)des liens sécurisés dans Microsoft Defender pour Office 365 .</span><span class="sxs-lookup"><span data-stu-id="a40c2-114">For instructions, see [Configure global settings for Safe Links in Microsoft Defender for Office 365](configure-global-settings-for-safe-links.md).</span></span>

<span data-ttu-id="a40c2-115">Vous pouvez configurer des stratégies de liens sécurisés dans le portail Microsoft 365 Defender ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec Microsoft Defender pour les abonnements de modules supplémentaires Office 365).</span><span class="sxs-lookup"><span data-stu-id="a40c2-115">You can configure Safe Links policies in the Microsoft 365 Defender portal or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Microsoft Defender for Office 365 add-on subscriptions).</span></span>

<span data-ttu-id="a40c2-116">Les éléments de base d’une stratégie de liens sécurisés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a40c2-116">The basic elements of a Safe Links policy are:</span></span>

- <span data-ttu-id="a40c2-117">La stratégie de liens sécurisés : activer la protection contre les liens sécurisés, activer l’analyse des URL en temps réel, spécifier s’il faut attendre la fin de l’analyse en temps réel avant de remettre le message, activer l’analyse des messages internes, spécifier s’il faut suivre les clics des utilisateurs sur les URL et spécifier s’il faut autoriser les utilisateurs à cliquer sur l’URL d’origine.</span><span class="sxs-lookup"><span data-stu-id="a40c2-117">**The safe links policy**: Turn on Safe Links protection, turn on real-time URL scanning, specify whether to wait for real-time scanning to complete before delivering the message, turn on scanning for internal messages, specify whether to track user clicks on URLs, and specify whether to allow users to click trough to the original URL.</span></span>
- <span data-ttu-id="a40c2-118">**La règle de liens sécurisés**: spécifie la priorité et les filtres de destinataires (à qui s’applique la stratégie).</span><span class="sxs-lookup"><span data-stu-id="a40c2-118">**The safe links rule**: Specifies the priority and recipient filters (who the policy applies to).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a40c2-119">Les administrateurs doivent prendre en compte les différents paramètres de configuration pour SafeLinks.</span><span class="sxs-lookup"><span data-stu-id="a40c2-119">Admins should consider the different configuration settings for SafeLinks.</span></span> <span data-ttu-id="a40c2-120">L’une des options disponibles consiste à inclure des informations d’identification utilisateur dans SafeLinks.</span><span class="sxs-lookup"><span data-stu-id="a40c2-120">One of the available options is to include user identifiable information in SafeLinks.</span></span> <span data-ttu-id="a40c2-121">Cette fonctionnalité permet aux équipes *d’opérations* de sécurité d’examiner la compromission potentielle de l’utilisateur, de prendre des mesures correctives et de limiter les violations coûteuses.</span><span class="sxs-lookup"><span data-stu-id="a40c2-121">This feature enables *Security Ops teams* to investigate potential user compromise, take corrective action, and limit costly breaches.</span></span>

<span data-ttu-id="a40c2-122">La différence entre ces deux éléments n’est pas évidente lorsque vous gérez les polices de liens sécurisés dans le portail Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="a40c2-122">The difference between these two elements isn't obvious when you manage Safe Links polices in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="a40c2-123">Lorsque vous créez une stratégie de liens sécurisés, vous créez en même temps une règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="a40c2-123">When you create a Safe Links policy, you're actually creating a safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>
- <span data-ttu-id="a40c2-124">Lorsque vous modifiez une stratégie de liens sécurisés, les paramètres liés au nom, à la priorité, activé ou désactivé, et aux filtres de destinataire modifient la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-124">When you modify a Safe Links policy, settings related to the name, priority, enabled or disabled, and recipient filters modify the safe links rule.</span></span> <span data-ttu-id="a40c2-125">Tous les autres paramètres modifient la stratégie de liens sécurisés associée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-125">All other settings modify the associated safe links policy.</span></span>
- <span data-ttu-id="a40c2-126">Lorsque vous supprimez une stratégie de liens sécurisés, la règle de liens sécurisés et la stratégie de liens sécurisés associée sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="a40c2-126">When you remove a Safe Links policy, the safe links rule and the associated safe links policy are removed.</span></span>

<span data-ttu-id="a40c2-127">Dans Exchange Online PowerShell ou EOP PowerShell autonome, vous gérez la stratégie et la règle séparément.</span><span class="sxs-lookup"><span data-stu-id="a40c2-127">In Exchange Online PowerShell or standalone EOP PowerShell, you manage the policy and the rule separately.</span></span> <span data-ttu-id="a40c2-128">Pour plus d’informations, voir la section Utiliser Exchange Online PowerShell ou [EOP PowerShell](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) autonome pour configurer des stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a40c2-128">For more information, see the [Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies](#use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies) section later in this article.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a40c2-129">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a40c2-129">What do you need to know before you begin?</span></span>

- <span data-ttu-id="a40c2-130">Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com/>.</span><span class="sxs-lookup"><span data-stu-id="a40c2-130">You open the Microsoft 365 Defender portal at <https://security.microsoft.com/>.</span></span> <span data-ttu-id="a40c2-131">Pour aller directement à la page **Liens sécurisés,** utilisez <https://security.microsoft.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="a40c2-131">To go directly to the **Safe Links** page, use <https://security.microsoft.com/safelinksv2>.</span></span>

- <span data-ttu-id="a40c2-132">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="a40c2-132">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="a40c2-133">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="a40c2-133">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="a40c2-134">Des autorisations doivent vous être attribuées avant de pouvoir suivre les procédures de cet article :</span><span class="sxs-lookup"><span data-stu-id="a40c2-134">You need to be assigned permissions before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="a40c2-135">Pour créer, modifier et supprimer des stratégies de liens  sécurisés, vous devez être membre des  groupes de rôles Gestion de l’organisation ou Administrateur de la sécurité dans le portail Microsoft 365 Defender et membre du groupe de rôles Gestion de l’organisation dans Exchange Online.  </span><span class="sxs-lookup"><span data-stu-id="a40c2-135">To create, modify, and delete Safe Links policies, you need to be a member of the **Organization Management** or **Security Administrator** role groups in the Microsoft 365 Defender portal **and** a member of the **Organization Management** role group in Exchange Online.</span></span>
  - <span data-ttu-id="a40c2-136">Pour accéder en lecture seule aux stratégies de liens  sécurisés, vous devez être membre des groupes de rôles Lecteur global ou Lecteur **de** sécurité.</span><span class="sxs-lookup"><span data-stu-id="a40c2-136">For read-only access to Safe Links policies, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="a40c2-137">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender](permissions-in-the-security-and-compliance-center.md) et [autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="a40c2-137">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md) and [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  > [!NOTE]
  > 
  > - <span data-ttu-id="a40c2-138">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne  aux utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a40c2-138">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="a40c2-139">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a40c2-139">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  <span data-ttu-id="a40c2-140">.</span><span class="sxs-lookup"><span data-stu-id="a40c2-140">.</span></span> <span data-ttu-id="a40c2-141">- Le **groupe de rôles** Gestion de l’organisation en affichage seul dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) donne également un accès en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a40c2-141">- The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="a40c2-142">Pour obtenir nos paramètres recommandés pour les stratégies de liens sécurisés, consultez les [paramètres de stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="a40c2-142">For our recommended settings for Safe Links policies, see [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).</span></span>

- <span data-ttu-id="a40c2-143">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-143">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="a40c2-144">[De nouvelles fonctionnalités sont continuellement ajoutées à Microsoft Defender pour Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="a40c2-144">[New features are continually being added to Microsoft Defender for Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="a40c2-145">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements à vos stratégies de liens sécurisés existantes.</span><span class="sxs-lookup"><span data-stu-id="a40c2-145">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-create-safe-links-policies"></a><span data-ttu-id="a40c2-146">Utiliser le portail Microsoft 365 Defender pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-146">Use the Microsoft 365 Defender portal to create Safe Links policies</span></span>

<span data-ttu-id="a40c2-147">La création d’une stratégie de liens sécurisés personnalisée dans le portail Microsoft 365 Defender crée la règle de liens sécurisés et la stratégie de liens sécurisés associée en utilisant le même nom pour les deux.</span><span class="sxs-lookup"><span data-stu-id="a40c2-147">Creating a custom Safe Links policy in the Microsoft 365 Defender portal creates the safe links rule and the associated safe links policy at the same time using the same name for both.</span></span>

1. <span data-ttu-id="a40c2-148">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-148">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-149">Dans la page **Liens sécurisés,** cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-149">On the **Safe Links** page, click **Create**.</span></span>

3. <span data-ttu-id="a40c2-150">**L’Assistant Nouvelle stratégie de liens sécurisés** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="a40c2-150">The **New Safe Links policy** wizard opens.</span></span> <span data-ttu-id="a40c2-151">Dans la page **Nom de votre stratégie,** configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a40c2-151">On the **Name your policy** page, configure the following settings:</span></span>

   - <span data-ttu-id="a40c2-152">**Nom** Entrez un nom unique et descriptif pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a40c2-152">**Name**: Enter a unique, descriptive name for the policy.</span></span>

   - <span data-ttu-id="a40c2-153">**Description** Entrez une description facultative pour la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a40c2-153">**Description**: Enter an optional description for the policy.</span></span>

   <span data-ttu-id="a40c2-154">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-154">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="a40c2-155">Sur la **Paramètres** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a40c2-155">On the **Settings** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="a40c2-156">**Sélectionnez l’action pour les URL potentiellement malveillantes inconnues** dans les messages : sélectionnez **Activé** pour activer la protection des liens vers des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a40c2-156">**Select the action for unknown potentially malicious URLs in messages**: Select **On** to enable Safe Links protection for links in email messages.</span></span>

   - <span data-ttu-id="a40c2-157">**Sélectionnez l’action** pour les URL inconnues ou  potentiellement malveillantes dans Microsoft Teams : sélectionnez Activé pour activer la protection des liens sécurisés pour les liens Teams.</span><span class="sxs-lookup"><span data-stu-id="a40c2-157">**Select the action for unknown or potentially malicious URLs within Microsoft Teams**: Select **On** to enable Safe Links protection for links in Teams.</span></span>

   - <span data-ttu-id="a40c2-158">**Appliquez l’analyse** des URL en temps réel pour les liens suspects et les liens pointant vers des fichiers : sélectionnez ce paramètre pour activer l’analyse en temps réel des liens dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a40c2-158">**Apply real-time URL scanning for suspicious links and links that point to files**: Select this setting to enable real-time scanning of links in email messages.</span></span>

   - <span data-ttu-id="a40c2-159">**Attendez que l’analyse des URL** se termine avant de remettre le message : sélectionnez ce paramètre pour attendre la fin de l’analyse de l’URL en temps réel avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="a40c2-159">**Wait for URL scanning to complete before delivering the message**: Select this setting to wait for real-time URL scanning to complete before delivering the message.</span></span>

   - <span data-ttu-id="a40c2-160">**Appliquer des liens sûrs** aux messages électroniques envoyés au sein de l’organisation : sélectionnez ce paramètre pour appliquer la stratégie de liens sécurisés aux messages entre les expéditeurs internes et les destinataires internes.</span><span class="sxs-lookup"><span data-stu-id="a40c2-160">**Apply Safe Links to email messages sent within the organization**: Select this setting to apply the Safe Links policy to messages between internal senders and internal recipients.</span></span>

   - <span data-ttu-id="a40c2-161">**Ne pas suivre les clics** de l’utilisateur : laissez ce paramètre désélectionnés pour activer les clics de l’utilisateur de suivi sur les URL des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a40c2-161">**Do not track user clicks**: Leave this setting unselected to enable the tracking user clicks on URLs in email messages.</span></span>

   - <span data-ttu-id="a40c2-162">**N’autorisez pas** les utilisateurs à cliquer sur l’URL d’origine : sélectionnez ce paramètre pour empêcher les utilisateurs de cliquer jusqu’à l’URL d’origine dans les [pages d’avertissement.](safe-links.md#warning-pages-from-safe-links)</span><span class="sxs-lookup"><span data-stu-id="a40c2-162">**Do not allow users to click through to original URL**: Select this setting to block users from clicking through to the original URL in [warning pages](safe-links.md#warning-pages-from-safe-links).</span></span>

   - <span data-ttu-id="a40c2-163">**Ne réécrivez pas les** URL suivantes : permet d’accéder aux URL spécifiées qui seraient autrement bloquées par les liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-163">**Do not rewrite the following URLs**: Allows access the specified URLs that would otherwise be blocked by Safe Links.</span></span>

     <span data-ttu-id="a40c2-164">Dans la zone, tapez l’URL ou la valeur de votre souhaitez, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="a40c2-164">In the box, type the URL or value that you want, and then click</span></span> ![Icône Ajouter un bouton](../../media/ITPro-EAC-AddIcon.png)<span data-ttu-id="a40c2-166">.</span><span class="sxs-lookup"><span data-stu-id="a40c2-166">.</span></span>

     <span data-ttu-id="a40c2-167">Pour supprimer une entrée existante, sélectionnez-la, puis cliquez sur</span><span class="sxs-lookup"><span data-stu-id="a40c2-167">To remove an existing entry, select it and then click</span></span> ![Icône Supprimer le bouton](../../media/ITPro-EAC-DeleteIcon.png)<span data-ttu-id="a40c2-169">.</span><span class="sxs-lookup"><span data-stu-id="a40c2-169">.</span></span>

     <span data-ttu-id="a40c2-170">Pour la syntaxe d’entrée, voir [syntaxe d’entrée pour la](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="a40c2-170">For entry syntax, see [Entry syntax for the "Do not rewrite the following URLs" list](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>

   <span data-ttu-id="a40c2-171">Pour plus d’informations sur ces paramètres, consultez la liste des paramètres de liens [sécurisés](safe-links.md#safe-links-settings-for-email-messages) pour les messages électroniques et les [paramètres](safe-links.md#safe-links-settings-for-microsoft-teams)de liens Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="a40c2-171">For detailed information about these settings, see [Safe Links settings for email messages](safe-links.md#safe-links-settings-for-email-messages) and [Safe Links settings for Microsoft Teams](safe-links.md#safe-links-settings-for-microsoft-teams).</span></span>

   <span data-ttu-id="a40c2-172">Pour plus d’informations sur les valeurs recommandées pour les paramètres de stratégie Standard et Strict, voir Paramètres de [stratégie de liens sécurisés.](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings)</span><span class="sxs-lookup"><span data-stu-id="a40c2-172">For more the recommended values for Standard and Strict policy settings, see [Safe Links policy settings](recommended-settings-for-eop-and-office365.md#safe-links-policy-settings).</span></span>

   <span data-ttu-id="a40c2-173">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-173">When you're finished, click **Next**.</span></span>

5. <span data-ttu-id="a40c2-174">Dans la page **Appliqué à** qui s’affiche, identifiez les destinataires internes à qui s’applique la stratégie.</span><span class="sxs-lookup"><span data-stu-id="a40c2-174">On the **Applied to** page that appears, identify the internal recipients that the policy applies to.</span></span>

   <span data-ttu-id="a40c2-175">Vous pouvez uniquement utiliser une condition ou une exception une seule fois, mais vous pouvez spécifier plusieurs valeurs pour la condition ou l’exception.</span><span class="sxs-lookup"><span data-stu-id="a40c2-175">You can only use a condition or exception once, but you can specify multiple values for the condition or exception.</span></span> <span data-ttu-id="a40c2-176">Plusieurs valeurs de la même condition ou exception utilisent la logique OU (par exemple, _\<recipient1\>_ ou _\<recipient2\>_).</span><span class="sxs-lookup"><span data-stu-id="a40c2-176">Multiple values of the same condition or exception use OR logic (for example, _\<recipient1\>_ or _\<recipient2\>_).</span></span> <span data-ttu-id="a40c2-177">Des conditions ou des exceptions différentes utilisent la logique ET (par exemple, _\<recipient1\>_ et _\<member of group 1\>_).</span><span class="sxs-lookup"><span data-stu-id="a40c2-177">Different conditions or exceptions use AND logic (for example, _\<recipient1\>_ and _\<member of group 1\>_).</span></span>

   <span data-ttu-id="a40c2-178">Cliquez **sur Ajouter une condition.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-178">Click **Add a condition**.</span></span> <span data-ttu-id="a40c2-179">Dans ladown qui s’affiche, sélectionnez une condition sous **Applied si**:</span><span class="sxs-lookup"><span data-stu-id="a40c2-179">In the dropdown that appears, select a condition under **Applied if**:</span></span>

   - <span data-ttu-id="a40c2-180">**Le destinataire est**: Spécifie une ou plusieurs boîtes aux lettres, utilisateurs de messagerie ou contacts de messagerie dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a40c2-180">**The recipient is**: Specifies one or more mailboxes, mail users, or mail contacts in your organization.</span></span>
   - <span data-ttu-id="a40c2-181">**Le destinataire est membre de**: Spécifie un ou plusieurs groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a40c2-181">**The recipient is a member of**: Specifies one or more groups in your organization.</span></span>
   - <span data-ttu-id="a40c2-182">**Le domaine du destinataire est** : spécifie les destinataires dans un ou plusieurs domaines configurés et acceptés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a40c2-182">**The recipient domain is**: Specifies recipients in one or more of the configured accepted domains in your organization.</span></span>

   <span data-ttu-id="a40c2-183">Une fois que vous avez sélectionné la condition, une zone « Tout » apparaît dans la zone « **Tout le** monde ».</span><span class="sxs-lookup"><span data-stu-id="a40c2-183">After you select the condition, a corresponding dropdown appears with an **Any of these** box.</span></span>

   - <span data-ttu-id="a40c2-184">Cliquez dans la zone et faites défiler la liste des valeurs à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="a40c2-184">Click in the box and scroll through the list of values to select.</span></span>
   - <span data-ttu-id="a40c2-185">Cliquez dans la zone et commencez à taper pour filtrer la liste et sélectionnez une valeur.</span><span class="sxs-lookup"><span data-stu-id="a40c2-185">Click in the box and start typing to filter the list and select a value.</span></span>
   - <span data-ttu-id="a40c2-186">Pour ajouter des valeurs supplémentaires, cliquez dans une zone vide dans la zone.</span><span class="sxs-lookup"><span data-stu-id="a40c2-186">To add additional values, click in an empty area in the box.</span></span>
   - <span data-ttu-id="a40c2-187">Pour supprimer des entrées individuelles, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la valeur.</span><span class="sxs-lookup"><span data-stu-id="a40c2-187">To remove individual entries, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the value.</span></span>
   - <span data-ttu-id="a40c2-188">Pour supprimer la condition entière, cliquez **sur Supprimer** ![ l’icône ](../../media/scc-remove-icon.png) sur la condition.</span><span class="sxs-lookup"><span data-stu-id="a40c2-188">To remove the whole condition, click **Remove** ![Remove icon](../../media/scc-remove-icon.png) on the condition.</span></span>

   <span data-ttu-id="a40c2-189">Pour ajouter une condition supplémentaire, cliquez sur **Ajouter une condition** et sélectionnez une valeur restante sous Appliqué **si**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-189">To add an additional condition, click **Add a condition** and select a remaining value under **Applied if**.</span></span>

   <span data-ttu-id="a40c2-190">Pour ajouter des exceptions, cliquez **sur Ajouter une condition** et sélectionnez une exception sous Sauf **si**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-190">To add exceptions, click **Add a condition** and select an exception under **Except if**.</span></span> <span data-ttu-id="a40c2-191">Les paramètres et le comportement sont exactement comme les conditions.</span><span class="sxs-lookup"><span data-stu-id="a40c2-191">The settings and behavior are exactly like the conditions.</span></span>

   <span data-ttu-id="a40c2-192">Lorsque vous avez terminé, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-192">When you're finished, click **Next**.</span></span>

6. <span data-ttu-id="a40c2-193">Dans la page **Examiner vos paramètres** qui s’affiche, examinez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="a40c2-193">On the **Review your settings** page that appears, review your settings.</span></span> <span data-ttu-id="a40c2-194">Vous pouvez cliquer **sur Modifier** sur chaque paramètre pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="a40c2-194">You can click **Edit** on each setting to modify it.</span></span>

   <span data-ttu-id="a40c2-195">Lorsque vous avez terminé, cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-195">When you're finished, click **Finish**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-view-safe-links-policies"></a><span data-ttu-id="a40c2-196">Utiliser le portail Microsoft 365 Defender pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-196">Use the Microsoft 365 Defender portal to view Safe Links policies</span></span>

1. <span data-ttu-id="a40c2-197">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-197">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-198">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="a40c2-198">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

   <span data-ttu-id="a40c2-199">Les détails de la stratégie apparaissent dans un volant</span><span class="sxs-lookup"><span data-stu-id="a40c2-199">The policy details appear in a fly out</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-modify-safe-links-policies"></a><span data-ttu-id="a40c2-200">Utiliser le portail Microsoft 365 Defender pour modifier les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-200">Use the Microsoft 365 Defender portal to modify Safe Links policies</span></span>

1. <span data-ttu-id="a40c2-201">Dans le portail Microsoft 365 Defender, go to \***Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-201">In the Microsoft 365 Defender portal, go to \***Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-202">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="a40c2-202">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="a40c2-203">Dans le volant des détails de stratégie qui s’affiche, cliquez **sur Modifier la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-203">In the policy details fly out that appears, click **Edit policy**.</span></span>

<span data-ttu-id="a40c2-204">Les paramètres disponibles dans le volant qui s’affiche sont identiques à ceux décrits dans la section Utiliser le portail Microsoft 365 Defender pour créer des stratégies de liens [sécurisés.](#use-the-microsoft-365-defender-portal-to-create-safe-links-policies)</span><span class="sxs-lookup"><span data-stu-id="a40c2-204">The available settings in the fly out that appears are identical to those described in the [Use the Microsoft 365 Defender portal to create Safe Links policies](#use-the-microsoft-365-defender-portal-to-create-safe-links-policies) section.</span></span>

<span data-ttu-id="a40c2-205">Pour activer ou désactiver une stratégie ou définir l’ordre de priorité de la stratégie, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a40c2-205">To enable or disable a policy or set the policy priority order, see the following sections.</span></span>

### <a name="enable-or-disable-safe-links-policies"></a><span data-ttu-id="a40c2-206">Activer ou désactiver les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-206">Enable or disable Safe Links policies</span></span>

1. <span data-ttu-id="a40c2-207">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-207">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-208">Notez la valeur dans la **colonne État** :</span><span class="sxs-lookup"><span data-stu-id="a40c2-208">Notice the value in the **Status** column:</span></span>

   - <span data-ttu-id="a40c2-209">Déplacez le bouton bascule vers la gauche pour désactiver la stratégie :</span><span class="sxs-lookup"><span data-stu-id="a40c2-209">Move the toggle to the left to disable the policy:</span></span> ![Désactiver la stratégie](../../media/scc-toggle-off.png)<span data-ttu-id="a40c2-211">.</span><span class="sxs-lookup"><span data-stu-id="a40c2-211">.</span></span>

   - <span data-ttu-id="a40c2-212">Déplacez le bouton bascule vers la droite pour activer la stratégie :</span><span class="sxs-lookup"><span data-stu-id="a40c2-212">Move the toggle to the right to enable the policy:</span></span> ![Activer la stratégie](../../media/scc-toggle-on.png)<span data-ttu-id="a40c2-214">.</span><span class="sxs-lookup"><span data-stu-id="a40c2-214">.</span></span>

### <a name="set-the-priority-of-safe-links-policies"></a><span data-ttu-id="a40c2-215">Définir la priorité des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-215">Set the priority of Safe Links policies</span></span>

<span data-ttu-id="a40c2-216">Par défaut, les stratégies de liens sécurisés ont une priorité qui est basée sur l’ordre dans quoi elles ont été créées (les stratégies les plus nouvelles sont moins prioritaires que les stratégies plus anciennes).</span><span class="sxs-lookup"><span data-stu-id="a40c2-216">By default, Safe Links policies are given a priority that's based on the order they were created in (newer polices are lower priority than older policies).</span></span> <span data-ttu-id="a40c2-217">Un numéro de priorité inférieur indique une priorité plus élevée pour la stratégie (la valeur 0 est la plus élevée) et les stratégies sont traitées dans l’ordre de priorité (les stratégies de priorité supérieure sont traitées avant les stratégies de priorité inférieure).</span><span class="sxs-lookup"><span data-stu-id="a40c2-217">A lower priority number indicates a higher priority for the policy (0 is the highest), and policies are processed in priority order (higher priority policies are processed before lower priority policies).</span></span> <span data-ttu-id="a40c2-218">Aucune stratégie ne peut avoir la même priorité, et le traitement de stratégie s’arrête une fois la première stratégie appliquée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-218">No two policies can have the same priority, and policy processing stops after the first policy is applied.</span></span>

<span data-ttu-id="a40c2-219">Pour plus d’informations sur l’ordre de priorité et l’évaluation et l’application de plusieurs stratégies, consultez [Ordre et la priorité de la protection de la messagerie](how-policies-and-protections-are-combined.md).</span><span class="sxs-lookup"><span data-stu-id="a40c2-219">For more information about the order of precedence and how multiple policies are evaluated and applied, see [Order and precedence of email protection](how-policies-and-protections-are-combined.md).</span></span>

<span data-ttu-id="a40c2-220">Les stratégies de liens sécurisés sont affichées dans l’ordre de traitement (la première stratégie a la valeur Priority 0). </span><span class="sxs-lookup"><span data-stu-id="a40c2-220">Safe Links policies are displayed in the order they're processed (the first policy has the **Priority** value 0).</span></span>

> [!NOTE]
> <span data-ttu-id="a40c2-221">Dans le Microsoft 365 Defender, vous ne pouvez modifier la priorité de la stratégie de liens sécurisés qu’une fois que vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="a40c2-221">In the Microsoft 365 Defender portal, you can only change the priority of the Safe Links policy after you create it.</span></span> <span data-ttu-id="a40c2-222">Dans PowerShell, vous pouvez remplacer la priorité par défaut lorsque vous créez la règle de liens sécurisés (ce qui peut affecter la priorité des règles existantes).</span><span class="sxs-lookup"><span data-stu-id="a40c2-222">In PowerShell, you can override the default priority when you create the safe links rule (which can affect the priority of existing rules).</span></span>

<span data-ttu-id="a40c2-223">Pour modifier la priorité d’une stratégie, déplacez-la vers le haut ou  vers le bas de la liste (vous ne pouvez pas modifier directement le numéro de priorité dans le portail Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="a40c2-223">To change the priority of a policy, move the policy up or down in the list (you can't directly modify the **Priority** number in the Microsoft 365 Defender portal).</span></span>

1. <span data-ttu-id="a40c2-224">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-224">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-225">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="a40c2-225">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="a40c2-226">Dans le volant des détails de stratégie qui s’affiche, cliquez sur le bouton de priorité disponible :</span><span class="sxs-lookup"><span data-stu-id="a40c2-226">In the policy details fly out that appears, click the available priority button:</span></span>

   - <span data-ttu-id="a40c2-227">La stratégie de liens sécurisés avec la valeur **de** priorité **0** ne dispose que **du** bouton Diminuer la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="a40c2-227">The Safe Links policy with the **Priority** value **0** has only the **Decrease priority** button available.</span></span>

   - <span data-ttu-id="a40c2-228">La stratégie de liens sécurisés avec la valeur **de** priorité la plus faible **(par** exemple, 3 ) ne dispose que du bouton **Augmenter** la priorité disponible.</span><span class="sxs-lookup"><span data-stu-id="a40c2-228">The Safe Links policy with the lowest **Priority** value (for example, **3**) has only the **Increase priority** button available.</span></span>

   - <span data-ttu-id="a40c2-229">Si vous disposez de trois stratégies de liens sécurisés ou  plus,  les stratégies entre les valeurs de priorité les plus élevées et les plus faibles disposent à la fois des boutons Augmenter la priorité et Diminuer la priorité.</span><span class="sxs-lookup"><span data-stu-id="a40c2-229">If you have three or more Safe Links policies, policies between the highest and lowest priority values have both the **Increase priority** and **Decrease priority** buttons available.</span></span>

4. <span data-ttu-id="a40c2-230">Cliquez **sur Augmenter la priorité** ou Diminuer la **priorité** pour modifier la **valeur** Priorité.</span><span class="sxs-lookup"><span data-stu-id="a40c2-230">Click **Increase priority** or **Decrease priority** to change the **Priority** value.</span></span>

5. <span data-ttu-id="a40c2-231">Lorsque vous avez terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-231">When you're finished, click **Close**.</span></span>

## <a name="use-the-microsoft-365-defender-portal-to-remove-safe-links-policies"></a><span data-ttu-id="a40c2-232">Utiliser le portail Microsoft 365 Defender pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-232">Use the Microsoft 365 Defender portal to remove Safe Links policies</span></span>

1. <span data-ttu-id="a40c2-233">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat Policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-233">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat Policies** \> **Safe Links**.</span></span>

2. <span data-ttu-id="a40c2-234">Dans la page **Liens sécurisés,** sélectionnez une stratégie dans la liste et cliquez dessus (ne cochez pas la case).</span><span class="sxs-lookup"><span data-stu-id="a40c2-234">On the **Safe Links** page, select a policy from the list and click on it (don't select the check box).</span></span>

3. <span data-ttu-id="a40c2-235">Dans la boîte de dialogue d’avertissement qui s’affiche, cliquez sur Supprimer la **stratégie,** puis cliquez sur **Oui.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-235">In the policy details fly out that appears, click **Delete policy**, and then click **Yes** in the warning dialog that appears.</span></span>

## <a name="use-exchange-online-powershell-or-standalone-eop-powershell-to-configure-safe-links-policies"></a><span data-ttu-id="a40c2-236">Utiliser Exchange Online PowerShell ou EOP PowerShell autonome pour configurer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-236">Use Exchange Online PowerShell or standalone EOP PowerShell to configure Safe Links policies</span></span>

<span data-ttu-id="a40c2-237">Comme décrit précédemment, une stratégie de liens sécurisés se compose d’une stratégie de liens sécurisés et d’une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-237">As previously described, a Safe Links policy consists of a safe links policy and a safe links rule.</span></span>

<span data-ttu-id="a40c2-238">Dans PowerShell, la différence entre les stratégies de liens sécurisés et les règles de liens sécurisés est évidente.</span><span class="sxs-lookup"><span data-stu-id="a40c2-238">In PowerShell, the difference between safe links policies and safe links rules is apparent.</span></span> <span data-ttu-id="a40c2-239">Vous gérez les stratégies de liens sécurisés à l’aide des cmdlets **\* -SafeLinksPolicy** et vous gérez les règles de liens sécurisés à l’aide des cmdlets **\* -SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-239">You manage safe links policies by using the **\*-SafeLinksPolicy** cmdlets, and you manage safe links rules by using the **\*-SafeLinksRule** cmdlets.</span></span>

- <span data-ttu-id="a40c2-240">Dans PowerShell, vous créez d’abord la stratégie de liens sécurisés, puis vous créez la règle de liens sécurisés qui identifie la stratégie à qui s’applique la règle.</span><span class="sxs-lookup"><span data-stu-id="a40c2-240">In PowerShell, you create the safe links policy first, then you create the safe links rule that identifies the policy that the rule applies to.</span></span>
- <span data-ttu-id="a40c2-241">Dans PowerShell, vous modifiez séparément les paramètres de la stratégie de liens sécurisés et de la règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-241">In PowerShell, you modify the settings in the safe links policy and the safe links rule separately.</span></span>
- <span data-ttu-id="a40c2-242">Lorsque vous supprimez une stratégie de liens sécurisés de PowerShell, la règle de liens sécurisés correspondante n’est pas automatiquement supprimée, et inversement.</span><span class="sxs-lookup"><span data-stu-id="a40c2-242">When you remove a safe links policy from PowerShell, the corresponding safe links rule isn't automatically removed, and vice versa.</span></span>

### <a name="use-powershell-to-create-safe-links-policies"></a><span data-ttu-id="a40c2-243">Utiliser PowerShell pour créer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-243">Use PowerShell to create Safe Links policies</span></span>

<span data-ttu-id="a40c2-244">La création d’une stratégie de liens sécurisés dans PowerShell est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="a40c2-244">Creating a Safe Links policy in PowerShell is a two-step process:</span></span>

1. <span data-ttu-id="a40c2-245">Créez la stratégie de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-245">Create the safe links policy.</span></span>
2. <span data-ttu-id="a40c2-246">Créez la règle de liens sécurisés qui spécifie la stratégie de liens sécurisés à qui la règle s’applique.</span><span class="sxs-lookup"><span data-stu-id="a40c2-246">Create the safe links rule that specifies the safe links policy that the rule applies to.</span></span>

> [!NOTE]
> 
> - <span data-ttu-id="a40c2-247">Vous pouvez créer une règle de liens sécurisés et lui attribuer une stratégie de liens sécurisés non associés existante.</span><span class="sxs-lookup"><span data-stu-id="a40c2-247">You can create a new safe links rule and assign an existing, unassociated safe links policy to it.</span></span> <span data-ttu-id="a40c2-248">Une règle de liens sécurisés ne peut pas être associée à plusieurs stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-248">A safe links rule can't be associated with more than one safe links policy.</span></span>
> 
> - <span data-ttu-id="a40c2-249">Vous pouvez configurer les paramètres suivants sur les nouvelles stratégies de liens sécurisés dans PowerShell qui ne sont pas disponibles dans le portail Microsoft 365 Defender tant que vous n’avez pas créé la stratégie :</span><span class="sxs-lookup"><span data-stu-id="a40c2-249">You can configure the following settings on new safe links policies in PowerShell that aren't available in the Microsoft 365 Defender portal until after you create the policy:</span></span>
> 
>   - <span data-ttu-id="a40c2-250">Créez la stratégie comme _désactivée_ ( activée sur la `$false` cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="a40c2-250">Create the new policy as disabled (_Enabled_ `$false` on the **New-SafeLinksRule** cmdlet).</span></span>
>   - <span data-ttu-id="a40c2-251">Définissez la priorité de la stratégie lors de la création (_Priorité_ ) sur la _\<Number\>_ cmdlet **New-SafeLinksRule).**</span><span class="sxs-lookup"><span data-stu-id="a40c2-251">Set the priority of the policy during creation (_Priority_ _\<Number\>_) on the **New-SafeLinksRule** cmdlet).</span></span>
> 
> - <span data-ttu-id="a40c2-252">Une nouvelle stratégie de liens sécurisés que vous créez dans PowerShell n’est pas visible dans le portail Microsoft 365 Defender tant que vous n’avez pas attribué la stratégie à une règle de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-252">A new safe links policy that you create in PowerShell isn't visible in the Microsoft 365 Defender portal until you assign the policy to a safe links rule.</span></span>

#### <a name="step-1-use-powershell-to-create-a-safe-links-policy"></a><span data-ttu-id="a40c2-253">Étape 1 : Utiliser PowerShell pour créer une stratégie de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-253">Step 1: Use PowerShell to create a safe links policy</span></span>

<span data-ttu-id="a40c2-254">Pour créer une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-254">To create a safe links policy, use this syntax:</span></span>

```PowerShell
New-SafeLinksPolicy -Name "<PolicyName>" [-AdminDisplayName "<Comments>"] [-IsEnabled <$true | $false>] [-EnableSafeLinksForTeams <$true | $false>] [-ScanUrls <$true | $false>] [-DeliverMessageAfterScan <$true | $false>] [-EnableForInternalSenders <$true | $false>] [-DoNotAllowClickThrough <$true | $false>] [-DoNotTrackUserClicks <$true | $false>] [-DoNotRewriteUrls "Entry1","Entry2",..."EntryN"]
```

> [!NOTE]
> 
> - <span data-ttu-id="a40c2-255">Pour plus d’informations sur la syntaxe d’entrée à utiliser pour le paramètre _DoNotRewriteUrls,_ voir la [syntaxe d’entrée](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list)pour la liste « Ne pas réécrire les URL suivantes ».</span><span class="sxs-lookup"><span data-stu-id="a40c2-255">For details about the entry syntax to use for the _DoNotRewriteUrls_ parameter, see [Entry syntax for the "Do not rewrite the following URLs" list](safe-links.md#entry-syntax-for-the-do-not-rewrite-the-following-urls-list).</span></span>
> 
> - <span data-ttu-id="a40c2-256">Pour obtenir une syntaxe supplémentaire que vous pouvez utiliser pour le paramètre _DoNotRewriteUrls_ lorsque vous modifiez des stratégies de liens sécurisés existantes à l’aide de la cmdlet **Set-SafeLinksPolicy,** consultez la section Utiliser [PowerShell](#use-powershell-to-modify-safe-links-policies) pour modifier les stratégies de liens sécurisés plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a40c2-256">For additional syntax that you can use for the _DoNotRewriteUrls_ parameter when you modify existing safe links policies by using the **Set-SafeLinksPolicy** cmdlet, see the [Use PowerShell to modify safe links policies](#use-powershell-to-modify-safe-links-policies) section later in this article.</span></span>

<span data-ttu-id="a40c2-257">Cet exemple crée une stratégie de liens sécurisés nommée Contoso All avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="a40c2-257">This example creates a safe links policy named Contoso All with the following values:</span></span>

- <span data-ttu-id="a40c2-258">Activer l’analyse et la réécriture d’URL dans les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="a40c2-258">Turn on URL scanning and rewriting in email messages.</span></span>
- <span data-ttu-id="a40c2-259">Activer l’analyse des URL dans Teams (aperçu tap uniquement).</span><span class="sxs-lookup"><span data-stu-id="a40c2-259">Turn on URL scanning in Teams (TAP Preview only).</span></span>
- <span data-ttu-id="a40c2-260">Activer l’analyse en temps réel des URL sur lesquelles vous avez cliqué, y compris les liens qui pointent vers des fichiers.</span><span class="sxs-lookup"><span data-stu-id="a40c2-260">Turn on real-time scanning of clicked URLs, including clicked links that point to files.</span></span>
- <span data-ttu-id="a40c2-261">Attendez la fin de l’analyse de l’URL avant de remettre le message.</span><span class="sxs-lookup"><span data-stu-id="a40c2-261">Wait for URL scanning to complete before delivering the message.</span></span>
- <span data-ttu-id="a40c2-262">Activer l’analyse et la réécriture d’URL pour les messages internes.</span><span class="sxs-lookup"><span data-stu-id="a40c2-262">Turn on URL scanning and rewriting for internal messages.</span></span>
- <span data-ttu-id="a40c2-263">Suivez les clics des utilisateurs liés à la protection contre les liens sécurisés (nous n’utilisons pas le paramètre _DoNotTrackUserClicks_ et la valeur par défaut est $false, ce qui signifie que les clics utilisateur sont suivis).</span><span class="sxs-lookup"><span data-stu-id="a40c2-263">Track user clicks related to Safe Links protection (we aren't using the _DoNotTrackUserClicks_ parameter, and the default value is $false, which means user clicks are tracked).</span></span>
- <span data-ttu-id="a40c2-264">N’autorisez pas les utilisateurs à accéder à l’URL d’origine en cliquant.</span><span class="sxs-lookup"><span data-stu-id="a40c2-264">Do not allow users to click through to the original URL.</span></span>

```PowerShell
New-SafeLinksPolicy -Name "Contoso All" -IsEnabled $true -EnableSafeLinksForTeams $true -ScanUrls $true -DeliverMessageAfterScan $true -EnableForInternalSenders $true -DoNotAllowClickThrough $true
```

<span data-ttu-id="a40c2-265">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksPolicy.](/powershell/module/exchange/new-safelinkspolicy)</span><span class="sxs-lookup"><span data-stu-id="a40c2-265">For detailed syntax and parameter information, see [New-SafeLinksPolicy](/powershell/module/exchange/new-safelinkspolicy).</span></span>

#### <a name="step-2-use-powershell-to-create-a-safe-links-rule"></a><span data-ttu-id="a40c2-266">Étape 2 : Utiliser PowerShell pour créer une règle de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-266">Step 2: Use PowerShell to create a safe links rule</span></span>

<span data-ttu-id="a40c2-267">Pour créer une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-267">To create a safe links rule, use this syntax:</span></span>

```PowerShell
New-SafeLinksRule -Name "<RuleName>" -SafeLinksPolicy "<PolicyName>" <Recipient filters> [<Recipient filter exceptions>] [-Comments "<OptionalComments>"] [-Enabled <$true | $false>]
```

<span data-ttu-id="a40c2-268">Cet exemple crée une règle de liens sécurisés nommée Contoso All avec les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a40c2-268">This example creates a safe links rule named Contoso All with the following conditions:</span></span>

- <span data-ttu-id="a40c2-269">La règle est associée à la stratégie de liens sécurisés nommée Contoso All.</span><span class="sxs-lookup"><span data-stu-id="a40c2-269">The rule is associated with the safe links policy named Contoso All.</span></span>
- <span data-ttu-id="a40c2-270">La règle s’applique à tous les destinataires du contoso.com domaine.</span><span class="sxs-lookup"><span data-stu-id="a40c2-270">The rule applies to all recipients in the contoso.com domain.</span></span>
- <span data-ttu-id="a40c2-271">Étant donné que nous n’utilisons pas le _paramètre Priority,_ la priorité par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-271">Because we aren't using the _Priority_ parameter, the default priority is used.</span></span>
- <span data-ttu-id="a40c2-272">La règle est activée (nous n’utilisons pas le paramètre _Enabled_ et la valeur par défaut est `$true` ).</span><span class="sxs-lookup"><span data-stu-id="a40c2-272">The rule is enabled (we aren't using the _Enabled_ parameter, and the default value is `$true`).</span></span>

```powershell
New-SafeLinksRule -Name "Contoso All" -SafeLinksPolicy "Contoso All" -RecipientDomainIs contoso.com
```

<span data-ttu-id="a40c2-273">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [New-SafeLinksRule](/powershell/module/exchange/new-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-273">For detailed syntax and parameter information, see [New-SafeLinksRule](/powershell/module/exchange/new-safelinksrule).</span></span>

### <a name="use-powershell-to-view-safe-links-policies"></a><span data-ttu-id="a40c2-274">Utiliser PowerShell pour afficher les stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-274">Use PowerShell to view safe links policies</span></span>

<span data-ttu-id="a40c2-275">Pour afficher les stratégies de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-275">To view existing safe links policies, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksPolicy [-Identity "<PolicyIdentity>"] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="a40c2-276">Cet exemple renvoie une liste récapitulatif de toutes les stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-276">This example returns a summary list of all safe links policies.</span></span>

```PowerShell
Get-SafeLinksPolicy | Format-Table Name
```

<span data-ttu-id="a40c2-277">Cet exemple renvoie des informations détaillées sur la stratégie de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="a40c2-277">This example returns detailed information for the safe links policy named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksPolicy -Identity "Contoso Executives"
```

<span data-ttu-id="a40c2-278">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksPolicy](/powershell/module/exchange/get-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="a40c2-278">For detailed syntax and parameter information, see [Get-SafeLinksPolicy](/powershell/module/exchange/get-safelinkspolicy).</span></span>

### <a name="use-powershell-to-view-safe-links-rules"></a><span data-ttu-id="a40c2-279">Utiliser PowerShell pour afficher les règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-279">Use PowerShell to view safe links rules</span></span>

<span data-ttu-id="a40c2-280">Pour afficher les règles de liens sécurisés existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-280">To view existing safe links rules, use the following syntax:</span></span>

```PowerShell
Get-SafeLinksRule [-Identity "<RuleIdentity>"] [-State <Enabled | Disabled] [| <Format-Table | Format-List> <Property1,Property2,...>]
```

<span data-ttu-id="a40c2-281">Cet exemple renvoie une liste récapitulatif de toutes les règles de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="a40c2-281">This example returns a summary list of all safe links rules.</span></span>

```PowerShell
Get-SafeLinksRule | Format-Table Name,State
```

<span data-ttu-id="a40c2-282">Pour filtrer la liste par règles activées ou désactivées, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a40c2-282">To filter the list by enabled or disabled rules, run the following commands:</span></span>

```PowerShell
Get-SafeLinksRule -State Disabled
```

```PowerShell
Get-SafeLinksRule -State Enabled
```

<span data-ttu-id="a40c2-283">Cet exemple renvoie des informations détaillées sur la règle de liens sécurisés nommée Contoso Executives.</span><span class="sxs-lookup"><span data-stu-id="a40c2-283">This example returns detailed information for the safe links rule named Contoso Executives.</span></span>

```PowerShell
Get-SafeLinksRule -Identity "Contoso Executives"
```

<span data-ttu-id="a40c2-284">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [voir Get-SafeLinksRule](/powershell/module/exchange/get-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-284">For detailed syntax and parameter information, see [Get-SafeLinksRule](/powershell/module/exchange/get-safelinksrule).</span></span>

### <a name="use-powershell-to-modify-safe-links-policies"></a><span data-ttu-id="a40c2-285">Utiliser PowerShell pour modifier des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-285">Use PowerShell to modify safe links policies</span></span>

<span data-ttu-id="a40c2-286">Vous ne pouvez pas renommer une stratégie de liens sécurisés dans PowerShell (la cmdlet **Set-SafeLinksPolicy** n’a pas _de paramètre_ Name).</span><span class="sxs-lookup"><span data-stu-id="a40c2-286">You can't rename a safe links policy in PowerShell (the **Set-SafeLinksPolicy** cmdlet has no _Name_ parameter).</span></span> <span data-ttu-id="a40c2-287">Lorsque vous renommez une stratégie de liens sécurisés dans le portail Microsoft 365 Defender, vous renommez uniquement la règle de liens _sécurisés._</span><span class="sxs-lookup"><span data-stu-id="a40c2-287">When you rename a Safe Links policy in the Microsoft 365 Defender portal, you're only renaming the safe links _rule_.</span></span>

<span data-ttu-id="a40c2-288">La seule considération supplémentaire pour modifier les stratégies de liens sécurisés dans PowerShell est la syntaxe disponible pour le paramètre _DoNotRewriteUrls_ (la liste « Ne pas réécrire les URL [suivantes](safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)» ) :</span><span class="sxs-lookup"><span data-stu-id="a40c2-288">The only additional consideration for modifying safe links policies in PowerShell is the available syntax for the _DoNotRewriteUrls_ parameter (the ["Do not rewrite the following URLs" list](safe-links.md#do-not-rewrite-the-following-urls-lists-in-safe-links-policies)):</span></span>

- <span data-ttu-id="a40c2-289">Pour ajouter des valeurs qui remplaceront les entrées existantes, utilisez la syntaxe suivante `"Entry1","Entry2,..."EntryN"` :</span><span class="sxs-lookup"><span data-stu-id="a40c2-289">To add values that will replace any existing entries, use the following syntax: `"Entry1","Entry2,..."EntryN"`.</span></span>
- <span data-ttu-id="a40c2-290">Pour ajouter ou supprimer des valeurs sans affecter les autres entrées existantes, utilisez la syntaxe suivante : `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span><span class="sxs-lookup"><span data-stu-id="a40c2-290">To add or remove values without affecting other existing entries, use the following syntax: `@{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}`</span></span>

<span data-ttu-id="a40c2-291">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une stratégie de liens sécurisés, comme décrit à l’étape 1 : Utiliser [PowerShell](#step-1-use-powershell-to-create-a-safe-links-policy) pour créer une section de stratégie de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a40c2-291">Otherwise, the same settings are available when you create a safe links policy as described in the [Step 1: Use PowerShell to create a safe links policy](#step-1-use-powershell-to-create-a-safe-links-policy) section earlier in this article.</span></span>

<span data-ttu-id="a40c2-292">Pour modifier une stratégie de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-292">To modify a safe links policy, use this syntax:</span></span>

```PowerShell
Set-SafeLinksPolicy -Identity "<PolicyName>" <Settings>
```

<span data-ttu-id="a40c2-293">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksPolicy](/powershell/module/exchange/set-safelinkspolicy).</span><span class="sxs-lookup"><span data-stu-id="a40c2-293">For detailed syntax and parameter information, see [Set-SafeLinksPolicy](/powershell/module/exchange/set-safelinkspolicy).</span></span>

### <a name="use-powershell-to-modify-safe-links-rules"></a><span data-ttu-id="a40c2-294">Utiliser PowerShell pour modifier des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-294">Use PowerShell to modify safe links rules</span></span>

<span data-ttu-id="a40c2-295">Le seul paramètre qui n’est pas disponible lorsque vous modifiez une règle de liens sécurisés dans PowerShell est le paramètre _Enabled_ qui vous permet de créer une règle désactivée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-295">The only setting that's not available when you modify a safe links rule in PowerShell is the _Enabled_ parameter that allows you to create a disabled rule.</span></span> <span data-ttu-id="a40c2-296">Pour activer ou désactiver des règles de liens sécurisés existantes, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="a40c2-296">To enable or disable existing safe links rules, see the next section.</span></span>

<span data-ttu-id="a40c2-297">Dans le cas contraire, les mêmes paramètres sont disponibles lorsque vous créez une règle comme décrit à l’étape 2 : Utiliser [PowerShell](#step-2-use-powershell-to-create-a-safe-links-rule) pour créer une section de règle de liens sécurisés plus tôt dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a40c2-297">Otherwise, the same settings are available when you create a rule as described in the [Step 2: Use PowerShell to create a safe links rule](#step-2-use-powershell-to-create-a-safe-links-rule) section earlier in this article.</span></span>

<span data-ttu-id="a40c2-298">Pour modifier une règle de liens sécurisés, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-298">To modify a safe links rule, use this syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" <Settings>
```

<span data-ttu-id="a40c2-299">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-299">For detailed syntax and parameter information, see [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-enable-or-disable-safe-links-rules"></a><span data-ttu-id="a40c2-300">Utiliser PowerShell pour activer ou désactiver des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-300">Use PowerShell to enable or disable safe links rules</span></span>

<span data-ttu-id="a40c2-301">L’activation ou la désactivation d’une règle de liens sécurisés dans PowerShell active ou désactive l’ensemble de la stratégie de liens sécurisés (la règle de liens sécurisés et la stratégie de liens sécurisés affectée).</span><span class="sxs-lookup"><span data-stu-id="a40c2-301">Enabling or disabling a safe links rule in PowerShell enables or disables the whole Safe Links policy (the safe links rule and the assigned safe links policy).</span></span>

<span data-ttu-id="a40c2-302">Pour activer ou désactiver une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-302">To enable or disable a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
<Enable-SafeLinksRule | Disable-SafeLinksRule> -Identity "<RuleName>"
```

<span data-ttu-id="a40c2-303">Cet exemple désactive la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="a40c2-303">This example disables the safe links rule named Marketing Department.</span></span>

```PowerShell
Disable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="a40c2-304">Cet exemple montre comment activer la même règle.</span><span class="sxs-lookup"><span data-stu-id="a40c2-304">This example enables same rule.</span></span>

```PowerShell
Enable-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="a40c2-305">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Enable-SafeLinksRule](/powershell/module/exchange/enable-safelinksrule) et [Disable-SafeLinksRule](/powershell/module/exchange/disable-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-305">For detailed syntax and parameter information, see [Enable-SafeLinksRule](/powershell/module/exchange/enable-safelinksrule) and [Disable-SafeLinksRule](/powershell/module/exchange/disable-safelinksrule).</span></span>

### <a name="use-powershell-to-set-the-priority-of-safe-links-rules"></a><span data-ttu-id="a40c2-306">Utiliser PowerShell pour définir la priorité des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-306">Use PowerShell to set the priority of safe links rules</span></span>

<span data-ttu-id="a40c2-p123">La valeur 0 est la priorité la plus élevée que vous pouvez définir sur une règle. La valeur la plus basse que vous pouvez définir dépend du nombre de règles. Par exemple, si vous avez cinq règles, vous pouvez utiliser les valeurs de priorité 0 à 4. Tout changement de priorité d'une règle existante peut avoir un effet en cascade sur les autres règles. Par exemple, si vous avez cinq règles personnalisées (priorités de 0 à 4) et que vous modifiez la priorité d'une règle sur 2, la règle existante de priorité 2 passe en priorité 3, et la règle de priorité 3 passe en priorité 4.</span><span class="sxs-lookup"><span data-stu-id="a40c2-p123">The highest priority value you can set on a rule is 0. The lowest value you can set depends on the number of rules. For example, if you have five rules, you can use the priority values 0 through 4. Changing the priority of an existing rule can have a cascading effect on other rules. For example, if you have five custom rules (priorities 0 through 4), and you change the priority of a rule to 2, the existing rule with priority 2 is changed to priority 3, and the rule with priority 3 is changed to priority 4.</span></span>

<span data-ttu-id="a40c2-312">Pour définir la priorité d’une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-312">To set the priority of a safe links rule in PowerShell, use the following syntax:</span></span>

```PowerShell
Set-SafeLinksRule -Identity "<RuleName>" -Priority <Number>
```

<span data-ttu-id="a40c2-p124">Cet exemple définit la priorité de la règle nommée Marketing Department sur 2. Toutes les règles existantes dont la priorité est inférieure ou égale à 2 sont diminuées d’une unité (leurs numéros de priorité sont augmentés de 1).</span><span class="sxs-lookup"><span data-stu-id="a40c2-p124">This example sets the priority of the rule named Marketing Department to 2. All existing rules that have a priority less than or equal to 2 are decreased by 1 (their priority numbers are increased by 1).</span></span>

```PowerShell
Set-SafeLinksRule -Identity "Marketing Department" -Priority 2
```

> [!NOTE]
> <span data-ttu-id="a40c2-315">Pour définir la priorité d’une nouvelle règle lorsque vous la créez, utilisez plutôt le paramètre _Priority_ de la cmdlet **New-SafeLinksRule.**</span><span class="sxs-lookup"><span data-stu-id="a40c2-315">To set the priority of a new rule when you create it, use the _Priority_ parameter on the **New-SafeLinksRule** cmdlet instead.</span></span>

<span data-ttu-id="a40c2-316">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-316">For detailed syntax and parameter information, see [Set-SafeLinksRule](/powershell/module/exchange/set-safelinksrule).</span></span>

### <a name="use-powershell-to-remove-safe-links-policies"></a><span data-ttu-id="a40c2-317">Utiliser PowerShell pour supprimer des stratégies de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-317">Use PowerShell to remove safe links policies</span></span>

<span data-ttu-id="a40c2-318">Lorsque vous utilisez PowerShell pour supprimer une stratégie de liens sécurisés, la règle de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-318">When you use PowerShell to remove a safe links policy, the corresponding safe links rule isn't removed.</span></span>

<span data-ttu-id="a40c2-319">Pour supprimer une stratégie de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-319">To remove a safe links policy in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "<PolicyName>"
```

<span data-ttu-id="a40c2-320">Cet exemple supprime la stratégie de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="a40c2-320">This example removes the safe links policy named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksPolicy -Identity "Marketing Department"
```

<span data-ttu-id="a40c2-321">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksPolicy.](/powershell/module/exchange/remove-safelinkspolicy)</span><span class="sxs-lookup"><span data-stu-id="a40c2-321">For detailed syntax and parameter information, see [Remove-SafeLinksPolicy](/powershell/module/exchange/remove-safelinkspolicy).</span></span>

### <a name="use-powershell-to-remove-safe-links-rules"></a><span data-ttu-id="a40c2-322">Utiliser PowerShell pour supprimer des règles de liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="a40c2-322">Use PowerShell to remove safe links rules</span></span>

<span data-ttu-id="a40c2-323">Lorsque vous utilisez PowerShell pour supprimer une règle de liens sécurisés, la stratégie de liens sécurisés correspondante n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="a40c2-323">When you use PowerShell to remove a safe links rule, the corresponding safe links policy isn't removed.</span></span>

<span data-ttu-id="a40c2-324">Pour supprimer une règle de liens sécurisés dans PowerShell, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="a40c2-324">To remove a safe links rule in PowerShell, use this syntax:</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "<PolicyName>"
```

<span data-ttu-id="a40c2-325">Cet exemple supprime la règle de liens sécurisés nommée Marketing Department.</span><span class="sxs-lookup"><span data-stu-id="a40c2-325">This example removes the safe links rule named Marketing Department.</span></span>

```PowerShell
Remove-SafeLinksRule -Identity "Marketing Department"
```

<span data-ttu-id="a40c2-326">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-SafeLinksRule](/powershell/module/exchange/remove-safelinksrule).</span><span class="sxs-lookup"><span data-stu-id="a40c2-326">For detailed syntax and parameter information, see [Remove-SafeLinksRule](/powershell/module/exchange/remove-safelinksrule).</span></span>

<span data-ttu-id="a40c2-327">Pour vérifier que la sécurité est en cours d’analyse des messages, vérifiez que Microsoft Defender est disponible Office 365 rapports.</span><span class="sxs-lookup"><span data-stu-id="a40c2-327">To verify that Safe Links is scanning messages, check the available Microsoft Defender for Office 365 reports.</span></span> <span data-ttu-id="a40c2-328">Pour plus d’informations, voir Afficher les [rapports de Defender pour Office 365](view-reports-for-mdo.md) et Utiliser l’Explorateur dans le portail Microsoft 365 [Defender.](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="a40c2-328">For more information, see [View reports for Defender for Office 365](view-reports-for-mdo.md) and [Use Explorer in the Microsoft 365 Defender portal](threat-explorer.md).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="a40c2-329">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="a40c2-329">How do you know these procedures worked?</span></span>

<span data-ttu-id="a40c2-330">Pour vérifier que vous avez correctement créé, modifié ou supprimé des stratégies de liens sécurisés, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a40c2-330">To verify that you've successfully created, modified, or removed Safe Links policies, do any of the following steps:</span></span>

- <span data-ttu-id="a40c2-331">Dans le portail Microsoft 365 Defender, go to **Policies &** \> **Threat policies** Safe \> **Links**.</span><span class="sxs-lookup"><span data-stu-id="a40c2-331">In the Microsoft 365 Defender portal, go to **Policies & rules** \> **Threat policies** \> **Safe Links**.</span></span> <span data-ttu-id="a40c2-332">Vérifiez la liste des stratégies, leurs **valeurs d’état** et leurs **valeurs de** priorité.</span><span class="sxs-lookup"><span data-stu-id="a40c2-332">Verify the list of policies, their **Status** values, and their **Priority** values.</span></span> <span data-ttu-id="a40c2-333">Pour afficher plus de détails, sélectionnez la stratégie dans la liste et affichez les détails dans le volant.</span><span class="sxs-lookup"><span data-stu-id="a40c2-333">To view more details, select the policy from the list, and view the details in the fly out.</span></span>

- <span data-ttu-id="a40c2-334">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, remplacez par le nom de la stratégie ou de la règle, exécutez la commande suivante et vérifiez les \<Name\> paramètres :</span><span class="sxs-lookup"><span data-stu-id="a40c2-334">In Exchange Online PowerShell or Exchange Online Protection PowerShell, replace \<Name\> with the name of the policy or rule, run the following command, and verify the settings:</span></span>

  ```PowerShell
  Get-SafeLinksPolicy -Identity "<Name>"
  ```

  ```PowerShell
  Get-SafeLinksRule -Identity "<Name>"
  ```