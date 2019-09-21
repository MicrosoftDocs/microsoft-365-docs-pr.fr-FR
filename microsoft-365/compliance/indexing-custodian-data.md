---
title: Indexation avancée des données des consignataires
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ba85ef90570dfbf2228148bf5211a4b041a1cb61
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078454"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="3ead4-102">Indexation avancée des données des consignataires</span><span class="sxs-lookup"><span data-stu-id="3ead4-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="3ead4-103">Lorsqu’un dépositaire est ajouté à un cas avancé de découverte électronique, tout contenu dans Office 365 considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.</span><span class="sxs-lookup"><span data-stu-id="3ead4-103">When a custodian is added to an Advanced eDiscovery case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.</span></span>  <span data-ttu-id="3ead4-104">Ce processus est appelé *indexation avancée*.</span><span class="sxs-lookup"><span data-stu-id="3ead4-104">This process is called *Advanced indexing*.</span></span> <span data-ttu-id="3ead4-105">Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l’existence d’images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d’indexation sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="3ead4-105">Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span>

<span data-ttu-id="3ead4-106">Pour en savoir plus sur le traitement de la prise en charge dans Office 365 et les éléments partiellement indexés, voir :</span><span class="sxs-lookup"><span data-stu-id="3ead4-106">To learn more about processing support in Office 365 and partially indexed items, see:</span></span>

- [<span data-ttu-id="3ead4-107">Types de fichiers pris en charge dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="3ead4-107">Supported file types in Advanced eDiscovery</span></span>](supported-filetypes-ediscovery20.md)
- [<span data-ttu-id="3ead4-108">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3ead4-108">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
- [<span data-ttu-id="3ead4-109">Formats de fichier indexés par le service de recherche Exchange</span><span class="sxs-lookup"><span data-stu-id="3ead4-109">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [<span data-ttu-id="3ead4-110">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="3ead4-110">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="3ead4-111">Affichage des résultats de l’indexation avancée</span><span class="sxs-lookup"><span data-stu-id="3ead4-111">Viewing Advanced indexing results</span></span>

<span data-ttu-id="3ead4-112">Une fois le processus d’indexation avancé terminé, vous pouvez comprendre l’efficacité du nouveau traitement.</span><span class="sxs-lookup"><span data-stu-id="3ead4-112">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="3ead4-113">Dans la vue d’indexation dépositaire, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.</span><span class="sxs-lookup"><span data-stu-id="3ead4-113">In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="3ead4-114">L’index hybride est l’emplacement où eDiscovery avancée stocke le contenu retraité.</span><span class="sxs-lookup"><span data-stu-id="3ead4-114">The hybrid index is where Advanced eDiscovery stores the re-processed content.</span></span>

<span data-ttu-id="3ead4-115">Le graphique inclut également le nombre d’éléments nécessitant une correction et un autre graphique d’erreurs par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="3ead4-115">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="3ead4-116">Pour plus d’informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="3ead4-116">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="3ead4-117">Mise à jour des index avancés pour les dépositaires</span><span class="sxs-lookup"><span data-stu-id="3ead4-117">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="3ead4-118">Lorsqu’un dépositaire est ajouté à un cas avancé eDiscovery, tous les éléments partiellement indexés sont retraités.</span><span class="sxs-lookup"><span data-stu-id="3ead4-118">When a custodian is added to an Advanced eDiscovery case, all partially indexed items are re-processed.</span></span> <span data-ttu-id="3ead4-119">Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ead4-119">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="3ead4-120">Si nécessaire, vous pouvez mettre à jour les index.</span><span class="sxs-lookup"><span data-stu-id="3ead4-120">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="3ead4-121">La mise à jour des index de dépositaire est un processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="3ead4-121">Updating custodian indexes is a long running process.</span></span> <span data-ttu-id="3ead4-122">Il est recommandé de ne pas mettre à jour les index plus d’une fois par jour dans un cas.</span><span class="sxs-lookup"><span data-stu-id="3ead4-122">It's recommended that you don't update indexes more than once per day in a case.</span></span>
