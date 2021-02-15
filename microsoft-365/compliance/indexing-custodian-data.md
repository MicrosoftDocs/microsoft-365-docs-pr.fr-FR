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
description: Lorsqu’un dépositaire est ajouté à un cas Advanced eDiscovery, tout contenu considéré comme partiellement indexé est réprocessé pour le rendre entièrement utilisable dans une recherche.
ms.openlocfilehash: 908d01cacc103639e1f9efe965240c33a5296ba9
ms.sourcegitcommit: 98b889e674ad1d5fa37d4b6c5fc3eda60a1d67f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49750755"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="aab4a-103">Indexation avancée des données des consignataires</span><span class="sxs-lookup"><span data-stu-id="aab4a-103">Advanced indexing of custodian data</span></span>

<span data-ttu-id="aab4a-104">Lorsqu’un dépositaire est ajouté à un cas Advanced eDiscovery, tout contenu considéré comme partiellement indexé est réprocessé pour le rendre entièrement utilisable dans une recherche.</span><span class="sxs-lookup"><span data-stu-id="aab4a-104">When a custodian is added to an Advanced eDiscovery case, any content that was deemed as partially indexed is reprocessed to make it fully searchable.</span></span>  <span data-ttu-id="aab4a-105">Ce processus est appelé *indexation avancée.*</span><span class="sxs-lookup"><span data-stu-id="aab4a-105">This process is called *Advanced indexing*.</span></span> <span data-ttu-id="aab4a-106">Le contenu peut être partiellement indexé pour plusieurs raisons, notamment l’existence d’images, de types de fichiers non pris en compte ou lorsque des limites de taille de fichier d’indexation sont rencontrées.</span><span class="sxs-lookup"><span data-stu-id="aab4a-106">Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span>

<span data-ttu-id="aab4a-107">Pour en savoir plus sur le traitement de la prise en charge et des éléments partiellement indexés, voir :</span><span class="sxs-lookup"><span data-stu-id="aab4a-107">To learn more about processing support and partially indexed items, see:</span></span>

- [<span data-ttu-id="aab4a-108">Types de fichiers pris en charge dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="aab4a-108">Supported file types in Advanced eDiscovery</span></span>](supported-filetypes-ediscovery20.md)

- [<span data-ttu-id="aab4a-109">Éléments partiellement indexés dans la recherche de contenu dans Office 365</span><span class="sxs-lookup"><span data-stu-id="aab4a-109">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)

- [<span data-ttu-id="aab4a-110">Formats de fichier indexés par le service de recherche Exchange</span><span class="sxs-lookup"><span data-stu-id="aab4a-110">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [<span data-ttu-id="aab4a-111">Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="aab4a-111">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="aab4a-112">Affichage des résultats de l’indexation avancée</span><span class="sxs-lookup"><span data-stu-id="aab4a-112">Viewing Advanced indexing results</span></span>

<span data-ttu-id="aab4a-113">Une fois le processus d’indexation avancé terminé, vous pouvez comprendre l’efficacité du nouveau traitement.</span><span class="sxs-lookup"><span data-stu-id="aab4a-113">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of reprocessing.</span></span>  <span data-ttu-id="aab4a-114">Dans l’affichage Des résultats  d’indexation avancée sous l’onglet Traitement d’un cas, le graphique répertorie le nombre d’éléments ajoutés à *l’index hybride.*</span><span class="sxs-lookup"><span data-stu-id="aab4a-114">In the Advanced indexing results view on the **Processing** tab for a case, the graph lists the number of items added to the *hybrid index*.</span></span>  <span data-ttu-id="aab4a-115">L’index hybride est l’endroit où Advanced eDiscovery stocke le contenu réprocessé.</span><span class="sxs-lookup"><span data-stu-id="aab4a-115">The hybrid index is where Advanced eDiscovery stores the reprocessed content.</span></span>

<span data-ttu-id="aab4a-116">Cette vue inclut également le nombre d’éléments qui nécessitent une correction et un autre graphique d’erreurs par type de fichier.</span><span class="sxs-lookup"><span data-stu-id="aab4a-116">This view  also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="aab4a-117">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="aab4a-117">For more information, see:</span></span>

- [<span data-ttu-id="aab4a-118">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="aab4a-118">Error remediation when processing data</span></span>](error-remediation-when-processing-data-in-advanced-ediscovery.md)

- [<span data-ttu-id="aab4a-119">Correction d’erreur sur élément unique</span><span class="sxs-lookup"><span data-stu-id="aab4a-119">Single item error remediation</span></span>](single-item-error-remediation.md)

## <a name="updating-the-advanced-index-for-custodians"></a><span data-ttu-id="aab4a-120">Mise à jour de l’index avancé pour les dépositaires</span><span class="sxs-lookup"><span data-stu-id="aab4a-120">Updating the Advanced index for custodians</span></span>

<span data-ttu-id="aab4a-121">Lorsqu’un dépositaire est ajouté à un cas Advanced eDiscovery, tous les éléments partiellement indexés sont retraités.</span><span class="sxs-lookup"><span data-stu-id="aab4a-121">When a custodian is added to an Advanced eDiscovery case, all partially indexed items are reprocessed.</span></span> <span data-ttu-id="aab4a-122">Toutefois, au fil du temps, des éléments partiellement indexés peuvent être ajoutés à la boîte aux lettres ou au compte OneDrive d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aab4a-122">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="aab4a-123">Si nécessaire, vous pouvez mettre à jour l’index pour un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="aab4a-123">If necessary, you can update the index for specific custodian.</span></span> <span data-ttu-id="aab4a-124">Pour plus d’informations, [voir Gérer les dépositaires dans un cas Advanced eDiscovery.](manage-new-custodians.md#re-index-custodian-data)</span><span class="sxs-lookup"><span data-stu-id="aab4a-124">For more information, see [Manage custodians in an Advanced eDiscovery case](manage-new-custodians.md#re-index-custodian-data).</span></span> <span data-ttu-id="aab4a-125">Vous pouvez également mettre à jour l’index pour tous les dépositaires dans un cas en cliquant sur **l’index** de mise à jour sous **l’onglet Traitement.**</span><span class="sxs-lookup"><span data-stu-id="aab4a-125">You can also update the index for all custodians in a case by clicking the **Update index** on the **Processing** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="aab4a-126">La mise à jour des index des dépositaires est un processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="aab4a-126">Updating custodian indexes is a long running process.</span></span> <span data-ttu-id="aab4a-127">Il est recommandé de ne pas mettre à jour les index plus d’une fois par jour dans un cas.</span><span class="sxs-lookup"><span data-stu-id="aab4a-127">It's recommended that you don't update indexes more than once a day in a case.</span></span>
