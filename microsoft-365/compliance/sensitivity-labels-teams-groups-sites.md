---
title: Utiliser des étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)
f1.keywords:
- NOCSH
ms.author: cabailey
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
description: Utilisez les étiquettes de confidentialité pour protéger le contenu des sites SharePoint et Microsoft Teams, ainsi que des groupes Office 365.
ms.openlocfilehash: 0ac1d9f605c32664115086057b7c17355d495c00
ms.sourcegitcommit: e695bcfc69203da5d3d96f3d6a891664a0e27ae2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43106132"
---
# <a name="use-sensitivity-labels-to-protect-content-in-microsoft-teams-office-365-groups-and-sharepoint-sites-public-preview"></a><span data-ttu-id="fd096-103">Utiliser les étiquettes de confidentialité pour protéger le contenu dans Microsoft Teams, les groupes Office 365 et les sites SharePoint (préversion publique)</span><span class="sxs-lookup"><span data-stu-id="fd096-103">Use sensitivity labels to protect content in Microsoft Teams, Office 365 groups, and SharePoint sites (public preview)</span></span>

><span data-ttu-id="fd096-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="fd096-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="fd096-105">Lorsque vous créez des étiquettes de confidentialité dans le [Centre de conformité Microsoft 365](https://protection.office.com/), vous pouvez désormais les appliquer aux conteneurs suivants : les sites Microsoft Teams et SharePoint et les groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd096-105">When you create sensitivity labels in the [Microsoft 365 compliance center](https://protection.office.com/), you can now apply them to the following containers: Microsoft Teams sites, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="fd096-106">Utilisez les paramètres d’étiquette suivants pour renforcer la protection du contenu de ces conteneurs :</span><span class="sxs-lookup"><span data-stu-id="fd096-106">Use the following label settings to help protect the content in those containers:</span></span>

- <span data-ttu-id="fd096-107">Confidentialité (privée ou publique) de sites d’équipes Office 365 connectés au groupe</span><span class="sxs-lookup"><span data-stu-id="fd096-107">Privacy (public or private) of Office 365 group-connected teams sites</span></span>
- <span data-ttu-id="fd096-108">Accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="fd096-108">External users access</span></span>
- <span data-ttu-id="fd096-109">Accès à partir d’appareils enregistrés</span><span class="sxs-lookup"><span data-stu-id="fd096-109">Access from unmanaged devices</span></span> 

<span data-ttu-id="fd096-110">Lorsque vous appliquez cette étiquette à l’un des conteneurs pris en charge, l’étiquette applique automatiquement les options configurées au site ou au groupe connecté.</span><span class="sxs-lookup"><span data-stu-id="fd096-110">When you apply this label to a supported container, the label automatically applies the configured options to the connected site or group.</span></span> 

<span data-ttu-id="fd096-111">Le contenu de ces conteneurs n’hérite toutefois pas des étiquettes pour les paramètres tels que le nom d’étiquette, les marques visuelles ou le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fd096-111">Content in those containers however, do not inherit the labels for settings such as the label name, visual markings, or encryption.</span></span> <span data-ttu-id="fd096-112">Pour que les utilisateurs puissent étiqueter leurs documents sur des sites SharePoint ou des sites d’équipe, [Activer les étiquettes de confidentialité pour les fichiers Office dans SharePoint et OneDrive](sensitivity-labels-sharepoint-onedrive-files.md).</span><span class="sxs-lookup"><span data-stu-id="fd096-112">So that users can label their documents in SharePoint sites or team sites, [enable sensitivity labels for Office files in SharePoint and OneDrive](sensitivity-labels-sharepoint-onedrive-files.md).</span></span>

## <a name="about-the-public-preview-for-microsoft-teams-office-365-groups-and-sharepoint-sites"></a><span data-ttu-id="fd096-113">À propos de la préversion publique Microsoft Teams, les groupes Office 365 et les sites SharePoint</span><span class="sxs-lookup"><span data-stu-id="fd096-113">About the public preview for Microsoft Teams, Office 365 groups, and SharePoint sites</span></span>

<span data-ttu-id="fd096-114">Les étiquettes de confidentialité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint sont progressivement déployés pour les clients, et peuvent encore être modifiées avant la publication finale.</span><span class="sxs-lookup"><span data-stu-id="fd096-114">Sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites are in gradual rollout to tenants and might change before final release.</span></span> <span data-ttu-id="fd096-115">Cette préversion publique ne fonctionne pas avec les réseaux de distribution de contenu Office 365 (CDN).</span><span class="sxs-lookup"><span data-stu-id="fd096-115">This public preview doesn't work with Office 365 Content Delivery Networks (CDNs).</span></span>

<span data-ttu-id="fd096-116">Avant d’activer cette préversion et de configurer des étiquettes de confidentialité pour les nouveaux paramètres, les utilisateurs peuvent afficher et appliquer des étiquettes de confidentialité dans leurs applications.</span><span class="sxs-lookup"><span data-stu-id="fd096-116">Before you enable this preview and configure sensitivity labels for the new settings, users can see and apply sensitivity labels in their apps.</span></span> <span data-ttu-id="fd096-117">Par exemple, à partir de Word :</span><span class="sxs-lookup"><span data-stu-id="fd096-117">For example, from Word:</span></span>

![Étiquette de confidentialité affichée dans l’application de bureau Word](../media/sensitivity-label-word.png)

<span data-ttu-id="fd096-119">Après avoir activé et configuré cette préversion, les utilisateurs peuvent également voir et appliquer des étiquettes de confidentialité à Microsoft Teams, à des groupes Office 365 et à des sites SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fd096-119">After you enable and configure this preview, users can additionally see and apply sensitivity labels to Microsoft Teams, Office 365 groups, and SharePoint sites.</span></span> <span data-ttu-id="fd096-120">Par exemple, lorsque vous créez un nouveau site d’équipe à partir de SharePoint :</span><span class="sxs-lookup"><span data-stu-id="fd096-120">For example, when you create a new team site from SharePoint:</span></span>

![Étiquette de confidentialité lors de la création d’un site d’équipe à partir de SharePoint](../media/sensitivity-labels-new-team-site.png)

## <a name="enable-this-preview-and-synchronize-labels"></a><span data-ttu-id="fd096-122">Activez cette préversion et synchronisez des étiquettes</span><span class="sxs-lookup"><span data-stu-id="fd096-122">Enable this preview and synchronize labels</span></span>

1. <span data-ttu-id="fd096-123">Cette fonctionnalité utilisant une fonctionnalité Azure Active Directory, suivez les instructions de la documentation Azure Active Directory pour activer la préversion : [Attribuer des étiquettes de confidentialité à des groupes Office 365 dans Azure Active Directory (préversion)](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="fd096-123">Because this feature uses Azure AD functionality, follow the instructions in the Azure AD documentation to enable the preview: [Assign sensitivity labels to Office 365 groups in Azure Active Directory (preview)](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels).</span></span>

2. <span data-ttu-id="fd096-124">Ouvrez une session PowerShell avec l’option **Exécuter en tant qu’Administrateur**, puis connectez-vous au Centre de Sécurité & de Conformité à l’aide d’un compte professionnel ou scolaire disposant de privilèges d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="fd096-124">Open a PowerShell session with the **Run as Administrator** option, and connect to the Security & Compliance Center by using a work or school account that has global admin privileges.</span></span> <span data-ttu-id="fd096-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fd096-125">For example:</span></span>
    
    ```powershell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    ```
    
    <span data-ttu-id="fd096-126">Si vous souhaitez voir les instructions détaillées, consultez [Se connecter au Centre de sécurité et conformité Office 365 Powershell](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="fd096-126">For full instructions, see [Connect to Office 365 Security & Compliance Center PowerShell](/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>

3. <span data-ttu-id="fd096-127">Exécutez la commande suivante pour synchroniser vos étiquettes de confidentialité avec Azure AD afin de pouvoir les utiliser avec des groupes Office 365 :</span><span class="sxs-lookup"><span data-stu-id="fd096-127">Run the following command to synchronize your sensitivity labels to Azure AD, so that they can be used with Office 365 groups:</span></span>
    
    ```powershell
    Execute-AzureAdLabelSync
    ```

## <a name="how-to-configure-site-and-group-settings-when-you-create-or-edit-sensitivity-labels"></a><span data-ttu-id="fd096-128">Configuration de paramètres de site et de groupe lorsque vous créez ou modifiez des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-128">How to configure site and group settings when you create or edit sensitivity labels</span></span>

<span data-ttu-id="fd096-129">Vous êtes maintenant prêt à créer ou modifier les étiquettes de confidentialité que vous souhaitez rendre disponibles pour des sites et des groupes.</span><span class="sxs-lookup"><span data-stu-id="fd096-129">You're now ready to create or edit sensitivity labels that you want to be available for sites and groups.</span></span> <span data-ttu-id="fd096-130">L’activation de la préversion permet de rendre une nouvelle page visible dans les assistants d'étiquetage de confidentialité : **Paramètres de site et de groupe**</span><span class="sxs-lookup"><span data-stu-id="fd096-130">Enabling the preview makes a new page visible in the sensitivity labeling wizards: **Site and group settings**</span></span>

<span data-ttu-id="fd096-131">Si vous avez besoin d’aide pour créer ou modifier une étiquette de confidentialité, consultez les instructions sur la [Création et configuration d'étiquettes de confidentialité](create-sensitivity-labels.md#create-and-configure-sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="fd096-131">If you need help with creating or editing a sensitivity label, see the instructions from [Create and configure sensitivity labels](create-sensitivity-labels.md#create-and-configure-sensitivity-labels).</span></span>

<span data-ttu-id="fd096-132">Dans cette nouvelle page de **Paramètres de site et de groupe**, configurez les paramètres :</span><span class="sxs-lookup"><span data-stu-id="fd096-132">On this new **Site and group settings** page, configure the settings:</span></span>

- <span data-ttu-id="fd096-133">**Confidentialité des sites d’équipe connectés au groupe Office 365** : le paramètre par défaut actuellement déployé pour les clients est **Aucune, l'utilisateur choisit qui peut accéder au site**.</span><span class="sxs-lookup"><span data-stu-id="fd096-133">**Privacy of Office 365 group-connected teams sites**: The default setting of **None - let user chose who can access the site** is currently rolling out to tenants.</span></span> <span data-ttu-id="fd096-134">Conservez ce paramètre par défaut si vous souhaitez protéger le contenu dans le conteneur à l’aide de l’étiquette de confidentialité, tout en laissant les utilisateurs configurer eux-même les paramètres de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="fd096-134">Keep this default setting when you want to protect content in the container by using the sensitivity label, but still let users configure the privacy setting themselves.</span></span>
    
    <span data-ttu-id="fd096-135">Sélectionnez **Public** ou **privé** pour définir et verrouiller le paramètre de confidentialité lorsque vous appliquez cette étiquette au conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd096-135">Select **Public** or**Private** to set and lock the privacy setting when you apply this label to the container.</span></span> <span data-ttu-id="fd096-136">Sélectionnez **Public** si vous souhaitez que tous les membres de votre organisation accèdent au site d’équipe ou au groupe dans lequel cette étiquette est appliquée, ou **Privé** si vous souhaitez limiter l’accès aux seuls membres approuvés au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fd096-136">Choose **Public** if you want anyone in your organization to access the team site or group where this label is applied, or **Private** if you want access to be restricted to only approved members in your organization.</span></span> 
    
    <span data-ttu-id="fd096-137">Le paramètre **Public** or **Privé** remplace le paramètre précédemment configuré pour l’équipe ou le groupe et verrouille la valeur de confidentialité afin qu’elle puisse être modifiée uniquement en supprimant d’abord l’étiquette de confidentialité du conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd096-137">The **Public** or **Private** setting replaces any previous privacy setting that might be configured for the team or group, and locks the privacy value so it can be changed only by first removing the sensitivity label from the container.</span></span> <span data-ttu-id="fd096-138">Une fois l'étiquette de confidentialité supprimée, le paramètre de confidentialité de l'étiquette peut à nouveau être modifié par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fd096-138">After you remove the sensitivity label, the privacy setting from the label remains and users can now change it again.</span></span>

- <span data-ttu-id="fd096-139">**Accès des utilisateurs externes** : déterminez si le propriétaire du groupe peut [ajouter des invités au groupe](/office365/admin/create-groups/manage-guest-access-in-groups).</span><span class="sxs-lookup"><span data-stu-id="fd096-139">**External users access**: Control whether the group owner can [add guests to the group](/office365/admin/create-groups/manage-guest-access-in-groups).</span></span>

- <span data-ttu-id="fd096-140">**Appareils non gérés** : pour les [appareils non gérés](/sharepoint/control-access-from-unmanaged-devices), autorisez l’accès total, l’accès web uniquement ou bloquer totalement l’accès.</span><span class="sxs-lookup"><span data-stu-id="fd096-140">**Unmanaged devices**: For [unmanaged devices](/sharepoint/control-access-from-unmanaged-devices), allow full access, web only access, or block access completely.</span></span> 

![L'onglet Paramètres de site et de groupe](../media/edit-sensitivity-label-site-group.png)

> [!IMPORTANT]
> <span data-ttu-id="fd096-142">Seuls ces paramètres de sites et de groupes prennent effet lorsque vous appliquez une étiquette à une équipe, un groupe ou un site.</span><span class="sxs-lookup"><span data-stu-id="fd096-142">Only these site and group settings take effect when you apply a label to a team, group, or site.</span></span> <span data-ttu-id="fd096-143">D'autres paramètres d'étiquette, tels que le chiffrement et le marquage de contenu, ne sont pas appliqués au contenu au sein de l’équipe, du groupe ou du site.</span><span class="sxs-lookup"><span data-stu-id="fd096-143">Other label settings, such as encryption and content marking, aren't applied to the content within the team, group, or site.</span></span>
> 
> <span data-ttu-id="fd096-144">Déploiement progressif sur les clients : seules les étiquettes concernant les paramètres de site et de groupe peuvent être sélectionnées lorsque les utilisateurs créent des équipes, des groupes et des sites.</span><span class="sxs-lookup"><span data-stu-id="fd096-144">Gradually rolling out to tenants: Only labels with the site and group settings will be available to select when users create teams, groups, and sites.</span></span> <span data-ttu-id="fd096-145">Si vous pouvez appliquer une étiquette à un conteneur alors que les paramètres de site et de groupe ne sont pas activés, seul le nom d’étiquette est appliqué au conteneur.</span><span class="sxs-lookup"><span data-stu-id="fd096-145">If you can currently apply a label to a container when the label doesn't have the site and group settings enabled, only the label name is applied to the container.</span></span>

<span data-ttu-id="fd096-146">Si votre étiquette de confidentialité n’est pas encore publiée, publiez-la dès maintenant en [l’ajoutant à une stratégie d'étiquette de confidentialité](create-sensitivity-labels.md#publish-sensitivity-labels-by-creating-a-label-policy).</span><span class="sxs-lookup"><span data-stu-id="fd096-146">If your sensitivity label isn't already published, now publish it by [adding it to a sensitivity label policy](create-sensitivity-labels.md#publish-sensitivity-labels-by-creating-a-label-policy).</span></span> <span data-ttu-id="fd096-147">Les utilisateurs auxquels sont assignés une stratégie d’étiquette de confidentialité incluant cette étiquette pourront la sélectionner pour des sites et des groupes.</span><span class="sxs-lookup"><span data-stu-id="fd096-147">The users who are assigned a sensitivity label policy that includes this label will be able to select it for sites and groups.</span></span>

<span data-ttu-id="fd096-148">À partir de la stratégie d’étiquette, seul le paramètre de stratégie **Appliquer cette étiquette par défaut aux documents et aux e-mails** s’applique lorsque vous appliquez cette étiquette à des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="fd096-148">From the label policy, only the policy setting **Apply this label by default to documents and email** is applicable when you apply this label to containers.</span></span> <span data-ttu-id="fd096-149">Les autres paramètres de stratégie ne sont pas appliqués, notamment l'étiquetage obligatoire, la justification de l'utilisateur et le lien vers la page d'aide personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fd096-149">Other policy settings are not applied, which include mandatory labeling, requiring user justification, and a link to the custom help page.</span></span>

## <a name="sensitivity-label-management"></a><span data-ttu-id="fd096-150">Gestion des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-150">Sensitivity label management</span></span>

> [!WARNING]
> <span data-ttu-id="fd096-151">La création, la modification et la suppression des étiquettes de confidentialité utilisées pour Microsoft Teams, les groupes Office 365 et les sites SharePoint nécessitent une coordination soigneuse avec les stratégies de publication des étiquettes pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fd096-151">Creating, modifying, and deleting sensitivity labels that you use for Microsoft Teams, Office 365 groups, and SharePoint sites requires careful coordination with publishing label policies to users.</span></span> 

<span data-ttu-id="fd096-152">Évitez les erreurs de création pour les sites et les groupes pouvant affecter tous les utilisateurs à l’aide des instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd096-152">Avoid creation errors for sites and groups that can affect all users by using the following guidance.</span></span>

<span data-ttu-id="fd096-153">**Création et publication d’étiquettes :**</span><span class="sxs-lookup"><span data-stu-id="fd096-153">**Creating and publishing labels:**</span></span>

<span data-ttu-id="fd096-154">Une fois que vous avez créé et publié une étiquette de confidentialité, il peut s'écouler jusqu'à 24 heures pour que l’étiquette devienne visible pour les utilisateurs d’équipes, de groupes et de sites.</span><span class="sxs-lookup"><span data-stu-id="fd096-154">After a sensitivity label is created and published, it can take up to 24 hours for the label to become visible for users in teams, groups, and sites.</span></span> <span data-ttu-id="fd096-155">Pour publier une étiquette pour tous les utilisateurs du client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd096-155">Use the following steps to publish a label for all users in the tenant:</span></span>

1. <span data-ttu-id="fd096-156">Créez l’étiquette de confidentialité et publiez-la pour quelques comptes d’utilisateur dans le locataire.</span><span class="sxs-lookup"><span data-stu-id="fd096-156">Create the sensitivity label and publish it for just a few user accounts in the tenant.</span></span>

2. <span data-ttu-id="fd096-157">Patientez 24 heures.</span><span class="sxs-lookup"><span data-stu-id="fd096-157">Wait for 24 hours.</span></span>

3. <span data-ttu-id="fd096-158">Une fois cette attente de 24 heures écoulée, utilisez l'un des comptes utilisateur que vous avez spécifié à l'étape 1 pour créer une équipe, un groupe Office 365 ou un site SharePoint avec l'étiquette que vous avez créée à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="fd096-158">After this 24 hours wait, use one of the user accounts you specified in step 1 to create a team, Office 365 group, or SharePoint site with the label that you created in step 1.</span></span>

4. <span data-ttu-id="fd096-159">S’il n’y a pas d’erreur pendant l’opération de création à l’étape 3, publiez l’étiquette pour tous les utilisateurs de votre client.</span><span class="sxs-lookup"><span data-stu-id="fd096-159">If there are no errors during the creation operation for step 3, publish the label for all users in your tenant.</span></span> <span data-ttu-id="fd096-160">En cas d’erreur, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="fd096-160">If there are errors, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

<span data-ttu-id="fd096-161">**Modification et suppression des étiquettes publiées :**</span><span class="sxs-lookup"><span data-stu-id="fd096-161">**Modifying and deleting published labels:**</span></span>

<span data-ttu-id="fd096-162">Modifier ou supprimer une étiquette de confidentialité avec les paramètres de site et de groupe activés alors que cette étiquette est incluse dans d’autres stratégies d'étiquette, peut entraîner des échecs de création pour toutes les équipes, tous les groupes et tous les sites.</span><span class="sxs-lookup"><span data-stu-id="fd096-162">If you modify or delete a sensitivity label with the site and group settings enabled, and that label is included in one or more label policies, these actions can result in creation failures for all teams, groups, and sites.</span></span> <span data-ttu-id="fd096-163">Pour éviter cette situation, suivez les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd096-163">To avoid this situation, use the following guidance:</span></span>

1. <span data-ttu-id="fd096-164">Supprimez l’étiquette de confidentialité de toutes les stratégies d’étiquette qui incluent l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="fd096-164">Remove the sensitivity label from all label policies that include the label.</span></span>

2. <span data-ttu-id="fd096-165">Patientez 48 heures.</span><span class="sxs-lookup"><span data-stu-id="fd096-165">Wait for 48 hours.</span></span>

3. <span data-ttu-id="fd096-166">Une fois les 48 heures écoulées, essayez de créer une équipe, un groupe ou un site et vérifiez que l’étiquette n’est plus visible.</span><span class="sxs-lookup"><span data-stu-id="fd096-166">After the 48 hours wait, try creating a team, group, or site and confirm that the label is no longer visible.</span></span>

4. <span data-ttu-id="fd096-167">Si l’étiquette de confidentialité n’est pas visible, vous pouvez désormais modifier ou supprimer l’étiquette en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="fd096-167">If the sensitivity label isn't visible, you can now safely modify or delete the label.</span></span> <span data-ttu-id="fd096-168">Si l’étiquette est toujours visible, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="fd096-168">If the label is still visible, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

## <a name="assign-sensitivity-labels-to-office-365-groups"></a><span data-ttu-id="fd096-169">Attribuer des étiquettes de confidentialité à des groupes Office 365</span><span class="sxs-lookup"><span data-stu-id="fd096-169">Assign sensitivity labels to Office 365 groups</span></span>

<span data-ttu-id="fd096-170">Vous êtes désormais prêt à appliquer une ou plusieurs étiquettes de confidentialité à des groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd096-170">You're now ready to apply the sensitivity label or labels to Office 365 groups.</span></span> <span data-ttu-id="fd096-171">Revenez à la documentation Azure Active Directory pour les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd096-171">Return to the Azure AD documentation for instructions:</span></span>

- [<span data-ttu-id="fd096-172">Attribuer une étiquette à un nouveau groupe dans le Portail Azure</span><span class="sxs-lookup"><span data-stu-id="fd096-172">Assign a label to a new group in Azure portal</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#assign-a-label-to-a-new-group-in-azure-portal)

-  [<span data-ttu-id="fd096-173">Attribuer une étiquette à un groupe existant dans le Portail Azure</span><span class="sxs-lookup"><span data-stu-id="fd096-173">Assign a label to an existing group in Azure portal</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#assign-a-label-to-an-existing-group-in-azure-portal)

-  <span data-ttu-id="fd096-174">[Supprimer une étiquette dans un groupe existant dans le Portail Azure](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#remove-a-label-from-an-existing-group-in-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="fd096-174">[Remove a label from an existing group in Azure portal](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#remove-a-label-from-an-existing-group-in-azure-portal).</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-team"></a><span data-ttu-id="fd096-175">Appliquez une étiquette de confidentialité à une nouvelle équipe</span><span class="sxs-lookup"><span data-stu-id="fd096-175">Apply a sensitivity label to a new team</span></span>

<span data-ttu-id="fd096-176">Les utilisateurs peuvent sélectionner des étiquettes de confidentialité lorsqu’ils créent des équipes dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="fd096-176">Users can select sensitivity labels when they create new teams in Microsoft Teams.</span></span> <span data-ttu-id="fd096-177">Lorsqu’ils sélectionnent l’étiquette dans la liste déroulante **Confidentialité**, le paramètre de confidentialité peut être modifié pour refléter la configuration de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="fd096-177">When they select the label from the **Sensitivity** dropdown, the privacy setting might change to reflect the label configuration.</span></span> <span data-ttu-id="fd096-178">Selon le paramètre d’accès pour les utilisateurs externes que vous avez sélectionné pour l’étiquette, les utilisateurs peuvent ajouter ou non des personnes extérieures à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="fd096-178">Depending on the external users access setting you selected for the label, users can or can't add people outside the organization to the team.</span></span>

[<span data-ttu-id="fd096-179">En savoir plus sur les étiquettes de niveau de confidentialité pour Teams</span><span class="sxs-lookup"><span data-stu-id="fd096-179">Learn more about sensitivity labels for Teams</span></span>](https://docs.microsoft.com/microsoftteams/sensitivity-labels)

![Le paramètre de confidentialité lors de la création d’une équipe](../media/privacy-setting-new-team.png)

<span data-ttu-id="fd096-181">Une fois l’équipe créée, l’étiquette de confidentialité s’affiche dans le coin supérieur droit de tous les canaux.</span><span class="sxs-lookup"><span data-stu-id="fd096-181">After you create the team, the sensitivity label appears in the upper-right corner of all channels.</span></span>

![L'étiquette de confidentialité apparaît sur l'équipe](../media/privacy-setting-teams.png)

<span data-ttu-id="fd096-183">Le service applique automatiquement la même étiquette de confidentialité au groupe Office 365 et au site d’équipe SharePoint connecté.</span><span class="sxs-lookup"><span data-stu-id="fd096-183">The service automatically applies the same sensitivity label to the Office 365 group and the connected SharePoint team site.</span></span>

## <a name="apply-a-sensitivity-label-to-a-new-group-in-outlook-on-the-web"></a><span data-ttu-id="fd096-184">Appliquez une étiquette de confidentialité à un nouveau groupe dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="fd096-184">Apply a sensitivity label to a new group in Outlook on the web</span></span>

<span data-ttu-id="fd096-185">Dans Outlook sur le web, lorsque vous créez un groupe, vous pouvez sélectionner ou modifier l’option de **Confidentialité** pour les étiquettes publiées :</span><span class="sxs-lookup"><span data-stu-id="fd096-185">In Outlook on the web, when you create a new group, you can select or change the **Sensitivity** option for published labels:</span></span>

![Création d'un groupe et sélection d'une option sous Confidentialité](../media/sensitivity-label-new-group.png)

## <a name="apply-a-sensitivity-label-to-a-new-site"></a><span data-ttu-id="fd096-187">Appliquez une étiquette de confidentialité à un nouveau site</span><span class="sxs-lookup"><span data-stu-id="fd096-187">Apply a sensitivity label to a new site</span></span>

<span data-ttu-id="fd096-188">Les administrateurs et les utilisateurs finaux peuvent sélectionner des étiquettes de confidentialité lorsqu’ils [créent des sites d’équipe et des sites de communication modernes](/sharepoint/create-site-collection), et développent les **Paramètres avancés** :</span><span class="sxs-lookup"><span data-stu-id="fd096-188">Admins and end users can select sensitivity labels when they [create modern team sites and communication sites](/sharepoint/create-site-collection), and expand **Advanced settings**:</span></span>

![Création d'un site et sélection d'une option sous Confidentialité](../media/sensitivity-label-new-communication-site.png)

<span data-ttu-id="fd096-190">La liste déroulante affiche les noms d'étiquette pour la sélection, et l'icône d'aide affiche tous les noms d'étiquette avec leur info-bulle, ce qui peut aider les utilisateurs à déterminer l'étiquette correcte à appliquer.</span><span class="sxs-lookup"><span data-stu-id="fd096-190">The dropdown box displays the label names for the selection, and the help icon displays all the label names with their tooltip, which can help users determine the correct label to apply.</span></span>

<span data-ttu-id="fd096-191">Lorsque l'étiquette est appliquée et que les utilisateurs accèdent au site, ils voient le nom de l'étiquette et les stratégies appliquées.</span><span class="sxs-lookup"><span data-stu-id="fd096-191">When the label is applied, and users browse to the site, they see the name of the label and applied policies.</span></span> <span data-ttu-id="fd096-192">Par exemple, ce site est étiqueté comme **confidentiel** et le paramètre de confidentialité est défini sur **privé** :</span><span class="sxs-lookup"><span data-stu-id="fd096-192">For example, this site has been labeled as **Confidential**, and the privacy setting is set to **Private**:</span></span>

![Un site avec une étiquette de confidentialité appliquée](../media/sensitivity-label-site.png)

## <a name="view-sensitivity-labels-in-the-sharepoint-admin-center"></a><span data-ttu-id="fd096-194">Afficher des étiquettes de confidentialité dans le Centre d'administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="fd096-194">View sensitivity labels in the SharePoint admin center</span></span>

<span data-ttu-id="fd096-195">Pour afficher les étiquettes de confidentialité appliquées, utilisez la page **Sites actifs** dans le nouveau Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fd096-195">To view the applied sensitivity labels, use the **Active sites** page in the new SharePoint admin center.</span></span> <span data-ttu-id="fd096-196">Il se peut que vous deviez tout d'abord ajouter la colonne de **Confidentialité** :</span><span class="sxs-lookup"><span data-stu-id="fd096-196">You might need to first add the **Sensitivity** column:</span></span>

![Colonne Confidentialité de la page Sites actifs](../media/manage-site-sensitivity-labels.png)

<span data-ttu-id="fd096-198">[EN savoir plus sur la gestion des sites dans le nouveau Centre d’administration SharePoint](/sharepoint/manage-sites-in-new-admin-center).</span><span class="sxs-lookup"><span data-stu-id="fd096-198">[Learn more about managing sites in the new SharePoint admin center](/sharepoint/manage-sites-in-new-admin-center).</span></span>

## <a name="change-site-and-group-settings-for-a-label"></a><span data-ttu-id="fd096-199">Modifier les paramètres de site et de groupe pour une étiquette</span><span class="sxs-lookup"><span data-stu-id="fd096-199">Change site and group settings for a label</span></span>

<span data-ttu-id="fd096-200">Lorsque vous apportez des modifications aux paramètres de site et de groupe pour une étiquette, vous devez exécuter les commandes PowerShell suivantes pour que vos équipes, sites et groupes puissent employer les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="fd096-200">Whenever you make a change to site and group settings for a label, you must run the following PowerShell commands so that your teams, sites, and groups can use the new settings.</span></span> <span data-ttu-id="fd096-201">Nous vous conseillons de ne pas modifier les paramètres de site et de groupe pour une étiquette une fois que vous avez appliqué l'étiquette à plusieurs équipes, groupes ou sites.</span><span class="sxs-lookup"><span data-stu-id="fd096-201">As a best practice, don't the change site and group settings for a label after you've applied the label to several teams, groups, or sites.</span></span>

1. <span data-ttu-id="fd096-202">Dans une session PowerShell que vous ouvrez à l’aide de l’option **Exécuter en tant qu’Administrateur**, exécutez les commandes suivantes pour vous connecter au Centre de sécurité et conformité Office 365 PowerShell et obtenir la liste des étiquettes de confidentialité et leurs GUID.</span><span class="sxs-lookup"><span data-stu-id="fd096-202">In a PowerShell session that you open with the **Run as Administrator** option, run the following commands to connect to Office 365 Security & Compliance Center PowerShell and get the list of sensitivity labels and their GUIDs.</span></span>
    
    ```powershell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid
    ```

2. <span data-ttu-id="fd096-203">Notez le GUID de l’étiquette ou des étiquettes que vous avez modifiées.</span><span class="sxs-lookup"><span data-stu-id="fd096-203">Make a note of the GUID for the label or labels you have changed.</span></span>

3. <span data-ttu-id="fd096-204">Connectez-vous à Exchange Online PowerShell et exécutez l’applet de commande Get-UnifiedGroup, en indiquant votre GUID d’étiquette à la place du GUID d’exemple de « e48058ea-98e8-4940-8db0-ba1310fd955e » :</span><span class="sxs-lookup"><span data-stu-id="fd096-204">Now connect to Exchange Online PowerShell and run the Get-UnifiedGroup cmdlet, specifying your label GUID in place of the example GUID of "e48058ea-98e8-4940-8db0-ba1310fd955e":</span></span> 
    
    ```powershell
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session
    $Groups= Get-UnifiedGroup | Where {$_.SensitivityLabel  -eq "e48058ea-98e8-4940-8db0-ba1310fd955e"}
    ```

4. <span data-ttu-id="fd096-205">Réappliquez l’étiquette de confidentialité pour chaque groupe, en spécifiant le GUID de votre étiquette à la place du GUID de l’exemple de « e48058ea-98e8-4940-8db0-ba1310fd955e » :</span><span class="sxs-lookup"><span data-stu-id="fd096-205">For each group, reapply the sensitivity label, specifying your label GUID in place of the example GUID of "e48058ea-98e8-4940-8db0-ba1310fd955e":</span></span>
    
    ```powershell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "e48058ea-98e8-4940-8db0-ba1310fd955e"}
    ```

## <a name="support-for-the-sensitivity-labels"></a><span data-ttu-id="fd096-206">Prise en charge des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-206">Support for the sensitivity labels</span></span>

<span data-ttu-id="fd096-207">Vous pouvez utiliser les étiquettes de confidentialité que vous avez configurées pour les paramètres de sites et de groupes avec les applications et services suivants :</span><span class="sxs-lookup"><span data-stu-id="fd096-207">You can use the sensitivity labels that you've configured for site and group settings with the following apps and services:</span></span>

- <span data-ttu-id="fd096-208">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fd096-208">SharePoint Online</span></span>
- <span data-ttu-id="fd096-209">Équipes</span><span class="sxs-lookup"><span data-stu-id="fd096-209">Teams</span></span>
- <span data-ttu-id="fd096-210">Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="fd096-210">Outlook on the web</span></span>
- <span data-ttu-id="fd096-211">Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="fd096-211">SharePoint admin center</span></span>
- <span data-ttu-id="fd096-212">Centre d’administration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="fd096-212">Azure AD admin center</span></span>

<span data-ttu-id="fd096-213">Les autres services et applications dans lesquels vous ne pouvez pas à ce jour utiliser les étiquettes de confidentialité configurées pour des paramètres de sites et de groupes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fd096-213">Other apps and services that you can't currently use the sensitivity labels that you've configured for site and group settings include:</span></span>

- <span data-ttu-id="fd096-214">Outlook pour Mac</span><span class="sxs-lookup"><span data-stu-id="fd096-214">Outlook for the Mac</span></span>
- <span data-ttu-id="fd096-215">Outlook Mobile</span><span class="sxs-lookup"><span data-stu-id="fd096-215">Outlook mobile</span></span>
- <span data-ttu-id="fd096-216">Version de bureau d’Outlook pour Windows</span><span class="sxs-lookup"><span data-stu-id="fd096-216">Outlook desktop for Windows</span></span>
- <span data-ttu-id="fd096-217">Formulaires</span><span class="sxs-lookup"><span data-stu-id="fd096-217">Forms</span></span>
- <span data-ttu-id="fd096-218">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fd096-218">Dynamics 365</span></span>
- <span data-ttu-id="fd096-219">Yammer</span><span class="sxs-lookup"><span data-stu-id="fd096-219">Yammer</span></span>
- <span data-ttu-id="fd096-220">Flux</span><span class="sxs-lookup"><span data-stu-id="fd096-220">Stream</span></span>
- <span data-ttu-id="fd096-221">Planificateur</span><span class="sxs-lookup"><span data-stu-id="fd096-221">Planner</span></span>
- <span data-ttu-id="fd096-222">Project</span><span class="sxs-lookup"><span data-stu-id="fd096-222">Project</span></span>
- <span data-ttu-id="fd096-223">PowerBI</span><span class="sxs-lookup"><span data-stu-id="fd096-223">PowerBI</span></span>
- <span data-ttu-id="fd096-224">Centre d’administration Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="fd096-224">Teams admin center</span></span>
- <span data-ttu-id="fd096-225">Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fd096-225">Microsoft 365 admin center</span></span>
- <span data-ttu-id="fd096-226">Centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="fd096-226">Exchange admin center</span></span>


## <a name="classic-azure-ad-site-classification"></a><span data-ttu-id="fd096-227">Classification classique de sites Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd096-227">Classic Azure AD site classification</span></span>

<span data-ttu-id="fd096-228">Office 365 ne prend plus en charge les anciennes classifications pour les nouveaux groupes et les sites SharePoint lorsque vous activez cette préversion.</span><span class="sxs-lookup"><span data-stu-id="fd096-228">Office 365 no longer supports the old classifications for new groups and SharePoint sites when you enable this preview.</span></span> <span data-ttu-id="fd096-229">Toutefois, les groupes et sites existants affichent encore les anciennes classifications, sauf si vous les convertissez pour utiliser des étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="fd096-229">However, existing groups and sites still display the old classifications unless you convert them to use sensitivity labels.</span></span> <span data-ttu-id="fd096-230">Les anciennes classifications incluent la classification de sites « moderne » que vous avez configurée, par l’intermédiaire d’Azure AD PowerShell ou de la bibliothèque principale PnP, qui a défini des valeurs pour le paramètre `ClassificationList`.</span><span class="sxs-lookup"><span data-stu-id="fd096-230">Old classifications include the "modern" sites classification you set up, possibly through Azure AD PowerShell or the PnP Core library, that defined values for the `ClassificationList` setting.</span></span>

<span data-ttu-id="fd096-231">Par exemple, dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="fd096-231">For example, in PowerShell:</span></span>

```powershell
   ($setting["ClassificationList"])
```

<span data-ttu-id="fd096-232">Pour plus d’informations sur l’ancienne méthode de classification, consultez [Classification des sites SharePoint « modernes »](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span><span class="sxs-lookup"><span data-stu-id="fd096-232">For more information about the old classification method, see [SharePoint "modern" sites classification](https://docs.microsoft.com/sharepoint/dev/solution-guidance/modern-experience-site-classification).</span></span>

<span data-ttu-id="fd096-233">Pour convertir vos anciennes classifications en étiquettes de confidentialité, réalisez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd096-233">To convert your old classifications to sensitivity labels, do one of the following:</span></span>

- <span data-ttu-id="fd096-234">Utiliser des étiquettes existantes : spécifiez les paramètres d’étiquette souhaités pour des sites et des groupes en modifiant les étiquettes de confidentialité de diffusion existantes déjà publiées.</span><span class="sxs-lookup"><span data-stu-id="fd096-234">Use existing labels: Specify the label settings you want for sites and groups by editing existing sensitivity labels that are already published.</span></span>

- <span data-ttu-id="fd096-235">Créer des étiquettes : spécifiez les paramètres d’étiquette souhaités pour des sites et des groupes en créant et en publiant des étiquettes de confidentialité portant les mêmes noms que vos classifications existantes.</span><span class="sxs-lookup"><span data-stu-id="fd096-235">Create new labels: Specify the label settings you want for sites and groups by creating and publishing new sensitivity labels that have the same names as your existing classifications.</span></span>

<span data-ttu-id="fd096-236">Ensuite :</span><span class="sxs-lookup"><span data-stu-id="fd096-236">Then:</span></span> 

1. <span data-ttu-id="fd096-237">Utilisez PowerShell pour appliquer les étiquettes de confidentialité aux groupes et sites SharePoint Office 365 existants à l’aide du mappage de noms.</span><span class="sxs-lookup"><span data-stu-id="fd096-237">Use PowerShell to apply the sensitivity labels to existing Office 365 groups and SharePoint sites by using name mapping.</span></span> <span data-ttu-id="fd096-238">Pour connaître les instructions, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="fd096-238">See the next section for instructions.</span></span>

2. <span data-ttu-id="fd096-239">Supprimez les anciennes classifications dans les groupes et sites existants.</span><span class="sxs-lookup"><span data-stu-id="fd096-239">Remove the old classifications from the existing groups and sites.</span></span>

<span data-ttu-id="fd096-240">Bien que vous ne puissiez pas empêcher les utilisateurs de créer des groupes dans les applications et les services qui ne prennent pas encore en charge les étiquettes de confidentialité, vous pouvez exécuter un script PowerShell récurrent recherchant les nouveaux groupes créés par des utilisateurs à l'aide des anciennes classifications et les convertir pour utiliser des étiquettes de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="fd096-240">Although you can't prevent users from creating new groups in apps and services that don't yet support sensitivity labels, you can run a recurring PowerShell script to look for new groups that users have created with the old classifications, and convert these to use sensitivity labels.</span></span> 

#### <a name="use-powershell-to-convert-classifications-for-office-365-groups-to-sensitivity-labels"></a><span data-ttu-id="fd096-241">Utilisez PowerShell pour convertir des classifications de groupes Office 365 en étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-241">Use PowerShell to convert classifications for Office 365 groups to sensitivity labels</span></span>

1. <span data-ttu-id="fd096-242">Assurez-vous que vous exécutez la version de SharePoint Online Management Shell 16.0.19418.12000 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fd096-242">Ensure that you're running SharePoint Online Management Shell version 16.0.19418.12000 or above.</span></span> <span data-ttu-id="fd096-243">Si vous disposez déjà de la dernière version, passez à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="fd096-243">If you already have the latest version, skip to step 4.</span></span>

2. <span data-ttu-id="fd096-244">Si vous avez installé une version antérieure de SharePoint Online Management Shell à partir de la Galerie PowerShell, vous pouvez mettre à jour le module en exécutant l’applet de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fd096-244">If you have installed a previous version of the SharePoint Online Management Shell from PowerShell gallery, you can update the module by running the following cmdlet.</span></span>
    
    ```PowerShell
    Update-Module -Name Microsoft.Online.SharePoint.PowerShell
    ```

3. <span data-ttu-id="fd096-245">Si vous avez installé une version antérieure de SharePoint Online Management Shell à partir du Centre de téléchargement Microsoft, accédez à **Ajouter ou supprimer des programmes** et désinstaller SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="fd096-245">If you have installed a previous version of the SharePoint Online Management Shell from the Microsoft Download Center, go to **Add or remove programs** and uninstall the SharePoint Online Management Shell.</span></span> <span data-ttu-id="fd096-246">Installez ensuite la dernière version SharePoint Online Management Shell à partir du [Centre de téléchargement](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="fd096-246">Then, install the latest SharePoint Online Management Shell from the [Download Center](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

4. <span data-ttu-id="fd096-247">À l’aide d’un compte professionnel ou scolaire avec des privilèges d’administrateur général ou d’administrateur SharePoint dans Office 365, connectez-vous à SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="fd096-247">Using a work or school account that has global administrator or SharePoint admin privileges in Office 365, connect to SharePoint Online Management Shell.</span></span> <span data-ttu-id="fd096-248">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="fd096-248">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

5. <span data-ttu-id="fd096-249">Exécutez les commandes suivantes pour obtenir la liste des étiquettes de confidentialité et leurs GUID.</span><span class="sxs-lookup"><span data-stu-id="fd096-249">Run the following commands to get the list of sensitivity labels and their GUIDs.</span></span>

    ```PowerShell
    Set-ExecutionPolicy RemoteSigned
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Authentication Basic -AllowRedirection -Credential $UserCredential
    Import-PSSession $Session
    Get-Label |ft Name, Guid  
    ```

6. <span data-ttu-id="fd096-250">Notez les GUID des étiquettes de confidentialité que vous voulez appliquer à vos groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd096-250">Make a note of the GUIDs for the sensitivity labels you want to apply to your Office 365 groups.</span></span>

7. <span data-ttu-id="fd096-251">Utilisez la commande suivante en tant qu'exemple pour obtenir la liste des groupes qui ont actuellement la classification « Général » :</span><span class="sxs-lookup"><span data-stu-id="fd096-251">Use the following command as an example to get the list of groups that currently have the classification of "General":</span></span>

   ```PowerShell
   $Groups= Get-UnifiedGroup | Where {$_.classification -eq "General"}
   ```

6. <span data-ttu-id="fd096-252">Pour chaque groupe, ajoutez le nouveau GUID de l’étiquette de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="fd096-252">For each group, add the new sensitivity label GUID.</span></span> <span data-ttu-id="fd096-253">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fd096-253">For example:</span></span>

    ```PowerShell
    foreach ($g in $groups)
    {Set-UnifiedGroup -Identity $g.Identity -SensitivityLabelId "457fa763-7c59-461c-b402-ad1ac6b703cc"}
    ```

## <a name="auditing-sensitivity-label-activities"></a><span data-ttu-id="fd096-254">Audit sur les activités des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-254">Auditing sensitivity label activities</span></span>

<span data-ttu-id="fd096-255">Si un utilisateur télécharge un document sur un site protégé par une étiquette de confidentialité et son document comporte une étiquette de confidentialité [plus élevée](sensitivity-labels.md#label-priority-order-matters) que celle du site, cette action n'est pas bloquée.</span><span class="sxs-lookup"><span data-stu-id="fd096-255">If somebody uploads a document to a site that's protected with a sensitivity label and their document has a [higher priority](sensitivity-labels.md#label-priority-order-matters) sensitivity label than the sensitivity label applied to the site, this action isn't blocked.</span></span> <span data-ttu-id="fd096-256">Par exemple, vous avez appliqué l'étiquette **Général** à un site SharePoint, et une personne télécharge un document étiqueté comme **Confidentiel**.</span><span class="sxs-lookup"><span data-stu-id="fd096-256">For example, you've applied the **General** label to a SharePoint site, and somebody uploads to this site a document labeled **Confidential**.</span></span> <span data-ttu-id="fd096-257">Une étiquette de confidentialité ayant une priorité plus élevée identifie un contenu plus sensible qu'un contenu présentant un ordre de priorité plus faible, cette situation peut devenir un problème de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fd096-257">Because a sensitivity label with a higher priority identifies content that is more sensitivity than content that has a lower priority order, this situation could be a security concern.</span></span>

<span data-ttu-id="fd096-258">Bien que l’action ne soit pas bloquée, elle est auditée pour vous permettre d'identifier les documents comportant un mauvais alignement de la priorité d’étiquette et prendre des mesures, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fd096-258">Although the action isn't blocked, it is audited, so you can identify documents that have this misalignment of label priority and take action if needed.</span></span> <span data-ttu-id="fd096-259">Par exemple, supprimer ou déplacer le document téléchargé à partir du site.</span><span class="sxs-lookup"><span data-stu-id="fd096-259">For example, delete or move the uploaded document from the site.</span></span> 

<span data-ttu-id="fd096-260">Il ne s'agit pas d'un problème de sécurité si le document comprend une étiquette de confidentialité de priorité inférieure à celle appliquée sur le site.</span><span class="sxs-lookup"><span data-stu-id="fd096-260">It wouldn't be a security concern if the document has a lower priority sensitivity label than the sensitivity label applied to the site.</span></span> <span data-ttu-id="fd096-261">Par exemple, un document marqué **Général** est téléchargé sur un site intitulé **Confidentiel**.</span><span class="sxs-lookup"><span data-stu-id="fd096-261">For example, a document labeled **General** is uploaded to a site labeled **Confidential**.</span></span> <span data-ttu-id="fd096-262">Dans ce scénario, l'événement d’audit n’est pas généré.</span><span class="sxs-lookup"><span data-stu-id="fd096-262">In this scenario, an auditing event isn't generated.</span></span>

<span data-ttu-id="fd096-263">Pour rechercher le journal d’audit pour cet événement, recherchez **Correspondance incorrecte des documents détectés** dans la catégorie **Activités de fichiers et de pages**.</span><span class="sxs-lookup"><span data-stu-id="fd096-263">To search the audit log for this event, look for **Detected document sensitivity mismatch** from the **File and page activities** category.</span></span> 

<span data-ttu-id="fd096-264">Lorsque quelqu’une personne ajoute ou supprime une étiquette de sensibilité sur ou à partir d’un site ou d’un groupe, ces activités sont également auditées.</span><span class="sxs-lookup"><span data-stu-id="fd096-264">When somebody adds or removes a sensitivity label to or from a site or group, these activities are also audited.</span></span> <span data-ttu-id="fd096-265">Vous pouvez consulter ces événements dans la catégorie [Activités des d’étiquette de confidentialité](search-the-audit-log-in-security-and-compliance.md#sensitivity-label-activities).</span><span class="sxs-lookup"><span data-stu-id="fd096-265">These events can be found in the [Sensitivity label activities](search-the-audit-log-in-security-and-compliance.md#sensitivity-label-activities) category.</span></span> 

<span data-ttu-id="fd096-266">Pour obtenir des instructions sur les recherches dans un journal d’audit, consultez [Effectuer des recherches dans le journal d’audit du Centre de sécurité et conformité](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="fd096-266">For instructions to search the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>

## <a name="troubleshoot-sensitivity-label-deployment"></a><span data-ttu-id="fd096-267">Résoudre les problèmes de déploiement des étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="fd096-267">Troubleshoot sensitivity label deployment</span></span>

<span data-ttu-id="fd096-268">Vous avez des problèmes avec des étiquettes de confidentialité pour Microsoft Teams, les groupes Office 365 et les sites SharePoint ?</span><span class="sxs-lookup"><span data-stu-id="fd096-268">Having problems with sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites?</span></span> <span data-ttu-id="fd096-269">Vérifiez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fd096-269">Check the following:</span></span>

### <a name="labels-not-visible-after-publishing"></a><span data-ttu-id="fd096-270">Étiquettes non visibles après la publication</span><span class="sxs-lookup"><span data-stu-id="fd096-270">Labels not visible after publishing</span></span>
<span data-ttu-id="fd096-271">Si vous rencontrez des problèmes lors de la création d’un site ou d’un groupe Office 365 après avoir activé ces paramètres ou modifié la description de l’étiquette de confidentialité, patientez quelques heures après avoir enregistré les modifications, puis essayez à nouveau de créer l’équipe ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="fd096-271">If you experience issues when you create a site or Office 365 group after you enable these settings or modify a sensitivity label's name or tooltip, wait a few hours after saving the label changes, and then try to create the team or group again.</span></span> <span data-ttu-id="fd096-272">Si vous souhaitez en savoir plus, consultez [Planifier le déploiement après avoir créé ou modifié une étiquette de confidentialité](sensitivity-labels-sharepoint-onedrive-files.md#schedule-roll-out-after-you-create-or-change-a-sensitivity-label).</span><span class="sxs-lookup"><span data-stu-id="fd096-272">For information, see [Schedule roll-out after you create or change a sensitivity label](sensitivity-labels-sharepoint-onedrive-files.md#schedule-roll-out-after-you-create-or-change-a-sensitivity-label).</span></span>

<span data-ttu-id="fd096-273">Si vous ne parvenez toujours pas à voir la nouvelle étiquette de confidentialité depuis SharePoint Online, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="fd096-273">If you still can't see the new sensitivity label from SharePoint Online, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

### <a name="team-group-or-sharepoint-site-creation-errors"></a><span data-ttu-id="fd096-274">Erreurs de création d'équipe, de groupe ou de site SharePoint</span><span class="sxs-lookup"><span data-stu-id="fd096-274">Team, group, or SharePoint site creation errors</span></span>
<span data-ttu-id="fd096-275">Si vous rencontrez des erreurs de création lors de préversion publique, vous pouvez désactiver les étiquettes de confidentialité pour les Microsoft Teams, les groupes Office 365 et les sites SharePoint en utilisant les instructions suivante : [Activer la prise en charge des étiquettes de confidentialité dans PowerShell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#enable-sensitivity-label-support-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="fd096-275">If you experience creation errors during the public preview, you can turn off sensitivity labels for Microsoft Teams, Office 365 groups, and SharePoint sites by using the same instructions from [Enable sensitivity label support in PowerShell](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-assign-sensitivity-labels#enable-sensitivity-label-support-in-powershell).</span></span> <span data-ttu-id="fd096-276">Toutefois, pour désactiver la préversion, à l’étape 5, désactivez la fonctionnalité à l’aide de `$setting["EnableMIPLabels"] = "False"`.</span><span class="sxs-lookup"><span data-stu-id="fd096-276">However, to disable the preview, in step 5, disable the feature by using `$setting["EnableMIPLabels"] = "False"`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd096-277">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fd096-277">Additional resources</span></span>

<span data-ttu-id="fd096-278">Regardez l’enregistrement du webinaire et les questions traitées pour [Utilisation d’étiquettes de confidentialité avec Microsoft Teams, les groupes Office 365 et les sites SharePoint Online](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/using-sensitivity-labels-with-microsoft-teams-o365-groups-and/ba-p/1221885#M1380).</span><span class="sxs-lookup"><span data-stu-id="fd096-278">See the webinar recording and answered questions for [Using Sensitivity labels with Microsoft Teams, O365 Groups and SharePoint Online sites](https://techcommunity.microsoft.com/t5/security-privacy-and-compliance/using-sensitivity-labels-with-microsoft-teams-o365-groups-and/ba-p/1221885#M1380).</span></span>

