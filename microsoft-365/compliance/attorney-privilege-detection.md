---
title: Configurer la détection des privilèges client-avocat dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez le modèle de détection des privilèges client-avocat pour utiliser la détection basée sur l’apprentissage automatique du contenu privilégié lors de l’examen du contenu dans Advanced eDiscovery cas.
ms.openlocfilehash: 73a0efeece7bc331045e9bbe1a1da56f9fd24700
ms.sourcegitcommit: 9ce9001aa41172152458da27c1c52825355f426d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2020
ms.locfileid: "47358040"
---
# <a name="set-up-attorney-client-privilege-detection-in-advanced-ediscovery"></a><span data-ttu-id="4c82a-103">Configurer la détection des privilèges client-avocat dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4c82a-103">Set up attorney-client privilege detection in Advanced eDiscovery</span></span>

<span data-ttu-id="4c82a-104">Un aspect majeur et coûteux de la phase de révision de tout processus eDiscovery consiste à examiner des documents pour le contenu privilégié.</span><span class="sxs-lookup"><span data-stu-id="4c82a-104">A major and costly aspect of the review phase of any eDiscovery process is reviewing documents for privileged content.</span></span> <span data-ttu-id="4c82a-105">Advanced eDiscovery permet une détection basée sur l’apprentissage automatique du contenu privilégié pour rendre ce processus plus efficace.</span><span class="sxs-lookup"><span data-stu-id="4c82a-105">Advanced eDiscovery provides machine learning-based detection of privileged content to make this process more efficient.</span></span> <span data-ttu-id="4c82a-106">Cette fonctionnalité est appelée *détection des privilèges client-avocat.*</span><span class="sxs-lookup"><span data-stu-id="4c82a-106">This feature is called *attorney-client privilege detection*.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="4c82a-107">Comment cela fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="4c82a-107">How does it work?</span></span>

<span data-ttu-id="4c82a-108">Lorsque la détection des privilèges client-avocat est activée, tous les documents d’un [](analyzing-data-in-review-set.md) jeu à réviser sont traitées par le modèle de détection des privilèges client-avocat lorsque vous analysez les données du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4c82a-108">When attorney-client privilege detection is enabled, all documents in a review set will be processed by the attorney-client privilege detection model when you [analyze the data](analyzing-data-in-review-set.md) in the review set.</span></span> <span data-ttu-id="4c82a-109">Le modèle recherche deux éléments :</span><span class="sxs-lookup"><span data-stu-id="4c82a-109">The model looks for two things:</span></span>

- <span data-ttu-id="4c82a-110">Contenu privilégié : le modèle utilise l’apprentissage automatique pour déterminer la probabilité que le document contienne du contenu de nature juridique.</span><span class="sxs-lookup"><span data-stu-id="4c82a-110">Privileged content – The model uses machine learning to determine the likelihood that the document contains content that is legal in nature.</span></span>

- <span data-ttu-id="4c82a-111">Participants : dans le cadre de la configuration de la détection des privilèges client-avocat, vous devez soumettre une liste d’avocats pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4c82a-111">Participants – As part of setting up attorney-client privilege detection, you have to submit a list of attorneys for your organization.</span></span> <span data-ttu-id="4c82a-112">Le modèle compare ensuite les participants du document avec la liste des avocats pour déterminer si un document a au moins un participant avocat.</span><span class="sxs-lookup"><span data-stu-id="4c82a-112">The model then compares the participants of the document with the attorney list to determine if a document has at least one attorney participant.</span></span>

<span data-ttu-id="4c82a-113">Le modèle produit les trois propriétés suivantes pour chaque document :</span><span class="sxs-lookup"><span data-stu-id="4c82a-113">The model produces the following three properties for every document:</span></span>

- <span data-ttu-id="4c82a-114">**AttorneyClientPrivilegeScore :** La probabilité que le document soit de nature juridique ; les valeurs du score sont entre **0** et **1**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-114">**AttorneyClientPrivilegeScore:** The likelihood the document is legal in nature; the values for the score are between **0** and **1**.</span></span>

- <span data-ttu-id="4c82a-115">**HasAttorney :** Cette propriété est définie sur **true si** l’un des participants au document est répertorié dans la liste des avocats ; Sinon, la valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-115">**HasAttorney:** This property is set to **true** if one of the document participants is listed in the attorney list; otherwise the value is **false**.</span></span> <span data-ttu-id="4c82a-116">La valeur est également **faux** si votre organisation n’a pas chargé de liste d’avocat.</span><span class="sxs-lookup"><span data-stu-id="4c82a-116">The value is also set to **false** if your organization didn't upload an attorney list.</span></span>

- <span data-ttu-id="4c82a-117">**IsPrivilege :** Cette propriété est définie sur **true** si la valeur de **AttorneyClientPrivilegeScore** est supérieure au seuil ou si le document a un participant avocat ;  Sinon, la valeur est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-117">**IsPrivilege:** This property is set to **true** if the value for **AttorneyClientPrivilegeScore** is above the threshold *or* if the document has an attorney participant; otherwise the value is set to **false**.</span></span>

<span data-ttu-id="4c82a-118">Ces propriétés (et leurs valeurs correspondantes) sont ajoutées aux métadonnées de fichier des documents dans un jeu à réviser, comme illustré dans la capture d’écran suivante :</span><span class="sxs-lookup"><span data-stu-id="4c82a-118">These properties (and their corresponding values) are added to the file metadata of the documents in a review set, as shown in the following screenshot:</span></span>

![Propriétés de privilège client-avocat affichées dans les métadonnées de fichier](../media/AeDAttorneyClientPrivilegeMetadata.png)

<span data-ttu-id="4c82a-120">Ces trois propriétés sont également utilisables dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4c82a-120">These three properties are also searchable within a review set.</span></span> <span data-ttu-id="4c82a-121">Pour plus d’informations, [voir Interroger les données dans un jeu à réviser.](review-set-search.md)</span><span class="sxs-lookup"><span data-stu-id="4c82a-121">For more information, see [Query the data in a review set](review-set-search.md).</span></span>

## <a name="set-up-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="4c82a-122">Configurer le modèle de détection des privilèges client-avocat</span><span class="sxs-lookup"><span data-stu-id="4c82a-122">Set up the attorney-client privilege detection model</span></span>

<span data-ttu-id="4c82a-123">Pour activer le modèle de détection des privilèges client-avocat, votre organisation doit l’activer, puis télécharger une liste d’avocats.</span><span class="sxs-lookup"><span data-stu-id="4c82a-123">To enable the attorney-client privilege detection model, your organization has to turn it on and then upload an attorney list.</span></span>

### <a name="step-1-turn-on-attorney-client-privilege-detection"></a><span data-ttu-id="4c82a-124">Étape 1 : Activer la détection des privilèges client-avocat</span><span class="sxs-lookup"><span data-stu-id="4c82a-124">Step 1: Turn on attorney-client privilege detection</span></span>

<span data-ttu-id="4c82a-125">Une personne qui est administrateur eDiscovery dans votre organisation (membre du sous-groupe Administrateur eDiscovery dans le groupe de rôles Gestionnaire eDiscovery) doit rendre le modèle disponible dans vos cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="4c82a-125">A person who is an eDiscovery Administrator in your organization (a member of the eDiscovery Administrator subgroup in the eDiscovery Manager role group) must make the model available in your Advanced eDiscovery cases.</span></span>

1. <span data-ttu-id="4c82a-126">Dans le Centre de sécurité & conformité, go to **eDiscovery > Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-126">In the Security & Compliance Center, go to **eDiscovery > Advanced eDiscovery**.</span></span>

2. <span data-ttu-id="4c82a-127">Sur la **Advanced eDiscovery** d’accueil, dans la **vignette Paramètres,** cliquez sur **Configurer les paramètres d’analyse globale.**</span><span class="sxs-lookup"><span data-stu-id="4c82a-127">On the **Advanced eDiscovery** home page, in the **Settings** tile, click **Configure global analytics settings**.</span></span>

   ![Sélectionnez « Configurer les fonctionnalités expérimentales »](../media/AeDExperimentalFeatures.png)

3. <span data-ttu-id="4c82a-129">Sous **l’onglet Paramètres d’analyse,** sélectionnez Gérer le paramètre de **privilège client-avocat.**</span><span class="sxs-lookup"><span data-stu-id="4c82a-129">On the **Analytics settings** tab, select **Manage attorney-client privilege setting**.</span></span>

4. <span data-ttu-id="4c82a-130">Sur la page de menu déroulant **Privilège client-avocat**, utilisez le bouton bascule pour activer la fonctionnalité, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-130">On the **Attorney-client privilege** flyout page, use the toggle to turn on the feature and then select **Save**.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="4c82a-131">Étape 2 : Télécharger liste des avocats (facultatif)</span><span class="sxs-lookup"><span data-stu-id="4c82a-131">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="4c82a-132">Pour tirer pleinement parti du modèle de détection des privilèges client-avocat et utiliser les résultats de la détection Has **Attorney** ou **Potentially Privileged** précédemment décrite, nous vous recommandons de charger une liste d’adresses de messagerie pour les avocats et le personnel juridique qui travaillent pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4c82a-132">To take full advantage of the attorney-client privilege detection model and use the results of the **Has Attorney** or **Potentially Privileged** detection that was previously described, we recommend that you upload a list of email addresses for the lawyers and legal personnel who work for your organization.</span></span> 

<span data-ttu-id="4c82a-133">Pour télécharger une liste d’avocats à utiliser par le modèle de détection des privilèges client-avocat :</span><span class="sxs-lookup"><span data-stu-id="4c82a-133">To upload an attorney list for use by the attorney-client privilege detection model:</span></span>

1. <span data-ttu-id="4c82a-p106">Créez un fichier .csv (sans ligne d’en-tête), puis ajoutez l’adresse de messagerie de chaque personne appropriée sur une ligne distincte. Enregistrez ce fichier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4c82a-p106">Create a .csv file (without a header row) and add the email address for each appropriate person on a separate line. Save this file to your local computer.</span></span>

2. <span data-ttu-id="4c82a-136">Sur la page **Advanced eDiscovery** d’accueil, dans la **vignette Paramètres,** sélectionnez Configurer les fonctionnalités expérimentales, puis sélectionnez Gérer le paramètre de privilège **client-avocat.**</span><span class="sxs-lookup"><span data-stu-id="4c82a-136">On the **Advanced eDiscovery** home page, in the **Settings** tile, select **Configure experimental features**, and then select **Manage attorney-client privilege setting**.</span></span>

   <span data-ttu-id="4c82a-137">La page **Privilège client-avocat** s’affiche et le basculement de détection des privilèges **client-avocat** est allumé.</span><span class="sxs-lookup"><span data-stu-id="4c82a-137">The **Attorney-client privilege** page is displayed, and the **Attorney-client privilege detection** toggle is turned on.</span></span>

   ![Page de volant de privilège client-avocat](../media/AeDUploadAttorneyList.png)

3. <span data-ttu-id="4c82a-139">Sélectionnez **Parcourir,** puis recherchez et sélectionnez .csv fichier que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="4c82a-139">Select **Browse** and then find and select the .csv file that you created in step 1.</span></span>

4. <span data-ttu-id="4c82a-140">Sélectionnez **Enregistrer** pour télécharger la liste des avocats.</span><span class="sxs-lookup"><span data-stu-id="4c82a-140">Select **Save** to upload the attorney list.</span></span>

## <a name="use-the-attorney-client-privilege-detection-model"></a><span data-ttu-id="4c82a-141">Utiliser le modèle de détection des privilèges client-avocat</span><span class="sxs-lookup"><span data-stu-id="4c82a-141">Use the attorney-client privilege detection model</span></span>

<span data-ttu-id="4c82a-142">Suivez les étapes de cette section pour utiliser la détection des privilèges client-avocat pour les documents d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="4c82a-142">Follow the steps in this section to use attorney-client privilege detection for documents in a review set.</span></span>

### <a name="step-1-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="4c82a-143">Étape 1 : Créer un groupe de balises intelligentes avec le modèle de détection des privilèges client-avocat</span><span class="sxs-lookup"><span data-stu-id="4c82a-143">Step 1: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="4c82a-144">L’un des principaux moyens d’afficher les résultats de la détection du privilège client-avocat dans le cadre de votre processus de révision est d’utiliser un groupe de balises actives.</span><span class="sxs-lookup"><span data-stu-id="4c82a-144">One of the primary ways to see the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="4c82a-145">Un groupe de balises actives indique les résultats de la détection de privilège client-avocat et affiche les résultats en ligne en regard des balises dans un groupe de balises actives.</span><span class="sxs-lookup"><span data-stu-id="4c82a-145">A smart tag group indicates the results of the attorney-client privilege detection and shows the results in-line next to the tags in a smart tag group.</span></span> <span data-ttu-id="4c82a-146">Cela vous permet d’identifier rapidement les documents potentiellement privilégiés lors de la révision des documents.</span><span class="sxs-lookup"><span data-stu-id="4c82a-146">This lets you quickly identify potentially privileged documents during document review.</span></span> <span data-ttu-id="4c82a-147">De plus, vous pouvez également utiliser les balises du groupe de balises actives pour marquer des documents comme privilégiés ou non privilégiés.</span><span class="sxs-lookup"><span data-stu-id="4c82a-147">Additionally, you can also use the tags in the smart tag group to tag documents as privileged or non-privileged.</span></span> <span data-ttu-id="4c82a-148">Pour plus d’informations sur les balises intelligentes, voir [Configurer des balises intelligentes dans Advanced eDiscovery](smart-tags.md).</span><span class="sxs-lookup"><span data-stu-id="4c82a-148">For more information about smart tags, see [Set up smart tags in Advanced eDiscovery](smart-tags.md).</span></span>

1. <span data-ttu-id="4c82a-149">Dans le jeu à réviser qui contient les documents que vous avez analysés à l’étape 1, sélectionnez Gérer le jeu à **réviser,** puis **sélectionnez Gérer les balises.**</span><span class="sxs-lookup"><span data-stu-id="4c82a-149">In the review set that contains the documents that you analyzed in Step 1, select **Manage review set** and then select **Manage tags**.</span></span>
 
2. <span data-ttu-id="4c82a-150">Sous **Balises,** sélectionnez le pull-down à côté **d’Ajouter** un groupe, puis **sélectionnez Ajouter un groupe de balises intelligentes.**</span><span class="sxs-lookup"><span data-stu-id="4c82a-150">Under **Tags**, select the pull-down next to **Add group** and then select **Add smart tag group**.</span></span>

   ![Sélectionnez « Ajouter un groupe de balises intelligentes »](../media/AeDCreateSmartTag.png)

3. <span data-ttu-id="4c82a-152">On the **Choose a model for your smart tag** page, choose **Select** next to **Attorney-client privilege**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-152">On the **Choose a model for your smart tag** page, choose **Select** next to **Attorney-client privilege**.</span></span>

   <span data-ttu-id="4c82a-153">Un groupe de balises **nommé Privilège client-avocat** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4c82a-153">A tag group named **Attorney-client privilege** is displayed.</span></span> <span data-ttu-id="4c82a-154">Il contient deux balises enfants nommées **Positive** et **Negative,** qui correspondent aux résultats possibles produits par le modèle.</span><span class="sxs-lookup"><span data-stu-id="4c82a-154">It contains two child tags named **Positive** and **Negative**, which correspond to the possible results produced by the model.</span></span>

   ![Groupe de balises à puce privilège client-avocat](../media/AeDAttorneyClientSmartTagGroup.png)

3. <span data-ttu-id="4c82a-156">Renommez le groupe de balises et les balises selon votre avis.</span><span class="sxs-lookup"><span data-stu-id="4c82a-156">Rename the tag group and tags as appropriate for your review.</span></span> <span data-ttu-id="4c82a-157">Par exemple, vous pouvez renommer **Positive** en **Privilégié** et **Négatif** en **Non privilégié**.</span><span class="sxs-lookup"><span data-stu-id="4c82a-157">For example, you can rename **Positive** to **Privileged** and **Negative** to **Not privileged**.</span></span>

### <a name="step-2-analyze-a-review-set"></a><span data-ttu-id="4c82a-158">Étape 2 : Analyser un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="4c82a-158">Step 2: Analyze a review set</span></span>

<span data-ttu-id="4c82a-159">Lorsque vous analysez les documents d’un jeu à réviser, le modèle de détection des privilèges client-avocat s’exécute également et les propriétés correspondantes (décrites dans How [does it work?](#how-does-it-work) sont ajoutées à chaque document du jeu à réviser).</span><span class="sxs-lookup"><span data-stu-id="4c82a-159">When you analyze the documents in a review set, the attorney-client privilege detection model will also run and the corresponding properties (described in [How does it work?](#how-does-it-work) will be added to every document in the review set.</span></span> <span data-ttu-id="4c82a-160">Pour plus d’informations sur l’analyse des données dans le jeu à réviser, voir Analyser les données dans un jeu à [réviser Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="4c82a-160">For more information about analyzing data in review set, see [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-3-use-the-smart-tag-group-for-review-of-privileged-content"></a><span data-ttu-id="4c82a-161">Étape 3 : Utiliser le groupe de balises intelligentes pour passer en revue le contenu privilégié</span><span class="sxs-lookup"><span data-stu-id="4c82a-161">Step 3: Use the smart tag group for review of privileged content</span></span>

<span data-ttu-id="4c82a-162">Après l’analyse de l’ensemble de révision et la configuration des balises intelligentes, l’étape suivante consiste à examiner les documents.</span><span class="sxs-lookup"><span data-stu-id="4c82a-162">After analyzing the review set and setting up smart tags, the next step is to review the documents.</span></span> <span data-ttu-id="4c82a-163">Si le modèle a déterminé que le document est  potentiellement privilégié, la balise intelligente correspondante dans le panneau de marquage indiquera les résultats suivants obtenus par la détection des privilèges client-avocat :</span><span class="sxs-lookup"><span data-stu-id="4c82a-163">If the model has determined the document is potentially privileged, the corresponding smart tag in the **Tagging panel** will indicate the following results produced by the attorney-client privilege detection:</span></span>

- <span data-ttu-id="4c82a-164">Si le document possède du contenu de  nature juridique, le contenu de l’étiquette Legal s’affiche à côté de la balise smart correspondante (qui est dans ce cas la balise **positive** par défaut).</span><span class="sxs-lookup"><span data-stu-id="4c82a-164">If the document has content that may be legal in nature, the label **Legal content** is displayed next to the corresponding smart tag (which in this case is the default **Positive** tag).</span></span>

- <span data-ttu-id="4c82a-165">Si le document contient un participant qui figure dans la liste des avocats de votre organisation, l’étiquette **Avocat** s’affiche à côté de la balise active correspondante (qui est également la balise **Positive** par défaut dans ce cas).</span><span class="sxs-lookup"><span data-stu-id="4c82a-165">If the document has a participant who is found in your organization's attorney list, the label **Attorney** is displayed next to the corresponding smart tag (which in this case is also the default **Positive** tag).</span></span>

- <span data-ttu-id="4c82a-166">Si le document contient du contenu de *nature* juridique et qu’un  participant  figure dans la liste des avocats, le contenu juridique et les étiquettes Avocat sont affichés.</span><span class="sxs-lookup"><span data-stu-id="4c82a-166">If the document has content that may be legal in nature *and* has a participant found in the attorney list, both the **Legal content**  and **Attorney** labels are displayed.</span></span> 

<span data-ttu-id="4c82a-167">Si le modèle détermine qu’un document ne contient pas de contenu de nature légale ou qu’il ne contient pas de participant de la liste des avocats, aucune des étiquettes n’est affichée dans le panneau de marquage.</span><span class="sxs-lookup"><span data-stu-id="4c82a-167">If the model determines that a document doesn't contain content that is legal in nature or doesn't contain a participant from the attorney list, then neither label is displayed in the tagging panel.</span></span>

<span data-ttu-id="4c82a-168">Par exemple, les captures d’écran suivantes montrent deux documents.</span><span class="sxs-lookup"><span data-stu-id="4c82a-168">For example, the following screenshots show two documents.</span></span> <span data-ttu-id="4c82a-169">Le premier contient du contenu de nature légale et un participant trouvé dans la liste des avocats.</span><span class="sxs-lookup"><span data-stu-id="4c82a-169">The first one contains content that is legal in nature and has a participant found in the list of attorneys.</span></span> <span data-ttu-id="4c82a-170">Le second ne contient ni étiquette, ni aucune étiquette.</span><span class="sxs-lookup"><span data-stu-id="4c82a-170">The second contains neither and therefore doesn't display any labels.</span></span>

![Document avec étiquettes de contenu avocat et juridique](../media/AeDTaggingPanelLegalContentAttorney.png)

![Document sans étiquette](../media/AeDTaggingPanelNegative.png)

<span data-ttu-id="4c82a-173">Après avoir passé en revue un document pour voir s’il contient du contenu privilégié, vous pouvez marquer le document avec la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="4c82a-173">After you review a document to see if it contains privileged content, you can tag the document with the appropriate tag.</span></span>
