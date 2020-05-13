---
title: Gérer les personnes autorisées à créer des groupes
f1.keywords: NOCSH
ms.author: mikeplum
ms.reviewer: arvaradh
author: MikePlumleyMSFT
manager: pamgreen
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
- MSP160
- MST160
- MET150
- MOE150
ms.assetid: 4c46c8cb-17d0-44b5-9776-005fced8e618
description: Découvrez comment contrôler quels utilisateurs peuvent créer des groupes Microsoft 365.
ms.openlocfilehash: 55b3ec119e8c74982ce340c58f6b8da684c9ffa8
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44208341"
---
# <a name="manage-who-can-create-groups"></a><span data-ttu-id="8d2ea-103">Gérer les personnes autorisées à créer des groupes</span><span class="sxs-lookup"><span data-stu-id="8d2ea-103">Manage who can create Groups</span></span>

  
<span data-ttu-id="8d2ea-104">Étant donné que les utilisateurs peuvent créer facilement des groupes Microsoft 365, vous n’êtes pas submergé par les demandes de création pour le compte d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-104">Because it's so easy for users to create Microsoft 365 groups, you aren't inundated with requests to create them on behalf of other people.</span></span> <span data-ttu-id="8d2ea-105">Toutefois, en fonction de votre activité, vous souhaiterez peut-être contrôler les personnes autorisées à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-105">Depending on your business, however, you might want to control who has the ability to create groups.</span></span>
  
<span data-ttu-id="8d2ea-106">Cet article explique comment désactiver la possibilité de créer des groupes dans tous les services Microsoft 365 qui utilisent des groupes, notamment :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-106">This article explains how to disable the ability to create groups in all Microsoft 365 services that use groups, including:</span></span>
  
- <span data-ttu-id="8d2ea-107">Outlook</span><span class="sxs-lookup"><span data-stu-id="8d2ea-107">Outlook</span></span>
    
- <span data-ttu-id="8d2ea-108">SharePoint</span><span class="sxs-lookup"><span data-stu-id="8d2ea-108">SharePoint</span></span>
    
- <span data-ttu-id="8d2ea-109">Yammer</span><span class="sxs-lookup"><span data-stu-id="8d2ea-109">Yammer</span></span>
    
- <span data-ttu-id="8d2ea-110">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8d2ea-110">Microsoft Teams</span></span>

- <span data-ttu-id="8d2ea-111">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="8d2ea-111">Microsoft Stream</span></span>
    
- <span data-ttu-id="8d2ea-112">StaffHub</span><span class="sxs-lookup"><span data-stu-id="8d2ea-112">StaffHub</span></span>
    
- <span data-ttu-id="8d2ea-113">Planificateur</span><span class="sxs-lookup"><span data-stu-id="8d2ea-113">Planner</span></span>
    
- <span data-ttu-id="8d2ea-114">PowerBI</span><span class="sxs-lookup"><span data-stu-id="8d2ea-114">PowerBI</span></span>

- <span data-ttu-id="8d2ea-115">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="8d2ea-115">Roadmap</span></span>
    
<span data-ttu-id="8d2ea-116">Vous pouvez restreindre la création de groupes Microsoft 365 aux membres d’un groupe de sécurité particulier.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-116">You can restrict Microsoft 365 group creation to the members of a particular security group.</span></span> <span data-ttu-id="8d2ea-117">Pour configurer ce, utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-117">To configure this, you use Windows PowerShell.</span></span> <span data-ttu-id="8d2ea-118">Cet article vous guide tout au long des étapes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-118">This article walks you through the needed steps.</span></span>
  
<span data-ttu-id="8d2ea-119">Les étapes décrites dans cet article n’empêchent pas les membres de certains rôles de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-119">The steps in this article won't prevent members of certain roles from creating Groups.</span></span> <span data-ttu-id="8d2ea-120">Les administrateurs globaux peuvent créer des groupes via n’importe quel moyen, comme le centre d’administration Microsoft 365, le planificateur, teams, Exchange et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-120">Global admins can create Groups via any means, such as the Microsoft 365 admin center, Planner, Teams, Exchange, and SharePoint Online.</span></span> <span data-ttu-id="8d2ea-121">D’autres rôles peuvent créer des groupes via des moyens limités, présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-121">Other roles can create Groups via limited means, listed below.</span></span>
        
  - <span data-ttu-id="8d2ea-122">Administrateur Exchange : Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-122">Exchange Administrator: Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="8d2ea-123">Prise en charge du niveau 1 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-123">Partner Tier 1 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="8d2ea-124">Prise en charge du niveau 2 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-124">Partner Tier 2 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="8d2ea-125">Writers d’annuaire : Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-125">Directory Writers: Azure AD</span></span>

  - <span data-ttu-id="8d2ea-126">Administrateur SharePoint : Centre d’administration SharePoint, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-126">SharePoint Administrator: SharePoint Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="8d2ea-127">Administrateur de service teams : Centre d’administration Teams, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-127">Teams Service Administrator: Teams Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="8d2ea-128">Administrateur de gestion des utilisateurs : Centre d’administration Microsoft 365, Yammer, Azure AD</span><span class="sxs-lookup"><span data-stu-id="8d2ea-128">User Management Administrator: Microsoft 365 Admin center, Yammer, Azure AD</span></span>
     
<span data-ttu-id="8d2ea-129">Si vous êtes membre de l’un de ces rôles, vous pouvez créer des groupes Microsoft 365 pour des utilisateurs restreints, puis affecter l’utilisateur comme propriétaire du groupe.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-129">If you're a member of one of these roles, you can create Microsoft 365 groups for restricted users, and then assign the user as the owner of the group.</span></span> <span data-ttu-id="8d2ea-130">Les utilisateurs qui ont ce rôle peuvent créer des groupes connectés dans Yammer, indépendamment des paramètres PowerShell susceptibles d’empêcher la création.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-130">Users that have this role are able to create connected groups in Yammer, regardless of any PowerShell settings that might prevent creation.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="8d2ea-131">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="8d2ea-131">Licensing requirements</span></span>

<span data-ttu-id="8d2ea-132">Pour gérer la personne qui crée des groupes, les personnes suivantes ont besoin de licences Azure AD Premium ou d’Azure AD base EDU qui leur sont attribuées :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-132">To manage who creates Groups, the following people need Azure AD Premium licenses or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="8d2ea-133">Administrateur qui configure ces paramètres de création de groupe</span><span class="sxs-lookup"><span data-stu-id="8d2ea-133">The admin who configures these group creation settings</span></span>
- <span data-ttu-id="8d2ea-134">Les membres du groupe de sécurité autorisés à créer des groupes</span><span class="sxs-lookup"><span data-stu-id="8d2ea-134">The members of the security group who are allowed to create groups</span></span>

> [!NOTE]
> <span data-ttu-id="8d2ea-135">Pour plus d’informations sur l’attribution de licences Azure [, voir attribuer ou supprimer des licences dans le portail Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups) .</span><span class="sxs-lookup"><span data-stu-id="8d2ea-135">See [Assign or remove licenses in the Azure Active Directory portal](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups) for more details about how to assign Azure licenses.</span></span>

<span data-ttu-id="8d2ea-136">Les personnes suivantes n’ont pas besoin de posséder des licences Azure ad Premium ou EDU AD basique EDU :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-136">The following people don't need Azure AD Premium or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="8d2ea-137">Personnes membres des groupes Microsoft 365 et qui ne peuvent pas créer d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-137">People who are members of Microsoft 365 groups and who don't have the ability to create other groups.</span></span>

## <a name="step-1-create-a-security-group-for-users-who-need-to-create-microsoft-365-groups"></a><span data-ttu-id="8d2ea-138">Étape 1 : créer un groupe de sécurité pour les utilisateurs qui ont besoin de créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8d2ea-138">Step 1: Create a security group for users who need to create Microsoft 365 groups</span></span>

<span data-ttu-id="8d2ea-139">Un seul groupe de sécurité dans votre organisation peut être utilisé pour contrôler qui est en mesure de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-139">Only one security group in your organization can be used to control who is able to create Groups.</span></span> <span data-ttu-id="8d2ea-140">Toutefois, vous pouvez imbriquer d'autres groupes de sécurité en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-140">But, you can nest other security groups as members of this group.</span></span> <span data-ttu-id="8d2ea-141">Par exemple, le groupe intitulé « Autoriser la création de groupes » est le groupe de sécurité désigné, et les groupes intitulés Utilisateurs du Planificateur Microsoft et Utilisateurs d'Exchange Online sont membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-141">For example, the group named Allow Group Creation is the designated security group, and the groups named Microsoft Planner Users and Exchange Online Users are members of that group.</span></span>

<span data-ttu-id="8d2ea-142">Les administrateurs appartenant aux rôles mentionnés ci-dessus n’ont pas besoin d’être membres de ce groupe : ils conservent leur capacité à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-142">Admins in the roles listed above do not need to be members of this group: they retain their ability to create groups.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d2ea-143">Veillez à utiliser un **groupe de sécurité** pour limiter les personnes autorisées à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-143">Be sure to use a **security group** to restrict who can create groups.</span></span> <span data-ttu-id="8d2ea-144">Si vous essayez d’utiliser un groupe Microsoft 365, les membres ne pourront pas créer de groupe à partir de SharePoint, car il recherche un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-144">If you try to use a Microsoft 365 group, members won't be able to create a group from SharePoint because it checks for a security group.</span></span> 
    
1. <span data-ttu-id="8d2ea-145">Dans le centre d’administration, accédez à **la page groupes de** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes</a> .</span><span class="sxs-lookup"><span data-stu-id="8d2ea-145">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>

2. <span data-ttu-id="8d2ea-146">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-146">Click on **Add a Group**.</span></span>

3. <span data-ttu-id="8d2ea-147">Choisissez **Security** comme type de groupe.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-147">Choose **Security** as the group type.</span></span> <span data-ttu-id="8d2ea-148">Notez bien le nom du groupe !</span><span class="sxs-lookup"><span data-stu-id="8d2ea-148">Remember the name of the group!</span></span> <span data-ttu-id="8d2ea-149">Vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-149">You'll need it later.</span></span>
  
4. <span data-ttu-id="8d2ea-150">Terminez la configuration du groupe de sécurité, en ajoutant des personnes ou d’autres groupes de sécurité qui doivent être en mesure de créer des groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-150">Finish setting up the security group, adding people or other security groups who you want to be able to create groups in your org.</span></span>
    
<span data-ttu-id="8d2ea-151">Pour obtenir des instructions détaillées, reportez-vous à [créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration 365 de Microsoft](../email/create-edit-or-delete-a-security-group.md).</span><span class="sxs-lookup"><span data-stu-id="8d2ea-151">For detailed instructions, see [Create, edit, or delete a security group in the Microsoft 365 admin center](../email/create-edit-or-delete-a-security-group.md).</span></span>
 
## <a name="step-2-run-powershell-commands"></a><span data-ttu-id="8d2ea-152">Étape 2 : exécuter les commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d2ea-152">Step 2: Run PowerShell commands</span></span>

<span data-ttu-id="8d2ea-153">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre d’accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-153">You must use the preview version of [Azure Active Directory PowerShell for Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="8d2ea-154">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-154">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="8d2ea-155">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-155">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="8d2ea-156">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-156">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>



<span data-ttu-id="8d2ea-157">Copiez le script ci-dessous dans un éditeur de texte, tel que le bloc-notes, ou [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span><span class="sxs-lookup"><span data-stu-id="8d2ea-157">Copy the script below into a text editor, such as Notepad, or the [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span></span>

<span data-ttu-id="8d2ea-158">Remplacez \* \< SecurityGroupName \> \* par le nom du groupe de sécurité que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-158">Replace *\<SecurityGroupName\>* with the name of the security group that you created.</span></span> <span data-ttu-id="8d2ea-159">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-159">For example:</span></span>

`$GroupName = "Group Creators"`

<span data-ttu-id="8d2ea-160">Enregistrez le fichier sous le GroupCreators. ps1.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-160">Save the file as GroupCreators.ps1.</span></span> 

<span data-ttu-id="8d2ea-161">Dans la fenêtre PowerShell, accédez à l’emplacement où vous avez enregistré le fichier (tapez « CD <FileLocation> »).</span><span class="sxs-lookup"><span data-stu-id="8d2ea-161">In the PowerShell window, navigate to the location where you saved the file (type "CD <FileLocation>").</span></span>

<span data-ttu-id="8d2ea-162">Exécutez le script en tapant :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-162">Run the script by typing:</span></span>

`.\GroupCreators.ps1`

<span data-ttu-id="8d2ea-163">Lorsque vous y êtes invité, [Connectez-vous avec votre compte d’administrateur](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#step-2-connect-to-azure-ad-for-your-office-365-subscription) .</span><span class="sxs-lookup"><span data-stu-id="8d2ea-163">and [sign in with your administrator account](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#step-2-connect-to-azure-ad-for-your-office-365-subscription) when prompted.</span></span>

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

<span data-ttu-id="8d2ea-164">La dernière ligne du script affiche les paramètres mis à jour :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-164">The last line of the script will display the updated settings:</span></span>

![This is what your settings will look like when you're done.](../../media/952cd982-5139-4080-9add-24bafca0830c.png)

<span data-ttu-id="8d2ea-166">Si, à l’avenir, vous souhaitez modifier le groupe de sécurité utilisé, vous pouvez réexécuter le script avec le nom du nouveau groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-166">If in the future you want to change which security group is used, you can rerun the script with the name of the new security group.</span></span>

<span data-ttu-id="8d2ea-167">Si vous souhaitez désactiver la restriction de création de groupe et permettre à tous les utilisateurs de créer des groupes, définissez $GroupName sur "" et $AllowGroupCreation sur "true", puis réexécutez le script.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-167">If you want to turn off the group creation restriction and again allow all users to create groups, set $GroupName to "" and $AllowGroupCreation to "True" and rerun the script.</span></span>
    
## <a name="step-4-verify-that-it-works"></a><span data-ttu-id="8d2ea-168">Étape 4 : vérifier qu’elle fonctionne</span><span class="sxs-lookup"><span data-stu-id="8d2ea-168">Step 4: Verify that it works</span></span>

<span data-ttu-id="8d2ea-169">Les modifications peuvent durer au moins 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-169">Changes can take thirty minutes or more to take effect.</span></span> <span data-ttu-id="8d2ea-170">Vous pouvez vérifier les nouveaux paramètres en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d2ea-170">You can verify the new settings by doing the following:</span></span>

1. <span data-ttu-id="8d2ea-171">Connectez-vous à l’aide d’un compte d’utilisateur qui ne doit pas avoir la possibilité de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-171">Sign in with a user account of someone who should NOT have the ability to create groups.</span></span> <span data-ttu-id="8d2ea-172">Autrement dit, ils ne sont pas membres du groupe de sécurité que vous avez créé ou d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-172">That is, they are not a member of the security group you created or an administrator.</span></span>
    
2. <span data-ttu-id="8d2ea-173">Sélectionnez la vignette **planificateur** .</span><span class="sxs-lookup"><span data-stu-id="8d2ea-173">Select the **Planner** tile.</span></span> 
    
3. <span data-ttu-id="8d2ea-174">Dans le planificateur, sélectionnez **nouveau plan** dans le volet de navigation de gauche pour créer un plan.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-174">In Planner, select **New Plan** in the left navigation to create a plan.</span></span> 
  
4. <span data-ttu-id="8d2ea-175">Vous devriez recevoir un message indiquant que la création de plan et de groupe est désactivée.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-175">You should get a message that plan and group creation is disabled.</span></span>

<span data-ttu-id="8d2ea-176">Renouvelez la même procédure avec un membre du groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8d2ea-176">Try the same procedure again with a member of the security group.</span></span>

> [!NOTE]
> <span data-ttu-id="8d2ea-177">Si les membres du groupe de sécurité ne peuvent pas créer de groupes, vérifiez qu’ils ne sont pas bloqués via leur [stratégie de boîte aux lettres OWA](https://go.microsoft.com/fwlink/?linkid=852135).</span><span class="sxs-lookup"><span data-stu-id="8d2ea-177">If members of the security group aren't able to create groups, check that they aren't being blocked through their [OWA mailbox policy](https://go.microsoft.com/fwlink/?linkid=852135).</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="8d2ea-178">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8d2ea-178">Related articles</span></span>

[<span data-ttu-id="8d2ea-179">Mise en route d’Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d2ea-179">Getting started with Office 365 PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=808033)

[<span data-ttu-id="8d2ea-180">Configurer la gestion des groupes en libre-service dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8d2ea-180">Set up self-service group management in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-self-service-management)

[<span data-ttu-id="8d2ea-181">Set-ExecutionPolicy</span><span class="sxs-lookup"><span data-stu-id="8d2ea-181">Set-ExecutionPolicy</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy)

[<span data-ttu-id="8d2ea-182">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="8d2ea-182">Azure Active Directory cmdlets for configuring group settings</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets)
