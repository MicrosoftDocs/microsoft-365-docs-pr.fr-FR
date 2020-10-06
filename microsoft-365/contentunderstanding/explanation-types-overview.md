---
title: Types d’explication
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: En savoir plus sur les types d’explications dans Microsoft SharePoint Syntex
ms.openlocfilehash: 43272504912451e4690cb8b7fe351462371bb252
ms.sourcegitcommit: 3a0accd616ca94d6ba7f50e502552b45e9661a95
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2020
ms.locfileid: "48350302"
---
# <a name="introduction-to-explanation-types"></a><span data-ttu-id="c7e1a-103">Introduction aux types d’explications</span><span class="sxs-lookup"><span data-stu-id="c7e1a-103">Introduction to explanation types</span></span>

<span data-ttu-id="c7e1a-104">Les explications sont utilisées pour vous permettre de définir les informations que vous souhaitez étiqueter et extraire dans vos modèles de compréhension de documents dans Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-104">Explanations are used to help to define the information you want to label and extract in your document understanding models in Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="c7e1a-105">Lors de la création d’une explication, vous devez sélectionner un type d’explication.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-105">When creating an explanation, you need to select an explanation type.</span></span> <span data-ttu-id="c7e1a-106">Cet article vous aidera à mieux comprendre les différents types d’explications et comment ils sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-106">This article will help you learn more to better understand the different explanation types and how they are used.</span></span> 

   ![Types d’explication](../media/content-understanding/explanation-types.png) 
   
<span data-ttu-id="c7e1a-108">Les types d’explications suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-108">These explanation types are available:</span></span>

- <span data-ttu-id="c7e1a-109">**Liste d’expressions** : liste de mots, expressions, nombres ou autres caractères que vous pouvez utiliser dans le document ou les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-109">**Phrase list**: List of words, phrases, numbers, or other characters you can use in the document or information that you are extracting.</span></span> <span data-ttu-id="c7e1a-110">Par exemple, la chaîne de texte **Médecin référent** se trouve dans tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-110">For example, the text string **Referring Doctor** is in all Medical Referral documents you are identifying.</span></span></br>

- <span data-ttu-id="c7e1a-111">**Liste de modèles** : répertorie les modèles de chiffres, de lettres ou d’autres caractères que vous pouvez utiliser pour identifier les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-111">**Pattern list**: List patterns of numbers, letters, or other characters that you can use to identify the information that you are extracting.</span></span> <span data-ttu-id="c7e1a-112">Par exemple, vous pouvez extraire le **numéro de téléphone** du médecin référent de tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-112">For example, you can extract the **Phone number** of the referring doctor from all Medical Referral document that you are identifying.</span></span></br>

- <span data-ttu-id="c7e1a-113">**Proximité** : décrit à quel point les explications sont proches les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-113">**Proximity**: Describes how close explanations are to each other.</span></span> <span data-ttu-id="c7e1a-114">Par exemple, une liste de modèles de *numéros de rue* se trouve juste avant la liste d’expressions des *noms de rue*, sans jetons entre les deux (vous en apprendrez davantage sur les jetons plus loin dans cet article).</span><span class="sxs-lookup"><span data-stu-id="c7e1a-114">For example, a *street number* pattern list goes right before the *street name* phrase list, with no tokens in between (you'll learn about tokens later in this article).</span></span> <span data-ttu-id="c7e1a-115">L’utilisation du type de proximité nécessite que vous ayez au moins deux explications dans votre modèle. Dans le cas contraire, l’option sera désactivée.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-115">Using the proximity type requires you to have at least two explanations in your model, or the option will be disabled.</span></span> 
 
## <a name="phrase-list"></a><span data-ttu-id="c7e1a-116">Liste d’expressions</span><span class="sxs-lookup"><span data-stu-id="c7e1a-116">Phrase list</span></span>

<span data-ttu-id="c7e1a-117">Un type d’explication de liste d’expressions est généralement utilisé pour identifier et classer un document dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-117">A phrase list explanation type is typically used to identify and classify a document through your model.</span></span> <span data-ttu-id="c7e1a-118">Comme décrit dans l’exemple d’étiquette *Médecin référent*, il s’agit d’une chaîne de mots, d’expressions, de nombres ou de caractères qui se trouve systématiquement dans les documents que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-118">As described in the *Referring Doctor* label example, it is a string of words, phrases, numbers, or characters that is consistently in the documents that you are identifying.</span></span>

<span data-ttu-id="c7e1a-119">Bien que ce ne soit pas obligatoire, vous pouvez améliorer les performances de votre explication si l’expression que vous capturez se trouve à un emplacement cohérent dans votre document.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-119">While not a requirement, you can achieve better success with your explanation if the phrase you are capturing is located in a consistent location in your document.</span></span> <span data-ttu-id="c7e1a-120">Par exemple, l’étiquette *Médecin référent* peut être située systématiquement dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-120">For example, the *Referring Doctor* label may be consistently located in the first paragraph of the document.</span></span>

<span data-ttu-id="c7e1a-121">Si le respect de la casse est une exigence pour identifier votre étiquette, l’utilisation du type de liste d’expressions vous permet de le spécifier dans votre explication en cochant la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-121">If case sensitivity is a requirement in identifying your label, using the phrase list type allows you to specify it in your explanation by selecting the **Only exact capitalization** checkbox.</span></span>

   ![Respect de la casse](../media/content-understanding/case-sensitivity.png) 

## <a name="pattern-lists"></a><span data-ttu-id="c7e1a-123">Listes de modèles</span><span class="sxs-lookup"><span data-stu-id="c7e1a-123">Pattern lists</span></span>

<span data-ttu-id="c7e1a-124">Un type de liste de modèles est particulièrement utile lorsque vous créez une explication qui identifie et extrait des informations d’un document.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-124">A pattern list type is especially useful when you create an explanation that identifies and extracts information from a document.</span></span> <span data-ttu-id="c7e1a-125">Il est généralement présenté dans différents formats, tels que des dates, des numéros de téléphone ou des numéros de carte bancaire.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-125">It is typically presented in different formats, such as dates, phone numbers, or credit card numbers.</span></span> <span data-ttu-id="c7e1a-126">Par exemple, une date peut être affichée dans plusieurs formats différents (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, 1 janvier 2020, etc.).</span><span class="sxs-lookup"><span data-stu-id="c7e1a-126">For example, a date can be displayed in a number of different formats (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, Jan 1,2020, etc.).</span></span> <span data-ttu-id="c7e1a-127">La définition d’une liste de modèles rend votre explication plus efficace en capturant toutes les variations possibles dans les données que vous essayez d’identifier et d’extraire.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-127">Defining a pattern list makes your explanation more efficient by capturing any possible variations in the data that you are trying to identify and extract.</span></span> 

<span data-ttu-id="c7e1a-128">Pour l’échantillon de **numéro de téléphone**, extrayez le numéro de téléphone de chaque médecin référent dans tous les documents de référence médicale que le modèle identifie.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-128">For the **Phone number** sample, extract the phone number for each referring doctor from all Medical Referral documents that the model identifies.</span></span> <span data-ttu-id="c7e1a-129">Lorsque vous créez l’explication, sélectionnez le type de liste de modèles pour autoriser les différents formats que vous pouvez vous attendre à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-129">When you create the explanation, select the Pattern list type to allow the different formats that you may expect to be returned.</span></span>

   ![Liste de modèles de numéros de téléphone](../media/content-understanding/pattern-list.png)

<span data-ttu-id="c7e1a-131">Pour cet échantillon, cochez la case **Tous les chiffres de 0 à 9**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-131">For this sample, select the **Any digit from 0-9** checkbox.</span></span> <span data-ttu-id="c7e1a-132">Sélectionner cette option permet de reconnaître chaque valeur « 0 » utilisée dans votre liste de modèles comme étant un chiffre entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-132">Selecting this recognizes each "0" value used in your pattern list to be any digit from 0 through 9.</span></span>

   ![Tous les chiffres de 0 à 9](../media/content-understanding/digit-identity.png)

<span data-ttu-id="c7e1a-134">De même, si vous créez une liste de modèles comprenant des caractères de texte, cochez la case **Toutes les lettres de a à z**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-134">Similarly, if you create a pattern list that includes text characters, select the **Any letter from a-z** checkbox.</span></span> <span data-ttu-id="c7e1a-135">Sélectionner cette option permet de reconnaître chaque valeur « a » utilisée dans votre liste de modèles comme étant un caractère entre a et z.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-135">Selecting this recognizes each "a" character used in the pattern list to be any character from "a" to "z".</span></span>

<span data-ttu-id="c7e1a-136">Par exemple, si vous créez une liste de modèles **Date** et que vous souhaitez vous assurer qu’un format de date tel que *Jan 1, 2020* est reconnu, vous devez :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-136">For example, if you create a **Date** pattern list and you want to make sure that a date format such as *Jan 1, 2020* is recognized, you need to:</span></span>
- <span data-ttu-id="c7e1a-137">ajouter *aaa 0, 0000* et *aaa 00, 0000* à votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-137">Add *aaa 0, 0000* and *aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="c7e1a-138">vous assurer que **Toutes les lettres de a à z** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-138">Make sure that **Any letter from a-z** is also selected.</span></span>

   ![Toutes les lettres de a à z](../media/content-understanding/any-letter.png)

<span data-ttu-id="c7e1a-140">De plus, si vous avez des exigences de mise en majuscule dans votre liste de modèles, vous avez la possibilité de cocher la case **Seulement la mise en majuscule exacte**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-140">Additionally, if you have capitalization requirements in your pattern list, you have the option to select the **Only exact capitalization** checkbox.</span></span> <span data-ttu-id="c7e1a-141">Pour l’exemple Date, si vous souhaitez que la première lettre du mois soit en majuscule, vous devez :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-141">For the Date example, if you require the first letter of the month to be capitalized, you need to:</span></span>

- <span data-ttu-id="c7e1a-142">ajouter *Aaa 0, 0000* et *Aaa 00, 0000* à votre liste de modèles.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-142">Add *Aaa 0, 0000* and *Aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="c7e1a-143">vous assurer que **Seulement la mise en majuscule exacte** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-143">Make sure that **Only exact capitalization** is also selected.</span></span>

   ![Seulement la mise en majuscule exacte](../media/content-understanding/exact-caps.png)

> [!NOTE]
> <span data-ttu-id="c7e1a-145">Au lieu de créer manuellement une explication de liste de modèles, utilisez la [bibliothèque d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-explanation-templates) pour utiliser des modèles de liste de modèles prédéfinis pour une liste de modèles commune, comme les *dates*, *numéros de téléphone*, *numéro de carte bancaire*, etc.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-145">Instead of manually creating pattern list explanation, use the [explanation library](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-explanation-templates) to use pre-made pattern list templates for common pattern list, such as *date*, *phone number*, *credit card number*, etc..</span></span> 

## <a name="proximity"></a><span data-ttu-id="c7e1a-146">Proximité</span><span class="sxs-lookup"><span data-stu-id="c7e1a-146">Proximity</span></span> 

<span data-ttu-id="c7e1a-147">Le type d’explication de proximité aide votre modèle à identifier les données en définissant la proximité d’un autre élément de données.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-147">The proximity explanation type helps your model identify data through defining how close another piece of data is to it.</span></span> <span data-ttu-id="c7e1a-148">Par exemple, dans votre modèle, vous avez défini deux explications qui étiquettent à la fois le *Numéro d’adresse* et le *Numéro de téléphone* du client.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-148">For example, in your model, you have defined two explanations that label both the customer *Street address number* and *Phone number*.</span></span> 

<span data-ttu-id="c7e1a-149">Vous remarquez également que les numéros de téléphone des clients apparaissent toujours avant le numéro de l’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-149">You also notice that customer phone numbers always appear before the street address number.</span></span> 

<span data-ttu-id="c7e1a-150">Alain Chauvin</span><span class="sxs-lookup"><span data-stu-id="c7e1a-150">Alex Wilburn</span></span><br>
<span data-ttu-id="c7e1a-151">555-555-5555</span><span class="sxs-lookup"><span data-stu-id="c7e1a-151">555-555-5555</span></span><br>
<span data-ttu-id="c7e1a-152">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="c7e1a-152">One Microsoft Way</span></span><br>
<span data-ttu-id="c7e1a-153">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="c7e1a-153">Redmond, WA 98034</span></span><br>

<span data-ttu-id="c7e1a-154">Utilisez l’explication de proximité pour définir la distance de l’explication du numéro de téléphone afin de mieux identifier le numéro de l’adresse postale dans vos documents.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-154">Use the proximity explanation to define how far away the phone number explanation is to better identify the street address number in your documents.</span></span>

   ![Explication de proximité](../media/content-understanding/proximity.png)</br>

#### <a name="what-are-tokens"></a><span data-ttu-id="c7e1a-156">Que sont les jetons ?</span><span class="sxs-lookup"><span data-stu-id="c7e1a-156">What are tokens?</span></span>

<span data-ttu-id="c7e1a-157">Pour utiliser le type d’explication de proximité, vous devez comprendre ce qu’est un jeton, car l’explication de proximité mesure la distance entre deux explications grâce au nombre de jetons.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-157">In order to use the proximity explanation type, you need to understand what a token is, as the number of tokens is how the proximity explanation measures distance from one explanation to another.</span></span>  

<span data-ttu-id="c7e1a-158">Un jeton est une étendue continue (sans espaces ni ponctuation) de lettres et de chiffres.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-158">A token is a continuous span (no spaces or punctuation) of letters and numbers.</span></span> <span data-ttu-id="c7e1a-159">Un espace n’est PAS un jeton.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-159">A space is NOT a token.</span></span> <span data-ttu-id="c7e1a-160">Chaque caractère de ponctuation est un jeton.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-160">Each punctuation character is a token.</span></span> <span data-ttu-id="c7e1a-161">Le tableau suivant illustre quelques exemples sur la façon de déterminer le nombre de jetons dans une expression.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-161">The following table shows some examples of how to determine the number of tokens in a phrase.</span></span>

|<span data-ttu-id="c7e1a-162">Expression</span><span class="sxs-lookup"><span data-stu-id="c7e1a-162">Phrase</span></span>|<span data-ttu-id="c7e1a-163">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="c7e1a-163">Number of tokens</span></span>|<span data-ttu-id="c7e1a-164">Explication</span><span class="sxs-lookup"><span data-stu-id="c7e1a-164">Explanation</span></span>|
|--|--|--|
|`Dog`|<span data-ttu-id="c7e1a-165">1</span><span class="sxs-lookup"><span data-stu-id="c7e1a-165">1</span></span>|<span data-ttu-id="c7e1a-166">Un seul mot sans ponctuation ni espaces.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-166">A single word with no punctuation or spaces.</span></span>|
|`RMT33W`|<span data-ttu-id="c7e1a-167">1</span><span class="sxs-lookup"><span data-stu-id="c7e1a-167">1</span></span>|<span data-ttu-id="c7e1a-168">Un numéro de localisateur d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-168">A record locator number.</span></span> <span data-ttu-id="c7e1a-169">Il peut contenir des chiffres et des lettres, mais pas de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-169">It may have numbers and letters, but does not have any punctuation.</span></span>|
|`425-555-5555`|<span data-ttu-id="c7e1a-170">5</span><span class="sxs-lookup"><span data-stu-id="c7e1a-170">5</span></span>|<span data-ttu-id="c7e1a-171">Un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-171">A phone number.</span></span> <span data-ttu-id="c7e1a-172">Chaque signe de ponctuation équivaut à un seul jeton, donc `425-555-5555` correspond à 5 jetons :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-172">Each punctuation mark is a single token so  `425-555-5555` would be 5 tokens:</span></span><br>`425`<br>`-`<br>`555`<br>`-`<br>`5555` |
|`https://luis.ai`|<span data-ttu-id="c7e1a-173">7</span><span class="sxs-lookup"><span data-stu-id="c7e1a-173">7</span></span>|`https`<br>`:`<br>`/`<br>`/`<br>`luis`<br>`.`<br>`ai`<br>|

#### <a name="configure-the-proximity-explanation-type"></a><span data-ttu-id="c7e1a-174">Configurer le type d’explication de proximité</span><span class="sxs-lookup"><span data-stu-id="c7e1a-174">Configure the proximity explanation type</span></span>

<span data-ttu-id="c7e1a-175">Pour l’échantillon, configurez le paramètre de proximité afin que nous puissions définir la plage du nombre de jetons. L’explication du *Numéro de téléphone* provient de l’explication du *Numéro d’adresse*.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-175">For the sample, configure the proximity setting so that we can define the range of the number of tokens the *Phone number* explanation is from the *Street address number* explanation.</span></span>

<span data-ttu-id="c7e1a-176">Vous devriez voir que la plage minimale est « 0 » car il n’y a pas de jetons entre le numéro de téléphone et le numéro d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-176">You should see that the minimum range is "0" since there are no tokens between the phone number and street address number.</span></span>

<span data-ttu-id="c7e1a-177">Cependant, certains numéros de téléphone dans les exemples de documents sont ajoutés avec un *(mobile)*.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-177">However, some phone numbers in the sample documents are appended with *(mobile)*.</span></span>

<span data-ttu-id="c7e1a-178">Maurice Boule</span><span class="sxs-lookup"><span data-stu-id="c7e1a-178">Nestor Wilke</span></span><br>
<span data-ttu-id="c7e1a-179">111-111-1111 (mobile)</span><span class="sxs-lookup"><span data-stu-id="c7e1a-179">111-111-1111 (mobile)</span></span><br>
<span data-ttu-id="c7e1a-180">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="c7e1a-180">One Microsoft Way</span></span><br>
<span data-ttu-id="c7e1a-181">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="c7e1a-181">Redmond, WA 98034</span></span><br>

<span data-ttu-id="c7e1a-182">Il y a trois jetons dans *(mobile)*  :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-182">There are three tokens in *(mobile)*:</span></span>

|<span data-ttu-id="c7e1a-183">Expression</span><span class="sxs-lookup"><span data-stu-id="c7e1a-183">Phrase</span></span>|<span data-ttu-id="c7e1a-184">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="c7e1a-184">Token count</span></span>|
|--|--|
|<span data-ttu-id="c7e1a-185">(</span><span class="sxs-lookup"><span data-stu-id="c7e1a-185">(</span></span>|<span data-ttu-id="c7e1a-186">1</span><span class="sxs-lookup"><span data-stu-id="c7e1a-186">1</span></span>|
|<span data-ttu-id="c7e1a-187">mobile</span><span class="sxs-lookup"><span data-stu-id="c7e1a-187">mobile</span></span>|<span data-ttu-id="c7e1a-188">2</span><span class="sxs-lookup"><span data-stu-id="c7e1a-188">2</span></span>|
|<span data-ttu-id="c7e1a-189">)</span><span class="sxs-lookup"><span data-stu-id="c7e1a-189">)</span></span>|<span data-ttu-id="c7e1a-190">3</span><span class="sxs-lookup"><span data-stu-id="c7e1a-190">3</span></span>|

<span data-ttu-id="c7e1a-191">Configurez le paramètre de proximité pour avoir une plage de 0 à 3.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-191">Configure the proximity setting to have a range of 0 through 3.</span></span>

   ![Exemple de proximité](../media/content-understanding/proximity-example.png)</br>

## <a name="use-explanation-templates"></a><span data-ttu-id="c7e1a-193">Utiliser des modèles d’explication</span><span class="sxs-lookup"><span data-stu-id="c7e1a-193">Use explanation templates</span></span>

<span data-ttu-id="c7e1a-194">Bien que vous puissiez ajouter manuellement différentes valeurs de liste de modèles pour votre explication, il peut être beaucoup plus facile d’utiliser les modèles pré-créés qui vous sont fournis dans la bibliothèque d’explications.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-194">While you can manually add various pattern list values for your explanation, it can be much easier to use the pre-created templates provided to you in the explanation library.</span></span>

<span data-ttu-id="c7e1a-195">Par exemple, au lieu d’ajouter manuellement toutes les variantes de *Date*, vous pouvez utiliser le modèle de liste de modèles pour *Date*, qui comprend déjà un certain nombre de valeurs de listes de modèles :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-195">For example, instead of manually adding all the variations for *Date*, you can use the pattern list template for *Date*, that already includes a number of pattern lists values:</span></span></br>

   ![Bibliothèque d’explications](../media/content-understanding/explanation-template.png)</br>
 
<span data-ttu-id="c7e1a-197">La bibliothèque d’explications comprend plusieurs explications de liste de modèles couramment utilisées, notamment :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-197">The explanation library includes a number of commonly used pattern list explanations, including:</span></span></br>

- <span data-ttu-id="c7e1a-198">Date</span><span class="sxs-lookup"><span data-stu-id="c7e1a-198">Date</span></span></br>
- <span data-ttu-id="c7e1a-199">Données (numériques)</span><span class="sxs-lookup"><span data-stu-id="c7e1a-199">Date (numeric)</span></span></br>
- <span data-ttu-id="c7e1a-200">Temps</span><span class="sxs-lookup"><span data-stu-id="c7e1a-200">Time</span></span></br>
- <span data-ttu-id="c7e1a-201">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7e1a-201">Number</span></span></br>
- <span data-ttu-id="c7e1a-202">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="c7e1a-202">Phone number</span></span></br>
- <span data-ttu-id="c7e1a-203">Code postal</span><span class="sxs-lookup"><span data-stu-id="c7e1a-203">Zip code</span></span></br>
- <span data-ttu-id="c7e1a-204">Premier mot de la phrase</span><span class="sxs-lookup"><span data-stu-id="c7e1a-204">First word of sentence</span></span></br>
- <span data-ttu-id="c7e1a-205">Carte bancaire</span><span class="sxs-lookup"><span data-stu-id="c7e1a-205">Credit card</span></span></br>
- <span data-ttu-id="c7e1a-206">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="c7e1a-206">Social security number</span></span></br>

<span data-ttu-id="c7e1a-207">Notez que la bibliothèque d’explications comprend également des modèles pour les explications de liste d’expressions, notamment :</span><span class="sxs-lookup"><span data-stu-id="c7e1a-207">Note that the explanation library also includes templates for phrase list explanations as well, including:</span></span>
- <span data-ttu-id="c7e1a-208">Fin de la phrase</span><span class="sxs-lookup"><span data-stu-id="c7e1a-208">End of sentence</span></span>
- <span data-ttu-id="c7e1a-209">Devise</span><span class="sxs-lookup"><span data-stu-id="c7e1a-209">Currency</span></span>

#### <a name="to-use-a-template-from-the-explanation-library"></a><span data-ttu-id="c7e1a-210">Pour utiliser un modèle de la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="c7e1a-210">To use a template from the explanation library</span></span>

1. <span data-ttu-id="c7e1a-211">Dans la section **Explications** de la page **Entraîner** de votre modèle, sélectionnez **Nouveau**, puis **À partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-211">From the **Explanations** section of your model's **Train** page, select **New**, then select **From a template**.</span></span></br>

   ![Créer à partir d’un modèle](../media/content-understanding/from-template.png)</br>

2.  <span data-ttu-id="c7e1a-213">Sur la page **Modèles d’explication**, sélectionnez l’explication que vous souhaitez utiliser, puis **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-213">On the **Explanation templates** page, select the explanation you want to use, and then select **Add**.</span></span></br>

       ![Sélectionner un modèle](../media/content-understanding/phone-template.png)</br>

3. <span data-ttu-id="c7e1a-215">Les informations relatives au modèle que vous avez sélectionné s’affichent sur la page **Créer une explication**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-215">The information for the template you selected will display on the **Create an explanation** page.</span></span> <span data-ttu-id="c7e1a-216">Si nécessaire, modifiez le nom de l’explication et ajoutez ou supprimez des éléments de la liste des modèles.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-216">If needed, edit the explanation name, and add or remove items from the pattern list.</span></span> </br> 

   ![Modifier le modèle](../media/content-understanding/phone-template-live.png)</br>

4. <span data-ttu-id="c7e1a-218">Lorsque vous avez terminé, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c7e1a-218">When finished, select **Save**.</span></span>
