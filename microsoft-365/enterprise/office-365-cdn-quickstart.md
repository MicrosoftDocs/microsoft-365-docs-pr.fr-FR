---
title: Démarrage rapide du réseau de distribution de contenu (CDN) Office 365
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/04/2020
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
- m365initiative-coredeploy
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- MET150
- SPO160
description: Démarrage rapide du réseau de distribution de contenu (CDN) Office 365
ms.openlocfilehash: e541b2ea63a69644de22329c45bd6963749964f7
ms.sourcegitcommit: d76a4c07f0be2938372bdfae50e0e4d523bd8e9f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "48456410"
---
# <a name="office-365-content-delivery-network-cdn-quickstart"></a><span data-ttu-id="a284b-103">Démarrage rapide du réseau de distribution de contenu (CDN) Office 365</span><span class="sxs-lookup"><span data-stu-id="a284b-103">Office 365 Content Delivery Network (CDN) Quickstart</span></span>

<span data-ttu-id="a284b-104">Vous pouvez utiliser le réseau de distribution de contenu **(CDN) Office 365** intégré pour héberger des ressources statiques (images, JavaScript, feuilles de style, fichiers WOFF) afin de fournir de meilleures performances pour vos pages SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a284b-104">You can use the built-in **Office 365 Content Delivery Network (CDN)** to host static assets (images, JavaScript, Stylesheets, WOFF files) to provide better performance for your SharePoint Online pages.</span></span> <span data-ttu-id="a284b-105">Le réseau de distribution de contenu Office 365 améliore les performances en procédant à la mise en cache des ressources statiques au plus près des navigateurs qui les demandent, ce qui permet d’accélérer les téléchargements et de réduire la latence.</span><span class="sxs-lookup"><span data-stu-id="a284b-105">The Office 365 CDN improves performance by caching static assets closer to the browsers requesting them, which helps to speed up downloads and reduce latency.</span></span> <span data-ttu-id="a284b-106">En outre, le CDN Office 365 utilise le protocole HTTP/2 pour améliorer la compression et le pipelining HTTP.</span><span class="sxs-lookup"><span data-stu-id="a284b-106">Also, the Office 365 CDN uses the HTTP/2 protocol for improved compression and HTTP pipelining.</span></span> <span data-ttu-id="a284b-107">Le réseau de distribution de contenu Office 365 est inclus dans votre abonnement SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="a284b-107">The Office 365 CDN service is included as part of your SharePoint Online subscription.</span></span>

<span data-ttu-id="a284b-108">Pour obtenir des instructions plus détaillées, voir Utiliser le réseau de distribution de contenu [(CDN) Office 365 avec SharePoint Online.](use-microsoft-365-cdn-with-spo.md)</span><span class="sxs-lookup"><span data-stu-id="a284b-108">For more detailed information guidance see [Use the Office 365 Content Delivery Network (CDN) with SharePoint Online](use-microsoft-365-cdn-with-spo.md).</span></span>

>[!NOTE]
><span data-ttu-id="a284b-109">Le CDN Office 365 est uniquement disponible pour les clients dans le cloud de production (dans le monde).</span><span class="sxs-lookup"><span data-stu-id="a284b-109">The Office 365 CDN is only available to tenants in the production (worldwide) cloud.</span></span> <span data-ttu-id="a284b-110">Les locataires du gouvernement des États-Unis, de la Chine et de l’Allemagne ne supportent pas actuellement le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="a284b-110">Tenants in the US Government, China and Germany clouds do not currently support the Office 365 CDN.</span></span>

## <a name="use-the-page-diagnostics-for-sharepoint-tool-to-identify-items-not-in-cdn"></a><span data-ttu-id="a284b-111">Utiliser l’outil Diagnostic de page pour SharePoint pour identifier les éléments qui ne sont pas dans le CDN</span><span class="sxs-lookup"><span data-stu-id="a284b-111">Use the Page Diagnostics for SharePoint tool to identify items not in CDN</span></span>

<span data-ttu-id="a284b-112">Vous pouvez utiliser l’extension de navigateur de l’outil Diagnostic de page pour SharePoint pour lister facilement les ressources dans vos pages SharePoint Online qui peuvent être **ajoutées** à une origine cdN.</span><span class="sxs-lookup"><span data-stu-id="a284b-112">You can use the **Page Diagnostics for SharePoint tool** browser extension to easily list assets in your SharePoint Online pages that can be added to a CDN origin.</span></span>

<span data-ttu-id="a284b-113">L’outil Diagnostic de page pour **SharePoint** est une extension de navigateur pour les nouveaux navigateurs Microsoft Edge (et Chrome qui analyse à la fois le portail moderne SharePoint Online et les pages de site de publication https://www.microsoft.com/edge) classiques).</span><span class="sxs-lookup"><span data-stu-id="a284b-113">The **Page Diagnostics for SharePoint tool** is a browser extension for the new Microsoft Edge (https://www.microsoft.com/edge) and Chrome browsers that analyzes both SharePoint Online modern portal and classic publishing site pages.</span></span> <span data-ttu-id="a284b-114">L’outil fournit un rapport pour chaque page analysée montrant comment la page se comporte par rapport à un ensemble défini de critères de performance.</span><span class="sxs-lookup"><span data-stu-id="a284b-114">The tool provides a report for each analyzed page showing how the page performs against a defined set of performance criteria.</span></span> <span data-ttu-id="a284b-115">Pour installer et découvrir l’outil Diagnostic de page pour SharePoint, consultez [Utiliser l’outil Diagnostic de page pour SharePoint Online](https://aka.ms/perftool).</span><span class="sxs-lookup"><span data-stu-id="a284b-115">To install and learn about the Page Diagnostics for SharePoint tool, visit [Use the Page Diagnostics tool for SharePoint Online](https://aka.ms/perftool).</span></span>

<span data-ttu-id="a284b-116">Lorsque vous exécutez l’outil Diagnostic de page pour SharePoint sur une page SharePoint Online, vous pouvez cliquer sur l’onglet Tests de **diagnostic** pour voir la liste des ressources qui ne sont pas hébergées par le CDN.</span><span class="sxs-lookup"><span data-stu-id="a284b-116">When you run the Page Diagnostics for SharePoint tool on a SharePoint Online page, you can click the **Diagnostic Tests** tab to see a list of assets not being hosted by the CDN.</span></span> <span data-ttu-id="a284b-117">Ces ressources sont répertoriées sous l’en-tête Réseau de distribution de contenu **(CDN),** comme illustré dans la capture d’écran ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a284b-117">These assets will be listed under the heading **Content Delivery Network (CDN) check** as shown in the screenshot below.</span></span>

![Diagnostics de page](../media/page-diagnostics-for-spo/pagediag-results-general.PNG)

>[!NOTE]
><span data-ttu-id="a284b-119">L’Outil Diagnostic de page fonctionne uniquement pour SharePoint Online et ne peut pas être utilisé sur une page système SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a284b-119">The Page Diagnostics tool only works for SharePoint Online, and cannot be used on a SharePoint system page.</span></span>

## <a name="cdn-overview"></a><span data-ttu-id="a284b-120">Vue d’ensemble du CDN</span><span class="sxs-lookup"><span data-stu-id="a284b-120">CDN Overview</span></span>

<span data-ttu-id="a284b-121">Le CDN Office 365 est conçu pour optimiser les performances pour les utilisateurs en distribuant des objets fréquemment utilisés tels que des images et des fichiers javascript sur un réseau global haut débit, ce qui réduit le temps de chargement des pages et permet d’accéder aux objets hébergés aussi près que possible de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a284b-121">The Office 365 CDN is designed to optimize performance for users by distributing frequently accessed objects like images and javascript files over a high-speed global network, reducing page load time and providing access to hosted objects as close as possible to the user.</span></span> <span data-ttu-id="a284b-122">Le CDN récupère vos ressources à partir d’un emplacement appelé _origine._</span><span class="sxs-lookup"><span data-stu-id="a284b-122">The CDN fetches your assets from a location called an _origin_.</span></span> <span data-ttu-id="a284b-123">Une origine peut être un site SharePoint, une bibliothèque de documents ou un dossier accessible par une URL.</span><span class="sxs-lookup"><span data-stu-id="a284b-123">An origin can be a SharePoint site, document library or folder that is accessible by a URL.</span></span>

<span data-ttu-id="a284b-124">Le CDN Office 365 est séparé en deux types de base :</span><span class="sxs-lookup"><span data-stu-id="a284b-124">The Office 365 CDN is separated into two basic types:</span></span>

- <span data-ttu-id="a284b-125">**Le CDN public** est conçu pour être utilisé pour les images JS (JavaScript), CSS (Feuilles de style), Web Font File (WOFF, WOFF2) et les images non propriétaires telles que les logos d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="a284b-125">**Public CDN** is designed to be used for JS (JavaScript), CSS (StyleSheets), Web Font File (WOFF, WOFF2) and non-proprietary images like company logos.</span></span>
- <span data-ttu-id="a284b-126">**Le CDN privé** est conçu pour être utilisé pour les images (PNG, JPG, JPEG, etc.).</span><span class="sxs-lookup"><span data-stu-id="a284b-126">**Private CDN** is designed to be used for images (PNG, JPG, JPEG, etc.).</span></span>

<span data-ttu-id="a284b-127">Vous pouvez choisir d’avoir des origines publiques ou privées pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a284b-127">You can choose to have both public or private origins for your organization.</span></span> <span data-ttu-id="a284b-128">La plupart des organisations choisiront d’implémenter une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="a284b-128">Most organizations will choose to implement a combination of the two.</span></span> <span data-ttu-id="a284b-129">Les options publiques et privées offrent des gains de performances similaires, mais chacune possède des attributs et des avantages uniques.</span><span class="sxs-lookup"><span data-stu-id="a284b-129">Both public and private options provide similar performance gains, but each has unique attributes and advantages.</span></span> <span data-ttu-id="a284b-130">Pour plus d’informations sur les origines du CDN public et privé, voir Choisir si [chaque origine doit être publique ou privée.](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate)</span><span class="sxs-lookup"><span data-stu-id="a284b-130">For more information about public and private CDN origins, see [Choose whether each origin should be public or private](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate).</span></span>

## <a name="how-to-enable-public-and-private-cdn-with-the-default-configuration"></a><span data-ttu-id="a284b-131">Comment activer le CDN public et privé avec la configuration par défaut</span><span class="sxs-lookup"><span data-stu-id="a284b-131">How to enable Public and Private CDN with the default configuration</span></span>
<span data-ttu-id="a284b-132">Avant d’apporter des modifications aux paramètres du CDN client, vous devez vérifier qu’il répond aux stratégies de conformité, de sécurité et de confidentialité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a284b-132">Before you make changes to the tenant CDN settings, you should verify that it meets compliance, security and privacy policies of your organization.</span></span>

<span data-ttu-id="a284b-133">Pour obtenir des paramètres de configuration plus détaillés, ou si vous avez déjà activé le CDN et souhaitez ajouter des emplacements supplémentaires (origines), consultez la section Installer et configurer le [CDN Office 365](use-microsoft-365-cdn-with-spo.md#set-up-and-configure-the-office-365-cdn-by-using-the-sharepoint-online-management-shell) à l’aide de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="a284b-133">For more detailed configuration settings, or if you have already enabled CDN and want to add additional locations (origins), please see the section [Set up and configure the Office 365 CDN by using the SharePoint Online Management Shell](use-microsoft-365-cdn-with-spo.md#set-up-and-configure-the-office-365-cdn-by-using-the-sharepoint-online-management-shell)</span></span>

<span data-ttu-id="a284b-134">Connectez-vous à votre client à l’aide de SharePoint Online Management Shell :</span><span class="sxs-lookup"><span data-stu-id="a284b-134">Connect to your tenant using the SharePoint Online Management Shell:</span></span>

```PowerShell
Connect-SPOService -Url https://<YourTenantName>-admin.sharepoint.com
```

<span data-ttu-id="a284b-135">Pour permettre à votre organisation d’utiliser des origines publiques et privées avec la configuration par défaut, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a284b-135">To enable your organization to use both public and private origins with the default configuration, type the following command:</span></span>

```PowerShell
Set-SPOTenantCdnEnabled -CdnType Both -Enable $true
```

<span data-ttu-id="a284b-136">La sortie de ces cmdlets doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="a284b-136">Output of these cmdlets should look like the following:</span></span>

![Sortie des Set-SPOTenantCdnEnabled](../media/O365-CDN/o365-cdn-enable-output.png)

## <a name="see-also"></a><span data-ttu-id="a284b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a284b-138">See also</span></span>

[<span data-ttu-id="a284b-139">Utiliser l’outil Diagnostic de page pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a284b-139">Use the Page Diagnostics tool for SharePoint Online</span></span>](https://aka.ms/perftool)

[<span data-ttu-id="a284b-140">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a284b-140">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)

[<span data-ttu-id="a284b-141">Réseaux de distribution de contenu</span><span class="sxs-lookup"><span data-stu-id="a284b-141">Content Delivery Networks</span></span>](https://aka.ms/o365cdns)

[<span data-ttu-id="a284b-142">Planification réseau et optimisation des performances pour Office 365</span><span class="sxs-lookup"><span data-stu-id="a284b-142">Network planning and performance tuning for Office 365</span></span>](https://aka.ms/tune)

[<span data-ttu-id="a284b-143">Série de performances SharePoint - Série de vidéos sur le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="a284b-143">SharePoint Performance Series - Office 365 CDN video series</span></span>](https://www.youtube.com/playlist?list=PLR9nK3mnD-OWMfr1BA9mr5oCw2aJXw4WA)
