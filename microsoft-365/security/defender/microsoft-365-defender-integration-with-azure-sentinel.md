---
title: intégration de Microsoft 365 Defender à Azure Sentinel
description: Utilisez Azure Sentinel comme SIEM pour Microsoft 365 Defender incident et les événements.
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
ms.openlocfilehash: b9a9a6381c93e2d252f75710adc206868c0a5546
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229910"
---
# <a name="microsoft-365-defender-integration-with-azure-sentinel"></a><span data-ttu-id="59b5a-104">intégration de Microsoft 365 Defender à Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="59b5a-104">Microsoft 365 Defender integration with Azure Sentinel</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="59b5a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="59b5a-105">**Applies to:**</span></span>
- <span data-ttu-id="59b5a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="59b5a-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="59b5a-107">Le connecteur Microsoft 365 Defender pour Azure Sentinel (prévisualisation) envoie tous les incidents Microsoft 365 Defender et les informations d’alerte à Azure Sentinel et maintient les incidents synchronisés.</span><span class="sxs-lookup"><span data-stu-id="59b5a-107">The Microsoft 365 Defender connector for Azure Sentinel (preview) sends all Microsoft 365 Defender incidents and alerts information to Azure Sentinel and keeps the incidents synchronized.</span></span> 

<span data-ttu-id="59b5a-108">Une fois que vous avez ajouté le connecteur, les incidents Microsoft 365 Defender qui incluent toutes les alertes associées, entités et informations pertinentes reçues de Microsoft Defender pour le point de terminaison, Microsoft Defender pour l’identité, Microsoft Defender pour Office 365 et Microsoft Cloud App Security sont diffusés vers Azure Sentinel en tant qu’informations de sécurité et données de gestion des événements &mdash; (SIEM), ce qui vous offre un contexte pour effectuer un tri et une réponse aux incidents avec &mdash; Azure Sentinel.</span><span class="sxs-lookup"><span data-stu-id="59b5a-108">Once you add the connector, Microsoft 365 Defender incidents&mdash;which include all associated alerts, entities, and relevant information received from Microsoft Defender for Endpoint, Microsoft Defender for Identity, Microsoft Defender for Office 365, and Microsoft Cloud App Security&mdash;are streamed to Azure Sentinel as security information and event management (SIEM) data, providing you with context to perform triage and incident response with Azure Sentinel.</span></span> 

<span data-ttu-id="59b5a-109">Une fois dans Azure Sentinel, les incidents restent synchronisés de manière bi-direction avec Microsoft 365 Defender, ce qui vous permet de tirer parti des avantages du centre de sécurité Microsoft 365 et d’Azure Sentinel dans le portail Azure pour l’examen et la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="59b5a-109">Once in Azure Sentinel, incidents remain bi-directionally synchronized with Microsoft 365 Defender, allowing you to take advantage of the benefits of both the Microsoft 365 security center and Azure Sentinel in the Azure portal for incident investigation and response.</span></span>

<span data-ttu-id="59b5a-110">Regardez cette courte vue d’ensemble de l’intégration d’Azure Sentinel Microsoft 365 Defender (4 minutes).</span><span class="sxs-lookup"><span data-stu-id="59b5a-110">Watch this short overview of Azure Sentinel integration with Microsoft 365 Defender (4 minutes).</span></span>

<br>

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWFIRo]


<span data-ttu-id="59b5a-111">Voici comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="59b5a-111">Here's how it works.</span></span>

:::image type="content" source="../../media/microsoft-365-defender-integration-with-azure-sentinel/microsoft-365-defender-integration-with-azure-sentinel.png" alt-text="Le flux et le partage des données d’incident entre Microsoft 365 Defender et Azure Sentinel":::

## <a name="next-steps"></a><span data-ttu-id="59b5a-113">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="59b5a-113">Next steps</span></span>

1. <span data-ttu-id="59b5a-114">Obtenez une compréhension plus approfondie de [l Microsoft 365 Defender’intégration à Azure Sentinel.](/azure/sentinel/microsoft-365-defender-sentinel-integration)</span><span class="sxs-lookup"><span data-stu-id="59b5a-114">Get a deeper understanding of [Microsoft 365 Defender integration with Azure Sentinel](/azure/sentinel/microsoft-365-defender-sentinel-integration).</span></span>
2. <span data-ttu-id="59b5a-115">[Connecter données de Microsoft 365 Defender à Azure Sentinel](/azure/sentinel/connect-microsoft-365-defender).</span><span class="sxs-lookup"><span data-stu-id="59b5a-115">[Connect data from Microsoft 365 Defender to Azure Sentinel](/azure/sentinel/connect-microsoft-365-defender).</span></span>

## <a name="see-also"></a><span data-ttu-id="59b5a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59b5a-116">See also</span></span>

- [<span data-ttu-id="59b5a-117">Vue d’ensemble des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="59b5a-117">Overview of incidents in Microsoft 365 Defender</span></span>](incidents-overview.md)
- [<span data-ttu-id="59b5a-118">Examiner les incidents avec Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="59b5a-118">Investigate incidents with Azure Sentinel</span></span>](/azure/sentinel/tutorial-investigate-cases)
