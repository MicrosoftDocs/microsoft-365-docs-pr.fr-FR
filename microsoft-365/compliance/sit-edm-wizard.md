---
title: Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
ms.date: ''
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: d9d6f870239b963ee7483b9f08e93e40b10f4f0b
ms.sourcegitcommit: 337e8d8a2fee112d799edd8a0e04b3a2f124f900
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52878003"
---
# <a name="use-the-exact-data-match-schema-and-sensitive-information-type-wizard"></a><span data-ttu-id="19b4d-103">Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="19b4d-103">Use the Exact Data Match Schema and Sensitive Information Type Wizard</span></span>

<span data-ttu-id="19b4d-104">La [Création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) implique de nombreuses étapes.</span><span class="sxs-lookup"><span data-stu-id="19b4d-104">[Creating a custom sensitive information type with Exact Data Match (EDM) based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)  involves many steps.</span></span>  <span data-ttu-id="19b4d-105">Vous pouvez utiliser cet Assistant pour créer votre schéma et vos fichiers de modèle de type d’informations sensibles (SIT) (package de règles) pour simplifier le processus.</span><span class="sxs-lookup"><span data-stu-id="19b4d-105">You can use this wizard to create your schema and sensitive information type (SIT) pattern (rule package) files to help simplify the process.</span></span>

> [!NOTE]
> <span data-ttu-id="19b4d-106">L’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles est disponible uniquement pour les nuages mondiaux et GCC.</span><span class="sxs-lookup"><span data-stu-id="19b4d-106">The Exact Data Match Schema and Sensitive Information Type Wizard is only available for the World Wide and GCC clouds only.</span></span>

<span data-ttu-id="19b4d-107">Cet Assistant peut être utilisé à la place des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="19b4d-107">This wizard can be used instead of the:</span></span>

- [<span data-ttu-id="19b4d-108">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="19b4d-108">Define the schema for your database of sensitive information</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#define-the-schema-for-your-database-of-sensitive-information)
- [<span data-ttu-id="19b4d-109">Configurer un modèle (package de règles)</span><span class="sxs-lookup"><span data-stu-id="19b4d-109">Set up a pattern (rule package)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#set-up-a-rule-package)

<span data-ttu-id="19b4d-110">dans [Partie 1 : configurer la classification EDM](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-1-set-up-edm-based-classification).</span><span class="sxs-lookup"><span data-stu-id="19b4d-110">steps in [Part 1: Set up EDM-based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-1-set-up-edm-based-classification).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="19b4d-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="19b4d-111">Pre-requisites</span></span>

1. <span data-ttu-id="19b4d-112">Familiarisez-vous avec les étapes de création d’un type d’informations sensibles personnalisées avec le [flux de travail EDM en un clin d’œil](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#the-work-flow-at-a-glance).</span><span class="sxs-lookup"><span data-stu-id="19b4d-112">Familiarize yourself with the steps to create a custom sensitive information type with EDM [work flow at a glance](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#the-work-flow-at-a-glance).</span></span>

2. <span data-ttu-id="19b4d-113">Effectuez les étapes de [l’étape Enregistrer les données sensibles .csv au format .tsv](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#save-sensitive-data-in-csv-or-tsv-format).</span><span class="sxs-lookup"><span data-stu-id="19b4d-113">Perform the steps in [Save sensitive data in .csv or .tsv format](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#save-sensitive-data-in-csv-or-tsv-format).</span></span>

## <a name="use-the-exact-data-match-schema-and-sensitive-information-type-pattern-wizard"></a><span data-ttu-id="19b4d-114">Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="19b4d-114">Use the exact data match schema and sensitive information type pattern wizard</span></span>

1. <span data-ttu-id="19b4d-115">Dans le Centre de conformité Microsoft 365 pour votre client, accédez à **Classification des données** > **Correspondances exactes des données**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-115">In the Microsoft 365 Compliance center for your tenant go to **Data classification** > **Exact data matches**.</span></span>

2. <span data-ttu-id="19b4d-116">Choisissez **Créer un schéma EDM** pour ouvrir le menu volant de configuration de l’Assistant de schéma.</span><span class="sxs-lookup"><span data-stu-id="19b4d-116">Choose **Create EDM schema** to open the schema wizard configuration flyout.</span></span>

![Menu volant de configuration de l’Assistant de création de schéma EDM](../media/edm-schema-wizard-1.png)

3. <span data-ttu-id="19b4d-118">Indiquez un nom **approprié** et **Description**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-118">Fill in an appropriate **Name** and **Description**.</span></span>

4. <span data-ttu-id="19b4d-119">Choisissez **Ignorer les délimiteur et la ponctuation pour tous** les champs de schéma si vous souhaitez ce comportement.</span><span class="sxs-lookup"><span data-stu-id="19b4d-119">Choose **Ignore delimiters and punctuation for all schema fields** if you want that behavior.</span></span> <span data-ttu-id="19b4d-120">Pour en savoir plus sur la configuration d’EDM pour ignorer les cas ou les délimiteur, voir Création d’un type d’informations sensibles personnalisé avec la [classification EDM (Exact Data Match).](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)</span><span class="sxs-lookup"><span data-stu-id="19b4d-120">To learn more about configuring EDM to ignore case or delimiters, see [Creating a custom sensitive information type with Exact Data Match (EDM) based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

5. <span data-ttu-id="19b4d-121">Renseignez les valeurs souhaitées pour votre **Champ de schéma n° 1** et ajoutez des champs si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="19b4d-121">Fill in your desired values for your **Schema field #1** and add more fields as needed.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="19b4d-122">Au moins un champ, mais pas plus de cinq, doivent être désignés comme pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="19b4d-122">At least one, but no more than five of your schema fields must be designated as searchable.</span></span>

6. <span data-ttu-id="19b4d-123">Cliquez sur Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="19b4d-123">Choose save.</span></span> <span data-ttu-id="19b4d-124">Votre schéma figure désormais dans la liste.</span><span class="sxs-lookup"><span data-stu-id="19b4d-124">Your schema will now be listed.</span></span>

7. <span data-ttu-id="19b4d-125">Choisissez **Types d’informations sensibles EDM** et **Créer un type d’informations sensibles EDM** pour ouvrir l’Assistant de configuration des types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="19b4d-125">Choose **EDM sensitive info types** and **Create EDM sensitive info type** to open the sensitive info type configuration wizard.</span></span>

8. <span data-ttu-id="19b4d-126">Choisissez **Choisir un schéma EDM existant** puis sélectionnez le schéma que vous avez créé dans les étapes 2-6 dans la liste.</span><span class="sxs-lookup"><span data-stu-id="19b4d-126">Choose **Choose an existing EDM schema** and choose the schema you created in steps 2-6 from the list.</span></span>

9. <span data-ttu-id="19b4d-127">Choisissez **Suivant**, puis **Créer un modèle**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-127">Choose **Next** and choose **Create pattern**.</span></span>

10. <span data-ttu-id="19b4d-128">Choisissez le **Niveau de confiance** et l’**Élément principal**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-128">Choose the **Confidence level** and **Primary element**.</span></span>  <span data-ttu-id="19b4d-129">Pour en savoir plus sur la configuration d’un modèle, voir [Créer un type d’informations sensibles personnalisé dans le Centre de conformité](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="19b4d-129">To learn more about configuring a pattern, see [Create a custom sensitive information type in the Compliance Center](create-a-custom-sensitive-information-type.md)</span></span>

11.  <span data-ttu-id="19b4d-130">Choisissez le **Type d’informations sensibles de l’élément principal** à associer.</span><span class="sxs-lookup"><span data-stu-id="19b4d-130">Choose the **Primary element's sensitive info type** to associate it with.</span></span> <span data-ttu-id="19b4d-131">Voir [Définitions des entités de types d’informations sensibles](sensitive-information-type-entity-definitions.md) pour en savoir plus sur les types d’informations sensibles disponibles.</span><span class="sxs-lookup"><span data-stu-id="19b4d-131">See [Sensitive Information Type Entity Definitions](sensitive-information-type-entity-definitions.md) to learn more about the available sensitive information types.</span></span>

12. <span data-ttu-id="19b4d-132">Choisissez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-132">Choose **Done**.</span></span>

13. <span data-ttu-id="19b4d-133">Choisissez vos **Niveau de confiance et proximité des caractères** souhaités.</span><span class="sxs-lookup"><span data-stu-id="19b4d-133">Choose your desired **Confidence level and character proximity**.</span></span>  <span data-ttu-id="19b4d-134">Il s’agit de la valeur par défaut pour l’ensemble du type d’informations sensibles EDM.</span><span class="sxs-lookup"><span data-stu-id="19b4d-134">This will be the default value for the whole EDM sensitive info type</span></span>

13. <span data-ttu-id="19b4d-135">Choisissez **Créer un modèle** si vous souhaitez créer des modèles supplémentaires pour votre type d’informations sensibles EDM.</span><span class="sxs-lookup"><span data-stu-id="19b4d-135">Choose **Create pattern** if you want to create additional patterns for your EDM sensitive info type.</span></span>

14. <span data-ttu-id="19b4d-136">Choisissez **Suivant**, puis entrez un **Nom** et une **Description pour les administrateurs**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-136">Choose **Next** and fill in a **Name** and **Description for admins**.</span></span>

15. <span data-ttu-id="19b4d-137">Passez en revue vos paramètres, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="19b4d-137">Review and choose **Submit**.</span></span>

<span data-ttu-id="19b4d-138">Vous pouvez supprimer ou modifier le modèle de type d’informations sensibles en le sélectionnant. Cela permet d’afficher les contrôles de modification et de suppression.</span><span class="sxs-lookup"><span data-stu-id="19b4d-138">You can delete or edit the sensitive information type pattern by selecting it which surfaces the edit and delete controls.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19b4d-139">Si vous voulez supprimer un schéma et que celui-ci est déjà associé à un type d’informations sensibles EDM, vous devez commencer par supprimer le type d’informations sensibles EDM. Vous pouvez ensuite supprimer le schéma.</span><span class="sxs-lookup"><span data-stu-id="19b4d-139">If you want to remove a schema, and it is already associated with an EDM sensitive info type, you must first delete the EDM sensitive info type, then you can delete the schema.</span></span>

## <a name="post-creation-steps"></a><span data-ttu-id="19b4d-140">Étapes de publication de la création</span><span class="sxs-lookup"><span data-stu-id="19b4d-140">Post creation steps</span></span>

<span data-ttu-id="19b4d-141">Une fois que vous avez utilisé cet Assistant pour créer vos fichiers de schéma et modèle EDM (package de règles), vous devez continuer à effectuer les étapes décrites dans [Partie 2 : hacher et charger les données sensibles](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-2-hash-and-upload-the-sensitive-data) avant de pouvoir utiliser le type d’informations sensibles personnalisé EDM.</span><span class="sxs-lookup"><span data-stu-id="19b4d-141">After you have used this wizard to create your EDM schema and pattern (rule package) files, you still have to perform the steps in [Part 2: Hash and upload the sensitive data](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-2-hash-and-upload-the-sensitive-data) before you can use the EDM custom sensitive information type.</span></span>

<span data-ttu-id="19b4d-142">Après avoir vérifié que votre table d’informations sensibles a été correctement téléchargée, vous pouvez vérifier qu’elle fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="19b4d-142">After verifying that your sensitive information table has correctly been uploaded, you can test that it's working properly.</span></span>

1. <span data-ttu-id="19b4d-143">Ouvrez **le Centre de conformité** Types  >  **d’informations**  >  **sensibles de classification des données.**</span><span class="sxs-lookup"><span data-stu-id="19b4d-143">Open **Compliance center** > **Data classification** > **Sensitive Information Types**.</span></span>
2. <span data-ttu-id="19b4d-144">Sélectionnez votre sit EDM dans la liste, puis **sélectionnez Tester** dans le volet volant.</span><span class="sxs-lookup"><span data-stu-id="19b4d-144">Select your EDM SIT from the list and then select **Test** in the flyout pane.</span></span> 
3. <span data-ttu-id="19b4d-145">Télécharger un élément qui contient des données que vous souhaitez détecter, par exemple, créez un élément qui contient certaines des données de votre table d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="19b4d-145">Upload an item that contains data you want to detect, for example create an item that contains some of the data in your sensitive information table.</span></span> <span data-ttu-id="19b4d-146">Si vous avez utilisé la fonctionnalité de correspondance configurable dans votre schéma pour définir des délimiteur ignorés, assurez-vous que l’élément inclut des exemples avec et sans ces délimiteur.</span><span class="sxs-lookup"><span data-stu-id="19b4d-146">If you used the configurable match feature in your schema to define ignored delimiters, make sure the item includes examples with and without those delimiters.</span></span>
4. <span data-ttu-id="19b4d-147">Une fois le fichier téléchargé et analysé, recherchez les correspondances avec votre sit EDM.</span><span class="sxs-lookup"><span data-stu-id="19b4d-147">After the file has been uploaded and scanned, check for matches to your EDM SIT.</span></span>
5. <span data-ttu-id="19b4d-148">Si la **fonction Test** dans la fonction SIT détecte une correspondance, vérifiez qu’elle ne le coupe pas ou ne l’extrait pas de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="19b4d-148">If the **Test** function in the SIT detects a match, check that it is not trimming it or extracting it incorrectly.</span></span> <span data-ttu-id="19b4d-149">Par exemple, en extrayant uniquement une sous-chaîne de la chaîne complète qu’elle est supposée détecter, ou en sélectionnant uniquement le premier mot d’une chaîne de plusieurs mots, ou en incluant des symboles ou des caractères supplémentaires dans l’extraction.</span><span class="sxs-lookup"><span data-stu-id="19b4d-149">For example by extracting only a substring of the full string it is supposed to detect, or picking up only the first word in a multi-word string, or including extra symbols or characters in the extraction.</span></span> <span data-ttu-id="19b4d-150">Voir [Langage des expressions régulières - Référence rapide pour](/dotnet/standard/base-types/regular-expression-language-quick-reference) la référence du langage d’expression régulière.</span><span class="sxs-lookup"><span data-stu-id="19b4d-150">See [Regular Expression Language - Quick Reference](/dotnet/standard/base-types/regular-expression-language-quick-reference) for the regular expression language reference.</span></span> 

### <a name="troubleshooting"></a><span data-ttu-id="19b4d-151">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="19b4d-151">Troubleshooting</span></span>

<span data-ttu-id="19b4d-152">Si vous ne trouvez aucune correspondance, essayez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="19b4d-152">If you don't find any matches, try the following:</span></span>
- <span data-ttu-id="19b4d-153">Confirmez que vos données sensibles ont été téléchargées correctement à l’aide des commandes expliquées dans les instructions de téléchargement de vos données sensibles à l’aide de [l’outil EDM](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span><span class="sxs-lookup"><span data-stu-id="19b4d-153">Confirm that your sensitive data was uploaded correctly using the commands explained in [the guidance for uploading your sensitive data using the EDM tool](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>
- <span data-ttu-id="19b4d-154">Vérifiez que les exemples que vous avez entrés dans l’élément sont présents dans votre table d’informations sensibles et que les délimiteur ignorés sont corrects.</span><span class="sxs-lookup"><span data-stu-id="19b4d-154">Check that the examples you entered in the item are present in your sensitive information table and that the ignored delimiters are correct.</span></span>
- <span data-ttu-id="19b4d-155">**Testez** la fonction SIT que vous avez utilisée lorsque vous avez configuré l’élément principal dans chacun de vos modèles.</span><span class="sxs-lookup"><span data-stu-id="19b4d-155">**Test** the SIT you used when you configured the primary element in each of your patterns.</span></span> <span data-ttu-id="19b4d-156">Cela permettra de confirmer que la sit est en mesure de correspondre aux exemples de l’élément.</span><span class="sxs-lookup"><span data-stu-id="19b4d-156">This will confirm that the SIT is able to match the examples in the item.</span></span> 
  -  <span data-ttu-id="19b4d-157">Si le sit que vous avez sélectionné pour un élément principal dans le type EDM ne trouve pas de correspondance dans l’élément ou trouve moins de correspondances que prévu, vérifiez qu’il prend en charge les séparateurs et les délimiteurs qui existent dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="19b4d-157">If the SIT you selected for a primary element in the EDM type doesn't find a match in the item or finds fewer matches than you expected, check that it supports separators and delimiters that exist in the content.</span></span> <span data-ttu-id="19b4d-158">N’oubliez pas d’inclure les délimiteur ignorés définis dans votre schéma.</span><span class="sxs-lookup"><span data-stu-id="19b4d-158">Be sure to include the ignored delimiters defined in your schema.</span></span> 
  -  <span data-ttu-id="19b4d-159">Si la **fonction Test** ne détecte aucun contenu, vérifiez si la fonction SIT que vous avez sélectionnée inclut des exigences pour des mots clés supplémentaires ou d’autres validations.</span><span class="sxs-lookup"><span data-stu-id="19b4d-159">If the **Test** function does not detect any content at all, check if the SIT you selected includes requirements for additional keywords or other validations.</span></span> <span data-ttu-id="19b4d-160">Pour les sits intégrées, voir définitions d’entité des types d’informations [sensibles](sensitive-information-type-entity-definitions.md) pour vérifier les conditions minimales requises pour la correspondance de chaque type.</span><span class="sxs-lookup"><span data-stu-id="19b4d-160">For the built-in SITs, see [Sensitive information types entity definitions](sensitive-information-type-entity-definitions.md) to verify what the minimum requirements are for matching each type.</span></span>
