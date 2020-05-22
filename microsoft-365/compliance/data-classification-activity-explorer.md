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
ms.openlocfilehash: 5cb6a8dbfa570b3b0e0d1ce39648d12050d2af81
ms.sourcegitcommit: f6840dfcfdbcadc53cda591fd6cf9ddcb749d303
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2020
ms.locfileid: "44327840"
---
# <a name="get-started-with-activity-explorer"></a><span data-ttu-id="3a305-103">Prise en main de l’explorateur d’activité</span><span class="sxs-lookup"><span data-stu-id="3a305-103">Get started with activity explorer</span></span>

<span data-ttu-id="3a305-104">Les onglets vue d’ensemble de la classification des données et explorateur de contenu vous permettent de voir quel contenu a été découvert et étiqueté, ainsi que son emplacement.</span><span class="sxs-lookup"><span data-stu-id="3a305-104">The data classification overview and content explorer tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="3a305-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="3a305-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="3a305-106">L’Explorateur d’activité permet de voir votre historique.</span><span class="sxs-lookup"><span data-stu-id="3a305-106">Activity explorer provides a historical view.</span></span>

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](../media/data-classification-activity-explorer-1.png)

<span data-ttu-id="3a305-108">Plus de 30 filtres différents sont à votre disposition. Parmi ceux-ci, figurent :</span><span class="sxs-lookup"><span data-stu-id="3a305-108">There are over 30 different filters available for use, some are:</span></span>

- <span data-ttu-id="3a305-109">plage de dates</span><span class="sxs-lookup"><span data-stu-id="3a305-109">date range</span></span>
- <span data-ttu-id="3a305-110">type d’activité</span><span class="sxs-lookup"><span data-stu-id="3a305-110">activity type</span></span>
- <span data-ttu-id="3a305-111">emplacement</span><span class="sxs-lookup"><span data-stu-id="3a305-111">location</span></span>
- <span data-ttu-id="3a305-112">utilisateur</span><span class="sxs-lookup"><span data-stu-id="3a305-112">user</span></span>
- <span data-ttu-id="3a305-113">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3a305-113">sensitivity label</span></span>
- <span data-ttu-id="3a305-114">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="3a305-114">retention label</span></span>
- <span data-ttu-id="3a305-115">chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="3a305-115">file path</span></span>
- <span data-ttu-id="3a305-116">Stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="3a305-116">DLP policy</span></span>


## <a name="prerequisites"></a><span data-ttu-id="3a305-117">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3a305-117">Prerequisites</span></span>

<span data-ttu-id="3a305-118">Chaque compte accédant et utilisant la classification de données doit posséder une licence pour l’un de abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="3a305-118">Every account that accesses and uses data classification must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="3a305-119">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="3a305-119">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="3a305-120">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="3a305-120">Office 365 (E5)</span></span>
- <span data-ttu-id="3a305-121">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="3a305-121">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="3a305-122">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="3a305-122">Advanced Threat Intelligence (E5) add-on</span></span>

### <a name="permissions"></a><span data-ttu-id="3a305-123">Autorisations</span><span class="sxs-lookup"><span data-stu-id="3a305-123">Permissions</span></span>

 <span data-ttu-id="3a305-124">Pour accéder à l’onglet d’explorateur d’activité, un compte doit être affecté à une appartenance dans l’un de ces rôles ou groupes de rôles.</span><span class="sxs-lookup"><span data-stu-id="3a305-124">In order to get access to the activity explorer tab, an account must be assigned membership in any one of these roles or role groups.</span></span>

<span data-ttu-id="3a305-125">**Groupes de rôles Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="3a305-125">**Microsoft 365 role groups**</span></span>

- <span data-ttu-id="3a305-126">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="3a305-126">Global administrator</span></span>
- <span data-ttu-id="3a305-127">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="3a305-127">Compliance administrator</span></span>
- <span data-ttu-id="3a305-128">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3a305-128">Security administrator</span></span>
- <span data-ttu-id="3a305-129">Administrateur de conformité des données</span><span class="sxs-lookup"><span data-stu-id="3a305-129">Compliance data administrator</span></span>

## <a name="activity-type"></a><span data-ttu-id="3a305-130">Type d’activité</span><span class="sxs-lookup"><span data-stu-id="3a305-130">Activity type</span></span>

<span data-ttu-id="3a305-131">Microsoft 365 contrôle et signale les types d’activités dans SharePoint Online, OneDrive, tels que :</span><span class="sxs-lookup"><span data-stu-id="3a305-131">Microsoft 365 monitors and reports on types of activities across SharePoint Online, and OneDrive like:</span></span>

- <span data-ttu-id="3a305-132">étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="3a305-132">label applied</span></span>
- <span data-ttu-id="3a305-133">étiquette modifiée (mise à niveau, rétrogradée ou supprimée)</span><span class="sxs-lookup"><span data-stu-id="3a305-133">label changed (upgraded, downgraded, or removed)</span></span>
- <span data-ttu-id="3a305-134">simulation d’étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="3a305-134">auto-labeling simulation</span></span>

<span data-ttu-id="3a305-135">L’intérêt de comprendre quelles actions sont accomplies avec votre contenu marqué par des étiquettes de confidentialité est de voir si les moyens de contrôle que vous avez déjà mis en place, comme les [stratégies de prévention de perte des données](data-loss-prevention-policies.md) sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="3a305-135">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention policies](data-loss-prevention-policies.md) are effective or not.</span></span> <span data-ttu-id="3a305-136">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="3a305-136">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

> [!NOTE]
> <span data-ttu-id="3a305-137">L’explorateur d’activité ne suit pas actuellement les activités de rétention pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3a305-137">Activity explorer doesn't currently monitor retention activities for Exchange Online.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a305-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a305-138">See also</span></span>
- [<span data-ttu-id="3a305-139">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="3a305-139">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="3a305-140">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="3a305-140">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="3a305-141">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="3a305-141">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="3a305-142">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="3a305-142">Overview of retention policies</span></span>](retention-policies.md)
