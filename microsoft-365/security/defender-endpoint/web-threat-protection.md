---
title: Protéger votre organisation contre les menaces web
description: Découvrez la protection web dans Microsoft Defender ATP et la façon dont elle peut protéger votre organisation.
keywords: protection web, protection contre les menaces web, navigation web, sécurité, hameçonnage, programmes malveillants, attaque, sites web, protection réseau, Edge, Internet Explorer, Chrome, Firefox, navigateur web
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 3376308988213b84bc7badb96ebacdf706d1ca5f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063633"
---
# <a name="protect-your-organization-against-web-threats"></a><span data-ttu-id="7507e-104">Protéger votre organisation contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="7507e-104">Protect your organization against web threats</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7507e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7507e-105">**Applies to:**</span></span>
- [<span data-ttu-id="7507e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7507e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="7507e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7507e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="7507e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7507e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="7507e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7507e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink&rtc=1)

<span data-ttu-id="7507e-110">La protection contre les menaces web fait partie de [la protection Web](web-protection-overview.md) dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="7507e-110">Web threat protection is part of [Web protection](web-protection-overview.md) in Defender for Endpoint.</span></span> <span data-ttu-id="7507e-111">Il utilise la [protection réseau](network-protection.md) pour sécuriser vos appareils contre les menaces web.</span><span class="sxs-lookup"><span data-stu-id="7507e-111">It uses [network protection](network-protection.md) to secure your devices against web threats.</span></span> <span data-ttu-id="7507e-112">Grâce à l’intégration à Microsoft Edge et aux navigateurs tiers populaires tels que Chrome et Firefox, la protection contre les menaces web arrête les menaces web sans proxy web et peut protéger les appareils lorsqu’ils sont absents ou locaux.</span><span class="sxs-lookup"><span data-stu-id="7507e-112">By integrating with Microsoft Edge and popular third-party browsers like Chrome and Firefox, web threat protection stops web threats without a web proxy and can protect devices while they are away or on premises.</span></span> <span data-ttu-id="7507e-113">La protection contre les menaces web arrête l’accès aux sites de hameçonnage, aux vecteurs de programmes malveillants, aux sites d’exploitation, aux sites non fiables ou à faible réputation, ainsi qu’aux sites que vous avez bloqués dans votre liste d’indicateurs [personnalisés.](manage-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="7507e-113">Web threat protection stops access to phishing sites, malware vectors, exploit sites, untrusted or low-reputation sites, as well as sites that you have blocked in your [custom indicator list](manage-indicators.md).</span></span>

>[!Note]
><span data-ttu-id="7507e-114">La réception de nouveaux indicateurs client sur les appareils peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="7507e-114">It can take up to an hour for devices to receive new customer indicators.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7507e-115">Prerequisites</span><span class="sxs-lookup"><span data-stu-id="7507e-115">Prerequisites</span></span>
<span data-ttu-id="7507e-116">La protection web utilise la protection réseau pour assurer la sécurité de la navigation web sur Microsoft Edge et les navigateurs web tiers.</span><span class="sxs-lookup"><span data-stu-id="7507e-116">Web protection uses network protection to provide web browsing security on Microsoft Edge and third-party web browsers.</span></span>

<span data-ttu-id="7507e-117">Pour activer la protection réseau sur vos appareils :</span><span class="sxs-lookup"><span data-stu-id="7507e-117">To turn on network protection on your devices:</span></span>
- <span data-ttu-id="7507e-118">Modifiez la ligne de base de sécurité Defender for Endpoint sous **Web & Network Protection** pour activer la protection réseau avant de la déployer ou de la redéployer.</span><span class="sxs-lookup"><span data-stu-id="7507e-118">Edit the Defender for Endpoint security baseline under **Web & Network Protection** to enable network protection before deploying or redeploying it.</span></span> [<span data-ttu-id="7507e-119">En savoir plus sur l’examen et l’affectation de la ligne de base de sécurité defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7507e-119">Learn about reviewing and assigning the Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md#review-and-assign-the-microsoft-defender-for-endpoint-security-baseline)
- <span data-ttu-id="7507e-120">Activer la protection réseau sur l’utilisation de la configuration de l’appareil Intune, de SCCM, de la stratégie de groupe ou de votre solution MDM.</span><span class="sxs-lookup"><span data-stu-id="7507e-120">Turn network protection on using Intune device configuration, SCCM, Group Policy, or your MDM solution.</span></span> [<span data-ttu-id="7507e-121">En savoir plus sur l’activation de la protection réseau</span><span class="sxs-lookup"><span data-stu-id="7507e-121">Read more about enabling network protection</span></span>](enable-network-protection.md)  

>[!Note]
><span data-ttu-id="7507e-122">Si vous définissez la protection réseau sur **Audit uniquement,** le blocage sera indisponible.</span><span class="sxs-lookup"><span data-stu-id="7507e-122">If you set network protection to **Audit only**, blocking will be unavailable.</span></span> <span data-ttu-id="7507e-123">En outre, vous pourrez détecter et enregistrer les tentatives d’accès aux sites web malveillants et indésirables uniquement sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7507e-123">Also, you will be able to detect and log attempts to access malicious and unwanted websites on Microsoft Edge only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7507e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7507e-124">Related topics</span></span>

- [<span data-ttu-id="7507e-125">Vue d’ensemble de la protection Web</span><span class="sxs-lookup"><span data-stu-id="7507e-125">Web protection overview</span></span>](web-protection-overview.md)
- [<span data-ttu-id="7507e-126">Protection contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="7507e-126">Web threat protection</span></span>](web-threat-protection.md)
- [<span data-ttu-id="7507e-127">Surveiller la sécurité web</span><span class="sxs-lookup"><span data-stu-id="7507e-127">Monitor web security</span></span>](web-protection-monitoring.md)
- [<span data-ttu-id="7507e-128">Répondre aux menaces web</span><span class="sxs-lookup"><span data-stu-id="7507e-128">Respond to web threats</span></span>](web-protection-response.md)
- [<span data-ttu-id="7507e-129">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="7507e-129">Network protection</span></span>](network-protection.md)