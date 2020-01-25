---
title: ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations
description: Les services Cloud Microsoft ont mis en œuvre ce code de pratique pour les contrôles de sécurité des informations.
keywords: Offres pour la conformité Microsoft 365
localization_priority: Priority
ms.prod: Microsoft-365-enterprise
ms.topic: article
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: M365-security-compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 758e7d0f3e82afa6cfd4b90501bd84080d8f6303
ms.sourcegitcommit: 3dca80f268006658a0b721aa4f6df1224c7964dc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "41260012"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a><span data-ttu-id="4dd5e-104">ISO/IEC 27017:2015 Code de pratique international des contrôles de sécurité des informations</span><span class="sxs-lookup"><span data-stu-id="4dd5e-104">ISO/IEC 27017:2015 Code of Practice for Information Security Controls</span></span>

## <a name="iso-iec-27017-overview"></a><span data-ttu-id="4dd5e-105">Présentation d’ISO-IEC 27017</span><span class="sxs-lookup"><span data-stu-id="4dd5e-105">ISO-IEC 27017 Overview</span></span>

<span data-ttu-id="4dd5e-106">Le code de pratique ISO/IEC 27017:2015 est conçu comme une référence permettant aux entreprises de sélectionner les contrôles de sécurité des informations des services Cloud lors de la mise en œuvre d’un système de gestion de la sécurité des informations de Cloud computing basé sur la norme ISO/IEC 27002:2013.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-106">The ISO/IEC 27017:2015 code of practice is designed for organizations to use as a reference for selecting cloud services information security controls when implementing a cloud computing information security management system based on ISO/IEC 27002:2013.</span></span> <span data-ttu-id="4dd5e-107">Il peut être également utilisé par les fournisseurs de services cloud comme document de référence pour l'implémentation des contrôles de protection communément admis.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-107">It can also be used by cloud service providers as a guidance document for implementing commonly accepted protection controls.</span></span>

<span data-ttu-id="4dd5e-108">Cette norme internationale fournit des conseils d'implémentation supplémentaires spécifiques au cloud basés sur la norme ISO/IEC 27002, et fournit des contrôles supplémentaires pour traiter les menaces et les risques de sécurité des informations spécifiques au cloud conformément aux clauses 5 à18 de la norme ISO/IEC 27002: 2013 pour les contrôles, des conseils d'implémentation, ainsi que d'autres informations.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-108">This international standard provides additional cloud-specific implementation guidance based on ISO/IEC 27002, and provides additional controls to address cloud-specific information security threats and risks referring to clauses 5–18 in ISO/IEC 27002: 2013 for controls, implementation guidance, and other information.</span></span> <span data-ttu-id="4dd5e-109">Plus précisément, cette norme fournit des conseils sur les 37 contrôles de la norme ISO/IEC 27002 et contient également 7 nouveaux contrôles non dupliqués dans la norme ISO/IEC 27002.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-109">Specifically, this standard provides guidance on 37 controls in ISO/IEC 27002, and it also features seven new controls that are not duplicated in ISO/IEC 27002.</span></span> <span data-ttu-id="4dd5e-110">Ces nouvelles commandes traitent des aspects importants suivants :</span><span class="sxs-lookup"><span data-stu-id="4dd5e-110">These new controls address the following important areas:</span></span>

- <span data-ttu-id="4dd5e-111">Rôles et responsabilités partagés dans un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="4dd5e-111">Shared roles and responsibilities within a cloud computing environment</span></span>
- <span data-ttu-id="4dd5e-112">Retrait et restitution des biens des clients des services cloud à la fin du contrat</span><span class="sxs-lookup"><span data-stu-id="4dd5e-112">Removal and return of cloud service customer assets upon contract termination</span></span>
- <span data-ttu-id="4dd5e-113">Protection et séparation de l'environnement virtuel d'un client de celui des autres clients</span><span class="sxs-lookup"><span data-stu-id="4dd5e-113">Protection and separation of a customer’s virtual environment from that of other customers</span></span>
- <span data-ttu-id="4dd5e-114">Durcissement des exigences des machines virtuelles pour répondre aux besoins des entreprises</span><span class="sxs-lookup"><span data-stu-id="4dd5e-114">Virtual machine hardening requirements to meet business needs</span></span>
- <span data-ttu-id="4dd5e-115">Procédures pour les opérations administratives d'un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="4dd5e-115">Procedures for administrative operations of a cloud computing environment</span></span>
- <span data-ttu-id="4dd5e-116">Possibilité donnée aux clients de surveiller les activités pertinentes dans un environnement de cloud computing</span><span class="sxs-lookup"><span data-stu-id="4dd5e-116">Enabling customers to monitor relevant activities within a cloud computing environment</span></span>
- <span data-ttu-id="4dd5e-117">Alignement de la gestion de la sécurité pour les réseaux virtuels et physiques</span><span class="sxs-lookup"><span data-stu-id="4dd5e-117">Alignment of security management for virtual and physical networks</span></span>

## <a name="microsoft-and-isoiec-27017"></a><span data-ttu-id="4dd5e-118">Microsoft et la norme ISO/IEC 27017</span><span class="sxs-lookup"><span data-stu-id="4dd5e-118">Microsoft and ISO/IEC 27017</span></span>

<span data-ttu-id="4dd5e-119">La norme ISO/IEC 27017 est la seule à fournir des conseils à la fois aux fournisseurs et aux clients des services Cloud.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-119">ISO/IEC 27017 is unique in providing guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="4dd5e-120">Elle fournit également aux clients des services cloud des informatiques pratiques sur ce à quoi ils doivent s'attendre de la part des fournisseurs de services cloud.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-120">It also provides cloud service customers with practical information on what they should expect from cloud service providers.</span></span> <span data-ttu-id="4dd5e-121">Les clients peuvent tirer parti directement de la norme ISO/IEC 27017 en s’assurant qu’ils ont bien compris les responsabilités partagées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-121">Customers can benefit directly from ISO/IEC 27017 by ensuring they understand the shared responsibilities in the cloud.</span></span>

<span data-ttu-id="4dd5e-122">Découvrez les avantages de la norme ISO/IEC 27017 sur le Microsoft Cloud : [Télécharger la norme ISO/IEC 27017 : Code de pratique pour les contrôles de sécurité des données](https://aka.ms/iso27017-backgrounder)</span><span class="sxs-lookup"><span data-stu-id="4dd5e-122">Learn about the benefits of ISO/IEC 27017 on the Microsoft Cloud: [Download the ISO/IEC 27017: Code of Practice for Information Security Controls](https://aka.ms/iso27017-backgrounder)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="4dd5e-123">Services Cloud Microsoft dans le périmètre</span><span class="sxs-lookup"><span data-stu-id="4dd5e-123">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="4dd5e-124">Azure, Azure Gouvernement et Azure Allemagne</span><span class="sxs-lookup"><span data-stu-id="4dd5e-124">Azure, Azure Government, and Azure Germany</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="4dd5e-125">Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="4dd5e-125">Cloud App Security</span></span>
- [<span data-ttu-id="4dd5e-126">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-126">Dynamics 365</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="4dd5e-127">Génomique</span><span class="sxs-lookup"><span data-stu-id="4dd5e-127">Genomics</span></span>
- <span data-ttu-id="4dd5e-128">Graph</span><span class="sxs-lookup"><span data-stu-id="4dd5e-128">Graph</span></span>
- <span data-ttu-id="4dd5e-129">Intune</span><span class="sxs-lookup"><span data-stu-id="4dd5e-129">Intune</span></span>
- <span data-ttu-id="4dd5e-130">Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="4dd5e-130">Microsoft Managed Desktop</span></span>
- <span data-ttu-id="4dd5e-131">Service Cloud Microsoft Flow, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-131">Microsoft Flow cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="4dd5e-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense et Office 365 Allemagne</span><span class="sxs-lookup"><span data-stu-id="4dd5e-132">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, and Office 365 Germany</span></span>
- <span data-ttu-id="4dd5e-133">Service Cloud Microsoft PowerApps, soit en service autonome, soit inclus dans un plan ou une suite Office 365 ou Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-133">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="4dd5e-134">Service Cloud Power BI soit en service autonome, soit inclus dans un plan ou une suite Office 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-134">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- <span data-ttu-id="4dd5e-135">Consultez une [liste détaillée](https://go.microsoft.com/fwlink/p/?linkid=2077751) des services couverts dans Office 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-135">See a [detailed list](https://go.microsoft.com/fwlink/p/?linkid=2077751) of covered services in Office 365</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="4dd5e-136">Audits, rapports et certificats</span><span class="sxs-lookup"><span data-stu-id="4dd5e-136">Audits, reports, and certificates</span></span>

<span data-ttu-id="4dd5e-137">Les services Cloud Microsoft font l’objet d’un audit une fois par an pour le code de pratique ISO/IEC 27017:2015 dans le cadre du processus de certification pour ISO/IEC 27001:2013.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-137">Microsoft cloud services are audited once a year for the ISO/IEC 27017:2015 code of practice as part of the certification process for ISO/IEC 27001:2013.</span></span>

- [<span data-ttu-id="4dd5e-138">Certificat ISO 27017 Azure</span><span class="sxs-lookup"><span data-stu-id="4dd5e-138">Azure ISO 27017 Certificate</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2078005)
- [<span data-ttu-id="4dd5e-139">Rapport d’évaluation d’Azure ISO 27017</span><span class="sxs-lookup"><span data-stu-id="4dd5e-139">Azure ISO 27017 Assessment report</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2078010)
- [<span data-ttu-id="4dd5e-140">Déclaration d'applicabilité ISO 27017 Azure</span><span class="sxs-lookup"><span data-stu-id="4dd5e-140">Azure ISO 27017 Statement of Applicability</span></span>](https://aka.ms/AzureISO27017StatementofApplicability)
- [<span data-ttu-id="4dd5e-141">Rapport d'évaluation d'audit ISO 27001, 27018 et 27017 Office 365</span><span class="sxs-lookup"><span data-stu-id="4dd5e-141">Office 365 ISO 27001, 27018, and 27017 Audit Assessment Report</span></span>](https://aka.ms/o365isoreport)

## <a name="frequently-asked-questions"></a><span data-ttu-id="4dd5e-142">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="4dd5e-142">Frequently asked questions</span></span>

<span data-ttu-id="4dd5e-143">À qui la norme s'applique-t-elle ?</span><span class="sxs-lookup"><span data-stu-id="4dd5e-143">To whom does the standard apply?</span></span>

<span data-ttu-id="4dd5e-144">Ce code de pratique fournit des contrôles et des conseils de mise en œuvre aux fournisseurs de services Cloud et à leurs clients.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-144">This code of practice provides controls and implementation guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="4dd5e-145">Il se présente sous la même forme que la norme ISO/IEC 27002:2013.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-145">It is structured in a format similar to ISO/IEC 27002:2013.</span></span>

<span data-ttu-id="4dd5e-146">**Où puis-je consulter les informations de conformité de Microsoft concernant la norme ISO/IEC 27017:2015 ?**</span><span class="sxs-lookup"><span data-stu-id="4dd5e-146">**Where can I view Microsoft’s compliance information for ISO/IEC 27017:2015?**</span></span>

<span data-ttu-id="4dd5e-147">Vous pouvez télécharger le certificat [ISO/IEC 27017:2015](https://aka.ms/azureiso27017) pour Azure, Intune et Power BI.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-147">You can download the [ISO/IEC 27017:2015 certificate](https://aka.ms/azureiso27017) for Azure, Intune, and Power BI.</span></span>

<span data-ttu-id="4dd5e-148">**Puis-je tirer profit de la conformité ISO/IEC 27017 des services Microsoft dans le processus de certification de mon entreprise ?**</span><span class="sxs-lookup"><span data-stu-id="4dd5e-148">**Can I use the ISO/IEC 27017 compliance of Microsoft services in my organization’s certification process?**</span></span>

<span data-ttu-id="4dd5e-149">Oui.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-149">Yes.</span></span> <span data-ttu-id="4dd5e-150">Si votre entreprise cherche une certification pour des implémentations déployées sur tous services Enterprise Cloud de Microsoft dans le périmètre, vous pouvez utiliser la certification pertinente de Microsoft dans votre évaluation de la conformité.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-150">If your business is seeking certification for implementations deployed on any Microsoft in-scope enterprise cloud services, you can use Microsoft’s relevant certifications in your compliance assessment.</span></span> <span data-ttu-id="4dd5e-151">Il vous incombe néanmoins d’engager un évaluateur pour mesurer votre mise en œuvre de la conformité, ainsi que des contrôles et des processus au sein de votre propre organisation.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-151">However, you are responsible for engaging an assessor to evaluate your implementation for compliance, and for the controls and processes within your own organization.</span></span>

<span data-ttu-id="4dd5e-152">**Comment puis-je me procurer des copies des rapports d’audit applicables ?**</span><span class="sxs-lookup"><span data-stu-id="4dd5e-152">**How can I get copies of the applicable audit reports?**</span></span>

<span data-ttu-id="4dd5e-153">Le [portail d'approbation de services](https://aka.ms/stphelp) fournit des rapports d'audit indépendants et tiers, ainsi que toute autre documentation.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-153">The [Service Trust Portal](https://aka.ms/stphelp) provides independent, third-party audit reports and other related documentation.</span></span> <span data-ttu-id="4dd5e-154">Vous pouvez utiliser le portail pour télécharger et examiner cette documentation afin d’obtenir de l’aide concernant vos propres exigences légales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="4dd5e-154">You can use the portal to download and review this documentation for assistance with your own regulatory requirements.</span></span>

## <a name="resources"></a><span data-ttu-id="4dd5e-155">Ressources</span><span class="sxs-lookup"><span data-stu-id="4dd5e-155">Resources</span></span>

- [<span data-ttu-id="4dd5e-156">Code de pratique ISO/IEC 27017:2015</span><span class="sxs-lookup"><span data-stu-id="4dd5e-156">ISO/IEC 27017:2015 code of practice</span></span>](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [<span data-ttu-id="4dd5e-157">Conditions de Microsoft Online Services</span><span class="sxs-lookup"><span data-stu-id="4dd5e-157">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="4dd5e-158">Conformité du Centre de gestion de la confidentialité Microsoft</span><span class="sxs-lookup"><span data-stu-id="4dd5e-158">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)

## <a name="download-the-offering-backgrounder"></a><span data-ttu-id="4dd5e-159">Télécharger notre document d’information sur la conformité</span><span class="sxs-lookup"><span data-stu-id="4dd5e-159">Download the offering backgrounder</span></span>

<span data-ttu-id="4dd5e-160">Vous souhaitez en savoir plus sur nos démarches concernant la conformité ?</span><span class="sxs-lookup"><span data-stu-id="4dd5e-160">Do you need the backgrounder document for this offering?</span></span> <span data-ttu-id="4dd5e-161">Téléchargez notre fichier [PDF](https://download.microsoft.com/download/7/7/9/7799D02B-A97A-48E0-A057-C19DD543BB24/ISO-IEC-27017_backgrounder.pdf) (disponible uniquement en anglais pour le moment).</span><span class="sxs-lookup"><span data-stu-id="4dd5e-161">Download the [PDF](https://download.microsoft.com/download/7/7/9/7799D02B-A97A-48E0-A057-C19DD543BB24/ISO-IEC-27017_backgrounder.pdf).</span></span>
