---
title: Informations supplémentaires pour les fournisseurs de solutions Cloud
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Informations supplémentaires pour les fournisseurs de solutions Cloud pertinents pour la migration à partir de Microsoft Cloud Deutschland.'
ms.openlocfilehash: 843552c55acba57c5c2da4a1a885d65cb4e59d84
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52984915"
---
# <a name="additional-information-for-cloud-solution-providers"></a><span data-ttu-id="42b5c-103">Informations supplémentaires pour les fournisseurs de solutions Cloud</span><span class="sxs-lookup"><span data-stu-id="42b5c-103">Additional information for Cloud Solution Providers</span></span>

<span data-ttu-id="42b5c-104">Les fournisseurs de solutions Cloud (CSP) qui prennent en charge les clients doivent prendre des mesures supplémentaires lors de la migration de Microsoft Cloud Deutschland vers la nouvelle région de centre de données allemande.</span><span class="sxs-lookup"><span data-stu-id="42b5c-104">Cloud Solution Providers (CSPs) supporting customers  need to take additional steps during the migration from Microsoft Cloud Deutschland to the new German datacenter region.</span></span>

## <a name="partner-tenant-migration"></a><span data-ttu-id="42b5c-105">Migration des locataires partenaires</span><span class="sxs-lookup"><span data-stu-id="42b5c-105">Partner tenant migration</span></span>

<span data-ttu-id="42b5c-106">Les clients Microsoft Cloud Deutschland partenaires ne seront pas migrés.</span><span class="sxs-lookup"><span data-stu-id="42b5c-106">Partner Microsoft Cloud Deutschland tenants won't be migrated.</span></span> <span data-ttu-id="42b5c-107">Au lieu de cela, un nouveau client Office 365 services sera créé pour chaque partenaire Microsoft dans la nouvelle région de centres de données allemande.</span><span class="sxs-lookup"><span data-stu-id="42b5c-107">Instead, a new Office 365 services tenant will be created for each Microsoft Partner in the new German datacenter region.</span></span>

<span data-ttu-id="42b5c-108">Les clients du programme CSP seront migrés vers la nouvelle région de centres de données allemande et liés au nouveau client de services Office 365 du même partenaire.</span><span class="sxs-lookup"><span data-stu-id="42b5c-108">CSP customer tenants will be migrated to the new German datacenter region and be linked to the new Office 365 services tenant of the same partner.</span></span> <span data-ttu-id="42b5c-109">Après la transition du client, le partenaire peut gérer le client à l’aide du nouveau client Office 365 services dans la région du centre de données allemand.</span><span class="sxs-lookup"><span data-stu-id="42b5c-109">After customer transition, the partner can manage the customer using the new Office 365 services tenant in the German datacenter region.</span></span>

## <a name="missing-subscriptions-in-azure"></a><span data-ttu-id="42b5c-110">Abonnements manquants dans Azure</span><span class="sxs-lookup"><span data-stu-id="42b5c-110">Missing subscriptions in Azure</span></span>

<span data-ttu-id="42b5c-111">Une fois la transition des abonnements et des licences [terminée (phase 3),](ms-cloud-germany-transition-phases.md#phase-3-subscription-transfer) les fournisseurs de solutions Cloud n’auront plus accès à l’abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="42b5c-111">After [the subscription and license transition (phase 3)](ms-cloud-germany-transition-phases.md#phase-3-subscription-transfer) has been completed, Cloud Solution Providers will not have access to the Azure subscription anymore.</span></span>

<span data-ttu-id="42b5c-112">Pour récupérer l’accès, suivez ces étapes pour élever [l’accès](/azure/role-based-access-control/elevate-access-global-admin)afin de gérer tous les abonnements Et groupes de gestion Azure.</span><span class="sxs-lookup"><span data-stu-id="42b5c-112">To recover access, follow these steps to [elevate access to manage all Azure subscriptions and management groups](/azure/role-based-access-control/elevate-access-global-admin).</span></span>
