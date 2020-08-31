---
title: Gérer les personnes autorisées à créer des groupes Microsoft 365
f1.keywords: NOCSH
ms.author: mikeplum
ms.reviewer: arvaradh
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- MET150
ms.assetid: 4c46c8cb-17d0-44b5-9776-005fced8e618
description: Découvrez comment contrôler quels utilisateurs peuvent créer des groupes Microsoft 365.
ms.openlocfilehash: d6e6c6d9caff2ac7c13d03dad97b73906a509f46
ms.sourcegitcommit: 555d756c69ac9031d1fb928f2e1f9750beede066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47307858"
---
# <a name="manage-who-can-create-microsoft-365-groups"></a><span data-ttu-id="0f8da-103">Gérer les personnes autorisées à créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0f8da-103">Manage who can create Microsoft 365 Groups</span></span>

<span data-ttu-id="0f8da-104">Par défaut, tous les utilisateurs peuvent créer des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f8da-104">By default, all users can create Microsoft 365 groups.</span></span> <span data-ttu-id="0f8da-105">Il s’agit de l’approche recommandée, car elle permet aux utilisateurs de commencer à collaborer sans avoir besoin d’assistance.</span><span class="sxs-lookup"><span data-stu-id="0f8da-105">This is the recommended approach because it allows users to start collaborating without requiring assistance from IT.</span></span>

<span data-ttu-id="0f8da-106">Si votre entreprise exige que vous restreigniez les personnes autorisées à créer des groupes, vous pouvez le faire en suivant les procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0f8da-106">If your business requires that you restrict who can create groups, you can do so by following the procedures in this article.</span></span> <span data-ttu-id="0f8da-107">Lorsque vous limitez les personnes autorisées à créer un groupe, elle affecte tous les services qui dépendent des groupes pour l’accès, notamment :</span><span class="sxs-lookup"><span data-stu-id="0f8da-107">When you limit who can create a group, it affects all services that rely on groups for access, including:</span></span>

- <span data-ttu-id="0f8da-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="0f8da-108">Outlook</span></span>
    
- <span data-ttu-id="0f8da-109">SharePoint</span><span class="sxs-lookup"><span data-stu-id="0f8da-109">SharePoint</span></span>
    
- <span data-ttu-id="0f8da-110">Yammer</span><span class="sxs-lookup"><span data-stu-id="0f8da-110">Yammer</span></span>
    
- <span data-ttu-id="0f8da-111">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0f8da-111">Microsoft Teams</span></span>

- <span data-ttu-id="0f8da-112">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="0f8da-112">Microsoft Stream</span></span>

- <span data-ttu-id="0f8da-113">Planificateur</span><span class="sxs-lookup"><span data-stu-id="0f8da-113">Planner</span></span>
    
- <span data-ttu-id="0f8da-114">PowerBI (classique)</span><span class="sxs-lookup"><span data-stu-id="0f8da-114">PowerBI (classic)</span></span>
    
- <span data-ttu-id="0f8da-115">Projet pour le Web/feuille de route</span><span class="sxs-lookup"><span data-stu-id="0f8da-115">Project for the web / Roadmap</span></span>
    
<span data-ttu-id="0f8da-116">Vous pouvez restreindre la création de groupes Microsoft 365 aux membres d’un groupe de sécurité particulier.</span><span class="sxs-lookup"><span data-stu-id="0f8da-116">You can restrict Microsoft 365 Group creation to the members of a particular security group.</span></span> <span data-ttu-id="0f8da-117">Pour configurer ce, utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f8da-117">To configure this, you use Windows PowerShell.</span></span> <span data-ttu-id="0f8da-118">Cet article vous guide tout au long des étapes nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0f8da-118">This article walks you through the needed steps.</span></span>
  
<span data-ttu-id="0f8da-119">Les étapes décrites dans cet article n’empêchent pas les membres de certains rôles de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-119">The steps in this article won't prevent members of certain roles from creating Groups.</span></span> <span data-ttu-id="0f8da-120">Les administrateurs globaux Office 365 peuvent créer des groupes via n’importe quel moyen, comme le centre d’administration Microsoft 365, le planificateur, teams, Exchange et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0f8da-120">Office 365 Global admins can create Groups via any means, such as the Microsoft 365 admin center, Planner, Teams, Exchange, and SharePoint Online.</span></span> <span data-ttu-id="0f8da-121">D’autres rôles peuvent créer des groupes via des moyens limités, présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0f8da-121">Other roles can create Groups via limited means, listed below.</span></span>
        
  - <span data-ttu-id="0f8da-122">Administrateur Exchange : Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-122">Exchange Administrator: Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="0f8da-123">Prise en charge du niveau 1 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-123">Partner Tier 1 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="0f8da-124">Prise en charge du niveau 2 du partenaire : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-124">Partner Tier 2 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
    
  - <span data-ttu-id="0f8da-125">Writers d’annuaire : Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-125">Directory Writers: Azure AD</span></span>

  - <span data-ttu-id="0f8da-126">Administrateur SharePoint : Centre d’administration SharePoint, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-126">SharePoint Administrator: SharePoint Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="0f8da-127">Administrateur de service teams : Centre d’administration Teams, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-127">Teams Service Administrator: Teams Admin center, Azure AD</span></span>
  
  - <span data-ttu-id="0f8da-128">Administrateur de gestion des utilisateurs : Centre d’administration Microsoft 365, Yammer, Azure AD</span><span class="sxs-lookup"><span data-stu-id="0f8da-128">User Management Administrator: Microsoft 365 Admin center, Yammer, Azure AD</span></span>
     
<span data-ttu-id="0f8da-129">Si vous êtes membre de l’un de ces rôles, vous pouvez créer des groupes Microsoft 365 pour des utilisateurs restreints, puis affecter l’utilisateur comme propriétaire du groupe.</span><span class="sxs-lookup"><span data-stu-id="0f8da-129">If you're a member of one of these roles, you can create Microsoft 365 Groups for restricted users, and then assign the user as the owner of the group.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="0f8da-130">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="0f8da-130">Licensing requirements</span></span>

<span data-ttu-id="0f8da-131">Pour gérer la personne qui crée des groupes, les personnes suivantes ont besoin de licences Azure AD Premium ou d’Azure AD base EDU qui leur sont attribuées :</span><span class="sxs-lookup"><span data-stu-id="0f8da-131">To manage who creates groups, the following people need Azure AD Premium licenses or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="0f8da-132">Administrateur qui configure ces paramètres de création de groupe</span><span class="sxs-lookup"><span data-stu-id="0f8da-132">The admin who configures these group creation settings</span></span>
- <span data-ttu-id="0f8da-133">Les membres du groupe de sécurité autorisés à créer des groupes</span><span class="sxs-lookup"><span data-stu-id="0f8da-133">The members of the security group who are allowed to create groups</span></span>
 
> [!NOTE]
> <span data-ttu-id="0f8da-134">Pour plus d’informations sur l’attribution de licences Azure [, voir attribuer ou supprimer des licences dans le portail Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups) .</span><span class="sxs-lookup"><span data-stu-id="0f8da-134">See [Assign or remove licenses in the Azure Active Directory portal](https://docs.microsoft.com/azure/active-directory/fundamentals/license-users-groups) for more details about how to assign Azure licenses.</span></span>

<span data-ttu-id="0f8da-135">Les personnes suivantes n’ont pas besoin de posséder des licences Azure ad Premium ou EDU AD basique EDU :</span><span class="sxs-lookup"><span data-stu-id="0f8da-135">The following people don't need Azure AD Premium or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="0f8da-136">Personnes membres des groupes Microsoft 365 et qui ne peuvent pas créer d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-136">People who are members of Microsoft 365 groups and who don't have the ability to create other groups.</span></span>

## <a name="step-1-create-a-security-group-for-users-who-need-to-create-microsoft-365-groups"></a><span data-ttu-id="0f8da-137">Étape 1 : créer un groupe de sécurité pour les utilisateurs qui ont besoin de créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0f8da-137">Step 1: Create a security group for users who need to create Microsoft 365 groups</span></span>

<span data-ttu-id="0f8da-138">Un seul groupe de sécurité dans votre organisation peut être utilisé pour contrôler qui est en mesure de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-138">Only one security group in your organization can be used to control who is able to create Groups.</span></span> <span data-ttu-id="0f8da-139">Toutefois, vous pouvez imbriquer d'autres groupes de sécurité en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="0f8da-139">But, you can nest other security groups as members of this group.</span></span>

<span data-ttu-id="0f8da-140">Les administrateurs appartenant aux rôles mentionnés ci-dessus n’ont pas besoin d’être membres de ce groupe : ils conservent leur capacité à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-140">Admins in the roles listed above do not need to be members of this group: they retain their ability to create groups.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f8da-141">Veillez à utiliser un **groupe de sécurité** pour limiter les personnes autorisées à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-141">Be sure to use a **security group** to restrict who can create groups.</span></span> <span data-ttu-id="0f8da-142">L’utilisation d’un groupe Microsoft 365 n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0f8da-142">Using a Microsoft 365 group is not supported.</span></span> 
    
1. <span data-ttu-id="0f8da-143">Dans le centre d’administration, accédez à la [page groupes](https://admin.microsoft.com/adminportal/home#/groups).</span><span class="sxs-lookup"><span data-stu-id="0f8da-143">In the admin center, go to the [Groups page](https://admin.microsoft.com/adminportal/home#/groups).</span></span>

2. <span data-ttu-id="0f8da-144">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="0f8da-144">Click on **Add a Group**.</span></span>

3. <span data-ttu-id="0f8da-145">Choisissez **Security** comme type de groupe.</span><span class="sxs-lookup"><span data-stu-id="0f8da-145">Choose **Security** as the group type.</span></span> <span data-ttu-id="0f8da-146">Notez bien le nom du groupe !</span><span class="sxs-lookup"><span data-stu-id="0f8da-146">Remember the name of the group!</span></span> <span data-ttu-id="0f8da-147">Vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="0f8da-147">You'll need it later.</span></span>
  
4. <span data-ttu-id="0f8da-148">Terminez la configuration du groupe de sécurité, en ajoutant des personnes ou d’autres groupes de sécurité qui doivent être en mesure de créer des groupes dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0f8da-148">Finish setting up the security group, adding people or other security groups who you want to be able to create groups in your org.</span></span>
    
<span data-ttu-id="0f8da-149">Pour obtenir des instructions détaillées, reportez-vous à [créer, modifier ou supprimer un groupe de sécurité dans le centre d’administration 365 de Microsoft](https://docs.microsoft.com/microsoft-365/admin/email/create-edit-or-delete-a-security-group).</span><span class="sxs-lookup"><span data-stu-id="0f8da-149">For detailed instructions, see [Create, edit, or delete a security group in the Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/email/create-edit-or-delete-a-security-group).</span></span>
 
## <a name="step-2-run-powershell-commands"></a><span data-ttu-id="0f8da-150">Étape 2 : exécuter les commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="0f8da-150">Step 2: Run PowerShell commands</span></span>

<span data-ttu-id="0f8da-151">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre d’accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="0f8da-151">You must use the preview version of [Azure Active Directory PowerShell for Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="0f8da-152">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="0f8da-152">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="0f8da-153">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="0f8da-153">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="0f8da-154">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="0f8da-154">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

<span data-ttu-id="0f8da-155">Copiez le script ci-dessous dans un éditeur de texte, tel que le bloc-notes, ou [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span><span class="sxs-lookup"><span data-stu-id="0f8da-155">Copy the script below into a text editor, such as Notepad, or the [Windows PowerShell ISE](https://docs.microsoft.com/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span></span>

<span data-ttu-id="0f8da-156">Remplacez *\<SecurityGroupName\>* par le nom du groupe de sécurité que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="0f8da-156">Replace *\<SecurityGroupName\>* with the name of the security group that you created.</span></span> <span data-ttu-id="0f8da-157">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0f8da-157">For example:</span></span>

`$GroupName = "Group Creators"`

<span data-ttu-id="0f8da-158">Enregistrez le fichier en tant que GroupCreators.ps1.</span><span class="sxs-lookup"><span data-stu-id="0f8da-158">Save the file as GroupCreators.ps1.</span></span> 

<span data-ttu-id="0f8da-159">Dans la fenêtre PowerShell, accédez à l’emplacement où vous avez enregistré le fichier (tapez « CD <FileLocation> »).</span><span class="sxs-lookup"><span data-stu-id="0f8da-159">In the PowerShell window, navigate to the location where you saved the file (type "CD <FileLocation>").</span></span>

<span data-ttu-id="0f8da-160">Exécutez le script en tapant :</span><span class="sxs-lookup"><span data-stu-id="0f8da-160">Run the script by typing:</span></span>

`.\GroupCreators.ps1`

<span data-ttu-id="0f8da-161">Lorsque vous y êtes invité, [Connectez-vous avec votre compte d’administrateur](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription) .</span><span class="sxs-lookup"><span data-stu-id="0f8da-161">and [sign in with your administrator account](https://docs.microsoft.com/microsoft-365/enterprise/connect-to-microsoft-365-powershell#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription) when prompted.</span></span>

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

<span data-ttu-id="0f8da-162">La dernière ligne du script affiche les paramètres mis à jour :</span><span class="sxs-lookup"><span data-stu-id="0f8da-162">The last line of the script will display the updated settings:</span></span>

![This is what your settings will look like when you're done.](../media/952cd982-5139-4080-9add-24bafca0830c.png)

<span data-ttu-id="0f8da-164">Si, à l’avenir, vous souhaitez modifier le groupe de sécurité utilisé, vous pouvez réexécuter le script avec le nom du nouveau groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f8da-164">If in the future you want to change which security group is used, you can rerun the script with the name of the new security group.</span></span>

<span data-ttu-id="0f8da-165">Si vous souhaitez désactiver la restriction de création de groupe et permettre à tous les utilisateurs de créer des groupes, définissez $GroupName sur "" et $AllowGroupCreation sur "true", puis réexécutez le script.</span><span class="sxs-lookup"><span data-stu-id="0f8da-165">If you want to turn off the group creation restriction and again allow all users to create groups, set $GroupName to "" and $AllowGroupCreation to "True" and rerun the script.</span></span>
    
## <a name="step-3-verify-that-it-works"></a><span data-ttu-id="0f8da-166">Étape 3 : vérifier le bon fonctionnement</span><span class="sxs-lookup"><span data-stu-id="0f8da-166">Step 3: Verify that it works</span></span>

<span data-ttu-id="0f8da-167">Les modifications peuvent durer au moins 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-167">Changes can take thirty minutes or more to take effect.</span></span> <span data-ttu-id="0f8da-168">Vous pouvez vérifier les nouveaux paramètres en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="0f8da-168">You can verify the new settings by doing the following:</span></span>

1. <span data-ttu-id="0f8da-169">Connectez-vous à Microsoft 365 avec un compte d’utilisateur qui ne doit pas avoir la possibilité de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="0f8da-169">Sign in to Microsoft 365 with a user account of someone who should NOT have the ability to create groups.</span></span> <span data-ttu-id="0f8da-170">Autrement dit, ils ne sont pas membres du groupe de sécurité que vous avez créé ou d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="0f8da-170">That is, they are not a member of the security group you created or an administrator.</span></span>
    
2. <span data-ttu-id="0f8da-171">Sélectionnez la vignette **planificateur** .</span><span class="sxs-lookup"><span data-stu-id="0f8da-171">Select the **Planner** tile.</span></span> 
    
3. <span data-ttu-id="0f8da-172">Dans le planificateur, sélectionnez **nouveau plan** dans le volet de navigation de gauche pour créer un plan.</span><span class="sxs-lookup"><span data-stu-id="0f8da-172">In Planner, select **New Plan** in the left navigation to create a plan.</span></span> 
  
4. <span data-ttu-id="0f8da-173">Vous devriez recevoir un message indiquant que la création de plan et de groupe est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0f8da-173">You should get a message that plan and group creation is disabled.</span></span>

<span data-ttu-id="0f8da-174">Renouvelez la même procédure avec un membre du groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f8da-174">Try the same procedure again with a member of the security group.</span></span>

> [!NOTE]
> <span data-ttu-id="0f8da-175">Si les membres du groupe de sécurité ne peuvent pas créer de groupes, vérifiez qu’ils ne sont pas bloqués via leur [stratégie de boîte aux lettres OWA](https://go.microsoft.com/fwlink/?linkid=852135).</span><span class="sxs-lookup"><span data-stu-id="0f8da-175">If members of the security group aren't able to create groups, check that they aren't being blocked through their [OWA mailbox policy](https://go.microsoft.com/fwlink/?linkid=852135).</span></span>
    
## <a name="related-articles"></a><span data-ttu-id="0f8da-176">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0f8da-176">Related articles</span></span>

[<span data-ttu-id="0f8da-177">Mise en route d’Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="0f8da-177">Getting started with Office 365 PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=808033)

[<span data-ttu-id="0f8da-178">Configurer la gestion des groupes en libre-service dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0f8da-178">Set up self-service group management in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-self-service-management)

[<span data-ttu-id="0f8da-179">Set-ExecutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0f8da-179">Set-ExecutionPolicy</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.security/set-executionpolicy)

[<span data-ttu-id="0f8da-180">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="0f8da-180">Azure Active Directory cmdlets for configuring group settings</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-settings-cmdlets)
