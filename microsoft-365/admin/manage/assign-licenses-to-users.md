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
ms.date: 08/14/2020
ms.openlocfilehash: e1f28107f7774fa4eccbecb3882cbd002a6eea1a
ms.sourcegitcommit: 919b5d0f33b41b4beaca5fbb06e1c75d65027b7e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2020
ms.locfileid: "46757556"
---
# <a name="assign-licenses-to-users"></a><span data-ttu-id="f08ba-103">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f08ba-103">Assign licenses to users</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="f08ba-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="f08ba-104">The admin center is changing.</span></span> <span data-ttu-id="f08ba-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="f08ba-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

<span data-ttu-id="f08ba-106">Vous pouvez attribuer des licences à des utilisateurs à partir de la page des **Utilisateurs actifs** ou de la page des **Licences**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-106">You can assign licenses to users on either the **Active users** page, or on the **Licenses** page.</span></span> <span data-ttu-id="f08ba-107">La méthode utilisée dépend de votre souhait d’attribuer des licences de produit à des utilisateurs déterminés ou d’attribuer des licences aux utilisateurs pour un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="f08ba-107">The method you use depends on whether you want to assign product licenses to specific users or assign users licenses to a specific product.</span></span>

::: moniker-end

<span data-ttu-id="f08ba-108">[Découvrez comment ajouter un utilisateur et attribuer une licence en même temps](../add-users/add-users.md).</span><span class="sxs-lookup"><span data-stu-id="f08ba-108">[Learn how to add a user and assign a license at the same time](../add-users/add-users.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f08ba-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f08ba-109">Before you begin</span></span>

- <span data-ttu-id="f08ba-110">Vous devez être un administrateur général, une licence ou un administrateur d’utilisateur pour attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="f08ba-110">You must be a Global, License, or User admin to assign licenses.</span></span> <span data-ttu-id="f08ba-111">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f08ba-111">For more information, see [About Microsoft 365 admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="f08ba-112">Vous pouvez [attribuer des licences à des comptes utilisateurs avec Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?linkid=850410).</span><span class="sxs-lookup"><span data-stu-id="f08ba-112">You can [assign licenses to user accounts with Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?linkid=850410).</span></span>
- <span data-ttu-id="f08ba-113">Pour utiliser la gestion des licences basée sur les groupes, voir [Attribuer des licences aux utilisateurs par appartenance aux groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="f08ba-113">To use group-based licensing, see [Assign licenses to users by group membership in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span></span>
- <span data-ttu-id="f08ba-114">Certains services, tels que Sway, sont automatiquement attribués aux utilisateurs et n’ont donc pas besoin d’être attribués individuellement.</span><span class="sxs-lookup"><span data-stu-id="f08ba-114">Some services, like Sway, are automatically assigned to users, and don't need to be assigned individually.</span></span>

::: moniker range="o365-worldwide"

## <a name="use-the-licenses-page-to-assign-licenses-to-users"></a><span data-ttu-id="f08ba-115">Utiliser la page licences pour attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f08ba-115">Use the Licenses page to assign licenses to users</span></span>

<span data-ttu-id="f08ba-116">Lorsque vous utilisez la page **Licences** pour l'attribution de licences, vous attribuez des licences pour un produit spécifique à un maximum de 20 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-116">When you use the **Licenses** page to assign licenses, you assign licenses for a specific product to up to 20 users.</span></span> <span data-ttu-id="f08ba-117">Dans la page **Licences**, une liste de tous les produits auxquels vous avez des abonnements s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f08ba-117">On the **Licenses** page, you see a list of all the products that you have subscriptions for.</span></span> <span data-ttu-id="f08ba-118">Vous pouvez également voir le nombre total de licences pour chaque produit, le nombre de licences attribuées et le nombre de licences disponibles.</span><span class="sxs-lookup"><span data-stu-id="f08ba-118">You also see the total number of licenses for each product, how many licenses are assigned, and how many are available.</span></span>

1. <span data-ttu-id="f08ba-119">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-119">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="f08ba-120">Sélectionnez un produit.</span><span class="sxs-lookup"><span data-stu-id="f08ba-120">Select a product.</span></span>
3. <span data-ttu-id="f08ba-121">Dans la page Détails du produit, sélectionnez **attribuer des licences**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-121">On the product details page, select **Assign licenses**.</span></span>
4. <span data-ttu-id="f08ba-122">Dans le volet **Attribuer des licences aux utilisateurs**, commencez à saisir un nom, puis sélectionnez-le dans les résultats pour l’ajouter à la liste.</span><span class="sxs-lookup"><span data-stu-id="f08ba-122">In the **Assign licenses to users** pane, begin typing a name, and then choose it from the results to add it to the list.</span></span> <span data-ttu-id="f08ba-123">Vous pouvez ajouter jusqu'à 20 utilisateurs à la fois.</span><span class="sxs-lookup"><span data-stu-id="f08ba-123">You can add up to 20 users at a time.</span></span>
5. <span data-ttu-id="f08ba-124">Sélectionnez **Activer ou désactiver les applications et les services** pour attribuer ou supprimer l’accès à des éléments particuliers.</span><span class="sxs-lookup"><span data-stu-id="f08ba-124">Select **Turn apps and services on or off** to assign or remove access to specific items.</span></span>
6. <span data-ttu-id="f08ba-125">Lorsque vous avez terminé, sélectionnez **Attribuer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-125">When you're finished, select **Assign**, then select **Close**.</span></span>

<span data-ttu-id="f08ba-126">S’il existe un conflit, un message s’affiche, vous indiquant la nature du problème et comment le résoudre.</span><span class="sxs-lookup"><span data-stu-id="f08ba-126">If there's a conflict, a message displays, tells you what the problem is, and tells you how to fix it.</span></span> <span data-ttu-id="f08ba-127">Par exemple, si vous avez sélectionné des licences contenant des services en conflit, le message d’erreur indique de vérifier les services inclus dans chaque licence et de réessayer.</span><span class="sxs-lookup"><span data-stu-id="f08ba-127">For example, if you selected licenses that contain conflicting services, the error message says to review the services included with each license and try again.</span></span>

## <a name="change-the-apps-and-services-a-user-has-access-to"></a><span data-ttu-id="f08ba-128">Modifier les applications et les services auxquels un utilisateur a accès</span><span class="sxs-lookup"><span data-stu-id="f08ba-128">Change the apps and services a user has access to</span></span>

1. <span data-ttu-id="f08ba-129">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-129">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="f08ba-130">Dans la page **Licences**, sélectionnez la ligne d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f08ba-130">On the **Licenses** page, select the row for a specific user.</span></span>
3. <span data-ttu-id="f08ba-131">Dans le volet droit, sélectionnez ou désélectionnez les applications et services auxquels vous voulez octroyer ou supprimer l'accès.</span><span class="sxs-lookup"><span data-stu-id="f08ba-131">In the right pane, select or deselect the apps and services that you want to give access to or remove access from.</span></span>
4. <span data-ttu-id="f08ba-132">Une fois terminé, sélectionnez **Enregistrer**, puis choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-132">When you're finished, select **Save**, then select **Close**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

## <a name="use-the-active-users-page-to-assign-licenses"></a><span data-ttu-id="f08ba-133">Utiliser la page utilisateurs actifs pour attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="f08ba-133">Use the Active users page to assign licenses</span></span>

<span data-ttu-id="f08ba-134">Lorsque vous utilisez la page **Utilisateurs actifs** pour attribuer des licences, vous attribuez des licences aux produits pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-134">When you use the **Active users** page to assign licenses, you assign users licenses to products.</span></span>

### <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="f08ba-135">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f08ba-135">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="f08ba-136">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-136">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-137">Sélectionnez les cercles en regard des noms d'utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="f08ba-137">Select the circles next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="f08ba-138">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-138">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="f08ba-139">Dans le volet **Attribuer des licences de produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-139">In the **Manage product licenses** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="f08ba-140">Dans le volet **Ajouter aux produits existants**, positionnez le bouton bascule sur **Actif**correspondant à la licence que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f08ba-140">In the **Add to existing products** pane, switch the toggle to the **On** position for the license that you want the selected users to have.</span></span>\
    <span data-ttu-id="f08ba-141">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-141">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="f08ba-142">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-142">You can limit which services are available to the users.</span></span> <span data-ttu-id="f08ba-143">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-143">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="f08ba-144">Dans la partie inférieure du volet, sélectionnez **Ajouter** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-144">At the bottom of the pane, select **Add** \> **Close**.</span></span>  

::: moniker-end

::: moniker range="o365-germany"

## <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="f08ba-145">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f08ba-145">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="f08ba-146">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-146">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-147">Cochez les cases en regard des noms des utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="f08ba-147">Select the boxes next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="f08ba-148">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-148">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="f08ba-149">Dans le volet **Attribuer des produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-149">In the **Assign products** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="f08ba-150">Positionnez le bouton bascule sur **Activer** pour les licences que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f08ba-150">Switch the toggle to the **On** position for the licenses that you want the selected users to have.</span></span>\
    <span data-ttu-id="f08ba-151">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-151">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="f08ba-152">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-152">You can limit which services are available to the users.</span></span> <span data-ttu-id="f08ba-153">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-153">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="f08ba-154">Dans la partie inférieure du volet **Ajouter aux produits existants**, sélectionnez **Ajouter** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-154">At the bottom of the **Add to existing products** pane, select **Add** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

## <a name="assign-licenses-to-multiple-users"></a><span data-ttu-id="f08ba-155">Attribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f08ba-155">Assign licenses to multiple users</span></span>

1. <span data-ttu-id="f08ba-156">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-156">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-157">Cochez les cases en regard des noms des utilisateurs auxquels vous voulez attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="f08ba-157">Select the boxes next to the names of the users that you want to assign licenses to.</span></span>
3. <span data-ttu-id="f08ba-158">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-158">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="f08ba-159">Dans le volet **Attribuer des produits**, sélectionnez **Ajouter aux attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-159">In the **Assign products** pane, select **Add to existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="f08ba-160">Positionnez le bouton bascule sur **Activer** pour les licences que vous voulez attribuer aux utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f08ba-160">Switch the toggle to the **On** position for the licenses that you want the selected users to have.</span></span>\
    <span data-ttu-id="f08ba-161">Par défaut, tous les services associés à ces licences sont automatiquement attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-161">By default, all services associated with those licenses are automatically assigned to the users.</span></span> <span data-ttu-id="f08ba-162">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-162">You can limit which services are available to the users.</span></span> <span data-ttu-id="f08ba-163">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f08ba-163">Switch the toggles to the **Off** position for the services that you don't want the users to have.</span></span>
6. <span data-ttu-id="f08ba-164">Dans la partie inférieure du volet **Ajouter aux produits existants**, sélectionnez **Ajouter** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-164">At the bottom of the **Add to existing products** pane, select **Add** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

### <a name="assign-licenses-to-one-user"></a><span data-ttu-id="f08ba-165">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f08ba-165">Assign licenses to one user</span></span>

1. <span data-ttu-id="f08ba-166">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-166">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-167">Sélectionnez la ligne de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="f08ba-167">Select the row of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="f08ba-168">Dans le volet de droite, sélectionnez **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-168">In the right pane, select **Licenses and Apps**.</span></span>
4. <span data-ttu-id="f08ba-169">Développez la section **Licences**, sélectionnez les cases des licences à attribuer, puis choisissez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-169">Expand the **Licenses** section, select the boxes for the licenses that you want to assign, then select **Save changes**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

## <a name="assign-licenses-to-one-user"></a><span data-ttu-id="f08ba-170">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f08ba-170">Assign licenses to one user</span></span>

1. <span data-ttu-id="f08ba-171">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-171">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-172">Cochez la case en regard du nom de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="f08ba-172">Select the box next to the name of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="f08ba-173">Dans le volet de droite, sur la ligne **Licences de produits**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-173">In the right pane, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="f08ba-174">Dans le volet **Licences de produits**, **activez** le bouton bascule correspondant à la licence que vous voulez attribuer à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-174">In the **Product licenses** pane, switch the toggle to the **On** position for the license that you want to assign to this user.</span></span>\
    <span data-ttu-id="f08ba-175">Par défaut, tous les services associés à cette licence sont automatiquement attribués à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-175">By default, all services associated with that license are automatically assigned to the user.</span></span> <span data-ttu-id="f08ba-176">Vous pouvez limiter les services mis à disposition de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-176">You can limit which services are available to the user.</span></span> <span data-ttu-id="f08ba-177">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-177">Switch the toggles to the **Off** position for the services that you don't want that user to have.</span></span>
5. <span data-ttu-id="f08ba-178">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-178">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

## <a name="assign-licenses-to-one-user"></a><span data-ttu-id="f08ba-179">Attribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="f08ba-179">Assign licenses to one user</span></span>

1. <span data-ttu-id="f08ba-180">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="f08ba-180">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="f08ba-181">Cochez la case en regard du nom de l’utilisateur auquel vous voulez attribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="f08ba-181">Select the box next to the name of the user that you want to assign a license to.</span></span>
3. <span data-ttu-id="f08ba-182">Dans le volet de droite, sur la ligne **Licences de produits**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-182">In the right pane, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="f08ba-183">Dans le volet **Licences de produits**, **activez** le bouton bascule correspondant à la licence que vous voulez attribuer à cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-183">In the **Product licenses** pane, switch the toggle to the **On** position for the license that you want to assign to this user.</span></span>\
    <span data-ttu-id="f08ba-184">Par défaut, tous les services associés à cette licence sont automatiquement attribués à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-184">By default, all services associated with that license are automatically assigned to the user.</span></span> <span data-ttu-id="f08ba-185">Vous pouvez limiter les services mis à disposition de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-185">You can limit which services are available to the user.</span></span> <span data-ttu-id="f08ba-186">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f08ba-186">Switch the toggles to the **Off** position for the services that you don't want that user to have.</span></span>
5. <span data-ttu-id="f08ba-187">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-187">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

## <a name="assign-a-license-to-a-guest-user"></a><span data-ttu-id="f08ba-188">Attribuer une licence à un utilisateur invité</span><span class="sxs-lookup"><span data-stu-id="f08ba-188">Assign a license to a guest user</span></span>

<span data-ttu-id="f08ba-189">Vous pouvez inviter des utilisateurs invités à collaborer avec votre organisation dans le Centre d’administration Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f08ba-189">You can invite guest users to collaborate with your organization in Azure Active directory admin center.</span></span> <span data-ttu-id="f08ba-190">Pour en savoir plus sur l’estimation des utilisateurs, consultez[Qu’est-ce que l’accès utilisateur invité dans Azure Active Directory B2B ?](https://docs.microsoft.com/azure/active-directory/external-identities/what-is-b2b)</span><span class="sxs-lookup"><span data-stu-id="f08ba-190">To learn about guess users, see [What is guest user access in Azure Active Directory B2B?](https://docs.microsoft.com/azure/active-directory/external-identities/what-is-b2b)</span></span> <span data-ttu-id="f08ba-191">Si vous n’avez pas d’utilisateurs invités, consultez [Démarrage rapide : ajouter des utilisateurs invités à votre annuaire dans le portail Azure](https://docs.microsoft.com/azure/active-directory/external-identities/b2b-quickstart-add-guest-users-portal).</span><span class="sxs-lookup"><span data-stu-id="f08ba-191">If you don't have any guest users, see [Quickstart: Add guest users to your directory in the Azure portal](https://docs.microsoft.com/azure/active-directory/external-identities/b2b-quickstart-add-guest-users-portal).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f08ba-192">Vous devez être un administrateur général pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="f08ba-192">You must be a Global admin to do these steps.</span></span>

1. <span data-ttu-id="f08ba-193">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2067268" target="_blank">Centre d’administration Azure Active Directory</a></span><span class="sxs-lookup"><span data-stu-id="f08ba-193">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2067268" target="_blank">Azure Active Directory admin center</a></span></span>
2. <span data-ttu-id="f08ba-194">Dans le volet de navigation, sélectionnez **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-194">In the navigation pane, select **Users**.</span></span>
3. <span data-ttu-id="f08ba-195">Dans la page **utilisateurs | Tous les utilisateurs (aperçu)**, sélectionnez **Ajouter des filtres**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-195">On the **Users | All Users (Preview)** page, select **Add filters**.</span></span>
4. <span data-ttu-id="f08ba-196">Dans le menu **Sélectionner un champ** , sélectionnez **Type d’utilisateur**, puis **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-196">In the **Pick a field** menu, choose **User type**, then select **Apply**.</span></span>
5. <span data-ttu-id="f08ba-197">Dans le menu suivant, sélectionnez **Invité**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-197">In the next menu, select **Guest**.</span></span>
6. <span data-ttu-id="f08ba-198">Dans la liste des résultats, sélectionnez l’utilisateur ayant besoin d’une licence.</span><span class="sxs-lookup"><span data-stu-id="f08ba-198">In the list of results, select the user who needs a license.</span></span>
7. <span data-ttu-id="f08ba-199">Sous **Gérer**, sélectionnez **Licences**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-199">Under **Manage**, select **Licenses**.</span></span>
8. <span data-ttu-id="f08ba-200">Sélectionnez **Devoirs**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-200">Select **Assignments**.</span></span>
9. <span data-ttu-id="f08ba-201">Sur la page **Mettre à jour les affectations de licence** , sélectionnez le produit pour lequel vous voulez affecter une licence.</span><span class="sxs-lookup"><span data-stu-id="f08ba-201">On the **Update license assignments** page, select the product you want to assign a license for.</span></span>
10. <span data-ttu-id="f08ba-202">Sur la droite, désactivez les cases à cocher des services auxquels vous ne voulez pas que l’utilisateur invité ait accès.</span><span class="sxs-lookup"><span data-stu-id="f08ba-202">On the right, clear the check boxes for any services you don't want the guest user to have access to.</span></span>
11. <span data-ttu-id="f08ba-203">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f08ba-203">Select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f08ba-204">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f08ba-204">Next steps</span></span>

<span data-ttu-id="f08ba-205">Si les applications Office ne sont pas encore installées sur vos utilisateurs, vous pouvez partager le[Guide de démarrage rapide d’employées](https://support.microsoft.com/office/b9700090-ce64-4046-ab92-ce8488a7bc0f) avec vos utilisateurs pour configurer des éléments, par [comment télécharger et installer Microsoft 365 ou Office 2019 sur un PC ou Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) et [comment configurer les applications Office et la messagerie électronique sur un appareil mobile](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span><span class="sxs-lookup"><span data-stu-id="f08ba-205">If your users don't yet have the Office apps installed, you can share the [Employee quick start guide](https://support.microsoft.com/office/b9700090-ce64-4046-ab92-ce8488a7bc0f) with your users to set up things, like [how to download and install Microsoft 365 or Office 2019 on a PC or Mac](https://support.microsoft.com/office/4414eaaf-0478-48be-9c42-23adc4716658) and [how to set up Office apps and email on a mobile device](https://support.microsoft.com/office/7dabb6cb-0046-40b6-81fe-767e0b1f014f).</span></span>

## <a name="related-content"></a><span data-ttu-id="f08ba-206">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="f08ba-206">Related content</span></span>

<span data-ttu-id="f08ba-207">[Comprendre les abonnements et les licences](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="f08ba-207">[Understand subscriptions and licenses](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span></span>\
<span data-ttu-id="f08ba-208">[Déattribuer des licences aux utilisateurs](remove-licenses-from-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="f08ba-208">[Unassign licenses from users](remove-licenses-from-users.md) (article)</span></span>\
<span data-ttu-id="f08ba-209">[Achetez ou supprimez des licences pour votre abonnement](../../commerce/licenses/buy-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="f08ba-209">[Buy or remove licenses for your subscription](../../commerce/licenses/buy-licenses.md) (article)</span></span>