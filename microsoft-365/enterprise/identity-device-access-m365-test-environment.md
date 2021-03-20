---
title: Accès aux identités et appareils pour votre environnement de test Microsoft 365
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Créer un environnement Microsoft 365 pour tester l’accès aux identités et appareils.
ms.openlocfilehash: 427b0589da0347008cca0e2004bc23f494bebb29
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907467"
---
# <a name="identity-and-device-access-for-your-microsoft-365-test-environment"></a><span data-ttu-id="4e4f4-103">Accès aux identités et appareils pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4e4f4-103">Identity and device access for your Microsoft 365 test environment</span></span>

<span data-ttu-id="4e4f4-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="4e4f4-105">[Les configurations](../security/office-365-security/microsoft-365-policies-configurations.md) d’accès aux identités et appareils sont un ensemble de configurations recommandées et de stratégies d’accès conditionnel pour protéger l’accès à tous les services intégrés à Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-105">[Identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md) are a set of recommended configurations and conditional access policies to protect access to all services that are integrated with Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="4e4f4-106">Pour créer un environnement de test qui dispose des configurations communes d’accès aux identités et aux appareils :</span><span class="sxs-lookup"><span data-stu-id="4e4f4-106">To create a test environment that has the common identity and device access configurations in place:</span></span>

1. <span data-ttu-id="4e4f4-107">Configurez votre environnement de test avec les fonctionnalités d’identité et de sécurité requises en fonction du modèle d’identité et de la méthode d’authentification que vous avez choisis :</span><span class="sxs-lookup"><span data-stu-id="4e4f4-107">Configure your test environment with the prerequisite identity and security features based on your choice of identity model and authentication method:</span></span>

  - [<span data-ttu-id="4e4f4-108">Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="4e4f4-108">Cloud only</span></span>](cloud-only-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="4e4f4-109">Synchronisation de hachage de mot de passe (PHS)</span><span class="sxs-lookup"><span data-stu-id="4e4f4-109">Password hash synchronization (PHS)</span></span>](phs-prereqs-m365-test-environment.md)
  - [<span data-ttu-id="4e4f4-110">Authentification directe (PTA)</span><span class="sxs-lookup"><span data-stu-id="4e4f4-110">Pass-through authentication (PTA)</span></span>](pta-prereqs-m365-test-environment.md)

2. <span data-ttu-id="4e4f4-111">Utilisez [des stratégies](../security/office-365-security/identity-access-policies.md) communes d’accès aux identités et appareils pour configurer les stratégies qui s’appuient sur les conditions préalables configurées pour votre environnement de test et explorer et vérifier la protection des identités et des appareils.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-111">Use [Common identity and device access policies](../security/office-365-security/identity-access-policies.md) to configure the policies that build on the prerequisites configured for your test environment and explore and verify protection for identities and devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e4f4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e4f4-112">See also</span></span>

[<span data-ttu-id="4e4f4-113">Guides de laboratoire de Test Autres identités</span><span class="sxs-lookup"><span data-stu-id="4e4f4-113">Additional identity Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md#identity)

[<span data-ttu-id="4e4f4-114">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="4e4f4-114">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="4e4f4-115">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="4e4f4-115">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="4e4f4-116">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4e4f4-116">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="4e4f4-117">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4e4f4-117">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)