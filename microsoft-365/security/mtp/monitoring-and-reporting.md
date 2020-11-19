---
title: Surveillance et affichage des rapports-centre de sécurité
description: Décrit comment le centre de sécurité Microsoft 365 fournit un résumé de l’état de protection et de sécurité.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, état
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: d52c401c4b2e995e5ec18895c158f77ce0fce746
ms.sourcegitcommit: 474bd6a86c3692d11fb2c454591c89029ac5bbd5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2020
ms.locfileid: "49356882"
---
# <a name="monitor-and-view-reports-in-the-microsoft-365-security-center"></a><span data-ttu-id="d673f-104">Surveillance et affichage des rapports dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d673f-104">Monitor and view reports in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

> <span data-ttu-id="d673f-105">Vous souhaitez découvrir Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="d673f-105">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="d673f-106">Vous pouvez l' [évaluer dans un environnement de laboratoire](https://aka.ms/mtp-trial-lab) ou [exécuter votre projet pilote en production](https://aka.ms/m365d-pilotplaybook).</span><span class="sxs-lookup"><span data-stu-id="d673f-106">You can [evaluate it in a lab environment](https://aka.ms/mtp-trial-lab) or [run your pilot project in production](https://aka.ms/m365d-pilotplaybook).</span></span>
>

<span data-ttu-id="d673f-107">Le centre de sécurité Microsoft 365 fournit un résumé des États de protection et de sécurité dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d673f-107">The Microsoft 365 security center provides a summary of protection and security statuses across your Microsoft 365 environment.</span></span>

<span data-ttu-id="d673f-108">Le centre de sécurité inclut une section de **rapports** qui comprend un hôte de cartes couvrant un grand nombre de domaines.</span><span class="sxs-lookup"><span data-stu-id="d673f-108">The security center includes a **Reports** section which features a host of cards covering a variety of areas.</span></span> <span data-ttu-id="d673f-109">Les analystes de la sécurité et les administrateurs peuvent suivre les cartes dans le cadre de leurs opérations quotidiennes.</span><span class="sxs-lookup"><span data-stu-id="d673f-109">Security analysts and administrators can track the cards as part of their day-to-day operations.</span></span> <span data-ttu-id="d673f-110">Sur l’exploration, les cartes fournissent des rapports détaillés et, dans certains cas, des options de gestion.</span><span class="sxs-lookup"><span data-stu-id="d673f-110">On drill-down, cards provide detailed reports and, in some cases, management options.</span></span>

## <a name="customize-views"></a><span data-ttu-id="d673f-111">Personnaliser les affichages</span><span class="sxs-lookup"><span data-stu-id="d673f-111">Customize views</span></span>

<span data-ttu-id="d673f-112">Par défaut, les cartes sont regroupées dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="d673f-112">By default, cards are grouped into these categories:</span></span>
  
* <span data-ttu-id="d673f-113">[Identités](monitor-and-report-identities.md) : comptes d’utilisateur et informations d’identification</span><span class="sxs-lookup"><span data-stu-id="d673f-113">[Identities](monitor-and-report-identities.md) - user accounts and credentials</span></span>
* <span data-ttu-id="d673f-114">[Données](monitor-data.md) -courrier électronique et contenu de document</span><span class="sxs-lookup"><span data-stu-id="d673f-114">[Data](monitor-data.md) - email and document contents</span></span>
* <span data-ttu-id="d673f-115">[Appareils](monitor-devices.md) : ordinateurs, téléphones mobiles et autres appareils</span><span class="sxs-lookup"><span data-stu-id="d673f-115">[Devices](monitor-devices.md) - computers, mobile phones, and other devices</span></span>
* <span data-ttu-id="d673f-116">[Apps](monitor-apps.md) : programmes et services en ligne associés</span><span class="sxs-lookup"><span data-stu-id="d673f-116">[Apps](monitor-apps.md) - programs and attached online services</span></span>

<span data-ttu-id="d673f-117">Passez à la **rubrique regrouper par**, pour réorganiser les cartes et les regrouper dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d673f-117">Switch to **Group by topic**, to rearrange the cards and group them into the following topics:</span></span>

* <span data-ttu-id="d673f-118">Cartes de **risque** qui mettent en évidence des entités, telles que des comptes et des appareils, susceptibles d’être menacées.</span><span class="sxs-lookup"><span data-stu-id="d673f-118">**Risk** - cards that highlight entities, such as accounts and devices, that might be at risk.</span></span> <span data-ttu-id="d673f-119">Ces cartes surlignent également les sources de risque possibles, telles que les nouvelles campagnes de menace et les applications Cloud avec privilèges.</span><span class="sxs-lookup"><span data-stu-id="d673f-119">These cards also highlight possible sources of risk, such as new threat campaigns and privileged cloud apps</span></span>  
* <span data-ttu-id="d673f-120">**Tendances de détection** -cartes qui mettent en évidence les nouvelles détections de menaces, les anomalies et les violations de stratégie</span><span class="sxs-lookup"><span data-stu-id="d673f-120">**Detection trends** - cards that highlight new threat detections, anomalies, and policy violations</span></span>
* <span data-ttu-id="d673f-121">Les cartes de **configuration et d’intégrité** qui couvrent la configuration et le déploiement des contrôles de sécurité, y compris les États d’intégration des appareils aux services de gestion</span><span class="sxs-lookup"><span data-stu-id="d673f-121">**Configuration and health** - cards that cover the configuration and deployment of security controls, including device onboarding states to management services</span></span>
* <span data-ttu-id="d673f-122">**Autre** -toutes les autres cartes non classées sous d’autres rubriques</span><span class="sxs-lookup"><span data-stu-id="d673f-122">**Other** - all other cards not categorized under other topics</span></span>
