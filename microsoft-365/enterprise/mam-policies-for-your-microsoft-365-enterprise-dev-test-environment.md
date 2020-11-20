---
title: Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour les entreprises
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
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce guide de laboratoire de test pour ajouter des stratégies de conformité d’appareil Intune à votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: d42c9a603ca581941cb5a8f30b9ecd9d6f780759
ms.sourcegitcommit: 001e64f89f9c3cd6bbd4a25459f5bee3b966820c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367094"
---
# <a name="device-compliance-policies-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="99858-103">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="99858-103">Device compliance policies for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="99858-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="99858-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="99858-105">Cet article explique comment ajouter une stratégie Intune de conformité des appareils pour les appareils Windows 10 et les applications Microsoft 365 pour les entreprises à votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="99858-105">This article describes how to add an Intune device compliance policy for Windows 10 devices and Microsoft 365 Apps for enterprise to your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="99858-106">L’ajout d’une stratégie Intune de conformité des appareils implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="99858-106">Adding an Intune device compliance policy involves two phases:</span></span>
- [<span data-ttu-id="99858-107">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="99858-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="99858-108">Phase 2 : créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="99858-108">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>](#phase-2-create-a-device-compliance-policy-for-windows-10-devices)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="99858-110">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="99858-110">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="99858-111">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="99858-111">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="99858-112">Si vous souhaitez configurer des stratégies MAM de manière simple avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="99858-112">If you want to configure MAM policies in only a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="99858-113">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="99858-113">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="99858-114">Le test des licences automatisées et l’appartenance aux groupes ne nécessitent pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="99858-114">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="99858-115">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="99858-115">It's provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span>
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="99858-116">Phase 2 : créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="99858-116">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="99858-117">Au cours de cette phase, vous allez créer une stratégie de conformité des appareils pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="99858-117">In this phase, you create a device compliance policy for Windows 10 devices.</span></span> <span data-ttu-id="99858-118">Cette phase utilise Microsoft Intune et le [Centre d’administration du gestionnaire de points de terminaison Microsoft](https://go.microsoft.com/fwlink/?linkid=2109431) pour ajouter un groupe et créer une stratégie de conformité.</span><span class="sxs-lookup"><span data-stu-id="99858-118">This phase uses Microsoft Intune and the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) to add a group, and create a compliance policy.</span></span>

1. <span data-ttu-id="99858-119">Accédez au [Centre d’administration microsoft 365](https://admin.microsoft.com), puis connectez-vous à votre abonnement de laboratoire de test Microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="99858-119">Go to the [Microsoft 365 admin center](https://admin.microsoft.com), and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span></span> <span data-ttu-id="99858-120">Sélectionnez le centre d’administration du **Gestionnaire de point de terminaison** .</span><span class="sxs-lookup"><span data-stu-id="99858-120">Select the **Endpoint Manager** admin center.</span></span> <span data-ttu-id="99858-121">Le [Centre d’administration du gestionnaire de point de terminaison](https://go.microsoft.com/fwlink/?linkid=2109431) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="99858-121">The [Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) opens.</span></span>

    <span data-ttu-id="99858-122">Si un message similaire à celui **que vous n’avez pas activé la gestion des appareils** , un message s’affiche, puis sélectionnez Intune comme autorité MDM.</span><span class="sxs-lookup"><span data-stu-id="99858-122">If a message similar to **You haven't enabled device management yet** message is shown, then select Intune as the MDM authority.</span></span> <span data-ttu-id="99858-123">Pour connaître les étapes spécifiques, reportez-vous à [la rubrique Set the Mobile Device Management Authority](/mem/intune/fundamentals/mdm-authority-set).</span><span class="sxs-lookup"><span data-stu-id="99858-123">For the specific steps, see [Set the mobile device management authority](/mem/intune/fundamentals/mdm-authority-set).</span></span>

    <span data-ttu-id="99858-124">Le centre d’administration du gestionnaire de point de terminaison est axé sur la gestion des applications et des applications.</span><span class="sxs-lookup"><span data-stu-id="99858-124">The Endpoint Manager admin center focuses on device management and app management.</span></span> <span data-ttu-id="99858-125">Pour une visite guidée de ce centre d’administration, consultez la rubrique [Tutorial : Walkthrough Intune in Microsoft Endpoint Manager](/mem/intune/fundamentals/tutorial-walkthrough-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="99858-125">For a tour of this admin center, see [Tutorial: Walkthrough Intune in Microsoft Endpoint Manager](/mem/intune/fundamentals/tutorial-walkthrough-endpoint-manager).</span></span>

2. <span data-ttu-id="99858-126">Dans **groupes**, ajoutez un nouveau groupe de sécurité ou un groupe de **sécurité** **Microsoft 365** nommé **utilisateurs d’appareils Windows 10 gérés**, avec un type d’appartenance **affecté** .</span><span class="sxs-lookup"><span data-stu-id="99858-126">In **Groups**, add a new **Microsoft 365** or **Security** group named **Managed Windows 10 device users**, with an **Assigned** membership type.</span></span> <span data-ttu-id="99858-127">Dans les étapes suivantes, vous allez affecter votre stratégie de conformité à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="99858-127">In the next steps, you'll assign your compliance policy to this group.</span></span> 

    <span data-ttu-id="99858-128">Pour connaître les étapes spécifiques, et pour plus d’informations sur **Microsoft 365** ou sur les groupes de **sécurité** , consultez la rubrique [Add Groups to organi Users and Devices](/mem/intune/fundamentals/groups-add).</span><span class="sxs-lookup"><span data-stu-id="99858-128">For the specific steps, and for information on **Microsoft 365** or **Security** groups, see [Add groups to organize users and devices](/mem/intune/fundamentals/groups-add).</span></span>

3. <span data-ttu-id="99858-129">Dans **appareils**, créez une stratégie de conformité Windows 10.</span><span class="sxs-lookup"><span data-stu-id="99858-129">In **Devices**, create a Windows 10 compliance policy.</span></span> <span data-ttu-id="99858-130">Affectez cette stratégie au groupe d' **utilisateurs d’appareils Windows 10 géré** que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="99858-130">Assign this policy to the **Managed Windows 10 device users** group you created.</span></span>

    <span data-ttu-id="99858-131">Dans votre stratégie, vous pouvez bloquer les mots de passe simples, exiger un pare-feu, exiger que le service anti-programme malveillant de Microsoft Defender soit en cours d’exécution, et plus encore.</span><span class="sxs-lookup"><span data-stu-id="99858-131">In your policy, you can block simple passwords, require a firewall, require the Microsoft Defender Antimalware service be running, and more.</span></span> <span data-ttu-id="99858-132">En règle générale, une stratégie de conformité inclut les paramètres de base ou le minimum absolu que chaque appareil doit avoir.</span><span class="sxs-lookup"><span data-stu-id="99858-132">A compliance policy typically includes the base settings, or bare minimum that every device should have.</span></span>

    <span data-ttu-id="99858-133">Pour connaître les étapes spécifiques, et pour plus d’informations sur les paramètres de conformité disponibles que vous pouvez configurer, reportez-vous à la rubrique [utiliser des stratégies de conformité pour définir des règles pour les appareils que vous gérez](/mem/intune/protect/device-compliance-get-started).</span><span class="sxs-lookup"><span data-stu-id="99858-133">For the specific steps, and for information on the available compliance settings you can configure, see [Use compliance policies to set rules for devices you manage](/mem/intune/protect/device-compliance-get-started).</span></span>

<span data-ttu-id="99858-134">Lorsque vous avez terminé, vous disposez d’une stratégie de conformité de l’appareil pour tester les membres dans le groupe **utilisateurs d’appareils Windows 10 gérés** .</span><span class="sxs-lookup"><span data-stu-id="99858-134">When finished, you have a device compliance policy for testing members in the **Managed Windows 10 device users** group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="99858-135">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="99858-135">Next step</span></span>

<span data-ttu-id="99858-136">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="99858-136">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="99858-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99858-137">See also</span></span>

<span data-ttu-id="99858-138">[Microsoft 365 pour les guides de laboratoire de test d’entreprise](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="99858-138">[Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="99858-139">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="99858-139">Enroll iOS and Android devices in your Microsoft 365 for enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="99858-140">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="99858-140">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="99858-141">Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="99858-141">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
