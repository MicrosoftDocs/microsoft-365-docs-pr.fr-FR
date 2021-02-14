---
title: Options de navigation pour SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 4/7/2020
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
search.appverid:
- SPO160
- MET150
ms.assetid: adb92b80-b342-4ecb-99a1-da2a2b4782eb
description: Cet article décrit les sites d’options de navigation avec la publication SharePoint activée dans SharePoint Online.
ms.openlocfilehash: 86cefc60a26687835fd6a88de7f249143811de4f
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695834"
---
# <a name="navigation-options-for-sharepoint-online"></a><span data-ttu-id="4820d-103">Options de navigation pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4820d-103">Navigation options for SharePoint Online</span></span>

<span data-ttu-id="4820d-104">Cet article décrit les sites d’options de navigation avec la publication SharePoint activée dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4820d-104">This article describes navigation options sites with SharePoint Publishing enabled in SharePoint Online.</span></span> <span data-ttu-id="4820d-105">Le choix et la configuration de la navigation ont un impact significatif sur les performances et l’évolutivité des sites dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4820d-105">The choice and configuration of navigation significantly impacts the performance and scalability of sites in SharePoint Online.</span></span> <span data-ttu-id="4820d-106">Le modèle de site de publication SharePoint ne doit être utilisé que si nécessaire pour un portail centralisé et la fonctionnalité de publication ne doit être activée que sur des sites spécifiques et uniquement en cas d’absolue nécessité, car elle peut avoir un impact sur les performances en cas d’utilisation incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4820d-106">The SharePoint Publishing site template should only be used if required for a centralized portal and the publishing feature should only be enabled on specific sites and only when absolutely required as it can impact performance when used incorrectly.</span></span>

>[!NOTE]
><span data-ttu-id="4820d-107">Si vous utilisez des options de navigation SharePoint modernes telles que le méga-menu, la navigation en cascade ou la navigation de hub, cet article ne s’applique pas à votre site.</span><span class="sxs-lookup"><span data-stu-id="4820d-107">If you're using modern SharePoint navigation options like mega menu, cascading navigation, or hub navigation, this article does not apply to your site.</span></span> <span data-ttu-id="4820d-108">Les architectures de site SharePoint modernes tirent parti d’une hiérarchie de sites plus aplatie et d’un modèle de hub-and-spoke.</span><span class="sxs-lookup"><span data-stu-id="4820d-108">Modern SharePoint site architectures leverage a more flattened site hierarchy and a hub-and-spoke model.</span></span> <span data-ttu-id="4820d-109">Cela permet d’atteindre de nombreux scénarios qui ne nécessitent PAS l’utilisation de la fonctionnalité de publication SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4820d-109">This allows many scenarios to be achieved that do NOT require use of the SharePoint Publishing feature.</span></span>

## <a name="overview-of-navigation-options"></a><span data-ttu-id="4820d-110">Vue d’ensemble des options de navigation</span><span class="sxs-lookup"><span data-stu-id="4820d-110">Overview of navigation options</span></span>

<span data-ttu-id="4820d-111">La configuration du fournisseur de navigation peut avoir un impact significatif sur les performances de l’ensemble du site, et il est important de prendre en compte le choix d’un fournisseur de navigation et d’une configuration qui s’dimensionnent efficacement pour les besoins d’un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4820d-111">Navigation provider configuration can significantly impact performance for the entire site, and careful consideration must be taken to pick a navigation provider and configuration that scales effectively for the requirements of a SharePoint site.</span></span> <span data-ttu-id="4820d-112">Il existe deux fournisseurs de navigation pré-personnalisés, ainsi que des implémentations de navigation personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4820d-112">There are two out-of-the-box navigation providers, as well as custom navigation implementations.</span></span>

<span data-ttu-id="4820d-113">La première option, la [**navigation**](#using-structural-navigation-in-sharepoint-online)structurelle, est l’option de navigation recommandée dans SharePoint Online pour les sites Sharepoint classiques, si vous allumez la mise en cache de navigation structurelle **pour votre site.**</span><span class="sxs-lookup"><span data-stu-id="4820d-113">The first option, [**Structural navigation**](#using-structural-navigation-in-sharepoint-online), is the recommended navigation option in SharePoint Online for classic Sharepoint sites, **if you turn on structural navigation caching for your site**.</span></span> <span data-ttu-id="4820d-114">Ce fournisseur de navigation affiche les éléments de navigation sous le site actuel, et éventuellement le site actuel et ses frères.</span><span class="sxs-lookup"><span data-stu-id="4820d-114">This navigation provider displays the navigation items below the current site, and optionally the current site and its siblings.</span></span> <span data-ttu-id="4820d-115">Il offre des fonctionnalités supplémentaires telles que le trimming de sécurité et l’éumération de la structure du site.</span><span class="sxs-lookup"><span data-stu-id="4820d-115">It provides additional capabilities such as security trimming and site structure enumeration.</span></span> <span data-ttu-id="4820d-116">Si la mise en cache est désactivée, cela a un impact négatif sur les performances et l’évolutivité, et peut être soumis à une limitation.</span><span class="sxs-lookup"><span data-stu-id="4820d-116">If caching is disabled, this will negatively impact performance and scalability, and may be subject to throttling.</span></span>

<span data-ttu-id="4820d-117">La deuxième option, [**navigation gérée (métadonnées),**](#using-managed-navigation-and-metadata-in-sharepoint-online)représente les éléments de navigation à l’aide d’un ensemble de termes métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="4820d-117">The second option, [**Managed (Metadata) navigation**](#using-managed-navigation-and-metadata-in-sharepoint-online), represents navigation items using a Managed Metadata term set.</span></span> <span data-ttu-id="4820d-118">Nous vous recommandons de désactiver le contrôle de sécurité sauf si cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4820d-118">We recommend that security trimming be disabled unless required.</span></span> <span data-ttu-id="4820d-119">Le trimming de sécurité est activé en tant que paramètre sécurisé par défaut pour ce fournisseur de navigation . toutefois, de nombreux sites ne nécessitent pas la surcharge du contrôle de sécurité, car les éléments de navigation sont souvent cohérents pour tous les utilisateurs du site.</span><span class="sxs-lookup"><span data-stu-id="4820d-119">Security trimming is enabled as a secure-by-default setting for this navigation provider; however, many sites do not require the overhead of security trimming since navigation elements often are consistent for all users of the site.</span></span> <span data-ttu-id="4820d-120">Avec la configuration recommandée pour désactiver le trimming de sécurité, ce fournisseur de navigation ne nécessite pas l’éumation de la structure du site et est hautement évolutif avec un impact acceptable sur les performances.</span><span class="sxs-lookup"><span data-stu-id="4820d-120">With the recommended configuration to disable security trimming, this navigation provider does not require enumerating site structure and is highly scalable with acceptable performance impact.</span></span>

<span data-ttu-id="4820d-121">Outre les fournisseurs de navigation pré-personnalisés, de nombreux clients ont implémenté d’autres implémentations de navigation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4820d-121">In addition to the out-of-the-box navigation providers, many customers have successfully implemented alternative custom navigation implementations.</span></span> <span data-ttu-id="4820d-122">Voir [les scripts côté client pilotés par](#using-search-driven-client-side-scripting) la recherche dans cet article.</span><span class="sxs-lookup"><span data-stu-id="4820d-122">See [Search-driven client-side scripting](#using-search-driven-client-side-scripting) in this article.</span></span>
  
## <a name="pros-and-cons-of-sharepoint-online-navigation-options"></a><span data-ttu-id="4820d-123">Avantages et inconvénients des options de navigation SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4820d-123">Pros and Cons of SharePoint Online navigation options</span></span>

<span data-ttu-id="4820d-124">Le tableau suivant récapitule les avantages et les inconvénients de chaque option.</span><span class="sxs-lookup"><span data-stu-id="4820d-124">The following table summarizes the pros and cons of each option.</span></span>

|<span data-ttu-id="4820d-125">Navigation structurelle</span><span class="sxs-lookup"><span data-stu-id="4820d-125">Structural navigation</span></span>  |<span data-ttu-id="4820d-126">Navigation gérée</span><span class="sxs-lookup"><span data-stu-id="4820d-126">Managed navigation</span></span>  |<span data-ttu-id="4820d-127">Navigation pilotée par la recherche</span><span class="sxs-lookup"><span data-stu-id="4820d-127">Search-driven navigation</span></span>  |<span data-ttu-id="4820d-128">Fournisseur de navigation personnalisée</span><span class="sxs-lookup"><span data-stu-id="4820d-128">Custom-navigation provider</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="4820d-129">Professionnels :</span><span class="sxs-lookup"><span data-stu-id="4820d-129">Pros:</span></span><br/><br/><span data-ttu-id="4820d-130">Facile à gérer</span><span class="sxs-lookup"><span data-stu-id="4820d-130">Easy to maintain</span></span><br/><span data-ttu-id="4820d-131">Sécurité découpée</span><span class="sxs-lookup"><span data-stu-id="4820d-131">Security trimmed</span></span><br/><span data-ttu-id="4820d-132">Mises à jour automatiques dans les 24 heures lorsque le contenu est modifié</span><span class="sxs-lookup"><span data-stu-id="4820d-132">Automatically updates within 24 hours when content is changed</span></span><br/>     |<span data-ttu-id="4820d-133">Professionnels :</span><span class="sxs-lookup"><span data-stu-id="4820d-133">Pros:</span></span><br/><br/><span data-ttu-id="4820d-134">Facile à gérer</span><span class="sxs-lookup"><span data-stu-id="4820d-134">Easy to maintain</span></span><br/>|<span data-ttu-id="4820d-135">Professionnels :</span><span class="sxs-lookup"><span data-stu-id="4820d-135">Pros:</span></span><br/><br/><span data-ttu-id="4820d-136">Sécurité découpée</span><span class="sxs-lookup"><span data-stu-id="4820d-136">Security trimmed</span></span><br/><span data-ttu-id="4820d-137">Mises à jour automatiques à mesure que des sites sont ajoutés</span><span class="sxs-lookup"><span data-stu-id="4820d-137">Automatically updates as sites are added</span></span><br/><span data-ttu-id="4820d-138">Temps de chargement rapide et structure de navigation mise en cache locale</span><span class="sxs-lookup"><span data-stu-id="4820d-138">Fast loading time and locally cached navigation structure</span></span><br/>|<span data-ttu-id="4820d-139">Professionnels :</span><span class="sxs-lookup"><span data-stu-id="4820d-139">Pros:</span></span><br/><br/><span data-ttu-id="4820d-140">Choix plus large d’options disponibles</span><span class="sxs-lookup"><span data-stu-id="4820d-140">Wider choice of options available</span></span><br/><span data-ttu-id="4820d-141">Chargement rapide lors de l’utilisation correcte de la mise en cache</span><span class="sxs-lookup"><span data-stu-id="4820d-141">Fast loading when caching is used correctly</span></span><br/><span data-ttu-id="4820d-142">De nombreuses options fonctionnent bien avec une conception de page réactive</span><span class="sxs-lookup"><span data-stu-id="4820d-142">Many options work well with responsive page design</span></span><br/>|
|<span data-ttu-id="4820d-143">Inconvénients :</span><span class="sxs-lookup"><span data-stu-id="4820d-143">Cons:</span></span><br/><br/><span data-ttu-id="4820d-144">**Impact sur les performances si la mise en cache est désactivée**</span><span class="sxs-lookup"><span data-stu-id="4820d-144">**Impacts performance if caching is disabled**</span></span><br/><span data-ttu-id="4820d-145">Objet de limitation</span><span class="sxs-lookup"><span data-stu-id="4820d-145">Subject to throttling</span></span><br/>|<span data-ttu-id="4820d-146">Inconvénients :</span><span class="sxs-lookup"><span data-stu-id="4820d-146">Cons:</span></span><br/><br/><span data-ttu-id="4820d-147">Non mis à jour automatiquement pour refléter la structure du site</span><span class="sxs-lookup"><span data-stu-id="4820d-147">Not automatically updated to reflect site structure</span></span><br/><span data-ttu-id="4820d-148">**Impact sur les performances si le contrôle de sécurité est activé** ou lorsque la structure de navigation est complexe</span><span class="sxs-lookup"><span data-stu-id="4820d-148">**Impacts performance if security trimming is enabled** or when navigation structure is complex</span></span><br/>|<span data-ttu-id="4820d-149">Inconvénients :</span><span class="sxs-lookup"><span data-stu-id="4820d-149">Cons:</span></span><br/><br/><span data-ttu-id="4820d-150">Aucune possibilité de commander facilement des sites</span><span class="sxs-lookup"><span data-stu-id="4820d-150">No ability to easily order sites</span></span><br/><span data-ttu-id="4820d-151">Nécessite une personnalisation de la page maître (compétences techniques requises)</span><span class="sxs-lookup"><span data-stu-id="4820d-151">Requires customization of the master page (technical skills required)</span></span><br/>|<span data-ttu-id="4820d-152">Inconvénients :</span><span class="sxs-lookup"><span data-stu-id="4820d-152">Cons:</span></span><br/><br/><span data-ttu-id="4820d-153">Le développement personnalisé est requis</span><span class="sxs-lookup"><span data-stu-id="4820d-153">Custom development is required</span></span><br/><span data-ttu-id="4820d-154">La source de données externe/le cache stocké est nécessaire, par exemple, Azure</span><span class="sxs-lookup"><span data-stu-id="4820d-154">External data source / cache stored is needed e.g. Azure</span></span><br/>|

<span data-ttu-id="4820d-155">L’option la plus appropriée pour votre site dépend des besoins de votre site et de vos capacités techniques.</span><span class="sxs-lookup"><span data-stu-id="4820d-155">The most appropriate option for your site will depend on your site requirements and on your technical capability.</span></span> <span data-ttu-id="4820d-156">Si vous souhaitez un fournisseur de navigation facile à configurer qui se met à jour automatiquement lorsque le contenu est modifié, la [navigation](https://support.office.com/article/structural-navigation-and-performance-f163053f-8eca-4b9c-b973-36b395093b43) structurelle avec la mise en cache activée est une bonne option.</span><span class="sxs-lookup"><span data-stu-id="4820d-156">If you want an easy-to-configure navigation provider that automatically updates when content is changed, then structural navigation [with caching enabled](https://support.office.com/article/structural-navigation-and-performance-f163053f-8eca-4b9c-b973-36b395093b43) is a good option.</span></span>

>[!NOTE]
><span data-ttu-id="4820d-157">L’application du même principe que les sites SharePoint modernes en simplifiant la structure globale du site à une structure plate et non hiérarchique améliore les performances et simplifie le passage à des sites SharePoint modernes.</span><span class="sxs-lookup"><span data-stu-id="4820d-157">Applying the same principle as modern SharePoint sites by simplifying the overall site structure to a flatter, non-hierarchical structure improves performance and simplifies moving to modern SharePoint sites.</span></span> <span data-ttu-id="4820d-158">Cela signifie qu’au lieu d’avoir une seule collection de sites avec des centaines de sites (sous-sites web), une meilleure approche consiste à avoir de nombreuses collections de sites avec très peu de sous-sites (sous-sites web).</span><span class="sxs-lookup"><span data-stu-id="4820d-158">What this means is that instead of having a single site collection with hundreds of sites (subwebs), a better approach is to have many site collections with very few subsites (subwebs).</span></span>

## <a name="analyzing-navigation-performance-in-sharepoint-online"></a><span data-ttu-id="4820d-159">Analyse des performances de navigation dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4820d-159">Analyzing navigation performance in SharePoint Online</span></span>

<span data-ttu-id="4820d-160">L’outil Diagnostic de page pour [SharePoint](https://aka.ms/perftool) est une extension de navigateur pour les navigateurs Microsoft Edge et Chrome qui analyse à la fois le portail moderne SharePoint Online et les pages de site de publication classiques.</span><span class="sxs-lookup"><span data-stu-id="4820d-160">The [Page Diagnostics for SharePoint tool](https://aka.ms/perftool) is a browser extension for Microsoft Edge and Chrome browsers that analyzes both SharePoint Online modern portal and classic publishing site pages.</span></span> <span data-ttu-id="4820d-161">Cet outil fonctionne uniquement pour SharePoint Online et ne peut pas être utilisé sur une page système SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4820d-161">This tool only works for SharePoint Online, and cannot be used on a SharePoint system page.</span></span>

<span data-ttu-id="4820d-162">L’outil génère un rapport pour chaque page analysée montrant comment la page fonctionne par rapport à un ensemble prédéfiny de règles et affiche des informations détaillées lorsque les résultats d’un test sont en dehors de la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="4820d-162">The tool generates a report for each analyzed page showing how the page performs against a pre-defined set of rules and displays detailed information when results for a test fall outside the baseline value.</span></span> <span data-ttu-id="4820d-163">Les administrateurs et concepteurs SharePoint Online peuvent utiliser l’outil pour résoudre les problèmes de performances afin de s’assurer que les nouvelles pages sont optimisées avant la publication.</span><span class="sxs-lookup"><span data-stu-id="4820d-163">SharePoint Online administrators and designers can use the tool to troubleshoot performance issues to ensure that new pages are optimized prior to publishing.</span></span>

<span data-ttu-id="4820d-164">**SPRequestDuration, en** particulier, est le temps qu’il faut à SharePoint pour traiter la page.</span><span class="sxs-lookup"><span data-stu-id="4820d-164">**SPRequestDuration** in particular is the time it takes for SharePoint to process the page.</span></span> <span data-ttu-id="4820d-165">La navigation lourde (par exemple, inclure des pages dans la navigation), les hiérarchies de sites complexes et d’autres options de configuration et de topologie peuvent contribuer considérablement à des durées plus longues.</span><span class="sxs-lookup"><span data-stu-id="4820d-165">Heavy navigation (like including pages in navigation), complex site hierarchies, and other configuration and topology options can all dramatically contribute to longer durations.</span></span>

## <a name="using-structural-navigation-in-sharepoint-online"></a><span data-ttu-id="4820d-166">Utilisation de la navigation structurelle dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4820d-166">Using structural navigation in SharePoint Online</span></span>

<span data-ttu-id="4820d-167">Il s’agit de la navigation pré-adaptée utilisée par défaut et de la solution la plus simple.</span><span class="sxs-lookup"><span data-stu-id="4820d-167">This is the out-of-the-box navigation used by default and is the most straightforward solution.</span></span> <span data-ttu-id="4820d-168">Il ne nécessite aucune personnalisation et un utilisateur non technique peut également facilement ajouter des éléments, masquer des éléments et gérer la navigation à partir de la page de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4820d-168">It does not require any customization and a non-technical user can also easily add items, hide items, and manage the navigation from the settings page.</span></span> <span data-ttu-id="4820d-169">Nous vous recommandons [d’activer la mise en cache,](https://support.office.com/article/structural-navigation-and-performance-f163053f-8eca-4b9c-b973-36b395093b43)sinon il existe un compromis coûteux en performances.</span><span class="sxs-lookup"><span data-stu-id="4820d-169">We recommend [enabling caching](https://support.office.com/article/structural-navigation-and-performance-f163053f-8eca-4b9c-b973-36b395093b43), otherwise there is an expensive performance trade-off.</span></span>

### <a name="how-to-implement-structural-navigation-caching"></a><span data-ttu-id="4820d-170">Comment implémenter la mise en cache de navigation structurelle</span><span class="sxs-lookup"><span data-stu-id="4820d-170">How to implement structural navigation caching</span></span>

<span data-ttu-id="4820d-171">Sous **l’apparence des paramètres** du site, vous pouvez vérifier si la navigation structurelle est sélectionnée pour la  >    >  navigation globale ou la navigation actuelle.</span><span class="sxs-lookup"><span data-stu-id="4820d-171">Under **Site Settings** > **Look and Feel** > **Navigation**, you can validate if structural navigation is selected for either global navigation or current navigation.</span></span> <span data-ttu-id="4820d-172">La sélection de **pages Afficher** aura un impact négatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="4820d-172">Selecting **Show pages** will have negative impact on performance.</span></span>

![Navigation structurelle avec afficher les sous-sites sélectionnés](../media/SPONavOptionsStructuredShowSubsites.png)

<span data-ttu-id="4820d-174">La mise en cache peut être activée ou désactivée au niveau de la collection de sites et au niveau du site, et est activée pour les deux par défaut.</span><span class="sxs-lookup"><span data-stu-id="4820d-174">Caching can be enabled or disabled at the site collection level and at the site level, and is enabled for both by default.</span></span> <span data-ttu-id="4820d-175">Pour activer au niveau de la collection de sites, sous **Paramètres** du site Administration de la collection de sites Navigation dans la collection de sites, activez la case à cocher  >    >  Activer **la mise en cache.**</span><span class="sxs-lookup"><span data-stu-id="4820d-175">To enable at the site collection level, under **Site Settings** > **Site Collection Administration** > **Site Collection Navigation**, check the box for **Enable caching**.</span></span>

![Activer la mise en cache au niveau du site](../media/structural-nav/structural-nav-caching-site-coll.png)

<span data-ttu-id="4820d-177">Pour activer au niveau du site, sous Navigation des **paramètres** du site, activez la case à cocher  >  Activer la mise en **cache.**</span><span class="sxs-lookup"><span data-stu-id="4820d-177">To enable at the site level, under **Site Settings** > **Navigation**, check the box for **Enable caching**.</span></span>

![Activer la mise en cache au niveau du site](../media/structural-nav/structural-nav-caching-site.png)

## <a name="using-managed-navigation-and-metadata-in-sharepoint-online"></a><span data-ttu-id="4820d-179">Utilisation de la navigation gérée et des métadonnées dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4820d-179">Using managed navigation and metadata in SharePoint Online</span></span>

<span data-ttu-id="4820d-180">La navigation gérée est une autre option pré-existante que vous pouvez utiliser pour recréer la plupart des mêmes fonctionnalités que la navigation structurelle.</span><span class="sxs-lookup"><span data-stu-id="4820d-180">Managed navigation is another out-of-the-box option that you can use to recreate most of the same functionality as structural navigation.</span></span> <span data-ttu-id="4820d-181">Les métadonnées gérées peuvent être configurées pour que le contrôle de sécurité soit activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="4820d-181">Managed metadata can be configured to have security trimming enabled or disabled.</span></span> <span data-ttu-id="4820d-182">Lorsqu’elle est configurée avec le contrôle de sécurité désactivé, la navigation gérée est relativement efficace car elle charge tous les liens de navigation avec un nombre constant d’appels de serveur.</span><span class="sxs-lookup"><span data-stu-id="4820d-182">When configured with security trimming disabled, managed navigation is fairly efficient as it loads all the navigation links with a constant number of server calls.</span></span> <span data-ttu-id="4820d-183">Toutefois, l’activation du contrôle de sécurité annule certains des avantages en matière de performances de la navigation gérée.</span><span class="sxs-lookup"><span data-stu-id="4820d-183">Enabling security trimming, however, negates some of the performance advantages of managed navigation.</span></span>

<span data-ttu-id="4820d-184">Si vous avez besoin d’activer le contrôle de sécurité, nous vous recommandons d':</span><span class="sxs-lookup"><span data-stu-id="4820d-184">If you need to enable security trimming, we recommend that you:</span></span>

- <span data-ttu-id="4820d-185">Mettre à jour tous les liens d’URL conviviales vers des liens simples</span><span class="sxs-lookup"><span data-stu-id="4820d-185">Update all friendly URL links to simple links</span></span>
- <span data-ttu-id="4820d-186">Ajouter les nodes de contrôle de sécurité requis en tant qu’URL conviviales</span><span class="sxs-lookup"><span data-stu-id="4820d-186">Add required security trimming nodes as friendly URLs</span></span>
- <span data-ttu-id="4820d-187">Limiter le nombre d’éléments de navigation à 100 et pas plus de 3 niveaux de profondeur</span><span class="sxs-lookup"><span data-stu-id="4820d-187">Limit the number of navigation items to no more than 100 and no more than 3 levels deep</span></span>

<span data-ttu-id="4820d-188">De nombreux sites ne nécessitent pas de contrôle de sécurité, car la structure de navigation est souvent cohérente pour tous les utilisateurs du site.</span><span class="sxs-lookup"><span data-stu-id="4820d-188">Many sites do not require security trimming, as the navigation structure is often consistent for all users of the site.</span></span> <span data-ttu-id="4820d-189">Si le contrôle de sécurité est désactivé et qu’un lien est ajouté à la navigation à l’accès de tous les utilisateurs, le lien s’affiche toujours, mais entraîne un message de refus d’accès.</span><span class="sxs-lookup"><span data-stu-id="4820d-189">If security trimming is disabled and a link is added to navigation that not all users have access to, the link will still show but will lead to an access denied message.</span></span> <span data-ttu-id="4820d-190">Il n’y a aucun risque d’accès par inadvertance au contenu.</span><span class="sxs-lookup"><span data-stu-id="4820d-190">There is no risk of inadvertent access to the content.</span></span>

### <a name="how-to-implement-managed-navigation-and-the-results"></a><span data-ttu-id="4820d-191">Comment implémenter la navigation gérée et les résultats</span><span class="sxs-lookup"><span data-stu-id="4820d-191">How to implement managed navigation and the results</span></span>

<span data-ttu-id="4820d-192">Il existe plusieurs articles sur docs.microsoft.com sur les détails de la navigation gérée.</span><span class="sxs-lookup"><span data-stu-id="4820d-192">There are several articles on docs.microsoft.com about the details of managed navigation.</span></span> <span data-ttu-id="4820d-193">Par exemple, voir [Vue d’ensemble de la navigation gérée dans SharePoint Server.](https://docs.microsoft.com/sharepoint/administration/overview-of-managed-navigation)</span><span class="sxs-lookup"><span data-stu-id="4820d-193">For example, see [Overview of managed navigation in SharePoint Server](https://docs.microsoft.com/sharepoint/administration/overview-of-managed-navigation).</span></span>

<span data-ttu-id="4820d-194">Pour implémenter la navigation gérée, vous devez configurer des termes avec des URL correspondant à la structure de navigation du site.</span><span class="sxs-lookup"><span data-stu-id="4820d-194">In order to implement managed navigation, you set up terms with URLs corresponding to the navigation structure of the site.</span></span> <span data-ttu-id="4820d-195">La navigation gérée peut même être organisée manuellement pour remplacer la navigation structurelle dans de nombreux cas.</span><span class="sxs-lookup"><span data-stu-id="4820d-195">Managed navigation can even be manually curated to replace structural navigation in many cases.</span></span> <span data-ttu-id="4820d-196">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4820d-196">For example:</span></span>

![Structure de site SharePoint Online](../media/SPONavOptionsListOfSites.png)<span data-ttu-id="4820d-198">)</span><span class="sxs-lookup"><span data-stu-id="4820d-198">)</span></span>

## <a name="using-search-driven-client-side-scripting"></a><span data-ttu-id="4820d-199">Utilisation de scripts côté client pilotés par la recherche</span><span class="sxs-lookup"><span data-stu-id="4820d-199">Using Search-driven client-side scripting</span></span>

<span data-ttu-id="4820d-200">Une classe courante d’implémentations de navigation personnalisées adopte des modèles de conception rendus par le client qui stockent un cache local de nodes de navigation.</span><span class="sxs-lookup"><span data-stu-id="4820d-200">One common class of custom navigation implementations embraces client-rendered design patterns that store a local cache of navigation nodes.</span></span>

<span data-ttu-id="4820d-201">Ces fournisseurs de navigation ont deux avantages clés :</span><span class="sxs-lookup"><span data-stu-id="4820d-201">These navigation providers have a couple of key advantages:</span></span>

- <span data-ttu-id="4820d-202">Ils fonctionnent généralement bien avec les conceptions de page réactives.</span><span class="sxs-lookup"><span data-stu-id="4820d-202">They generally work well with responsive page designs.</span></span>
- <span data-ttu-id="4820d-203">Ils sont extrêmement évolutifs et performants, car ils peuvent s’restituer sans coût de ressource (et s’actualiser en arrière-plan après un délai d’attente).</span><span class="sxs-lookup"><span data-stu-id="4820d-203">They are extremely scalable and performant because they can render with no resource cost (and refresh in the background after a timeout).</span></span>
- <span data-ttu-id="4820d-204">Ces fournisseurs de navigation peuvent récupérer des données de navigation à l’aide de différentes stratégies, allant de configurations statiques simples à différents fournisseurs de données dynamiques.</span><span class="sxs-lookup"><span data-stu-id="4820d-204">These navigation providers can retrieve navigation data using various strategies, ranging from simple static configurations to various dynamic data providers.</span></span>

<span data-ttu-id="4820d-205">Un exemple de fournisseur de données consiste à utiliser une **navigation** pilotée par la recherche, ce qui permet d’éumer les nodes de navigation et de gérer efficacement le tri de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4820d-205">An example of a data provider is to use a **Search-driven navigation**, which allows flexibility for enumerating navigation nodes and handling security trimming efficiently.</span></span>

<span data-ttu-id="4820d-206">Il existe d’autres options populaires pour créer **des fournisseurs de navigation personnalisés.**</span><span class="sxs-lookup"><span data-stu-id="4820d-206">There are other popular options to build **Custom navigation providers**.</span></span> <span data-ttu-id="4820d-207">Consultez les solutions de navigation pour les [portails SharePoint Online](https://docs.microsoft.com/sharepoint/dev/solution-guidance/portal-navigation) pour obtenir des instructions supplémentaires sur la création d’un fournisseur de navigation personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4820d-207">Please review [Navigation solutions for SharePoint Online portals](https://docs.microsoft.com/sharepoint/dev/solution-guidance/portal-navigation) for further guidance on building a Custom navigation provider.</span></span>

<span data-ttu-id="4820d-208">À l’aide de la recherche, vous pouvez tirer parti des index qui sont créés en arrière-plan à l’aide de l’analyse continue.</span><span class="sxs-lookup"><span data-stu-id="4820d-208">Using search you can leverage the indexes that are built up in the background using continuous crawl.</span></span> <span data-ttu-id="4820d-209">Les résultats de la recherche sont obtenus à partir de l’index de recherche et les résultats sont découpés en sécurité.</span><span class="sxs-lookup"><span data-stu-id="4820d-209">The search results are pulled from the search index and the results are security-trimmed.</span></span> <span data-ttu-id="4820d-210">Cela est généralement plus rapide que les fournisseurs de navigation pré-requis lorsque le tri de sécurité est requis.</span><span class="sxs-lookup"><span data-stu-id="4820d-210">This is generally faster than out-of-the-box navigation providers when security trimming is required.</span></span> <span data-ttu-id="4820d-211">L’utilisation de la recherche pour la navigation structurelle, en particulier si vous avez une structure de site complexe, accélérera considérablement le temps de chargement des pages.</span><span class="sxs-lookup"><span data-stu-id="4820d-211">Using search for structural navigation, especially if you have a complex site structure, will speed up page loading time considerably.</span></span> <span data-ttu-id="4820d-212">Le principal avantage de cette navigation gérée est que vous bénéficiez du trimming de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4820d-212">The main advantage of this over managed navigation is that you benefit from security trimming.</span></span>

<span data-ttu-id="4820d-213">Cette approche implique la création d’une page maître personnalisée et le remplacement du code de navigation pré-personnalisé par du code HTML personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4820d-213">This approach involves creating a custom master page and replacing the out-of-the-box navigation code with custom HTML.</span></span> <span data-ttu-id="4820d-214">Suivez cette procédure décrite dans l’exemple suivant pour remplacer le code de navigation dans le fichier `seattle.html` .</span><span class="sxs-lookup"><span data-stu-id="4820d-214">Follow this procedure outlined in the following example to replace the navigation code in the file `seattle.html`.</span></span> <span data-ttu-id="4820d-215">Dans cet exemple, vous allez ouvrir le `seattle.html` fichier et remplacer l’élément entier `id="DeltaTopNavigation"` par du code HTML personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4820d-215">In this example, you will open the `seattle.html` file and replace the whole element `id="DeltaTopNavigation"` with custom HTML code.</span></span>

### <a name="example-replace-the-out-of-the-box-navigation-code-in-a-master-page"></a><span data-ttu-id="4820d-216">Exemple : Remplacer le code de navigation pré-encadré dans une page maître</span><span class="sxs-lookup"><span data-stu-id="4820d-216">Example: Replace the out-of-the-box navigation code in a master page</span></span>

1. <span data-ttu-id="4820d-217">Accédez à la page Paramètres du site.</span><span class="sxs-lookup"><span data-stu-id="4820d-217">Navigate to the Site Settings page.</span></span>
2. <span data-ttu-id="4820d-218">Ouvrez la galerie de pages maîtres en cliquant sur **Pages maîtres.**</span><span class="sxs-lookup"><span data-stu-id="4820d-218">Open the master page gallery by clicking **Master Pages**.</span></span>
3. <span data-ttu-id="4820d-219">À partir de là, vous pouvez naviguer dans la bibliothèque et télécharger le `seattle.master` fichier.</span><span class="sxs-lookup"><span data-stu-id="4820d-219">From here you can navigate through the library and download the file `seattle.master`.</span></span>
4. <span data-ttu-id="4820d-220">Modifiez le code à l’aide d’un éditeur de texte et supprimez le bloc de code dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="4820d-220">Edit the code using a text editor and delete the code block in the following screen shot.</span></span><br/>![Supprimer le bloc de code affiché](../media/SPONavOptionsDeleteCodeBlock.png)<br/>
5. <span data-ttu-id="4820d-222">Supprimez le code entre les balises et les balises et remplacez-le `<SharePoint:AjaxDelta id="DeltaTopNavigation">` `<\SharePoint:AjaxDelta>` par l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="4820d-222">Remove the code between the `<SharePoint:AjaxDelta id="DeltaTopNavigation">` and `<\SharePoint:AjaxDelta>` tags and replace it with the following snippet:</span></span><br/>

```javascript
<div id="loading">
  <!--Replace with path to loading image.-->
  <div style="background-image: url(''); height: 22px; width: 22px; ">
  </div>
</div>
<!-- Main Content-->
<div id="navContainer" style="display:none">
    <div data-bind="foreach: hierarchy" class="noindex ms-core-listMenu-horizontalBox">
        <a class="dynamic menu-item ms-core-listMenu-item ms-displayInline ms-navedit-linkNode" data-bind="attr: { href: item.Url, title: item.Title }">
            <span class="menu-item-text" data-bind="text: item.Title">
            </span>
        </a>
        <ul id="menu" data-bind="foreach: $data.children" style="padding-left:20px">
            <li class="static dynamic-children level1">
                <a class="static dynamic-children menu-item ms-core-listMenu-item ms-displayInline ms-navedit-linkNode" data-bind="attr: { href: item.Url, title: item.Title }">

                 <!-- ko if: children.length > 0-->
                    <span aria-haspopup="true" class="additional-background ms-navedit-flyoutArrow dynamic-children">
                        <span class="menu-item-text" data-bind="text: item.Title">
                        </span>
                    </span>
                <!-- /ko -->
                <!-- ko if: children.length == 0-->
                    <span aria-haspopup="true" class="ms-navedit-flyoutArrow dynamic-children">
                        <span class="menu-item-text" data-bind="text: item.Title">
                        </span>
                    </span>
                <!-- /ko -->
                </a>

                <!-- ko if: children.length > 0-->
                <ul id="menu"  data-bind="foreach: children;" class="dynamic  level2" >
                    <li class="dynamic level2">
                        <a class="dynamic menu-item ms-core-listMenu-item ms-displayInline  ms-navedit-linkNode" data-bind="attr: { href: item.Url, title: item.Title }">

          <!-- ko if: children.length > 0-->
          <span aria-haspopup="true" class="additional-background ms-navedit-flyoutArrow dynamic-children">
           <span class="menu-item-text" data-bind="text: item.Title">
           </span>
          </span>
           <!-- /ko -->
          <!-- ko if: children.length == 0-->
          <span aria-haspopup="true" class="ms-navedit-flyoutArrow dynamic-children">
           <span class="menu-item-text" data-bind="text: item.Title">
           </span>
          </span>
          <!-- /ko -->
                        </a>
          <!-- ko if: children.length > 0-->
         <ul id="menu" data-bind="foreach: children;" class="dynamic level3" >
          <li class="dynamic level3">
           <a class="dynamic menu-item ms-core-listMenu-item ms-displayInline ms-navedit-linkNode" data-bind="attr: { href: item.Url, title: item.Title }">
            <span class="menu-item-text" data-bind="text: item.Title">
            </span>
           </a>
          </li>
         </ul>
           <!-- /ko -->
                    </li>
                </ul>
                <!-- /ko -->
            </li>
        </ul>
    </div>
</div>
```

<br/>
6. <span data-ttu-id="4820d-223">Remplacez l’URL dans la balise d’ancrage d’image de chargement au début, par un lien vers une image de chargement dans votre collection de sites.</span><span class="sxs-lookup"><span data-stu-id="4820d-223">Replace the URL in the loading image anchor tag at the beginning, with a link to a loading image in your site collection.</span></span> <span data-ttu-id="4820d-224">Une fois les modifications apportées, renommez le fichier, puis téléchargez-le dans la galerie de pages maîtres.</span><span class="sxs-lookup"><span data-stu-id="4820d-224">After you have made the changes, rename the file and then upload it to the master page gallery.</span></span> <span data-ttu-id="4820d-225">Cela génère un nouveau fichier .master.</span><span class="sxs-lookup"><span data-stu-id="4820d-225">This generates a new .master file.</span></span><br/>
7. <span data-ttu-id="4820d-226">Ce code HTML est le code de base qui sera rempli par les résultats de recherche renvoyés à partir du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4820d-226">This HTML is the basic markup that will be populated by the search results returned from JavaScript code.</span></span> <span data-ttu-id="4820d-227">Vous devez modifier le code pour modifier la valeur de var root = « site collection URL » comme indiqué dans l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="4820d-227">You will need to edit the code to change the value for var root = "site collection URL" as demonstrated in the following snippet:</span></span><br/>

```javascript
var root = "https://spperformance.sharepoint.com/sites/NavigationBySearch";
```

<br/>
8. <span data-ttu-id="4820d-228">Les résultats sont affectés au tableau self.nodes et une hiérarchie est construite à partir des objets à l’aide linq.js en attribuant la sortie à un tableau self.hierarchy.</span><span class="sxs-lookup"><span data-stu-id="4820d-228">The results are assigned to the self.nodes array and a hierarchy is built out of the objects using linq.js assigning the output to an array self.hierarchy.</span></span> <span data-ttu-id="4820d-229">Ce tableau est l’objet lié au code HTML.</span><span class="sxs-lookup"><span data-stu-id="4820d-229">This array is the object that is bound to the HTML.</span></span> <span data-ttu-id="4820d-230">Cette fonction est effectuée dans la fonction toggleView() en passant l’objet self à la fonction ko.applyBinding().</span><span class="sxs-lookup"><span data-stu-id="4820d-230">This is done in the toggleView() function by passing the self object to the ko.applyBinding() function.</span></span><br/><span data-ttu-id="4820d-231">Le tableau de hiérarchie est alors lié au code HTML suivant :</span><span class="sxs-lookup"><span data-stu-id="4820d-231">This then causes the hierarchy array to be bound to the following HTML:</span></span><br/>

```javascript
<div data-bind="foreach: hierarchy" class="noindex ms-core-listMenu-horizontalBox">
```

<span data-ttu-id="4820d-232">Les handlers d’événements pour et sont ajoutés à la navigation de niveau supérieur pour gérer les menus de listes des sous-site qui sont `mouseenter` `mouseexit` effectués dans la `addEventsToElements()` fonction.</span><span class="sxs-lookup"><span data-stu-id="4820d-232">The event handlers for `mouseenter` and `mouseexit` are added to the top-level navigation to handle the subsite drop-down menus which is done in the `addEventsToElements()` function.</span></span>

<span data-ttu-id="4820d-233">Dans notre exemple de navigation complexe, une nouvelle charge de page sans la mise en cache locale indique que le temps passé sur le serveur a été réduit par rapport à la navigation structurelle de référence pour obtenir un résultat similaire à l’approche de navigation gérée.</span><span class="sxs-lookup"><span data-stu-id="4820d-233">In our complex navigation example, a fresh page load without the local caching shows the time spent on the server has been cut down from the benchmark structural navigation to get a similar result as the managed navigation approach.</span></span>

### <a name="about-the-javascript-file"></a><span data-ttu-id="4820d-234">À propos du fichier JavaScript...</span><span class="sxs-lookup"><span data-stu-id="4820d-234">About the JavaScript file...</span></span>

>[!NOTE]
><span data-ttu-id="4820d-235">Si vous utilisez javaScript personnalisé, assurez-vous que le CDN public est activé et que le fichier se trouve dans un emplacement CDN.</span><span class="sxs-lookup"><span data-stu-id="4820d-235">If using custom JavaScript, ensure that public CDN is enabled and the file is in a CDN location.</span></span>

<span data-ttu-id="4820d-236">L’intégralité du fichier JavaScript est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4820d-236">The entire JavaScript file is as follows:</span></span>

```javascript
//Models and Namespaces
var SPOCustom = SPOCustom || {};
SPOCustom.Models = SPOCustom.Models || {}
SPOCustom.Models.NavigationNode = function () {

    this.Url = ko.observable("");
    this.Title = ko.observable("");
    this.Parent = ko.observable("");

};

var root = "https://spperformance.sharepoint.com/sites/NavigationBySearch";
var baseUrl = root + "/_api/search/query?querytext=";
var query = baseUrl + "'contentClass=\"STS_Web\"+path:" + root + "'&trimduplicates=false&rowlimit=300";

var baseRequest = {
    url: "",
    type: ""
};


//Parses a local object from JSON search result.
function getNavigationFromDto(dto) {
    var item = new SPOCustom.Models.NavigationNode();
    if (dto != undefined) {

        var webTemplate = getSearchResultsValue(dto.Cells.results, 'WebTemplate');

        if (webTemplate != "APP") {
            item.Title(getSearchResultsValue(dto.Cells.results, 'Title')); //Key = Title
            item.Url(getSearchResultsValue(dto.Cells.results, 'Path')); //Key = Path
            item.Parent(getSearchResultsValue(dto.Cells.results, 'ParentLink')); //Key = ParentLink
        }

    }
    return item;
}

function getSearchResultsValue(results, key) {

    for (i = 0; i < results.length; i++) {
        if (results[i].Key == key) {
            return results[i].Value;
        }
    }
    return null;
}

//Parse a local object from the serialized cache.
function getNavigationFromCache(dto) {
    var item = new SPOCustom.Models.NavigationNode();

    if (dto != undefined) {

        item.Title(dto.Title);
        item.Url(dto.Url);
        item.Parent(dto.Parent);
    }

    return item;
}

/* create a new OData request for JSON response */
function getRequest(endpoint) {
    var request = baseRequest;
    request.type = "GET";
    request.url = endpoint;
    request.headers = { ACCEPT: "application/json;odata=verbose" };
    return request;
};

/* Navigation Module*/
function NavigationViewModel() {
    "use strict";
    var self = this;
    self.nodes = ko.observableArray([]);
    self.hierarchy = ko.observableArray([]);;
    self.loadNavigatioNodes = function () {
        //Check local storage for cached navigation datasource.
        var fromStorage = localStorage["nodesCache"];
        if (false) {
            var cachedNodes = JSON.parse(localStorage["nodesCache"]);

            if (cachedNodes && timeStamp) {
                //Check for cache expiration. Currently set to 3 hrs.
                var now = new Date();
                var diff = now.getTime() - timeStamp;
                if (Math.round(diff / (1000 * 60 * 60)) < 3) {

                    //return from cache.
                    var cacheResults = [];
                    $.each(cachedNodes, function (i, item) {
                        var nodeitem = getNavigationFromCache(item, true);
                        cacheResults.push(nodeitem);
                    });

                    self.buildHierarchy(cacheResults);
                    self.toggleView();
                    addEventsToElements();
                    return;
                }
            }
        }
        //No cache hit, REST call required.
        self.queryRemoteInterface();
    };

    //Executes a REST call and builds the navigation hierarchy.
    self.queryRemoteInterface = function () {
        var oDataRequest = getRequest(query);
        $.ajax(oDataRequest).done(function (data) {
            var results = [];
            $.each(data.d.query.PrimaryQueryResult.RelevantResults.Table.Rows.results, function (i, item) {

                if (i == 0) {
                    //Add root element.
                    var rootItem = new SPOCustom.Models.NavigationNode();
                    rootItem.Title("Root");
                    rootItem.Url(root);
                    rootItem.Parent(null);
                    results.push(rootItem);
                }
                var navItem = getNavigationFromDto(item);
                results.push(navItem);
            });
            //Add to local cache
            localStorage["nodesCache"] = ko.toJSON(results);

            localStorage["nodesCachedAt"] = new Date().getTime();
            self.nodes(results);
            if (self.nodes().length > 0) {
                var unsortedArray = self.nodes();
                var sortedArray = unsortedArray.sort(self.sortObjectsInArray);

                self.buildHierarchy(sortedArray);
                self.toggleView();
                addEventsToElements();
            }
        }).fail(function () {
            //Handle error here!!
            $("#loading").hide();
            $("#error").show();
        });
    };
    self.toggleView = function () {
        var navContainer = document.getElementById("navContainer");
        ko.applyBindings(self, navContainer);
        $("#loading").hide();
        $("#navContainer").show();

    };
    //Uses linq.js to build the navigation tree.
    self.buildHierarchy = function (enumerable) {
        self.hierarchy(Enumerable.From(enumerable).ByHierarchy(function (d) {
            return d.Parent() == null;
        }, function (parent, child) {
            if (parent.Url() == null || child.Parent() == null)
                return false;
            return parent.Url().toUpperCase() == child.Parent().toUpperCase();
        }).ToArray());

        self.sortChildren(self.hierarchy()[0]);
    };


    self.sortChildren = function (parent) {

        // sjip processing if no children
        if (!parent || !parent.children || parent.children.length === 0) {
            return;
        }

        parent.children = parent.children.sort(self.sortObjectsInArray2);

        for (var i = 0; i < parent.children.length; i++) {
            var elem = parent.children[i];

            if (elem.children && elem.children.length > 0) {
                self.sortChildren(elem);
            }
        }
    };

    // ByHierarchy method breaks the sorting in chrome and firefox
    // we need to resort  as ascending
    self.sortObjectsInArray2 = function (a, b) {
        if (a.item.Title() > b.item.Title())
            return 1;
        if (a.item.Title() < b.item.Title())
            return -1;
        return 0;
    };


    self.sortObjectsInArray = function (a, b) {
        if (a.Title() > b.Title())
            return -1;
        if (a.Title() < b.Title())
            return 1;
        return 0;
    }
}

//Loads the navigation on load and binds the event handlers for mouse interaction.
function InitCustomNav() {
    var viewModel = new NavigationViewModel();
    viewModel.loadNavigatioNodes();
}

function addEventsToElements() {
    //events.
      $("li.level1").mouseover(function () {
          var position = $(this).position();
          $(this).find("ul.level2").css({ width: 100, left: position.left + 10, top: 50 });
      })
   .mouseout(function () {
     $(this).find("ul.level2").css({  left: -99999, top: 0 });
   
    });
   
     $("li.level2").mouseover(function () {
          var position = $(this).position();
          console.log(JSON.stringify(position));
          $(this).find("ul.level3").css({ width: 100, left: position.left + 95, top:  position.top});
      })
   .mouseout(function () {
     $(this).find("ul.level3").css({  left: -99999, top: 0 });
    });
} _spBodyOnLoadFunctionNames.push("InitCustomNav");

```

<span data-ttu-id="4820d-237">Pour résumer le code indiqué ci-dessus dans la fonction, une fonction est créée, puis la `jQuery $(document).ready` fonction sur cet objet est `viewModel object` `loadNavigationNodes()` appelée.</span><span class="sxs-lookup"><span data-stu-id="4820d-237">To summarize the code shown above in the `jQuery $(document).ready` function there is a `viewModel object` created and then the `loadNavigationNodes()` function on that object is called.</span></span> <span data-ttu-id="4820d-238">Cette fonction charge la hiérarchie de navigation précédemment intégrée stockée dans le stockage local HTML5 du navigateur client ou elle appelle la `queryRemoteInterface()` fonction.</span><span class="sxs-lookup"><span data-stu-id="4820d-238">This function either loads the previously built navigation hierarchy stored in the HTML5 local storage of the client browser or it calls the function `queryRemoteInterface()`.</span></span>

<span data-ttu-id="4820d-239">`QueryRemoteInterface()` crée une requête à l’aide de la fonction avec le paramètre de requête défini précédemment dans le script, puis renvoie des données `getRequest()` à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="4820d-239">`QueryRemoteInterface()` builds a request using the `getRequest()` function with the query parameter defined earlier in the script and then returns data from the server.</span></span> <span data-ttu-id="4820d-240">Ces données sont essentiellement un tableau de tous les sites de la collection de sites représentés en tant qu’objets de transfert de données avec différentes propriétés.</span><span class="sxs-lookup"><span data-stu-id="4820d-240">This data is essentially an array of all the sites in the site collection represented as data transfer objects with various properties.</span></span>

<span data-ttu-id="4820d-241">Ces données sont ensuite analysees dans les objets précédemment définis qui utilisent pour créer des propriétés observables à utiliser par les données liant les valeurs dans le code HTML que nous avons défini `SPO.Models.NavigationNode` `Knockout.js` précédemment.</span><span class="sxs-lookup"><span data-stu-id="4820d-241">This data is then parsed into the previously defined `SPO.Models.NavigationNode` objects which use `Knockout.js` to create observable properties for use by data binding the values into the HTML that we defined earlier.</span></span>

<span data-ttu-id="4820d-242">Les objets sont ensuite placés dans un tableau de résultats.</span><span class="sxs-lookup"><span data-stu-id="4820d-242">The objects are then put into a results array.</span></span> <span data-ttu-id="4820d-243">Ce tableau est en JSON à l’aide de Knockout et stocké dans le stockage du navigateur local pour améliorer les performances lors des chargements de page futurs.</span><span class="sxs-lookup"><span data-stu-id="4820d-243">This array is parsed into JSON using Knockout and stored in the local browser storage for improved performance on future page loads.</span></span>

### <a name="benefits-of-this-approach"></a><span data-ttu-id="4820d-244">Avantages de cette approche</span><span class="sxs-lookup"><span data-stu-id="4820d-244">Benefits of this approach</span></span>

<span data-ttu-id="4820d-245">L’un [](#example-replace-the-out-of-the-box-navigation-code-in-a-master-page) des principaux avantages de cette approche est qu’en utilisant le stockage local HTML5, la navigation est stockée localement pour l’utilisateur lors du prochain chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="4820d-245">One major benefit of [this approach](#example-replace-the-out-of-the-box-navigation-code-in-a-master-page) is that by using HTML5 local storage, the navigation is stored locally for the user the next time they load the page.</span></span> <span data-ttu-id="4820d-246">L’utilisation de l’API de recherche pour la navigation structurelle nous permet d’obtenir des améliorations majeures en matière de performances. Toutefois, l’exécution et la personnalisation de cette fonctionnalité prennent des fonctions techniques.</span><span class="sxs-lookup"><span data-stu-id="4820d-246">We get major performance improvements from using the search API for structural navigation; however, it takes some technical capability to execute and customize this functionality.</span></span>

<span data-ttu-id="4820d-247">Dans [l’exemple d’implémentation,](#example-replace-the-out-of-the-box-navigation-code-in-a-master-page)les sites sont ordonnés de la même manière que la navigation structurelle pré-ant. par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="4820d-247">In the [example implementation](#example-replace-the-out-of-the-box-navigation-code-in-a-master-page), the sites are ordered in the same way as the out-of-the-box structural navigation; alphabetical order.</span></span> <span data-ttu-id="4820d-248">Si vous souhaitez vous dévier de cet ordre, il serait plus compliqué de développer et de maintenir.</span><span class="sxs-lookup"><span data-stu-id="4820d-248">If you wanted to deviate from this order, it would be more complicated to develop and maintain.</span></span> <span data-ttu-id="4820d-249">En outre, cette approche nécessite que vous déviiez des pages maîtres pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4820d-249">Also, this approach requires you to deviate from the supported master pages.</span></span> <span data-ttu-id="4820d-250">Si la page maître personnalisée n’est pas conservée, votre site manquera les mises à jour et les améliorations apportées par Microsoft aux pages maîtres.</span><span class="sxs-lookup"><span data-stu-id="4820d-250">If the custom master page is not maintained, your site will miss out on updates and improvements that Microsoft makes to the master pages.</span></span>

<span data-ttu-id="4820d-251">Le [code ci-dessus](#about-the-javascript-file) présente les dépendances suivantes :</span><span class="sxs-lookup"><span data-stu-id="4820d-251">The [above code](#about-the-javascript-file) has the following dependencies:</span></span>

- <span data-ttu-id="4820d-252">jQuery - https://jquery.com/</span><span class="sxs-lookup"><span data-stu-id="4820d-252">jQuery - https://jquery.com/</span></span>
- <span data-ttu-id="4820d-253">KnockoutJS - https://knockoutjs.com/</span><span class="sxs-lookup"><span data-stu-id="4820d-253">KnockoutJS - https://knockoutjs.com/</span></span>
- <span data-ttu-id="4820d-254">Linq.js - https://linqjs.codeplex.com/ ou github.com/neuecc/linq.js</span><span class="sxs-lookup"><span data-stu-id="4820d-254">Linq.js - https://linqjs.codeplex.com/, or github.com/neuecc/linq.js</span></span>

<span data-ttu-id="4820d-255">La version actuelle de LinqJS ne contient pas la méthode ByHierarchy utilisée dans le code ci-dessus et va rompre le code de navigation.</span><span class="sxs-lookup"><span data-stu-id="4820d-255">The current version of LinqJS does not contain the ByHierarchy method used in the above code and will break the navigation code.</span></span> <span data-ttu-id="4820d-256">Pour résoudre ce problème, ajoutez la méthode suivante au fichier Linq.js avant la `Flatten: function ()` ligne.</span><span class="sxs-lookup"><span data-stu-id="4820d-256">To fix this, add the following method to the Linq.js file before the line `Flatten: function ()`.</span></span>

```javascript
ByHierarchy: function(firstLevel, connectBy, orderBy, ascending, parent) {
     ascending = ascending == undefined ? true : ascending;
     var orderMethod = ascending == true ? 'OrderBy' : 'OrderByDescending';
     var source = this;
     firstLevel = Utils.CreateLambda(firstLevel);
     connectBy = Utils.CreateLambda(connectBy);
     orderBy = Utils.CreateLambda(orderBy);

     //Initiate or increase level
     var level = parent === undefined ? 1 : parent.level + 1;

    return new Enumerable(function() {
         var enumerator;
         var index = 0;

        var createLevel = function() {
                 var obj = {
                     item: enumerator.Current(),
                     level : level
                 };
                 obj.children = Enumerable.From(source).ByHierarchy(firstLevel, connectBy, orderBy, ascending, obj);
                 if (orderBy !== undefined) {
                     obj.children = obj.children[orderMethod](function(d) {
                         return orderBy(d.item); //unwrap the actual item for sort to work
                     });
                 }
                 obj.children = obj.children.ToArray();
                 Enumerable.From(obj.children).ForEach(function(child) {
                     child.getParent = function() {
                         return obj;
                     };
                 });
                 return obj;
             };

        return new IEnumerator(

        function() {
             enumerator = source.GetEnumerator();
         }, function() {
             while (enumerator.MoveNext()) {
                 var returnArr;
                 if (!parent) {
                     if (firstLevel(enumerator.Current(), index++)) {
                         return this.Yield(createLevel());
                     }

                } else {
                     if (connectBy(parent.item, enumerator.Current(), index++)) {
                         return this.Yield(createLevel());
                     }
                 }
             }
             return false;
         }, function() {
             Utils.Dispose(enumerator);
         })
     });
 },

```
  
## <a name="related-topics"></a><span data-ttu-id="4820d-257">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4820d-257">Related topics</span></span>

[<span data-ttu-id="4820d-258">Vue d'ensemble de la navigation gérée dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="4820d-258">Overview of managed navigation in SharePoint Server</span></span>](https://docs.microsoft.com/sharepoint/administration/overview-of-managed-navigation)

[<span data-ttu-id="4820d-259">Mise en cache et performances de navigation structurelle</span><span class="sxs-lookup"><span data-stu-id="4820d-259">Structural navigation caching and performance</span></span>](https://support.office.com/article/structural-navigation-and-performance-f163053f-8eca-4b9c-b973-36b395093b43)
