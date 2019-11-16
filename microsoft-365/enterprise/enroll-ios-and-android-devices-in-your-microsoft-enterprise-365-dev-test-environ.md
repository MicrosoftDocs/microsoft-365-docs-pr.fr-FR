---
title: Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/11/2018
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom: Ent_TLGs
ms.assetid: 49c7758a-1c01-4153-9b63-5eae3f6305ce
description: Utilisez ce guide de laboratoire de test pour inscrire des appareils dans votre environnement de test Microsoft 365 et les gérer à distance.
ms.openlocfilehash: ea583a5f14acb2162d22da6d53d533246cbb035e
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38672650"
---
# <a name="enroll-ios-and-android-devices-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="272d5-103">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="272d5-103">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="272d5-104">*Ce guide de laboratoire de test ne peut être utilisé qu’avec un environnement de test Microsoft 365 Enterprise.*</span><span class="sxs-lookup"><span data-stu-id="272d5-104">*This Test Lab Guide can be only used with a Microsoft 365 Enterprise test environment.*</span></span>

<span data-ttu-id="272d5-105">En suivant les instructions fournies dans cet article, vous serez en mesure d’inscrire et de tester des fonctionnalités de gestion des appareils mobiles de base pour les appareils iOS et Android dans votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="272d5-105">By following the instructions provided in this article, you'll be able to enroll and test basic mobile device management capabilities for iOS and Android devices in your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="272d5-107">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="272d5-107">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="272d5-108">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="272d5-108">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="272d5-109">Si vous souhaitez simplement inscrire des appareils iOS et Android de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="272d5-109">If you just want to enroll iOS and Android devices in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="272d5-110">Si vous souhaitez inscrire des appareils iOS et Android dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="272d5-110">If you want to enroll iOS and Android devices in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="272d5-111">Le test des licences automatisées et l’appartenance aux groupes ne nécessitent pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="272d5-111">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="272d5-112">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="272d5-112">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-enroll-your-ios-and-android-devices"></a><span data-ttu-id="272d5-113">Phase 2 : inscrire vos appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="272d5-113">Phase 2: Enroll your iOS and Android devices</span></span>

<span data-ttu-id="272d5-114">Tout d’abord, suivez les instructions de la procédure d' [installation et connectez-vous à l’application portail d’entreprise](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) pour personnaliser l’application portail d’entreprise Microsoft Intune pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="272d5-114">First, use the instructions in [Install and sign in to the Company Portal app](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) to customize the Microsoft Intune Company Portal app for your test environment.</span></span>

<span data-ttu-id="272d5-115">Ensuite, suivez les instructions de la procédure [configurer l’accès aux ressources de votre entreprise](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) pour inscrire un appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="272d5-115">Next, use the instructions in [Set up access to your company resources](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) to enroll an iOS device.</span></span>

<span data-ttu-id="272d5-116">Ensuite, suivez les instructions de la procédure [inscrire votre appareil Android dans Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) pour inscrire un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="272d5-116">Next, use the instructions in [Enroll your Android device in Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) to enroll an Android device.</span></span>

## <a name="phase-3-manage-your-ios-and-android-devices-remotely"></a><span data-ttu-id="272d5-117">Phase 3 : gérer les appareils iOS et Android à distance</span><span class="sxs-lookup"><span data-stu-id="272d5-117">Phase 3: Manage your iOS and Android devices remotely</span></span>

<span data-ttu-id="272d5-118">Microsoft Intune fournit des fonctionnalités de verrouillage à distance et de réinitialisation du code secret.</span><span class="sxs-lookup"><span data-stu-id="272d5-118">Microsoft Intune provides both remote lock and passcode reset capabilities.</span></span> <span data-ttu-id="272d5-119">Si une personne perd son appareil, vous pouvez le verrouiller à distance.</span><span class="sxs-lookup"><span data-stu-id="272d5-119">If someone loses their device, you can lock the device remotely.</span></span> <span data-ttu-id="272d5-120">Si une personne oublie son mot de passe, vous pouvez le réinitialiser à distance.</span><span class="sxs-lookup"><span data-stu-id="272d5-120">If someone forgets their passcode, you can reset it remotely.</span></span>
  
<span data-ttu-id="272d5-121">Pour verrouiller un appareil iOS ou Android à distance :</span><span class="sxs-lookup"><span data-stu-id="272d5-121">To lock an iOS or Android device remotely:</span></span>

1. <span data-ttu-id="272d5-122">Connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide des informations d’identification de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="272d5-122">Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="272d5-123">Cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="272d5-123">Click **All services**, type **Intune**, and then click **Intune**.</span></span>
3. <span data-ttu-id="272d5-124">Cliquez sur **périphériques > tous les appareils**.</span><span class="sxs-lookup"><span data-stu-id="272d5-124">Click **Devices > All devices**.</span></span>
4. <span data-ttu-id="272d5-125">Dans la liste des périphériques, cliquez sur un appareil iOS ou Android, puis sur l’action de **verrouillage à distance** .</span><span class="sxs-lookup"><span data-stu-id="272d5-125">In the list of devices, click an iOS or Android device, and then click the **Remote lock** action.</span></span>

    
<span data-ttu-id="272d5-126">Pour réinitialiser le code secret à distance, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="272d5-126">To reset the passcode remotely:</span></span>

1. <span data-ttu-id="272d5-127">Si nécessaire, connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide des informations d’identification de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="272d5-127">If needed, sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="272d5-128">Cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="272d5-128">Click **All services**, type **Intune**, and then click **Intune**.</span></span>
3. <span data-ttu-id="272d5-129">Cliquez sur **périphériques > tous les appareils**.</span><span class="sxs-lookup"><span data-stu-id="272d5-129">Click **Devices > All devices**.</span></span>
4. <span data-ttu-id="272d5-130">Dans la liste des appareils gérés, cliquez sur un appareil iOS ou Android, puis choisissez **... Plus encore**.</span><span class="sxs-lookup"><span data-stu-id="272d5-130">From the list of devices you manage, click an iOS or Android device, and choose **...More**.</span></span> <span data-ttu-id="272d5-131">Ensuite, sélectionnez l’action de **suppression** de l’appareil à distance.</span><span class="sxs-lookup"><span data-stu-id="272d5-131">Then choose the **Remove passcode** device remote action.</span></span>

<span data-ttu-id="272d5-132">Pour une expérience supplémentaire, consultez la rubrique [available Device actions](https://docs.microsoft.com/intune/device-management#available-device-actions).</span><span class="sxs-lookup"><span data-stu-id="272d5-132">For additional experimentation, see [Available device actions](https://docs.microsoft.com/intune/device-management#available-device-actions).</span></span>

    
## <a name="next-step"></a><span data-ttu-id="272d5-133">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="272d5-133">Next step</span></span>

<span data-ttu-id="272d5-134">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="272d5-134">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="272d5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="272d5-135">See Also</span></span>

[<span data-ttu-id="272d5-136">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="272d5-136">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)
  
[<span data-ttu-id="272d5-137">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="272d5-137">Device compliance policies for your Microsoft 365 Enterprise test environment</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
  
[<span data-ttu-id="272d5-138">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="272d5-138">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

