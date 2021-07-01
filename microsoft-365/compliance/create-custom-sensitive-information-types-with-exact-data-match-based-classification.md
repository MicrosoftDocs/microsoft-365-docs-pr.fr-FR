---
title: Créer des types d’informations sensibles personnalisés à l’aide du classifieur Exact Data Match
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: ''
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment créer des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: e8f6c075d706da46d7163705f6aa9d0ca6cad1a2
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53227126"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a><span data-ttu-id="7d636-103">Créez des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.</span><span class="sxs-lookup"><span data-stu-id="7d636-103">Create custom sensitive information types with Exact Data Match based classification</span></span>



<span data-ttu-id="7d636-104">[Les types d’informations sensibles personnalisés](sensitive-information-type-learn-about.md) sont utilisés pour vous aider à identifier les éléments sensibles afin de pouvoir empêcher leur partage par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="7d636-104">[Custom sensitive information types](sensitive-information-type-learn-about.md) are used to help identify sensitive items so that you can prevent them from being inadvertently or inappropriately shared.</span></span> <span data-ttu-id="7d636-105">Vous définissez un type d’informations sensibles personnalisé (SIT) basé sur :</span><span class="sxs-lookup"><span data-stu-id="7d636-105">You define a custom sensitive information type (SIT)based on:</span></span>

- <span data-ttu-id="7d636-106">modèles</span><span class="sxs-lookup"><span data-stu-id="7d636-106">patterns</span></span>
- <span data-ttu-id="7d636-107">mots clés de preuve, tels que *employé*,*badge* ou *ID*</span><span class="sxs-lookup"><span data-stu-id="7d636-107">keyword evidence such as *employee*, *badge*, or *ID*</span></span>
- <span data-ttu-id="7d636-108">caractère à proximité de la preuve dans un modèle particulier</span><span class="sxs-lookup"><span data-stu-id="7d636-108">character proximity to evidence in a particular pattern</span></span>
- <span data-ttu-id="7d636-109">niveaux de confiance</span><span class="sxs-lookup"><span data-stu-id="7d636-109">confidence levels</span></span>

 <span data-ttu-id="7d636-110">De tels types d’informations sensibles personnalisés répondent aux besoins métier de nombreuses organisations.</span><span class="sxs-lookup"><span data-stu-id="7d636-110">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="7d636-111">Mais que se passe-t-il si vous voulez utiliser un type d’informations sensibles personnalisé qui utilise des valeurs de données exactes, au lieu d’un type qui établissait des correspondances avec des modèles génériques ?</span><span class="sxs-lookup"><span data-stu-id="7d636-111">But what if you wanted a custom sensitive information type (SIT) that uses exact data values, instead of one that found matches based on generic patterns?</span></span> <span data-ttu-id="7d636-112">Une classification Exact Data Match (EDM) vous permet de créer un type d’informations sensibles personnalisé conçu pour :</span><span class="sxs-lookup"><span data-stu-id="7d636-112">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>

- <span data-ttu-id="7d636-113">être dynamique et actualisé facilement ;</span><span class="sxs-lookup"><span data-stu-id="7d636-113">be dynamic and easily refreshed</span></span>
- <span data-ttu-id="7d636-114">être plus évolutif ;</span><span class="sxs-lookup"><span data-stu-id="7d636-114">be more scalable</span></span>
- <span data-ttu-id="7d636-115">entraîner moins de faux positifs ;</span><span class="sxs-lookup"><span data-stu-id="7d636-115">result in fewer false-positives</span></span>
- <span data-ttu-id="7d636-116">utiliser des données sensibles structurées ;</span><span class="sxs-lookup"><span data-stu-id="7d636-116">work with structured sensitive data</span></span>
- <span data-ttu-id="7d636-117">gérer les informations sensibles de manière plus sécurisée ;</span><span class="sxs-lookup"><span data-stu-id="7d636-117">handle sensitive information more securely</span></span>
- <span data-ttu-id="7d636-118">être utilisé avec différents services de cloud computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d636-118">be used with several Microsoft cloud services</span></span>

![Classification EDM](../media/EDMClassification.png)

<span data-ttu-id="7d636-120">La classification EDM vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-120">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="7d636-121">La base de données peut être actualisée quotidiennement et peut contenir jusqu’à 100 millions de lignes de données.</span><span class="sxs-lookup"><span data-stu-id="7d636-121">The database can be refreshed daily, and contain up to 100 million rows of data.</span></span> <span data-ttu-id="7d636-122">À mesure que des employés, patients ou clients vont et viennent, et que les enregistrements changent, vos types d’informations sensibles personnalisés restent à jour et valides.</span><span class="sxs-lookup"><span data-stu-id="7d636-122">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="7d636-123">Vous pouvez également utiliser la classification basée sur EDM avec des stratégies, telles [que les stratégies de protection contre la perte de données](dlp-learn-about-dlp.md) ou [les stratégies de fichier de Microsoft Cloud App Security](/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="7d636-123">And, you can use EDM-based classification with policies, such as [data loss prevention policies](dlp-learn-about-dlp.md) or [Microsoft Cloud App Security file policies](/cloud-app-security/data-protection-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-124">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="7d636-124">Microsoft 365 Information Protection supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="7d636-125">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="7d636-125">Chinese (simplified)</span></span>
> - <span data-ttu-id="7d636-126">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="7d636-126">Chinese (traditional)</span></span>
> - <span data-ttu-id="7d636-127">Korean</span><span class="sxs-lookup"><span data-stu-id="7d636-127">Korean</span></span>
> - <span data-ttu-id="7d636-128">Japanese</span><span class="sxs-lookup"><span data-stu-id="7d636-128">Japanese</span></span>
> 
> <span data-ttu-id="7d636-129">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-129">This support is available for sensitive information types.</span></span> <span data-ttu-id="7d636-130">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="7d636-130">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>
 

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="7d636-131">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="7d636-131">Required licenses and permissions</span></span>

<span data-ttu-id="7d636-132">Pour effectuer les tâches décrites dans cet article, vous devez être un administrateur général, un administrateur de conformité ou un administrateur Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="7d636-132">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="7d636-133">Pour en avoir plus sur les autorisations DLP, consultez la section[Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="7d636-133">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

<span data-ttu-id="7d636-134">La classification EDM est incluse dans ces abonnements</span><span class="sxs-lookup"><span data-stu-id="7d636-134">EDM-based classification is included in these subscriptions</span></span>

- <span data-ttu-id="7d636-135">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="7d636-135">Office 365 E5</span></span>
- <span data-ttu-id="7d636-136">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="7d636-136">Microsoft 365 E5</span></span>
- <span data-ttu-id="7d636-137">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="7d636-137">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="7d636-138">Microsoft E5/A5 Information Protection et gouvernance</span><span class="sxs-lookup"><span data-stu-id="7d636-138">Microsoft E5/A5 Information Protection and Governance</span></span>

## <a name="portal-links-for-your-subscription"></a><span data-ttu-id="7d636-139">Liens vers les portails de votre abonnement</span><span class="sxs-lookup"><span data-stu-id="7d636-139">Portal links for your subscription</span></span>


|<span data-ttu-id="7d636-140">Portail</span><span class="sxs-lookup"><span data-stu-id="7d636-140">Portal</span></span>  |<span data-ttu-id="7d636-141">World Wide/GCC</span><span class="sxs-lookup"><span data-stu-id="7d636-141">World Wide/GCC</span></span>  |<span data-ttu-id="7d636-142">GCC-High</span><span class="sxs-lookup"><span data-stu-id="7d636-142">GCC-High</span></span>  |<span data-ttu-id="7d636-143">DOD</span><span class="sxs-lookup"><span data-stu-id="7d636-143">DOD</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="7d636-144">Office SCC</span><span class="sxs-lookup"><span data-stu-id="7d636-144">Office SCC</span></span>     |  <span data-ttu-id="7d636-145">protection.office.com</span><span class="sxs-lookup"><span data-stu-id="7d636-145">protection.office.com</span></span>       |<span data-ttu-id="7d636-146">scc.office365.us</span><span class="sxs-lookup"><span data-stu-id="7d636-146">scc.office365.us</span></span>         |<span data-ttu-id="7d636-147">scc.protection.apps.mil</span><span class="sxs-lookup"><span data-stu-id="7d636-147">scc.protection.apps.mil</span></span> |
|<span data-ttu-id="7d636-148">Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7d636-148">Microsoft 365 Security center</span></span>     |<span data-ttu-id="7d636-149">security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7d636-149">security.microsoft.com</span></span>         |<span data-ttu-id="7d636-150">security.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="7d636-150">security.microsoft.us</span></span>         |<span data-ttu-id="7d636-151">security.apps.mil</span><span class="sxs-lookup"><span data-stu-id="7d636-151">security.apps.mil</span></span>|
|<span data-ttu-id="7d636-152">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7d636-152">Microsoft 365 Compliance center</span></span>     |<span data-ttu-id="7d636-153">compliance.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="7d636-153">compliance.microsoft.com</span></span>         |<span data-ttu-id="7d636-154">compliance.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="7d636-154">compliance.microsoft.us</span></span>         |<span data-ttu-id="7d636-155">compliance.apps.mil</span><span class="sxs-lookup"><span data-stu-id="7d636-155">compliance.apps.mil</span></span>|


## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="7d636-156">Flux de travail en un clin d’œil</span><span class="sxs-lookup"><span data-stu-id="7d636-156">The work flow at a glance</span></span>

|<span data-ttu-id="7d636-157">Phase</span><span class="sxs-lookup"><span data-stu-id="7d636-157">Phase</span></span>  |<span data-ttu-id="7d636-158">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="7d636-158">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="7d636-159">Partie 1: configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-159">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="7d636-160">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="7d636-160">(As needed)</span></span><br/><span data-ttu-id="7d636-161">- [Modifier le schéma de base de données](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="7d636-161">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="7d636-162">- [Supprimer le schéma](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="7d636-162">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="7d636-163">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-163">- Read access to the sensitive data</span></span><br/><span data-ttu-id="7d636-164">-Schéma de base de données au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="7d636-164">- Database schema in XML format (example provided)</span></span><br/><span data-ttu-id="7d636-165">-Package de règles au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="7d636-165">- Rule package in XML format (example provided)</span></span><br/><span data-ttu-id="7d636-166">-Autorisations d’administrateur sur le centre de sécurité & conformité (à l’aide de PowerShell)</span><span class="sxs-lookup"><span data-stu-id="7d636-166">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="7d636-167">Partie 2 : hacher et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-167">Part 2: Hash and upload the sensitive data</span></span>](#part-2-hash-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="7d636-168">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="7d636-168">(As needed)</span></span><br/>[<span data-ttu-id="7d636-169">Actualiser les données</span><span class="sxs-lookup"><span data-stu-id="7d636-169">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="7d636-170">-Groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7d636-170">- Custom security group and user account</span></span><br/><span data-ttu-id="7d636-171">-Accès administrateur local à l’ordinateur à l’aide de l’agent de téléchargement EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-171">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="7d636-172">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-172">- Read access to the sensitive data</span></span><br/><span data-ttu-id="7d636-173">-Processus et planification pour l’actualisation des données</span><span class="sxs-lookup"><span data-stu-id="7d636-173">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="7d636-174">Partie 3: utiliser la classification EDM avec vos services Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d636-174">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="7d636-175">- Abonnement Microsoft 365 avec DLP</span><span class="sxs-lookup"><span data-stu-id="7d636-175">- Microsoft 365 subscription with DLP</span></span><br/><span data-ttu-id="7d636-176">- Fonctionnalité de classification EDM activée</span><span class="sxs-lookup"><span data-stu-id="7d636-176">- EDM-based classification feature enabled</span></span> |

### <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="7d636-177">Partie 1 : configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-177">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="7d636-178">La configuration de la classification basée sur EDM inclut les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d636-178">Setting up and configuring EDM-based classification involves:</span></span>

1. [<span data-ttu-id="7d636-179">Enregistrement de données sensibles au format .csv ou .tsv</span><span class="sxs-lookup"><span data-stu-id="7d636-179">Saving sensitive data in .csv or .tsv format</span></span>](#save-sensitive-data-in-csv-or-tsv-format)
2. [<span data-ttu-id="7d636-180">Définition de votre schéma de base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-180">Define your sensitive information database schema</span></span>](#define-the-schema-for-your-database-of-sensitive-information)
3. [<span data-ttu-id="7d636-181">Création d’un package de règles</span><span class="sxs-lookup"><span data-stu-id="7d636-181">Create a rule package</span></span>](#set-up-a-rule-package)


#### <a name="save-sensitive-data-in-csv-or-tsv-format"></a><span data-ttu-id="7d636-182">Enregistrer des données sensibles au format .csv format .tsv ou .tsv</span><span class="sxs-lookup"><span data-stu-id="7d636-182">Save sensitive data in .csv or .tsv format</span></span>

1. <span data-ttu-id="7d636-183">Identifiez les informations sensibles que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="7d636-183">Identify the sensitive information you want to use.</span></span> <span data-ttu-id="7d636-184">Exportez les données vers une application, telle que Microsoft Excel, et enregistrez le fichier dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="7d636-184">Export the data to an app, such as Microsoft Excel, and save the file in a text file.</span></span> <span data-ttu-id="7d636-185">Le fichier peut être enregistré au format .csv (valeurs séparées par des virgules), .tsv (valeurs séparées par des tabulations) ou séparés par des |.</span><span class="sxs-lookup"><span data-stu-id="7d636-185">The file can be saved in .csv (comma-separated values), .tsv (tab-separated values), or pipe-separated (|) format.</span></span> <span data-ttu-id="7d636-186">Le format .tsv est recommandé dans les cas où vos valeurs de données peuvent inclure des virgules, telles que des adresses postales.</span><span class="sxs-lookup"><span data-stu-id="7d636-186">The .tsv format is recommended in cases where your data values may included commas, such as street addresses.</span></span>
<span data-ttu-id="7d636-187">Le fichier de données peut inclure au maximum :</span><span class="sxs-lookup"><span data-stu-id="7d636-187">The data file can include a maximum of:</span></span>
      - <span data-ttu-id="7d636-188">100 millions de lignes de données sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-188">Up to 100 million rows of sensitive data</span></span>
      - <span data-ttu-id="7d636-189">32 colonnes (champs) par source de données</span><span class="sxs-lookup"><span data-stu-id="7d636-189">Up to 32 columns (fields) per data source</span></span>
      - <span data-ttu-id="7d636-190">5 colonnes (champs) marquées comme pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="7d636-190">Up to 5 columns (fields) marked as searchable</span></span>

2. <span data-ttu-id="7d636-191">Structurez les données sensibles dans le fichier .csv ou .tsv afin que la première ligne comprenne les noms des champs utilisés pour la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="7d636-191">Structure the sensitive data in the .csv or .tsv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="7d636-192">Dans votre fichier, vous pouvez avoir des noms de champ tels que « ssn », « birthdate », « firstname », « lastname ».</span><span class="sxs-lookup"><span data-stu-id="7d636-192">In your file you might have field names such as "ssn", "birthdate", "firstname", "lastname".</span></span> <span data-ttu-id="7d636-193">Les noms d’en-tête de colonne ne peuvent pas contenir des espaces ni des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="7d636-193">The column header names can't include spaces or underscores.</span></span> <span data-ttu-id="7d636-194">Par exemple, le fichier .csv utilisé dans cet exemple est appelé *PatientRecords.csv*. Ses colonnes incluent *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN*, etc.</span><span class="sxs-lookup"><span data-stu-id="7d636-194">For example, the sample .csv file that we use in this article is named *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN*, and more.</span></span>

3. <span data-ttu-id="7d636-195">Prêtez attention au format des champs de données sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-195">Pay attention to the format of the sensitive data fields.</span></span> <span data-ttu-id="7d636-196">En particulier, les champs qui peuvent contenir des virgules dans leur contenu, par exemple, une adresse de rue qui contient la valeur « Seattle,WA » sera évaluée en tant que deux champs distincts lors de l'.csv si le format .csv est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7d636-196">In particular, fields that may contain commas in their content, for example, a street address that contains the value "Seattle,WA" would be parsed as two separate fields when parsed if the .csv format is selected.</span></span> <span data-ttu-id="7d636-197">Pour éviter cela, utilisez le format .tsv ou entourez la virgule contenant des valeurs par des guillemets doubles dans la table de données sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-197">To avoid this, use the .tsv format or surrounded the comma containing values by double quotes in the sensitive data table.</span></span> <span data-ttu-id="7d636-198">Si des virgules contenant des valeurs contiennent également des espaces, vous devez créer un sit personnalisé qui correspond au format correspondant.</span><span class="sxs-lookup"><span data-stu-id="7d636-198">If comma containing values also contain spaces, you need to create a custom SIT that matches the corresponding format.</span></span> <span data-ttu-id="7d636-199">Par exemple, un SIT qui détecte une chaîne à plusieurs mots avec des virgules et des espaces.</span><span class="sxs-lookup"><span data-stu-id="7d636-199">For example, a SIT that detects multi-word string with commas and spaces in it.</span></span>

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="7d636-200">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-200">Define the schema for your database of sensitive information</span></span>

<span data-ttu-id="7d636-201">Si, pour des raisons commerciales ou techniques, vous préférez ne pas utiliser PowerShell ou la ligne de commande pour créer votre schéma et votre modèle de type d’informations sensibles EDM (package de règles), vous pouvez utiliser l’[Assistant de correspondance exacte de données et de type d’informations sensibles](sit-edm-wizard.md) pour les créer.</span><span class="sxs-lookup"><span data-stu-id="7d636-201">If for business or technical reasons, you prefer not to use PowerShell or command line to create your schema and EDM sensitive info type pattern (rule package), you can use the [Exact Data Match Schema and Sensitive Information Type Wizard](sit-edm-wizard.md) to create them.</span></span> <span data-ttu-id="7d636-202">Lorsque vous avez terminé de créer le schéma et le modèle de type d’informations sensibles EDM, revenez à la procédure afin d’effectuer toutes les étapes nécessaires pour que votre type d’informations sensibles EDM soit disponible.</span><span class="sxs-lookup"><span data-stu-id="7d636-202">When you are done creating the schema and EDM sensitive info type pattern, return to complete all the steps necessary to make your EDM based sensitive information type available for use.</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-203">L’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles est disponible uniquement pour les nuages mondiaux et GCC.</span><span class="sxs-lookup"><span data-stu-id="7d636-203">The Exact Data Match Schema and Sensitive Information Type Wizard is only available for the World Wide and GCC clouds only.</span></span>

1. <span data-ttu-id="7d636-204">Définissez le schéma pour la base de données d’informations sensibles dans un fichier XML (comme dans l’exemple ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="7d636-204">Define the schema for the database of sensitive information in XML format (similar to our example below).</span></span> <span data-ttu-id="7d636-205">Nommez ce fichier de schéma **edm.xml** et configurez-le de telle sorte que pour chaque colonne de la base de données, une ligne utilise la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="7d636-205">Name this schema file **edm.xml**, and configure it such that for each column in the database, there is a line that uses the syntax:</span></span> 

      <span data-ttu-id="7d636-206">`\<Field name="" searchable=""/\>`.</span><span class="sxs-lookup"><span data-stu-id="7d636-206">`\<Field name="" searchable=""/\>`.</span></span>

      - <span data-ttu-id="7d636-207">Utilisez les noms de colonne pour les valeurs de *nom de champ*.</span><span class="sxs-lookup"><span data-stu-id="7d636-207">Use column names for *Field name* values.</span></span>
      - <span data-ttu-id="7d636-208">Utilisez *searchable="true"* pour jusqu’à 5 champs dont vous voulez qu’il puissent faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="7d636-208">Use *searchable="true"* for the fields that you want to be searchable up to a maximum of 5 fields.</span></span> <span data-ttu-id="7d636-209">Au moins un champ doit pouvoir faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="7d636-209">At least one field must be searchable.</span></span>

      <span data-ttu-id="7d636-210">Par exemple, le fichier XML suivant définit le schéma d’une base de données de dossiers de patients, avec cinq champs pouvant faire l’objet d’une recherche : *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span><span class="sxs-lookup"><span data-stu-id="7d636-210">As an example, the following XML file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span>

      <span data-ttu-id="7d636-211">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="7d636-211">(You can copy, modify, and use our example.)</span></span>

      ```xml
      <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
            <DataStore name="PatientRecords" description="Schema for patient records" version="1">
                  <Field name="PatientID" searchable="true" caseInsensitive="true" ignoredDelimiters="-,/,*,#,^" />
                  <Field name="MRN" searchable="true" />
                  <Field name="FirstName" />
                  <Field name="LastName" />
                  <Field name="SSN" searchable="true" />
                  <Field name="Phone" searchable="true" />
                  <Field name="DOB" searchable="true" />
                  <Field name="Gender" />
                  <Field name="Address" />
            </DataStore>
      </EdmSchema>
      ```

##### <a name="configurable-match-using-the-caseinsensitive-and-ignoreddelimiters-fields"></a><span data-ttu-id="7d636-212">Correspondance configurable à l’aide des champs caseInsensitive et ignoredDelimiters</span><span class="sxs-lookup"><span data-stu-id="7d636-212">Configurable match using the caseInsensitive and ignoredDelimiters fields</span></span>

<span data-ttu-id="7d636-213">L’exemple XML ci-dessus utilise les champs `caseInsensitive` et `ignoredDelimiters`.</span><span class="sxs-lookup"><span data-stu-id="7d636-213">The above XML sample makes use of the `caseInsensitive` and the `ignoredDelimiters` fields.</span></span> 

<span data-ttu-id="7d636-214">Lorsque vous incluez le champ \***caseInsensitive** _ défini sur la valeur `true` dans votre définition de schéma, EDM n’exclut pas un élément sur la base des différences de casse dans le champ `PatientID`.</span><span class="sxs-lookup"><span data-stu-id="7d636-214">When you include the \***caseInsensitive** _ field set to the value of `true` in your schema definition, EDM will not exclude an item based on case differences for `PatientID` field.</span></span> <span data-ttu-id="7d636-215">EDM considère donc `PatientID` _ *FOO-1234*\* et **fOo-1234** comme étant identiques.</span><span class="sxs-lookup"><span data-stu-id="7d636-215">So EDM will see, `PatientID` _ *FOO-1234*\* and **fOo-1234** as being identical.</span></span>

<span data-ttu-id="7d636-216">Lorsque vous incluez le champ **ignoredDelimiters** _ avec les caractères pris en charge, EDM ignore ces caractères dans `PatientID`.</span><span class="sxs-lookup"><span data-stu-id="7d636-216">When you include the \***ignoredDelimiters** _ field with supported characters,  EDM will ignore those characters in the `PatientID`.</span></span> <span data-ttu-id="7d636-217">EDM considère donc `PatientID` _ *FOO-1234*\* et `PatientID` **FOO#1234** comme étant identiques.</span><span class="sxs-lookup"><span data-stu-id="7d636-217">So EDM will see, `PatientID` _ *FOO-1234*\* and `PatientID` **FOO#1234** as being identical.</span></span> <span data-ttu-id="7d636-218">L’indicateur `ignoredDelimiters` prend en charge tous les caractères non alphanumériques. Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="7d636-218">The `ignoredDelimiters` flag supports any non-alphanumeric character, here are some examples:</span></span>
- <span data-ttu-id="7d636-219">\.</span><span class="sxs-lookup"><span data-stu-id="7d636-219">\.</span></span>
- \-
- \/
- \_
- \*
- \^
- \#
- \!
- \?
- \[
- \]
- \{
- \}
- \\
- \~
- \; 

<span data-ttu-id="7d636-220">L’indicateur `ignoredDelimiters` ne prend pas en charge :</span><span class="sxs-lookup"><span data-stu-id="7d636-220">The `ignoredDelimiters` flag doesn't support:</span></span>
- <span data-ttu-id="7d636-221">Les caractères 0 à 9</span><span class="sxs-lookup"><span data-stu-id="7d636-221">characters 0-9</span></span>
- <span data-ttu-id="7d636-222">A-Z</span><span class="sxs-lookup"><span data-stu-id="7d636-222">A-Z</span></span>
- <span data-ttu-id="7d636-223">a-z</span><span class="sxs-lookup"><span data-stu-id="7d636-223">a-z</span></span>
- \"
- \,

<span data-ttu-id="7d636-224">Dans cet exemple, où `caseInsensitive` et `ignoredDelimiters` sont utilisés ensemble, EDM considère **FOO-1234** et **fOo#1234** comme étant identiques et classifie l’élément comme un type d’informations sensibles de dossier de patient.</span><span class="sxs-lookup"><span data-stu-id="7d636-224">In this example, where both `caseInsensitive` and `ignoredDelimiters` are used, EDM would see **FOO-1234** and **fOo#1234** as  identical and classify the item as a patient record sensitive information type.</span></span> 

4. <span data-ttu-id="7d636-225">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="7d636-225">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

5. <span data-ttu-id="7d636-226">Pour charger le schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="7d636-226">To upload the database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="7d636-227">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d636-227">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="7d636-228">Confirmer</span><span class="sxs-lookup"><span data-stu-id="7d636-228">Confirm</span></span>
      >
      > <span data-ttu-id="7d636-229">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="7d636-229">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="7d636-230">Un nouveau schéma EDM pour le magasin de données « patientrecords » va être importé.</span><span class="sxs-lookup"><span data-stu-id="7d636-230">New EDM Schema for the data store 'patientrecords' will be imported.</span></span>
      >
      > <span data-ttu-id="7d636-231">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="7d636-231">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="7d636-232">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 5, utilisez plutôt la cmdlet New-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="7d636-232">If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: New-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-233">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="7d636-233">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="7d636-234">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="7d636-234">The update must complete before you execute steps that use the additions.</span></span>

#### <a name="set-up-a-rule-package"></a><span data-ttu-id="7d636-235">Configurer un package de règles</span><span class="sxs-lookup"><span data-stu-id="7d636-235">Set up a rule package</span></span>

1. <span data-ttu-id="7d636-236">Créez un package de règles au format XML (avec codage Unicode) similaire à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7d636-236">Create a rule package in XML format (with Unicode encoding), similar to the following example.</span></span> <span data-ttu-id="7d636-237">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="7d636-237">(You can copy, modify, and use our example.)</span></span>

      <span data-ttu-id="7d636-238">Lorsque vous définissez votre package de règles, veillez à référencer correctement .csv fichier .tsv ou .tsv **etedm.xml** fichier.</span><span class="sxs-lookup"><span data-stu-id="7d636-238">When you set up your rule package, make sure to correctly reference your .csv or .tsv file and **edm.xml** file.</span></span> <span data-ttu-id="7d636-239">Vous pouvez copier, modifier et utiliser notre exemple.</span><span class="sxs-lookup"><span data-stu-id="7d636-239">You can copy, modify, and use our example.</span></span> <span data-ttu-id="7d636-240">Dans cet exemple de fichier xml, les champs suivants doivent être personnalisés pour créer votre type sensible d’EDM :</span><span class="sxs-lookup"><span data-stu-id="7d636-240">In this sample xml the following fields needs to be customized to create your EDM sensitive type:</span></span>

      - <span data-ttu-id="7d636-241">**RulePack id & ExactMatch id** : utilisez [New-GUID](/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) pour générer un GUID.</span><span class="sxs-lookup"><span data-stu-id="7d636-241">**RulePack id & ExactMatch id**: Use [New-GUID](/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) to generate a GUID.</span></span>

      - <span data-ttu-id="7d636-242">**Datastore** : ce champ spécifie le magasin de données de recherche EDM à utiliser.</span><span class="sxs-lookup"><span data-stu-id="7d636-242">**Datastore**: This field specifies EDM lookup data store to be used.</span></span> <span data-ttu-id="7d636-243">Vous indiquez un nom de source de données ou un schéma EDM configuré.</span><span class="sxs-lookup"><span data-stu-id="7d636-243">You provide a data source name of a configured EDM Schema.</span></span>

      - <span data-ttu-id="7d636-244">**idMatch** : ce champ pointe vers l’élément principal pour EDM.</span><span class="sxs-lookup"><span data-stu-id="7d636-244">**idMatch**: This field points to the primary element for EDM.</span></span>
        - <span data-ttu-id="7d636-245">Matches : spécifie le champ à utiliser dans la recherche exacte.</span><span class="sxs-lookup"><span data-stu-id="7d636-245">Matches: Specifies the field to be used in exact lookup.</span></span> <span data-ttu-id="7d636-246">Vous fournissez un nom de champ pouvant faire l’objet d’une recherche dans le schéma EDM pour le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="7d636-246">You provide a searchable field name in EDM Schema for the DataStore.</span></span>
        - <span data-ttu-id="7d636-247">Classification : ce champ spécifie la correspondance de type sensible qui déclenche la recherche EDM.</span><span class="sxs-lookup"><span data-stu-id="7d636-247">Classification: This field specifies the sensitive type match that triggers EDM lookup.</span></span> <span data-ttu-id="7d636-248">Vous pouvez fournir le nom ou le GUID d’un type d’informations sensibles intégré ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="7d636-248">You can provide the Name or GUID of an existing built-in or custom sensitive information type.</span></span> <span data-ttu-id="7d636-249">N’ignorez pas que toute chaîne qui correspond au type d’informations sensibles fourni sera hachée et comparée à chaque entrée de la table des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-249">Be aware that any string that matches the sensitive information type provided will be hashed and compared to every entry in the sensitive information table.</span></span> <span data-ttu-id="7d636-250">Pour éviter de provoquer des problèmes de performances, si vous utilisez un type d’informations sensibles personnalisé comme élément Classification dans Dem, évitez d’en utiliser un qui corresponde à un grand pourcentage de contenu (par exemple, « n’importe quel nombre » ou « tout mot de cinq lettres ») en ajoutant des mots clés à l’appui ou en ajoutant une mise en forme dans la définition du type d’informations sensibles de classification personnalisée.</span><span class="sxs-lookup"><span data-stu-id="7d636-250">In order to avoid causing performance issues, if you use a custom sensitive information type as the Classification element in EDM, avoid using one that will match a large percentage of content (such as "any number" or "any five-letter word") by adding supporting keywords or including formatting in the definition of the custom classification sensitive information type.</span></span> 

      - <span data-ttu-id="7d636-251">**Match :** ce champ pointe vers d’autres preuves à proximité d’idMatch.</span><span class="sxs-lookup"><span data-stu-id="7d636-251">**Match:** This field points to additional evidence found in proximity of idMatch.</span></span>
        - <span data-ttu-id="7d636-252">Matches : vous indiquez un nom de champ dans le schéma EDM pour DataStore.</span><span class="sxs-lookup"><span data-stu-id="7d636-252">Matches: You provide any field name in EDM Schema for DataStore.</span></span>
      - <span data-ttu-id="7d636-253">**Resource :** cette section spécifie le nom et la description du type sensible dans plusieurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="7d636-253">**Resource:** This section specifies the name and description for sensitive type in multiple locales.</span></span>
        - <span data-ttu-id="7d636-254">idRef : fournissez un GUID pour ExactMatch ID.</span><span class="sxs-lookup"><span data-stu-id="7d636-254">idRef: You provide GUID for ExactMatch ID.</span></span>
        - <span data-ttu-id="7d636-255">Nom et descriptions : personnalisez si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7d636-255">Name & descriptions: customize as required.</span></span>

      ```xml
      <RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
        <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
          <Version build="0" major="2" minor="0" revision="0" />
          <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
          <Details defaultLangCode="en-us">
            <LocalizedDetails langcode="en-us">
              <PublisherName>IP DLP</PublisherName>
              <Name>Health Care EDM Rulepack</Name>
              <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
            </LocalizedDetails>
          </Details>
        </RulePack>
        <Rules>
          <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
            <Pattern confidenceLevel="65">
              <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
            </Pattern>
            <Pattern confidenceLevel="75">
              <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
              <Any minMatches ="3" maxMatches ="6">
                <match matches="PatientID" />
                <match matches="MRN"/>
                <match matches="FirstName"/>
                <match matches="LastName"/>
                <match matches="Phone"/>
                <match matches="DOB"/>
              </Any>
            </Pattern>
          </ExactMatch>
          <LocalizedStrings>
            <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
              <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
              <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
            </Resource>
          </LocalizedStrings>
        </Rules>
      </RulePackage>
      ```

2. <span data-ttu-id="7d636-256">Téléchargez le package de règles en exécutant les cmdlets PowerShell suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="7d636-256">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

      ```powershell
      $rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
      New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
      ```

<span data-ttu-id="7d636-257">À ce stade, vous avez configuré la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="7d636-257">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="7d636-258">L’étape suivante consiste à hacher les données sensibles, puis à charger les hachages pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="7d636-258">The next step is to hash the sensitive data, and then upload the hashes for indexing.</span></span>

<span data-ttu-id="7d636-259">Rappelez-vous que la procédure précédente de notre schéma PatientRecords définit cinq champs pouvant faire l’objet d’une recherche : *PatientID*,*MRN*, *SSN*, *Phone* et *DOB*.</span><span class="sxs-lookup"><span data-stu-id="7d636-259">Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> <span data-ttu-id="7d636-260">Notre exemple de package de règles inclut ces champs et référence le fichier de schéma de base de données (**edm.xml**), avec un seul élément *ExactMatch* par champ pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="7d636-260">Our example rule package includes those fields and references the database schema file (**edm.xml**), with one *ExactMatch* item per searchable field.</span></span> <span data-ttu-id="7d636-261">Prenons l’élément ExactMatch suivant :</span><span class="sxs-lookup"><span data-stu-id="7d636-261">Consider the following ExactMatch item:</span></span>

```xml
<ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="100">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </ExactMatch>
```

<span data-ttu-id="7d636-262">À partir de cet exemple, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="7d636-262">In this example, note that:</span></span>

- <span data-ttu-id="7d636-263">Le nom du magasin de données fait référence au fichier .csv que nous avons créé précédemment : **dataStore = "PatientRecords"**.</span><span class="sxs-lookup"><span data-stu-id="7d636-263">The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.</span></span>

- <span data-ttu-id="7d636-264">La valeur idMatch fait référence à un champ pouvant faire l’objet d’une recherche figurant dans le fichier de schéma de base de données : **idMatch matches = "SSN"**.</span><span class="sxs-lookup"><span data-stu-id="7d636-264">The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.</span></span>

- <span data-ttu-id="7d636-265">La valeur de classification fait référence à un type d’informations sensibles existant ou personnalisé : **classification = "U.S. Social Security Number (SSN)"**</span><span class="sxs-lookup"><span data-stu-id="7d636-265">The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**.</span></span> <span data-ttu-id="7d636-266">(en l’occurrence, nous utilisons le type d’informations sensibles existant pour le numéro de sécurité sociale aux États-Unis).</span><span class="sxs-lookup"><span data-stu-id="7d636-266">(In this case, we use the existing sensitive information type of U.S. Social Security Number.)</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-267">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="7d636-267">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="7d636-268">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="7d636-268">The update must complete before you execute steps that use the additions.</span></span>
 
<span data-ttu-id="7d636-269">Après avoir importé votre package de règles avec votre type d’informations sensibles EDM et importé votre table de données sensibles, vous pouvez tester votre type nouvellement créé à l’aide de la fonction **Tester** dans l’Assistant Gestion des problèmes de sécurité des données dans le Centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="7d636-269">After you have imported your rule package with your EDM sensitive info type and have imported your sensitive data table, you can test your newly created type by using the **Test** function in the EDM wizard in the compliance center.</span></span> <span data-ttu-id="7d636-270">Consultez [Utiliser l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles](sit-edm-wizard.md) pour obtenir des instructions sur l’utilisation de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7d636-270">See [Use the Exact Data Match Schema and Sensitive Information Type Wizard](sit-edm-wizard.md) for instructions on using this functionality.</span></span>

#### <a name="editing-the-schema-for-edm-based-classification"></a><span data-ttu-id="7d636-271">Modification du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-271">Editing the schema for EDM-based classification</span></span>

<span data-ttu-id="7d636-272">Si vous souhaitez modifier votre fichier **edm.xml**, par exemple pour changer les champs utilisés pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d636-272">If you want to make changes to your **edm.xml** file, such as changing which fields are used for EDM-based classification, follow these steps:</span></span>

> [!TIP]
> <span data-ttu-id="7d636-273">Vous pouvez modifier votre schéma EDM et votre fichier de données pour tirer parti d’une **correspondance configurable**.</span><span class="sxs-lookup"><span data-stu-id="7d636-273">You can change your EDM schema and data file to take advantage of **configurable match**.</span></span> <span data-ttu-id="7d636-274">Lorsqu’il est configuré, EDM ignore les différences de casse et certains séparateurs lorsqu’il évalue un élément.</span><span class="sxs-lookup"><span data-stu-id="7d636-274">When configured, EDM will ignore case differences and some delimiters when it evaluates an item.</span></span> <span data-ttu-id="7d636-275">Cela simplifie la définition de votre schéma XML et de vos fichiers de données sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-275">This makes defining your xml schema and your sensitive data files easier.</span></span> <span data-ttu-id="7d636-276">Pour plus d’informations, voir [Modifier le schéma de correspondance des données exactes pour utiliser la correspondance configurable](sit-modify-edm-schema-configurable-match.md).</span><span class="sxs-lookup"><span data-stu-id="7d636-276">To learn more see, [Modify Exact Data Match schema to use configurable match](sit-modify-edm-schema-configurable-match.md).</span></span>

1. <span data-ttu-id="7d636-277">Modifiez votre fichier **edm.xml** (présenté dans la section [Définir le schéma](#define-the-schema-for-your-database-of-sensitive-information) de cet article).</span><span class="sxs-lookup"><span data-stu-id="7d636-277">Edit your **edm.xml** file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).</span></span>

2. <span data-ttu-id="7d636-278">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="7d636-278">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

3. <span data-ttu-id="7d636-279">Pour mettre à jour votre schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="7d636-279">To update your database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="7d636-280">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d636-280">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="7d636-281">Confirmer</span><span class="sxs-lookup"><span data-stu-id="7d636-281">Confirm</span></span>
      >
      > <span data-ttu-id="7d636-282">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="7d636-282">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="7d636-283">Le schéma EDM pour le magasin de données « patientrecords » va être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7d636-283">EDM Schema for the data store 'patientrecords' will be updated.</span></span>
      >
      > <span data-ttu-id="7d636-284">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="7d636-284">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      > <span data-ttu-id="7d636-285">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 3, utilisez plutôt la cmdlet Set-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="7d636-285">If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: Set-DlpEdmSchema -FileData $edmSchemaXml</span></span>

      > [!NOTE]
      > <span data-ttu-id="7d636-286">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="7d636-286">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="7d636-287">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="7d636-287">The update must complete before you execute steps that use the additions.</span></span>

#### <a name="removing-the-schema-for-edm-based-classification"></a><span data-ttu-id="7d636-288">Suppression du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-288">Removing the schema for EDM-based classification</span></span>

<span data-ttu-id="7d636-289">(Le cas échéant) Si vous voulez supprimer le schéma que vous utilisez pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7d636-289">(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="7d636-290">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="7d636-290">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="7d636-291">Exécutez les applets de commande PowerShell suivantes, en remplaçant le nom de magasin de données « patient records » par celui que vous voulez supprimer :</span><span class="sxs-lookup"><span data-stu-id="7d636-291">Run the following PowerShell cmdlets, substituting the data store name of "patient records" with the one you want to remove:</span></span>

      ```powershell
      Remove-DlpEdmSchema -Identity patientrecords
      ```

      <span data-ttu-id="7d636-292">Vous serez invité à confirmer :</span><span class="sxs-lookup"><span data-stu-id="7d636-292">You will be prompted to confirm:</span></span>

      > <span data-ttu-id="7d636-293">Confirmer</span><span class="sxs-lookup"><span data-stu-id="7d636-293">Confirm</span></span>
      >
      > <span data-ttu-id="7d636-294">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="7d636-294">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="7d636-295">Le schéma EDM pour le magasin de données « patientrecords » va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="7d636-295">EDM Schema for the data store 'patientrecords' will be removed.</span></span>
      >
      > <span data-ttu-id="7d636-296">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="7d636-296">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      >  <span data-ttu-id="7d636-297">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 2, utilisez plutôt la cmdlet Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span><span class="sxs-lookup"><span data-stu-id="7d636-297">If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span></span>

### <a name="part-2-hash-and-upload-the-sensitive-data"></a><span data-ttu-id="7d636-298">Partie 2 : hacher et charger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-298">Part 2: Hash and upload the sensitive data</span></span>

<span data-ttu-id="7d636-299">Au cours de cette phase, vous configurez un groupe de sécurité personnalisé et un compte d’utilisateur, et configurez l’outil de chargement de l’agent EDM.</span><span class="sxs-lookup"><span data-stu-id="7d636-299">In this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="7d636-300">Vous utilisez ensuite l’outil pour hacher les données sensibles avec valeur salt et les charger.</span><span class="sxs-lookup"><span data-stu-id="7d636-300">Then, you use the tool to hash with salt value the sensitive data, and upload it.</span></span>

<span data-ttu-id="7d636-301">L’opération de hachage et de chargement peut être effectuée à l’aide d’un ordinateur ou vous pouvez séparer ces deux étapes pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="7d636-301">The hashing and uploading can be done using one computer or you can separate the hashing step from the upload step for greater security.</span></span>

<span data-ttu-id="7d636-302">Si vous voulez hacher et charger à partir d’un ordinateur, vous devez le faire à partir d’un ordinateur qui peut se connecter directement à votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7d636-302">If you want to hash and upload from one computer, you need to do it from a computer that can directly connect to your Microsoft 365 tenant.</span></span> <span data-ttu-id="7d636-303">Vos fichiers de données sensibles en texte clair doivent se trouver sur cet ordinateur pour le hachage.</span><span class="sxs-lookup"><span data-stu-id="7d636-303">This requires that your clear text sensitive data files are on that computer for hashing.</span></span>

<span data-ttu-id="7d636-p129">Si vous ne souhaitez pas exposer votre fichier de données sensibles en texte clair, vous pouvez le hacher sur un ordinateur dans un emplacement sécurisé, puis copier le fichier de hachage et le fichier salt sur un ordinateur qui peut se connecter directement à votre client Microsoft 365 pour le chargement. Dans ce scénario, vous aurez besoin d’EDMUploadAgent sur les deux ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7d636-p129">If you do not want to expose your clear text sensitive data file, you can hash it on a computer in a secure location and then copy the hash file and the salt file to a computer that can directly connect to your Microsoft 365 tenant for upload. In this scenario, you will need the EDMUploadAgent on both computers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d636-306">Si vous utilisiez l’assistant du schéma de correspondance des données exacte et du type d’informations sensibles pour créer vos fichiers de schéma et de modèle, vous ***devez*** télécharger le schéma pour cette procédure.</span><span class="sxs-lookup"><span data-stu-id="7d636-306">If you used the Exact Data Match schema and sensitive information type wizard to create your schema and pattern files, you ***must*** download the schema for this procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-307">Si votre organisation a installé la clé client pour [Microsoft 365](customer-key-overview.md)au niveau du client, la correspondance exacte des données utilisera automatiquement sa fonctionnalité de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="7d636-307">If your organization has set up [Customer Key for Microsoft 365 at the tenant level](customer-key-overview.md), Exact data match will make use of its encryption functionality automatically.</span></span> <span data-ttu-id="7d636-308">Cette offre est disponible uniquement pour les clients sous licence E5 dans le cloud commercial.</span><span class="sxs-lookup"><span data-stu-id="7d636-308">This is available only to E5 licensed tenants in the Commercial cloud.</span></span>

#### <a name="prerequisites"></a><span data-ttu-id="7d636-309">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d636-309">Prerequisites</span></span>

- <span data-ttu-id="7d636-310">Un compte professionnel ou scolaire pour Microsoft 365 qui sera ajouté au groupe de sécurité **EDM\_DataUploaders**</span><span class="sxs-lookup"><span data-stu-id="7d636-310">a work or school account for Microsoft 365  that will be added to the **EDM\_DataUploaders** security group</span></span>
- <span data-ttu-id="7d636-311">Un ordinateur Windows 10 ou Windows Server 2016 avec .NET version 4.6.2 pour l’exécution d’EDMUploadAgent</span><span class="sxs-lookup"><span data-stu-id="7d636-311">a Windows 10 or Windows Server 2016 machine with .NET version 4.6.2 for running the EDMUploadAgent</span></span>
- <span data-ttu-id="7d636-312">Un répertoire sur votre ordinateur de téléchargement pour :</span><span class="sxs-lookup"><span data-stu-id="7d636-312">a directory on your upload machine for the:</span></span>
  - <span data-ttu-id="7d636-313">EDMUploadAgent</span><span class="sxs-lookup"><span data-stu-id="7d636-313">EDMUploadAgent</span></span>
  - <span data-ttu-id="7d636-314">votre fichier d’élément sensible au format .csv .tsv ou .tsv, **PatientRecords.csv** dans nos exemples</span><span class="sxs-lookup"><span data-stu-id="7d636-314">your sensitive item file in .csv or .tsv format, **PatientRecords.csv** in our examples</span></span>
  - <span data-ttu-id="7d636-315">fichiers de hachage et salt de sortie</span><span class="sxs-lookup"><span data-stu-id="7d636-315">the output hash and salt files</span></span>
  - <span data-ttu-id="7d636-316">Le nom du magasin de données provenant du fichier **edm.xml**, ici `PatientRecords`</span><span class="sxs-lookup"><span data-stu-id="7d636-316">the datastore name from the **edm.xml** file, for this example its `PatientRecords`</span></span>
- <span data-ttu-id="7d636-317">Si vous avez utilisé l’[Assistant de schéma de correspondance exacte des données et de type d’informations sensibles](sit-edm-wizard.md), vous ***devez*** le télécharger.</span><span class="sxs-lookup"><span data-stu-id="7d636-317">If you used the [Exact Data Match schema and sensitive information type wizard](sit-edm-wizard.md) you ***must*** download it</span></span>

#### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="7d636-318">Configurer les groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7d636-318">Set up the security group and user account</span></span>

1. <span data-ttu-id="7d636-319">En tant qu’administrateur général, accédez au centre d’administration à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription) et [créez un groupe de sécurité](/office365/admin/email/create-edit-or-delete-a-security-group) nommé **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="7d636-319">As a global administrator, go to the admin center using the appropriate [link for your subscription](#portal-links-for-your-subscription) and [create a security group](/office365/admin/email/create-edit-or-delete-a-security-group) called **EDM\_DataUploaders**.</span></span>

2. <span data-ttu-id="7d636-320">Ajoutez un ou plusieurs utilisateurs au groupe de sécurité **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="7d636-320">Add one or more users to the **EDM\_DataUploaders** security group.</span></span> <span data-ttu-id="7d636-321">(ces utilisateurs peuvent gérer la base de données d’informations sensibles).</span><span class="sxs-lookup"><span data-stu-id="7d636-321">(These users will manage the database of sensitive information.)</span></span>

#### <a name="hash-and-upload-from-one-computer"></a><span data-ttu-id="7d636-322">Hacher et charger à partir d’un même ordinateur</span><span class="sxs-lookup"><span data-stu-id="7d636-322">Hash and upload from one computer</span></span>

<span data-ttu-id="7d636-323">Cet ordinateur doit avoir accès directement à votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7d636-323">This computer must have direct access to your Microsoft 365 tenant.</span></span>

> [!NOTE]
>
> <span data-ttu-id="7d636-324">Avant de commencer cette procédure, assurez-vous que vous êtes membre du groupe de sécurité **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="7d636-324">Before you begin this procedure, make sure that you are a member of the **EDM\_DataUploaders** security group.</span></span>
>
> <span data-ttu-id="7d636-325">Si vous le souhaitez, vous pouvez exécuter une validation sur votre fichier .csv .tsv ou .tsv avant de télécharger en exécutant :</span><span class="sxs-lookup"><span data-stu-id="7d636-325">Optionally, you can run a validation against your .csv or .tsv file before uploading by running:</span></span>
>
> `EdmUploadAgent.exe /ValidateData /DataFile [data file] /Schema [schema file]`
>
> <span data-ttu-id="7d636-326">Pour plus d’informations sur tous les paramètres pris en charge par EdmUploadAgent.exe</span><span class="sxs-lookup"><span data-stu-id="7d636-326">For more information on all the EdmUploadAgent.exe >supported parameters run</span></span>
>
> `EdmUploadAgent.exe /?`

#### <a name="links-to-edm-upload-agent-by-subscription-type"></a><span data-ttu-id="7d636-327">Liens vers l’agent de chargement EDM par type d’abonnement</span><span class="sxs-lookup"><span data-stu-id="7d636-327">Links to EDM upload agent by subscription type</span></span>

- <span data-ttu-id="7d636-328">[Commercial + GCC](https://go.microsoft.com/fwlink/?linkid=2088639) : pour la plupart des clients commerciaux</span><span class="sxs-lookup"><span data-stu-id="7d636-328">[Commercial + GCC](https://go.microsoft.com/fwlink/?linkid=2088639) - most commercial customers should use this</span></span>
- <span data-ttu-id="7d636-329">[GCC-High](https://go.microsoft.com/fwlink/?linkid=2137521) : conçu spécifiquement pour les abonnés cloud du secteur public haute sécurité</span><span class="sxs-lookup"><span data-stu-id="7d636-329">[GCC-High](https://go.microsoft.com/fwlink/?linkid=2137521) - This is specifically for high security government cloud subscribers</span></span>
- <span data-ttu-id="7d636-330">[DoD](https://go.microsoft.com/fwlink/?linkid=2137807) : conçu spécifiquement pour les clients cloud du Department of Defense américain</span><span class="sxs-lookup"><span data-stu-id="7d636-330">[DoD](https://go.microsoft.com/fwlink/?linkid=2137807) - this is specifically for United States Department of Defense cloud customers</span></span>

1. <span data-ttu-id="7d636-331">Créez un répertoire de travail pour EDMUploadAgent.</span><span class="sxs-lookup"><span data-stu-id="7d636-331">Create a working directory for the EDMUploadAgent.</span></span> <span data-ttu-id="7d636-332">Par exemple, **C:\EDM\Data**.</span><span class="sxs-lookup"><span data-stu-id="7d636-332">For example, **C:\EDM\Data**.</span></span> <span data-ttu-id="7d636-333">Placez le fichier **PatientRecords.csv** à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="7d636-333">Place the **PatientRecords.csv** file there.</span></span>

2. <span data-ttu-id="7d636-334">Téléchargez et installez l’[agent de chargement EDM](#links-to-edm-upload-agent-by-subscription-type) approprié pour votre abonnement dans le répertoire créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="7d636-334">Download and install the appropriate [EDM Upload Agent](#links-to-edm-upload-agent-by-subscription-type) for your subscription into the directory you created in step 1.</span></span>

   > [!NOTE]
   > <span data-ttu-id="7d636-335">La version d’EDMUploadAgent fournie à travers les liens ci-dessus a été mise à jour afin d’ajouter automatiquement une valeur salt aux données hachées.</span><span class="sxs-lookup"><span data-stu-id="7d636-335">The EDMUploadAgent at the above links has been updated to automatically add a salt value to the hashed data.</span></span> <span data-ttu-id="7d636-336">Vous pouvez également fournir votre propre valeur salt.</span><span class="sxs-lookup"><span data-stu-id="7d636-336">Alternately, you can provide your own salt value.</span></span> <span data-ttu-id="7d636-337">Une fois que vous avez utilisé cette version, vous ne pourrez pas utiliser la version précédente d’EDMUploadAgent.</span><span class="sxs-lookup"><span data-stu-id="7d636-337">Once you have used this version, you will not be able to use the previous version of the EDMUploadAgent.</span></span>
   >
   > <span data-ttu-id="7d636-338">Vous pouvez télécharger des données avec EDMUploadAgent vers n’importe quel magasin de données donné deux fois par jour uniquement.</span><span class="sxs-lookup"><span data-stu-id="7d636-338">You can upload data with the EDMUploadAgent to any given data store only twice per day.</span></span>

   > [!TIP]
   > <span data-ttu-id="7d636-p134">Exécutez l'agent sans arguments pour obtenir une liste des paramètres de commande pris en charge. Par exemple, « EdmUploadAgent.exe ».</span><span class="sxs-lookup"><span data-stu-id="7d636-p134">To a get a list out of the supported command parameters, run the agent no arguments. For example 'EdmUploadAgent.exe'.</span></span>

2. <span data-ttu-id="7d636-341">Autorisez l’agent de chargement EDM, en ouvrant l’invite de commandes Windows (en tant qu’administrateur), puis en accédant au répertoire **C:\EDM\Data** pour exécuter la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7d636-341">Authorize the EDM Upload Agent, open  Command Prompt window (as an administrator), switch to the **C:\EDM\Data** directory and then run the following command:</span></span>

   `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="7d636-342">Connectez-vous à l’aide de votre compte professionnel ou scolaire pour Microsoft 365 qui a été ajouté au groupe de sécurité EDM_DataUploaders.</span><span class="sxs-lookup"><span data-stu-id="7d636-342">Sign in with your work or school account for Microsoft 365 that was added to the EDM_DataUploaders security group.</span></span> <span data-ttu-id="7d636-343">Vos informations de client sont extraites du compte d’utilisateur pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="7d636-343">Your tenant information is extracted from the user account to make the connection.</span></span>

   <span data-ttu-id="7d636-344">FACULTATIF : si vous avez utilisé l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles pour créer vos fichiers de schéma et de modèle, exécutez la commande suivante dans une fenêtre Invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="7d636-344">OPTIONAL: If you used the Exact Data Match schema and sensitive information type wizard to create your schema and pattern files, run the following command in a Command Prompt window:</span></span>

   `EdmUploadAgent.exe /SaveSchema /DataStoreName <schema name> /OutputDir <path to output folder>`

4. <span data-ttu-id="7d636-345">Pour hacher et charger les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="7d636-345">To hash and upload the sensitive data, run the following command in Command Prompt window:</span></span>

   `EdmUploadAgent.exe /UploadData /DataStoreName [DS Name] /DataFile [data file] /HashLocation [hash file location] /Schema [Schema file] /ColumnSeparator ["{Tab}"|"|"]`

   <span data-ttu-id="7d636-346">Exemple : **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\Edm\Hash\PatientRecords.csv /HashLocation C:\Edm\Hash /Schema edm.xml**</span><span class="sxs-lookup"><span data-stu-id="7d636-346">Example: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\Edm\Hash\PatientRecords.csv /HashLocation C:\Edm\Hash /Schema edm.xml**</span></span>

   <span data-ttu-id="7d636-347">Le format par défaut du fichier de données sensibles est les valeurs séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="7d636-347">The default format for the sensitive data file is comma-separated values.</span></span> <span data-ttu-id="7d636-348">Vous pouvez spécifier un fichier séparé par des tabulations en indiquant l’option « {Tab} » avec le paramètre /ColumnSeparator, ou vous pouvez spécifier un fichier séparé par un canal en indiquant l’option « | ».</span><span class="sxs-lookup"><span data-stu-id="7d636-348">You can specify a tab-separated file by indicating the "{Tab}" option with the /ColumnSeparator parameter, or you can specify a pipe-separated file by indicating the "|" option.</span></span>  
   <span data-ttu-id="7d636-349">Cette commande ajoute automatiquement une valeur salt générée de manière aléatoire au hachage pour une sécurité accrue.</span><span class="sxs-lookup"><span data-stu-id="7d636-349">This command will automatically add a randomly generated salt value to the hash for greater security.</span></span> <span data-ttu-id="7d636-350">Si vous voulez utiliser votre propre valeur salt, vous pouvez également ajouter **/Salt <saltvalue>** à la commande.</span><span class="sxs-lookup"><span data-stu-id="7d636-350">Optionally, if you want to use your own salt value, add the **/Salt <saltvalue>** to the command.</span></span> <span data-ttu-id="7d636-351">Cette valeur doit comporter 64 caractères et ne peut contenir que les caractères allant de a à z et de 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="7d636-351">This value must be 64 characters in length and can only contain the a-z characters and 0-9 characters.</span></span>

5. <span data-ttu-id="7d636-352">Vérifiez l’état du chargement en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7d636-352">Check the upload status by running this command:</span></span>

   `EdmUploadAgent.exe /GetSession /DataStoreName \<DataStoreName\>`

   <span data-ttu-id="7d636-353">Exemple : **EdmUploadAgent.exe /GetSession /DataStoreName PatientRecords**</span><span class="sxs-lookup"><span data-stu-id="7d636-353">Example: **EdmUploadAgent.exe /GetSession /DataStoreName PatientRecords**</span></span>

   <span data-ttu-id="7d636-354">Vous verrez l’état **ProcessingInProgress**.</span><span class="sxs-lookup"><span data-stu-id="7d636-354">Look for the status to be in **ProcessingInProgress**.</span></span> <span data-ttu-id="7d636-355">Vérifiez à quelques minutes d’intervalle jusqu’à ce que l’état devienne **Completed**.</span><span class="sxs-lookup"><span data-stu-id="7d636-355">Check again every few minutes until the status changes to **Completed**.</span></span> <span data-ttu-id="7d636-356">Une fois que le chargement est à l’état Completed, vos données EDM sont prêtes à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="7d636-356">Once the status is completed, your EDM data is ready for use.</span></span>

#### <a name="separate-hash-and-upload"></a><span data-ttu-id="7d636-357">Séparer le hachage et le chargement</span><span class="sxs-lookup"><span data-stu-id="7d636-357">Separate Hash and upload</span></span>

<span data-ttu-id="7d636-358">Effectuez le hachage sur un ordinateur dans un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7d636-358">Perform the hash on a computer in a secure environment.</span></span>

<span data-ttu-id="7d636-359">FACULTATIF : si vous avez utilisé l’Assistant de schéma de correspondance exacte des données et de type d’informations sensibles pour créer vos fichiers de schéma et de modèle, exécutez la commande suivante dans une fenêtre Invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="7d636-359">OPTIONAL: If you used the Exact Data Match schema and sensitive information type wizard to create your schema and pattern files, run the following command in a Command Prompt window:</span></span>

`EdmUploadAgent.exe /SaveSchema /DataStoreName <schema name> /OutputDir <path to output folder>`

1. <span data-ttu-id="7d636-360">À l’invite de commandes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7d636-360">Run the following command in Command Prompt windows:</span></span>

   `EdmUploadAgent.exe /CreateHash /DataFile [data file] /HashLocation [hash file location] /Schema [Schema file] >`

   <span data-ttu-id="7d636-361">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7d636-361">For example:</span></span>

   > <span data-ttu-id="7d636-362">**EdmUploadAgent.exe /CreateHash /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash /Schema edm.xml**</span><span class="sxs-lookup"><span data-stu-id="7d636-362">**EdmUploadAgent.exe /CreateHash /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash /Schema edm.xml**</span></span>

   <span data-ttu-id="7d636-363">Cela génère un fichier haché et un fichier salt avec les extensions suivantes si vous n’avez pas spécifié l’option **/Salt <saltvalue>**  :</span><span class="sxs-lookup"><span data-stu-id="7d636-363">This will output a hashed file and a salt file with these extensions if you didn't specify the **/Salt <saltvalue>** option:</span></span>
   - <span data-ttu-id="7d636-364">.EdmHash</span><span class="sxs-lookup"><span data-stu-id="7d636-364">.EdmHash</span></span>
   - <span data-ttu-id="7d636-365">.EdmSalt</span><span class="sxs-lookup"><span data-stu-id="7d636-365">.EdmSalt</span></span>

2. <span data-ttu-id="7d636-366">Copiez ces fichiers de manière sécurisée sur l’ordinateur que vous utiliserez pour télécharger vos éléments sensibles .csv ou .tsv (PatientRecords) vers votre client.</span><span class="sxs-lookup"><span data-stu-id="7d636-366">Copy these files in a secure fashion to the computer you will use to upload your sensitive items .csv or .tsv file (PatientRecords) to your tenant.</span></span>

   <span data-ttu-id="7d636-367">Pour charger les données hachées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="7d636-367">To upload the hashed data, run the following command in Windows Command Prompt:</span></span>

   `EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

   <span data-ttu-id="7d636-368">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="7d636-368">For example:</span></span>

   > <span data-ttu-id="7d636-369">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="7d636-369">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span></span>


   <span data-ttu-id="7d636-370">Pour vérifier que vos données sensibles ont été téléchargées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="7d636-370">To verify that your sensitive data has been uploaded, run the following command in Command Prompt window:</span></span>

   `EdmUploadAgent.exe /GetDataStore`

   <span data-ttu-id="7d636-371">La liste des magasins de données apparaît, ainsi que la date de la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7d636-371">You'll see a list of data stores and when they were last updated.</span></span>

   <span data-ttu-id="7d636-372">Si vous voulez afficher toutes les données téléchargées vers un magasin particulier, exécutez la commande suivante dans une invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="7d636-372">If you want to see all the data uploads to a particular store, run the following command in a Windows command prompt:</span></span>

   `EdmUploadAgent.exe /GetSession /DataStoreName <DataStoreName>`

   <span data-ttu-id="7d636-373">Poursuivez la configuration de votre processus et planifiez l’[actualisation de votre base de données d'informations sensibles](#refreshing-your-sensitive-information-database).</span><span class="sxs-lookup"><span data-stu-id="7d636-373">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="7d636-374">À ce stade, vous êtes prêt à utiliser la classification basée sur EDM avec vos services de Cloud Computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d636-374">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="7d636-375">Par exemple, vous pouvez [configurer une stratégie DLP à l’aide d’une classification basée sur EDM](#to-create-a-dlp-policy-with-edm).</span><span class="sxs-lookup"><span data-stu-id="7d636-375">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span>

#### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="7d636-376">Actualisation de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-376">Refreshing your sensitive information database</span></span>

<span data-ttu-id="7d636-377">Vous pouvez actualiser quotidiennement votre base de données d’informations sensibles, et l’outil de chargement EDM peut réindexer les données sensibles, puis recharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="7d636-377">You can refresh your sensitive information database daily, and the EDM Upload Tool can reindex the sensitive data and then reupload the indexed data.</span></span>

1. <span data-ttu-id="7d636-378">Déterminez vos processus et leur fréquence (quotidien ou hebdomadaire) pour actualiser la base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="7d636-378">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="7d636-379">Réexportez les données sensibles vers une application, telle que Microsoft Excel, et enregistrez le fichier au format .csv ou .tsv.</span><span class="sxs-lookup"><span data-stu-id="7d636-379">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv or .tsv format.</span></span> <span data-ttu-id="7d636-380">Conservez le même nom de fichier et l’emplacement que vous avez utilisé lorsque vous avez suivi les étapes décrites dans[Hachage et téléchargement des données sensibles](#part-2-hash-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="7d636-380">Keep the same file name and location you used when you followed the steps described in [Hash and upload the sensitive data](#part-2-hash-and-upload-the-sensitive-data).</span></span>

      > [!NOTE]
      > <span data-ttu-id="7d636-381">Si aucune modification n’est apportée à la structure (noms de champs) du fichier .csv ou .tsv, vous n’avez pas besoin d’apporter des modifications à votre fichier de schéma de base de données lorsque vous actualisez les données.</span><span class="sxs-lookup"><span data-stu-id="7d636-381">If there are no changes to the structure (field names) of the .csv or .tsv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="7d636-382">Si vous devez apporter des modifications, assurez-vous de modifier le schéma de base de données et votre package de règles en conséquence.</span><span class="sxs-lookup"><span data-stu-id="7d636-382">But if you must make changes, make sure to edit the database schema and your rule package accordingly.</span></span>

3. <span data-ttu-id="7d636-383">Utilisez [le planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page) pour automatiser les étapes 2 et 3 dans la procédure[hacher et télécharger les données sensibles](#part-2-hash-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="7d636-383">Use [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Hash and upload the sensitive data](#part-2-hash-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="7d636-384">Vous pouvez planifier des tâches à l’aide de plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="7d636-384">You can schedule tasks using several methods:</span></span>

      | <span data-ttu-id="7d636-385">Méthode</span><span class="sxs-lookup"><span data-stu-id="7d636-385">Method</span></span>             | <span data-ttu-id="7d636-386">Procédure</span><span class="sxs-lookup"><span data-stu-id="7d636-386">What to do</span></span> |
      | ---------------------- | ---------------- |
      | <span data-ttu-id="7d636-387">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d636-387">Windows PowerShell</span></span>     | <span data-ttu-id="7d636-388">Consultez la documentation[ScheduledTasks](/powershell/module/scheduledtasks/?view=win10-ps) et l’[exemple de script PowerShell](#example-powershell-script-for-task-scheduler) dans cet article</span><span class="sxs-lookup"><span data-stu-id="7d636-388">See the [ScheduledTasks](/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span> |
      | <span data-ttu-id="7d636-389">API planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7d636-389">Task Scheduler API</span></span>     | <span data-ttu-id="7d636-390">Consultez la documentation relative au [planificateur de tâches](/windows/desktop/TaskSchd/using-the-task-scheduler)</span><span class="sxs-lookup"><span data-stu-id="7d636-390">See the [Task Scheduler](/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span>                                                                                                                                                                                                                                                                                |
      | <span data-ttu-id="7d636-391">Interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="7d636-391">Windows user interface</span></span> | <span data-ttu-id="7d636-392">Dans Windows, cliquez sur **Démarrer**, puis tapez Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7d636-392">In Windows, click **Start**, and type Task Scheduler.</span></span> <span data-ttu-id="7d636-393">Dans la liste des résultats, cliquez avec le bouton droit sur **planificateur de tâches**, puis sélectionnez **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="7d636-393">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="7d636-394">Exemple de script PowerShell pour le planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="7d636-394">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="7d636-395">Cette section inclut un exemple de script PowerShell que vous pouvez utiliser pour planifier vos tâches de hachage de données et de téléchargement des données hachées :</span><span class="sxs-lookup"><span data-stu-id="7d636-395">This section includes an example PowerShell script you can use to schedule your tasks for hashing data and uploading the hashed data:</span></span>

##### <a name="to-schedule-hashing-and-upload-in-a-combined-step"></a><span data-ttu-id="7d636-396">Pour planifier un hachage et effectuer un téléchargement dans une étape seule combinée</span><span class="sxs-lookup"><span data-stu-id="7d636-396">To schedule hashing and upload in a combined step</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$schemaext = '.xml'
\# Assuming file name is same as data store name and file is in .csv format
$dataFile = "$fileLocation\\$dataStoreName$csvext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
\# Assuming Schema file name is same as data store name
$schemaFile = "$fileLocation\\$dataStoreName$schemaext"
$uploadDataArgs = '/UploadData /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation' + $hashLocation + ' /Schema ' + $schemaFile
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadDataArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```

#### <a name="to-schedule-hashing-and-upload-as-separate-steps"></a><span data-ttu-id="7d636-397">Pour planifier un hachage et effectuer un téléchargement en deux étapes distinctes</span><span class="sxs-lookup"><span data-stu-id="7d636-397">To schedule hashing and upload as separate steps</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
$schemaext = '.xml'
\# Assuming file name is same as data store name and file is in .csv format
$dataFile = "$fileLocation\\$dataStoreName$csvext"
$hashFile = "$fileLocation\\$dataStoreName$edmext"
\# Assuming Schema file name is same as data store name
$schemaFile = "$fileLocation\\$dataStoreName$schemaext "

\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash' + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation + ' /Schema ' + $schemaFile
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
\# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
\# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
\# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
\# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
\# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=\[Runtime.InteropServices.Marshal\]::PtrToStringAuto(\[Runtime.InteropServices.Marshal\]::SecureStringToBSTR($creds.Password))
\# Register the scheduled task
$taskName = 'EDMUpload\_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password

```

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="7d636-398">Partie 3 : utiliser la classification EDM avec vos services de cloud computing Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d636-398">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="7d636-399">Ces emplacements prennent en charge les types d’informations sensibles EDM :</span><span class="sxs-lookup"><span data-stu-id="7d636-399">These locations are support EDM sensitive information types:</span></span>

- <span data-ttu-id="7d636-400">DLP pour Exchange Online (e-mail)</span><span class="sxs-lookup"><span data-stu-id="7d636-400">DLP for Exchange Online (email)</span></span>
- <span data-ttu-id="7d636-401">OneDrive Entreprise (fichiers)</span><span class="sxs-lookup"><span data-stu-id="7d636-401">OneDrive for Business (files)</span></span>
- <span data-ttu-id="7d636-402">Microsoft Teams (conversations)</span><span class="sxs-lookup"><span data-stu-id="7d636-402">Microsoft Teams (conversations)</span></span>
- <span data-ttu-id="7d636-403">DLP pour SharePoint (fichiers)</span><span class="sxs-lookup"><span data-stu-id="7d636-403">DLP for SharePoint (files)</span></span>
- <span data-ttu-id="7d636-404">Stratégies DLP de la sécurité de l’application Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="7d636-404">Microsoft Cloud App Security DLP policies</span></span>
- <span data-ttu-id="7d636-405">Stratégies d’étiquetage automatique côté serveur : disponibles pour les clients du cloud commercial et les clients cloud du secteur public</span><span class="sxs-lookup"><span data-stu-id="7d636-405">Server-side auto-labeling policies - available for commercial cloud customers and government cloud customers</span></span>

#### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="7d636-406">Pour créer une stratégie DLP avec EDM</span><span class="sxs-lookup"><span data-stu-id="7d636-406">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="7d636-407">Accédez au Centre de conformité et de sécurité à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription).</span><span class="sxs-lookup"><span data-stu-id="7d636-407">Go to the Security & Compliance Center using the appropriate [link for your subscription](#portal-links-for-your-subscription).</span></span>

2. <span data-ttu-id="7d636-408">Sélectionnez stratégie de **Protection contre la perte de données** \> \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="7d636-408">Choose **Data loss prevention** \> **Policy**.</span></span>

3. <span data-ttu-id="7d636-409">Sélectionnez **Créer une stratégie** \> **Personnaliser** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-409">Choose **Create a policy** \> **Custom** \> **Next**.</span></span>

4. <span data-ttu-id="7d636-410">Sous l'onglet **Nommez votre stratégie**, spécifiez un nom et une description, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-410">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="7d636-411">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-411">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span>

6. <span data-ttu-id="7d636-412">Dans la colonne **État**, sélectionnez **Courrier Exchange, Comptes OneDrive, Messages de conversation et de canal de Teams**, puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-412">In the **Status** column, select **Exchange email, OneDrive accounts, Teams chat and channel message**, and then choose **Next**.</span></span>

7. <span data-ttu-id="7d636-413">Sous l'onglet **paramètres de stratégie**, sélectionnez **utiliser les paramètres avancés**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-413">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span>

8. <span data-ttu-id="7d636-414">Sélectionnez **+ Nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="7d636-414">Choose **+ New rule**.</span></span>

9. <span data-ttu-id="7d636-415">Dans la section **Nom**, spécifiez un nom et une description pour la règle.</span><span class="sxs-lookup"><span data-stu-id="7d636-415">In the **Name** section, specify a name and description for the rule.</span></span>

10. <span data-ttu-id="7d636-416">Dans la section **conditions**, dans la liste **+ ajouter une condition**, sélectionnez **le contenu contient un type de contenu sensible**.</span><span class="sxs-lookup"><span data-stu-id="7d636-416">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span>

      ![Le contenu contient des types d’informations sensibles](../media/edm-dlp-newrule-conditions.png)

11. <span data-ttu-id="7d636-418">Recherchez le type d’informations sensibles que vous avez créé lorsque vous avez configuré votre package de règles, puis sélectionnez **+ ajouter**.</span><span class="sxs-lookup"><span data-stu-id="7d636-418">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span>  
    <span data-ttu-id="7d636-419">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="7d636-419">Then choose **Done**.</span></span>

12. <span data-ttu-id="7d636-420">Terminez de sélectionner les options de votre règle, telles que **notifications d’utilisateur**,**remplacements d’utilisateur**, **rapports d’incident**, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7d636-420">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="7d636-421">Sous l'onglet **paramètres de stratégie**, passez en revue vos règles, puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-421">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="7d636-422">Indiquez si vous voulez activer la stratégie immédiatement, tester celle-ci ou la maintenir désactivée.</span><span class="sxs-lookup"><span data-stu-id="7d636-422">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="7d636-423">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7d636-423">Then choose **Next**.</span></span>

15. <span data-ttu-id="7d636-424">Sous l'onglet **Vérifier vos paramètres**, passez en revue votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="7d636-424">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="7d636-425">Apportez les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7d636-425">Make any needed changes.</span></span> <span data-ttu-id="7d636-426">Lorsque vous avez terminé, sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="7d636-426">When you're ready, choose **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="7d636-427">Comptez environ une heure avant que votre nouvelle stratégie DLP soit appliquée à l’ensemble de votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="7d636-427">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="7d636-428">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="7d636-428">Related articles</span></span>

- [<span data-ttu-id="7d636-429">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="7d636-429">Sensitive information type-entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- <span data-ttu-id="7d636-430">[En savoir plus sur les types d’informations confidentielles](sensitive-information-type-learn-about.md).</span><span class="sxs-lookup"><span data-stu-id="7d636-430">[Learn about sensitive information types](sensitive-information-type-learn-about.md)</span></span>
- [<span data-ttu-id="7d636-431">En savoir plus sur la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="7d636-431">Learn about data loss prevention</span></span>](dlp-learn-about-dlp.md)
- [<span data-ttu-id="7d636-432">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="7d636-432">Microsoft Cloud App Security</span></span>](/cloud-app-security)
- [<span data-ttu-id="7d636-433">New-DlpEdmSchema</span><span class="sxs-lookup"><span data-stu-id="7d636-433">New-DlpEdmSchema</span></span>](/powershell/module/exchange/new-dlpedmschema)
- [<span data-ttu-id="7d636-434">Modifier le schéma de correspondance des données exactes pour utiliser la correspondance configurable</span><span class="sxs-lookup"><span data-stu-id="7d636-434">Modify Exact Data Match schema to use configurable match</span></span>](sit-modify-edm-schema-configurable-match.md)
