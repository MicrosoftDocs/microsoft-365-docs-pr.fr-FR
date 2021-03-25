---
title: Gérer les groupes de rôles dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: Les administrateurs peuvent apprendre à attribuer ou supprimer des autorisations dans le Centre d’administration Exchange (EAC) dans Exchange Online Protection.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 5e712c47d49508934ec7dd2438beff00eb6e1a20
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204522"
---
# <a name="manage-role-groups-in-standalone-eop"></a><span data-ttu-id="fbe89-103">Gérer les groupes de rôles dans une application EOP autonome</span><span class="sxs-lookup"><span data-stu-id="fbe89-103">Manage role groups in standalone EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="fbe89-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fbe89-104">**Applies to**</span></span>
-  [<span data-ttu-id="fbe89-105">Exchange Online Protection autonome</span><span class="sxs-lookup"><span data-stu-id="fbe89-105">Exchange Online Protection standalone</span></span>](exchange-online-protection-overview.md)

<span data-ttu-id="fbe89-106">Dans les organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, vous pouvez utiliser le Centre d’administration Exchange (CAE) pour ajouter des utilisateurs à des groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-106">In standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, you can use the Exchange admin center (EAC) to add users to role groups.</span></span> <span data-ttu-id="fbe89-107">L’ajout d’utilisateurs à un groupe de rôles donne à l’utilisateur l’autorisation d’effectuer des tâches d’administration spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fbe89-107">Adding a users to a role group gives the user permissions to do specific admin tasks.</span></span> <span data-ttu-id="fbe89-108">Vous pouvez également supprimer des utilisateurs de groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-108">You can also remove users from role groups.</span></span>

<span data-ttu-id="fbe89-109">Pour plus d’informations sur les rôles et les groupes de [rôles, voir Autorisations dans EOP autonome.](feature-permissions-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="fbe89-109">For more information about roles and role groups, see [Permissions in standalone EOP](feature-permissions-in-eop.md).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="fbe89-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="fbe89-110">What do you need to know before you begin?</span></span>

- <span data-ttu-id="fbe89-111">Pour ouvrir le Centre d’administration Exchange (CAE), consultez le Centre [d’administration Exchange dans EOP autonome.](exchange-admin-center-in-exchange-online-protection-eop.md)</span><span class="sxs-lookup"><span data-stu-id="fbe89-111">To open the Exchange admin center (EAC), see [Exchange admin center in standalone EOP](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="fbe89-112">Pour ouvrir EOP PowerShell autonome, voir [Se connecter à Exchange Online Protection PowerShell.](/powershell/exchange/connect-to-exchange-online-protection-powershell)</span><span class="sxs-lookup"><span data-stu-id="fbe89-112">To open standalone EOP PowerShell, see [Connect to Exchange Online Protection PowerShell](/powershell/exchange/connect-to-exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="fbe89-113">Des autorisations doivent vous être attribuées dans Exchange Online Protection avant de pouvoir suivre les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="fbe89-113">You need to be assigned permissions in Exchange Online Protection before you can do the procedures in this article.</span></span> <span data-ttu-id="fbe89-114">Plus précisément, vous avez besoin du rôle  **gestion** des rôles, qui est attribué au groupe de rôles Gestion de l’organisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="fbe89-114">Specifically, you need the **Role Management** role, which is assigned to the **Organization Management** role group by default.</span></span> <span data-ttu-id="fbe89-115">Pour plus d’informations, voir [Autorisations](feature-permissions-in-eop.md) dans EOP autonome et utiliser le CAE pour modifier la liste des membres des groupes [de rôles.](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups)</span><span class="sxs-lookup"><span data-stu-id="fbe89-115">For more information, see [Permissions in standalone EOP](feature-permissions-in-eop.md) and [Use the EAC modify the list of members in role groups](manage-admin-role-group-permissions-in-eop.md#use-the-eac-modify-the-list-of-members-in-role-groups).</span></span>

- <span data-ttu-id="fbe89-116">Pour plus d’informations sur les raccourcis clavier qui peuvent s’appliquer aux procédures de cet article, voir raccourcis clavier pour le Centre d’administration [Exchange dans Exchange Online.](/Exchange/accessibility/keyboard-shortcuts-in-admin-center)</span><span class="sxs-lookup"><span data-stu-id="fbe89-116">For information about keyboard shortcuts that may apply to the procedures in this article, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>

> [!TIP]
> <span data-ttu-id="fbe89-117">Vous rencontrez des difficultés ?</span><span class="sxs-lookup"><span data-stu-id="fbe89-117">Having problems?</span></span> <span data-ttu-id="fbe89-118">Demandez de l’aide dans le Forum [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) .</span><span class="sxs-lookup"><span data-stu-id="fbe89-118">Ask for help in the [Exchange Online Protection](https://social.technet.microsoft.com/Forums/forefront/home?forum=FOPE) forum.</span></span>

## <a name="use-the-eac-to-manage-role-groups"></a><span data-ttu-id="fbe89-119">Utiliser le EAC pour gérer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-119">Use the EAC to manage role groups</span></span>

### <a name="use-the-eac-to-view-role-groups"></a><span data-ttu-id="fbe89-120">Utiliser le EAC pour afficher les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-120">Use the EAC to view role groups</span></span>

1. <span data-ttu-id="fbe89-121">Dans le EAC, allez aux **rôles d’administrateur des** \> **autorisations.**</span><span class="sxs-lookup"><span data-stu-id="fbe89-121">In the EAC, go to **Permissions** \> **Admin roles**.</span></span> <span data-ttu-id="fbe89-122">Tous les groupes de rôles de votre organisation sont répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="fbe89-122">All of the role groups in your organization are listed here.</span></span>

2. <span data-ttu-id="fbe89-123">Sélectionnez un groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-123">Select a role group.</span></span> <span data-ttu-id="fbe89-124">Le volet Détails affiche le  **nom,** **la description,** les rôles attribués et géré par **le** groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-124">The Details pane shows the **Name**, **Description**, **Assigned roles**, and **Managed by** of the role group.</span></span> <span data-ttu-id="fbe89-125">Vous pouvez également voir ces informations en cliquant sur **Modifier** ![ l’icône ](../../media/ITPro-EAC-EditIcon.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="fbe89-125">You can also see this information by clicking **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

### <a name="use-the-eac-to-create-role-groups"></a><span data-ttu-id="fbe89-126">Utiliser le EAC pour créer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-126">Use the EAC to create role groups</span></span>

<span data-ttu-id="fbe89-127">Lorsque vous créez un groupe de rôles, vous pouvez configurer tous les paramètres vous-même (lors de la création du groupe ou après).</span><span class="sxs-lookup"><span data-stu-id="fbe89-127">When you create a new role group, you can configure all of the settings yourself (during the creation of the group or after).</span></span> <span data-ttu-id="fbe89-128">Vous pouvez également copier un groupe de rôles existant et le modifier.</span><span class="sxs-lookup"><span data-stu-id="fbe89-128">Or, you can copy an existing role group and modify it.</span></span>

1. <span data-ttu-id="fbe89-129">Dans le EAC, allez à Rôles d’administrateur **des autorisations,** puis faites l’une des \> étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbe89-129">In the EAC, go to **Permissions** \> **Admin roles**, and then do one of the following steps:</span></span>

   - <span data-ttu-id="fbe89-130">**Créer manuellement un nouveau groupe de rôles :** cliquez **sur Ajouter** une ![ icône ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="fbe89-130">**Manually create a new role group**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png).</span></span>

   - <span data-ttu-id="fbe89-131">**Copiez un groupe de rôles existant**: sélectionnez  le groupe de rôles à copier, puis cliquez sur Icône Copier ![ la ](../../media/ITPro-EAC-CopyIcon.png) copie.</span><span class="sxs-lookup"><span data-stu-id="fbe89-131">**Copy an existing role group**: Select the role group that you want to copy and then click **Copy** ![Copy icon](../../media/ITPro-EAC-CopyIcon.png).</span></span>

2. <span data-ttu-id="fbe89-132">Dans la **fenêtre Nouveau groupe de rôles** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="fbe89-132">In the **New role group** window that appears, configure the following settings:</span></span>

    - <span data-ttu-id="fbe89-133">**Nom**: entrez un nom unique pour le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-133">**Name**: Enter a unique name for the role group.</span></span>

    - <span data-ttu-id="fbe89-134">**Description**: entrez une description facultative pour le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-134">**Description**: Enter an optional description for the role group.</span></span>

    - <span data-ttu-id="fbe89-135">**Rôles**: cliquez **sur Icône** Ajouter ou Supprimer pour sélectionner ou modifier les rôles attribués au groupe ![ de ](../../media/ITPro-EAC-AddIcon.png)  ![ ](../../media/ITPro-EAC-RemoveIcon.gif) rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-135">**Roles**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) or **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif) to select or modify the roles that are assigned to the role group.</span></span>

    - <span data-ttu-id="fbe89-136">**Membres :** cliquez sur **Ajouter une icône** ou Supprimer l’icône pour modifier ![ ](../../media/ITPro-EAC-AddIcon.png)  ![ ](../../media/ITPro-EAC-RemoveIcon.gif) l’appartenance au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-136">**Members**: Click **Add** ![Add icon](../../media/ITPro-EAC-AddIcon.png) or **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif) to modify the role group membership.</span></span>

3. <span data-ttu-id="fbe89-137">Lorsque vous avez terminé, cliquez sur **Enregistrer** pour créer le groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-137">When you're finished, click **Save** to create the role group.</span></span>

### <a name="use-the-eac-to-modify-role-groups"></a><span data-ttu-id="fbe89-138">Utiliser le EAC pour modifier des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-138">Use the EAC to modify role groups</span></span>

<span data-ttu-id="fbe89-139">Dans le EAC, sélectionnez les rôles d’administrateur des **autorisations,** sélectionnez le groupe de rôles à modifier, puis cliquez sur Modifier \>   ![ l’icône ](../../media/ITPro-EAC-EditIcon.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="fbe89-139">In the EAC, go to **Permissions** \> **Admin roles**, select the role group you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

<span data-ttu-id="fbe89-140">Les mêmes options sont disponibles lorsque vous modifiez des groupes de rôles que lorsque vous créez des groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-140">The same options are available when you modify role groups as when you create role groups.</span></span> <span data-ttu-id="fbe89-141">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="fbe89-141">You can:</span></span>

- <span data-ttu-id="fbe89-142">Modifiez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="fbe89-142">Change the name and description.</span></span>

- <span data-ttu-id="fbe89-143">Ajouter et supprimer des rôles de gestion (créer ou supprimer des attributions de rôles).</span><span class="sxs-lookup"><span data-stu-id="fbe89-143">Add and remove management roles (create or remove role assignments).</span></span>

- <span data-ttu-id="fbe89-144">Ajouter et supprimer des membres.</span><span class="sxs-lookup"><span data-stu-id="fbe89-144">Add and remove members.</span></span>

<span data-ttu-id="fbe89-145">**Remarque**: certains groupes de rôles (par exemple, Gestion de l’organisation) limitent les rôles que vous pouvez supprimer d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="fbe89-145">**Note**: Some role groups (for example, Organization Management) restrict the roles that you can remove from group.</span></span>

#### <a name="use-the-eac-modify-the-list-of-members-in-role-groups"></a><span data-ttu-id="fbe89-146">Utiliser le EAC pour modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-146">Use the EAC modify the list of members in role groups</span></span>

1. <span data-ttu-id="fbe89-147">Dans le EAC, sélectionnez les rôles d’administrateur des **autorisations,** sélectionnez le groupe de rôles à modifier, puis cliquez sur Modifier \>   ![ l’icône ](../../media/ITPro-EAC-EditIcon.png) Modifier.</span><span class="sxs-lookup"><span data-stu-id="fbe89-147">In the EAC, go to **Permissions** \> **Admin roles**, select the role group that you want to modify, and then click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

2. <span data-ttu-id="fbe89-148">Dans la page des propriétés du groupe de rôles qui s’ouvre, dans la section **Membres,** faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbe89-148">In the role group properties page that opens, in the **Members** section, do either of the following steps:</span></span>

   - <span data-ttu-id="fbe89-149">Cliquez **sur Ajouter** une icône ![ ](../../media/ITPro-EAC-AddIcon.png) .</span><span class="sxs-lookup"><span data-stu-id="fbe89-149">Click **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png).</span></span> <span data-ttu-id="fbe89-150">Dans la page qui s’affiche, recherchez l’utilisateur que wou souhaite ajouter, puis cliquez sur **ajouter ->**.</span><span class="sxs-lookup"><span data-stu-id="fbe89-150">In the page that appears, find the user that wou want to add, and then click **add ->**.</span></span> <span data-ttu-id="fbe89-151">Sélectionnez des utilisateurs **et cliquez sur Ajouter ->** plusieurs fois si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fbe89-151">Select users and click **add ->** many times as necessary.</span></span> <span data-ttu-id="fbe89-152">Lorsque vous avez terminé, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="fbe89-152">When you're finished, click **OK**.</span></span>

   - <span data-ttu-id="fbe89-153">Sélectionnez les utilisateurs à supprimer, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-RemoveIcon.gif) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="fbe89-153">Select the users that you want to remove, and then click **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif).</span></span>

3. <span data-ttu-id="fbe89-154">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fbe89-154">When you're finished, click **Save**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="fbe89-155">Après avoir ajouté ou supprimé des membres dans le groupe de rôles, il est possible que les utilisateurs doivent se déconnecter puis se reconnecter pour que les modifications au niveau de leurs droits d'administration soit appliquées.</span><span class="sxs-lookup"><span data-stu-id="fbe89-155">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span>

### <a name="use-the-eac-to-remove-role-groups"></a><span data-ttu-id="fbe89-156">Utiliser le EAC pour supprimer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-156">Use the EAC to remove role groups</span></span>

<span data-ttu-id="fbe89-157">Vous ne pouvez pas supprimer des groupes de rôles intégrés, mais vous pouvez supprimer des groupes de rôles personnalisés que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="fbe89-157">You can't remove built-in role groups, but you can remove custom role groups that you've created.</span></span>

1. <span data-ttu-id="fbe89-158">Dans le EAC, allez aux **rôles d’administrateur des** \> **autorisations.**</span><span class="sxs-lookup"><span data-stu-id="fbe89-158">In the EAC, go to **Permissions** \> **Admin roles**.</span></span>

2. <span data-ttu-id="fbe89-159">Sélectionnez le groupe de rôles à supprimer, puis cliquez sur **Supprimer** ![ l’icône ](../../media/ITPro-EAC-DeleteIcon.png) Supprimer.</span><span class="sxs-lookup"><span data-stu-id="fbe89-159">Select the role group you want to remove and then click **Delete** ![Delete icon](../../media/ITPro-EAC-DeleteIcon.png).</span></span>

3. <span data-ttu-id="fbe89-160">Cliquez **sur Oui** dans la fenêtre de confirmation qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fbe89-160">Click **Yes** in the confirmation window that appears.</span></span>

## <a name="use-powershell-to-manage-role-groups"></a><span data-ttu-id="fbe89-161">Utiliser PowerShell pour gérer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-161">Use PowerShell to manage role groups</span></span>

### <a name="use-standalone-eop-powershell-to-view-role-groups"></a><span data-ttu-id="fbe89-162">Utiliser EOP PowerShell autonome pour afficher les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-162">Use standalone EOP PowerShell to view role groups</span></span>

<span data-ttu-id="fbe89-163">Pour afficher un groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-163">To view a role group, use the following syntax:</span></span>

```PowerShell
Get-RoleGroup [-Identity "<Role Group Name>"] [-Filter <Filter>]
```

<span data-ttu-id="fbe89-164">Cet exemple renvoie une liste récapitulatif de tous les groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-164">This example returns a summary list of all role groups.</span></span>

```PowerShell
Get-RoleGroup
```

<span data-ttu-id="fbe89-165">Cet exemple renvoie des informations détaillées sur le groupe de rôles nommé Administrateurs des destinataires.</span><span class="sxs-lookup"><span data-stu-id="fbe89-165">This example returns detailed information for the role group named Recipient Administrators.</span></span>

```PowerShell
Get-RoleGroup -Identity "Recipient Administrators" | Format-List
```

<span data-ttu-id="fbe89-166">Cet exemple renvoie tous les groupes de rôles dont l’utilisateur Julia est membre.</span><span class="sxs-lookup"><span data-stu-id="fbe89-166">This example returns all role groups where the user Julia is a member.</span></span> <span data-ttu-id="fbe89-167">Vous devez utiliser la valeur DistinguishedName (DN) pour Julia, que vous pouvez trouver en exécutant la commande : `Get-User -Identity Julia | Format-List DistinguishedName` .</span><span class="sxs-lookup"><span data-stu-id="fbe89-167">You need to use the DistinguishedName (DN) value for Julia, which you can find by running the command: `Get-User -Identity Julia | Format-List DistinguishedName`.</span></span>

```PowerShell
Get-RoleGroup -Filter "Members -eq 'CN=Julia,OU=contoso.onmicrosoft.com,OU=Microsoft Exchange Hosted Organizations,DC=NAMPR001,DC=PROD,DC=OUTLOOK,DC=COM'"
```

<span data-ttu-id="fbe89-168">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-RoleGroup](/powershell/module/exchange/Get-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="fbe89-168">For detailed syntax and parameter information, see [Get-RoleGroup](/powershell/module/exchange/Get-RoleGroup).</span></span>

### <a name="use-standalone-eop-powershell-to-create-role-groups"></a><span data-ttu-id="fbe89-169">Utiliser EOP PowerShell autonome pour créer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-169">Use standalone EOP PowerShell to create role groups</span></span>

<span data-ttu-id="fbe89-170">Lorsque vous créez un groupe de rôles, vous pouvez configurer tous les paramètres manuellement (lors de la création du groupe ou après).</span><span class="sxs-lookup"><span data-stu-id="fbe89-170">When you create a new role group, you can configure all of the settings manually (during the creation of the group or after).</span></span> <span data-ttu-id="fbe89-171">Vous pouvez également copier un groupe de rôles existant et le modifier.</span><span class="sxs-lookup"><span data-stu-id="fbe89-171">Or, you can copy an existing role group and modify it.</span></span>

- <span data-ttu-id="fbe89-172">Pour créer manuellement un groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-172">To manually create a new role group, use the following syntax:</span></span>

  ```PowerShell
  New-RoleGroup -Name "Unique Name" -Description "Descriptive text" -Roles <"Role1","Role2"...>
  ```

  - <span data-ttu-id="fbe89-173">Le _paramètre Roles_ spécifie les rôles de gestion à attribuer au groupe de rôles à l’aide de la syntaxe `"Role1","Role1",..."RoleN"` suivante.</span><span class="sxs-lookup"><span data-stu-id="fbe89-173">The _Roles_ parameter specifies the management roles to assign to the role group by using the following syntax `"Role1","Role1",..."RoleN"`.</span></span> <span data-ttu-id="fbe89-174">Vous pouvez voir les rôles disponibles à l’aide de l’applet de commande **Get-ManagementRole**.</span><span class="sxs-lookup"><span data-stu-id="fbe89-174">You can see the available roles by using the **Get-ManagementRole** cmdlet.</span></span>

  - <span data-ttu-id="fbe89-175">Le _paramètre Members_ spécifie les membres du groupe de rôles à l’aide de la syntaxe suivante : `"Member1","Member2",..."MemberN"` .</span><span class="sxs-lookup"><span data-stu-id="fbe89-175">The _Members_ parameter specifies the members of the role group by using the following syntax: `"Member1","Member2",..."MemberN"`.</span></span> <span data-ttu-id="fbe89-176">Vous pouvez spécifier des utilisateurs, des groupes de sécurité universels à extension messagerie ou d’autres groupes de rôles (entités de sécurité).</span><span class="sxs-lookup"><span data-stu-id="fbe89-176">You can specify users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

  <span data-ttu-id="fbe89-177">Cet exemple crée un groupe de rôles nommé « Limited Recipient Management » avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="fbe89-177">This example creates a new role group named "Limited Recipient Management" with the following settings:</span></span>

  - <span data-ttu-id="fbe89-178">Le rôle Destinataires de message est attribué au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="fbe89-178">The Mail Recipients role is assigned to the role group.</span></span>

  - <span data-ttu-id="fbe89-179">Les utilisateurs Kim et Martin sont ajoutés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="fbe89-179">The users Kim and Martin are added as members.</span></span>

  ```PowerShell
  New-RoleGroup -Name "Limited Recipient Management" -Roles "Mail Recipients" -Members "Kim","Martin"
  ```

- <span data-ttu-id="fbe89-180">Pour copier un groupe de rôles existant, faites les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbe89-180">To copy an existing role group, do the following steps:</span></span>

  1. <span data-ttu-id="fbe89-181">Stockez le groupe de rôles que vous souhaitez copier dans une variable à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-181">Store the role group that you want to copy in a variable using the following syntax:</span></span>

     ```PowerShell
     $RoleGroup = Get-RoleGroup "<Existing Role Group Name>"
     ```

  2. <span data-ttu-id="fbe89-182">Créez le nouveau groupe de rôles à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-182">Create the new role group using the following syntax:</span></span>

     ```PowerShell
     New-RoleGroup -Name "<Unique Name>" -Roles $RoleGroup.Roles [-Members <Members>]
     ```

     <span data-ttu-id="fbe89-183">Le _paramètre Members_ spécifie les membres du groupe de rôles à l’aide de la syntaxe suivante : `"Member1","Member2",..."MemberN"` .</span><span class="sxs-lookup"><span data-stu-id="fbe89-183">The _Members_ parameter specifies the members of the role group by using the following syntax: `"Member1","Member2",..."MemberN"`.</span></span> <span data-ttu-id="fbe89-184">Vous pouvez spécifier des utilisateurs, des groupes de sécurité universels à extension messagerie ou d’autres groupes de rôles (entités de sécurité).</span><span class="sxs-lookup"><span data-stu-id="fbe89-184">You can specify users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

     <span data-ttu-id="fbe89-185">Cet exemple copie le groupe de rôles Gestion de l’organisation dans le nouveau groupe de rôles nommé « Limited Organization Management ».</span><span class="sxs-lookup"><span data-stu-id="fbe89-185">This example copies the Organization Management role group to the new role group named "Limited Organization Management".</span></span> <span data-ttu-id="fbe89-186">Les membres du groupe de rôles sont Isabelle, Carter et Lukas.</span><span class="sxs-lookup"><span data-stu-id="fbe89-186">The role group members are Isabelle, Carter, and Lukas.</span></span>

     ```PowerShell
     $RoleGroup = Get-RoleGroup "Organization Management"
     New-RoleGroup "Limited Organization Management" -Roles $RoleGroup.Roles -Members "Isabelle","Carter","Lukas"
     ```

<span data-ttu-id="fbe89-187">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, [New-RoleGroup](/powershell/module/exchange/New-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="fbe89-187">For detailed syntax and parameter information, [New-RoleGroup](/powershell/module/exchange/New-RoleGroup).</span></span>

### <a name="use-standalone-eop-powershell-modify-the-list-of-members-in-role-groups"></a><span data-ttu-id="fbe89-188">Utiliser EOP PowerShell autonome pour modifier la liste des membres dans les groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-188">Use standalone EOP PowerShell modify the list of members in role groups</span></span>

- <span data-ttu-id="fbe89-189">Les cmdlets **Add-RoleGroupMember** et **Remove-RoleGroupMember** ajoutent ou suppriment des membres individuels un par un.</span><span class="sxs-lookup"><span data-stu-id="fbe89-189">The **Add-RoleGroupMember** and **Remove-RoleGroupMember** cmdlets add or remove individual members one at a time.</span></span> <span data-ttu-id="fbe89-190">La cmdlet **Update-RoleGroupMember** peut remplacer ou modifier la liste de membres existante.</span><span class="sxs-lookup"><span data-stu-id="fbe89-190">The **Update-RoleGroupMember** cmdlet can replace or modify the existing list of members.</span></span>

- <span data-ttu-id="fbe89-191">Les membres d’un groupe de rôles peuvent être des utilisateurs, des groupes de sécurité universels à messagerie ou d’autres groupes de rôles (principaux de sécurité).</span><span class="sxs-lookup"><span data-stu-id="fbe89-191">The members of a role group can be users, mail-enabled universal security groups (USGs), or other role groups (security principals).</span></span>

<span data-ttu-id="fbe89-192">Pour modifier les membres d’un groupe de rôles, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-192">To modify the members of a role group, use the following syntax:</span></span>

```PowerShell
Update-RoleGroupMember -Identity "<Role Group Name>" -Members <Members>
```

- <span data-ttu-id="fbe89-193">Pour _remplacer_ la liste existante des membres par les valeurs que vous spécifiez, utilisez la syntaxe suivante `"Member1","Member2",..."MemberN"` :</span><span class="sxs-lookup"><span data-stu-id="fbe89-193">To _replace_ the existing list of members with the values you specify, use the following syntax: `"Member1","Member2",..."MemberN"`.</span></span>

- <span data-ttu-id="fbe89-194">Pour _modifier de manière sélective_ la liste existante des membres, utilisez la syntaxe suivante : `@{Add="Member1","Member2"...; Remove="Member3","Member4"...}` .</span><span class="sxs-lookup"><span data-stu-id="fbe89-194">To _selectively modify_ the existing list of members, use the following syntax: `@{Add="Member1","Member2"...; Remove="Member3","Member4"...}`.</span></span>

<span data-ttu-id="fbe89-195">Cet exemple remplace tous les membres actuels du groupe de rôles Help Desk par les utilisateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fbe89-195">This example replaces all current members of the Help Desk role group with the specified users.</span></span>

```PowerShell
Update-RoleGroupMember -Identity "Help Desk" -Members "Gabriela Laureano","Hyun-Ae Rim","Jacob Berger"
```

<span data-ttu-id="fbe89-196">Cet exemple ajoute Legoro Akai et supprime Valeria Barrio de la liste des membres du groupe de rôles Help Desk.</span><span class="sxs-lookup"><span data-stu-id="fbe89-196">This example adds Daigoro Akai and removes Valeria Barrio from the list of members on the Help Desk role group.</span></span>

```PowerShell
Update-RoleGroupMember -Identity "Help Desk" -Members @{Add="Daigoro Akai"; Remove="Valeria Barrios"}
```

<span data-ttu-id="fbe89-197">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Update-RoleGroupMember](/powershell/module/exchange/Update-RoleGroupMember).</span><span class="sxs-lookup"><span data-stu-id="fbe89-197">For detailed syntax and parameter information, see [Update-RoleGroupMember](/powershell/module/exchange/Update-RoleGroupMember).</span></span>

### <a name="use-standalone-eop-powershell-to-remove-role-groups"></a><span data-ttu-id="fbe89-198">Utiliser EOP PowerShell autonome pour supprimer des groupes de rôles</span><span class="sxs-lookup"><span data-stu-id="fbe89-198">Use standalone EOP PowerShell to remove role groups</span></span>

<span data-ttu-id="fbe89-199">Vous ne pouvez pas supprimer des groupes de rôles intégrés, mais vous pouvez supprimer des groupes de rôles personnalisés que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="fbe89-199">You can't remove built-in role groups, but you can remove custom role groups that you've created.</span></span>

<span data-ttu-id="fbe89-200">Pour supprimer un groupe de rôles personnalisé, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="fbe89-200">To remove a custom role group, use the following syntax:</span></span>

```PowerShell
Remove-RoleGroup -Identity "<Role Group Name>" [-BypassSecurityGroupManagerCheck]
```

<span data-ttu-id="fbe89-201">Cet exemple supprime le groupe de rôles Administrateurs de formation.</span><span class="sxs-lookup"><span data-stu-id="fbe89-201">This example removes the Training Administrators role group.</span></span>

```PowerShell
Remove-RoleGroup -Identity "Training Administrators"
```

<span data-ttu-id="fbe89-202">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Remove-RoleGroup](/powershell/module/exchange/Remove-RoleGroup).</span><span class="sxs-lookup"><span data-stu-id="fbe89-202">For detailed syntax and parameter information, see [Remove-RoleGroup](/powershell/module/exchange/Remove-RoleGroup).</span></span>

### <a name="how-do-you-know-these-procedures-worked"></a><span data-ttu-id="fbe89-203">Comment savoir si ces procédures ont fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="fbe89-203">How do you know these procedures worked?</span></span>

<span data-ttu-id="fbe89-204">Pour vérifier que vous avez correctement copié un groupe de rôles, faites l’une des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbe89-204">To verify that you've successfully copied a role group, do either of the following steps:</span></span>

- <span data-ttu-id="fbe89-205">Dans le EAC, allez à Rôles d’administrateur des **autorisations** et vérifiez que le groupe de rôles est répertorié \> (ou non répertorié).</span><span class="sxs-lookup"><span data-stu-id="fbe89-205">In the EAC, go to **Permissions** \> **Admin roles**, and verify the role group is listed (or not listed).</span></span> <span data-ttu-id="fbe89-206">Sélectionnez le groupe de rôles et vérifiez les  paramètres dans le volet Détails ou cliquez sur Modifier l’icône ![ modifier pour vérifier les ](../../media/ITPro-EAC-EditIcon.png) paramètres.</span><span class="sxs-lookup"><span data-stu-id="fbe89-206">Select the role group, and verify the settings in the Details pane or click **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png) to verify the settings.</span></span>

- <span data-ttu-id="fbe89-207">Dans Exchange Online PowerShell, remplacez par le nom du groupe de rôles, puis exécutez la commande suivante pour vérifier que le groupe de rôles existe (ou n’existe pas) et vérifier les \<Role Group Name\> paramètres :</span><span class="sxs-lookup"><span data-stu-id="fbe89-207">In Exchange Online PowerShell, replace \<Role Group Name\> with the name of the role group, and run the following command to verify the role group exists (or doesn't exist) and verify the settings:</span></span>

    ```PowerShell
    Get-RoleGroup -Identity "<Role Group Name>" | Format-List
    ```