---
title: Événement Stream Microsoft Defender for Endpoint
description: Découvrez comment configurer Microsoft Defender ATP pour diffuser des événements de recherche avancée vers des hubs d’événements ou un compte de stockage Azure
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
ms.openlocfilehash: 22f4e4c974b60e291273eb9bebfa34583f4e2fb7
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063846"
---
# <a name="raw-data-streaming-api"></a><span data-ttu-id="40385-104">API de diffusion de données brutes</span><span class="sxs-lookup"><span data-stu-id="40385-104">Raw Data Streaming API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="40385-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="40385-105">**Applies to:**</span></span>
- [<span data-ttu-id="40385-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40385-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="40385-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="40385-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="40385-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="40385-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="stream-advanced-hunting-events-to-event-hubs-andor-azure-storage-account"></a><span data-ttu-id="40385-109">Diffusez des événements de recherche avancée sur des hubs d’événements et/ou un compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="40385-109">Stream Advanced Hunting events to Event Hubs and/or Azure storage account.</span></span>

<span data-ttu-id="40385-110">Defender pour le point de terminaison prend en charge la diffusion en continu de tous les événements disponibles via la recherche avancée vers un hub [d’événements](https://docs.microsoft.com/azure/event-hubs/) et/ou un [compte de stockage Azure.](https://docs.microsoft.com/azure/event-hubs/) [](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="40385-110">Defender for Endpoint supports streaming all the events available through [Advanced Hunting](advanced-hunting-overview.md) to an [Event Hubs](https://docs.microsoft.com/azure/event-hubs/) and/or [Azure storage account](https://docs.microsoft.com/azure/event-hubs/).</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4r4ga]


## <a name="in-this-section"></a><span data-ttu-id="40385-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="40385-111">In this section</span></span>

<span data-ttu-id="40385-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="40385-112">Topic</span></span> | <span data-ttu-id="40385-113">Description</span><span class="sxs-lookup"><span data-stu-id="40385-113">Description</span></span>
:---|:---
[<span data-ttu-id="40385-114">Diffuser des événements Microsoft Defender for Endpoint vers des Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="40385-114">Stream Microsoft Defender for Endpoint events to Azure Event Hubs</span></span>](raw-data-export-event-hub.md)| <span data-ttu-id="40385-115">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Defender pour le point de terminaison pour diffuser en continu [la](advanced-hunting-overview.md) recherche avancée vers les hubs d’événements.</span><span class="sxs-lookup"><span data-stu-id="40385-115">Learn about enabling the streaming API in your tenant and configure Defender for Endpoint to stream [Advanced Hunting](advanced-hunting-overview.md) to Event Hubs.</span></span>
[<span data-ttu-id="40385-116">Événements Stream Defender for Endpoint sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="40385-116">Stream Defender for Endpoint events to your Azure storage account</span></span>](raw-data-export-storage.md)| <span data-ttu-id="40385-117">En savoir plus sur l’activation de l’API de diffusion en continu dans votre client et configurer Defender pour le point de terminaison pour diffuser en continu la recherche [avancée](advanced-hunting-overview.md) sur votre compte de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="40385-117">Learn about enabling the streaming API in your tenant and configure Defender for Endpoint to stream [Advanced Hunting](advanced-hunting-overview.md) to your Azure storage account.</span></span>


## <a name="related-topics"></a><span data-ttu-id="40385-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40385-118">Related topics</span></span>
- [<span data-ttu-id="40385-119">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="40385-119">Overview of Advanced Hunting</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="40385-120">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="40385-120">Azure Event Hubs documentation</span></span>](https://docs.microsoft.com/azure/event-hubs/)
- [<span data-ttu-id="40385-121">Documentation du compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="40385-121">Azure Storage Account documentation</span></span>](https://docs.microsoft.com/azure/storage/common/storage-account-overview)