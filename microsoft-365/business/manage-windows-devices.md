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
ms.openlocfilehash: 2eaf5aa76cae1680b93af008af615ae872e4fb20
ms.sourcegitcommit: fab425ea4580d1924fb421e6db233d135f5b7d19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2020
ms.locfileid: "46533782"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business-premium"></a><span data-ttu-id="7a119-103">Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="7a119-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium</span></span>

<span data-ttu-id="7a119-104">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 Business Premium pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="7a119-104">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business Premium to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span>
<span data-ttu-id="7a119-105">Pour configurer cette protection, vous pouvez implémenter des **appareils joints Azure ad hybrides**.</span><span class="sxs-lookup"><span data-stu-id="7a119-105">To set up this protection, you can implement **Hybrid Azure AD joined devices**.</span></span> <span data-ttu-id="7a119-106">Ces appareils sont joints à votre annuaire Active Directory local et à votre Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a119-106">These devices are joined to both your on-premises Active Directory and your Azure Active Directory.</span></span>

<span data-ttu-id="7a119-107">Cette vidéo décrit la procédure à suivre pour le scénario le plus courant, qui est également détaillée dans les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a119-107">This video describes the steps for how to set this up for the most common scenario, which is also detailed in the steps that follow.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3C9hO]
  

## <a name="before-you-get-started-make-sure-you-complete-these-steps"></a><span data-ttu-id="7a119-108">Avant de commencer, veillez à effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7a119-108">Before you get started, make sure you complete these steps:</span></span>
- <span data-ttu-id="7a119-109">Synchroniser les utilisateurs vers Azure AD avec Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="7a119-109">Synchronize users to Azure AD with Azure AD Connect.</span></span>
- <span data-ttu-id="7a119-110">Exécutez la synchronisation des unités d’organisation Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="7a119-110">Complete Azure AD Connect Organizational Unit (OU) sync.</span></span>
- <span data-ttu-id="7a119-111">Assurez-vous que tous les utilisateurs du domaine que vous synchronisez disposent de licences pour Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7a119-111">Make sure all the domain users you sync have licenses to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="7a119-112">Pour plus d’informations, consultez la rubrique [synchroniser les utilisateurs de domaine à Microsoft](manage-domain-users.md) .</span><span class="sxs-lookup"><span data-stu-id="7a119-112">See [Synchronize domain users to Microsoft](manage-domain-users.md) for the steps.</span></span>

## <a name="1-verify-mdm-authority-in-intune"></a><span data-ttu-id="7a119-113">1. vérifier l’autorité MDM dans Intune</span><span class="sxs-lookup"><span data-stu-id="7a119-113">1. Verify MDM Authority in Intune</span></span>

<span data-ttu-id="7a119-114">Accédez à portal.azure.com et dans la partie supérieure de la page recherche de Intune.</span><span class="sxs-lookup"><span data-stu-id="7a119-114">Go to portal.azure.com and on the top of the page search for Intune.</span></span>
<span data-ttu-id="7a119-115">Sur la page Microsoft Intune, sélectionnez l’option d’enregistrement de l' **appareil** et, dans la page de **vue d’ensemble** , vérifiez que l' **autorité MDM** est **Intune**.</span><span class="sxs-lookup"><span data-stu-id="7a119-115">On the Microsoft Intune page, select **Device enrollment** and on the **Overview** page make sure **MDM authority** is **Intune**.</span></span>

- <span data-ttu-id="7a119-116">Si l' **autorité MDM** est **None**, cliquez sur l' **autorité MDM** pour la définir sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="7a119-116">If **MDM authority** is **None**, click the **MDM authority** to set it to **Intune**.</span></span>
- <span data-ttu-id="7a119-117">Si l' **autorité MDM** est **Microsoft Office 365**, accédez **à périphériques**d'  >  **inscription** des appareils et utilisez la boîte de dialogue Ajouter une **autorité** MDM sur la droite pour ajouter l’autorité **MDM MDM** (la boîte de dialogue **Ajouter une autorité** MDM est uniquement disponible si l' **autorité MDM** est définie sur Microsoft Office 365).</span><span class="sxs-lookup"><span data-stu-id="7a119-117">If **MDM authority** is **Microsoft Office 365**,go to **Devices** > **Enroll devices** and use the **Add MDM authority** dialog on the right to add **Intune MDM** authority (the **Add MDM Authority** dialog is only available if the **MDM Authority** is set to Microsoft Office 365).</span></span>

## <a name="2-verify-azure-ad-is-enabled-for-joining-computers"></a><span data-ttu-id="7a119-118">2. Vérifiez que Azure AD est activé pour la jonction d’ordinateurs</span><span class="sxs-lookup"><span data-stu-id="7a119-118">2. Verify Azure AD is enabled for joining computers</span></span>

- <span data-ttu-id="7a119-119">Accédez au centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> et sélectionnez **Azure Active Directory** (sélectionnez Afficher tout si Azure Active Directory n’est pas visible) dans la liste **centres d’administration** .</span><span class="sxs-lookup"><span data-stu-id="7a119-119">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select **Azure Active Directory** (select Show all if Azure Active Directory is not visible) in the **Admin centers** list.</span></span> 
- <span data-ttu-id="7a119-120">Dans le **Centre d’administration Azure Active Directory**, accédez à **Azure Active Directory** , sélectionnez **périphériques** , puis paramètres de l' **appareil**.</span><span class="sxs-lookup"><span data-stu-id="7a119-120">In the **Azure Active Directory admin center**, go to **Azure Active Directory** , choose **Devices** and then **Device settings**.</span></span>
- <span data-ttu-id="7a119-121">Vérifier que**les utilisateurs peuvent joindre des appareils à Azure ad** est activé</span><span class="sxs-lookup"><span data-stu-id="7a119-121">Verify**Users may join devices to Azure AD** is enabled</span></span> 
    1. <span data-ttu-id="7a119-122">Pour activer tous les utilisateurs, définissez sur **tous**.</span><span class="sxs-lookup"><span data-stu-id="7a119-122">To enable all users, set to **All**.</span></span>
    2. <span data-ttu-id="7a119-123">Pour activer des utilisateurs spécifiques, définissez sur **sélectionné** pour activer un groupe spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7a119-123">To enable specific users, set to **Selected** to enable a specific group of users.</span></span>
        - <span data-ttu-id="7a119-124">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure Active Directory à un [groupe de sécurité](../admin/create-groups/create-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7a119-124">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        - <span data-ttu-id="7a119-125">Sélectionnez **Sélectionner les groupes** pour activer l’étendue utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7a119-125">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="3-verify-azure-ad-is-enabled-for-mdm"></a><span data-ttu-id="7a119-126">3. Vérifiez que Azure AD est activé pour MDM</span><span class="sxs-lookup"><span data-stu-id="7a119-126">3. Verify Azure AD is enabled for MDM</span></span>

- <span data-ttu-id="7a119-127">Accédez au centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> et sélectionnez Sélectionner le **point de terminaison Manager**t (sélectionnez **Afficher tout** si le **Gestionnaire de point de terminaison** n’est pas visible).</span><span class="sxs-lookup"><span data-stu-id="7a119-127">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select select **Endpoint Managemen**t (select **Show all** if **Endpoint Manager** is not visible)</span></span>
- <span data-ttu-id="7a119-128">Dans le **Centre d’administration du gestionnaire de points de terminaison Microsoft**, accédez à **périphériques**  >  **Windows**  >  **Windows inscriptions**  >  **automatiques**.</span><span class="sxs-lookup"><span data-stu-id="7a119-128">In the **Microsoft Endpoint Manager admin center**, go to **Devices** > **Windows** > **Windows Enrollment** > **Automatic Enrollment**.</span></span>
- <span data-ttu-id="7a119-129">Vérifiez que l’étendue utilisateur MDM est activée.</span><span class="sxs-lookup"><span data-stu-id="7a119-129">Verify MDM user scope is enabled.</span></span>

    1. <span data-ttu-id="7a119-130">Pour inscrire tous les ordinateurs, définissez sur **tous** pour inscrire automatiquement tous les ordinateurs des utilisateurs qui sont joints à Azure ad et les nouveaux ordinateurs lorsque les utilisateurs ajoutent un compte professionnel à Windows.</span><span class="sxs-lookup"><span data-stu-id="7a119-130">To enroll all computers, set to **All** to automatically enroll all user computers that are joined to Azure AD and new computers  when the users add a work account to Windows.</span></span>
    2. <span data-ttu-id="7a119-131">Définissez sur **some** pour inscrire les ordinateurs d’un groupe d’utilisateurs spécifique.</span><span class="sxs-lookup"><span data-stu-id="7a119-131">Set to **Some** to enroll the computers of a specific group of users.</span></span>
        -  <span data-ttu-id="7a119-132">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure Active Directory à un [groupe de sécurité](../admin/create-groups/create-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7a119-132">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        -  <span data-ttu-id="7a119-133">Sélectionnez **Sélectionner les groupes** pour activer l’étendue utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7a119-133">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="4-create-the-required-resources"></a><span data-ttu-id="7a119-134">4. créer les ressources requises</span><span class="sxs-lookup"><span data-stu-id="7a119-134">4. Create the required resources</span></span> 

<span data-ttu-id="7a119-135">L’exécution des tâches requises pour [configurer la jointure Azure ad hybride](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join) a été simplifiée à l’aide de la cmdlet [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) figurant dans le module [SecMgmt](https://www.powershellgallery.com/packages/SecMgmt) PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7a119-135">Performing the required tasks to [configure hybrid Azure AD join](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join) has been simplified through the use of the [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) cmdlet found in the [SecMgmt](https://www.powershellgallery.com/packages/SecMgmt) PowerShell module.</span></span> <span data-ttu-id="7a119-136">Lorsque vous appelez cette applet de commande, celle-ci crée et configure le point de connexion de service et la stratégie de groupe requis.</span><span class="sxs-lookup"><span data-stu-id="7a119-136">When you invoke this cmdlet it will create and configure the required service connection point and group policy.</span></span>

<span data-ttu-id="7a119-137">Vous pouvez installer ce module en appelant les éléments suivants à partir d’une instance de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="7a119-137">You can install this module by invoking the following from an instance of PowerShell:</span></span>

```powershell
Install-Module SecMgmt
```

> [!IMPORTANT]
> <span data-ttu-id="7a119-138">Il est recommandé d’installer ce module sur le serveur Windows exécutant Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="7a119-138">It is recommended that you install this module on the Windows Server running Azure AD Connect.</span></span>

<span data-ttu-id="7a119-139">Pour créer le point de connexion de service et la stratégie de groupe requis, vous devez appeler la cmdlet [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) .</span><span class="sxs-lookup"><span data-stu-id="7a119-139">To create the required service connection point and group policy, you will invoke the  [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) cmdlet.</span></span> <span data-ttu-id="7a119-140">Vous aurez besoin de vos informations d’identification d’administrateur global Microsoft 365 Business Premium lorsque vous effectuerez cette tâche.</span><span class="sxs-lookup"><span data-stu-id="7a119-140">You will need your Microsoft 365 Business Premium global admin credentials when performing this task.</span></span> <span data-ttu-id="7a119-141">Lorsque vous êtes prêt à créer les ressources, appelez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7a119-141">When you are ready to create the resources, invoke the following:</span></span>

```powershell
PS C:\> Connect-SecMgmtAccount
PS C:\> Initialize-SecMgmtHybirdDeviceEnrollment -GroupPolicyDisplayName 'Device Management'
```

<span data-ttu-id="7a119-142">La première commande établira une connexion avec le Cloud Microsoft et, lorsque vous y êtes invité, spécifiez vos informations d’identification d’administrateur global Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7a119-142">The first command will establish a connection with the Microsoft cloud, and when you are prompted, specify your Microsoft 365 Business Premium global admin credentials.</span></span>

## <a name="5-link-the-group-policy"></a><span data-ttu-id="7a119-143">5. lier la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="7a119-143">5. Link the Group Policy</span></span>

1. <span data-ttu-id="7a119-144">Dans la console de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l’emplacement auquel vous souhaitez lier la stratégie, puis sélectionnez *lier un objet de stratégie de groupe existant...* dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7a119-144">In the Group Policy Management Console (GPMC), right-click on the location where you want to link the policy and select *Link an existing GPO...* from the context menu.</span></span>
2. <span data-ttu-id="7a119-145">Sélectionnez la stratégie créée à l’étape ci-dessus, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a119-145">Select the policy created in the above step, then click **OK**.</span></span>

## <a name="get-the-latest-administrative-templates"></a><span data-ttu-id="7a119-146">Obtenir les derniers modèles d’administration</span><span class="sxs-lookup"><span data-stu-id="7a119-146">Get the latest Administrative Templates</span></span>

<span data-ttu-id="7a119-147">Si vous ne voyez pas la stratégie **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut**, il se peut que vous n’ayez pas installé ADMX pour Windows 10, version 1803, version 1809 ou version 1903.</span><span class="sxs-lookup"><span data-stu-id="7a119-147">If you do not see the policy **Enable automatic MDM enrollment using default Azure AD credentials**, it may be because you don’t have the ADMX installed for Windows 10, version 1803, version 1809, or version 1903.</span></span> <span data-ttu-id="7a119-148">Pour résoudre le problème, procédez comme suit (Remarque : la dernière version de MDM. admx est compatible avec les versions antérieures) :</span><span class="sxs-lookup"><span data-stu-id="7a119-148">To fix the issue, follow these steps (Note: the latest MDM.admx is backwards compatible):</span></span>

1.  <span data-ttu-id="7a119-149">Téléchargement : [modèles d’administration (. admx) pour Windows 10 mai 2019 mise à jour (1903)](https://www.microsoft.com/download/details.aspx?id=58495&WT.mc_id=rss_alldownloads_all).</span><span class="sxs-lookup"><span data-stu-id="7a119-149">Download: [Administrative Templates (.admx) for Windows 10 May 2019 Update (1903)](https://www.microsoft.com/download/details.aspx?id=58495&WT.mc_id=rss_alldownloads_all).</span></span>
2.  <span data-ttu-id="7a119-150">Installez le package sur le contrôleur de domaine principal (PDC).</span><span class="sxs-lookup"><span data-stu-id="7a119-150">Install the package on the Primary Domain Controller (PDC).</span></span>
3.  <span data-ttu-id="7a119-151">Naviguez en fonction de la version du dossier : **C:\Program Files (x86) \Microsoft Group Policy\Windows 10 mai 2019 mise à jour (1903) v3**.</span><span class="sxs-lookup"><span data-stu-id="7a119-151">Navigate, depending on the version to the folder: **C:\Program Files (x86)\Microsoft Group Policy\Windows 10 May 2019 Update (1903) v3**.</span></span>
4.  <span data-ttu-id="7a119-152">Renommez le dossier des **définitions de stratégie** dans le chemin d’accès ci-dessus en **PolicyDefinitions**.</span><span class="sxs-lookup"><span data-stu-id="7a119-152">Rename the **Policy Definitions** folder in the above path to **PolicyDefinitions**.</span></span>
5.  <span data-ttu-id="7a119-153">Copiez le dossier **PolicyDefinitions** dans **C:\Windows\SYSVOL\domain\Policies**.</span><span class="sxs-lookup"><span data-stu-id="7a119-153">Copy **PolicyDefinitions** folder to **C:\Windows\SYSVOL\domain\Policies**.</span></span> 
    -   <span data-ttu-id="7a119-154">Si vous envisagez d’utiliser un magasin de stratégies central pour l’ensemble de votre domaine, ajoutez le contenu de PolicyDefinitions.</span><span class="sxs-lookup"><span data-stu-id="7a119-154">If you plan to use a central policy store for your entire domain, add the contents of PolicyDefinitions there.</span></span>
6.  <span data-ttu-id="7a119-155">Redémarrez le contrôleur de domaine principal pour que la stratégie soit disponible.</span><span class="sxs-lookup"><span data-stu-id="7a119-155">Restart the Primary Domain Controller for the policy to be available.</span></span> <span data-ttu-id="7a119-156">Cette procédure fonctionnera également pour toute version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a119-156">This procedure will work for any future version as well.</span></span>

<span data-ttu-id="7a119-157">À ce stade, vous devriez être en mesure d’afficher la stratégie **activer l’enregistrement MDM automatique à l’aide des informations d’identification Azure ad par défaut** disponibles.</span><span class="sxs-lookup"><span data-stu-id="7a119-157">At this point you should be able to see the policy **Enable automatic MDM enrollment using default Azure AD credentials** available.</span></span>
