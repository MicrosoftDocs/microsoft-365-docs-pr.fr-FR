---
title: Utiliser l’explorateur d’activité de classification des données
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
ms.openlocfilehash: f80ce94433028b2434d442a364c336060b730d94
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42076760"
---
# <a name="view-activity-on-your-labeled-content-preview"></a><span data-ttu-id="80ec5-103">Afficher l’activité sur votre contenu étiqueté (aperçu)</span><span class="sxs-lookup"><span data-stu-id="80ec5-103">View activity on your labeled content (preview)</span></span>

<span data-ttu-id="80ec5-104">Les onglets vue d’ensemble de la classification des données et explorateur de contenu vous permettent de voir quel contenu a été découvert et étiqueté, ainsi que son emplacement.</span><span class="sxs-lookup"><span data-stu-id="80ec5-104">The data classification overview and content explorer tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="80ec5-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="80ec5-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="80ec5-106">L’Explorateur d’activité permet de voir votre historique.</span><span class="sxs-lookup"><span data-stu-id="80ec5-106">Activity explorer provides a historical view.</span></span>

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](../media/data-classification-activity-explorer-1.png)

<span data-ttu-id="80ec5-108">Vous pouvez filtrer les données par :</span><span class="sxs-lookup"><span data-stu-id="80ec5-108">You can filter the data by:</span></span>

- <span data-ttu-id="80ec5-109">plage de dates</span><span class="sxs-lookup"><span data-stu-id="80ec5-109">date range</span></span>
- <span data-ttu-id="80ec5-110">type d’activité</span><span class="sxs-lookup"><span data-stu-id="80ec5-110">activity type</span></span>
- <span data-ttu-id="80ec5-111">emplacement</span><span class="sxs-lookup"><span data-stu-id="80ec5-111">location</span></span>
- <span data-ttu-id="80ec5-112">utilisateur</span><span class="sxs-lookup"><span data-stu-id="80ec5-112">user</span></span>
- <span data-ttu-id="80ec5-113">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="80ec5-113">sensitivity label</span></span>
- <span data-ttu-id="80ec5-114">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="80ec5-114">retention label</span></span>


<span data-ttu-id="80ec5-115">Vous pouvez afficher les données sous la forme d’une liste ou d’un histogramme.</span><span class="sxs-lookup"><span data-stu-id="80ec5-115">You can view the data either as a list or a bar graph.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="80ec5-116">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="80ec5-116">Prerequisites</span></span>

<span data-ttu-id="80ec5-117">Chaque compte accédant et utilisant l’Explorateur d’activités doit posséder une licence pour l’un de ces abonnements :</span><span class="sxs-lookup"><span data-stu-id="80ec5-117">Every account that accesses and uses activity explorer must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="80ec5-118">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="80ec5-118">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="80ec5-119">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="80ec5-119">Office 365 (E5)</span></span>
- <span data-ttu-id="80ec5-120">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="80ec5-120">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="80ec5-121">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="80ec5-121">Advanced Threat Intelligence (E5) add-on</span></span>

## <a name="activity-type"></a><span data-ttu-id="80ec5-122">Type d’activité</span><span class="sxs-lookup"><span data-stu-id="80ec5-122">Activity type</span></span>

<span data-ttu-id="80ec5-123">Microsoft 365 contrôle et signale 12 types d’activités dans SharePoint Online, OneDrive et les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="80ec5-123">Microsoft 365 monitors and reports on 12 types of activities across SharePoint Online, OneDrive and endpoints.</span></span> <span data-ttu-id="80ec5-124">Les points de terminaison sont des appareils utilisateur exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="80ec5-124">Endpoints are user devices running Windows 10.</span></span>

- <span data-ttu-id="80ec5-125">Fichier créé</span><span class="sxs-lookup"><span data-stu-id="80ec5-125">File created</span></span>
- <span data-ttu-id="80ec5-126">Fichier modifié</span><span class="sxs-lookup"><span data-stu-id="80ec5-126">File modified</span></span>
- <span data-ttu-id="80ec5-127">Fichier renommé</span><span class="sxs-lookup"><span data-stu-id="80ec5-127">File renamed</span></span>
- <span data-ttu-id="80ec5-128">Fichier copié dans le cloud</span><span class="sxs-lookup"><span data-stu-id="80ec5-128">File copied to cloud</span></span>
- <span data-ttu-id="80ec5-129">Fichier consulté par une application non autorisée</span><span class="sxs-lookup"><span data-stu-id="80ec5-129">File accessed by unallowed app</span></span>
- <span data-ttu-id="80ec5-130">Fichier imprimé</span><span class="sxs-lookup"><span data-stu-id="80ec5-130">File printed</span></span>
- <span data-ttu-id="80ec5-131">Fichier copié sur un support amovible</span><span class="sxs-lookup"><span data-stu-id="80ec5-131">File copied to removable media</span></span>
- <span data-ttu-id="80ec5-132">Fichier copié sur le partage réseau</span><span class="sxs-lookup"><span data-stu-id="80ec5-132">File copied to network share</span></span>
- <span data-ttu-id="80ec5-133">Fichier lu</span><span class="sxs-lookup"><span data-stu-id="80ec5-133">File read</span></span>
- <span data-ttu-id="80ec5-134">Fichier copié dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="80ec5-134">file copied to clipboard</span></span>
- <span data-ttu-id="80ec5-135">Étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="80ec5-135">Label applied</span></span>
- <span data-ttu-id="80ec5-136">Étiquette modifiée (mise à niveau, rétrogradée ou supprimé)</span><span class="sxs-lookup"><span data-stu-id="80ec5-136">Label changed (upgraded, downgraded, or removed)</span></span>

<span data-ttu-id="80ec5-137">L’intérêt de comprendre quelles actions sont accomplies avec votre contenu marqué par des étiquettes de confidentialité est de voir si les moyens de contrôle que vous avez déjà mis en place, comme les [stratégies de prévention de perte des données](data-loss-prevention-policies.md) sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="80ec5-137">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention policies](data-loss-prevention-policies.md) are effective or not.</span></span> <span data-ttu-id="80ec5-138">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="80ec5-138">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

<span data-ttu-id="80ec5-139">Une fois vos filtres définis, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="80ec5-139">Once your filters are set, you can:</span></span>

- <span data-ttu-id="80ec5-140">pointer votre curseur sur un segment de l’histogramme pour afficher le nombre d’éléments inclus dans cette catégorie ![pointer sur explorateur d’activités](../media/data-classification-activity-explorer-hover-over-2.png)</span><span class="sxs-lookup"><span data-stu-id="80ec5-140">hover over a segment of the bar chart to see the number of items that fall into that category ![activity explorer hover over](../media/data-classification-activity-explorer-hover-over-2.png)</span></span>
- <span data-ttu-id="80ec5-141">exporter les données</span><span class="sxs-lookup"><span data-stu-id="80ec5-141">export the data</span></span>
- <span data-ttu-id="80ec5-142">sélectionner un élément donné dans la liste et afficher les détails de l’action dans le menu volant</span><span class="sxs-lookup"><span data-stu-id="80ec5-142">select any given item from the list and view the details of the action in the fly-out</span></span>

![Menu volant des détails de l’explorateur d’activités](../media/data-classification-activity-explorer-fly-out-3.png)

## <a name="see-also"></a><span data-ttu-id="80ec5-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80ec5-144">See also</span></span>
- [<span data-ttu-id="80ec5-145">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="80ec5-145">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="80ec5-146">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="80ec5-146">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="80ec5-147">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="80ec5-147">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="80ec5-148">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="80ec5-148">Overview of retention policies</span></span>](retention-policies.md)
