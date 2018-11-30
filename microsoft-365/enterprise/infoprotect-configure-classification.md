---
title: 'Étape 2 : Configurer la classification pour votre environnement'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez différentes méthodes pour classer les données de votre organisation.
ms.openlocfilehash: bee0885eb3f8899560532895d1558723b281ab02
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867037"
---
# <a name="step-2-configure-classification-for-your-environment"></a><span data-ttu-id="6ee50-103">Étape 2 : Configurer la classification pour votre environnement</span><span class="sxs-lookup"><span data-stu-id="6ee50-103">Step 2: Configure classification for your environment</span></span>

<span data-ttu-id="6ee50-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="6ee50-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="6ee50-105">Dans cette étape, vous travaillez avec vos équipes juridiques et de conformité pour définir un système de classification pour les données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ee50-105">In Step 3, you work with your legal and compliance teams to define a classification scheme for your organization’s data.</span></span>

## <a name="microsoft-classifications"></a><span data-ttu-id="6ee50-106">Classifications de Microsoft</span><span class="sxs-lookup"><span data-stu-id="6ee50-106">Microsoft classifications</span></span>

<span data-ttu-id="6ee50-107">Microsoft 365 inclut trois types de classification :</span><span class="sxs-lookup"><span data-stu-id="6ee50-107">Microsoft 365 includes three types of classification:</span></span>

- <span data-ttu-id="6ee50-108">Types d’informations sensibles pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ee50-108">Sensitive information types for Office 365</span></span>
- <span data-ttu-id="6ee50-109">Étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="6ee50-109">Office 365 labels</span></span>
- <span data-ttu-id="6ee50-110">Étiquettes Azure Information Protection et protection</span><span class="sxs-lookup"><span data-stu-id="6ee50-110">Azure Information Protection labels and protection</span></span>

### <a name="sensitive-information-types-for-office-365"></a><span data-ttu-id="6ee50-111">Types d’informations sensibles pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ee50-111">Sensitive information types for Office 365</span></span>

<span data-ttu-id="6ee50-p101">Les types d’informations sensibles pour Office 365 définissent la façon dont les processus automatisés tels que la recherche reconnaissent des types d’informations spécifiques (numéros de service de santé et numéros de carte de crédit, par exemple). Les types d’informations sensibles permettent de rechercher des données sensibles et d’appliquer des stratégies et des règles de protection contre la perte de données afin de protéger ces données. Pour plus d’informations, reportez-vous à la rubrique [Vue d’ensemble des stratégies de protection contre la perte de données](https://support.office.com/article/overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e). Par exemple, les types d’informations sensibles sont particulièrement utiles pour la conformité aux exigences de réglementation (pour le RGPD, par exemple).</span><span class="sxs-lookup"><span data-stu-id="6ee50-p101">Sensitive information types for Office 365 define how automated processes such as search recognize specific information types such as health service numbers and credit card numbers. You use sensitive information types to find sensitive data and apply data loss prevention rules and policies to protect this data. For more information, see [Overview of data loss prevention policies](https://support.office.com/article/overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e). For example, sensitive information types are especially helpful for meeting compliance and regulation requirements, such as for the General Data Protection Regulation (GDPR).</span></span>

### <a name="office-365-labels"></a><span data-ttu-id="6ee50-116">Étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="6ee50-116">Office 365 labels</span></span>
<span data-ttu-id="6ee50-p102">Vous pouvez utiliser des étiquettes Office 365 pour des données personnelles ou pour des fichiers secrets et hautement réglementés stockés dans SharePoint Online et OneDrive Entreprise. Pour plus d’informations, notamment sur leur création, reportez-vous à la rubrique [Vue d’ensemble des étiquettes](https://support.office.com/article/overview-of-labels-af398293-c69d-465e-a249-d74561552d30).</span><span class="sxs-lookup"><span data-stu-id="6ee50-p102">You can use Office 365 labels for personal data and for highly regulated and trade secret files stored in SharePoint Online and OneDrive for Business. For more information, including how to create them, see [Overview of labels](https://support.office.com/article/overview-of-labels-af398293-c69d-465e-a249-d74561552d30).</span></span>

<span data-ttu-id="6ee50-p103">Si vous décidez d’utiliser des étiquettes Office 365, vous devez en configurer au moins une pour chaque niveau de protection. Par exemple, créez trois étiquettes pour :</span><span class="sxs-lookup"><span data-stu-id="6ee50-p103">If you decide to use Office 365 labels, you should configure at least one for each level of protection. For example, create three labels for:</span></span>

- <span data-ttu-id="6ee50-121">Baseline</span><span class="sxs-lookup"><span data-stu-id="6ee50-121">Baseline</span></span>
- <span data-ttu-id="6ee50-122">Sensible</span><span class="sxs-lookup"><span data-stu-id="6ee50-122">Sensitive</span></span>
- <span data-ttu-id="6ee50-123">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="6ee50-123">Highly regulated</span></span>

### <a name="azure-information-protection-labels-and-protection"></a><span data-ttu-id="6ee50-124">Étiquettes Azure Information Protection et protection</span><span class="sxs-lookup"><span data-stu-id="6ee50-124">Azure Information Protection labels and protection</span></span>

<span data-ttu-id="6ee50-p104">Vous pouvez utiliser des étiquettes Azure Information Protection pour classer et éventuellement protéger, les messages électroniques et documents de votre organisation. Ces étiquettes peuvent s’appliquer à des documents stockés en dehors d’Office 365. Ces étiquettes peuvent être appliquées automatiquement par les administrateurs qui définissent les règles et conditions, manuellement par les utilisateurs ou une combinaison des deux lorsque les utilisateurs reçoivent des recommandations.</span><span class="sxs-lookup"><span data-stu-id="6ee50-p104">You can use Azure Information Protection labels to classify, and optionally protect, your organization’s documents and emails. These labels can apply to documents that are stored outside of Office 365. These labels can be applied automatically by administrators who define rules and conditions, manually by users, or a combination where users are given recommendations.</span></span>

<span data-ttu-id="6ee50-128">Pour planifier et déployer des étiquettes Azure Information Protection, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="6ee50-128">To plan and deploy Azure Information Protection labels and protection, do the following:</span></span>

1. <span data-ttu-id="6ee50-129">Revoyez la [configuration requise pour Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/requirements).</span><span class="sxs-lookup"><span data-stu-id="6ee50-129">Review the [requirements for Azure Information Protection](https://docs.microsoft.com/information-protection/get-started/requirements).</span></span>
2. <span data-ttu-id="6ee50-130">Suivez la [feuille de route de déploiement pour la classification, l’utilisation d’étiquettes et la protection](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap#deployment-roadmap-for-classification-labeling-and-protection).</span><span class="sxs-lookup"><span data-stu-id="6ee50-130">Follow the [deployment roadmap for classification, labeling, and protection](https://docs.microsoft.com/information-protection/plan-design/deployment-roadmap#deployment-roadmap-for-classification-labeling-and-protection).</span></span>

<span data-ttu-id="6ee50-131">Pour plus d’informations, reportez-vous à la [bibliothèque de documentation Azure Information Protection](https://docs.microsoft.com/information-protection/).</span><span class="sxs-lookup"><span data-stu-id="6ee50-131">For more information, see the [library of Azure Information Protection documentation](https://docs.microsoft.com/information-protection/).</span></span>

## <a name="classification-for-gdpr"></a><span data-ttu-id="6ee50-132">Classification pour le RGPD</span><span class="sxs-lookup"><span data-stu-id="6ee50-132">Classification for GDPR</span></span>

<span data-ttu-id="6ee50-133">Pour consulter un exemple de système de classification qui comprend des données personnelles pour le RGPD, reportez-vous à la rubrique [Création d’un schéma de classification pour les données personnelles](https://docs.microsoft.com/office365/enterprise/architect-a-classification-schema-for-personal-data).</span><span class="sxs-lookup"><span data-stu-id="6ee50-133">For an example classification scheme that includes personal data for GDPR, see [Architect a classification schema for personal data](https://docs.microsoft.com/office365/enterprise/architect-a-classification-schema-for-personal-data).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="6ee50-135">Guide de Laboratoire de Test : Classification des données</span><span class="sxs-lookup"><span data-stu-id="6ee50-135">Test Lab Guide: Data classification</span></span>](data-classification-microsoft-365-enterprise-dev-test-environment.md) |
|||

<span data-ttu-id="6ee50-136">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step3) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="6ee50-136">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step3) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="6ee50-137">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="6ee50-137">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step3.png)|[<span data-ttu-id="6ee50-138">Configurez une sécurité accrue pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6ee50-138">Configure increased security for Office 365</span></span>](infoprotect-configure-increased-security-office-365.md)|

