---
title: Environnement de test Azure Protection d’identité AD pour votre entreprise 365 de Microsoft
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
description: Configurer la Protection d’identité Azure AD et analyser les comptes en cours dans votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 165667ad2122839336ef0790ab5661cff53ca32b
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866923"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="0dd7a-103">Environnement de test Azure Protection d’identité AD pour votre entreprise 365 de Microsoft</span><span class="sxs-lookup"><span data-stu-id="0dd7a-103">Azure AD Identity Protection for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="0dd7a-p101">Azure Protection d’identité AD vous permet de détecter les vulnérabilités potentielles affectant les identités de votre organisation, configurer des réponses automatiques et examiner les incidents. Cet article décrit comment activer la Protection d’identité Azure AD et afficher l’analyse de vos comptes d’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-p101">Azure AD Identity Protection allows you to detect potential vulnerabilities affecting your organization’s identities, configure automated responses, and investigate incidents. This article describes how to enable Azure AD Identity Protection and view the analysis of your test environment accounts.</span></span>

<span data-ttu-id="0dd7a-106">Il existe deux phases de configuration de la Protection d’Azure AD identité dans votre environnement de test Microsoft 365 pour entreprises :</span><span class="sxs-lookup"><span data-stu-id="0dd7a-106">There are two phases to setting up Azure AD Identity Protection in your Microsoft 365 Enterprise test environment:</span></span>

1. <span data-ttu-id="0dd7a-107">Créer l’environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-107">Create the Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="0dd7a-108">Activer et utiliser la Protection d’identité Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-108">Enable and use Azure AD Identity Protection.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="0dd7a-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="0dd7a-111">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="0dd7a-111">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="0dd7a-112">Si vous souhaitez uniquement tester Protection Azure AD Identity dans une solution légère avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="0dd7a-112">If you just want to test Azure AD Identity Protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="0dd7a-113">Si vous souhaitez tester Protection Azure AD Identity dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="0dd7a-113">If you want to test Azure AD Identity Protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0dd7a-p102">Test de la Protection d’Azure AD identité ne nécessite pas l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option de sorte que vous pouvez tester la Protection d’identité Azure AD et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-p102">Testing Azure AD Identity Protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test Azure AD Identity Protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-enable-and-use-azure-ad-identity-protection"></a><span data-ttu-id="0dd7a-116">Phase 2 : Activer et utiliser la Protection d’identité Azure AD</span><span class="sxs-lookup"><span data-stu-id="0dd7a-116">Phase 2: Enable and use Azure AD Identity Protection</span></span>

1. <span data-ttu-id="0dd7a-117">Ouvrez une instance privée de votre navigateur et connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) avec le compte d’administrateur global de votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-117">Open a private instance of your browser and sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the global administrator account of your Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="0dd7a-118">Dans le portail Azure, cliquez sur **tous les services > Marketplace**.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-118">In the Azure portal, click **All services > Marketplace**.</span></span>
3. <span data-ttu-id="0dd7a-119">Tapez **Azure AD identité Protection** , puis cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-119">Type **Azure AD Identity Protection** and then click it.</span></span>
4. <span data-ttu-id="0dd7a-120">Sur le serveur lame **Mise en route** , cliquez sur **Onboard** sous **paramètres**, cliquez sur **Ajouter au tableau de bord**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-120">On the **Getting Started** blade, click **Onboard** under **Settings**, click **Pin to dashboard**, and then click **Create**.</span></span>
5. <span data-ttu-id="0dd7a-121">Dans le portail Azure, cliquez sur **la Protection d’Azure AD identité** sur le tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-121">In the Azure portal, click **Azure AD Identity Protection** on the dashboard.</span></span> 

   <span data-ttu-id="0dd7a-p103">Vous devez voir une lame **Azure AD identité Protection-vue d’ensemble** avec un tableau de bord. Sous **les failles**, notez qu’il déterminé le nombre de comptes d’utilisateurs sans l’inscription de l’authentification multifacteur. Ce nombre varie en fonction précédente Microsoft 365 entreprise Test Guides de laboratoire que vous avez effectuées.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-p103">You should see an **Azure AD Identity Protection-Overview** blade with a dashboard. Under **Vulnerabilities**, notice that it determined the number of user accounts without multi-factor authentication registration. This number will vary based on previous Microsoft 365 Enterprise Test Lab Guides that you have done.</span></span>

6. <span data-ttu-id="0dd7a-125">Cliquez sur les catégories pour **examiner** voir s’il existe des utilisateurs ou des événements qui ont été détectés.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-125">Click through the categories for **Investigate** to see if there are any users or events that have been detected.</span></span>

<span data-ttu-id="0dd7a-126">Pour davantage de test et l’expérimentation, voir [événements risque de simulation](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span><span class="sxs-lookup"><span data-stu-id="0dd7a-126">For further testing and experimentation, see [Simulating risk events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span></span>

<span data-ttu-id="0dd7a-127">Voir l’étape de [protection contre les informations d’identification de compromettre](identity-azure-ad-identity-protection.md) lors de la phase d’identité pour des informations et des liens pour déployer la Protection d’Azure AD identité en production.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-127">See the [Protect against credential compromise](identity-azure-ad-identity-protection.md) step in the Identity phase for information and links to deploy Azure AD Identity Protection in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="0dd7a-128">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0dd7a-128">Next step</span></span>

<span data-ttu-id="0dd7a-129">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="0dd7a-129">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="0dd7a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dd7a-130">See also</span></span>

[<span data-ttu-id="0dd7a-131">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="0dd7a-131">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="0dd7a-132">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0dd7a-132">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="0dd7a-133">Déploiement de Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="0dd7a-133">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="0dd7a-134">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0dd7a-134">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
