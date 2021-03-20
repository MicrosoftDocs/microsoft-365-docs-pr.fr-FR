---
title: Référence de format SKOS pour la taxonomie SharePoint
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
description: Référence de format SKOS pour la taxonomie SharePoint
ms.openlocfilehash: 6a565de9598706e998206304093ed86a1a55704d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50911173"
---
# <a name="skos-format-reference-for-sharepoint-taxonomy"></a><span data-ttu-id="cd96c-103">Référence de format SKOS pour la taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="cd96c-103">SKOS format reference for SharePoint taxonomy</span></span>

<span data-ttu-id="cd96c-104">Cet article comprend le vocabulaire RDF utilisé pour représenter la [taxonomie SharePoint](/dotnet/api/microsoft.sharepoint.taxonomy) et est basé sur [SKOS](https://www.w3.org/TR/skos-primer/).</span><span class="sxs-lookup"><span data-stu-id="cd96c-104">This article includes RDF vocabulary used to represent [SharePoint taxonomy](/dotnet/api/microsoft.sharepoint.taxonomy) and is based on [SKOS](https://www.w3.org/TR/skos-primer/).</span></span> <span data-ttu-id="cd96c-105">Pour la sérialisation de cette syntaxe RDF, utilisez RDF [TURTLE](https://www.w3.org/TR/turtle/).</span><span class="sxs-lookup"><span data-stu-id="cd96c-105">For serialization of this RDF syntax, use RDF [TURTLE](https://www.w3.org/TR/turtle/).</span></span>

<span data-ttu-id="cd96c-106">Le tableau suivant affiche les équivalents [SKOS](https://www.w3.org/TR/skos-primer/) pour le vocabulaire de [taxonomie SharePoint](/dotnet/api/microsoft.sharepoint.taxonomy).</span><span class="sxs-lookup"><span data-stu-id="cd96c-106">The following table shows the [SKOS](https://www.w3.org/TR/skos-primer/) equivalents for the [SharePoint taxonomy](/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary.</span></span> <span data-ttu-id="cd96c-107">SharePoint ne prend pas en charge les valeurs [SKOS](https://www.w3.org/TR/skos-primer/) qui n’ont pas d’équivalent de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd96c-107">SharePoint does not support [SKOS](https://www.w3.org/TR/skos-primer/) values that have no SharePoint taxonomy equivalent.</span></span>

|<span data-ttu-id="cd96c-108">Taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="cd96c-108">SharePoint taxonomy</span></span>|<span data-ttu-id="cd96c-109">Équivalent SKOS</span><span class="sxs-lookup"><span data-stu-id="cd96c-109">SKOS equivalent</span></span>|
|:-----------------|:--------------|
|<span data-ttu-id="cd96c-110">sharepoint-taxonomy:Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-110">sharepoint-taxonomy:Term</span></span>|<span data-ttu-id="cd96c-111">skos:Concept</span><span class="sxs-lookup"><span data-stu-id="cd96c-111">skos:Concept</span></span>|
|<span data-ttu-id="cd96c-112">sharepoint-taxonomy:TermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-112">sharepoint-taxonomy:TermSet</span></span>|<span data-ttu-id="cd96c-113">skos:ConceptScheme</span><span class="sxs-lookup"><span data-stu-id="cd96c-113">skos:ConceptScheme</span></span>|
|<span data-ttu-id="cd96c-114">sharepoint-taxonomy:inTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-114">sharepoint-taxonomy:inTermSet</span></span>|<span data-ttu-id="cd96c-115">skos:inScheme</span><span class="sxs-lookup"><span data-stu-id="cd96c-115">skos:inScheme</span></span>|
|<span data-ttu-id="cd96c-116">sharepoint-taxonomy:hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-116">sharepoint-taxonomy:hasTopLevelTerm</span></span>|<span data-ttu-id="cd96c-117">skos:hasTopConcept</span><span class="sxs-lookup"><span data-stu-id="cd96c-117">skos:hasTopConcept</span></span>|
|<span data-ttu-id="cd96c-118">sharepoint-taxonomy:topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="cd96c-118">sharepoint-taxonomy:topLevelTermOf</span></span>|<span data-ttu-id="cd96c-119">skos:topConceptOf</span><span class="sxs-lookup"><span data-stu-id="cd96c-119">skos:topConceptOf</span></span>|
|<span data-ttu-id="cd96c-120">sharepoint-taxonomy:defaultLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-120">sharepoint-taxonomy:defaultLabel</span></span>|<span data-ttu-id="cd96c-121">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-121">skos:prefLabel</span></span>|
|<span data-ttu-id="cd96c-122">sharepoint-taxonomy:termSetName</span><span class="sxs-lookup"><span data-stu-id="cd96c-122">sharepoint-taxonomy:termSetName</span></span>|<span data-ttu-id="cd96c-123">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-123">skos:prefLabel</span></span>|
|<span data-ttu-id="cd96c-124">sharepoint-taxonomy:propertyName</span><span class="sxs-lookup"><span data-stu-id="cd96c-124">sharepoint-taxonomy:propertyName</span></span>|<span data-ttu-id="cd96c-125">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-125">skos:prefLabel</span></span>|
|<span data-ttu-id="cd96c-126">sharepoint-taxonomy:otherLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-126">sharepoint-taxonomy:otherLabel</span></span>|<span data-ttu-id="cd96c-127">skos:altLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-127">skos:altLabel</span></span>|
|<span data-ttu-id="cd96c-128">sharepoint-taxonomy:description</span><span class="sxs-lookup"><span data-stu-id="cd96c-128">sharepoint-taxonomy:description</span></span>|<span data-ttu-id="cd96c-129">skos:definition</span><span class="sxs-lookup"><span data-stu-id="cd96c-129">skos:definition</span></span>|
|<span data-ttu-id="cd96c-130">sharepoint-taxonomy:parent</span><span class="sxs-lookup"><span data-stu-id="cd96c-130">sharepoint-taxonomy:parent</span></span>|<span data-ttu-id="cd96c-131">skos:broader</span><span class="sxs-lookup"><span data-stu-id="cd96c-131">skos:broader</span></span>|
|<span data-ttu-id="cd96c-132">sharepoint-taxonomy:child</span><span class="sxs-lookup"><span data-stu-id="cd96c-132">sharepoint-taxonomy:child</span></span>|<span data-ttu-id="cd96c-133">skos:narrower</span><span class="sxs-lookup"><span data-stu-id="cd96c-133">skos:narrower</span></span>|

<span data-ttu-id="cd96c-134">Le tableau suivant affiche les entités du vocabulaire de taxonomie SharePoint dérivé de [OWL](https://www.w3.org/TR/owl2-primer/).</span><span class="sxs-lookup"><span data-stu-id="cd96c-134">The following table displays the entities of the SharePoint taxonomy vocabulary derived from [OWL](https://www.w3.org/TR/owl2-primer/).</span></span>

|<span data-ttu-id="cd96c-135">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="cd96c-135">SharePoint taxonomy vocabulary</span></span>|<span data-ttu-id="cd96c-136">Dérivé de OWL</span><span class="sxs-lookup"><span data-stu-id="cd96c-136">Derived from OWL</span></span>|
|:-----------------------------|:----------------------|
|<span data-ttu-id="cd96c-137">sharepoint-taxonomy:isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="cd96c-137">sharepoint-taxonomy:isAvailableForTagging</span></span>|<span data-ttu-id="cd96c-138">owl:datatypeproperty</span><span class="sxs-lookup"><span data-stu-id="cd96c-138">owl:datatypeproperty</span></span>|
|<span data-ttu-id="cd96c-139">sharepoint-taxonomy:SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-139">sharepoint-taxonomy:SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="cd96c-140">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="cd96c-140">owl:ObjectProperty</span></span>|
|<span data-ttu-id="cd96c-141">sharepoint-taxonomy:LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-141">sharepoint-taxonomy:LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="cd96c-142">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="cd96c-142">owl:ObjectProperty</span></span>|
|<span data-ttu-id="cd96c-143">sharepoint-taxonomy:CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-143">sharepoint-taxonomy:CustomPropertyForTermSet</span></span>|<span data-ttu-id="cd96c-144">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="cd96c-144">owl:ObjectProperty</span></span>|

## <a name="sharepoint-taxonomy-vocabulary"></a><span data-ttu-id="cd96c-145">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="cd96c-145">SharePoint taxonomy vocabulary</span></span>

<span data-ttu-id="cd96c-146">Une taxonomie est un système de classification formel.</span><span class="sxs-lookup"><span data-stu-id="cd96c-146">A taxonomy is a formal classification system.</span></span> <span data-ttu-id="cd96c-147">Une taxonomie regroupe les mots, les étiquettes et les termes qui décrivent un élément, puis organise les groupes au sein d’une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="cd96c-147">A taxonomy groups the words, labels, and terms that describe something, and then arranges the groups into a hierarchy.</span></span>

<span data-ttu-id="cd96c-148">**sharepoint-taxonomy:Term**</span><span class="sxs-lookup"><span data-stu-id="cd96c-148">**sharepoint-taxonomy:Term**</span></span>

<span data-ttu-id="cd96c-149">Représente un Terme ou un Mot-clé dans une hiérarchie de métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="cd96c-149">Represents a Term or a Keyword in a managed metadata hierarchy.</span></span>

<span data-ttu-id="cd96c-150">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) est l’unité atomique d’un [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd96c-150">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) is the atomic unit of a SharePoint [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span></span> <span data-ttu-id="cd96c-151">Chaque [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) appartient à un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) qui appartient à un [TermGroup](/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="cd96c-151">Each [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) belongs to a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) that belongs to a [TermGroup](/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> 

<span data-ttu-id="cd96c-152">La syntaxe pour définir un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cd96c-152">The syntax to define a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) is as follows:</span></span>

```SKOS
ex:TermA    a    sharepoint-taxonomy:Term;
    sharepoint-taxonomy:inTermSet    ex:TermSetA;
    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA;
    sharepoint-taxonomy:child    ex:TermA1;
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharePoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="cd96c-153">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) se trouve obligatoirement dans un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-153">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) compulsorily exists within a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-154">DefaultLabel est le nom du [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) tel qu’il apparaît dans la représentation visuelle.</span><span class="sxs-lookup"><span data-stu-id="cd96c-154">DefaultLabel is the name of the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) as it appears in the visual representation.</span></span> <span data-ttu-id="cd96c-155">Les champs obligatoires pour définir un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) incluent :</span><span class="sxs-lookup"><span data-stu-id="cd96c-155">The required fields for defining a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) include:</span></span>

- <span data-ttu-id="cd96c-156">sharepoint-taxonomy:defaultLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-156">sharepoint-taxonomy:defaultLabel</span></span>
- <span data-ttu-id="cd96c-157">sharepoint-taxonomy:inTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-157">sharepoint-taxonomy:inTermSet</span></span>

<span data-ttu-id="cd96c-158">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) peut :</span><span class="sxs-lookup"><span data-stu-id="cd96c-158">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) can:</span></span>

- <span data-ttu-id="cd96c-159">être lié de manière hiérarchique à un autre [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) à condition que les deux [Termes](/dotnet/api/microsoft.sharepoint.taxonomy.term) appartiennent au même [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-159">Be hierarchically related to another [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) that is provided both the [Terms](/dotnet/api/microsoft.sharepoint.taxonomy.term) belong to the same [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="cd96c-160">avoir plusieurs [Termes](/dotnet/api/microsoft.sharepoint.taxonomy.term) enfants, mais un seul [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="cd96c-160">Have multiple child [Terms](/dotnet/api/microsoft.sharepoint.taxonomy.term), but only a single parent [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>
- <span data-ttu-id="cd96c-161">ne pas avoir de [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) parent défini, s’il s’agit d’un topLevelTermOf d’un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-161">Not have a parent [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) defined, if it is a topLevelTermOf a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="cd96c-162">avoir un defaultLabel par langue de travail [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="cd96c-162">Have one defaultLabel, per [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>
- <span data-ttu-id="cd96c-163">ne pas exister s’il ne contient ni un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) parent, ni le topLevelTermOf d’un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-163">Not exist if it neither contains a parent [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term), nor is the topLevelTermOf a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> 
- <span data-ttu-id="cd96c-164">avoir seulement un defaultLabel unique dans le même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="cd96c-164">Have only a unique defaultLabel in the same hierarchical level.</span></span>

<span data-ttu-id="cd96c-165">**sharepoint-taxonomy:TermSet**</span><span class="sxs-lookup"><span data-stu-id="cd96c-165">**sharepoint-taxonomy:TermSet**</span></span>

<span data-ttu-id="cd96c-166">Représente un ensemble hiérarchique ou plat d’objets Terme appelé « TermSet ».</span><span class="sxs-lookup"><span data-stu-id="cd96c-166">Represents a hierarchical or flat set of Term objects known as a "TermSet".</span></span>

<span data-ttu-id="cd96c-167">Comme son nom l’indique, TermSet est un ensemble de [Termes](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-167">As the name suggests, TermSet is a set of [Terms](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="cd96c-168">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) doit appartenir à un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-168">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) must belong to a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-169">Aucun [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut exister indépendamment.</span><span class="sxs-lookup"><span data-stu-id="cd96c-169">No [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) can exist independently.</span></span> 

<span data-ttu-id="cd96c-170">La syntaxe pour définir un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-170">The syntax to define a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

```SKOS
ex:TermSetA    a    sharepoint-taxonomy:TermSet;
    sharepoint-taxonomy:termSetName    “TermSet A";
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharepoint-taxonomy:hasTopLevelTerm    Ex:Term A.
```

<span data-ttu-id="cd96c-171">Les [TermSets](/dotnet/api/microsoft.sharepoint.taxonomy.termset) sont regroupés de façon logique dans les [TermGroups](/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="cd96c-171">[TermSets](/dotnet/api/microsoft.sharepoint.taxonomy.termset) are logically grouped together in [TermGroups](/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> <span data-ttu-id="cd96c-172">Le champ obligatoire pour définir un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-172">The required field for defining a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

- <span data-ttu-id="cd96c-173">sharepoint-taxonomy:termSetName</span><span class="sxs-lookup"><span data-stu-id="cd96c-173">sharepoint-taxonomy:termSetName</span></span>

<span data-ttu-id="cd96c-174">Dans le cas où le termSetName fourni n’est pas unique dans le [TermGroup](/dotnet/api/microsoft.sharepoint.taxonomy.group), SharePoint ajoute un numéro à la fin du nom pour maintenir l’unicité du ou des termSetName.</span><span class="sxs-lookup"><span data-stu-id="cd96c-174">In the case of the termSetName provided is not unique within the [TermGroup](/dotnet/api/microsoft.sharepoint.taxonomy.group), SharePoint appends a number at the end of the name to maintain the uniqueness of termSetName(s).</span></span>

<span data-ttu-id="cd96c-175">**sharepoint-taxonomy:hasTopLevelTerm**</span><span class="sxs-lookup"><span data-stu-id="cd96c-175">**sharepoint-taxonomy:hasTopLevelTerm**</span></span>

<span data-ttu-id="cd96c-176">SharePoint utilise cette propriété pour mapper le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur dans le [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), qui est le point d’entrée de la hiérarchie des [Termes](/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-176">SharePoint uses this property to map the top most [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) in the [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), which is the entry point to the hierarchy of [Terms](/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-177">Il s’agit d’une relation inverse avec la taxonomie sharepoint:topLevelTermOf.</span><span class="sxs-lookup"><span data-stu-id="cd96c-177">This is an inverse relation to sharepoint-taxonomy:topLevelTermOf.</span></span> 

<span data-ttu-id="cd96c-178">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-178">The syntax to define this is:</span></span>

```SKOS
ex:TermSetA    sharepoint-taxonomy:hasTopLevelTerm    ex:TermA.
```

>[!NOTE]
> <span data-ttu-id="cd96c-179">Vous ne pouvez pas définir le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur d’un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="cd96c-179">You cannot define the top level [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) of a parent [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="cd96c-180">**sharepoint-taxonomy:topLevelTermOf**</span><span class="sxs-lookup"><span data-stu-id="cd96c-180">**sharepoint-taxonomy:topLevelTermOf**</span></span>

<span data-ttu-id="cd96c-181">Sharepoint-taxonomy:topLevelTermOf est l’inverse de sharepoint-taxonomy:hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-181">Sharepoint-taxonomy:topLevelTermOf is the inverse of sharepoint-taxonomy:hasTopLevelTerm</span></span>

<span data-ttu-id="cd96c-182">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-182">The syntax to define this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA.
```

<span data-ttu-id="cd96c-183">**sharepoint-taxonomy:inTermSet**</span><span class="sxs-lookup"><span data-stu-id="cd96c-183">**sharepoint-taxonomy:inTermSet**</span></span>

<span data-ttu-id="cd96c-184">Utilisez ceci pour mapper un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) à un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-184">Use this to map a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) to a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-185">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut exister que dans un seul [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-185">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) can only exist in a single [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-186">SharePoint requiert cette propriété lors de la [définition d’un terme](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-186">SharePoint requires this property when [defining a term](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span></span>

## <a name="required-labels"></a><span data-ttu-id="cd96c-187">Étiquettes requises</span><span class="sxs-lookup"><span data-stu-id="cd96c-187">Required labels</span></span>

<span data-ttu-id="cd96c-188">Votre organisation peut souhaiter effectuer une planification minutieuse avant de commencer à utiliser des métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="cd96c-188">Your organization may want to do careful planning before you start to use managed metadata.</span></span> <span data-ttu-id="cd96c-189">La quantité de planification que vous devez effectuer dépend de la formalité de votre taxonomie.</span><span class="sxs-lookup"><span data-stu-id="cd96c-189">The amount of planning that you must do depends on how formal your taxonomy is.</span></span> <span data-ttu-id="cd96c-190">Cela dépend également du degré de contrôle que vous souhaitez imposer aux métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cd96c-190">It also depends on how much control that you want to impose on metadata.</span></span> <span data-ttu-id="cd96c-191">À chaque niveau de la hiérarchie, vous devez configurer les étiquettes requises pour un Terme ou un TermSet.</span><span class="sxs-lookup"><span data-stu-id="cd96c-191">At each level of the hierarchy, you need to configure required labels for a Term or TermSet.</span></span>

<span data-ttu-id="cd96c-192">Un Terme peut avoir une ou plusieurs étiquettes dans la langue par défaut et zéro ou plusieurs étiquettes dans la langue autre que celle par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd96c-192">A Term can have one or more labels in the default language, and zero or more labels in the non-default language.</span></span> <span data-ttu-id="cd96c-193">Si le terme a des étiquettes dans une langue, l’une des étiquettes doit être l’étiquette par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd96c-193">If the term has labels in a language, one of the labels must be the default label.</span></span>

<span data-ttu-id="cd96c-194">**sharepoint-taxonomy:defaultLabel**</span><span class="sxs-lookup"><span data-stu-id="cd96c-194">**sharepoint-taxonomy:defaultLabel**</span></span>

<span data-ttu-id="cd96c-195">Utilisez cette étiquette lexicale par défaut pour un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) qui est un paramètre obligatoire pour un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-195">Use this default lexical label for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) that is a required parameter for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="cd96c-196">Utilisez-la pour représenter visuellement le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-196">Use to visually representing the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="cd96c-197">La syntaxe pour définir un defaultLabel est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-197">The syntax to define a defaultLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="cd96c-198">Le defaultLabel contient deux parties : la chaîne et la balise de langue.</span><span class="sxs-lookup"><span data-stu-id="cd96c-198">The defaultLabel contains two parts to it – the string and the language tag.</span></span> <span data-ttu-id="cd96c-199">La langue doit être l’une des langues de travail du [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="cd96c-199">The language must be one of the [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working languages.</span></span> <span data-ttu-id="cd96c-200">Le defaultLabel doit être unique pour tous les [Termes](/dotnet/api/microsoft.sharepoint.taxonomy.term) du même [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), au même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="cd96c-200">The defaultLabel must be unique for all [Terms](/dotnet/api/microsoft.sharepoint.taxonomy.term) in the same [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), at the same hierarchical level.</span></span>

<span data-ttu-id="cd96c-201">**sharepoint-taxonomy:termSetName**</span><span class="sxs-lookup"><span data-stu-id="cd96c-201">**sharepoint-taxonomy:termSetName**</span></span>

<span data-ttu-id="cd96c-202">Obtient et définit le nom de l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="cd96c-202">Gets and sets the name for the current TermSet object.</span></span>

<span data-ttu-id="cd96c-203">Il s’agit de l’étiquette lexicale d’un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), dans une langue de travail [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="cd96c-203">This the lexical label for a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), in a [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span> <span data-ttu-id="cd96c-204">Il s’agit d’un paramètre obligatoire pour un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-204">This is a required parameter for a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-205">Utilisez-la pour représenter visuellement un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-205">Use to visually representing a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>

<span data-ttu-id="cd96c-206">La syntaxe pour définir un termSetName est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-206">The syntax to define a termSetName is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:TermSetName    “Term Set A”@en-us.
```

<span data-ttu-id="cd96c-207">**sharepoint-taxonomy:propertyName**</span><span class="sxs-lookup"><span data-stu-id="cd96c-207">**sharepoint-taxonomy:propertyName**</span></span>

<span data-ttu-id="cd96c-208">Obtient et définit le nom de propriété de l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="cd96c-208">Gets and sets the property name for the current TermSet object.</span></span>

<span data-ttu-id="cd96c-209">Il s’agit d’une étiquette lexicale pour sharepoint-taxonomy:SharedCustomPropertyForTerm, sharepoint-taxonomy:LocalCustomPropertyForTerm et sharepoint-taxonomy:CustomPropertyForTermSet dans une langue de travail [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="cd96c-209">This is the lexical label for a sharepoint-taxonomy:SharedCustomPropertyForTerm, sharepoint-taxonomy:LocalCustomPropertyForTerm and sharepoint-taxonomy:CustomPropertyForTermSet in a [TermStore](/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>

<span data-ttu-id="cd96c-210">Le sharepoint-taxonomy:propertyName est traité comme la clé de CustomProperty.</span><span class="sxs-lookup"><span data-stu-id="cd96c-210">The sharepoint-taxonomy:propertyName is treated as the key of the CustomProperty.</span></span>

<span data-ttu-id="cd96c-211">La syntaxe pour définir un propetyName est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-211">The syntax to define a propetyName is:</span></span>

```SKOS
ex:SharedCustomProperty1    sharepoint-taxonomy:propertyName    “Shared Custom Property Key 1”@en-us.
```

## <a name="optional-labels"></a><span data-ttu-id="cd96c-212">Étiquettes facultatives</span><span class="sxs-lookup"><span data-stu-id="cd96c-212">Optional labels</span></span>

<span data-ttu-id="cd96c-213">Vous pouvez également ajouter des étiquettes facultatives à votre taxonomie.</span><span class="sxs-lookup"><span data-stu-id="cd96c-213">You can also add optional labels to your taxonomy.</span></span>

<span data-ttu-id="cd96c-214">**sharepoint-taxonomy:otherLabel**</span><span class="sxs-lookup"><span data-stu-id="cd96c-214">**sharepoint-taxonomy:otherLabel**</span></span>

<span data-ttu-id="cd96c-215">Il s’agit de l’étiquette lexicale alternative pour un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-215">This is the alternate lexical label for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="cd96c-216">La syntaxe pour définir un otherLabel est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-216">The syntax to define an otherLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:otherLabel    “Term A”@en-us.
```

## <a name="semantic-relationships"></a><span data-ttu-id="cd96c-217">Relations sémantiques</span><span class="sxs-lookup"><span data-stu-id="cd96c-217">Semantic relationships</span></span>

<span data-ttu-id="cd96c-218">Les taxonomies ont une relation hiérarchique et parfois une simple relation associative de « terme apparenté », mais certaines ont des « relations sémantiques » ou des relations créées sur mesure.</span><span class="sxs-lookup"><span data-stu-id="cd96c-218">Taxonomies have hierarchical and sometimes a simple “related term” associative relationship, but some have "semantic relationships" or custom-created relationships.</span></span> 

<span data-ttu-id="cd96c-219">**sharepoint-taxonomy:parent**</span><span class="sxs-lookup"><span data-stu-id="cd96c-219">**sharepoint-taxonomy:parent**</span></span>

<span data-ttu-id="cd96c-220">Cela relie hiérarchiquement un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-220">This hierarchically relates a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="cd96c-221">Un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) peut être un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur d’un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), mais si ce n’est pas le cas, il doit avoir un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="cd96c-221">A [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) could be a top level [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) of a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), but in case it doesn’t it must have a parent [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="cd96c-222">La syntaxe pour définir un parent est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-222">The syntax to define a parent is:</span></span>

```SKOS
ex:TermA1    sharepoint-taxonomy:parent    ex:TermA.
```

<span data-ttu-id="cd96c-223">Cela signifie que TermA est le parent et TermA est l’enfant.</span><span class="sxs-lookup"><span data-stu-id="cd96c-223">This means that TermA is the parent and  TermA is the child.</span></span>

<span data-ttu-id="cd96c-224">**sharepoint-taxonomy:child**</span><span class="sxs-lookup"><span data-stu-id="cd96c-224">**sharepoint-taxonomy:child**</span></span>

<span data-ttu-id="cd96c-225">L’objet contient une ou plusieurs instances TermSet enfants, accessibles via la propriété TermSets.</span><span class="sxs-lookup"><span data-stu-id="cd96c-225">The object contains one or more child TermSet instances, and these can be accessed through the TermSets property.</span></span> <span data-ttu-id="cd96c-226">Cette classe fournit également des méthodes pour créer de nouveaux objets TermSet enfants.</span><span class="sxs-lookup"><span data-stu-id="cd96c-226">This class also provides methods for creating new child TermSet objects.</span></span> <span data-ttu-id="cd96c-227">Les autorisations de modification des instances de Term et de TermSet enfants sont spécifiées sur le groupe.</span><span class="sxs-lookup"><span data-stu-id="cd96c-227">Permissions for editing child Term and TermSet instances is specified on the group.</span></span> 

<span data-ttu-id="cd96c-228">Cela relie hiérarchiquement un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="cd96c-228">This hierarchically relates a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="cd96c-229">La syntaxe pour définir un enfant est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-229">The syntax to define a child is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:child    ex:TermA1.
```

<span data-ttu-id="cd96c-230">Cela signifie que TermA est le parent et TermA est l’enfant.</span><span class="sxs-lookup"><span data-stu-id="cd96c-230">This means that TermA is the parent and  TermA is the child.</span></span>

## <a name="documentation-notes"></a><span data-ttu-id="cd96c-231">Notes de documentation</span><span class="sxs-lookup"><span data-stu-id="cd96c-231">Documentation notes</span></span>

<span data-ttu-id="cd96c-232">Cette section décrit la taxonomie détaillée dans Microsoft.SharePoint.Taxonomy Namespace.</span><span class="sxs-lookup"><span data-stu-id="cd96c-232">This section discusses the taxonomy detailed in the Microsoft.SharePoint.Taxonomy Namespace.</span></span>

<span data-ttu-id="cd96c-233">**sharepoint-taxonomy:description**</span><span class="sxs-lookup"><span data-stu-id="cd96c-233">**sharepoint-taxonomy:description**</span></span>

<span data-ttu-id="cd96c-234">Il s’agit d’une explication détaillée des entités de vocabulaire de la [taxonomie SharePoint](/dotnet/api/microsoft.sharepoint.taxonomy).</span><span class="sxs-lookup"><span data-stu-id="cd96c-234">This is a detailed explanation of any [SharePoint taxonomy](/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary entity.</span></span> 

<span data-ttu-id="cd96c-235">La syntaxe pour ajouter une description est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-235">The syntax to add a description is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:description    “Term A is the top level term of TermSetA”@en-us.
```

## <a name="custom-properties"></a><span data-ttu-id="cd96c-236">Propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="cd96c-236">Custom properties</span></span>

<span data-ttu-id="cd96c-237">Obtient la collection d’objets de propriété personnalisés pour l’objet Term actuel à partir du dictionnaire en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cd96c-237">Gets the collection of custom property objects for the current Term object from the read-only dictionary.</span></span>

<span data-ttu-id="cd96c-238">Les propriétés personnalisées sont des paires de valeurs-clés qui peuvent être définies pour un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), pour approfondir la description du [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ou d’un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="cd96c-238">Custom Properties are key-values pairs that can be defined for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset), to further the description of the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="cd96c-239">SharePoint spécifie la clé de la propriété personnalisée à l’aide de propertyName.</span><span class="sxs-lookup"><span data-stu-id="cd96c-239">SharePoint specifies the key of the custom property with the help of propertyName.</span></span>

<span data-ttu-id="cd96c-240">**sharepoint-taxonomy:CustomPropertyForTermSet**</span><span class="sxs-lookup"><span data-stu-id="cd96c-240">**sharepoint-taxonomy:CustomPropertyForTermSet**</span></span>

<span data-ttu-id="cd96c-241">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-241">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp1    rdf:type    sharepoint-taxonomy:CustomPropertyForTermSet;
    sharepoint-taxonomy:propertyName “Colour”.

ex:TermSetA    ex:CustomProp1    “Red”@en-us.
```

<span data-ttu-id="cd96c-242">**sharepoint-taxonomy:SharedCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="cd96c-242">**sharepoint-taxonomy:SharedCustomPropertyForTerm**</span></span>

<span data-ttu-id="cd96c-243">Si la propriété personnalisée d’un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) doit être transportée avec le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous SharedCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="cd96c-243">If the custom property for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) needs to be carried along with the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to be define it under SharedCustomPropertyForTerm.</span></span>

<span data-ttu-id="cd96c-244">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-244">The syntax to define this is:</span></span>

``` SKOS
ex:CustomProp2    rdf:type sharepoint-taxonomy:SharedCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “Length”.

ex:TermA    ex:CustomProp2    “5 cm”@en-us.
```
<span data-ttu-id="cd96c-245">**sharepoint-taxonomy:LocalCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="cd96c-245">**sharepoint-taxonomy:LocalCustomPropertyForTerm**</span></span>

<span data-ttu-id="cd96c-246">Si la propriété personnalisée d’un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) n’a pas besoin d’être transportée avec le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous LocalCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="cd96c-246">If the custom property for a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) does not need to be carried along with the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to define it under LocalCustomPropertyForTerm.</span></span>

<span data-ttu-id="cd96c-247">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-247">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp3    rdf:type sharepoint-taxonomy:LocalCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “width”.

ex:TermA    ex:CustomProp3    “5 cm”@en-us.
```

## <a name="data-properties"></a><span data-ttu-id="cd96c-248">Propriétés des données</span><span class="sxs-lookup"><span data-stu-id="cd96c-248">Data properties</span></span>

<span data-ttu-id="cd96c-249">À chaque niveau de la hiérarchie, vous pouvez configurer des propriétés de données spécifiques pour un Term ou TermSet.</span><span class="sxs-lookup"><span data-stu-id="cd96c-249">At each level of the hierarchy, you can configure specific data properties for a Term or TermSet.</span></span>

<span data-ttu-id="cd96c-250">**sharepoint-taxonomy:isAvailableForTagging**</span><span class="sxs-lookup"><span data-stu-id="cd96c-250">**sharepoint-taxonomy:isAvailableForTagging**</span></span>

<span data-ttu-id="cd96c-251">Utilisez cette option pour spécifier si un [Terme](/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) est disponible dans les listes et bibliothèques SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd96c-251">Use this to specify if a [Term](/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](/dotnet/api/microsoft.sharepoint.taxonomy.termset) available in SharePoint Lists and Libraries.</span></span>  

<span data-ttu-id="cd96c-252">La syntaxe pour cela est :</span><span class="sxs-lookup"><span data-stu-id="cd96c-252">The syntax for this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:isAvailableForTagging     "true"^^xsd:Boolean;
```

## <a name="domain-and-range"></a><span data-ttu-id="cd96c-253">Domaine et plage</span><span class="sxs-lookup"><span data-stu-id="cd96c-253">Domain and range</span></span>

<span data-ttu-id="cd96c-254">Le tableau ci-dessous décrit le domaine et la plage du vocabulaire de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd96c-254">The table below describes the domain and range of SharePoint taxonomy vocabulary.</span></span>

|<span data-ttu-id="cd96c-255">Prédicats/verbe</span><span class="sxs-lookup"><span data-stu-id="cd96c-255">Predicates/verb</span></span>|<span data-ttu-id="cd96c-256">Signification</span><span class="sxs-lookup"><span data-stu-id="cd96c-256">Meaning</span></span>|<span data-ttu-id="cd96c-257">Domaine</span><span class="sxs-lookup"><span data-stu-id="cd96c-257">Domain</span></span>|<span data-ttu-id="cd96c-258">Plage</span><span class="sxs-lookup"><span data-stu-id="cd96c-258">Range</span></span>|
|:--------------|:------|:-----|:----|
<span data-ttu-id="cd96c-259">inTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-259">inTermSet</span></span>|<span data-ttu-id="cd96c-260">Dans l’ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="cd96c-260">In term set</span></span>|<span data-ttu-id="cd96c-261">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-261">Term</span></span>|<span data-ttu-id="cd96c-262">Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="cd96c-262">Term Set</span></span>|
<span data-ttu-id="cd96c-263">inTermGroup</span><span class="sxs-lookup"><span data-stu-id="cd96c-263">inTermGroup</span></span>|<span data-ttu-id="cd96c-264">Dans le groupe de termes</span><span class="sxs-lookup"><span data-stu-id="cd96c-264">In term group</span></span>|<span data-ttu-id="cd96c-265">TermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-265">TermSet</span></span>|<span data-ttu-id="cd96c-266">TermGroup</span><span class="sxs-lookup"><span data-stu-id="cd96c-266">TermGroup</span></span>|
<span data-ttu-id="cd96c-267">topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="cd96c-267">topLevelTermOf</span></span>|<span data-ttu-id="cd96c-268">Est le Terme de niveau supérieur de</span><span class="sxs-lookup"><span data-stu-id="cd96c-268">Is Top Level Term Of</span></span>|<span data-ttu-id="cd96c-269">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-269">Term</span></span>|<span data-ttu-id="cd96c-270">TermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-270">TermSet</span></span>|
<span data-ttu-id="cd96c-271">hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-271">hasTopLevelTerm</span></span>|<span data-ttu-id="cd96c-272">A un terme de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="cd96c-272">Has top level term</span></span>|<span data-ttu-id="cd96c-273">Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="cd96c-273">Term Set</span></span>|<span data-ttu-id="cd96c-274">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-274">Term</span></span>|
<span data-ttu-id="cd96c-275">termSetName</span><span class="sxs-lookup"><span data-stu-id="cd96c-275">termSetName</span></span>|<span data-ttu-id="cd96c-276">L’ensemble de Termes a un nom</span><span class="sxs-lookup"><span data-stu-id="cd96c-276">Term set has Name</span></span>|<span data-ttu-id="cd96c-277">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-277">Term</span></span>|<span data-ttu-id="cd96c-278">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="cd96c-278">Plain literal</span></span>|
<span data-ttu-id="cd96c-279">defaultLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-279">defaultLabel</span></span>|<span data-ttu-id="cd96c-280">Le Terme a une étiquette par défaut</span><span class="sxs-lookup"><span data-stu-id="cd96c-280">Term has default label</span></span>|<span data-ttu-id="cd96c-281">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-281">Term</span></span>|<span data-ttu-id="cd96c-282">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="cd96c-282">Plain literal</span></span>|
<span data-ttu-id="cd96c-283">otherLabel</span><span class="sxs-lookup"><span data-stu-id="cd96c-283">otherLabel</span></span>|<span data-ttu-id="cd96c-284">Le Terme a une autre étiquette</span><span class="sxs-lookup"><span data-stu-id="cd96c-284">Term has other label</span></span>|<span data-ttu-id="cd96c-285">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-285">Term</span></span>|<span data-ttu-id="cd96c-286">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="cd96c-286">Plain literal</span></span>|
<span data-ttu-id="cd96c-287">propertyName</span><span class="sxs-lookup"><span data-stu-id="cd96c-287">propertyName</span></span>|<span data-ttu-id="cd96c-288">A une étiquette de propriété</span><span class="sxs-lookup"><span data-stu-id="cd96c-288">Has Property Label</span></span>|<span data-ttu-id="cd96c-289">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-289">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span></span> |<span data-ttu-id="cd96c-290">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="cd96c-290">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="cd96c-291">description</span><span class="sxs-lookup"><span data-stu-id="cd96c-291">description</span></span>|<span data-ttu-id="cd96c-292">A une description</span><span class="sxs-lookup"><span data-stu-id="cd96c-292">Has Description</span></span>|<span data-ttu-id="cd96c-293">Tous</span><span class="sxs-lookup"><span data-stu-id="cd96c-293">All</span></span>|<span data-ttu-id="cd96c-294">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="cd96c-294">Plain literal</span></span>|
|<span data-ttu-id="cd96c-295">parent</span><span class="sxs-lookup"><span data-stu-id="cd96c-295">parent</span></span>|<span data-ttu-id="cd96c-296">A un parent</span><span class="sxs-lookup"><span data-stu-id="cd96c-296">Has parent</span></span>|<span data-ttu-id="cd96c-297">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-297">Term</span></span>|<span data-ttu-id="cd96c-298">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-298">Term</span></span>|
|<span data-ttu-id="cd96c-299">enfant</span><span class="sxs-lookup"><span data-stu-id="cd96c-299">child</span></span>|<span data-ttu-id="cd96c-300">a un enfant</span><span class="sxs-lookup"><span data-stu-id="cd96c-300">Has Child</span></span>|<span data-ttu-id="cd96c-301">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-301">Term</span></span>|<span data-ttu-id="cd96c-302">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-302">Term</span></span>|
|<span data-ttu-id="cd96c-303">isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="cd96c-303">isAvailableForTagging</span></span>|<span data-ttu-id="cd96c-304">Est disponible pour le marquage</span><span class="sxs-lookup"><span data-stu-id="cd96c-304">Is available for tagging</span></span>|<span data-ttu-id="cd96c-305">Terme, Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="cd96c-305">Term, Term Set</span></span>|<span data-ttu-id="cd96c-306">Booléen</span><span class="sxs-lookup"><span data-stu-id="cd96c-306">Boolean</span></span>|
|<span data-ttu-id="cd96c-307">SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-307">SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="cd96c-308">A partagé une propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="cd96c-308">Has shared custom property</span></span>|<span data-ttu-id="cd96c-309">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-309">Term</span></span>|<span data-ttu-id="cd96c-310">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="cd96c-310">Boolean, string, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="cd96c-311">LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="cd96c-311">LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="cd96c-312">Possède une propriété personnalisée locale</span><span class="sxs-lookup"><span data-stu-id="cd96c-312">Has local custom property</span></span>|<span data-ttu-id="cd96c-313">Term</span><span class="sxs-lookup"><span data-stu-id="cd96c-313">Term</span></span>|<span data-ttu-id="cd96c-314">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="cd96c-314">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="cd96c-315">CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-315">CustomPropertyForTermSet</span></span>|<span data-ttu-id="cd96c-316">Possède une propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="cd96c-316">Has Custom Property</span></span>|<span data-ttu-id="cd96c-317">TermSet</span><span class="sxs-lookup"><span data-stu-id="cd96c-317">TermSet</span></span>|<span data-ttu-id="cd96c-318">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="cd96c-318">Boolean, String, Integer, Decimal, Double</span></span>|

<span data-ttu-id="cd96c-319">Scénarios [SKOS](https://www.w3.org/TR/skos-primer/) valides que la [taxonomie SharePoint](/dotnet/api/microsoft.sharepoint.taxonomy) n’autorise pas :</span><span class="sxs-lookup"><span data-stu-id="cd96c-319">[SKOS](https://www.w3.org/TR/skos-primer/) valid scenarios that [SharePoint taxonomy](/dotnet/api/microsoft.sharepoint.taxonomy) does not allow:</span></span>

- <span data-ttu-id="cd96c-320">Redondance hiérarchique : un concept [SKOS](https://www.w3.org/TR/skos-primer/) peut être attaché à plusieurs concepts plus larges en même temps, mais sharepoint-taxonomy:Term ne peut avoir qu’un seul sharepoint-taxonomy:parent, donc la dépendance cyclique des Termes n’est pas non plus autorisé.</span><span class="sxs-lookup"><span data-stu-id="cd96c-320">Hierarchical redundancy - A [SKOS](https://www.w3.org/TR/skos-primer/) concept can be attached to several broader concepts at the same time, but a sharepoint-taxonomy:Term can have only one sharepoint-taxonomy:parent, hence cyclic dependency, of Terms is also not allowed.</span></span>
- <span data-ttu-id="cd96c-321">Les termes orphelins ne sont pas autorisés dans la taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cd96c-321">Orphaned terms are not allowed in SharePoint taxonomy.</span></span> <span data-ttu-id="cd96c-322">Chaque sharepoint-taxonomy:Term doit avoir un sharepoint-taxonomy:parent ou doit être le sharepoint-taxonomy:topLevelTermOf d’un TermSet.</span><span class="sxs-lookup"><span data-stu-id="cd96c-322">Every sharepoint-taxonomy:Term should either have a sharepoint-taxonomy:parent or it should be the sharepoint-taxonomy:topLevelTermOf a TermSet.</span></span>
- <span data-ttu-id="cd96c-323">La taxonomie SharePoint ne prend pas en charge les relations associatives.</span><span class="sxs-lookup"><span data-stu-id="cd96c-323">SharePoint taxonomy does not support associative relations.</span></span>
- <span data-ttu-id="cd96c-324">La taxonomie SharePoint n’autorise que 2 types de relations hiérarchiques : sharepoint-taxonomy:parent et sharepoint-Taxonomy:child.</span><span class="sxs-lookup"><span data-stu-id="cd96c-324">SharePoint taxonomy only allows 2 types of Hierarchical relations – sharepoint-taxonomy:parent and sharepoint-Taxonomy:child.</span></span> 
- <span data-ttu-id="cd96c-325">Contrairement à [SKOS](https://www.w3.org/TR/skos-primer/), la relation hiérarchique dans le vocabulaire de la taxonomie SharePoint ne peut être établie qu’avec des Termes dans le même TermSet.</span><span class="sxs-lookup"><span data-stu-id="cd96c-325">Unlike [SKOS](https://www.w3.org/TR/skos-primer/) the hierarchical relationship in SharePoint taxonomy vocabulary, can only be established with Terms within the same TermSet.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd96c-326">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd96c-326">See also</span></span>

[<span data-ttu-id="cd96c-327">Importer un ensemble de termes avec un format basé sur SKOS</span><span class="sxs-lookup"><span data-stu-id="cd96c-327">Import a term set using a SKOS-based format</span></span>](import-term-set-skos.md)