---
title: Événement Stream Microsoft Defender for Endpoint
description: Découvrez comment configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers des hubs d’événements ou un compte de stockage Azure
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
ms.custom: api
ms.openlocfilehash: c8403dee11070dcf0825fad2502d8d21d54933fd
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782752"
---
# <a name="raw-data-streaming-api"></a><span data-ttu-id="f3c95-104">API de diffusion de données brutes</span><span class="sxs-lookup"><span data-stu-id="f3c95-104">Raw Data Streaming API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f3c95-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f3c95-105">**Applies to:**</span></span>
- [<span data-ttu-id="f3c95-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f3c95-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="f3c95-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="f3c95-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="f3c95-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f3c95-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="stream-advanced-hunting-events-to-event-hubs-andor-azure-storage-account"></a><span data-ttu-id="f3c95-109">Diffusez des événements de recherche avancée sur des hubs d’événements et/ou un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c95-109">Stream Advanced Hunting events to Event Hubs and/or Azure storage account.</span></span>


<span data-ttu-id="f3c95-110">Microsoft Defender pour le point [](../defender/advanced-hunting-overview.md) de terminaison prend en charge les événements de diffusion en continu disponibles via le service de recherche avancée sur un hub [d’événements](/azure/event-hubs/) et/ou un [compte de stockage Azure.](/azure/storage/common/storage-account-overview)</span><span class="sxs-lookup"><span data-stu-id="f3c95-110">Microsoft Defender for Endpoint supports streaming events available through [Advanced Hunting](../defender/advanced-hunting-overview.md) to an [Event Hubs](/azure/event-hubs/) and/or [Azure storage account](/azure/storage/common/storage-account-overview).</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4r4ga]


## <a name="in-this-section"></a><span data-ttu-id="f3c95-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f3c95-111">In this section</span></span>

<span data-ttu-id="f3c95-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f3c95-112">Topic</span></span> | <span data-ttu-id="f3c95-113">Description</span><span class="sxs-lookup"><span data-stu-id="f3c95-113">Description</span></span>
:---|:---
[<span data-ttu-id="f3c95-114">Diffuser des événements Microsoft Defender for Endpoint vers des Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="f3c95-114">Stream Microsoft Defender for Endpoint events to Azure Event Hubs</span></span>](raw-data-export-event-hub.md)| <span data-ttu-id="f3c95-115">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Defender pour le point de terminaison pour diffuser en continu [la](advanced-hunting-overview.md) recherche avancée vers les hubs d’événements.</span><span class="sxs-lookup"><span data-stu-id="f3c95-115">Learn about enabling the streaming API in your tenant and configure Defender for Endpoint to stream [Advanced Hunting](advanced-hunting-overview.md) to Event Hubs.</span></span>
[<span data-ttu-id="f3c95-116">Événements Stream Defender for Endpoint sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f3c95-116">Stream Defender for Endpoint events to your Azure storage account</span></span>](raw-data-export-storage.md)| <span data-ttu-id="f3c95-117">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Defender pour le point de terminaison pour diffuser en continu la recherche [avancée](advanced-hunting-overview.md) sur votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c95-117">Learn about enabling the streaming API in your tenant and configure Defender for Endpoint to stream [Advanced Hunting](advanced-hunting-overview.md) to your Azure storage account.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f3c95-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c95-118">Related topics</span></span>
- [<span data-ttu-id="f3c95-119">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="f3c95-119">Overview of Advanced Hunting</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="f3c95-120">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="f3c95-120">Azure Event Hubs documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="f3c95-121">stockage Azure Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="f3c95-121">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)