---
title: Configurer et gérer les fonctionnalités de Microsoft Defender pour les points de terminaison
ms.reviewer: ''
description: Configurer et gérer les fonctionnalités de Microsoft Defender pour les points de terminaison telles que la réduction de la surface d'attaque et la protection nouvelle génération
keywords: configurer, gérer, fonctionnalités, réduction de la surface d'attaque, protection nouvelle génération, contrôles de sécurité, détection et réponse des points de terminaison, examen et correction automatiques, contrôles de sécurité, contrôles
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 25b70f91824db2a6d05db5d3981dd50f4f2b477a
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934740"
---
# <a name="configure-and-manage-microsoft-defender-for-endpoint-capabilities"></a><span data-ttu-id="b9ae5-104">Configurer et gérer les fonctionnalités de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b9ae5-104">Configure and manage Microsoft Defender for Endpoint capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b9ae5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b9ae5-105">**Applies to:**</span></span>

- [<span data-ttu-id="b9ae5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b9ae5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b9ae5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b9ae5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b9ae5-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b9ae5-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b9ae5-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="b9ae5-110">Découvrez comment configurer et gérer les fonctionnalités de Defender for Endpoint pour obtenir la meilleure protection de sécurité pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-110">Learn how to configure and manage Defender for Endpoint features, to get the best security protection for your organization.</span></span>

<span data-ttu-id="b9ae5-111">Pour obtenir des conseils pratiques sur la connexion de nouveaux appareils dans votre organisation, voir Appareils intégrés [au service Microsoft Defender for Endpoint.](./onboard-configure.md)</span><span class="sxs-lookup"><span data-stu-id="b9ae5-111">For practical advice on connecting new devices in your organization, see [Onboard devices to the Microsoft Defender for Endpoint service](./onboard-configure.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b9ae5-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b9ae5-112">In this section</span></span>

<span data-ttu-id="b9ae5-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b9ae5-113">Topic</span></span> | <span data-ttu-id="b9ae5-114">Description</span><span class="sxs-lookup"><span data-stu-id="b9ae5-114">Description</span></span>
:---|:---
[<span data-ttu-id="b9ae5-115">Configurer les paramètres du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b9ae5-115">Configure Microsoft Defender Security Center settings</span></span>](preferences-setup.md) | <span data-ttu-id="b9ae5-116">Configurez les paramètres liés au portail tels que les paramètres généraux, les fonctionnalités avancées ou activez l'expérience d'aperçu.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-116">Configure portal-related settings such as general settings, advanced features, or enable the preview experience.</span></span>
[<span data-ttu-id="b9ae5-117">Configurer les fonctionnalités de réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="b9ae5-117">Configure attack surface reduction capabilities</span></span>](configure-attack-surface-reduction.md) | <span data-ttu-id="b9ae5-118">Configurez les fonctionnalités de réduction de la surface d'attaque pour vous assurer que les paramètres sont correctement appliqués et que les techniques d'atténuation des attaques sont définies.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-118">Configure attack surface reduction capabilities, to ensure that settings are properly applied, and exploit mitigation techniques are set.</span></span>
[<span data-ttu-id="b9ae5-119">Configurer la protection nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="b9ae5-119">Configure next-generation protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) | <span data-ttu-id="b9ae5-120">Configurez la protection nouvelle génération pour capturer tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-120">Configure next-generation protection to catch all types of emerging threats.</span></span>
[<span data-ttu-id="b9ae5-121">Configurer les fonctionnalités des experts microsoft en matière de menaces</span><span class="sxs-lookup"><span data-stu-id="b9ae5-121">Configure Microsoft Threat Experts capabilities</span></span>](configure-microsoft-threat-experts.md) | <span data-ttu-id="b9ae5-122">Configurez et gérez la veille contre les menaces de cybersécurité à partir d'experts microsoft en matière de menaces.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-122">Configure and manage cybersecurity threat intelligence from Microsoft Threat Experts.</span></span>
[<span data-ttu-id="b9ae5-123">Configurer l'intégration de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b9ae5-123">Configure Microsoft 365 Defender integration</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/threat-protection-integration) | <span data-ttu-id="b9ae5-124">Configurez d'autres solutions qui s'intègrent à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-124">Configure other solutions that integrate with Defender for Endpoint.</span></span>
[<span data-ttu-id="b9ae5-125">Prise en charge de la gestion et de l'API</span><span class="sxs-lookup"><span data-stu-id="b9ae5-125">Management and API support</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/management-apis) | <span data-ttu-id="b9ae5-126">Tirez des alertes vers votre siEM (Security Information and Event Management) ou utilisez des API pour créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-126">Pull alerts to your Security Information and Event Management (SIEM) or use APIs to create custom alerts.</span></span> <span data-ttu-id="b9ae5-127">Créez et créez des rapports Power BI.</span><span class="sxs-lookup"><span data-stu-id="b9ae5-127">Create and build Power BI reports.</span></span>
