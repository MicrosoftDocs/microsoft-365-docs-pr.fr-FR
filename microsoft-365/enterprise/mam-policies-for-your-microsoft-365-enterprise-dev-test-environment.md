---
title: Stratégies GAM pour votre environnement de test Microsoft 365 Entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/16/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_TLGs
ms.assetid: 1aa9639b-2862-49c4-bc33-1586dda636b8
description: Utilisez ce Guide de laboratoire de Test pour ajouter l’environnement de test des stratégies de gestion (MAM) Intune application mobile à votre entreprise de 365 Microsoft.
ms.openlocfilehash: f00379a5e70dce5e07c031a7647b27041d3fa9d1
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867468"
---
# <a name="mam-policies-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="cdfd2-103">Stratégies GAM pour votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="cdfd2-103">MAM policies for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="cdfd2-104">Avec les instructions de cet article, vous ajoutez d’environnement de test des stratégies de gestion (MAM) Intune application mobile à votre entreprise de 365 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-104">With the instructions in this article, you add Intune mobile application management (MAM) policies to your Microsoft 365 Enterprise test environment.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="cdfd2-106">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-106">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="cdfd2-107">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="cdfd2-107">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="cdfd2-108">Si vous souhaitez simplement configurer des stratégies MAM de manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="cdfd2-108">If you just want to configure MAM policies in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="cdfd2-109">Si vous souhaitez configurer des stratégies MAM dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cdfd2-109">If you want to configure MAM policies in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="cdfd2-p101">Test automatisé de gestion des licences et l’appartenance au groupe ne nécessite pas de l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-p101">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
>  

## <a name="phase-2-create-and-deploy-mam-policies-for-ios-and-android-devices"></a><span data-ttu-id="cdfd2-112">Phase 2 : Créer et déployer des stratégies de gestion des applications mobiles pour les appareils iOS et Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-112">Phase 2: Create and deploy MAM policies for iOS and Android devices</span></span>

<span data-ttu-id="cdfd2-113">Dans cette phase, vous créez et déployez deux stratégies de gestion des applications mobiles différentes : une pour les appareils iOS et une pour les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-113">In this phase, you create and deploy two different MAM policies: one for iOS devices and one for Android devices.</span></span>
  
1. <span data-ttu-id="cdfd2-114">Accédez au portail Office 365 à ([https://portal.office.com](https://portal.office.com)) et se connecter à votre abonnement d’évaluation d’Office 365 avec votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-114">Go to the Office 365 portal at ([https://portal.office.com](https://portal.office.com)) and sign in to your Office 365 trial subscription with your global administrator account.</span></span>
    
2. <span data-ttu-id="cdfd2-115">Sur un nouvel onglet de votre navigateur, ouvrez le portail Azure à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="cdfd2-115">On a new tab of your browser, open the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>

3. <span data-ttu-id="cdfd2-116">Sous l’onglet portail Azure dans Internet Explorer, dans le volet de navigation, cliquez sur **tous les services**, tapez **Intune**, puis cliquez sur **Intune**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-116">On the Azure portal tab in Internet Explorer, in the navigation pane, click **All services**, type **Intune**, and then click **Intune**.</span></span>
    
4. <span data-ttu-id="cdfd2-p102">Si vous voyez un message **vous n’avez pas activé la gestion de périphérique encore** sur le serveur lame **Intune Microsoft** , cliquez dessus. Sur la **Gestion des périphériques mobiles autorité** blade, cliquez sur **L’autorité Intune Mobile Device Manager**, puis cliquez sur **Choisir**. Actualisez votre onglet du navigateur.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-p102">If you see a **You haven't enabled device management yet** message on the **Microsoft Intune** blade, click it. On the **Mobile Device Management authority** blade, click **Intune MDM Authority**, and then click **Choose**. Refresh your browser tab.</span></span>
    
5. <span data-ttu-id="cdfd2-120">Dans le volet de navigation gauche, cliquez sur **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-120">In the left navigation pane, click **Groups**.</span></span>
    
6. <span data-ttu-id="cdfd2-121">Sur le serveur lame **groupes de groupes** , cliquez sur **+ Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-121">On the **Groups-All groups** blade, click **+ New Group**.</span></span>
    
7. <span data-ttu-id="cdfd2-122">Dans la **groupe** lame, sélectionnez **Office 365** pour **type de groupe ?**, tapez **gérées les utilisateurs d’appareils iOS** dans **nom**, sélectionnez **assigné** dans le **type d’appartenance**et puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-122">On the **Group** blade, select **Office 365** for **Group type?**, type **Managed iOS device users** in **Name**, select **Assigned** in **Membership type**,  and then click **Create**.</span></span> 
    
8. <span data-ttu-id="cdfd2-123">Fermez le volet **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-123">Close the **Group** blade.</span></span>
    
9. <span data-ttu-id="cdfd2-124">Sur le serveur lame **groupes de groupes** , cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-124">On the **Groups-All groups** blade, click **Add**.</span></span>
    
10. <span data-ttu-id="cdfd2-125">Dans la **groupe** lame, sélectionnez **Office 365** pour **type de groupe ?**, tapez **utilisateur d’un appareil Android gérés** dans **nom**, sélectionnez **assigné** dans le **type d’appartenance**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-125">On the **Group** blade, select **Office 365** for **Group type?**, type **Managed Android device user** in **Name**, select **Assigned** in **Membership type**,  and then click **Create**.</span></span>
    
11. <span data-ttu-id="cdfd2-126">Fermez la lame de **groupes de groupes** .</span><span class="sxs-lookup"><span data-stu-id="cdfd2-126">Close the **Groups-All groups** blade.</span></span>
    
12. <span data-ttu-id="cdfd2-127">Dans le volet **Intune**, dans la liste **Tâches rapides**, cliquez sur **Créer une stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-127">On the **Intune** blade, in the **Quick tasks** list, click **Create a compliance policy**.</span></span>
    
13. <span data-ttu-id="cdfd2-128">Dans le volet **Profils de stratégie de conformité**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-128">On the **Compliance Policy Profiles** blade, click **Create Policy**.</span></span>
    
14. <span data-ttu-id="cdfd2-p103">Dans le volet **Créer une stratégie**, dans **Nom**, tapez **iOS**. Dans **Plateforme**, sélectionnez **iOS**, cliquez sur **OK** dans le volet **Stratégie de conformité iOS**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-p103">On the **Create Policy** blade, in **Name**, type **iOS**. In **Platform**, select **iOS**, click **OK** on the **iOS compliance policy** blade, and then click **Create**.</span></span>
    
15. <span data-ttu-id="cdfd2-131">Dans le volet **Profils de stratégie de conformité**, cliquez sur **Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-131">On the **Compliance Policy Profiles** blade, click **Create Policy**.</span></span>
    
16. <span data-ttu-id="cdfd2-p104">Dans le volet **Créer une stratégie**, dans **Nom**, tapez **Android**. Dans **Plateforme**, sélectionnez **Android**, cliquez sur **OK** dans le volet **Stratégie de conformité Android**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-p104">On the **Create Policy** blade, in **Name**, type **Android**. In **Platform**, select **Android**, click **OK** on the **Android compliance policy** blade, and then click **Create**.</span></span>
    
17. <span data-ttu-id="cdfd2-134">Dans le volet **Profils de stratégie de conformité**, cliquez sur le nom de la stratégie **Android**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-134">On the **Compliance Policy Profiles** blade, click the **Android** policy name.</span></span>
    
18. <span data-ttu-id="cdfd2-135">Dans la barre de navigation de gauche du volet **Android - Propriétés**, cliquez sur **Affectations**, puis cliquez sur **Sélectionner des groupes**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-135">In the left navigation of the **Android - Properties** blade, click **Assignments**, and then click **Select groups**.</span></span>
    
19. <span data-ttu-id="cdfd2-136">Dans le volet **Sélectionner des groupes**, sélectionnez le groupe **Utilisateurs d’appareils Android partagés**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-136">On the **Select groups** blade, click the **Managed Android device users** group, and then click **Select**.</span></span>
    
20. <span data-ttu-id="cdfd2-137">Cliquez sur **Enregistrer**, puis fermez la lame **Android - affectations** .</span><span class="sxs-lookup"><span data-stu-id="cdfd2-137">Click **Save**, and then close the **Android - Assignments** blade.</span></span>
    
21. <span data-ttu-id="cdfd2-138">Dans le volet **Profils de stratégie de conformité**, cliquez sur le nom de la stratégie **iOS**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-138">On the **Compliance Policy Profiles** blade, click the **iOS** policy name.</span></span>
    
22. <span data-ttu-id="cdfd2-139">Dans la barre de navigation de gauche du volet **iOS - Propriétés**, cliquez sur **Affectations**, puis cliquez sur **Sélectionner des groupes**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-139">In the left navigation of the **iOS - Properties** blade, click **Assignments**, and then click **Select groups**.</span></span>
    
23. <span data-ttu-id="cdfd2-140">Dans le volet **Sélectionner des groupes**, sélectionnez le groupe **Utilisateurs d’appareils iOS gérés**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-140">On the **Select groups** blade, click the **Managed iOS device users** group, and then click **Select**.</span></span>
    
24. <span data-ttu-id="cdfd2-141">Cliquez sur **Enregistrer**, puis fermez la lame **iOS - affectations** .</span><span class="sxs-lookup"><span data-stu-id="cdfd2-141">Click **Save**, and then close the **iOS - Assignments** blade.</span></span>
    
25. <span data-ttu-id="cdfd2-142">Fermez le volet **Profils de stratégie de conformité**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-142">Close the **Compliance Policy Profiles** blade.</span></span>
    
26. <span data-ttu-id="cdfd2-143">Dans le volet **Intune**, cliquez sur **Gérer les applications** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-143">On the **Intune** blade, click **Manage apps** in the left navigation.</span></span>
    
27. <span data-ttu-id="cdfd2-144">Dans le volet **Applications mobiles**, cliquez sur **Applications**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-144">On the **Mobile Apps** blade, click **Apps**.</span></span>
    
28. <span data-ttu-id="cdfd2-145">Dans la liste des applications, cliquez sur **PowerPoint**. </span><span class="sxs-lookup"><span data-stu-id="cdfd2-145">In the list of apps, click **PowerPoint**,</span></span> 
    
29. <span data-ttu-id="cdfd2-p105">Dans le volet **Présentation PowerPoint**, cliquez sur **Affectations > Sélectionner des groupes > Appareils iOS gérés > Sélectionner**. Dans **Type**, sélectionnez **Disponible**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-p105">On the **PowerPoint Overview** blade, click **Assignments > Select groups > Managed iOS devices > Select**. In **Type**, select **Available**, and then click **Save**.</span></span>
    
30. <span data-ttu-id="cdfd2-148">Répétez l’étape 29 pour les applications suivantes :</span><span class="sxs-lookup"><span data-stu-id="cdfd2-148">Repeat step 29 for the following apps:</span></span>
    
    - <span data-ttu-id="cdfd2-149">Outlook pour Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-149">Outlook for Android</span></span>
    
    - <span data-ttu-id="cdfd2-150">Word pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-150">Word for iOS</span></span>
    
    - <span data-ttu-id="cdfd2-151">Excel pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-151">Excel for iOS</span></span>
    
    - <span data-ttu-id="cdfd2-152">Outlook pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-152">Outlook for iOS</span></span>
    
    - <span data-ttu-id="cdfd2-153">Microsoft Dynamics CRM sur iPad pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-153">Microsoft Dynamics CRM on iPad for iOS</span></span>
    
    - <span data-ttu-id="cdfd2-154">Microsoft Dynamics CRM sur iPhone pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-154">Microsoft Dynamics CRM on iPhone for iOS</span></span>
    
    - <span data-ttu-id="cdfd2-155">Dynamics CRM pour les téléphones Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-155">Dynamics CRM for Phones for Android</span></span>
    
    - <span data-ttu-id="cdfd2-156">Dynamics CRM pour les tablettes Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-156">Dynamics CRM for Tablets for Android</span></span>
    
    - <span data-ttu-id="cdfd2-157">Excel pour Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-157">Excel for Android</span></span>
    
    - <span data-ttu-id="cdfd2-158">Word pour Android</span><span class="sxs-lookup"><span data-stu-id="cdfd2-158">Word for Android</span></span>
    
    - <span data-ttu-id="cdfd2-159">OneNote pour iOS</span><span class="sxs-lookup"><span data-stu-id="cdfd2-159">OneNote for iOS</span></span>
    
31. <span data-ttu-id="cdfd2-160">Fermez le volet **Applications mobiles - Applications**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-160">Close the **Mobile Apps - Apps** blade.</span></span>
    
32. <span data-ttu-id="cdfd2-161">Dans le volet **Applications mobiles**, cliquez sur **Stratégies de protection de l’application**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-161">On the **Mobile Apps** blade, click **App Protection Policies**.</span></span>
    
33. <span data-ttu-id="cdfd2-162">Dans le volet **Stratégies de protection de l’application**, cliquez sur **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-162">On the **App Protection Policies** blade, click **Add a policy**.</span></span>
    
34. <span data-ttu-id="cdfd2-163">Dans le volet **Ajouter une stratégie**, tapez **iOS**, puis cliquez sur **Sélectionner les applications requises**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-163">On the **Add a policy** blade, type **iOS**, and then click **Select required apps**.</span></span>
    
35. <span data-ttu-id="cdfd2-164">Dans le volet **Applications**, cliquez sur **PowerPoint**, **Microsoft Dynamics CRM sur iPhone**, **Excel**, **Microsoft Dynamics CRM sur iPhone**, **Word**, **OneNote** et **Outlook**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-164">On the **Apps** blade, click **PowerPoint**, **Microsoft Dynamics CRM on iPhone**, **Excel**, **Microsoft Dynamics CRM on iPhone**, **Word**, **OneNote**, and **Outlook**, and then click **Select**.</span></span>
    
36. <span data-ttu-id="cdfd2-165">Dans le volet **Ajouter une stratégie**, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-165">On the **Add a policy** blade, click **Create**.</span></span>
    
37. <span data-ttu-id="cdfd2-166">Dans le volet **Stratégies de protection de l’application**, cliquez sur **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-166">On the **App Protection Policies** blade, click **Add a policy**.</span></span>
    
38. <span data-ttu-id="cdfd2-167">Dans le volet **Ajouter une stratégie**, tapez **Android**, sélectionnez **Android** dans **Plateforme**, puis cliquez sur **Sélectionner les applications requises**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-167">On the **Add a policy** blade, type **Android**, select **Android** in **Platform**, and then click **Select required apps**.</span></span>
    
39. <span data-ttu-id="cdfd2-168">Dans le volet **Applications**, cliquez sur **PowerPoint**, **Dynamics CRM pour tablettes**, **Excel**, **Word**, **Outlook**, et **Dynamics CRM pour téléphones**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-168">On the **Apps** blade, click **PowerPoint**, **Dynamics CRM for tablets**, **Excel**, **Word**, **Outlook**, and **Dynamics CRM for phones**, and then click **Select**.</span></span>
    
40. <span data-ttu-id="cdfd2-169">Dans le volet **Ajouter une stratégie**, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-169">On the **Add a policy** blade, click **Create**.</span></span>
    
<span data-ttu-id="cdfd2-170">Vous avez deux stratégies de gestion des applications mobiles : une pour les appareils iOS et l’autre pour les appareils Android. Vous souhaitez tester les paramètres pour les applications sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-170">You now have two MAM policies, one for iOS devices and one for Android devices, and are ready to experiment with testing settings for the selected apps.</span></span> 
  
## <a name="next-step"></a><span data-ttu-id="cdfd2-171">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="cdfd2-171">Next step</span></span>

<span data-ttu-id="cdfd2-172">Explorez des fonctionnalités de [Gestion des appareils mobiles](m365-enterprise-test-lab-guides.md#mobile-device-management) dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="cdfd2-172">Explore additional [mobile device management](m365-enterprise-test-lab-guides.md#mobile-device-management) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdfd2-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdfd2-173">See also</span></span>

<span data-ttu-id="cdfd2-174">[Guides de laboratoire de Test Microsoft Enterprise 365](m365-enterprise-test-lab-guides.md).</span><span class="sxs-lookup"><span data-stu-id="cdfd2-174">[Microsoft 365 Enterprise Test Lab Guides](m365-enterprise-test-lab-guides.md).</span></span>
  
[<span data-ttu-id="cdfd2-175">Inscription d’appareils iOS et Android dans votre environnement de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="cdfd2-175">Enroll iOS and Android devices in your Microsoft 365 Enterprise test environment</span></span>](enroll-ios-and-android-devices-in-your-microsoft-enterprise-365-dev-test-environ.md)
  
[<span data-ttu-id="cdfd2-176">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="cdfd2-176">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="cdfd2-177">Mobilité d’entreprise + sécurité (EMS)</span><span class="sxs-lookup"><span data-stu-id="cdfd2-177">Enterprise Mobility + Security (EMS)</span></span>](https://www.microsoft.com/cloud-platform/enterprise-mobility-security)
