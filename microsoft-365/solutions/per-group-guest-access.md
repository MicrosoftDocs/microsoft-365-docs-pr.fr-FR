---
title: Bloquer les utilisateurs invités d’un groupe spécifique
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
ms.custom:
- M365solutions
f1.keywords: NOCSH
description: Bloquer les utilisateurs invités d’un groupe spécifique
ms.openlocfilehash: 2e9c9cae13932a33b8c486148f93901904e80006
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48328016"
---
# <a name="block-guest-users-from-a-specific-microsoft-365-group-or-microsoft-teams-team"></a><span data-ttu-id="0a2cb-103">Bloquer les utilisateurs invités d’un groupe Microsoft 365 spécifique ou d’une équipe Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="0a2cb-103">Block guest users from a specific Microsoft 365 group or Microsoft Teams team</span></span>

<span data-ttu-id="0a2cb-104">Si vous souhaitez autoriser l’accès invité à la plupart des groupes et des équipes, mais que vous avez certains pour lesquels vous souhaitez empêcher l’accès invité, vous pouvez bloquer l’accès invité pour des groupes et des équipes individuels.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-104">If you want to allow guest access to most groups and teams, but have some where you want to prevent guest access, you can block guest access for individual groups and teams.</span></span> <span data-ttu-id="0a2cb-105">(Le blocage de l’accès invité à une équipe est assuré par le blocage de l’accès invité au groupe associé.)</span><span class="sxs-lookup"><span data-stu-id="0a2cb-105">(Blocking guest access to a team is done by blocking guest access to the associated group.)</span></span>

<span data-ttu-id="0a2cb-106">Si vous utilisez des étiquettes de confidentialité dans votre organisation, nous vous recommandons de les utiliser pour contrôler l’accès invité par groupe.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-106">If you use sensitivity labels in your organization, we recommend using them to control guest access on a per-group basis.</span></span> <span data-ttu-id="0a2cb-107">Pour plus d’informations sur la procédure à suivre, [Utilisez les étiquettes de confidentialité pour protéger le contenu dans Microsoft Teams, les groupes microsoft 365 et les sites SharePoint](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span><span class="sxs-lookup"><span data-stu-id="0a2cb-107">For information about how to do this, [Use sensitivity labels to protect content in Microsoft Teams, Microsoft 365 groups, and SharePoint sites](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-teams-groups-sites).</span></span> <span data-ttu-id="0a2cb-108">Il s’agit de l’approche recommandée.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-108">This is the recommended approach.</span></span>

<span data-ttu-id="0a2cb-109">Vous pouvez également bloquer l’accès invité à des groupes individuels à l’aide de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-109">You can also block guest access to individual groups by using Microsoft PowerShell.</span></span>

<span data-ttu-id="0a2cb-110">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="0a2cb-110">You must use the preview version of [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="0a2cb-111">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-111">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="0a2cb-112">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-112">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="0a2cb-113">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-113">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

> [!NOTE]
> <span data-ttu-id="0a2cb-114">Vous devez disposer des droits d’administrateur globaux pour exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-114">You must have global admin rights to run these commands.</span></span> 

<span data-ttu-id="0a2cb-115">Exécutez le script suivant, */<GroupName/>* en remplaçant par le nom du groupe dans lequel vous souhaitez bloquer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-115">Run the following script, changing */<GroupName/>* to the name of the group where you want to block guest access.</span></span>

```PowerShell
$GroupName = "<GroupName>"

Connect-AzureAD

$template = Get-AzureADDirectorySettingTemplate | ? {$_.displayname -eq "group.unified.guest"}
$settingsCopy = $template.CreateDirectorySetting()
$settingsCopy["AllowToAddGuests"]=$False
$groupID= (Get-AzureADGroup -SearchString $GroupName).ObjectId
New-AzureADObjectSetting -TargetType Groups -TargetObjectId $groupID -DirectorySetting $settingsCopy
```

<span data-ttu-id="0a2cb-116">Pour vérifier vos paramètres, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0a2cb-116">To verify your settings, run this command:</span></span>

```PowerShell
Get-AzureADObjectSetting -TargetObjectId $groupID -TargetType Groups | fl Values
```

<span data-ttu-id="0a2cb-117">La vérification se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="0a2cb-117">The verification looks like this:</span></span>
    
![Capture d’écran de la fenêtre PowerShell indiquant que l’accès au groupe invité a été défini sur false.](../media/09ebfb4f-859f-44c3-a29e-63a59fd6ef87.png)
  
## <a name="allow-or-block-guest-access-based-on-their-domain"></a><span data-ttu-id="0a2cb-119">Autoriser ou bloquer l’accès invité en fonction de leur domaine</span><span class="sxs-lookup"><span data-stu-id="0a2cb-119">Allow or block guest access based on their domain</span></span>

<span data-ttu-id="0a2cb-120">Vous pouvez autoriser ou bloquer les utilisateurs invités qui utilisent un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-120">You can allow or block guest users who are using a specific domain.</span></span> <span data-ttu-id="0a2cb-121">Par exemple, si votre entreprise (contoso) a un partenariat avec une autre entreprise (Fabrikam), vous pouvez ajouter Fabrikam à votre liste verte afin que vos utilisateurs puissent ajouter ces invités à leurs groupes.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-121">For example, if your business (Contoso) has a partnership with another business (Fabrikam), you can add Fabrikam to your Allow list so your users can add those guests to their groups.</span></span>

<span data-ttu-id="0a2cb-122">Pour plus d’informations, reportez-vous à la rubrique [autoriser ou bloquer des invitations à des utilisateurs B2B d’organisations spécifiques](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span><span class="sxs-lookup"><span data-stu-id="0a2cb-122">For more information, see [Allow or block invitations to B2B users from specific organizations](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span></span>

## <a name="add-guests-to-the-global-address-list"></a><span data-ttu-id="0a2cb-123">Ajouter des invités à la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="0a2cb-123">Add guests to the global address list</span></span>

<span data-ttu-id="0a2cb-124">Par défaut, les invités ne sont pas visibles dans la liste d’adresses globale d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-124">By default, guests aren't visible in the Exchange Global Address List.</span></span> <span data-ttu-id="0a2cb-125">Utilisez les étapes répertoriées ci-dessous pour faire en sorte qu’un invité soit visible dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-125">Use the steps listed below to make a guest visible in the global address list.</span></span>

<span data-ttu-id="0a2cb-126">Recherchez l’ObjectID de l’utilisateur invité en exécutant :</span><span class="sxs-lookup"><span data-stu-id="0a2cb-126">Find the guest user's ObjectID by running:</span></span>

```PowerShell
Get-AzureADUser -Filter "userType eq 'Guest'"
```

<span data-ttu-id="0a2cb-127">Exécutez ensuite la commande suivante à l’aide des valeurs appropriées pour ObjectID, GivenName, Surname, DisplayName et TelephoneNumber.</span><span class="sxs-lookup"><span data-stu-id="0a2cb-127">Then run the following using the appropriate values for ObjectID, GivenName, Surname, DisplayName, and TelephoneNumber.</span></span>

```PowerShell
Set-AzureADUser -ObjectId cfcbd1a0-ed18-4210-9b9d-cf0ba93cf6b2 -ShowInAddressList $true -GivenName 'Megan' -Surname 'Bowen' -DisplayName 'Megan Bowen' -TelephoneNumber '555-555-5555'
```

## <a name="related-articles"></a><span data-ttu-id="0a2cb-128">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0a2cb-128">Related articles</span></span>

[<span data-ttu-id="0a2cb-129">Gérer l’appartenance au groupe dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0a2cb-129">Manage Group membership in the Microsoft 365 admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/create-groups/add-or-remove-members-from-groups)
  
[<span data-ttu-id="0a2cb-130">Avis d’accès à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0a2cb-130">Azure Active Directory access reviews</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-azure-ad-controls-perform-access-review)

[<span data-ttu-id="0a2cb-131">Set-AzureADUser</span><span class="sxs-lookup"><span data-stu-id="0a2cb-131">Set-AzureADUser</span></span>](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser)