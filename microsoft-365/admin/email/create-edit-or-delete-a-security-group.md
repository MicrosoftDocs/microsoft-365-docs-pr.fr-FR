---
title: Créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration Microsoft 365
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 55c96b32-e086-4c9e-948b-a018b44510cb
description: Apprenez à créer, modifier ou supprimer un groupe de sécurité.
ms.openlocfilehash: 689adb46bdec4d4f669482af6b5467fdcf63482c
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43628878"
---
# <a name="create-edit-or-delete-a-security-group-in-the-microsoft-365-admin-center"></a><span data-ttu-id="4e31d-103">Créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4e31d-103">Create, edit, or delete a security group in the Microsoft 365 admin center</span></span>

<span data-ttu-id="4e31d-104">Sur la page **groupes** Microsoft 365, vous pouvez créer des groupes de comptes d’utilisateur que vous pouvez utiliser pour attribuer les mêmes autorisations à dans SharePoint Online et CRM Online.</span><span class="sxs-lookup"><span data-stu-id="4e31d-104">On the Microsoft 365 **Groups** page, you can create groups of user accounts that you can use to assign the same permissions to in SharePoint Online and CRM Online.</span></span> <span data-ttu-id="4e31d-105">Par exemple, un administrateur peut créer un groupe de sécurité pour accorder à un certain groupe de personnes l’accès à un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4e31d-105">For example, an administrator can create a security group to grant a certain group of people access to a SharePoint site.</span></span> <span data-ttu-id="4e31d-106">Seuls les administrateurs de gestion des utilisateurs et globaux sont autorisés à créer, modifier ou supprimer des groupes de sécurité ; Pour plus d’informations sur les rôles d’administrateur, consultez la rubrique [attribution de rôles](../add-users/assign-admin-roles.md)d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4e31d-106">Only global and user management administrators have permissions to create, edit, or delete security groups; for more information about administrator roles, see [Assigning admin roles](../add-users/assign-admin-roles.md).</span></span> 
  
<span data-ttu-id="4e31d-107">En outre, vous pouvez utiliser des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) pour envoyer du courrier électronique ou affecter des autorisations à un groupe d'utilisateurs, ainsi que des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) qui accordent des droits d'utilisateur et un accès aux sites et aux collections de sites.</span><span class="sxs-lookup"><span data-stu-id="4e31d-107">There are also [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that you can use to send email or assign permissions to a group of users, and [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that grant users rights and access to sites and site collections.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="4e31d-108">Vous prévoyez d'utiliser des boîtes aux lettres de site ?</span><span class="sxs-lookup"><span data-stu-id="4e31d-108">Planning on using site mailboxes?</span></span> <span data-ttu-id="4e31d-109">Tous les utilisateurs ajoutés à un site SharePoint via un groupe de sécurité plutôt qu'individuellement ne peuvent utiliser la boîte aux lettres de site qu'à partir de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4e31d-109">All the users that are added to a SharePoint site via a security group rather than being added individually can use only the site mailbox from SharePoint.</span></span> <span data-ttu-id="4e31d-110">Ils n'auront pas accès à la boîte aux lettres de site à partir d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="4e31d-110">These users won't be able to access the site mailbox from Outlook.</span></span> <span data-ttu-id="4e31d-111">Pour plus d’informations, consultez la rubrique [utiliser des groupes Microsoft 365 à la place des boîtes aux lettres de site](https://support.office.com/article/737d6b1f-67cc-41fe-8db8-f2d09dd1673b.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e31d-111">For more information, see [Use Microsoft 365 groups instead of Site Mailboxes](https://support.office.com/article/737d6b1f-67cc-41fe-8db8-f2d09dd1673b.aspx).</span></span> 
  
## <a name="manage-security-groups-in-the-admin-center"></a><span data-ttu-id="4e31d-112">Gérer les groupes de sécurité dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="4e31d-112">Manage security groups in the admin center</span></span>

### <a name="add-a-security-group"></a><span data-ttu-id="4e31d-113">Ajouter un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="4e31d-113">Add a security group</span></span>

1. <span data-ttu-id="4e31d-114">Dans le centre d’administration Microsoft 365, accédez > à **la page groupes de**<a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="4e31d-114">In the Microsoft 365 admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="4e31d-115">Dans la page **groupes** , sélectionnez **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-115">On the **Groups** page, select **Add a group**.</span></span>
    
3. <span data-ttu-id="4e31d-116">Dans la page **choisir un type de groupe** , choisissez **sécurité**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-116">On the **Choose a group type** page, choose **Security**.</span></span> 
    
4. <span data-ttu-id="4e31d-117">Suivez les étapes pour terminer la création du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-117">Follow the steps to complete creation of the group.</span></span> 
 
### <a name="add-members-to-a-security-group"></a><span data-ttu-id="4e31d-118">Ajouter des membres à un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="4e31d-118">Add members to a security group</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="4e31d-119">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4e31d-119">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>
    
1. <span data-ttu-id="4e31d-120">Sélectionnez le nom du groupe de sécurité sur la page **groupes** , puis sous l’onglet **membres** , sélectionnez **Afficher tout et gérer les membres**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-120">Select the security group name on the **Groups** page, and on the **Members** tab, select **View all and manage members**.</span></span> 
    
2. <span data-ttu-id="4e31d-121">Dans le volet groupe, sélectionnez **Ajouter des membres** , choisissez la personne dans la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de **recherche** , puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-121">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="4e31d-122">Pour supprimer des membres, sélectionnez le X en regard de leur nom.</span><span class="sxs-lookup"><span data-stu-id="4e31d-122">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4e31d-123">Sélectionnez le nom du groupe de sécurité sur la page **groupes** , puis sélectionnez **modifier** en regard de **membres**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-123">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="4e31d-124">Dans le volet groupe, sélectionnez **Ajouter des membres** , choisissez la personne dans la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de **recherche** , puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-124">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="4e31d-125">Pour supprimer des membres, sélectionnez le X en regard de leur nom.</span><span class="sxs-lookup"><span data-stu-id="4e31d-125">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-21vianet"


1. <span data-ttu-id="4e31d-126">Sélectionnez le nom du groupe de sécurité sur la page **groupes** , puis sélectionnez **modifier** en regard de **membres**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-126">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="4e31d-127">Dans le volet groupe, sélectionnez **Ajouter des membres** , choisissez la personne dans la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de **recherche** , puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-127">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="4e31d-128">Pour supprimer des membres, sélectionnez le X en regard de leur nom.</span><span class="sxs-lookup"><span data-stu-id="4e31d-128">To remove members, select the X next to their name.</span></span>

::: moniker-end

### <a name="edit-a-security-group"></a><span data-ttu-id="4e31d-129">Modifier un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="4e31d-129">Edit a security group</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="4e31d-130">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4e31d-130">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="4e31d-131">Dans le centre d’administration, accédez \> à **la page groupes de** <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="4e31d-131">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="4e31d-132">Dans la page **groupes** , sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-132">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="4e31d-133">Dans le volet Paramètres, sélectionnez l’onglet **général** ou l’onglet **membres** pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="4e31d-133">In the settings pane, select the **General** tab or the **Members** tab to edit either group details or members.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4e31d-134">Dans le centre d’administration, accédez \> à **la page groupes de** <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="4e31d-134">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="4e31d-135">Dans la page **groupes** , sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-135">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="4e31d-136">Dans le volet groupe de sécurité, sélectionnez **modifier** en regard de l’onglet **nom** ou **membres** pour modifier les détails ou les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-136">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="4e31d-137">Une fois que vous avez apporté des modifications, sélectionnez **Enregistrer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-137">After you've made changes, select **Save** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4e31d-138">Dans le centre d’administration, accédez \> à **la page groupes de** <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="4e31d-138">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="4e31d-139">Dans la page **groupes** , sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-139">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="4e31d-140">Dans le volet groupe de sécurité, sélectionnez **modifier** en regard de l’onglet **nom** ou **membres** pour modifier les détails ou les membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-140">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="4e31d-141">Une fois que vous avez apporté des modifications, sélectionnez **Enregistrer** > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-141">After you've made changes, select **Save** > **Close**.</span></span>

::: moniker-end


### <a name="delete-a-security-group"></a><span data-ttu-id="4e31d-142">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="4e31d-142">Delete a security group</span></span>

1. <span data-ttu-id="4e31d-143">Dans le centre d’administration, accédez > à **la page groupes de**<a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="4e31d-143">In the admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
    
2. <span data-ttu-id="4e31d-144">Dans la page **groupes** , sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="4e31d-144">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="4e31d-145">Sélectionnez **supprimer un groupe** (wasetbin Icon), puis confirmez-le en sélectionnant **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="4e31d-145">Select **Delete group** (wasetbin icon), and then confirm by selecting **Delete**.</span></span>
    
    <span data-ttu-id="4e31d-146">Sélectionnez **Fermer** une fois le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="4e31d-146">Select **Close** once the group is deleted.</span></span> 
    
## <a name="groups-in-exchange-online-and-sharepoint-online"></a><span data-ttu-id="4e31d-147">Groupes dans Exchange Online et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4e31d-147">Groups in Exchange Online and SharePoint Online</span></span>

<span data-ttu-id="4e31d-148">Si vous souhaitez créer des groupes d’utilisateurs afin de pouvoir leur envoyer des courriers électroniques tous en même temps, vous pouvez le faire dans le centre d’administration Exchange en accédant à **groupes**de **destinataires** \> **Exchange** \> d' **administration** \> .</span><span class="sxs-lookup"><span data-stu-id="4e31d-148">If you want to create groups of users so you can send email to them all at the same time, you can do that in the Exchange admin center by going to **Admin** \> **Exchange** \> **Recipients** \> **Groups**.</span></span> <span data-ttu-id="4e31d-149">Ensuite, sélectionnez **nouveau**![ajouter](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png), puis sélectionnez le type de groupe que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="4e31d-149">Next, select **New**![Add](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png), and select the kind of group you want to create:</span></span> 
  
- <span data-ttu-id="4e31d-150">**Groupe de distribution**: un groupe de distribution permet de distribuer des messages à un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4e31d-150">**Distribution group**: Used to distribute messages to a group of users.</span></span> <span data-ttu-id="4e31d-151">Il est également appelé *groupe de distribution à extension messagerie*, ou liste de *distribution*.</span><span class="sxs-lookup"><span data-stu-id="4e31d-151">It's also called a  *mail-enabled distribution group*, or, a  *distribution list*.</span></span> <span data-ttu-id="4e31d-152">Pour plus d'informations, voir [Gestion des groupes de distribution](https://technet.microsoft.com/library/bb124513.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e31d-152">For more information, see [Manage distribution groups](https://technet.microsoft.com/library/bb124513.aspx).</span></span>
    
- <span data-ttu-id="4e31d-153">**Groupe de sécurité**: un groupe de sécurité permet de distribuer des messages à un groupe d'utilisateurs ou d'accorder des autorisations d'accès à des ressources.</span><span class="sxs-lookup"><span data-stu-id="4e31d-153">**Security group**: Can be used to distribute messages to a group of users, or to grant access permissions to resources.</span></span> <span data-ttu-id="4e31d-154">Ce groupe est également appelé *groupe de sécurité à extension messagerie*.</span><span class="sxs-lookup"><span data-stu-id="4e31d-154">This group is also called a *mail-enabled security group*.</span></span> <span data-ttu-id="4e31d-155">Pour plus d'informations, voir [Gérer les groupes de sécurité à extension de messagerie](https://technet.microsoft.com/library/bb123521.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e31d-155">For more information, see [Manage mail-enabled security groups](https://technet.microsoft.com/library/bb123521.aspx).</span></span>
    
- <span data-ttu-id="4e31d-156">**Groupe de distribution dynamique**: type de groupe de distribution dont la liste de destinataires est recalculée chaque fois que vous envoyez un message en fonction des filtres et des conditions définis par vos soins.</span><span class="sxs-lookup"><span data-stu-id="4e31d-156">**Dynamic distribution group**: A type of distribution group whose list of recipients is recalculated every time you send a message based on filters and conditions that you define.</span></span> <span data-ttu-id="4e31d-157">Pour plus d'informations, reportez-vous à [Gérer des groupes de distribution dynamiques](https://technet.microsoft.com/library/bb123722.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e31d-157">For more information, see [Manage dynamic distribution groups](https://technet.microsoft.com/library/bb123722.aspx).</span></span>
    
<span data-ttu-id="4e31d-158">Après avoir créé des groupes de distribution et des groupes de sécurité à extension messagerie dans le centre d’administration Exchange, leurs noms et leurs listes d’utilisateurs apparaissent dans la page **groupes de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="4e31d-158">After you create distribution groups and mail-enabled security groups in the Exchange admin center, their names and user lists appear on the **Security groups** page.</span></span> <span data-ttu-id="4e31d-159">Vous pouvez supprimer ces groupes aux deux emplacements, mais vous ne pouvez les modifier que dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e31d-159">You can delete these groups in both locations, but you can edit them only in the Exchange admin center.</span></span> <span data-ttu-id="4e31d-160">Les groupes de distribution dynamique n’apparaissent pas dans la page **groupes de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="4e31d-160">Dynamic distribution groups don't show up on the **Security groups** page.</span></span> 
  
 <span data-ttu-id="4e31d-161">Les groupes SharePoint sont générés automatiquement quand vous créez une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="4e31d-161">SharePoint groups are created automatically when you make a site collection.</span></span> <span data-ttu-id="4e31d-162">Les groupes par défaut utilisent les niveaux d'autorisation par défaut dans SharePoint  parfois appelés rôles SharePoint  pour accorder aux utilisateurs des droits et un accès.</span><span class="sxs-lookup"><span data-stu-id="4e31d-162">The default groups use the default permission levels in SharePoint—sometimes called SharePoint roles—to grant users rights and access.</span></span> <span data-ttu-id="4e31d-163">Pour plus d’informations, voir [groupes SharePoint par défaut dans SharePoint Online](https://support.office.com/article/13bb2b6b-dd8c-447e-b71b-0e4bb9efe1d3.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e31d-163">For more information, see [Default SharePoint groups in SharePoint Online](https://support.office.com/article/13bb2b6b-dd8c-447e-b71b-0e4bb9efe1d3.aspx).</span></span>
  
## <a name="how-is-a-security-group-different-from-security-groups-i-create-in-sharepoint"></a><span data-ttu-id="4e31d-164">En quoi un groupe de sécurité est-il différent des groupes de sécurité que j’ai créés dans SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="4e31d-164">How is a security group different from security groups I create in SharePoint?</span></span>

<span data-ttu-id="4e31d-165">Les groupes de sécurité peuvent être utilisés avec SharePoint, Exchange, MDM, Windows et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="4e31d-165">Security groups can be used with SharePoint, Exchange, MDM, Windows, and more.</span></span> <span data-ttu-id="4e31d-166">Un groupe de sécurité que vous créez dans SharePoint n’est reconnu que par cette collection de sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4e31d-166">A security group you create in SharePoint is only recognized by that SharePoint site collection.</span></span>
  
## <a name="do-i-have-to-use-security-groups-for-my-organization-to-be-secure"></a><span data-ttu-id="4e31d-167">Dois-je utiliser les groupes de sécurité de mon organisation pour assurer la sécurité ?</span><span class="sxs-lookup"><span data-stu-id="4e31d-167">Do I have to use security groups for my organization to be secure?</span></span>

<span data-ttu-id="4e31d-168">Non.</span><span class="sxs-lookup"><span data-stu-id="4e31d-168">No.</span></span> <span data-ttu-id="4e31d-169">Il s’agit simplement d’une autre façon de gérer la sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4e31d-169">This is just one more way you can manage security for your organization.</span></span> <span data-ttu-id="4e31d-170">Vous pouvez toujours accorder des autorisations utilisateur et l’accès aux sites individuellement.</span><span class="sxs-lookup"><span data-stu-id="4e31d-170">You can always grant user permissions and access to sites individually.</span></span> <span data-ttu-id="4e31d-171">Toutefois, avec les groupes de sécurité, vous pouvez facilement gérer des groupes d’utilisateurs plus importants.</span><span class="sxs-lookup"><span data-stu-id="4e31d-171">But with security groups, you can easily manage larger groups of users.</span></span>
  
## <a name="can-i-send-email-to-a-security-group"></a><span data-ttu-id="4e31d-172">Puis-je envoyer des courriers électroniques à un groupe de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="4e31d-172">Can I send email to a security group?</span></span>

<span data-ttu-id="4e31d-173">Oui.</span><span class="sxs-lookup"><span data-stu-id="4e31d-173">Yes.</span></span> <span data-ttu-id="4e31d-174">Toutefois, si vous souhaitez utiliser des groupes pour la messagerie et la collaboration, nous vous recommandons de [créer un groupe Microsoft 365 à la](../create-groups/create-groups.md) place.</span><span class="sxs-lookup"><span data-stu-id="4e31d-174">But if you want to use groups for email and collaboration, we recommend that you [create a Microsoft 365 group](../create-groups/create-groups.md) instead.</span></span> 
  
