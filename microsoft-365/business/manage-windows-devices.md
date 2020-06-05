---
title: Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 pour les entreprises
f1.keywords:
- CSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
description: Découvrez comment permettre à Microsoft 365 de protéger les appareils Windows 10 à annuaire Active Directory joints en quelques étapes seulement.
ms.openlocfilehash: 857651081fb10856d28dd419333ebef655388407
ms.sourcegitcommit: e6e704cbd9a50fc7db1e6a0cf5d3f8c6cbb94363
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2020
ms.locfileid: "44564934"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business-premium"></a><span data-ttu-id="e740e-103">Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="e740e-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium</span></span>

<span data-ttu-id="e740e-104">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 Business Premium pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="e740e-104">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business Premium to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span>
<span data-ttu-id="e740e-105">Pour configurer cette protection, vous pouvez implémenter des **appareils joints Azure ad hybrides**.</span><span class="sxs-lookup"><span data-stu-id="e740e-105">To set up this protection, you can implement **Hybrid Azure AD joined devices**.</span></span> <span data-ttu-id="e740e-106">Ces appareils sont joints à votre annuaire Active Directory local et à votre Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e740e-106">These devices are joined to both your on-premises Active Directory and your Azure Active Directory.</span></span>

<span data-ttu-id="e740e-107">Cette vidéo décrit la procédure à suivre pour le scénario le plus courant, qui est également détaillée dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e740e-107">This video describes the steps for how to set this up for the most common scenario, which is also detailed in the steps that follow.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3C9hO]
  

## <a name="before-you-get-started-make-sure-you-complete-these-steps"></a><span data-ttu-id="e740e-108">Avant de commencer, veillez à effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e740e-108">Before you get started, make sure you complete these steps:</span></span>
- <span data-ttu-id="e740e-109">Synchroniser les utilisateurs vers Azure AD avec Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="e740e-109">Synchronize users to Azure AD with Azure AD Connect.</span></span>
- <span data-ttu-id="e740e-110">Exécutez la synchronisation des unités d’organisation Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="e740e-110">Complete Azure AD Connect Organizational Unit (OU) sync.</span></span>
- <span data-ttu-id="e740e-111">Assurez-vous que tous les utilisateurs du domaine que vous synchronisez disposent de licences pour Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="e740e-111">Make sure all the domain users you sync have licenses to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="e740e-112">Pour plus d’informations, consultez la rubrique [synchroniser les utilisateurs de domaine à Microsoft](manage-domain-users.md) .</span><span class="sxs-lookup"><span data-stu-id="e740e-112">See [Synchronize domain users to Microsoft](manage-domain-users.md) for the steps.</span></span>

## <a name="1-verify-mdm-authority-in-intune"></a><span data-ttu-id="e740e-113">1. vérifier l’autorité MDM dans Intune</span><span class="sxs-lookup"><span data-stu-id="e740e-113">1. Verify MDM Authority in Intune</span></span>

<span data-ttu-id="e740e-114">Accédez à portal.azure.com et dans la partie supérieure de la page recherche de Intune.</span><span class="sxs-lookup"><span data-stu-id="e740e-114">Go to portal.azure.com and on the top of the page search for Intune.</span></span>
<span data-ttu-id="e740e-115">Sur la page Microsoft Intune, sélectionnez l’option d’enregistrement de l' **appareil** et, dans la page de **vue d’ensemble** , vérifiez que l' **autorité MDM** est **Intune**.</span><span class="sxs-lookup"><span data-stu-id="e740e-115">On the Microsoft Intune page, select **Device enrollment** and on the **Overview** page make sure **MDM authority** is **Intune**.</span></span>

- <span data-ttu-id="e740e-116">Si l' **autorité MDM** est **None**, cliquez sur l' **autorité MDM** pour la définir sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="e740e-116">If **MDM authority** is **None**, click the **MDM authority** to set it to **Intune**.</span></span>
- <span data-ttu-id="e740e-117">Si l' **autorité MDM** est **Microsoft Office 365**, accédez **à périphériques**d'  >  **inscription** des appareils et utilisez la boîte de dialogue Ajouter une **autorité** MDM sur la droite pour ajouter l’autorité **MDM MDM** (la boîte de dialogue **Ajouter une autorité** MDM est uniquement disponible si l' **autorité MDM** est définie sur Microsoft Office 365).</span><span class="sxs-lookup"><span data-stu-id="e740e-117">If **MDM authority** is **Microsoft Office 365**,go to **Devices** > **Enroll devices** and use the **Add MDM authority** dialog on the right to add **Intune MDM** authority (the **Add MDM Authority** dialog is only available if the **MDM Authority** is set to Microsoft Office 365).</span></span>

## <a name="2-verify-azure-ad-is-enabled-for-joining-computers"></a><span data-ttu-id="e740e-118">2. Vérifiez que Azure AD est activé pour la jonction d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="e740e-118">2. Verify Azure AD is enabled for joining computers</span></span>

- <span data-ttu-id="e740e-119">Accédez au centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> et sélectionnez **Azure Active Directory** (sélectionnez Afficher tout si Azure Active Directory n’est pas visible) dans la liste **centres d’administration** .</span><span class="sxs-lookup"><span data-stu-id="e740e-119">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select **Azure Active Directory** (select Show all if Azure Active Directory is not visible) in the **Admin centers** list.</span></span> 
- <span data-ttu-id="e740e-120">Dans le **Centre d’administration Azure Active Directory**, accédez à **Azure Active Directory** , sélectionnez **périphériques** , puis paramètres de l' **appareil**.</span><span class="sxs-lookup"><span data-stu-id="e740e-120">In the **Azure Active Directory admin center**, go to **Azure Active Directory** , choose **Devices** and then **Device settings**.</span></span>
- <span data-ttu-id="e740e-121">Vérifier que**les utilisateurs peuvent joindre des appareils à Azure ad** est activé</span><span class="sxs-lookup"><span data-stu-id="e740e-121">Verify**Users may join devices to Azure AD** is enabled</span></span> 
    1. <span data-ttu-id="e740e-122">Pour activer tous les utilisateurs, définissez sur **tous**.</span><span class="sxs-lookup"><span data-stu-id="e740e-122">To enable all users, set to **All**.</span></span>
    2. <span data-ttu-id="e740e-123">Pour activer des utilisateurs spécifiques, définissez sur **sélectionné** pour activer un groupe spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e740e-123">To enable specific users, set to **Selected** to enable a specific group of users.</span></span>
        - <span data-ttu-id="e740e-124">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure Active Directory à un [groupe de sécurité](../admin/create-groups/create-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e740e-124">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        - <span data-ttu-id="e740e-125">Sélectionnez **Sélectionner les groupes** pour activer l’étendue utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e740e-125">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="3-verify-azure-ad-is-enabled-for-mdm"></a><span data-ttu-id="e740e-126">3. Vérifiez que Azure AD est activé pour MDM</span><span class="sxs-lookup"><span data-stu-id="e740e-126">3. Verify Azure AD is enabled for MDM</span></span>

- <span data-ttu-id="e740e-127">Accédez au centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> et sélectionnez Sélectionner le **point de terminaison Manager**t (sélectionnez **Afficher tout** si le **Gestionnaire de point de terminaison** n’est pas visible).</span><span class="sxs-lookup"><span data-stu-id="e740e-127">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select select **Endpoint Managemen**t (select **Show all** if **Endpoint Manager** is not visible)</span></span>
- <span data-ttu-id="e740e-128">Dans le **Centre d’administration du gestionnaire de points de terminaison Microsoft**, accédez à **périphériques**  >  **Windows**  >  **Windows inscriptions**  >  **automatiques**.</span><span class="sxs-lookup"><span data-stu-id="e740e-128">In the **Microsoft Endpoint Manager admin center**, go to **Devices** > **Windows** > **Windows Enrollment** > **Automatic Enrollment**.</span></span>
- <span data-ttu-id="e740e-129">Vérifiez que l’étendue utilisateur MDM est activée.</span><span class="sxs-lookup"><span data-stu-id="e740e-129">Verify MDM user scope is enabled.</span></span>

    1. <span data-ttu-id="e740e-130">Pour inscrire tous les ordinateurs, définissez sur **tous** pour inscrire automatiquement tous les ordinateurs des utilisateurs qui sont joints à Azure ad et les nouveaux ordinateurs lorsque les utilisateurs ajoutent un compte professionnel à Windows.</span><span class="sxs-lookup"><span data-stu-id="e740e-130">To enroll all computers, set to **All** to automatically enroll all user computers that are joined to Azure AD and new computers  when the users add a work account to Windows.</span></span>
    2. <span data-ttu-id="e740e-131">Définissez sur **some** pour inscrire les ordinateurs d’un groupe d’utilisateurs spécifique.</span><span class="sxs-lookup"><span data-stu-id="e740e-131">Set to **Some** to enroll the computers of a specific group of users.</span></span>
        -  <span data-ttu-id="e740e-132">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure Active Directory à un [groupe de sécurité](../admin/create-groups/create-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e740e-132">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        -  <span data-ttu-id="e740e-133">Sélectionnez **Sélectionner les groupes** pour activer l’étendue utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e740e-133">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="4-set-up-service-connection-point-scp"></a><span data-ttu-id="e740e-134">4. configurer le point de connexion de service (SCP)</span><span class="sxs-lookup"><span data-stu-id="e740e-134">4. Set up Service connection point (SCP)</span></span>

<span data-ttu-id="e740e-135">Ces étapes sont simplifiées à partir de la configuration de la [jointure Azure ad hybride](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join).</span><span class="sxs-lookup"><span data-stu-id="e740e-135">These steps are simplified from [configure hybrid azure AD join](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join).</span></span> <span data-ttu-id="e740e-136">Pour effectuer les étapes, vous devez utiliser Azure AD Connect et vos mots de passe d’administrateur global Microsoft 365 Business Premium et d’administrateur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e740e-136">To complete the steps you need to use Azure AD Connect and your Microsoft 365 Business Premium global admin and Active Directory admin passwords.</span></span>

1.  <span data-ttu-id="e740e-137">Démarrez Azure AD Connect, puis sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="e740e-137">Start Azure AD Connect, and then select **Configure**.</span></span>
2.  <span data-ttu-id="e740e-138">Sur la page **tâches supplémentaires** , sélectionnez **configurer les options des appareils**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e740e-138">On the **Additional tasks**  page, select **Configure device options**, and then select **Next**.</span></span>
3.  <span data-ttu-id="e740e-139">Sur la page **vue d’ensemble** , sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e740e-139">On the **Overview** page, select **Next**.</span></span>
4.  <span data-ttu-id="e740e-140">Sur la page **connexion à Azure ad** , entrez les informations d’identification d’un administrateur général pour Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="e740e-140">On the **Connect to Azure AD** page, enter the credentials of a global administrator for Microsoft 365 Business Premium.</span></span>
5.  <span data-ttu-id="e740e-141">Sur la page **options d’appareil** , sélectionnez configurer une **jointure Azure ad hybride**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e740e-141">On the **Device options** page, select **Configure Hybrid Azure AD join**, and then select **Next**.</span></span>
6.  <span data-ttu-id="e740e-142">Sur la page **SCP** , pour chaque forêt dans laquelle vous souhaitez qu’Azure ad Connect configure le SCP, effectuez les étapes suivantes, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="e740e-142">On the **SCP** page, for each forest where you want Azure AD Connect to configure the SCP, complete the following steps, and then select **Next**:</span></span>
    - <span data-ttu-id="e740e-143">Activez la case à cocher en regard du nom de la forêt.</span><span class="sxs-lookup"><span data-stu-id="e740e-143">Check the box beside the forest name.</span></span> <span data-ttu-id="e740e-144">La forêt doit être le nom de votre domaine AD.</span><span class="sxs-lookup"><span data-stu-id="e740e-144">The forest should be your AD domain name.</span></span>
    - <span data-ttu-id="e740e-145">Dans la colonne **service d’authentification** , ouvrez la liste déroulante et sélectionnez nom de domaine correspondant (il ne doit y avoir qu’une seule option).</span><span class="sxs-lookup"><span data-stu-id="e740e-145">Under the **Authentication Service** column, open the dropdown and select matching domain name (there should only be one only option).</span></span>
    - <span data-ttu-id="e740e-146">Sélectionnez **Ajouter** pour entrer les informations d’identification d’administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="e740e-146">Select **Add** to enter the domain administrator credentials.</span></span>  
7.  <span data-ttu-id="e740e-147">Sur la page **système d’exploitation des appareils** , sélectionnez appareils joints à un domaine Windows 10 ou version ultérieure uniquement.</span><span class="sxs-lookup"><span data-stu-id="e740e-147">On the **Device operating systems** page, select Windows 10 or later domain-joined devices only.</span></span>
8.  <span data-ttu-id="e740e-148">Sur la page **prêt à configurer** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="e740e-148">On the **Ready to configure** page, select **Configure**.</span></span>
9.  <span data-ttu-id="e740e-149">Sur la page **Configuration terminée** , sélectionnez **quitter**.</span><span class="sxs-lookup"><span data-stu-id="e740e-149">On the **Configuration complete** page, select **Exit**.</span></span>


## <a name="5-create-a-gpo-for-intune-enrollment--admx-method"></a><span data-ttu-id="e740e-150">5. créer un objet de stratégie de groupe pour l’enregistrement Intune – ADMX, méthode</span><span class="sxs-lookup"><span data-stu-id="e740e-150">5. Create a GPO for Intune Enrollment – ADMX method</span></span>

<span data-ttu-id="e740e-151">Utilisant. Fichier de modèle ADMX.</span><span class="sxs-lookup"><span data-stu-id="e740e-151">Use .ADMX template file.</span></span>

1.  <span data-ttu-id="e740e-152">Connectez-vous à AD Server, recherchez et ouvrez les outils du **Gestionnaire de serveur**  >  **Tools**  >  **gestion des stratégies de groupe**.</span><span class="sxs-lookup"><span data-stu-id="e740e-152">Log on to AD server, search and open **Server Manager** > **Tools** > **Group Policy Management**.</span></span>
2.  <span data-ttu-id="e740e-153">Sélectionnez votre nom de domaine sous **domaines** , puis cliquez avec le bouton droit sur **objets de stratégie de groupe** pour sélectionner **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="e740e-153">Select your domain name under **Domains** and right-click **Group Policy Objects** to select **New**.</span></span>
3.  <span data-ttu-id="e740e-154">Donnez un nom au nouvel objet de stratégie de groupe, par exemple «*Cloud_Enrollment*», puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e740e-154">Give the new GPO an name, for example “*Cloud_Enrollment*” and then select **OK**.</span></span>
4.  <span data-ttu-id="e740e-155">Cliquez avec le bouton droit sur le nouvel objet GPO sous **objets de stratégie de groupe** et sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="e740e-155">Right-click the new GPO under **Group Policy Objects** and select **Edit**.</span></span>
5.  <span data-ttu-id="e740e-156">Dans l' **éditeur de gestion des stratégies de groupe**, accédez à stratégies de configuration de l' **ordinateur**  >  **Policies**  >  **modèles d’administration**  >  **Windows Components**  >  **MDM**.</span><span class="sxs-lookup"><span data-stu-id="e740e-156">In the **Group Policy Management Editor**, go to **Computer Configuration** > **Policies** > **Administrative Templates** > **Windows Components** > **MDM**.</span></span>
6. <span data-ttu-id="e740e-157">Cliquez avec le bouton droit sur **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut** , puis sélectionnez **activé**  >  **OK**.</span><span class="sxs-lookup"><span data-stu-id="e740e-157">Right-click **Enable automatic MDM enrollment using default Azure AD credentials** and then select **Enabled** > **OK**.</span></span> <span data-ttu-id="e740e-158">Fermez la fenêtre de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="e740e-158">Close the editor window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e740e-159">Si vous ne voyez pas la stratégie **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut**, reportez-vous à [la rubrique obtenir les derniers modèles d’administration](#get-the-latest-administrative-templates).</span><span class="sxs-lookup"><span data-stu-id="e740e-159">If you do not see the policy **Enable automatic MDM enrollment using default Azure AD credentials**, see [Get the latest Administrative Templates](#get-the-latest-administrative-templates).</span></span>

## <a name="6-deploy-the-group-policy"></a><span data-ttu-id="e740e-160">6. déployer la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e740e-160">6. Deploy the Group Policy</span></span>

1.  <span data-ttu-id="e740e-161">Dans le gestionnaire de serveur, sous **domaines** > objets de stratégie de groupe, sélectionnez l’objet GPO de l’étape 3 ci-dessus, par exemple « Cloud_Enrollment ».</span><span class="sxs-lookup"><span data-stu-id="e740e-161">In the Server Manager, under **Domains** > Group Policy objects, select the GPO from Step 3 above, for example “Cloud_Enrollment”.</span></span>
2.  <span data-ttu-id="e740e-162">Sélectionnez l’onglet **étendue** de votre objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e740e-162">Select the **Scope** tab for your GPO.</span></span>
3.  <span data-ttu-id="e740e-163">Dans l’onglet étendue de l’objet de stratégie de groupe, cliquez avec le bouton droit sur le lien vers le domaine sous **liens**.</span><span class="sxs-lookup"><span data-stu-id="e740e-163">In the GPO’s Scope tab, right-click the link to the domain under **Links**.</span></span>
4.  <span data-ttu-id="e740e-164">Sélectionnez **appliqué** pour déployer l’objet de stratégie de groupe, puis **OK** dans l’écran de confirmation.</span><span class="sxs-lookup"><span data-stu-id="e740e-164">Select **Enforced** to deploy the GPO and then **OK** in the confirmation screen.</span></span>

## <a name="get-the-latest-administrative-templates"></a><span data-ttu-id="e740e-165">Obtenir les derniers modèles d’administration</span><span class="sxs-lookup"><span data-stu-id="e740e-165">Get the latest Administrative Templates</span></span>

<span data-ttu-id="e740e-166">Si vous ne voyez pas la stratégie **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut**, il se peut que vous n’ayez pas installé ADMX pour Windows 10, version 1803, version 1809 ou version 1903.</span><span class="sxs-lookup"><span data-stu-id="e740e-166">If you do not see the policy **Enable automatic MDM enrollment using default Azure AD credentials**, it may be because you don’t have the ADMX installed for Windows 10, version 1803, version 1809, or version 1903.</span></span> <span data-ttu-id="e740e-167">Pour résoudre le problème, procédez comme suit (Remarque : la dernière version de MDM. admx est compatible avec les versions antérieures) :</span><span class="sxs-lookup"><span data-stu-id="e740e-167">To fix the issue, follow these steps (Note: the latest MDM.admx is backwards compatible):</span></span>

1.  <span data-ttu-id="e740e-168">Téléchargement : [modèles d’administration (. admx) pour Windows 10 mai 2019 mise à jour (1903)](https://www.microsoft.com/download/details.aspx?id=58495&WT.mc_id=rss_alldownloads_all).</span><span class="sxs-lookup"><span data-stu-id="e740e-168">Download: [Administrative Templates (.admx) for Windows 10 May 2019 Update (1903)](https://www.microsoft.com/download/details.aspx?id=58495&WT.mc_id=rss_alldownloads_all).</span></span>
2.  <span data-ttu-id="e740e-169">Installez le package sur le contrôleur de domaine principal (PDC).</span><span class="sxs-lookup"><span data-stu-id="e740e-169">Install the package on the Primary Domain Controller (PDC).</span></span>
3.  <span data-ttu-id="e740e-170">Naviguez en fonction de la version du dossier : **C:\Program Files (x86) \Microsoft Group Policy\Windows 10 mai 2019 mise à jour (1903) v3**.</span><span class="sxs-lookup"><span data-stu-id="e740e-170">Navigate, depending on the version to the folder: **C:\Program Files (x86)\Microsoft Group Policy\Windows 10 May 2019 Update (1903) v3**.</span></span>
4.  <span data-ttu-id="e740e-171">Renommez le dossier des **définitions de stratégie** dans le chemin d’accès ci-dessus en **PolicyDefinitions**.</span><span class="sxs-lookup"><span data-stu-id="e740e-171">Rename the **Policy Definitions** folder in the above path to **PolicyDefinitions**.</span></span>
5.  <span data-ttu-id="e740e-172">Copiez le dossier **PolicyDefinitions** dans **C:\Windows\SYSVOL\domain\Policies**.</span><span class="sxs-lookup"><span data-stu-id="e740e-172">Copy **PolicyDefinitions** folder to **C:\Windows\SYSVOL\domain\Policies**.</span></span> 
    -   <span data-ttu-id="e740e-173">Si vous envisagez d’utiliser un magasin de stratégies central pour l’ensemble de votre domaine, ajoutez le contenu de PolicyDefinitions.</span><span class="sxs-lookup"><span data-stu-id="e740e-173">If you plan to use a central policy store for your entire domain, add the contents of PolicyDefinitions there.</span></span>
6.  <span data-ttu-id="e740e-174">Redémarrez le contrôleur de domaine principal pour que la stratégie soit disponible.</span><span class="sxs-lookup"><span data-stu-id="e740e-174">Restart the Primary Domain Controller for the policy to be available.</span></span> <span data-ttu-id="e740e-175">Cette procédure fonctionnera également pour toute version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e740e-175">This procedure will work for any future version as well.</span></span>

<span data-ttu-id="e740e-176">À ce stade, vous devriez être en mesure d’afficher la stratégie **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut** disponibles.</span><span class="sxs-lookup"><span data-stu-id="e740e-176">At this point you should be able to see the policy **Enable automatic MDM enrollment using default Azure AD credentials** available.</span></span>

