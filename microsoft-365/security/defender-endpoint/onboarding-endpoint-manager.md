---
title: Intégration à l'aide de Microsoft Endpoint Manager
description: Découvrez comment intégrer Microsoft Defender pour endpoint à l'aide de Microsoft Endpoint Manager
keywords: intégration, configuration, déploiement, déploiement, gestionnaire de point de terminaison, Microsoft Defender pour le point de terminaison, création de collection, réponse de détection de point de terminaison, protection nouvelle génération, réduction de la surface d'attaque, gestionnaire de point de terminaison Microsoft
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
ms.openlocfilehash: e744262cfd63383e69abf02be9fbf91d2d229db2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935256"
---
# <a name="onboarding-using-microsoft-endpoint-manager"></a><span data-ttu-id="79097-104">Intégration à l'aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="79097-104">Onboarding using Microsoft Endpoint Manager</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="79097-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="79097-105">**Applies to:**</span></span>
- [<span data-ttu-id="79097-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79097-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="79097-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="79097-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="79097-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="79097-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="79097-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="79097-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="79097-110">Cet article fait partie du guide de déploiement et agit comme un exemple de méthode d'intégration.</span><span class="sxs-lookup"><span data-stu-id="79097-110">This article is part of the Deployment guide and acts as an example onboarding method.</span></span> 

<span data-ttu-id="79097-111">Dans la [rubrique Planification,](deployment-strategy.md) plusieurs méthodes ont été fournies pour intégrer des appareils au service.</span><span class="sxs-lookup"><span data-stu-id="79097-111">In the [Planning](deployment-strategy.md) topic, there were several methods provided to onboard devices to the service.</span></span> <span data-ttu-id="79097-112">Cette rubrique traite de l'architecture native du cloud.</span><span class="sxs-lookup"><span data-stu-id="79097-112">This topic covers the cloud-native architecture.</span></span> 

<span data-ttu-id="79097-113">![Image de l'architecture native du cloud ](images/cloud-native-architecture.png)
 *Diagramme des architectures d'environnement*</span><span class="sxs-lookup"><span data-stu-id="79097-113">![Image of cloud-native architecture](images/cloud-native-architecture.png)
*Diagram of environment architectures*</span></span>

<span data-ttu-id="79097-114">Bien que Defender pour point de terminaison prend en charge l'intégration de différents points de terminaison et outils, cet article ne les traite pas.</span><span class="sxs-lookup"><span data-stu-id="79097-114">While Defender for Endpoint supports onboarding of various endpoints and tools, this article does not cover them.</span></span> <span data-ttu-id="79097-115">Pour plus d'informations sur l'intégration générale à l'aide d'autres outils et méthodes de déploiement pris en charge, voir [vue d'ensemble de l'intégration.](onboarding.md)</span><span class="sxs-lookup"><span data-stu-id="79097-115">For information on general onboarding using other supported deployment tools and methods, see [Onboarding overview](onboarding.md).</span></span>


<span data-ttu-id="79097-116">[Microsoft Endpoint Manager est](https://docs.microsoft.com/mem/endpoint-manager-overview) une plateforme de solution qui unifie plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="79097-116">[Microsoft Endpoint Manager](https://docs.microsoft.com/mem/endpoint-manager-overview) is a solution platform that unifies several services.</span></span> <span data-ttu-id="79097-117">Il inclut [Microsoft Intune pour](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) la gestion des appareils en nuage.</span><span class="sxs-lookup"><span data-stu-id="79097-117">It includes [Microsoft Intune](https://docs.microsoft.com/mem/intune/fundamentals/what-is-intune) for cloud-based device management.</span></span>


<span data-ttu-id="79097-118">Cette rubrique guide les utilisateurs dans :</span><span class="sxs-lookup"><span data-stu-id="79097-118">This topic guides users in:</span></span>
- <span data-ttu-id="79097-119">Étape 1 : intégration d'appareils au service en créant un groupe dans Microsoft Endpoint Manager (MEM) pour affecter des configurations sur</span><span class="sxs-lookup"><span data-stu-id="79097-119">Step 1: Onboarding devices to the service by creating a group in Microsoft Endpoint Manager (MEM) to assign configurations on</span></span>
- <span data-ttu-id="79097-120">Étape 2 : Configuration des fonctionnalités de Defender pour les points de terminaison à l'aide de Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="79097-120">Step 2: Configuring Defender for Endpoint capabilities using Microsoft Endpoint Manager</span></span>

<span data-ttu-id="79097-121">Ces instructions d'intégration vous guident tout au long des étapes de base suivantes que vous devez suivre lors de l'utilisation de Microsoft Endpoint Manager :</span><span class="sxs-lookup"><span data-stu-id="79097-121">This onboarding guidance will walk you through the following basic steps that you need to take when using Microsoft Endpoint Manager:</span></span>

-   [<span data-ttu-id="79097-122">Identification des appareils ou des utilisateurs cibles</span><span class="sxs-lookup"><span data-stu-id="79097-122">Identifying target devices or users</span></span>](#identify-target-devices-or-users)

    -   <span data-ttu-id="79097-123">Création d'un groupe Azure Active Directory (utilisateur ou appareil)</span><span class="sxs-lookup"><span data-stu-id="79097-123">Creating an Azure Active Directory group (User or Device)</span></span>

-   [<span data-ttu-id="79097-124">Création d'un profil de configuration</span><span class="sxs-lookup"><span data-stu-id="79097-124">Creating a Configuration Profile</span></span>](#step-2-create-configuration-policies-to-configure-microsoft-defender-for-endpoint-capabilities)

    -   <span data-ttu-id="79097-125">Dans Microsoft Endpoint Manager, nous vous guiderons dans la création d'une stratégie distincte pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="79097-125">In Microsoft Endpoint Manager, we'll guide you in creating a separate policy for each capability.</span></span>





## <a name="resources"></a><span data-ttu-id="79097-126">Ressources</span><span class="sxs-lookup"><span data-stu-id="79097-126">Resources</span></span>


<span data-ttu-id="79097-127">Voici les liens dont vous aurez besoin pour le reste du processus :</span><span class="sxs-lookup"><span data-stu-id="79097-127">Here are the links you'll need for the rest of the process:</span></span>

-   [<span data-ttu-id="79097-128">Portail MEM</span><span class="sxs-lookup"><span data-stu-id="79097-128">MEM portal</span></span>](https://aka.ms/memac)

-   [<span data-ttu-id="79097-129">Centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="79097-129">Security Center</span></span>](https://securitycenter.windows.com/)

-   [<span data-ttu-id="79097-130">Bases de référence de sécurité Intune</span><span class="sxs-lookup"><span data-stu-id="79097-130">Intune Security baselines</span></span>](https://docs.microsoft.com/mem/intune/protect/security-baseline-settings-defender-atp#microsoft-defender)

<span data-ttu-id="79097-131">Pour plus d'informations sur Microsoft Endpoint Manager, consultez les ressources ci-après :</span><span class="sxs-lookup"><span data-stu-id="79097-131">For more information about Microsoft Endpoint Manager, check out these resources:</span></span>
- [<span data-ttu-id="79097-132">Page Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="79097-132">Microsoft Endpoint Manager page</span></span>](https://docs.microsoft.com/mem/)
- [<span data-ttu-id="79097-133">Billet de blog sur la convergence d'Intune et configMgr</span><span class="sxs-lookup"><span data-stu-id="79097-133">Blog post on convergence of Intune and ConfigMgr</span></span>](https://www.microsoft.com/microsoft-365/blog/2019/11/04/use-the-power-of-cloud-intelligence-to-simplify-and-accelerate-it-and-the-move-to-a-modern-workplace/)
- [<span data-ttu-id="79097-134">Vidéo d'introduction sur MEM</span><span class="sxs-lookup"><span data-stu-id="79097-134">Introduction video on MEM</span></span>](https://www.microsoft.com/microsoft-365/blog/2019/11/04/use-the-power-of-cloud-intelligence-to-simplify-and-accelerate-it-and-the-move-to-a-modern-workplace)

## <a name="step-1-onboard-devices-by-creating-a-group-in-mem-to-assign-configurations-on"></a><span data-ttu-id="79097-135">Étape 1 : intégrer des appareils en créant un groupe dans MEM pour affecter des configurations</span><span class="sxs-lookup"><span data-stu-id="79097-135">Step 1: Onboard devices by creating a group in MEM to assign configurations on</span></span>
### <a name="identify-target-devices-or-users"></a><span data-ttu-id="79097-136">Identifier les appareils ou les utilisateurs cibles</span><span class="sxs-lookup"><span data-stu-id="79097-136">Identify target devices or users</span></span>
<span data-ttu-id="79097-137">Dans cette section, nous allons créer un groupe de test pour affecter vos configurations.</span><span class="sxs-lookup"><span data-stu-id="79097-137">In this section, we will create a test group to assign your configurations on.</span></span>

>[!NOTE]
><span data-ttu-id="79097-138">Intune utilise des groupes Azure Active Directory (Azure AD) pour gérer les appareils et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="79097-138">Intune uses Azure Active Directory (Azure AD) groups to manage devices and users.</span></span> <span data-ttu-id="79097-139">En tant qu'administrateur Intune, vous pouvez configurer des groupes en fonction des besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="79097-139">As an Intune admin, you can set up groups to suit your organizational needs.</span></span><br>
<span data-ttu-id="79097-140">Pour plus d'informations, voir [Ajouter des groupes pour organiser les utilisateurs et les appareils.](https://docs.microsoft.com/mem/intune/fundamentals/groups-add)</span><span class="sxs-lookup"><span data-stu-id="79097-140">For more information, see [Add groups to organize users and devices](https://docs.microsoft.com/mem/intune/fundamentals/groups-add).</span></span>

### <a name="create-a-group"></a><span data-ttu-id="79097-141">Créer un groupe</span><span class="sxs-lookup"><span data-stu-id="79097-141">Create a group</span></span>

1.  <span data-ttu-id="79097-142">Ouvrez le portail MEM.</span><span class="sxs-lookup"><span data-stu-id="79097-142">Open the MEM portal.</span></span>

2.  <span data-ttu-id="79097-143">Ouvrez **groupes > nouveau groupe.**</span><span class="sxs-lookup"><span data-stu-id="79097-143">Open **Groups > New Group**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-144">![Image de Microsoft Endpoint Manager portal1](images/66f724598d9c3319cba27f79dd4617a4.png)</span><span class="sxs-lookup"><span data-stu-id="79097-144">![Image of Microsoft Endpoint Manager portal1](images/66f724598d9c3319cba27f79dd4617a4.png)</span></span>

3.  <span data-ttu-id="79097-145">Entrez des détails et créez un groupe.</span><span class="sxs-lookup"><span data-stu-id="79097-145">Enter details and create a new group.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-146">![Image de Microsoft Endpoint Manager portal2](images/b1e0206d675ad07db218b63cd9b9abc3.png)</span><span class="sxs-lookup"><span data-stu-id="79097-146">![Image of Microsoft Endpoint Manager portal2](images/b1e0206d675ad07db218b63cd9b9abc3.png)</span></span>

4.  <span data-ttu-id="79097-147">Ajoutez votre utilisateur ou appareil de test.</span><span class="sxs-lookup"><span data-stu-id="79097-147">Add your test user or device.</span></span>

5.  <span data-ttu-id="79097-148">Dans le **volet Groupes >** tous les groupes, ouvrez votre nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="79097-148">From the **Groups > All groups** pane, open your new group.</span></span>

6.  <span data-ttu-id="79097-149">Sélectionnez **membres > ajouter des membres.**</span><span class="sxs-lookup"><span data-stu-id="79097-149">Select  **Members > Add members**.</span></span>

7.  <span data-ttu-id="79097-150">Recherchez votre utilisateur ou appareil de test et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="79097-150">Find your test user or device and select it.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-151">![Image de Microsoft Endpoint Manager portal3](images/149cbfdf221cdbde8159d0ab72644cd0.png)</span><span class="sxs-lookup"><span data-stu-id="79097-151">![Image of Microsoft Endpoint Manager portal3](images/149cbfdf221cdbde8159d0ab72644cd0.png)</span></span>

8.  <span data-ttu-id="79097-152">Votre groupe de test a maintenant un membre à tester.</span><span class="sxs-lookup"><span data-stu-id="79097-152">Your testing group now has a member to test.</span></span>

## <a name="step-2-create-configuration-policies-to-configure-microsoft-defender-for-endpoint-capabilities"></a><span data-ttu-id="79097-153">Étape 2 : Créer des stratégies de configuration pour configurer microsoft Defender pour les fonctionnalités de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79097-153">Step 2: Create configuration policies to configure Microsoft Defender for Endpoint capabilities</span></span>
<span data-ttu-id="79097-154">Dans la section suivante, vous allez créer un certain nombre de stratégies de configuration.</span><span class="sxs-lookup"><span data-stu-id="79097-154">In the following section, you'll create a number of configuration policies.</span></span>

<span data-ttu-id="79097-155">Tout d'abord, il s'agit d'une stratégie de configuration qui permet de sélectionner les groupes d'utilisateurs ou d'appareils qui seront intégrés à Defender for Endpoint :</span><span class="sxs-lookup"><span data-stu-id="79097-155">First is a configuration policy to select which groups of users or devices will be onboarded to Defender for Endpoint:</span></span>

- [<span data-ttu-id="79097-156">Détection et réponse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79097-156">Endpoint detection and response</span></span>](#endpoint-detection-and-response) 

<span data-ttu-id="79097-157">Ensuite, vous allez continuer en créant différents types de stratégies de sécurité de point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="79097-157">Then you will continue by creating several different types of endpoint security policies:</span></span>

- [<span data-ttu-id="79097-158">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="79097-158">Next-generation protection</span></span>](#next-generation-protection)
- [<span data-ttu-id="79097-159">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="79097-159">Attack surface reduction</span></span>](#attack-surface-reduction--attack-surface-reduction-rules)

### <a name="endpoint-detection-and-response"></a><span data-ttu-id="79097-160">Détection et réponse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79097-160">Endpoint detection and response</span></span>

1.  <span data-ttu-id="79097-161">Ouvrez le portail MEM.</span><span class="sxs-lookup"><span data-stu-id="79097-161">Open the MEM portal.</span></span>

2.  <span data-ttu-id="79097-162">Accédez à **Endpoint security > endpoint detection and response**.</span><span class="sxs-lookup"><span data-stu-id="79097-162">Navigate to **Endpoint security > Endpoint detection and response**.</span></span> <span data-ttu-id="79097-163">Cliquez sur **Créer un profil.**</span><span class="sxs-lookup"><span data-stu-id="79097-163">Click on **Create Profile**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-164">![Image de Microsoft Endpoint Manager portal4](images/58dcd48811147feb4ddc17212b7fe840.png)</span><span class="sxs-lookup"><span data-stu-id="79097-164">![Image of Microsoft Endpoint Manager portal4](images/58dcd48811147feb4ddc17212b7fe840.png)</span></span>

3.  <span data-ttu-id="79097-165">Sous **Plateforme, sélectionnez Windows 10** et ultérieur, Profil - Détection de point de terminaison et réponse > créer.</span><span class="sxs-lookup"><span data-stu-id="79097-165">Under **Platform, select Windows 10 and Later, Profile - Endpoint detection and response > Create**.</span></span>

4.  <span data-ttu-id="79097-166">Entrez un nom et une description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-166">Enter a name and description, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-167">![Image de Microsoft Endpoint Manager portal5](images/a5b2d23bdd50b160fef4afd25dda28d4.png)</span><span class="sxs-lookup"><span data-stu-id="79097-167">![Image of Microsoft Endpoint Manager portal5](images/a5b2d23bdd50b160fef4afd25dda28d4.png)</span></span>

5.  <span data-ttu-id="79097-168">Sélectionnez les paramètres selon les besoins, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-168">Select settings as required, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-169">![Image de Microsoft Endpoint Manager portal6](images/cea7e288b5d42a9baf1aef0754ade910.png)</span><span class="sxs-lookup"><span data-stu-id="79097-169">![Image of Microsoft Endpoint Manager portal6](images/cea7e288b5d42a9baf1aef0754ade910.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="79097-170">Dans cette instance, cela a été automatiquement rempli comme Defender pour point de terminaison a déjà été intégré à Intune.</span><span class="sxs-lookup"><span data-stu-id="79097-170">In this instance, this has been auto populated as Defender for Endpoint has already been integrated with Intune.</span></span> <span data-ttu-id="79097-171">Pour plus d'informations sur l'intégration, voir [Activer Microsoft Defender pour le point de terminaison dans Intune.](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection-configure#to-enable-microsoft-defender-atp)</span><span class="sxs-lookup"><span data-stu-id="79097-171">For more information on the integration, see [Enable Microsoft Defender for Endpoint in Intune](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection-configure#to-enable-microsoft-defender-atp).</span></span>
    > 
    > <span data-ttu-id="79097-172">L'image suivante illustre ce que vous voyez lorsque Microsoft Defender pour le point de terminaison n'est PAS intégré à Intune :</span><span class="sxs-lookup"><span data-stu-id="79097-172">The following image is an example of what you'll see when Microsoft Defender for Endpoint is NOT integrated with Intune:</span></span>
    >
    > ![Image de Microsoft Endpoint Manager portal7](images/2466460812371ffae2d19a10c347d6f4.png)

6.  <span data-ttu-id="79097-174">Ajoutez des balises d'étendue si nécessaire, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-174">Add scope tags if necessary, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-175">![Image de Microsoft Endpoint Manager portal8](images/ef844f52ec2c0d737ce793f68b5e8408.png)</span><span class="sxs-lookup"><span data-stu-id="79097-175">![Image of Microsoft Endpoint Manager portal8](images/ef844f52ec2c0d737ce793f68b5e8408.png)</span></span>

7.  <span data-ttu-id="79097-176">Ajoutez un groupe de test en cliquant sur **Sélectionner les groupes à inclure** et choisissez votre groupe, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-176">Add test group by clicking on **Select groups to include** and choose your group, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-177">![Image de Microsoft Endpoint Manager portal9](images/fc3525e20752da026ec9f46ab4fec64f.png)</span><span class="sxs-lookup"><span data-stu-id="79097-177">![Image of Microsoft Endpoint Manager portal9](images/fc3525e20752da026ec9f46ab4fec64f.png)</span></span>

8.  <span data-ttu-id="79097-178">Examinez et acceptez, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="79097-178">Review and accept, then select  **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-179">![Image de Microsoft Endpoint Manager portal10](images/289172dbd7bd34d55d24810d9d4d8158.png)</span><span class="sxs-lookup"><span data-stu-id="79097-179">![Image of Microsoft Endpoint Manager portal10](images/289172dbd7bd34d55d24810d9d4d8158.png)</span></span>

9.  <span data-ttu-id="79097-180">Vous pouvez afficher votre stratégie terminée.</span><span class="sxs-lookup"><span data-stu-id="79097-180">You can view your completed policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-181">![Image de Microsoft Endpoint Manager portal11](images/5a568b6878be8243ea2b9d82d41ed297.png)</span><span class="sxs-lookup"><span data-stu-id="79097-181">![Image of Microsoft Endpoint Manager portal11](images/5a568b6878be8243ea2b9d82d41ed297.png)</span></span>

### <a name="next-generation-protection"></a><span data-ttu-id="79097-182">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="79097-182">Next-generation protection</span></span>

1.  <span data-ttu-id="79097-183">Ouvrez le portail MEM.</span><span class="sxs-lookup"><span data-stu-id="79097-183">Open the MEM portal.</span></span>

2.  <span data-ttu-id="79097-184">Accédez **à Endpoint Security > Antivirus > Create Policy**.</span><span class="sxs-lookup"><span data-stu-id="79097-184">Navigate to **Endpoint security > Antivirus > Create Policy**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-185">![Image de Microsoft Endpoint Manager portal12](images/6b728d6e0d71108d768e368b416ff8ba.png)</span><span class="sxs-lookup"><span data-stu-id="79097-185">![Image of Microsoft Endpoint Manager portal12](images/6b728d6e0d71108d768e368b416ff8ba.png)</span></span>

3.  <span data-ttu-id="79097-186">Select **Platform - Windows 10 and Later - Windows and Profile – Microsoft Defender Antivirus > Create**.</span><span class="sxs-lookup"><span data-stu-id="79097-186">Select **Platform - Windows 10 and Later - Windows and Profile – Microsoft Defender Antivirus > Create**.</span></span>

4.  <span data-ttu-id="79097-187">Entrez le nom et la description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-187">Enter name and description, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-188">![Image de Microsoft Endpoint Manager portal13](images/a7d738dd4509d65407b7d12beaa3e917.png)</span><span class="sxs-lookup"><span data-stu-id="79097-188">![Image of Microsoft Endpoint Manager portal13](images/a7d738dd4509d65407b7d12beaa3e917.png)</span></span>

5.  <span data-ttu-id="79097-189">Dans la **page Paramètres** de configuration : définissez les configurations dont vous avez besoin pour l'Antivirus Microsoft Defender (Protection cloud, Exclusions, Protection Real-Time et Correction).</span><span class="sxs-lookup"><span data-stu-id="79097-189">In the **Configuration settings page**: Set the configurations you require for Microsoft Defender Antivirus (Cloud Protection, Exclusions, Real-Time Protection, and Remediation).</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-190">![Image de Microsoft Endpoint Manager portal14](images/3840b1576d6f79a1d72eb14760ef5e8c.png)</span><span class="sxs-lookup"><span data-stu-id="79097-190">![Image of Microsoft Endpoint Manager portal14](images/3840b1576d6f79a1d72eb14760ef5e8c.png)</span></span>

6.  <span data-ttu-id="79097-191">Ajoutez des balises d'étendue si nécessaire, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-191">Add scope tags if necessary, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-192">![Image de Microsoft Endpoint Manager portal15](images/2055e4f9b9141525c0eb681e7ba19381.png)</span><span class="sxs-lookup"><span data-stu-id="79097-192">![Image of Microsoft Endpoint Manager portal15](images/2055e4f9b9141525c0eb681e7ba19381.png)</span></span>

7.  <span data-ttu-id="79097-193">Sélectionnez les groupes à inclure, affectez à votre groupe de test, puis sélectionnez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="79097-193">Select groups to include, assign to your test group, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-194">![Image de Microsoft Endpoint Manager portal16](images/48318a51adee06bff3908e8ad4944dc9.png)</span><span class="sxs-lookup"><span data-stu-id="79097-194">![Image of Microsoft Endpoint Manager portal16](images/48318a51adee06bff3908e8ad4944dc9.png)</span></span>

8.  <span data-ttu-id="79097-195">Examinez et créez, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="79097-195">Review and create, then select  **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-196">![Image de Microsoft Endpoint Manager portal17](images/dfdadab79112d61bd3693d957084b0ec.png)</span><span class="sxs-lookup"><span data-stu-id="79097-196">![Image of Microsoft Endpoint Manager portal17](images/dfdadab79112d61bd3693d957084b0ec.png)</span></span>

9.  <span data-ttu-id="79097-197">Vous verrez la stratégie de configuration que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="79097-197">You'll see the configuration policy you created.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-198">![Image de Microsoft Endpoint Manager portal18](images/38180219e632d6e4ec7bd25a46398da8.png)</span><span class="sxs-lookup"><span data-stu-id="79097-198">![Image of Microsoft Endpoint Manager portal18](images/38180219e632d6e4ec7bd25a46398da8.png)</span></span>

### <a name="attack-surface-reduction--attack-surface-reduction-rules"></a><span data-ttu-id="79097-199">Réduction de la surface d'attaque : règles de réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="79097-199">Attack Surface Reduction – Attack surface reduction rules</span></span>

1.  <span data-ttu-id="79097-200">Ouvrez le portail MEM.</span><span class="sxs-lookup"><span data-stu-id="79097-200">Open the MEM portal.</span></span>

2.  <span data-ttu-id="79097-201">Accédez à **Endpoint Security > Attack surface reduction**.</span><span class="sxs-lookup"><span data-stu-id="79097-201">Navigate to **Endpoint security > Attack surface reduction**.</span></span>

3.  <span data-ttu-id="79097-202">Sélectionnez **Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="79097-202">Select  **Create Policy**.</span></span>

4.  <span data-ttu-id="79097-203">Select **Platform - Windows 10 and Later – Profile - Attack surface reduction rules > Create**.</span><span class="sxs-lookup"><span data-stu-id="79097-203">Select **Platform - Windows 10 and Later – Profile - Attack surface reduction rules > Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-204">![Image de Microsoft Endpoint Manager portal19](images/522d9bb4288dc9c1a957392b51384fdd.png)</span><span class="sxs-lookup"><span data-stu-id="79097-204">![Image of Microsoft Endpoint Manager portal19](images/522d9bb4288dc9c1a957392b51384fdd.png)</span></span>

5.  <span data-ttu-id="79097-205">Entrez un nom et une description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-205">Enter a name and description, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-206">![Image de Microsoft Endpoint Manager portal20](images/a5a71fd73ec389f3cdce6d1a6bd1ff31.png)</span><span class="sxs-lookup"><span data-stu-id="79097-206">![Image of Microsoft Endpoint Manager portal20](images/a5a71fd73ec389f3cdce6d1a6bd1ff31.png)</span></span>

6.  <span data-ttu-id="79097-207">Dans la **page Paramètres de configuration**: définissez les configurations dont vous avez besoin pour les règles de réduction de la surface d'attaque, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-207">In the **Configuration settings page**: Set the configurations you require for Attack surface reduction rules, then select  **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79097-208">Nous allons configurer toutes les règles de réduction de la surface d'attaque sur Audit.</span><span class="sxs-lookup"><span data-stu-id="79097-208">We will be configuring all of the Attack surface reduction rules to Audit.</span></span>
    > 
    > <span data-ttu-id="79097-209">Pour plus d'informations, voir [Règles de réduction de la surface d'attaque.](attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="79097-209">For more information, see [Attack surface reduction rules](attack-surface-reduction.md).</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-210">![Image de Microsoft Endpoint Manager portal21](images/dd0c00efe615a64a4a368f54257777d0.png)</span><span class="sxs-lookup"><span data-stu-id="79097-210">![Image of Microsoft Endpoint Manager portal21](images/dd0c00efe615a64a4a368f54257777d0.png)</span></span>

7.  <span data-ttu-id="79097-211">Ajoutez des balises d'étendue selon les besoins, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-211">Add Scope Tags as required, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-212">![Image de Microsoft Endpoint Manager portal22](images/6daa8d347c98fe94a0d9c22797ff6f28.png)</span><span class="sxs-lookup"><span data-stu-id="79097-212">![Image of Microsoft Endpoint Manager portal22](images/6daa8d347c98fe94a0d9c22797ff6f28.png)</span></span>

8.  <span data-ttu-id="79097-213">Sélectionnez les groupes à inclure et à affecter au groupe de test, puis sélectionnez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="79097-213">Select groups to include and assign to test group, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-214">![Image de Microsoft Endpoint Manager portal23](images/45cefc8e4e474321b4d47b4626346597.png)</span><span class="sxs-lookup"><span data-stu-id="79097-214">![Image of Microsoft Endpoint Manager portal23](images/45cefc8e4e474321b4d47b4626346597.png)</span></span>

9. <span data-ttu-id="79097-215">Examinez les détails, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="79097-215">Review the details, then select  **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-216">![Image de Microsoft Endpoint Manager portal24](images/2c2e87c5fedc87eba17be0cdeffdb17f.png)</span><span class="sxs-lookup"><span data-stu-id="79097-216">![Image of Microsoft Endpoint Manager portal24](images/2c2e87c5fedc87eba17be0cdeffdb17f.png)</span></span>

10. <span data-ttu-id="79097-217">Afficher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="79097-217">View the policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-218">![Image de Microsoft Endpoint Manager portal25](images/7a631d17cc42500dacad4e995823ffef.png)</span><span class="sxs-lookup"><span data-stu-id="79097-218">![Image of Microsoft Endpoint Manager portal25](images/7a631d17cc42500dacad4e995823ffef.png)</span></span>

### <a name="attack-surface-reduction--web-protection"></a><span data-ttu-id="79097-219">Réduction de la surface d'attaque – Protection Web</span><span class="sxs-lookup"><span data-stu-id="79097-219">Attack Surface Reduction – Web Protection</span></span>

1.  <span data-ttu-id="79097-220">Ouvrez le portail MEM.</span><span class="sxs-lookup"><span data-stu-id="79097-220">Open the MEM portal.</span></span>

2.  <span data-ttu-id="79097-221">Accédez à **Endpoint Security > Attack surface reduction**.</span><span class="sxs-lookup"><span data-stu-id="79097-221">Navigate to **Endpoint security > Attack surface reduction**.</span></span>

3.  <span data-ttu-id="79097-222">Sélectionnez **Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="79097-222">Select  **Create Policy**.</span></span>

4.  <span data-ttu-id="79097-223">Select **Windows 10 and Later – Web protection > Create**.</span><span class="sxs-lookup"><span data-stu-id="79097-223">Select **Windows 10 and Later – Web protection > Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-224">![Image de Microsoft Endpoint Manager portal26](images/cd7b5a1cbc16cc05f878cdc99ba4c27f.png)</span><span class="sxs-lookup"><span data-stu-id="79097-224">![Image of Microsoft Endpoint Manager portal26](images/cd7b5a1cbc16cc05f878cdc99ba4c27f.png)</span></span>

5.  <span data-ttu-id="79097-225">Entrez un nom et une description, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-225">Enter a name and description, then select  **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-226">![Image de Microsoft Endpoint Manager portal27](images/5be573a60cd4fa56a86a6668b62dd808.png)</span><span class="sxs-lookup"><span data-stu-id="79097-226">![Image of Microsoft Endpoint Manager portal27](images/5be573a60cd4fa56a86a6668b62dd808.png)</span></span>

6.  <span data-ttu-id="79097-227">Dans la **page Paramètres de configuration**: définissez les configurations dont vous avez besoin pour la protection web, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="79097-227">In the **Configuration settings page**: Set the configurations you require for Web Protection, then select  **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79097-228">Nous configurons la protection Web sur Bloquer.</span><span class="sxs-lookup"><span data-stu-id="79097-228">We are configuring Web Protection to Block.</span></span>
    > 
    > <span data-ttu-id="79097-229">Pour plus d'informations, voir [Web Protection](web-protection-overview.md).</span><span class="sxs-lookup"><span data-stu-id="79097-229">For more information, see [Web Protection](web-protection-overview.md).</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-230">![Image de Microsoft Endpoint Manager portal28](images/6104aa33a56fab750cf30ecabef9f5b6.png)</span><span class="sxs-lookup"><span data-stu-id="79097-230">![Image of Microsoft Endpoint Manager portal28](images/6104aa33a56fab750cf30ecabef9f5b6.png)</span></span>

7.  <span data-ttu-id="79097-231">Ajoutez **des balises d'étendue comme > suivant**.</span><span class="sxs-lookup"><span data-stu-id="79097-231">Add **Scope Tags as required > Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-232">![Image de Microsoft Endpoint Manager portal29](images/6daa8d347c98fe94a0d9c22797ff6f28.png)</span><span class="sxs-lookup"><span data-stu-id="79097-232">![Image of Microsoft Endpoint Manager portal29](images/6daa8d347c98fe94a0d9c22797ff6f28.png)</span></span>

8.  <span data-ttu-id="79097-233">Sélectionnez **Affecter au groupe de test > Suivant**.</span><span class="sxs-lookup"><span data-stu-id="79097-233">Select **Assign to test group > Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-234">![Image de Microsoft Endpoint Manager portal30](images/45cefc8e4e474321b4d47b4626346597.png)</span><span class="sxs-lookup"><span data-stu-id="79097-234">![Image of Microsoft Endpoint Manager portal30](images/45cefc8e4e474321b4d47b4626346597.png)</span></span>

9.  <span data-ttu-id="79097-235">Select **Review and Create > Create**.</span><span class="sxs-lookup"><span data-stu-id="79097-235">Select **Review and Create > Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-236">![Image de Microsoft Endpoint Manager portal31](images/8ee0405f1a96c23d2eb6f737f11c1ae5.png)</span><span class="sxs-lookup"><span data-stu-id="79097-236">![Image of Microsoft Endpoint Manager portal31](images/8ee0405f1a96c23d2eb6f737f11c1ae5.png)</span></span>

10. <span data-ttu-id="79097-237">Afficher la stratégie.</span><span class="sxs-lookup"><span data-stu-id="79097-237">View the policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-238">![Image de Microsoft Endpoint Manager portal32](images/e74f6f6c150d017a286e6ed3dffb7757.png)</span><span class="sxs-lookup"><span data-stu-id="79097-238">![Image of Microsoft Endpoint Manager portal32](images/e74f6f6c150d017a286e6ed3dffb7757.png)</span></span>

## <a name="validate-configuration-settings"></a><span data-ttu-id="79097-239">Valider les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="79097-239">Validate configuration settings</span></span>


### <a name="confirm-policies-have-been-applied"></a><span data-ttu-id="79097-240">Confirmer que les stratégies ont été appliquées</span><span class="sxs-lookup"><span data-stu-id="79097-240">Confirm Policies have been applied</span></span>


<span data-ttu-id="79097-241">Une fois que la stratégie de configuration a été affectée, l'application prend un certain temps.</span><span class="sxs-lookup"><span data-stu-id="79097-241">Once the Configuration policy has been assigned, it will take some time to apply.</span></span>

<span data-ttu-id="79097-242">Pour plus d'informations sur le minutage, consultez [les informations de configuration d'Intune.](https://docs.microsoft.com/mem/intune/configuration/device-profile-troubleshoot#how-long-does-it-take-for-devices-to-get-a-policy-profile-or-app-after-they-are-assigned)</span><span class="sxs-lookup"><span data-stu-id="79097-242">For information on timing, see [Intune configuration information](https://docs.microsoft.com/mem/intune/configuration/device-profile-troubleshoot#how-long-does-it-take-for-devices-to-get-a-policy-profile-or-app-after-they-are-assigned).</span></span>

<span data-ttu-id="79097-243">Pour vérifier que la stratégie de configuration a été appliquée à votre périphérique de test, suivez le processus suivant pour chaque stratégie de configuration.</span><span class="sxs-lookup"><span data-stu-id="79097-243">To confirm that the configuration policy has been applied to your test device, follow the following process for each configuration policy.</span></span>

1.  <span data-ttu-id="79097-244">Ouvrez le portail MEM et accédez à la stratégie pertinente, comme indiqué dans les étapes ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="79097-244">Open the MEM portal and navigate to the relevant policy as shown in the steps above.</span></span> <span data-ttu-id="79097-245">L'exemple suivant illustre les paramètres de protection nouvelle génération.</span><span class="sxs-lookup"><span data-stu-id="79097-245">The following example shows the next generation protection settings.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-246">[![Image de Microsoft Endpoint Manager portal33 ](images/43ab6aa74471ee2977e154a4a5ef2d39.png)](images/43ab6aa74471ee2977e154a4a5ef2d39.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-246">[ ![Image of Microsoft Endpoint Manager portal33](images/43ab6aa74471ee2977e154a4a5ef2d39.png) ](images/43ab6aa74471ee2977e154a4a5ef2d39.png#lightbox)</span></span>

2.  <span data-ttu-id="79097-247">Sélectionnez la **stratégie de configuration** pour afficher l'état de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="79097-247">Select  the **Configuration Policy** to view the policy status.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-248">[![Image de Microsoft Endpoint Manager portal34 ](images/55ecaca0e4a022f0e29d45aeed724e6c.png)](images/55ecaca0e4a022f0e29d45aeed724e6c.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-248">[ ![Image of Microsoft Endpoint Manager portal34](images/55ecaca0e4a022f0e29d45aeed724e6c.png) ](images/55ecaca0e4a022f0e29d45aeed724e6c.png#lightbox)</span></span>

3.  <span data-ttu-id="79097-249">Sélectionnez  **État de l'appareil** pour voir l'état.</span><span class="sxs-lookup"><span data-stu-id="79097-249">Select  **Device Status** to see the status.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-250">[![Image de Microsoft Endpoint Manager portal35 ](images/18a50df62cc38749000dbfb48e9a4c9b.png)](images/18a50df62cc38749000dbfb48e9a4c9b.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-250">[ ![Image of Microsoft Endpoint Manager portal35](images/18a50df62cc38749000dbfb48e9a4c9b.png) ](images/18a50df62cc38749000dbfb48e9a4c9b.png#lightbox)</span></span>

4.  <span data-ttu-id="79097-251">Sélectionnez  **État de l'utilisateur** pour voir l'état.</span><span class="sxs-lookup"><span data-stu-id="79097-251">Select  **User Status** to see the status.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-252">[![Image de Microsoft Endpoint Manager portal36 ](images/4e965749ff71178af8873bc91f9fe525.png)](images/4e965749ff71178af8873bc91f9fe525.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-252">[ ![Image of Microsoft Endpoint Manager portal36](images/4e965749ff71178af8873bc91f9fe525.png) ](images/4e965749ff71178af8873bc91f9fe525.png#lightbox)</span></span>

5.  <span data-ttu-id="79097-253">Sélectionnez  **l'état par paramètre** pour voir l'état.</span><span class="sxs-lookup"><span data-stu-id="79097-253">Select  **Per-setting status** to see the status.</span></span>

    >[!TIP]
    ><span data-ttu-id="79097-254">Cet affichage est très utile pour identifier les paramètres qui entrent en conflit avec une autre stratégie.</span><span class="sxs-lookup"><span data-stu-id="79097-254">This view is very useful to identify any settings that conflict with another policy.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-255">[![Image de Microsoft Endpoint Manager portal37 ](images/42acc69d0128ed09804010bdbdf0a43c.png)](images/42acc69d0128ed09804010bdbdf0a43c.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-255">[ ![Image of Microsoft Endpoint Manager portal37](images/42acc69d0128ed09804010bdbdf0a43c.png) ](images/42acc69d0128ed09804010bdbdf0a43c.png#lightbox)</span></span>

### <a name="endpoint-detection-and-response"></a><span data-ttu-id="79097-256">Détection et réponse du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="79097-256">Endpoint detection and response</span></span>


1.  <span data-ttu-id="79097-257">Avant d'appliquer la configuration, le service Defender pour Endpoint Protection ne doit pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="79097-257">Before applying the configuration, the Defender for Endpoint Protection service should not be started.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-258">[![Image du panneau Services 1 ](images/b418a232a12b3d0a65fc98248dbb0e31.png)](images/b418a232a12b3d0a65fc98248dbb0e31.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-258">[ ![Image of Services panel1](images/b418a232a12b3d0a65fc98248dbb0e31.png) ](images/b418a232a12b3d0a65fc98248dbb0e31.png#lightbox)</span></span>

2.  <span data-ttu-id="79097-259">Une fois la configuration appliquée, le service Defender for Endpoint Protection doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="79097-259">After the configuration has been applied, the Defender for Endpoint Protection Service should be started.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-260">[![Image du panneau Services2 ](images/a621b699899f1b41db211170074ea59e.png)](images/a621b699899f1b41db211170074ea59e.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-260">[ ![Image of Services panel2](images/a621b699899f1b41db211170074ea59e.png) ](images/a621b699899f1b41db211170074ea59e.png#lightbox)</span></span>

3.  <span data-ttu-id="79097-261">Une fois que les services sont en cours d'exécution sur l'appareil, l'appareil apparaît dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="79097-261">After the services are running on the device, the device appears in Microsoft Defender Security Center.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-262">[![Image du Centre de sécurité Microsoft Defender ](images/df0c64001b9219cfbd10f8f81a273190.png)](images/df0c64001b9219cfbd10f8f81a273190.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79097-262">[ ![Image of Microsoft Defender Security Center](images/df0c64001b9219cfbd10f8f81a273190.png) ](images/df0c64001b9219cfbd10f8f81a273190.png#lightbox)</span></span>

### <a name="next-generation-protection"></a><span data-ttu-id="79097-263">Protection de nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="79097-263">Next-generation protection</span></span>

1.  <span data-ttu-id="79097-264">Avant d'appliquer la stratégie sur un périphérique de test, vous devez être en mesure de gérer manuellement les paramètres, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="79097-264">Before applying the policy on a test device, you should be able to manually manage the settings as shown below.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-265">![Image du paramètre page1](images/88efb4c3710493a53f2840c3eac3e3d3.png)</span><span class="sxs-lookup"><span data-stu-id="79097-265">![Image of setting page1](images/88efb4c3710493a53f2840c3eac3e3d3.png)</span></span>

2.  <span data-ttu-id="79097-266">Une fois la stratégie appliquée, vous ne devez pas être en mesure de gérer manuellement les paramètres.</span><span class="sxs-lookup"><span data-stu-id="79097-266">After the policy has been applied, you should not be able to manually manage the settings.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79097-267">Dans l'image **suivante,** activer la protection cloud et activer la **protection** en temps réel sont affichés comme gérés.</span><span class="sxs-lookup"><span data-stu-id="79097-267">In the following image **Turn on cloud-delivered protection** and **Turn on real-time protection** are being shown as managed.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="79097-268">![Image du paramètre page2](images/9341428b2d3164ca63d7d4eaa5cff642.png)</span><span class="sxs-lookup"><span data-stu-id="79097-268">![Image of setting page2](images/9341428b2d3164ca63d7d4eaa5cff642.png)</span></span>

### <a name="attack-surface-reduction--attack-surface-reduction-rules"></a><span data-ttu-id="79097-269">Réduction de la surface d'attaque : règles de réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="79097-269">Attack Surface Reduction – Attack surface reduction rules</span></span>


1.  <span data-ttu-id="79097-270">Avant d'appliquer la stratégie sur un périphérique de test, stylet une fenêtre PowerShell et tapez `Get-MpPreference` .</span><span class="sxs-lookup"><span data-stu-id="79097-270">Before applying the policy on a test device, pen a PowerShell Window and type `Get-MpPreference`.</span></span>

2.  <span data-ttu-id="79097-271">Cela doit répondre avec les lignes suivantes sans contenu :</span><span class="sxs-lookup"><span data-stu-id="79097-271">This should respond with the following lines with no content:</span></span>

    > <span data-ttu-id="79097-272">AttackSurfaceReductionOnlyExclusions :</span><span class="sxs-lookup"><span data-stu-id="79097-272">AttackSurfaceReductionOnlyExclusions:</span></span>
    > 
    > <span data-ttu-id="79097-273">AttackSurfaceReductionRules_Actions :</span><span class="sxs-lookup"><span data-stu-id="79097-273">AttackSurfaceReductionRules_Actions:</span></span>
    > 
    > <span data-ttu-id="79097-274">AttackSurfaceReductionRules_Ids :</span><span class="sxs-lookup"><span data-stu-id="79097-274">AttackSurfaceReductionRules_Ids:</span></span>

    ![Image de la ligne de commande 1](images/cb0260d4b2636814e37eee427211fe71.png)

3.  <span data-ttu-id="79097-276">Après avoir appliqué la stratégie sur un périphérique de test, ouvrez un Windows PowerShell et tapez `Get-MpPreference` .</span><span class="sxs-lookup"><span data-stu-id="79097-276">After applying the policy on a test device, open a PowerShell Windows and type `Get-MpPreference`.</span></span>

4.  <span data-ttu-id="79097-277">Cela doit répondre avec les lignes suivantes avec le contenu comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="79097-277">This should respond with the following lines with content as shown below:</span></span>

    ![Image de la ligne de commande 2](images/619fb877791b1fc8bc7dfae1a579043d.png)

### <a name="attack-surface-reduction--web-protection"></a><span data-ttu-id="79097-279">Réduction de la surface d'attaque – Protection Web</span><span class="sxs-lookup"><span data-stu-id="79097-279">Attack Surface Reduction – Web Protection</span></span>

1.  <span data-ttu-id="79097-280">Sur l'appareil de test, ouvrez un Windows PowerShell et tapez `(Get-MpPreference).EnableNetworkProtection` .</span><span class="sxs-lookup"><span data-stu-id="79097-280">On the test device, open a PowerShell Windows and type `(Get-MpPreference).EnableNetworkProtection`.</span></span>

2.  <span data-ttu-id="79097-281">Cela doit répondre avec un 0 comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="79097-281">This should respond with a 0 as shown below.</span></span>

    ![Image de la ligne de commande 3](images/196a8e194ac99d84221f405d0f684f8c.png)

3.  <span data-ttu-id="79097-283">Après avoir appliqué la stratégie, ouvrez un Windows PowerShell et tapez `(Get-MpPreference).EnableNetworkProtection` .</span><span class="sxs-lookup"><span data-stu-id="79097-283">After applying the policy, open a PowerShell Windows and type `(Get-MpPreference).EnableNetworkProtection`.</span></span>

4.  <span data-ttu-id="79097-284">Cela doit répondre avec un 1, comme illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="79097-284">This should respond with a 1 as shown below.</span></span>

    ![Image de la ligne de commande 4](images/c06fa3bbc2f70d59dfe1e106cd9a4683.png)
