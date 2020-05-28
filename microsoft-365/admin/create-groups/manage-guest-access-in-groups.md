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
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
- MOE150
ms.assetid: 9de497a9-2f5c-43d6-ae18-767f2e6fe6e0
description: Découvrez comment ajouter des invités à un groupe Microsoft 365, afficher des utilisateurs invités et utiliser PowerShell pour contrôler l’accès invité.
ms.openlocfilehash: 99288521f29d67f3146cafe1f194662750cc8a5d
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44386780"
---
# <a name="manage-guest-access-in-microsoft-365-groups"></a><span data-ttu-id="73dda-103">Gérer l’accès invité dans les groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="73dda-103">Manage guest access in Microsoft 365 groups</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="73dda-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="73dda-104">The admin center is changing.</span></span> <span data-ttu-id="73dda-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="73dda-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="73dda-106">Par défaut, l’accès invité pour les groupes Microsoft 365 est activé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="73dda-106">By default, guest access for Microsoft 365 groups is turned on for your organization.</span></span> <span data-ttu-id="73dda-107">Les administrateurs peuvent contrôler s’il faut autoriser l’accès invité à des groupes pour l’ensemble de l’organisation ou pour des groupes individuels.</span><span class="sxs-lookup"><span data-stu-id="73dda-107">Admins can control whether to allow guest access to groups for their whole organization or for individual groups.</span></span>

<span data-ttu-id="73dda-108">Lorsqu’elle est activée, les membres du groupe peuvent inviter des utilisateurs invités à un groupe Microsoft 365 via Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="73dda-108">When it's turned on, group members can invite guest users to a Microsoft 365 group through Outlook on Web.</span></span> <span data-ttu-id="73dda-109">Les invitations sont envoyées au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="73dda-109">Invitations are sent to the group owner for approval.</span></span>

> [!Note]
> <span data-ttu-id="73dda-110">Les réseaux d’entreprise yammer en mode natif ou dans l' [Union européenne](https://go.microsoft.com/fwlink/?linkid=2107357) ne prennent pas en charge les invités réseau.</span><span class="sxs-lookup"><span data-stu-id="73dda-110">Yammer Enterprise networks that are in Native Mode or the [EU Geo](https://go.microsoft.com/fwlink/?linkid=2107357) do not support network guests.</span></span>
> <span data-ttu-id="73dda-111">Les groupes Yammer connectés à Microsoft 365 ne prennent actuellement pas en charge l’accès invité, mais vous pouvez créer des groupes externes non connectés dans votre réseau Yammer.</span><span class="sxs-lookup"><span data-stu-id="73dda-111">Microsoft 365 Connected Yammer groups do not currently support guest access, but you can create non-connected, external groups in your Yammer network.</span></span> <span data-ttu-id="73dda-112">Consultez la rubrique [créer et gérer des groupes externes dans Yammer](https://docs.microsoft.com/yammer/work-with-external-users/create-and-manage-external-groups) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="73dda-112">See [Create and manage external groups in Yammer](https://docs.microsoft.com/yammer/work-with-external-users/create-and-manage-external-groups) for instructions.</span></span>

### <a name="edit-guest-information"></a><span data-ttu-id="73dda-113">Modifier les informations invité</span><span class="sxs-lookup"><span data-stu-id="73dda-113">Edit guest information</span></span>

<span data-ttu-id="73dda-114">Une fois approuvé, l’utilisateur invité est ajouté au répertoire et au groupe.</span><span class="sxs-lookup"><span data-stu-id="73dda-114">Once approved, the guest user is added to the directory and the group.</span></span>

<span data-ttu-id="73dda-115">L’accès invité dans des groupes est souvent utilisé dans le cadre d’un scénario plus large qui inclut SharePoint ou Teams.</span><span class="sxs-lookup"><span data-stu-id="73dda-115">Guest access in groups is often used as part of a broader scenario that includes SharePoint or Teams.</span></span> <span data-ttu-id="73dda-116">Ces services ont leurs propres paramètres de partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="73dda-116">These services have their own guest sharing settings.</span></span> <span data-ttu-id="73dda-117">Pour obtenir des instructions complètes sur la configuration du partage d’invités entre les groupes, SharePoint et Teams, voir :</span><span class="sxs-lookup"><span data-stu-id="73dda-117">For complete instructions for setting up guest sharing across groups, SharePoint, and Teams, see:</span></span>

- [<span data-ttu-id="73dda-118">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="73dda-118">Collaborate with guests in a site</span></span>](../../solutions/collaborate-in-site.md)
- [<span data-ttu-id="73dda-119">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="73dda-119">Collaborate with guests in a team</span></span>](../../solutions/collaborate-as-team.md)

## <a name="manage-groups-guest-access"></a><span data-ttu-id="73dda-120">Gérer les groupes accès invité</span><span class="sxs-lookup"><span data-stu-id="73dda-120">Manage groups guest access</span></span>

<span data-ttu-id="73dda-121">Si vous souhaitez activer ou désactiver l’accès invité dans des groupes, vous pouvez le faire dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73dda-121">If you want to enable or disable guest access in groups, you can do so in the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="73dda-122">Dans le centre d’administration, accédez aux **Settings** \> **paramètres** paramètres et sélectionnez **groupes Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="73dda-122">In the admin center, go to the **Settings** \> **Settings** and select **Microsoft 365 groups**.</span></span>
  
2. <span data-ttu-id="73dda-123">Sur la page **groupes Microsoft 365** , indiquez si vous souhaitez autoriser les personnes extérieures à votre organisation à accéder aux ressources de groupe ou les propriétaires de groupes à ajouter des personnes en dehors de votre organisation à des groupes.</span><span class="sxs-lookup"><span data-stu-id="73dda-123">On the **Microsoft 365 Groups** page, choose whether you want to let people outside your organization access group resources or let group owners add people outside your organization to groups.</span></span>

## <a name="add-guests-to-a-microsoft-365-group-from-the-admin-center"></a><span data-ttu-id="73dda-124">Ajouter des invités à un groupe Microsoft 365 à partir du centre d’administration</span><span class="sxs-lookup"><span data-stu-id="73dda-124">Add guests to a Microsoft 365 group from the admin center</span></span>

<span data-ttu-id="73dda-125">Si l’invité existe déjà dans votre répertoire, vous pouvez l’ajouter à vos groupes à partir du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73dda-125">If the guest already exists in your directory, you can add them to your groups from the Microsoft 365 admin center.</span></span>
  
1. <span data-ttu-id="73dda-126">Dans le centre d’administration, accédez à **la page groupes de**  >  **groupes** .</span><span class="sxs-lookup"><span data-stu-id="73dda-126">In the admin center, go to the **Groups** > **Groups** page.</span></span>
  
2. <span data-ttu-id="73dda-127">Cliquez sur le groupe auquel vous souhaitez ajouter l’invité, puis sélectionnez **Afficher tout et gérer les membres** sous l’onglet **membres** .</span><span class="sxs-lookup"><span data-stu-id="73dda-127">Click the group you want to add the guest to, and select **View all and manage members** on the **Members** tab.</span></span> 
  
4. <span data-ttu-id="73dda-128">Sélectionnez **Ajouter des membres**, puis choisissez le nom de l’invité que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="73dda-128">Select **Add members**, and choose the name of the guest you want to add.</span></span>
    
5. <span data-ttu-id="73dda-129">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="73dda-129">Select **Save**.</span></span>

<span data-ttu-id="73dda-130">Si vous souhaitez ajouter un invité directement à l’annuaire, vous pouvez [Ajouter des utilisateurs de collaboration B2B Azure Active Directory dans le portail Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="73dda-130">If you want to add a guest to the directory directly, you can [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

<span data-ttu-id="73dda-131">Si vous souhaitez modifier les informations d’un invité, vous pouvez [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="73dda-131">If you want to edit any of a guest's information, you can [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>
  
## <a name="block-guest-users-from-a-specific-group"></a><span data-ttu-id="73dda-132">Bloquer les utilisateurs invités d’un groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="73dda-132">Block guest users from a specific group</span></span>

<span data-ttu-id="73dda-133">Si vous souhaitez autoriser l’accès invité à la plupart des groupes, mais que vous souhaitez empêcher l’accès invité à la plupart des groupes à l’aide de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="73dda-133">If you want to allow guest access to most groups, but have some where you want to prevent guest access, you can block guest access for individual groups by using Microsoft PowerShell.</span></span>

<span data-ttu-id="73dda-134">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="73dda-134">You must use the preview version of [Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="73dda-135">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="73dda-135">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="73dda-136">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="73dda-136">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="73dda-137">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="73dda-137">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

> [!NOTE]
> <span data-ttu-id="73dda-138">Vous devez disposer des droits d’administrateur globaux pour exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="73dda-138">You must have global admin rights to run these commands.</span></span> 

<span data-ttu-id="73dda-139">Exécutez le script suivant, */<GroupName/>* en remplaçant par le nom du groupe dans lequel vous souhaitez bloquer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="73dda-139">Run the following script, changing */<GroupName/>* to the name of the group where you want to block guest access.</span></span>

```PowerShell
$GroupName = "<GroupName>"

Connect-AzureAD

$template = Get-AzureADDirectorySettingTemplate | ? {$_.displayname -eq "group.unified.guest"}
$settingsCopy = $template.CreateDirectorySetting()
$settingsCopy["AllowToAddGuests"]=$False
$groupID= (Get-AzureADGroup -SearchString $GroupName).ObjectId
New-AzureADObjectSetting -TargetType Groups -TargetObjectId $groupID -DirectorySetting $settingsCopy
```

<span data-ttu-id="73dda-140">Pour vérifier vos paramètres, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="73dda-140">To verify your settings, run this command:</span></span>

```PowerShell
Get-AzureADObjectSetting -TargetObjectId $groupID -TargetType Groups | fl Values
```

<span data-ttu-id="73dda-141">La vérification se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="73dda-141">The verification looks like this:</span></span>
    
![Capture d’écran de la fenêtre PowerShell indiquant que l’accès au groupe invité a été défini sur false.](../../media/09ebfb4f-859f-44c3-a29e-63a59fd6ef87.png)
  
## <a name="allow-or-block-guest-access-based-on-their-domain"></a><span data-ttu-id="73dda-143">Autoriser ou bloquer l’accès invité en fonction de leur domaine</span><span class="sxs-lookup"><span data-stu-id="73dda-143">Allow or block guest access based on their domain</span></span>

<span data-ttu-id="73dda-144">Vous pouvez autoriser ou bloquer les utilisateurs invités qui utilisent un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="73dda-144">You can allow or block guest users who are using a specific domain.</span></span> <span data-ttu-id="73dda-145">Par exemple, si votre entreprise (contoso) a un partenariat avec une autre entreprise (Fabrikam), vous pouvez ajouter Fabrikam à votre liste verte afin que vos utilisateurs puissent ajouter ces invités à leurs groupes.</span><span class="sxs-lookup"><span data-stu-id="73dda-145">For example, if your business (Contoso) has a partnership with another business (Fabrikam), you can add Fabrikam to your Allow list so your users can add those guests to their groups.</span></span>

<span data-ttu-id="73dda-146">Pour plus d’informations, reportez-vous à la rubrique [autoriser ou bloquer des invitations à des utilisateurs B2B d’organisations spécifiques](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span><span class="sxs-lookup"><span data-stu-id="73dda-146">For more information, see [Allow or block invitations to B2B users from specific organizations](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span></span>

## <a name="add-guests-to-the-global-address-list"></a><span data-ttu-id="73dda-147">Ajouter des invités à la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="73dda-147">Add guests to the global address list</span></span>

<span data-ttu-id="73dda-148">Par défaut, les invités ne sont pas visibles dans la liste d’adresses globale d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="73dda-148">By default, guests aren't visible in the Exchange Global Address List.</span></span> <span data-ttu-id="73dda-149">Utilisez les étapes répertoriées ci-dessous pour faire en sorte qu’un invité soit visible dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="73dda-149">Use the steps listed below to make a guest visible in the global address list.</span></span>

<span data-ttu-id="73dda-150">Recherchez l’ObjectID de l’utilisateur invité en exécutant :</span><span class="sxs-lookup"><span data-stu-id="73dda-150">Find the guest user's ObjectID by running:</span></span>

```PowerShell
Get-AzureADUser -Filter "userType eq 'Guest'"
```

<span data-ttu-id="73dda-151">Exécutez ensuite la commande suivante à l’aide des valeurs appropriées pour ObjectID, GivenName, Surname, DisplayName et TelephoneNumber.</span><span class="sxs-lookup"><span data-stu-id="73dda-151">Then run the following using the appropriate values for ObjectID, GivenName, Surname, DisplayName, and TelephoneNumber.</span></span>

```PowerShell
Set-AzureADUser -ObjectId cfcbd1a0-ed18-4210-9b9d-cf0ba93cf6b2 -ShowInAddressList $true -GivenName 'Megan' -Surname 'Bowen' -DisplayName 'Megan Bowen' -TelephoneNumber '555-555-5555'
```

## <a name="related-articles"></a><span data-ttu-id="73dda-152">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="73dda-152">Related articles</span></span>

[<span data-ttu-id="73dda-153">Gérer l’appartenance au groupe dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="73dda-153">Manage group membership in the Microsoft 365 admin center</span></span>](add-or-remove-members-from-groups.md)
  
[<span data-ttu-id="73dda-154">Avis d’accès à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="73dda-154">Azure Active Directory access reviews</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-azure-ad-controls-perform-access-review)

[<span data-ttu-id="73dda-155">Set-AzureADUser</span><span class="sxs-lookup"><span data-stu-id="73dda-155">Set-AzureADUser</span></span>](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser)
