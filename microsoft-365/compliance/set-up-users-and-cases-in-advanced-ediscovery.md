---
title: Configurer des utilisateurs et des cas dans Office 365 Advanced eDiscovery
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
description: 'Découvrez comment configurer des rôles d’utilisateur, créer des cas et affecter des utilisateurs à des cas dans Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 754cc7d73fc3325c2525e3101d1378d55afea4de
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601451"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="a6f4d-103">Configurer des utilisateurs et des cas dans Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a6f4d-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="a6f4d-104">Cette rubrique décrit comment configurer des utilisateurs et des cas pour Office 365 Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a6f4d-105">À mesure que nous continuons à investir dans les versions plus récentes de la découverte électronique avancée, nous annonçaons le retrait d’Office 365 Advanced eDiscovery (également appelé *Advanced eDiscovery v 1.0*).</span><span class="sxs-lookup"><span data-stu-id="a6f4d-105">As we continue to invest in newer versions of Advanced eDiscovery, we are announcing the retirement of Office 365 Advanced eDiscovery (also known as *Advanced eDiscovery v1.0*).</span></span> <span data-ttu-id="a6f4d-106">Si vous utilisez toujours Advanced eDiscovery v 1.0, effectuez une transition vers [Advanced eDiscovery v 2.0](overview-ediscovery-20.md) (également appelée *solution eDiscovery avancée dans Microsoft 365*) dès que possible.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-106">If you're still using Advanced eDiscovery v1.0, please transition to [Advanced eDiscovery v2.0](overview-ediscovery-20.md) (also known as the *Advanced eDiscovery solution in Microsoft 365*) as soon as possible.</span></span> <span data-ttu-id="a6f4d-107">Advanced eDiscovery 2,0 contient des fonctionnalités similaires dans Advanced eDiscovery v 1.0, mais offre également de nombreuses nouvelles fonctionnalités telles que la gestion des dépositaires, la gestion des communications et les ensembles de révision.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-107">Advanced eDiscovery 2.0 contains similar functionality found in Advanced eDiscovery v1.0, but also offers many new features such as custodian management, communications management, and review sets.</span></span> <span data-ttu-id="a6f4d-108">Pour en savoir plus sur le retrait de Advanced eDiscovery v 1.0, consultez la rubrique [déclassement des outils eDiscovery hérités](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span><span class="sxs-lookup"><span data-stu-id="a6f4d-108">To learn more about the retirement of Advanced eDiscovery v1.0, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="a6f4d-109">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="a6f4d-109">Prerequisites</span></span>

<span data-ttu-id="a6f4d-110">Avant de configurer des cas et des utilisateurs dans Advanced eDiscovery, les éléments suivants sont requis :</span><span class="sxs-lookup"><span data-stu-id="a6f4d-110">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="a6f4d-111">Pour analyser les données d’un utilisateur à l’aide de Advanced eDiscovery, l’utilisateur (le dépositaire des données) doit disposer d’une licence Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-111">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license.</span></span> <span data-ttu-id="a6f4d-112">Par ailleurs, les utilisateurs disposant d’une licence Office 365 E1 ou E3 peuvent se voir attribuer une licence avancée eDiscovery autonome.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-112">Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license.</span></span> <span data-ttu-id="a6f4d-113">Les administrateurs et les responsables de la mise en conformité qui sont affectés à des cas et utilisent Advanced eDiscovery pour analyser les données n’ont pas besoin d’une licence E5.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-113">Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="a6f4d-114">Vous devez être membre du groupe de rôles gestionnaire de découverte électronique dans le centre de sécurité &amp; conformité Office 365 pour créer un cas eDiscovery et y ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-114">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it.</span></span> <span data-ttu-id="a6f4d-115">Pour vous ajouter au groupe de rôles gestionnaire de découverte électronique &amp; dans le centre de sécurité conformité, vous devez être un administrateur général dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-115">To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization.</span></span> <span data-ttu-id="a6f4d-116">Si vous n’êtes pas un administrateur général, vous devrez demander à un administrateur général de vous ajouter au groupe de rôles gestionnaire de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-116">If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group.</span></span> <span data-ttu-id="a6f4d-117">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="a6f4d-117">For more information, see:</span></span>
    
  - [<span data-ttu-id="a6f4d-118">Autorisations dans le centre de sécurité &amp; conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a6f4d-118">Permissions in the Microsoft 365 Security &amp; Compliance Center</span></span>](~/security/office-365-security/protect-against-threats.md)
    
  - [<span data-ttu-id="a6f4d-119">Attribuer des autorisations eDiscovery dans le centre de &amp; sécurité conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a6f4d-119">Assign eDiscovery permissions in the Microsoft‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="a6f4d-120">Étape 1 : attribuer des autorisations eDiscovery aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a6f4d-120">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="a6f4d-121">La première étape consiste à attribuer aux utilisateurs les autorisations requises dans le &amp; Centre de sécurité conformité afin qu’ils puissent m’ajouter en tant que membre d’un cas eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-121">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case.</span></span> <span data-ttu-id="a6f4d-122">Une fois qu’un utilisateur est ajouté en tant que membre d’un cas &amp; dans le centre de sécurité conformité, il pourra accéder à l’incident dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-122">After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="a6f4d-123">Pour attribuer aux utilisateurs les autorisations nécessaires afin qu’ils puissent être ajoutés en tant que membre d’un cas de découverte électronique, voir l’étape 1 dans [les cas &amp; eDiscovery dans le centre de sécurité conformité de Microsoft 365](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="a6f4d-123">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="a6f4d-124">Étape 2 : créer un cas eDiscovery et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="a6f4d-124">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="a6f4d-125">L’étape suivante consiste à créer un nouveau cas eDiscovery dans le centre &amp; de sécurité et à ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-125">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members.</span></span> <span data-ttu-id="a6f4d-126">Les membres de ce cas seront alors en mesure d’accéder au cas dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-126">Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="a6f4d-127">Pour créer un cas de découverte électronique, voir l’étape 2 dans [cas de découverte électronique dans &amp; le centre de sécurité conformité Microsoft 365](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="a6f4d-127">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="a6f4d-128">Pour ajouter des membres à un cas eDiscovery, reportez-vous à l’étape 3 dans [cas de découverte électronique dans le centre de sécurité &amp; conformité Microsoft 365](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="a6f4d-128">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="a6f4d-129">Étape 3 : passer un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a6f4d-129">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="a6f4d-130">Une fois que vous avez créé un cas eDiscovery et ajouté des membres, vous (ou tout membre du cas) pouvez accéder à la casse correspondante dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="a6f4d-130">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery.</span></span> <span data-ttu-id="a6f4d-131">Pour accéder à un cas dans Advanced eDiscovery, reportez-vous à l’étape 8 dans [les cas de découverte électronique dans le centre de sécurité &amp; conformité Microsoft 365](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="a6f4d-131">To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Microsoft 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6f4d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6f4d-132">See also</span></span>

[<span data-ttu-id="a6f4d-133">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a6f4d-133">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="a6f4d-134">Préparation des données</span><span class="sxs-lookup"><span data-stu-id="a6f4d-134">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
 
