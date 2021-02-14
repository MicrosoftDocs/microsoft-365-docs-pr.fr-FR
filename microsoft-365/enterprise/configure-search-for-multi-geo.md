---
title: Configurer la recherche pour Microsoft 365 Multi-Geo
ms.reviewer: adwood
ms.author: tlarsen
author: tklarsen
manager: arnek
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.custom: seo-marvel-mar2020
ms.collection: Strat_SP_gtc
localization_priority: Normal
f1.keywords:
- NOCSH
description: Découvrez comment configurer la recherche dans un environnement multigéogé. Seuls certains clients, tels que OneDrive Entreprise, peuvent renvoyer des résultats dans un environnement multigéogé.
ms.openlocfilehash: e213e93cfbc967a723b4d27f4b36a83fe6687da9
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47547151"
---
# <a name="configure-search-for-microsoft-365-multi-geo"></a><span data-ttu-id="6e214-104">Configurer la recherche pour Microsoft 365 Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="6e214-104">Configure Search for Microsoft 365 Multi-Geo</span></span>

<span data-ttu-id="6e214-105">Dans un environnement multigéographique, chaque emplacement géographique comporte son propre index de recherche et son centre de recherche.</span><span class="sxs-lookup"><span data-stu-id="6e214-105">In a multi-geo environment, each geo location has its own search index and Search Center.</span></span> <span data-ttu-id="6e214-106">Lorsqu’un utilisateur effectue une recherche, la requête est distribuée à tous les index et les résultats renvoyés sont fusionnés.</span><span class="sxs-lookup"><span data-stu-id="6e214-106">When a user searches, the query is fanned out to all the indexes, and the returned results are merged.</span></span>

<span data-ttu-id="6e214-107">Par exemple, un utilisateur d’un emplacement géographique peut rechercher du contenu stocké dans un autre emplacement géographique ou du contenu sur un site SharePoint limité à un emplacement géographique différent.</span><span class="sxs-lookup"><span data-stu-id="6e214-107">For example, a user in one geo location can search for content stored in another geo location, or for content on a SharePoint site that's restricted to a different geo location.</span></span> <span data-ttu-id="6e214-108">Si l’utilisateur a accès à ce contenu, la recherche affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="6e214-108">If the user has access to this content, search will show the result.</span></span>

## <a name="which-search-clients-work-in-a-multi-geo-environment"></a><span data-ttu-id="6e214-109">Quels sont les clients de recherche qui fonctionnent dans un environnement Multi-Géo ?</span><span class="sxs-lookup"><span data-stu-id="6e214-109">Which search clients work in a multi-geo environment?</span></span>

<span data-ttu-id="6e214-110">Ces clients peuvent renvoyer des résultats de tous les emplacements géographiques :</span><span class="sxs-lookup"><span data-stu-id="6e214-110">These clients can return results from all geo locations:</span></span>

- <span data-ttu-id="6e214-111">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="6e214-111">OneDrive for Business</span></span>
- <span data-ttu-id="6e214-112">Delve</span><span class="sxs-lookup"><span data-stu-id="6e214-112">Delve</span></span>
- <span data-ttu-id="6e214-113">Page d’accueil SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e214-113">The SharePoint home page</span></span>
- <span data-ttu-id="6e214-114">Centre de recherche</span><span class="sxs-lookup"><span data-stu-id="6e214-114">The Search Center</span></span>
- <span data-ttu-id="6e214-115">Applications de recherche personnalisée qui utilisent l’API de recherche SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e214-115">Custom search applications that use the SharePoint Search API</span></span>

### <a name="onedrive-for-business"></a><span data-ttu-id="6e214-116">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="6e214-116">OneDrive for Business</span></span>

<span data-ttu-id="6e214-117">Dès que l’environnement Multi-Géo est configuré, les utilisateurs qui effectuent des recherches dans OneDrive obtiennent des résultats de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-117">As soon as the multi-geo environment has been set up, users that search in OneDrive get results from all geo locations.</span></span>

### <a name="delve"></a><span data-ttu-id="6e214-118">Delve</span><span class="sxs-lookup"><span data-stu-id="6e214-118">Delve</span></span>

<span data-ttu-id="6e214-119">Dès que l’environnement Multi-Géo est configuré, les utilisateurs qui effectuent des recherches dans Delve obtiennent des résultats de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-119">As soon as the multi-geo environment has been set up, users that search in Delve get results from all geo locations.</span></span>

<span data-ttu-id="6e214-120">Le flux Delve et la fiche de profil n’affichent que les aperçus de fichiers stockés dans l’emplacement central.</span><span class="sxs-lookup"><span data-stu-id="6e214-120">The Delve feed and the profile card only show previews of files that are stored in the central location.</span></span> <span data-ttu-id="6e214-121">Pour les fichiers stockés dans des emplacements satellites, l’icône du type de fichier apparaît à la place.</span><span class="sxs-lookup"><span data-stu-id="6e214-121">For files that are stored in satellite locations, the icon for the file type is shown instead.</span></span>

### <a name="the-sharepoint-home-page"></a><span data-ttu-id="6e214-122">Page d’accueil SharePoint</span><span class="sxs-lookup"><span data-stu-id="6e214-122">The SharePoint home page</span></span>

<span data-ttu-id="6e214-p105">Dès que l’environnement Multi-Géo est configuré, les utilisateurs voient les actualités, les sites récents et les sites suivis de plusieurs emplacements géographiques sur leur page d’accueil SharePoint. S’ils utilisent la zone de recherche sur la page d’accueil SharePoint, ils obtiennent des résultats fusionnés provenant de plusieurs emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-p105">As soon as the multi-geo environment has been set up, users will see news, recent and followed sites from multiple geo locations on their SharePoint home page. If they use the search box on the SharePoint home page, they'll get merged results from multiple geo locations.</span></span>

### <a name="the-search-center"></a><span data-ttu-id="6e214-125">Centre de recherche</span><span class="sxs-lookup"><span data-stu-id="6e214-125">The Search Center</span></span>

<span data-ttu-id="6e214-p106">Une fois que l’environnement Multi-Géo est configuré, chaque centre de recherche continue à afficher uniquement les résultats de son propre emplacement géographique. Les administrateurs doivent [modifier les paramètres de chaque centre de recherche](#_Set_up_a_1) pour obtenir des résultats de tous les emplacements géographiques. Par la suite, les utilisateurs qui effectuent une recherche dans le centre de recherche obtiennent des résultats de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-p106">After the multi-geo environment has been set up, each Search Center continues to only show results from their own geo location. Admins must [change the settings of each Search Center](#_Set_up_a_1) to get results from all geo locations. Afterwards, users that search in the Search Center get results from all geo locations.</span></span>

### <a name="custom-search-applications"></a><span data-ttu-id="6e214-129">Applications de recherche personnalisée</span><span class="sxs-lookup"><span data-stu-id="6e214-129">Custom search applications</span></span>

<span data-ttu-id="6e214-p107">Comme d’habitude, les applications de recherche personnalisée interagissent avec les index de recherche en utilisant les API REST de recherche SharePoint existantes. Pour obtenir des résultats de tous les emplacements géographiques (ou une partie), l’application doit [appeler l’API et inclure les nouveaux paramètres de requête Multi-Géo](#_Get_custom_search) dans la demande. Cela déclenche une distribution ramifiée de la requête à tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-p107">As usual, custom search applications interact with the search indexes by using the existing SharePoint Search REST APIs. To get results from all, or some geo locations, the application must [call the API and include the new Multi-Geo query parameters](#_Get_custom_search) in the request. This triggers a fan out of the query to all geo locations.</span></span>

## <a name="whats-different-about-search-in-a-multi-geo-environment"></a><span data-ttu-id="6e214-133">Quelles différences la recherche présente-t-elle dans un environnement multigéographique ?</span><span class="sxs-lookup"><span data-stu-id="6e214-133">What's different about search in a multi-geo environment?</span></span>

<span data-ttu-id="6e214-134">Certaines fonctionnalités de recherche auxquelles vous êtes habitué fonctionnent différemment dans un environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-134">Some search features you might be familiar with, work differently in a multi-geo environment.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e214-135"><strong>Fonctionnalité</strong></span><span class="sxs-lookup"><span data-stu-id="6e214-135"><strong>Feature</strong></span></span></th>
<th align="left"><span data-ttu-id="6e214-136"><strong>Fonctionnement</strong></span><span class="sxs-lookup"><span data-stu-id="6e214-136"><strong>How it works</strong></span></span></th>
<th align="left"><span data-ttu-id="6e214-137"><strong>Solution de contournement</strong></span><span class="sxs-lookup"><span data-stu-id="6e214-137"><strong>Workaround</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-138">Résultats promus</span><span class="sxs-lookup"><span data-stu-id="6e214-138">Promoted results</span></span></td>
<td align="left"><span data-ttu-id="6e214-139">Vous pouvez créer des règles de requête avec des résultats promus à différents niveaux : pour le client entier, pour une collection de sites ou pour un site.</span><span class="sxs-lookup"><span data-stu-id="6e214-139">You can create query rules with promoted results at different levels: for the whole tenant, for a site collection, or for a site.</span></span> <span data-ttu-id="6e214-140">Dans un environnement multigéographique, définissez les résultats promus au niveau du client pour promouvoir les résultats aux centres de recherche de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-140">In a multi-geo environment, define promoted results at the tenant level to promote the results to the Search Centers in all geo locations.</span></span> <span data-ttu-id="6e214-141">Si vous souhaitez seulement promouvoir les résultats dans le centre de recherche qui se trouve dans l’emplacement géographique de la collection de sites ou du site, définissez les résultats promus au niveau de la collection de sites ou du site.</span><span class="sxs-lookup"><span data-stu-id="6e214-141">If you only want to promote results in the Search Center that's in the geo location of the site collection or site, define the promoted results at the site collection or site level.</span></span> <span data-ttu-id="6e214-142">Ces résultats ne sont pas promus dans d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-142">These results are not promoted in other geo locations.</span></span></td>
<td align="left"><span data-ttu-id="6e214-143">Si vous n’avez pas besoin d’autres résultats promus par emplacement géographique (par exemple, des règles différentes pour les déplacements), nous vous recommandons de définir les résultats promus au niveau du client.</span><span class="sxs-lookup"><span data-stu-id="6e214-143">If you don't need different promoted results per geo location, for example different rules for traveling, we recommend defining promoted results at the tenant level.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-144">Affinements de la recherche</span><span class="sxs-lookup"><span data-stu-id="6e214-144">Search refiners</span></span></td>
<td align="left"><span data-ttu-id="6e214-p109">La recherche renvoie des affinements de tous les emplacements géographiques d’un client puis les regroupe. Le regroupement est ce qu’il y a de mieux, ce qui signifie que le nombre d’affinements peut ne pas être précis à 100 %. Pour la plupart des scénarios de recherche, cette précision est suffisante. </span><span class="sxs-lookup"><span data-stu-id="6e214-p109">Search returns refiners from all the geo locations of a tenant and then aggregates them. The aggregation is a best effort, meaning that the refiner counts might not be 100% accurate. For most search-driven scenarios, this accuracy is sufficient. </span></span></td>
<td align="left"><span data-ttu-id="6e214-148">Pour les applications basées sur la recherche qui dépendent de l’intégralité de l’affinement, effectuez une requête indépendante sur chaque emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-148">For search-driven applications that depend on refiner completeness, query each geo location independently.</span></span></td>
</tr>
<tr class="odd">
<td align="left"></td>
<td align="left"><span data-ttu-id="6e214-149">La recherche multigéographique ne prend pas en charge la création dynamique de compartiments pour les affinements numériques.</span><span class="sxs-lookup"><span data-stu-id="6e214-149">Multi-geo search doesn't support dynamic bucketing for numerical refiners.</span></span></td>
<td align="left"><span data-ttu-id="6e214-150">Utilisez le <a href="https://docs.microsoft.com/sharepoint/dev/general-development/query-refinement-in-sharepoint">paramètre « Discretize » pour</a> les affinements numériques.</span><span class="sxs-lookup"><span data-stu-id="6e214-150">Use the <a href="https://docs.microsoft.com/sharepoint/dev/general-development/query-refinement-in-sharepoint">"Discretize" parameter</a> for numerical refiners.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-151">ID de document</span><span class="sxs-lookup"><span data-stu-id="6e214-151">Document IDs</span></span></td>
<td align="left"><span data-ttu-id="6e214-152">Si vous développez une application basée sur la recherche qui dépend des ID de document, notez que les ID de document d’un environnement multigéographique ne sont pas uniques parmi les emplacements géographiques, mais le sont par emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-152">If you're developing a search-driven application that depends on document IDs, note that document IDs in a multi-geo environment aren't unique across geo locations, they are unique per geo location.</span></span></td>
<td align="left"><span data-ttu-id="6e214-153">Nous avons ajouté une colonne qui identifie l’emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-153">We've added a column that identifies the geo location.</span></span> <span data-ttu-id="6e214-154">Utilisez cette colonne pour atteindre l’unicité.</span><span class="sxs-lookup"><span data-stu-id="6e214-154">Use this column to achieve uniqueness.</span></span> <span data-ttu-id="6e214-155">Cette colonne est nommée « GeoLocationSource ».</span><span class="sxs-lookup"><span data-stu-id="6e214-155">This column is named "GeoLocationSource".</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-156">Nombre de résultats</span><span class="sxs-lookup"><span data-stu-id="6e214-156">Number of results</span></span></td>
<td align="left"><span data-ttu-id="6e214-157">La page des résultats de recherche affiche les résultats combinés des emplacements géographiques, mais il n’est pas possible d’afficher plus de 500 résultats par page.</span><span class="sxs-lookup"><span data-stu-id="6e214-157">The search results page shows combined results from the geo locations, but it's not possible to page beyond 500 results.</span></span></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-158">Recherche hybride</span><span class="sxs-lookup"><span data-stu-id="6e214-158">Hybrid search</span></span></td>
<td align="left"><span data-ttu-id="6e214-159">Dans un environnement SharePoint hybride avec <a href="https://docs.microsoft.com/sharepoint/hybrid/learn-about-cloud-hybrid-search-for-sharepoint">recherche hybride dans le cloud</a>, le contenu local est ajouté à l’index Microsoft 365 de l’emplacement central.</span><span class="sxs-lookup"><span data-stu-id="6e214-159">In a hybrid SharePoint environment with <a href="https://docs.microsoft.com/sharepoint/hybrid/learn-about-cloud-hybrid-search-for-sharepoint">cloud hybrid search</a>,  on-premises content is added to the Microsoft 365 index of the central location.</span></span></td>
<td align="left"></td>
</tr>
</tbody>
</table>

## <a name="whats-not-supported-for-search-in-a-multi-geo-environment"></a><span data-ttu-id="6e214-160">Quels sont les éléments qui ne sont pas pris en charge par la recherche dans un environnement multigéographique ?</span><span class="sxs-lookup"><span data-stu-id="6e214-160">What's not supported for search in a multi-geo environment?</span></span>

<span data-ttu-id="6e214-161">Certaines fonctionnalités de recherche auxquelles vous êtes habitué ne sont pas prises en charge dans un environnement multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-161">Some of the search features you might be familiar with, aren't supported in a multi-geo environment.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e214-162"><strong>Fonctionnalité de recherche</strong></span><span class="sxs-lookup"><span data-stu-id="6e214-162"><strong>Search feature</strong></span></span></th>
<th align="left"><span data-ttu-id="6e214-163"><strong>Remarque</strong></span><span class="sxs-lookup"><span data-stu-id="6e214-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-164">Authentification d’application uniquement</span><span class="sxs-lookup"><span data-stu-id="6e214-164">App-only authentication</span></span></td>
<td align="left"><span data-ttu-id="6e214-165">L’authentification d’application uniquement (accès privilégié depuis les services) n’est pas prise en charge dans la recherche multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-165">App-only authentication (privileged access from services) isn't supported in multi-geo search.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-166">Utilisateurs invités</span><span class="sxs-lookup"><span data-stu-id="6e214-166">Guest users</span></span></td>
<td align="left"><span data-ttu-id="6e214-167">Les utilisateurs invités obtiennent uniquement les résultats de l’emplacement géographique à partir duquel ils effectuent leur recherche.</span><span class="sxs-lookup"><span data-stu-id="6e214-167">Guest users only get results from the geo location that they're searching from.</span></span></td>
</tr>
</tbody>
</table>

## <a name="how-does-search-work-in-a-multi-geo-environment"></a><span data-ttu-id="6e214-168">Comment fonctionne la recherche dans un environnement multigéographique ?</span><span class="sxs-lookup"><span data-stu-id="6e214-168">How does search work in a multi-geo environment?</span></span>

<span data-ttu-id="6e214-169">Tous les clients de recherche utilisent les API REST de recherche SharePoint existantes pour interagir avec les index de recherche.</span><span class="sxs-lookup"><span data-stu-id="6e214-169">All the search clients use the existing SharePoint Search REST APIs to interact with the search indexes.</span></span>

![Diagramme montrant comment les API REST de recherche SharePoint interagissent avec les index de recherche](../media/configure-search-for-multi-geo-image1-1.png)

1. <span data-ttu-id="6e214-171">Un client de recherche appelle le point de terminaison REST de recherche avec la propriété de requête EnableMultiGeoSearch= true.</span><span class="sxs-lookup"><span data-stu-id="6e214-171">A search client calls the Search REST endpoint with the query property EnableMultiGeoSearch= true.</span></span>
2. <span data-ttu-id="6e214-172">La requête est envoyée à tous les emplacements géographiques dans le client.</span><span class="sxs-lookup"><span data-stu-id="6e214-172">The query is sent to all geo locations in the tenant.</span></span>
3. <span data-ttu-id="6e214-173">Les résultats de recherche de chaque emplacement géographique sont fusionnés et classés.</span><span class="sxs-lookup"><span data-stu-id="6e214-173">Search results from each geo location are merged and ranked.</span></span>
4. <span data-ttu-id="6e214-174">Le client obtient des résultats de recherche unifiés.</span><span class="sxs-lookup"><span data-stu-id="6e214-174">The client gets unified search results.</span></span>

<span data-ttu-id="6e214-175"><span id="_Set_up_a" class="anchor"><span id="_Ref501388384" class="anchor"></span></span>Notez que nous ne fusionnons pas les résultats de recherche avant d’avoir reçu les résultats de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-175"><span id="_Set_up_a" class="anchor"><span id="_Ref501388384" class="anchor"></span></span>Notice that we don't merge the search results until we've received results from all the geo locations.</span></span> <span data-ttu-id="6e214-176">Cela signifie que les recherches géographiques multiples souffrent d’une latence supplémentaire par rapport aux recherches dans un environnement ne comportant qu’un seul emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-176">This means that multi-geo searches have additional latency compared to searches in an environment with only one geo location.</span></span>

<span id="_Set_up_a_1" class="anchor"><span id="_Ref505252370" class="anchor"></span></span>
## <a name="get-a-search-center-to-show-results-from-all-geo-locations"></a><span data-ttu-id="6e214-177">Obtenir un centre de recherche pour afficher les résultats de tous les emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-177">Get a Search Center to show results from all geo locations</span></span>

<span data-ttu-id="6e214-178">Chaque centre de recherche possède plusieurs secteurs verticaux et vous devez configurer chaque secteur vertical individuellement.</span><span class="sxs-lookup"><span data-stu-id="6e214-178">Each Search Center has several verticals and you have to set up each vertical individually.</span></span>

1. <span data-ttu-id="6e214-179">Vérifiez que vous effectuez ces étapes avec un compte doté d’autorisations pour modifier la page des résultats de la recherche et le composant WebPart Search Result.</span><span class="sxs-lookup"><span data-stu-id="6e214-179">Ensure that you perform these steps with an account that has permission to edit the search results page and the Search Result Web Part.</span></span>

2. <span data-ttu-id="6e214-180">Accédez à la page des résultats de la recherche (reportez-vous à la [liste](https://support.office.com/article/174d36e0-2f85-461a-ad9a-8b3f434a4213) des pages des résultats de la recherche)</span><span class="sxs-lookup"><span data-stu-id="6e214-180">Navigate to the search results page (see the [list](https://support.office.com/article/174d36e0-2f85-461a-ad9a-8b3f434a4213) of search results pages)</span></span>

3. <span data-ttu-id="6e214-p112">Sélectionnez le secteur vertical à configurer, cliquez sur l’icône d’engrenage **Paramètres** située en haut à droite, puis cliquez sur **Modifier la page**. La page des résultats de la recherche s’ouvre en mode Édition.</span><span class="sxs-lookup"><span data-stu-id="6e214-p112">Select the vertical to set up, click **Settings** gear icon in the upper, right corner, and then click **Edit Page**. The search results page opens in Edit mode.</span></span>

   ![Modifier la sélection de page dans Paramètres](../media/configure-search-for-multi-geo-image2.png)

4. <span data-ttu-id="6e214-184">Dans le composant WebPart de résultats de recherche, déplacez le pointeur vers le coin supérieur droit et cliquez sur la flèche, puis sur **Modifier le composant WebPart** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="6e214-184">In the Search Results Web Part, move the pointer to the upper, right corner of the web part, click the arrow, and then click **Edit Web Part** on the menu.</span></span> <span data-ttu-id="6e214-185">Le volet des outils du composant WebPart des résultats de recherche s’ouvre sous le ruban en haut à droite de la page.</span><span class="sxs-lookup"><span data-stu-id="6e214-185">The Search Results Web Part tool pane opens under the ribbon in the top right of the page.</span></span>

   ![Modifier la sélection de la partie Web](../media/configure-search-for-multi-geo-image3.png)

5. <span data-ttu-id="6e214-187">Dans le volet des outils du composant WebPart, dans la section **Paramètres**, sous **Paramètres de contrôle des résultats**, sélectionnez **Afficher les résultats multigéographiques** pour que le composant WebPart Résultats de la recherche affiche les résultats de tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-187">In the Web Part tool pane, in the **Settings** section, under **Results control settings**, select **Show Multi-Geo results** to get the Search Results Web Part to show results from all geo locations.</span></span>

6. <span data-ttu-id="6e214-188">Cliquez sur **OK** pour enregistrer vos changements et fermer le volet des outils du composant WebPart.</span><span class="sxs-lookup"><span data-stu-id="6e214-188">Click **OK** to save your change and close the Web Part tool pane.</span></span>

7. <span data-ttu-id="6e214-189">Vérifiez les changements que vous avez apportés au composant WebPart Résultats de la recherche en cliquant sur **Archiver** sur l’onglet Page du menu principal.</span><span class="sxs-lookup"><span data-stu-id="6e214-189">Check your changes to the Search Results Web Part by clicking **Check-In** on the Page tab of the main menu.</span></span>

8. <span data-ttu-id="6e214-190">Publiez les changements en utilisant le lien fourni dans la note en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="6e214-190">Publish the changes by using the link provided in the note at the top of the page.</span></span>

<span id="_Get_custom_search" class="anchor"><span id="_Ref501388387" class="anchor"></span></span>
## <a name="get-custom-search-applications-to-show-results-from-all-or-some-geo-locations"></a><span data-ttu-id="6e214-191">Configurer des applications de recherche personnalisée pour qu’elles affichent les résultats de l’ensemble ou d’une partie des emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-191">Get custom search applications to show results from all or some geo locations</span></span>

<span data-ttu-id="6e214-p114">Les applications de recherche personnalisée obtiennent les résultats de l’ensemble (ou d’une partie) des emplacements géographiques en spécifiant des paramètres de requête avec la demande à l’API REST de recherche SharePoint. Selon les paramètres, la requête est distribuée à tous les emplacements géographiques ou à certains emplacements géographiques. Par exemple, si vous devez seulement interroger un sous-ensemble des emplacements géographiques pour rechercher des informations pertinentes, vous pouvez contrôler la distribution ramifiée à ces derniers uniquement. Si la demande fonctionne, l’API REST de recherche SharePoint renvoie des données de réponse.</span><span class="sxs-lookup"><span data-stu-id="6e214-p114">Custom search applications get results from all, or some, geo locations by specifying query parameters with the request to the SharePoint Search REST API. Depending on the query parameters, the query is fanned out to all geo locations, or to some geo locations. For example, if you only need to query a subset of geo locations to find relevant information, you can control the fan out to only these. If the request succeeds, the SharePoint Search REST API returns response data.</span></span>

### <a name="requirement"></a><span data-ttu-id="6e214-196">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="6e214-196">Requirement</span></span>

<span data-ttu-id="6e214-197">Pour chaque emplacement géographique, vous devez vous assurer que tous les utilisateurs de l’organisation ont reçu l’autorisation de **lecture** du site web racine (par exemple contoso **APAC**.sharepoint.com/ et contoso **EU**.sharepoint.com/).</span><span class="sxs-lookup"><span data-stu-id="6e214-197">For each geo location, you must ensure that all users in the organization have been granted the **Read** permission level for the root website (for example contoso **APAC**.sharepoint.com/ and contoso **EU**.sharepoint.com/).</span></span> <span data-ttu-id="6e214-198">[En savoir plus sur les autorisations](https://support.office.com/article/understanding-permission-levels-in-sharepoint-87ecbb0e-6550-491a-8826-c075e4859848).</span><span class="sxs-lookup"><span data-stu-id="6e214-198">[Learn about permissions](https://support.office.com/article/understanding-permission-levels-in-sharepoint-87ecbb0e-6550-491a-8826-c075e4859848).</span></span>

### <a name="query-parameters"></a><span data-ttu-id="6e214-199">Paramètres de requête</span><span class="sxs-lookup"><span data-stu-id="6e214-199">Query parameters</span></span>

<span data-ttu-id="6e214-200">EnableMultiGeoSearch : il s’agit une valeur booléenne qui spécifie si la requête doit être étendue aux index des autres emplacements géographiques du client multigéographique.</span><span class="sxs-lookup"><span data-stu-id="6e214-200">EnableMultiGeoSearch - This is a Boolean value that specifies whether the query shall be fanned out to the indexes of other geo locations of the multi-geo tenant.</span></span> <span data-ttu-id="6e214-201">Définissez-la sur **true** pour étendre la requête et sur **false** pour ne pas l’étendre.</span><span class="sxs-lookup"><span data-stu-id="6e214-201">Set it to **true** to fan out the query; **false** to not fan out the query.</span></span> <span data-ttu-id="6e214-202">Si vous n’incluez pas ce paramètre, la valeur par défaut est **false**, sauf lorsque vous effectuez un appel de l’API REST contre un site qui utilise le modèle Centre de recherche d’entreprise, dans ce cas, la valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="6e214-202">If you don't include this parameter, the default value is **false**, except when making a REST API call against a site which uses the Enterprise Search Center template, in this case the default value is **true**.</span></span> <span data-ttu-id="6e214-203">Si vous utilisez ce paramètre dans un environnement qui n’est pas multigéographique, le paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6e214-203">If you use the parameter in an environment that isn't multi-geo, the parameter is ignored.</span></span>

<span data-ttu-id="6e214-204">TypeClient : il s’agit d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="6e214-204">ClientType - This is a string.</span></span> <span data-ttu-id="6e214-205">Entrez un nom de client unique pour chaque application de recherche.</span><span class="sxs-lookup"><span data-stu-id="6e214-205">Enter a unique client name for each search application.</span></span> <span data-ttu-id="6e214-206">Si vous n’incluez pas ce paramètre, la requête n’est pas étendue à d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-206">If you don't include this parameter, the query is not fanned out to other geo locations.</span></span>

<span data-ttu-id="6e214-207">MultiGeoSearchConfiguration : il s’agit d’une liste facultative d’emplacements géographiques dans le client multigéographique pour étendre la requête lorsque **EnableMultiGeoSearch** est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="6e214-207">MultiGeoSearchConfiguration - This is an optional list of which geo locations in the multi-geo tenant to fan the query out to when **EnableMultiGeoSearch** is **true**.</span></span> <span data-ttu-id="6e214-208">Si vous n’incluez pas ce paramètre ou que vous le laissez vide, la requête est étendue à d’autres emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-208">If you don't include this parameter, or leave it blank, the query is fanned out to all geo locations.</span></span> <span data-ttu-id="6e214-209">Pour chaque emplacement géographique, entrez les éléments suivants au format JSON :</span><span class="sxs-lookup"><span data-stu-id="6e214-209">For each geo location, enter the following items, in JSON format:</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e214-210">Option</span><span class="sxs-lookup"><span data-stu-id="6e214-210">Item</span></span></th>
<th align="left"><span data-ttu-id="6e214-211">Description</span><span class="sxs-lookup"><span data-stu-id="6e214-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-212">DataLocation</span><span class="sxs-lookup"><span data-stu-id="6e214-212">DataLocation</span></span></td>
<td align="left"><span data-ttu-id="6e214-213">L’emplacement géographique, par exemple NAM.</span><span class="sxs-lookup"><span data-stu-id="6e214-213">The geo location, for example NAM.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-214">EndPoint</span><span class="sxs-lookup"><span data-stu-id="6e214-214">EndPoint</span></span></td>
<td align="left"><span data-ttu-id="6e214-215">Le point de terminaison auquel se connecter, par exemple https://contoso.sharepoint.com</span><span class="sxs-lookup"><span data-stu-id="6e214-215">The endpoint to connect to, for example https://contoso.sharepoint.com</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-216">SourceId</span><span class="sxs-lookup"><span data-stu-id="6e214-216">SourceId</span></span></td>
<td align="left"><span data-ttu-id="6e214-217">GUID de l’origine des résultats, par exemple B81EAB55-3140-4312-B0F4-9459D1B4FFEE.</span><span class="sxs-lookup"><span data-stu-id="6e214-217">The GUID of the result source, for example B81EAB55-3140-4312-B0F4-9459D1B4FFEE.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6e214-p119">Si vous omettez DataLocation ou EndPoint, ou si une DataLocation est dupliquée, la demande échoue. [Vous pouvez obtenir des informations sur le point de terminaison des emplacements géographiques d’un client à l’aide de Microsoft Graph](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-discovery).</span><span class="sxs-lookup"><span data-stu-id="6e214-p119">If you omit DataLocation or EndPoint, or if a DataLocation is duplicated, the request fails. [You can get information about the endpoint of a tenant's geo locations by using Microsoft Graph](https://docs.microsoft.com/sharepoint/dev/solution-guidance/multigeo-discovery).</span></span>

### <a name="response-data"></a><span data-ttu-id="6e214-220">Données de réponse</span><span class="sxs-lookup"><span data-stu-id="6e214-220">Response data</span></span>

<span data-ttu-id="6e214-p120">MultiGeoSearchStatus : il s’agit d’une propriété renvoyée par l’API de recherche SharePoint en réponse à une demande. La valeur de la propriété est une chaîne et fournit les informations suivantes sur les résultats renvoyés par l’API de recherche SharePoint :</span><span class="sxs-lookup"><span data-stu-id="6e214-p120">MultiGeoSearchStatus – This is a property that the SharePoint Search API returns in response to a request. The value of the property is a string and gives the following information about the results that the SharePoint Search API returns:</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e214-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e214-223">Value</span></span></th>
<th align="left"><span data-ttu-id="6e214-224">Description</span><span class="sxs-lookup"><span data-stu-id="6e214-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-225">Complet</span><span class="sxs-lookup"><span data-stu-id="6e214-225">Full</span></span></td>
<td align="left"><span data-ttu-id="6e214-226">Résultats complets de <strong>tous</strong> les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="6e214-226">Full results from <strong>all</strong> the geo locations.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="6e214-227">Partielle</span><span class="sxs-lookup"><span data-stu-id="6e214-227">Partial</span></span></td>
<td align="left"><span data-ttu-id="6e214-p121">Résultats partiels d’un ou plusieurs emplacements géographiques. Les résultats sont incomplets en raison d’une erreur temporaire.</span><span class="sxs-lookup"><span data-stu-id="6e214-p121">Partial results from one or more geo locations. The results are incomplete due to a transient error.</span></span></td>
</tr>
</tbody>
</table>

### <a name="query-using-the-rest-service"></a><span data-ttu-id="6e214-230">Requête à l’aide du service REST</span><span class="sxs-lookup"><span data-stu-id="6e214-230">Query using the REST service</span></span>

<span data-ttu-id="6e214-p122">Avec une demande GET, spécifiez les paramètres de la requête dans l’URL. Avec une demande POST, vous transmettez les paramètres de la requête dans le corps au format JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="6e214-p122">With a GET request, you specify the query parameters in the URL. With a POST request, you pass the query parameters in the body in JavaScript Object Notation (JSON) format.</span></span>

#### <a name="request-headers"></a><span data-ttu-id="6e214-233">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6e214-233">Request headers</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e214-234">Nom</span><span class="sxs-lookup"><span data-stu-id="6e214-234">Name</span></span></th>
<th align="left"><span data-ttu-id="6e214-235">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e214-235">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="6e214-236">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6e214-236">Content-Type</span></span></td>
<td align="left"><span data-ttu-id="6e214-237">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="6e214-237">application/json;odata=verbose</span></span></td>
</tr>
</tbody>
</table>

#### <a name="sample-get-request-thats-fanned-out-to-all-geo-locations"></a><span data-ttu-id="6e214-238">Exemple de demande GET étendue à **tous** les emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-238">Sample GET request that's fanned out to **all** geo locations</span></span>

<span data-ttu-id="6e214-239"> https:// \<tenant\> / \_ api/search/query?querytext='sharepoint'&Properties='EnableMultiGeoSearch:true'&ClientType='my \_ client \_ id'</span><span class="sxs-lookup"><span data-stu-id="6e214-239">https:// \<tenant\>/\_api/search/query?querytext='sharepoint'&Properties='EnableMultiGeoSearch:true'&ClientType='my\_client\_id'</span></span>

#### <a name="sample-get-request-to-fan-out-to-some-geo-locations"></a><span data-ttu-id="6e214-240">Exemple de demande GET à distribuer à **certains** emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-240">Sample GET request to fan out to **some** geo locations</span></span>

<span data-ttu-id="6e214-241"> https:// \<tenant\> / \_ api/search/query?querytext='site'&ClientType='my_client_id'&Properties='EnableMultiGeoSearch:true, MultiGeoSearchConfiguration:[{DataLocation \\ :"NAM » \\ ,Endpoint \\ :"https \\ ://contosoNAM.sharepoint.com » \\ ,SourceId \\ :"B81EAB55-3140-4312-B0F4-9459D1B4FFEE"} \\ ,{DataLocation \\ :"CAN » \\ ,Endpoint \\ :"https \\ ://contosoCAN.sharepoint-df.com"}]'</span><span class="sxs-lookup"><span data-stu-id="6e214-241">https:// \<tenant\>/\_api/search/query?querytext='site'&ClientType='my_client_id'&Properties='EnableMultiGeoSearch:true, MultiGeoSearchConfiguration:[{DataLocation\\:"NAM"\\,Endpoint\\:"https\\://contosoNAM.sharepoint.com"\\,SourceId\\:"B81EAB55-3140-4312-B0F4-9459D1B4FFEE"}\\,{DataLocation\\:"CAN"\\,Endpoint\\:"https\\://contosoCAN.sharepoint-df.com"}]'</span></span>

> [!NOTE]
> <span data-ttu-id="6e214-242">Les symboles virgule et deux-points de la liste des emplacements géographiques pour la propriété MultiGeoSearchConfiguration sont précédés par le caractère **barre oblique inverse**,</span><span class="sxs-lookup"><span data-stu-id="6e214-242">Commas and colons in the list of geo locations for the MultiGeoSearchConfiguration property are preceded by the **backslash** character.</span></span> <span data-ttu-id="6e214-243">car les demandes GET utilisent des syboles deux-points pour séparer les propriétés, et des virgules pour séparer les arguments des propriétés.</span><span class="sxs-lookup"><span data-stu-id="6e214-243">This is because GET requests use colons to separate properties and commas to separate arguments of properties.</span></span> <span data-ttu-id="6e214-244">Sans barre oblique inverse comme caractère d’échappement, la propriété MultiGeoSearchConfiguration est interprétée de façon erronée.</span><span class="sxs-lookup"><span data-stu-id="6e214-244">Without the backslash as an escape character, the MultiGeoSearchConfiguration property is interpreted wrongly.</span></span>

#### <a name="sample-post-request-thats-fanned-out-to-all-geo-locations"></a><span data-ttu-id="6e214-245">Exemple de demande POST étendue à **tous** les emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-245">Sample POST request that's fanned out to **all** geo locations</span></span>

```text
    {
    "request": {
            "__metadata": {
            "type": "Microsoft.Office.Server.Search.REST.SearchRequest"
        },
        "Querytext": "sharepoint",
        "Properties": {
            "results": [
                {
                    "Name": "EnableMultiGeoSearch",
                    "Value": {
                        "QueryPropertyValueTypeIndex": 3,
                        "BoolVal": true
                    }
                }
            ]
        },
        "ClientType": "my_client_id"
        }
    }
```

#### <a name="sample-post-request-thats-fanned-out-to-some-geo-locations"></a><span data-ttu-id="6e214-246">Exemple de demande POST étendue à **certains** emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="6e214-246">Sample POST request that's fanned out to **some** geo locations</span></span>

```text
    {
        "request": {
            "Querytext": "SharePoint",
            "ClientType": "my_client_id",
            "Properties": {
                "results": [
                    {
                        "Name": "EnableMultiGeoSearch",
                        "Value": {
                            "QueryPropertyValueTypeIndex": 3,
                            "BoolVal": true
                        }
                    },
                    {
                        "Name": "MultiGeoSearchConfiguration",
                        "Value": {
                        "StrVal": "[{\"DataLocation\":\"NAM\",\"Endpoint\":\"https://contoso.sharepoint.com\",\"SourceId\":\"B81EAB55-3140-4312-B0F4-9459D1B4FFEE\"},{\"DataLocation\":\"CAN\",\"Endpoint\":\"https://contosoCAN.sharepoint.com\"}]",
                            "QueryPropertyValueTypeIndex": 1
                        }
                    }
                ]
            }
        }
    }
```

### <a name="query-using-csom"></a><span data-ttu-id="6e214-247">Requête utilisant CSOM</span><span class="sxs-lookup"><span data-stu-id="6e214-247">Query using CSOM</span></span>

<span data-ttu-id="6e214-248">Voici un exemple de requête CSOM étendue à **tous** les emplacements géographiques :</span><span class="sxs-lookup"><span data-stu-id="6e214-248">Here's a sample CSOM query that's fanned out to **all** geo locations:</span></span>

```text
var keywordQuery = new KeywordQuery(ctx);
keywordQuery.QueryText = query.SearchQueryText;
keywordQuery.ClientType = <enter a string here>;
keywordQuery["EnableMultiGeoSearch"] = true;
```
