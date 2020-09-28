---
title: Utilisation de la taxonomie de magasin de termes lors de la création d’un extracteur
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 10/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Utiliser la taxonomie de magasin de termes lors de la création d’un extracteur dans votre modèle de présentation de document dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 94f7a0389d2f06e0f8c1a60a341a02e43dfb2071
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295861"
---
# <a name="leverage-term-store-taxonomy-when-creating-an-extractor"></a><span data-ttu-id="7ac11-103">Utilisation de la taxonomie de magasin de termes lors de la création d’un extracteur</span><span class="sxs-lookup"><span data-stu-id="7ac11-103">Leverage term store taxonomy when creating an extractor</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSoL]

</br>

<span data-ttu-id="7ac11-104">Lorsque vous créez un extracteur dans votre modèle de présentation de document dans SharePoint Syntex, vous pouvez tirer parti de la taxonomie de magasin de termes [services de métadonnées gérées](https://docs.microsoft.com/sharepoint/managed-metadata#terms) pour afficher les termes préférés des données que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="7ac11-104">When you create an extractor in your document understanding model in SharePoint Syntex, you can take advantage of [Managed Metadata services](https://docs.microsoft.com/sharepoint/managed-metadata#terms) term store taxonomy to display preferred terms for data that you extract.</span></span>  

<span data-ttu-id="7ac11-105">Par exemple, votre modèle identifie et classe tous les documents de **contrat** téléchargés vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="7ac11-105">As an example, your model identifies and classifies all **Contract** documents that are uploaded to the document library.</span></span>  <span data-ttu-id="7ac11-106">En outre, le modèle extrait également une valeur de **service de contrat** de chaque contrat et l’affiche dans une colonne de votre vue de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7ac11-106">Additionally, the model also extracts a **Contract Service** value from each contract, and will display it in a column in your library view.</span></span> <span data-ttu-id="7ac11-107">Parmi les différentes valeurs de services contractuels dans les contrats, il existe plusieurs valeurs plus anciennes que votre société n’utilise plus et qui ont été renommées.</span><span class="sxs-lookup"><span data-stu-id="7ac11-107">Among the various Contract Services values in the contracts, there are several older values that your company no longer uses and have been renamed.</span></span> <span data-ttu-id="7ac11-108">Par exemple, toutes les références à la *conception*des termes, aux *graphiques*ou aux services contractuels *topographiques* doivent maintenant être nommées *Creative*.</span><span class="sxs-lookup"><span data-stu-id="7ac11-108">For example, all references to the terms *Design*, *Graphics*, or *Topography* contract services should now be called *Creative*.</span></span> <span data-ttu-id="7ac11-109">Chaque fois que votre modèle extrait l’un des termes obsolètes d’un document de contrat, vous voulez qu’il affiche le terme « Creative » dans votre vue de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7ac11-109">Whenever your model extracts one of the outdated terms from a contract document, you want it to display the current term - Creative - in your library view.</span></span> <span data-ttu-id="7ac11-110">Dans l’exemple ci-dessous, lors de la formation du modèle, nous voyons qu’un exemple de document contient le terme de *conception*obsolète.</span><span class="sxs-lookup"><span data-stu-id="7ac11-110">In the example below, while training the model we see that one sample document contains the outdated term of *Design*.</span></span>

   ![Banque de termes](../media/content-understanding/design.png)</br>


## <a name="term-set-synonyms"></a><span data-ttu-id="7ac11-112">Synonymes de l’ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="7ac11-112">Term set synonyms</span></span> 

<span data-ttu-id="7ac11-113">Les ensembles de termes sont configurés dans le magasin de termes services de métadonnées gérées dans le centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7ac11-113">Term sets are configured in the Managed Metadata services term store in the SharePoint admin center.</span></span> <span data-ttu-id="7ac11-114">Dans l’exemple ci-dessous, l' [ensemble de termes](https://docs.microsoft.com/sharepoint/managed-metadata#term-set) *services contractuel* est configuré pour inclure un certain nombre de termes, y compris *Creative*.</span><span class="sxs-lookup"><span data-stu-id="7ac11-114">In the the example below, the *Contract Services* [term set](https://docs.microsoft.com/sharepoint/managed-metadata#term-set) is configured to include a number of terms, including *Creative*.</span></span>  <span data-ttu-id="7ac11-115">Les détails s’affichent pour indiquer que le terme a trois synonymes (*conception*, *graphiques*et *topographie*) et que les synonymes doivent être traduits en *éléments créatifs*.</span><span class="sxs-lookup"><span data-stu-id="7ac11-115">The details for it show that the term has three synonyms (*Design*, *Graphics*, and *Topography*) and the synonyms should be translated to *Creative*.</span></span>

   ![Ensemble de termes](../media/content-understanding/term-store.png)</br>

<span data-ttu-id="7ac11-117"><Mike, je ne sais pas comment le décrire.</span><span class="sxs-lookup"><span data-stu-id="7ac11-117"><Mike, here is where I am unsure about how to describe this.</span></span>  <span data-ttu-id="7ac11-118">Quelle action indique au modèle que lors de la création d’un extracteur pour extraire et afficher une colonne services de contrat, comment cette colonne est-elle « marquée » pour utiliser l’ensemble de termes de métadonnées gérées pour les services Creative ? ></span><span class="sxs-lookup"><span data-stu-id="7ac11-118">What action tells the model that when I create an extractor to extract and display a Contract Services column, how is that column "marked" to use the managed metadata term set for Creative Services?></span></span>

## <a name="configure-your-document-library-site-column-for-a-managed-metadata-field"></a><span data-ttu-id="7ac11-119">Configurer votre colonne de site de bibliothèque de documents pour un champ de métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="7ac11-119">Configure your document library site column for a managed metadata field</span></span>


   ![Créer des métadonnées gérées](../media/content-understanding/creative.png)</br>

## <a name="see-also"></a><span data-ttu-id="7ac11-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ac11-121">See Also</span></span>
[<span data-ttu-id="7ac11-122">Présentation des métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="7ac11-122">Introduction to Managed Metadata</span></span>](https://docs.microsoft.com/sharepoint/managed-metadata#terms)</br>
[<span data-ttu-id="7ac11-123">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="7ac11-123">Create an extractor</span></span>](create-an-extractor.md)</br>
[<span data-ttu-id="7ac11-124">Créer une colonne de métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="7ac11-124">Create a managed metadata column</span></span>](https://support.microsoft.com/office/create-a-managed-metadata-column-8fad9e35-a618-4400-b3c7-46f02785d27f?redirectSourcePath=%252farticle%252fc2a06717-8105-4aea-890d-3082853ab7b7&ui=en-US&rs=en-US&ad=US)</br>





