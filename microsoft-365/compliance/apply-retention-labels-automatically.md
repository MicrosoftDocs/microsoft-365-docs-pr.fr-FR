---
title: Application automatique d’une étiquette de rétention pour conserver ou supprimer du contenu
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Créez et publiez automatiquement des étiquettes de rétention afin de pouvoir les appliquer de manière automatique pour conserver les éléments dont vous avez besoin et de supprimer ceux qui sont inutiles
ms.openlocfilehash: 7528fed52ae3df1a60303c40df35a42de6bc1f31
ms.sourcegitcommit: 19515d787246d38c4e0da579a767ce67b9dbc2bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "47315813"
---
# <a name="automatically-apply-a-retention-label-to-retain-or-delete-content"></a><span data-ttu-id="91ee5-103">Application automatique d’une étiquette de rétention pour conserver ou supprimer du contenu</span><span class="sxs-lookup"><span data-stu-id="91ee5-103">Automatically apply a retention label to retain or delete content</span></span>

><span data-ttu-id="91ee5-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="91ee5-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="91ee5-105">L’une des fonctionnalités les plus puissantes des [étiquettes de rétention](retention.md) est la possibilité d’appliquer celles-ci automatiquement à tout contenu correspondant à certaines conditions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="91ee5-105">One of the most powerful features of [retention labels](retention.md) is the ability to apply them automatically to content that matches specified conditions.</span></span> <span data-ttu-id="91ee5-106">Dans ce cas, les personnes au sein de votre organisation ne doivent pas appliquer les étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="91ee5-106">In this case, people in your organization don't need to apply the retention labels.</span></span> <span data-ttu-id="91ee5-107">Microsoft 365 s’en charge à leur place.</span><span class="sxs-lookup"><span data-stu-id="91ee5-107">Microsoft 365 does the work for them.</span></span>
  
<span data-ttu-id="91ee5-108">Les étiquettes de rétention appliquées automatiquement sont puissantes pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="91ee5-108">Auto-applying retention labels are powerful because:</span></span>
  
- <span data-ttu-id="91ee5-109">Vous n’avez pas besoin de former les utilisateurs concernant l’ensemble de vos classifications.</span><span class="sxs-lookup"><span data-stu-id="91ee5-109">You don't need to train your users on all of your classifications.</span></span>
    
- <span data-ttu-id="91ee5-110">Vous n’avez pas à dépendre des utilisateurs pour classer tout le contenu correctement.</span><span class="sxs-lookup"><span data-stu-id="91ee5-110">You don't need to rely on users to classify all content correctly.</span></span>
    
- <span data-ttu-id="91ee5-111">Les utilisateurs n’ont plus besoin de connaître les stratégies de gouvernance des données : ils peuvent se concentrer sur leur travail.</span><span class="sxs-lookup"><span data-stu-id="91ee5-111">Users no longer need to know about data governance policies - they can focus on their work.</span></span>
    
<span data-ttu-id="91ee5-112">Vous pouvez appliquer automatiquement des étiquettes de rétention à du contenu lorsque celui-ci contient des informations sensibles, des mots clés, des propriétés pouvant faire l’objet d’une recherche ou une correspondance pour des [classifieurs pouvant être formés](classifier-getting-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="91ee5-112">You can apply retention labels to content automatically when that content contains sensitive information, keywords or searchable properties, or a match for [trainable classifiers](classifier-getting-started-with.md).</span></span>

<span data-ttu-id="91ee5-113">Les processus d’application automatique d’une étiquette de rétention sont fonction des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="91ee5-113">The processes to automatically apply a retention label based on these conditions:</span></span>

![Diagramme des rôles et des tâches pour les étiquettes à appliquer automatiquement](../media/32f2f2fd-18a8-43fd-839d-72ad7a43e069.png)

<span data-ttu-id="91ee5-115">Utilisez les instructions suivantes pour les deux étapes d’administration.</span><span class="sxs-lookup"><span data-stu-id="91ee5-115">Use the following instructions for the two admin steps.</span></span>

> [!NOTE]
> <span data-ttu-id="91ee5-116">Les stratégies automatiques utilisent l’étiquetage côté service avec des conditions pour appliquer automatiquement des étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="91ee5-116">Auto-policies use service-side labeling with conditions to automatically apply retention labels.</span></span> <span data-ttu-id="91ee5-117">Vous pouvez également appliquer automatiquement une étiquette de rétention avec une stratégie d’étiquette lorsque vous procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="91ee5-117">You can also automatically apply a retention label with a label policy when you do the following:</span></span> 
>
> - <span data-ttu-id="91ee5-118">Appliquez une étiquette de rétention par défaut à une bibliothèque, un dossier ou à un groupe de documents SharePoint afin que le contenu sans étiquette dans ce conteneur soit automatiquement étiqueté</span><span class="sxs-lookup"><span data-stu-id="91ee5-118">Apply a default retention label to a SharePoint library, folder, or document set so that unlabeled content in that container is automatically labeled</span></span>
>- <span data-ttu-id="91ee5-119">Application automatique d’une étiquette de rétention pour les e-mails à l’aide de règles</span><span class="sxs-lookup"><span data-stu-id="91ee5-119">Automatically applying a retention label to email by using rules</span></span>
>
> <span data-ttu-id="91ee5-120">Pour ces scénarios, voir [Créer des étiquettes de rétention et les appliquer dans les applications](create-apply-retention-labels.md).</span><span class="sxs-lookup"><span data-stu-id="91ee5-120">For these scenarios, see [Create and apply retention labels in apps](create-apply-retention-labels.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="91ee5-121">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="91ee5-121">Before you begin</span></span>

<span data-ttu-id="91ee5-122">L’administrateur général de votre organisation dispose de toutes les autorisations pour créer et gérer les étiquettes de rétention et leurs stratégies.</span><span class="sxs-lookup"><span data-stu-id="91ee5-122">The global admin for your organization has full permissions to create and edit retention labels and their policies.</span></span> <span data-ttu-id="91ee5-123">Si vous ne vous connectez pas en tant qu’administrateur général, voir [Autorisations nécessaires pour créer et gérer des stratégies et des étiquettes de confidentialité](get-started-with-retention.md#permissions-required-to-create-and-manage-retention-policies-and-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="91ee5-123">If you aren't signing in as a global admin, see [Permissions required to create and manage retention policies and retention labels](get-started-with-retention.md#permissions-required-to-create-and-manage-retention-policies-and-retention-labels).</span></span>

## <a name="how-to-auto-apply-a-retention-label"></a><span data-ttu-id="91ee5-124">Application automatique d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="91ee5-124">How to auto-apply a retention label</span></span>

<span data-ttu-id="91ee5-125">Tout d’abord, créez votre étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="91ee5-125">First, create your retention label.</span></span> <span data-ttu-id="91ee5-126">Créez ensuite une stratégie automatique pour appliquer l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="91ee5-126">Then create an auto-policy to apply that label.</span></span> <span data-ttu-id="91ee5-127">Si vous avez déjà créé votre étiquette de rétention, passez à [Création d’une stratégie automatique](#step-2-create-an-auto-apply-policy).</span><span class="sxs-lookup"><span data-stu-id="91ee5-127">If you have already created your retention label, skip to [creating an auto-policy](#step-2-create-an-auto-apply-policy).</span></span>

<span data-ttu-id="91ee5-128">Les instructions de navigation varient selon que vous utilisez la [gestion des enregistrements](records-management.md) ou non.</span><span class="sxs-lookup"><span data-stu-id="91ee5-128">Navigation instructions depend on whether you're using [records management](records-management.md) or not.</span></span> <span data-ttu-id="91ee5-129">Des instructions sont fournies pour les deux scénarios.</span><span class="sxs-lookup"><span data-stu-id="91ee5-129">Instructions are provided for both scenarios.</span></span>

### <a name="step-1-create-a-retention-label"></a><span data-ttu-id="91ee5-130">Étape 1 : créer une étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="91ee5-130">Step 1: Create a retention label</span></span>

1. <span data-ttu-id="91ee5-131">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="91ee5-131">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="91ee5-132">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="91ee5-132">If you are using records management:</span></span>
        - <span data-ttu-id="91ee5-133">**Solutions** > **Gestion des enregistrements** > **Plan de fichiers** onglet > **+ Créer une étiquette** > **Étiquette de rétention**</span><span class="sxs-lookup"><span data-stu-id="91ee5-133">**Solutions** > **Records management** > **File plan** tab > **+ Create a label** > **Retention label**</span></span>
        
    - <span data-ttu-id="91ee5-134">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="91ee5-134">If you are not using records management:</span></span>
       - <span data-ttu-id="91ee5-135">**Solutions** > **Gouvernance d’informations** > **Étiquettes** onglet > + **Créer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="91ee5-135">**Solutions** > **Information governance** > **Labels** tab > + **Create a label**</span></span>
    
    <span data-ttu-id="91ee5-136">Votre option ne s’affiche pas immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="91ee5-136">Don't immediately see your option?</span></span> <span data-ttu-id="91ee5-137">Sélectionnez tout d’abord **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="91ee5-137">First select **Show all**.</span></span> 

2. <span data-ttu-id="91ee5-138">Suivez les invites de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="91ee5-138">Follow the prompts in the wizard.</span></span> <span data-ttu-id="91ee5-139">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="91ee5-139">If you are using records management:</span></span>
    
    - <span data-ttu-id="91ee5-140">Pour plus d’informations sur les descripteurs de plan de fichier, consultez [Utiliser le plan de gestion des fichiers pour gérer les étiquettes de rétention](file-plan-manager.md)</span><span class="sxs-lookup"><span data-stu-id="91ee5-140">For information about the file plan descriptors, see [Use file plan to manage retention labels](file-plan-manager.md)</span></span>
    
    - <span data-ttu-id="91ee5-141">Pour utiliser l’étiquette de rétention pour déclarer du contenu en tant qu’enregistrement, activez la case à cocher **Utiliser une étiquette pour classifier du contenu en tant qu’« enregistrement »**.</span><span class="sxs-lookup"><span data-stu-id="91ee5-141">To use the retention label to declare content as a record, enable the checkbox **Use label to classify content as a "Record"**.</span></span>

<span data-ttu-id="91ee5-142">Pour modifier une étiquette existante, sélectionnez-la, puis sélectionnez **Modifier l’étiquette** pour démarrer le même Assistant qui vous permet de modifier les descriptions d’étiquette et les [Paramètres éligibles](#updating-retention-labels-and-their-policies) à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="91ee5-142">To edit an existing label, select it, and then select **Edit label** to start the same wizard that lets you change the label descriptions and any [eligible settings](#updating-retention-labels-and-their-policies) from step 2.</span></span> <span data-ttu-id="91ee5-143">Vous pouvez également sélectionner une option disponible **Modifier** pour accéder directement à la page correspondante afin de mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="91ee5-143">Alternatively, select any of the available **Edit** options to go directly to the relevant page to make your update.</span></span>


### <a name="step-2-create-an-auto-apply-policy"></a><span data-ttu-id="91ee5-144">Étape 2 : créer une stratégie d’application automatique</span><span class="sxs-lookup"><span data-stu-id="91ee5-144">Step 2: Create an auto-apply policy</span></span>

<span data-ttu-id="91ee5-145">Lorsque vous créez une stratégie d’application automatique, vous sélectionnez une étiquette de rétention pour l’appliquer automatiquement à du contenu, en fonction des conditions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="91ee5-145">When you create an auto-apply policy, you select a retention label to automatically apply to content, based on the conditions that you specify.</span></span>

1. <span data-ttu-id="91ee5-146">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="91ee5-146">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="91ee5-147">Si vous utilisez la gestion des enregistrements : **Gouvernance d’informations** :</span><span class="sxs-lookup"><span data-stu-id="91ee5-147">If you are using records management: **Information governance**:</span></span>
        - <span data-ttu-id="91ee5-148">**Solutions** > **Gestion des enregistrements** > **Stratégies d’étiquette** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="91ee5-148">**Solutions** > **Records management** > **Label policies** tab > **Auto-apply label**</span></span>
    
    - <span data-ttu-id="91ee5-149">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="91ee5-149">If you are not using records management:</span></span>
        - <span data-ttu-id="91ee5-150">**Solutions** > **Gouvernance d’informations** > **Stratégies d’étiquette** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="91ee5-150">**Solutions** > **Information governance** > **Label policies** tab > **Auto-apply label**</span></span>
    
    <span data-ttu-id="91ee5-151">Votre option ne s’affiche pas immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="91ee5-151">Don't immediately see your option?</span></span> <span data-ttu-id="91ee5-152">Sélectionnez tout d’abord **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="91ee5-152">First select **Show all**.</span></span> 

2. <span data-ttu-id="91ee5-153">Suivez les invites de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="91ee5-153">Follow the prompts in the wizard.</span></span>
    
    <span data-ttu-id="91ee5-154">Pour plus d’informations sur la configuration des conditions qui appliquent automatiquement l’étiquette de rétention, voir la section [Configuration des conditions d’application automatique des étiquettes de rétention](#configuring-conditions-for-auto-apply-retention-labels) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="91ee5-154">For information about configuring the conditions that automatically apply the retention label, see the [Configuring conditions for auto-apply retention labels](#configuring-conditions-for-auto-apply-retention-labels) section on this page.</span></span>
    
    <span data-ttu-id="91ee5-155">Pour plus d’informations sur la prise en charge des emplacements par des étiquettes de rétention, voir la section [Étiquettes de rétention et emplacements](retention.md#retention-label-policies-and-locations).</span><span class="sxs-lookup"><span data-stu-id="91ee5-155">For information about the locations supported by retention labels, see the [Retention labels and locations](retention.md#retention-label-policies-and-locations) section.</span></span>

<span data-ttu-id="91ee5-156">Pour modifier une stratégie d’étiquette d’application existante, sélectionnez-la, puis sélectionnez **Modifier la stratégie** pour démarrer le même Assistant qui vous permet de modifier les descriptions de la stratégie et les [Paramètres éligibles](#updating-retention-labels-and-their-policies) à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="91ee5-156">To edit an existing auto-apply label policy, select it, and then select **Edit policy** to start the same wizard that lets you change the policy description and any [eligible settings](#updating-retention-labels-and-their-policies) from step 2.</span></span> <span data-ttu-id="91ee5-157">Vous pouvez également sélectionner une option disponible **Modifier** pour accéder directement à la page correspondante afin de mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="91ee5-157">Alternatively, select any of the available **Edit** options to go directly to the relevant page to make your update.</span></span>

### <a name="configuring-conditions-for-auto-apply-retention-labels"></a><span data-ttu-id="91ee5-158">Configuration des conditions d’application automatique des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="91ee5-158">Configuring conditions for auto-apply retention labels</span></span>

<span data-ttu-id="91ee5-159">Vous pouvez appliquer automatiquement des étiquettes de rétention au contenu quand celui-ci inclut :</span><span class="sxs-lookup"><span data-stu-id="91ee5-159">You can apply retention labels to content automatically when that content contains:</span></span>

- [<span data-ttu-id="91ee5-160">Types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="91ee5-160">Specific types of sensitive information</span></span>](#auto-apply-labels-to-content-with-specific-types-of-sensitive-information)

- [<span data-ttu-id="91ee5-161">Mots clés spécifiques ou propriétés pouvant faire l’objet d’une recherche qui correspondent à une requête que vous créez</span><span class="sxs-lookup"><span data-stu-id="91ee5-161">Specific keywords or searchable properties that match a query you create</span></span>](#auto-apply-labels-to-content-with-keywords-or-searchable-properties)

- [<span data-ttu-id="91ee5-162">Correspondance pour les classifieurs entraînables</span><span class="sxs-lookup"><span data-stu-id="91ee5-162">A match for trainable classifiers</span></span>](#auto-apply-labels-to-content-by-using-trainable-classifiers)

#### <a name="auto-apply-labels-to-content-with-specific-types-of-sensitive-information"></a><span data-ttu-id="91ee5-163">Application automatique d’étiquettes au contenu incluant des types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="91ee5-163">Auto-apply labels to content with specific types of sensitive information</span></span>

<span data-ttu-id="91ee5-164">Lorsque vous créez des étiquettes de rétention d’application automatique pour des informations sensibles, vous voyez s’afficher la même liste de modèles de stratégie que lorsque vous créez une stratégie de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="91ee5-164">When you create auto-apply retention labels for sensitive information, you see the same list of policy templates as when you create a data loss prevention (DLP) policy.</span></span> <span data-ttu-id="91ee5-165">Chaque modèle de stratégie est préconfiguré pour rechercher des types spécifiques d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="91ee5-165">Each policy template is preconfigured to look for specific types of sensitive information.</span></span> <span data-ttu-id="91ee5-166">Par exemple, le modèle illustré ici recherche les numéros ITIN, SSN et de passeport américains.</span><span class="sxs-lookup"><span data-stu-id="91ee5-166">For example, the template shown here looks for U.S. ITIN, SSN, and passport numbers.</span></span> <span data-ttu-id="91ee5-167">Pour plus d’informations sur la protection contre la perte de données, voir [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="91ee5-167">To learn more about DLP, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
![Modèles de stratégie avec des types d’informations sensibles](../media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)
  
<span data-ttu-id="91ee5-p112">Après avoir sélectionné un modèle de stratégie, vous pouvez ajouter ou supprimer tout type d’informations sensibles, et vous pouvez modifier le nombre d’instances et la précision de correspondance. Dans l’exemple présenté ici, une étiquette de rétention sera appliquée automatiquement uniquement dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="91ee5-p112">After you select a policy template, you can add or remove any types of sensitive information, and you can change the instance count and match accuracy. In the example shown here, a retention label will be auto-applied only when:</span></span>
  
- <span data-ttu-id="91ee5-p113">Le contenu comprend entre 1 et 9 instances de l’un de ces trois types d’informations sensibles. Vous pouvez supprimer la valeur **max** pour la définir sur **any**.</span><span class="sxs-lookup"><span data-stu-id="91ee5-p113">The content contains between 1 and 9 instances of any of these three sensitive information types. You can delete the **max** value so that it changes to **any**.</span></span>
    
- <span data-ttu-id="91ee5-173">Le type d’information sensible est détecté avec une précision de correspondance (ou niveau de confiance) minimale de 75.</span><span class="sxs-lookup"><span data-stu-id="91ee5-173">The type of sensitive information that's detected has a match accuracy (or confidence level) of at least 75.</span></span> <span data-ttu-id="91ee5-174">De nombreux types d’informations sensibles sont définis avec plusieurs modèles. Un modèle définissant une précision de correspondance élevée impose davantage de critères (par exemple, mots clés, dates ou adresses) qu’un modèle définissant une précision de correspondance moindre.</span><span class="sxs-lookup"><span data-stu-id="91ee5-174">Many sensitive information types are defined with multiple patterns, where a pattern with a higher match accuracy requires more evidence to be found (such as keywords, dates, or addresses), while a pattern with a lower match accuracy requires less evidence.</span></span> <span data-ttu-id="91ee5-175">Plus la valeur de précision de correspondance **min** est faible, plus il y a de contenu correspondant à la condition.</span><span class="sxs-lookup"><span data-stu-id="91ee5-175">The lower the **min** match accuracy, the easier it is for content to match the condition.</span></span> 
    
<span data-ttu-id="91ee5-176">Pour plus d’informations relatives à ces options, voir[optimisation des règles afin de les rendre plus facile ou plus difficile à associer](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span><span class="sxs-lookup"><span data-stu-id="91ee5-176">For more information on these options, see [Tuning rules to make them easier or harder to match](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span></span>
    
![Options permettant d’identifier les types d’informations sensibles](../media/de255881-f596-4c8d-8359-e974e3a0819a.png)
  
#### <a name="auto-apply-labels-to-content-with-keywords-or-searchable-properties"></a><span data-ttu-id="91ee5-178">Application automatique d’étiquettes au contenu comprenant des mots clés ou des propriétés pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="91ee5-178">Auto-apply labels to content with keywords or searchable properties</span></span>

<span data-ttu-id="91ee5-p115">Vous pouvez appliquer automatiquement des étiquettes au contenu à l’aide d’une requête qui contient des mots, des phrases ou des valeurs de propriétés pouvant faire l’objet d’une recherche. Vous pouvez affiner votre requête en utilisant des opérateurs de recherche tels que et, ou et non.</span><span class="sxs-lookup"><span data-stu-id="91ee5-p115">You can auto-apply labels to content by using a query that contains specific words, phrases, or values of searchable properties. You can refine your query by using search operators such as AND, OR, and NOT.</span></span>

![Éditeur de requête](../media/ac5b8e5e-7453-4ec7-905c-160df57298d3.png)

<span data-ttu-id="91ee5-182">Pour plus d’informations sur la syntaxe de requête qui utilise le langage de requête de mot clé (KQL), consultez [Référence de syntaxe de langage de requête de mot clé (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference).</span><span class="sxs-lookup"><span data-stu-id="91ee5-182">For more information about the query syntax that uses Keyword Query Language (KQL), see [Keyword Query Language (KQL) syntax reference](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference).</span></span>

<span data-ttu-id="91ee5-183">Les étiquettes basées sur une requête utilisent l’index de recherche pour identifier le contenu.</span><span class="sxs-lookup"><span data-stu-id="91ee5-183">Query-based labels use the search index to identify content.</span></span> <span data-ttu-id="91ee5-184">Pour plus d’informations sur les propriétés pouvant faire l’objet d’une recherche, consultez :</span><span class="sxs-lookup"><span data-stu-id="91ee5-184">For more information about the searchable properties that you can use, see:</span></span>

- [<span data-ttu-id="91ee5-185">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="91ee5-185">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
- [<span data-ttu-id="91ee5-186">Vue d’ensemble des propriétés analysées et gérées dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="91ee5-186">Overview of crawled and managed properties in SharePoint Server</span></span>](https://docs.microsoft.com/SharePoint/technical-reference/crawled-and-managed-properties-overview)

> [!NOTE]
> <span data-ttu-id="91ee5-187">Bien que les propriétés gérées de SharePoint prennent en charge les alias, ne les utilisez pas lorsque vous configurez vos étiquettes de rétention.</span><span class="sxs-lookup"><span data-stu-id="91ee5-187">Although SharePoint managed properties support aliases, don't use these when you configure your retention labels.</span></span> <span data-ttu-id="91ee5-188">Spécifiez toujours le nom réel de la propriété gérée (par exemple, « RefinableString01 »).</span><span class="sxs-lookup"><span data-stu-id="91ee5-188">Always specify the actual name of the managed property, for example, "RefinableString01".</span></span>

<span data-ttu-id="91ee5-189">Exemples de requêtes :</span><span class="sxs-lookup"><span data-stu-id="91ee5-189">Examples queries:</span></span>

| <span data-ttu-id="91ee5-190">Charge de travail</span><span class="sxs-lookup"><span data-stu-id="91ee5-190">Workload</span></span> | <span data-ttu-id="91ee5-191">Exemple</span><span class="sxs-lookup"><span data-stu-id="91ee5-191">Example</span></span> |
|:-----|:-----|
|<span data-ttu-id="91ee5-192">Exchange</span><span class="sxs-lookup"><span data-stu-id="91ee5-192">Exchange</span></span>   | `subject:"Quarterly Financials"` |
|<span data-ttu-id="91ee5-193">Exchange</span><span class="sxs-lookup"><span data-stu-id="91ee5-193">Exchange</span></span>   | `recipients:garthf@contoso.com` |
|<span data-ttu-id="91ee5-194">SharePoint</span><span class="sxs-lookup"><span data-stu-id="91ee5-194">SharePoint</span></span> | `contenttype:contract` |
|<span data-ttu-id="91ee5-195">SharePoint</span><span class="sxs-lookup"><span data-stu-id="91ee5-195">SharePoint</span></span> | `site:https://contoso.sharepoint.com/sites/teams/procurement AND contenttype:contract`|

#### <a name="auto-apply-labels-to-content-by-using-trainable-classifiers"></a><span data-ttu-id="91ee5-196">Appliquer automatiquement des étiquettes au contenu à l’aide de classifieurs entraînables</span><span class="sxs-lookup"><span data-stu-id="91ee5-196">Auto-apply labels to content by using trainable classifiers</span></span>

<span data-ttu-id="91ee5-197">Lorsque vous choisissez l’option de classifieur entraînable, vous pouvez sélectionner un classifieur intégré ou un classifieur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="91ee5-197">When you choose the option for a trainable classifier, you can select one of the built-in classifiers, or a custom classifier.</span></span> <span data-ttu-id="91ee5-198">Les classifieurs intégrés incluent : **CV**, **SourceCode**, **Harcèlement ciblé**, **Blasphème** et la **Menace** :</span><span class="sxs-lookup"><span data-stu-id="91ee5-198">The built-in classifiers include **Resumes**, **SourceCode**, **Targeted Harassment**, **Profanity**, and **Threat**:</span></span>

![Sélectionnez un classificateur à entraîner](../media/retention-label-classifers.png)

> [!CAUTION]
> <span data-ttu-id="91ee5-200">Nous déprécions le **langage inconvenant** classifieur intégré, car il génère un grand nombre de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="91ee5-200">We are deprecating the **Offensive Language** built-in classifier because it has been producing a high number of false positives.</span></span> <span data-ttu-id="91ee5-201">N’utilisez pas ce classifieur intégré et si vous l’utilisez actuellement, vous devez déplacer vos processus métier.</span><span class="sxs-lookup"><span data-stu-id="91ee5-201">Don't use this built-in classifier and if you are currently using it, you should move your business processes off it.</span></span> <span data-ttu-id="91ee5-202">Nous vous recommandons d’utiliser les classifieurs intégrés de **Harcèlement ciblée** , de **blasphème** et de **Menace** à la place.</span><span class="sxs-lookup"><span data-stu-id="91ee5-202">We recommend using the **Targeted Harassment**, **Profanity**, and **Threat** built-in classifiers instead.</span></span>

<span data-ttu-id="91ee5-203">Pour appliquer automatiquement une étiquette à l’aide de cette option, les sites et boîtes aux lettres SharePoint Online doivent avoir au moins 10 Mo de données.</span><span class="sxs-lookup"><span data-stu-id="91ee5-203">To automatically apply a label by using this option, SharePoint Online sites and mailboxes must have at least 10 MB of data.</span></span>

<span data-ttu-id="91ee5-204">Pour plus d’informations sur les classifieurs entraînables, voir la [Prise en main des classifieurs entrainables (version d'évaluation)](classifier-getting-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="91ee5-204">For more information about trainable classifiers, see [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md).</span></span>

<span data-ttu-id="91ee5-205">Pour consulter un exemple de configuration, voir [Comment préparer et utiliser un classifieur prêt à l'emploi](classifier-using-a-ready-to-use-classifier.md#how-to-verify-that-a-built-in-classifier-will-meet-your-needs).</span><span class="sxs-lookup"><span data-stu-id="91ee5-205">For an example configuration, see [How to prepare for and use a built-in classifier](classifier-using-a-ready-to-use-classifier.md#how-to-verify-that-a-built-in-classifier-will-meet-your-needs).</span></span>

## <a name="how-long-it-takes-for-retention-labels-to-take-effect"></a><span data-ttu-id="91ee5-206">Délai d’activation des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="91ee5-206">How long it takes for retention labels to take effect</span></span>

<span data-ttu-id="91ee5-207">Lorsque vous appliquez automatiquement des étiquettes de rétention, l’application de ces étiquettes à ce contenu peut prendre jusqu’à sept jours.</span><span class="sxs-lookup"><span data-stu-id="91ee5-207">When you auto-apply retention labels, it can take up to seven days for the retention labels to be applied to all existing content that matches the conditions.</span></span>
  
![Diagramme indiquant quand les étiquettes d’application automatique prennent effet](../media/b8c00657-477a-4ade-b914-e643ef97a10d.png)
  
## <a name="updating-retention-labels-and-their-policies"></a><span data-ttu-id="91ee5-209">Mise à jour des étiquettes de rétention et de leurs stratégies</span><span class="sxs-lookup"><span data-stu-id="91ee5-209">Updating retention labels and their policies</span></span>

<span data-ttu-id="91ee5-210">Lorsque vous modifiez une étiquette de rétention ou une stratégie d’application automatique et que l’étiquette de rétention est déjà appliquée au contenu, vos paramètres mis à jour sont automatiquement appliqués à ce contenu, en plus du contenu nouvellement identifié.</span><span class="sxs-lookup"><span data-stu-id="91ee5-210">When you edit a retention label or auto-apply policy, and the retention label is already applied to content, your updated settings will automatically be applied to this content in addition to content that's newly identified.</span></span>

<span data-ttu-id="91ee5-211">Certains paramètres ne peuvent pas être modifiés une fois l’étiquette ou la stratégie créée et enregistrée, notamment :</span><span class="sxs-lookup"><span data-stu-id="91ee5-211">Some settings can't be changed after the label or policy is created and saved, which include:</span></span>
- <span data-ttu-id="91ee5-212">Paramètres de rétention à l’exception de la période de rétention, sauf si vous avez configuré l’étiquette pour conserver ou supprimer le contenu en fonction de sa date de création.</span><span class="sxs-lookup"><span data-stu-id="91ee5-212">The retention settings except the retention period, unless you've configured the label to retain or delete the content based on when it was created.</span></span>
- <span data-ttu-id="91ee5-213">Possibilité de classifier en tant qu’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="91ee5-213">The option to classify as a record.</span></span>

## <a name="next-steps"></a><span data-ttu-id="91ee5-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="91ee5-214">Next steps</span></span>

<span data-ttu-id="91ee5-215">Consultez [Utiliser les étiquettes de rétention pour gérer le cycle de vie des documents stockés dans SharePoint](auto-apply-retention-labels-scenario.md) pour un exemple de scénario qui utilise une stratégie d’application automatique avec des propriétés gérées dans SharePoint et la rétention basée sur les événements pour démarrer la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="91ee5-215">See [Use retention labels to manage the lifecycle of documents stored in SharePoint](auto-apply-retention-labels-scenario.md) for an example scenario that uses an auto-apply policy with managed properties in SharePoint, and event-based retention to start the retention period.</span></span>
