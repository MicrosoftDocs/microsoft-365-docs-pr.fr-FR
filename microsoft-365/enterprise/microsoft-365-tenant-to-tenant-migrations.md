---
title: Microsoft 365 migrations client à client
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-collaboration
- M365-subscription-management
- SPO_Content
search.appverid:
- MET150
- MOE150
ms.assetid: eb45fd8b-1d5d-4b0c-9c5a-479dbb176e7d
f1.keywords:
- NOCSH
description: Découvrez comment migrer des Microsoft 365 client.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: f6e8277a7ca768db3a4a4acd2488859b7764a40c
ms.sourcegitcommit: 8b1bd7ca8cd81e4270f0c1e06d2b6ca81804a6aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "50819713"
---
# <a name="microsoft-365-tenant-to-tenant-migrations"></a><span data-ttu-id="2ba17-103">Microsoft 365 migrations client à client</span><span class="sxs-lookup"><span data-stu-id="2ba17-103">Microsoft 365 tenant-to-tenant migrations</span></span>

<span data-ttu-id="2ba17-104">Il existe plusieurs approches d’architecture pour les fusions, les acquisitions, les déssinttures et d’autres scénarios qui peuvent vous amener à migrer un client Microsoft 365 existant vers un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="2ba17-104">There are several architecture approaches for mergers, acquisitions, divestitures, and other scenarios that might lead you to migrate an existing Microsoft 365 tenant to a new tenant.</span></span> <span data-ttu-id="2ba17-105">La plupart des clients travaillent avec Microsoft Consulting Services ou un partenaire Microsoft pour migrer des clients, notamment à l’aide d’outils tiers pour migrer du contenu.</span><span class="sxs-lookup"><span data-stu-id="2ba17-105">Most customers work with Microsoft Consulting Services or a Microsoft partner to migrate tenants, including using third-party tools to migrate content.</span></span> 

<span data-ttu-id="2ba17-106">Utilisez le [modèle d’architecture](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf) de migration client à client pour comprendre comment planifier Microsoft 365 migrations client à client et les étapes d’une migration.</span><span class="sxs-lookup"><span data-stu-id="2ba17-106">Use the [Tenant-to-tenant migration architecture model](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf) to understand how to plan for Microsoft 365 tenant-to-tenant migrations and the steps of a migration.</span></span>

<span data-ttu-id="2ba17-107">[![Modèle de migration client à client](../media/solutions-architecture-center/msft-tenant-to-tenant-migration-thumb.png)](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf)</span><span class="sxs-lookup"><span data-stu-id="2ba17-107">[![Tenant-to-tenant migration model](../media/solutions-architecture-center/msft-tenant-to-tenant-migration-thumb.png)](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf)</span></span> 

<span data-ttu-id="2ba17-108">Vous téléchargez ce modèle au format [PDF](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf) et l’imprimez sur du papier de format lettre, légal ou tabloïd (11 x 17).</span><span class="sxs-lookup"><span data-stu-id="2ba17-108">You download this model in [PDF](https://download.microsoft.com/download/b/a/1/ba19dfe7-96e2-4983-8783-4dcff9cebe7b/microsoft-365-tenant-to-tenant-migration.pdf) format and print it on letter, legal, or tabloid (11 x 17) size paper.</span></span>

<span data-ttu-id="2ba17-109">Ce modèle fournit des conseils et un point de départ pour la planification avec des sections sur :</span><span class="sxs-lookup"><span data-stu-id="2ba17-109">This model provides guidance and a starting-point for planning with sections on:</span></span>

- <span data-ttu-id="2ba17-110">Mappage des scénarios d’entreprise aux approches d’architecture</span><span class="sxs-lookup"><span data-stu-id="2ba17-110">Mapping of business scenarios to architecture approaches</span></span>
- <span data-ttu-id="2ba17-111">Considérations relatives à la conception</span><span class="sxs-lookup"><span data-stu-id="2ba17-111">Design considerations</span></span>

<span data-ttu-id="2ba17-112">Ce modèle contient également des exemples détaillés des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2ba17-112">This model also contains detailed examples of:</span></span>

- <span data-ttu-id="2ba17-113">Un flux de migration d’événements unique</span><span class="sxs-lookup"><span data-stu-id="2ba17-113">A single event migration flow</span></span>
- <span data-ttu-id="2ba17-114">Un flux de migration par phases</span><span class="sxs-lookup"><span data-stu-id="2ba17-114">A phased migration flow</span></span>
- <span data-ttu-id="2ba17-115">Un flux de déplacement ou de fractionnement de client</span><span class="sxs-lookup"><span data-stu-id="2ba17-115">A tenant move or split flow</span></span>
