---
title: Scénarios et opportunités de partenaires Microsoft Defender ATP
ms.reviewer: ''
description: Découvrez comment étendre les offres de sécurité existantes en plus de l’infrastructure ouverte et d’un ensemble riche d’API pour créer des extensions et des intégrations avec Microsoft Defender ATP
keywords: API, partenaire, étendre, ouvrir une infrastructure, api, extensions, intégrations, détection, gestion, réponse, vulnérabilités, intelligence
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 1db82afa06fd0b6b3d7228aaf3020c5496ed69e7
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186892"
---
# <a name="microsoft-defender-for-endpoint-partner-opportunities-and-scenarios"></a><span data-ttu-id="ec12d-104">Scénarios et opportunités de partenaires Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ec12d-104">Microsoft Defender for Endpoint partner opportunities and scenarios</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ec12d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ec12d-105">**Applies to:**</span></span>
- [<span data-ttu-id="ec12d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ec12d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ec12d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ec12d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="ec12d-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ec12d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ec12d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ec12d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


<span data-ttu-id="ec12d-110">Les partenaires peuvent facilement étendre leurs offres de sécurité existantes en plus de l’infrastructure ouverte et d’un ensemble complet et complet d’API pour créer des extensions et des intégrations avec Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec12d-110">Partners can easily extend their existing security offerings on top of the open framework and a rich and complete set of APIs to build extensions and integrations with Defender for Endpoint.</span></span> 

<span data-ttu-id="ec12d-111">Les API couvrent des domaines fonctionnels, notamment la détection, la gestion, la réponse, les vulnérabilités et la gamme de cas d’utilisation à l’échelle de l’intelligence.</span><span class="sxs-lookup"><span data-stu-id="ec12d-111">The APIs span functional areas including detection, management, response, vulnerabilities, and intelligence-wide range of use cases.</span></span> <span data-ttu-id="ec12d-112">En fonction du cas d’utilisation et des besoins, les partenaires peuvent soit diffuser des données, soit interroger des données à partir de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec12d-112">Based on the use case and need, partners can either stream or query data from Defender for Endpoint.</span></span> 


## <a name="scenario-1-external-alert-correlation-and-automated-investigation-and-remediation"></a><span data-ttu-id="ec12d-113">Scénario 1 : corrélation d’alertes externes et examen et correction automatisés</span><span class="sxs-lookup"><span data-stu-id="ec12d-113">Scenario 1: External alert correlation and Automated investigation and remediation</span></span>
<span data-ttu-id="ec12d-114">Defender pour le point de terminaison offre des fonctionnalités d’investigation et de correction automatisées uniques pour stimuler la réponse aux incidents à grande échelle.</span><span class="sxs-lookup"><span data-stu-id="ec12d-114">Defender for Endpoint offers unique automated investigation and remediation capabilities to drive incident response at scale.</span></span> 

<span data-ttu-id="ec12d-115">L’intégration de la fonctionnalité d’examen et de réponse automatisée à d’autres solutions telles que des produits de sécurité réseau ou d’autres produits de sécurité de point de terminaison permettra de résoudre les alertes.</span><span class="sxs-lookup"><span data-stu-id="ec12d-115">Integrating the automated investigation and response capability with other solutions such as network security products or other endpoint security products will help to address alerts.</span></span> <span data-ttu-id="ec12d-116">L’intégration réduit également les complexités autour de la corrélation de signal réseau et de périphérique, rationalisant efficacement les actions d’examen et de correction des menaces sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="ec12d-116">The integration also minimizes the complexities surrounding network and device signal correlation, effectively streamlining the investigation and threat remediation actions on devices.</span></span>

<span data-ttu-id="ec12d-117">Defender for Endpoint ajoute la prise en charge de ce scénario sous les formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec12d-117">Defender for Endpoint adds support for this scenario in the following forms:</span></span>

- <span data-ttu-id="ec12d-118">Les alertes externes peuvent être poussées dans Defender pour point de terminaison et présentées côte à côte avec des alertes supplémentaires basées sur l’appareil de Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ec12d-118">External alerts can be pushed into Defender for Endpoint and presented side by side with additional device-based alerts from Defender for Endpoint.</span></span> <span data-ttu-id="ec12d-119">Cette vue fournit le contexte complet de l’alerte, avec le processus réel et l’article complet de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="ec12d-119">This view provides the full context of the alert - with the real process and the full story of attack.</span></span>

- <span data-ttu-id="ec12d-120">Une fois qu’une alerte est générée, le signal est partagé entre tous les points de terminaison protégés par Defender for Endpoint dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ec12d-120">Once an alert is generated, the signal is shared across all Defender for Endpoint protected endpoints in the enterprise.</span></span> <span data-ttu-id="ec12d-121">Defender pour le point de terminaison prend immédiatement une réponse automatisée ou assistée par l’opérateur pour résoudre l’alerte.</span><span class="sxs-lookup"><span data-stu-id="ec12d-121">Defender for Endpoint takes immediate automated or operator-assisted response to address the alert.</span></span>

## <a name="scenario-2-security-orchestration-and-automation-response-soar-integration"></a><span data-ttu-id="ec12d-122">Scénario 2 : intégration de l’orchestration de la sécurité et de la réponse automation (CASER)</span><span class="sxs-lookup"><span data-stu-id="ec12d-122">Scenario 2: Security orchestration and automation response (SOAR) integration</span></span>
<span data-ttu-id="ec12d-123">Les solutions d’orchestration peuvent aider à créer des playbooks et à intégrer le modèle de données enrichi et les actions que les API Defender for Endpoint exposent pour orchestrer des réponses, telles que la requête de données de périphérique, déclencher l’isolation de l’appareil, bloquer/autoriser, résoudre une alerte, etc.</span><span class="sxs-lookup"><span data-stu-id="ec12d-123">Orchestration solutions can help build playbooks and integrate the rich data model and actions that Defender for Endpoint APIs expose to orchestrate responses, such as query for device data, trigger device isolation, block/allow, resolve alert and others.</span></span>

## <a name="scenario-3-indicators-matching"></a><span data-ttu-id="ec12d-124">Scénario 3 : correspondance des indicateurs</span><span class="sxs-lookup"><span data-stu-id="ec12d-124">Scenario 3: Indicators matching</span></span> 
<span data-ttu-id="ec12d-125">L’indicateur de compromission (IoCs) est une fonctionnalité essentielle dans chaque solution de protection des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ec12d-125">Indicator of compromise (IoCs) matching is an essential feature in every endpoint protection solution.</span></span> <span data-ttu-id="ec12d-126">Cette fonctionnalité est disponible dans Defender pour point de terminaison et permet de définir une liste d’indicateurs pour la prévention, la détection et l’exclusion d’entités.</span><span class="sxs-lookup"><span data-stu-id="ec12d-126">This capability is available in Defender for Endpoint and gives the ability to set a list of indicators for prevention, detection, and exclusion of entities.</span></span> <span data-ttu-id="ec12d-127">Vous pouvez définir l’action à prendre ainsi que la durée de l’application de l’action.</span><span class="sxs-lookup"><span data-stu-id="ec12d-127">One can define the action to be taken as well as the duration for when to apply the action.</span></span>

<span data-ttu-id="ec12d-128">Les scénarios ci-dessus servent d’exemples d’extensibilité de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ec12d-128">The above scenarios serve as examples of the extensibility of the platform.</span></span> <span data-ttu-id="ec12d-129">Vous n’êtes pas limité aux exemples et nous vous encourageons certainement à tirer parti de l’infrastructure ouverte pour découvrir et explorer d’autres scénarios.</span><span class="sxs-lookup"><span data-stu-id="ec12d-129">You are not limited to the examples and we certainly encourage you to leverage the open framework to discover and explore other scenarios.</span></span>

<span data-ttu-id="ec12d-130">Suivez les étapes [de l’étape](get-started-partner-integration.md) Devenir un partenaire Microsoft Defender pour Point de terminaison pour intégrer votre solution dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec12d-130">Follow the steps in [Become a Microsoft Defender for Endpoint partner](get-started-partner-integration.md) to integrate your solution in Defender for Endpoint.</span></span>

## <a name="related-topic"></a><span data-ttu-id="ec12d-131">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="ec12d-131">Related topic</span></span>
- [<span data-ttu-id="ec12d-132">Vue d’ensemble de la gestion et des API</span><span class="sxs-lookup"><span data-stu-id="ec12d-132">Overview of management and APIs</span></span>](management-apis.md)
