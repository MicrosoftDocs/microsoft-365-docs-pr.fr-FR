---
title: Configurer les paramètres globaux pour les paramètres de liens fiables dans Office 365 DAV
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: article
ms.date: ''
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à afficher et à configurer les paramètres globaux (la liste des URL « bloquer les URL suivantes » et la protection pour les applications Office 365) pour les liens fiables dans Office 365 Advanced Threat Protection (ATP).
ms.openlocfilehash: 6ca18bfb555419a8f4a61b55715f328ed7da5e88
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48328532"
---
# <a name="configure-global-settings-for-safe-links-in-office-365-atp"></a><span data-ttu-id="6f9f5-103">Configurer les paramètres globaux pour les liens fiables dans Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="6f9f5-103">Configure global settings for Safe Links in Office 365 ATP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!IMPORTANT]
> <span data-ttu-id="6f9f5-104">Cet article est destiné aux entreprises qui ont [Office 365 – Protection avancée contre les menaces](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-104">This article is intended for business customers who have [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="6f9f5-105">Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur Safelinks dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-105">If you are a home user looking for information about Safelinks in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="6f9f5-106">La fonctionnalité liens fiables est une fonctionnalité de la [protection avancée contre les menaces (ATP) d’Office 365](office-365-atp.md) qui permet d’analyser les messages électroniques entrants dans le flux de messagerie et de cliquer sur vérification des URL et des liens dans les messages électroniques et à d’autres emplacements.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-106">Safe Links is a feature in [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md) that provides URL scanning of inbound email messages in mail flow, and time of click verification of URLs and links in email messages and in other locations.</span></span> <span data-ttu-id="6f9f5-107">Pour plus d’informations, consultez la rubrique [liens approuvés dans Office 365 ATP](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-107">For more information, see [Safe Links in Office 365 ATP](atp-safe-links.md).</span></span>

<span data-ttu-id="6f9f5-108">Vous configurez la plupart des paramètres de liens fiables dans stratégies de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-108">You configure most Safe Links settings in Safe Links policies.</span></span> <span data-ttu-id="6f9f5-109">Pour obtenir des instructions, consultez la rubrique relative [à la configuration des stratégies de liens fiables dans Office 365 DAV](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-109">For instructions, see [Set up Safe Links policies in Office 365 ATP](set-up-atp-safe-links-policies.md).</span></span>

<span data-ttu-id="6f9f5-110">Toutefois, les liens fiables utilisent également des paramètres globaux qui s’appliquent à tous les utilisateurs inclus dans les stratégies de liens fiables actives.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-110">But, Safe Links also uses global settings that apply to all users who are included in any active Safe Links policies.</span></span> <span data-ttu-id="6f9f5-111">Ces paramètres globaux :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-111">These global settings area:</span></span>

- <span data-ttu-id="6f9f5-112">La liste **bloquer les URL suivantes** .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-112">The **Block the following URLs** list.</span></span> <span data-ttu-id="6f9f5-113">Pour plus d’informations, reportez-vous à [la liste « bloquer les URL suivantes » pour les liens fiables](atp-safe-links.md#block-the-following-urls-list-for-safe-links)</span><span class="sxs-lookup"><span data-stu-id="6f9f5-113">For more information, see ["Block the following URLs" list for Safe Links](atp-safe-links.md#block-the-following-urls-list-for-safe-links)</span></span>
- <span data-ttu-id="6f9f5-114">Protection des liens fiables pour les applications Office 365.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-114">Safe Links protection for Office 365 apps.</span></span> <span data-ttu-id="6f9f5-115">Pour plus d’informations, consultez la rubrique [paramètres de liens approuvés pour les applications Office 365](atp-safe-links.md#safe-links-settings-for-office-365-apps).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-115">For more information, see [Safe Links settings for Office 365 apps](atp-safe-links.md#safe-links-settings-for-office-365-apps).</span></span>

<span data-ttu-id="6f9f5-116">Vous pouvez configurer les paramètres de liens de sécurité globaux dans le centre de sécurité & conformité ou dans PowerShell (Exchange Online PowerShell pour les organisations Microsoft 365 éligibles avec des boîtes aux lettres dans Exchange Online ; environnement de ligne de commande Exchange autonome EOP pour les organisations sans boîtes aux lettres Exchange Online, mais avec les abonnements complémentaires Office 365 ATP).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-116">You can configure the global Safe Links settings in the Security & Compliance Center or in PowerShell (Exchange Online PowerShell for eligible Microsoft 365 organizations with mailboxes in Exchange Online; standalone EOP PowerShell for organizations without Exchange Online mailboxes, but with Office 365 ATP add-on subscriptions).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="6f9f5-117">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6f9f5-117">What do you need to know before you begin?</span></span>

- <span data-ttu-id="6f9f5-118">Les fonctionnalités fournies par les paramètres globaux pour les liens fiables s’appliquent uniquement aux utilisateurs qui sont inclus dans les stratégies de liens fiables actifs.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-118">The features provided by global settings for Safe Links are only applied to users who are included in active Safe Links policies.</span></span> <span data-ttu-id="6f9f5-119">Il n’existe pas de stratégie de liens de sécurité intégrée ou par défaut, vous devez donc créer au moins une stratégie de liens fiables pour que ces paramètres globaux soient actifs.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-119">There is no built-in or default Safe Links policy, so you need to create at least one Safe Links policy in order for these global settings to be active.</span></span> <span data-ttu-id="6f9f5-120">Pour obtenir des instructions, consultez la rubrique relative [à la configuration des stratégies de liens fiables dans Office 365 DAV](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-120">For instructions, see [Set up Safe Links policies in Office 365 ATP](set-up-atp-safe-links-policies.md).</span></span>

- <span data-ttu-id="6f9f5-121">Vous ouvrez le Centre de conformité et sécurité sur <https://protection.office.com/>.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-121">You open the Security & Compliance Center at <https://protection.office.com/>.</span></span> <span data-ttu-id="6f9f5-122">Pour accéder directement à la page **liens approuvés ATP** , utilisez <https://protection.office.com/safelinksv2> .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-122">To go directly to the **ATP Safe Links** page, use <https://protection.office.com/safelinksv2>.</span></span>

- <span data-ttu-id="6f9f5-123">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-123">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="6f9f5-124">Pour vous connecter à un service Exchange Online Protection PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-124">To connect to standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="6f9f5-125">Pour afficher et configurer les paramètres globaux pour les liens fiables, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-125">To view and configure the global settings for Safe Links, you need to be a member of one of the following role groups:</span></span>

  - <span data-ttu-id="6f9f5-126">**Gestion de l’organisation** ou **Administrateur de sécurité** dans le [Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-126">**Organization Management** or **Security Administrator** in the [Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  - <span data-ttu-id="6f9f5-127">**Gestion** de l’organisation dans [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-127">**Organization Management** in [Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo#role-groups).</span></span>

- <span data-ttu-id="6f9f5-128">Pour connaître les valeurs recommandées pour les paramètres globaux des liens fiables, consultez la rubrique [Safe Links Settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-settings).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-128">For our recommended values for the global settings for Safe Links, see [Safe Links settings](recommended-settings-for-eop-and-office365-atp.md#safe-links-settings).</span></span>

- <span data-ttu-id="6f9f5-129">Autoriser jusqu’à 30 minutes pour l’application d’une stratégie nouvelle ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-129">Allow up to 30 minutes for a new or updated policy to be applied.</span></span>

- <span data-ttu-id="6f9f5-130">De [nouvelles fonctionnalités sont continuellement ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-130">[New features are continually being added to ATP](office-365-atp.md#new-features-in-office-365-atp).</span></span> <span data-ttu-id="6f9f5-131">À mesure que de nouvelles fonctionnalités sont ajoutées, vous devrez peut-être apporter des ajustements aux stratégies de liens fiables existantes.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-131">As new features are added, you may need to make adjustments to your existing Safe Links policies.</span></span>

## <a name="configure-the-block-the-following-urls-list-in-the-security--compliance-center"></a><span data-ttu-id="6f9f5-132">Configurer la liste « bloquer les URL suivantes » dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="6f9f5-132">Configure the "Block the following URLs" list in the Security & Compliance Center</span></span>

<span data-ttu-id="6f9f5-133">La liste **bloquer les URL suivantes** identifie les liens qui doivent toujours être bloqués par l’analyse des liens fiables dans les applications prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-133">The **Block the following URLs** list identifies the links that should always be blocked by Safe Links scanning in supported apps.</span></span> <span data-ttu-id="6f9f5-134">Pour plus d’informations, reportez-vous à [la section « bloquer les URL suivantes » pour les liens fiables](atp-safe-links.md#block-the-following-urls-list-for-safe-links).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-134">For more information, see ["Block the following URLs" list for Safe Links](atp-safe-links.md#block-the-following-urls-list-for-safe-links).</span></span>

1. <span data-ttu-id="6f9f5-135">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \> **Policy** \> **liens approuvés ATP**, puis cliquez sur **paramètres globaux**.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-135">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="6f9f5-136">Dans la **stratégie de liens fiables pour votre organisation** , passez à la zone **bloquer les URL suivantes** .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-136">In the **Safe Links policy for your organization** fly out that appears, go to the **Block the following URLs** box.</span></span>

3. <span data-ttu-id="6f9f5-137">Configurez une ou plusieurs entrées comme décrit dans [la syntaxe d’entrée pour la liste « bloquer les URL suivantes »](atp-safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-137">Configure one or more entries as described in [Entry syntax for the "Block the following URLs" list](atp-safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span></span>

   <span data-ttu-id="6f9f5-138">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-138">When you're finished, click **Save**.</span></span>

### <a name="configure-the-block-the-following-urls-list-in-powershell"></a><span data-ttu-id="6f9f5-139">Configurer la liste « bloquer les URL suivantes » dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9f5-139">Configure the "Block the following URLs" list in PowerShell</span></span>

<span data-ttu-id="6f9f5-140">Pour plus d’informations sur la syntaxe d’entrée, voir la [syntaxe d’entrée pour la liste « bloquer les URL suivantes »](atp-safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-140">For details about the entry syntax, see [Entry syntax for the "Block the following URLs" list](atp-safe-links.md#entry-syntax-for-the-block-the-following-urls-list).</span></span>

<span data-ttu-id="6f9f5-141">Vous pouvez utiliser la cmdlet **Get-AtpPolicyForO365** pour afficher les entrées existantes dans la propriété _BlockURLs_ .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-141">You can use the **Get-AtpPolicyForO365** cmdlet to view existing entries in the _BlockURLs_ property.</span></span>

- <span data-ttu-id="6f9f5-142">Pour ajouter des valeurs qui remplaceront toutes les entrées existantes, utilisez la syntaxe suivante dans Exchange Online PowerShell ou Exchange Online Protection PowerShell :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-142">To add values that will replace any existing entries, use the following syntax in Exchange Online PowerShell or Exchange Online Protection PowerShell:</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls "Entry1","Entry2",..."EntryN"
  ```

  <span data-ttu-id="6f9f5-143">Cet exemple montre comment ajouter les entrées suivantes à la liste :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-143">This example adds the following entries to the list:</span></span>

  - <span data-ttu-id="6f9f5-144">Bloquez le domaine, les sous-domaines et les chemins d’accès pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-144">Block the domain, subdomains, and paths for fabrikam.com.</span></span>
  - <span data-ttu-id="6f9f5-145">Bloquer la recherche de sous-domaine, mais pas le domaine parent, ni les autres sous-domaines dans tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="6f9f5-145">Block the subdomain research, but not the parent domain or other subdomains in tailspintoys.com</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls "fabrikam.com","https://research.tailspintoys.com*"
  ```

- <span data-ttu-id="6f9f5-146">Pour ajouter ou supprimer des valeurs sans affecter les entrées existantes, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-146">To add or remove values without affecting other existing entries, use the following syntax:</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls @{Add="Entry1","Entry2"...; Remove="Entry3","Entry4"...}
  ```

  <span data-ttu-id="6f9f5-147">Cet exemple montre comment ajouter une nouvelle entrée pour adatum.com et supprimer l’entrée pour fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-147">This example adds a new entry for adatum.com, and removes the entry for fabrikam.com.</span></span>

  ```powershell
  Set-AtpPolicyForO365 -BlockUrls @{Add="adatum.com"; Remove="fabrikam"}
  ```

## <a name="configure-safe-links-protection-for-office-365-apps-in-the-security--compliance-center"></a><span data-ttu-id="6f9f5-148">Configuration de la protection des liens fiables pour les applications Office 365 dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="6f9f5-148">Configure Safe Links protection for Office 365 apps in the Security & Compliance Center</span></span>

<span data-ttu-id="6f9f5-149">La protection des liens fiables pour les applications Office 365 s’applique aux documents dans les applications de bureau, mobiles et Web Office prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-149">Safe Links protection for Office 365 apps applies to documents in supported Office desktop, mobile, and web apps.</span></span> <span data-ttu-id="6f9f5-150">Pour plus d’informations, consultez la rubrique [paramètres de liens approuvés pour les applications Office 365](atp-safe-links.md#safe-links-settings-for-office-365-apps).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-150">For more information, see [Safe Links settings for Office 365 apps](atp-safe-links.md#safe-links-settings-for-office-365-apps).</span></span>

1. <span data-ttu-id="6f9f5-151">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \> **Policy** \> **liens approuvés ATP**, puis cliquez sur **paramètres globaux**.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-151">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, and then click **Global settings**.</span></span>

2. <span data-ttu-id="6f9f5-152">Dans la **stratégie de liens fiables pour votre organisation** , la fonctionnalité de survol qui s’affiche, configurez les paramètres suivants dans la section **paramètres qui s’appliquent au contenu à l’exception de la messagerie** :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-152">In the **Safe Links policy for your organization** fly out that appears, configure the following settings in the **Settings that apply to content except email** section:</span></span>

   - <span data-ttu-id="6f9f5-153">**Applications office 365**: Vérifiez que le bouton bascule est sur la droite pour activer les liens fiables pour les applications Office 365 prises en charge : ![ activer/désactiver ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-153">**Office 365 applications**: Verify the toggle is to the right to enable Safe Links for supported Office 365 apps: ![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png).</span></span>

   - <span data-ttu-id="6f9f5-154">**Ne pas suivre lorsque les utilisateurs cliquent sur les liens fiables**: déplacer le bouton bascule vers la gauche pour suivre les clics d’utilisateur liés aux URL bloquées dans les applications Office 365 prises en charge : désactiver ![ ](../../media/scc-toggle-off.png) .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-154">**Do not track when users click Safe Links**: Move the toggle to the left to track user clicks related to blocked URLs in supported Office 365 apps: ![Toggle off](../../media/scc-toggle-off.png).</span></span>

   - <span data-ttu-id="6f9f5-155">**Ne laissez pas les utilisateurs cliquer via les liens fiables à l’URL d’origine**: Vérifiez que le bouton bascule est sur la droite pour empêcher les utilisateurs de cliquer sur l’URL bloquée d’origine dans les applications Office 365 prises en charge : ![ activer/désactiver ](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png) .</span><span class="sxs-lookup"><span data-stu-id="6f9f5-155">**Do not let users click through Safe Links to the original URL**: Verify the toggle is to the right to prevent users from clicking through to the original blocked URL in supported Office 365 apps: ![Toggle on](../../media/963dfcd0-1765-4306-bcce-c3008c4406b9.png).</span></span>

   <span data-ttu-id="6f9f5-156">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-156">When you're finished, click **Save**.</span></span>

### <a name="configure-safe-links-protection-for-office-365-apps-in-powershell"></a><span data-ttu-id="6f9f5-157">Configurer la protection des liens fiables pour les applications Office 365 dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f9f5-157">Configure Safe Links protection for Office 365 apps in PowerShell</span></span>

<span data-ttu-id="6f9f5-158">Si vous préférez utiliser PowerShell pour configurer la protection des liens approuvés pour les applications Office 365, utilisez la syntaxe suivante dans Exchange Online PowerShell ou Exchange Online Protection PowerShell :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-158">If you'd rather use PowerShell to configure Safe Links protection for Office 365 apps, use the following syntax in Exchange Online PowerShell or Exchange Online Protection PowerShell:</span></span>

```powershell
Set-AtpPolicyForO365 [-EnableSafeLinksForO365Clients <$true | $false> [-AllowClickThrough <$true | $false>] [-TrackClicks <$true | $false>]
```

<span data-ttu-id="6f9f5-159">Cet exemple montre comment configurer les paramètres suivants pour la protection des liens fiables dans les applications Office 365 :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-159">This example configures the following settings for Safe Links protection in Office 365 apps:</span></span>

- <span data-ttu-id="6f9f5-160">Les liens approuvés pour les applications Office 365 sont activés (nous n’utilisons pas le paramètre _EnableSafeLinksForO365Clients_ et la valeur par défaut est $true).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-160">Safe Links for Office 365 apps is turned on (we aren't using the _EnableSafeLinksForO365Clients_ parameter, and the default value is $true).</span></span>
- <span data-ttu-id="6f9f5-161">Les utilisateurs cliquent sur en relation avec les URL bloquées dans les applications Office 365 prises en charge sont suivies.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-161">User clicks related to blocked URLs in supported Office 365 apps are tracked.</span></span>
- <span data-ttu-id="6f9f5-162">Les utilisateurs ne sont pas autorisés à cliquer à travers l’URL bloquée d’origine dans les applications Office 365 prises en charge (nous n’utilisons pas le paramètre _AllowClickThrough_ et la valeur par défaut est $false).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-162">Users are not allowed to click through to the original blocked URL in supported Office 365 apps (we aren't using the _AllowClickThrough_ parameter, and the default value is $false).</span></span>

```powershell
Set-AtpPolicyForO365 -TrackClicks $true
```

<span data-ttu-id="6f9f5-163">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-163">For detailed syntax and parameter information, see [Set-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/set-atppolicyforo365).</span></span>

## <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="6f9f5-164">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="6f9f5-164">How do you know these procedures worked?</span></span>

<span data-ttu-id="6f9f5-165">Pour vérifier que vous avez bien configuré les paramètres globaux pour les liens fiables (la liste **bloquer les URL suivantes** et les paramètres protection des applications Office 365), effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-165">To verify that you've successfully configured the global settings for Safe Links (the **Block the following URLs** list and the Office 365 app protection settings), do any of the following steps:</span></span>

- <span data-ttu-id="6f9f5-166">Dans le centre de sécurité & conformité, accédez à la stratégie de **gestion des menaces** - \> **Policy** \> **liens approuvés ATP**, cliquez sur **paramètres globaux**et vérifiez les paramètres dans le survol qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6f9f5-166">In the Security & Compliance Center, go to **Threat management** \> **Policy** \> **ATP Safe Links**, click **Global settings**, and verify the settings in the fly out that appears.</span></span>

- <span data-ttu-id="6f9f5-167">Dans Exchange Online PowerShell ou Exchange Online Protection PowerShell, exécutez la commande suivante et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="6f9f5-167">In Exchange Online PowerShell or Exchange Online Protection PowerShell, run the following command and verify the settings:</span></span>

  ```powershell
  Get-AtpPolicyForO365 | Format-List BlockUrls,EnableSafeLinksForO365Clients,AllowClickThrough,TrackClicks
  ```

  <span data-ttu-id="6f9f5-168">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Get-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/get-atppolicyforo365).</span><span class="sxs-lookup"><span data-stu-id="6f9f5-168">For detailed syntax and parameter information, see [Get-AtpPolicyForO365](https://docs.microsoft.com/powershell/module/exchange/get-atppolicyforo365).</span></span>
