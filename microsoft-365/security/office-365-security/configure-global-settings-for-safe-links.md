---
title: Configurer les paramètres globaux pour les paramètres de liens sécurisés dans Defender pour Office 365
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
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir comment afficher et configurer les paramètres globaux (la liste « Bloquer les URL suivantes » et la protection pour les applications Office 365) pour les liens sécurisés dans Microsoft Defender pour Office 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 11544953bf348c47e697b3210da709cccdb31a7e
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245839"
---
# <a name="configure-global-settings-for-safe-links-in-microsoft-defender-for-office-365"></a><span data-ttu-id="bd688-103">Configurer les paramètres globaux pour la stratégie de liens sécurisés dans Microsoft Defender Office 365</span><span class="sxs-lookup"><span data-stu-id="bd688-103">Configure global settings for Safe Links in Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="bd688-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bd688-104">**Applies to**</span></span>
- [<span data-ttu-id="bd688-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="bd688-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="bd688-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd688-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!IMPORTANT]
> <span data-ttu-id="bd688-107">Cet article est destiné aux entreprises qui ont [Microsoft Defender pour Office 365](defender-for-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="bd688-107">This article is intended for business customers who have [Microsoft Defender for Office 365](defender-for-office-365.md).</span></span> <span data-ttu-id="bd688-108">Si vous êtes un utilisateur d’accueil à la recherche d’informations sur les liens sécurisés dans Outlook, voir [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="bd688-108">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="bd688-109">La fonctionnalité Liens sécurisés de [Microsoft Defender](defender-for-office-365.md) pour Office 365 permet d’analyser les URL des messages électroniques entrants dans le flux de messagerie et de vérifier en un clic les URL et les liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="bd688-109">Safe Links is a feature in [Microsoft Defender for Office 365](defender-for-office-365.md) that provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="bd688-110">Pour plus d’informations, [voir Liens sécurisés dans Microsoft Defender pour Office 365](safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="bd688-110">For more information, see [Safe Links in Microsoft Defender for Office 365](safe-links.md).</span></span>

<span data-ttu-id="bd688-111">Vous configurez la plupart des paramètres de liens sécurisés dans les stratégies de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="bd688-111">You configure most Safe Links settings in Safe Links policies.</span></span> <span data-ttu-id="bd688-112">Pour obtenir des instructions, voir [Configurer des stratégies de liens](set-up-safe-links-policies.md)sécurisés dans Microsoft Defender Office 365 .</span><span class="sxs-lookup"><span data-stu-id="bd688-112">For instructions, see [Set up Safe Links policies in Microsoft Defender for Office 365](set-up-safe-links-policies.md).</span></span>

<span data-ttu-id="bd688-113">Toutefois, la stratégie de liens sécurisés utilise également les paramètres globaux suivants que vous configurez en dehors des stratégies de liens sécurisés elles-mêmes :</span><span class="sxs-lookup"><span data-stu-id="bd688-113">But, Safe Links also uses the following global settings that you configure outside of the Safe Links policies themselves:</span></span>

- <span data-ttu-id="bd688-114">La **liste Bloquer les URL suivantes.**</span><span class="sxs-lookup"><span data-stu-id="bd688-114">The **Block the following URLs** list.</span></span> <span data-ttu-id="bd688-115">Ce paramètre s’applique à tous les utilisateurs inclus dans les stratégies de liens sécurisés actives.</span><span class="sxs-lookup"><span data-stu-id="bd688-115">This setting applies to all users who are included in any active Safe Links policies.</span></span> <span data-ttu-id="bd688-116">Pour plus d’informations, consultez la liste [« Bloquer les URL suivantes](safe-links.md#block-the-following-urls-list-for-safe-links) » pour les liens sécurisés</span><span class="sxs-lookup"><span data-stu-id="bd688-116">For more information, see ["Block the following URLs" list for Safe Links](safe-links.md#block-the-following-urls-list-for-safe-links)</span></span>
- <span data-ttu-id="bd688-117">Protection des liens sécurisés pour Office 365 applications.</span><span class="sxs-lookup"><span data-stu-id="bd688-117">Safe Links protection for Office 365 apps.</span></span> <span data-ttu-id="bd688-118">Ces paramètres s’appliquent à tous les utilisateurs de l’organisation titulaires d’une licence Defender pour Office 365, que les utilisateurs soient inclus ou non dans les stratégies de liens sécurisés actives.</span><span class="sxs-lookup"><span data-stu-id="bd688-118">These settings apply to all users in the organization who are licensed for Defender for Office 365, regardless of whether the users are included in active Safe Links policies or not.</span></span> <span data-ttu-id="bd688-119">Pour plus d’informations, voir paramètres de liens [sécurisés pour Office 365 applications.](safe-links.md#safe-links-settings-for-office-365-apps)</span><span class="sxs-lookup"><span data-stu-id="bd688-119">For more information, see [Safe Links settings for Office 365 apps](safe-links.md#safe-links-settings-for-office-365-apps).</span></span>

<span data-ttu-id="bd688-120">Vous pouvez configurer les paramètres globaux de liens sécurisés dans le Centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres en Exchange Online ; EOP PowerShell autonome pour les organisations sans boîtes aux lettres Exchange Online, mais avec Microsoft Defender pour les abonnements de modules supplémentaires Office 365).</span><span class="sxs-lookup"><span data-stu-id="bd688-120">You can configure the global Safe Links settings in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Microsoft Defender for Office 365 add-on subscriptions).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="bd688-121">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="bd688-121">What do you need to know before you begin?</span></span>

- <span data-ttu-id="bd688-122">Il n’existe aucune stratégie de liens sécurisés intégrée ou par défaut. Vous devez donc créer au moins une stratégie de liens sécurisés pour que la liste Bloquer les URL **suivantes** soit active.</span><span class="sxs-lookup"><span data-stu-id="bd688-122">There is no built-in or default Safe Links policy, so you need to create at least one Safe Links policy in order for the **Block the following URLs** list to be active.</span></span> <span data-ttu-id="bd688-123">Pour obtenir des instructions, voir [Configurer des stratégies de liens](set-up-safe-links-policies.md)sécurisés dans Microsoft Defender Office 365 .</span><span class="sxs-lookup"><span data-stu-id="bd688-123">For instructions, see [Set up Safe Links policies in Microsoft Defender for Office 365](set-up-safe-links-policies.md).</span></span>

- <span data-ttu-id="bd688-124">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="bd688-124">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="bd688-125">Pour aller directement à la page **Liens sécurisés,** utilisez <https://protection.office.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="bd688-125">To go directly to the **Safe Links** page, use <https://protection.office.com/safelinksv2>.</span></span>

- <span data-ttu-id="bd688-126">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="bd688-126">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="bd688-127">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="bd688-127">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="bd688-128">Des autorisations doivent vous avoir été attribuées dans **Exchange Online** pour que vous puissiez effectuer les procédures décrites dans cet article :</span><span class="sxs-lookup"><span data-stu-id="bd688-128">You need to be assigned permissions in **Exchange Online** before you can do the procedures in this article:</span></span>
  - <span data-ttu-id="bd688-129">Pour configurer les paramètres globaux des liens sécurisés,  vous devez être membre des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd688-129">To configure the global settings for Safe Links, you need to be a member of the **Organization Management** or **Security Administrator** role groups.</span></span>
  - <span data-ttu-id="bd688-130">Pour accéder en lecture seule aux paramètres globaux des liens  sécurisés,  vous devez être membre des groupes de rôles Lecteur global ou Lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bd688-130">For read-only access to the global settings for Safe Links, you need to be a member of the **Global Reader** or **Security Reader** role groups.</span></span>

  <span data-ttu-id="bd688-131">Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).</span><span class="sxs-lookup"><span data-stu-id="bd688-131">For more information, see [Permissions in Exchange Online](/exchange/permissions-exo/permissions-exo).</span></span>

  <span data-ttu-id="bd688-132">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="bd688-132">**Notes**:</span></span>

  - <span data-ttu-id="bd688-133">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bd688-133">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="bd688-134">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bd688-134">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>
  - <span data-ttu-id="bd688-135">Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bd688-135">The **View-Only Organization Management** role group in [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) also gives read-only access to the feature.</span></span>

- <span data-ttu-id="bd688-136">Pour obtenir les valeurs recommandées pour les paramètres globaux de liens sécurisés, consultez les [paramètres de liens sécurisés.](recommended-settings-for-eop-and-office365.md#safe-links-settings)</span><span class="sxs-lookup"><span data-stu-id="bd688-136">For our recommended values for the global settings for Safe Links, see [Safe Links settings](recommended-settings-for-eop-and-office365.md#safe-links-settings).</span></span>

- <span data-ttu-id="bd688-137">Autorisez jusqu’à 30 minutes pour qu’une stratégie nouvelle ou mise à jour soit appliquée.</span><span class="sxs-lookup"><span data-stu-id="bd688-137">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="bd688-138">[De nouvelles fonctionnalités sont continuellement ajoutées à Microsoft Defender pour Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span><span class="sxs-lookup"><span data-stu-id="bd688-138">[New features are continually being added to Microsoft Defender for Office 365](defender-for-office-365.md#new-features-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="bd688-139">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements à vos stratégies de liens sécurisés existantes.</span><span class="sxs-lookup"><span data-stu-id="bd688-139">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="configure-the-block-the-following-urls-list-in-the-security--compliance-center"></a><span data-ttu-id="bd688-140">Configurer la liste « Bloquer les URL suivantes » dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="bd688-140">Configure the "Block the following URLs" list in the Security & Compliance Center</span></span>

<span data-ttu-id="bd688-141">La **liste Bloquer les URL suivantes** identifie les liens qui doivent toujours être bloqués par l’analyse des liens sécurisés dans les applications pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd688-141">The **Block the following URLs** list identifies the links that should always be blocked by Safe Links scanning in supported apps.</span></span> <span data-ttu-id="bd688-142">Pour plus d’informations, consultez la liste « Bloquer les URL suivantes » [pour les liens sécurisés.](safe-links.md#block-the-following-urls-list-for-safe-links)</span><span class="sxs-lookup"><span data-stu-id="bd688-142">For more information, see ["Block the following URLs" list for Safe Links](safe-links.md#block-the-following-urls-list-for-safe-links).</span></span>

1. <span data-ttu-id="bd688-143">Dans le Centre de sécurité &  conformité, cliquez sur Stratégie de gestion des menaces - Liens \>  \> sécurisés **ATP,** puis cliquez sur **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="bd688-143">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="bd688-144">Dans la **stratégie de liens sécurisés de votre** organisation qui s’affiche, allez dans la zone Bloquer les URL **suivantes.**</span><span class="sxs-lookup"><span data-stu-id="bd688-144">In the **Safe Links policy for your organization** fly out that appears, go to the **Block the following URLs** box.</span></span>

3. <span data-ttu-id="bd688-145">Configurez une ou plusieurs entrées comme décrit dans la syntaxe d’entrée pour la liste [« Bloquer les URL suivantes](safe-links.md#entry-syntax-for-the-block-the-following-urls-list)».</span><span class="sxs-lookup"><span data-stu-id="bd688-145">Configure one or more entries as described in [Entry syntax for the "Block the following URLs" list](safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span></span>

   <span data-ttu-id="bd688-146">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bd688-146">When you're finished, click **Save**.</span></span>

### <a name="configure-the-block-the-following-urls-list-in-powershell"></a><span data-ttu-id="bd688-147">Configurer la liste « Bloquer les URL suivantes » dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd688-147">Configure the "Block the following URLs" list in PowerShell</span></span>

<span data-ttu-id="bd688-148">Pour plus d’informations sur la syntaxe d’entrée, voir la syntaxe d’entrée pour la liste [« Bloquer les URL suivantes](safe-links.md#entry-syntax-for-the-block-the-following-urls-list)».</span><span class="sxs-lookup"><span data-stu-id="bd688-148">For details about the entry syntax, see [Entry syntax for the "Block the following URLs" list](safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span></span>

<span data-ttu-id="bd688-149">Vous pouvez utiliser la cmdlet **Get-AtpPolicyForO365** pour afficher les entrées existantes dans la _propriété BlockURLs._</span><span class="sxs-lookup"><span data-stu-id="bd688-149">You can use the **Get-AtpPolicyForO365** cmdlet to view existing entries in the _BlockURLs_ property.</span></span>

- <span data-ttu-id="bd688-150">Pour ajouter des valeurs qui remplaceront les entrées existantes, utilisez la syntaxe suivante dans Exchange Online PowerShell ou Exchange Online Protection PowerShell :</span><span class="sxs-lookup"><span data-stu-id="bd688-150">To add values that will replace any existing entries, use the following syntax in Exchange Online PowerShell or Exchange Online Protection PowerShell:</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls "Entry1","Entry2",..."EntryN"
  ```

  <span data-ttu-id="bd688-151">Cet exemple ajoute les entrées suivantes à la liste :</span><span class="sxs-lookup"><span data-stu-id="bd688-151">This example adds the following entries to the list:</span></span>

  - <span data-ttu-id="bd688-152">Bloquez le domaine, les sous-domaines et les chemins d’accès fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="bd688-152">Block the domain, subdomains, and paths for fabrikam.com.</span></span>
  - <span data-ttu-id="bd688-153">Bloquer la recherche de sous-domaine, mais pas le domaine parent ou d’autres sous-domaines dans tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="bd688-153">Block the subdomain research, but not the parent domain or other subdomains in tailspintoys.com</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls "fabrikam.com","https://research.tailspintoys.com*"
  ```

- <span data-ttu-id="bd688-154">Pour ajouter ou supprimer des valeurs sans affecter les autres entrées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="bd688-154">To add or remove values without affecting other existing entries, use the following syntax:</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls @{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}
  ```

  <span data-ttu-id="bd688-155">Cet exemple ajoute une nouvelle entrée pour adatum.com et supprime l’entrée pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="bd688-155">This example adds a new entry for adatum.com, and removes the entry for fabrikam.com.</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls @{Add="adatum.com"; Remove="fabrikam"}
  ```

## <a name="configure-safe-links-protection-for-office-365-apps-in-the-security--compliance-center"></a><span data-ttu-id="bd688-156">Configurer la protection des liens sécurisés pour Office 365 applications dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="bd688-156">Configure Safe Links protection for Office 365 apps in the Security & Compliance Center</span></span>

<span data-ttu-id="bd688-157">La protection des liens sécurisés Office 365 applications s’applique aux documents dans les applications Office bureau, mobiles et web pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd688-157">Safe Links protection for Office 365 apps applies to documents in supported Office desktop, mobile, and web apps.</span></span> <span data-ttu-id="bd688-158">Pour plus d’informations, voir paramètres de liens [sécurisés pour Office 365 applications.](safe-links.md#safe-links-settings-for-office-365-apps)</span><span class="sxs-lookup"><span data-stu-id="bd688-158">For more information, see [Safe Links settings for Office 365 apps](safe-links.md#safe-links-settings-for-office-365-apps).</span></span>

1. <span data-ttu-id="bd688-159">Dans le Centre de sécurité &  conformité, cliquez sur Stratégie de gestion des menaces - Liens \>  \> sécurisés **ATP,** puis cliquez sur **Paramètres globaux.**</span><span class="sxs-lookup"><span data-stu-id="bd688-159">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="bd688-160">Dans la stratégie **de** liens sécurisés de votre organisation qui s’affiche, configurez les paramètres suivants dans la Paramètres qui s’appliquent au contenu à l’exception de la section **courrier** électronique :</span><span class="sxs-lookup"><span data-stu-id="bd688-160">In the **Safe Links policy for your organization** fly out that appears, configure the following settings in the **Settings that apply to content except email** section:</span></span>

   - <span data-ttu-id="bd688-161">**Office 365 applications**: vérifiez que le basculement se trouve à droite pour activer les liens sécurisés pour les applications Office 365 pris en charge : ![ activer/ ](../../media/scc-toggle-on.png) activer.</span><span class="sxs-lookup"><span data-stu-id="bd688-161">**Office 365 applications**: Verify the toggle is to the right to enable Safe Links for supported Office 365 apps: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   - <span data-ttu-id="bd688-162">**Ne suivez** pas le moment où les utilisateurs cliquent sur Liens sécurisés : déplacez le bouton bascule vers la gauche pour suivre les clics des utilisateurs liés aux URL bloquées dans les applications Office 365 pris en charge : ![ basculez vers la ](../../media/scc-toggle-off.png) gauche.</span><span class="sxs-lookup"><span data-stu-id="bd688-162">**Do not track when users click Safe Links**: Move the toggle to the left to track user clicks related to blocked URLs in supported Office 365 apps: ![Toggle off](../../media/scc-toggle-off.png).</span></span>

   - <span data-ttu-id="bd688-163">Ne laissez pas les utilisateurs cliquer sur liens sécurisés vers **l’URL** d’origine : vérifiez que le bouton bascule est à droite pour empêcher les utilisateurs de cliquer sur l’URL bloquée d’origine dans les applications Office 365 pris en charge : basculez sur ![ ](../../media/scc-toggle-on.png) .</span><span class="sxs-lookup"><span data-stu-id="bd688-163">**Do not let users click through Safe Links to the original URL**: Verify the toggle is to the right to prevent users from clicking through to the original blocked URL in supported Office 365 apps: ![Toggle on](../../media/scc-toggle-on.png).</span></span>

   <span data-ttu-id="bd688-164">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="bd688-164">When you're finished, click **Save**.</span></span>

### <a name="configure-safe-links-protection-for-office-365-apps-in-powershell"></a><span data-ttu-id="bd688-165">Configurer la protection des liens sécurisés pour Office 365 applications dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd688-165">Configure Safe Links protection for Office 365 apps in PowerShell</span></span>

<span data-ttu-id="bd688-166">Si vous préférez utiliser PowerShell pour configurer la protection des liens sécurisés pour les applications Office 365, utilisez la syntaxe suivante dans Exchange Online PowerShell ou Exchange Online Protection PowerShell :</span><span class="sxs-lookup"><span data-stu-id="bd688-166">If you'd rather use PowerShell to configure Safe Links protection for Office 365 apps, use the following syntax in Exchange Online PowerShell or Exchange Online Protection PowerShell:</span></span>

```powershell
Set-AtpPolicyForO365 [-EnableSafeLinksForO365Clients <$true | $false> [-AllowClickThrough <$true | $false>] [-TrackClicks <$true | $false>]
```

<span data-ttu-id="bd688-167">Cet exemple configure les paramètres suivants pour la protection des liens sécurisés dans Office 365 applications :</span><span class="sxs-lookup"><span data-stu-id="bd688-167">This example configures the following settings for Safe Links protection in Office 365 apps:</span></span>

- <span data-ttu-id="bd688-168">La fonction Liens sécurisés pour Office 365 applications est activée (nous n’utilisons pas le paramètre _EnableSafeLinksForO365Clients_ et la valeur par défaut est $true).</span><span class="sxs-lookup"><span data-stu-id="bd688-168">Safe Links for Office 365 apps is turned on (we aren't using the _EnableSafeLinksForO365Clients_ parameter, and the default value is $true).</span></span>
- <span data-ttu-id="bd688-169">L’utilisateur clique sur les URL bloquées dans les Office 365 les applications sont suivis.</span><span class="sxs-lookup"><span data-stu-id="bd688-169">User clicks related to blocked URLs in supported Office 365 apps are tracked.</span></span>
- <span data-ttu-id="bd688-170">Les utilisateurs ne sont pas autorisés à accéder à l’URL bloquée d’origine dans les applications Office 365 pris en charge (nous n’utilisons pas le paramètre _AllowClickThrough_ et la valeur par défaut est $false).</span><span class="sxs-lookup"><span data-stu-id="bd688-170">Users are not allowed to click through to the original blocked URL in supported Office 365 apps (we aren't using the _AllowClickThrough_ parameter, and the default value is $false).</span></span>

```powershell
Set-AtpPolicyForO365 -TrackClicks $true
```

<span data-ttu-id="bd688-171">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="bd688-171">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="bd688-172">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="bd688-172">How do you know these procedures worked?</span></span>

<span data-ttu-id="bd688-173">Pour vérifier que vous avez correctement configuré les paramètres globaux des liens sécurisés (la liste Bloquer les URL suivantes et les **paramètres** de protection des applications Office 365), vous devez suivre l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd688-173">To verify that you've successfully configured the global settings for Safe Links (the **Block the following URLs** list and the Office 365 app protection settings), do any of the following steps:</span></span>

- <span data-ttu-id="bd688-174">Dans le Centre de sécurité &  conformité, rendez-vous sur Liens sécurisés de la stratégie de gestion des menaces - Protection contre les menaces, cliquez sur Paramètres globaux et vérifiez les paramètres dans le volant qui \>  \> s’affiche. </span><span class="sxs-lookup"><span data-stu-id="bd688-174">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, click **Global settings**, and verify the settings in the fly out that appears.</span></span>

- <span data-ttu-id="bd688-175">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="bd688-175">In Exchange Online PowerShell or Exchange Online Protection PowerShell, run the following command and verify the settings:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List BlockUrls,EnableSafeLinksForO365Clients,AllowClickThrough,TrackClicks
  ```

  <span data-ttu-id="bd688-176">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="bd688-176">For detailed syntax and parameter information, see [Get-AtpPolicyForO365](/powershell/module/exchange/get-atppolicyforo365).</span></span>
