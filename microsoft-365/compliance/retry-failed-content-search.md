---
title: Réessayer une recherche de contenu pour résoudre une erreur d’emplacement de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Au cours d’un examen, vous pouvez utiliser le bouton Nouvelle tentative pour résoudre les recherches de contenu qui ont des erreurs d’emplacement de contenu.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: fb85a882ef111aa38a73dbe155a9ad0ef57dd3de
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311819"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="619c0-103">Réessayer une recherche de contenu pour résoudre une erreur d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="619c0-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="619c0-104">Lorsque vous utilisez la recherche de contenu dans le centre de sécurité et conformité pour rechercher un grand nombre de boîtes aux lettres, vous pouvez obtenir des erreurs de recherche similaires à l’erreur :</span><span class="sxs-lookup"><span data-stu-id="619c0-104">When you use Content Search in the security and compliance center to search a large number of mailboxes, you may get search errors that are similar to the  error:</span></span>

```text
Error


The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="619c0-105">Ces erreurs (avec des codes d’erreur de CS001-002, CS003-002, CS008-009, CS012-002 et d’autres erreurs de la forme CS0XX-0XX) indiquent que la recherche de contenu n’a pas réussi à rechercher des emplacements de contenu spécifiques ; dans cet exemple, deux boîtes aux lettres n’ont pas été recherchés.</span><span class="sxs-lookup"><span data-stu-id="619c0-105">These errors (with error codes of CS001-002, CS003-002, CS008-009, CS012-002, and other errors of the form CS0XX-0XX) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched.</span></span> <span data-ttu-id="619c0-106">Ces erreurs sont affichées dans la page de présentation des détails de l’état de la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="619c0-106">These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="619c0-107">Cause des erreurs d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="619c0-107">Cause of content location errors</span></span>

<span data-ttu-id="619c0-108">Lorsque vous recherchez un grand nombre de boîtes aux lettres, la recherche est distribuée sur des milliers de serveurs dans un centre de données Microsoft.</span><span class="sxs-lookup"><span data-stu-id="619c0-108">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter.</span></span> <span data-ttu-id="619c0-109">À tout moment, des serveurs spécifiques peuvent être en état de redémarrage ou en cours de rerouillage vers des copies redondantes.</span><span class="sxs-lookup"><span data-stu-id="619c0-109">At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies.</span></span> <span data-ttu-id="619c0-110">Dans l’un ou l’autre de ces cas, la demande de récupération des données par la recherche de contenu prendra du temps. Dans l’exemple précédent, les erreurs des boîtes aux lettres qui ont échoué étaient le résultat du délai d’insétion de la recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-110">In either of these cases, the Content Search's request to retrieve data will time out. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="619c0-111">Résolution des erreurs d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="619c0-111">Resolving content location errors</span></span>

<span data-ttu-id="619c0-112">Le redémarrage de la recherche entraîne souvent des erreurs similaires sur différents serveurs.</span><span class="sxs-lookup"><span data-stu-id="619c0-112">Restarting the search will often result in similar errors on different servers.</span></span> <span data-ttu-id="619c0-113">Au lieu de redémarrer la  recherche, cliquez sur le bouton Nouvelle tentative qui s’affiche en haut de la page des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-113">Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Cliquez sur le bouton Nouvelle tentative pour résoudre les erreurs d’emplacement de contenu](../media/retrycontentsearch3.png)

<span data-ttu-id="619c0-115">Cela entraîne une nouvelle tentative de recherche uniquement pour les boîtes aux lettres qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="619c0-115">This will result in the retrying the search only for the mailboxes that failed.</span></span> <span data-ttu-id="619c0-116">Lorsque vous retentez la recherche, les autres résultats renvoyés avec succès sont conservés.</span><span class="sxs-lookup"><span data-stu-id="619c0-116">When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="619c0-117">Astuces éviter les erreurs d’emplacement de contenu</span><span class="sxs-lookup"><span data-stu-id="619c0-117">Tips to avoid content location errors</span></span>

<span data-ttu-id="619c0-118">Voici quelques causes supplémentaires des erreurs d’emplacement de contenu et quelques conseils pour vous aider à les éviter lors de la recherche d’un grand nombre de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-118">Here are some additional causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="619c0-119">La boîte aux lettres à rechercher peut être occupée en raison de l’activité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="619c0-119">The mailbox being searched might be busy due to user activity.</span></span> <span data-ttu-id="619c0-120">Dans ce cas, le service de recherche peut se limiter lui-même pour empêcher l’indisponibilité de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-120">In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable.</span></span> <span data-ttu-id="619c0-121">Pour éviter cela, essayez d’effectuer des recherches en de autres heures d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="619c0-121">To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="619c0-122">La requête de recherche peut récupérer trop de contenu de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-122">The search query might be retrieving too much content from the mailbox.</span></span> <span data-ttu-id="619c0-123">Si possible, essayez de restreindre l’étendue de la recherche à l’aide de mots clés, de plages de dates et de conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-123">If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="619c0-124">Trop de mots clés ou d’expressions de mots clés lorsque vous créez une requête de recherche à l’aide de la liste [de mots clés.](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-searches)</span><span class="sxs-lookup"><span data-stu-id="619c0-124">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-searches).</span></span> <span data-ttu-id="619c0-125">Lorsque vous exécutez une requête de recherche qui utilise la liste de mots clés, le service exécute essentiellement une recherche distincte pour chaque ligne de la liste de mots clés afin que des statistiques soient générées.</span><span class="sxs-lookup"><span data-stu-id="619c0-125">When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated.</span></span> <span data-ttu-id="619c0-126">Si vous utilisez la liste de mots clés dans les requêtes de recherche, réduisez le nombre de lignes dans la liste de mots clés ou divisez les mots clés numériques en listes plus petites et créez une recherche différente pour chaque liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="619c0-126">If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="619c0-127">Pour réduire les problèmes causés par les grandes listes de mots clés, vous êtes maintenant limité à 20 lignes au maximum dans la liste des mots clés d’une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-127">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="619c0-128">Trop de recherches sont effectuées sur la même boîte aux lettres en même temps.</span><span class="sxs-lookup"><span data-stu-id="619c0-128">Too many searches are being performed on the same mailbox at the same time.</span></span> <span data-ttu-id="619c0-129">Si possible, essayez d’exécuter une recherche à la fois sur une seule boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-129">If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="619c0-130">Recherche d’un trop grand nombre de boîtes aux lettres dans une seule recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-130">Searching too many mailboxes in a single search.</span></span> <span data-ttu-id="619c0-131">La probabilité d’erreurs d’emplacement de contenu augmente lorsque vous recherchez un grand nombre de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-131">The probability of content location errors increases when searching a large number of mailboxes.</span></span> <span data-ttu-id="619c0-132">Si possible, essayez d’exécuter plusieurs recherches afin que chaque recherche inclut un sous-ensemble de boîtes aux lettres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="619c0-132">If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="619c0-133">La maintenance requise est en cours sur la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="619c0-133">Required maintenance is being performed on the mailbox.</span></span> <span data-ttu-id="619c0-134">Bien que cette cause se produise probablement rarement, patientez un peu après la réception de l’erreur d’emplacement de contenu, puis réessayez la recherche.</span><span class="sxs-lookup"><span data-stu-id="619c0-134">Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
