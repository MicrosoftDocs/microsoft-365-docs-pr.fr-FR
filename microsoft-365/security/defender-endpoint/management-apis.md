---
title: Vue d’ensemble de la gestion et des API
ms.reviewer: ''
description: En savoir plus sur les outils de gestion et les catégories d'API dans Microsoft Defender pour point de terminaison
keywords: onboarding, api, siem, rbac, access, portal, integration, investigation, response, entities, entity, user context, application context, streaming
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
ms.openlocfilehash: 9e54fb5f2105f0a77c4b63e8d880135005c17168
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51862090"
---
# <a name="overview-of-management-and-apis"></a><span data-ttu-id="9cee5-104">Vue d’ensemble de la gestion et des API</span><span class="sxs-lookup"><span data-stu-id="9cee5-104">Overview of management and APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9cee5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9cee5-105">**Applies to:**</span></span>
- [<span data-ttu-id="9cee5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9cee5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9cee5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9cee5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="9cee5-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="9cee5-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9cee5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9cee5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mgt-apis-abovefoldlink)


<span data-ttu-id="9cee5-110">Defender pour le point de terminaison prend en charge un large éventail d'options pour s'assurer que les clients peuvent facilement adopter la plateforme.</span><span class="sxs-lookup"><span data-stu-id="9cee5-110">Defender for Endpoint supports a wide variety of options to ensure that customers can easily adopt the platform.</span></span> 

<span data-ttu-id="9cee5-111">Sachant que les environnements et structures des clients peuvent varier, Defender for Endpoint a été créé avec flexibilité et contrôle granulaire pour s'adapter à différentes exigences des clients.</span><span class="sxs-lookup"><span data-stu-id="9cee5-111">Acknowledging that customer environments and structures can vary, Defender for Endpoint was created with flexibility and granular control to fit varying customer requirements.</span></span> 

## <a name="endpoint-onboarding-and-portal-access"></a><span data-ttu-id="9cee5-112">Intégration de point de terminaison et accès au portail</span><span class="sxs-lookup"><span data-stu-id="9cee5-112">Endpoint onboarding and portal access</span></span> 

<span data-ttu-id="9cee5-113">L'intégration d'appareils est entièrement intégrée à Microsoft Endpoint Manager et Microsoft Intune pour les appareils clients et au Centre de sécurité Azure pour les appareils serveur, offrant ainsi une expérience complète de configuration, de déploiement et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="9cee5-113">Device onboarding is fully integrated into Microsoft Endpoint Manager and Microsoft Intune for client devices and Azure Security Center for server devices, providing complete end-to-end experience of configuration, deployment, and monitoring.</span></span> <span data-ttu-id="9cee5-114">En outre, Microsoft Defender pour point de terminaison prend en charge la stratégie de groupe et d'autres outils tiers utilisés pour la gestion des appareils.</span><span class="sxs-lookup"><span data-stu-id="9cee5-114">In addition, Microsoft Defender for Endpoint supports Group Policy and other third-party tools used for devices management.</span></span>

<span data-ttu-id="9cee5-115">Defender pour le point de terminaison fournit un contrôle fin sur ce que les utilisateurs ayant accès au portail peuvent voir et faire grâce à la flexibilité du contrôle d'accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="9cee5-115">Defender for Endpoint provides fine-grained control over what users with access to the portal can see and do through the flexibility of role-based access control (RBAC).</span></span> <span data-ttu-id="9cee5-116">Le modèle RBAC prend en charge toutes les sortes de structure des équipes de sécurité :</span><span class="sxs-lookup"><span data-stu-id="9cee5-116">The RBAC model supports all flavors of security teams structure:</span></span>
- <span data-ttu-id="9cee5-117">Organisations et équipes de sécurité distribuées globalement</span><span class="sxs-lookup"><span data-stu-id="9cee5-117">Globally distributed organizations and security teams</span></span>
- <span data-ttu-id="9cee5-118">Équipes d'opérations de sécurité de modèle à plusieurs niveaux</span><span class="sxs-lookup"><span data-stu-id="9cee5-118">Tiered model security operations teams</span></span>
- <span data-ttu-id="9cee5-119">Divisions entièrement séparées avec des équipes d'opérations de sécurité globale centralisées</span><span class="sxs-lookup"><span data-stu-id="9cee5-119">Fully segregated divisions with single centralized global security operations teams</span></span> 

## <a name="available-apis"></a><span data-ttu-id="9cee5-120">API disponibles</span><span class="sxs-lookup"><span data-stu-id="9cee5-120">Available APIs</span></span>
<span data-ttu-id="9cee5-121">La solution Microsoft Defender pour point de terminaison est conçue sur une plateforme prête à l'intégration.</span><span class="sxs-lookup"><span data-stu-id="9cee5-121">The Microsoft Defender for Endpoint solution is built on top of an integration-ready platform.</span></span>

<span data-ttu-id="9cee5-122">Defender pour le point de terminaison expose la plupart de ses données et actions par le biais d'un ensemble d'API par programme.</span><span class="sxs-lookup"><span data-stu-id="9cee5-122">Defender for Endpoint exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="9cee5-123">Ces API vous permettront d'automatiser les flux de travail et d'innover en fonction des fonctionnalités de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="9cee5-123">Those APIs will enable you to automate workflows and innovate based on Defender for Endpoint capabilities.</span></span>

![Image de l'API et de l'intégration disponibles dans Microsoft Defender pour le point de terminaison](images/mdatp-apis.png)  

<span data-ttu-id="9cee5-125">Les API Defender pour point de terminaison peuvent être regroupées en trois :</span><span class="sxs-lookup"><span data-stu-id="9cee5-125">The Defender for Endpoint APIs can be grouped into three:</span></span>
- <span data-ttu-id="9cee5-126">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9cee5-126">Microsoft Defender for Endpoint APIs</span></span> 
- <span data-ttu-id="9cee5-127">API de diffusion en continu de données brutes</span><span class="sxs-lookup"><span data-stu-id="9cee5-127">Raw data streaming API</span></span>
- <span data-ttu-id="9cee5-128">Intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="9cee5-128">SIEM integration</span></span>

## <a name="microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="9cee5-129">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9cee5-129">Microsoft Defender for Endpoint APIs</span></span>

<span data-ttu-id="9cee5-130">Defender pour le point de terminaison offre un modèle d'API en couches exposant des données et des fonctionnalités dans un modèle structuré, clair et facile à utiliser, exposé via un modèle d'authentification et d'autorisation Azure AD standard permettant l'accès dans le contexte des utilisateurs ou des applications SaaS.</span><span class="sxs-lookup"><span data-stu-id="9cee5-130">Defender for Endpoint offers a layered API model exposing data and capabilities in a structured, clear, and easy to use model, exposed through a standard Azure  AD-based authentication and authorization model allowing access in context of users or SaaS applications.</span></span> <span data-ttu-id="9cee5-131">Le modèle API a été conçu pour exposer des entités et des fonctionnalités sous une forme cohérente.</span><span class="sxs-lookup"><span data-stu-id="9cee5-131">The API model was designed to expose entities and capabilities in a consistent form.</span></span> 

<span data-ttu-id="9cee5-132">Regardez cette vidéo pour obtenir une vue d'ensemble rapide des API de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="9cee5-132">Watch this video for a quick overview of Defender for Endpoint's APIs.</span></span> 
>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4d73M]

<span data-ttu-id="9cee5-133">**L'API** Investigation expose la richesse de Defender pour point de terminaison : elle expose des entités calculées ou « profilées » (par exemple, des appareils, des utilisateurs et des fichiers) et des événements discrets (par exemple, création de processus et création de fichiers) qui décrivent généralement un comportement lié à une entité, ce qui permet d'accéder aux données via des interfaces d'investigation permettant un accès basé sur une requête aux données.</span><span class="sxs-lookup"><span data-stu-id="9cee5-133">The **Investigation API** exposes the richness of Defender for Endpoint - exposing calculated or 'profiled' entities (for example, device, user, and file) and discrete events (for example, process creation and file creation) which typically describes a behavior related to an entity, enabling access to data via investigation interfaces allowing a query-based access to data.</span></span> <span data-ttu-id="9cee5-134">Pour plus d'informations, voir [API pris en charge.](exposed-apis-list.md)</span><span class="sxs-lookup"><span data-stu-id="9cee5-134">For more information, see [Supported APIs](exposed-apis-list.md).</span></span>

<span data-ttu-id="9cee5-135">**L'API Response** expose la possibilité d'agir dans le service et sur les appareils, ce qui permet aux clients d'ing d'indicateurs, de gérer les paramètres, l'état des alertes, ainsi que d'agir sur les appareils par programme, comme isoler les appareils du réseau, mettre en quarantaine des fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="9cee5-135">The **Response API** exposes the ability to take actions in the service and on devices, enabling customers to ingest indicators, manage settings, alert status, as well as take response actions on devices programmatically such as isolate devices from the network, quarantine files, and others.</span></span> 

## <a name="raw-data-streaming-api"></a><span data-ttu-id="9cee5-136">API de diffusion en continu de données brutes</span><span class="sxs-lookup"><span data-stu-id="9cee5-136">Raw data streaming API</span></span> 
<span data-ttu-id="9cee5-137">Defender for Endpoint raw data streaming API provides the ability for customers to ship real-time events and alerts from their instances as they occur within a single data stream, providing a low latency, high débit delivery mechanism.</span><span class="sxs-lookup"><span data-stu-id="9cee5-137">Defender for Endpoint raw data streaming API provides the ability for customers to ship real-time events and alerts from their instances as they occur within a single data stream, providing a low latency, high throughput delivery mechanism.</span></span>

<span data-ttu-id="9cee5-138">Les informations d'événement Defender for Endpoint sont directement poussées vers le stockage Azure pour la rétention des données à long terme, ou vers les Hubs d'événements Azure pour une consommation par des services de visualisation ou des moteurs de traitement de données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9cee5-138">The Defender for Endpoint event information is pushed directly to Azure storage for long-term data retention, or to Azure Event Hubs for consumption by visualization services or additional data processing engines.</span></span> 

<span data-ttu-id="9cee5-139">Pour plus d'informations, voir [l'API de diffusion en continu des données brutes.](raw-data-export.md)</span><span class="sxs-lookup"><span data-stu-id="9cee5-139">For more information, see [Raw data streaming API](raw-data-export.md).</span></span>


## <a name="siem-api"></a><span data-ttu-id="9cee5-140">SIEM API</span><span class="sxs-lookup"><span data-stu-id="9cee5-140">SIEM API</span></span>
<span data-ttu-id="9cee5-141">Lorsque vous activez l'intégration SIEM (Security Information and Event Management), cela vous permet d'obtenir des détections à partir du Centre de sécurité Microsoft Defender à l'aide de votre solution SIEM ou en vous connectant directement à l'API REST de détections.</span><span class="sxs-lookup"><span data-stu-id="9cee5-141">When you enable security information and event management (SIEM) integration, it allows you to pull detections from Microsoft Defender Security Center using your SIEM solution or by connecting directly to the detections REST API.</span></span> <span data-ttu-id="9cee5-142">Cela active la section des détails d'accès au connecteur SIEM avec des valeurs pré-remplies et une application est créée sous votre client Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="9cee5-142">This activates the SIEM connector access details section with pre-populated values and an application is created under your Azure Active Directory (Azure AD) tenant.</span></span> <span data-ttu-id="9cee5-143">Pour plus d'informations, voir [intégration SIEM.](enable-siem-integration.md)</span><span class="sxs-lookup"><span data-stu-id="9cee5-143">For more information, see [SIEM integration](enable-siem-integration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cee5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cee5-144">Related topics</span></span>
- [<span data-ttu-id="9cee5-145">Accéder aux API Microsoft Defender for Endpoint </span><span class="sxs-lookup"><span data-stu-id="9cee5-145">Access the Microsoft Defender for Endpoint APIs </span></span>](apis-intro.md)
- [<span data-ttu-id="9cee5-146">API prise en charge</span><span class="sxs-lookup"><span data-stu-id="9cee5-146">Supported APIs</span></span>](exposed-apis-list.md)
- [<span data-ttu-id="9cee5-147">Opportunités de partenariat technique</span><span class="sxs-lookup"><span data-stu-id="9cee5-147">Technical partner opportunities</span></span>](partner-integration.md)

