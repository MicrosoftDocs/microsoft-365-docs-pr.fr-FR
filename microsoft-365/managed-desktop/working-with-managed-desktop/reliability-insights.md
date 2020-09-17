---
title: Informations de fiabilité
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 06e1446ca290439c9e6689f4461c825438cf6aaf
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950341"
---
# <a name="reliability-insights"></a><span data-ttu-id="544e6-103">Informations de fiabilité</span><span class="sxs-lookup"><span data-stu-id="544e6-103">Reliability insights</span></span>

<span data-ttu-id="544e6-104">Cet affichage vous fournit un résumé de l’intégrité de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="544e6-104">This view provides you with a health summary of your managed devices.</span></span> <span data-ttu-id="544e6-105">Pour afficher les données de fiabilité, sélectionnez l’onglet **fiabilité** .</span><span class="sxs-lookup"><span data-stu-id="544e6-105">To view reliability data, select the **Reliability** tab.</span></span>


![Volet de fiabilité : fiabilité entre les appareils dans l’angle supérieur gauche, fiabilité sur le graphique des temps dans le coin supérieur droit de la table des problèmes en haut.](../../media/insights_reliability.png)

<span data-ttu-id="544e6-108">La section **fiabilité sur les appareils** offre un récapitulatif de l’intégrité rapide de votre déploiement au cours des 14 derniers jours en signalant le pourcentage d’appareils considérés comme « sains » et le temps moyen observé depuis le dernier échec signalé.</span><span class="sxs-lookup"><span data-stu-id="544e6-108">The **Reliability across devices** section offers a quick health summary of your deployment over the last 14 days by reporting the percentage of devices considered to be “healthy” and the mean time observed since the last reported failure.</span></span> 

 
<span data-ttu-id="544e6-109">La **fiabilité** dans le graphique temporel signale le nombre d’appareils présentant des erreurs critiques et le nombre total d’erreurs critiques observées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="544e6-109">The **Reliability over time** graph on the right reports the number of devices with critical errors and the total number of observed critical errors over time.</span></span>

<span data-ttu-id="544e6-110">La section des **problèmes principaux** explique en détail des problèmes détectés spécifiques affectant au moins 5% de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="544e6-110">The **Top issues** section details specific detected issues that affect at least 5% of your managed devices.</span></span> <span data-ttu-id="544e6-111">Les détails signalés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="544e6-111">Reported details include:</span></span>

- <span data-ttu-id="544e6-112">Type de problème</span><span class="sxs-lookup"><span data-stu-id="544e6-112">The type of issue</span></span>
    - <span data-ttu-id="544e6-113">L’application se bloque, dans laquelle une application cesse de fonctionner ou s’arrête de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="544e6-113">Application crashes, in which an app stops functioning or unexpectedly stops</span></span>
    - <span data-ttu-id="544e6-114">L’application se bloque lorsqu’une application cesse de répondre aux entrées</span><span class="sxs-lookup"><span data-stu-id="544e6-114">Application hangs, where an application stops responding to input</span></span>
    - <span data-ttu-id="544e6-115">Erreurs critiques, qui se produisent lorsque Windows a rencontré un problème qu’il ne peut pas récupérer à partir de</span><span class="sxs-lookup"><span data-stu-id="544e6-115">Critical errors, which occur when Windows has encountered an issue it can't recover from</span></span>
- <span data-ttu-id="544e6-116">Nombre d’appareils affectés par le même problème</span><span class="sxs-lookup"><span data-stu-id="544e6-116">The number of devices affected by the same issue</span></span>
- <span data-ttu-id="544e6-117">Pourcentage d’appareils gérés que le nombre représente</span><span class="sxs-lookup"><span data-stu-id="544e6-117">The percentage of managed devices that number represents</span></span>
- <span data-ttu-id="544e6-118">Nombre total d’occurrences du problème spécifique</span><span class="sxs-lookup"><span data-stu-id="544e6-118">The total count of occurrences of the specific issue</span></span>
- <span data-ttu-id="544e6-119">Composant logiciel qui semble être à l’origine du problème</span><span class="sxs-lookup"><span data-stu-id="544e6-119">The software component that appears to be the source of the problem</span></span>
- <span data-ttu-id="544e6-120">Catégorie du problème détecté :</span><span class="sxs-lookup"><span data-stu-id="544e6-120">The category of the detected problem:</span></span>
    - <span data-ttu-id="544e6-121">Navigateur (Edge, chrome, IE)</span><span class="sxs-lookup"><span data-stu-id="544e6-121">Browser (Edge, Chrome, IE)</span></span>
    - <span data-ttu-id="544e6-122">Inconnu (composants non-Microsoft)</span><span class="sxs-lookup"><span data-stu-id="544e6-122">Unknown (Non-Microsoft components)</span></span>
    - <span data-ttu-id="544e6-123">Pilote (audio, graphiques ou autres pilotes)</span><span class="sxs-lookup"><span data-stu-id="544e6-123">Driver (audio, graphics, or other drivers)</span></span>
    - <span data-ttu-id="544e6-124">Productivité (marge, G-Suites, Microsoft Office et ses compléments ou extensions, Teams)</span><span class="sxs-lookup"><span data-stu-id="544e6-124">Productivity (Slack, G-Suites, Microsoft Office and its add-ons or extensions, Teams)</span></span>
    - <span data-ttu-id="544e6-125">Applications multimédia (image, musique ou vidéo)</span><span class="sxs-lookup"><span data-stu-id="544e6-125">Media (image, music, or video apps</span></span>
    - <span data-ttu-id="544e6-126">Sécurité (composants de sécurité Windows)</span><span class="sxs-lookup"><span data-stu-id="544e6-126">Security (Windows security components)</span></span>
- <span data-ttu-id="544e6-127">État actuel lorsque Microsoft Managed Desktop Operations examine et corrige le problème</span><span class="sxs-lookup"><span data-stu-id="544e6-127">The current status as Microsoft Managed Desktop Operations investigates and remediates the issue</span></span>

