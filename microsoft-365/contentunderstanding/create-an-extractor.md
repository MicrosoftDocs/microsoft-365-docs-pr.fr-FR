---
title: Créer un extracteur
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
description: Découvrez comment créer un extracteur dans Microsoft SharePoint Syntex.
ms.openlocfilehash: dd26b049f71688804cd5110a5a0bb7c87950be94
ms.sourcegitcommit: d354727303d9574991b5a0fd298d2c9414e19f6c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/02/2021
ms.locfileid: "50080485"
---
# <a name="create-an-extractor-in-microsoft-sharepoint-syntex"></a><span data-ttu-id="81025-103">Créer un extracteur dans Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="81025-103">Create an extractor in Microsoft SharePoint Syntex</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL2G]

</br> 

<span data-ttu-id="81025-104">La création d’un modèle de classifieur sert à automatiser l’identification et la classification de types de documents spécifiques. Avant ou après cette opération, vous pouvez, si vous le souhaitez, ajouter des extracteurs à votre modèle pour extraire des informations spécifiques de ces documents.</span><span class="sxs-lookup"><span data-stu-id="81025-104">Before or after you create a classifier model to automate identification and classification of specific document types, you can optionally choose to add extractors to your model to pull out specific information from these documents.</span></span> <span data-ttu-id="81025-105">Par exemple, vous souhaiterez sans doute que votre modèle identifie tous les documents *Renouvellement de contrat* ajoutés à votre bibliothèque de documents. Vous souhaiterez sans doute, également, qu’il affiche la *date de démarrage du service* de chaque document sous la forme d’une valeur de colonne dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="81025-105">For example, you may want your model not only to identify all *Contract Renewal* documents added to your document library, but also to display the *Service Start date* for each document as a column value in the document library.</span></span>

<span data-ttu-id="81025-106">Vous devez créer un extracteur pour chaque entité dans le document à extraire.</span><span class="sxs-lookup"><span data-stu-id="81025-106">You need to create an extractor for each entity in the document that you want to extract.</span></span> <span data-ttu-id="81025-107">Dans notre exemple, nous devons extraire la  **date de démarrage du service**  de chaque \*\* document Renouvellement de contrat\*\*  identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="81025-107">In our example, we want to extract the **Service Start Date** for each **Contract Renewal** document that is identified by the model.</span></span> <span data-ttu-id="81025-108">Nous devons pouvoir consulter dans la bibliothèque de documents une vue de tous les documents  **Renouvellement de contrat** , avec une colonne qui affiche la date de **démarrage du service** de chaque document.</span><span class="sxs-lookup"><span data-stu-id="81025-108">We want to be able to see a view in the document library of all  **Contract Renewal** documents, with a column that shows the **Service Start** date value of each document.</span></span> 

> [!NOTE]
> <span data-ttu-id="81025-109">Pour créer un extracteur, utilisez les fichiers déjà chargés pour entraîner le classifieur.</span><span class="sxs-lookup"><span data-stu-id="81025-109">In order to create an extractor, you use the same files you previously uploaded to train the classifier.</span></span> 

## <a name="name-your-extractor"></a><span data-ttu-id="81025-110">Nommer votre extracteur</span><span class="sxs-lookup"><span data-stu-id="81025-110">Name your extractor</span></span>

1. <span data-ttu-id="81025-111">Depuis la page d’accueil du modèle, dans la mosaïque **Créer et entraîner des extracteurs**, cliquez sur **Entraîner un extracteur**.</span><span class="sxs-lookup"><span data-stu-id="81025-111">From the model home page, in the **Create and train extractors** tile, click **Train extractor**.</span></span>
2. <span data-ttu-id="81025-112">À l’écran **Nouvel extracteur d’entités**, tapez le nom de votre extracteur dans le champ **Nom du nouvel extracteur**.</span><span class="sxs-lookup"><span data-stu-id="81025-112">On the **New entity extractor** screen, type the name of your extractor in the **New extractor name** field.</span></span> <span data-ttu-id="81025-113">Par exemple, nommez-le **Date de démarrage du service** si vous souhaitez extraire la date de démarrage du service à partir de chaque document Renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="81025-113">For example, name it **Service Start Date** if you want to extract the service start date from each Contract Renewal document.</span></span> <span data-ttu-id="81025-114">Vous pouvez également choisir de réutiliser une colonne précédemment créée (par exemple, une colonne de métadonnées gérées).</span><span class="sxs-lookup"><span data-stu-id="81025-114">You can also choose to reuse a previously created column (for example, a managed metadata column).</span></span>
> [!NOTE]
> <span data-ttu-id="81025-115">Si vous créez un nouvel extracteur, sélectionnez **Nouveau type de colonne**, puis sélectionnez **Une seule ligne de texte**, la limite de caractères maximale est 255.</span><span class="sxs-lookup"><span data-stu-id="81025-115">If you create a new extractor, then select **New column type** and choose **Single line of text**, the maximum character limit is 255.</span></span> <span data-ttu-id="81025-116">Les caractères que vous tapez au-delà de la limite sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="81025-116">Any characters that you type exceeding the limit get truncated.</span></span> 
3. <span data-ttu-id="81025-117">Une fois que vous avez terminé, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="81025-117">When you're done, click **Create**.</span></span>

## <a name="add-a-label"></a><span data-ttu-id="81025-118">Ajouter une étiquette</span><span class="sxs-lookup"><span data-stu-id="81025-118">Add a label</span></span>

<span data-ttu-id="81025-119">L’étape suivante consiste à étiqueter l’entité à extraire dans vos exemples de fichiers d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="81025-119">The next step is to label the entity you want to extract in your example training files.</span></span>

<span data-ttu-id="81025-120">La création de l’extracteur entraîne l’ouverture de la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="81025-120">Creating the extractor opens the extractor page.</span></span> <span data-ttu-id="81025-121">Cette page affiche la liste des fichiers échantillons, le premier fichier de la liste étant affiché dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="81025-121">Here you see a list of your sample files, with the first file on the list displayed in the viewer.</span></span>

1. <span data-ttu-id="81025-122">Dans la visionneuse, sélectionnez les données à extraire des fichiers.</span><span class="sxs-lookup"><span data-stu-id="81025-122">From the viewer, select the data that you want to extract from the files.</span></span> <span data-ttu-id="81025-123">Par exemple, si vous souhaitez extraire la *date de démarrage du service*, mettez en évidence la valeur de date du premier fichier (*lundi 14 octobre 2019*).</span><span class="sxs-lookup"><span data-stu-id="81025-123">For example, if you want to extract the *Start Service Date*, you highlight the date value in the first file (*Monday, October 14, 2019*).</span></span> <span data-ttu-id="81025-124">Ensuite, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="81025-124">and then click **Save**.</span></span>  <span data-ttu-id="81025-125">Normalement, la valeur sera affichée dans la liste d’exemples étiquetés du fichier, sous la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="81025-125">You should see the value display from the file in the Labeled examples list, under the **Label** column.</span></span>
2. <span data-ttu-id="81025-126">Sélectionnez **Fichier suivant** pour enregistrer automatiquement et ouvrir le fichier suivant dans la liste de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="81025-126">Select **Next file** to auto save and open the next file in the list in the viewer.</span></span> <span data-ttu-id="81025-127">Vous pouvez également sélectionner **Enregistrer**, puis sélectionner un autre fichier dans la liste **Exemples étiquetés**.</span><span class="sxs-lookup"><span data-stu-id="81025-127">Or select **Save** and then select another file from the **Labeled examples** list.</span></span>
3. <span data-ttu-id="81025-128">Dans la visionneuse, répétez les étapes 1 et 2, puis répétez l’opération jusqu’à enregistrer l’étiquette dans les cinq fichiers.</span><span class="sxs-lookup"><span data-stu-id="81025-128">In the viewer, repeat steps 1 and 2, then repeat until you saved the label in all five files.</span></span>

    ![Paramètres avancés](../media/content-understanding/select-service-start-date.png) 

 
<span data-ttu-id="81025-130">Après l’étiquetage de cinq fichiers, une bannière de notification vous dit de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="81025-130">Once you labeled five files, a notification banner displays informing you to move to training.</span></span> <span data-ttu-id="81025-131">Vous pouvez choisir d’étiqueter d’autres documents ou de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="81025-131">You can choose to more label more documents or advance to training.</span></span> 

### <a name="use-find-to-search-your-file"></a><span data-ttu-id="81025-132">Utiliser la recherche pour effectuer une recherche dans votre fichier</span><span class="sxs-lookup"><span data-stu-id="81025-132">Use Find to search your file</span></span>
<span data-ttu-id="81025-133">Vous pouvez utiliser la fonctionnalité <b>Rechercher</b> pour rechercher une entité dans votre document que vous voulez étiqueter.</span><span class="sxs-lookup"><span data-stu-id="81025-133">You can use the <b>Find</b> feature to search for an entity in your document that you want to label.</span></span>

   ![Rechercher dans le fichier](../media/content-understanding/find-feature.png) 

<span data-ttu-id="81025-135">La fonctionnalité Rechercher est utile si vous recherchez un document de grande taille ou si le document contient plusieurs instances de l’entité.</span><span class="sxs-lookup"><span data-stu-id="81025-135">The Find feature is useful if you are searching a large document or if there are multiple instances of the entity in the document.</span></span> <span data-ttu-id="81025-136">Si vous trouvez plusieurs instances, vous pouvez sélectionner celle dont vous avez besoin dans les résultats de recherche pour y aller dans la visionneuse afin de l’étiqueter.</span><span class="sxs-lookup"><span data-stu-id="81025-136">If you find multiple instances, you can select the one you need in the search results to go to that location in the viewer to label it.</span></span>


## <a name="add-an-explanation"></a><span data-ttu-id="81025-137">Ajouter une explication</span><span class="sxs-lookup"><span data-stu-id="81025-137">Add an explanation</span></span>

<span data-ttu-id="81025-138">Dans notre exemple, nous allons créer une explication du format de l’entité proprement dit et des variations susceptibles d’apparaître dans les exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="81025-138">For our example, we are going to create an explanation that provides a hint about the entity format itself and variations it may have in the sample documents.</span></span> <span data-ttu-id="81025-139">Par exemple, une date peut être affichée dans plusieurs formats différents :</span><span class="sxs-lookup"><span data-stu-id="81025-139">For example, a date value can be in a number of different formats, such as:</span></span>
- <span data-ttu-id="81025-140">14/10/2019</span><span class="sxs-lookup"><span data-stu-id="81025-140">10/14/2019</span></span>
- <span data-ttu-id="81025-141">14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="81025-141">October 14, 2019</span></span>
- <span data-ttu-id="81025-142">Lundi 14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="81025-142">Monday, October 14, 2019</span></span>
 

<span data-ttu-id="81025-143">Pour identifier plus facilement la *date de démarrage du service*, vous pouvez créer une explication de modèle.</span><span class="sxs-lookup"><span data-stu-id="81025-143">To help identify the *Service Start Date* you can create a pattern explanation.</span></span>

1. <span data-ttu-id="81025-144">Dans la section Explication, sélectionnez **Nouveau**, puis tapez un nom (par exemple, *Date*).</span><span class="sxs-lookup"><span data-stu-id="81025-144">In the Explanation section, select **New** and type a name (for example, *Date*).</span></span>
2. <span data-ttu-id="81025-145">Type : sélectionnez **Liste de modèles**.</span><span class="sxs-lookup"><span data-stu-id="81025-145">For Type, select **Pattern list**.</span></span>
3. <span data-ttu-id="81025-146">Valeur : indiquez la variation de la date telle qu’elle apparaît dans les fichiers échantillons.</span><span class="sxs-lookup"><span data-stu-id="81025-146">For Value, provide the date variation as they appear in the sample files.</span></span> <span data-ttu-id="81025-147">Par exemple, si certaines dates apparaissent au format 0/00/0000, vous devez entrer les variations qui apparaissent dans vos documents, par exemple :</span><span class="sxs-lookup"><span data-stu-id="81025-147">For example, if you have date formats that appear as 0/00/0000, you enter any variations that appear in your documents, such as:</span></span>
    - <span data-ttu-id="81025-148">0/0/0000</span><span class="sxs-lookup"><span data-stu-id="81025-148">0/0/0000</span></span>
    - <span data-ttu-id="81025-149">0/00/0000</span><span class="sxs-lookup"><span data-stu-id="81025-149">0/00/0000</span></span>
    - <span data-ttu-id="81025-150">00/0/0000</span><span class="sxs-lookup"><span data-stu-id="81025-150">00/0/0000</span></span>
    - <span data-ttu-id="81025-151">00/00/0000</span><span class="sxs-lookup"><span data-stu-id="81025-151">00/00/0000</span></span>
4. <span data-ttu-id="81025-152">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="81025-152">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="81025-153">Si vous souhaitez en savoir plus sur les types d’explications, veuillez consulter la rubrique [Types d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview).</span><span class="sxs-lookup"><span data-stu-id="81025-153">For more learn more about explanation types, see [Explanation types](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview).</span></span>  


### <a name="use-the-explanation-library"></a><span data-ttu-id="81025-154">Utiliser la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="81025-154">Use the Explanation library</span></span>

<span data-ttu-id="81025-155">Pour créer des explications d’éléments tels que des dates, il est plus facile d’[utiliser la bibliothèque d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-the-explanation-library) que d’entrer manuellement toutes les variations.</span><span class="sxs-lookup"><span data-stu-id="81025-155">For creating explanations for items such as dates, it is easier to [use the explanation library](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-the-explanation-library) than to manually enter all variations.</span></span> <span data-ttu-id="81025-156">La bibliothèque d’explications est un ensemble d’explications de modèles et d’expressions prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="81025-156">The explanation library is a set of pre-built phrase and pattern explanations.</span></span> <span data-ttu-id="81025-157">La bibliothèque tente d’offrir tous les formats de listes de modèles ou d’expressions courantes, comme des dates, des numéros de téléphone, des codes postaux, etc.</span><span class="sxs-lookup"><span data-stu-id="81025-157">The library tries to provides all formats for common phrase or pattern lists, such as dates, phone numbers, zip codes, and many others.</span></span> 

<span data-ttu-id="81025-158">Pour l’échantillon *Date de début du service*, nous vous recommandons d’utiliser l’explication prédéfinie de la *date* dans la bibliothèque d’explications :</span><span class="sxs-lookup"><span data-stu-id="81025-158">For the *Service Start Date* sample, it is more efficient to use the pre-built explanation for *Date* in the explanation library:</span></span>

1. <span data-ttu-id="81025-159">Dans la section **Explication**, sélectionnez **Nouveau**, puis **Depuis la bibliothèque d’explications**.</span><span class="sxs-lookup"><span data-stu-id="81025-159">In the **Explanation section**, select **New**, and then select **From explanation library**.</span></span>
2. <span data-ttu-id="81025-160">Depuis la bibliothèque d’explications, sélectionnez **Date**.</span><span class="sxs-lookup"><span data-stu-id="81025-160">From the explanation library, select **Date**.</span></span> <span data-ttu-id="81025-161">Vous pouvez afficher toutes les variations de date reconnues.</span><span class="sxs-lookup"><span data-stu-id="81025-161">You can view all variations of date that are recognized.</span></span>
3. <span data-ttu-id="81025-162">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="81025-162">Select **Add**.</span></span></br>

    ![Bibliothèque d’explications](../media/content-understanding/explanation-library.png) 

4. <span data-ttu-id="81025-164">À la page **Créer une explication**, les champs sont automatiquement remplis avec la *date*.</span><span class="sxs-lookup"><span data-stu-id="81025-164">On the **Create an explanation** page, the *Date* information from the explanation library auto fills the fields.</span></span> <span data-ttu-id="81025-165">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="81025-165">Select **Save**.</span></span></br>

    ![Date](../media/content-understanding/date-explanation-library.png) 

## <a name="train-the-model"></a><span data-ttu-id="81025-167">Entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="81025-167">Train the model</span></span> 

<span data-ttu-id="81025-168">L’enregistrement de vos explications démarre l’entraînement.</span><span class="sxs-lookup"><span data-stu-id="81025-168">Saving your explanation start the training.</span></span> <span data-ttu-id="81025-169">Si votre modèle dispose d’informations suffisantes pour extraire les données de vos exemples de fichiers étiquetés, chacun d’entre eux comportera l’étiquette **Correspondance**.</span><span class="sxs-lookup"><span data-stu-id="81025-169">If your model has enough information to extract the data from your labeled example files, you will see each file labeled with **Match**.</span></span>  

![Correspondance](../media/content-understanding/match2.png) 

<span data-ttu-id="81025-171">Si l’explication ne dispose pas d’informations suffisante pour rechercher les données à extraire, chaque fichier est labellisé comportera l’étiquette **Incompatibilité**.</span><span class="sxs-lookup"><span data-stu-id="81025-171">If the explanation does not have enough information to find the data you want to extract, each file will be labeled with **Mismatch**.</span></span> <span data-ttu-id="81025-172">Si vous souhaitez en savoir plus sur l’incompatibilité en question, veuillez cliquer sur les fichiers **incompatibles**.</span><span class="sxs-lookup"><span data-stu-id="81025-172">You can click on the **Mismatched** files to see more information about why there was a mismatch.</span></span>


## <a name="add-another-explanation"></a><span data-ttu-id="81025-173">Ajouter une autre explication</span><span class="sxs-lookup"><span data-stu-id="81025-173">Add another explanation</span></span>

<span data-ttu-id="81025-174">L’incompatibilité indique souvent que l’explication fournie ne comportait pas d’informations suffisantes pour extraire la valeur de la date de démarrage du service afin de faire correspondre les fichiers étiquetés.</span><span class="sxs-lookup"><span data-stu-id="81025-174">Often the mismatch is an indication that the explanation we provided did not provide enough information to extract the service start date value to match our labeled files.</span></span> <span data-ttu-id="81025-175">Vous devrez sans doute la modifier ou ajouter une autre explication.</span><span class="sxs-lookup"><span data-stu-id="81025-175">You may need to edit it, or add another explanation.</span></span>

<span data-ttu-id="81025-176">Dans notre exemple, vous remarquerez que la chaîne de texte *Date de démarrage du service du* précède toujours la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="81025-176">For our example, notice that the text string *Start Service date of* always precedes the actual value.</span></span> <span data-ttu-id="81025-177">Pour identifier plus facilement la date de démarrage du service, vous devez créer une explication d’expression.</span><span class="sxs-lookup"><span data-stu-id="81025-177">To help identify the Service Start Date, you need to create a phrase explanation.</span></span>

1. <span data-ttu-id="81025-178">Dans la section Explication, sélectionnez **Nouveau**, puis tapez un nom (par exemple, *Chaîne de préfixe*).</span><span class="sxs-lookup"><span data-stu-id="81025-178">In the Explanation section, select **New**, and then type a name (for example, *Prefix String*).</span></span>
2. <span data-ttu-id="81025-179">Type : sélectionnez **Liste d’expressions**.</span><span class="sxs-lookup"><span data-stu-id="81025-179">For the Type, select **Phrase list**.</span></span>
3. <span data-ttu-id="81025-180">Utilisez la valeur *Date de démarrage du service du*.</span><span class="sxs-lookup"><span data-stu-id="81025-180">Use *Service Start Date of* as the value.</span></span>
4. <span data-ttu-id="81025-181">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="81025-181">Select **Save**.</span></span>

    ![Chaîne de préfixe](../media/content-understanding/prefix-string.png) 

## <a name="train-the-model-again"></a><span data-ttu-id="81025-183">Entraîner de nouveau le modèle</span><span class="sxs-lookup"><span data-stu-id="81025-183">Train the model again</span></span>

<span data-ttu-id="81025-184">L’enregistrement de l’explication génère le redémarrage de l’entraînement, cette fois à l’aide des explications de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="81025-184">Saving the explanation starts the training again, this time using both explanations in the example.</span></span> <span data-ttu-id="81025-185">Si votre modèle dispose d’informations suffisantes pour extraire les données des exemples de fichiers étiquetés, chacun d’entre eux comportera l’étiquette **Correspondance**.</span><span class="sxs-lookup"><span data-stu-id="81025-185">If your model has enough information to extract the data from the labeled example files, you see each file labeled with **Match**.</span></span> 

<span data-ttu-id="81025-186">Si vous recevez de nouveau une **incompatibilité** sur vos fichiers étiquetés, vous devrez probablement créer une autre explication. Le modèle aura sans doute besoin d’informations supplémentaires sur le type de document. Sinon, vous devrez probablement envisager de modifier vos fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="81025-186">If you again receive a **Mismatch** on your labeled files, you likely need to create another explanation to provide the model more information to identify the document type, or consider making changes to your existing ones.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="81025-187">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="81025-187">Test your model</span></span>

<span data-ttu-id="81025-188">Si vous recevez une correspondance sur vos fichiers échantillons étiquetés, vous pouvez à présent tester votre modèle sur les autres exemples de fichiers non étiquetés.</span><span class="sxs-lookup"><span data-stu-id="81025-188">If you receive a match on your labeled sample files, you can now test your model on the remaining unlabeled example files.</span></span> <span data-ttu-id="81025-189">Cette étape est facultative mais utile, car elle permet d’évaluer la « pertinence » ou le degré de préparation du modèle avant utilisation, en le testant sur des fichiers pour l’instant inconnus de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="81025-189">This is optional, but a useful step to evaluate the “fitness” or readiness of the model before using it, by testing it on files the model hasn’t seen before.</span></span>

1. <span data-ttu-id="81025-190">Dans la page d’accueil du modèle, cliquez sur l’onglet **Test**. Le modèle s’exécute alors sur vos fichiers échantillons non étiquetés.</span><span class="sxs-lookup"><span data-stu-id="81025-190">From the model home page, click the **Test** tab.  This runs the model on your unlabeled sample files.</span></span>
2. <span data-ttu-id="81025-191">Dans la liste **Fichiers de test**, vos exemples de fichiers affichés indiquent si le modèle peut extraire les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="81025-191">In the **Test files** list, your example files display to show if the model is able to extract the information you need.</span></span> <span data-ttu-id="81025-192">Utilisez ces informations pour déterminer plus facilement l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="81025-192">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Test de vos fichiers](../media/content-understanding/test-filies-extractor.png) 

## <a name="see-also"></a><span data-ttu-id="81025-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81025-194">See Also</span></span>
[<span data-ttu-id="81025-195">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="81025-195">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="81025-196">Types d’explications</span><span class="sxs-lookup"><span data-stu-id="81025-196">Explanation types</span></span>](explanation-types-overview.md)

[<span data-ttu-id="81025-197">Utiliser la taxonomie du magasin de termes lors de la création d’un extracteur</span><span class="sxs-lookup"><span data-stu-id="81025-197">Leverage term store taxonomy when creating an extractor</span></span>](leverage-term-store-taxonomy.md)

[<span data-ttu-id="81025-198">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="81025-198">Document Understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="81025-199">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="81025-199">Apply a model</span></span>](apply-a-model.md) 
