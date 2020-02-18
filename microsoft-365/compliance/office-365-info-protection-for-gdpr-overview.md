---
title: Protection des informations Office 365 pour le RGPD - Vue d’ensemble
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Obtenez une vue d’ensemble de la protection des informations Office 365 pour le RGPD. Apprenez à découvrir, classer, protéger et surveiller les données personnelles.
ms.openlocfilehash: dbb420cce572b2e03260f9f5b1be63e65504276b
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42071162"
---
# <a name="overview-of-office-365-information-protection-for-gdpr"></a><span data-ttu-id="2f796-104">Protection des informations Office 365 pour le RGPD - Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="2f796-104">Overview of Office 365 Information Protection for GDPR</span></span>

<span data-ttu-id="2f796-p102">Cette solution décrit comment protéger les données sensibles stockées dans les services Office 365. Elle inclut des recommandations normatives pour la découverte, la classification, la protection et la surveillance des données personnelles. Cette solution utilise le Règlement général sur la protection des données (RGPD) comme exemple, mais vous pouvez appliquer le même processus pour être conforme aux nombreux autres règlements.</span><span class="sxs-lookup"><span data-stu-id="2f796-p102">This solution demonstrates how to protect sensitive data that is stored in Office 365 services. It includes prescriptive recommendations for discovering, classifying, protecting, and monitoring personal data. This solution uses General Data Protection Regulation (GDPR) as an example, but you can apply the same process to achieve compliance with many other regulations.</span></span>

<span data-ttu-id="2f796-p103">Le RGPD réglemente la collecte, le stockage, le traitement et le partage des données personnelles. Les données personnelles sont définies à très grande échelle dans le cadre du RGPD comme les données associées à une personne naturelle identifiée ou identifiable qui est résidente de l’Union européenne (UE).</span><span class="sxs-lookup"><span data-stu-id="2f796-p103">GDPR regulates the collection, storage, processing, and sharing of personal data. Personal data is defined very broadly under the GDPR as any data that relates to an identified or identifiable natural person that is a resident of the European Union (EU).</span></span>

<span data-ttu-id="2f796-110">Article 4 - Définitions</span><span class="sxs-lookup"><span data-stu-id="2f796-110">Article 4 – Definitions</span></span>

> <span data-ttu-id="2f796-111">Les « données personnelles » correspondent aux informations relatives à une personne naturelle identifiée ou identifiable (« la personne concernée ») ; une personne naturelle identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne naturelle ;</span><span class="sxs-lookup"><span data-stu-id="2f796-111">‘personal data’ means any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person;</span></span>

<span data-ttu-id="2f796-p104">Cette solution a été conçue pour permettre aux organisations de découvrir et protéger les données personnelles dans Office 365 qui peuvent être soumises au RGPD. Elle n’est pas proposée comme attestation de conformité au RGPD. Les organisations doivent garantir elles-mêmes leur conformité au RGPD et sont invitées à consulter leurs équipes juridiques et de conformité ou à s’adresser à des tiers spécialisés dans le domaine de la conformité.</span><span class="sxs-lookup"><span data-stu-id="2f796-p104">This solution is intended to help organizations discover and protect personal data in Office 365 that might be subject to the GDPR. It is not offered as a GDPR compliance attestation. Organizations are responsible for ensuring their own GDPR compliance and are advised to consult their legal and compliance teams or to seek guidance and advice from third parties that specialize in compliance.</span></span>

<span data-ttu-id="2f796-115">L’outil d’[évaluation RGPD](https://www.microsoft.com/cyberassessment/en/gdpr/uso365?ls=Email&mkt_tok=eyJpIjoiTTJFeE5USXlOR1EwTWpJMiIsInQiOiJQTmdCYWR5NTlOd3JLWHZlb2NzNldKclQ4ZVBzVmhGeUhoUlFcL1pvSDIyXC9Ka05iTUR1aGpxT0YxQ0FUeGNDOUlkbWZLM1U4SUZWZmEyaGF6XC9ueUxkTHJzZnB3VDRMZlhPdkR4MzRLWkF5ckRNdWwxUkgzXC9yRU8yNkttSHhTb3VpZjNyVlJrNm9TTVZRYU5HR240a0FRPT0ifQ%3D%3D) est un outil rapide d’auto-évaluation en ligne, disponible gratuitement pour aider votre organisation à revoir son niveau de préparation global pour se conformer au RGPD.</span><span class="sxs-lookup"><span data-stu-id="2f796-115">[GDPR Assessment](https://www.microsoft.com/cyberassessment/en/gdpr/uso365?ls=Email&mkt_tok=eyJpIjoiTTJFeE5USXlOR1EwTWpJMiIsInQiOiJQTmdCYWR5NTlOd3JLWHZlb2NzNldKclQ4ZVBzVmhGeUhoUlFcL1pvSDIyXC9Ka05iTUR1aGpxT0YxQ0FUeGNDOUlkbWZLM1U4SUZWZmEyaGF6XC9ueUxkTHJzZnB3VDRMZlhPdkR4MzRLWkF5ckRNdWwxUkgzXC9yRU8yNkttSHhTb3VpZjNyVlJrNm9TTVZRYU5HR240a0FRPT0ifQ%3D%3D) is a quick, online self-evaluation tool available at no cost to help your organization review its overall level of readiness to comply with the GDPR.</span></span>

## <a name="assess-and-manage-your-compliance-risk"></a><span data-ttu-id="2f796-116">Évaluation et gestion des risques de conformité</span><span class="sxs-lookup"><span data-stu-id="2f796-116">Assess and manage your compliance risk</span></span>

<span data-ttu-id="2f796-p105">La première étape vers la conformité au RGPD consiste à évaluer si le RGPD s’applique à votre organisation et, si c’est le cas, dans quelle mesure. Cette analyse permet de comprendre les données traitées par votre organisation et l’endroit où elles résident.</span><span class="sxs-lookup"><span data-stu-id="2f796-p105">The first step towards GDPR compliance is to assess whether the GDPR applies to your organization, and, if so, to what extent. This analysis includes understanding the data your organization processes and where it resides.</span></span>

### <a name="step-1--use-compliance-score-to-view-the-regulation-requirements-and-track-your-progress"></a><span data-ttu-id="2f796-119">Étape 1 - Utilisez le Score de conformité pour afficher les exigences en matière de règlement et suivre votre progression</span><span class="sxs-lookup"><span data-stu-id="2f796-119">Step 1 — Use Compliance Score to view the regulation requirements and track your progress</span></span>

<span data-ttu-id="2f796-120">Le Score de conformité fournit des outils pour suivre, implémenter et gérer les contrôles d’audit qui permettent à votre organisation d’être conforme à différentes normes, notamment au RGPD.</span><span class="sxs-lookup"><span data-stu-id="2f796-120">Compliance Score provides tools to track, implement, and manage the auditing controls to help your organization reach compliance against various standards, including GDPR.</span></span>

![Utilisation du Score de conformité et le Gestionnaire de conformité pour afficher les exigences et suivre la progression](../media/Overview-image1.png)

<span data-ttu-id="2f796-122">Pour en savoir plus, consultez la section [Score de conformité](compliance-score.md).</span><span class="sxs-lookup"><span data-stu-id="2f796-122">For more information, see [Compliance Score](compliance-score.md).</span></span>

### <a name="step-2--use-content-search-and-sensitive-information-types-to-find-personal-data"></a><span data-ttu-id="2f796-123">Étape 2 - Utilisez la recherche de contenu et les types d’informations sensibles pour rechercher des données personnelles</span><span class="sxs-lookup"><span data-stu-id="2f796-123">Step 2 — Use Content Search and sensitive information types to find personal data</span></span> 

<span data-ttu-id="2f796-p106">Découvrez les données personnelles dans votre environnement qui sont soumises au RGPD. Utilisez la recherche de contenu avec des types d’informations sensibles pour :</span><span class="sxs-lookup"><span data-stu-id="2f796-p106">Discover personal data in your environment that is subject to the GDPR. Use Content Search together with sensitive information types to:</span></span>

- <span data-ttu-id="2f796-126">Rechercher et créer des rapports sur l’emplacement des données personnelles.</span><span class="sxs-lookup"><span data-stu-id="2f796-126">Find and report on where personal data resides.</span></span>

- <span data-ttu-id="2f796-127">Optimiser les types de données sensibles et d’autres requêtes pour rechercher toutes les données personnelles dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="2f796-127">Optimize sensitive data types and other queries to find all personal data in your environment.</span></span>

![Utilisation de la recherche de contenu et des types d’informations sensibles pour rechercher des données personnelles](../media/Overview-image2.png)

<span data-ttu-id="2f796-p107">Les types d’informations sensibles définissent la façon dont le processus automatisé reconnaît des types d’informations spécifiques tels que les numéros de sécurité sociale et les numéros de carte de crédit. Cet article inclut un ensemble de données que vous pouvez utiliser comme point de départ. De nombreux autres types d’informations sensibles seront prochainement disponibles pour les données personnelles dans les pays de l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="2f796-p107">Sensitive information types define how the automated process recognizes specific information types such as health service numbers and credit card numbers. This article includes a set you can use as a starting point. Many more sensitive information types are coming soon for personal data in EU countries.</span></span>

<span data-ttu-id="2f796-132">Pour plus d’informations, reportez-vous à la rubrique relative à la [recherche et à la localisation des données personnelles](search-for-and-find-personal-data.md).</span><span class="sxs-lookup"><span data-stu-id="2f796-132">For more information, see [Search for and find personal data](search-for-and-find-personal-data.md).</span></span> 

## <a name="classify-protect-and-monitor-personal-data-in-office-365-and-other-saas-apps"></a><span data-ttu-id="2f796-133">Classification, protection et surveillance des données personnelles dans Office 365 et d’autres applications SaaS</span><span class="sxs-lookup"><span data-stu-id="2f796-133">Classify, protect, and monitor personal data in Office 365 and other SaaS apps</span></span>

<span data-ttu-id="2f796-134">Certaines fonctionnalités utilisées pour la protection des informations dans Office 365 peuvent également servir à protéger les données sensibles dans d’autres applications SaaS.</span><span class="sxs-lookup"><span data-stu-id="2f796-134">Some of the capabilities used for information protection in Office 365 can also be used to protect sensitive data in other SaaS applications.</span></span>

![Classification, protection et surveillance des données personnelles](../media/Overview-image3.png)

<span data-ttu-id="2f796-136">Cette illustration est décrite dans le reste cette section (étapes 3 à 5).</span><span class="sxs-lookup"><span data-stu-id="2f796-136">This illustration is described by the rest this section (steps 3-5).</span></span>

### <a name="step-3--decide-if-you-want-to-use-labels-in-addition-to-sensitive-information-types"></a><span data-ttu-id="2f796-137">Étape 3 - Déterminez si vous voulez utiliser des étiquettes en plus des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="2f796-137">Step 3 — Decide if you want to use labels in addition to sensitive information types</span></span>

<span data-ttu-id="2f796-p108">Les types d’informations sensibles constituent une forme de classification. Reportez-vous à la rubrique relative à la [création d’un schéma de classification pour les données personnelles](architect-a-classification-schema-for-personal-data.md) pour décider si vous souhaitez implémenter des étiquettes également. Pour appliquer des étiquettes, reportez-vous à la rubrique relative à l’[application d’étiquettes à des données personnelles dans Office 365](apply-labels-to-personal-data-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="2f796-p108">Sensitive information types are a form of classification. See [Architect a classification schema for personal data](architect-a-classification-schema-for-personal-data.md), to decide if you also want to implement labels. To apply labels, see [Apply labels to personal data in Office 365](apply-labels-to-personal-data-in-office-365.md).</span></span>

<span data-ttu-id="2f796-p109">Dans l’illustration, des étiquettes et types d’informations sensibles sont utilisés dans Office 365. Bientôt, vous pourrez les utiliser avec Cloud App Security pour rechercher des données sensibles dans d’autres applications SaaS, telles que Box et Salesforce.</span><span class="sxs-lookup"><span data-stu-id="2f796-p109">In the illustration, sensitive information types and labels work across Office 365. Coming soon, you can use these with Cloud App Security to find sensitive data in other SaaS apps, such as Box and Salesforce.</span></span>

### <a name="step-4--protect-personal-data-in-office-365"></a><span data-ttu-id="2f796-143">Étape 4 - Protégez des données personnelles dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2f796-143">Step 4 — Protect personal data in Office 365</span></span> 

<span data-ttu-id="2f796-p110">La protection des données personnelles commence par la prévention contre la perte de données Office 365. Il existe plusieurs autres fonctionnalités recommandées pour protéger l’accès aux données personnelles, notamment le chiffrement de messages Office 365 pour le courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="2f796-p110">Protection for personal data starts with Office 365 data loss prevention. There are several other capabilities recommended for protecting access to personal data, including Office 365 Message Encryption for email.</span></span>

<span data-ttu-id="2f796-146">Ces protections peuvent cibler des ensembles de données spécifiques :</span><span class="sxs-lookup"><span data-stu-id="2f796-146">These protections can be targeted to specific data sets:</span></span>

- <span data-ttu-id="2f796-147">Autorisations au niveau de la bibliothèque et du site</span><span class="sxs-lookup"><span data-stu-id="2f796-147">Site and library-level permissions</span></span>

- <span data-ttu-id="2f796-148">Stratégies de partage externe au niveau du site</span><span class="sxs-lookup"><span data-stu-id="2f796-148">Site-level external sharing policies</span></span>

- <span data-ttu-id="2f796-149">Stratégies d’accès d’appareil au niveau du site</span><span class="sxs-lookup"><span data-stu-id="2f796-149">Site-level device access policies</span></span>

<span data-ttu-id="2f796-150">La protection pour l’accès à Office 365 et les autres services cloud comprend :</span><span class="sxs-lookup"><span data-stu-id="2f796-150">Protection for access to Office 365 and other cloud services include:</span></span>

- <span data-ttu-id="2f796-151">Protection des identités et protection d’accès d’appareil dans Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="2f796-151">Identity and device access protection in Enterprise Mobility + Security (EMS)</span></span>

- <span data-ttu-id="2f796-152">Gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="2f796-152">Privileged access management</span></span>

- <span data-ttu-id="2f796-153">Fonctionnalités de sécurité Windows 10</span><span class="sxs-lookup"><span data-stu-id="2f796-153">Windows 10 security capabilities</span></span>

<span data-ttu-id="2f796-154">Pour plus d’informations sur l’application de la protection, reportez-vous à la rubrique relative à l’[application de la protection aux données personnelles dans Office 365](apply-protection-to-personal-data-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="2f796-154">For more information about applying proteciton, see [Apply protection to personal data in Office 365](apply-protection-to-personal-data-in-office-365.md).</span></span>

### <a name="step-5--monitor-for-leaks-of-personal-data"></a><span data-ttu-id="2f796-155">Étape 5 - Surveillez les fuites de données personnelles</span><span class="sxs-lookup"><span data-stu-id="2f796-155">Step 5 — Monitor for leaks of personal data</span></span>

<span data-ttu-id="2f796-p111">Les rapports sur la protection contre la perte de données Office 365 fournissent les informations les plus détaillées concernant la surveillance des données sensibles. Vous pouvez configurer des alertes automatisées et examiner les violations de données à l’aide du journal d’audit Office 365. Cloud App Security étend la possibilité de rechercher et de surveiller les données sensibles à d’autres fournisseurs SaaS. Pour plus d’informations sur ces outils, reportez-vous à la rubrique relative à la [surveillance des atteintes à la sécurité des données personnelles](/security/office-365-security/monitor-for-leaks-of-personal-data.md).</span><span class="sxs-lookup"><span data-stu-id="2f796-p111">Office 365 data loss prevention reports provide the greatest level of detail for monitoring sensitive data. You can setup automated alerts and investigate breaches by using the Office 365 audit log. Cloud App Security extends the ability to find and monitor sensitive data to other SaaS providers. For more information on these tools, see [Monitor for breaches of personal data](/security/office-365-security/monitor-for-leaks-of-personal-data.md).</span></span>
