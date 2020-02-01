---
title: Comment signaler les faux positifs ou les faux négatifs dans AIR dans la protection contre les menaces Microsoft
description: Un message a-t-il été manqué ou incorrectement détecté par AIR dans la protection contre les menaces Microsoft ? Découvrez comment soumettre des faux positifs ou faux négatifs à Microsoft pour analyse.
keywords: automatisation, analyse, alerte, déclencheur, action, correction, faux positif, faux négatif
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
ms.openlocfilehash: d9175e78326832a2be874359babae5ae9c689420
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600081"
---
# <a name="how-to-report-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a><span data-ttu-id="f695d-105">Comment signaler les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="f695d-105">How to report false positives/negatives in automated investigation and response capabilities</span></span>

<span data-ttu-id="f695d-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f695d-106">**Applies to:**</span></span>
- <span data-ttu-id="f695d-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f695d-107">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="f695d-108">La protection contre les menaces a-t-elle permis d’effectuer des [recherches et des réponses automatiques](mtp-autoir.md) dans Microsoft Threat Protection ?</span><span class="sxs-lookup"><span data-stu-id="f695d-108">Did [automated investigation and response capabilities](mtp-autoir.md) in Microsoft Threat Protection miss or wrongly detect something?</span></span> <span data-ttu-id="f695d-109">Vous pouvez le signaler à Microsoft ou ajuster vos alertes (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="f695d-109">You can report it to Microsoft or adjust your alerts (if needed).</span></span> <span data-ttu-id="f695d-110">Utilisez le tableau suivant comme guide :</span><span class="sxs-lookup"><span data-stu-id="f695d-110">Use the following table as a guide:</span></span> 


|<span data-ttu-id="f695d-111">Item</span><span class="sxs-lookup"><span data-stu-id="f695d-111">Item</span></span>  |<span data-ttu-id="f695d-112">Détectés par</span><span class="sxs-lookup"><span data-stu-id="f695d-112">Detected by</span></span>  |<span data-ttu-id="f695d-113">Comment le signaler</span><span class="sxs-lookup"><span data-stu-id="f695d-113">How to report it</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="f695d-114">Message électronique</span><span class="sxs-lookup"><span data-stu-id="f695d-114">Email message</span></span> <br/><span data-ttu-id="f695d-115">Pièce jointe de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="f695d-115">Email attachment</span></span> <br/><span data-ttu-id="f695d-116">URL dans un message électronique ou un fichier Office</span><span class="sxs-lookup"><span data-stu-id="f695d-116">URL in an email message or Office file</span></span>      |[<span data-ttu-id="f695d-117">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f695d-117">Office 365 Advanced Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)        |[<span data-ttu-id="f695d-118">Soumission de courrier indésirable, hameçon, URL et fichiers suspects à Microsoft pour l’analyse Office 365</span><span class="sxs-lookup"><span data-stu-id="f695d-118">Submit suspected spam, phish, URLs, and files to Microsoft for Office 365 scanning</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission)         |
|<span data-ttu-id="f695d-119">Fichier ou application sur un appareil</span><span class="sxs-lookup"><span data-stu-id="f695d-119">File or app on a device</span></span>    |[<span data-ttu-id="f695d-120">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f695d-120">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection)         |[<span data-ttu-id="f695d-121">Envoi d’un fichier à Microsoft pour l’analyse des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="f695d-121">Submit a file to Microsoft for malware analysis</span></span>](https://www.microsoft.com/wdsi/filesubmission)         |
|<span data-ttu-id="f695d-122">Alerte déclenchée par une utilisation légitime</span><span class="sxs-lookup"><span data-stu-id="f695d-122">Alert triggered by legitimate use</span></span> <br/><span data-ttu-id="f695d-123">Alerte inexacte</span><span class="sxs-lookup"><span data-stu-id="f695d-123">Inaccurate alert</span></span>    |[<span data-ttu-id="f695d-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="f695d-124">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)<br/> <span data-ttu-id="f695d-125">ou</span><span class="sxs-lookup"><span data-stu-id="f695d-125">or</span></span> <br/>[<span data-ttu-id="f695d-126">Détection de menaces avancées Azure</span><span class="sxs-lookup"><span data-stu-id="f695d-126">Azure Advanced Threat Detection</span></span>](https://docs.microsoft.com/azure/security/fundamentals/threat-detection)         |[<span data-ttu-id="f695d-127">Gérer les alertes dans le portail de sécurité des applications Cloud</span><span class="sxs-lookup"><span data-stu-id="f695d-127">Manage alerts in the Cloud App Security portal</span></span>](https://docs.microsoft.com/cloud-app-security/managing-alerts)         |


## <a name="next-steps"></a><span data-ttu-id="f695d-128">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f695d-128">Next steps</span></span>

- [<span data-ttu-id="f695d-129">Approuver ou refuser les actions liées à un examen et réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="f695d-129">Approve or reject actions related to automated investigation and response</span></span>](mtp-autoir-actions.md)
- <span data-ttu-id="f695d-130">[En savoir plus sur le centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="f695d-130">[Learn more about the Action center](mtp-action-center.md)</span></span>
- [<span data-ttu-id="f695d-131">Repérage proactive de menaces avec repérage avancé dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f695d-131">Proactively hunt for threats with advanced hunting in Microsoft Threat Protection</span></span>](advanced-hunting-overview.md)
