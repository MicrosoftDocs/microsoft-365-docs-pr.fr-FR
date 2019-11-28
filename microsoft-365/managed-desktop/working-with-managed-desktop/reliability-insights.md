---
title: Informations de fiabilité
description: ''
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 8ecc117b2bc6e7cec3dcf0470a6d3c61ad34adf0
ms.sourcegitcommit: e386037c9cc335c86896dc153344850735afbccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "39634031"
---
# <a name="reliability-insights"></a><span data-ttu-id="63c71-103">Informations de fiabilité</span><span class="sxs-lookup"><span data-stu-id="63c71-103">Reliability insights</span></span>

<span data-ttu-id="63c71-104">Cet affichage vous fournit un résumé de l’intégrité de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="63c71-104">This view provides you with a health summary of your managed devices.</span></span> <span data-ttu-id="63c71-105">Pour afficher les données de fiabilité, sélectionnez l’onglet **fiabilité** .</span><span class="sxs-lookup"><span data-stu-id="63c71-105">To view reliability data, select the **Reliability** tab.</span></span>


![Volet de fiabilité](images/insights_reliability.png)

<span data-ttu-id="63c71-107">La section **fiabilité sur les appareils** offre un récapitulatif de l’intégrité rapide de votre déploiement au cours des 14 derniers jours en signalant le pourcentage d’appareils considérés comme « sains » et le temps moyen observé depuis le dernier échec signalé.</span><span class="sxs-lookup"><span data-stu-id="63c71-107">The **Reliability across devices** section offers a quick health summary of your deployment over the last 14 days by reporting the percentage of devices considered to be “healthy” and the mean time observed since the last reported failure.</span></span> 

 
<span data-ttu-id="63c71-108">La **fiabilité** dans le graphique temporel signale le nombre d’appareils présentant des erreurs critiques et le nombre total d’erreurs critiques observées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="63c71-108">The **Reliability over time** graph on the right reports the number of devices with critical errors and the total number of observed critical errors over time.</span></span>

<span data-ttu-id="63c71-109">La section des **problèmes principaux** explique en détail des problèmes détectés spécifiques affectant au moins 5% de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="63c71-109">The **Top issues** section details specific detected issues that affect at least 5% of your managed devices.</span></span> <span data-ttu-id="63c71-110">Les détails signalés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="63c71-110">Reported details include:</span></span>

- <span data-ttu-id="63c71-111">Type de problème</span><span class="sxs-lookup"><span data-stu-id="63c71-111">The type of issue</span></span>
    - <span data-ttu-id="63c71-112">L’application se bloque, dans laquelle une application cesse de fonctionner ou s’arrête de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="63c71-112">Application crashes, in which an app stops functioning or unexpectedly stops</span></span>
    - <span data-ttu-id="63c71-113">L’application se bloque lorsqu’une application cesse de répondre aux entrées</span><span class="sxs-lookup"><span data-stu-id="63c71-113">Application hangs, where an application stops responding to input</span></span>
    - <span data-ttu-id="63c71-114">Erreurs critiques, qui se produisent lorsque Windows a rencontré un problème qu’il ne peut pas récupérer à partir de</span><span class="sxs-lookup"><span data-stu-id="63c71-114">Critical errors, which occur when Windows has encountered an issue it can't recover from</span></span>
- <span data-ttu-id="63c71-115">Nombre d’appareils affectés par le même problème</span><span class="sxs-lookup"><span data-stu-id="63c71-115">The number of devices affected by the same issue</span></span>
- <span data-ttu-id="63c71-116">Pourcentage d’appareils gérés que le nombre représente</span><span class="sxs-lookup"><span data-stu-id="63c71-116">The percentage of managed devices that number represents</span></span>
- <span data-ttu-id="63c71-117">Nombre total d’occurrences d’un problème spécifique</span><span class="sxs-lookup"><span data-stu-id="63c71-117">The total count of occurences of the specific issue</span></span>
- <span data-ttu-id="63c71-118">Composant logiciel qui semble être à l’origine du problème</span><span class="sxs-lookup"><span data-stu-id="63c71-118">The software component that appears to be the source of the problem</span></span>
- <span data-ttu-id="63c71-119">Catégorie du problème détecté :</span><span class="sxs-lookup"><span data-stu-id="63c71-119">The category of the detected problem:</span></span>
    - <span data-ttu-id="63c71-120">Navigateur (Edge, chrome, IE)</span><span class="sxs-lookup"><span data-stu-id="63c71-120">Browser (Edge, Chrome, IE)</span></span>
    - <span data-ttu-id="63c71-121">Inconnu (composants non-Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63c71-121">Unknown (Non-Microsoft components)</span></span>
    - <span data-ttu-id="63c71-122">Pilote (audio, graphiques ou autres pilotes)</span><span class="sxs-lookup"><span data-stu-id="63c71-122">Driver (audio, graphics, or other drivers)</span></span>
    - <span data-ttu-id="63c71-123">Productivité (marge, G-Suites, Microsoft Office et ses compléments ou extensions, Teams)</span><span class="sxs-lookup"><span data-stu-id="63c71-123">Productivity (Slack, G-Suites, Microsoft Office and its add-ons or extensions, Teams)</span></span>
    - <span data-ttu-id="63c71-124">Applications multimédia (image, musique ou vidéo)</span><span class="sxs-lookup"><span data-stu-id="63c71-124">Media (image, music, or video apps</span></span>
    - <span data-ttu-id="63c71-125">Sécurité (composants de sécurité Windows)</span><span class="sxs-lookup"><span data-stu-id="63c71-125">Security (Windows security components)</span></span>
- <span data-ttu-id="63c71-126">État actuel lorsque Microsoft Managed Desktop Operations examine et corrige le problème</span><span class="sxs-lookup"><span data-stu-id="63c71-126">The current status as Microsoft Managed Desktop Operations investigates and remediates the issue</span></span>

