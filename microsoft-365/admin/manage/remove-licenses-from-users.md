---
title: Annuler l'assignation des licences aux utilisateurs
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
- manage_licenses
- okr_smb
- commerce
search.appverid:
- MET150
description: Découvrez comment désattribuer des licences à des comptes d’utilisateurs.
ms.date: 07/01/2020
ms.openlocfilehash: 550136c2cfa8d81a31e52a4313dc9c967a55d56e
ms.sourcegitcommit: c5d1528559953c6db7dca1d5cb453e0aa3215f02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "51398192"
---
# <a name="unassign-licenses-from-users"></a><span data-ttu-id="d319d-103">Annuler l'assignation des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d319d-103">Unassign licenses from users</span></span>

<span data-ttu-id="d319d-104">Vous pouvez désattribuer des licences à des utilisateurs sur la page **Utilisateurs** actifs ou sur la page **Licences.**</span><span class="sxs-lookup"><span data-stu-id="d319d-104">You can unassign licenses from users on either the **Active users** page, or on the **Licenses** page.</span></span> <span data-ttu-id="d319d-105">La méthode que vous utilisez varie selon que vous souhaitez soit désattribuer des licences de produits à des utilisateurs spécifiques, soit désattribuer des licences d’utilisateurs à partir d’un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="d319d-105">The method you use depends on whether you want to unassign product licenses from specific users or unassign users licenses from a specific product.</span></span>

> [!NOTE]
> <span data-ttu-id="d319d-106">En tant qu’administrateur, vous ne pouvez pas attribuer ou désattribuer des licences pour un abonnement d’achat en libre-service acheté par un utilisateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d319d-106">As an admin, you can't assign or unassign licenses for a self-service purchase subscription bought by a user in your organization.</span></span> <span data-ttu-id="d319d-107">Vous pouvez [prendre le contrôle d’un abonnement d’achat en libre-service,](../../commerce/subscriptions/manage-self-service-purchases-admins.md#take-over-a-self-service-purchase-subscription)puis attribuer ou désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="d319d-107">You can [take over a self-service purchase subscription](../../commerce/subscriptions/manage-self-service-purchases-admins.md#take-over-a-self-service-purchase-subscription), and then assign or unassign licenses.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="d319d-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="d319d-108">Before you begin</span></span>

- <span data-ttu-id="d319d-109">Vous devez être un administrateur global, de licence, d’utilisateur pour désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="d319d-109">You must be a Global, License, User admin to unassign licenses.</span></span> <span data-ttu-id="d319d-110">Si vous souhaitez en savoir plus, consultez l’article [À propos des rôles d’administrateur Microsoft 365](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="d319d-110">For more information, see [About Microsoft 365 admin roles](../add-users/about-admin-roles.md).</span></span>
- <span data-ttu-id="d319d-111">Vous pouvez [supprimer des licences de comptes d'utilisateurs à l'aide d'Office 365 PowerShell](../../enterprise/remove-licenses-from-user-accounts-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="d319d-111">You can [remove licenses from user accounts with Office 365 PowerShell](../../enterprise/remove-licenses-from-user-accounts-with-microsoft-365-powershell.md).</span></span>
- <span data-ttu-id="d319d-112">Vous pouvez également [supprimer les comptes d’utilisateurs](../add-users/delete-a-user.md) qui ont été affectés à une licence afin de les rendre disponibles pour d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d319d-112">You can also [delete user accounts](../add-users/delete-a-user.md) that were assigned a license to make their license available to other users.</span></span> <span data-ttu-id="d319d-113">Lorsque vous supprimez un compte d’utilisateur, sa licence est immédiatement disponible pour une autre personne.</span><span class="sxs-lookup"><span data-stu-id="d319d-113">When you delete a user account, their license is immediately available to assign to someone else.</span></span>

## <a name="use-the-licenses-page-to-unassign-licenses"></a><span data-ttu-id="d319d-114">Utiliser la page Licences pour désattribuer des licences</span><span class="sxs-lookup"><span data-stu-id="d319d-114">Use the Licenses page to unassign licenses</span></span>

<span data-ttu-id="d319d-115">Lorsque vous utilisez la page **Licences** pour désattribuer des licences, vous désattribuez les licences d’un produit spécifique à 20 utilisateurs au plus.</span><span class="sxs-lookup"><span data-stu-id="d319d-115">When you use the **Licenses** page to unassign licenses, you unassign licenses for a specific product for up to 20 users.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="d319d-116">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="d319d-116">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="d319d-117">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration,</a>allez à la page  > **Licences de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-117">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="d319d-118">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration,</a>allez à la page  > **Licences de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-118">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Licenses** page.</span></span>

::: moniker-end

2. <span data-ttu-id="d319d-119">Sélectionnez le produit pour lequel vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="d319d-119">Select the product for which you want to unassign licenses.</span></span>
3. <span data-ttu-id="d319d-120">Sélectionnez les utilisateurs pour lesquels vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="d319d-120">Select the users for which you want to unassign licenses.</span></span>
4. <span data-ttu-id="d319d-121">Sélectionnez **Désattribuer des licences.**</span><span class="sxs-lookup"><span data-stu-id="d319d-121">Select **Unassign licenses**.</span></span>
5. <span data-ttu-id="d319d-122">In the **Unassign licenses** box, select **Unassign**.</span><span class="sxs-lookup"><span data-stu-id="d319d-122">In the **Unassign licenses** box, select **Unassign**.</span></span>

## <a name="use-the-active-users-page-to-unassign-licenses"></a><span data-ttu-id="d319d-123">Utiliser la page Utilisateurs actifs pour désattribuer des licences</span><span class="sxs-lookup"><span data-stu-id="d319d-123">Use the Active users page to unassign licenses</span></span>

<span data-ttu-id="d319d-124">Lorsque vous utilisez la page **Utilisateurs actifs** pour désattribuer des licences, vous désattribuez des licences de produits aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d319d-124">When you use the **Active users** page to unassign licenses, you unassign product licenses from users.</span></span>

### <a name="unassign-licenses-from-one-user"></a><span data-ttu-id="d319d-125">Désattribuer des licences à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="d319d-125">Unassign licenses from one user</span></span>
  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="d319d-126">Dans le Centre d’administration, accédez à la page **Utilisateurs >** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="d319d-126">In the admin center, go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="d319d-127">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">d’administration,</a>allez à la page **Utilisateurs** > **actifs de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-127">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="d319d-128">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">d’administration,</a>allez à la page **Utilisateurs** > **actifs de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-128">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

2. <span data-ttu-id="d319d-129">Sélectionnez la ligne de l’utilisateur pour qui vous souhaitez désattribuer une licence.</span><span class="sxs-lookup"><span data-stu-id="d319d-129">Select the row of the user that you want to unassign a license for.</span></span>
3. <span data-ttu-id="d319d-130">Dans le volet de droite, sélectionnez **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="d319d-130">In the right pane, select **Licenses and Apps**.</span></span>
4. <span data-ttu-id="d319d-131">Développez la section **Licences,** désélectionnez les zones des licences que vous souhaitez désattribuer, puis sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="d319d-131">Expand the **Licenses** section, clear the boxes for the licenses that you want to unassign, then select **Save changes**.</span></span>

###  <a name="unassign-licenses-from-multiple-users"></a><span data-ttu-id="d319d-132">Désattribuer des licences à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d319d-132">Unassign licenses from multiple users</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="d319d-133">Dans le Centre d’administration, accédez à la page **Utilisateurs >** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="d319d-133">In the admin center, go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="d319d-134">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">d’administration,</a>allez à la page **Utilisateurs** > **actifs de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-134">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="d319d-135">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">d’administration,</a>allez à la page **Utilisateurs** > **actifs de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d319d-135">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Active users** page.</span></span>

::: moniker-end

2. <span data-ttu-id="d319d-136">Sélectionnez les cercles en de côté des noms des utilisateurs pour qui vous souhaitez désattribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="d319d-136">Select the circles next to the names of the users that you want to unassign licenses for.</span></span>
3. <span data-ttu-id="d319d-137">Dans la partie supérieure, sélectionnez **Plus d'options (...)**, puis choisissez **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="d319d-137">At the top, select **More options (...)**, then select **Manage product licenses**.</span></span>
4. <span data-ttu-id="d319d-138">Dans le volet **Gérer des licences de produits**, sélectionnez **Remplacer les attributions de licence de produit existantes** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d319d-138">In the **Manage product licenses** pane, select **Replace existing product license assignments** \> **Next**.</span></span>
5. <span data-ttu-id="d319d-139">En bas du  volet Remplacer les produits existants, cochez la case Supprimer toutes les licences de produits des **utilisateurs sélectionnés,** puis **sélectionnez Remplacer** \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="d319d-139">At the bottom of the **Replace existing products** pane, select the **Remove all product licenses from the selected users** check box, then select **Replace** \> **Close**.</span></span>

## <a name="what-happens-to-a-users-data-when-you-remove-their-license"></a><span data-ttu-id="d319d-140">Qu’advient-il des données d’un utilisateur lorsque vous supprimez sa licence ?</span><span class="sxs-lookup"><span data-stu-id="d319d-140">What happens to a user's data when you remove their license?</span></span>

- <span data-ttu-id="d319d-141">Lorsqu’une licence est supprimée d’un utilisateur, les données associées à ce compte sont détenues pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="d319d-141">When a license is removed from a user, data that is associated with that account is held for 30 days.</span></span> <span data-ttu-id="d319d-142">Après la période de grâce de 30 jours, les données sont supprimées et ne peuvent pas être récupérées.</span><span class="sxs-lookup"><span data-stu-id="d319d-142">After the 30-day grace period, the data is deleted and can't be recovered.</span></span>
- <span data-ttu-id="d319d-143">Les fichiers enregistrés dans OneDrive Entreprise ne sont pas supprimés, sauf si l’utilisateur est supprimé du Centre d’administration Microsoft 365 ou supprimé via la synchronisation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d319d-143">Files saved in OneDrive for Business aren't deleted unless the user is deleted from the Microsoft 365 admin center or is removed through Active Directory synchronization.</span></span> <span data-ttu-id="d319d-144">Pour plus d’informations, voir Rétention et [suppression de OneDrive.](/onedrive/retention-and-deletion)</span><span class="sxs-lookup"><span data-stu-id="d319d-144">For more information, see [OneDrive retention and deletion](/onedrive/retention-and-deletion).</span></span>
- <span data-ttu-id="d319d-145">Lorsque la licence est supprimée, la boîte aux lettres de l’utilisateur n’est plus utilisable dans une recherche à l’aide d’un outil eDiscovery tel que la recherche de contenu ou Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d319d-145">When the license is removed, the user's mailbox is no longer searchable by using an eDiscovery tool such as Content Search or Advanced eDiscovery.</span></span> <span data-ttu-id="d319d-146">Pour plus d’informations, voir « Recherche de boîtes aux lettres déconnectées ou déconnectées » dans la recherche de [contenu dans Microsoft 365.](../../compliance/content-search.md#searching-disconnected-or-de-licensed-mailboxes)</span><span class="sxs-lookup"><span data-stu-id="d319d-146">For more information, see "Searching disconnected or de-licensed mailboxes" in [Content Search in Microsoft 365](../../compliance/content-search.md#searching-disconnected-or-de-licensed-mailboxes).</span></span>
- <span data-ttu-id="d319d-147">Si vous avez un abonnement Entreprise, comme Office 365 Entreprise E3, Exchange Online vous permet de conserver les données de boîte aux lettres d’un compte d’utilisateur supprimé à l’aide de boîtes aux lettres [inactives.](../../compliance/inactive-mailboxes-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="d319d-147">If you have an Enterprise subscription, like Office 365 Enterprise E3, Exchange Online lets you preserve the mailbox data of a deleted user account by using [inactive mailboxes](../../compliance/inactive-mailboxes-in-office-365.md).</span></span> <span data-ttu-id="d319d-148">Pour plus d’informations, voir Créer et gérer des boîtes aux lettres [inactives dans Exchange Online.](../../compliance/create-and-manage-inactive-mailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="d319d-148">For more information, see [Create and manage inactive mailboxes in Exchange Online](../../compliance/create-and-manage-inactive-mailboxes.md).</span></span>
- <span data-ttu-id="d319d-149">Pour savoir comment bloquer l’accès d’un utilisateur aux données Microsoft 365 après la suppression de sa licence et comment accéder aux données par la suite, voir Supprimer un ancien [employé.](../add-users/remove-former-employee.md)</span><span class="sxs-lookup"><span data-stu-id="d319d-149">To learn how to block a user's access to Microsoft 365 data after their license is removed, and how to get access to the data afterwards, see [Remove a former employee](../add-users/remove-former-employee.md).</span></span>
- <span data-ttu-id="d319d-150">Si vous supprimez la licence d’un utilisateur et que des applications Office sont toujours [installées,](https://support.microsoft.com/office/0d23d3c0-c19c-4b2f-9845-5344fedc4380) les erreurs d’activation et de produit sans licence s’y sont installées lorsqu’ils utilisent des applications Office.</span><span class="sxs-lookup"><span data-stu-id="d319d-150">If you remove a user's license and they still have Office apps installed, they see [Unlicensed Product and activation errors in Office](https://support.microsoft.com/office/0d23d3c0-c19c-4b2f-9845-5344fedc4380) when they use Office apps.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d319d-151">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="d319d-151">Next steps</span></span>

<span data-ttu-id="d319d-152">Si vous ne comptez pas réattribuer les licences inutilisées à d’autres [utilisateurs,](../../managed-desktop/get-started/assign-licenses.md)envisagez de supprimer les [licences](../../commerce/licenses/buy-licenses.md) de votre abonnement afin de ne pas payer plus de licences que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d319d-152">If you’re not going to [reassign the unused licenses to other users](../../managed-desktop/get-started/assign-licenses.md), consider [removing the licenses from your subscription](../../commerce/licenses/buy-licenses.md) so that you’re not paying for more licenses than you need.</span></span>

## <a name="related-content"></a><span data-ttu-id="d319d-153">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="d319d-153">Related content</span></span>

<span data-ttu-id="d319d-154">[Supprimer des licences de votre abonnement](../../commerce/licenses/buy-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="d319d-154">[Remove licenses from your subscription](../../commerce/licenses/buy-licenses.md) (article)</span></span>\
<span data-ttu-id="d319d-155">[Attribuer des licences aux utilisateurs](assign-licenses-to-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="d319d-155">[Assign licenses to users](assign-licenses-to-users.md) (article)</span></span>\
<span data-ttu-id="d319d-156">[Comprendre les abonnements et les licences dans Microsoft 365 pour les entreprises](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span><span class="sxs-lookup"><span data-stu-id="d319d-156">[Understand subscriptions and licenses in Microsoft 365 for business](../../commerce/licenses/subscriptions-and-licenses.md) (article)</span></span>