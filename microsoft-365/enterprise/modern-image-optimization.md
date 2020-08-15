---
title: Optimiser les images dans les pages de sites modernes SharePoint Online
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 03/11/2020
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- SPO_Content
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.reviewer: sstewart
search.appverid:
- MET150
description: Découvrez comment utiliser les outils inclus dans SharePoint Online pour optimiser les images dans les pages de site modernes SharePoint Online.
ms.openlocfilehash: 09122dfd0bc832cf9a09cfb05bf0540e323797d9
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690108"
---
# <a name="optimize-images-in-sharepoint-online-modern-site-pages"></a><span data-ttu-id="59a20-103">Optimiser les images dans les pages de sites modernes SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="59a20-103">Optimize images in SharePoint Online modern site pages</span></span>

<span data-ttu-id="59a20-104">Cet article vous aidera à comprendre comment optimiser les images dans les pages de sites modernes SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="59a20-104">This article will help you understand how to optimize images in SharePoint Online modern site pages.</span></span>

<span data-ttu-id="59a20-105">Pour plus d’informations sur l’optimisation des images dans les sites de publication classiques, consultez [Optimisation des images pour SharePoint Online](image-optimization-for-sharepoint-online.md).</span><span class="sxs-lookup"><span data-stu-id="59a20-105">For information about optimizing images in classic publishing sites, see [Image optimization for SharePoint Online](image-optimization-for-sharepoint-online.md)..</span></span>

>[!NOTE]
><span data-ttu-id="59a20-106">Pour plus d’informations sur les performances dans les portails modernes SharePoint Online, consultez [Performances offertes par l’expérience moderne de SharePoint](https://docs.microsoft.com/sharepoint/modern-experience-performance).</span><span class="sxs-lookup"><span data-stu-id="59a20-106">For more information about performance in SharePoint Online modern portals, see [Performance in the modern SharePoint experience](https://docs.microsoft.com/sharepoint/modern-experience-performance).</span></span>

## <a name="use-the-page-diagnostics-for-sharepoint-tool-to-analyze-image-optimization"></a><span data-ttu-id="59a20-107">Utiliser l’outil Diagnostic de page pour SharePoint pour analyser l’optimisation des images</span><span class="sxs-lookup"><span data-stu-id="59a20-107">Use the Page Diagnostics for SharePoint tool to analyze image optimization</span></span>

<span data-ttu-id="59a20-108">L’outil Diagnostic de page pour SharePoint est une extension de navigateur pour le nouveau Microsoft Edge (https://www.microsoft.com/edge) et les navigateurs Chrome que vous pouvez utiliser pour analyser les pages de sites de publication SharePoint classiques et les portails modernes.</span><span class="sxs-lookup"><span data-stu-id="59a20-108">The Page Diagnostics for SharePoint tool is a browser extension for the new Microsoft Edge (https://www.microsoft.com/edge) and Chrome browsers that analyzes both SharePoint Online modern portal and classic publishing site pages.</span></span> <span data-ttu-id="59a20-109">L’outil fournit un rapport pour chaque page analysée montrant comment la page se comporte par rapport à un ensemble défini de critères de performance.</span><span class="sxs-lookup"><span data-stu-id="59a20-109">The tool provides a report for each analyzed page showing how the page performs against a defined set of performance criteria.</span></span> <span data-ttu-id="59a20-110">Pour installer et découvrir l’outil Diagnostic de page pour SharePoint, consultez [Utiliser l’outil Diagnostic de page pour SharePoint Online](page-diagnostics-for-spo.md).</span><span class="sxs-lookup"><span data-stu-id="59a20-110">To install and learn about the Page Diagnostics for SharePoint tool, visit [Use the Page Diagnostics tool for SharePoint Online](page-diagnostics-for-spo.md).</span></span>

>[!NOTE]
><span data-ttu-id="59a20-111">L’outil Diagnostic de page fonctionne uniquement pour SharePoint Online et ne peut pas être utilisé sur une page système SharePoint.</span><span class="sxs-lookup"><span data-stu-id="59a20-111">The Page Diagnostics tool only works for SharePoint Online, and cannot be used on a SharePoint system page.</span></span>

<span data-ttu-id="59a20-112">Lorsque vous analysez une page de site moderne SharePoint avec l’outil Diagnostic de page pour SharePoint, vous pouvez voir des informations sur les images de grande taille dans le volet Tests de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="59a20-112">When you analyze a SharePoint modern site with the Page Diagnostics for SharePoint tool, you can see information about large images in the _Diagnostic tests_ pane.</span></span>

<span data-ttu-id="59a20-113">Les résultats possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="59a20-113">Possible results include:</span></span>

- <span data-ttu-id="59a20-114">**Attention requise** (rouge) : la page contient **une ou plusieurs** images dont la taille est supérieure à 300 Ko</span><span class="sxs-lookup"><span data-stu-id="59a20-114">**Attention required** (red): The page contains **one or more** images over 300KB in size</span></span>
- <span data-ttu-id="59a20-115">**Aucune action requise** (vert) : la page ne contient pas d’images dont la taille est supérieure à 300 Ko</span><span class="sxs-lookup"><span data-stu-id="59a20-115">**No action required** (green): The page contains no images over 300KB in size</span></span>

<span data-ttu-id="59a20-116">Si le résultat **Images de grande taille détectées** apparaît dans la section des résultats **Attention requise**, vous pouvez cliquer sur le résultat pour afficher les détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="59a20-116">If the **Large images detected** result appears in the **Attention required** section of the results, you can click the result to see additional details.</span></span>

![Résultats de l’outil Diagnostic de page](../media/modern-portal-optimization/pagediag-large-images.png)

## <a name="remediate-large-image-issues"></a><span data-ttu-id="59a20-118">Résoudre les problèmes liés aux images de grande taille</span><span class="sxs-lookup"><span data-stu-id="59a20-118">Remediate large image issues</span></span>

<span data-ttu-id="59a20-119">Si une page contient des images dont la taille est supérieure à 300 Ko, sélectionnez le résultat **Images de grande taille détectées** pour voir les images trop volumineuses.</span><span class="sxs-lookup"><span data-stu-id="59a20-119">If a page contains images over 300KB in size, select the **Large images detected** result to see which images are too large.</span></span> <span data-ttu-id="59a20-120">Dans les pages modernes SharePoint Online, les rendus d’images sont automatiquement fournis et dimensionnés en fonction de la taille de la fenêtre du navigateur et de la résolution du moniteur client.</span><span class="sxs-lookup"><span data-stu-id="59a20-120">In modern SharePoint Online pages, renditions of images are automatically provided and sized depending on the size of the browser window and the resolution of the client monitor.</span></span> <span data-ttu-id="59a20-121">Vous devez toujours optimiser les images pour une utilisation sur le Web avant de les télécharger sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="59a20-121">You should always optimize images for web use prior to upload to SharePoint Online.</span></span> <span data-ttu-id="59a20-122">Les images de très grand taille sont automatiquement réduites en taille et en résolution, ce qui peut entraîner des caractéristiques de rendu inattendues.</span><span class="sxs-lookup"><span data-stu-id="59a20-122">Very large images will be automatically reduced in size and resolution which can result in unexpected rendering characteristics.</span></span>

<span data-ttu-id="59a20-123">Avant d’apporter des révisions de page pour résoudre les problèmes de performances, notez le temps de chargement des pages dans les résultats de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="59a20-123">Before you make page revisions to remediate performance issues, make a note of the page load time in the analysis results.</span></span> <span data-ttu-id="59a20-124">Exécutez à nouveau l’outil après votre révision pour déterminer si le nouveau résultat est inclus dans la norme de référence et vérifier le nouveau temps de chargement des pages pour voir s’il y a eu une amélioration.</span><span class="sxs-lookup"><span data-stu-id="59a20-124">Run the tool again after your revision to see if the new result is within the baseline standard, and check the new page load time to see if there was an improvement.</span></span>

![Résultats du temps de chargement des pages](../media/modern-portal-optimization/pagediag-page-load-time.png)

>[!NOTE]
><span data-ttu-id="59a20-126">Le temps de chargement des pages peut varier en fonction de nombreux facteurs tels que la charge réseau, l’heure de la journée et d’autres conditions transitoires.</span><span class="sxs-lookup"><span data-stu-id="59a20-126">Page load time can vary based on a variety of factors such as network load, time of day, and other transient conditions.</span></span> <span data-ttu-id="59a20-127">Vous devez tester le temps de chargement des pages plusieurs fois avant et après avoir apporté des modifications pour vous aider à faire la moyenne des résultats.</span><span class="sxs-lookup"><span data-stu-id="59a20-127">You should test page load time a few times before and after making changes to help you average the results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a20-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59a20-128">Related topics</span></span>

[<span data-ttu-id="59a20-129">Optimisation des performances SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="59a20-129">Tune SharePoint Online performance</span></span>](tune-sharepoint-online-performance.md)

[<span data-ttu-id="59a20-130">Optimisation des performances Office 365</span><span class="sxs-lookup"><span data-stu-id="59a20-130">Tune Office 365 performance</span></span>](tune-microsoft-365-performance.md)

[<span data-ttu-id="59a20-131">Performances offertes par l’expérience moderne de SharePoint</span><span class="sxs-lookup"><span data-stu-id="59a20-131">Performance in the modern SharePoint experience</span></span>](https://docs.microsoft.com/sharepoint/modern-experience-performance)

[<span data-ttu-id="59a20-132">Réseaux de distribution de contenu</span><span class="sxs-lookup"><span data-stu-id="59a20-132">Content delivery networks</span></span>](content-delivery-networks.md)

[<span data-ttu-id="59a20-133">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="59a20-133">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)
