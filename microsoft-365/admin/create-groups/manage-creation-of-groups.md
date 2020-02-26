---
title: Gérer les personnes autorisées à créer des groupes Office 365
f1.keywords:
- NOCSH
ms.author: mikeplum
ms.reviewer: arvaradh
author: MikePlumleyMSFT
manager: pamgreen
audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MSP160
- MST160
- MET150
- MOE150
ms.assetid: 4c46c8cb-17d0-44b5-9776-005fced8e618
description: Découvrez comment contrôler quels utilisateurs peuvent créer des groupes Office 365.
ms.openlocfilehash: a211cb3b69348a4d4a401a3c318fe019d8fd257f
ms.sourcegitcommit: 109b44aa71bb8453d0a602663df0fcf7ed7dfdbe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2020
ms.locfileid: "42277191"
---
# <a name="manage-who-can-create-office-365-groups"></a><span data-ttu-id="02b50-103">Gérer les personnes autorisées à créer des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="02b50-103">Manage who can create Office 365 Groups</span></span>

  
<span data-ttu-id="02b50-104">Étant donné que les utilisateurs peuvent créer facilement des groupes Office 365, vous n'êtes pas submergé par des demandes de création de la part d'autres personnes.</span><span class="sxs-lookup"><span data-stu-id="02b50-104">Because it's so easy for users to create Office 365 Groups, you aren't inundated with requests to create them on behalf of other people.</span></span> <span data-ttu-id="02b50-105">Toutefois, en fonction de votre activité, vous souhaiterez peut-être contrôler les personnes autorisées à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-105">Depending on your business, however, you might want to control who has the ability to create groups.</span></span>
  
<span data-ttu-id="02b50-106">Cet article vous explique comment désactiver la possibilité de créer des groupes **dans tous les services Office 365 qui utilisent les groupes**:</span><span class="sxs-lookup"><span data-stu-id="02b50-106">This article explains how to disable the ability to create groups **in all Office 365 services that use groups**:</span></span> 
  
- <span data-ttu-id="02b50-107">Outlook</span><span class="sxs-lookup"><span data-stu-id="02b50-107">Outlook</span></span>
    
- <span data-ttu-id="02b50-108">SharePoint</span><span class="sxs-lookup"><span data-stu-id="02b50-108">SharePoint</span></span>
    
- <span data-ttu-id="02b50-109">Yammer</span><span class="sxs-lookup"><span data-stu-id="02b50-109">Yammer</span></span>
    
- <span data-ttu-id="02b50-110">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="02b50-110">Microsoft Teams</span></span>

- <span data-ttu-id="02b50-111">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="02b50-111">Microsoft Stream</span></span>
    
- <span data-ttu-id="02b50-112">StaffHub</span><span class="sxs-lookup"><span data-stu-id="02b50-112">StaffHub</span></span>
    
- <span data-ttu-id="02b50-113">Planificateur</span><span class="sxs-lookup"><span data-stu-id="02b50-113">Planner</span></span>
    
- <span data-ttu-id="02b50-114">PowerBI</span><span class="sxs-lookup"><span data-stu-id="02b50-114">PowerBI</span></span>

- <span data-ttu-id="02b50-115">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="02b50-115">Roadmap</span></span>
    
<span data-ttu-id="02b50-116">Vous pouvez restreindre la création de groupe Office 365 aux membres d’un groupe de sécurité particulier.</span><span class="sxs-lookup"><span data-stu-id="02b50-116">You can restrict Office 365 Group creation to the members of a particular security group.</span></span> <span data-ttu-id="02b50-117">Pour configurer ce, utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02b50-117">To configure this, you use Windows PowerShell.</span></span> <span data-ttu-id="02b50-118">Cet article vous guide tout au long des étapes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="02b50-118">This article walks you through the needed steps.</span></span>
  
<span data-ttu-id="02b50-119">Les étapes décrites dans cet article n’empêchent pas les membres de certains rôles de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-119">The steps in this article won't prevent members of certain roles from creating Groups.</span></span> <span data-ttu-id="02b50-120">Les administrateurs globaux Office 365 peuvent créer des groupes via n’importe quel moyen, comme le centre d’administration Microsoft 365, le planificateur, teams, Exchange et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="02b50-120">Office 365 Global admins can create Groups via any means, such as the Microsoft 365 admin center, Planner, Teams, Exchange, and SharePoint Online.</span></span> <span data-ttu-id="02b50-121">D’autres rôles peuvent créer des groupes via des moyens limités, présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="02b50-121">Other roles can create Groups via limited means, listed below.</span></span>
        
  - <span data-ttu-id="02b50-122">Administrateur Exchange : Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-122">Exchange Administrator: Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="02b50-123">Prise en charge du niveau 1 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-123">Partner Tier 1 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="02b50-124">Prise en charge du niveau 2 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-124">Partner Tier 2 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="02b50-125">Writers d’annuaire : Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-125">Directory Writers: Azure AD</span></span>

  - <span data-ttu-id="02b50-126">Administrateur SharePoint : Centre d’administration SharePoint, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-126">SharePoint Administrator: SharePoint Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="02b50-127">Administrateur de service teams : Centre d’administration Teams, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-127">Teams Service Administrator: Teams Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="02b50-128">Administrateur de gestion des utilisateurs : Centre d’administration Microsoft 365, Yammer, Azure AD</span><span class="sxs-lookup"><span data-stu-id="02b50-128">User Management Administrator: Microsoft 365 Admin center, Yammer, Azure AD</span></span>
     
<span data-ttu-id="02b50-129">Si vous êtes membre de l'un de ces rôles, vous pouvez créer des Groupes Office 365 pour un utilisateur avec accès restreint, puis attribuer le statut de propriétaire du groupe à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="02b50-129">If you're a member of one of these roles, you can create Office 365 Groups for restricted users, and then assign the user as the owner of the group.</span></span> <span data-ttu-id="02b50-130">Les utilisateurs qui ont ce rôle peuvent créer des groupes connectés dans Yammer, indépendamment des paramètres PowerShell susceptibles d’empêcher la création.</span><span class="sxs-lookup"><span data-stu-id="02b50-130">Users that have this role are able to create connected groups in Yammer, regardless of any PowerShell settings that might prevent creation.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="02b50-131">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="02b50-131">Licensing requirements</span></span>

<span data-ttu-id="02b50-132">Pour gérer la personne qui crée des groupes, les personnes suivantes ont besoin de licences Azure AD Premium ou d’Azure AD base EDU qui leur sont attribuées :</span><span class="sxs-lookup"><span data-stu-id="02b50-132">To manage who creates Groups, the following people need Azure AD Premium licenses or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="02b50-133">Administrateur qui configure ces paramètres de création de groupe</span><span class="sxs-lookup"><span data-stu-id="02b50-133">The admin who configures these group creation settings</span></span>
- <span data-ttu-id="02b50-134">Les membres du groupe de sécurité autorisés à créer des groupes</span><span class="sxs-lookup"><span data-stu-id="02b50-134">The members of the security group who are allowed to create Groups</span></span>

<span data-ttu-id="02b50-135">Les personnes suivantes n’ont pas besoin de posséder des licences Azure ad Premium ou EDU AD basique EDU :</span><span class="sxs-lookup"><span data-stu-id="02b50-135">The following people don't need Azure AD Premium or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="02b50-136">Personnes membres des groupes Office 365 et qui ne peuvent pas créer d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-136">People who are members of Office 365 groups and who don't have the ability to create other groups.</span></span>

## <a name="step-1-create-a-security-group-for-users-who-need-to-create-office-365-groups"></a><span data-ttu-id="02b50-137">Étape 1 : créer un groupe de sécurité pour des utilisateurs qui ont besoin de créer des Groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="02b50-137">Step 1: Create a security group for users who need to create Office 365 Groups</span></span>

<span data-ttu-id="02b50-138">Un seul groupe de sécurité dans votre organisation peut être utilisé pour contrôler qui est en mesure de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-138">Only one security group in your organization can be used to control who is able to create Groups.</span></span> <span data-ttu-id="02b50-139">Toutefois, vous pouvez imbriquer d'autres groupes de sécurité en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="02b50-139">But, you can nest other security groups as members of this group.</span></span> <span data-ttu-id="02b50-140">Par exemple, le groupe intitulé « Autoriser la création de groupes » est le groupe de sécurité désigné, et les groupes intitulés Utilisateurs du Planificateur Microsoft et Utilisateurs d'Exchange Online sont membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="02b50-140">For example, the group named Allow Group Creation is the designated security group, and the groups named Microsoft Planner Users and Exchange Online Users are members of that group.</span></span>

<span data-ttu-id="02b50-141">Les administrateurs appartenant aux rôles mentionnés ci-dessus n’ont pas besoin d’être membres de ce groupe : ils conservent leur capacité à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-141">Admins in the roles listed above do not need to be members of this group: they retain their ability to create groups.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="02b50-142">Veillez à utiliser un **groupe de sécurité** pour limiter les personnes autorisées à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-142">Be sure to use a **security group** to restrict who can create groups.</span></span> <span data-ttu-id="02b50-143">Si vous essayez d'utiliser un groupe Office 365, les membres ne pourront pas créer de groupe à partir de SharePoint, car ce service vérifie l'existence d'un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="02b50-143">If you try to use an Office 365 Group, members won't be able to create a group from SharePoint because it checks for a security group.</span></span> 
    
1. <span data-ttu-id="02b50-144">Dans le centre d’administration, accédez \> à **la page groupes de** <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes.</a></span><span class="sxs-lookup"><span data-stu-id="02b50-144">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>

2. <span data-ttu-id="02b50-145">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="02b50-145">Click on **Add a Group**.</span></span>

3. <span data-ttu-id="02b50-146">Choisissez **Security** comme type de groupe.</span><span class="sxs-lookup"><span data-stu-id="02b50-146">Choose **Security** as the group type.</span></span> <span data-ttu-id="02b50-147">Notez bien le nom du groupe !</span><span class="sxs-lookup"><span data-stu-id="02b50-147">Remember the name of the group!</span></span> <span data-ttu-id="02b50-148">Vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="02b50-148">You'll need it later.</span></span>
  
4. <span data-ttu-id="02b50-149">Terminez la configuration du groupe de sécurité, en ajoutant des personnes ou d’autres groupes de sécurité qui doivent être en mesure de créer des groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02b50-149">Finish setting up the security group, adding people or other security groups who you want to be able to create Groups in your org.</span></span>
    
<span data-ttu-id="02b50-150">Pour obtenir des instructions détaillées, reportez-vous à [créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration 365 de Microsoft](../email/create-edit-or-delete-a-security-group.md).</span><span class="sxs-lookup"><span data-stu-id="02b50-150">For detailed instructions, see [Create, edit, or delete a security group in the Microsoft 365 admin center](../email/create-edit-or-delete-a-security-group.md).</span></span>
  
## <a name="step-2-install-the-preview-version-of-the-azure-active-directory-powershell-for-graph"></a><span data-ttu-id="02b50-151">Étape 2 : installer la version d’évaluation d’Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="02b50-151">Step 2: Install the preview version of the Azure Active Directory PowerShell for Graph</span></span>

<span data-ttu-id="02b50-152">Ces procédures nécessitent la version préliminaire d’Azure Active Directory PowerShell pour Graph.</span><span class="sxs-lookup"><span data-stu-id="02b50-152">These procedures require the preview version of the Azure Active Directory PowerShell for Graph.</span></span> <span data-ttu-id="02b50-153">La version GA ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="02b50-153">The GA version will not work.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="02b50-154">Vous ne pouvez pas installer simultanément les versions aperçu et GA sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02b50-154">You cannot install both the preview and GA versions on the same computer at the same time.</span></span> <span data-ttu-id="02b50-155">Vous pouvez installer le module sur Windows 10, Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="02b50-155">You can install the module on Windows 10, Windows Server 2016.</span></span>

  
<span data-ttu-id="02b50-156">Pour obtenir les meilleurs résultats, nous vous recommandons de  *toujours*  être à jour : désinstallez l'ancienne version d'AzureADPreview ou AzureAD, et téléchargez la plus récente.</span><span class="sxs-lookup"><span data-stu-id="02b50-156">As a best practice, we recommend  *always*  staying current: uninstall the old AzureADPreview or old AzureAD version and get the latest one.</span></span> 
  
1. <span data-ttu-id="02b50-157">Dans la barre de recherche, tapez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02b50-157">In your search bar, type Windows PowerShell.</span></span>
    
2. <span data-ttu-id="02b50-158">Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="02b50-158">Right-click on **Windows PowerShell** and select **Run as Administrator**.</span></span>
    
    ![Ouvrez PowerShell avec « Exécuter en tant qu'administrateur ».](../media/52517af8-c7b0-4c8f-b2f3-0f82f9d5ace1.png)
    
3. <span data-ttu-id="02b50-160">Définissez la stratégie sur RemoteSigned à l’aide de [Set-ExecutionPolicy](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy).</span><span class="sxs-lookup"><span data-stu-id="02b50-160">Set the policy to RemoteSigned by using [Set-ExecutionPolicy](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy).</span></span>
    
    ```
    Set-ExecutionPolicy RemoteSigned
    ```
  
4. <span data-ttu-id="02b50-161">Vérifiez le module installé :</span><span class="sxs-lookup"><span data-stu-id="02b50-161">Check installed module:</span></span>
    
    ```
    Get-InstalledModule -Name "AzureAD*"
    ```

5. <span data-ttu-id="02b50-162">Pour désinstaller une version précédente de AzureADPreview ou AzureAD, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="02b50-162">To uninstall a previous version of AzureADPreview or AzureAD, run this command:</span></span>
  
    ```
    Uninstall-Module AzureADPreview
    ```

    <span data-ttu-id="02b50-163">ou</span><span class="sxs-lookup"><span data-stu-id="02b50-163">or</span></span>
  
    ```
    Uninstall-Module AzureAD
    ```

6. <span data-ttu-id="02b50-164">To install the latest version of AzureADPreview, run this command:</span><span class="sxs-lookup"><span data-stu-id="02b50-164">To install the latest version of AzureADPreview, run this command:</span></span>
  
    ```
    Install-Module AzureADPreview
    ```

    <span data-ttu-id="02b50-165">At the message about an untrusted repository, type **Y**. It will take a minute or so for the new module to install. </span><span class="sxs-lookup"><span data-stu-id="02b50-165">At the message about an untrusted repository, type **Y**. It will take a minute or so for the new module to install.</span></span>

<span data-ttu-id="02b50-166">Laissez la fenêtre PowerShell ouverte à l’étape 3, ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="02b50-166">Leave the PowerShell window open for Step 3, below.</span></span>
  
## <a name="step-3-run-powershell-commands"></a><span data-ttu-id="02b50-167">Étape 3 : exécuter les commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="02b50-167">Step 3: Run PowerShell commands</span></span>

<span data-ttu-id="02b50-168">Copiez le script ci-dessous dans un éditeur de texte, tel que le bloc-notes, ou [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span><span class="sxs-lookup"><span data-stu-id="02b50-168">Copy the script below into a text editor, such as Notepad, or the [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span></span>

<span data-ttu-id="02b50-169">Remplacez \* \<SecurityGroupName\> \* par le nom du groupe de sécurité que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="02b50-169">Replace *\<SecurityGroupName\>* with the name of the security group that you created.</span></span> <span data-ttu-id="02b50-170">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="02b50-170">For example:</span></span>

`$GroupName = "Group Creators"`

<span data-ttu-id="02b50-171">Enregistrez le fichier sous le GroupCreators. ps1.</span><span class="sxs-lookup"><span data-stu-id="02b50-171">Save the file as GroupCreators.ps1.</span></span> 

<span data-ttu-id="02b50-172">Dans la fenêtre PowerShell, accédez à l’emplacement où vous avez enregistré le fichier (tapez « <FileLocation>CD »).</span><span class="sxs-lookup"><span data-stu-id="02b50-172">In the PowerShell window, navigate to the location where you saved the file (type "CD <FileLocation>").</span></span>

<span data-ttu-id="02b50-173">Exécutez le script en tapant :</span><span class="sxs-lookup"><span data-stu-id="02b50-173">Run the script by typing:</span></span>

`.\GroupCreators.ps1`

<span data-ttu-id="02b50-174">Lorsque vous y êtes invité, [Connectez-vous avec votre compte d’administrateur](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#step-2-connect-to-azure-ad-for-your-office-365-subscription) .</span><span class="sxs-lookup"><span data-stu-id="02b50-174">and [sign in with your administrator account](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#step-2-connect-to-azure-ad-for-your-office-365-subscription) when prompted.</span></span>

```PowerShell
$GroupName = "<SecurityGroupName>"
$AllowGroupCreation = "False"

Connect-AzureAD

$settingsObjectID = (Get-AzureADDirectorySetting | Where-object -Property Displayname -Value "Group.Unified" -EQ).id
if(!$settingsObjectID)
{
      $template = Get-AzureADDirectorySettingTemplate | Where-object {$_.displayname -eq "group.unified"}
    $settingsCopy = $template.CreateDirectorySetting()
    New-AzureADDirectorySetting -DirectorySetting $settingsCopy
    $settingsObjectID = (Get-AzureADDirectorySetting | Where-object -Property Displayname -Value "Group.Unified" -EQ).id
}

$settingsCopy = Get-AzureADDirectorySetting -Id $settingsObjectID
$settingsCopy["EnableGroupCreation"] = $AllowGroupCreation

if($GroupName)
{
    $settingsCopy["GroupCreationAllowedGroupId"] = (Get-AzureADGroup -SearchString $GroupName).objectid
}
 else {
$settingsCopy["GroupCreationAllowedGroupId"] = $GroupName
}
Set-AzureADDirectorySetting -Id $settingsObjectID -DirectorySetting $settingsCopy

(Get-AzureADDirectorySetting -Id $settingsObjectID).Values
```

<span data-ttu-id="02b50-175">La dernière ligne du script affiche les paramètres mis à jour :</span><span class="sxs-lookup"><span data-stu-id="02b50-175">The last line of the script will display the updated settings:</span></span>

![This is what your settings will look like when you're done.](../media/952cd982-5139-4080-9add-24bafca0830c.png)

<span data-ttu-id="02b50-177">Si, à l’avenir, vous souhaitez modifier le groupe de sécurité utilisé, vous pouvez réexécuter le script avec le nom du nouveau groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="02b50-177">If in the future you want to change which security group is used, you can rerun the script with the name of the new security group.</span></span>

<span data-ttu-id="02b50-178">Si vous souhaitez désactiver la restriction de création de groupe et permettre à tous les utilisateurs de créer des groupes, définissez $GroupName sur "" et $AllowGroupCreation sur "true", puis réexécutez le script.</span><span class="sxs-lookup"><span data-stu-id="02b50-178">If you want to turn off the group creation restriction and again allow all users to create groups, set $GroupName to "" and $AllowGroupCreation to "True" and rerun the script.</span></span>
    
## <a name="step-4-verify-that-it-works"></a><span data-ttu-id="02b50-179">Étape 4 : vérifier qu’elle fonctionne</span><span class="sxs-lookup"><span data-stu-id="02b50-179">Step 4: Verify that it works</span></span>

1. <span data-ttu-id="02b50-180">Connectez-vous à Office 365 avec le compte d'utilisateur d'une personne qui ne doit PAS être autorisée à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="02b50-180">Sign in to Office 365 with a user account of someone who should NOT have the ability to create groups.</span></span> <span data-ttu-id="02b50-181">Autrement dit, ils ne sont pas membres du groupe de sécurité que vous avez créé ou d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="02b50-181">That is, they are not a member of the security group you created or an administrator.</span></span>
    
2. <span data-ttu-id="02b50-182">Sélectionnez la vignette **planificateur** .</span><span class="sxs-lookup"><span data-stu-id="02b50-182">Select the **Planner** tile.</span></span> 
    
3. <span data-ttu-id="02b50-183">Dans le planificateur, sélectionnez **nouveau plan** dans le volet de navigation de gauche pour créer un plan.</span><span class="sxs-lookup"><span data-stu-id="02b50-183">In Planner, select **New Plan** in the left navigation to create a plan.</span></span> 
  
4. <span data-ttu-id="02b50-184">Vous devriez recevoir un message indiquant que la création de plan et de groupe est désactivée.</span><span class="sxs-lookup"><span data-stu-id="02b50-184">You should get a message that plan and group creation is disabled.</span></span>

<span data-ttu-id="02b50-185">Renouvelez la même procédure avec un membre du groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="02b50-185">Try the same procedure again with a member of the security group.</span></span>

> [!NOTE]
> <span data-ttu-id="02b50-186">Si les membres du groupe de sécurité ne peuvent pas créer de groupes, vérifiez qu’ils ne sont pas bloqués via leur [stratégie de boîte aux lettres OWA](https://go.microsoft.com/fwlink/?linkid=852135).</span><span class="sxs-lookup"><span data-stu-id="02b50-186">If members of the security group aren't able to create groups, check that they aren't being blocked through their [OWA mailbox policy](https://go.microsoft.com/fwlink/?linkid=852135).</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="02b50-187">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="02b50-187">Related articles</span></span>

[<span data-ttu-id="02b50-188">Mise en route d’Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="02b50-188">Getting started with Office 365 PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=808033)

[<span data-ttu-id="02b50-189">Configurer la gestion des groupes en libre-service dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="02b50-189">Set up self-service group management in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-self-service-management)

[<span data-ttu-id="02b50-190">Set-ExecutionPolicy</span><span class="sxs-lookup"><span data-stu-id="02b50-190">Set-ExecutionPolicy</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy)

[<span data-ttu-id="02b50-191">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="02b50-191">Azure Active Directory cmdlets for configuring group settings</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets)
