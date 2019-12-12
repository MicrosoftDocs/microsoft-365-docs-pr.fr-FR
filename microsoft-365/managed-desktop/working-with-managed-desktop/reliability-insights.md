---
title: Informations de fiabilité
description: ''
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 1f642d2790af5f4ec83dd1bbe57a9be249d095d1
ms.sourcegitcommit: b65c80051e53d9be223f4769f4d42a39f5a07735
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "39962331"
---
# <a name="reliability-insights"></a><span data-ttu-id="f836f-103">Informations de fiabilité</span><span class="sxs-lookup"><span data-stu-id="f836f-103">Reliability insights</span></span>

<span data-ttu-id="f836f-104">Cet affichage vous fournit un résumé de l’intégrité de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="f836f-104">This view provides you with a health summary of your managed devices.</span></span> <span data-ttu-id="f836f-105">Pour afficher les données de fiabilité, sélectionnez l’onglet **fiabilité** .</span><span class="sxs-lookup"><span data-stu-id="f836f-105">To view reliability data, select the **Reliability** tab.</span></span>


![Volet de fiabilité : fiabilité entre les appareils dans l’angle supérieur gauche, fiabilité sur le graphique des temps dans le coin supérieur droit de la table des problèmes en haut.](images/insights_reliability.png)

<span data-ttu-id="f836f-108">La section **fiabilité sur les appareils** offre un récapitulatif de l’intégrité rapide de votre déploiement au cours des 14 derniers jours en signalant le pourcentage d’appareils considérés comme « sains » et le temps moyen observé depuis le dernier échec signalé.</span><span class="sxs-lookup"><span data-stu-id="f836f-108">The **Reliability across devices** section offers a quick health summary of your deployment over the last 14 days by reporting the percentage of devices considered to be “healthy” and the mean time observed since the last reported failure.</span></span> 

 
<span data-ttu-id="f836f-109">La **fiabilité** dans le graphique temporel signale le nombre d’appareils présentant des erreurs critiques et le nombre total d’erreurs critiques observées au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="f836f-109">The **Reliability over time** graph on the right reports the number of devices with critical errors and the total number of observed critical errors over time.</span></span>

<span data-ttu-id="f836f-110">La section des **problèmes principaux** explique en détail des problèmes détectés spécifiques affectant au moins 5% de vos appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="f836f-110">The **Top issues** section details specific detected issues that affect at least 5% of your managed devices.</span></span> <span data-ttu-id="f836f-111">Les détails signalés sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f836f-111">Reported details include:</span></span>

- <span data-ttu-id="f836f-112">Type de problème</span><span class="sxs-lookup"><span data-stu-id="f836f-112">The type of issue</span></span>
    - <span data-ttu-id="f836f-113">L’application se bloque, dans laquelle une application cesse de fonctionner ou s’arrête de manière inattendue</span><span class="sxs-lookup"><span data-stu-id="f836f-113">Application crashes, in which an app stops functioning or unexpectedly stops</span></span>
    - <span data-ttu-id="f836f-114">L’application se bloque lorsqu’une application cesse de répondre aux entrées</span><span class="sxs-lookup"><span data-stu-id="f836f-114">Application hangs, where an application stops responding to input</span></span>
    - <span data-ttu-id="f836f-115">Erreurs critiques, qui se produisent lorsque Windows a rencontré un problème qu’il ne peut pas récupérer à partir de</span><span class="sxs-lookup"><span data-stu-id="f836f-115">Critical errors, which occur when Windows has encountered an issue it can't recover from</span></span>
- <span data-ttu-id="f836f-116">Nombre d’appareils affectés par le même problème</span><span class="sxs-lookup"><span data-stu-id="f836f-116">The number of devices affected by the same issue</span></span>
- <span data-ttu-id="f836f-117">Pourcentage d’appareils gérés que le nombre représente</span><span class="sxs-lookup"><span data-stu-id="f836f-117">The percentage of managed devices that number represents</span></span>
- <span data-ttu-id="f836f-118">Nombre total d’occurrences d’un problème spécifique</span><span class="sxs-lookup"><span data-stu-id="f836f-118">The total count of occurences of the specific issue</span></span>
- <span data-ttu-id="f836f-119">Composant logiciel qui semble être à l’origine du problème</span><span class="sxs-lookup"><span data-stu-id="f836f-119">The software component that appears to be the source of the problem</span></span>
- <span data-ttu-id="f836f-120">Catégorie du problème détecté :</span><span class="sxs-lookup"><span data-stu-id="f836f-120">The category of the detected problem:</span></span>
    - <span data-ttu-id="f836f-121">Navigateur (Edge, chrome, IE)</span><span class="sxs-lookup"><span data-stu-id="f836f-121">Browser (Edge, Chrome, IE)</span></span>
    - <span data-ttu-id="f836f-122">Inconnu (composants non-Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f836f-122">Unknown (Non-Microsoft components)</span></span>
    - <span data-ttu-id="f836f-123">Pilote (audio, graphiques ou autres pilotes)</span><span class="sxs-lookup"><span data-stu-id="f836f-123">Driver (audio, graphics, or other drivers)</span></span>
    - <span data-ttu-id="f836f-124">Productivité (marge, G-Suites, Microsoft Office et ses compléments ou extensions, Teams)</span><span class="sxs-lookup"><span data-stu-id="f836f-124">Productivity (Slack, G-Suites, Microsoft Office and its add-ons or extensions, Teams)</span></span>
    - <span data-ttu-id="f836f-125">Applications multimédia (image, musique ou vidéo)</span><span class="sxs-lookup"><span data-stu-id="f836f-125">Media (image, music, or video apps</span></span>
    - <span data-ttu-id="f836f-126">Sécurité (composants de sécurité Windows)</span><span class="sxs-lookup"><span data-stu-id="f836f-126">Security (Windows security components)</span></span>
- <span data-ttu-id="f836f-127">État actuel lorsque Microsoft Managed Desktop Operations examine et corrige le problème</span><span class="sxs-lookup"><span data-stu-id="f836f-127">The current status as Microsoft Managed Desktop Operations investigates and remediates the issue</span></span>

