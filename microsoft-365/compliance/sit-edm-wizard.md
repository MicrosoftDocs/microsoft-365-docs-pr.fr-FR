---
title: Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 2081de887e09794350222dac3527bb3ff932837a
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49699148"
---
# <a name="use-the-exact-data-match-schema-and-sensitive-information-type-wizard"></a><span data-ttu-id="fc8ef-103">Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="fc8ef-103">Use the Exact Data Match Schema and Sensitive Information Type Wizard</span></span>

<span data-ttu-id="fc8ef-104">La [Création d’un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md) implique de nombreuses étapes.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-104">[Creating a custom sensitive information type with Exact Data Match (EDM) based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)  involves many steps.</span></span>  <span data-ttu-id="fc8ef-105">Vous pouvez utiliser cet Assistant pour créer votre schéma et votre modèle de type d’informations sensibles (package de règles) en vue de simplifier le processus.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-105">You can use this wizard to create your schema and sensitive information type pattern (rule package) files to help simplify the process.</span></span>

> [!NOTE]
> <span data-ttu-id="fc8ef-106">L’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles est disponible uniquement pour les nuages mondiaux et GCC.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-106">The Exact Data Match Schema and Sensitive Information Type Wizard is only available for the World Wide and GCC clouds only.</span></span>

<span data-ttu-id="fc8ef-107">Cet Assistant peut être utilisé à la place des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc8ef-107">This wizard can be used instead of the:</span></span>

- [<span data-ttu-id="fc8ef-108">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="fc8ef-108">Define the schema for your database of sensitive information</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#define-the-schema-for-your-database-of-sensitive-information)
- [<span data-ttu-id="fc8ef-109">Configurer un modèle (package de règles)</span><span class="sxs-lookup"><span data-stu-id="fc8ef-109">Set up a pattern (rule package)</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#set-up-a-rule-package)

<span data-ttu-id="fc8ef-110">dans [Partie 1 : configurer la classification EDM](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-1-set-up-edm-based-classification).</span><span class="sxs-lookup"><span data-stu-id="fc8ef-110">steps in [Part 1: Set up EDM-based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-1-set-up-edm-based-classification).</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="fc8ef-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="fc8ef-111">Pre-requisites</span></span>

1. <span data-ttu-id="fc8ef-112">Familiarisez-vous avec les étapes de création d’un type d’informations sensibles personnalisées avec le [flux de travail EDM en un clin d’œil](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#the-work-flow-at-a-glance).</span><span class="sxs-lookup"><span data-stu-id="fc8ef-112">Familiarize yourself with the steps to create a custom sensitive information type with EDM [work flow at a glance](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#the-work-flow-at-a-glance).</span></span>

2. <span data-ttu-id="fc8ef-113">Suivez les étapes décrites dans la section [Enregistrer des données sensibles au format. csv](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#save-sensitive-data-in-csv-format).</span><span class="sxs-lookup"><span data-stu-id="fc8ef-113">Perform the steps in the [Save sensitive data in .csv format](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#save-sensitive-data-in-csv-format) section.</span></span>

## <a name="use-the-exact-data-match-schema-and-sensitive-information-type-pattern-wizard"></a><span data-ttu-id="fc8ef-114">Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="fc8ef-114">Use the exact data match schema and sensitive information type pattern wizard</span></span>

1. <span data-ttu-id="fc8ef-115">Dans le Centre de conformité Microsoft 365 pour votre client, accédez à **Classification des données** > **Correspondances exactes des données**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-115">In the Microsoft 365 Compliance center for your tenant go to **Data classification** > **Exact data matches**.</span></span>

2. <span data-ttu-id="fc8ef-116">Choisissez **Créer un schéma EDM** pour ouvrir le menu volant de configuration de l’Assistant de schéma.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-116">Choose **Create EDM schema** to open the schema wizard configuration flyout.</span></span>

![Menu volant de configuration de l’Assistant de création de schéma EDM](../media/edm-schema-wizard-1.png)

3. <span data-ttu-id="fc8ef-118">Indiquez un nom **approprié** et **Description**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-118">Fill in an appropriate **Name** and **Description**.</span></span>

4. <span data-ttu-id="fc8ef-119">Choisissez **Ignorer les séparateurs et ponctuations pour tous les champs du schéma** si vous souhaitez ce comportement.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-119">Choose **Ignore delimiters and punctuations for all schema fields** if you want that behavior.</span></span> <span data-ttu-id="fc8ef-120">Pour en savoir plus sur la configuration d’EDM afin d’ignorer la casse ou les séparateurs, voir [Création d’un type d’informations sensibles personnalisé avec une classification de correspondance exacte de données (EDM)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ef-120">To learn more about configuring EDM to ignore case or delimitere, see [Creating a custom sensitive information type with Exact Data Match (EDM) based classification](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).</span></span>

5. <span data-ttu-id="fc8ef-121">Renseignez les valeurs souhaitées pour votre **Champ de schéma n° 1** et ajoutez des champs si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-121">Fill in your desired values for your **Schema field #1** and add more fields as needed.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="fc8ef-122">Au moins un champ, mais pas plus de cinq, doivent être désignés comme pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-122">At least one, but no more than five of your schema fields must be designated as searchable.</span></span>

6. <span data-ttu-id="fc8ef-123">Cliquez sur Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-123">Choose save.</span></span> <span data-ttu-id="fc8ef-124">Votre schéma figure désormais dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-124">Your schema will now be listed.</span></span>

7. <span data-ttu-id="fc8ef-125">Choisissez **Types d’informations sensibles EDM** et **Créer un type d’informations sensibles EDM** pour ouvrir l’Assistant de configuration des types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-125">Choose **EDM sensitive info types** and **Create EDM sensitive info type** to open the sensitive info type configuration wizard.</span></span>

8. <span data-ttu-id="fc8ef-126">Choisissez **Choisir un schéma EDM existant** puis sélectionnez le schéma que vous avez créé dans les étapes 2-6 dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-126">Choose **Choose an existing EDM schema** and choose the schema you created in steps 2-6 from the list.</span></span>

9. <span data-ttu-id="fc8ef-127">Choisissez **Suivant**, puis **Créer un modèle**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-127">Choose **Next** and choose **Create pattern**.</span></span>

10. <span data-ttu-id="fc8ef-128">Choisissez le **Niveau de confiance** et l’**Élément principal**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-128">Choose the **Confidence level** and **Primary element**.</span></span>  <span data-ttu-id="fc8ef-129">Pour en savoir plus sur la configuration d’un modèle, voir [Créer un type d’informations sensibles personnalisé dans le Centre de conformité](create-a-custom-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="fc8ef-129">To learn more about configuring a pattern, see [Create a custom sensitive information type in the Compliance Center](create-a-custom-sensitive-information-type.md)</span></span>

11.  <span data-ttu-id="fc8ef-130">Choisissez le **Type d’informations sensibles de l’élément principal** à associer.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-130">Choose the **Primary element's sensitive info type** to associate it with.</span></span> <span data-ttu-id="fc8ef-131">Voir [Définitions des entités de types d’informations sensibles](sensitive-information-type-entity-definitions.md) pour en savoir plus sur les types d’informations sensibles disponibles.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-131">See [Sensitive Information Type Entity Definitions](sensitive-information-type-entity-definitions.md) to learn more about the available sensitive information types.</span></span>

12. <span data-ttu-id="fc8ef-132">Choisissez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-132">Choose **Done**.</span></span>

13. <span data-ttu-id="fc8ef-133">Choisissez vos **Niveau de confiance et proximité des caractères** souhaités.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-133">Choose your desired **Confidence level and character proximity**.</span></span>  <span data-ttu-id="fc8ef-134">Il s’agit de la valeur par défaut pour l’ensemble du type d’informations sensibles EDM.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-134">This will be the default value for the whole EDM sensitive info type</span></span>

13. <span data-ttu-id="fc8ef-135">Choisissez **Créer un modèle** si vous voulez créer des modèles supplémentaires pour votre type d’informations sensibles EDM.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-135">Choose **Create pattern** if you want to creaet additional patterns for your EDM sensitive info type.</span></span>

14. <span data-ttu-id="fc8ef-136">Choisissez **Suivant**, puis entrez un **Nom** et une **Description pour les administrateurs**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-136">Choose **Next** and fill in a **Name** and **Description for admins**.</span></span>

15. <span data-ttu-id="fc8ef-137">Passez en revue vos paramètres, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-137">Review and choose **Submit**.</span></span>

<span data-ttu-id="fc8ef-138">Vous pouvez supprimer ou modifier le modèle de type d’informations sensibles en le sélectionnant. Cela permet d’afficher les contrôles de modification et de suppression.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-138">You can delete or edit the sensitive information type pattern by selecting it which surfaces the edit and delete controls.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc8ef-139">Si vous voulez supprimer un schéma et que celui-ci est déjà associé à un type d’informations sensibles EDM, vous devez commencer par supprimer le type d’informations sensibles EDM. Vous pouvez ensuite supprimer le schéma.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-139">If you want to remove a schema, and it is already associated with an EDM sensitive info type, you must first delete the EDM sensitive info type, then you can delete the schema.</span></span>

## <a name="post-steps"></a><span data-ttu-id="fc8ef-140">Étapes ultérieures</span><span class="sxs-lookup"><span data-stu-id="fc8ef-140">Post steps</span></span>

<span data-ttu-id="fc8ef-141">Une fois que vous avez utilisé cet Assistant pour créer vos fichiers de schéma et modèle EDM (package de règles), vous devez continuer à effectuer les étapes décrites dans [Partie 2 : hacher et charger les données sensibles](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-2-hash-and-upload-the-sensitive-data) avant de pouvoir utiliser le type d’informations sensibles personnalisé EDM.</span><span class="sxs-lookup"><span data-stu-id="fc8ef-141">After you have used this wizard to create your EDM schema and pattern (rule package) files, you still have to perform the steps in [Part 2: Hash and upload the sensitive data](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md#part-2-hash-and-upload-the-sensitive-data) before you can use the EDM custom sensitive information type.</span></span>