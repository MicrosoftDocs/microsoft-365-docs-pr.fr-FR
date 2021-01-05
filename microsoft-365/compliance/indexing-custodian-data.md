---
title: Indexation avancée des données des consignataires
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
description: Lorsqu’un dépositaire est ajouté à un cas avancé de découverte électronique, tout contenu considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.
ms.openlocfilehash: 908d01cacc103639e1f9efe965240c33a5296ba9
ms.sourcegitcommit: 98b889e674ad1d5fa37d4b6c5fc3eda60a1d67f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49750755"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="8455e-103">Indexation avancée des données des consignataires</span><span class="sxs-lookup"><span data-stu-id="8455e-103">Advanced indexing of custodian data</span></span>

<span data-ttu-id="8455e-104">Lorsqu’un dépositaire est ajouté à un cas avancé de découverte électronique, tout contenu considéré comme partiellement indexé est retraité afin de le faire entièrement chercher.</span><span class="sxs-lookup"><span data-stu-id="8455e-104">When a custodian is added to an Advanced eDiscovery case, any content that was deemed as partially indexed is reprocessed to make it fully searchable.</span></span>  <span data-ttu-id="8455e-105">Ce processus est appelé *indexation avancée*.</span><span class="sxs-lookup"><span data-stu-id="8455e-105">This process is called *Advanced indexing*.</span></span> <span data-ttu-id="8455e-106">Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l’existence d’images, de types de fichiers non pris en charge ou lorsque des limites de taille de fichier d’indexation sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="8455e-106">Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span>

<span data-ttu-id="8455e-107">Pour en savoir plus sur le traitement de la prise en charge et des éléments partiellement indexés, voir :</span><span class="sxs-lookup"><span data-stu-id="8455e-107">To learn more about processing support and partially indexed items, see:</span></span>

- [<span data-ttu-id="8455e-108">Types de fichiers pris en charge dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8455e-108">Supported file types in Advanced eDiscovery</span></span>](supported-filetypes-ediscovery20.md)

- [<span data-ttu-id="8455e-109">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="8455e-109">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)

- [<span data-ttu-id="8455e-110">Formats de fichier indexés par le service de recherche Exchange</span><span class="sxs-lookup"><span data-stu-id="8455e-110">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [<span data-ttu-id="8455e-111">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="8455e-111">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="8455e-112">Affichage des résultats de l’indexation avancée</span><span class="sxs-lookup"><span data-stu-id="8455e-112">Viewing Advanced indexing results</span></span>

<span data-ttu-id="8455e-113">Une fois le processus d’indexation avancé terminé, vous pouvez comprendre l’efficacité du retraitement.</span><span class="sxs-lookup"><span data-stu-id="8455e-113">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of reprocessing.</span></span>  <span data-ttu-id="8455e-114">Dans l’affichage des résultats d’indexation avancés, sous l’onglet **traitement** d’un cas, le graphique indique le nombre d’éléments ajoutés à l' *index hybride*.</span><span class="sxs-lookup"><span data-stu-id="8455e-114">In the Advanced indexing results view on the **Processing** tab for a case, the graph lists the number of items added to the *hybrid index*.</span></span>  <span data-ttu-id="8455e-115">L’index hybride est l’emplacement où la découverte électronique avancée stocke le contenu retraité.</span><span class="sxs-lookup"><span data-stu-id="8455e-115">The hybrid index is where Advanced eDiscovery stores the reprocessed content.</span></span>

<span data-ttu-id="8455e-116">Cette vue inclut également le nombre d’éléments nécessitant une correction et un autre graphique d’erreurs par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="8455e-116">This view  also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="8455e-117">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="8455e-117">For more information, see:</span></span>

- [<span data-ttu-id="8455e-118">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="8455e-118">Error remediation when processing data</span></span>](error-remediation-when-processing-data-in-advanced-ediscovery.md)

- [<span data-ttu-id="8455e-119">Correction d’erreur sur élément unique</span><span class="sxs-lookup"><span data-stu-id="8455e-119">Single item error remediation</span></span>](single-item-error-remediation.md)

## <a name="updating-the-advanced-index-for-custodians"></a><span data-ttu-id="8455e-120">Mise à jour de l’index avancé pour les dépositaires</span><span class="sxs-lookup"><span data-stu-id="8455e-120">Updating the Advanced index for custodians</span></span>

<span data-ttu-id="8455e-121">Lorsqu’un dépositaire est ajouté à un cas avancé eDiscovery, tous les éléments partiellement indexés sont retraités.</span><span class="sxs-lookup"><span data-stu-id="8455e-121">When a custodian is added to an Advanced eDiscovery case, all partially indexed items are reprocessed.</span></span> <span data-ttu-id="8455e-122">Toutefois, dans le temps, des éléments indexés plus partiellement peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8455e-122">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="8455e-123">Si nécessaire, vous pouvez mettre à jour l’index pour un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="8455e-123">If necessary, you can update the index for specific custodian.</span></span> <span data-ttu-id="8455e-124">Pour plus d’informations, consultez la rubrique [Manage dépositaires in an Advanced eDiscovery case](manage-new-custodians.md#re-index-custodian-data).</span><span class="sxs-lookup"><span data-stu-id="8455e-124">For more information, see [Manage custodians in an Advanced eDiscovery case](manage-new-custodians.md#re-index-custodian-data).</span></span> <span data-ttu-id="8455e-125">Vous pouvez également mettre à jour l’index de tous les dépositaires dans un cas en cliquant sur l' **index de mise à jour** sous l’onglet **traitement** .</span><span class="sxs-lookup"><span data-stu-id="8455e-125">You can also update the index for all custodians in a case by clicking the **Update index** on the **Processing** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="8455e-126">La mise à jour des index de dépositaire est un processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="8455e-126">Updating custodian indexes is a long running process.</span></span> <span data-ttu-id="8455e-127">Il est recommandé de ne pas mettre à jour les index plus d’une fois par jour dans un cas.</span><span class="sxs-lookup"><span data-stu-id="8455e-127">It's recommended that you don't update indexes more than once a day in a case.</span></span>
