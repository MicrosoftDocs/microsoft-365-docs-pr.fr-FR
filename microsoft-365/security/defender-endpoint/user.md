---
title: Type de ressource utilisateur
description: Récupérer les alertes récentes de Microsoft Defender pour les points de terminaison relatives aux utilisateurs.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
search.product: eADQiWindows 10XVcnh
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 39b73772bcc626590aa784bb5b21357f66229816
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772136"
---
# <a name="user-resource-type"></a><span data-ttu-id="810b1-104">Type de ressource utilisateur</span><span class="sxs-lookup"><span data-stu-id="810b1-104">User resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="810b1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="810b1-105">**Applies to:**</span></span>
- [<span data-ttu-id="810b1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="810b1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="810b1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="810b1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="810b1-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="810b1-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="810b1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="810b1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="810b1-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="810b1-110">Method</span></span>|<span data-ttu-id="810b1-111">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="810b1-111">Return Type</span></span> |<span data-ttu-id="810b1-112">Description</span><span class="sxs-lookup"><span data-stu-id="810b1-112">Description</span></span>
:---|:---|:---
[<span data-ttu-id="810b1-113">Liste des alertes associées à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="810b1-113">List User related alerts</span></span>](get-user-related-alerts.md) | <span data-ttu-id="810b1-114">collection[alert](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="810b1-114">[alert](alerts.md) collection</span></span> |  <span data-ttu-id="810b1-115">Liste de toutes les alertes associées à un [utilisateur.](user.md)</span><span class="sxs-lookup"><span data-stu-id="810b1-115">List all the alerts that are associated with a [user](user.md).</span></span>
[<span data-ttu-id="810b1-116">List User related devices</span><span class="sxs-lookup"><span data-stu-id="810b1-116">List User related devices</span></span>](get-user-related-machines.md) | <span data-ttu-id="810b1-117">[collection d’ordinateurs](machine.md)</span><span class="sxs-lookup"><span data-stu-id="810b1-117">[machine](machine.md) collection</span></span> | <span data-ttu-id="810b1-118">Liste de tous les appareils qui ont été connectés par un [utilisateur.](user.md)</span><span class="sxs-lookup"><span data-stu-id="810b1-118">List all the devices that were logged on by a [user](user.md).</span></span>
