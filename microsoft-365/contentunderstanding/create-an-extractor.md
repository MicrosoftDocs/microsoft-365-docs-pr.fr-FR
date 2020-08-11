---
title: Créer un extracteur (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment créer un extracteur
ms.openlocfilehash: 64dede9f6613da82c65ca12c6c335a25301f5b9e
ms.sourcegitcommit: a3a5dc541b0c971608cc86ef480509c25a13ca60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "46612761"
---
# <a name="create-an-extractor-preview"></a><span data-ttu-id="2f465-103">Créer un extracteur (aperçu)</span><span class="sxs-lookup"><span data-stu-id="2f465-103">Create an extractor (Preview)</span></span>
> [!Note] 
> <span data-ttu-id="2f465-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="2f465-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="2f465-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="2f465-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CL2G]

</br> 

<span data-ttu-id="2f465-106">Avant ou après avoir créé un modèle de classifieur pour automatiser l’identification et la classification de types de documents spécifiques, vous pouvez choisir d’ajouter des extracteurs à votre modèle pour extraire des informations spécifiques de ces documents.</span><span class="sxs-lookup"><span data-stu-id="2f465-106">Either before or after you create a classifier model to automate identification and classification of specific document types, you can optionally choose to add extractors to your model to pull out specific information from these documents.</span></span> <span data-ttu-id="2f465-107">Par exemple, vous souhaiterez peut-être que votre modèle identifie tous les documents de *renouvellement de contrats* ajoutés à votre bibliothèque de documents, mais aussi afficher la date de *début du service* pour chaque document sous forme de colonne dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="2f465-107">For example, you may want your model not only to identify all *Contract Renewal* documents that are added to your document library, but to also display the *Service Start date* for each document as a column in the document library.</span></span>

<span data-ttu-id="2f465-108">Vous devez créer un extracteur pour chaque entité dans le document que vous souhaitez extraire.</span><span class="sxs-lookup"><span data-stu-id="2f465-108">You need to create an extractor for each entity in the document that you want to extract.</span></span> <span data-ttu-id="2f465-109">Dans notre exemple, nous souhaitons extraire la *Date de début du service* pour chaque document de renouvellement de *contrat* identifié par le modèle.</span><span class="sxs-lookup"><span data-stu-id="2f465-109">In our example, we want to extract the *Service Start Date* for each *Contract Renewal* document that is identified by the model.</span></span> <span data-ttu-id="2f465-110">Nous souhaitons être en mesure d’afficher une vue dans la bibliothèque de documents de tous les documents de *renouvellement de contrat* , avec une colonne qui indique la valeur de date de début du service de chaque document.</span><span class="sxs-lookup"><span data-stu-id="2f465-110">We want to be able to see a view in the document library of all *Contract Renewal* documents, with a column that shows the Service Start date value of each document.</span></span>

> [!Note]
> <span data-ttu-id="2f465-111">Avant de créer un extracteur, vous devez [ajouter vos exemples de fichiers](https://docs.microsoft.com/microsoft-365/contentunderstanding/create-a-classifier?view=o365-worldwide#add-your-example-files) dont vous aurez besoin pour former le modèle afin d’identifier les informations que vous souhaitez extraire.</span><span class="sxs-lookup"><span data-stu-id="2f465-111">Before creating an extractor, you need to [add your example files](https://docs.microsoft.com/microsoft-365/contentunderstanding/create-a-classifier?view=o365-worldwide#add-your-example-files) you will need to help train the model to identify the information you want to extract.</span></span> <span data-ttu-id="2f465-112">Utilisez les mêmes exemples de fichiers que ceux utilisés pour créer votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="2f465-112">Use the same example files you used to create your classifier.</span></span>


## <a name="name-your-extractor"></a><span data-ttu-id="2f465-113">Nommer votre extracteur</span><span class="sxs-lookup"><span data-stu-id="2f465-113">Name your extractor</span></span>

1. <span data-ttu-id="2f465-114">Sur la page d’accueil du modèle, dans la vignette **créer et former** des **extracteurs**, cliquez sur extracteur de train.</span><span class="sxs-lookup"><span data-stu-id="2f465-114">On the model home page, in the **Create and train extractors** tile, click **Train extractor**.</span></span>
2. <span data-ttu-id="2f465-115">Sur l’écran **nouvel extracteur d’entités** , tapez le nom de votre extracteur dans le nouveau champ nom de l' **extracteur** .</span><span class="sxs-lookup"><span data-stu-id="2f465-115">On the **New entity extractor** screen, type the name of your extractor in the **New extractor name** field.</span></span> <span data-ttu-id="2f465-116">Par exemple, nous pouvons nommer **Date de début du service** si nous voulons extraire la date de début du service de chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="2f465-116">For example, we can name it **Service Start Date** if we want to extract the service start date from each Contract Renewal document.</span></span>
3. <span data-ttu-id="2f465-117">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-117">Click **Create**.</span></span>

## <a name="add-a-label"></a><span data-ttu-id="2f465-118">Ajouter une étiquette</span><span class="sxs-lookup"><span data-stu-id="2f465-118">Add a label</span></span>

<span data-ttu-id="2f465-119">L’étape suivante consiste à étiqueter les informations que vous souhaitez extraire dans vos exemples de fichiers de formation.</span><span class="sxs-lookup"><span data-stu-id="2f465-119">The next step is to label the information you want to extract in your example training files.</span></span>

<span data-ttu-id="2f465-120">La création de l’extracteur ouvre la page extracteur dans laquelle vous verrez une liste de vos exemples de fichiers, avec le premier fichier de la liste affichée dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="2f465-120">Creating the extractor will open the extractor page in which you will see a list of your example files, with the first file on the list displayed in the viewer.</span></span>

1. <span data-ttu-id="2f465-121">Dans la visionneuse, sélectionnez les données que vous souhaitez extraire des fichiers.</span><span class="sxs-lookup"><span data-stu-id="2f465-121">In the viewer, select the data that you want to extract from the files.</span></span> <span data-ttu-id="2f465-122">Par exemple, si vous souhaitez extraire la *date du service de démarrage*, vous devez mettre en surbrillance la valeur de date correspondant au premier fichier (*lundi 14 octobre 2019*).</span><span class="sxs-lookup"><span data-stu-id="2f465-122">For example, if you want to extract the *Start Service Date*, you will highlight the date value for it in the first file (*Monday, October 14, 2019*).</span></span> <span data-ttu-id="2f465-123">Puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-123">Then click **Save**.</span></span>  <span data-ttu-id="2f465-124">Vous verrez l’affichage de la valeur du fichier dans la liste d’exemples étiquetée sous la colonne **étiquette** .</span><span class="sxs-lookup"><span data-stu-id="2f465-124">You will see the value display for the file in the Labeled examples list under the **Label** column.</span></span>
2. <span data-ttu-id="2f465-125">Sélectionnez **fichier suivant** pour l’enregistrement automatique et ouvrez le fichier suivant dans la liste de la visionneuse, ou sélectionnez **Enregistrer** et sélectionnez un autre fichier dans la liste **exemples étiquetés** .</span><span class="sxs-lookup"><span data-stu-id="2f465-125">Select **Next file** to autosave and open the next file in the list in the viewer, or you can select **Save** and select another file from the **Labeled examples** list.</span></span>
3. <span data-ttu-id="2f465-126">Dans la visionneuse, répétez les étapes 1 et 2, puis faites-le jusqu’à ce que vous ayez enregistré l’étiquette dans cinq fichiers.</span><span class="sxs-lookup"><span data-stu-id="2f465-126">In the viewer, repeat steps 1 and 2, and do this until you have saved the label in five files.</span></span>

    ![Paramètres avancés](../media/content-understanding/select-service-start-date.png) 


### <a name="add-a-negative-example"></a><span data-ttu-id="2f465-128">Ajouter un exemple négatif</span><span class="sxs-lookup"><span data-stu-id="2f465-128">Add a negative example</span></span>

<span data-ttu-id="2f465-129">De la même manière que vous ajoutez un fichier d’exemple négatif lors de la création d’un classifieur, vous devez ajouter un exemple négatif pour l’extracteur.</span><span class="sxs-lookup"><span data-stu-id="2f465-129">Similar to how you would add a negative example file when creating a classifier, you need to add a negative example for the extractor.</span></span> <span data-ttu-id="2f465-130">Pour notre exemple, il doit s’agir d’un fichier qui ne contient pas de valeur de date de début de service.</span><span class="sxs-lookup"><span data-stu-id="2f465-130">For our example, it should be a file that does not contain a Service Start Date value.</span></span>

1. <span data-ttu-id="2f465-131">Dans la liste des **exemples étiquetés** , sélectionnez un exemple négatif.</span><span class="sxs-lookup"><span data-stu-id="2f465-131">From the **Labeled examples** list, select a negative example.</span></span>
2. <span data-ttu-id="2f465-132">Dans la visionneuse, en haut de l’article, sélectionnez **aucune étiquette présente**.</span><span class="sxs-lookup"><span data-stu-id="2f465-132">In the viewer, on the top of the article, select **No label present**.</span></span>
3. <span data-ttu-id="2f465-133">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-133">Click **Save**.</span></span>
 
<span data-ttu-id="2f465-134">Une fois que vous avez étiqueté cinq fichiers, une bannière de notification s’affiche pour vous informer sur la formation.</span><span class="sxs-lookup"><span data-stu-id="2f465-134">Once you have labeled five files, a notification banner will display informing you to move to training.</span></span> <span data-ttu-id="2f465-135">Vous pouvez choisir un plus grand nombre de documents ou passer à la formation.</span><span class="sxs-lookup"><span data-stu-id="2f465-135">You can choose to more documents or advance to training.</span></span> 

## <a name="add-an-explanation"></a><span data-ttu-id="2f465-136">Ajouter une explication</span><span class="sxs-lookup"><span data-stu-id="2f465-136">Add an explanation</span></span>

<span data-ttu-id="2f465-137">Pour notre exemple, nous allons créer une explication qui fournit une indication sur le format d’entité lui-même et les variantes qu’il peut contenir dans les exemples de documents.</span><span class="sxs-lookup"><span data-stu-id="2f465-137">For our example, we are going to create an explanation that provides a hint about the entity format itself and variations it may have in the example documents.</span></span> <span data-ttu-id="2f465-138">Par exemple, une valeur de date peut être dans différents formats, par exemple :</span><span class="sxs-lookup"><span data-stu-id="2f465-138">For example,a date value can be in a number of different formats, such as:</span></span>
- <span data-ttu-id="2f465-139">10/14/2019</span><span class="sxs-lookup"><span data-stu-id="2f465-139">10/14/2019</span></span>
- <span data-ttu-id="2f465-140">14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="2f465-140">October 14, 2019</span></span>
- <span data-ttu-id="2f465-141">Lundi 14 octobre 2019</span><span class="sxs-lookup"><span data-stu-id="2f465-141">Monday, October 14, 2019</span></span>
 

<span data-ttu-id="2f465-142">Pour vous aider à identifier la *Date de début du service* , vous pouvez créer une explication de modèle.</span><span class="sxs-lookup"><span data-stu-id="2f465-142">To help identify the *Service Start Date* you can create a pattern explanation.</span></span>

1. <span data-ttu-id="2f465-143">Dans la section explication, sélectionnez **nouveau**, puis tapez un nom (par exemple, *Date*).</span><span class="sxs-lookup"><span data-stu-id="2f465-143">In the Explanation section, select **New**, and then type a name (for example, *Date*).</span></span>
2. <span data-ttu-id="2f465-144">Pour le type, sélectionnez **liste de motifs**.</span><span class="sxs-lookup"><span data-stu-id="2f465-144">For the Type, select **Pattern list**.</span></span>
3. <span data-ttu-id="2f465-145">Pour la valeur, vous devez indiquer la variation de date telle qu’elle apparaît dans les fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="2f465-145">For the value, you need to provide the date variation as they appear in the sample files.</span></span> <span data-ttu-id="2f465-146">Par exemple, si des formats de date s’affichent sous la forme 0/00/0000, vous devez entrer les variations susceptibles d’apparaître dans vos documents, telles que :</span><span class="sxs-lookup"><span data-stu-id="2f465-146">For example, if you have date formats that appear as 0/00/0000, you would enter any variations that might appear in your documents, such as:</span></span>
    - <span data-ttu-id="2f465-147">0/0/0000</span><span class="sxs-lookup"><span data-stu-id="2f465-147">0/0/0000</span></span>
    - <span data-ttu-id="2f465-148">0/00/0000</span><span class="sxs-lookup"><span data-stu-id="2f465-148">0/00/0000</span></span>
    - <span data-ttu-id="2f465-149">00/0/0000</span><span class="sxs-lookup"><span data-stu-id="2f465-149">00/0/0000</span></span>
    - <span data-ttu-id="2f465-150">00/00/0000</span><span class="sxs-lookup"><span data-stu-id="2f465-150">00/00/0000</span></span>
4. <span data-ttu-id="2f465-151">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-151">Select **Save**.</span></span>


### <a name="use-the-explanation-library"></a><span data-ttu-id="2f465-152">Utiliser la bibliothèque d’explication</span><span class="sxs-lookup"><span data-stu-id="2f465-152">Use the Explanation library</span></span>

<span data-ttu-id="2f465-153">Pour créer des explications pour des éléments tels que des dates, il est beaucoup plus facile d’utiliser la bibliothèque d’explications que d’entrer manuellement toutes les variantes.</span><span class="sxs-lookup"><span data-stu-id="2f465-153">For creating explanations for things such as dates, it is much easier to use the explanation library than to manually enter all variations.</span></span> <span data-ttu-id="2f465-154">La bibliothèque d’explications est un ensemble d’explications prégénérées d’expressions et de modèles.</span><span class="sxs-lookup"><span data-stu-id="2f465-154">The explanation library is a set of pre-built phrase and pattern explanations.</span></span> <span data-ttu-id="2f465-155">La bibliothèque tente de fournir tous les formats pour les listes d’expressions ou de modèles courantes, telles que les dates, les numéros de téléphone, le code postal et bien d’autres.</span><span class="sxs-lookup"><span data-stu-id="2f465-155">The library tries to provide all formats for common phrase or pattern lists, such as dates, phone numbers, zip code, and many others.</span></span> 

<span data-ttu-id="2f465-156">Pour notre exemple de *Date de début de service* , il est plus efficace d’utiliser l’explication prédéfinie pour la *Date* dans la bibliothèque d’explication :</span><span class="sxs-lookup"><span data-stu-id="2f465-156">For our *Service Start Date* example, it is more efficient to use the pre-built explanation for *Date* in the explanation library:</span></span>

1. <span data-ttu-id="2f465-157">Dans la **section Explication**, \* \* sélectionnez **nouveau**, puis sélectionnez **à partir de la bibliothèque d’explication**.</span><span class="sxs-lookup"><span data-stu-id="2f465-157">In the **Explanation section**,\*\* select **New**, and then select **From explanation library**.</span></span>
2. <span data-ttu-id="2f465-158">Dans la bibliothèque d’explication, sélectionnez **Date**.</span><span class="sxs-lookup"><span data-stu-id="2f465-158">From the explanation library, select **Date**.</span></span> <span data-ttu-id="2f465-159">Vous pouvez afficher toutes les variantes de date qui seront reconnues.</span><span class="sxs-lookup"><span data-stu-id="2f465-159">You can view all variations of date that will be recognized.</span></span>
3. <span data-ttu-id="2f465-160">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="2f465-160">Select **Add**.</span></span></br>

    ![Bibliothèque d’explications](../media/content-understanding/explanation-library.png) 

4. <span data-ttu-id="2f465-162">Sur la page **créer une explication** , les informations de *Date* de la bibliothèque d’explication renseignent automatiquement les champs.</span><span class="sxs-lookup"><span data-stu-id="2f465-162">On the **Create an explanation** page, the *Date* information from the explanation library will autofill the fields.</span></span> <span data-ttu-id="2f465-163">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-163">Select **Save**.</span></span></br>

    ![Bibliothèque d’explications](../media/content-understanding/date-explanation-library.png) 

 
## <a name="train-the-model"></a><span data-ttu-id="2f465-165">Former le modèle</span><span class="sxs-lookup"><span data-stu-id="2f465-165">Train the model</span></span> 

<span data-ttu-id="2f465-166">L’enregistrement de votre explication démarrera la formation.</span><span class="sxs-lookup"><span data-stu-id="2f465-166">Saving your explanation will start the training.</span></span> <span data-ttu-id="2f465-167">Si votre modèle dispose de suffisamment d’informations pour extraire les données de vos fichiers d’exemple étiquetés, vous verrez chaque fichier étiqueté avec **match**.</span><span class="sxs-lookup"><span data-stu-id="2f465-167">If your model has enough information to extract the data from your labeled example files, you will see each file labeled with **Match**.</span></span>  

![Bibliothèque d’explications](../media/content-understanding/match2.png) 

<span data-ttu-id="2f465-169">Si l’explication ne contient pas suffisamment d’informations pour rechercher les données que vous souhaitez extraire, chaque fichier sera étiqueté sans **correspondance**.</span><span class="sxs-lookup"><span data-stu-id="2f465-169">If the explanation does not have enough information to find the data you want to extract, each file will be labeled with **Mismatch**.</span></span> <span data-ttu-id="2f465-170">Vous pouvez cliquer sur les fichiers qui ne correspondent pas pour obtenir plus d’informations sur les raisons d’une incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="2f465-170">You can click on the Mismatched files to see more information about why there was a mismatch.</span></span>


## <a name="add-another-explanation"></a><span data-ttu-id="2f465-171">Ajouter une autre explication</span><span class="sxs-lookup"><span data-stu-id="2f465-171">Add another explanation</span></span>

<span data-ttu-id="2f465-172">En règle générale, l’incompatibilité est une indication que l’explication que nous avons fournie n’a pas fourni suffisamment d’informations pour extraire la valeur de la date de début du service pour qu’elle corresponde à nos fichiers étiquetés.</span><span class="sxs-lookup"><span data-stu-id="2f465-172">Often the mismatch is an indication that the explanation we provided did not provide enough information to extract the service start date value to match our labeled files.</span></span> <span data-ttu-id="2f465-173">Vous devrez peut-être le modifier ou ajouter une autre explication.</span><span class="sxs-lookup"><span data-stu-id="2f465-173">You may need to edit it, or add another explanation.</span></span>

<span data-ttu-id="2f465-174">Pour notre exemple, nous constatons que la *Date de début de* la chaîne de texte de Always précède la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="2f465-174">For our example, we notice that the text string *Start Service date of* always precedes the actual value.</span></span> <span data-ttu-id="2f465-175">Pour vous aider à identifier la date de début du service, nous pouvons créer une explication de l’expression.</span><span class="sxs-lookup"><span data-stu-id="2f465-175">To help identify the Service Start Date we can create a phrase explanation.</span></span>

1. <span data-ttu-id="2f465-176">Dans la section explication, sélectionnez **nouveau**, puis tapez un nom (par exemple, *chaîne de préfixe*).</span><span class="sxs-lookup"><span data-stu-id="2f465-176">In the Explanation section, select **New**, and then type a name (for example, *Prefix String*).</span></span>
2. <span data-ttu-id="2f465-177">Pour le type, sélectionnez **liste des expressions**.</span><span class="sxs-lookup"><span data-stu-id="2f465-177">For the Type, select **Phrase list**.</span></span>
3. <span data-ttu-id="2f465-178">Utiliser la *Date de début du service* comme valeur.</span><span class="sxs-lookup"><span data-stu-id="2f465-178">Use *Service Start Date of* as the value.</span></span>
4. <span data-ttu-id="2f465-179">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2f465-179">Select **Save**.</span></span>

    ![Bibliothèque d’explications](../media/content-understanding/prefix-string.png) 


## <a name="train-the-model"></a><span data-ttu-id="2f465-181">Former le modèle</span><span class="sxs-lookup"><span data-stu-id="2f465-181">Train the model</span></span>

<span data-ttu-id="2f465-182">L’enregistrement de votre explication redémarrera la formation, cette fois en utilisant les explications de notre exemple.</span><span class="sxs-lookup"><span data-stu-id="2f465-182">Saving your explanation will start the training again, this time using both explanations in our example.</span></span> <span data-ttu-id="2f465-183">Si votre modèle dispose de suffisamment d’informations pour extraire les données de vos fichiers d’exemple étiquetés, vous verrez chaque fichier étiqueté avec **match**.</span><span class="sxs-lookup"><span data-stu-id="2f465-183">If your model has enough information to extract the data from your labeled example files, you will see each file labeled with **Match**.</span></span> 

<span data-ttu-id="2f465-184">Si vous recevez une nouvelle fois une **incompatibilité** avec vos fichiers étiquetés, vous devrez peut-être créer une autre explication pour fournir au modèle plus d’informations afin d’identifier le type de document ou d’apporter des modifications à vos existants.</span><span class="sxs-lookup"><span data-stu-id="2f465-184">If you again receive a **Mismatch** on your labeled files, you may need to create another explanation to provide the model more information to identify the document type, or look at making changes to your existing ones.</span></span>

## <a name="test-your-model"></a><span data-ttu-id="2f465-185">Tester votre modèle</span><span class="sxs-lookup"><span data-stu-id="2f465-185">Test your model</span></span>

<span data-ttu-id="2f465-186">Si vous avez reçu une correspondance sur vos exemples de fichiers étiquetés, vous pouvez maintenant tester votre modèle sur vos fichiers d’exemple sans étiquette restants.</span><span class="sxs-lookup"><span data-stu-id="2f465-186">If you received a match on your labeled example files, you can now test your model on your remaining unlabeled example files.</span></span>

1. <span data-ttu-id="2f465-187">Sur la page d’accueil du modèle, cliquez sur l’onglet **test** .  Cette opération exécutera le modèle sur vos fichiers d’exemple sans étiquette.</span><span class="sxs-lookup"><span data-stu-id="2f465-187">On the model home page, click the **Test** tab.  This will run the model on your unlabeled example files.</span></span>
2. <span data-ttu-id="2f465-188">Dans la liste des **fichiers test** , vos exemples de fichiers s’affichent et s’affichent si le modèle peut extraire les informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="2f465-188">In the **Test files** list, your example files will display and will show if the model is able to extract the information you need from them.</span></span> <span data-ttu-id="2f465-189">Vous pouvez utiliser ces informations pour déterminer l’efficacité de votre classifieur lors de l’identification de vos documents.</span><span class="sxs-lookup"><span data-stu-id="2f465-189">You can use this information to help determine the effectiveness of your classifier in identifying your documents.</span></span>

    ![Tester vos fichiers](../media/content-understanding/test-filies-extractor.png) 

## <a name="see-also"></a><span data-ttu-id="2f465-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f465-191">See Also</span></span>
  




