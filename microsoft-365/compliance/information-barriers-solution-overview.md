---
title: Barrières relatives aux informations dans Microsoft 365
description: Découvrez comment configurer des barrières d’informations dans Microsoft 365.
keywords: Microsoft 365, Risk Insider, conformité
localization_priority: Normal
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- m365-security-compliance
- m365solution-insiderrisk
- m365initiative-compliance
ms.openlocfilehash: 74a5b557ae610f8d008ad9d43bd2ccac43179131
ms.sourcegitcommit: a0cddd1f888edb940717e434cda2dbe62e5e9475
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "49613780"
---
# <a name="information-barriers-in-microsoft-365"></a><span data-ttu-id="1156d-104">Barrières relatives aux informations dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1156d-104">Information barriers in Microsoft 365</span></span>

<span data-ttu-id="1156d-105">Microsoft 365 permet la communication et la collaboration entre les groupes et les organisations et prend en charge des moyens de restreindre la communication et la collaboration entre des groupes d’utilisateurs spécifiques lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1156d-105">Microsoft 365 enables communication and collaboration across groups and organizations and supports ways to restrict communication and collaboration among specific groups of users when necessary.</span></span> <span data-ttu-id="1156d-106">Cela peut inclure des situations ou des scénarios dans lesquels vous souhaitez restreindre la communication et la collaboration entre deux groupes afin d’éviter un conflit d’intérêts au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1156d-106">This may include situations or scenarios where you want to restrict communication and collaboration between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="1156d-107">Cela peut également inclure des situations dans lesquelles vous devez restreindre la communication et la collaboration entre certaines personnes au sein de votre organisation afin de protéger les informations internes.</span><span class="sxs-lookup"><span data-stu-id="1156d-107">This may also include situations when you need to restrict communication and collaboration between certain people inside your organization to safeguard internal information.</span></span>

<span data-ttu-id="1156d-108">Les barrières d’informations sont prises en charge dans Microsoft Teams, SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="1156d-108">Information barriers are supported in Microsoft Teams, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="1156d-109">Un administrateur de conformité ou un administrateur des barrières de l’information peut définir des stratégies pour autoriser ou empêcher les communications entre les groupes d’utilisateurs dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1156d-109">A compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="1156d-110">Les stratégies de barrière des informations peuvent être utilisées pour des situations comme celles-ci :</span><span class="sxs-lookup"><span data-stu-id="1156d-110">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="1156d-111">L’utilisateur dans le groupe de la journée du commerçant ne doit pas communiquer ou partager des fichiers avec l’équipe marketing</span><span class="sxs-lookup"><span data-stu-id="1156d-111">User in the day trader group should not communicate or share files with the marketing team</span></span>
- <span data-ttu-id="1156d-112">Le personnel financier travaillant sur les informations confidentielles de l’entreprise ne doit pas communiquer ou partager des fichiers avec certains groupes au sein de son organisation</span><span class="sxs-lookup"><span data-stu-id="1156d-112">Finance personnel working on confidential company information should not communicate or share files with certain groups within their organization</span></span>
- <span data-ttu-id="1156d-113">Une équipe interne avec des éléments secrets commerciaux ne doit pas appeler ou converser en ligne avec des personnes appartenant à certains groupes au sein de leur organisation</span><span class="sxs-lookup"><span data-stu-id="1156d-113">An internal team with trade secret material should not call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="1156d-114">Une équipe de recherche doit uniquement appeler ou converser en ligne avec une équipe de développement de produit</span><span class="sxs-lookup"><span data-stu-id="1156d-114">A research team should only call or chat online with a product development team</span></span>

## <a name="configure-information-barriers-for-microsoft-365"></a><span data-ttu-id="1156d-115">Configurer les barrières relatives à l’information pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1156d-115">Configure information barriers for Microsoft 365</span></span>

<span data-ttu-id="1156d-116">Procédez comme suit pour configurer les barrières d’information pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="1156d-116">Use the following steps to configure information barriers for your organization:</span></span>

![Informations sur la solution des risques initiés](../media/ir-solution-ib-steps.png)

1. <span data-ttu-id="1156d-118">En savoir plus sur les [barrières relatives aux informations](information-barriers.md) dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1156d-118">Learn about [information barriers](information-barriers.md) in Microsoft 365</span></span>
2. <span data-ttu-id="1156d-119">Configurer [les conditions préalables et les autorisations](information-barriers-policies.md#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="1156d-119">Configure [prerequisites and permissions](information-barriers-policies.md#prerequisites)</span></span>
3. <span data-ttu-id="1156d-120">Segmenter [les utilisateurs de votre organisation](information-barriers-policies.md#part-1-segment-users)</span><span class="sxs-lookup"><span data-stu-id="1156d-120">Segment [users in your organization](information-barriers-policies.md#part-1-segment-users)</span></span>
4. <span data-ttu-id="1156d-121">Créer et configurer des [stratégies de barrière des informations](information-barriers-policies.md#part-2-define-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="1156d-121">Create and configure [information barrier policies](information-barriers-policies.md#part-2-define-information-barrier-policies)</span></span>
5. <span data-ttu-id="1156d-122">Appliquer des [stratégies de barrière des informations](information-barriers-policies.md#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="1156d-122">Apply [information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies)</span></span>

## <a name="more-information-about-information-barriers"></a><span data-ttu-id="1156d-123">Plus d’informations sur les barrières des informations</span><span class="sxs-lookup"><span data-stu-id="1156d-123">More information about information barriers</span></span>

- [<span data-ttu-id="1156d-124">Attributs pour les stratégies d’obstacle aux informations</span><span class="sxs-lookup"><span data-stu-id="1156d-124">Attributes for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="1156d-125">Modifier ou supprimer des stratégies de barrière des informations</span><span class="sxs-lookup"><span data-stu-id="1156d-125">Edit or remove information barrier policies</span></span>](information-barriers-edit-segments-policies.md)