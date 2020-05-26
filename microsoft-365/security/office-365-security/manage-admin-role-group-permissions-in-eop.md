---
title: Gérer les groupes de rôles dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Les administrateurs peuvent apprendre à attribuer ou supprimer des autorisations dans le centre d’administration Exchange dans Exchange Online Protection.
ms.openlocfilehash: ba2d053e1e75bd8867ebb9eb7f426cde92abd3e8
ms.sourcegitcommit: 40ec697e27b6c9a78f2b679c6f5a8875dacde943
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2020
ms.locfileid: "44352334"
---
# <a name="manage-role-groups-in-standalone-eop"></a><span data-ttu-id="9eead-103">Gérer les groupes de rôles dans une application EOP autonome</span><span class="sxs-lookup"><span data-stu-id="9eead-103">Manage role groups in standalone EOP</span></span>

<span data-ttu-id="9eead-104">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez utiliser le centre d’administration Exchange pour ajouter des utilisateurs à des groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-104">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can use the Exchange admin center (EAC) to add users to role groups.</span></span> <span data-ttu-id="9eead-105">L’ajout d’un utilisateur à un groupe de rôles donne à l’utilisateur des autorisations pour effectuer des tâches d’administration spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9eead-105">Adding a users to a role group gives the user permissions to do specific admin tasks.</span></span> <span data-ttu-id="9eead-106">Vous pouvez également supprimer des utilisateurs des groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-106">You can also remove users from role groups.</span></span>

<span data-ttu-id="9eead-107">Pour plus d’informations sur les rôles et les groupes de rôles, voir [Permissions in standalone EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="9eead-107">For more information about roles and role groups, see [Permissions in standalone EOP](feature-permissions-in-eop.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="9eead-108">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9eead-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="9eead-109">Pour ouvrir le centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="9eead-109">To open the Exchange admin center (EAC), see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="9eead-110">Pour ouvrir la version PowerShell d’EOP autonome, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="9eead-110">To open standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="9eead-111">Des autorisations doivent vous être attribuées avant de pouvoir exécuter ces procédures.</span><span class="sxs-lookup"><span data-stu-id="9eead-111">You need to be assigned permissions before you can perform these procedures.</span></span> <span data-ttu-id="9eead-112">Plus précisément, vous avez besoin du rôle de gestion des rôles, qui est affecté par défaut au groupe de rôles OrganizationManagement (administrateurs globaux).</span><span class="sxs-lookup"><span data-stu-id="9eead-112">Specifically, you need the Role Management role, which is assigned to the OrganizationManagement (global admins) role group by default.</span></span> <span data-ttu-id="9eead-113">Pour plus d’informations, consultez la rubrique [autorisations dans EOP autonome](feature-permissions-in-eop.md) et utiliser le centre d’administration Exchange pour [modifier la liste des membres dans les groupes de rôles](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span><span class="sxs-lookup"><span data-stu-id="9eead-113">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="9eead-114">Pour plus d’informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir [raccourcis clavier pour le centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="9eead-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="9eead-115">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="9eead-115">Having problems?</span></span> <span data-ttu-id="9eead-116">Demandez de l’aide dans le forum [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) .</span><span class="sxs-lookup"><span data-stu-id="9eead-116">Ask for help in the [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351) forum.</span></span>

## <a name="use-the-eac-to-manage-role-groups"></a><span data-ttu-id="9eead-117">Utiliser le centre d’administration Exchange pour gérer les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-117">Use the EAC to manage role groups</span></span>

### <a name="use-the-eac-to-view-role-groups"></a><span data-ttu-id="9eead-118">Utiliser le centre d’administration Exchange pour afficher les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-118">Use the EAC to view role groups</span></span>

1. <span data-ttu-id="9eead-119">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**.</span><span class="sxs-lookup"><span data-stu-id="9eead-119">In the EAC, go to **Permissions** \> **Admin roles**.</span></span> <span data-ttu-id="9eead-120">Tous les groupes de rôles de votre organisation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="9eead-120">All of the role groups in your organization are listed here.</span></span>

2. <span data-ttu-id="9eead-121">Sélectionnez un groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-121">Select a role group.</span></span> <span data-ttu-id="9eead-122">Le volet d’informations affiche le **nom**, la **Description**, les **rôles attribués**et **gérés par** le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-122">The Details pane shows the **Name**, **Description**, **Assigned roles**, and **Managed by** of the role group.</span></span> <span data-ttu-id="9eead-123">Vous pouvez également afficher ces informations en cliquant sur **modifier** l' ![ icône modifier ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-123">You can also see this information by clicking **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

### <a name="use-the-eac-to-create-role-groups"></a><span data-ttu-id="9eead-124">Utiliser le centre d’administration Exchange pour créer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-124">Use the EAC to create role groups</span></span>

<span data-ttu-id="9eead-125">Lorsque vous créez un nouveau groupe de rôles, vous pouvez configurer tous les paramètres vous-même (lors de la création du groupe ou après).</span><span class="sxs-lookup"><span data-stu-id="9eead-125">When you create a new role group, you can configure all of the settings yourself (during the creation of the group or after).</span></span> <span data-ttu-id="9eead-126">Sinon, vous pouvez copier un groupe de rôles existant et le modifier.</span><span class="sxs-lookup"><span data-stu-id="9eead-126">Or, you can copy an existing role group and modify it.</span></span>

1. <span data-ttu-id="9eead-127">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**, puis effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eead-127">In the EAC, go to **Permissions** \> **Admin roles**, and then do one of the following steps:</span></span>

   - <span data-ttu-id="9eead-128">**Créez manuellement un nouveau groupe de rôles**: cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-128">**Manually create a new role group**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

   - <span data-ttu-id="9eead-129">**Copier un groupe de rôles existant**: sélectionnez le groupe de rôles que vous souhaitez copier, puis cliquez sur icône **copier** ![ ](../../media/ITPro-EAC-CopyIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-129">**Copy an existing role group**: Select the role group that you want to copy and then click **Copy** ![Copy icon](../../media/ITPro-EAC-CopyIcon.png).</span></span>

2. <span data-ttu-id="9eead-130">Dans la fenêtre **nouveau groupe de rôles** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9eead-130">In the **New role group** window that appears, configure the following settings:</span></span>

    - <span data-ttu-id="9eead-131">**Nom**: entrez un nom unique pour le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-131">**Name**: Enter a unique name for the role group.</span></span>

    - <span data-ttu-id="9eead-132">**Description**: entrez une description facultative pour le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-132">**Description**: Enter an optional description for the role group.</span></span>

    - <span data-ttu-id="9eead-133">**Rôles**: cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) ou **supprimer** ![ ITPro-EAC-RemoveIcon. gif ](../../media/ITPro-EAC-RemoveIcon.gif) pour sélectionner ou modifier les rôles attribués au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-133">**Roles**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) or **Remove** ![ITPro-EAC-RemoveIcon.gif](../../media/ITPro-EAC-RemoveIcon.gif) to select or modify the roles that are assigned to the role group.</span></span>

    - <span data-ttu-id="9eead-134">**Membres**: cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) ou **supprimer** ![ ITPro-EAC-RemoveIcon. gif ](../../media/ITPro-EAC-RemoveIcon.gif) pour modifier l’appartenance au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-134">**Members**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) or **Remove** ![ITPro-EAC-RemoveIcon.gif](../../media/ITPro-EAC-RemoveIcon.gif) to modify the role group membership.</span></span>

3. <span data-ttu-id="9eead-135">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-135">When you're finished, click **Save** to create the role group.</span></span>

### <a name="use-the-eac-to-modify-role-groups"></a><span data-ttu-id="9eead-136">Utiliser le centre d’administration Exchange pour modifier des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-136">Use the EAC to modify role groups</span></span>

<span data-ttu-id="9eead-137">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**, sélectionnez le groupe de rôles que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône d’édition ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-137">In the EAC, go to **Permissions** \> **Admin roles**, select the role group you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

<span data-ttu-id="9eead-138">Les mêmes options sont disponibles lorsque vous modifiez des groupes de rôles, comme lorsque vous créez des groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-138">The same options are available when you modify role groups as when you create role groups.</span></span> <span data-ttu-id="9eead-139">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="9eead-139">You can:</span></span>

- <span data-ttu-id="9eead-140">Modifiez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="9eead-140">Change the name and description.</span></span>

- <span data-ttu-id="9eead-141">Ajouter et supprimer des rôles de gestion (créer ou supprimer des attributions de rôles).</span><span class="sxs-lookup"><span data-stu-id="9eead-141">Add and remove management roles (create or remove role assignments).</span></span>

- <span data-ttu-id="9eead-142">Ajouter et supprimer des membres.</span><span class="sxs-lookup"><span data-stu-id="9eead-142">Add and remove members.</span></span>

<span data-ttu-id="9eead-143">**Remarque**: certains groupes de rôles (par exemple, gestion de l’organisation) restreignent les rôles que vous pouvez supprimer du groupe.</span><span class="sxs-lookup"><span data-stu-id="9eead-143">**Note**: Some role groups (for example, Organization Management) restrict the roles that you can remove from group.</span></span>

#### <a name="use-the-eac-modify-the-list-of-members-in-role-groups"></a><span data-ttu-id="9eead-144">Utiliser le centre d’administration Exchange modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-144">Use the EAC modify the list of members in role groups</span></span>

1. <span data-ttu-id="9eead-145">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**, sélectionnez le groupe de rôles que vous souhaitez modifier, puis cliquez sur **modifier** l' ![ icône d’édition ](../../media/ITPro-EAC-EditIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-145">In the EAC, go to **Permissions** \> **Admin roles**, select the role group that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

2. <span data-ttu-id="9eead-146">Dans la page des propriétés du groupe de rôles qui s’ouvre, dans la section **memebers** , effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eead-146">In the role group properties page that opens, in the **Memebers** section, do either of the following steps:</span></span>

   - <span data-ttu-id="9eead-147">Cliquez sur **Ajouter** une ![ icône Ajouter ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-147">Click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="9eead-148">Dans la page qui s’affiche, recherchez l’utilisateur que Wou souhaite ajouter, puis cliquez sur **Ajouter->**.</span><span class="sxs-lookup"><span data-stu-id="9eead-148">In the page that appears, find the user that wou want to add, and then click **add ->**.</span></span> <span data-ttu-id="9eead-149">Sélectionnez utilisateurs, puis cliquez sur **ajouter >** plusieurs fois autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9eead-149">Select users and click **add ->** many times as necessary.</span></span> <span data-ttu-id="9eead-150">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9eead-150">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="9eead-151">Sélectionnez les utilisateurs à supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-RemoveIcon.gif) .</span><span class="sxs-lookup"><span data-stu-id="9eead-151">Select the users that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

3. <span data-ttu-id="9eead-152">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9eead-152">When you're finished, click **Save**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9eead-153">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="9eead-153">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span>

### <a name="use-the-eac-to-remove-role-groups"></a><span data-ttu-id="9eead-154">Utiliser le centre d’administration Exchange pour supprimer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-154">Use the EAC to remove role groups</span></span>

<span data-ttu-id="9eead-155">Vous ne pouvez pas supprimer les groupes de rôles intégrés, mais vous pouvez supprimer les groupes de rôles personnalisés que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="9eead-155">You can't remove built-in role groups, but you can remove custom role groups that you've created.</span></span>

1. <span data-ttu-id="9eead-156">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**.</span><span class="sxs-lookup"><span data-stu-id="9eead-156">In the EAC, go to **Permissions** \> **Admin roles**.</span></span>

2. <span data-ttu-id="9eead-157">Sélectionnez le groupe de rôles que vous souhaitez supprimer, puis cliquez sur **supprimer** l' ![ icône Supprimer ](../../media/ITPro-EAC-DeleteIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="9eead-157">Select the role group you want to remove and then click **Delete** ![Delete icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

3. <span data-ttu-id="9eead-158">Cliquez sur **Oui** dans la fenêtre de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9eead-158">Click **Yes** in the confirmation window that appears.</span></span>

## <a name="use-powershell-to-manage-role-groups"></a><span data-ttu-id="9eead-159">Utiliser PowerShell pour gérer les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-159">Use PowerShell to manage role groups</span></span>

### <a name="use-standalone-eop-powershell-to-view-role-groups"></a><span data-ttu-id="9eead-160">Utilisation d’EOP PowerShell autonome pour afficher des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-160">Use standalone EOP PowerShell to view role groups</span></span>

<span data-ttu-id="9eead-161">Pour afficher un groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-161">To view a role group, use the following syntax:</span></span>

```PowerShell
Get-RoleGroup [-Identity "<Role Group Name>"] [-Filter <Filter>]
```

<span data-ttu-id="9eead-162">Cet exemple renvoie la liste récapitulative de tous les groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-162">This example returns a summary list of all role groups.</span></span>

```PowerShell
Get-RoleGroup
```

<span data-ttu-id="9eead-163">Cet exemple renvoie des informations détaillées sur le groupe de rôles administrateurs des destinataires.</span><span class="sxs-lookup"><span data-stu-id="9eead-163">This example returns detailed information for the role group named Recipient Administrators.</span></span>

```PowerShell
Get-RoleGroup -Identity "Recipient Administrators" | Format-List
```

<span data-ttu-id="9eead-164">Cet exemple renvoie tous les groupes de rôles pour lesquels l’utilisateur Julia est membre.</span><span class="sxs-lookup"><span data-stu-id="9eead-164">This example returns all role groups where the user Julia is a member.</span></span> <span data-ttu-id="9eead-165">Vous devez utiliser la valeur DistinguishedName (DN) pour Julia, que vous pouvez trouver en exécutant la commande : `Get-User -Identity Julia | Format-List DistinguishedName` .</span><span class="sxs-lookup"><span data-stu-id="9eead-165">You need to use the DistinguishedName (DN) value for Julia, which you can find by running the command: `Get-User -Identity Julia | Format-List DistinguishedName`.</span></span>

```PowerShell
Get-RoleGroup -Filter "Members -eq 'CN=Julia,OU=contoso.onmicrosoft.com,OU=Microsoft Exchange Hosted Organizations,DC=NAMPR001,DC=PROD,DC=OUTLOOK,DC=COM'"
```

<span data-ttu-id="9eead-166">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="9eead-166">For detailed syntax and parameter information, see [Get-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/Get-RoleGroup).</span></span>

### <a name="use-standalone-eop-powershell-to-create-role-groups"></a><span data-ttu-id="9eead-167">Utilisation d’EOP PowerShell autonome pour créer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-167">Use standalone EOP PowerShell to create role groups</span></span>

<span data-ttu-id="9eead-168">Lorsque vous créez un nouveau groupe de rôles, vous pouvez configurer tous les paramètres manuellement (lors de la création du groupe ou après).</span><span class="sxs-lookup"><span data-stu-id="9eead-168">When you create a new role group, you can configure all of the settings manually (during the creation of the group or after).</span></span> <span data-ttu-id="9eead-169">Sinon, vous pouvez copier un groupe de rôles existant et le modifier.</span><span class="sxs-lookup"><span data-stu-id="9eead-169">Or, you can copy an existing role group and modify it.</span></span>

- <span data-ttu-id="9eead-170">Pour créer manuellement un nouveau groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-170">To manually create a new role group, use the following syntax:</span></span>

  ```PowerShell
  New-RoleGroup -Name "Unique Name" -Description "Descriptive text" -Roles <"Role1","Role2"...>
  ```

  - <span data-ttu-id="9eead-171">Le paramètre _roles_ spécifie les rôles de gestion à affecter au groupe de rôles à l’aide de la syntaxe suivante `"Role1","Role1",..."RoleN"` .</span><span class="sxs-lookup"><span data-stu-id="9eead-171">The _Roles_ parameter specifies the management roles to assign to the role group by using the following syntax `"Role1","Role1",..."RoleN"`.</span></span> <span data-ttu-id="9eead-172">Vous pouvez voir les rôles disponibles à l’aide de la cmdlet **Get-ManagementRole** .</span><span class="sxs-lookup"><span data-stu-id="9eead-172">You can see the available roles by using the **Get-ManagementRole** cmdlet.</span></span>

  - <span data-ttu-id="9eead-173">Le paramètre _members_ spécifie les membres du groupe de rôles à l’aide de la syntaxe suivante : `"Member1","Member2",..."MemberN"` .</span><span class="sxs-lookup"><span data-stu-id="9eead-173">The _Members_ parameter specifies the members of the role group by using the following syntax: `"Member1","Member2",..."MemberN"`.</span></span> <span data-ttu-id="9eead-174">Vous pouvez spécifier des utilisateurs, des groupes de sécurité universels à extension messagerie (USG) ou d’autres groupes de rôles (principaux de sécurité).</span><span class="sxs-lookup"><span data-stu-id="9eead-174">You can specify users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

  <span data-ttu-id="9eead-175">Cet exemple crée un groupe de rôles nommé « gestion limitée des destinataires » avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9eead-175">This example creates a new role group named "Limited Recipient Management" with the following settings:</span></span>

  - <span data-ttu-id="9eead-176">Le rôle Destinataires de message est attribué au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="9eead-176">The Mail Recipients role is assigned to the role group.</span></span>

  - <span data-ttu-id="9eead-177">Les utilisateurs Kim et Martin sont ajoutés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="9eead-177">The users Kim and Martin are added as members.</span></span>

  ```PowerShell
  New-RoleGroup -Name "Limited Recipient Management" -Roles "Mail Recipients" -Members "Kim","Martin"
  ```

- <span data-ttu-id="9eead-178">Pour copier un groupe de rôles existant, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9eead-178">To copy an existing role group, do the following steps:</span></span>

  1. <span data-ttu-id="9eead-179">Stockez le groupe de rôles que vous souhaitez copier dans une variable à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-179">Store the role group that you want to copy in a variable using the following syntax:</span></span>

     ```PowerShell
     $RoleGroup = Get-RoleGroup "<Existing Role Group Name>"
     ```

  2. <span data-ttu-id="9eead-180">Créez le nouveau groupe de rôles à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-180">Create the new role group using the following syntax:</span></span>

     ```PowerShell
     New-RoleGroup -Name "<Unique Name>" -Roles $RoleGroup.Roles [-Members <Members>]
     ```

     <span data-ttu-id="9eead-181">Le paramètre _members_ spécifie les membres du groupe de rôles à l’aide de la syntaxe suivante : `"Member1","Member2",..."MemberN"` .</span><span class="sxs-lookup"><span data-stu-id="9eead-181">The _Members_ parameter specifies the members of the role group by using the following syntax: `"Member1","Member2",..."MemberN"`.</span></span> <span data-ttu-id="9eead-182">Vous pouvez spécifier des utilisateurs, des groupes de sécurité universels à extension messagerie (USG) ou d’autres groupes de rôles (principaux de sécurité).</span><span class="sxs-lookup"><span data-stu-id="9eead-182">You can specify users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

     <span data-ttu-id="9eead-183">Cet exemple copie le groupe de rôles gestion de l’organisation dans le nouveau groupe de rôles appelé « gestion limitée de l’organisation ».</span><span class="sxs-lookup"><span data-stu-id="9eead-183">This example copies the Organization Management role group to the new role group named "Limited Organization Management".</span></span> <span data-ttu-id="9eead-184">Les membres du groupe de rôles sont Isabelle, Carter et Lukas.</span><span class="sxs-lookup"><span data-stu-id="9eead-184">The role group members are Isabelle, Carter, and Lukas.</span></span>

     ```PowerShell
     $RoleGroup = Get-RoleGroup "Organization Management"
     New-RoleGroup "Limited Organization Management" -Roles $RoleGroup.Roles -Members "Isabelle","Carter","Lukas"
     ```

<span data-ttu-id="9eead-185">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [New-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/New-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="9eead-185">For detailed syntax and parameter information, [New-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/New-RoleGroup).</span></span>

### <a name="use-standalone-eop-powershell-modify-the-list-of-members-in-role-groups"></a><span data-ttu-id="9eead-186">Utiliser l’PowerShell EOP autonome modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-186">Use standalone EOP PowerShell modify the list of members in role groups</span></span>

- <span data-ttu-id="9eead-187">Les applets **de commande Add-RoleGroupMember** et **Remove-RoleGroupMember** ajoutent ou suppriment des membres individuels un par un.</span><span class="sxs-lookup"><span data-stu-id="9eead-187">The **Add-RoleGroupMember** and **Remove-RoleGroupMember** cmdlets add or remove individual members one at a time.</span></span> <span data-ttu-id="9eead-188">L’applet de commande **Update-RoleGroupMember** peut remplacer ou modifier la liste de membres existante.</span><span class="sxs-lookup"><span data-stu-id="9eead-188">The **Update-RoleGroupMember** cmdlet can replace or modify the existing list of members.</span></span>

- <span data-ttu-id="9eead-189">Les membres d’un groupe de rôles peuvent être des utilisateurs, des groupes de sécurité universels à extension messagerie (USG) ou d’autres groupes de rôles (principaux de sécurité).</span><span class="sxs-lookup"><span data-stu-id="9eead-189">The members of a role group can be users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

<span data-ttu-id="9eead-190">Pour modifier les membres d’un groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-190">To modify the members of a role group, use the following syntax:</span></span>

```PowerShell
Update-RoleGroupMember -Identity "<Role Group Name>" -Members <Members>
```

- <span data-ttu-id="9eead-191">Pour _remplacer_ la liste de membres existante par les valeurs que vous spécifiez, utilisez la syntaxe suivante : `"Member1","Member2",..."MemberN"` .</span><span class="sxs-lookup"><span data-stu-id="9eead-191">To _replace_ the existing list of members with the values you specify, use the following syntax: `"Member1","Member2",..."MemberN"`.</span></span>

- <span data-ttu-id="9eead-192">Pour _modifier de manière sélective_ la liste de membres existante, utilisez la syntaxe suivante : `@{Add="Member1","Member2"...; Remove="Member3","Member4"...}` .</span><span class="sxs-lookup"><span data-stu-id="9eead-192">To _selectively modify_ the existing list of members, use the following syntax: `@{Add="Member1","Member2"...; Remove="Member3","Member4"...}`.</span></span>

<span data-ttu-id="9eead-193">Cet exemple remplace tous les membres actuels du groupe de rôles support technique par les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9eead-193">This example replaces all current members of the Help Desk role group with the specified users.</span></span>

```PowerShell
Update-RoleGroupMember -Identity "Help Desk" -Members "Gabriela Laureano","Hyun-Ae Rim","Jacob Berger"
```

<span data-ttu-id="9eead-194">Cet exemple montre comment ajouter Daigoro Akai et supprimer Valeria Barrio de la liste des membres du groupe de rôles support technique.</span><span class="sxs-lookup"><span data-stu-id="9eead-194">This example adds Daigoro Akai and removes Valeria Barrio from the list of members on the Help Desk role group.</span></span>

```PowerShell
Update-RoleGroupMember -Identity "Help Desk" -Members @{Add="Daigoro Akai"; Remove="Valeria Barrios"}
```

<span data-ttu-id="9eead-195">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez la rubrique [Update-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Update-RoleGroupMember).</span><span class="sxs-lookup"><span data-stu-id="9eead-195">For detailed syntax and parameter information, see [Update-RoleGroupMember](https://docs.microsoft.com/powershell/module/exchange/Update-RoleGroupMember).</span></span>

### <a name="use-standalone-eop-powershell-to-remove-role-groups"></a><span data-ttu-id="9eead-196">Utilisation d’EOP PowerShell autonome pour supprimer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="9eead-196">Use standalone EOP PowerShell to remove role groups</span></span>

<span data-ttu-id="9eead-197">Vous ne pouvez pas supprimer les groupes de rôles intégrés, mais vous pouvez supprimer les groupes de rôles personnalisés que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="9eead-197">You can't remove built-in role groups, but you can remove custom role groups that you've created.</span></span>

<span data-ttu-id="9eead-198">Pour supprimer un groupe de rôles personnalisé, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="9eead-198">To remove a custom role group, use the following syntax:</span></span>

```PowerShell
Remove-RoleGroup -Identity "<Role Group Name>" [-BypassSecurityGroupManagerCheck]
```

<span data-ttu-id="9eead-199">Cet exemple supprime le groupe de rôles Administrateurs de formation.</span><span class="sxs-lookup"><span data-stu-id="9eead-199">This example removes the Training Administrators role group.</span></span>

```PowerShell
Remove-RoleGroup -Identity "Training Administrators"
```

<span data-ttu-id="9eead-200">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/Remove-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="9eead-200">For detailed syntax and parameter information, see [Remove-RoleGroup](https://docs.microsoft.com/powershell/module/exchange/Remove-RoleGroup).</span></span>

### <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="9eead-201">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="9eead-201">How do you know these procedures worked?</span></span>

<span data-ttu-id="9eead-202">Pour vérifier que vous avez bien copié un groupe de rôles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9eead-202">To verify that you've successfully copied a role group, do either of the following steps:</span></span>

- <span data-ttu-id="9eead-203">Dans le centre d’administration Exchange, accédez à rôles d’administrateur des **autorisations** \> **Admin roles**et vérifiez que le groupe de rôles est affiché (ou non).</span><span class="sxs-lookup"><span data-stu-id="9eead-203">In the EAC, go to **Permissions** \> **Admin roles**, and verify the role group is listed (or not listed).</span></span> <span data-ttu-id="9eead-204">Sélectionnez le groupe de rôles et vérifiez les paramètres dans le volet d’informations ou cliquez sur **modifier** ![ l’icône modifier ](../../media/ITPro-EAC-EditIcon.png) pour vérifier les paramètres.</span><span class="sxs-lookup"><span data-stu-id="9eead-204">Select the role group, and verify the settings in the Details pane or click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png) to verify the settings.</span></span>

- <span data-ttu-id="9eead-205">Dans Exchange Online PowerShell, remplacez \< nom du groupe \> de rôles par le nom du groupe de rôles, puis exécutez la commande suivante pour vérifier que le groupe de rôles existe (ou n’existe pas) et vérifiez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="9eead-205">In Exchange Online PowerShell, replace \<Role Group Name\> with the name of the role group, and run the following command to verify the role group exists (or doesn't exist) and verify the settings:</span></span>

    ```PowerShell
    Get-RoleGroup -Identity "<Role Group Name>" | Format-List
    ```
