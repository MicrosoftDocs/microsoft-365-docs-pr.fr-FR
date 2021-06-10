---
title: Vue d’ensemble des détections personnalisées dans Microsoft 365 Defender
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
ms.openlocfilehash: 748b3534ef1f6ca5736667fc3910bb9fa96d23ff
ms.sourcegitcommit: 7cc2be0244fcc30049351e35c25369cacaaf4ca9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51952535"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="c0cdf-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="c0cdf-104">Custom detections overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c0cdf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c0cdf-105">**Applies to:**</span></span>
- <span data-ttu-id="c0cdf-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c0cdf-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="c0cdf-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c0cdf-107">Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="c0cdf-108">Grâce aux détections personnalisées, vous pouvez surveiller et répondre de manière proactive à divers événements et états système, y compris les activités suspectées de violation et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-108">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="c0cdf-109">Cela est rendu possible par des règles de détection personnalisables qui déclenchent automatiquement des alertes, ainsi que des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-109">This is made possible by customizable detection rules that automatically trigger alerts as well as response actions.</span></span>

<span data-ttu-id="c0cdf-110">Les détections personnalisées fonctionnent avec le repérage [avancé,](advanced-hunting-overview.md)qui fournit un langage de requête puissant et flexible qui couvre un large éventail d’événements et d’informations système à partir de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-110">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="c0cdf-111">Vous pouvez les configurer pour qu’ils s’exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu’il existe des correspondances.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-111">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="c0cdf-112">Les détections personnalisées fournissent :</span><span class="sxs-lookup"><span data-stu-id="c0cdf-112">Custom detections provide:</span></span>
- <span data-ttu-id="c0cdf-113">Alertes pour les détections basées sur des règles conçues à partir de requêtes de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c0cdf-113">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="c0cdf-114">Actions de réponse automatique</span><span class="sxs-lookup"><span data-stu-id="c0cdf-114">Automatic response actions</span></span>

## <a name="see-also"></a><span data-ttu-id="c0cdf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0cdf-115">See also</span></span>
- [<span data-ttu-id="c0cdf-116">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="c0cdf-116">Create and manage custom detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="c0cdf-117">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c0cdf-117">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c0cdf-118">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c0cdf-118">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>](advanced-hunting-migrate-from-mde.md)
