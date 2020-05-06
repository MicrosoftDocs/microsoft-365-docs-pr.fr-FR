---
title: Création d’un schéma de classification pour les données personnelles
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
audience: ITPro
ms.topic: overview
ms.collection:
- Strat_O365_Enterprise
- Ent_O365
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Déterminez si votre organisation doit implémenter des étiquettes dans le cadre de votre plan de Règlement général sur la protection des données (RGPD).
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 17484e56206ba8f32db3c779623f2f8d7ed57496
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44035166"
---
# <a name="architect-a-classification-schema-for-personal-data"></a><span data-ttu-id="21068-103">Création d’un schéma de classification pour les données personnelles</span><span class="sxs-lookup"><span data-stu-id="21068-103">Architect a classification schema for personal data</span></span>

<span data-ttu-id="21068-p101">Les articles précédents de cette série se concentrent sur l’utilisation des types d’informations sensibles pour identifier les données personnelles qui sont soumises au RGPD. Les types d’informations sensibles constituent une forme de classification qui pourrait vous suffire. Toutefois, de nombreuses organisations implémentent une stratégie de gouvernance des données plus large qui utilise des étiquettes. Utilisez cette rubrique pour déterminer si vous souhaitez implémenter des étiquettes également dans le cadre de votre plan RGPD. Si c’est le cas, cette rubrique fournit des conseils et des exemples.</span><span class="sxs-lookup"><span data-stu-id="21068-p101">Previous articles in this series focus on using sensitive information types to identify personal data that is subject to GDPR. Sensitive information types are a form of classification. This might be all the classification you need. However, many organizations implement a broader data governance strategy using labels. Use this topic to decide if you also want to implement labels as part of your GDPR plan. If you do, this topic provides some guidance and examples.</span></span>

<span data-ttu-id="21068-p102">Remarque : la définition d’un schéma de classification pour une organisation et la configuration des stratégies, étiquettes et conditions nécessitent une planification et une préparation rigoureuses. Il est important de savoir qu’il ne s’agit pas d’un processus informatisé. Vous devez collaborer avec votre équipe juridique et de conformité pour développer une classification appropriée et un schéma de création d’étiquettes pour les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="21068-p102">Note: Defining a classification schema for an organization and configuring policies, labels, and conditions requires careful planning and preparation. It's important to realize that this isn't an IT driven process. Be sure to work with your legal and compliance team to develop an appropriate classification and labeling schema for your organization's data.</span></span>

## <a name="decide-if-youre-using-labels-in-addition-to-sensitive-data-types"></a><span data-ttu-id="21068-113">Utilisation ou non d’étiquettes en plus des types de données sensibles</span><span class="sxs-lookup"><span data-stu-id="21068-113">Decide if you're using labels in addition to sensitive data types</span></span>

<span data-ttu-id="21068-p103">Vous avez le choix entre deux approches de classification dans Microsoft 365 pour les informations personnelles. L’une d’elles peut être utilisée pour la protection RGPD. Si vous décidez d’utiliser uniquement des types d’informations sensibles pour la classification, vous pouvez ignorer le reste de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="21068-p103">You can take one of two approaches for classification in Microsoft 365 for personal information. Either of these can be used for GDPR protection. If you decide to use only sensitive information types for classification, you can skip the rest of this topic.</span></span>

<span data-ttu-id="21068-117">Choisissez l'une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="21068-117">Choose one of the following options.</span></span>

### <a name="option-1-use-only-microsoft-365-sensitive-information-types"></a><span data-ttu-id="21068-118">Option 1 : utiliser des types d’informations sensibles Microsoft 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="21068-118">Option 1: Use only Microsoft 365 sensitive information types</span></span>

- <span data-ttu-id="21068-119">Les types d’informations sensibles sont efficaces pour identifier et protéger les données personnelles soumises au RGPD et d’autres types de règlements.</span><span class="sxs-lookup"><span data-stu-id="21068-119">Sensitive information types work well to identify and protect personal data subject to GDPR and other types of regulations.</span></span>

- <span data-ttu-id="21068-120">Ils sont plus simples à utiliser si votre organisation n’a pas encore (ou n’envisage pas d’implémenter) de plan de gouvernance de données plus large qui utilise des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="21068-120">These are simpler to use if your organization doesn't already have or plan to implement a broader data governance plan using labels.</span></span>

- <span data-ttu-id="21068-121">Fonctionne avec les règles DLP (comme les étiquettes de rétention).</span><span class="sxs-lookup"><span data-stu-id="21068-121">These work with DLP rules (so do retention labels).</span></span>

- <span data-ttu-id="21068-122">Les types d’informations sensibles sont compatibles à Cloud App Security pour détecter les informations sensibles dans d’autres applications SaaS.</span><span class="sxs-lookup"><span data-stu-id="21068-122">Sensitive information types work with Cloud App Security so you can detect sensitive information in other SaaS apps.</span></span>

### <a name="option-2-use-sensitive-information-types--retention-labels"></a><span data-ttu-id="21068-123">Option 2 : utiliser des types d’informations sensibles + des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="21068-123">Option 2: Use sensitive information types + retention labels</span></span>

- <span data-ttu-id="21068-124">Vous aurez besoin de types d’informations sensibles pour appliquer automatiquement des étiquettes à des données personnelles qui sont soumises au RGPD, donc ceci est une condition préalable.</span><span class="sxs-lookup"><span data-stu-id="21068-124">You'll need sensitive information types to automatically apply labels to personal data that is subject to GDPR, so these are a prerequisite.</span></span>

- <span data-ttu-id="21068-125">L’utilisation d’étiquettes Office vous permet d’inclure des données personnelles qui sont soumises au RGPD dans un plan de gouvernance des données plus large pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="21068-125">Using retention labels allows you to include personal data that is subject to GDPR into a broader data governance plan for your organization.</span></span>

## <a name="develop-a-label-schema-that-includes-personal-data"></a><span data-ttu-id="21068-126">Développement d’un schéma d’étiquettes qui comprend des données personnelles</span><span class="sxs-lookup"><span data-stu-id="21068-126">Develop a label schema that includes personal data</span></span>

<span data-ttu-id="21068-p104">Avant d’utiliser des fonctionnalités techniques pour appliquer des étiquettes et une protection, commencez par définir un schéma de classification à utiliser au sein de votre organisation. Il se peut que votre organisation ait déjà un schéma de classification, ce qui facilite l’ajout de données personnelles. Cette rubrique inclut un exemple de schéma de classification. Vous pouvez utiliser cet exemple comme point de départ, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="21068-p104">Before using technical capabilities to apply labels and protection, first work across your organization to define a classification schema. Your organization might already have a classification schema, which makes it easier to add personal data. This topic includes an example classification schema. You can use this example as a starting point, if needed.</span></span>

### <a name="getting-started"></a><span data-ttu-id="21068-131">Prise en main</span><span class="sxs-lookup"><span data-stu-id="21068-131">Getting started</span></span>

<span data-ttu-id="21068-p105">Commencez par décider du nombre et des noms des étiquettes à implémenter. Ne vous souciez pas de la technologie à utiliser ni de la façon dont les étiquettes seront appliquées. Appliquez ce schéma dans l’ensemble de votre organisation, y compris les données qui se trouvent en local et dans d’autres services cloud.</span><span class="sxs-lookup"><span data-stu-id="21068-p105">Begin by deciding on the number and names of labels to implement. Do this activity without worrying about which technology to use and how labels will be applied. Apply this schema universally throughout your organization, including data that resides on premises and in other cloud services.</span></span>

### <a name="recommendations"></a><span data-ttu-id="21068-135">Recommandations</span><span class="sxs-lookup"><span data-stu-id="21068-135">Recommendations</span></span> 

<span data-ttu-id="21068-136">Lorsque vous concevez et implémentez des stratégies, étiquettes et conditions, vous pouvez suivre ces recommandations :</span><span class="sxs-lookup"><span data-stu-id="21068-136">When designing and implementing policies, labels and conditions, consider following these recommendations:</span></span>

- <span data-ttu-id="21068-p106">Utilisez le schéma de classification existant (le cas échéant) &ndash; de nombreuses organisations utilisent déjà la classification des données d’une certaine façon. Évaluez soigneusement le schéma d’étiquettes existant et, si possible, utilisez-le en l’état. L’utilisation d’étiquettes connues qui sont reconnaissables pour l’utilisateur final favorisa l’adoption.</span><span class="sxs-lookup"><span data-stu-id="21068-p106">Use existing classification schema (if any) &ndash; Many organizations already are using data classification in some form. Carefully evaluate the existing label schema and if possible use it as is. Using familiar labels that are recognizable to the end user will drive adoption.</span></span>

- <span data-ttu-id="21068-p107">Commencez par des étiquettes et des stratégies par défaut &ndash; toutes les solutions sont accompagnées d’un ensemble d’étiquettes et de stratégies prédéfinies. Évaluez-les soigneusement en fonction des exigences juridiques et professionnelles des organisations et envisagez de les utiliser plutôt que d’en créer d’autres.</span><span class="sxs-lookup"><span data-stu-id="21068-p107">Start with default policies and labels &ndash; All solutions come with a set of predefined policies and labels. Carefully evaluate these against the organization's legal and business requirements and consider using them instead of creating new ones.</span></span>

- <span data-ttu-id="21068-p108">Commencez avec un petit nombre &ndash; il n’y a presque aucune limite au nombre d’étiquettes pouvant être créées. Toutefois, un grand nombre d’étiquettes et d’étiquettes secondaires aura un impact négatif sur l’adoption. Trop de choix signifie souvent aucun choix.</span><span class="sxs-lookup"><span data-stu-id="21068-p108">Start small &ndash; There's virtually no limit to the number of labels that can be created. However, large numbers of labels and sub-labels will negatively impact the adoption. Too many choices often mean no choice at all.</span></span>

- <span data-ttu-id="21068-145">Utilisez des scénarios et des cas d’utilisation &ndash; identifiez des cas d’utilisation courants au sein de l’organisation et utilisez des scénarios dérivés du RGPD pour vérifier si la configuration d’étiquette et de classification envisagée fonctionnera en pratique.</span><span class="sxs-lookup"><span data-stu-id="21068-145">Use scenarios and use cases &ndash; Identify common use cases within the organization and use scenarios derived from the GDPR to verify if the envisioned label and classification configuration will work in practice.</span></span>

- <span data-ttu-id="21068-p109">Posez-vous des questions à chaque demande d’une nouvelle étiquette &ndash; est-ce que chaque scénario ou cas d’utilisation nécessite vraiment une nouvelle étiquette ou pouvez-vous utiliser celles que vous avez déjà ? Le fait d’utiliser un nombre d’étiquettes restreint améliore l’adoption.</span><span class="sxs-lookup"><span data-stu-id="21068-p109">Question every request for a new label &ndash; Does every scenario or use case really need a new label or can you use what you already have? Keeping the number of labels to a minimum improves adoption.</span></span>

- <span data-ttu-id="21068-p110">Utilisez des étiquettes secondaires pour des services clés &ndash; Certains services auront des besoins spécifiques nécessitant des étiquettes spécifiques. Définissez ces étiquettes comme étiquettes secondaires d’une étiquette existante et envisagez d’utiliser des stratégies limitées qui sont affectées à des groupes d’utilisateurs plutôt que des stratégies globales.</span><span class="sxs-lookup"><span data-stu-id="21068-p110">Use sub-labels for key departments &ndash; Some departments will have specific needs that require specific labels. Define these labels as sub-labels to an existing label, and consider using scoped policies that are assigned to user groups instead of globally.</span></span>

- <span data-ttu-id="21068-p111">Utilisez des stratégies limitées &ndash; C’est-à-dire des stratégies qui ciblent des sous-ensembles d’utilisateurs, pour éviter la « surcharge d’étiquettes ». Une stratégie limitée permet d’attribuer des étiquettes (secondaires) propres à un rôle ou à un service uniquement aux employés qui travaillent pour ce service spécifique.</span><span class="sxs-lookup"><span data-stu-id="21068-p111">Consider scoped policies &ndash; Policies targeted at subsets of users will prevent "label overload". A scoped policy lets you assign role or department-specific (sub-)labels to just employees that work for that specific department.</span></span>

- <span data-ttu-id="21068-p112">Utiliser des noms d’étiquette explicites &ndash; Il est recommandé de ne pas utiliser de jargon, de normes ni d’acronymes comme noms d’étiquette. Essayez d’utiliser des noms évocateurs pour l’utilisateur final afin d’améliorer l’adoption. Au lieu d’utiliser des étiquettes comme PII, PCI, HIPAA, LBI, MBI et HBI, utilisez des noms tels que Non professionnel, Public, Général, Confidentiel et Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="21068-p112">Use meaningful label names &ndash; We recommend that you don't use jargon, standards, or acronyms as label names. Try to use names that resonate with the end user to improve adoption. Instead of using labels like PII, PCI, HIPAA, LBI, MBI, and HBI, consider names like Non-Business, Public, General, Confidential, and Highly Confidential.</span></span>

### <a name="example-classification-schema"></a><span data-ttu-id="21068-155">Exemple de schéma de classification</span><span class="sxs-lookup"><span data-stu-id="21068-155">Example classification schema</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21068-156"><strong>Nom de l’étiquette</strong></span><span class="sxs-lookup"><span data-stu-id="21068-156"><strong>Label name</strong></span></span></th>
<th align="left"><span data-ttu-id="21068-157"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="21068-157"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-158">Personnel</span><span class="sxs-lookup"><span data-stu-id="21068-158">Personal</span></span></td>
<td align="left"><span data-ttu-id="21068-159">Données non métiers, pour une utilisation personnelle uniquement.</span><span class="sxs-lookup"><span data-stu-id="21068-159">Non-business data, for personal use only.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-160">Public</span><span class="sxs-lookup"><span data-stu-id="21068-160">Public</span></span></td>
<td align="left"><span data-ttu-id="21068-161">Données métiers qui sont spécifiquement préparées et approuvées pour une utilisation publique.</span><span class="sxs-lookup"><span data-stu-id="21068-161">Business data that is specifically prepared and approved for public consumption.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-162">Données client</span><span class="sxs-lookup"><span data-stu-id="21068-162">Customer data</span></span></td>
<td align="left"><span data-ttu-id="21068-p113">Données métiers qui contiennent des informations personnelles identifiables. Les numéros de carte de crédit, les numéros de compte bancaire et les numéros de sécurité sociale en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="21068-p113">Business data that contains personal identifiable information. Examples are credit card numbers, bank account numbers, and social security numbers.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-165">Données RH</span><span class="sxs-lookup"><span data-stu-id="21068-165">HR data</span></span></td>
<td align="left"><span data-ttu-id="21068-166">Données de ressources humaines relatives aux employés de Contoso, telles que les données de salaire et de numéro d’employé.</span><span class="sxs-lookup"><span data-stu-id="21068-166">Human Resource data about Contoso employees, such as employee number and salary data.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-167">Confidentiel</span><span class="sxs-lookup"><span data-stu-id="21068-167">Confidential</span></span></td>
<td align="left"><span data-ttu-id="21068-p114">Données métiers sensibles qui peuvent porter atteinte à l’entreprise si elles sont partagées avec des personnes non autorisées. Les contrats, rapports de sécurité, résumés des prévisions et données des comptes commerciaux en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="21068-p114">Sensitive business data that could cause damage to the business if shared with unauthorized people. Examples include contracts, security reports, forecast summaries, and sales account data.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-170">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="21068-170">Highly confidential</span></span></td>
<td align="left"><span data-ttu-id="21068-p115">Données métiers très sensibles qui porteraient atteinte à l’entreprise si elles étaient partagées avec des personnes non autorisées. Les informations relatives aux employés et aux clients, mots de passe, code source et rapports financiers prédéfinis en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="21068-p115">Very sensitive business data that would cause damage to the business if it was shared with unauthorized people. Examples include employee and customer information, passwords, source code, and pre-announced financial reports.</span></span></td>
</tr>
</tbody>
</table>

## <a name="define-a-taxonomy-and-search-criteria-for-each-label"></a><span data-ttu-id="21068-173">Définition d’une taxonomie et de critères de recherche pour chaque étiquette</span><span class="sxs-lookup"><span data-stu-id="21068-173">Define a taxonomy and search criteria for each label</span></span>

<span data-ttu-id="21068-p116">Après le développement d’un schéma de classification pour votre organisation, l’étape suivante consiste à développer la taxonomie et les critères de recherche pour rechercher ces données. Pour les données personnelles, vous avez déjà effectué cette tâche en identifiant les types d’informations sensibles et en personnalisant ou créant des types d’informations sensibles pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="21068-p116">After developing a classification schema for your organization, the next step is to develop the taxonomy and search criteria for finding this data. For personal data, you've already completed this work by identifying sensitive information types and customizing or creating new sensitive information types for your environment.</span></span>

<span data-ttu-id="21068-p117">Le tableau suivant fournit un exemple de schéma de taxonomie et des critères de recherche pour une organisation. Les étiquettes sont classées par niveau de confidentialité (de moins sensibles à plus sensibles) pour garantir que l’étiquette appropriée est attribuée aux données qui correspondent à plusieurs conditions d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="21068-p117">The following table provides an example schema, taxonomy, and search criteria for an organization. The labels are ordered by sensitivity level from least sensitive to most sensitive to ensure that data that matches multiple label conditions is assigned the appropriate label.</span></span>

<span data-ttu-id="21068-178">Remarque : l’exemple de configuration est fourni à des fins d’illustration uniquement et n’est pas destiné à servir de conseil ni de référence.</span><span class="sxs-lookup"><span data-stu-id="21068-178">Note: The configuration example is provided for illustration only and is not intended as deployment guidance or reference.</span></span>

<span data-ttu-id="21068-179">L’important est de garantir que le travail que vous effectuez pour classer les données personnelles pour la conformité au RGPD fonctionne bien avec les objectifs de l’ensemble de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="21068-179">The important takeaway is to ensure that the work you invest to classify personal data for GDPR compliance fits together with the objectives for your entire organization.</span></span>

### <a name="example-schema-taxonomy-and-search-criteria"></a><span data-ttu-id="21068-180">Exemple de schéma, taxonomie et critères de recherche</span><span class="sxs-lookup"><span data-stu-id="21068-180">Example schema, taxonomy, and search criteria</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="21068-181"><strong>Étiquette</strong></span><span class="sxs-lookup"><span data-stu-id="21068-181"><strong>Label</strong></span></span></th>
<th align="left"><span data-ttu-id="21068-182"><strong>Taxonomie</strong></span><span class="sxs-lookup"><span data-stu-id="21068-182"><strong>Taxonomy</strong></span></span></th>
<th align="left"><span data-ttu-id="21068-183"><strong>Méthode</strong></span><span class="sxs-lookup"><span data-stu-id="21068-183"><strong>Method</strong></span></span></th>
<th align="left"><span data-ttu-id="21068-184"><strong>Syntaxe de recherche</strong></span><span class="sxs-lookup"><span data-stu-id="21068-184"><strong>Search syntax</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-185">Personnel</span><span class="sxs-lookup"><span data-stu-id="21068-185">Personal</span></span></td>
<td align="left"><span data-ttu-id="21068-186">Documents étiquetés manuellement avec l’étiquette Personnel par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="21068-186">Documents manually labeled personal by the end user.</span></span></td>
<td align="left"><span data-ttu-id="21068-187">Manuel</span><span class="sxs-lookup"><span data-stu-id="21068-187">Manual</span></span></td>
<td align="left"><span data-ttu-id="21068-188">Documents étiquetés manuellement avec l’étiquette Personnel par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="21068-188">Documents manually labeled personal by the end user.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-189">Public</span><span class="sxs-lookup"><span data-stu-id="21068-189">Public</span></span></td>
<td align="left"><span data-ttu-id="21068-190">Documents contenant l’expression ne respectant pas la casse Approuvé pour divulgation publique ##/### où # représente n’importe quel chiffre.</span><span class="sxs-lookup"><span data-stu-id="21068-190">Documents containing the case insensitive phrase Approved for Public Release ##/#### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="21068-191">KQL</span><span class="sxs-lookup"><span data-stu-id="21068-191">KQL</span></span></p>
<p><span data-ttu-id="21068-192">RegEx</span><span class="sxs-lookup"><span data-stu-id="21068-192">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="21068-193">KQL — Approuvé pour divulgation publique\*</span><span class="sxs-lookup"><span data-stu-id="21068-193">KQL — Approved for Public Release\*</span></span></p>
<p><span data-ttu-id="21068-194">RegEx — (?i)(\bApprouvé pour divulgation publique \d{2}\/\d{4}\b)</span><span class="sxs-lookup"><span data-stu-id="21068-194">RegEx — (?i)(\bApproved for Public Release \d{2}\/\d{4}\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-195">Données client</span><span class="sxs-lookup"><span data-stu-id="21068-195">Customer data</span></span></td>
<td align="left"><span data-ttu-id="21068-196">Types d’informations sensibles pour les données des citoyens européens.</span><span class="sxs-lookup"><span data-stu-id="21068-196">Sensitive information types for EU citizen data.</span></span></td>
<td align="left"><span data-ttu-id="21068-197">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="21068-197">Sensitive information types</span></span></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-198">Ressources humaines — Données des employés</span><span class="sxs-lookup"><span data-stu-id="21068-198">Human Resources — Employee Data</span></span></td>
<td align="left"><span data-ttu-id="21068-199">Documents incluant l’ID d’employé respectant la casse au format CONTOSO-9##### où # représente n’importe quel chiffre.</span><span class="sxs-lookup"><span data-stu-id="21068-199">Documents that include the case-sensitive employee id in the format CONTOSO-9##### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="21068-200">KQL</span><span class="sxs-lookup"><span data-stu-id="21068-200">KQL</span></span></p>
<p><span data-ttu-id="21068-201">RegEx</span><span class="sxs-lookup"><span data-stu-id="21068-201">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="21068-202">KQL — CONTOSO-9\*</span><span class="sxs-lookup"><span data-stu-id="21068-202">KQL — CONTOSO-9\*</span></span></p>
<p><span data-ttu-id="21068-203">RegEx — (\bCONTOSO-9\d{5}\b)</span><span class="sxs-lookup"><span data-stu-id="21068-203">RegEx — (\bCONTOSO-9\d{5}\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-204">Ressources humaines — Données salariales</span><span class="sxs-lookup"><span data-stu-id="21068-204">Human Resources — Salary Data</span></span></td>
<td align="left"><span data-ttu-id="21068-205">Documents qui incluent le mot-clé (ne respectant pas la casse) Contoso ET le mot-clé Salaire (ne respectant pas la casse) OU Rémunération</span><span class="sxs-lookup"><span data-stu-id="21068-205">Documents that include the keyword (not case sensitive) Contoso AND either keyword (not case sensitive) Salary OR Compensation</span></span></td>
<td align="left"><p><span data-ttu-id="21068-206">KQL</span><span class="sxs-lookup"><span data-stu-id="21068-206">KQL</span></span></p>
<p><span data-ttu-id="21068-207">RegEx</span><span class="sxs-lookup"><span data-stu-id="21068-207">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="21068-208">KQL — Contoso AND (Salaire OR Rémunération)</span><span class="sxs-lookup"><span data-stu-id="21068-208">KQL — Contoso AND (Salary OR Compensation)</span></span></p>
<p><span data-ttu-id="21068-209">RegEx — (\bCONTOSO-9\d{5}\b)</span><span class="sxs-lookup"><span data-stu-id="21068-209">RegEx — (\bCONTOSO-9\d{5}\b)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="21068-210">Confidentiel</span><span class="sxs-lookup"><span data-stu-id="21068-210">Confidential</span></span></td>
<td align="left"><span data-ttu-id="21068-211">Tous les documents contenant l’expression Contoso Confidentiel (ne respectant pas la casse).</span><span class="sxs-lookup"><span data-stu-id="21068-211">Documents containing the phrase (not case sensitive) Contoso Confidential.</span></span></td>
<td align="left"><p><span data-ttu-id="21068-212">KQL</span><span class="sxs-lookup"><span data-stu-id="21068-212">KQL</span></span></p>
<p><span data-ttu-id="21068-213">RegEx</span><span class="sxs-lookup"><span data-stu-id="21068-213">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="21068-214">KQL — Contoso Confidentiel</span><span class="sxs-lookup"><span data-stu-id="21068-214">KQL — Contoso Confidential</span></span></p>
<p><span data-ttu-id="21068-215">RegEx — (?i)(\bContoso Confidentiel\b)</span><span class="sxs-lookup"><span data-stu-id="21068-215">RegEx — (?i)(\bContoso Confidential\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="21068-216">Hautement confidentiel</span><span class="sxs-lookup"><span data-stu-id="21068-216">Highly confidential</span></span></td>
<td align="left"><span data-ttu-id="21068-217">Documents incluant l’expression Contoso Secret (respectant la casse) ou Secret-C#### où # représente n’importe quel chiffre.</span><span class="sxs-lookup"><span data-stu-id="21068-217">Documents that include either pharase (case sensitive) Contoso Secret or Secret-C#### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="21068-218">KQL</span><span class="sxs-lookup"><span data-stu-id="21068-218">KQL</span></span></p>
<p><span data-ttu-id="21068-219">RegEx</span><span class="sxs-lookup"><span data-stu-id="21068-219">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="21068-220">KQL — Contoso Secret OR Secret-C\*</span><span class="sxs-lookup"><span data-stu-id="21068-220">KQL — Contoso Secret OR Secret-C\*</span></span></p>
<p><span data-ttu-id="21068-221">RegEx — (?i)(\bContoso Secret\b)|(\bSecret-C\d{4}\b)</span><span class="sxs-lookup"><span data-stu-id="21068-221">RegEx — (?i)(\bContoso Secret\b)|(\bSecret-C\d{4}\b)</span></span></p></td>
</tr>
</tbody>
</table>
