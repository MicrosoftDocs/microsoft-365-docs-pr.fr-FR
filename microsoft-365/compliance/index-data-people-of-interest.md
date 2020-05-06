---
title: Indexation avancée des données pour une enquête
f1.keywords:
- NOCSH
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
description: Découvrez comment utiliser l’indexation avancée pour vous assurer que votre recherche capture toutes les données que vous souhaitez analyser.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: dc7d73c233aa48b88e9dce32fad613ccc5e19333
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035060"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a><span data-ttu-id="81025-103">Indexation avancée des données pour une enquête</span><span class="sxs-lookup"><span data-stu-id="81025-103">Advanced indexing of data for an investigation</span></span>

<span data-ttu-id="81025-104">Le contenu du système réel peut être partiellement indexé pour plusieurs raisons, notamment l’existence d’images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d’indexation sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="81025-104">Content in the live system can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span> <span data-ttu-id="81025-105">Lorsque vous traitez des données à risque élevé, vous devez vous assurer que votre recherche a capturé toutes les données que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="81025-105">When you are dealing with high risk data spill, you want to make sure that your search captured all data that you want to investigate.</span></span> <span data-ttu-id="81025-106">Lorsqu’une personne concernée est ajoutée à une enquête de données, tout contenu considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.</span><span class="sxs-lookup"><span data-stu-id="81025-106">When a person of interest is added to a Data investigation, any content that was deemed as partially indexed is re-processed to make it fully searchable.</span></span> <span data-ttu-id="81025-107">Ce processus est appelé *indexation avancée*.</span><span class="sxs-lookup"><span data-stu-id="81025-107">This process is called *Advanced indexing*.</span></span> 

<span data-ttu-id="81025-108">Pour en savoir plus sur le traitement de la prise en charge et des éléments partiellement indexés, voir :</span><span class="sxs-lookup"><span data-stu-id="81025-108">To learn more about processing support and partially indexed items, see:</span></span>

- [<span data-ttu-id="81025-109">Types de fichiers pris en charge dans les enquêtes de données</span><span class="sxs-lookup"><span data-stu-id="81025-109">Supported file types in Data Investigations</span></span>](supported-filetypes-datainvestigations.md)

- [<span data-ttu-id="81025-110">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="81025-110">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)

- [<span data-ttu-id="81025-111">Formats de fichier indexés par le service de recherche Exchange</span><span class="sxs-lookup"><span data-stu-id="81025-111">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [<span data-ttu-id="81025-112">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="81025-112">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="81025-113">Affichage des résultats de l’indexation avancée</span><span class="sxs-lookup"><span data-stu-id="81025-113">Viewing Advanced indexing results</span></span>

<span data-ttu-id="81025-114">Une fois le processus d’indexation avancé terminé, vous pouvez comprendre l’efficacité du nouveau traitement.</span><span class="sxs-lookup"><span data-stu-id="81025-114">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="81025-115">Dans l’affichage indexation des personnes à intérêt, le graphique répertorie tous les éléments ajoutés à l' *index hybride*.</span><span class="sxs-lookup"><span data-stu-id="81025-115">In the People of interest indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="81025-116">L’index hybride permet aux enquêtes de données (préversion) de stocker le contenu retraité.</span><span class="sxs-lookup"><span data-stu-id="81025-116">The hybrid index is where Data Investigations (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="81025-117">Le graphique inclut également le nombre d’éléments nécessitant une correction et un autre graphique d’erreurs par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="81025-117">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="81025-118">Pour plus d’informations, consultez la rubrique [erreur de correction lors du traitement des données](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="81025-118">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-people-of-interest"></a><span data-ttu-id="81025-119">Mise à jour des index avancés pour les personnes concernées</span><span class="sxs-lookup"><span data-stu-id="81025-119">Updating Advanced indexes for people of interest</span></span>

<span data-ttu-id="81025-120">Lorsqu’une personne d’intérêt est ajoutée à une enquête de données, tous les éléments partiellement indexés sont retraités.</span><span class="sxs-lookup"><span data-stu-id="81025-120">When a person of interest is added to a data investigation, all partially indexed items are re-processed.</span></span> <span data-ttu-id="81025-121">Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81025-121">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="81025-122">Si nécessaire, vous pouvez mettre à jour les index.</span><span class="sxs-lookup"><span data-stu-id="81025-122">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="81025-123">La mise à jour des index de personnes d’intérêt est un processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="81025-123">Updating people of interest indexes is a long running process.</span></span> <span data-ttu-id="81025-124">Il est recommandé de ne pas mettre à jour les index plus d’une fois par jour dans une enquête.</span><span class="sxs-lookup"><span data-stu-id="81025-124">It's recommended that you don't update indexes more than once per day in an investigation.</span></span>
