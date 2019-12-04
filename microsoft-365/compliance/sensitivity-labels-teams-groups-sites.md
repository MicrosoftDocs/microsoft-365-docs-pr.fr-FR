---
title: Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/03/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Vous pouvez appliquer des étiquettes à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.
ms.openlocfilehash: 72bdfef27ba20fabb0d59852e4e20425b2747425
ms.sourcegitcommit: 99d759d5c4e7d81266c3ebc087eaa37486cc0bc1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39818836"
---
# <a name="use-sensitivity-labels-with-microsoft-teams-office-365-groups-and-sharepoint-sites-public-preview"></a><span data-ttu-id="4720c-103">Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="4720c-103">Use sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites (public preview)</span></span>

<span data-ttu-id="4720c-104">Lorsque vous créez des étiquettes de confidentialité dans le [Centre de conformité microsoft 365](https://protection.office.com/), vous pouvez les appliquer à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4720c-104">When you create sensitivity labels in the [Microsoft 365 compliance center](https://protection.office.com/), you can now apply them to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="4720c-105">Vous pouvez associer des stratégies aux étiquettes pour contrôler :</span><span class="sxs-lookup"><span data-stu-id="4720c-105">You can associate policies with the labels to control:</span></span>

- <span data-ttu-id="4720c-106">Paramètres publics/privés</span><span class="sxs-lookup"><span data-stu-id="4720c-106">Public/private settings</span></span>
- <span data-ttu-id="4720c-107">Accès invité</span><span class="sxs-lookup"><span data-stu-id="4720c-107">Guest access</span></span>
- <span data-ttu-id="4720c-108">Accès à partir d’appareils non gérés</span><span class="sxs-lookup"><span data-stu-id="4720c-108">Access from unmanaged devices</span></span>

<span data-ttu-id="4720c-109">Lorsque vous appliquez une étiquette à une équipe ou un groupe, l’étiquette s’applique automatiquement au site d’équipe SharePoint connecté et inversement.</span><span class="sxs-lookup"><span data-stu-id="4720c-109">When you apply a label to a team or group, the label automatically applies to the connected SharePoint team site and the other way around.</span></span>

<span data-ttu-id="4720c-110">À présent, vous pouvez également activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="4720c-110">Now, You can also enable sensitivity labels for Office files in SharePoint and OneDrive.</span></span> <span data-ttu-id="4720c-111">[En savoir plus](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="4720c-111">[Learn more](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

## <a name="about-the-public-preview-for-microsoft-teams-office-365-groups-and-sharepoint-sites"></a><span data-ttu-id="4720c-112">À propos de la préversion publique pour Microsoft Teams, les groupes Office 365 et les sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-112">About the public preview for Microsoft Teams, Office 365 groups, and SharePoint sites</span></span>

<span data-ttu-id="4720c-113">Les étiquettes de sensibilité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint sont progressivement déployés sur les clients et peuvent changer avant la version finale.</span><span class="sxs-lookup"><span data-stu-id="4720c-113">Sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites is gradually rolling out to tenants and might change before final release.</span></span>

<span data-ttu-id="4720c-114">La préversion publique ne fonctionne pas avec les réseaux de distribution de contenu (CDN) Office 365.</span><span class="sxs-lookup"><span data-stu-id="4720c-114">The public preview doesn't work with Office 365 Content Delivery Networks (CDNs).</span></span>

## <a name="overview"></a><span data-ttu-id="4720c-115">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="4720c-115">Overview</span></span>

<span data-ttu-id="4720c-116">Lorsque vous publiez des étiquettes de confidentialité, les utilisateurs d’Office 365 ont accès à la même liste d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4720c-116">When you publish sensitivity labels, users across Office 365 have access to the same list of labels.</span></span>

<span data-ttu-id="4720c-117">Ces images présentent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4720c-117">These images show:</span></span>

- <span data-ttu-id="4720c-118">Affichage de la liste lors de la création d’un site d’équipe à partir de SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-118">How the list appears when you create a new team site from SharePoint</span></span>

- <span data-ttu-id="4720c-119">Lorsque vous affichez la liste dans Word</span><span class="sxs-lookup"><span data-stu-id="4720c-119">When you view the list in Word</span></span>

![Étiquette de critère de diffusion lors de la création d’un site d’équipe à partir de SharePoint](media/sensitivity-label-new-team-site.png)

![Étiquette de confidentialité affichée dans l’application Word de bureau](media/sensitivity-label-word.png)

## <a name="enable-this-preview-by-using-azure-powershell"></a><span data-ttu-id="4720c-122">Activer cet aperçu à l’aide d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4720c-122">Enable this preview by using Azure PowerShell</span></span>

1. <span data-ttu-id="4720c-123">Connectez-vous à Azure en tant qu’administrateur général à l’aide d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4720c-123">Sign in to Azure as a global admin by using Azure PowerShell.</span></span> <span data-ttu-id="4720c-124">Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="4720c-124">For instructions, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

2. <span data-ttu-id="4720c-125">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4720c-125">Run the following command:</span></span>

```powershell
  Connect-AzureAD
  $setting=(Get-AzureADDirectorySetting | where -Property DisplayName -Value "Group.Unified" -EQ)
  if ($setting -eq $null)
  {
    $template = Get-AzureADDirectorySettingTemplate -Id 62375ab9-6b52-47ed-826b-58e47e0e304b
    $setting = $template.CreateDirectorySetting()
    $setting["EnableMIPLabels"] = "True"
    New-AzureADDirectorySetting -DirectorySetting $setting
  }
  else
  {
    $setting["EnableMIPLabels"] = "True"
    Set-AzureADDirectorySetting -Id $setting.Id -DirectorySetting $setting
  }
```

<span data-ttu-id="4720c-126">Office 365 n’utilise plus les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cet aperçu.</span><span class="sxs-lookup"><span data-stu-id="4720c-126">Office 365 no longer uses the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="4720c-127">Si vous avez utilisé la [Classification de site Azure ad](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($Setting ["ClassificationList"]), les groupes et les sites existants affichent toujours les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="4720c-127">If you used [Azure AD site classification](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($setting["ClassificationList"]), existing groups and sites still display the old classifications.</span></span> <span data-ttu-id="4720c-128">Pour afficher les nouvelles classifications, convertissez-les.</span><span class="sxs-lookup"><span data-stu-id="4720c-128">To display the new classifications, convert them.</span></span> <span data-ttu-id="4720c-129">Pour plus d’informations sur la façon de les convertir, voir [si vous avez utilisé une classification de site Azure ad classique](#if-you-used-classic-azure-ad-site-classification).</span><span class="sxs-lookup"><span data-stu-id="4720c-129">For information about how to convert them, see [If you used classic Azure AD site classification](#if-you-used-classic-azure-ad-site-classification).</span></span>

## <a name="set-site-and-group-settings-when-you-create-or-edit-sensitivity-labels"></a><span data-ttu-id="4720c-130">Définir les paramètres de site et de groupe lorsque vous créez (ou modifiez) des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="4720c-130">Set site and group settings when you create (or edit) sensitivity labels</span></span>

<span data-ttu-id="4720c-131">Une fois l’aperçu activé, procédez comme suit pour créer des étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="4720c-131">After you enable the preview, follow these steps to create sensitivity labels.</span></span> <span data-ttu-id="4720c-132">La synchronisation des modifications apportées à ces paramètres peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="4720c-132">Changes to these settings may take up to 24 hours sync.</span></span>

1. <span data-ttu-id="4720c-133">Dans le centre de conformité Microsoft 365, sélectionnez**Etiquettes**de **classification** > .</span><span class="sxs-lookup"><span data-stu-id="4720c-133">In the Microsoft 365 compliance center, select **Classification** > **Sensitivity labels**.</span></span>

2. <span data-ttu-id="4720c-134">Sélectionnez **créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="4720c-134">Select **Create a label**.</span></span>

3. <span data-ttu-id="4720c-135">Sélectionnez les options souhaitées, puis sous l’onglet **paramètres de site et de groupe** , choisissez :</span><span class="sxs-lookup"><span data-stu-id="4720c-135">Select the options you want, and then on the **Site and group settings** tab, choose:</span></span>

    - <span data-ttu-id="4720c-136">Confidentialité (publique/privée) : privé signifie que seuls les membres approuvés de votre organisation peuvent voir ce qui se trouve à l’intérieur du groupe.</span><span class="sxs-lookup"><span data-stu-id="4720c-136">Privacy (Public/Private): Private means only approved members in your organization can see what's inside the group.</span></span> <span data-ttu-id="4720c-137">Les autres utilisateurs de votre organisation ne peuvent pas voir ce qui se trouve dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="4720c-137">Anyone else in your organization can't see what's in the group.</span></span> [<span data-ttu-id="4720c-138">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="4720c-138">Learn more</span></span>](https://support.office.com/article/36236e39-26d3-420b-b0ac-8072d2d2bedc)
    - <span data-ttu-id="4720c-139">Accès invité : vous pouvez contrôler si des invités peuvent être ajoutés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="4720c-139">Guest access: You can control if guests can be added to a group.</span></span> [<span data-ttu-id="4720c-140">En savoir plus sur la gestion de l’accès invité dans les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="4720c-140">Learn about managing guest access in Office 365 Groups</span></span>](/office365/admin/create-groups/manage-guest-access-in-groups)
    - <span data-ttu-id="4720c-141">Périphériques non gérés : ce paramètre vous permet de bloquer ou de limiter l’accès au contenu SharePoint à partir d’appareils qui ne sont pas liés à une publicité hybride ou qui ne sont pas conformes dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4720c-141">Unmanaged devices: This setting lets you block or limit access to SharePoint content from devices that aren't hybrid AD joined or compliant in Intune.</span></span> <span data-ttu-id="4720c-142">Si vous sélectionnez appareils non gérés, vous devez accéder à Azure AD pour terminer la configuration de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4720c-142">If you select Unmanaged devices, you need to go to Azure AD to finish setting up the policy.</span></span> <span data-ttu-id="4720c-143">Pour plus d’informations, consultez la rubrique [contrôler l’accès à partir d’appareils non gérés](/sharepoint/control-access-from-unmanaged-devices).</span><span class="sxs-lookup"><span data-stu-id="4720c-143">For info, see [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices).</span></span>

![Onglet Paramètres de site et de groupe](media/edit-sensitivity-label-site-group.png)

> [!IMPORTANT]
> <span data-ttu-id="4720c-145">Seuls les paramètres de site et de groupe prennent effet lorsque vous appliquez une étiquette à une équipe, un groupe ou un site.</span><span class="sxs-lookup"><span data-stu-id="4720c-145">Only the site and group settings take effect when you apply a label to a team, group, or site.</span></span> <span data-ttu-id="4720c-146">D’autres paramètres, tels que le chiffrement et le marquage de contenu, ne sont pas appliqués à tout le contenu au sein de l’équipe, du groupe ou du site.</span><span class="sxs-lookup"><span data-stu-id="4720c-146">Other settings, such as encryption and content marking, aren't applied to all content within the team, group, or site.</span></span> <span data-ttu-id="4720c-147">De même, si vous créez une étiquette et que vous n’activez pas les paramètres de site et de groupe, l’étiquette reste disponible lorsque les utilisateurs créent des équipes, des groupes et des sites, mais il ne peut rien faire lorsque les utilisateurs l’appliquent.</span><span class="sxs-lookup"><span data-stu-id="4720c-147">Similarly, if you create a label and don't turn on site and group settings, the label will still be available when users create teams, groups, and sites, but it won't do anything when users apply it.</span></span>

[<span data-ttu-id="4720c-148">En savoir plus sur la publication d’une étiquette de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4720c-148">Learn how to publish a sensitivity label</span></span>](/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do)

## <a name="apply-a-sensitivity-label-to-a-new-team"></a><span data-ttu-id="4720c-149">Appliquer une étiquette de critère de diffusion à une nouvelle équipe</span><span class="sxs-lookup"><span data-stu-id="4720c-149">Apply a sensitivity label to a new team</span></span>

<span data-ttu-id="4720c-150">Les utilisateurs peuvent sélectionner des étiquettes de confidentialité lorsqu’ils créent de nouvelles équipes dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4720c-150">Users can select sensitivity labels when they create new teams in Microsoft Teams.</span></span> <span data-ttu-id="4720c-151">Lorsqu’ils sélectionnent le niveau de confidentialité, le paramètre de confidentialité change si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4720c-151">When they select the sensitivity level, the privacy setting changes as necessary.</span></span> <span data-ttu-id="4720c-152">Selon le paramètre d’accès invité que vous avez sélectionné pour l’étiquette, les utilisateurs peuvent ou ne peuvent pas ajouter des personnes en dehors de l’organisation à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="4720c-152">Depending on the guest access setting you selected for the label, users can or can't add people outside the organization to the team.</span></span>

![Paramètre de confidentialité lors de la création d’une équipe](media/privacy-setting-new-team.png)

<span data-ttu-id="4720c-154">Une fois l’équipe créée, l’étiquette de sensibilité apparaît dans le coin supérieur droit de tous les canaux.</span><span class="sxs-lookup"><span data-stu-id="4720c-154">After you create the team, the sensitivity label appears in the upper-right corner of all channels.</span></span>

![L’étiquette de sensibilité apparaît dans l’équipe.](media/privacy-setting-teams.png)

<span data-ttu-id="4720c-156">Le service applique automatiquement la même étiquette de confidentialité au groupe Office 365 et au site d’équipe SharePoint connecté.</span><span class="sxs-lookup"><span data-stu-id="4720c-156">The service automatically applies the same sensitivity label to the Office 365 group and the connected SharePoint team site.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-group"></a><span data-ttu-id="4720c-157">Application d’une étiquette de critère de diffusion à un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="4720c-157">Apply a sensitivity label to a new group</span></span>

<span data-ttu-id="4720c-158">Dans Outlook sur le Web, la zone nouvelle **sensibilité** contient des étiquettes publiées.</span><span class="sxs-lookup"><span data-stu-id="4720c-158">In Outlook on the web, the new **Sensitivity** box contains published labels.</span></span> <span data-ttu-id="4720c-159">Si les utilisateurs souhaitent obtenir plus d’informations, ils peuvent cliquer sur l’icône d’aide pour lire les détails sur les étiquettes disponibles et les stratégies associées.</span><span class="sxs-lookup"><span data-stu-id="4720c-159">If users want more info, they can click the help icon to read details about the available labels and associated policies.</span></span>

![Création d’un groupe et sélection d’une option sous sensibilité](media/sensitivity-label-new-group.png)

## <a name="apply-a-sensitivity-label-to-a-new-site"></a><span data-ttu-id="4720c-161">Appliquer une étiquette de critère de diffusion à un nouveau site</span><span class="sxs-lookup"><span data-stu-id="4720c-161">Apply a sensitivity label to a new site</span></span>

<span data-ttu-id="4720c-162">Les administrateurs et les utilisateurs finaux peuvent sélectionner des étiquettes de confidentialité lors de la création de sites d’équipe et de sites de communication modernes.</span><span class="sxs-lookup"><span data-stu-id="4720c-162">Admins and end users can select sensitivity labels when they create modern team sites and communication sites.</span></span>

[<span data-ttu-id="4720c-163">Découvrez comment créer un site dans le nouveau centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-163">Learn how to create a site in the new SharePoint admin center</span></span>](/sharepoint/create-site-collection)

<span data-ttu-id="4720c-164">Lorsque les utilisateurs créent des sites d’équipe et de communication modernes, une étiquette de sensibilité est déjà sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="4720c-164">When users create modern team and communication sites, a sensitivity label is already selected by default.</span></span> <span data-ttu-id="4720c-165">Les utilisateurs peuvent sélectionner l’icône aide pour en savoir plus sur les étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4720c-165">Users can select the help icon to learn more about the labels.</span></span>

![Création d’un site et sélection d’une option sous sensibilité](media/sensitivity-label-new-communication-site.png)

<span data-ttu-id="4720c-167">Lorsque les utilisateurs accèdent au site, ils peuvent voir le nom de l’étiquette et des stratégies appliquées.</span><span class="sxs-lookup"><span data-stu-id="4720c-167">When users browse to the site, they can see the name of the label and applied policies.</span></span>

![Un site auquel une étiquette de sensibilité est appliquée](media/sensitivity-label-site.png)

## <a name="manage-sensitivity-labels-in-the-sharepoint-admin-center"></a><span data-ttu-id="4720c-169">Gérer les étiquettes de confidentialité dans le centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-169">Manage sensitivity labels in the SharePoint admin center</span></span>

<span data-ttu-id="4720c-170">Pour afficher et modifier les étiquettes, utilisez la page sites actifs dans le nouveau centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4720c-170">To view and edit the labels, use the Active sites page in the new SharePoint admin center.</span></span>

![Colonne critère de diffusion de la page sites actifs](media/manage-site-sensitivity-labels.png)

<span data-ttu-id="4720c-172">[En savoir plus sur la gestion des sites dans le nouveau centre d’administration SharePoint](/sharepoint/manage-sites-in-new-admin-center).</span><span class="sxs-lookup"><span data-stu-id="4720c-172">[Learn more about managing sites in the new SharePoint admin center](/sharepoint/manage-sites-in-new-admin-center).</span></span>

## <a name="change-site-and-group-settings-for-a-label"></a><span data-ttu-id="4720c-173">Modifier les paramètres de site et de groupe d’une étiquette</span><span class="sxs-lookup"><span data-stu-id="4720c-173">Change site and group settings for a label</span></span>

<span data-ttu-id="4720c-174">Il est recommandé de ne pas modifier les paramètres après avoir appliqué une étiquette à plusieurs équipes, groupes ou sites.</span><span class="sxs-lookup"><span data-stu-id="4720c-174">As a best practice, don't change settings after you've applied a label to several teams, groups, or sites.</span></span> <span data-ttu-id="4720c-175">Si vous devez effectuer une modification, vous devez utiliser un script Azure AD PowerShell pour appliquer les mises à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="4720c-175">If you must make a change, you'll need to use an Azure AD PowerShell script to manually apply updates.</span></span> <span data-ttu-id="4720c-176">Cette méthode garantit que toutes les équipes, les sites et les groupes existants appliquent le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="4720c-176">This method ensures all existing teams, sites, and groups enforce the new setting.</span></span>

## <a name="support-for-the-new-sensitivity-labels"></a><span data-ttu-id="4720c-177">Prise en charge des nouvelles étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4720c-177">Support for the new sensitivity labels</span></span>

<span data-ttu-id="4720c-178">Les applications et services suivants prennent en charge les étiquettes de sensibilité dans cet aperçu :</span><span class="sxs-lookup"><span data-stu-id="4720c-178">The following apps and services support the sensitivity labels in this preview:</span></span>

- <span data-ttu-id="4720c-179">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4720c-179">Microsoft 365 compliance center</span></span>
- <span data-ttu-id="4720c-180">SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-180">SharePoint</span></span>
- <span data-ttu-id="4720c-181">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="4720c-181">Outlook on the web</span></span>
- <span data-ttu-id="4720c-182">Teams</span><span class="sxs-lookup"><span data-stu-id="4720c-182">Teams</span></span>
- <span data-ttu-id="4720c-183">Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4720c-183">SharePoint admin center</span></span>
- <span data-ttu-id="4720c-184">Centre d’administration Azure AD</span><span class="sxs-lookup"><span data-stu-id="4720c-184">Azure AD admin center</span></span>

<span data-ttu-id="4720c-185">Vous ne pouvez pas utiliser les applications et services suivants pour créer des groupes Office 365 avec les nouvelles étiquettes de sensibilité :</span><span class="sxs-lookup"><span data-stu-id="4720c-185">You can't use the following apps and services to create Office 365 groups with the new sensitivity labels:</span></span>

- <span data-ttu-id="4720c-186">Outlook pour Mac</span><span class="sxs-lookup"><span data-stu-id="4720c-186">Outlook for the Mac</span></span>
- <span data-ttu-id="4720c-187">Outlook Mobile</span><span class="sxs-lookup"><span data-stu-id="4720c-187">Outlook mobile</span></span>  
- <span data-ttu-id="4720c-188">Bureau Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="4720c-188">Outlook desktop for Windows</span></span>
- <span data-ttu-id="4720c-189">Formulaires</span><span class="sxs-lookup"><span data-stu-id="4720c-189">Forms</span></span>  
- <span data-ttu-id="4720c-190">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4720c-190">Dynamics 365</span></span>  
- <span data-ttu-id="4720c-191">Yammer</span><span class="sxs-lookup"><span data-stu-id="4720c-191">Yammer</span></span>  
- <span data-ttu-id="4720c-192">Stream</span><span class="sxs-lookup"><span data-stu-id="4720c-192">Stream</span></span>  
- <span data-ttu-id="4720c-193">Planificateur</span><span class="sxs-lookup"><span data-stu-id="4720c-193">Planner</span></span>  
- <span data-ttu-id="4720c-194">Project</span><span class="sxs-lookup"><span data-stu-id="4720c-194">Project</span></span>  
- <span data-ttu-id="4720c-195">PowerBI</span><span class="sxs-lookup"><span data-stu-id="4720c-195">PowerBI</span></span>  
- <span data-ttu-id="4720c-196">Centre d’administration teams</span><span class="sxs-lookup"><span data-stu-id="4720c-196">Teams admin center</span></span>  
- <span data-ttu-id="4720c-197">Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4720c-197">Microsoft 365 admin center</span></span>  
- <span data-ttu-id="4720c-198">Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="4720c-198">Exchange admin center</span></span>

## <a name="if-you-used-classic-azure-ad-site-classification"></a><span data-ttu-id="4720c-199">Si vous avez utilisé une classification de site Azure AD classique</span><span class="sxs-lookup"><span data-stu-id="4720c-199">If you used classic Azure AD site classification</span></span>

<span data-ttu-id="4720c-200">Office 365 ne prend plus en charge les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cet aperçu.</span><span class="sxs-lookup"><span data-stu-id="4720c-200">Office 365 no longer supports the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="4720c-201">Toutefois, les groupes et les sites existants affichent toujours les anciennes classifications, sauf si vous les convertissez.</span><span class="sxs-lookup"><span data-stu-id="4720c-201">However, existing groups and sites still display the old classifications unless you convert them.</span></span> <span data-ttu-id="4720c-202">Les anciennes classifications incluent la classification de sites « modernes » que vous avez configurée, éventuellement via Azure AD PowerShell ou la bibliothèque principale PnP, qui `ClassificationList` a défini des valeurs pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="4720c-202">Old classifications include the "modern" sites classification you set up, possibly through Azure AD PowerShell or the PnP Core library, that defined values for the `ClassificationList` setting.</span></span>

<span data-ttu-id="4720c-203">Par exemple, dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="4720c-203">For example, in PowerShell:</span></span>

```powershell
   ($setting["ClassificationList"])
```

<span data-ttu-id="4720c-204">Pour plus d’informations sur l’ancienne méthode de classification, voir la rubrique sur la [classification des sites SharePoint « moderne »](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span><span class="sxs-lookup"><span data-stu-id="4720c-204">For more information about the old classification method, see [SharePoint "modern" sites classification](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span></span>

<span data-ttu-id="4720c-205">En fonction de votre déploiement actuel, vous disposez de deux options pour convertir vos anciennes classifications en nouvelles classifications.</span><span class="sxs-lookup"><span data-stu-id="4720c-205">Based on your current deployment, you have two options to convert your old classifications to the new classifications.</span></span>

### <a name="if-you-never-used-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="4720c-206">Si vous n’avez jamais utilisé les étiquettes de critère de diffusion (étiquettes de protection des informations Microsoft) pour les fichiers et le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4720c-206">If you never used sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="4720c-207">Nous vous recommandons d'effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4720c-207">We recommend that you:</span></span>

1. <span data-ttu-id="4720c-208">Créez des étiquettes de sensibilité dans le centre de conformité Microsoft 365 portant le même nom que vos classifications existantes.</span><span class="sxs-lookup"><span data-stu-id="4720c-208">Create new sensitivity labels in the Microsoft 365 compliance center that have the same names as your existing classifications.</span></span>
2. <span data-ttu-id="4720c-209">Utilisez PowerShell pour appliquer les nouvelles étiquettes aux groupes Office 365 existants et aux sites SharePoint à l’aide du mappage de nom.</span><span class="sxs-lookup"><span data-stu-id="4720c-209">Use PowerShell to apply the new labels to existing Office 365 groups and SharePoint sites using name mapping.</span></span>
3. <span data-ttu-id="4720c-210">Supprimez les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="4720c-210">Delete the old classifications.</span></span>

<span data-ttu-id="4720c-211">Les applications et les services qui prennent en charge les nouvelles étiquettes de sensibilité les affichent.</span><span class="sxs-lookup"><span data-stu-id="4720c-211">Apps and services that support the new sensitivity labels will show them.</span></span> <span data-ttu-id="4720c-212">Vous créez des équipes, des groupes et des sites avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4720c-212">You create new teams, groups, and sites with the new labels.</span></span> <span data-ttu-id="4720c-213">Les utilisateurs peuvent toujours créer des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4720c-213">Users can still create groups from apps and services that don't support the new labels.</span></span> <span data-ttu-id="4720c-214">Toutefois, les utilisateurs ne peuvent pas appliquer une étiquette à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4720c-214">However, users can't apply a label to these groups.</span></span> <span data-ttu-id="4720c-215">Utilisez PowerShell pour appliquer les nouvelles étiquettes de sensibilité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4720c-215">Use PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="4720c-216">Vous pouvez conserver vos anciennes classifications ; Toutefois, nous vous recommandons vivement d’utiliser PowerShell pour appliquer les nouvelles étiquettes de sensibilité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4720c-216">You can keep your old classifications; however, we highly recommend using PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="4720c-217">Les applications et les services qui prennent en charge les nouvelles étiquettes de sensibilité seront créés avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4720c-217">Apps and services that support the new sensitivity labels will get created with the new labels.</span></span> <span data-ttu-id="4720c-218">Lorsque les utilisateurs créent des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes, ils peuvent sélectionner une classification.</span><span class="sxs-lookup"><span data-stu-id="4720c-218">When users create groups from apps and services that don't support the new labels, they can select a classification.</span></span>

### <a name="if-you-use-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="4720c-219">Si vous utilisez des étiquettes de confidentialité (étiquettes de protection des informations Microsoft unifiées) pour les fichiers et le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4720c-219">If you use sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="4720c-220">Dès que vous activez cet aperçu, accédez à chaque étiquette dans le centre de conformité Microsoft 365 et appliquez les stratégies de votre choix pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="4720c-220">As soon as you enable this preview, go to each label in the Microsoft 365 compliance center and apply the policies you want for sites and groups.</span></span> <span data-ttu-id="4720c-221">Les utilisateurs commencent à voir les étiquettes existantes disponibles pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="4720c-221">Users will start seeing your existing labels available for sites and groups.</span></span>

### <a name="prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups"></a><span data-ttu-id="4720c-222">Préparer SharePoint Online Management Shell avant de réattribuer un nouveau libellé aux groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="4720c-222">Prepare the SharePoint Online Management Shell before you relabel Office 365 groups</span></span>

<span data-ttu-id="4720c-223">Avant d’appliquer de nouvelles étiquettes, vérifiez que vous utilisez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4720c-223">Before you apply new labels, ensure that you're running the latest SharePoint Online Management Shell.</span></span> <span data-ttu-id="4720c-224">Si vous disposez déjà de la dernière version, vous pouvez continuer et [attribuer un nouveau libellé aux groupes Office 365 avec de nouvelles étiquettes de confidentialité](#relabel-office-365-groups-with-new-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="4720c-224">If you already have the latest version, you can go ahead and [Relabel Office 365 groups with new sensitivity labels](#relabel-office-365-groups-with-new-sensitivity-labels).</span></span>

<span data-ttu-id="4720c-225">Pour préparer SharePoint Online Management Shell pour l’aperçu :</span><span class="sxs-lookup"><span data-stu-id="4720c-225">To prepare the SharePoint Online Management Shell for the preview:</span></span>

1. <span data-ttu-id="4720c-226">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à **Ajouter ou supprimer des programmes** et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="4720c-226">If you installed a previous version of the SharePoint Online Management Shell, go to **Add or remove programs** and uninstall “SharePoint Online Management Shell”.</span></span>

2. <span data-ttu-id="4720c-227">Dans un navigateur Web, accédez à la page du centre de téléchargement et [Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="4720c-227">In a web browser, go to the Download Center page and [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

3. <span data-ttu-id="4720c-228">Sélectionnez votre langue, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="4720c-228">Select your language and then click **Download**.</span></span>

4. <span data-ttu-id="4720c-229">Choisissez entre le fichier x64 et x86. msi.</span><span class="sxs-lookup"><span data-stu-id="4720c-229">Choose between the x64 and x86 .msi file.</span></span> <span data-ttu-id="4720c-230">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4720c-230">Download the x64 file if you run the 64-bit version of Windows or the x86 file if you’re run the 32-bit version.</span></span> <span data-ttu-id="4720c-231">Si vous ne le Sachez pas, consultez [la version du système d’exploitation Windows que je suis en cours d’exécution ?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="4720c-231">If you don’t know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span>

5. <span data-ttu-id="4720c-232">Après avoir téléchargé le fichier, exécutez le fichier et suivez les étapes de l’Assistant d’installation.</span><span class="sxs-lookup"><span data-stu-id="4720c-232">After you download the file, run the file and follow the steps in the Setup Wizard.</span></span>

### <a name="relabel-office-365-groups-with-new-sensitivity-labels"></a><span data-ttu-id="4720c-233">Attribution d’un nouveau libellé aux groupes Office 365 avec de nouvelles étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4720c-233">Relabel Office 365 groups with new sensitivity labels</span></span>

1. <span data-ttu-id="4720c-234">Assurez-vous que vous utilisez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4720c-234">Ensure that you're using the latest version of the SharePoint Online Management Shell.</span></span> <span data-ttu-id="4720c-235">Pour obtenir des instructions, consultez [la rubrique prepare the SharePoint Online Management Shell avant de réattribuer un nouveau libellé aux groupes Office 365](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span><span class="sxs-lookup"><span data-stu-id="4720c-235">For instructions, see [Prepare the SharePoint Online Management Shell before you relabel Office 365 groups](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span></span>

2. <span data-ttu-id="4720c-236">À l’aide d’un compte professionnel ou scolaire disposant des privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4720c-236">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint Online Management Shell.</span></span> <span data-ttu-id="4720c-237">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="4720c-237">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

3. <span data-ttu-id="4720c-238">Exécutez la commande suivante pour obtenir la liste des étiquettes de sensibilité et leurs GUID.</span><span class="sxs-lookup"><span data-stu-id="4720c-238">Run the following command to get the list of sensitivity labels and their GUIDs.</span></span>

    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid  
    ```

4. <span data-ttu-id="4720c-239">Notez le GUID de l’étiquette que vous souhaitez remplacer.</span><span class="sxs-lookup"><span data-stu-id="4720c-239">Make a note of the GUID for the label you want to overwrite.</span></span> <span data-ttu-id="4720c-240">Par exemple, l’étiquette « général ».</span><span class="sxs-lookup"><span data-stu-id="4720c-240">For example, the "General" label.</span></span>

5. <span data-ttu-id="4720c-241">Utilisez la commande suivante pour obtenir la liste des groupes qui ont la classification « General ».</span><span class="sxs-lookup"><span data-stu-id="4720c-241">Use the following command to get the list of groups that have the “General” classification.</span></span> <span data-ttu-id="4720c-242">Lorsque vous exécutez cette commande, vous vous connectez à Exchange Online PowerShell et exécutez la cmdlet Get-UnifiedGroup.</span><span class="sxs-lookup"><span data-stu-id="4720c-242">When you run this command, you'll connect to Exchange Online PowerShell and run the Get-UnifiedGroup cmdlet.</span></span>

   ```PowerShell
   Set-ExecutionPolicy RemoteSigned
   $UserCredential = Get-Credential
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   Import-PSSession $Session
   ```

6. <span data-ttu-id="4720c-243">Pour chaque groupe, ajoutez le GUID de l’étiquette de la nouvelle sensibilité.</span><span class="sxs-lookup"><span data-stu-id="4720c-243">For each group, add the new sensitivity label GUID.</span></span>

    ```PowerShell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "457fa763-7c59-461c-b402-ad1ac6b703cc"}
    ```
