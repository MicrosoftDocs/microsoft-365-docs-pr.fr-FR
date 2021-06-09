---
title: Obstacles à l’information Microsoft 365
description: Découvrez comment configurer les obstacles aux informations dans Microsoft 365.
keywords: Microsoft 365, risques internes, conformité
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
- m365solution-scenario
ms.openlocfilehash: a4c7b711c0a977e0980cd0c72f9369833e9e5c65
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50423595"
---
# <a name="information-barriers-in-microsoft-365"></a><span data-ttu-id="8c76c-104">Obstacles à l’information Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8c76c-104">Information barriers in Microsoft 365</span></span>

<span data-ttu-id="8c76c-105">Microsoft 365 permet la communication et la collaboration entre les groupes et les organisations, et prend en charge les moyens de restreindre la communication et la collaboration entre des groupes spécifiques d’utilisateurs si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8c76c-105">Microsoft 365 enables communication and collaboration across groups and organizations and supports ways to restrict communication and collaboration among specific groups of users when necessary.</span></span> <span data-ttu-id="8c76c-106">Il peut s’agir de situations ou de scénarios dans lesquelles vous souhaitez restreindre la communication et la collaboration entre deux groupes afin d’éviter qu’un conflit d’intérêts ne se produise dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8c76c-106">This may include situations or scenarios where you want to restrict communication and collaboration between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="8c76c-107">Cela peut également inclure des situations dans lesquelles vous devez restreindre la communication et la collaboration entre certaines personnes au sein de votre organisation afin de protéger les informations internes.</span><span class="sxs-lookup"><span data-stu-id="8c76c-107">This may also include situations when you need to restrict communication and collaboration between certain people inside your organization to safeguard internal information.</span></span>

<span data-ttu-id="8c76c-108">Les obstacles aux informations sont pris en charge dans Microsoft Teams, SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8c76c-108">Information barriers are supported in Microsoft Teams, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="8c76c-109">Un administrateur de conformité ou un administrateur des obstacles à l’information peut définir des stratégies pour autoriser ou empêcher les communications entre des groupes d’utilisateurs Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8c76c-109">A compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="8c76c-110">Les stratégies de obstacle à l’information peuvent être utilisées dans des situations comme celles-ci :</span><span class="sxs-lookup"><span data-stu-id="8c76c-110">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="8c76c-111">L’utilisateur du jour ne doit pas communiquer ou partager des fichiers avec l’équipe marketing</span><span class="sxs-lookup"><span data-stu-id="8c76c-111">User in the day trader group should not communicate or share files with the marketing team</span></span>
- <span data-ttu-id="8c76c-112">Le personnel financier travaillant sur des informations confidentielles sur l’entreprise ne doit pas communiquer ou partager des fichiers avec certains groupes au sein de leur organisation</span><span class="sxs-lookup"><span data-stu-id="8c76c-112">Finance personnel working on confidential company information should not communicate or share files with certain groups within their organization</span></span>
- <span data-ttu-id="8c76c-113">Une équipe interne avec du matériel de secret commercial ne doit pas appeler ou discuter en ligne avec des personnes de certains groupes au sein de leur organisation</span><span class="sxs-lookup"><span data-stu-id="8c76c-113">An internal team with trade secret material should not call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="8c76c-114">Une équipe de recherche doit uniquement appeler ou discuter en ligne avec une équipe de développement de produits</span><span class="sxs-lookup"><span data-stu-id="8c76c-114">A research team should only call or chat online with a product development team</span></span>

## <a name="configure-information-barriers-for-microsoft-365"></a><span data-ttu-id="8c76c-115">Configurer les obstacles aux informations pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8c76c-115">Configure information barriers for Microsoft 365</span></span>

<span data-ttu-id="8c76c-116">Pour configurer les obstacles à l’information pour votre organisation, utilisez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c76c-116">Use the following steps to configure information barriers for your organization:</span></span>

![Étapes des obstacles aux informations sur les solutions à risque internes](../media/ir-solution-ib-steps.png)

1. <span data-ttu-id="8c76c-118">En savoir plus [sur les obstacles aux informations](information-barriers.md) dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8c76c-118">Learn about [information barriers](information-barriers.md) in Microsoft 365</span></span>
2. <span data-ttu-id="8c76c-119">Configurer les [conditions préalables et les autorisations](information-barriers-policies.md#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="8c76c-119">Configure [prerequisites and permissions](information-barriers-policies.md#prerequisites)</span></span>
3. <span data-ttu-id="8c76c-120">Segmenter [les utilisateurs de votre organisation](information-barriers-policies.md#part-1-segment-users)</span><span class="sxs-lookup"><span data-stu-id="8c76c-120">Segment [users in your organization](information-barriers-policies.md#part-1-segment-users)</span></span>
4. <span data-ttu-id="8c76c-121">Créer et configurer des stratégies de [obstacle à l’information](information-barriers-policies.md#part-2-define-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="8c76c-121">Create and configure [information barrier policies](information-barriers-policies.md#part-2-define-information-barrier-policies)</span></span>
5. <span data-ttu-id="8c76c-122">Appliquer des [stratégies de obstacle à l’information](information-barriers-policies.md#part-3-apply-information-barrier-policies)</span><span class="sxs-lookup"><span data-stu-id="8c76c-122">Apply [information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies)</span></span>

## <a name="more-information-about-information-barriers"></a><span data-ttu-id="8c76c-123">Plus d’informations sur les obstacles aux informations</span><span class="sxs-lookup"><span data-stu-id="8c76c-123">More information about information barriers</span></span>

- [<span data-ttu-id="8c76c-124">Attributs pour les stratégies d’obstacle aux informations</span><span class="sxs-lookup"><span data-stu-id="8c76c-124">Attributes for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="8c76c-125">Modifier ou supprimer des stratégies de obstacle à l’information</span><span class="sxs-lookup"><span data-stu-id="8c76c-125">Edit or remove information barrier policies</span></span>](information-barriers-edit-segments-policies.md)