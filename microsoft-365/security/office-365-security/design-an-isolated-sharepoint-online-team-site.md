---
title: Conception d’un site d’équipe SharePoint Online isolé
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: 'Résumé : Découvrez comment concevoir des sites d’équipe SharePoint Online.'
ms.openlocfilehash: f03df1f99650f458dd9df2c9e561decf491c3011
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083208"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="e4c5b-103">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="e4c5b-103">Design an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="e4c5b-104">**Résumé :** Découvrez comment concevoir des sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-104">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="e4c5b-105">Cet article vous aide à faire les bons choix de conception avant de créer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-105">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="e4c5b-106">Phase 1 : choix des groupes SharePoint et des niveaux d’autorisation</span><span class="sxs-lookup"><span data-stu-id="e4c5b-106">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="e4c5b-107">Chaque site d’équipe SharePoint Online par défaut est créé avec les groupes SharePoint suivants :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-107">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>
  
- <span data-ttu-id="e4c5b-108">\<nom du site> membres</span><span class="sxs-lookup"><span data-stu-id="e4c5b-108">\<site name> Members</span></span>
    
- <span data-ttu-id="e4c5b-109">\<nom du site> visiteurs</span><span class="sxs-lookup"><span data-stu-id="e4c5b-109">\<site name> Visitors</span></span>
    
- <span data-ttu-id="e4c5b-110">\<Propriétaires de nom de site></span><span class="sxs-lookup"><span data-stu-id="e4c5b-110">\<site name> Owners</span></span>
    
<span data-ttu-id="e4c5b-111">Ces groupes sont différents des groupes Office 365 et Azure Active Directory (AD), et permettent d’attribuer des autorisations pour l’utilisation des ressources du site.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-111">These groups are separate from Office 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>
  
<span data-ttu-id="e4c5b-p101">L’ensemble des autorisations qui déterminent ce que le membre d’un groupe SharePoint peut faire dans un site est un niveau d’autorisation. Il existe trois niveaux d’autorisation par défaut pour un site d’équipe SharePoint Online : Modification, Lecture et Contrôle total. Le tableau suivant indique la corrélation par défaut des groupes SharePoint et les niveaux d’autorisation affectés :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p101">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level. There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control. The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>
  
|<span data-ttu-id="e4c5b-115">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-115">**SharePoint group**</span></span>|<span data-ttu-id="e4c5b-116">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-116">**Permission level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4c5b-117">\<nom du site> membres</span><span class="sxs-lookup"><span data-stu-id="e4c5b-117">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e4c5b-118">Edit</span><span class="sxs-lookup"><span data-stu-id="e4c5b-118">Edit</span></span>  <br/> |
|<span data-ttu-id="e4c5b-119">\<nom du site> visiteurs</span><span class="sxs-lookup"><span data-stu-id="e4c5b-119">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="e4c5b-120">Lecture</span><span class="sxs-lookup"><span data-stu-id="e4c5b-120">Read</span></span>  <br/> |
|<span data-ttu-id="e4c5b-121">\<Propriétaires de nom de site></span><span class="sxs-lookup"><span data-stu-id="e4c5b-121">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="e4c5b-122">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="e4c5b-122">Full control</span></span>  <br/> |
   
 <span data-ttu-id="e4c5b-p102">**Conseil :** vous pouvez créer des groupes SharePoint et des niveaux d’autorisation supplémentaires. Cependant, nous vous recommandons d’utiliser les groupes SharePoint par défaut et les niveaux d’autorisation pour votre site SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p102">**Best practice:** You can create additional SharePoint groups and permission levels. However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>
  
<span data-ttu-id="e4c5b-125">Voici les groupes et les niveaux d’autorisation SharePoint par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-125">Here are the default SharePoint groups and permission levels.</span></span>
  
![Les groupes et les niveaux d’autorisation SharePoint par défaut pour un site SharePoint Online.](../../media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="e4c5b-127">Phase 2 : attribution des autorisations aux utilisateurs membres de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="e4c5b-127">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="e4c5b-p103">Vous pouvez attribuer des autorisations aux utilisateurs en ajoutant leur compte d’utilisateur, ou un groupe Office 365 ou Azure AD dont est membre le compte d’utilisateur, aux groupes SharePoint. Une fois ajoutés, les comptes d’utilisateur Office 365 reçoivent, directement ou indirectement via l’appartenance à un groupe Office 365 ou Azure AD, le niveau d’autorisation associé au groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p103">You can assign permissions to users by adding their user account, or an Office 365 or Azure AD group of which the user account is a member, to the SharePoint groups. Once added, the Office 365 user accounts, either directly or indirectly via membership in an Office 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>
  
<span data-ttu-id="e4c5b-130">En prenant l’exemple des groupes SharePoint par défaut :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-130">Using the default SharePoint groups as an example:</span></span>
  
- <span data-ttu-id="e4c5b-131">Les membres du \*\* \<nom du site>\*\* groupe SharePoint membres, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **modifier**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-131">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>
    
- <span data-ttu-id="e4c5b-132">Les membres du \*\* \<nom du site>\*\* groupe SharePoint visiteurs, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **lecture**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-132">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>
    
- <span data-ttu-id="e4c5b-133">Les membres du \*\* \<nom du site>\*\* groupe SharePoint propriétaires, qui peut inclure à la fois des comptes d’utilisateur et des groupes, se voient attribuer le niveau d’autorisation **contrôle total** .</span><span class="sxs-lookup"><span data-stu-id="e4c5b-133">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>
    
 <span data-ttu-id="e4c5b-p104">**Conseil :** même si vous pouvez gérer les autorisations dans chaque compte d’utilisateur, nous vous recommandons plutôt d’utiliser un seul groupe Azure AD, appelé groupe d’accès. Cela simplifie la gestion des autorisations via l’appartenance au groupe d’accès, plutôt que via la gestion de la liste des comptes d’utilisateur pour chaque groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p104">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead. This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>
  
<span data-ttu-id="e4c5b-136">Les groupes Azure AD pour Office 365 sont différents des groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-136">Azure AD groups for Office 365 are different than Office 365 groups.</span></span> <span data-ttu-id="e4c5b-137">Les groupes Azure AD apparaissent dans le centre d’administration 365 de Microsoft, dont le **type** est défini sur **sécurité** et n’ont pas d’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-137">Azure AD groups appear in the Microsoft 365 admin center with their **Type** set to **Security** and do not have an email address.</span></span> <span data-ttu-id="e4c5b-138">Les groupes Azure AD peuvent être gérés dans les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-138">Azure AD groups can be managed within:</span></span>
  
- <span data-ttu-id="e4c5b-139">Services de domaine Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="e4c5b-139">Active Directory Domain Services (AD DS)</span></span>
    
    <span data-ttu-id="e4c5b-140">Il s’agit de groupes qui ont été créés dans votre infrastructure AD DS sur site et synchronisés avec votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-140">These are groups that have been created in your on-premises AD DS infrastructure and synchronized to your Office 365 subscription.</span></span> <span data-ttu-id="e4c5b-141">Dans le centre d’administration 365 de Microsoft, ces groupes ont l' **État** **synchronisé avec Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-141">In the Microsoft 365 admin center, these groups have a **Status** of **Synched with active directory**.</span></span>
    
- <span data-ttu-id="e4c5b-142">Office 365</span><span class="sxs-lookup"><span data-stu-id="e4c5b-142">Office 365</span></span>
    
    <span data-ttu-id="e4c5b-143">Il s’agit de groupes qui ont été créés à l’aide du centre d’administration Microsoft 365, du portail Azure ou de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-143">These are groups that have been created using either the Microsoft 365 admin center, the Azure portal, or Microsoft PowerShell.</span></span> <span data-ttu-id="e4c5b-144">Dans le centre d’administration 365 de Microsoft, ces groupes ont l' **État** **Cloud**.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-144">In the Microsoft 365 admin center, these groups have a **Status** of **Cloud**.</span></span>
    
 <span data-ttu-id="e4c5b-145">**Meilleure pratique :** Si vous utilisez AD DS en local et que vous vous synchronisez avec votre abonnement Office 365, effectuez votre gestion des utilisateurs et des groupes avec AD DS.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-145">**Best practice:** If you are using AD DS on-premises and synchronizing with your Office 365 subscription, perform your user and group management with AD DS.</span></span>
  
<span data-ttu-id="e4c5b-146">Pour les sites d’équipe SharePoint Online isolés, voici à quoi ressemble la structure recommandée du groupe :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-146">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>
  
|<span data-ttu-id="e4c5b-147">**Groupe SharePoint**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-147">**SharePoint group**</span></span>|<span data-ttu-id="e4c5b-148">**Groupe d’accès basé sur Azure AD**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-148">**Azure AD-based access group**</span></span>|<span data-ttu-id="e4c5b-149">**Niveau d’autorisation**</span><span class="sxs-lookup"><span data-stu-id="e4c5b-149">**Permission level**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4c5b-150">\<nom du site> membres</span><span class="sxs-lookup"><span data-stu-id="e4c5b-150">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e4c5b-151">\<nom du site> membres</span><span class="sxs-lookup"><span data-stu-id="e4c5b-151">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e4c5b-152">Edit</span><span class="sxs-lookup"><span data-stu-id="e4c5b-152">Edit</span></span>  <br/> |
|<span data-ttu-id="e4c5b-153">\<nom du site> visiteurs</span><span class="sxs-lookup"><span data-stu-id="e4c5b-153">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="e4c5b-154">\<Visionneuse de nom de site></span><span class="sxs-lookup"><span data-stu-id="e4c5b-154">\<site name> Viewers</span></span>  <br/> |<span data-ttu-id="e4c5b-155">Lire</span><span class="sxs-lookup"><span data-stu-id="e4c5b-155">Read</span></span>  <br/> |
|<span data-ttu-id="e4c5b-156">\<Propriétaires de nom de site></span><span class="sxs-lookup"><span data-stu-id="e4c5b-156">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="e4c5b-157">\<nom du site> administrateurs</span><span class="sxs-lookup"><span data-stu-id="e4c5b-157">\<site name> Admins</span></span>  <br/> |<span data-ttu-id="e4c5b-158">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="e4c5b-158">Full control</span></span>  <br/> |
   
 <span data-ttu-id="e4c5b-159">**Meilleure pratique :** Bien que vous puissiez utiliser les groupes Office 365 ou Azure AD comme membres des groupes SharePoint, nous vous recommandons d’utiliser les groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-159">**Best practice:** Although you can use either Office 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups.</span></span> <span data-ttu-id="e4c5b-160">Les groupes Azure AD, gérés via AD DS ou Office 365, offrent davantage de flexibilité pour l’utilisation de groupes imbriqués pour attribuer des autorisations.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-160">Azure AD groups, managed either through AD DS or Office 365, give you more flexibility to use nested groups to assign permissions.</span></span>
  
<span data-ttu-id="e4c5b-161">Voici les groupes SharePoint par défaut configurés pour utiliser les groupes d’accès basé sur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-161">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>
  
![Utilisation de groupes d’accès en tant que membres des groupes de sites SharePoint Online par défaut.](../../media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
<span data-ttu-id="e4c5b-163">Lorsque vous concevez les trois groupes d’accès, rappelez-vous de ceci :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-163">When designing the three access groups, keep the following in mind:</span></span>
  
- <span data-ttu-id="e4c5b-164">Le \*\* \<nom du site>\*\* groupe d’accès administrateurs ne doit contenir que quelques membres, ce qui correspond à un petit nombre d’administrateurs SharePoint Online qui gèrent le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-164">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>
    
- <span data-ttu-id="e4c5b-165">La plupart des membres de votre site figurent dans le \*\* \<nom du site> les membres\*\* ou \*\* \<le nom du site> les utilisateurs\*\* accèdent aux groupes.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-165">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups.</span></span> <span data-ttu-id="e4c5b-166">Étant donné que les membres du site dans le groupe d’accès \*\* \<nom du site> membres\*\* ont la possibilité de supprimer ou de modifier les ressources du site, il est préférable de prendre en compte son appartenance.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-166">Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership.</span></span> <span data-ttu-id="e4c5b-167">En cas de doute, ajoutez le membre du site au \*\* \<nom du site>\*\* groupe d’accès observateurs.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-167">When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>
    
<span data-ttu-id="e4c5b-168">Voici un exemple des groupes SharePoint et des groupes d’accès pour un site isolé nommé ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-168">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>
  
![Exemple d’utilisation de groupes d’accès pour un site SharePoint Online nommé ProjectX.](../../media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="e4c5b-170">Phase 3 : utiliser des groupes Azure AD imbriqués</span><span class="sxs-lookup"><span data-stu-id="e4c5b-170">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="e4c5b-171">Pour un projet impliquant un petit nombre d’utilisateurs, vous pouvez ajouter, dans la plupart des cas, un seul niveau de groupes d’accès basés sur Azure AD aux groupes SharePoint du site.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-171">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios.</span></span> <span data-ttu-id="e4c5b-172">Toutefois, si vous avez un grand nombre de personnes et que ces personnes sont déjà membres de groupes Azure AD établis, vous pouvez plus facilement attribuer des autorisations SharePoint à l’aide de groupes imbriqués ou de groupes qui contiennent d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-172">However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>
  
<span data-ttu-id="e4c5b-p111">Par exemple, vous souhaitez créer un site d’équipe SharePoint Online isolé pour favoriser la collaboration entre les responsables des services ventes, marketing, ingénierie, juridique et support technique, mais ils ont déjà leur propre groupe de comptes de responsable. Au lieu de créer un groupe pour les nouveaux membres du site et d’y placer tous les comptes de responsable un par un, placez les groupes de responsables existants pour chaque service dans le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p111">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership. Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>
  
 <span data-ttu-id="e4c5b-p112"> Si vous partagez un abonnement Office 365 avec d’autres organisations, il peut s’avérer difficile de gérer un seul niveau de groupe pour le site isolé d’une organisation en raison du nombre important de comptes d’utilisateur. Dans ce cas, vous pouvez utiliser les groupes Azure AD imbriqués pour chaque organisation dont les groupes gèrent les autorisations.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-p112">If you are sharing an Office 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts. In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>
  
<span data-ttu-id="e4c5b-177">Pour utiliser les groupes Azure AD imbriqués, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4c5b-177">To use nested Azure AD groups:</span></span>
  
1. <span data-ttu-id="e4c5b-178">Identifiez ou créez les groupes Azure AD qui contiendront les comptes d’utilisateur et ajoutez les comptes d’utilisateur en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-178">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>
    
2. <span data-ttu-id="e4c5b-179">Créez le groupe d’accès basé sur Azure AD conteneur qui contiendra les autres groupes Azure AD et ajoutez ces groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-179">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>
    
3.  <span data-ttu-id="e4c5b-180"> Pour définir le niveau d’accès approprié pour le groupe d’accès conteneur, identifiez le groupe SharePoint et définissez le niveau d’autorisation correspondant.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-180">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e4c5b-181">Vous ne pouvez pas utiliser des groupes Office 365 imbriqués.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-181">You cannot use nested Office 365 groups.</span></span> 
  
<span data-ttu-id="e4c5b-182">Voici un exemple de groupes Azure AD imbriqués pour le groupe d’accès au membre ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-182">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>
  
![Un exemple d’utilisation de groupes d’accès imbriqués pour le groupe d’accès membres pour le site ProjectX.](../../media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
<span data-ttu-id="e4c5b-184">Étant donné que tous les comptes d’utilisateur dans les équipes de recherche, d’ingénierie et de projet sont destinés à être membres de site, il est plus facile d’ajouter leurs groupes Azure AD au groupe d’accès membres ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e4c5b-184">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="e4c5b-185">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e4c5b-185">Next step</span></span>

<span data-ttu-id="e4c5b-186">Lorsque vous êtes prêt à créer et à configurer un site isolé en production, consultez la rubrique [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="e4c5b-186">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4c5b-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4c5b-187">See Also</span></span>

[<span data-ttu-id="e4c5b-188">Sites d'équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="e4c5b-188">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="e4c5b-189">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="e4c5b-189">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="e4c5b-190">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="e4c5b-190">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



