---
title: Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 pour les entreprises
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
ms.assetid: 49c7758a-1c01-4153-9b63-5eae3f6305ce
description: Utilisez ce guide de laboratoire de test pour inscrire des appareils dans votre environnement de test Microsoft 365 et les gérer à distance.
ms.openlocfilehash: 3736934dbb62e84aad6a91fcd1d65b4a47ef8637
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487695"
---
# <a name="enroll-ios-and-android-devices-in-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="b481b-103">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b481b-103">Enroll iOS and Android devices in your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="b481b-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="b481b-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="b481b-105">Cet article explique comment inscrire et tester les fonctionnalités de base de gestion des appareils mobiles pour les appareils iOS et Android dans votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="b481b-105">This article describes how to enroll and test basic mobile device management capabilities for iOS and Android devices in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="b481b-106">L’enregistrement des appareils iOS et Android dans votre environnement de test implique trois phases :</span><span class="sxs-lookup"><span data-stu-id="b481b-106">Enrolling iOS and Android devices in your test environment involves three phases:</span></span>
- [<span data-ttu-id="b481b-107">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b481b-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="b481b-108">Phase 2 : inscrire vos appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="b481b-108">Phase 2: Enroll your iOS and Android devices</span></span>](#phase-2-enroll-your-ios-and-android-devices)
- [<span data-ttu-id="b481b-109">Phase 3 : gérer les appareils iOS et Android à distance</span><span class="sxs-lookup"><span data-stu-id="b481b-109">Phase 3: Manage your iOS and Android devices remotely</span></span>](#phase-3-manage-your-ios-and-android-devices-remotely)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="b481b-111">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="b481b-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="b481b-112">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b481b-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="b481b-113">Si vous souhaitez inscrire des appareils iOS et Android de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="b481b-113">If you want to enroll iOS and Android devices in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="b481b-114">Si vous souhaitez inscrire des appareils iOS et Android dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b481b-114">If you want to enroll iOS and Android devices in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b481b-115">Le test des licences automatisées et l’appartenance aux groupes ne nécessitent pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b481b-115">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="b481b-116">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et l’appartenance aux groupes, et vous pouvez l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="b481b-116">It's provided here as an option so that you can test automated licensing and group membership, and you can experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-enroll-your-ios-and-android-devices"></a><span data-ttu-id="b481b-117">Phase 2 : inscrire vos appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="b481b-117">Phase 2: Enroll your iOS and Android devices</span></span>

<span data-ttu-id="b481b-118">Tout d’abord, suivez les instructions de la procédure d' [installation et connectez-vous à l’application portail d’entreprise](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) pour personnaliser l’application portail d’entreprise Microsoft Intune pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="b481b-118">First, use the instructions in [Install and sign in to the Company Portal app](https://docs.microsoft.com/intune-user-help/install-and-sign-in-to-the-intune-company-portal-app-ios) to customize the Microsoft Intune Company Portal app for your test environment.</span></span>

<span data-ttu-id="b481b-119">Ensuite, suivez les instructions de la procédure [configurer l’accès aux ressources de votre entreprise](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) pour inscrire un appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="b481b-119">Next, use the instructions in [Set up access to your company resources](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-ios) to enroll an iOS device.</span></span>

<span data-ttu-id="b481b-120">Ensuite, suivez les instructions de la procédure [inscrire votre appareil Android dans Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) pour inscrire un appareil Android.</span><span class="sxs-lookup"><span data-stu-id="b481b-120">Next, use the instructions in [Enroll your Android device in Intune](https://docs.microsoft.com/intune-user-help/enroll-your-device-in-intune-android) to enroll an Android device.</span></span>

## <a name="phase-3-manage-your-ios-and-android-devices-remotely"></a><span data-ttu-id="b481b-121">Phase 3 : gérer les appareils iOS et Android à distance</span><span class="sxs-lookup"><span data-stu-id="b481b-121">Phase 3: Manage your iOS and Android devices remotely</span></span>

<span data-ttu-id="b481b-122">Microsoft Intune fournit des fonctionnalités de verrouillage à distance et de réinitialisation du code secret.</span><span class="sxs-lookup"><span data-stu-id="b481b-122">Microsoft Intune provides both remote lock and passcode reset capabilities.</span></span> <span data-ttu-id="b481b-123">Si une personne perd son appareil, vous pouvez verrouiller l’appareil à distance.</span><span class="sxs-lookup"><span data-stu-id="b481b-123">If someone loses their device, you can remotely lock the device.</span></span> <span data-ttu-id="b481b-124">Si une personne oublie son mot de passe, vous pouvez la réinitialiser à distance.</span><span class="sxs-lookup"><span data-stu-id="b481b-124">If someone forgets their passcode, you can remotely reset it.</span></span>
  
<span data-ttu-id="b481b-125">Pour verrouiller un appareil iOS ou Android à distance :</span><span class="sxs-lookup"><span data-stu-id="b481b-125">To remotely lock an iOS or Android device:</span></span>

1. <span data-ttu-id="b481b-126">Connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide des informations d’identification de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b481b-126">Sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="b481b-127">Dans le portail Azure, entrez **Intune** dans la zone de recherche, puis sélectionnez **Intune**.</span><span class="sxs-lookup"><span data-stu-id="b481b-127">In the Azure portal, enter **Intune** in the search box, and then select **Intune**.</span></span>
3. <span data-ttu-id="b481b-128">Cliquez sur **périphériques > tous les appareils**.</span><span class="sxs-lookup"><span data-stu-id="b481b-128">Click **Devices > All devices**.</span></span>
4. <span data-ttu-id="b481b-129">Dans la liste des périphériques, sélectionnez un appareil iOS ou Android, puis sélectionnez l’action de **verrouillage à distance** .</span><span class="sxs-lookup"><span data-stu-id="b481b-129">In the list of devices, select an iOS or Android device, and then select the **Remote lock** action.</span></span>
    
<span data-ttu-id="b481b-130">Pour réinitialiser le code secret à distance :</span><span class="sxs-lookup"><span data-stu-id="b481b-130">To remotely reset the passcode:</span></span>

1. <span data-ttu-id="b481b-131">Si nécessaire, connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide des informations d’identification de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b481b-131">If needed, sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="b481b-132">Dans le portail Azure, entrez **Intune** dans la zone de recherche, puis sélectionnez **Intune**.</span><span class="sxs-lookup"><span data-stu-id="b481b-132">In the Azure portal, enter **Intune** in the search box, and then select **Intune**.</span></span>
3. <span data-ttu-id="b481b-133">Sélectionnez **périphériques**  >  **tous les appareils**.</span><span class="sxs-lookup"><span data-stu-id="b481b-133">Select **Devices** > **All devices**.</span></span>
4. <span data-ttu-id="b481b-134">Dans la liste des appareils que vous gérez, sélectionnez un appareil iOS ou Android, sélectionnez **... Plus encore**, puis sélectionnez l’action de **suppression** de l’appareil à distance.</span><span class="sxs-lookup"><span data-stu-id="b481b-134">From the list of devices you manage, select an iOS or Android device, select **...More**, and then select the **Remove passcode** device remote action.</span></span>

<span data-ttu-id="b481b-135">Pour une expérience supplémentaire, consultez la rubrique [available Device actions](https://docs.microsoft.com/intune/device-management#available-device-actions).</span><span class="sxs-lookup"><span data-stu-id="b481b-135">For additional experimentation, see [Available device actions](https://docs.microsoft.com/intune/device-management#available-device-actions).</span></span>
    
## <a name="next-step"></a><span data-ttu-id="b481b-136">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b481b-136">Next step</span></span>

<span data-ttu-id="b481b-137">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="b481b-137">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="b481b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b481b-138">See Also</span></span>

[<span data-ttu-id="b481b-139">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="b481b-139">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)
  
[<span data-ttu-id="b481b-140">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="b481b-140">Device compliance policies for your Microsoft 365 for enterprise test environment</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
  
[<span data-ttu-id="b481b-141">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="b481b-141">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)
