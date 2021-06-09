---
title: Types d’explications dans Microsoft SharePoint Syntex
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: En savoir plus sur la liste d’expressions, les expressions régulières et les types d’explications de proximité dans Microsoft SharePoint Syntex.
ms.openlocfilehash: cfc217d9e671f2a3a9daa89f80e7d932adeac2c0
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843349"
---
# <a name="explanation-types-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="59511-103">Types d’explications dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="59511-103">Explanation types in Microsoft SharePoint Syntex</span></span>

<span data-ttu-id="59511-104">Les explications sont utilisées pour vous permettre de définir les informations que vous souhaitez étiqueter et extraire dans vos modèles de compréhension de documents dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="59511-104">Explanations are used to help to define the information you want to label and extract in your document understanding models in Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="59511-105">Lorsque vous créez une explication, vous devez sélectionner un type d’explication.</span><span class="sxs-lookup"><span data-stu-id="59511-105">When you create an explanation, you need to select an explanation type.</span></span> <span data-ttu-id="59511-106">Cet article vous permet de comprendre les différents types d’explications et comment ils sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="59511-106">This article helps you understand the different explanation types and how they're used.</span></span>

![Capture d’écran du panneau Créer une explication montrant les trois types d’explications.](../media/content-understanding/explanation-types.png)

<span data-ttu-id="59511-108">Les types d’explications suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="59511-108">These explanation types are available:</span></span>

- <span data-ttu-id="59511-109">[**Liste d’expressions**](#phrase-list) : liste de mots, expressions, nombres ou autres caractères que vous pouvez utiliser dans le document ou les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="59511-109">[**Phrase list**](#phrase-list): List of words, phrases, numbers, or other characters you can use in the document or information that you're extracting.</span></span> <span data-ttu-id="59511-110">Par exemple, la chaîne de texte *Médecin référent* se trouve dans tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="59511-110">For example, the text string *referring doctor* is in all Medical Referral documents you're identifying.</span></span> <span data-ttu-id="59511-111">Ou le *Numéro de téléphone* du médecin référent de tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="59511-111">Or the *phone number* of the referring doctor from all Medical Referral documents that you're identifying.</span></span>

- <span data-ttu-id="59511-112">[**Expression régulière**](#regular-expression) utilise une notation correspondant à un modèle pour rechercher des modèles de caractères spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59511-112">[**Regular expression**](#regular-expression): Uses a pattern-matching notation to find specific character patterns.</span></span> <span data-ttu-id="59511-113">Par exemple, vous pouvez utiliser une expression régulière pour rechercher toutes les instances d’une *adresse e-mail* modèle dans un ensemble de documents.</span><span class="sxs-lookup"><span data-stu-id="59511-113">For example, you can use a regular expression to find all instances of an *email address* pattern in a set of documents.</span></span>

- <span data-ttu-id="59511-114">[**Proximité**](#proximity) : décrit à quel point les explications sont proches les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="59511-114">[**Proximity**](#proximity): Describes how close explanations are to each other.</span></span> <span data-ttu-id="59511-115">Par exemple, une liste de phrases de *numéros de rue* se trouve juste avant la liste d’expressions des *noms de rue*, sans jetons entre les deux (vous en apprendrez davantage sur les jetons plus loin dans cet article).</span><span class="sxs-lookup"><span data-stu-id="59511-115">For example, a *street number* phrase list goes right before the *street name* phrase list, with no tokens in between (you'll learn about tokens later in this article).</span></span> <span data-ttu-id="59511-116">L’utilisation du type de proximité nécessite que vous ayez au moins deux explications dans votre modèle. Dans le cas contraire, l’option sera désactivée.</span><span class="sxs-lookup"><span data-stu-id="59511-116">Using the proximity type requires you to have at least two explanations in your model or the option will be disabled.</span></span>

## <a name="phrase-list"></a><span data-ttu-id="59511-117">Liste d’expressions</span><span class="sxs-lookup"><span data-stu-id="59511-117">Phrase list</span></span>

<span data-ttu-id="59511-118">Un type d’explication de liste d’expressions est généralement utilisé pour identifier et classer un document dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="59511-118">A phrase list explanation type is typically used to identify and classify a document through your model.</span></span> <span data-ttu-id="59511-119">Comme décrit dans l’exemple d’étiquette *Médecin référent*, il s’agit d’une chaîne de mots, d’expressions, de nombres ou de caractères qui se trouve systématiquement dans les documents que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="59511-119">As described in the *referring doctor* label example, it's a string of words, phrases, numbers, or characters that is consistently in the documents that you're identifying.</span></span>

<span data-ttu-id="59511-120">Bien que ce ne soit pas obligatoire, vous pouvez améliorer les performances de votre explication si l’expression que vous capturez se trouve à un emplacement cohérent dans votre document.</span><span class="sxs-lookup"><span data-stu-id="59511-120">While not a requirement, you can achieve better success with your explanation if the phrase you're capturing is located in a consistent location in your document.</span></span> <span data-ttu-id="59511-121">Par exemple, l’étiquette *Médecin référent* peut être située systématiquement dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="59511-121">For example, the *referring doctor* label might be consistently located in the first paragraph of the document.</span></span> <span data-ttu-id="59511-122">Vous pouvez également utiliser le paramètre avancé **[Configurer l’emplacement de survenance des phrases dans le document](explanation-types-overview.md#configure-where-phrases-occur-in-the-document)** pour sélectionner des zones spécifiques dans lesquelles la phrase se situe, surtout s’il existe une possibilité que la phrase se produise dans plusieurs emplacements au sein de votre document.</span><span class="sxs-lookup"><span data-stu-id="59511-122">You can also use the **[Configure where phrases occur in the document](explanation-types-overview.md#configure-where-phrases-occur-in-the-document)** advanced setting to select specific areas where the phrase is located, especially if there's a chance that the phrase might occur in multiple locations in your document.</span></span>

<span data-ttu-id="59511-123">Si le respect de la casse est une exigence pour identifier votre étiquette, l’utilisation du type de liste d’expressions vous permet de le spécifier dans votre explication en cochant la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="59511-123">If case sensitivity is a requirement in identifying your label, using the phrase list type allows you to specify it in your explanation by selecting the **Only exact capitalization** checkbox.</span></span>

![Respect de la casse](../media/content-understanding/case-sensitivity.png)

<span data-ttu-id="59511-125">Un type de phrase est particulièrement utile lorsque vous créez une explication qui identifie et extraie des informations dans divers formats, telles que des dates, numéros de téléphone et de cartes bancaires.</span><span class="sxs-lookup"><span data-stu-id="59511-125">A phrase type is especially useful when you create an explanation that identifies and extracts information in different formats, such as dates, phone numbers, and credit card numbers.</span></span> <span data-ttu-id="59511-126">Par exemple, une date peut être affichée dans de nombreux formats différents (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020 ou 1 janvier 2020).</span><span class="sxs-lookup"><span data-stu-id="59511-126">For example, a date can be displayed in many different formats (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, or Jan 1,2020).</span></span> <span data-ttu-id="59511-127">La définition d’une liste de phrases rend votre explication plus efficace en capturant toutes les variations possibles dans les données que vous essayez d’identifier et d’extraire.</span><span class="sxs-lookup"><span data-stu-id="59511-127">Defining a phrase list makes your explanation more efficient by capturing any possible variations in the data that you're trying to identify and extract.</span></span>

<span data-ttu-id="59511-128">Pour l’exemple du *Numéro de téléphone*, vous extrayez le numéro de téléphone de chaque médecin traitant dans tous les documents de référence médicale que le modèle identifie.</span><span class="sxs-lookup"><span data-stu-id="59511-128">For the *phone number* example, you extract the phone number for each referring doctor from all Medical Referral documents that the model identifies.</span></span> <span data-ttu-id="59511-129">Lorsque vous créez l’explication, tapez les différents formats pouvant correspondre à un affichage de numéro de téléphone dans votre document de sorte que vous puissiez capturer les variations possibles.</span><span class="sxs-lookup"><span data-stu-id="59511-129">When you create the explanation, type the different formats a phone number might display in your document so that you're able to capture possible variations.</span></span>

![Modèles de phrase de numéro de téléphone](../media/content-understanding/pattern-list.png)

<span data-ttu-id="59511-131">Pour cet exemple, dans les **Paramètres avancés**, sélectionnez la case à cocher **N’importe quel chiffre de 0 à 9** pour identifier chaque valeur « 0 » utilisée dans votre liste de phrases comme un chiffre compris entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="59511-131">For this example, in **Advanced Settings** select the **Any digit from 0-9** checkbox to recognize each "0" value used in your phrase list to be any digit from 0 through 9.</span></span>

![Tous les chiffres de 0 à 9](../media/content-understanding/digit-identity.png)

<span data-ttu-id="59511-133">De même, si vous créez une liste de phrases qui contient des caractères texte, sélectionnez la case à cocher **Une lettre de a à z** pour que chaque caractère « a » utilisé dans la liste de phrases soit n’importe quel caractère de « a » à « z ».</span><span class="sxs-lookup"><span data-stu-id="59511-133">Similarly, if you create a phrase list that includes text characters, select the **Any letter from a-z** checkbox to recognize each "a" character used in the phrase list to be any character from "a" to "z".</span></span>

<span data-ttu-id="59511-134">Par exemple, si vous créez une liste de phrases **Date** et que vous souhaitez vous assurer qu’un format de date tel que *Jan 1, 2020* est reconnu, vous devez :</span><span class="sxs-lookup"><span data-stu-id="59511-134">For example, if you create a **Date** phrase list and you want to make sure that a date format such as *Jan 1, 2020* is recognized, you need to:</span></span>

- <span data-ttu-id="59511-135">ajouter *aaa 0, 0000* et *aaa 00, 0000* à votre liste de phrases.</span><span class="sxs-lookup"><span data-stu-id="59511-135">Add *aaa 0, 0000* and *aaa 00, 0000* to your phrase list.</span></span>
- <span data-ttu-id="59511-136">vous assurer que **Toutes les lettres de a à z** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-136">Make sure that **Any letter from a-z** is also selected.</span></span>

![Toutes les lettres de a à z](../media/content-understanding/any-letter.png)

<span data-ttu-id="59511-138">Si vous avez des exigences de mise en majuscule dans votre liste de phrases, vous pouvez cocher la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="59511-138">If you have capitalization requirements in your phrase list, you can select the **Only exact capitalization** checkbox.</span></span> <span data-ttu-id="59511-139">Pour l’exemple Date, si vous souhaitez que la première lettre du mois soit en majuscule, vous devez :</span><span class="sxs-lookup"><span data-stu-id="59511-139">For the date example, if you require the first letter of the month to be capitalized, you need to:</span></span>

- <span data-ttu-id="59511-140">ajouter *Aaa 0, 0000* et *Aaa 00, 0000* à votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="59511-140">Add *Aaa 0, 0000* and *Aaa 00, 0000* to your phrase list.</span></span>
- <span data-ttu-id="59511-141">vous assurer que **Seulement la mise en majuscule exacte** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-141">Make sure that **Only exact capitalization** is also selected.</span></span>

![Seulement la mise en majuscule exacte](../media/content-understanding/exact-caps.png)

> [!NOTE]
> <span data-ttu-id="59511-143">Au lieu de créer manuellement une explication de liste de phrases, utilisez la [bibliothèque d’explications](explanation-types-overview.md#use-explanation-templates) pour utiliser des modèles de liste de phrases pour une liste de phrases commune, comme les *dates*, *numéros de téléphone*, ou *numéro de carte bancaire*.</span><span class="sxs-lookup"><span data-stu-id="59511-143">Instead of manually creating a phrase list explanation, use the [explanation library](explanation-types-overview.md#use-explanation-templates) to use phrase list templates for a common phrase list, such as *date*, *phone number*, or *credit card number*.</span></span>

## <a name="regular-expression"></a><span data-ttu-id="59511-144">Expression régulière</span><span class="sxs-lookup"><span data-stu-id="59511-144">Regular expression</span></span>

<span data-ttu-id="59511-145">Un type d’explication d’expression régulière vous permet de créer des modèles qui permettent de rechercher et d’identifier certaines chaînes de texte dans des documents.</span><span class="sxs-lookup"><span data-stu-id="59511-145">A regular expression explanation type allows you to create patterns that help find and identify certain text strings in documents.</span></span> <span data-ttu-id="59511-146">Vous pouvez utiliser des expressions régulières pour analyser rapidement de grandes quantités de texte pour :</span><span class="sxs-lookup"><span data-stu-id="59511-146">You can use regular expressions to quickly parse large amounts of text to:</span></span>

- <span data-ttu-id="59511-147">Recherchez des modèles de caractères spécifiques.</span><span class="sxs-lookup"><span data-stu-id="59511-147">Find specific character patterns.</span></span>
- <span data-ttu-id="59511-148">Validez le texte pour vous assurer qu’il correspond à un modèle prédéfini (par exemple, une adresse e-mail).</span><span class="sxs-lookup"><span data-stu-id="59511-148">Validate text to ensure that it matches a predefined pattern (such as an email address).</span></span>
- <span data-ttu-id="59511-149">Extrayez, modifiez, remplacez ou supprimez des sous-chaînes de texte.</span><span class="sxs-lookup"><span data-stu-id="59511-149">Extract, edit, replace, or delete text substrings.</span></span>

<span data-ttu-id="59511-150">Un type d’expression régulière est particulièrement utile lorsque vous créez une explication qui identifie et extrait des informations dans des formats similaires, tels que des adresses e-mail, des numéros de compte bancaire ou des URL.</span><span class="sxs-lookup"><span data-stu-id="59511-150">A regular expression type is especially useful when you create an explanation that identifies and extracts information in similar formats, such as email addresses, bank account numbers, or URLs.</span></span> <span data-ttu-id="59511-151">Par exemple, une adresse e-mail, telle que megan@contoso.com, s’affiche dans un certain modèle (« megan » est la première partie et « com » est la dernière partie).</span><span class="sxs-lookup"><span data-stu-id="59511-151">For example, an email address, such as megan@contoso.com, is displayed in a certain pattern ("megan" is the first part, and "com" is the last part).</span></span>

<span data-ttu-id="59511-152">L’expression régulière d’une adresse e-mail est : **[A-Za-z0-9._%-]+@[A-Za-z0-9.-]+. [A-Za-z]{2,6}**.</span><span class="sxs-lookup"><span data-stu-id="59511-152">The regular expression for an email address is: **[A-Za-z0-9._%-]+@[A-Za-z0-9.-]+.[A-Za-z]{2,6}**.</span></span>

<span data-ttu-id="59511-153">Cette expression se compose de cinq parties, dans cet ordre :</span><span class="sxs-lookup"><span data-stu-id="59511-153">This expression consists of five parts, in this order:</span></span>

1. <span data-ttu-id="59511-154">Un des caractères spéciaux suivants :</span><span class="sxs-lookup"><span data-stu-id="59511-154">Any amount of the following characters:</span></span>

   <span data-ttu-id="59511-p112">a. Lettres de a à z</span><span class="sxs-lookup"><span data-stu-id="59511-p112">a. Letters from a to z</span></span>

   <span data-ttu-id="59511-p113">b. Chiffres entre 0 et 9</span><span class="sxs-lookup"><span data-stu-id="59511-p113">b. Numbers from 0-9</span></span>

   <span data-ttu-id="59511-p114">c. Point, trait de soulignement, pourcentage ou tiret</span><span class="sxs-lookup"><span data-stu-id="59511-p114">c. Period, underscore, percent, or dash</span></span>

2. <span data-ttu-id="59511-161">Le symbole @</span><span class="sxs-lookup"><span data-stu-id="59511-161">The @ symbol</span></span>

3. <span data-ttu-id="59511-162">Toute quantité des mêmes caractères que la première partie de l’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="59511-162">Any amount of the same characters as the first part of the email address</span></span>

4. <span data-ttu-id="59511-163">Un point</span><span class="sxs-lookup"><span data-stu-id="59511-163">A period</span></span>

5. <span data-ttu-id="59511-164">Deux à six lettres</span><span class="sxs-lookup"><span data-stu-id="59511-164">Two to six letters</span></span>

<span data-ttu-id="59511-165">Pour ajouter un type d’explication d’expression régulière :</span><span class="sxs-lookup"><span data-stu-id="59511-165">To add a regular expression explanation type:</span></span>

1. <span data-ttu-id="59511-166">Dans le panneau **Créer une explication** , sous **Type d’explication**, sélectionnez **Expression régulière**.</span><span class="sxs-lookup"><span data-stu-id="59511-166">From the **Create an explanation** panel, under **Explanation type**, select **Regular expression**.</span></span>

   ![Capture d’écran montrant le panneau Créer une explication avec l’expression régulière sélectionnée.](../media/content-understanding/create-regular-expression.png)

2. <span data-ttu-id="59511-168">Vous pouvez taper une expression dans la zone de texte **Expression régulière** ou sélectionner **Ajouter une expression régulière à partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="59511-168">You can either type an expression in the **Regular expression** text box or select **Add a regular expression from a template**.</span></span>

   <span data-ttu-id="59511-169">Lorsque vous ajoutez une expression régulière à l’aide d’un modèle, elle ajoute automatiquement le nom et l’expression régulière à la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="59511-169">When you add a regular expression by using a template, it automatically adds the name and the regular expression to the text box.</span></span> <span data-ttu-id="59511-170">Par exemple, si vous choisissez le modèle **Adresse e-mail**, le panneau **Créer une explication** est renseigné.</span><span class="sxs-lookup"><span data-stu-id="59511-170">For example, if you choose the **Email address** template, the **Create an explanation** panel will be populated.</span></span>

   ![Capture d’écran montrant le panneau Créer une explication avec le modèle d’adresse e-mail appliqué.](../media/content-understanding/create-regular-expression-email.png)

### <a name="limitations"></a><span data-ttu-id="59511-172">Limites</span><span class="sxs-lookup"><span data-stu-id="59511-172">Limitations</span></span>

<span data-ttu-id="59511-173">Le tableau suivant présente les options de caractères inline qui ne sont actuellement pas disponibles pour une utilisation dans les modèles d’expression régulière.</span><span class="sxs-lookup"><span data-stu-id="59511-173">The following table shows inline character options that currently are not available for use in regular expression patterns.</span></span>

|<span data-ttu-id="59511-174">Option</span><span class="sxs-lookup"><span data-stu-id="59511-174">Option</span></span>  |<span data-ttu-id="59511-175">État</span><span class="sxs-lookup"><span data-stu-id="59511-175">State</span></span>  |<span data-ttu-id="59511-176">Fonctionnalités actuelles</span><span class="sxs-lookup"><span data-stu-id="59511-176">Current functionality</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="59511-177">Respect de la casse</span><span class="sxs-lookup"><span data-stu-id="59511-177">Case sensitivity</span></span> | <span data-ttu-id="59511-178">Actuellement non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="59511-178">Currently not supported.</span></span> | <span data-ttu-id="59511-179">Toutes les correspondances effectuées ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="59511-179">All matches performed are case-insensitive.</span></span>  |
|<span data-ttu-id="59511-180">Ancres de ligne</span><span class="sxs-lookup"><span data-stu-id="59511-180">Line anchors</span></span>     | <span data-ttu-id="59511-181">Actuellement non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="59511-181">Currently not supported.</span></span> | <span data-ttu-id="59511-182">Impossible de spécifier une position spécifique dans une chaîne où une correspondance doit se produire.</span><span class="sxs-lookup"><span data-stu-id="59511-182">Unable to specify a specific position in a string where a match must occur.</span></span>   |

## <a name="proximity"></a><span data-ttu-id="59511-183">Proximité</span><span class="sxs-lookup"><span data-stu-id="59511-183">Proximity</span></span>

<span data-ttu-id="59511-184">Le type d’explication de proximité aide votre modèle à identifier les données en définissant la proximité d’un autre élément de données.</span><span class="sxs-lookup"><span data-stu-id="59511-184">The proximity explanation type helps your model identify data by defining how close another piece of data is to it.</span></span> <span data-ttu-id="59511-185">Par exemple, dans votre modèle, vous avez défini deux explications qui étiquettent à la fois le *Numéro d’adresse* et le *Numéro de téléphone* du client.</span><span class="sxs-lookup"><span data-stu-id="59511-185">For example, in your model say you have defined two explanations that label both the customer *street address number* and *phone number*.</span></span>

<span data-ttu-id="59511-186">Remarquez également que les numéros de téléphone des clients apparaissent toujours avant le numéro de l’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="59511-186">Notice that customer phone numbers always appear before the street address number.</span></span>

<span data-ttu-id="59511-187">Alain Chauvin</span><span class="sxs-lookup"><span data-stu-id="59511-187">Alex Wilburn</span></span><br>
<span data-ttu-id="59511-188">555-555-5555</span><span class="sxs-lookup"><span data-stu-id="59511-188">555-555-5555</span></span><br>
<span data-ttu-id="59511-189">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="59511-189">One Microsoft Way</span></span><br>
<span data-ttu-id="59511-190">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="59511-190">Redmond, WA 98034</span></span><br>

<span data-ttu-id="59511-191">Utilisez l’explication de proximité pour définir la distance de l’explication du numéro de téléphone afin de mieux identifier le numéro de l’adresse postale dans vos documents.</span><span class="sxs-lookup"><span data-stu-id="59511-191">Use the proximity explanation to define how far away the phone number explanation is to better identify the street address number in your documents.</span></span>

![Explication de proximité](../media/content-understanding/proximity.png)

#### <a name="what-are-tokens"></a><span data-ttu-id="59511-193">Que sont les jetons ?</span><span class="sxs-lookup"><span data-stu-id="59511-193">What are tokens?</span></span>

<span data-ttu-id="59511-194">Pour utiliser le type d’explication de proximité, vous devez comprendre ce qu’est un jeton.</span><span class="sxs-lookup"><span data-stu-id="59511-194">To use the proximity explanation type, you need to understand what a token is.</span></span> <span data-ttu-id="59511-195">Le nombre de jetons est la façon dont l'explication de proximité mesure la distance d'une explication à une autre.</span><span class="sxs-lookup"><span data-stu-id="59511-195">The number of tokens is how the proximity explanation measures distance from one explanation to another.</span></span> <span data-ttu-id="59511-196">Un jeton est une étendue continue (non compris les espaces et la ponctuation) de lettres et de chiffres.</span><span class="sxs-lookup"><span data-stu-id="59511-196">A token is a continuous span (not including spaces or punctuation) of letters and numbers.</span></span>

<span data-ttu-id="59511-197">Le tableau suivant illustre des exemples sur la façon de déterminer le nombre de jetons dans une expression.</span><span class="sxs-lookup"><span data-stu-id="59511-197">The following table shows examples for how to determine the number of tokens in a phrase.</span></span>

|<span data-ttu-id="59511-198">Expression</span><span class="sxs-lookup"><span data-stu-id="59511-198">Phrase</span></span>|<span data-ttu-id="59511-199">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="59511-199">Number of tokens</span></span>|<span data-ttu-id="59511-200">Explication</span><span class="sxs-lookup"><span data-stu-id="59511-200">Explanation</span></span>|
|--|--|--|
|`Dog`|<span data-ttu-id="59511-201">1</span><span class="sxs-lookup"><span data-stu-id="59511-201">1</span></span>|<span data-ttu-id="59511-202">Un seul mot sans ponctuation ni espaces.</span><span class="sxs-lookup"><span data-stu-id="59511-202">A single word with no punctuation or spaces.</span></span>|
|`RMT33W`|<span data-ttu-id="59511-203">1</span><span class="sxs-lookup"><span data-stu-id="59511-203">1</span></span>|<span data-ttu-id="59511-p118">Numéro de localisateur d’enregistrement. Il peut inclure des chiffres et des lettres, mais n’a pas de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="59511-p118">A record locator number. It might include numbers and letters, but doesn't have punctuation.</span></span>|
|`425-555-5555`|<span data-ttu-id="59511-206">5</span><span class="sxs-lookup"><span data-stu-id="59511-206">5</span></span>|<span data-ttu-id="59511-207">Un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="59511-207">A phone number.</span></span> <span data-ttu-id="59511-208">Chaque signe de ponctuation équivaut à un seul jeton, donc `425-555-5555` correspond à 5 jetons :</span><span class="sxs-lookup"><span data-stu-id="59511-208">Each punctuation mark is a single token, so `425-555-5555` is 5 tokens:</span></span><br>`425`<br>`-`<br>`555`<br>`-`<br>`5555` |
|`https://luis.ai`|<span data-ttu-id="59511-209">7</span><span class="sxs-lookup"><span data-stu-id="59511-209">7</span></span>|`https`<br>`:`<br>`/`<br>`/`<br>`luis`<br>`.`<br>`ai`<br>|

#### <a name="configure-the-proximity-explanation-type"></a><span data-ttu-id="59511-210">Configurer le type d’explication de proximité</span><span class="sxs-lookup"><span data-stu-id="59511-210">Configure the proximity explanation type</span></span>

<span data-ttu-id="59511-211">Pour l’exemple, configurez le paramètre de proximité pour définir la plage du nombre de jetons. L’explication dans le *Numéro de téléphone* provient de l’explication du *Numéro d’adresse*.</span><span class="sxs-lookup"><span data-stu-id="59511-211">For the example, configure the proximity setting to define the range of the number of tokens in the *phone number* explanation from the *street address number* explanation.</span></span> <span data-ttu-id="59511-212">Remarquez que la plage minimale est « 0 » car il n’y a pas de jetons entre le numéro de téléphone et le numéro d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="59511-212">Notice that the minimum range is "0", because there are no tokens between the phone number and street address number.</span></span>

<span data-ttu-id="59511-213">Certains numéros de téléphone dans les exemples de documents sont toutefois ajoutés avec un *(mobile)*.</span><span class="sxs-lookup"><span data-stu-id="59511-213">But some phone numbers in the sample documents are appended with *(mobile)*.</span></span>

<span data-ttu-id="59511-214">Maurice Boule</span><span class="sxs-lookup"><span data-stu-id="59511-214">Nestor Wilke</span></span><br>
<span data-ttu-id="59511-215">111-111-1111 (mobile)</span><span class="sxs-lookup"><span data-stu-id="59511-215">111-111-1111 (mobile)</span></span><br>
<span data-ttu-id="59511-216">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="59511-216">One Microsoft Way</span></span><br>
<span data-ttu-id="59511-217">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="59511-217">Redmond, WA 98034</span></span><br>

<span data-ttu-id="59511-218">Il y a trois jetons dans *(mobile)* :</span><span class="sxs-lookup"><span data-stu-id="59511-218">There are three tokens in *(mobile)*:</span></span>

|<span data-ttu-id="59511-219">Expression</span><span class="sxs-lookup"><span data-stu-id="59511-219">Phrase</span></span>|<span data-ttu-id="59511-220">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="59511-220">Token count</span></span>|
|--|--|
|<span data-ttu-id="59511-221">(</span><span class="sxs-lookup"><span data-stu-id="59511-221">(</span></span>|<span data-ttu-id="59511-222">1</span><span class="sxs-lookup"><span data-stu-id="59511-222">1</span></span>|
|<span data-ttu-id="59511-223">mobile</span><span class="sxs-lookup"><span data-stu-id="59511-223">mobile</span></span>|<span data-ttu-id="59511-224">2</span><span class="sxs-lookup"><span data-stu-id="59511-224">2</span></span>|
|<span data-ttu-id="59511-225">)</span><span class="sxs-lookup"><span data-stu-id="59511-225">)</span></span>|<span data-ttu-id="59511-226">3</span><span class="sxs-lookup"><span data-stu-id="59511-226">3</span></span>|

<span data-ttu-id="59511-227">Configurez le paramètre de proximité pour avoir une plage de 0 à 3.</span><span class="sxs-lookup"><span data-stu-id="59511-227">Configure the proximity setting to have a range of 0 through 3.</span></span>

![Exemple de proximité](../media/content-understanding/proximity-example.png)

## <a name="configure-where-phrases-occur-in-the-document"></a><span data-ttu-id="59511-229">Configurer l’endroit où des phrases apparaissent dans le document</span><span class="sxs-lookup"><span data-stu-id="59511-229">Configure where phrases occur in the document</span></span>

<span data-ttu-id="59511-230">Lorsque vous créez une explication, par défaut, l’ensemble du document est recherché à la recherche de l’expression que vous essayez d’extraire.</span><span class="sxs-lookup"><span data-stu-id="59511-230">When you create an explanation, by default the entire document is searched for the phrase you're trying to extract.</span></span> <span data-ttu-id="59511-231">Toutefois, vous pouvez utiliser le **Où ces expressions se produisent** paramètre avancé pour vous aider à isoler un emplacement spécifique dans le document où se produit une expression.</span><span class="sxs-lookup"><span data-stu-id="59511-231">However, you can use the **Where these phrases occur** advanced setting to help in isolating a specific location in the document that a phrase occurs.</span></span> <span data-ttu-id="59511-232">Ce paramètre est utile dans les situations où des instances similaires d’une expression peuvent apparaître à un autre endroit dans le document et dont vous voulez vous assurer que celle qui est correcte est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-232">This setting is useful in situations where similar instances of a phrase might appear somewhere else in the document, and you want to make sure that the correct one is selected.</span></span>

<span data-ttu-id="59511-233">En référence à notre exemple de document de référence médical, la *Référence médecin* est toujours mentionnée dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="59511-233">Referring to our Medical Referral document example, the *referring doctor* is always mentioned in the first paragraph of the document.</span></span> <span data-ttu-id="59511-234">Avec le paramètre **Où ces expressions se produisent**, dans cet exemple, vous pouvez configurer votre explication pour rechercher cette étiquette uniquement dans la section de début du document ou dans tout autre emplacement où elle pourrait se produire.</span><span class="sxs-lookup"><span data-stu-id="59511-234">With the **Where these phrases occur** setting, in this example you can configure your explanation to search for this label only in the beginning section of the document, or any other location in which it might occur.</span></span>

![Paramètre où ces phrases se produisent](../media/content-understanding/phrase-location.png)

<span data-ttu-id="59511-236">Vous pouvez choisir l'une des trois options suivantes :</span><span class="sxs-lookup"><span data-stu-id="59511-236">You can choose the following options for this setting:</span></span>

- <span data-ttu-id="59511-237">N’importe où dans le fichier : recherche l’expression dans l’ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="59511-237">Anywhere in the file: The entire document is searched for the phrase.</span></span>

- <span data-ttu-id="59511-238">Début du fichier : La recherche s’effectuera du début jusqu’à l’emplacement des expressions.</span><span class="sxs-lookup"><span data-stu-id="59511-238">Beginning of the file:  The document is searched from the beginning to the phrase location.</span></span>

   ![Début du fichier](../media/content-understanding/beginning-of-file.png)

    <span data-ttu-id="59511-240">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="59511-240">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="59511-241">La valeur **Position de fin** est mise à jour de manière à afficher le nombre de jetons inclus dans la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-241">The **End position** value will update to show the number of tokens your selected area includes.</span></span> <span data-ttu-id="59511-242">Vous pouvez également mettre à jour la valeur de **Position de fin** pour ajuster la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-242">You can update the **End position** value as well to adjust the selected area.</span></span>

   ![Zone Début de la position du fichier](../media/content-understanding/beginning-box.png)

- <span data-ttu-id="59511-244">Fin du fichier : La recherche s’effectuera de la fin jusqu’à l’emplacement des expressions.</span><span class="sxs-lookup"><span data-stu-id="59511-244">End of the file: The document is searched from the end to the phrase location.</span></span>

   ![Fin du fichier](../media/content-understanding/end-of-file.png)

    <span data-ttu-id="59511-246">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="59511-246">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="59511-247">La valeur **Position de début** est mise à jour de manière à afficher le nombre de jetons inclus dans la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-247">The **Starting position** value will update to show the number of tokens your selected area includes.</span></span> <span data-ttu-id="59511-248">Vous pouvez également mettre à jour la valeur de position de début pour ajuster la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="59511-248">You can update the Starting position value as well to adjust the selected area.</span></span>

   ![Zone Fin de fichier](../media/content-understanding/end-box.png)

- <span data-ttu-id="59511-250">Plage personnalisée : recherche l’emplacement de l’expression dans une plage spécifiée du document.</span><span class="sxs-lookup"><span data-stu-id="59511-250">Custom range: The document is searched within a specified range for the phrase location.</span></span>

   ![Plage personnalisée.](../media/content-understanding/custom-file.png)

    <span data-ttu-id="59511-252">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="59511-252">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="59511-253">Pour ce paramètre, vous devez sélectionner une position de **Début** et une position de **Fin**.</span><span class="sxs-lookup"><span data-stu-id="59511-253">For this setting, you need to select a **Start** and an **End** position.</span></span> <span data-ttu-id="59511-254">Ces valeurs représentent le nombre de jetons dès le début du document.</span><span class="sxs-lookup"><span data-stu-id="59511-254">These values represent the number of tokens from the beginning of the document.</span></span> <span data-ttu-id="59511-255">Bien que vous pouvez entrer manuellement ces valeurs, il est plus facile d’ajuster manuellement la case à sélectionner dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="59511-255">While you can manually enter in these values, it's easier to manually adjust the select box in the viewer.</span></span>

## <a name="use-explanation-templates"></a><span data-ttu-id="59511-256">Utiliser des modèles d’explication</span><span class="sxs-lookup"><span data-stu-id="59511-256">Use explanation templates</span></span>

<span data-ttu-id="59511-257">Bien que vous puissiez ajouter manuellement différentes valeurs de liste d'expressions pour votre explication, il peut être plus facile d’utiliser les modèles qui vous sont fournis dans la bibliothèque d’explications.</span><span class="sxs-lookup"><span data-stu-id="59511-257">While you can manually add various phrase list values for your explanation, it can be easier to use the templates provided to you in the explanation library.</span></span>

<span data-ttu-id="59511-258">Par exemple, au lieu d’ajouter manuellement toutes les variantes de *Date*, vous pouvez utiliser le modèle de liste d’expressions pour *Date*, car il comprend déjà de nombreuses valeurs de listes d’expressions :</span><span class="sxs-lookup"><span data-stu-id="59511-258">For example, instead of manually adding all the variations for *date*, you can use the phrase list template for *date* because it already includes many phrase lists values:</span></span>

![Bibliothèque d’explications](../media/content-understanding/explanation-template.png)

<span data-ttu-id="59511-260">La bibliothèque d’explications comprend des explications de *liste d’expressions* couramment utilisées, notamment :</span><span class="sxs-lookup"><span data-stu-id="59511-260">The explanation library includes commonly used *phrase list* explanations, including:</span></span>

- <span data-ttu-id="59511-261">Date : Dates du calendrier, tous les formats.</span><span class="sxs-lookup"><span data-stu-id="59511-261">Date: Calendar dates, all formats.</span></span> <span data-ttu-id="59511-262">Inclut du texte et des chiffres (par exemple, « 9 décembre 2020 »).</span><span class="sxs-lookup"><span data-stu-id="59511-262">Includes text and numbers (for example, "Dec 9, 2020").</span></span>
- <span data-ttu-id="59511-263">Date (numérique) : Dates du calendrier, tous les formats.</span><span class="sxs-lookup"><span data-stu-id="59511-263">Date (numeric): Calendar dates, all formats.</span></span> <span data-ttu-id="59511-264">Inclut les numéros (par exemple 1-11-2020).</span><span class="sxs-lookup"><span data-stu-id="59511-264">Includes numbers (for example, 1-11-2020).</span></span>
- <span data-ttu-id="59511-265">Heure : formats 12 et 24 heures.</span><span class="sxs-lookup"><span data-stu-id="59511-265">Time: 12 and 24 hour formats.</span></span>
- <span data-ttu-id="59511-266">Nombre : Nombres positifs et négatifs jusqu'à deux décimales.</span><span class="sxs-lookup"><span data-stu-id="59511-266">Number: Positive and negative numbers up to two decimals.</span></span>
- <span data-ttu-id="59511-267">Pourcentage : Une liste de motifs représentant un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="59511-267">Percentage: A list of patterns representing a percentage.</span></span> <span data-ttu-id="59511-268">Par exemple : 1%, 11%, 100%, ou 11.11%.</span><span class="sxs-lookup"><span data-stu-id="59511-268">For example, 1%, 11%, 100%, or 11.11%.</span></span>
- <span data-ttu-id="59511-269">Numéro de téléphone : Formats américains et internationaux courants.</span><span class="sxs-lookup"><span data-stu-id="59511-269">Phone number: Common US and International formats.</span></span> <span data-ttu-id="59511-270">Par exemple, 000 000 0000, 000-000-0000, (000)000-0000, ou (000) 000-0000.</span><span class="sxs-lookup"><span data-stu-id="59511-270">For example, 000 000 0000, 000-000-0000, (000)000-0000, or (000) 000-0000.</span></span>
- <span data-ttu-id="59511-271">Code postal : Formats de code postal américain.</span><span class="sxs-lookup"><span data-stu-id="59511-271">Zip code: US Zip code formats.</span></span> <span data-ttu-id="59511-272">Par exemple, 11111, 11111-1111.</span><span class="sxs-lookup"><span data-stu-id="59511-272">For example, 11111, 11111-1111.</span></span>
- <span data-ttu-id="59511-273">Premier mot de la phrase : Modèles courants pour les mots jusqu'à neuf caractères.</span><span class="sxs-lookup"><span data-stu-id="59511-273">First word of sentence: Common patterns for words up to nine characters.</span></span>
- <span data-ttu-id="59511-274">Fin de phrase : Ponctuation courante pour la fin d'une phrase.</span><span class="sxs-lookup"><span data-stu-id="59511-274">End of sentence: Common punctuation for end of a sentence.</span></span>
- <span data-ttu-id="59511-275">Carte de crédit : Formats courants de numéros de cartes de crédit.</span><span class="sxs-lookup"><span data-stu-id="59511-275">Credit card: Common credit card number formats.</span></span> <span data-ttu-id="59511-276">Par exemple, 1111-1111-1111-1111.</span><span class="sxs-lookup"><span data-stu-id="59511-276">For example, 1111-1111-1111-1111.</span></span>
- <span data-ttu-id="59511-p132">Numéro de sécurité sociale : Format du numéro de sécurité sociale américain. Par exemple, 111-11-1111.</span><span class="sxs-lookup"><span data-stu-id="59511-p132">Social security number: US Social Security Number format. For example, 111-11-1111.</span></span>
- <span data-ttu-id="59511-279">Case à cocher : Une liste de phrases représentant des variations d'une case à cocher remplie.</span><span class="sxs-lookup"><span data-stu-id="59511-279">Checkbox: A phrase list representing variations on a filled in checkbox.</span></span> <span data-ttu-id="59511-280">Par exemple, _X_, _ _X_.</span><span class="sxs-lookup"><span data-stu-id="59511-280">For example, _X_, _ _X_.</span></span>
- <span data-ttu-id="59511-281">La monnaie : Principaux symboles internationaux.</span><span class="sxs-lookup"><span data-stu-id="59511-281">Currency: Major international symbols.</span></span> <span data-ttu-id="59511-282">Par exemple, $.</span><span class="sxs-lookup"><span data-stu-id="59511-282">For example, $.</span></span>
- <span data-ttu-id="59511-283">E-mail CC : Une liste de phrases avec le terme « CC : », que l'on trouve souvent près des noms ou des adresses e-mail de personnes ou des autres groupes auxquels le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="59511-283">Email CC: A phrase list with the term 'CC:', often found near the names or email addresses of other people or groups the message was sent to.</span></span>
- <span data-ttu-id="59511-284">Date de l' e-mail : Une liste de phrases avec le terme « Envoyé le :», qui se trouve souvent près de la date d'envoi de l' e-mail.</span><span class="sxs-lookup"><span data-stu-id="59511-284">Email date: A phrase list with the term 'Sent on:', often found near the date the email was sent.</span></span>
- <span data-ttu-id="59511-285">Message d'accueil par e-mail : Lignes d'ouverture courantes pour les e-mails.</span><span class="sxs-lookup"><span data-stu-id="59511-285">Email greeting: Common opening lines for emails.</span></span>
- <span data-ttu-id="59511-286">Destinataire de l' e-mail : Une liste de phrases avec le terme « À :», que l'on trouve souvent près des noms ou des adresses e-mail des personnes ou des groupes auxquels le message a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="59511-286">Email recipient: A phrase list with the term 'To:', often found near the names or email addresses of people or groups the message was sent to.</span></span>
- <span data-ttu-id="59511-287">Expéditeur de l' email : Une liste de phrases avec le terme « De : », que l'on trouve souvent près du nom ou de l'adresse électronique de l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="59511-287">Email sender: A phrase list with the term 'From:', often found near the sender's name or email address.</span></span>
- <span data-ttu-id="59511-288">Objet de l' e-mail : Une liste de phrases avec le terme « Objet : », qui se trouve souvent près de l'objet de l' e-mail.</span><span class="sxs-lookup"><span data-stu-id="59511-288">Email subject: A phrase list with the term 'Subject:', often found near the email's subject.</span></span>

<span data-ttu-id="59511-289">La bibliothèque d’explications inclut également des explications *expression régulière* couramment utilisées, notamment :</span><span class="sxs-lookup"><span data-stu-id="59511-289">The explanation library also includes commonly used *regular expression* explanations, including:</span></span>

- <span data-ttu-id="59511-290">Nombres de 6 à 17 chiffres : correspond à un nombre compris entre 6 et 17 chiffres.</span><span class="sxs-lookup"><span data-stu-id="59511-290">6 to 17 digit numbers: Matches any number from 6 to 17 digits long.</span></span> <span data-ttu-id="59511-291">Les numéros de compte bancaire américain correspondent à ce modèle.</span><span class="sxs-lookup"><span data-stu-id="59511-291">US bank account numbers fit this pattern.</span></span>
- <span data-ttu-id="59511-292">Adresse e-mail : correspond à un type commun d’adresse de messagerie telle que meganb@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="59511-292">Email address: Matches a common type of email address like meganb@contoso.com.</span></span>
- <span data-ttu-id="59511-293">Numéro d’identification du contribuable américain : correspond à un nombre à trois chiffres commençant par 9 suivi d’un numéro à 6 chiffres commençant par 7 ou 8</span><span class="sxs-lookup"><span data-stu-id="59511-293">US taxpayer ID number: Matches a three-digit number starting with 9 followed by a 6 digit number starting with 7 or 8.</span></span>
- <span data-ttu-id="59511-294">Adresse web (URL) : correspond au format d’une adresse web, en commençant par http:// ou https://.</span><span class="sxs-lookup"><span data-stu-id="59511-294">Web address (URL): Matches the format of a web address, starting with http:// or https://.</span></span>

<span data-ttu-id="59511-295">En outre, la bibliothèque d’explications inclut trois types de modèles automatiques qui fonctionnent avec les données que vous avez étiquetées dans vos exemples de fichiers :</span><span class="sxs-lookup"><span data-stu-id="59511-295">In addition, the explanation library includes three automatic template types that work with the data you've labeled in your example files:</span></span>

- <span data-ttu-id="59511-296">Après l’étiquette : mots ou caractères qui apparaissent après les étiquettes dans les exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="59511-296">After label: The words or characters that occur after the labels in the example files.</span></span>
- <span data-ttu-id="59511-297">Après l’étiquette : mots ou caractères qui apparaissent avant les étiquettes dans les exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="59511-297">Before label: The words or characters that occur before the labels in the example files.</span></span>
- <span data-ttu-id="59511-298">Étiquettes : jusqu’aux 10 premières étiquettes des exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="59511-298">Labels: Up to the first 10 labels from the example files.</span></span>

<span data-ttu-id="59511-299">Pour vous donner un exemple du fonctionnement des modèles automatiques, dans l’exemple de fichier suivant, nous allons utiliser le modèle d’explication avant étiquette pour fournir au modèle plus d’informations pour obtenir une correspondance plus précise.</span><span class="sxs-lookup"><span data-stu-id="59511-299">To give you an example of how automatic templates work, in the following example file, we'll use the Before label explanation template to help give the model more information to get a more accurate match.</span></span>

![Options de sélecteur de fichiers exemple](../media/content-understanding/before-label.png)

<span data-ttu-id="59511-301">Lorsque vous sélectionnez le modèle d’explication Avant étiquette, il recherche le premier jeu de mots qui apparaît avant l’étiquette dans vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="59511-301">When you select the Before label explanation template, it will look for the first set of words that appear before the label in your example files.</span></span> <span data-ttu-id="59511-302">Dans l’exemple, les mots identifiés dans le premier exemple de fichier sont « En tant que ».</span><span class="sxs-lookup"><span data-stu-id="59511-302">In the example, the words that are identified in the first example file is "As of".</span></span>

![Modèle Avant d’étiquette](../media/content-understanding/before-label-explanation.png)

<span data-ttu-id="59511-304">Vous pouvez sélectionner **Ajouter** pour créer une explication à partir du modèle.</span><span class="sxs-lookup"><span data-stu-id="59511-304">You can select **Add** to create an explanation from the template.</span></span>  <span data-ttu-id="59511-305">À mesure que vous ajoutez d’autres exemples de fichiers, des mots supplémentaires sont identifiés et ajoutés à la liste des expressions.</span><span class="sxs-lookup"><span data-stu-id="59511-305">As you add more example files, additional words will be identified and added to the phrase list.</span></span>

![Ajouter l'étiquette](../media/content-understanding/before-label-add.png)

#### <a name="to-use-a-template-from-the-explanation-library"></a><span data-ttu-id="59511-307">Pour utiliser un modèle de la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="59511-307">To use a template from the explanation library</span></span>

1. <span data-ttu-id="59511-308">Dans la section **Explications** de la page **Entraîner** de votre modèle, sélectionnez **Nouveau**, puis **À partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="59511-308">From the **Explanations** section of your model's **Train** page, select **New**, then select **From a template**.</span></span>

   ![Ajouter Avant l’étiquette](../media/content-understanding/from-template.png)

2.  <span data-ttu-id="59511-310">Sur la page **Modèles d’explication**, sélectionnez l’explication que vous souhaitez utiliser, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="59511-310">On the **Explanation templates** page, select the explanation you want to use, then select **Add**.</span></span>

    ![Sélectionner un modèle](../media/content-understanding/phone-template.png)

3. <span data-ttu-id="59511-312">Les informations relatives au modèle que vous avez sélectionné s’affichent sur la page **Créer une explication**.</span><span class="sxs-lookup"><span data-stu-id="59511-312">The information for the template you selected displays on the **Create an explanation** page.</span></span> <span data-ttu-id="59511-313">Si nécessaire, modifiez le nom de l’explication et ajoutez ou supprimez des éléments de la liste d’expressions.</span><span class="sxs-lookup"><span data-stu-id="59511-313">If needed, edit the explanation name and add or remove items from the phrase list.</span></span>

    ![Modifier le modèle](../media/content-understanding/phone-template-live.png)

4. <span data-ttu-id="59511-315">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59511-315">When finished, select **Save**.</span></span>