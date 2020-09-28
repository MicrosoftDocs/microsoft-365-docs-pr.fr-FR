---
title: Types d’explications
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 10/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: En savoir plus sur les types d’explications dans Microsoft SharePoint Syntex
ms.openlocfilehash: f4f5dbc24bef57b1801f7df1b7e2fc7ef9b08116
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295849"
---
# <a name="introduction-to-explanation-types"></a><span data-ttu-id="e1469-103">Présentation des types d’explications</span><span class="sxs-lookup"><span data-stu-id="e1469-103">Introduction to explanation types</span></span>

<span data-ttu-id="e1469-104">Utilisez des explications pour définir les informations que vous souhaitez étiqueter et extrayez dans votre document les modèles de présentation pour Microsoft SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="e1469-104">Use explanations to help to define the information that you want to label, and extract in your document the understanding models for Microsoft SharePoint Syntex.</span></span> <span data-ttu-id="e1469-105">Lorsque vous créez une explication, veillez à sélectionner un type d’explication.</span><span class="sxs-lookup"><span data-stu-id="e1469-105">When you create an explanation, be sure to select an explanation type.</span></span> 

<span data-ttu-id="e1469-106">Cet article vous aide à comprendre les différents types d’explications et la façon dont ils sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="e1469-106">This article helps you understand the different explanation types and how they are used.</span></span>

   ![Types d’explications](../media/content-understanding/explanation-types.png) 
   
<span data-ttu-id="e1469-108">Ces types d’explications sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="e1469-108">These explanation types are available:</span></span>

- <span data-ttu-id="e1469-109">**Liste d’expressions**: liste de mots, d’expressions, de nombres ou d’autres caractères que vous pouvez utiliser dans le document ou des informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="e1469-109">**Phrase list**: List of words, phrases, numbers, or other characters you can use in the document or information that you are extracting.</span></span> <span data-ttu-id="e1469-110">Par exemple, la chaîne de texte **faisant référence à médecin** se trouve dans tous les documents de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="e1469-110">For example, the text string **Referring Doctor** is in all Medical Referral documents you are identifying.</span></span></br>

- <span data-ttu-id="e1469-111">**Liste de motifs**: modèles de liste de nombres, lettres ou autres caractères que vous pouvez utiliser pour identifier les informations que vous extrayez.</span><span class="sxs-lookup"><span data-stu-id="e1469-111">**Pattern list**: List patterns of numbers, letters, or other characters that you can use to identify the information that you are extracting.</span></span> <span data-ttu-id="e1469-112">Par exemple, vous pouvez extraire le **numéro de téléphone** du docteur de référence à partir de l’ensemble du document de référence médicale que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="e1469-112">For example, you can extract the **Phone number** of the referring doctor from all Medical Referral document that you are identifying.</span></span></br>

- <span data-ttu-id="e1469-113">**Proximité**: décrit le mode de fermeture des explications.</span><span class="sxs-lookup"><span data-stu-id="e1469-113">**Proximity**: Describes how close explanations are to each other.</span></span> <span data-ttu-id="e1469-114">Par exemple, une liste de modèles de *numéro de rue* se place juste avant la liste d’expressions de *nom de rue* , sans jeton entre les points (vous allez découvrir les jetons plus loin dans cet article).</span><span class="sxs-lookup"><span data-stu-id="e1469-114">For example, a *street number* pattern list goes right before the *street name* phrase list, with no tokens in between (you'll learn about tokens later in this article).</span></span> 
 
## <a name="phrase-list"></a><span data-ttu-id="e1469-115">Liste des expressions</span><span class="sxs-lookup"><span data-stu-id="e1469-115">Phrase list</span></span>

<span data-ttu-id="e1469-116">Un type d’explication de liste d’expressions est généralement utilisé pour identifier et classer un document par le biais de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="e1469-116">A phrase list explanation type is typically used to identify and classify a document through your model.</span></span> <span data-ttu-id="e1469-117">Comme décrit dans l’exemple d’étiquette *Doctor de référence* , il s’agit d’une chaîne de mots, d’expressions, de chiffres ou de caractères qui est cohérente dans les documents que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="e1469-117">As described in the *Referring Doctor* label example, it is a string of words, phrases, numbers, or characters that is consistently in the documents that you are identifying.</span></span>

<span data-ttu-id="e1469-118">Bien que ce ne soit pas obligatoire, vous pouvez obtenir une meilleure réussite avec votre explication si l’expression que vous capturez se trouve à un emplacement cohérent dans votre document.</span><span class="sxs-lookup"><span data-stu-id="e1469-118">While not a requirement, you can acheive better success with your explanation if the phrase you are capturing is located in a consistent location in your document.</span></span> <span data-ttu-id="e1469-119">Par exemple, l’étiquette *médecin de référence* peut se trouver régulièrement dans le premier paragraphe du document.</span><span class="sxs-lookup"><span data-stu-id="e1469-119">For example, the *Referring Doctor* label may be consistently located in the first paragraph of the document.</span></span>

<span data-ttu-id="e1469-120">Si le respect de la casse est une condition requise pour l’identification de votre étiquette, l’utilisation du type de liste phrase vous permet de la spécifier dans votre explication en activant la seule case à cocher **majuscule exacte** .</span><span class="sxs-lookup"><span data-stu-id="e1469-120">If case sensitivity is a requirement in identifying your label, using the phrase list type allows you to specify it in your explanation by selecting the **Only exact capitalization** checkbox.</span></span>

   ![Respect de la casse](../media/content-understanding/case-sensitivity.png) 

## <a name="pattern-lists"></a><span data-ttu-id="e1469-122">Listes de modèles</span><span class="sxs-lookup"><span data-stu-id="e1469-122">Pattern lists</span></span>

<span data-ttu-id="e1469-123">Un type de liste de motifs est particulièrement utile lorsque vous créez une explication qui identifie et extrait des informations d’un document.</span><span class="sxs-lookup"><span data-stu-id="e1469-123">A pattern list type is especially useful when you create an explanation that identifies and extracts information from a document.</span></span> <span data-ttu-id="e1469-124">Il est généralement présenté sous différents formats, tels que des dates, des numéros de téléphone ou des numéros de carte de crédit.</span><span class="sxs-lookup"><span data-stu-id="e1469-124">It is typically presented in different formats, such as dates, phone numbers, or credit card numbers.</span></span> <span data-ttu-id="e1469-125">Par exemple, une date peut être affichée dans différents formats (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, Jan 1, 2020, etc.).</span><span class="sxs-lookup"><span data-stu-id="e1469-125">For example, a date can be displayed in a number of different formats (1/1/2020, 1-1-2020, 01/01/20, 01/01/2020, Jan 1,2020, etc.).</span></span> <span data-ttu-id="e1469-126">La définition d’une liste de modèles rend votre explication plus efficace en capturant toutes les variantes possibles dans les données que vous tentez d’identifier et d’extraire.</span><span class="sxs-lookup"><span data-stu-id="e1469-126">Defining a pattern list makes your explanation more efficient by capturing any possible variations in the data that you are trying to identify and extract.</span></span> 

<span data-ttu-id="e1469-127">Pour l’exemple de **numéro de téléphone** , extrayez le numéro de téléphone de chaque docteur de référence de tous les documents de référence médicale que le modèle identifie.</span><span class="sxs-lookup"><span data-stu-id="e1469-127">For the **Phone number** sample, extract the phone number for each referring doctor from all Medical Referral documents that the model identifies.</span></span> <span data-ttu-id="e1469-128">Lorsque vous créez l’explication, sélectionnez le type de liste motif pour autoriser les différents formats susceptibles d’être renvoyés.</span><span class="sxs-lookup"><span data-stu-id="e1469-128">When you create the explanation, select the Pattern list type to allow the different formats that you may expect to be returned.</span></span>

   ![Liste de modèles de numéros de téléphone](../media/content-understanding/pattern-list.png)

<span data-ttu-id="e1469-130">Pour cet exemple, activez la case à cocher **tout chiffre de 0-9** .</span><span class="sxs-lookup"><span data-stu-id="e1469-130">For this sample, select the **Any digit from 0-9** checkbox.</span></span> <span data-ttu-id="e1469-131">La sélection de cette option permet de reconnaître chaque valeur « 0 » utilisée dans votre liste de motifs comme un chiffre compris entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="e1469-131">Selecting this recognizes each "0" value used in your pattern list to be any digit from 0 through 9.</span></span>

   ![N’importe quel chiffre de 0-9](../media/content-understanding/digit-identity.png)

<span data-ttu-id="e1469-133">De même, si vous créez une liste de motifs qui inclut des caractères de texte, sélectionnez toutes les lettres de la case à cocher **a-z** .</span><span class="sxs-lookup"><span data-stu-id="e1469-133">Similarly, if you create a pattern list that includes text characters, select the **Any letter from a-z** checkbox.</span></span> <span data-ttu-id="e1469-134">La sélection de cette option reconnaît tous les caractères « a » utilisés dans la liste motif comme n’importe quel caractère compris entre « a » et « z ».</span><span class="sxs-lookup"><span data-stu-id="e1469-134">Selecting this recognizes each "a" character used in the pattern list to be any character from "a" to "z".</span></span>

<span data-ttu-id="e1469-135">Par exemple, si vous créez une liste de modèles de **Date** et que vous souhaitez vous assurer qu’un format de date, tel que le *1er janvier 2020* , est reconnu, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1469-135">For example, if you create a **Date** pattern list and you want to make sure that a date format such as *Jan 1, 2020* is recognized, you need to:</span></span>
- <span data-ttu-id="e1469-136">Ajoutez les *AAA 0, 0000* et *AAA 00, 0000* à votre liste de motifs.</span><span class="sxs-lookup"><span data-stu-id="e1469-136">Add *aaa 0, 0000* and *aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="e1469-137">Assurez-vous que **toute lettre comprise entre a et z** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1469-137">Make sure that **Any letter from a-z** is also selected.</span></span>

   ![N’importe quelle lettre de a à z](../media/content-understanding/any-letter.png)

<span data-ttu-id="e1469-139">En outre, si votre liste de motifs comporte des exigences de majuscules, vous avez la possibilité de sélectionner la seule case à cocher mise en **majuscules exacte** .</span><span class="sxs-lookup"><span data-stu-id="e1469-139">Additionally, if you have capitalization requirements in your pattern list, you have the option to select the **Only exact capitalization** checkbox.</span></span> <span data-ttu-id="e1469-140">Pour l’exemple de date, si vous avez besoin que la première lettre du mois soit capitalisée, vous devez :</span><span class="sxs-lookup"><span data-stu-id="e1469-140">For the Date example, if you require the first letter of the month to be capitalized, you need to:</span></span>

- <span data-ttu-id="e1469-141">Ajoutez les *AAA 0, 0000* et *AAA 00, 0000* à votre liste de motifs.</span><span class="sxs-lookup"><span data-stu-id="e1469-141">Add *Aaa 0, 0000* and *Aaa 00, 0000* to your pattern list.</span></span>
- <span data-ttu-id="e1469-142">Assurez-vous que **seule la casse exacte** est également sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e1469-142">Make sure that **Only exact capitalization** is also selected.</span></span>

   ![Majuscule exacte uniquement](../media/content-understanding/exact-caps.png)

> [!NOTE]
> <span data-ttu-id="e1469-144">Au lieu de créer manuellement une explication de liste de motifs, utilisez la [bibliothèque d’explication]() pour utiliser des modèles de liste de modèles prédéfinis pour une liste de modèles commune, comme une *Date*, un *numéro de téléphone*, *un numéro de carte de crédit*, etc..</span><span class="sxs-lookup"><span data-stu-id="e1469-144">Instead of manually creating pattern list explanation, use the [explanation library]() to use pre-made pattern list templates for common pattern list, such as *date*, *phone number*, *credit card number*, etc..</span></span> 

## <a name="proximity"></a><span data-ttu-id="e1469-145">Proximité</span><span class="sxs-lookup"><span data-stu-id="e1469-145">Proximity</span></span> 

<span data-ttu-id="e1469-146">Le type d’explication de proximité aide votre modèle à identifier les données par le biais de la définition de la fermeture d’un autre élément de données.</span><span class="sxs-lookup"><span data-stu-id="e1469-146">The proximity explanation type helps your model identify data through defining how close another piece of data is to it.</span></span> <span data-ttu-id="e1469-147">Par exemple, dans votre modèle, vous avez défini deux explications qui étiquetent le *numéro d’adresse* et le *numéro de téléphone*du client.</span><span class="sxs-lookup"><span data-stu-id="e1469-147">For example, in your model, you have defined two explanations that label both the customer *Street address number* and *Phone number*.</span></span> 

<span data-ttu-id="e1469-148">Vous pouvez également remarquer que les numéros de téléphone des clients apparaissent toujours avant le numéro d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="e1469-148">You also notice that customer phone numbers always appear before the street address number.</span></span> 

<span data-ttu-id="e1469-149">Alex Wilburn</span><span class="sxs-lookup"><span data-stu-id="e1469-149">Alex Wilburn</span></span><br>
<span data-ttu-id="e1469-150">555-555-5555</span><span class="sxs-lookup"><span data-stu-id="e1469-150">555-555-5555</span></span><br>
<span data-ttu-id="e1469-151">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="e1469-151">One Microsoft Way</span></span><br>
<span data-ttu-id="e1469-152">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="e1469-152">Redmond, WA 98034</span></span><br>

<span data-ttu-id="e1469-153">Utilisez l’explication de proximité pour définir la distance de l’explication du numéro de téléphone afin de mieux identifier le numéro d’adresse postale dans vos documents.</span><span class="sxs-lookup"><span data-stu-id="e1469-153">Use the proximity explanation to define how far away the phone number explanation is to better identify the street address number in your documents.</span></span>

   ![Explication de proximité](../media/content-understanding/proximity.png)</br>

#### <a name="what-are-tokens"></a><span data-ttu-id="e1469-155">Qu’est-ce qu’un jeton ?</span><span class="sxs-lookup"><span data-stu-id="e1469-155">What are tokens?</span></span>

<span data-ttu-id="e1469-156">Pour utiliser le type d’explication de proximité, vous pouvez comprendre ce qu’est un jeton, car le nombre de jetons mesure la distance d’une explication à une autre.</span><span class="sxs-lookup"><span data-stu-id="e1469-156">In order to use the proximity explanation type, understand what a token is, as the number of tokens is how the proximity explanation measures distance from one explanation to another.</span></span>  

<span data-ttu-id="e1469-157">Un jeton est une plage continue (sans espace ni ponctuation) de lettres et de chiffres.</span><span class="sxs-lookup"><span data-stu-id="e1469-157">A token is a continuous span (no spaces or punctuation) of letters and numbers.</span></span> <span data-ttu-id="e1469-158">Un espace n’est pas un jeton.</span><span class="sxs-lookup"><span data-stu-id="e1469-158">A space is NOT a token.</span></span> <span data-ttu-id="e1469-159">Chaque caractère de ponctuation est un jeton.</span><span class="sxs-lookup"><span data-stu-id="e1469-159">Each punctuation character is a token.</span></span> <span data-ttu-id="e1469-160">Le tableau suivant montre quelques exemples illustrant comment déterminer le nombre de jetons dans une expression.</span><span class="sxs-lookup"><span data-stu-id="e1469-160">The following table shows some examples of how to determine the number of tokens in a phrase.</span></span>

|<span data-ttu-id="e1469-161">Souhaitée</span><span class="sxs-lookup"><span data-stu-id="e1469-161">Phrase</span></span>|<span data-ttu-id="e1469-162">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="e1469-162">Number of tokens</span></span>|<span data-ttu-id="e1469-163">Explication</span><span class="sxs-lookup"><span data-stu-id="e1469-163">Explanation</span></span>|
|--|--|--|
|`Dog`|<span data-ttu-id="e1469-164">1 </span><span class="sxs-lookup"><span data-stu-id="e1469-164">1</span></span>|<span data-ttu-id="e1469-165">Un seul mot sans ponctuation ou espaces.</span><span class="sxs-lookup"><span data-stu-id="e1469-165">A single word with no punctuation or spaces.</span></span>|
|`RMT33W`|<span data-ttu-id="e1469-166">1 </span><span class="sxs-lookup"><span data-stu-id="e1469-166">1</span></span>|<span data-ttu-id="e1469-167">Numéro de localisateur d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e1469-167">A record locator number.</span></span> <span data-ttu-id="e1469-168">Il peut contenir des chiffres et des lettres, mais n’a pas de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="e1469-168">It may have numbers and letters, but does not have any punctuation.</span></span>|
|`425-555-5555`|<span data-ttu-id="e1469-169">5 </span><span class="sxs-lookup"><span data-stu-id="e1469-169">5</span></span>|<span data-ttu-id="e1469-170">Un numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="e1469-170">A phone number.</span></span> <span data-ttu-id="e1469-171">Chaque signe de ponctuation est un jeton unique de sorte qu’il s’agit de  `425-555-5555` 5 jetons :</span><span class="sxs-lookup"><span data-stu-id="e1469-171">Each punctuation mark is a single token so  `425-555-5555` would be 5 tokens:</span></span><br>`425`<br>`-`<br>`555`<br>`-`<br>`5555` |
|`https://luis.ai`|<span data-ttu-id="e1469-172">7 </span><span class="sxs-lookup"><span data-stu-id="e1469-172">7</span></span>|`https`<br>`:`<br>`/`<br>`/`<br>`luis`<br>`.`<br>`ai`<br>|

#### <a name="configure-the-proximity-explanation-type"></a><span data-ttu-id="e1469-173">Configurer le type d’explication de proximité</span><span class="sxs-lookup"><span data-stu-id="e1469-173">Configure the proximity explanation type</span></span>

<span data-ttu-id="e1469-174">Pour l’exemple, configurez le paramètre de proximité de manière à pouvoir définir la plage du nombre de jetons dont le numéro de *téléphone* explique l’explication relative au *numéro d’adresse postale* .</span><span class="sxs-lookup"><span data-stu-id="e1469-174">For the sample, configure the proximity setting so that we can define the range of the number of tokens the *Phone number* explanation is from the *Street address number* explanation.</span></span>

<span data-ttu-id="e1469-175">Vous devriez voir que la plage minimale est « 0 », car il n’y a aucun jeton entre le numéro de téléphone et le numéro d’adresse postale.</span><span class="sxs-lookup"><span data-stu-id="e1469-175">You should see that the minimum range is "0" since there are no tokens between the phone number and street address number.</span></span>

<span data-ttu-id="e1469-176">Toutefois, certains numéros de téléphone dans les exemples de documents sont ajoutés avec *(mobile)*.</span><span class="sxs-lookup"><span data-stu-id="e1469-176">However, some phone numbers in the sample documents are appended with *(mobile)*.</span></span>

<span data-ttu-id="e1469-177">Nestor Wilke</span><span class="sxs-lookup"><span data-stu-id="e1469-177">Nestor Wilke</span></span><br>
<span data-ttu-id="e1469-178">111-111-1111 (mobile)</span><span class="sxs-lookup"><span data-stu-id="e1469-178">111-111-1111 (mobile)</span></span><br>
<span data-ttu-id="e1469-179">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="e1469-179">One Microsoft Way</span></span><br>
<span data-ttu-id="e1469-180">Redmond, WA 98034</span><span class="sxs-lookup"><span data-stu-id="e1469-180">Redmond, WA 98034</span></span><br>

<span data-ttu-id="e1469-181">Il y a trois jetons dans *(mobile)*:</span><span class="sxs-lookup"><span data-stu-id="e1469-181">There are three tokens in *(mobile)*:</span></span>

|<span data-ttu-id="e1469-182">Souhaitée</span><span class="sxs-lookup"><span data-stu-id="e1469-182">Phrase</span></span>|<span data-ttu-id="e1469-183">Nombre de jetons</span><span class="sxs-lookup"><span data-stu-id="e1469-183">Token count</span></span>|
|--|--|
|<span data-ttu-id="e1469-184">(</span><span class="sxs-lookup"><span data-stu-id="e1469-184">(</span></span>|<span data-ttu-id="e1469-185">1 </span><span class="sxs-lookup"><span data-stu-id="e1469-185">1</span></span>|
|<span data-ttu-id="e1469-186">Mobile</span><span class="sxs-lookup"><span data-stu-id="e1469-186">mobile</span></span>|<span data-ttu-id="e1469-187">2 </span><span class="sxs-lookup"><span data-stu-id="e1469-187">2</span></span>|
|<span data-ttu-id="e1469-188">)</span><span class="sxs-lookup"><span data-stu-id="e1469-188">)</span></span>|<span data-ttu-id="e1469-189">3 </span><span class="sxs-lookup"><span data-stu-id="e1469-189">3</span></span>|

<span data-ttu-id="e1469-190">Configurez le paramètre de proximité sur une plage comprise entre 0 et 3.</span><span class="sxs-lookup"><span data-stu-id="e1469-190">Configure the proximity setting to have a range of 0 through 3.</span></span>

   ![Exemple de proximité](../media/content-understanding/proximity-example.png)</br>

## <a name="use-the-explanation-library"></a><span data-ttu-id="e1469-192">Utiliser la bibliothèque d’explication</span><span class="sxs-lookup"><span data-stu-id="e1469-192">Use the explanation library</span></span>

<span data-ttu-id="e1469-193">Bien que vous puissiez ajouter manuellement différentes valeurs de liste de modèles pour votre explication, il est plus facile d’utiliser les modèles pré-créés fournis dans la bibliothèque d’explication.</span><span class="sxs-lookup"><span data-stu-id="e1469-193">While you can manually add various pattern list values for your explanation, it's much easier to use the pre-created templates provided to you in the explanation library.</span></span>

<span data-ttu-id="e1469-194">Par exemple, au lieu d’ajouter manuellement toutes les variantes de *Date*, utilisez le modèle de liste de modèles pour *Date*, qui inclut déjà un certain nombre de valeurs de liste de modèles :</span><span class="sxs-lookup"><span data-stu-id="e1469-194">For example, instead of manually adding all the variations for *Date*, use the pattern list template for *Date*, that already includes a number of pattern lists values:</span></span></br>

   ![Bibliothèque d’explications](../media/content-understanding/explanation-template.png)</br>
 
<span data-ttu-id="e1469-196">La bibliothèque d’explications comprend un certain nombre d’explications de liste de modèles communément utilisées, notamment :</span><span class="sxs-lookup"><span data-stu-id="e1469-196">The explanation library includes a number of commonly used pattern list explanations, including:</span></span></br>

- <span data-ttu-id="e1469-197">Date</span><span class="sxs-lookup"><span data-stu-id="e1469-197">Date</span></span></br>
- <span data-ttu-id="e1469-198">Date (numérique)</span><span class="sxs-lookup"><span data-stu-id="e1469-198">Date (numeric)</span></span></br>
- <span data-ttu-id="e1469-199">Time</span><span class="sxs-lookup"><span data-stu-id="e1469-199">Time</span></span></br>
- <span data-ttu-id="e1469-200">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1469-200">Number</span></span></br>
- <span data-ttu-id="e1469-201">Numéro de téléphone</span><span class="sxs-lookup"><span data-stu-id="e1469-201">Phone number</span></span></br>
- <span data-ttu-id="e1469-202">Code postal</span><span class="sxs-lookup"><span data-stu-id="e1469-202">Zip code</span></span></br>
- <span data-ttu-id="e1469-203">Premier mot de phrase</span><span class="sxs-lookup"><span data-stu-id="e1469-203">First word of sentence</span></span></br>
- <span data-ttu-id="e1469-204">Carte de crédit</span><span class="sxs-lookup"><span data-stu-id="e1469-204">Credit card</span></span></br>
- <span data-ttu-id="e1469-205">Numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="e1469-205">Social security number</span></span></br>

<span data-ttu-id="e1469-206">Notez que la bibliothèque d’explications inclut également des modèles pour les explications de la liste des phrases, notamment :</span><span class="sxs-lookup"><span data-stu-id="e1469-206">Note that the explanation library also includes templates for phrase list explanations as well, including:</span></span>
- <span data-ttu-id="e1469-207">Fin de la phrase</span><span class="sxs-lookup"><span data-stu-id="e1469-207">End of sentence</span></span>
- <span data-ttu-id="e1469-208">Monétaire</span><span class="sxs-lookup"><span data-stu-id="e1469-208">Currency</span></span>

#### <a name="to-use-a-template-from-the-explanation-library"></a><span data-ttu-id="e1469-209">Pour utiliser un modèle à partir de la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="e1469-209">To use a template from the explanation library</span></span>

1. <span data-ttu-id="e1469-210">Dans la section **explications** de la page de **formation** de votre modèle, sélectionnez **nouveau**, puis sélectionnez **à partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="e1469-210">From the **Explanations** section of your model's **Train** page, select **New**, then select **From a template**.</span></span></br>

   ![Créer à partir d’un modèle](../media/content-understanding/from-template.png)</br>

2.  <span data-ttu-id="e1469-212">Sur la page **modèles d’explication** , sélectionnez l’explication que vous souhaitez utiliser, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e1469-212">On the **Explanation templates** page, select the explanation you want to use, and then select **Add**.</span></span></br>

       ![Sélectionner un modèle](../media/content-understanding/phone-template.png)</br>

3. <span data-ttu-id="e1469-214">Les informations du modèle que vous avez sélectionné s’afficheront dans la page **créer une explication** .</span><span class="sxs-lookup"><span data-stu-id="e1469-214">The information for the template you selected will display on the **Create an explanation** page.</span></span> <span data-ttu-id="e1469-215">Si nécessaire, modifiez le nom de l’explication, puis ajoutez ou supprimez des éléments dans la liste motif.</span><span class="sxs-lookup"><span data-stu-id="e1469-215">If needed, edit the explanation name, and add or remove items from the pattern list.</span></span> </br> 

   ![Modifier le modèle](../media/content-understanding/phone-template-live.png)</br>

4. <span data-ttu-id="e1469-217">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e1469-217">When finished, select **Save**.</span></span>
