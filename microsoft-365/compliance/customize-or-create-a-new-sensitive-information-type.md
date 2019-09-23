---
title: Personnalisation ou création d’un type d’informations sensibles
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Découvrez comment modifier ou créer des types d’informations sensibles Office 365 pour le RGPD.
ms.openlocfilehash: 264e310c019c47d1b3109b20fbdd61b323ec5530
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078614"
---
# <a name="customize-or-create-a-new-sensitive-information-type"></a><span data-ttu-id="a0e52-103">Personnalisation ou création d’un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a0e52-103">Customize or create a new sensitive information type</span></span>

<span data-ttu-id="a0e52-104">Cet article fournit trois exemples qui décrivent comment modifier ou créer de nouveaux types d’informations sensibles Office 365 pour le RGPD.</span><span class="sxs-lookup"><span data-stu-id="a0e52-104">This article provides three examples to demonstrate how to modify or create new Office 365 sensitive information types for GDPR.</span></span>

- <span data-ttu-id="a0e52-105">Modification d’un type d’informations sensibles existant : Numéro de carte de crédit de l'U.E.</span><span class="sxs-lookup"><span data-stu-id="a0e52-105">Modify an existing sensitive information type — EU Debit Card Number</span></span>

- <span data-ttu-id="a0e52-106">Création d’un type d’informations sensibles : adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="a0e52-106">Create a new sensitive information type — email address</span></span>

- <span data-ttu-id="a0e52-107">Création d’un type d’informations sensibles avec un exemple de fichier XML : numéro de client Contoso</span><span class="sxs-lookup"><span data-stu-id="a0e52-107">Create a new sensitive information type with example XML file — Contoso customer number</span></span>

<span data-ttu-id="a0e52-108">Voir également :</span><span class="sxs-lookup"><span data-stu-id="a0e52-108">Also see:</span></span>

- [<span data-ttu-id="a0e52-109">Créer un type d’informations sensibles personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a0e52-109">Create a custom sensitive information type using PowerShell</span></span>](create-a-custom-sensitive-information-type-in-scc-powershell.md)

- [<span data-ttu-id="a0e52-110">Personnaliser un type d’informations sensibles intégré</span><span class="sxs-lookup"><span data-stu-id="a0e52-110">Customize a built-in sensitive information type</span></span>](customize-a-built-in-sensitive-information-type.md)

## <a name="modify-a-sensitive-information-type-to-improve-accuracy"></a><span data-ttu-id="a0e52-111">Modification d’un type d’informations sensibles pour améliorer la précision</span><span class="sxs-lookup"><span data-stu-id="a0e52-111">Modify a sensitive information type to improve accuracy</span></span>

<span data-ttu-id="a0e52-112">Si vous utilisez la recherche de contenu pour rechercher des données personnelles à l’aide des types d’informations sensibles et que vous n’obtenez pas les résultats attendus ou que la requête renvoie un trop grand nombre de faux positifs, vous pouvez modifier le type d’informations sensibles en fonction de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a0e52-112">If you’re using Content Search to search for personal data using sensitive information types and you’re not returning the expected results, or the query returns too many false positives, consider modifying the sensitive information type to work better with your environment.</span></span>

<span data-ttu-id="a0e52-p101">La meilleure pratique lorsque vous créez ou personnalisez un type d’informations sensibles consiste à créer un type d’informations sensibles sur la base d’un type existant et à lui attribuer un nom et des identificateurs uniques. Par exemple, si vous souhaitez ajuster les paramètres du type d’informations sensibles « Numéro de carte de crédit de l'U.E. », vous pouvez nommer votre copie de cette règle « Carte de crédit de l’U.E. améliorée » pour la distinguer de l’originale.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p101">The best practice when creating or customizing a sensitive information type is to create a new sensitive information type based on an existing one, giving it a unique name and identifiers. For example, if you wish to adjust the parameters of the “EU Debit Card Number” sensitive information type, you could name your copy of that rule “EU Debit Card Enhanced” to distinguish it from the original.</span></span>

<span data-ttu-id="a0e52-p102">Dans votre nouveau type d’informations sensibles, il suffit de modifier les valeurs à modifier pour améliorer sa précision. Ensuite, chargez votre nouveau type d’informations sensibles et créez une règle DLP (ou modifiez-en une existante) pour utiliser le nouveau type d’informations sensibles que vous venez d’ajouter. La modification de la précision de types d’informations sensibles peut nécessiter des essais et des erreurs. Par conséquent, conservez une copie du type d’origine pour l’utiliser éventuellement à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p102">In your new sensitive information type, simply modify the values you wish to change to improve its accuracy. Once complete, upload your new sensitive information type and create a new DLP rule (or modify an existing one) to use the new sensitive information type you just added. Modifying the accuracy of sensitive information types might require some trial and error, so maintaining a copy of the original type allows you to fall back to it if required in the future.</span></span>

<span data-ttu-id="a0e52-118">Pour personnaliser un type d’informations sensibles :</span><span class="sxs-lookup"><span data-stu-id="a0e52-118">To customize a sensitive information type:</span></span>

1.  <span data-ttu-id="a0e52-119">Exportez le Package de règles Microsoft existant des types d’informations sensibles intégrés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="a0e52-119">Export the existing Microsoft Rule Package of built in sensitive information types in Office 365.</span></span>

2.  <span data-ttu-id="a0e52-120">Renommez ce fichier XML et ouvrez-le dans votre éditeur XML préféré.</span><span class="sxs-lookup"><span data-stu-id="a0e52-120">Rename this XML file and open it in your favorite XML editor.</span></span>

3.  <span data-ttu-id="a0e52-121">Isolez le type d’informations sensibles et supprimez tous les autres.</span><span class="sxs-lookup"><span data-stu-id="a0e52-121">Isolate the sensitive information type and remove all others.</span></span>

4.  <span data-ttu-id="a0e52-122">Utilisez PowerShell pour générer deux nouveaux GUID pour le type d’informations sensibles que vous modifiez.</span><span class="sxs-lookup"><span data-stu-id="a0e52-122">Use PowerShell to generate two new GUIDs for the sensitive information type you are modifying.</span></span>

5.  <span data-ttu-id="a0e52-123">Modifiez l’ID et d’autres éléments de base pour que le type d’informations sensibles soit unique (remplacez également les deux GUID par les deux nouveaux que vous avez générés).</span><span class="sxs-lookup"><span data-stu-id="a0e52-123">Modify the ID and other basic elements so the sensitive information type is unique (this includes replacing two GUIDs with the new ones you generated).</span></span>

6.  <span data-ttu-id="a0e52-124">Affinez les exigences de correspondance pour améliorer la précision.</span><span class="sxs-lookup"><span data-stu-id="a0e52-124">Tune the match requirements to improve accuracy.</span></span>

    1.  <span data-ttu-id="a0e52-125">Modifications de la proximité : modifiez la proximité du motif de caractère pour développer ou réduire la fenêtre dans laquelle les mots-clés doivent être recherchés autour du type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="a0e52-125">Proximity modifications — Modify the character pattern proximity to expand or shrink the window in which keywords must be found around the sensitive information type.</span></span>

    2.  <span data-ttu-id="a0e52-p103">Modifications du mot-clé : ajoutez des mots clés à l’un des éléments \<Keyword\> afin de fournir à notre type d’informations sensibles un élément de preuve corroborante plus spécifique à rechercher pour signaler une correspondance sur cette règle. Vous pouvez aussi supprimer des mots-clés qui sont à l’origine de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p103">Keyword modifications — Add keywords to one of the \<Keywords\> element in order to provide our sensitive information type more specific corroborative evidence to search for in order to signal a match on this rule. Or remove keywords that are causing false positives.</span></span>

    3.  <span data-ttu-id="a0e52-128">Modifications de confiance : modifiez la confiance avec laquelle le type d’informations sensibles doit correspondre aux critères spécifiés dans sa définition avant qu’une correspondance soit signalée et déclarée.</span><span class="sxs-lookup"><span data-stu-id="a0e52-128">Confidence modifications — Modify the confidence with which the sensitive information type must match the criteria specified in its definition before a match is signaled and reported.</span></span>

7.  <span data-ttu-id="a0e52-129">Chargez le nouveau type d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="a0e52-129">Upload the new sensitive information type.</span></span>

8.  <span data-ttu-id="a0e52-p104">Analysez de nouveau votre contenu pour identifier les informations sensibles. Reportez-vous à la rubrique [Demander manuellement l’analyse et la réindexation d’un site](https://support.office.com/fr-FR/article/Manually-request-crawling-and-re-indexing-of-a-site-a-library-or-a-list-9AFA977D-39DE-4321-B4CA-8C7C7E6D264E).</span><span class="sxs-lookup"><span data-stu-id="a0e52-p104">Recrawl your content to identify the sensitive information. See [Manually request crawling and re-indexing of a site](https://support.office.com/fr-FR/article/Manually-request-crawling-and-re-indexing-of-a-site-a-library-or-a-list-9AFA977D-39DE-4321-B4CA-8C7C7E6D264E).</span></span>

## <a name="example-modify-the-eu-debit-card-number-sensitive-information-type"></a><span data-ttu-id="a0e52-132">Exemple : modification du type d’informations sensibles « Numéro de carte de crédit de l'U.E. »</span><span class="sxs-lookup"><span data-stu-id="a0e52-132">Example: modify the ‘EU Debit Card Number’ sensitive information type</span></span>

<span data-ttu-id="a0e52-p105">Lorsque vous améliorez la précision des règles DLP dans un système, vous devez effectuer des tests sur un ensemble de données exemple et éventuellement des réglages précis à l’aide de tests et modifications répétitifs. Cet exemple décrit des modifications du type d’informations sensibles « Numéro de carte de crédit de l'U.E. » pour améliorer sa précision.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p105">Improving the accuracy of DLP rules in any system requires testing against a sample data set, and may require fine tuning through repetitive modifications and tests. This example demonstrates modifications to the ‘EU Debit Card Number’ sensitive information type to improve its accuracy.</span></span>

<span data-ttu-id="a0e52-p106">Lorsque vous recherchez un numéro de carte de crédit de l'U.E., la définition de ce numéro est strictement définie comme 16 chiffres utilisant un modèle complexe et soumis à la validation d’une somme de contrôle. Nous ne pouvons pas modifier ce modèle en raison de la définition de chaîne de ce type d’informations sensibles. Toutefois, nous pouvons effectuer les ajustements suivants pour améliorer la précision avec laquelle la DLP Office 365 recherche ce type d’informations sensibles dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p106">When searching for an EU Debit Card Number in our example, the definition of that number is strictly defined as 16 digits using a complex pattern, and being subject to the validation of a checksum. We cannot alter this pattern due to the string definition of this sensitive information type. However, we can make the following adjustments to improve the accuracy of how Office 365 DLP finds this sensitive information type within Office 365.</span></span>

### <a name="proximity-modification"></a><span data-ttu-id="a0e52-138">Modification de la proximité</span><span class="sxs-lookup"><span data-stu-id="a0e52-138">Proximity modification</span></span>

<span data-ttu-id="a0e52-p107">Nous allons réduire la fenêtre en modifiant la valeur patternProximity dans notre élément \<Entity\> de 300 à 150 caractères. Cela signifie que notre preuve corroborante, ou nos mots-clés doivent être plus proches de notre type d’informations sensibles pour signaler une correspondance sur cette règle.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p107">We'll shrink the window by modifying the patternProximity value in our \<Entity\> element from 300 to 150 characters. This means that our corroborative evidence, or our keywords, must be closer to our sensitive information type in order to signal a match on this rule.</span></span>

<span data-ttu-id="a0e52-141">\<Entity id="48da7072-821e-4804-9fab-72ffb48f6f78" patternsProximity="150" recommendedConfidence="85"\></span><span class="sxs-lookup"><span data-stu-id="a0e52-141">\<Entity id="48da7072-821e-4804-9fab-72ffb48f6f78" patternsProximity="150" recommendedConfidence="85"\></span></span>

### <a name="keyword-modifications"></a><span data-ttu-id="a0e52-142">Modifications des mots-clés</span><span class="sxs-lookup"><span data-stu-id="a0e52-142">Keyword modifications</span></span>

<span data-ttu-id="a0e52-p108">Certains mots-clés peuvent entraîner des faux positifs. Par conséquent, vous pouvez supprimer des mots-clés. Voici les mots-clés pour cet exemple :</span><span class="sxs-lookup"><span data-stu-id="a0e52-p108">Some keywords might cause false positives to occur. As a result you might want to remove keywords. Here are the keywords for this example::</span></span>

<span data-ttu-id="a0e52-146">\<Keyword id="Keyword\_card\_terms\_dict"\></span><span class="sxs-lookup"><span data-stu-id="a0e52-146">\<Keyword id="Keyword\_card\_terms\_dict"\></span></span>

<span data-ttu-id="a0e52-147">\<Group\></span><span class="sxs-lookup"><span data-stu-id="a0e52-147">\<Group\></span></span>

<span data-ttu-id="a0e52-148">\<Term\>corporate card\</Term\></span><span class="sxs-lookup"><span data-stu-id="a0e52-148">\<Term\>corporate card\</Term\></span></span>

<span data-ttu-id="a0e52-149">\<Term\>organization card\</Term\></span><span class="sxs-lookup"><span data-stu-id="a0e52-149">\<Term\>organization card\</Term\></span></span>

<span data-ttu-id="a0e52-150">\<Term\>acct nbr\</Term\></span><span class="sxs-lookup"><span data-stu-id="a0e52-150">\<Term\>acct nbr\</Term\></span></span>

<span data-ttu-id="a0e52-151">\<Term\>acct num\</Term\></span><span class="sxs-lookup"><span data-stu-id="a0e52-151">\<Term\>acct num\</Term\></span></span>

<span data-ttu-id="a0e52-152">\<Term\>acct no\</Term\></span><span class="sxs-lookup"><span data-stu-id="a0e52-152">\<Term\>acct no\</Term\></span></span>

<span data-ttu-id="a0e52-153">…</span><span class="sxs-lookup"><span data-stu-id="a0e52-153">…</span></span>

<span data-ttu-id="a0e52-154">\</Group\></span><span class="sxs-lookup"><span data-stu-id="a0e52-154">\</Group\></span></span>

<span data-ttu-id="a0e52-155">\</Keyword\></span><span class="sxs-lookup"><span data-stu-id="a0e52-155">\</Keyword\></span></span>

### <a name="confidence-modifications"></a><span data-ttu-id="a0e52-156">Modifications de la confiance</span><span class="sxs-lookup"><span data-stu-id="a0e52-156">Confidence modifications</span></span>

<span data-ttu-id="a0e52-p109">Si vous supprimez des mots-clés de la définition, vous voudrez généralement ajuster le niveau de confiance que vous avez concernant le fait que ce type d’informations sensibles a été trouvé en diminuant cette valeur. Le niveau par défaut pour le type de numéro de carte de crédit de l'U.E. est 85.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p109">If you remove keywords from the definition, you would typically want to adjust how confident you are that this sensitive information type was found by lowering this value. The default level for EU Debit Card Number type is 85.</span></span>

<span data-ttu-id="a0e52-159">\<Entity id="48da7072-821e-4804-9fab-72ffb48f6f78" patternsProximity="150" recommendedConfidence="85"\></span><span class="sxs-lookup"><span data-stu-id="a0e52-159">\<Entity id="48da7072-821e-4804-9fab-72ffb48f6f78" patternsProximity="150" recommendedConfidence="85"\></span></span>

<span data-ttu-id="a0e52-160">\<Pattern confidenceLevel="85"\></span><span class="sxs-lookup"><span data-stu-id="a0e52-160">\<Pattern confidenceLevel="85"\></span></span>

<span data-ttu-id="a0e52-161">…</span><span class="sxs-lookup"><span data-stu-id="a0e52-161">…</span></span>

<span data-ttu-id="a0e52-162">\</Pattern\></span><span class="sxs-lookup"><span data-stu-id="a0e52-162">\</Pattern\></span></span>

<span data-ttu-id="a0e52-163">\</Entity\></span><span class="sxs-lookup"><span data-stu-id="a0e52-163">\</Entity\></span></span>

## <a name="create-a-new-custom-sensitive-information-type"></a><span data-ttu-id="a0e52-164">Création d’un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="a0e52-164">Create a new custom sensitive information type</span></span>

<span data-ttu-id="a0e52-165">Pour créer un type d’informations sensibles personnalisé, commencez par utiliser la recherche de contenu pour :</span><span class="sxs-lookup"><span data-stu-id="a0e52-165">To create a new custom sensitive information type, start by using Content Search to:</span></span>

-   <span data-ttu-id="a0e52-166">Optimiser une requête KQL</span><span class="sxs-lookup"><span data-stu-id="a0e52-166">Optimize a KQL query</span></span>

-   <span data-ttu-id="a0e52-167">Voir les mots-clés les plus utiles</span><span class="sxs-lookup"><span data-stu-id="a0e52-167">See which keywords are most useful</span></span>

<span data-ttu-id="a0e52-p110">Utilisez ces résultats pour créer un type d’informations sensibles. Ensuite, optimisez le nouveau type d’informations sensibles pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p110">Use these results to create a new sensitive information type. Then optimize the new sensitive information type for your environment.</span></span>

<span data-ttu-id="a0e52-p111">Remarque : de nombreux nouveaux types d’informations sensibles seront bientôt disponibles pour les données personnelles dans les pays de l’UE. Si vous avez besoin de créer de nouveaux types d’informations sensibles, commencez par cibler des données qui sont personnalisées pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p111">Note: Many new sensitive information types are coming soon for personal data in EU countries. If you need to create new sensitive information types, begin by targeting data that is custom to your environment.</span></span>

### <a name="step-1--use-kql-queries-and-key-words-to-find-additional-data-in-your-environment"></a><span data-ttu-id="a0e52-172">Étape 1 : utilisez des requêtes KQL et des mots-clés pour rechercher des données supplémentaires dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="a0e52-172">Step 1 — Use KQL queries and key words to find additional data in your environment</span></span>

<span data-ttu-id="a0e52-p112">Il se peut que vous deviez créer des requêtes afin d’obtenir des données personnelles qui sont soumises au RGPD. La recherche de contenu utilise le langage de requête de mot-clé (KQL) pour rechercher des données. Les données les plus sensibles ne peuvent pas être correctement détectées à l’aide de KQL seul sans types d’informations sensibles. Par conséquent, l’objectif consiste à tester et optimiser des chaînes KQL à l’aide de la recherche de contenu, puis à les utiliser pour créer et affiner de nouveaux types d’informations sensibles dans lesquels vous pouvez obtenir une précision encore plus grande.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p112">You might need to create additional queries to find personal data that is subject to GDPR. Content Search uses Keyword Query Language (KQL) to find data. Most sensitive data can’t be accurately detected using just KQL without sensitive information types. So the goal is to test and optimize KQL strings using Content Search and then use these to create and tune new sensitive information types where you can achieve even greater accuracy.</span></span>

<span data-ttu-id="a0e52-177">Utilisez ces ressources pour formuler et optimiser des requêtes à l’aide de KQL :</span><span class="sxs-lookup"><span data-stu-id="a0e52-177">Use these resources to formulate and optimize queries using KQL:</span></span>

-   [<span data-ttu-id="a0e52-178">Référence de syntaxe de langage de requête de mot-clé (KQL) (DMC)</span><span class="sxs-lookup"><span data-stu-id="a0e52-178">Keyword Query Language (KQL) syntax reference (DMC)</span></span>](https://docs.microsoft.com/fr-FR/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

-   [<span data-ttu-id="a0e52-179">Exécuter une Recherche de Contenu</span><span class="sxs-lookup"><span data-stu-id="a0e52-179">Run a Content Search</span></span>](https://support.office.com/fr-FR/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a) 

<span data-ttu-id="a0e52-p113">La recherche de contenu fournit une autre ressource pour vous aider à développer des requêtes KQL appropriées et des types d’informations sensibles : les mots-clés. Pourquoi utiliser la liste de mots-clés ? Vous pouvez obtenir des statistiques indiquant le nombre d’éléments qui correspondent à chaque mot-clé. Cela peut vous aider à identifier rapidement les mots-clés les plus (et les moins) efficaces. Pour plus d’informations sur les statistiques de recherche, reportez-vous à la rubrique relative à l’[affichage des statistiques de mots-clés pour les résultats de la recherche de contenu](https://support.office.com/fr-FR/article/View-keyword-statistics-for-Content-Search-results-9701a024-c52e-43f0-b545-9a53478aec04).</span><span class="sxs-lookup"><span data-stu-id="a0e52-p113">Content Search provides another resource to help you develop KQL queries and sensitive information types — keywords. Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. For more information about search statistics, see [View keyword statistics for Content Search results](https://support.office.com/fr-FR/article/View-keyword-statistics-for-Content-Search-results-9701a024-c52e-43f0-b545-9a53478aec04).</span></span>

<span data-ttu-id="a0e52-p114">Les mots-clés sur chaque ligne sont connectés par l’opérateur OR dans la requête de recherche qui est créée. Vous pouvez également utiliser une expression de mots-clés (entre parenthèses) dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p114">Keywords on each row are connected by the OR operator in the search query that's created. You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span>

<span data-ttu-id="a0e52-187">Pour plus d’informations, reportez-vous à la rubrique [Requêtes par mots-clés et conditions de recherche pour la recherche de contenu](https://support.office.com/fr-FR/article/Keyword-queries-and-search-conditions-for-Content-Search-c4639c2e-7223-4302-8e0d-b6e10f1c3be3).</span><span class="sxs-lookup"><span data-stu-id="a0e52-187">For more information, see [Keyword queries and search conditions for Content Search](https://support.office.com/fr-FR/article/Keyword-queries-and-search-conditions-for-Content-Search-c4639c2e-7223-4302-8e0d-b6e10f1c3be3).</span></span>

### <a name="exampleusing-content-search-to-identify-email-addresses"></a><span data-ttu-id="a0e52-188">Exemple : utilisation de la recherche de contenu pour identifier des adresses e-mail</span><span class="sxs-lookup"><span data-stu-id="a0e52-188">Example—Using Content Search to identify email addresses</span></span>

<span data-ttu-id="a0e52-p115">Les adresses e-mail sont considérées comme des informations sensibles liées à des personnes. Voici un exemple simple qui décrit comment la recherche de contenu peut être utile.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p115">Email addresses are considered sensitive information related to data subjects. This is a simple example to demonstrate how Content Search can help.</span></span>

<span data-ttu-id="a0e52-p116">Le langage KQL et les mots-clés ne peuvent pas être utilisés conjointement. Utilisez ces outils séparément pour affiner votre requête et identifier des mots-clés qui peuvent être utiles dans les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p116">KQL and keywords can’t be used together. Use these tools separately to hone your query and determine keywords that might be useful in sensitive information types.</span></span>

### <a name="kql-query"></a><span data-ttu-id="a0e52-193">Requête KQL</span><span class="sxs-lookup"><span data-stu-id="a0e52-193">KQL query</span></span>

<span data-ttu-id="a0e52-194">(^|\\b)([a-zA-Z0-9\_\\-\\.]+)@([a-zA-Z0-9\_\\-\\.]+)\\.([a-zA-Z]{2,5})($|\\b)</span><span class="sxs-lookup"><span data-stu-id="a0e52-194">(^|\\b)([a-zA-Z0-9\_\\-\\.]+)@([a-zA-Z0-9\_\\-\\.]+)\\.([a-zA-Z]{2,5})($|\\b)</span></span>

<span data-ttu-id="a0e52-195">Remarques :</span><span class="sxs-lookup"><span data-stu-id="a0e52-195">Notes:</span></span>

-   <span data-ttu-id="a0e52-196">Vous pouvez utiliser NEAR et ONEAR pour les recherches de proximité.</span><span class="sxs-lookup"><span data-stu-id="a0e52-196">You can use NEAR and ONEAR for proximity searches.</span></span>

-   <span data-ttu-id="a0e52-197">Malheureusement, le langage KQL ne prend pas en charge les requêtes avec la classe Regex (ex : IdRef="Regex\_email\_address")</span><span class="sxs-lookup"><span data-stu-id="a0e52-197">Unfortunately, KQL doesn’t support queries with the Regex Class (ex: IdRef="Regex\_email\_address")</span></span>

### <a name="keywords"></a><span data-ttu-id="a0e52-198">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a0e52-198">Keywords</span></span>

<span data-ttu-id="a0e52-p117">Entrez chaque mot-clé sur une ligne distincte. Exemple de mots-clés :</span><span class="sxs-lookup"><span data-stu-id="a0e52-p117">Enter each keyword on a separate line. Example keywords:</span></span>

-   <span data-ttu-id="a0e52-201">adresse électronique</span><span class="sxs-lookup"><span data-stu-id="a0e52-201">email address</span></span>

-   <span data-ttu-id="a0e52-202">messagerie</span><span class="sxs-lookup"><span data-stu-id="a0e52-202">mail</span></span>

-   <span data-ttu-id="a0e52-203">contact</span><span class="sxs-lookup"><span data-stu-id="a0e52-203">contact</span></span>

-   <span data-ttu-id="a0e52-204">expéditeur</span><span class="sxs-lookup"><span data-stu-id="a0e52-204">sender</span></span>

-   <span data-ttu-id="a0e52-205">destinataire</span><span class="sxs-lookup"><span data-stu-id="a0e52-205">recipient</span></span>

-   <span data-ttu-id="a0e52-206">cc</span><span class="sxs-lookup"><span data-stu-id="a0e52-206">cc</span></span>

-   <span data-ttu-id="a0e52-207">bcc</span><span class="sxs-lookup"><span data-stu-id="a0e52-207">bcc</span></span>

<span data-ttu-id="a0e52-208">Dans cet exemple, vous pouvez voir que les mots-clés ne sont pas nécessaires et produisent un grand nombre de résultats faux positifs.</span><span class="sxs-lookup"><span data-stu-id="a0e52-208">In this example, you might learn the keywords are not necessary and produce a lot of false positive results.</span></span>

### <a name="step-2--create-a-new-custom-sensitive-information-type"></a><span data-ttu-id="a0e52-209">Étape 2 : créez un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="a0e52-209">Step 2 — Create a new custom sensitive information type</span></span>

<span data-ttu-id="a0e52-p118">Après avoir utilisé des requêtes KQL et des mots-clés pour identifier des informations sensibles, utilisez-les pour créer des types d’informations sensibles personnalisés. Dans de nombreux cas, vous aurez besoin de la sophistication des types d’informations sensibles pour atteindre le niveau de précision adéquat. Vous pouvez ensuite utiliser ces types d’informations sensibles personnalisés avec la recherche de contenu dans les stratégies DLP et d’autres outils, ainsi que dans d’autres requêtes KQL.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p118">After using KQL queries and keywords to identify sensitive information, use these to create new custom sensitive information types. In many cases, you’ll require the sophistication of sensitive information types to achieve the right level of accuracy. You can then use these custom sensitive information types with Content Search, in DLP policies and other tools, and within other KQL queries.</span></span>

<span data-ttu-id="a0e52-p119">La meilleure pratique consiste à créer un type d’informations sensibles basé sur un type existant. Utilisez la même procédure décrite plus haut dans cet article.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p119">The best practice is to create a new sensitive information type based on an existing one. Use the same process described earlier in this article.</span></span>

### <a name="example--create-a-new-sensitive-information-for-email-addresses"></a><span data-ttu-id="a0e52-215">Exemple : création d’un type d’informations sensibles pour les adresses e-mail</span><span class="sxs-lookup"><span data-stu-id="a0e52-215">Example — Create a new sensitive information for email addresses</span></span> 

<span data-ttu-id="a0e52-p120">Nous allons poursuivre avec l’adresse e-mail car il s’agit d’un exemple simple. Le tableau suivant indique les modifications recommandées pour un nouveau type d’informations sensibles de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p120">We’ll continue with the email address as an example because it’s simple. The following table details the modifications recommended for a new email sensitive information type.</span></span>

<table><span data-ttu-id="a0e52-218">
<thead>
<tr class="header">
<th align="left"><strong>Étape</strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-218">Step</span></span></th>
<th align="left"><span data-ttu-id="a0e52-219"><strong>Modification </strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-219"><strong>Modification </strong></span></span></th>
<th align="left"><span data-ttu-id="a0e52-220"><strong>Exemple de syntaxe XML</strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-220"><strong>Example XML syntax</strong></span></span></th>
</tr><span data-ttu-id="a0e52-221">
</thead>
<tbody>
<tr class="odd">
<td align="left">1</span><span class="sxs-lookup"><span data-stu-id="a0e52-221">1.</span></span></td>
<td align="left"><span data-ttu-id="a0e52-222">Définissez la propriété IdRef</span><span class="sxs-lookup"><span data-stu-id="a0e52-222">Set the IdRef property</span></span>
<p><span data-ttu-id="a0e52-p121">Dans l’élément &lt;Entity&gt;, modifiez l’élément &lt;IdMatch&gt; afin que sa propriété idRef est une valeur unique. Cette valeur pointera vers un élément qui définit notre expression régulière pour qu’elle recherche des adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p121">Within the &lt;Entity&gt; element, modify the &lt;IdMatch&gt; element so that its idRef property is = to a unique value. This value will point to an element that defines our regular expression to find email addresses.</span></span></p></td>
<td align="left"><span data-ttu-id="a0e52-225">IdRef=&quot;Regex_email_address&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-225">IdRef=&quot;Regex_email_address&quot;</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-226">2</span><span class="sxs-lookup"><span data-stu-id="a0e52-226">2</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-227">Attribut de proximité</span><span class="sxs-lookup"><span data-stu-id="a0e52-227">Proximity attribute</span></span></p>
<p><span data-ttu-id="a0e52-228">Nous allons commencer par une valeur patternProximity dans notre élément &lt;Entity&gt; de 300.</span><span class="sxs-lookup"><span data-stu-id="a0e52-228">We'll start with a patternProximity value in our &lt;Entity&gt; element of 300.</span></span></p></td>
<td align="left"><span data-ttu-id="a0e52-229">patternsProximity=&quot;300&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-229">patternsProximity=&quot;300&quot;</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="a0e52-230">3</span><span class="sxs-lookup"><span data-stu-id="a0e52-230">3</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-231">Niveau de confiance</span><span class="sxs-lookup"><span data-stu-id="a0e52-231">Confidence level</span></span></p>
<p><span data-ttu-id="a0e52-p122">Définissez la propriété recommendedConfidence sur une valeur qui représentera la probabilité de trouver une correspondance précise. Vous devrez probablement effectuer des tests avec un ensemble de données représentatif pour obtenir un résultat précis. Comme paramètre initial, définissez cette valeur sur 75.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p122">Set the recommendedConfidence property to a value you feel will represent the confidence of finding an accurate match. This will likely require testing with a representative data set to get an accurate result. As an initial setting, set this value to 75.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e52-235">recommendedConfidence=&quot;75&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-235">recommendedConfidence=&quot;75&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-236">Le code XML obtenu pour ces trois premiers éléments combinés ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="a0e52-236">The resulting XML for these first three elements combined looks like this:</span></span></p>
<p><span data-ttu-id="a0e52-237">&lt;Entity id=&quot;42e6348e-27f0-4774-9604-d470cb3e219a&quot; patternsProximity=&quot;300&quot; recommendedConfidence=&quot;75&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-237">&lt;Entity id=&quot;42e6348e-27f0-4774-9604-d470cb3e219a&quot; patternsProximity=&quot;300&quot; recommendedConfidence=&quot;75&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-238">&lt;Pattern confidenceLevel=&quot;75&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-238">&lt;Pattern confidenceLevel=&quot;75&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-239">&lt;IdMatch idRef=&quot;Regex_email_address&quot; /&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-239">&lt;IdMatch idRef=&quot;Regex_email_address&quot; /&gt;</span></span></p>
<p><span data-ttu-id="a0e52-240">&lt;Any minMatches=&quot;1&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-240">&lt;Any minMatches=&quot;1&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-241">&lt;Match idRef=&quot;Keyword_email_terms&quot; /&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-241">&lt;Match idRef=&quot;Keyword_email_terms&quot; /&gt;</span></span></p>
<p><span data-ttu-id="a0e52-242">&lt;/Any&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-242">&lt;/Any&gt;</span></span></p>
<p><span data-ttu-id="a0e52-243">&lt;/Pattern&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-243">&lt;/Pattern&gt;</span></span></p>
<p><span data-ttu-id="a0e52-244">&lt;/Entity&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-244">&lt;/Entity&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-245">4</span><span class="sxs-lookup"><span data-stu-id="a0e52-245">4</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-246">Élément Regex</span><span class="sxs-lookup"><span data-stu-id="a0e52-246">Regex element</span></span></p>
<p><span data-ttu-id="a0e52-247">Ajoutez un nouvel élément &lt;Regex&gt; immédiatement en dessous de l’élément &lt;Entity&gt; qui définit l’expression régulière utilisée pour identifier les adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="a0e52-247">Add a new &lt;Regex&gt; element immediately be below the &lt;Entity&gt; elements that defines the regular expression used to identify email addresses.</span></span></p></td>
<td align="left"><span data-ttu-id="a0e52-248">&lt;Regex id=&quot;Regex_email_address&quot;&gt;(^|\b)([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})($|\b)&lt;/Regex&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-248">&lt;Regex id=&quot;Regex_email_address&quot;&gt;(^|\b)([a-zA-Z0-9_\-\.]+)@([a-zA-Z0-9_\-\.]+)\.([a-zA-Z]{2,5})($|\b)&lt;/Regex&gt;</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="a0e52-249">5</span><span class="sxs-lookup"><span data-stu-id="a0e52-249">5</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-250">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="a0e52-250">Keywords</span></span></p>
<p><span data-ttu-id="a0e52-p123">Ajoutez un nouvel élément &lt;Keyword&gt; sous l’élément &lt;Regex&gt; qui définit la liste des mots-clés liés à des adresses e-mail. Vérifiez que la valeur id pour l’élément &lt;Keyword&gt; correspond à la valeur &lt;Match idRef&gt; dans l’élément &lt;Entity&gt;&lt;Pattern&gt;. Vous pouvez continuer à ajouter vos propres mots-clés, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p123">Add a new &lt;Keyword&gt; element below the &lt;Regex&gt; element that defines list of email address related keywords. Ensure that the id value for the &lt;Keyword&gt; element matches the &lt;Match idRef&gt; value in the &lt;Entity&gt;&lt;Pattern&gt; element. You may continue to add your own keywords if needed.</span></span></p>
<p><span data-ttu-id="a0e52-p124">Il n’est probablement pas nécessaire d’inclure des mots-clés dans un type d’informations sensibles de messagerie. Ceux-ci sont fournis en guise d’exemple.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p124">Keywords are likely not necessary to include in an email sensitive information type. These are provided as an example.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e52-256">&lt;Keyword id=&quot;Keyword_email_terms&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-256">&lt;Keyword id=&quot;Keyword_email_terms&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-257">&lt;Group&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-257">&lt;Group&gt;</span></span></p>
<p><span data-ttu-id="a0e52-258">&lt;Term&gt;email&lt;/Term&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-258">&lt;Term&gt;email&lt;/Term&gt;</span></span></p>
<p><span data-ttu-id="a0e52-259">&lt;Term&gt;email address&lt;/Term&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-259">&lt;Term&gt;email address&lt;/Term&gt;</span></span></p>
<p><span data-ttu-id="a0e52-260">&lt;Term&gt;contact&lt;/Term&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-260">&lt;Term&gt;contact&lt;/Term&gt;</span></span></p>
<p><span data-ttu-id="a0e52-261">&lt;/Group&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-261">&lt;/Group&gt;</span></span></p>
<p><span data-ttu-id="a0e52-262">&lt;/Keyword&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-262">&lt;/Keyword&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-263">6</span><span class="sxs-lookup"><span data-stu-id="a0e52-263">6</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-264">Élément LocalizedStrings</span><span class="sxs-lookup"><span data-stu-id="a0e52-264">LocalizedStrings element</span></span></p>
<p><span data-ttu-id="a0e52-265">Dans l’élément &lt;LocalizedStrings&gt;&lt;Resource&gt;, vérifiez que vous avez un nom unique qui identifie votre type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="a0e52-265">In the &lt;LocalizedStrings&gt;&lt;Resource&gt; element ensure that you have a unique name that identifies your sensitive information type.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0e52-266">&lt;LocalizedStrings&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-266">&lt;LocalizedStrings&gt;</span></span></p>
<p><span data-ttu-id="a0e52-267">&lt;Resource idRef=&quot;42e6348e-27f0-4774-9604-d470cb3e219a&quot;&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-267">&lt;Resource idRef=&quot;42e6348e-27f0-4774-9604-d470cb3e219a&quot;&gt;</span></span></p>
<p><span data-ttu-id="a0e52-268">&lt;Name default=&quot;true&quot; langcode=&quot;en-us&quot;&gt;Email Address&lt;/Name&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-268">&lt;Name default=&quot;true&quot; langcode=&quot;en-us&quot;&gt;Email Address&lt;/Name&gt;</span></span></p>
<p><span data-ttu-id="a0e52-269">&lt;Description default=&quot;true&quot; langcode=&quot;en-us&quot;&gt;Detects email addresses.&lt;/Description&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-269">&lt;Description default=&quot;true&quot; langcode=&quot;en-us&quot;&gt;Detects email addresses.&lt;/Description&gt;</span></span></p>
<p><span data-ttu-id="a0e52-270">&lt;/Resource&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-270">&lt;/Resource&gt;</span></span></p>
<p><span data-ttu-id="a0e52-271">&lt;/LocalizedStrings&gt;</span><span class="sxs-lookup"><span data-stu-id="a0e52-271">&lt;/LocalizedStrings&gt;</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="create-a-new-sensitive-information-type-with-example-powershell-and-xml-file--contoso-customer-number"></a><span data-ttu-id="a0e52-272">Création d’un type d’informations sensibles avec un exemple de fichier XML et PowerShell : numéro de client Contoso</span><span class="sxs-lookup"><span data-stu-id="a0e52-272">Create a new sensitive information type with example PowerShell and XML file — Contoso customer number</span></span>

<span data-ttu-id="a0e52-p125">Contoso utilise un numéro de client Contoso (CCN) pour identifier chaque client dans sa base de données clients. Un CCN est constitué de la taxonomie suivante :</span><span class="sxs-lookup"><span data-stu-id="a0e52-p125">Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following taxonomy:</span></span>

-   <span data-ttu-id="a0e52-p126">Deux chiffres qui représentent l’année de création de l’enregistrement. Contoso a été fondée en 2002 ; par conséquent, la valeur la plus précoce serait 02.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p126">Two digits to represent the year that the record was created. Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span>

-   <span data-ttu-id="a0e52-p127">Trois chiffres qui représentent l’agence partenaire qui a créé l’enregistrement. La plage des valeurs possibles pour les agences se situe entre 000 et 999.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p127">Three digits to represent the partner agency that created the record. Possible agency values range from 000 to 999.</span></span>

-   <span data-ttu-id="a0e52-p128">Un caractère alpha qui représente la ligne de l’entreprise. Les valeurs possibles sont les caractères de a à z et doivent respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p128">An alpha character to represent the line of business. Possible values are a-z and should be case insensitive.</span></span>

-   <span data-ttu-id="a0e52-p129">Un numéro de série à quatre chiffres. La plage des valeurs de numéro de série possible est comprise entre 0000 et 9999.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p129">A four-digit serial number. Possible serial number values range from 0000 to 9999.</span></span>

<span data-ttu-id="a0e52-283">Exemples de CCN :</span><span class="sxs-lookup"><span data-stu-id="a0e52-283">Example CCNs:</span></span>

> <span data-ttu-id="a0e52-284">15080P9562</span><span class="sxs-lookup"><span data-stu-id="a0e52-284">15080P9562</span></span>
>
> <span data-ttu-id="a0e52-285">14040O1119</span><span class="sxs-lookup"><span data-stu-id="a0e52-285">14040O1119</span></span>
>
> <span data-ttu-id="a0e52-286">15020J8317</span><span class="sxs-lookup"><span data-stu-id="a0e52-286">15020J8317</span></span>
>
> <span data-ttu-id="a0e52-287">14050E2330</span><span class="sxs-lookup"><span data-stu-id="a0e52-287">14050E2330</span></span>
>
> <span data-ttu-id="a0e52-288">16050E2166</span><span class="sxs-lookup"><span data-stu-id="a0e52-288">16050E2166</span></span>
>
> <span data-ttu-id="a0e52-289">17040O1118</span><span class="sxs-lookup"><span data-stu-id="a0e52-289">17040O1118</span></span>

<span data-ttu-id="a0e52-290">Contoso fait toujours référence aux clients en utilisant un CCN dans la correspondance interne, la correspondance externe, les documents, etc. Il souhaite créer un type d’informations sensibles personnalisé pour détecter l’utilisation d’un CCN dans Office 365 pour appliquer la protection à l’utilisation de ce formulaire de données personnelles.</span><span class="sxs-lookup"><span data-stu-id="a0e52-290">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, etc. They would like to create a custom sensitive information type to detect the use of CCN in Office 365 so that they may apply protection to the use of this form of personal data.</span></span>

### <a name="create-a-new-sensitive-information-type-for-contoso-customer-number"></a><span data-ttu-id="a0e52-291">Création d’un type d’informations sensibles pour un numéro de client Contoso</span><span class="sxs-lookup"><span data-stu-id="a0e52-291">Create a new sensitive information type for Contoso customer number</span></span>

<table><span data-ttu-id="a0e52-292">
<thead>
<tr class="header">
<th align="left"><strong>Étape</strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-292">Step</span></span></th>
<th align="left"><span data-ttu-id="a0e52-293"><strong>Action </strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-293"><strong>Action </strong></span></span></th>
<th align="left"><span data-ttu-id="a0e52-294"><strong>Résultat</strong></span><span class="sxs-lookup"><span data-stu-id="a0e52-294"><strong>Result</strong></span></span></th>
</tr><span data-ttu-id="a0e52-295">
</thead>
<tbody>
<tr class="odd">
<td align="left">1</span><span class="sxs-lookup"><span data-stu-id="a0e52-295">1.</span></span></td>
<td align="left"><span data-ttu-id="a0e52-296">Contoso utilise PowerShell et la recherche de contenu pour rechercher des documents qui correspondent à un exemple de jeu de CCN.</span><span class="sxs-lookup"><span data-stu-id="a0e52-296">Contoso uses PowerShell and Content Search to find documents that match an example set of CCNs.</span></span></td>
<td align="left">

<p><span data-ttu-id="a0e52-297">#Se connecter au Centre de sécurité et de conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="a0e52-297">#Connect to Office 365 Security &amp; Compliance Center</span></span></p>
<p><span data-ttu-id="a0e52-298">$adminUser = &quot;alland@contoso.com&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-298">$adminUser = &quot;alland@contoso.com&quot;</span></span></p>
<p><span data-ttu-id="a0e52-299">Connect-IPPSSession -UserPrincipalName $adminUser</span><span class="sxs-lookup"><span data-stu-id="a0e52-299">Connect-IPPSSession -UserPrincipalName $adminUser</span></span></p>
<p><span data-ttu-id="a0e52-300">#Créer et lancer une recherche pour un exemple de données</span><span class="sxs-lookup"><span data-stu-id="a0e52-300">#Create &amp; start search for sample data</span></span></p>
<p><span data-ttu-id="a0e52-301">$searchName = &quot;Sample Customer Information Search&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-301">$searchName = &quot;Sample Customer Information Search&quot;</span></span></p>
<p><span data-ttu-id="a0e52-302">$searchQuery = &quot;15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-302">$searchQuery = &quot;15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118&quot;</span></span></p>
<p><span data-ttu-id="a0e52-303">New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery</span><span class="sxs-lookup"><span data-stu-id="a0e52-303">New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery</span></span></p>
<p><span data-ttu-id="a0e52-304">Start-ComplianceSearch -Identity $searchName</span><span class="sxs-lookup"><span data-stu-id="a0e52-304">Start-ComplianceSearch -Identity $searchName</span></span></p>
</td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-305">2</span><span class="sxs-lookup"><span data-stu-id="a0e52-305">2</span></span></td>
<td align="left"><span data-ttu-id="a0e52-p130">Contoso analyse les résultats. Chaque fois que le CCN a été utilisé, une date au format européen mis en forme a été utilisée et l’un de ces mots-clés a été utilisé également dans une proximité de 300 caractères.</span><span class="sxs-lookup"><span data-stu-id="a0e52-p130">Contoso analyzes the results. Every time the CCN was used, an EU formatted date was used and one of these keywords were also used within a proximity of 300 characters.</span></span></td>
<td align="left"><span data-ttu-id="a0e52-308">customer number, customer no, customer #, customer#, Contoso customer</span><span class="sxs-lookup"><span data-stu-id="a0e52-308">customer number, customer no, customer #, customer#, Contoso customer</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="a0e52-309">3</span><span class="sxs-lookup"><span data-stu-id="a0e52-309">3</span></span></td>
<td align="left"><span data-ttu-id="a0e52-310">Contoso a développé le modèle d’expression régulière (RegEx) suivant afin d’identifier son CCN.</span><span class="sxs-lookup"><span data-stu-id="a0e52-310">Contoso developed the following Regular Expression (RegEx) pattern to identify their CCN.</span></span></td>
<td align="left"><span data-ttu-id="a0e52-311">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</span><span class="sxs-lookup"><span data-stu-id="a0e52-311">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-312">4</span><span class="sxs-lookup"><span data-stu-id="a0e52-312">4</span></span></td>
<td align="left"><span data-ttu-id="a0e52-313">Contoso a développé le modèle d’expression régulière (RegEx) suivant pour identifier les dates européennes aux formats utilisés par ses différentes filiales.</span><span class="sxs-lookup"><span data-stu-id="a0e52-313">Contoso developed the following Regular Expression (RegEx) pattern to identify EU dates in the formats used by their various subsidiaries.</span></span></td>
<td align="left">
````xml
(0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)?|‌ feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|‌ apr(ile|il)?|abr(il)?|avril|may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|‌ oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)?|nov(ember|iembre|embre|embro)?|dec(ember)?|‌ dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}
````
</td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="a0e52-314">5</span><span class="sxs-lookup"><span data-stu-id="a0e52-314">5</span></span></td>
<td align="left"><span data-ttu-id="a0e52-315">Contoso utilise PowerShell pour générer trois GUID uniques.</span><span class="sxs-lookup"><span data-stu-id="a0e52-315">Contoso uses PowerShell to generate three unique GUIDs.</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-316">#Générer un GUID unique pour RulePack Id, Publisher Id et Entity Id</span><span class="sxs-lookup"><span data-stu-id="a0e52-316">#Generate a unique GUID for RulePack Id, Publisher Id, and Entity Id</span></span></p>
<p>[guid]::NewGuid().Guid</p>
<p>[guid]::NewGuid().Guid</p>
<p>[guid]::NewGuid().Guid</p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-317">6</span><span class="sxs-lookup"><span data-stu-id="a0e52-317">6</span></span></td>
<td align="left"><span data-ttu-id="a0e52-318">Contoso définit les paramètres suivants pour sa règle de type d’élément sensible.</span><span class="sxs-lookup"><span data-stu-id="a0e52-318">Contoso defines the following parameters for their sensitive item type rule.</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-319">Nom : Numéro de client Contoso (CCN)</span><span class="sxs-lookup"><span data-stu-id="a0e52-319">Name: Contoso Customer Number (CCN)</span></span></p>
<p><span data-ttu-id="a0e52-320">Description : Numéro de client Contoso (CCN) qui recherche des mots-clés supplémentaires et une date au format européen</span><span class="sxs-lookup"><span data-stu-id="a0e52-320">Description: Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="a0e52-321">7</span><span class="sxs-lookup"><span data-stu-id="a0e52-321">7</span></span></td>
<td align="left"><span data-ttu-id="a0e52-322">Contoso crée un fichier XML pour un nouveau type d’informations sensibles pour détecter un numéro de client Contoso (CCN) et l’enregistre dans un système de fichiers local C:\Scripts\ContosoCCN.xml avec codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="a0e52-322">Contoso creates an XML file for a new sensitive information type to detect a Contoso Customer Number (CCN) and saves this to a local file system as C:\Scripts\ContosoCCN.xml in with UTF-8 encoding.</span></span></td>
<td align="left"><span data-ttu-id="a0e52-323">Reportez-vous au fichier XML sous ce tableau.</span><span class="sxs-lookup"><span data-stu-id="a0e52-323">See the XML file below this table.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="a0e52-324">8</span><span class="sxs-lookup"><span data-stu-id="a0e52-324">8</span></span></td>
<td align="left"><span data-ttu-id="a0e52-325">Contoso crée le type d’informations sensibles personnalisé avec le PowerShell suivant.</span><span class="sxs-lookup"><span data-stu-id="a0e52-325">Contoso creates the custom sensitive information type with the following PowerShell.</span></span></td>
<td align="left"><p><span data-ttu-id="a0e52-326">#Se connecter au Centre de sécurité et de conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="a0e52-326">#Connect to Office 365 Security &amp; Compliance Center</span></span></p>
<p><span data-ttu-id="a0e52-327">$adminUser = &quot;alland@contoso.com&quot;</span><span class="sxs-lookup"><span data-stu-id="a0e52-327">$adminUser = &quot;alland@contoso.com&quot;</span></span></p>
<p><span data-ttu-id="a0e52-328">Connect-IPPSSession -UserPrincipalName $adminUser</span><span class="sxs-lookup"><span data-stu-id="a0e52-328">Connect-IPPSSession -UserPrincipalName $adminUser</span></span></p>
<p><span data-ttu-id="a0e52-329">#Créer un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a0e52-329">#Create new Sensitive Information Type</span></span></p>
<p><span data-ttu-id="a0e52-330">New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path &quot;C:\Scripts\ContosoCCN.xml&quot; -Encoding Byte -ReadCount 0)</span><span class="sxs-lookup"><span data-stu-id="a0e52-330">New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path &quot;C:\Scripts\ContosoCCN.xml&quot; -Encoding Byte -ReadCount 0)</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="example-xml-file-for-the-new-sensitive-information-type-step-7"></a><span data-ttu-id="a0e52-331">Exemple de fichier XML pour le nouveau type d’informations sensibles (étape 7)</span><span class="sxs-lookup"><span data-stu-id="a0e52-331">Example XML file for the new sensitive information type (step 7)</span></span>
```xml
\<?xml version="1.0" encoding="utf-8"?\>

\<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce"\>

\<RulePack id="130ae63b-a91e-4a12-9e02-a90e36a83d7f"\>

\<Version major="1" minor="0" build="0" revision="0" /\>

\<Publisher id="47148982-defd-42a1-890a-7b9472099f1f" /\>

\<Details defaultLangCode="en"\>

\<LocalizedDetails langcode="en"\>

\<PublisherName\>Contoso Ltd.\</PublisherName\>

\<Name\>Contoso Rule Package\</Name\>

\<Description\>Defines Contoso's custom set of classification rules\</Description\>

\</LocalizedDetails\>

\</Details\>

\</RulePack\>

\<Rules\>

\<!-- Contoso Customer Number (CCN) --\>

\<Entity id="a91f9a2e-6cfc-4622-8c5d-954875aa5b2b" patternsProximity="300" recommendedConfidence="85"\>

\<Pattern confidenceLevel="85"\>

\<IdMatch idRef="Regex\_contoso\_ccn" /\>

\<Match idRef="Keyword\_contoso\_ccn" /\>

\<Match idRef="Regex\_eu\_date" /\>

\</Pattern\>

\</Entity\>

\<Regex id="Regex\_contoso\_ccn"\>[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}\</Regex\>

\<Keyword id="Keyword\_contoso\_ccn"\>

\<Group matchStyle="word"\>

\<Term caseSensitive="false"\>customer number\</Term\>

\<Term caseSensitive="false"\>customer no\</Term\>

\<Term caseSensitive="false"\>customer \#\</Term\>

\<Term caseSensitive="false"\>customer\#\</Term\>

\<Term caseSensitive="false"\>Contoso customer\</Term\>

\</Group\>

\</Keyword\>

\<Regex id="Regex\_eu\_date"\> (0?[1-9]|[12][0-9]|3[0-1])[\\/-](0?[1-9]|1[0-2]|j\\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)?‌ |feb(ruary|ruari|rero|braio|ruar|br)?|f\\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\\x00e4rz|maart‌|apr(ile|il)?|abr(il)?|avril‌ |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)?‌ |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\\x00e9c(embre)?)[ \\/-](19|20)?[0-9]{2}\</Regex\>

\<LocalizedStrings\>

\<Resource idRef="a91f9a2e-6cfc-4622-8c5d-954875aa5b2b"\>

\<Name default="true" langcode="en-us"\>Contoso Customer Number (CCN)\</Name\>

\<Description default="true" langcode="en-us"\>Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date\</Description\>

\</Resource\>

\</LocalizedStrings\>

\</Rules\>

\</RulePackage\>
```
