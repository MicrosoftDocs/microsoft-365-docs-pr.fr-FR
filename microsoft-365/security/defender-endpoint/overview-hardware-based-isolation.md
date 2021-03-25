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
ms.openlocfilehash: 82841ccdb2a6ad09f43d0bf8d12cb54fe44d6dfe
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186904"
---
# <a name="hardware-based-isolation-in-windows-10"></a><span data-ttu-id="ed299-103">Isolation matérielle dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed299-103">Hardware-based isolation in Windows 10</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ed299-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ed299-104">**Applies to:**</span></span>
- [<span data-ttu-id="ed299-105">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ed299-105">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ed299-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ed299-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="ed299-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ed299-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ed299-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ed299-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="ed299-109">L’isolation matérielle permet de protéger l’intégrité du système dans Windows 10 et est intégrée à Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="ed299-109">Hardware-based isolation helps protect system integrity in Windows 10 and is integrated with Microsoft Defender for Endpoint.</span></span> 

| <span data-ttu-id="ed299-110">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="ed299-110">Feature</span></span> | <span data-ttu-id="ed299-111">Description</span><span class="sxs-lookup"><span data-stu-id="ed299-111">Description</span></span> |
|------------|-------------|
| [<span data-ttu-id="ed299-112">Windows Defender Application Guard</span><span class="sxs-lookup"><span data-stu-id="ed299-112">Windows Defender Application Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview.md) | <span data-ttu-id="ed299-113">Application Guard protège votre appareil contre les attaques avancées tout en vous conservant productif.</span><span class="sxs-lookup"><span data-stu-id="ed299-113">Application Guard protects your device from advanced attacks while keeping you productive.</span></span> <span data-ttu-id="ed299-114">À l’aide d’une approche d’isolation matérielle unique, l’objectif est d’isoler les sites web non confiance et les documents PDF à l’intérieur d’un conteneur léger séparé du système d’exploitation via l’hyperviseur Windows natif.</span><span class="sxs-lookup"><span data-stu-id="ed299-114">Using a unique hardware-based isolation approach, the goal is to isolate untrusted websites and PDF documents inside a lightweight container that is separated from the operating system via the native Windows Hypervisor.</span></span> <span data-ttu-id="ed299-115">Si un site non sécurisé ou un document PDF s’avère malveillant, il reste contenu dans le conteneur sécurisé d’Application Guard, en maintenant le PC de bureau protégé et l’attaquant à l’écart de vos données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ed299-115">If an untrusted site or PDF document turns out to be malicious, it still remains contained within Application Guard’s secure container, keeping the desktop PC protected and the attacker away from your enterprise data.</span></span> |
| [<span data-ttu-id="ed299-116">Windows Defender System Guard</span><span class="sxs-lookup"><span data-stu-id="ed299-116">Windows Defender System Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-system-guard/system-guard-how-hardware-based-root-of-trust-helps-protect-windows.md) | <span data-ttu-id="ed299-117">System Guard protège et maintient l’intégrité du système au démarrage et après son exécution, et valide l’intégrité du système à l’aide de l’attestation.</span><span class="sxs-lookup"><span data-stu-id="ed299-117">System Guard protects and maintains the integrity of the system as it starts and after it's running, and validates system integrity by using attestation.</span></span>  |

