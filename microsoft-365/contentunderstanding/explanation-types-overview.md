---
title: Types d’explication
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: En savoir plus sur les types d’explications dans Microsoft SharePoint Syntex
ms.openlocfilehash: 2c2997fd165339cc43f7f007050f343794021a23
ms.sourcegitcommit: d354727303d9574991b5a0fd298d2c9414e19f6c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "50080589"
---
# <a name="introduction-to-explanation-types"></a><span data-ttu-id="7345e-103">Introduction aux types d’explications</span><span class="sxs-lookup"><span data-stu-id="7345e-103">Introduction to explanation types</span></span>

<span data-ttu-id="7345e-104">Les explications sont utilisées pour vous permettre de définir les informations que vous souhaitez étiqueter et extraire dans vos modèles de compréhension de documents dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="7345e-104">Explanations are used to help to define the information you want to label and extract in your document understanding models in Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="7345e-105">Lors de la création d’une explication, vous devez sélectionner un type d’explication.</span><span class="sxs-lookup"><span data-stu-id="7345e-105">When creating an explanation, you need to select an explanation type.</span></span> <span data-ttu-id="7345e-106">Cet article vous permet de comprendre les différents types d’explications et comment ils sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="7345e-106">This article helps you understand the different explanation types and how they are used.</span></span> 

   ![Types d’explication](../media/content-understanding/explanation-types.png) 
   
<span data-ttu-id="7345e-108">Les types d’explications suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="7345e-108">These explanation types are available:</span></span>

- <span data-ttu-id="7345e-109">**Liste d’expressions** : liste de mots, expressions, nombres ou autres caractères que vous pouvez utiliser dans le document ou les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="7345e-109">**Phrase list**: List of words, phrases, numbers, or other characters you can use in the document or information that you are extracting.</span></span> <span data-ttu-id="7345e-110">Par exemple, la chaîne de texte **Médecin référent** se trouve dans tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="7345e-110">For example, the text string **Referring Doctor** is in all Medical Referral documents you are identifying.</span></span></br>

- <span data-ttu-id="7345e-111">**Liste de modèles** : répertorie les modèles de chiffres, de lettres ou d’autres caractères que vous pouvez utiliser pour identifier les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="7345e-111">**Pattern list**: List patterns of numbers, letters, or other characters that you can use to identify the information that you are extracting.</span></span> <span data-ttu-id="7345e-112">Par exemple, vous pouvez extraire le **numéro de téléphone** du médecin référent de tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="7345e-112">For example, you can extract the **Phone number** of the referring doctor from all Medical Referral document that you are identifying.</span></span></br>

- <span data-ttu-id="7345e-113">**Proximité** : décrit à quel point les explications sont proches les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="7345e-113">**Proximity**: Describes how close explanations are to each other.</span></span> <span data-ttu-id="7345e-114">Par exemple, une liste de modèles de *numéros de rue* se trouve juste avant la liste d’expressions des *noms de rue*, sans jetons entre les deux (vous en apprendrez davantage sur les jetons plus loin dans cet article).</span><span class="sxs-lookup"><span data-stu-id="7345e-114">For example, a *street number* pattern list goes right before the *street name* phrase list, with no tokens in between (you'll learn about tokens later in this article).</span></span> <span data-ttu-id="7345e-115">L’utilisation du type de proximité nécessite que vous ayez au moins deux explications dans votre modèle. Dans le cas contraire, l’option sera désactivée.</span><span class="sxs-lookup"><span data-stu-id="7345e-115">Using the proximity type requires you to have at least two explanations in your model or the option will be disabled.</span></span> 
 
## <a name="phrase-list"></a><span data-ttu-id="7345e-116">Liste d’expressions</span><span class="sxs-lookup"><span data-stu-id="7345e-116">Phrase list</span></span>

<span data-ttu-id="7345e-117">Un type d’explication de liste d’expressions est généralement utilisé pour identifier et classer un document dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="7345e-117">A phrase list explanation type is typically used to identify and classify a document through your model.</span></span> <span data-ttu-id="7345e-118">Comme décrit dans l’exemple d’étiquette *Médecin référent*, il s’agit d’une chaîne de mots, d’expressions, de nombres ou de caractères qui se trouve systématiquement dans les documents que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="7345e-118">As described in the *Referring Doctor* label example, it is a string of words, phrases, numbers, or characters that is consistently in the documents that you are identifying.</span></span>

<span data-ttu-id="7345e-119">Bien que ce ne soit pas obligatoire, vous pouvez améliorer les performances de votre explication si l’expression que vous capturez se trouve à un emplacement cohérent dans votre document.</span><span class="sxs-lookup"><span data-stu-id="7345e-119">While not a requirement, you can achieve better success with your explanation if the phrase you are capturing is located in a consistent location in your document.</span></span> <span data-ttu-id="7345e-120">Par exemple, l’étiquette *Médecin référent* peut être située systématiquement dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="7345e-120">For example, the *Referring Doctor* label may be consistently located in the first paragraph of the document.</span></span>

<span data-ttu-id="7345e-121">Si le respect de la casse est une exigence pour identifier votre étiquette, l’utilisation du type de liste d’expressions vous permet de le spécifier dans votre explication en cochant la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="7345e-121">If case sensitivity is a requirement in identifying your label, using the phrase list type allows you to specify it in your explanation by selecting the **Only exact capitalization** checkbox.</span></span>

   ![Respect de la casse](../media/content-understanding/case-sensitivity.png) 

## <a name="pattern-lists"></a><span data-ttu-id="7345e-123">Listes de modèles</span><span class="sxs-lookup"><span data-stu-id="7345e-123">Pattern lists</span></span>

<span data-ttu-id="7345e-124">Un type de liste de modèles est particulièrement utile lorsque vous créez une explication qui identifie et extrait des informations d’un document.</span><span class="sxs-lookup"><span data-stu-id="7345e-124">A pattern list type is especially useful when you create an explanation that identifies and extracts information from a document.</span></span> <span data-ttu-id="7345e-125">Il est généralement présenté dans différents formats, tels que des dates, des numéros de téléphone et des numéros de carte bancaire.</span><span class="sxs-lookup"><span data-stu-id="7345e-125">It is typically presented in different formats, such as dates, phone numbers, and credit card numbers.</span></span> <span data-ttu-id="7345e-126">Par exemple, une date peut être affichée dans plusieurs formats différents (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, 1 janvier 2020, etc.).</span><span class="sxs-lookup"><span data-stu-id="7345e-126">For example, a date can be displayed in a number of different formats (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, Jan 1,2020, etc.).</span></span> <span data-ttu-id="7345e-127">La définition d’une liste de modèles rend votre explication plus efficace en capturant toutes les variations possibles dans les données que vous essayez d’identifier et d’extraire.</span><span class="sxs-lookup"><span data-stu-id="7345e-127">Defining a pattern list makes your explanation more efficient by capturing any possible variations in the data that you are trying to identify and extract.</span></span> 

<span data-ttu-id="7345e-128">Pour l’exemple du **numéro de téléphone**, vous extrayez le numéro de téléphone de chaque médecin traitant dans tous les documents de référence médicale que le modèle identifie.</span><span class="sxs-lookup"><span data-stu-id="7345e-128">For the **Phone number** example, you extract the phone number for each referring doctor from all Medical Referral documents that the model identifies.</span></span> <span data-ttu-id="7345e-129">Lorsque vous créez l’explication, sélectionnez le type de liste de modèles pour autoriser les différents formats que vous pouvez vous attendre à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="7345e-129">When you create the explanation, select the Pattern list type to allow the different formats that you may expect to be returned.</span></span>

   ![Liste de modèles de numéros de téléphone](../media/content-understanding/pattern-list.png)

<span data-ttu-id="7345e-131">Pour cet exemple, activez la case à cocher **N’importe quel chiffre de 0 à 9** pour identifier chaque valeur « 0 » utilisée dans votre liste de modèles comme un chiffre compris entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="7345e-131">For this example, select the **Any digit from 0-9** checkbox to recognize each "0" value used in your pattern list to be any digit from 0 through 9.</span></span>

   ![Tous les chiffres de 0 à 9](../media/content-understanding/digit-identity.png)

<span data-ttu-id="7345e-133">De même, si vous créez une liste de modèles qui contient des caractères texte, sélectionnez la case à cocher **Une lettre de a à z** pour que chaque caractère « a » utilisé dans la liste de modèles soit n’importe quel caractère de « a » à « z ».</span><span class="sxs-lookup"><span data-stu-id="7345e-133">Similarly, if you create a pattern list that includes text characters, select the **Any letter from a-z** checkbox to recognize each "a" character used in the pattern list to be any character from "a" to "z".</span></span>

<span data-ttu-id="7345e-134">Par exemple, si vous créez une liste de modèles **Date** et que vous souhaitez vous assurer qu’un format de date tel que *Jan 1, 2020* est reconnu, vous devez :</span><span class="sxs-lookup"><span data-stu-id="7345e-134">For example, if you create a **Date** pattern list and you want to make sure that a date format such as *Jan 1, 2020* is recognized, you need to:</span></span>
- <span data-ttu-id="7345e-135">ajouter *aaa 0, 0000* et *aaa 00, 0000* à votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="7345e-135">Add *aaa 0, 0000* and *aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="7345e-136">vous assurer que **Toutes les lettres de a à z** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-136">Make sure that **Any letter from a-z** is also selected.</span></span>

   ![Toutes les lettres de a à z](../media/content-understanding/any-letter.png)

<span data-ttu-id="7345e-138">De plus, si vous avez des exigences de mise en majuscule dans votre liste de modèles, vous avez la possibilité de cocher la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="7345e-138">Additionally, if you have capitalization requirements in your pattern list, you have the option to select the **Only exact capitalization** checkbox.</span></span> <span data-ttu-id="7345e-139">Pour l’exemple Date, si vous souhaitez que la première lettre du mois soit en majuscule, vous devez :</span><span class="sxs-lookup"><span data-stu-id="7345e-139">For the Date example, if you require the first letter of the month to be capitalized, you need to:</span></span>

- <span data-ttu-id="7345e-140">ajouter *Aaa 0, 0000* et *Aaa 00, 0000* à votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="7345e-140">Add *Aaa 0, 0000* and *Aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="7345e-141">vous assurer que **Seulement la mise en majuscule exacte** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-141">Make sure that **Only exact capitalization** is also selected.</span></span>

   ![Seulement la mise en majuscule exacte](../media/content-understanding/exact-caps.png)

> [!NOTE]
> <span data-ttu-id="7345e-143">Au lieu de créer manuellement une explication de liste de modèles, utilisez la [bibliothèque d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-explanation-templates) pour utiliser des modèles de liste de modèles pour une liste de modèles commune, comme les *dates*, *numéros de téléphone*, *numéro de carte bancaire*, etc.</span><span class="sxs-lookup"><span data-stu-id="7345e-143">Instead of manually creating a pattern list explanation, use the [explanation library](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-explanation-templates) to use pattern list templates for a common pattern list, such as *date*, *phone number*, *credit card number*, etc.</span></span>

## <a name="proximity"></a><span data-ttu-id="7345e-144">Proximité</span><span class="sxs-lookup"><span data-stu-id="7345e-144">Proximity</span></span> 

<span data-ttu-id="7345e-145">Le type d’explication de proximité aide votre modèle à identifier les données en définissant la proximité d’un autre élément de données.</span><span class="sxs-lookup"><span data-stu-id="7345e-145">The proximity explanation type helps your model identify data by defining how close another piece of data is to it.</span></span> <span data-ttu-id="7345e-146">Par exemple, dans votre modèle, vous avez défini deux explications qui étiquettent à la fois le *Numéro d’adresse* et le *Numéro de téléphone* du client.</span><span class="sxs-lookup"><span data-stu-id="7345e-146">For example, in your model say you have defined two explanations that label both the customer *Street address number* and *Phone number*.</span></span> 

<span data-ttu-id="7345e-147">Remarquez également que les numéros de téléphone des clients apparaissent toujours avant le numéro de l’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="7345e-147">Notice that customer phone numbers always appear before the street address number.</span></span> 

<span data-ttu-id="7345e-148">Alain Chauvin</span><span class="sxs-lookup"><span data-stu-id="7345e-148">Alex Wilburn</span></span><br>
<span data-ttu-id="7345e-149">555-555-5555</span><span class="sxs-lookup"><span data-stu-id="7345e-149">555-555-5555</span></span><br>
<span data-ttu-id="7345e-150">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="7345e-150">One Microsoft Way</span></span><br>
<span data-ttu-id="7345e-151">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="7345e-151">Redmond, WA 98034</span></span><br>

<span data-ttu-id="7345e-152">Utilisez l’explication de proximité pour définir la distance de l’explication du numéro de téléphone afin de mieux identifier le numéro de l’adresse postale dans vos documents.</span><span class="sxs-lookup"><span data-stu-id="7345e-152">Use the proximity explanation to define how far away the phone number explanation is to better identify the street address number in your documents.</span></span>

   ![Explication de proximité](../media/content-understanding/proximity.png)</br>

#### <a name="what-are-tokens"></a><span data-ttu-id="7345e-154">Que sont les jetons ?</span><span class="sxs-lookup"><span data-stu-id="7345e-154">What are tokens?</span></span>

<span data-ttu-id="7345e-155">Pour utiliser le type d’explication de proximité, vous devez comprendre ce qu’est un jeton, car l’explication de proximité mesure la distance entre deux explications grâce au nombre de jetons.</span><span class="sxs-lookup"><span data-stu-id="7345e-155">In order to use the proximity explanation type, you need to understand what a token is, as the number of tokens is how the proximity explanation measures distance from one explanation to another.</span></span> <span data-ttu-id="7345e-156">Un jeton est une étendue continue (non compris les espaces et la ponctuation) de lettres et de chiffres.</span><span class="sxs-lookup"><span data-stu-id="7345e-156">A token is a continuous span (not including spaces or punctuation) of letters and numbers.</span></span> 

<span data-ttu-id="7345e-157">Le tableau suivant illustre des exemples sur la façon de déterminer le nombre de jetons dans une expression.</span><span class="sxs-lookup"><span data-stu-id="7345e-157">The following table shows examples for how to determine the number of tokens in a phrase.</span></span>

|<span data-ttu-id="7345e-158">Expression</span><span class="sxs-lookup"><span data-stu-id="7345e-158">Phrase</span></span>|<span data-ttu-id="7345e-159">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="7345e-159">Number of tokens</span></span>|<span data-ttu-id="7345e-160">Explication</span><span class="sxs-lookup"><span data-stu-id="7345e-160">Explanation</span></span>|
|--|--|--|
|`Dog`|<span data-ttu-id="7345e-161">1</span><span class="sxs-lookup"><span data-stu-id="7345e-161">1</span></span>|<span data-ttu-id="7345e-162">Un seul mot sans ponctuation ni espaces.</span><span class="sxs-lookup"><span data-stu-id="7345e-162">A single word with no punctuation or spaces.</span></span>|
|`RMT33W`|<span data-ttu-id="7345e-163">1</span><span class="sxs-lookup"><span data-stu-id="7345e-163">1</span></span>|<span data-ttu-id="7345e-164">Un numéro de localisateur d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="7345e-164">A record locator number.</span></span> <span data-ttu-id="7345e-165">Il peut inclure des chiffres et des lettres, mais pas de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="7345e-165">It may include numbers and letters, but does not have punctuation.</span></span>|
|`425-555-5555`|<span data-ttu-id="7345e-166">5</span><span class="sxs-lookup"><span data-stu-id="7345e-166">5</span></span>|<span data-ttu-id="7345e-167">Un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="7345e-167">A phone number.</span></span> <span data-ttu-id="7345e-168">Chaque signe de ponctuation équivaut à un seul jeton, donc `425-555-5555` correspond à 5 jetons :</span><span class="sxs-lookup"><span data-stu-id="7345e-168">Each punctuation mark is a single token, so `425-555-5555` is 5 tokens:</span></span><br>`425`<br>`-`<br>`555`<br>`-`<br>`5555` |
|`https://luis.ai`|<span data-ttu-id="7345e-169">7</span><span class="sxs-lookup"><span data-stu-id="7345e-169">7</span></span>|`https`<br>`:`<br>`/`<br>`/`<br>`luis`<br>`.`<br>`ai`<br>|

#### <a name="configure-the-proximity-explanation-type"></a><span data-ttu-id="7345e-170">Configurer le type d’explication de proximité</span><span class="sxs-lookup"><span data-stu-id="7345e-170">Configure the proximity explanation type</span></span>

<span data-ttu-id="7345e-171">Pour l’exemple, configurez le paramètre de proximité pour définir la plage du nombre de jetons. L’explication dans le *Numéro de téléphone* provient de l’explication du *Numéro d’adresse*.</span><span class="sxs-lookup"><span data-stu-id="7345e-171">For the example, configure the proximity setting to define the range of the number of tokens in the *Phone number* explanation from the *Street address number* explanation.</span></span> <span data-ttu-id="7345e-172">Remarquez que la plage minimale est « 0 » car il n’y a pas de jetons entre le numéro de téléphone et le numéro d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="7345e-172">Notice that the minimum range is "0", because there are no tokens between the phone number and street address number.</span></span>

<span data-ttu-id="7345e-173">Certains numéros de téléphone dans les exemples de documents sont toutefois ajoutés avec un *(mobile)*.</span><span class="sxs-lookup"><span data-stu-id="7345e-173">But some phone numbers in the sample documents are appended with *(mobile)*.</span></span>

<span data-ttu-id="7345e-174">Maurice Boule</span><span class="sxs-lookup"><span data-stu-id="7345e-174">Nestor Wilke</span></span><br>
<span data-ttu-id="7345e-175">111-111-1111 (mobile)</span><span class="sxs-lookup"><span data-stu-id="7345e-175">111-111-1111 (mobile)</span></span><br>
<span data-ttu-id="7345e-176">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="7345e-176">One Microsoft Way</span></span><br>
<span data-ttu-id="7345e-177">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="7345e-177">Redmond, WA 98034</span></span><br>

<span data-ttu-id="7345e-178">Il y a trois jetons dans *(mobile)*  :</span><span class="sxs-lookup"><span data-stu-id="7345e-178">There are three tokens in *(mobile)*:</span></span>

|<span data-ttu-id="7345e-179">Expression</span><span class="sxs-lookup"><span data-stu-id="7345e-179">Phrase</span></span>|<span data-ttu-id="7345e-180">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="7345e-180">Token count</span></span>|
|--|--|
|<span data-ttu-id="7345e-181">(</span><span class="sxs-lookup"><span data-stu-id="7345e-181">(</span></span>|<span data-ttu-id="7345e-182">1</span><span class="sxs-lookup"><span data-stu-id="7345e-182">1</span></span>|
|<span data-ttu-id="7345e-183">mobile</span><span class="sxs-lookup"><span data-stu-id="7345e-183">mobile</span></span>|<span data-ttu-id="7345e-184">2</span><span class="sxs-lookup"><span data-stu-id="7345e-184">2</span></span>|
|<span data-ttu-id="7345e-185">)</span><span class="sxs-lookup"><span data-stu-id="7345e-185">)</span></span>|<span data-ttu-id="7345e-186">3</span><span class="sxs-lookup"><span data-stu-id="7345e-186">3</span></span>|

<span data-ttu-id="7345e-187">Configurez le paramètre de proximité pour avoir une plage de 0 à 3.</span><span class="sxs-lookup"><span data-stu-id="7345e-187">Configure the proximity setting to have a range of 0 through 3.</span></span>

   ![Exemple de proximité](../media/content-understanding/proximity-example.png)</br>


## <a name="configure-where-phrases-occur-in-the-document"></a><span data-ttu-id="7345e-189">Configurer l’endroit où des phrases apparaissent dans le document</span><span class="sxs-lookup"><span data-stu-id="7345e-189">Configure where phrases occur in the document</span></span>

<span data-ttu-id="7345e-190">Lorsque vous créez une explication, par défaut, l’ensemble du document est recherché à la recherche de l’expression que vous essayez d’extraire.</span><span class="sxs-lookup"><span data-stu-id="7345e-190">When you create an explanation, by default the entire document is searched for the phrase you are trying to extract.</span></span> <span data-ttu-id="7345e-191">Toutefois, vous pouvez utiliser le <b>Où ces expressions se produisent</b> paramètre avancé pour vous aider à isoler un emplacement spécifique dans le document où se produit une expression.</span><span class="sxs-lookup"><span data-stu-id="7345e-191">However, you can use the <b>Where these phrases occur</b> advanced setting to help in isolating a specific location in the document that a phrase occurs.</span></span> <span data-ttu-id="7345e-192">Cela est utile dans les situations où des instances similaires d’une expression peuvent apparaître à un autre endroit dans le document et dont vous voulez vous assurer que celle qui est correcte est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-192">This is useful in situations where similar instances of a phrase might appear somewhere else in the document, and you want to make sure that the correct one is selected.</span></span> <span data-ttu-id="7345e-193">En référence à notre exemple de document de référence médical, la **Référence médecin** est toujours mentionnée dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="7345e-193">Referring to our Medical Referral document example, the **Referring Doctor** is always mentioned in the first paragraph of the document.</span></span> <span data-ttu-id="7345e-194">Avec le paramètre <b>Où ces expressions se produisent</b>, dans cet exemple, vous pouvez configurer votre explication pour rechercher cette étiquette uniquement dans la section de début du document ou dans tout autre emplacement où elle pourrait se produire.</span><span class="sxs-lookup"><span data-stu-id="7345e-194">With the <b>Where these phrases occur</b> setting, in this example you can configure your explanation to search for this label only in the beginning section of the document, or any other location in which it might occur.</span></span>

   ![Paramètre où ces phrases se produisent](../media/content-understanding/phrase-location.png)</br>

<span data-ttu-id="7345e-196">Vous pouvez choisir l'une des trois options suivantes :</span><span class="sxs-lookup"><span data-stu-id="7345e-196">You can choose the following options for this setting:</span></span>

- <span data-ttu-id="7345e-197">N’importe où dans le fichier : recherche l’expression dans l’ensemble du document.</span><span class="sxs-lookup"><span data-stu-id="7345e-197">Anywhere in the file: The entire document is searched for the phrase.</span></span>
- <span data-ttu-id="7345e-198">Début du fichier : La recherche s’effectuera du début jusqu’à l’emplacement des expressions.</span><span class="sxs-lookup"><span data-stu-id="7345e-198">Beginning of the file:  The document is searched from the beginning to the phrase location.</span></span></br> 
   <span data-ttu-id="7345e-199">![Début du fichier](../media/content-understanding/beginning-of-file.png)</span><span class="sxs-lookup"><span data-stu-id="7345e-199">![Beginning of file](../media/content-understanding/beginning-of-file.png)</span></span></br>
<span data-ttu-id="7345e-200">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="7345e-200">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="7345e-201">La valeur <b>Position de fin</b> est mise à jour de manière à afficher le nombre de jetons inclus dans la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-201">The <b>End position</b> value will update to show the number of tokens your selected area includes.</span></span> <span data-ttu-id="7345e-202">Notez que vous pouvez également mettre à jour la valeur de position de fin pour ajuster la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-202">Note that you can update the End position value as well to adjust the selected area.</span></span></br>
   <span data-ttu-id="7345e-203">![Zone Début de la position du fichier](../media/content-understanding/beginning-box.png)</span><span class="sxs-lookup"><span data-stu-id="7345e-203">![Beginning of file position box](../media/content-understanding/beginning-box.png)</span></span></br>

- <span data-ttu-id="7345e-204">Fin du fichier : La recherche s’effectuera de la fin jusqu’à l’emplacement des expressions.</span><span class="sxs-lookup"><span data-stu-id="7345e-204">End of the file:  The document is searched from the end to the phrase location.</span></span></br> 
   <span data-ttu-id="7345e-205">![Fin du fichier](../media/content-understanding/end-of-file.png)</span><span class="sxs-lookup"><span data-stu-id="7345e-205">![End of file](../media/content-understanding/end-of-file.png)</span></span></br>
<span data-ttu-id="7345e-206">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="7345e-206">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="7345e-207">La valeur <b>Position de début</b> est mise à jour de manière à afficher le nombre de jetons inclus dans la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-207">The <b>Starting position</b> value will update to show the number of tokens your selected area includes.</span></span> <span data-ttu-id="7345e-208">Notez que vous pouvez également mettre à jour la valeur de position de début pour ajuster la zone sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7345e-208">Note that you can update the Starting position value as well to adjust the selected area.</span></span></br> 
   <span data-ttu-id="7345e-209">![Zone Fin de fichier](../media/content-understanding/end-box.png)</span><span class="sxs-lookup"><span data-stu-id="7345e-209">![End of file end box](../media/content-understanding/end-box.png)</span></span></br>
- <span data-ttu-id="7345e-210">Plage personnalisée : recherche l’emplacement de l’expression dans une plage spécifiée du document.</span><span class="sxs-lookup"><span data-stu-id="7345e-210">Custom range:  The document is searched in a specified range within the it for the phrase location.</span></span></br> 
   <span data-ttu-id="7345e-211">![Plage personnalisée](../media/content-understanding/custom-file.png).</span><span class="sxs-lookup"><span data-stu-id="7345e-211">![Custom range](../media/content-understanding/custom-file.png)</span></span></br>
<span data-ttu-id="7345e-212">Dans la visionneuse, vous pouvez ajuster manuellement la case à sélectionner de manière à inclure l’emplacement où la phase a lieu.</span><span class="sxs-lookup"><span data-stu-id="7345e-212">In the viewer, you can manually adjust the select box to include the location where the phase occurs.</span></span> <span data-ttu-id="7345e-213">Pour ce paramètre, vous devez sélectionner une position de <b>Début</b> et une position de <b>Fin</b>.</span><span class="sxs-lookup"><span data-stu-id="7345e-213">For this setting, you need to select a <b>Start</b> and an <b>End</b> position.</span></span> <span data-ttu-id="7345e-214">Ces valeurs représentent le nombre de jetons dès le début du document.</span><span class="sxs-lookup"><span data-stu-id="7345e-214">These values represent the number of tokens from the begging of the document.</span></span> <span data-ttu-id="7345e-215">Bien que vous pouvez entrer manuellement ces valeurs, il est plus facile d’ajuster manuellement la case à sélectionner dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="7345e-215">While you can manually enter in these values, it is easier to manually adjust the select box in the viewer.</span></span></br> 
   


## <a name="use-explanation-templates"></a><span data-ttu-id="7345e-216">Utiliser des modèles d’explication</span><span class="sxs-lookup"><span data-stu-id="7345e-216">Use explanation templates</span></span>

<span data-ttu-id="7345e-217">Bien que vous puissiez ajouter manuellement différentes valeurs de liste de modèles pour votre explication, il peut être plus facile d’utiliser les modèles qui vous sont fournis dans la bibliothèque d’explications.</span><span class="sxs-lookup"><span data-stu-id="7345e-217">While you can manually add various pattern list values for your explanation, it can be easier to use the templates provided to you in the explanation library.</span></span>

<span data-ttu-id="7345e-218">Par exemple, au lieu d’ajouter manuellement toutes les variantes de *Date*, vous pouvez utiliser le modèle de liste de modèles pour *Date*, qui comprend déjà un certain nombre de valeurs de listes de modèles :</span><span class="sxs-lookup"><span data-stu-id="7345e-218">For example, instead of manually adding all the variations for *Date*, you can use the pattern list template for *Date* as it already includes a number of pattern lists values:</span></span></br>

   ![Bibliothèque d’explications](../media/content-understanding/explanation-template.png)</br>
 
<span data-ttu-id="7345e-220">La bibliothèque d’explications comprend des explications de liste de modèles couramment utilisées, notamment :</span><span class="sxs-lookup"><span data-stu-id="7345e-220">The explanation library includes commonly used pattern list explanations, including:</span></span></br>

- <span data-ttu-id="7345e-221">Date</span><span class="sxs-lookup"><span data-stu-id="7345e-221">Date</span></span></br>
- <span data-ttu-id="7345e-222">Données (numériques)</span><span class="sxs-lookup"><span data-stu-id="7345e-222">Date (numeric)</span></span></br>
- <span data-ttu-id="7345e-223">Temps</span><span class="sxs-lookup"><span data-stu-id="7345e-223">Time</span></span></br>
- <span data-ttu-id="7345e-224">Nombre</span><span class="sxs-lookup"><span data-stu-id="7345e-224">Number</span></span></br>
- <span data-ttu-id="7345e-225">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="7345e-225">Phone number</span></span></br>
- <span data-ttu-id="7345e-226">Code postal</span><span class="sxs-lookup"><span data-stu-id="7345e-226">Zip code</span></span></br>
- <span data-ttu-id="7345e-227">Premier mot de la phrase</span><span class="sxs-lookup"><span data-stu-id="7345e-227">First word of sentence</span></span></br>
- <span data-ttu-id="7345e-228">Carte bancaire</span><span class="sxs-lookup"><span data-stu-id="7345e-228">Credit card</span></span></br>
- <span data-ttu-id="7345e-229">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="7345e-229">Social security number</span></span></br>

<span data-ttu-id="7345e-230">Notez que la bibliothèque d’explications comprend également des modèles pour les explications de liste d’expressions :</span><span class="sxs-lookup"><span data-stu-id="7345e-230">Note that the explanation library also includes templates for phrase list explanations:</span></span>
- <span data-ttu-id="7345e-231">Fin de la phrase</span><span class="sxs-lookup"><span data-stu-id="7345e-231">End of sentence</span></span>
- <span data-ttu-id="7345e-232">Devise</span><span class="sxs-lookup"><span data-stu-id="7345e-232">Currency</span></span>

#### <a name="to-use-a-template-from-the-explanation-library"></a><span data-ttu-id="7345e-233">Pour utiliser un modèle de la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="7345e-233">To use a template from the explanation library</span></span>

1. <span data-ttu-id="7345e-234">Dans la section **Explications** de la page **Entraîner** de votre modèle, sélectionnez **Nouveau**, puis **À partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="7345e-234">From the **Explanations** section of your model's **Train** page, select **New**, then select **From a template**.</span></span></br>

   ![Créer à partir d’un modèle](../media/content-understanding/from-template.png)</br>

2.  <span data-ttu-id="7345e-236">Sur la page **Modèles d’explication**, sélectionnez l’explication que vous souhaitez utiliser, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7345e-236">On the **Explanation templates** page, select the explanation you want to use, then select **Add**.</span></span></br>

       ![Sélectionner un modèle](../media/content-understanding/phone-template.png)</br>

3. <span data-ttu-id="7345e-238">Les informations relatives au modèle que vous avez sélectionné s’affichent sur la page **Créer une explication**.</span><span class="sxs-lookup"><span data-stu-id="7345e-238">The information for the template you selected displays on the **Create an explanation** page.</span></span> <span data-ttu-id="7345e-239">Si nécessaire, modifiez le nom de l’explication et ajoutez ou supprimez des éléments de la liste des modèles.</span><span class="sxs-lookup"><span data-stu-id="7345e-239">If needed, edit the explanation name and add or remove items from the pattern list.</span></span> </br> 

   ![Modifier le modèle](../media/content-understanding/phone-template-live.png)</br>

4. <span data-ttu-id="7345e-241">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7345e-241">When finished, select **Save**.</span></span>
