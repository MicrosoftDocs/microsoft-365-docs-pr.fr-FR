---
title: Optimiser le poids des pages de sites modernes SharePoint Online
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
description: Découvrez comment utiliser l’outil Diagnostic de page pour optimiser le poids des pages dans les pages de sites modernes SharePoint Online.
ms.openlocfilehash: 780d8ca0debbc5efb834f8f3543b9a5a8d168108
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907443"
---
# <a name="optimize-page-weight-in-sharepoint-online-modern-site-pages"></a><span data-ttu-id="1a7df-103">Optimiser le poids des pages de sites modernes SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a7df-103">Optimize page weight in SharePoint Online modern site pages</span></span>

<span data-ttu-id="1a7df-104">Les pages de sites modernes SharePoint Online contiennent du code sérialisé nécessaire pour restituer le contenu de la page, y compris les images, le texte, les objets dans la zone de contenu sous les barres de navigation/commandes et d’autres codes HTML qui constituent la structure de la page.</span><span class="sxs-lookup"><span data-stu-id="1a7df-104">SharePoint Online modern site pages contain serialized code that is required to render page content of the page, including images, text, objects in the content area underneath navigation/command bars and other HTML code that forms the framework of the page.</span></span> <span data-ttu-id="1a7df-105">Le poids de pages est une mesure de ce code HTML et doit être limitée afin de garantir des temps de chargement optimaux pour les pages.</span><span class="sxs-lookup"><span data-stu-id="1a7df-105">Page weight is a measurement of this HTML code, and should be limited to ensure optimal page load times.</span></span>

<span data-ttu-id="1a7df-106">Cet article vous permet de comprendre comment réduire le poids des pages de vos sites modernes.</span><span class="sxs-lookup"><span data-stu-id="1a7df-106">This article will help you understand how to reduce page weight in your modern site pages.</span></span>

>[!NOTE]
><span data-ttu-id="1a7df-107">Pour plus d’informations sur les performances dans les portails modernes SharePoint Online, consultez [Performances offertes par l’expérience moderne de SharePoint](/sharepoint/modern-experience-performance).</span><span class="sxs-lookup"><span data-stu-id="1a7df-107">For more information about performance in SharePoint Online modern portals, see [Performance in the modern SharePoint experience](/sharepoint/modern-experience-performance).</span></span>

## <a name="use-the-page-diagnostics-for-sharepoint-tool-to-analyze-page-weight"></a><span data-ttu-id="1a7df-108">Utiliser l’outil Diagnostic de page pour SharePoint pour analyser le poids des pages</span><span class="sxs-lookup"><span data-stu-id="1a7df-108">Use the Page Diagnostics for SharePoint tool to analyze page weight</span></span>

<span data-ttu-id="1a7df-109">L’outil Diagnostic de page pour SharePoint est une extension de navigateur pour le nouveau Microsoft Edge (https://www.microsoft.com/edge) et les navigateurs Chrome que vous pouvez utiliser pour analyser les pages de sites de publication SharePoint classiques et les portails modernes.</span><span class="sxs-lookup"><span data-stu-id="1a7df-109">The Page Diagnostics for SharePoint tool is a browser extension for the new Microsoft Edge (https://www.microsoft.com/edge) and Chrome browsers that analyzes both SharePoint Online modern portal and classic publishing site pages.</span></span> <span data-ttu-id="1a7df-110">L’outil fournit un rapport pour chaque page analysée montrant comment la page se comporte par rapport à un ensemble défini de critères de performance.</span><span class="sxs-lookup"><span data-stu-id="1a7df-110">The tool provides a report for each analyzed page showing how the page performs against a defined set of performance criteria.</span></span> <span data-ttu-id="1a7df-111">Pour installer et découvrir l’outil Diagnostic de page pour SharePoint, consultez [Utiliser l’outil Diagnostic de page pour SharePoint Online](page-diagnostics-for-spo.md).</span><span class="sxs-lookup"><span data-stu-id="1a7df-111">To install and learn about the Page Diagnostics for SharePoint tool, visit [Use the Page Diagnostics tool for SharePoint Online](page-diagnostics-for-spo.md).</span></span>

>[!NOTE]
><span data-ttu-id="1a7df-112">L’outil Diagnostic de page fonctionne uniquement pour SharePoint Online et ne peut pas être utilisé sur une page système SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1a7df-112">The Page Diagnostics tool only works for SharePoint Online, and cannot be used on a SharePoint system page.</span></span>

<span data-ttu-id="1a7df-113">Lorsque vous analysez une page de site SharePoint avec l’outil Diagnostic de page pour SharePoint, vous pouvez voir des informations sur la page dans les résultats **Poids de pages inférieur à 500 Ko** du volet _Tests de diagnostic_.</span><span class="sxs-lookup"><span data-stu-id="1a7df-113">When you analyze a SharePoint site page with the Page Diagnostics for SharePoint tool, you can see information about page in the **Page weight under 500KB** result of the _Diagnostic tests_ pane.</span></span> <span data-ttu-id="1a7df-114">Le résultat s’affiche en vert si le poids de la page est inférieur à la valeur de référence et rouge si le poids de la page dépasse la valeur de référence.</span><span class="sxs-lookup"><span data-stu-id="1a7df-114">The result will appear in green if the page weight is under the baseline value, and red if the page weight exceeds the baseline value.</span></span>

<span data-ttu-id="1a7df-115">Les résultats possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="1a7df-115">Possible results include:</span></span>

- <span data-ttu-id="1a7df-116">**Attention requise** (rouge) : le poids de la page dépasse 500 Ko</span><span class="sxs-lookup"><span data-stu-id="1a7df-116">**Attention required** (red): Page weight exceeds 500KB</span></span>
- <span data-ttu-id="1a7df-117">**Aucune action requise** (vert) : le poids de la page est inférieur à 500 Ko</span><span class="sxs-lookup"><span data-stu-id="1a7df-117">**No action required** (green): Page weight is under 500KB</span></span>

<span data-ttu-id="1a7df-118">Si le résultat **Poids de page inférieur à 500 Ko** apparaît dans la section **Attention requise**, vous pouvez cliquer sur le résultat pour afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="1a7df-118">If the **Page weight under 500KB** result appears in the **Attention required** section, you can click the result for details.</span></span>

![Résultats de requêtes à SharePoint](../media/modern-portal-optimization/pagediag-page-weight.png)

## <a name="remediate-page-weight-issues"></a><span data-ttu-id="1a7df-120">Résoudre les problèmes de poids de pages</span><span class="sxs-lookup"><span data-stu-id="1a7df-120">Remediate page weight issues</span></span>

<span data-ttu-id="1a7df-121">Si le poids des pages dépasse 500 Ko, vous pouvez améliorer le temps de chargement général des pages en réduisant le nombre de composants WebPart et en réduisant le contenu de la page dans la mesure appropriée.</span><span class="sxs-lookup"><span data-stu-id="1a7df-121">If page weight exceeds 500KB, you can improve overall page load time by reducing the number of web parts and limiting page content to an appropriate degree.</span></span>

<span data-ttu-id="1a7df-122">Les recommandations générales pour réduire le poids des pages incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1a7df-122">General guidance for reducing page weight includes:</span></span>

- <span data-ttu-id="1a7df-123">Limitez le contenu de la page à un volume raisonnable et utilisez plusieurs pages pour le contenu connexe.</span><span class="sxs-lookup"><span data-stu-id="1a7df-123">Limit the page content to a reasonable amount and use multiple pages for related content.</span></span>
- <span data-ttu-id="1a7df-124">Réduisez l’utilisation des composants WebPart comportant de grands conteneurs de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a7df-124">Minimize the use of web parts that have large property bags.</span></span>
- <span data-ttu-id="1a7df-125">Utilisez les vues cumulatives non interactives lorsque c’est possible.</span><span class="sxs-lookup"><span data-stu-id="1a7df-125">Use non-interactive rollup views when possible.</span></span>
- <span data-ttu-id="1a7df-126">Optimisez la taille des images en redimensionnant les images de façon appropriée en utilisant des formats d’images compressés et en vous assurant qu’elles sont téléchargées à partir d’un réseau de distribution de contenu.</span><span class="sxs-lookup"><span data-stu-id="1a7df-126">Optimize image sizes by sizing images appropriately, using compressed image formats and ensuring that they are downloaded from a CDN.</span></span>

<span data-ttu-id="1a7df-127">Vous trouverez des conseils supplémentaires pour limiter le poids des pages dans l’article suivant :</span><span class="sxs-lookup"><span data-stu-id="1a7df-127">You can find additional guidance for limiting page weight in the following article:</span></span>

- [<span data-ttu-id="1a7df-128">Optimiser les performances des pages dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="1a7df-128">Optimize page performance in SharePoint</span></span>](/sharepoint/dev/general-development/optimize-page-performance-in-sharepoint)

<span data-ttu-id="1a7df-129">Avant d’apporter des révisions de page pour résoudre les problèmes de performances, notez le temps de chargement des pages dans les résultats de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="1a7df-129">Before you make page revisions to remediate performance issues, make a note of the page load time in the analysis results.</span></span> <span data-ttu-id="1a7df-130">Exécutez à nouveau l’outil après votre révision pour déterminer si le nouveau résultat est inclus dans la norme de référence et vérifier le nouveau temps de chargement des pages pour voir s’il y a eu une amélioration.</span><span class="sxs-lookup"><span data-stu-id="1a7df-130">Run the tool again after your revision to see if the new result is within the baseline standard, and check the new page load time to see if there was an improvement.</span></span>

![Résultats du temps de chargement des pages](../media/modern-portal-optimization/pagediag-page-load-time.png)

>[!NOTE]
><span data-ttu-id="1a7df-132">Le temps de chargement des pages peut varier en fonction de nombreux facteurs tels que la charge réseau, l’heure de la journée et d’autres conditions transitoires.</span><span class="sxs-lookup"><span data-stu-id="1a7df-132">Page load time can vary based on a variety of factors such as network load, time of day, and other transient conditions.</span></span> <span data-ttu-id="1a7df-133">Vous devez tester le temps de chargement des pages plusieurs fois avant et après avoir apporté des modifications pour vous aider à faire la moyenne des résultats.</span><span class="sxs-lookup"><span data-stu-id="1a7df-133">You should test page load time a few times before and after making changes to help you average the results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a7df-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a7df-134">Related topics</span></span>

[<span data-ttu-id="1a7df-135">Optimisation des performances SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a7df-135">Tune SharePoint Online performance</span></span>](tune-sharepoint-online-performance.md)

[<span data-ttu-id="1a7df-136">Optimisation des performances Office 365</span><span class="sxs-lookup"><span data-stu-id="1a7df-136">Tune Office 365 performance</span></span>](tune-microsoft-365-performance.md)

[<span data-ttu-id="1a7df-137">Performances offertes par l’expérience moderne de SharePoint</span><span class="sxs-lookup"><span data-stu-id="1a7df-137">Performance in the modern SharePoint experience</span></span>](/sharepoint/modern-experience-performance)

[<span data-ttu-id="1a7df-138">Réseaux de distribution de contenu</span><span class="sxs-lookup"><span data-stu-id="1a7df-138">Content delivery networks</span></span>](content-delivery-networks.md)

[<span data-ttu-id="1a7df-139">Utilisation du réseau de distribution de contenu Office 365 avec SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a7df-139">Use the Office 365 Content Delivery Network (CDN) with SharePoint Online</span></span>](use-microsoft-365-cdn-with-spo.md)