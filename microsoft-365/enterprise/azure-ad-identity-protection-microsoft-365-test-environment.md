---
title: Protection des identités Azure AD pour votre environnement de test Microsoft 365 Enterprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/10/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Configurez Azure AD identity protection et analysez les comptes actuels dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: 376fc838191314e93ae37accb7fc5066456499fb
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41597161"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="d6853-103">Protection des identités Azure AD pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d6853-103">Azure AD Identity Protection for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="d6853-104">*Ce Guide de Laboratoire Test peut uniquement être utilisé pour les environnements de test Microsoft 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="d6853-104">*This Test Lab Guide can only be used for Microsoft 365 Enterprise test environments.*</span></span>

<span data-ttu-id="d6853-105">Azure Active Directory (Azure AD) Identity Protection vous permet de détecter les vulnérabilités potentielles affectant les identités de votre organisation, de configurer des réponses automatiques et d’examiner les incidents.</span><span class="sxs-lookup"><span data-stu-id="d6853-105">Azure Active Directory (Azure AD) Identity Protection allows you to detect potential vulnerabilities affecting your organization’s identities, configure automated responses, and investigate incidents.</span></span> <span data-ttu-id="d6853-106">Cet article explique comment utiliser Azure AD Identity Protection pour afficher l’analyse de vos comptes d’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="d6853-106">This article describes how to use Azure AD Identity Protection to view the analysis of your test environment accounts.</span></span>

<span data-ttu-id="d6853-107">Il existe deux phases de configuration de la protection des identités Azure AD dans votre environnement de test Microsoft 365 Enterprise :</span><span class="sxs-lookup"><span data-stu-id="d6853-107">There are two phases to setting up Azure AD Identity Protection in your Microsoft 365 Enterprise test environment:</span></span>

1. <span data-ttu-id="d6853-108">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d6853-108">Create the Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="d6853-109">Utiliser Azure AD identity protection.</span><span class="sxs-lookup"><span data-stu-id="d6853-109">Use Azure AD Identity Protection.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="d6853-111">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d6853-111">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="d6853-112">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d6853-112">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="d6853-113">Si vous souhaitez simplement tester la protection des identités Azure AD avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="d6853-113">If you just want to test Azure AD Identity Protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="d6853-114">Si vous souhaitez tester la protection des identités Azure AD dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d6853-114">If you want to test Azure AD Identity Protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d6853-115">Le test de la protection des identités Azure AD n’exige pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="d6853-115">Testing Azure AD Identity Protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="d6853-116">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des identités Azure AD et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="d6853-116">It is provided here as an option so that you can test Azure AD Identity Protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-use-azure-ad-identity-protection"></a><span data-ttu-id="d6853-117">Phase 2 : utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="d6853-117">Phase 2: Use Azure AD Identity Protection</span></span>

1. <span data-ttu-id="d6853-118">Ouvrez une instance privée de votre navigateur et connectez-vous au portail Azure à [https://portal.azure.com](https://portal.azure.com) l’aide du compte d’administrateur général de votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="d6853-118">Open a private instance of your browser and sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the global administrator account of your Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="d6853-119">Dans le portail Azure, tapez **protection des identités** dans la zone de recherche, puis cliquez sur **protection des identités Azure ad**.</span><span class="sxs-lookup"><span data-stu-id="d6853-119">In the Azure portal, type **identity protection** in the search box, and then click **Azure AD Identity Protection**.</span></span>
3. <span data-ttu-id="d6853-120">Dans le panneau **identity protection-Overview** , cliquez sur chacun des rapports pour voir ce qu’ils signalent.</span><span class="sxs-lookup"><span data-stu-id="d6853-120">In the **Identity Protection - Overview** blade, click on each of the reports to see what they are reporting.</span></span>
4. <span data-ttu-id="d6853-121">Sous **avertir**, cliquez sur **utilisateurs à risque-alertes détectées**.</span><span class="sxs-lookup"><span data-stu-id="d6853-121">Under **Notify**, click **Users at risk detected alerts**.</span></span>
5. <span data-ttu-id="d6853-122">Dans le volet des **alertes détection des utilisateurs à risque** , sélectionnez **moyen**.</span><span class="sxs-lookup"><span data-stu-id="d6853-122">In the **Users at risk detected alerts** pane, select **Medium**.</span></span>
6. <span data-ttu-id="d6853-123">Pour les **messages électroniques envoyés aux utilisateurs suivants**, cliquez sur **inclus** et vérifiez que votre compte d’administrateur global figure dans la liste des membres sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d6853-123">For **Emails are sent to the following users**, click **Included** and verify that your global admin account is in the list of selected members.</span></span>
7. <span data-ttu-id="d6853-124">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="d6853-124">Click **Save**.</span></span>

<span data-ttu-id="d6853-125">Cliquez sur les différentes stratégies sous **protéger** pour voir comment les configurer.</span><span class="sxs-lookup"><span data-stu-id="d6853-125">Click through the different policies under **Protect** to see how to configure them.</span></span> <span data-ttu-id="d6853-126">Si vous créez et activez une stratégie, assurez-vous qu’elle ne bloque pas l’accès pour une étendue de conditions trop large, ou que vous ne parvenez pas à vous connecter, même en tant qu’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="d6853-126">If you create and activate a policy, make sure it is not blocking access for too wide a scope of conditions, or you might not be able to sign in, even as the global admin.</span></span>

<span data-ttu-id="d6853-127">Pour des tests et des expériences supplémentaires, consultez la rubrique [simulationing Risk Events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span><span class="sxs-lookup"><span data-stu-id="d6853-127">For further testing and experimentation, see [Simulating risk events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span></span>

<span data-ttu-id="d6853-128">Consultez l’étape [protéger contre la compromission des informations d’identification](identity-secure-user-sign-ins.md#identity-ident-prot) dans la phase d’identité pour obtenir des informations et des liens permettant de déployer la protection des identités Azure AD en production.</span><span class="sxs-lookup"><span data-stu-id="d6853-128">See the [Protect against credential compromise](identity-secure-user-sign-ins.md#identity-ident-prot) step in the Identity phase for information and links to deploy Azure AD Identity Protection in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="d6853-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d6853-129">Next step</span></span>

<span data-ttu-id="d6853-130">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="d6853-130">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6853-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6853-131">See also</span></span>

[<span data-ttu-id="d6853-132">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="d6853-132">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="d6853-133">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d6853-133">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="d6853-134">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d6853-134">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="d6853-135">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d6853-135">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
