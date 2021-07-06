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
ms.openlocfilehash: 3f64b981b60db9f9089af0555e4bf734864913b9
ms.sourcegitcommit: 17d82e5617f0466eb825e15ab88594afcdaf4437
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2021
ms.locfileid: "53300380"
---
# <a name="learn-about-sensitive-information-types"></a><span data-ttu-id="c7dcb-102">En savoir plus sur les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c7dcb-102">Learn about sensitive information types</span></span>

<span data-ttu-id="c7dcb-103">L’identification et la classification des éléments sensibles qui sont sous le contrôle de votre organisation est la première étape de la [protection des informations.](./information-protection.md)</span><span class="sxs-lookup"><span data-stu-id="c7dcb-103">Identifying and classifying sensitive items that are under your organizations control is the first step in the [Information Protection discipline](./information-protection.md).</span></span>  <span data-ttu-id="c7dcb-104">Microsoft 365 propose trois façons d’identifier les éléments afin qu’ils soient classés :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-104">Microsoft 365 provides three ways of identifying items so that they can be classified:</span></span>

- <span data-ttu-id="c7dcb-105">manuellement par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c7dcb-105">manually by users</span></span>
- <span data-ttu-id="c7dcb-106">reconnaissance automatique des modèles, comme les types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c7dcb-106">automated pattern recognition, like sensitive information types</span></span>
- [<span data-ttu-id="c7dcb-107">apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="c7dcb-107">machine learning</span></span>](classifier-learn-about.md)

<span data-ttu-id="c7dcb-108">Les types d’informations sensibles sont des classifieurs basés sur des modèles.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-108">Sensitive information types are pattern-based classifiers.</span></span> <span data-ttu-id="c7dcb-109">Ils détectent les informations sensibles telles que la sécurité sociale, la carte bancaire ou les numéros de compte bancaire pour identifier les éléments [sensibles. Voir Définitions d’entités des types d’informations sensibles](sensitive-information-type-entity-definitions.md)</span><span class="sxs-lookup"><span data-stu-id="c7dcb-109">They detect sensitive information like social security, credit card, or bank account numbers to identify sensitive items, see [Sensitive information types entity definitions](sensitive-information-type-entity-definitions.md)</span></span>

## <a name="sensitive-information-types-are-used-in"></a><span data-ttu-id="c7dcb-110">Les types d’informations sensibles sont utilisés dans</span><span class="sxs-lookup"><span data-stu-id="c7dcb-110">Sensitive information types are used in</span></span>

- [<span data-ttu-id="c7dcb-111">Stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="c7dcb-111">Data loss prevention policies</span></span>](dlp-learn-about-dlp.md) 
- [<span data-ttu-id="c7dcb-112">Étiquettes de confidentialité</span><span class="sxs-lookup"><span data-stu-id="c7dcb-112">Sensitivity labels</span></span>](sensitivity-labels.md)
- [<span data-ttu-id="c7dcb-113">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="c7dcb-113">Retention labels</span></span>](retention.md)
- [<span data-ttu-id="c7dcb-114">Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="c7dcb-114">Insider risk management</span></span>](insider-risk-management.md)
- [<span data-ttu-id="c7dcb-115">Conformité des communications</span><span class="sxs-lookup"><span data-stu-id="c7dcb-115">Communication compliance</span></span>](communication-compliance.md)
- [<span data-ttu-id="c7dcb-116">Stratégies de étiquetage automatique</span><span class="sxs-lookup"><span data-stu-id="c7dcb-116">Auto-labelling policies</span></span>](apply-sensitivity-label-automatically.md#how-to-configure-auto-labeling-for-office-apps)

## <a name="fundamental-parts-of-a-sensitive-information-type"></a><span data-ttu-id="c7dcb-117">Parties fondamentales d’un type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c7dcb-117">Fundamental parts of a sensitive information type</span></span>

<span data-ttu-id="c7dcb-118">Chaque entité de type d’informations sensibles est définie par les champs ci-après :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-118">Every sensitive information type entity is defined by these fields:</span></span>

- <span data-ttu-id="c7dcb-119">name: how the sensitive information type is referred to</span><span class="sxs-lookup"><span data-stu-id="c7dcb-119">name: how the sensitive information type is referred to</span></span>
- <span data-ttu-id="c7dcb-120">description : décrit ce que le type d’informations sensibles recherche</span><span class="sxs-lookup"><span data-stu-id="c7dcb-120">description: describes what the sensitive information type is looking for</span></span>
- <span data-ttu-id="c7dcb-121">modèle : un modèle définit ce qu’un type d’informations sensibles détecte.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-121">pattern: A pattern defines what a sensitive information type detects.</span></span> <span data-ttu-id="c7dcb-122">Il se compose des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-122">It consists of the following components</span></span>
    - <span data-ttu-id="c7dcb-123">Élément principal : élément principal que le type d’informations sensibles recherche.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-123">Primary element – the main element that the sensitive information type is looking for.</span></span> <span data-ttu-id="c7dcb-124">Il peut s’agit **d’une expression** régulière avec ou sans validation de la liste de contrôle, d’une liste de mots **clés,** d’un dictionnaire de mots clés **ou** d’une **fonction.**</span><span class="sxs-lookup"><span data-stu-id="c7dcb-124">It can be a **regular expression** with or without a checksum validation, a **keyword list**, a **keyword dictionary**, or a **function**.</span></span>
    - <span data-ttu-id="c7dcb-125">Élément de prise en charge : éléments qui agissent en tant que preuves justificatives qui contribuent à augmenter la confiance de la correspondance.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-125">Supporting element – elements that act as supporting evidence that help in increasing the confidence of the match.</span></span> <span data-ttu-id="c7dcb-126">Par exemple, le mot clé « SSN » à proximité d’un numéro SSN.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-126">For example, keyword “SSN” in proximity of an SSN number.</span></span> <span data-ttu-id="c7dcb-127">Il peut s’agit d’une expression régulière avec ou sans validation de la liste de contrôle, d’une liste de mots clés, d’un dictionnaire de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-127">It can be a regular expression with or without a checksum validation, keyword list, keyword dictionary.</span></span>
    - <span data-ttu-id="c7dcb-128">Niveau de confiance : les niveaux de confiance (élevé, moyen, faible) reflètent la quantité de preuves justificatives détectées avec l’élément principal.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-128">Confidence Level - Confidence levels (high, medium, low) reflect how much supporting evidence was detected along with the primary element.</span></span> <span data-ttu-id="c7dcb-129">Plus la preuve justificative qu’un élément contient est importante, plus la confiance qu’un élément correspond contient les informations sensibles que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-129">The more supporting evidence an item contains, the higher the confidence that a matched item contains the sensitive info you're looking for.</span></span>
    - <span data-ttu-id="c7dcb-130">Proximité : nombre de caractères entre l’élément principal et l’élément de prise en charge</span><span class="sxs-lookup"><span data-stu-id="c7dcb-130">Proximity – Number of characters between primary and supporting element</span></span>

![Diagramme de la fenêtre de proximité et de preuves probantes](../media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

<span data-ttu-id="c7dcb-132">En savoir plus sur les niveaux de confiance dans cette vidéo</span><span class="sxs-lookup"><span data-stu-id="c7dcb-132">Learn more about confidence levels in this video</span></span>


 > [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Hx60]  

### <a name="example-sensitive-information-type"></a><span data-ttu-id="c7dcb-133">Exemple de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c7dcb-133">Example sensitive information type</span></span>


## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="c7dcb-134">Numéro d’identité nationale (DNI) argentine</span><span class="sxs-lookup"><span data-stu-id="c7dcb-134">Argentina national identity (DNI) number</span></span>

### <a name="format"></a><span data-ttu-id="c7dcb-135">Format</span><span class="sxs-lookup"><span data-stu-id="c7dcb-135">Format</span></span>

<span data-ttu-id="c7dcb-136">Huit chiffres séparés par des points</span><span class="sxs-lookup"><span data-stu-id="c7dcb-136">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="c7dcb-137">Modèle</span><span class="sxs-lookup"><span data-stu-id="c7dcb-137">Pattern</span></span>

<span data-ttu-id="c7dcb-138">Huit chiffres :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-138">Eight digits:</span></span>
- <span data-ttu-id="c7dcb-139">deux chiffres</span><span class="sxs-lookup"><span data-stu-id="c7dcb-139">two digits</span></span>
- <span data-ttu-id="c7dcb-140">un point</span><span class="sxs-lookup"><span data-stu-id="c7dcb-140">a period</span></span>
- <span data-ttu-id="c7dcb-141">trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c7dcb-141">three digits</span></span>
- <span data-ttu-id="c7dcb-142">un point</span><span class="sxs-lookup"><span data-stu-id="c7dcb-142">a period</span></span>
- <span data-ttu-id="c7dcb-143">trois chiffres</span><span class="sxs-lookup"><span data-stu-id="c7dcb-143">three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="c7dcb-144">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c7dcb-144">Checksum</span></span>

<span data-ttu-id="c7dcb-145">Non</span><span class="sxs-lookup"><span data-stu-id="c7dcb-145">No</span></span>

### <a name="definition"></a><span data-ttu-id="c7dcb-146">Définition</span><span class="sxs-lookup"><span data-stu-id="c7dcb-146">Definition</span></span>

<span data-ttu-id="c7dcb-147">Une stratégie DLP a un niveau de confiance moyen qu’elle a détecté ce type d’informations sensibles si, dans une proximité de 300 caractères :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-147">A DLP policy has medium confidence that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="c7dcb-148">L’expression régulière Regex_argentina_national_id trouve un contenu qui correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-148">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="c7dcb-149">Un mot clé figurant dans la liste Keyword_argentina_national_id est trouvé.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-149">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="c7dcb-150">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c7dcb-150">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="c7dcb-151">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="c7dcb-151">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="c7dcb-152">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="c7dcb-152">Argentina National Identity number</span></span> 
- <span data-ttu-id="c7dcb-153">Identité</span><span class="sxs-lookup"><span data-stu-id="c7dcb-153">Identity</span></span> 
- <span data-ttu-id="c7dcb-154">Carte d’identité nationale d’identification</span><span class="sxs-lookup"><span data-stu-id="c7dcb-154">Identification National Identity Card</span></span> 
- <span data-ttu-id="c7dcb-155">DNI</span><span class="sxs-lookup"><span data-stu-id="c7dcb-155">DNI</span></span> 
- <span data-ttu-id="c7dcb-156">Registre national des personnes de la NIC</span><span class="sxs-lookup"><span data-stu-id="c7dcb-156">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="c7dcb-157">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="c7dcb-157">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="c7dcb-158">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="c7dcb-158">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="c7dcb-159">Identidad</span><span class="sxs-lookup"><span data-stu-id="c7dcb-159">Identidad</span></span> 
- <span data-ttu-id="c7dcb-160">Identificación</span><span class="sxs-lookup"><span data-stu-id="c7dcb-160">Identificación</span></span> 

### <a name="more-on-confidence-levels"></a><span data-ttu-id="c7dcb-161">Plus d’informations sur les niveaux de confiance</span><span class="sxs-lookup"><span data-stu-id="c7dcb-161">More on confidence levels</span></span>

<span data-ttu-id="c7dcb-162">Dans une définition d’entité  de type d’informations sensibles, le niveau de confiance reflète la quantité de preuves justificatives détectées en plus de l’élément principal.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-162">In a sensitive information type entity definition, **confidence level** reflects how much supporting evidence is detected in addition to the primary element.</span></span> <span data-ttu-id="c7dcb-163">Plus la preuve justificative qu’un élément contient est importante, plus la confiance qu’un élément correspond contient les informations sensibles que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-163">The more supporting evidence an item contains, the higher the confidence that a matched item contains the sensitive info you're looking for.</span></span> <span data-ttu-id="c7dcb-164">Par exemple, les correspondances avec un niveau de confiance élevé contiennent davantage de preuves justificatives à proximité immédiate de l’élément principal, tandis que les correspondances avec un niveau de confiance faible contiennent peu ou pas de preuves à proximité.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-164">For example, matches with a high confidence level will contain more supporting evidence in close proximity of the primary element, whereas matches with a low confidence level would contain little to no supporting evidence in close proximity.</span></span> 

<span data-ttu-id="c7dcb-165">Un niveau de confiance élevé renvoie le moins de faux positifs, mais peut entraîner davantage de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-165">A high confidence level returns the fewest false positives but might result in more false negatives.</span></span> <span data-ttu-id="c7dcb-166">Les niveaux de confiance faibles ou moyens renvoient plus de faux positifs, mais peu à zéro faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-166">Low or medium confidence levels returns more false positives but few to zero false negatives.</span></span>

- <span data-ttu-id="c7dcb-167">**faible niveau de** confiance : valeur 65, les éléments qui correspondent contiennent le moins de faux négatifs, mais le plus de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-167">**low confidence**: Value of 65, matched items will contain the fewest false negatives but the most false positives.</span></span> <span data-ttu-id="c7dcb-168">Une confiance faible renvoie toutes les correspondances de confiance faible, moyenne et élevée.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-168">Low confidence returns all low, medium, and high confidence matches.</span></span>
- <span data-ttu-id="c7dcb-169">**confiance moyenne**: valeur de 75, les éléments qui correspondent contiennent une quantité moyenne de faux positifs et de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-169">**medium confidence**: Value of 75, matched items will contain an average amount of false positives and false negatives.</span></span> <span data-ttu-id="c7dcb-170">Une confiance moyenne renvoie toutes les correspondances de confiance moyenne et élevée.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-170">Medium confidence returns all medium, and high confidence matches.</span></span>  
- <span data-ttu-id="c7dcb-171">**niveau de confiance** élevé : valeur 85, les éléments qui correspondent contiennent le moins de faux positifs, mais le plus de faux négatifs.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-171">**high confidence**: Value of 85, matched items will contain the fewest false positives but the most false negatives.</span></span> <span data-ttu-id="c7dcb-172">Un niveau de confiance élevé renvoie uniquement des correspondances à haut niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-172">High confidence only returns high confidence matches.</span></span>  

<span data-ttu-id="c7dcb-173">Vous devez utiliser des modèles de niveau de confiance élevé avec un nombre faible, par ex. 5 à 10, et des modèles de confiance faible avec des nombres plus élevés, par ex. 20 ou plus.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-173">You should use high confidence level patterns with low counts, say five to ten, and low confidence patterns with higher counts, say 20 or more.</span></span>

> [!NOTE]
> <span data-ttu-id="c7dcb-174">Si vous avez des stratégies existantes ou des types d’informations sensibles personnalisés (SIT) définis à l’aide de niveaux de confiance basés sur le nombre (également défini comme précision), ils seront automatiquement mappés aux trois niveaux de confiance discrets ; confiance faible, confiance moyenne et confiance élevée, dans l’interface utilisateur du Centre de sécurité @ conformité.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-174">If you have existing policies or custom sensitive information types (SITs) defined using number-based confidence levels (also know as accuracy), they will automatically be mapped to the three discrete confidence levels; low confidence, medium confidence, and high confidence, across the Security @ Compliance Center UI.</span></span>
> - <span data-ttu-id="c7dcb-175">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance entre 76 et 100 seront mappées à un niveau de confiance élevé.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-175">All policies with minimum accuracy or custom SIT patterns with confidence levels of between 76 and 100 will be mapped to high confidence.</span></span> 
> - <span data-ttu-id="c7dcb-176">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance entre 66 et 75 seront mappées à un niveau de confiance moyen.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-176">All policies with minimum accuracy or custom SIT patterns with confidence levels of between 66 and 75 will be mapped to medium confidence.</span></span>
> - <span data-ttu-id="c7dcb-177">Toutes les stratégies avec une précision minimale ou des modèles SIT personnalisés avec des niveaux de confiance inférieurs ou égaux à 65 seront mappées à un niveau de confiance faible.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-177">All policies with minimum accuracy or custom SIT patterns with confidence levels less than or equal to 65 will be mapped to low confidence.</span></span> 

## <a name="creating-custom-sensitive-information-types"></a><span data-ttu-id="c7dcb-178">Création de types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="c7dcb-178">Creating custom sensitive information types</span></span>

<span data-ttu-id="c7dcb-179">Pour créer des types d’informations sensibles personnalisés dans le Centre de sécurité et conformité, vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-179">To create custom sensitive information types in the Security & Compliance Center, you can choose from several options:</span></span>

- <span data-ttu-id="c7dcb-180">**Utiliser l’interface utilisateur** Vous pouvez configurer un type d’informations sensibles personnalisé à l’aide de l’interface utilisateur du Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-180">**Use the UI** You can set up a custom sensitive information type using the Security & Compliance Center UI.</span></span> <span data-ttu-id="c7dcb-181">Cette méthode vous permet d’utiliser des expressions régulières, des mots clés et des dictionnaires de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-181">With this method, you can use regular expressions, keywords, and keyword dictionaries.</span></span> <span data-ttu-id="c7dcb-182">Pour en savoir plus, voir [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-182">To learn more, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

- <span data-ttu-id="c7dcb-183">**Utiliser EDM** Vous pouvez configurer des types d’informations sensibles personnalisés à l’aide d’une classification de correspondance exacte des données (EDM).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-183">**Use EDM** You can set up custom sensitive information types using Exact Data Match (EDM)-based classification.</span></span> <span data-ttu-id="c7dcb-184">Cette méthode vous permet de créer un type d’informations sensibles dynamique à l’aide d’une base de données sécurisée que vous pouvez actualiser régulièrement.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-184">This method enables you to create a dynamic sensitive information type using a secure database that you can refresh periodically.</span></span> <span data-ttu-id="c7dcb-185">Voir l’article sur la [création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-185">See [Create a custom sensitive information type with Exact Data Match based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

- <span data-ttu-id="c7dcb-186">**Utiliser PowerShell** vous pouvez configurer des types d’informations sensibles personnalisés à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-186">**Use PowerShell** You can set up custom sensitive information types using PowerShell.</span></span> <span data-ttu-id="c7dcb-187">Bien que cette méthode soit plus complexe que celle de l’interface utilisateur, elle offre davantage d’options de configuration.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-187">Although this method is more complex than using the UI, you have more configuration options.</span></span> <span data-ttu-id="c7dcb-188">Voir [Créer un type d’informations sensibles personnalisé dans l’interface PowerShell du Centre de sécurité et conformité](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-188">See [Create a custom sensitive information type in Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>



> [!NOTE]
> <span data-ttu-id="c7dcb-189">Des niveaux de confiance améliorés sont disponibles pour une utilisation immédiate dans la protection contre la perte de données pour les services Microsoft 365, les Protection des données Microsoft pour les services Microsoft 365, la conformité des communications, la gouvernance des informations et la gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-189">Improved confidence levels are available for immediate use within Data Loss Prevention for Microsoft 365 services, Microsoft Information Protection for Microsoft 365 services, Communication Compliance, Information Governance, and Records Management.</span></span>
> <span data-ttu-id="c7dcb-190">Microsoft 365 La Protection des informations prend désormais en charge les langues de jeu de caractères à doubles caractères pour :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-190">Microsoft 365 Information Protection now  supports double byte character set languages for:</span></span>
> - <span data-ttu-id="c7dcb-191">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="c7dcb-191">Chinese (simplified)</span></span>
> - <span data-ttu-id="c7dcb-192">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="c7dcb-192">Chinese (traditional)</span></span>
> - <span data-ttu-id="c7dcb-193">Korean</span><span class="sxs-lookup"><span data-stu-id="c7dcb-193">Korean</span></span>
> - <span data-ttu-id="c7dcb-194">Japanese</span><span class="sxs-lookup"><span data-stu-id="c7dcb-194">Japanese</span></span>
> 
> <span data-ttu-id="c7dcb-195">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-195">This support is available for sensitive information types.</span></span> <span data-ttu-id="c7dcb-196">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-196">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

> [!TIP]
> <span data-ttu-id="c7dcb-197">Pour détecter les modèles contenant des caractères chinois/japonais et des caractères d’octet unique ou pour détecter les modèles contenant du chinois/le japonais et l’anglais, définissez deux variantes du mot clé ou de regex.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-197">To detect patterns containing Chinese/Japanese characters and single byte characters or to detect patterns containing Chinese/Japanese and English, define two variants of the keyword or regex.</span></span>
> 
> <span data-ttu-id="c7dcb-198">Par exemple, pour détecter un mot clé tel que « 机密的document », utilisez deux variantes du mot clé ; l’un avec un espace entre le texte japonais et anglais et l’autre sans espace entre le texte japonais et l’anglais.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-198">For example, to detect a keyword like "机密的document", use two variants of the keyword; one with a space between the Japanese and English text and another without a space between the Japanese and English text.</span></span> <span data-ttu-id="c7dcb-199">Par conséquent, les mots clés à ajouter dans le SIT doivent être « 机密的 document » et « 机密的document ».</span><span class="sxs-lookup"><span data-stu-id="c7dcb-199">So, the keywords to be added in the SIT should be "机密的 document" and "机密的document".</span></span> <span data-ttu-id="c7dcb-200">De la même façon, pour détecter une expression « 東京オリンピック2020 », deux variantes doivent être utilisées : « 東京オリンピック 2020 » et « 東京オリンピック2020 ».</span><span class="sxs-lookup"><span data-stu-id="c7dcb-200">Similarly, to detect a phrase "東京オリンピック2020", two variants should be used; "東京オリンピック 2020" and "東京オリンピック2020".</span></span>
> 
> <span data-ttu-id="c7dcb-201">Lorsque vous créez une regex en utilisant un trait d'union à double octet ou un point à double octet, assurez-vous d'échapper les deux caractères comme on le ferait pour un trait d'union ou un point dans une regex.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-201">While creating a regex using a double byte hyphen or a double byte period, make sure to escape both the characters like one would escape a hyphen or period in a regex.</span></span> <span data-ttu-id="c7dcb-202">Voici un exemple de regex pour référence :</span><span class="sxs-lookup"><span data-stu-id="c7dcb-202">Here is a sample regex for reference:</span></span>
>    - <span data-ttu-id="c7dcb-203">(?<!\d)([４][０-９]{3}[\-?\－\t]\*[０-９]{4}</span><span class="sxs-lookup"><span data-stu-id="c7dcb-203">(?<!\d)([４][０-９]{3}[\-?\－\t]\*[０-９]{4}</span></span>
>
> <span data-ttu-id="c7dcb-204">Nous vous recommandons d’utiliser une correspondance de chaîne au lieu d’une correspondance de mot dans une liste de mots clés.</span><span class="sxs-lookup"><span data-stu-id="c7dcb-204">We recommend using string match instead of word match in a keyword list.</span></span>

## <a name="for-further-information"></a><span data-ttu-id="c7dcb-205">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="c7dcb-205">For further information</span></span>
- [<span data-ttu-id="c7dcb-206">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="c7dcb-206">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="c7dcb-207">Créer un type d’informations sensibles personnalisé</span><span class="sxs-lookup"><span data-stu-id="c7dcb-207">Create a custom sensitive information type</span></span>](create-a-custom-sensitive-information-type.md)
- [<span data-ttu-id="c7dcb-208">Créer un type d’informations sensibles personnalisé dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="c7dcb-208">Create a custom sensitive information type in PowerShell</span></span>](create-a-custom-sensitive-information-type-in-scc-powershell.md)

<span data-ttu-id="c7dcb-209">Pour découvrir comment utiliser des types d’informations sensibles pour se conformer aux réglementations en matière de confidentialité des données, voir [Deploy information protection for data privacy regulations with Microsoft 365](../solutions/information-protection-deploy.md) (aka.ms/m365dataprivacy).</span><span class="sxs-lookup"><span data-stu-id="c7dcb-209">To learn how to use sensitive information types to comply with data privacy regulations, see [Deploy information protection for data privacy regulations with Microsoft 365](../solutions/information-protection-deploy.md)  (aka.ms/m365dataprivacy).</span></span>

<!-- fwlink for this topic https://go.microsoft.com/fwlink/?linkid=2135644-->
