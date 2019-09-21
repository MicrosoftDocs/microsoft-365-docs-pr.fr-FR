---
title: Ajouter des données d’un ensemble de révision à un autre ensemble de révision
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
ms.openlocfilehash: bd33d57380e99225d741b9c38677c2b49694139a
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078982"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="0cb57-102">Ajouter des données à un jeu de révision à partir d’un autre ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="0cb57-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="0cb57-103">Dans certains cas, il peut s’avérer nécessaire de supprimer une partie des documents d’un ensemble de révision et de les utiliser individuellement dans un autre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0cb57-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="0cb57-104">Ceci est particulièrement utile si vous avez consulté du contenu dans un jeu de révision et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.</span><span class="sxs-lookup"><span data-stu-id="0cb57-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="0cb57-105">Suivez le flux de travail de cet article pour ajouter du contenu d’un jeu de révision à un autre.</span><span class="sxs-lookup"><span data-stu-id="0cb57-105">Follow the workflow in this article to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0cb57-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0cb57-106">Before you begin</span></span>

<span data-ttu-id="0cb57-107">Avant de commencer, vous devez créer un nouveau jeu de révision auquel ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="0cb57-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="0cb57-108">Un nouvel ensemble de révision peut être ajouté sous l’onglet **ensembles de révision** de la case.</span><span class="sxs-lookup"><span data-stu-id="0cb57-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="0cb57-109">Pour plus d’informations, consultez [la rubrique Create a Review Set](managing-review-sets.md#create-a-review-set).</span><span class="sxs-lookup"><span data-stu-id="0cb57-109">For more information, see [Create a review set](managing-review-sets.md#create-a-review-set).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="0cb57-110">Étape 1 : identifier le contenu à ajouter à un autre ensemble de validation</span><span class="sxs-lookup"><span data-stu-id="0cb57-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="0cb57-111">Vous pouvez ajouter du contenu d’un jeu de réexamen à un autre en sélectionnant des documents spécifiques dans le jeu de révision source ou b seleting tous les éléments renvoyés par la requête Set Review.</span><span class="sxs-lookup"><span data-stu-id="0cb57-111">You can add content from one review set to another one by selecting specific documents in the source review set or b seleting all items returned by review set query.</span></span>  <span data-ttu-id="0cb57-112">Si vous ajoutez des éléments sélectionnés, sélectionnez-les, cliquez sur **action**, puis sur **Ajouter à un autre ensemble de réexamen**.</span><span class="sxs-lookup"><span data-stu-id="0cb57-112">If you're adding selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Ajouter à un autre ensemble de révision](media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="0cb57-114">Étape 2 : spécification des options d’ajout à un autre ensemble de réexamen</span><span class="sxs-lookup"><span data-stu-id="0cb57-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="0cb57-115">Dans la page de menu **Ajouter à un autre jeu de réviseur options** , choisissez l’ensemble de révision auquel vous souhaitez ajouter les éléments.</span><span class="sxs-lookup"><span data-stu-id="0cb57-115">In the **Add to another review set options** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="0cb57-116">Indiquez si vous souhaitez ajouter **tous les résultats de recherche ou les** **éléments sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="0cb57-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="0cb57-117">Informations supplémentaires fournit des options permettant d’inclure toutes les métadonnées des éléments et d’inclure les balises (en activant la case à cocher **étiquettes** ) à partir de l’ensemble de révision source lorsque les documents sont ajoutés au nouvel ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0cb57-117">Additional information provides options to include all metadata from the items and whether to include the tags (by selecting the **Labels** checkbox) from the source review set when the documents are added to the new review set.</span></span>  

![Ajouter à un autre ensemble de révision](media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

<span data-ttu-id="0cb57-119">Une fois que vous avez cliqué sur **OK**, un nouveau travail (nommé **Ajout de données à un autre ensemble de vérification**) est créé pour ajouter le contenu à un autre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0cb57-119">After you click **Ok**, a new job (named **Adding data to another review set**) is created to add the content to a another review set.</span></span>  <span data-ttu-id="0cb57-120">Vous pouvez accéder à l’onglet **travaux** et surveiller la progression de ce travail.</span><span class="sxs-lookup"><span data-stu-id="0cb57-120">You can go to **Jobs** tab and monitor the progress of this job.</span></span> <span data-ttu-id="0cb57-121">Pour plus d’informations, consultez la rubrique [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="0cb57-121">For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>
