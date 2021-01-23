---
title: Prise en main de l’explorateur d’activité
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: L’explorateur d’activité complète les fonctionnalités de classification des données en vous permettant de voir et de filtrer les actions que les utilisateurs effectuent sur votre contenu étiqueté.
ms.openlocfilehash: 6825c00373617011db28fa484f272086f887ea40
ms.sourcegitcommit: 7ecd10b302b3b3dfa4ba3be3a6986dd3c189fbff
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "49921632"
---
# <a name="get-started-with-activity-explorer"></a><span data-ttu-id="3e866-103">Prise en main de l’explorateur d’activité</span><span class="sxs-lookup"><span data-stu-id="3e866-103">Get started with activity explorer</span></span>

<span data-ttu-id="3e866-104">Les onglets vue d’ensemble de la classification des données et explorateur de contenu vous permettent de voir quel contenu a été découvert et étiqueté, ainsi que son emplacement.</span><span class="sxs-lookup"><span data-stu-id="3e866-104">The data classification overview and content explorer tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="3e866-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="3e866-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="3e866-106">L’Explorateur d’activité permet de voir votre historique.</span><span class="sxs-lookup"><span data-stu-id="3e866-106">Activity explorer provides a historical view.</span></span>

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](../media/data-classification-activity-explorer-1.png)

<span data-ttu-id="3e866-108">Plus de 30 filtres différents sont à votre disposition. Parmi ceux-ci, figurent :</span><span class="sxs-lookup"><span data-stu-id="3e866-108">There are over 30 different filters available for use, some are:</span></span>

- <span data-ttu-id="3e866-109">plage de dates</span><span class="sxs-lookup"><span data-stu-id="3e866-109">date range</span></span>
- <span data-ttu-id="3e866-110">type d’activité</span><span class="sxs-lookup"><span data-stu-id="3e866-110">activity type</span></span>
- <span data-ttu-id="3e866-111">emplacement</span><span class="sxs-lookup"><span data-stu-id="3e866-111">location</span></span>
- <span data-ttu-id="3e866-112">utilisateur</span><span class="sxs-lookup"><span data-stu-id="3e866-112">user</span></span>
- <span data-ttu-id="3e866-113">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3e866-113">sensitivity label</span></span>
- <span data-ttu-id="3e866-114">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="3e866-114">retention label</span></span>
- <span data-ttu-id="3e866-115">chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="3e866-115">file path</span></span>
- <span data-ttu-id="3e866-116">Stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="3e866-116">DLP policy</span></span>


## <a name="prerequisites"></a><span data-ttu-id="3e866-117">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3e866-117">Prerequisites</span></span>

<span data-ttu-id="3e866-118">Chaque compte accédant et utilisant la classification de données doit posséder une licence pour l’un de abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="3e866-118">Every account that accesses and uses data classification must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="3e866-119">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="3e866-119">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="3e866-120">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="3e866-120">Office 365 (E5)</span></span>
- <span data-ttu-id="3e866-121">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="3e866-121">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="3e866-122">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="3e866-122">Advanced Threat Intelligence (E5) add-on</span></span>
- <span data-ttu-id="3e866-123">Microsoft 365 E5/A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="3e866-123">Microsoft 365 E5/A5 Info Protection & Governance</span></span>
- <span data-ttu-id="3e866-124">Conformité Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="3e866-124">Microsoft 365 E5/A5 Compliance</span></span>

### <a name="permissions"></a><span data-ttu-id="3e866-125">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3e866-125">Permissions</span></span>

 <span data-ttu-id="3e866-126">Pour accéder à l’onglet d’explorateur d’activité, un compte doit être affecté à une appartenance dans l’un de ces rôles ou groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="3e866-126">In order to get access to the activity explorer tab, an account must be assigned membership in any one of these roles or role groups.</span></span>

<span data-ttu-id="3e866-127">**Groupes de rôles Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="3e866-127">**Microsoft 365 role groups**</span></span>

- <span data-ttu-id="3e866-128">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="3e866-128">Global administrator</span></span>
- <span data-ttu-id="3e866-129">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="3e866-129">Compliance administrator</span></span>
- <span data-ttu-id="3e866-130">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3e866-130">Security administrator</span></span>
- <span data-ttu-id="3e866-131">Administrateur de conformité des données</span><span class="sxs-lookup"><span data-stu-id="3e866-131">Compliance data administrator</span></span>

## <a name="activity-type"></a><span data-ttu-id="3e866-132">Type d’activité</span><span class="sxs-lookup"><span data-stu-id="3e866-132">Activity type</span></span>

<span data-ttu-id="3e866-133">Microsoft 365 contrôle et signale les types d’activités dans SharePoint Online, OneDrive, tels que :</span><span class="sxs-lookup"><span data-stu-id="3e866-133">Microsoft 365 monitors and reports on types of activities across SharePoint Online, and OneDrive like:</span></span>

- <span data-ttu-id="3e866-134">étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="3e866-134">label applied</span></span>
- <span data-ttu-id="3e866-135">étiquette modifiée (mise à niveau, rétrogradée ou supprimée)</span><span class="sxs-lookup"><span data-stu-id="3e866-135">label changed (upgraded, downgraded, or removed)</span></span>
- <span data-ttu-id="3e866-136">simulation d’étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="3e866-136">auto-labeling simulation</span></span>

<span data-ttu-id="3e866-137">L’intérêt de comprendre quelles actions sont accomplies avec votre contenu marqué par des étiquettes de confidentialité est de voir si les moyens de contrôle que vous avez déjà mis en place, comme les [stratégies de prévention de perte des données](data-loss-prevention-policies.md) sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="3e866-137">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention policies](data-loss-prevention-policies.md) are effective or not.</span></span> <span data-ttu-id="3e866-138">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="3e866-138">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

> [!NOTE]
> <span data-ttu-id="3e866-139">L’explorateur d’activité ne suit pas actuellement les activités de rétention pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3e866-139">Activity explorer doesn't currently monitor retention activities for Exchange Online.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e866-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e866-140">See also</span></span>
- [<span data-ttu-id="3e866-141">En savoir plus sur les étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3e866-141">Learn about sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="3e866-142">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="3e866-142">Learn about retention policies and retention labels</span></span>](retention.md)
- [<span data-ttu-id="3e866-143">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="3e866-143">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

