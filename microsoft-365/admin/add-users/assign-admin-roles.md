---
title: Attribuer des rôles d’administrateur au Microsoft 365'administration centrale
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- okr_smb
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: eac4d046-1afd-4f1a-85fc-8219c79e1504
description: Découvrez comment attribuer des rôles d’administrateur à un ou plusieurs utilisateurs de votre entreprise afin qu’ils peuvent effectuer des tâches spécifiques dans le Centre d’administration.
ms.openlocfilehash: 8a9da12a8ebc01a02e4362f09ccaa9e92c21b7e9
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52634171"
---
# <a name="assign-admin-roles"></a><span data-ttu-id="c28dc-103">Attribuer des rôles d’administrateur</span><span class="sxs-lookup"><span data-stu-id="c28dc-103">Assign admin roles</span></span>

<span data-ttu-id="c28dc-104">Si vous êtes la personne qui a acheté votre abonnement Microsoft Business, vous êtes l’administrateur global. Cela signifie que vous avez un contrôle illimité sur les produits de vos abonnements et que vous pouvez accéder à la plupart des données.</span><span class="sxs-lookup"><span data-stu-id="c28dc-104">If you're the person who purchased your Microsoft business subscription, you are the global admin. This means you have unlimited control over the products in your subscriptions and you can access most data.</span></span>

<span data-ttu-id="c28dc-105">Pour plus d’informations, consultez [À propos des rôles d’administrateur](about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c28dc-105">For more information, see [About admin roles](about-admin-roles.md).</span></span>

<span data-ttu-id="c28dc-106">Lorsque vous ajoutez de nouveaux utilisateurs, si vous ne  leur attribuez pas de rôle d’administrateur, ils sont dans le rôle d’utilisateur et n’ont pas de privilèges d’administrateur sur les centres d’administration Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c28dc-106">When you add new users, if you don't assign them an admin role then they are in the *user role* and don't have admin privileges to any of the Microsoft admin centers.</span></span> <span data-ttu-id="c28dc-107">Toutefois, si vous avez besoin d’aide pour ce faire, vous pouvez attribuer un rôle d’administrateur à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-107">But if you need help getting things done, you can assign an admin role to a user.</span></span> <span data-ttu-id="c28dc-108">Par exemple, si vous avez besoin d’une personne pour réinitialiser les mots de passe, vous ne devez pas lui attribuer le rôle d’administrateur global, vous devez lui attribuer le rôle d’administrateur de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="c28dc-108">For example, if you need someone to help reset passwords, you shouldn't assign them the global admin role, you should assign them the password admin role.</span></span> <span data-ttu-id="c28dc-109">Le fait d’avoir un trop grand nombre d’administrateurs généraux, avec un accès illimité à vos données et à votre entreprise en ligne, constitue un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="c28dc-109">Having too many global admins, with unlimited access to your data and online business, is a security risk.</span></span>

## <a name="watch-add-an-adminbrbr"></a><span data-ttu-id="c28dc-110">Regarder : Ajouter un administrateur</span><span class="sxs-lookup"><span data-stu-id="c28dc-110">Watch: Add an admin</span></span><br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FOfO] 

<span data-ttu-id="c28dc-111">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](../../business-video/index.yml).</span><span class="sxs-lookup"><span data-stu-id="c28dc-111">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](../../business-video/index.yml).</span></span>

## <a name="assign-admin-roles"></a><span data-ttu-id="c28dc-112">Attribuer des rôles d’administrateur</span><span class="sxs-lookup"><span data-stu-id="c28dc-112">Assign admin roles</span></span> 

::: moniker range="o365-worldwide"

<span data-ttu-id="c28dc-113">Vous pouvez affecter des utilisateurs à un rôle de 2 manières différentes :</span><span class="sxs-lookup"><span data-stu-id="c28dc-113">You can assign users to a role in 2 different ways:</span></span>

- <span data-ttu-id="c28dc-114">Vous pouvez obtenir les détails de l’utilisateur et gérer **les rôles** pour lui attribuer un rôle.</span><span class="sxs-lookup"><span data-stu-id="c28dc-114">You can go to the user's details and **Manage roles** to assign a role to the user.</span></span>
- <span data-ttu-id="c28dc-115">Vous pouvez également utiliser **rôles** et sélectionner le rôle, puis y ajouter plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c28dc-115">Or you can go to **Roles** and select the role, and then add multiple users to it.</span></span>

### <a name="assign-admin-roles-to-users-using-roles"></a><span data-ttu-id="c28dc-116">Attribuer des rôles d’administrateur à des utilisateurs à l’aide de rôles</span><span class="sxs-lookup"><span data-stu-id="c28dc-116">Assign admin roles to users using Roles</span></span>

1. <span data-ttu-id="c28dc-117">Dans le Centre d’administration, allez à **Rôles.**</span><span class="sxs-lookup"><span data-stu-id="c28dc-117">In the admin center, go to **Roles**.</span></span> <span data-ttu-id="c28dc-118">Choisissez les **onglets Azure AD** ou **Intune** pour afficher les rôles d’administrateur disponibles pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c28dc-118">Choose the **Azure AD** or **Intune** tabs to view the admin roles available for your organization.</span></span>
2. <span data-ttu-id="c28dc-119">Sélectionnez le rôle d’administrateur à attribuer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-119">Select the admin role that you want to assign the user to.</span></span>
3. <span data-ttu-id="c28dc-120">Sélectionnez **Administrateurs affectés** > **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="c28dc-120">Select **Assigned admins** > **Add**.</span></span>
4. <span data-ttu-id="c28dc-121">Tapez le nom **d’affichage** ou le nom d’utilisateur de l’utilisateur, puis sélectionnez l’utilisateur dans la liste des suggestions.</span><span class="sxs-lookup"><span data-stu-id="c28dc-121">Type the user's **display name** or **username**, and then select the user from the list of suggestions.</span></span>
5. <span data-ttu-id="c28dc-122">Ajoutez plusieurs utilisateurs jusqu’à ce que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="c28dc-122">Add multiple users until you're done.</span></span>
6. <span data-ttu-id="c28dc-123">**Sélectionnez** Enregistrer, puis l’utilisateur est ajouté à la liste des administrateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="c28dc-123">Select **Save**, and then the user will be added to the list of assigned admins.</span></span>

### <a name="assign-a-user-to-an-admin-role-from-active-users"></a><span data-ttu-id="c28dc-124">Attribuer un rôle d’administrateur à un utilisateur via l’option Utilisateurs actifs</span><span class="sxs-lookup"><span data-stu-id="c28dc-124">Assign a user to an admin role from Active users</span></span>

1. <span data-ttu-id="c28dc-125">Dans le Centre d’administration, allez à la page  > [Utilisateurs actifs.](https://go.microsoft.com/fwlink/p/?linkid=834822)</span><span class="sxs-lookup"><span data-stu-id="c28dc-125">In the admin center, go to **Users** > [Active users](https://go.microsoft.com/fwlink/p/?linkid=834822) page.</span></span>

2. <span data-ttu-id="c28dc-126">Dans la page **Utilisateurs** actifs, sélectionnez l’utilisateur dont vous souhaitez modifier le rôle d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-126">On the **Active users** page, select the user whose admin role you want to change.</span></span> <span data-ttu-id="c28dc-127">Dans le volet volant, sous **Rôles,** **sélectionnez Gérer les rôles.**</span><span class="sxs-lookup"><span data-stu-id="c28dc-127">In the flyout pane, under **Roles**, select **Manage roles**.</span></span>

3. <span data-ttu-id="c28dc-128">Sélectionnez le rôle d’administrateur que vous voulez attribuer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-128">Select the admin role that you want to assign to the user.</span></span> <span data-ttu-id="c28dc-129">Si vous ne voyez pas le rôle que vous recherchez, sélectionnez **Afficher tout** en bas de la liste.</span><span class="sxs-lookup"><span data-stu-id="c28dc-129">If you don't see the role you're looking for, select **Show all** at the bottom of the list.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="c28dc-130">Dans le Centre d’administration, accédez à la page **Utilisateurs >** > <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="c28dc-130">In the admin center, go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="c28dc-131">Dans la page **Utilisateurs** actifs, sélectionnez l’utilisateur dont vous souhaitez modifier le rôle d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-131">On the **Active users** page, select the user whose admin role you want to change.</span></span> <span data-ttu-id="c28dc-132">In the flyout pane, next to **Roles**, select **Edit**.</span><span class="sxs-lookup"><span data-stu-id="c28dc-132">In the flyout pane, next to **Roles**, select **Edit**.</span></span> 

    <span data-ttu-id="c28dc-133">Si vous ne voyez  pas l’option Modifier, vous n’êtes pas autorisé à modifier et vous ne pouvez pas attribuer de rôles d’administrateur à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="c28dc-133">If you don't see the **Edit** option, then you don't have a permission to edit and can't assign admin roles to other people.</span></span> <span data-ttu-id="c28dc-134">Demandez à un administrateur global de votre entreprise d’attribuer des rôles à votre place.</span><span class="sxs-lookup"><span data-stu-id="c28dc-134">Ask a global admin in your business to assign roles for you.</span></span> <span data-ttu-id="c28dc-135">Dans une petite entreprise, le propriétaire de l’entreprise (la personne qui a acheté votre abonnement) est un administrateur global. Dans une grande entreprise, les personnes clés du service informatique sont des administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="c28dc-135">In a small business, the business owner (the person who purchased your subscription) is a global admin. In a large business, key people in the IT department are global admins.</span></span>

3. <span data-ttu-id="c28dc-136">Sélectionnez **Administrateur personnalisé** pour voir la liste des rôles que nous avons personnalisés pour vous.</span><span class="sxs-lookup"><span data-stu-id="c28dc-136">Select **Customized administrator** to see a list of roles we've customized for you.</span></span> <span data-ttu-id="c28dc-137">Pour obtenir une description de chaque rôle, voir [à propos des rôles d’administrateur.](about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="c28dc-137">For a description of each role, see [About admin roles.](about-admin-roles.md)</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="c28dc-138">Dans le Centre d’administration, accédez à la page **Utilisateurs >** > <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="c28dc-138">In the admin center, go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="c28dc-139">Dans la page **Utilisateurs** actifs, sélectionnez l’utilisateur dont vous souhaitez modifier le rôle d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c28dc-139">On the **Active users** page, select the user whose admin role you want to change.</span></span> <span data-ttu-id="c28dc-140">In the flyout pane, next to **Roles**, select **Edit**.</span><span class="sxs-lookup"><span data-stu-id="c28dc-140">In the flyout pane, next to **Roles**, select **Edit**.</span></span>

    <span data-ttu-id="c28dc-141">Si vous ne voyez  pas l’option Modifier, vous n’êtes pas autorisé à modifier et vous ne pouvez pas attribuer de rôles d’administrateur à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="c28dc-141">If you don't see the **Edit** option, then you don't have a permission to edit and can't assign admin roles to other people.</span></span> <span data-ttu-id="c28dc-142">Demandez à un administrateur global de votre entreprise d’attribuer des rôles à votre place.</span><span class="sxs-lookup"><span data-stu-id="c28dc-142">Ask a global admin in your business to assign roles for you.</span></span> <span data-ttu-id="c28dc-143">Dans une petite entreprise, le propriétaire de l’entreprise (la personne qui a acheté votre abonnement) est un administrateur global. Dans une grande entreprise, les personnes clés du service informatique sont des administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="c28dc-143">In a small business, the business owner (the person who purchased your subscription) is a global admin. In a large business, key people in the IT department are global admins.</span></span>

3. <span data-ttu-id="c28dc-144">Sélectionnez **Administrateur personnalisé** pour voir la liste des rôles que nous avons personnalisés pour vous.</span><span class="sxs-lookup"><span data-stu-id="c28dc-144">Select **Customized administrator** to see a list of roles we've customized for you.</span></span> <span data-ttu-id="c28dc-145">Pour obtenir une description de chaque rôle, voir [à propos des rôles d’administrateur.](about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="c28dc-145">For a description of each role, see [About admin roles.](about-admin-roles.md)</span></span>

::: moniker-end

## <a name="assign-admin-roles-to-multiple-users"></a><span data-ttu-id="c28dc-146">Attribuer des rôles d'administrateur à plusieurs utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c28dc-146">Assign admin roles to multiple users</span></span>

<span data-ttu-id="c28dc-147">Si vous connaissez PowerShell, voir [Attribuer des rôles aux comptes d’utilisateurs avec PowerShell.](../../enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="c28dc-147">If you know PowerShell, see [Assign roles to user accounts with PowerShell](../../enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell.md).</span></span> <span data-ttu-id="c28dc-148">Cet environnement est idéal pour attribuer des rôles à des centaines d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c28dc-148">It's ideal for assigning roles to hundreds of users.</span></span>
  
<span data-ttu-id="c28dc-149">Utilisez les instructions suivantes pour attribuer des rôles à des dizaines d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c28dc-149">Use the following instructions to assign roles to tens of users.</span></span>

::: moniker range="o365-worldwide"

## <a name="check-admin-roles-in-your-organization"></a><span data-ttu-id="c28dc-150">Vérifier les rôles d’administrateur dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="c28dc-150">Check admin roles in your organization</span></span>

<span data-ttu-id="c28dc-151">Vous n’avez peut-être pas les autorisations correctes pour attribuer des rôles d’administrateur à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c28dc-151">You might not have the correct permissions to assign admin roles to other users.</span></span> <span data-ttu-id="c28dc-152">Vérifiez que vous avez les autorisations correctes ou demandez à un autre administrateur d’attribuer des rôles à votre place.</span><span class="sxs-lookup"><span data-stu-id="c28dc-152">Check to make sure you have the correct permissions or ask another admin to assign roles for you.</span></span>

<span data-ttu-id="c28dc-153">Vous pouvez vérifier les autorisations de rôle d’administrateur de 2 manières différentes :</span><span class="sxs-lookup"><span data-stu-id="c28dc-153">You can check admin role permissions in 2 different ways:</span></span>

- <span data-ttu-id="c28dc-154">Vous pouvez obtenir les détails de l’utilisateur et regarder sous **Rôles** dans la page **Compte.**</span><span class="sxs-lookup"><span data-stu-id="c28dc-154">You can go to the user's details and look under **Roles** on the **Account** page.</span></span>
- <span data-ttu-id="c28dc-155">Vous pouvez également aller à **Rôles** et sélectionner le rôle d’administrateur, puis sélectionner les administrateurs affectés pour voir quels utilisateurs sont affectés.</span><span class="sxs-lookup"><span data-stu-id="c28dc-155">Or you can go to **Roles** and select the admin role, and select assigned admins to see which users are assigned.</span></span>

::: moniker-end

## <a name="related-content"></a><span data-ttu-id="c28dc-156">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="c28dc-156">Related content</span></span>

<span data-ttu-id="c28dc-157">[À propos Microsoft 365 rôles d’administrateur](about-admin-roles.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c28dc-157">[About Microsoft 365 admin roles](about-admin-roles.md) (article)</span></span>\
<span data-ttu-id="c28dc-158">[Autorisations de rôle d’administrateur dans Azure Active Directory](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) (article)</span><span class="sxs-lookup"><span data-stu-id="c28dc-158">[Administrator role permissions in Azure Active Directory](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) (article)</span></span>\
<span data-ttu-id="c28dc-159">[Attribuer des rôles à des comptes d’utilisateur avec PowerShell](../../enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c28dc-159">[Assign roles to user accounts with PowerShell](../../enterprise/assign-roles-to-user-accounts-with-microsoft-365-powershell.md) (article)</span></span>\
<span data-ttu-id="c28dc-160">[Autoriser ou supprimer des relations de partenaires](../misc/add-partner.md) (article)</span><span class="sxs-lookup"><span data-stu-id="c28dc-160">[Authorize or remove partner relationships](../misc/add-partner.md) (article)</span></span>