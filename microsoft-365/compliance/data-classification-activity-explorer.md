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
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: L’explorateur d’activité complète les fonctionnalités de classification des données en vous permettant de voir et de filtrer les actions que les utilisateurs effectuent sur votre contenu étiqueté.
ms.openlocfilehash: 414ef4e5d9f6472180a5eaef391d3eba33463b02
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114006"
---
# <a name="get-started-with-activity-explorer"></a><span data-ttu-id="f9afe-103">Prise en main de l’explorateur d’activité</span><span class="sxs-lookup"><span data-stu-id="f9afe-103">Get started with activity explorer</span></span>

<span data-ttu-id="f9afe-104">La [vue d’ensemble](data-classification-overview.md) de la classification des données et les onglets de l’Explorateur de contenu vous donnent une visibilité sur le contenu qui a été découvert et étiqueté, ainsi que sur l’endroit où il se trouve. [](data-classification-content-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="f9afe-104">The [data classification overview](data-classification-overview.md) and [content explorer](data-classification-content-explorer.md) tabs give you visibility into what content has been discovered and labeled, and where that content is.</span></span> <span data-ttu-id="f9afe-105">L’explorateur d’activité complète cette suite de fonctionnalités en vous permettant de contrôler les opérations effectuées avec votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="f9afe-105">Activity explorer rounds out this suite of functionality by allowing you to monitor what's being done with your labeled content.</span></span> <span data-ttu-id="f9afe-106">L’Explorateur d’activités fournit un affichage historique des activités sur votre contenu étiqueté.</span><span class="sxs-lookup"><span data-stu-id="f9afe-106">Activity explorer provides a historical view of activities on your labeled content.</span></span> <span data-ttu-id="f9afe-107">Les informations d’activité sont collectées à partir Microsoft 365 journaux d’audit unifiés, transformées et disponibles dans l’interface utilisateur de l’Explorateur d’activités.</span><span class="sxs-lookup"><span data-stu-id="f9afe-107">The activity information is collected from the Microsoft 365 unified audit logs, transformed and made available in the Activity explorer UI.</span></span> 

![emplacement réservé pour la capture d’écran aperçu de l’explorateur d’activité](../media/data-classification-activity-explorer-1.png)

<span data-ttu-id="f9afe-109">Plus de 30 filtres différents sont à votre disposition. Parmi ceux-ci, figurent :</span><span class="sxs-lookup"><span data-stu-id="f9afe-109">There are over 30 different filters available for use, some are:</span></span>

- <span data-ttu-id="f9afe-110">plage de dates</span><span class="sxs-lookup"><span data-stu-id="f9afe-110">date range</span></span>
- <span data-ttu-id="f9afe-111">type d’activité</span><span class="sxs-lookup"><span data-stu-id="f9afe-111">activity type</span></span>
- <span data-ttu-id="f9afe-112">emplacement</span><span class="sxs-lookup"><span data-stu-id="f9afe-112">location</span></span>
- <span data-ttu-id="f9afe-113">utilisateur</span><span class="sxs-lookup"><span data-stu-id="f9afe-113">user</span></span>
- <span data-ttu-id="f9afe-114">étiquette de confidentialité</span><span class="sxs-lookup"><span data-stu-id="f9afe-114">sensitivity label</span></span>
- <span data-ttu-id="f9afe-115">étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="f9afe-115">retention label</span></span>
- <span data-ttu-id="f9afe-116">chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="f9afe-116">file path</span></span>
- <span data-ttu-id="f9afe-117">Stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="f9afe-117">DLP policy</span></span>



## <a name="prerequisites"></a><span data-ttu-id="f9afe-118">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f9afe-118">Prerequisites</span></span>

<span data-ttu-id="f9afe-119">Chaque compte qui accède et utilise la classification de données doit posséder une licence pour l’un des abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="f9afe-119">Every account that accesses and uses data classification must have a license assigned to it from one of these subscriptions:</span></span>

- <span data-ttu-id="f9afe-120">Microsoft 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="f9afe-120">Microsoft 365 (E5)</span></span>
- <span data-ttu-id="f9afe-121">Office 365 (E5)</span><span class="sxs-lookup"><span data-stu-id="f9afe-121">Office 365 (E5)</span></span>
- <span data-ttu-id="f9afe-122">Complément Conformité avancée (E5)</span><span class="sxs-lookup"><span data-stu-id="f9afe-122">Advanced Compliance (E5) add-on</span></span>
- <span data-ttu-id="f9afe-123">Complément Threat Intelligence avancé (E5)</span><span class="sxs-lookup"><span data-stu-id="f9afe-123">Advanced Threat Intelligence (E5) add-on</span></span>
- <span data-ttu-id="f9afe-124">Microsoft 365 E5/A5, Protection des informations et gouvernance</span><span class="sxs-lookup"><span data-stu-id="f9afe-124">Microsoft 365 E5/A5 Info Protection & Governance</span></span>
- <span data-ttu-id="f9afe-125">Conformité Microsoft 365 E5/A5</span><span class="sxs-lookup"><span data-stu-id="f9afe-125">Microsoft 365 E5/A5 Compliance</span></span>

### <a name="permissions"></a><span data-ttu-id="f9afe-126">Autorisations</span><span class="sxs-lookup"><span data-stu-id="f9afe-126">Permissions</span></span>

 <span data-ttu-id="f9afe-127">Pour accéder à l’onglet Explorateur d’activités, un compte doit être explicitement affecté à l’un de ces groupes de rôles ou avoir reçu explicitement le rôle.</span><span class="sxs-lookup"><span data-stu-id="f9afe-127">In order to get access to the activity explorer tab, an account must be explicitly assigned membership in any one of these role groups or explicitly granted the role.</span></span>

<!--
> [!IMPORTANT]
> Access to Activity explorer via the Security reader or Device Management role groups or other has been removed-->

<span data-ttu-id="f9afe-128">**Groupes de rôles Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="f9afe-128">**Microsoft 365 role groups**</span></span>

- <span data-ttu-id="f9afe-129">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="f9afe-129">Global administrator</span></span>
- <span data-ttu-id="f9afe-130">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="f9afe-130">Compliance administrator</span></span>
- <span data-ttu-id="f9afe-131">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f9afe-131">Security administrator</span></span>
- <span data-ttu-id="f9afe-132">Administrateur des données de conformité</span><span class="sxs-lookup"><span data-stu-id="f9afe-132">Compliance data administrator</span></span>

<span data-ttu-id="f9afe-133">**Microsoft 365 rôles**</span><span class="sxs-lookup"><span data-stu-id="f9afe-133">**Microsoft 365 roles**</span></span>

- <span data-ttu-id="f9afe-134">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="f9afe-134">Compliance administrator</span></span>
- <span data-ttu-id="f9afe-135">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f9afe-135">Security administrator</span></span>

## <a name="activity-types"></a><span data-ttu-id="f9afe-136">Types d’activité</span><span class="sxs-lookup"><span data-stu-id="f9afe-136">Activity types</span></span>

<span data-ttu-id="f9afe-137">L’Explorateur d’activités collecte des informations d’activité à partir des journaux d’audit sur plusieurs sources d’activités.</span><span class="sxs-lookup"><span data-stu-id="f9afe-137">Activity explorer gathers activity information from the audit logs on multiple sources of activities.</span></span> <span data-ttu-id="f9afe-138">Pour plus d’informations sur l’activité d’étiquetage dans l’Explorateur d’activités, voir événements [d’étiquetage disponibles dans l’Explorateur d’activités.](data-classification-activity-explorer-available-events.md)</span><span class="sxs-lookup"><span data-stu-id="f9afe-138">For more detailed information on what labeling activity makes it to Activity explorer, see [Labeling events available in Activity explorer](data-classification-activity-explorer-available-events.md).</span></span>

<span data-ttu-id="f9afe-139"> Activités des étiquettes  de niveau de sensibilité et activités d’étiquetage de rétention à partir d’applications natives Office, d’un add-in Azure Information Protection, de SharePoint Online, d’Exchange Online (étiquettes de sensibilité uniquement) et de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f9afe-139">**Sensitivity label activities** and **Retention labeling activities** from Office native applications, Azure Information Protection add-in, SharePoint Online, Exchange Online (sensitivity labels only) and OneDrive.</span></span> <span data-ttu-id="f9afe-140">En voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="f9afe-140">Some examples are:</span></span>

- <span data-ttu-id="f9afe-141">étiquette appliqué</span><span class="sxs-lookup"><span data-stu-id="f9afe-141">label applied</span></span>
- <span data-ttu-id="f9afe-142">étiquette modifiée (mise à niveau, rétrogradée ou supprimée)</span><span class="sxs-lookup"><span data-stu-id="f9afe-142">label changed (upgraded, downgraded, or removed)</span></span>
- <span data-ttu-id="f9afe-143">simulation d’étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="f9afe-143">auto-labeling simulation</span></span>
- <span data-ttu-id="f9afe-144">lecture de fichier</span><span class="sxs-lookup"><span data-stu-id="f9afe-144">file read</span></span> 

<span data-ttu-id="f9afe-145">**Scanneur Azure Information Protection (AIP) et clients AIP**</span><span class="sxs-lookup"><span data-stu-id="f9afe-145">**Azure Information Protection (AIP) scanner and AIP clients**</span></span>

- <span data-ttu-id="f9afe-146">protection appliquée</span><span class="sxs-lookup"><span data-stu-id="f9afe-146">protection applied</span></span>
- <span data-ttu-id="f9afe-147">protection modifiée</span><span class="sxs-lookup"><span data-stu-id="f9afe-147">protection changed</span></span>
- <span data-ttu-id="f9afe-148">protection supprimée</span><span class="sxs-lookup"><span data-stu-id="f9afe-148">protection removed</span></span>
- <span data-ttu-id="f9afe-149">fichiers découverts</span><span class="sxs-lookup"><span data-stu-id="f9afe-149">files discovered</span></span> 

<span data-ttu-id="f9afe-150">L’Explorateur d’activités rassemble également la stratégie **DLP** qui correspond aux événements provenant de Exchange Online, SharePoint Online, OneDrive, Teams Chat et Canal (prévisualisation), des dossiers et bibliothèques SharePoint locaux, des partages de fichiers locaux et des appareils Windows 10 via la protection contre la perte de données **(DLP)** de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f9afe-150">Activity explorer also gathers **DLP policy matches** events from Exchange Online, SharePoint Online, OneDrive, Teams Chat and Channel (preview), on-premises SharePoint folders and libraries, and on-premises file shares, and Windows 10 devices via **Endpoint data loss prevention (DLP)**.</span></span> <span data-ttu-id="f9afe-151">Voici quelques exemples d’événements Windows 10 appareils mobiles :</span><span class="sxs-lookup"><span data-stu-id="f9afe-151">Some examples events from Windows 10 devices are file:</span></span>

- <span data-ttu-id="f9afe-152">suppressions</span><span class="sxs-lookup"><span data-stu-id="f9afe-152">deletions</span></span>
- <span data-ttu-id="f9afe-153">creations</span><span class="sxs-lookup"><span data-stu-id="f9afe-153">creations</span></span>
- <span data-ttu-id="f9afe-154">copié dans le Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="f9afe-154">copied to clipboard</span></span>
- <span data-ttu-id="f9afe-155">modifié</span><span class="sxs-lookup"><span data-stu-id="f9afe-155">modified</span></span>
- <span data-ttu-id="f9afe-156">read</span><span class="sxs-lookup"><span data-stu-id="f9afe-156">read</span></span>
- <span data-ttu-id="f9afe-157">imprimé</span><span class="sxs-lookup"><span data-stu-id="f9afe-157">printed</span></span>
- <span data-ttu-id="f9afe-158">renommé</span><span class="sxs-lookup"><span data-stu-id="f9afe-158">renamed</span></span>
- <span data-ttu-id="f9afe-159">copié sur le partage réseau</span><span class="sxs-lookup"><span data-stu-id="f9afe-159">copied to network share</span></span>
- <span data-ttu-id="f9afe-160">accès par une application non autorisé</span><span class="sxs-lookup"><span data-stu-id="f9afe-160">accessed by unallowed app</span></span> 

<span data-ttu-id="f9afe-161">L’intérêt de comprendre quelles actions sont prises avec votre contenu étiqueté sensible est que vous [](dlp-learn-about-dlp.md) pouvez voir si les contrôles que vous avez déjà mis en place, tels que la protection contre la perte de données, sont efficaces ou non.</span><span class="sxs-lookup"><span data-stu-id="f9afe-161">The value of understanding what actions are being taken with your sensitive labeled content is that you can see if the controls that you have already put into place, such as [data loss prevention](dlp-learn-about-dlp.md) are effective or not.</span></span> <span data-ttu-id="f9afe-162">Si ce n’est pas le cas ou si vous découvrez quelque chose d’inattendu tel qu’un grand nombre d’éléments qui sont étiquetés `highly confidential`et sont rétrogradés`general` vous pouvez gérer vos différentes stratégies et entreprendre de nouvelles actions pour limiter le comportement indésirable.</span><span class="sxs-lookup"><span data-stu-id="f9afe-162">If not, or if you discover something unexpected, such as a large number of items that are labeled `highly confidential` and are downgraded `general`, you can manage your various policies and take new actions to restrict the undesired behavior.</span></span>

> [!NOTE]
> <span data-ttu-id="f9afe-163">L’explorateur d’activité ne suit pas actuellement les activités de rétention pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f9afe-163">Activity explorer doesn't currently monitor retention activities for Exchange Online.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9afe-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9afe-164">See also</span></span>

- [<span data-ttu-id="f9afe-165">En savoir plus sur les étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="f9afe-165">Learn about sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="f9afe-166">En savoir plus sur les stratégies et les balises de rétention</span><span class="sxs-lookup"><span data-stu-id="f9afe-166">Learn about retention policies and retention labels</span></span>](retention.md)
- <span data-ttu-id="f9afe-167">[En savoir plus sur les types d’informations confidentielles](sensitive-information-type-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="f9afe-167">[Learn about sensitive information types](sensitive-information-type-learn-about.md)</span></span>
- [<span data-ttu-id="f9afe-168">En savoir plus sur la classification des données</span><span class="sxs-lookup"><span data-stu-id="f9afe-168">Learn about data classification</span></span>](data-classification-overview.md)
