---
title: Déploiement basé sur l’application pour Microsoft Defender pour Endpoint sur iOS
ms.reviewer: ''
description: Décrit comment déployer Microsoft Defender pour endpoint sur iOS à l’aide d’une application
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, ios, application, installation, déployer, désinstallation, intune
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: a3711018034bcabdde10c21b3c968c3e813d0565
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245255"
---
# <a name="deploy-microsoft-defender-for-endpoint-on-ios"></a><span data-ttu-id="dd64b-104">Déployer Microsoft Defender pour le point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="dd64b-104">Deploy Microsoft Defender for Endpoint on iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="dd64b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dd64b-105">**Applies to:**</span></span>
- [<span data-ttu-id="dd64b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dd64b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="dd64b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dd64b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="dd64b-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="dd64b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="dd64b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="dd64b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="dd64b-110">Cette rubrique décrit le déploiement de Defender pour Endpoint sur iOS Portail d’entreprise Intune appareils inscrits.</span><span class="sxs-lookup"><span data-stu-id="dd64b-110">This topic describes deploying Defender for Endpoint on iOS on Intune Company Portal enrolled devices.</span></span> <span data-ttu-id="dd64b-111">Pour plus d’informations sur l’inscription d’appareils Intune, voir Inscrire des appareils [iOS/iPadOS dans Intune.](https://docs.microsoft.com/mem/intune/enrollment/ios-enroll)</span><span class="sxs-lookup"><span data-stu-id="dd64b-111">For more information about Intune device enrollment, see [Enroll iOS/iPadOS devices in Intune](https://docs.microsoft.com/mem/intune/enrollment/ios-enroll).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="dd64b-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="dd64b-112">Before you begin</span></span>

- <span data-ttu-id="dd64b-113">Assurez-vous que vous avez accès au [Centre d’administration Microsoft Endpoint Manager.](https://go.microsoft.com/fwlink/?linkid=2109431)</span><span class="sxs-lookup"><span data-stu-id="dd64b-113">Ensure you have access to [Microsoft Endpoint manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431).</span></span>

- <span data-ttu-id="dd64b-114">Assurez-vous que l’inscription iOS est effectuée pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dd64b-114">Ensure iOS enrollment is done for your users.</span></span> <span data-ttu-id="dd64b-115">Une licence Defender pour point de terminaison doit être attribuée aux utilisateurs pour pouvoir utiliser Defender pour Endpoint sur iOS.</span><span class="sxs-lookup"><span data-stu-id="dd64b-115">Users need to have a Defender for Endpoint license assigned in order to use Defender for Endpoint on iOS.</span></span> <span data-ttu-id="dd64b-116">Reportez-vous [à Attribuer des licences aux](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign) utilisateurs pour obtenir des instructions sur la façon d’attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="dd64b-116">Refer to [Assign licenses to users](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign) for instructions on how to assign licenses.</span></span>

> [!NOTE]
> <span data-ttu-id="dd64b-117">Microsoft Defender pour le point de terminaison sur iOS est désormais disponible dans [l’App Store d’Apple.](https://aka.ms/mdatpiosappstore)</span><span class="sxs-lookup"><span data-stu-id="dd64b-117">Microsoft Defender for Endpoint on iOS is now available in the [Apple App Store](https://aka.ms/mdatpiosappstore).</span></span>

## <a name="deployment-steps"></a><span data-ttu-id="dd64b-118">Étapes de déploiement</span><span class="sxs-lookup"><span data-stu-id="dd64b-118">Deployment steps</span></span>

<span data-ttu-id="dd64b-119">Déployez Defender pour endpoint sur iOS via Portail d’entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="dd64b-119">Deploy Defender for Endpoint on iOS via Intune Company Portal.</span></span>

### <a name="add-ios-store-app"></a><span data-ttu-id="dd64b-120">Ajouter une application du Store iOS</span><span class="sxs-lookup"><span data-stu-id="dd64b-120">Add iOS store app</span></span>

1. <span data-ttu-id="dd64b-121">Dans [le Centre d’administration Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431)allez sur **Applications**  ->  **iOS/iPadOS** Ajouter une application de la Boutique  ->    ->  **d’applications iOS,** puis cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-121">In [Microsoft Endpoint manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Apps** -> **iOS/iPadOS** -> **Add** -> **iOS store app** and click **Select**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-122">![Image de Microsoft Endpoint Manager Centre d’administration 1](images/ios-deploy-1.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-122">![Image of Microsoft Endpoint Manager Admin Center1](images/ios-deploy-1.png)</span></span>

1. <span data-ttu-id="dd64b-123">Dans la page Ajouter une application, cliquez sur Rechercher dans **l’App Store** et tapez **Microsoft Defender Endpoint** dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd64b-123">On the Add app page, click on **Search the App Store** and type **Microsoft Defender Endpoint** in the search bar.</span></span> <span data-ttu-id="dd64b-124">Dans la section des résultats de la recherche, cliquez sur Le point de terminaison *Microsoft Defender* et cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-124">In the search results section, click on *Microsoft Defender Endpoint* and click **Select**.</span></span>

1. <span data-ttu-id="dd64b-125">Sélectionnez **iOS 11.0 comme** système d’exploitation minimum.</span><span class="sxs-lookup"><span data-stu-id="dd64b-125">Select **iOS 11.0** as the Minimum operating system.</span></span> <span data-ttu-id="dd64b-126">Consultez le reste des informations sur l’application et cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-126">Review the rest of information about the app and click **Next**.</span></span>

1. <span data-ttu-id="dd64b-127">Dans la section *Affectations,* allez à la section **Obligatoire** et **sélectionnez Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-127">In the *Assignments* section, go to the **Required** section and select **Add group**.</span></span> <span data-ttu-id="dd64b-128">Vous pouvez ensuite choisir le ou les groupes d’utilisateurs que vous souhaitez cibler Defender pour le point de terminaison sur l’application iOS.</span><span class="sxs-lookup"><span data-stu-id="dd64b-128">You can then choose the user group(s) that you would like to target Defender for Endpoint on iOS app.</span></span> <span data-ttu-id="dd64b-129">Cliquez **sur Sélectionner,** puis **sur Suivant.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-129">Click **Select** and then **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd64b-130">Le groupe d’utilisateurs sélectionné doit être constitué d’utilisateurs inscrits à Intune.</span><span class="sxs-lookup"><span data-stu-id="dd64b-130">The selected user group should consist of Intune enrolled users.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-131">![Image de Microsoft Endpoint Manager Admin Center2](images/ios-deploy-2.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-131">![Image of Microsoft Endpoint Manager Admin Center2](images/ios-deploy-2.png)</span></span>

1. <span data-ttu-id="dd64b-132">Dans la section *Révision + Créer,* vérifiez que toutes les informations entrées sont correctes, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-132">In the *Review + Create* section, verify that all the information entered is correct and then select **Create**.</span></span> <span data-ttu-id="dd64b-133">Dans quelques instants, l’application Defender pour point de terminaison doit être créée correctement et une notification doit s’afficher dans le coin supérieur droit de la page.</span><span class="sxs-lookup"><span data-stu-id="dd64b-133">In a few moments, the Defender for Endpoint app should be created successfully, and a notification should show up at the top-right corner of the page.</span></span>

1. <span data-ttu-id="dd64b-134">Dans la page d’informations sur l’application  qui s’affiche, dans la **section** Moniteur, sélectionnez État de l’installation de l’appareil pour vérifier que l’installation de l’appareil s’est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="dd64b-134">In the app information page that is displayed, in the **Monitor** section, select **Device install status** to verify that the device installation has completed successfully.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-135">![Image de Microsoft Endpoint Manager Centre d’administration 3](images/ios-deploy-3.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-135">![Image of Microsoft Endpoint Manager Admin Center3](images/ios-deploy-3.png)</span></span>

## <a name="auto-onboarding-of-vpn-profile-simplified-onboarding"></a><span data-ttu-id="dd64b-136">Intégration automatique du profil VPN (intégration simplifiée)</span><span class="sxs-lookup"><span data-stu-id="dd64b-136">Auto-Onboarding of VPN profile (Simplified Onboarding)</span></span>

> [!NOTE]
> <span data-ttu-id="dd64b-137">L’intégration automatique du profil VPN est actuellement en prévisualisation et les étapes mentionnées dans cette section peuvent être considérablement modifiées avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="dd64b-137">Auto-onboarding of VPN profile is currently in preview and the steps mentioned in this section may be substantially modified before it's commercially released.</span></span>

<span data-ttu-id="dd64b-138">Les administrateurs peuvent configurer la configuration automatique du profil VPN.</span><span class="sxs-lookup"><span data-stu-id="dd64b-138">Admins can configure auto-setup of VPN profile.</span></span> <span data-ttu-id="dd64b-139">Cela permet de configurer automatiquement le profil VPN Defender pour point de terminaison sans que l’utilisateur le fait lors de l’intégration.</span><span class="sxs-lookup"><span data-stu-id="dd64b-139">This will automatically setup the Defender for Endpoint VPN profile without having the user to do so while onboarding.</span></span> <span data-ttu-id="dd64b-140">Notez que le VPN est utilisé pour fournir la fonctionnalité de protection Web.</span><span class="sxs-lookup"><span data-stu-id="dd64b-140">Note that VPN is used in order to provide the Web Protection feature.</span></span> <span data-ttu-id="dd64b-141">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd64b-141">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span>

1. <span data-ttu-id="dd64b-142">Dans [le Centre d’administration Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431)allez à **l’application** Créer des profils de configuration des appareils et  ->    ->    ->   cliquez sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-142">In [Microsoft Endpoint manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices** -> **Configuration Profiles** -> **Create** -> **iOS store app** and click **Select**.</span></span>
1. <span data-ttu-id="dd64b-143">Choisissez **Plateforme en** tant que **iOS/iPadOS** et type de profil en **tant** que **VPN**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-143">Choose **Platform** as **iOS/iPadOS** and **Profile type** as **VPN**.</span></span> <span data-ttu-id="dd64b-144">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-144">Click **Create**.</span></span>
1. <span data-ttu-id="dd64b-145">Tapez un nom pour le profil, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-145">Type a name for the profile and click **Next**.</span></span>
1. <span data-ttu-id="dd64b-146">Sélectionnez **VPN personnalisé** pour le type de connexion et, dans la section VPN de **base,** entrez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="dd64b-146">Select **Custom VPN** for Connection Type and in the **Base VPN** section, enter the following:</span></span>
    - <span data-ttu-id="dd64b-147">Nom de connexion = Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="dd64b-147">Connection Name = Microsoft Defender for Endpoint</span></span>
    - <span data-ttu-id="dd64b-148">Adresse du serveur VPN = 127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="dd64b-148">VPN server address = 127.0.0.1</span></span>
    - <span data-ttu-id="dd64b-149">Méthode Auth = « Nom d’utilisateur et mot de passe »</span><span class="sxs-lookup"><span data-stu-id="dd64b-149">Auth method = "Username and password"</span></span>
    - <span data-ttu-id="dd64b-150">Tunneling fractionner = Désactiver</span><span class="sxs-lookup"><span data-stu-id="dd64b-150">Split Tunneling = Disable</span></span>
    - <span data-ttu-id="dd64b-151">Identificateur VPN = com.microsoft.scmx</span><span class="sxs-lookup"><span data-stu-id="dd64b-151">VPN identifier = com.microsoft.scmx</span></span>
    - <span data-ttu-id="dd64b-152">Dans les paires clé-valeur, entrez la clé **AutoOnboard** et définissez la valeur sur **True**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-152">In the key-value pairs, enter the key **AutoOnboard** and set the value to **True**.</span></span>
    - <span data-ttu-id="dd64b-153">Type de VPN automatique = VPN à la demande</span><span class="sxs-lookup"><span data-stu-id="dd64b-153">Type of Automatic VPN = On-demand VPN</span></span>
    - <span data-ttu-id="dd64b-154">Cliquez **sur** Ajouter pour **les règles à** la demande et sélectionnez « Je veux faire ce qui suit = Établir un **VPN**, je souhaite me limiter à = Tous **les domaines**».</span><span class="sxs-lookup"><span data-stu-id="dd64b-154">Click **Add** for **On Demand Rules** and select **I want to do the following = Establish VPN**, **I want to restrict to = All domains**.</span></span>

    ![Capture d’écran de la configuration de profil VPN](images/ios-deploy-8.png)

1. <span data-ttu-id="dd64b-156">Cliquez sur Suivant et affectez le profil à des utilisateurs ciblés.</span><span class="sxs-lookup"><span data-stu-id="dd64b-156">Click Next and assign the profile to targeted users.</span></span>
1. <span data-ttu-id="dd64b-157">Dans la section *Révision + Créer,* vérifiez que toutes les informations entrées sont correctes, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-157">In the *Review + Create* section, verify that all the information entered is correct and then select **Create**.</span></span>

## <a name="complete-onboarding-and-check-status"></a><span data-ttu-id="dd64b-158">Terminer l’intégration et vérifier l’état</span><span class="sxs-lookup"><span data-stu-id="dd64b-158">Complete onboarding and check status</span></span>

1. <span data-ttu-id="dd64b-159">Une fois Que Defender pour le point de terminaison sur iOS a été installé sur l’appareil, vous verrez l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="dd64b-159">Once Defender for Endpoint on iOS has been installed on the device, you  will see the app icon.</span></span>

    ![Capture d’écran d’une description de smartphone générée automatiquement](images/41627a709700c324849bf7e13510c516.png)

2. <span data-ttu-id="dd64b-161">Appuyez sur l’icône de l’application Defender for Endpoint et suivez les instructions à l’écran pour effectuer les étapes d’intégration.</span><span class="sxs-lookup"><span data-stu-id="dd64b-161">Tap the Defender for Endpoint app icon and follow the on-screen instructions to complete the onboarding steps.</span></span> <span data-ttu-id="dd64b-162">Les détails incluent l’acceptation par l’utilisateur final des autorisations iOS requises par Defender pour endpoint sur iOS.</span><span class="sxs-lookup"><span data-stu-id="dd64b-162">The details include end-user acceptance of iOS permissions required by Defender for Endpoint on iOS.</span></span>

3. <span data-ttu-id="dd64b-163">Une fois l’intégration réussie, l’appareil commence à s’afficher dans la liste Des appareils dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="dd64b-163">Upon successful onboarding, the device will start showing up on the Devices list in Microsoft Defender Security Center.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-164">![Capture d’écran d’une description de téléphone portable générée automatiquement](images/e07f270419f7b1e5ee6744f8b38ddeaf.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-164">![A screenshot of a cell phone Description automatically generated](images/e07f270419f7b1e5ee6744f8b38ddeaf.png)</span></span>

## <a name="configure-microsoft-defender-for-endpoint-for-supervised-mode"></a><span data-ttu-id="dd64b-165">Configurer Microsoft Defender pour le point de terminaison pour le mode Supervisé</span><span class="sxs-lookup"><span data-stu-id="dd64b-165">Configure Microsoft Defender for Endpoint for Supervised Mode</span></span>

<span data-ttu-id="dd64b-166">Microsoft Defender pour endpoint sur l’application iOS dispose d’une capacité spécialisée sur les appareils iOS/iPadOS supervisés, étant donné les fonctionnalités de gestion accrues fournies par la plateforme sur ces types d’appareils.</span><span class="sxs-lookup"><span data-stu-id="dd64b-166">The Microsoft Defender for Endpoint on iOS app has specialized ability on supervised iOS/iPadOS devices, given the increased management capabilities provided by the platform on these types of devices.</span></span> <span data-ttu-id="dd64b-167">Pour tirer parti de ces fonctionnalités, l’application Defender for Endpoint doit savoir si un appareil est en mode Supervisé.</span><span class="sxs-lookup"><span data-stu-id="dd64b-167">To take advantage of these capabilities, the Defender for Endpoint app needs to know if a device is in Supervised Mode.</span></span>

### <a name="configure-supervised-mode-via-intune"></a><span data-ttu-id="dd64b-168">Configurer le mode Supervisé via Intune</span><span class="sxs-lookup"><span data-stu-id="dd64b-168">Configure Supervised Mode via Intune</span></span>

<span data-ttu-id="dd64b-169">Intune vous permet de configurer l’application Defender pour iOS via une stratégie de configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="dd64b-169">Intune allows you to configure the Defender for iOS app through an App Configuration policy.</span></span>

   > [!NOTE]
   > <span data-ttu-id="dd64b-170">Cette stratégie de configuration d’application pour les appareils supervisés s’applique uniquement aux appareils gérés et doit être ciblée pour tous les appareils iOS gérés en tant que meilleure pratique.</span><span class="sxs-lookup"><span data-stu-id="dd64b-170">This app configuration policy for supervised devices is applicable only to managed devices and should be targeted for all managed iOS devices as a best practice.</span></span>

1. <span data-ttu-id="dd64b-171">Connectez-vous au [centre d Microsoft Endpoint Manager’administration](https://go.microsoft.com/fwlink/?linkid=2109431) et allez aux stratégies de configuration **des applications**  >  **.**  >  </span><span class="sxs-lookup"><span data-stu-id="dd64b-171">Sign in to the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) and go to **Apps** > **App configuration policies** > **Add**.</span></span> <span data-ttu-id="dd64b-172">Cliquez sur **Appareils gérés.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-172">Click on **Managed devices**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-173">![Image de Microsoft Endpoint Manager Centre d’administration 4](images/ios-deploy-4.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-173">![Image of Microsoft Endpoint Manager Admin Center4](images/ios-deploy-4.png)</span></span>

1. <span data-ttu-id="dd64b-174">Dans la page *Créer une stratégie de configuration d’application,* fournissez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dd64b-174">In the *Create app configuration policy* page, provide the following information:</span></span>
    - <span data-ttu-id="dd64b-175">Nom de la stratégie</span><span class="sxs-lookup"><span data-stu-id="dd64b-175">Policy Name</span></span>
    - <span data-ttu-id="dd64b-176">Plateforme : sélectionner iOS/iPadOS</span><span class="sxs-lookup"><span data-stu-id="dd64b-176">Platform: Select iOS/iPadOS</span></span>
    - <span data-ttu-id="dd64b-177">Application ciblée : sélectionnez **Microsoft Defender ATP** dans la liste</span><span class="sxs-lookup"><span data-stu-id="dd64b-177">Targeted app: Select **Microsoft Defender ATP** from the list</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-178">![Image de Microsoft Endpoint Manager Centre d’administration 5](images/ios-deploy-5.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-178">![Image of Microsoft Endpoint Manager Admin Center5](images/ios-deploy-5.png)</span></span>

1. <span data-ttu-id="dd64b-179">Dans l’écran suivant, sélectionnez Utiliser **le concepteur de configuration** comme format.</span><span class="sxs-lookup"><span data-stu-id="dd64b-179">In the next screen, select **Use configuration designer** as the format.</span></span> <span data-ttu-id="dd64b-180">Spécifiez la propriété suivante :</span><span class="sxs-lookup"><span data-stu-id="dd64b-180">Specify the following property:</span></span>
    - <span data-ttu-id="dd64b-181">Clé de configuration : issupervised</span><span class="sxs-lookup"><span data-stu-id="dd64b-181">Configuration Key: issupervised</span></span>
    - <span data-ttu-id="dd64b-182">Type de valeur : Chaîne</span><span class="sxs-lookup"><span data-stu-id="dd64b-182">Value type: String</span></span>
    - <span data-ttu-id="dd64b-183">Valeur de configuration : {{issupervised}}</span><span class="sxs-lookup"><span data-stu-id="dd64b-183">Configuration Value: {{issupervised}}</span></span>
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-184">![Image de Microsoft Endpoint Manager Centre d’administration 6](images/ios-deploy-6.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-184">![Image of Microsoft Endpoint Manager Admin Center6](images/ios-deploy-6.png)</span></span>

1. <span data-ttu-id="dd64b-185">Cliquez **sur Suivant** pour ouvrir la page **Balises d’étendue.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-185">Click **Next** to open the **Scope tags** page.</span></span> <span data-ttu-id="dd64b-186">Les balises d’étendue sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="dd64b-186">Scope tags are optional.</span></span> <span data-ttu-id="dd64b-187">Cliquez sur **Suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="dd64b-187">Click **Next** to continue.</span></span>

1. <span data-ttu-id="dd64b-188">Dans la page **Affectations,** sélectionnez les groupes qui recevront ce profil.</span><span class="sxs-lookup"><span data-stu-id="dd64b-188">On the **Assignments** page, select the groups that will receive this profile.</span></span> <span data-ttu-id="dd64b-189">Pour ce scénario, il est préférable de cibler **tous les appareils.**</span><span class="sxs-lookup"><span data-stu-id="dd64b-189">For this scenario, it is best practice to target **All Devices**.</span></span> <span data-ttu-id="dd64b-190">Pour plus d’informations sur l’attribution de profils, voir [Attribuer des profils utilisateur et d’appareil.](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign)</span><span class="sxs-lookup"><span data-stu-id="dd64b-190">For more information on assigning profiles, see [Assign user and device profiles](https://docs.microsoft.com/mem/intune/configuration/device-profile-assign).</span></span>

   <span data-ttu-id="dd64b-191">Lors du déploiement sur des groupes d’utilisateurs, un utilisateur doit se connecter à un appareil avant que la stratégie ne s’applique.</span><span class="sxs-lookup"><span data-stu-id="dd64b-191">When deploying to user groups, a user must sign in to a device before the policy applies.</span></span>

   <span data-ttu-id="dd64b-192">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-192">Click **Next**.</span></span>

1. <span data-ttu-id="dd64b-193">On the **Review + create** page, when you’re done, choose **Create**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-193">On the **Review + create** page, when you're done, choose **Create**.</span></span> <span data-ttu-id="dd64b-194">Le nouveau profil s’affiche dans la liste des profils de configuration.</span><span class="sxs-lookup"><span data-stu-id="dd64b-194">The new profile is displayed in the list of configuration profiles.</span></span>

1. <span data-ttu-id="dd64b-195">Ensuite, pour les fonctionnalités anti-hameçonnage améliorées, vous pouvez déployer un profil personnalisé sur les appareils iOS supervisés.</span><span class="sxs-lookup"><span data-stu-id="dd64b-195">Next, for enhanced Anti-phishing capabilities, you can deploy a custom profile on the supervised iOS devices.</span></span> <span data-ttu-id="dd64b-196">Suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="dd64b-196">Follow the steps below:</span></span>
    - <span data-ttu-id="dd64b-197">Télécharger le profil de config à partir de [https://aka.ms/mdatpiossupervisedprofile](https://aka.ms/mdatpiossupervisedprofile)</span><span class="sxs-lookup"><span data-stu-id="dd64b-197">Download the config profile from [https://aka.ms/mdatpiossupervisedprofile](https://aka.ms/mdatpiossupervisedprofile)</span></span>
    - <span data-ttu-id="dd64b-198">Accéder aux **profils**  ->  **de configuration iOS/iPadOS** Des appareils  ->    ->  **créent un profil**</span><span class="sxs-lookup"><span data-stu-id="dd64b-198">Navigate to **Devices** -> **iOS/iPadOS** -> **Configuration profiles** -> **Create Profile**</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="dd64b-199">![Image de Microsoft Endpoint Manager Centre d’administration 7](images/ios-deploy-7.png)</span><span class="sxs-lookup"><span data-stu-id="dd64b-199">![Image of Microsoft Endpoint Manager Admin Center7](images/ios-deploy-7.png)</span></span>

    - <span data-ttu-id="dd64b-200">Fournissez le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="dd64b-200">Provide a name of the profile.</span></span> <span data-ttu-id="dd64b-201">Lorsque vous y invitez l’importation d’un fichier de profil de configuration, sélectionnez celui téléchargé ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="dd64b-201">When prompted to import a Configuration profile file, select the one downloaded above.</span></span>
    - <span data-ttu-id="dd64b-202">Dans la section **Affectation,** sélectionnez le groupe d’appareils auquel vous souhaitez appliquer ce profil.</span><span class="sxs-lookup"><span data-stu-id="dd64b-202">In the **Assignment** section, select the device group to which you want to apply this profile.</span></span> <span data-ttu-id="dd64b-203">Il est préférable de l’appliquer à tous les appareils iOS gérés.</span><span class="sxs-lookup"><span data-stu-id="dd64b-203">As a best practice, this should be applied to all managed iOS devices.</span></span> <span data-ttu-id="dd64b-204">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-204">Click **Next**.</span></span>
    - <span data-ttu-id="dd64b-205">On the **Review + create** page, when you’re done, choose **Create**.</span><span class="sxs-lookup"><span data-stu-id="dd64b-205">On the **Review + create** page, when you're done, choose **Create**.</span></span> <span data-ttu-id="dd64b-206">Le nouveau profil s’affiche dans la liste des profils de configuration.</span><span class="sxs-lookup"><span data-stu-id="dd64b-206">The new profile is displayed in the list of configuration profiles.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dd64b-207">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="dd64b-207">Next Steps</span></span>

[<span data-ttu-id="dd64b-208">Configurer Defender pour endpoint sur les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="dd64b-208">Configure Defender for Endpoint on iOS features</span></span>](ios-configure-features.md)
