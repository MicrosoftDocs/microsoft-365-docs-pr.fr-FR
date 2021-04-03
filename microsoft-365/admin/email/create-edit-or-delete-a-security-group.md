---
title: Créer, modifier ou supprimer un groupe de sécurité dans le Centre d’administration Microsoft 365
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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 55c96b32-e086-4c9e-948b-a018b44510cb
description: Apprenez à créer, modifier ou supprimer un groupe de sécurité.
ms.openlocfilehash: 03e391727f9a61b1fc8e819e92d5a119017c38e0
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51579337"
---
# <a name="create-edit-or-delete-a-security-group-in-the-microsoft-365-admin-center"></a><span data-ttu-id="3240d-103">Créer, modifier ou supprimer un groupe de sécurité dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3240d-103">Create, edit, or delete a security group in the Microsoft 365 admin center</span></span>

<span data-ttu-id="3240d-104">Dans la **page** Groupes Microsoft 365, vous pouvez créer des groupes de comptes d’utilisateurs que vous pouvez utiliser pour attribuer les mêmes autorisations dans SharePoint Online et CRM Online.</span><span class="sxs-lookup"><span data-stu-id="3240d-104">On the Microsoft 365 **Groups** page, you can create groups of user accounts that you can use to assign the same permissions to in SharePoint Online and CRM Online.</span></span> <span data-ttu-id="3240d-105">Par exemple, un administrateur peut créer un groupe de sécurité pour accorder à un certain groupe de personnes l’accès à un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3240d-105">For example, an administrator can create a security group to grant a certain group of people access to a SharePoint site.</span></span> <span data-ttu-id="3240d-106">Seuls les administrateurs globaux et de gestion des utilisateurs sont autorisés à créer, modifier ou supprimer des groupes de sécurité . Pour plus d’informations sur les rôles d’administrateur, voir [Attribuer des rôles d’administrateur.](../add-users/assign-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="3240d-106">Only global and user management administrators have permissions to create, edit, or delete security groups; for more information about administrator roles, see [Assigning admin roles](../add-users/assign-admin-roles.md).</span></span> 
  
<span data-ttu-id="3240d-107">En outre, vous pouvez utiliser des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) pour envoyer du courrier électronique ou affecter des autorisations à un groupe d'utilisateurs, ainsi que des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) qui accordent des droits d'utilisateur et un accès aux sites et aux collections de sites.</span><span class="sxs-lookup"><span data-stu-id="3240d-107">There are also [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that you can use to send email or assign permissions to a group of users, and [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that grant users rights and access to sites and site collections.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="3240d-108">Vous prévoyez d'utiliser des boîtes aux lettres de site ?</span><span class="sxs-lookup"><span data-stu-id="3240d-108">Planning on using site mailboxes?</span></span> <span data-ttu-id="3240d-109">Tous les utilisateurs ajoutés à un site SharePoint via un groupe de sécurité plutôt qu'individuellement ne peuvent utiliser la boîte aux lettres de site qu'à partir de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3240d-109">All the users that are added to a SharePoint site via a security group rather than being added individually can use only the site mailbox from SharePoint.</span></span> <span data-ttu-id="3240d-110">Ils n'auront pas accès à la boîte aux lettres de site à partir d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="3240d-110">These users won't be able to access the site mailbox from Outlook.</span></span> <span data-ttu-id="3240d-111">Pour plus d’informations, voir Utiliser les groupes [Microsoft 365 au lieu des boîtes](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b)aux lettres de site.</span><span class="sxs-lookup"><span data-stu-id="3240d-111">For more information, see [Use Microsoft 365 Groups instead of Site Mailboxes](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b).</span></span> 
  
## <a name="manage-security-groups-in-the-admin-center"></a><span data-ttu-id="3240d-112">Gérer les groupes de sécurité dans le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="3240d-112">Manage security groups in the admin center</span></span>

### <a name="add-a-security-group"></a><span data-ttu-id="3240d-113">Ajouter un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="3240d-113">Add a security group</span></span>

1. <span data-ttu-id="3240d-114">Dans le Centre d’administration Microsoft 365, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="3240d-114">In the Microsoft 365 admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="3240d-115">Dans la page **Groupes,** **sélectionnez Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="3240d-115">On the **Groups** page, select **Add a group**.</span></span>
    
3. <span data-ttu-id="3240d-116">Dans la page **Choisir un type de groupe,** choisissez **Sécurité.**</span><span class="sxs-lookup"><span data-stu-id="3240d-116">On the **Choose a group type** page, choose **Security**.</span></span> 
    
4. <span data-ttu-id="3240d-117">Suivez les étapes pour terminer la création du groupe.</span><span class="sxs-lookup"><span data-stu-id="3240d-117">Follow the steps to complete creation of the group.</span></span> 
 
### <a name="add-members-to-a-security-group"></a><span data-ttu-id="3240d-118">Ajouter des membres à un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="3240d-118">Add members to a security group</span></span>

::: moniker range="o365-worldwide"
    
1. <span data-ttu-id="3240d-119">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis sous l’onglet **Membres,** sélectionnez **Afficher tout et gérer les membres.**</span><span class="sxs-lookup"><span data-stu-id="3240d-119">Select the security group name on the **Groups** page, and on the **Members** tab, select **View all and manage members**.</span></span> 
    
2. <span data-ttu-id="3240d-120">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3240d-120">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="3240d-121">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="3240d-121">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="3240d-122">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis sélectionnez **Modifier en** côté de **Membres.**</span><span class="sxs-lookup"><span data-stu-id="3240d-122">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="3240d-123">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3240d-123">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="3240d-124">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="3240d-124">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-21vianet"


1. <span data-ttu-id="3240d-125">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis sélectionnez **Modifier en** côté de **Membres.**</span><span class="sxs-lookup"><span data-stu-id="3240d-125">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="3240d-126">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3240d-126">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="3240d-127">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="3240d-127">To remove members, select the X next to their name.</span></span>

::: moniker-end

### <a name="edit-a-security-group"></a><span data-ttu-id="3240d-128">Modifier un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="3240d-128">Edit a security group</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="3240d-129">Dans le Centre d’administration, allez à la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="3240d-129">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="3240d-130">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="3240d-130">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="3240d-131">Dans le volet Paramètres,  sélectionnez  l’onglet Général ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="3240d-131">In the settings pane, select the **General** tab or the **Members** tab to edit either group details or members.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="3240d-132">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration,</a>allez à la page  \> **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="3240d-132">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** \> **Groups** page.</span></span>  
  
2. <span data-ttu-id="3240d-133">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="3240d-133">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="3240d-134">Dans le volet de groupe de  sécurité,  sélectionnez **Modifier** à côté de l’onglet Nom ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="3240d-134">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="3240d-135">Une fois que vous avez apporté des modifications, **sélectionnez Fermer** \> **.**</span><span class="sxs-lookup"><span data-stu-id="3240d-135">After you've made changes, select **Save** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="3240d-136">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration,</a>allez à la page  \> **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="3240d-136">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** \> **Groups** page.</span></span>
  
2. <span data-ttu-id="3240d-137">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="3240d-137">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="3240d-138">Dans le volet de groupe de  sécurité,  sélectionnez **Modifier** à côté de l’onglet Nom ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="3240d-138">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="3240d-139">Une fois que vous avez apporté des modifications, **sélectionnez Fermer** > **.**</span><span class="sxs-lookup"><span data-stu-id="3240d-139">After you've made changes, select **Save** > **Close**.</span></span>

::: moniker-end


### <a name="delete-a-security-group"></a><span data-ttu-id="3240d-140">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="3240d-140">Delete a security group</span></span>

1. <span data-ttu-id="3240d-141">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="3240d-141">In the admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
    
2. <span data-ttu-id="3240d-142">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="3240d-142">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="3240d-143">Sélectionnez **Supprimer le** groupe (icône wasetbin), puis confirmez en sélectionnant **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="3240d-143">Select **Delete group** (wasetbin icon), and then confirm by selecting **Delete**.</span></span>
    
    <span data-ttu-id="3240d-144">Sélectionnez **Fermer** une fois le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="3240d-144">Select **Close** once the group is deleted.</span></span> 
    
## <a name="groups-in-exchange-online-and-sharepoint-online"></a><span data-ttu-id="3240d-145">Groupes dans Exchange Online et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3240d-145">Groups in Exchange Online and SharePoint Online</span></span>

<span data-ttu-id="3240d-146">Si vous souhaitez créer des groupes d’utilisateurs afin de pouvoir leur envoyer des messages électroniques  en même temps, vous pouvez le faire dans le Centre d’administration Exchange en allant à Groupes de \>  \> **destinataires** Exchange \> **d’administration.**</span><span class="sxs-lookup"><span data-stu-id="3240d-146">If you want to create groups of users so you can send email to them all at the same time, you can do that in the Exchange admin center by going to **Admin** \> **Exchange** \> **Recipients** \> **Groups**.</span></span> <span data-ttu-id="3240d-147">Ensuite, **sélectionnez Nouvel** ![ ](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png) ajout, puis sélectionnez le type de groupe que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="3240d-147">Next, select **New**![Add](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png), and select the kind of group you want to create:</span></span> 
  
- <span data-ttu-id="3240d-148">**Groupe de distribution**: un groupe de distribution permet de distribuer des messages à un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3240d-148">**Distribution group**: Used to distribute messages to a group of users.</span></span> <span data-ttu-id="3240d-149">Il s’agit également d’un groupe de distribution à *messagerie* ou d’une *liste de distribution.*</span><span class="sxs-lookup"><span data-stu-id="3240d-149">It's also called a  *mail-enabled distribution group*, or, a  *distribution list*.</span></span> <span data-ttu-id="3240d-150">Pour plus d'informations, voir [Gestion des groupes de distribution](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="3240d-150">For more information, see [Manage distribution groups](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span></span>
    
- <span data-ttu-id="3240d-151">**Groupe de sécurité**: un groupe de sécurité permet de distribuer des messages à un groupe d'utilisateurs ou d'accorder des autorisations d'accès à des ressources.</span><span class="sxs-lookup"><span data-stu-id="3240d-151">**Security group**: Can be used to distribute messages to a group of users, or to grant access permissions to resources.</span></span> <span data-ttu-id="3240d-152">Ce groupe est également appelé groupe de sécurité à *messagerie.*</span><span class="sxs-lookup"><span data-stu-id="3240d-152">This group is also called a *mail-enabled security group*.</span></span> <span data-ttu-id="3240d-153">Pour plus d'informations, voir [Gérer les groupes de sécurité à extension de messagerie](/Exchange/recipients/mail-enabled-security-groups).</span><span class="sxs-lookup"><span data-stu-id="3240d-153">For more information, see [Manage mail-enabled security groups](/Exchange/recipients/mail-enabled-security-groups).</span></span>
    
- <span data-ttu-id="3240d-154">**Groupe de distribution dynamique**: type de groupe de distribution dont la liste de destinataires est recalculée chaque fois que vous envoyez un message en fonction des filtres et des conditions définis par vos soins.</span><span class="sxs-lookup"><span data-stu-id="3240d-154">**Dynamic distribution group**: A type of distribution group whose list of recipients is recalculated every time you send a message based on filters and conditions that you define.</span></span> <span data-ttu-id="3240d-155">Pour plus d'informations, reportez-vous à [Gérer des groupes de distribution dynamiques](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="3240d-155">For more information, see [Manage dynamic distribution groups](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span></span>
    
<span data-ttu-id="3240d-156">Une fois que vous avez créé des groupes de distribution et des groupes de sécurité à messagerie dans le Centre d’administration Exchange, leurs noms et leurs listes d’utilisateurs apparaissent sur la page **Groupes de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="3240d-156">After you create distribution groups and mail-enabled security groups in the Exchange admin center, their names and user lists appear on the **Security groups** page.</span></span> <span data-ttu-id="3240d-157">Vous pouvez supprimer ces groupes aux deux emplacements, mais vous ne pouvez les modifier que dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="3240d-157">You can delete these groups in both locations, but you can edit them only in the Exchange admin center.</span></span> <span data-ttu-id="3240d-158">Les groupes de distribution dynamiques ne s’affiche pas sur la page **Groupes de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="3240d-158">Dynamic distribution groups don't show up on the **Security groups** page.</span></span> 
  
 <span data-ttu-id="3240d-159">Les groupes SharePoint sont générés automatiquement quand vous créez une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="3240d-159">SharePoint groups are created automatically when you make a site collection.</span></span> <span data-ttu-id="3240d-160">Les groupes par défaut utilisent les niveaux d'autorisation par défaut dans SharePoint  parfois appelés rôles SharePoint  pour accorder aux utilisateurs des droits et un accès.</span><span class="sxs-lookup"><span data-stu-id="3240d-160">The default groups use the default permission levels in SharePoint—sometimes called SharePoint roles—to grant users rights and access.</span></span> <span data-ttu-id="3240d-161">Pour plus d’informations, [voir Groupes SharePoint par défaut dans SharePoint Online.](/sharepoint/default-sharepoint-groups)</span><span class="sxs-lookup"><span data-stu-id="3240d-161">For more information, see [Default SharePoint groups in SharePoint Online](/sharepoint/default-sharepoint-groups).</span></span>
  
## <a name="how-is-a-security-group-different-from-security-groups-i-create-in-sharepoint"></a><span data-ttu-id="3240d-162">En quoi un groupe de sécurité est-il différent des groupes de sécurité que j’ai créés dans SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="3240d-162">How is a security group different from security groups I create in SharePoint?</span></span>

<span data-ttu-id="3240d-163">Les groupes de sécurité peuvent être utilisés avec SharePoint, Exchange, MDM, Windows, etc.</span><span class="sxs-lookup"><span data-stu-id="3240d-163">Security groups can be used with SharePoint, Exchange, MDM, Windows, and more.</span></span> <span data-ttu-id="3240d-164">Un groupe de sécurité que vous créez dans SharePoint est uniquement reconnu par cette collection de sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3240d-164">A security group you create in SharePoint is only recognized by that SharePoint site collection.</span></span>
  
## <a name="do-i-have-to-use-security-groups-for-my-organization-to-be-secure"></a><span data-ttu-id="3240d-165">Dois-je utiliser des groupes de sécurité pour que mon organisation soit sécurisée ?</span><span class="sxs-lookup"><span data-stu-id="3240d-165">Do I have to use security groups for my organization to be secure?</span></span>

<span data-ttu-id="3240d-166">Non.</span><span class="sxs-lookup"><span data-stu-id="3240d-166">No.</span></span> <span data-ttu-id="3240d-167">Il s’agit simplement d’un moyen de plus pour gérer la sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3240d-167">This is just one more way you can manage security for your organization.</span></span> <span data-ttu-id="3240d-168">Vous pouvez toujours accorder des autorisations utilisateur et l’accès aux sites individuellement.</span><span class="sxs-lookup"><span data-stu-id="3240d-168">You can always grant user permissions and access to sites individually.</span></span> <span data-ttu-id="3240d-169">Toutefois, avec les groupes de sécurité, vous pouvez facilement gérer des groupes d’utilisateurs plus importants.</span><span class="sxs-lookup"><span data-stu-id="3240d-169">But with security groups, you can easily manage larger groups of users.</span></span>
  
## <a name="can-i-send-email-to-a-security-group"></a><span data-ttu-id="3240d-170">Puis-je envoyer des courriers électroniques à un groupe de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="3240d-170">Can I send email to a security group?</span></span>

<span data-ttu-id="3240d-171">Oui.</span><span class="sxs-lookup"><span data-stu-id="3240d-171">Yes.</span></span> <span data-ttu-id="3240d-172">Toutefois, si vous souhaitez utiliser des groupes pour la messagerie et la collaboration, nous vous recommandons plutôt de créer un groupe [Microsoft 365.](../create-groups/create-groups.md)</span><span class="sxs-lookup"><span data-stu-id="3240d-172">But if you want to use groups for email and collaboration, we recommend that you [create a Microsoft 365 group](../create-groups/create-groups.md) instead.</span></span> 
