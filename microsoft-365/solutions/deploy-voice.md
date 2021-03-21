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
description: Découvrez comment choisir et déployer la solution vocale Teams appropriée pour votre organisation.
ms.openlocfilehash: ede8075767e9d0a80123ac742403f8a4d171392e
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918381"
---
# <a name="plan-and-deploy-a-teams-voice-solution"></a><span data-ttu-id="d2f14-103">Planifier et déployer une solution vocale Teams</span><span class="sxs-lookup"><span data-stu-id="d2f14-103">Plan and deploy a Teams voice solution</span></span>

<span data-ttu-id="d2f14-104">Une solution vocale Teams permet aux membres de votre organisation d’effectuer des appels à l’intérieur et à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d2f14-104">A Teams voice solution enables people in your organization to make calls both within and outside your organization.</span></span> <span data-ttu-id="d2f14-105">Une solution vocale complète se compose de Teams, du système téléphonique Microsoft et d’un choix d’options pour la connexion au réseau téléphonique commuté (PSTN).</span><span class="sxs-lookup"><span data-stu-id="d2f14-105">A complete voice solution consists of Teams, Microsoft Phone System, and a choice of options for connecting to the Public Switched Telephone Network (PSTN).</span></span>

![Vue d’ensemble des solutions vocales Teams](..\media\solutions-architecture-center\voice-concepts.png)

<span data-ttu-id="d2f14-107">Le système téléphonique fournit des fonctionnalités PBX (Private Branch Exchange) complètes pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d2f14-107">Phone System provides complete Private Branch Exchange (PBX) capabilities for your organization.</span></span> <span data-ttu-id="d2f14-108">Les appels entre les utilisateurs de votre organisation, quel que soit leur emplacement géographique, sont gérés en interne au sein du système téléphonique, supprimant ainsi les coûts longue distance sur ces appels internes.</span><span class="sxs-lookup"><span data-stu-id="d2f14-108">Calls between users in your organization--no matter their geographic location--are handled internally within Phone System thereby removing long-distance costs on these internal calls.</span></span>  

<span data-ttu-id="d2f14-109">En connectant le système téléphonique au réseau téléphonique commuté (PSTN), vos utilisateurs Teams peuvent également passer des appels à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d2f14-109">By connecting Phone System to the Public Switched Telephone Network (PSTN), your Teams users can make calls outside your organization as well.</span></span>

<span data-ttu-id="d2f14-110">Ces conseils de solution vous aident à :</span><span class="sxs-lookup"><span data-stu-id="d2f14-110">This solution guidance helps you to:</span></span>

- <span data-ttu-id="d2f14-111">Choisir la solution vocale adaptée à votre organisation</span><span class="sxs-lookup"><span data-stu-id="d2f14-111">Choose the voice solution that is right for your organization</span></span>
- <span data-ttu-id="d2f14-112">Déployer la solution vocale que vous avez sélectionnée</span><span class="sxs-lookup"><span data-stu-id="d2f14-112">Deploy the voice solution you selected</span></span>

<span data-ttu-id="d2f14-113">Suivez ces étapes pour choisir, planifier et configurer votre solution vocale :</span><span class="sxs-lookup"><span data-stu-id="d2f14-113">Follow these steps to choose, plan, and configure your voice solution:</span></span>

![Choisissez votre solution vocale :](..\media\solutions-architecture-center\voice-solutions-overview-1.png)

1. [<span data-ttu-id="d2f14-115">Choisissez votre solution vocale :</span><span class="sxs-lookup"><span data-stu-id="d2f14-115">Choose your voice solution</span></span>](/MicrosoftTeams/cloud-voice-landing-page?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json)

2. [<span data-ttu-id="d2f14-116">Configurer le système téléphonique</span><span class="sxs-lookup"><span data-stu-id="d2f14-116">Set up Phone System</span></span>](/microsoftteams/setting-up-your-phone-system?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json)

3. <span data-ttu-id="d2f14-117">Configurer la connectivité PSTN en choisissant une ou plusieurs des solutions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2f14-117">Set up PSTN connectivity by choosing one, or a combination, of the following:</span></span>
   - <span data-ttu-id="d2f14-118">[Forfait d’appels](/microsoftteams/set-up-calling-plans?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json) : solution microsoft tout-dans-le-cloud avec Microsoft comme opérateur PSTN</span><span class="sxs-lookup"><span data-stu-id="d2f14-118">[Calling Plan](/microsoftteams/set-up-calling-plans?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json) - Microsoft's all-in-the-cloud solution with Microsoft as your PSTN carrier</span></span>
   - <span data-ttu-id="d2f14-119">[Routage direct](/microsoftteams/direct-routing-configure?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json) : utiliser le routage direct pour connecter votre propre opérateur PSTN à Teams</span><span class="sxs-lookup"><span data-stu-id="d2f14-119">[Direct Routing](/microsoftteams/direct-routing-configure?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json) - Use Direct Routing to connect your own PSTN carrier to Teams</span></span> 

<span data-ttu-id="d2f14-120">En outre, vous souhaitez peut-être en savoir plus sur la migration d’une grande entreprise multinationale vers une solution vocale Teams dans l’étude de [cas Contoso](/MicrosoftTeams/voice-case-study-overview?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="d2f14-120">In addition, you might want read about how a large, multi-national corporation migrated to a Teams voice solution in the [Contoso case study](/MicrosoftTeams/voice-case-study-overview?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&toc=%2fmicrosoft-365%2fsolutions%2ftoc.json).</span></span>

<span data-ttu-id="d2f14-121">Pour plus d’informations sur les licences requises, consultez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2f14-121">For information about required licenses, see the following:</span></span>

- [<span data-ttu-id="d2f14-122">Licences de modules add-on Teams</span><span class="sxs-lookup"><span data-stu-id="d2f14-122">Teams add-on licenses</span></span>](/microsoftteams/teams-add-on-licensing/microsoft-teams-add-on-licensing?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json&tabs=enterprise#what-voice-features-are-available-with-my-plan/toc.json)

- [<span data-ttu-id="d2f14-123">Exigences en matière de licences de routage direct</span><span class="sxs-lookup"><span data-stu-id="d2f14-123">Direct Routing licensing requirements</span></span>](/microsoftteams/direct-routing-plan?bc=%2fmicrosoft-365%2fsolutions%2fbreadcrumb%2ftoc.json#licensing-and-other-requirements/toc.json)