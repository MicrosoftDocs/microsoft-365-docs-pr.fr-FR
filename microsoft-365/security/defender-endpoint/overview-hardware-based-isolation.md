---
title: Isolation matérielle (Windows 10)
ms.reviewer: ''
description: Découvrez comment l’isolation matérielle dans Windows 10 permet de lutter contre les programmes malveillants.
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.author: macapara
ms.date: 09/07/2018
ms.technology: mde
ms.openlocfilehash: b3babf858ac19e70119a2dc6a58b25359f1b05c1
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842985"
---
# <a name="hardware-based-isolation-in-windows-10"></a><span data-ttu-id="efabe-103">Isolation basée sur le matériel dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="efabe-103">Hardware-based isolation in Windows 10</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="efabe-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="efabe-104">**Applies to:**</span></span>
- [<span data-ttu-id="efabe-105">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="efabe-105">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="efabe-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="efabe-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="efabe-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="efabe-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="efabe-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="efabe-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="efabe-109">L’isolation matérielle permet de protéger l’intégrité du système Windows 10 et est intégrée à Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="efabe-109">Hardware-based isolation helps protect system integrity in Windows 10 and is integrated with Microsoft Defender for Endpoint.</span></span> 

| <span data-ttu-id="efabe-110">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="efabe-110">Feature</span></span> | <span data-ttu-id="efabe-111">Description</span><span class="sxs-lookup"><span data-stu-id="efabe-111">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="efabe-112">Windows Defender Application Guard</span><span class="sxs-lookup"><span data-stu-id="efabe-112">Windows Defender Application Guard</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview.md) | <span data-ttu-id="efabe-113">Application Guard protège votre appareil contre les attaques avancées tout en vous conservant productif.</span><span class="sxs-lookup"><span data-stu-id="efabe-113">Application Guard protects your device from advanced attacks while keeping you productive.</span></span> <span data-ttu-id="efabe-114">À l’aide d’une approche d’isolation matérielle unique, l’objectif est d’isoler les sites web non confiance et les documents PDF à l’intérieur d’un conteneur léger séparé du système d’exploitation via l’hyperviseur Windows natif.</span><span class="sxs-lookup"><span data-stu-id="efabe-114">Using a unique hardware-based isolation approach, the goal is to isolate untrusted websites and PDF documents inside a lightweight container that is separated from the operating system via the native Windows Hypervisor.</span></span> <span data-ttu-id="efabe-115">Si un site non sécurisé ou un document PDF s’avère malveillant, il reste contenu dans le conteneur sécurisé d’Application Guard, en maintenant le PC de bureau protégé et l’attaquant à l’écart de vos données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="efabe-115">If an untrusted site or PDF document turns out to be malicious, it still remains contained within Application Guard’s secure container, keeping the desktop PC protected and the attacker away from your enterprise data.</span></span> |
| [<span data-ttu-id="efabe-116">Windows Defender System Guard</span><span class="sxs-lookup"><span data-stu-id="efabe-116">Windows Defender System Guard</span></span>](/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows.md) | <span data-ttu-id="efabe-117">System Guard protège et maintient l’intégrité du système au démarrage et après son exécution, et valide l’intégrité du système à l’aide de l’attestation.</span><span class="sxs-lookup"><span data-stu-id="efabe-117">System Guard protects and maintains the integrity of the system as it starts and after it's running, and validates system integrity by using attestation.</span></span>  |

