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
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: Concevoir des sites d’équipe SharePoint Online isolés, y compris déterminer les niveaux d’autorisation, attribuer des autorisations aux utilisateurs avec des groupes d’accès et des groupes Azure AD imbrmbrés.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: f0f92a925948dbf6c8c5c1beb6b9c709f508c4b3
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50165510"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="8d1c9-103">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="8d1c9-103">Design an isolated SharePoint Online team site</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8d1c9-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8d1c9-104">**Applies to**</span></span>
- [<span data-ttu-id="8d1c9-105">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="8d1c9-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="8d1c9-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8d1c9-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


 <span data-ttu-id="8d1c9-107">**Résumé :** Découvrez comment concevoir des sites d’équipe SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-107">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>

<span data-ttu-id="8d1c9-108">Cet article vous aide à faire les bons choix de conception avant de créer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-108">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>

## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="8d1c9-109">Phase 1 : choix des groupes SharePoint et des niveaux d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8d1c9-109">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="8d1c9-110">Chaque site d’équipe SharePoint Online par défaut est créé avec les groupes SharePoint suivants :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-110">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>

- <span data-ttu-id="8d1c9-111">\<site name> Membres</span><span class="sxs-lookup"><span data-stu-id="8d1c9-111">\<site name> Members</span></span>

- <span data-ttu-id="8d1c9-112">\<site name> Visiteurs</span><span class="sxs-lookup"><span data-stu-id="8d1c9-112">\<site name> Visitors</span></span>

- <span data-ttu-id="8d1c9-113">\<site name> Propriétaires</span><span class="sxs-lookup"><span data-stu-id="8d1c9-113">\<site name> Owners</span></span>

<span data-ttu-id="8d1c9-114">Ces groupes sont distincts des groupes Microsoft 365 et Azure Active Directory (AD) et sont la base de l’affectation d’autorisations pour les ressources du site.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-114">These groups are separate from Microsoft 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>

<span data-ttu-id="8d1c9-p101">L’ensemble des autorisations qui déterminent ce que le membre d’un groupe SharePoint peut faire dans un site est un niveau d’autorisation. Il existe trois niveaux d’autorisation par défaut pour un site d’équipe SharePoint Online : Modification, Lecture et Contrôle total. Le tableau suivant indique la corrélation par défaut des groupes SharePoint et les niveaux d’autorisation affectés :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-p101">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level. There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control. The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>

****

|<span data-ttu-id="8d1c9-118">Groupe SharePoint</span><span class="sxs-lookup"><span data-stu-id="8d1c9-118">SharePoint group</span></span>|<span data-ttu-id="8d1c9-119">Niveau d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8d1c9-119">Permission level</span></span>|
|---|---|
|<span data-ttu-id="8d1c9-120">\<site name> Membres</span><span class="sxs-lookup"><span data-stu-id="8d1c9-120">\<site name> Members</span></span>|<span data-ttu-id="8d1c9-121">Modifier</span><span class="sxs-lookup"><span data-stu-id="8d1c9-121">Edit</span></span>|
|<span data-ttu-id="8d1c9-122">\<site name> Visiteurs</span><span class="sxs-lookup"><span data-stu-id="8d1c9-122">\<site name> Visitors</span></span>|<span data-ttu-id="8d1c9-123">Lire</span><span class="sxs-lookup"><span data-stu-id="8d1c9-123">Read</span></span>|
|<span data-ttu-id="8d1c9-124">\<site name> Propriétaires</span><span class="sxs-lookup"><span data-stu-id="8d1c9-124">\<site name> Owners</span></span>|<span data-ttu-id="8d1c9-125">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="8d1c9-125">Full control</span></span>|
|

 <span data-ttu-id="8d1c9-p102">**Conseil :** vous pouvez créer des groupes SharePoint et des niveaux d’autorisation supplémentaires. Cependant, nous vous recommandons d’utiliser les groupes SharePoint par défaut et les niveaux d’autorisation pour votre site SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-p102">**Best practice:** You can create additional SharePoint groups and permission levels. However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>

<span data-ttu-id="8d1c9-128">Voici les groupes et les niveaux d’autorisation SharePoint par défaut.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-128">Here are the default SharePoint groups and permission levels.</span></span>

![Groupes Et niveaux d’autorisation SharePoint par défaut pour un site SharePoint Online.](../../media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)

## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="8d1c9-130">Phase 2 : attribution des autorisations aux utilisateurs membres de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="8d1c9-130">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="8d1c9-131">Vous pouvez attribuer des autorisations aux utilisateurs en ajoutant leur compte d’utilisateur, ou un groupe Microsoft 365 ou Azure AD dont le compte d’utilisateur est membre, aux groupes SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-131">You can assign permissions to users by adding their user account, or a Microsoft 365 or Azure AD group of which the user account is a member, to the SharePoint groups.</span></span> <span data-ttu-id="8d1c9-132">Une fois ajoutés, les comptes d’utilisateurs, directement ou indirectement via l’appartenance à un groupe Microsoft 365 ou Azure AD, se voient attribuer le niveau d’autorisation associé au groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-132">Once added, the user accounts, either directly or indirectly via membership in a Microsoft 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>

<span data-ttu-id="8d1c9-133">En prenant l’exemple des groupes SharePoint par défaut :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-133">Using the default SharePoint groups as an example:</span></span>

- <span data-ttu-id="8d1c9-134">Le niveau **\<site name> d’autorisation** Modifier est attribué aux membres du groupe  SharePoint Membres, qui peut inclure des comptes d’utilisateur et des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-134">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>

- <span data-ttu-id="8d1c9-135">Le niveau  d’autorisation Lecture est attribué aux membres du groupe Visiteurs SharePoint, qui peut inclure des comptes d’utilisateur et des groupes. **\<site name>**</span><span class="sxs-lookup"><span data-stu-id="8d1c9-135">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>

- <span data-ttu-id="8d1c9-136">Le niveau  d’autorisation Contrôle total est attribué aux membres du groupe SharePoint Propriétaires, qui peut inclure des comptes d’utilisateur et des groupes. **\<site name>**</span><span class="sxs-lookup"><span data-stu-id="8d1c9-136">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>

 <span data-ttu-id="8d1c9-p104">**Conseil :** même si vous pouvez gérer les autorisations dans chaque compte d’utilisateur, nous vous recommandons plutôt d’utiliser un seul groupe Azure AD, appelé groupe d’accès. Cela simplifie la gestion des autorisations via l’appartenance au groupe d’accès, plutôt que via la gestion de la liste des comptes d’utilisateur pour chaque groupe SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-p104">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead. This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>

<span data-ttu-id="8d1c9-139">Les groupes Azure AD pour Microsoft 365 sont différents groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-139">Azure AD groups for Microsoft 365 are different tha Microsoft 365 groups.</span></span> <span data-ttu-id="8d1c9-140">Les groupes Azure AD apparaissent dans le Centre d’administration Microsoft 365 avec leur **type** de sécurité et n’ont pas d’adresse de messagerie. </span><span class="sxs-lookup"><span data-stu-id="8d1c9-140">Azure AD groups appear in the Microsoft 365 admin center with their **Type** set to **Security** and do not have an email address.</span></span> <span data-ttu-id="8d1c9-141">Les groupes Azure AD peuvent être gérés dans :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-141">Azure AD groups can be managed within:</span></span>

- <span data-ttu-id="8d1c9-142">Services de domaine Active Directory (AD DS) ;</span><span class="sxs-lookup"><span data-stu-id="8d1c9-142">Active Directory Domain Services (AD DS)</span></span>

    <span data-ttu-id="8d1c9-143">Il s’agit de groupes qui ont été créés dans votre infrastructure AD DS locale et synchronisés avec votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-143">These are groups that have been created in your on-premises AD DS infrastructure and synchronized to your Microsoft 365 subscription.</span></span> <span data-ttu-id="8d1c9-144">Dans le Centre d’administration Microsoft 365, ces groupes ont l’état Synchronisé **avec Active Directory.** </span><span class="sxs-lookup"><span data-stu-id="8d1c9-144">In the Microsoft 365 admin center, these groups have a **Status** of **Synched with active directory**.</span></span>

- <span data-ttu-id="8d1c9-145">Office 365</span><span class="sxs-lookup"><span data-stu-id="8d1c9-145">Office 365</span></span>

    <span data-ttu-id="8d1c9-146">Ce sont des groupes qui ont été créés à l’aide du Centre d’administration Microsoft 365, du portail Azure ou de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-146">These are groups that have been created using either the Microsoft 365 admin center, the Azure portal, or Microsoft PowerShell.</span></span> <span data-ttu-id="8d1c9-147">Dans le Centre d’administration Microsoft 365, ces groupes ont **l’état** **Cloud.**</span><span class="sxs-lookup"><span data-stu-id="8d1c9-147">In the Microsoft 365 admin center, these groups have a **Status** of **Cloud**.</span></span>

 <span data-ttu-id="8d1c9-148">**Meilleure pratique :** Si vous utilisez AD DS en local et que vous effectuez une synchronisation avec votre abonnement Microsoft 365, effectuez la gestion de vos utilisateurs et groupes avec AD DS.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-148">**Best practice:** If you are using AD DS on-premises and synchronizing with your Microsoft 365 subscription, perform your user and group management with AD DS.</span></span>

<span data-ttu-id="8d1c9-149">Pour les sites d’équipe SharePoint Online isolés, voici à quoi ressemble la structure recommandée du groupe :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-149">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>

****

|<span data-ttu-id="8d1c9-150">Groupe SharePoint</span><span class="sxs-lookup"><span data-stu-id="8d1c9-150">SharePoint group</span></span>|<span data-ttu-id="8d1c9-151">Groupe d’accès basé sur Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d1c9-151">Azure AD-based access group</span></span>|<span data-ttu-id="8d1c9-152">Niveau d’autorisation</span><span class="sxs-lookup"><span data-stu-id="8d1c9-152">Permission level</span></span>|
|---|---|---|
|<span data-ttu-id="8d1c9-153">\<site name> Membres</span><span class="sxs-lookup"><span data-stu-id="8d1c9-153">\<site name> Members</span></span>|<span data-ttu-id="8d1c9-154">\<site name> Membres</span><span class="sxs-lookup"><span data-stu-id="8d1c9-154">\<site name> Members</span></span>|<span data-ttu-id="8d1c9-155">Modifier</span><span class="sxs-lookup"><span data-stu-id="8d1c9-155">Edit</span></span>|
|<span data-ttu-id="8d1c9-156">\<site name> Visiteurs</span><span class="sxs-lookup"><span data-stu-id="8d1c9-156">\<site name> Visitors</span></span>|<span data-ttu-id="8d1c9-157">\<site name> Visionneuses</span><span class="sxs-lookup"><span data-stu-id="8d1c9-157">\<site name> Viewers</span></span>|<span data-ttu-id="8d1c9-158">Lire</span><span class="sxs-lookup"><span data-stu-id="8d1c9-158">Read</span></span>|
|<span data-ttu-id="8d1c9-159">\<site name> Propriétaires</span><span class="sxs-lookup"><span data-stu-id="8d1c9-159">\<site name> Owners</span></span>|<span data-ttu-id="8d1c9-160">\<site name> Administrateurs</span><span class="sxs-lookup"><span data-stu-id="8d1c9-160">\<site name> Admins</span></span>|<span data-ttu-id="8d1c9-161">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="8d1c9-161">Full control</span></span>|
|

 <span data-ttu-id="8d1c9-162">**Meilleure pratique :** Bien que vous pouvez utiliser des groupes Microsoft 365 ou Azure AD en tant que membres de groupes SharePoint, nous vous recommandons d’utiliser des groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-162">**Best practice:** Although you can use either Microsoft 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups.</span></span> <span data-ttu-id="8d1c9-163">Les groupes Azure AD, gérés via AD DS ou Microsoft 365, vous offrent plus de flexibilité pour utiliser des groupes imbrmbrés afin d’attribuer des autorisations.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-163">Azure AD groups, managed either through AD DS or Microsoft 365, give you more flexibility to use nested groups to assign permissions.</span></span>

<span data-ttu-id="8d1c9-164">Voici les groupes SharePoint par défaut configurés pour utiliser les groupes d’accès basés sur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-164">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>

![Utilisation de groupes d’accès en tant que membres des groupes de sites SharePoint Online par défaut.](../../media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)

<span data-ttu-id="8d1c9-166">Lorsque vous concevez les trois groupes d’accès, rappelez-vous de ceci :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-166">When designing the three access groups, keep the following in mind:</span></span>

- <span data-ttu-id="8d1c9-167">Il ne doit y avoir que quelques membres dans le groupe d’accès **\<site name> Administrateurs,** correspondant à un petit nombre d’administrateurs SharePoint Online qui gèrent le site d’équipe.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-167">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>

- <span data-ttu-id="8d1c9-168">La plupart des membres de votre site font partie des groupes **\<site name> d’accès Membres** **ou \<site name>** Visionneuses.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-168">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups.</span></span> <span data-ttu-id="8d1c9-169">Étant donné que les membres du site dans le groupe d’accès **\<site name> Membres** ont la possibilité de supprimer ou de modifier des ressources dans le site, réfléchissez bien à son appartenance.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-169">Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership.</span></span> <span data-ttu-id="8d1c9-170">En cas de doute, ajoutez le membre du site au groupe **\<site name> d’accès Visionneuses.**</span><span class="sxs-lookup"><span data-stu-id="8d1c9-170">When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>

<span data-ttu-id="8d1c9-171">Voici un exemple des groupes SharePoint et des groupes d’accès pour un site isolé nommé ProjectX.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-171">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>

![Exemple d’utilisation de groupes d’accès pour un site SharePoint Online nommé ProjectX.](../../media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)

## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="8d1c9-173">Phase 3 : Utiliser des groupes Azure AD imbrmbrés</span><span class="sxs-lookup"><span data-stu-id="8d1c9-173">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="8d1c9-174">Pour un projet impliquant un petit nombre d’utilisateurs, vous pouvez ajouter, dans la plupart des cas, un seul niveau de groupes d’accès basés sur Azure AD aux groupes SharePoint du site.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-174">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios.</span></span> <span data-ttu-id="8d1c9-175">Toutefois, si vous avez un grand nombre de personnes et que ces personnes sont déjà membres de groupes Azure AD établis, vous pouvez plus facilement attribuer des autorisations SharePoint à l’aide de groupes imbrmbrés ou de groupes qui contiennent d’autres groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-175">However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>

<span data-ttu-id="8d1c9-p111">Par exemple, vous souhaitez créer un site d’équipe SharePoint Online isolé pour favoriser la collaboration entre les responsables des services ventes, marketing, ingénierie, juridique et support technique, mais ils ont déjà leur propre groupe de comptes de responsable. Au lieu de créer un groupe pour les nouveaux membres du site et d’y placer tous les comptes de responsable un par un, placez les groupes de responsables existants pour chaque service dans le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-p111">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership. Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>

 <span data-ttu-id="8d1c9-178">Si vous partagez un abonnement Microsoft 365 entre plusieurs organisations, un seul niveau d’appartenance à un groupe pour un site isolé d’une organisation peut devenir difficile à gérer en raison du nombre important de comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-178">If you are sharing a Microsoft 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts.</span></span> <span data-ttu-id="8d1c9-179">Dans ce cas, vous pouvez utiliser les groupes Azure AD imbriqués pour chaque organisation dont les groupes gèrent les autorisations.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-179">In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>

<span data-ttu-id="8d1c9-180">Pour utiliser les groupes Azure AD imbriqués, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d1c9-180">To use nested Azure AD groups:</span></span>

1. <span data-ttu-id="8d1c9-181">Identifiez ou créez les groupes Azure AD qui contiendront les comptes d’utilisateur et ajoutez les comptes d’utilisateur en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-181">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>

2. <span data-ttu-id="8d1c9-182">Créez le groupe d’accès basé sur Azure AD conteneur qui contiendra les autres groupes Azure AD et ajoutez ces groupes en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-182">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>

3. <span data-ttu-id="8d1c9-183"> Pour définir le niveau d’accès approprié pour le groupe d’accès conteneur, identifiez le groupe SharePoint et définissez le niveau d’autorisation correspondant.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-183">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>

> [!NOTE]
> <span data-ttu-id="8d1c9-184">Vous ne pouvez pas utiliser les groupes Microsoft 365 imbrmbrés.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-184">You cannot use nested Microsoft 365 groups.</span></span>

<span data-ttu-id="8d1c9-185">Voici un exemple de groupes Azure AD imbrmbrés pour le groupe d’accès aux membres ProjectX.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-185">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>

![Exemple d’utilisation de groupes d’accès imbrmbrés pour le groupe d’accès Membres pour le site ProjectX.](../../media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)

<span data-ttu-id="8d1c9-187">Étant donné que tous les comptes d’utilisateur des équipes responsables de la recherche, de l’ingénierie et du projet sont destinés à être membres du site, il est plus facile d’ajouter leurs groupes Azure AD au groupe d’accès Membres ProjectX.</span><span class="sxs-lookup"><span data-stu-id="8d1c9-187">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>

## <a name="next-step"></a><span data-ttu-id="8d1c9-188">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="8d1c9-188">Next step</span></span>

<span data-ttu-id="8d1c9-189">Lorsque vous êtes prêt à créer et à configurer un site isolé en production, consultez la rubrique [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="8d1c9-189">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8d1c9-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d1c9-190">See Also</span></span>

[<span data-ttu-id="8d1c9-191">Sites d'équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="8d1c9-191">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)

[<span data-ttu-id="8d1c9-192">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="8d1c9-192">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="8d1c9-193">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="8d1c9-193">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)
