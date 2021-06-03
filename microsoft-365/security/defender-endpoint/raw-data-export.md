---
title: Événements Stream Microsoft 365 Defender
description: Découvrez comment configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers des hubs d’événements ou un compte de stockage Azure
keywords: exportation de données brutes, API de diffusion en continu, API, hubs d’événements, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 0c25ec8bc88a2714fb2f02ef8641c3eae700efe0
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730689"
---
# <a name="streaming-api"></a><span data-ttu-id="c5994-104">API de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="c5994-104">Streaming API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c5994-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c5994-105">**Applies to:**</span></span>
- [<span data-ttu-id="c5994-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c5994-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="stream-advanced-hunting-events-to-event-hubs-andor-azure-storage-account"></a><span data-ttu-id="c5994-107">Diffusez des événements de recherche avancée sur des hubs d’événements et/ou un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="c5994-107">Stream Advanced Hunting events to Event Hubs and/or Azure storage account.</span></span>

<span data-ttu-id="c5994-108">Microsoft 365 Defender prend en charge la diffusion en continu de tous les événements disponibles via [la](../defender/advanced-hunting-overview.md) recherche avancée vers un hub [d’événements](/azure/event-hubs/) et/ou un [compte de stockage Azure.](/azure/event-hubs/)</span><span class="sxs-lookup"><span data-stu-id="c5994-108">Microsoft 365 Defender supports streaming all the events available through [Advanced Hunting](../defender/advanced-hunting-overview.md) to an [Event Hubs](/azure/event-hubs/) and/or [Azure storage account](/azure/event-hubs/).</span></span>



## <a name="in-this-section"></a><span data-ttu-id="c5994-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c5994-109">In this section</span></span>

<span data-ttu-id="c5994-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c5994-110">Topic</span></span> | <span data-ttu-id="c5994-111">Description</span><span class="sxs-lookup"><span data-stu-id="c5994-111">Description</span></span>
:---|:---
[<span data-ttu-id="c5994-112">Flux d’événements dans les Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="c5994-112">Stream events to Azure Event Hubs</span></span>](raw-data-export-event-hub.md)| <span data-ttu-id="c5994-113">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu la recherche avancée vers [les](../defender/advanced-hunting-overview.md) hubs d’événements.</span><span class="sxs-lookup"><span data-stu-id="c5994-113">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](../defender/advanced-hunting-overview.md) to Event Hubs.</span></span>
[<span data-ttu-id="c5994-114">Flux d’événements sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="c5994-114">Stream events to your Azure storage account</span></span>](raw-data-export-storage.md)| <span data-ttu-id="c5994-115">Découvrez comment activer l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu la recherche avancée [sur](../defender/advanced-hunting-overview.md) votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="c5994-115">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](../defender/advanced-hunting-overview.md) to your Azure storage account.</span></span>


## <a name="related-topics"></a><span data-ttu-id="c5994-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5994-116">Related topics</span></span>
- [<span data-ttu-id="c5994-117">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="c5994-117">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="c5994-118">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="c5994-118">Azure Event Hubs documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="c5994-119">stockage Azure Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="c5994-119">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)
