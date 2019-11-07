---
title: Notions de base sur les unités
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:
- commerce
ms.custom: ''
description: En savoir plus sur la nouvelle fonctionnalité unités.
ms.openlocfilehash: 3414fce02844629826edc6d9474f746aa27cfa2e
ms.sourcegitcommit: 3d37043c0447359c952dc99026c219dd69f6fb8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "38012462"
---
# <a name="allotment-basics"></a><span data-ttu-id="97d6d-103">Notions de base sur les unités</span><span class="sxs-lookup"><span data-stu-id="97d6d-103">Allotment basics</span></span>

<span data-ttu-id="97d6d-104">Les allouer des licences vous permettent de définir des limites de licence et de déléguer la gestion de l’attribution de licence uniquement aux limites de produits et de licences que vous sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="97d6d-104">License allotments let you set license limits and delegate management of license assignment to only the products and license limits that you select.</span></span>

<span data-ttu-id="97d6d-105">Les unités utilisent une licence basée sur les groupes pour attribuer des licences à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="97d6d-105">Allotments use group-based licensing to assign licenses to your users.</span></span> <span data-ttu-id="97d6d-106">Les limites de licence fournissent un contrôle supplémentaire sur le nombre de licences attribuées aux utilisateurs de vos groupes.</span><span class="sxs-lookup"><span data-stu-id="97d6d-106">License limits provide added control over how many licenses are assigned to the users in your groups.</span></span> <span data-ttu-id="97d6d-107">Par conséquent, même lorsque vous augmentez le nombre d’utilisateurs de vos groupes, vous pouvez vous assurer que vous respectez la limite de licence que vous avez définie pour votre unité.</span><span class="sxs-lookup"><span data-stu-id="97d6d-107">So even as the number of users in your groups increases, you can ensure that you stay within the license limit that you have set for your allotment.</span></span>

<span data-ttu-id="97d6d-108">Vous pouvez également déléguer la gestion de vos unités.</span><span class="sxs-lookup"><span data-stu-id="97d6d-108">You can also delegate management of your allotments.</span></span> <span data-ttu-id="97d6d-109">Les propriétaires de compartiments délégués ont accès au centre d’administration, mais ils peuvent uniquement voir et gérer les licences dans les unités qu’ils possèdent.</span><span class="sxs-lookup"><span data-stu-id="97d6d-109">Delegated allotment owners gain access to the admin center, but can only see and manage the licenses in the allotments they own.</span></span> <span data-ttu-id="97d6d-110">Cela permet une délégation plus granulaire de la gestion des licences au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="97d6d-110">This provides more granular delegation of license management within your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97d6d-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="97d6d-111">Prerequisites</span></span>

<span data-ttu-id="97d6d-112">Vous devez respecter les exigences en matière de licences pour les [licences basées sur les groupes](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="97d6d-112">You must meet the licensing requirements for [group-based licensing](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal#licensing-requirements).</span></span>

<span data-ttu-id="97d6d-113">Vous pouvez utiliser des unités avec n’importe quel produit Office 365 disponible pour les utilisateurs :</span><span class="sxs-lookup"><span data-stu-id="97d6d-113">You can use allotments with any Office 365 product available to users:</span></span>

- <span data-ttu-id="97d6d-114">Suites Office et produits autonomes</span><span class="sxs-lookup"><span data-stu-id="97d6d-114">Office suites and standalone products</span></span>
- <span data-ttu-id="97d6d-115">Produits d’entreprise et de mobilité</span><span class="sxs-lookup"><span data-stu-id="97d6d-115">Enterprise and Mobility products</span></span>
- <span data-ttu-id="97d6d-116">Produits Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="97d6d-116">Dynamics 365 products</span></span>

<span data-ttu-id="97d6d-117">Les produits suivants ne peuvent pas être utilisés avec des unités :</span><span class="sxs-lookup"><span data-stu-id="97d6d-117">The following products can’t be used with allotments:</span></span>

- <span data-ttu-id="97d6d-118">Applications du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="97d6d-118">Microsoft Store apps</span></span>
- <span data-ttu-id="97d6d-119">Logiciel perpétuel ou logiciel affecté directement à un utilisateur s’il n’y a pas de licence impliquée.</span><span class="sxs-lookup"><span data-stu-id="97d6d-119">Perpetual software, or software that is directly assigned to a user if there is no license involved.</span></span>
- <span data-ttu-id="97d6d-120">Ressources Azure</span><span class="sxs-lookup"><span data-stu-id="97d6d-120">Azure resources</span></span>

<span data-ttu-id="97d6d-121">Vous devez être un administrateur général ou un administrateur de licence pour commencer à utiliser une unité.</span><span class="sxs-lookup"><span data-stu-id="97d6d-121">You must be a global or license admin to get started with an allotment.</span></span>

## <a name="getting-started"></a><span data-ttu-id="97d6d-122">Prise en main</span><span class="sxs-lookup"><span data-stu-id="97d6d-122">Getting started</span></span>

<span data-ttu-id="97d6d-123">La fonctionnalité unités est disponible dans une préversion privée pour un petit nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="97d6d-123">The allotments feature is available in a private preview to only a small number of customers.</span></span> <span data-ttu-id="97d6d-124">Si vous souhaitez rejoindre, veuillez remplir ce formulaire :[https://aka.ms/allotment-pilot-signup](https://aka.ms/allotment-pilot-signup)</span><span class="sxs-lookup"><span data-stu-id="97d6d-124">If you are interested in joining, please fill out this form: [https://aka.ms/allotment-pilot-signup](https://aka.ms/allotment-pilot-signup)</span></span>