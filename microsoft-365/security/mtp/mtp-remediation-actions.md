---
title: Actions de correction dans les fonctionnalités d’enquête et de réponse automatisées dans Microsoft Threat Protection
description: Obtenez une vue d’ensemble des fonctionnalités d’examen et réponses automatisés dans Protection Microsoft contre les menaces
keywords: automatisation, examen, alerte, déclencheur, action, correction
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 65ace4bda091b3e000d25a984b706f26fe9c8696
ms.sourcegitcommit: 48b69caf6550e68cb14472ea8cfc76b53e7ae9c6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2020
ms.locfileid: "42225482"
---
# <a name="remediation-actions-in-automated-investigation-and-response-capabilities-in-microsoft-threat-protection"></a><span data-ttu-id="d7f5c-104">Actions de correction dans les fonctionnalités d’enquête et de réponse automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d7f5c-104">Remediation actions in automated investigation and response capabilities in Microsoft Threat Protection</span></span>

<span data-ttu-id="d7f5c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d7f5c-105">**Applies to:**</span></span>
- <span data-ttu-id="d7f5c-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="d7f5c-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="d7f5c-107">Les fonctionnalités d’analyse et de réponse automatisées dans Microsoft Threat Protection incluent certaines actions de correction.</span><span class="sxs-lookup"><span data-stu-id="d7f5c-107">Automated investigation and response capabilities in Microsoft Threat Protection include certain remediation actions.</span></span> <span data-ttu-id="d7f5c-108">Certains types d’actions de correction sont pris sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d7f5c-108">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="d7f5c-109">D’autres actions de correction sont appliquées au contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="d7f5c-109">Other remediation actions are taken on email content.</span></span>

<span data-ttu-id="d7f5c-110">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="d7f5c-110">The following table summarizes remediation actions that are currently supported in Microsoft Threat Protection:</span></span> 

|<span data-ttu-id="d7f5c-111">Actions de correction des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="d7f5c-111">Endpoints remediation actions</span></span>  |<span data-ttu-id="d7f5c-112">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="d7f5c-112">Email remediation actions</span></span>  |
|---------|---------|
|<span data-ttu-id="d7f5c-113">Fichier de quarantaine</span><span class="sxs-lookup"><span data-stu-id="d7f5c-113">Quarantine file</span></span><br/><span data-ttu-id="d7f5c-114">Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="d7f5c-114">Remove registry key</span></span><br/><span data-ttu-id="d7f5c-115">Processus d’arrêt</span><span class="sxs-lookup"><span data-stu-id="d7f5c-115">Kill process</span></span> <br/><span data-ttu-id="d7f5c-116">Arrêter le service</span><span class="sxs-lookup"><span data-stu-id="d7f5c-116">Stop service</span></span> <br/><span data-ttu-id="d7f5c-117">Désactiver le pilote</span><span class="sxs-lookup"><span data-stu-id="d7f5c-117">Disable driver</span></span> <br/><span data-ttu-id="d7f5c-118">Supprimer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="d7f5c-118">Remove scheduled task</span></span>      |<span data-ttu-id="d7f5c-119">Supprimer (récupération possible) le courrier ou des clusters</span><span class="sxs-lookup"><span data-stu-id="d7f5c-119">Soft delete email messages or clusters</span></span><br/><span data-ttu-id="d7f5c-120">Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="d7f5c-120">Block URL (time-of-click)</span></span><br/><span data-ttu-id="d7f5c-121">Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="d7f5c-121">Turn off external mail forwarding</span></span>          |

<span data-ttu-id="d7f5c-122">Les actions de correction, qu’elles soient en attente d’approbation ou qui sont déjà terminées, peuvent être affichées dans le [Centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="d7f5c-122">Remediation actions, whether they're pending approval or are already complete, can be viewed in the [Action Center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span></span>

## <a name="next-steps"></a><span data-ttu-id="d7f5c-123">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d7f5c-123">Next steps</span></span>

- [<span data-ttu-id="d7f5c-124">Approuver ou refuser les actions liées à un examen et réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="d7f5c-124">Approve or reject actions related to automated investigation and response</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)
- <span data-ttu-id="d7f5c-125">[En savoir plus sur le centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="d7f5c-125">[Learn more about the Action center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)</span></span>
