---
title: Attribuer des licences aux utilisateurs
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Adm_TOC
- commerce
ms.custom:
- TopSMBIssues
- SaRA
- okr_SMB
- AdminSurgePortfolio
- manage_licenses
search.appverid:
- MET150
description: Découvrez comment attribuer des licences aux utilisateurs.
ms.date: 07/01/2020
ms.openlocfilehash: 648a3433bf5c2bd9bb96abb90335f56ee4fb6bee
ms.sourcegitcommit: 0650da0e54a2b484a3156b3aabe44397fbb38e00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "45015946"
---
# <a name="assign-licenses-to-users"></a><span data-ttu-id="78281-103">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78281-103">Assign licenses to users</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="78281-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="78281-104">The admin center is changing.</span></span> <span data-ttu-id="78281-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="78281-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

<span data-ttu-id="78281-106">Vous pouvez attribuer des licences à des utilisateurs à partir de la page des **Utilisateurs actifs** ou de la page des **Licences**.</span><span class="sxs-lookup"><span data-stu-id="78281-106">You can assign licenses to users on either the **Active users** page, or on the **Licenses** page.</span></span> <span data-ttu-id="78281-107">La méthode utilisée dépend de votre souhait d’attribuer des licences de produit à des utilisateurs déterminés ou d’attribuer des licences aux utilisateurs pour un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="78281-107">The method you use depends on whether you want to assign product licenses to specific users or assign users licenses to a specific product.</span></span>

::: moniker-end

<span data-ttu-id="78281-108">[Découvrez comment ajouter un utilisateur et attribuer une licence en même temps](../add-users/add-users.md).</span><span class="sxs-lookup"><span data-stu-id="78281-108">[Learn how to add a user and assign a license at the same time](../add-users/add-users.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="78281-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="78281-109">Before you begin</span></span>

- <span data-ttu-id="78281-110">Vous devez être un administrateur général, une licence ou un administrateur d’utilisateur pour attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="78281-110">You must be a Global, License, or User admin to assign licenses.</span></span> <span data-ttu-id="78281-111">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="78281-111">For more information, see [About Microsoft 365 admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="78281-112">Vous pouvez [attribuer des licences à des comptes utilisateurs avec Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?linkid=850410).</span><span class="sxs-lookup"><span data-stu-id="78281-112">You can [assign licenses to user accounts with Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?linkid=850410).</span></span>
- <span data-ttu-id="78281-113">Pour utiliser la gestion des licences basée sur les groupes, voir [Attribuer des licences aux utilisateurs par appartenance aux groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="78281-113">To use group-based licensing, see [Assign licenses to users by group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span></span>
- <span data-ttu-id="78281-114">Certains services, tels que Sway, sont automatiquement attribués aux utilisateurs et n’ont donc pas besoin d’être attribués individuellement.</span><span class="sxs-lookup"><span data-stu-id="78281-114">Some services, like Sway, are automatically assigned to users, and don't need to be assigned individually.</span></span>

::: moniker range="o365-worldwide"

## <a name="use-the-licenses-page-to-assign-licenses-to-users"></a><span data-ttu-id="78281-115">Utiliser la page licences pour attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78281-115">Use the Licenses page to assign licenses to users</span></span>

<span data-ttu-id="78281-116">Lorsque vous utilisez la page **Licences** pour l'attribution de licences, vous attribuez des licences pour un produit spécifique à un maximum de 20 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-116">When you use the **Licenses** page to assign licenses, you assign licenses for a specific product to up to 20 users.</span></span> <span data-ttu-id="78281-117">Dans la page **Licences**, une liste de tous les produits auxquels vous avez des abonnements s’affiche.</span><span class="sxs-lookup"><span data-stu-id="78281-117">On the **Licenses** page, you see a list of all the products that you have subscriptions for.</span></span> <span data-ttu-id="78281-118">Vous pouvez également voir le nombre total de licences pour chaque produit, le nombre de licences attribuées et le nombre de licences disponibles.</span><span class="sxs-lookup"><span data-stu-id="78281-118">You also see the total number of licenses for each product, how many licenses are assigned, and how many are available.</span></span>

1. <span data-ttu-id="78281-119">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-119">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="78281-120">Sélectionnez un produit.</span><span class="sxs-lookup"><span data-stu-id="78281-120">Select a product.</span></span>
3. <span data-ttu-id="78281-121">Dans la page Détails du produit, sélectionnez **attribuer des licences**.</span><span class="sxs-lookup"><span data-stu-id="78281-121">On the product details page, select **Assign licenses**.</span></span>
4. <span data-ttu-id="78281-122">Dans le volet **Attribuer des licences aux utilisateurs**, commencez à saisir un nom, puis sélectionnez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="78281-122">In the **Assign licenses to users** pane, begin typing a name, and then choose it from the results to add it to the list.</span></span> <span data-ttu-id="78281-123">Vous pouvez ajouter jusqu'à 20 utilisateurs à la fois.</span><span class="sxs-lookup"><span data-stu-id="78281-123">You can add up to 20 users at a time.</span></span>
5. <span data-ttu-id="78281-124">Sélectionnez **Activer ou désactiver les applications et les services** pour attribuer ou supprimer l’accès à des éléments particuliers.</span><span class="sxs-lookup"><span data-stu-id="78281-124">Select **Turn apps and services on or off** to assign or remove access to specific items.</span></span>
6. <span data-ttu-id="78281-125">Lorsque vous avez terminé, sélectionnez **Attribuer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-125">When you're finished, select **Assign**, then select **Close**.</span></span>

<span data-ttu-id="78281-126">S’il existe un conflit, un message s’affiche, vous indiquant la nature du problème et comment le résoudre.</span><span class="sxs-lookup"><span data-stu-id="78281-126">If there's a conflict, a message displays, tells you what the problem is, and tells you how to fix it.</span></span> <span data-ttu-id="78281-127">Par exemple, si vous avez sélectionné des licences contenant des services en conflit, le message d’erreur indique de vérifier les services inclus dans chaque licence et de réessayer.</span><span class="sxs-lookup"><span data-stu-id="78281-127">For example, if you selected licenses that contain conflicting services, the error message says to review the services included with each license and try again.</span></span>

## <a name="change-the-apps-and-services-a-user-has-access-to"></a><span data-ttu-id="78281-128">Modifier les applications et les services auxquels un utilisateur a accès</span><span class="sxs-lookup"><span data-stu-id="78281-128">Change the apps and services a user has access to</span></span>

1. <span data-ttu-id="78281-129">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-129">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="78281-130">Dans la page **Licences**, sélectionnez la ligne d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="78281-130">On the **Licenses** page, select the row for a specific user.</span></span>
3. <span data-ttu-id="78281-131">Dans le volet droit, sélectionnez ou désélectionnez les applications et services auxquels vous voulez octroyer ou supprimer l'accès.</span><span class="sxs-lookup"><span data-stu-id="78281-131">In the right pane, select or deselect the apps and services that you want to give access to or remove access from.</span></span>
4. <span data-ttu-id="78281-132">Une fois terminé, sélectionnez **Enregistrer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-132">When you're finished, select **Save**, then select **Close**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

## <a name="use-the-active-users-page-to-assign-licenses"></a><span data-ttu-id="78281-133">Utiliser la page utilisateurs actifs pour attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="78281-133">Use the Active users page to assign licenses</span></span>

<span data-ttu-id="78281-134">Lorsque vous utilisez la page **Utilisateurs actifs** pour attribuer des licences, vous attribuez des licences aux produits pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-134">When you use the **Active users** page to assign licenses, you assign users licenses to products.</span></span>

### <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="78281-135">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78281-135">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="78281-136">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-136">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-137">Sélectionnez les cercles en regard des noms d'utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="78281-137">Select the circles next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="78281-138">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="78281-138">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="78281-139">Dans le volet **Attribuer des licences de produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="78281-139">In the **Manage product licenses** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="78281-140">Dans le volet **Ajouter aux produits existants**, positionnez le bouton bascule sur **Actif**correspondant à la licence que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="78281-140">In the **Add to existing products** pane, switch the toggle to the **On** position for the license that you want the selected users to have.</span></span>\
    <span data-ttu-id="78281-141">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-141">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="78281-142">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-142">You can limit which services are available to the users.</span></span> <span data-ttu-id="78281-143">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-143">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="78281-144">Dans la partie inférieure du volet, sélectionnez **Ajouter** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-144">At the bottom of the pane, select **Add** \> **Close**.</span></span>  

::: moniker-end

::: moniker range="o365-germany"

## <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="78281-145">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78281-145">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="78281-146">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-146">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-147">Cochez les cases en regard des noms des utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="78281-147">Select the boxes next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="78281-148">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="78281-148">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="78281-149">Dans le volet **Attribuer des produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="78281-149">In the **Assign products** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="78281-150">Positionnez le bouton bascule sur **Activer** pour les licences que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="78281-150">Switch the toggle to the **On** position for the licenses that you want the selected users to have.</span></span>\
    <span data-ttu-id="78281-151">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-151">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="78281-152">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-152">You can limit which services are available to the users.</span></span> <span data-ttu-id="78281-153">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-153">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="78281-154">Dans la partie inférieure du volet **Ajouter aux produits existants**, sélectionnez **Ajouter** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-154">At the bottom of the **Add to existing products** pane, select **Add** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

## <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="78281-155">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78281-155">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="78281-156">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-156">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-157">Cochez les cases en regard des noms des utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="78281-157">Select the boxes next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="78281-158">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="78281-158">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="78281-159">Dans le volet **Attribuer des produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="78281-159">In the **Assign products** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="78281-160">Positionnez le bouton bascule sur **Activer** pour les licences que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="78281-160">Switch the toggle to the **On** position for the licenses that you want the selected users to have.</span></span>\
    <span data-ttu-id="78281-161">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-161">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="78281-162">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-162">You can limit which services are available to the users.</span></span> <span data-ttu-id="78281-163">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78281-163">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="78281-164">Dans la partie inférieure du volet **Ajouter aux produits existants**, sélectionnez **Ajouter** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-164">At the bottom of the **Add to existing products** pane, select **Add** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

### <a name="assign-licenses-to-one-user"></a><span data-ttu-id="78281-165">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="78281-165">Assign licenses to one user</span></span>

1. <span data-ttu-id="78281-166">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-166">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-167">Sélectionnez la ligne de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="78281-167">Select the row of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="78281-168">Dans le volet de droite, sélectionnez **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="78281-168">In the right pane, select **Licenses and Apps**.</span></span>
4. <span data-ttu-id="78281-169">Développez la section **Licences**, sélectionnez les cases des licences à attribuer, puis choisissez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="78281-169">Expand the **Licenses** section, select the boxes for the licenses that you want to assign, then select **Save changes**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

## <a name="assign-licenses-to-one-user"></a><span data-ttu-id="78281-170">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="78281-170">Assign licenses to one user</span></span>

1. <span data-ttu-id="78281-171">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-171">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-172">Cochez la case en regard du nom de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="78281-172">Select the box next to the name of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="78281-173">Dans le volet de droite, sur la ligne **Licences de produits**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="78281-173">In the right pane, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="78281-174">Dans le volet **Licences de produits**, **activez** le bouton bascule correspondant à la licence que vous voulez attribuer à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-174">In the **Product licenses** pane, switch the toggle to the **On** position for the license that you want to assign to this user.</span></span>\
    <span data-ttu-id="78281-175">Par défaut, tous les services associés à cette licence sont automatiquement attribués à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-175">By default, all services associated with that license are automatically assigned to the user.</span></span> <span data-ttu-id="78281-176">Vous pouvez limiter les services mis à disposition de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-176">You can limit which services are available to the user.</span></span> <span data-ttu-id="78281-177">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-177">Switch the toggles to the **Off** position for the services that you don't want that user to have.</span></span>
5. <span data-ttu-id="78281-178">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-178">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

## <a name="assign-licenses-to-one-user"></a><span data-ttu-id="78281-179">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="78281-179">Assign licenses to one user</span></span>

1. <span data-ttu-id="78281-180">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="78281-180">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="78281-181">Cochez la case en regard du nom de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="78281-181">Select the box next to the name of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="78281-182">Dans le volet de droite, sur la ligne **Licences de produits**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="78281-182">In the right pane, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="78281-183">Dans le volet **Licences de produits**, **activez** le bouton bascule correspondant à la licence que vous voulez attribuer à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-183">In the **Product licenses** pane, switch the toggle to the **On** position for the license that you want to assign to this user.</span></span>\
    <span data-ttu-id="78281-184">Par défaut, tous les services associés à cette licence sont automatiquement attribués à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-184">By default, all services associated with that license are automatically assigned to the user.</span></span> <span data-ttu-id="78281-185">Vous pouvez limiter les services mis à disposition de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-185">You can limit which services are available to the user.</span></span> <span data-ttu-id="78281-186">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78281-186">Switch the toggles to the **Off** position for the services that you don't want that user to have.</span></span>
5. <span data-ttu-id="78281-187">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78281-187">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

## <a name="next-steps"></a><span data-ttu-id="78281-188">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="78281-188">Next steps</span></span>

<span data-ttu-id="78281-189">Si les applications Office ne sont pas encore installées sur vos utilisateurs, vous pouvez partager le[Guide de démarrage rapide d’employées](https://support.microsoft.com/office/b9700090-ce64-4046-ab92-ce8488a7bc0f) avec vos utilisateurs pour configurer des éléments, par [comment télécharger et installer Microsoft 365 ou Office 2019 sur un PC ou Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) et [comment configurer les applications Office et la messagerie électronique sur un appareil mobile](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span><span class="sxs-lookup"><span data-stu-id="78281-189">If your users don't yet have the Office apps installed, you can share the [Employee quick start guide](https://support.microsoft.com/office/b9700090-ce64-4046-ab92-ce8488a7bc0f) with your users to set up things, like [how to download and install Microsoft 365 or Office 2019 on a PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) and [how to set up Office apps and email on a mobile device](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span></span>

## <a name="related-content"></a><span data-ttu-id="78281-190">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="78281-190">Related content</span></span>

<span data-ttu-id="78281-191">[Comprendre les abonnements et les licences](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="78281-191">[Understand subscriptions and licenses](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span></span>\
<span data-ttu-id="78281-192">[Déattribuer des licences aux utilisateurs](remove-licenses-from-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="78281-192">[Unassign licenses from users](remove-licenses-from-users.md) (article)</span></span>\
<span data-ttu-id="78281-193">[Achetez ou supprimez des licences pour votre abonnement](../../commerce/licenses/buy-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="78281-193">[Buy or remove licenses for your subscription](../../commerce/licenses/buy-licenses.md) (article)</span></span>