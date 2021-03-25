---
title: Configurer et gérer les fonctionnalités de Microsoft Defender ATP
ms.reviewer: ''
description: Configurer et gérer les fonctionnalités de Microsoft Defender ATP telles que la réduction de la surface d’attaque et la protection nouvelle génération
keywords: configurer, gérer, fonctionnalités, réduction de la surface d’attaque, protection nouvelle génération, contrôles de sécurité, détection et réponse des points de terminaison, examen et correction automatiques, contrôles de sécurité, contrôles
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
ms.openlocfilehash: a0872de9774773c136bca6febd621daba5b2d7d3
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186376"
---
# <a name="configure-and-manage-microsoft-defender-for-endpoint-capabilities"></a><span data-ttu-id="b49ac-104">Configurer et gérer les fonctionnalités de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49ac-104">Configure and manage Microsoft Defender for Endpoint capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b49ac-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b49ac-105">**Applies to:**</span></span>
- [<span data-ttu-id="b49ac-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b49ac-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b49ac-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b49ac-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b49ac-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b49ac-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b49ac-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b49ac-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="b49ac-110">Configurez et gérez toutes les fonctionnalités de Defender for Endpoint pour obtenir la meilleure protection de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b49ac-110">Configure and manage all the Defender for Endpoint capabilities to get the best security protection for your organization.</span></span> 


## <a name="in-this-section"></a><span data-ttu-id="b49ac-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b49ac-111">In this section</span></span> 
<span data-ttu-id="b49ac-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b49ac-112">Topic</span></span> | <span data-ttu-id="b49ac-113">Description</span><span class="sxs-lookup"><span data-stu-id="b49ac-113">Description</span></span> 
:---|:---
[<span data-ttu-id="b49ac-114">Configurer les fonctionnalités de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="b49ac-114">Configure attack surface reduction capabilities</span></span>](configure-attack-surface-reduction.md) |  <span data-ttu-id="b49ac-115">En veillant à ce que les paramètres de configuration soient correctement définies et que des techniques d’atténuation des attaques soient appliquées, ces fonctionnalités peuvent résister aux attaques et à l’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b49ac-115">By ensuring configuration settings are properly set and exploit mitigation techniques are applied, these set of capabilities resist attacks and exploitation.</span></span> 
[<span data-ttu-id="b49ac-116">Configurer la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="b49ac-116">Configure next-generation protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) | <span data-ttu-id="b49ac-117">Configurez la protection nouvelle génération pour capturer tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="b49ac-117">Configure next-generation protection to catch all types of emerging threats.</span></span>
[<span data-ttu-id="b49ac-118">Configurer les fonctionnalités des experts microsoft en matière de menaces</span><span class="sxs-lookup"><span data-stu-id="b49ac-118">Configure Microsoft Threat Experts capabilities</span></span>](configure-microsoft-threat-experts.md) | <span data-ttu-id="b49ac-119">Configurez et gérez la façon dont vous souhaitez obtenir des informations sur les menaces de cybersécurité auprès d’experts microsoft en matière de menaces.</span><span class="sxs-lookup"><span data-stu-id="b49ac-119">Configure and manage how you would like to get cybersecurity threat intelligence from Microsoft Threat Experts.</span></span>
[<span data-ttu-id="b49ac-120">Configurer l’intégration de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="b49ac-120">Configure Microsoft Threat Protection integration</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/threat-protection-integration)| <span data-ttu-id="b49ac-121">Configurez d’autres solutions qui s’intègrent à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b49ac-121">Configure other solutions that integrate with Defender for Endpoint.</span></span>
[<span data-ttu-id="b49ac-122">Prise en charge de la gestion et de l’API</span><span class="sxs-lookup"><span data-stu-id="b49ac-122">Management and API support</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/management-apis)| <span data-ttu-id="b49ac-123">Tirez des alertes vers votre SIEM ou utilisez des API pour créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b49ac-123">Pull alerts to your SIEM or use APIs to create custom alerts.</span></span> <span data-ttu-id="b49ac-124">Créez et créez des rapports Power BI.</span><span class="sxs-lookup"><span data-stu-id="b49ac-124">Create and build Power BI reports.</span></span> 
[<span data-ttu-id="b49ac-125">Configurer les paramètres du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b49ac-125">Configure Microsoft Defender Security Center settings</span></span>](preferences-setup.md) |  <span data-ttu-id="b49ac-126">Configurez les paramètres relatifs au portail tels que les paramètres généraux, les fonctionnalités avancées, activez l’expérience d’aperçu, etc.</span><span class="sxs-lookup"><span data-stu-id="b49ac-126">Configure portal-related settings such as general settings, advanced features, enable the preview experience and others.</span></span>



