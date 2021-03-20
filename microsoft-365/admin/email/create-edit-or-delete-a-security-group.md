---
title: Créer, modifier ou supprimer un groupe de sécurité dans le Centre d’administration Microsoft 365
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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 55c96b32-e086-4c9e-948b-a018b44510cb
description: Apprenez à créer, modifier ou supprimer un groupe de sécurité.
ms.openlocfilehash: d2cc749acaf7b2e23674156f6ad9a200ec7b386d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50915817"
---
# <a name="create-edit-or-delete-a-security-group-in-the-microsoft-365-admin-center"></a><span data-ttu-id="13305-103">Créer, modifier ou supprimer un groupe de sécurité dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="13305-103">Create, edit, or delete a security group in the Microsoft 365 admin center</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="13305-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="13305-104">The admin center is changing.</span></span> <span data-ttu-id="13305-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="13305-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="13305-106">Dans la **page** Groupes Microsoft 365, vous pouvez créer des groupes de comptes d’utilisateurs que vous pouvez utiliser pour attribuer les mêmes autorisations dans SharePoint Online et CRM Online.</span><span class="sxs-lookup"><span data-stu-id="13305-106">On the Microsoft 365 **Groups** page, you can create groups of user accounts that you can use to assign the same permissions to in SharePoint Online and CRM Online.</span></span> <span data-ttu-id="13305-107">Par exemple, un administrateur peut créer un groupe de sécurité pour accorder à un certain groupe de personnes l’accès à un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="13305-107">For example, an administrator can create a security group to grant a certain group of people access to a SharePoint site.</span></span> <span data-ttu-id="13305-108">Seuls les administrateurs globaux et de gestion des utilisateurs sont autorisés à créer, modifier ou supprimer des groupes de sécurité . Pour plus d’informations sur les rôles d’administrateur, voir [Attribuer des rôles d’administrateur.](../add-users/assign-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="13305-108">Only global and user management administrators have permissions to create, edit, or delete security groups; for more information about administrator roles, see [Assigning admin roles](../add-users/assign-admin-roles.md).</span></span> 
  
<span data-ttu-id="13305-109">En outre, vous pouvez utiliser des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) pour envoyer du courrier électronique ou affecter des autorisations à un groupe d'utilisateurs, ainsi que des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) qui accordent des droits d'utilisateur et un accès aux sites et aux collections de sites.</span><span class="sxs-lookup"><span data-stu-id="13305-109">There are also [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that you can use to send email or assign permissions to a group of users, and [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that grant users rights and access to sites and site collections.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="13305-110">Vous prévoyez d'utiliser des boîtes aux lettres de site ?</span><span class="sxs-lookup"><span data-stu-id="13305-110">Planning on using site mailboxes?</span></span> <span data-ttu-id="13305-111">Tous les utilisateurs ajoutés à un site SharePoint via un groupe de sécurité plutôt qu'individuellement ne peuvent utiliser la boîte aux lettres de site qu'à partir de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="13305-111">All the users that are added to a SharePoint site via a security group rather than being added individually can use only the site mailbox from SharePoint.</span></span> <span data-ttu-id="13305-112">Ils n'auront pas accès à la boîte aux lettres de site à partir d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="13305-112">These users won't be able to access the site mailbox from Outlook.</span></span> <span data-ttu-id="13305-113">Pour plus d’informations, voir Utiliser les groupes [Microsoft 365 au lieu des boîtes](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b)aux lettres de site.</span><span class="sxs-lookup"><span data-stu-id="13305-113">For more information, see [Use Microsoft 365 Groups instead of Site Mailboxes](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b).</span></span> 
  
## <a name="manage-security-groups-in-the-admin-center"></a><span data-ttu-id="13305-114">Gérer les groupes de sécurité dans le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="13305-114">Manage security groups in the admin center</span></span>

### <a name="add-a-security-group"></a><span data-ttu-id="13305-115">Ajouter un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="13305-115">Add a security group</span></span>

1. <span data-ttu-id="13305-116">Dans le Centre d’administration Microsoft 365, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="13305-116">In the Microsoft 365 admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="13305-117">Dans la page **Groupes,** **sélectionnez Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="13305-117">On the **Groups** page, select **Add a group**.</span></span>
    
3. <span data-ttu-id="13305-118">Dans la page **Choisir un type de groupe,** choisissez **Sécurité.**</span><span class="sxs-lookup"><span data-stu-id="13305-118">On the **Choose a group type** page, choose **Security**.</span></span> 
    
4. <span data-ttu-id="13305-119">Suivez les étapes pour terminer la création du groupe.</span><span class="sxs-lookup"><span data-stu-id="13305-119">Follow the steps to complete creation of the group.</span></span> 
 
### <a name="add-members-to-a-security-group"></a><span data-ttu-id="13305-120">Ajouter des membres à un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="13305-120">Add members to a security group</span></span>

::: moniker range="o365-worldwide"
    
1. <span data-ttu-id="13305-121">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis sous l’onglet **Membres,** sélectionnez **Afficher tout et gérer les membres.**</span><span class="sxs-lookup"><span data-stu-id="13305-121">Select the security group name on the **Groups** page, and on the **Members** tab, select **View all and manage members**.</span></span> 
    
2. <span data-ttu-id="13305-122">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="13305-122">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="13305-123">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="13305-123">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="13305-124">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis **sélectionnez Modifier** en côté de **Membres.**</span><span class="sxs-lookup"><span data-stu-id="13305-124">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="13305-125">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="13305-125">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="13305-126">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="13305-126">To remove members, select the X next to their name.</span></span> 
  
::: moniker-end

::: moniker range="o365-21vianet"


1. <span data-ttu-id="13305-127">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis **sélectionnez Modifier** en côté de **Membres.**</span><span class="sxs-lookup"><span data-stu-id="13305-127">Select the security group name on the **Groups** page, and then select **Edit** next to **Members**.</span></span> 
    
2. <span data-ttu-id="13305-128">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="13305-128">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="13305-129">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="13305-129">To remove members, select the X next to their name.</span></span>

::: moniker-end

### <a name="edit-a-security-group"></a><span data-ttu-id="13305-130">Modifier un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="13305-130">Edit a security group</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="13305-131">Dans le Centre d’administration, allez à la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="13305-131">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="13305-132">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="13305-132">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="13305-133">Dans le volet Paramètres,  sélectionnez  l’onglet Général ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="13305-133">In the settings pane, select the **General** tab or the **Members** tab to edit either group details or members.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="13305-134">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration,</a>allez à la page  \> **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="13305-134">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** \> **Groups** page.</span></span>  
  
2. <span data-ttu-id="13305-135">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="13305-135">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="13305-136">Dans le volet de groupe de  sécurité,  sélectionnez **Modifier** à côté de l’onglet Nom ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="13305-136">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="13305-137">Une fois que vous avez apporté des modifications, **sélectionnez Fermer** \> **.**</span><span class="sxs-lookup"><span data-stu-id="13305-137">After you've made changes, select **Save** \> **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="13305-138">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration,</a>allez à la page  \> **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="13305-138">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** \> **Groups** page.</span></span>
  
2. <span data-ttu-id="13305-139">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="13305-139">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="13305-140">Dans le volet de groupe de  sécurité,  sélectionnez **Modifier** à côté de l’onglet Nom ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="13305-140">In the security group pane, select **Edit** next to either **Name** or **Members** tab to edit either group details or members.</span></span>
    
4. <span data-ttu-id="13305-141">Une fois que vous avez apporté des modifications, **sélectionnez Fermer** > **.**</span><span class="sxs-lookup"><span data-stu-id="13305-141">After you've made changes, select **Save** > **Close**.</span></span>

::: moniker-end


### <a name="delete-a-security-group"></a><span data-ttu-id="13305-142">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="13305-142">Delete a security group</span></span>

1. <span data-ttu-id="13305-143">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="13305-143">In the admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
    
2. <span data-ttu-id="13305-144">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="13305-144">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="13305-145">Sélectionnez **Supprimer le** groupe (icône wasetbin), puis confirmez en sélectionnant **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="13305-145">Select **Delete group** (wasetbin icon), and then confirm by selecting **Delete**.</span></span>
    
    <span data-ttu-id="13305-146">Sélectionnez **Fermer** une fois le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="13305-146">Select **Close** once the group is deleted.</span></span> 
    
## <a name="groups-in-exchange-online-and-sharepoint-online"></a><span data-ttu-id="13305-147">Groupes dans Exchange Online et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="13305-147">Groups in Exchange Online and SharePoint Online</span></span>

<span data-ttu-id="13305-148">Si vous souhaitez créer des groupes d’utilisateurs afin de pouvoir leur envoyer des messages électroniques  en même temps, vous pouvez le faire dans le Centre d’administration Exchange en allant à Groupes de \>  \> **destinataires** Exchange \> **d’administration.**</span><span class="sxs-lookup"><span data-stu-id="13305-148">If you want to create groups of users so you can send email to them all at the same time, you can do that in the Exchange admin center by going to **Admin** \> **Exchange** \> **Recipients** \> **Groups**.</span></span> <span data-ttu-id="13305-149">Ensuite, **sélectionnez Nouvel** ![ ](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png) ajout, puis sélectionnez le type de groupe que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="13305-149">Next, select **New**![Add](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png), and select the kind of group you want to create:</span></span> 
  
- <span data-ttu-id="13305-150">**Groupe de distribution**: un groupe de distribution permet de distribuer des messages à un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="13305-150">**Distribution group**: Used to distribute messages to a group of users.</span></span> <span data-ttu-id="13305-151">Il s’agit également d’un groupe de distribution à *messagerie* ou d’une *liste de distribution.*</span><span class="sxs-lookup"><span data-stu-id="13305-151">It's also called a  *mail-enabled distribution group*, or, a  *distribution list*.</span></span> <span data-ttu-id="13305-152">Pour plus d'informations, voir [Gestion des groupes de distribution](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="13305-152">For more information, see [Manage distribution groups](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span></span>
    
- <span data-ttu-id="13305-153">**Groupe de sécurité**: un groupe de sécurité permet de distribuer des messages à un groupe d'utilisateurs ou d'accorder des autorisations d'accès à des ressources.</span><span class="sxs-lookup"><span data-stu-id="13305-153">**Security group**: Can be used to distribute messages to a group of users, or to grant access permissions to resources.</span></span> <span data-ttu-id="13305-154">Ce groupe est également appelé groupe de sécurité à *messagerie.*</span><span class="sxs-lookup"><span data-stu-id="13305-154">This group is also called a *mail-enabled security group*.</span></span> <span data-ttu-id="13305-155">Pour plus d'informations, voir [Gérer les groupes de sécurité à extension de messagerie](/Exchange/recipients/mail-enabled-security-groups).</span><span class="sxs-lookup"><span data-stu-id="13305-155">For more information, see [Manage mail-enabled security groups](/Exchange/recipients/mail-enabled-security-groups).</span></span>
    
- <span data-ttu-id="13305-156">**Groupe de distribution dynamique**: type de groupe de distribution dont la liste de destinataires est recalculée chaque fois que vous envoyez un message en fonction des filtres et des conditions définis par vos soins.</span><span class="sxs-lookup"><span data-stu-id="13305-156">**Dynamic distribution group**: A type of distribution group whose list of recipients is recalculated every time you send a message based on filters and conditions that you define.</span></span> <span data-ttu-id="13305-157">Pour plus d'informations, reportez-vous à [Gérer des groupes de distribution dynamiques](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="13305-157">For more information, see [Manage dynamic distribution groups](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span></span>
    
<span data-ttu-id="13305-158">Une fois que vous avez créé des groupes de distribution et des groupes de sécurité à messagerie dans le Centre d’administration Exchange, leurs noms et leurs listes d’utilisateurs apparaissent sur la page **Groupes de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="13305-158">After you create distribution groups and mail-enabled security groups in the Exchange admin center, their names and user lists appear on the **Security groups** page.</span></span> <span data-ttu-id="13305-159">Vous pouvez supprimer ces groupes aux deux emplacements, mais vous ne pouvez les modifier que dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="13305-159">You can delete these groups in both locations, but you can edit them only in the Exchange admin center.</span></span> <span data-ttu-id="13305-160">Les groupes de distribution dynamiques ne s’affiche pas sur la page **Groupes de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="13305-160">Dynamic distribution groups don't show up on the **Security groups** page.</span></span> 
  
 <span data-ttu-id="13305-161">Les groupes SharePoint sont générés automatiquement quand vous créez une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="13305-161">SharePoint groups are created automatically when you make a site collection.</span></span> <span data-ttu-id="13305-162">Les groupes par défaut utilisent les niveaux d'autorisation par défaut dans SharePoint  parfois appelés rôles SharePoint  pour accorder aux utilisateurs des droits et un accès.</span><span class="sxs-lookup"><span data-stu-id="13305-162">The default groups use the default permission levels in SharePoint—sometimes called SharePoint roles—to grant users rights and access.</span></span> <span data-ttu-id="13305-163">Pour plus d’informations, [voir Groupes SharePoint par défaut dans SharePoint Online.](/sharepoint/default-sharepoint-groups)</span><span class="sxs-lookup"><span data-stu-id="13305-163">For more information, see [Default SharePoint groups in SharePoint Online](/sharepoint/default-sharepoint-groups).</span></span>
  
## <a name="how-is-a-security-group-different-from-security-groups-i-create-in-sharepoint"></a><span data-ttu-id="13305-164">En quoi un groupe de sécurité est-il différent des groupes de sécurité que j’ai créés dans SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="13305-164">How is a security group different from security groups I create in SharePoint?</span></span>

<span data-ttu-id="13305-165">Les groupes de sécurité peuvent être utilisés avec SharePoint, Exchange, MDM, Windows, etc.</span><span class="sxs-lookup"><span data-stu-id="13305-165">Security groups can be used with SharePoint, Exchange, MDM, Windows, and more.</span></span> <span data-ttu-id="13305-166">Un groupe de sécurité que vous créez dans SharePoint est uniquement reconnu par cette collection de sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="13305-166">A security group you create in SharePoint is only recognized by that SharePoint site collection.</span></span>
  
## <a name="do-i-have-to-use-security-groups-for-my-organization-to-be-secure"></a><span data-ttu-id="13305-167">Dois-je utiliser des groupes de sécurité pour que mon organisation soit sécurisée ?</span><span class="sxs-lookup"><span data-stu-id="13305-167">Do I have to use security groups for my organization to be secure?</span></span>

<span data-ttu-id="13305-168">Non.</span><span class="sxs-lookup"><span data-stu-id="13305-168">No.</span></span> <span data-ttu-id="13305-169">Il s’agit simplement d’un moyen de plus pour gérer la sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="13305-169">This is just one more way you can manage security for your organization.</span></span> <span data-ttu-id="13305-170">Vous pouvez toujours accorder des autorisations utilisateur et l’accès aux sites individuellement.</span><span class="sxs-lookup"><span data-stu-id="13305-170">You can always grant user permissions and access to sites individually.</span></span> <span data-ttu-id="13305-171">Toutefois, avec les groupes de sécurité, vous pouvez facilement gérer des groupes d’utilisateurs plus importants.</span><span class="sxs-lookup"><span data-stu-id="13305-171">But with security groups, you can easily manage larger groups of users.</span></span>
  
## <a name="can-i-send-email-to-a-security-group"></a><span data-ttu-id="13305-172">Puis-je envoyer un courrier électronique à un groupe de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="13305-172">Can I send email to a security group?</span></span>

<span data-ttu-id="13305-173">Oui.</span><span class="sxs-lookup"><span data-stu-id="13305-173">Yes.</span></span> <span data-ttu-id="13305-174">Toutefois, si vous souhaitez utiliser des groupes pour la messagerie et la collaboration, nous vous recommandons plutôt de créer un groupe [Microsoft 365.](../create-groups/create-groups.md)</span><span class="sxs-lookup"><span data-stu-id="13305-174">But if you want to use groups for email and collaboration, we recommend that you [create a Microsoft 365 group](../create-groups/create-groups.md) instead.</span></span> 
