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
ms.openlocfilehash: ebe5e00c3458782e1874274cb508326968461ce3
ms.sourcegitcommit: 1bd81cf48c7fab1b8aaf7c3f550ce42ab02136dc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39822490"
---
# <a name="use-sensitivity-labels-with-microsoft-teams-office-365-groups-and-sharepoint-sites-public-preview"></a><span data-ttu-id="4aa85-103">Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="4aa85-103">Use sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites (public preview)</span></span>

<span data-ttu-id="4aa85-104">Lorsque vous créez des étiquettes de confidentialité dans le [Centre de conformité microsoft 365](https://protection.office.com/), vous pouvez les appliquer à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4aa85-104">When you create sensitivity labels in the [Microsoft 365 compliance center](https://protection.office.com/), you can now apply them to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="4aa85-105">Vous pouvez associer des stratégies aux étiquettes pour contrôler :</span><span class="sxs-lookup"><span data-stu-id="4aa85-105">You can associate policies with the labels to control:</span></span>

- <span data-ttu-id="4aa85-106">Paramètres publics/privés</span><span class="sxs-lookup"><span data-stu-id="4aa85-106">Public/private settings</span></span>
- <span data-ttu-id="4aa85-107">Accès invité</span><span class="sxs-lookup"><span data-stu-id="4aa85-107">Guest access</span></span>
- <span data-ttu-id="4aa85-108">Accès à partir d’appareils non gérés</span><span class="sxs-lookup"><span data-stu-id="4aa85-108">Access from unmanaged devices</span></span>

<span data-ttu-id="4aa85-109">Lorsque vous appliquez une étiquette à une équipe ou un groupe, l’étiquette s’applique automatiquement au site d’équipe SharePoint connecté et inversement.</span><span class="sxs-lookup"><span data-stu-id="4aa85-109">When you apply a label to a team or group, the label automatically applies to the connected SharePoint team site and the other way around.</span></span>

<span data-ttu-id="4aa85-110">À présent, vous pouvez également activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="4aa85-110">Now, You can also enable sensitivity labels for Office files in SharePoint and OneDrive.</span></span> <span data-ttu-id="4aa85-111">[En savoir plus](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="4aa85-111">[Learn more](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

## <a name="about-the-public-preview-for-microsoft-teams-office-365-groups-and-sharepoint-sites"></a><span data-ttu-id="4aa85-112">À propos de la préversion publique pour Microsoft Teams, les groupes Office 365 et les sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-112">About the public preview for Microsoft Teams, Office 365 groups, and SharePoint sites</span></span>

<span data-ttu-id="4aa85-113">Les étiquettes de sensibilité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint sont progressivement déployés sur les clients et peuvent changer avant la version finale.</span><span class="sxs-lookup"><span data-stu-id="4aa85-113">Sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites is gradually rolling out to tenants and might change before final release.</span></span>

<span data-ttu-id="4aa85-114">La préversion publique ne fonctionne pas avec les réseaux de distribution de contenu (CDN) Office 365.</span><span class="sxs-lookup"><span data-stu-id="4aa85-114">The public preview doesn't work with Office 365 Content Delivery Networks (CDNs).</span></span>

## <a name="overview"></a><span data-ttu-id="4aa85-115">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="4aa85-115">Overview</span></span>

<span data-ttu-id="4aa85-116">Lorsque vous publiez des étiquettes de confidentialité, les utilisateurs d’Office 365 ont accès à la même liste d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-116">When you publish sensitivity labels, users across Office 365 have access to the same list of labels.</span></span>

<span data-ttu-id="4aa85-117">Ces images présentent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4aa85-117">These images show:</span></span>

- <span data-ttu-id="4aa85-118">Affichage de la liste lors de la création d’un site d’équipe à partir de SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-118">How the list appears when you create a new team site from SharePoint</span></span>

- <span data-ttu-id="4aa85-119">Lorsque vous affichez la liste dans Word</span><span class="sxs-lookup"><span data-stu-id="4aa85-119">When you view the list in Word</span></span>

![Étiquette de critère de diffusion lors de la création d’un site d’équipe à partir de SharePoint](media/sensitivity-label-new-team-site.png)

![Étiquette de confidentialité affichée dans l’application Word de bureau](media/sensitivity-label-word.png)

## <a name="enable-this-preview-by-using-azure-powershell"></a><span data-ttu-id="4aa85-122">Activer cet aperçu à l’aide d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4aa85-122">Enable this preview by using Azure PowerShell</span></span>

1. <span data-ttu-id="4aa85-123">Connectez-vous à Azure en tant qu’administrateur général à l’aide d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4aa85-123">Sign in to Azure as a global admin by using Azure PowerShell.</span></span> <span data-ttu-id="4aa85-124">Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="4aa85-124">For instructions, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

2. <span data-ttu-id="4aa85-125">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4aa85-125">Run the following command:</span></span>

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

<span data-ttu-id="4aa85-126">Office 365 n’utilise plus les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cet aperçu.</span><span class="sxs-lookup"><span data-stu-id="4aa85-126">Office 365 no longer uses the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="4aa85-127">Si vous avez utilisé la [Classification de site Azure ad](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($Setting ["ClassificationList"]), les groupes et les sites existants affichent toujours les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="4aa85-127">If you used [Azure AD site classification](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($setting["ClassificationList"]), existing groups and sites still display the old classifications.</span></span> <span data-ttu-id="4aa85-128">Pour afficher les nouvelles classifications, convertissez-les.</span><span class="sxs-lookup"><span data-stu-id="4aa85-128">To display the new classifications, convert them.</span></span> <span data-ttu-id="4aa85-129">Pour plus d’informations sur la façon de les convertir, voir [si vous avez utilisé une classification de site Azure ad classique](#if-you-used-classic-azure-ad-site-classification).</span><span class="sxs-lookup"><span data-stu-id="4aa85-129">For information about how to convert them, see [If you used classic Azure AD site classification](#if-you-used-classic-azure-ad-site-classification).</span></span> 

## <a name="set-site-and-group-settings-when-you-create-or-edit-sensitivity-labels"></a><span data-ttu-id="4aa85-130">Définir les paramètres de site et de groupe lors de la création ou de la modification des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="4aa85-130">Set site and group settings when you create or edit sensitivity labels</span></span>

<span data-ttu-id="4aa85-131">Une fois l’aperçu activé, procédez comme suit pour créer ou modifier des étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="4aa85-131">After you enable the preview, follow these steps to create or edit sensitivity labels.</span></span> <span data-ttu-id="4aa85-132">Vous devez effectuer ces étapes pour que les nouvelles étiquettes de sensibilité fonctionnent avec les sites et les groupes, même si vous avez déjà défini des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-132">You must complete these steps for the new sensitivity labels to work with sites and groups, even if you already have labels defined.</span></span> <span data-ttu-id="4aa85-133">La synchronisation des modifications apportées à ces paramètres peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="4aa85-133">Changes to these settings may take up to 24 hours sync.</span></span>

1. <span data-ttu-id="4aa85-134">Dans le centre de conformité Microsoft 365, sélectionnez**Etiquettes**de **classification** > .</span><span class="sxs-lookup"><span data-stu-id="4aa85-134">In the Microsoft 365 compliance center, select **Classification** > **Sensitivity labels**.</span></span>

2. <span data-ttu-id="4aa85-135">Sélectionnez **créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="4aa85-135">Select **Create a label**.</span></span> <span data-ttu-id="4aa85-136">Si vous avez déjà une étiquette, passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="4aa85-136">If you already have a label, skip to the next step.</span></span>

3. <span data-ttu-id="4aa85-137">Sélectionnez les options souhaitées, puis sous l’onglet **paramètres de site et de groupe** , choisissez :</span><span class="sxs-lookup"><span data-stu-id="4aa85-137">Select the options you want, and then on the **Site and group settings** tab, choose:</span></span>

    - <span data-ttu-id="4aa85-138">Confidentialité (publique/privée) : privé signifie que seuls les membres approuvés de votre organisation peuvent voir ce qui se trouve à l’intérieur du groupe.</span><span class="sxs-lookup"><span data-stu-id="4aa85-138">Privacy (Public/Private): Private means only approved members in your organization can see what's inside the group.</span></span> <span data-ttu-id="4aa85-139">Les autres utilisateurs de votre organisation ne peuvent pas voir ce qui se trouve dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="4aa85-139">Anyone else in your organization can't see what's in the group.</span></span> [<span data-ttu-id="4aa85-140">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="4aa85-140">Learn more</span></span>](https://support.office.com/article/36236e39-26d3-420b-b0ac-8072d2d2bedc)
    - <span data-ttu-id="4aa85-141">Accès invité : vous pouvez contrôler si des invités peuvent être ajoutés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="4aa85-141">Guest access: You can control if guests can be added to a group.</span></span> [<span data-ttu-id="4aa85-142">En savoir plus sur la gestion de l’accès invité dans les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="4aa85-142">Learn about managing guest access in Office 365 Groups</span></span>](/office365/admin/create-groups/manage-guest-access-in-groups)
    - <span data-ttu-id="4aa85-143">Périphériques non gérés : ce paramètre vous permet de bloquer ou de limiter l’accès au contenu SharePoint à partir d’appareils qui ne sont pas liés à une publicité hybride ou qui ne sont pas conformes dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4aa85-143">Unmanaged devices: This setting lets you block or limit access to SharePoint content from devices that aren't hybrid AD joined or compliant in Intune.</span></span> <span data-ttu-id="4aa85-144">Si vous sélectionnez appareils non gérés, vous devez accéder à Azure AD pour terminer la configuration de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4aa85-144">If you select Unmanaged devices, you need to go to Azure AD to finish setting up the policy.</span></span> <span data-ttu-id="4aa85-145">Pour plus d’informations, consultez la rubrique [contrôler l’accès à partir d’appareils non gérés](/sharepoint/control-access-from-unmanaged-devices).</span><span class="sxs-lookup"><span data-stu-id="4aa85-145">For info, see [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices).</span></span>

![Onglet Paramètres de site et de groupe](media/edit-sensitivity-label-site-group.png)

> [!IMPORTANT]
> <span data-ttu-id="4aa85-147">Seuls les paramètres de site et de groupe prennent effet lorsque vous appliquez une étiquette à une équipe, un groupe ou un site.</span><span class="sxs-lookup"><span data-stu-id="4aa85-147">Only the site and group settings take effect when you apply a label to a team, group, or site.</span></span> <span data-ttu-id="4aa85-148">D’autres paramètres, tels que le chiffrement et le marquage de contenu, ne sont pas appliqués à tout le contenu au sein de l’équipe, du groupe ou du site.</span><span class="sxs-lookup"><span data-stu-id="4aa85-148">Other settings, such as encryption and content marking, aren't applied to all content within the team, group, or site.</span></span> <span data-ttu-id="4aa85-149">De même, si vous créez une étiquette et que vous n’activez pas les paramètres de site et de groupe, l’étiquette reste disponible lorsque les utilisateurs créent des équipes, des groupes et des sites, mais il ne peut rien faire lorsque les utilisateurs l’appliquent.</span><span class="sxs-lookup"><span data-stu-id="4aa85-149">Similarly, if you create a label and don't turn on site and group settings, the label will still be available when users create teams, groups, and sites, but it won't do anything when users apply it.</span></span>

[<span data-ttu-id="4aa85-150">En savoir plus sur la publication d’une étiquette de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4aa85-150">Learn how to publish a sensitivity label</span></span>](/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do)

## <a name="troubleshoot-sensitivity-label-deployment"></a><span data-ttu-id="4aa85-151">Résoudre les problèmes de déploiement des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="4aa85-151">Troubleshoot sensitivity label deployment</span></span>

<span data-ttu-id="4aa85-152">Si vous rencontrez des problèmes lorsque vous créez un groupe teams ou Office 365 après avoir activé ces paramètres ou modifié la description d’une étiquette de sensibilité, enregistrez l’étiquette, patientez quelques heures, puis réessayez de créer le groupe Team 365 ou Office.</span><span class="sxs-lookup"><span data-stu-id="4aa85-152">If you experience issues when you create a Teams or Office 365 group after you enable these settings or make a change to a sensitivity label's description, save the label, wait a few hours, and then try to create the Team or Office 365 group again.</span></span>

<span data-ttu-id="4aa85-153">Si vous ne parvenez toujours pas à voir la nouvelle étiquette de sensibilité à partir de SharePoint Online, contactez immédiatement le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4aa85-153">If you are still not able to see the new sensitivity label from SharePoint Online, then contact Microsoft Support immediately.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-team"></a><span data-ttu-id="4aa85-154">Appliquer une étiquette de critère de diffusion à une nouvelle équipe</span><span class="sxs-lookup"><span data-stu-id="4aa85-154">Apply a sensitivity label to a new team</span></span>

<span data-ttu-id="4aa85-155">Les utilisateurs peuvent sélectionner des étiquettes de confidentialité lorsqu’ils créent de nouvelles équipes dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4aa85-155">Users can select sensitivity labels when they create new teams in Microsoft Teams.</span></span> <span data-ttu-id="4aa85-156">Lorsqu’ils sélectionnent le niveau de confidentialité, le paramètre de confidentialité change si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4aa85-156">When they select the sensitivity level, the privacy setting changes as necessary.</span></span> <span data-ttu-id="4aa85-157">Selon le paramètre d’accès invité que vous avez sélectionné pour l’étiquette, les utilisateurs peuvent ou ne peuvent pas ajouter des personnes en dehors de l’organisation à l’équipe.</span><span class="sxs-lookup"><span data-stu-id="4aa85-157">Depending on the guest access setting you selected for the label, users can or can't add people outside the organization to the team.</span></span>

![Paramètre de confidentialité lors de la création d’une équipe](media/privacy-setting-new-team.png)

<span data-ttu-id="4aa85-159">Une fois l’équipe créée, l’étiquette de sensibilité apparaît dans le coin supérieur droit de tous les canaux.</span><span class="sxs-lookup"><span data-stu-id="4aa85-159">After you create the team, the sensitivity label appears in the upper-right corner of all channels.</span></span>

![L’étiquette de sensibilité apparaît dans l’équipe.](media/privacy-setting-teams.png)

<span data-ttu-id="4aa85-161">Le service applique automatiquement la même étiquette de confidentialité au groupe Office 365 et au site d’équipe SharePoint connecté.</span><span class="sxs-lookup"><span data-stu-id="4aa85-161">The service automatically applies the same sensitivity label to the Office 365 group and the connected SharePoint team site.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-group"></a><span data-ttu-id="4aa85-162">Application d’une étiquette de critère de diffusion à un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="4aa85-162">Apply a sensitivity label to a new group</span></span>

<span data-ttu-id="4aa85-163">Dans Outlook sur le Web, la zone nouvelle **sensibilité** contient des étiquettes publiées.</span><span class="sxs-lookup"><span data-stu-id="4aa85-163">In Outlook on the web, the new **Sensitivity** box contains published labels.</span></span> <span data-ttu-id="4aa85-164">Si les utilisateurs souhaitent obtenir plus d’informations, ils peuvent cliquer sur l’icône d’aide pour lire les détails sur les étiquettes disponibles et les stratégies associées.</span><span class="sxs-lookup"><span data-stu-id="4aa85-164">If users want more info, they can click the help icon to read details about the available labels and associated policies.</span></span>

![Création d’un groupe et sélection d’une option sous sensibilité](media/sensitivity-label-new-group.png)

## <a name="apply-a-sensitivity-label-to-a-new-site"></a><span data-ttu-id="4aa85-166">Appliquer une étiquette de critère de diffusion à un nouveau site</span><span class="sxs-lookup"><span data-stu-id="4aa85-166">Apply a sensitivity label to a new site</span></span>

<span data-ttu-id="4aa85-167">Les administrateurs et les utilisateurs finaux peuvent sélectionner des étiquettes de confidentialité lors de la création de sites d’équipe et de sites de communication modernes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-167">Admins and end users can select sensitivity labels when they create modern team sites and communication sites.</span></span>

[<span data-ttu-id="4aa85-168">Découvrez comment créer un site dans le nouveau centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-168">Learn how to create a site in the new SharePoint admin center</span></span>](/sharepoint/create-site-collection)

<span data-ttu-id="4aa85-169">Lorsque les utilisateurs créent des sites d’équipe et de communication modernes, une étiquette de sensibilité est déjà sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="4aa85-169">When users create modern team and communication sites, a sensitivity label is already selected by default.</span></span> <span data-ttu-id="4aa85-170">Les utilisateurs peuvent sélectionner l’icône aide pour en savoir plus sur les étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-170">Users can select the help icon to learn more about the labels.</span></span>

![Création d’un site et sélection d’une option sous sensibilité](media/sensitivity-label-new-communication-site.png)

<span data-ttu-id="4aa85-172">Lorsque les utilisateurs accèdent au site, ils peuvent voir le nom de l’étiquette et des stratégies appliquées.</span><span class="sxs-lookup"><span data-stu-id="4aa85-172">When users browse to the site, they can see the name of the label and applied policies.</span></span>

![Un site auquel une étiquette de sensibilité est appliquée](media/sensitivity-label-site.png)

## <a name="manage-sensitivity-labels-in-the-sharepoint-admin-center"></a><span data-ttu-id="4aa85-174">Gérer les étiquettes de confidentialité dans le centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-174">Manage sensitivity labels in the SharePoint admin center</span></span>

<span data-ttu-id="4aa85-175">Pour afficher et modifier les étiquettes, utilisez la page sites actifs dans le nouveau centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4aa85-175">To view and edit the labels, use the Active sites page in the new SharePoint admin center.</span></span>

![Colonne critère de diffusion de la page sites actifs](media/manage-site-sensitivity-labels.png)

<span data-ttu-id="4aa85-177">[En savoir plus sur la gestion des sites dans le nouveau centre d’administration SharePoint](/sharepoint/manage-sites-in-new-admin-center).</span><span class="sxs-lookup"><span data-stu-id="4aa85-177">[Learn more about managing sites in the new SharePoint admin center](/sharepoint/manage-sites-in-new-admin-center).</span></span>

## <a name="change-site-and-group-settings-for-a-label"></a><span data-ttu-id="4aa85-178">Modifier les paramètres de site et de groupe d’une étiquette</span><span class="sxs-lookup"><span data-stu-id="4aa85-178">Change site and group settings for a label</span></span>

<span data-ttu-id="4aa85-179">Il est recommandé de ne pas modifier les paramètres après avoir appliqué une étiquette à plusieurs équipes, groupes ou sites.</span><span class="sxs-lookup"><span data-stu-id="4aa85-179">As a best practice, don't change settings after you've applied a label to several teams, groups, or sites.</span></span> <span data-ttu-id="4aa85-180">Si vous devez effectuer une modification, vous devez utiliser un script Azure AD PowerShell pour appliquer les mises à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="4aa85-180">If you must make a change, you'll need to use an Azure AD PowerShell script to manually apply updates.</span></span> <span data-ttu-id="4aa85-181">Cette méthode garantit que toutes les équipes, les sites et les groupes existants appliquent le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="4aa85-181">This method ensures all existing teams, sites, and groups enforce the new setting.</span></span>

## <a name="support-for-the-new-sensitivity-labels"></a><span data-ttu-id="4aa85-182">Prise en charge des nouvelles étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4aa85-182">Support for the new sensitivity labels</span></span>

<span data-ttu-id="4aa85-183">Les applications et services suivants prennent en charge les étiquettes de sensibilité dans cet aperçu :</span><span class="sxs-lookup"><span data-stu-id="4aa85-183">The following apps and services support the sensitivity labels in this preview:</span></span>

- <span data-ttu-id="4aa85-184">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4aa85-184">Microsoft 365 compliance center</span></span>
- <span data-ttu-id="4aa85-185">SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-185">SharePoint</span></span>
- <span data-ttu-id="4aa85-186">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="4aa85-186">Outlook on the web</span></span>
- <span data-ttu-id="4aa85-187">Teams</span><span class="sxs-lookup"><span data-stu-id="4aa85-187">Teams</span></span>
- <span data-ttu-id="4aa85-188">Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="4aa85-188">SharePoint admin center</span></span>
- <span data-ttu-id="4aa85-189">Centre d’administration Azure AD</span><span class="sxs-lookup"><span data-stu-id="4aa85-189">Azure AD admin center</span></span>

<span data-ttu-id="4aa85-190">Vous ne pouvez pas utiliser les applications et services suivants pour créer des groupes Office 365 avec les nouvelles étiquettes de sensibilité :</span><span class="sxs-lookup"><span data-stu-id="4aa85-190">You can't use the following apps and services to create Office 365 groups with the new sensitivity labels:</span></span>

- <span data-ttu-id="4aa85-191">Outlook pour Mac</span><span class="sxs-lookup"><span data-stu-id="4aa85-191">Outlook for the Mac</span></span>
- <span data-ttu-id="4aa85-192">Outlook Mobile</span><span class="sxs-lookup"><span data-stu-id="4aa85-192">Outlook mobile</span></span>  
- <span data-ttu-id="4aa85-193">Bureau Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="4aa85-193">Outlook desktop for Windows</span></span>
- <span data-ttu-id="4aa85-194">Formulaires</span><span class="sxs-lookup"><span data-stu-id="4aa85-194">Forms</span></span>  
- <span data-ttu-id="4aa85-195">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4aa85-195">Dynamics 365</span></span>  
- <span data-ttu-id="4aa85-196">Yammer</span><span class="sxs-lookup"><span data-stu-id="4aa85-196">Yammer</span></span>  
- <span data-ttu-id="4aa85-197">Stream</span><span class="sxs-lookup"><span data-stu-id="4aa85-197">Stream</span></span>  
- <span data-ttu-id="4aa85-198">Planificateur</span><span class="sxs-lookup"><span data-stu-id="4aa85-198">Planner</span></span>  
- <span data-ttu-id="4aa85-199">Project</span><span class="sxs-lookup"><span data-stu-id="4aa85-199">Project</span></span>  
- <span data-ttu-id="4aa85-200">PowerBI</span><span class="sxs-lookup"><span data-stu-id="4aa85-200">PowerBI</span></span>  
- <span data-ttu-id="4aa85-201">Centre d’administration teams</span><span class="sxs-lookup"><span data-stu-id="4aa85-201">Teams admin center</span></span>  
- <span data-ttu-id="4aa85-202">Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4aa85-202">Microsoft 365 admin center</span></span>  
- <span data-ttu-id="4aa85-203">Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="4aa85-203">Exchange admin center</span></span>

## <a name="if-you-used-classic-azure-ad-site-classification"></a><span data-ttu-id="4aa85-204">Si vous avez utilisé une classification de site Azure AD classique</span><span class="sxs-lookup"><span data-stu-id="4aa85-204">If you used classic Azure AD site classification</span></span>

<span data-ttu-id="4aa85-205">Office 365 ne prend plus en charge les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cet aperçu.</span><span class="sxs-lookup"><span data-stu-id="4aa85-205">Office 365 no longer supports the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="4aa85-206">Toutefois, les groupes et les sites existants affichent toujours les anciennes classifications, sauf si vous les convertissez.</span><span class="sxs-lookup"><span data-stu-id="4aa85-206">However, existing groups and sites still display the old classifications unless you convert them.</span></span> <span data-ttu-id="4aa85-207">Les anciennes classifications incluent la classification de sites « modernes » que vous avez configurée, éventuellement via Azure AD PowerShell ou la bibliothèque principale PnP, qui `ClassificationList` a défini des valeurs pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="4aa85-207">Old classifications include the "modern" sites classification you set up, possibly through Azure AD PowerShell or the PnP Core library, that defined values for the `ClassificationList` setting.</span></span>

<span data-ttu-id="4aa85-208">Par exemple, dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="4aa85-208">For example, in PowerShell:</span></span>

```powershell
   ($setting["ClassificationList"])
```

<span data-ttu-id="4aa85-209">Pour plus d’informations sur l’ancienne méthode de classification, voir la rubrique sur la [classification des sites SharePoint « moderne »](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span><span class="sxs-lookup"><span data-stu-id="4aa85-209">For more information about the old classification method, see [SharePoint "modern" sites classification](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span></span>

<span data-ttu-id="4aa85-210">En fonction de votre déploiement actuel, vous disposez de deux options pour convertir vos anciennes classifications en nouvelles classifications.</span><span class="sxs-lookup"><span data-stu-id="4aa85-210">Based on your current deployment, you have two options to convert your old classifications to the new classifications.</span></span>

### <a name="if-you-never-used-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="4aa85-211">Si vous n’avez jamais utilisé les étiquettes de critère de diffusion (étiquettes de protection des informations Microsoft) pour les fichiers et le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4aa85-211">If you never used sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="4aa85-212">Nous vous recommandons d'effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4aa85-212">We recommend that you:</span></span>

1. <span data-ttu-id="4aa85-213">Créez des étiquettes de sensibilité dans le centre de conformité Microsoft 365 portant le même nom que vos classifications existantes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-213">Create new sensitivity labels in the Microsoft 365 compliance center that have the same names as your existing classifications.</span></span>
2. <span data-ttu-id="4aa85-214">Utilisez PowerShell pour appliquer les nouvelles étiquettes aux groupes Office 365 existants et aux sites SharePoint à l’aide du mappage de nom.</span><span class="sxs-lookup"><span data-stu-id="4aa85-214">Use PowerShell to apply the new labels to existing Office 365 groups and SharePoint sites using name mapping.</span></span>
3. <span data-ttu-id="4aa85-215">Supprimez les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="4aa85-215">Delete the old classifications.</span></span>

<span data-ttu-id="4aa85-216">Les applications et les services qui prennent en charge les nouvelles étiquettes de sensibilité les affichent.</span><span class="sxs-lookup"><span data-stu-id="4aa85-216">Apps and services that support the new sensitivity labels will show them.</span></span> <span data-ttu-id="4aa85-217">Vous créez des équipes, des groupes et des sites avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-217">You create new teams, groups, and sites with the new labels.</span></span> <span data-ttu-id="4aa85-218">Les utilisateurs peuvent toujours créer des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-218">Users can still create groups from apps and services that don't support the new labels.</span></span> <span data-ttu-id="4aa85-219">Toutefois, les utilisateurs ne peuvent pas appliquer une étiquette à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-219">However, users can't apply a label to these groups.</span></span> <span data-ttu-id="4aa85-220">Utilisez PowerShell pour appliquer les nouvelles étiquettes de sensibilité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-220">Use PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="4aa85-221">Vous pouvez conserver vos anciennes classifications ; Toutefois, nous vous recommandons vivement d’utiliser PowerShell pour appliquer les nouvelles étiquettes de sensibilité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-221">You can keep your old classifications; however, we highly recommend using PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="4aa85-222">Les applications et les services qui prennent en charge les nouvelles étiquettes de sensibilité seront créés avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-222">Apps and services that support the new sensitivity labels will get created with the new labels.</span></span> <span data-ttu-id="4aa85-223">Lorsque les utilisateurs créent des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes, ils peuvent sélectionner une classification.</span><span class="sxs-lookup"><span data-stu-id="4aa85-223">When users create groups from apps and services that don't support the new labels, they can select a classification.</span></span>

### <a name="if-you-use-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="4aa85-224">Si vous utilisez des étiquettes de confidentialité (étiquettes de protection des informations Microsoft unifiées) pour les fichiers et le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="4aa85-224">If you use sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="4aa85-225">Dès que vous activez cet aperçu, accédez à chaque étiquette dans le centre de conformité Microsoft 365 et appliquez les stratégies de votre choix pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-225">As soon as you enable this preview, go to each label in the Microsoft 365 compliance center and apply the policies you want for sites and groups.</span></span> <span data-ttu-id="4aa85-226">Les utilisateurs commencent à voir les étiquettes existantes disponibles pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="4aa85-226">Users will start seeing your existing labels available for sites and groups.</span></span>

### <a name="prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups"></a><span data-ttu-id="4aa85-227">Préparer SharePoint Online Management Shell avant de réattribuer un nouveau libellé aux groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="4aa85-227">Prepare the SharePoint Online Management Shell before you relabel Office 365 groups</span></span>

<span data-ttu-id="4aa85-228">Avant d’appliquer de nouvelles étiquettes, vérifiez que vous utilisez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4aa85-228">Before you apply new labels, ensure that you're running the latest SharePoint Online Management Shell.</span></span> <span data-ttu-id="4aa85-229">Si vous disposez déjà de la dernière version, vous pouvez continuer et [attribuer un nouveau libellé aux groupes Office 365 avec de nouvelles étiquettes de confidentialité](#relabel-office-365-groups-with-new-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="4aa85-229">If you already have the latest version, you can go ahead and [Relabel Office 365 groups with new sensitivity labels](#relabel-office-365-groups-with-new-sensitivity-labels).</span></span>

<span data-ttu-id="4aa85-230">Pour préparer SharePoint Online Management Shell pour l’aperçu :</span><span class="sxs-lookup"><span data-stu-id="4aa85-230">To prepare the SharePoint Online Management Shell for the preview:</span></span>

1. <span data-ttu-id="4aa85-231">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à **Ajouter ou supprimer des programmes** et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="4aa85-231">If you installed a previous version of the SharePoint Online Management Shell, go to **Add or remove programs** and uninstall “SharePoint Online Management Shell”.</span></span>

2. <span data-ttu-id="4aa85-232">Dans un navigateur Web, accédez à la page du centre de téléchargement et [Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="4aa85-232">In a web browser, go to the Download Center page and [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

3. <span data-ttu-id="4aa85-233">Sélectionnez votre langue, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="4aa85-233">Select your language and then click **Download**.</span></span>

4. <span data-ttu-id="4aa85-234">Choisissez entre le fichier x64 et x86. msi.</span><span class="sxs-lookup"><span data-stu-id="4aa85-234">Choose between the x64 and x86 .msi file.</span></span> <span data-ttu-id="4aa85-235">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4aa85-235">Download the x64 file if you run the 64-bit version of Windows or the x86 file if you’re run the 32-bit version.</span></span> <span data-ttu-id="4aa85-236">Si vous ne le Sachez pas, consultez [la version du système d’exploitation Windows que je suis en cours d’exécution ?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="4aa85-236">If you don’t know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span>

5. <span data-ttu-id="4aa85-237">Après avoir téléchargé le fichier, exécutez le fichier et suivez les étapes de l’Assistant d’installation.</span><span class="sxs-lookup"><span data-stu-id="4aa85-237">After you download the file, run the file and follow the steps in the Setup Wizard.</span></span>

### <a name="relabel-office-365-groups-with-new-sensitivity-labels"></a><span data-ttu-id="4aa85-238">Attribution d’un nouveau libellé aux groupes Office 365 avec de nouvelles étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="4aa85-238">Relabel Office 365 groups with new sensitivity labels</span></span>

1. <span data-ttu-id="4aa85-239">Assurez-vous que vous utilisez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4aa85-239">Ensure that you're using the latest version of the SharePoint Online Management Shell.</span></span> <span data-ttu-id="4aa85-240">Pour obtenir des instructions, consultez [la rubrique prepare the SharePoint Online Management Shell avant de réattribuer un nouveau libellé aux groupes Office 365](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span><span class="sxs-lookup"><span data-stu-id="4aa85-240">For instructions, see [Prepare the SharePoint Online Management Shell before you relabel Office 365 groups](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span></span>

2. <span data-ttu-id="4aa85-241">À l’aide d’un compte professionnel ou scolaire disposant des privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="4aa85-241">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint Online Management Shell.</span></span> <span data-ttu-id="4aa85-242">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="4aa85-242">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

3. <span data-ttu-id="4aa85-243">Exécutez la commande suivante pour obtenir la liste des étiquettes de sensibilité et leurs GUID.</span><span class="sxs-lookup"><span data-stu-id="4aa85-243">Run the following command to get the list of sensitivity labels and their GUIDs.</span></span>

    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid  
    ```

4. <span data-ttu-id="4aa85-244">Notez le GUID de l’étiquette que vous souhaitez remplacer.</span><span class="sxs-lookup"><span data-stu-id="4aa85-244">Make a note of the GUID for the label you want to overwrite.</span></span> <span data-ttu-id="4aa85-245">Par exemple, l’étiquette « général ».</span><span class="sxs-lookup"><span data-stu-id="4aa85-245">For example, the "General" label.</span></span>

5. <span data-ttu-id="4aa85-246">Utilisez la commande suivante pour obtenir la liste des groupes qui ont la classification « General ».</span><span class="sxs-lookup"><span data-stu-id="4aa85-246">Use the following command to get the list of groups that have the “General” classification.</span></span> <span data-ttu-id="4aa85-247">Lorsque vous exécutez cette commande, vous vous connectez à Exchange Online PowerShell et exécutez la cmdlet Get-UnifiedGroup.</span><span class="sxs-lookup"><span data-stu-id="4aa85-247">When you run this command, you'll connect to Exchange Online PowerShell and run the Get-UnifiedGroup cmdlet.</span></span>

   ```PowerShell
   Set-ExecutionPolicy RemoteSigned
   $UserCredential = Get-Credential
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   Import-PSSession $Session
   ```

6. <span data-ttu-id="4aa85-248">Pour chaque groupe, ajoutez le GUID de l’étiquette de la nouvelle sensibilité.</span><span class="sxs-lookup"><span data-stu-id="4aa85-248">For each group, add the new sensitivity label GUID.</span></span>

    ```PowerShell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "457fa763-7c59-461c-b402-ad1ac6b703cc"}
    ```
