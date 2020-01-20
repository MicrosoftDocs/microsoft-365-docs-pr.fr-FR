---
title: Utiliser l’explorateur d’activité de classification des données
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
ms.openlocfilehash: ab80de0e1be3a164da8414ef3791fb9717bcc190
ms.sourcegitcommit: 48a45b0d2c60d4d79669174f462603a43f272875
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2020
ms.locfileid: "41233695"
---
# <a name="view-activity-on-your-labeled-content-preview"></a><span data-ttu-id="6dc4c-103">Afficher l’activité sur votre contenu étiqueté (aperçu)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-103">View activity on your labeled content (preview)</span></span>

<span data-ttu-id="6dc4c-104">Les onglets vue d’ensemble de la classification des données et explorateur de contenu vous permettent de voir quel contenu a été découvert et étiqueté, ainsi que son emplacement.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-104">The data classification overview and content explorer tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="6dc4c-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="6dc4c-106">L’Explorateur d’activité permet de voir votre historique.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-106">Activity explorer provides a historical view.</span></span>

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](media/data-classification-activity-explorer-1.png)

<span data-ttu-id="6dc4c-108">Vous pouvez filtrer les données par :</span><span class="sxs-lookup"><span data-stu-id="6dc4c-108">You can filter the data by:</span></span>

- <span data-ttu-id="6dc4c-109">plage de dates</span><span class="sxs-lookup"><span data-stu-id="6dc4c-109">date range</span></span>
- <span data-ttu-id="6dc4c-110">type d’activité</span><span class="sxs-lookup"><span data-stu-id="6dc4c-110">activity type</span></span>
- <span data-ttu-id="6dc4c-111">emplacement</span><span class="sxs-lookup"><span data-stu-id="6dc4c-111">location</span></span>
- <span data-ttu-id="6dc4c-112">utilisateur</span><span class="sxs-lookup"><span data-stu-id="6dc4c-112">user</span></span>
- <span data-ttu-id="6dc4c-113">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="6dc4c-113">sensitivity label</span></span>
- <span data-ttu-id="6dc4c-114">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="6dc4c-114">retention label</span></span>


<span data-ttu-id="6dc4c-115">Vous pouvez afficher les données sous la forme d’une liste ou d’un histogramme.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-115">You can view the data either as a list or a bar graph.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6dc4c-116">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="6dc4c-116">Prerequisites</span></span>

<span data-ttu-id="6dc4c-117">Chaque compte accédant et utilisant l’Explorateur d’activités doit posséder une licence pour l’un de ces abonnements :</span><span class="sxs-lookup"><span data-stu-id="6dc4c-117">Every account that accesses and uses activity explorer must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="6dc4c-118">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-118">Microsoft 365 E5</span></span>
- <span data-ttu-id="6dc4c-119">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-119">Office 365 E5</span></span>
- <span data-ttu-id="6dc4c-120">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-120">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="6dc4c-121">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-121">Advanced Threat Intelligence (E5) add-on</span></span>
- <span data-ttu-id="6dc4c-122">Complément Protection avancée contre les menace (E5)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-122">Advanced Threat Protection (E5) add-on</span></span>

## <a name="activity-type"></a><span data-ttu-id="6dc4c-123">Type d’activité</span><span class="sxs-lookup"><span data-stu-id="6dc4c-123">Activity type</span></span>

<span data-ttu-id="6dc4c-124">Microsoft 365 contrôle et signale 12 types d’activités dans SharePoint Online, OneDrive et les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-124">Microsoft 365 monitors and reports on 12 types of activities across SharePoint Online, OneDrive and endpoints.</span></span> <span data-ttu-id="6dc4c-125">Les points de terminaison sont des appareils utilisateur exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-125">Endpoints are user devices running Windows 10.</span></span>

- <span data-ttu-id="6dc4c-126">Fichier créé</span><span class="sxs-lookup"><span data-stu-id="6dc4c-126">File created</span></span>
- <span data-ttu-id="6dc4c-127">Fichier modifié</span><span class="sxs-lookup"><span data-stu-id="6dc4c-127">File modified</span></span>
- <span data-ttu-id="6dc4c-128">Fichier renommé</span><span class="sxs-lookup"><span data-stu-id="6dc4c-128">File renamed</span></span>
- <span data-ttu-id="6dc4c-129">Fichier copié dans le cloud</span><span class="sxs-lookup"><span data-stu-id="6dc4c-129">File copied to cloud</span></span>
- <span data-ttu-id="6dc4c-130">Fichier consulté par une application non autorisée</span><span class="sxs-lookup"><span data-stu-id="6dc4c-130">File accessed by unallowed app</span></span>
- <span data-ttu-id="6dc4c-131">Fichier imprimé</span><span class="sxs-lookup"><span data-stu-id="6dc4c-131">File printed</span></span>
- <span data-ttu-id="6dc4c-132">Fichier copié sur un support amovible</span><span class="sxs-lookup"><span data-stu-id="6dc4c-132">File copied to removable media</span></span>
- <span data-ttu-id="6dc4c-133">Fichier copié sur le partage réseau</span><span class="sxs-lookup"><span data-stu-id="6dc4c-133">File copied to network share</span></span>
- <span data-ttu-id="6dc4c-134">Fichier lu</span><span class="sxs-lookup"><span data-stu-id="6dc4c-134">File read</span></span>
- <span data-ttu-id="6dc4c-135">Fichier copié dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="6dc4c-135">file copied to clipboard</span></span>
- <span data-ttu-id="6dc4c-136">Étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="6dc4c-136">Label applied</span></span>
- <span data-ttu-id="6dc4c-137">Étiquette modifiée (mise à niveau, rétrogradée ou supprimé)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-137">Label changed (upgraded, downgraded, or removed)</span></span>

<span data-ttu-id="6dc4c-138">L’intérêt de comprendre quelles actions sont accomplies avec votre contenu marqué par des étiquettes de confidentialité est de voir si les moyens de contrôle que vous avez déjà mis en place, comme les [stratégies de prévention de perte des données](data-loss-prevention-policies.md) sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-138">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention policies](data-loss-prevention-policies.md) are effective or not.</span></span> <span data-ttu-id="6dc4c-139">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="6dc4c-139">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

<span data-ttu-id="6dc4c-140">Une fois vos filtres définis, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="6dc4c-140">Once your filters are set, you can:</span></span>

- <span data-ttu-id="6dc4c-141">pointer votre curseur sur un segment de l’histogramme pour afficher le nombre d’éléments inclus dans cette catégorie ![pointer sur explorateur d’activités](media/data-classification-activity-explorer-hover-over-2.png)</span><span class="sxs-lookup"><span data-stu-id="6dc4c-141">hover over a segment of the bar chart to see the number of items that fall into that category ![activity explorer hover over](media/data-classification-activity-explorer-hover-over-2.png)</span></span>
- <span data-ttu-id="6dc4c-142">exporter les données</span><span class="sxs-lookup"><span data-stu-id="6dc4c-142">export the data</span></span>
- <span data-ttu-id="6dc4c-143">sélectionner un élément donné dans la liste et afficher les détails de l’action dans le menu volant</span><span class="sxs-lookup"><span data-stu-id="6dc4c-143">select any given item from the list and view the details of the action in the fly-out</span></span>

![Menu volant des détails de l’explorateur d’activités](media/data-classification-activity-explorer-fly-out-3.png)

## <a name="see-also"></a><span data-ttu-id="6dc4c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc4c-145">See also</span></span>
- [<span data-ttu-id="6dc4c-146">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="6dc4c-146">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="6dc4c-147">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="6dc4c-147">Retention labels</span></span>](labels.md)
- [<span data-ttu-id="6dc4c-148">Éléments recherchés par les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="6dc4c-148">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
- [<span data-ttu-id="6dc4c-149">Vue d’ensemble des stratégies de rétention</span><span class="sxs-lookup"><span data-stu-id="6dc4c-149">Overview of retention policies</span></span>](retention-policies.md)