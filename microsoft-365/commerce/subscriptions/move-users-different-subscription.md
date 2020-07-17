---
title: Transférer des utilisateurs vers un autre abonnement
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_TOC
- commerce
ms.custom:
- AdminSurgePortfolio
- manage_licenses
search.appverid:
- MET150
description: Découvrez comment déplacer des utilisateurs entre des abonnements.
ms.date: 07/01/2020
ms.openlocfilehash: d110ee7c49befa34f5a2cd3bb44dc114aec25b62
ms.sourcegitcommit: 0650da0e54a2b484a3156b3aabe44397fbb38e00
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "45016543"
---
# <a name="move-users-to-a-different-subscription"></a><span data-ttu-id="e5629-103">Transférer des utilisateurs vers un autre abonnement</span><span class="sxs-lookup"><span data-stu-id="e5629-103">Move users to a different subscription</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="e5629-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="e5629-104">The admin center is changing.</span></span> <span data-ttu-id="e5629-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="e5629-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="e5629-106">Si vous avez plusieurs abonnements, que les utilisateurs disposent d’une licence pour un abonnement, mais que vous souhaitez les déplacer vers un autre abonnement, vous pouvez remplacer leur licence existante par une autre.</span><span class="sxs-lookup"><span data-stu-id="e5629-106">If you have more than one subscription, have users with a license for one subscription, but want to move them to another subscription, you can replace their existing license with a different one.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e5629-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e5629-107">Before you begin</span></span>

<span data-ttu-id="e5629-108">Vous devez être un administrateur général, de licence ou d’utilisateur pour attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="e5629-108">You must be a Global, License, or User admin to assign licenses.</span></span> <span data-ttu-id="e5629-109">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e5629-109">For more information, see [About Microsoft 365 admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide).</span></span>

## <a name="move-users-to-a-different-subscription"></a><span data-ttu-id="e5629-110">Transférer des utilisateurs vers un autre abonnement</span><span class="sxs-lookup"><span data-stu-id="e5629-110">Move users to a different subscription</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="e5629-111">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e5629-111">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="e5629-112">Sélectionnez les cercles en regard des noms des utilisateurs pour lesquels vous souhaitez remplacer les licences existantes.</span><span class="sxs-lookup"><span data-stu-id="e5629-112">Select the circles next to the names of the users that you want to replace existing licenses for.</span></span>
3. <span data-ttu-id="e5629-113">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="e5629-113">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="e5629-114">Dans le volet **Gérer des licences de produits**, sélectionnez **Remplacer les attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e5629-114">In the **Manage product licenses** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="e5629-115">Activez **le bouton** bascule pour les licences que vous souhaitez attribuer à ces utilisateurs. </span><span class="sxs-lookup"><span data-stu-id="e5629-115">Switch the toggle to the **On** position for the licenses that you want to assign to these users.</span></span>\
    <span data-ttu-id="e5629-116">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-116">You can limit which services are available to the users.</span></span> <span data-ttu-id="e5629-117">Positionnez le bouton bascule sur **Désactiver** pour les services que vous ne souhaitez pas attribuer à ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-117">Switch the toggles to the **Off** position for the services that you don't want those users to have.</span></span> <span data-ttu-id="e5629-118">Les attributions de licences précédentes sont alors supprimées pour les utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e5629-118">Any previous license assignments for the selected users are removed.</span></span>
6. <span data-ttu-id="e5629-119">En bas du volet **Remplacer les produits existants**, sélectionnez **Remplacer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e5629-119">At the bottom of the **Replace existing products** pane, select **Replace** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="e5629-120">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e5629-120">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="e5629-121">Cochez les cases en regard des noms des utilisateurs pour lesquels vous souhaitez remplacer les licences existantes.</span><span class="sxs-lookup"><span data-stu-id="e5629-121">Select the boxes next to the names of the users you want to replace existing licenses for.</span></span>
3. <span data-ttu-id="e5629-122">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="e5629-122">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="e5629-123">Dans le volet **Attribuer des produits**, sélectionnez **Remplacer des attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e5629-123">In the **Assign products** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="e5629-124">Activez **le bouton** bascule pour les licences que vous souhaitez attribuer à ces utilisateurs. </span><span class="sxs-lookup"><span data-stu-id="e5629-124">Switch the toggle to the **On** position for the licenses that you want to assign to these users.</span></span>\
    <span data-ttu-id="e5629-125">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-125">You can limit which services are available to the users.</span></span> <span data-ttu-id="e5629-126">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-126">Switch the toggles to the **Off** position for the services that you don't want that users to have.</span></span> <span data-ttu-id="e5629-127">Les attributions de licences précédentes sont alors supprimées pour les utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e5629-127">Any previous license assignments for the selected users are removed.</span></span>
6. <span data-ttu-id="e5629-128">Au bas du volet **Remplacer les produits existants**, sélectionnez **Remplacer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e5629-128">At the bottom of the **Replace existing products** pane, select **Replace** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="e5629-129">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e5629-129">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="e5629-130">Cochez les cases en regard des noms des utilisateurs pour lesquels vous souhaitez remplacer les licences existantes.</span><span class="sxs-lookup"><span data-stu-id="e5629-130">Select the boxes next to the names of the users you want to replace existing licenses for.</span></span>
3. <span data-ttu-id="e5629-131">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="e5629-131">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="e5629-132">Dans le volet **Attribuer des produits**, sélectionnez **Remplacer des attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e5629-132">In the **Assign products** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="e5629-133">Activez **le bouton** bascule pour les licences que vous souhaitez attribuer à ces utilisateurs. </span><span class="sxs-lookup"><span data-stu-id="e5629-133">Switch the toggle to the **On** position for the licenses that you want to assign to these users.</span></span>\
    <span data-ttu-id="e5629-134">Vous pouvez limiter les services mis à disposition des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-134">You can limit which services are available to the users.</span></span> <span data-ttu-id="e5629-135">Positionnez le bouton bascule sur **Inactif** pour les services que vous ne souhaitez pas attribuer à ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e5629-135">Switch the toggles to the **Off** position for the services that you don't want that users to have.</span></span> <span data-ttu-id="e5629-136">Les attributions de licences précédentes sont alors supprimées pour les utilisateurs sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e5629-136">Any previous license assignments for the selected users are removed.</span></span>
6. <span data-ttu-id="e5629-137">Au bas du volet **Remplacer les produits existants**, sélectionnez **Remplacer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e5629-137">At the bottom of the **Replace existing products** pane, select **Replace** \> **Close** \> **Close**.</span></span>

::: moniker-end

## <a name="next-steps"></a><span data-ttu-id="e5629-138">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e5629-138">Next steps</span></span>

<span data-ttu-id="e5629-139">Si vous ne souhaitez pas [réaffecter les licences inutilisées à d’autres utilisateurs](../../managed-desktop/get-started/assign-licenses.md), envisagez [de supprimer les licences de votre abonnement](../../commerce/licenses/buy-licenses.md) afin de ne pas payer plus de licences que vous n’en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="e5629-139">If you’re not going to [reassign the unused licenses to other users](../../managed-desktop/get-started/assign-licenses.md), consider [removing the licenses from your subscription](../../commerce/licenses/buy-licenses.md) so that you’re not paying for more licenses than you need.</span></span>

## <a name="related-content"></a><span data-ttu-id="e5629-140">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="e5629-140">Related content</span></span>

<span data-ttu-id="e5629-141">[Attribuer des licences aux utilisateurs](../../admin/manage/assign-licenses-to-users.md) (article) </span><span class="sxs-lookup"><span data-stu-id="e5629-141">[Assign licenses to users](../../admin/manage/assign-licenses-to-users.md) (article)</span></span>\
<span data-ttu-id="e5629-142">[Supprimer des licences de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md) (article) </span><span class="sxs-lookup"><span data-stu-id="e5629-142">[Remove licenses from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md) (article)</span></span>\
<span data-ttu-id="e5629-143">[Modifier les offres manuellement](change-plans-manually.md) (article) </span><span class="sxs-lookup"><span data-stu-id="e5629-143">[Change plans manually](change-plans-manually.md) (article)</span></span>\
<span data-ttu-id="e5629-144">[Comprendre les abonnements et les licences dans Microsoft 365 pour les entreprises](../licenses/subscriptions-and-licenses.md) (article) </span><span class="sxs-lookup"><span data-stu-id="e5629-144">[Understand subscriptions and licenses in Microsoft 365 for business](../licenses/subscriptions-and-licenses.md) (article)</span></span>\
<span data-ttu-id="e5629-145">[Acheter un autre abonnement Microsoft 365 pour les entreprises](../buy-another-subscription.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e5629-145">[Buy another Microsoft 365 for business subscription](../buy-another-subscription.md) (article)</span></span>