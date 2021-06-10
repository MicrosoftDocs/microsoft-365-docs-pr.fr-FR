---
title: 'Rapport sur les appareils vulnérables : Gestion des menaces et des vulnérabilités'
description: Rapport présentant les tendances des appareils vulnérables et les statistiques actuelles. L’objectif est que vous compreniez le bruit et l’étendue de l’exposition de votre appareil.
keywords: Microsoft Defender pour les appareils vulnérables endpoint-tvm, Microsoft Defender pour le point de terminaison, tvm, réduire les menaces & exposition aux vulnérabilités, réduire les menaces et les vulnérabilités, surveiller la configuration de la sécurité
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 355561936642b1fa38228bfa07ad59269c48d817
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245479"
---
# <a name="vulnerable-devices-report---threat-and-vulnerability-management"></a><span data-ttu-id="12741-105">Rapport sur les appareils vulnérables : Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="12741-105">Vulnerable devices report - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="12741-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="12741-106">**Applies to:**</span></span>

- [<span data-ttu-id="12741-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="12741-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="12741-108">Menaces et gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="12741-108">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="12741-109">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="12741-109">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="12741-110">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="12741-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="12741-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="12741-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="12741-112">Le rapport présente des graphiques et des graphiques à barres avec des tendances d’appareils vulnérables et des statistiques actuelles.</span><span class="sxs-lookup"><span data-stu-id="12741-112">The report shows graphs and bar charts with vulnerable device trends and current statistics.</span></span> <span data-ttu-id="12741-113">L’objectif est que vous compreniez le bruit et l’étendue de l’exposition de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="12741-113">The goal is for you to understand the breath and scope of your device exposure.</span></span>

<span data-ttu-id="12741-114">Accédez au rapport dans le Centre de sécurité Microsoft Defender en accédant à **Rapports > appareils vulnérables**</span><span class="sxs-lookup"><span data-stu-id="12741-114">Access the report in the Microsoft Defender Security Center by going to **Reports > Vulnerable devices**</span></span>

<span data-ttu-id="12741-115">Il existe deux colonnes :</span><span class="sxs-lookup"><span data-stu-id="12741-115">There are two columns:</span></span>

- <span data-ttu-id="12741-116">Tendances (au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="12741-116">Trends (over time).</span></span> <span data-ttu-id="12741-117">Peut afficher les 30 derniers jours, 3 mois, 6 mois ou une plage de dates personnalisée.</span><span class="sxs-lookup"><span data-stu-id="12741-117">Can show the past 30 days, 3 months, 6 months, or a custom date range.</span></span>
- <span data-ttu-id="12741-118">Aujourd’hui (informations actuelles)</span><span class="sxs-lookup"><span data-stu-id="12741-118">Today (current information)</span></span>

<span data-ttu-id="12741-119">**Filtre :** vous pouvez filtrer les données par niveaux de gravité de vulnérabilité, disponibilité d’exploit, âge de vulnérabilité, plateforme du système d’exploitation, version Windows 10 ou groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="12741-119">**Filter**: You can filter the data by vulnerability severity levels, exploit availability, vulnerability age, operating system platform, Windows 10 version, or device group.</span></span>

<span data-ttu-id="12741-120">**Exploration :** s’il existe un aperçu que vous souhaitez explorer plus en détail, sélectionnez le graphique à barres approprié pour afficher une liste filtrée d’appareils dans la page d’inventaire des appareils.</span><span class="sxs-lookup"><span data-stu-id="12741-120">**Drill down**: If there is an insight you want to explore further, select the relevant bar chart to view a filtered list of devices in the Device inventory page.</span></span> <span data-ttu-id="12741-121">À partir de là, vous pouvez exporter la liste.</span><span class="sxs-lookup"><span data-stu-id="12741-121">From there, you can export the list.</span></span>

## <a name="severity-level-graphs"></a><span data-ttu-id="12741-122">Graphiques de niveau de gravité</span><span class="sxs-lookup"><span data-stu-id="12741-122">Severity level graphs</span></span>

<span data-ttu-id="12741-123">Chaque appareil est compté une seule fois en fonction de la vulnérabilité la plus grave trouvée sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="12741-123">Each device is counted only once according to the most severe vulnerability found on that device.</span></span>

![Graphique des niveaux de gravité de vulnérabilité actuels de l’appareil et graphique montrant les niveaux au fil du temps.](images/tvm-report-severity.png)

## <a name="exploit-availability-graphs"></a><span data-ttu-id="12741-125">Exploiter les graphiques de disponibilité</span><span class="sxs-lookup"><span data-stu-id="12741-125">Exploit availability graphs</span></span>

<span data-ttu-id="12741-126">Chaque appareil est compté une seule fois en fonction du niveau d’exploitation connu le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="12741-126">Each device is counted only once based on the highest level of known exploit.</span></span>

![Un graphique de la disponibilité actuelle de l’exploitation des appareils et un graphique montrant la disponibilité au fil du temps.](images/tvm-report-exploit-availability.png)

## <a name="vulnerability-age-graphs"></a><span data-ttu-id="12741-128">Graphiques de l’âge de vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="12741-128">Vulnerability age graphs</span></span>

<span data-ttu-id="12741-129">Chaque appareil est compté une seule fois sous la date de publication de la vulnérabilité la plus ancienne.</span><span class="sxs-lookup"><span data-stu-id="12741-129">Each device is counted only once under the oldest vulnerability publication date.</span></span> <span data-ttu-id="12741-130">Les vulnérabilités plus anciennes ont plus de chances d’être exploitées.</span><span class="sxs-lookup"><span data-stu-id="12741-130">Older vulnerabilities have a higher chance of being exploited.</span></span>

![Graphique de l’âge actuel de vulnérabilité de l’appareil et graphique montrant l’âge au fil du temps.](images/tvm-report-age.png)

## <a name="vulnerable-devices-by-operating-system-platform-graphs"></a><span data-ttu-id="12741-132">Appareils vulnérables par graphiques de plateforme de système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="12741-132">Vulnerable devices by operating system platform graphs</span></span>

<span data-ttu-id="12741-133">Nombre d’appareils sur chaque système d’exploitation exposés en raison de vulnérabilités logicielles.</span><span class="sxs-lookup"><span data-stu-id="12741-133">The number of devices on each operating system that are exposed due to software vulnerabilities.</span></span>

![Un graphique des appareils vulnérables actuels par plateforme de système d’exploitation et un graphique montrant les appareils vulnérables par les plateformes de système d’exploitation au fil du temps.](images/tvm-report-os.png)

## <a name="vulnerable-devices-by-windows-10-version-graphs"></a><span data-ttu-id="12741-135">Appareils vulnérables en Windows 10 graphiques de version</span><span class="sxs-lookup"><span data-stu-id="12741-135">Vulnerable devices by Windows 10 version graphs</span></span>

<span data-ttu-id="12741-136">Nombre d’appareils sur chaque version Windows 10 qui sont exposés en raison d’applications ou de système d’exploitation vulnérables.</span><span class="sxs-lookup"><span data-stu-id="12741-136">The number of devices on each Windows 10 version that are exposed due to vulnerable applications or OS.</span></span>

![Un graphique des appareils vulnérables actuels par version Windows 10 et un graphique montrant les appareils vulnérables par Windows 10 version au fil du temps.](images/tvm-report-version.png)

## <a name="related-topics"></a><span data-ttu-id="12741-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12741-138">Related topics</span></span>

- [<span data-ttu-id="12741-139">Vue d’ensemble gestion des vulnérabilités menaces et gestion des vulnérabilités menaces</span><span class="sxs-lookup"><span data-stu-id="12741-139">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="12741-140">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="12741-140">Security recommendations</span></span>](tvm-security-recommendation.md)
