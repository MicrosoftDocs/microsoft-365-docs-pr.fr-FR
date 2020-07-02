---
title: Résoudre les conflits de licence
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
ms.assetid: 796f7eda-b1f8-479a-adee-bd9226ca47ec
description: Découvrez comment résoudre les conflits de licences avec votre abonnement Microsoft 365 pour les entreprises.
ms.openlocfilehash: 2270fd3ad831ec0ad92ac4eddec5f08a1d07f8be
ms.sourcegitcommit: 0650da0e54a2b484a3156b3aabe44397fbb38e00
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "45015970"
---
# <a name="resolve-license-conflicts"></a><span data-ttu-id="5c703-103">Résoudre les conflits de licence</span><span class="sxs-lookup"><span data-stu-id="5c703-103">Resolve license conflicts</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="5c703-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="5c703-104">The admin center is changing.</span></span> <span data-ttu-id="5c703-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="5c703-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="5c703-106">Nous vous recommandons d’acheter les licences dont vous avez besoin pour votre abonnement avant de créer de nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="5c703-106">We recommend that you buy the licenses that you need for your subscription before you create new users.</span></span> <span data-ttu-id="5c703-107">De cette manière, une licence peut être attribuée à chaque nouvel utilisateur lors de la création d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5c703-107">That way, a license can be assigned to new users as user accounts are created.</span></span> <span data-ttu-id="5c703-108">Si vous avez déjà attribué toutes vos licences aux utilisateurs, mais que certaines licences ont expiré, ou vous essayez de supprimer une licence déjà attribuée à un utilisateur, vous rencontrerez un conflit de licence.</span><span class="sxs-lookup"><span data-stu-id="5c703-108">If you have already assigned all of your licenses to users, but some of the licenses have expired, or you try to remove a license that is already assigned to a user, you will have license conflicts.</span></span> <span data-ttu-id="5c703-109">Pour plus d’informations, consultez [la rubrique supprimer des licences de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="5c703-109">For more information, see [Remove licenses from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>
  
## <a name="how-do-i-view-license-conflicts"></a><span data-ttu-id="5c703-110">Comment afficher les conflits de licence ?</span><span class="sxs-lookup"><span data-stu-id="5c703-110">How do I view license conflicts?</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="5c703-111">Dans le centre d’administration, accédez à **Billing** la > page <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de facturation.</span><span class="sxs-lookup"><span data-stu-id="5c703-111">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="5c703-112">Dans le centre d’administration, accédez à **Billing** la > page <a href="https://go.microsoft.com/fwlink/p/?linkid=848038" target="_blank">licences</a> de facturation.</span><span class="sxs-lookup"><span data-stu-id="5c703-112">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=848038" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="5c703-113">Dans le centre d’administration, accédez à **Billing** la > page <a href="https://go.microsoft.com/fwlink/p/?linkid=850625" target="_blank">licences</a> de facturation.</span><span class="sxs-lookup"><span data-stu-id="5c703-113">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=850625" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

2. <span data-ttu-id="5c703-114">Vérifiez la colonne **État** pour obtenir des informations sur le conflit.</span><span class="sxs-lookup"><span data-stu-id="5c703-114">Check the **Status** column for information about the conflict.</span></span> <span data-ttu-id="5c703-115">En cas de conflit, un message d’avertissement s’affiche, indiquant qu’un ou plusieurs utilisateurs ont besoin d’une licence valide.</span><span class="sxs-lookup"><span data-stu-id="5c703-115">If there's a conflict, you'll see a warning message, that says one or more users need a valid license.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c703-116">La colonne **État** ne s'affiche qu'en cas de conflit.</span><span class="sxs-lookup"><span data-stu-id="5c703-116">You won't see the **Status** column if there are no conflicts.</span></span>

## <a name="how-do-i-resolve-license-conflicts"></a><span data-ttu-id="5c703-117">Comment résoudre les conflits de licence ?</span><span class="sxs-lookup"><span data-stu-id="5c703-117">How do I resolve license conflicts?</span></span>

<span data-ttu-id="5c703-118">Vous pouvez résoudre les conflits de licence en [achetant davantage de licences](../../commerce/licenses/buy-licenses.md) ou en [supprimant les licences des utilisateurs qui n’en ont plus besoin](remove-licenses-from-users.md).</span><span class="sxs-lookup"><span data-stu-id="5c703-118">You can resolve license conflicts by either [buying more licenses](../../commerce/licenses/buy-licenses.md) or by [removing licenses from users who no longer need them](remove-licenses-from-users.md).</span></span> <span data-ttu-id="5c703-119">Vous pouvez aussi [supprimer un compte d'utilisateur pour libérer une licence](../add-users/delete-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="5c703-119">You can optionally [delete a user account to free a license](../add-users/delete-a-user.md).</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="5c703-120">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="5c703-120">Related articles</span></span>

[<span data-ttu-id="5c703-121">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5c703-121">Assign licenses to users</span></span>](assign-licenses-to-users.md)
  
[<span data-ttu-id="5c703-122">Retirer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="5c703-122">Remove licenses from users</span></span>](remove-licenses-from-users.md)
