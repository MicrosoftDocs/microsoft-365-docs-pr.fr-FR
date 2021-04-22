---
title: Vue d'ensemble des détections personnalisées dans Microsoft 365 Defender
description: Comprendre comment utiliser le repérage avancé pour créer des détections personnalisées et générer des alertes
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, recherche, requête, télémétrie, détections personnalisées, schéma, kusto
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: bf635ed03cb0d99d54fc94b622bf244447b32a80
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935700"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="aa7c3-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="aa7c3-104">Custom detections overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="aa7c3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="aa7c3-105">**Applies to:**</span></span>
- <span data-ttu-id="aa7c3-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="aa7c3-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="aa7c3-107">Grâce aux détections personnalisées, vous pouvez surveiller et répondre de manière proactive à divers événements et états système, y compris les activités suspectées de violation et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="aa7c3-107">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="aa7c3-108">Cela est rendu possible par des règles de détection personnalisables qui déclenchent automatiquement des alertes, ainsi que des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="aa7c3-108">This is made possible by customizable detection rules that automatically trigger alerts as well as response actions.</span></span>

<span data-ttu-id="aa7c3-109">Les détections personnalisées fonctionnent avec le repérage [avancé,](advanced-hunting-overview.md)qui fournit un langage de requête puissant et flexible qui couvre un large éventail d'événements et d'informations système à partir de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="aa7c3-109">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="aa7c3-110">Vous pouvez les configurer pour qu'ils s'exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu'il existe des correspondances.</span><span class="sxs-lookup"><span data-stu-id="aa7c3-110">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="aa7c3-111">Les détections personnalisées fournissent :</span><span class="sxs-lookup"><span data-stu-id="aa7c3-111">Custom detections provide:</span></span>
- <span data-ttu-id="aa7c3-112">Alertes pour les détections basées sur des règles conçues à partir de requêtes de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="aa7c3-112">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="aa7c3-113">Actions de réponse automatique</span><span class="sxs-lookup"><span data-stu-id="aa7c3-113">Automatic response actions</span></span>

## <a name="see-also"></a><span data-ttu-id="aa7c3-114">Articles associés</span><span class="sxs-lookup"><span data-stu-id="aa7c3-114">See also</span></span>
- [<span data-ttu-id="aa7c3-115">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="aa7c3-115">Create and manage custom detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="aa7c3-116">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="aa7c3-116">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="aa7c3-117">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="aa7c3-117">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>](advanced-hunting-migrate-from-mde.md)
