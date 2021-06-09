---
title: Créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration Microsoft 365 de sécurité
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
ms.openlocfilehash: 7887a6371287ebef3a91cc1a37f2ed696df1948d
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52624000"
---
# <a name="create-edit-or-delete-a-security-group-in-the-microsoft-365-admin-center"></a><span data-ttu-id="73146-103">Créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration Microsoft 365 de sécurité</span><span class="sxs-lookup"><span data-stu-id="73146-103">Create, edit, or delete a security group in the Microsoft 365 admin center</span></span>

<span data-ttu-id="73146-104">Dans la **page** Groupes Microsoft 365, vous pouvez créer des groupes de comptes d’utilisateurs que vous pouvez utiliser pour attribuer les mêmes autorisations dans SharePoint Online et CRM Online.</span><span class="sxs-lookup"><span data-stu-id="73146-104">On the Microsoft 365 **Groups** page, you can create groups of user accounts that you can use to assign the same permissions to in SharePoint Online and CRM Online.</span></span> <span data-ttu-id="73146-105">Par exemple, un administrateur peut créer un groupe de sécurité pour accorder à un certain groupe de personnes l’accès à un SharePoint site.</span><span class="sxs-lookup"><span data-stu-id="73146-105">For example, an administrator can create a security group to grant a certain group of people access to a SharePoint site.</span></span> <span data-ttu-id="73146-106">Seuls les administrateurs globaux et de gestion des utilisateurs sont autorisés à créer, modifier ou supprimer des groupes de sécurité . Pour plus d’informations sur les rôles d’administrateur, voir [Attribuer des rôles d’administrateur.](../add-users/assign-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="73146-106">Only global and user management administrators have permissions to create, edit, or delete security groups; for more information about administrator roles, see [Assigning admin roles](../add-users/assign-admin-roles.md).</span></span> 
  
<span data-ttu-id="73146-107">En outre, vous pouvez utiliser des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) pour envoyer du courrier électronique ou affecter des autorisations à un groupe d'utilisateurs, ainsi que des [Groupes dans Exchange Online et SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) qui accordent des droits d'utilisateur et un accès aux sites et aux collections de sites.</span><span class="sxs-lookup"><span data-stu-id="73146-107">There are also [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that you can use to send email or assign permissions to a group of users, and [Groups in Exchange Online and SharePoint Online](#groups-in-exchange-online-and-sharepoint-online) that grant users rights and access to sites and site collections.</span></span> 
  
> [!IMPORTANT]
>  <span data-ttu-id="73146-108">Vous prévoyez d'utiliser des boîtes aux lettres de site ?</span><span class="sxs-lookup"><span data-stu-id="73146-108">Planning on using site mailboxes?</span></span> <span data-ttu-id="73146-109">Tous les utilisateurs ajoutés à un site SharePoint via un groupe de sécurité plutôt qu'individuellement ne peuvent utiliser la boîte aux lettres de site qu'à partir de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="73146-109">All the users that are added to a SharePoint site via a security group rather than being added individually can use only the site mailbox from SharePoint.</span></span> <span data-ttu-id="73146-110">Ils n'auront pas accès à la boîte aux lettres de site à partir d'Outlook.</span><span class="sxs-lookup"><span data-stu-id="73146-110">These users won't be able to access the site mailbox from Outlook.</span></span> <span data-ttu-id="73146-111">Pour plus d’informations, [voir Utiliser des groupes Microsoft 365 plutôt que des boîtes aux lettres de site.](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b)</span><span class="sxs-lookup"><span data-stu-id="73146-111">For more information, see [Use Microsoft 365 Groups instead of Site Mailboxes](https://support.microsoft.com/office/737d6b1f-67cc-41fe-8db8-f2d09dd1673b).</span></span> 
  
## <a name="manage-security-groups-in-the-admin-center"></a><span data-ttu-id="73146-112">Gérer les groupes de sécurité dans le Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="73146-112">Manage security groups in the admin center</span></span>

### <a name="add-a-security-group"></a><span data-ttu-id="73146-113">Ajouter un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="73146-113">Add a security group</span></span>

1. <span data-ttu-id="73146-114">Dans le Microsoft 365 d’administration, allez à la page  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="73146-114">In the Microsoft 365 admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="73146-115">Dans la page **Groupes,** **sélectionnez Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="73146-115">On the **Groups** page, select **Add a group**.</span></span>
    
3. <span data-ttu-id="73146-116">Dans la page **Choisir un type de groupe,** choisissez **Sécurité.**</span><span class="sxs-lookup"><span data-stu-id="73146-116">On the **Choose a group type** page, choose **Security**.</span></span> 
    
4. <span data-ttu-id="73146-117">Suivez les étapes pour terminer la création du groupe.</span><span class="sxs-lookup"><span data-stu-id="73146-117">Follow the steps to complete creation of the group.</span></span> 
 
### <a name="add-members-to-a-security-group"></a><span data-ttu-id="73146-118">Ajouter des membres à un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="73146-118">Add members to a security group</span></span>
    
1. <span data-ttu-id="73146-119">Sélectionnez le nom du groupe de sécurité dans la page **Groupes,** puis sous l’onglet **Membres,** sélectionnez **Afficher tout et gérer les membres.**</span><span class="sxs-lookup"><span data-stu-id="73146-119">Select the security group name on the **Groups** page, and on the **Members** tab, select **View all and manage members**.</span></span> 
    
2. <span data-ttu-id="73146-120">Dans le volet de  groupe, sélectionnez Ajouter des membres et choisissez la personne dans  la liste ou tapez le nom de la personne que vous souhaitez ajouter dans la zone de recherche, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="73146-120">In the group pane, select **Add members** and choose the person from the list or type the name of the person you want to add in the **Search** box, and then select **Save**.</span></span>
    
    <span data-ttu-id="73146-121">Pour supprimer des membres, sélectionnez le X à côté de leur nom.</span><span class="sxs-lookup"><span data-stu-id="73146-121">To remove members, select the X next to their name.</span></span> 
  
### <a name="edit-a-security-group"></a><span data-ttu-id="73146-122">Modifier un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="73146-122">Edit a security group</span></span>

1. <span data-ttu-id="73146-123">Dans le Centre d’administration, allez à la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="73146-123">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="73146-124">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="73146-124">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="73146-125">Dans le volet Paramètres,  sélectionnez  l’onglet Général ou Membres pour modifier les détails du groupe ou les membres.</span><span class="sxs-lookup"><span data-stu-id="73146-125">In the settings pane, select the **General** tab or the **Members** tab to edit either group details or members.</span></span>

### <a name="delete-a-security-group"></a><span data-ttu-id="73146-126">Supprimer un groupe de sécurité</span><span class="sxs-lookup"><span data-stu-id="73146-126">Delete a security group</span></span>

1. <span data-ttu-id="73146-127">Dans le Centre d’administration, allez à la page   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groupes.</a></span><span class="sxs-lookup"><span data-stu-id="73146-127">In the admin center, go to the **Groups** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
    
2. <span data-ttu-id="73146-128">Dans la page **Groupes,** sélectionnez le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="73146-128">On the **Groups** page, select the group's name.</span></span> 
    
3. <span data-ttu-id="73146-129">Sélectionnez **Supprimer le** groupe (icône wasetbin), puis confirmez en sélectionnant **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="73146-129">Select **Delete group** (wasetbin icon), and then confirm by selecting **Delete**.</span></span>
    
    <span data-ttu-id="73146-130">Sélectionnez **Fermer** une fois le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="73146-130">Select **Close** once the group is deleted.</span></span> 
    
## <a name="groups-in-exchange-online-and-sharepoint-online"></a><span data-ttu-id="73146-131">Groupes dans Exchange Online et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="73146-131">Groups in Exchange Online and SharePoint Online</span></span>

<span data-ttu-id="73146-132">Si vous souhaitez créer des groupes d’utilisateurs afin de pouvoir leur envoyer des courriers électroniques en  même temps, vous pouvez le faire dans le Centre d’administration Exchange en allant à Groupes de \>  \> **destinataires** \> Exchange Admin Exchange .</span><span class="sxs-lookup"><span data-stu-id="73146-132">If you want to create groups of users so you can send email to them all at the same time, you can do that in the Exchange admin center by going to **Admin** \> **Exchange** \> **Recipients** \> **Groups**.</span></span> <span data-ttu-id="73146-133">Ensuite, **sélectionnez Nouvel** ![ ](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png) ajout, puis sélectionnez le type de groupe que vous souhaitez créer :</span><span class="sxs-lookup"><span data-stu-id="73146-133">Next, select **New**![Add](../../media/328ffb57-5f31-430a-b653-4a6b8e76d338.png), and select the kind of group you want to create:</span></span> 
  
- <span data-ttu-id="73146-134">**Groupe de distribution**: un groupe de distribution permet de distribuer des messages à un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="73146-134">**Distribution group**: Used to distribute messages to a group of users.</span></span> <span data-ttu-id="73146-135">Il s’agit également d’un groupe de distribution à *messagerie* ou d’une *liste de distribution.*</span><span class="sxs-lookup"><span data-stu-id="73146-135">It's also called a  *mail-enabled distribution group*, or, a  *distribution list*.</span></span> <span data-ttu-id="73146-136">Pour plus d'informations, voir [Gestion des groupes de distribution](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="73146-136">For more information, see [Manage distribution groups](/exchange/recipients-in-exchange-online/manage-distribution-groups/manage-distribution-groups).</span></span>
    
- <span data-ttu-id="73146-137">**Groupe de sécurité**: un groupe de sécurité permet de distribuer des messages à un groupe d'utilisateurs ou d'accorder des autorisations d'accès à des ressources.</span><span class="sxs-lookup"><span data-stu-id="73146-137">**Security group**: Can be used to distribute messages to a group of users, or to grant access permissions to resources.</span></span> <span data-ttu-id="73146-138">Ce groupe est également appelé groupe de sécurité à *messagerie.*</span><span class="sxs-lookup"><span data-stu-id="73146-138">This group is also called a *mail-enabled security group*.</span></span> <span data-ttu-id="73146-139">Pour plus d'informations, voir [Gérer les groupes de sécurité à extension de messagerie](/Exchange/recipients/mail-enabled-security-groups).</span><span class="sxs-lookup"><span data-stu-id="73146-139">For more information, see [Manage mail-enabled security groups](/Exchange/recipients/mail-enabled-security-groups).</span></span>
    
- <span data-ttu-id="73146-140">**Groupe de distribution dynamique**: type de groupe de distribution dont la liste de destinataires est recalculée chaque fois que vous envoyez un message en fonction des filtres et des conditions définis par vos soins.</span><span class="sxs-lookup"><span data-stu-id="73146-140">**Dynamic distribution group**: A type of distribution group whose list of recipients is recalculated every time you send a message based on filters and conditions that you define.</span></span> <span data-ttu-id="73146-141">Pour plus d'informations, reportez-vous à [Gérer des groupes de distribution dynamiques](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span><span class="sxs-lookup"><span data-stu-id="73146-141">For more information, see [Manage dynamic distribution groups](/Exchange/recipients/dynamic-distribution-groups/dynamic-distribution-groups).</span></span>
    
<span data-ttu-id="73146-142">Une fois que vous avez créé des groupes de distribution et des groupes de sécurité à messagerie dans le Centre d’administration Exchange, leurs noms et leurs listes d’utilisateurs apparaissent sur la page Groupes **de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="73146-142">After you create distribution groups and mail-enabled security groups in the Exchange admin center, their names and user lists appear on the **Security groups** page.</span></span> <span data-ttu-id="73146-143">Vous pouvez supprimer ces groupes aux deux emplacements, mais vous ne pouvez les modifier que dans le Centre d'administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="73146-143">You can delete these groups in both locations, but you can edit them only in the Exchange admin center.</span></span> <span data-ttu-id="73146-144">Les groupes de distribution dynamiques ne s’affiche pas sur la page **Groupes de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="73146-144">Dynamic distribution groups don't show up on the **Security groups** page.</span></span> 
  
 <span data-ttu-id="73146-145">Les groupes SharePoint sont générés automatiquement quand vous créez une collection de sites.</span><span class="sxs-lookup"><span data-stu-id="73146-145">SharePoint groups are created automatically when you make a site collection.</span></span> <span data-ttu-id="73146-146">Les groupes par défaut utilisent les niveaux d'autorisation par défaut dans SharePoint  parfois appelés rôles SharePoint  pour accorder aux utilisateurs des droits et un accès.</span><span class="sxs-lookup"><span data-stu-id="73146-146">The default groups use the default permission levels in SharePoint—sometimes called SharePoint roles—to grant users rights and access.</span></span> <span data-ttu-id="73146-147">Pour plus d’informations, [voir Groupes SharePoint par défaut dans SharePoint Online.](/sharepoint/default-sharepoint-groups)</span><span class="sxs-lookup"><span data-stu-id="73146-147">For more information, see [Default SharePoint groups in SharePoint Online](/sharepoint/default-sharepoint-groups).</span></span>
  
## <a name="how-is-a-security-group-different-from-security-groups-i-create-in-sharepoint"></a><span data-ttu-id="73146-148">En quoi un groupe de sécurité est-il différent des groupes de sécurité que j’ai créés dans SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="73146-148">How is a security group different from security groups I create in SharePoint?</span></span>

<span data-ttu-id="73146-149">Les groupes de sécurité peuvent être utilisés avec SharePoint, Exchange, la gestion des Windows, etc.</span><span class="sxs-lookup"><span data-stu-id="73146-149">Security groups can be used with SharePoint, Exchange, MDM, Windows, and more.</span></span> <span data-ttu-id="73146-150">Un groupe de sécurité que vous créez dans SharePoint est reconnu uniquement par cette SharePoint collection de sites.</span><span class="sxs-lookup"><span data-stu-id="73146-150">A security group you create in SharePoint is only recognized by that SharePoint site collection.</span></span>
  
## <a name="do-i-have-to-use-security-groups-for-my-organization-to-be-secure"></a><span data-ttu-id="73146-151">Dois-je utiliser des groupes de sécurité pour que mon organisation soit sécurisée ?</span><span class="sxs-lookup"><span data-stu-id="73146-151">Do I have to use security groups for my organization to be secure?</span></span>

<span data-ttu-id="73146-152">Non.</span><span class="sxs-lookup"><span data-stu-id="73146-152">No.</span></span> <span data-ttu-id="73146-153">Il s’agit simplement d’un moyen de plus pour gérer la sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="73146-153">This is just one more way you can manage security for your organization.</span></span> <span data-ttu-id="73146-154">Vous pouvez toujours accorder des autorisations utilisateur et l’accès aux sites individuellement.</span><span class="sxs-lookup"><span data-stu-id="73146-154">You can always grant user permissions and access to sites individually.</span></span> <span data-ttu-id="73146-155">Toutefois, avec les groupes de sécurité, vous pouvez facilement gérer des groupes d’utilisateurs plus importants.</span><span class="sxs-lookup"><span data-stu-id="73146-155">But with security groups, you can easily manage larger groups of users.</span></span>
  
## <a name="can-i-send-email-to-a-security-group"></a><span data-ttu-id="73146-156">Puis-je envoyer des courriers électroniques à un groupe de sécurité ?</span><span class="sxs-lookup"><span data-stu-id="73146-156">Can I send email to a security group?</span></span>

<span data-ttu-id="73146-157">Oui.</span><span class="sxs-lookup"><span data-stu-id="73146-157">Yes.</span></span> <span data-ttu-id="73146-158">Toutefois, si vous souhaitez utiliser des groupes pour la messagerie et la collaboration, nous vous recommandons de créer [un groupe Microsoft 365 à](../create-groups/create-groups.md) la place.</span><span class="sxs-lookup"><span data-stu-id="73146-158">But if you want to use groups for email and collaboration, we recommend that you [create a Microsoft 365 group](../create-groups/create-groups.md) instead.</span></span> 

## <a name="related-content"></a><span data-ttu-id="73146-159">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="73146-159">Related content</span></span>

<span data-ttu-id="73146-160">[Créer un groupe dans le centre d’administration Microsoft 365](../create-groups/create-groups.md) (article)</span><span class="sxs-lookup"><span data-stu-id="73146-160">[Create a group in the Microsoft 365 admin center](../create-groups/create-groups.md) (article)</span></span>\
<span data-ttu-id="73146-161">[Expliquer Microsoft 365 groupes à vos utilisateurs](../create-groups/explain-groups-knowledge-worker.md) (article)</span><span class="sxs-lookup"><span data-stu-id="73146-161">[Explaining Microsoft 365 Groups to your users](../create-groups/explain-groups-knowledge-worker.md) (article)</span></span>\
<span data-ttu-id="73146-162">[Gérer un groupe dans le centre d’administration Microsoft 365 de gestion](../create-groups/manage-groups.md) (article)</span><span class="sxs-lookup"><span data-stu-id="73146-162">[Manage a group in the Microsoft 365 admin center](../create-groups/manage-groups.md) (article)</span></span>