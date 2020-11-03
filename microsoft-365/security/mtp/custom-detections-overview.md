---
title: Vue d’ensemble des détections personnalisées dans Microsoft 365 Defender
description: Comprendre comment utiliser la chasse avancée pour créer des détections personnalisées et générer des alertes
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, détections personnalisées, schéma, Kusto, Microsoft 365, protection contre les menaces Microsoft
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: fe2b9f1b52fa2c8d9031bb58597992f3dda91520
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843911"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="5ac38-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="5ac38-104">Custom detections overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="5ac38-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5ac38-105">**Applies to:**</span></span>
- <span data-ttu-id="5ac38-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5ac38-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="5ac38-107">Avec des détections personnalisées, vous pouvez surveiller et répondre de manière proactive aux divers événements et États du système, y compris l’activité de violation présumée et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="5ac38-107">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="5ac38-108">Cela est possible grâce à des règles de détection personnalisables qui déclenchent automatiquement des alertes et des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="5ac38-108">This is made possible by customizable detection rules that automatically trigger alerts as well as response actions.</span></span>

<span data-ttu-id="5ac38-109">Les détections personnalisées fonctionnent avec la [chasse avancée](advanced-hunting-overview.md), qui fournit un langage de requête puissant et flexible qui couvre un large éventail d’informations sur les événements et les systèmes de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="5ac38-109">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="5ac38-110">Vous pouvez les configurer pour qu’elles s’exécutent à intervalles réguliers, générant des alertes et en prenant des mesures de réponse chaque fois qu’il y a des correspondances.</span><span class="sxs-lookup"><span data-stu-id="5ac38-110">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="5ac38-111">Les détections personnalisées fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ac38-111">Custom detections provide:</span></span>
- <span data-ttu-id="5ac38-112">Alertes pour les détections basées sur des règles et générées à partir de requêtes de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="5ac38-112">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="5ac38-113">Actions de réponse automatique</span><span class="sxs-lookup"><span data-stu-id="5ac38-113">Automatic response actions</span></span>

## <a name="related-topic"></a><span data-ttu-id="5ac38-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ac38-114">Related topic</span></span>
- [<span data-ttu-id="5ac38-115">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="5ac38-115">Create and manage custom detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="5ac38-116">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5ac38-116">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
