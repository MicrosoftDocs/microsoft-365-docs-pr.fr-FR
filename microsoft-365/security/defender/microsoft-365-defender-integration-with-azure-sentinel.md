---
title: Microsoft 365 Intégration de Defender à Azure Sentinel
description: Utilisez Azure Sentinel comme SIEM pour Microsoft 365 incident et événements Defender.
keywords: incidents, alertes, examiner, analyser, réponse, corrélation, attaque, ordinateurs, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 7d9cff584f35c39544034501c607b7156a0f1bf2
ms.sourcegitcommit: 3b9fab82d63aea41d5f544938868c5d2cbf52d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52782920"
---
# <a name="microsoft-365-defender-integration-with-azure-sentinel"></a><span data-ttu-id="de9cf-104">Microsoft 365 Intégration de Defender à Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="de9cf-104">Microsoft 365 Defender integration with Azure Sentinel</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="de9cf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="de9cf-105">**Applies to:**</span></span>
- <span data-ttu-id="de9cf-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="de9cf-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="de9cf-107">Le connecteur Microsoft 365 Defender pour Azure Sentinel (prévisualisation) envoie tous les incidents Microsoft 365 Defender et les informations d’alerte à Azure Sentinel et maintient les incidents synchronisés.</span><span class="sxs-lookup"><span data-stu-id="de9cf-107">The Microsoft 365 Defender connector for Azure Sentinel (preview) sends all Microsoft 365 Defender incidents and alerts information to Azure Sentinel and keeps the incidents synchronized.</span></span> 

<span data-ttu-id="de9cf-108">Une fois que vous avez ajouté le connecteur, les incidents Microsoft 365 Defender qui incluent toutes les alertes associées, entités et informations pertinentes reçues de Microsoft Defender pour le point de terminaison, Microsoft Defender pour l’identité, Microsoft Defender pour Office 365 et Microsoft Cloud App Security sont diffusés à Azure Sentinel en tant que données d’informations de sécurité et de gestion des événements &mdash; (SIEM), ce qui vous permet d’effectuer un tri et une réponse aux incidents avec &mdash; Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="de9cf-108">Once you add the connector, Microsoft 365 Defender incidents&mdash;which include all associated alerts, entities, and relevant information received from Microsoft Defender for Endpoint, Microsoft Defender for Identity, Microsoft Defender for Office 365, and Microsoft Cloud App Security&mdash;are streamed to Azure Sentinel as security information and event management (SIEM) data, providing you with context to perform triage and incident response with Azure Sentinel.</span></span> 

<span data-ttu-id="de9cf-109">Une fois dans Azure Sentinel, les incidents restent synchronisés de façon bi-direction avec Microsoft 365 Defender, ce qui vous permet de tirer parti des avantages du centre de sécurité Microsoft 365 et d’Azure Sentinel dans le portail Azure pour l’examen et la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="de9cf-109">Once in Azure Sentinel, incidents remain bi-directionally synchronized with Microsoft 365 Defender, allowing you to take advantage of the benefits of both the Microsoft 365 security center and Azure Sentinel in the Azure portal for incident investigation and response.</span></span>

<span data-ttu-id="de9cf-110">Voici comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="de9cf-110">Here's how it works.</span></span>

:::image type="content" source="../../media/microsoft-365-defender-integration-with-azure-sentinel/microsoft-365-defender-integration-with-azure-sentinel.png" alt-text="Flux et partage des données d’incident entre Microsoft 365 Defender et Azure Sentinel":::

## <a name="next-steps"></a><span data-ttu-id="de9cf-112">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="de9cf-112">Next steps</span></span>

1. <span data-ttu-id="de9cf-113">Obtenez une compréhension approfondie de [l’intégration Microsoft 365 Defender à Azure Sentinel.](/azure/sentinel/microsoft-365-defender-sentinel-integration)</span><span class="sxs-lookup"><span data-stu-id="de9cf-113">Get a deeper understanding of [Microsoft 365 Defender integration with Azure Sentinel](/azure/sentinel/microsoft-365-defender-sentinel-integration).</span></span>
2. <span data-ttu-id="de9cf-114">[Connecter données de Microsoft 365 Defender à Azure Sentinel](/azure/sentinel/connect-microsoft-365-defender).</span><span class="sxs-lookup"><span data-stu-id="de9cf-114">[Connect data from Microsoft 365 Defender to Azure Sentinel](/azure/sentinel/connect-microsoft-365-defender).</span></span>

## <a name="see-also"></a><span data-ttu-id="de9cf-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de9cf-115">See also</span></span>

- [<span data-ttu-id="de9cf-116">Vue d’ensemble des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="de9cf-116">Overview of incidents in Microsoft 365 Defender</span></span>](incidents-overview.md)
- [<span data-ttu-id="de9cf-117">Examiner les incidents avec Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="de9cf-117">Investigate incidents with Azure Sentinel</span></span>](/azure/sentinel/tutorial-investigate-cases)
