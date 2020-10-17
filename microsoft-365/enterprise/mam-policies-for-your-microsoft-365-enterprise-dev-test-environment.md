---
title: Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour les entreprises
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
description: Utilisez ce guide de laboratoire de test pour ajouter des stratégies de conformité d’appareil Intune à votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: c1de822e5a97416bd0c672d88f2902d8986638c8
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487411"
---
# <a name="device-compliance-policies-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="90913-103">Stratégies de conformité des appareils pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="90913-103">Device compliance policies for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="90913-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="90913-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="90913-105">Cet article explique comment ajouter une stratégie Intune de conformité des appareils pour les appareils Windows 10 et les applications Microsoft 365 pour les entreprises à votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="90913-105">This article describes how to add an Intune device compliance policy for Windows 10 devices and Microsoft 365 Apps for enterprise to your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="90913-106">L’ajout d’une stratégie Intune de conformité des appareils implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="90913-106">Adding an Intune device compliance policy involves two phases:</span></span>
- [<span data-ttu-id="90913-107">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="90913-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="90913-108">Phase 2 : créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="90913-108">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>](#phase-2-create-a-device-compliance-policy-for-windows-10-devices)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="90913-110">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="90913-110">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="90913-111">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="90913-111">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="90913-112">Si vous souhaitez configurer des stratégies MAM de manière simple avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="90913-112">If you want to configure MAM policies in only a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="90913-113">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="90913-113">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="90913-114">Le test des licences automatisées et l’appartenance aux groupes ne nécessitent pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="90913-114">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="90913-115">Elle est fournie ici en tant qu’option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="90913-115">It's provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span>
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="90913-116">Phase 2 : créer une stratégie de conformité des appareils pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="90913-116">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="90913-117">Dans cette phase, créez une stratégie de conformité des appareils pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="90913-117">In this phase, create a device compliance policy for Windows 10 devices.</span></span>
  
1. <span data-ttu-id="90913-118">Accédez au [Centre d’administration microsoft 365](https://admin.microsoft.com) et connectez-vous à votre abonnement de laboratoire de test Microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="90913-118">Go to the [Microsoft 365 admin center](https://admin.microsoft.com) and sign in to your Microsoft 365 test lab subscription with your global administrator account.</span></span>
1. <span data-ttu-id="90913-119">Dans un nouvel onglet de votre navigateur, ouvrez le portail Azure à l’adresse [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="90913-119">On a new tab of your browser, open the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>
1. <span data-ttu-id="90913-120">Dans la zone de recherche du portail Azure, entrez **Intune**, puis sélectionnez **Intune**.</span><span class="sxs-lookup"><span data-stu-id="90913-120">In the search box of the Azure portal, enter **Intune**, and then select **Intune**.</span></span>
1. <span data-ttu-id="90913-121">Si vous voyez un message « **vous n’avez pas activé la gestion des appareils activés** » dans le volet **Microsoft Intune** , sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="90913-121">If you see a **You haven't enabled device management yet** message in the **Microsoft Intune** pane, select it.</span></span> <span data-ttu-id="90913-122">Dans le volet **autorité de gestion des appareils mobiles** , sélectionnez **autorité MDM Intune**, puis sélectionnez **choisir**.</span><span class="sxs-lookup"><span data-stu-id="90913-122">In the **Mobile Device Management authority** pane, select **Intune MDM Authority**, and then select **Choose**.</span></span>
1. <span data-ttu-id="90913-123">Actualisez l’onglet de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="90913-123">Refresh your browser tab.</span></span>
1. <span data-ttu-id="90913-124">Dans le volet de navigation de gauche, sélectionnez **groupes**.</span><span class="sxs-lookup"><span data-stu-id="90913-124">In the left navigation pane, select **Groups**.</span></span>
1. <span data-ttu-id="90913-125">Dans le volet **groupes-tous les groupes** , sélectionnez **+ nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="90913-125">In the **Groups-All groups** pane, select **+ New Group**.</span></span>
1. <span data-ttu-id="90913-126">Dans le volet de **groupe** , sélectionnez **Microsoft 365** ou **sécurité** pour **type de groupe ?**, entrez **utilisateurs d’appareils Windows 10 gérés** dans **nom**, sélectionnez **attribué** dans **type d’appartenance**, puis sélectionnez **créer**.</span><span class="sxs-lookup"><span data-stu-id="90913-126">In the **Group** pane, select **Microsoft 365** or **Security** for **Group type?**, enter **Managed Windows 10 device users** in **Name**, select **Assigned** in **Membership type**,  and then select **Create**.</span></span>
1. <span data-ttu-id="90913-127">Sélectionnez **Microsoft Intune**.</span><span class="sxs-lookup"><span data-stu-id="90913-127">Select **Microsoft Intune**.</span></span>
1. <span data-ttu-id="90913-128">Dans le volet **Microsoft Intune** , dans la liste **tâches rapides** , sélectionnez **créer une stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="90913-128">In the **Microsoft Intune** pane, in the **Quick tasks** list, select **Create a compliance policy**.</span></span>
1. <span data-ttu-id="90913-129">Dans le volet **profils de stratégie de conformité** , sélectionnez créer une **stratégie**.</span><span class="sxs-lookup"><span data-stu-id="90913-129">In the **Compliance Policy Profiles** pane, select **Create Policy**.</span></span>
1. <span data-ttu-id="90913-130">Dans le volet **créer une stratégie** , dans **nom**, entrez **Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="90913-130">In the **Create Policy** pane, in **Name**, enter **Windows 10**.</span></span> <span data-ttu-id="90913-131">Dans **plateforme**, sélectionnez **Windows 10 et versions ultérieures**, sélectionnez **OK** dans le volet **stratégie de conformité Windows 10** , puis sélectionnez **créer**.</span><span class="sxs-lookup"><span data-stu-id="90913-131">In **Platform**, select **Windows 10 and later**, select **OK** in the **Windows 10 compliance policy** pane, and then select **Create**.</span></span>
1. <span data-ttu-id="90913-132">Sélectionnez **profils de stratégie de conformité**, puis sélectionnez le nom de la stratégie **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="90913-132">Select **Compliance Policy Profiles**, and then select the **Windows 10** policy name.</span></span>
1. <span data-ttu-id="90913-133">Dans le volet **Windows 10** , sélectionnez **affectations**, puis sélectionnez les **groupes à inclure**.</span><span class="sxs-lookup"><span data-stu-id="90913-133">In the **Windows 10** pane, select **Assignments**, and then select **Select groups to include**.</span></span>
1. <span data-ttu-id="90913-134">Dans le volet **Sélectionner des groupes à inclure** , sélectionnez le groupe **utilisateurs d’appareils Windows 10 gérés** , puis sélectionnez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="90913-134">In the **Select groups to include** pane, select the **Managed Windows 10 device users** group, and then select **Select**.</span></span>
1. <span data-ttu-id="90913-135">Sélectionnez **Enregistrer**, sélectionnez **Microsoft Intune-vue d’ensemble**, puis sélectionnez **applications client** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="90913-135">Select **Save**, select **Microsoft Intune-Overview**, and then select **Client apps** in the left navigation.</span></span>
1. <span data-ttu-id="90913-136">Dans le volet **applications client** , sélectionnez **applications**, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="90913-136">In the **Client Apps** pane, select **Apps**, and then select **Add**.</span></span>
1. <span data-ttu-id="90913-137">Dans le volet **Ajouter une application** , sélectionnez type d' **application**, puis sélectionnez **Windows 10** sous **Microsoft 365 suite**.</span><span class="sxs-lookup"><span data-stu-id="90913-137">In the **Add app** pane, select **App type**, and then select **Windows 10** under **Microsoft 365 Suite**.</span></span>
1. <span data-ttu-id="90913-138">Dans le volet **Ajouter une application** , sélectionnez **informations sur la suite d’applications**.</span><span class="sxs-lookup"><span data-stu-id="90913-138">In the **Add App** pane, select **App Suite Information**.</span></span>
1. <span data-ttu-id="90913-139">Dans le volet d' **informations App suite** , entrez **Microsoft 365 apps pour entreprises** dans les descriptions nom et **suite**de la **suite** , puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="90913-139">In the **App Suite Information** pane, enter **Microsoft 365 Apps for enterprise** in both **Suite Name** and **Suite Description**, and then select **OK**.</span></span>
1. <span data-ttu-id="90913-140">Dans le volet **Ajouter une application** , sélectionnez configurer une suite d' **applications**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="90913-140">In the **Add App** pane, select **Configure App Suite**, and then select **OK**.</span></span>
1. <span data-ttu-id="90913-141">Dans le volet **Ajouter une application** , sélectionnez Paramètres de la suite d' **applications**.</span><span class="sxs-lookup"><span data-stu-id="90913-141">In the **Add App** pane, select **App Suite Settings**.</span></span>
1. <span data-ttu-id="90913-142">Pour **canal de mise à jour**, sélectionnez **entreprise semi-annuelle**, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="90913-142">For **Update Channel**, select **Semi-Annual Enterprise**, and then select **OK**.</span></span>
1. <span data-ttu-id="90913-143">Dans le volet **Ajouter une application** , sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="90913-143">In the **Add app** pane, select **Add**.</span></span>

<span data-ttu-id="90913-144">Vous disposez maintenant d’une stratégie de conformité de l’appareil pour tester les applications sélectionnées dans la stratégie de conformité des appareils **Windows 10** et pour les membres du groupe **utilisateurs d’appareils Windows 10 gérés** .</span><span class="sxs-lookup"><span data-stu-id="90913-144">You now have a device compliance policy for testing the selected apps in the **Windows 10** device compliance policy and for members of the **Managed Windows 10 device users** group.</span></span> <span data-ttu-id="90913-145">Veuillez noter que la sélection de **Microsoft 365** comme type de groupe crée des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="90913-145">Please note that selecting **Microsoft 365** as the group type creates additional resources.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="90913-146">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="90913-146">Next step</span></span>

<span data-ttu-id="90913-147">Explorez les fonctionnalités supplémentaires de [gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="90913-147">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="90913-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90913-148">See also</span></span>

<span data-ttu-id="90913-149">[Microsoft 365 pour les guides de laboratoire de test d’entreprise](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="90913-149">[Microsoft 365 for enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="90913-150">Inscrire des appareils iOS et Android dans votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="90913-150">Enroll iOS and Android devices in your Microsoft 365 for enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="90913-151">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="90913-151">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="90913-152">Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="90913-152">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
