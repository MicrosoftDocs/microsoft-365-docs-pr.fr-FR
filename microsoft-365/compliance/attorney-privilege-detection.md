---
title: Configuration de la détection des droits du client dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
description: Utilisez le modèle de détection des privilèges du client avocat pour utiliser la détection basée sur l’apprentissage automatique du contenu privilégié lors de l’examen du contenu dans un cas avancé de découverte électronique.
ms.openlocfilehash: 8fb635e429af2ae4d796e9c847a34d949d8dd6d9
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42079252"
---
# <a name="set-up-attorney-client-privilege-detection-in-advanced-ediscovery"></a><span data-ttu-id="77e9f-103">Configuration de la détection des droits du client dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="77e9f-103">Set up attorney-client privilege detection in Advanced eDiscovery</span></span>

<span data-ttu-id="77e9f-104">Un aspect majeur et coûteux de la phase de révision d’un processus eDiscovery consiste à examiner des documents pour le contenu privilégié.</span><span class="sxs-lookup"><span data-stu-id="77e9f-104">A major and costly aspect of the review phase of any eDiscovery process is reviewing documents for privileged content.</span></span> <span data-ttu-id="77e9f-105">Advanced eDiscovery offre une fonctionnalité de détection de contenu privilégié basée sur l’apprentissage d’un ordinateur pour améliorer l’efficacité de ce processus.</span><span class="sxs-lookup"><span data-stu-id="77e9f-105">Advanced eDiscovery provides machine learning-based detection of privileged content to make this process more efficient.</span></span> <span data-ttu-id="77e9f-106">Cette fonctionnalité est appelée *détection des privilèges client*.</span><span class="sxs-lookup"><span data-stu-id="77e9f-106">This feature is called *attorney-client privilege detection*.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="77e9f-107">Comment cela fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="77e9f-107">How does it work?</span></span>

<span data-ttu-id="77e9f-108">Lorsque la détection de privilèges client est activée, tous les documents d’un ensemble de révision sont traités par le modèle de détection de privilège du client avocat lors de l' [analyse des données](analyzing-data-in-review-set.md) dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-108">When attorney-client privilege detection is enabled, all documents in a review set will be processed by the attorney-client privilege detection model when you [analyze the data](analyzing-data-in-review-set.md) in the review set.</span></span> <span data-ttu-id="77e9f-109">Le modèle recherche deux éléments :</span><span class="sxs-lookup"><span data-stu-id="77e9f-109">The model looks for two things:</span></span>

- <span data-ttu-id="77e9f-110">Contenu privilégié : le modèle utilise l’apprentissage automatique d’ordinateur pour déterminer si le document contient du contenu juridique.</span><span class="sxs-lookup"><span data-stu-id="77e9f-110">Privileged content – The model uses machine learning to determine the likelihood that the document contains content that is legal in nature.</span></span>

- <span data-ttu-id="77e9f-111">Participants : dans le cadre de la configuration de la détection des privilèges client, vous devez soumettre une liste d’avocats pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="77e9f-111">Participants – As part of setting up attorney-client privilege detection, you have to submit a list of attorneys for your organization.</span></span> <span data-ttu-id="77e9f-112">Le modèle compare ensuite les participants du document à la liste des avocats afin de déterminer si un document a au moins un participant à un avocat.</span><span class="sxs-lookup"><span data-stu-id="77e9f-112">The model then compares the participants of the document with the attorney list to determine if a document has at least one attorney participant.</span></span>

<span data-ttu-id="77e9f-113">Le modèle produit les trois propriétés suivantes pour chaque document :</span><span class="sxs-lookup"><span data-stu-id="77e9f-113">The model produces the following three properties for every document:</span></span>

- <span data-ttu-id="77e9f-114">**AttorneyClientPrivilegeScore :** La probabilité que le document soit juridique ; les valeurs du score sont comprises entre **0** et **1**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-114">**AttorneyClientPrivilegeScore:** The likelihood the document is legal in nature; the values for the score are between **0** and **1**.</span></span>

- <span data-ttu-id="77e9f-115">**HasAttorney :** Cette propriété est définie sur **true** si l’un des participants du document est répertorié dans la liste des avocats ; Sinon, la valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-115">**HasAttorney:** This property is set to **true** if one of the document participants is listed in the attorney list; otherwise the value is **false**.</span></span> <span data-ttu-id="77e9f-116">La valeur est également définie sur **false** si votre organisation n’a pas téléchargé de liste d’avocats.</span><span class="sxs-lookup"><span data-stu-id="77e9f-116">The value is also set to **false** if your organization didn't upload an attorney list.</span></span>

- <span data-ttu-id="77e9f-117">**IsPrivilege :** Cette propriété est définie sur **true** si la valeur de **AttorneyClientPrivilegeScore** est supérieure au seuil *ou* si le document a un participant à un avocat ; Sinon, la valeur est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-117">**IsPrivilege:** This property is set to **true** if the value for **AttorneyClientPrivilegeScore** is above the threshold *or* if the document has an attorney participant; otherwise the value is set to **false**.</span></span>

<span data-ttu-id="77e9f-118">Ces propriétés (et leurs valeurs correspondantes) sont ajoutées aux métadonnées de fichier des documents dans un jeu de révision, comme illustré dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="77e9f-118">These properties (and their corresponding values) are added to the file metadata of the documents in a review set, as shown in the following screenshot:</span></span>

![Avocat-propriétés du privilège client affichées dans les métadonnées de fichier](../media/AeDAttorneyClientPrivilegeMetadata.png)

<span data-ttu-id="77e9f-120">Ces trois propriétés peuvent également faire l’objet d’une recherche dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-120">These three properties are also searchable within a review set.</span></span> <span data-ttu-id="77e9f-121">Pour plus d’informations, reportez-vous à [la rubrique Query the Data in a Review Set](review-set-search.md).</span><span class="sxs-lookup"><span data-stu-id="77e9f-121">For more information, see [Query the data in a review set](review-set-search.md).</span></span>

## <a name="set-up-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="77e9f-122">Configurer le modèle de détection de privilèges client pour les avocats</span><span class="sxs-lookup"><span data-stu-id="77e9f-122">Set up the attorney-client privilege detection model</span></span>

<span data-ttu-id="77e9f-123">Pour activer le modèle de détection des privilèges du client avocat, votre organisation doit l’activer, puis télécharger une liste d’avocats.</span><span class="sxs-lookup"><span data-stu-id="77e9f-123">To enable the attorney-client privilege detection model, your organization has to turn it on and then upload an attorney list.</span></span>

### <a name="step-1-turn-on-attorney-client-privilege-detection"></a><span data-ttu-id="77e9f-124">Étape 1 : activer le juriste-détection des privilèges client</span><span class="sxs-lookup"><span data-stu-id="77e9f-124">Step 1: Turn on attorney-client privilege detection</span></span>

<span data-ttu-id="77e9f-125">Une personne qui est un administrateur de découverte électronique dans votre organisation (membre du sous-groupe administrateur eDiscovery dans le groupe de rôles gestionnaire eDiscovery) doit mettre le modèle à disposition dans vos cas avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="77e9f-125">A person who is an eDiscovery Administrator in your organization (a member of the eDiscovery Administrator subgroup in the eDiscovery Manager role group) must make the model available in your Advanced eDiscovery cases.</span></span>

1. <span data-ttu-id="77e9f-126">Dans le centre de sécurité & conformité, accédez à **ediscovery > Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-126">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery**.</span></span>

2. <span data-ttu-id="77e9f-127">Sur la page d’accueil de la **découverte électronique avancée** , dans la vignette **paramètres** , cliquez sur **configurer les paramètres d’analyse globale**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-127">On the **Advanced eDiscovery** home page, in the **Settings** tile, click **Configure global analytics settings**.</span></span>

   ![Sélectionnez « configurer les fonctionnalités expérimentales »](../media/AeDExperimentalFeatures.png)

3. <span data-ttu-id="77e9f-129">Dans l’onglet Paramètres de l' **analyse** , sélectionnez **gérer le paramètre de privilège client**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-129">On the **Analytics settings** tab, select **Manage attorney-client privilege setting**.</span></span>

4. <span data-ttu-id="77e9f-130">Sur la page de menu **déroulante avocat-client** , utilisez le bouton bascule pour activer la fonctionnalité, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-130">On the **Attorney-client privilege** flyout page, use the toggle to turn on the feature and then select **Save**.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="77e9f-131">Étape 2 : télécharger une liste d’avocats (facultatif)</span><span class="sxs-lookup"><span data-stu-id="77e9f-131">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="77e9f-132">Pour tirer pleinement parti du modèle de détection des privilèges du client avocat et utiliser les résultats de l’offre d’un **avocat** ou d’une détection **potentiellement privilégiée** décrite précédemment, nous vous recommandons de télécharger une liste d’adresses de messagerie pour les avocats et le personnel juridique qui travaillent pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="77e9f-132">To take full advantage of the attorney-client privilege detection model and use the results of the **Has Attorney** or **Potentially Privileged** detection that was previously described, we recommend that you upload a list of email addresses for the lawyers and legal personnel who work for your organization.</span></span> 

<span data-ttu-id="77e9f-133">Pour télécharger une liste d’avocats à utiliser par le modèle de détection de privilège du client :</span><span class="sxs-lookup"><span data-stu-id="77e9f-133">To upload an attorney list for use by the attorney-client privilege detection model:</span></span>

1. <span data-ttu-id="77e9f-134">Créez un fichier. csv (sans ligne d’en-tête) et ajoutez l’adresse de messagerie de chaque personne appropriée sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="77e9f-134">Create a .csv file (without a header row) and add the email address for each appropriate person on a separate line.</span></span> <span data-ttu-id="77e9f-135">Enregistrez ce fichier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="77e9f-135">Save this file to your local computer.</span></span>

2. <span data-ttu-id="77e9f-136">Sur la page d’accueil de la **découverte électronique avancée** , dans la vignette **paramètres** , sélectionnez **configurer les fonctionnalités expérimentales**, puis sélectionnez **gérer le paramètre de privilège du client**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-136">On the **Advanced eDiscovery** home page, in the **Settings** tile, select **Configure experimental features**, and then select **Manage attorney-client privilege setting**.</span></span>

   <span data-ttu-id="77e9f-137">La page de **privilège avocat-client** s’affiche et le bouton bascule de **détection de privilège client** est activé.</span><span class="sxs-lookup"><span data-stu-id="77e9f-137">The **Attorney-client privilege** page is displayed, and the **Attorney-client privilege detection** toggle is turned on.</span></span>

   ![Page de menu déroulant avocat-privilège client](../media/AeDUploadAttorneyList.png)

3. <span data-ttu-id="77e9f-139">Sélectionnez **Parcourir** , puis recherchez et sélectionnez le fichier. csv que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="77e9f-139">Select **Browse** and then find and select the .csv file that you created in step 1.</span></span>

4. <span data-ttu-id="77e9f-140">Sélectionnez **Enregistrer** pour télécharger la liste des avocats.</span><span class="sxs-lookup"><span data-stu-id="77e9f-140">Select **Save** to upload the attorney list.</span></span>

## <a name="use-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="77e9f-141">Utiliser le modèle de détection des privilèges du client avocat</span><span class="sxs-lookup"><span data-stu-id="77e9f-141">Use the attorney-client privilege detection model</span></span>

<span data-ttu-id="77e9f-142">Suivez les étapes de cette section pour utiliser la détection des privilèges du client avocat pour les documents dans un ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-142">Follow the steps in this section to use attorney-client privilege detection for documents in a review set.</span></span>

### <a name="step-1-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="77e9f-143">Étape 1 : créer un groupe de balises actives avec le modèle de détection de privilège client</span><span class="sxs-lookup"><span data-stu-id="77e9f-143">Step 1: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="77e9f-144">L’utilisation d’un groupe de balises actives est l’une des principales façons de voir les résultats de la détection des droits du client dans votre processus de révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-144">One of the primary ways to see the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="77e9f-145">Un groupe de balises actives indique les résultats de la détection de privilège au client et affiche les résultats en ligne en regard des balises dans un groupe de balises actives.</span><span class="sxs-lookup"><span data-stu-id="77e9f-145">A smart tag group indicates the results of the attorney-client privilege detection and shows the results in-line next to the tags in a smart tag group.</span></span> <span data-ttu-id="77e9f-146">Cela vous permet d’identifier rapidement des documents potentiellement privilégiés lors de la révision d’un document.</span><span class="sxs-lookup"><span data-stu-id="77e9f-146">This lets you quickly identify potentially privileged documents during document review.</span></span> <span data-ttu-id="77e9f-147">En outre, vous pouvez également utiliser les balises dans le groupe de balises actives pour marquer des documents comme étant privilégiés ou non privilégiés.</span><span class="sxs-lookup"><span data-stu-id="77e9f-147">Additionally, you can also use the tags in the smart tag group to tag documents as privileged or non-privileged.</span></span> <span data-ttu-id="77e9f-148">Pour plus d’informations sur les balises actives, voir [configurer les balises actives dans Advanced eDiscovery](smart-tags.md).</span><span class="sxs-lookup"><span data-stu-id="77e9f-148">For more information about smart tags, see [Set up smart tags in Advanced eDiscovery](smart-tags.md).</span></span>

1. <span data-ttu-id="77e9f-149">Dans l’ensemble de révision qui contient les documents que vous avez analysés à l’étape 1, sélectionnez **Manage Review Set** , puis **Manage Tags**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-149">In the review set that contains the documents that you analyzed in Step 1, select **Manage review set** and then select **Manage tags**.</span></span>
 
2. <span data-ttu-id="77e9f-150">Sous **balises**, sélectionnez la liste déroulante en regard de **Ajouter un groupe** , puis sélectionnez Ajouter un **groupe de balises actives**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-150">Under **Tags**, select the pull-down next to **Add group** and then select **Add smart tag group**.</span></span>

   ![Sélectionnez « Ajouter un groupe de balises actives »](../media/AeDCreateSmartTag.png)

3. <span data-ttu-id="77e9f-152">Sur la page **choisir un modèle pour la balise active** , choisissez Sélectionner en regard de l' **option** **avocat-client**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-152">On the **Choose a model for your smart tag** page, choose **Select** next to **Attorney-client privilege**.</span></span>

   <span data-ttu-id="77e9f-153">Un groupe de balises nommé **avocat-le privilège client** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="77e9f-153">A tag group named **Attorney-client privilege** is displayed.</span></span> <span data-ttu-id="77e9f-154">Il contient deux balises enfants nommées **positive** et **Negative**, qui correspondent aux résultats possibles produits par le modèle.</span><span class="sxs-lookup"><span data-stu-id="77e9f-154">It contains two child tags named **Positive** and **Negative**, which correspond to the possible results produced by the model.</span></span>

   ![Groupe de balises actives de privilège de client pour les avocats](../media/AeDAttorneyClientSmartTagGroup.png)

3. <span data-ttu-id="77e9f-156">Renommez le groupe de balises et les balises en fonction de votre révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-156">Rename the tag group and tags as appropriate for your review.</span></span> <span data-ttu-id="77e9f-157">Par exemple, vous pouvez renommer **positif** sur **privilégié** et **négatif** sur **non privilégié**.</span><span class="sxs-lookup"><span data-stu-id="77e9f-157">For example, you can rename **Positive** to **Privileged** and **Negative** to **Not privileged**.</span></span>

### <a name="step-2-analyze-a-review-set"></a><span data-ttu-id="77e9f-158">Étape 2 : analyser un jeu de révision</span><span class="sxs-lookup"><span data-stu-id="77e9f-158">Step 2: Analyze a review set</span></span>

<span data-ttu-id="77e9f-159">Lorsque vous analysez les documents d’un jeu de révision, le modèle de détection des privilèges du client avocat s’exécute également et les propriétés correspondantes (décrites dans [How do it Work ?](#how-does-it-work) sont ajoutées à chaque document de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="77e9f-159">When you analyze the documents in a review set, the attorney-client privilege detection model will also run and the corresponding properties (described in [How does it work?](#how-does-it-work) will be added to every document in the review set.</span></span> <span data-ttu-id="77e9f-160">Pour plus d’informations sur l’analyse des données dans l’ensemble de validation, voir [analyze Data in a Review Set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="77e9f-160">For more information about analyzing data in review set, see [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-3-use-the-smart-tag-group-for-review-of-privileged-content"></a><span data-ttu-id="77e9f-161">Étape 3 : utiliser le groupe de balises actives pour vérifier le contenu privilégié</span><span class="sxs-lookup"><span data-stu-id="77e9f-161">Step 3: Use the smart tag group for review of privileged content</span></span>

<span data-ttu-id="77e9f-162">Après avoir analysé l’ensemble de révision et configuré les balises actives, l’étape suivante consiste à passer en revue les documents.</span><span class="sxs-lookup"><span data-stu-id="77e9f-162">After analyzing the review set and setting up smart tags, the next step is to review the documents.</span></span> <span data-ttu-id="77e9f-163">Si le modèle a déterminé que le document est potentiellement privilégié, la balise active correspondante dans le **panneau balisage** indique les résultats suivants générés par la détection des privilèges du client avocat :</span><span class="sxs-lookup"><span data-stu-id="77e9f-163">If the model has determined the document is potentially privileged, the corresponding smart tag in the **Tagging panel** will indicate the following results produced by the attorney-client privilege detection:</span></span>

- <span data-ttu-id="77e9f-164">Si le contenu du document peut être légal, le **contenu légal** de l’étiquette est affiché en regard de la balise active correspondante (dans ce cas, il s’agit de la balise **positive** par défaut).</span><span class="sxs-lookup"><span data-stu-id="77e9f-164">If the document has content that may be legal in nature, the label **Legal content** is displayed next to the corresponding smart tag (which in this case is the default **Positive** tag).</span></span>

- <span data-ttu-id="77e9f-165">Si le document a un participant trouvé dans la liste des avocats de votre organisation, le **juriste** est affiché en regard de la balise active correspondante (dans ce cas, il s’agit également de la balise **positive** par défaut).</span><span class="sxs-lookup"><span data-stu-id="77e9f-165">If the document has a participant who is found in your organization's attorney list, the label **Attorney** is displayed next to the corresponding smart tag (which in this case is also the default **Positive** tag).</span></span>

- <span data-ttu-id="77e9f-166">Si le document a un contenu qui peut être légal *et* qui a un participant trouvé dans la liste des avocats, les étiquettes de **contenu juridique** et d' **avocat** sont affichées.</span><span class="sxs-lookup"><span data-stu-id="77e9f-166">If the document has content that may be legal in nature *and* has a participant found in the attorney list, both the **Legal content**  and **Attorney** labels are displayed.</span></span> 

<span data-ttu-id="77e9f-167">Si le modèle détermine qu’un document ne contient pas de contenu légal ou qu’il ne contient pas de participant à partir de la liste des avocats, aucune étiquette n’est affichée dans le panneau balisage.</span><span class="sxs-lookup"><span data-stu-id="77e9f-167">If the model determines that a document doesn't contain content that is legal in nature or doesn't contain a participant from the attorney list, then neither label is displayed in the tagging panel.</span></span>

<span data-ttu-id="77e9f-168">Par exemple, les captures d’écran suivantes illustrent deux documents.</span><span class="sxs-lookup"><span data-stu-id="77e9f-168">For example, the following screenshots show two documents.</span></span> <span data-ttu-id="77e9f-169">Le premier contient un contenu légal et un participant se trouve dans la liste des avocats.</span><span class="sxs-lookup"><span data-stu-id="77e9f-169">The first one contains content that is legal in nature and has a participant found in the list of attorneys.</span></span> <span data-ttu-id="77e9f-170">La seconde ne contient pas et, par conséquent, n’affiche aucune étiquette.</span><span class="sxs-lookup"><span data-stu-id="77e9f-170">The second contains neither and therefore doesn't display any labels.</span></span>

![Document avec les étiquettes d’avocat et de contenu juridique](../media/AeDTaggingPanelLegalContentAttorney.png)

![Document sans étiquette](../media/AeDTaggingPanelNegative.png)

<span data-ttu-id="77e9f-173">Après avoir examiné un document pour voir s’il contient du contenu privilégié, vous pouvez le marquer avec la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="77e9f-173">After you review a document to see if it contains privileged content, you can tag the document with the appropriate tag.</span></span>
