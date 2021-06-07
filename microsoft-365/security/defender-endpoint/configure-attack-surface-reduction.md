---
title: Configurer les fonctionnalités de réduction de la surface d’attaque
description: Utilisez Microsoft Intune, Microsoft Endpoint Configuration Manager, les cmdlets PowerShell et la stratégie de groupe pour configurer la réduction de la surface d’attaque.
keywords: asr, réduction de la surface d’attaque, windows defender, microsoft defender, antivirus, av
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: deniseb
author: denisebmsft
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.date: 06/02/2021
ms.openlocfilehash: d2f984e21338e2f9a4ed579cde2d74339031d649
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770960"
---
# <a name="configure-attack-surface-reduction-capabilities"></a><span data-ttu-id="eb257-104">Configurer les fonctionnalités de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="eb257-104">Configure attack surface reduction capabilities</span></span>

<span data-ttu-id="eb257-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="eb257-105">**Applies to:**</span></span>
- [<span data-ttu-id="eb257-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="eb257-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="eb257-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="eb257-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> <span data-ttu-id="eb257-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="eb257-108">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="eb257-109">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="eb257-109">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink).</span></span>

<span data-ttu-id="eb257-110">Defender pour le point de terminaison inclut plusieurs fonctionnalités de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="eb257-110">Defender for Endpoint includes several attack surface reduction capabilities.</span></span> <span data-ttu-id="eb257-111">Pour plus d’informations, voir [Vue d’ensemble des fonctionnalités de réduction de la surface d’attaque.](overview-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="eb257-111">To learn more, see [Overview of attack surface reduction capabilities](overview-attack-surface-reduction.md).</span></span> <span data-ttu-id="eb257-112">Pour configurer la réduction de la surface d’attaque dans votre environnement, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb257-112">To configure attack surface reduction in your environment, follow these steps:</span></span> 

1. <span data-ttu-id="eb257-113">[Activer l’isolation matérielle pour Microsoft Edge](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard).</span><span class="sxs-lookup"><span data-stu-id="eb257-113">[Enable hardware-based isolation for Microsoft Edge](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard).</span></span>

2. <span data-ttu-id="eb257-114">Activer le contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="eb257-114">Enable application control.</span></span> 

   1. <span data-ttu-id="eb257-115">Passer en revue les stratégies de base Windows.</span><span class="sxs-lookup"><span data-stu-id="eb257-115">Review base policies in Windows.</span></span> <span data-ttu-id="eb257-116">Voir des [exemples de stratégies de base.](/windows/security/threat-protection/windows-defender-application-control/example-wdac-base-policies)</span><span class="sxs-lookup"><span data-stu-id="eb257-116">See [example base policies](/windows/security/threat-protection/windows-defender-application-control/example-wdac-base-policies).</span></span>
   2. <span data-ttu-id="eb257-117">Voir le [guide de conception des contrôles d’application.](/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-design-guide)</span><span class="sxs-lookup"><span data-stu-id="eb257-117">See the [application control design guide](/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-design-guide).</span></span>
   3. <span data-ttu-id="eb257-118">Reportez-vous au [guide de conception du contrôle d’application.](/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-deployment-guide)</span><span class="sxs-lookup"><span data-stu-id="eb257-118">Refer to the [application control design guide](/windows/security/threat-protection/windows-defender-application-control/windows-defender-application-control-deployment-guide).</span></span>

3. <span data-ttu-id="eb257-119">[Activer l’accès contrôlé aux dossiers.](enable-controlled-folders.md)</span><span class="sxs-lookup"><span data-stu-id="eb257-119">[Enable controlled folder access](enable-controlled-folders.md).</span></span>

4. <span data-ttu-id="eb257-120">[Activer la protection du réseau.](enable-network-protection.md)</span><span class="sxs-lookup"><span data-stu-id="eb257-120">[Turn on Network protection](enable-network-protection.md).</span></span>

5. <span data-ttu-id="eb257-121">[Activer Exploit Protection](enable-exploit-protection.md).</span><span class="sxs-lookup"><span data-stu-id="eb257-121">[Enable exploit protection](enable-exploit-protection.md).</span></span>

6. <span data-ttu-id="eb257-122">[Configurer les règles de réduction de la surface d’attaque.](enable-attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="eb257-122">[Configure attack surface reduction rules](enable-attack-surface-reduction.md).</span></span>

7. <span data-ttu-id="eb257-123">Configurer votre pare-feu réseau.</span><span class="sxs-lookup"><span data-stu-id="eb257-123">Set up your network firewall.</span></span>

   1. <span data-ttu-id="eb257-124">Obtenez une vue [d’ensemble Pare-feu Windows Defender avec une sécurité avancée.](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)</span><span class="sxs-lookup"><span data-stu-id="eb257-124">Get an overview of [Windows Defender Firewall with advanced security](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span>
   2. <span data-ttu-id="eb257-125">Utilisez le [guide Pare-feu Windows Defender de conception](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security-design-guide) pour déterminer la façon dont vous souhaitez concevoir vos stratégies de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="eb257-125">Use the [Windows Defender Firewall design guide](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security-design-guide) to decide how you want to design your firewall policies.</span></span>
   3. <span data-ttu-id="eb257-126">Utilisez le [guide Pare-feu Windows Defender de déploiement](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security-deployment-guide) pour configurer le pare-feu de votre organisation avec une sécurité avancée.</span><span class="sxs-lookup"><span data-stu-id="eb257-126">Use the [Windows Defender Firewall deployment guide](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security-deployment-guide) to set up your organization's firewall with advanced security.</span></span> 

> [!TIP]
> <span data-ttu-id="eb257-127">Dans la plupart des cas, lorsque vous configurez des fonctionnalités de réduction de la surface d’attaque, vous pouvez choisir parmi plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="eb257-127">In most cases, when you configure attack surface reduction capabilities, you can choose from among several methods:</span></span>
> - <span data-ttu-id="eb257-128">Microsoft Endpoint Manager (qui inclut désormais Microsoft Intune et Microsoft Endpoint Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="eb257-128">Microsoft Endpoint Manager (which now includes Microsoft Intune and Microsoft Endpoint Configuration Manager)</span></span>
> - <span data-ttu-id="eb257-129">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="eb257-129">Group Policy</span></span>
> - <span data-ttu-id="eb257-130">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="eb257-130">PowerShell cmdlets</span></span>
