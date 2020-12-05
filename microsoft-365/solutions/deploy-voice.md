---
title: Déployer la voix dans Microsoft 365
ms.author: crowe
author: CarolynRowe
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: msteams
localization_priority: Normal
ms.collection:
- M365-collaboration
- m365solution-overview
- m365solution-voice
- M365-voice
ms.custom:
- M365solutions
- seo-marvel-jun2020
f1.keywords: NOCSH
description: Découvrez comment choisir et déployer la solution vocale teams appropriée pour votre organisation.
ms.openlocfilehash: b5dda0ed3d9310c3c43052b9bac4996802e0ed2f
ms.sourcegitcommit: e53234b1f64ebca00e121da1706c02b3337c35f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2020
ms.locfileid: "49580898"
---
# <a name="plan-and-deploy-a-teams-voice-solution"></a><span data-ttu-id="d7aa8-103">Planification et déploiement d’une solution vocale teams</span><span class="sxs-lookup"><span data-stu-id="d7aa8-103">Plan and deploy a Teams voice solution</span></span>

<span data-ttu-id="d7aa8-104">Une solution vocale teams permet aux membres de votre organisation d’effectuer des appels à la fois à l’intérieur et à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-104">A Teams voice solution enables people in your organization to make calls both within and outside your organization.</span></span> <span data-ttu-id="d7aa8-105">Une solution vocale complète se compose de teams, du système Microsoft Phone et d’un choix d’options pour la connexion au réseau téléphonique commuté (RTC).</span><span class="sxs-lookup"><span data-stu-id="d7aa8-105">A complete voice solution consists of Teams, Microsoft Phone System, and a choice of options for connecting to the Public Switched Telephone Network (PSTN).</span></span>

![Vue d’ensemble des solutions vocales teams](..\media\solutions-architecture-center\voice-concepts.png)

<span data-ttu-id="d7aa8-107">Le système téléphonique offre des fonctionnalités PBX (Private Branch Exchange) complètes pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-107">Phone System provides complete Private Branch Exchange (PBX) capabilities for your organization.</span></span> <span data-ttu-id="d7aa8-108">Les appels entre les utilisateurs de votre organisation, quel que soit leur emplacement géographique, sont gérés en interne dans le système téléphonique, ce qui permet de supprimer les coûts à longue distance de ces appels internes.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-108">Calls between users in your organization--no matter their geographic location--are handled internally within Phone System thereby removing long-distance costs on these internal calls.</span></span>  

<span data-ttu-id="d7aa8-109">En connectant le système téléphonique au réseau téléphonique commuté (RTC), les utilisateurs de teams peuvent également effectuer des appels à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d7aa8-109">By connecting Phone System to the Public Switched Telephone Network (PSTN), your Teams users can make calls outside your organization as well.</span></span>

<span data-ttu-id="d7aa8-110">Ce guide de solution vous permet d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7aa8-110">This solution guidance helps you to:</span></span>

- <span data-ttu-id="d7aa8-111">Choisir la solution vocale la plus adaptée à votre organisation</span><span class="sxs-lookup"><span data-stu-id="d7aa8-111">Choose the voice solution that is right for your organization</span></span>
- <span data-ttu-id="d7aa8-112">Déployer la solution vocale que vous avez sélectionnée</span><span class="sxs-lookup"><span data-stu-id="d7aa8-112">Deploy the voice solution you selected</span></span>

<span data-ttu-id="d7aa8-113">Suivez les étapes ci-dessous pour choisir, planifier et configurer votre solution vocale :</span><span class="sxs-lookup"><span data-stu-id="d7aa8-113">Follow these steps to choose, plan, and configure your voice solution:</span></span>

![Choisir votre solution vocale](..\media\solutions-architecture-center\voice-solutions-overview-1.png)

1. [<span data-ttu-id="d7aa8-115">Choisir votre solution vocale</span><span class="sxs-lookup"><span data-stu-id="d7aa8-115">Choose your voice solution</span></span>](https://docs.microsoft.com/MicrosoftTeams/cloud-voice-landing-page?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json)

2. [<span data-ttu-id="d7aa8-116">Configurer le système téléphonique</span><span class="sxs-lookup"><span data-stu-id="d7aa8-116">Set up Phone System</span></span>](https://docs.microsoft.com/microsoftteams/setting-up-your-phone-system?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json)

3. <span data-ttu-id="d7aa8-117">Configurez la connectivité RTC en choisissant une ou plusieurs des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7aa8-117">Set up PSTN connectivity by choosing one, or a combination, of the following:</span></span>
   - <span data-ttu-id="d7aa8-118">[Forfait d’appels](https://docs.microsoft.com/microsoftteams/set-up-calling-plans?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json) -solution Microsoft tout-en-un pour le Cloud avec Microsoft comme opérateur RTC</span><span class="sxs-lookup"><span data-stu-id="d7aa8-118">[Calling Plan](https://docs.microsoft.com/microsoftteams/set-up-calling-plans?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json) - Microsoft's all-in-the-cloud solution with Microsoft as your PSTN carrier</span></span>
   - <span data-ttu-id="d7aa8-119">[Routage direct](https://docs.microsoft.com/microsoftteams/direct-routing-configure?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json) : utilisez le routage direct pour connecter votre propre opérateur RTC à teams</span><span class="sxs-lookup"><span data-stu-id="d7aa8-119">[Direct Routing](https://docs.microsoft.com/microsoftteams/direct-routing-configure?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json) - Use Direct Routing to connect your own PSTN carrier to Teams</span></span> 

<span data-ttu-id="d7aa8-120">En outre, vous souhaiterez peut-être consulter la rubrique relative à la migration d’une grande entreprise multinationale vers une solution vocale teams dans l' [étude de cas contoso](https://docs.microsoft.com/MicrosoftTeams/voice-case-study-overview?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d7aa8-120">In addition, you might want read about how a large, multi-national corporation migrated to a Teams voice solution in the [Contoso case study](https://docs.microsoft.com/MicrosoftTeams/voice-case-study-overview?toc=/microsoft-365/solutions/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json).</span></span>

<span data-ttu-id="d7aa8-121">Pour plus d’informations sur les licences requises, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7aa8-121">For information about required licenses, see the following:</span></span>

- [<span data-ttu-id="d7aa8-122">Licences de module complémentaire teams</span><span class="sxs-lookup"><span data-stu-id="d7aa8-122">Teams add-on licenses</span></span>](https://docs.microsoft.com/microsoftteams/teams-add-on-licensing/microsoft-teams-add-on-licensing?tabs=enterprise#what-voice-features-are-available-with-my-plan/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json)

- [<span data-ttu-id="d7aa8-123">Exigences en matière de licences de routage direct</span><span class="sxs-lookup"><span data-stu-id="d7aa8-123">Direct Routing licensing requirements</span></span>](https://docs.microsoft.com/microsoftteams/direct-routing-plan#licensing-and-other-requirements/toc.json&bc=/microsoft-365/solutions/breadcrumb/toc.json)
