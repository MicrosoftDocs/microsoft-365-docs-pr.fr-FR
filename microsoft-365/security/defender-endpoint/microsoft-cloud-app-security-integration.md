---
title: Vue d’ensemble de l’intégration de Microsoft Cloud App Security
ms.reviewer: ''
description: Microsoft Defender pour le point de terminaison s’intègre à Cloud App Security en axant toutes les activités de mise en réseau des applications cloud.
keywords: cloud, application, réseau, visibilité, utilisation
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
ms.date: 10/18/2018
ms.technology: mde
ms.openlocfilehash: d756c738f9f61638a9e7424aa3fdf639f8f02f2a
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185598"
---
# <a name="microsoft-cloud-app-security-in-defender-for-endpoint-overview"></a><span data-ttu-id="9a09d-104">Vue d’ensemble de Microsoft Cloud App Security dans Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="9a09d-104">Microsoft Cloud App Security in Defender for Endpoint overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="9a09d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9a09d-105">**Applies to:**</span></span>
- [<span data-ttu-id="9a09d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9a09d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9a09d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9a09d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


> <span data-ttu-id="9a09d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9a09d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9a09d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9a09d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="9a09d-110">Microsoft Cloud App Security (Cloud App Security) est une solution complète qui offre une visibilité sur les applications et services cloud en vous permettant de contrôler et de limiter l’accès aux applications cloud, tout en appliquant des exigences de conformité sur les données stockées dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="9a09d-110">Microsoft Cloud App Security (Cloud App Security) is a comprehensive solution that gives visibility into cloud apps and services by allowing you to control and limit access to cloud apps, while enforcing compliance requirements on data stored in the cloud.</span></span> <span data-ttu-id="9a09d-111">Pour plus d’informations, [voir Cloud App Security.](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)</span><span class="sxs-lookup"><span data-stu-id="9a09d-111">For more information, see [Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security).</span></span>

>[!NOTE]
><span data-ttu-id="9a09d-112">Cette fonctionnalité est disponible avec une licence E5 pour [Enterprise Mobility + Security](https://www.microsoft.com/cloud-platform/enterprise-mobility-security) sur les appareils exécutant Windows 10 version 1809 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a09d-112">This feature is available with an E5 license for [Enterprise Mobility + Security](https://www.microsoft.com/cloud-platform/enterprise-mobility-security) on devices running Windows 10 version 1809 or later.</span></span>

## <a name="microsoft-defender-for-endpoint-and-cloud-app-security-integration"></a><span data-ttu-id="9a09d-113">Intégration de Microsoft Defender pour Endpoint et Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9a09d-113">Microsoft Defender for Endpoint and Cloud App Security integration</span></span> 

<span data-ttu-id="9a09d-114">La découverte de Cloud App Security s’appuie sur les journaux de trafic cloud qui lui sont transmis à partir du pare-feu d’entreprise et des serveurs proxy.</span><span class="sxs-lookup"><span data-stu-id="9a09d-114">Cloud App Security discovery relies on cloud traffic logs being forwarded to it from enterprise firewall and proxy servers.</span></span> <span data-ttu-id="9a09d-115">Microsoft Defender pour le point de terminaison s’intègre à Cloud App Security en collectant et en apportant toutes les activités de mise en réseau des applications cloud, offrant ainsi une visibilité renforcée de l’utilisation des applications cloud.</span><span class="sxs-lookup"><span data-stu-id="9a09d-115">Microsoft Defender for Endpoint integrates with Cloud App Security by collecting and forwarding all cloud app networking activities, providing unparalleled visibility to cloud app usage.</span></span> <span data-ttu-id="9a09d-116">La fonctionnalité d’analyse est intégrée à l’appareil, fournissant une couverture complète de l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="9a09d-116">The monitoring functionality is built into the device, providing complete coverage of network activity.</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4r4yQ]


<span data-ttu-id="9a09d-117">L’intégration apporte les améliorations majeures suivantes à la découverte de Cloud App Security existante :</span><span class="sxs-lookup"><span data-stu-id="9a09d-117">The integration provides the following major improvements to the existing Cloud App Security discovery:</span></span> 

- <span data-ttu-id="9a09d-118">Disponible partout : étant donné que l’activité réseau est collectée directement à partir du point de terminaison, elle est disponible partout où l’appareil se trouve, sur ou en dehors du réseau d’entreprise, car il ne dépend plus du trafic acheminé via le pare-feu d’entreprise ou les serveurs proxy.</span><span class="sxs-lookup"><span data-stu-id="9a09d-118">Available everywhere - Since the network activity is collected directly from the endpoint, it's available wherever the device is, on or off corporate network, as it's no longer depended on traffic routed through the enterprise firewall or proxy servers.</span></span> 

- <span data-ttu-id="9a09d-119">Ne fonctionne pas, aucune configuration n’est requise : le transport des journaux de trafic cloud vers Cloud App Security nécessite une configuration de pare-feu et de serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="9a09d-119">Works out of the box, no configuration required - Forwarding cloud traffic logs to Cloud App Security requires firewall and proxy server configuration.</span></span> <span data-ttu-id="9a09d-120">Avec l’intégration de Defender for Endpoint et Cloud App Security, aucune configuration n’est requise.</span><span class="sxs-lookup"><span data-stu-id="9a09d-120">With the Defender for Endpoint and Cloud App Security integration, there's no configuration required.</span></span> <span data-ttu-id="9a09d-121">Il vous suffit de l’allumer dans les paramètres du Centre de sécurité Microsoft Defender et vous êtes en bonne santé.</span><span class="sxs-lookup"><span data-stu-id="9a09d-121">Just switch it on in Microsoft Defender Security Center settings and you're good to go.</span></span> 

- <span data-ttu-id="9a09d-122">Contexte de périphérique : les journaux de trafic cloud n’ont pas de contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="9a09d-122">Device context - Cloud traffic logs lack device context.</span></span> <span data-ttu-id="9a09d-123">L’activité réseau de Defender for Endpoint est signalée avec le contexte de périphérique (quel appareil a accédé à l’application cloud), afin que vous compreniez exactement où (appareil) l’activité réseau a eu lieu, en plus de qui (utilisateur) l’a effectuée.</span><span class="sxs-lookup"><span data-stu-id="9a09d-123">Defender for Endpoint network activity is reported with the device context (which device accessed the cloud app), so you are able to understand exactly where (device) the network activity took place, in addition to who (user) performed it.</span></span> 

<span data-ttu-id="9a09d-124">Pour plus d’informations sur la découverte dans le cloud, voir [Working with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="9a09d-124">For more information about cloud discovery, see [Working with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>

## <a name="related-topic"></a><span data-ttu-id="9a09d-125">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="9a09d-125">Related topic</span></span>

- [<span data-ttu-id="9a09d-126">Configurer l’intégration de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9a09d-126">Configure Microsoft Cloud App Security integration</span></span>](microsoft-cloud-app-security-config.md)
