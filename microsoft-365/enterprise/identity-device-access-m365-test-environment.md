---
title: Accès aux identités et appareils pour votre environnement de test Microsoft 365
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 04/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créer un environnement Microsoft 365 pour tester l’accès aux identités et appareils.
ms.openlocfilehash: 9195f532222511fc9dce474617ed52916d8e382a
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34073594"
---
# <a name="identity-and-device-access-for-your-microsoft-365-test-environment"></a><span data-ttu-id="6beea-103">Accès aux identités et appareils pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6beea-103">Identity and device access for your Microsoft 365 test environment</span></span>

<span data-ttu-id="6beea-104">Les [configurations d’accès aux identités et appareils](microsoft-365-policies-configurations.md) sont un ensemble de configurations et stratégies d’accès conditionnel pour protéger l’accès à tous les services qui sont intégrés avec Azure Active Directory (Azure AD), dont Office 365 et Enterprise Mobility + Security (EMS) dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="6beea-104">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of features and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Enterprise Mobility + Security (EMS) in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="6beea-105">Pour créer un environnement de test disposant des stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="6beea-105">To create a test environment that has these policies in place:</span></span>

1. <span data-ttu-id="6beea-106">Configurez votre environnement de test avec les fonctionnalités d’identité et de sécurité requises en fonction du modèle d’identité et de la méthode d’authentification que vous avez choisis :</span><span class="sxs-lookup"><span data-stu-id="6beea-106">Configure your test environment with the prerequisite identity and security features based on your choice of identity model and authentication method:</span></span>

  - [<span data-ttu-id="6beea-107">Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="6beea-107">Cloud only</span></span>](cloud-only-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="6beea-108">Synchronisation de hachage de mot de passe (PHS)</span><span class="sxs-lookup"><span data-stu-id="6beea-108">Password hash sync (PHS)</span></span>](phs-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="6beea-109">Authentification directe (PTA)</span><span class="sxs-lookup"><span data-stu-id="6beea-109">Pass-through authentication (PTA)</span></span>](pta-prereqs-m365-test-environment.md)

2. <span data-ttu-id="6beea-110">Utilisez des [stratégies courantes d’accès aux identités et appareils](identity-access-policies.md) pour configurer des stratégies qui respectent des conditions préalables et testent la protection des identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="6beea-110">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and test protection for identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="6beea-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6beea-111">See also</span></span>

[<span data-ttu-id="6beea-112">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="6beea-112">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="6beea-113">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="6beea-113">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="6beea-114">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="6beea-114">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="6beea-115">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="6beea-115">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="6beea-116">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="6beea-116">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
