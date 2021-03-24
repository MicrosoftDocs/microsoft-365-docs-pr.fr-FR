---
title: Surveillance de la sécurité de navigation web dans Microsoft Defender ATP
description: Utiliser la protection web dans Microsoft Defender ATP pour surveiller la sécurité de navigation web
keywords: protection web, protection contre les menaces web, navigation web, surveillance, rapports, cartes, liste de domaines, sécurité, hameçonnage, programme malveillant, attaque, sites web, protection réseau, Edge, Internet Explorer, Chrome, Firefox, navigateur web
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
ms.openlocfilehash: 5d5cb89bccb0d7ea0fa4891c3b5b0d11a7244cf8
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063705"
---
# <a name="monitor-web-browsing-security"></a><span data-ttu-id="cf4c8-104">Surveiller la sécurité de navigation web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-104">Monitor web browsing security</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="cf4c8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cf4c8-105">**Applies to:**</span></span>
- [<span data-ttu-id="cf4c8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cf4c8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="cf4c8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cf4c8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="cf4c8-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="cf4c8-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="cf4c8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-main-abovefoldlink&rtc=1)

<span data-ttu-id="cf4c8-110">La protection Web vous permet de surveiller la sécurité de navigation web de votre organisation via des rapports sous Rapports > **protection Web** dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-110">Web protection lets you monitor your organization’s web browsing security through reports under **Reports > Web protection** in the Microsoft Defender Security Center.</span></span> <span data-ttu-id="cf4c8-111">Le rapport contient des cartes qui fournissent des statistiques sur la détection des menaces web.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-111">The report contains cards that provide web threat detection statistics.</span></span>

- <span data-ttu-id="cf4c8-112">Détections de protection contre les **menaces web** au fil du temps : cette carte tendance affiche le nombre de menaces web détectées par type au cours de la période sélectionnée (30 derniers jours, 3 derniers mois, 6 derniers mois)</span><span class="sxs-lookup"><span data-stu-id="cf4c8-112">**Web threat protection detections over time** - this trending card displays the number of web threats detected by type during the selected time period (Last 30 days, Last 3 months, Last 6 months)</span></span>
 
    ![Image de la carte montrant les détections de protection contre les menaces web au fil du temps](images/wtp-blocks-over-time.png)

- <span data-ttu-id="cf4c8-114">**Résumé de la protection** contre les menaces web : cette carte affiche le nombre total de détections de menaces web au cours des 30 derniers jours, montrant la répartition entre les différents types de menaces web.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-114">**Web threat protection summary** - this card displays the total web threat detections in the past 30 days, showing distribution across the different types of web threats.</span></span> <span data-ttu-id="cf4c8-115">La sélection d’une tranche ouvre la liste des domaines qui ont été trouvés avec des sites web malveillants ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-115">Selecting a slice opens the list of the domains that were found with malicious or unwanted websites.</span></span>

    ![Image de la carte montrant le résumé de la protection contre les menaces web](images/wtp-summary.png)

>[!Note]
><span data-ttu-id="cf4c8-117">La réflexion d’un bloc dans les cartes ou la liste de domaines peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-117">It can take up to 12 hours before a block is reflected in the cards or the domain list.</span></span>

## <a name="types-of-web-threats"></a><span data-ttu-id="cf4c8-118">Types de menaces web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-118">Types of web threats</span></span>

<span data-ttu-id="cf4c8-119">La protection web classe les sites web malveillants et indésirables comme :</span><span class="sxs-lookup"><span data-stu-id="cf4c8-119">Web protection categorizes malicious and unwanted websites as:</span></span>

- <span data-ttu-id="cf4c8-120">**Hameçonnage :** sites web qui contiennent des formulaires web usurpés et d’autres mécanismes de hameçonnage conçus pour leurre les utilisateurs à divulguer des informations d’identification et d’autres informations sensibles</span><span class="sxs-lookup"><span data-stu-id="cf4c8-120">**Phishing** - websites that contain spoofed web forms and other phishing mechanisms designed to trick users into divulging credentials and other sensitive information</span></span>
- <span data-ttu-id="cf4c8-121">**Malveillant :** sites web qui hébergent des programmes malveillants et du code d’exploitation</span><span class="sxs-lookup"><span data-stu-id="cf4c8-121">**Malicious** - websites that host malware and exploit code</span></span>
- <span data-ttu-id="cf4c8-122">**Indicateur personnalisé** : sites web dont vous avez ajouté les URL ou les domaines à votre liste d’indicateurs personnalisés [pour](manage-indicators.md) le blocage</span><span class="sxs-lookup"><span data-stu-id="cf4c8-122">**Custom indicator** - websites whose URLs or domains you've added to your [custom indicator list](manage-indicators.md) for blocking</span></span>

## <a name="view-the-domain-list"></a><span data-ttu-id="cf4c8-123">Afficher la liste des domaines</span><span class="sxs-lookup"><span data-stu-id="cf4c8-123">View the domain list</span></span>

<span data-ttu-id="cf4c8-124">Sélectionnez une catégorie de menaces web spécifique dans la carte **récapitulative de la protection web** contre les menaces pour ouvrir la page **Domaines.**</span><span class="sxs-lookup"><span data-stu-id="cf4c8-124">Select a specific web threat category in the **Web threat protection summary** card to open the **Domains** page.</span></span> <span data-ttu-id="cf4c8-125">Cette page affiche la liste des domaines de cette catégorie de menaces.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-125">This page displays the list of the domains under that threat category.</span></span> <span data-ttu-id="cf4c8-126">La page fournit les informations suivantes pour chaque domaine :</span><span class="sxs-lookup"><span data-stu-id="cf4c8-126">The page provides the following information for each domain:</span></span>

- <span data-ttu-id="cf4c8-127">**Nombre d’accès** : nombre de demandes d’URL dans le domaine</span><span class="sxs-lookup"><span data-stu-id="cf4c8-127">**Access count** - number of requests for URLs in the domain</span></span>
- <span data-ttu-id="cf4c8-128">**Blocs :** nombre de fois que les demandes ont été bloquées</span><span class="sxs-lookup"><span data-stu-id="cf4c8-128">**Blocks** - number of times requests were blocked</span></span>
- <span data-ttu-id="cf4c8-129">**Tendance d’accès** : changement du nombre de tentatives d’accès</span><span class="sxs-lookup"><span data-stu-id="cf4c8-129">**Access trend** - change in number of access attempts</span></span>
- <span data-ttu-id="cf4c8-130">**Catégorie de menace** : type de menace web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-130">**Threat category** - type of web threat</span></span>
- <span data-ttu-id="cf4c8-131">**Appareils** : nombre d’appareils avec tentatives d’accès</span><span class="sxs-lookup"><span data-stu-id="cf4c8-131">**Devices** - number of devices with access attempts</span></span>

<span data-ttu-id="cf4c8-132">Sélectionnez un domaine pour afficher la liste des périphériques qui ont tenté d’accéder aux URL de ce domaine et la liste des URL.</span><span class="sxs-lookup"><span data-stu-id="cf4c8-132">Select a domain to view the list of devices that have attempted to access URLs in that domain and the list of URLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf4c8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf4c8-133">Related topics</span></span>

- [<span data-ttu-id="cf4c8-134">Vue d’ensemble de la protection Web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-134">Web protection overview</span></span>](web-protection-overview.md)
- [<span data-ttu-id="cf4c8-135">Filtrage de contenu Web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-135">Web content filtering</span></span>](web-content-filtering.md)
- [<span data-ttu-id="cf4c8-136">Protection contre les menaces web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-136">Web threat protection</span></span>](web-threat-protection.md)
- [<span data-ttu-id="cf4c8-137">Répondre aux menaces web</span><span class="sxs-lookup"><span data-stu-id="cf4c8-137">Respond to web threats</span></span>](web-protection-response.md)
