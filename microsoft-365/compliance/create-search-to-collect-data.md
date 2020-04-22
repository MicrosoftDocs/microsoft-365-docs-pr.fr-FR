---
title: Créer une recherche
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
description: ''
ms.openlocfilehash: 4b740b07b59b7500b8f57584767796b7f31ae87d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43635974"
---
# <a name="create-a-search"></a><span data-ttu-id="2c7f0-102">Créer une recherche</span><span class="sxs-lookup"><span data-stu-id="2c7f0-102">Create a search</span></span>

<span data-ttu-id="2c7f0-103">Sous l’onglet **recherches** de votre cas, vous pouvez créer une nouvelle recherche en cliquant sur **nouvelle recherche** et en suivant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

![Assistant recherche dans un cas avancé eDiscovery](../media/AeDSearch1.png)

## <a name="name-the-search-and-give-it-a-description"></a><span data-ttu-id="2c7f0-105">Nommez la recherche et donnez-lui une description.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-105">Name the search and give it a description</span></span>

<span data-ttu-id="2c7f0-106">Chaque recherche avec un cas doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-106">Each search with a case should have a unique name.</span></span> <span data-ttu-id="2c7f0-107">Vous pouvez éventuellement fournir une description pour votre recherche.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-107">You can optionally provide a description for your search.</span></span> 

## <a name="choose-the-custodians-and-custodial-locations-to-search"></a><span data-ttu-id="2c7f0-108">Choisir les dépositaires et les lieux de recherche</span><span class="sxs-lookup"><span data-stu-id="2c7f0-108">Choose the custodians and custodial locations to search</span></span>

<span data-ttu-id="2c7f0-109">Choisissez les emplacements de contenu de dépositaire à rechercher en spécifiant les dépositaires que vous avez ajoutés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-109">Choose custodian content locations to search by specifying that custodians you have added to the case.</span></span> <span data-ttu-id="2c7f0-110">En sélectionnant un dépositaire, vous lancez la recherche par rapport à toutes les sources de données mappées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-110">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="2c7f0-111">Vous avez également la possibilité de limiter la recherche aux sources de données sélectionnées pour chaque dépositaire.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-111">You also have the option to narrow the search to selected data sources for each custodian.</span></span> <span data-ttu-id="2c7f0-112">Pour plus d’informations sur la façon d’ajouter des dépositaires et de gérer leurs sources de données, consultez la rubrique [work with dépositaires](managing-custodians.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f0-112">For more information about how to add custodians and manage their data sources, see [Work with custodians](managing-custodians.md).</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="2c7f0-113">Choisir les emplacements non privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="2c7f0-113">Choose non-custodial locations</span></span>

<span data-ttu-id="2c7f0-114">Dans certains cas, vous souhaiterez peut-être Rechercher des sources de données qui ne sont pas associées à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="2c7f0-114">In some cases, you may want to search data sources that are not associated with a custodian.</span></span> <span data-ttu-id="2c7f0-115">Dans ce cas, vous pouvez spécifier les emplacements de recherche, ou choisir de rechercher tous les emplacements de contenu d’un service Microsoft spécifique (par exemple, rechercher toutes les boîtes aux lettres Exchange ou tous les sites SharePoint et OneDrive).</span><span class="sxs-lookup"><span data-stu-id="2c7f0-115">In this case, you can specify the locations you want to search, or choose to search all content locations for a specific Microsoft service (such as searching all Exchange mailboxes or all SharePoint sites and OneDrive accounts).</span></span>

## <a name="define-the-search-query-and-conditions"></a><span data-ttu-id="2c7f0-116">Définir la requête de recherche et les conditions</span><span class="sxs-lookup"><span data-stu-id="2c7f0-116">Define the search query and conditions</span></span>

<span data-ttu-id="2c7f0-117">Vous pouvez définir la requête de mots clés et les conditions de la recherche à l’aide des cartes de condition prédéfinies ou du langage de requête de mot clé (KQL).</span><span class="sxs-lookup"><span data-stu-id="2c7f0-117">You can define the keywords query and any conditions for the search by using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="2c7f0-118">Pour plus d’informations, consultez la rubrique [créer des requêtes de recherche](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f0-118">For more information, see [Build search queries](building-search-queries.md).</span></span>
