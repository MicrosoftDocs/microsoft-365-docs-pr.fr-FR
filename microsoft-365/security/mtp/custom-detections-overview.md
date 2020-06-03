---
title: Vue d’ensemble des détections personnalisées dans la protection contre les menaces Microsoft
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
ms.openlocfilehash: cdbaf9cfd2172656ed75cb3c0a1a9e361070f25b
ms.sourcegitcommit: 7bb3d8a93a85246172e2499d6c58c390e46f5bb9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44498350"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="ffa79-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="ffa79-104">Custom detections overview</span></span>

<span data-ttu-id="ffa79-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ffa79-105">**Applies to:**</span></span>
- <span data-ttu-id="ffa79-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ffa79-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="ffa79-107">Avec des détections personnalisées, vous pouvez surveiller et répondre de manière proactive aux divers événements et États du système, y compris l’activité de violation présumée et les points de terminaison mal configurés.</span><span class="sxs-lookup"><span data-stu-id="ffa79-107">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured endpoints.</span></span> <span data-ttu-id="ffa79-108">Cela est possible grâce à des règles de détection personnalisables qui déclenchent automatiquement des alertes et des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="ffa79-108">This is made possible by customizable detection rules that automatically trigger alerts as well as response actions.</span></span>

<span data-ttu-id="ffa79-109">Les détections personnalisées fonctionnent avec la [chasse avancée](advanced-hunting-overview.md), qui fournit un langage de requête puissant et flexible qui couvre un large éventail d’informations sur les événements et les systèmes de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="ffa79-109">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="ffa79-110">Vous pouvez les configurer pour qu’elles s’exécutent à intervalles réguliers, générant des alertes et en prenant des mesures de réponse chaque fois qu’il y a des correspondances.</span><span class="sxs-lookup"><span data-stu-id="ffa79-110">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="ffa79-111">Les détections personnalisées fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ffa79-111">Custom detections provide:</span></span>
- <span data-ttu-id="ffa79-112">Alertes pour les détections basées sur des règles et générées à partir de requêtes de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="ffa79-112">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="ffa79-113">Actions de réponse automatique</span><span class="sxs-lookup"><span data-stu-id="ffa79-113">Automatic response actions</span></span>

## <a name="related-topic"></a><span data-ttu-id="ffa79-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffa79-114">Related topic</span></span>
- [<span data-ttu-id="ffa79-115">Créer et gérer des règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="ffa79-115">Create and manage custom detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="ffa79-116">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="ffa79-116">Advanced hunting overview</span></span>](advanced-hunting-overview.md)