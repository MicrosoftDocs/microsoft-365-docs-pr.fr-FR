---
title: Gérer l’accès invité dans les groupes Microsoft 365
ms.reviewer: arvaradh
f1.keywords: NOCSH
ms.author: mikeplum
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
- MET150
- MOE150
ms.assetid: 9de497a9-2f5c-43d6-ae18-767f2e6fe6e0
description: Découvrez comment ajouter des invités à un groupe Microsoft 365, afficher des utilisateurs invités et utiliser PowerShell pour contrôler l’accès invité.
ms.openlocfilehash: cca1d3dff4d95f5b15b9f18d5eeebcf054e52fe3
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43630066"
---
# <a name="manage-guest-access-in-microsoft-365-groups"></a><span data-ttu-id="d5ee5-103">Gérer l’accès invité dans les groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d5ee5-103">Manage guest access in Microsoft 365 groups</span></span>

<span data-ttu-id="d5ee5-104">Par défaut, l’accès invité pour les groupes Microsoft 365 est activé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-104">By default, guest access for Microsoft 365 groups is turned on for your organization.</span></span> <span data-ttu-id="d5ee5-105">Les administrateurs peuvent contrôler s’il faut autoriser l’accès invité à des groupes pour l’ensemble de l’organisation ou pour des groupes individuels.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-105">Admins can control whether to allow guest access to groups for their whole organization or for individual groups.</span></span>

<span data-ttu-id="d5ee5-106">Lorsqu’elle est activée, les membres du groupe peuvent inviter des utilisateurs invités à un groupe Microsoft 365 via Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-106">When it's turned on, group members can invite guest users to a Microsoft 365 group through Outlook on Web.</span></span> <span data-ttu-id="d5ee5-107">Les invitations sont envoyées au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-107">Invitations are sent to the group owner for approval.</span></span>

> [!Note]
> <span data-ttu-id="d5ee5-108">Les réseaux d’entreprise yammer en mode natif ou dans l' [Union européenne](https://go.microsoft.com/fwlink/?linkid=2107357) ne prennent pas en charge les invités réseau.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-108">Yammer Enterprise networks that are in Native Mode or the [EU Geo](https://go.microsoft.com/fwlink/?linkid=2107357) do not support network guests.</span></span>
> <span data-ttu-id="d5ee5-109">Les groupes Yammer connectés à Microsoft 365 ne prennent actuellement pas en charge l’accès invité, mais vous pouvez créer des groupes externes non connectés dans votre réseau Yammer.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-109">Microsoft 365 Connected Yammer groups do not currently support guest access, but you can create non-connected, external groups in your Yammer network.</span></span> <span data-ttu-id="d5ee5-110">Consultez la rubrique [créer et gérer des groupes externes dans Yammer](https://support.office.com/article/9ccd15ce-0efc-4dc1-81bc-4a424ab6f92a.aspx) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-110">See [Create and manage external groups in Yammer](https://support.office.com/article/9ccd15ce-0efc-4dc1-81bc-4a424ab6f92a.aspx) for instructions.</span></span>

### <a name="edit-guest-information"></a><span data-ttu-id="d5ee5-111">Modifier les informations invité</span><span class="sxs-lookup"><span data-stu-id="d5ee5-111">Edit guest information</span></span>

<span data-ttu-id="d5ee5-112">Une fois approuvé, l’utilisateur invité est ajouté au répertoire et au groupe.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-112">Once approved, the guest user is added to the directory and the group.</span></span>

<span data-ttu-id="d5ee5-113">L’accès invité dans des groupes est souvent utilisé dans le cadre d’un scénario plus large qui inclut SharePoint ou Teams.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-113">Guest access in groups is often used as part of a broader scenario that includes SharePoint or Teams.</span></span> <span data-ttu-id="d5ee5-114">Ces services ont leurs propres paramètres de partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-114">These services have their own guest sharing settings.</span></span> <span data-ttu-id="d5ee5-115">Pour obtenir des instructions complètes sur la configuration du partage d’invités entre les groupes, SharePoint et Teams, voir :</span><span class="sxs-lookup"><span data-stu-id="d5ee5-115">For complete instructions for setting up guest sharing across groups, SharePoint, and Teams, see:</span></span>

- [<span data-ttu-id="d5ee5-116">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="d5ee5-116">Collaborate with guests in a site</span></span>](../../solutions/collaborate-in-site.md)
- [<span data-ttu-id="d5ee5-117">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="d5ee5-117">Collaborate with guests in a team</span></span>](../../solutions/collaborate-as-team.md)

## <a name="manage-groups-guest-access"></a><span data-ttu-id="d5ee5-118">Gérer les groupes accès invité</span><span class="sxs-lookup"><span data-stu-id="d5ee5-118">Manage groups guest access</span></span>

<span data-ttu-id="d5ee5-119">Si vous souhaitez activer ou désactiver l’accès invité dans des groupes, vous pouvez le faire dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-119">If you want to enable or disable guest access in groups, you can do so in the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="d5ee5-120">Dans le centre d’administration, accédez aux **Settings** \> **paramètres** paramètres et sélectionnez **groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-120">In the admin center, go to the **Settings** \> **Settings** and select **Microsoft 365 groups**.</span></span>
  
2. <span data-ttu-id="d5ee5-121">Sur la page **groupes Microsoft 365** , indiquez si vous souhaitez autoriser les personnes extérieures à votre organisation à accéder aux ressources de groupe ou les propriétaires de groupes à ajouter des personnes en dehors de votre organisation à des groupes.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-121">On the **Microsoft 365 Groups** page, choose whether you want to let people outside your organization access group resources or let group owners add people outside your organization to groups.</span></span>

## <a name="add-guests-to-a-microsoft-365-group-from-the-admin-center"></a><span data-ttu-id="d5ee5-122">Ajouter des invités à un groupe Microsoft 365 à partir du centre d’administration</span><span class="sxs-lookup"><span data-stu-id="d5ee5-122">Add guests to a Microsoft 365 group from the admin center</span></span>

<span data-ttu-id="d5ee5-123">Si l’invité existe déjà dans votre répertoire, vous pouvez l’ajouter à vos groupes à partir du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-123">If the guest already exists in your directory, you can add them to your groups from the Microsoft 365 admin center.</span></span>
  
1. <span data-ttu-id="d5ee5-124">Dans le centre d’administration, accédez > à **la page groupes de\*\*\*\*groupes.**</span><span class="sxs-lookup"><span data-stu-id="d5ee5-124">In the admin center, go to the **Groups** > **Groups** page.</span></span>
  
2. <span data-ttu-id="d5ee5-125">Cliquez sur le groupe auquel vous souhaitez ajouter l’invité, puis sélectionnez **Afficher tout et gérer les membres** sous l’onglet **membres** .</span><span class="sxs-lookup"><span data-stu-id="d5ee5-125">Click the group you want to add the guest to, and select **View all and manage members** on the **Members** tab.</span></span> 
  
4. <span data-ttu-id="d5ee5-126">Sélectionnez **Ajouter des membres**, puis choisissez le nom de l’invité que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-126">Select **Add members**, and choose the name of the guest you want to add.</span></span>
    
5. <span data-ttu-id="d5ee5-127">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-127">Select **Save**.</span></span>

<span data-ttu-id="d5ee5-128">Si vous souhaitez ajouter un invité directement à l’annuaire, vous pouvez [Ajouter des utilisateurs de collaboration B2B Azure Active Directory dans le portail Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="d5ee5-128">If you want to add a guest to the directory directly, you can [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

<span data-ttu-id="d5ee5-129">Si vous souhaitez modifier les informations d’un invité, vous pouvez [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="d5ee5-129">If you want to edit any of a guest's information, you can [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>
  
## <a name="block-guest-users-from-a-specific-group"></a><span data-ttu-id="d5ee5-130">Bloquer les utilisateurs invités d’un groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="d5ee5-130">Block guest users from a specific group</span></span>

<span data-ttu-id="d5ee5-131">Si vous souhaitez autoriser l’accès invité à la plupart des groupes, mais que vous souhaitez empêcher l’accès invité à la plupart des groupes à l’aide de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-131">If you want to allow guest access to most groups, but have some where you want to prevent guest access, you can block guest access for individual groups by using Microsoft PowerShell.</span></span>

<span data-ttu-id="d5ee5-132">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="d5ee5-132">You must use the preview version of [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="d5ee5-133">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-133">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="d5ee5-134">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-134">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="d5ee5-135">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-135">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

> [!NOTE]
> <span data-ttu-id="d5ee5-136">Vous devez disposer des droits d’administrateur globaux pour exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-136">You must have global admin rights to run these commands.</span></span> 

<span data-ttu-id="d5ee5-137">Exécutez le script suivant, en \* / \* remplaçant par le nom du groupe dans lequel vous souhaitez bloquer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-137">Run the following script, changing */<GroupName/>* to the name of the group where you want to block guest access.</span></span>

```PowerShell
$GroupName = "<GroupName>"

Connect-AzureAD

$template = Get-AzureADDirectorySettingTemplate | ? {$_.displayname -eq "group.unified.guest"}
$settingsCopy = $template.CreateDirectorySetting()
$settingsCopy["AllowToAddGuests"]=$False
$groupID= (Get-AzureADGroup -SearchString $GroupName).ObjectId
New-AzureADObjectSetting -TargetType Groups -TargetObjectId $groupID -DirectorySetting $settingsCopy
```

<span data-ttu-id="d5ee5-138">Pour vérifier vos paramètres, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d5ee5-138">To verify your settings, run this command:</span></span>

```PowerShell
Get-AzureADObjectSetting -TargetObjectId $groupID -TargetType Groups | fl Values
```

<span data-ttu-id="d5ee5-139">La vérification se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5ee5-139">The verification looks like this:</span></span>
    
![Capture d’écran de la fenêtre PowerShell indiquant que l’accès au groupe invité a été défini sur false.](../../media/09ebfb4f-859f-44c3-a29e-63a59fd6ef87.png)
  
## <a name="allow-or-block-guest-access-based-on-their-domain"></a><span data-ttu-id="d5ee5-141">Autoriser ou bloquer l’accès invité en fonction de leur domaine</span><span class="sxs-lookup"><span data-stu-id="d5ee5-141">Allow or block guest access based on their domain</span></span>

<span data-ttu-id="d5ee5-142">Vous pouvez autoriser ou bloquer les utilisateurs invités qui utilisent un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-142">You can allow or block guest users who are using a specific domain.</span></span> <span data-ttu-id="d5ee5-143">Par exemple, si votre entreprise (contoso) a un partenariat avec une autre entreprise (Fabrikam), vous pouvez ajouter Fabrikam à votre liste verte afin que vos utilisateurs puissent ajouter ces invités à leurs groupes.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-143">For example, if your business (Contoso) has a partnership with another business (Fabrikam), you can add Fabrikam to your Allow list so your users can add those guests to their groups.</span></span>

<span data-ttu-id="d5ee5-144">Pour plus d’informations, reportez-vous à la rubrique [autoriser ou bloquer des invitations à des utilisateurs B2B d’organisations spécifiques](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span><span class="sxs-lookup"><span data-stu-id="d5ee5-144">For more information, see [Allow or block invitations to B2B users from specific organizations](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span></span>

## <a name="add-guests-to-the-global-address-list"></a><span data-ttu-id="d5ee5-145">Ajouter des invités à la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="d5ee5-145">Add guests to the global address list</span></span>

<span data-ttu-id="d5ee5-146">Par défaut, les invités ne sont pas visibles dans la liste d’adresses globale d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-146">By default, guests aren't visible in the Exchange Global Address List.</span></span> <span data-ttu-id="d5ee5-147">Utilisez les étapes répertoriées ci-dessous pour faire en sorte qu’un invité soit visible dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-147">Use the steps listed below to make a guest visible in the global address list.</span></span>

<span data-ttu-id="d5ee5-148">Recherchez l’ObjectID de l’utilisateur invité en exécutant :</span><span class="sxs-lookup"><span data-stu-id="d5ee5-148">Find the guest user's ObjectID by running:</span></span>

```PowerShell
Get-AzureADUser -Filter "userType eq 'Guest'"
```

<span data-ttu-id="d5ee5-149">Exécutez ensuite la commande suivante à l’aide des valeurs appropriées pour ObjectID, GivenName, Surname, DisplayName et TelephoneNumber.</span><span class="sxs-lookup"><span data-stu-id="d5ee5-149">Then run the following using the appropriate values for ObjectID, GivenName, Surname, DisplayName, and TelephoneNumber.</span></span>

```PowerShell
Set-AzureADUser -ObjectId cfcbd1a0-ed18-4210-9b9d-cf0ba93cf6b2 -ShowInAddressList $true -GivenName 'Megan' -Surname 'Bowen' -DisplayName 'Megan Bowen' -TelephoneNumber '555-555-5555'
```

## <a name="related-articles"></a><span data-ttu-id="d5ee5-150">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d5ee5-150">Related articles</span></span>

[<span data-ttu-id="d5ee5-151">Gérer l’appartenance au groupe dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d5ee5-151">Manage group membership in the Microsoft 365 admin center</span></span>](add-or-remove-members-from-groups.md)
  
[<span data-ttu-id="d5ee5-152">Avis d’accès à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d5ee5-152">Azure Active Directory access reviews</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-azure-ad-controls-perform-access-review)

[<span data-ttu-id="d5ee5-153">Set-AzureADUser</span><span class="sxs-lookup"><span data-stu-id="d5ee5-153">Set-AzureADUser</span></span>](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser)
