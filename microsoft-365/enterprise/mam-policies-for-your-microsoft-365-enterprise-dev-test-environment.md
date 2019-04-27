---
title: Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour ajouter des stratégies de conformité d'appareil Intune à votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: d20b050bfc56776656bf1d485b2e107a9debe2f7
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33353186"
---
# <a name="device-compliance-policies-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="b5bd1-103">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5bd1-103">Device compliance policies for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="b5bd1-104">À l'aide des instructions fournies dans cet article, vous ajoutez une stratégie Intune Device Compliance à votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-104">With the instructions in this article, you add an Intune device compliance policy to your Microsoft 365 Enterprise test environment.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="b5bd1-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="b5bd1-107">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5bd1-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="b5bd1-108">Si vous souhaitez simplement configurer des stratégies MAM de manière simple avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="b5bd1-108">If you just want to configure MAM policies in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="b5bd1-109">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b5bd1-109">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b5bd1-110">Le test des licences automatisées et l'appartenance aux groupes ne nécessitent pas l'environnement de test d'entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d'annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b5bd1-110">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="b5bd1-111">Elle est fournie ici en tant qu'option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-111">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="b5bd1-112">Phase 2: créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="b5bd1-112">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="b5bd1-113">Au cours de cette phase, vous allez créer une stratégie de conformité des appareils pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-113">In this phase, you create a device compliance policy for Windows 10 devices.</span></span>
  
1. <span data-ttu-id="b5bd1-114">Accédez au portail Office 365 à l'adresse[https://portal.office.com](https://portal.office.com)() et connectez-vous à votre abonnement de laboratoire de test Office 365 avec votre compte d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-114">Go to the Office 365 portal at ([https://portal.office.com](https://portal.office.com)) and sign in to your Office 365 test lab subscription with your global administrator account.</span></span>
    
2. <span data-ttu-id="b5bd1-115">Dans un nouvel onglet de votre navigateur, ouvrez le portail Azure à [https://portal.azure.com](https://portal.azure.com)l'adresse.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-115">On a new tab of your browser, open the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>

3. <span data-ttu-id="b5bd1-116">Sur l'onglet portail Azure de votre navigateur, dans le volet de navigation, cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-116">On the Azure portal tab in your browser, in the navigation pane, click **All services**, type **Intune**, and then click **Intune**.</span></span>
    
4. <span data-ttu-id="b5bd1-117">Si vous voyez un message « **vous n'avez pas encore activé la gestion des appareils** sur le panneau **Microsoft Intune** , cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-117">If you see a **You haven't enabled device management yet** message on the **Microsoft Intune** blade, click it.</span></span> <span data-ttu-id="b5bd1-118">Dans le panneau **autorité de gestion des appareils mobiles** , cliquez sur **autorité MDM Intune**, puis sur **choisir**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-118">On the **Mobile Device Management authority** blade, click **Intune MDM Authority**, and then click **Choose**.</span></span> <span data-ttu-id="b5bd1-119">Actualisez l'onglet de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-119">Refresh your browser tab.</span></span>
    
5. <span data-ttu-id="b5bd1-120">Dans le volet de navigation gauche, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-120">In the left navigation pane, click **Groups**.</span></span>
    
6. <span data-ttu-id="b5bd1-121">Dans le panneau **groupes-tous les groupes** , cliquez sur **+ nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-121">On the **Groups-All groups** blade, click **+ New Group**.</span></span>
    
7. <span data-ttu-id="b5bd1-122">Dans le volet **groupe** , sélectionnez **Office 365** pour **type de groupe?**, entrez **utilisateurs d'appareils Windows 10 gérés** dans **nom**, sélectionnez **attribué** dans **type d'appartenance**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-122">On the **Group** blade, select **Office 365** for **Group type?**, type **Managed Windows 10 device users** in **Name**, select **Assigned** in **Membership type**,  and then click **Create**.</span></span> 
    
8. <span data-ttu-id="b5bd1-123">Fermez le volet **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-123">Close the **Group** blade.</span></span>
    
11. <span data-ttu-id="b5bd1-124">Fermez le panneau **groupes-tous les groupes** .</span><span class="sxs-lookup"><span data-stu-id="b5bd1-124">Close the **Groups-All groups** blade.</span></span>
    
12. <span data-ttu-id="b5bd1-125">Sur le panneau **Microsoft Intune** , dans la liste **tâches rapides** , cliquez sur **créer une stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-125">On the **Microsoft Intune** blade, in the **Quick tasks** list, click **Create a compliance policy**.</span></span>
    
13. <span data-ttu-id="b5bd1-126">Dans le volet **Profils de stratégie de conformité**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-126">On the **Compliance Policy Profiles** blade, click **Create Policy**.</span></span>
    
14. <span data-ttu-id="b5bd1-127">Dans le panneau **créer une stratégie** , dans **nom**, tapez **Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-127">On the **Create Policy** blade, in **Name**, type **Windows 10**.</span></span> <span data-ttu-id="b5bd1-128">Dans **plateforme**, sélectionnez **Windows 10 et versions ultérieures**, cliquez sur **OK** dans le panneau de **stratégie de conformité Windows 10** , puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-128">In **Platform**, select **Windows 10 and later**, click **OK** on the **Windows 10 compliance policy** blade, and then click **Create**.</span></span> <span data-ttu-id="b5bd1-129">Fermez la lame **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="b5bd1-129">Close the **Windows 10** blade.</span></span>
    
15. <span data-ttu-id="b5bd1-130">Dans le panneau **profils de stratégie de conformité** , cliquez sur le nom de la stratégie **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="b5bd1-130">On the **Compliance Policy Profiles** blade, click the **Windows 10** policy name.</span></span>
    
16. <span data-ttu-id="b5bd1-131">Dans le panneau **Windows 10** , cliquez sur **affectations**, puis sur Sélectionner les **groupes à inclure**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-131">On the **Windows 10** blade, click **Assignments**, and then click **Select groups to include**.</span></span>
    
17. <span data-ttu-id="b5bd1-132">Sur le panneau **Sélectionner les groupes à inclure** , cliquez sur le groupe **utilisateurs d'appareils Windows 10 gérés** , puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-132">On the **Select groups to include** blade, click the **Managed Windows 10 device users** group, and then click **Select**.</span></span>
    
18. <span data-ttu-id="b5bd1-133">Cliquez sur **Enregistrer**, puis fermez le panneau affectations de **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="b5bd1-133">Click **Save**, and then close the **Windows 10 - Assignments** blade.</span></span>
    
19. <span data-ttu-id="b5bd1-134">Fermez le volet **Profils de stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-134">Close the **Compliance Policy Profiles** blade.</span></span>
    
20. <span data-ttu-id="b5bd1-135">Sur le panneau **Microsoft Intune** , cliquez sur **applications clientes** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-135">On the **Microsoft Intune** blade, click **Client apps** in the left navigation.</span></span>
    
21. <span data-ttu-id="b5bd1-136">Dans le panneau **applications clientes** , cliquez sur **applications**, puis sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-136">On the **Client Apps** blade, click **Apps**, and then click **Add**.</span></span> 

22. <span data-ttu-id="b5bd1-137">Dans le panneau **Ajouter une application** , sélectionnez type d' **application**, puis sélectionnez **Windows 10** sous la **suite Office 365**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-137">In the **Add app** blade, select **App type**, and then select **Windows 10** under **Office 365 Suite**.</span></span>

23. <span data-ttu-id="b5bd1-138">Cliquez sur **configurer l'application suite**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-138">Click **Configure App Suite**, and then click **OK**.</span></span>

24. <span data-ttu-id="b5bd1-139">Cliquez sur informations sur la **suite d'applications**, tapez **applications Office pour Windows 10** dans la **suite nom**, **applications Office pour Windows 10** dans la **Description**de la suite, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-139">Click **App Suite Information**, type **Office Apps for Windows 10** in **Suite Name**, **Office Apps for Windows 10** in **Suite Description**, and then click **OK**.</span></span>

25. <span data-ttu-id="b5bd1-140">Cliquez sur paramètres de la **suite d'applications**, sélectionnez **semi-annuel** dans **canal de mise à jour**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-140">Click **App Suite Settings**, select **Semi-Annual** in **Update channel**, and then click **OK**.</span></span>

26. <span data-ttu-id="b5bd1-141">Dans le panneau **Ajouter une application** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-141">On the **Add app** blade, click **Add**.</span></span>

<span data-ttu-id="b5bd1-142">Vous disposez maintenant d'une stratégie de conformité de l'appareil pour tester les applications sélectionnées dans la stratégie de conformité des appareils **Windows 10** et pour les membres du groupe **utilisateurs d'appareils Windows 10 gérés** .</span><span class="sxs-lookup"><span data-stu-id="b5bd1-142">You now have a device compliance policy for testing the selected apps in the **Windows 10** device compliance policy and for members of the **Managed Windows 10 device users** group.</span></span> 
  
## <a name="next-step"></a><span data-ttu-id="b5bd1-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b5bd1-143">Next step</span></span>

<span data-ttu-id="b5bd1-144">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="b5bd1-144">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5bd1-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5bd1-145">See also</span></span>

<span data-ttu-id="b5bd1-146">[Guides de laboratoire de test Microsoft 365 Enterprise](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="b5bd1-146">[Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="b5bd1-147">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="b5bd1-147">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="b5bd1-148">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="b5bd1-148">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="b5bd1-149">Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="b5bd1-149">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
