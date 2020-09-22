---
title: Configurer une liste d’URL bloquées personnalisée à l’aide de liens fiables ATP
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment configurer une liste d’URL bloquées pour votre organisation à l’aide d’Office 365 Advanced Threat Protection.
ms.openlocfilehash: e153d5631c12d52564643477216b777cdbc49433
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201002"
---
# <a name="set-up-a-custom-blocked-urls-list-using-atp-safe-links"></a><span data-ttu-id="19041-103">Configurer une liste d’URL bloquées personnalisée à l’aide de liens fiables ATP</span><span class="sxs-lookup"><span data-stu-id="19041-103">Set up a custom blocked URLs list using ATP Safe Links</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!IMPORTANT]
> <span data-ttu-id="19041-104">Cet article est destiné aux entreprises qui ont [Office 365 – Protection avancée contre les menaces](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="19041-104">This article is intended for business customers who have [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="19041-105">Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur les liens fiables dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="19041-105">If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.microsoft.com/office/882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="19041-106">Avec [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), votre organisation peut avoir une liste personnalisée d’adresses de sites Web (URL) bloquées.</span><span class="sxs-lookup"><span data-stu-id="19041-106">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked.</span></span> <span data-ttu-id="19041-107">Lorsqu’une URL est bloquée, les personnes qui cliquent sur les liens vers l’URL bloquée sont dirigées vers une [page d’avertissement](atp-safe-links-warning-pages.md) semblable à l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="19041-107">When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span>

![Ce site est bloqué](../../media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)

<span data-ttu-id="19041-109">La liste des URL bloquées est définie par l’équipe de sécurité Microsoft 365 de votre organisation et s’applique à tous les membres de l’organisation qui sont couverts par les stratégies de liens approuvés Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="19041-109">The blocked URLs list is defined by your organization's Microsoft 365 for business security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span>

<span data-ttu-id="19041-110">Lisez cet article pour découvrir comment configurer la liste des URL bloquées personnalisées de votre organisation pour les [liens fiables ATP dans Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="19041-110">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>

## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="19041-111">Afficher ou modifier une liste personnalisée d’URL bloquées</span><span class="sxs-lookup"><span data-stu-id="19041-111">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="19041-112">Les [liens approuvés ATP dans Office 365](atp-safe-links.md) utilisent plusieurs listes, y compris la liste des URL bloquées personnalisées de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="19041-112">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list.</span></span> <span data-ttu-id="19041-113">Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="19041-113">If you have the necessary permissions, you can set up your organization's custom list.</span></span> <span data-ttu-id="19041-114">Pour ce faire, vous devez modifier la stratégie de liens approuvés par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="19041-114">You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="19041-115">Pour modifier (ou définir) des stratégies ATP, vous devez disposer de l’un des rôles décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="19041-115">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

****

|<span data-ttu-id="19041-116">Rôle</span><span class="sxs-lookup"><span data-stu-id="19041-116">Role</span></span>|<span data-ttu-id="19041-117">WHERE/How Assigned</span><span class="sxs-lookup"><span data-stu-id="19041-117">Where/how assigned</span></span>|
|---|---|
|<span data-ttu-id="19041-118">administrateur général</span><span class="sxs-lookup"><span data-stu-id="19041-118">global administrator</span></span>|<span data-ttu-id="19041-119">La personne qui s’inscrit pour acheter Microsoft 365 est un administrateur global par défaut.</span><span class="sxs-lookup"><span data-stu-id="19041-119">The person who signs up to buy Microsoft 365 is a global admin by default.</span></span> <span data-ttu-id="19041-120">(Pour en savoir plus, consultez la rubrique [à propos des rôles d’administrateur Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="19041-120">(See [About Microsoft 365 admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles) to learn more.)</span></span>|
|<span data-ttu-id="19041-121">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="19041-121">Security Administrator</span></span>|<span data-ttu-id="19041-122">Centre d’administration Azure Active Directory ( [https://aad.portal.azure.com](https://aad.portal.azure.com) )</span><span class="sxs-lookup"><span data-stu-id="19041-122">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="19041-123">Gestion d’Organisation Exchange Online</span><span class="sxs-lookup"><span data-stu-id="19041-123">Exchange Online Organization Management</span></span>|<span data-ttu-id="19041-124">Centre d’administration Exchange ( [https://outlook.office365.com/ecp](https://outlook.office365.com/ecp) )</span><span class="sxs-lookup"><span data-stu-id="19041-124">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="19041-125">ou</span><span class="sxs-lookup"><span data-stu-id="19041-125">or</span></span> <br>  <span data-ttu-id="19041-126">Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell))</span><span class="sxs-lookup"><span data-stu-id="19041-126">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell))</span></span>|
|

> [!TIP]
> <span data-ttu-id="19041-127">Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="19041-127">To learn more about roles and permissions, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a><span data-ttu-id="19041-128">Pour afficher ou modifier une liste d’URL bloquées personnalisée</span><span class="sxs-lookup"><span data-stu-id="19041-128">To view or edit a custom blocked URLs list</span></span>

1. <span data-ttu-id="19041-129">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="19041-129">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span>

2. <span data-ttu-id="19041-130">Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **Policy** \> **liens approuvés**de stratégie.</span><span class="sxs-lookup"><span data-stu-id="19041-130">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>

3. <span data-ttu-id="19041-131">Dans la section **stratégies qui s’appliquent à l’ensemble de l’organisation** , sélectionnez **par défaut**, puis **modifier** (le bouton modifier ressemble à un crayon).</span><span class="sxs-lookup"><span data-stu-id="19041-131">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="19041-132">![Cliquez sur modifier pour modifier votre stratégie par défaut pour la protection des liens fiables.](../../media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="19041-132">![Click Edit to edit your default policy for Safe Links protection](../../media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="19041-133">Cela vous permet d’afficher la liste des URL bloquées.</span><span class="sxs-lookup"><span data-stu-id="19041-133">This enables you to view your list of blocked URLs.</span></span> <span data-ttu-id="19041-134">Dans un premier temps, il se peut que vous n’ayez aucune URL répertoriée ici.</span><span class="sxs-lookup"><span data-stu-id="19041-134">At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="19041-135">![Liste des URL bloquées dans la stratégie de liens approuvés par défaut](../../media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="19041-135">![Blocked URLs list in the default Safe Links policy](../../media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>

4. <span data-ttu-id="19041-136">Sélectionnez la zone **Entrez une URL valide** , tapez une URL, puis choisissez le signe plus ( **+** ).</span><span class="sxs-lookup"><span data-stu-id="19041-136">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span>

5. <span data-ttu-id="19041-137">Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="19041-137">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>

## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="19041-138">Quelques éléments à garder à l’esprit</span><span class="sxs-lookup"><span data-stu-id="19041-138">A few things to keep in mind</span></span>

<span data-ttu-id="19041-139">Lorsque vous ajoutez des URL à votre liste, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="19041-139">While you add URLs to your list, keep the following points in mind:</span></span>

- <span data-ttu-id="19041-140">N’incluez pas une barre oblique ( **/** ) à la fin de l’URL.</span><span class="sxs-lookup"><span data-stu-id="19041-140">Do not include a forward slash ( **/**) at the end of the URL.</span></span> <span data-ttu-id="19041-141">Par exemple, au lieu de taper `https://www.contoso.com/` , entrez `https://www.contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="19041-141">For example, instead of entering `https://www.contoso.com/`, enter `https://www.contoso.com`.</span></span>

- <span data-ttu-id="19041-142">Vous pouvez spécifier une URL de domaine uniquement (par `contoso.com` exemple `tailspintoys.com` , ou).</span><span class="sxs-lookup"><span data-stu-id="19041-142">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`).</span></span> <span data-ttu-id="19041-143">Cette opération bloque les clics sur les URL qui contiennent le domaine.</span><span class="sxs-lookup"><span data-stu-id="19041-143">This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="19041-144">Vous pouvez spécifier un sous-domaine (par exemple `toys.contoso.com*` ) sans bloquer un domaine complet (par exemple `contoso.com` ,).</span><span class="sxs-lookup"><span data-stu-id="19041-144">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`).</span></span> <span data-ttu-id="19041-145">Cette opération bloque le clic sur toute URL qui contient le sous-domaine, mais ne bloque pas les clics vers une URL qui contient le domaine complet.</span><span class="sxs-lookup"><span data-stu-id="19041-145">This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>

- <span data-ttu-id="19041-146">Vous pouvez inclure jusqu’à trois astérisques génériques ( \* ) par URL.</span><span class="sxs-lookup"><span data-stu-id="19041-146">You can include up to three wildcard asterisks (\*) per URL.</span></span> <span data-ttu-id="19041-147">Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et de l’effet de ces entrées.</span><span class="sxs-lookup"><span data-stu-id="19041-147">The following table lists some examples of what you can enter and what effect those entries have.</span></span>

****

|<span data-ttu-id="19041-148">Exemple d’entrée</span><span class="sxs-lookup"><span data-stu-id="19041-148">Example Entry</span></span>|<span data-ttu-id="19041-149">Ce qu’il fait</span><span class="sxs-lookup"><span data-stu-id="19041-149">What It Does</span></span>|
|---|---|
|<span data-ttu-id="19041-150">`contoso.com` ou `*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="19041-150">`contoso.com` or `*contoso.com*`</span></span>|<span data-ttu-id="19041-151">Bloque le domaine, les sous-domaines et les chemins d’accès, par exemple, `https://www.contoso.com` `https://sub.contoso.com` et `https://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="19041-151">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `https://sub.contoso.com`, and `https://contoso.com/abc`</span></span>|
|`https://contoso.com/a`|<span data-ttu-id="19041-152">Bloque un site, mais pas les sous- `https://contoso.com/a` chemins supplémentaires comme `https://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="19041-152">Blocks a site `https://contoso.com/a` but not additional subpaths like `https://contoso.com/a/b`</span></span>|
|`https://contoso.com/a*`|<span data-ttu-id="19041-153">Bloque un site `https://contoso.com/a` et des sous-chemins supplémentaires comme `https://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="19041-153">Blocks a site `https://contoso.com/a` and additional subpaths like `https://contoso.com/a/b`</span></span>|
|`https://toys.contoso.com*`|<span data-ttu-id="19041-154">Bloque un sous-domaine (« jouets » dans ce cas) tout en permettant de cliquer sur d’autres URL de domaine (par exemple `https://contoso.com` `https://home.contoso.com` , ou).</span><span class="sxs-lookup"><span data-stu-id="19041-154">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `https://contoso.com` or `https://home.contoso.com`).</span></span>|
|

> [!NOTE]
> <span data-ttu-id="19041-155">Par défaut, vous pouvez uniquement ajouter 500 URL à la liste d’URL bloquées dans la stratégie par défaut des liens approuvés Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="19041-155">By default, you can only add 500 URLs to the blocked URL list in the Office 365 ATP Safe Links default policy.</span></span> <span data-ttu-id="19041-156">Une URL individuelle ne peut pas dépasser 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="19041-156">An individual URL can't exceed 128 characters.</span></span> <span data-ttu-id="19041-157">La liste des URL bloquées entière ne peut pas dépasser 10 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="19041-157">The entire Blocked URL list can't exceed 10,000 characters.</span></span>

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="19041-158">Procédure de définition des exceptions pour certains utilisateurs d’une organisation</span><span class="sxs-lookup"><span data-stu-id="19041-158">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="19041-159">Si vous souhaitez que certains groupes puissent afficher les URL susceptibles d’être bloquées pour d’autres, vous pouvez spécifier une stratégie de liens approuvés ATP qui s’applique à des destinataires spécifiques.</span><span class="sxs-lookup"><span data-stu-id="19041-159">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients.</span></span> <span data-ttu-id="19041-160">Consultez [la rubrique Configurer une liste d’URL personnalisée « ne pas réécrire » à l’aide des liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="19041-160">See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
