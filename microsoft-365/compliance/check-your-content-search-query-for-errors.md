---
title: Vérifier la présence d’erreurs dans vos requêtes de recherche
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
search.appverid:
- MOE150
- MET150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
ms.custom: seo-marvel-apr2020
description: Découvrez comment détecter les erreurs et les fautes de frappe dans votre requête de mot clé pour les recherches de découverte électronique avant d’effectuer la recherche.
ms.openlocfilehash: 9c041ca690df3306347cbca77df3ba9639801245
ms.sourcegitcommit: efb932db63ad3ab4af4b585428d567d069410e4e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2021
ms.locfileid: "52311687"
---
# <a name="check-your-search-query-for-errors"></a><span data-ttu-id="ec716-103">Vérifier la présence d’erreurs dans vos requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="ec716-103">Check your search query for errors</span></span>
  
<span data-ttu-id="ec716-104">Voici une liste des caractères non pris en place que nous vérifions dans les requêtes de recherche pour la recherche de contenu et la découverte électronique principale.</span><span class="sxs-lookup"><span data-stu-id="ec716-104">Here's a list of the unsupported characters that we check for in search queries for Content search and Core eDiscovery.</span></span> <span data-ttu-id="ec716-105">Les caractères non pris enupportés sont souvent masqués et ils provoquent généralement une erreur de recherche ou retournent des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="ec716-105">Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="ec716-106">**Guillemets intelligents** : les guillemets simples et doubles (également appelés guillemets) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec716-106">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported.</span></span> <span data-ttu-id="ec716-107">Seuls les guillemets droits peuvent être utilisés dans une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="ec716-107">Only straight quotation marks can be used in a search query.</span></span> 

- <span data-ttu-id="ec716-108">**Caractères non imprimables** et de contrôle : les caractères non imprimables et les caractères de contrôle ne représentent pas un symbole écrit, tel qu’un caractère alpha-numérique.</span><span class="sxs-lookup"><span data-stu-id="ec716-108">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as an alpha-numeric character.</span></span> <span data-ttu-id="ec716-109">Il peut s'agir de caractères servant à mettre en forme le texte ou à séparer des lignes.</span><span class="sxs-lookup"><span data-stu-id="ec716-109">Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 

- <span data-ttu-id="ec716-110"> Marques de gauche à droite et de droite à gauche : ces marques sont des caractères de contrôle utilisés pour indiquer l’orientation du texte pour les langues de gauche à droite (telles que l’anglais et l’espagnol) et de droite à gauche (comme l’arabe et l’hébreu).</span><span class="sxs-lookup"><span data-stu-id="ec716-110">**Left-to-right and right-to-left marks** - These marks are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>

- <span data-ttu-id="ec716-111">**Opérateurs booléens** en minuscules : si vous utilisez un opérateur booléen, tel que **AND**, **OR** et **NOT** dans une requête de recherche, il doit être en minuscules.</span><span class="sxs-lookup"><span data-stu-id="ec716-111">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase.</span></span> <span data-ttu-id="ec716-112">Lorsque nous vérifions une requête pour des fautes de frappe, la syntaxe de requête indique souvent qu’un opérateur booléen est utilisé même si des opérateurs en minuscules peuvent être utilisés ; par exemple,  `(WordA or WordB) and (WordC or WordD)` .</span><span class="sxs-lookup"><span data-stu-id="ec716-112">When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>

## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="ec716-113">Que se passe-t-il si une requête a un caractère non pris en compte ?</span><span class="sxs-lookup"><span data-stu-id="ec716-113">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="ec716-114">Si des caractères non pris en compte sont trouvés dans votre requête, un message d’avertissement indique que des caractères non pris en compte ont été trouvés et suggère une alternative.</span><span class="sxs-lookup"><span data-stu-id="ec716-114">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters were found and suggests an alternative.</span></span> <span data-ttu-id="ec716-115">Vous avez ensuite la possibilité de conserver la requête d’origine ou de la remplacer par la requête révisée suggérée.</span><span class="sxs-lookup"><span data-stu-id="ec716-115">You then have the option keep the original query or replace it with the suggested revised query.</span></span>

<span data-ttu-id="ec716-116">Voici un exemple du message d’avertissement qui s’affiche après que vous avez cliqué sur Rechercher les fautes de frappe pour la requête de recherche dans la capture d’écran précédente. </span><span class="sxs-lookup"><span data-stu-id="ec716-116">Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot.</span></span> <span data-ttu-id="ec716-117">Notez que la requête d’origine utilisait des guillemets intelligents et des opérateurs booléens en minuscules.</span><span class="sxs-lookup"><span data-stu-id="ec716-117">Note the original query used smart quotes and lowercase Boolean operators.</span></span>
  
![Un message d’avertissement s’affiche avec une révision suggérée pour votre requête](../media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="ec716-119">Comment empêcher les caractères non pris en compte dans vos requêtes de recherche</span><span class="sxs-lookup"><span data-stu-id="ec716-119">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="ec716-120">Les caractères non pris en aide sont généralement ajoutés à une requête lorsque vous copiez la requête ou certaines parties de la requête à partir d’autres applications (telles que Microsoft Word ou Microsoft Excel) et que vous les collez dans la zone de mot clé de la page de requête d’une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="ec716-120">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and paste them in the keyword box on the query page of a Content Search.</span></span> <span data-ttu-id="ec716-121">Le meilleur moyen d'éviter les caractères non pris en charge est de saisir la requête dans la zone de mot clé.</span><span class="sxs-lookup"><span data-stu-id="ec716-121">The best way to prevent unsupported characters is to just type the query in the keyword box.</span></span> <span data-ttu-id="ec716-122">Vous pouvez également copier une requête à partir de Word ou Excel, puis la coller dans un éditeur de texte simple, tel que Microsoft Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="ec716-122">Or you can copy a query from Word or Excel, and then paste it in a plain text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="ec716-123">Enregistrez le fichier texte et sélectionnez **ANSI** dans **la** liste de listes listes de codage.</span><span class="sxs-lookup"><span data-stu-id="ec716-123">Save the text file and select **ANSI** in the **Encoding** drop-down list.</span></span> <span data-ttu-id="ec716-124">Cette action supprime tout le formatage et tous les caractères non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ec716-124">This will remove any formatting and unsupported characters.</span></span> <span data-ttu-id="ec716-125">Vous pouvez ensuite copier la requête du fichier texte vers la zone de mot clé de la requête.</span><span class="sxs-lookup"><span data-stu-id="ec716-125">Then you can copy and paste the query from the text file to the keyword query box.</span></span>
