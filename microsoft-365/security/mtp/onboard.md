---
title: Configurer et gérer les fonctionnalités ATP de Microsoft Defender
ms.reviewer: ''
description: Configurer et gérer les fonctionnalités ATP de Microsoft Defender telles que la réduction de la surface d’attaque, la protection nouvelle génération et les contrôles de sécurité
keywords: configuration, gestion, fonctionnalités, réduction de la surface d’attaque, protection de la nouvelle génération, contrôles de sécurité, détection et réponse aux points de terminaison, recherche et correction automatiques, contrôles de sécurité, contrôles
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.openlocfilehash: 64c6e5f7eefad50aa59301de3fd46cae60d6876f
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48429430"
---
# <a name="configure-and-manage-microsoft-defender-atp-capabilities"></a><span data-ttu-id="319b0-104">Configurer et gérer les fonctionnalités ATP de Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="319b0-104">Configure and manage Microsoft Defender ATP capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="319b0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="319b0-105">**Applies to:**</span></span>

- [<span data-ttu-id="319b0-106">Microsoft Defender – Protection avancée contre les menaces (Microsoft Defender ATP)</span><span class="sxs-lookup"><span data-stu-id="319b0-106">Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP)</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2069559)

<span data-ttu-id="319b0-107">Configurez et Gérez toutes les fonctionnalités ATP de Microsoft Defender pour bénéficier de la meilleure protection de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="319b0-107">Configure and manage all the Microsoft Defender ATP capabilities to get the best security protection for your organization.</span></span> 


## <a name="in-this-section"></a><span data-ttu-id="319b0-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="319b0-108">In this section</span></span> 
<span data-ttu-id="319b0-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="319b0-109">Topic</span></span> | <span data-ttu-id="319b0-110">Description</span><span class="sxs-lookup"><span data-stu-id="319b0-110">Description</span></span> 
:---|:---
[<span data-ttu-id="319b0-111">Configurer les fonctionnalités de réduction de surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="319b0-111">Configure attack surface reduction capabilities</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-attack-surface-reduction) |  <span data-ttu-id="319b0-112">En veillant à ce que les paramètres de configuration soient correctement définis et que les techniques d’atténuation des risques soient appliquées, ces fonctionnalités permettent de résister aux attaques et aux exploitations.</span><span class="sxs-lookup"><span data-stu-id="319b0-112">By ensuring configuration settings are properly set and exploit mitigation techniques are applied, these set of capabilities resist attacks and exploitations.</span></span> 
[<span data-ttu-id="319b0-113">Configurer la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="319b0-113">Configure next generation protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/configure-windows-defender-antivirus-features) | <span data-ttu-id="319b0-114">Configurez la protection de nouvelle génération pour détecter tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="319b0-114">Configure next generation protection to catch all types of emerging threats.</span></span>
[<span data-ttu-id="319b0-115">Configurer les fonctionnalités de Microsoft Threat experts</span><span class="sxs-lookup"><span data-stu-id="319b0-115">Configure Microsoft Threat Experts capabilities</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-microsoft-threat-experts) | <span data-ttu-id="319b0-116">Configurez et gérez la manière dont vous aimeriez obtenir des informations sur les menaces Cybersecurity à partir de Microsoft Threat experts.</span><span class="sxs-lookup"><span data-stu-id="319b0-116">Configure and manage how you would like to get cybersecurity threat intelligence from Microsoft Threat Experts.</span></span>
[<span data-ttu-id="319b0-117">Configurer l’intégration de la protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="319b0-117">Configure Microsoft Threat Protection integration</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/threat-protection-integration)| <span data-ttu-id="319b0-118">Configurez d’autres solutions qui s’intègrent à Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="319b0-118">Configure other solutions that integrate with Microsoft Defender ATP.</span></span>
[<span data-ttu-id="319b0-119">Prise en charge de l’API et de la gestion</span><span class="sxs-lookup"><span data-stu-id="319b0-119">Management and API support</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/management-apis)| <span data-ttu-id="319b0-120">Attirez les alertes sur votre SIEM ou utilisez des API pour créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="319b0-120">Pull alerts to your SIEM or use APIs to create custom alerts.</span></span> <span data-ttu-id="319b0-121">Créez et générez des rapports Power BI.</span><span class="sxs-lookup"><span data-stu-id="319b0-121">Create and build Power BI reports.</span></span> 
[<span data-ttu-id="319b0-122">Configurer les paramètres du centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="319b0-122">Configure Microsoft Defender Security Center settings</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/preferences-setup) |  <span data-ttu-id="319b0-123">Configurez les paramètres liés au portail, tels que les paramètres généraux, les fonctionnalités avancées, l’expérience d’aperçu et autres.</span><span class="sxs-lookup"><span data-stu-id="319b0-123">Configure portal related settings such as general settings, advanced features, enable the preview experience and others.</span></span>



