---
title: Protéger votre organisation contre les menaces web
description: Découvrez la protection web dans Microsoft Defender pour point de terminaison et la façon dont elle peut protéger votre organisation.
keywords: protection web, protection contre les menaces web, navigation web, sécurité, hameçonnage, programmes malveillants, attaque, sites web, protection réseau, Edge, Internet Explorer, Chrome, Firefox, navigateur web
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 0c42c05e318390741b94b6d7d1b5394fca961714
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51688944"
---
# <a name="protect-your-organization-against-web-threats"></a><span data-ttu-id="6482b-104">Protéger votre organisation contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="6482b-104">Protect your organization against web threats</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6482b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6482b-105">**Applies to:**</span></span>
- [<span data-ttu-id="6482b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6482b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6482b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6482b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="6482b-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6482b-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6482b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6482b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink&rtc=1)

<span data-ttu-id="6482b-110">La protection contre les menaces web fait partie de [la protection Web](web-protection-overview.md) dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="6482b-110">Web threat protection is part of [Web protection](web-protection-overview.md) in Defender for Endpoint.</span></span> <span data-ttu-id="6482b-111">Il utilise la [protection réseau](network-protection.md) pour sécuriser vos appareils contre les menaces web.</span><span class="sxs-lookup"><span data-stu-id="6482b-111">It uses [network protection](network-protection.md) to secure your devices against web threats.</span></span> <span data-ttu-id="6482b-112">Grâce à l'intégration à Microsoft Edge et aux navigateurs tiers populaires tels que Chrome et Firefox, la protection contre les menaces web arrête les menaces web sans proxy web et peut protéger les appareils lorsqu'ils sont absents ou locaux.</span><span class="sxs-lookup"><span data-stu-id="6482b-112">By integrating with Microsoft Edge and popular third-party browsers like Chrome and Firefox, web threat protection stops web threats without a web proxy and can protect devices while they are away or on premises.</span></span> <span data-ttu-id="6482b-113">La protection contre les menaces web arrête l'accès aux sites de hameçonnage, aux vecteurs de programmes malveillants, aux sites d'exploitation, aux sites non fiables ou à faible réputation, ainsi qu'aux sites que vous avez bloqués dans votre liste d'indicateurs [personnalisés.](manage-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="6482b-113">Web threat protection stops access to phishing sites, malware vectors, exploit sites, untrusted or low-reputation sites, as well as sites that you have blocked in your [custom indicator list](manage-indicators.md).</span></span>

>[!Note]
><span data-ttu-id="6482b-114">La réception de nouveaux indicateurs personnalisés peut prendre jusqu'à une heure.</span><span class="sxs-lookup"><span data-stu-id="6482b-114">It can take up to an hour for devices to receive new custom indicators.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6482b-115">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="6482b-115">Prerequisites</span></span>
<span data-ttu-id="6482b-116">La protection web utilise la protection réseau pour assurer la sécurité de navigation web sur Microsoft Edge et les navigateurs web tiers.</span><span class="sxs-lookup"><span data-stu-id="6482b-116">Web protection uses network protection to provide web browsing security on Microsoft Edge and third-party web browsers.</span></span>

<span data-ttu-id="6482b-117">Pour activer la protection réseau sur vos appareils :</span><span class="sxs-lookup"><span data-stu-id="6482b-117">To turn on network protection on your devices:</span></span>
- <span data-ttu-id="6482b-118">Modifiez la ligne de base de sécurité Defender for Endpoint sous **Web & Network Protection** pour activer la protection réseau avant de la déployer ou de la redéployer.</span><span class="sxs-lookup"><span data-stu-id="6482b-118">Edit the Defender for Endpoint security baseline under **Web & Network Protection** to enable network protection before deploying or redeploying it.</span></span> [<span data-ttu-id="6482b-119">En savoir plus sur l'examen et l'affectation de la ligne de base de sécurité defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6482b-119">Learn about reviewing and assigning the Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md#review-and-assign-the-microsoft-defender-for-endpoint-security-baseline)
- <span data-ttu-id="6482b-120">Activer la protection réseau sur l'utilisation de la configuration de l'appareil Intune, de SCCM, de la stratégie de groupe ou de votre solution MDM.</span><span class="sxs-lookup"><span data-stu-id="6482b-120">Turn network protection on using Intune device configuration, SCCM, Group Policy, or your MDM solution.</span></span> [<span data-ttu-id="6482b-121">En savoir plus sur l'activation de la protection réseau</span><span class="sxs-lookup"><span data-stu-id="6482b-121">Read more about enabling network protection</span></span>](enable-network-protection.md)  

>[!Note]
><span data-ttu-id="6482b-122">Si vous définissez la protection réseau sur **Audit uniquement,** le blocage sera indisponible.</span><span class="sxs-lookup"><span data-stu-id="6482b-122">If you set network protection to **Audit only**, blocking will be unavailable.</span></span> <span data-ttu-id="6482b-123">En outre, vous pourrez détecter et enregistrer les tentatives d'accès aux sites web malveillants et indésirables uniquement sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6482b-123">Also, you will be able to detect and log attempts to access malicious and unwanted websites on Microsoft Edge only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6482b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6482b-124">Related topics</span></span>

- [<span data-ttu-id="6482b-125">Vue d’ensemble de la protection web</span><span class="sxs-lookup"><span data-stu-id="6482b-125">Web protection overview</span></span>](web-protection-overview.md)
- [<span data-ttu-id="6482b-126">Protection contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="6482b-126">Web threat protection</span></span>](web-threat-protection.md)
- [<span data-ttu-id="6482b-127">Surveiller la sécurité web</span><span class="sxs-lookup"><span data-stu-id="6482b-127">Monitor web security</span></span>](web-protection-monitoring.md)
- [<span data-ttu-id="6482b-128">Répondre aux menaces web</span><span class="sxs-lookup"><span data-stu-id="6482b-128">Respond to web threats</span></span>](web-protection-response.md)
- [<span data-ttu-id="6482b-129">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="6482b-129">Network protection</span></span>](network-protection.md)
