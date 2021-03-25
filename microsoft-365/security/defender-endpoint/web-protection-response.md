---
title: Répondre aux menaces web dans Microsoft Defender ATP
description: Répondre aux alertes liées aux sites web malveillants et indésirables. Comprendre comment la protection contre les menaces web informe les utilisateurs finaux via leurs navigateurs web et les notifications Windows
keywords: protection web, protection contre les menaces web, navigation web, alertes, réponse, sécurité, hameçonnage, programme malveillant, attaque, sites web, protection réseau, Edge, Internet Explorer, Chrome, Firefox, navigateur web, notifications, utilisateurs finaux, notifications Windows, page de blocage,
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
ms.openlocfilehash: a9f3873db4f85cec3f5f1a400dcfb7930c6a4faa
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187540"
---
# <a name="respond-to-web-threats"></a><span data-ttu-id="880a4-105">Répondre aux menaces web</span><span class="sxs-lookup"><span data-stu-id="880a4-105">Respond to web threats</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="880a4-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="880a4-106">**Applies to:**</span></span>
- [<span data-ttu-id="880a4-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="880a4-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="880a4-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="880a4-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="880a4-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="880a4-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="880a4-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="880a4-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink&rtc=1)

<span data-ttu-id="880a4-111">La protection web dans Microsoft Defender pour le point de terminaison vous permet d’examiner et de répondre efficacement aux alertes liées aux sites web malveillants et aux sites web dans votre liste d’indicateurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="880a4-111">Web protection in Microsoft Defender for Endpoint lets you efficiently investigate and respond to alerts related to malicious websites and websites in your custom indicator list.</span></span>

## <a name="view-web-threat-alerts"></a><span data-ttu-id="880a4-112">Afficher les alertes de menaces web</span><span class="sxs-lookup"><span data-stu-id="880a4-112">View web threat alerts</span></span>
<span data-ttu-id="880a4-113">Microsoft Defender pour le point de terminaison génère les [alertes suivantes](manage-alerts.md) pour les activités web malveillantes ou suspectes :</span><span class="sxs-lookup"><span data-stu-id="880a4-113">Microsoft Defender for Endpoint generates the following [alerts](manage-alerts.md) for malicious or suspicious web activity:</span></span>
- <span data-ttu-id="880a4-114">**Connexion suspecte bloquée** par la protection réseau : cette alerte est générée lorsqu’une  tentative d’accès à un site web malveillant ou à un site web dans votre liste d’indicateurs personnalisés est arrêtée par la protection réseau en *mode* blocage</span><span class="sxs-lookup"><span data-stu-id="880a4-114">**Suspicious connection blocked by network protection** — this alert is generated when an attempt to access a malicious website or a website in your custom indicator list is *stopped* by network protection in *block* mode</span></span>
- <span data-ttu-id="880a4-115">**Connexion suspecte** détectée par la protection réseau : cette alerte est générée lorsqu’une tentative d’accès à un site web malveillant ou à un site web dans votre liste d’indicateurs personnalisés est détectée par la protection réseau en mode *audit* uniquement</span><span class="sxs-lookup"><span data-stu-id="880a4-115">**Suspicious connection detected by network protection** — this alert is generated when an attempt to access a malicious website or a website in your custom indicator list is detected by network protection in *audit only* mode</span></span>

<span data-ttu-id="880a4-116">Chaque alerte fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="880a4-116">Each alert provides the following information:</span></span> 
- <span data-ttu-id="880a4-117">Appareil qui a tenté d’accéder au site web bloqué</span><span class="sxs-lookup"><span data-stu-id="880a4-117">Device that attempted to access the blocked website</span></span>
- <span data-ttu-id="880a4-118">Application ou programme utilisé pour envoyer la demande web</span><span class="sxs-lookup"><span data-stu-id="880a4-118">Application or program used to send the web request</span></span>
- <span data-ttu-id="880a4-119">URL ou URL malveillante dans la liste des indicateurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="880a4-119">Malicious URL or URL in the custom indicator list</span></span>
- <span data-ttu-id="880a4-120">Actions recommandées pour les répondeurs</span><span class="sxs-lookup"><span data-stu-id="880a4-120">Recommended actions for responders</span></span>

![Image d’une alerte liée à la protection contre les menaces web](images/wtp-alert.png)

>[!Note]
><span data-ttu-id="880a4-122">Pour réduire le volume d’alertes, Microsoft Defender pour point de terminaison consolide les détections de menaces web pour le même domaine sur le même appareil chaque jour en une seule alerte.</span><span class="sxs-lookup"><span data-stu-id="880a4-122">To reduce the volume of alerts, Microsoft Defender for Endpoint consolidates web threat detections for the same domain on the same device each day to a single alert.</span></span> <span data-ttu-id="880a4-123">Une seule alerte est générée et comptabilisée dans le rapport [de protection web.](web-protection-monitoring.md)</span><span class="sxs-lookup"><span data-stu-id="880a4-123">Only one alert is generated and counted into the [web protection report](web-protection-monitoring.md).</span></span>

## <a name="inspect-website-details"></a><span data-ttu-id="880a4-124">Inspecter les détails du site web</span><span class="sxs-lookup"><span data-stu-id="880a4-124">Inspect website details</span></span>
<span data-ttu-id="880a4-125">Vous pouvez approfondir l’analyse en sélectionnant l’URL ou le domaine du site web dans l’alerte.</span><span class="sxs-lookup"><span data-stu-id="880a4-125">You can dive deeper by selecting the URL or domain of the website in the alert.</span></span> <span data-ttu-id="880a4-126">Une page sur cette URL ou ce domaine particulier s’ouvre avec différentes informations, notamment :</span><span class="sxs-lookup"><span data-stu-id="880a4-126">This opens a page about that particular URL or domain with various information, including:</span></span>
- <span data-ttu-id="880a4-127">Appareils qui ont tenté d’accéder au site web</span><span class="sxs-lookup"><span data-stu-id="880a4-127">Devices that attempted to access website</span></span>
- <span data-ttu-id="880a4-128">Incidents et alertes liés au site web</span><span class="sxs-lookup"><span data-stu-id="880a4-128">Incidents and alerts related to the website</span></span>
- <span data-ttu-id="880a4-129">Fréquence d’utilisation du site web dans les événements de votre organisation</span><span class="sxs-lookup"><span data-stu-id="880a4-129">How frequent the website was seen in events in your organization</span></span>

    ![Image de la page de détails d’entité de domaine ou d’URL](images/wtp-website-details.png)

[<span data-ttu-id="880a4-131">En savoir plus sur les pages d’URL ou d’entité de domaine</span><span class="sxs-lookup"><span data-stu-id="880a4-131">Learn more about URL or domain entity pages</span></span>](investigate-domain.md)

## <a name="inspect-the-device"></a><span data-ttu-id="880a4-132">Inspecter l’appareil</span><span class="sxs-lookup"><span data-stu-id="880a4-132">Inspect the device</span></span>
<span data-ttu-id="880a4-133">Vous pouvez également vérifier l’appareil qui a tenté d’accéder à une URL bloquée.</span><span class="sxs-lookup"><span data-stu-id="880a4-133">You can also check the device that attempted to access a blocked URL.</span></span> <span data-ttu-id="880a4-134">La sélection du nom de l’appareil sur la page d’alerte ouvre une page avec des informations complètes sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="880a4-134">Selecting the name of the device on the alert page opens a page with comprehensive information about the device.</span></span>

[<span data-ttu-id="880a4-135">En savoir plus sur les pages d’entité d’appareil</span><span class="sxs-lookup"><span data-stu-id="880a4-135">Learn more about device entity pages</span></span>](investigate-machines.md)

## <a name="web-browser-and-windows-notifications-for-end-users"></a><span data-ttu-id="880a4-136">Navigateur web et notifications Windows pour les utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="880a4-136">Web browser and Windows notifications for end users</span></span>

<span data-ttu-id="880a4-137">Avec la protection web dans Microsoft Defender pour point de terminaison, vos utilisateurs finaux ne pourront pas visiter des sites web malveillants ou indésirables à l’aide de Microsoft Edge ou d’autres navigateurs.</span><span class="sxs-lookup"><span data-stu-id="880a4-137">With web protection in Microsoft Defender for Endpoint, your end users will be prevented from visiting malicious or unwanted websites using Microsoft Edge or other browsers.</span></span> <span data-ttu-id="880a4-138">Étant donné que le blocage est effectué par la [protection](network-protection.md)réseau, une erreur générique s’est produite à partir du navigateur web.</span><span class="sxs-lookup"><span data-stu-id="880a4-138">Because blocking is performed by [network protection](network-protection.md), they will see a generic error from the web browser.</span></span> <span data-ttu-id="880a4-139">Ils voient également une notification de Windows.</span><span class="sxs-lookup"><span data-stu-id="880a4-139">They will also see a notification from Windows.</span></span>

<span data-ttu-id="880a4-140">![Image de Microsoft Edge montrant une erreur 403 et la menace web de notification Windows ](images/wtp-browser-blocking-page.png)
 *bloquée sur Microsoft Edge*</span><span class="sxs-lookup"><span data-stu-id="880a4-140">![Image of Microsoft Edge showing a 403 error and the Windows notification](images/wtp-browser-blocking-page.png)
*Web threat blocked on Microsoft Edge*</span></span>

<span data-ttu-id="880a4-141">![Image du navigateur web Chrome affichant un avertissement de connexion sécurisée et la menace web de notification Windows ](images/wtp-chrome-browser-blocking-page.png)
 *bloquée sur Chrome*</span><span class="sxs-lookup"><span data-stu-id="880a4-141">![Image of Chrome web browser showing a secure connection warning and the Windows notification](images/wtp-chrome-browser-blocking-page.png)
*Web threat blocked on Chrome*</span></span>

## <a name="related-topics"></a><span data-ttu-id="880a4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="880a4-142">Related topics</span></span>
- [<span data-ttu-id="880a4-143">Vue d’ensemble de la protection Web</span><span class="sxs-lookup"><span data-stu-id="880a4-143">Web protection overview</span></span>](web-protection-overview.md)
- [<span data-ttu-id="880a4-144">Filtrage de contenu Web</span><span class="sxs-lookup"><span data-stu-id="880a4-144">Web content filtering</span></span>](web-content-filtering.md)
- [<span data-ttu-id="880a4-145">Protection contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="880a4-145">Web threat protection</span></span>](web-threat-protection.md)
- [<span data-ttu-id="880a4-146">Surveiller la sécurité web</span><span class="sxs-lookup"><span data-stu-id="880a4-146">Monitor web security</span></span>](web-protection-monitoring.md)
