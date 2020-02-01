---
title: Gestion d'un site d'équipe SharePoint Online isolé
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
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: "Résumé : Découvrez comment gérer votre site d'équipe SharePoint Online isolé."
ms.openlocfilehash: 59c86c869ed38c3e64ff19974660cf96ec4c715e
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599001"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="1e7e7-103">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1e7e7-103">Manage an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="1e7e7-104">**Résumé :** Découvrez comment gérer votre site d'équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-104">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>
  
<span data-ttu-id="1e7e7-105">Cet article vous explique comment gérer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-105">This article describes common management operations for an isolated SharePoint Online team site.</span></span>
  
## <a name="add-a-new-user"></a><span data-ttu-id="1e7e7-106">Ajouter un nouvel utilisateur</span><span class="sxs-lookup"><span data-stu-id="1e7e7-106">Add a new user</span></span>

<span data-ttu-id="1e7e7-107">Lorsqu’un nouvel utilisateur rejoint le site, vous devez choisir son niveau de participation :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-107">When someone new joins the site, you must decide their level of participation in the site:</span></span>
  
- <span data-ttu-id="1e7e7-108">Administration : ajoutez le compte du nouvel utilisateur au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-108">Administration: Add the new user account to the site admins access group</span></span>
    
- <span data-ttu-id="1e7e7-109">Collaboration active : ajoutez le compte de l'utilisateur au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-109">Active collaboration: Add the user account to the site members access group</span></span>
    
- <span data-ttu-id="1e7e7-110">Consultation : ajoutez le compte de l'utilisateur au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-110">Viewing: Add the user account to the site viewers access group</span></span>
    
<span data-ttu-id="1e7e7-111">Si vous gérez des comptes d’utilisateur et des groupes par le biais des services de domaine Active Directory (AD DS), ajoutez les utilisateurs appropriés aux groupes d’accès appropriés en utilisant vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-111">If you are managing user accounts and groups through Active Directory Domain Services (AD DS), add the appropriate users to the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="1e7e7-112">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou Microsoft PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-112">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or Microsoft PowerShell:</span></span>
  
- <span data-ttu-id="1e7e7-113">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les utilisateurs appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-113">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>
    
- <span data-ttu-id="1e7e7-114">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-114">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span> <span data-ttu-id="1e7e7-115">Pour ajouter un compte d'utilisateur à un groupe d'accès en utilisant son nom d'utilisateur principal (UPN), exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-115">To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>
    
```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="1e7e7-116">Pour ajouter un compte d’utilisateur à un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-116">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="1e7e7-117">Ajouter un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="1e7e7-117">Add a new group</span></span>

<span data-ttu-id="1e7e7-118">Pour ajouter un accès à un groupe, vous devez choisir le niveau de participation de tous les membres du groupe sur le site :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-118">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>
  
- <span data-ttu-id="1e7e7-119">Administration : ajoutez le groupe d'utilisateurs au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-119">Administration: Add the group to the site admins access group</span></span>
    
- <span data-ttu-id="1e7e7-120">Collaboration active : ajoutez le groupe d'utilisateurs au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-120">Active collaboration: Add the group to the site members access group</span></span>
    
- <span data-ttu-id="1e7e7-121">Consultation : ajoutez le groupe d'utilisateurs au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-121">Viewing: Add the group to the site viewers access group</span></span>
    
<span data-ttu-id="1e7e7-122">Si vous gérez des comptes d’utilisateur et des groupes via AD DS, ajoutez les groupes appropriés aux groupes appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-122">If you are managing user accounts and groups through AD DS, add the appropriate groups to the appropriate groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="1e7e7-123">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-123">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="1e7e7-124">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour ajouter les groupes appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-124">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>
    
- <span data-ttu-id="1e7e7-125">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-125">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
 <span data-ttu-id="1e7e7-126">Ensuite, utilisez les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-126">Then, use the following PowerShell commands:</span></span>
 
```powershell
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="1e7e7-127">Supprimer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="1e7e7-127">Remove a user</span></span>

<span data-ttu-id="1e7e7-128">Lorsque l'accès d'un utilisateur doit être supprimé du site, supprimez-le du groupe d'accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-128">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="1e7e7-129">Administration : supprimez le compte d'utilisateur du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-129">Administration: Remove the user account from the site admins access group</span></span>
    
- <span data-ttu-id="1e7e7-130">Collaboration active : supprimez le compte d'utilisateur du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-130">Active collaboration: Remove the user account from the site members access group</span></span>
    
- <span data-ttu-id="1e7e7-131">Consultation : supprimez le compte d'utilisateur du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-131">Viewing: Remove the user account from the site viewers access group</span></span>
    
<span data-ttu-id="1e7e7-132">Si vous gérez des comptes d’utilisateur et des groupes via AD DS, supprimez les utilisateurs appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales, puis attendez la synchronisation avec votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-132">If you are managing user accounts and groups through AD DS, remove the appropriate users from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="1e7e7-133">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-133">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="1e7e7-134">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les utilisateurs appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-134">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>
    
- <span data-ttu-id="1e7e7-135">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-135">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
<span data-ttu-id="1e7e7-136">Pour supprimer un compte d'utilisateur d'un groupe d'accès en utilisant son UPN, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-136">To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>
    
```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="1e7e7-137">Pour supprimer un compte d’utilisateur d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-137">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>
    
```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="1e7e7-138">Supprimer un groupe</span><span class="sxs-lookup"><span data-stu-id="1e7e7-138">Remove a group</span></span>

<span data-ttu-id="1e7e7-139">Pour supprimer l’accès d’un groupe, supprimez le groupe du groupe d’accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-139">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="1e7e7-140">Administration : supprimez le groupe du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-140">Administration: Remove the group from the site admins access group</span></span>
    
- <span data-ttu-id="1e7e7-141">Collaboration active : supprimez le groupe du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-141">Active collaboration: Remove the group from the site members access group</span></span>
    
- <span data-ttu-id="1e7e7-142">Consultation : supprimez le groupe du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="1e7e7-142">Viewing: Remove the group from the site viewers access group</span></span>
    
<span data-ttu-id="1e7e7-143">Si vous gérez des comptes d’utilisateur et des groupes par le biais de Windows Server Active Directory, supprimez les groupes appropriés des groupes d’accès appropriés à l’aide de vos procédures de gestion des utilisateurs et des groupes AD DS normales et attendez la synchronisation avec votre Office 365 abonnés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-143">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="1e7e7-144">Si vous gérez des comptes d’utilisateur et des groupes via Office 365, vous pouvez utiliser le centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-144">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>
  
- <span data-ttu-id="1e7e7-145">Pour le centre d’administration Microsoft 365, connectez-vous à l’aide d’un compte d’utilisateur auquel a été attribué le rôle administrateur de compte d’utilisateur ou administrateur de société et utilisez des groupes pour supprimer les groupes appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-145">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>
    
- <span data-ttu-id="1e7e7-146">Pour PowerShell, [Connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-146">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>    
<span data-ttu-id="1e7e7-147">Pour supprimer un groupe d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-147">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>
    
```powershell
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="1e7e7-148">Création d’un sous-dossier de documents avec des autorisations personnalisées</span><span class="sxs-lookup"><span data-stu-id="1e7e7-148">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="1e7e7-p104">Il arrive que des utilisateurs travaillant dans un site isolé aient besoin d'un espace privé pour travailler en équipe. Pour les sites SharePoint Online, vous pouvez créer un sous-dossier dans le dossier Documents du site et affecter des autorisations personnalisées. Les personnes non autorisées ne verront pas ce sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-p104">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>
  
<span data-ttu-id="1e7e7-152">Pour créer un sous-dossier de documents avec des autorisations personnalisées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1e7e7-152">To create a documents subfolder with custom permissions, do the following:</span></span>
  
1. <span data-ttu-id="1e7e7-p105">Connectez-vous à Office 365 avec un compte membre du groupe d'accès Administrateurs du site. Pour plus d'informations, consultez la rubrique [Se connecter à Office 365 pour les entreprises](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-p105">Sign in to Office 365 with an account that is a member of the admins access group for the site. For help, see [Where to sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="1e7e7-155">Accédez au site d'équipe isolé, puis cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-155">Go to the isolated team site and click **Documents**.</span></span>
    
3. <span data-ttu-id="1e7e7-156">Accédez au dossier dans le dossier de documents qui contiendra le sous-dossier bénéficiant d’autorisations personnalisées, créez le dossier, puis ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-156">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>
    
4. <span data-ttu-id="1e7e7-157">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-157">Click **Share**.</span></span>
    
5. <span data-ttu-id="1e7e7-158">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-158">Click **Shared with > Advanced**.</span></span>
    
6. <span data-ttu-id="1e7e7-159">Cliquez sur **Arrêter l'héritage des autorisations**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-159">Click **Stop inheriting permissions**, and then click **OK**.</span></span>
    
7. <span data-ttu-id="1e7e7-160">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-160">Click **Share**.</span></span>
    
8. <span data-ttu-id="1e7e7-161">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-161">Click **Shared with > Advanced**.</span></span>
    
9. <span data-ttu-id="1e7e7-162">Cliquez sur **Accorder des autorisations > Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-162">Click **Grant Permissions > Shared with > Advanced**.</span></span>
    
10. <span data-ttu-id="1e7e7-163">Sur la page Autorisations, cliquez sur Membres de **\<nom du site> dans la liste**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-163">On the permissions page, click **\<site name> Members in the list**.</span></span>
    
11. <span data-ttu-id="1e7e7-164">Sur la page Membres de **\<nom du site>**, cochez la case en regard du groupe d’accès Membres du site, cliquez sur **Actions**, sur **Supprimer des utilisateurs du groupe**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-164">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>
    
12. <span data-ttu-id="1e7e7-165">Pour ajouter des membres à ce sous-dossier, cliquez sur **Nouveau > Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-165">To add specific members to this subfolder, click **New > Add users**.</span></span>
    
13. <span data-ttu-id="1e7e7-166">Dans la boîte de dialogue **Partager**, saisissez les noms des comptes d'utilisateur qui peuvent collaborer sur des fichiers du sous-dossier, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-166">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>
    
14. <span data-ttu-id="1e7e7-167">Actualisez la page web pour afficher les nouveaux résultats.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-167">Refresh the web page to see the new results.</span></span>
    
15. <span data-ttu-id="1e7e7-168">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Visiteurs de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent afficher les fichiers du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-168">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>
    
16. <span data-ttu-id="1e7e7-169">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe Propriétaires de **\<nom du site>** et suivez les étapes 11 à 14 pour indiquer les comptes d’utilisateur qui peuvent gérer les autorisations du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="1e7e7-169">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>
    
17. <span data-ttu-id="1e7e7-170">Fermez l’onglet **Utilisateurs et groupes** dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="1e7e7-170">Close the **People and Groups** tab in your browser.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e7e7-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7e7-171">See Also</span></span>

[<span data-ttu-id="1e7e7-172">Sites d’équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="1e7e7-172">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="1e7e7-173">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1e7e7-173">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="1e7e7-174">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="1e7e7-174">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



