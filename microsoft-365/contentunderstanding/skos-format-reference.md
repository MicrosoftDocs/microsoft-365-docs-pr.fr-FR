---
title: Référence de format SKOS pour la taxonomie SharePoint
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: Référence de format SKOS pour la taxonomie SharePoint
ms.openlocfilehash: f81b618a7c302ce033c4e8ce2f7400e9616f2de0
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321324"
---
# <a name="skos-format-reference-for-sharepoint-taxonomy"></a><span data-ttu-id="ce1de-103">Référence de format SKOS pour la taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce1de-103">SKOS format reference for SharePoint taxonomy</span></span>

<span data-ttu-id="ce1de-104">Cet article comprend le vocabulaire RDF utilisé pour représenter la [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) et est basé sur [SKOS](https://www.w3.org/TR/skos-primer/).</span><span class="sxs-lookup"><span data-stu-id="ce1de-104">This article includes RDF vocabulary used to represent [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) and is based on [SKOS](https://www.w3.org/TR/skos-primer/).</span></span> <span data-ttu-id="ce1de-105">Pour la sérialisation de cette syntaxe RDF, utilisez RDF [TURTLE](https://www.w3.org/TR/turtle/).</span><span class="sxs-lookup"><span data-stu-id="ce1de-105">For serialization of this RDF syntax, use RDF [TURTLE](https://www.w3.org/TR/turtle/).</span></span>

<span data-ttu-id="ce1de-106">Le tableau suivant affiche les équivalents [SKOS](https://www.w3.org/TR/skos-primer/) pour le vocabulaire de [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy).</span><span class="sxs-lookup"><span data-stu-id="ce1de-106">The following table shows the [SKOS](https://www.w3.org/TR/skos-primer/) equivalents for the [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary.</span></span> <span data-ttu-id="ce1de-107">SharePoint ne prend pas en charge les valeurs [SKOS](https://www.w3.org/TR/skos-primer/) qui n’ont pas d’équivalent de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ce1de-107">SharePoint does not support [SKOS](https://www.w3.org/TR/skos-primer/) values that have no SharePoint taxonomy equivalent.</span></span>

|<span data-ttu-id="ce1de-108">Taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce1de-108">SharePoint taxonomy</span></span>|<span data-ttu-id="ce1de-109">Équivalent SKOS</span><span class="sxs-lookup"><span data-stu-id="ce1de-109">SKOS equivalent</span></span>|
|:-----------------|:--------------|
|<span data-ttu-id="ce1de-110">sharepoint-taxonomy:Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-110">sharepoint-taxonomy:Term</span></span>|<span data-ttu-id="ce1de-111">skos:Concept</span><span class="sxs-lookup"><span data-stu-id="ce1de-111">skos:Concept</span></span>|
|<span data-ttu-id="ce1de-112">sharepoint-taxonomy:TermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-112">sharepoint-taxonomy:TermSet</span></span>|<span data-ttu-id="ce1de-113">skos:ConceptScheme</span><span class="sxs-lookup"><span data-stu-id="ce1de-113">skos:ConceptScheme</span></span>|
|<span data-ttu-id="ce1de-114">sharepoint-taxonomy:inTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-114">sharepoint-taxonomy:inTermSet</span></span>|<span data-ttu-id="ce1de-115">skos:inScheme</span><span class="sxs-lookup"><span data-stu-id="ce1de-115">skos:inScheme</span></span>|
|<span data-ttu-id="ce1de-116">sharepoint-taxonomy:hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-116">sharepoint-taxonomy:hasTopLevelTerm</span></span>|<span data-ttu-id="ce1de-117">skos:hasTopConcept</span><span class="sxs-lookup"><span data-stu-id="ce1de-117">skos:hasTopConcept</span></span>|
|<span data-ttu-id="ce1de-118">sharepoint-taxonomy:topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="ce1de-118">sharepoint-taxonomy:topLevelTermOf</span></span>|<span data-ttu-id="ce1de-119">skos:topConceptOf</span><span class="sxs-lookup"><span data-stu-id="ce1de-119">skos:topConceptOf</span></span>|
|<span data-ttu-id="ce1de-120">sharepoint-taxonomy:defaultLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-120">sharepoint-taxonomy:defaultLabel</span></span>|<span data-ttu-id="ce1de-121">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-121">skos:prefLabel</span></span>|
|<span data-ttu-id="ce1de-122">sharepoint-taxonomy:termSetName</span><span class="sxs-lookup"><span data-stu-id="ce1de-122">sharepoint-taxonomy:termSetName</span></span>|<span data-ttu-id="ce1de-123">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-123">skos:prefLabel</span></span>|
|<span data-ttu-id="ce1de-124">sharepoint-taxonomy:propertyName</span><span class="sxs-lookup"><span data-stu-id="ce1de-124">sharepoint-taxonomy:propertyName</span></span>|<span data-ttu-id="ce1de-125">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-125">skos:prefLabel</span></span>|
|<span data-ttu-id="ce1de-126">sharepoint-taxonomy:otherLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-126">sharepoint-taxonomy:otherLabel</span></span>|<span data-ttu-id="ce1de-127">skos:altLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-127">skos:altLabel</span></span>|
|<span data-ttu-id="ce1de-128">sharepoint-taxonomy:description</span><span class="sxs-lookup"><span data-stu-id="ce1de-128">sharepoint-taxonomy:description</span></span>|<span data-ttu-id="ce1de-129">skos:definition</span><span class="sxs-lookup"><span data-stu-id="ce1de-129">skos:definition</span></span>|
|<span data-ttu-id="ce1de-130">sharepoint-taxonomy:parent</span><span class="sxs-lookup"><span data-stu-id="ce1de-130">sharepoint-taxonomy:parent</span></span>|<span data-ttu-id="ce1de-131">skos:broader</span><span class="sxs-lookup"><span data-stu-id="ce1de-131">skos:broader</span></span>|
|<span data-ttu-id="ce1de-132">sharepoint-taxonomy:child</span><span class="sxs-lookup"><span data-stu-id="ce1de-132">sharepoint-taxonomy:child</span></span>|<span data-ttu-id="ce1de-133">skos:narrower</span><span class="sxs-lookup"><span data-stu-id="ce1de-133">skos:narrower</span></span>|

<span data-ttu-id="ce1de-134">Le tableau suivant affiche les entités du vocabulaire de taxonomie SharePoint dérivé de [OWL](https://www.w3.org/TR/owl2-primer/).</span><span class="sxs-lookup"><span data-stu-id="ce1de-134">The following table displays the entities of the SharePoint taxonomy vocabulary derived from [OWL](https://www.w3.org/TR/owl2-primer/).</span></span>

|<span data-ttu-id="ce1de-135">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce1de-135">SharePoint taxonomy vocabulary</span></span>|<span data-ttu-id="ce1de-136">Dérivé de OWL</span><span class="sxs-lookup"><span data-stu-id="ce1de-136">Derived from OWL</span></span>|
|:-----------------------------|:----------------------|
|<span data-ttu-id="ce1de-137">sharepoint-taxonomy:isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="ce1de-137">sharepoint-taxonomy:isAvailableForTagging</span></span>|<span data-ttu-id="ce1de-138">owl:datatypeproperty</span><span class="sxs-lookup"><span data-stu-id="ce1de-138">owl:datatypeproperty</span></span>|
|<span data-ttu-id="ce1de-139">sharepoint-taxonomy:SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-139">sharepoint-taxonomy:SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="ce1de-140">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="ce1de-140">owl:ObjectProperty</span></span>|
|<span data-ttu-id="ce1de-141">sharepoint-taxonomy:LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-141">sharepoint-taxonomy:LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="ce1de-142">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="ce1de-142">owl:ObjectProperty</span></span>|
|<span data-ttu-id="ce1de-143">sharepoint-taxonomy:CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-143">sharepoint-taxonomy:CustomPropertyForTermSet</span></span>|<span data-ttu-id="ce1de-144">owl:ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="ce1de-144">owl:ObjectProperty</span></span>|

## <a name="sharepoint-taxonomy-vocabulary"></a><span data-ttu-id="ce1de-145">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="ce1de-145">SharePoint taxonomy vocabulary</span></span>

<span data-ttu-id="ce1de-146">Une taxonomie est un système de classification formel.</span><span class="sxs-lookup"><span data-stu-id="ce1de-146">A taxonomy is a formal classification system.</span></span> <span data-ttu-id="ce1de-147">Une taxonomie regroupe les mots, les étiquettes et les termes qui décrivent un élément, puis organise les groupes au sein d’une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="ce1de-147">A taxonomy groups the words, labels, and terms that describe something, and then arranges the groups into a hierarchy.</span></span>

<span data-ttu-id="ce1de-148">**sharepoint-taxonomy:Term**</span><span class="sxs-lookup"><span data-stu-id="ce1de-148">**sharepoint-taxonomy:Term**</span></span>

<span data-ttu-id="ce1de-149">Représente un Terme ou un Mot-clé dans une hiérarchie de métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="ce1de-149">Represents a Term or a Keyword in a managed metadata hierarchy.</span></span>

<span data-ttu-id="ce1de-150">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) est l’unité atomique d’un [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ce1de-150">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) is the atomic unit of a SharePoint [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span></span> <span data-ttu-id="ce1de-151">Chaque [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) appartient à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) qui appartient à un [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="ce1de-151">Each [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) belongs to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) that belongs to a [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> 

<span data-ttu-id="ce1de-152">La syntaxe pour définir un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ce1de-152">The syntax to define a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) is as follows:</span></span>

```SKOS
ex:TermA    a    sharepoint-taxonomy:Term;
    sharepoint-taxonomy:inTermSet    ex:TermSetA;
    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA;
    sharepoint-taxonomy:child    ex:TermA1;
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharePoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="ce1de-153">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) se trouve obligatoirement dans un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-153">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) compulsorily exists within a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-154">DefaultLabel est le nom du [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) tel qu’il apparaît dans la représentation visuelle.</span><span class="sxs-lookup"><span data-stu-id="ce1de-154">DefaultLabel is the name of the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) as it appears in the visual representation.</span></span> <span data-ttu-id="ce1de-155">Les champs obligatoires pour définir un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) incluent :</span><span class="sxs-lookup"><span data-stu-id="ce1de-155">The required fields for defining a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) include:</span></span>

- <span data-ttu-id="ce1de-156">sharepoint-taxonomy:defaultLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-156">sharepoint-taxonomy:defaultLabel</span></span>
- <span data-ttu-id="ce1de-157">sharepoint-taxonomy:inTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-157">sharepoint-taxonomy:inTermSet</span></span>

<span data-ttu-id="ce1de-158">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) peut :</span><span class="sxs-lookup"><span data-stu-id="ce1de-158">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can:</span></span>

- <span data-ttu-id="ce1de-159">être lié de manière hiérarchique à un autre [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à condition que les deux [Termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) appartiennent au même [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-159">Be hierarchically related to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) that is provided both the [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) belong to the same [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="ce1de-160">avoir plusieurs [Termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) enfants, mais un seul [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="ce1de-160">Have multiple child [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), but only a single parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>
- <span data-ttu-id="ce1de-161">ne pas avoir de [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent défini, s’il s’agit d’un topLevelTermOf d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-161">Not have a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) defined, if it is a topLevelTermOf a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="ce1de-162">avoir un defaultLabel par langue de travail [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="ce1de-162">Have one defaultLabel, per [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>
- <span data-ttu-id="ce1de-163">ne pas exister s’il ne contient ni un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent, ni le topLevelTermOf d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-163">Not exist if it neither contains a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), nor is the topLevelTermOf a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> 
- <span data-ttu-id="ce1de-164">avoir seulement un defaultLabel unique dans le même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="ce1de-164">Have only a unique defaultLabel in the same hierarchical level.</span></span>

<span data-ttu-id="ce1de-165">**sharepoint-taxonomy:TermSet**</span><span class="sxs-lookup"><span data-stu-id="ce1de-165">**sharepoint-taxonomy:TermSet**</span></span>

<span data-ttu-id="ce1de-166">Représente un ensemble hiérarchique ou plat d’objets Terme appelé « TermSet ».</span><span class="sxs-lookup"><span data-stu-id="ce1de-166">Represents a hierarchical or flat set of Term objects known as a "TermSet".</span></span>

<span data-ttu-id="ce1de-167">Comme son nom l’indique, TermSet est un ensemble de [Termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-167">As the name suggests, TermSet is a set of [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="ce1de-168">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) doit appartenir à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-168">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) must belong to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-169">Aucun [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut exister indépendamment.</span><span class="sxs-lookup"><span data-stu-id="ce1de-169">No [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can exist independently.</span></span> 

<span data-ttu-id="ce1de-170">La syntaxe pour définir un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-170">The syntax to define a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

```SKOS
ex:TermSetA    a    sharepoint-taxonomy:TermSet;
    sharepoint-taxonomy:termSetName    “TermSet A";
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharepoint-taxonomy:hasTopLevelTerm    Ex:Term A.
```

<span data-ttu-id="ce1de-171">Les [TermSets](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) sont regroupés de façon logique dans les [TermGroups](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="ce1de-171">[TermSets](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) are logically grouped together in [TermGroups](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> <span data-ttu-id="ce1de-172">Le champ obligatoire pour définir un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-172">The required field for defining a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

- <span data-ttu-id="ce1de-173">sharepoint-taxonomy:termSetName</span><span class="sxs-lookup"><span data-stu-id="ce1de-173">sharepoint-taxonomy:termSetName</span></span>

<span data-ttu-id="ce1de-174">Dans le cas où le termSetName fourni n’est pas unique dans le [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group), SharePoint ajoute un numéro à la fin du nom pour maintenir l’unicité du ou des termSetName.</span><span class="sxs-lookup"><span data-stu-id="ce1de-174">In the case of the termSetName provided is not unique within the [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group), SharePoint appends a number at the end of the name to maintain the uniqueness of termSetName(s).</span></span>

<span data-ttu-id="ce1de-175">**sharepoint-taxonomy:hasTopLevelTerm**</span><span class="sxs-lookup"><span data-stu-id="ce1de-175">**sharepoint-taxonomy:hasTopLevelTerm**</span></span>

<span data-ttu-id="ce1de-176">SharePoint utilise cette propriété pour mapper le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur dans le [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), qui est le point d’entrée de la hiérarchie des [Termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-176">SharePoint uses this property to map the top most [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in the [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), which is the entry point to the hierarchy of [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-177">Il s’agit d’une relation inverse avec la taxonomie sharepoint:topLevelTermOf.</span><span class="sxs-lookup"><span data-stu-id="ce1de-177">This is an inverse relation to sharepoint-taxonomy:topLevelTermOf.</span></span> 

<span data-ttu-id="ce1de-178">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-178">The syntax to define this is:</span></span>

```SKOS
ex:TermSetA    sharepoint-taxonomy:hasTopLevelTerm    ex:TermA.
```

>[!NOTE]
> <span data-ttu-id="ce1de-179">Vous ne pouvez pas définir le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur d’un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="ce1de-179">You cannot define the top level [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) of a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="ce1de-180">**sharepoint-taxonomy:topLevelTermOf**</span><span class="sxs-lookup"><span data-stu-id="ce1de-180">**sharepoint-taxonomy:topLevelTermOf**</span></span>

<span data-ttu-id="ce1de-181">Sharepoint-taxonomy:topLevelTermOf est l’inverse de sharepoint-taxonomy:hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-181">Sharepoint-taxonomy:topLevelTermOf is the inverse of sharepoint-taxonomy:hasTopLevelTerm</span></span>

<span data-ttu-id="ce1de-182">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-182">The syntax to define this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA.
```

<span data-ttu-id="ce1de-183">**sharepoint-taxonomy:inTermSet**</span><span class="sxs-lookup"><span data-stu-id="ce1de-183">**sharepoint-taxonomy:inTermSet**</span></span>

<span data-ttu-id="ce1de-184">Utilisez ceci pour mapper un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-184">Use this to map a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-185">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut exister que dans un seul [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-185">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can only exist in a single [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-186">SharePoint requiert cette propriété lors de la [définition d’un terme](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-186">SharePoint requires this property when [defining a term](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span></span>

## <a name="required-labels"></a><span data-ttu-id="ce1de-187">Étiquettes requises</span><span class="sxs-lookup"><span data-stu-id="ce1de-187">Required labels</span></span>

<span data-ttu-id="ce1de-188">Votre organisation peut souhaiter effectuer une planification minutieuse avant de commencer à utiliser des métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="ce1de-188">Your organization may want to do careful planning before you start to use managed metadata.</span></span> <span data-ttu-id="ce1de-189">La quantité de planification que vous devez effectuer dépend de la formalité de votre taxonomie.</span><span class="sxs-lookup"><span data-stu-id="ce1de-189">The amount of planning that you must do depends on how formal your taxonomy is.</span></span> <span data-ttu-id="ce1de-190">Cela dépend également du degré de contrôle que vous souhaitez imposer aux métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ce1de-190">It also depends on how much control that you want to impose on metadata.</span></span> <span data-ttu-id="ce1de-191">À chaque niveau de la hiérarchie, vous devez configurer les étiquettes requises pour un Terme ou un TermSet.</span><span class="sxs-lookup"><span data-stu-id="ce1de-191">At each level of the hierarchy, you need to configure required labels for a Term or TermSet.</span></span>

<span data-ttu-id="ce1de-192">Un Terme peut avoir une ou plusieurs étiquettes dans la langue par défaut et zéro ou plusieurs étiquettes dans la langue autre que celle par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce1de-192">A Term can have one or more labels in the default language, and zero or more labels in the non-default language.</span></span> <span data-ttu-id="ce1de-193">Si le terme a des étiquettes dans une langue, l’une des étiquettes doit être l’étiquette par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce1de-193">If the term has labels in a language, one of the labels must be the default label.</span></span>

<span data-ttu-id="ce1de-194">**sharepoint-taxonomy:defaultLabel**</span><span class="sxs-lookup"><span data-stu-id="ce1de-194">**sharepoint-taxonomy:defaultLabel**</span></span>

<span data-ttu-id="ce1de-195">Utilisez cette étiquette lexicale par défaut pour un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) qui est un paramètre obligatoire pour un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-195">Use this default lexical label for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) that is a required parameter for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="ce1de-196">Utilisez-la pour représenter visuellement le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-196">Use to visually representing the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="ce1de-197">La syntaxe pour définir un defaultLabel est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-197">The syntax to define a defaultLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="ce1de-198">Le defaultLabel contient deux parties : la chaîne et la balise de langue.</span><span class="sxs-lookup"><span data-stu-id="ce1de-198">The defaultLabel contains two parts to it – the string and the language tag.</span></span> <span data-ttu-id="ce1de-199">La langue doit être l’une des langues de travail du [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="ce1de-199">The language must be one of the [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working languages.</span></span> <span data-ttu-id="ce1de-200">Le defaultLabel doit être unique pour tous les [Termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) du même [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), au même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="ce1de-200">The defaultLabel must be unique for all [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in the same [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), at the same hierarchical level.</span></span>

<span data-ttu-id="ce1de-201">**sharepoint-taxonomy:termSetName**</span><span class="sxs-lookup"><span data-stu-id="ce1de-201">**sharepoint-taxonomy:termSetName**</span></span>

<span data-ttu-id="ce1de-202">Obtient et définit le nom de l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="ce1de-202">Gets and sets the name for the current TermSet object.</span></span>

<span data-ttu-id="ce1de-203">Il s’agit de l’étiquette lexicale d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), dans une langue de travail [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="ce1de-203">This the lexical label for a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span> <span data-ttu-id="ce1de-204">Il s’agit d’un paramètre obligatoire pour un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-204">This is a required parameter for a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-205">Utilisez-la pour représenter visuellement un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-205">Use to visually representing a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>

<span data-ttu-id="ce1de-206">La syntaxe pour définir un termSetName est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-206">The syntax to define a termSetName is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:TermSetName    “Term Set A”@en-us.
```

<span data-ttu-id="ce1de-207">**sharepoint-taxonomy:propertyName**</span><span class="sxs-lookup"><span data-stu-id="ce1de-207">**sharepoint-taxonomy:propertyName**</span></span>

<span data-ttu-id="ce1de-208">Obtient et définit le nom de propriété de l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="ce1de-208">Gets and sets the property name for the current TermSet object.</span></span>

<span data-ttu-id="ce1de-209">Il s’agit d’une étiquette lexicale pour sharepoint-taxonomy:SharedCustomPropertyForTerm, sharepoint-taxonomy:LocalCustomPropertyForTerm et sharepoint-taxonomy:CustomPropertyForTermSet dans une langue de travail [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span><span class="sxs-lookup"><span data-stu-id="ce1de-209">This is the lexical label for a sharepoint-taxonomy:SharedCustomPropertyForTerm, sharepoint-taxonomy:LocalCustomPropertyForTerm and sharepoint-taxonomy:CustomPropertyForTermSet in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>

<span data-ttu-id="ce1de-210">Le sharepoint-taxonomy:propertyName est traité comme la clé de CustomProperty.</span><span class="sxs-lookup"><span data-stu-id="ce1de-210">The sharepoint-taxonomy:propertyName is treated as the key of the CustomProperty.</span></span>

<span data-ttu-id="ce1de-211">La syntaxe pour définir un propetyName est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-211">The syntax to define a propetyName is:</span></span>

```SKOS
ex:SharedCustomProperty1    sharepoint-taxonomy:propertyName    “Shared Custom Property Key 1”@en-us.
```

## <a name="optional-labels"></a><span data-ttu-id="ce1de-212">Étiquettes facultatives</span><span class="sxs-lookup"><span data-stu-id="ce1de-212">Optional labels</span></span>

<span data-ttu-id="ce1de-213">Vous pouvez également ajouter des étiquettes facultatives à votre taxonomie.</span><span class="sxs-lookup"><span data-stu-id="ce1de-213">You can also add optional labels to your taxonomy.</span></span>

<span data-ttu-id="ce1de-214">**sharepoint-taxonomy:otherLabel**</span><span class="sxs-lookup"><span data-stu-id="ce1de-214">**sharepoint-taxonomy:otherLabel**</span></span>

<span data-ttu-id="ce1de-215">Il s’agit de l’étiquette lexicale alternative pour un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-215">This is the alternate lexical label for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="ce1de-216">La syntaxe pour définir un otherLabel est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-216">The syntax to define an otherLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:otherLabel    “Term A”@en-us.
```

## <a name="semantic-relationships"></a><span data-ttu-id="ce1de-217">Relations sémantiques</span><span class="sxs-lookup"><span data-stu-id="ce1de-217">Semantic relationships</span></span>

<span data-ttu-id="ce1de-218">Les taxonomies ont une relation hiérarchique et parfois une simple relation associative de « terme apparenté », mais certaines ont des « relations sémantiques » ou des relations créées sur mesure.</span><span class="sxs-lookup"><span data-stu-id="ce1de-218">Taxonomies have hierarchical and sometimes a simple “related term” associative relationship, but some have "semantic relationships" or custom-created relationships.</span></span> 

<span data-ttu-id="ce1de-219">**sharepoint-taxonomy:parent**</span><span class="sxs-lookup"><span data-stu-id="ce1de-219">**sharepoint-taxonomy:parent**</span></span>

<span data-ttu-id="ce1de-220">Cela relie hiérarchiquement un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-220">This hierarchically relates a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="ce1de-221">Un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) peut être un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) supérieur d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), mais si ce n’est pas le cas, il doit avoir un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent.</span><span class="sxs-lookup"><span data-stu-id="ce1de-221">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) could be a top level [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) of a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), but in case it doesn’t it must have a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="ce1de-222">La syntaxe pour définir un parent est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-222">The syntax to define a parent is:</span></span>

```SKOS
ex:TermA1    sharepoint-taxonomy:parent    ex:TermA.
```

<span data-ttu-id="ce1de-223">Cela signifie que TermA est le parent et TermA est l’enfant.</span><span class="sxs-lookup"><span data-stu-id="ce1de-223">This means that TermA is the parent and  TermA is the child.</span></span>

<span data-ttu-id="ce1de-224">**sharepoint-taxonomy:child**</span><span class="sxs-lookup"><span data-stu-id="ce1de-224">**sharepoint-taxonomy:child**</span></span>

<span data-ttu-id="ce1de-225">L’objet contient une ou plusieurs instances TermSet enfants, accessibles via la propriété TermSets.</span><span class="sxs-lookup"><span data-stu-id="ce1de-225">The object contains one or more child TermSet instances, and these can be accessed through the TermSets property.</span></span> <span data-ttu-id="ce1de-226">Cette classe fournit également des méthodes pour créer de nouveaux objets TermSet enfants.</span><span class="sxs-lookup"><span data-stu-id="ce1de-226">This class also provides methods for creating new child TermSet objects.</span></span> <span data-ttu-id="ce1de-227">Les autorisations de modification des instances de Term et de TermSet enfants sont spécifiées sur le groupe.</span><span class="sxs-lookup"><span data-stu-id="ce1de-227">Permissions for editing child Term and TermSet instances is specified on the group.</span></span> 

<span data-ttu-id="ce1de-228">Cela relie hiérarchiquement un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="ce1de-228">This hierarchically relates a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="ce1de-229">La syntaxe pour définir un enfant est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-229">The syntax to define a child is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:child    ex:TermA1.
```

<span data-ttu-id="ce1de-230">Cela signifie que TermA est le parent et TermA est l’enfant.</span><span class="sxs-lookup"><span data-stu-id="ce1de-230">This means that TermA is the parent and  TermA is the child.</span></span>

## <a name="documentation-notes"></a><span data-ttu-id="ce1de-231">Notes de documentation</span><span class="sxs-lookup"><span data-stu-id="ce1de-231">Documentation notes</span></span>

<span data-ttu-id="ce1de-232">Cette section décrit la taxonomie détaillée dans Microsoft.SharePoint.Taxonomy Namespace.</span><span class="sxs-lookup"><span data-stu-id="ce1de-232">This section discusses the taxonomy detailed in the Microsoft.SharePoint.Taxonomy Namespace.</span></span>

<span data-ttu-id="ce1de-233">**sharepoint-taxonomy:description**</span><span class="sxs-lookup"><span data-stu-id="ce1de-233">**sharepoint-taxonomy:description**</span></span>

<span data-ttu-id="ce1de-234">Il s’agit d’une explication détaillée des entités de vocabulaire de la [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy).</span><span class="sxs-lookup"><span data-stu-id="ce1de-234">This is a detailed explanation of any [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary entity.</span></span> 

<span data-ttu-id="ce1de-235">La syntaxe pour ajouter une description est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-235">The syntax to add a description is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:description    “Term A is the top level term of TermSetA”@en-us.
```

## <a name="custom-properties"></a><span data-ttu-id="ce1de-236">Propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="ce1de-236">Custom properties</span></span>

<span data-ttu-id="ce1de-237">Obtient la collection d’objets de propriété personnalisés pour l’objet Term actuel à partir du dictionnaire en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ce1de-237">Gets the collection of custom property objects for the current Term object from the read-only dictionary.</span></span>

<span data-ttu-id="ce1de-238">Les propriétés personnalisées sont des paires de valeurs-clés qui peuvent être définies pour un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), pour approfondir la description du [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="ce1de-238">Custom Properties are key-values pairs that can be defined for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), to further the description of the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="ce1de-239">SharePoint spécifie la clé de la propriété personnalisée à l’aide de propertyName.</span><span class="sxs-lookup"><span data-stu-id="ce1de-239">SharePoint specifies the key of the custom property with the help of propertyName.</span></span>

<span data-ttu-id="ce1de-240">**sharepoint-taxonomy:CustomPropertyForTermSet**</span><span class="sxs-lookup"><span data-stu-id="ce1de-240">**sharepoint-taxonomy:CustomPropertyForTermSet**</span></span>

<span data-ttu-id="ce1de-241">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-241">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp1    rdf:type    sharepoint-taxonomy:CustomPropertyForTermSet;
    sharepoint-taxonomy:propertyName “Colour”.

ex:TermSetA    ex:CustomProp1    “Red”@en-us.
```

<span data-ttu-id="ce1de-242">**sharepoint-taxonomy:SharedCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="ce1de-242">**sharepoint-taxonomy:SharedCustomPropertyForTerm**</span></span>

<span data-ttu-id="ce1de-243">Si la propriété personnalisée d’un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) doit être transportée avec le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous SharedCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="ce1de-243">If the custom property for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) needs to be carried along with the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to be define it under SharedCustomPropertyForTerm.</span></span>

<span data-ttu-id="ce1de-244">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-244">The syntax to define this is:</span></span>

``` SKOS
ex:CustomProp2    rdf:type sharepoint-taxonomy:SharedCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “Length”.

ex:TermA    ex:CustomProp2    “5 cm”@en-us.
```
<span data-ttu-id="ce1de-245">**sharepoint-taxonomy:LocalCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="ce1de-245">**sharepoint-taxonomy:LocalCustomPropertyForTerm**</span></span>

<span data-ttu-id="ce1de-246">Si la propriété personnalisée d’un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) n’a pas besoin d’être transportée avec le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous LocalCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="ce1de-246">If the custom property for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) does not need to be carried along with the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to define it under LocalCustomPropertyForTerm.</span></span>

<span data-ttu-id="ce1de-247">La syntaxe pour définir ceci est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-247">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp3    rdf:type sharepoint-taxonomy:LocalCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “width”.

ex:TermA    ex:CustomProp3    “5 cm”@en-us.
```

## <a name="data-properties"></a><span data-ttu-id="ce1de-248">Propriétés des données</span><span class="sxs-lookup"><span data-stu-id="ce1de-248">Data properties</span></span>

<span data-ttu-id="ce1de-249">À chaque niveau de la hiérarchie, vous pouvez configurer des propriétés de données spécifiques pour un Term ou TermSet.</span><span class="sxs-lookup"><span data-stu-id="ce1de-249">At each level of the hierarchy, you can configure specific data properties for a Term or TermSet.</span></span>

<span data-ttu-id="ce1de-250">**sharepoint-taxonomy:isAvailableForTagging**</span><span class="sxs-lookup"><span data-stu-id="ce1de-250">**sharepoint-taxonomy:isAvailableForTagging**</span></span>

<span data-ttu-id="ce1de-251">Utilisez cette option pour spécifier si un [Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est disponible dans les listes et bibliothèques SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ce1de-251">Use this to specify if a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) available in SharePoint Lists and Libraries.</span></span>  

<span data-ttu-id="ce1de-252">La syntaxe pour cela est :</span><span class="sxs-lookup"><span data-stu-id="ce1de-252">The syntax for this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:isAvailableForTagging     "true"^^xsd:Boolean;
```

## <a name="domain-and-range"></a><span data-ttu-id="ce1de-253">Domaine et plage</span><span class="sxs-lookup"><span data-stu-id="ce1de-253">Domain and range</span></span>

<span data-ttu-id="ce1de-254">Le tableau ci-dessous décrit le domaine et la plage du vocabulaire de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ce1de-254">The table below describes the domain and range of SharePoint taxonomy vocabulary.</span></span>

|<span data-ttu-id="ce1de-255">Prédicats/verbe</span><span class="sxs-lookup"><span data-stu-id="ce1de-255">Predicates/verb</span></span>|<span data-ttu-id="ce1de-256">Signification</span><span class="sxs-lookup"><span data-stu-id="ce1de-256">Meaning</span></span>|<span data-ttu-id="ce1de-257">Domaine</span><span class="sxs-lookup"><span data-stu-id="ce1de-257">Domain</span></span>|<span data-ttu-id="ce1de-258">Plage</span><span class="sxs-lookup"><span data-stu-id="ce1de-258">Range</span></span>|
|:--------------|:------|:-----|:----|
<span data-ttu-id="ce1de-259">inTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-259">inTermSet</span></span>|<span data-ttu-id="ce1de-260">Dans l’ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="ce1de-260">In term set</span></span>|<span data-ttu-id="ce1de-261">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-261">Term</span></span>|<span data-ttu-id="ce1de-262">Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="ce1de-262">Term Set</span></span>|
<span data-ttu-id="ce1de-263">inTermGroup</span><span class="sxs-lookup"><span data-stu-id="ce1de-263">inTermGroup</span></span>|<span data-ttu-id="ce1de-264">Dans le groupe de termes</span><span class="sxs-lookup"><span data-stu-id="ce1de-264">In term group</span></span>|<span data-ttu-id="ce1de-265">TermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-265">TermSet</span></span>|<span data-ttu-id="ce1de-266">TermGroup</span><span class="sxs-lookup"><span data-stu-id="ce1de-266">TermGroup</span></span>|
<span data-ttu-id="ce1de-267">topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="ce1de-267">topLevelTermOf</span></span>|<span data-ttu-id="ce1de-268">Est le Terme de niveau supérieur de</span><span class="sxs-lookup"><span data-stu-id="ce1de-268">Is Top Level Term Of</span></span>|<span data-ttu-id="ce1de-269">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-269">Term</span></span>|<span data-ttu-id="ce1de-270">TermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-270">TermSet</span></span>|
<span data-ttu-id="ce1de-271">hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-271">hasTopLevelTerm</span></span>|<span data-ttu-id="ce1de-272">A un terme de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="ce1de-272">Has top level term</span></span>|<span data-ttu-id="ce1de-273">Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="ce1de-273">Term Set</span></span>|<span data-ttu-id="ce1de-274">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-274">Term</span></span>|
<span data-ttu-id="ce1de-275">termSetName</span><span class="sxs-lookup"><span data-stu-id="ce1de-275">termSetName</span></span>|<span data-ttu-id="ce1de-276">L’ensemble de Termes a un nom</span><span class="sxs-lookup"><span data-stu-id="ce1de-276">Term set has Name</span></span>|<span data-ttu-id="ce1de-277">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-277">Term</span></span>|<span data-ttu-id="ce1de-278">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="ce1de-278">Plain literal</span></span>|
<span data-ttu-id="ce1de-279">defaultLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-279">defaultLabel</span></span>|<span data-ttu-id="ce1de-280">Le Terme a une étiquette par défaut</span><span class="sxs-lookup"><span data-stu-id="ce1de-280">Term has default label</span></span>|<span data-ttu-id="ce1de-281">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-281">Term</span></span>|<span data-ttu-id="ce1de-282">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="ce1de-282">Plain literal</span></span>|
<span data-ttu-id="ce1de-283">otherLabel</span><span class="sxs-lookup"><span data-stu-id="ce1de-283">otherLabel</span></span>|<span data-ttu-id="ce1de-284">Le Terme a une autre étiquette</span><span class="sxs-lookup"><span data-stu-id="ce1de-284">Term has other label</span></span>|<span data-ttu-id="ce1de-285">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-285">Term</span></span>|<span data-ttu-id="ce1de-286">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="ce1de-286">Plain literal</span></span>|
<span data-ttu-id="ce1de-287">propertyName</span><span class="sxs-lookup"><span data-stu-id="ce1de-287">propertyName</span></span>|<span data-ttu-id="ce1de-288">A une étiquette de propriété</span><span class="sxs-lookup"><span data-stu-id="ce1de-288">Has Property Label</span></span>|<span data-ttu-id="ce1de-289">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-289">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span></span> |<span data-ttu-id="ce1de-290">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="ce1de-290">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="ce1de-291">description</span><span class="sxs-lookup"><span data-stu-id="ce1de-291">description</span></span>|<span data-ttu-id="ce1de-292">A une description</span><span class="sxs-lookup"><span data-stu-id="ce1de-292">Has Description</span></span>|<span data-ttu-id="ce1de-293">Tous</span><span class="sxs-lookup"><span data-stu-id="ce1de-293">All</span></span>|<span data-ttu-id="ce1de-294">Littéral simple</span><span class="sxs-lookup"><span data-stu-id="ce1de-294">Plain literal</span></span>|
|<span data-ttu-id="ce1de-295">parent</span><span class="sxs-lookup"><span data-stu-id="ce1de-295">parent</span></span>|<span data-ttu-id="ce1de-296">A un parent</span><span class="sxs-lookup"><span data-stu-id="ce1de-296">Has parent</span></span>|<span data-ttu-id="ce1de-297">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-297">Term</span></span>|<span data-ttu-id="ce1de-298">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-298">Term</span></span>|
|<span data-ttu-id="ce1de-299">enfant</span><span class="sxs-lookup"><span data-stu-id="ce1de-299">child</span></span>|<span data-ttu-id="ce1de-300">a un enfant</span><span class="sxs-lookup"><span data-stu-id="ce1de-300">Has Child</span></span>|<span data-ttu-id="ce1de-301">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-301">Term</span></span>|<span data-ttu-id="ce1de-302">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-302">Term</span></span>|
|<span data-ttu-id="ce1de-303">isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="ce1de-303">isAvailableForTagging</span></span>|<span data-ttu-id="ce1de-304">Est disponible pour le marquage</span><span class="sxs-lookup"><span data-stu-id="ce1de-304">Is available for tagging</span></span>|<span data-ttu-id="ce1de-305">Terme, Ensemble de Termes</span><span class="sxs-lookup"><span data-stu-id="ce1de-305">Term, Term Set</span></span>|<span data-ttu-id="ce1de-306">Booléen</span><span class="sxs-lookup"><span data-stu-id="ce1de-306">Boolean</span></span>|
|<span data-ttu-id="ce1de-307">SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-307">SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="ce1de-308">A partagé une propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="ce1de-308">Has shared custom property</span></span>|<span data-ttu-id="ce1de-309">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-309">Term</span></span>|<span data-ttu-id="ce1de-310">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="ce1de-310">Boolean, string, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="ce1de-311">LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="ce1de-311">LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="ce1de-312">Possède une propriété personnalisée locale</span><span class="sxs-lookup"><span data-stu-id="ce1de-312">Has local custom property</span></span>|<span data-ttu-id="ce1de-313">Term</span><span class="sxs-lookup"><span data-stu-id="ce1de-313">Term</span></span>|<span data-ttu-id="ce1de-314">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="ce1de-314">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="ce1de-315">CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-315">CustomPropertyForTermSet</span></span>|<span data-ttu-id="ce1de-316">Possède une propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="ce1de-316">Has Custom Property</span></span>|<span data-ttu-id="ce1de-317">TermSet</span><span class="sxs-lookup"><span data-stu-id="ce1de-317">TermSet</span></span>|<span data-ttu-id="ce1de-318">Booléen, chaîne, entier, décimal, double</span><span class="sxs-lookup"><span data-stu-id="ce1de-318">Boolean, String, Integer, Decimal, Double</span></span>|

<span data-ttu-id="ce1de-319">Scénarios [SKOS](https://www.w3.org/TR/skos-primer/) valides que la [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) n’autorise pas :</span><span class="sxs-lookup"><span data-stu-id="ce1de-319">[SKOS](https://www.w3.org/TR/skos-primer/) valid scenarios that [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) does not allow:</span></span>

- <span data-ttu-id="ce1de-320">Redondance hiérarchique : un concept [SKOS](https://www.w3.org/TR/skos-primer/) peut être attaché à plusieurs concepts plus larges en même temps, mais sharepoint-taxonomy:Term ne peut avoir qu’un seul sharepoint-taxonomy:parent, donc la dépendance cyclique des Termes n’est pas non plus autorisé.</span><span class="sxs-lookup"><span data-stu-id="ce1de-320">Hierarchical redundancy - A [SKOS](https://www.w3.org/TR/skos-primer/) concept can be attached to several broader concepts at the same time, but a sharepoint-taxonomy:Term can have only one sharepoint-taxonomy:parent, hence cyclic dependency, of Terms is also not allowed.</span></span>
- <span data-ttu-id="ce1de-321">Les termes orphelins ne sont pas autorisés dans la taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ce1de-321">Orphaned terms are not allowed in SharePoint taxonomy.</span></span> <span data-ttu-id="ce1de-322">Chaque sharepoint-taxonomy:Term doit avoir un sharepoint-taxonomy:parent ou doit être le sharepoint-taxonomy:topLevelTermOf d’un TermSet.</span><span class="sxs-lookup"><span data-stu-id="ce1de-322">Every sharepoint-taxonomy:Term should either have a sharepoint-taxonomy:parent or it should be the sharepoint-taxonomy:topLevelTermOf a TermSet.</span></span>
- <span data-ttu-id="ce1de-323">La taxonomie SharePoint ne prend pas en charge les relations associatives.</span><span class="sxs-lookup"><span data-stu-id="ce1de-323">SharePoint taxonomy does not support associative relations.</span></span>
- <span data-ttu-id="ce1de-324">La taxonomie SharePoint n’autorise que 2 types de relations hiérarchiques : sharepoint-taxonomy:parent et sharepoint-Taxonomy:child.</span><span class="sxs-lookup"><span data-stu-id="ce1de-324">SharePoint taxonomy only allows 2 types of Hierarchical relations – sharepoint-taxonomy:parent and sharepoint-Taxonomy:child.</span></span> 
- <span data-ttu-id="ce1de-325">Contrairement à [SKOS](https://www.w3.org/TR/skos-primer/), la relation hiérarchique dans le vocabulaire de la taxonomie SharePoint ne peut être établie qu’avec des Termes dans le même TermSet.</span><span class="sxs-lookup"><span data-stu-id="ce1de-325">Unlike [SKOS](https://www.w3.org/TR/skos-primer/) the hierarchical relationship in SharePoint taxonomy vocabulary, can only be established with Terms within the same TermSet.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce1de-326">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce1de-326">See also</span></span>

[<span data-ttu-id="ce1de-327">Importer un ensemble de termes avec un format basé sur SKOS</span><span class="sxs-lookup"><span data-stu-id="ce1de-327">Import a term set using a SKOS-based format</span></span>](import-term-set-skos.md)

