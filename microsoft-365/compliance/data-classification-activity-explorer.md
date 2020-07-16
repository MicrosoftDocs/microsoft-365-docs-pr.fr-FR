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
search.appverid:
- MOE150
- MET150
description: L’explorateur d’activité complète les fonctionnalités de classification des données en vous permettant de voir et de filtrer les actions que les utilisateurs effectuent sur votre contenu étiqueté.
ms.openlocfilehash: 63ecb84c0ae658b0fd3463dba10d56059352910b
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45126643"
---
# <a name="get-started-with-activity-explorer"></a><span data-ttu-id="66fd3-103">Prise en main de l’explorateur d’activité</span><span class="sxs-lookup"><span data-stu-id="66fd3-103">Get started with activity explorer</span></span>

<span data-ttu-id="66fd3-104">Les onglets vue d’ensemble de la classification des données et explorateur de contenu vous permettent de voir quel contenu a été découvert et étiqueté, ainsi que son emplacement.</span><span class="sxs-lookup"><span data-stu-id="66fd3-104">The data classification overview and content explorer tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="66fd3-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="66fd3-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="66fd3-106">L’Explorateur d’activité permet de voir votre historique.</span><span class="sxs-lookup"><span data-stu-id="66fd3-106">Activity explorer provides a historical view.</span></span>

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](../media/data-classification-activity-explorer-1.png)

<span data-ttu-id="66fd3-108">Plus de 30 filtres différents sont à votre disposition. Parmi ceux-ci, figurent :</span><span class="sxs-lookup"><span data-stu-id="66fd3-108">There are over 30 different filters available for use, some are:</span></span>

- <span data-ttu-id="66fd3-109">plage de dates</span><span class="sxs-lookup"><span data-stu-id="66fd3-109">date range</span></span>
- <span data-ttu-id="66fd3-110">type d’activité</span><span class="sxs-lookup"><span data-stu-id="66fd3-110">activity type</span></span>
- <span data-ttu-id="66fd3-111">emplacement</span><span class="sxs-lookup"><span data-stu-id="66fd3-111">location</span></span>
- <span data-ttu-id="66fd3-112">utilisateur</span><span class="sxs-lookup"><span data-stu-id="66fd3-112">user</span></span>
- <span data-ttu-id="66fd3-113">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="66fd3-113">sensitivity label</span></span>
- <span data-ttu-id="66fd3-114">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="66fd3-114">retention label</span></span>
- <span data-ttu-id="66fd3-115">chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="66fd3-115">file path</span></span>
- <span data-ttu-id="66fd3-116">Stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="66fd3-116">DLP policy</span></span>


## <a name="prerequisites"></a><span data-ttu-id="66fd3-117">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="66fd3-117">Prerequisites</span></span>

<span data-ttu-id="66fd3-118">Chaque compte qui accède et utilise la classification de données doit posséder une licence pour l’un des abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="66fd3-118">Every account that accesses and uses data classification must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="66fd3-119">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="66fd3-119">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="66fd3-120">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="66fd3-120">Office 365 (E5)</span></span>
- <span data-ttu-id="66fd3-121">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="66fd3-121">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="66fd3-122">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="66fd3-122">Advanced Threat Intelligence (E5) add-on</span></span>

### <a name="permissions"></a><span data-ttu-id="66fd3-123">Autorisations</span><span class="sxs-lookup"><span data-stu-id="66fd3-123">Permissions</span></span>

 <span data-ttu-id="66fd3-124">Pour accéder à l’onglet d’explorateur d’activité, un compte doit être affecté à une appartenance dans l’un de ces rôles ou groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="66fd3-124">In order to get access to the activity explorer tab, an account must be assigned membership in any one of these roles or role groups.</span></span>

<span data-ttu-id="66fd3-125">**Groupes de rôles Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="66fd3-125">**Microsoft 365 role groups**</span></span>

- <span data-ttu-id="66fd3-126">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="66fd3-126">Global administrator</span></span>
- <span data-ttu-id="66fd3-127">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="66fd3-127">Compliance administrator</span></span>
- <span data-ttu-id="66fd3-128">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="66fd3-128">Security administrator</span></span>
- <span data-ttu-id="66fd3-129">Administrateur de conformité des données</span><span class="sxs-lookup"><span data-stu-id="66fd3-129">Compliance data administrator</span></span>

## <a name="activity-type"></a><span data-ttu-id="66fd3-130">Type d’activité</span><span class="sxs-lookup"><span data-stu-id="66fd3-130">Activity type</span></span>

<span data-ttu-id="66fd3-131">Microsoft 365 contrôle et signale les types d’activités dans SharePoint Online, OneDrive, tels que :</span><span class="sxs-lookup"><span data-stu-id="66fd3-131">Microsoft 365 monitors and reports on types of activities across SharePoint Online, and OneDrive like:</span></span>

- <span data-ttu-id="66fd3-132">étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="66fd3-132">label applied</span></span>
- <span data-ttu-id="66fd3-133">étiquette modifiée (mise à niveau, rétrogradée ou supprimée)</span><span class="sxs-lookup"><span data-stu-id="66fd3-133">label changed (upgraded, downgraded, or removed)</span></span>
- <span data-ttu-id="66fd3-134">simulation d’étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="66fd3-134">auto-labeling simulation</span></span>

<span data-ttu-id="66fd3-135">L’intérêt de comprendre quelles actions sont accomplies avec votre contenu marqué par des étiquettes de confidentialité est de voir si les moyens de contrôle que vous avez déjà mis en place, comme les [stratégies de prévention de perte des données](data-loss-prevention-policies.md) sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="66fd3-135">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention policies](data-loss-prevention-policies.md) are effective or not.</span></span> <span data-ttu-id="66fd3-136">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="66fd3-136">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

> [!NOTE]
> <span data-ttu-id="66fd3-137">L’explorateur d’activité ne suit pas actuellement les activités de rétention pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="66fd3-137">Activity explorer doesn't currently monitor retention activities for Exchange Online.</span></span>

## <a name="see-also"></a><span data-ttu-id="66fd3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66fd3-138">See also</span></span>
- [<span data-ttu-id="66fd3-139">En savoir plus sur les étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="66fd3-139">Learn about sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="66fd3-140">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="66fd3-140">Learn about retention policies and retention labels</span></span>](retention.md)
- [<span data-ttu-id="66fd3-141">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="66fd3-141">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

