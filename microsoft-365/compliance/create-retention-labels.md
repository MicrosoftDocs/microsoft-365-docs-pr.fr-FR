---
title: Créer, publier ou appliquer automatiquement des étiquettes de rétention
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
description: Instructions pour créer, publier et appliquer automatiquement des étiquettes de rétention pour conserver les informations nécessaires, supprimer l’inutile et déclarer un élément en tant qu’enregistrement dans votre environnement Office 365.
ms.openlocfilehash: 65319baa0fd238ebdc403307fb8bb91a59d87cd6
ms.sourcegitcommit: 3cd487476efe4138d1b42499fbffbbe4bacfe5b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "44408466"
---
# <a name="create-publish-and-auto-apply-retention-labels"></a><span data-ttu-id="732e1-103">Créer, publier ou appliquer automatiquement des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="732e1-103">Create, publish, and auto-apply retention labels</span></span>

><span data-ttu-id="732e1-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="732e1-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="732e1-105">Utilisez les informations suivantes pour créer des [étiquettes de rétention](labels.md), puis appliquez-les automatiquement aux documents et e-mails, ou publiez-les afin que les utilisateurs puissent les appliquer manuellement.</span><span class="sxs-lookup"><span data-stu-id="732e1-105">Use the following information to help you create [retention labels](labels.md), and then automatically apply them to documents and emails, or publish them so that users can manually apply them.</span></span>

<span data-ttu-id="732e1-106">Les étiquettes de rétention vous permettent de conserver ce qui est nécessaire et de supprimer l’inutile.</span><span class="sxs-lookup"><span data-stu-id="732e1-106">Retention labels help you retain what you need and delete what you don't.</span></span> <span data-ttu-id="732e1-107">Elles s’utilisent également pour déclarer un élément en tant qu’enregistrement dans le cadre d’une [gestion des enregistrements](records-management.md) pour vos données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="732e1-107">They are also used to declare an item as a record as part of a [records management](records-management.md) solution for your Microsoft 365 data.</span></span>

<span data-ttu-id="732e1-108">L’emplacement dans lequel vous créez et configurez vos étiquettes de rétention dépend de votre utilisation ou non de la gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="732e1-108">Where you create and configure your retention labels depend on whether you're using records management or not.</span></span> <span data-ttu-id="732e1-109">Des instructions sont fournies pour les deux scénarios.</span><span class="sxs-lookup"><span data-stu-id="732e1-109">Instructions are provided for both scenarios.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="732e1-110">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="732e1-110">Before you begin</span></span>

<span data-ttu-id="732e1-111">Les membres de votre équipe de conformité appelés à créer des étiquettes de rétention ont besoin d’autorisations pour accéder au Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="732e1-111">Members of your compliance team who will create retention labels need permissions to the Security &amp; Compliance Center.</span></span> <span data-ttu-id="732e1-112">Par défaut, votre administrateur locataire a accès à cet emplacement et peut accorder l’accès aux responsables de la mise en conformité et à d’autres personnes du Centre de sécurité et de conformité, sans leur donner toutes les autorisations d’un administrateur locataire. Pour ce faire, nous vous recommandons d’accéder à la page **Autorisations** du Centre de sécurité et de conformité, de modifier le groupe de rôles **Administrateur de conformité** et d’ajouter des membres à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="732e1-112">By default, your tenant admin has access to this location and can give compliance officers and other people access to the Security &amp; Compliance Center, without giving them all of the permissions of a tenant admin. To do this, we recommend that you go to the **Permissions** page of the Security &amp; Compliance Center, edit the **Compliance Administrator** role group, and add members to that role group.</span></span> 
  
<span data-ttu-id="732e1-113">Pour obtenir plus d’informations, consultez l’article [Octroi de l’accès au Centre de sécurité &amp; conformité Office 365 aux utilisateurs](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="732e1-113">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span></span>
  
<span data-ttu-id="732e1-p104">Ces autorisations sont requises uniquement pour créer et appliquer des étiquettes de rétention et une stratégie d’étiquette. L’application d’une stratégie ne nécessite pas d’accès au contenu.</span><span class="sxs-lookup"><span data-stu-id="732e1-p104">These permissions are required only to create and apply retention labels and a label policy. Policy enforcement does not require access to the content.</span></span>

## <a name="create-and-configure-retention-labels"></a><span data-ttu-id="732e1-116">Créer et configurer des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="732e1-116">Create and configure retention labels</span></span>

1. <span data-ttu-id="732e1-117">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="732e1-117">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="732e1-118">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-118">If you are using records management:</span></span>
        - <span data-ttu-id="732e1-119">**Solutions** > **Gestion des enregistrements** > **Plan de fichiers** onglet > **+ Créer une étiquette** > **Étiquette de rétention**</span><span class="sxs-lookup"><span data-stu-id="732e1-119">**Solutions** > **Records management** > **File plan** tab > **+ Create a label** > **Retention label**</span></span>
        
    - <span data-ttu-id="732e1-120">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-120">If you are not using records management:</span></span>
       - <span data-ttu-id="732e1-121">**Solutions** > **Gouvernance d’informations** > **Étiquettes** onglet > + **Créer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="732e1-121">**Solutions** > **Information governance** > **Labels** tab > + **Create a label**</span></span>
    
    <span data-ttu-id="732e1-122">Votre option ne s’affiche pas immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="732e1-122">Don't immediately see your option?</span></span> <span data-ttu-id="732e1-123">Sélectionnez tout d’abord **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="732e1-123">First select **Show all**.</span></span> 

2. <span data-ttu-id="732e1-124">Suivez les invites de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="732e1-124">Follow the prompts in the wizard.</span></span> <span data-ttu-id="732e1-125">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-125">If you are using records management:</span></span>
    
    - <span data-ttu-id="732e1-126">Pour plus d’informations sur les descripteurs de plan de fichiers, voir [Présentation du gestionnaire de plans de fichiers](file-plan-manager.md)</span><span class="sxs-lookup"><span data-stu-id="732e1-126">For information about the file plan descriptors, see [Overview of file plan manager](file-plan-manager.md)</span></span>
    
    - <span data-ttu-id="732e1-127">Pour utiliser l’étiquette de rétention pour déclarer du contenu en tant qu’enregistrement, activez la case à cocher **Utiliser une étiquette pour classifier du contenu en tant qu’« enregistrement »**.</span><span class="sxs-lookup"><span data-stu-id="732e1-127">To use the retention label to declare content as a record, enable the checkbox **Use label to classify content as a "Record"**.</span></span>

3. <span data-ttu-id="732e1-128">Répétez ces étapes pour créer d’autres étiquettes.</span><span class="sxs-lookup"><span data-stu-id="732e1-128">Repeat these steps to create more labels.</span></span>

<span data-ttu-id="732e1-129">Pour modifier une étiquette existante, sélectionnez-la, puis choisissez **Modifier l'étiquette**.</span><span class="sxs-lookup"><span data-stu-id="732e1-129">To edit an existing label, select it, and then select **Edit label**.</span></span> <span data-ttu-id="732e1-130">Cette opération démarre le même Assistant, ce qui vous permet de modifier les descriptions et paramètres d’étiquette à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="732e1-130">This starts the same wizard, which lets you change the label descriptions and settings in step 2.</span></span>

## <a name="publish-retention-labels-by-creating-a-retention-label-policy"></a><span data-ttu-id="732e1-131">Publier des étiquettes de rétention en créant une stratégie de rétention d’étiquette</span><span class="sxs-lookup"><span data-stu-id="732e1-131">Publish retention labels by creating a retention label policy</span></span>

<span data-ttu-id="732e1-132">Publiez vos étiquettes de rétention pour que les utilisateurs puissent les appliquer manuellement.</span><span class="sxs-lookup"><span data-stu-id="732e1-132">Publish retention labels so that they can be manually applied by users.</span></span>

1. <span data-ttu-id="732e1-133">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="732e1-133">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="732e1-134">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-134">If you are using records management:</span></span>
        - <span data-ttu-id="732e1-135">**Solutions** > **Gestion des enregistrements** > > **Stratégies d’étiquette** onglet > **Publier des étiquettes**</span><span class="sxs-lookup"><span data-stu-id="732e1-135">**Solutions** > **Records management** > > **Label policies** tab > **Publish labels**</span></span>
    
    - <span data-ttu-id="732e1-136">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-136">If you are not using records management:</span></span>
        - <span data-ttu-id="732e1-137">**Solutions** > **Gouvernance d’informations** > **Stratégies d’étiquette** onglet > **Publier des étiquettes**</span><span class="sxs-lookup"><span data-stu-id="732e1-137">**Solutions** > **Information governance** > **Label policies** tab > **Publish labels**</span></span>
    
    <span data-ttu-id="732e1-138">Votre option ne s’affiche pas immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="732e1-138">Don't immediately see your option?</span></span> <span data-ttu-id="732e1-139">Sélectionnez tout d’abord **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="732e1-139">First select **Show all**.</span></span> 

2. <span data-ttu-id="732e1-140">Suivez les invites de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="732e1-140">Follow the prompts in the wizard.</span></span>
    
    <span data-ttu-id="732e1-141">Pour plus d’informations sur la prise en charge des emplacements par des étiquettes de rétention, voir la section [Étiquettes de rétention et emplacements](labels.md#retention-label-policies-and-locations).</span><span class="sxs-lookup"><span data-stu-id="732e1-141">For information about the locations supported by retention labels, see the [Retention labels and locations](labels.md#retention-label-policies-and-locations) section.</span></span> 

## <a name="auto-apply-a-retention-label"></a><span data-ttu-id="732e1-142">Étiquettes de rétention appliquées automatiquement</span><span class="sxs-lookup"><span data-stu-id="732e1-142">Auto-apply a retention label</span></span>

<span data-ttu-id="732e1-143">Appliquez automatiquement une étiquette de rétention, en fonction des conditions que vous indiquez.</span><span class="sxs-lookup"><span data-stu-id="732e1-143">Auto-apply a retention label, based on the conditions that you specify.</span></span>

1. <span data-ttu-id="732e1-144">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="732e1-144">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="732e1-145">Si vous utilisez la gestion des enregistrements : **Gouvernance d’informations** :</span><span class="sxs-lookup"><span data-stu-id="732e1-145">If you are using records management: **Information governance**:</span></span>
        - <span data-ttu-id="732e1-146">**Solutions** > **Gestion des enregistrements** > **Stratégies d’étiquette** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="732e1-146">**Solutions** > **Records management** > **Label policies** tab > **Auto-apply label**</span></span>
    
    - <span data-ttu-id="732e1-147">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="732e1-147">If you are not using records management:</span></span>
        - <span data-ttu-id="732e1-148">**Solutions** > **Gouvernance d’informations** > **Stratégies d’étiquette** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="732e1-148">**Solutions** > **Information governance** > **Label policies** tab > **Auto-apply label**</span></span>
    
    <span data-ttu-id="732e1-149">Votre option ne s’affiche pas immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="732e1-149">Don't immediately see your option?</span></span> <span data-ttu-id="732e1-150">Sélectionnez tout d’abord **Afficher tout**.</span><span class="sxs-lookup"><span data-stu-id="732e1-150">First select **Show all**.</span></span> 

2. <span data-ttu-id="732e1-151">Suivez les invites de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="732e1-151">Follow the prompts in the wizard.</span></span>
    
    <span data-ttu-id="732e1-152">Pour plus d’informations sur la configuration des conditions qui appliquent automatiquement l’étiquette de rétention, voir la section [Configuration des conditions d’application automatique des étiquettes de rétention](#configuring-conditions-for-auto-apply-retention-labels) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="732e1-152">For information about configuring the conditions that automatically apply the retention label, see the [Configuring conditions for auto-apply retention labels](#configuring-conditions-for-auto-apply-retention-labels) section on this page.</span></span>
    
    <span data-ttu-id="732e1-153">Pour plus d’informations sur la prise en charge des emplacements par des étiquettes de rétention, voir la section [Étiquettes de rétention et emplacements](labels.md#retention-label-policies-and-locations).</span><span class="sxs-lookup"><span data-stu-id="732e1-153">For information about the locations supported by retention labels, see the [Retention labels and locations](labels.md#retention-label-policies-and-locations) section.</span></span>


## <a name="configuring-conditions-for-auto-apply-retention-labels"></a><span data-ttu-id="732e1-154">Configuration des conditions d’application automatique des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="732e1-154">Configuring conditions for auto-apply retention labels</span></span>

<span data-ttu-id="732e1-155">Vous pouvez appliquer automatiquement des étiquettes de rétention au contenu quand celui-ci inclut :</span><span class="sxs-lookup"><span data-stu-id="732e1-155">You can apply retention labels to content automatically when that content contains:</span></span>
  
- [<span data-ttu-id="732e1-156">Types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="732e1-156">Specific types of sensitive information</span></span>](#auto-apply-labels-to-content-with-specific-types-of-sensitive-information)
    
- [<span data-ttu-id="732e1-157">Mots clés spécifiques correspondant à une requête que vous créez</span><span class="sxs-lookup"><span data-stu-id="732e1-157">Specific keywords that match a query you create</span></span>](#auto-apply-labels-to-content-with-keywords-or-searchable-properties)

- [<span data-ttu-id="732e1-158">Correspondance pour les classifieurs entraînables</span><span class="sxs-lookup"><span data-stu-id="732e1-158">A match for trainable classifiers</span></span>](#auto-apply-labels-to-content-by-using-trainable-classifiers)
    
![Page Choisir une condition pour l'application automatique de l’étiquette](../media/classifier-pre-trained-apply-label-match-trainable-classifier.png)

<span data-ttu-id="732e1-160">L’application automatique d'étiquettes de rétention à tout le contenu correspondant aux conditions que vous avez configurées peut prendre jusqu’à sept jours.</span><span class="sxs-lookup"><span data-stu-id="732e1-160">It can take up to seven days for auto-apply retention labels to be applied to all content that matches the conditions you've configured.</span></span>

### <a name="auto-apply-labels-to-content-with-specific-types-of-sensitive-information"></a><span data-ttu-id="732e1-161">Application automatique d’étiquettes au contenu incluant des types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="732e1-161">Auto-apply labels to content with specific types of sensitive information</span></span>

<span data-ttu-id="732e1-162">Lorsque vous créez des étiquettes de rétention d’application automatique pour des informations sensibles, vous voyez s’afficher la même liste de modèles de stratégie que lorsque vous créez une stratégie de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="732e1-162">When you create auto-apply retention labels for sensitive information, you see the same list of policy templates as when you create a data loss prevention (DLP) policy.</span></span> <span data-ttu-id="732e1-163">Chaque modèle de stratégie est préconfiguré pour rechercher des types spécifiques d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="732e1-163">Each policy template is preconfigured to look for specific types of sensitive information.</span></span> <span data-ttu-id="732e1-164">Par exemple, le modèle illustré ici recherche les numéros ITIN, SSN et de passeport américains.</span><span class="sxs-lookup"><span data-stu-id="732e1-164">For example, the template shown here looks for U.S. ITIN, SSN, and passport numbers.</span></span> <span data-ttu-id="732e1-165">Pour plus d’informations sur la protection contre la perte de données, voir [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="732e1-165">To learn more about DLP, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
![Modèles de stratégie avec des types d’informations sensibles](../media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)
  
<span data-ttu-id="732e1-p111">Après avoir sélectionné un modèle de stratégie, vous pouvez ajouter ou supprimer tout type d’informations sensibles, et vous pouvez modifier le nombre d’instances et la précision de correspondance. Dans l’exemple présenté ici, une étiquette de rétention sera appliquée automatiquement uniquement dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="732e1-p111">After you select a policy template, you can add or remove any types of sensitive information, and you can change the instance count and match accuracy. In the example shown here, a retention label will be auto-applied only when:</span></span>
  
- <span data-ttu-id="732e1-p112">Le contenu comprend entre 1 et 9 instances de l’un de ces trois types d’informations sensibles. Vous pouvez supprimer la valeur **max** pour la définir sur **any**.</span><span class="sxs-lookup"><span data-stu-id="732e1-p112">The content contains between 1 and 9 instances of any of these three sensitive information types. You can delete the **max** value so that it changes to **any**.</span></span>
    
- <span data-ttu-id="732e1-p113">Le type d’informations sensibles détecté a une précision de correspondance (ou niveau de confiance) minimale de 75. De nombreux types d’informations sensibles sont définis avec plusieurs modèles. Tandis qu’un modèle avec une précision de correspondance plus élevée nécessite un nombre de preuves plus important (par exemple, des mots clés, des dates ou des adresses), un modèle avec une précision de correspondance inférieure nécessite moins de preuves. En d’autres termes, plus la précision de correspondance **min** est faible, plus il est facile de faire correspondre le contenu à la condition.</span><span class="sxs-lookup"><span data-stu-id="732e1-p113">The type of sensitive information that's detected has a match accuracy (or confidence level) of at least 75. Many sensitive information types are defined with multiple patterns, where a pattern with a higher match accuracy requires more evidence to be found (such as keywords, dates, or addresses), while a pattern with a lower match accuracy requires less evidence. Simply put, the lower the **min** match accuracy, the easier it is for content to match the condition.</span></span> 
    
<span data-ttu-id="732e1-174">Pour plus d’informations relatives à ces options, voir[optimisation des règles afin de les rendre plus facile ou plus difficile à associer](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span><span class="sxs-lookup"><span data-stu-id="732e1-174">For more information on these options, see [Tuning rules to make them easier or harder to match](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span></span>
    
![Options permettant d’identifier les types d’informations sensibles](../media/de255881-f596-4c8d-8359-e974e3a0819a.png)
  
### <a name="auto-apply-labels-to-content-with-keywords-or-searchable-properties"></a><span data-ttu-id="732e1-176">Application automatique d’étiquettes au contenu comprenant des mots clés ou des propriétés pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="732e1-176">Auto-apply labels to content with keywords or searchable properties</span></span>

<span data-ttu-id="732e1-p114">Vous pouvez appliquer automatiquement des étiquettes au contenu remplissant certaines conditions. Les conditions actuellement disponibles prennent en charge l’application d’une étiquette au contenu comprenant des mots, des phrases spécifiques ou des valeurs de propriété pouvant faire l’objet d’une recherche. Vous pouvez affiner votre requête à l’aide des opérateurs de recherche tels que AND, OR et NOT.</span><span class="sxs-lookup"><span data-stu-id="732e1-p114">You can auto-apply labels to content that satisfies certain conditions. The conditions now available support applying a label to content that contains specific words, phrases, or values of searchable properties. You can refine your query by using search operators like AND, OR, and NOT.</span></span>

<span data-ttu-id="732e1-180">Pour obtenir plus d’informations sur la syntaxe de requête, consultez l’article suivant :</span><span class="sxs-lookup"><span data-stu-id="732e1-180">For more information on query syntax, see:</span></span>

- [<span data-ttu-id="732e1-181">Référence de syntaxe de langage de requête de mot clé (KQL)</span><span class="sxs-lookup"><span data-stu-id="732e1-181">Keyword Query Language (KQL) syntax reference</span></span>](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference)

<span data-ttu-id="732e1-p115">Les étiquettes basées sur une requête utilisent l’index de recherche pour identifier le contenu. Pour plus d’informations sur les propriétés valides utilisables dans une requête, consultez l’article suivant :</span><span class="sxs-lookup"><span data-stu-id="732e1-p115">Query-based labels use the search index to identify content. For more information on valid searchable properties, see:</span></span>

- [<span data-ttu-id="732e1-184">Requêtes par mots clés et conditions de recherche pour la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="732e1-184">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
- [<span data-ttu-id="732e1-185">Vue d’ensemble des propriétés analysées et gérées dans SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="732e1-185">Overview of crawled and managed properties in SharePoint Server</span></span>](https://docs.microsoft.com/SharePoint/technical-reference/crawled-and-managed-properties-overview)

<span data-ttu-id="732e1-186">Exemples de requêtes :</span><span class="sxs-lookup"><span data-stu-id="732e1-186">Examples queries:</span></span>

- <span data-ttu-id="732e1-187">Exchange</span><span class="sxs-lookup"><span data-stu-id="732e1-187">Exchange</span></span>
    - <span data-ttu-id="732e1-188">subject:"Quarterly Financials"</span><span class="sxs-lookup"><span data-stu-id="732e1-188">subject:"Quarterly Financials"</span></span>
    - <span data-ttu-id="732e1-189">recipients:garthf</span><span class="sxs-lookup"><span data-stu-id="732e1-189">recipients:garthf</span></span><!--nolink--><span data-ttu-id="732e1-190">@contoso.com</span><span class="sxs-lookup"><span data-stu-id="732e1-190">@contoso.com</span></span>
- <span data-ttu-id="732e1-191">SharePoint et OneDrive</span><span class="sxs-lookup"><span data-stu-id="732e1-191">SharePoint and OneDrive</span></span>
    - <span data-ttu-id="732e1-192">contenttype:contract</span><span class="sxs-lookup"><span data-stu-id="732e1-192">contenttype:contract</span></span>
    - <span data-ttu-id="732e1-193">site:https</span><span class="sxs-lookup"><span data-stu-id="732e1-193">site:https</span></span><!--nolink--><span data-ttu-id="732e1-194">://contoso.sharepoint.com/sites/teams/procurement AND contenttype:contract</span><span class="sxs-lookup"><span data-stu-id="732e1-194">://contoso.sharepoint.com/sites/teams/procurement AND contenttype:contract</span></span>

![Éditeur de requête](../media/ac5b8e5e-7453-4ec7-905c-160df57298d3.png)


### <a name="auto-apply-labels-to-content-by-using-trainable-classifiers"></a><span data-ttu-id="732e1-196">Appliquer automatiquement des étiquettes au contenu à l’aide de classifieurs entraînables</span><span class="sxs-lookup"><span data-stu-id="732e1-196">Auto-apply labels to content by using trainable classifiers</span></span>

<span data-ttu-id="732e1-197">Lorsque vous choisissez l’option de classifieur entraînable, vous pouvez sélectionner un classifieur intégré ou un classifieur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="732e1-197">When you choose the option for a trainable classifier, you can select one of the built-in classifiers, or a custom classifier.</span></span> <span data-ttu-id="732e1-198">Les classifieurs intégrés incluent : **CV**, **SourceCode**, **Harcèlement ciblé**, **Blasphème** et la **Menace** :</span><span class="sxs-lookup"><span data-stu-id="732e1-198">The built-in classifiers include **Resumes**, **SourceCode**, **Targeted Harassment**, **Profanity**, and **Threat**:</span></span>

![Sélectionnez un classificateur à entraîner](../media/retention-label-classifers.png)

<span data-ttu-id="732e1-200">Pour appliquer automatiquement une étiquette à l’aide de cette option, les sites et boîtes aux lettres SharePoint Online doivent avoir au moins 10 Mo de données.</span><span class="sxs-lookup"><span data-stu-id="732e1-200">To automatically apply a label by using this option, SharePoint Online sites and mailboxes must have at least 10 MB of data.</span></span>

<span data-ttu-id="732e1-201">Pour plus d’informations sur les classifieurs entraînables, voir la [Prise en main des classifieurs entrainables (version d'évaluation)](classifier-getting-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="732e1-201">For more information about trainable classifiers, see [Getting started with trainable classifiers (preview)](classifier-getting-started-with.md).</span></span>

<span data-ttu-id="732e1-202">Pour consulter un exemple de configuration, voir [Comment préparer et utiliser un classifieur prêt à l'emploi](classifier-using-a-ready-to-use-classifier.md#how-to-verify-that-a-built-in-classifier-will-meet-your-needs).</span><span class="sxs-lookup"><span data-stu-id="732e1-202">For an example configuration, see [How to prepare for and use a built-in classifier](classifier-using-a-ready-to-use-classifier.md#how-to-verify-that-a-built-in-classifier-will-meet-your-needs).</span></span>

## <a name="how-long-it-takes-for-retention-labels-to-take-effect"></a><span data-ttu-id="732e1-203">Délai d’activation des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="732e1-203">How long it takes for retention labels to take effect</span></span>

<span data-ttu-id="732e1-204">Lorsque vous publiez ou appliquez automatiquement des étiquettes de rétention, elles ne prennent pas effet immédiatement :</span><span class="sxs-lookup"><span data-stu-id="732e1-204">When you publish or auto-apply retention labels, they don't take effect immediately:</span></span>
  
1. <span data-ttu-id="732e1-205">La première étape consiste à accéder au centre d’administration pour synchroniser la stratégie d’étiquette avec les emplacements définis dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="732e1-205">First the label policy needs to be synced from the admin center to the locations in the policy.</span></span>
    
2. <span data-ttu-id="732e1-206">Ensuite, selon l’emplacement, un certain temps pourra s’écouler avant que des étiquettes de rétention soient rendues disponibles aux utilisateurs finaux ou que des étiquettes d’application automatique soient attribuées à du contenu.</span><span class="sxs-lookup"><span data-stu-id="732e1-206">Then the location might require time to make published retention labels available to end users or time to auto-apply labels to content.</span></span> <span data-ttu-id="732e1-207">Le temps nécessaire dépend de l’emplacement et du type d’étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="732e1-207">How long this takes depends on the location and type of retention label.</span></span>
    
### <a name="published-retention-labels"></a><span data-ttu-id="732e1-208">Étiquettes de rétention publiées</span><span class="sxs-lookup"><span data-stu-id="732e1-208">Published retention labels</span></span>

<span data-ttu-id="732e1-p118">Si vous publiez des étiquettes de rétention sur SharePoint ou OneDrive, cela peut prendre un jour pour que ces étiquettes soient visibles pour les utilisateurs finals. De plus, si vous publiez des étiquettes de rétention sur Exchange, cela peut prendre 7 jours pour que ces étiquettes soient visibles pour les utilisateurs finals, et la boîte aux lettres doit contenir au moins 10 Mo de données.</span><span class="sxs-lookup"><span data-stu-id="732e1-p118">If you publish retention labels to SharePoint or OneDrive, it can take one day for those retention labels to appear for end users. In addition, if you publish retention labels to Exchange, it can take 7 days for those retention labels to appear for end users, and the mailbox needs to contain at least 10 MB of data.</span></span>
  
![Diagramme de la date d’effet des étiquettes manuelles](../media/b19f3a10-f625-45bf-9a53-dd14df02ae7c.png)
  
### <a name="auto-apply-retention-labels"></a><span data-ttu-id="732e1-212">Étiquettes de rétention appliquées automatiquement</span><span class="sxs-lookup"><span data-stu-id="732e1-212">Auto-apply retention labels</span></span>

<span data-ttu-id="732e1-213">Si vous appliquez automatiquement des étiquettes de rétention à du contenu remplissant des critères spécifiques, l’application de ces étiquettes à ce contenu peut prendre jusqu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="732e1-213">If you auto-apply retention labels to content matching specific conditions, it can take seven days for the retention labels to be applied to all existing content that matches the conditions.</span></span>
  
![Diagramme indiquant quand les étiquettes d’application automatique prennent effet](../media/b8c00657-477a-4ade-b914-e643ef97a10d.png)
  
### <a name="how-to-check-on-the-status-of-retention-labels-published-to-exchange"></a><span data-ttu-id="732e1-215">Vérifier l’état des étiquettes de rétention publiées dans Exchange</span><span class="sxs-lookup"><span data-stu-id="732e1-215">How to check on the status of retention labels published to Exchange</span></span>

<span data-ttu-id="732e1-216">Dans Exchange Online, les étiquettes de rétention deviennent disponibles pour les utilisateurs finaux à l’issue d’un processus qui s’exécute tous les sept jours.</span><span class="sxs-lookup"><span data-stu-id="732e1-216">In Exchange Online, retention labels are made available to end users by a process that runs every seven days.</span></span> <span data-ttu-id="732e1-217">Powershell vous permet de voir quand ce processus a été exécuté pour la dernière fois et définit donc la période de sa prochaine exécution.</span><span class="sxs-lookup"><span data-stu-id="732e1-217">By using Powershell, you can see when this process last ran and therefore identify when it will run again.</span></span>
  
1. <span data-ttu-id="732e1-218">[Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=799773).</span><span class="sxs-lookup"><span data-stu-id="732e1-218">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=799773).</span></span>
    
2. <span data-ttu-id="732e1-219">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="732e1-219">Run these commands.</span></span>
    
   ```powershell
   $logProps = Export-MailboxDiagnosticLogs <user> -ExtendedProperties
   ```

   ```powershell
   $xmlprops = [xml]($logProps.MailboxLog)
   ```

   ```powershell
   $xmlprops.Properties.MailboxTable.Property | ? {$_.Name -like "ELC*"}
   ```

<span data-ttu-id="732e1-220">Dans les résultats, la propriété `ELCLastSuccessTimeStamp` (UTC) indique quand le système a traité votre boîte aux lettres pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="732e1-220">In the results, the `ELCLastSuccessTimeStamp` (UTC) property shows when the system last processed your mailbox.</span></span> <span data-ttu-id="732e1-221">Si cela ne s’est pas produit depuis la création de la stratégie, les étiquettes ne s’affichent pas.</span><span class="sxs-lookup"><span data-stu-id="732e1-221">If it has not happened since the time you created the policy, the labels are not going to appear.</span></span> <span data-ttu-id="732e1-222">Pour forcer le traitement, exécutez la commande `Start-ManagedFolderAssistant -Identity <user>`.</span><span class="sxs-lookup"><span data-stu-id="732e1-222">To force processing, run  `Start-ManagedFolderAssistant -Identity <user>`.</span></span>
    
<span data-ttu-id="732e1-223">Si les étiquettes n’apparaissent pas dans Outlook sur le web comme prévu, veillez à vider le cache dans votre navigateur (CTRL + F5).</span><span class="sxs-lookup"><span data-stu-id="732e1-223">If labels aren't appearing in Outlook on the web and you think they should be, make sure to clear the cache in your browser (CTRL+F5).</span></span>
    

## <a name="updating-retention-labels-and-their-policies"></a><span data-ttu-id="732e1-224">Mise à jour des étiquettes de rétention et de leurs stratégies</span><span class="sxs-lookup"><span data-stu-id="732e1-224">Updating retention labels and their policies</span></span>

<span data-ttu-id="732e1-225">Si vous modifiez une étiquette de rétention, une stratégie d’étiquette de rétention ou une stratégie d’application automatique et que l’étiquette de rétention est déjà appliquée au contenu, vos paramètres mis à jour sont automatiquement appliqués à ce contenu, en plus du contenu nouvellement étiqueté.</span><span class="sxs-lookup"><span data-stu-id="732e1-225">If you edit a retention label, retention label policy, or auto-apply policy and the retention label is already applied to content, your updated settings will automatically be applied to this content in addition to content that's newly labeled.</span></span>

## <a name="find-the-powershell-cmdlets-for-retention-labels"></a><span data-ttu-id="732e1-226">Rechercher les cmdlets PowerShell pour les étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="732e1-226">Find the PowerShell cmdlets for retention labels</span></span>

<span data-ttu-id="732e1-227">Pour utiliser les cmdlets des étiquettes de conservation :</span><span class="sxs-lookup"><span data-stu-id="732e1-227">To use the retention label cmdlets:</span></span>
  
1. [<span data-ttu-id="732e1-228">Connexion au Centre de sécurité et de conformité Office 365 PowerShell</span><span class="sxs-lookup"><span data-stu-id="732e1-228">Connect to the Office 365 Security & Compliance Center Powershell</span></span>](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell)
    
2. <span data-ttu-id="732e1-229">Utilisez les cmdlets ci-après du Centre de sécurité et de conformité Office 365 :</span><span class="sxs-lookup"><span data-stu-id="732e1-229">Use these Office 365 Security & Compliance Center cmdlets:</span></span>
    
    - [<span data-ttu-id="732e1-230">Get-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="732e1-230">Get-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancetag)
    
    - [<span data-ttu-id="732e1-231">New-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="732e1-231">New-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-compliancetag)
    
    - [<span data-ttu-id="732e1-232">Remove-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="732e1-232">Remove-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-compliancetag)
    
    - [<span data-ttu-id="732e1-233">Set-ComplianceTag</span><span class="sxs-lookup"><span data-stu-id="732e1-233">Set-ComplianceTag</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-compliancetag)
    
    - [<span data-ttu-id="732e1-234">Enable-ComplianceTagStorage</span><span class="sxs-lookup"><span data-stu-id="732e1-234">Enable-ComplianceTagStorage</span></span>](https://docs.microsoft.com/powershell/module/exchange/enable-compliancetagstorage)
    
    - [<span data-ttu-id="732e1-235">Get-ComplianceTagStorage</span><span class="sxs-lookup"><span data-stu-id="732e1-235">Get-ComplianceTagStorage</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-compliancetagstorage)
    
    - [<span data-ttu-id="732e1-236">Get-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="732e1-236">Get-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy)
    
    - [<span data-ttu-id="732e1-237">New-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="732e1-237">New-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-retentioncompliancepolicy)
    
    - [<span data-ttu-id="732e1-238">Remove-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="732e1-238">Remove-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-retentioncompliancepolicy)
    
    - [<span data-ttu-id="732e1-239">Set-RetentionCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="732e1-239">Set-RetentionCompliancePolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy)
    
    - [<span data-ttu-id="732e1-240">Get-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="732e1-240">Get-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancerule)
    
    - [<span data-ttu-id="732e1-241">New-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="732e1-241">New-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-retentioncompliancerule)
    
    - [<span data-ttu-id="732e1-242">Remove-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="732e1-242">Remove-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/remove-retentioncompliancerule)
    
    - [<span data-ttu-id="732e1-243">Set-RetentionComplianceRule</span><span class="sxs-lookup"><span data-stu-id="732e1-243">Set-RetentionComplianceRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancerule)
