---
title: Attribuer des licences aux utilisateurs
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: sinakassaw, nicholak
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- TopSMBIssues
- SaRA
- okr_SMB
- manage_licenses
- commerce_licensing
search.appverid: MET150
description: Découvrez comment attribuer des licences aux utilisateurs.
ms.date: 04/26/2021
ms.openlocfilehash: ef8169658c6aef03cf8ff0cf9714c980ce63b060
ms.sourcegitcommit: 967f64dfa1a05f31179c8316b96bfb7758a5d990
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52332485"
---
# <a name="assign-licenses-to-users"></a><span data-ttu-id="0b62e-103">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0b62e-103">Assign licenses to users</span></span>

<span data-ttu-id="0b62e-104">Vous pouvez attribuer des licences à des utilisateurs à partir de la page des **Utilisateurs actifs** ou de la page des **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-104">You can assign licenses to users on either the **Active users** page, or on the **Licenses** page.</span></span> <span data-ttu-id="0b62e-105">La méthode utilisée dépend de votre souhait d’attribuer des licences de produit à des utilisateurs déterminés ou d’attribuer des licences aux utilisateurs pour un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="0b62e-105">The method you use depends on whether you want to assign product licenses to specific users or assign users licenses to a specific product.</span></span>

> [!NOTE]
> <span data-ttu-id="0b62e-106">En tant qu’administrateur, vous ne pouvez pas attribuer ou annuler des attributions de licences pour un abonnement d’achat en libre-service acheté par un utilisateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0b62e-106">As an admin, you can't assign or unassign licenses for a self-service purchase subscription bought by a user in your organization.</span></span> <span data-ttu-id="0b62e-107">Vous pouvez [prendre le contrôle d’un abonnement d’achat en libre-service](../../commerce/subscriptions/manage-self-service-purchases-admins.md#take-over-a-self-service-purchase-subscription), puis attribuer ou annuler des attributions de licences.</span><span class="sxs-lookup"><span data-stu-id="0b62e-107">You can [take over a self-service purchase subscription](../../commerce/subscriptions/manage-self-service-purchases-admins.md#take-over-a-self-service-purchase-subscription), and then assign or unassign licenses.</span></span>

<span data-ttu-id="0b62e-108">[Découvrez comment ajouter un utilisateur et attribuer une licence en même temps](../add-users/add-users.md).</span><span class="sxs-lookup"><span data-stu-id="0b62e-108">[Learn how to add a user and assign a license at the same time](../add-users/add-users.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0b62e-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0b62e-109">Before you begin</span></span>

- <span data-ttu-id="0b62e-110">Vous devez être un administrateur général, une licence ou un administrateur d’utilisateur pour attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="0b62e-110">You must be a Global, License, or User admin to assign licenses.</span></span> <span data-ttu-id="0b62e-111">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0b62e-111">For more information, see [About Microsoft 365 admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="0b62e-112">Vous pouvez [attribuer des licences Microsoft 365 à des comptes utilisateurs avec PowerShell](../../enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="0b62e-112">You can [assign Microsoft 365 licenses to user accounts with PowerShell](../../enterprise/assign-licenses-to-user-accounts-with-microsoft-365-powershell.md).</span></span>
- <span data-ttu-id="0b62e-113">Pour utiliser la gestion des licences basée sur les groupes, voir [Attribuer des licences aux utilisateurs par appartenance aux groupes dans Azure Active Directory](/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="0b62e-113">To use group-based licensing, see [Assign licenses to users by group membership in Azure Active Directory](/azure/active-directory/users-groups-roles/licensing-groups-assign)</span></span>
- <span data-ttu-id="0b62e-114">Certains services, tels que Sway, sont automatiquement attribués aux utilisateurs et n’ont donc pas besoin d’être attribués individuellement.</span><span class="sxs-lookup"><span data-stu-id="0b62e-114">Some services, like Sway, are automatically assigned to users, and don't need to be assigned individually.</span></span>


## <a name="use-the-licenses-page-to-assign-licenses-to-users"></a><span data-ttu-id="0b62e-115">Utiliser la page licences pour attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0b62e-115">Use the Licenses page to assign licenses to users</span></span>

<span data-ttu-id="0b62e-116">Lorsque vous utilisez la page **Licences** pour l'attribution de licences, vous attribuez des licences pour un produit spécifique à un maximum de 20 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b62e-116">When you use the **Licenses** page to assign licenses, you assign licenses for a specific product to up to 20 users.</span></span> <span data-ttu-id="0b62e-117">Dans la page **Licences**, une liste de tous les produits auxquels vous avez des abonnements s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0b62e-117">On the **Licenses** page, you see a list of all the products that you have subscriptions for.</span></span> <span data-ttu-id="0b62e-118">Vous pouvez également voir le nombre total de licences pour chaque produit, le nombre de licences attribuées et le nombre de licences disponibles.</span><span class="sxs-lookup"><span data-stu-id="0b62e-118">You also see the total number of licenses for each product, how many licenses are assigned, and how many are available.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b62e-119">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="0b62e-119">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="0b62e-120">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, choisissez la page **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-120">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b62e-121">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, choisissez la page **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-121">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>

::: moniker-end

2. <span data-ttu-id="0b62e-122">Sélectionnez un produit.</span><span class="sxs-lookup"><span data-stu-id="0b62e-122">Select a product.</span></span>
3. <span data-ttu-id="0b62e-123">Dans la page Détails du produit, sélectionnez **attribuer des licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-123">On the product details page, select **Assign licenses**.</span></span>
4. <span data-ttu-id="0b62e-124">Dans le volet **Attribuer des licences aux utilisateurs**, commencez à saisir un nom, puis sélectionnez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="0b62e-124">In the **Assign licenses to users** pane, begin typing a name, and then choose it from the results to add it to the list.</span></span> <span data-ttu-id="0b62e-125">Vous pouvez ajouter jusqu'à 20 utilisateurs à la fois.</span><span class="sxs-lookup"><span data-stu-id="0b62e-125">You can add up to 20 users at a time.</span></span>
4. <span data-ttu-id="0b62e-126">Sélectionnez **Activer ou désactiver les applications et les services** pour attribuer ou supprimer l’accès à des éléments particuliers.</span><span class="sxs-lookup"><span data-stu-id="0b62e-126">Select **Turn apps and services on or off** to assign or remove access to specific items.</span></span>
6. <span data-ttu-id="0b62e-127">Lorsque vous avez terminé, sélectionnez **Attribuer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-127">When you're finished, select **Assign**, then select **Close**.</span></span>

<span data-ttu-id="0b62e-128">S’il existe un conflit, un message s’affiche, vous indiquant la nature du problème et comment le résoudre.</span><span class="sxs-lookup"><span data-stu-id="0b62e-128">If there's a conflict, a message displays, tells you what the problem is, and tells you how to fix it.</span></span> <span data-ttu-id="0b62e-129">Par exemple, si vous avez sélectionné des licences contenant des services en conflit, le message d’erreur indique de vérifier les services inclus dans chaque licence et de réessayer.</span><span class="sxs-lookup"><span data-stu-id="0b62e-129">For example, if you selected licenses that contain conflicting services, the error message says to review the services included with each license and try again.</span></span>

## <a name="change-the-apps-and-services-a-user-has-access-to"></a><span data-ttu-id="0b62e-130">Modifier les applications et les services auxquels un utilisateur a accès</span><span class="sxs-lookup"><span data-stu-id="0b62e-130">Change the apps and services a user has access to</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b62e-131">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="0b62e-131">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="0b62e-132">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, choisissez la page **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-132">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b62e-133">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, choisissez la page **Facturation** > **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-133">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>

::: moniker-end

2. <span data-ttu-id="0b62e-134">Dans la page **Licences**, sélectionnez la ligne d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="0b62e-134">On the **Licenses** page, select the row for a specific user.</span></span>
3. <span data-ttu-id="0b62e-135">Dans le volet droit, sélectionnez ou désélectionnez les applications et services auxquels vous voulez octroyer ou supprimer l'accès.</span><span class="sxs-lookup"><span data-stu-id="0b62e-135">In the right pane, select or deselect the apps and services that you want to give access to or remove access from.</span></span>
4. <span data-ttu-id="0b62e-136">Une fois terminé, sélectionnez **Enregistrer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-136">When you're finished, select **Save**, then select **Close**.</span></span>

## <a name="use-the-active-users-page-to-assign-licenses"></a><span data-ttu-id="0b62e-137">Utiliser la page utilisateurs actifs pour attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="0b62e-137">Use the Active users page to assign licenses</span></span>

<span data-ttu-id="0b62e-138">Lorsque vous utilisez la page **Utilisateurs actifs** pour attribuer des licences, vous attribuez des licences aux produits pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b62e-138">When you use the **Active users** page to assign licenses, you assign users licenses to products.</span></span>

### <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="0b62e-139">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0b62e-139">Assign licenses to multiple users</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b62e-140">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0b62e-140">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="0b62e-141">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Facturation** > **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-141">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b62e-142">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Facturation** > **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-142">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

2. <span data-ttu-id="0b62e-143">Sélectionnez les cercles en regard des noms d'utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="0b62e-143">Select the circles next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="0b62e-144">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-144">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="0b62e-145">Dans le volet **Attribuer des licences de produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-145">In the **Manage product licenses** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="0b62e-146">Dans le volet **Ajouter aux produits existants**, positionnez le bouton bascule sur **Actif** correspondant à la licence que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="0b62e-146">In the **Add to existing products** pane, switch the toggle to the **On** position for the license that you want the selected users to have.</span></span>\
    <span data-ttu-id="0b62e-147">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b62e-147">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="0b62e-148">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b62e-148">You can limit which services are available to the users.</span></span> <span data-ttu-id="0b62e-149">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0b62e-149">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="0b62e-150">Dans la partie inférieure du volet, sélectionnez **Ajouter** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-150">At the bottom of the pane, select **Add** \> **Close**.</span></span>  


> [!NOTE]
> <span data-ttu-id="0b62e-151">Si vous voulez attribuer des licences à un grand nombre d’utilisateurs, utilisez [Attribuer des licences aux utilisateurs en les appartenance aux groupes dans Azure Active Directory.](/azure/active-directory/enterprise-users/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="0b62e-151">If you want to assign licenses for a large number of users, use [Assign licenses to users by group membership in Azure Active Directory](/azure/active-directory/enterprise-users/licensing-groups-assign)</span></span>

### <a name="assign-licenses-to-one-user"></a><span data-ttu-id="0b62e-152">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="0b62e-152">Assign licenses to one user</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0b62e-153">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0b62e-153">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="0b62e-154">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Facturation** > **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-154">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0b62e-155">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Facturation** > **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-155">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

2. <span data-ttu-id="0b62e-156">Sélectionnez la ligne de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="0b62e-156">Select the row of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="0b62e-157">Dans le volet de droite, sélectionnez **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-157">In the right pane, select **Licenses and Apps**.</span></span>
4. <span data-ttu-id="0b62e-158">Développez la section **Licences**, sélectionnez les cases des licences à attribuer, puis choisissez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-158">Expand the **Licenses** section, select the boxes for the licenses that you want to assign, then select **Save changes**.</span></span>

## <a name="assign-a-license-to-a-guest-user"></a><span data-ttu-id="0b62e-159">Attribuer une licence à un utilisateur invité</span><span class="sxs-lookup"><span data-stu-id="0b62e-159">Assign a license to a guest user</span></span>

<span data-ttu-id="0b62e-160">Vous pouvez inviter des utilisateurs invités à collaborer avec votre organisation dans le Centre d’administration Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0b62e-160">You can invite guest users to collaborate with your organization in the Azure Active Directory admin center.</span></span> <span data-ttu-id="0b62e-161">Pour en savoir plus sur l’estimation des utilisateurs, consultez[Qu’est-ce que l’accès utilisateur invité dans Azure Active Directory B2B ?](/azure/active-directory/external-identities/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="0b62e-161">To learn about guest users, see [What is guest user access in Azure Active Directory B2B?](/azure/active-directory/external-identities/what-is-b2b).</span></span> <span data-ttu-id="0b62e-162">Si vous n’avez pas d’utilisateurs invités, consultez [Démarrage rapide : ajouter des utilisateurs invités à votre annuaire dans le portail Azure](/azure/active-directory/external-identities/b2b-quickstart-add-guest-users-portal).</span><span class="sxs-lookup"><span data-stu-id="0b62e-162">If you don't have any guest users, see [Quickstart: Add guest users to your directory in the Azure portal](/azure/active-directory/external-identities/b2b-quickstart-add-guest-users-portal).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b62e-163">Vous devez être un administrateur général pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="0b62e-163">You must be a Global admin to do these steps.</span></span>

1. <span data-ttu-id="0b62e-164">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2067268" target="_blank">Centre d’administration Azure Active Directory</a></span><span class="sxs-lookup"><span data-stu-id="0b62e-164">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2067268" target="_blank">Azure Active Directory admin center</a></span></span>
2. <span data-ttu-id="0b62e-165">Dans le volet de navigation, sélectionnez **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-165">In the navigation pane, select **Users**.</span></span>
3. <span data-ttu-id="0b62e-166">Dans la page **utilisateurs | Tous les utilisateurs (aperçu)**, sélectionnez **Ajouter des filtres**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-166">On the **Users | All Users (Preview)** page, select **Add filters**.</span></span>
4. <span data-ttu-id="0b62e-167">Dans le menu **Sélectionner un champ** , sélectionnez **Type d’utilisateur**, puis **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-167">In the **Pick a field** menu, choose **User type**, then select **Apply**.</span></span>
5. <span data-ttu-id="0b62e-168">Dans le menu suivant, sélectionnez **Invité**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-168">In the next menu, select **Guest**.</span></span>
6. <span data-ttu-id="0b62e-169">Dans la liste des résultats, sélectionnez l’utilisateur ayant besoin d’une licence.</span><span class="sxs-lookup"><span data-stu-id="0b62e-169">In the list of results, select the user who needs a license.</span></span>
7. <span data-ttu-id="0b62e-170">Sous **Gérer**, sélectionnez **Licences**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-170">Under **Manage**, select **Licenses**.</span></span>
8. <span data-ttu-id="0b62e-171">Sélectionnez **Devoirs**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-171">Select **Assignments**.</span></span>
9. <span data-ttu-id="0b62e-172">Sur la page **Mettre à jour les affectations de licence** , sélectionnez le produit pour lequel vous voulez affecter une licence.</span><span class="sxs-lookup"><span data-stu-id="0b62e-172">On the **Update license assignments** page, select the product you want to assign a license for.</span></span>
10. <span data-ttu-id="0b62e-173">Sur la droite, désactivez les cases à cocher des services auxquels vous ne voulez pas que l’utilisateur invité ait accès.</span><span class="sxs-lookup"><span data-stu-id="0b62e-173">On the right, clear the check boxes for any services you don't want the guest user to have access to.</span></span>
11. <span data-ttu-id="0b62e-174">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0b62e-174">Select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0b62e-175">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0b62e-175">Next steps</span></span>

<span data-ttu-id="0b62e-176">Si les applications Office ne sont pas encore installées sur vos utilisateurs, vous pouvez partager le[Guide de démarrage rapide d’employées](../../business-video/employee-quick-setup.md) avec vos utilisateurs pour configurer des éléments, par [comment télécharger et installer Microsoft 365 ou Office 2019 sur un PC ou Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) et [comment configurer les applications Office et la messagerie électronique sur un appareil mobile](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span><span class="sxs-lookup"><span data-stu-id="0b62e-176">If your users don't yet have the Office apps installed, you can share the [Employee quick start guide](../../business-video/employee-quick-setup.md) with your users to set up things, like [how to download and install Microsoft 365 or Office 2019 on a PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) and [how to set up Office apps and email on a mobile device](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span></span>

## <a name="related-content"></a><span data-ttu-id="0b62e-177">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="0b62e-177">Related content</span></span>

<span data-ttu-id="0b62e-178">[Comprendre les abonnements et les licences](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0b62e-178">[Understand subscriptions and licenses](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span></span>\
<span data-ttu-id="0b62e-179">[Déattribuer des licences aux utilisateurs](remove-licenses-from-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0b62e-179">[Unassign licenses from users](remove-licenses-from-users.md) (article)</span></span>\
<span data-ttu-id="0b62e-180">[Achetez ou supprimez des licences pour votre abonnement](../../commerce/licenses/buy-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0b62e-180">[Buy or remove licenses for your subscription](../../commerce/licenses/buy-licenses.md) (article)</span></span>
