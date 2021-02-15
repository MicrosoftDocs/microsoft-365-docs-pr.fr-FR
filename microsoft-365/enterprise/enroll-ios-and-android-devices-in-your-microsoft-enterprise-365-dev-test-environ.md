---
title: Inscrire des appareils iOS/iPadOS et Android dans votre environnement de test Microsoft 365 pour entreprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/19/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom: Ent_TLGs
ms.assetid: 49c7758a-1c01-4153-9b63-5eae3f6305ce
description: Utilisez ce guide de laboratoire de test pour inscrire des appareils dans votre environnement de test Microsoft 365 et les gérer à distance.
ms.openlocfilehash: 06f83d1ed61bcc530b6aa974d7730f1aadc0ecbd
ms.sourcegitcommit: 001e64f89f9c3cd6bbd4a25459f5bee3b966820c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367082"
---
# <a name="enroll-ios-and-android-devices-in-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="01c84-103">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="01c84-103">Enroll iOS and Android devices in your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="01c84-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="01c84-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="01c84-105">Cet article explique comment inscrire et tester les fonctionnalités de gestion des appareils mobiles de base pour les appareils iOS/iPadOS et Android dans votre environnement de test Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="01c84-105">This article describes how to enroll and test basic mobile device management capabilities for iOS/iPadOS and Android devices in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="01c84-106">L’inscription d’appareils iOS/iPadOS et Android dans votre environnement de test implique trois phases :</span><span class="sxs-lookup"><span data-stu-id="01c84-106">Enrolling iOS/iPadOS and Android devices in your test environment involves three phases:</span></span>
- [<span data-ttu-id="01c84-107">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="01c84-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="01c84-108">Phase 2 : Inscrire vos appareils iOS/iPadOS et Android</span><span class="sxs-lookup"><span data-stu-id="01c84-108">Phase 2: Enroll your iOS/iPadOS and Android devices</span></span>](#phase-2-enroll-your-ios-and-android-devices)
- [<span data-ttu-id="01c84-109">Phase 3 : Gérer vos appareils iOS/iPadOS et Android à distance</span><span class="sxs-lookup"><span data-stu-id="01c84-109">Phase 3: Manage your iOS/iPadOS and Android devices remotely</span></span>](#phase-3-manage-your-ios-and-android-devices-remotely)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)
  
> [!TIP]
> <span data-ttu-id="01c84-111">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="01c84-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="01c84-112">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="01c84-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="01c84-113">Si vous souhaitez inscrire les appareils iOS/iPadOS et Android de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="01c84-113">If you want to enroll iOS/iPadOS and Android devices in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="01c84-114">Si vous souhaitez inscrire des appareils iOS/iPadOS et Android dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="01c84-114">If you want to enroll iOS/iPadOS and Android devices in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="01c84-115">Le test de la gestion automatisée des licences et de l’appartenance à un groupe ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="01c84-115">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="01c84-116">Il est fourni ici en tant qu’option afin que vous pouvez tester les licences automatisées et l’appartenance à un groupe, et vous pouvez l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="01c84-116">It's provided here as an option so that you can test automated licensing and group membership, and you can experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-enroll-your-ios-and-android-devices"></a><span data-ttu-id="01c84-117">Phase 2 : Inscrire vos appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="01c84-117">Phase 2: Enroll your iOS and Android devices</span></span>

<span data-ttu-id="01c84-118">Si vous envisagez d’utiliser une solution de gestion des périphériques mobiles (MDM) pour gérer vos appareils, vous pouvez utiliser Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="01c84-118">If you're considering a mobile device management (MDM) solution to manage your devices, you can use Microsoft Intune.</span></span> <span data-ttu-id="01c84-119">Lorsque vous travaillez avec un fournisseur de gestion des périphériques mobiles, y compris Intune, les appareils sont « inscrits ».</span><span class="sxs-lookup"><span data-stu-id="01c84-119">When working with any MDM provider, including Intune, devices are "enrolled".</span></span> <span data-ttu-id="01c84-120">Une fois inscrits, ils reçoivent les fonctionnalités et paramètres que vous configurez.</span><span class="sxs-lookup"><span data-stu-id="01c84-120">When enrolled, they receive the features and settings you configure.</span></span> 

<span data-ttu-id="01c84-121">Dans Intune, il existe plusieurs façons d’inscrire vos appareils iOS/iPadOS et Android.</span><span class="sxs-lookup"><span data-stu-id="01c84-121">In Intune, there are a few ways to enroll your iOS/iPadOS and Android devices.</span></span> <span data-ttu-id="01c84-122">Vous pouvez choisir l’option d’inscription qui fonctionne le mieux pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="01c84-122">You can choose the enrollment option that works best for your organization.</span></span> <span data-ttu-id="01c84-123">Pour plus d’informations et de conseils, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="01c84-123">For more information and guidance, see the following articles:</span></span>

- [<span data-ttu-id="01c84-124">Guide de déploiement : Inscrire des appareils iOS et iPadOS dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="01c84-124">Deployment guide: Enroll iOS and iPadOS devices in Microsoft Intune</span></span>](/mem/intune/fundamentals/deployment-guide-enrollment-ios-ipados)
- [<span data-ttu-id="01c84-125">Guide de déploiement : Inscrire des appareils Android dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="01c84-125">Deployment guide: Enroll Android devices in Microsoft Intune</span></span>](/mem/intune/fundamentals/deployment-guide-enrollment-android)

<span data-ttu-id="01c84-126">Si vous êtes prêt à utiliser Intune pour la gestion des appareils et que vous souhaitez obtenir des conseils, les informations suivantes peuvent vous aider :</span><span class="sxs-lookup"><span data-stu-id="01c84-126">If you're ready to use Intune for device management, and want some guidance, then the following information may help:</span></span>

- [<span data-ttu-id="01c84-127">Vue d’ensemble de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="01c84-127">Device management overview</span></span>](/mem/intune/fundamentals/what-is-device-management)
- [<span data-ttu-id="01c84-128">Didacticiel : Présentation d’Intune dans Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="01c84-128">Tutorial: Walkthrough Intune in Microsoft Endpoint Manager</span></span>](/mem/intune/fundamentals/tutorial-walkthrough-endpoint-manager)
- [<span data-ttu-id="01c84-129">Guide de déploiement : configuration ou déplacement vers Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="01c84-129">Deployment guide: Setup or move to Microsoft Intune</span></span>](/mem/intune/fundamentals/deployment-guide-intune-setup)

## <a name="phase-3-manage-your-ios-and-android-devices-remotely"></a><span data-ttu-id="01c84-130">Phase 3 : Gérer vos appareils iOS et Android à distance</span><span class="sxs-lookup"><span data-stu-id="01c84-130">Phase 3: Manage your iOS and Android devices remotely</span></span>

<span data-ttu-id="01c84-131">Microsoft Intune fournit la fonctionnalité de réinitialisation de code secret et de verrouillage à distance.</span><span class="sxs-lookup"><span data-stu-id="01c84-131">Microsoft Intune provides remote lock and passcode reset feature.</span></span> <span data-ttu-id="01c84-132">Si quelqu’un perd son appareil, vous pouvez verrouiller l’appareil à distance.</span><span class="sxs-lookup"><span data-stu-id="01c84-132">If someone loses their device, you can remotely lock the device.</span></span> <span data-ttu-id="01c84-133">Si quelqu’un oublie son code secret, vous pouvez le réinitialiser à distance.</span><span class="sxs-lookup"><span data-stu-id="01c84-133">If someone forgets their passcode, you can remotely reset it.</span></span>

- <span data-ttu-id="01c84-134">Pour verrouiller à distance un appareil iOS/iPadOS ou Android, voir Verrouiller à distance les appareils [avec Intune.](/mem/intune/remote-actions/device-remote-lock)</span><span class="sxs-lookup"><span data-stu-id="01c84-134">To remotely lock an iOS/iPadOS or Android device, see [Remotely lock devices with Intune](/mem/intune/remote-actions/device-remote-lock).</span></span>
- <span data-ttu-id="01c84-135">Pour réinitialiser à distance le code secret, voir Réinitialiser ou supprimer un code [secret d’appareil dans Intune.](/mem/intune/remote-actions/device-passcode-reset)</span><span class="sxs-lookup"><span data-stu-id="01c84-135">To remotely reset the passcode, see [Reset or remove a device passcode in Intune](/mem/intune/remote-actions/device-passcode-reset).</span></span>

<span data-ttu-id="01c84-136">Pour les autres tâches que vous pouvez exécuter à distance, consultez les [actions de périphérique disponibles.](/mem/intune/remote-actions/device-management#available-device-actions)</span><span class="sxs-lookup"><span data-stu-id="01c84-136">For additional tasks you can run remotely, see [available device actions](/mem/intune/remote-actions/device-management#available-device-actions).</span></span>
    
## <a name="next-step"></a><span data-ttu-id="01c84-137">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="01c84-137">Next step</span></span>

<span data-ttu-id="01c84-138">Explorez [d’autres fonctionnalités de gestion des](m365-enterprise-test-lab-guides.md#mobile-device-management) appareils mobiles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="01c84-138">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="01c84-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01c84-139">See Also</span></span>

[<span data-ttu-id="01c84-140">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="01c84-140">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)
  
[<span data-ttu-id="01c84-141">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="01c84-141">Device compliance policies for your Microsoft 365 for enterprise test environment</span></span>](mam-policies-for-your-microsoft-365-enterprise-dev-test-environment.md)
  
[<span data-ttu-id="01c84-142">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="01c84-142">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)
