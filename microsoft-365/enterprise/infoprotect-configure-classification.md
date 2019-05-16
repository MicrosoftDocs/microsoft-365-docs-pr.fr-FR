---
title: 'Étape 2 : Configurer la classification pour votre environnement'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez différentes méthodes pour classer les données de votre organisation.
ms.openlocfilehash: 483549e7eaa7f6b77b775cf35bda7b0f42834ad2
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34072254"
---
# <a name="step-2-configure-classification-for-your-environment"></a><span data-ttu-id="7f70c-103">Étape 2 : Configurer la classification pour votre environnement</span><span class="sxs-lookup"><span data-stu-id="7f70c-103">Step 2: Configure classification for your environment</span></span>

<span data-ttu-id="7f70c-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="7f70c-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="7f70c-105">Dans cette étape, vous travaillez avec vos équipes juridiques et de conformité pour définir un système de classification pour les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7f70c-105">In this step, you work with your legal and compliance teams to define a classification scheme for your organization’s data.</span></span>

## <a name="microsoft-365-classification-types"></a><span data-ttu-id="7f70c-106">Types de classification de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7f70c-106">Microsoft 365 classification types</span></span>

<span data-ttu-id="7f70c-107">Microsoft 365 inclut quatre types de classification :</span><span class="sxs-lookup"><span data-stu-id="7f70c-107">Microsoft 365 includes four types of classification:</span></span>

- <span data-ttu-id="7f70c-108">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7f70c-108">Sensitive information types</span></span>
- <span data-ttu-id="7f70c-109">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="7f70c-109">Retention labels</span></span>
- <span data-ttu-id="7f70c-110">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="7f70c-110">Sensitivity labels</span></span>
- <span data-ttu-id="7f70c-111">Étiquettes Azure Information Protection et protection</span><span class="sxs-lookup"><span data-stu-id="7f70c-111">Azure Information Protection labels and protection</span></span>

### <a name="sensitive-information-types"></a><span data-ttu-id="7f70c-112">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7f70c-112">Sensitive information types</span></span>

<span data-ttu-id="7f70c-113">Les types d’informations sensibles pour Microsoft 365 définissent comment les processus automatisés tels que la recherche reconnaissent les types d’informations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7f70c-113">Sensitive information types for Microsoft 365 define how automated processes such as search recognize specific information types.</span></span> <span data-ttu-id="7f70c-114">Celles-ci incluent les données sensibles employé ou client tels que les numéros de sécurité sociale et les numéros de carte bancaire.</span><span class="sxs-lookup"><span data-stu-id="7f70c-114">These include sensitive employee or customer data such as health service numbers and credit card numbers.</span></span> <span data-ttu-id="7f70c-115">Vous utilisez les types d’informations sensibles pour trouver des données sensibles et appliquer des règles de prévention contre la perte de données et des stratégies pour protéger ces données.</span><span class="sxs-lookup"><span data-stu-id="7f70c-115">You use sensitive information types to find sensitive data and apply data loss prevention (DLP) rules and policies to protect this data.</span></span> <span data-ttu-id="7f70c-116">Pour plus d’informations, voir [ce que contient une stratégie DLP](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies#what-a-dlp-policy-contains).</span><span class="sxs-lookup"><span data-stu-id="7f70c-116">For more information, see [what a DLP policy contains](https://docs.microsoft.com/office365/securitycompliance/data-loss-prevention-policies#what-a-dlp-policy-contains).</span></span> 

<span data-ttu-id="7f70c-117">Les types d’informations sensibles sont particulièrement utiles pour se plier aux exigences de conformité et réglementation, comme pour la Protection générale des données (RGPD).</span><span class="sxs-lookup"><span data-stu-id="7f70c-117">Sensitive information types are especially helpful for meeting compliance and regulation requirements, such as for the General Data Protection Regulation (GDPR).</span></span>

### <a name="retention-labels"></a><span data-ttu-id="7f70c-118">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="7f70c-118">Retention labels</span></span>

<span data-ttu-id="7f70c-119">Une partie de définir une stratégie de gouvernance des données consiste à décider combien de temps des types spécifiques de documents ou des documents avec contenu spécifique doivent être conservés, conformément aux stratégies de l’organisation et aux réglementations régionales.</span><span class="sxs-lookup"><span data-stu-id="7f70c-119">Part of defining a data governance strategy is deciding how long specific types of documents or documents with specific contents should be retained in compliance with organization policies and regional regulations.</span></span> <span data-ttu-id="7f70c-120">Par exemple, certains types de documents doivent être conservés pendant une durée définie avant d’être supprimés et d’autres doivent être conservés indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="7f70c-120">For example, some types of documents should be retained for a set amount of time and then deleted and others must be retained indefinitely.</span></span>

<span data-ttu-id="7f70c-121">Pour les documents stockés dans Microsoft 365, définir et appliquer des étiquettes de rétention à des documents et données stockées dans la messagerie Exchange, SharePoint Online, OneDrive Entreprise et messages de conversation et canal Teams.</span><span class="sxs-lookup"><span data-stu-id="7f70c-121">For documents stored in Microsoft 365, you define and apply retention labels to documents and data stored in Exchange email, SharePoint Online, OneDrive for Business, and Teams chat and channel messages.</span></span> 

<span data-ttu-id="7f70c-122">Si vous utilisez des étiquettes de rétention, vous devez configurer une étiquette pour chaque catégorie de fichier qui doit disposer d’une stratégie de rétention appliquée.</span><span class="sxs-lookup"><span data-stu-id="7f70c-122">If you use retention labels, you should configure a label for each category of file that needs to have a retention policy applied.</span></span> <span data-ttu-id="7f70c-123">Au sein de l’étiquette de rétention, vous pouvez spécifier :</span><span class="sxs-lookup"><span data-stu-id="7f70c-123">Within the retention label, you can specify:</span></span>

- <span data-ttu-id="7f70c-124">Un ensemble de descriptifs pour les fichiers (par exemple, par département d’entreprise, catégorie de fichier ou règlement).</span><span class="sxs-lookup"><span data-stu-id="7f70c-124">A set of descriptors for the files (for example, by business department, file category, or regulation).</span></span>
- <span data-ttu-id="7f70c-125">Les paramètres de rétention pour les fichiers qui ont l’étiquette de rétention, tels que les heures de conservation et comportements après que la durée de conservation a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="7f70c-125">The retention settings for the files that have the retention label attached, such as retain times and behaviors after the retain time has been reached.</span></span>

<span data-ttu-id="7f70c-126">Vous pouvez également appliquer automatiquement une étiquette de rétention aux fichiers en configurant un site SharePoint Online pour appliquer une étiquette de rétention par défaut pour tous les nouveaux documents dans le site.</span><span class="sxs-lookup"><span data-stu-id="7f70c-126">You can also apply a retention label to files automatically by configuring a SharePoint Online site to apply a default retention label to all new documents in the site.</span></span> 

<span data-ttu-id="7f70c-127">Pour plus d’informations, voir[Vue d’ensemble des étiquettes de rétention](https://docs.microsoft.com/office365/securitycompliance/labels).</span><span class="sxs-lookup"><span data-stu-id="7f70c-127">For more information, see the [overview of retention labels](https://docs.microsoft.com/office365/securitycompliance/labels).</span></span>

### <a name="sensitivity-labels"></a><span data-ttu-id="7f70c-128">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="7f70c-128">Sensitivity labels</span></span>

<span data-ttu-id="7f70c-129">Une partie de protection et implémentation de sécurité pour des types de documents ou des documents avec contenu spécifique consiste en les marquer d’une étiquette de sorte que la sécurité supplémentaire puisse être appliquée.</span><span class="sxs-lookup"><span data-stu-id="7f70c-129">Part of protecting and implementing security for specific types of documents or documents with specific contents is marking them with a label so that the additional security can be applied.</span></span> <span data-ttu-id="7f70c-130">Avec des étiquettes de niveau de confidentialité dans Microsoft 365, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="7f70c-130">With sensitivity labels in Microsoft 365, you can:</span></span>

- <span data-ttu-id="7f70c-131">Appliquer des paramètres de protection comme le chiffrement, autorisations ou ajouter un filigrane.</span><span class="sxs-lookup"><span data-stu-id="7f70c-131">Enforce protection settings such as encryption, permissions, or adding a watermark.</span></span>
- <span data-ttu-id="7f70c-132">Empêcher les contenus sensibles de sortir de votre organisation sur les appareils exécutant Windows, à l’aide de la protection de point de terminaison dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="7f70c-132">Prevent sensitive content from leaving your organization on devices running Windows, by using endpoint protection in Microsoft Intune.</span></span> 
- <span data-ttu-id="7f70c-133">Utiliser la protection de point de terminaison Protection des Informations Windows (WIP) permet d’empêcher que le contenu soit copié à une application tierce, par exemple, Twitter ou Gmail, ou copié sur un stockage amovible, par exemple, un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="7f70c-133">Use Windows Information Protection (WIP) endpoint protection to prevent that content from being copied to a third-party app, such as Twitter or Gmail, or being copied to removable storage, such as a USB drive.</span></span>
- <span data-ttu-id="7f70c-134">Utiliser Microsoft Cloud App Security pour protéger le contenu dans les services tiers et les applications tierces.</span><span class="sxs-lookup"><span data-stu-id="7f70c-134">Use Microsoft Cloud App Security to protect content in third-party apps and services.</span></span> 
- <span data-ttu-id="7f70c-135">Classifier du contenu sans utiliser les paramètres de protection.</span><span class="sxs-lookup"><span data-stu-id="7f70c-135">Classify content without using any protection settings.</span></span>

<span data-ttu-id="7f70c-136">Si vous utilisez des étiquettes de niveau de confidentialité, vous devez configurer une étiquette pour chaque niveau de protection d’information et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="7f70c-136">If you use sensitivity labels, you should configure a label for each security and information protection level.</span></span> <span data-ttu-id="7f70c-137">Par exemple, créer trois étiquettes sensibilité pour :</span><span class="sxs-lookup"><span data-stu-id="7f70c-137">For example, create three sensitivity labels for:</span></span>

- <span data-ttu-id="7f70c-138">Baseline</span><span class="sxs-lookup"><span data-stu-id="7f70c-138">Baseline</span></span>
- <span data-ttu-id="7f70c-139">Sensible</span><span class="sxs-lookup"><span data-stu-id="7f70c-139">Sensitive</span></span>
- <span data-ttu-id="7f70c-140">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="7f70c-140">Highly regulated</span></span>

<span data-ttu-id="7f70c-141">Pour plus d’informations, voir[Vue d’ensemble des étiquettes de sensibilité](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels).</span><span class="sxs-lookup"><span data-stu-id="7f70c-141">For more information, see this [overview of sensitivity labels](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels).</span></span>

### <a name="azure-information-protection-labels-and-protection"></a><span data-ttu-id="7f70c-142">Étiquettes Azure Information Protection et protection</span><span class="sxs-lookup"><span data-stu-id="7f70c-142">Azure Information Protection labels and protection</span></span>

<span data-ttu-id="7f70c-143">Vous pouvez utiliser des étiquettes Azure Information Protection pour classifier et également protéger les messages électroniques et documents de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7f70c-143">You can use Azure Information Protection labels to classify, and optionally protect, your organization’s documents and emails.</span></span> <span data-ttu-id="7f70c-144">Ces étiquettes peuvent s’appliquer à des documents qui sont stockés en dehors de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f70c-144">These labels can apply to documents that are stored outside of Microsoft 365.</span></span> <span data-ttu-id="7f70c-145">Ces opérations peuvent être effectuées automatiquement par les administrateurs qui définissent des règles et des conditions ou manuellement par les utilisateurs, ou une combinaison où les utilisateurs peuvent recevoir des recommandations.</span><span class="sxs-lookup"><span data-stu-id="7f70c-145">These labels can be applied automatically by administrators who define rules and conditions, manually by users, or a combination where users are given recommendations.</span></span>

<span data-ttu-id="7f70c-146">Pour planifier et déployer des étiquettes Azure Information Protection, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7f70c-146">To plan and deploy Azure Information Protection labels and protection, do the following:</span></span>

1. <span data-ttu-id="7f70c-147">Revoyez la [configuration requise pour Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/requirements).</span><span class="sxs-lookup"><span data-stu-id="7f70c-147">Review the [requirements for Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/requirements).</span></span>
2. <span data-ttu-id="7f70c-148">Suivez la [feuille de route de déploiement pour la classification, l’utilisation d’étiquettes et la protection](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap#deployment-roadmap-for-classification-labeling-and-protection).</span><span class="sxs-lookup"><span data-stu-id="7f70c-148">Follow the [deployment roadmap for classification, labeling, and protection](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap#deployment-roadmap-for-classification-labeling-and-protection).</span></span>

<span data-ttu-id="7f70c-149">Pour plus d’informations, reportez-vous à la [bibliothèque de documentation Azure Information Protection](https://docs.microsoft.com/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="7f70c-149">For more information, see the [library of Azure Information Protection documentation](https://docs.microsoft.com/information-protection/).</span></span>

<span data-ttu-id="7f70c-150">Fonctionnement des étiquettes de niveau de confidentialité avec les étiquettes Protection Information Existante Azure.</span><span class="sxs-lookup"><span data-stu-id="7f70c-150">Existing Azure Information Protection labels work seamlessly with sensitivity labels.</span></span> <span data-ttu-id="7f70c-151">Par exemple, vous pouvez maintenir vos étiquettes Azure Information Protection existantes et les étiquettes qui sont appliquées aux documents et courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="7f70c-151">For example, you can keep your existing Azure Information Protection labels and the labels that are applied to documents and email.</span></span>

<span data-ttu-id="7f70c-152">Si vous avez des étiquettes sensibilité et Azure Information Protection, vous devez [migrer vos étiquettes Azure Information Protection aux étiquettes sensibilité](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels#how-sensitivity-labels-work-with-existing-azure-information-protection-labels).</span><span class="sxs-lookup"><span data-stu-id="7f70c-152">If you have both sensitivity and Azure Information Protection labels, you should [migrate your Azure Information Protection labels to sensitivity labels](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels#how-sensitivity-labels-work-with-existing-azure-information-protection-labels).</span></span>

## <a name="example-classification-for-gdpr"></a><span data-ttu-id="7f70c-153">Exemple : Classification pour RGPD</span><span class="sxs-lookup"><span data-stu-id="7f70c-153">Example: Classification for GDPR</span></span>

<span data-ttu-id="7f70c-154">Pour consulter un exemple de système de classification qui comprend des données personnelles pour le RGPD, reportez-vous à la rubrique [Création d’un schéma de classification pour les données personnelles](https://docs.microsoft.com/office365/enterprise/architect-a-classification-schema-for-personal-data).</span><span class="sxs-lookup"><span data-stu-id="7f70c-154">For an example classification scheme that includes personal data for GDPR, see [Architect a classification schema for personal data](https://docs.microsoft.com/office365/enterprise/architect-a-classification-schema-for-personal-data).</span></span>

## <a name="take-it-for-a-test-drive"></a><span data-ttu-id="7f70c-155">Obtenir la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="7f70c-155">Take it for a test drive</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="7f70c-157">Guide de Laboratoire de Test : Classification des données</span><span class="sxs-lookup"><span data-stu-id="7f70c-157">Test Lab Guide: Data classification</span></span>](data-classification-microsoft-365-enterprise-dev-test-environment.md) |
|||

<span data-ttu-id="7f70c-158">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step2) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="7f70c-158">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step2) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="7f70c-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7f70c-159">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)|[<span data-ttu-id="7f70c-160">Configurez une sécurité accrue pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7f70c-160">Configure increased security for Office 365</span></span>](infoprotect-configure-increased-security-office-365.md)|

