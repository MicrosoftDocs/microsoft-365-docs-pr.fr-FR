---
title: Gérer les personnes autorisées à créer des groupes Microsoft 365
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
- m365solution-collabgovernance
search.appverid:
- MET150
ms.assetid: 4c46c8cb-17d0-44b5-9776-005fced8e618
description: Découvrez comment contrôler les utilisateurs qui peuvent créer des groupes Microsoft 365.
ms.openlocfilehash: 9c3edf335ce09f04e9b0b538e69fa607a9c34044
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50929155"
---
# <a name="manage-who-can-create-microsoft-365-groups"></a><span data-ttu-id="a27c8-103">Gérer les personnes autorisées à créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a27c8-103">Manage who can create Microsoft 365 Groups</span></span>

<span data-ttu-id="a27c8-104">Par défaut, tous les utilisateurs peuvent créer des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a27c8-104">By default, all users can create Microsoft 365 groups.</span></span> <span data-ttu-id="a27c8-105">Il s’agit de l’approche recommandée, car elle permet aux utilisateurs de commencer à collaborer sans nécessiter l’assistance de l’équipe technique.</span><span class="sxs-lookup"><span data-stu-id="a27c8-105">This is the recommended approach because it allows users to start collaborating without requiring assistance from IT.</span></span>

<span data-ttu-id="a27c8-106">Si votre entreprise exige que vous restreignez les personnes qui peuvent créer des groupes, vous pouvez limiter la création de groupes Microsoft 365 aux membres d’un groupe ou d’un groupe de sécurité Microsoft 365 particulier.</span><span class="sxs-lookup"><span data-stu-id="a27c8-106">If your business requires that you restrict who can create groups, you can restrict Microsoft 365 Group creation to the members of a particular Microsoft 365 group or security group.</span></span>

<span data-ttu-id="a27c8-107">Si vous êtes préoccupé par le fait que les utilisateurs créent des équipes ou des groupes qui ne sont pas conformes à vos normes professionnelles, envisagez de demander aux utilisateurs de terminer un cours de formation, puis de les ajouter au groupe d’utilisateurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="a27c8-107">If you're concerned about users creating teams or groups that don't comply with your business standards, consider requiring users to complete a training course and then adding them to the group of allowed users.</span></span>

<span data-ttu-id="a27c8-108">Lorsque vous limitez les personnes autorisées à créer un groupe, cela affecte tous les services qui s’appuient sur les groupes pour l’accès, notamment :</span><span class="sxs-lookup"><span data-stu-id="a27c8-108">When you limit who can create a group, it affects all services that rely on groups for access, including:</span></span>

- <span data-ttu-id="a27c8-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="a27c8-109">Outlook</span></span>
- <span data-ttu-id="a27c8-110">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a27c8-110">SharePoint</span></span>
- <span data-ttu-id="a27c8-111">Yammer</span><span class="sxs-lookup"><span data-stu-id="a27c8-111">Yammer</span></span>
- <span data-ttu-id="a27c8-112">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a27c8-112">Microsoft Teams</span></span>
- <span data-ttu-id="a27c8-113">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="a27c8-113">Microsoft Stream</span></span>
- <span data-ttu-id="a27c8-114">Planificateur</span><span class="sxs-lookup"><span data-stu-id="a27c8-114">Planner</span></span>
- <span data-ttu-id="a27c8-115">Power BI (classique)</span><span class="sxs-lookup"><span data-stu-id="a27c8-115">Power BI (classic)</span></span>
- <span data-ttu-id="a27c8-116">Projet pour le web / Feuille de route</span><span class="sxs-lookup"><span data-stu-id="a27c8-116">Project for the web / Roadmap</span></span>

<span data-ttu-id="a27c8-117">Les étapes de cet article n’empêchent pas les membres de certains rôles de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="a27c8-117">The steps in this article won't prevent members of certain roles from creating Groups.</span></span> <span data-ttu-id="a27c8-118">Les administrateurs globaux Office 365 peuvent créer des groupes par n’importe quel moyen, comme le Centre d’administration Microsoft 365, le Planificateur, Teams, Exchange et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a27c8-118">Office 365 Global admins can create Groups via any means, such as the Microsoft 365 admin center, Planner, Teams, Exchange, and SharePoint Online.</span></span> <span data-ttu-id="a27c8-119">D’autres rôles peuvent créer des groupes via des moyens limités, répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a27c8-119">Other roles can create Groups via limited means, listed below.</span></span>

- <span data-ttu-id="a27c8-120">Administrateur Exchange : Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-120">Exchange Administrator: Exchange Admin center, Azure AD</span></span>
- <span data-ttu-id="a27c8-121">Support partenaire de niveau 1 : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-121">Partner Tier 1 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
- <span data-ttu-id="a27c8-122">Support partenaire de niveau 2 : Centre d’administration Microsoft 365, Centre d’administration Exchange, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-122">Partner Tier 2 Support: Microsoft 365 Admin center, Exchange Admin center, Azure AD</span></span>
- <span data-ttu-id="a27c8-123">Rédacteurs d’annuaire : Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-123">Directory Writers: Azure AD</span></span>
- <span data-ttu-id="a27c8-124">Administrateur SharePoint : Centre d’administration SharePoint, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-124">SharePoint Administrator: SharePoint Admin center, Azure AD</span></span>
- <span data-ttu-id="a27c8-125">Administrateur de service Teams : Centre d’administration Teams, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-125">Teams Service Administrator: Teams Admin center, Azure AD</span></span>
- <span data-ttu-id="a27c8-126">Administrateur utilisateur : Centre d’administration Microsoft 365, Azure AD</span><span class="sxs-lookup"><span data-stu-id="a27c8-126">User Administrator: Microsoft 365 Admin center, Azure AD</span></span>

<span data-ttu-id="a27c8-127">Si vous êtes membre de l’un de ces rôles, vous pouvez créer des groupes Microsoft 365 pour les utilisateurs restreints, puis affecter l’utilisateur en tant que propriétaire du groupe.</span><span class="sxs-lookup"><span data-stu-id="a27c8-127">If you're a member of one of these roles, you can create Microsoft 365 Groups for restricted users, and then assign the user as the owner of the group.</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="a27c8-128">Critères de licence</span><span class="sxs-lookup"><span data-stu-id="a27c8-128">Licensing requirements</span></span>

<span data-ttu-id="a27c8-129">Pour gérer les personnes qui créent des groupes, les personnes suivantes ont besoin de licences Azure AD Premium ou de licences Azure AD Basic EDU qui leur sont attribuées :</span><span class="sxs-lookup"><span data-stu-id="a27c8-129">To manage who creates groups, the following people need Azure AD Premium licenses or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="a27c8-130">Administrateur qui configure ces paramètres de création de groupe</span><span class="sxs-lookup"><span data-stu-id="a27c8-130">The admin who configures these group creation settings</span></span>
- <span data-ttu-id="a27c8-131">Membres du groupe autorisés à créer des groupes</span><span class="sxs-lookup"><span data-stu-id="a27c8-131">The members of the group who are allowed to create groups</span></span>

> [!NOTE]
> <span data-ttu-id="a27c8-132">Pour plus d’informations sur l’attribution de licences Azure, voir Attribuer ou supprimer des licences dans le portail [Azure Active Directory.](/azure/active-directory/fundamentals/license-users-groups)</span><span class="sxs-lookup"><span data-stu-id="a27c8-132">See [Assign or remove licenses in the Azure Active Directory portal](/azure/active-directory/fundamentals/license-users-groups) for more details about how to assign Azure licenses.</span></span>

<span data-ttu-id="a27c8-133">Les personnes suivantes n’ont pas besoin de licences Azure AD Premium ou Azure AD Basic EDU qui leur sont attribuées :</span><span class="sxs-lookup"><span data-stu-id="a27c8-133">The following people don't need Azure AD Premium or Azure AD Basic EDU licenses assigned to them:</span></span>

- <span data-ttu-id="a27c8-134">Personnes qui sont membres de groupes Microsoft 365 et qui n’ont pas la possibilité de créer d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="a27c8-134">People who are members of Microsoft 365 groups and who don't have the ability to create other groups.</span></span>

## <a name="step-1-create-a-group-for-users-who-need-to-create-microsoft-365-groups"></a><span data-ttu-id="a27c8-135">Étape 1 : Créer un groupe pour les utilisateurs qui doivent créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a27c8-135">Step 1: Create a group for users who need to create Microsoft 365 groups</span></span>

<span data-ttu-id="a27c8-136">Un seul groupe de votre organisation peut être utilisé pour contrôler qui est en mesure de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="a27c8-136">Only one group in your organization can be used to control who is able to create Groups.</span></span> <span data-ttu-id="a27c8-137">Toutefois, vous pouvez imbribrier d’autres groupes en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="a27c8-137">But, you can nest other groups as members of this group.</span></span>

<span data-ttu-id="a27c8-138">Les administrateurs des rôles répertoriés ci-dessus n’ont pas besoin d’être membres de ce groupe : ils conservent leur capacité à créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="a27c8-138">Admins in the roles listed above do not need to be members of this group: they retain their ability to create groups.</span></span>

1. <span data-ttu-id="a27c8-139">Dans le Centre d’administration, allez à la [page Groupes.](https://admin.microsoft.com/adminportal/home#/groups)</span><span class="sxs-lookup"><span data-stu-id="a27c8-139">In the admin center, go to the [Groups page](https://admin.microsoft.com/adminportal/home#/groups).</span></span>

2. <span data-ttu-id="a27c8-140">Cliquez sur **Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="a27c8-140">Click on **Add a Group**.</span></span>

3. <span data-ttu-id="a27c8-141">Choisissez le type de groupe de votre choix.</span><span class="sxs-lookup"><span data-stu-id="a27c8-141">Choose the group type you want.</span></span> <span data-ttu-id="a27c8-142">Notez bien le nom du groupe !</span><span class="sxs-lookup"><span data-stu-id="a27c8-142">Remember the name of the group!</span></span> <span data-ttu-id="a27c8-143">Vous en aurez besoin plus tard.</span><span class="sxs-lookup"><span data-stu-id="a27c8-143">You'll need it later.</span></span>

4. <span data-ttu-id="a27c8-144">Terminez la configuration du groupe, en ajoutant des personnes ou d’autres groupes que vous souhaitez pouvoir créer dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a27c8-144">Finish setting up the group, adding people or other groups who you want to be able to create groups in your org.</span></span>

<span data-ttu-id="a27c8-145">Pour obtenir des instructions détaillées, voir Créer, modifier ou supprimer un groupe de sécurité dans le Centre d’administration [Microsoft 365.](../admin/email/create-edit-or-delete-a-security-group.md)</span><span class="sxs-lookup"><span data-stu-id="a27c8-145">For detailed instructions, see [Create, edit, or delete a security group in the Microsoft 365 admin center](../admin/email/create-edit-or-delete-a-security-group.md).</span></span>

## <a name="step-2-run-powershell-commands"></a><span data-ttu-id="a27c8-146">Étape 2 : exécuter les commandes PowerShell</span><span class="sxs-lookup"><span data-stu-id="a27c8-146">Step 2: Run PowerShell commands</span></span>

<span data-ttu-id="a27c8-147">Vous devez utiliser la version d’aperçu [d’Azure Active Directory PowerShell pour Graph (AzureAD) (nom](/powershell/azure/active-directory/install-adv2) du module **AzureADPreview)** pour modifier le paramètre d’accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="a27c8-147">You must use the preview version of [Azure Active Directory PowerShell for Graph (AzureAD)](/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="a27c8-148">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](/powershell/azure/active-directory/install-adv2?preserve-view=true&view=azureadps-2.0-preview) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="a27c8-148">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](/powershell/azure/active-directory/install-adv2?preserve-view=true&view=azureadps-2.0-preview) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="a27c8-149">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="a27c8-149">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="a27c8-150">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="a27c8-150">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

<span data-ttu-id="a27c8-151">Copiez le script ci-dessous dans un éditeur de texte, tel que le Bloc-notes ou [le Windows PowerShell ISE](/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span><span class="sxs-lookup"><span data-stu-id="a27c8-151">Copy the script below into a text editor, such as Notepad, or the [Windows PowerShell ISE](/powershell/scripting/components/ise/introducing-the-windows-powershell-ise).</span></span>

<span data-ttu-id="a27c8-152">Remplacez *\<GroupName\>* par le nom du groupe que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="a27c8-152">Replace *\<GroupName\>* with the name of the group that you created.</span></span> <span data-ttu-id="a27c8-153">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a27c8-153">For example:</span></span>

`$GroupName = "Group Creators"`

<span data-ttu-id="a27c8-154">Enregistrez le fichier sous GroupCreators.ps1.</span><span class="sxs-lookup"><span data-stu-id="a27c8-154">Save the file as GroupCreators.ps1.</span></span>

<span data-ttu-id="a27c8-155">Dans la fenêtre PowerShell, accédez à l’emplacement où vous avez enregistré le fichier (tapez « CD <FileLocation> »).</span><span class="sxs-lookup"><span data-stu-id="a27c8-155">In the PowerShell window, navigate to the location where you saved the file (type "CD <FileLocation>").</span></span>

<span data-ttu-id="a27c8-156">Exécutez le script en tapant :</span><span class="sxs-lookup"><span data-stu-id="a27c8-156">Run the script by typing:</span></span>

`.\GroupCreators.ps1`

<span data-ttu-id="a27c8-157">et [connectez-vous à l’invite avec votre compte](../enterprise/connect-to-microsoft-365-powershell.md#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription) d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a27c8-157">and [sign in with your administrator account](../enterprise/connect-to-microsoft-365-powershell.md#step-2-connect-to-azure-ad-for-your-microsoft-365-subscription) when prompted.</span></span>

```PowerShell
$GroupName = "<GroupName>"
$AllowGroupCreation = $False

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

<span data-ttu-id="a27c8-158">La dernière ligne du script affiche les paramètres mis à jour :</span><span class="sxs-lookup"><span data-stu-id="a27c8-158">The last line of the script will display the updated settings:</span></span>

![Capture d’écran de la sortie du script PowerShell.](../media/952cd982-5139-4080-9add-24bafca0830c.png)

<span data-ttu-id="a27c8-160">Si, à l’avenir, vous souhaitez modifier le groupe utilisé, vous pouvez réexécuter le script avec le nom du nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="a27c8-160">If in the future you want to change which group is used, you can rerun the script with the name of the new group.</span></span>

<span data-ttu-id="a27c8-161">Si vous souhaitez désactiver la restriction de création de groupe et autoriser à nouveau tous les utilisateurs à créer des groupes, définissez $GroupName sur « » et $AllowGroupCreation sur « True » et réexécutez le script.</span><span class="sxs-lookup"><span data-stu-id="a27c8-161">If you want to turn off the group creation restriction and again allow all users to create groups, set $GroupName to "" and $AllowGroupCreation to "True" and rerun the script.</span></span>

## <a name="step-3-verify-that-it-works"></a><span data-ttu-id="a27c8-162">Étape 3 : vérifier le bon fonctionnement</span><span class="sxs-lookup"><span data-stu-id="a27c8-162">Step 3: Verify that it works</span></span>

<span data-ttu-id="a27c8-163">L’application des modifications peut prendre 30 minutes ou plus.</span><span class="sxs-lookup"><span data-stu-id="a27c8-163">Changes can take thirty minutes or more to take effect.</span></span> <span data-ttu-id="a27c8-164">Vous pouvez vérifier les nouveaux paramètres en suivant les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="a27c8-164">You can verify the new settings by doing the following:</span></span>

1. <span data-ttu-id="a27c8-165">Connectez-vous à Microsoft 365 avec un compte d’utilisateur d’une personne qui ne doit PAS avoir la possibilité de créer des groupes.</span><span class="sxs-lookup"><span data-stu-id="a27c8-165">Sign in to Microsoft 365 with a user account of someone who should NOT have the ability to create groups.</span></span> <span data-ttu-id="a27c8-166">Autrement dit, ils ne sont pas membres du groupe que vous avez créé ou administrateur.</span><span class="sxs-lookup"><span data-stu-id="a27c8-166">That is, they are not a member of the group you created or an administrator.</span></span>

2. <span data-ttu-id="a27c8-167">Sélectionnez la **vignette Planificateur.**</span><span class="sxs-lookup"><span data-stu-id="a27c8-167">Select the **Planner** tile.</span></span>

3. <span data-ttu-id="a27c8-168">Dans le Planificateur, **sélectionnez Nouveau plan** dans le navigation de gauche pour créer un plan.</span><span class="sxs-lookup"><span data-stu-id="a27c8-168">In Planner, select **New Plan** in the left navigation to create a plan.</span></span>

4. <span data-ttu-id="a27c8-169">Vous devez obtenir un message vous messageant que la création de groupe et de plan est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a27c8-169">You should get a message that plan and group creation is disabled.</span></span>

<span data-ttu-id="a27c8-170">Essayez à nouveau la même procédure avec un membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="a27c8-170">Try the same procedure again with a member of the group.</span></span>

> [!NOTE]
> <span data-ttu-id="a27c8-171">Si les membres du groupe ne sont pas en mesure de créer des groupes, vérifiez qu’ils ne sont pas bloqués par le biais de [leur stratégie OWA boîte aux lettres.](/powershell/module/exchange/set-owamailboxpolicy)</span><span class="sxs-lookup"><span data-stu-id="a27c8-171">If members of the group aren't able to create groups, check that they aren't being blocked through their [OWA mailbox policy](/powershell/module/exchange/set-owamailboxpolicy).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a27c8-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a27c8-172">Related topics</span></span>

[<span data-ttu-id="a27c8-173">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="a27c8-173">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="a27c8-174">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="a27c8-174">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="a27c8-175">Mise en route d’Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="a27c8-175">Getting started with Office 365 PowerShell</span></span>](../enterprise/getting-started-with-microsoft-365-powershell.md)

[<span data-ttu-id="a27c8-176">Configurer la gestion des groupes libre-service dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a27c8-176">Set up self-service group management in Azure Active Directory</span></span>](/azure/active-directory/users-groups-roles/groups-self-service-management)

[<span data-ttu-id="a27c8-177">Set-ExecutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a27c8-177">Set-ExecutionPolicy</span></span>](/powershell/module/microsoft.powershell.security/set-executionpolicy)

[<span data-ttu-id="a27c8-178">Cmdlets Azure Active Directory pour la configuration de paramètres de groupe</span><span class="sxs-lookup"><span data-stu-id="a27c8-178">Azure Active Directory cmdlets for configuring group settings</span></span>](/azure/active-directory/users-groups-roles/groups-settings-cmdlets)