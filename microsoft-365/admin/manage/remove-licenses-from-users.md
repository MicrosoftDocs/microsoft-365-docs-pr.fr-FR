---
title: Annuler l'assignation des licences aux utilisateurs
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
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
description: Découvrez comment désattribuer des licences à des comptes d’utilisateurs.
ms.date: 07/01/2020
ms.openlocfilehash: 6fb07883fdfd4f4a837890e3e8c4c04b2411772b
ms.sourcegitcommit: 0d709e9ab0d8d56c5fc11a921298f82e40e122c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50114476"
---
# <a name="unassign-licenses-from-users"></a><span data-ttu-id="29960-103">Annuler l'assignation des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="29960-103">Unassign licenses from users</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="29960-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="29960-104">The admin center is changing.</span></span> <span data-ttu-id="29960-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="29960-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

<span data-ttu-id="29960-106">Vous pouvez désattribuer des licences à des utilisateurs sur la page **Utilisateurs** actifs ou sur la page **Licences.**</span><span class="sxs-lookup"><span data-stu-id="29960-106">You can unassign licenses from users on either the **Active users** page, or on the **Licenses** page.</span></span> <span data-ttu-id="29960-107">La méthode que vous utilisez varie selon que vous souhaitez soit désattribuer des licences de produits à des utilisateurs spécifiques, soit désattribuer des licences d’utilisateurs à partir d’un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="29960-107">The method you use depends on whether you want to unassign product licenses from specific users or unassign users licenses from a specific product.</span></span>

::: moniker-end

## <a name="before-you-begin"></a><span data-ttu-id="29960-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="29960-108">Before you begin</span></span>

- <span data-ttu-id="29960-109">Vous devez être un administrateur global, de licence, d’utilisateur pour désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="29960-109">You must be a Global, License, User admin to unassign licenses.</span></span> <span data-ttu-id="29960-110">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="29960-110">For more information, see [About Microsoft 365 admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="29960-111">Vous pouvez [supprimer des licences de comptes d'utilisateurs à l'aide d'Office 365 PowerShell](https://docs.microsoft.com/microsoft-365/enterprise/remove-licenses-from-user-accounts-with-microsoft-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="29960-111">You can [remove licenses from user accounts with Office 365 PowerShell](https://docs.microsoft.com/microsoft-365/enterprise/remove-licenses-from-user-accounts-with-microsoft-365-powershell).</span></span>
- <span data-ttu-id="29960-112">Vous pouvez également [supprimer les comptes d’utilisateurs](../add-users/delete-a-user.md) qui ont été affectés à une licence pour les rendre disponibles pour d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="29960-112">You can also [delete user accounts](../add-users/delete-a-user.md) that were assigned a license to make their license available to other users.</span></span> <span data-ttu-id="29960-113">Lorsque vous supprimez un compte d’utilisateur, sa licence est immédiatement disponible pour être assignée à une autre personne.</span><span class="sxs-lookup"><span data-stu-id="29960-113">When you delete a user account, their license is immediately available to assign to someone else.</span></span>

::: moniker range="o365-worldwide"

## <a name="use-the-licenses-page-to-unassign-licenses"></a><span data-ttu-id="29960-114">Utiliser la page Licences pour désattribuer des licences</span><span class="sxs-lookup"><span data-stu-id="29960-114">Use the Licenses page to unassign licenses</span></span>

<span data-ttu-id="29960-115">Lorsque vous utilisez la page **Licences** pour désattribuer des licences, vous désattribuez les licences d’un produit spécifique à 20 utilisateurs au plus.</span><span class="sxs-lookup"><span data-stu-id="29960-115">When you use the **Licenses** page to unassign licenses, you unassign licenses for a specific product for up to 20 users.</span></span>

1. <span data-ttu-id="29960-116">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-116">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>
2. <span data-ttu-id="29960-117">Sélectionnez le produit pour lequel vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="29960-117">Select the product for which you want to unassign licenses.</span></span>
3. <span data-ttu-id="29960-118">Sélectionnez les utilisateurs pour lesquels vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="29960-118">Select the users for which you want to unassign licenses.</span></span>
4. <span data-ttu-id="29960-119">Sélectionnez **Désattribuer des licences.**</span><span class="sxs-lookup"><span data-stu-id="29960-119">Select **Unassign licenses**.</span></span>
5. <span data-ttu-id="29960-120">In the **Unassign licenses** box, select **Unassign**.</span><span class="sxs-lookup"><span data-stu-id="29960-120">In the **Unassign licenses** box, select **Unassign**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

## <a name="use-the-active-users-page-to-unassign-licenses"></a><span data-ttu-id="29960-121">Utiliser la page Utilisateurs actifs pour désattribuer des licences</span><span class="sxs-lookup"><span data-stu-id="29960-121">Use the Active users page to unassign licenses</span></span>

<span data-ttu-id="29960-122">Lorsque vous utilisez la page **Utilisateurs actifs** pour désattribuer des licences, vous désattribuez des licences de produits aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="29960-122">When you use the **Active users** page to unassign licenses, you unassign product licenses from users.</span></span>

### <a name="unassign-licenses-from-one-user"></a><span data-ttu-id="29960-123">Désattribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="29960-123">Unassign licenses from one user</span></span>
  
1. <span data-ttu-id="29960-124">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-124">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-125">Sélectionnez la ligne de l’utilisateur pour qui vous souhaitez désattribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="29960-125">Select the row of the user that you want to unassign a license for.</span></span>
3. <span data-ttu-id="29960-126">Dans le volet de droite, sélectionnez **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="29960-126">In the right pane, select **Licenses and Apps**.</span></span>
4. <span data-ttu-id="29960-127">Développez la section **Licences,** désélectionnez les zones des licences que vous souhaitez désattribuer, puis sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="29960-127">Expand the **Licenses** section, clear the boxes for the licenses that you want to unassign, then select **Save changes**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

## <a name="unassign-licenses-from-one-user"></a><span data-ttu-id="29960-128">Désattribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="29960-128">Unassign licenses from one user</span></span>

1. <span data-ttu-id="29960-129">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-129">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-130">Sélectionnez l’utilisateur pour qui vous souhaitez désattribuer la licence.</span><span class="sxs-lookup"><span data-stu-id="29960-130">Pick the user that you want to unassign the license for.</span></span>
3. <span data-ttu-id="29960-131">Sur la droite, dans la ligne **Licences de produits,** sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="29960-131">On the right, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="29960-132">Dans le **volet Licences de** produits, basculez vers la **position** d’arrêt de la licence que vous souhaitez désattribuer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29960-132">In the **Product licenses** pane, switch the toggle to the **Off** position for the license you want to unassign for the user.</span></span> <span data-ttu-id="29960-133">Par exemple, si vous désaffectez la licence Office 365 Entreprise E3, elle désattribue cette licence et tous les services sous cette licence pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29960-133">For example, if you switch off the Office 365 Enterprise E3 license, it unassigns that license and all services under that license for that user.</span></span>
5. <span data-ttu-id="29960-134">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="29960-134">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

## <a name="unassign-licenses-from-one-user"></a><span data-ttu-id="29960-135">Désattribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="29960-135">Unassign licenses from one user</span></span>

1. <span data-ttu-id="29960-136">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-136">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-137">Sélectionnez l’utilisateur pour qui vous souhaitez désattribuer la licence.</span><span class="sxs-lookup"><span data-stu-id="29960-137">Pick the user that you want to unassign the license for.</span></span>
3. <span data-ttu-id="29960-138">Sur la droite, dans la ligne **Licences de produits,** sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="29960-138">On the right, in the **Product licenses** row, select **Edit**.</span></span>
4. <span data-ttu-id="29960-139">Dans le **volet Licences de** produits, basculez vers la **position** d’arrêt de la licence que vous souhaitez désattribuer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29960-139">In the **Product licenses** pane, switch the toggle to the **Off** position for the license you want to unassign for the user.</span></span> <span data-ttu-id="29960-140">Par exemple, si vous désaffectez la licence Office 365 Entreprise E3, elle désattribue cette licence et tous les services sous cette licence pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29960-140">For example, if you switch off the Office 365 Enterprise E3 license, it unassigns that license and all services under that license for that user.</span></span>
5. <span data-ttu-id="29960-141">En bas du volet **Licences de produits**, sélectionnez **Enregistrer** \> **Fermer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="29960-141">At the bottom of the **Product licenses** pane, select **Save** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"
###  <a name="unassign-licenses-from-multiple-users"></a><span data-ttu-id="29960-142">Désattribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="29960-142">Unassign licenses from multiple users</span></span>

1. <span data-ttu-id="29960-143">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-143">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-144">Sélectionnez les cercles en de côté des noms des utilisateurs pour qui vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="29960-144">Select the circles next to the names of the users that you want to unassign licenses for.</span></span>
3. <span data-ttu-id="29960-145">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="29960-145">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="29960-146">Dans le volet **Gérer des licences de produits**, sélectionnez **Remplacer les attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="29960-146">In the **Manage product licenses** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="29960-147">En bas du  volet Remplacer les produits existants, cochez la case Supprimer toutes les licences de produits des **utilisateurs sélectionnés,** puis **sélectionnez Remplacer** \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="29960-147">At the bottom of the **Replace existing products** pane, select the **Remove all product licenses from the selected users** check box, then select **Replace** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

##  <a name="unassign-licenses-from-multiple-users"></a><span data-ttu-id="29960-148">Désattribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="29960-148">Unassign licenses from multiple users</span></span>

1. <span data-ttu-id="29960-149">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-149">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-150">Sélectionnez les cases en de côté des noms des utilisateurs pour qui vous souhaitez désattribuer toutes les licences.</span><span class="sxs-lookup"><span data-stu-id="29960-150">Select the boxes next to the names of the users that you want to unassign all licenses for.</span></span>
3. <span data-ttu-id="29960-151">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="29960-151">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="29960-152">Dans le volet **Remplacer les produits existants**, sélectionnez **Remplacer les attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="29960-152">In the **Replace existing products** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="29960-153">En bas du  volet Remplacer les produits **existants,** cochez la case Supprimer toutes les licences de produits de la case utilisateur sélectionnée, puis **sélectionnez** Remplacer \>  \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="29960-153">At the bottom of the **Replace existing products** pane, select the **Remove all product licenses from the selected users** check box, then select **Replace** \> **Close** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

##  <a name="unassign-licenses-from-multiple-users"></a><span data-ttu-id="29960-154">Désattribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="29960-154">Unassign licenses from multiple users</span></span>
  
1. <span data-ttu-id="29960-155">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="29960-155">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
2. <span data-ttu-id="29960-156">Sélectionnez les cases en de côté des noms des utilisateurs pour qui vous souhaitez désattribuer toutes les licences.</span><span class="sxs-lookup"><span data-stu-id="29960-156">Select the boxes next to the names of the users that you want to unassign all licenses for.</span></span>
3. <span data-ttu-id="29960-157">Dans le volet **Actions en bloc**, sélectionnez **Modifier les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="29960-157">In the **Bulk actions** pane, select **Edit product licenses**.</span></span>
4. <span data-ttu-id="29960-158">Dans le volet **Remplacer les produits existants**, sélectionnez **Remplacer les attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="29960-158">In the **Replace existing products** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="29960-159">En bas du  volet Remplacer les produits **existants,** cochez la case Supprimer toutes les licences de produits de la case utilisateur sélectionnée, puis **sélectionnez** Remplacer \>  \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="29960-159">At the bottom of the **Replace existing products** pane, select the **Remove all product licenses from the selected users** check box, then select **Replace** \> **Close** \> **Close**.</span></span>

::: moniker-end

## <a name="what-happens-to-a-users-data-when-you-remove-their-license"></a><span data-ttu-id="29960-160">Qu’advient-il des données d’un utilisateur lorsque vous supprimez sa licence ?</span><span class="sxs-lookup"><span data-stu-id="29960-160">What happens to a user's data when you remove their license?</span></span>

- <span data-ttu-id="29960-161">Lorsqu’une licence est supprimée d’un utilisateur, les données associées à ce compte sont détenues pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="29960-161">When a license is removed from a user, data that is associated with that account is held for 30 days.</span></span> <span data-ttu-id="29960-162">Après la période de grâce de 30 jours, les données sont supprimées et ne peuvent pas être récupérées.</span><span class="sxs-lookup"><span data-stu-id="29960-162">After the 30-day grace period, the data is deleted and can't be recovered.</span></span>
- <span data-ttu-id="29960-163">Les fichiers enregistrés dans OneDrive Entreprise ne sont pas supprimés, sauf si l’utilisateur est supprimé du Centre d’administration Microsoft 365 ou supprimé via la synchronisation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="29960-163">Files saved in OneDrive for Business aren't deleted unless the user is deleted from the Microsoft 365 admin center or is removed through Active Directory synchronization.</span></span> <span data-ttu-id="29960-164">Pour plus d’informations, voir Rétention et [suppression de OneDrive.](https://docs.microsoft.com/onedrive/retention-and-deletion)</span><span class="sxs-lookup"><span data-stu-id="29960-164">For more information, see [OneDrive retention and deletion](https://docs.microsoft.com/onedrive/retention-and-deletion).</span></span>
- <span data-ttu-id="29960-165">Lorsque la licence est supprimée, la boîte aux lettres de l’utilisateur n’est plus utilisable dans une recherche à l’aide d’un outil eDiscovery tel que la recherche de contenu ou Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="29960-165">When the license is removed, the user's mailbox is no longer searchable by using an eDiscovery tool such as Content Search or Advanced eDiscovery.</span></span> <span data-ttu-id="29960-166">Pour plus d’informations, voir « Recherche de boîtes aux lettres déconnectées ou déconnectées » dans la recherche de [contenu dans Microsoft 365.](https://docs.microsoft.com/microsoft-365/compliance/content-search#searching-disconnected-or-de-licensed-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="29960-166">For more information, see "Searching disconnected or de-licensed mailboxes" in [Content Search in Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/content-search#searching-disconnected-or-de-licensed-mailboxes).</span></span>
- <span data-ttu-id="29960-167">Si vous avez un abonnement Entreprise, comme Office 365 Entreprise E3, Exchange Online vous permet de conserver les données de boîte aux lettres d’un compte d’utilisateur supprimé à l’aide de boîtes aux lettres [inactives.](https://docs.microsoft.com/microsoft-365/compliance/inactive-mailboxes-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="29960-167">If you have an Enterprise subscription, like Office 365 Enterprise E3, Exchange Online lets you preserve the mailbox data of a deleted user account by using [inactive mailboxes](https://docs.microsoft.com/microsoft-365/compliance/inactive-mailboxes-in-office-365).</span></span> <span data-ttu-id="29960-168">Pour plus d’informations, voir Créer et gérer des boîtes aux lettres [inactives dans Exchange Online.](https://docs.microsoft.com/microsoft-365/compliance/create-and-manage-inactive-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="29960-168">For more information, see [Create and manage inactive mailboxes in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/create-and-manage-inactive-mailboxes).</span></span>
- <span data-ttu-id="29960-169">Pour savoir comment bloquer l’accès d’un utilisateur aux données Microsoft 365 après la suppression de sa licence et comment accéder aux données par la suite, voir Supprimer un ancien [employé.](../add-users/remove-former-employee.md)</span><span class="sxs-lookup"><span data-stu-id="29960-169">To learn how to block a user's access to Microsoft 365 data after their license is removed, and how to get access to the data afterwards, see [Remove a former employee](../add-users/remove-former-employee.md).</span></span>
- <span data-ttu-id="29960-170">Si vous supprimez la licence d’un utilisateur et que des applications Office sont toujours [installées,](https://support.microsoft.com/office/0d23d3c0-c19c-4b2f-9845-5344fedc4380) les erreurs d’activation et de produit sans licence s’y sont installées lorsqu’ils utilisent des applications Office.</span><span class="sxs-lookup"><span data-stu-id="29960-170">If you remove a user's license and they still have Office apps installed, they see [Unlicensed Product and activation errors in Office](https://support.microsoft.com/office/0d23d3c0-c19c-4b2f-9845-5344fedc4380) when they use Office apps.</span></span>

## <a name="next-steps"></a><span data-ttu-id="29960-171">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="29960-171">Next steps</span></span>

<span data-ttu-id="29960-172">Si vous ne comptez pas réattribuer les licences inutilisées à d’autres [utilisateurs,](../../managed-desktop/get-started/assign-licenses.md)envisagez de supprimer les [licences](../../commerce/licenses/buy-licenses.md) de votre abonnement afin de ne pas payer plus de licences que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="29960-172">If you’re not going to [reassign the unused licenses to other users](../../managed-desktop/get-started/assign-licenses.md), consider [removing the licenses from your subscription](../../commerce/licenses/buy-licenses.md) so that you’re not paying for more licenses than you need.</span></span>

## <a name="related-content"></a><span data-ttu-id="29960-173">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="29960-173">Related content</span></span>

<span data-ttu-id="29960-174">[Supprimer des licences de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md) (article)</span><span class="sxs-lookup"><span data-stu-id="29960-174">[Remove licenses from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md) (article)</span></span>\
<span data-ttu-id="29960-175">[Attribuer des licences aux utilisateurs](assign-licenses-to-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="29960-175">[Assign licenses to users](assign-licenses-to-users.md) (article)</span></span>\
<span data-ttu-id="29960-176">[Comprendre les abonnements et les licences dans Microsoft 365 pour les entreprises](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="29960-176">[Understand subscriptions and licenses in Microsoft 365 for business](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span></span>