---
title: Configurer la réduction de la surface d’attaque
description: Utilisez Microsoft Intune, Microsoft Endpoint Configuration Manager, les cmdlets PowerShell et la stratégie de groupe pour configurer la réduction de la surface d’attaque.
keywords: asr, réduction de la surface d’attaque, windows defender, microsoft defender, antivirus, av
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 6129fb889e2bd42f177c4e3be30f676854119f91
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166160"
---
# <a name="configure-attack-surface-reduction"></a><span data-ttu-id="6e5fd-104">Configurer la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e5fd-104">Configure attack surface reduction</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6e5fd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6e5fd-105">**Applies to:**</span></span>
- [<span data-ttu-id="6e5fd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6e5fd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6e5fd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6e5fd-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="6e5fd-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="6e5fd-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="6e5fd-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6e5fd-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="6e5fd-110">Vous pouvez configurer la réduction de la surface d’attaque à l’aide de nombreux outils, notamment :</span><span class="sxs-lookup"><span data-stu-id="6e5fd-110">You can configure attack surface reduction with many tools, including:</span></span>

* <span data-ttu-id="6e5fd-111">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="6e5fd-111">Microsoft Intune</span></span>
* <span data-ttu-id="6e5fd-112">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="6e5fd-112">Microsoft Endpoint Configuration Manager</span></span>
* <span data-ttu-id="6e5fd-113">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="6e5fd-113">Group Policy</span></span>
* <span data-ttu-id="6e5fd-114">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e5fd-114">PowerShell cmdlets</span></span>

<span data-ttu-id="6e5fd-115">Article</span><span class="sxs-lookup"><span data-stu-id="6e5fd-115">Article</span></span> | <span data-ttu-id="6e5fd-116">Description</span><span class="sxs-lookup"><span data-stu-id="6e5fd-116">Description</span></span>
-|-
[<span data-ttu-id="6e5fd-117">Activer l’isolation matérielle pour Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6e5fd-117">Enable hardware-based isolation for Microsoft Edge</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard) | <span data-ttu-id="6e5fd-118">Comment préparer et installer Application Guard, y compris la configuration matérielle et logicielle requise</span><span class="sxs-lookup"><span data-stu-id="6e5fd-118">How to prepare for and install Application Guard, including hardware and software requirements</span></span>
[<span data-ttu-id="6e5fd-119">Activer le contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="6e5fd-119">Enable application control</span></span>](/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control)|<span data-ttu-id="6e5fd-120">Comment contrôler les applications exécutés par les utilisateurs et protéger les processus en mode noyau</span><span class="sxs-lookup"><span data-stu-id="6e5fd-120">How to control applications run by users and protect kernel mode processes</span></span>
[<span data-ttu-id="6e5fd-121">Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="6e5fd-121">Exploit protection</span></span>](./enable-exploit-protection.md)|<span data-ttu-id="6e5fd-122">Comment appliquer automatiquement des techniques d’atténuation des attaques sur les processus du système d’exploitation et sur des applications individuelles</span><span class="sxs-lookup"><span data-stu-id="6e5fd-122">How to automatically apply exploit mitigation techniques on both operating system processes and on individual apps</span></span>
[<span data-ttu-id="6e5fd-123">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="6e5fd-123">Network protection</span></span>](./enable-network-protection.md)|<span data-ttu-id="6e5fd-124">Comment empêcher les utilisateurs d’utiliser des applications pour accéder à des domaines dangereux</span><span class="sxs-lookup"><span data-stu-id="6e5fd-124">How to prevent users from using any apps to access dangerous domains</span></span>
[<span data-ttu-id="6e5fd-125">Accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="6e5fd-125">Controlled folder access</span></span>](./enable-controlled-folders.md)|<span data-ttu-id="6e5fd-126">Comment protéger les données précieuses contre les applications malveillantes</span><span class="sxs-lookup"><span data-stu-id="6e5fd-126">How to protect valuable data from malicious apps</span></span>
[<span data-ttu-id="6e5fd-127">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e5fd-127">Attack surface reduction</span></span>](./enable-attack-surface-reduction.md)|<span data-ttu-id="6e5fd-128">Comment empêcher les actions et les applications qui sont généralement utilisées par des programmes malveillants à la recherche d’attaques</span><span class="sxs-lookup"><span data-stu-id="6e5fd-128">How to prevent actions and apps that are typically used by exploit-seeking malware</span></span>
[<span data-ttu-id="6e5fd-129">Pare-feu réseau</span><span class="sxs-lookup"><span data-stu-id="6e5fd-129">Network firewall</span></span>](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security-deployment-guide)|<span data-ttu-id="6e5fd-130">Comment protéger les appareils et les données sur un réseau</span><span class="sxs-lookup"><span data-stu-id="6e5fd-130">How to protect devices and data across a network</span></span>

