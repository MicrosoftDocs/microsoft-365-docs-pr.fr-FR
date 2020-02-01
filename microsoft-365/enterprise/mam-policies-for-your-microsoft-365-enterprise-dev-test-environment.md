---
title: Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 Enterprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/09/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour ajouter des stratégies de conformité d’appareil Intune à votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: f5d258dd9b4e0ff8799534cce64818a7fdaf663e
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600901"
---
# <a name="device-compliance-policies-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="09464-103">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="09464-103">Device compliance policies for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="09464-104">*Ce Guide de Laboratoire Test peut uniquement être utilisé pour les environnements de test Microsoft 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="09464-104">*This Test Lab Guide can only be used for Microsoft 365 Enterprise test environments.*</span></span>

<span data-ttu-id="09464-105">À l’aide des instructions fournies dans cet article, vous ajoutez une stratégie Intune Device Compliance pour les appareils Windows 10 et Office 365 ProPlus à votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="09464-105">With the instructions in this article, you add an Intune device compliance policy for Windows 10 devices and Office 365 ProPlus to your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="09464-107">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="09464-107">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="09464-108">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="09464-108">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="09464-109">Si vous souhaitez simplement configurer des stratégies MAM de manière simple avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="09464-109">If you just want to configure MAM policies in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="09464-110">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="09464-110">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="09464-111">Le test des licences automatisées et l’appartenance aux groupes ne nécessitent pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="09464-111">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="09464-112">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="09464-112">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="09464-113">Phase 2 : créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="09464-113">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="09464-114">Au cours de cette phase, vous allez créer une stratégie de conformité des appareils pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="09464-114">In this phase, you create a device compliance policy for Windows 10 devices.</span></span>
  
1. <span data-ttu-id="09464-115">Accédez au portail Office 365 à l’adresse[https://portal.office.com](https://portal.office.com)() et connectez-vous à votre abonnement de laboratoire de test Office 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="09464-115">Go to the Office 365 portal at ([https://portal.office.com](https://portal.office.com)) and sign in to your Office 365 test lab subscription with your global administrator account.</span></span>
    
2. <span data-ttu-id="09464-116">Dans un nouvel onglet de votre navigateur, ouvrez le portail Azure à [https://portal.azure.com](https://portal.azure.com)l’adresse.</span><span class="sxs-lookup"><span data-stu-id="09464-116">On a new tab of your browser, open the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>

3. <span data-ttu-id="09464-117">Dans l’onglet portail Azure de votre navigateur, saisissez **Intune** dans la zone de recherche, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="09464-117">From the Azure portal tab in your browser, type **Intune** in the search box, and then click **Intune**.</span></span>
    
4. <span data-ttu-id="09464-118">Si vous voyez un message « **vous n’avez pas activé la gestion des appareils activés** » dans le volet **Microsoft Intune** , cliquez sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="09464-118">If you see a **You haven't enabled device management yet** message In the **Microsoft Intune** pane, click it.</span></span> <span data-ttu-id="09464-119">Dans le volet **autorité de gestion des appareils mobiles** , cliquez sur **autorité MDM Intune**, puis sur **choisir**.</span><span class="sxs-lookup"><span data-stu-id="09464-119">In the **Mobile Device Management authority** pane, click **Intune MDM Authority**, and then click **Choose**.</span></span> <span data-ttu-id="09464-120">Actualisez l’onglet de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="09464-120">Refresh your browser tab.</span></span>
    
5. <span data-ttu-id="09464-121">Dans le volet de navigation gauche, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="09464-121">In the left navigation pane, click **Groups**.</span></span>
    
6. <span data-ttu-id="09464-122">Dans le volet **groupes-tous les groupes** , cliquez sur **+ nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="09464-122">In the **Groups-All groups** pane, click **+ New Group**.</span></span>
    
7. <span data-ttu-id="09464-123">Dans le **volet groupe** , sélectionnez **Office 365** ou **sécurité** pour **type de groupe ?**, entrez **utilisateurs d’appareils Windows 10 gérés** dans **nom**, sélectionnez **attribué** dans **type d’appartenance**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="09464-123">In the **Group** pane, select **Office 365** or **Security** for **Group type?**, type **Managed Windows 10 device users** in **Name**, select **Assigned** in **Membership type**,  and then click **Create**.</span></span> 
    
8. <span data-ttu-id="09464-124">Cliquez sur **Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="09464-124">Click **Microsoft Intune**.</span></span> <span data-ttu-id="09464-125">Dans le volet **Microsoft Intune** , dans la liste **tâches rapides** , cliquez sur **créer une stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="09464-125">In the **Microsoft Intune** pane, in the **Quick tasks** list, click **Create a compliance policy**.</span></span>
    
9. <span data-ttu-id="09464-126">Dans le volet **profils de stratégie de conformité** , cliquez sur créer une **stratégie**.</span><span class="sxs-lookup"><span data-stu-id="09464-126">In the **Compliance Policy Profiles** pane, click **Create Policy**.</span></span>
    
10. <span data-ttu-id="09464-127">Dans le volet **créer une stratégie** , dans **nom**, tapez **Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="09464-127">In the **Create Policy** pane, in **Name**, type **Windows 10**.</span></span> <span data-ttu-id="09464-128">Dans **plateforme**, sélectionnez **Windows 10 et versions ultérieures**, cliquez sur **OK** dans le volet **stratégie de conformité Windows 10** , puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="09464-128">In **Platform**, select **Windows 10 and later**, click **OK** In the **Windows 10 compliance policy** pane, and then click **Create**.</span></span> 
    
11. <span data-ttu-id="09464-129">Cliquez sur **profils de stratégie de conformité**, puis sur le nom de la stratégie **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="09464-129">Click **Compliance Policy Profiles**, and then click the **Windows 10** policy name.</span></span>
    
12. <span data-ttu-id="09464-130">Dans le volet **Windows 10** , cliquez sur **affectations**, puis sur **Sélectionner les groupes à inclure**.</span><span class="sxs-lookup"><span data-stu-id="09464-130">In the **Windows 10** pane, click **Assignments**, and then click **Select groups to include**.</span></span>
    
13. <span data-ttu-id="09464-131">Dans le volet **Sélectionner des groupes à inclure** , cliquez sur le groupe **utilisateurs d’appareils Windows 10 gérés** , puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="09464-131">In the **Select groups to include** pane, click the **Managed Windows 10 device users** group, and then click **Select**.</span></span>
    
14. <span data-ttu-id="09464-132">Cliquez sur **Enregistrer**, sur **Microsoft Intune-vue d’ensemble**, puis sur **applications clientes** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="09464-132">Click **Save**, click **Microsoft Intune-Overview**, and then click **Client apps** in the left navigation.</span></span>
    
15. <span data-ttu-id="09464-133">Dans le volet **applications client** , cliquez sur **applications**, puis sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="09464-133">In the **Client Apps** pane, click **Apps**, and then click **Add**.</span></span> 

16. <span data-ttu-id="09464-134">Dans le volet **Ajouter une application** , sélectionnez type d' **application**, puis sélectionnez **Windows 10** sous la **suite Office 365**.</span><span class="sxs-lookup"><span data-stu-id="09464-134">In the **Add app** pane, select **App type**, and then select **Windows 10** under **Office 365 Suite**.</span></span>

17. <span data-ttu-id="09464-135">Dans le volet **Ajouter une application** , sélectionnez **informations sur la suite d’applications**.</span><span class="sxs-lookup"><span data-stu-id="09464-135">In the **Add App** pane, select **App Suite Information**.</span></span>
 
18. <span data-ttu-id="09464-136">Dans le volet d' **informations App suite** , tapez **Office 365 ProPlus** dans la **Description**de la suite et du nom de la **suite** .</span><span class="sxs-lookup"><span data-stu-id="09464-136">In the **App Suite Information** pane, type **Office 365 ProPlus** in both **Suite Name** and **Suite Description**.</span></span>
<span data-ttu-id="09464-137">Cliquez sur OK.</span><span class="sxs-lookup"><span data-stu-id="09464-137">Click OK.</span></span>

19. <span data-ttu-id="09464-138">Dans le volet **Ajouter une application** , sélectionnez configurer une suite d' **applications**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="09464-138">In the **Add App** pane, select **Configure App Suite**, and then click **OK**.</span></span>

20. <span data-ttu-id="09464-139">Dans le volet **Ajouter une application** , sélectionnez Paramètres de la suite d' **applications**.</span><span class="sxs-lookup"><span data-stu-id="09464-139">In the **Add App** pane, select **App Suite Settings**.</span></span>

21. <span data-ttu-id="09464-140">Pour **canal de mise à jour**, sélectionnez **semi-annuel**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="09464-140">For **Update Channel**, select **Semi-Annual**, and then click **OK**.</span></span>

22. <span data-ttu-id="09464-141">Dans le volet **Ajouter une application** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="09464-141">In the **Add app** pane, click **Add**.</span></span>

<span data-ttu-id="09464-142">Vous disposez maintenant d’une stratégie de conformité de l’appareil pour tester les applications sélectionnées dans la stratégie de conformité des appareils **Windows 10** et pour les membres du groupe **utilisateurs d’appareils Windows 10 gérés** .</span><span class="sxs-lookup"><span data-stu-id="09464-142">You now have a device compliance policy for testing the selected apps in the **Windows 10** device compliance policy and for members of the **Managed Windows 10 device users** group.</span></span> <span data-ttu-id="09464-143">Notez que si vous sélectionnez Office 365 comme type de groupe, des ressources supplémentaires seront créées.</span><span class="sxs-lookup"><span data-stu-id="09464-143">Please note that selecting Office 365 as the group type will create additional resources.</span></span> 
  
## <a name="next-step"></a><span data-ttu-id="09464-144">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="09464-144">Next step</span></span>

<span data-ttu-id="09464-145">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="09464-145">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="09464-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09464-146">See also</span></span>

<span data-ttu-id="09464-147">[Guides de laboratoire de test Microsoft 365 Enterprise](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="09464-147">[Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="09464-148">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="09464-148">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="09464-149">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="09464-149">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="09464-150">Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="09464-150">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
