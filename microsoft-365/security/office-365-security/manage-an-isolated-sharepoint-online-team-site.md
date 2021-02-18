---
title: Gestion d’un site d’équipe SharePoint Online isolé
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: Gérez un site d’équipe SharePoint Online isolé, ajoutez de nouveaux utilisateurs et groupes, supprimez des utilisateurs et des groupes et créez un sous-dossier de documents avec des autorisations personnalisées.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 20e354de77b70ea69d69e201bd3b1d40ea32cc5b
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50289520"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="724ed-103">Gestion d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="724ed-103">Manage an isolated SharePoint Online team site</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="724ed-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="724ed-104">**Applies to**</span></span>
- [<span data-ttu-id="724ed-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="724ed-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="724ed-106">Microsoft Defender pour Office 365 (plan 1)</span><span class="sxs-lookup"><span data-stu-id="724ed-106">Microsoft Defender for Office 365 plan 1</span></span>](office-365-atp.md)
- <span data-ttu-id="724ed-107">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="724ed-107">SharePoint Online</span></span> 

 <span data-ttu-id="724ed-108">**Résumé :** Découvrez comment gérer votre site d'équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="724ed-108">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>

<span data-ttu-id="724ed-109">Cet article vous explique comment gérer un site d’équipe SharePoint Online isolé.</span><span class="sxs-lookup"><span data-stu-id="724ed-109">This article describes common management operations for an isolated SharePoint Online team site.</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="724ed-110">Ajouter un nouvel utilisateur</span><span class="sxs-lookup"><span data-stu-id="724ed-110">Add a new user</span></span>

<span data-ttu-id="724ed-111">Lorsqu’un nouvel utilisateur rejoint le site, vous devez choisir son niveau de participation :</span><span class="sxs-lookup"><span data-stu-id="724ed-111">When someone new joins the site, you must decide their level of participation in the site:</span></span>

- <span data-ttu-id="724ed-112">Administration : ajoutez le compte du nouvel utilisateur au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-112">Administration: Add the new user account to the site admins access group</span></span>

- <span data-ttu-id="724ed-113">Collaboration active : ajoutez le compte de l'utilisateur au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="724ed-113">Active collaboration: Add the user account to the site members access group</span></span>

- <span data-ttu-id="724ed-114">Consultation : ajoutez le compte de l'utilisateur au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-114">Viewing: Add the user account to the site viewers access group</span></span>

<span data-ttu-id="724ed-115">Si vous gérez des comptes d’utilisateurs et des groupes via les services de domaine Active Directory (AD DS), ajoutez les utilisateurs appropriés aux groupes d’accès appropriés à l’aide de vos procédures normales de gestion des utilisateurs et des groupes AD DS et attendez la synchronisation avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="724ed-115">If you are managing user accounts and groups through Active Directory Domain Services (AD DS), add the appropriate users to the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your subscription.</span></span>

<span data-ttu-id="724ed-116">Si vous gérez des comptes d’utilisateurs et des groupes via Microsoft 365, vous pouvez utiliser le Centre d’administration Microsoft 365 ou Microsoft PowerShell :</span><span class="sxs-lookup"><span data-stu-id="724ed-116">If you are managing user accounts and groups through Microsoft 365, you can use the Microsoft 365 admin center or Microsoft PowerShell:</span></span>

- <span data-ttu-id="724ed-117">Pour le Centre d’administration Microsoft 365, connectez-vous avec un compte d’utilisateur ayant le rôle Administrateur de compte d’utilisateur ou Administrateur d’entreprise et utilisez les groupes pour ajouter les utilisateurs appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="724ed-117">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>

- <span data-ttu-id="724ed-118">Pour PowerShell, [connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph.](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="724ed-118">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span> <span data-ttu-id="724ed-119">Pour ajouter un compte d'utilisateur à un groupe d'accès en utilisant son nom d'utilisateur principal (UPN), exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="724ed-119">To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>

```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="724ed-120">Pour ajouter un compte d’utilisateur à un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="724ed-120">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="724ed-121">Ajouter un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="724ed-121">Add a new group</span></span>

<span data-ttu-id="724ed-122">Pour ajouter un accès à un groupe, vous devez choisir le niveau de participation de tous les membres du groupe sur le site :</span><span class="sxs-lookup"><span data-stu-id="724ed-122">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>

- <span data-ttu-id="724ed-123">Administration : ajoutez le groupe d'utilisateurs au groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-123">Administration: Add the group to the site admins access group</span></span>

- <span data-ttu-id="724ed-124">Collaboration active : ajoutez le groupe d'utilisateurs au groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="724ed-124">Active collaboration: Add the group to the site members access group</span></span>

- <span data-ttu-id="724ed-125">Consultation : ajoutez le groupe d'utilisateurs au groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-125">Viewing: Add the group to the site viewers access group</span></span>

<span data-ttu-id="724ed-126">Si vous gérez des comptes d’utilisateurs et des groupes via AD DS, ajoutez les groupes appropriés aux groupes appropriés à l’aide de vos procédures de gestion normales des utilisateurs et des groupes AD DS et attendez la synchronisation avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="724ed-126">If you are managing user accounts and groups through AD DS, add the appropriate groups to the appropriate groups using your normal AD DS user and group management procedures and wait for synchronization with your subscription.</span></span>

<span data-ttu-id="724ed-127">Si vous gérez des comptes d’utilisateurs et des groupes via Office 365, vous pouvez utiliser le Centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="724ed-127">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>

- <span data-ttu-id="724ed-128">Pour le Centre d’administration Microsoft 365, connectez-vous avec un compte d’utilisateur ayant le rôle Administrateur de compte d’utilisateur ou Administrateur d’entreprise et utilisez les groupes pour ajouter les groupes appropriés aux groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="724ed-128">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>

- <span data-ttu-id="724ed-129">Pour PowerShell, [connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph.](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="724ed-129">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
 <span data-ttu-id="724ed-130">Ensuite, utilisez les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="724ed-130">Then, use the following PowerShell commands:</span></span>

```powershell
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="724ed-131">Supprimer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="724ed-131">Remove a user</span></span>

<span data-ttu-id="724ed-132">Lorsque l'accès d'un utilisateur doit être supprimé du site, supprimez-le du groupe d'accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="724ed-132">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>

- <span data-ttu-id="724ed-133">Administration : supprimez le compte d'utilisateur du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-133">Administration: Remove the user account from the site admins access group</span></span>

- <span data-ttu-id="724ed-134">Collaboration active : supprimez le compte d'utilisateur du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="724ed-134">Active collaboration: Remove the user account from the site members access group</span></span>

- <span data-ttu-id="724ed-135">Consultation : supprimez le compte d'utilisateur du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-135">Viewing: Remove the user account from the site viewers access group</span></span>

<span data-ttu-id="724ed-136">Si vous gérez des comptes d’utilisateurs et des groupes via AD DS, supprimez les utilisateurs appropriés des groupes d’accès appropriés à l’aide de vos procédures normales de gestion des utilisateurs et des groupes AD DS et attendez la synchronisation avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="724ed-136">If you are managing user accounts and groups through AD DS, remove the appropriate users from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your subscription.</span></span>

<span data-ttu-id="724ed-137">Si vous gérez des comptes d’utilisateurs et des groupes via Office 365, vous pouvez utiliser le Centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="724ed-137">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>

- <span data-ttu-id="724ed-138">Pour le Centre d’administration Microsoft 365, connectez-vous avec un compte d’utilisateur ayant le rôle Administrateur de compte d’utilisateur ou Administrateur d’entreprise et utilisez des groupes pour supprimer les utilisateurs appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="724ed-138">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>

- <span data-ttu-id="724ed-139">Pour PowerShell, [connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph.](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="724ed-139">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
<span data-ttu-id="724ed-140">Pour supprimer un compte d'utilisateur d'un groupe d'accès en utilisant son UPN, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="724ed-140">To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>

```powershell
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="724ed-141">Pour supprimer un compte d’utilisateur d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="724ed-141">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>

```powershell
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="724ed-142">Supprimer un groupe</span><span class="sxs-lookup"><span data-stu-id="724ed-142">Remove a group</span></span>

<span data-ttu-id="724ed-143">Pour supprimer l’accès d’un groupe, supprimez le groupe du groupe d’accès dont il est membre en fonction de sa participation sur le site :</span><span class="sxs-lookup"><span data-stu-id="724ed-143">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>

- <span data-ttu-id="724ed-144">Administration : supprimez le groupe du groupe d'accès Administrateurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-144">Administration: Remove the group from the site admins access group</span></span>

- <span data-ttu-id="724ed-145">Collaboration active : supprimez le groupe du groupe d'accès Membres du site</span><span class="sxs-lookup"><span data-stu-id="724ed-145">Active collaboration: Remove the group from the site members access group</span></span>

- <span data-ttu-id="724ed-146">Consultation : supprimez le groupe du groupe d'accès Visiteurs du site</span><span class="sxs-lookup"><span data-stu-id="724ed-146">Viewing: Remove the group from the site viewers access group</span></span>

<span data-ttu-id="724ed-147">Si vous gérez des comptes d’utilisateurs et des groupes via Windows Server Active Directory, supprimez les groupes appropriés des groupes d’accès appropriés à l’aide de vos procédures normales de gestion des utilisateurs et des groupes AD DS et attendez la synchronisation avec votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="724ed-147">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal AD DS user and group management procedures and wait for synchronization with your subscription.</span></span>

<span data-ttu-id="724ed-148">Si vous gérez des comptes d’utilisateurs et des groupes via Office 365, vous pouvez utiliser le Centre d’administration Microsoft 365 ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="724ed-148">If you are managing user accounts and groups through Office 365, you can use the Microsoft 365 admin center or PowerShell:</span></span>

- <span data-ttu-id="724ed-149">Pour le Centre d’administration Microsoft 365, connectez-vous avec un compte d’utilisateur ayant le rôle Administrateur de compte d’utilisateur ou Administrateur d’entreprise et utilisez les groupes pour supprimer les groupes appropriés des groupes d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="724ed-149">For the Microsoft 365 admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>

- <span data-ttu-id="724ed-150">Pour PowerShell, [connectez-vous d’abord avec le module Azure Active Directory PowerShell pour Graph.](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="724ed-150">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](../../enterprise/connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
<span data-ttu-id="724ed-151">Pour supprimer un groupe d’un groupe d’accès en utilisant son nom d’affichage, exécutez le bloc de commandes PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="724ed-151">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>

```powershell
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="724ed-152">Création d’un sous-dossier de documents avec des autorisations personnalisées</span><span class="sxs-lookup"><span data-stu-id="724ed-152">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="724ed-p105">Il arrive que des utilisateurs travaillant dans un site isolé aient besoin d'un espace privé pour travailler en équipe. Pour les sites SharePoint Online, vous pouvez créer un sous-dossier dans le dossier Documents du site et affecter des autorisations personnalisées. Les personnes non autorisées ne verront pas ce sous-dossier.</span><span class="sxs-lookup"><span data-stu-id="724ed-p105">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>

<span data-ttu-id="724ed-156">Pour créer un sous-dossier de documents avec des autorisations personnalisées, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="724ed-156">To create a documents subfolder with custom permissions, do the following:</span></span>

1. <span data-ttu-id="724ed-157">Connectez-vous à un compte membre du groupe d’accès Administrateurs pour le site.</span><span class="sxs-lookup"><span data-stu-id="724ed-157">Sign in to an account that is a member of the admins access group for the site.</span></span> <span data-ttu-id="724ed-158">Pour obtenir de l’aide, consultez [Où se connecter à Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="724ed-158">For help, see [Where to sign in to Microsoft 365](https://support.microsoft.com/office/e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>

2. <span data-ttu-id="724ed-159">Accédez au site d'équipe isolé, puis cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="724ed-159">Go to the isolated team site and click **Documents**.</span></span>

3. <span data-ttu-id="724ed-160">Accédez au dossier dans le dossier de documents qui contiendra le sous-dossier bénéficiant d’autorisations personnalisées, créez le dossier, puis ouvrez-le.</span><span class="sxs-lookup"><span data-stu-id="724ed-160">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>

4. <span data-ttu-id="724ed-161">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="724ed-161">Click **Share**.</span></span>

5. <span data-ttu-id="724ed-162">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="724ed-162">Click **Shared with > Advanced**.</span></span>

6. <span data-ttu-id="724ed-163">Cliquez sur **Arrêter l'héritage des autorisations**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="724ed-163">Click **Stop inheriting permissions**, and then click **OK**.</span></span>

7. <span data-ttu-id="724ed-164">Cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="724ed-164">Click **Share**.</span></span>

8. <span data-ttu-id="724ed-165">Cliquez sur **Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="724ed-165">Click **Shared with > Advanced**.</span></span>

9. <span data-ttu-id="724ed-166">Cliquez sur **Accorder des autorisations > Partagé avec > Avancé**.</span><span class="sxs-lookup"><span data-stu-id="724ed-166">Click **Grant Permissions > Shared with > Advanced**.</span></span>

10. <span data-ttu-id="724ed-167">Sur la page Autorisations, cliquez sur **Membres de \<site name>** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="724ed-167">On the permissions page, click **\<site name> Members in the list**.</span></span>

11. <span data-ttu-id="724ed-168">Sur la page **Membres de \<site name>**, cochez la case en regard du groupe d'accès Membres du site, cliquez sur **Actions**, sur **Supprimer des utilisateurs du groupe**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="724ed-168">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>

12. <span data-ttu-id="724ed-169">Pour ajouter des membres à ce sous-dossier, cliquez sur **Nouveau > Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="724ed-169">To add specific members to this subfolder, click **New > Add users**.</span></span>

13. <span data-ttu-id="724ed-170">Dans la boîte de dialogue **Partager**, saisissez les noms des comptes d'utilisateur qui peuvent collaborer sur des fichiers du sous-dossier, puis cliquez sur **Partager**.</span><span class="sxs-lookup"><span data-stu-id="724ed-170">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>

14. <span data-ttu-id="724ed-171">Actualisez la page web pour afficher les nouveaux résultats.</span><span class="sxs-lookup"><span data-stu-id="724ed-171">Refresh the web page to see the new results.</span></span>

15. <span data-ttu-id="724ed-172">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe **Visiteurs de \<site name>** et suivez les étapes 11 à 14 pour indiquer les comptes d'utilisateur qui peuvent afficher les fichiers du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="724ed-172">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>

16. <span data-ttu-id="724ed-173">Sous **Groupes** dans le volet de navigation de gauche, cliquez sur le groupe **Propriétaires de \<site name>** et suivez les étapes 11 à 14 pour indiquer les comptes d'utilisateur qui peuvent gérer les autorisations du sous-dossier (selon vos besoins).</span><span class="sxs-lookup"><span data-stu-id="724ed-173">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>

17. <span data-ttu-id="724ed-174">Fermez l’onglet **Utilisateurs et groupes** dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="724ed-174">Close the **People and Groups** tab in your browser.</span></span>

## <a name="see-also"></a><span data-ttu-id="724ed-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="724ed-175">See Also</span></span>

[<span data-ttu-id="724ed-176">Sites d’équipe SharePoint Online isolés</span><span class="sxs-lookup"><span data-stu-id="724ed-176">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)

[<span data-ttu-id="724ed-177">Conception d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="724ed-177">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="724ed-178">Déploiement d’un site d’équipe SharePoint Online isolé</span><span class="sxs-lookup"><span data-stu-id="724ed-178">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)
