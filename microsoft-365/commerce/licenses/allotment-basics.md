---
title: Informations de base sur l’allotment
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:
- commerce
ms.custom: AdminSurgePortfolio
description: Découvrez la nouvelle fonctionnalité d’allotments.
ms.openlocfilehash: 2ab8efd637bb278faf6065559cab26cb7016975b
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48638230"
---
# <a name="allotment-basics"></a><span data-ttu-id="f17cd-103">Informations de base sur l’allotment</span><span class="sxs-lookup"><span data-stu-id="f17cd-103">Allotment basics</span></span>

<span data-ttu-id="f17cd-104">Les attributions de licence vous permet de définir des limites de licence et de déléguer la gestion de l’attribution de licence uniquement aux produits et licences que vous sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="f17cd-104">License allotments let you set license limits and delegate management of license assignment to only the products and license limits that you select.</span></span>

<span data-ttu-id="f17cd-105">Les affectations utilisent des licences basées sur des groupes pour attribuer des licences à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f17cd-105">Allotments use group-based licensing to assign licenses to your users.</span></span> <span data-ttu-id="f17cd-106">Les limites de licence offrent un contrôle supplémentaire sur le nombre de licences attribuées aux utilisateurs de vos groupes.</span><span class="sxs-lookup"><span data-stu-id="f17cd-106">License limits provide added control over how many licenses are assigned to the users in your groups.</span></span> <span data-ttu-id="f17cd-107">Ainsi, même à mesure que le nombre d’utilisateurs dans vos groupes augmente, vous pouvez vous assurer que vous respectez la limite de licence que vous avez définie pour votre allotment.</span><span class="sxs-lookup"><span data-stu-id="f17cd-107">So even as the number of users in your groups increases, you can ensure that you stay within the license limit that you have set for your allotment.</span></span>

<span data-ttu-id="f17cd-108">Vous pouvez également déléguer la gestion de vos allotments.</span><span class="sxs-lookup"><span data-stu-id="f17cd-108">You can also delegate management of your allotments.</span></span> <span data-ttu-id="f17cd-109">Les propriétaires d’autorisation délégués ont accès au Centre d’administration, mais peuvent uniquement voir et gérer les licences dans les autorisations dont ils sont propriétaires.</span><span class="sxs-lookup"><span data-stu-id="f17cd-109">Delegated allotment owners gain access to the admin center, but can only see and manage the licenses in the allotments they own.</span></span> <span data-ttu-id="f17cd-110">Cela fournit une délégation plus granulaire de la gestion des licences au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f17cd-110">This provides more granular delegation of license management within your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f17cd-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f17cd-111">Prerequisites</span></span>

<span data-ttu-id="f17cd-112">Vous devez respecter les exigences de licence pour [les licences basées sur des groupes.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="f17cd-112">You must meet the licensing requirements for [group-based licensing](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal#licensing-requirements).</span></span>

<span data-ttu-id="f17cd-113">Vous pouvez utiliser des allotments avec n’importe quel produit disponible pour les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="f17cd-113">You can use allotments with any product available to users:</span></span>

- <span data-ttu-id="f17cd-114">Suites Office et produits autonomes</span><span class="sxs-lookup"><span data-stu-id="f17cd-114">Office suites and standalone products</span></span>
- <span data-ttu-id="f17cd-115">Produits Enterprise et Mobility</span><span class="sxs-lookup"><span data-stu-id="f17cd-115">Enterprise and Mobility products</span></span>
- <span data-ttu-id="f17cd-116">Produits Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f17cd-116">Dynamics 365 products</span></span>

<span data-ttu-id="f17cd-117">Les produits suivants ne peuvent pas être utilisés avec des allotments :</span><span class="sxs-lookup"><span data-stu-id="f17cd-117">The following products can't be used with allotments:</span></span>

- <span data-ttu-id="f17cd-118">Applications du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f17cd-118">Microsoft Store apps</span></span>
- <span data-ttu-id="f17cd-119">Logiciels perpétuelles ou logiciels directement attribués à un utilisateur en l’absence de licence.</span><span class="sxs-lookup"><span data-stu-id="f17cd-119">Perpetual software, or software that is directly assigned to a user if there is no license involved.</span></span>
- <span data-ttu-id="f17cd-120">Ressources Azure</span><span class="sxs-lookup"><span data-stu-id="f17cd-120">Azure resources</span></span>

<span data-ttu-id="f17cd-121">Vous devez être un administrateur global ou un administrateur de licence pour prendre en compte une autorisation.</span><span class="sxs-lookup"><span data-stu-id="f17cd-121">You must be a global or license admin to get started with an allotment.</span></span>

## <a name="getting-started"></a><span data-ttu-id="f17cd-122">Prise en main</span><span class="sxs-lookup"><span data-stu-id="f17cd-122">Getting started</span></span>

<span data-ttu-id="f17cd-123">La fonctionnalité d’allotments est disponible en prévisualisation privée uniquement pour un petit nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="f17cd-123">The allotments feature is available in a private preview to only a small number of customers.</span></span> <span data-ttu-id="f17cd-124">Si vous êtes intéressé par la jointation, remplissez ce formulaire : [https://aka.ms/allotment-pilot-signup](https://aka.ms/allotment-pilot-signup) .</span><span class="sxs-lookup"><span data-stu-id="f17cd-124">If you're interested in joining, fill out this form: [https://aka.ms/allotment-pilot-signup](https://aka.ms/allotment-pilot-signup).</span></span>
