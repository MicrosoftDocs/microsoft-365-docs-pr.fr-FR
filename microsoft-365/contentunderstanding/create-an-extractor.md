---
title: Créer un extracteur
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment créer un extracteur dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 740df6769b3a1675e4e1691f84d164312b15567c
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295455"
---
# <a name="create-an-extractor-preview"></a><span data-ttu-id="cf7b3-103">Créer un extracteur (aperçu)</span><span class="sxs-lookup"><span data-stu-id="cf7b3-103">Create an extractor (Preview)</span></span>

<span data-ttu-id="cf7b3-104">Le contenu de cet article est destiné à la préversion privée du projet cortex.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-104">The content in this article is for the Project Cortex Private Preview.</span></span> <span data-ttu-id="cf7b3-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="cf7b3-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL2G]

</br> 

<span data-ttu-id="cf7b3-106">Avant ou après avoir créé un modèle de classifieur pour automatiser l’identification et la classification de types de documents spécifiques, vous pouvez choisir d’ajouter des extracteurs à votre modèle pour extraire des informations spécifiques de ces documents.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-106">Before or after you create a classifier model to automate identification and classification of specific document types, you can optionally choose to add extractors to your model to pull out specific information from these documents.</span></span> <span data-ttu-id="cf7b3-107">Par exemple, vous souhaiterez peut-être que votre modèle identifie tous les documents de *renouvellement de contrats* ajoutés à votre bibliothèque de documents, mais également d’afficher la date de *début du service* pour chaque document sous forme de colonne dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-107">For example, you may want your model not only to identify all *Contract Renewal* documents added to your document library, but also to display the *Service Start date* for each document as a column in the document library.</span></span>

<span data-ttu-id="cf7b3-108">Vous devez créer un extracteur pour chaque entité dans le document que vous souhaitez extraire.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-108">You need to create an extractor for each entity in the document that you want to extract.</span></span> <span data-ttu-id="cf7b3-109">Dans l’exemple, vous souhaitez extraire la *Date de début du service* pour chaque document de renouvellement de *contrat* identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-109">In the sample, you want to extract the *Service Start Date* for each *Contract Renewal* document that is identified by the model.</span></span> <span data-ttu-id="cf7b3-110">Cela doit se produire lorsque vous souhaitez afficher une vue dans la bibliothèque de documents de tous les documents de *renouvellement de contrat* avec une colonne indiquant la valeur de date de début du service pour chaque document.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-110">This must happen when you want to see a view in the document library of all the *Contract Renewal* documents with a column showing the Service Start date value for each document.</span></span>

> [!NOTE]
> <span data-ttu-id="cf7b3-111">Avant de créer un extracteur, vous devez [ajouter vos exemples de fichiers](https://docs.microsoft.com/microsoft-365/contentunderstanding/create-a-classifier#add-your-example-files) pour former le modèle afin d’identifier les informations que vous souhaitez extraire.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-111">Before creating an extractor, you need to [add your example files](https://docs.microsoft.com/microsoft-365/contentunderstanding/create-a-classifier#add-your-example-files) to help train the model to identify the information you want to extract.</span></span> <span data-ttu-id="cf7b3-112">Utilisez les mêmes exemples de fichiers que ceux utilisés pour créer votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-112">Use the same sample files you used to create your classifier.</span></span>

## <a name="name-your-extractor"></a><span data-ttu-id="cf7b3-113">Nommer votre extracteur</span><span class="sxs-lookup"><span data-stu-id="cf7b3-113">Name your extractor</span></span>

1. <span data-ttu-id="cf7b3-114">À partir de la page d’accueil du modèle, dans la vignette **créer et former** des **extracteurs**, cliquez sur extracteur de train.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-114">From the model home page, in the **Create and train extractors** tile, click **Train extractor**.</span></span>
2. <span data-ttu-id="cf7b3-115">Sur l’écran **nouvel extracteur d’entités** , tapez le nom de votre extracteur dans le nouveau champ nom de l' **extracteur** .</span><span class="sxs-lookup"><span data-stu-id="cf7b3-115">On the **New entity extractor** screen, type the name of your extractor in the **New extractor name** field.</span></span> <span data-ttu-id="cf7b3-116">Par exemple, nommez la **Date de début du service** si vous souhaitez extraire la date de début du service de chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-116">For example, name it **Service Start Date** if you want to extract the service start date from each Contract Renewal document.</span></span>
3. <span data-ttu-id="cf7b3-117">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-117">Click **Create**.</span></span>

## <a name="add-a-label"></a><span data-ttu-id="cf7b3-118">Ajouter une étiquette</span><span class="sxs-lookup"><span data-stu-id="cf7b3-118">Add a label</span></span>

<span data-ttu-id="cf7b3-119">L’étape suivante consiste à étiqueter les informations que vous souhaitez extraire dans vos exemples de fichiers de formation.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-119">The next step is to label the information you want to extract in your sample training files.</span></span>

<span data-ttu-id="cf7b3-120">La création de l’extracteur ouvre la page extracteur.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-120">Creating the extractor opens the extractor page.</span></span> <span data-ttu-id="cf7b3-121">Cette section affiche la liste de vos fichiers d’exemple, avec le premier fichier de la liste affichée dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-121">Here you see a list of your sample files, with the first file on the list displayed in the viewer.</span></span>

1. <span data-ttu-id="cf7b3-122">À partir de la visionneuse, sélectionnez les données que vous souhaitez extraire des fichiers.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-122">From the viewer, select the data that you want to extract from the files.</span></span> <span data-ttu-id="cf7b3-123">Par exemple, si vous souhaitez extraire la *date du service de démarrage*, sélectionnez la valeur date dans le premier fichier (*lundi 14 octobre 2019*).</span><span class="sxs-lookup"><span data-stu-id="cf7b3-123">For example, if you want to extract the *Start Service Date*, you highlight the date value in the first file (*Monday, October 14, 2019*).</span></span> <span data-ttu-id="cf7b3-124">puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-124">and then click **Save**.</span></span>  <span data-ttu-id="cf7b3-125">La valeur s’affiche à partir du fichier dans la liste des exemples étiquetés, sous la colonne **étiquette** .</span><span class="sxs-lookup"><span data-stu-id="cf7b3-125">You should see the value display from the file in the Labeled examples list, under the **Label** column.</span></span>
2. <span data-ttu-id="cf7b3-126">Sélectionnez **fichier suivant** pour l’enregistrement automatique et ouvrez le fichier suivant dans la liste de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-126">Select **Next file** to auto save and open the next file in the list in the viewer.</span></span> <span data-ttu-id="cf7b3-127">Ou sélectionnez **Enregistrer** , puis un autre fichier dans la liste d' **exemples étiquetés** .</span><span class="sxs-lookup"><span data-stu-id="cf7b3-127">Or select **Save** and then select another file from the **Labeled examples** list.</span></span>
3. <span data-ttu-id="cf7b3-128">Dans la visionneuse, répétez les étapes 1 et 2, puis répétez l’opération jusqu’à ce que vous enregistriez l’étiquette dans les cinq fichiers.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-128">In the viewer, repeat steps 1 and 2, then repeat until you saved the label in all five files.</span></span>

    ![Paramètres avancés](../media/content-understanding/select-service-start-date.png) 

### <a name="add-a-negative-example"></a><span data-ttu-id="cf7b3-130">Ajouter un exemple négatif</span><span class="sxs-lookup"><span data-stu-id="cf7b3-130">Add a negative example</span></span>

<span data-ttu-id="cf7b3-131">De la même manière que vous ajoutez un fichier d’exemple négatif lors de la création d’un classifieur, vous devez ajouter un échantillon négatif pour l’extracteur.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-131">Similar to how you add a negative sample file when creating a classifier, you need to add a negative sample for the extractor.</span></span> <span data-ttu-id="cf7b3-132">Il doit s’agir d’un fichier qui ne contient pas la valeur de date « start of service ».</span><span class="sxs-lookup"><span data-stu-id="cf7b3-132">It should be a file that does not contain a "Service Start" date value.</span></span>

1. <span data-ttu-id="cf7b3-133">Dans la liste des **exemples étiquetés** , sélectionnez un exemple négatif.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-133">From the **Labeled examples** list, select a negative example.</span></span>
2. <span data-ttu-id="cf7b3-134">Dans la visionneuse en haut de l’article, sélectionnez **aucune étiquette présente**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-134">In the viewer on the top of the article, select **No label present**.</span></span>
3. <span data-ttu-id="cf7b3-135">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-135">Click **Save**.</span></span>
 
<span data-ttu-id="cf7b3-136">Une fois que vous avez étiqueté cinq fichiers, une bannière de notification s’affiche pour vous informer de la formation.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-136">Once you labeled five files, a notification banner displays informing you to move to training.</span></span> <span data-ttu-id="cf7b3-137">Vous pouvez choisir un plus grand nombre de documents ou passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-137">You can choose to more documents or advance to training.</span></span> 

## <a name="add-an-explanation"></a><span data-ttu-id="cf7b3-138">Ajouter une explication</span><span class="sxs-lookup"><span data-stu-id="cf7b3-138">Add an explanation</span></span>

<span data-ttu-id="cf7b3-139">Pour l’exemple, vous créez une explication qui fournit une indication sur le format d’entité lui-même et les variantes qu’il peut avoir dans les exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-139">For the example, you create an explanation that provides a hint about the entity format itself and variations it may have in the sample documents.</span></span> <span data-ttu-id="cf7b3-140">Par exemple, une valeur de date peut être dans différents formats, par exemple :</span><span class="sxs-lookup"><span data-stu-id="cf7b3-140">For example, a date value can be in a number of different formats, such as:</span></span>
- <span data-ttu-id="cf7b3-141">10/14/2019</span><span class="sxs-lookup"><span data-stu-id="cf7b3-141">10/14/2019</span></span>
- <span data-ttu-id="cf7b3-142">14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="cf7b3-142">October 14, 2019</span></span>
- <span data-ttu-id="cf7b3-143">Lundi 14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="cf7b3-143">Monday, October 14, 2019</span></span>
 

<span data-ttu-id="cf7b3-144">Pour vous aider à identifier la *Date de début du service* , vous devez créer une explication de modèle.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-144">To help identify the *Service Start Date* you create a pattern explanation.</span></span>

1. <span data-ttu-id="cf7b3-145">Dans la section explication, sélectionnez **nouveau** , puis tapez un nom (par exemple, *Date*).</span><span class="sxs-lookup"><span data-stu-id="cf7b3-145">In the Explanation section, select **New** and type a name (for example, *Date*).</span></span>
2. <span data-ttu-id="cf7b3-146">Pour type, sélectionnez **liste de motifs**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-146">For Type, select **Pattern list**.</span></span>
3. <span data-ttu-id="cf7b3-147">Pour valeur, indiquez la variation de date telle qu’elle apparaît dans les fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-147">For Value, provide the date variation as they appear in the sample files.</span></span> <span data-ttu-id="cf7b3-148">Par exemple, si des formats de date s’affichent sous la forme 0/00/0000, vous entrez les variations qui apparaissent dans vos documents, telles que :</span><span class="sxs-lookup"><span data-stu-id="cf7b3-148">For example, if you have date formats that appear as 0/00/0000, you enter any variations that appear in your documents, such as:</span></span>
    - <span data-ttu-id="cf7b3-149">0/0/0000</span><span class="sxs-lookup"><span data-stu-id="cf7b3-149">0/0/0000</span></span>
    - <span data-ttu-id="cf7b3-150">0/00/0000</span><span class="sxs-lookup"><span data-stu-id="cf7b3-150">0/00/0000</span></span>
    - <span data-ttu-id="cf7b3-151">00/0/0000</span><span class="sxs-lookup"><span data-stu-id="cf7b3-151">00/0/0000</span></span>
    - <span data-ttu-id="cf7b3-152">00/00/0000</span><span class="sxs-lookup"><span data-stu-id="cf7b3-152">00/00/0000</span></span>
4. <span data-ttu-id="cf7b3-153">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-153">Select **Save**.</span></span>

### <a name="use-the-explanation-library"></a><span data-ttu-id="cf7b3-154">Utiliser la bibliothèque d’explication</span><span class="sxs-lookup"><span data-stu-id="cf7b3-154">Use the Explanation library</span></span>

<span data-ttu-id="cf7b3-155">Pour créer des explications pour des éléments tels que des dates, il est plus facile d’utiliser la bibliothèque d’explications que d’entrer manuellement toutes les variantes.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-155">For creating explanations for items such as dates, it is easier to use the explanation library than to manually enter all variations.</span></span> <span data-ttu-id="cf7b3-156">La bibliothèque d’explications est un ensemble d’explications prégénérées d’expressions et de modèles.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-156">The explanation library is a set of pre-built phrase and pattern explanations.</span></span> <span data-ttu-id="cf7b3-157">La bibliothèque fournit tous les formats pour les listes d’expressions ou de modèles courantes, telles que les dates, les numéros de téléphone, le code postal, etc.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-157">The library provides all formats for common phrase or pattern lists, such as dates, phone numbers, zip code, etc.</span></span> 

<span data-ttu-id="cf7b3-158">Pour l’exemple de *Date de démarrage du service* , il est plus efficace d’utiliser l’explication prédéfinie pour la *Date* dans la bibliothèque d’explication :</span><span class="sxs-lookup"><span data-stu-id="cf7b3-158">For the *Service Start Date* sample, it is more efficient to use the pre-built explanation for *Date* in the explanation library:</span></span>

1. <span data-ttu-id="cf7b3-159">Dans la **section Explication**, sélectionnez **nouveau**, puis sélectionnez **à partir de la bibliothèque d’explication**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-159">In the **Explanation section**, select **New**, and then select **From explanation library**.</span></span>
2. <span data-ttu-id="cf7b3-160">Dans la bibliothèque d’explication, sélectionnez **Date**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-160">From the explanation library, select **Date**.</span></span> <span data-ttu-id="cf7b3-161">Vous pouvez afficher toutes les variantes de date reconnues.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-161">You can view all variations of date that are recognized.</span></span>
3. <span data-ttu-id="cf7b3-162">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-162">Select **Add**.</span></span></br>

    ![Bibliothèque d’explications](../media/content-understanding/explanation-library.png) 

4. <span data-ttu-id="cf7b3-164">Sur la page **créer une explication** , les informations de *Date* de la bibliothèque d’explication remplissent automatiquement les champs.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-164">On the **Create an explanation** page, the *Date* information from the explanation library auto fills the fields.</span></span> <span data-ttu-id="cf7b3-165">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-165">Select **Save**.</span></span></br>

    ![Date](../media/content-understanding/date-explanation-library.png) 

## <a name="train-the-model"></a><span data-ttu-id="cf7b3-167">Former le modèle</span><span class="sxs-lookup"><span data-stu-id="cf7b3-167">Train the model</span></span> 

<span data-ttu-id="cf7b3-168">Enregistrement de votre explication démarrez la formation.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-168">Saving your explanation start the training.</span></span> <span data-ttu-id="cf7b3-169">Si votre modèle dispose de suffisamment d’informations pour extraire les données de vos fichiers d’exemple étiquetés, vous verrez chaque fichier étiqueté avec **match**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-169">If your model has enough information to extract the data from your labeled example files, you will see each file labeled with **Match**.</span></span>  

![Match](../media/content-understanding/match2.png) 

<span data-ttu-id="cf7b3-171">Si l’explication ne contient pas suffisamment d’informations pour rechercher les données que vous souhaitez extraire, chaque fichier sera étiqueté sans **correspondance**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-171">If the explanation does not have enough information to find the data you want to extract, each file will be labeled with **Mismatch**.</span></span> <span data-ttu-id="cf7b3-172">Vous pouvez cliquer sur les fichiers qui ne **correspondent** pas pour obtenir plus d’informations sur les raisons d’une incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-172">You can click on the **Mismatched** files to see more information about why there was a mismatch.</span></span>


## <a name="add-another-explanation"></a><span data-ttu-id="cf7b3-173">Ajouter une autre explication</span><span class="sxs-lookup"><span data-stu-id="cf7b3-173">Add another explanation</span></span>

<span data-ttu-id="cf7b3-174">En règle générale, l’incompatibilité est une indication que l’explication que nous avons fournie n’a pas fourni suffisamment d’informations pour extraire la valeur de la date de début du service pour qu’elle corresponde à nos fichiers étiquetés.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-174">Often the mismatch is an indication that the explanation we provided did not provide enough information to extract the service start date value to match our labeled files.</span></span> <span data-ttu-id="cf7b3-175">Vous devrez peut-être le modifier ou ajouter une autre explication.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-175">You may need to edit it, or add another explanation.</span></span>

<span data-ttu-id="cf7b3-176">Pour l’exemple, Notez que la *Date de début de* la chaîne de texte de Always précède la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-176">For the sample, notice that the text string *Start Service date of* always precedes the actual value.</span></span> <span data-ttu-id="cf7b3-177">Pour vous aider à identifier la date de début du service, vous devez créer une explication de l’expression.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-177">To help identify the Service Start Date, you need ot create a phrase explanation.</span></span>

1. <span data-ttu-id="cf7b3-178">Dans la section explication, sélectionnez **nouveau**, puis tapez un nom (par exemple, *chaîne de préfixe*).</span><span class="sxs-lookup"><span data-stu-id="cf7b3-178">In the Explanation section, select **New**, and then type a name (for example, *Prefix String*).</span></span>
2. <span data-ttu-id="cf7b3-179">Pour le type, sélectionnez **liste des expressions**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-179">For the Type, select **Phrase list**.</span></span>
3. <span data-ttu-id="cf7b3-180">Utiliser la *Date de début du service* comme valeur.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-180">Use *Service Start Date of* as the value.</span></span>
4. <span data-ttu-id="cf7b3-181">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-181">Select **Save**.</span></span>

    ![Chaîne de préfixe](../media/content-understanding/prefix-string.png) 

## <a name="train-the-model-again"></a><span data-ttu-id="cf7b3-183">Former de nouveau le modèle</span><span class="sxs-lookup"><span data-stu-id="cf7b3-183">Train the model again</span></span>

<span data-ttu-id="cf7b3-184">En enregistrant l’explication, vous redémarrez la formation, cette fois en utilisant les explications de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-184">Saving the explanation starts the training again, this time using both explanations in the sample.</span></span> <span data-ttu-id="cf7b3-185">Si votre modèle dispose de suffisamment d’informations pour extraire les données des exemples de fichiers étiquetés, vous voyez chaque fichier étiqueté avec **match**.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-185">If your model has enough information to extract the data from the labeled sample files, you see each file labeled with **Match**.</span></span> 

<span data-ttu-id="cf7b3-186">Si vous recevez une nouvelle fois une **incompatibilité** avec vos fichiers étiquetés, vous devez probablement créer une autre explication pour fournir au modèle plus d’informations afin d’identifier le type de document ou envisager d’apporter des modifications à votre modèle.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-186">If you again receive a **Mismatch** on your labeled files, you likely need to create another explanation to provide the model more information to identify the document type, or consider making changes to your sample model.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="cf7b3-187">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="cf7b3-187">Test your model</span></span>

<span data-ttu-id="cf7b3-188">Si vous recevez une correspondance sur vos fichiers d’exemple étiquetés, vous pouvez maintenant tester votre modèle sur les fichiers d’exemple non labellisés restants.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-188">If you receive a match on your labeled sample files, you can now test your model on the remaining unlabeled sample files.</span></span>

1. <span data-ttu-id="cf7b3-189">À partir de la page d’accueil du modèle, cliquez sur l’onglet **test** .  Cela exécute le modèle sur vos fichiers d’exemple non labellisés.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-189">From the model home page, click the **Test** tab.  This runs the model on your unlabeled sample files.</span></span>
2. <span data-ttu-id="cf7b3-190">Dans la liste des **fichiers test** , vos exemples de fichiers affichent pour indiquer si le modèle peut extraire les informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-190">In the **Test files** list, your example files display to show if the model is able to extract the information you need.</span></span> <span data-ttu-id="cf7b3-191">Utilisez ces informations pour vous aider à déterminer l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="cf7b3-191">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Tester vos fichiers](../media/content-understanding/test-filies-extractor.png) 
