---
title: Déployer Microsoft Defender pour point de terminaison Android via Microsoft Intune
description: Décrit comment déployer Microsoft Defender pour Endpoint pour Android avec Microsoft Intune
keywords: microsoft, defender, atp, mde, android, installation, déployer, désinstallation,
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: fdfc6e63945e15ce2d1f1a293c377f641eeb9bc4
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587694"
---
# <a name="deploy-microsoft-defender-for-endpoint-for-android-with-microsoft-intune"></a><span data-ttu-id="b8d01-104">Déployer Microsoft Defender pour point de terminaison Android via Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="b8d01-104">Deploy Microsoft Defender for Endpoint for Android with Microsoft Intune</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b8d01-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b8d01-105">**Applies to:**</span></span>
- [<span data-ttu-id="b8d01-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b8d01-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b8d01-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b8d01-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b8d01-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b8d01-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b8d01-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b8d01-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="b8d01-110">Découvrez comment déployer Defender pour endpoint pour Android sur les appareils inscrits au portail d’entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="b8d01-110">Learn how to deploy Defender for Endpoint for Android on Intune Company Portal enrolled devices.</span></span> <span data-ttu-id="b8d01-111">Pour plus d’informations sur l’inscription d’appareils Intune, voir [Inscrire votre appareil.](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal)</span><span class="sxs-lookup"><span data-stu-id="b8d01-111">For more information about Intune device enrollment, see  [Enroll your device](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal).</span></span>

> [!NOTE]
> <span data-ttu-id="b8d01-112">**Defender pour le point de terminaison pour Android est désormais disponible sur [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.scmx)**</span><span class="sxs-lookup"><span data-stu-id="b8d01-112">**Defender for Endpoint for Android is now available on [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.scmx)**</span></span> <br>
> <span data-ttu-id="b8d01-113">Vous pouvez vous connecter à Google Play à partir d’Intune pour déployer l’application Defender pour Endpoint sur les modes d’inscription Administrateur d’appareil et Android Entreprise.</span><span class="sxs-lookup"><span data-stu-id="b8d01-113">You can connect to Google Play from Intune to deploy Defender for Endpoint app across Device Administrator and Android Enterprise entrollment modes.</span></span>
<span data-ttu-id="b8d01-114">Les mises à jour de l’application sont automatiques via Google Play.</span><span class="sxs-lookup"><span data-stu-id="b8d01-114">Updates to the app are automatic via Google Play.</span></span>

## <a name="deploy-on-device-administrator-enrolled-devices"></a><span data-ttu-id="b8d01-115">Déployer sur les appareils inscrits à l’administrateur de périphérique</span><span class="sxs-lookup"><span data-stu-id="b8d01-115">Deploy on Device Administrator enrolled devices</span></span>

<span data-ttu-id="b8d01-116">**Deploy Defender for Endpoint for Android on Intune Company Portal - Device Administrator enrolled devices**</span><span class="sxs-lookup"><span data-stu-id="b8d01-116">**Deploy Defender for Endpoint for Android on Intune Company Portal - Device Administrator enrolled devices**</span></span>

<span data-ttu-id="b8d01-117">Découvrez comment déployer Defender pour endpoint pour Android sur le portail d’entreprise Intune - Appareils inscrits par l’administrateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b8d01-117">Learn how to deploy Defender for Endpoint for Android on Intune Company Portal - Device Administrator enrolled devices.</span></span> 

### <a name="add-as-android-store-app"></a><span data-ttu-id="b8d01-118">Ajouter en tant qu’application de l’Android Store</span><span class="sxs-lookup"><span data-stu-id="b8d01-118">Add as Android store app</span></span>

1. <span data-ttu-id="b8d01-119">Dans [le Centre d’administration Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431) sélectionnez **Applications** Android Apps Ajouter une application de la boutique \>  \> **\> Android** et **sélectionnez Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-119">In [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) , go to **Apps** \> **Android Apps** \> **Add \> Android store app** and choose **Select**.</span></span>

   ![Image du Centre d’administration Microsoft Endpoint Manager pour ajouter une application de l’Android Store](images/mda-addandroidstoreapp.png)

2. <span data-ttu-id="b8d01-121">Dans la page **Ajouter une** application et dans la section Informations sur *l’application,* entrez :</span><span class="sxs-lookup"><span data-stu-id="b8d01-121">On the **Add app** page and in the *App Information* section enter:</span></span> 

   - <span data-ttu-id="b8d01-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8d01-122">**Name**</span></span> 
   - <span data-ttu-id="b8d01-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8d01-123">**Description**</span></span>
   - <span data-ttu-id="b8d01-124">**Éditeur** en tant que Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8d01-124">**Publisher** as Microsoft.</span></span>
   - <span data-ttu-id="b8d01-125">**URL du Magasin d’applications** sous (URL du Google Play Store de l’application https://play.google.com/store/apps/details?id=com.microsoft.scmx Defender for Endpoint)</span><span class="sxs-lookup"><span data-stu-id="b8d01-125">**App store URL** as https://play.google.com/store/apps/details?id=com.microsoft.scmx (Defender for Endpoint app Google Play Store URL)</span></span> 

   <span data-ttu-id="b8d01-126">Les autres champs sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b8d01-126">Other fields are optional.</span></span> <span data-ttu-id="b8d01-127">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-127">Select **Next**.</span></span>

   ![Image du Centre d’administration Microsoft Endpoint Manager pour ajouter des informations sur l’application](images/mda-addappinfo.png)

3. <span data-ttu-id="b8d01-129">Dans la section *Affectations,* allez à la section **Obligatoire** et **sélectionnez Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-129">In the *Assignments* section, go to the **Required** section and select **Add group.**</span></span> <span data-ttu-id="b8d01-130">Vous pouvez ensuite choisir le ou les groupes d’utilisateurs que vous souhaitez cibler Defender pour l’application Endpoint pour Android.</span><span class="sxs-lookup"><span data-stu-id="b8d01-130">You can then choose the user group(s) that you would like to target Defender for Endpoint for Android app.</span></span> <span data-ttu-id="b8d01-131">Sélectionnez **Sélectionner,** puis **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-131">Choose **Select** and then **Next**.</span></span>

    >[!NOTE]
    ><span data-ttu-id="b8d01-132">Le groupe d’utilisateurs sélectionné doit être constitué d’utilisateurs inscrits à Intune.</span><span class="sxs-lookup"><span data-stu-id="b8d01-132">The selected user group should consist of Intune enrolled users.</span></span>

    > [!div class="mx-imgBorder"]

    > ![Image du Centre d’administration Microsoft Endpoint Manager sélectionné pour les groupes d’utilisateurs](images/363bf30f7d69a94db578e8af0ddd044b.png)

4. <span data-ttu-id="b8d01-134">Dans la section **Révision+Créer,** vérifiez que toutes les informations entrées sont correctes, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-134">In the **Review+Create** section, verify that all the information entered is correct and then select **Create**.</span></span>

    <span data-ttu-id="b8d01-135">Dans quelques instants, l’application Defender pour point de terminaison sera correctement créée et une notification s’affichera dans le coin supérieur droit de la page.</span><span class="sxs-lookup"><span data-stu-id="b8d01-135">In a few moments, the Defender for Endpoint app would be created successfully, and a notification would show up at the top-right corner of the page.</span></span>

    ![Image de la notification du Centre d’administration Microsoft Endpoint Manager de l’application de point de terminaison Defender](images/86cbe56f88bb6e93e9c63303397fc24f.png)

5. <span data-ttu-id="b8d01-137">Dans la page d’informations sur l’application  qui s’affiche, dans la **section** Moniteur, sélectionnez État de l’installation de l’appareil pour vérifier que l’installation de l’appareil s’est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="b8d01-137">In the app information page that is displayed, in the **Monitor** section, select **Device install status** to verify that the device installation has completed successfully.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-138">![Image de l’installation de l’appareil du Centre d’administration Microsoft Endpoint Manager](images/513cf5d59eaaef5d2b5bc122715b5844.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-138">![Image of Microsoft Endpoint Manager Admin Center device install](images/513cf5d59eaaef5d2b5bc122715b5844.png)</span></span>

### <a name="complete-onboarding-and-check-status"></a><span data-ttu-id="b8d01-139">Terminer l’intégration et vérifier l’état</span><span class="sxs-lookup"><span data-stu-id="b8d01-139">Complete onboarding and check status</span></span>

1. <span data-ttu-id="b8d01-140">Une fois Defender pour le point de terminaison pour Android installé sur l’appareil, vous verrez l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="b8d01-140">Once Defender for Endpoint for Android has been installed on the device, you'll see the app icon.</span></span>

    ![Icône sur l’appareil mobile](images/7cf9311ad676ec5142002a4d0c2323ca.jpg)

2. <span data-ttu-id="b8d01-142">Appuyez sur l’icône de l’application Microsoft Defender ATP et suivez les instructions à l’écran pour terminer l’intégration de l’application.</span><span class="sxs-lookup"><span data-stu-id="b8d01-142">Tap the Microsoft Defender ATP app icon and follow the on-screen instructions to complete onboarding the app.</span></span> <span data-ttu-id="b8d01-143">Les détails incluent l’acceptation par l’utilisateur final des autorisations Android requises par Defender pour Endpoint pour Android.</span><span class="sxs-lookup"><span data-stu-id="b8d01-143">The details include end-user acceptance of Android permissions required by Defender for Endpoint for Android.</span></span>

3. <span data-ttu-id="b8d01-144">Une fois l’intégration réussie, l’appareil commence à s’afficher dans la liste Appareils dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b8d01-144">Upon successful onboarding, the device will start showing up on the Devices list in Microsoft Defender Security Center.</span></span>

    ![Image de l’appareil dans le portail Defender for Endpoint](images/9fe378a1dce0f143005c3aa53d8c4f51.png)

## <a name="deploy-on-android-enterprise-enrolled-devices"></a><span data-ttu-id="b8d01-146">Déployer sur les appareils inscrits à Android Enterprise</span><span class="sxs-lookup"><span data-stu-id="b8d01-146">Deploy on Android Enterprise enrolled devices</span></span>

<span data-ttu-id="b8d01-147">Defender pour le point de terminaison pour Android prend en charge les appareils inscrits à Android Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b8d01-147">Defender for Endpoint for Android supports Android Enterprise enrolled devices.</span></span>

<span data-ttu-id="b8d01-148">Pour plus d’informations sur les options d’inscription pris en charge par Intune, voir [Options d’inscription.](https://docs.microsoft.com/mem/intune/enrollment/android-enroll)</span><span class="sxs-lookup"><span data-stu-id="b8d01-148">For more information on the enrollment options supported by Intune, see [Enrollment Options](https://docs.microsoft.com/mem/intune/enrollment/android-enroll).</span></span>

<span data-ttu-id="b8d01-149">**Actuellement, les appareils personnels avec profil de travail et les inscriptions d’appareils utilisateur entièrement gérées par l’entreprise sont pris en charge pour le déploiement.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-149">**Currently, Personally owned devices with work profile and Corporate-owned fully managed user device enrollments are supported for deployment.**</span></span>

## <a name="add-microsoft-defender-for-endpoint-for-android-as-a-managed-google-play-app"></a><span data-ttu-id="b8d01-150">Ajouter Microsoft Defender pour le point de terminaison pour Android en tant qu’application Google Play gérée</span><span class="sxs-lookup"><span data-stu-id="b8d01-150">Add Microsoft Defender for Endpoint for Android as a Managed Google Play app</span></span>

<span data-ttu-id="b8d01-151">Suivez les étapes ci-dessous pour ajouter l’application Microsoft Defender for Endpoint à votre Google Play géré.</span><span class="sxs-lookup"><span data-stu-id="b8d01-151">Follow the steps below to add Microsoft Defender for Endpoint app into your managed Google Play.</span></span>

1. <span data-ttu-id="b8d01-152">Dans [le Centre d’administration Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431) sélectionnez **Applications** \> **Android Apps** \> **Add** et **sélectionnez Application Google Play gérée.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-152">In [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) , go to **Apps** \> **Android Apps** \> **Add** and select **Managed Google Play app**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-153">![Image du centre d’administration Microsoft Endpoint Manager géré google play](images/579ff59f31f599414cedf63051628b2e.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-153">![Image of Microsoft Endpoint Manager admin center managed google play](images/579ff59f31f599414cedf63051628b2e.png)</span></span>

2. <span data-ttu-id="b8d01-154">Sur votre page Google Play gérée qui se charge par la suite, allez dans la zone de recherche et **recherchez Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-154">On your managed Google Play page that loads subsequently, go to the search box and lookup **Microsoft Defender.**</span></span> <span data-ttu-id="b8d01-155">Votre recherche doit afficher l’application Microsoft Defender for Endpoint dans votre Google Play géré.</span><span class="sxs-lookup"><span data-stu-id="b8d01-155">Your search should display the Microsoft Defender for Endpoint app in your Managed Google Play.</span></span> <span data-ttu-id="b8d01-156">Cliquez sur l’application Microsoft Defender pour le point de terminaison à partir du résultat de recherche Applications.</span><span class="sxs-lookup"><span data-stu-id="b8d01-156">Click on the Microsoft Defender for Endpoint app from the Apps search result.</span></span>

    ![Image de recherche des applications du Centre d’administration Microsoft Endpoint Manager](images/0f79cb37900b57c3e2bb0effad1c19cb.png)

3. <span data-ttu-id="b8d01-158">Dans la page de description de l’application qui arrive ensuite, vous devriez être en mesure de voir les détails de l’application sur Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b8d01-158">In the App description page that comes up next, you should be able to see app details on Defender for Endpoint.</span></span> <span data-ttu-id="b8d01-159">Examinez les informations sur la page, puis sélectionnez **Approuver.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-159">Review the information on the page and then select **Approve**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-160">![Capture d’écran d’un Google Play géré](images/07e6d4119f265037e3b80a20a73b856f.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-160">![A screenshot of a Managed Google Play](images/07e6d4119f265037e3b80a20a73b856f.png)</span></span>

4. <span data-ttu-id="b8d01-161">Les autorisations obtenues par Defender for Endpoint vous seront présentées pour qu’il fonctionne.</span><span class="sxs-lookup"><span data-stu-id="b8d01-161">You'll be presented with the permissions that Defender for Endpoint obtains for it to work.</span></span> <span data-ttu-id="b8d01-162">Examinez-les, puis sélectionnez **Approuver.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-162">Review them and then select **Approve**.</span></span>

    ![Capture d’écran de l’approbation de l’application d’aperçu defender pour point de terminaison](images/206b3d954f06cc58b3466fb7a0bd9f74.png)

5. <span data-ttu-id="b8d01-164">La page Paramètres d’approbation vous sera présentée.</span><span class="sxs-lookup"><span data-stu-id="b8d01-164">You'll be presented with the Approval settings page.</span></span> <span data-ttu-id="b8d01-165">La page confirme votre préférence pour gérer les nouvelles autorisations d’application que Defender pour endpoint pour Android peut demander.</span><span class="sxs-lookup"><span data-stu-id="b8d01-165">The page confirms your preference to handle new app permissions that Defender for Endpoint for Android might ask.</span></span> <span data-ttu-id="b8d01-166">Examinez les choix et sélectionnez votre option préférée.</span><span class="sxs-lookup"><span data-stu-id="b8d01-166">Review the choices and select your preferred option.</span></span> <span data-ttu-id="b8d01-167">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-167">Select **Done**.</span></span>

    <span data-ttu-id="b8d01-168">Par défaut, Google Play géré sélectionne *Conserver approuvé lorsque l’application demande de nouvelles autorisations*</span><span class="sxs-lookup"><span data-stu-id="b8d01-168">By default, managed Google Play selects *Keep approved when app requests new permissions*</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-169">![Image de l’onglet Notifications](images/ffecfdda1c4df14148f1526c22cc0236.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-169">![Image of notifications tab](images/ffecfdda1c4df14148f1526c22cc0236.png)</span></span>

6. <span data-ttu-id="b8d01-170">Après avoir sélectionné la gestion des autorisations, sélectionnez **Synchroniser** pour synchroniser Microsoft Defender pour le point de terminaison avec votre liste d’applications.</span><span class="sxs-lookup"><span data-stu-id="b8d01-170">After the permissions handling selection is made, select **Sync** to sync Microsoft Defender for Endpoint to your apps list.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-171">![Image de la page de synchronisation](images/34e6b9a0dae125d085c84593140180ed.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-171">![Image of sync page](images/34e6b9a0dae125d085c84593140180ed.png)</span></span>

7. <span data-ttu-id="b8d01-172">La synchronisation se terminera dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="b8d01-172">The sync will complete in a few minutes.</span></span>

    ![Image de l’application Android](images/9fc07ffc150171f169dc6e57fe6f1c74.png)

8. <span data-ttu-id="b8d01-174">Sélectionnez **le bouton** Actualiser dans l’écran des applications Android et Microsoft Defender ATP doit être visible dans la liste des applications.</span><span class="sxs-lookup"><span data-stu-id="b8d01-174">Select the **Refresh** button in the Android apps screen and Microsoft Defender ATP should be visible in the apps list.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-175">![Image de la liste des applications Android](images/fa4ac18a6333335db3775630b8e6b353.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-175">![Image of list of Android apps](images/fa4ac18a6333335db3775630b8e6b353.png)</span></span>

9. <span data-ttu-id="b8d01-176">Defender pour le point de terminaison prend en charge les stratégies de configuration d’application pour les appareils gérés via Intune.</span><span class="sxs-lookup"><span data-stu-id="b8d01-176">Defender for Endpoint supports App configuration policies for managed devices via Intune.</span></span> <span data-ttu-id="b8d01-177">Cette fonctionnalité peut être mise à profit pour obtenir automatiquement les autorisations Android applicables, de sorte que l’utilisateur final n’a pas besoin d’accepter ces autorisations.</span><span class="sxs-lookup"><span data-stu-id="b8d01-177">This capability can be leveraged to autogrant applicable Android permission(s), so the end user does not need to accept these permission(s).</span></span>

    1. <span data-ttu-id="b8d01-178">Dans la page **Applications,** go to **Policy > App configuration policies > Add > Managed devices**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-178">In the **Apps** page, go to **Policy > App configuration policies > Add > Managed devices**.</span></span>

       ![Image des appareils gérés Android du Centre d’administration Microsoft Endpoint Manager](images/android-mem.png)

    1. <span data-ttu-id="b8d01-180">Dans la page **Créer une stratégie de configuration d’application,** entrez les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="b8d01-180">In the **Create app configuration policy** page, enter the following details:</span></span>
    
        - <span data-ttu-id="b8d01-181">Nom : Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="b8d01-181">Name: Microsoft Defender ATP.</span></span>
        - <span data-ttu-id="b8d01-182">Choisissez **Android Entreprise comme** plateforme.</span><span class="sxs-lookup"><span data-stu-id="b8d01-182">Choose **Android Enterprise** as platform.</span></span>
        - <span data-ttu-id="b8d01-183">Choisissez **Profil de travail uniquement en** tant que type de profil.</span><span class="sxs-lookup"><span data-stu-id="b8d01-183">Choose **Work Profile only** as Profile Type.</span></span>
        - <span data-ttu-id="b8d01-184">Cliquez **sur Sélectionner l’application,** choisissez Microsoft Defender **ATP,** **sélectionnez OK,** puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-184">Click **Select App**, choose **Microsoft Defender ATP**, select **OK** and then **Next**.</span></span>
    
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b8d01-185">![Image de la page créer une stratégie de configuration d’application](images/android-create-app.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-185">![Image of create app configuration policy page](images/android-create-app.png)</span></span>

    1. <span data-ttu-id="b8d01-186">Dans la page **Paramètres,** cliquez sur Ajouter pour afficher la liste des autorisations prise en charge dans la section Autorisations.</span><span class="sxs-lookup"><span data-stu-id="b8d01-186">In the **Settings** page, go to the Permissions section click on Add to view the list of supported permissions.</span></span> <span data-ttu-id="b8d01-187">Dans la section Ajouter des autorisations, sélectionnez les autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8d01-187">In the Add Permissions section, select the following permissions:</span></span>

       - <span data-ttu-id="b8d01-188">Stockage externe (lecture)</span><span class="sxs-lookup"><span data-stu-id="b8d01-188">External storage (read)</span></span>
       - <span data-ttu-id="b8d01-189">Stockage externe (écriture)</span><span class="sxs-lookup"><span data-stu-id="b8d01-189">External storage (write)</span></span>

       <span data-ttu-id="b8d01-190">Puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-190">Then select **OK**.</span></span>

       > [!div class="mx-imgBorder"]
      > <span data-ttu-id="b8d01-191">![Image de la stratégie de configuration de création d’application Android](images/android-create-app-config.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-191">![Image of android create app configuration policy](images/android-create-app-config.png)</span></span>

    1. <span data-ttu-id="b8d01-192">Vous devez maintenant voir les autorisations répertoriées et maintenant vous pouvezgrant  automatiquement à la fois en choisissant legrant automatique dans la liste d’état d’autorisation, puis en sélectionnant **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-192">You should now see both the permissions listed and now you can autogrant both by choosing autogrant in the **Permission state** drop-down and then select **Next**.</span></span>

       > [!div class="mx-imgBorder"]
       > <span data-ttu-id="b8d01-193">![Image de la stratégie de configuration de création d’application pour l’octroi automatique Android](images/android-auto-grant.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-193">![Image of android auto grant create app configuration policy](images/android-auto-grant.png)</span></span>

    1. <span data-ttu-id="b8d01-194">Dans la page **Affectations,** sélectionnez le groupe d’utilisateurs auquel cette stratégie de config d’application sera affectée.</span><span class="sxs-lookup"><span data-stu-id="b8d01-194">In the **Assignments** page, select the user group to which this app config policy would be assigned to.</span></span> <span data-ttu-id="b8d01-195">Cliquez **sur Sélectionner les groupes à inclure,** puis sélectionnez le groupe applicable, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-195">Click **Select groups to include** and selecting the applicable group and then selecting **Next**.</span></span>  <span data-ttu-id="b8d01-196">Le groupe sélectionné ici est généralement le même groupe que celui auquel vous affecteriez l’application Microsoft Defender pour Endpoint Android.</span><span class="sxs-lookup"><span data-stu-id="b8d01-196">The group selected here is usually the same group to which you would assign Microsoft Defender for Endpoint Android app.</span></span> 

       > [!div class="mx-imgBorder"]
       > <span data-ttu-id="b8d01-197">![Image de la stratégie de création de configuration d’application](images/android-select-group.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-197">![Image of the create app configuration policy](images/android-select-group.png)</span></span>
    

     1. <span data-ttu-id="b8d01-198">Dans la page **Révision + Créer** qui arrive ensuite, examinez toutes les informations, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-198">In the **Review + Create** page that comes up next, review all the information and then select **Create**.</span></span> <br>
    
        <span data-ttu-id="b8d01-199">La stratégie de configuration d’application pour Defender for Endpoint autogranting l’autorisation de stockage est désormais attribuée au groupe d’utilisateurs sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b8d01-199">The app configuration policy for Defender for Endpoint autogranting the storage permission is now assigned to the selected user group.</span></span>

        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="b8d01-200">![Image de la révision Android pour créer une stratégie de config d’application](images/android-review-create.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-200">![Image of android review create app config policy](images/android-review-create.png)</span></span>


10. <span data-ttu-id="b8d01-201">Sélectionnez **l’application Microsoft Defender ATP** dans la liste \> **Propriétés** modifier les \> **affectations.** \> </span><span class="sxs-lookup"><span data-stu-id="b8d01-201">Select **Microsoft Defender ATP** app in the list \> **Properties** \> **Assignments** \> **Edit**.</span></span>

    ![Image de la liste des applications](images/mda-properties.png)


11. <span data-ttu-id="b8d01-203">Affectez l’application en *tant qu’application obligatoire* à un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b8d01-203">Assign the app as a *Required* app to a user group.</span></span> <span data-ttu-id="b8d01-204">Il est automatiquement installé  dans le profil de travail lors de la synchronisation suivante de l’appareil via l’application Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b8d01-204">It is automatically installed in the *work profile* during the next sync of the device via Company Portal app.</span></span> <span data-ttu-id="b8d01-205">Cette affectation peut être effectuée en naviguant vers la section *Obligatoire* Ajouter un groupe, en sélectionnant le groupe d’utilisateurs, \>  puis en cliquant sur **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-205">This assignment can be done by navigating to the *Required* section \> **Add group,** selecting the user group and click **Select**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-206">![Image de la page modifier l’application](images/ea06643280075f16265a596fb9a96042.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-206">![Image of edit application page](images/ea06643280075f16265a596fb9a96042.png)</span></span>


12. <span data-ttu-id="b8d01-207">Dans la page **Modifier l’application,** examinez toutes les informations entrées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b8d01-207">In the **Edit Application** page, review all the information that was entered above.</span></span> <span data-ttu-id="b8d01-208">Sélectionnez **Ensuite Révision + Enregistrer,** puis **Réessoy pour** commencer l’affectation.</span><span class="sxs-lookup"><span data-stu-id="b8d01-208">Then select **Review + Save** and then **Save** again to commence assignment.</span></span>

### <a name="auto-setup-of-always-on-vpn"></a><span data-ttu-id="b8d01-209">Configuration automatique du VPN toujours en service</span><span class="sxs-lookup"><span data-stu-id="b8d01-209">Auto Setup of Always-on VPN</span></span> 
<span data-ttu-id="b8d01-210">Defender pour le point de terminaison prend en charge les stratégies de configuration des appareils gérés via Intune.</span><span class="sxs-lookup"><span data-stu-id="b8d01-210">Defender for Endpoint supports Device configuration policies for managed devices via Intune.</span></span> <span data-ttu-id="b8d01-211">Cette fonctionnalité peut être mise à profit pour la configuration automatique du **VPN** toujours connecté sur les appareils inscrits à Android Enterprise, de sorte que l’utilisateur final n’a pas besoin de configurer le service VPN lors de l’intégration.</span><span class="sxs-lookup"><span data-stu-id="b8d01-211">This capability can be leveraged to **Auto setup of Always-on VPN** on Android Enterprise enrolled devices, so the end user does not need to set up VPN service while onboarding.</span></span>
1.  <span data-ttu-id="b8d01-212">Sur **les appareils,** sélectionnez **Profils** de configuration Créer une plateforme de profil Android Enterprise Sélectionner des restrictions d’appareil sous l’une des conditions  >    >    >   **suivantes,** en fonction du type d’inscription de votre appareil</span><span class="sxs-lookup"><span data-stu-id="b8d01-212">On **Devices**, select **Configuration Profiles** > **Create Profile** > **Platform** > **Android Enterprise** Select **Device restrictions** under one of the following, based on your device enrollment type</span></span> 
- <span data-ttu-id="b8d01-213">**Profil de travail entièrement géré, dédié Corporate-Owned travail**</span><span class="sxs-lookup"><span data-stu-id="b8d01-213">**Fully Managed, Dedicated, and Corporate-Owned Work Profile**</span></span>
- <span data-ttu-id="b8d01-214">**Profil de travail personnel**</span><span class="sxs-lookup"><span data-stu-id="b8d01-214">**Personally owned Work Profile**</span></span>

<span data-ttu-id="b8d01-215">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-215">Select **Create**.</span></span>
 
   > ![Image du profil de configuration des appareils Créer](images/1autosetupofvpn.png)
    
2. <span data-ttu-id="b8d01-217">**Paramètres de configuration** Fournissez **un nom et** une description **pour** identifier le profil de configuration de manière unique.</span><span class="sxs-lookup"><span data-stu-id="b8d01-217">**Configuration Settings** Provide a **Name** and a **Description** to uniquely identify the configuration profile.</span></span> 

   > ![Image du nom et de la description du profil de configuration des appareils](images/2autosetupofvpn.png)
   
 3. <span data-ttu-id="b8d01-219">Sélectionnez **Connectivité et** configurez vpn :</span><span class="sxs-lookup"><span data-stu-id="b8d01-219">Select **Connectivity** and configure VPN:</span></span>
- <span data-ttu-id="b8d01-220">Activez **le programme d’installation VPN** toujours activé pour un client VPN dans le profil professionnel afin de vous connecter et de vous reconnecter automatiquement au VPN dès que possible.</span><span class="sxs-lookup"><span data-stu-id="b8d01-220">Enable **Always-on VPN** Setup a VPN client in the work profile to automatically connect and reconnect to the VPN whenever possible.</span></span> <span data-ttu-id="b8d01-221">Un seul client VPN peut être configuré pour un VPN toujours connecté sur un appareil donné. Assurez-vous donc de n’avoir qu’une seule stratégie VPN toujours en service déployée sur un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="b8d01-221">Only one VPN client can be configured for always-on VPN on a given device, so be sure to have no more than one always-on VPN policy deployed to a single device.</span></span> 
- <span data-ttu-id="b8d01-222">Select **Custom** in VPN client dropdown list Custom VPN in this case is Defender for Endpoint VPN which is used to provide the Web Protection feature.</span><span class="sxs-lookup"><span data-stu-id="b8d01-222">Select **Custom** in VPN client dropdown list Custom VPN in this case is Defender for Endpoint VPN which is used to provide the Web Protection feature.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="b8d01-223">L’application Microsoft Defender ATP doit être installée sur l’appareil de l’utilisateur, pour que la configuration automatique de ce VPN fonctionne.</span><span class="sxs-lookup"><span data-stu-id="b8d01-223">Microsoft Defender ATP app must be installed on user’s device, in order to functioning of auto setup of this VPN.</span></span>

- <span data-ttu-id="b8d01-224">Entrez **l’ID de package** de l’application Microsoft Defender ATP dans le Google Play Store.</span><span class="sxs-lookup"><span data-stu-id="b8d01-224">Enter **Package ID** of the Microsoft Defender ATP app in Google Play store.</span></span> <span data-ttu-id="b8d01-225">Pour l’URL de l’application https://play.google.com/store/apps/details?id=com.microsoft.scmx Defender, l’ID de package **est com.microsoft.scmx**</span><span class="sxs-lookup"><span data-stu-id="b8d01-225">For the Defender app URL https://play.google.com/store/apps/details?id=com.microsoft.scmx, Package ID is **com.microsoft.scmx**</span></span>  
- <span data-ttu-id="b8d01-226">**Mode verrouillage** Non configuré (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="b8d01-226">**Lockdown mode** Not configured (Default)</span></span> 

     ![Image du profil de configuration des appareils qui activent vpn toujours activé](images/3autosetupofvpn.png)
   
4. <span data-ttu-id="b8d01-228">**Affectation** Dans la page  **Affectations,** sélectionnez le groupe d’utilisateurs auquel cette stratégie de config d’application   sera affectée.</span><span class="sxs-lookup"><span data-stu-id="b8d01-228">**Assignment** In the **Assignments** page, select the user group to which this app config policy would be assigned to.</span></span> <span data-ttu-id="b8d01-229">Cliquez **sur Sélectionner les** groupes à inclure et en sélectionnant le groupe applicable, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b8d01-229">Click **Select groups** to include and selecting the applicable group and then click **Next**.</span></span> <span data-ttu-id="b8d01-230">Le groupe sélectionné ici est généralement le même groupe que celui auquel vous affecteriez l’application Microsoft Defender pour Endpoint Android.</span><span class="sxs-lookup"><span data-stu-id="b8d01-230">The group selected here is usually the same group to which you would assign Microsoft Defender for Endpoint Android app.</span></span> 

     ![Image de l’affectation du profil de configuration des appareils](images/4autosetupofvpn.png)

5. <span data-ttu-id="b8d01-232">Dans la page **Révision + Créer** qui arrive ensuite, examinez toutes les informations, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-232">In the **Review + Create** page that comes up next, review all the information and then select **Create**.</span></span> <span data-ttu-id="b8d01-233">Le profil de configuration de l’appareil est maintenant affecté au groupe d’utilisateurs sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b8d01-233">The device configuration profile is now assigned to the selected user group.</span></span>    

    ![Image de la révision et de la création du profil de configuration des appareils](images/5autosetupofvpn.png)

## <a name="complete-onboarding-and-check-status"></a><span data-ttu-id="b8d01-235">Terminer l’intégration et vérifier l’état</span><span class="sxs-lookup"><span data-stu-id="b8d01-235">Complete onboarding and check status</span></span>

1. <span data-ttu-id="b8d01-236">Confirmez l’état d’installation de Microsoft Defender pour le point de terminaison pour Android en cliquant sur l’état **d’installation de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-236">Confirm the installation status of Microsoft Defender for Endpoint for Android by clicking on the **Device Install Status**.</span></span> <span data-ttu-id="b8d01-237">Vérifiez que l’appareil s’affiche ici.</span><span class="sxs-lookup"><span data-stu-id="b8d01-237">Verify that the device is displayed here.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="b8d01-238">![Image de l’état d’installation de l’appareil](images/900c0197aa59f9b7abd762ab2b32e80c.png)</span><span class="sxs-lookup"><span data-stu-id="b8d01-238">![Image of device installation status](images/900c0197aa59f9b7abd762ab2b32e80c.png)</span></span>


2. <span data-ttu-id="b8d01-239">Sur l’appareil, vous pouvez valider l’état d’intégration en allant au **profil professionnel.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-239">On the device, you can validate the onboarding status by going to the **work profile**.</span></span> <span data-ttu-id="b8d01-240">Confirmez que Defender pour le point de terminaison est disponible et que vous êtes inscrit sur les appareils personnels **avec profil de travail.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-240">Confirm that Defender for Endpoint is available and that you are enrolled to the **Personally owned devices with work profile**.</span></span>  <span data-ttu-id="b8d01-241">Si vous êtes inscrit à un appareil utilisateur entièrement géré par l’entreprise, vous disposez d’un profil unique sur l’appareil où vous pouvez confirmer que Defender pour le point de terminaison est disponible.</span><span class="sxs-lookup"><span data-stu-id="b8d01-241">If you are enrolled to a **Corporate-owned, fully managed user device**, you will have a single profile on the device where you can confirm that Defender for Endpoint is available.</span></span>

    ![Image de l’application sur un appareil mobile](images/c2e647fc8fa31c4f2349c76f2497bc0e.png)

3. <span data-ttu-id="b8d01-243">Lorsque l’application est installée, ouvrez l’application et acceptez les autorisations, puis votre intégration doit réussir.</span><span class="sxs-lookup"><span data-stu-id="b8d01-243">When the app is installed, open the app and accept the permissions and then your onboarding should be successful.</span></span>

    ![Image de l’appareil mobile avec l’application Microsoft Defender pour le point de terminaison](images/mda-devicesafe.png)

4. <span data-ttu-id="b8d01-245">À ce stade, l’appareil est correctement intégré à Defender for Endpoint pour Android.</span><span class="sxs-lookup"><span data-stu-id="b8d01-245">At this stage the device is successfully onboarded onto Defender for Endpoint for Android.</span></span> <span data-ttu-id="b8d01-246">Vous pouvez le vérifier dans le Centre de sécurité [Microsoft Defender](https://securitycenter.microsoft.com) en naviguant vers la page **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="b8d01-246">You can verify this on the [Microsoft Defender Security Center](https://securitycenter.microsoft.com) by navigating to the **Devices** page.</span></span>

    ![Image du portail Microsoft Defender pour les points de terminaison](images/9fe378a1dce0f143005c3aa53d8c4f51.png)


## <a name="related-topics"></a><span data-ttu-id="b8d01-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8d01-248">Related topics</span></span>
- [<span data-ttu-id="b8d01-249">Vue d’ensemble de Microsoft Defender pour point de terminaison Android</span><span class="sxs-lookup"><span data-stu-id="b8d01-249">Overview of Microsoft Defender for Endpoint for Android</span></span>](microsoft-defender-endpoint-android.md)
- [<span data-ttu-id="b8d01-250">Configurer Microsoft Defender pour point de terminaison pour des fonctionnalités Android</span><span class="sxs-lookup"><span data-stu-id="b8d01-250">Configure Microsoft Defender for Endpoint for Android features</span></span>](android-configure.md)
