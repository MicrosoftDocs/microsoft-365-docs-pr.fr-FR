---
title: Empêcher l’ajout d’invités à un groupe spécifique
ms.reviewer: arvaradh
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-collaboration
- m365solution-collabgovernance
ms.custom:
- M365solutions
f1.keywords: NOCSH
recommendations: false
description: Découvrez comment empêcher l’ajout d’invités à un groupe spécifique
ms.openlocfilehash: 1db2055f3e546c05905dbf4c854333387112f06e
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538926"
---
# <a name="prevent-guests-from-being-added-to-a-specific-microsoft-365-group-or-microsoft-teams-team"></a><span data-ttu-id="582b5-103">Empêcher l’ajout d’invités à un groupe Microsoft 365 ou une équipe Microsoft Teams spécifique</span><span class="sxs-lookup"><span data-stu-id="582b5-103">Prevent guests from being added to a specific Microsoft 365 group or Microsoft Teams team</span></span>

<span data-ttu-id="582b5-104">Si vous souhaitez autoriser l’accès invité à la plupart des groupes et équipes, mais que vous souhaitez en empêcher l’accès, vous pouvez bloquer l’accès invité pour des groupes et des équipes individuels.</span><span class="sxs-lookup"><span data-stu-id="582b5-104">If you want to allow guest access to most groups and teams, but have some where you want to prevent guest access, you can block guest access for individual groups and teams.</span></span> <span data-ttu-id="582b5-105">(Le blocage de l’accès invité à une équipe s’fait en bloquant l’accès invité au groupe associé.) Cela empêche l’ajout de nouveaux invités, mais ne supprime pas les invités qui sont déjà dans le groupe ou l’équipe.</span><span class="sxs-lookup"><span data-stu-id="582b5-105">(Blocking guest access to a team is done by blocking guest access to the associated group.) This prevents new guests from being added but does not remove guests that are already in the group or team.</span></span>

<span data-ttu-id="582b5-106">Si vous utilisez des étiquettes de niveau de sensibilité dans votre organisation, nous vous recommandons de les utiliser pour contrôler l’accès invité par groupe.</span><span class="sxs-lookup"><span data-stu-id="582b5-106">If you use sensitivity labels in your organization, we recommend using them to control guest access on a per-group basis.</span></span> <span data-ttu-id="582b5-107">Pour plus d’informations sur la façon de faire, utilisez des étiquettes de niveau de sensibilité pour protéger le contenu dans [Microsoft Teams, Microsoft 365 groupes](../compliance/sensitivity-labels-teams-groups-sites.md)et SharePoint sites.</span><span class="sxs-lookup"><span data-stu-id="582b5-107">For information about how to do this, [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](../compliance/sensitivity-labels-teams-groups-sites.md).</span></span> <span data-ttu-id="582b5-108">Il s’agit de l’approche recommandée.</span><span class="sxs-lookup"><span data-stu-id="582b5-108">This is the recommended approach.</span></span>

## <a name="change-group-settings-using-microsoft-powershell"></a><span data-ttu-id="582b5-109">Modifier les paramètres de groupe à l’aide de Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="582b5-109">Change group settings using Microsoft PowerShell</span></span>

<span data-ttu-id="582b5-110">Vous pouvez également empêcher l’ajout de nouveaux invités à des groupes individuels à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="582b5-110">You can also prevent the addition of new guests to individual groups by using PowerShell.</span></span> <span data-ttu-id="582b5-111">(N’oubliez pas que le site SharePoint de l’équipe possède des [contrôles de partage d’invités distincts.)](/sharepoint/change-external-sharing-site)</span><span class="sxs-lookup"><span data-stu-id="582b5-111">(Remember that the team's associated SharePoint site has [separate guest sharing controls](/sharepoint/change-external-sharing-site).)</span></span>

<span data-ttu-id="582b5-112">Vous devez utiliser la version d’aperçu [de Azure Active Directory PowerShell pour Graph](/powershell/azure/active-directory/install-adv2) (nom du module **AzureADPreview**) pour modifier le paramètre d’accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="582b5-112">You must use the preview version of [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="582b5-113">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](/powershell/azure/active-directory/install-adv2?preserve-view=true&view=azureadps-2.0-preview) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="582b5-113">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](/powershell/azure/active-directory/install-adv2?preserve-view=true&view=azureadps-2.0-preview) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="582b5-114">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="582b5-114">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="582b5-115">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="582b5-115">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

> [!NOTE]
> <span data-ttu-id="582b5-116">Vous devez avoir des droits d’administrateur général pour exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="582b5-116">You must have global admin rights to run these commands.</span></span> 

<span data-ttu-id="582b5-117">Exécutez le script suivant, en accédant au nom du groupe dans lequel */<GroupName/>* vous souhaitez bloquer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="582b5-117">Run the following script, changing */<GroupName/>* to the name of the group where you want to block guest access.</span></span>

```PowerShell
$GroupName = "<GroupName>"

Connect-AzureAD

$template = Get-AzureADDirectorySettingTemplate | ? {$_.displayname -eq "group.unified.guest"}
$settingsCopy = $template.CreateDirectorySetting()
$settingsCopy["AllowToAddGuests"]=$False
$groupID= (Get-AzureADGroup -SearchString $GroupName).ObjectId
New-AzureADObjectSetting -TargetType Groups -TargetObjectId $groupID -DirectorySetting $settingsCopy
```

<span data-ttu-id="582b5-118">Pour vérifier vos paramètres, exécutez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="582b5-118">To verify your settings, run this command:</span></span>

```PowerShell
Get-AzureADObjectSetting -TargetObjectId $groupID -TargetType Groups | fl Values
```

<span data-ttu-id="582b5-119">La vérification ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="582b5-119">The verification looks like this:</span></span>
    
![Capture d’écran de la fenêtre PowerShell montrant que l’accès au groupe d’invités a été définie sur false.](../media/09ebfb4f-859f-44c3-a29e-63a59fd6ef87.png)
  
## <a name="allow-or-block-guest-access-based-on-their-domain"></a><span data-ttu-id="582b5-121">Autoriser ou bloquer l’accès invité en fonction de son domaine</span><span class="sxs-lookup"><span data-stu-id="582b5-121">Allow or block guest access based on their domain</span></span>

<span data-ttu-id="582b5-122">Vous pouvez autoriser ou bloquer les invités qui utilisent un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="582b5-122">You can allow or block guests who are using a specific domain.</span></span> <span data-ttu-id="582b5-123">Par exemple, si votre entreprise (Contoso) a un partenariat avec une autre entreprise (Fabrikam), vous pouvez ajouter Fabrikam à votre liste d’invités pour permettre à vos utilisateurs d’ajouter ces invités à leurs groupes.</span><span class="sxs-lookup"><span data-stu-id="582b5-123">For example, if your business (Contoso) has a partnership with another business (Fabrikam), you can add Fabrikam to your Allow list so your users can add those guests to their groups.</span></span>

<span data-ttu-id="582b5-124">Pour plus d’informations, voir Autoriser ou bloquer les invitations à [des utilisateurs B2B d’organisations spécifiques.](/azure/active-directory/b2b/allow-deny-list)</span><span class="sxs-lookup"><span data-stu-id="582b5-124">For more information, see [Allow or block invitations to B2B users from specific organizations](/azure/active-directory/b2b/allow-deny-list).</span></span>

## <a name="add-guests-to-the-global-address-list"></a><span data-ttu-id="582b5-125">Ajouter des invités à la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="582b5-125">Add guests to the global address list</span></span>

<span data-ttu-id="582b5-126">Par défaut, les invités ne sont pas visibles dans la Exchange d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="582b5-126">By default, guests aren't visible in the Exchange Global Address List.</span></span> <span data-ttu-id="582b5-127">Utilisez les étapes répertoriées ci-dessous pour rendre un invité visible dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="582b5-127">Use the steps listed below to make a guest visible in the global address list.</span></span>

<span data-ttu-id="582b5-128">Recherchez l’ObjectID de l’invité en exécutant :</span><span class="sxs-lookup"><span data-stu-id="582b5-128">Find the guest's ObjectID by running:</span></span>

```PowerShell
Get-AzureADUser -Filter "userType eq 'Guest'"
```

<span data-ttu-id="582b5-129">Exécutez ensuite ce qui suit en utilisant les valeurs appropriées pour ObjectID, GivenName, Surname, DisplayName et TelephoneNumber.</span><span class="sxs-lookup"><span data-stu-id="582b5-129">Then run the following using the appropriate values for ObjectID, GivenName, Surname, DisplayName, and TelephoneNumber.</span></span>

```PowerShell
Set-AzureADUser -ObjectId cfcbd1a0-ed18-4210-9b9d-cf0ba93cf6b2 -ShowInAddressList $true -GivenName 'Megan' -Surname 'Bowen' -DisplayName 'Megan Bowen' -TelephoneNumber '555-555-5555'
```

## <a name="related-topics"></a><span data-ttu-id="582b5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="582b5-130">Related topics</span></span>

[<span data-ttu-id="582b5-131">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="582b5-131">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="582b5-132">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="582b5-132">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="582b5-133">Gérer l’appartenance à un groupe dans Microsoft 365'administration centrale</span><span class="sxs-lookup"><span data-stu-id="582b5-133">Manage Group membership in the Microsoft 365 admin center</span></span>](../admin/create-groups/add-or-remove-members-from-groups.md)
  
[<span data-ttu-id="582b5-134">Azure Active Directory’accès aux données</span><span class="sxs-lookup"><span data-stu-id="582b5-134">Azure Active Directory access reviews</span></span>](/azure/active-directory/active-directory-azure-ad-controls-perform-access-review)

[<span data-ttu-id="582b5-135">Set-AzureADUser</span><span class="sxs-lookup"><span data-stu-id="582b5-135">Set-AzureADUser</span></span>](/powershell/module/azuread/set-azureaduser)