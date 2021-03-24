---
title: Vue d’ensemble des détections personnalisées dans Microsoft Defender ATP
ms.reviewer: ''
description: Comprendre comment utiliser le repérage avancé pour créer des détections personnalisées et générer des alertes
keywords: détections personnalisées, alertes, règles de détection, repérage avancé, recherche, requête, actions de réponse, intervalle, mdatp, microsoft defender atp
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 6c9befcc4b1224cacb2ab4eb8530e30a397aab49
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51056737"
---
# <a name="custom-detections-overview"></a><span data-ttu-id="76bf3-104">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="76bf3-104">Custom detections overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="76bf3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="76bf3-105">**Applies to:**</span></span>
- [<span data-ttu-id="76bf3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="76bf3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="76bf3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="76bf3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="76bf3-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="76bf3-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="76bf3-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="76bf3-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="76bf3-110">Grâce aux détections personnalisées, vous pouvez surveiller et répondre de manière proactive à divers événements et états système, y compris les activités suspectées de violation et les appareils mal configurés.</span><span class="sxs-lookup"><span data-stu-id="76bf3-110">With custom detections, you can proactively monitor for and respond to various events and system states, including suspected breach activity and misconfigured devices.</span></span> <span data-ttu-id="76bf3-111">Vous pouvez le faire avec des règles de détection personnalisables qui déclenchent automatiquement des alertes et des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="76bf3-111">You can do this with customizable detection rules that automatically trigger alerts and response actions.</span></span>

<span data-ttu-id="76bf3-112">Les détections personnalisées fonctionnent avec le repérage [avancé,](advanced-hunting-overview.md)qui fournit un langage de requête puissant et flexible qui couvre un large éventail d’événements et d’informations système à partir de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="76bf3-112">Custom detections work with [advanced hunting](advanced-hunting-overview.md), which provides a powerful, flexible query language that covers a broad set of event and system information from your network.</span></span> <span data-ttu-id="76bf3-113">Vous pouvez les configurer pour qu’ils s’exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu’il existe des correspondances.</span><span class="sxs-lookup"><span data-stu-id="76bf3-113">You can set them to run at regular intervals, generating alerts and taking response actions whenever there are matches.</span></span>

<span data-ttu-id="76bf3-114">Les détections personnalisées fournissent :</span><span class="sxs-lookup"><span data-stu-id="76bf3-114">Custom detections provide:</span></span>
- <span data-ttu-id="76bf3-115">Alertes pour les détections basées sur des règles conçues à partir de requêtes de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="76bf3-115">Alerts for rule-based detections built from advanced hunting queries</span></span>
- <span data-ttu-id="76bf3-116">Actions de réponse automatique qui s’appliquent aux fichiers et appareils</span><span class="sxs-lookup"><span data-stu-id="76bf3-116">Automatic response actions that apply to files and devices</span></span>

## <a name="related-topics"></a><span data-ttu-id="76bf3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76bf3-117">Related topics</span></span>
- [<span data-ttu-id="76bf3-118">Créer des règles de détection</span><span class="sxs-lookup"><span data-stu-id="76bf3-118">Create detection rules</span></span>](custom-detection-rules.md)
- [<span data-ttu-id="76bf3-119">Afficher et gérer les règles de détection</span><span class="sxs-lookup"><span data-stu-id="76bf3-119">View and manage detection rules</span></span>](custom-detections-manage.md)
- [<span data-ttu-id="76bf3-120">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="76bf3-120">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
