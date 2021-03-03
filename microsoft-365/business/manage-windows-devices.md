---
title: Activer la gestion des appareils Windows 10 joints à un domaine par Microsoft 365 pour les entreprises
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
description: Découvrez comment activer Microsoft 365 pour protéger les appareils Windows 10 locaux joints à Active Directory en quelques étapes.
ms.openlocfilehash: 0b597110447272be128bfe1866234ac25a8e67e6
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50407075"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business-premium"></a><span data-ttu-id="6e4e9-103">Activer la gestion des appareils Windows 10 joints à un domaine par Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="6e4e9-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium</span></span>

<span data-ttu-id="6e4e9-104">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 Business Premium pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-104">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business Premium to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span>
<span data-ttu-id="6e4e9-105">Pour configurer cette protection, vous pouvez implémenter des appareils **joints à Azure AD hybride.**</span><span class="sxs-lookup"><span data-stu-id="6e4e9-105">To set up this protection, you can implement **Hybrid Azure AD joined devices**.</span></span> <span data-ttu-id="6e4e9-106">Ces appareils sont joints à votre annuaire Active Directory local et à azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-106">These devices are joined to both your on-premises Active Directory and your Azure Active Directory.</span></span>

<span data-ttu-id="6e4e9-107">Cette vidéo décrit les étapes à suivre pour la configurer pour le scénario le plus courant, qui est également détaillée dans les étapes qui suivent.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-107">This video describes the steps for how to set this up for the most common scenario, which is also detailed in the steps that follow.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3C9hO]
  

## <a name="before-you-get-started-make-sure-you-complete-these-steps"></a><span data-ttu-id="6e4e9-108">Avant de commencer, veillez à effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e4e9-108">Before you get started, make sure you complete these steps:</span></span>
- <span data-ttu-id="6e4e9-109">Synchronisez les utilisateurs avec Azure AD avec Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-109">Synchronize users to Azure AD with Azure AD Connect.</span></span>
- <span data-ttu-id="6e4e9-110">Synchronisez l’unité d’organisation (OU) Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-110">Complete Azure AD Connect Organizational Unit (OU) sync.</span></span>
- <span data-ttu-id="6e4e9-111">Assurez-vous que tous les utilisateurs de domaine que vous synchronisez ont des licences pour Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-111">Make sure all the domain users you sync have licenses to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="6e4e9-112">Pour obtenir la procédure [à suivre, consultez](manage-domain-users.md) Synchroniser les utilisateurs de domaine avec Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-112">See [Synchronize domain users to Microsoft](manage-domain-users.md) for the steps.</span></span>

## <a name="1-verify-mdm-authority-in-intune"></a><span data-ttu-id="6e4e9-113">1. Vérifier l’autorité mdm dans Intune</span><span class="sxs-lookup"><span data-stu-id="6e4e9-113">1. Verify MDM Authority in Intune</span></span>

<span data-ttu-id="6e4e9-114">Go to [Endpoint Manager](https://endpoint.microsoft.com/#blade/Microsoft_Intune_Enrollment/EnrollmentMenu/overview) and on the Microsoft Intune page, select **Device enrollment**, then on the **Overview** page, make sure **MDM authority** is **Intune**.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-114">Go to [Endpoint Manager](https://endpoint.microsoft.com/#blade/Microsoft_Intune_Enrollment/EnrollmentMenu/overview) and on the Microsoft Intune page, select **Device enrollment**, then on the **Overview** page, make sure **MDM authority** is **Intune**.</span></span>

- <span data-ttu-id="6e4e9-115">Si **l’autorité MDM** est **Aucune,** cliquez sur l’autorité **DE GESTION** pour la définir sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-115">If **MDM authority** is **None**, click the **MDM authority** to set it to **Intune**.</span></span>
- <span data-ttu-id="6e4e9-116">Si  l’autorité de gestion des périphériques mobiles est Microsoft Office **365**, allez sur Périphériques Inscrire des appareils et utilisez la boîte de dialogue Ajouter une autorité de gestion des appareils mobiles sur le droit pour ajouter l’autorité de gestion des appareils mobiles  >   **Intune** (la boîte de dialogue Ajouter une autorité **MDM** est disponible uniquement si l’autorité **mdm** est définie sur Microsoft Office 365). </span><span class="sxs-lookup"><span data-stu-id="6e4e9-116">If **MDM authority** is **Microsoft Office 365**,go to **Devices** > **Enroll devices** and use the **Add MDM authority** dialog on the right to add **Intune MDM** authority (the **Add MDM Authority** dialog is only available if the **MDM Authority** is set to Microsoft Office 365).</span></span>

## <a name="2-verify-azure-ad-is-enabled-for-joining-computers"></a><span data-ttu-id="6e4e9-117">2. Vérifiez qu’Azure AD est activé pour joindre des ordinateurs</span><span class="sxs-lookup"><span data-stu-id="6e4e9-117">2. Verify Azure AD is enabled for joining computers</span></span>

- <span data-ttu-id="6e4e9-118">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select Azure Active **Directory** (select Show all if Azure Active Directory is not visible) in the **Admin centers** list.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-118">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select **Azure Active Directory** (select Show all if Azure Active Directory is not visible) in the **Admin centers** list.</span></span> 
- <span data-ttu-id="6e4e9-119">Dans le **Centre d’administration Azure Active Directory,** allez à **Azure Active Directory,** choisissez Appareils, puis **Paramètres de l’appareil.** </span><span class="sxs-lookup"><span data-stu-id="6e4e9-119">In the **Azure Active Directory admin center**, go to **Azure Active Directory** , choose **Devices** and then **Device settings**.</span></span>
- <span data-ttu-id="6e4e9-120">Vérifier **que les utilisateurs peuvent joindre des appareils à Azure AD** est activé</span><span class="sxs-lookup"><span data-stu-id="6e4e9-120">Verify **Users may join devices to Azure AD** is enabled</span></span> 
    1. <span data-ttu-id="6e4e9-121">Pour activer tous les utilisateurs, définissez-le sur **Tous.**</span><span class="sxs-lookup"><span data-stu-id="6e4e9-121">To enable all users, set to **All**.</span></span>
    2. <span data-ttu-id="6e4e9-122">Pour activer des utilisateurs spécifiques, **définissez-le sur Sélectionné** pour activer un groupe spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-122">To enable specific users, set to **Selected** to enable a specific group of users.</span></span>
        - <span data-ttu-id="6e4e9-123">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure AD à un [groupe de sécurité.](../admin/create-groups/create-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-123">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        - <span data-ttu-id="6e4e9-124">Sélectionnez **Sélectionner des groupes** pour activer l’étendue de l’utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-124">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="3-verify-azure-ad-is-enabled-for-mdm"></a><span data-ttu-id="6e4e9-125">3. Vérifier qu’Azure AD est activé pour la gestion des données de gestion des données</span><span class="sxs-lookup"><span data-stu-id="6e4e9-125">3. Verify Azure AD is enabled for MDM</span></span>

- <span data-ttu-id="6e4e9-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select **select Endpoint Managemen** t (select **Show all** if **Endpoint Manager** is not visible)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a>  and select select **Endpoint Managemen** t (select **Show all** if **Endpoint Manager** is not visible)</span></span>
- <span data-ttu-id="6e4e9-127">Dans le Centre **d’administration Microsoft Endpoint Manager,** allez sur **Appareils**  >    >  **Windows Inscription** automatique  >  .</span><span class="sxs-lookup"><span data-stu-id="6e4e9-127">In the **Microsoft Endpoint Manager admin center**, go to **Devices** > **Windows** > **Windows Enrollment** > **Automatic Enrollment**.</span></span>
- <span data-ttu-id="6e4e9-128">Vérifiez que l’étendue de l’utilisateur mdm est activée.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-128">Verify MDM user scope is enabled.</span></span>

    1. <span data-ttu-id="6e4e9-129">Pour inscrire tous les  ordinateurs, définissez-le sur Tous pour inscrire automatiquement tous les ordinateurs utilisateur qui sont joints à Azure AD et les nouveaux ordinateurs lorsque les utilisateurs ajoutent un compte de travail à Windows.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-129">To enroll all computers, set to **All** to automatically enroll all user computers that are joined to Azure AD and new computers  when the users add a work account to Windows.</span></span>
    2. <span data-ttu-id="6e4e9-130">Définir sur **Some pour** inscrire les ordinateurs d’un groupe spécifique d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-130">Set to **Some** to enroll the computers of a specific group of users.</span></span>
        -  <span data-ttu-id="6e4e9-131">Ajoutez les utilisateurs de domaine souhaités synchronisés dans Azure AD à un [groupe de sécurité.](../admin/create-groups/create-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-131">Add the desired domain users synced in Azure AD to a [security group](../admin/create-groups/create-groups.md).</span></span>
        -  <span data-ttu-id="6e4e9-132">Sélectionnez **Sélectionner des groupes** pour activer l’étendue de l’utilisateur MDM pour ce groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-132">Choose **Select groups** to enable MDM user scope for that security group.</span></span>

## <a name="4-create-the-required-resources"></a><span data-ttu-id="6e4e9-133">4. Créer les ressources requises</span><span class="sxs-lookup"><span data-stu-id="6e4e9-133">4. Create the required resources</span></span> 

<span data-ttu-id="6e4e9-134">L’utilisation de l’cmdlet [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) trouvée dans le module [SecMgmt](https://www.powershellgallery.com/packages/SecMgmt) PowerShell a simplifié l’réalisation des tâches requises pour configurer la jointage [Azure AD](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join) hybride.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-134">Performing the required tasks to [configure hybrid Azure AD join](https://docs.microsoft.com/azure/active-directory/devices/hybrid-azuread-join-managed-domains#configure-hybrid-azure-ad-join) has been simplified through the use of the [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) cmdlet found in the [SecMgmt](https://www.powershellgallery.com/packages/SecMgmt) PowerShell module.</span></span> <span data-ttu-id="6e4e9-135">Lorsque vous voquez cette cmdlet, elle crée et configure le point de connexion de service et la stratégie de groupe requis.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-135">When you invoke this cmdlet it will create and configure the required service connection point and group policy.</span></span>

<span data-ttu-id="6e4e9-136">Vous pouvez installer ce module en invoquant les éléments suivants à partir d’une instance de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="6e4e9-136">You can install this module by invoking the following from an instance of PowerShell:</span></span>

```powershell
Install-Module SecMgmt
```

> [!IMPORTANT]
> <span data-ttu-id="6e4e9-137">Il est recommandé d’installer ce module sur le serveur Windows exécutant Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-137">It is recommended that you install this module on the Windows Server running Azure AD Connect.</span></span>

<span data-ttu-id="6e4e9-138">Pour créer le point de connexion de service et la stratégie de groupe requis, vous allez appeler l’cmdlet [Initialize-SecMgmtHybirdDeviceEnrollment.](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-138">To create the required service connection point and group policy, you will invoke the  [Initialize-SecMgmtHybirdDeviceEnrollment](https://github.com/microsoft/secmgmt-open-powershell/blob/master/docs/help/Initialize-SecMgmtHybirdDeviceEnrollment.md) cmdlet.</span></span> <span data-ttu-id="6e4e9-139">Vous aurez besoin de vos informations d’identification d’administrateur global Microsoft 365 Business Premium pour effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-139">You will need your Microsoft 365 Business Premium global admin credentials when performing this task.</span></span> <span data-ttu-id="6e4e9-140">Lorsque vous êtes prêt à créer les ressources, invoke the following:</span><span class="sxs-lookup"><span data-stu-id="6e4e9-140">When you are ready to create the resources, invoke the following:</span></span>

```powershell
PS C:\> Connect-SecMgmtAccount
PS C:\> Initialize-SecMgmtHybirdDeviceEnrollment -GroupPolicyDisplayName 'Device Management'
```

<span data-ttu-id="6e4e9-141">La première commande établit une connexion avec le cloud Microsoft et, lorsque vous y êtes invité, spécifiez vos informations d’identification d’administrateur général Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-141">The first command will establish a connection with the Microsoft cloud, and when you are prompted, specify your Microsoft 365 Business Premium global admin credentials.</span></span>

## <a name="5-link-the-group-policy"></a><span data-ttu-id="6e4e9-142">5. Lier la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6e4e9-142">5. Link the Group Policy</span></span>

1. <span data-ttu-id="6e4e9-143">Dans la Console de gestion des stratégies de groupe (GPMC), cliquez avec le bouton droit sur l’emplacement où vous souhaitez lier la stratégie et sélectionnez Lier un *GPO existant...* dans le menu contextique.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-143">In the Group Policy Management Console (GPMC), right-click on the location where you want to link the policy and select *Link an existing GPO...* from the context menu.</span></span>
2. <span data-ttu-id="6e4e9-144">Sélectionnez la stratégie créée à l’étape ci-dessus, puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="6e4e9-144">Select the policy created in the above step, then click **OK**.</span></span>

## <a name="get-the-latest-administrative-templates"></a><span data-ttu-id="6e4e9-145">Obtenir les derniers modèles d’administration</span><span class="sxs-lookup"><span data-stu-id="6e4e9-145">Get the latest Administrative Templates</span></span>

<span data-ttu-id="6e4e9-146">Si vous ne voyez pas la stratégie Activer l’inscription mdm automatique à l’aide des informations d’identification **Azure AD** par défaut, c’est peut-être parce que vous n’avez pas installé ADMX pour Windows 10, version 1803 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-146">If you do not see the policy **Enable automatic MDM enrollment using default Azure AD credentials**, it may be because you don’t have the ADMX installed for Windows 10, version 1803, or later.</span></span> <span data-ttu-id="6e4e9-147">Pour résoudre le problème, suivez les étapes suivantes (Remarque : la dernière version de MDM.admx est à compatibilité avec l’arrière) :</span><span class="sxs-lookup"><span data-stu-id="6e4e9-147">To fix the issue, follow these steps (Note: the latest MDM.admx is backwards compatible):</span></span>

1.  <span data-ttu-id="6e4e9-148">Téléchargement : [Modèles d’administration (.admx) pour la mise à jour d’octobre 2020 de Windows 10 (20H2)](https://www.microsoft.com/download/102157).</span><span class="sxs-lookup"><span data-stu-id="6e4e9-148">Download: [Administrative Templates (.admx) for Windows 10 October 2020 Update (20H2)](https://www.microsoft.com/download/102157).</span></span>
2.  <span data-ttu-id="6e4e9-149">Installez le package sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-149">Install the package on a Domain Controller.</span></span>
3.  <span data-ttu-id="6e4e9-150">Accédez, en fonction de la version des modèles d’administration, au dossier **: C:\Program Files (x86)\Microsoft Group Policy\Windows 10 October 2020 Update (20H2)**.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-150">Navigate, depending on the Administrative Templates version to the folder: **C:\Program Files (x86)\Microsoft Group Policy\Windows 10 October 2020 Update (20H2)**.</span></span>
4.  <span data-ttu-id="6e4e9-151">Renommons le **dossier Définitions de stratégie dans** le chemin d’accès ci-dessus à **PolicyDefinitions**.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-151">Rename the **Policy Definitions** folder in the above path to **PolicyDefinitions**.</span></span>
5.  <span data-ttu-id="6e4e9-152">Copiez **le dossier PolicyDefinitions** dans votre partage SYSVOL, par défaut situé dans **C:\Windows\SYSVOL\domain\Policies**.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-152">Copy the **PolicyDefinitions** folder to your SYSVOL share, by default located at **C:\Windows\SYSVOL\domain\Policies**.</span></span> 
    -   <span data-ttu-id="6e4e9-153">Si vous envisagez d’utiliser un magasin central de stratégies pour l’ensemble de votre domaine, ajoutez-y le contenu de PolicyDefinitions.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-153">If you plan to use a central policy store for your entire domain, add the contents of PolicyDefinitions there.</span></span>
6.  <span data-ttu-id="6e4e9-154">Si vous avez plusieurs contrôleurs de domaine, attendez que SYSVOL réplique pour que les stratégies soient disponibles.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-154">In case you have several Domain Controllers, wait for SYSVOL to replicate for the policies to be available.</span></span> <span data-ttu-id="6e4e9-155">Cette procédure fonctionne également pour n’importe quelle version future des modèles d’administration.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-155">This procedure will work for any future version of the Administrative Templates as well.</span></span>

<span data-ttu-id="6e4e9-156">À ce stade, vous devriez être en mesure de voir la stratégie Activer l’inscription mdm automatique à l’aide des informations d’identification **Azure AD par défaut** disponibles.</span><span class="sxs-lookup"><span data-stu-id="6e4e9-156">At this point you should be able to see the policy **Enable automatic MDM enrollment using default Azure AD credentials** available.</span></span>
