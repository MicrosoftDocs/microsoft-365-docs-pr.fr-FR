---
title: Configurer des utilisateurs et des cas dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: Découvrez comment configurer des rôles d’utilisateur, créer des cas et affecter des utilisateurs à des cas dans Advanced eDiscovery.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8e24354960b517815bef3cf498822d6ce9fd9dbe
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44936741"
---
# <a name="set-up-users-and-cases-in-advanced-ediscovery-classic"></a><span data-ttu-id="d8506-103">Configurer des utilisateurs et des cas dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="d8506-103">Set up users and cases in Advanced eDiscovery (classic)</span></span>

<span data-ttu-id="d8506-104">Cette rubrique décrit comment configurer des utilisateurs et des cas pour Advanced eDiscovery (classique).</span><span class="sxs-lookup"><span data-stu-id="d8506-104">This topic describes how to set up users and cases for Advanced eDiscovery (classic).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d8506-105">Au fur et à mesure que nous investissons dans de nouvelles versions d’Advanced eDiscovery, nous annonçons le retrait d’Advanced eDiscovery, également appelé *Advanced eDiscovery (classique)* ou *Advanced eDiscovery v1.0*.</span><span class="sxs-lookup"><span data-stu-id="d8506-105">As we continue to invest in newer versions of Advanced eDiscovery, we are announcing the retirement of Advanced eDiscovery, also known as *Advanced eDiscovery (classic)* or *Advanced eDiscovery v1.0*.</span></span> <span data-ttu-id="d8506-106">Si vous utilisez Advanced eDiscovery v 1.0, veuillez faire la transition vers [Advanced eDiscovery v2.0](overview-ediscovery-20.md) (également connu sous le nom de *solution eDiscovery avancée dans Microsoft 365*) dès que possible.</span><span class="sxs-lookup"><span data-stu-id="d8506-106">If you're still using Advanced eDiscovery v1.0, please transition to [Advanced eDiscovery v2.0](overview-ediscovery-20.md) (also known as the *Advanced eDiscovery solution in Microsoft 365*) as soon as possible.</span></span> <span data-ttu-id="d8506-107">Advanced eDiscovery 2.0 contient des fonctionnalités similaires à celles de Advanced eDiscovery v1.0, et elle offre également de nombreuses fonctions inédites telles que la gestion des consignataires, la gestion des communications et les jeux à réviser.</span><span class="sxs-lookup"><span data-stu-id="d8506-107">Advanced eDiscovery 2.0 contains similar functionality found in Advanced eDiscovery v1.0, but also offers many new features such as custodian management, communications management, and review sets.</span></span> <span data-ttu-id="d8506-108">Pour en savoir plus sur le retrait d’Advanced eDiscovery v1.0, voir la [Suppression des outils hérités eDiscovery](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span><span class="sxs-lookup"><span data-stu-id="d8506-108">To learn more about the retirement of Advanced eDiscovery v1.0, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span></span> 
  
## <a name="requirements-to-set-up-users-and-cases"></a><span data-ttu-id="d8506-109">Conditions requises pour configurer des utilisateurs et des cas</span><span class="sxs-lookup"><span data-stu-id="d8506-109">Requirements to set up users and cases</span></span>

<span data-ttu-id="d8506-110">Avant de configurer des cas et des utilisateurs dans Advanced eDiscovery, les éléments suivants sont requis :</span><span class="sxs-lookup"><span data-stu-id="d8506-110">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="d8506-111">Pour analyser les données d’un utilisateur à l’aide de Advanced eDiscovery, l’utilisateur (le dépositaire des données) doit disposer d’une licence Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="d8506-111">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license.</span></span> <span data-ttu-id="d8506-112">Par ailleurs, les utilisateurs disposant d’une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome.</span><span class="sxs-lookup"><span data-stu-id="d8506-112">Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license.</span></span> <span data-ttu-id="d8506-113">Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n’ont pas besoin d’une licence E5.</span><span class="sxs-lookup"><span data-stu-id="d8506-113">Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="d8506-114">Vous devez être membre du groupe de rôles gestionnaire eDiscovery dans le centre de sécurité &amp; conformité pour créer un cas eDiscovery et y ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="d8506-114">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to create an eDiscovery case and add members to it.</span></span> <span data-ttu-id="d8506-115">Pour vous ajouter au groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité &amp; conformité, vous devez être un administrateur général de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d8506-115">To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your organization.</span></span> <span data-ttu-id="d8506-116">Si vous n’êtes pas un administrateur général, vous devrez demander à un administrateur général de vous ajouter au groupe de rôles gestionnaire de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="d8506-116">If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group.</span></span> <span data-ttu-id="d8506-117">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="d8506-117">For more information, see:</span></span>
    
  - [<span data-ttu-id="d8506-118">Autorisations dans le centre de sécurité &amp; conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d8506-118">Permissions in the Microsoft 365 Security &amp; Compliance Center</span></span>](~/security/office-365-security/protect-against-threats.md)
    
  - [<span data-ttu-id="d8506-119">Attribuer des autorisations eDiscovery dans le centre de sécurité conformité Microsoft 365 &amp;</span><span class="sxs-lookup"><span data-stu-id="d8506-119">Assign eDiscovery permissions in the Microsoft‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="d8506-120">Étape 1 : attribuer des autorisations eDiscovery aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d8506-120">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="d8506-121">La première étape consiste à attribuer aux utilisateurs les autorisations requises dans le &amp; Centre de sécurité conformité afin qu’ils puissent m’ajouter en tant que membre d’un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d8506-121">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case.</span></span> <span data-ttu-id="d8506-122">Une fois qu’un utilisateur est ajouté en tant que membre d’un cas dans le centre de sécurité &amp; conformité, il pourra accéder à l’incident dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d8506-122">After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="d8506-123">Pour attribuer aux utilisateurs les autorisations nécessaires afin qu’ils puissent être ajoutés en tant que membre d’un cas de découverte électronique, voir l’étape 1 dans [les cas eDiscovery dans le centre de sécurité &amp; conformité de Microsoft 365](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="d8506-123">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="d8506-124">Étape 2 : créer un cas eDiscovery et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="d8506-124">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="d8506-125">L’étape suivante consiste à créer un nouveau cas eDiscovery dans le centre de sécurité & la sécurité et à ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="d8506-125">The next step is to create a new eDiscovery case in the Security & Compliance Center and add members.</span></span> <span data-ttu-id="d8506-126">Les membres de ce cas seront alors en mesure d’accéder au cas dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d8506-126">Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="d8506-127">Pour créer un cas de découverte électronique, voir l’étape 3 dans prise en main de la [découverte électronique principale](get-started-core-ediscovery.md#step-3-create-a-core-ediscovery-case).</span><span class="sxs-lookup"><span data-stu-id="d8506-127">To create a new eDiscovery case, see Step 3 in [Get started with Core eDiscovery](get-started-core-ediscovery.md#step-3-create-a-core-ediscovery-case).</span></span>

2. <span data-ttu-id="d8506-128">Pour ajouter des membres à un cas eDiscovery, reportez-vous à l’étape 4 de prise en main de la [découverte électronique principale](get-started-core-ediscovery.md#step-4-optional-add-members-to-a-core-ediscovery-case)</span><span class="sxs-lookup"><span data-stu-id="d8506-128">To add members to an eDiscovery case, see Step 4 in [Get started with Core eDiscovery](get-started-core-ediscovery.md#step-4-optional-add-members-to-a-core-ediscovery-case)</span></span>

## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="d8506-129">Étape 3 : passer un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d8506-129">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="d8506-130">Une fois que vous avez créé un cas eDiscovery et ajouté des membres, vous (ou tout membre du cas) pouvez accéder à la casse correspondante dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d8506-130">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery.</span></span> <span data-ttu-id="d8506-131">Pour accéder à un cas dans Advanced eDiscovery, reportez-vous à [la rubrique accès à un cas dans Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md#accessing-a-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="d8506-131">To access a case in Advanced eDiscovery, see [Accessing a case in Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md#accessing-a-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d8506-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8506-132">See also</span></span>

[<span data-ttu-id="d8506-133">Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="d8506-133">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d8506-134">Préparation des données pour Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="d8506-134">Preparing data for Advanced eDiscovery (classic)</span></span>](prepare-data-for-advanced-ediscovery.md)
 
