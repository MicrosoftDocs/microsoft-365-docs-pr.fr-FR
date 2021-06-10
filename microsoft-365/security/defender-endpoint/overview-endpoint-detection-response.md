---
title: Vue d’ensemble protection évolutive des points de terminaison fonctionnalités de gestion
ms.reviewer: ''
description: En savoir plus sur protection évolutive des points de terminaison fonctionnalités de microsoft Defender pour le point de terminaison
keywords: Microsoft Defender pour le point de terminaison, protection évolutive des points de terminaison, réponse, détection, cybersécurité, protection
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
ms.openlocfilehash: b00bef611a3e4b33bf15a5366b09a96f68d4c1a2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933516"
---
# <a name="overview-of-endpoint-detection-and-response"></a><span data-ttu-id="f9383-104">Vue d’ensemble protection évolutive des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="f9383-104">Overview of endpoint detection and response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f9383-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f9383-105">**Applies to:**</span></span>
- [<span data-ttu-id="f9383-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f9383-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="f9383-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f9383-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f9383-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f9383-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f9383-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f9383-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="f9383-110">Les fonctionnalités de protection évolutive des points de terminaison de Defender for Endpoint fournissent des détections d’attaques avancées quasiment en temps réel et actionnables.</span><span class="sxs-lookup"><span data-stu-id="f9383-110">Defender for Endpoint endpoint detection and response capabilities provide advanced attack detections that are near real-time and actionable.</span></span> <span data-ttu-id="f9383-111">Les analystes de la sécurité peuvent hiérarchiser efficacement les alertes, avoir une meilleure visibilité de l’ampleur d’une faille et prendre des mesures correctives pour remédier aux menaces.</span><span class="sxs-lookup"><span data-stu-id="f9383-111">Security analysts can prioritize alerts effectively, gain visibility into the full scope of a breach, and take response actions to remediate threats.</span></span>

<span data-ttu-id="f9383-112">Lorsqu’une menace est détectée, les alertes sont créées dans le système à des fins d’analyse par un analyste.</span><span class="sxs-lookup"><span data-stu-id="f9383-112">When a threat is detected, alerts are created in the system for an analyst to investigate.</span></span> <span data-ttu-id="f9383-113">Les alertes présentant les mêmes techniques d’attaque ou attribuées au même agresseur sont regroupées dans une entité appelée _incident_.</span><span class="sxs-lookup"><span data-stu-id="f9383-113">Alerts with the same attack techniques or attributed to the same attacker are aggregated into an entity called an _incident_.</span></span> <span data-ttu-id="f9383-114">Ce regroupement d’alertes permet plus facilement aux analystes d’étudier les menaces collectivement et d’y répondre.</span><span class="sxs-lookup"><span data-stu-id="f9383-114">Aggregating alerts in this manner makes it easy for analysts to collectively investigate and respond to threats.</span></span>

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4o1j5]

<span data-ttu-id="f9383-115">Inspired by the « assume breach » mindset, Defender for Endpoint continuously collects behavioral cyber telemetry.</span><span class="sxs-lookup"><span data-stu-id="f9383-115">Inspired by the "assume breach" mindset, Defender for Endpoint continuously collects behavioral cyber telemetry.</span></span> <span data-ttu-id="f9383-116">Cela englobe les informations des processus, les activités réseau, l’inspection approfondie du noyau et du gestionnaire de mémoire, les activités de connexion utilisateur, les modifications du Registre et du système de fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="f9383-116">This includes process information, network activities, deep optics into the kernel and memory manager, user login activities, registry and file system changes, and others.</span></span> <span data-ttu-id="f9383-117">Les informations sont conservées pendant six mois, ce qui permet à un analyste de remonter au début d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="f9383-117">The information is stored for six months, enabling an analyst to travel back in time to the start of an attack.</span></span> <span data-ttu-id="f9383-118">Il peut alors analyser différents axes et adopter une approche d’investigation via plusieurs vecteurs.</span><span class="sxs-lookup"><span data-stu-id="f9383-118">The analyst can then pivot in various views and approach an investigation through multiple vectors.</span></span>

<span data-ttu-id="f9383-119">Les fonctionnalités de réponse vous offrent la possibilité de remédier rapidement aux menaces en agissant sur les entités affectées.</span><span class="sxs-lookup"><span data-stu-id="f9383-119">The response capabilities give you the power to promptly remediate threats by acting on the affected entities.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f9383-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9383-120">Related topics</span></span>
- [<span data-ttu-id="f9383-121">Tableau de bord des opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="f9383-121">Security operations dashboard</span></span>](security-operations-dashboard.md)
- [<span data-ttu-id="f9383-122">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="f9383-122">Incidents queue</span></span>](view-incidents-queue.md)
- [<span data-ttu-id="f9383-123">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="f9383-123">Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="f9383-124">Liste des appareils</span><span class="sxs-lookup"><span data-stu-id="f9383-124">Devices list</span></span>](machines-view-overview.md)

