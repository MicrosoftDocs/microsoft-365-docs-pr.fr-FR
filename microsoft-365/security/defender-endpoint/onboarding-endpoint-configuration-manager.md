---
title: Intégration à l’aide de Microsoft Endpoint Configuration Manager
description: Découvrez comment intégrer Microsoft Defender pour endpoint à l’aide de Microsoft Endpoint Configuration Manager
keywords: intégration, configuration, déploiement, déploiement, gestionnaire de configuration de point de terminaison, mdatp, protection avancée contre les menaces, création de collections, réponse de détection de point de terminaison, protection nouvelle génération, réduction de la surface d’attaque, gestionnaire de configuration de point de terminaison Microsoft
search.product: eADQiWindows 10XVcnh
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
- M365-security-compliance
- m365solution-endpointprotect
- m365solution-scenario
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 31c946ccad84aca3b2fc86c95655cea9e66e182f
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186400"
---
# <a name="onboarding-using-microsoft-endpoint-configuration-manager"></a><span data-ttu-id="004c7-104">Intégration à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="004c7-104">Onboarding using Microsoft Endpoint Configuration Manager</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="004c7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="004c7-105">**Applies to:**</span></span>
- [<span data-ttu-id="004c7-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c7-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="004c7-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="004c7-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="004c7-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="004c7-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="004c7-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="004c7-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="004c7-110">Cet article fait partie du guide de déploiement et agit comme un exemple de méthode d’intégration.</span><span class="sxs-lookup"><span data-stu-id="004c7-110">This article is part of the Deployment guide and acts as an example onboarding method.</span></span> 

<span data-ttu-id="004c7-111">Dans la [rubrique Planification,](deployment-strategy.md) plusieurs méthodes ont été fournies pour intégrer des appareils au service.</span><span class="sxs-lookup"><span data-stu-id="004c7-111">In the [Planning](deployment-strategy.md) topic, there were several methods provided to onboard devices to the service.</span></span> <span data-ttu-id="004c7-112">Cette rubrique traite de l’architecture de cogestion.</span><span class="sxs-lookup"><span data-stu-id="004c7-112">This topic covers the co-management architecture.</span></span> 

<span data-ttu-id="004c7-113">![Image de l’architecture native du cloud ](images/co-management-architecture.png)
 *Diagramme des architectures d’environnement*</span><span class="sxs-lookup"><span data-stu-id="004c7-113">![Image of cloud-native architecture](images/co-management-architecture.png)
*Diagram of environment architectures*</span></span>


<span data-ttu-id="004c7-114">Bien que Defender pour point de terminaison prend en charge l’intégration de différents points de terminaison et outils, cet article ne les traite pas.</span><span class="sxs-lookup"><span data-stu-id="004c7-114">While Defender for Endpoint supports onboarding of various endpoints and tools, this article does not cover them.</span></span> <span data-ttu-id="004c7-115">Pour plus d’informations sur l’intégration générale à l’aide d’autres outils et méthodes de déploiement pris en charge, voir [vue d’ensemble de l’intégration.](onboarding.md)</span><span class="sxs-lookup"><span data-stu-id="004c7-115">For information on general onboarding using other supported deployment tools and methods, see [Onboarding overview](onboarding.md).</span></span>



<span data-ttu-id="004c7-116">Cette rubrique guide les utilisateurs dans :</span><span class="sxs-lookup"><span data-stu-id="004c7-116">This topic guides users in:</span></span>
- <span data-ttu-id="004c7-117">Étape 1 : intégration d’appareils Windows au service</span><span class="sxs-lookup"><span data-stu-id="004c7-117">Step 1: Onboarding Windows devices to the service</span></span> 
- <span data-ttu-id="004c7-118">Étape 2 : Configuration de Defender pour les fonctionnalités de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c7-118">Step 2: Configuring Defender for Endpoint capabilities</span></span>

<span data-ttu-id="004c7-119">Ces instructions d’intégration vous guident tout au long des étapes de base suivantes que vous devez suivre lors de l’utilisation de Microsoft Endpoint Configuration Manager :</span><span class="sxs-lookup"><span data-stu-id="004c7-119">This onboarding guidance will walk you through the following basic steps that you need to take when using Microsoft Endpoint Configuration Manager:</span></span>
- <span data-ttu-id="004c7-120">**Création d’une collection dans Microsoft Endpoint Configuration Manager**</span><span class="sxs-lookup"><span data-stu-id="004c7-120">**Creating a collection in Microsoft Endpoint Configuration Manager**</span></span>
- <span data-ttu-id="004c7-121">**Configuration des fonctionnalités de Microsoft Defender pour les points de terminaison à l’aide de Microsoft Endpoint Configuration Manager**</span><span class="sxs-lookup"><span data-stu-id="004c7-121">**Configuring Microsoft Defender for Endpoint capabilities using Microsoft Endpoint Configuration Manager**</span></span>

>[!NOTE]
><span data-ttu-id="004c7-122">Seuls les appareils Windows sont couverts dans cet exemple de déploiement.</span><span class="sxs-lookup"><span data-stu-id="004c7-122">Only Windows devices are covered in this example deployment.</span></span> 



## <a name="step-1-onboard-windows-devices-using-microsoft-endpoint-configuration-manager"></a><span data-ttu-id="004c7-123">Étape 1 : Intégrer des appareils Windows à l’aide de Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="004c7-123">Step 1: Onboard Windows devices using Microsoft Endpoint Configuration Manager</span></span>

### <a name="collection-creation"></a><span data-ttu-id="004c7-124">Création de collection</span><span class="sxs-lookup"><span data-stu-id="004c7-124">Collection creation</span></span>
<span data-ttu-id="004c7-125">Pour intégrer des appareils Windows 10 avec Microsoft Endpoint Configuration Manager, le déploiement peut cibler une collection existante ou une nouvelle collection peut être créée pour les tests.</span><span class="sxs-lookup"><span data-stu-id="004c7-125">To onboard Windows 10 devices with Microsoft Endpoint Configuration Manager, the deployment can target an existing collection or a new collection can be created for testing.</span></span> 

<span data-ttu-id="004c7-126">L’intégration à l’aide d’outils tels que la stratégie de groupe ou la méthode manuelle n’installe aucun agent sur le système.</span><span class="sxs-lookup"><span data-stu-id="004c7-126">Onboarding using tools such as Group policy or manual method does not install any agent on the system.</span></span> 

<span data-ttu-id="004c7-127">Dans la console Microsoft Endpoint Configuration Manager, le processus d’intégration est configuré dans le cadre des paramètres de conformité au sein de la console.</span><span class="sxs-lookup"><span data-stu-id="004c7-127">Within the Microsoft Endpoint Configuration Manager console the onboarding process will be configured as part of the compliance settings within the console.</span></span>

<span data-ttu-id="004c7-128">Tout système qui reçoit cette configuration requise conserve cette configuration tant que le client Configuration Manager continue de recevoir cette stratégie à partir du point de gestion.</span><span class="sxs-lookup"><span data-stu-id="004c7-128">Any system that receives this required configuration will maintain that configuration for as long as the Configuration Manager client continues to receive this policy from the management point.</span></span> 

<span data-ttu-id="004c7-129">Suivez les étapes ci-dessous pour intégrer des points de terminaison à l’aide de Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="004c7-129">Follow the steps below to onboard endpoints using Microsoft Endpoint Configuration Manager.</span></span>

1. <span data-ttu-id="004c7-130">Dans la console Microsoft Endpoint Configuration Manager, accédez à **Assets and Compliance \> Overview Device \> Collections**.</span><span class="sxs-lookup"><span data-stu-id="004c7-130">In Microsoft Endpoint Configuration Manager console, navigate to **Assets and Compliance \> Overview \> Device Collections**.</span></span>            

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager1](images/configmgr-device-collections.png)

2. <span data-ttu-id="004c7-132">Cliquez avec le bouton **droit sur La collection d’appareils,** puis **sélectionnez Créer une collection d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="004c7-132">Right Click **Device Collection** and select **Create Device Collection**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager2](images/configmgr-create-device-collection.png)

3. <span data-ttu-id="004c7-134">Fournissez **un nom** et **limitez la collection,** puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-134">Provide a **Name** and **Limiting Collection**, then select **Next**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager3](images/configmgr-limiting-collection.png)

4. <span data-ttu-id="004c7-136">Sélectionnez **Ajouter une règle** et choisissez Règle de **requête.**</span><span class="sxs-lookup"><span data-stu-id="004c7-136">Select **Add Rule** and choose **Query Rule**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager4](images/configmgr-query-rule.png)

5.  <span data-ttu-id="004c7-138">Cliquez **sur Suivant** dans **l’Assistant Adhésion directe** et cliquez sur Modifier **l’instruction de requête.**</span><span class="sxs-lookup"><span data-stu-id="004c7-138">Click **Next** on the **Direct Membership Wizard** and click on **Edit Query Statement**.</span></span>

     ![Image de l’Assistant Microsoft Endpoint Configuration Manager5](images/configmgr-direct-membership.png)

6. <span data-ttu-id="004c7-140">Sélectionnez **Critères,** puis sélectionnez l’icône étoile.</span><span class="sxs-lookup"><span data-stu-id="004c7-140">Select **Criteria** and then choose the star icon.</span></span>

     ![Image de l’Assistant Microsoft Endpoint Configuration Manager6](images/configmgr-criteria.png)

7. <span data-ttu-id="004c7-142">Conservez le type de critère comme **valeur simple,**  choisissez où en tant que système d’exploitation - numéro de **build**, opérateur supérieur ou égal à et valeur **14393** et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="004c7-142">Keep criterion type as **simple value**, choose where as **Operating System - build number**, operator as **is greater than or equal to** and value **14393** and click on **OK**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager7](images/configmgr-simple-value.png)

8. <span data-ttu-id="004c7-144">Sélectionnez **Suivant** et **Fermez.**</span><span class="sxs-lookup"><span data-stu-id="004c7-144">Select **Next** and **Close**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager8](images/configmgr-membership-rules.png)

9. <span data-ttu-id="004c7-146">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-146">Select **Next**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager9](images/configmgr-confirm.png)


<span data-ttu-id="004c7-148">Après avoir effectué cette tâche, vous avez maintenant une collection d’appareils avec tous les points de terminaison Windows 10 dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="004c7-148">After completing this task, you now have a device collection with all the Windows 10 endpoints in the environment.</span></span> 


## <a name="step-2-configure-microsoft-defender-for-endpoint-capabilities"></a><span data-ttu-id="004c7-149">Étape 2 : Configurer Microsoft Defender pour les fonctionnalités de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c7-149">Step 2: Configure Microsoft Defender for Endpoint capabilities</span></span> 
<span data-ttu-id="004c7-150">Cette section vous guide dans la configuration des fonctionnalités suivantes à l’aide de Microsoft Endpoint Configuration Manager sur les appareils Windows :</span><span class="sxs-lookup"><span data-stu-id="004c7-150">This section guides you in configuring the following capabilities using Microsoft Endpoint Configuration Manager on Windows devices:</span></span>

- [<span data-ttu-id="004c7-151">**Détection et réponse des points de terminaison**</span><span class="sxs-lookup"><span data-stu-id="004c7-151">**Endpoint detection and response**</span></span>](#endpoint-detection-and-response)
- [<span data-ttu-id="004c7-152">**Protection nouvelle génération**</span><span class="sxs-lookup"><span data-stu-id="004c7-152">**Next-generation protection**</span></span>](#next-generation-protection)
- [<span data-ttu-id="004c7-153">**Réduction de la surface d’attaque**</span><span class="sxs-lookup"><span data-stu-id="004c7-153">**Attack surface reduction**</span></span>](#attack-surface-reduction)


### <a name="endpoint-detection-and-response"></a><span data-ttu-id="004c7-154">Détection et réponse au point de terminaison</span><span class="sxs-lookup"><span data-stu-id="004c7-154">Endpoint detection and response</span></span>
#### <a name="windows-10"></a><span data-ttu-id="004c7-155">Windows 10</span><span class="sxs-lookup"><span data-stu-id="004c7-155">Windows 10</span></span>
<span data-ttu-id="004c7-156">À partir du Centre de sécurité Microsoft Defender, il est possible de télécharger la stratégie « .onboarding » qui peut être utilisée pour créer la stratégie dans System Center Configuration Manager et déployer cette stratégie sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="004c7-156">From within the Microsoft Defender Security Center it is possible to download the '.onboarding' policy that can be used to create the policy in System Center Configuration Manager and deploy that policy to Windows 10 devices.</span></span>

1. <span data-ttu-id="004c7-157">À partir d’un portail centre de sécurité Microsoft Defender, [sélectionnez Paramètres, puis Intégration.](https://securitycenter.windows.com/preferences2/onboarding)</span><span class="sxs-lookup"><span data-stu-id="004c7-157">From a Microsoft Defender Security Center Portal, select [Settings and then Onboarding](https://securitycenter.windows.com/preferences2/onboarding).</span></span>



2. <span data-ttu-id="004c7-158">Sous Méthode de déploiement, sélectionnez la version prise en charge **de Microsoft Endpoint Configuration Manager.**</span><span class="sxs-lookup"><span data-stu-id="004c7-158">Under Deployment method select the supported version of **Microsoft Endpoint Configuration Manager**.</span></span>

    ![Image de l’Assistant Intégration de Microsoft Defender pour les points de terminaison10](images/mdatp-onboarding-wizard.png)

3. <span data-ttu-id="004c7-160">Sélectionnez **le package de téléchargement.**</span><span class="sxs-lookup"><span data-stu-id="004c7-160">Select **Download package**.</span></span>

    ![Image de l’Assistant Intégration de Microsoft Defender pour les points de terminaison11](images/mdatp-download-package.png)

4. <span data-ttu-id="004c7-162">Enregistrez le package dans un emplacement accessible.</span><span class="sxs-lookup"><span data-stu-id="004c7-162">Save the package to an accessible location.</span></span>
5. <span data-ttu-id="004c7-163">Dans Microsoft Endpoint Configuration Manager, accédez à : **Assets and Compliance > Overview > Endpoint Protection > Microsoft Defender ATP Policies**.</span><span class="sxs-lookup"><span data-stu-id="004c7-163">In  Microsoft Endpoint Configuration Manager, navigate to: **Assets and Compliance > Overview > Endpoint Protection > Microsoft Defender ATP Policies**.</span></span>

6. <span data-ttu-id="004c7-164">Cliquez avec le bouton **droit sur Stratégies Microsoft Defender ATP** et **sélectionnez Créer une stratégie Microsoft Defender ATP.**</span><span class="sxs-lookup"><span data-stu-id="004c7-164">Right-click **Microsoft Defender ATP Policies** and select **Create Microsoft Defender ATP Policy**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager12](images/configmgr-create-policy.png)

7. <span data-ttu-id="004c7-166">Entrez le nom et la description, vérifiez **que l’intégration** est sélectionnée, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-166">Enter the name and description, verify **Onboarding** is selected, then select **Next**.</span></span>

    ![Image de l’Assistant Microsoft Endpoint Configuration Manager13](images/configmgr-policy-name.png)


8. <span data-ttu-id="004c7-168">Cliquez sur **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="004c7-168">Click **Browse**.</span></span>

9. <span data-ttu-id="004c7-169">Accédez à l’emplacement du fichier téléchargé à l’étape 4 ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="004c7-169">Navigate to the location of the downloaded file from step 4 above.</span></span>

10. <span data-ttu-id="004c7-170">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-170">Click **Next**.</span></span>
11. <span data-ttu-id="004c7-171">Configurez l’agent avec les exemples appropriés (**Aucun** ou **Tous les types de fichiers).**</span><span class="sxs-lookup"><span data-stu-id="004c7-171">Configure the Agent with the appropriate samples (**None** or **All file types**).</span></span>

    ![Image des paramètres de configuration1](images/configmgr-config-settings.png)

12. <span data-ttu-id="004c7-173">Sélectionnez la télémétrie appropriée **(Normale** ou **Accélérée),** puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-173">Select the appropriate telemetry (**Normal** or **Expedited**) then click **Next**.</span></span>

    ![Image des paramètres de configuration2](images/configmgr-telemetry.png)

14. <span data-ttu-id="004c7-175">Vérifiez la configuration, puis cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-175">Verify the configuration, then click **Next**.</span></span>

     ![Image des paramètres de configuration3](images/configmgr-verify-configuration.png)

15. <span data-ttu-id="004c7-177">Cliquez **sur Fermer** une fois l’Assistant terminé.</span><span class="sxs-lookup"><span data-stu-id="004c7-177">Click **Close** when the Wizard completes.</span></span>

16.  <span data-ttu-id="004c7-178">Dans la console Microsoft Endpoint Configuration Manager, cliquez avec le bouton droit sur la stratégie Defender for Endpoint que vous avez créée et sélectionnez **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-178">In the Microsoft Endpoint Configuration Manager console, right-click the Defender for Endpoint policy you just created and select **Deploy**.</span></span>

     ![Image des paramètres de configuration4](images/configmgr-deploy.png)

17. <span data-ttu-id="004c7-180">Dans le panneau droit, sélectionnez la collection créée précédemment et cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="004c7-180">On the right panel, select the previously created collection and click **OK**.</span></span>

    ![Image des paramètres de configuration5](images/configmgr-select-collection.png)


#### <a name="previous-versions-of-windows-client-windows-7-and-windows-81"></a><span data-ttu-id="004c7-182">Versions précédentes de Windows Client (Windows 7 et Windows 8.1)</span><span class="sxs-lookup"><span data-stu-id="004c7-182">Previous versions of Windows Client (Windows 7 and Windows 8.1)</span></span>
<span data-ttu-id="004c7-183">Suivez les étapes ci-dessous pour identifier l’ID d’espace de travail Defender pour le point de terminaison et la clé d’espace de travail, qui seront requis pour l’intégration des versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="004c7-183">Follow the steps below to identify the Defender for Endpoint Workspace ID and Workspace Key, that will be required for the onboarding of previous versions of Windows.</span></span>

1. <span data-ttu-id="004c7-184">À partir d’un portail centre de sécurité Microsoft Defender, **sélectionnez Paramètres >'intégration.**</span><span class="sxs-lookup"><span data-stu-id="004c7-184">From a Microsoft Defender Security Center Portal, select **Settings > Onboarding**.</span></span>

2. <span data-ttu-id="004c7-185">Sous le système **d’exploitation, choisissez Windows 7 SP1 et 8.1**.</span><span class="sxs-lookup"><span data-stu-id="004c7-185">Under operating system choose **Windows 7 SP1 and 8.1**.</span></span>

3. <span data-ttu-id="004c7-186">Copiez **l’ID d’espace de travail** et la clé **d’espace de travail** et enregistrez-les.</span><span class="sxs-lookup"><span data-stu-id="004c7-186">Copy the **Workspace ID** and **Workspace Key** and save them.</span></span> <span data-ttu-id="004c7-187">Ils seront utilisés plus tard dans le processus.</span><span class="sxs-lookup"><span data-stu-id="004c7-187">They will be used later in the process.</span></span>

    ![Image de l’intégration](images/91b738e4b97c4272fd6d438d8c2d5269.png)

4. <span data-ttu-id="004c7-189">Installez l’agent de surveillance Microsoft (MMA).</span><span class="sxs-lookup"><span data-stu-id="004c7-189">Install the Microsoft Monitoring Agent (MMA).</span></span> <br>
    <span data-ttu-id="004c7-190">MMA est actuellement pris en charge (depuis janvier 2019) sur les systèmes d’exploitation Windows suivants :</span><span class="sxs-lookup"><span data-stu-id="004c7-190">MMA is currently (as of January 2019) supported on the following Windows Operating Systems:</span></span>

    -   <span data-ttu-id="004c7-191">SSO serveur : Windows Server 2008 SP1 ou plus nouveau</span><span class="sxs-lookup"><span data-stu-id="004c7-191">Server SKUs: Windows Server 2008 SP1 or Newer</span></span>

    -   <span data-ttu-id="004c7-192">SSO client : Windows 7 SP1 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="004c7-192">Client SKUs: Windows 7 SP1 and later</span></span>

    <span data-ttu-id="004c7-193">L’agent MMA doit être installé sur les appareils Windows.</span><span class="sxs-lookup"><span data-stu-id="004c7-193">The MMA agent will need to be installed on Windows devices.</span></span> <span data-ttu-id="004c7-194">Pour installer l’agent, certains systèmes doivent télécharger la mise à jour pour l’expérience client et la [télémétrie](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry) de diagnostic afin de collecter les données avec MMA.</span><span class="sxs-lookup"><span data-stu-id="004c7-194">To install the agent, some systems will need to download the [Update for customer experience and diagnostic telemetry](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry) in order to collect the data with MMA.</span></span> <span data-ttu-id="004c7-195">Ces versions système incluent, sans s’y limiter, les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="004c7-195">These system versions include but may not be limited to:</span></span>

    -   <span data-ttu-id="004c7-196">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="004c7-196">Windows 8.1</span></span>

    -   <span data-ttu-id="004c7-197">Windows 7</span><span class="sxs-lookup"><span data-stu-id="004c7-197">Windows 7</span></span>

    -   <span data-ttu-id="004c7-198">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="004c7-198">Windows Server 2016</span></span>

    -   <span data-ttu-id="004c7-199">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="004c7-199">Windows Server 2012 R2</span></span>

    -   <span data-ttu-id="004c7-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="004c7-200">Windows Server 2008 R2</span></span>

    <span data-ttu-id="004c7-201">Plus précisément, pour Windows 7 SP1, les correctifs suivants doivent être installés :</span><span class="sxs-lookup"><span data-stu-id="004c7-201">Specifically, for Windows 7 SP1, the following patches must be installed:</span></span>

    -   <span data-ttu-id="004c7-202">Installer [KB4074598](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span><span class="sxs-lookup"><span data-stu-id="004c7-202">Install [KB4074598](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span></span>

    -   <span data-ttu-id="004c7-203">Installez la [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (ou **ultérieure)** ou 
         [la KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework).</span><span class="sxs-lookup"><span data-stu-id="004c7-203">Install either [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (or later) **or**
        [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework).</span></span>
        <span data-ttu-id="004c7-204">N’installez pas les deux sur le même système.</span><span class="sxs-lookup"><span data-stu-id="004c7-204">Do not install both on the same system.</span></span>

5. <span data-ttu-id="004c7-205">Si vous utilisez un proxy pour vous connecter à Internet, consultez la section Configurer les paramètres du proxy.</span><span class="sxs-lookup"><span data-stu-id="004c7-205">If you're using a proxy to connect to the Internet see the Configure proxy settings section.</span></span>

<span data-ttu-id="004c7-206">Une fois terminé, vous devriez voir les points de terminaison intégrés dans le portail dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="004c7-206">Once completed, you should see onboarded endpoints in the portal within an hour.</span></span>

### <a name="next-generation-protection"></a><span data-ttu-id="004c7-207">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="004c7-207">Next generation protection</span></span> 
<span data-ttu-id="004c7-208">L’antivirus Microsoft Defender est une solution de protection contre les programmes malveillants intégrée qui offre une protection nouvelle génération pour les ordinateurs de bureau, les ordinateurs portables et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="004c7-208">Microsoft Defender Antivirus is a built-in antimalware solution that provides next generation protection for desktops, portable computers, and servers.</span></span>

1. <span data-ttu-id="004c7-209">Dans la console Microsoft Endpoint Configuration Manager, accédez à **Assets and Compliance \> Overview \> Endpoint Protection \> Antimalware Polices** et choisissez Créer une stratégie **anti-programme malveillant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-209">In the Microsoft Endpoint Configuration Manager console, navigate to **Assets and Compliance \> Overview \> Endpoint Protection \> Antimalware Polices** and choose **Create Antimalware Policy**.</span></span>

    ![Image de la stratégie anti-programme malveillant](images/9736e0358e86bc778ce1bd4c516adb8b.png)

2. <span data-ttu-id="004c7-211">Select **Scheduled scans**, **Scan settings**, **Default actions**, **Real-time protection**, Exclusion **settings**, **Advanced**, **Threat overrides**, Cloud Protection **Service** and Security **intelligence updates** and choose **OK**.</span><span class="sxs-lookup"><span data-stu-id="004c7-211">Select **Scheduled scans**, **Scan settings**, **Default actions**, **Real-time protection**, **Exclusion settings**, **Advanced**, **Threat overrides**, **Cloud Protection Service** and **Security intelligence   updates** and choose **OK**.</span></span>

    ![Image du volet de protection nouvelle génération1](images/1566ad81bae3d714cc9e0d47575a8cbd.png)

    <span data-ttu-id="004c7-213">Dans certains secteurs d’activité ou certains clients d’entreprise, certains peuvent avoir des besoins spécifiques sur la configuration de l’antivirus.</span><span class="sxs-lookup"><span data-stu-id="004c7-213">In certain industries or some select enterprise customers might have specific needs on how Antivirus is configured.</span></span>

  
    [<span data-ttu-id="004c7-214">Analyse rapide par rapport à l’analyse complète et à l’analyse personnalisée</span><span class="sxs-lookup"><span data-stu-id="004c7-214">Quick scan versus full scan and custom scan</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/scheduled-catch-up-scans-microsoft-defender-antivirus#quick-scan-versus-full-scan-and-custom-scan)

    <span data-ttu-id="004c7-215">Pour plus d’informations, voir [Infrastructure de configuration de sécurité Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-security-configuration-framework/windows-security-configuration-framework)</span><span class="sxs-lookup"><span data-stu-id="004c7-215">For more details, see [Windows Security configuration framework](https://docs.microsoft.com/windows/security/threat-protection/windows-security-configuration-framework/windows-security-configuration-framework)</span></span>
  
    ![Image du volet de protection nouvelle génération2](images/cd7daeb392ad5a36f2d3a15d650f1e96.png)

    ![Image du volet de protection nouvelle génération3](images/36c7c2ed737f2f4b54918a4f20791d4b.png)

    ![Image du volet de protection nouvelle génération 4](images/a28afc02c1940d5220b233640364970c.png)

    ![Image du volet de protection nouvelle génération5](images/5420a8790c550f39f189830775a6d4c9.png)

    ![Image du volet de protection nouvelle génération6](images/33f08a38f2f4dd12a364f8eac95e8c6b.png)

    ![Image du volet de protection nouvelle génération7](images/41b9a023bc96364062c2041a8f5c344e.png)

    ![Image du volet de protection nouvelle génération8](images/945c9c5d66797037c3caeaa5c19f135c.png)

    ![Image du volet de protection nouvelle génération9](images/3876ca687391bfc0ce215d221c683970.png)

3. <span data-ttu-id="004c7-224">Cliquez avec le bouton droit sur la stratégie anti-programme malveillant nouvellement créée et sélectionnez **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-224">Right-click on the newly created antimalware policy and select **Deploy**.</span></span>

    ![Image du volet de protection nouvelle génération10](images/f5508317cd8c7870627cb4726acd5f3d.png)

4. <span data-ttu-id="004c7-226">Ciblez la nouvelle stratégie anti-programme malveillant sur votre collection Windows 10, puis cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="004c7-226">Target the new antimalware policy to your Windows 10 collection and click **OK**.</span></span>

     ![Image du volet de protection nouvelle génération11](images/configmgr-select-collection.png)

<span data-ttu-id="004c7-228">Après avoir terminé cette tâche, vous avez configuré correctement Windows Defender Antivirus.</span><span class="sxs-lookup"><span data-stu-id="004c7-228">After completing this task, you now have successfully configured Windows Defender Antivirus.</span></span>

### <a name="attack-surface-reduction"></a><span data-ttu-id="004c7-229">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="004c7-229">Attack surface reduction</span></span>
<span data-ttu-id="004c7-230">Le pilier de réduction de la surface d’attaque de Defender pour le point de terminaison inclut l’ensemble de fonctionnalités disponible sous Exploit Guard.</span><span class="sxs-lookup"><span data-stu-id="004c7-230">The attack surface reduction pillar of Defender for Endpoint includes the feature set that is available under Exploit Guard.</span></span> <span data-ttu-id="004c7-231">Règles de réduction de la surface d’attaque (ASR), Accès contrôlé aux dossiers, Protection du réseau et Exploit Protection.</span><span class="sxs-lookup"><span data-stu-id="004c7-231">Attack surface reduction (ASR) rules, Controlled Folder Access, Network Protection and Exploit Protection.</span></span> 

<span data-ttu-id="004c7-232">Toutes ces fonctionnalités fournissent un mode audit et un mode bloc.</span><span class="sxs-lookup"><span data-stu-id="004c7-232">All these features provide an audit mode and a block mode.</span></span> <span data-ttu-id="004c7-233">En mode audit, il n’y a pas d’impact sur l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="004c7-233">In audit mode there is no end-user impact.</span></span> <span data-ttu-id="004c7-234">Il s’agit uniquement de collecter des données de télémétrie supplémentaires et de les rendre disponibles dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="004c7-234">All it does is collect additional telemetry and make it available in the Microsoft Defender Security Center.</span></span> <span data-ttu-id="004c7-235">L’objectif d’un déploiement est de déplacer pas à pas les contrôles de sécurité en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="004c7-235">The goal with a deployment is to step-by-step move security controls into block mode.</span></span>

<span data-ttu-id="004c7-236">Pour définir des règles de récupération de l’accès en mode audit :</span><span class="sxs-lookup"><span data-stu-id="004c7-236">To set ASR rules in Audit mode:</span></span>

1. <span data-ttu-id="004c7-237">Dans la console Microsoft Endpoint Configuration Manager, accédez à **Assets and Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** et choisissez Créer une stratégie Exploit **Guard.**</span><span class="sxs-lookup"><span data-stu-id="004c7-237">In the Microsoft Endpoint Configuration Manager console, navigate to **Assets and Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** and choose **Create Exploit Guard Policy**.</span></span>

   ![Image de la console Microsoft Endpoint Configuration Manager 0](images/728c10ef26042bbdbcd270b6343f1a8a.png)

2.  <span data-ttu-id="004c7-239">Sélectionnez **Réduction de la surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="004c7-239">Select **Attack Surface Reduction**.</span></span>
   

3. <span data-ttu-id="004c7-240">Définissez les règles sur **Audit** et cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-240">Set rules to **Audit** and click **Next**.</span></span>


    ![Image de Microsoft Endpoint Configuration Manager console1](images/d18e40c9e60aecf1f9a93065cb7567bd.png)

4. <span data-ttu-id="004c7-242">Confirmez la nouvelle stratégie Exploit Guard en cliquant sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-242">Confirm the new Exploit Guard policy by clicking on **Next**.</span></span>

    ![Image de Microsoft Endpoint Configuration Manager console2](images/0a6536f2c4024c08709cac8fcf800060.png)

    
5. <span data-ttu-id="004c7-244">Une fois la stratégie créée, cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-244">Once the policy is created click **Close**.</span></span>

    ![Image de microsoft Endpoint Configuration Manager console3](images/95d23a07c2c8bc79176788f28cef7557.png)

    ![Image de Microsoft Endpoint Manager console1](images/95d23a07c2c8bc79176788f28cef7557.png)
   

6.  <span data-ttu-id="004c7-247">Cliquez avec le bouton droit sur la stratégie nouvellement créée et choisissez **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-247">Right-click on the newly created policy and choose **Deploy**.</span></span>
    
    ![Image de la console Microsoft Endpoint Configuration Manager 4](images/8999dd697e3b495c04eb911f8b68a1ef.png)

7. <span data-ttu-id="004c7-249">Ciblez la stratégie sur la collection Windows 10 nouvellement créée et cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="004c7-249">Target the policy to the newly created Windows 10 collection and click **OK**.</span></span>

    ![Image de la console Microsoft Endpoint Configuration Manager 5](images/0ccfe3e803be4b56c668b220b51da7f7.png)

<span data-ttu-id="004c7-251">Après avoir effectué cette tâche, vous avez correctement configuré les règles de la asr en mode audit.</span><span class="sxs-lookup"><span data-stu-id="004c7-251">After completing this task, you now have successfully configured ASR rules in audit mode.</span></span>  
  
<span data-ttu-id="004c7-252">Vous trouverez ci-dessous des étapes supplémentaires pour vérifier si les règles de réponse aux erreurs sont correctement appliquées aux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="004c7-252">Below are additional steps to verify whether ASR rules are correctly applied to endpoints.</span></span> <span data-ttu-id="004c7-253">(Cela peut prendre quelques minutes)</span><span class="sxs-lookup"><span data-stu-id="004c7-253">(This may take few minutes)</span></span>


1. <span data-ttu-id="004c7-254">À partir d’un navigateur web, accédez à <https://securitycenter.windows.com> .</span><span class="sxs-lookup"><span data-stu-id="004c7-254">From a web browser, navigate to <https://securitycenter.windows.com>.</span></span>

2.  <span data-ttu-id="004c7-255">Sélectionnez **Gestion de la configuration** dans le menu gauche.</span><span class="sxs-lookup"><span data-stu-id="004c7-255">Select **Configuration management** from left side menu.</span></span>

3. <span data-ttu-id="004c7-256">Cliquez **sur Aller à la gestion de la surface d’attaque** dans le panneau De gestion de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="004c7-256">Click **Go to attack surface management** in the Attack surface management panel.</span></span> 
    
    ![Image de la gestion de la surface d’attaque](images/security-center-attack-surface-mgnt-tile.png)

4. <span data-ttu-id="004c7-258">Cliquez sur **l’onglet Configuration** dans les rapports de règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="004c7-258">Click **Configuration** tab in Attack surface reduction rules reports.</span></span> <span data-ttu-id="004c7-259">Il présente la vue d’ensemble de la configuration des règles de la asr et l’état des règles de la asr sur chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="004c7-259">It shows ASR rules configuration overview and ASR rules status on each devices.</span></span>

    ![Capture d’écran des règles de réduction de la surface d’attaque reports1](images/f91f406e6e0aae197a947d3b0e8b2d0d.png)

5. <span data-ttu-id="004c7-261">Cliquez sur chaque appareil pour obtenir les détails de configuration des règles asr.</span><span class="sxs-lookup"><span data-stu-id="004c7-261">Click each device shows configuration details of ASR rules.</span></span>

    ![Capture d’écran des règles de réduction de la surface d’attaque rapports2](images/24bfb16ed561cbb468bd8ce51130ca9d.png)

<span data-ttu-id="004c7-263">Pour [plus d’informations, voir Optimiser](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-machines-asr)   le déploiement et les détections de règles asr.</span><span class="sxs-lookup"><span data-stu-id="004c7-263">See [Optimize ASR rule deployment and detections](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-machines-asr)   for more details.</span></span>  


#### <a name="set-network-protection-rules-in-audit-mode"></a><span data-ttu-id="004c7-264">Définissez des règles de protection réseau en mode audit :</span><span class="sxs-lookup"><span data-stu-id="004c7-264">Set Network Protection rules in Audit mode:</span></span>
1. <span data-ttu-id="004c7-265">Dans la console Microsoft Endpoint Configuration Manager, accédez à **Assets and Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** et choisissez Créer une stratégie Exploit **Guard.**</span><span class="sxs-lookup"><span data-stu-id="004c7-265">In the Microsoft Endpoint Configuration Manager console, navigate to **Assets and  Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** and choose **Create Exploit Guard Policy**.</span></span>

    ![Capture d’écran de System Center Configuration Manager1](images/728c10ef26042bbdbcd270b6343f1a8a.png)

2. <span data-ttu-id="004c7-267">Sélectionnez **Protection du réseau.**</span><span class="sxs-lookup"><span data-stu-id="004c7-267">Select **Network protection**.</span></span>

3. <span data-ttu-id="004c7-268">Définissez le paramètre sur **Audit et** cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-268">Set the setting to **Audit** and click **Next**.</span></span> 

    ![Capture d’écran de System Center Confirugatiom Manager2](images/c039b2e05dba1ade6fb4512456380c9f.png)

4. <span data-ttu-id="004c7-270">Confirmez la nouvelle stratégie Exploit Guard en cliquant sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-270">Confirm the new Exploit Guard Policy by clicking **Next**.</span></span>
    
    ![Capture d’écran Exploit GUard policy1](images/0a6536f2c4024c08709cac8fcf800060.png)

5. <span data-ttu-id="004c7-272">Une fois la stratégie créée, cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-272">Once the policy is created click on **Close**.</span></span>

    ![Capture d’écran Exploit GUard policy2](images/95d23a07c2c8bc79176788f28cef7557.png)

6. <span data-ttu-id="004c7-274">Cliquez avec le bouton droit sur la stratégie nouvellement créée et choisissez **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-274">Right-click on the newly created policy and choose **Deploy**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager1](images/8999dd697e3b495c04eb911f8b68a1ef.png)

7. <span data-ttu-id="004c7-276">Sélectionnez la stratégie pour la collection Windows 10 nouvellement créée et choisissez **OK.**</span><span class="sxs-lookup"><span data-stu-id="004c7-276">Select the policy to the newly created Windows 10 collection and choose **OK**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager2](images/0ccfe3e803be4b56c668b220b51da7f7.png)



<span data-ttu-id="004c7-278">Après avoir effectué cette tâche, vous avez correctement configuré la Protection du réseau en mode audit.</span><span class="sxs-lookup"><span data-stu-id="004c7-278">After completing this task, you now have successfully configured Network Protection in audit mode.</span></span>

#### <a name="to-set-controlled-folder-access-rules-in-audit-mode"></a><span data-ttu-id="004c7-279">Pour définir des règles d’accès contrôlé aux dossiers en mode Audit :</span><span class="sxs-lookup"><span data-stu-id="004c7-279">To set Controlled Folder Access rules in Audit mode:</span></span>

1. <span data-ttu-id="004c7-280">Dans la console Microsoft Endpoint Configuration Manager, accédez à **Assets and Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** et choisissez Créer une stratégie Exploit **Guard.**</span><span class="sxs-lookup"><span data-stu-id="004c7-280">In the Microsoft Endpoint Configuration Manager console, navigate to **Assets and Compliance \> Overview \> Endpoint Protection \> Windows Defender Exploit Guard** and choose **Create Exploit Guard Policy**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager3](images/728c10ef26042bbdbcd270b6343f1a8a.png)

2. <span data-ttu-id="004c7-282">Sélectionnez **Accès contrôlé aux dossiers.**</span><span class="sxs-lookup"><span data-stu-id="004c7-282">Select **Controlled folder access**.</span></span>
    
3. <span data-ttu-id="004c7-283">Définissez la configuration sur **Audit et** cliquez sur **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="004c7-283">Set the configuration to **Audit** and click **Next**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager4](images/a8b934dab2dbba289cf64fe30e0e8aa4.png)    
    
4. <span data-ttu-id="004c7-285">Confirmez la nouvelle stratégie Exploit Guard en cliquant sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="004c7-285">Confirm the new Exploit Guard Policy by clicking on **Next**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager5](images/0a6536f2c4024c08709cac8fcf800060.png)

5. <span data-ttu-id="004c7-287">Une fois la stratégie créée, cliquez sur **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-287">Once the policy is created click on **Close**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager6](images/95d23a07c2c8bc79176788f28cef7557.png)

6. <span data-ttu-id="004c7-289">Cliquez avec le bouton droit sur la stratégie nouvellement créée et choisissez **Déployer.**</span><span class="sxs-lookup"><span data-stu-id="004c7-289">Right-click on the newly created policy and choose **Deploy**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager7](images/8999dd697e3b495c04eb911f8b68a1ef.png)

7.  <span data-ttu-id="004c7-291">Ciblez la stratégie sur la collection Windows 10 nouvellement créée et cliquez sur **OK.**</span><span class="sxs-lookup"><span data-stu-id="004c7-291">Target the policy to the newly created Windows 10 collection and click **OK**.</span></span>

    ![Capture d’écran de Microsoft Endpoint Configuration Manager8](images/0ccfe3e803be4b56c668b220b51da7f7.png)

<span data-ttu-id="004c7-293">Vous avez maintenant configuré l’accès contrôlé aux dossiers en mode audit.</span><span class="sxs-lookup"><span data-stu-id="004c7-293">You have now successfully configured Controlled folder access in audit mode.</span></span>

## <a name="related-topic"></a><span data-ttu-id="004c7-294">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="004c7-294">Related topic</span></span>
- [<span data-ttu-id="004c7-295">Intégration à l’aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="004c7-295">Onboarding using Microsoft Endpoint Manager</span></span>](onboarding-endpoint-manager.md)
