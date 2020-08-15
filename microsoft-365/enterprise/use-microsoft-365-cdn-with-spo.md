---
title: Utiliser le réseau de distribution de contenu (CDN) Office 365 avec SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 2/19/2020
audience: ITPro
ms.topic: article
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
- MET150
- SPO160
ms.assetid: bebb285f-1d54-4f79-90a5-94985afc6af8
description: Découvrez comment utiliser le réseau de distribution de contenu (CDN) Office 365 pour accélérer la remise de vos ressources SharePoint Online.
ms.openlocfilehash: 0ef7922f4e8881065f97a5fdeb4f21242c2b6467
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689639"
---
# <a name="use-the-office-365-content-delivery-network-cdn-with-sharepoint-online"></a><span data-ttu-id="b1e9b-103">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-103">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>

<span data-ttu-id="b1e9b-104">Vous pouvez utiliser le réseau de distribution de contenu Office 365 intégré pour héberger des ressources statiques afin d’améliorer les performances de vos pages SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-104">You can use the built-in Office 365 Content Delivery Network (CDN) to host static assets to provide better performance for your SharePoint Online pages.</span></span> <span data-ttu-id="b1e9b-105">Le réseau de distribution de contenu Office 365 améliore les performances en procédant à la mise en cache des ressources statiques au plus près des navigateurs qui les demandent, ce qui permet d’accélérer les téléchargements et de réduire la latence.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-105">The Office 365 CDN improves performance by caching static assets closer to the browsers requesting them, which helps to speed up downloads and reduce latency.</span></span> <span data-ttu-id="b1e9b-106">Par ailleurs, le CDN Office 365 utilise le [protocole http/2](https://en.wikipedia.org/wiki/HTTP/2) pour une compression améliorée et un traitement en pipeline http.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-106">Also, the Office 365 CDN uses the [HTTP/2 protocol](https://en.wikipedia.org/wiki/HTTP/2) for improved compression and HTTP pipelining.</span></span> <span data-ttu-id="b1e9b-107">Le réseau de distribution de contenu Office 365 est inclus dans votre abonnement SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-107">The Office 365 CDN service is included as part of your SharePoint Online subscription.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-108">Le CDN Office 365 est uniquement disponible pour les clients dans le Cloud de **production** (dans le monde entier).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-108">The Office 365 CDN is only available to tenants in the **Production** (worldwide) cloud.</span></span> <span data-ttu-id="b1e9b-109">Les clients des nuages des États-Unis, de Chine et d’Allemagne ne prennent actuellement pas en charge le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-109">Tenants in the US Government, China and Germany clouds do not currently support the Office 365 CDN.</span></span>

<span data-ttu-id="b1e9b-110">Le réseau de distribution de contenu Office 365 est composé de plusieurs réseaux de distribution de contenu qui vous permettent d’héberger des ressources statiques à différents emplacements (ou _origines_) et de les servir à partir de réseaux à haut débit mondiaux.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-110">The Office 365 CDN is composed of multiple CDNs that allow you to host static assets in multiple locations, or _origins_, and serve them from global high-speed networks.</span></span> <span data-ttu-id="b1e9b-111">Selon le type de contenu que vous souhaitez héberger sur le réseau de distribution de contenu Office 365, vous pouvez ajouter des origines **publiques**, **privées** ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-111">Depending on the kind of content you want to host in the Office 365 CDN, you can add **public** origins, **private** origins or both.</span></span> <span data-ttu-id="b1e9b-112">Voir [choisir si chaque origine doit être publique ou privée](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate) pour plus d’informations sur la différence entre les origines publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-112">See [Choose whether each origin should be public or private](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate) for more information on the difference between public and private origins.</span></span>

<span data-ttu-id="b1e9b-113">![Diagramme conceptuel de CDN Office 365](../media/O365-CDN/o365-cdn-flow-transparent.svg "Diagramme conceptuel de CDN Office 365")</span><span class="sxs-lookup"><span data-stu-id="b1e9b-113">![Office 365 CDN conceptual diagram](../media/O365-CDN/o365-cdn-flow-transparent.svg "Office 365 CDN conceptual diagram")</span></span>

<span data-ttu-id="b1e9b-114">Si vous êtes déjà familiarisé avec la façon dont CDN fonctionne, vous devez uniquement effectuer quelques étapes pour activer le CDN Office 365 pour votre client.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-114">If you are already familiar with the way that CDNs work, you only need to complete a few steps to enable the Office 365 CDN for your tenant.</span></span> <span data-ttu-id="b1e9b-115">Cette rubrique décrit la procédure.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-115">This topic describes how.</span></span> <span data-ttu-id="b1e9b-116">Pour plus d’informations sur la prise en main de l’hébergement de vos composants statiques, consultez la rubrique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-116">Read on for information about how to get started hosting your static assets.</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-117">Il existe d’autres CDN hébergés par Microsoft qui peuvent être utilisés avec Office 365 pour des scénarios d’utilisation spécialisés, mais qui ne sont pas abordés dans cette rubrique, car ils ne font pas partie de l’étendue du CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-117">There are other Microsoft-hosted CDNs that can be used with Office 365 for specialized usage scenarios, but are not discussed in this topic because they fall outside the scope of the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-118">Pour plus d’informations, consultez la rubrique [autres Microsoft CDN](content-delivery-networks.md#other-microsoft-cdns).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-118">For more information, see [Other Microsoft CDNs](content-delivery-networks.md#other-microsoft-cdns).</span></span>

 <span data-ttu-id="b1e9b-119">**La tête revient à la [planification réseau et au réglage des performances pour Office 365](https://aka.ms/tune).**</span><span class="sxs-lookup"><span data-stu-id="b1e9b-119">**Head back to [Network planning and performance tuning for Office 365](https://aka.ms/tune).**</span></span>

## <a name="overview-of-working-with-the-office-365-cdn-in-sharepoint-online"></a><span data-ttu-id="b1e9b-120">Vue d’ensemble de l’utilisation du CDN Office 365 dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-120">Overview of working with the Office 365 CDN in SharePoint Online</span></span>

<span data-ttu-id="b1e9b-121">Pour configurer le CDN Office 365 pour votre organisation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-121">To set up the Office 365 CDN for your organization, you follow these basic steps:</span></span>

+ [<span data-ttu-id="b1e9b-122">Planifier le déploiement du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-122">Plan for deployment of the Office 365 CDN</span></span>](use-microsoft-365-cdn-with-spo.md#plan-for-deployment-of-the-office-365-cdn)

  + <span data-ttu-id="b1e9b-123">[Déterminez les composants statiques que vous souhaitez héberger sur le CDN](use-microsoft-365-cdn-with-spo.md#CDNAssets).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-123">[Determine which static assets you want to host on the CDN](use-microsoft-365-cdn-with-spo.md#CDNAssets).</span></span>
  + <span data-ttu-id="b1e9b-124">[Déterminez l’emplacement où vous souhaitez stocker vos biens](use-microsoft-365-cdn-with-spo.md#CDNStoreAssets).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-124">[Determine where you want to store your assets](use-microsoft-365-cdn-with-spo.md#CDNStoreAssets).</span></span> <span data-ttu-id="b1e9b-125">Cet emplacement peut être un site, une bibliothèque ou un dossier SharePoint et est appelé « _origine_».</span><span class="sxs-lookup"><span data-stu-id="b1e9b-125">This location can be a SharePoint site, library or folder and is called an _origin_.</span></span>
  + <span data-ttu-id="b1e9b-126">[Indiquez si chaque origine doit être publique ou privée](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-126">[Choose whether each origin should be public or private](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate).</span></span> <span data-ttu-id="b1e9b-127">Vous pouvez ajouter plusieurs origines des types publics et privés.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-127">You can add multiple origins of both public and private types.</span></span>

+ <span data-ttu-id="b1e9b-128">Installer et configurer le CDN à l’aide de PowerShell ou de l’interface de ligne de commande SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-128">Set up and configure the CDN, using either PowerShell or the SharePoint Online CLI</span></span>

  + [<span data-ttu-id="b1e9b-129">Installer et configurer le CDN à l’aide de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="b1e9b-129">Set up and configure the CDN by using the SharePoint Online Management Shell</span></span>](use-microsoft-365-cdn-with-spo.md#CDNSetupinPShell)
  + [<span data-ttu-id="b1e9b-130">Installer et configurer le CDN à l’aide de PowerShell PnP</span><span class="sxs-lookup"><span data-stu-id="b1e9b-130">Set up and configure the CDN by using PnP PowerShell</span></span>](use-microsoft-365-cdn-with-spo.md#CDNSetupinPnPPosh)
  + [<span data-ttu-id="b1e9b-131">Installer et configurer le CDN à l’aide de l’interface CLI Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-131">Set up and configure the CDN by using the Office 365 CLI</span></span>](use-microsoft-365-cdn-with-spo.md#CDNSetupinCLI)

  <span data-ttu-id="b1e9b-132">Lorsque vous effectuez cette étape, vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-132">When you complete this step, you will have:</span></span>

  + <span data-ttu-id="b1e9b-133">Activation du CDN pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-133">Enabled the CDN for your organization.</span></span>
  + <span data-ttu-id="b1e9b-134">Ajout de vos origines, identifiant chaque origine comme étant public ou privé.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-134">Added your origins, identifying each origin as public or private.</span></span>

<span data-ttu-id="b1e9b-135">Une fois que vous avez terminé l’installation, vous pouvez [gérer le CDN Office 365](use-microsoft-365-cdn-with-spo.md#CDNManage) au fil du temps en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-135">Once you're done with setup, you can [Manage the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#CDNManage) over time by:</span></span>
  
+ <span data-ttu-id="b1e9b-136">Ajout, mise à jour et suppression de ressources</span><span class="sxs-lookup"><span data-stu-id="b1e9b-136">Adding, updating, and removing assets</span></span>
+ <span data-ttu-id="b1e9b-137">Ajout et suppression d’origines</span><span class="sxs-lookup"><span data-stu-id="b1e9b-137">Adding and removing origins</span></span>
+ <span data-ttu-id="b1e9b-138">Configuration des stratégies de CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-138">Configuring CDN policies</span></span>
+ <span data-ttu-id="b1e9b-139">Si nécessaire, désactivation du CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-139">If necessary, disabling the CDN</span></span>

<span data-ttu-id="b1e9b-140">Enfin, reportez-vous [à la rubrique utilisation de vos ressources CDN](use-microsoft-365-cdn-with-spo.md#using-your-cdn-assets) pour en savoir plus sur l’accès à vos ressources de CDN à partir d’origines publiques et privées.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-140">Finally, see [Using your CDN assets](use-microsoft-365-cdn-with-spo.md#using-your-cdn-assets) to learn about accessing your CDN assets from both public and private origins.</span></span>

<span data-ttu-id="b1e9b-141">Pour obtenir des conseils sur la résolution des problèmes courants, consultez [la rubrique Troubleshooting the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#CDNTroubleshooting) .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-141">See [Troubleshooting the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#CDNTroubleshooting) for guidance on resolving common issues.</span></span>

## <a name="plan-for-deployment-of-the-office-365-cdn"></a><span data-ttu-id="b1e9b-142">Planifier le déploiement du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-142">Plan for deployment of the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-143">Avant de déployer le CDN Office 365 pour votre client 365 Office, vous devez prendre en compte les facteurs suivants dans le cadre de votre processus de planification.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-143">Before you deploy the Office 365 CDN for your Office 365 tenant, you should consider the following factors as part of your planning process.</span></span>

  + [<span data-ttu-id="b1e9b-144">Déterminer les ressources statiques que vous souhaitez héberger sur le CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-144">Determine which static assets you want to host on the CDN</span></span>](use-microsoft-365-cdn-with-spo.md#CDNAssets)
  + [<span data-ttu-id="b1e9b-145">Déterminer où vous souhaitez stocker vos ressources</span><span class="sxs-lookup"><span data-stu-id="b1e9b-145">Determine where you want to store your assets</span></span>](use-microsoft-365-cdn-with-spo.md#CDNStoreAssets)
  + [<span data-ttu-id="b1e9b-146">Choisir si chaque origine doit être publique ou privée</span><span class="sxs-lookup"><span data-stu-id="b1e9b-146">Choose whether each origin should be public or private</span></span>](use-microsoft-365-cdn-with-spo.md#CDNOriginChoosePublicPrivate)

<span data-ttu-id="b1e9b-147"><a name="CDNAssets"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-147"><a name="CDNAssets"> </a></span></span>
### <a name="determine-which-static-assets-you-want-to-host-on-the-cdn"></a><span data-ttu-id="b1e9b-148">Déterminer les ressources statiques que vous souhaitez héberger sur le CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-148">Determine which static assets you want to host on the CDN</span></span>

<span data-ttu-id="b1e9b-149">En règle générale, les CDN sont plus efficaces pour héberger des _composants statiques_ou des ressources qui ne changent pas très souvent.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-149">In general, CDNs are most effective for hosting _static assets_, or assets that don't change very often.</span></span> <span data-ttu-id="b1e9b-150">En règle générale, il est recommandé d’identifier les fichiers qui répondent à une partie ou l’ensemble de ces conditions :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-150">A good rule of thumb is to identify files that meet some or all of these conditions:</span></span>

+ <span data-ttu-id="b1e9b-151">Fichiers statiques incorporés dans une page (par exemple les scripts et les images) qui peuvent avoir un impact significatif sur le chargement des pages</span><span class="sxs-lookup"><span data-stu-id="b1e9b-151">Static files embedded in a page (like scripts and images) that may have a significant incremental impact on page load times</span></span>
+ <span data-ttu-id="b1e9b-152">Fichiers volumineux comme les fichiers exécutables et les fichiers d’installation</span><span class="sxs-lookup"><span data-stu-id="b1e9b-152">Large files like executables and installation files</span></span>
+ <span data-ttu-id="b1e9b-153">Bibliothèques de ressources qui prennent en charge le code côté client</span><span class="sxs-lookup"><span data-stu-id="b1e9b-153">Resource libraries that support client-side code</span></span>

<span data-ttu-id="b1e9b-154">Par exemple, les petits fichiers qui sont fréquemment demandés comme les images de site et les scripts peuvent considérablement améliorer les performances de rendu de site et réduire de façon incrémentielle la charge sur vos sites SharePoint Online lorsque vous les ajoutez à une origine de CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-154">For example, small files that are repeatedly requested like site images and scripts can significantly improve site rendering performance and incrementally reduce the load on your SharePoint Online sites when you add them to a CDN origin.</span></span> <span data-ttu-id="b1e9b-155">Des fichiers plus volumineux, tels que des fichiers exécutables d’installation, peuvent être téléchargés à partir du CDN, ce qui offre un impact positif sur les performances et la réduction ultérieure de la charge sur votre site SharePoint Online, même si elles ne sont pas accessibles aussi souvent.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-155">Larger files such as installation executables can be downloaded from the CDN, delivering a positive performance impact and subsequent reduction of the load on your SharePoint Online site, even if they are not accessed as often.</span></span>

<span data-ttu-id="b1e9b-156">L’amélioration des performances en fonction des fichiers dépend de nombreux facteurs, notamment de la proximité du client par le point de terminaison CDN le plus proche, des conditions passagères sur le réseau local, etc.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-156">Performance improvement on a per-file basis is dependent on many factors, including the client's proximity to the nearest CDN endpoint, transient conditions on the local network, and so forth.</span></span> <span data-ttu-id="b1e9b-157">De nombreux fichiers statiques sont relativement petits et peuvent être téléchargés à partir d’Office 365 en moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-157">Many static files are quite small, and can be downloaded from Office 365 in less than a second.</span></span> <span data-ttu-id="b1e9b-158">Toutefois, une page Web peut contenir un grand nombre de fichiers incorporés avec un temps de téléchargement cumulé de plusieurs secondes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-158">However, a web page may contain many embedded files with a cumulative download time of several seconds.</span></span> <span data-ttu-id="b1e9b-159">Le traitement de ces fichiers à partir du CDN peut considérablement réduire le temps de chargement global de la page.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-159">Serving these files from the CDN can significantly reduce the overall page load time.</span></span> <span data-ttu-id="b1e9b-160">Voir [Quels sont les gains de performances fournis par un CDN ?](content-delivery-networks.md#what-performance-gains-does-a-cdn-provide) pour obtenir un exemple.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-160">See [What performance gains does a CDN provide?](content-delivery-networks.md#what-performance-gains-does-a-cdn-provide) for an example.</span></span>

<span data-ttu-id="b1e9b-161"><a name="CDNStoreAssets"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-161"><a name="CDNStoreAssets"> </a></span></span>
### <a name="determine-where-you-want-to-store-your-assets"></a><span data-ttu-id="b1e9b-162">Déterminer où vous souhaitez stocker vos ressources</span><span class="sxs-lookup"><span data-stu-id="b1e9b-162">Determine where you want to store your assets</span></span>

<span data-ttu-id="b1e9b-163">Le CDN extrait vos biens à partir d’un emplacement appelé _origine_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-163">The CDN fetches your assets from a location called an _origin_.</span></span> <span data-ttu-id="b1e9b-164">Une origine peut être un site SharePoint, une bibliothèque de documents ou un dossier accessible par une URL.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-164">An origin can be a SharePoint site, document library or folder that is accessible by a URL.</span></span> <span data-ttu-id="b1e9b-165">Vous disposez d’une grande souplesse lorsque vous spécifiez des origines pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-165">You have great flexibility when you specify origins for your organization.</span></span> <span data-ttu-id="b1e9b-166">Par exemple, vous pouvez spécifier plusieurs origines ou une seule origine pour placer toutes vos ressources de CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-166">For example, you can specify multiple origins or a single origin where you want to put all your CDN assets.</span></span> <span data-ttu-id="b1e9b-167">Vous pouvez choisir d’avoir à la fois des origines publiques ou privées pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-167">You can choose to have both public or private origins for your organization.</span></span> <span data-ttu-id="b1e9b-168">La plupart des organisations choisiront d’implémenter une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-168">Most organizations will choose to implement a combination of the two.</span></span>

<span data-ttu-id="b1e9b-169">Vous pouvez créer un nouveau conteneur pour vos origines, comme des dossiers ou des bibliothèques de documents, et ajouter des fichiers que vous souhaitez mettre à disposition à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-169">You can create new container for your origins such as folders or document libraries, and add files you want to make available from the CDN.</span></span> <span data-ttu-id="b1e9b-170">Cette approche est intéressante si vous disposez d’un ensemble spécifique de ressources que vous souhaitez mettre à disposition du CDN et que vous souhaitez limiter l’ensemble des ressources CDN uniquement aux fichiers du conteneur.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-170">This is a good approach if you have a specific set of assets you want to be available from the CDN, and want to restrict the set of CDN assets to only those files in the container.</span></span>

<span data-ttu-id="b1e9b-171">Vous pouvez également configurer une collection de sites, un site, une bibliothèque ou un dossier existant en tant qu’origine, ce qui rendra tous les composants éligibles dans le conteneur disponible à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-171">You can also configure an existing site collection, site, library or folder as an origin, which will make all eligible assets in the container available from the CDN.</span></span> <span data-ttu-id="b1e9b-172">Avant d’ajouter un conteneur existant en tant qu’origine, il est important de vous assurer que vous connaissez bien son contenu et ses autorisations afin de ne pas exposer par inadvertance les ressources à l’accès anonyme ou aux utilisateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-172">Before you add an existing container as an origin, it's important to make sure you are aware of its contents and permissions so you do not inadvertently expose assets to anonymous access or unauthorized users.</span></span>

<span data-ttu-id="b1e9b-173">Vous pouvez définir des _stratégies de CDN_ pour exclure le contenu de vos origines du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-173">You can define _CDN policies_ to exclude content in your origins from the CDN.</span></span> <span data-ttu-id="b1e9b-174">Les stratégies de CDN excluent les ressources dans les origines publiques ou privées par attributs tels que le _type de fichier_ et la _Classification de site_, et sont appliquées à toutes les origines de l’CdnType (privées ou publiques) que vous spécifiez dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-174">CDN policies exclude assets in public or private origins by attributes such as _file type_ and _site classification_, and are applied to all origins of the CdnType (private or public) you specify in the policy.</span></span> <span data-ttu-id="b1e9b-175">Par exemple, si vous ajoutez une origine privée composée d’un site qui contient plusieurs sous-sites, vous pouvez définir une stratégie pour exclure les sites marqués comme **confidentiels** de sorte que le contenu des sites avec cette classification appliquée ne sera pas pris en charge par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-175">For example, if you add a private origin consisting of a site that contains multiple subsites, you can define a policy to exclude sites marked as **Confidential** so content from sites with that classification applied will not be served from the CDN.</span></span> <span data-ttu-id="b1e9b-176">La stratégie s’applique au contenu de _toutes les_ origines privées que vous avez ajoutées au CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-176">The policy will apply to content from _all_ private origins you have added to the CDN.</span></span>
  
<span data-ttu-id="b1e9b-177">Gardez à l’esprit que plus le nombre d’origines est élevé, plus l’impact sur le service CDN est important pour traiter les demandes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-177">Keep in mind that the greater the number of origins, the greater the impact on the time it takes the CDN service to process requests.</span></span> <span data-ttu-id="b1e9b-178">Nous vous recommandons de limiter le nombre d’origines autant que possible.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-178">We recommend that you limit the number of origins as much as possible.</span></span>
  
<span data-ttu-id="b1e9b-179"><a name="CDNOriginChoosePublicPrivate"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-179"><a name="CDNOriginChoosePublicPrivate"> </a></span></span>
### <a name="choose-whether-each-origin-should-be-public-or-private"></a><span data-ttu-id="b1e9b-180">Choisir si chaque origine doit être publique ou privée</span><span class="sxs-lookup"><span data-stu-id="b1e9b-180">Choose whether each origin should be public or private</span></span>

<span data-ttu-id="b1e9b-181">Lorsque vous identifiez une origine, vous spécifiez si elle doit être _publique_ ou _privée_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-181">When you identify an origin, you specify whether it should be made _public_ or _private_.</span></span> <span data-ttu-id="b1e9b-182">L’accès aux biens CDN dans les origines publiques est anonyme et le contenu CDN des origines privées est sécurisé par des jetons générés dynamiquement pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-182">Access to CDN assets in public origins is anonymous, and CDN content in private origins is secured by dynamically generated tokens for greater security.</span></span> <span data-ttu-id="b1e9b-183">Quelle que soit l’option que vous choisissez, Microsoft effectue tout le lourd de levage lorsqu’il s’agit de l’administration du CDN lui-même.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-183">Regardless of which option you choose, Microsoft does all the heavy lifting for you when it comes to administration of the CDN itself.</span></span> <span data-ttu-id="b1e9b-184">Vous pouvez également modifier votre avis ultérieurement, une fois que vous avez configuré le CDN et identifié vos origines.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-184">Also, you can change your mind later, after you've set up the CDN and identified your origins.</span></span>

<span data-ttu-id="b1e9b-185">Les options publiques et privées offrent des gains de performances similaires, mais chacune a des avantages et des attributs uniques.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-185">Both public and private options provide similar performance gains, but each has unique attributes and advantages.</span></span>

<span data-ttu-id="b1e9b-186">Les origines **publiques** au sein du CDN Office 365 sont accessibles de manière anonyme, et les ressources hébergées sont accessibles par quiconque dispose de l’URL de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-186">**Public** origins within the Office 365 CDN are accessible anonymously, and hosted assets can be accessed by anyone who has the URL to the asset.</span></span> <span data-ttu-id="b1e9b-187">Comme l’accès au contenu des origines publiques est anonyme, vous ne devez l’utiliser que pour mettre en cache du contenu générique non sensible, comme des scripts, des icônes, des images et des fichiers javascript.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-187">Because access to content in public origins is anonymous, you should only use them to cache non-sensitive generic content such as javascript files, scripts, icons and images.</span></span>

<span data-ttu-id="b1e9b-188">Les origines **privées** dans le CDN Office 365 fournissent un accès privé au contenu utilisateur comme les bibliothèques de documents, les sites et les images propriétaires SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-188">**Private** origins within the Office 365 CDN provide private access to user content such as SharePoint Online document libraries, sites and proprietary images.</span></span> <span data-ttu-id="b1e9b-189">L’accès au contenu des origines privées est sécurisé par des jetons générés de manière dynamique afin de permettre uniquement aux utilisateurs disposant d’autorisations sur la bibliothèque de documents ou l’emplacement de stockage d’origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-189">Access to content in private origins is secured by dynamically generated tokens so it can only be accessed by users with permissions to the original document library or storage location.</span></span> <span data-ttu-id="b1e9b-190">Les origines privées dans le CDN Office 365 ne peuvent être utilisées que pour le contenu SharePoint Online, et vous pouvez uniquement accéder aux ressources dans des origines privées via la redirection à partir de votre client SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-190">Private origins in the Office 365 CDN can only be used for SharePoint Online content, and you can only access assets in private origins through redirection from your SharePoint Online tenant.</span></span>

<span data-ttu-id="b1e9b-191">Pour plus d’informations sur l’accès CDN aux biens dans une origine privée, consultez la rubrique [utilisation des biens dans des origines privées](use-microsoft-365-cdn-with-spo.md#using-assets-in-private-origins).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-191">You can read more about how CDN access to assets in a private origin works in [Using assets in private origins](use-microsoft-365-cdn-with-spo.md#using-assets-in-private-origins).</span></span>

#### <a name="attributes-and-advantages-of-hosting-assets-in-public-origins"></a><span data-ttu-id="b1e9b-192">Attributs et avantages de l’hébergement des biens dans des origines publiques</span><span class="sxs-lookup"><span data-stu-id="b1e9b-192">Attributes and advantages of hosting assets in public origins</span></span>
  
+ <span data-ttu-id="b1e9b-193">Les ressources exposées dans une origine publique sont accessibles par tout le monde de manière anonyme.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-193">Assets exposed in a public origin are accessible by everyone anonymously.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="b1e9b-194">Vous ne devez jamais placer de ressources qui contiennent des informations utilisateur ou qui sont considérées comme sensibles à votre organisation dans une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-194">You should never place resources that contain user information or are considered sensitive to your organization in a public origin.</span></span>
+ <span data-ttu-id="b1e9b-195">Si vous supprimez une ressource d’une origine publique, celle-ci reste disponible pendant un maximum de 30 jours à partir du cache. Cependant, nous rendons les liens vers la ressource dans le CDN non valides dans les 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-195">If you remove an asset from a public origin, the asset may continue to be available for up to 30 days from the cache; however, we will invalidate links to the asset in the CDN within 15 minutes.</span></span>
+ <span data-ttu-id="b1e9b-196">Lorsque vous hébergez des feuilles de style (fichiers CSS) depuis une origine publique, vous pouvez utiliser les URI et les chemins d’accès relatifs dans le code.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-196">When you host style sheets (CSS files) in a public origin, you can use relative paths and URIs within the code.</span></span> <span data-ttu-id="b1e9b-197">Cela signifie que vous pouvez faire référence à l’emplacement d’images d’arrière-plan et d’autres objets de manière relative, par rapport à l’emplacement de la ressource qui les appelle.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-197">This means that you can reference the location of background images and other objects relative to the location of the asset that's calling it.</span></span>
+ <span data-ttu-id="b1e9b-198">Même si vous pouvez coder en dur l’URL d’une origine publique, cette méthode n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-198">While you can hard code a public origin's URL, doing so is not recommended.</span></span> <span data-ttu-id="b1e9b-199">En effet, si l’accès au CDN devient indisponible, l’URL ne renverra pas automatiquement à votre organisation dans SharePoint Online, ce qui pourrait générer des liens défectueux et d’autres erreurs.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-199">The reason for this is that if access to the CDN becomes unavailable, the URL will not automatically resolve to your organization in SharePoint Online and might result in broken links and other errors.</span></span>
+ <span data-ttu-id="b1e9b-200">Les types de fichier par défaut inclus pour les origines publiques sont. CSS,. EOT,. gif,. ico,. jpeg,. jpg,. js,. map,. png,. svg,. ttf,. WOFF et. woff2.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-200">The default file types that are included for public origins are .css, .eot, .gif, .ico, .jpeg, .jpg, .js, .map, .png, .svg, .ttf, .woff and .woff2.</span></span> <span data-ttu-id="b1e9b-201">Vous pouvez spécifier des types de fichier supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-201">You can specify additional file types.</span></span>
+ <span data-ttu-id="b1e9b-202">Vous pouvez configurer une stratégie pour exclure les ressources identifiées par les classifications de site que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-202">You can configure a policy to exclude assets that have been identified by site classifications that you specify.</span></span> <span data-ttu-id="b1e9b-203">Par exemple, vous pouvez choisir d’exclure toutes les ressources marquées comme « confidentiel » ou « accès réservé », même s’il s’agit d’un type de fichier autorisé et qu’elles ont une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-203">For example, you can choose to exclude all assets that are marked as "confidential" or "restricted" even if they are an allowed file type and are located in a public origin.</span></span>

#### <a name="attributes-and-advantages-of-hosting-assets-in-private-origins"></a><span data-ttu-id="b1e9b-204">Attributs et avantages de l’hébergement des biens dans des origines privées</span><span class="sxs-lookup"><span data-stu-id="b1e9b-204">Attributes and advantages of hosting assets in private origins</span></span>

+ <span data-ttu-id="b1e9b-205">Les origines privées ne peuvent être utilisées que pour les ressources SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-205">Private origins can only be used for SharePoint Online assets.</span></span>
+ <span data-ttu-id="b1e9b-206">Les utilisateurs peuvent accéder aux biens à partir d’une origine privée uniquement s’ils disposent des autorisations nécessaires pour accéder au conteneur.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-206">Users can only access the assets from a private origin if they have permissions to access the container.</span></span> <span data-ttu-id="b1e9b-207">Vous êtes protégé contre l’accès anonyme à ces ressources.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-207">Anonymous access to these assets is prevented.</span></span>
+ <span data-ttu-id="b1e9b-208">Les biens dans des origines privées doivent être référencés à partir du client SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-208">Assets in private origins must be referred from the SharePoint Online tenant.</span></span> <span data-ttu-id="b1e9b-209">L’accès direct aux ressources CDN privées ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-209">Direct access to private CDN assets does not work.</span></span>
+ <span data-ttu-id="b1e9b-210">Si vous supprimez un bien de l’origine privée, il se peut que la ressource continue à être disponible pendant une heure au maximum à partir du cache ; Toutefois, nous allons invalider les liens vers la ressource dans le CDN dans un délai de 15 minutes après la suppression de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-210">If you remove an asset from the private origin, the asset may continue to be available for up to an hour from the cache; however, we will invalidate links to the asset in the CDN within 15 minutes of the asset's removal.</span></span>
+ <span data-ttu-id="b1e9b-211">Les types de fichier par défaut inclus pour les origines privées sont les suivants : .gif, .ico, .jpeg, .jpg, .js et .png.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-211">The default file types that are included for private origins are .gif, .ico, .jpeg, .jpg, .js, and .png.</span></span> <span data-ttu-id="b1e9b-212">Vous pouvez spécifier des types de fichier supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-212">You can specify additional file types.</span></span>
+ <span data-ttu-id="b1e9b-213">Tout comme avec les origines publiques, vous pouvez configurer une stratégie pour exclure les ressources identifiées par des classifications de site que vous spécifiez même si vous utilisez des caractères génériques pour inclure toutes les ressources dans un dossier ou une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-213">Just like with public origins, you can configure a policy to exclude assets that have been identified by site classifications that you specify even if you use wildcards to include all assets within a folder or document library.</span></span>

<span data-ttu-id="b1e9b-214">Pour plus d’informations sur les raisons d’utiliser le CDN Office 365, les concepts généraux du CDN et d’autres CDN Microsoft que vous pouvez utiliser avec votre client Office 365, consultez la rubrique [Content Delivery Networks](content-delivery-networks.md).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-214">For more information about why to use the Office 365 CDN, general CDN concepts, and other Microsoft CDNs you can use with your Office 365 tenant, see [Content Delivery Networks](content-delivery-networks.md).</span></span>

### <a name="default-cdn-origins"></a><span data-ttu-id="b1e9b-215">Origines par défaut du CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-215">Default CDN origins</span></span>

<span data-ttu-id="b1e9b-216">Sauf indication contraire, Office 365 configure certaines origines par défaut lorsque vous activez le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-216">Unless you specify otherwise, Office 365 sets up some default origins for you when you enable the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-217">Si vous choisissez initialement de ne pas les mettre en service, vous pouvez ajouter ces origines une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-217">If you initially opt not to provision them, you can add these origins after you complete setup.</span></span> <span data-ttu-id="b1e9b-218">À moins que vous ne compreniez les conséquences de l’omission de la configuration des origines par défaut et que vous avez une raison particulière de le faire, vous devez les autoriser à être créées lorsque vous activez le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-218">Unless you understand the consequences of skipping the setup of default origins and have a specific reason for doing so, you should allow them to be created when you enable the CDN.</span></span>
  
<span data-ttu-id="b1e9b-219">Origines du CDN privé par défaut :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-219">Default private CDN origins:</span></span>
  
+ <span data-ttu-id="b1e9b-220">\*/userphoto.aspx</span><span class="sxs-lookup"><span data-stu-id="b1e9b-220">\*/userphoto.aspx</span></span>
+ <span data-ttu-id="b1e9b-221">\*/siteassets</span><span class="sxs-lookup"><span data-stu-id="b1e9b-221">\*/siteassets</span></span>

<span data-ttu-id="b1e9b-222">Origines par défaut du CDN public :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-222">Default public CDN origins:</span></span>
  
+ <span data-ttu-id="b1e9b-223">\*/masterpage</span><span class="sxs-lookup"><span data-stu-id="b1e9b-223">\*/masterpage</span></span>
+ <span data-ttu-id="b1e9b-224">\*Bibliothèque/style</span><span class="sxs-lookup"><span data-stu-id="b1e9b-224">\*/style library</span></span>
+ <span data-ttu-id="b1e9b-225">\*/clientsideassets</span><span class="sxs-lookup"><span data-stu-id="b1e9b-225">\*/clientsideassets</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-226">_clientsideassets_ est une origine publique par défaut qui a été ajoutée au service de CDN Office 365 en décembre 2017.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-226">_clientsideassets_ is a default public origin that was added to the Office 365 CDN service in December 2017.</span></span> <span data-ttu-id="b1e9b-227">Cette origine doit être présente afin que les solutions SharePoint Framework du CDN fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-227">This origin must be present in order for SharePoint Framework solutions in the CDN to work.</span></span> <span data-ttu-id="b1e9b-228">Si vous avez activé le CDN Office 365 avant le 2017 décembre, ou si vous avez ignoré le programme d’installation des origines par défaut lorsque vous avez activé le CDN, vous pouvez ajouter manuellement cette origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-228">If you enabled the Office 365 CDN prior to December 2017, or if you skipped setup of default origins when you enabled the CDN, you can manually add this origin.</span></span> <span data-ttu-id="b1e9b-229">Pour plus d’informations, consultez la rubrique [mon composant WebPart côté client ou la solution SharePoint Framework ne fonctionne pas](use-microsoft-365-cdn-with-spo.md#my-client-side-web-part-or-sharepoint-framework-solution-isnt-working).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-229">For more information, see [My client-side web part or SharePoint Framework solution isn't working](use-microsoft-365-cdn-with-spo.md#my-client-side-web-part-or-sharepoint-framework-solution-isnt-working).</span></span>

<span data-ttu-id="b1e9b-230"><a name="CDNSetupinPShell"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-230"><a name="CDNSetupinPShell"> </a></span></span>
## <a name="set-up-and-configure-the-office-365-cdn-by-using-the-sharepoint-online-management-shell"></a><span data-ttu-id="b1e9b-231">Installer et configurer le CDN Office 365 à l’aide de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="b1e9b-231">Set up and configure the Office 365 CDN by using the SharePoint Online Management Shell</span></span>

<span data-ttu-id="b1e9b-232">Les procédures décrites dans cette section vous obligent à utiliser SharePoint Online Management Shell pour se connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-232">The procedures in this section require you to use the SharePoint Online Management Shell to connect to SharePoint Online.</span></span> <span data-ttu-id="b1e9b-233">Pour plus d’informations, voir [Connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-233">For instructions, see [Connect to SharePoint Online PowerShell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps).</span></span>

<span data-ttu-id="b1e9b-234">Procédez comme suit pour installer et configurer le CDN afin d’héberger vos ressources dans SharePoint Online à l’aide de SharePoint Online Management Shell.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-234">Complete these steps to set up and configure the CDN to host your assets in SharePoint Online using the SharePoint Online Management Shell.</span></span>

<details>
  <summary><span data-ttu-id="b1e9b-235">Cliquez pour développer</span><span class="sxs-lookup"><span data-stu-id="b1e9b-235">Click to expand</span></span></summary>

### <a name="enable-your-organization-to-use-the-office-365-cdn"></a><span data-ttu-id="b1e9b-236">Permettre à votre organisation d’utiliser le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-236">Enable your organization to use the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-237">Avant de modifier les paramètres de CDN de client, vous devez récupérer l’état actuel de la configuration de CDN privé dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-237">Before you make changes to the tenant CDN settings, you should retrieve the current status of the private CDN configuration in your Office 365 tenant.</span></span> <span data-ttu-id="b1e9b-238">Connectez-vous à votre client à l’aide de SharePoint Online Management Shell :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-238">Connect to your tenant using the SharePoint Online Management Shell:</span></span>

``` powershell
Connect-SPOService -Url https://contoso-admin.sharepoint.com
```

<span data-ttu-id="b1e9b-239">À présent, utilisez la cmdlet **Get-SPOTenantCdnEnabled** pour récupérer les paramètres d’État CDN à partir du client :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-239">Now use the **Get-SPOTenantCdnEnabled** cmdlet to retrieve the CDN status settings from the tenant:</span></span>

``` powershell
Get-SPOTenantCdnEnabled -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-240">L’état du CDN pour le CdnType spécifié s’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-240">The status of the CDN for the specified CdnType will output to the screen.</span></span>

<span data-ttu-id="b1e9b-241">Utilisez l’applet de commande **Set-SPOTenantCdnEnabled** pour permettre à votre organisation d’utiliser le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-241">Use the **Set-SPOTenantCdnEnabled** cmdlet to enable your organization to use the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-242">Vous pouvez permettre à votre organisation d’utiliser des origines publiques, des origines privées ou les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-242">You can enable your organization to use public origins, private origins, or both at once.</span></span> <span data-ttu-id="b1e9b-243">Vous pouvez également configurer le CDN de sorte qu’il ignore le paramétrage des origines par défaut lorsque vous l’activez.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-243">You can also configure the CDN to skip the setup of default origins when you enable it.</span></span> <span data-ttu-id="b1e9b-244">Vous pouvez toujours ajouter ces origines plus tard, comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-244">You can always add these origins later as described in this topic.</span></span>
  
<span data-ttu-id="b1e9b-245">Dans Windows PowerShell pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-245">In Windows Powershell for SharePoint Online:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType <Public | Private | Both> -Enable $true
```

<span data-ttu-id="b1e9b-246">Par exemple, pour permettre à votre organisation d’utiliser des origines publiques et privées, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-246">For example, to enable your organization to use both public and private origins, type the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Both -Enable $true
```

<span data-ttu-id="b1e9b-247">Pour permettre à votre organisation d’utiliser des origines publiques et privées, mais de ne pas configurer les origines par défaut, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-247">To enable your organization to use both public and private origins but skip setting up the default origins, type the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Both -Enable $true -NoDefaultOrigins
```

<span data-ttu-id="b1e9b-248">Consultez la rubrique [origines du CDN par défaut](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) pour obtenir des informations sur les origines qui sont configurées par défaut lorsque vous activez le CDN Office 365, ainsi que l’impact potentiel de l’omission de la configuration des origines par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-248">See [Default CDN origins](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) for information about the origins that are provisioned by default when you enable the Office 365 CDN, and the potential impact of skipping the setup of default origins.</span></span>

<span data-ttu-id="b1e9b-249">Pour permettre à votre organisation d’utiliser des origines publiques, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-249">To enable your organization to use public origins, type the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Public -Enable $true
```

<span data-ttu-id="b1e9b-250">Pour permettre à votre organisation d’utiliser des origines privées, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-250">To enable your organization to use private origins, type the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Private -Enable $true
```

<span data-ttu-id="b1e9b-251">Pour plus d’informations sur cette cmdlet, consultez la rubrique [Set-SPOTenantCdnEnabled](https://technet.microsoft.com/library/mt790765.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-251">For more information about this cmdlet, see [Set-SPOTenantCdnEnabled](https://technet.microsoft.com/library/mt790765.aspx).</span></span>

<span data-ttu-id="b1e9b-252"><a name="Office365CDNforSPOFileType"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-252"><a name="Office365CDNforSPOFileType"> </a></span></span>
### <a name="change-the-list-of-file-types-to-include-in-the-office-365-cdn-optional"></a><span data-ttu-id="b1e9b-253">Modifier la liste des types de fichiers à inclure dans le CDN Office 365 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b1e9b-253">Change the list of file types to include in the Office 365 CDN (Optional)</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-254">Lorsque vous définissez des types de fichiers à l’aide de la cmdlet **Set-SPOTenantCdnPolicy** , vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-254">When you define file types by using the **Set-SPOTenantCdnPolicy** cmdlet, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-255">Si vous souhaitez ajouter d’autres types de fichiers à la liste, utilisez d’abord la cmdlet pour savoir quels types de fichiers sont déjà autorisés et les inclure dans la liste en même temps que les nouveaux.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-255">If you want to add additional file types to the list, use the cmdlet first to find out what file types are already allowed and include them in the list along with your new ones.</span></span>
  
<span data-ttu-id="b1e9b-256">La cmdlet **Set-SPOTenantCdnPolicy** permet de définir des types de fichiers statiques qui peuvent être hébergés par des origines publiques et privées dans le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-256">Use the **Set-SPOTenantCdnPolicy** cmdlet to define static file types that can be hosted by public and private origins in the CDN.</span></span> <span data-ttu-id="b1e9b-257">Par défaut, les types d’éléments communs sont autorisés, par exemple. CSS,. gif,. jpg et. js.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-257">By default, common asset types are allowed, for example .css, .gif, .jpg, and .js.</span></span>

<span data-ttu-id="b1e9b-258">Dans Windows PowerShell pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-258">In Windows PowerShell for SharePoint Online:</span></span>

``` powershell
Set-SPOTenantCdnPolicy -CdnType <Public | Private> -PolicyType IncludeFileExtensions -PolicyValue "<Comma-separated list of file types >"
```

<span data-ttu-id="b1e9b-259">Par exemple, pour permettre au CDN d’héberger des fichiers. CSS et. png, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-259">For example, to enable the CDN to host .css and .png files, you would enter the command:</span></span>

``` powershell
Set-SPOTenantCdnPolicy -CdnType Private -PolicyType IncludeFileExtensions -PolicyValue "CSS,PNG"
```

<span data-ttu-id="b1e9b-260">Pour voir les types de fichiers actuellement autorisés par le CDN, utilisez la cmdlet **Get-SPOTenantCdnPolicies** :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-260">To see what file types are currently allowed by the CDN, use the **Get-SPOTenantCdnPolicies** cmdlet:</span></span>

``` powershell
Get-SPOTenantCdnPolicies -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-261">Pour plus d’informations sur ces applets de commande, voir [Set-SPOTenantCdnPolicy](https://technet.microsoft.com/library/mt800839.aspx) et [Get-SPOTenantCdnPolicies](https://technet.microsoft.com/library/mt800838.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-261">For more information about these cmdlets, see [Set-SPOTenantCdnPolicy](https://technet.microsoft.com/library/mt800839.aspx) and [Get-SPOTenantCdnPolicies](https://technet.microsoft.com/library/mt800838.aspx).</span></span>

<span data-ttu-id="b1e9b-262"><a name="Office365CDNforSPOSiteClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-262"><a name="Office365CDNforSPOSiteClassification"> </a></span></span>
### <a name="change-the-list-of-site-classifications-you-want-to-exclude-from-the-office-365-cdn-optional"></a><span data-ttu-id="b1e9b-263">Modifier la liste des classifications de sites que vous souhaitez exclure du CDN Office 365 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b1e9b-263">Change the list of site classifications you want to exclude from the Office 365 CDN (Optional)</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-264">Lorsque vous excluez les classifications de site à l’aide de la cmdlet **Set-SPOTenantCdnPolicy** , vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-264">When you exclude site classifications by using the **Set-SPOTenantCdnPolicy** cmdlet, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-265">Si vous souhaitez exclure des classifications de site supplémentaires, utilisez d’abord la cmdlet pour savoir quelles classifications sont déjà exclues, puis ajoutez-les en même temps que les nouvelles classifications.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-265">If you want to exclude additional site classifications, use the cmdlet first to find out what classifications are already excluded and then add them along with your new ones.</span></span>

<span data-ttu-id="b1e9b-266">Utilisez la cmdlet **Set-SPOTenantCdnPolicy** pour exclure les classifications de site que vous ne souhaitez pas rendre disponibles via le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-266">Use the **Set-SPOTenantCdnPolicy** cmdlet to exclude site classifications that you do not want to make available over the CDN.</span></span> <span data-ttu-id="b1e9b-267">Par défaut, aucune classification de site n’est exclue.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-267">By default, no site classifications are excluded.</span></span>

<span data-ttu-id="b1e9b-268">Dans Windows PowerShell pour SharePoint Online :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-268">In Windows PowerShell for SharePoint Online:</span></span>

``` powershell
Set-SPOTenantCdnPolicy -CdnType <Public | Private> -PolicyType ExcludeRestrictedSiteClassifications  -PolicyValue "<Comma-separated list of site classifications >"
```

<span data-ttu-id="b1e9b-269">Pour voir les classifications de site actuellement restreintes, utilisez la cmdlet **Get-SPOTenantCdnPolicies** :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-269">To see what site classifications are currently restricted, use the **Get-SPOTenantCdnPolicies** cmdlet:</span></span>

``` powershell
Get-SPOTenantCdnPolicies -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-270">Les propriétés qui seront renvoyées sont _IncludeFileExtensions_, _ExcludeRestrictedSiteClassifications_ et _ExcludeIfNoScriptDisabled_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-270">The properties that will be returned are _IncludeFileExtensions_, _ExcludeRestrictedSiteClassifications_ and _ExcludeIfNoScriptDisabled_.</span></span>

<span data-ttu-id="b1e9b-271">La propriété _IncludeFileExtensions_ contient la liste des extensions de fichiers qui seront fournies à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-271">The _IncludeFileExtensions_ property contains the list of file extensions that will be served from the CDN.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-272">Les extensions de fichier par défaut sont différentes entre public et Private.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-272">The default file extensions are different between public and private.</span></span>

<span data-ttu-id="b1e9b-273">La propriété _ExcludeRestrictedSiteClassifications_ contient les classifications de site que vous souhaitez exclure du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-273">The _ExcludeRestrictedSiteClassifications_ property contains the site classifications that you want to exclude from the CDN.</span></span> <span data-ttu-id="b1e9b-274">Par exemple, vous pouvez exclure des sites marqués comme **confidentiels** de sorte que le contenu de sites avec cette classification appliquée ne sera pas pris en charge par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-274">For example, you can exclude sites marked as **Confidential** so content from sites with that classification applied will not be served from the CDN.</span></span>

<span data-ttu-id="b1e9b-275">La propriété _ExcludeIfNoScriptDisabled_ exclut le contenu du CDN en fonction des paramètres d’attribut _NoScript_ au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-275">The _ExcludeIfNoScriptDisabled_ property excludes content from the CDN based on the site-level _NoScript_ attribute settings.</span></span> <span data-ttu-id="b1e9b-276">Par défaut, l’attribut _NoScript_ est défini sur **activé** pour les sites _modernes_ et **désactivé** pour les sites _classiques_ .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-276">By default, the _NoScript_ attribute is set to **Enabled** for _Modern_ sites and **Disabled** for _Classic_ sites.</span></span> <span data-ttu-id="b1e9b-277">Cela dépend de vos paramètres de client.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-277">This depends on your tenant settings.</span></span>

<span data-ttu-id="b1e9b-278">Pour plus d’informations sur ces applets de commande, voir [Set-SPOTenantCdnPolicy](https://technet.microsoft.com/library/mt800839.aspx) et [Get-SPOTenantCdnPolicies](https://technet.microsoft.com/library/mt800838.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-278">For more information about these cmdlets, see [Set-SPOTenantCdnPolicy](https://technet.microsoft.com/library/mt800839.aspx) and [Get-SPOTenantCdnPolicies](https://technet.microsoft.com/library/mt800838.aspx).</span></span>

<span data-ttu-id="b1e9b-279"><a name="Office365CDNforSPOOriginPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-279"><a name="Office365CDNforSPOOriginPosh"> </a></span></span>
### <a name="add-an-origin-for-your-assets"></a><span data-ttu-id="b1e9b-280">Ajouter une origine pour vos biens</span><span class="sxs-lookup"><span data-stu-id="b1e9b-280">Add an origin for your assets</span></span>

<span data-ttu-id="b1e9b-281">Utilisez l’applet de commande **Add-SPOTenantCdnOrigin** pour définir une origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-281">Use the **Add-SPOTenantCdnOrigin** cmdlet to define an origin.</span></span> <span data-ttu-id="b1e9b-282">Vous pouvez définir plusieurs origines.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-282">You can define multiple origins.</span></span> <span data-ttu-id="b1e9b-283">L’origine est une URL pointant vers un dossier ou une bibliothèque SharePoint qui contient les ressources qui doivent être hébergées par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-283">The origin is a URL that points to a SharePoint library or folder that contains the assets that you want to be hosted by the CDN.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b1e9b-284">Vous ne devez jamais placer de ressources qui contiennent des informations utilisateur ou qui sont considérées comme sensibles à votre organisation dans une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-284">You should never place resources that contain user information or are considered sensitive to your organization in a public origin.</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType <Public | Private> -OriginUrl <path>
```

<span data-ttu-id="b1e9b-285">La valeur _path_ est le chemin d’accès relatif à la bibliothèque ou au dossier qui contient les composants.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-285">The value of _path_ is the relative path to the library or folder that contains the assets.</span></span> <span data-ttu-id="b1e9b-286">Vous pouvez utiliser des caractères génériques en plus des chemins d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-286">You can use wildcards in addition to relative paths.</span></span> <span data-ttu-id="b1e9b-287">Les origines prennent en charge les caractères génériques ajoutés à l’URL.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-287">Origins support wildcards prepended to the URL.</span></span> <span data-ttu-id="b1e9b-288">Cela vous permet de créer des origines qui s’étendent sur plusieurs sites.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-288">This allows you to create origins that span multiple sites.</span></span> <span data-ttu-id="b1e9b-289">Par exemple, pour inclure toutes les ressources dans le dossier MasterPages pour tous vos sites en tant qu’origine publique dans le CDN, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-289">For example, to include all of the assets in the masterpages folder for all of your sites as a public origin within the CDN, type the following command:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Public -OriginUrl */masterpage
```

+ <span data-ttu-id="b1e9b-290">Le modificateur de caractère générique \* **/** peut uniquement être utilisé au début du chemin d’accès et correspondra à tous les segments d’URL sous l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-290">The wildcard modifier \***/** can only be used at the beginning of the path, and will match all URL segments under the specified URL.</span></span>
+ <span data-ttu-id="b1e9b-291">Le chemin d’accès peut pointer vers une bibliothèque de documents, un dossier ou un site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-291">The path can point to a document library, folder or site.</span></span> <span data-ttu-id="b1e9b-292">Par exemple, le chemin d’accès _\*/site1_ correspondra à toutes les bibliothèques de documents sous le site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-292">For example, the path _\*/site1_ will match all the document libraries under the site.</span></span>

<span data-ttu-id="b1e9b-293">Vous pouvez ajouter une origine avec un chemin d’accès relatif spécifique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-293">You can add an origin with a specific relative path.</span></span> <span data-ttu-id="b1e9b-294">Vous ne pouvez pas ajouter d’origine à l’aide du chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-294">You cannot add an origin using the full path.</span></span>

<span data-ttu-id="b1e9b-295">Cet exemple ajoute une origine privée de la bibliothèque éléments sur un site spécifique :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-295">This example adds a private origin of the siteassets library on a specific site:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl sites/site1/siteassets
```

<span data-ttu-id="b1e9b-296">Cet exemple ajoute une origine privée du dossier _dossier1_ dans la bibliothèque de sites de la collection de sites :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-296">This example adds a private origin of the _folder1_ folder in the site collection's site assets library:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl sites/test/siteassets/folder1
```

<span data-ttu-id="b1e9b-297">S’il y a un espace dans le chemin d’accès, vous pouvez placer le chemin d’accès entre guillemets ou remplacer l’espace par le codage d’URL %20.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-297">If there is a space in the path, you can either surround the path in double quotes or replace the space with the URL encoding %20.</span></span> <span data-ttu-id="b1e9b-298">Les exemples suivants ajoutent une origine privée du dossier _Folder 1_ dans la bibliothèque de sites de la collection de sites :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-298">The following examples add a private origin of the _folder 1_ folder in the site collection's site assets library:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl sites/test/siteassets/folder%201
```

``` powershell
Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl "sites/test/siteassets/folder 1"
```

<span data-ttu-id="b1e9b-299">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-299">For more information about this command and its syntax, see [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-300">Dans les origines privées, les biens partagés à partir d’une origine doivent avoir une version majeure publiée pour pouvoir être accessibles à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-300">In private origins, assets being shared from an origin must have a major version published before they can be accessed from the CDN.</span></span>
  
<span data-ttu-id="b1e9b-301">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-301">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-302">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-302">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-303"><a name="ExamplePublicOrigin"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-303"><a name="ExamplePublicOrigin"> </a></span></span>
### <a name="example-configure-a-public-origin-for-your-master-pages-and-for-your-style-library-for-sharepoint-online"></a><span data-ttu-id="b1e9b-304">Exemple : configurer une origine publique pour vos pages maîtres et pour votre bibliothèque de styles pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-304">Example: Configure a public origin for your master pages and for your style library for SharePoint Online</span></span>

<span data-ttu-id="b1e9b-305">Normalement, ces origines sont définies par défaut lorsque vous activez le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-305">Normally, these origins are set up for you by default when you enable the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-306">Toutefois, si vous souhaitez les activer manuellement, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-306">However, if you want to enable them manually, follow these steps.</span></span>
  
+ <span data-ttu-id="b1e9b-307">Utilisez l’applet de commande **Add-SPOTenantCdnOrigin** pour définir la bibliothèque de styles comme origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-307">Use the **Add-SPOTenantCdnOrigin** cmdlet to define the style library as a public origin.</span></span>

``` powershell
  Add-SPOTenantCdnOrigin -CdnType Public -OriginUrl */style%20library
  ```

+ <span data-ttu-id="b1e9b-308">Utilisez la cmdlet **Add-SPOTenantCdnOrigin** pour définir les pages maîtres comme une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-308">Use the **Add-SPOTenantCdnOrigin** cmdlet to define the master pages as a public origin.</span></span>

``` powershell
  Add-SPOTenantCdnOrigin -CdnType Public -OriginUrl */masterpage
  ```

<span data-ttu-id="b1e9b-309">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-309">For more information about this command and its syntax, see [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span></span>

<span data-ttu-id="b1e9b-310">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-310">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-311">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-311">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-312"><a name="ExamplePrivateOrigin"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-312"><a name="ExamplePrivateOrigin"> </a></span></span>
### <a name="example-configure-a-private-origin-for-your-site-assets-site-pages-and-publishing-images-for-sharepoint-online"></a><span data-ttu-id="b1e9b-313">Exemple : configurer une origine privée pour vos ressources de site, pages de site et images de publication pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-313">Example: Configure a private origin for your site assets, site pages, and publishing images for SharePoint Online</span></span>

+ <span data-ttu-id="b1e9b-314">Utilisez l’applet de commande **Add-SPOTenantCdnOrigin** pour définir le dossier des éléments de site comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-314">Use the **Add-SPOTenantCdnOrigin** cmdlet to define the site assets folder as a private origin.</span></span>

``` powershell
  Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl */siteassets
  ```

+ <span data-ttu-id="b1e9b-315">Utilisez l’applet de commande **Add-SPOTenantCdnOrigin** pour définir le dossier des pages de site comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-315">Use the **Add-SPOTenantCdnOrigin** cmdlet to define the site pages folder as a private origin.</span></span>

``` powershell
  Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl */sitepages
  ```

+ <span data-ttu-id="b1e9b-316">Utilisez l’applet de commande **Add-SPOTenantCdnOrigin** pour définir le dossier Publishing images comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-316">Use the **Add-SPOTenantCdnOrigin** cmdlet to define the publishing images folder as a private origin.</span></span>

``` powershell
  Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl */publishingimages
  ```

<span data-ttu-id="b1e9b-317">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-317">For more information about this command and its syntax, see [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span></span>

<span data-ttu-id="b1e9b-318">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-318">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-319">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-319">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-320"><a name="ExamplePrivateOriginSiteCollection"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-320"><a name="ExamplePrivateOriginSiteCollection"> </a></span></span>
### <a name="example-configure-a-private-origin-for-a-site-collection-for-sharepoint-online"></a><span data-ttu-id="b1e9b-321">Exemple : configurer une origine privée pour une collection de sites pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-321">Example: Configure a private origin for a site collection for SharePoint Online</span></span>

<span data-ttu-id="b1e9b-322">La cmdlet **Add-SPOTenantCdnOrigin** permet de définir une collection de sites en tant qu’origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-322">Use the **Add-SPOTenantCdnOrigin** cmdlet to define a site collection as a private origin.</span></span> <span data-ttu-id="b1e9b-323">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-323">For example:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Private -OriginUrl sites/site1/siteassets
```

<span data-ttu-id="b1e9b-324">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-324">For more information about this command and its syntax, see [Add-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790772.aspx).</span></span>
  
<span data-ttu-id="b1e9b-325">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-325">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-326">Il se peut que vous rencontriez un message de _configuration en attente_ qui est attendu lorsque le client SharePoint Online se connecte au service CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-326">You may see a _Configuration pending_ message which is expected as the SharePoint Online tenant connects to the CDN service.</span></span> <span data-ttu-id="b1e9b-327">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-327">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-328"><a name="CDNManage"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-328"><a name="CDNManage"> </a></span></span>
### <a name="manage-the-office-365-cdn"></a><span data-ttu-id="b1e9b-329">Gérer le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-329">Manage the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-330">Une fois que vous avez configuré le CDN, vous pouvez modifier votre configuration lors de la mise à jour du contenu ou à mesure que vos besoins changent, comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-330">Once you've set up the CDN, you can make changes to your configuration as you update content or as your needs change, as described in this section.</span></span>
  
<span data-ttu-id="b1e9b-331"><a name="Office365CDNforSPOaddremoveasset"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-331"><a name="Office365CDNforSPOaddremoveasset"> </a></span></span>
#### <a name="add-update-or-remove-assets-from-the-office-365-cdn"></a><span data-ttu-id="b1e9b-332">Ajouter, mettre à jour ou supprimer des ressources du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-332">Add, update, or remove assets from the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-333">Une fois que vous avez terminé les étapes de configuration, vous pouvez ajouter de nouvelles ressources, ainsi que mettre à jour ou supprimer des biens existants chaque fois que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-333">Once you've completed the setup steps, you can add new assets, and update or remove existing assets whenever you want.</span></span> <span data-ttu-id="b1e9b-334">Modifiez simplement les ressources dans le dossier ou la bibliothèque SharePoint que vous avez identifiée comme origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-334">Just make your changes to the assets in the folder or SharePoint library that you identified as an origin.</span></span> <span data-ttu-id="b1e9b-335">Si vous ajoutez une nouvelle ressource, elle est immédiatement disponible via le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-335">If you add a new asset, it is available through the CDN immediately.</span></span> <span data-ttu-id="b1e9b-336">Toutefois, si vous mettez à jour l’élément, la propagation de la nouvelle copie peut prendre jusqu’à 15 minutes et devenir disponible dans le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-336">However, if you update the asset, it will take up to 15 minutes for the new copy to propagate and become available in the CDN.</span></span>
  
<span data-ttu-id="b1e9b-337">Si vous avez besoin de récupérer l’emplacement de l’origine, vous pouvez utiliser la cmdlet **Get-SPOTenantCdnOrigins** .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-337">If you need to retrieve the location of the origin, you can use the **Get-SPOTenantCdnOrigins** cmdlet.</span></span> <span data-ttu-id="b1e9b-338">Pour plus d’informations sur l’utilisation de cette cmdlet, consultez la rubrique [Get-SPOTenantCdnOrigins](https://technet.microsoft.com/library/mt790770.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-338">For information on how to use this cmdlet, see [Get-SPOTenantCdnOrigins](https://technet.microsoft.com/library/mt790770.aspx).</span></span>

<span data-ttu-id="b1e9b-339"><a name="Office365CDNforSPORemoveOriginPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-339"><a name="Office365CDNforSPORemoveOriginPosh"> </a></span></span>
#### <a name="remove-an-origin-from-the-office-365-cdn"></a><span data-ttu-id="b1e9b-340">Supprimer une origine du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-340">Remove an origin from the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-341">Vous pouvez supprimer l’accès à un dossier ou à une bibliothèque SharePoint que vous avez identifiée comme origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-341">You can remove access to a folder or SharePoint library that you identified as an origin.</span></span> <span data-ttu-id="b1e9b-342">Pour ce faire, utilisez la cmdlet **Remove-SPOTenantCdnOrigin** .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-342">To do this, use the **Remove-SPOTenantCdnOrigin** cmdlet.</span></span>

``` powershell
Remove-SPOTenantCdnOrigin -OriginUrl <path> -CdnType <Public | Private | Both>
```

<span data-ttu-id="b1e9b-343">Pour plus d’informations sur l’utilisation de cette cmdlet, consultez la rubrique [Remove-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790761.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-343">For information on how to use this cmdlet, see [Remove-SPOTenantCdnOrigin](https://technet.microsoft.com/library/mt790761.aspx).</span></span>

<span data-ttu-id="b1e9b-344"><a name="Office365CDNforSPOModifyOrigin"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-344"><a name="Office365CDNforSPOModifyOrigin"> </a></span></span>
#### <a name="modify-an-origin-in-the-office-365-cdn"></a><span data-ttu-id="b1e9b-345">Modifier une origine dans le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-345">Modify an origin in the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-346">Vous ne pouvez pas modifier une origine que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-346">You cannot modify an origin you've created.</span></span> <span data-ttu-id="b1e9b-347">Au lieu de cela, supprimez l’origine, puis ajoutez-en une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-347">Instead, remove the origin and then add a new one.</span></span> <span data-ttu-id="b1e9b-348">Pour plus d’informations, reportez-vous [à la rubrique pour supprimer une origine du CDN Office 365](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPORemoveOriginPosh) et [Ajouter une origine pour vos biens](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPOOriginPosh).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-348">For more information, see [To remove an origin from the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPORemoveOriginPosh) and [To add an origin for your assets](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPOOriginPosh).</span></span>

<span data-ttu-id="b1e9b-349"><a name="Office365CDNforSPODisable"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-349"><a name="Office365CDNforSPODisable"> </a></span></span>
#### <a name="disable-the-office-365-cdn"></a><span data-ttu-id="b1e9b-350">Désactiver le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-350">Disable the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-351">La cmdlet **Set-SPOTenantCdnEnabled** permet de désactiver le CDN pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-351">Use the **Set-SPOTenantCdnEnabled** cmdlet to disable the CDN for your organization.</span></span> <span data-ttu-id="b1e9b-352">Si vous avez à la fois les origines publique et privée activées pour le CDN, vous devez exécuter l’applet de commande deux fois, comme illustré dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-352">If you have both the public and private origins enabled for the CDN, you need to run the cmdlet twice as shown in the following examples.</span></span>
  
<span data-ttu-id="b1e9b-353">Pour désactiver l’utilisation des origines publiques dans le CDN, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-353">To disable use of public origins in the CDN, enter the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Public -Enable $false
```

<span data-ttu-id="b1e9b-354">Pour désactiver l’utilisation des origines privées dans le CDN, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-354">To disable use of the private origins in the CDN, enter the following command:</span></span>

``` powershell
Set-SPOTenantCdnEnabled -CdnType Private -Enable $false
```

<span data-ttu-id="b1e9b-355">Pour plus d’informations sur cette cmdlet, consultez la rubrique [Set-SPOTenantCdnEnabled](https://technet.microsoft.com/library/mt790765.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-355">For more information about this cmdlet, see [Set-SPOTenantCdnEnabled](https://technet.microsoft.com/library/mt790765.aspx).</span></span>

</details>

<span data-ttu-id="b1e9b-356"><a name="CDNSetupinPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-356"><a name="CDNSetupinPnPPosh"> </a></span></span>
## <a name="set-up-and-configure-the-office-365-cdn-by-using-pnp-powershell"></a><span data-ttu-id="b1e9b-357">Installer et configurer le CDN Office 365 à l’aide de PowerShell PnP</span><span class="sxs-lookup"><span data-stu-id="b1e9b-357">Set up and configure the Office 365 CDN by using PnP PowerShell</span></span>

<span data-ttu-id="b1e9b-358">Les procédures décrites dans cette section nécessitent l’utilisation de PowerShell PnP pour se connecter à SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-358">The procedures in this section require you to use PnP PowerShell to connect to SharePoint Online.</span></span> <span data-ttu-id="b1e9b-359">Pour obtenir des instructions, consultez la rubrique [prise en main de PowerShell PNP](https://github.com/SharePoint/PnP-PowerShell#getting-started).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-359">For instructions, see [Getting started with PnP PowerShell](https://github.com/SharePoint/PnP-PowerShell#getting-started).</span></span>

<span data-ttu-id="b1e9b-360">Procédez comme suit pour installer et configurer le CDN afin d’héberger vos ressources dans SharePoint Online à l’aide de PowerShell PnP.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-360">Complete these steps to set up and configure the CDN to host your assets in SharePoint Online using PnP PowerShell.</span></span>

<details>
  <summary><span data-ttu-id="b1e9b-361">Cliquez pour développer</span><span class="sxs-lookup"><span data-stu-id="b1e9b-361">Click to expand</span></span></summary>

### <a name="enable-your-organization-to-use-the-office-365-cdn"></a><span data-ttu-id="b1e9b-362">Permettre à votre organisation d’utiliser le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-362">Enable your organization to use the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-363">Avant de modifier les paramètres de CDN de client, vous devez récupérer l’état actuel de la configuration de CDN privé dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-363">Before you make changes to the tenant CDN settings, you should retrieve the current status of the private CDN configuration in your Office 365 tenant.</span></span> <span data-ttu-id="b1e9b-364">Connectez-vous à votre client à l’aide de PowerShell PnP :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-364">Connect to your tenant using PnP PowerShell:</span></span>

``` powershell
Connect-PnPOnline -Url https://contoso-admin.sharepoint.com -UseWebLogin
```

<span data-ttu-id="b1e9b-365">À présent, utilisez la cmdlet **Get-PnPTenantCdnEnabled** pour récupérer les paramètres d’État CDN à partir du client :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-365">Now use the **Get-PnPTenantCdnEnabled** cmdlet to retrieve the CDN status settings from the tenant:</span></span>

``` powershell
Get-PnPTenantCdnEnabled -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-366">L’état du CDN pour le CdnType spécifié s’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-366">The status of the CDN for the specified CdnType will output to the screen.</span></span>

<span data-ttu-id="b1e9b-367">Utilisez l’applet de commande **Set-PnPTenantCdnEnabled** pour permettre à votre organisation d’utiliser le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-367">Use the **Set-PnPTenantCdnEnabled** cmdlet to enable your organization to use the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-368">Vous pouvez permettre à votre organisation d’utiliser des origines publiques, des origines privées ou les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-368">You can enable your organization to use public origins, private origins, or both at at the same time.</span></span> <span data-ttu-id="b1e9b-369">Vous pouvez également configurer le CDN de sorte qu’il ignore le paramétrage des origines par défaut lorsque vous l’activez.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-369">You can also configure the CDN to skip the setup of default origins when you enable it.</span></span> <span data-ttu-id="b1e9b-370">Vous pouvez toujours ajouter ces origines plus tard, comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-370">You can always add these origins later as described in this topic.</span></span>
  
<span data-ttu-id="b1e9b-371">Dans PowerShell PnP :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-371">In PnP PowerShell:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType <Public | Private | Both> -Enable $true
```

<span data-ttu-id="b1e9b-372">Par exemple, pour permettre à votre organisation d’utiliser des origines publiques et privées, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-372">For example, to enable your organization to use both public and private origins, type the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Both -Enable $true
```

<span data-ttu-id="b1e9b-373">Pour permettre à votre organisation d’utiliser des origines publiques et privées, mais de ne pas configurer les origines par défaut, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-373">To enable your organization to use both public and private origins but skip setting up the default origins, type the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Both -Enable $true -NoDefaultOrigins
```

<span data-ttu-id="b1e9b-374">Consultez la rubrique [origines du CDN par défaut](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) pour obtenir des informations sur les origines qui sont configurées par défaut lorsque vous activez le CDN Office 365, ainsi que l’impact potentiel de l’omission de la configuration des origines par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-374">See [Default CDN origins](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) for information about the origins that are provisioned by default when you enable the Office 365 CDN, and the potential impact of skipping the setup of default origins.</span></span>

<span data-ttu-id="b1e9b-375">Pour permettre à votre organisation d’utiliser des origines publiques, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-375">To enable your organization to use public origins, type the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Public -Enable $true
```

<span data-ttu-id="b1e9b-376">Pour permettre à votre organisation d’utiliser des origines privées, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-376">To enable your organization to use private origins, type the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Private -Enable $true
```

<span data-ttu-id="b1e9b-377">Pour plus d’informations sur cette cmdlet, consultez la rubrique [Set-PnPTenantCdnEnabled](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnenabled).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-377">For more information about this cmdlet, see [Set-PnPTenantCdnEnabled](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnenabled).</span></span>

<span data-ttu-id="b1e9b-378"><a name="Office365CDNforPnPPoshFileType"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-378"><a name="Office365CDNforPnPPoshFileType"> </a></span></span>
### <a name="change-the-list-of-file-types-to-include-in-the-office-365-cdn-optional"></a><span data-ttu-id="b1e9b-379">Modifier la liste des types de fichiers à inclure dans le CDN Office 365 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b1e9b-379">Change the list of file types to include in the Office 365 CDN (Optional)</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-380">Lorsque vous définissez des types de fichiers à l’aide de la cmdlet **Set-PnPTenantCdnPolicy** , vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-380">When you define file types by using the **Set-PnPTenantCdnPolicy** cmdlet, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-381">Si vous souhaitez ajouter d’autres types de fichiers à la liste, utilisez d’abord la cmdlet pour savoir quels types de fichiers sont déjà autorisés et les inclure dans la liste en même temps que les nouveaux.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-381">If you want to add additional file types to the list, use the cmdlet first to find out what file types are already allowed and include them in the list along with your new ones.</span></span>
  
<span data-ttu-id="b1e9b-382">La cmdlet **Set-PnPTenantCdnPolicy** permet de définir des types de fichiers statiques qui peuvent être hébergés par des origines publiques et privées dans le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-382">Use the **Set-PnPTenantCdnPolicy** cmdlet to define static file types that can be hosted by public and private origins in the CDN.</span></span> <span data-ttu-id="b1e9b-383">Par défaut, les types d’éléments communs sont autorisés, par exemple. CSS,. gif,. jpg et. js.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-383">By default, common asset types are allowed, for example .css, .gif, .jpg, and .js.</span></span>

<span data-ttu-id="b1e9b-384">Dans PowerShell PnP :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-384">In PnP PowerShell:</span></span>

``` powershell
Set-PnPTenantCdnPolicy -CdnType <Public | Private> -PolicyType IncludeFileExtensions -PolicyValue "<Comma-separated list of file types >"
```

<span data-ttu-id="b1e9b-385">Par exemple, pour permettre au CDN d’héberger des fichiers. CSS et. png, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-385">For example, to enable the CDN to host .css and .png files, you would enter the command:</span></span>

``` powershell
Set-PnPTenantCdnPolicy -CdnType Private -PolicyType IncludeFileExtensions -PolicyValue "CSS,PNG"
```

<span data-ttu-id="b1e9b-386">Pour voir les types de fichiers actuellement autorisés par le CDN, utilisez la cmdlet **Get-PnPTenantCdnPolicies** :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-386">To see what file types are currently allowed by the CDN, use the **Get-PnPTenantCdnPolicies** cmdlet:</span></span>

``` powershell
Get-PnPTenantCdnPolicies -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-387">Pour plus d’informations sur ces applets de commande, voir [Set-PnPTenantCdnPolicy](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnpolicy) et [Get-PnPTenantCdnPolicies](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnpolicies).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-387">For more information about these cmdlets, see [Set-PnPTenantCdnPolicy](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnpolicy) and [Get-PnPTenantCdnPolicies](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnpolicies).</span></span>

<span data-ttu-id="b1e9b-388"><a name="Office365CDNforPnPPoshSiteClassification"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-388"><a name="Office365CDNforPnPPoshSiteClassification"> </a></span></span>
### <a name="change-the-list-of-site-classifications-you-want-to-exclude-from-the-office-365-cdn-optional"></a><span data-ttu-id="b1e9b-389">Modifier la liste des classifications de sites que vous souhaitez exclure du CDN Office 365 (facultatif)</span><span class="sxs-lookup"><span data-stu-id="b1e9b-389">Change the list of site classifications you want to exclude from the Office 365 CDN (Optional)</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-390">Lorsque vous excluez les classifications de site à l’aide de la cmdlet **Set-PnPTenantCdnPolicy** , vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-390">When you exclude site classifications by using the **Set-PnPTenantCdnPolicy** cmdlet, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-391">Si vous souhaitez exclure des classifications de site supplémentaires, utilisez d’abord la cmdlet pour savoir quelles classifications sont déjà exclues, puis ajoutez-les en même temps que les nouvelles classifications.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-391">If you want to exclude additional site classifications, use the cmdlet first to find out what classifications are already excluded and then add them along with your new ones.</span></span>

<span data-ttu-id="b1e9b-392">Utilisez la cmdlet **Set-PnPTenantCdnPolicy** pour exclure les classifications de site que vous ne souhaitez pas mettre à disposition sur le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-392">Use the **Set-PnPTenantCdnPolicy** cmdlet to exclude site classifications that you do not want to make available over the CDN.</span></span> <span data-ttu-id="b1e9b-393">Par défaut, aucune classification de site n’est exclue.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-393">By default, no site classifications are excluded.</span></span>

<span data-ttu-id="b1e9b-394">Dans PowerShell PnP :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-394">In PnP PowerShell:</span></span>

``` powershell
Set-PnPTenantCdnPolicy -CdnType <Public | Private> -PolicyType ExcludeRestrictedSiteClassifications  -PolicyValue "<Comma-separated list of site classifications>"
```

<span data-ttu-id="b1e9b-395">Pour voir les classifications de site actuellement restreintes, utilisez la cmdlet **Get-PnPTenantCdnPolicies** :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-395">To see what site classifications are currently restricted, use the **Get-PnPTenantCdnPolicies** cmdlet:</span></span>

``` powershell
Get-PnPTenantCdnPolicies -CdnType <Public | Private>
```

<span data-ttu-id="b1e9b-396">Les propriétés qui seront renvoyées sont _IncludeFileExtensions_, _ExcludeRestrictedSiteClassifications_ et _ExcludeIfNoScriptDisabled_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-396">The properties that will be returned are _IncludeFileExtensions_, _ExcludeRestrictedSiteClassifications_ and _ExcludeIfNoScriptDisabled_.</span></span>

<span data-ttu-id="b1e9b-397">La propriété _IncludeFileExtensions_ contient la liste des extensions de fichiers qui seront fournies à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-397">The _IncludeFileExtensions_ property contains the list of file extensions that will be served from the CDN.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-398">Les extensions de fichier par défaut sont différentes entre public et Private.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-398">The default file extensions are different between public and private.</span></span>

<span data-ttu-id="b1e9b-399">La propriété _ExcludeRestrictedSiteClassifications_ contient les classifications de site que vous souhaitez exclure du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-399">The _ExcludeRestrictedSiteClassifications_ property contains the site classifications that you want to exclude from the CDN.</span></span> <span data-ttu-id="b1e9b-400">Par exemple, vous pouvez exclure des sites marqués comme **confidentiels** de sorte que le contenu de sites avec cette classification appliquée ne sera pas pris en charge par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-400">For example, you can exclude sites marked as **Confidential** so content from sites with that classification applied will not be served from the CDN.</span></span>

<span data-ttu-id="b1e9b-401">La propriété _ExcludeIfNoScriptDisabled_ exclut le contenu du CDN en fonction des paramètres d’attribut _NoScript_ au niveau du site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-401">The _ExcludeIfNoScriptDisabled_ property excludes content from the CDN based on the site-level _NoScript_ attribute settings.</span></span> <span data-ttu-id="b1e9b-402">Par défaut, l’attribut _NoScript_ est défini sur **activé** pour les sites _modernes_ et **désactivé** pour les sites _classiques_ .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-402">By default, the _NoScript_ attribute is set to **Enabled** for _Modern_ sites and **Disabled** for _Classic_ sites.</span></span> <span data-ttu-id="b1e9b-403">Cela dépend de vos paramètres de client.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-403">This depends on your tenant settings.</span></span>

<span data-ttu-id="b1e9b-404">Pour plus d’informations sur ces applets de commande, voir [Set-PnPTenantCdnPolicy](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnpolicy) et [Get-PnPTenantCdnPolicies](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnpolicies).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-404">For more information about these cmdlets, see [Set-PnPTenantCdnPolicy](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnpolicy) and [Get-PnPTenantCdnPolicies](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnpolicies).</span></span>

<span data-ttu-id="b1e9b-405"><a name="Office365CDNforSPOOriginPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-405"><a name="Office365CDNforSPOOriginPnPPosh"> </a></span></span>
### <a name="add-an-origin-for-your-assets"></a><span data-ttu-id="b1e9b-406">Ajouter une origine pour vos biens</span><span class="sxs-lookup"><span data-stu-id="b1e9b-406">Add an origin for your assets</span></span>

<span data-ttu-id="b1e9b-407">Utilisez l’applet de commande **Add-PnPTenantCdnOrigin** pour définir une origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-407">Use the **Add-PnPTenantCdnOrigin** cmdlet to define an origin.</span></span> <span data-ttu-id="b1e9b-408">Vous pouvez définir plusieurs origines.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-408">You can define multiple origins.</span></span> <span data-ttu-id="b1e9b-409">L’origine est une URL pointant vers un dossier ou une bibliothèque SharePoint qui contient les ressources qui doivent être hébergées par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-409">The origin is a URL that points to a SharePoint library or folder that contains the assets that you want to be hosted by the CDN.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b1e9b-410">Vous ne devez jamais placer de ressources qui contiennent des informations utilisateur ou qui sont considérées comme sensibles à votre organisation dans une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-410">You should never place resources that contain user information or are considered sensitive to your organization in a public origin.</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType <Public | Private> -OriginUrl <path>
```

<span data-ttu-id="b1e9b-411">La valeur _path_ est le chemin d’accès relatif à la bibliothèque ou au dossier qui contient les composants.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-411">The value of _path_ is the relative path to the library or folder that contains the assets.</span></span> <span data-ttu-id="b1e9b-412">Vous pouvez utiliser des caractères génériques en plus des chemins d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-412">You can use wildcards in addition to relative paths.</span></span> <span data-ttu-id="b1e9b-413">Les origines prennent en charge les caractères génériques ajoutés à l’URL.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-413">Origins support wildcards prepended to the URL.</span></span> <span data-ttu-id="b1e9b-414">Cela vous permet de créer des origines qui s’étendent sur plusieurs sites.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-414">This allows you to create origins that span multiple sites.</span></span> <span data-ttu-id="b1e9b-415">Par exemple, pour inclure toutes les ressources dans le dossier MasterPages pour tous vos sites en tant qu’origine publique dans le CDN, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-415">For example, to include all of the assets in the masterpages folder for all of your sites as a public origin within the CDN, type the following command:</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType Public -OriginUrl */masterpage
```

+ <span data-ttu-id="b1e9b-416">Le modificateur de caractère générique \* **/** peut uniquement être utilisé au début du chemin d’accès et correspondra à tous les segments d’URL sous l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-416">The wildcard modifier \***/** can only be used at the beginning of the path, and will match all URL segments under the specified URL.</span></span>
+ <span data-ttu-id="b1e9b-417">Le chemin d’accès peut pointer vers une bibliothèque de documents, un dossier ou un site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-417">The path can point to a document library, folder or site.</span></span> <span data-ttu-id="b1e9b-418">Par exemple, le chemin d’accès _\*/site1_ correspondra à toutes les bibliothèques de documents sous le site.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-418">For example, the path _\*/site1_ will match all the document libraries under the site.</span></span>

<span data-ttu-id="b1e9b-419">Vous pouvez ajouter une origine avec un chemin d’accès relatif spécifique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-419">You can add an origin with a specific relative path.</span></span> <span data-ttu-id="b1e9b-420">Vous ne pouvez pas ajouter d’origine à l’aide du chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-420">You cannot add an origin using the full path.</span></span>

<span data-ttu-id="b1e9b-421">Cet exemple ajoute une origine privée de la bibliothèque d’éléments de site sur un site spécifique :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-421">This example adds a private origin of the site assets library on a specific site:</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl sites/site1/siteassets
```

<span data-ttu-id="b1e9b-422">Cet exemple ajoute une origine privée du dossier _dossier1_ dans la bibliothèque de sites de la collection de sites :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-422">This example adds a private origin of the _folder1_ folder in the site collection's site assets library:</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl sites/test/siteassets/folder1
```

<span data-ttu-id="b1e9b-423">S’il y a un espace dans le chemin d’accès, vous pouvez placer le chemin d’accès entre guillemets ou remplacer l’espace par le codage d’URL %20.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-423">If there is a space in the path, you can either surround the path in double quotes or replace the space with the URL encoding %20.</span></span> <span data-ttu-id="b1e9b-424">Les exemples suivants ajoutent une origine privée du dossier _Folder 1_ dans la bibliothèque de sites de la collection de sites :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-424">The following examples add a private origin of the _folder 1_ folder in the site collection's site assets library:</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl sites/test/siteassets/folder%201
```

``` powershell
Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl "sites/test/siteassets/folder 1"
```

<span data-ttu-id="b1e9b-425">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-425">For more information about this command and its syntax, see [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-426">Dans les origines privées, les biens partagés à partir d’une origine doivent avoir une version majeure publiée pour pouvoir être accessibles à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-426">In private origins, assets being shared from an origin must have a major version published before they can be accessed from the CDN.</span></span>
  
<span data-ttu-id="b1e9b-427">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-427">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-428">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-428">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-429"><a name="ExamplePublicOriginPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-429"><a name="ExamplePublicOriginPnPPosh"> </a></span></span>
### <a name="example-configure-a-public-origin-for-your-master-pages-and-for-your-style-library-for-sharepoint-online"></a><span data-ttu-id="b1e9b-430">Exemple : configurer une origine publique pour vos pages maîtres et pour votre bibliothèque de styles pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-430">Example: Configure a public origin for your master pages and for your style library for SharePoint Online</span></span>

<span data-ttu-id="b1e9b-431">Normalement, ces origines sont définies par défaut lorsque vous activez le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-431">Normally, these origins are set up for you by default when you enable the Office 365 CDN.</span></span> <span data-ttu-id="b1e9b-432">Toutefois, si vous souhaitez les activer manuellement, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-432">However, if you want to enable them manually, follow these steps.</span></span>
  
+ <span data-ttu-id="b1e9b-433">Utilisez l’applet de commande **Add-PnPTenantCdnOrigin** pour définir la bibliothèque de styles comme origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-433">Use the **Add-PnPTenantCdnOrigin** cmdlet to define the style library as a public origin.</span></span>

``` powershell
  Add-PnPTenantCdnOrigin -CdnType Public -OriginUrl */style%20library
  ```

+ <span data-ttu-id="b1e9b-434">Utilisez la cmdlet **Add-PnPTenantCdnOrigin** pour définir les pages maîtres comme une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-434">Use the **Add-PnPTenantCdnOrigin** cmdlet to define the master pages as a public origin.</span></span>

``` powershell
  Add-PnPTenantCdnOrigin -CdnType Public -OriginUrl */masterpage
  ```

<span data-ttu-id="b1e9b-435">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-435">For more information about this command and its syntax, see [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span></span>

<span data-ttu-id="b1e9b-436">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-436">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-437">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-437">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-438"><a name="ExamplePrivateOriginPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-438"><a name="ExamplePrivateOriginPnPPosh"> </a></span></span>
### <a name="example-configure-a-private-origin-for-your-site-assets-site-pages-and-publishing-images-for-sharepoint-online"></a><span data-ttu-id="b1e9b-439">Exemple : configurer une origine privée pour vos ressources de site, pages de site et images de publication pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-439">Example: Configure a private origin for your site assets, site pages, and publishing images for SharePoint Online</span></span>

+ <span data-ttu-id="b1e9b-440">Utilisez l’applet de commande **Add-PnPTenantCdnOrigin** pour définir le dossier des éléments de site comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-440">Use the **Add-PnPTenantCdnOrigin** cmdlet to define the site assets folder as a private origin.</span></span>

``` powershell
  Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl */siteassets
  ```

+ <span data-ttu-id="b1e9b-441">Utilisez l’applet de commande **Add-PnPTenantCdnOrigin** pour définir le dossier des pages de site comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-441">Use the **Add-PnPTenantCdnOrigin** cmdlet to define the site pages folder as a private origin.</span></span>

``` powershell
  Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl */sitepages
  ```

+ <span data-ttu-id="b1e9b-442">Utilisez l’applet de commande **Add-PnPTenantCdnOrigin** pour définir le dossier Publishing images comme origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-442">Use the **Add-PnPTenantCdnOrigin** cmdlet to define the publishing images folder as a private origin.</span></span>

``` powershell
  Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl */publishingimages
  ```

<span data-ttu-id="b1e9b-443">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-443">For more information about this command and its syntax, see [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span></span>

<span data-ttu-id="b1e9b-444">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-444">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-445">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-445">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-446"><a name="ExamplePrivateOriginSiteCollectionPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-446"><a name="ExamplePrivateOriginSiteCollectionPnPPosh"> </a></span></span>
### <a name="example-configure-a-private-origin-for-a-site-collection-for-sharepoint-online"></a><span data-ttu-id="b1e9b-447">Exemple : configurer une origine privée pour une collection de sites pour SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-447">Example: Configure a private origin for a site collection for SharePoint Online</span></span>

<span data-ttu-id="b1e9b-448">La cmdlet **Add-PnPTenantCdnOrigin** permet de définir une collection de sites en tant qu’origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-448">Use the **Add-PnPTenantCdnOrigin** cmdlet to define a site collection as a private origin.</span></span> <span data-ttu-id="b1e9b-449">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-449">For example:</span></span>

``` powershell
Add-PnPTenantCdnOrigin -CdnType Private -OriginUrl sites/site1/siteassets
```

<span data-ttu-id="b1e9b-450">Pour plus d’informations sur cette commande et sa syntaxe, voir [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-450">For more information about this command and its syntax, see [Add-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/add-pnptenantcdnorigin).</span></span>
  
<span data-ttu-id="b1e9b-451">Une fois que vous avez exécuté la commande, le système synchronise la configuration dans le centre de l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-451">Once you've run the command, the system synchronizes the configuration across the datacenter.</span></span> <span data-ttu-id="b1e9b-452">Il se peut que vous rencontriez un message de _configuration en attente_ qui est attendu lorsque le client SharePoint Online se connecte au service CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-452">You may see a _Configuration pending_ message which is expected as the SharePoint Online tenant connects to the CDN service.</span></span> <span data-ttu-id="b1e9b-453">Cela peut prendre jusqu’à 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-453">This can take up to 15 minutes.</span></span>

<span data-ttu-id="b1e9b-454"><a name="CDNManagePnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-454"><a name="CDNManagePnPPosh"> </a></span></span>
### <a name="manage-the-office-365-cdn"></a><span data-ttu-id="b1e9b-455">Gérer le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-455">Manage the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-456">Une fois que vous avez configuré le CDN, vous pouvez modifier votre configuration lors de la mise à jour du contenu ou à mesure que vos besoins changent, comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-456">Once you've set up the CDN, you can make changes to your configuration as you update content or as your needs change, as described in this section.</span></span>
  
<span data-ttu-id="b1e9b-457"><a name="Office365CDNforSPOaddremoveassetPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-457"><a name="Office365CDNforSPOaddremoveassetPnPPosh"> </a></span></span>
#### <a name="add-update-or-remove-assets-from-the-office-365-cdn"></a><span data-ttu-id="b1e9b-458">Ajouter, mettre à jour ou supprimer des ressources du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-458">Add, update, or remove assets from the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-459">Une fois que vous avez terminé les étapes de configuration, vous pouvez ajouter de nouvelles ressources, ainsi que mettre à jour ou supprimer des biens existants chaque fois que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-459">Once you've completed the setup steps, you can add new assets, and update or remove existing assets whenever you want.</span></span> <span data-ttu-id="b1e9b-460">Modifiez simplement les ressources dans le dossier ou la bibliothèque SharePoint que vous avez identifiée comme origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-460">Just make your changes to the assets in the folder or SharePoint library that you identified as an origin.</span></span> <span data-ttu-id="b1e9b-461">Si vous ajoutez une nouvelle ressource, elle est immédiatement disponible via le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-461">If you add a new asset, it is available through the CDN immediately.</span></span> <span data-ttu-id="b1e9b-462">Toutefois, si vous mettez à jour l’élément, la propagation de la nouvelle copie peut prendre jusqu’à 15 minutes et devenir disponible dans le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-462">However, if you update the asset, it will take up to 15 minutes for the new copy to propagate and become available in the CDN.</span></span>
  
<span data-ttu-id="b1e9b-463">Si vous avez besoin de récupérer l’emplacement de l’origine, vous pouvez utiliser la cmdlet **Get-PnPTenantCdnOrigin** .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-463">If you need to retrieve the location of the origin, you can use the **Get-PnPTenantCdnOrigin** cmdlet.</span></span> <span data-ttu-id="b1e9b-464">Pour plus d’informations sur l’utilisation de cette cmdlet, consultez la rubrique [Get-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-464">For information on how to use this cmdlet, see [Get-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnptenantcdnorigin).</span></span>

<span data-ttu-id="b1e9b-465"><a name="Office365CDNforSPORemoveOriginPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-465"><a name="Office365CDNforSPORemoveOriginPnPPosh"> </a></span></span>
#### <a name="remove-an-origin-from-the-office-365-cdn"></a><span data-ttu-id="b1e9b-466">Supprimer une origine du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-466">Remove an origin from the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-467">Vous pouvez supprimer l’accès à un dossier ou à une bibliothèque SharePoint que vous avez identifiée comme origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-467">You can remove access to a folder or SharePoint library that you identified as an origin.</span></span> <span data-ttu-id="b1e9b-468">Pour ce faire, utilisez la cmdlet **Remove-PnPTenantCdnOrigin** .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-468">To do this, use the **Remove-PnPTenantCdnOrigin** cmdlet.</span></span>

``` powershell
Remove-PnPTenantCdnOrigin -OriginUrl <path> -CdnType <Public | Private | Both>
```

<span data-ttu-id="b1e9b-469">Pour plus d’informations sur l’utilisation de cette cmdlet, consultez la rubrique [Remove-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/remove-pnptenantcdnorigin).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-469">For information on how to use this cmdlet, see [Remove-PnPTenantCdnOrigin](https://docs.microsoft.com/powershell/module/sharepoint-pnp/remove-pnptenantcdnorigin).</span></span>

<span data-ttu-id="b1e9b-470"><a name="Office365CDNforSPOModifyOriginPnPPosh"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-470"><a name="Office365CDNforSPOModifyOriginPnPPosh"> </a></span></span>
#### <a name="modify-an-origin-in-the-office-365-cdn"></a><span data-ttu-id="b1e9b-471">Modifier une origine dans le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-471">Modify an origin in the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-472">Vous ne pouvez pas modifier une origine que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-472">You cannot modify an origin you've created.</span></span> <span data-ttu-id="b1e9b-473">Au lieu de cela, supprimez l’origine, puis ajoutez-en une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-473">Instead, remove the origin and then add a new one.</span></span> <span data-ttu-id="b1e9b-474">Pour plus d’informations, reportez-vous [à la rubrique pour supprimer une origine du CDN Office 365](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPORemoveOriginPnPPosh) et [Ajouter une origine pour vos biens](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPOOriginPnPPosh).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-474">For more information, see [To remove an origin from the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPORemoveOriginPnPPosh) and [To add an origin for your assets](use-microsoft-365-cdn-with-spo.md#Office365CDNforSPOOriginPnPPosh).</span></span>

<span data-ttu-id="b1e9b-475"><a name="Office365CDNforSPODisable"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-475"><a name="Office365CDNforSPODisable"> </a></span></span>
#### <a name="disable-the-office-365-cdn"></a><span data-ttu-id="b1e9b-476">Désactiver le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-476">Disable the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-477">La cmdlet **Set-PnPTenantCdnEnabled** permet de désactiver le CDN pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-477">Use the **Set-PnPTenantCdnEnabled** cmdlet to disable the CDN for your organization.</span></span> <span data-ttu-id="b1e9b-478">Si vous avez à la fois les origines publique et privée activées pour le CDN, vous devez exécuter l’applet de commande deux fois, comme illustré dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-478">If you have both the public and private origins enabled for the CDN, you need to run the cmdlet twice as shown in the following examples.</span></span>
  
<span data-ttu-id="b1e9b-479">Pour désactiver l’utilisation des origines publiques dans le CDN, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-479">To disable use of public origins in the CDN, enter the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Public -Enable $false
```

<span data-ttu-id="b1e9b-480">Pour désactiver l’utilisation des origines privées dans le CDN, entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-480">To disable use of the private origins in the CDN, enter the following command:</span></span>

``` powershell
Set-PnPTenantCdnEnabled -CdnType Private -Enable $false
```

<span data-ttu-id="b1e9b-481">Pour plus d’informations sur cette cmdlet, consultez la rubrique [Set-PnPTenantCdnEnabled](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnenabled).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-481">For more information about this cmdlet, see [Set-PnPTenantCdnEnabled](https://docs.microsoft.com/powershell/module/sharepoint-pnp/set-pnptenantcdnenabled).</span></span>

</details>

<span data-ttu-id="b1e9b-482"><a name="CDNSetupinCLI"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-482"><a name="CDNSetupinCLI"> </a></span></span>
## <a name="set-up-and-configure-the-office-365-cdn-using-the-office-365-cli"></a><span data-ttu-id="b1e9b-483">Installation et configuration du CDN Office 365 à l’aide de la CLI Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-483">Set up and configure the Office 365 CDN using the Office 365 CLI</span></span>

<span data-ttu-id="b1e9b-484">Les procédures décrites dans cette section nécessitent l’installation de l' [interface CLI Office 365](https://aka.ms/o365cli).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-484">The procedures in this section require that you have installed the [Office 365 CLI](https://aka.ms/o365cli).</span></span> <span data-ttu-id="b1e9b-485">Ensuite, connectez-vous à votre client Office 365 à l’aide de la commande [login](https://pnp.github.io/office365-cli/cmd/login/) .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-485">Next, connect to your Office 365 tenant using the [login](https://pnp.github.io/office365-cli/cmd/login/) command.</span></span>

<span data-ttu-id="b1e9b-486">Suivez ces étapes pour installer et configurer le CDN afin d’héberger vos ressources dans SharePoint Online à l’aide de l’interface de ligne de commande Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-486">Complete these steps to set up and configure the CDN to host your assets in SharePoint Online using the Office 365 CLI.</span></span>

<details>
  <summary><span data-ttu-id="b1e9b-487">Cliquez pour développer</span><span class="sxs-lookup"><span data-stu-id="b1e9b-487">Click to expand</span></span></summary>

### <a name="enable-the-office-365-cdn"></a><span data-ttu-id="b1e9b-488">Activer le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-488">Enable the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-489">Vous pouvez gérer l’état du CDN Office 365 dans votre client à l’aide de la commande [spo cdn set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-set/).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-489">You can manage the state of the Office 365 CDN in your tenant using the [spo cdn set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-set/) command.</span></span>

<span data-ttu-id="b1e9b-490">Pour activer le CDN public Office 365 dans votre client exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-490">To enable the Office 365 Public CDN in your tenant execute:</span></span>

```sh
spo cdn set --type Public --enabled true
```

<span data-ttu-id="b1e9b-491">Pour activer le CDN Office 365 SharePoint, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-491">To enable the Office 365 SharePoint CDN, execute:</span></span>

```sh
spo cdn set --type Private --enabled true
```

#### <a name="view-the-current-status-of-the-office-365-cdn"></a><span data-ttu-id="b1e9b-492">Affichage de l’état actuel du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-492">View the current status of the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-493">Pour vérifier si le type particulier de CDN Office 365 est activé ou désactivé, utilisez la commande [SPO CDN Get](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-get/) .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-493">To check if the particular type of Office 365 CDN is enabled or disabled, use the [spo cdn get](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-get/) command.</span></span>

<span data-ttu-id="b1e9b-494">Pour vérifier si le CDN public Office 365 est activé, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-494">To check if the Office 365 Public CDN is enabled, execute:</span></span>

```sh
spo cdn get --type Public
```

### <a name="view-the-office-365-cdn-origins"></a><span data-ttu-id="b1e9b-495">Afficher les origines du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-495">View the Office 365 CDN origins</span></span>

<span data-ttu-id="b1e9b-496">Pour afficher les origines actuellement configurées du CDN public Office 365, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-496">To view the currently configured Office 365 Public CDN origins execute:</span></span>

```sh
spo cdn origin list --type Public
```

<span data-ttu-id="b1e9b-497">Consultez la rubrique [origines du CDN par défaut](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) pour obtenir des informations sur les origines qui sont configurées par défaut lorsque vous activez le CDN Office 365.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-497">See [Default CDN origins](use-microsoft-365-cdn-with-spo.md#default-cdn-origins) for information about the origins that are provisioned by default when you enable the Office 365 CDN.</span></span>

### <a name="add-an-office-365-cdn-origin"></a><span data-ttu-id="b1e9b-498">Ajouter une origine de CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-498">Add an Office 365 CDN origin</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1e9b-499">Vous ne devez jamais placer de ressources sensibles à votre organisation dans une bibliothèque de documents SharePoint configurée comme une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-499">You should never place resources that are considered sensitive to your organization in a SharePoint document library configured as a public origin.</span></span>

<span data-ttu-id="b1e9b-500">Utilisez la commande [spo cdn origin add](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-add/) pour définir une origine de CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-500">Use the [spo cdn origin add](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-add/) command to define a CDN origin.</span></span> <span data-ttu-id="b1e9b-501">Vous pouvez définir plusieurs origines.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-501">You can define multiple origins.</span></span> <span data-ttu-id="b1e9b-502">L’origine est une URL pointant vers un dossier ou une bibliothèque SharePoint qui contient les ressources qui doivent être hébergées par le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-502">The origin is a URL that points to a SharePoint library or folder that contains the assets that you want to be hosted by the CDN.</span></span>

```sh
spo cdn origin add --type [Public | Private] --origin <path>
```

<span data-ttu-id="b1e9b-503">Où `path` est le chemin d’accès relatif au dossier qui contient les biens.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-503">Where `path` is the relative path to the folder that contains the assets.</span></span> <span data-ttu-id="b1e9b-504">Vous pouvez utiliser des caractères génériques en plus des chemins d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-504">You can use wildcards in addition to relative paths.</span></span>

<span data-ttu-id="b1e9b-505">Pour inclure toutes les ressources de la **Galerie de pages maîtres** de tous les sites en tant qu’origine publique, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-505">To include all assets in the **Master Page Gallery** of all sites as a public origin, execute:</span></span>

```sh
spo cdn origin add --type Public --origin */masterpage
```

<span data-ttu-id="b1e9b-506">Pour configurer une origine privée pour une collection de sites spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-506">To configure a private origin for a specific site collection, execute:</span></span>

```sh
spo cdn origin add --type Private --origin sites/site1/siteassets
```

> [!NOTE]
> <span data-ttu-id="b1e9b-507">Après l’ajout d’une origine de CDN, un délai de 15 minutes maximum peut être nécessaire avant que vous ne puissiez récupérer des fichiers par le biais du service de CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-507">After adding a CDN origin, it might take up to 15 minutes for you to be able to retrieve files via the CDN service.</span></span> <span data-ttu-id="b1e9b-508">Vous pouvez vérifier si l’origine spécifique a déjà été activée à l’aide la commande [spo cdn origin list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-list/).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-508">You can verify if the particular origin has already been enabled using the [spo cdn origin list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-list/) command.</span></span>

### <a name="remove-an-office-365-cdn-origin"></a><span data-ttu-id="b1e9b-509">Supprimer une origine de CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-509">Remove an Office 365 CDN origin</span></span>

<span data-ttu-id="b1e9b-510">Utilisez la commande [spo cdn origin remove](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-remove/) pour supprimer une origine de CDN pour le type de CDN spécifié.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-510">Use the [spo cdn origin remove](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-remove/) command to remove a CDN origin for the specified CDN type.</span></span>

<span data-ttu-id="b1e9b-511">Pour supprimer une origine publique de la configuration du CDN, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-511">To remove a public origin from the CDN configuration, execute:</span></span>

```sh
spo cdn origin remove --type Public --origin */masterpage
```

> [!NOTE]
> <span data-ttu-id="b1e9b-512">La suppression d’une origine de CDN n’affecte pas les fichiers stockés dans une bibliothèque de documents correspondant à cette origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-512">Removing a CDN origin doesn't affect the files stored in any document library matching that origin.</span></span> <span data-ttu-id="b1e9b-513">Si ces ressources ont été référencées à l’aide de leur URL SharePoint, SharePoint revient automatiquement à l’URL d’origine pointant vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-513">If these assets have been referenced using their SharePoint URL, SharePoint will automatically switch back to the original URL pointing to the document library.</span></span> <span data-ttu-id="b1e9b-514">Toutefois, si des ressources ont été référencées à l’aide d’une URL de CDN public, la suppression de l’origine rompt le lien et vous devez les modifier manuellement.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-514">If, however, assets have been referenced using a public CDN URL, then removing the origin will break the link and you will need to manually change them.</span></span>

### <a name="modify-an-office-365-cdn-origin"></a><span data-ttu-id="b1e9b-515">Modifier une origine de CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-515">Modify an Office 365 CDN origin</span></span>

<span data-ttu-id="b1e9b-516">Il n’est pas possible de modifier une origine de CDN existante.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-516">It's not possible to modify an existing CDN origin.</span></span> <span data-ttu-id="b1e9b-517">Vous devez plutôt supprimer l’origine de CDN définie précédemment à l’aide de la commande `spo cdn origin remove` et en ajouter une nouvelle à l’aide de la commande `spo cdn origin add`.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-517">Instead, you should remove the previously defined CDN origin using the `spo cdn origin remove` command and add a new one using the `spo cdn origin add` command.</span></span>

### <a name="change-the-types-of-files-to-include-in-the-office-365-cdn"></a><span data-ttu-id="b1e9b-518">Modifier les types de fichiers à inclure dans le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-518">Change the types of files to include in the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-519">Par défaut, les types de fichiers suivants sont inclus dans le CDN : _. CSS,. EOT,. gif,. ico,. jpeg,. jpg,. js,. map,. png,. svg,. ttf,. WOFF et. woff2_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-519">By default, the following file types are included in the CDN: _.css, .eot, .gif, .ico, .jpeg, .jpg, .js, .map, .png, .svg, .ttf, .woff and .woff2_.</span></span> <span data-ttu-id="b1e9b-520">Si vous devez inclure des types de fichier supplémentaires dans le CDN, vous pouvez modifier la configuration du CDN à l’aide de la commande [spo cdn policy set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-set/).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-520">If you need to include additional file types in the CDN, you can change the CDN configuration using the [spo cdn policy set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-set/) command.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-521">Lorsque vous modifiez la liste des types de fichier, vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-521">When changing the list of file types, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-522">Pour inclure des types de fichier supplémentaires, utilisez d’abord la commande [spo cdn policy list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-list/) afin de vérifier les types de fichier qui sont actuellement configurés.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-522">If you want to include additional file types, first use the [spo cdn policy list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-origin-list/) command to find out which file types are currently configured.</span></span>

<span data-ttu-id="b1e9b-523">Pour ajouter le type de fichier _JSON_ à la liste par défaut des types de fichiers inclus dans le CDN public, exécutez :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-523">To add the _JSON_ file type to the default list of file types included in the public CDN, execute:</span></span>

```sh
spo cdn policy set --type Public --policy IncludeFileExtensions --value "CSS,EOT,GIF,ICO,JPEG,JPG,JS,MAP,PNG,SVG,TTF,WOFF,JSON"
```

### <a name="change-the-list-of-site-classifications-you-want-to-exclude-from-the-office-365-cdn"></a><span data-ttu-id="b1e9b-524">Modification de la liste des classifications de site que vous souhaitez exclure du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-524">Change the list of site classifications you want to exclude from the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-525">Utilisez la commande [spo cdn policy set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-set/) pour exclure les classifications de site que vous ne souhaitez pas rendre disponibles via le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-525">Use the [spo cdn policy set](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-set/) command to exclude site classifications that you do not want to make available over the CDN.</span></span> <span data-ttu-id="b1e9b-526">Par défaut, aucune classification de site n’est exclue.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-526">By default, no site classifications are excluded.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-527">Lorsque vous modifiez la liste des classifications de site exclues, vous remplacez la liste actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-527">When changing the list of excluded site classifications, you overwrite the currently defined list.</span></span> <span data-ttu-id="b1e9b-528">Pour exclure des classifications supplémentaires, utilisez d’abord la commande [spo cdn policy list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-list/) afin de vérifier les classifications qui sont actuellement configurées.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-528">If you want to exclude additional classifications, first use the [spo cdn policy list](https://pnp.github.io/office365-cli/cmd/spo/cdn/cdn-policy-list/) command to find out which classifications are currently configured.</span></span>

<span data-ttu-id="b1e9b-529">Pour exclure les sites classés comme _IEA_ du CDN public, exécutez</span><span class="sxs-lookup"><span data-stu-id="b1e9b-529">To exclude sites classified as _HBI_ from the public CDN, execute</span></span>

```sh
spo cdn policy set --type Public --policy ExcludeRestrictedSiteClassifications --value "HBI"
```

### <a name="disable-the-office-365-cdn"></a><span data-ttu-id="b1e9b-530">Désactiver le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-530">Disable the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-531">Pour désactiver le CDN Office 365, utilisez la commande `spo cdn set`, par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-531">To disable the Office 365 CDN use the `spo cdn set` command, for example:</span></span>

```sh
spo cdn set --type Public --enabled false
```

</details>

## <a name="using-your-cdn-assets"></a><span data-ttu-id="b1e9b-532">Utilisation de vos ressources CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-532">Using your CDN assets</span></span>

<span data-ttu-id="b1e9b-533">À présent que vous avez activé le CDN et les origines et les stratégies configurées, vous pouvez commencer à utiliser vos ressources CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-533">Now that you have enabled the CDN and configured origins and policies, you can begin using your CDN assets.</span></span>

<span data-ttu-id="b1e9b-534">Cette section vous aidera à comprendre comment utiliser les URL du CDN dans vos pages et votre contenu SharePoint afin que SharePoint redirige les demandes d’actifs dans les origines publiques et privées vers le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-534">This section will help you understand how to use CDN URLs in your SharePoint pages and content so that SharePoint redirects requests for assets in both public and private origins to the CDN.</span></span>

+ [<span data-ttu-id="b1e9b-535">Mise à jour des liens vers les éléments CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-535">Updating links to CDN assets</span></span>](use-microsoft-365-cdn-with-spo.md#updating-links-to-cdn-assets)
+ [<span data-ttu-id="b1e9b-536">Utilisation des biens dans des origines publiques</span><span class="sxs-lookup"><span data-stu-id="b1e9b-536">Using assets in public origins</span></span>](use-microsoft-365-cdn-with-spo.md#using-assets-in-public-origins)
+ [<span data-ttu-id="b1e9b-537">Utilisation des biens dans les origines privées</span><span class="sxs-lookup"><span data-stu-id="b1e9b-537">Using assets in private origins</span></span>](use-microsoft-365-cdn-with-spo.md#using-assets-in-private-origins)

<span data-ttu-id="b1e9b-538">Pour plus d’informations sur l’utilisation du CDN pour l’hébergement de composants WebPart côté client, consultez la rubrique [héberger votre composant WebPart côté client à partir d’Office 365 CDN (Hello World quatrième partie)](https://docs.microsoft.com/sharepoint/dev/spfx/web-parts/get-started/hosting-webpart-from-office-365-cdn).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-538">For information on how to use the CDN for hosting client-side web parts, see the topic [Host your client-side web part from Office 365 CDN (Hello World part 4)](https://docs.microsoft.com/sharepoint/dev/spfx/web-parts/get-started/hosting-webpart-from-office-365-cdn).</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-539">Si vous ajoutez le dossier _ClientSideAssets_ à la liste des origines du CDN **privé** , les composants WebPart hébergés dans le CDN ne seront pas affichés.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-539">If you add the _ClientSideAssets_ folder to the **private** CDN origins list, CDN-hosted custom web parts will fail to render.</span></span> <span data-ttu-id="b1e9b-540">Les fichiers utilisés par les composants WebPart SPFX ne peuvent utiliser que le CDN public et le dossier ClientSideAssets est une origine par défaut pour le CDN public.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-540">Files used by SPFX web parts can only utilize the public CDN and the ClientSideAssets folder is a default origin for public CDN.</span></span> 

### <a name="updating-links-to-cdn-assets"></a><span data-ttu-id="b1e9b-541">Mise à jour des liens vers les éléments CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-541">Updating links to CDN assets</span></span>

<span data-ttu-id="b1e9b-542">Pour utiliser des biens que vous avez ajoutés à une origine, il vous suffit de mettre à jour les liens vers le fichier d’origine avec le chemin d’accès au fichier dans l’origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-542">To use assets that you have added to an origin, you simply update links to the original file with the path to the file in the origin.</span></span>

+ <span data-ttu-id="b1e9b-543">Modifier la page ou le contenu qui contient des liens vers des ressources que vous avez ajoutées à une origine.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-543">Edit the page or content that contains links to assets you have added to an origin.</span></span> <span data-ttu-id="b1e9b-544">Vous pouvez également utiliser l’une des méthodes suivantes pour rechercher et remplacer des liens dans une collection de sites ou de sites si vous souhaitez mettre à jour le lien vers un élément donné partout où il apparaît.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-544">You can also use one of several methods to globally search and replace links across an enter site or site collection if you want to update the link to a given asset everywhere it appears.</span></span>
+ <span data-ttu-id="b1e9b-545">Pour chaque lien vers un élément dans une origine, remplacez le chemin d’accès par le chemin d’accès au fichier dans l’origine du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-545">For each link to an asset in an origin, replace the path with the path to the file in the CDN origin.</span></span> <span data-ttu-id="b1e9b-546">Vous pouvez utiliser des chemins d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-546">You can use relative paths.</span></span>
+ <span data-ttu-id="b1e9b-547">Enregistrez la page ou le contenu.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-547">Save the page or content.</span></span>

<span data-ttu-id="b1e9b-548">Par exemple, considérez l’image _/site/SiteAssets/images/image.png_, que vous avez copiée dans le dossier de la bibliothèque de documents _/site/CDN_origins/public/_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-548">For example, consider the image _/site/SiteAssets/images/image.png_, which you have copied to the document library folder _/site/CDN_origins/public/_.</span></span> <span data-ttu-id="b1e9b-549">Pour utiliser l’élément CDN, remplacez le chemin d’accès d’origine de l’emplacement du fichier image par le chemin d’accès à l’origine pour que la nouvelle URL _/site/CDN_origins/public/image.png_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-549">To use the CDN asset, replace the original path to the image file location with the path to the origin to make the new URL _/site/CDN_origins/public/image.png_.</span></span>

<span data-ttu-id="b1e9b-550">Si vous souhaitez utiliser l’URL complète de l’élément au lieu d’un chemin d’accès relatif, construisez le lien comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-550">If you want to use the full URL to the asset instead of a relative path, construct the link like so:</span></span>

`https://<TenantHostName>.sharepoint.com/sites/site/CDN_origins/public/image.png`

> [!NOTE]
> <span data-ttu-id="b1e9b-551">En règle générale, vous ne devez pas coder les URL directement dans les ressources du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-551">In general, you should not hardcode URLs directly to assets in the CDN.</span></span> <span data-ttu-id="b1e9b-552">Toutefois, vous pouvez créer manuellement des URL pour des biens dans des origines publiques si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-552">However, you can manually construct URLs for assets in public origins if needed.</span></span> <span data-ttu-id="b1e9b-553">Pour plus d’informations, consultez la rubrique relative [aux URL de CDN en dur pour les biens publics](use-microsoft-365-cdn-with-spo.md#hardcoding-cdn-urls-for-public-assets).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-553">For more information, see [Hardcoding CDN URLs for public assets](use-microsoft-365-cdn-with-spo.md#hardcoding-cdn-urls-for-public-assets).</span></span>

<span data-ttu-id="b1e9b-554">Pour en savoir plus sur la façon de vérifier que les biens sont pris en charge par le CDN, voir [Comment puis-je vérifier que les biens sont pris en charge par le CDN ?](use-microsoft-365-cdn-with-spo.md#CDNConfirm) dans la section [Troubleshooting the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#CDNTroubleshooting) .</span><span class="sxs-lookup"><span data-stu-id="b1e9b-554">To learn about how to verify that assets are being served from the CDN, see [How do I confirm that assets are being served by the CDN?](use-microsoft-365-cdn-with-spo.md#CDNConfirm) in the [Troubleshooting the Office 365 CDN](use-microsoft-365-cdn-with-spo.md#CDNTroubleshooting) section.</span></span>

### <a name="using-assets-in-public-origins"></a><span data-ttu-id="b1e9b-555">Utilisation des biens dans des origines publiques</span><span class="sxs-lookup"><span data-stu-id="b1e9b-555">Using assets in public origins</span></span>

<span data-ttu-id="b1e9b-556">La **fonctionnalité de publication** de SharePoint Online réécrit automatiquement les URL des biens stockés dans des origines publiques vers leurs équivalents CDN afin que les biens soient pris en charge par le service CDN au lieu de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-556">The **Publishing feature** in SharePoint Online automatically rewrites URLs of assets stored in public origins to their CDN equivalents so that assets are served from the CDN service instead of SharePoint.</span></span>

<span data-ttu-id="b1e9b-557">Si votre origine se trouve dans un site où la fonctionnalité de publication est activée et que les ressources que vous souhaitez décharger vers le CDN se trouvent dans l’une des catégories suivantes, SharePoint réécrit automatiquement les URL des biens dans l’origine, à condition que l’actif n’ait pas été exclu par une stratégie de CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-557">If your origin is in a site with the Publishing feature enabled, and the assets you want to offload to the CDN are in one of the following categories, SharePoint will automatically rewrite URLs for assets in the origin, provided that the asset has not been excluded by a CDN policy.</span></span>

<span data-ttu-id="b1e9b-558">Voici un aperçu des liens qui sont réécrits automatiquement par la fonctionnalité de publication SharePoint :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-558">The following is an overview of which links are automatically rewritten by the SharePoint Publishing feature:</span></span>

+ <span data-ttu-id="b1e9b-559">URL IMG/LINK/CSS dans les réponses HTML de pages de publications classiques</span><span class="sxs-lookup"><span data-stu-id="b1e9b-559">IMG/LINK/CSS URLs in classic publishing page HTML responses</span></span>
  + <span data-ttu-id="b1e9b-560">Cela comprend les images ajoutées par des auteurs dans le contenu HTML d’une page.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-560">This includes images added by authors within the HTML content of a page</span></span>
+ <span data-ttu-id="b1e9b-561">URL d’images de composants WebPart de diaporamas de bibliothèque d’images</span><span class="sxs-lookup"><span data-stu-id="b1e9b-561">Picture Library SlideShow webpart image URLs</span></span>
+ <span data-ttu-id="b1e9b-562">Champs d’image dans les résultats d’API REST SPList (RenderListDataAsStream)</span><span class="sxs-lookup"><span data-stu-id="b1e9b-562">Image fields in SPList REST API (RenderListDataAsStream) results</span></span>
  + <span data-ttu-id="b1e9b-563">Utiliser la nouvelle propriété _ImageFieldsToTryRewriteToCdnUrls_ pour fournir une liste de champs séparés par des virgules</span><span class="sxs-lookup"><span data-stu-id="b1e9b-563">Use the new property _ImageFieldsToTryRewriteToCdnUrls_ to provide a comma separated list of fields</span></span>
  + <span data-ttu-id="b1e9b-564">Prend en charge les champs de lien hypertexte et PublishingImage</span><span class="sxs-lookup"><span data-stu-id="b1e9b-564">Supports hyperlink fields and PublishingImage fields</span></span>
+ <span data-ttu-id="b1e9b-565">Rendus d’image SharePoint</span><span class="sxs-lookup"><span data-stu-id="b1e9b-565">SharePoint image renditions</span></span>

<span data-ttu-id="b1e9b-566">Le diagramme suivant illustre le flux de travail lorsque SharePoint reçoit une demande pour une page contenant des biens provenant d’une origine publique.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-566">The following diagram illustrates the workflow when SharePoint receives a request for a page containing assets from a public origin.</span></span>

<span data-ttu-id="b1e9b-567">![Diagramme de flux de travail : récupération des composants de CDN Office 365 à partir d’une origine publique](../media/O365-CDN/o365-cdn-public-steps-transparent.svg "Flux de travail : extraction des ressources CDN Office 365 d’une origine publique")</span><span class="sxs-lookup"><span data-stu-id="b1e9b-567">![Workflow diagram: Retrieving Office 365 CDN assets from a public origin](../media/O365-CDN/o365-cdn-public-steps-transparent.svg "Workflow: Retrieving Office 365 CDN assets from a public origin")</span></span>

> [!TIP]
> <span data-ttu-id="b1e9b-568">Si vous souhaitez désactiver la réécriture automatique pour des URL spécifiques sur une page, vous pouvez extraire la page et ajouter le paramètre de chaîne de requête. \*\* NoAutoReWrites = true\*\* jusqu’à la fin de chaque lien que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-568">If you want to disable auto-rewriting for specific URLs on a page, you can check out the page and add the query string parameter **?NoAutoReWrites=true** to the end of each link you want to disable.</span></span>

#### <a name="hardcoding-cdn-urls-for-public-assets"></a><span data-ttu-id="b1e9b-569">URL de CDN en dur pour les ressources publiques</span><span class="sxs-lookup"><span data-stu-id="b1e9b-569">Hardcoding CDN URLs for public assets</span></span>

<span data-ttu-id="b1e9b-570">Si la fonctionnalité de _publication_ n’est pas activée pour une origine publique ou si l’élément n’est pas l’un des types de liens pris en charge par la fonctionnalité de réécriture automatique du service CDN, vous pouvez créer manuellement des URL vers l’emplacement du CDN des biens et utiliser ces URL dans votre contenu.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-570">If the _Publishing_ feature is not enabled for a public origin, or the asset is not one of the link types supported by the auto-rewrite feature of the CDN service, you can manually construct URLs to the CDN location of the assets and use these URLs in your content.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-571">Vous ne pouvez pas coder en dur les URL de CDN vers des biens dans une origine privée car le jeton d’accès requis qui forme la dernière section de l’URL est généré au moment de la demande de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-571">You cannot hardcode CDN URLs to assets in a private origin because the required access token that forms the last section of the URL is generated at the time the resource is requested.</span></span>

<span data-ttu-id="b1e9b-572">Pour les ressources de CDN public, le format de l’URL se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-572">For public CDN assets, the URL format will look like the following:</span></span>

``` html
https://publiccdn.sharepointonline.com/<TenantHostName>/sites/site/library/asset.png
```

<span data-ttu-id="b1e9b-573">Remplacez **TenantHostName** par le nom de votre client.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-573">Replace **TenantHostName** with your tenant name.</span></span> <span data-ttu-id="b1e9b-574">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-574">Example:</span></span>

``` html
https://publiccdn.sharepointonline.com/contoso.sharepoint.com/sites/site/library/asset.png
```

### <a name="using-assets-in-private-origins"></a><span data-ttu-id="b1e9b-575">Utilisation des biens dans les origines privées</span><span class="sxs-lookup"><span data-stu-id="b1e9b-575">Using assets in private origins</span></span>

<span data-ttu-id="b1e9b-576">Aucune configuration supplémentaire n’est requise pour utiliser des biens dans des origines privées.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-576">No additional configuration is required to use assets in private origins.</span></span> <span data-ttu-id="b1e9b-577">SharePoint Online réécrit automatiquement des URL pour des biens dans des origines privées, de sorte que les demandes de ces ressources seront toujours traitées à partir du CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-577">SharePoint Online automatically rewrites URLs for assets in private origins so requests for those assets will always be served from the CDN.</span></span> <span data-ttu-id="b1e9b-578">Vous ne pouvez pas créer manuellement des URL vers des éléments CDN dans des origines privées car ces URL contiennent des jetons qui doivent être générés automatiquement par SharePoint Online au moment de la demande de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-578">You cannot manually build URLs to CDN assets in private origins because these URLs contain tokens that must be auto-generated by SharePoint Online at the time the asset is requested.</span></span>

<span data-ttu-id="b1e9b-579">L’accès aux biens dans des origines privées est protégé par des jetons générés de manière dynamique en fonction des autorisations des utilisateurs pour l’origine, avec les limitations décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-579">Access to assets in private origins is protected by dynamically generated tokens based on user permissions to the origin, with the caveats described in the following sections.</span></span> <span data-ttu-id="b1e9b-580">Les utilisateurs doivent disposer au moins d’un accès **en lecture** à l’origine du CDN pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-580">Users must have at least **read** access to the origins for the CDN to render content.</span></span>

<span data-ttu-id="b1e9b-581">Le diagramme suivant illustre le flux de travail lorsque SharePoint reçoit une demande pour une page contenant des ressources provenant d’une origine privée.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-581">The following diagram illustrates the workflow when SharePoint receives a request for a page containing assets from a private origin.</span></span>

<span data-ttu-id="b1e9b-582">![Diagramme de flux de travail : récupération des composants de CDN Office 365 à partir d’une origine privée](../media/O365-CDN/o365-cdn-private-steps-transparent.svg "Flux de travail : extraction des composants CDN Office 365 d’une origine privée")</span><span class="sxs-lookup"><span data-stu-id="b1e9b-582">![Workflow diagram: Retrieving Office 365 CDN assets from a private origin](../media/O365-CDN/o365-cdn-private-steps-transparent.svg "Workflow: Retrieving Office 365 CDN assets from a private origin")</span></span>

#### <a name="token-based-authorization-in-private-origins"></a><span data-ttu-id="b1e9b-583">Autorisation basée sur des jetons dans les origines privées</span><span class="sxs-lookup"><span data-stu-id="b1e9b-583">Token-based authorization in private origins</span></span>

<span data-ttu-id="b1e9b-584">L’accès aux biens dans les origines privées dans le CDN Office 365 est accordé par des jetons générés par SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-584">Access to assets in private origins in the Office 365 CDN is granted by tokens generated by SharePoint Online.</span></span> <span data-ttu-id="b1e9b-585">Les utilisateurs qui ont déjà l’autorisation d’accéder au dossier ou à la bibliothèque désigné par l’origine reçoivent automatiquement des jetons qui permettent à l’utilisateur d’accéder au fichier en fonction de son niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-585">Users who already have permission to access to the folder or library designated by the origin are automatically granted tokens that permit the user to access the file based on their permission level.</span></span> <span data-ttu-id="b1e9b-586">Ces jetons d’accès sont valides entre 30 et 90 minutes après leur génération afin d’empêcher les attaques par relecture de jetons.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-586">These access tokens are valid for 30 to 90 minutes after they are generated to help prevent token replay attacks.</span></span>

<span data-ttu-id="b1e9b-587">Une fois que le jeton d’accès est généré, SharePoint Online renvoie un URI personnalisé vers le client contenant deux paramètres d’autorisation _manger_ (jeton d’autorisation Edge) et _avoine_ (jeton d’autorisation d’origine).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-587">Once the access token is generated, SharePoint Online returns a custom URI to the client containing two authorization parameters _eat_ (edge authorization token) and _oat_ (origin authorization token).</span></span> <span data-ttu-id="b1e9b-588">La structure de chaque jeton est _< « heure d’expiration au format de l’heure de l’époque » >__< « signature sécurisée » >_.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-588">The structure of each token is _<'expiration time in Epoch time format'>__<'secure signature'>_.</span></span> <span data-ttu-id="b1e9b-589">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-589">For example:</span></span>

``` html
https://privatecdn.sharepointonline.com/contoso.sharepoint.com/sites/site1/library1/folder1/image1.jpg?eat=1486154359_cc59042c5c55c90b26a2775323c7c8112718431228fe84d568a3795a63912840&oat=1486154359_7d73c2e3ba4b7b1f97242332900616db0d4ffb04312
```

> [!NOTE]
> <span data-ttu-id="b1e9b-590">Toute personne en possession du jeton peut accéder à la ressource dans le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-590">Anyone in possession of the token can access the resource in the CDN.</span></span> <span data-ttu-id="b1e9b-591">Toutefois, les URL contenant ces jetons d’accès sont partagées uniquement via HTTPs, de sorte que, sauf si l’URL est explicitement partagée par un utilisateur final avant l’expiration du jeton, ce dernier n’est pas accessible aux utilisateurs non autorisés.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-591">However, URLs containing these access tokens are only shared over HTTPS, so unless the URL is explicitly shared by an end user before the token expires, the asset won't be accessible to unauthorized users.</span></span>

#### <a name="item-level-permissions-are-not-supported-for-assets-in-private-origins"></a><span data-ttu-id="b1e9b-592">Les autorisations au niveau des éléments ne sont pas prises en charge pour les biens dans les origines privées</span><span class="sxs-lookup"><span data-stu-id="b1e9b-592">Item-level permissions are not supported for assets in private origins</span></span>

<span data-ttu-id="b1e9b-593">Il est important de noter que SharePoint Online ne prend pas en charge les autorisations au niveau des éléments dans les origines privées.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-593">It is important to note that SharePoint Online does not support item-level permissions for assets in private origins.</span></span> <span data-ttu-id="b1e9b-594">Par exemple, pour un fichier se trouvant à `https://contoso.sharepoint.com/sites/site1/library1/folder1/image1.jpg` , les utilisateurs ont un accès effectif au fichier en fonction des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-594">For example, for a file located at `https://contoso.sharepoint.com/sites/site1/library1/folder1/image1.jpg`, users have effective access to the file given the following conditions:</span></span>

|<span data-ttu-id="b1e9b-595">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="b1e9b-595">User</span></span>  |<span data-ttu-id="b1e9b-596">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b1e9b-596">Permissions</span></span>  |<span data-ttu-id="b1e9b-597">Accès effectif</span><span class="sxs-lookup"><span data-stu-id="b1e9b-597">Effective access</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="b1e9b-598">Utilisateur 1</span><span class="sxs-lookup"><span data-stu-id="b1e9b-598">User 1</span></span>     |<span data-ttu-id="b1e9b-599">A accès à dossier1</span><span class="sxs-lookup"><span data-stu-id="b1e9b-599">Has access to folder1</span></span>         |<span data-ttu-id="b1e9b-600">Peut accéder à image1.jpg à partir du CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-600">Can access image1.jpg from the CDN</span></span>         |
|<span data-ttu-id="b1e9b-601">Utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="b1e9b-601">User 2</span></span>     |<span data-ttu-id="b1e9b-602">N’a pas accès à dossier1</span><span class="sxs-lookup"><span data-stu-id="b1e9b-602">Does not have access to folder1</span></span>         |<span data-ttu-id="b1e9b-603">Impossible d’accéder à image1.jpg à partir du CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-603">Cannot access image1.jpg from the CDN</span></span>         |
|<span data-ttu-id="b1e9b-604">Utilisateur 3</span><span class="sxs-lookup"><span data-stu-id="b1e9b-604">User 3</span></span>     |<span data-ttu-id="b1e9b-605">N’a pas accès à Dossier1, mais dispose d’une autorisation explicite pour accéder à image1.jpg dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-605">Does not have access to folder1, but is granted explicit permission to access image1.jpg in SharePoint Online</span></span>         |<span data-ttu-id="b1e9b-606">Peut accéder à la image1.jpg des biens directement à partir de SharePoint Online, mais pas à partir du CDN</span><span class="sxs-lookup"><span data-stu-id="b1e9b-606">Can access the asset image1.jpg directly from SharePoint Online, but not from the CDN</span></span>         |
|<span data-ttu-id="b1e9b-607">Utilisateur 4</span><span class="sxs-lookup"><span data-stu-id="b1e9b-607">User 4</span></span>     |<span data-ttu-id="b1e9b-608">A accès à Dossier1, mais a explicitement refusé l’accès à image1.jpg dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-608">Has access to folder1, but has been explicitly denied access to image1.jpg in SharePoint Online</span></span>         |<span data-ttu-id="b1e9b-609">Impossible d’accéder au bien à partir de SharePoint Online, mais peut accéder à l’élément à partir du CDN malgré le fait que l’accès au fichier est refusé dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b1e9b-609">Cannot access the asset from SharePoint Online, but can access the asset from the CDN despite being denied access to the file in SharePoint Online</span></span>         |

<span data-ttu-id="b1e9b-610"><a name="CDNTroubleshooting"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-610"><a name="CDNTroubleshooting"> </a></span></span>
## <a name="troubleshooting-the-office-365-cdn"></a><span data-ttu-id="b1e9b-611">Dépannage du CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-611">Troubleshooting the Office 365 CDN</span></span>

<span data-ttu-id="b1e9b-612"><a name="CDNConfirm"> </a></span><span class="sxs-lookup"><span data-stu-id="b1e9b-612"><a name="CDNConfirm"> </a></span></span>
### <a name="how-do-i-confirm-that-assets-are-being-served-by-the-cdn"></a><span data-ttu-id="b1e9b-613">Comment puis-je vérifier que les biens sont pris en charge par le CDN ?</span><span class="sxs-lookup"><span data-stu-id="b1e9b-613">How do I confirm that assets are being served by the CDN?</span></span>

<span data-ttu-id="b1e9b-614">Une fois que vous avez ajouté des liens vers des ressources CDN à une page, vous pouvez confirmer que l’élément est pris en charge par le CDN en accédant à la page, en cliquant avec le bouton droit sur l’image une fois qu’elle a affiché et vérifié l’URL de l’image.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-614">Once you have added links to CDN assets to a page, you can confirm that the asset is being served from the CDN by browsing to the page, right clicking on the image once it has rendered and reviewing the image URL.</span></span>

<span data-ttu-id="b1e9b-615">Vous pouvez également utiliser les outils de développement de votre navigateur pour afficher l’URL de chaque ressource sur une page ou utiliser un outil de suivi réseau tiers.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-615">You can also use your browser's developer tools to view the URL for each asset on a page, or use a third party network trace tool.</span></span>

> [!NOTE]
> <span data-ttu-id="b1e9b-616">Si vous utilisez un outil réseau tel que Fiddler pour tester vos biens en dehors du rendu de l’élément à partir d’une page SharePoint, vous devez ajouter manuellement l’en-tête Referer « Referer : `https://yourdomain.sharepoint.com` » à la requête get où l’URL est l’URL racine de votre client SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-616">If you use a network tool such as Fiddler to test your assets outside of rendering the asset from a SharePoint page, you must manually add the referer header "Referer: `https://yourdomain.sharepoint.com`" to the GET request where the URL is the root URL of your SharePoint Online tenant.</span></span>

<span data-ttu-id="b1e9b-617">Vous ne pouvez pas tester les URL du CDN directement dans un navigateur Web, car vous devez disposer d’un Referer provenant de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-617">You cannot test CDN URLs directly in a web browser because you must have a referer coming from SharePoint Online.</span></span> <span data-ttu-id="b1e9b-618">Toutefois, si vous ajoutez l’URL de la ressource CDN à une page SharePoint, puis ouvrez la page dans un navigateur, vous verrez l’élément CDN s’afficher sur la page.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-618">However, if you add the CDN asset URL to a SharePoint page and then open the page in a browser, you will see the CDN asset rendered on the page.</span></span>

<span data-ttu-id="b1e9b-619">Pour plus d’informations sur l’utilisation des outils de développement dans le navigateur Microsoft Edge, consultez la rubrique [outils de développement Microsoft Edge](https://docs.microsoft.com/microsoft-edge/devtools-guide).</span><span class="sxs-lookup"><span data-stu-id="b1e9b-619">For more information on using the developer tools in the Microsoft Edge browser, see [Microsoft Edge Developer Tools](https://docs.microsoft.com/microsoft-edge/devtools-guide).</span></span>

<span data-ttu-id="b1e9b-620">Pour regarder une courte vidéo hébergée dans la [chaîne YouTube des modèles et des pratiques pour les développeurs SharePoint](https://aka.ms/sppnp-videos) montrant comment vérifier que votre CDN fonctionne, consultez la rubrique [vérification de votre utilisation du CDN et assurez](https://www.youtube.com/watch?v=ClCtBAtGjE8&list=PLR9nK3mnD-OWMfr1BA9mr5oCw2aJXw4WA&index=5)-vous que la connectivité réseau est optimale.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-620">To watch a short video hosted in the [SharePoint Developer Patterns and Practices YouTube channel](https://aka.ms/sppnp-videos) demonstrating how to verify that your CDN is working, please see [Verifying your CDN usage and ensuring optimal network connectivity](https://www.youtube.com/watch?v=ClCtBAtGjE8&list=PLR9nK3mnD-OWMfr1BA9mr5oCw2aJXw4WA&index=5).</span></span>

### <a name="why-are-assets-from-a-new-origin-unavailable"></a><span data-ttu-id="b1e9b-621">Pourquoi les biens d’une nouvelle origine ne sont-ils pas disponibles ?</span><span class="sxs-lookup"><span data-stu-id="b1e9b-621">Why are assets from a new origin unavailable?</span></span>
<span data-ttu-id="b1e9b-622">Les biens dans de nouvelles origines ne seront pas immédiatement disponibles à l’utilisation, car le temps nécessaire pour que l’inscription se propage via le CDN et que les biens soient chargés du stockage de l’origine vers le CDN.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-622">Assets in new origins will not immediately be available for use, as it takes time for the registration to propagate through the CDN and for the assets to be uploaded from the origin to CDN storage.</span></span> <span data-ttu-id="b1e9b-623">Le temps nécessaire pour que les biens soient disponibles dans le CDN dépend du nombre de ressources et de tailles de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-623">The time required for assets to be available in the CDN depends on how many assets and the files sizes.</span></span>

### <a name="my-client-side-web-part-or-sharepoint-framework-solution-isnt-working"></a><span data-ttu-id="b1e9b-624">Mon composant WebPart côté client ou la solution SharePoint Framework ne fonctionne pas</span><span class="sxs-lookup"><span data-stu-id="b1e9b-624">My client-side web part or SharePoint Framework solution isn't working</span></span>

<span data-ttu-id="b1e9b-625">Lorsque vous activez le CDN Office 365 pour les origines publiques, le service CDN crée automatiquement ces origines par défaut :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-625">When you enable the Office 365 CDN for public origins, the CDN service automatically creates these default origins:</span></span>

+ <span data-ttu-id="b1e9b-626">\*/MASTERPAGE</span><span class="sxs-lookup"><span data-stu-id="b1e9b-626">\*/MASTERPAGE</span></span>
+ <span data-ttu-id="b1e9b-627">\* BIBLIOTHÈQUE/STYLE</span><span class="sxs-lookup"><span data-stu-id="b1e9b-627">\*/STYLE LIBRARY</span></span>
+ <span data-ttu-id="b1e9b-628">\*/CLIENTSIDEASSETS</span><span class="sxs-lookup"><span data-stu-id="b1e9b-628">\*/CLIENTSIDEASSETS</span></span>

<span data-ttu-id="b1e9b-629">Si l’origine \*/clientsideassets est manquante, les solutions de l’infrastructure SharePoint échouent et aucun message d’avertissement ou d’erreur n’est généré.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-629">If the \*/clientsideassets origin is missing, SharePoint Framework solutions will fail, and no warning or error messages are generated.</span></span> <span data-ttu-id="b1e9b-630">Cette origine peut être manquante, car le CDN a été activé avec le paramètre _-NoDefaultOrigins_ défini sur **$true**ou parce que l’origine a été supprimée manuellement.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-630">This origin may be missing either because the CDN was enabled with the _-NoDefaultOrigins_ parameter set to **$true**, or because the origin was manually deleted.</span></span>

<span data-ttu-id="b1e9b-631">Vous pouvez vérifier les origines présentes à l’aide de la commande PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-631">You can check to see which origins are present with the following PowerShell command:</span></span>

``` powershell
Get-SPOTenantCdnOrigins -CdnType Public
```

<span data-ttu-id="b1e9b-632">Ou vous pouvez consulter la CLI Office 365 :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-632">Or you can check with the Office 365 CLI:</span></span>

``` powershell
spo cdn origin list
```

<span data-ttu-id="b1e9b-633">Pour ajouter l’origine dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-633">To add the origin in PowerShell:</span></span>

``` powershell
Add-SPOTenantCdnOrigin -CdnType Public -OriginUrl */CLIENTSIDEASSETS
```

<span data-ttu-id="b1e9b-634">Pour ajouter l’origine dans l’interface CLI Office 365 :</span><span class="sxs-lookup"><span data-stu-id="b1e9b-634">To add the origin in the Office 365 CLI:</span></span>

``` powershell
spo cdn origin add --origin */CLIENTSIDEASSETS
```

### <a name="what-powershell-modules-and-cli-shells-do-i-need-to-work-with-the-office-365-cdn"></a><span data-ttu-id="b1e9b-635">Quels modules PowerShell et shells CLI dois-je utiliser avec le CDN Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="b1e9b-635">What PowerShell modules and CLI shells do I need to work with the Office 365 CDN?</span></span>

<span data-ttu-id="b1e9b-636">Vous pouvez choisir de travailler avec le CDN Office 365 à l’aide du module PowerShell de **SharePoint Online Management Shell** ou de l’interface de ligne de **commande Office 365**.</span><span class="sxs-lookup"><span data-stu-id="b1e9b-636">You can choose to work with the Office 365 CDN using either the **SharePoint Online Management Shell** PowerShell module or the **Office 365 CLI**.</span></span>

+ [<span data-ttu-id="b1e9b-637">Prise en main de SharePoint Online Management Shell</span><span class="sxs-lookup"><span data-stu-id="b1e9b-637">Getting started with SharePoint Online Management Shell</span></span>](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online?view=sharepoint-ps)
+ [<span data-ttu-id="b1e9b-638">Installation d’Office 365 CLI</span><span class="sxs-lookup"><span data-stu-id="b1e9b-638">Installing the Office 365 CLI</span></span>](https://pnp.github.io/office365-cli/user-guide/installing-cli/)

## <a name="see-also"></a><span data-ttu-id="b1e9b-639">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1e9b-639">See also</span></span>

[<span data-ttu-id="b1e9b-640">Réseaux de distribution de contenu</span><span class="sxs-lookup"><span data-stu-id="b1e9b-640">Content Delivery Networks</span></span>](https://aka.ms/o365cdns)

[<span data-ttu-id="b1e9b-641">Planification réseau et optimisation des performances pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-641">Network planning and performance tuning for Office 365</span></span>](https://aka.ms/tune)

[<span data-ttu-id="b1e9b-642">Série de performances SharePoint-série de vidéos pour le CDN Office 365</span><span class="sxs-lookup"><span data-stu-id="b1e9b-642">SharePoint Performance Series - Office 365 CDN video series</span></span>](https://www.youtube.com/playlist?list=PLR9nK3mnD-OWMfr1BA9mr5oCw2aJXw4WA)
