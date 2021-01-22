---
title: Surveiller et afficher les rapports - Centre de sécurité
description: Décrit comment le Centre de sécurité Microsoft 365 fournit un résumé rapide de l’état de la protection et de la sécurité.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, surveiller, signaler, état
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-apr2020
ms.technology: m365d
ms.openlocfilehash: 4667c39a8d416d7e186d41063d7057109758cd33
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930401"
---
# <a name="monitor-and-view-reports-in-the-microsoft-365-security-center"></a><span data-ttu-id="03f48-104">Surveiller et afficher des rapports dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="03f48-104">Monitor and view reports in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

> <span data-ttu-id="03f48-105">Vous souhaitez découvrir Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="03f48-105">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="03f48-106">Vous pouvez [l’évaluer dans un environnement de laboratoire](https://aka.ms/mtp-trial-lab) ou exécuter votre projet pilote en [production.](https://aka.ms/m365d-pilotplaybook)</span><span class="sxs-lookup"><span data-stu-id="03f48-106">You can [evaluate it in a lab environment](https://aka.ms/mtp-trial-lab) or [run your pilot project in production](https://aka.ms/m365d-pilotplaybook).</span></span>
>

<span data-ttu-id="03f48-107">Le Centre de sécurité Microsoft 365 fournit un résumé des statuts de protection et de sécurité au sein de votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="03f48-107">The Microsoft 365 security center provides a summary of protection and security statuses across your Microsoft 365 environment.</span></span>

<span data-ttu-id="03f48-108">Le centre de sécurité inclut une section **Rapports** qui propose une multitude de cartes couvrant différents domaines.</span><span class="sxs-lookup"><span data-stu-id="03f48-108">The security center includes a **Reports** section which features a host of cards covering a variety of areas.</span></span> <span data-ttu-id="03f48-109">Les analystes et les administrateurs de sécurité peuvent suivre les cartes dans le cadre de leurs opérations quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="03f48-109">Security analysts and administrators can track the cards as part of their day-to-day operations.</span></span> <span data-ttu-id="03f48-110">Lors de l’analyse, les cartes fournissent des rapports détaillés et, dans certains cas, des options de gestion.</span><span class="sxs-lookup"><span data-stu-id="03f48-110">On drill-down, cards provide detailed reports and, in some cases, management options.</span></span>

## <a name="customize-views"></a><span data-ttu-id="03f48-111">Personnaliser les affichages</span><span class="sxs-lookup"><span data-stu-id="03f48-111">Customize views</span></span>

<span data-ttu-id="03f48-112">Par défaut, les cartes sont regroupées dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="03f48-112">By default, cards are grouped into these categories:</span></span>
  
* <span data-ttu-id="03f48-113">[Identités :](monitor-and-report-identities.md) comptes d’utilisateur et informations d’identification</span><span class="sxs-lookup"><span data-stu-id="03f48-113">[Identities](monitor-and-report-identities.md) - user accounts and credentials</span></span>
* <span data-ttu-id="03f48-114">[Données :](monitor-data.md) contenu du courrier électronique et du document</span><span class="sxs-lookup"><span data-stu-id="03f48-114">[Data](monitor-data.md) - email and document contents</span></span>
* <span data-ttu-id="03f48-115">[Appareils](monitor-devices.md) : ordinateurs, téléphones mobiles et autres appareils</span><span class="sxs-lookup"><span data-stu-id="03f48-115">[Devices](monitor-devices.md) - computers, mobile phones, and other devices</span></span>
* <span data-ttu-id="03f48-116">[Applications :](monitor-apps.md) programmes et services en ligne connectés</span><span class="sxs-lookup"><span data-stu-id="03f48-116">[Apps](monitor-apps.md) - programs and attached online services</span></span>

<span data-ttu-id="03f48-117">Basculez vers **Grouper par rubrique,** pour réorganiser les cartes et les grouper dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="03f48-117">Switch to **Group by topic**, to rearrange the cards and group them into the following topics:</span></span>

* <span data-ttu-id="03f48-118">**Risque** : cartes qui mettent en évidence les entités, telles que les comptes et les appareils, qui peuvent être à risque.</span><span class="sxs-lookup"><span data-stu-id="03f48-118">**Risk** - cards that highlight entities, such as accounts and devices, that might be at risk.</span></span> <span data-ttu-id="03f48-119">Ces cartes mettent également en évidence les sources de risque possibles, telles que les nouvelles campagnes contre les menaces et les applications cloud privilégiées</span><span class="sxs-lookup"><span data-stu-id="03f48-119">These cards also highlight possible sources of risk, such as new threat campaigns and privileged cloud apps</span></span>  
* <span data-ttu-id="03f48-120">**Tendances de détection** : cartes qui mettent en évidence les nouvelles détections de menaces, les anomalies et les violations de stratégie</span><span class="sxs-lookup"><span data-stu-id="03f48-120">**Detection trends** - cards that highlight new threat detections, anomalies, and policy violations</span></span>
* <span data-ttu-id="03f48-121">**Configuration et santé :** cartes qui couvrent la configuration et le déploiement des contrôles de sécurité, y compris les états d’intégration d’appareil aux services de gestion</span><span class="sxs-lookup"><span data-stu-id="03f48-121">**Configuration and health** - cards that cover the configuration and deployment of security controls, including device onboarding states to management services</span></span>
* <span data-ttu-id="03f48-122">**Autre** - toutes les autres cartes non classées dans d’autres rubriques</span><span class="sxs-lookup"><span data-stu-id="03f48-122">**Other** - all other cards not categorized under other topics</span></span>
