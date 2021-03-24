---
title: Vue d’ensemble des détections personnalisées dans Microsoft 365 Defender
description: Comprendre comment utiliser le repérage avancé pour créer des détections personnalisées et générer des alertes
keywords: repérage avancé, repérage de menace, repérage de cybermenace, protection microsoft contre les menaces, microsoft 365, mtp, m365, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, microsoft 365, Protection Microsoft contre les menaces
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 4a4b601b5f8b9a21d7e7260fcadf9fecd0e37c5b
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51056661"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="58b61-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="58b61-104">Custom detections overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="58b61-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="58b61-105">**Applies to:**</span></span>
- <span data-ttu-id="58b61-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="58b61-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="58b61-107">Grâce aux détections personnalisées, vous pouvez surveiller et répondre de manière proactive à divers événements et états système, y compris les activités suspectées de violation et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="58b61-107">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="58b61-108">Cela est rendu possible par des règles de détection personnalisables qui déclenchent automatiquement des alertes ainsi que des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="58b61-108">This is made possible by customizable detection rules that automatically trigger alerts as well as response actions.</span></span>

<span data-ttu-id="58b61-109">Les détections personnalisées fonctionnent avec le repérage [avancé,](advanced-hunting-overview.md)qui fournit un langage de requête puissant et flexible qui couvre un large éventail d’événements et d’informations système à partir de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="58b61-109">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="58b61-110">Vous pouvez les configurer pour qu’ils s’exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu’il existe des correspondances.</span><span class="sxs-lookup"><span data-stu-id="58b61-110">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="58b61-111">Les détections personnalisées fournissent :</span><span class="sxs-lookup"><span data-stu-id="58b61-111">Custom detections provide:</span></span>
- <span data-ttu-id="58b61-112">Alertes pour les détections basées sur des règles conçues à partir de requêtes de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="58b61-112">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="58b61-113">Actions de réponse automatique</span><span class="sxs-lookup"><span data-stu-id="58b61-113">Automatic response actions</span></span>

## <a name="see-also"></a><span data-ttu-id="58b61-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58b61-114">See also</span></span>
- [<span data-ttu-id="58b61-115">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="58b61-115">Create and manage custom detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="58b61-116">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="58b61-116">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="58b61-117">Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58b61-117">Migrate advanced hunting queries from Microsoft Defender for Endpoint</span></span>](advanced-hunting-migrate-from-mde.md)