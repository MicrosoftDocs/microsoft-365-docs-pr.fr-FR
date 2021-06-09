---
title: Azure AD Identity Protection pour votre environnement de test Microsoft 365 entreprise
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
description: Configurez Azure AD Identity Protection et analysez les comptes actuels dans votre Microsoft 365 environnement de test d’entreprise.
ms.openlocfilehash: 0cb0acf3faee13676573b04178bd6b4d3d36da4d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905343"
---
# <a name="azure-ad-identity-protection-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="39b1e-103">Azure AD Identity Protection pour votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="39b1e-103">Azure AD Identity Protection for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="39b1e-104">*Ce Guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="39b1e-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="39b1e-105">Vous pouvez utiliser Azure Active Directory Identity Protection (Azure AD) pour détecter les vulnérabilités potentielles qui affectent les identités de votre organisation, configurer des réponses automatisées et examiner les incidents.</span><span class="sxs-lookup"><span data-stu-id="39b1e-105">You can use Azure Active Directory (Azure AD) Identity Protection to detect potential vulnerabilities that affect your organization’s identities, configure automated responses, and investigate incidents.</span></span> <span data-ttu-id="39b1e-106">Cet article explique comment utiliser Azure AD Identity Protection pour afficher l’analyse de vos comptes d’environnement de test.</span><span class="sxs-lookup"><span data-stu-id="39b1e-106">This article describes how to use Azure AD Identity Protection to view the analysis of your test environment accounts.</span></span>

<span data-ttu-id="39b1e-107">La configuration d’Azure AD Identity Protection dans votre Microsoft 365 environnement de test d’entreprise implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="39b1e-107">Setting up Azure AD Identity Protection in your Microsoft 365 for enterprise test environment involves two phases:</span></span>

- [<span data-ttu-id="39b1e-108">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="39b1e-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="39b1e-109">Phase 2 : Utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="39b1e-109">Phase 2: Use Azure AD Identity Protection</span></span>](#phase-2-use-azure-ad-identity-protection)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="39b1e-111">Pour obtenir une carte visuelle de tous les articles de la pile Microsoft 365 guide de laboratoire de test pour entreprise, Microsoft 365 pour la pile de guides de laboratoire de [test d’entreprise.](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="39b1e-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="39b1e-112">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="39b1e-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="39b1e-113">Si vous souhaitez uniquement tester Azure AD Identity Protection de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="39b1e-113">If you want to only test Azure AD Identity Protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="39b1e-114">Si vous souhaitez tester Azure AD Identity Protection dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="39b1e-114">If you want to test Azure AD Identity Protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="39b1e-115">Le test d’Azure AD Identity Protection ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="39b1e-115">Testing Azure AD Identity Protection doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="39b1e-116">Il est fourni ici en tant qu’option afin que vous pouvez tester Azure AD Identity Protection et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="39b1e-116">It is provided here as an option so that you can test Azure AD Identity Protection and experiment with it in an environment that represents a typical organization.</span></span>
  
## <a name="phase-2-use-azure-ad-identity-protection"></a><span data-ttu-id="39b1e-117">Phase 2 : Utiliser Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="39b1e-117">Phase 2: Use Azure AD Identity Protection</span></span>

1. <span data-ttu-id="39b1e-118">Ouvrez une instance privée de votre navigateur et connectez-vous au portail Azure avec le compte d’administrateur général de votre environnement de [https://portal.azure.com](https://portal.azure.com) test Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="39b1e-118">Open a private instance of your browser and sign in to the Azure portal at [https://portal.azure.com](https://portal.azure.com) with the global administrator account of your Microsoft 365 for enterprise test environment.</span></span>
2. <span data-ttu-id="39b1e-119">Dans le portail Azure, tapez **protection des** identités dans la zone de recherche, puis sélectionnez **Azure AD Identity Protection**.</span><span class="sxs-lookup"><span data-stu-id="39b1e-119">In the Azure portal, type **identity protection** in the search box, and then select **Azure AD Identity Protection**.</span></span>
3. <span data-ttu-id="39b1e-120">Dans le tableau **Identity Protection - Vue d’ensemble,** sélectionnez chaque rapport pour voir ce qu’il signale.</span><span class="sxs-lookup"><span data-stu-id="39b1e-120">In the **Identity Protection - Overview** blade, select each report to see what it's reporting.</span></span>
4. <span data-ttu-id="39b1e-121">Sous **Avertir,** sélectionnez **Les utilisateurs à risque détectés alertes**.</span><span class="sxs-lookup"><span data-stu-id="39b1e-121">Under **Notify**, select **Users at risk detected alerts**.</span></span>
5. <span data-ttu-id="39b1e-122">Dans le **volet Utilisateurs à risque détectés,** sélectionnez **Moyenne**.</span><span class="sxs-lookup"><span data-stu-id="39b1e-122">In the **Users at risk detected alerts** pane, select **Medium**.</span></span>
6. <span data-ttu-id="39b1e-123">Pour **les e-mails sont envoyés aux** utilisateurs suivants , sélectionnez **Inclus** et vérifiez que votre compte d’administrateur global figure dans la liste des membres sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="39b1e-123">For **Emails are sent to the following users**, select **Included** and verify that your global admin account is in the list of selected members.</span></span>
7. <span data-ttu-id="39b1e-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="39b1e-124">Select **Save**.</span></span>

<span data-ttu-id="39b1e-125">Sous **Protéger,** sélectionnez différentes polices pour voir comment les configurer.</span><span class="sxs-lookup"><span data-stu-id="39b1e-125">Under **Protect**, select various polices to see how to configure them.</span></span> <span data-ttu-id="39b1e-126">Si vous créez et activez une stratégie, assurez-vous qu’elle ne bloque pas l’accès pour tous les utilisateurs ou que vous ne pourrez peut-être pas vous y connecter.</span><span class="sxs-lookup"><span data-stu-id="39b1e-126">If you create and activate a policy, make sure that it's not blocking access for all users, or you might not be able to sign in.</span></span> <span data-ttu-id="39b1e-127">Pour éviter cela, excluez les comptes d’utilisateurs spécifiques, tels que les administrateurs globaux.</span><span class="sxs-lookup"><span data-stu-id="39b1e-127">To prevent this, exclude specific user accounts, such as global admins.</span></span>

<span data-ttu-id="39b1e-128">Pour d’autres tests et expérimentations, voir [Simulation d’événements de risque.](/azure/active-directory/active-directory-identityprotection-playbook)</span><span class="sxs-lookup"><span data-stu-id="39b1e-128">For further testing and experimentation, see [Simulating risk events](/azure/active-directory/active-directory-identityprotection-playbook).</span></span>

## <a name="next-step"></a><span data-ttu-id="39b1e-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="39b1e-129">Next step</span></span>

<span data-ttu-id="39b1e-130">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="39b1e-130">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="39b1e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b1e-131">See also</span></span>

[<span data-ttu-id="39b1e-132">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="39b1e-132">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="39b1e-133">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="39b1e-133">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="39b1e-134">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="39b1e-134">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="39b1e-135">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="39b1e-135">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)