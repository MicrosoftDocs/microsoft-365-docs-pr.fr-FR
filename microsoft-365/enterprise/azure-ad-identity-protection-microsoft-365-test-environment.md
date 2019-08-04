---
title: Protection des identités Azure AD pour votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Configurez Azure AD identity protection et analysez les comptes actuels dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: d267bb9dff94acfec46fa1275887f9cade2a7285
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34074084"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="473f7-103">Protection des identités Azure AD pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="473f7-103">Azure AD Identity Protection for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="473f7-104">Azure AD Identity Protection vous permet de détecter les vulnérabilités potentielles affectant les identités de votre organisation, de configurer des réponses automatiques et de rechercher des incidents.</span><span class="sxs-lookup"><span data-stu-id="473f7-104">Azure AD Identity Protection allows you to detect potential vulnerabilities affecting your organization’s identities, configure automated responses, and investigate incidents.</span></span> <span data-ttu-id="473f7-105">Cet article explique comment activer la protection des identités Azure AD et afficher l’analyse de vos comptes d’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="473f7-105">This article describes how to enable Azure AD Identity Protection and view the analysis of your test environment accounts.</span></span>

<span data-ttu-id="473f7-106">Il existe deux phases de configuration de la protection des identités Azure AD dans votre environnement de test Microsoft 365 Enterprise:</span><span class="sxs-lookup"><span data-stu-id="473f7-106">There are two phases to setting up Azure AD Identity Protection in your Microsoft 365 Enterprise test environment:</span></span>

1. <span data-ttu-id="473f7-107">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="473f7-107">Create the Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="473f7-108">Activer et utiliser Azure AD identity protection.</span><span class="sxs-lookup"><span data-stu-id="473f7-108">Enable and use Azure AD Identity Protection.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="473f7-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="473f7-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="473f7-111">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="473f7-111">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="473f7-112">Si vous souhaitez simplement tester la protection des identités Azure AD avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="473f7-112">If you just want to test Azure AD Identity Protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="473f7-113">Si vous souhaitez tester la protection des identités Azure AD dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="473f7-113">If you want to test Azure AD Identity Protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="473f7-114">Le test de la protection des identités Azure AD n’exige pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="473f7-114">Testing Azure AD Identity Protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="473f7-115">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des identités Azure AD et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="473f7-115">It is provided here as an option so that you can test Azure AD Identity Protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-enable-and-use-azure-ad-identity-protection"></a><span data-ttu-id="473f7-116">Phase 2: activer et utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="473f7-116">Phase 2: Enable and use Azure AD Identity Protection</span></span>

1. <span data-ttu-id="473f7-117">Ouvrez une instance privée de votre navigateur et connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide du compte d’administrateur général de votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="473f7-117">Open a private instance of your browser and sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the global administrator account of your Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="473f7-118">Dans le portail Azure, cliquez sur **tous les services > Marketplace**.</span><span class="sxs-lookup"><span data-stu-id="473f7-118">In the Azure portal, click **All services > Marketplace**.</span></span>
3. <span data-ttu-id="473f7-119">Tapez **Azure ad Identity Protection** , puis cliquez sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="473f7-119">Type **Azure AD Identity Protection** and then click it.</span></span>
4. <span data-ttu-id="473f7-120">Dans le **volet mise** en route, cliquez sur **intégré** sous **paramètres**, cliquez sur **Épingler au tableau de bord**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="473f7-120">On the **Getting Started** blade, click **Onboard** under **Settings**, click **Pin to dashboard**, and then click **Create**.</span></span>
5. <span data-ttu-id="473f7-121">Dans le portail Azure, cliquez sur **protection des identités Azure ad** dans le tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="473f7-121">In the Azure portal, click **Azure AD Identity Protection** on the dashboard.</span></span> 

   <span data-ttu-id="473f7-122">Vous devriez voir une lame **Azure ad Identity Protection-Overview** avec un tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="473f7-122">You should see an **Azure AD Identity Protection-Overview** blade with a dashboard.</span></span> <span data-ttu-id="473f7-123">Sous **vulnérabilités**, Notez que le nombre de comptes d’utilisateurs est déterminé sans l’enregistrement d’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="473f7-123">Under **Vulnerabilities**, notice that it determined the number of user accounts without multi-factor authentication registration.</span></span> <span data-ttu-id="473f7-124">Ce nombre varie en fonction des guides de laboratoire de test Microsoft 365 Enterprise que vous avez effectués.</span><span class="sxs-lookup"><span data-stu-id="473f7-124">This number will vary based on previous Microsoft 365 Enterprise Test Lab Guides that you have done.</span></span>

6. <span data-ttu-id="473f7-125">Cliquez sur les catégories pour \*\*\*\* vérifier si des utilisateurs ou des événements ont été détectés.</span><span class="sxs-lookup"><span data-stu-id="473f7-125">Click through the categories for **Investigate** to see if there are any users or events that have been detected.</span></span>

<span data-ttu-id="473f7-126">Pour des tests et des expériences supplémentaires, consultez la rubrique [simulationing Risk Events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span><span class="sxs-lookup"><span data-stu-id="473f7-126">For further testing and experimentation, see [Simulating risk events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span></span>

<span data-ttu-id="473f7-127">Consultez l’étape [protéger contre la compromission des informations d’identification](identity-multi-factor-authentication.md#identity-ident-prot) dans la phase d’identité pour obtenir des informations et des liens permettant de déployer la protection des identités Azure AD en production.</span><span class="sxs-lookup"><span data-stu-id="473f7-127">See the [Protect against credential compromise](identity-multi-factor-authentication.md#identity-ident-prot) step in the Identity phase for information and links to deploy Azure AD Identity Protection in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="473f7-128">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="473f7-128">Next step</span></span>

<span data-ttu-id="473f7-129">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="473f7-129">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="473f7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="473f7-130">See also</span></span>

[<span data-ttu-id="473f7-131">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="473f7-131">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="473f7-132">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="473f7-132">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="473f7-133">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="473f7-133">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="473f7-134">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="473f7-134">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
