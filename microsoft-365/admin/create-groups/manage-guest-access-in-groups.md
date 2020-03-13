---
title: Gérer l’accès invité dans les groupes Office 365
ms.reviewer: arvaradh
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.date: 12/18/2019
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
description: Découvrez comment ajouter des invités à un groupe Office 365, afficher les utilisateurs invités et utiliser PowerShell pour contrôler l’accès invité.
ms.openlocfilehash: 3314746e4d12c318eaae8fbfa34c2ed0b4d31aed
ms.sourcegitcommit: dcea75af89f5f80ec6670346ee176407e043de54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2020
ms.locfileid: "42610611"
---
# <a name="manage-guest-access-in-office-365-groups"></a><span data-ttu-id="fcefe-103">Gérer l’accès invité dans les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="fcefe-103">Manage guest access in Office 365 Groups</span></span>

<span data-ttu-id="fcefe-104">Par défaut, l’accès invité pour les groupes Office 365 est activé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fcefe-104">By default, guest access for Office 365 groups is turned on for your organization.</span></span> <span data-ttu-id="fcefe-105">Les administrateurs peuvent contrôler s’il faut autoriser l’accès invité à des groupes pour l’ensemble de l’organisation ou pour des groupes individuels.</span><span class="sxs-lookup"><span data-stu-id="fcefe-105">Admins can control whether to allow guest access to groups for their whole organization or for individual groups.</span></span>

<span data-ttu-id="fcefe-106">Lorsqu’elle est activée, les membres du groupe peuvent inviter des utilisateurs invités à un groupe Office 365 via Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="fcefe-106">When it's turned on, group members can invite guest users to an Office 365 group through Outlook on Web.</span></span> <span data-ttu-id="fcefe-107">Les invitations sont envoyées au propriétaire du groupe pour approbation.</span><span class="sxs-lookup"><span data-stu-id="fcefe-107">Invitations are sent to the group owner for approval.</span></span>

> [!Note]
> <span data-ttu-id="fcefe-108">Les réseaux d’entreprise yammer en mode natif ou dans l' [Union européenne](https://go.microsoft.com/fwlink/?linkid=2107357) ne prennent pas en charge les invités réseau.</span><span class="sxs-lookup"><span data-stu-id="fcefe-108">Yammer Enterprise networks that are in Native Mode or the [EU Geo](https://go.microsoft.com/fwlink/?linkid=2107357) do not support network guests.</span></span>
> <span data-ttu-id="fcefe-109">Les groupes Yammer connectés à Office 365 ne prennent actuellement pas en charge l’accès invité, mais vous pouvez créer des groupes externes non connectés dans votre réseau Yammer.</span><span class="sxs-lookup"><span data-stu-id="fcefe-109">Office 365 Connected Yammer Groups do not currently support guest access, but you can create non-connected, external groups in your Yammer network.</span></span> <span data-ttu-id="fcefe-110">Consultez la rubrique [créer et gérer des groupes externes dans Yammer](https://support.office.com/article/9ccd15ce-0efc-4dc1-81bc-4a424ab6f92a.aspx) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="fcefe-110">See [Create and manage external groups in Yammer](https://support.office.com/article/9ccd15ce-0efc-4dc1-81bc-4a424ab6f92a.aspx) for instructions.</span></span>

### <a name="edit-guest-information"></a><span data-ttu-id="fcefe-111">Modifier les informations invité</span><span class="sxs-lookup"><span data-stu-id="fcefe-111">Edit guest information</span></span>

<span data-ttu-id="fcefe-112">Une fois approuvé, l’utilisateur invité est ajouté au répertoire et au groupe.</span><span class="sxs-lookup"><span data-stu-id="fcefe-112">Once approved, the guest user is added to the directory and the group.</span></span>

<span data-ttu-id="fcefe-113">L’accès invité dans des groupes est souvent utilisé dans le cadre d’un scénario plus large qui inclut SharePoint ou Teams.</span><span class="sxs-lookup"><span data-stu-id="fcefe-113">Guest access in groups is often used as part of a broader scenario that includes SharePoint or Teams.</span></span> <span data-ttu-id="fcefe-114">Ces services ont leurs propres paramètres de partage d’invités.</span><span class="sxs-lookup"><span data-stu-id="fcefe-114">These services have their own guest sharing settings.</span></span> <span data-ttu-id="fcefe-115">Pour obtenir des instructions complètes sur la configuration du partage d’invités entre les groupes, SharePoint et Teams, voir :</span><span class="sxs-lookup"><span data-stu-id="fcefe-115">For complete instructions for setting up guest sharing across groups, SharePoint, and Teams, see:</span></span>

- [<span data-ttu-id="fcefe-116">Collaborer avec des invités sur un site</span><span class="sxs-lookup"><span data-stu-id="fcefe-116">Collaborate with guests in a site</span></span>](../../solutions/collaborate-in-site.md)
- [<span data-ttu-id="fcefe-117">Collaborer avec des invités au sein d’une équipe</span><span class="sxs-lookup"><span data-stu-id="fcefe-117">Collaborate with guests in a team</span></span>](../../solutions/collaborate-as-team.md)

## <a name="manage-groups-guest-access"></a><span data-ttu-id="fcefe-118">Gérer les groupes accès invité</span><span class="sxs-lookup"><span data-stu-id="fcefe-118">Manage groups guest access</span></span>

<span data-ttu-id="fcefe-119">Si vous souhaitez activer ou désactiver l’accès invité dans des groupes, vous pouvez le faire dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fcefe-119">If you want to enable or disable guest access in groups, you can do so in the Microsoft 365 admin center.</span></span>

1. <span data-ttu-id="fcefe-120">Dans le centre d’administration, accédez à la page **paramètres** \> de <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">& des compléments</a> .</span><span class="sxs-lookup"><span data-stu-id="fcefe-120">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2053743" target="_blank">Services & add-ins</a> page.</span></span>

2. <span data-ttu-id="fcefe-121">Sélectionnez **groupes Office 365**.</span><span class="sxs-lookup"><span data-stu-id="fcefe-121">Select **Office 365 Groups**.</span></span>
  
3. <span data-ttu-id="fcefe-122">Sur la page **groupes Office 365** , indiquez si vous souhaitez autoriser les personnes extérieures à votre organisation à accéder aux ressources de groupe ou les propriétaires de groupes à ajouter des personnes en dehors de votre organisation à des groupes.</span><span class="sxs-lookup"><span data-stu-id="fcefe-122">On the **Office 365 Groups** page, choose whether you want to let people outside your organization access group resources or let group owners add people outside your organization to groups.</span></span>

## <a name="add-guests-to-an-office-365-group-from-the-admin-center"></a><span data-ttu-id="fcefe-123">Ajouter des invités à un groupe Office 365 à partir du centre d’administration</span><span class="sxs-lookup"><span data-stu-id="fcefe-123">Add guests to an Office 365 group from the admin center</span></span>

<span data-ttu-id="fcefe-124">Si l’invité existe déjà dans votre répertoire, vous pouvez l’ajouter à vos groupes à partir du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fcefe-124">If the guest already exists in your directory, you can add them to your groups from the Microsoft 365 admin center.</span></span>
  
1. <span data-ttu-id="fcefe-125">Dans le centre d’administration, accédez > à **la page groupes de\*\*\*\*groupes.**</span><span class="sxs-lookup"><span data-stu-id="fcefe-125">In the admin center, go to the **Groups** > **Groups** page.</span></span>
  
2. <span data-ttu-id="fcefe-126">Sélectionnez le groupe auquel vous souhaitez ajouter l’invité, puis sélectionnez **Afficher tout et gérer les membres** sous l’onglet **membres** .</span><span class="sxs-lookup"><span data-stu-id="fcefe-126">Select the group you want to add the guest to, and select **View all and manage members** on the **Members** tab.</span></span> 
  
4. <span data-ttu-id="fcefe-127">Sélectionnez **Ajouter des membres**, puis choisissez le nom de l’invité que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="fcefe-127">Select **Add members**, and choose the name of the guest you want to add.</span></span>
    
5. <span data-ttu-id="fcefe-128">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fcefe-128">Select **Save**.</span></span>

<span data-ttu-id="fcefe-129">Si vous souhaitez ajouter un invité directement à l’annuaire, vous pouvez [Ajouter des utilisateurs de collaboration B2B Azure Active Directory dans le portail Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="fcefe-129">If you want to add a guest to the directory directly, you can [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

<span data-ttu-id="fcefe-130">Si vous souhaitez modifier les informations d’un invité, vous pouvez [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="fcefe-130">If you want to edit any of a guest's information, you can [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>
  
## <a name="block-guest-users-from-a-specific-group"></a><span data-ttu-id="fcefe-131">Bloquer les utilisateurs invités d’un groupe spécifique</span><span class="sxs-lookup"><span data-stu-id="fcefe-131">Block guest users from a specific group</span></span>

<span data-ttu-id="fcefe-132">Si vous souhaitez autoriser l’accès invité à la plupart des groupes, mais que vous souhaitez empêcher l’accès invité à la plupart des groupes à l’aide de Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fcefe-132">If you want to allow guest access to most groups, but have some where you want to prevent guest access, you can block guest access for individual groups by using Microsoft PowerShell.</span></span>

<span data-ttu-id="fcefe-133">Vous devez utiliser la version d’évaluation d' [Azure Active Directory PowerShell pour Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (nom de module **AzureADPreview**) pour modifier le paramètre d’accès invité au niveau du groupe :</span><span class="sxs-lookup"><span data-stu-id="fcefe-133">You must use the preview version of [Azure Active Directory PowerShell for Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) (module name **AzureADPreview**) to change the group-level guest access setting:</span></span>

- <span data-ttu-id="fcefe-134">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="fcefe-134">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="fcefe-135">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="fcefe-135">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="fcefe-136">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="fcefe-136">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

> [!NOTE]
> <span data-ttu-id="fcefe-137">Vous devez disposer des droits d’administrateur globaux pour exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="fcefe-137">You must have global admin rights to run these commands.</span></span> 

<span data-ttu-id="fcefe-138">Exécutez le script suivant, en \* / \* remplaçant par le nom du groupe dans lequel vous souhaitez bloquer l’accès invité.</span><span class="sxs-lookup"><span data-stu-id="fcefe-138">Run the following script, changing */<GroupName/>* to the name of the group where you want to block guest access.</span></span>

```PowerShell
$GroupName = "<GroupName>"

Connect-AzureAD

$template = Get-AzureADDirectorySettingTemplate | ? {$_.displayname -eq "group.unified.guest"}
$settingsCopy = $template.CreateDirectorySetting()
$settingsCopy["AllowToAddGuests"]=$False
$groupID= (Get-AzureADGroup -SearchString $GroupName).ObjectId
New-AzureADObjectSetting -TargetType Groups -TargetObjectId $groupID -DirectorySetting $settingsCopy
```

<span data-ttu-id="fcefe-139">Pour vérifier vos paramètres, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fcefe-139">To verify your settings, run this command:</span></span>

```PowerShell
Get-AzureADObjectSetting -TargetObjectId $groupID -TargetType Groups | fl Values
```

<span data-ttu-id="fcefe-140">La vérification se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="fcefe-140">The verification looks like this:</span></span>
    
![Capture d’écran de la fenêtre PowerShell indiquant que l’accès au groupe invité a été défini sur false.](../../media/09ebfb4f-859f-44c3-a29e-63a59fd6ef87.png)
  
## <a name="allow-or-block-guest-access-based-on-their-domain"></a><span data-ttu-id="fcefe-142">Autoriser ou bloquer l’accès invité en fonction de leur domaine</span><span class="sxs-lookup"><span data-stu-id="fcefe-142">Allow or block guest access based on their domain</span></span>

<span data-ttu-id="fcefe-143">Vous pouvez autoriser ou bloquer les utilisateurs invités qui utilisent un domaine spécifique.</span><span class="sxs-lookup"><span data-stu-id="fcefe-143">You can allow or block guest users who are using a specific domain.</span></span> <span data-ttu-id="fcefe-144">Par exemple, si votre entreprise (contoso) a un partenariat avec une autre entreprise (Fabrikam), vous pouvez ajouter Fabrikam à votre liste verte afin que vos utilisateurs puissent ajouter ces invités à leurs groupes.</span><span class="sxs-lookup"><span data-stu-id="fcefe-144">For example, if your business (Contoso) has a partnership with another business (Fabrikam), you can add Fabrikam to your Allow list so your users can add those guests to their groups.</span></span>

<span data-ttu-id="fcefe-145">Pour plus d’informations, reportez-vous à la rubrique [autoriser ou bloquer des invitations à des utilisateurs B2B d’organisations spécifiques](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span><span class="sxs-lookup"><span data-stu-id="fcefe-145">For more information, see [Allow or block invitations to B2B users from specific organizations](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list).</span></span>

## <a name="add-guests-to-the-global-address-list"></a><span data-ttu-id="fcefe-146">Ajouter des invités à la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="fcefe-146">Add guests to the global address list</span></span>

<span data-ttu-id="fcefe-147">Par défaut, les invités ne sont pas visibles dans la liste d’adresses globale d’Exchange.</span><span class="sxs-lookup"><span data-stu-id="fcefe-147">By default, guests aren't visible in the Exchange Global Address List.</span></span> <span data-ttu-id="fcefe-148">Utilisez les étapes répertoriées ci-dessous pour faire en sorte qu’un invité soit visible dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="fcefe-148">Use the steps listed below to make a guest visible in the global address list.</span></span>

<span data-ttu-id="fcefe-149">Recherchez l’ObjectID de l’utilisateur invité en exécutant :</span><span class="sxs-lookup"><span data-stu-id="fcefe-149">Find the guest user's ObjectID by running:</span></span>

```PowerShell
Get-AzureADUser -Filter "userType eq 'Guest'"
```

<span data-ttu-id="fcefe-150">Exécutez ensuite la commande suivante à l’aide des valeurs appropriées pour ObjectID, GivenName, Surname, DisplayName et TelephoneNumber.</span><span class="sxs-lookup"><span data-stu-id="fcefe-150">Then run the following using the appropriate values for ObjectID, GivenName, Surname, DisplayName, and TelephoneNumber.</span></span>

```PowerShell
Set-AzureADUser -ObjectId cfcbd1a0-ed18-4210-9b9d-cf0ba93cf6b2 -ShowInAddressList $true -GivenName 'Megan' -Surname 'Bowen' -DisplayName 'Megan Bowen' -TelephoneNumber '555-555-5555'
```

## <a name="related-articles"></a><span data-ttu-id="fcefe-151">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="fcefe-151">Related articles</span></span>

[<span data-ttu-id="fcefe-152">Gérer l’appartenance au groupe dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fcefe-152">Manage Group membership in the Microsoft 365 admin center</span></span>](add-or-remove-members-from-groups.md)
  
[<span data-ttu-id="fcefe-153">Avis d’accès à Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fcefe-153">Azure Active Directory access reviews</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-azure-ad-controls-perform-access-review)

[<span data-ttu-id="fcefe-154">Set-AzureADUser</span><span class="sxs-lookup"><span data-stu-id="fcefe-154">Set-AzureADUser</span></span>](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser)
