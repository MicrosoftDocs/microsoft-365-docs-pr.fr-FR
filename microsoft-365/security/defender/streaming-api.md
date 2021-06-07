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
ms.openlocfilehash: 21a83c4876a90a231eb2a78d10a290be2dca2fa0
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782476"
---
# <a name="streaming-api"></a><span data-ttu-id="24e46-104">API de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="24e46-104">Streaming API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="24e46-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="24e46-105">**Applies to:**</span></span>
- [<span data-ttu-id="24e46-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="24e46-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="stream-advanced-hunting-events-to-event-hubs-andor-azure-storage-account"></a><span data-ttu-id="24e46-107">Diffusez des événements de recherche avancée sur des hubs d’événements et/ou un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="24e46-107">Stream Advanced Hunting events to Event Hubs and/or Azure storage account.</span></span>

<span data-ttu-id="24e46-108">Microsoft 365 Defender prend en charge les événements de diffusion en continu [via le service de](../defender/advanced-hunting-overview.md) recherche avancée sur un hub [d’événements](/azure/event-hubs/) et/ou un [compte de stockage Azure.](/azure/event-hubs/)</span><span class="sxs-lookup"><span data-stu-id="24e46-108">Microsoft 365 Defender supports streaming events through [Advanced Hunting](../defender/advanced-hunting-overview.md) to an [Event Hubs](/azure/event-hubs/) and/or [Azure storage account](/azure/event-hubs/).</span></span>



## <a name="in-this-section"></a><span data-ttu-id="24e46-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="24e46-109">In this section</span></span>

<span data-ttu-id="24e46-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="24e46-110">Topic</span></span> | <span data-ttu-id="24e46-111">Description</span><span class="sxs-lookup"><span data-stu-id="24e46-111">Description</span></span>
:---|:---
[<span data-ttu-id="24e46-112">Flux d’événements dans les Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="24e46-112">Stream events to Azure Event Hubs</span></span>](streaming-api-event-hub.md)| <span data-ttu-id="24e46-113">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu la recherche avancée vers [les](../defender/advanced-hunting-overview.md) hubs d’événements.</span><span class="sxs-lookup"><span data-stu-id="24e46-113">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](../defender/advanced-hunting-overview.md) to Event Hubs.</span></span>
[<span data-ttu-id="24e46-114">Flux d’événements sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="24e46-114">Stream events to your Azure storage account</span></span>](streaming-api-storage.md)| <span data-ttu-id="24e46-115">Découvrez comment activer l’API de diffusion en continu dans votre client et configurer Microsoft 365 Defender pour diffuser en continu la recherche avancée [sur](advanced-hunting-overview.md) votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="24e46-115">Learn about enabling the streaming API in your tenant and configure Microsoft 365 Defender to stream [Advanced Hunting](advanced-hunting-overview.md) to your Azure storage account.</span></span>


## <a name="related-topics"></a><span data-ttu-id="24e46-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24e46-116">Related topics</span></span>
- [<span data-ttu-id="24e46-117">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="24e46-117">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="24e46-118">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="24e46-118">Azure Event Hubs documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="24e46-119">stockage Azure Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="24e46-119">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)
