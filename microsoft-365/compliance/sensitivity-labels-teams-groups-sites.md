---
title: Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)
f1.keywords:
- NOCSH
ms.author: krowley
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Vous pouvez appliquer des étiquettes à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.
ms.openlocfilehash: 7fd19d9d8f84bd6463d61aec68dbd86c4fc627c0
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601561"
---
# <a name="use-sensitivity-labels-with-microsoft-teams-office-365-groups-and-sharepoint-sites-public-preview"></a><span data-ttu-id="05e3b-103">Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="05e3b-103">Use sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites (public preview)</span></span>

<span data-ttu-id="05e3b-104">Lorsque vous créez des étiquettes de confidentialité dans le [Centre de conformité Microsoft 365](https://protection.office.com/), vous pouvez désormais les appliquer à Microsoft Teams, aux groupes Office 365 et aux sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="05e3b-104">When you create sensitivity labels in the [Microsoft 365 compliance center](https://protection.office.com/), you can now apply them to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="05e3b-105">Vous pouvez associer les stratégies aux étiquettes pour contrôler :</span><span class="sxs-lookup"><span data-stu-id="05e3b-105">You can associate policies with the labels to control:</span></span>

- <span data-ttu-id="05e3b-106">Paramètres publics/privés</span><span class="sxs-lookup"><span data-stu-id="05e3b-106">Public/private settings</span></span>
- <span data-ttu-id="05e3b-107">Accès invité</span><span class="sxs-lookup"><span data-stu-id="05e3b-107">Guest access</span></span>
- <span data-ttu-id="05e3b-108">Accès à partir d’appareils enregistrés</span><span class="sxs-lookup"><span data-stu-id="05e3b-108">Access from unmanaged devices</span></span>

<span data-ttu-id="05e3b-109">Lorsque vous appliquez une étiquette à une équipe ou à un groupe, celle-ci s’applique automatiquement au site d’équipe SharePoint connecté et inversement.</span><span class="sxs-lookup"><span data-stu-id="05e3b-109">When you apply a label to a team or group, the label automatically applies to the connected SharePoint team site and the other way around.</span></span>

<span data-ttu-id="05e3b-110">Vous pouvez désormais activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="05e3b-110">You can now also enable sensitivity labels for Office files in SharePoint and OneDrive.</span></span> <span data-ttu-id="05e3b-111">Pour en savoir plus, consulter [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive (préversion publique)](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="05e3b-111">For more information, see [Enable sensitivity labels for Office files in SharePoint and OneDrive (public preview)](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

## <a name="about-the-public-preview-for-microsoft-teams-office-365-groups-and-sharepoint-sites"></a><span data-ttu-id="05e3b-112">À propos de la préversion publique Microsoft Teams, les groupes Office 365 et les sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-112">About the public preview for Microsoft Teams, Office 365 groups, and SharePoint sites</span></span>

<span data-ttu-id="05e3b-113">Les étiquettes de confidentialité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint sont progressivement déployés pour les locataires, et peuvent changer avant la publication finale.</span><span class="sxs-lookup"><span data-stu-id="05e3b-113">Sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites are gradually rolling out to tenants and might change before final release.</span></span>

<span data-ttu-id="05e3b-114">Cette préversion publique ne fonctionne pas avec les réseaux de distribution de contenu Office 365 (CDN).</span><span class="sxs-lookup"><span data-stu-id="05e3b-114">This public preview doesn't work with Office 365 Content Delivery Networks (CDNs).</span></span>

## <a name="overview"></a><span data-ttu-id="05e3b-115">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="05e3b-115">Overview</span></span>

<span data-ttu-id="05e3b-116">Lorsque vous publiez des étiquettes de confidentialité, les utilisateurs dans Office 365 ont accès à la même liste d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-116">When you publish sensitivity labels, users across Office 365 have access to the same list of labels.</span></span>

<span data-ttu-id="05e3b-117">Ces images présentent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="05e3b-117">These images show:</span></span>

- <span data-ttu-id="05e3b-118">Affichage de la liste lorsque vous créez un site d’équipe à partir de SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-118">How the list appears when you create a new team site from SharePoint</span></span>

- <span data-ttu-id="05e3b-119">Lorsque vous affichez la liste dans Word</span><span class="sxs-lookup"><span data-stu-id="05e3b-119">When you view the list in Word</span></span>

<span data-ttu-id="05e3b-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="05e3b-120">For example:</span></span>

![Étiquette de confidentialité lors de la création d’un site d’équipe à partir de SharePoint](media/sensitivity-label-new-team-site.png)

![Étiquette de confidentialité affichée dans l’application de bureau Word](media/sensitivity-label-word.png)

## <a name="enable-this-preview"></a><span data-ttu-id="05e3b-123">Activer ce préversion</span><span class="sxs-lookup"><span data-stu-id="05e3b-123">Enable this preview</span></span>

<span data-ttu-id="05e3b-124">Vous devez utiliser la version d’évaluation d’[Azure Active Directory PowerShell pour Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-2.0) (nom de module **AzureADPreview**) pour activer cette préversion des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint :</span><span class="sxs-lookup"><span data-stu-id="05e3b-124">You must use the preview version of [Azure Active Directory PowerShell for Graph (AzureAD)](https://docs.microsoft.com/powershell/azure/active-directory/overview?view=azureadps-2.0) (module name **AzureADPreview**) to enable this preview of sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites:</span></span>

- <span data-ttu-id="05e3b-125">Si vous n’avez jamais installé une version du module Azure AD PowerShell, consultez [l’installation du module Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) et suivez les instructions d’installation de la préversion publique.</span><span class="sxs-lookup"><span data-stu-id="05e3b-125">If you haven't installed any version of the Azure AD PowerShell module before, see [Installing the Azure AD Module](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#installing-the-azure-ad-module) and follow the instructions to install the public preview release.</span></span>

- <span data-ttu-id="05e3b-126">Si la version générale 2.0 du module Azure AD PowerShell (AzureAD) est installée sur votre ordinateur, vous devez la désinstaller en exécutant `Uninstall-Module AzureAD` dans votre session PowerShell, puis installer la préversion en exécutant `Install-Module AzureADPreview`.</span><span class="sxs-lookup"><span data-stu-id="05e3b-126">If you have the 2.0 general availability version of the Azure AD PowerShell module (AzureAD) installed, you must uninstall it by running `Uninstall-Module AzureAD` in your PowerShell session, and then install the preview version by running `Install-Module AzureADPreview`.</span></span>

- <span data-ttu-id="05e3b-127">Si vous avez déjà installé lapréversion, exécutez `Install-Module AzureADPreview` pour vous assurer qu’il s’agit de la dernière version de ce module.</span><span class="sxs-lookup"><span data-stu-id="05e3b-127">If you have already installed the preview version, run `Install-Module AzureADPreview` to make sure it's the latest version of this module.</span></span>

<span data-ttu-id="05e3b-128">Vous êtes maintenant prêt à activer la préversion des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint :</span><span class="sxs-lookup"><span data-stu-id="05e3b-128">You're now ready to enable the preview of sensitivity labels with Microsoft Teams, Office 365 groups, and SharePoint sites:</span></span>

1. <span data-ttu-id="05e3b-129">Dans une session PowerShell, l’utilisation d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général se connecte à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="05e3b-129">In a PowerShell session, using a work or school account that has global admin privileges, connect to Azure Active Directory.</span></span> <span data-ttu-id="05e3b-130">Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="05e3b-130">For example, run:</span></span>
    
    ```powershell
    Connect-AzureAD
    ````
    
    <span data-ttu-id="05e3b-131">Pour obtenir des instructions complètes, consultez[Se connecter à Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#connect-to-azure-ad).</span><span class="sxs-lookup"><span data-stu-id="05e3b-131">For full instructions, see [Connect to Azure AD](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2?view=azureadps-2.0-preview#connect-to-azure-ad).</span></span>

2. <span data-ttu-id="05e3b-132">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="05e3b-132">Run the following commands:</span></span>
    
    ```powershell
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
    
    > [!NOTE]
    > <span data-ttu-id="05e3b-133">Office 365 n’utilise plus les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cette préversion.</span><span class="sxs-lookup"><span data-stu-id="05e3b-133">Office 365 no longer uses the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="05e3b-134">Si vous avez utilisé [Classification de sites Azure AD](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($setting ["ClassificationList"]), les groupes et sites existants affichent encore les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="05e3b-134">If you used [Azure AD site classification](/sharepoint/dev/solution-guidance/modern-experience-site-classification) ($setting["ClassificationList"]), existing groups and sites still display the old classifications.</span></span> <span data-ttu-id="05e3b-135">Pour afficher les nouvelles classifications, convertissez-les.</span><span class="sxs-lookup"><span data-stu-id="05e3b-135">To display the new classifications, convert them.</span></span> <span data-ttu-id="05e3b-136">Si vous souhaitez plus en savoir sur la manière de les convertir, consultez[Si vous avez utilisé la classification classique du site Microsoft Azure Active Directory](#if-you-used-classic-azure-ad-site-classification).</span><span class="sxs-lookup"><span data-stu-id="05e3b-136">For information about how to convert them, see [If you used classic Azure AD site classification](#if-you-used-classic-azure-ad-site-classification).</span></span> 

3. <span data-ttu-id="05e3b-137">Dans la même session PowerShell, connectez-vous désormais au Centre de sécurité et de conformité à l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="05e3b-137">In the same PowerShell session, now connect to the Security & Compliance Center by using a work or school account that has global admin privileges.</span></span> <span data-ttu-id="05e3b-138">Pour obtenir des instructions, veuillez consulter [Se connecter au Centre de sécurité et conformité Office 365 PowerShell](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="05e3b-138">For instructions, see [Connect to Office 365 Security & Compliance Center PowerShell](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

4. <span data-ttu-id="05e3b-139">Exécutez les commandes suivantes pour synchroniser vos étiquettes avec Azure AD afin de pouvoir les utiliser avec des groupes Office 365 :</span><span class="sxs-lookup"><span data-stu-id="05e3b-139">Run the following commands to synchronize your labels to Azure AD, so that they can used with Office 365 groups:</span></span>
    
    ```powershell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    Execute-AzureAdLabelSync
    ```
## <a name="set-site-and-group-settings-when-you-create-or-edit-sensitivity-labels"></a><span data-ttu-id="05e3b-140">Définissez les paramètres de site et de groupe lorsque vous créez ou modifiez des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-140">Set site and group settings when you create or edit sensitivity labels</span></span>

<span data-ttu-id="05e3b-141">Une fois la préversion activée, procédez comme suit pour créer ou modifier des étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="05e3b-141">After you enable the preview, use the following steps to create or edit sensitivity labels.</span></span> <span data-ttu-id="05e3b-142">Vous devez suivre ces étapes pour que les nouvelles étiquettes de confidentialité fonctionnent avec les sites et les groupes, même si des étiquettes sont déjà définies.</span><span class="sxs-lookup"><span data-stu-id="05e3b-142">You must complete these steps for the new sensitivity labels to work with sites and groups, even if you already have labels defined.</span></span> <span data-ttu-id="05e3b-143">La synchronisation des modifications apportées à ces paramètres peut prendre jusqu’à 24 heures.</span><span class="sxs-lookup"><span data-stu-id="05e3b-143">Changes to these settings might take up to 24 hours to synchronize.</span></span>

1. <span data-ttu-id="05e3b-144">Dans le Centre de conformité Microsoft 365, sélectionnez **Classification** > **Étiquettes de confidentialité**.</span><span class="sxs-lookup"><span data-stu-id="05e3b-144">In the Microsoft 365 compliance center, select **Classification** > **Sensitivity labels**.</span></span>

2. <span data-ttu-id="05e3b-145">Sélectionnez **Créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="05e3b-145">Select **Create a label**.</span></span> <span data-ttu-id="05e3b-146">(si vous avez déjà une étiquette, passez à l’étape suivante).</span><span class="sxs-lookup"><span data-stu-id="05e3b-146">If you already have a label, skip to the next step.</span></span>

3. <span data-ttu-id="05e3b-147">Sélectionnez les options souhaitées, puis sous l’onglet **Paramètres du site et du groupe**, sélectionnez :</span><span class="sxs-lookup"><span data-stu-id="05e3b-147">Select the options you want, and then on the **Site and group settings** tab, choose:</span></span>
    
    - <span data-ttu-id="05e3b-148">Confidentialité (public/privé) : privé signifie que seuls les membres approuvés de votre organisation peuvent en consulter le contenu.</span><span class="sxs-lookup"><span data-stu-id="05e3b-148">Privacy (Public/Private): Private means that only approved members in your organization can see what's inside the group.</span></span> <span data-ttu-id="05e3b-149">Tous les autres membres de votre organisation n’ont pas cette possibilité.</span><span class="sxs-lookup"><span data-stu-id="05e3b-149">Anyone else in your organization can't see what's in the group.</span></span> [<span data-ttu-id="05e3b-150">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="05e3b-150">Learn more</span></span>](https://support.office.com/article/36236e39-26d3-420b-b0ac-8072d2d2bedc)
    - <span data-ttu-id="05e3b-151">Accès invité : vous pouvez contrôler si des invités peuvent être ajoutés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="05e3b-151">Guest access: You can control if guests can be added to a group.</span></span> [<span data-ttu-id="05e3b-152">Découvrez comment gérer l'accès invité dans les Groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="05e3b-152">Learn about managing guest access in Office 365 Groups</span></span>](/office365/admin/create-groups/manage-guest-access-in-groups)
    - <span data-ttu-id="05e3b-153">Appareils non gérés : ce paramètre vous permet de bloquer ou de limiter l’accès à du contenu SharePoint à partir d’appareils qui ne sont pas joints à AD hybride dans Intune.</span><span class="sxs-lookup"><span data-stu-id="05e3b-153">Unmanaged devices: This setting lets you block or limit access to SharePoint content from devices that aren't hybrid AD joined or compliant in Intune.</span></span> <span data-ttu-id="05e3b-154">Si vous sélectionnez appareils non gérés, vous devez accéder à Azure AD pour terminer la configuration de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="05e3b-154">If you select Unmanaged devices, you must go to Azure AD to finish setting up the policy.</span></span> <span data-ttu-id="05e3b-155">SI vous souhaitez en savoir plus, veuillez consulter[Contrôler l’accès depuis des appareils enregistrés](/sharepoint/control-access-from-unmanaged-devices).</span><span class="sxs-lookup"><span data-stu-id="05e3b-155">For info, see [Control access from unmanaged devices](/sharepoint/control-access-from-unmanaged-devices).</span></span>
    
    ![L'onglet Paramètres de site et de groupe](media/edit-sensitivity-label-site-group.png)

> [!IMPORTANT]
> <span data-ttu-id="05e3b-157">Seuls les paramètres de site et de groupe prennent effet lorsque vous appliquez une étiquette à une équipe, un groupe ou un site.</span><span class="sxs-lookup"><span data-stu-id="05e3b-157">Only the site and group settings take effect when you apply a label to a team, group, or site.</span></span> <span data-ttu-id="05e3b-158">Les autres paramètres, tels que le chiffrement et le marquage de contenu, ne sont pas appliqués à tout le contenu au sein de l’équipe, du groupe ou du site.</span><span class="sxs-lookup"><span data-stu-id="05e3b-158">Other settings, such as encryption and content marking, aren't applied to all content within the team, group, or site.</span></span>
> 
> <span data-ttu-id="05e3b-159">De même, si vous créez une étiquette et que vous n’activez pas les paramètres de site et de groupe, l’étiquette reste disponible lorsque les utilisateurs créent des équipes, des groupes et des sites, mais elle les classe sans appliquer de paramètres.</span><span class="sxs-lookup"><span data-stu-id="05e3b-159">Similarly, if you create a label and don't turn on site and group settings, the label will still be available when users create teams, groups, and sites, but it will classify without applying any settings.</span></span>

[<span data-ttu-id="05e3b-160">En savoir plus sur la publication des étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-160">Learn more about publishing sensitivity labels</span></span>](/microsoft-365/compliance/sensitivity-labels#what-label-policies-can-do)

## <a name="sensitivity-label-management"></a><span data-ttu-id="05e3b-161">Gestion des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-161">Sensitivity label management</span></span>

> [!WARNING]
> <span data-ttu-id="05e3b-162">La création, la modification et la suppression des étiquettes de confidentialité utilisées pour Microsoft Teams, les groupes Office 365 et les sites SharePoint nécessitent une coordination soigneuse avec les stratégies de publication des étiquettes pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05e3b-162">Creating, modifying, and deleting sensitivity labels that you use for Microsoft Teams, Office 365 groups, and SharePoint sites requires careful coordination with publishing label policies to users.</span></span> 

<span data-ttu-id="05e3b-163">Évitez les erreurs de création pour les sites et les groupes pouvant affecter tous les utilisateurs à l’aide des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-163">Avoid creation errors for sites and groups that can affect all users by using the following guidance.</span></span>

<span data-ttu-id="05e3b-164">**Création et publication d’étiquettes :**</span><span class="sxs-lookup"><span data-stu-id="05e3b-164">**Creating and publishing labels:**</span></span>

<span data-ttu-id="05e3b-165">Une fois que vous avez créé et publié une étiquette de confidentialité, il peut s'écouler jusqu'à 24 heures pour que l’étiquette devienne visible pour les utilisateurs d’équipes, de groupes et de sites.</span><span class="sxs-lookup"><span data-stu-id="05e3b-165">After a sensitivity label is created and published, it can take up to 24 hours for the label to become visible for users in teams, groups, and sites.</span></span> <span data-ttu-id="05e3b-166">Pour publier une étiquette pour tous les utilisateurs du client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="05e3b-166">Use the following steps to publish a label for all users in the tenant:</span></span>

1. <span data-ttu-id="05e3b-167">Créez l’étiquette de confidentialité et publiez-la pour quelques comptes d’utilisateur dans le locataire.</span><span class="sxs-lookup"><span data-stu-id="05e3b-167">Create the sensitivity label and publish it for just a few user accounts in the tenant.</span></span>

2. <span data-ttu-id="05e3b-168">Patientez 24 heures.</span><span class="sxs-lookup"><span data-stu-id="05e3b-168">Wait for 24 hours.</span></span>

3. <span data-ttu-id="05e3b-169">Une fois cette attente de 24 heures écoulée, utilisez l'un des comptes utilisateur que vous avez spécifié à l'étape 1 pour créer une équipe, un groupe Office 365 ou un site SharePoint avec l'étiquette que vous avez créée à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="05e3b-169">After this 24 hours wait, use one of the user accounts you specified in step 1 to create a team, Office 365 group, or SharePoint site with the label that you created in step 1.</span></span>

4. <span data-ttu-id="05e3b-170">S’il n’y a pas d’erreur pendant l’opération de création à l’étape 3, publiez l’étiquette pour tous les utilisateurs de votre client.</span><span class="sxs-lookup"><span data-stu-id="05e3b-170">If there are no errors during the creation operation for step 3, publish the label for all users in your tenant.</span></span> <span data-ttu-id="05e3b-171">En cas d’erreur, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="05e3b-171">If there are errors, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

<span data-ttu-id="05e3b-172">**Modification et suppression des étiquettes publiées :**</span><span class="sxs-lookup"><span data-stu-id="05e3b-172">**Modifying and deleting published labels:**</span></span>

<span data-ttu-id="05e3b-173">Si vous modifiez ou supprimez une étiquette de confidentialité incluse dans une ou plusieurs stratégies d’étiquette, ces actions peuvent entraîner des échecs de création pour toutes les équipes, les groupes et les sites.</span><span class="sxs-lookup"><span data-stu-id="05e3b-173">If you modify or delete a sensitivity label that is included in one or more label policies, these actions can result in creation failures for all teams, groups, and sites.</span></span> <span data-ttu-id="05e3b-174">Pour éviter cette situation, suivez les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="05e3b-174">To avoid this situation, use the following guidance:</span></span>

1. <span data-ttu-id="05e3b-175">Supprimez l’étiquette de confidentialité de toutes les stratégies d’étiquette qui incluent l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="05e3b-175">Remove the sensitivity label from all label policies that include the label.</span></span>

2. <span data-ttu-id="05e3b-176">Patientez 48 heures.</span><span class="sxs-lookup"><span data-stu-id="05e3b-176">Wait for 48 hours.</span></span>

3. <span data-ttu-id="05e3b-177">Une fois les 48 heures écoulées, essayez de créer une équipe, un groupe ou un site et vérifiez que l’étiquette n’est plus visible.</span><span class="sxs-lookup"><span data-stu-id="05e3b-177">After the 48 hours wait, try creating a team, group, or site and confirm that the label is no longer visible.</span></span>

4. <span data-ttu-id="05e3b-178">Si l’étiquette de confidentialité n’est pas visible, vous pouvez désormais modifier ou supprimer l’étiquette en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="05e3b-178">If the sensitivity label isn't visible, you can now safely modify or delete the label.</span></span> <span data-ttu-id="05e3b-179">Si l’étiquette est toujours visible, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="05e3b-179">If the label is still visible, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

## <a name="troubleshoot-sensitivity-label-deployment"></a><span data-ttu-id="05e3b-180">Résoudre les problèmes de déploiement des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-180">Troubleshoot sensitivity label deployment</span></span>

### <a name="labels-not-visible-after-publishing"></a><span data-ttu-id="05e3b-181">Étiquettes non visibles après la publication</span><span class="sxs-lookup"><span data-stu-id="05e3b-181">Labels not visible after publishing</span></span>
<span data-ttu-id="05e3b-182">Si vous rencontrez des problèmes lors de la création d’une équipe ou d’un groupe Office 365 une fois que vous avez activé ces paramètres ou modifié la description de l’étiquette de confidentialité, enregistrez l’étiquette, patientez quelques heures, puis essayez de créer l’équipe ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="05e3b-182">If you experience issues when you create a team or Office 365 group after you enable these settings or modify a sensitivity label's description, save the label, wait a few hours, and then try to create the team or group again.</span></span> <span data-ttu-id="05e3b-183">Pour plus d'informations, consultez [Planifier le déploiement après avoir créé ou modifié une étiquette de confidentialité](sensitivity-labels-sharepoint-onedrive-files.md#schedule-roll-out-after-you-create-or-change-a-sensitivity-label).</span><span class="sxs-lookup"><span data-stu-id="05e3b-183">For information, see [Schedule roll-out after you create or change a sensitivity label](sensitivity-labels-sharepoint-onedrive-files.md#schedule-roll-out-after-you-create-or-change-a-sensitivity-label).</span></span>

<span data-ttu-id="05e3b-184">Si vous ne parvenez toujours pas à voir la nouvelle étiquette de confidentialité depuis SharePoint Online, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="05e3b-184">If you are still not able to see the new sensitivity label from SharePoint Online, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

### <a name="team-group-or-sharepoint-site-creation-errors"></a><span data-ttu-id="05e3b-185">Erreurs de création d'équipe, de groupe ou de site SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-185">Team, group, or SharePoint site creation errors</span></span>
<span data-ttu-id="05e3b-186">Si vous rencontrez des erreurs de création dans le cadre de la préversion publique, deux options s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="05e3b-186">If you experience creation errors during the public preview, you have two options:</span></span>

- <span data-ttu-id="05e3b-187">Assurez-vous que les étiquettes de confidentialité ne sont pas obligatoires pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05e3b-187">Ensure that sensitivity labels are not mandatory for any user.</span></span>

- <span data-ttu-id="05e3b-188">Vous pouvez désactiver les étiquettes de confidentialité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint en suivant les instructions de la section [activer cette préversion](#enable-this-preview) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="05e3b-188">You can turn off sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites by using the same instructions from the [Enable this preview](#enable-this-preview) section on this page.</span></span> <span data-ttu-id="05e3b-189">Toutefois, pour désactiver la préversion, effectuez une recherche sur la ligne `$setting["EnableMIPLabels"] = "True"`et modifiez la valeur de **Vrai** en **Faux**.</span><span class="sxs-lookup"><span data-stu-id="05e3b-189">However, to disable the preview, search for the line `$setting["EnableMIPLabels"] = "True"`, and change the **True** value to **False**.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-team"></a><span data-ttu-id="05e3b-190">Appliquez une étiquette de confidentialité à une nouvelle équipe</span><span class="sxs-lookup"><span data-stu-id="05e3b-190">Apply a sensitivity label to a new team</span></span>

<span data-ttu-id="05e3b-191">Les utilisateurs peuvent sélectionner des étiquettes de confidentialité lorsqu’ils créent des équipes dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="05e3b-191">Users can select sensitivity labels when they create new teams in Microsoft Teams.</span></span> <span data-ttu-id="05e3b-192">Lorsqu’ils sélectionnent le niveau de confidentialité, le paramètre de confidentialité change autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="05e3b-192">When they select the sensitivity level, the privacy setting changes as necessary.</span></span> <span data-ttu-id="05e3b-193">Selon le paramètre d’accès invité que vous avez sélectionné pour l’étiquette, les utilisateurs peuvent ou ne peuvent pas ajouter des personnes extérieures à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="05e3b-193">Depending on the guest access setting you selected for the label, users can or can't add people outside the organization to the team.</span></span>

[<span data-ttu-id="05e3b-194">En savoir plus sur les étiquettes de niveau de confidentialité pour Teams</span><span class="sxs-lookup"><span data-stu-id="05e3b-194">Learn more about sensitivity labels for Teams</span></span>](https://docs.microsoft.com/microsoftteams/sensitivity-labels)

![Le paramètre de confidentialité lors de la création d’une équipe](media/privacy-setting-new-team.png)

<span data-ttu-id="05e3b-196">Une fois l’équipe créée, l’étiquette de confidentialité s’affiche dans le coin supérieur droit de tous les canaux.</span><span class="sxs-lookup"><span data-stu-id="05e3b-196">After you create the team, the sensitivity label appears in the upper-right corner of all channels.</span></span>

![L'étiquette de confidentialité apparaît sur l'équipe](media/privacy-setting-teams.png)

<span data-ttu-id="05e3b-198">Le service applique automatiquement la même étiquette de confidentialité au groupe Office 365 et au site d’équipe SharePoint connecté.</span><span class="sxs-lookup"><span data-stu-id="05e3b-198">The service automatically applies the same sensitivity label to the Office 365 group and the connected SharePoint team site.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-group"></a><span data-ttu-id="05e3b-199">Appliquez une étiquette de confidentialité à un nouveau groupe</span><span class="sxs-lookup"><span data-stu-id="05e3b-199">Apply a sensitivity label to a new group</span></span>

<span data-ttu-id="05e3b-200">Dans Outlook sur le web, la nouvelle boîte de dialogue **Confidentialité** contient des étiquettes publiées.</span><span class="sxs-lookup"><span data-stu-id="05e3b-200">In Outlook on the web, the new **Sensitivity** box contains published labels.</span></span> <span data-ttu-id="05e3b-201">Si les utilisateurs ont besoin d’informations supplémentaires, ils peuvent cliquer sur l’icône aide pour consulter des informations sur les étiquettes disponibles et les stratégies associées.</span><span class="sxs-lookup"><span data-stu-id="05e3b-201">If users want more info, they can click the help icon to read details about the available labels and associated policies.</span></span>

![Création d'un groupe et sélection d'une option sous Confidentialité](media/sensitivity-label-new-group.png)

## <a name="apply-a-sensitivity-label-to-a-new-site"></a><span data-ttu-id="05e3b-203">Appliquez une étiquette de confidentialité à un nouveau site</span><span class="sxs-lookup"><span data-stu-id="05e3b-203">Apply a sensitivity label to a new site</span></span>

<span data-ttu-id="05e3b-204">Les administrateurs et les utilisateurs finaux peuvent sélectionner des étiquettes de confidentialité lorsqu’ils créent des sites d’équipe et des sites de communication modernes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-204">Admins and end users can select sensitivity labels when they create modern team sites and communication sites.</span></span>

[<span data-ttu-id="05e3b-205">Découvrez comment créer un site dans le nouveau Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-205">Learn how to create a site in the new SharePoint admin center</span></span>](/sharepoint/create-site-collection)

<span data-ttu-id="05e3b-206">Lorsque les utilisateurs créent des sites d’équipe et de communication modernes, une étiquette de confidentialité est déjà sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="05e3b-206">When users create modern team and communication sites, a sensitivity label is already selected by default.</span></span> <span data-ttu-id="05e3b-207">Les utilisateurs peuvent sélectionner l’icône aide pour en savoir plus sur les étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-207">Users can select the help icon to learn more about the labels.</span></span>

![Création d'un site et sélection d'une option sous Confidentialité](media/sensitivity-label-new-communication-site.png)

<span data-ttu-id="05e3b-209">Lorsque les utilisateurs accèdent au site, ils peuvent voir le nom de l’étiquette et les stratégies appliquées.</span><span class="sxs-lookup"><span data-stu-id="05e3b-209">When users browse to the site, they can see the name of the label and applied policies.</span></span>

![Un site avec une étiquette de confidentialité appliquée](media/sensitivity-label-site.png)

## <a name="manage-sensitivity-labels-in-the-sharepoint-admin-center"></a><span data-ttu-id="05e3b-211">Gérer les étiquettes de confidentialité dans le Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-211">Manage sensitivity labels in the SharePoint admin center</span></span>

<span data-ttu-id="05e3b-212">Pour afficher et modifier les étiquettes, utilisez la page sites actifs dans le nouveau Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="05e3b-212">To view and edit the labels, use the Active sites page in the new SharePoint admin center.</span></span>

![Colonne Confidentialité de la page Sites actifs](media/manage-site-sensitivity-labels.png)

<span data-ttu-id="05e3b-214">[EN savoir plus sur la gestion des sites dans le nouveau Centre d’administration SharePoint](/sharepoint/manage-sites-in-new-admin-center).</span><span class="sxs-lookup"><span data-stu-id="05e3b-214">[Learn more about managing sites in the new SharePoint admin center](/sharepoint/manage-sites-in-new-admin-center).</span></span>

## <a name="change-site-and-group-settings-for-a-label"></a><span data-ttu-id="05e3b-215">Modifier les paramètres de site et de groupe pour une étiquette</span><span class="sxs-lookup"><span data-stu-id="05e3b-215">Change site and group settings for a label</span></span>

<span data-ttu-id="05e3b-216">Lorsque vous apportez des modifications aux paramètres de site et de groupe pour une étiquette, vous devez exécuter les commandes PowerShell suivantes pour que vos équipes, sites et groupes puissent employer les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="05e3b-216">Whenever you make a change to site and group settings for a label, you must run the following PowerShell commands so that your teams, sites, and groups can use the new settings.</span></span> <span data-ttu-id="05e3b-217">Nous vous conseillons de ne pas modifier les paramètres de site et de groupe pour une étiquette une fois que vous avez appliqué l'étiquette à plusieurs équipes, groupes ou sites.</span><span class="sxs-lookup"><span data-stu-id="05e3b-217">As a best practice, don't the change site and group settings for a label after you've applied the label to several teams, groups, or sites.</span></span>

1. <span data-ttu-id="05e3b-218">Exécutez les commandes suivantes pour vous connecter au Centre de sécurité et de conformité PowerShell d'Office 365 et obtenir la liste des étiquettes de confidentialité et leurs GUIDS.</span><span class="sxs-lookup"><span data-stu-id="05e3b-218">Run the following commands to connect to Office 365 Security & Compliance Center PowerShell and get the list of sensitivity labels and their GUIDs.</span></span>
    
    ```powershell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid
    ```

2. <span data-ttu-id="05e3b-219">Notez le GUID de l’étiquette ou des étiquettes que vous avez modifiées.</span><span class="sxs-lookup"><span data-stu-id="05e3b-219">Make a note of the GUID for the label or labels you have changed.</span></span>

3. <span data-ttu-id="05e3b-220">Connectez-vous à Exchange Online PowerShell et exécutez l’applet de commande Get-UnifiedGroup, en indiquant votre GUID d’étiquette à la place du GUID d’exemple de « e48058ea-98e8-4940-8db0-ba1310fd955e » :</span><span class="sxs-lookup"><span data-stu-id="05e3b-220">Now connect to Exchange Online PowerShell and run the Get-UnifiedGroup cmdlet, specifying your label GUID in place of the example GUID of "e48058ea-98e8-4940-8db0-ba1310fd955e":</span></span> 
    
    ```powershell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session
    $Groups= Get-UnifiedGroup | Where {$_.SensitivityLabel  -eq "e48058ea-98e8-4940-8db0-ba1310fd955e"}
    ```

4. <span data-ttu-id="05e3b-221">Réappliquez l’étiquette de confidentialité pour chaque groupe, en spécifiant le GUID de votre étiquette à la place du GUID de l’exemple de « e48058ea-98e8-4940-8db0-ba1310fd955e » :</span><span class="sxs-lookup"><span data-stu-id="05e3b-221">For each group, reapply the sensitivity label, specifying your label GUID in place of the example GUID of "e48058ea-98e8-4940-8db0-ba1310fd955e":</span></span>
    
    ```powershell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "e48058ea-98e8-4940-8db0-ba1310fd955e"}
    ```

## <a name="support-for-the-new-sensitivity-labels"></a><span data-ttu-id="05e3b-222">Prise en charge des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-222">Support for the new sensitivity labels</span></span>

<span data-ttu-id="05e3b-223">Les applications et services suivants prennent en charge les étiquettes de confidentialité dans cette préversion :</span><span class="sxs-lookup"><span data-stu-id="05e3b-223">The following apps and services support the sensitivity labels in this preview:</span></span>

- <span data-ttu-id="05e3b-224">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="05e3b-224">Microsoft 365 compliance center</span></span>
- <span data-ttu-id="05e3b-225">SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-225">SharePoint</span></span>
- <span data-ttu-id="05e3b-226">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="05e3b-226">Outlook on the web</span></span>
- <span data-ttu-id="05e3b-227">Équipes</span><span class="sxs-lookup"><span data-stu-id="05e3b-227">Teams</span></span>
- <span data-ttu-id="05e3b-228">Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="05e3b-228">SharePoint admin center</span></span>
- <span data-ttu-id="05e3b-229">Centre d’administration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="05e3b-229">Azure AD admin center</span></span>

<span data-ttu-id="05e3b-230">Vous ne pouvez pas utiliser les applications et services suivants pour créer des groupes Office 365 avec les nouvelles étiquettes de confidentialité :</span><span class="sxs-lookup"><span data-stu-id="05e3b-230">You can't use the following apps and services to create Office 365 groups with the new sensitivity labels:</span></span>

- <span data-ttu-id="05e3b-231">Outlook pour Mac</span><span class="sxs-lookup"><span data-stu-id="05e3b-231">Outlook for the Mac</span></span>
- <span data-ttu-id="05e3b-232">Outlook Mobile</span><span class="sxs-lookup"><span data-stu-id="05e3b-232">Outlook mobile</span></span>  
- <span data-ttu-id="05e3b-233">Version de bureau d’Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="05e3b-233">Outlook desktop for Windows</span></span>
- <span data-ttu-id="05e3b-234">Formulaires</span><span class="sxs-lookup"><span data-stu-id="05e3b-234">Forms</span></span>  
- <span data-ttu-id="05e3b-235">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="05e3b-235">Dynamics 365</span></span>  
- <span data-ttu-id="05e3b-236">Yammer</span><span class="sxs-lookup"><span data-stu-id="05e3b-236">Yammer</span></span>  
- <span data-ttu-id="05e3b-237">Flux</span><span class="sxs-lookup"><span data-stu-id="05e3b-237">Stream</span></span>  
- <span data-ttu-id="05e3b-238">Planificateur</span><span class="sxs-lookup"><span data-stu-id="05e3b-238">Planner</span></span>  
- <span data-ttu-id="05e3b-239">Project</span><span class="sxs-lookup"><span data-stu-id="05e3b-239">Project</span></span>  
- <span data-ttu-id="05e3b-240">PowerBI</span><span class="sxs-lookup"><span data-stu-id="05e3b-240">PowerBI</span></span>  
- <span data-ttu-id="05e3b-241">Centre d’administration Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="05e3b-241">Teams admin center</span></span>  
- <span data-ttu-id="05e3b-242">Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="05e3b-242">Microsoft 365 admin center</span></span>  
- <span data-ttu-id="05e3b-243">Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="05e3b-243">Exchange admin center</span></span>

## <a name="if-you-used-classic-azure-ad-site-classification"></a><span data-ttu-id="05e3b-244">Si vous avez utilisé la classification classique de sites Azure AD</span><span class="sxs-lookup"><span data-stu-id="05e3b-244">If you used classic Azure AD site classification</span></span>

<span data-ttu-id="05e3b-245">Office 365 ne prend plus en charge les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cette préversion.</span><span class="sxs-lookup"><span data-stu-id="05e3b-245">Office 365 no longer supports the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="05e3b-246">Toutefois, les groupes et sites existants affichent encore les anciennes classifications, sauf si vous les convertissez.</span><span class="sxs-lookup"><span data-stu-id="05e3b-246">However, existing groups and sites still display the old classifications unless you convert them.</span></span> <span data-ttu-id="05e3b-247">Les anciennes classifications incluent la classification de sites « moderne » que vous avez configurée, par l’intermédiaire d’Azure AD PowerShell ou de la bibliothèque principale PnP, qui a défini des valeurs pour le paramètre `ClassificationList`.</span><span class="sxs-lookup"><span data-stu-id="05e3b-247">Old classifications include the "modern" sites classification you set up, possibly through Azure AD PowerShell or the PnP Core library, that defined values for the `ClassificationList` setting.</span></span>

<span data-ttu-id="05e3b-248">Par exemple, dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="05e3b-248">For example, in PowerShell:</span></span>

```powershell
   ($setting["ClassificationList"])
```

<span data-ttu-id="05e3b-249">Pour plus d’informations sur l’ancienne méthode de classification, consultez [Classification des sites SharePoint « modernes »](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span><span class="sxs-lookup"><span data-stu-id="05e3b-249">For more information about the old classification method, see [SharePoint "modern" sites classification](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span></span>

<span data-ttu-id="05e3b-250">En fonction de votre déploiement actuel, deux options s’offrent à vous pour convertir vos anciennes classifications en nouvelles classifications.</span><span class="sxs-lookup"><span data-stu-id="05e3b-250">Based on your current deployment, you have two options to convert your old classifications to the new classifications.</span></span>

### <a name="if-you-never-used-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="05e3b-251">Si vous n’avez jamais utilisé les étiquettes de confidentialité (étiquettes Protection des données Microsoft unifiées) pour les fichiers et les e-mail</span><span class="sxs-lookup"><span data-stu-id="05e3b-251">If you never used sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="05e3b-252">Nous vous recommandons d’effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="05e3b-252">We recommend that you:</span></span>

1. <span data-ttu-id="05e3b-253">Créez des étiquettes de confidentialité dans le Centre de conformité Microsoft 365 portant les mêmes noms que vos classifications existantes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-253">Create new sensitivity labels in the Microsoft 365 compliance center that have the same names as your existing classifications.</span></span>
2. <span data-ttu-id="05e3b-254">Utilisez PowerShell pour appliquer les nouvelles étiquettes aux groupes et sites SharePoint Office 365 existants à l’aide du mappage de noms.</span><span class="sxs-lookup"><span data-stu-id="05e3b-254">Use PowerShell to apply the new labels to existing Office 365 groups and SharePoint sites using name mapping.</span></span>
3. <span data-ttu-id="05e3b-255">Supprimez les anciennes classifications.</span><span class="sxs-lookup"><span data-stu-id="05e3b-255">Delete the old classifications.</span></span>

<span data-ttu-id="05e3b-256">Les applications et les services qui prennent en charge les nouvelles étiquettes de confidentialité les affichent.</span><span class="sxs-lookup"><span data-stu-id="05e3b-256">Apps and services that support the new sensitivity labels will show them.</span></span> <span data-ttu-id="05e3b-257">Vous créez des équipes, des groupes et des sites avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-257">You create new teams, groups, and sites with the new labels.</span></span> <span data-ttu-id="05e3b-258">Les utilisateurs peuvent créer des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-258">Users can still create groups from apps and services that don't support the new labels.</span></span> <span data-ttu-id="05e3b-259">Toutefois, les utilisateurs ne peuvent pas appliquer une étiquette à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-259">However, users can't apply a label to these groups.</span></span> <span data-ttu-id="05e3b-260">Utilisez PowerShell pour appliquer les nouvelles étiquettes de confidentialité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-260">Use PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="05e3b-261">Vous pouvez conserver vos anciennes classifications. Toutefois, nous vous recommandons vivement d’utiliser PowerShell pour appliquer les nouvelles étiquettes de confidentialité à ces groupes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-261">You can keep your old classifications; however, we highly recommend using PowerShell to apply the new sensitivity labels to these groups.</span></span>

<span data-ttu-id="05e3b-262">Les applications et les services qui prennent en charge les nouvelles étiquettes de confidentialité sont créées avec les nouvelles étiquettes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-262">Apps and services that support the new sensitivity labels will get created with the new labels.</span></span> <span data-ttu-id="05e3b-263">Lorsque les utilisateurs créent des groupes à partir d’applications et de services qui ne prennent pas en charge les nouvelles étiquettes, ils peuvent sélectionner une classification.</span><span class="sxs-lookup"><span data-stu-id="05e3b-263">When users create groups from apps and services that don't support the new labels, they can select a classification.</span></span>

### <a name="if-you-use-sensitivity-labels-unified-microsoft-information-protection-labels-for-files-and-email"></a><span data-ttu-id="05e3b-264">Si vous utilisez les étiquettes de confidentialité (étiquettes Protection des données Microsoft unifiées) pour les fichiers et les e-mail</span><span class="sxs-lookup"><span data-stu-id="05e3b-264">If you use sensitivity labels (unified Microsoft Information Protection labels) for files and email</span></span>

<span data-ttu-id="05e3b-265">Une fois la préversion activée, accédez à chaque étiquette dans le Centre de conformité Microsoft 365 et appliquez les stratégies souhaitées pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-265">As soon as you enable this preview, go to each label in the Microsoft 365 compliance center and apply the policies you want for sites and groups.</span></span> <span data-ttu-id="05e3b-266">Les utilisateurs commencent à voir vos étiquettes existantes disponibles pour les sites et les groupes.</span><span class="sxs-lookup"><span data-stu-id="05e3b-266">Users will start seeing your existing labels available for sites and groups.</span></span>

### <a name="prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups"></a><span data-ttu-id="05e3b-267">Préparer SharePoint Online Management Shell avant d’attribuer un nouveau libellé les groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="05e3b-267">Prepare the SharePoint Online Management Shell before you relabel Office 365 groups</span></span>

<span data-ttu-id="05e3b-268">Avant d’appliquer de nouvelles étiquettes, assurez-vous que vous exécutez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="05e3b-268">Before you apply new labels, ensure that you're running the latest SharePoint Online Management Shell.</span></span> <span data-ttu-id="05e3b-269">Si vous disposez déjà de la dernière version, vous pouvez [Attribuer un nouveau libellé aux groupes Office 365 avec de nouvelles étiquettes de confidentialité](#relabel-office-365-groups-with-new-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="05e3b-269">If you already have the latest version, you can go ahead and [Relabel Office 365 groups with new sensitivity labels](#relabel-office-365-groups-with-new-sensitivity-labels).</span></span>

<span data-ttu-id="05e3b-270">Pour préparer SharePoint Online Management Shell pour la préversion :</span><span class="sxs-lookup"><span data-stu-id="05e3b-270">To prepare the SharePoint Online Management Shell for the preview:</span></span>

1. <span data-ttu-id="05e3b-271">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à **Ajouter ou supprimer des programmes** et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="05e3b-271">If you installed a previous version of the SharePoint Online Management Shell, go to **Add or remove programs** and uninstall “SharePoint Online Management Shell”.</span></span>

2. <span data-ttu-id="05e3b-272">Dans un navigateur web, accédez à la page du Centre de téléchargement et [Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="05e3b-272">In a web browser, go to the Download Center page and [Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

3. <span data-ttu-id="05e3b-273">Sélectionnez votre langue, puis cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="05e3b-273">Select your language and then click **Download**.</span></span>

4. <span data-ttu-id="05e3b-274">Choisissez entre le fichier x64 et x86 .msi.</span><span class="sxs-lookup"><span data-stu-id="05e3b-274">Choose between the x64 and x86 .msi file.</span></span> <span data-ttu-id="05e3b-275">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="05e3b-275">Download the x64 file if you run the 64-bit version of Windows or the x86 file if you’re run the 32-bit version.</span></span> <span data-ttu-id="05e3b-276">En cas de doute, consultez [Quelle est la version du système d’exploitation Windows que j’utilise ?.](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="05e3b-276">If you don’t know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span>

5. <span data-ttu-id="05e3b-277">Une fois le fichier téléchargé, exécutez le fichier et suivez les étapes de l'Assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="05e3b-277">After you download the file, run the file and follow the steps in the Setup Wizard.</span></span>

### <a name="relabel-office-365-groups-with-new-sensitivity-labels"></a><span data-ttu-id="05e3b-278">Attribuez un nouveau libellé aux groupes Office 365 avec d’autres étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="05e3b-278">Relabel Office 365 groups with new sensitivity labels</span></span>

1. <span data-ttu-id="05e3b-279">Assurez-vous que vous utilisez la dernière version de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="05e3b-279">Ensure that you're using the latest version of the SharePoint Online Management Shell.</span></span> <span data-ttu-id="05e3b-280">Pour obtenir des instructions, consultez [Préparer SharePoint Online Management Shell avant d’attribuer un nouveau libellé les groupes Office 365](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span><span class="sxs-lookup"><span data-stu-id="05e3b-280">For instructions, see [Prepare the SharePoint Online Management Shell before you relabel Office 365 groups](#prepare-the-sharepoint-online-management-shell-before-you-relabel-office-365-groups).</span></span>

2. <span data-ttu-id="05e3b-281">À l’aide d’un compte professionnel ou scolaire avec des privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="05e3b-281">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint Online Management Shell.</span></span> <span data-ttu-id="05e3b-282">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="05e3b-282">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

3. <span data-ttu-id="05e3b-283">Exécutez la commande suivante pour obtenir la liste des étiquettes de confidentialité et leurs GUID.</span><span class="sxs-lookup"><span data-stu-id="05e3b-283">Run the following command to get the list of sensitivity labels and their GUIDs.</span></span>

    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid  
    ```

4. <span data-ttu-id="05e3b-284">Notez le GUID de l’étiquette que vous voulez remplacer.</span><span class="sxs-lookup"><span data-stu-id="05e3b-284">Make a note of the GUID for the label you want to overwrite.</span></span> <span data-ttu-id="05e3b-285">Par exemple, l’étiquette « Général ».</span><span class="sxs-lookup"><span data-stu-id="05e3b-285">For example, the "General" label.</span></span>

5. <span data-ttu-id="05e3b-286">Utilisez la commande suivante pour obtenir la liste des groupes qui ont la classification « Général ».</span><span class="sxs-lookup"><span data-stu-id="05e3b-286">Use the following command to get the list of groups that have the “General” classification.</span></span> <span data-ttu-id="05e3b-287">Lorsque vous exécutez cette commande, vous vous connectez à Exchange Online PowerShell et exécutez la cmdlet Get-UnifiedGroup.</span><span class="sxs-lookup"><span data-stu-id="05e3b-287">When you run this command, you'll connect to Exchange Online PowerShell and run the Get-UnifiedGroup cmdlet.</span></span>

   ```PowerShell
   Set-ExecutionPolicy RemoteSigned
   $UserCredential = Get-Credential
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   Import-PSSession $Session
   $Groups= Get-UnifiedGroup | Where {$_.classification -eq "General"}
   ```

6. <span data-ttu-id="05e3b-288">Pour chaque groupe, ajoutez le nouveau GUID de l’étiquette de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="05e3b-288">For each group, add the new sensitivity label GUID.</span></span>

    ```PowerShell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "457fa763-7c59-461c-b402-ad1ac6b703cc"}
    ```
