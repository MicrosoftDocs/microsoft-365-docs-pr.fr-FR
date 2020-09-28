---
title: Référence de format SKOS pour la taxonomie SharePoint
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
description: Référence de format SKOS pour la taxonomie SharePoint
ms.openlocfilehash: eb228394b06b6e6027937ab105df7c0079875226
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295895"
---
# <a name="skos-format-reference-for-sharepoint-taxonomy"></a><span data-ttu-id="fb416-103">Référence de format SKOS pour la taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="fb416-103">SKOS format reference for SharePoint taxonomy</span></span>

<span data-ttu-id="fb416-104">Cet article inclut le vocabulaire RDF utilisé pour représenter la [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) et s’appuie sur [SKOS](https://www.w3.org/TR/skos-primer/).</span><span class="sxs-lookup"><span data-stu-id="fb416-104">This article includes RDF vocabulary used to represent [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) and is based on [SKOS](https://www.w3.org/TR/skos-primer/).</span></span> <span data-ttu-id="fb416-105">Pour la sérialisation de cette syntaxe RDF, utilisez RDF [Turtle](https://www.w3.org/TR/turtle/).</span><span class="sxs-lookup"><span data-stu-id="fb416-105">For serialization of this RDF syntax, use RDF [TURTLE](https://www.w3.org/TR/turtle/).</span></span>

<span data-ttu-id="fb416-106">Le tableau suivant présente les équivalents [SKOS](https://www.w3.org/TR/skos-primer/) pour le vocabulaire de [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) .</span><span class="sxs-lookup"><span data-stu-id="fb416-106">The following table shows the [SKOS](https://www.w3.org/TR/skos-primer/) equivalents for the [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary.</span></span> <span data-ttu-id="fb416-107">SharePoint ne prend pas en charge les valeurs [SKOS](https://www.w3.org/TR/skos-primer/) qui n’ont pas d’équivalent de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fb416-107">SharePoint does not support [SKOS](https://www.w3.org/TR/skos-primer/) values that have no SharePoint taxonomy equivalent.</span></span>

|<span data-ttu-id="fb416-108">Taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="fb416-108">SharePoint taxonomy</span></span>|<span data-ttu-id="fb416-109">Équivalent SKOS</span><span class="sxs-lookup"><span data-stu-id="fb416-109">SKOS equivalent</span></span>|
|:-----------------|:--------------|
|<span data-ttu-id="fb416-110">SharePoint-taxonomie : terme</span><span class="sxs-lookup"><span data-stu-id="fb416-110">sharepoint-taxonomy:Term</span></span>|<span data-ttu-id="fb416-111">SKOS : concept</span><span class="sxs-lookup"><span data-stu-id="fb416-111">skos:Concept</span></span>|
|<span data-ttu-id="fb416-112">SharePoint-taxonomie : TermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-112">sharepoint-taxonomy:TermSet</span></span>|<span data-ttu-id="fb416-113">skos:ConceptScheme</span><span class="sxs-lookup"><span data-stu-id="fb416-113">skos:ConceptScheme</span></span>|
|<span data-ttu-id="fb416-114">SharePoint-taxonomie : inTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-114">sharepoint-taxonomy:inTermSet</span></span>|<span data-ttu-id="fb416-115">SKOS : inscheme</span><span class="sxs-lookup"><span data-stu-id="fb416-115">skos:inScheme</span></span>|
|<span data-ttu-id="fb416-116">SharePoint-taxonomie : hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-116">sharepoint-taxonomy:hasTopLevelTerm</span></span>|<span data-ttu-id="fb416-117">skos:hasTopConcept</span><span class="sxs-lookup"><span data-stu-id="fb416-117">skos:hasTopConcept</span></span>|
|<span data-ttu-id="fb416-118">SharePoint-taxonomie : topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="fb416-118">sharepoint-taxonomy:topLevelTermOf</span></span>|<span data-ttu-id="fb416-119">skos:topConceptOf</span><span class="sxs-lookup"><span data-stu-id="fb416-119">skos:topConceptOf</span></span>|
|<span data-ttu-id="fb416-120">SharePoint-taxonomie : defaultLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-120">sharepoint-taxonomy:defaultLabel</span></span>|<span data-ttu-id="fb416-121">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-121">skos:prefLabel</span></span>|
|<span data-ttu-id="fb416-122">SharePoint-taxonomie : termSetName</span><span class="sxs-lookup"><span data-stu-id="fb416-122">sharepoint-taxonomy:termSetName</span></span>|<span data-ttu-id="fb416-123">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-123">skos:prefLabel</span></span>|
|<span data-ttu-id="fb416-124">SharePoint-taxonomie : propertyName</span><span class="sxs-lookup"><span data-stu-id="fb416-124">sharepoint-taxonomy:propertyName</span></span>|<span data-ttu-id="fb416-125">skos:prefLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-125">skos:prefLabel</span></span>|
|<span data-ttu-id="fb416-126">SharePoint-taxonomie : otherLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-126">sharepoint-taxonomy:otherLabel</span></span>|<span data-ttu-id="fb416-127">skos:altLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-127">skos:altLabel</span></span>|
|<span data-ttu-id="fb416-128">SharePoint-taxonomie : description</span><span class="sxs-lookup"><span data-stu-id="fb416-128">sharepoint-taxonomy:description</span></span>|<span data-ttu-id="fb416-129">SKOS : définition</span><span class="sxs-lookup"><span data-stu-id="fb416-129">skos:definition</span></span>|
|<span data-ttu-id="fb416-130">SharePoint : taxonomie : parent</span><span class="sxs-lookup"><span data-stu-id="fb416-130">sharepoint-taxonomy:parent</span></span>|<span data-ttu-id="fb416-131">SKOS : plus large</span><span class="sxs-lookup"><span data-stu-id="fb416-131">skos:broader</span></span>|
|<span data-ttu-id="fb416-132">SharePoint-taxonomie : enfant</span><span class="sxs-lookup"><span data-stu-id="fb416-132">sharepoint-taxonomy:child</span></span>|<span data-ttu-id="fb416-133">SKOS : plus étroit</span><span class="sxs-lookup"><span data-stu-id="fb416-133">skos:narrower</span></span>|

<span data-ttu-id="fb416-134">Le tableau suivant affiche les entités du vocabulaire de taxonomie SharePoint dérivé de [Owl](https://www.w3.org/TR/owl2-primer/).</span><span class="sxs-lookup"><span data-stu-id="fb416-134">The following table displays the entities of the SharePoint taxonomy vocabulary derived from [OWL](https://www.w3.org/TR/owl2-primer/).</span></span>

|<span data-ttu-id="fb416-135">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="fb416-135">SharePoint taxonomy vocabulary</span></span>|<span data-ttu-id="fb416-136">Dérivé de OWL</span><span class="sxs-lookup"><span data-stu-id="fb416-136">Derived from OWL</span></span>|
|:-----------------------------|:----------------------|
|<span data-ttu-id="fb416-137">SharePoint-taxonomie : isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="fb416-137">sharepoint-taxonomy:isAvailableForTagging</span></span>|<span data-ttu-id="fb416-138">owl:datatypeproperty</span><span class="sxs-lookup"><span data-stu-id="fb416-138">owl:datatypeproperty</span></span>|
|<span data-ttu-id="fb416-139">SharePoint-taxonomie : SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-139">sharepoint-taxonomy:SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="fb416-140">Owl : ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="fb416-140">owl:ObjectProperty</span></span>|
|<span data-ttu-id="fb416-141">SharePoint-taxonomie : LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-141">sharepoint-taxonomy:LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="fb416-142">Owl : ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="fb416-142">owl:ObjectProperty</span></span>|
|<span data-ttu-id="fb416-143">SharePoint-taxonomie : CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-143">sharepoint-taxonomy:CustomPropertyForTermSet</span></span>|<span data-ttu-id="fb416-144">Owl : ObjectProperty</span><span class="sxs-lookup"><span data-stu-id="fb416-144">owl:ObjectProperty</span></span>|

## <a name="sharepoint-taxonomy-vocabulary"></a><span data-ttu-id="fb416-145">Vocabulaire de taxonomie SharePoint</span><span class="sxs-lookup"><span data-stu-id="fb416-145">SharePoint taxonomy vocabulary</span></span>

<span data-ttu-id="fb416-146">Une taxonomie est un système de classification formel.</span><span class="sxs-lookup"><span data-stu-id="fb416-146">A taxonomy is a formal classification system.</span></span> <span data-ttu-id="fb416-147">Une taxonomie regroupe les mots, étiquettes et termes qui décrivent un article, puis réorganise les groupes dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="fb416-147">A taxonomy groups the words, labels, and terms that describe something, and then arranges the groups into a hierarchy.</span></span>

<span data-ttu-id="fb416-148">**SharePoint-taxonomie : terme**</span><span class="sxs-lookup"><span data-stu-id="fb416-148">**sharepoint-taxonomy:Term**</span></span>

<span data-ttu-id="fb416-149">Représente un terme ou un mot clé dans une hiérarchie de métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="fb416-149">Represents a Term or a Keyword in a managed metadata hierarchy.</span></span>

<span data-ttu-id="fb416-150">Un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) est l’unité atomique d’un [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore)SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fb416-150">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) is the atomic unit of a SharePoint [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore).</span></span> <span data-ttu-id="fb416-151">Chaque [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) appartient à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) qui appartient à un [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="fb416-151">Each [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) belongs to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) that belongs to a [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> 

<span data-ttu-id="fb416-152">La syntaxe de définition d’un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-152">The syntax to define a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) is as follows:</span></span>

```SKOS
ex:TermA    a    sharepoint-taxonomy:Term;
    sharepoint-taxonomy:inTermSet    ex:TermSetA;
    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA;
    sharepoint-taxonomy:child    ex:TermA1;
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharePoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="fb416-153">[Terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) obligatoire dans un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-153">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) compulsorily exists within a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-154">DefaultLabel est le nom du [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) tel qu’il apparaît dans la représentation visuelle.</span><span class="sxs-lookup"><span data-stu-id="fb416-154">DefaultLabel is the name of the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) as it appears in the visual representation.</span></span> <span data-ttu-id="fb416-155">Les champs requis pour la définition d’un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fb416-155">The required fields for defining a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) include:</span></span>

- <span data-ttu-id="fb416-156">SharePoint-taxonomie : defaultLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-156">sharepoint-taxonomy:defaultLabel</span></span>
- <span data-ttu-id="fb416-157">SharePoint-taxonomie : inTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-157">sharepoint-taxonomy:inTermSet</span></span>

<span data-ttu-id="fb416-158">Un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) peut :</span><span class="sxs-lookup"><span data-stu-id="fb416-158">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can:</span></span>

- <span data-ttu-id="fb416-159">Être hiérarchiquement lié à un autre [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) qui est fourni les deux [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) appartiennent au même [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-159">Be hierarchically related to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) that is provided both the [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) belong to the same [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="fb416-160">Avoir plusieurs [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term)enfants, mais un seul [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term)parent.</span><span class="sxs-lookup"><span data-stu-id="fb416-160">Have multiple child [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), but only a single parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>
- <span data-ttu-id="fb416-161">N’a pas de [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) parent défini, s’il s’agit d’un TopLevelTermOf un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-161">Not have a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) defined, if it is a topLevelTermOf a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>
- <span data-ttu-id="fb416-162">Avoir un defaultLabel, par [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) de travail.</span><span class="sxs-lookup"><span data-stu-id="fb416-162">Have one defaultLabel, per [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>
- <span data-ttu-id="fb416-163">N’existe pas s’il ne contient pas de [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term)parent et s’il n’est pas TopLevelTermOf un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-163">Not exist if it neither contains a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), nor is the topLevelTermOf a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> 
- <span data-ttu-id="fb416-164">Ont seulement un defaultLabel unique au même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="fb416-164">Have only a unique defaultLabel in the same hierarchical level.</span></span>

<span data-ttu-id="fb416-165">**SharePoint-taxonomie : TermSet**</span><span class="sxs-lookup"><span data-stu-id="fb416-165">**sharepoint-taxonomy:TermSet**</span></span>

<span data-ttu-id="fb416-166">Représente un ensemble hiérarchique ou plat d’objets Term appelés « TermSet ».</span><span class="sxs-lookup"><span data-stu-id="fb416-166">Represents a hierarchical or flat set of Term objects known as a "TermSet".</span></span>

<span data-ttu-id="fb416-167">Comme son nom l’indique, TermSet est un ensemble de [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-167">As the name suggests, TermSet is a set of [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="fb416-168">Un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) doit appartenir à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-168">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) must belong to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-169">Aucun [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut être indépendant.</span><span class="sxs-lookup"><span data-stu-id="fb416-169">No [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can exist independently.</span></span> 

<span data-ttu-id="fb416-170">La syntaxe de définition d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-170">The syntax to define a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

```SKOS
ex:TermSetA    a    sharepoint-taxonomy:TermSet;
    sharepoint-taxonomy:termSetName    “TermSet A";
    sharepoint-taxonomy:isAvailableForTagging    “true”^^xsd:Boolean;
    sharepoint-taxonomy:hasTopLevelTerm    Ex:Term A.
```

<span data-ttu-id="fb416-171">Les [TermSets](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) sont regroupés de manière logique dans [TermGroups](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span><span class="sxs-lookup"><span data-stu-id="fb416-171">[TermSets](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) are logically grouped together in [TermGroups](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group).</span></span> <span data-ttu-id="fb416-172">Le champ obligatoire pour la définition d’une [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est le suivant :</span><span class="sxs-lookup"><span data-stu-id="fb416-172">The required field for defining a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) is:</span></span>

- <span data-ttu-id="fb416-173">SharePoint-taxonomie : termSetName</span><span class="sxs-lookup"><span data-stu-id="fb416-173">sharepoint-taxonomy:termSetName</span></span>

<span data-ttu-id="fb416-174">Dans le cas de l’termSetName fourni n’est pas unique au sein de l' [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group), mis ajoute un numéro à la fin du nom pour maintenir l’unicité de termSetName (s).</span><span class="sxs-lookup"><span data-stu-id="fb416-174">In the case of the termSetName provided is not unique within the [TermGroup](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.group), SharPoint appends a number at the end of the name to maintain the uniqueness of termSetName(s).</span></span>

<span data-ttu-id="fb416-175">**SharePoint-taxonomie : hasTopLevelTerm**</span><span class="sxs-lookup"><span data-stu-id="fb416-175">**sharepoint-taxonomy:hasTopLevelTerm**</span></span>

<span data-ttu-id="fb416-176">SharePoint utilise cette propriété pour mapper le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) le plus élevé dans le [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), qui est le point d’entrée de la hiérarchie des [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) dans un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-176">SharePoint uses this property to map the top most [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in the [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), which is the entry point to the hierarchy of [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-177">Il s’agit d’une relation inverse avec SharePoint-taxonomique : topLevelTermOf.</span><span class="sxs-lookup"><span data-stu-id="fb416-177">This is an inverse relation to sharepoint-taxonomy:topLevelTermOf.</span></span> 

<span data-ttu-id="fb416-178">La syntaxe de définition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-178">The syntax to define this is:</span></span>

```SKOS
ex:TermSetA    sharepoint-taxonomy:hasTopLevelTerm    ex:TermA.
```

>[!NOTE]
> <span data-ttu-id="fb416-179">Vous ne pouvez pas définir le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) de niveau supérieur d’un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term)parent.</span><span class="sxs-lookup"><span data-stu-id="fb416-179">You cannot define the top level [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) of a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="fb416-180">**SharePoint-taxonomie : topLevelTermOf**</span><span class="sxs-lookup"><span data-stu-id="fb416-180">**sharepoint-taxonomy:topLevelTermOf**</span></span>

<span data-ttu-id="fb416-181">SharePoint : taxonomie : topLevelTermOf est l’inverse de la taxonomie SharePoint : hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-181">Sharepoint-taxonomy:topLevelTermOf is the inverse of sharepoint-taxonomy:hasTopLevelTerm</span></span>

<span data-ttu-id="fb416-182">La syntaxe de définition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-182">The syntax to define this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:topLevelTermOf    ex:TermSetA.
```

<span data-ttu-id="fb416-183">**SharePoint-taxonomie : inTermSet**</span><span class="sxs-lookup"><span data-stu-id="fb416-183">**sharepoint-taxonomy:inTermSet**</span></span>

<span data-ttu-id="fb416-184">Utilisez-le pour mapper un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-184">Use this to map a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-185">Un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ne peut exister que dans un seul [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-185">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) can only exist in a single [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-186">SharePoint requiert cette propriété lors [de la définition d’un terme](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span><span class="sxs-lookup"><span data-stu-id="fb416-186">SharePoint requires this property when [defining a term](https://github.com/MicrosoftDocs/microsoft-365-docs-pr/blob/3a3cd54dd076b18bdff1d43b3e342897f8704c23/microsoft-365/contentunderstanding/skos-format-reference.md#term).</span></span>

## <a name="required-labels"></a><span data-ttu-id="fb416-187">Étiquettes requises</span><span class="sxs-lookup"><span data-stu-id="fb416-187">Required labels</span></span>

<span data-ttu-id="fb416-188">Votre organisation peut souhaiter effectuer une planification soignée avant de commencer à utiliser des métadonnées gérées.</span><span class="sxs-lookup"><span data-stu-id="fb416-188">Your organization may want to do careful planning before you start to use managed metadata.</span></span> <span data-ttu-id="fb416-189">La planification que vous devez effectuer dépend de la façon dont votre taxonomie est formalisée.</span><span class="sxs-lookup"><span data-stu-id="fb416-189">The amount of planning that you must do depends on how formal your taxonomy is.</span></span> <span data-ttu-id="fb416-190">Elle dépend également de la proportion de contrôle que vous souhaitez imposer sur les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="fb416-190">It also depends on how much control that you want to impose on metadata.</span></span> <span data-ttu-id="fb416-191">À chaque niveau de la hiérarchie, vous devez configurer le lables requis pour un terme ou TermSet.</span><span class="sxs-lookup"><span data-stu-id="fb416-191">At each level of the hierarchy, you need to configure required lables for a Term or TermSet.</span></span>

<span data-ttu-id="fb416-192">Un terme peut avoir une ou plusieurs étiquettes dans la langue par défaut, et zéro, une ou plusieurs étiquettes dans la langue non définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb416-192">A Term can have one or more labels in the default language, and zero or more labels in the non-default language.</span></span> <span data-ttu-id="fb416-193">Si le terme contient des étiquettes dans une langue, l’une des étiquettes doit être l’étiquette par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb416-193">If the term has labels in a language, one of the labels must be the default label.</span></span>

<span data-ttu-id="fb416-194">**SharePoint-taxonomie : defaultLabel**</span><span class="sxs-lookup"><span data-stu-id="fb416-194">**sharepoint-taxonomy:defaultLabel**</span></span>

<span data-ttu-id="fb416-195">Utilisez cette étiquette lexicale par défaut pour un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) qui est un paramètre obligatoire pour un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-195">Use this default lexical label for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) that is a required parameter for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="fb416-196">Utilisez pour représenter visuellement le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-196">Use to visually representing the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="fb416-197">La syntaxe de définition d’un defaultLabel est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-197">The syntax to define a defaultLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:defaultLabel    “Term A”@en-us.
```

<span data-ttu-id="fb416-198">La defaultLabel contient deux parties : la chaîne et la balise de langue.</span><span class="sxs-lookup"><span data-stu-id="fb416-198">The defaultLabel contains two parts to it – the string and the language tag.</span></span> <span data-ttu-id="fb416-199">La langue doit être l’une des langues de travail [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) .</span><span class="sxs-lookup"><span data-stu-id="fb416-199">The language must be one of the [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working languages.</span></span> <span data-ttu-id="fb416-200">Le defaultLabel doit être unique pour tous les [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) du même [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), au même niveau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="fb416-200">The defaultLabel must be unique for all [Terms](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) in the same [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), at the same hierarchical level.</span></span>

<span data-ttu-id="fb416-201">**SharePoint-taxonomie : termSetName**</span><span class="sxs-lookup"><span data-stu-id="fb416-201">**sharepoint-taxonomy:termSetName**</span></span>

<span data-ttu-id="fb416-202">Obtient et définit le nom de l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="fb416-202">Gets and sets the name for the current TermSet object.</span></span>

<span data-ttu-id="fb416-203">Cette étiquette lexicale pour un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), dans une langue de travail [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) .</span><span class="sxs-lookup"><span data-stu-id="fb416-203">This the lexical label for a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span> <span data-ttu-id="fb416-204">Il s’agit d’un paramètre obligatoire pour un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-204">This is a required parameter for a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-205">Permet de représenter visuellement un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-205">Use to visually representing a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span>

<span data-ttu-id="fb416-206">La syntaxe de définition d’un termSetName est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-206">The syntax to define a termSetName is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:TermSetName    “Term Set A”@en-us.
```

<span data-ttu-id="fb416-207">**SharePoint-taxonomie : propertyName**</span><span class="sxs-lookup"><span data-stu-id="fb416-207">**sharepoint-taxonomy:propertyName**</span></span>

<span data-ttu-id="fb416-208">Obtient et définit le nom de la propriété pour l’objet TermSet actuel.</span><span class="sxs-lookup"><span data-stu-id="fb416-208">Gets and sets the property name for the current TermSet object.</span></span>

<span data-ttu-id="fb416-209">Il s’agit de l’étiquette lexicale pour une taxonomie SharePoint : SharedCustomPropertyForTerm, SharePoint-taxonomique : LocalCustomPropertyForTerm et SharePoint-taxonomique : CustomPropertyForTermSet dans une langue de travail [termes](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) .</span><span class="sxs-lookup"><span data-stu-id="fb416-209">This is the lexical label for a sharepoint-taxonomy:SharedCustomPropertyForTerm, sharepoint-taxonomy:LocalCustomPropertyForTerm and sharepoint-taxonomy:CustomPropertyForTermSet in a [TermStore](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termstore) working language.</span></span>

<span data-ttu-id="fb416-210">La taxonomie SharePoint-taxonomique : propertyName est traitée comme la clé de CustomProperty.</span><span class="sxs-lookup"><span data-stu-id="fb416-210">The sharepoint-taxonomy:propertyName is treated as the key of the CustomProperty.</span></span>

<span data-ttu-id="fb416-211">La syntaxe de définition d’un propetyName est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-211">The syntax to define a propetyName is:</span></span>

```SKOS
ex:SharedCustomProperty1    sharepoint-taxonomy:propertyName    “Shared Custom Property Key 1”@en-us.
```

## <a name="optional-labels"></a><span data-ttu-id="fb416-212">Étiquettes facultatives</span><span class="sxs-lookup"><span data-stu-id="fb416-212">Optional labels</span></span>

<span data-ttu-id="fb416-213">Vous pouvez également ajouter des étiquettes facultatives à votre taxonomie.</span><span class="sxs-lookup"><span data-stu-id="fb416-213">You can also add optional labels to your taxonomy.</span></span>

<span data-ttu-id="fb416-214">**SharePoint-taxonomie : otherLabel**</span><span class="sxs-lookup"><span data-stu-id="fb416-214">**sharepoint-taxonomy:otherLabel**</span></span>

<span data-ttu-id="fb416-215">Il s’agit de l’étiquette lexicale de remplacement pour un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-215">This is the alternate lexical label for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="fb416-216">La syntaxe de définition d’une otherLabel est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-216">The syntax to define an otherLabel is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:otherLabel    “Term A”@en-us.
```

## <a name="semantic-relationships"></a><span data-ttu-id="fb416-217">Relations sémantiques</span><span class="sxs-lookup"><span data-stu-id="fb416-217">Semantic relationships</span></span>

<span data-ttu-id="fb416-218">Les taxonomies ont une relation associative hiérarchique et parfois un simple « terme apparenté », mais certains ont des relations de « sémantique » ou de création personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fb416-218">Taxonomies have hierarchical and sometimes a simple “related term” associative relationship, but some have "semantic relationships" or custom-created relationships.</span></span> 

<span data-ttu-id="fb416-219">**SharePoint : taxonomie : parent**</span><span class="sxs-lookup"><span data-stu-id="fb416-219">**sharepoint-taxonomy:parent**</span></span>

<span data-ttu-id="fb416-220">Cela associe hiérarchiquement un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-220">This hierarchically relates a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> <span data-ttu-id="fb416-221">Un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) peut être un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) de niveau supérieur d’un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), mais si ce n’est pas le cas, il ne doit pas avoir de [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term)parent.</span><span class="sxs-lookup"><span data-stu-id="fb416-221">A [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) could be a top level [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) of a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), but in case it doesn’t it must have a parent [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span> 

<span data-ttu-id="fb416-222">La syntaxe de définition d’un parent est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-222">The syntax to define a parent is:</span></span>

```SKOS
ex:TermA1    sharepoint-taxonomy:parent    ex:TermA.
```

<span data-ttu-id="fb416-223">Cela signifie que TermA1 a un terme parent.</span><span class="sxs-lookup"><span data-stu-id="fb416-223">This means that TermA1 has parent TermA.</span></span> <span data-ttu-id="fb416-224">Inversement, cela signifie également que TermA1 est l’enfant de Terma.</span><span class="sxs-lookup"><span data-stu-id="fb416-224">Inversely it also means that TermA1 is the child of TermA.</span></span> <span data-ttu-id="fb416-225">La relation parent-enfant est une relation inversible.</span><span class="sxs-lookup"><span data-stu-id="fb416-225">Parent-child relationship is an inversible relationship.</span></span>

<span data-ttu-id="fb416-226">**SharePoint-taxonomie : enfant**</span><span class="sxs-lookup"><span data-stu-id="fb416-226">**sharepoint-taxonomy:child**</span></span>

<span data-ttu-id="fb416-227">L’objet contient une ou plusieurs instances TermSet enfants, qui sont accessibles par le biais de la propriété TermSets.</span><span class="sxs-lookup"><span data-stu-id="fb416-227">The object contains one or more child TermSet instances, and these can be accessed through the TermSets property.</span></span> <span data-ttu-id="fb416-228">Cette classe fournit également des méthodes pour créer des objets TermSet enfants.</span><span class="sxs-lookup"><span data-stu-id="fb416-228">This class also provides methods for creating new child TermSet objects.</span></span> <span data-ttu-id="fb416-229">Les autorisations permettant de modifier le terme enfant et les instances TermSet sont spécifiées dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="fb416-229">Permissions for editing child Term and TermSet instances is specified on the group.</span></span> 

<span data-ttu-id="fb416-230">Cela associe hiérarchiquement un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) à un autre [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span><span class="sxs-lookup"><span data-stu-id="fb416-230">This hierarchically relates a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) to another [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term).</span></span>

<span data-ttu-id="fb416-231">La syntaxe de définition d’un enfant est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-231">The syntax to define a child is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:child    ex:TermA1.
```

<span data-ttu-id="fb416-232">Cela signifie que Terma a un enfant TermA1.</span><span class="sxs-lookup"><span data-stu-id="fb416-232">This means that TermA has child TermA1.</span></span> <span data-ttu-id="fb416-233">Inversement, cela signifie également que Terma est le parent de TermA1 Parent-Child Relationship est une relation inversible.</span><span class="sxs-lookup"><span data-stu-id="fb416-233">Inversely it also means that TermA is the parent of TermA1 parent-child relationship is an inversible relationship.</span></span>

## <a name="documentation-notes"></a><span data-ttu-id="fb416-234">Notes de documentation</span><span class="sxs-lookup"><span data-stu-id="fb416-234">Documentation notes</span></span>

<span data-ttu-id="fb416-235">Cette section traite de la taxonomie détaillée dans l’espace de noms Microsoft. SharePoint. taxonomique.</span><span class="sxs-lookup"><span data-stu-id="fb416-235">This section discusses the taxonomy detailed in the Microsoft.SharePoint.Taxonomy Namespace.</span></span>

<span data-ttu-id="fb416-236">**SharePoint-taxonomie : description**</span><span class="sxs-lookup"><span data-stu-id="fb416-236">**sharepoint-taxonomy:description**</span></span>

<span data-ttu-id="fb416-237">Il s’agit d’une explication détaillée de toute entité de vocabulaire de [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) .</span><span class="sxs-lookup"><span data-stu-id="fb416-237">This is a detailed explanation of any [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) vocabulary entity.</span></span> 

<span data-ttu-id="fb416-238">La syntaxe permettant d’ajouter une description est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-238">The syntax to add a description is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:description    “Term A is the top level term of TermSetA”@en-us.
```

## <a name="custom-properties"></a><span data-ttu-id="fb416-239">Propriétés personnalisées</span><span class="sxs-lookup"><span data-stu-id="fb416-239">Custom properties</span></span>

<span data-ttu-id="fb416-240">Obtient la collection d’objets Property personnalisés pour l’objet Term actuel à partir du dictionnaire en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fb416-240">Gets the collection of custom property objects for the current Term object from the read-only dictionary.</span></span>

<span data-ttu-id="fb416-241">Les propriétés personnalisées sont des paires clé-valeur qui peuvent être définies pour un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), afin de mieux décrire le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span><span class="sxs-lookup"><span data-stu-id="fb416-241">Custom Properties are key-values pairs that can be defined for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset), to further the description of the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset).</span></span> <span data-ttu-id="fb416-242">SharePoint spécifie la clé de la propriété personnalisée avec l’aide de propertyName.</span><span class="sxs-lookup"><span data-stu-id="fb416-242">SharePoint specifies the key of the custom property with the help of propertyName.</span></span>

<span data-ttu-id="fb416-243">**SharePoint-taxonomie : CustomPropertyForTermSet**</span><span class="sxs-lookup"><span data-stu-id="fb416-243">**sharepoint-taxonomy:CustomPropertyForTermSet**</span></span>

<span data-ttu-id="fb416-244">La syntaxe de définition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-244">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp1    rdf:type    sharepoint-taxonomy:CustomPropertyForTermSet;
    sharepoint-taxonomy:propertyName “Colour”.

ex:TermSetA    ex:CustomProp1    “Red”@en-us.
```

<span data-ttu-id="fb416-245">**SharePoint-taxonomie : SharedCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="fb416-245">**sharepoint-taxonomy:SharedCustomPropertyForTerm**</span></span>

<span data-ttu-id="fb416-246">Si la propriété personnalisée d’un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) doit être exécutée avec le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous SharedCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="fb416-246">If the custom property for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) needs to be carried along with the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to be define it under SharedCustomPropertyForTerm.</span></span>

<span data-ttu-id="fb416-247">La syntaxe de définition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-247">The syntax to define this is:</span></span>

``` SKOS
ex:CustomProp2    rdf:type sharepoint-taxonomy:SharedCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “Length”.

ex:TermA    ex:CustomProp2    “5 cm”@en-us.
```
<span data-ttu-id="fb416-248">**SharePoint-taxonomie : LocalCustomPropertyForTerm**</span><span class="sxs-lookup"><span data-stu-id="fb416-248">**sharepoint-taxonomy:LocalCustomPropertyForTerm**</span></span>

<span data-ttu-id="fb416-249">Si la propriété personnalisée d’un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ne doit pas être exécutée avec le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), lorsque vous réutilisez le [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ailleurs, vous devez le définir sous LocalCustomPropertyForTerm.</span><span class="sxs-lookup"><span data-stu-id="fb416-249">If the custom property for a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) does not need to be carried along with the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term), when you reuse the [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) somewhere else, then you need to define it under LocalCustomPropertyForTerm.</span></span>

<span data-ttu-id="fb416-250">La syntaxe de définition est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-250">The syntax to define this is:</span></span>

```SKOS
ex:CustomProp3    rdf:type sharepoint-taxonomy:LocalCustomPropertyForTerm;
    sharepoint-taxonomy:propertyName “width”.

ex:TermA    ex:CustomProp3    “5 cm”@en-us.
```

## <a name="data-properties"></a><span data-ttu-id="fb416-251">Propriétés de données</span><span class="sxs-lookup"><span data-stu-id="fb416-251">Data properties</span></span>

<span data-ttu-id="fb416-252">À chaque niveau de la hiérarchie, vous pouvez configurer des propriétés de données spécifiques pour un terme ou TermSet.</span><span class="sxs-lookup"><span data-stu-id="fb416-252">At each level of the hierarchy, you can configure specific data properties for a Term or TermSet.</span></span>

<span data-ttu-id="fb416-253">**SharePoint-taxonomie : isAvailableForTagging**</span><span class="sxs-lookup"><span data-stu-id="fb416-253">**sharepoint-taxonomy:isAvailableForTagging**</span></span>

<span data-ttu-id="fb416-254">Utilisez cette pour spécifier si un [terme](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) ou un [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) est disponible dans les listes et les bibliothèques SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fb416-254">Use this to specify if a [Term](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.term) or a [TermSet](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy.termset) available in SharePoint Lists and Libraries.</span></span>  

<span data-ttu-id="fb416-255">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb416-255">The syntax for this is:</span></span>

```SKOS
ex:TermA    sharepoint-taxonomy:isAvailableForTagging     "true"^^xsd:Boolean;
```

## <a name="domain-and-range"></a><span data-ttu-id="fb416-256">Domaine et plage</span><span class="sxs-lookup"><span data-stu-id="fb416-256">Domain and range</span></span>

<span data-ttu-id="fb416-257">Le tableau ci-dessous décrit le domaine et la plage de vocabulaire de taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fb416-257">The table below describes the domain and range of SharePoint taxonomy vocabulary.</span></span>

|<span data-ttu-id="fb416-258">Prédicats/verbe</span><span class="sxs-lookup"><span data-stu-id="fb416-258">Predicates/verb</span></span>|<span data-ttu-id="fb416-259">Signification</span><span class="sxs-lookup"><span data-stu-id="fb416-259">Meaning</span></span>|<span data-ttu-id="fb416-260">Domaine</span><span class="sxs-lookup"><span data-stu-id="fb416-260">Domain</span></span>|<span data-ttu-id="fb416-261">Plage</span><span class="sxs-lookup"><span data-stu-id="fb416-261">Range</span></span>|
|:--------------|:------|:-----|:----|
<span data-ttu-id="fb416-262">inTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-262">inTermSet</span></span>|<span data-ttu-id="fb416-263">Dans l’ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="fb416-263">In term set</span></span>|<span data-ttu-id="fb416-264">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-264">Term</span></span>|<span data-ttu-id="fb416-265">Ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="fb416-265">Term Set</span></span>|
<span data-ttu-id="fb416-266">inTermGroup</span><span class="sxs-lookup"><span data-stu-id="fb416-266">inTermGroup</span></span>|<span data-ttu-id="fb416-267">Dans le groupe de termes</span><span class="sxs-lookup"><span data-stu-id="fb416-267">In term group</span></span>|<span data-ttu-id="fb416-268">TermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-268">TermSet</span></span>|<span data-ttu-id="fb416-269">TermGroup</span><span class="sxs-lookup"><span data-stu-id="fb416-269">TermGroup</span></span>|
<span data-ttu-id="fb416-270">topLevelTermOf</span><span class="sxs-lookup"><span data-stu-id="fb416-270">topLevelTermOf</span></span>|<span data-ttu-id="fb416-271">Est le terme de niveau supérieur de</span><span class="sxs-lookup"><span data-stu-id="fb416-271">Is Top Level Term Of</span></span>|<span data-ttu-id="fb416-272">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-272">Term</span></span>|<span data-ttu-id="fb416-273">TermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-273">TermSet</span></span>|
<span data-ttu-id="fb416-274">hasTopLevelTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-274">hasTopLevelTerm</span></span>|<span data-ttu-id="fb416-275">Est un terme de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="fb416-275">Has top level term</span></span>|<span data-ttu-id="fb416-276">Ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="fb416-276">Term Set</span></span>|<span data-ttu-id="fb416-277">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-277">Term</span></span>|
<span data-ttu-id="fb416-278">termSetName</span><span class="sxs-lookup"><span data-stu-id="fb416-278">termSetName</span></span>|<span data-ttu-id="fb416-279">L’ensemble de termes a le nom</span><span class="sxs-lookup"><span data-stu-id="fb416-279">Term set has Name</span></span>|<span data-ttu-id="fb416-280">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-280">Term</span></span>|<span data-ttu-id="fb416-281">Littéral brut</span><span class="sxs-lookup"><span data-stu-id="fb416-281">Plain literal</span></span>|
<span data-ttu-id="fb416-282">defaultLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-282">defaultLabel</span></span>|<span data-ttu-id="fb416-283">Le terme a une étiquette par défaut</span><span class="sxs-lookup"><span data-stu-id="fb416-283">Term has default label</span></span>|<span data-ttu-id="fb416-284">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-284">Term</span></span>|<span data-ttu-id="fb416-285">Littéral brut</span><span class="sxs-lookup"><span data-stu-id="fb416-285">Plain literal</span></span>|
<span data-ttu-id="fb416-286">otherLabel</span><span class="sxs-lookup"><span data-stu-id="fb416-286">otherLabel</span></span>|<span data-ttu-id="fb416-287">Le terme a une autre étiquette</span><span class="sxs-lookup"><span data-stu-id="fb416-287">Term has other label</span></span>|<span data-ttu-id="fb416-288">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-288">Term</span></span>|<span data-ttu-id="fb416-289">Littéral brut</span><span class="sxs-lookup"><span data-stu-id="fb416-289">Plain literal</span></span>|
<span data-ttu-id="fb416-290">propertyName</span><span class="sxs-lookup"><span data-stu-id="fb416-290">propertyName</span></span>|<span data-ttu-id="fb416-291">Possède une étiquette de propriété</span><span class="sxs-lookup"><span data-stu-id="fb416-291">Has Property Label</span></span>|<span data-ttu-id="fb416-292">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-292">SharedCustomPropertyForTerm, LocalCustomPropertyForTerm, CustomPropertyForTermSet</span></span> |<span data-ttu-id="fb416-293">Boolean, String, Integer, Decimal, double</span><span class="sxs-lookup"><span data-stu-id="fb416-293">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="fb416-294">description</span><span class="sxs-lookup"><span data-stu-id="fb416-294">description</span></span>|<span data-ttu-id="fb416-295">Comporte une description</span><span class="sxs-lookup"><span data-stu-id="fb416-295">Has Description</span></span>|<span data-ttu-id="fb416-296">Tous</span><span class="sxs-lookup"><span data-stu-id="fb416-296">All</span></span>|<span data-ttu-id="fb416-297">Littéral brut</span><span class="sxs-lookup"><span data-stu-id="fb416-297">Plain literal</span></span>|
|<span data-ttu-id="fb416-298">parent</span><span class="sxs-lookup"><span data-stu-id="fb416-298">parent</span></span>|<span data-ttu-id="fb416-299">A un parent</span><span class="sxs-lookup"><span data-stu-id="fb416-299">Has parent</span></span>|<span data-ttu-id="fb416-300">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-300">Term</span></span>|<span data-ttu-id="fb416-301">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-301">Term</span></span>|
|<span data-ttu-id="fb416-302">derniers</span><span class="sxs-lookup"><span data-stu-id="fb416-302">child</span></span>|<span data-ttu-id="fb416-303">A un enfant</span><span class="sxs-lookup"><span data-stu-id="fb416-303">Has Child</span></span>|<span data-ttu-id="fb416-304">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-304">Term</span></span>|<span data-ttu-id="fb416-305">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-305">Term</span></span>|
|<span data-ttu-id="fb416-306">isAvailableForTagging</span><span class="sxs-lookup"><span data-stu-id="fb416-306">isAvailableForTagging</span></span>|<span data-ttu-id="fb416-307">Est disponible pour le marquage</span><span class="sxs-lookup"><span data-stu-id="fb416-307">Is available for tagging</span></span>|<span data-ttu-id="fb416-308">Terme, ensemble de termes</span><span class="sxs-lookup"><span data-stu-id="fb416-308">Term, Term Set</span></span>|<span data-ttu-id="fb416-309">Boolean</span><span class="sxs-lookup"><span data-stu-id="fb416-309">Boolean</span></span>|
|<span data-ttu-id="fb416-310">SharedCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-310">SharedCustomPropertyForTerm</span></span>|<span data-ttu-id="fb416-311">Possède une propriété personnalisée partagée</span><span class="sxs-lookup"><span data-stu-id="fb416-311">Has shared custom property</span></span>|<span data-ttu-id="fb416-312">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-312">Term</span></span>|<span data-ttu-id="fb416-313">Boolean, String, Integer, Decimal, double</span><span class="sxs-lookup"><span data-stu-id="fb416-313">Boolean, string, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="fb416-314">LocalCustomPropertyForTerm</span><span class="sxs-lookup"><span data-stu-id="fb416-314">LocalCustomPropertyForTerm</span></span>|<span data-ttu-id="fb416-315">Possède une propriété personnalisée locale</span><span class="sxs-lookup"><span data-stu-id="fb416-315">Has local custom property</span></span>|<span data-ttu-id="fb416-316">Term</span><span class="sxs-lookup"><span data-stu-id="fb416-316">Term</span></span>|<span data-ttu-id="fb416-317">Boolean, String, Integer, Decimal, double</span><span class="sxs-lookup"><span data-stu-id="fb416-317">Boolean, String, Integer, Decimal, Double</span></span>|
|<span data-ttu-id="fb416-318">CustomPropertyForTermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-318">CustomPropertyForTermSet</span></span>|<span data-ttu-id="fb416-319">Possède une propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="fb416-319">Has Custom Property</span></span>|<span data-ttu-id="fb416-320">TermSet</span><span class="sxs-lookup"><span data-stu-id="fb416-320">TermSet</span></span>|<span data-ttu-id="fb416-321">Boolean, String, Integer, Decimal, double</span><span class="sxs-lookup"><span data-stu-id="fb416-321">Boolean, String, Integer, Decimal, Double</span></span>|

<span data-ttu-id="fb416-322">[SKOS](https://www.w3.org/TR/skos-primer/) les scénarios valides que la [taxonomie SharePoint](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) n’autorise pas :</span><span class="sxs-lookup"><span data-stu-id="fb416-322">[SKOS](https://www.w3.org/TR/skos-primer/) valid scenarios that [SharePoint taxonomy](https://docs.microsoft.com/dotnet/api/microsoft.sharepoint.taxonomy) does not allow:</span></span>

- <span data-ttu-id="fb416-323">Redondance hiérarchique : un concept [SKOS](https://www.w3.org/TR/skos-primer/) peut être associé à plusieurs concepts plus larges en même temps, mais une taxonomie SharePoint : le terme ne peut avoir qu’une seule taxonomie SharePoint : le parent, ainsi que la dépendance cyclique, des termes ne sont pas non plus autorisés.</span><span class="sxs-lookup"><span data-stu-id="fb416-323">Hierarchical redundancy - A [SKOS](https://www.w3.org/TR/skos-primer/) concept can be attached to several broader concepts at the same time, but a sharepoint-taxonomy:Term can have only one sharepoint-taxonomy:parent, hence cyclic dependency, of Terms is also not allowed.</span></span>
- <span data-ttu-id="fb416-324">Les termes orphelins ne sont pas autorisés dans la taxonomie SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fb416-324">Orphaned terms are not allowed in SharePoint taxonomy.</span></span> <span data-ttu-id="fb416-325">Chaque taxonomie SharePoint-taxonomique : term doit disposer d’une taxonomie SharePoint : parent ou il doit s’agir de la taxonomie SharePoint : topLevelTermOf a TermSet.</span><span class="sxs-lookup"><span data-stu-id="fb416-325">Every sharepoint-taxonomy:Term should either have a sharepoint-taxonomy:parent or it should be the sharepoint-taxonomy:topLevelTermOf a TermSet.</span></span>
- <span data-ttu-id="fb416-326">La taxonomie SharePoint ne prend pas en charge les relations associatives.</span><span class="sxs-lookup"><span data-stu-id="fb416-326">SharePoint taxonomy does not support associative relations.</span></span>
- <span data-ttu-id="fb416-327">La taxonomie SharePoint n’autorise que 2 types de relations hiérarchiques – SharePoint-taxonomie : parent et SharePoint-taxonomie : enfant.</span><span class="sxs-lookup"><span data-stu-id="fb416-327">SharePoint taxonomy only allows 2 types of Hierarchical relations – sharepoint-taxonomy:parent and sharepoint-Taxonomy:child.</span></span> 
- <span data-ttu-id="fb416-328">Contrairement à [SKOS](https://www.w3.org/TR/skos-primer/) , la relation hiérarchique dans le vocabulaire de taxonomie SharePoint ne peut être établie qu’avec des termes appartenant à la même TermSet.</span><span class="sxs-lookup"><span data-stu-id="fb416-328">Unlike [SKOS](https://www.w3.org/TR/skos-primer/) the hierarchical relationship in SharePoint taxonomy vocabulary, can only be established with Terms within the same TermSet.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb416-329">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb416-329">See also</span></span>

[<span data-ttu-id="fb416-330">Importer un ensemble de termes à l’aide d’un format basé sur SKOS</span><span class="sxs-lookup"><span data-stu-id="fb416-330">Import a term set using a SKOS-based format</span></span>](import-term-set-skos.md)

