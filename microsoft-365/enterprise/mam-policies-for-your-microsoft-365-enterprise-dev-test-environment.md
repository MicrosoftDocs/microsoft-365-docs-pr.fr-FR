---
title: Environnement de test des stratégies de conformité de périphérique pour votre entreprise 365 de Microsoft
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce Guide de laboratoire de Test pour ajouter l’environnement de test des stratégies de conformité d’appareil Intune à votre entreprise de 365 Microsoft.
ms.openlocfilehash: 1d957c5cdc888251224bbca43fe82ab0a15e7a93
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867468"
---
# <a name="device-compliance-policies-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="e7b00-103">Environnement de test des stratégies de conformité de périphérique pour votre entreprise 365 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="e7b00-103">Device compliance policies for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="e7b00-104">Avec les instructions de cet article, vous ajoutez une stratégie de conformité de périphérique Intune dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="e7b00-104">With the instructions in this article, you add an Intune device compliance policy to your Microsoft 365 Enterprise test environment.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="e7b00-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="e7b00-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="e7b00-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="e7b00-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="e7b00-108">Si vous souhaitez simplement configurer des stratégies MAM de manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="e7b00-108">If you just want to configure MAM policies in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="e7b00-109">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e7b00-109">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="e7b00-p101">Test automatisé de gestion des licences et l’appartenance au groupe ne nécessite pas de l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="e7b00-p101">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-create-a-device-compliance-policy-for-windows-10-devices"></a><span data-ttu-id="e7b00-112">Phase 2 : Créer une stratégie de conformité de périphérique pour les périphériques Windows 10</span><span class="sxs-lookup"><span data-stu-id="e7b00-112">Phase 2: Create a device compliance policy for Windows 10 devices</span></span>

<span data-ttu-id="e7b00-113">Dans cette phase, vous créez une stratégie de conformité de périphérique pour les périphériques Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e7b00-113">In this phase, you create a device compliance policy for Windows 10 devices.</span></span>
  
1. <span data-ttu-id="e7b00-114">Accédez au portail Office au ([https://office.com](https://office.com)) et se connecter à votre abonnement d’évaluation d’Office 365 avec votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="e7b00-114">Go to the Office portal at ([https://office.com](https://office.com)) and sign in to your Office 365 trial subscription with your global administrator account.</span></span>
    
2. <span data-ttu-id="e7b00-115">Sur un nouvel onglet de votre navigateur, ouvrez le portail Azure à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e7b00-115">On a new tab of your browser, open the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>

3. <span data-ttu-id="e7b00-116">Sous l’onglet portail Azure dans votre navigateur, dans le volet de navigation, cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-116">On the Azure portal tab in your browser, in the navigation pane, click **All services**, type **Intune**, and then click **Intune**.</span></span>
    
4. <span data-ttu-id="e7b00-p102">Si vous voyez un message **vous n’avez pas activé la gestion de périphérique encore** sur le serveur lame **Intune Microsoft** , cliquez dessus. Sur la **Gestion des périphériques mobiles autorité** blade, cliquez sur **L’autorité Intune Mobile Device Manager**, puis cliquez sur **Choisir**. Actualisez votre onglet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="e7b00-p102">If you see a **You haven't enabled device management yet** message on the **Microsoft Intune** blade, click it. On the **Mobile Device Management authority** blade, click **Intune MDM Authority**, and then click **Choose**. Refresh your browser tab.</span></span>
    
5. <span data-ttu-id="e7b00-120">Dans le volet de navigation gauche, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-120">In the left navigation pane, click **Groups**.</span></span>
    
6. <span data-ttu-id="e7b00-121">Sur le serveur lame **groupes de groupes** , cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-121">On the **Groups-All groups** blade, click **+ New Group**.</span></span>
    
7. <span data-ttu-id="e7b00-122">Dans la **groupe** lame, sélectionnez **Office 365** pour **type de groupe ?**, tapez **les utilisateurs d’appareils gérées Windows 10** dans **nom**, sélectionnez **assigné** dans le **type d’appartenance**et puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-122">On the **Group** blade, select **Office 365** for **Group type?**, type **Managed Windows 10 device users** in **Name**, select **Assigned** in **Membership type**,  and then click **Create**.</span></span> 
    
8. <span data-ttu-id="e7b00-123">Fermez le volet **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-123">Close the **Group** blade.</span></span>
    
11. <span data-ttu-id="e7b00-124">Fermez la lame de **groupes de groupes** .</span><span class="sxs-lookup"><span data-stu-id="e7b00-124">Close the **Groups-All groups** blade.</span></span>
    
12. <span data-ttu-id="e7b00-125">Sur la blade **Intune Microsoft** , dans la liste de **tâches rapides** , cliquez sur **créer une stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-125">On the **Microsoft Intune** blade, in the **Quick tasks** list, click **Create a compliance policy**.</span></span>
    
13. <span data-ttu-id="e7b00-126">Dans le volet **Profils de stratégie de conformité**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-126">On the **Compliance Policy Profiles** blade, click **Create Policy**.</span></span>
    
14. <span data-ttu-id="e7b00-p103">Sur le serveur lame **Créer une stratégie** , dans **nom**, tapez **Windows 10**. Dans la **plateforme**, sélectionnez **Windows 10 et les versions ultérieures**, cliquez sur **OK** dans la **stratégie de conformité Windows 10** lame, puis cliquez sur **créer**. Fermez la lame **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="e7b00-p103">On the **Create Policy** blade, in **Name**, type **Windows 10**. In **Platform**, select **Windows 10 and later**, click **OK** on the **Windows 10 compliance policy** blade, and then click **Create**. Close the **Windows 10** blade.</span></span>
    
15. <span data-ttu-id="e7b00-130">Sur le serveur lame **Profils de stratégie de conformité** , cliquez sur le nom de la stratégie **Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="e7b00-130">On the **Compliance Policy Profiles** blade, click the **Windows 10** policy name.</span></span>
    
16. <span data-ttu-id="e7b00-131">Sur le serveur lame **10 Windows** , cliquez sur **les affectations**, puis cliquez sur **Sélectionner les groupes à inclure**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-131">On the **Windows 10** blade, click **Assignments**, and then click **Select groups to include**.</span></span>
    
17. <span data-ttu-id="e7b00-132">Sur le serveur lame **Sélectionnez groupes à inclure** , cliquez sur le groupe **d’utilisateurs d’appareils gérées Windows 10** , puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-132">On the **Select groups to include** blade, click the **Managed Windows 10 device users** group, and then click **Select**.</span></span>
    
18. <span data-ttu-id="e7b00-133">Cliquez sur **Enregistrer**, puis fermez la lame **Windows 10 - affectations** .</span><span class="sxs-lookup"><span data-stu-id="e7b00-133">Click **Save**, and then close the **Windows 10 - Assignments** blade.</span></span>
    
19. <span data-ttu-id="e7b00-134">Fermez le volet **Profils de stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-134">Close the **Compliance Policy Profiles** blade.</span></span>
    
20. <span data-ttu-id="e7b00-135">Sur le serveur lame **Intune Microsoft** , cliquez sur **applications clientes** dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="e7b00-135">On the **Microsoft Intune** blade, click **Client apps** in the left navigation.</span></span>
    
21. <span data-ttu-id="e7b00-136">Sur le serveur lame **Applications clientes** , cliquez sur **applications**, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-136">On the **Client Apps** blade, click **Apps**, and then click **Add**.</span></span> 

22. <span data-ttu-id="e7b00-137">Dans **l’application Add** lame, sélectionnez **type d’application**, puis sélectionnez **Windows 10** sous **Office 365 Suite**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-137">In the **Add app** blade, select **App type**, and then select **Windows 10** under **Office 365 Suite**.</span></span>

23. <span data-ttu-id="e7b00-138">Cliquez sur **Configurer la Suite application**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-138">Click **Configure App Suite**, and then click **OK**.</span></span>

24. <span data-ttu-id="e7b00-139">Cliquez sur **Informations Suite d’application**, tapez des **applications Office pour Windows 10** dans **Nom de la Suite**, **les applications Office pour Windows 10** dans la **Description de la Suite**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-139">Click **App Suite Information**, type **Office Apps for Windows 10** in **Suite Name**, **Office Apps for Windows 10** in **Suite Description**, and then click **OK**.</span></span>

25. <span data-ttu-id="e7b00-140">Cliquez sur **Paramètres de Suite de l’application**, sélectionnez **annuel séparées** dans le **canal de mise à jour**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-140">Click **App Suite Settings**, select **Semi-Annual** in **Update channel**, and then click **OK**.</span></span>

26. <span data-ttu-id="e7b00-141">Dans **l’application Add** lame, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e7b00-141">On the **Add app** blade, click **Add**.</span></span>

<span data-ttu-id="e7b00-142">Vous disposez maintenant d’une stratégie de conformité de périphérique pour tester les applications sélectionnées dans la stratégie de conformité de périphérique **Windows 10** et pour les membres du groupe **utilisateurs d’appareils gérées Windows 10** .</span><span class="sxs-lookup"><span data-stu-id="e7b00-142">You now have a device compliance policy for testing the selected apps in the **Windows 10** device compliance policy and for members of the **Managed Windows 10 device users** group.</span></span> 
  
## <a name="next-step"></a><span data-ttu-id="e7b00-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e7b00-143">Next step</span></span>

<span data-ttu-id="e7b00-144">Explorez des fonctionnalités de [Gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="e7b00-144">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7b00-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7b00-145">See also</span></span>

<span data-ttu-id="e7b00-146">[Guides de laboratoire de Test Microsoft Enterprise 365](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="e7b00-146">[Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="e7b00-147">Inscription d’appareils iOS et Android dans votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="e7b00-147">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="e7b00-148">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="e7b00-148">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="e7b00-149">Mobilité d’entreprise + sécurité (EMS)</span><span class="sxs-lookup"><span data-stu-id="e7b00-149">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
