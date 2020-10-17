---
title: Protection des identités Azure AD pour votre environnement de test Microsoft 365 pour les entreprises
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
description: Configurez Azure AD identity protection et analysez les comptes actuels dans votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: 162a6504fb7541874798f5e795bd2ecd590b5035
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487707"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="8ea35-103">Protection des identités Azure AD pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="8ea35-103">Azure AD Identity Protection for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="8ea35-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="8ea35-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="8ea35-105">Vous pouvez utiliser la protection des identités Azure Active Directory (Azure AD) pour détecter les vulnérabilités potentielles qui affectent les identités de votre organisation, configurer des réponses automatiques et examiner les incidents.</span><span class="sxs-lookup"><span data-stu-id="8ea35-105">You can use Azure Active Directory (Azure AD) Identity Protection to detect potential vulnerabilities that affect your organization’s identities, configure automated responses, and investigate incidents.</span></span> <span data-ttu-id="8ea35-106">Cet article explique comment utiliser Azure AD Identity Protection pour afficher l’analyse de vos comptes d’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="8ea35-106">This article describes how to use Azure AD Identity Protection to view the analysis of your test environment accounts.</span></span>

<span data-ttu-id="8ea35-107">La configuration d’Azure AD identity protection dans votre environnement de test Microsoft 365 pour entreprise implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="8ea35-107">Setting up Azure AD Identity Protection in your Microsoft 365 for enterprise test environment involves two phases:</span></span>

- [<span data-ttu-id="8ea35-108">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="8ea35-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="8ea35-109">Phase 2 : utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="8ea35-109">Phase 2: Use Azure AD Identity Protection</span></span>](#phase-2-use-azure-ad-identity-protection)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="8ea35-111">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="8ea35-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="8ea35-112">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="8ea35-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="8ea35-113">Si vous souhaitez tester uniquement la protection des identités Azure AD avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="8ea35-113">If you want to only test Azure AD Identity Protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="8ea35-114">Si vous souhaitez tester la protection des identités Azure AD dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8ea35-114">If you want to test Azure AD Identity Protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8ea35-115">Le test de la protection des identités Azure AD n’exige pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8ea35-115">Testing Azure AD Identity Protection doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="8ea35-116">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des identités Azure AD et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="8ea35-116">It is provided here as an option so that you can test Azure AD Identity Protection and experiment with it in an environment that represents a typical organization.</span></span>
  
## <a name="phase-2-use-azure-ad-identity-protection"></a><span data-ttu-id="8ea35-117">Phase 2 : utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="8ea35-117">Phase 2: Use Azure AD Identity Protection</span></span>

1. <span data-ttu-id="8ea35-118">Ouvrez une instance privée de votre navigateur et connectez-vous au portail Azure à l' [https://portal.azure.com](https://portal.azure.com) aide du compte d’administrateur général de votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="8ea35-118">Open a private instance of your browser and sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the global administrator account of your Microsoft 365 for enterprise test environment.</span></span>
2. <span data-ttu-id="8ea35-119">Dans le portail Azure, tapez **protection des identités** dans la zone de recherche, puis sélectionnez **protection des identités Azure ad**.</span><span class="sxs-lookup"><span data-stu-id="8ea35-119">In the Azure portal, type **identity protection** in the search box, and then select **Azure AD Identity Protection**.</span></span>
3. <span data-ttu-id="8ea35-120">Dans le panneau **identity protection-Overview** , sélectionnez chaque rapport pour afficher les rapports qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="8ea35-120">In the **Identity Protection - Overview** blade, select each report to see what it's reporting.</span></span>
4. <span data-ttu-id="8ea35-121">Sous **avertir**, sélectionnez **utilisateurs à risque-alertes détectées**.</span><span class="sxs-lookup"><span data-stu-id="8ea35-121">Under **Notify**, select **Users at risk detected alerts**.</span></span>
5. <span data-ttu-id="8ea35-122">Dans le volet des **alertes détection des utilisateurs à risque** , sélectionnez **moyen**.</span><span class="sxs-lookup"><span data-stu-id="8ea35-122">In the **Users at risk detected alerts** pane, select **Medium**.</span></span>
6. <span data-ttu-id="8ea35-123">Pour les **messages électroniques envoyés aux utilisateurs suivants**, sélectionnez **inclus** et vérifiez que votre compte d’administrateur global figure dans la liste des membres sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="8ea35-123">For **Emails are sent to the following users**, select **Included** and verify that your global admin account is in the list of selected members.</span></span>
7. <span data-ttu-id="8ea35-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8ea35-124">Select **Save**.</span></span>

<span data-ttu-id="8ea35-125">Sous **protéger**, sélectionnez plusieurs stratégies pour voir comment les configurer.</span><span class="sxs-lookup"><span data-stu-id="8ea35-125">Under **Protect**, select various polices to see how to configure them.</span></span> <span data-ttu-id="8ea35-126">Si vous créez et activez une stratégie, assurez-vous qu’elle ne bloque pas l’accès pour tous les utilisateurs ou que vous ne parvenez pas à vous connecter.</span><span class="sxs-lookup"><span data-stu-id="8ea35-126">If you create and activate a policy, make sure that it's not blocking access for all users, or you might not be able to sign in.</span></span> <span data-ttu-id="8ea35-127">Pour éviter cela, excluez des comptes d’utilisateurs spécifiques, tels que des administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="8ea35-127">To prevent this, exclude specific user accounts, such as global admins.</span></span>

<span data-ttu-id="8ea35-128">Pour des tests et des expériences supplémentaires, consultez la rubrique [simulationing Risk Events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span><span class="sxs-lookup"><span data-stu-id="8ea35-128">For further testing and experimentation, see [Simulating risk events](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-playbook).</span></span>

## <a name="next-step"></a><span data-ttu-id="8ea35-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="8ea35-129">Next step</span></span>

<span data-ttu-id="8ea35-130">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="8ea35-130">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ea35-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ea35-131">See also</span></span>

[<span data-ttu-id="8ea35-132">Feuille de route d’identité</span><span class="sxs-lookup"><span data-stu-id="8ea35-132">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="8ea35-133">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="8ea35-133">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="8ea35-134">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="8ea35-134">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="8ea35-135">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="8ea35-135">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
