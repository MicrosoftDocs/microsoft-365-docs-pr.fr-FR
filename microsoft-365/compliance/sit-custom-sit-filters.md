---
title: Référence des filtres de types d’informations sensibles personnalisés
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Cet article présente une liste des filtres qui peuvent être codés dans des types d’informations sensibles personnalisés.
ms.openlocfilehash: 6dfa562d581f14c0b1ac41c4ce803e2367a94636
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322703"
---
# <a name="custom-sensitive-information-type-filters-reference"></a><span data-ttu-id="1cbd0-103">Référence des filtres de types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="1cbd0-103">Custom sensitive information type filters reference</span></span>

<span data-ttu-id="1cbd0-104">Dans Microsoft, vous pouvez définir des filtres ou des vérifications supplémentaires lors de la création d’un type d’informations sensibles personnalisé (SIT).</span><span class="sxs-lookup"><span data-stu-id="1cbd0-104">In Microsoft you can define filters or additional checks while creating a custom sensitive information types (SIT).</span></span>

## <a name="list-of-supported-filters-and-use-cases"></a><span data-ttu-id="1cbd0-105">Liste des filtres et cas d’utilisation pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cbd0-105">List of supported filters and use cases</span></span>

### <a name="alldigitssame-exclude"></a><span data-ttu-id="1cbd0-106">AllDigitsSame Exclude</span><span class="sxs-lookup"><span data-stu-id="1cbd0-106">AllDigitsSame Exclude</span></span>

<span data-ttu-id="1cbd0-107">Description : vous permet d’exclure les correspondances qui ont tous les chiffres comme chiffres en double, comme 111111111 ou 111-111-111</span><span class="sxs-lookup"><span data-stu-id="1cbd0-107">Description: Allows you to exclude matches which have all digits as duplicate digits, like 111111111 or 111-111-111</span></span>

<span data-ttu-id="1cbd0-108">Définition des filtres</span><span class="sxs-lookup"><span data-stu-id="1cbd0-108">Defining filters</span></span>
```xml
<Filters id="ssn_filters">
    <Filter type="AllDigitsSameFilter"></Filter>
</Filters>
```

<span data-ttu-id="1cbd0-109">L’utiliser dans le package de règles au niveau de l’entité</span><span class="sxs-lookup"><span data-stu-id="1cbd0-109">Using it in rule package at the entity level</span></span>
```xml
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85"  filters="ssn_filters">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
      </Pattern>
</Entity>
```

<span data-ttu-id="1cbd0-110">L’utiliser dans le package de règles au niveau du modèle</span><span class="sxs-lookup"><span data-stu-id="1cbd0-110">Using it in rule package at the pattern level</span></span>
```xml
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85"  filters="ssn_filters">
        <IdMatch idRef="Func_ssn" />
      </Pattern>
</Entity>
```

### <a name="textmatchfilter-startswith"></a><span data-ttu-id="1cbd0-111">TextMatchFilter StartsWith</span><span class="sxs-lookup"><span data-stu-id="1cbd0-111">TextMatchFilter StartsWith</span></span> 

<span data-ttu-id="1cbd0-112">Description : vous permet de définir les caractères de départ de l’entité.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-112">Description: Allows you to define the starting characters for the entity.</span></span> <span data-ttu-id="1cbd0-113">Il a deux variantes , inclure et exclure.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-113">It has two variants, include and exclude.</span></span>

<span data-ttu-id="1cbd0-114">Par exemple, pour exclure les numéros commençant par 0500, 91, 091, 010 dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-114">For example to exclude the numbers starting with 0500, 91, 091, 010 in a list like this:</span></span>

- <span data-ttu-id="1cbd0-115">0500-4500-027</span><span class="sxs-lookup"><span data-stu-id="1cbd0-115">0500-4500-027</span></span>
- <span data-ttu-id="1cbd0-116">91564721450</span><span class="sxs-lookup"><span data-stu-id="1cbd0-116">91564721450</span></span>
- <span data-ttu-id="1cbd0-117">91-8523697410</span><span class="sxs-lookup"><span data-stu-id="1cbd0-117">91-8523697410</span></span>
- <span data-ttu-id="1cbd0-118">700-8956-7844</span><span class="sxs-lookup"><span data-stu-id="1cbd0-118">700-8956-7844</span></span>
- <span data-ttu-id="1cbd0-119">1000-3265-9874</span><span class="sxs-lookup"><span data-stu-id="1cbd0-119">1000-3265-9874</span></span>
- <span data-ttu-id="1cbd0-120">0100-7892-3012</span><span class="sxs-lookup"><span data-stu-id="1cbd0-120">0100-7892-3012</span></span>

<span data-ttu-id="1cbd0-121">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-121">you can use this xml</span></span>

```xml
<Filters id="phone_number_filters_exc">
    <Filter type="TextMatchFilter" direction="StartsWith" logic="Exclude" textProcessorId="Keyword_false_positives_sw">
</Filter>
</Filters>

  <Keyword id="Keyword_false_positives_sw">
    <Group matchStyle="string">
      <Term>0500</Term>
      <Term>91</Term>
      <Term>091</Term>
      <Term>0100</Term>
    </Group>
  </Keyword>
```
<span data-ttu-id="1cbd0-122">Par exemple, pour inclure les numéros commençant par 0500, 91, 091, 0100 dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-122">For example, to include the numbers starting with 0500, 91, 091, 0100 in a list like this:</span></span> 

- <span data-ttu-id="1cbd0-123">0500-4500-027</span><span class="sxs-lookup"><span data-stu-id="1cbd0-123">0500-4500-027</span></span>
- <span data-ttu-id="1cbd0-124">91564721450</span><span class="sxs-lookup"><span data-stu-id="1cbd0-124">91564721450</span></span>
- <span data-ttu-id="1cbd0-125">91-8523697410</span><span class="sxs-lookup"><span data-stu-id="1cbd0-125">91-8523697410</span></span>
- <span data-ttu-id="1cbd0-126">700-8956-7844</span><span class="sxs-lookup"><span data-stu-id="1cbd0-126">700-8956-7844</span></span>
- <span data-ttu-id="1cbd0-127">1000-3265-9874</span><span class="sxs-lookup"><span data-stu-id="1cbd0-127">1000-3265-9874</span></span>
- <span data-ttu-id="1cbd0-128">0100-7892-3012</span><span class="sxs-lookup"><span data-stu-id="1cbd0-128">0100-7892-3012</span></span>

<span data-ttu-id="1cbd0-129">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-129">you can use this xml</span></span>

```xml
<Filters id="phone_filters_inc">
    <Filter type="TextMatchFilter" direction="StartsWith" logic="Include" textProcessorId="Keyword_false_positives_sw">
</Filter>
```

### <a name="textmatchfilter-endswith"></a><span data-ttu-id="1cbd0-130">TextMatchFilter EndsWith</span><span class="sxs-lookup"><span data-stu-id="1cbd0-130">TextMatchFilter EndsWith</span></span> 

<span data-ttu-id="1cbd0-131">Description : vous permet de définir les caractères de fin de l’entité.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-131">Description: Allows you to define the ending characters for the entity.</span></span> 

<span data-ttu-id="1cbd0-132">Par exemple, pour exclure les numéros se terminant par 0500 91 091 0100 dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-132">For example, to exclude the numbers ending with 0500,91,091, 0100 in a list like this:</span></span>

- <span data-ttu-id="1cbd0-133">1234567891</span><span class="sxs-lookup"><span data-stu-id="1cbd0-133">1234567891</span></span>
- <span data-ttu-id="1cbd0-134">1234-5678-0091</span><span class="sxs-lookup"><span data-stu-id="1cbd0-134">1234-5678-0091</span></span>
- <span data-ttu-id="1cbd0-135">1234.4567.7091</span><span class="sxs-lookup"><span data-stu-id="1cbd0-135">1234.4567.7091</span></span>
- <span data-ttu-id="1cbd0-136">1234-8091-4564</span><span class="sxs-lookup"><span data-stu-id="1cbd0-136">1234-8091-4564</span></span>

<span data-ttu-id="1cbd0-137">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-137">you can use this xml</span></span>

```xml
<Filters id="phone_number_filters_exc">
    <Filter type="TextMatchFilter" direction="EndsWith" logic="Exclude" textProcessorId="Keyword_false_positives_sw">
</Filter>

  <Keyword id="Keyword_false_positives_sw">
    <Group matchStyle="string">
      <Term>0500</Term>
      <Term>91</Term>
      <Term>091</Term>
      <Term>0100</Term>
    </Group>
  </Keyword>
```

<span data-ttu-id="1cbd0-138">Par exemple, pour inclure les numéros se terminant par 0500, 91, 091, 0100, dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-138">For example, to include the numbers ending with 0500, 91, 091, 0100, in a list like this:</span></span>

- <span data-ttu-id="1cbd0-139">1234567891</span><span class="sxs-lookup"><span data-stu-id="1cbd0-139">1234567891</span></span>
- <span data-ttu-id="1cbd0-140">1234-5678-0091</span><span class="sxs-lookup"><span data-stu-id="1cbd0-140">1234-5678-0091</span></span>
- <span data-ttu-id="1cbd0-141">1234.4567.7091</span><span class="sxs-lookup"><span data-stu-id="1cbd0-141">1234.4567.7091</span></span>
- <span data-ttu-id="1cbd0-142">1234-8091-4564</span><span class="sxs-lookup"><span data-stu-id="1cbd0-142">1234-8091-4564</span></span>

<span data-ttu-id="1cbd0-143">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-143">you can use this xml</span></span>

```xml
<Filters id="phone_filters_inc">
    <Filter type="TextMatchFilter" direction=" EndsWith" logic="Include" textProcessorId="Keyword_false_positives_sw">
</Filter>
```

### <a name="textmatchfilter-full"></a><span data-ttu-id="1cbd0-144">TextMatchFilter Full</span><span class="sxs-lookup"><span data-stu-id="1cbd0-144">TextMatchFilter Full</span></span>

<span data-ttu-id="1cbd0-145">Description : vous permet d’interdire certaines correspondances pour les empêcher de déclencher la règle.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-145">Description: Allows you to prohibit certain matches to prevent them from triggering the rule.</span></span> <span data-ttu-id="1cbd0-146">Par exemple, excluez 411111111111111 de la liste des correspondances de carte de crédit valides.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-146">For example, exclude 4111111111111111 from the list of valid credit card matches.</span></span>

<span data-ttu-id="1cbd0-147">Par exemple, pour exclure des numéros de carte de crédit tels que 4111111111111 et 3241891031113111, dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-147">For example, to exclude credit card numbers like 4111111111111111 and 3241891031113111 in a list like this:</span></span>

- <span data-ttu-id="1cbd0-148">4485 3647 3952 7352</span><span class="sxs-lookup"><span data-stu-id="1cbd0-148">4485 3647 3952 7352</span></span>
- <span data-ttu-id="1cbd0-149">4111111111111111</span><span class="sxs-lookup"><span data-stu-id="1cbd0-149">4111111111111111</span></span>
- <span data-ttu-id="1cbd0-150">3241891031113111</span><span class="sxs-lookup"><span data-stu-id="1cbd0-150">3241891031113111</span></span>

<span data-ttu-id="1cbd0-151">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-151">you can use this xml</span></span>

```xml
<Filters id="cc_number_filters_exc">
    <Filter type="TextMatchFilter" direction="Full" logic="Exclude" textProcessorId="Keyword_false_positives_full">
</Filter>

  <Keyword id="Keyword_false_positives_full">
    <Group matchStyle="string">
      <Term>4111111111111111</Term>
      <Term>3241891031113111</Term>
    </Group>
  </Keyword>
```

<span data-ttu-id="1cbd0-152">Par exemple, pour inclure des numéros de carte de crédit comme 41111111111111 et 3241891031113111 dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-152">For example, to include credit card numbers like 4111111111111111 and 3241891031113111 in a list like this:</span></span>

- <span data-ttu-id="1cbd0-153">4485 3647 3952 7352</span><span class="sxs-lookup"><span data-stu-id="1cbd0-153">4485 3647 3952 7352</span></span>
- <span data-ttu-id="1cbd0-154">4111111111111111</span><span class="sxs-lookup"><span data-stu-id="1cbd0-154">4111111111111111</span></span>
- <span data-ttu-id="1cbd0-155">3241891031113111</span><span class="sxs-lookup"><span data-stu-id="1cbd0-155">3241891031113111</span></span>

<span data-ttu-id="1cbd0-156">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-156">you can use this xml</span></span>

```xml
<Filters id="cc_filters_inc">
    <Filter type="TextMatchFilter" direction="Full" logic="Include" textProcessorId="Keyword_false_positives_full">
</Filter>
```

### <a name="textmatchfilter-prefix"></a><span data-ttu-id="1cbd0-157">Préfixe TextMatchFilter</span><span class="sxs-lookup"><span data-stu-id="1cbd0-157">TextMatchFilter Prefix</span></span>

<span data-ttu-id="1cbd0-158">Description : vous permet de définir les caractères précédents qui doivent toujours être inclus ou exclus.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-158">Description: Allows you to define the preceding characters that should be always included or excluded.</span></span> <span data-ttu-id="1cbd0-159">Par exemple, si le numéro de carte de crédit est précédé de « ID de commande : » supprimez la correspondance des correspondances valides.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-159">For example, if Credit card number is preceded by ‘Order ID:’ then remove the match from the valid matches.</span></span>

<span data-ttu-id="1cbd0-160">Par exemple, pour exclure les occurrences de numéros  de téléphone qui ont Téléphone **numéro** et m’appeler à des chaînes avant le numéro de téléphone, dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-160">For example, to exclude occurrences of phone numbers which have **Phone number** and **call me at** strings before the phone number, in a list like this:</span></span>

- <span data-ttu-id="1cbd0-161">numéro de téléphone 091-8974-653278</span><span class="sxs-lookup"><span data-stu-id="1cbd0-161">phone number 091-8974-653278</span></span>
- <span data-ttu-id="1cbd0-162">Téléphone 45-124576532-123</span><span class="sxs-lookup"><span data-stu-id="1cbd0-162">Phone 45-124576532-123</span></span>
- <span data-ttu-id="1cbd0-163">45-124576532-123</span><span class="sxs-lookup"><span data-stu-id="1cbd0-163">45-124576532-123</span></span>

<span data-ttu-id="1cbd0-164">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-164">you can use this xml</span></span>

```xml
<Filters id="cc_number_filters_exc">
    <Filter type="TextMatchFilter" direction="Prefix" logic="Exclude" textProcessorId="Keyword_false_positives_prefix">
</Filter>
  <Keyword id="Keyword_false_positives_prefix">
    <Group matchStyle="string">
      <Term>phone number</Term>
      <Term>call me at</Term>
    </Group>
  </Keyword>
```

<span data-ttu-id="1cbd0-165">Par exemple, pour inclure  les occurrences qui ont des chaînes de carte de crédit et de carte **#** avant le numéro de carte de crédit, dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-165">For example, to include occurrences that have **credit card** and **card #** strings before the credit card number, in a list like this:</span></span>

- <span data-ttu-id="1cbd0-166">Carte de crédit 45-124576532-123</span><span class="sxs-lookup"><span data-stu-id="1cbd0-166">Credit card 45-124576532-123</span></span> 
- <span data-ttu-id="1cbd0-167">45-124576532-123 (qui peut être un numéro de téléphone)</span><span class="sxs-lookup"><span data-stu-id="1cbd0-167">45-124576532-123  (which could be phone number)</span></span>

<span data-ttu-id="1cbd0-168">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-168">you can use this xml</span></span>

```xml
<Filters id="cc_filters_inc">
    <Filter type="TextMatchFilter" direction="Full" logic="Include" textProcessorId="Keyword_true_positives_prefix">
</Filter>

  <Keyword id="Keyword_true_positives_prefix">
    <Group matchStyle="string">
      <Term>credit card</Term>
      <Term>card #</Term>
    </Group>
  </Keyword
```

### <a name="textmatchfilter-suffix"></a><span data-ttu-id="1cbd0-169">Suffixe TextMatchFilter</span><span class="sxs-lookup"><span data-stu-id="1cbd0-169">TextMatchFilter Suffix</span></span>

<span data-ttu-id="1cbd0-170">Description : vous permet de définir les caractères suivants qui doivent toujours être inclus ou exclus.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-170">Description: Allows you to define the following characters that should be always included or excluded.</span></span> <span data-ttu-id="1cbd0-171">Par exemple, si le numéro de carte de crédit est suivi de « /xuid », supprimez la correspondance des correspondances valides.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-171">For example, if Credit card number is followed by ‘/xuid’ then remove the match from the valid matches.</span></span>

<span data-ttu-id="1cbd0-172">Par exemple, les occurrences les plus exclues s’il y a 5 instances de quatre chiffres en plus comme suffixe dans une liste comme celle-ci :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-172">For example, top exclude occurrences if there are 5 more instances of four digits as suffix in a list like this:</span></span>

- <span data-ttu-id="1cbd0-173">1234-5678-9321 4500 9870 6321 48925566</span><span class="sxs-lookup"><span data-stu-id="1cbd0-173">1234-5678-9321 4500 9870 6321 48925566</span></span>
- <span data-ttu-id="1cbd0-174">1234-5678-9321</span><span class="sxs-lookup"><span data-stu-id="1cbd0-174">1234-5678-9321</span></span>

<span data-ttu-id="1cbd0-175">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-175">you can use this xml</span></span>

```xml
<Filters id="cc_number_filters_exc">
    <Filter type="TextMatchFilter" direction="Prefix" logic="Exclude" textProcessorId="Regex_false_positives_suffix">
</Filter>

  <Regexid="Regex_false_positives_suffix">(\d{4}){5,}</Regex>
```
<span data-ttu-id="1cbd0-176">Par exemple, pour exclure les occurrences si elles sont **suivies par /xuidsuffix,** comme une dans cette liste :</span><span class="sxs-lookup"><span data-stu-id="1cbd0-176">For example, to exclude occurrences if they are followed by **/xuidsuffix**, like one in this list:</span></span>

- <span data-ttu-id="1cbd0-177">1234-5678-9321 /xuid</span><span class="sxs-lookup"><span data-stu-id="1cbd0-177">1234-5678-9321 /xuid</span></span>
- <span data-ttu-id="1cbd0-178">1234-5678-9321</span><span class="sxs-lookup"><span data-stu-id="1cbd0-178">1234-5678-9321</span></span>

<span data-ttu-id="1cbd0-179">vous pouvez utiliser ce xml</span><span class="sxs-lookup"><span data-stu-id="1cbd0-179">you can use this xml</span></span>

<span data-ttu-id="1cbd0-180">''xml <Filters id="cc_number_filters_exc"></span><span class="sxs-lookup"><span data-stu-id="1cbd0-180">\`\`xml <Filters id="cc_number_filters_exc"></span></span>
    <Filter type="TextMatchFilter" direction="Prefix" logic="Exclude" textProcessorId="Keyword_false_positives_suffix">
</Filter>

  <span data-ttu-id="1cbd0-181"><Keyword id="Keyword_false_positives_suffix"> <Group matchStyle="string">
      </span><span class="sxs-lookup"><span data-stu-id="1cbd0-181"><Keyword id="Keyword_false_positives_suffix"> <Group matchStyle="string">
      </span></span><Term><span data-ttu-id="1cbd0-182">/xuid</span><span class="sxs-lookup"><span data-stu-id="1cbd0-182">/xuid</span></span></Term>
    <span data-ttu-id="1cbd0-183"></Group> </Keyword></span><span class="sxs-lookup"><span data-stu-id="1cbd0-183"></Group> </Keyword></span></span>
```

For example, to include an occurrence only if it is followed by **cvv** or **expires**, like two in this list:

- 45-124576532-123 
- 45-124576532-123  cvv 966
- 45-124576532-123  expires 03/23

you can use this xml

```xml
<Filters id="cc_filters_inc">
    <Filter type="TextMatchFilter" direction="Full" logic="Include" textProcessorId="Keyword_true_positives_suffix">
</Filter>

  <Keyword id="Keyword_true_positives_suffix">
    <Group matchStyle="string">
      <Term>cvv</Term>
      <Term>expires</Term>
    </Group>
  </Keyword>
```

## <a name="using-filters-in-rule-packages"></a><span data-ttu-id="1cbd0-184">Utilisation de filtres dans des packages de règles</span><span class="sxs-lookup"><span data-stu-id="1cbd0-184">Using filters in rule packages</span></span>

<span data-ttu-id="1cbd0-185">Les filtres peuvent être définis sur l’ensemble du sit ou sur un modèle.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-185">Filters can be defined on the entire SIT or on a pattern.</span></span> <span data-ttu-id="1cbd0-186">Voici quelques exemples d’extraits de code.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-186">Here are some code snippets examples.</span></span> 

### <a name="at-sensitive-information-type-level"></a><span data-ttu-id="1cbd0-187">Au niveau du type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="1cbd0-187">At sensitive information type level</span></span>

<span data-ttu-id="1cbd0-188">Filtres au niveau de l’entité : couvrira tous les modèles enfants</span><span class="sxs-lookup"><span data-stu-id="1cbd0-188">Filters at Entity - will cover all child patterns</span></span>

<span data-ttu-id="1cbd0-189">Les filtres seront appliqués sur **toutes les** instances classées par l’un des modèles de ce type d’entité/sensible</span><span class="sxs-lookup"><span data-stu-id="1cbd0-189">The filters will be applied on **all** the instances classified by any of the patterns in that entity / sensitive type</span></span>

```xml
<Entity id="6443b88f-2808-482a-8e1a-3ae5026645e1" patternsProximity="300" recommendedConfidence="85" filters="CompositeFiltersAtEntityLevel">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_denmark_id" />
      </Pattern>
</Entity>
```

### <a name="at-the-individual-pattern-of-the-sensitive-information-type-level"></a><span data-ttu-id="1cbd0-190">Au niveau du modèle individuel du niveau de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="1cbd0-190">At the individual pattern of the sensitive information type level</span></span>

<span data-ttu-id="1cbd0-191">Filtre uniquement au niveau du modèle.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-191">Filters only at the pattern level.</span></span>

<span data-ttu-id="1cbd0-192">Le filtre sera appliqué sur les instances qui correspondent au modèle.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-192">The filter will be applied on the instances matched by the pattern.</span></span>

```xml
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85"  filters="CompositeFiltersAtPattern">
        <IdMatch idRef="Keyword_cc_verification" />
      </Pattern>
</Entity>
```


### <a name="at-sensitive-information-type-level-and-an-additional-filter-on-some-of-the-patterns-of-that-entity"></a><span data-ttu-id="1cbd0-193">Au niveau du type d’informations sensibles et un filtre supplémentaire sur certains modèles de cette entité</span><span class="sxs-lookup"><span data-stu-id="1cbd0-193">At sensitive information type level and an additional filter on some of the patterns of that entity</span></span>

<span data-ttu-id="1cbd0-194">Filtres au niveau de l’entité + modèle</span><span class="sxs-lookup"><span data-stu-id="1cbd0-194">Filters at Entity + pattern</span></span>

<span data-ttu-id="1cbd0-195">Les filtres seront appliqués sur **toutes les** instances classées par l’un des modèles de cette entité/type sensible.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-195">The filters will be applied on **all** the instances classified by any of the patterns in that entity / sensitive type.</span></span> <span data-ttu-id="1cbd0-196">Le filtre de niveau modèle filtre les instances qui correspondent à ce modèle.</span><span class="sxs-lookup"><span data-stu-id="1cbd0-196">The pattern level filter will filter the instances matched by that pattern.</span></span>

```xml
<Entity id="6443b88f-2808-482a-8e1a-3ae5026645e1" patternsProximity="300" recommendedConfidence="85" filters="CompositeFiltersAtEntityLevel">
      <Pattern confidenceLevel="85" filters="CompositeFiltersAtPattern">
        <IdMatch idRef="Regex_denmark_id" />
      </Pattern>
</Entity>
``` 

 

## <a name="more-information"></a><span data-ttu-id="1cbd0-197">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1cbd0-197">More information</span></span>

- [<span data-ttu-id="1cbd0-198">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="1cbd0-198">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)

- [<span data-ttu-id="1cbd0-199">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="1cbd0-199">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

- [<span data-ttu-id="1cbd0-200">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="1cbd0-200">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
