---
title: Stratégies de conformité des appareils pour votre environnement Microsoft 365 de test d’entreprise
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
description: Utilisez ce guide de laboratoire de test pour ajouter des stratégies de conformité d’appareil Intune à votre Microsoft 365 environnement de test d’entreprise.
ms.openlocfilehash: d42c9a603ca581941cb5a8f30b9ecd9d6f780759
ms.sourcegitcommit: 001e64f89f9c3cd6bbd4a25459f5bee3b966820c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367094"
---
# <a name="device-compliance-policies-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="677ce-103">Stratégies de conformité des appareils pour votre environnement Microsoft 365 de test d’entreprise</span><span class="sxs-lookup"><span data-stu-id="677ce-103">Device compliance policies for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="677ce-104">*Ce Guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="677ce-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="677ce-105">Cet article explique comment ajouter une stratégie de conformité des appareils Intune pour les appareils Windows 10 et les Applications Microsoft 365 pour les grandes entreprises à votre environnement de test Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="677ce-105">This article describes how to add an Intune device compliance policy for Windows 10 devices and Microsoft 365 Apps for enterprise to your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="677ce-106">L’ajout d’une stratégie de conformité d’appareil Intune implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="677ce-106">Adding an Intune device compliance policy involves two phases:</span></span>
- [<span data-ttu-id="677ce-107">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="677ce-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="677ce-108">Phase 2 : Création d’une stratégie de conformité des appareils Windows 10 appareils</span><span class="sxs-lookup"><span data-stu-id="677ce-108">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>](#phase-2-create-a-device-compliance-policy-for-windows-10-devices)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="677ce-110">Pour obtenir une carte visuelle de tous les articles de la pile Microsoft 365 guide de laboratoire de test pour entreprise, Microsoft 365 pour la pile de guides de laboratoire de [test d’entreprise.](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="677ce-110">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="677ce-111">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="677ce-111">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="677ce-112">Si vous souhaitez configurer des stratégies DE GESTION uniquement de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="677ce-112">If you want to configure MAM policies in only a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="677ce-113">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="677ce-113">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="677ce-114">Le test de la gestion automatisée des licences et de l’appartenance à un groupe ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="677ce-114">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="677ce-115">Il est fourni ici en tant qu’option afin que vous pouvez tester la gestion automatisée des licences et l’appartenance à un groupe et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="677ce-115">It's provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span>
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="677ce-116">Phase 2 : Création d’une stratégie de conformité des appareils Windows 10 appareils</span><span class="sxs-lookup"><span data-stu-id="677ce-116">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="677ce-117">Dans cette phase, vous allez créer une stratégie de conformité des appareils Windows 10 appareils.</span><span class="sxs-lookup"><span data-stu-id="677ce-117">In this phase, you create a device compliance policy for Windows 10 devices.</span></span> <span data-ttu-id="677ce-118">Cette phase utilise Microsoft Intune et le [centre d Microsoft Endpoint Manager’administration](https://go.microsoft.com/fwlink/?linkid=2109431) pour ajouter un groupe et créer une stratégie de conformité.</span><span class="sxs-lookup"><span data-stu-id="677ce-118">This phase uses Microsoft Intune and the [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) to add a group, and create a compliance policy.</span></span>

1. <span data-ttu-id="677ce-119">Go to the [Microsoft 365 admin center,](https://admin.microsoft.com)and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span><span class="sxs-lookup"><span data-stu-id="677ce-119">Go to the [Microsoft 365 admin center](https://admin.microsoft.com), and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span></span> <span data-ttu-id="677ce-120">Sélectionnez le **Endpoint Manager’administration** centrale.</span><span class="sxs-lookup"><span data-stu-id="677ce-120">Select the **Endpoint Manager** admin center.</span></span> <span data-ttu-id="677ce-121">Le [centre Endpoint Manager’administration](https://go.microsoft.com/fwlink/?linkid=2109431) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="677ce-121">The [Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431) opens.</span></span>

    <span data-ttu-id="677ce-122">Si un message similaire à **Vous n’avez** pas encore activé la gestion des appareils s’affiche, sélectionnez Intune comme autorité de gestion des périphériques.</span><span class="sxs-lookup"><span data-stu-id="677ce-122">If a message similar to **You haven't enabled device management yet** message is shown, then select Intune as the MDM authority.</span></span> <span data-ttu-id="677ce-123">Pour les étapes spécifiques, voir [Définir l’autorité de gestion des appareils mobiles.](/mem/intune/fundamentals/mdm-authority-set)</span><span class="sxs-lookup"><span data-stu-id="677ce-123">For the specific steps, see [Set the mobile device management authority](/mem/intune/fundamentals/mdm-authority-set).</span></span>

    <span data-ttu-id="677ce-124">Le Centre Endpoint Manager’administration de l’entreprise se concentre sur la gestion des appareils et des applications.</span><span class="sxs-lookup"><span data-stu-id="677ce-124">The Endpoint Manager admin center focuses on device management and app management.</span></span> <span data-ttu-id="677ce-125">Pour une visite guidée de ce centre d’administration, voir [Didacticiel : Intune](/mem/intune/fundamentals/tutorial-walkthrough-endpoint-manager)pas à pas dans Microsoft Endpoint Manager .</span><span class="sxs-lookup"><span data-stu-id="677ce-125">For a tour of this admin center, see [Tutorial: Walkthrough Intune in Microsoft Endpoint Manager](/mem/intune/fundamentals/tutorial-walkthrough-endpoint-manager).</span></span>

2. <span data-ttu-id="677ce-126">Dans **groupes,** ajoutez un  nouveau groupe **Microsoft 365** ou de sécurité nommé **Utilisateurs** Windows 10'appareil géré, avec un type **d’appartenance** affecté.</span><span class="sxs-lookup"><span data-stu-id="677ce-126">In **Groups**, add a new **Microsoft 365** or **Security** group named **Managed Windows 10 device users**, with an **Assigned** membership type.</span></span> <span data-ttu-id="677ce-127">Dans les étapes suivantes, vous allez affecter votre stratégie de conformité à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="677ce-127">In the next steps, you'll assign your compliance policy to this group.</span></span> 

    <span data-ttu-id="677ce-128">Pour les étapes spécifiques et pour  plus d’informations **sur Microsoft 365** ou les groupes de sécurité, voir Ajouter des groupes pour organiser les utilisateurs et [les appareils.](/mem/intune/fundamentals/groups-add)</span><span class="sxs-lookup"><span data-stu-id="677ce-128">For the specific steps, and for information on **Microsoft 365** or **Security** groups, see [Add groups to organize users and devices](/mem/intune/fundamentals/groups-add).</span></span>

3. <span data-ttu-id="677ce-129">Dans **Les appareils,** créez une stratégie Windows 10 conformité.</span><span class="sxs-lookup"><span data-stu-id="677ce-129">In **Devices**, create a Windows 10 compliance policy.</span></span> <span data-ttu-id="677ce-130">Affectez cette stratégie au **groupe d’utilisateurs Windows 10 d’appareil géré** que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="677ce-130">Assign this policy to the **Managed Windows 10 device users** group you created.</span></span>

    <span data-ttu-id="677ce-131">Dans votre stratégie, vous pouvez bloquer des mots de passe simples, exiger un pare-feu, exiger l’exécution du service anti-programme malveillant De Microsoft Defender, etc.</span><span class="sxs-lookup"><span data-stu-id="677ce-131">In your policy, you can block simple passwords, require a firewall, require the Microsoft Defender Antimalware service be running, and more.</span></span> <span data-ttu-id="677ce-132">Une stratégie de conformité inclut généralement les paramètres de base, ou un minimum minimal, pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="677ce-132">A compliance policy typically includes the base settings, or bare minimum that every device should have.</span></span>

    <span data-ttu-id="677ce-133">Pour les étapes spécifiques et pour plus d’informations sur les paramètres de conformité disponibles que vous pouvez configurer, voir Utiliser des stratégies de conformité pour définir des règles pour les appareils [que vous gérez.](/mem/intune/protect/device-compliance-get-started)</span><span class="sxs-lookup"><span data-stu-id="677ce-133">For the specific steps, and for information on the available compliance settings you can configure, see [Use compliance policies to set rules for devices you manage](/mem/intune/protect/device-compliance-get-started).</span></span>

<span data-ttu-id="677ce-134">Lorsque vous avez terminé, vous avez une stratégie de conformité des appareils pour tester les membres du groupe d’utilisateurs Windows 10 **géré.**</span><span class="sxs-lookup"><span data-stu-id="677ce-134">When finished, you have a device compliance policy for testing members in the **Managed Windows 10 device users** group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="677ce-135">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="677ce-135">Next step</span></span>

<span data-ttu-id="677ce-136">Explorez [d’autres fonctionnalités de gestion](m365-enterprise-test-lab-guides.md#mobile-device-management) des appareils mobiles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="677ce-136">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="677ce-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="677ce-137">See also</span></span>

<span data-ttu-id="677ce-138">[Microsoft 365 guides de laboratoire de test pour entreprise.](m365-enterprise-test-lab-guides.md)</span><span class="sxs-lookup"><span data-stu-id="677ce-138">[Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="677ce-139">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="677ce-139">Enroll iOS and Android devices in your Microsoft 365 for enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="677ce-140">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="677ce-140">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="677ce-141">Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="677ce-141">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
