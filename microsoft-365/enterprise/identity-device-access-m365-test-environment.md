---
title: Accès aux identités et appareils pour votre environnement de test Microsoft 365
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
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
ms.openlocfilehash: 45749140698553a75df50ed1111cdbfc8eb15684
ms.sourcegitcommit: e525bcf073a61e1350484719a0c3ceb6ff0d8db1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2020
ms.locfileid: "43153737"
---
# <a name="identity-and-device-access-for-your-microsoft-365-test-environment"></a><span data-ttu-id="43250-103">Accès aux identités et appareils pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="43250-103">Identity and device access for your Microsoft 365 test environment</span></span>

<span data-ttu-id="43250-104">*Ce Guide de Laboratoire Test peut uniquement être utilisé pour les environnements de test Microsoft 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="43250-104">*This Test Lab Guide can only be used for Microsoft 365 Enterprise test environments.*</span></span>

<span data-ttu-id="43250-105">Les [configurations d’accès aux identités et appareils](microsoft-365-policies-configurations.md) sont un ensemble de fonctionnalités et de stratégies d’accès conditionnel permettant de protéger l’accès à tous les services intégrés à Azure Active Directory (Azure AD), parmi lesquels Office 365 et Microsoft Intune dans Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="43250-105">[Identity and device access configurations](microsoft-365-policies-configurations.md) are a set of features and Conditional Access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD), including Office 365 and Microsoft Intune in Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="43250-106">Pour créer un environnement de test disposant des stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="43250-106">To create a test environment that has these policies in place:</span></span>

1. <span data-ttu-id="43250-107">Configurez votre environnement de test avec les fonctionnalités d’identité et de sécurité requises en fonction du modèle d’identité et de la méthode d’authentification que vous avez choisis :</span><span class="sxs-lookup"><span data-stu-id="43250-107">Configure your test environment with the prerequisite identity and security features based on your choice of identity model and authentication method:</span></span>

  - [<span data-ttu-id="43250-108">Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="43250-108">Cloud only</span></span>](cloud-only-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="43250-109">Synchronisation de hachage de mot de passe (PHS)</span><span class="sxs-lookup"><span data-stu-id="43250-109">Password hash sync (PHS)</span></span>](phs-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="43250-110">Authentification directe (PTA)</span><span class="sxs-lookup"><span data-stu-id="43250-110">Pass-through authentication (PTA)</span></span>](pta-prereqs-m365-test-environment.md)

2. <span data-ttu-id="43250-111">Utilisez des [stratégies courantes d’accès aux identités et appareils](identity-access-policies.md) pour configurer des stratégies qui respectent des conditions préalables et testent la protection des identités et appareils.</span><span class="sxs-lookup"><span data-stu-id="43250-111">Use [Common identity and device access policies](identity-access-policies.md) to configure the policies that build on the prerequisites and test protection for identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="43250-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43250-112">See also</span></span>

[<span data-ttu-id="43250-113">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="43250-113">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="43250-114">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="43250-114">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="43250-115">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="43250-115">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="43250-116">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="43250-116">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="43250-117">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="43250-117">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
