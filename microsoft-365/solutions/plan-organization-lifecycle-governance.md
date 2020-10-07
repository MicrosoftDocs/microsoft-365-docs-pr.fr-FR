---
title: Planification de la gouvernance d’organisation et du cycle de vie pour les groupes Microsoft 365 et Microsoft teams
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
description: Les options de gouvernance du cycle de vie des outils de collaboration dans Microsoft 365
ms.openlocfilehash: 706f1aaecf22c4088d4539c208fef68320c5e710
ms.sourcegitcommit: 9841058fcc95f7c2fed6af92bc3c3686944829b6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2020
ms.locfileid: "48377186"
---
# <a name="plan-organization-and-lifecycle-governance-for-microsoft-365-groups-and-microsoft-teams"></a><span data-ttu-id="11688-103">Planification de la gouvernance d’organisation et du cycle de vie pour les groupes Microsoft 365 et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="11688-103">Plan organization and lifecycle governance for Microsoft 365 groups and Microsoft Teams</span></span>

<span data-ttu-id="11688-104">Les groupes Microsoft 365 disposent d’un ensemble complet d’outils permettant d’implémenter les capacités de gouvernance dont votre organisation a besoin.</span><span class="sxs-lookup"><span data-stu-id="11688-104">Microsoft 365 groups has a rich set of tools to implement the governance capabilities your organization requires.</span></span> 

<span data-ttu-id="11688-105">La section suivante décrit les fonctionnalités, recommande les meilleures pratiques et fournit des instructions pour poser les bonnes questions afin de déterminer les exigences de gouvernance et comment les répondre.</span><span class="sxs-lookup"><span data-stu-id="11688-105">The following section describes the capabilities, recommends best practices, and provides guidance to ask the right questions to determine the requirements for governance, and how to meet them.</span></span>

## <a name="control-who-can-create-microsoft-365-groups"></a><span data-ttu-id="11688-106">Contrôler qui peut créer des groupes Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="11688-106">Control who can create Microsoft 365 groups</span></span>

<span data-ttu-id="11688-107">Les utilisateurs finaux peuvent créer des groupes à partir de plusieurs points de terminaison, dont Outlook, SharePoint, teams et d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="11688-107">Groups can be created by end-users from multiple end-points including Outlook, SharePoint, Teams, and other environments.</span></span>

![Description de l’image](../media/04.png)

<span data-ttu-id="11688-109">Nous vous recommandons vivement de fournir des propriétaires de groupes et d’aider les utilisateurs à effectuer leur travail plus facilement.</span><span class="sxs-lookup"><span data-stu-id="11688-109">We highly recommend self-service to empower group owners and help users get their work done more easily.</span></span> <span data-ttu-id="11688-110">La limitation de la création de groupes et d’équipes peut ralentir la productivité des utilisateurs, car de nombreux services Microsoft 365 nécessitent la création de groupes pour que le service fonctionne.</span><span class="sxs-lookup"><span data-stu-id="11688-110">Limiting group and team creation can slow users productivity because many Microsoft 365 services require that groups be created for the service to function.</span></span>

<span data-ttu-id="11688-111">Envisagez les options de gouvernance suivantes pour la création de groupes :</span><span class="sxs-lookup"><span data-stu-id="11688-111">Consider the following governance options for groups creation:</span></span>

- <span data-ttu-id="11688-112">Pour limiter la prolifération des groupes, utilisez les [stratégies d’expiration des groupes](microsoft-365-groups-expiration-policy.md) pour supprimer automatiquement les groupes qui ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="11688-112">To limit group sprawl, use [groups expiration policies](microsoft-365-groups-expiration-policy.md) to automatically delete groups that are not being used.</span></span>
- <span data-ttu-id="11688-113">Limitez la création de groupes aux membres d’un groupe de [sécurité dont l’appartenance dynamique](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule) contient, par exemple, tous les employés à plein temps.</span><span class="sxs-lookup"><span data-stu-id="11688-113">Limit group creation to members of a [security groups with dynamic membership](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule) containing, for example, all full-time employees.</span></span>
- <span data-ttu-id="11688-114">Limitez la création de groupe à un groupe de sécurité et obligez les utilisateurs à effectuer une formation dans les stratégies d’utilisation de groupe de votre organisation afin de devenir membres du groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="11688-114">Limit group creation to a security group and require users to complete training in your organization's group usage policies in order to become members of the security group.</span></span>

<span data-ttu-id="11688-115">Si vous souhaitez limiter les personnes autorisées à créer des groupes, voir [gérer les personnes autorisées à créer des groupes Microsoft 365](manage-creation-of-groups.md) pour plus d’informations sur la configuration de ce.</span><span class="sxs-lookup"><span data-stu-id="11688-115">If you want to limit who can create groups, see [Manage who can create Microsoft 365 groups](manage-creation-of-groups.md) for information on how to configure this.</span></span>

## <a name="group-delete-restore-and-archiving"></a><span data-ttu-id="11688-116">Suppression, restauration et archivage de groupe</span><span class="sxs-lookup"><span data-stu-id="11688-116">Group delete, restore, and archiving</span></span>

<span data-ttu-id="11688-117">Lorsqu’un groupe Microsoft 365 est supprimé, il est conservé par défaut pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="11688-117">When a Microsoft 365 group is deleted, by default it's retained for 30 days.</span></span> <span data-ttu-id="11688-118">Cette période de 30 jours est appelée « suppression réversible », car vous avez encore la possibilité de le restaurer.</span><span class="sxs-lookup"><span data-stu-id="11688-118">This 30-day period is called "soft-delete" because you can still restore the group.</span></span> <span data-ttu-id="11688-119">Après cette période de 30 jours, le groupe et le contenu associé sont supprimés de manière définitive et ne peuvent plus être restaurés.</span><span class="sxs-lookup"><span data-stu-id="11688-119">After 30 days, the group and associated content is permanently deleted and cannot be restored.</span></span>

<span data-ttu-id="11688-120">Si vous avez des stratégies de rétention en place pour conserver la conversation, les fichiers ou le courrier, ces éléments seront conservés une fois le groupe supprimé.</span><span class="sxs-lookup"><span data-stu-id="11688-120">If you have retention policies in place to retain chat, files, or mail, those items will be preserved after the group is deleted.</span></span> <span data-ttu-id="11688-121">Pour plus d’informations, voir [en savoir plus sur les stratégies de rétention](https://docs.microsoft.com/microsoft-365/compliance/retention-policies) .</span><span class="sxs-lookup"><span data-stu-id="11688-121">See [Learn about retention policies](https://docs.microsoft.com/microsoft-365/compliance/retention-policies) for details.</span></span>

<span data-ttu-id="11688-122">Si vous souhaitez supprimer un groupe tout en conservant le contenu d’un ou plusieurs services connectés à un groupe, reportez-vous à la rubrique [groupes d’archivage, teams et Yammer](end-life-cycle-groups-teams-sites-yammer.md) pour obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="11688-122">If you want to delete a group but preserve the content from one or more of the group-connected services, see [Archive groups, teams, and Yammer](end-life-cycle-groups-teams-sites-yammer.md) for information.</span></span>

## <a name="group-naming-policy"></a><span data-ttu-id="11688-123">Stratégie de noms de groupes</span><span class="sxs-lookup"><span data-stu-id="11688-123">Group naming policy</span></span>

<span data-ttu-id="11688-124">Une stratégie de noms de groupes peut vous aider à gérer les groupes de deux manières :</span><span class="sxs-lookup"><span data-stu-id="11688-124">A groups naming policy can help you govern groups in two ways:</span></span>

- <span data-ttu-id="11688-125">Une stratégie de noms de préfixe/suffixe peut être utilisée pour appliquer des chaînes fixes ou des attributs Azure AD au début ou à la fin d’un nom de groupe et de son adresse de messagerie associée.</span><span class="sxs-lookup"><span data-stu-id="11688-125">A prefix/suffix naming policy can be used to enforce fixed strings or Azure AD attributes at the beginning or end of a group name and its associated email address.</span></span> <span data-ttu-id="11688-126">En procédant ainsi, vous pouvez vous assurer de l’inclusion, par exemple, des noms de service ou des régions dans les noms de groupe.</span><span class="sxs-lookup"><span data-stu-id="11688-126">By doing this, you can ensure the inclusion of, for example, department names or regions in group names.</span></span>
- <span data-ttu-id="11688-127">Une stratégie de mots bloqués permet de s’assurer que certains mots, tels que les noms des cadres, ne sont pas utilisés dans les noms de groupe.</span><span class="sxs-lookup"><span data-stu-id="11688-127">A blocked words policy can ensure that certain words, such as the names of executives, are not used in group names.</span></span>

<span data-ttu-id="11688-128">Les stratégies d’attribution de noms sont appliquées lors de la création de groupes à partir de l’un des services connectés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="11688-128">Naming policies are applied when groups are created from any of the group-connected services.</span></span>

<span data-ttu-id="11688-129">Si vous décidez d’utiliser des stratégies d’attribution de noms pour les groupes, consultez la rubrique [stratégie de noms de groupes Microsoft 365](groups-naming-policy.md).</span><span class="sxs-lookup"><span data-stu-id="11688-129">If you decide to use naming policies for groups, see [Microsoft 365 Groups naming policy](groups-naming-policy.md).</span></span>

## <a name="group-expiration-policy"></a><span data-ttu-id="11688-130">Stratégie d’expiration de groupe</span><span class="sxs-lookup"><span data-stu-id="11688-130">Group expiration policy</span></span>

<span data-ttu-id="11688-131">Vous pouvez spécifier une période d’expiration et tout groupe qui atteint la fin de cette période et qui n’est pas renouvelé, sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="11688-131">You can specify an expiration period and any group that reaches the end of that period, and is not renewed, will be deleted.</span></span> <span data-ttu-id="11688-132">La période d’expiration commence lorsque le groupe est créé, ou à la date à laquelle il a été renouvelé pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="11688-132">The expiration period begins when the group is created, or on the date it was last renewed.</span></span>

<span data-ttu-id="11688-133">Une fois que vous avez défini les groupes pour qu’ils expirent :</span><span class="sxs-lookup"><span data-stu-id="11688-133">Once you set groups to expire:</span></span>
- <span data-ttu-id="11688-134">Les propriétaires du groupe sont invités à renouveler le groupe en tant qu’expiration.</span><span class="sxs-lookup"><span data-stu-id="11688-134">Owners of the group are notified to renew the group as the expiration nears.</span></span>
- <span data-ttu-id="11688-135">Les groupes actifs sont renouvelés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="11688-135">Active groups are renewed automatically.</span></span>
- <span data-ttu-id="11688-136">Tout groupe qui n’est pas renouvelé est supprimé.</span><span class="sxs-lookup"><span data-stu-id="11688-136">Any group that is not renewed is deleted.</span></span>
- <span data-ttu-id="11688-137">Tous les groupes qui sont supprimés peuvent être restaurés dans les 30 jours par les propriétaires du groupe ou l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="11688-137">Any group that is deleted can be restored within 30 days by the group owners or the admin.</span></span>

<span data-ttu-id="11688-138">Les stratégies d’expiration constituent un bon moyen de limiter la prolifération des groupes en s’assurant que les groupes qui ne sont plus utilisés sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="11688-138">Expiration policies are a good way to limit group sprawl by ensuring that groups that are no longer in use are deleted.</span></span> <span data-ttu-id="11688-139">Si vous souhaitez créer une stratégie d’expiration de groupe, consultez la rubrique [Microsoft 365 Group expiration Policy](microsoft-365-groups-expiration-policy.md).</span><span class="sxs-lookup"><span data-stu-id="11688-139">If you want to create a group expiration policy, see [Microsoft 365 Group Expiration Policy](microsoft-365-groups-expiration-policy.md).</span></span>
