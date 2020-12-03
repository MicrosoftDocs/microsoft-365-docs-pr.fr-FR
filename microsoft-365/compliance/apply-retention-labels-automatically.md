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
description: Créez des étiquettes de rétention et des stratégies d’étiquetage automatique afin de pouvoir appliquer les étiquettes de manière automatique pour conserver les éléments utiles et supprimer les éléments inutiles.
ms.openlocfilehash: 766106e9c650047e37c9fa341bd2e78b390d814d
ms.sourcegitcommit: d3ca8021f7da00a474ac14aac5f1358204a848f2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/01/2020
ms.locfileid: "49519452"
---
# <a name="automatically-apply-a-retention-label-to-retain-or-delete-content"></a><span data-ttu-id="a7f7c-103">Application automatique d’une étiquette de rétention pour conserver ou supprimer du contenu</span><span class="sxs-lookup"><span data-stu-id="a7f7c-103">Automatically apply a retention label to retain or delete content</span></span>

><span data-ttu-id="a7f7c-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="a7f7c-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

> [!NOTE]
> <span data-ttu-id="a7f7c-105">Ce scénario n’est pas pris en charge pour les [enregistrements réglementaires](records-management.md#records).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-105">This scenario is not supported for [regulatory records](records-management.md#records).</span></span>

<span data-ttu-id="a7f7c-p101">L’une des fonctionnalités les plus puissantes des [étiquettes de rétention](retention.md) est la possibilité de les appliquer automatiquement au contenu qui remplit certaines conditions. Dans ce cas, les membres de votre organisation n’ont pas besoin d’appliquer les étiquettes de rétention. Microsoft 365 s’en charge à leur place.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p101">One of the most powerful features of [retention labels](retention.md) is the ability to apply them automatically to content that matches specified conditions. In this case, people in your organization don't need to apply the retention labels. Microsoft 365 does the work for them.</span></span>
  
<span data-ttu-id="a7f7c-109">Les étiquettes de rétention appliquées automatiquement sont puissantes pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-109">Auto-applying retention labels are powerful because:</span></span>
  
- <span data-ttu-id="a7f7c-110">Vous n’avez pas besoin de former les utilisateurs concernant l’ensemble de vos classifications.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-110">You don't need to train your users on all of your classifications.</span></span>
    
- <span data-ttu-id="a7f7c-111">Vous n’avez pas à dépendre des utilisateurs pour classer tout le contenu correctement.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-111">You don't need to rely on users to classify all content correctly.</span></span>
    
- <span data-ttu-id="a7f7c-112">Les utilisateurs n’ont plus besoin de connaître les stratégies de gouvernance des données : ils peuvent se concentrer sur leur travail.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-112">Users no longer need to know about data governance policies - they can focus on their work.</span></span>
    
<span data-ttu-id="a7f7c-113">Vous pouvez appliquer automatiquement des étiquettes de rétention à du contenu lorsque celui-ci contient des informations sensibles, des mots clés, des propriétés pouvant faire l’objet d’une recherche ou une correspondance pour des [classifieurs pouvant être formés](classifier-get-started-with.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-113">You can apply retention labels to content automatically when that content contains sensitive information, keywords or searchable properties, or a match for [trainable classifiers](classifier-get-started-with.md).</span></span>

> [!TIP]
> <span data-ttu-id="a7f7c-114">A présent dans l’aperçu, utiliser les propriétés de recherche pour identifier [Les enregistrements de réunion Teams](#microsoft-teams-meeting-recordings).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-114">Now in preview, use searchable properties to identify [Teams meeting recordings](#microsoft-teams-meeting-recordings).</span></span>

<span data-ttu-id="a7f7c-115">Les processus d’application automatique d’une étiquette de rétention sont fonction des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-115">The processes to automatically apply a retention label based on these conditions:</span></span>

![Diagramme des rôles et des tâches pour les étiquettes à appliquer automatiquement](../media/32f2f2fd-18a8-43fd-839d-72ad7a43e069.png)

<span data-ttu-id="a7f7c-117">Utilisez les instructions suivantes pour les deux étapes d’administration.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-117">Use the following instructions for the two admin steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a7f7c-p102">Les polices automatiques utilisent l'étiquetage côté service avec des conditions pour appliquer automatiquement des étiquettes de conservation. Vous pouvez également appliquer automatiquement un label de conservation avec une politique d'étiquetage lorsque vous faites ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p102">Auto-policies use service-side labeling with conditions to automatically apply retention labels. You can also automatically apply a retention label with a label policy when you do the following:</span></span> 
>
> - <span data-ttu-id="a7f7c-120">Appliquer un label de conservation par défaut pour sharePoint et Outlook, de sorte que les contenus non étiquetés soient automatiquement étiquetés</span><span class="sxs-lookup"><span data-stu-id="a7f7c-120">Apply a default retention label for SharePoint and Outlook, so that unlabeled content is automatically labeled</span></span>
>- <span data-ttu-id="a7f7c-121">Appliquer automatiquement un label de conservation au e-mail en utilisant des règles</span><span class="sxs-lookup"><span data-stu-id="a7f7c-121">Automatically applying a retention label to email by using rules</span></span>
>
> <span data-ttu-id="a7f7c-122">Pour ces scénarios, voir [Créer des étiquettes de rétention et les appliquer dans les applications](create-apply-retention-labels.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-122">For these scenarios, see [Create and apply retention labels in apps](create-apply-retention-labels.md).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a7f7c-123">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="a7f7c-123">Before you begin</span></span>

<span data-ttu-id="a7f7c-p103">L’administrateur général de votre organisation dispose de toutes les autorisations pour créer et modifier les étiquettes de rétention ainsi que leurs stratégies. Si vous ne vous connectez pas en tant qu’administrateur général, consultez [Autorisations nécessaires pour créer et gérer des stratégies et des étiquettes de rétention](get-started-with-retention.md#permissions-required-to-create-and-manage-retention-policies-and-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p103">The global admin for your organization has full permissions to create and edit retention labels and their policies. If you aren't signing in as a global admin, see [Permissions required to create and manage retention policies and retention labels](get-started-with-retention.md#permissions-required-to-create-and-manage-retention-policies-and-retention-labels).</span></span>

## <a name="how-to-auto-apply-a-retention-label"></a><span data-ttu-id="a7f7c-126">Application automatique d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="a7f7c-126">How to auto-apply a retention label</span></span>

<span data-ttu-id="a7f7c-p104">Tout d’abord, créez votre étiquette de rétention. Puis créez une stratégie automatique pour appliquer cette étiquette. Si vous avez déjà créé votre étiquette de rétention, passez à [création d’une stratégie automatique](#step-2-create-an-auto-apply-policy).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p104">First, create your retention label. Then create an auto-policy to apply that label. If you have already created your retention label, skip to [creating an auto-policy](#step-2-create-an-auto-apply-policy).</span></span>

<span data-ttu-id="a7f7c-p105">Les instructions de navigation varient selon que vous utilisez la [gestion des enregistrements](records-management.md) ou non. Il existe des instructions pour les deux scénarios. </span><span class="sxs-lookup"><span data-stu-id="a7f7c-p105">Navigation instructions depend on whether you're using [records management](records-management.md) or not. Instructions are provided for both scenarios.</span></span>

### <a name="step-1-create-a-retention-label"></a><span data-ttu-id="a7f7c-132">Étape 1 : créer une étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="a7f7c-132">Step 1: Create a retention label</span></span>

1. <span data-ttu-id="a7f7c-133">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-133">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="a7f7c-134">Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-134">If you are using records management:</span></span>
        - <span data-ttu-id="a7f7c-135">**Solutions** > **Gestion des enregistrements** > **Plan de fichiers** onglet > **+ Créer une étiquette** > **Étiquette de rétention**</span><span class="sxs-lookup"><span data-stu-id="a7f7c-135">**Solutions** > **Records management** > **File plan** tab > **+ Create a label** > **Retention label**</span></span>
        
    - <span data-ttu-id="a7f7c-136">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-136">If you are not using records management:</span></span>
       - <span data-ttu-id="a7f7c-137">**Solutions** > **Gouvernance d’informations** > **Étiquettes** onglet > + **Créer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="a7f7c-137">**Solutions** > **Information governance** > **Labels** tab > + **Create a label**</span></span>
    
    <span data-ttu-id="a7f7c-p106">Si vous ne voyez pas immédiatement votre option, sélectionnez d’abord **Tout afficher**.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p106">Don't immediately see your option? First select **Show all**.</span></span> 

2. <span data-ttu-id="a7f7c-p107">Suivez les invites de l’Assistant. Si vous utilisez la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p107">Follow the prompts in the wizard. If you are using records management:</span></span>
    
    - <span data-ttu-id="a7f7c-142">Pour plus d’informations sur les descripteurs de plan de fichier, consultez [Utiliser le plan de gestion des fichiers pour gérer les étiquettes de rétention](file-plan-manager.md)</span><span class="sxs-lookup"><span data-stu-id="a7f7c-142">For information about the file plan descriptors, see [Use file plan to manage retention labels](file-plan-manager.md)</span></span>
    
    - <span data-ttu-id="a7f7c-p108">Pour utiliser l’étiquette de rétention pour déclarer des enregistrements, sélectionnez **Marquer les éléments comme enregistrements**, ou **Marquer les éléments comme enregistrements réglementaires**. Pour plus d’informations, consultez [Configuration des étiquettes de rétention pour déclarer les enregistrements](declare-records.md#configuring-retention-labels-to-declare-records)</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p108">To use the retention label to declare records, select **Mark items as records**, or **Mark items as regulatory records**. For more information, see [Configuring retention labels to declare records](declare-records.md#configuring-retention-labels-to-declare-records).</span></span>

3. <span data-ttu-id="a7f7c-145">Une fois l’étiquette créée, les options permettant de la publier s’affichent. Appliquez automatiquement l’étiquette, ou enregistrez-la simplement : sélectionnez **Appliquer automatiquement cette étiquette à un type spécifique de contenu**, puis sélectionnez **Terminé** pour démarrer l’assistant à la création d’attribution automatique d’étiquettes qui vous conduit directement à l’étape 2 de la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-145">After you have created the label and you see the options to publish the label, auto-apply the label, or just save the label: Select **Auto-apply this label to a specific type of content**, and then select **Done** to start the Create auto-labeling wizard that takes you directly to step 2 in the following procedure.</span></span>

<span data-ttu-id="a7f7c-146">Pour modifier une étiquette existante, sélectionnez-la, puis sélectionnez **Modifier l’étiquette** pour démarrer l’assistant à l’édition de rétention qui vous permet de modifier les descriptions d’étiquettes et les [paramètres éligibles](#updating-retention-labels-and-their-policies) à partir de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-146">To edit an existing label, select it, and then select the **Edit label** option to start the Edit retention wizard that lets you change the label descriptions and any [eligible settings](#updating-retention-labels-and-their-policies) from step 2.</span></span>

### <a name="step-2-create-an-auto-apply-policy"></a><span data-ttu-id="a7f7c-147">Étape 2 : créer une stratégie d’application automatique</span><span class="sxs-lookup"><span data-stu-id="a7f7c-147">Step 2: Create an auto-apply policy</span></span>

<span data-ttu-id="a7f7c-148">Lorsque vous créez une stratégie d’application automatique, vous sélectionnez une étiquette de rétention pour l’appliquer automatiquement à du contenu, en fonction des conditions spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-148">When you create an auto-apply policy, you select a retention label to automatically apply to content, based on the conditions that you specify.</span></span>

1. <span data-ttu-id="a7f7c-149">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com/), accédez à l’un des emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-149">In the [Microsoft 365 compliance center](https://compliance.microsoft.com/), navigate to one of the following locations:</span></span>
    
    - <span data-ttu-id="a7f7c-150">Si vous utilisez la gestion des enregistrements : **Gouvernance d’informations** :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-150">If you are using records management: **Information governance**:</span></span>
        - <span data-ttu-id="a7f7c-151">**Solutions** > **Gestion des enregistrements** > **Stratégies des étiquettes** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="a7f7c-151">**Solutions** > **Records management** > **Label policies** tab > **Auto-apply a label**</span></span>
    
    - <span data-ttu-id="a7f7c-152">Si vous n’utilisez pas la gestion des enregistrements :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-152">If you are not using records management:</span></span>
        - <span data-ttu-id="a7f7c-153">**Solutions** > **Gouvernance d’informations** > **Stratégies des étiquettes** onglet > **Auto-appliquer une étiquette**</span><span class="sxs-lookup"><span data-stu-id="a7f7c-153">**Solutions** > **Information governance** > **Label policies** tab > **Auto-apply a label**</span></span>
    
    <span data-ttu-id="a7f7c-p109">Si vous ne voyez pas immédiatement votre option, sélectionnez d’abord **Tout afficher**.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p109">Don't immediately see your option? First select **Show all**.</span></span> 

2. <span data-ttu-id="a7f7c-156">Suivez les invites de l’assistant à la création d’attribution automatique d’étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-156">Follow the prompts in the Create auto-labeling wizard.</span></span>
    
    <span data-ttu-id="a7f7c-157">Pour plus d’informations sur la configuration des conditions qui appliquent automatiquement l’étiquette de rétention, voir la section [Configuration des conditions d’application automatique des étiquettes de rétention](#configuring-conditions-for-auto-apply-retention-labels) sur cette page.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-157">For information about configuring the conditions that automatically apply the retention label, see the [Configuring conditions for auto-apply retention labels](#configuring-conditions-for-auto-apply-retention-labels) section on this page.</span></span>
    
    <span data-ttu-id="a7f7c-158">Pour plus d’informations sur la prise en charge des emplacements par des étiquettes de rétention, voir la section [Étiquettes de rétention et emplacements](retention.md#retention-label-policies-and-locations).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-158">For information about the locations supported by retention labels, see the [Retention labels and locations](retention.md#retention-label-policies-and-locations) section.</span></span>

<span data-ttu-id="a7f7c-159">Pour modifier une politique d'application automatique existante, sélectionnez-la pour lancer l'assistant Modifier la politique de conservation qui vous permet de modifier l'étiquette de conservation sélectionnée et tous[les paramètres admissibles](#updating-retention-labels-and-their-policies)à partir de l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-159">To edit an existing auto-apply policy, select it to start the Edit retention policy wizard that lets you change the selected retention label and any [eligible settings](#updating-retention-labels-and-their-policies) from step 2.</span></span>

<span data-ttu-id="a7f7c-160">Une fois que le contenu est étiqueté au moyen d'une politique d'étiquetage automatique, l'étiquette appliquée ne peut pas être automatiquement retirée ou modifiée en changeant le contenu ou la politique, ou par une nouvelle politique d'étiquetage automatique.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-160">After content is labeled by using an auto-apply label policy, the applied label can't be automatically removed or changed by changing the content or the policy, or by a new auto-apply label policy.</span></span> <span data-ttu-id="a7f7c-161">Pour plus d'informations, voir [Une seule étiquette de conservation à la fois](retention.md#only-one-retention-label-at-a-time).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-161">For more information, see [Only one retention label at a time](retention.md#only-one-retention-label-at-a-time).</span></span>

### <a name="configuring-conditions-for-auto-apply-retention-labels"></a><span data-ttu-id="a7f7c-162">Configurer les conditions d'application automatique des étiquettes de conservation</span><span class="sxs-lookup"><span data-stu-id="a7f7c-162">Configuring conditions for auto-apply retention labels</span></span>

<span data-ttu-id="a7f7c-163">Vous pouvez appliquer automatiquement des étiquettes de rétention au contenu quand celui-ci inclut :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-163">You can apply retention labels to content automatically when that content contains:</span></span>

- [<span data-ttu-id="a7f7c-164">Types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a7f7c-164">Specific types of sensitive information</span></span>](#auto-apply-labels-to-content-with-specific-types-of-sensitive-information)

- [<span data-ttu-id="a7f7c-165">Mots clés spécifiques ou propriétés pouvant faire l’objet d’une recherche qui correspondent à une requête que vous créez</span><span class="sxs-lookup"><span data-stu-id="a7f7c-165">Specific keywords or searchable properties that match a query you create</span></span>](#auto-apply-labels-to-content-with-keywords-or-searchable-properties)

- [<span data-ttu-id="a7f7c-166">Correspondance pour les classifieurs entraînables</span><span class="sxs-lookup"><span data-stu-id="a7f7c-166">A match for trainable classifiers</span></span>](#auto-apply-labels-to-content-by-using-trainable-classifiers)

#### <a name="auto-apply-labels-to-content-with-specific-types-of-sensitive-information"></a><span data-ttu-id="a7f7c-167">Application automatique d’étiquettes au contenu incluant des types spécifiques d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="a7f7c-167">Auto-apply labels to content with specific types of sensitive information</span></span>

<span data-ttu-id="a7f7c-p111">Lorsque vous créez des stratégies d’étiquettes de rétention à appliquer automatiquement pour des informations sensibles, vous observez la même liste de modèles de stratégies que lorsque vous créez une stratégie de prévention contre la perte de données (DLP). Chaque modèle de stratégie est préconfiguré pour rechercher des types spécifiques d’informations sensibles. Par exemple, le modèle présenté ici recherche les numéros d’identification fiscale individuels américains (ITIN), les numéros de sécurité sociale et les numéros de passeport à partir de la catégorie **Confidentialité** et **du modèle de données relatives aux Informations personnelles américain** :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p111">When you create auto-apply retention label policies for sensitive information, you see the same list of policy templates as when you create a data loss prevention (DLP) policy. Each template is preconfigured to look for specific types of sensitive information. For example, the template shown here looks for U.S. ITIN, SSN, and passport numbers from the **Privacy** category, and **U.S Personally Identifiable Information (PII) Data template**:</span></span>

![Modèles de stratégies avec des types d’informations sensibles](../media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)

<span data-ttu-id="a7f7c-172">Pour plus d’informations sur les types d’informations sensibles, voir les [définitions d’entités de types d’informations sensibles](sensitive-information-type-entity-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-172">To learn more about the sensitivity information types, see [Sensitive information type entity definitions](sensitive-information-type-entity-definitions.md).</span></span>

<span data-ttu-id="a7f7c-p112">Après avoir sélectionné un modèle de stratégie, vous pouvez ajouter ou supprimer tout type d’informations sensibles, et vous pouvez modifier le nombre d’instances et  la précision de correspondance. Dans l’exemple de capture d’écran présenté ici, une étiquette de rétention sera appliquée automatiquement uniquement dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p112">After you select a policy template, you can add or remove any types of sensitive information, and you can change the instance count and match accuracy. In the example screenshot shown next, a retention label will be auto-applied only when:</span></span>
  
- <span data-ttu-id="a7f7c-p113">Le type d’informations sensibles détecté a une précision de correspondance (ou niveau de confiance) minimale de 75. De nombreux types d’informations sensibles sont définis avec plusieurs modèles. Tandis qu’un modèle avec une précision de correspondance plus élevée nécessite un nombre de preuves plus important (par exemple, des mots clés, des dates ou des adresses), un modèle avec une précision de correspondance inférieure nécessite moins de preuves. En d’autres termes, plus la précision de correspondance **min** est faible, plus il est facile de faire correspondre le contenu à la condition de correspondance</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p113">The type of sensitive information that's detected has a match accuracy (or confidence level) of at least 75. Many sensitive information types are defined with multiple patterns, where a pattern with a higher match accuracy requires more evidence to be found (such as keywords, dates, or addresses), while a pattern with a lower match accuracy requires less evidence. The lower the **min** match accuracy, the easier it is for content to match the condition.</span></span>

- <span data-ttu-id="a7f7c-p114">Le contenu comprend entre 1 et 9 instances de chacun des trois types d’informations sensibles. Vous pouvez supprimer la valeur **à** pour la définir sur **Tous**.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p114">The content contains between 1 and 9 instances of any of these three sensitive information types. You can delete the **to** value so that it changes to **Any**.</span></span>

<span data-ttu-id="a7f7c-180">Pour plus d’informations sur ces options, reportez-vous aux instructions suivantes de la documentation DLP : [Affiner les réglages pour rendre la correspondance plus ou moins précise](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-180">For more information about these options, see the following guidance from the DLP documentation [Tuning rules to make them easier or harder to match](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span></span>
    
![Options permettant d’identifier les types d’informations sensibles](../media/de255881-f596-4c8d-8359-e974e3a0819a.png)

<span data-ttu-id="a7f7c-182">Lorsque vous utilisez des types d’informations sensibles pour appliquer automatiquement des étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-182">To consider when using sensitive information types to auto-apply retention labels:</span></span>

- <span data-ttu-id="a7f7c-183">Les éléments nouveaux et modifiés peuvent être étiquetés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-183">New and modified items can be auto-labeled.</span></span>

#### <a name="auto-apply-labels-to-content-with-keywords-or-searchable-properties"></a><span data-ttu-id="a7f7c-184">Application automatique d’étiquettes au contenu comprenant des mots clés ou des propriétés pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="a7f7c-184">Auto-apply labels to content with keywords or searchable properties</span></span>

<span data-ttu-id="a7f7c-p115">Vous pouvez appliquer automatiquement des étiquettes au contenu à l’aide d’une requête qui contient des mots, des phrases ou des valeurs de propriétés pouvant faire l’objet d’une recherche. Vous pouvez affiner votre requête en utilisant des opérateurs de recherche tels que et, ou et non.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-p115">You can auto-apply labels to content by using a query that contains specific words, phrases, or values of searchable properties. You can refine your query by using search operators such as AND, OR, and NOT.</span></span>

![Éditeur de requête](../media/new-retention-query-editor.png)

<span data-ttu-id="a7f7c-188">Pour plus d’informations sur la syntaxe de requête qui utilise le langage de requête de mot clé (KQL), consultez [Référence de syntaxe de langage de requête de mot clé (KQL)](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-188">For more information about the query syntax that uses Keyword Query Language (KQL), see [Keyword Query Language (KQL) syntax reference](https://docs.microsoft.com/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference).</span></span>

<span data-ttu-id="a7f7c-189">Les stratégies d’application automatique basées sur une requête utilisent le même index de recherche que la recherche de contenu eDiscovery pour identifier du contenu.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-189">Query-based auto-apply policies use the same search index as eDiscovery content search to identify content.</span></span> <span data-ttu-id="a7f7c-190">Pour plus d’informations sur ces propriétés utilisables dans une requête, consultez [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-190">For more information about the searchable properties that you can use, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>

<span data-ttu-id="a7f7c-191">Éléments à prendre en compte lorsque vous utilisez des mots clés ou des propriétés utilisables dans une requête pour appliquer automatiquement des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="a7f7c-191">Some things to consider when using keywords or searchable properties to auto-apply retention labels:</span></span>

- <span data-ttu-id="a7f7c-192">Les éléments nouveaux, modifiés et existants sont automatiquement étiquetés pour SharePoint, OneDrive et Exchange.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-192">New, modified, and existing items will be auto-labeled for SharePoint, OneDrive, and Exchange.</span></span>

- <span data-ttu-id="a7f7c-193">Pour SharePoint, les propriétés analysées et les propriétés personnalisées ne sont pas prises en charge pour ces requêtes KQL et vous devez utiliser uniquement des propriétés gérées prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-193">For SharePoint, crawled properties and custom properties aren't supported for these KQL queries and you must use only predefined managed properties.</span></span> <span data-ttu-id="a7f7c-194">Toutefois, vous pouvez utiliser des mappages au niveau du client avec les propriétés gérées prédéfinies qui sont activées comme affinements par défaut (RefinableDate00-19, RefinableString00-99, RefinableInt00-49, RefinableDecimals00-09 et RefinableDouble00-09).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-194">However, you can use mappings at the tenant level with the predefined managed properties that are enabled as refiners by default (RefinableDate00-19, RefinableString00-99, RefinableInt00-49, RefinableDecimals00-09, and RefinableDouble00-09).</span></span> <span data-ttu-id="a7f7c-195">Pour plus d’informations, consultez[vue d’ensemble des propriétés analysées et gérées dans SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/crawled-and-managed-properties-overview)et pour obtenir des instructions, consultez [créer une propriété gérée](https://docs.microsoft.com/sharepoint/manage-search-schema#create-a-new-managed-property).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-195">For more information, see [Overview of crawled and managed properties in SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/crawled-and-managed-properties-overview), and for instructions, see [Create a new managed property](https://docs.microsoft.com/sharepoint/manage-search-schema#create-a-new-managed-property).</span></span>

- <span data-ttu-id="a7f7c-196">Si vous mappez une propriété personnalisée à l’une des propriétés d’affinement, attendez 24 heures avant de l’utiliser dans votre requête KQL pour une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-196">If you map a custom property to one of the refiner properties, wait 24 hours before you use it in your KQL query for a retention label.</span></span>

- <span data-ttu-id="a7f7c-197">Bien que les propriétés gérées de SharePoint puissent être renommées à l’aide d’alias, ne les utilisez pas pour les requêtes KQL dans vos étiquettes.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-197">Although SharePoint managed properties can be renamed by using aliases, don't use these for KQL queries in your labels.</span></span> <span data-ttu-id="a7f7c-198">Spécifiez toujours le nom réel de la propriété gérée (par exemple, « RefinableString01 »).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-198">Always specify the actual name of the managed property, for example, "RefinableString01".</span></span>

- <span data-ttu-id="a7f7c-199">Pour rechercher les valeurs qui contiennent des espaces ou des caractères spéciaux, utilisez les guillemets (`" "`) pour contenir la phrase; par exemple `subject:"Financial Statements"`.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-199">To search for values that contain spaces or special characters, use double quotation marks (`" "`) to contain the phrase; for example, `subject:"Financial Statements"`.</span></span>

- <span data-ttu-id="a7f7c-200">Utilisez la propriété *DocumentLink* au lieu de *Path* pour faire correspondre un élément en fonction de son URL.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-200">Use the *DocumentLink* property instead of *Path* to match an item based on its URL.</span></span> 

- <span data-ttu-id="a7f7c-201">Les recherches par caractères génériques suffixées (telles que `*cat`) ou les recherches par caractères génériques de sous-chaîne (telles que `*cat*`) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-201">Suffix wildcard searches ( such as `*cat`) or substring wildcard searches (such as `*cat*`) aren't supported.</span></span> <span data-ttu-id="a7f7c-202">Cependant, les recherches par caractères génériques suffixées (telles que `cat*`) sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-202">However, prefix wildcard searches (such as `cat*`) are supported.</span></span>

- <span data-ttu-id="a7f7c-203">N’oubliez pas que les éléments partiellement indexés peuvent être responsables du non étiquetage des éléments attendus, ou de l’étiquetage des éléments que vous souhaitez exclure de l’étiquetage lorsque vous utilisez l’opérateur non.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-203">Be aware that partially indexed items can be responsible for not labeling items that you're expecting, or labeling items that you're expecting to be excluded from labeling when you use the NOT operator.</span></span> <span data-ttu-id="a7f7c-204">Si vous souhaitez en savoir plus, consultez  [Éléments partiellement indexés dans la recherche de contenu](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-204">For more information, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>


<span data-ttu-id="a7f7c-205">Exemples de requêtes :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-205">Examples queries:</span></span>

| <span data-ttu-id="a7f7c-206">Charge de travail</span><span class="sxs-lookup"><span data-stu-id="a7f7c-206">Workload</span></span> | <span data-ttu-id="a7f7c-207">Exemple</span><span class="sxs-lookup"><span data-stu-id="a7f7c-207">Example</span></span> |
|:-----|:-----|
|<span data-ttu-id="a7f7c-208">Exchange</span><span class="sxs-lookup"><span data-stu-id="a7f7c-208">Exchange</span></span>   | `subject:"Financial Statements"` |
|<span data-ttu-id="a7f7c-209">Exchange</span><span class="sxs-lookup"><span data-stu-id="a7f7c-209">Exchange</span></span>   | `recipients:garthf@contoso.com` |
|<span data-ttu-id="a7f7c-210">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a7f7c-210">SharePoint</span></span> | `contenttype:document` |
|<span data-ttu-id="a7f7c-211">SharePoint</span><span class="sxs-lookup"><span data-stu-id="a7f7c-211">SharePoint</span></span> | `site:https://contoso.sharepoint.com/sites/teams/procurement AND contenttype:document`|
|<span data-ttu-id="a7f7c-212">Exchange ou SharePoint</span><span class="sxs-lookup"><span data-stu-id="a7f7c-212">Exchange or SharePoint</span></span> | `"customer information" OR "private"`|

<span data-ttu-id="a7f7c-213">Exemples plus complexes :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-213">More complex examples:</span></span>

<span data-ttu-id="a7f7c-214">La requête suivante pour SharePoint identifie des documents Word ou des feuilles de calcul Excel lorsque ces fichiers contiennent les mots clés **mot de passe**, **mots de passe** ou **pw**:</span><span class="sxs-lookup"><span data-stu-id="a7f7c-214">The following query for SharePoint identifies Word documents or Excel spreadsheets when those files contain the keywords **password**, **passwords**, or **pw**:</span></span>

```
(password OR passwords OR pw) AND (filetype:doc* OR filetype:xls*)
```

<span data-ttu-id="a7f7c-215">La requête Exchange suivante identifie tout document Word ou PDF contenant le mot **accord de confidentialité** ou l’expression **contrat de non-divulgation** lorsque ces documents sont joints à un e-mail :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-215">The following query for Exchange identifies any Word document or PDF that contains the word **nda** or the phrase **non disclosure agreement** when those documents are attached to an email:</span></span>

```
(nda OR "non disclosure agreement") AND (attachmentnames:.doc* OR attachmentnames:.pdf)
```

<span data-ttu-id="a7f7c-216">La requête SharePoint suivante identifie les documents qui contiennent un numéro de carte de crédit :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-216">The following query for SharePoint identifies documents that contain a credit card number:</span></span> 

```
sensitivetype:"credit card number"
```

<span data-ttu-id="a7f7c-217">La requête suivante contient des mots clés courants pour vous aider à identifier les documents ou les e-mails qui contiennent du contenu juridique :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-217">The following query contains some typical keywords to help identify documents or emails that contain legal content:</span></span>

```
ACP OR (Attorney Client Privilege*) OR (AC Privilege)
```

<span data-ttu-id="a7f7c-218">La requête suivante contient des mots clés courants pour vous aider à identifier les documents ou les e-mails des ressources humaines :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-218">The following query contains typical keywords to help identify documents or emails for human resources:</span></span> 

```
(resume AND staff AND employee AND salary AND recruitment AND candidate)
```

<span data-ttu-id="a7f7c-219">Notez que ce dernier exemple utilise la pratique recommandée qui consiste à toujours inclure des opérateurs entre les mots clés.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-219">Note that this final example uses the best practice of always including  operators between keywords.</span></span> <span data-ttu-id="a7f7c-220">Un espace entre des mots-clés (ou deux expressions de valeur de propriété) revient au même que l’utilisation de l’opérateur AND.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-220">A space between keywords (or two property:value expressions) is the same as using AND.</span></span> <span data-ttu-id="a7f7c-221">En ajoutant toujours des opérateurs, il est plus facile de voir que cet exemple de requête identifie uniquement le contenu qui contient tous ces mots clés, au lieu du contenu contenant tous les mots clés.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-221">By always adding operators, it's easier to see that this example query will identify only content that contains all these keywords, instead of content that contains any of the keywords.</span></span> <span data-ttu-id="a7f7c-222">Si vous avez l’intention d’identifier le contenu contenant l’un des mots clés, spécifiez ou au lieu de et.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-222">If your intention is to identify content that contains any of the keywords, specify OR instead of AND.</span></span> <span data-ttu-id="a7f7c-223">Comme cet exemple montre, lorsque vous spécifiez toujours les opérateurs, il est plus facile d’interpréter correctement la requête.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-223">As this example shows, when you always specify the operators, it's easier to correctly interpret the query.</span></span> 

##### <a name="microsoft-teams-meeting-recordings"></a><span data-ttu-id="a7f7c-224">Enregistrements de réunion Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a7f7c-224">Microsoft Teams meeting recordings</span></span>

> [!NOTE]
> <span data-ttu-id="a7f7c-225">La possibilité de conserver et de supprimer les enregistrements de réunions Teams est déployé dans l’aperçu et ne fonctionnera pas avant la sauvegarde des enregistrements dans OneDrive ou SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-225">The ability to retain and delete Teams meeting recordings is in preview and won't work before recordings are saved to OneDrive or SharePoint.</span></span> <span data-ttu-id="a7f7c-226">Pour plus d’informations, consultez [Utiliser OneDrive Entreprise et SharePoint Online ou Stream pour les enregistrements de réunion](https://docs.microsoft.com/MicrosoftTeams/tmr-meeting-recording-change).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-226">For more information, see [Use OneDrive for Business and SharePoint Online or Stream for meeting recordings](https://docs.microsoft.com/MicrosoftTeams/tmr-meeting-recording-change).</span></span>

<span data-ttu-id="a7f7c-227">Pour identifier les enregistrements de réunion Microsoft Teams stockés dans les comptes OneDrive des utilisateurs ou dans SharePoint, spécifiez les éléments suivants pour **l’éditeur de requête de mot clé**:</span><span class="sxs-lookup"><span data-stu-id="a7f7c-227">To identify Microsoft Teams meeting recordings that are stored in users' OneDrive accounts or in SharePoint, specify the following for the **Keyword query editor**:</span></span>

``` 
ProgID:Media AND ProgID:Meeting
```

<span data-ttu-id="a7f7c-228">La plupart du temps, les enregistrements de réunion sont enregistrés dans OneDrive.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-228">Most of the time, meeting recordings are saved to OneDrive.</span></span> <span data-ttu-id="a7f7c-229">Mais les réunions de canal sont enregistrés dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-229">But for channel meetings, they are saved in SharePoint.</span></span>


#### <a name="auto-apply-labels-to-content-by-using-trainable-classifiers"></a><span data-ttu-id="a7f7c-230">Appliquer automatiquement des étiquettes au contenu à l’aide de classificateurs entraînables</span><span class="sxs-lookup"><span data-stu-id="a7f7c-230">Auto-apply labels to content by using trainable classifiers</span></span>

<span data-ttu-id="a7f7c-231">Lorsque vous choisissez l’option de classifieur entraînable, vous pouvez sélectionner un classifieur intégré ou un classifieur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-231">When you choose the option for a trainable classifier, you can select one of the built-in classifiers, or a custom classifier.</span></span> <span data-ttu-id="a7f7c-232">Les classifieurs intégrés incluent : **CV**, **SourceCode**, **Harcèlement ciblé**, **Blasphème** et la **Menace** :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-232">The built-in classifiers include **Resumes**, **SourceCode**, **Targeted Harassment**, **Profanity**, and **Threat**:</span></span>

![Sélectionnez un classificateur à entraîner](../media/retention-label-classifers.png)

> [!CAUTION]
> <span data-ttu-id="a7f7c-234">Nous déprécions le **langage inconvenant** classifieur intégré, car il génère un grand nombre de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-234">We are deprecating the **Offensive Language** built-in classifier because it has been producing a high number of false positives.</span></span> <span data-ttu-id="a7f7c-235">N’utilisez pas ce classifieur intégré et si vous l’utilisez actuellement, vous devez déplacer vos processus métier.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-235">Don't use this built-in classifier and if you are currently using it, you should move your business processes off it.</span></span> <span data-ttu-id="a7f7c-236">Nous vous recommandons d’utiliser les classifieurs intégrés de **Harcèlement ciblée** , de **blasphème** et de **Menace** à la place.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-236">We recommend using the **Targeted Harassment**, **Profanity**, and **Threat** built-in classifiers instead.</span></span>

<span data-ttu-id="a7f7c-237">Pour appliquer automatiquement une étiquette à l’aide de cette option, les sites et boîtes aux lettres SharePoint doivent avoir au moins 10 Mo de données.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-237">To automatically apply a label by using this option, SharePoint sites and mailboxes must have at least 10 MB of data.</span></span>

<span data-ttu-id="a7f7c-238">Pour plus d’informations sur les classifieurs de formation, consultez [Découvrez les classifieurs de formation (préversion)](classifier-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-238">For more information about trainable classifiers, see [Learn about trainable classifiers (preview)](classifier-learn-about.md).</span></span>

> [!TIP]
> <span data-ttu-id="a7f7c-239">Si vous utilisez des classifieurs entraînables pour Exchange, voir le récent article [Comment recycler un classifieur dans l’Explorateur de contenu (préversion)](classifier-how-to-retrain-content-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-239">If you use trainable classifiers for Exchange, see the recently released [How to retrain a classifier in content explorer (preview)](classifier-how-to-retrain-content-explorer.md).</span></span>

<span data-ttu-id="a7f7c-240">Lorsque vous utilisez des classificateurs pouvant apprendre pour appliquer automatiquement des étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-240">To consider when using trainable classifiers to auto-apply retention labels:</span></span>

- <span data-ttu-id="a7f7c-241">Les éléments nouveaux et modifiés peuvent être étiquetés automatiquement ainsi que les éléments existants des six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-241">New and modified items can be auto-labeled, and existing items from the last six months.</span></span>

## <a name="how-long-it-takes-for-retention-labels-to-take-effect"></a><span data-ttu-id="a7f7c-242">Délai d’activation des étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="a7f7c-242">How long it takes for retention labels to take effect</span></span>

<span data-ttu-id="a7f7c-243">Lorsque vous appliquez automatiquement des étiquettes de rétention, l’application de ces étiquettes à ce contenu peut prendre jusqu’à sept jours.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-243">When you auto-apply retention labels, it can take up to seven days for the retention labels to be applied to all existing content that matches the conditions.</span></span>
  
![Diagramme indiquant quand les étiquettes d’application automatique prennent effet](../media/b8c00657-477a-4ade-b914-e643ef97a10d.png)

<span data-ttu-id="a7f7c-245">Si les étiquettes attendues n’apparaissent pas après sept jours, consultez l’**État** de la stratégie d’application automatique en sélectionnant celle-ci dans la page des **Stratégies d’étiquette** dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-245">If the expected labels don't appear after seven days, check the **Status** of the auto-apply policy by selecting it from the **Label policies** page in the compliance center.</span></span> <span data-ttu-id="a7f7c-246">Si vous voyez l’état de **Désactivé (erreur)** et dans les détails des emplacements, consultez un message indiquant qu’il prend plus de temps que prévu pour déployer la stratégie (pour SharePoint) ou essayez de redéployer la stratégie (pour OneDrive), essayez d’exécuter la commande PowerShell [RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) pour réessayer la distribution de la stratégie :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-246">If you see the status of **Off (Error)** and in the details for the locations see a message that it's taking longer than expected to deploy the policy (for SharePoint) or to try redeploying the policy (for OneDrive), try running the [Set-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) PowerShell command to retry the policy distribution:</span></span>

1. <span data-ttu-id="a7f7c-247">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-247">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="a7f7c-248">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-248">Run the following command:</span></span>
    
    ``` PowerShell
    Set-RetentionCompliancePolicy -Identity <policy name> -RetryDistribution
   ```

## <a name="updating-retention-labels-and-their-policies"></a><span data-ttu-id="a7f7c-249">Mise à jour des étiquettes de rétention et de leurs stratégies</span><span class="sxs-lookup"><span data-stu-id="a7f7c-249">Updating retention labels and their policies</span></span>

<span data-ttu-id="a7f7c-250">Lorsque vous modifiez une étiquette de rétention ou une stratégie d’application automatique et que l’étiquette de rétention est déjà appliquée au contenu, vos paramètres mis à jour sont automatiquement appliqués à ce contenu, en plus du contenu nouvellement identifié.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-250">When you edit a retention label or auto-apply policy, and the retention label is already applied to content, your updated settings will automatically be applied to this content in addition to content that's newly identified.</span></span>

<span data-ttu-id="a7f7c-251">Certains paramètres ne peuvent pas être modifiés une fois l’étiquette ou la stratégie créée et enregistrée, notamment :</span><span class="sxs-lookup"><span data-stu-id="a7f7c-251">Some settings can't be changed after the label or policy is created and saved, which include:</span></span>
- <span data-ttu-id="a7f7c-252">Étiquette de rétention et le nom de la stratégie, et les paramètres de rétention à l’exception de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-252">The retention label and policy name, and the retention settings except the retention period.</span></span> <span data-ttu-id="a7f7c-253">Cependant, vous ne pouvez pas modifier la période de rétention lorsque la période de rétention est basée sur la période d’étiquetage des éléments.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-253">However, you can't change the retention period when the retention period is based on when items were labeled.</span></span>
- <span data-ttu-id="a7f7c-254">Option de marquage des éléments comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-254">The option to mark items as a record.</span></span>

## <a name="locking-the-policy-to-prevent-changes"></a><span data-ttu-id="a7f7c-255">Verrouillage de la stratégie pour empêcher toute modification</span><span class="sxs-lookup"><span data-stu-id="a7f7c-255">Locking the policy to prevent changes</span></span>

<span data-ttu-id="a7f7c-256">Si vous voulez vous assurer que personne ne peut désactiver la stratégie, supprimer la stratégie ou la rendre moins restrictive, consultez [Utiliser le Verrou de Conservation pour restreindre les modifications apportées aux stratégies de rétention et aux stratégies d’étiquette de rétention](retention-preservation-lock.md).</span><span class="sxs-lookup"><span data-stu-id="a7f7c-256">If you need to ensure that no one can turn off the policy, delete the policy, or make it less restrictive, see [Use Preservation Lock to restrict changes to retention policies and retention label policies](retention-preservation-lock.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a7f7c-257">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="a7f7c-257">Next steps</span></span>

<span data-ttu-id="a7f7c-258">Consultez [Utiliser les étiquettes de rétention pour gérer le cycle de vie des documents stockés dans SharePoint](auto-apply-retention-labels-scenario.md) pour un exemple de scénario qui utilise une stratégie d’application automatique avec des propriétés gérées dans SharePoint et la rétention basée sur les événements pour démarrer la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="a7f7c-258">See [Use retention labels to manage the lifecycle of documents stored in SharePoint](auto-apply-retention-labels-scenario.md) for an example scenario that uses an auto-apply retention label policy with managed properties in SharePoint, and event-based retention to start the retention period.</span></span>
