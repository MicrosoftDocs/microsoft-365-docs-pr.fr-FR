---
title: Créer un extracteur
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: Découvrez comment créer un extracteur dans Microsoft SharePoint Syntex.
ms.openlocfilehash: d68cc8b8c337c1ae6740eb5775576a54279b8389
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321808"
---
# <a name="create-an-extractor-preview"></a><span data-ttu-id="6a46d-103">Créer un extracteur (aperçu)</span><span class="sxs-lookup"><span data-stu-id="6a46d-103">Create an extractor (Preview)</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL2G]

</br> 

<span data-ttu-id="6a46d-104">La création d’un modèle de classifieur sert à automatiser l’identification et la classification de types de documents spécifiques. Avant ou après cette opération, vous pouvez, si vous le souhaitez, ajouter des extracteurs à votre modèle pour extraire des informations spécifiques de ces documents.</span><span class="sxs-lookup"><span data-stu-id="6a46d-104">Before or after you create a classifier model to automate identification and classification of specific document types, you can optionally choose to add extractors to your model to pull out specific information from these documents.</span></span> <span data-ttu-id="6a46d-105">Par exemple, vous souhaiterez sans doute que votre modèle identifie tous les documents *Renouvellement de contrat* ajoutés à votre bibliothèque de documents. Vous souhaiterez sans doute, également, qu’il affiche la *date de démarrage du service* de chaque document sous la forme d’une valeur de colonne dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="6a46d-105">For example, you may want your model not only to identify all *Contract Renewal* documents added to your document library, but also to display the *Service Start date* for each document as a column value in the document library.</span></span>

<span data-ttu-id="6a46d-106">Vous devez créer un extracteur pour chaque entité dans le document à extraire.</span><span class="sxs-lookup"><span data-stu-id="6a46d-106">You need to create an extractor for each entity in the document that you want to extract.</span></span> <span data-ttu-id="6a46d-107">Dans notre exemple, nous devons extraire la  **date de démarrage du service**  de chaque \*\* document Renouvellement de contrat\*\*  identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="6a46d-107">In our example, we want to extract the **Service Start Date** for each **Contract Renewal** document that is identified by the model.</span></span> <span data-ttu-id="6a46d-108">Nous devons pouvoir consulter dans la bibliothèque de documents une vue de tous les documents  **Renouvellement de contrat** , avec une colonne qui affiche la date de **démarrage du service** de chaque document.</span><span class="sxs-lookup"><span data-stu-id="6a46d-108">We want to be able to see a view in the document library of all **Contract Renewal** documents, with a column that shows the **Service Start** date value of each document.</span></span> 

> [!NOTE]
> <span data-ttu-id="6a46d-109">Pour créer un extracteur, utilisez les fichiers déjà chargés pour entraîner le classifieur.</span><span class="sxs-lookup"><span data-stu-id="6a46d-109">In order to create an extractor, you use the same files you previously uploaded to train the classifier.</span></span> 

## <a name="name-your-extractor"></a><span data-ttu-id="6a46d-110">Nommer votre extracteur</span><span class="sxs-lookup"><span data-stu-id="6a46d-110">Name your extractor</span></span>

1. <span data-ttu-id="6a46d-111">Depuis la page d’accueil du modèle, dans la mosaïque **Créer et entraîner des extracteurs**, cliquez sur **Entraîner un extracteur**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-111">From the model home page, in the **Create and train extractors** tile, click **Train extractor**.</span></span>
2. <span data-ttu-id="6a46d-112">À l’écran **Nouvel extracteur d’entités**, tapez le nom de votre extracteur dans le champ **Nom du nouvel extracteur**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-112">On the **New entity extractor** screen, type the name of your extractor in the **New extractor name** field.</span></span> <span data-ttu-id="6a46d-113">Par exemple, nommez-le **Date de démarrage du service** si vous souhaitez extraire la date de démarrage du service à partir de chaque document Renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="6a46d-113">For example, name it **Service Start Date** if you want to extract the service start date from each Contract Renewal document.</span></span> <span data-ttu-id="6a46d-114">Vous pouvez également choisir de réutiliser une colonne précédemment créée (par exemple, une colonne de métadonnées gérées).</span><span class="sxs-lookup"><span data-stu-id="6a46d-114">You can also choose to reuse a previously created column (for example, a managed metadata column).</span></span>
3. <span data-ttu-id="6a46d-115">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-115">Click **Create**.</span></span>

## <a name="add-a-label"></a><span data-ttu-id="6a46d-116">Ajouter une étiquette</span><span class="sxs-lookup"><span data-stu-id="6a46d-116">Add a label</span></span>

<span data-ttu-id="6a46d-117">L’étape suivante consiste à étiqueter l’entité à extraire dans vos exemples de fichiers d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="6a46d-117">The next step is to label the entity you want to extract in your example training files.</span></span>

<span data-ttu-id="6a46d-118">La création de l’extracteur entraîne l’ouverture de la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="6a46d-118">Creating the extractor opens the extractor page.</span></span> <span data-ttu-id="6a46d-119">Cette page affiche la liste des fichiers échantillons, le premier fichier de la liste étant affiché dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="6a46d-119">Here you see a list of your sample files, with the first file on the list displayed in the viewer.</span></span>

1. <span data-ttu-id="6a46d-120">Dans la visionneuse, sélectionnez les données à extraire des fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a46d-120">From the viewer, select the data that you want to extract from the files.</span></span> <span data-ttu-id="6a46d-121">Par exemple, si vous souhaitez extraire la *date de démarrage du service*, mettez en évidence la valeur de date du premier fichier (*lundi 14 octobre 2019*).</span><span class="sxs-lookup"><span data-stu-id="6a46d-121">For example, if you want to extract the *Start Service Date*, you highlight the date value in the first file (*Monday, October 14, 2019*).</span></span> <span data-ttu-id="6a46d-122">Ensuite, cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-122">and then click **Save**.</span></span>  <span data-ttu-id="6a46d-123">Normalement, la valeur sera affichée dans la liste d’exemples étiquetés du fichier, sous la colonne **Étiquette**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-123">You should see the value display from the file in the Labeled examples list, under the **Label** column.</span></span>
2. <span data-ttu-id="6a46d-124">Sélectionnez **Fichier suivant** pour enregistrer automatiquement et ouvrir le fichier suivant dans la liste de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="6a46d-124">Select **Next file** to auto save and open the next file in the list in the viewer.</span></span> <span data-ttu-id="6a46d-125">Vous pouvez également sélectionner **Enregistrer**, puis sélectionner un autre fichier dans la liste **Exemples étiquetés**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-125">Or select **Save** and then select another file from the **Labeled examples** list.</span></span>
3. <span data-ttu-id="6a46d-126">Dans la visionneuse, répétez les étapes 1 et 2, puis répétez l’opération jusqu’à enregistrer l’étiquette dans les cinq fichiers.</span><span class="sxs-lookup"><span data-stu-id="6a46d-126">In the viewer, repeat steps 1 and 2, then repeat until you saved the label in all five files.</span></span>

    ![Paramètres avancés](../media/content-understanding/select-service-start-date.png) 

 
<span data-ttu-id="6a46d-128">Après l’étiquetage de cinq fichiers, une bannière de notification vous dit de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="6a46d-128">Once you labeled five files, a notification banner displays informing you to move to training.</span></span> <span data-ttu-id="6a46d-129">Vous pouvez choisir d’étiqueter d’autres documents ou de passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="6a46d-129">You can choose to more label more documents or advance to training.</span></span> 

## <a name="add-an-explanation"></a><span data-ttu-id="6a46d-130">Ajouter une explication</span><span class="sxs-lookup"><span data-stu-id="6a46d-130">Add an explanation</span></span>

<span data-ttu-id="6a46d-131">Dans notre exemple, nous allons créer une explication du format de l’entité proprement dit et des variations susceptibles d’apparaître dans les exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="6a46d-131">For our example, we are going to create an explanation that provides a hint about the entity format itself and variations it may have in the sample documents.</span></span> <span data-ttu-id="6a46d-132">Par exemple, une date peut être affichée dans plusieurs formats différents :</span><span class="sxs-lookup"><span data-stu-id="6a46d-132">For example, a date value can be in a number of different formats, such as:</span></span>
- <span data-ttu-id="6a46d-133">14/10/2019</span><span class="sxs-lookup"><span data-stu-id="6a46d-133">10/14/2019</span></span>
- <span data-ttu-id="6a46d-134">14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="6a46d-134">October 14, 2019</span></span>
- <span data-ttu-id="6a46d-135">Lundi 14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="6a46d-135">Monday, October 14, 2019</span></span>
 

<span data-ttu-id="6a46d-136">Pour identifier plus facilement la *date de démarrage du service*, vous pouvez créer une explication de modèle.</span><span class="sxs-lookup"><span data-stu-id="6a46d-136">To help identify the *Service Start Date* you can create a pattern explanation.</span></span>

1. <span data-ttu-id="6a46d-137">Dans la section Explication, sélectionnez **Nouveau**, puis tapez un nom (par exemple, *Date*).</span><span class="sxs-lookup"><span data-stu-id="6a46d-137">In the Explanation section, select **New** and type a name (for example, *Date*).</span></span>
2. <span data-ttu-id="6a46d-138">Type : sélectionnez **Liste de modèles**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-138">For Type, select **Pattern list**.</span></span>
3. <span data-ttu-id="6a46d-139">Valeur : indiquez la variation de la date telle qu’elle apparaît dans les fichiers échantillons.</span><span class="sxs-lookup"><span data-stu-id="6a46d-139">For Value, provide the date variation as they appear in the sample files.</span></span> <span data-ttu-id="6a46d-140">Par exemple, si certaines dates apparaissent au format 0/00/0000, vous devez entrer les variations qui apparaissent dans vos documents, par exemple :</span><span class="sxs-lookup"><span data-stu-id="6a46d-140">For example, if you have date formats that appear as 0/00/0000, you enter any variations that appear in your documents, such as:</span></span>
    - <span data-ttu-id="6a46d-141">0/0/0000</span><span class="sxs-lookup"><span data-stu-id="6a46d-141">0/0/0000</span></span>
    - <span data-ttu-id="6a46d-142">0/00/0000</span><span class="sxs-lookup"><span data-stu-id="6a46d-142">0/00/0000</span></span>
    - <span data-ttu-id="6a46d-143">00/0/0000</span><span class="sxs-lookup"><span data-stu-id="6a46d-143">00/0/0000</span></span>
    - <span data-ttu-id="6a46d-144">00/00/0000</span><span class="sxs-lookup"><span data-stu-id="6a46d-144">00/00/0000</span></span>
4. <span data-ttu-id="6a46d-145">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-145">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="6a46d-146">Si vous souhaitez en savoir plus sur les types d’explications, veuillez consulter la rubrique [Types d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview).</span><span class="sxs-lookup"><span data-stu-id="6a46d-146">For more learn more about explanation types, see [Explanation types](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview).</span></span>  


### <a name="use-the-explanation-library"></a><span data-ttu-id="6a46d-147">Utiliser la bibliothèque d’explications</span><span class="sxs-lookup"><span data-stu-id="6a46d-147">Use the Explanation library</span></span>

<span data-ttu-id="6a46d-148">Pour créer des explications d’éléments tels que des dates, il est plus facile d’[utiliser la bibliothèque d’explications](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-the-explanation-library) que d’entrer manuellement toutes les variations.</span><span class="sxs-lookup"><span data-stu-id="6a46d-148">For creating explanations for items such as dates, it is easier to [use the explanation library](https://docs.microsoft.com/microsoft-365/contentunderstanding/explanation-types-overview#use-the-explanation-library) than to manually enter all variations.</span></span> <span data-ttu-id="6a46d-149">La bibliothèque d’explications est un ensemble d’explications de modèles et d’expressions prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="6a46d-149">The explanation library is a set of pre-built phrase and pattern explanations.</span></span> <span data-ttu-id="6a46d-150">La bibliothèque tente d’offrir tous les formats de listes de modèles ou d’expressions courantes, comme des dates, des numéros de téléphone, des codes postaux, etc.</span><span class="sxs-lookup"><span data-stu-id="6a46d-150">The library tries to provides all formats for common phrase or pattern lists, such as dates, phone numbers, zip codes, and many others.</span></span> 

<span data-ttu-id="6a46d-151">Pour l’échantillon *Date de début du service*, nous vous recommandons d’utiliser l’explication prédéfinie de la *date* dans la bibliothèque d’explications :</span><span class="sxs-lookup"><span data-stu-id="6a46d-151">For the *Service Start Date* sample, it is more efficient to use the pre-built explanation for *Date* in the explanation library:</span></span>

1. <span data-ttu-id="6a46d-152">Dans la section **Explication**, sélectionnez **Nouveau**, puis **Depuis la bibliothèque d’explications**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-152">In the **Explanation section**, select **New**, and then select **From explanation library**.</span></span>
2. <span data-ttu-id="6a46d-153">Depuis la bibliothèque d’explications, sélectionnez **Date**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-153">From the explanation library, select **Date**.</span></span> <span data-ttu-id="6a46d-154">Vous pouvez afficher toutes les variations de date reconnues.</span><span class="sxs-lookup"><span data-stu-id="6a46d-154">You can view all variations of date that are recognized.</span></span>
3. <span data-ttu-id="6a46d-155">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-155">Select **Add**.</span></span></br>

    ![Bibliothèque d’explications](../media/content-understanding/explanation-library.png) 

4. <span data-ttu-id="6a46d-157">À la page **Créer une explication**, les champs sont automatiquement remplis avec la *date*.</span><span class="sxs-lookup"><span data-stu-id="6a46d-157">On the **Create an explanation** page, the *Date* information from the explanation library auto fills the fields.</span></span> <span data-ttu-id="6a46d-158">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-158">Select **Save**.</span></span></br>

    ![Date](../media/content-understanding/date-explanation-library.png) 

## <a name="train-the-model"></a><span data-ttu-id="6a46d-160">Entraîner le modèle</span><span class="sxs-lookup"><span data-stu-id="6a46d-160">Train the model</span></span> 

<span data-ttu-id="6a46d-161">L’enregistrement de vos explications démarre l’entraînement.</span><span class="sxs-lookup"><span data-stu-id="6a46d-161">Saving your explanation start the training.</span></span> <span data-ttu-id="6a46d-162">Si votre modèle dispose d’informations suffisantes pour extraire les données de vos exemples de fichiers étiquetés, chacun d’entre eux comportera l’étiquette **Correspondance**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-162">If your model has enough information to extract the data from your labeled example files, you will see each file labeled with **Match**.</span></span>  

![Correspondance](../media/content-understanding/match2.png) 

<span data-ttu-id="6a46d-164">Si l’explication ne dispose pas d’informations suffisante pour rechercher les données à extraire, chaque fichier est labellisé comportera l’étiquette **Incompatibilité**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-164">If the explanation does not have enough information to find the data you want to extract, each file will be labeled with **Mismatch**.</span></span> <span data-ttu-id="6a46d-165">Si vous souhaitez en savoir plus sur l’incompatibilité en question, veuillez cliquer sur les fichiers **incompatibles**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-165">You can click on the **Mismatched** files to see more information about why there was a mismatch.</span></span>


## <a name="add-another-explanation"></a><span data-ttu-id="6a46d-166">Ajouter une autre explication</span><span class="sxs-lookup"><span data-stu-id="6a46d-166">Add another explanation</span></span>

<span data-ttu-id="6a46d-167">L’incompatibilité indique souvent que l’explication fournie ne comportait pas d’informations suffisantes pour extraire la valeur de la date de démarrage du service afin de faire correspondre les fichiers étiquetés.</span><span class="sxs-lookup"><span data-stu-id="6a46d-167">Often the mismatch is an indication that the explanation we provided did not provide enough information to extract the service start date value to match our labeled files.</span></span> <span data-ttu-id="6a46d-168">Vous devrez sans doute la modifier ou ajouter une autre explication.</span><span class="sxs-lookup"><span data-stu-id="6a46d-168">You may need to edit it, or add another explanation.</span></span>

<span data-ttu-id="6a46d-169">Dans notre exemple, vous remarquerez que la chaîne de texte *Date de démarrage du service du* précède toujours la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="6a46d-169">For our example, notice that the text string *Start Service date of* always precedes the actual value.</span></span> <span data-ttu-id="6a46d-170">Pour identifier plus facilement la date de démarrage du service, vous devez créer une explication d’expression.</span><span class="sxs-lookup"><span data-stu-id="6a46d-170">To help identify the Service Start Date, you need to create a phrase explanation.</span></span>

1. <span data-ttu-id="6a46d-171">Dans la section Explication, sélectionnez **Nouveau**, puis tapez un nom (par exemple, *Chaîne de préfixe*).</span><span class="sxs-lookup"><span data-stu-id="6a46d-171">In the Explanation section, select **New**, and then type a name (for example, *Prefix String*).</span></span>
2. <span data-ttu-id="6a46d-172">Type : sélectionnez **Liste d’expressions**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-172">For the Type, select **Phrase list**.</span></span>
3. <span data-ttu-id="6a46d-173">Utilisez la valeur *Date de démarrage du service du*.</span><span class="sxs-lookup"><span data-stu-id="6a46d-173">Use *Service Start Date of* as the value.</span></span>
4. <span data-ttu-id="6a46d-174">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-174">Select **Save**.</span></span>

    ![Chaîne de préfixe](../media/content-understanding/prefix-string.png) 

## <a name="train-the-model-again"></a><span data-ttu-id="6a46d-176">Entraîner de nouveau le modèle</span><span class="sxs-lookup"><span data-stu-id="6a46d-176">Train the model again</span></span>

<span data-ttu-id="6a46d-177">L’enregistrement de l’explication génère le redémarrage de l’entraînement, cette fois à l’aide des explications de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6a46d-177">Saving the explanation starts the training again, this time using both explanations in the example.</span></span> <span data-ttu-id="6a46d-178">Si votre modèle dispose d’informations suffisantes pour extraire les données des exemples de fichiers étiquetés, chacun d’entre eux comportera l’étiquette **Correspondance**.</span><span class="sxs-lookup"><span data-stu-id="6a46d-178">If your model has enough information to extract the data from the labeled example files, you see each file labeled with **Match**.</span></span> 

<span data-ttu-id="6a46d-179">Si vous recevez de nouveau une **incompatibilité** sur vos fichiers étiquetés, vous devrez probablement créer une autre explication. Le modèle aura sans doute besoin d’informations supplémentaires sur le type de document. Sinon, vous devrez probablement envisager de modifier vos fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="6a46d-179">If you again receive a **Mismatch** on your labeled files, you likely need to create another explanation to provide the model more information to identify the document type, or consider making changes to your existing ones.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="6a46d-180">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="6a46d-180">Test your model</span></span>

<span data-ttu-id="6a46d-181">Si vous recevez une correspondance sur vos fichiers échantillons étiquetés, vous pouvez à présent tester votre modèle sur les autres exemples de fichiers non étiquetés.</span><span class="sxs-lookup"><span data-stu-id="6a46d-181">If you receive a match on your labeled sample files, you can now test your model on the remaining unlabeled example files.</span></span> <span data-ttu-id="6a46d-182">Cette étape permet d’évaluer la « pertinence » ou le degré de préparation du modèle avant utilisation, en le testant sur des fichiers pour l’instant inconnus de lui.</span><span class="sxs-lookup"><span data-stu-id="6a46d-182">This is a useful step to evaluate the “fitness” or readiness of the model before using it, by testing it on files the model hasn’t seen before.</span></span>

1. <span data-ttu-id="6a46d-183">Dans la page d’accueil du modèle, cliquez sur l’onglet **Test**. Le modèle est alors exécuté sur vos fichiers échantillons non étiquetés.</span><span class="sxs-lookup"><span data-stu-id="6a46d-183">From the model home page, click the **Test** tab.  This runs the model on your unlabeled sample files.</span></span>
2. <span data-ttu-id="6a46d-184">Dans la liste **Fichiers de test**, vos exemples de fichiers affichés indiquent si le modèle peut extraire les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6a46d-184">In the **Test files** list, your example files display to show if the model is able to extract the information you need.</span></span> <span data-ttu-id="6a46d-185">Utilisez ces informations pour déterminer plus facilement l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="6a46d-185">Use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Test de vos fichiers](../media/content-understanding/test-filies-extractor.png) 
