---
title: En savoir plus sur les types d’informations sensibles
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
search.appverid: MET150
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: ''
ms.openlocfilehash: 12a4e8873cb7212bfa7dde12bba9e98528cd859a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919670"
---
# <a name="learn-about-sensitive-information-types"></a><span data-ttu-id="c21df-102">En savoir plus sur les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c21df-102">Learn about sensitive information types</span></span>

<span data-ttu-id="c21df-103">L’identification et la classification des éléments sensibles qui sont sous le contrôle de votre organisation est la première étape de la [protection des informations.](./information-protection.md)</span><span class="sxs-lookup"><span data-stu-id="c21df-103">Identifying and classifying sensitive items that are under your organizations control is the first step in the [Information Protection discipline](./information-protection.md).</span></span>  <span data-ttu-id="c21df-104">Microsoft 365 propose trois façons d’identifier les éléments afin qu’ils soient classés :</span><span class="sxs-lookup"><span data-stu-id="c21df-104">Microsoft 365 provides three ways of identifying items so that they can be classified:</span></span>

- <span data-ttu-id="c21df-105">manuellement par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c21df-105">manually by users</span></span>
- <span data-ttu-id="c21df-106">reconnaissance automatique des modèles, comme les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c21df-106">automated pattern recognition, like sensitive information types</span></span>
- [<span data-ttu-id="c21df-107">apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="c21df-107">machine learning</span></span>](classifier-learn-about.md)

<span data-ttu-id="c21df-108">Les types d’informations sensibles sont des classifieurs basés sur des modèles.</span><span class="sxs-lookup"><span data-stu-id="c21df-108">Sensitive information types are pattern-based classifiers.</span></span> <span data-ttu-id="c21df-109">Ils détectent les informations sensibles telles que la sécurité sociale, la carte bancaire ou les numéros de compte bancaire pour identifier les éléments [sensibles. Voir Définitions d’entités des types d’informations sensibles](sensitive-information-type-entity-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="c21df-109">They detect sensitive information like social security, credit card, or bank account numbers to identify sensitive items, see [Sensitive information types entity definitions](sensitive-information-type-entity-definitions.md)</span></span>

## <a name="sensitive-information-types-are-used-in"></a><span data-ttu-id="c21df-110">Les types d’informations sensibles sont utilisés dans</span><span class="sxs-lookup"><span data-stu-id="c21df-110">Sensitive information types are used in</span></span>

- [<span data-ttu-id="c21df-111">Stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="c21df-111">Data loss prevention policies</span></span>](data-loss-prevention-policies.md) 
- [<span data-ttu-id="c21df-112">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="c21df-112">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="c21df-113">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="c21df-113">Retention labels</span></span>](retention.md)
- [<span data-ttu-id="c21df-114">Conformité des communications</span><span class="sxs-lookup"><span data-stu-id="c21df-114">Communication compliance</span></span>](communication-compliance.md)
- [<span data-ttu-id="c21df-115">Stratégies de étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="c21df-115">Auto-labelling policies</span></span>](apply-sensitivity-label-automatically.md#how-to-configure-auto-labeling-for-office-apps)

## <a name="fundamental-parts-of-a-sensitive-information-type"></a><span data-ttu-id="c21df-116">Parties fondamentales d’un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c21df-116">Fundamental parts of a sensitive information type</span></span>

<span data-ttu-id="c21df-117">Chaque entité de type d’informations sensibles est définie par les champs ci-après :</span><span class="sxs-lookup"><span data-stu-id="c21df-117">Every sensitive information type entity is defined by these fields:</span></span>

- <span data-ttu-id="c21df-118">name: how the sensitive information type is referred to</span><span class="sxs-lookup"><span data-stu-id="c21df-118">name: how the sensitive information type is referred to</span></span>
- <span data-ttu-id="c21df-119">description : décrit ce que le type d’informations sensibles recherche</span><span class="sxs-lookup"><span data-stu-id="c21df-119">description: describes what the sensitive information type is looking for</span></span>
- <span data-ttu-id="c21df-120">modèle : un modèle définit ce qu’un type d’informations sensibles détecte.</span><span class="sxs-lookup"><span data-stu-id="c21df-120">pattern: A pattern defines what a sensitive information type detects.</span></span> <span data-ttu-id="c21df-121">Il se compose des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="c21df-121">It consists of the following components</span></span>
    - <span data-ttu-id="c21df-122">Élément principal : élément principal que le type d’informations sensibles recherche.</span><span class="sxs-lookup"><span data-stu-id="c21df-122">Primary element – the main element that the sensitive information type is looking for.</span></span> <span data-ttu-id="c21df-123">Il peut s’agit **d’une expression** régulière avec ou sans validation de la liste de contrôle, d’une liste de mots **clés,** d’un dictionnaire de mots clés **ou** d’une **fonction.**</span><span class="sxs-lookup"><span data-stu-id="c21df-123">It can be a **regular expression** with or without a checksum validation, a **keyword list**, a **keyword dictionary**, or a **function**.</span></span>
    - <span data-ttu-id="c21df-124">Élément de prise en charge : éléments qui agissent comme des preuves qui contribuent à augmenter la confiance de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="c21df-124">Supporting element – elements that act as supporting evidence that help in increasing the confidence of the match.</span></span> <span data-ttu-id="c21df-125">Par exemple, le mot clé « SSN » à proximité d’un numéro SSN.</span><span class="sxs-lookup"><span data-stu-id="c21df-125">For example, keyword “SSN” in proximity of an SSN number.</span></span> <span data-ttu-id="c21df-126">Il peut s’agit d’une expression régulière avec ou sans validation de la liste de contrôle, d’une liste de mots clés, d’un dictionnaire de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c21df-126">It can be a regular expression with or without a checksum validation, keyword list, keyword dictionary.</span></span>
    - <span data-ttu-id="c21df-127">Niveau de confiance : les niveaux de confiance (élevé, moyen, faible) reflètent la quantité de preuves justificatives détectées avec l’élément principal.</span><span class="sxs-lookup"><span data-stu-id="c21df-127">Confidence Level - Confidence levels (high, medium, low) reflect how much supporting evidence was detected along with the primary element.</span></span> <span data-ttu-id="c21df-128">Plus la preuve justificative qu’un élément contient est importante, plus la confiance qu’un élément correspond contient les informations sensibles que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c21df-128">The more supporting evidence an item contains, the higher the confidence that a matched item contains the sensitive info you're looking for.</span></span>
    - <span data-ttu-id="c21df-129">Proximité : nombre de caractères entre l’élément principal et l’élément de prise en charge</span><span class="sxs-lookup"><span data-stu-id="c21df-129">Proximity – Number of characters between primary and supporting element</span></span>

![Diagramme de la fenêtre de proximité et de preuves probantes](../media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

<span data-ttu-id="c21df-131">En savoir plus sur les niveaux de confiance dans cette vidéo</span><span class="sxs-lookup"><span data-stu-id="c21df-131">Learn more about confidence levels in this video</span></span>


 > [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Hx60]  

### <a name="example-sensitive-information-type"></a><span data-ttu-id="c21df-132">Exemple de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c21df-132">Example sensitive information type</span></span>


## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="c21df-133">Numéro d’identité nationale (DNI) argentine</span><span class="sxs-lookup"><span data-stu-id="c21df-133">Argentina national identity (DNI) number</span></span>

### <a name="format"></a><span data-ttu-id="c21df-134">Format</span><span class="sxs-lookup"><span data-stu-id="c21df-134">Format</span></span>

<span data-ttu-id="c21df-135">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="c21df-135">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="c21df-136">Modèle</span><span class="sxs-lookup"><span data-stu-id="c21df-136">Pattern</span></span>

<span data-ttu-id="c21df-137">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="c21df-137">Eight digits:</span></span>
- <span data-ttu-id="c21df-138">deux chiffres</span><span class="sxs-lookup"><span data-stu-id="c21df-138">two digits</span></span>
- <span data-ttu-id="c21df-139">un point</span><span class="sxs-lookup"><span data-stu-id="c21df-139">a period</span></span>
- <span data-ttu-id="c21df-140">trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c21df-140">three digits</span></span>
- <span data-ttu-id="c21df-141">un point</span><span class="sxs-lookup"><span data-stu-id="c21df-141">a period</span></span>
- <span data-ttu-id="c21df-142">trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c21df-142">three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c21df-143">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c21df-143">Checksum</span></span>

<span data-ttu-id="c21df-144">Non</span><span class="sxs-lookup"><span data-stu-id="c21df-144">No</span></span>

### <a name="definition"></a><span data-ttu-id="c21df-145">Définition</span><span class="sxs-lookup"><span data-stu-id="c21df-145">Definition</span></span>

<span data-ttu-id="c21df-146">Une stratégie DLP a un niveau de confiance moyen qu’elle a détecté ce type d’informations sensibles si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c21df-146">A DLP policy has medium confidence that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c21df-147">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c21df-147">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c21df-148">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c21df-148">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c21df-149">Mots-clés</span><span class="sxs-lookup"><span data-stu-id="c21df-149">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="c21df-150">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="c21df-150">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="c21df-151">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="c21df-151">Argentina National Identity number</span></span> 
- <span data-ttu-id="c21df-152">Identité</span><span class="sxs-lookup"><span data-stu-id="c21df-152">Identity</span></span> 
- <span data-ttu-id="c21df-153">Carte d’identité nationale d’identification</span><span class="sxs-lookup"><span data-stu-id="c21df-153">Identification National Identity Card</span></span> 
- <span data-ttu-id="c21df-154">DNI</span><span class="sxs-lookup"><span data-stu-id="c21df-154">DNI</span></span> 
- <span data-ttu-id="c21df-155">Registre national des personnes de la NIC</span><span class="sxs-lookup"><span data-stu-id="c21df-155">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="c21df-156">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="c21df-156">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="c21df-157">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="c21df-157">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="c21df-158">Identidad</span><span class="sxs-lookup"><span data-stu-id="c21df-158">Identidad</span></span> 
- <span data-ttu-id="c21df-159">Identificación</span><span class="sxs-lookup"><span data-stu-id="c21df-159">Identificación</span></span> 

### <a name="more-on-confidence-levels"></a><span data-ttu-id="c21df-160">Plus d’informations sur les niveaux de confiance</span><span class="sxs-lookup"><span data-stu-id="c21df-160">More on confidence levels</span></span>

<span data-ttu-id="c21df-161">Dans une définition d’entité  de type d’informations sensibles, le niveau de confiance reflète la quantité de preuves justificatives détectées en plus de l’élément principal.</span><span class="sxs-lookup"><span data-stu-id="c21df-161">In a sensitive information type entity definition, **confidence level** reflects how much supporting evidence is detected in addition to the primary element.</span></span> <span data-ttu-id="c21df-162">Plus la preuve justificative qu’un élément contient est importante, plus la confiance qu’un élément correspond contient les informations sensibles que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c21df-162">The more supporting evidence an item contains, the higher the confidence that a matched item contains the sensitive info you're looking for.</span></span> <span data-ttu-id="c21df-163">Par exemple, les correspondances avec un niveau de confiance élevé contiennent davantage de preuves justificatives à proximité immédiate de l’élément principal, tandis que les correspondances avec un niveau de confiance faible contiennent peu ou pas de preuves justificatives à proximité immédiate.</span><span class="sxs-lookup"><span data-stu-id="c21df-163">For example, matches with a high confidence level will contain more supporting evidence in close proximity of the primary element, whereas matches with a low confidence level would contain little to no supporting evidence in close proximity.</span></span> 

<span data-ttu-id="c21df-164">Un niveau de confiance élevé renvoie le moins de faux positifs, mais peut entraîner davantage de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c21df-164">A high confidence level returns the fewest false positives but might result in more false negatives.</span></span> <span data-ttu-id="c21df-165">Les niveaux de confiance faibles ou moyens renvoient plus de faux positifs, mais peu à zéro faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c21df-165">Low or medium confidence levels returns more false positives but few to zero false negatives.</span></span>

- <span data-ttu-id="c21df-166">**faible niveau de** confiance : valeur 65, les éléments qui correspondent contiennent le moins de faux négatifs, mais le plus de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="c21df-166">**low confidence**: Value of 65, matched items will contain the fewest false negatives but the most false positives.</span></span> <span data-ttu-id="c21df-167">Une confiance faible renvoie toutes les correspondances de confiance faible, moyenne et élevée.</span><span class="sxs-lookup"><span data-stu-id="c21df-167">Low confidence returns all low, medium, and high confidence matches.</span></span>
- <span data-ttu-id="c21df-168">**confiance moyenne**: valeur de 75, les éléments qui correspondent contiennent une quantité moyenne de faux positifs et de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c21df-168">**medium confidence**: Value of 75, matched items will contain an average amount of false positives and false negatives.</span></span> <span data-ttu-id="c21df-169">Une confiance moyenne renvoie toutes les correspondances de confiance moyenne et élevée.</span><span class="sxs-lookup"><span data-stu-id="c21df-169">Medium confidence returns all medium, and high confidence matches.</span></span>  
- <span data-ttu-id="c21df-170">**niveau de confiance** élevé : valeur 85, les éléments qui correspondent contiennent le moins de faux positifs, mais le plus de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c21df-170">**high confidence**: Value of 85, matched items will contain the fewest false positives but the most false negatives.</span></span> <span data-ttu-id="c21df-171">Un niveau de confiance élevé renvoie uniquement des correspondances à haut niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="c21df-171">High confidence only returns high confidence matches.</span></span>  

<span data-ttu-id="c21df-172">Vous devez utiliser des modèles de niveau de confiance élevé avec un nombre faible, par ex. 5 à 10, et des modèles de confiance faible avec des nombres plus élevés, par ex. 20 ou plus.</span><span class="sxs-lookup"><span data-stu-id="c21df-172">You should use high confidence level patterns with low counts, say five to ten, and low confidence patterns with higher counts, say 20 or more.</span></span>

> [!NOTE]
> <span data-ttu-id="c21df-173">Si vous avez des stratégies existantes ou des types d’informations sensibles personnalisés (SIT) définis à l’aide de niveaux de confiance basés sur le nombre (également défini comme précision), ils seront automatiquement mappés aux trois niveaux de confiance discrets ; confiance faible, confiance moyenne et confiance élevée, dans l’interface utilisateur du Centre de sécurité @ conformité.</span><span class="sxs-lookup"><span data-stu-id="c21df-173">If you have existing policies or custom sensitive information types (SITs) defined using number-based confidence levels (also know as accuracy), they will automatically be mapped to the three discrete confidence levels; low confidence, medium confidence, and high confidence, across the Security @ Compliance Center UI.</span></span>
> - <span data-ttu-id="c21df-174">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance entre 76 et 100 seront mappées à un niveau de confiance élevé.</span><span class="sxs-lookup"><span data-stu-id="c21df-174">All policies with minimum accuracy or custom SIT patterns with confidence levels of between 76 and 100 will be mapped to high confidence.</span></span> 
> - <span data-ttu-id="c21df-175">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance entre 66 et 75 seront mappées à un niveau de confiance moyen.</span><span class="sxs-lookup"><span data-stu-id="c21df-175">All policies with minimum accuracy or custom SIT patterns with confidence levels of between 66 and 75 will be mapped to medium confidence.</span></span>
> - <span data-ttu-id="c21df-176">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance inférieurs ou égaux à 65 seront mappées à un niveau de confiance faible.</span><span class="sxs-lookup"><span data-stu-id="c21df-176">All policies with minimum accuracy or custom SIT patterns with confidence levels less than or equal to 65 will be mapped to low confidence.</span></span> 

## <a name="creating-custom-sensitive-information-types"></a><span data-ttu-id="c21df-177">Création de types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="c21df-177">Creating custom sensitive information types</span></span>

<span data-ttu-id="c21df-178">Pour créer des types d’informations sensibles personnalisés dans le Centre de sécurité et conformité, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c21df-178">To create custom sensitive information types in the Security & Compliance Center, you can choose from several options:</span></span>

- <span data-ttu-id="c21df-179">**Utiliser l’interface utilisateur** Vous pouvez configurer un type d’informations sensibles personnalisé à l’aide de l’interface utilisateur du Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="c21df-179">**Use the UI** You can set up a custom sensitive information type using the Security & Compliance Center UI.</span></span> <span data-ttu-id="c21df-180">Cette méthode vous permet d’utiliser des expressions régulières, des mots clés et des dictionnaires de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c21df-180">With this method, you can use regular expressions, keywords, and keyword dictionaries.</span></span> <span data-ttu-id="c21df-181">Pour en savoir plus, voir [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="c21df-181">To learn more, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

- <span data-ttu-id="c21df-182">**Utiliser EDM** Vous pouvez configurer des types d’informations sensibles personnalisés à l’aide d’une classification de correspondance exacte des données (EDM).</span><span class="sxs-lookup"><span data-stu-id="c21df-182">**Use EDM** You can set up custom sensitive information types using Exact Data Match (EDM)-based classification.</span></span> <span data-ttu-id="c21df-183">Cette méthode vous permet de créer un type d’informations sensibles dynamique à l’aide d’une base de données sécurisée que vous pouvez actualiser régulièrement.</span><span class="sxs-lookup"><span data-stu-id="c21df-183">This method enables you to create a dynamic sensitive information type using a secure database that you can refresh periodically.</span></span> <span data-ttu-id="c21df-184">Voir l’article sur la [création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span><span class="sxs-lookup"><span data-stu-id="c21df-184">See [Create a custom sensitive information type with Exact Data Match based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

- <span data-ttu-id="c21df-185">**Utiliser PowerShell** vous pouvez configurer des types d’informations sensibles personnalisés à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c21df-185">**Use PowerShell** You can set up custom sensitive information types using PowerShell.</span></span> <span data-ttu-id="c21df-186">Bien que cette méthode soit plus complexe que celle de l’interface utilisateur, elle offre davantage d’options de configuration.</span><span class="sxs-lookup"><span data-stu-id="c21df-186">Although this method is more complex than using the UI, you have more configuration options.</span></span> <span data-ttu-id="c21df-187">Voir [Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c21df-187">See [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>



> [!NOTE]
> <span data-ttu-id="c21df-188">Des niveaux de confiance améliorés sont disponibles pour une utilisation immédiate dans le cadre de la protection contre la perte de données pour les services Microsoft 365, la Protection des informations Microsoft pour les services Microsoft 365, la conformité des communications, la gouvernance des informations et la gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c21df-188">Improved confidence levels are available for immediate use within Data Loss Prevention for Microsoft 365 services, Microsoft Information Protection for Microsoft 365 services, Communication Compliance, Information Governance, and Records Management.</span></span>

> <span data-ttu-id="c21df-189">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="c21df-189">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="c21df-190">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="c21df-190">Chinese (simplified)</span></span>
> - <span data-ttu-id="c21df-191">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="c21df-191">Chinese (traditional)</span></span>
> - <span data-ttu-id="c21df-192">Korean</span><span class="sxs-lookup"><span data-stu-id="c21df-192">Korean</span></span>
> - <span data-ttu-id="c21df-193">Japanese</span><span class="sxs-lookup"><span data-stu-id="c21df-193">Japanese</span></span>

><span data-ttu-id="c21df-194">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="c21df-194">This support is available for sensitive information types.</span></span> <span data-ttu-id="c21df-195">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="c21df-195">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

## <a name="for-further-information"></a><span data-ttu-id="c21df-196">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c21df-196">For further information</span></span>
- [<span data-ttu-id="c21df-197">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c21df-197">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="c21df-198">Créer un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="c21df-198">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
- [<span data-ttu-id="c21df-199">Créer un type d’informations sensibles personnalisé dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c21df-199">Create a custom sensitive information type in PowerShell</span></span>](create-a-custom-sensitive-information-type-in-scc-powershell.md)

<!-- fwlink for this topic https://go.microsoft.com/fwlink/?linkid=2135644-->