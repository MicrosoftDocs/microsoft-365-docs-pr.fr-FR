---
title: Planifier la gouvernance de l’organisation et du cycle de vie Microsoft 365 groupes et Microsoft Teams
ms.reviewer: arvaradh
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-collaboration
- m365solution-collabgovernance
ms.custom:
- M365solutions
f1.keywords: NOCSH
recommendations: false
description: En savoir plus sur les options de gouvernance du cycle de vie pour les outils de collaboration Microsoft 365
ms.openlocfilehash: 7d88618b75ef731bf38df029970efdc05f3eea5a
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52538818"
---
# <a name="plan-organization-and-lifecycle-governance-for-microsoft-365-groups-and-microsoft-teams"></a><span data-ttu-id="a48ef-103">Planifier la gouvernance de l’organisation et du cycle de vie Microsoft 365 groupes et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a48ef-103">Plan organization and lifecycle governance for Microsoft 365 groups and Microsoft Teams</span></span>

<span data-ttu-id="a48ef-104">Microsoft 365 groupes disposent d’un riche ensemble d’outils pour implémenter les fonctionnalités de gouvernance dont votre organisation a besoin.</span><span class="sxs-lookup"><span data-stu-id="a48ef-104">Microsoft 365 groups has a rich set of tools to implement the governance capabilities your organization requires.</span></span> 

<span data-ttu-id="a48ef-105">La section suivante décrit les fonctionnalités, recommande les meilleures pratiques et fournit des conseils pour poser les bonnes questions afin de déterminer les conditions requises pour la gouvernance et comment y répondre.</span><span class="sxs-lookup"><span data-stu-id="a48ef-105">The following section describes the capabilities, recommends best practices, and provides guidance to ask the right questions to determine the requirements for governance, and how to meet them.</span></span>

## <a name="control-who-can-create-microsoft-365-groups"></a><span data-ttu-id="a48ef-106">Contrôler les personnes qui peuvent créer Microsoft 365 groupes</span><span class="sxs-lookup"><span data-stu-id="a48ef-106">Control who can create Microsoft 365 groups</span></span>

<span data-ttu-id="a48ef-107">Les groupes peuvent être créés par les utilisateurs finaux à partir de plusieurs points de fin, notamment Outlook, SharePoint, Teams et d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="a48ef-107">Groups can be created by end-users from multiple end-points including Outlook, SharePoint, Teams, and other environments.</span></span>

![image desc](../media/04.png)

<span data-ttu-id="a48ef-109">Nous vous recommandons vivement le libre-service pour permettre aux propriétaires de groupes et aider les utilisateurs à faire leur travail plus facilement.</span><span class="sxs-lookup"><span data-stu-id="a48ef-109">We highly recommend self-service to empower group owners and help users get their work done more easily.</span></span> <span data-ttu-id="a48ef-110">La limitation de la création de groupes et d’équipes peut ralentir la productivité des utilisateurs, car de nombreux services Microsoft 365 nécessitent que des groupes soient créés pour que le service fonctionne.</span><span class="sxs-lookup"><span data-stu-id="a48ef-110">Limiting group and team creation can slow users productivity because many Microsoft 365 services require that groups be created for the service to function.</span></span>

<span data-ttu-id="a48ef-111">Prenons les options de gouvernance suivantes pour la création de groupes :</span><span class="sxs-lookup"><span data-stu-id="a48ef-111">Consider the following governance options for groups creation:</span></span>

- <span data-ttu-id="a48ef-112">Pour limiter la prolifération des groupes, utilisez des [stratégies d’expiration](microsoft-365-groups-expiration-policy.md) de groupes pour supprimer automatiquement les groupes qui ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="a48ef-112">To limit group sprawl, use [groups expiration policies](microsoft-365-groups-expiration-policy.md) to automatically delete groups that are not being used.</span></span>
- <span data-ttu-id="a48ef-113">Limiter la création de groupes aux membres [d’un](/azure/active-directory/users-groups-roles/groups-create-rule) groupe de sécurité avec une appartenance dynamique contenant, par exemple, tous les employés à plein temps.</span><span class="sxs-lookup"><span data-stu-id="a48ef-113">Limit group creation to members of a [security groups with dynamic membership](/azure/active-directory/users-groups-roles/groups-create-rule) containing, for example, all full-time employees.</span></span>
- <span data-ttu-id="a48ef-114">Limitez la création de groupes à un groupe de sécurité et obligez les utilisateurs à effectuer une formation sur les stratégies d’utilisation des groupes de votre organisation afin de devenir membres du groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a48ef-114">Limit group creation to a security group and require users to complete training in your organization's group usage policies in order to become members of the security group.</span></span>

<span data-ttu-id="a48ef-115">Si vous souhaitez limiter les personnes autorisées à créer des groupes, consultez Gérer les personnes autorisées à créer des groupes Microsoft 365 [pour](manage-creation-of-groups.md) plus d’informations sur la configuration de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="a48ef-115">If you want to limit who can create groups, see [Manage who can create Microsoft 365 groups](manage-creation-of-groups.md) for information on how to configure this.</span></span>

## <a name="group-delete-restore-and-archiving"></a><span data-ttu-id="a48ef-116">Suppression, restauration et archivage de groupes</span><span class="sxs-lookup"><span data-stu-id="a48ef-116">Group delete, restore, and archiving</span></span>

<span data-ttu-id="a48ef-117">Lorsqu’Microsoft 365 groupe est supprimé, il est conservé par défaut pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="a48ef-117">When a Microsoft 365 group is deleted, by default it's retained for 30 days.</span></span> <span data-ttu-id="a48ef-118">Cette période de 30 jours est appelée « suppression réversible », car vous avez encore la possibilité de le restaurer.</span><span class="sxs-lookup"><span data-stu-id="a48ef-118">This 30-day period is called "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="a48ef-119">Après cette période de 30 jours, le groupe et le contenu associé sont supprimés de manière définitive et ne peuvent plus être restaurés.</span><span class="sxs-lookup"><span data-stu-id="a48ef-119">After 30 days, the group and associated content is permanently deleted and cannot be restored.</span></span>

<span data-ttu-id="a48ef-120">Si vous avez des stratégies de rétention en place pour conserver la conversation, les fichiers ou le courrier, ces éléments sont conservés après la suppression du groupe.</span><span class="sxs-lookup"><span data-stu-id="a48ef-120">If you have retention policies in place to retain chat, files, or mail, those items will be preserved after the group is deleted.</span></span> <span data-ttu-id="a48ef-121">Pour plus [d’informations, voir](../compliance/retention.md) En savoir plus sur les stratégies de rétention.</span><span class="sxs-lookup"><span data-stu-id="a48ef-121">See [Learn about retention policies](../compliance/retention.md) for details.</span></span>

<span data-ttu-id="a48ef-122">Si vous souhaitez supprimer un groupe, mais conserver le contenu d’un ou plusieurs services connectés à un groupe, consultez Groupes d’archivage, équipes et [Yammer](end-life-cycle-groups-teams-sites-yammer.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a48ef-122">If you want to delete a group but preserve the content from one or more of the group-connected services, see [Archive groups, teams, and Yammer](end-life-cycle-groups-teams-sites-yammer.md) for information.</span></span>

## <a name="group-naming-policy"></a><span data-ttu-id="a48ef-123">Stratégie de noms de groupes</span><span class="sxs-lookup"><span data-stu-id="a48ef-123">Group naming policy</span></span>

<span data-ttu-id="a48ef-124">Une stratégie de noms de groupes peut vous aider à régir les groupes de deux manières :</span><span class="sxs-lookup"><span data-stu-id="a48ef-124">A groups naming policy can help you govern groups in two ways:</span></span>

- <span data-ttu-id="a48ef-125">Une stratégie de noms de préfixe/suffixe peut être utilisée pour appliquer des chaînes fixes ou des attributs Azure AD au début ou à la fin d’un nom de groupe et de son adresse de messagerie associée.</span><span class="sxs-lookup"><span data-stu-id="a48ef-125">A prefix/suffix naming policy can be used to enforce fixed strings or Azure AD attributes at the beginning or end of a group name and its associated email address.</span></span> <span data-ttu-id="a48ef-126">En faisant cela, vous pouvez garantir l’inclusion, par exemple, des noms de service ou des régions dans les noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="a48ef-126">By doing this, you can ensure the inclusion of, for example, department names or regions in group names.</span></span>
- <span data-ttu-id="a48ef-127">Une stratégie de mots bloqués permet de s’assurer que certains mots, tels que les noms des cadres, ne sont pas utilisés dans les noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="a48ef-127">A blocked words policy can ensure that certain words, such as the names of executives, are not used in group names.</span></span>

<span data-ttu-id="a48ef-128">Les stratégies d’attribution de noms sont appliquées lorsque des groupes sont créés à partir de l’un des services connectés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="a48ef-128">Naming policies are applied when groups are created from any of the group-connected services.</span></span>

<span data-ttu-id="a48ef-129">Si vous décidez d’utiliser des stratégies d’attribution de noms pour les groupes, [voir Microsoft 365 d’attribution de](groups-naming-policy.md)noms de groupes.</span><span class="sxs-lookup"><span data-stu-id="a48ef-129">If you decide to use naming policies for groups, see [Microsoft 365 Groups naming policy](groups-naming-policy.md).</span></span>

## <a name="group-expiration-policy"></a><span data-ttu-id="a48ef-130">Stratégie d’expiration de groupe</span><span class="sxs-lookup"><span data-stu-id="a48ef-130">Group expiration policy</span></span>

<span data-ttu-id="a48ef-131">Vous pouvez spécifier une période d’expiration et tout groupe qui arrive à la fin de cette période et qui n’est pas renouvelé sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="a48ef-131">You can specify an expiration period and any group that reaches the end of that period, and is not renewed, will be deleted.</span></span> <span data-ttu-id="a48ef-132">La période d’expiration commence lors de la création du groupe ou à la date de son dernier renouvellement.</span><span class="sxs-lookup"><span data-stu-id="a48ef-132">The expiration period begins when the group is created, or on the date it was last renewed.</span></span>

<span data-ttu-id="a48ef-133">Une fois que vous avez fixé l’expiration des groupes :</span><span class="sxs-lookup"><span data-stu-id="a48ef-133">Once you set groups to expire:</span></span>
- <span data-ttu-id="a48ef-134">Les propriétaires du groupe sont avertis de renouveler le groupe à mesure que l’expiration approche.</span><span class="sxs-lookup"><span data-stu-id="a48ef-134">Owners of the group are notified to renew the group as the expiration nears.</span></span>
- <span data-ttu-id="a48ef-135">Les groupes actifs sont renouvelés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a48ef-135">Active groups are renewed automatically.</span></span>
- <span data-ttu-id="a48ef-136">Tout groupe qui n’est pas renouvelé est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a48ef-136">Any group that is not renewed is deleted.</span></span>
- <span data-ttu-id="a48ef-137">Tout groupe supprimé peut être restauré dans les 30 jours par les propriétaires du groupe ou l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a48ef-137">Any group that is deleted can be restored within 30 days by the group owners or the admin.</span></span>

<span data-ttu-id="a48ef-138">Les stratégies d’expiration sont un bon moyen de limiter la prolifération des groupes en veillant à ce que les groupes qui ne sont plus utilisés soient supprimés.</span><span class="sxs-lookup"><span data-stu-id="a48ef-138">Expiration policies are a good way to limit group sprawl by ensuring that groups that are no longer in use are deleted.</span></span> <span data-ttu-id="a48ef-139">Si vous souhaitez créer une stratégie d’expiration de groupe, voir [Microsoft 365 stratégie d’expiration de groupe.](microsoft-365-groups-expiration-policy.md)</span><span class="sxs-lookup"><span data-stu-id="a48ef-139">If you want to create a group expiration policy, see [Microsoft 365 Group Expiration Policy](microsoft-365-groups-expiration-policy.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a48ef-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a48ef-140">Related topics</span></span>

[<span data-ttu-id="a48ef-141">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="a48ef-141">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="a48ef-142">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="a48ef-142">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)

[<span data-ttu-id="a48ef-143">Supprimer un ancien employé et sécuriser les données</span><span class="sxs-lookup"><span data-stu-id="a48ef-143">Remove a former employee and secure data</span></span>](/microsoft-365/admin/add-users/remove-former-employee)
