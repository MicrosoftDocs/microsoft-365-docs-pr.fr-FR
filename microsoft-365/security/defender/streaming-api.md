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
ms.openlocfilehash: fad3dd64c9acf079bd8da778d417240c44031569
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772440"
---
# <a name="streaming-api"></a><span data-ttu-id="f46e0-104">API de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="f46e0-104">Streaming API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f46e0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f46e0-105">**Applies to:**</span></span>
- [<span data-ttu-id="f46e0-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f46e0-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="stream-advanced-hunting-events-to-event-hubs-andor-azure-storage-account"></a><span data-ttu-id="f46e0-107">Diffusez des événements de recherche avancée sur des hubs d’événements et/ou un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f46e0-107">Stream Advanced Hunting events to Event Hubs and/or Azure storage account.</span></span>

<span data-ttu-id="f46e0-108">Microsoft 365 Defender prend en charge la diffusion en continu de tous les événements disponibles via [la](../defender/advanced-hunting-overview.md) recherche avancée vers un hub [d’événements](/azure/event-hubs/) et/ou un [compte de stockage Azure.](/azure/event-hubs/)</span><span class="sxs-lookup"><span data-stu-id="f46e0-108">Microsoft 365 Defender supports streaming all the events available through [Advanced Hunting](../defender/advanced-hunting-overview.md) to an [Event Hubs](/azure/event-hubs/) and/or [Azure storage account](/azure/event-hubs/).</span></span>



## <a name="in-this-section"></a><span data-ttu-id="f46e0-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f46e0-109">In this section</span></span>

<span data-ttu-id="f46e0-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f46e0-110">Topic</span></span> | <span data-ttu-id="f46e0-111">Description</span><span class="sxs-lookup"><span data-stu-id="f46e0-111">Description</span></span>
:---|:---
[<span data-ttu-id="f46e0-112">Flux d’événements dans les Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="f46e0-112">Stream events to Azure Event Hubs</span></span>](streaming-api-event-hub.md)| <span data-ttu-id="f46e0-113">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu le recherche avancée [sur](../defender/advanced-hunting-overview.md) les hubs d’événements.</span><span class="sxs-lookup"><span data-stu-id="f46e0-113">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](../defender/advanced-hunting-overview.md) to Event Hubs.</span></span>
[<span data-ttu-id="f46e0-114">Flux d’événements sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f46e0-114">Stream events to your Azure storage account</span></span>](streaming-api-storage.md)| <span data-ttu-id="f46e0-115">Découvrez comment activer l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu la recherche avancée [sur](advanced-hunting-overview.md) votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f46e0-115">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](advanced-hunting-overview.md) to your Azure storage account.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f46e0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f46e0-116">Related topics</span></span>
- [<span data-ttu-id="f46e0-117">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="f46e0-117">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="f46e0-118">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="f46e0-118">Azure Event Hubs documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="f46e0-119">stockage Azure Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="f46e0-119">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)
