---
title: Inscription d’appareils iOS et Android dans votre environnement de test Microsoft 365 Entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
ms.assetid: 49c7758a-1c01-4153-9b63-5eae3f6305ce
description: Utilisez ce Guide de laboratoire de Test pour inscrire des périphériques dans votre environnement de test Microsoft 365 et les gérer à distance.
ms.openlocfilehash: a78db19099ccacd1b2f62e8438d1749f28d22f52
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866976"
---
# <a name="enroll-ios-and-android-devices-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="4f71e-103">Inscription d’appareils iOS et Android dans votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4f71e-103">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="4f71e-104">En suivant les instructions fournies dans cet article, vous serez en mesure de s’inscrire et tester les fonctionnalités de gestion de base des périphériques mobiles pour les périphériques iOS ou Android dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="4f71e-104">By following the instructions provided in this article, you'll be able to enroll and test basic mobile device management capabilities for iOS and Android devices in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="4f71e-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="4f71e-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="4f71e-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="4f71e-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="4f71e-108">Si vous souhaitez simplement inscrire les périphériques iOS ou Android de manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="4f71e-108">If you just want to enroll iOS and Android devices in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="4f71e-109">Si vous souhaitez inscrire les périphériques iOS ou Android dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4f71e-109">If you want to enroll iOS and Android devices in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="4f71e-p101">Test automatisé de gestion des licences et l’appartenance au groupe ne nécessite pas de l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="4f71e-p101">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-enroll-your-ios-and-android-devices"></a><span data-ttu-id="4f71e-112">Phase 2 : Inscrire vos périphériques iOS ou Android</span><span class="sxs-lookup"><span data-stu-id="4f71e-112">Phase 2: Enroll your iOS and Android devices</span></span>

<span data-ttu-id="4f71e-113">Tout d’abord, suivez les instructions fournies dans [installer et se connecter à l’application de portail d’entreprise](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) pour personnaliser l’application de portail d’entreprise Microsoft Intune pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="4f71e-113">First, use the instructions in [Install and sign in to the Company Portal app](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) to customize the Microsoft Intune Company Portal app for your test environment.</span></span>

<span data-ttu-id="4f71e-114">Ensuite, suivez les instructions de [configurer l’accès aux ressources de votre société](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) à inscrire un périphérique iOS.</span><span class="sxs-lookup"><span data-stu-id="4f71e-114">Next, use the instructions in [Set up access to your company resources](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) to enroll an iOS device.</span></span>

<span data-ttu-id="4f71e-115">Ensuite, suivez les instructions dans [l’inscription de votre appareil Android dans Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) pour inscrire un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="4f71e-115">Next, use the instructions in [Enroll your Android device in Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) to enroll an Android device.</span></span>

## <a name="phase-3-manage-your-ios-and-android-devices-remotely"></a><span data-ttu-id="4f71e-116">Phase 3 : Gérer vos périphériques iOS ou Android à distance</span><span class="sxs-lookup"><span data-stu-id="4f71e-116">Phase 3: Manage your iOS and Android devices remotely</span></span>

<span data-ttu-id="4f71e-p102">Intune Microsoft fournit à distance verrouillage et code secret réinitialisation de fonctionnalités. Si une personne perd leur appareil, vous pouvez verrouiller le périphérique à distance. Si une personne oublie son code confidentiel, vous pouvez le réinitialiser à distance.</span><span class="sxs-lookup"><span data-stu-id="4f71e-p102">Microsoft Intune provides both remote lock and passcode reset capabilities. If someone loses their device, you can lock the device remotely. If someone forgets their passcode, you can reset it remotely.</span></span>
  
<span data-ttu-id="4f71e-120">Pour verrouiller une iOS ou un appareil Android à distance :</span><span class="sxs-lookup"><span data-stu-id="4f71e-120">To lock an iOS or Android device remotely:</span></span>

1. <span data-ttu-id="4f71e-121">Connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) avec les informations d’identification de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="4f71e-121">Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="4f71e-122">Cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="4f71e-122">Click **All services**, type **Intune**, and then click **Intune**.</span></span>
3. <span data-ttu-id="4f71e-123">Cliquez sur **périphériques > tous les périphériques**.</span><span class="sxs-lookup"><span data-stu-id="4f71e-123">Click **Devices > All devices**.</span></span>
4. <span data-ttu-id="4f71e-124">Dans la liste des périphériques, cliquez sur un appareil Android ou sur iOS, puis cliquez sur l’action **Verrouiller à distance** .</span><span class="sxs-lookup"><span data-stu-id="4f71e-124">In the list of devices, click an iOS or Android device, and then click the **Remote lock** action.</span></span>

    
<span data-ttu-id="4f71e-125">Pour réinitialiser le code secret à distance, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4f71e-125">To reset the passcode remotely:</span></span>

1. <span data-ttu-id="4f71e-126">Si nécessaire, connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) avec les informations d’identification de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="4f71e-126">If needed, sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="4f71e-127">Cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="4f71e-127">Click **All services**, type **Intune**, and then click **Intune**.</span></span>
3. <span data-ttu-id="4f71e-128">Cliquez sur **périphériques > tous les périphériques**.</span><span class="sxs-lookup"><span data-stu-id="4f71e-128">Click **Devices > All devices**.</span></span>
4. <span data-ttu-id="4f71e-p103">Dans la liste des périphériques gérer, cliquez sur un appareil Android ou sur iOS et choisissez **... Plus**. Puis sélectionnez l’action **Supprimer le code secret** périphérique à distance.</span><span class="sxs-lookup"><span data-stu-id="4f71e-p103">From the list of devices you manage, click an iOS or Android device, and choose **...More**. Then choose the **Remove passcode** device remote action.</span></span>

<span data-ttu-id="4f71e-131">Pour une expérimentation supplémentaire, voir [actions de périphérique disponible](https://docs.microsoft.com/intune/device-management#available-device-actions).</span><span class="sxs-lookup"><span data-stu-id="4f71e-131">For additional experimentation, see [Available device actions](https://docs.microsoft.com/intune/device-management#available-device-actions).</span></span>

    
## <a name="next-step"></a><span data-ttu-id="4f71e-132">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="4f71e-132">Next step</span></span>

<span data-ttu-id="4f71e-133">Explorez des fonctionnalités de [Gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="4f71e-133">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f71e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f71e-134">See Also</span></span>

[<span data-ttu-id="4f71e-135">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4f71e-135">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)
  
[<span data-ttu-id="4f71e-136">Environnement de test des stratégies de conformité de périphérique pour votre entreprise 365 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="4f71e-136">Device compliance policies for your Microsoft 365 Enterprise test environment</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
  
[<span data-ttu-id="4f71e-137">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4f71e-137">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="4f71e-138">Mobilité d’entreprise + sécurité (EMS)</span><span class="sxs-lookup"><span data-stu-id="4f71e-138">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
