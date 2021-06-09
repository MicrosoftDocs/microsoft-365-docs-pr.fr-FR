---
title: Informations de fiabilité
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 06e1446ca290439c9e6689f4461c825438cf6aaf
ms.sourcegitcommit: cebbdd393dcfd93ff43a1ab66ad70115853f83e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52739782"
---
# <a name="reliability-insights"></a><span data-ttu-id="fbb91-103">Informations de fiabilité</span><span class="sxs-lookup"><span data-stu-id="fbb91-103">Reliability insights</span></span>

<span data-ttu-id="fbb91-104">Cette vue vous fournit un résumé d’état de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="fbb91-104">This view provides you with a health summary of your managed devices.</span></span> <span data-ttu-id="fbb91-105">Pour afficher les données de fiabilité, sélectionnez **l’onglet** Fiabilité.</span><span class="sxs-lookup"><span data-stu-id="fbb91-105">To view reliability data, select the **Reliability** tab.</span></span>


![Volet de fiabilité : fiabilité sur les appareils en haut à gauche, fiabilité dans le graphique dans le temps en haut à droite, tableau des problèmes les plus élevés dans la partie inférieure.](../../media/insights_reliability.png)

<span data-ttu-id="fbb91-108">La **section** Fiabilité sur les appareils offre un résumé d’état d’état rapide de votre déploiement au cours des 14 derniers jours en signalant le pourcentage d’appareils considérés comme « sains » et le temps moyen observé depuis la dernière défaillance signalée.</span><span class="sxs-lookup"><span data-stu-id="fbb91-108">The **Reliability across devices** section offers a quick health summary of your deployment over the last 14 days by reporting the percentage of devices considered to be “healthy” and the mean time observed since the last reported failure.</span></span> 

 
<span data-ttu-id="fbb91-109">Le **graphique Fiabilité au fil du** temps sur la droite indique le nombre d’appareils avec des erreurs critiques et le nombre total d’erreurs critiques observées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="fbb91-109">The **Reliability over time** graph on the right reports the number of devices with critical errors and the total number of observed critical errors over time.</span></span>

<span data-ttu-id="fbb91-110">La section **Problèmes principaux** détaille les problèmes détectés spécifiques qui affectent au moins 5 % de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="fbb91-110">The **Top issues** section details specific detected issues that affect at least 5% of your managed devices.</span></span> <span data-ttu-id="fbb91-111">Les détails signalés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fbb91-111">Reported details include:</span></span>

- <span data-ttu-id="fbb91-112">Type de problème</span><span class="sxs-lookup"><span data-stu-id="fbb91-112">The type of issue</span></span>
    - <span data-ttu-id="fbb91-113">L’application se bloque, au cours de laquelle une application cesse de fonctionner ou s’arrête de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="fbb91-113">Application crashes, in which an app stops functioning or unexpectedly stops</span></span>
    - <span data-ttu-id="fbb91-114">L’application se bloque, où une application cesse de répondre aux entrées</span><span class="sxs-lookup"><span data-stu-id="fbb91-114">Application hangs, where an application stops responding to input</span></span>
    - <span data-ttu-id="fbb91-115">Erreurs critiques, qui se produisent lorsque Windows a rencontré un problème dont il ne peut pas récupérer</span><span class="sxs-lookup"><span data-stu-id="fbb91-115">Critical errors, which occur when Windows has encountered an issue it can't recover from</span></span>
- <span data-ttu-id="fbb91-116">Nombre d’appareils affectés par le même problème</span><span class="sxs-lookup"><span data-stu-id="fbb91-116">The number of devices affected by the same issue</span></span>
- <span data-ttu-id="fbb91-117">Pourcentage d’appareils gérés représenté par le nombre</span><span class="sxs-lookup"><span data-stu-id="fbb91-117">The percentage of managed devices that number represents</span></span>
- <span data-ttu-id="fbb91-118">Nombre total d’occurrences du problème spécifique</span><span class="sxs-lookup"><span data-stu-id="fbb91-118">The total count of occurrences of the specific issue</span></span>
- <span data-ttu-id="fbb91-119">Composant logiciel qui semble être la source du problème</span><span class="sxs-lookup"><span data-stu-id="fbb91-119">The software component that appears to be the source of the problem</span></span>
- <span data-ttu-id="fbb91-120">Catégorie du problème détecté :</span><span class="sxs-lookup"><span data-stu-id="fbb91-120">The category of the detected problem:</span></span>
    - <span data-ttu-id="fbb91-121">Navigateur (Edge, Chrome, IE)</span><span class="sxs-lookup"><span data-stu-id="fbb91-121">Browser (Edge, Chrome, IE)</span></span>
    - <span data-ttu-id="fbb91-122">Inconnu (composants autres que Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbb91-122">Unknown (Non-Microsoft components)</span></span>
    - <span data-ttu-id="fbb91-123">Pilote (audio, graphiques ou autres pilotes)</span><span class="sxs-lookup"><span data-stu-id="fbb91-123">Driver (audio, graphics, or other drivers)</span></span>
    - <span data-ttu-id="fbb91-124">Productivité (Slack, G-Suites, Microsoft Office et ses extensions ou extensions, Teams)</span><span class="sxs-lookup"><span data-stu-id="fbb91-124">Productivity (Slack, G-Suites, Microsoft Office and its add-ons or extensions, Teams)</span></span>
    - <span data-ttu-id="fbb91-125">Média (applications d’image, de musique ou de vidéo)</span><span class="sxs-lookup"><span data-stu-id="fbb91-125">Media (image, music, or video apps</span></span>
    - <span data-ttu-id="fbb91-126">Sécurité (Windows composants de sécurité)</span><span class="sxs-lookup"><span data-stu-id="fbb91-126">Security (Windows security components)</span></span>
- <span data-ttu-id="fbb91-127">L’état actuel de Bureau géré Microsoft Operations examine et remédie au problème</span><span class="sxs-lookup"><span data-stu-id="fbb91-127">The current status as Microsoft Managed Desktop Operations investigates and remediates the issue</span></span>

