---
title: Service web d’URL et d’adresses IP Office 365
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 8/6/2019
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- m365initiative-coredeploy
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.reviewer: pandrew
search.appverid:
- MET150
- MOE150
- BCS160
description: Découvrez comment utiliser l’adresse IP et le service web d’URL Office 365 pour mieux identifier et différencier le trafic réseau d’Office 365.
ms.openlocfilehash: 1948491e1d3db724e7b7b6a5275234acab4be08a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918953"
---
# <a name="office-365-ip-address-and-url-web-service"></a><span data-ttu-id="884ae-103">Service web d’URL et d’adresses IP Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-103">Office 365 IP Address and URL web service</span></span>

<span data-ttu-id="884ae-104">L’adresse IP Office 365 et le service Web URL vous aident à mieux identifier et différencier le trafic réseau d’Office 365, ce qui vous permet d’évaluer, de configurer et de rester à jour avec les modifications.</span><span class="sxs-lookup"><span data-stu-id="884ae-104">The Office 365 IP Address and URL web service helps you better identify and differentiate Office 365 network traffic, making it easier for you to evaluate, configure, and stay up to date with changes.</span></span> <span data-ttu-id="884ae-105">Ce service Web basé sur REST remplace les anciens fichiers XML téléchargés, qui ont été supprimés le 2 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="884ae-105">This REST-based web service replaces the previous XML downloadable files, which were phased out on October 2, 2018.</span></span>

<span data-ttu-id="884ae-106">En tant que fournisseur de périphériques de périmètre réseau ou client, vous pouvez créer le service Web pour les entrées d’adresse IP et de nom de domaine complet Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-106">As a customer or a network perimeter device vendor, you can build against the web service for Office 365 IP address and FQDN entries.</span></span> <span data-ttu-id="884ae-107">Vous pouvez accéder aux données directement dans un navigateur Web à l’aide des URL suivantes :</span><span class="sxs-lookup"><span data-stu-id="884ae-107">You can access the data directly in a web browser using these URLs:</span></span>

- <span data-ttu-id="884ae-108">Pour obtenir la dernière version des URL et plages d’adresses IP Office 365, utilisez [https://endpoints.office.com/version](https://endpoints.office.com/version?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span><span class="sxs-lookup"><span data-stu-id="884ae-108">For the latest version of the Office 365 URLs and IP address ranges, use [https://endpoints.office.com/version](https://endpoints.office.com/version?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span></span>
- <span data-ttu-id="884ae-109">Pour les données sur la page des URL et plages d’adresses IP Office 365 pour les pare-feux et les serveurs proxy, utilisez [https://endpoints.office.com/endpoints/worldwide](https://endpoints.office.com/endpoints/worldwide?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span><span class="sxs-lookup"><span data-stu-id="884ae-109">For the data on the Office 365 URLs and IP address ranges page for firewalls and proxy servers, use [https://endpoints.office.com/endpoints/worldwide](https://endpoints.office.com/endpoints/worldwide?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span></span>
- <span data-ttu-id="884ae-110">Pour obtenir les dernières modifications depuis juillet 2018, date de première mise à disposition du service web, utilisez [https://endpoints.office.com/changes/worldwide/0000000000](https://endpoints.office.com/changes/worldwide/0000000000?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span><span class="sxs-lookup"><span data-stu-id="884ae-110">To get all the latest changes since July 2018 when the web service was first available, use [https://endpoints.office.com/changes/worldwide/0000000000](https://endpoints.office.com/changes/worldwide/0000000000?clientrequestid=b10c5ed1-bad1-445f-b386-b919946339a7).</span></span>

<span data-ttu-id="884ae-111">En tant que client, vous pouvez utiliser ce service web pour :</span><span class="sxs-lookup"><span data-stu-id="884ae-111">As a customer, you can use this web service to:</span></span>

- <span data-ttu-id="884ae-112">mettre à jour vos scripts PowerShell et obtenir des données de point de terminaison Office 365 et modifier la mise en forme de vos périphériques réseau ;</span><span class="sxs-lookup"><span data-stu-id="884ae-112">Update your PowerShell scripts to obtain Office 365 endpoint data and modify any formatting for your networking devices.</span></span>
- <span data-ttu-id="884ae-113">utiliser ces informations pour mettre à jour des fichiers PAC déployés sur des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="884ae-113">Use this information to update PAC files deployed to client computers.</span></span>

<span data-ttu-id="884ae-114">En tant que fournisseur de périphérique de périmètre réseau, vous pouvez utiliser ce service web pour :</span><span class="sxs-lookup"><span data-stu-id="884ae-114">As a network perimeter device vendor, you can use this web service to:</span></span>

- <span data-ttu-id="884ae-115">créer et tester le logiciel du périphérique pour télécharger la liste pour une configuration automatisée ;</span><span class="sxs-lookup"><span data-stu-id="884ae-115">Create and test device software to download the list for automated configuration.</span></span>
- <span data-ttu-id="884ae-116">rechercher la version actuelle ;</span><span class="sxs-lookup"><span data-stu-id="884ae-116">Check for the current version.</span></span>
- <span data-ttu-id="884ae-117">obtenir les modifications actuelles.</span><span class="sxs-lookup"><span data-stu-id="884ae-117">Get the current changes.</span></span>

> [!NOTE]
> <span data-ttu-id="884ae-118">Si vous utilisez Azure ExpressRoute pour vous connecter à Office 365, consultez [Azure ExpressRoute pour Office 365](azure-expressroute.md) pour vous familiariser avec les services Office 365 pris en charge sur Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="884ae-118">If you are using Azure ExpressRoute to connect to Office 365, please review [Azure ExpressRoute for Office 365](azure-expressroute.md) to familiarize yourself with the Office 365 services supported over Azure ExpressRoute.</span></span> <span data-ttu-id="884ae-119">Consultez l’article [ URLs and plages d’adresse IP Office 365](urls-and-ip-address-ranges.md) pour identifier les requêtes réseau des applications Office 365 qui nécessitent une connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="884ae-119">Also review the article [Office 365 URLs and IP address ranges](urls-and-ip-address-ranges.md) to understand which network requests for Office 365 applications require Internet connectivity.</span></span> <span data-ttu-id="884ae-120">Cette opération permet de mieux configurer vos périphériques de sécurité de périmètre.</span><span class="sxs-lookup"><span data-stu-id="884ae-120">This will help to better configure your perimeter security devices.</span></span>

<span data-ttu-id="884ae-121">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="884ae-121">For more information, see:</span></span>

- [<span data-ttu-id="884ae-122">Annonce du billet de blog dans le Forum de la communauté technique Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-122">Announcement blog post in the Office 365 Tech Community Forum</span></span>](https://techcommunity.microsoft.com/t5/Office-365-Blog/Announcing-Office-365-endpoint-categories-and-Office-365-IP/ba-p/177638)
- [<span data-ttu-id="884ae-123">Forum de la communauté technique Office 365 pour les questions sur l’utilisation des services web</span><span class="sxs-lookup"><span data-stu-id="884ae-123">Office 365 Tech Community Forum for questions about use of the web services</span></span>](https://techcommunity.microsoft.com/t5/Office-365-Networking/bd-p/Office365Networking)

## <a name="common-parameters"></a><span data-ttu-id="884ae-124">Paramètres communs</span><span class="sxs-lookup"><span data-stu-id="884ae-124">Common parameters</span></span>

<span data-ttu-id="884ae-125">Ces paramètres sont communs à toutes les méthodes de service web :</span><span class="sxs-lookup"><span data-stu-id="884ae-125">These parameters are common across all the web service methods:</span></span>

- <span data-ttu-id="884ae-126">**format = < JSON | CSV >** : par défaut, le format de données renvoyé est JSON.</span><span class="sxs-lookup"><span data-stu-id="884ae-126">**format=<JSON | CSV>** — By default, the returned data format is JSON.</span></span> <span data-ttu-id="884ae-127">Utilisez ce paramètre facultatif pour renvoyer les données au format de valeurs séparées par des virgules (CSV).</span><span class="sxs-lookup"><span data-stu-id="884ae-127">Use this optional parameter to return the data in comma-separated values (CSV) format.</span></span>
- <span data-ttu-id="884ae-128">**ClientRequestId =\<guid>**: un GUID requis que vous générez pour association client.</span><span class="sxs-lookup"><span data-stu-id="884ae-128">**ClientRequestId=\<guid>** — A required GUID that you generate for client association.</span></span> <span data-ttu-id="884ae-129">Générer un GUID unique pour chaque ordinateur appelant le service Web (les scripts inclus sur cette page génèrent un GUID pour vous).</span><span class="sxs-lookup"><span data-stu-id="884ae-129">Generate a unique GUID for each machine that calls the web service (the scripts included on this page generate a GUID for you).</span></span> <span data-ttu-id="884ae-130">N’utilisez pas les GUID illustrés dans les exemples suivants, car ils peuvent être bloqués par le service web à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="884ae-130">Do not use the GUIDs shown in the following examples because they might be blocked by the web service in the future.</span></span> <span data-ttu-id="884ae-131">Format GUID est _xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx_, où x représente un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="884ae-131">GUID format is _xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx_, where x represents a hexadecimal number.</span></span>

  <span data-ttu-id="884ae-132">Pour générer un GUID, vous pouvez utiliser la commande PowerShell [New-GUID](/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) ou utiliser un service en ligne tel que [générateur de GUID en ligne](https://www.guidgenerator.com/).</span><span class="sxs-lookup"><span data-stu-id="884ae-132">To generate a GUID, you can use the [New-Guid](/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) PowerShell command, or use an online service such as [Online GUID Generator](https://www.guidgenerator.com/).</span></span>

## <a name="version-web-method"></a><span data-ttu-id="884ae-133">Méthode web version </span><span class="sxs-lookup"><span data-stu-id="884ae-133">Version web method</span></span>

<span data-ttu-id="884ae-134">Microsoft met à jour les entrées d’adresse IP et de nom de domaine complet Office 365 à la fin de chaque mois.</span><span class="sxs-lookup"><span data-stu-id="884ae-134">Microsoft updates the Office 365 IP address and FQDN entries at the end of each month.</span></span> <span data-ttu-id="884ae-135">Les mises à jour hors bande sont parfois publiées en raison de problèmes de support, de mises à jour de sécurité ou d’autres exigences opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="884ae-135">Out-of-band updates are sometimes published due to support incidents, security updates or other operational requirements.</span></span>

<span data-ttu-id="884ae-136">Un numéro de version est attribué aux données pour chaque instance publiée et la méthode Web version vous permet de rechercher la dernière version de chaque instance du service Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-136">The data for each published instance is assigned a version number, and the version web method enables you to check for the latest version of each Office 365 service instance.</span></span> <span data-ttu-id="884ae-137">Nous vous recommandons de ne pas vérifier la version plus d’une fois par heure.</span><span class="sxs-lookup"><span data-stu-id="884ae-137">We recommend that you check the version not more than once an hour.</span></span>

<span data-ttu-id="884ae-138">Les paramètres pour la méthode web de version sont :</span><span class="sxs-lookup"><span data-stu-id="884ae-138">Parameters for the version web method are:</span></span>

- <span data-ttu-id="884ae-139">**AllVersions = < true | Faux >** : par défaut, la version renvoyée est la dernière version.</span><span class="sxs-lookup"><span data-stu-id="884ae-139">**AllVersions=<true | false>** — By default, the version returned is the latest.</span></span> <span data-ttu-id="884ae-140">Inclure ce paramètre facultatif pour demander toutes les versions publiées depuis que le service web a été publié.</span><span class="sxs-lookup"><span data-stu-id="884ae-140">Include this optional parameter to request all published versions since the web service was first released.</span></span>
- <span data-ttu-id="884ae-141">**Format = < JSON | CSV | RSS >** : outre les formats JSON et CSV, la méthode web version prend également en charge RSS.</span><span class="sxs-lookup"><span data-stu-id="884ae-141">**Format=<JSON | CSV | RSS>** — In addition to the JSON and CSV formats, the version web method also supports RSS.</span></span> <span data-ttu-id="884ae-142">Vous pouvez utiliser ce paramètre facultatif conjointement avec le paramètre _AllVersions = true_ pour demander un flux RSS qui peut être utilisé avec Outlook ou d’autres lecteurs de RSS.</span><span class="sxs-lookup"><span data-stu-id="884ae-142">You can use this optional parameter along with the _AllVersions=true_ parameter to request an RSS feed that can be used with Outlook or other RSS readers.</span></span>
- <span data-ttu-id="884ae-143">**Instance=<Worldwide | China | Germany | USGovDoD | USGovGCCHigh>** : ce paramètre facultatif spécifie l’instance vers laquelle renvoyer la version.</span><span class="sxs-lookup"><span data-stu-id="884ae-143">**Instance=<Worldwide | China | Germany | USGovDoD | USGovGCCHigh>** — This optional parameter specifies the instance to return the version for.</span></span> <span data-ttu-id="884ae-144">Si cet argument est omis, toutes les instances sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="884ae-144">If omitted, all instances are returned.</span></span> <span data-ttu-id="884ae-145">Les instances valides sont : Worldwide, China, Germany, USGovDoD, USGovGCCHigh.</span><span class="sxs-lookup"><span data-stu-id="884ae-145">Valid instances are: Worldwide, China, Germany, USGovDoD, USGovGCCHigh.</span></span>

<span data-ttu-id="884ae-146">La méthode Web version n’est pas limitée au taux et ne renvoie jamais de codes de réponse HTTP 429.</span><span class="sxs-lookup"><span data-stu-id="884ae-146">The version web method is not rate limited and does not ever return 429 HTTP Response Codes.</span></span> <span data-ttu-id="884ae-147">La réponse à la méthode Web version inclut un en-tête de contrôle du cache qui recommande la mise en cache des données pendant 1 heure.</span><span class="sxs-lookup"><span data-stu-id="884ae-147">The response to the version web method does include a cache-control header recommending caching of the data for 1 hour.</span></span> <span data-ttu-id="884ae-148">Le résultat de la méthode web de version peut être un enregistrement unique ou un tableau d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="884ae-148">The result from the version web method can be a single record or an array of records.</span></span> <span data-ttu-id="884ae-149">Les éléments de chaque enregistrement sont :</span><span class="sxs-lookup"><span data-stu-id="884ae-149">The elements of each record are:</span></span>

- <span data-ttu-id="884ae-150">instance : nom court de l’instance de service Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-150">instance — The short name of the Office 365 service instance.</span></span>
- <span data-ttu-id="884ae-151">dernière : dernière version pour les points de terminaison de l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="884ae-151">latest — The latest version for endpoints of the specified instance.</span></span>
- <span data-ttu-id="884ae-152">versions : liste de toutes les versions précédentes pour l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="884ae-152">versions — A list of all previous versions for the specified instance.</span></span> <span data-ttu-id="884ae-153">Cet élément est inclus uniquement si le paramètre _AllVersions_ est true.</span><span class="sxs-lookup"><span data-stu-id="884ae-153">This element is only included if the _AllVersions_ parameter is true.</span></span>

### <a name="examples"></a><span data-ttu-id="884ae-154">Exemples :</span><span class="sxs-lookup"><span data-stu-id="884ae-154">Examples:</span></span>

<span data-ttu-id="884ae-155">Exemple 1 d’URI de requête : [https://endpoints.office.com/version?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-155">Example 1 request URI: [https://endpoints.office.com/version?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p113">Cet URI renvoie la dernière version de chaque instance du service Office 365. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p113">This URI returns the latest version of each Office 365 service instance. Example result:</span></span>

```json
[
 {
  "instance": "Worldwide",
  "latest": "2018063000"
 },
 {
  "instance": "USGovDoD",
  "latest": "2018063000"
 },
 {
  "instance": "USGovGCCHigh",
  "latest": "2018063000"
 },
 {
  "instance": "China",
  "latest": "2018063000"
 },
 {
  "instance": "Germany",
  "latest": "2018063000"
 }
]
```

> [!IMPORTANT]
> <span data-ttu-id="884ae-p114">Le GUID pour le paramètre ClientRequestID dans ces URI n’est qu’un exemple. Pour essayer les URI de service web, générez votre propre GUID. Les GUID illustrés dans ces exemples pourront être bloqués par le service web à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="884ae-p114">The GUID for the ClientRequestID parameter in these URIs are only an example. To try the web service URIs out, generate your own GUID. The GUIDs shown in these examples may be blocked by the web service in the future.</span></span>

<span data-ttu-id="884ae-161">Exemple 2 d’URI de requête : [https://endpoints.office.com/version/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-161">Example 2 request URI: [https://endpoints.office.com/version/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p115">Cet URI renvoie la dernière version de chaque instance du service Office 365 spécifiée. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p115">This URI returns the latest version of the specified Office 365 service instance. Example result:</span></span>

```json
{
 "instance": "Worldwide",
 "latest": "2018063000"
}
```

<span data-ttu-id="884ae-164">Exemple 3 d’URI de requête : [https://endpoints.office.com/version/Worldwide?Format=CSV&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?Format=CSV&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-164">Example 3 request URI: [https://endpoints.office.com/version/Worldwide?Format=CSV&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?Format=CSV&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p116">Cet URI affiche le résultat au format CSV. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p116">This URI shows output in CSV format. Example result:</span></span>

```csv
instance,latest
Worldwide,2018063000
```

<span data-ttu-id="884ae-167">Exemple 4 d’URI de requête : [https://endpoints.office.com/version/Worldwide?AllVersions=true&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?AllVersions=true&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-167">Example 4 request URI: [https://endpoints.office.com/version/Worldwide?AllVersions=true&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/version/Worldwide?AllVersions=true&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p117">Cet URI affiche toutes les versions antérieures publiées pour l’instance du service Office 365 dans le monde. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p117">This URI shows all prior versions that have been published for the Office 365 worldwide service instance. Example result:</span></span>

```json
{
  "instance": "Worldwide",
  "latest": "2018063000",
  "versions": [
    "2018063000",
    "2018062000"
  ]
}
```

<span data-ttu-id="884ae-170">Exemple 5 d’URI de flux RSS : [https://endpoints.office.com/version/worldwide?clientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7&allVersions=true&format=RSS](https://endpoints.office.com/version/worldwide?clientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7&allVersions=true&format=RSS)</span><span class="sxs-lookup"><span data-stu-id="884ae-170">Example 5 RSS Feed URI: [https://endpoints.office.com/version/worldwide?clientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7&allVersions=true&format=RSS](https://endpoints.office.com/version/worldwide?clientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7&allVersions=true&format=RSS)</span></span>

<span data-ttu-id="884ae-p118">Cet URI affiche un flux RSS des versions publiées qui incluent des liens vers la liste des modifications apportées à chaque version. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p118">This URI shows an RSS feed of the published versions that include links to the list of changes for each version. Example result:</span></span>

```xml
<?xml version="1.0" encoding="ISO-8859-1"?>
<rss version="2.0" xmlns:a10="https://www.w3.org/2005/Atom">
<channel>
<link>https://aka.ms/o365ip</link>
<description/>
<language>en-us</language>
<lastBuildDate>Thu, 02 Aug 2018 00:00:00 Z</lastBuildDate>
<item>
<guid isPermaLink="false">2018080200</guid>
<link>https://endpoints.office.com/changes/Worldwide/2018080200?singleVersion&clientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7</link> <description>Version 2018080200 includes 2 changes. IPs: 2 added and 0 removed.</description>
<pubDate>Thu, 02 Aug 2018 00:00:00 Z</pubDate>
</item>
```

## <a name="endpoints-web-method"></a><span data-ttu-id="884ae-173">Points de terminaison méthode web</span><span class="sxs-lookup"><span data-stu-id="884ae-173">Endpoints web method</span></span>

<span data-ttu-id="884ae-174">Les points de terminaison de la méthode web renvoient tous les enregistrements pour les plages d’adresses IP et URL qui composent le service Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-174">The endpoints web method returns all records for IP address ranges and URLs that make up the Office 365 service.</span></span> <span data-ttu-id="884ae-175">Les données les plus récentes des points de terminaison de la méthode Web doivent toujours être utilisées pour la configuration des périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="884ae-175">The latest data from the endpoints web method should always be used for network device configuration.</span></span> <span data-ttu-id="884ae-176">Microsoft fournit une notification préalable 30 jours avant la publication de nouveaux ajouts afin de vous laisser le temps de mettre à jour les listes de contrôle d’accès et les listes de contournement du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="884ae-176">Microsoft provides advance notice 30 days prior to publishing new additions to give you time to update access control lists and proxy server bypass lists.</span></span> <span data-ttu-id="884ae-177">Nous vous recommandons de rappeler uniquement les points de terminaison méthode web uniquement lorsque la méthode web version indique qu’une nouvelle version des données est disponible.</span><span class="sxs-lookup"><span data-stu-id="884ae-177">We recommend that you only call the endpoints web method again when the version web method indicates that a new version of the data is available.</span></span>

<span data-ttu-id="884ae-178">Les paramètres pour les points de terminaison de la méthode web sont :</span><span class="sxs-lookup"><span data-stu-id="884ae-178">Parameters for the endpoints web method are:</span></span>

- <span data-ttu-id="884ae-179">**ServiceAreas=<Common | Exchange | SharePoint | Skype >** : une liste de zones de service séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="884ae-179">**ServiceAreas=<Common | Exchange | SharePoint | Skype>** — A comma-separated list of service areas.</span></span> <span data-ttu-id="884ae-180">Éléments valides sont _Common_, _Exchange_, _SharePoint_, et _Skype_.</span><span class="sxs-lookup"><span data-stu-id="884ae-180">Valid items are _Common_, _Exchange_, _SharePoint_, and _Skype_.</span></span> <span data-ttu-id="884ae-181">Étant donné que les éléments _Common_ de zone de service sont une condition préalable pour toutes les autres zones de service, le service web les inclura toujours.</span><span class="sxs-lookup"><span data-stu-id="884ae-181">Because _Common_ service area items are a prerequisite for all other service areas, the web service always includes them.</span></span> <span data-ttu-id="884ae-182">Si vous n’incluez pas ce paramètre, toutes les zones de service sont renvoyées.</span><span class="sxs-lookup"><span data-stu-id="884ae-182">If you do not include this parameter, all service areas are returned.</span></span>
- <span data-ttu-id="884ae-183">**TenantName=<tenant_name>** : nom de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-183">**TenantName=<tenant_name>** — Your Office 365 tenant name.</span></span> <span data-ttu-id="884ae-184">Le service web prend votre nom fourni et l’insère en plusieurs parties d’URL qui incluent le nom de client.</span><span class="sxs-lookup"><span data-stu-id="884ae-184">The web service takes your provided name and inserts it in parts of URLs that include the tenant name.</span></span> <span data-ttu-id="884ae-185">Si vous ne fournissez pas de nom de client, ces composants d’URL ont le caractère générique (\*).</span><span class="sxs-lookup"><span data-stu-id="884ae-185">If you don't provide a tenant name, those parts of URLs have the wildcard character (\*).</span></span>
- <span data-ttu-id="884ae-186">**NoIPv6=<true | false>**  : définissez cette option sur _true_ pour exclure les adresses IPv6 du résultat, par exemple, si vous n’utilisez pas IPv6 dans votre réseau.</span><span class="sxs-lookup"><span data-stu-id="884ae-186">**NoIPv6=<true | false>** — Set the value to _true_ to exclude IPv6 addresses from the output if you don't use IPv6 in your network.</span></span>
- <span data-ttu-id="884ae-187">**Instance=<Worldwide | China | Germany | USGovDoD | USGovGCCHigh>** : ce paramètre facultatif spécifie l’instance vers laquelle renvoyer les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-187">**Instance=<Worldwide | China | Germany | USGovDoD | USGovGCCHigh>** — This required parameter specifies the instance from which to return the endpoints.</span></span> <span data-ttu-id="884ae-188">Les instances valides sont : _Worldwide_, _China_, _Germany_, _USGovDoD_, and _USGovGCCHigh_.</span><span class="sxs-lookup"><span data-stu-id="884ae-188">Valid instances are: _Worldwide_, _China_, _Germany_, _USGovDoD_, and _USGovGCCHigh_.</span></span>

<span data-ttu-id="884ae-189">Si vous appelez la méthode web points de terminaison un trop grand nombre de fois à partir de la même adresse IP du client, vous pouvez recevoir le code de réponse HTTP _429 (Trop de requêtes)_.</span><span class="sxs-lookup"><span data-stu-id="884ae-189">If you call the endpoints web method too many times from the same client IP address, you might receive HTTP response code _429 (Too Many Requests)_.</span></span> <span data-ttu-id="884ae-190">Si vous recevez ce code de réponse, patientez 1 heure avant de renouveler votre demande, ou générez un nouveau GUID pour la demande.</span><span class="sxs-lookup"><span data-stu-id="884ae-190">If you get this response code, wait 1 hour before repeating your request, or generate a new GUID for the request.</span></span> <span data-ttu-id="884ae-191">Nous recommandons de ne rappeler la méthode web points de terminaison uniquement lorsque la méthode web indique qu’une nouvelle version est disponible.</span><span class="sxs-lookup"><span data-stu-id="884ae-191">As a general best practice, only call the endpoints web method when the version web method indicates that a new version is available.</span></span>

<span data-ttu-id="884ae-192">Le résultat de la méthode web de points de terminaison est un tableau d’enregistrements avec chaque enregistrement représentant un ensemble de points de terminaison spécifique.</span><span class="sxs-lookup"><span data-stu-id="884ae-192">The result from the endpoints web method is an array of records in which each record represents a specific endpoint set.</span></span> <span data-ttu-id="884ae-193">Les éléments pour chaque enregistrement sont :</span><span class="sxs-lookup"><span data-stu-id="884ae-193">The elements for each record are:</span></span>

- <span data-ttu-id="884ae-194">id : l’ID non modifiable de l’ensemble de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-194">id — The immutable id number of the endpoint set.</span></span>
- <span data-ttu-id="884ae-195">serviceArea : la zone de service dont il fait partie : _Common_, _Exchange_, _SharePoint_, ou _Skype_.</span><span class="sxs-lookup"><span data-stu-id="884ae-195">serviceArea — The service area that this is part of: _Common_, _Exchange_, _SharePoint_, or _Skype_.</span></span>
- <span data-ttu-id="884ae-196">URL : URL pour l’entité de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-196">urls — URLs for the endpoint set.</span></span> <span data-ttu-id="884ae-197">Tableau JSON d’enregistrements DNS.</span><span class="sxs-lookup"><span data-stu-id="884ae-197">A JSON array of DNS records.</span></span> <span data-ttu-id="884ae-198">Omis si vide.</span><span class="sxs-lookup"><span data-stu-id="884ae-198">Omitted if blank.</span></span>
- <span data-ttu-id="884ae-199">tcpPorts — ports TCP pour l’entité de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-199">tcpPorts — TCP ports for the endpoint set.</span></span> <span data-ttu-id="884ae-200">Tous les éléments port sont mis en forme en tant que liste de ports séparés par des virgules ou plages de ports séparés par un tiret (-).</span><span class="sxs-lookup"><span data-stu-id="884ae-200">All ports elements are formatted as a comma-separated list of ports or port ranges separated by a dash character (-).</span></span> <span data-ttu-id="884ae-201">Les ports s’appliquent à toutes les adresses IP et toutes les URL du point de terminaison défini pour une catégorie donnée.</span><span class="sxs-lookup"><span data-stu-id="884ae-201">Ports apply to all IP addresses and all URLs in the endpoint set for a given category.</span></span> <span data-ttu-id="884ae-202">Omis si vide.</span><span class="sxs-lookup"><span data-stu-id="884ae-202">Omitted if blank.</span></span>
- <span data-ttu-id="884ae-203">udpPorts : ports UDP pour les plages d’adresses IP dans cet ensemble de points de terminaison. </span><span class="sxs-lookup"><span data-stu-id="884ae-203">udpPorts — UDP ports for the IP address ranges in this endpoint set.</span></span> <span data-ttu-id="884ae-204">Omis si vide.</span><span class="sxs-lookup"><span data-stu-id="884ae-204">Omitted if blank.</span></span>
- <span data-ttu-id="884ae-205">ips : plages d’adresses IP associées à cet ensemble de points de terminaison tel qu’associées aux ports TCP ou UDP répertoriés.</span><span class="sxs-lookup"><span data-stu-id="884ae-205">ips — The IP address ranges associated with this endpoint set as associated with the listed TCP or UDP ports.</span></span> <span data-ttu-id="884ae-206">Un tableau JSON des plages d’adresses IP. </span><span class="sxs-lookup"><span data-stu-id="884ae-206">A JSON array of IP address ranges.</span></span> <span data-ttu-id="884ae-207">Omis si vide.</span><span class="sxs-lookup"><span data-stu-id="884ae-207">Omitted if blank.</span></span>
- <span data-ttu-id="884ae-208">Catégorie : catégorie de connectivité pour l’entité de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-208">category — The connectivity category for the endpoint set.</span></span> <span data-ttu-id="884ae-209">Les valeurs valides sont : _Optimiser_, _Autoriser_, and _Défaut_.</span><span class="sxs-lookup"><span data-stu-id="884ae-209">Valid values are _Optimize_, _Allow_, and _Default_.</span></span> <span data-ttu-id="884ae-210">Si vous recherchez la sortie de la méthode Web de points de terminaison pour la catégorie d’une adresse IP ou d’une URL spécifique, il est possible que votre requête renvoie plusieurs catégories.</span><span class="sxs-lookup"><span data-stu-id="884ae-210">If you search the endpoints web method output for the category of a specific IP address or URL, it is possible that your query will return multiple categories.</span></span> <span data-ttu-id="884ae-211">Dans ce cas, suivez la recommandation pour la catégorie de priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="884ae-211">In such a case, follow the recommendation for the highest priority category.</span></span> <span data-ttu-id="884ae-212">Par exemple, si le point de terminaison apparaît dans les deux options _optimiser_ et _autoriser_, vous devez respecter les conditions requises pour _optimiser_.</span><span class="sxs-lookup"><span data-stu-id="884ae-212">For example, if the endpoint appears in both _Optimize_ and _Allow_, you should follow the requirements for _Optimize_.</span></span> <span data-ttu-id="884ae-213">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="884ae-213">Required.</span></span>
- <span data-ttu-id="884ae-214">expressRoute : _True_ si cet ensemble de points de terminaison est routé sur ExpressRoute, _False_ si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="884ae-214">expressRoute — _True_ if this endpoint set is routed over ExpressRoute, _False_ if not.</span></span>
- <span data-ttu-id="884ae-215">required : _True_ si cet ensemble de points de terminaison est obligatoire pour disposer d’une connectivité et prendre en charge Office 365. </span><span class="sxs-lookup"><span data-stu-id="884ae-215">required — _True_ if this endpoint set is required to have connectivity for Office 365 to be supported.</span></span> <span data-ttu-id="884ae-216">_False_ si cet ensemble de points de terminaison est facultatif.</span><span class="sxs-lookup"><span data-stu-id="884ae-216">_False_ if this endpoint set is optional.</span></span>
- <span data-ttu-id="884ae-217">notes : pour les points de terminaison facultatifs, ce texte décrit les fonctionnalités Office 365 qui seront indisponibles si les adresses IP ou les URL dans cet ensemble de points de terminaison ne sont pas accessibles sur la couche réseau.</span><span class="sxs-lookup"><span data-stu-id="884ae-217">notes — For optional endpoints, this text describes Office 365 functionality that would be unavailable if IP addresses or URLs in this endpoint set cannot be accessed at the network layer.</span></span> <span data-ttu-id="884ae-218">Omis si vide.</span><span class="sxs-lookup"><span data-stu-id="884ae-218">Omitted if blank.</span></span>

### <a name="examples"></a><span data-ttu-id="884ae-219">Exemples :</span><span class="sxs-lookup"><span data-stu-id="884ae-219">Examples:</span></span>

<span data-ttu-id="884ae-220">Exemple 1 d’URI de requête : [https://endpoints.office.com/endpoints/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/endpoints/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-220">Example 1 request URI: [https://endpoints.office.com/endpoints/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/endpoints/Worldwide?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-221">Cet URL a obtenu tous les points de terminaison pour l’instance Worldwide d’Office 365 pour toutes les charges de travail. </span><span class="sxs-lookup"><span data-stu-id="884ae-221">This URI obtains all endpoints for the Office 365 worldwide instance for all workloads.</span></span> <span data-ttu-id="884ae-222">Exemple de résultat montrant un extrait du résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-222">Example result that shows an excerpt of the output:</span></span>

```json
[
 {
  "id": 1,
  "serviceArea": "Exchange",
  "serviceAreaDisplayName": "Exchange Online",
  "urls":
   [
    "*.protection.outlook.com"
   ],
  "ips":
   [
    "2a01:111:f403::/48", "23.103.132.0/22", "23.103.136.0/21", "23.103.198.0/23", "23.103.212.0/22", "40.92.0.0/14", "40.107.0.0/17", "40.107.128.0/18", "52.100.0.0/14", "213.199.154.0/24", "213.199.180.128/26", "94.245.120.64/26", "207.46.163.0/24", "65.55.88.0/24", "216.32.180.0/23", "23.103.144.0/20", "65.55.169.0/24", "207.46.100.0/24", "2a01:111:f400:7c00::/54", "157.56.110.0/23", "23.103.200.0/22", "104.47.0.0/17", "2a01:111:f400:fc00::/54", "157.55.234.0/24", "157.56.112.0/24", "52.238.78.88/32"
   ],
  "tcpPorts": "443",
  "expressRoute": true,
  "category": "Allow"
 },
 {
  "id": 2,
  "serviceArea": "Exchange",
  "serviceAreaDisplayName": "Exchange Online",
  "urls":
   [
    "*.mail.protection.outlook.com"
   ],
```

<span data-ttu-id="884ae-223">Notez que le résultat complet de la requête dans cet exemple contient d’autres jeux de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-223">Note that the full output of the request in this example would contain other endpoint sets.</span></span>

<span data-ttu-id="884ae-224">Exemple 2 d’URI de requête : [https://endpoints.office.com/endpoints/Worldwide?ServiceAreas=Exchange&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/endpoints/Worldwide?ServiceAreas=Exchange&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-224">Example 2 request URI: [https://endpoints.office.com/endpoints/Worldwide?ServiceAreas=Exchange&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/endpoints/Worldwide?ServiceAreas=Exchange&amp;ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-225">Cet exemple obtient des points de terminaison pour l’instance Worldwide d’Office 365 pour Exchange Online et les dépendances uniquement.</span><span class="sxs-lookup"><span data-stu-id="884ae-225">This example obtains endpoints for the Office 365 Worldwide instance for Exchange Online and dependencies only.</span></span>

<span data-ttu-id="884ae-226">Le résultat pour l’exemple 2 ressemble à l’exemple 1 sauf que les résultats n’incluent pas les points de terminaison pour SharePoint Online ou Skype Entreprise Online.</span><span class="sxs-lookup"><span data-stu-id="884ae-226">The output for example 2 is similar to example 1 except that the results would not include endpoints for SharePoint Online or Skype for Business Online.</span></span>

## <a name="changes-web-method"></a><span data-ttu-id="884ae-227">Méthode web de modifications</span><span class="sxs-lookup"><span data-stu-id="884ae-227">Changes web method</span></span>

<span data-ttu-id="884ae-228">La méthode Web modifications renvoie les mises à jour les plus récentes qui ont été publiées, généralement les modifications apportées au mois précédent en plages d’adresses IP et URL.</span><span class="sxs-lookup"><span data-stu-id="884ae-228">The changes web method returns the most recent updates that have been published, typically the previous month's changes to IP address ranges and URLs.</span></span>

<span data-ttu-id="884ae-229">Les modifications les plus critiques apportées aux données de points de terminaison sont les nouvelles URL et les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="884ae-229">The most critical changes to endpoints data are new URLs and IP addresses.</span></span> <span data-ttu-id="884ae-230">L’échec de l’ajout d’une adresse IP à une liste de contrôle d’accès de pare-feu ou d’une URL à une liste de contournement de serveur proxy peut provoquer une panne pour les utilisateurs d’Office 365 derrière ce périphérique réseau.</span><span class="sxs-lookup"><span data-stu-id="884ae-230">Failure to add an IP address to a firewall access control list or a URL to a proxy server bypass list can cause an outage for Office 365 users behind that network device.</span></span> <span data-ttu-id="884ae-231">Nonobstant les impératifs opérationnels, les nouveaux points de terminaison sont publiés sur le service Web 30 jours avant la date à laquelle les points de terminaison sont configurés pour vous laisser le temps de mettre à jour les listes de contrôle d’accès et les listes de contournement du serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="884ae-231">Notwithstanding operational requirements, new endpoints are published to the web service 30 days in advance of the date the endpoints are provisioned for use to give you time to update access control lists and proxy server bypass lists.</span></span>

<span data-ttu-id="884ae-232">Le paramètre requis pour la méthode web changes est le suivant :</span><span class="sxs-lookup"><span data-stu-id="884ae-232">The required parameter for the changes web method is:</span></span>

- <span data-ttu-id="884ae-233">**Version =\<YYYYMMDDNN>** : paramètre d’itinéraire URL requis.</span><span class="sxs-lookup"><span data-stu-id="884ae-233">**Version=\<YYYYMMDDNN>** — Required URL route parameter.</span></span> <span data-ttu-id="884ae-234">Cette valeur est la version que vous avez implémentée actuellement.</span><span class="sxs-lookup"><span data-stu-id="884ae-234">This value is the version that you have currently implemented.</span></span> <span data-ttu-id="884ae-235">Le service web renvoie les modifications depuis cette version.</span><span class="sxs-lookup"><span data-stu-id="884ae-235">The web service will return the changes since that version.</span></span> <span data-ttu-id="884ae-236">Le format est _JJNN/MM/AAAA_, où _NN_ est un nombre entier incrémenté si plusieurs versions doivent être publiées un même jour,  _00_ représentant la première mise à jour à la date concernée.</span><span class="sxs-lookup"><span data-stu-id="884ae-236">The format is _YYYYMMDDNN_, where _NN_ is a natural number incremented if there are multiple versions required to be published on a single day, with _00_ representing the first update for a given day.</span></span> <span data-ttu-id="884ae-237">Le service web exige que le paramètre _version_ contienne exactement 10 chiffres.</span><span class="sxs-lookup"><span data-stu-id="884ae-237">The web service requires the _version_ parameter to contain exactly 10 digits.</span></span>

<span data-ttu-id="884ae-238">La méthode web changes est limitée par le débit de la même manière que la méthode web endpoints.</span><span class="sxs-lookup"><span data-stu-id="884ae-238">The changes web method is rate limited in the same way as the endpoints web method.</span></span> <span data-ttu-id="884ae-239">Si vous recevez ce code de réponse 429, patientez 1 heure avant de renouveler votre demande, ou générez un nouveau GUID pour la demande.</span><span class="sxs-lookup"><span data-stu-id="884ae-239">If you receive a 429 HTTP response code, wait 1 hour before repeating your request or generate a new GUID for the request.</span></span>

<span data-ttu-id="884ae-240">Le résultat de la méthode web modifications est un tableau d’enregistrements avec chaque enregistrement représentant une modification d’une version de points de terminaison spécifique.</span><span class="sxs-lookup"><span data-stu-id="884ae-240">The result from the changes web method is an array of records in which each record represents a change in a specific version of the endpoints.</span></span> <span data-ttu-id="884ae-241">Les éléments pour chaque enregistrement sont :</span><span class="sxs-lookup"><span data-stu-id="884ae-241">The elements for each record are:</span></span>

- <span data-ttu-id="884ae-242">ID : ID non modifiable de l’enregistrement de la modification.</span><span class="sxs-lookup"><span data-stu-id="884ae-242">id — The immutable id of the change record.</span></span>
- <span data-ttu-id="884ae-243">endpointSetId : ID de l’enregistrement du point de terminaison qui est modifié.</span><span class="sxs-lookup"><span data-stu-id="884ae-243">endpointSetId — The ID of the endpoint set record that is changed.</span></span>
- <span data-ttu-id="884ae-244">disposition : décrit les modifications apportées à l’enregistrement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-244">disposition — Describes what the change did to the endpoint set record.</span></span> <span data-ttu-id="884ae-245">Les valeurs sont _modifier_, _ajouter_, or _supprimer_.</span><span class="sxs-lookup"><span data-stu-id="884ae-245">Values are _change_, _add_, or _remove_.</span></span>
- <span data-ttu-id="884ae-246">impact : toutes les modifications ne sont pas aussi importantes pour tous les environnements.</span><span class="sxs-lookup"><span data-stu-id="884ae-246">impact — Not all changes will be equally important to every environment.</span></span> <span data-ttu-id="884ae-247">Cet élément décrit l’impact attendu sur l’environnement du périmètre d’un réseau d’entreprise en raison de cette modification.</span><span class="sxs-lookup"><span data-stu-id="884ae-247">This element describes the expected impact to an enterprise network perimeter environment as a result of this change.</span></span> <span data-ttu-id="884ae-248">Cet élément est inclus uniquement dans les enregistrements de modification de la version **2018112800** et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="884ae-248">This element is included only in change records of version **2018112800** and later.</span></span> <span data-ttu-id="884ae-249">Les options d’impact sont les suivantes : — AddedIp – une adresse IP a été ajoutée à Office 365 et sera bientôt disponible sur le service.</span><span class="sxs-lookup"><span data-stu-id="884ae-249">Options for the impact are: — AddedIp – An IP address was added to Office 365 and will be live on the service soon.</span></span> <span data-ttu-id="884ae-250">Il s’agit d’un changement que vous devez apporter à un pare-feu ou à un autre périphérique de périmètre réseau couche 3.</span><span class="sxs-lookup"><span data-stu-id="884ae-250">This represents a change you need to take on a firewall or other layer 3 network perimeter device.</span></span> <span data-ttu-id="884ae-251">Si vous ne l’ajoutez pas avant que nous commencions à l’utiliser, vous pourriez subir une panne.</span><span class="sxs-lookup"><span data-stu-id="884ae-251">If you don’t add this before we start using it, you may experience an outage.</span></span>
  <span data-ttu-id="884ae-252">– AddedUrl – Une URL a été ajoutée à Office 365 et sera bientôt disponible sur le service.</span><span class="sxs-lookup"><span data-stu-id="884ae-252">— AddedUrl – A URL was added to Office 365 and will be live on the service soon.</span></span> <span data-ttu-id="884ae-253">Il s’agit d’un changement que vous devez apporter à un serveur proxy ou à un périphérique réseau d’analyse d’URL.</span><span class="sxs-lookup"><span data-stu-id="884ae-253">This represents a change you need to take on a proxy server or URL parsing network perimeter device.</span></span> <span data-ttu-id="884ae-254">Si vous ne l’ajoutez pas avant que nous commencions à l’utiliser, vous pourriez subir une panne.</span><span class="sxs-lookup"><span data-stu-id="884ae-254">If you don’t add this URL before we start using it, you may experience an outage.</span></span>
  <span data-ttu-id="884ae-255">— AddedIpAndUrl — une adresse IP et une URL ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="884ae-255">— AddedIpAndUrl — Both an IP address and a URL were added.</span></span> <span data-ttu-id="884ae-256">Il s’agit d’un changement que vous devez apporter à un périphérique de périmètre réseau couche 3, un serveur proxy ou à un périphérique réseau d’analyse d’URL.</span><span class="sxs-lookup"><span data-stu-id="884ae-256">This represents a change you need to take on either a firewall layer 3 device or a proxy server or URL parsing device.</span></span> <span data-ttu-id="884ae-257">Si vous ne l’ajoutez pas avant que nous commencions à l’utiliser, vous pourriez subir une panne.</span><span class="sxs-lookup"><span data-stu-id="884ae-257">If you don’t add this IP/URL pair before we start using it, you may experience an outage.</span></span>
  <span data-ttu-id="884ae-258">— RemovedIpOrUrl – au moins une adresse IP ou une URL a été supprimée d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="884ae-258">— RemovedIpOrUrl – At least one IP address or URL was removed from Office 365.</span></span> <span data-ttu-id="884ae-259">Supprimez les points de terminaison réseau de vos périphériques de périmètre, mais il n’y a aucune échéance pour le faire.</span><span class="sxs-lookup"><span data-stu-id="884ae-259">Remove the network endpoints from your perimeter devices, but there’s no deadline for you to do this.</span></span>
  <span data-ttu-id="884ae-260">— ChangedIsExpressRoute – l’attribut support ExpressRoute a été modifié.</span><span class="sxs-lookup"><span data-stu-id="884ae-260">— ChangedIsExpressRoute – The ExpressRoute support attribute was changed.</span></span> <span data-ttu-id="884ae-261">Si vous utilisez ExpressRoute, vous devrez peut-être agir en fonction de votre configuration.</span><span class="sxs-lookup"><span data-stu-id="884ae-261">If you use ExpressRoute, you might need to take action depending on your configuration.</span></span>
  <span data-ttu-id="884ae-262">—MovedIpOrUrl — nous avons déplacé une adresse IP ou une URL entre cet ensemble de points de terminaison et un autre emplacement. </span><span class="sxs-lookup"><span data-stu-id="884ae-262">— MovedIpOrUrl – We moved an IP address or Url between this endpoint set and another one.</span></span> <span data-ttu-id="884ae-263">En général, aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="884ae-263">Generally no action is required.</span></span>
  <span data-ttu-id="884ae-264">— RemovedDuplicateIpOrUrl – nous avons supprimé une adresse IP ou une URL en double, mais celle-ci est toujours publiée pour Office 365. </span><span class="sxs-lookup"><span data-stu-id="884ae-264">— RemovedDuplicateIpOrUrl – We removed a duplicate IP address or Url but it’s still published for Office 365.</span></span> <span data-ttu-id="884ae-265">En général, aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="884ae-265">Generally no action is required.</span></span>
  <span data-ttu-id="884ae-266">— OtherNonPriorityChanges – nous avons modifié un élément moins critique que toutes les autres options, comme un champ de note.</span><span class="sxs-lookup"><span data-stu-id="884ae-266">— OtherNonPriorityChanges – We changed something less critical than all of the other options, such as the contents of a note field.</span></span>
- <span data-ttu-id="884ae-267">version : version de l’entité de point de terminaison publiée dans laquelle la modification a été introduite.</span><span class="sxs-lookup"><span data-stu-id="884ae-267">version — The version of the published endpoint set in which the change was introduced.</span></span> <span data-ttu-id="884ae-268">Le format des numéros de version est _JJNN/MM/AAAA_, où _NN_ est un nombre entier incrémenté si plusieurs versions doivent être publiées un même jour.</span><span class="sxs-lookup"><span data-stu-id="884ae-268">Version numbers are of the format _YYYYMMDDNN_, where _NN_ is a natural number incremented if there are multiple versions required to be published on a single day.</span></span>
- <span data-ttu-id="884ae-269">previous : sous-structure détaillant les valeurs précédentes des éléments modifiés sur le point de terminaison défini.</span><span class="sxs-lookup"><span data-stu-id="884ae-269">previous — A substructure detailing previous values of changed elements on the endpoint set.</span></span> <span data-ttu-id="884ae-270">Elle ne sera pas incluse pour les nouveaux ensembles de points de terminaison ajoutés.</span><span class="sxs-lookup"><span data-stu-id="884ae-270">This will not be included for newly added endpoint sets.</span></span> <span data-ttu-id="884ae-271">Inclut _ExpressRoute_, _serviceArea_, _category_, _required_, _tcpPorts_, _udpPorts_ et _notes_.</span><span class="sxs-lookup"><span data-stu-id="884ae-271">Includes  _ExpressRoute_, _serviceArea_, _category_, _required_, _tcpPorts_, _udpPorts_, and _notes_.</span></span>
- <span data-ttu-id="884ae-272">current : une sous-structure détaillant les valeurs mises à jour des éléments de modifications dans l’ensemble des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-272">current — A substructure detailing updated values of changes elements on the endpoint set.</span></span> <span data-ttu-id="884ae-273">Inclut _ExpressRoute_, _serviceArea_, _category_, _required_, _tcpPorts_, _udpPorts_ et _notes_.</span><span class="sxs-lookup"><span data-stu-id="884ae-273">Includes _ExpressRoute_, _serviceArea_, _category_, _required_, _tcpPorts_, _udpPorts_, and _notes_.</span></span>
- <span data-ttu-id="884ae-274">add : sous-structure détaillant les éléments à ajouter aux collections d’ensembles de points de terminaison. </span><span class="sxs-lookup"><span data-stu-id="884ae-274">add — A substructure detailing items to be added to endpoint set collections.</span></span> <span data-ttu-id="884ae-275">Omis s’il n’y a aucun ajout.</span><span class="sxs-lookup"><span data-stu-id="884ae-275">Omitted if there are no additions.</span></span>
  <span data-ttu-id="884ae-276">— effectiveDate — définit les données lorsque les ajouts seront disponibles dans le service.</span><span class="sxs-lookup"><span data-stu-id="884ae-276">— effectiveDate — Defines the data when the additions will be live in the service.</span></span>
  <span data-ttu-id="884ae-277">— ips — éléments à ajouter au tableau d’adresses _ips_.</span><span class="sxs-lookup"><span data-stu-id="884ae-277">— ips — Items to be added to the _ips_ array.</span></span>
  <span data-ttu-id="884ae-278">— urls — éléments à ajouter au tableau _urls_.</span><span class="sxs-lookup"><span data-stu-id="884ae-278">— urls- Items to be added to the _urls_ array.</span></span>
- <span data-ttu-id="884ae-279">remove : sous-structure détaillant les éléments à supprimer de l’ensemble de points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="884ae-279">remove — A substructure detailing items to be removed from the endpoint set.</span></span> <span data-ttu-id="884ae-280">Omis si aucune suppression.</span><span class="sxs-lookup"><span data-stu-id="884ae-280">Omitted if there are no removals.</span></span>
  <span data-ttu-id="884ae-281">— ips — éléments à supprimer du tableau d’adresses _ips_.</span><span class="sxs-lookup"><span data-stu-id="884ae-281">— ips — Items to be removed from the _ips_ array.</span></span>
  <span data-ttu-id="884ae-282">— urls — éléments à supprimer du tableau _urls_.</span><span class="sxs-lookup"><span data-stu-id="884ae-282">— urls- Items to be removed from the _urls_ array.</span></span>

### <a name="examples"></a><span data-ttu-id="884ae-283">Exemples :</span><span class="sxs-lookup"><span data-stu-id="884ae-283">Examples:</span></span>

<span data-ttu-id="884ae-284">Exemple 1 d’URI de requête : [https://endpoints.office.com/changes/worldwide/0000000000?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/changes/worldwide/0000000000?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-284">Example 1 request URI: [https://endpoints.office.com/changes/worldwide/0000000000?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/changes/worldwide/0000000000?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p144">Toutes les modifications précédentes apportées à l’instance de service Worldwide d’Office 365 sont demandées. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p144">This requests all previous changes to the Office 365 worldwide service instance. Example result:</span></span>

```json
[
 {
  "id": 424,
  "endpointSetId": 32,
  "disposition": "Change",
  "version": "2018062700",
  "remove":
   {
    "urls":
     [
      "*.api.skype.com", "skypegraph.skype.com"
     ]
   }
 },
 {
  "id": 426,
  "endpointSetId": 31,
  "disposition": "Change",
  "version": "2018062700",
  "add":
   {
    "effectiveDate": "20180609",
    "ips":
     [
      "51.140.203.190/32"
     ]
   },
  "remove":
   {
    "ips":
     [
```

<span data-ttu-id="884ae-287">Exemple 2 d’URI de requête : [https://endpoints.office.com/changes/worldwide/2018062700?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/changes/worldwide/2018062700?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span><span class="sxs-lookup"><span data-stu-id="884ae-287">Example 2 request URI: [https://endpoints.office.com/changes/worldwide/2018062700?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7](https://endpoints.office.com/changes/worldwide/2018062700?ClientRequestId=b10c5ed1-bad1-445f-b386-b919946339a7)</span></span>

<span data-ttu-id="884ae-p145">Les modifications apportées à l’instance Worldwide d’Office 365 depuis la version spécifiée sont demandées. Dans ce cas, la version spécifiée est la dernière. Exemple de résultat :</span><span class="sxs-lookup"><span data-stu-id="884ae-p145">This requests changes since the specified version to the Office 365 Worldwide instance. In this case, the version specified is the latest. Example result:</span></span>

```json
[
  {
    "id":3,
    "endpointSetId":33,
    "changeDescription":"Removing old IP prefixes",
    "disposition":"Change",
    "version":"2018031301",
    "remove":{
      "ips":["65.55.127.0/24","66.119.157.192/26","66.119.158.0/25",
      "111.221.76.128/25","111.221.77.0/26","207.46.5.0/24"]
    }
  },
  {
    "id":4,
    "endpointSetId":45,
    "changeDescription":"Removing old IP prefixes",
    "disposition":"Change",
    "version":"2018031301",
    "remove":{
      "ips":["13.78.93.8/32","40.113.87.220/32","40.114.149.220/32",
      "40.117.100.83/32","40.118.214.164/32","104.208.31.113/32"]
    }
  }
]
```

## <a name="example-powershell-script"></a><span data-ttu-id="884ae-291">Exemple de Script PowerShell</span><span class="sxs-lookup"><span data-stu-id="884ae-291">Example PowerShell Script</span></span>

<span data-ttu-id="884ae-292">Vous pouvez exécuter un script PowerShell pour voir s’il y a des actions à suivre pour les données mises à jour.</span><span class="sxs-lookup"><span data-stu-id="884ae-292">You can run this PowerShell script to see if there are actions you need to take for updated data.</span></span> <span data-ttu-id="884ae-293">Vous pouvez exécuter ce script sous la forme d’une tâche planifiée pour rechercher une mise à jour de la version.</span><span class="sxs-lookup"><span data-stu-id="884ae-293">You can run this script as a scheduled task to check for a version update.</span></span> <span data-ttu-id="884ae-294">Pour éviter une charge excessive sur le service Web, essayez de ne pas exécuter le script plus d’une fois par heure.</span><span class="sxs-lookup"><span data-stu-id="884ae-294">To avoid excessive load on the web service, try not to run the script more than once an hour.</span></span>

<span data-ttu-id="884ae-295">Ce script effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="884ae-295">The script does the following:</span></span>

- <span data-ttu-id="884ae-296">Vérifie le numéro de version des points de terminaison d’instance dans le monde Office 365 en appelant l’API REST du service Web.</span><span class="sxs-lookup"><span data-stu-id="884ae-296">Checks the version number of the current Office 365 Worldwide instance endpoints by calling the web service REST API.</span></span>
- <span data-ttu-id="884ae-297">Recherche un fichier de version actuelle sur _$Env:TEMP\O365_endpoints_latestversion.txt_.</span><span class="sxs-lookup"><span data-stu-id="884ae-297">Checks for a current version file at _$Env:TEMP\O365_endpoints_latestversion.txt_.</span></span> <span data-ttu-id="884ae-298">Le chemin d’accès de la variable globale **$Env:TEMP** est généralement _C:\Users\\<username\>\AppData\Local\Temp_.</span><span class="sxs-lookup"><span data-stu-id="884ae-298">The path of the global variable **$Env:TEMP** is usually _C:\Users\\<username\>\AppData\Local\Temp_.</span></span>
- <span data-ttu-id="884ae-299">S’il s’agit de la première fois que le script est exécuté, le script renvoie la version actuelle et toutes les adresses IP et URL actuelles, écrit la version des points de terminaison dans le fichier _$Env:TEMP\O365_endpoints_latestversion.txt_ et les points de terminaison la sortie des données vers le fichier _$Env:TEMP\O365_endpoints_data.txt_.</span><span class="sxs-lookup"><span data-stu-id="884ae-299">If this is the first time the script has been run, the script returns the current version and all current IP addresses and URLs, writes the endpoints version to the file _$Env:TEMP\O365_endpoints_latestversion.txt_ and the endpoints data output to the file _$Env:TEMP\O365_endpoints_data.txt_.</span></span> <span data-ttu-id="884ae-300">Vous pouvez modifier le chemin d’accès et/ou le nom du fichier de sortie en modifiant les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="884ae-300">You can modify the path and/or name of the output file by editing these lines:</span></span>

    ``` powershell
    $versionpath = $Env:TEMP + "\O365_endpoints_latestversion.txt"
    $datapath = $Env:TEMP + "\O365_endpoints_data.txt"
    ```

- <span data-ttu-id="884ae-301">À chaque exécution suivante du script, si la version de service Web la plus récente est identique à la version figurant dans le fichier _O365_endpoints_latestversion.txt_, le script se ferme sans apporter de modifications.</span><span class="sxs-lookup"><span data-stu-id="884ae-301">On each subsequent execution of the script, if the latest web service version is identical to the version in the _O365_endpoints_latestversion.txt_ file, the script exits without making any changes.</span></span>
- <span data-ttu-id="884ae-302">Lorsque la dernière version du service Web est plus récente que la version du fichier _O365_endpoints_latestversion.txt_, le script renvoie les points de terminaison et les filtres pour les points de terminaison catégories **autoriser** et **optimiser**, met à jour la version figurant dans le fichier _O365_endpoints_latestversion.txt_ et écrit les données mises à jour dans le fichier _O365_endpoints_data.txt_. </span><span class="sxs-lookup"><span data-stu-id="884ae-302">When the latest web service version is newer than the version in the _O365_endpoints_latestversion.txt_ file, the script returns the endpoints and filters for the **Allow** and **Optimize** category endpoints, updates the version in the _O365_endpoints_latestversion.txt_ file, and writes the updated data to the _O365_endpoints_data.txt_ file.</span></span>

<span data-ttu-id="884ae-303">Le script génère une _ClientRequestId_ unique pour l’ordinateur sur lequel il est exécuté et réutilise cet ID dans plusieurs appels.</span><span class="sxs-lookup"><span data-stu-id="884ae-303">The script generates a unique _ClientRequestId_ for the computer it is executed on, and reuses this ID across multiple calls.</span></span> <span data-ttu-id="884ae-304">Cet ID est stocké dans le fichier _O365_endpoints_latestversion.txt_.</span><span class="sxs-lookup"><span data-stu-id="884ae-304">This ID is stored in the _O365_endpoints_latestversion.txt_ file.</span></span>

### <a name="to-run-the-powershell-script"></a><span data-ttu-id="884ae-305">Exécution du script PowerShell</span><span class="sxs-lookup"><span data-stu-id="884ae-305">To run the PowerShell script</span></span>

1. <span data-ttu-id="884ae-306">Copiez le script et enregistrez-le sur votre disque dur local ou sur l’emplacement de votre script sous _Get-O365WebServiceUpdates.ps1_.</span><span class="sxs-lookup"><span data-stu-id="884ae-306">Copy the script and save it to your local hard drive or script location as _Get-O365WebServiceUpdates.ps1_.</span></span>
1. <span data-ttu-id="884ae-307">Exécutez le script dans votre éditeur de script favori, tel que le code ISE ou VS PowerShell, ou à partir d’une console PowerShell à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="884ae-307">Execute the script in your preferred script editor such as the PowerShell ISE or VS Code, or from a PowerShell console using the following command:</span></span>

    ``` powershell
   powershell.exe -file <path>\Get-O365WebServiceUpdates.ps1
    ```

    <span data-ttu-id="884ae-308">Il n’existe aucun paramètre à transmettre au script.</span><span class="sxs-lookup"><span data-stu-id="884ae-308">There are no parameters to pass to the script.</span></span>

```powershell
<# Get-O365WebServiceUpdates.ps1
From https://aka.ms/ipurlws
v1.1 8/6/2019

DESCRIPTION
This script calls the REST API of the Office 365 IP and URL Web Service (Worldwide instance)
and checks to see if there has been a new update since the version stored in an existing
$Env:TEMP\O365_endpoints_latestversion.txt file in your user directory's temp folder
(usually C:\Users\<username>\AppData\Local\Temp).
If the file doesn't exist, or the latest version is newer than the current version in the
file, the script returns IPs and/or URLs that have been changed, added or removed in the latest
update and writes the new version and data to the output file $Env:TEMP\O365_endpoints_data.txt.

USAGE
Run as a scheduled task every 60 minutes.

PARAMETERS
n/a

PREREQUISITES
PS script execution policy: Bypass
PowerShell 3.0 or later
Does not require elevation
#>

#Requires -Version 3.0

# web service root URL
$ws = "https://endpoints.office.com"
# path where output files will be stored
$versionpath = $Env:TEMP + "\O365_endpoints_latestversion.txt"
$datapath = $Env:TEMP + "\O365_endpoints_data.txt"

# fetch client ID and version if version file exists; otherwise create new file and client ID
if (Test-Path $versionpath) {
    $content = Get-Content $versionpath
    $clientRequestId = $content[0]
    $lastVersion = $content[1]
    Write-Output ("Version file exists! Current version: " + $lastVersion)
}
else {
    Write-Output ("First run! Creating version file at " + $versionpath + ".")
    $clientRequestId = [GUID]::NewGuid().Guid
    $lastVersion = "0000000000"
    @($clientRequestId, $lastVersion) | Out-File $versionpath
}

# call version method to check the latest version, and pull new data if version number is different
$version = Invoke-RestMethod -Uri ($ws + "/version/Worldwide?clientRequestId=" + $clientRequestId)
if ($version.latest -gt $lastVersion) {
    Write-Host "New version of Office 365 worldwide commercial service instance endpoints detected"
    # write the new version number to the version file
    @($clientRequestId, $version.latest) | Out-File $versionpath
    # invoke endpoints method to get the new data
    $endpointSets = Invoke-RestMethod -Uri ($ws + "/endpoints/Worldwide?clientRequestId=" + $clientRequestId)
    # filter results for Allow and Optimize endpoints, and transform these into custom objects with port and category
    # URL results
    $flatUrls = $endpointSets | ForEach-Object {
        $endpointSet = $_
        $urls = $(if ($endpointSet.urls.Count -gt 0) { $endpointSet.urls } else { @() })
        $urlCustomObjects = @()
        if ($endpointSet.category -in ("Allow", "Optimize")) {
            $urlCustomObjects = $urls | ForEach-Object {
                [PSCustomObject]@{
                    category = $endpointSet.category;
                    url      = $_;
                    tcpPorts = $endpointSet.tcpPorts;
                    udpPorts = $endpointSet.udpPorts;
                }
            }
        }
        $urlCustomObjects
    }
    # IPv4 results
    $flatIp4s = $endpointSets | ForEach-Object {
        $endpointSet = $_
        $ips = $(if ($endpointSet.ips.Count -gt 0) { $endpointSet.ips } else { @() })
        # IPv4 strings contain dots
        $ip4s = $ips | Where-Object { $_ -like '*.*' }
        $ip4CustomObjects = @()
        if ($endpointSet.category -in ("Allow", "Optimize")) {
            $ip4CustomObjects = $ip4s | ForEach-Object {
                [PSCustomObject]@{
                    category = $endpointSet.category;
                    ip = $_;
                    tcpPorts = $endpointSet.tcpPorts;
                    udpPorts = $endpointSet.udpPorts;
                }
            }
        }
        $ip4CustomObjects
    }
    # IPv6 results
    $flatIp6s = $endpointSets | ForEach-Object {
        $endpointSet = $_
        $ips = $(if ($endpointSet.ips.Count -gt 0) { $endpointSet.ips } else { @() })
        # IPv6 strings contain colons
        $ip6s = $ips | Where-Object { $_ -like '*:*' }
        $ip6CustomObjects = @()
        if ($endpointSet.category -in ("Optimize")) {
            $ip6CustomObjects = $ip6s | ForEach-Object {
                [PSCustomObject]@{
                    category = $endpointSet.category;
                    ip = $_;
                    tcpPorts = $endpointSet.tcpPorts;
                    udpPorts = $endpointSet.udpPorts;
                }
            }
        }
        $ip6CustomObjects
    }

    # write output to screen
    Write-Output ("Client Request ID: " + $clientRequestId)
    Write-Output ("Last Version: " + $lastVersion)
    Write-Output ("New Version: " + $version.latest)
    Write-Output ""
    Write-Output "IPv4 Firewall IP Address Ranges"
    ($flatIp4s.ip | Sort-Object -Unique) -join "," | Out-String
    Write-Output "IPv6 Firewall IP Address Ranges"
    ($flatIp6s.ip | Sort-Object -Unique) -join "," | Out-String
    Write-Output "URLs for Proxy Server"
    ($flatUrls.url | Sort-Object -Unique) -join "," | Out-String
    Write-Output ("IP and URL data written to " + $datapath)

    # write output to data file
    Write-Output "Office 365 IP and UL Web Service data" | Out-File $datapath
    Write-Output "Worldwide instance" | Out-File $datapath -Append
    Write-Output "" | Out-File $datapath -Append
    Write-Output ("Version: " + $version.latest) | Out-File $datapath -Append
    Write-Output "" | Out-File $datapath -Append
    Write-Output "IPv4 Firewall IP Address Ranges" | Out-File $datapath -Append
    ($flatIp4s.ip | Sort-Object -Unique) -join "," | Out-File $datapath -Append
    Write-Output "" | Out-File $datapath -Append
    Write-Output "IPv6 Firewall IP Address Ranges" | Out-File $datapath -Append
    ($flatIp6s.ip | Sort-Object -Unique) -join "," | Out-File $datapath -Append
    Write-Output "" | Out-File $datapath -Append
    Write-Output "URLs for Proxy Server" | Out-File $datapath -Append
    ($flatUrls.url | Sort-Object -Unique) -join "," | Out-File $datapath -Append
}
else {
    Write-Host "Office 365 worldwide commercial service instance endpoints are up-to-date."
}
```

## <a name="example-python-script"></a><span data-ttu-id="884ae-309">Exemple de Script Python</span><span class="sxs-lookup"><span data-stu-id="884ae-309">Example Python Script</span></span>

<span data-ttu-id="884ae-p150">Voici un script Python testé avec Python 3.6.3 on Windows 10, que vous pouvez exécuter pour voir s’il y a des actions à exécuter pour les données mises à jour. Ce script vérifie le numéro de version pour les points de terminaison de l’instance Worldwide d’Office 365. Lorsqu’une modification a lieu, il télécharge les points de terminaison et les filtre en fonction de la catégorie _Allow_ et _Optimize_. Il utilise aussi un ClientRequestId unique dans plusieurs appels et enregistre la dernière version trouvée dans un fichier temporaire. Vous devez appeler ce script une fois toutes les heures afin de rechercher une mise à jour de version.</span><span class="sxs-lookup"><span data-stu-id="884ae-p150">Here is a Python script, tested with Python 3.6.3 on Windows 10, that you can run to see if there are actions you need to take for updated data. This script checks the version number for the Office 365 Worldwide instance endpoints. When there is a change, it downloads the endpoints and filters for the _Allow_ and _Optimize_ category endpoints. It also uses a unique ClientRequestId across multiple calls and saves the latest version found in a temporary file. You should call this script once an hour to check for a version update.</span></span>

```python
import json
import tempfile
from pathlib import Path
import urllib.request
import uuid
# helper to call the webservice and parse the response
def webApiGet(methodName, instanceName, clientRequestId):
    ws = "https://endpoints.office.com"
    requestPath = ws + '/' + methodName + '/' + instanceName + '?clientRequestId=' + clientRequestId
    request = urllib.request.Request(requestPath)
    with urllib.request.urlopen(request) as response:
        return json.loads(response.read().decode())
# path where client ID and latest version number will be stored
datapath = Path(tempfile.gettempdir() + '/endpoints_clientid_latestversion.txt')
# fetch client ID and version if data exists; otherwise create new file
if datapath.exists():
    with open(datapath, 'r') as fin:
        clientRequestId = fin.readline().strip()
        latestVersion = fin.readline().strip()
else:
    clientRequestId = str(uuid.uuid4())
    latestVersion = '0000000000'
    with open(datapath, 'w') as fout:
        fout.write(clientRequestId + '\n' + latestVersion)
# call version method to check the latest version, and pull new data if version number is different
version = webApiGet('version', 'Worldwide', clientRequestId)
if version['latest'] > latestVersion:
    print('New version of Office 365 worldwide commercial service instance endpoints detected')
    # write the new version number to the data file
    with open(datapath, 'w') as fout:
        fout.write(clientRequestId + '\n' + version['latest'])
    # invoke endpoints method to get the new data
    endpointSets = webApiGet('endpoints', 'Worldwide', clientRequestId)
    # filter results for Allow and Optimize endpoints, and transform these into tuples with port and category
    flatUrls = []
    for endpointSet in endpointSets:
        if endpointSet['category'] in ('Optimize', 'Allow'):
            category = endpointSet['category']
            urls = endpointSet['urls'] if 'urls' in endpointSet else []
            tcpPorts = endpointSet['tcpPorts'] if 'tcpPorts' in endpointSet else ''
            udpPorts = endpointSet['udpPorts'] if 'udpPorts' in endpointSet else ''
            flatUrls.extend([(category, url, tcpPorts, udpPorts) for url in urls])
    flatIps = []
    for endpointSet in endpointSets:
        if endpointSet['category'] in ('Optimize', 'Allow'):
            ips = endpointSet['ips'] if 'ips' in endpointSet else []
            category = endpointSet['category']
            # IPv4 strings have dots while IPv6 strings have colons
            ip4s = [ip for ip in ips if '.' in ip]
            tcpPorts = endpointSet['tcpPorts'] if 'tcpPorts' in endpointSet else ''
            udpPorts = endpointSet['udpPorts'] if 'udpPorts' in endpointSet else ''
            flatIps.extend([(category, ip, tcpPorts, udpPorts) for ip in ip4s])
    print('IPv4 Firewall IP Address Ranges')
    print(','.join(sorted(set([ip for (category, ip, tcpPorts, udpPorts) in flatIps]))))
    print('URLs for Proxy Server')
    print(','.join(sorted(set([url for (category, url, tcpPorts, udpPorts) in flatUrls]))))

    # TODO send mail (e.g. with smtplib/email modules) with new endpoints data
else:
    print('Office 365 worldwide commercial service instance endpoints are up-to-date')
```

## <a name="web-service-interface-versioning"></a><span data-ttu-id="884ae-315">Contrôle de version interface de Service Web</span><span class="sxs-lookup"><span data-stu-id="884ae-315">Web Service interface versioning</span></span>

<span data-ttu-id="884ae-316">Des mises à jour des paramètres ou des résultats pour ces méthodes de service Web peuvent être nécessaires à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="884ae-316">Updates to the parameters or results for these web service methods may be required in the future.</span></span> <span data-ttu-id="884ae-317">Une fois la version de disponibilité générale de ces services Web publiée, Microsoft fera des efforts raisonnables pour fournir à l’avance les mises à jour de matériel du service Web.</span><span class="sxs-lookup"><span data-stu-id="884ae-317">After the general availability version of these web services is published, Microsoft will make reasonable efforts to provide advance notice of material updates to the web service.</span></span> <span data-ttu-id="884ae-318">Lorsque Microsoft pense qu’une mise à jour nécessite des modifications pour les clients utilisant le service Web, Microsoft conserve la version précédente (une version avant) du service Web disponible au moins 12 mois après la publication de la nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="884ae-318">When Microsoft believes that an update will require changes to clients using the web service, Microsoft will keep the previous version (one version back) of the web service available for at least 12 months after the release of the new version.</span></span> <span data-ttu-id="884ae-319">Les clients qui n’effectuent pas de mise à niveau pendant ce temps peuvent être incapables d’accéder au service Web et à ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="884ae-319">Customers who do not upgrade during that time may be unable to access the web service and its methods.</span></span> <span data-ttu-id="884ae-320">Les clients doivent s’assurer que les clients du service Web continuent de fonctionner sans erreur si les modifications suivantes sont apportées à la signature de l’interface de service Web :</span><span class="sxs-lookup"><span data-stu-id="884ae-320">Customers must ensure that clients of the web service continue working without error if the following changes are made to the web service interface signature:</span></span>

- <span data-ttu-id="884ae-321">Ajout d’un nouveau paramètre facultatif à une méthode web existant qui ne doit pas être fournie par des clients plus anciens et n’affecte pas le résultat qu’un client plus ancien reçoit.</span><span class="sxs-lookup"><span data-stu-id="884ae-321">Adding a new optional parameter to an existing web method that doesn't have to be provided by older clients and doesn't impact the result an older client receives.</span></span>
- <span data-ttu-id="884ae-322">Ajout d’un attribut avec un nouveau nom dans l’un des éléments REST de réponse ou de colonnes supplémentaires au CSV de réponse.</span><span class="sxs-lookup"><span data-stu-id="884ae-322">Adding a new named attribute in one of the response REST items or additional columns to the response CSV.</span></span>
- <span data-ttu-id="884ae-323">Ajout d’une nouvelle méthode web avec un nouveau nom qui n’est pas appelée par les clients plus anciens.</span><span class="sxs-lookup"><span data-stu-id="884ae-323">Adding a new web method with a new name that is not called by the older clients.</span></span>

## <a name="update-notifications"></a><span data-ttu-id="884ae-324">Notifications de mise à jour</span><span class="sxs-lookup"><span data-stu-id="884ae-324">Update notifications</span></span>

<span data-ttu-id="884ae-325">Vous pouvez utiliser plusieurs méthodes pour recevoir des notifications par courrier électronique lorsque des modifications apportées aux adresses IP et aux URL sont publiées sur le service Web.</span><span class="sxs-lookup"><span data-stu-id="884ae-325">You can use a few different methods to get email notifications when changes to the IP addresses and URLs are published to the web service.</span></span>

- <span data-ttu-id="884ae-326">Pour utiliser une solution de flux Microsoft, voir [utiliser Microsoft Flow pour recevoir un courrier électronique pour les modifications apportées aux adresses IP et URL d’Office 365](https://techcommunity.microsoft.com/t5/Office-365-Networking/Use-Microsoft-Flow-to-receive-an-email-for-changes-to-Office-365/m-p/240651).</span><span class="sxs-lookup"><span data-stu-id="884ae-326">To use a Microsoft Flow solution, see [Use Microsoft Flow to receive an email for changes to Office 365 IP Addresses and URLs](https://techcommunity.microsoft.com/t5/Office-365-Networking/Use-Microsoft-Flow-to-receive-an-email-for-changes-to-Office-365/m-p/240651).</span></span>
- <span data-ttu-id="884ae-327">Pour déployer une application de logique Azure à l’aide d’un modèle ARM, voir [notification de mise à jour d’Office 365 (v 1.1)](https://aka.ms/ipurlws-updates-template).</span><span class="sxs-lookup"><span data-stu-id="884ae-327">To deploy an Azure Logic App using an ARM template, see [Office 365 Update Notification (v1.1)](https://aka.ms/ipurlws-updates-template).</span></span>
- <span data-ttu-id="884ae-328">Pour écrire votre propre script de notification à l’aide de PowerShell, voir [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage).</span><span class="sxs-lookup"><span data-stu-id="884ae-328">To write your own notification script using PowerShell, see [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage).</span></span>

## <a name="exporting-a-proxy-pac-file"></a><span data-ttu-id="884ae-329">Exporte un fichier PAC Proxy</span><span class="sxs-lookup"><span data-stu-id="884ae-329">Exporting a Proxy PAC file</span></span>

<span data-ttu-id="884ae-330">[Get-PacFile](https://www.powershellgallery.com/packages/Get-PacFile) est un script PowerShell qui lit les derniers points de terminaison réseau à partir de l’adresse IP et du service Web d’URL Office 365 et crée un exemple de fichier PAC.</span><span class="sxs-lookup"><span data-stu-id="884ae-330">[Get-PacFile](https://www.powershellgallery.com/packages/Get-PacFile) is a PowerShell script that reads the latest network endpoints from the Office 365 IP Address and URL web service and creates a sample PAC file.</span></span> <span data-ttu-id="884ae-331">Pour plus d’informations sur l’utilisation de Get-PacFile, voir [utiliser un fichier PAC pour le routage direct du trafic Office 365 vital](managing-office-365-endpoints.md#use-a-pac-file-for-direct-routing-of-vital-office-365-traffic).</span><span class="sxs-lookup"><span data-stu-id="884ae-331">For information on using Get-PacFile, see [Use a PAC file for direct routing of vital Office 365 traffic](managing-office-365-endpoints.md#use-a-pac-file-for-direct-routing-of-vital-office-365-traffic).</span></span>

## <a name="related-topics"></a><span data-ttu-id="884ae-332">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="884ae-332">Related Topics</span></span>
  
[<span data-ttu-id="884ae-333">URL et plages d’adresses IP Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-333">Office 365 URLs and IP address ranges</span></span>](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2)

[<span data-ttu-id="884ae-334">Gestion des points de terminaison Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-334">Managing Office 365 endpoints</span></span>](managing-office-365-endpoints.md)
  
[<span data-ttu-id="884ae-335">Points de terminaison Office 365 - FAQ</span><span class="sxs-lookup"><span data-stu-id="884ae-335">Office 365 endpoints FAQ</span></span>](https://support.office.com/article/d4088321-1c89-4b96-9c99-54c75cae2e6d)

[<span data-ttu-id="884ae-336">Principes de connectivité réseau Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-336">Office 365 Network Connectivity Principles</span></span>](microsoft-365-network-connectivity-principles.md)

[<span data-ttu-id="884ae-337">Paramétrage des performances et du réseau Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-337">Office 365 network and performance tuning</span></span>](network-planning-and-performance.md)

[<span data-ttu-id="884ae-338">Évaluation de la connectivité réseau Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-338">Assessing Office 365 network connectivity</span></span>](assessing-network-connectivity.md)
  
[<span data-ttu-id="884ae-339">Qualité des médias et performances de connectivité réseau dans Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="884ae-339">Media Quality and Network Connectivity Performance in Skype for Business Online</span></span>](https://support.office.com/article/5fe3e01b-34cf-44e0-b897-b0b2a83f0917)
  
[<span data-ttu-id="884ae-340">Optimisation de votre réseau pour Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="884ae-340">Optimizing your network for Skype for Business Online</span></span>](https://support.office.com/article/b363bdca-b00d-4150-96c3-ec7eab5a8a43)

[<span data-ttu-id="884ae-341">Réglage des performances Office 365 à l’aide du planning de référence et de l’historique des performances</span><span class="sxs-lookup"><span data-stu-id="884ae-341">Office 365 performance tuning using baselines and performance history</span></span>](performance-tuning-using-baselines-and-history.md)
  
[<span data-ttu-id="884ae-342">Plan de résolution des problèmes de performances pour Office 365</span><span class="sxs-lookup"><span data-stu-id="884ae-342">Performance troubleshooting plan for Office 365</span></span>](performance-troubleshooting-plan.md)