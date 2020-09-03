---
title: Microsoft 365 traitant de l’endommagement des données
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
description: Cet article décrit la corruption des données dans Microsoft 365, ainsi que les efforts entrepris par Microsoft pour prévenir et récupérer les données.
ms.openlocfilehash: 767be71bb08c49070488cc965165ac86e98836bd
ms.sourcegitcommit: c029834c8a914b4e072de847fc4c3a3dde7790c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47331871"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="300e8-103">Gérer l’altération des données dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="300e8-103">Dealing with Data Corruption in Microsoft 365</span></span>

<span data-ttu-id="300e8-104">L’un des aspects les plus délicats de l’exécution d’un service Cloud de grande envergure est la façon de gérer l’altération des données, compte tenu du volume important de données et des systèmes indépendants.</span><span class="sxs-lookup"><span data-stu-id="300e8-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="300e8-105">La corruption des données peut être causée par :</span><span class="sxs-lookup"><span data-stu-id="300e8-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="300e8-106">Bogues d’application ou d’infrastructure, en corrompant tout ou partie de l’état de l’application</span><span class="sxs-lookup"><span data-stu-id="300e8-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="300e8-107">Problèmes matériels entraînant la perte de données ou l’impossibilité de lire des données</span><span class="sxs-lookup"><span data-stu-id="300e8-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="300e8-108">Erreurs opérationnelles humaines</span><span class="sxs-lookup"><span data-stu-id="300e8-108">Human operational errors</span></span>
- <span data-ttu-id="300e8-109">Pirates malveillants et employés mécontents</span><span class="sxs-lookup"><span data-stu-id="300e8-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="300e8-110">Incidents dans les services externes entraînant une perte de données</span><span class="sxs-lookup"><span data-stu-id="300e8-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="300e8-111">Étant donné que la résilience accrue de l’intégrité des données signifie moins d’incidents d’endommagement des données, Microsoft a intégré les mécanismes de protection de Microsoft 365 pour empêcher la corruption, ainsi que les systèmes et les processus qui nous permettent de récupérer les données le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="300e8-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="300e8-112">Il existe des vérifications et des processus dans les différentes étapes du processus de publication d’ingénierie afin de renforcer la résistance contre l’altération des données, notamment :</span><span class="sxs-lookup"><span data-stu-id="300e8-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="300e8-113">Conception du système</span><span class="sxs-lookup"><span data-stu-id="300e8-113">System Design</span></span>
- <span data-ttu-id="300e8-114">Structure et organisation du code</span><span class="sxs-lookup"><span data-stu-id="300e8-114">Code organization and structure</span></span>
- <span data-ttu-id="300e8-115">Révision du code</span><span class="sxs-lookup"><span data-stu-id="300e8-115">Code review</span></span>
- <span data-ttu-id="300e8-116">Tests d’unité, tests d’intégration et tests système</span><span class="sxs-lookup"><span data-stu-id="300e8-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="300e8-117">Tests/portails de fils de voyage</span><span class="sxs-lookup"><span data-stu-id="300e8-117">Trip wires tests/gates</span></span>

<span data-ttu-id="300e8-118">Dans les environnements de production Microsoft 365, la réplication d’homologue entre centres de données garantit qu’il y a toujours plusieurs copies dynamiques de toutes les données.</span><span class="sxs-lookup"><span data-stu-id="300e8-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="300e8-119">Les images et les scripts standard permettent de récupérer les serveurs perdus, et les données répliquées sont utilisées pour restaurer les données client.</span><span class="sxs-lookup"><span data-stu-id="300e8-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="300e8-120">En raison des contrôles et des processus de résilience des données intégrés, Microsoft conserve uniquement les sauvegardes de la documentation du système d’information Microsoft 365 (y compris la documentation liée à la sécurité), à l’aide de la réplication intégrée dans SharePoint Online et de notre outil référentiel de code interne, Source Depot.</span><span class="sxs-lookup"><span data-stu-id="300e8-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="300e8-121">La documentation système est stockée dans SharePoint Online, et Source Depot contient des images système et d’application.</span><span class="sxs-lookup"><span data-stu-id="300e8-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="300e8-122">SharePoint Online et le SAV source utilisent tous deux le contrôle de version et sont répliqués en quasi-temps réel.</span><span class="sxs-lookup"><span data-stu-id="300e8-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
