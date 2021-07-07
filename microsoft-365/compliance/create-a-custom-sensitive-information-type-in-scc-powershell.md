---
title: Créer un type d’informations sensibles personnalisé à l’aide de PowerShell
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez la création et l’importation d’un type d’informations sensibles personnalisé des stratégies dans le centre de conformité.
ms.openlocfilehash: ab89104804fd1af781ca30ed8893bed60cd29e47
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322256"
---
# <a name="create-a-custom-sensitive-information-type-using-powershell"></a><span data-ttu-id="b72b7-103">Créer un type d’informations sensibles personnalisé à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="b72b7-103">Create a custom sensitive information type using PowerShell</span></span>

<span data-ttu-id="b72b7-104">Cette rubrique vous montre comment utiliser PowerShell pour créer une *Règle de package* qui définit vos propres [Types d’informations sensibles](sensitive-information-type-entity-definitions.md) personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b72b7-104">This topic shows you how to use PowerShell to create an XML *rule package* file that defines your own custom [sensitive information types](sensitive-information-type-entity-definitions.md).</span></span> <span data-ttu-id="b72b7-105">Vous devez savoir comment créer une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="b72b7-105">You need to know how to create a regular expression.</span></span> <span data-ttu-id="b72b7-106">À titre d’exemple, cette rubrique permet de créer un type d’informations sensibles personnalisé qui identifie un ID d’employé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-106">As an example, this topic creates a custom sensitive information type that identifies an employee ID.</span></span> <span data-ttu-id="b72b7-107">Vous pouvez utiliser cet exemple de code XML comme point de départ de votre propre fichier XML.</span><span class="sxs-lookup"><span data-stu-id="b72b7-107">You can use this example XML as a starting point for your own XML file.</span></span> <span data-ttu-id="b72b7-108">Si vous découvrez les types d’informations sensibles pour la première fois, consultez [En savoir plus sur les types d’informations sensibles](sensitive-information-type-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="b72b7-108">If you are new to sensitive information types, see [Learn about sensitive information types](sensitive-information-type-learn-about.md).</span></span>

<span data-ttu-id="b72b7-p102">Après avoir créé un fichier XML bien formé, vous pouvez le charger sur Microsoft 365 à l’aide de Microsoft 365 PowerShell. Ensuite, vous pouvez utiliser votre type d’informations sensibles personnalisé dans vos stratégies et vérifier qu’il détecte bien les informations sensibles comme souhaité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p102">After you've created a well-formed XML file, you can upload it to Microsoft 365 by using Microsoft 365 PowerShell. Then you're ready to use your custom sensitive information type in your policies and test that it's detecting the sensitive information as you intended.</span></span>

> [!NOTE]
> <span data-ttu-id="b72b7-111">Si vous n’avez pas besoin du contrôle parfait offert par PowerShell, vous pouvez créer des types d’informations sensibles personnalisés dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-111">If you don't need the fine grained control that PowerShell provides, you can create custom sensitive information types in the Compliance center.</span></span> <span data-ttu-id="b72b7-112">Pour en savoir plus, consulter [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="b72b7-112">For more information, see [Create a custom sensitive information type](create-a-custom-sensitive-information-type.md).</span></span>

## <a name="important-disclaimer"></a><span data-ttu-id="b72b7-113">Clause d’exclusion de responsabilité importante</span><span class="sxs-lookup"><span data-stu-id="b72b7-113">Important disclaimer</span></span>

<span data-ttu-id="b72b7-p104"> En raison des différences dans les environnements client et les exigences de correspondance de contenu, le support Microsoft ne peut pas fournir de définitions de correspondance de contenu personnalisée, par exemple, en définissant des classifications personnalisées ou des modèles d’expressions régulières (« RegEx »). Pour le développement, le test et le débogage liés à la correspondance de contenu personnalisée, les clients Microsoft 365 doivent s’appuyer sur leurs ressources informatiques internes ou recourir à une ressource de conseil externe telle que Microsoft Consulting Services (MCS). Les ingénieurs du support peuvent fournir une assistance limitée pour la fonctionnalité, mais ils ne peuvent pas fournir de garanties en matière d’adéquation entre les obligations ou exigences d’un client et le développement de correspondances de contenu personnalisées. Dans le cadre de l’assistance susceptible d’être fournie, des exemples de modèles d’expression régulière peuvent être donnés à des fins de test. Le support peut également aider à résoudre un problème de modèle RegEx existant dont le déclenchement ne fonctionne pas comme prévu avec un exemple de contenu spécifique unique.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p104">Due to the variances in customer environments and content match requirements, Microsoft Support cannot assist in providing custom content-matching definitions; e.g., defining custom classifications or regular expression (also known as RegEx) patterns. For custom content-matching development, testing, and debugging, Microsoft 365 customers will need to rely upon internal IT resources, or use an external consulting resource such as Microsoft Consulting Services (MCS). Support engineers can provide limited support for the feature, but cannot provide assurances that any custom content-matching development will fulfill the customer's requirements or obligations.  As an example of the type of support that can be provided, sample regular expression patterns may be provided for testing purposes. Or, support can assist with troubleshooting an existing RegEx pattern which is not triggering as expected with a single specific content example.</span></span>

<span data-ttu-id="b72b7-119">Voir [Éventuels problèmes de validation à prendre en compte](#potential-validation-issues-to-be-aware-of) dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b72b7-119">See [Potential validation issues to be aware of](#potential-validation-issues-to-be-aware-of) in this topic.</span></span>

<span data-ttu-id="b72b7-120">Pour plus d’informations sur le moteur Boost.RegEx (anciennement RegEx ++) utilisé pour traiter le texte, consultez [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="b72b7-120">For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

> [!NOTE]
> <span data-ttu-id="b72b7-121">Si vous utilisez un caractère & (&) dans le cadre d’un mot clé dans votre type d’informations sensibles personnalisé, notez qu’il existe un problème connu.</span><span class="sxs-lookup"><span data-stu-id="b72b7-121">If you use an ampersand character (&) as part of a keyword in your custom sensitive information type, please note that there is a known issue.</span></span> <span data-ttu-id="b72b7-122">Vous devez ajouter un terme supplémentaire avec des espaces autour du caractère pour vous assurer que le caractère est correctement identifié, par exemple, L & P _et_ non L&P.</span><span class="sxs-lookup"><span data-stu-id="b72b7-122">You should add an additional term with spaces around the character to make sure that the character is properly identified, for example, L & P _not_ L&P.</span></span>

## <a name="sample-xml-of-a-rule-package"></a><span data-ttu-id="b72b7-123">Exemple de code XML d’un package de règles</span><span class="sxs-lookup"><span data-stu-id="b72b7-123">Sample XML of a rule package</span></span>

<span data-ttu-id="b72b7-p106">Voici l’exemple de code XML du package de règles que nous allons créer dans cette rubrique. Les éléments et les attributs sont expliqués dans les sections ci-après.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p106">Here's the sample XML of the rule package that we'll create in this topic. Elements and attributes are explained in the sections below.</span></span>
  
```xml
<?xml version="1.0" encoding="UTF-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
<RulePack id="DAD86A92-AB18-43BB-AB35-96F7C594ADAA">
  <Version build="0" major="1" minor="0" revision="0"/>
  <Publisher id="619DD8C3-7B80-4998-A312-4DF0402BAC04"/>
  <Details defaultLangCode="en-us">
    <LocalizedDetails langcode="en-us">
      <PublisherName>Contoso</PublisherName>
      <Name>Employee ID Custom Rule Pack</Name>
      <Description>
      This rule package contains the custom Employee ID entity.
      </Description>
    </LocalizedDetails>
  </Details>
</RulePack>
<Rules>
<!-- Employee ID -->
  <Entity id="E1CC861E-3FE9-4A58-82DF-4BD259EAB378" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="65">
      <IdMatch idRef="Regex_employee_id"/>
    </Pattern>
    <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_employee_id"/>
      <Match idRef="Func_us_date"/>
    </Pattern>
    <Pattern confidenceLevel="85">
      <IdMatch idRef="Regex_employee_id"/>
      <Match idRef="Func_us_date"/>
      <Any minMatches="1">
        <Match idRef="Keyword_badge" minCount="2"/>
        <Match idRef="Keyword_employee"/>
      </Any>
      <Any minMatches="0" maxMatches="0">
        <Match idRef="Keyword_false_positives_local"/>
        <Match idRef="Keyword_false_positives_intl"/>
      </Any>
    </Pattern>
  </Entity>
  <Regex id="Regex_employee_id">(\s)(\d{9})(\s)</Regex>
  <Keyword id="Keyword_employee">
    <Group matchStyle="word">
      <Term>Identification</Term>
      <Term>Contoso Employee</Term>
    </Group>
  </Keyword>
  <Keyword id="Keyword_badge">
    <Group matchStyle="string">
      <Term>card</Term>
      <Term>badge</Term>
      <Term caseSensitive="true">ID</Term>
    </Group>
  </Keyword>
  <Keyword id="Keyword_false_positives_local">
    <Group matchStyle="word">
      <Term>credit card</Term>
      <Term>national ID</Term>
    </Group>
  </Keyword>
  <Keyword id="Keyword_false_positives_intl">
    <Group matchStyle="word">
      <Term>identity card</Term>
      <Term>national ID</Term>
      <Term>EU debit card</Term>
    </Group>
  </Keyword>
  <LocalizedStrings>
    <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB378">
      <Name default="true" langcode="en-us">Employee ID</Name>
      <Description default="true" langcode="en-us">
      A custom classification for detecting Employee IDs.
      </Description>
      <Description default="false" langcode="de-de">
      Description for German locale.
      </Description>
    </Resource>
  </LocalizedStrings>
</Rules>
</RulePackage>
```

## <a name="what-are-your-key-requirements-rule-entity-pattern-elements"></a><span data-ttu-id="b72b7-p107">Quelles sont vos principales exigences ? [éléments Rule, Entity et Pattern]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p107">What are your key requirements? [Rule, Entity, Pattern elements]</span></span>

<span data-ttu-id="b72b7-128">Avant de commencer, il est utile de comprendre la structure de base du schéma XML d’une règle et comment utiliser cette structure pour définir votre type d’informations sensibles personnalisé afin qu’il identifie le contenu approprié.</span><span class="sxs-lookup"><span data-stu-id="b72b7-128">Before you get started, it's helpful to understand the basic structure of the XML schema for a rule, and how you can use this structure to define your custom sensitive information type so that it will identify the right content.</span></span>
  
<span data-ttu-id="b72b7-p108">Une règle définit une ou plusieurs entités (types d’informations sensibles), et chaque entité définit un ou plusieurs modèles. Un motif est l’élément recherché par une stratégie lors de l’évaluation d’un contenu tel qu’un e-mail et des documents.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p108">A rule defines one or more entities (sensitive information types), and each entity defines one or more patterns. A pattern is what a policy looks for when it evaluates content such as email and documents.</span></span>

<span data-ttu-id="b72b7-p109">Dans cette rubrique, les marques XML utilisent la règle pour désigner les motifs qui définissent une entité, également appelée type d’informations sensibles. Par conséquent, lorsqu’une règle s’affiche, vous devez le comprendre comme une entité ou type d’informations sensibles, et pas comme conditions et actions.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p109">In this topic, the XML markup uses rule to mean the patterns that define an entity, also known as a sensitive information type. So in this topic, when you see rule, think entity or sensitive information type, not conditions and actions.</span></span>
  
### <a name="simplest-scenario-entity-with-one-pattern"></a><span data-ttu-id="b72b7-133">Scénario le plus simple : entité avec un modèle</span><span class="sxs-lookup"><span data-stu-id="b72b7-133">Simplest scenario: entity with one pattern</span></span>

<span data-ttu-id="b72b7-p110">Voici le scénario le plus simple : vous souhaitez que votre stratégie identifie le contenu qui comprend l’ID d’employé de votre organisation, sous la forme d’un nombre à neuf chiffres. Par conséquent, le modèle référence une expression régulière contenue dans la règle qui identifie le nombre à neuf chiffres. Tout contenu comprenant un nombre à neuf chiffres correspond au modèle.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p110">Here's the simplest scenario. You want your policy to identify content that contains your organization's employee ID, which is formatted as a nine-digit number. So the pattern refers to a regular expression contained in the rule that identifies nine-digit numbers. Any content containing a nine-digit number satisfies the pattern.</span></span>
  
![Diagramme d’une entité avec un modèle](../media/4cc82dcf-068f-43ff-99b2-bac3892e9819.png)
  
<span data-ttu-id="b72b7-139">Même s’il est simple, ce modèle peut identifier de nombreux faux positifs en faisant correspondre du contenu comprenant un nombre à neuf chiffres qui n’est pas nécessairement un ID d’employé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-139">However, while simple, this pattern may identify many false positives by matching content that contains any nine-digit number that is not necessarily an employee ID.</span></span>
  
### <a name="more-common-scenario-entity-with-multiple-patterns"></a><span data-ttu-id="b72b7-140">Scénario le plus courant : entité avec plusieurs modèles</span><span class="sxs-lookup"><span data-stu-id="b72b7-140">More common scenario: entity with multiple patterns</span></span>

<span data-ttu-id="b72b7-141">Pour cette raison, il est plus courant de définir une entité à l’aide de plusieurs modèles, où ces derniers identifient la preuve à l’appui (par exemple, un mot clé ou une date) en plus de l’entité (par exemple, un nombre à neuf chiffres).</span><span class="sxs-lookup"><span data-stu-id="b72b7-141">For this reason, it's more common to define an entity by using more than one pattern, where the patterns identify supporting evidence (such as a keyword or date) in addition to the entity (such as a nine-digit number).</span></span>
  
<span data-ttu-id="b72b7-142">Par exemple, pour augmenter la probabilité d’identifier le contenu qui contient un ID d’employé, vous pouvez définir un autre modèle qui identifie également une date d’embauche, et définir un autre modèle qui identifie une date d’embauche et un mot clé (par exemple, « ID d’employé ») en plus du nombre à neuf chiffres.</span><span class="sxs-lookup"><span data-stu-id="b72b7-142">For example, to increase the likelihood of identifying content that contains an employee ID, you can define another pattern that also identifies a hire date, and define yet another pattern that identifies both a hire date and a keyword (such as "employee ID"), in addition to the nine-digit number.</span></span>
  
![Diagramme d’une entité avec plusieurs modèle](../media/c8dc2c9d-00c6-4ebc-889a-53b41a90024a.png)
  
<span data-ttu-id="b72b7-144">Voici quelques aspects importants de cette structure à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="b72b7-144">Note a couple of important aspects of this structure:</span></span>
  
- <span data-ttu-id="b72b7-p111">Les modèles qui nécessitent plus de preuves ont un niveau de confiance plus élevé. Ceci est utile, car lorsque vous utilisez ultérieurement ce type d’informations sensibles dans une stratégie, vous pouvez utiliser des actions plus restrictives (par exemple, le blocage de contenu) avec uniquement les correspondances dont le niveau de confiance est le plus élevé, et vous pouvez utiliser les actions moins restrictives (par exemple, l’envoi de notification) avec les correspondances dont le niveau de confiance est le moins élevé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p111">Patterns that require more evidence have a higher confidence level. This is useful because when you later use this sensitive information type in a policy, you can use more restrictive actions (such as block content) with only the higher-confidence matches, and you can use less restrictive actions (such as send notification) with the lower-confidence matches.</span></span>

- <span data-ttu-id="b72b7-p112">Les éléments de soutien IdMatch et Match font référence à des regex (expressions régulières) et à des mots clés qui sont des enfants de l’élément Rule, pas de l’élément Pattern. Ces éléments de soutien sont référencés par le modèle, mais inclus dans la règle. Cela signifie qu’une seule définition d’un élément de soutien, par exemple, une expression régulière ou une liste de mots clés, peut être référencée par plusieurs entités et modèles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p112">The supporting IdMatch and Match elements reference regexes and keywords that are actually children of the Rule element, not the Pattern. These supporting elements are referenced by the Pattern but included in the Rule. This means that a single definition of a supporting element, like a regular expression or a keyword list, can be referenced by multiple entities and patterns.</span></span>

## <a name="what-entity-do-you-need-to-identify-entity-element-id-attribute"></a><span data-ttu-id="b72b7-p113">Quelle entité devez-vous identifier ? [élément Entity, attribut id]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p113">What entity do you need to identify? [Entity element, id attribute]</span></span>

<span data-ttu-id="b72b7-p114">Une entité est un type d’informations sensibles, tel qu’un numéro de carte de crédit, associé à un modèle bien défini. Chaque entité possède un GUID unique en tant qu’ID.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p114">An entity is a sensitive information type, such as a credit card number, that has a well-defined pattern. Each entity has a unique GUID as its ID.</span></span>
  
### <a name="name-the-entity-and-generate-its-guid"></a><span data-ttu-id="b72b7-154">Nommer l’entité et générer son GUID</span><span class="sxs-lookup"><span data-stu-id="b72b7-154">Name the entity and generate its GUID</span></span>

1. <span data-ttu-id="b72b7-155">Dans l’éditeur XML de votre choix, ajoutez les éléments Règles et Entité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-155">In your XML editor of choice, add the Rules and Entity elements.</span></span>
2. <span data-ttu-id="b72b7-p115">Ajoutez un commentaire qui contient le nom de votre entité personnalisée – dans cet exemple, l’ID d’employé. Plus tard, vous allez ajouter le nom de l’entité à la section de chaînes localisées et ce nom s’affiche dans l’interface utilisateur lorsque vous créez une stratégie.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p115">Add a comment that contains the name of your custom entity — in this example, Employee ID. Later, you'll add the entity name to the localized strings section, and that name is what appears in the UI when you create a policy.</span></span>
3. <span data-ttu-id="b72b7-158">Générez un GUID pour votre entité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-158">Generate a GUID for your entity.</span></span> <span data-ttu-id="b72b7-159">Vous disposez de plusieurs méthodes pour générer des GUID, mais cette opération peut être effectuée facilement dans PowerShell en saisissant **[guid]::NewGuid()**.</span><span class="sxs-lookup"><span data-stu-id="b72b7-159">There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing **[guid]::NewGuid()**.</span></span> <span data-ttu-id="b72b7-160">Plus tard, vous ajouterez également le GUID de l’entité à la section de chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="b72b7-160">Later, you'll also add the entity GUID to the localized strings section.</span></span>
  
![Balisage XML montrant les éléments Rules et Entity](../media/c46c0209-0947-44e0-ac3a-8fd5209a81aa.png)
  
## <a name="what-pattern-do-you-want-to-match-pattern-element-idmatch-element-regex-element"></a><span data-ttu-id="b72b7-p117">Quel modèle voulez-vous faire correspondre [élément Pattern, élément IdMatch et élément Regex]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p117">What pattern do you want to match? [Pattern element, IdMatch element, Regex element]</span></span>

<span data-ttu-id="b72b7-p118">Le modèle contient la liste des éléments recherchés par le type d’informations sensibles. Cela peut inclure des regex, des mots clés et des fonctions intégrées (qui effectuent des tâches telles que l’exécution des expressions régulières pour rechercher des dates ou des adresses). Ces types d’informations sensibles peuvent avoir plusieurs modèles avec des niveaux de confiance uniques.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p118">The pattern contains the list of what the sensitive information type is looking for. This can include regexes, keywords, and built-in functions (which perform tasks like running regexes to find dates or addresses). Sensitive information types can have multiple patterns with unique confidences.</span></span>
  
<span data-ttu-id="b72b7-p119">Le point commun de tous les modèles suivants est qu’ils référencent tous la même expression régulière, qui recherche un nombre à neuf chiffres (\d{9}) entre espaces (\s) … (\s). Cette expression régulière est référencée par l’élément IdMatch et est la condition requise commune à tous les modèles qui recherchent l’entité Employee ID. IdMatch est l’identificateur que le modèle cherche à faire correspondre, par exemple, comme ID d’employé, numéro de carte de crédit ou numéro de sécurité sociale. Un élément Pattern doit avoir exactement un élément IdMatch.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p119">What all of the below patterns have in common is that they all reference the same regular expression, which looks for a nine-digit number (\d{9}) surrounded by white space (\s) … (\s). This regular expression is referenced by the IdMatch element and is the common requirement for all patterns that look for the Employee ID entity. IdMatch is the identifier that the pattern is to trying to match, such as Employee ID or credit card number or social security number. A Pattern element must have exactly one IdMatch element.</span></span>
  
![Balisage XML montrant plusieurs éléments Pattern référençant un seul élément Regex](../media/8f3f497b-3b8b-4bad-9c6a-d9abf0520854.png)
  
<span data-ttu-id="b72b7-p120">Lorsqu’il est satisfait, le motif renvoie un nombre et un niveau de confiance, que vous pouvez utiliser dans les conditions de votre stratégie. Lorsque vous ajoutez une condition de détection d’un type d’informations sensibles à une stratégie, vous pouvez modifier le nombre et le niveau de confiance comme illustré ici. La notion de niveau de confiance (également appelée précision de correspondance) est expliquée plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p120">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your policy. When you add a condition for detecting a sensitive information type to a policy, you can edit the count and confidence level as shown here. Confidence level (also called match accuracy) is explained later in this topic.</span></span>
  
![Nombre d’instances et options de précision de correspondance](../media/sit-confidence-level.png)
  
<span data-ttu-id="b72b7-p121">Lorsque vous créez une expression régulière, n’oubliez pas que des problèmes peuvent survenir. Par exemple, si vous écrivez et chargez une regex qui identifie trop de contenu, cela peut nuire aux performances. Pour en savoir plus sur ces problèmes potentiels, consultez la section ultérieure [Problèmes de validation éventuels à prendre en compte](#potential-validation-issues-to-be-aware-of).</span><span class="sxs-lookup"><span data-stu-id="b72b7-p121">When you create your regular expression, keep in mind that there are potential issues to be aware of. For example, if you write and upload a regex that identifies too much content, this can impact performance. To learn more about these potential issues, see the later section [Potential validation issues to be aware of](#potential-validation-issues-to-be-aware-of).</span></span>
  
## <a name="do-you-want-to-require-additional-evidence-match-element-mincount-attribute"></a><span data-ttu-id="b72b7-p122">Voulez-vous demander des preuves supplémentaires ? [élément Match, attribut minCount]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p122">Do you want to require additional evidence? [Match element, minCount attribute]</span></span>

<span data-ttu-id="b72b7-182">En plus de l’élément IdMatch, un modèle peut utiliser l’élément Match pour demander des preuves à l’appui supplémentaires, telles qu’un mot clé, une regex, une date ou une adresse.</span><span class="sxs-lookup"><span data-stu-id="b72b7-182">In addition to the IdMatch, a pattern can use the Match element to require additional supporting evidence, such as a keyword, regex, date, or address.</span></span>
  
<span data-ttu-id="b72b7-p123">Un élément Pattern peut comporter plusieurs éléments Match ; ces éléments sont inclus directement dans l’élément Pattern ou combinés à l’aide de l’élément Any. Les éléments Match sont joints par un opérateur implicite AND ; tous les éléments Match doivent être satisfaits pour que le modèle corresponde. Vous pouvez utiliser l’élément Any pour introduire les opérateurs AND ou OR (plus d’informations dans une section ultérieure).</span><span class="sxs-lookup"><span data-stu-id="b72b7-p123">A Pattern can include multiple Match elements; they can be included directly in the Pattern element or combined by using the Any element. Match elements are joined by an implicit AND operator; all Match elements must be satisfied for the pattern to be matched. You can use the Any element to introduce AND or OR operators (more on that in a later section).</span></span>
  
<span data-ttu-id="b72b7-p124">Vous pouvez utiliser l’attribut facultatif minCount pour spécifier le nombre d’instances d’une correspondance qui doivent être trouvées pour chaque élément Match. Par exemple, vous pouvez spécifier qu’un modèle est satisfait uniquement lorsqu’au moins deux mots clés d’une liste de mots clés sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p124">You can use the optional minCount attribute to specify how many instances of a match need to be found for each of the Match elements. For example, you can specify that a pattern is satisfied only when at least two keywords from a keyword list are found.</span></span>
  
![Balisage XML montrant l’élément Match avec l’attribut minOccurs](../media/607f6b5e-2c7d-43a5-a131-a649f122e15a.png)
  
### <a name="keywords-keyword-group-and-term-elements-matchstyle-and-casesensitive-attributes"></a><span data-ttu-id="b72b7-189">Mots clés [éléments Keyword, Group et Term, attributs matchStyle et caseSensitive]</span><span class="sxs-lookup"><span data-stu-id="b72b7-189">Keywords [Keyword, Group, and Term elements, matchStyle and caseSensitive attributes]</span></span>

<span data-ttu-id="b72b7-p125">Lorsque vous identifiez les informations sensibles, telles qu’un ID d’employé, vous pouvez demander des mots clés comme preuve probante. Par exemple, en plus de faire correspondre un nombre à neuf chiffres, vous souhaiterez peut-être rechercher des mots tels que « carte », « badge » ou « ID ». Pour ce faire, utilisez l’élément Keyword. L’élément Keyword possède l’attribut ID qui peut être référencé par plusieurs éléments Match dans plusieurs modèles ou entités.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p125">When you identify sensitive information, like an employee ID, you often want to require keywords as corroborative evidence. For example, in addition to matching a nine-digit number, you may want to look for words like "card", "badge", or "ID". To do this, you use the Keyword element. The Keyword element has an ID attribute that can be referenced by multiple Match elements in multiple patterns or entities.</span></span>
  
<span data-ttu-id="b72b7-p126">Les mots clés sont inclus sous forme de liste d’éléments Term dans un élément Group. L’élément Group possède un attribut matchStyle avec deux valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="b72b7-p126">Keywords are included as a list of Term elements in a Group element. The Group element has a matchStyle attribute with two possible values:</span></span>
  
- <span data-ttu-id="b72b7-p127">**matchStyle="word"** La correspondance de mots identifie des mots entiers entourés par des espaces ou d’autres séparateurs. Vous devez toujours utiliser « word », sauf si vous devez faire correspondre des parties de mots ou des mots dans des langues asiatiques.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p127">**matchStyle="word"** Word match identifies whole words surrounded by white space or other delimiters. You should always use word unless you need to match parts of words or match words in Asian languages.</span></span> 
    
- <span data-ttu-id="b72b7-p128">**matchStyle="string"** La correspondance de chaînes identifie les chaînes, peu importe ce qui les entoure. Par exemple, « id » correspondra à « bid» et à « idea ». Utilisez « string » uniquement lorsque vous recherchez des mots asiatiques ou si votre mot clé est inclus dans d’autres chaînes.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p128">**matchStyle="string"** String match identifies strings no matter what they're surrounded by. For example, "id" will match "bid" and "idea". Use string only when you need to match Asian words or if your keyword may be included as part of other strings.</span></span> 
    
<span data-ttu-id="b72b7-201">Enfin, vous pouvez utiliser l’attribut caseSensitive de l’élément Term pour préciser que le contenu doit correspondre exactement au mot clé, notamment les lettres minuscules et majuscules.</span><span class="sxs-lookup"><span data-stu-id="b72b7-201">Finally, you can use the caseSensitive attribute of the Term element to specify that the content must match the keyword exactly, including lower- and upper-case letters.</span></span>
  
![Balisage XML montrant les éléments Match référençant des mots clés](../media/e729ba27-dec6-46f4-9242-584c6c12fd85.png)
  
### <a name="regular-expressions-regex-element"></a><span data-ttu-id="b72b7-203">Expressions régulières [élément Regex]</span><span class="sxs-lookup"><span data-stu-id="b72b7-203">Regular expressions [Regex element]</span></span>

<span data-ttu-id="b72b7-p129">Dans cet exemple, l’entité d’ID d’employé utilise déjà l’élément IdMatch pour référencer une regex pour le modèle (un nombre à neuf chiffres entouré d’espaces). De plus, un modèle peut utiliser un élément Match pour référencer un élément Regex supplémentaire afin d’identifier la preuve probante, par exemple un nombre de cinq ou neuf chiffres sous la forme d’un code postal des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p129">In this example, the employee ID entity already uses the IdMatch element to reference a regex for the pattern — a nine-digit number surrounded by whitespace. In addition, a pattern can use a Match element to reference an additional Regex element to identify corroborative evidence, such as a five- or nine-digit number in the format of a US zip code.</span></span>
  
### <a name="additional-patterns-such-as-dates-or-addresses-built-in-functions"></a><span data-ttu-id="b72b7-206">Autres modèles tels que des dates ou des adresses [fonctions intégrées]</span><span class="sxs-lookup"><span data-stu-id="b72b7-206">Additional patterns such as dates or addresses [built-in functions]</span></span>

<span data-ttu-id="b72b7-p130">En plus des types d’informations sensibles intégrés, les types d’informations sensibles peuvent également utiliser des fonctions intégrées qui peuvent identifier une preuve d’appui telle que la date des États-Unis, celle de l’Union Européenne, la date d’expiration, une adresse des États-Unis. Microsoft 365 ne prend pas en charge le chargement de fonctions personnalisées, mais lorsque vous créez un type d’informations sensibles personnalisé, votre entité peut référencer les fonctions intégrées.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p130">In addition to the built-in sensitive information types, sensitive information types can also use built-in functions that can identify corroborative evidence such as a US date, EU date, expiration date, or US address. Microsoft 365 does not support uploading your own custom functions, but when you create a custom sensitive information type, your entity can reference the built-in functions.</span></span>
  
<span data-ttu-id="b72b7-209">Par exemple, une date figure sur les badges d’ID d’employé. Cette entité personnalisée peut donc utiliser la fonction intégrée `Func_us_date` pour identifier une date au format utilisé aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="b72b7-209">For example, an employee ID badge has a hire date on it, so this custom entity can use the built-in function  `Func_us_date` to identify a date in the format commonly used in the US.</span></span> 
  
<span data-ttu-id="b72b7-210">Pour obtenir plus d’informations, consultez l’article [Éléments recherchés par les fonctions DLP](what-the-dlp-functions-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b72b7-210">For more information, see [What the DLP functions look for](what-the-dlp-functions-look-for.md).</span></span>
  
![Balisage XML montrant les éléments Match référençant une fonction intégrée](../media/dac6eae3-9c52-4537-b984-f9f127cc9c33.png)
  
## <a name="different-combinations-of-evidence-any-element-minmatches-and-maxmatches-attributes"></a><span data-ttu-id="b72b7-212">Différentes combinaisons de preuves [élément Any, attributs minMatches et maxMatches]</span><span class="sxs-lookup"><span data-stu-id="b72b7-212">Different combinations of evidence [Any element, minMatches and maxMatches attributes]</span></span>

<span data-ttu-id="b72b7-p131">Dans un élément Pattern, tous les éléments IdMatch et Match sont joints par un opérateur implicite AND : toutes les correspondances doivent être satisfaites pour que le modèle soit satisfait. Cependant, vous pouvez créer une logique de correspondance plus flexible en utilisant l’élément Any afin de regrouper des éléments Match. Par exemple, vous pouvez utiliser l’élément Any pour faire correspondre tous les sous-ensembles, aucun sous-ensemble ou un sous-ensemble exact de ses éléments Match enfants.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p131">In a Pattern element, all IdMatch and Match elements are joined by an implicit AND operator — all of the matches must be satisfied before the pattern can be satisfied. However, you can create more flexible matching logic by using the Any element to group Match elements. For example, you can use the Any element to match all, none, or an exact subset of its children Match elements.</span></span>
  
<span data-ttu-id="b72b7-p132">L’élément Any a des attributs minMatches et maxMatches facultatifs que vous pouvez utiliser pour définir le nombre d’éléments Match enfants qui doivent être satisfaits pour que le modèle corresponde. Notez que ces attributs définissent le nombre d’éléments Match qui doivent être satisfaits, pas le nombre d’instances de preuves trouvées pour les correspondances. Pour définir un nombre minimal d’instances pour une correspondance spécifique, par exemple, deux mots clés d’une liste, utilisez l’attribut minCount d’un élément Match (voir ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="b72b7-p132">The Any element has optional minMatches and maxMatches attributes that you can use to define how many of the children Match elements must be satisfied before the pattern is matched. Note that these attributes define the number of Match elements that must be satisfied, not the number of instances of evidence found for the matches. To define a minimum number of instances for a specific match, such as two keywords from a list, use the minCount attribute for a Match element (see above).</span></span>
  
### <a name="match-at-least-one-child-match-element"></a><span data-ttu-id="b72b7-219">Faire correspondre au moins un élément Match enfant</span><span class="sxs-lookup"><span data-stu-id="b72b7-219">Match at least one child Match element</span></span>

<span data-ttu-id="b72b7-p133">Si vous voulez exiger qu’au moins un nombre minimal d’éléments Match corresponde, vous pouvez utiliser l’attribut minMatches. En effet, ces éléments Match sont joints par un opérateur implicite OR. Cet élément Any est satisfait si une date au format américain ou un mot clé d’une liste est trouvé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p133">If you want to require that only a minimum number of Match elements must be met, you can use the minMatches attribute. In effect, these Match elements are joined by an implicit OR operator. This Any element is satisfied if a US-formatted date or a keyword from either list is found.</span></span>

```xml
<Any minMatches="1" >
     <Match idRef="Func_us_date" />
     <Match idRef="Keyword_employee" />
     <Match idRef="Keyword_badge" />
</Any>
```
    
### <a name="match-an-exact-subset-of-any-children-match-elements"></a><span data-ttu-id="b72b7-223">Faire correspondre un sous-ensemble exact d’éléments Match enfants</span><span class="sxs-lookup"><span data-stu-id="b72b7-223">Match an exact subset of any children Match elements</span></span>

<span data-ttu-id="b72b7-p134">Si vous voulez exiger qu’un nombre exact d’éléments Match corresponde, vous pouvez définir les attributs minMatches et maxMatches sur la même valeur. Cet élément Any est satisfait uniquement si une seule date ou un seul mot clé est trouvé (si plusieurs dates ou mots clés sont trouvés, le modèle ne correspond pas).</span><span class="sxs-lookup"><span data-stu-id="b72b7-p134">If you want to require that an exact number of Match elements must be met, you can set minMatches and maxMatches to the same value. This Any element is satisfied only if exactly one date or keyword is found — any more than that, and the pattern won't be matched.</span></span>

```xml
<Any minMatches="1" maxMatches="1" >
     <Match idRef="Func_us_date" />
     <Match idRef="Keyword_employee" />
     <Match idRef="Keyword_badge" />
</Any>
```
  
### <a name="match-none-of-children-match-elements"></a><span data-ttu-id="b72b7-226">Faire correspondre tous les enfants Match enfants</span><span class="sxs-lookup"><span data-stu-id="b72b7-226">Match none of children Match elements</span></span>

<span data-ttu-id="b72b7-p135">Si vous voulez exiger l’absence de preuve spécifique pour qu’un modèle soit satisfait, vous pouvez définir les attributs minMatches et maxMatches sur 0. Cela est utile si vous avez une liste de mots clés ou d’autres preuves susceptibles d’indiquer de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p135">If you want to require the absence of specific evidence for a pattern to be satisfied, you can set both minMatches and maxMatches to 0. This can be useful if you have a keyword list or other evidence that are likely to indicate a false positive.</span></span>
  
<span data-ttu-id="b72b7-p136">Par exemple, l’entité d’ID d’employé recherche le mot clé « carte », car il peut désigner une « carte d’identité ». Toutefois, si « carte » apparaît uniquement dans l’expression « carte de crédit », il est peu probable que « carte » dans ce contenu signifie « carte d’identité ». Par conséquent, vous pouvez ajouter « carte de crédit » comme mot clé à une liste de termes que vous voulez exclure de la satisfaction du modèle.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p136">For example, the employee ID entity looks for the keyword "card" because it might refer to an "ID card". However, if card appears only in the phrase "credit card", "card" in this content is unlikely to mean "ID card". So you can add "credit card" as a keyword to a list of terms that you want to exclude from satisfying the pattern.</span></span>
  
```xml
<Any minMatches="0" maxMatches="0" >
    <Match idRef="Keyword_false_positives_local" />
    <Match idRef="Keyword_false_positives_intl" />
</Any>
```

### <a name="match-a-number-of-unique-terms"></a><span data-ttu-id="b72b7-232">Corrélation de termes uniques</span><span class="sxs-lookup"><span data-stu-id="b72b7-232">Match a number of unique terms</span></span>

<span data-ttu-id="b72b7-233">Si vous voulez corréler un certain nombre de termes uniques, utilisez le paramètre *uniqueResults* et définissez-le sur *true* comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b72b7-233">If you want to match a number of unique terms, use the *uniqueResults* parameter, set to *true*, as shown in the following example:</span></span>

```xml
<Pattern confidenceLevel="75">
    <IdMatch idRef="Salary_Revision_terms" />
    <Match idRef=" Salary_Revision_ID " minCount="3" uniqueResults="true" />
</Pattern>
```

<span data-ttu-id="b72b7-234">Dans cet exemple, un modèle est défini pour une révision salariale utilisant au moins trois correspondances uniques.</span><span class="sxs-lookup"><span data-stu-id="b72b7-234">In this example, a pattern is defined for salary revision using at least three unique matches.</span></span> 
  
## <a name="how-close-to-the-entity-must-the-other-evidence-be-patternsproximity-attribute"></a><span data-ttu-id="b72b7-p137">Quel doit être le degré de proximité de l’entité par rapport à l’autre preuve ? [attribut patternsProximity]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p137">How close to the entity must the other evidence be? [patternsProximity attribute]</span></span>

<span data-ttu-id="b72b7-p138">Votre type d’informations sensibles recherche un modèle qui représente un ID d’employé et dans le cadre de ce modèle, il recherche également comme preuve probante un mot clé tel que « ID ». Il est logique que plus la proximité de cette preuve est élevée, plus le modèle est susceptible d’être un ID d’employé. Vous pouvez déterminer le degré de proximité d’autres preuves par rapport à l’entité dans le modèle à l’aide de l’attribut obligatoire patternsProximity de l’élément Entity.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p138">Your sensitive information type is looking for a pattern that represents an employee ID, and as part of that pattern it's also looking for corroborative evidence like a keyword such as "ID". It makes sense that the closer together this evidence is, the more likely the pattern is to be an actual employee ID. You can determine how close other evidence in the pattern must be to the entity by using the required patternsProximity attribute of the Entity element.</span></span>
  
![Balisage XML montrant l’attribut patternsProximity](../media/e97eb7dc-b897-4e11-9325-91c742d9839b.png)
  
<span data-ttu-id="b72b7-p139">Pour chaque modèle de l’entité, la valeur de l’attribut patternsProximity définit la distance (en caractères Unicode) à partir de l’emplacement IdMatch pour toutes les autres correspondances spécifiées pour ce modèle. La fenêtre de proximité est ancrée par l’emplacement IdMatch. La fenêtre s’étend à gauche et à droite de l’IdMatch.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p139">For each pattern in the entity, the patternsProximity attribute value defines the distance (in Unicode characters) from the IdMatch location for all other Matches specified for that Pattern. The proximity window is anchored by the IdMatch location, with the window extending to the left and right of the IdMatch.</span></span>
  
![Diagramme de la fenêtre de proximité](../media/b593dfd1-5eef-4d79-8726-a28923f7c31e.png)
  
<span data-ttu-id="b72b7-p140">L’exemple indiqué ci-après illustre comment la fenêtre de proximité affecte la correspondance du modèle là où l’élément IdMatch requiert au moins une correspondance probante de mot clé ou de date pour l’entité personnalisée d’ID d’employé. Seul ID1 correspond, car pour ID2 et ID3, seule une preuve probante partielle (voire aucune preuve probante) a été détectée au sein de la fenêtre de proximité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p140">The example below illustrates how the proximity window affects the pattern matching where IdMatch element for the employee ID custom entity requires at least one corroborating match of keyword or date. Only ID1 matches because for ID2 and ID3, either no or only partial corroborating evidence is found within the proximity window.</span></span>
  
![Diagramme de la fenêtre de proximité et de preuves probantes](../media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)
  
<span data-ttu-id="b72b7-p141">Notez que pour la messagerie, le corps du message et chaque pièce jointe sont traités comme des éléments distincts. Cela signifie que la fenêtre de proximité ne s’étend pas au-delà de chacun de ces éléments. Pour chaque élément (pièce jointe ou corps), l’attribut idMatch et la preuve probante doivent résider dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p141">Note that for email, the message body and each attachment are treated as separate items. This means that the proximity window does not extend beyond the end of each of these items. For each item (attachment or body), both the idMatch and corroborative evidence needs to reside in that item.</span></span>
  
## <a name="what-are-the-right-confidence-levels-for-different-patterns-confidencelevel-attribute-recommendedconfidence-attribute"></a><span data-ttu-id="b72b7-p142">Quels sont les niveaux de confiance appropriés pour les différents modèles ? [attributs confidenceLevel et recommendedConfidence]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p142">What are the right confidence levels for different patterns? [confidenceLevel attribute, recommendedConfidence attribute]</span></span>

<span data-ttu-id="b72b7-p143">Plus un modèle nécessite de preuves, plus vous pouvez être certain qu’une entité (par exemple, l’ID d’employé) a effectivement été identifiée lorsque le modèle a été mis en correspondance. Par exemple, vous pouvez davantage compter sur un modèle qui nécessite un numéro d’identification à neuf chiffres, une date d’embauche et un mot clé situés à proximité immédiate les uns des autres, que sur un modèle qui nécessite uniquement un numéro d’identification à neuf chiffres.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p143">The more evidence that a pattern requires, the more confidence you have that an actual entity (such as employee ID) has been identified when the pattern is matched. For example, you have more confidence in a pattern that requires a nine-digit ID number, hire date, and keyword in close proximity, than you do in a pattern that requires only a nine-digit ID number.</span></span>
  
<span data-ttu-id="b72b7-p144">L’élément Pattern est associé à un attribut confidenceLevel obligatoire. Vous pouvez considérer la valeur confidenceLevel (un nombre entier compris entre 1 et 100) comme un ID unique pour chaque motif d’une entité : les motifs d’une entité doivent avoir des niveaux de confiance distincts que vous attribuez. Peu importe la valeur précise du nombre entier, sélectionnez simplement un nombre approuvé par votre équipe de conformité. Une fois que vous avez chargé votre type d’informations sensibles personnalisé et que vous avez créé une stratégie, vous pouvez référencer ces niveaux de confiance dans les conditions des règles que vous créez.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p144">The Pattern element has a required confidenceLevel attribute. You can think of the value of confidenceLevel (an integer between 1 and 100) as a unique ID for each pattern in an entity — the patterns in an entity must have different confidence levels that you assign. The precise value of the integer doesn't matter — simply pick numbers that make sense to your compliance team. After you upload your custom sensitive information type and then create a policy, you can reference these confidence levels in the conditions of the rules that you create.</span></span>
  
![Balisage XML montrant les éléments Pattern avec des valeurs différentes pour l’attribut confidenceLevel](../media/sit-xml-markedup-2.png)
  
<span data-ttu-id="b72b7-259">En plus de l’attribut confidenceLevel de chaque modèle, l’entité possède un attribut recommendedConfidence.</span><span class="sxs-lookup"><span data-stu-id="b72b7-259">In addition to confidenceLevel for each Pattern, the Entity has a recommendedConfidence attribute.</span></span> <span data-ttu-id="b72b7-260">L’attribut de niveau de confiance recommandé est assimilable au niveau de confiance par défaut de la règle.</span><span class="sxs-lookup"><span data-stu-id="b72b7-260">The recommended confidence attribute can be thought of as the default confidence level for the rule.</span></span> <span data-ttu-id="b72b7-261">Lorsque vous créez une règle dans une stratégie, si vous n’indiquez pas le niveau de confiance que la règle doit utiliser, cette règle recherche les correspondances en fonction du niveau de confiance recommandé pour l’entité.</span><span class="sxs-lookup"><span data-stu-id="b72b7-261">When you create a rule in a policy, if you don't specify a confidence level for the rule to use, that rule will match based on the recommended confidence level for the entity.</span></span> <span data-ttu-id="b72b7-262">Notez que l’attribut recommendedConfidence est obligatoire pour chaque ID d’entité dans le package de règles, sans lui, vous ne pourrez pas enregistrer les stratégies utilisant le type d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-262">Please note that the recommendedConfidence attribute is mandatory for each Entity ID in the Rule Package, if missing you won't be able to save policies that use the Sensitive Information Type.</span></span> 
  
## <a name="do-you-want-to-support-other-languages-in-the-ui-of-the-compliance-center-localizedstrings-element"></a><span data-ttu-id="b72b7-p146">Voulez-vous prendre en charge d’autres langues dans l’interface utilisateur du Centre de conformité ? [élément LocalizedStrings]</span><span class="sxs-lookup"><span data-stu-id="b72b7-p146">Do you want to support other languages in the UI of the Compliance center? [LocalizedStrings element]</span></span>

<span data-ttu-id="b72b7-p147">Si votre équipe de conformité utilise le Centre de conformité Microsoft 365 pour créer des stratégies avec différents paramètres régionaux et dans différentes langues, vous pouvez fournir des versions localisées du nom et de la description de votre type d’informations sensibles personnalisé. Lorsque votre équipe de conformité utilise Microsoft 365 dans une langue que vous prenez en charge, le nom localisé s’affiche dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p147">If your compliance team uses the Microsoft 365 Compliance center to create polices policies in different locales and in different languages, you can provide localized versions of the name and description of your custom sensitive information type. When your compliance team uses Microsoft 365 in a language that you support, they'll see the localized name in the UI.</span></span>
  
![Nombre d’instances et options de précision de correspondance](../media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
<span data-ttu-id="b72b7-p148">L’élément Rules doit contenir un élément LocalizedStrings, qui contient un élément Resource référençant le GUID de votre entité personnalisée. À son tour, chaque élément Resource contient un ou plusieurs éléments Name et Description qui utilisent l’attribut langcode afin de fournir une chaîne localisée pour une langue spécifique.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p148">The Rules element must contain a LocalizedStrings element, which contains a Resource element that references the GUID of your custom entity. In turn, each Resource element contains one or more Name and Description elements that each use the langcode attribute to provide a localized string for a specific language.</span></span>
  
![Balisage XML montrant le contenu de l’élément LocalizedStrings](../media/a96fc34a-b93d-498f-8b92-285b16a7bbe6.png)
  
<span data-ttu-id="b72b7-p149">Notez que vous utilisez des chaînes localisées uniquement pour l’affichage de votre type d’informations sensibles dans l’interface utilisateur du Centre de conformité. Vous ne pouvez pas utiliser des chaînes localisées pour fournir différentes versions localisées d’une liste de mots clés ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p149">Note that you use localized strings only for how your custom sensitive information type appears in the UI of the Compliance center. You can't use localized strings to provide different localized versions of a keyword list or regular expression.</span></span>
  
## <a name="other-rule-package-markup-rulepack-guid"></a><span data-ttu-id="b72b7-273">Autre balisage de package de règles [GUID RulePack]</span><span class="sxs-lookup"><span data-stu-id="b72b7-273">Other rule package markup [RulePack GUID]</span></span>

<span data-ttu-id="b72b7-p150">Enfin, le début de chaque RulePackage contient des informations générales que vous avez besoin de compléter. Vous pouvez utiliser le balisage suivant comme modèle et remplacer les espaces réservés « ... » avec vos propres informations.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p150">Finally, the beginning of each RulePackage contains some general information that you need to fill in. You can use the following markup as a template and replace the ". . ." placeholders with your own info.</span></span>
  
<span data-ttu-id="b72b7-p151">Vous devez surtout générer un GUID pour le RulePack. Ci-dessus, vous avez généré un GUID pour l’entité ; il s’agit d’un second GUID pour le RulePack. Il existe plusieurs méthodes pour générer des GUID, mais vous pouvez le faire facilement dans PowerShell en saisissant [guid]::NewGuid().</span><span class="sxs-lookup"><span data-stu-id="b72b7-p151">Most importantly, you'll need to generate a GUID for the RulePack. Above, you generated a GUID for the entity; this is a second GUID for the RulePack. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing [guid]::NewGuid().</span></span>
  
<span data-ttu-id="b72b7-p152">L’élément Version est également important. Lorsque vous chargez votre package de règles pour la première fois, Microsoft 365 prend note du numéro de version. Si vous mettez à jour le package de règles ultérieurement et téléchargez une nouvelle version, veillez à mettre à jour le numéro de version, sinon Microsoft 365 ne déploiera pas le package de règles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p152">The Version element is also important. When you upload your rule package for the first time, Microsoft 365 notes the version number. Later, if you update the rule package and upload a new version, make sure to update the version number or Microsoft 365 won't deploy the rule package.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
  . . .
 </Rules>
</RulePackage>

```

<span data-ttu-id="b72b7-285">Lorsque vous avez terminé, votre élément RulePack doit ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b72b7-285">When complete, your RulePack element should look like this.</span></span>
  
![Balisage XML montrant l’élément RulePack](../media/fd0f31a7-c3ee-43cd-a71b-6a3813b21155.png)

## <a name="validators"></a><span data-ttu-id="b72b7-287">Validators</span><span class="sxs-lookup"><span data-stu-id="b72b7-287">Validators</span></span>

<span data-ttu-id="b72b7-288">Microsoft 365 des processeurs de fonctions pour les sits couramment utilisés comme validateurs.</span><span class="sxs-lookup"><span data-stu-id="b72b7-288">Microsoft 365 exposes function processors for commonly used SITs as validators.</span></span> <span data-ttu-id="b72b7-289">Voici une liste d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="b72b7-289">Here's a list of them.</span></span> 

### <a name="list-of-validators-currently-available"></a><span data-ttu-id="b72b7-290">Liste des validateurs actuellement disponibles</span><span class="sxs-lookup"><span data-stu-id="b72b7-290">List of validators currently available</span></span>

- <span data-ttu-id="b72b7-291">Func_credit_card</span><span class="sxs-lookup"><span data-stu-id="b72b7-291">Func_credit_card</span></span>
- <span data-ttu-id="b72b7-292">Func_ssn</span><span class="sxs-lookup"><span data-stu-id="b72b7-292">Func_ssn</span></span>
- <span data-ttu-id="b72b7-293">Func_unformatted_ssn</span><span class="sxs-lookup"><span data-stu-id="b72b7-293">Func_unformatted_ssn</span></span>
- <span data-ttu-id="b72b7-294">Func_randomized_formatted_ssn</span><span class="sxs-lookup"><span data-stu-id="b72b7-294">Func_randomized_formatted_ssn</span></span>
- <span data-ttu-id="b72b7-295">Func_randomized_unformatted_ssn</span><span class="sxs-lookup"><span data-stu-id="b72b7-295">Func_randomized_unformatted_ssn</span></span>
- <span data-ttu-id="b72b7-296">Func_aba_routing</span><span class="sxs-lookup"><span data-stu-id="b72b7-296">Func_aba_routing</span></span>
- <span data-ttu-id="b72b7-297">Func_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="b72b7-297">Func_south_africa_identification_number</span></span>
- <span data-ttu-id="b72b7-298">Func_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="b72b7-298">Func_brazil_cpf</span></span>
- <span data-ttu-id="b72b7-299">Func_iban</span><span class="sxs-lookup"><span data-stu-id="b72b7-299">Func_iban</span></span>
- <span data-ttu-id="b72b7-300">Func_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="b72b7-300">Func_brazil_cnpj</span></span>
- <span data-ttu-id="b72b7-301">Func_swedish_national_identifier</span><span class="sxs-lookup"><span data-stu-id="b72b7-301">Func_swedish_national_identifier</span></span>
- <span data-ttu-id="b72b7-302">Func_india_aadhaar</span><span class="sxs-lookup"><span data-stu-id="b72b7-302">Func_india_aadhaar</span></span>
- <span data-ttu-id="b72b7-303">Func_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="b72b7-303">Func_uk_nhs_number</span></span>
- <span data-ttu-id="b72b7-304">Func_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="b72b7-304">Func_Turkish_National_Id</span></span>
- <span data-ttu-id="b72b7-305">Func_australian_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="b72b7-305">Func_australian_tax_file_number</span></span>
- <span data-ttu-id="b72b7-306">Func_usa_uk_passport</span><span class="sxs-lookup"><span data-stu-id="b72b7-306">Func_usa_uk_passport</span></span>
- <span data-ttu-id="b72b7-307">Func_canadian_sin</span><span class="sxs-lookup"><span data-stu-id="b72b7-307">Func_canadian_sin</span></span>
- <span data-ttu-id="b72b7-308">Func_formatted_itin</span><span class="sxs-lookup"><span data-stu-id="b72b7-308">Func_formatted_itin</span></span>
- <span data-ttu-id="b72b7-309">Func_unformatted_itin</span><span class="sxs-lookup"><span data-stu-id="b72b7-309">Func_unformatted_itin</span></span>
- <span data-ttu-id="b72b7-310">Func_dea_number_v2</span><span class="sxs-lookup"><span data-stu-id="b72b7-310">Func_dea_number_v2</span></span>
- <span data-ttu-id="b72b7-311">Func_dea_number</span><span class="sxs-lookup"><span data-stu-id="b72b7-311">Func_dea_number</span></span>
- <span data-ttu-id="b72b7-312">Func_japanese_my_number_personal</span><span class="sxs-lookup"><span data-stu-id="b72b7-312">Func_japanese_my_number_personal</span></span>
- <span data-ttu-id="b72b7-313">Func_japanese_my_number_corporate</span><span class="sxs-lookup"><span data-stu-id="b72b7-313">Func_japanese_my_number_corporate</span></span>

<span data-ttu-id="b72b7-314">Cela vous permet de définir votre propre regex et de les valider.</span><span class="sxs-lookup"><span data-stu-id="b72b7-314">This gives you the ability to define your own regex and validate them.</span></span> <span data-ttu-id="b72b7-315">Pour utiliser des validateurs, définissez votre propre regex et, lors de la définition de l’regex, utilisez la propriété validator pour ajouter le processeur de fonction de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b72b7-315">To use validators, define your own regex and while defining the regex use the validator property to add the function processor of your choice.</span></span> <span data-ttu-id="b72b7-316">Une fois défini, vous pouvez utiliser cette regex dans un SIT.</span><span class="sxs-lookup"><span data-stu-id="b72b7-316">Once defined, you can use this regex in an SIT.</span></span> 

<span data-ttu-id="b72b7-317">Dans l’exemple ci-dessous, une expression régulière - Regex_credit_card_AdditionalDelimiters est définie pour la carte de crédit qui est ensuite validée à l’aide de la fonction checksum pour la carte de crédit à l’aide de Func_credit_card comme validateur.</span><span class="sxs-lookup"><span data-stu-id="b72b7-317">In the example below, a regular expression - Regex_credit_card_AdditionalDelimiters is defined for Credit card which is then validated using the checksum function for credit card by using Func_credit_card as a validator.</span></span>

```xml
<Regex id="Regex_credit_card_AdditionalDelimiters" validators="Func_credit_card"> (?:^|[\s,;\:\(\)\[\]"'])([0-9]{4}[ -_][0-9]{4}[ -_][0-9]{4}[ -_][0-9]{4})(?:$|[\s,;\:\(\)\[\]"'])</Regex>
<Entity id="675634eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
<Pattern confidenceLevel="85">
<IdMatch idRef="Regex_credit_card_AdditionalDelimiters" />
<Any minMatches="1">
<Match idRef="Keyword_cc_verification" />
<Match idRef="Keyword_cc_name" />
<Match idRef="Func_expiration_date" />
</Any>
</Pattern>
</Entity>
```

<span data-ttu-id="b72b7-318">Microsoft 365 fournit deux validateurs génériques</span><span class="sxs-lookup"><span data-stu-id="b72b7-318">Microsoft 365 provides two generic validators</span></span>

### <a name="checksum-validator"></a><span data-ttu-id="b72b7-319">Validateur checksum</span><span class="sxs-lookup"><span data-stu-id="b72b7-319">Checksum validator</span></span>

<span data-ttu-id="b72b7-320">Dans cet exemple, un validateur de checkum pour l’ID d’employé est défini pour valider l’regex pour EmployeeID.</span><span class="sxs-lookup"><span data-stu-id="b72b7-320">In this example, a checksum validator for employee ID is defined to validate the regex for EmployeeID.</span></span>

```xml
<Validators id="EmployeeIDChecksumValidator">
<Validator type="Checksum">
<Param name="Weights">2, 2, 2, 2, 2, 1</Param>
<Param name="Mod">28</Param>
<Param name="CheckDigit">2</Param> <!-- Check 2nd digit -->
<Param name="AllowAlphabets">1</Param> <!— 0 if no Alphabets -->
</Validator>
</Validators>
<Regex id="Regex_EmployeeID" validators="ChecksumValidator">(\d{5}[A-Z])</Regex>
<Entity id="675634eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
<Pattern confidenceLevel="85">
<IdMatch idRef="Regex_EmployeeID"/>
</Pattern>
</Entity>
```

### <a name="date-validator"></a><span data-ttu-id="b72b7-321">Validateur de date</span><span class="sxs-lookup"><span data-stu-id="b72b7-321">Date Validator</span></span>

<span data-ttu-id="b72b7-322">Dans cet exemple, un validateur de date est défini pour une partie regex dont la date est.</span><span class="sxs-lookup"><span data-stu-id="b72b7-322">In this example, a date validator is defined for a regex part of which is date.</span></span>

```xml
<Validators id="date_validator_1"> <Validator type="DateSimple"> <Param name="Pattern">DDMMYYYY</Param> <!—supported patterns DDMMYYYY, MMDDYYYY, YYYYDDMM, YYYYMMDD, DDMMYYYY, DDMMYY, MMDDYY, YYDDMM, YYMMDD --> </Validator> </Validators>
<Regex id="date_regex_1" validators="date_validator_1">\d{8}</Regex>
```
  
## <a name="changes-for-exchange-online"></a><span data-ttu-id="b72b7-323">Modifications pour Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b72b7-323">Changes for Exchange Online</span></span>

<span data-ttu-id="b72b7-p155">Auparavant, vous utilisiez peut-être Exchange Online PowerShell pour importer vos types d’informations sensibles personnalisés pour DLP. Désormais, vos types d’informations sensibles personnalisés peuvent être utilisés dans le Centre d’administration Exchange et dans le Centre de conformité. Dans le cadre de cette amélioration, nous vous conseillons d’utiliser l’interface PowerShell du Centre conformité pour importer vos types d’informations sensibles personnalisés, car vous ne pouvez plus les importer à partir de PowerShell Exchange. Vos types d’informations sensibles personnalisés continueront à fonctionner comme d’habitude. Toutefois, l’affichage dans le Centre d’administration Exchange des modifications apportées aux types d’informations sensibles personnalisés dans le Centre de conformité peut prendre au maximum une heure.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p155">Previously, you might have used Exchange Online PowerShell to import your custom sensitive information types for DLP. Now your custom sensitive information types can be used in both the Exchange admin center and the Compliance center. As part of this improvement, you should use Compliance center PowerShell to import your custom sensitive information types — you can't import them from the Exchange PowerShell anymore. Your custom sensitive information types will continue to work just like before; however, it may take up to one hour for changes made to custom sensitive information types in the Compliance center to appear in the Exchange admin center.</span></span>
  
<span data-ttu-id="b72b7-328">Notez que, dans le centre de conformité, vous pouvez utiliser la cmdlet **[New-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/new-dlpsensitiveinformationtyperulepackage)** pour charger un package de règles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-328">Note that in the Compliance center, you use the **[New-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/new-dlpsensitiveinformationtyperulepackage)** cmdlet to upload a rule package.</span></span> <span data-ttu-id="b72b7-329">(Auparavant, dans le centre d’administration Exchange, vous utilisiez la cmdlet **ClassificationRuleCollection**.)</span><span class="sxs-lookup"><span data-stu-id="b72b7-329">(Previously, in the Exchange admin center, you used the  **ClassificationRuleCollection**\` cmdlet.)</span></span> 
  
## <a name="upload-your-rule-package"></a><span data-ttu-id="b72b7-330">Télécharger votre package de règles</span><span class="sxs-lookup"><span data-stu-id="b72b7-330">Upload your rule package</span></span>

<span data-ttu-id="b72b7-331">Pour télécharger votre package de règles, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b72b7-331">To upload your rule package, do the following steps:</span></span>
  
1. <span data-ttu-id="b72b7-332">Enregistrez-le en tant que fichier .xml avec le codage Unicode.</span><span class="sxs-lookup"><span data-stu-id="b72b7-332">Save it as an .xml file with Unicode encoding.</span></span>
    
2. [<span data-ttu-id="b72b7-333">Se connecter à PowerShell du centre de conformité</span><span class="sxs-lookup"><span data-stu-id="b72b7-333">Connect to Compliance center PowerShell</span></span>](/powershell/exchange/exchange-online-powershell)
    
3. <span data-ttu-id="b72b7-334">Utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b72b7-334">Use the following syntax:</span></span>

   ```powershell
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "PathToUnicodeXMLFile" -Encoding Byte -ReadCount 0)
   ```

   <span data-ttu-id="b72b7-335">Cet exemple télécharge le fichier XML Unicode nommé MyNewRulePack.xml à partir de C:\My Documents.</span><span class="sxs-lookup"><span data-stu-id="b72b7-335">This example uploads the Unicode XML file named MyNewRulePack.xml from C:\My Documents.</span></span>

   ```powershell
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\My Documents\MyNewRulePack.xml" -Encoding Byte -ReadCount 0)
   ```

   <span data-ttu-id="b72b7-336">Pour une syntaxe détaillée et des informations de paramètrage, voir [New-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/new-dlpsensitiveinformationtyperulepackage).</span><span class="sxs-lookup"><span data-stu-id="b72b7-336">For detailed syntax and parameter information, see [New-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/new-dlpsensitiveinformationtyperulepackage).</span></span>

   > [!NOTE]
   > <span data-ttu-id="b72b7-337">Le nombre maximal de packages de règles pris en charge est de 10. Cependant, chaque package peut contenir la définition de plusieurs types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-337">The maximum number of rule packages supported is 10, but each package can contain the definition of multiple sensitive information types.</span></span>

4. <span data-ttu-id="b72b7-338">Pour vérifier que vous avez correctement créé un nouveau type d’informations sensibles, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b72b7-338">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

   - <span data-ttu-id="b72b7-339">Exécutez la cmdlet [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) pour vérifier que le nouveau package de règles est répertorié :</span><span class="sxs-lookup"><span data-stu-id="b72b7-339">Run the [Get-DlpSensitiveInformationTypeRulePackage](/powershell/module/exchange/get-dlpsensitiveinformationtyperulepackage) cmdlet to verify the new rule package is listed:</span></span>

     ```powershell
     Get-DlpSensitiveInformationTypeRulePackage
     ``` 

   - <span data-ttu-id="b72b7-340">Exécutez la cmdlet [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) pour vérifier que le type d’informations sensibles est répertorié :</span><span class="sxs-lookup"><span data-stu-id="b72b7-340">Run the [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) cmdlet to verify the sensitive information type is listed:</span></span>

     ```powershell
     Get-DlpSensitiveInformationType
     ``` 

     <span data-ttu-id="b72b7-341">Pour les types d’informations sensibles personnalisés, la valeur de propriété Publisher sera un numéro autre que Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-341">For custom sensitive information types, the Publisher property value will be something other than Microsoft Corporation.</span></span>

   - <span data-ttu-id="b72b7-342">Remplacez \<Name\> par la valeur Name du type d’informations sensibles (par exemple, Réf employé), puis exécutez la cmdlet [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) :</span><span class="sxs-lookup"><span data-stu-id="b72b7-342">Replace \<Name\> with the Name value of the sensitive information type (example: Employee ID) and run the [Get-DlpSensitiveInformationType](/powershell/module/exchange/get-dlpsensitiveinformationtype) cmdlet:</span></span>

     ```powershell
     Get-DlpSensitiveInformationType -Identity "<Name>"
     ```
    
## <a name="potential-validation-issues-to-be-aware-of"></a><span data-ttu-id="b72b7-343">Problèmes de validation éventuels à prendre en compte</span><span class="sxs-lookup"><span data-stu-id="b72b7-343">Potential validation issues to be aware of</span></span>

<span data-ttu-id="b72b7-p157">Lorsque vous chargez votre fichier XML de package de règles, le système valide le fichier XML et recherche des modèles incorrects connus et des problèmes de performance évidents. Voici quelques-uns des problèmes connus que la validation contrôle. Une expression régulière :</span><span class="sxs-lookup"><span data-stu-id="b72b7-p157">When you upload your rule package XML file, the system validates the XML and checks for known bad patterns and obvious performance issues. Here are some known issues that the validation checks for — a regular expression:</span></span>
  
- <span data-ttu-id="b72b7-346">ne peut pas commencer ou se terminer par l’alternateur « | », qui correspond à tous les éléments, car il est considéré comme une correspondance vide ;</span><span class="sxs-lookup"><span data-stu-id="b72b7-346">Cannot begin or end with alternator "|", which matches everything because it's considered an empty match.</span></span>
    
  <span data-ttu-id="b72b7-347">Par exemple, « |a » ou « b| » échoue à la validation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-347">For example, "|a" or "b|" will not pass validation.</span></span>
    
- <span data-ttu-id="b72b7-348">ne peut pas commencer ou se terminer par un modèle « .{0,m} » qui n’a aucune fonction et nuit uniquement aux performances ;</span><span class="sxs-lookup"><span data-stu-id="b72b7-348">Cannot begin or end with a ".{0,m}" pattern, which has no functional purpose and only impairs performance.</span></span>
    
  <span data-ttu-id="b72b7-349">Par exemple, « .{0,50}ASDF » ou « ASDF.{0,50} » échoue à la validation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-349">For example, ".{0,50}ASDF" or "ASDF.{0,50}" will not pass validation.</span></span>
    
- <span data-ttu-id="b72b7-350">ne peut pas contenir « .{0,m} » ou « .{1,m} » dans des groupes, et ne peut pas contenir « .\* » ou « .+ » dans des groupes ;</span><span class="sxs-lookup"><span data-stu-id="b72b7-350">Cannot have ".{0,m}" or ".{1,m}" in groups, and cannot have ".\*" or ".+" in groups.</span></span>
    
  <span data-ttu-id="b72b7-351">Par exemple, « (.{0,50000}) » échoue à la validation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-351">For example, "(.{0,50000})" will not pass validation.</span></span>
    
- <span data-ttu-id="b72b7-352">ne peut pas contenir de caractère avec les répéteurs « {0,m} » ou « {1, m} » dans des groupes ;</span><span class="sxs-lookup"><span data-stu-id="b72b7-352">Cannot have any character with "{0,m}" or "{1,m}" repeaters in groups.</span></span>
    
  <span data-ttu-id="b72b7-353">Par exemple, « (a\*) » échoue à la validation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-353">For example, "(a\*)" will not pass validation.</span></span>
    
- <span data-ttu-id="b72b7-354">ne peut pas commencer ou se terminer par « .{1,m} » ; utilisez simplement « . » ;</span><span class="sxs-lookup"><span data-stu-id="b72b7-354">Cannot begin or end with ".{1,m}"; instead, use just "."</span></span>
    
  <span data-ttu-id="b72b7-355">Par exemple, « .{1,m}asdf » échoue à la validation ; utilisez simplement « .asdf ».</span><span class="sxs-lookup"><span data-stu-id="b72b7-355">For example, ".{1,m}asdf" will not pass validation; instead, use just ".asdf".</span></span>
    
- <span data-ttu-id="b72b7-356">ne peut pas contenir de répéteur illimité (tel que « \* » ou « + ») dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="b72b7-356">Cannot have an unbounded repeater (such as "\*" or "+") on a group.</span></span>
    
  <span data-ttu-id="b72b7-357">Par exemple, « (xx)\* » et « (xx)+ » échouent à la validation.</span><span class="sxs-lookup"><span data-stu-id="b72b7-357">For example, "(xx)\*" and "(xx)+" will not pass validation.</span></span>
  
- <span data-ttu-id="b72b7-358">Les mots clés ne peuvent pas contenir plus de 50 caractères.</span><span class="sxs-lookup"><span data-stu-id="b72b7-358">Keywords have a maximum of 50 characters in Length.</span></span>  <span data-ttu-id="b72b7-359">Si un mot clé au sein d’un groupe dépasse cette limite, une solution suggérée consiste à créer le groupe de termes en tant que [Dictionnaire de mots clés](./create-a-keyword-dictionary.md) et à référencer le GUID du dictionnaire de mots clés au sein de la structure XML dans le cadre de l’entité pour les correspondances ou idMatch dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b72b7-359">If you have a keyword within a Group exceeding this, a suggested solution is to create the Group of terms as a [Keyword Dictionary](./create-a-keyword-dictionary.md) and reference the GUID of the Keyword Dictionary within the XML structure as part of the Entity for Match or idMatch in the file.</span></span>

- <span data-ttu-id="b72b7-360">Chaque type d’informations sensibles personnalisé peut contenir un total maximum de 2 048 mots clés.</span><span class="sxs-lookup"><span data-stu-id="b72b7-360">Each Custom Sensitive Information Type can have a maximum of 2048 keywords total.</span></span>

- <span data-ttu-id="b72b7-361">La taille maximale des dictionnaires de mots clés dans un client est de 1 Mo au format compressé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-361">The maximum size of Keyword Dictionaries in a single tenant is 1 MB compressed.</span></span> <span data-ttu-id="b72b7-362">Faites référence au même dictionnaire autant de fois que nécessaire lors de la création de types d’informations sensibles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b72b7-362">Reference the same dictionary as many times as necessary when creating custom sensitive information types.</span></span> <span data-ttu-id="b72b7-363">Commencez par créer des listes de mots clés personnalisés dans le type informations sensibles, puis utilisez des dictionnaires de mots clés si une liste de mots clés en comporte plus de 2048 ou si un mot clé comporte plus de 50 caractères.</span><span class="sxs-lookup"><span data-stu-id="b72b7-363">Start with creating custom keyword lists in the sensitive information type and use keyword dictionaries if you have more than 2048 keywords in a keyword list or a keyword is larger than 50 characters in length.</span></span>

- <span data-ttu-id="b72b7-364">Un maximum de 50 types d’informations sensibles basés sur un dictionnaire de mots clés sont autorisés dans un client.</span><span class="sxs-lookup"><span data-stu-id="b72b7-364">A maximum of 50 keyword dictionary based sensitive information types are allowed in a tenant.</span></span>

- <span data-ttu-id="b72b7-365">Vérifiez que chaque élément Entité contient un attribut recommendedConfidence.</span><span class="sxs-lookup"><span data-stu-id="b72b7-365">Ensure each Entity element contains a recommendedConfidence attribute.</span></span>

- <span data-ttu-id="b72b7-366">Lorsque vous utilisez la cmdlet PowerShell, la taille de retour maximale des données désérialisées est d’environ 1 mégaoctet.</span><span class="sxs-lookup"><span data-stu-id="b72b7-366">When using the PowerShell Cmdlet there is a maximum return size of the Deserialized Data of approximately 1 megabyte.</span></span>   <span data-ttu-id="b72b7-367">Cela affecte la taille de votre fichier XML de pack de règles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-367">This will affect the size of your rule pack XML file.</span></span> <span data-ttu-id="b72b7-368">Conservez le fichier chargé limité à un maximum de 770 kilo-octets comme limite recommandée pour obtenir des résultats cohérents sans erreur lors du traitement.</span><span class="sxs-lookup"><span data-stu-id="b72b7-368">Keep the uploaded file limited to a 770 kilobyte maximum as a suggested limit for consistent results without error when processing.</span></span>

- <span data-ttu-id="b72b7-369">La structure XML ne requiert pas de caractères de mise en forme tels que des espaces, des tabulations ou des entrées de retour chariot/de saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="b72b7-369">The XML structure does not require formatting characters such as spaces, tabs, or carriage return/linefeed entries.</span></span>  <span data-ttu-id="b72b7-370">Prenez-en note lorsque vous optimisez l’espace disponible sur les téléchargements.</span><span class="sxs-lookup"><span data-stu-id="b72b7-370">Take note of this when optimizing for space on uploads.</span></span> <span data-ttu-id="b72b7-371">Des outils tels que Microsoft Visual Code fournissent des fonctionnalités de ligne de jointure permettant de compacter le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="b72b7-371">Tools such as Microsoft Visual Code provide join line features to compact the XML file.</span></span>
    
<span data-ttu-id="b72b7-372">Si un type d’informations sensibles personnalisé contient un problème qui peut affecter les performances, il n’est pas chargé et l’un des messages d’erreur suivants s’affichent :</span><span class="sxs-lookup"><span data-stu-id="b72b7-372">If a custom sensitive information type contains an issue that may affect performance, it won't be uploaded and you may see one of these error messages:</span></span>
  
- <span data-ttu-id="b72b7-373">**Quantificateurs génériques correspondant à plus de contenu que prévu (par exemple, « + » et « \* »)**</span><span class="sxs-lookup"><span data-stu-id="b72b7-373">**Generic quantifiers which match more content than expected (e.g., '+', '\*')**</span></span>
    
- <span data-ttu-id="b72b7-374">**Assertions d’inspection**</span><span class="sxs-lookup"><span data-stu-id="b72b7-374">**Lookaround assertions**</span></span>
    
- <span data-ttu-id="b72b7-375">**Regroupement complexe conjointement avec des quantificateurs généraux**</span><span class="sxs-lookup"><span data-stu-id="b72b7-375">**Complex grouping in conjunction with general quantifiers**</span></span>
    
## <a name="recrawl-your-content-to-identify-the-sensitive-information"></a><span data-ttu-id="b72b7-376">Analyser de nouveau le contenu pour identifier les informations sensibles</span><span class="sxs-lookup"><span data-stu-id="b72b7-376">Recrawl your content to identify the sensitive information</span></span>

<span data-ttu-id="b72b7-p162">Microsoft 365 utilise le robot de recherche pour identifier et classer les informations sensibles du contenu d’un site. Le contenu des sites SharePoint Online et OneDrive Entreprise est à nouveau analysé automatiquement chaque fois qu’il est mis à jour. Mais pour que votre nouveau type d’informations sensibles personnalisé puisse être identifié dans l’ensemble du contenu existant, il doit être de nouveau analysé.</span><span class="sxs-lookup"><span data-stu-id="b72b7-p162">Microsoft 365 uses the search crawler to identify and classify sensitive information in site content. Content in SharePoint Online and OneDrive for Business sites is recrawled automatically whenever it's updated. But to identify your new custom type of sensitive information in all existing content, that content must be recrawled.</span></span>
  
<span data-ttu-id="b72b7-380">Dans Microsoft 365, vous ne pouvez pas demander manuellement une nouvelle analyse de l’ensemble d’un client, mais vous pouvez le faire pour une collection de sites, une liste ou une bibliothèque (consultez l’article [Demander manuellement l’analyse et la réindexation d’un site, d’une bibliothèque ou d’une liste](/sharepoint/crawl-site-content)).</span><span class="sxs-lookup"><span data-stu-id="b72b7-380">In Microsoft 365, you can't manually request a recrawl of an entire tenant, but you can do this for a site collection, list, or library — see [Manually request crawling and re-indexing of a site, a library or a list](/sharepoint/crawl-site-content).</span></span>
  
## <a name="reference-rule-package-xml-schema-definition"></a><span data-ttu-id="b72b7-381">Référence : Définition du schéma XML du package de règles</span><span class="sxs-lookup"><span data-stu-id="b72b7-381">Reference: Rule package XML schema definition</span></span>

<span data-ttu-id="b72b7-382">Vous pouvez copier ce balisage, l’enregistrer sous la forme d’un fichier XSD et l’utiliser pour valider le fichier XML de votre package de règles.</span><span class="sxs-lookup"><span data-stu-id="b72b7-382">You can copy this markup, save it as an XSD file, and use it to validate your rule package XML file.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema xmlns:mce="http://schemas.microsoft.com/office/2011/mce"
           targetNamespace="http://schemas.microsoft.com/office/2011/mce"
           xmlns:xs="https://www.w3.org/2001/XMLSchema"
           elementFormDefault="qualified"
           attributeFormDefault="unqualified"
           id="RulePackageSchema">
  <!-- Use include if this schema has the same target namespace as the schema being referenced, otherwise use import -->
  <xs:element name="RulePackage" type="mce:RulePackageType"/>
  <xs:simpleType name="LangType">
    <xs:union memberTypes="xs:language">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value=""/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="GuidType" final="#all">
    <xs:restriction base="xs:token">
      <xs:pattern value="[0-9a-fA-F]{8}\-([0-9a-fA-F]{4}\-){3}[0-9a-fA-F]{12}"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulePackageType">
    <xs:sequence>
      <xs:element name="RulePack" type="mce:RulePackType"/>
      <xs:element name="Rules" type="mce:RulesType">
        <xs:key name="UniqueRuleId">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueProcessorId">
          <xs:selector xpath="mce:Regex|mce:Keyword|mce:Fingerprint"></xs:selector>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueResourceIdRef">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:key>
        <xs:keyref name="ReferencedRuleMustExist" refer="mce:UniqueRuleId">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:keyref>
        <xs:keyref name="RuleMustHaveResource" refer="mce:UniqueResourceIdRef">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:keyref>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="RulePackType">
    <xs:sequence>
      <xs:element name="Version" type="mce:VersionType"/>
      <xs:element name="Publisher" type="mce:PublisherType"/>
      <xs:element name="Details" type="mce:DetailsType">
        <xs:key name="UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="mce:LocalizedDetails"/>
          <xs:field xpath="@langcode"/>
        </xs:key>
        <xs:keyref name="DefaultLangCodeMustExist" refer="mce:UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="."/>
          <xs:field xpath="@defaultLangCode"/>
        </xs:keyref>
      </xs:element>
      <xs:element name="Encryption" type="mce:EncryptionType" minOccurs="0" maxOccurs="1"/>
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="VersionType">
    <xs:attribute name="major" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="minor" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="build" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="revision" type="xs:unsignedShort" use="required"/>
  </xs:complexType>
  <xs:complexType name="PublisherType">
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="LocalizedDetailsType">
    <xs:sequence>
      <xs:element name="PublisherName" type="mce:NameType"/>
      <xs:element name="Name" type="mce:RulePackNameType"/>
      <xs:element name="Description" type="mce:OptionalNameType"/>
    </xs:sequence>
    <xs:attribute name="langcode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="DetailsType">
    <xs:sequence>
      <xs:element name="LocalizedDetails" type="mce:LocalizedDetailsType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="defaultLangCode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="EncryptionType">
    <xs:sequence>
      <xs:element name="Key" type="xs:normalizedString"/>
      <xs:element name="IV" type="xs:normalizedString"/>
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="RulePackNameType">
    <xs:restriction base="xs:token">
      <xs:minLength value="1"/>
      <xs:maxLength value="64"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="NameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="1"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="OptionalNameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="0"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="RestrictedTermType">
    <xs:restriction base="xs:string">
      <xs:minLength value="1"/>
      <xs:maxLength value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulesType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Entity" type="mce:EntityType"/>
        <xs:element name="Affinity" type="mce:AffinityType"/>
        <xs:element name="Version" type="mce:VersionedRuleType"/>
      </xs:choice>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Regex" type="mce:RegexType"/>
        <xs:element name="Keyword" type="mce:KeywordType"/>
        <xs:element name="Fingerprint" type="mce:FingerprintType"/>
        <xs:element name="ExtendedKeyword" type="mce:ExtendedKeywordType"/>
      </xs:choice>
      <xs:element name="LocalizedStrings" type="mce:LocalizedStringsType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="EntityType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedPatternType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="patternsProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="recommendedConfidence" type="mce:ProbabilityType"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="PatternType">
    <xs:sequence>
      <xs:element name="IdMatch" type="mce:IdMatchType"/>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="AffinityType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedEvidenceType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="evidencesProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="thresholdConfidenceLevel" type="mce:ProbabilityType" use="required"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="EvidenceType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="IdMatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
  </xs:complexType>
  <xs:complexType name="MatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
    <xs:attribute name="minCount" type="xs:positiveInteger" use="optional"/>
    <xs:attribute name="uniqueResults" type="xs:boolean" use="optional"/>
  </xs:complexType>
  <xs:complexType name="AnyType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="minMatches" type="xs:nonNegativeInteger" default="1"/>
    <xs:attribute name="maxMatches" type="xs:nonNegativeInteger" use="optional"/>
  </xs:complexType>
  <xs:simpleType name="ProximityType">
    <xs:union>
      <xs:simpleType>
        <xs:restriction base='xs:string'>
          <xs:enumeration value="unlimited"/>
        </xs:restriction>
      </xs:simpleType>
      <xs:simpleType>
        <xs:restriction base="xs:positiveInteger">
          <xs:minInclusive value="1"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="ProbabilityType">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="1"/>
      <xs:maxInclusive value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="WorkloadType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange"/>
      <xs:enumeration value="Outlook"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="EngineVersionType">
    <xs:restriction base="xs:token">
      <xs:pattern value="^\d{2}\.01?\.\d{3,4}\.\d{1,3}$"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="VersionedRuleType">
    <xs:choice maxOccurs="unbounded">
      <xs:element name="Entity" type="mce:EntityType"/>
      <xs:element name="Affinity" type="mce:AffinityType"/>
    </xs:choice>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedPatternType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedEvidenceType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:simpleType name="FingerprintValueType">
    <xs:restriction base="xs:string">
      <xs:minLength value="2732"/>
      <xs:maxLength value="2732"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="FingerprintType">
    <xs:simpleContent>
      <xs:extension base="mce:FingerprintValueType">
        <xs:attribute name="id" type="xs:token" use="required"/>
        <xs:attribute name="threshold" type="mce:ProbabilityType" use="required"/>
        <xs:attribute name="shingleCount" type="xs:positiveInteger" use="required"/>
        <xs:attribute name="description" type="xs:string" use="optional"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="RegexType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="KeywordType">
    <xs:sequence>
      <xs:element name="Group" type="mce:GroupType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:token" use="required"/>
  </xs:complexType>
  <xs:complexType name="GroupType">
    <xs:sequence>
      <xs:choice>
        <xs:element name="Term" type="mce:TermType" maxOccurs="unbounded"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="matchStyle" default="word">
      <xs:simpleType>
        <xs:restriction base="xs:NMTOKEN">
          <xs:enumeration value="word"/>
          <xs:enumeration value="string"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  <xs:complexType name="TermType">
    <xs:simpleContent>
      <xs:extension base="mce:RestrictedTermType">
        <xs:attribute name="caseSensitive" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="ExtendedKeywordType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="LocalizedStringsType">
    <xs:sequence>
      <xs:element name="Resource" type="mce:ResourceType" maxOccurs="unbounded">
      <xs:key name="UniqueLangCodeUsedInNamePerResource">
        <xs:selector xpath="mce:Name"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
      <xs:key name="UniqueLangCodeUsedInDescriptionPerResource">
        <xs:selector xpath="mce:Description"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
    </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="ResourceType">
    <xs:sequence>
      <xs:element name="Name" type="mce:ResourceNameType" maxOccurs="unbounded"/>
      <xs:element name="Description" type="mce:DescriptionType" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="idRef" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="ResourceNameType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="DescriptionType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
</xs:schema>
```

## <a name="more-information"></a><span data-ttu-id="b72b7-383">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b72b7-383">More information</span></span>

- [<span data-ttu-id="b72b7-384">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="b72b7-384">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)

- [<span data-ttu-id="b72b7-385">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="b72b7-385">Sensitive information type entity definitions</span></span>](sensitive-information-type-entity-definitions.md)

- [<span data-ttu-id="b72b7-386">Éléments recherchés par les fonctions DLP</span><span class="sxs-lookup"><span data-stu-id="b72b7-386">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
