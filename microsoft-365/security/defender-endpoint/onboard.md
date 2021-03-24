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
ms.openlocfilehash: e2082929cf1fb7f4b55331cf62adcd9b936168d0
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51061077"
---
# <a name="configure-and-manage-microsoft-defender-for-endpoint-capabilities"></a><span data-ttu-id="f8b73-104">Configurer et gérer les fonctionnalités de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="f8b73-104">Configure and manage Microsoft Defender for Endpoint capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f8b73-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f8b73-105">**Applies to:**</span></span>
- [<span data-ttu-id="f8b73-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f8b73-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="f8b73-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f8b73-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f8b73-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f8b73-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f8b73-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f8b73-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="f8b73-110">Configurez et gérez toutes les fonctionnalités de Defender for Endpoint pour obtenir la meilleure protection de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8b73-110">Configure and manage all the Defender for Endpoint capabilities to get the best security protection for your organization.</span></span> 


## <a name="in-this-section"></a><span data-ttu-id="f8b73-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f8b73-111">In this section</span></span> 
<span data-ttu-id="f8b73-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f8b73-112">Topic</span></span> | <span data-ttu-id="f8b73-113">Description</span><span class="sxs-lookup"><span data-stu-id="f8b73-113">Description</span></span> 
:---|:---
[<span data-ttu-id="f8b73-114">Configurer les fonctionnalités de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="f8b73-114">Configure attack surface reduction capabilities</span></span>](configure-attack-surface-reduction.md) |  <span data-ttu-id="f8b73-115">En veillant à ce que les paramètres de configuration soient correctement définies et que des techniques d’atténuation des attaques soient appliquées, ces fonctionnalités peuvent résister aux attaques et à l’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f8b73-115">By ensuring configuration settings are properly set and exploit mitigation techniques are applied, these set of capabilities resist attacks and exploitation.</span></span> 
[<span data-ttu-id="f8b73-116">Configurer la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="f8b73-116">Configure next-generation protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) | <span data-ttu-id="f8b73-117">Configurez la protection nouvelle génération pour capturer tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="f8b73-117">Configure next-generation protection to catch all types of emerging threats.</span></span>
[<span data-ttu-id="f8b73-118">Configurer les fonctionnalités des experts microsoft en matière de menaces</span><span class="sxs-lookup"><span data-stu-id="f8b73-118">Configure Microsoft Threat Experts capabilities</span></span>](configure-microsoft-threat-experts.md) | <span data-ttu-id="f8b73-119">Configurez et gérez la façon dont vous souhaitez obtenir des informations sur les menaces de cybersécurité auprès d’experts microsoft en matière de menaces.</span><span class="sxs-lookup"><span data-stu-id="f8b73-119">Configure and manage how you would like to get cybersecurity threat intelligence from Microsoft Threat Experts.</span></span>
[<span data-ttu-id="f8b73-120">Configurer l’intégration de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f8b73-120">Configure Microsoft Threat Protection integration</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/threat-protection-integration)| <span data-ttu-id="f8b73-121">Configurez d’autres solutions qui s’intègrent à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="f8b73-121">Configure other solutions that integrate with Defender for Endpoint.</span></span>
[<span data-ttu-id="f8b73-122">Prise en charge de la gestion et de l’API</span><span class="sxs-lookup"><span data-stu-id="f8b73-122">Management and API support</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/management-apis)| <span data-ttu-id="f8b73-123">Tirez des alertes vers votre SIEM ou utilisez des API pour créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f8b73-123">Pull alerts to your SIEM or use APIs to create custom alerts.</span></span> <span data-ttu-id="f8b73-124">Créez et créez des rapports Power BI.</span><span class="sxs-lookup"><span data-stu-id="f8b73-124">Create and build Power BI reports.</span></span> 
[<span data-ttu-id="f8b73-125">Configurer les paramètres du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f8b73-125">Configure Microsoft Defender Security Center settings</span></span>](preferences-setup.md) |  <span data-ttu-id="f8b73-126">Configurez les paramètres relatifs au portail tels que les paramètres généraux, les fonctionnalités avancées, activez l’expérience d’aperçu, etc.</span><span class="sxs-lookup"><span data-stu-id="f8b73-126">Configure portal-related settings such as general settings, advanced features, enable the preview experience and others.</span></span>



