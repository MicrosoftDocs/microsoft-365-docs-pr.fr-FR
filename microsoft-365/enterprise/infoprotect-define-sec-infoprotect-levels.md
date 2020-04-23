---
title: 'Étape 1 : Définir les niveaux de protection des informations et de sécurité'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez les niveaux de protection des informations et de sécurité pour votre organisation.
ms.openlocfilehash: 0fa3e9fa11070ea505752d781ecdd21b344c8222
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43636963"
---
# <a name="step-1-define-security-and-information-protection-levels"></a><span data-ttu-id="68256-103">Étape 1 : Définir les niveaux de protection des informations et de sécurité</span><span class="sxs-lookup"><span data-stu-id="68256-103">Step 1: Define security and information protection levels</span></span>

<span data-ttu-id="68256-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="68256-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : Protection des informations](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="68256-106">Lors de cette étape, vous allez définir les niveaux de sécurité et de protection de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68256-106">In this step, you'll define the levels of security and protection for your organization.</span></span> <span data-ttu-id="68256-107">Par exemple, un niveau de sécurité relativement faible peut suffire à votre service commercial.</span><span class="sxs-lookup"><span data-stu-id="68256-107">For example, your sales department might only require a low security level.</span></span> <span data-ttu-id="68256-108">En revanche, votre service de recherche et sa précieuse propriété intellectuelle nécessitent probablement un niveau de sécurité élevé avec chiffrage des fichiers et limitation d’accès au seul personnel de recherche.</span><span class="sxs-lookup"><span data-stu-id="68256-108">However, your research department and its highly valuable intellectual property might require a high security level that encrypts files and limits access to only research staff.</span></span>

<span data-ttu-id="68256-109">Bien que vous puissiez définir vos propres niveaux de sécurité et même si vous en avez déjà définis, Microsoft recommande d’élaborer un plan pour utiliser au moins trois niveaux de sécurité et de protection différents.</span><span class="sxs-lookup"><span data-stu-id="68256-109">Although you can define your own security levels and might already have some in place, Microsoft recommends that you develop a plan to use at least three different levels of security and protection that can be applied.</span></span> <span data-ttu-id="68256-110">Voici une liste pour commencer :</span><span class="sxs-lookup"><span data-stu-id="68256-110">Here is a list to get you started:</span></span> 

- <span data-ttu-id="68256-p103">**De base :** il s’agit d’un minimum standard pour la protection des données et pour les identités et les appareils qui accèdent à vos données. Vous pouvez suivre des recommandations de base en matière de sécurité et de protection pour fournir une protection par défaut forte qui répond aux besoins de nombreuses organisations ou de leurs services.</span><span class="sxs-lookup"><span data-stu-id="68256-p103">**Baseline:** This is a minimum standard for protecting data and for the identities and devices that access your data. You can follow baseline security and protection recommendations to provide strong default protection that meets the needs of many organizations or their departments.</span></span>
- <span data-ttu-id="68256-p104">**Sensible :** il s’agit d’une protection supplémentaire pour un sous-ensemble de vos données qui doivent être protégées au-delà du niveau de base. Vous pouvez appliquer cette protection accrue à des ensembles de données spécifiques dans votre environnement Microsoft 365. Microsoft recommande également d’appliquer le niveau de sécurité sensible aux identités et appareils qui accèdent aux données sensibles.</span><span class="sxs-lookup"><span data-stu-id="68256-p104">**Sensitive:** This is additional protection for a subset of your data that must be protected beyond the baseline level. You can apply this increased protection to specific data sets in your Microsoft 365 environment. Microsoft also recommends applying the sensitive security level to identities and devices that access sensitive data.</span></span>
- <span data-ttu-id="68256-p105">**Hautement réglementée :** il s’agit du niveau de protection le plus élevé pour les organisations qui ont généralement une très petite quantité de données hautement classées, considérées comme étant la propriété intellectuelle ou des secrets commerciaux, ou des données devant respecter des réglementations de sécurité strictes. Microsoft 365 Entreprise dispose de fonctionnalités pour aider les organisations à respecter ces exigences de sécurité élevé, avec notamment une protection équivalente pour les appareils et identités.</span><span class="sxs-lookup"><span data-stu-id="68256-p105">**Highly regulated:** This is the highest level of protection for organizations that typically have a very small amount of data that is highly classified, considered intellectual property or trade secrets, or data that must adhere to strict security regulations. Microsoft 365 Enterprise has capabilities to help organizations meet these high security requirements, including equivalent protection for identities and devices.</span></span>

<span data-ttu-id="68256-118">Pour en savoir plus, consultez la rubrique sur les [trois niveaux de protection](microsoft-365-policies-configurations.md#three-tiers-of-protection).</span><span class="sxs-lookup"><span data-stu-id="68256-118">For more information, see [Three tiers of protection](microsoft-365-policies-configurations.md#three-tiers-of-protection).</span></span>

<span data-ttu-id="68256-119">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step1) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="68256-119">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step1) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="68256-120">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="68256-120">Next step</span></span>

|||
|:-------|:-----|
|![Étape 2](../media/stepnumbers/Step2.png)|[<span data-ttu-id="68256-122">Configurer la classification pour votre environnement</span><span class="sxs-lookup"><span data-stu-id="68256-122">Configure classification for your environment</span></span>](infoprotect-configure-classification.md)|
