---
title: Ajouter des données d’un ensemble de révision à un autre ensemble de révision
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
description: Découvrez comment sélectionner des documents dans un ensemble de validation et les utiliser individuellement dans un autre ensemble dans un cas avancé eDiscovery.
ms.custom:
- seo-marvel-mar2020
- seo-marvel-apr2020
ms.openlocfilehash: 433e59629ec40dbdf66b8daf6437ce84e41a3a33
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44818601"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="df869-103">Ajouter des données à un jeu de révision à partir d’un autre ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="df869-103">Add data to a review set from another review set</span></span>

<span data-ttu-id="df869-104">Dans certains cas, il peut s’avérer nécessaire de sélectionner des documents dans un ensemble de révision et de les utiliser individuellement dans un autre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="df869-104">In some cases, it may be necessary to select documents from one review set and work with them individually in another review set.</span></span> <span data-ttu-id="df869-105">Ceci est particulièrement utile si vous avez consulté du contenu dans un jeu de révision et que vous souhaitez exécuter des analyses sur le sous-ensemble de données.</span><span class="sxs-lookup"><span data-stu-id="df869-105">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="df869-106">Suivez le flux de travail de cet article pour ajouter du contenu d’un jeu de révision à un autre.</span><span class="sxs-lookup"><span data-stu-id="df869-106">Follow the workflow in this article to add content from one review set to another.</span></span>

## <a name="create-a-review-set"></a><span data-ttu-id="df869-107">Créer un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="df869-107">Create a review set</span></span>

<span data-ttu-id="df869-108">Avant de commencer, vous devez créer un jeu de révision pour y ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="df869-108">Before you start, you'll need to create a review set to add the data to.</span></span>  <span data-ttu-id="df869-109">Un nouvel ensemble de révision peut être ajouté sous l’onglet **ensembles de révision** de la case.</span><span class="sxs-lookup"><span data-stu-id="df869-109">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="df869-110">Pour plus d’informations, consultez [la rubrique Create a Review Set](managing-review-sets.md#create-a-review-set).</span><span class="sxs-lookup"><span data-stu-id="df869-110">For more information, see [Create a review set](managing-review-sets.md#create-a-review-set).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="df869-111">Étape 1 : identifier le contenu à ajouter à un autre ensemble de validation</span><span class="sxs-lookup"><span data-stu-id="df869-111">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="df869-112">Vous pouvez ajouter du contenu d’un ensemble de réexamen à un autre en sélectionnant des documents spécifiques dans le jeu de révision source ou en sélectionnant tous les éléments renvoyés par la requête de jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="df869-112">You can add content from one review set to another one by selecting specific documents in the source review set or by selecting all items returned by review set query.</span></span> <span data-ttu-id="df869-113">Si vous ajoutez des éléments sélectionnés, sélectionnez-les, sélectionnez **action**, puis **Ajouter à un autre ensemble de réexamen**.</span><span class="sxs-lookup"><span data-stu-id="df869-113">If you're adding selected items, select the items, select **Action**, and then select **Add to another review set**.</span></span>

![Ajouter à un autre ensemble de révision](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="df869-115">Étape 2 : spécification des options d’ajout à un autre ensemble de réexamen</span><span class="sxs-lookup"><span data-stu-id="df869-115">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="df869-116">Dans la page de menu **Ajouter à un autre jeu de réviseur options** , choisissez l’ensemble de révision auquel vous souhaitez ajouter les éléments.</span><span class="sxs-lookup"><span data-stu-id="df869-116">In the **Add to another review set options** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="df869-117">Indiquez si vous souhaitez ajouter **tous les résultats de recherche ou les** **éléments sélectionnés**.</span><span class="sxs-lookup"><span data-stu-id="df869-117">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="df869-118">**Informations supplémentaires** fournit des options permettant d’inclure toutes les métadonnées des éléments et d’inclure les balises (en activant la case à cocher **étiquettes** ) à partir de l’ensemble de révision source lorsque les documents sont ajoutés au nouvel ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="df869-118">**Additional information** provides options to include all metadata from the items and whether to include the tags (by selecting the **Labels** check box) from the source review set when the documents are added to the new review set.</span></span>  

![Ajouter à un autre ensemble de révision](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

<span data-ttu-id="df869-120">Une fois que vous avez cliqué sur **OK**, un nouveau travail (nommé **Ajout de données à un autre ensemble de vérification**) est créé pour ajouter le contenu à un autre ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="df869-120">After you click **Ok**, a new job (named **Adding data to another review set**) is created to add the content to another review set.</span></span> <span data-ttu-id="df869-121">Vous pouvez accéder à l’onglet **travaux** et surveiller la progression de ce travail.</span><span class="sxs-lookup"><span data-stu-id="df869-121">You can go to the **Jobs** tab and monitor the progress of this job.</span></span> <span data-ttu-id="df869-122">Pour plus d’informations, consultez la rubrique [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="df869-122">For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>
