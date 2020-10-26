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
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment créer des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 229eb733af85ea5f450969c6d70709cfadcb8f06
ms.sourcegitcommit: 554755bc9ce40228ce6e34bde6fc6e226869b6a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48681772"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a><span data-ttu-id="d9b32-103">Créez des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.</span><span class="sxs-lookup"><span data-stu-id="d9b32-103">Create custom sensitive information types with Exact Data Match based classification</span></span>

<span data-ttu-id="d9b32-104">[Les types d’informations sensibles personnalisés](custom-sensitive-info-types.md) sont utilisés pour vous aider à identifier les éléments sensibles afin de pouvoir empêcher leur partage par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="d9b32-104">[Custom sensitive information types](custom-sensitive-info-types.md) are used to help identify sensitive items so that you can prevent them from being inadvertently or inappropriately shared.</span></span> <span data-ttu-id="d9b32-105">Vous pouvez définir un type d’informations sensibles personnalisé sur la base des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d9b32-105">You define a custom sensitive information type based on:</span></span>

- <span data-ttu-id="d9b32-106">modèles</span><span class="sxs-lookup"><span data-stu-id="d9b32-106">patterns</span></span>
- <span data-ttu-id="d9b32-107">mots clés de preuve, tels que*employé*,*badge* ou *ID*</span><span class="sxs-lookup"><span data-stu-id="d9b32-107">keyword evidence such as *employee*, *badge*, or *ID*</span></span>
- <span data-ttu-id="d9b32-108">caractère à proximité de la preuve dans un modèle particulier</span><span class="sxs-lookup"><span data-stu-id="d9b32-108">character proximity to evidence in a particular pattern</span></span>
- <span data-ttu-id="d9b32-109">niveaux de confiance</span><span class="sxs-lookup"><span data-stu-id="d9b32-109">confidence levels</span></span>

 <span data-ttu-id="d9b32-110">De tels types d’informations sensibles personnalisés répondent aux besoins métier de nombreuses organisations.</span><span class="sxs-lookup"><span data-stu-id="d9b32-110">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="d9b32-111">Mais que se passe-t-il si vous voulez utiliser un type d’informations sensibles personnalisé qui utilise des valeurs de données exactes au lieu d’établir des concordances avec des modèles génériques ?</span><span class="sxs-lookup"><span data-stu-id="d9b32-111">But what if you wanted a custom sensitive information type that uses exact data values, instead of one that found matches based on generic patterns?</span></span> <span data-ttu-id="d9b32-112">Une classification Exact Data Match (EDM) vous permet de créer un type d’informations sensibles personnalisé conçu pour :</span><span class="sxs-lookup"><span data-stu-id="d9b32-112">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>

- <span data-ttu-id="d9b32-113">être dynamique et actualisable ;</span><span class="sxs-lookup"><span data-stu-id="d9b32-113">be dynamic and refreshable</span></span>
- <span data-ttu-id="d9b32-114">être plus évolutif ;</span><span class="sxs-lookup"><span data-stu-id="d9b32-114">be more scalable</span></span>
- <span data-ttu-id="d9b32-115">entraîner moins de faux positifs ;</span><span class="sxs-lookup"><span data-stu-id="d9b32-115">result in fewer false-positives</span></span>
- <span data-ttu-id="d9b32-116">utiliser des données sensibles structurées ;</span><span class="sxs-lookup"><span data-stu-id="d9b32-116">work with structured sensitive data</span></span>
- <span data-ttu-id="d9b32-117">gérer les informations sensibles de manière plus sécurisée ;</span><span class="sxs-lookup"><span data-stu-id="d9b32-117">handle sensitive information more securely</span></span>
- <span data-ttu-id="d9b32-118">être utilisé avec différents services de cloud computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9b32-118">be used with several Microsoft cloud services</span></span>

![Classification EDM](../media/EDMClassification.png)

<span data-ttu-id="d9b32-120">La classification EDM vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="d9b32-120">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="d9b32-121">La base de données peut être actualisée quotidiennement et peut contenir jusqu’à 100 millions de lignes de données.</span><span class="sxs-lookup"><span data-stu-id="d9b32-121">The database can be refreshed daily, and contain up to 100 million rows of data.</span></span> <span data-ttu-id="d9b32-122">À mesure que des employés, patients ou clients vont et viennent, et que les enregistrements changent, vos types d’informations sensibles personnalisés restent à jour et valides.</span><span class="sxs-lookup"><span data-stu-id="d9b32-122">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="d9b32-123">Vous pouvez également utiliser la classification basée sur EDM avec des stratégies, telles [que les stratégies de protection contre la perte de données](data-loss-prevention-policies.md) (DLP) ou [les stratégies de fichier de Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="d9b32-123">And, you can use EDM-based classification with policies, such as [data loss prevention policies](data-loss-prevention-policies.md) (DLP) or [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="d9b32-124">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="d9b32-124">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="d9b32-125">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="d9b32-125">Chinese (simplified)</span></span>
> - <span data-ttu-id="d9b32-126">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="d9b32-126">Chinese (traditional)</span></span>
> - <span data-ttu-id="d9b32-127">Korean</span><span class="sxs-lookup"><span data-stu-id="d9b32-127">Korean</span></span>
> - <span data-ttu-id="d9b32-128">Japanese</span><span class="sxs-lookup"><span data-stu-id="d9b32-128">Japanese</span></span>

><span data-ttu-id="d9b32-129">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="d9b32-129">This support is available for sensitive information types.</span></span> <span data-ttu-id="d9b32-130">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="d9b32-130">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="d9b32-131">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="d9b32-131">Required licenses and permissions</span></span>

<span data-ttu-id="d9b32-132">Vous devez être un administrateur général, un administrateur de conformité ou un administrateur Exchange Online pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="d9b32-132">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="d9b32-133">Pour en avoir plus sur les autorisations DLP, consultez la section[Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="d9b32-133">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

<span data-ttu-id="d9b32-134">La classification EDM est incluse dans ces abonnements</span><span class="sxs-lookup"><span data-stu-id="d9b32-134">EDM-based classification is included in these subscriptions</span></span>

- <span data-ttu-id="d9b32-135">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="d9b32-135">Office 365 E5</span></span>
- <span data-ttu-id="d9b32-136">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="d9b32-136">Microsoft 365 E5</span></span>
- <span data-ttu-id="d9b32-137">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="d9b32-137">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="d9b32-138">Microsoft E5/A5 Information Protection et gouvernance</span><span class="sxs-lookup"><span data-stu-id="d9b32-138">Microsoft E5/A5 Information Protection and Governance</span></span>

## <a name="portal-links-for-your-subscription"></a><span data-ttu-id="d9b32-139">Liens vers les portails de votre abonnement</span><span class="sxs-lookup"><span data-stu-id="d9b32-139">Portal links for your subscription</span></span>


|<span data-ttu-id="d9b32-140">Portail</span><span class="sxs-lookup"><span data-stu-id="d9b32-140">Portal</span></span>  |<span data-ttu-id="d9b32-141">World Wide/GCC</span><span class="sxs-lookup"><span data-stu-id="d9b32-141">World Wide/GCC</span></span>  |<span data-ttu-id="d9b32-142">GCC-High</span><span class="sxs-lookup"><span data-stu-id="d9b32-142">GCC-High</span></span>  |<span data-ttu-id="d9b32-143">DOD</span><span class="sxs-lookup"><span data-stu-id="d9b32-143">DOD</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="d9b32-144">Office SCC</span><span class="sxs-lookup"><span data-stu-id="d9b32-144">Office SCC</span></span>     |  <span data-ttu-id="d9b32-145">protection.office.com</span><span class="sxs-lookup"><span data-stu-id="d9b32-145">protection.office.com</span></span>       |<span data-ttu-id="d9b32-146">scc.office365.us</span><span class="sxs-lookup"><span data-stu-id="d9b32-146">scc.office365.us</span></span>         |<span data-ttu-id="d9b32-147">scc.protection.apps.mil</span><span class="sxs-lookup"><span data-stu-id="d9b32-147">scc.protection.apps.mil</span></span> |
|<span data-ttu-id="d9b32-148">Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d9b32-148">Microsoft 365 Security center</span></span>     |<span data-ttu-id="d9b32-149">security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d9b32-149">security.microsoft.com</span></span>         |<span data-ttu-id="d9b32-150">security.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="d9b32-150">security.microsoft.us</span></span>         |<span data-ttu-id="d9b32-151">security.apps.mil</span><span class="sxs-lookup"><span data-stu-id="d9b32-151">security.apps.mil</span></span>|
|<span data-ttu-id="d9b32-152">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d9b32-152">Microsoft 365 Compliance center</span></span>     |<span data-ttu-id="d9b32-153">compliance.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="d9b32-153">compliance.microsoft.com</span></span>         |<span data-ttu-id="d9b32-154">compliance.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="d9b32-154">compliance.microsoft.us</span></span>         |<span data-ttu-id="d9b32-155">compliance.apps.mil</span><span class="sxs-lookup"><span data-stu-id="d9b32-155">compliance.apps.mil</span></span>|


## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="d9b32-156">Flux de travail en un clin d’œil</span><span class="sxs-lookup"><span data-stu-id="d9b32-156">The work flow at a glance</span></span>

|<span data-ttu-id="d9b32-157">Phase</span><span class="sxs-lookup"><span data-stu-id="d9b32-157">Phase</span></span>  |<span data-ttu-id="d9b32-158">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="d9b32-158">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="d9b32-159">Partie 1: configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-159">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="d9b32-160">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="d9b32-160">(As needed)</span></span><br/><span data-ttu-id="d9b32-161">- [Modifier le schéma de base de données](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="d9b32-161">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="d9b32-162">- [Supprimer le schéma](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="d9b32-162">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="d9b32-163">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-163">- Read access to the sensitive data</span></span><br/><span data-ttu-id="d9b32-164">-Schéma de base de données au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="d9b32-164">- Database schema in XML format (example provided)</span></span><br/><span data-ttu-id="d9b32-165">-Package de règles au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="d9b32-165">- Rule package in XML format (example provided)</span></span><br/><span data-ttu-id="d9b32-166">-Autorisations d’administrateur sur le centre de sécurité & conformité (à l’aide de PowerShell)</span><span class="sxs-lookup"><span data-stu-id="d9b32-166">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="d9b32-167">Partie 2 : hacher et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-167">Part 2: Hash and upload the sensitive data</span></span>](#part-2-hash-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="d9b32-168">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="d9b32-168">(As needed)</span></span><br/>[<span data-ttu-id="d9b32-169">Actualiser les données</span><span class="sxs-lookup"><span data-stu-id="d9b32-169">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="d9b32-170">-Groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d9b32-170">- Custom security group and user account</span></span><br/><span data-ttu-id="d9b32-171">-Accès administrateur local à l’ordinateur à l’aide de l’agent de téléchargement EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-171">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="d9b32-172">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-172">- Read access to the sensitive data</span></span><br/><span data-ttu-id="d9b32-173">-Processus et planification pour l’actualisation des données</span><span class="sxs-lookup"><span data-stu-id="d9b32-173">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="d9b32-174">Partie 3: utiliser la classification EDM avec vos services Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="d9b32-174">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="d9b32-175">- Abonnement Microsoft 365 avec DLP</span><span class="sxs-lookup"><span data-stu-id="d9b32-175">- Microsoft 365 subscription with DLP</span></span><br/><span data-ttu-id="d9b32-176">- Fonctionnalité de classification EDM activée</span><span class="sxs-lookup"><span data-stu-id="d9b32-176">- EDM-based classification feature enabled</span></span> |

### <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="d9b32-177">Partie 1 : configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-177">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="d9b32-178">La configuration de la classification basée sur EDM inclut les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9b32-178">Setting up and configuring EDM-based classification involves:</span></span>

1. [<span data-ttu-id="d9b32-179">Enregistrement des données sensibles au format .csv</span><span class="sxs-lookup"><span data-stu-id="d9b32-179">Saving sensitive data in .csv format</span></span>](#save-sensitive-data-in-csv-format)
2. [<span data-ttu-id="d9b32-180">Définition de votre schéma de base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-180">Define your sensitive information database schema</span></span>](#define-the-schema-for-your-database-of-sensitive-information)
3. [<span data-ttu-id="d9b32-181">Création d’un package de règles</span><span class="sxs-lookup"><span data-stu-id="d9b32-181">Create a rule package</span></span>](#set-up-a-rule-package)


#### <a name="save-sensitive-data-in-csv-format"></a><span data-ttu-id="d9b32-182">Enregistrer des données sensibles au format .csv</span><span class="sxs-lookup"><span data-stu-id="d9b32-182">Save sensitive data in .csv format</span></span>

1. <span data-ttu-id="d9b32-183">Identifiez les informations sensibles que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="d9b32-183">Identify the sensitive information you want to use.</span></span> <span data-ttu-id="d9b32-184">Exportez les données vers une application, telle que Microsoft Excel, puis enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="d9b32-184">Export the data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="d9b32-185">Le fichier de données peut inclure au maximum :</span><span class="sxs-lookup"><span data-stu-id="d9b32-185">The data file can include a maximum of:</span></span>
      - <span data-ttu-id="d9b32-186">100 millions de lignes de données sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-186">Up to 100 million rows of sensitive data</span></span>
      - <span data-ttu-id="d9b32-187">32 colonnes (champs) par source de données</span><span class="sxs-lookup"><span data-stu-id="d9b32-187">Up to 32 columns (fields) per data source</span></span>
      - <span data-ttu-id="d9b32-188">5 colonnes (champs) marquées comme pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="d9b32-188">Up to 5 columns (fields) marked as searchable</span></span>

2. <span data-ttu-id="d9b32-189">Structurez les données sensibles dans le fichier .csv de telle sorte que la première ligne contienne les noms des champs utilisés pour la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="d9b32-189">Structure the sensitive data in the .csv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="d9b32-190">Votre fichier .csv contient peut-être des noms de champs, tels que « ssn », « birthdate », « firstname » et « lastname ».</span><span class="sxs-lookup"><span data-stu-id="d9b32-190">In your .csv file, you might have field names, such as "ssn", "birthdate", "firstname", "lastname".</span></span> <span data-ttu-id="d9b32-191">Les noms d’en-tête de colonne ne peuvent pas contenir des espaces ni des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="d9b32-191">The column header names can't include spaces or underscores.</span></span> <span data-ttu-id="d9b32-192">Par exemple, le fichier .csv utilisé dans cet exemple est appelé *PatientRecords.csv*. Ses colonnes incluent *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN*, etc.</span><span class="sxs-lookup"><span data-stu-id="d9b32-192">For example, the sample .csv file that we use in this article is named *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN*, and more.</span></span>

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="d9b32-193">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-193">Define the schema for your database of sensitive information</span></span>

3. <span data-ttu-id="d9b32-194">Définissez le schéma pour la base de données d’informations sensibles dans un fichier XML (comme dans l’exemple ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="d9b32-194">Define the schema for the database of sensitive information in XML format (similar to our example below).</span></span> <span data-ttu-id="d9b32-195">Nommez ce fichier de schéma**edm.xml** et configurez-le de telle sorte que pour chaque colonne de la base de données, une ligne utilise la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="d9b32-195">Name this schema file **edm.xml**, and configure it such that for each column in the database, there is a line that uses the syntax:</span></span> 

      <span data-ttu-id="d9b32-196">`\<Field name="" searchable=""/\>`.</span><span class="sxs-lookup"><span data-stu-id="d9b32-196">`\<Field name="" searchable=""/\>`.</span></span>

      - <span data-ttu-id="d9b32-197">Utilisez les noms de colonne pour les valeurs de *nom de champ*.</span><span class="sxs-lookup"><span data-stu-id="d9b32-197">Use column names for *Field name* values.</span></span>
      - <span data-ttu-id="d9b32-198">Utilisez *searchable="true"* pour jusqu’à 5 champs dont vous voulez qu’il puissent faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="d9b32-198">Use *searchable="true"* for the fields that you want to be searchable up to a maximum of 5 fields.</span></span> <span data-ttu-id="d9b32-199">Au moins un champ doit pouvoir faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="d9b32-199">At least one field must be searchable.</span></span>

      <span data-ttu-id="d9b32-200">Par exemple, le fichier XML suivant définit le schéma d’une base de données de dossiers de patients, avec cinq champs pouvant faire l’objet d’une recherche : *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span><span class="sxs-lookup"><span data-stu-id="d9b32-200">As an example, the following XML file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span>

      <span data-ttu-id="d9b32-201">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="d9b32-201">(You can copy, modify, and use our example.)</span></span>

      ```xml
      <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
            <DataStore name="PatientRecords" description="Schema for patient records" version="1">
                  <Field name="PatientID" searchable="true" />
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

4. <span data-ttu-id="d9b32-202">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="d9b32-202">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

5. <span data-ttu-id="d9b32-203">Pour charger le schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="d9b32-203">To upload the database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="d9b32-204">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9b32-204">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="d9b32-205">Confirmer</span><span class="sxs-lookup"><span data-stu-id="d9b32-205">Confirm</span></span>
      >
      > <span data-ttu-id="d9b32-206">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="d9b32-206">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="d9b32-207">Un nouveau schéma EDM pour le magasin de données « patientrecords » va être importé.</span><span class="sxs-lookup"><span data-stu-id="d9b32-207">New EDM Schema for the data store 'patientrecords' will be imported.</span></span>
      >
      > <span data-ttu-id="d9b32-208">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="d9b32-208">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="d9b32-209">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 5, utilisez plutôt la cmdlet New-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="d9b32-209">If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: New-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="d9b32-210">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="d9b32-210">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d9b32-211">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="d9b32-211">The update must complete before you execute steps that use the additions.</span></span>

#### <a name="set-up-a-rule-package"></a><span data-ttu-id="d9b32-212">Configurer un package de règles</span><span class="sxs-lookup"><span data-stu-id="d9b32-212">Set up a rule package</span></span>

1. <span data-ttu-id="d9b32-213">Créez un package de règles au format XML (avec codage Unicode) similaire à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="d9b32-213">Create a rule package in XML format (with Unicode encoding), similar to the following example.</span></span> <span data-ttu-id="d9b32-214">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="d9b32-214">(You can copy, modify, and use our example.)</span></span>

      <span data-ttu-id="d9b32-215">Lorsque vous configurez votre package de règles, veillez à référencer correctement vos fichier .csv et **edm.xml**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-215">When you set up your rule package, make sure to correctly reference your .csv file and **edm.xml** file.</span></span> <span data-ttu-id="d9b32-216">Vous pouvez copier, modifier et utiliser notre exemple.</span><span class="sxs-lookup"><span data-stu-id="d9b32-216">You can copy, modify, and use our example.</span></span> <span data-ttu-id="d9b32-217">Dans cet exemple de fichier xml, les champs suivants doivent être personnalisés pour créer votre type sensible d’EDM :</span><span class="sxs-lookup"><span data-stu-id="d9b32-217">In this sample xml the following fields needs to be customized to create your EDM sensitive type:</span></span>

      - <span data-ttu-id="d9b32-218">**RulePack id & ExactMatch id** : utilisez [New-GUID](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) pour générer un GUID.</span><span class="sxs-lookup"><span data-stu-id="d9b32-218">**RulePack id & ExactMatch id**: Use [New-GUID](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) to generate a GUID.</span></span>

      - <span data-ttu-id="d9b32-219">**Datastore** : ce champ spécifie le magasin de données de recherche EDM à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d9b32-219">**Datastore**: This field specifies EDM lookup data store to be used.</span></span> <span data-ttu-id="d9b32-220">Vous indiquez un nom de source de données ou un schéma EDM configuré.</span><span class="sxs-lookup"><span data-stu-id="d9b32-220">You provide a data source name of a configured EDM Schema.</span></span>

      - <span data-ttu-id="d9b32-221">**idMatch** : ce champ pointe vers l’élément principal pour EDM.</span><span class="sxs-lookup"><span data-stu-id="d9b32-221">**idMatch**: This field points to the primary element for EDM.</span></span>
        - <span data-ttu-id="d9b32-222">Matches : spécifie le champ à utiliser dans la recherche exacte.</span><span class="sxs-lookup"><span data-stu-id="d9b32-222">Matches: Specifies the field to be used in exact lookup.</span></span> <span data-ttu-id="d9b32-223">Vous fournissez un nom de champ pouvant faire l’objet d’une recherche dans le schéma EDM pour le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="d9b32-223">You provide a searchable field name in EDM Schema for the DataStore.</span></span>
        - <span data-ttu-id="d9b32-224">Classification : ce champ spécifie la correspondance de type sensible qui déclenche la recherche EDM.</span><span class="sxs-lookup"><span data-stu-id="d9b32-224">Classification: This field specifies the sensitive type match that triggers EDM lookup.</span></span> <span data-ttu-id="d9b32-225">Vous pouvez fournir le nom ou le GUID d’une classification personnalisée ou prédéfinie existante.</span><span class="sxs-lookup"><span data-stu-id="d9b32-225">You can provide Name or GUID of an existing built-in or custom classification.</span></span>

      - <span data-ttu-id="d9b32-226">**Match :** ce champ pointe vers d’autres preuves à proximité d’idMatch.</span><span class="sxs-lookup"><span data-stu-id="d9b32-226">**Match:** This field points to additional evidence found in proximity of idMatch.</span></span>
        - <span data-ttu-id="d9b32-227">Matches : vous indiquez un nom de champ dans le schéma EDM pour DataStore.</span><span class="sxs-lookup"><span data-stu-id="d9b32-227">Matches: You provide any field name in EDM Schema for DataStore.</span></span>
      - <span data-ttu-id="d9b32-228">**Resource :** cette section spécifie le nom et la description du type sensible dans plusieurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d9b32-228">**Resource:** This section specifies the name and description for sensitive type in multiple locales.</span></span>
        - <span data-ttu-id="d9b32-229">idRef : fournissez un GUID pour ExactMatch ID.</span><span class="sxs-lookup"><span data-stu-id="d9b32-229">idRef: You provide GUID for ExactMatch ID.</span></span>
        - <span data-ttu-id="d9b32-230">Nom et descriptions : personnalisez si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d9b32-230">Name & descriptions: customize as required.</span></span>

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

1. <span data-ttu-id="d9b32-231">Téléchargez le package de règles en exécutant les cmdlets PowerShell suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="d9b32-231">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

      ```powershell
      $rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
      New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
      ```

<span data-ttu-id="d9b32-232">À ce stade, vous avez configuré la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="d9b32-232">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="d9b32-233">L’étape suivante consiste à hacher les données sensibles, puis à charger les hachages pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="d9b32-233">The next step is to hash the sensitive data, and then upload the hashes for indexing.</span></span>

<span data-ttu-id="d9b32-234">Rappelez-vous que la procédure précédente de notre schéma PatientRecords définit cinq champs pouvant faire l’objet d’une recherche : *PatientID*,*MRN*, *SSN*, *Phone* et *DOB*.</span><span class="sxs-lookup"><span data-stu-id="d9b32-234">Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> <span data-ttu-id="d9b32-235">Notre exemple de package de règles inclut ces champs et référence le fichier de schéma de base de données (**edm.xml**), avec un seul élément *ExactMatch* par champ pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="d9b32-235">Our example rule package includes those fields and references the database schema file (**edm.xml**), with one *ExactMatch* item per searchable field.</span></span> <span data-ttu-id="d9b32-236">Prenons l’élément ExactMatch suivant :</span><span class="sxs-lookup"><span data-stu-id="d9b32-236">Consider the following ExactMatch item:</span></span>

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

<span data-ttu-id="d9b32-237">À partir de cet exemple, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="d9b32-237">In this example, note that:</span></span>

- <span data-ttu-id="d9b32-238">Le nom du magasin de données fait référence au fichier .csv que nous avons créé précédemment : **dataStore = "PatientRecords"**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-238">The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.</span></span>

- <span data-ttu-id="d9b32-239">La valeur idMatch fait référence à un champ pouvant faire l’objet d’une recherche figurant dans le fichier de schéma de base de données : **idMatch matches = "SSN"**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-239">The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.</span></span>

- <span data-ttu-id="d9b32-240">La valeur de classification fait référence à un type d’informations sensibles existant ou personnalisé : **classification = "U.S. Social Security Number (SSN)"**</span><span class="sxs-lookup"><span data-stu-id="d9b32-240">The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**.</span></span> <span data-ttu-id="d9b32-241">(en l’occurrence, nous utilisons le type d’informations sensibles existant pour le numéro de sécurité sociale aux États-Unis).</span><span class="sxs-lookup"><span data-stu-id="d9b32-241">(In this case, we use the existing sensitive information type of U.S. Social Security Number.)</span></span>

> [!NOTE]
> <span data-ttu-id="d9b32-242">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="d9b32-242">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d9b32-243">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="d9b32-243">The update must complete before you execute steps that use the additions.</span></span>

#### <a name="editing-the-schema-for-edm-based-classification"></a><span data-ttu-id="d9b32-244">Modification du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-244">Editing the schema for EDM-based classification</span></span>

<span data-ttu-id="d9b32-245">Si vous souhaitez modifier votre fichier **edm.xml**, par exemple pour changer les champs utilisés pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9b32-245">If you want to make changes to your **edm.xml** file, such as changing which fields are used for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="d9b32-246">Modifiez votre fichier **edm.xml** (présenté dans la section [Définir le schéma](#define-the-schema-for-your-database-of-sensitive-information) de cet article).</span><span class="sxs-lookup"><span data-stu-id="d9b32-246">Edit your **edm.xml** file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).</span></span>

2. <span data-ttu-id="d9b32-247">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="d9b32-247">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

3. <span data-ttu-id="d9b32-248">Pour mettre à jour votre schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="d9b32-248">To update your database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="d9b32-249">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9b32-249">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="d9b32-250">Confirmer</span><span class="sxs-lookup"><span data-stu-id="d9b32-250">Confirm</span></span>
      >
      > <span data-ttu-id="d9b32-251">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="d9b32-251">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="d9b32-252">Le schéma EDM pour le magasin de données « patientrecords » va être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="d9b32-252">EDM Schema for the data store 'patientrecords' will be updated.</span></span>
      >
      > <span data-ttu-id="d9b32-253">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="d9b32-253">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      > <span data-ttu-id="d9b32-254">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 3, utilisez plutôt la cmdlet Set-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="d9b32-254">If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: Set-DlpEdmSchema -FileData $edmSchemaXml</span></span>

      > [!NOTE]
      > <span data-ttu-id="d9b32-255">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="d9b32-255">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="d9b32-256">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="d9b32-256">The update must complete before you execute steps that use the additions.</span></span>

#### <a name="removing-the-schema-for-edm-based-classification"></a><span data-ttu-id="d9b32-257">Suppression du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-257">Removing the schema for EDM-based classification</span></span>

<span data-ttu-id="d9b32-258">(Le cas échéant) Si vous voulez supprimer le schéma que vous utilisez pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9b32-258">(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="d9b32-259">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="d9b32-259">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="d9b32-260">Exécutez les applets de commande PowerShell suivantes, en remplaçant le nom de magasin de données « patient records » par celui que vous voulez supprimer :</span><span class="sxs-lookup"><span data-stu-id="d9b32-260">Run the following PowerShell cmdlets, substituting the data store name of "patient records" with the one you want to remove:</span></span>

      ```powershell
      Remove-DlpEdmSchema -Identity patientrecords
      ```

      <span data-ttu-id="d9b32-261">Vous serez invité à confirmer :</span><span class="sxs-lookup"><span data-stu-id="d9b32-261">You will be prompted to confirm:</span></span>

      > <span data-ttu-id="d9b32-262">Confirmer</span><span class="sxs-lookup"><span data-stu-id="d9b32-262">Confirm</span></span>
      >
      > <span data-ttu-id="d9b32-263">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="d9b32-263">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="d9b32-264">Le schéma EDM pour le magasin de données « patientrecords » va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d9b32-264">EDM Schema for the data store 'patientrecords' will be removed.</span></span>
      >
      > <span data-ttu-id="d9b32-265">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="d9b32-265">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      >  <span data-ttu-id="d9b32-266">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 2, utilisez plutôt la cmdlet Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span><span class="sxs-lookup"><span data-stu-id="d9b32-266">If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span></span>


<!-- salt notes
need two salting procedures, one for onestep from the externally facing and another for two step, on an internal machine then the upload from the external machine

- create A  folder put the edmupload agent and, csv and salt file there, run all processes there
- 
- stuff you need to have first: DataStoreName, /DataFile name (csv file)  /Hashlocation

- salt can be randomly generated by Microsoft or can be provided by the customer. If provided by the customer it must follow  format of 64 character, and can contain only letters or 0-9 characters.  Use a website to generate a valid salt value.
 
- can run EDMuploadagent.exe from PS or Windows cmd window . tested on Windows Server 2016 or Windows 10 and dot net version 4.6.2

when defiuning the schema file the searchable fields must be either an out of box SIT or custom SIT, only 5 fields )column headings) can be searchable

1. From outbound access device from the cmd prompt run EdmUploadAgent.exe /Authorize -  
2. data store schema must have already been uploaded
3.  create hash first then do upload
4. EdmUploadAgent.exe /CreateHash /DataFile (where the data file is ) E:\emd\test\data\schema32_1000000,csv /HashLocation  (where to store it) E:\edm\tat\hash this makes the salt file and the hash file as output
5. next is upload EdmUploadAgent.exe /UploadHash /DataStoreName (found in the Schema file DataSore name="FOO" /HashFile (path to hash file locaztion and file name /HashLocation path to hash)  for example
1.EdmUploadAgent/exe /UploadHash /DataStoreName schema321 /HashFile E:\edm\test\hash\schema32_10000000.EdmHash /HashLocation E:\edm\test\hash  -this one  uses MSFT generated salt, so no need to provide

Salt is an optional parameter so if yo uwant to use a custom salt add /salt and the salt value if salt file not copied to the outbound machine 

OR copy both files hash and salt to the same directory and the commmand will get both


OR do it in single step hash, salt ulopad

!! once they download the updated upload agent they will always have SALT, there is no going back.


all in one step: EdmUploadAgent.exe /UploadData /DataStoreName schema321 /DataFile E:\edm\test\data\schema32_10000.csv /HashLocation E:\edm\test\hash

tshooting/check status cmd



Once it gets to completed the admin can start using it in the custom SIT

they have to get their own custom SALT

just copy SALT over in a secure fashion










1.
6.
7.
1.  


 -->

### <a name="part-2-hash-and-upload-the-sensitive-data"></a><span data-ttu-id="d9b32-267">Partie 2 : hacher et charger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-267">Part 2: Hash and upload the sensitive data</span></span>

<span data-ttu-id="d9b32-268">Au cours de cette phase, vous configurez un groupe de sécurité personnalisé et un compte d’utilisateur, et configurez l’outil de chargement de l’agent EDM.</span><span class="sxs-lookup"><span data-stu-id="d9b32-268">In this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="d9b32-269">Vous utilisez ensuite l’outil pour hacher les données sensibles avec valeur salt et les charger.</span><span class="sxs-lookup"><span data-stu-id="d9b32-269">Then, you use the tool to hash with salt value the sensitive data, and upload it.</span></span>

<span data-ttu-id="d9b32-270">L’opération de hachage et de chargement peut être effectuée à l’aide d’un ordinateur ou vous pouvez séparer ces deux étapes pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="d9b32-270">The hashing and uploading can be done using one computer or you can separate the hashing step from the upload step for greater security.</span></span>

<span data-ttu-id="d9b32-271">Si vous voulez hacher et charger à partir d’un ordinateur, vous devez le faire à partir d’un ordinateur qui peut se connecter directement à votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9b32-271">If you want to hash and upload from one computer, you need to do it from a computer that can directly connect to your Microsoft 365 tenant.</span></span> <span data-ttu-id="d9b32-272">Vos fichiers de données sensibles en texte clair doivent se trouver sur cet ordinateur pour le hachage.</span><span class="sxs-lookup"><span data-stu-id="d9b32-272">This requires that your clear text sensitive data files are on that computer for hashing.</span></span>

<span data-ttu-id="d9b32-273">Si vous ne souhaitez pas exposer votre fichier de données sensibles en texte clair, vous pouvez le hacher sur un ordinateur dans un emplacement sécurisé, puis copier le fichier de hachage et le fichier salt sur un ordinateur qui peut se connecter directement à votre client Microsoft 365 pour le chargement.</span><span class="sxs-lookup"><span data-stu-id="d9b32-273">If you do not want to expose your clear text sensitive data file, you can hash it on a computer in a secure location and then copy the hash file and the salt file to a computer that can directly connect to your Microsoft 365 tenant for upload.</span></span> <span data-ttu-id="d9b32-274">Dans ce scénario, vous aurez besoin d’EDMUploadAgent sur les deux ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="d9b32-274">In this scenario, you will need the EDMUploadAgent on both computers.</span></span> 

#### <a name="prerequisites"></a><span data-ttu-id="d9b32-275">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9b32-275">Prerequisites</span></span>

- <span data-ttu-id="d9b32-276">Un compte professionnel ou scolaire pour Microsoft 365 qui sera ajouté au groupe de sécurité **EDM\_DataUploaders**</span><span class="sxs-lookup"><span data-stu-id="d9b32-276">a work or school account for Microsoft 365  that will be added to the **EDM\_DataUploaders** security group</span></span>
- <span data-ttu-id="d9b32-277">Un ordinateur Windows 10 ou Windows Server 2016 avec .NET version 4.6.2 pour l’exécution d’EDMUploadAgent</span><span class="sxs-lookup"><span data-stu-id="d9b32-277">a Windows 10 or Windows Server 2016 machine with .NET version 4.6.2 for running the EDMUploadAgent</span></span>
- <span data-ttu-id="d9b32-278">Un répertoire sur votre ordinateur de téléchargement pour :</span><span class="sxs-lookup"><span data-stu-id="d9b32-278">a directory on your upload machine for the:</span></span>
    -  <span data-ttu-id="d9b32-279">EDMUploadAgent</span><span class="sxs-lookup"><span data-stu-id="d9b32-279">EDMUploadAgent</span></span>
    - <span data-ttu-id="d9b32-280">Votre fichier d’élément sensible au format CSV, **PatientRecords.csv** dans nos exemples</span><span class="sxs-lookup"><span data-stu-id="d9b32-280">your sensitive item file in csv format **PatientRecords.csv** in our examples</span></span>
    -  <span data-ttu-id="d9b32-281">Les fichiers de hachage et salt générés</span><span class="sxs-lookup"><span data-stu-id="d9b32-281">and the output hash and salt files</span></span>
    - <span data-ttu-id="d9b32-282">Le nom du magasin de données provenant du fichier **edm.xml**, ici `PatientRecords`</span><span class="sxs-lookup"><span data-stu-id="d9b32-282">the datastore name from the **edm.xml** file, for this example its `PatientRecords`</span></span>

#### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="d9b32-283">Configurer les groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d9b32-283">Set up the security group and user account</span></span>

1. <span data-ttu-id="d9b32-284">En tant qu’administrateur général, accédez au centre d’administration à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription) et [créez un groupe de sécurité](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) nommé **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-284">As a global administrator, go to the admin center using the appropriate [link for your subscription](#portal-links-for-your-subscription) and [create a security group](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) called **EDM\_DataUploaders**.</span></span>

2. <span data-ttu-id="d9b32-285">Ajoutez un ou plusieurs utilisateurs au groupe de sécurité**EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-285">Add one or more users to the **EDM\_DataUploaders** security group.</span></span> <span data-ttu-id="d9b32-286">(ces utilisateurs peuvent gérer la base de données d’informations sensibles).</span><span class="sxs-lookup"><span data-stu-id="d9b32-286">(These users will manage the database of sensitive information.)</span></span>

#### <a name="hash-and-upload-from-one-computer"></a><span data-ttu-id="d9b32-287">Hacher et charger à partir d’un même ordinateur</span><span class="sxs-lookup"><span data-stu-id="d9b32-287">Hash and upload from one computer</span></span>

<span data-ttu-id="d9b32-288">Cet ordinateur doit avoir accès directement à votre client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9b32-288">This computer must have direct access to your Microsoft 365 tenant.</span></span>

>[!NOTE]
> <span data-ttu-id="d9b32-289">Avant de commencer cette procédure, assurez-vous que vous êtes membre du groupe de sécurité **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-289">Before you begin this procedure, make sure that you are a member of the **EDM\_DataUploaders** security group.</span></span>

#### <a name="links-to-edm-upload-agent-by-subscription-type"></a><span data-ttu-id="d9b32-290">Liens vers l’agent de chargement EDM par type d’abonnement</span><span class="sxs-lookup"><span data-stu-id="d9b32-290">Links to EDM upload agent by subscription type</span></span>

- [<span data-ttu-id="d9b32-291">Commercial + GCC</span><span class="sxs-lookup"><span data-stu-id="d9b32-291">Commercial + GCC</span></span>](https://go.microsoft.com/fwlink/?linkid=2088639)
- [<span data-ttu-id="d9b32-292">GCC-High</span><span class="sxs-lookup"><span data-stu-id="d9b32-292">GCC-High</span></span>](https://go.microsoft.com/fwlink/?linkid=2137521)
- [<span data-ttu-id="d9b32-293">DOD</span><span class="sxs-lookup"><span data-stu-id="d9b32-293">DoD</span></span>](https://go.microsoft.com/fwlink/?linkid=2137807)

1. <span data-ttu-id="d9b32-294">Créez un répertoire de travail pour EDMUploadAgent.</span><span class="sxs-lookup"><span data-stu-id="d9b32-294">Create a working directory for the EDMUploadAgent.</span></span> <span data-ttu-id="d9b32-295">Par exemple, **C:\EDM\Data**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-295">For example, **C:\EDM\Data**.</span></span> <span data-ttu-id="d9b32-296">Placez le fichier **PatientRecords.csv** à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="d9b32-296">Place the **PatientRecords.csv** file there.</span></span>

2. <span data-ttu-id="d9b32-297">Téléchargez et installez l’[agent de chargement EDM](#links-to-edm-upload-agent-by-subscription-type) approprié pour votre abonnement dans le répertoire créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="d9b32-297">Download and install the appropriate [EDM Upload Agent](#links-to-edm-upload-agent-by-subscription-type) for your subscription into the directory you created in step 1.</span></span>

> [!NOTE]
> <span data-ttu-id="d9b32-298">La version d’EDMUploadAgent fournie à travers les liens ci-dessus a été mise à jour afin d’ajouter automatiquement une valeur salt aux données hachées.</span><span class="sxs-lookup"><span data-stu-id="d9b32-298">The EDMUploadAgent at the above links has been updated to automatically add a salt value to the hashed data.</span></span> <span data-ttu-id="d9b32-299">Vous pouvez également fournir votre propre valeur salt.</span><span class="sxs-lookup"><span data-stu-id="d9b32-299">Alternately, you can provide your own salt value.</span></span> <span data-ttu-id="d9b32-300">Une fois que vous avez utilisé cette version, vous ne pourrez pas utiliser la version précédente d’EDMUploadAgent.</span><span class="sxs-lookup"><span data-stu-id="d9b32-300">Once you have used this version, you will not be able to use the previous version of the EDMUploadAgent.</span></span>
>
> <span data-ttu-id="d9b32-301">Vous pouvez télécharger des données avec EDMUploadAgent vers n’importe quel magasin de données donné deux fois par jour uniquement.</span><span class="sxs-lookup"><span data-stu-id="d9b32-301">You can upload data with the EDMUploadAgent to any given data store only twice per day.</span></span>

> [!TIP]
> <span data-ttu-id="d9b32-302">Exécutez l'agent sans arguments pour obtenir une liste des paramètres de commande pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d9b32-302">To a get a list out of the supported command parameters, run the agent no arguments.</span></span> <span data-ttu-id="d9b32-303">Par exemple, « EdmUploadAgent. exe ».</span><span class="sxs-lookup"><span data-stu-id="d9b32-303">For example 'EdmUploadAgent.exe'.</span></span>

2. <span data-ttu-id="d9b32-304">Autorisez l’agent de chargement EDM, en ouvrant l’invite de commandes Windows (en tant qu’administrateur), puis en accédant au répertoire **C:\EDM\Data** pour exécuter la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9b32-304">Authorize the EDM Upload Agent, open  Command Prompt window (as an administrator), switch to the **C:\EDM\Data** directory and then run the following command:</span></span>

   `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="d9b32-305">Connectez-vous à l’aide de votre compte professionnel ou scolaire pour Microsoft 365 qui a été ajouté au groupe de sécurité EDM_DataUploaders.</span><span class="sxs-lookup"><span data-stu-id="d9b32-305">Sign in with your work or school account for Microsoft 365 that was added to the EDM_DataUploaders security group.</span></span> <span data-ttu-id="d9b32-306">Vos informations de client sont extraites du compte d’utilisateur pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="d9b32-306">Your tenant information is extracted from the user account to make the connection.</span></span>

4. <span data-ttu-id="d9b32-307">Pour hacher et charger les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="d9b32-307">To hash and upload the sensitive data, run the following command in Command Prompt window:</span></span>

`EdmUploadAgent.exe /UploadData /DataStoreName \<DataStoreName\> /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="d9b32-308">Exemple : **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\Edm\Hash\PatientRecords.csv /HashLocation C:\Edm\Hash**</span><span class="sxs-lookup"><span data-stu-id="d9b32-308">Example: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\Edm\Hash\PatientRecords.csv /HashLocation C:\Edm\Hash**</span></span>

<span data-ttu-id="d9b32-309">Cela a pour effet d’ajouter automatiquement une valeur salt générée de façon aléatoire au hachage afin de renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="d9b32-309">This will automatically add a randomly generated salt value to the hash for greater security.</span></span> <span data-ttu-id="d9b32-310">Si vous voulez utiliser votre propre valeur salt, vous pouvez également ajouter **/Salt <saltvalue>** à la commande.</span><span class="sxs-lookup"><span data-stu-id="d9b32-310">Optionally, if you want to use your own salt value, add the **/Salt <saltvalue>** to the command.</span></span> <span data-ttu-id="d9b32-311">Cette valeur doit comporter 64 caractères et ne peut contenir que les caractères allant de a à z et de 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="d9b32-311">This value must be 64 characters in length and can only contain the a-z characters and 0-9 characters.</span></span>

5. <span data-ttu-id="d9b32-312">Vérifiez l’état du chargement en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9b32-312">Check the upload status by running this command:</span></span>

`EdmUploadAgent.exe /GetSession /DataStoreName \<DataStoreName\>`

<span data-ttu-id="d9b32-313">Exemple : **EdmUploadAgent.exe /GetSession /DataStoreName PatientRecords**</span><span class="sxs-lookup"><span data-stu-id="d9b32-313">Example: **EdmUploadAgent.exe /GetSession /DataStoreName PatientRecords**</span></span>

<span data-ttu-id="d9b32-314">Vous verrez l’état **ProcessingInProgress**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-314">Look for the status to be in **ProcessingInProgress**.</span></span> <span data-ttu-id="d9b32-315">Vérifiez à quelques minutes d’intervalle jusqu’à ce que l’état devienne **Completed**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-315">Check again every few minutes until the status changes to **Completed**.</span></span> <span data-ttu-id="d9b32-316">Une fois que le chargement est à l’état Completed, vos données EDM sont prêtes à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="d9b32-316">Once the status is completed, your EDM data is ready for use.</span></span>

#### <a name="separate-hash-and-upload"></a><span data-ttu-id="d9b32-317">Séparer le hachage et le chargement</span><span class="sxs-lookup"><span data-stu-id="d9b32-317">Separate Hash and upload</span></span>

<span data-ttu-id="d9b32-318">Effectuez le hachage sur un ordinateur dans un environnement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="d9b32-318">Perform the hash on a computer in a secure environment.</span></span>

1. <span data-ttu-id="d9b32-319">À l’invite de commandes, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="d9b32-319">Run the following command in Command Prompt windows:</span></span>

`EdmUploadAgent.exe /CreateHash /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="d9b32-320">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d9b32-320">For example:</span></span>

> <span data-ttu-id="d9b32-321">**EdmUploadAgent.exe /CreateHash /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash**</span><span class="sxs-lookup"><span data-stu-id="d9b32-321">**EdmUploadAgent.exe /CreateHash /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash**</span></span>

<span data-ttu-id="d9b32-322">Cela génère un fichier haché et un fichier salt avec les extensions suivantes si vous n’avez pas spécifié l’option **/Salt <saltvalue>**  :</span><span class="sxs-lookup"><span data-stu-id="d9b32-322">This will output a hashed file and a salt file with these extensions if you didn't specify the **/Salt <saltvalue>** option:</span></span>
- <span data-ttu-id="d9b32-323">.EdmHash</span><span class="sxs-lookup"><span data-stu-id="d9b32-323">.EdmHash</span></span>
- <span data-ttu-id="d9b32-324">.EdmSalt</span><span class="sxs-lookup"><span data-stu-id="d9b32-324">.EdmSalt</span></span>

2. <span data-ttu-id="d9b32-325">Copiez ces fichiers de façon sécurisée sur l’ordinateur que vous allez utiliser pour charger sur votre client votre fichier CSV d’éléments sensibles (PatientRecords).</span><span class="sxs-lookup"><span data-stu-id="d9b32-325">Copy these files in a secure fashion to the computer you will use to upload your sensitive items csv file (PatientRecords) to your tenant.</span></span>

<span data-ttu-id="d9b32-326">Pour charger les données hachées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="d9b32-326">To upload the hashed data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

<span data-ttu-id="d9b32-327">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d9b32-327">For example:</span></span>

> <span data-ttu-id="d9b32-328">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="d9b32-328">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span></span>


<span data-ttu-id="d9b32-329">Pour vérifier que vos données sensibles ont été téléchargées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="d9b32-329">To verify that your sensitive data has been uploaded, run the following command in Command Prompt window:</span></span>


`EdmUploadAgent.exe /GetDataStore`

<span data-ttu-id="d9b32-330">La liste des magasins de données apparaît, ainsi que la date de la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d9b32-330">You'll see a list of data stores and when they were last updated.</span></span>

<span data-ttu-id="d9b32-331">Si vous voulez afficher toutes les données téléchargées vers un magasin particulier, exécutez la commande suivante dans une invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="d9b32-331">If you want to see all the data uploads to a particular store, run the following command in a Windows command prompt:</span></span>

`EdmUploadAgent.exe /GetSession /DataStoreName <DataStoreName>`

<span data-ttu-id="d9b32-332">Poursuivez la configuration de votre processus et planifiez l’[actualisation de votre base de données d'informations sensibles](#refreshing-your-sensitive-information-database).</span><span class="sxs-lookup"><span data-stu-id="d9b32-332">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="d9b32-333">À ce stade, vous êtes prêt à utiliser la classification basée sur EDM avec vos services de Cloud Computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9b32-333">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="d9b32-334">Par exemple, vous pouvez [configurer une stratégie DLP à l’aide d’une classification basée sur EDM](#to-create-a-dlp-policy-with-edm).</span><span class="sxs-lookup"><span data-stu-id="d9b32-334">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span>

#### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="d9b32-335">Actualisation de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-335">Refreshing your sensitive information database</span></span>

<span data-ttu-id="d9b32-336">Vous pouvez actualiser quotidiennement votre base de données d’informations sensibles, et l’outil de chargement EDM peut réindexer les données sensibles, puis recharger les données indexées.</span><span class="sxs-lookup"><span data-stu-id="d9b32-336">You can refresh your sensitive information database daily, and the EDM Upload Tool can reindex the sensitive data and then reupload the indexed data.</span></span>

1. <span data-ttu-id="d9b32-337">Déterminez vos processus et leur fréquence (quotidien ou hebdomadaire) pour actualiser la base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="d9b32-337">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="d9b32-338">Exportez de nouveau les données vers une application, telle que Microsoft Excel, et enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="d9b32-338">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="d9b32-339">Conservez le même nom de fichier et l’emplacement que vous avez utilisé lorsque vous avez suivi les étapes décrites dans[Hachage et téléchargement des données sensibles](#part-2-hash-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="d9b32-339">Keep the same file name and location you used when you followed the steps described in [Hash and upload the sensitive data](#part-2-hash-and-upload-the-sensitive-data).</span></span>

      > [!NOTE]
      > <span data-ttu-id="d9b32-340">S’il n’y a pas de modifications apportées à la structure (noms de champs) du fichier .csv, vous n’avez pas besoin d’apporter des modifications à votre fichier de schéma de base de données lorsque vous actualisez les données.</span><span class="sxs-lookup"><span data-stu-id="d9b32-340">If there are no changes to the structure (field names) of the .csv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="d9b32-341">Si vous devez apporter des modifications, assurez-vous de modifier le schéma de base de données et votre package de règles en conséquence.</span><span class="sxs-lookup"><span data-stu-id="d9b32-341">But if you must make changes, make sure to edit the database schema and your rule package accordingly.</span></span>

3. <span data-ttu-id="d9b32-342">Utilisez [le planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) pour automatiser les étapes 2 et 3 dans la procédure[hacher et télécharger les données sensibles](#part-2-hash-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="d9b32-342">Use [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Hash and upload the sensitive data](#part-2-hash-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="d9b32-343">Vous pouvez planifier des tâches à l’aide de plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="d9b32-343">You can schedule tasks using several methods:</span></span>

      | <span data-ttu-id="d9b32-344">Méthode</span><span class="sxs-lookup"><span data-stu-id="d9b32-344">Method</span></span>             | <span data-ttu-id="d9b32-345">Procédure</span><span class="sxs-lookup"><span data-stu-id="d9b32-345">What to do</span></span> |
      | ---------------------- | ---------------- |
      | <span data-ttu-id="d9b32-346">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d9b32-346">Windows PowerShell</span></span>     | <span data-ttu-id="d9b32-347">Consultez la documentation[ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) et l’[exemple de script PowerShell](#example-powershell-script-for-task-scheduler) dans cet article</span><span class="sxs-lookup"><span data-stu-id="d9b32-347">See the [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span> |
      | <span data-ttu-id="d9b32-348">API planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d9b32-348">Task Scheduler API</span></span>     | <span data-ttu-id="d9b32-349">Consultez la documentation relative au [planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler)</span><span class="sxs-lookup"><span data-stu-id="d9b32-349">See the [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span>                                                                                                                                                                                                                                                                                |
      | <span data-ttu-id="d9b32-350">Interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="d9b32-350">Windows user interface</span></span> | <span data-ttu-id="d9b32-351">Dans Windows, cliquez sur **Démarrer**, puis tapez Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d9b32-351">In Windows, click **Start**, and type Task Scheduler.</span></span> <span data-ttu-id="d9b32-352">Dans la liste des résultats, cliquez avec le bouton droit sur**planificateur de tâches**, puis sélectionnez**exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-352">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="d9b32-353">Exemple de script PowerShell pour le planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="d9b32-353">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="d9b32-354">Cette section inclut un exemple de script PowerShell que vous pouvez utiliser pour planifier vos tâches de hachage de données et de téléchargement des données hachées :</span><span class="sxs-lookup"><span data-stu-id="d9b32-354">This section includes an example PowerShell script you can use to schedule your tasks for hashing data and uploading the hashed data:</span></span>

##### <a name="to-schedule-hashing-and-upload-in-a-combined-step"></a><span data-ttu-id="d9b32-355">Pour planifier un hachage et effectuer un téléchargement dans une étape seule combinée</span><span class="sxs-lookup"><span data-stu-id="d9b32-355">To schedule hashing and upload in a combined step</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$uploadDataArgs = '/UploadData /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation' + $hashLocation
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

#### <a name="to-schedule-hashing-and-upload-as-separate-steps"></a><span data-ttu-id="d9b32-356">Pour planifier un hachage et effectuer un téléchargement en deux étapes distinctes</span><span class="sxs-lookup"><span data-stu-id="d9b32-356">To schedule hashing and upload as separate steps</span></span>

```powershell
param(\[string\]$dataStoreName,\[string\]$fileLocation)
\# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\\$env:USERNAME"
$edminstallpath = 'C:\\Program Files\\Microsoft\\EdmUploadAgent\\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
\# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\\$dataStoreName$csvext"
$hashFile = "$fileLocation\\$dataStoreName$edmext"
\# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash' + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
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

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="d9b32-357">Partie 3 : utiliser la classification EDM avec vos services de cloud computing Microsoft</span><span class="sxs-lookup"><span data-stu-id="d9b32-357">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="d9b32-358">Ces emplacements prennent en charge les types d’informations sensibles EDM :</span><span class="sxs-lookup"><span data-stu-id="d9b32-358">These locations are support EDM sensitive information types:</span></span>

- <span data-ttu-id="d9b32-359">DLP pour Exchange Online (e-mail)</span><span class="sxs-lookup"><span data-stu-id="d9b32-359">DLP for Exchange Online (email)</span></span>
- <span data-ttu-id="d9b32-360">OneDrive Entreprise (fichiers)</span><span class="sxs-lookup"><span data-stu-id="d9b32-360">OneDrive for Business (files)</span></span>
- <span data-ttu-id="d9b32-361">Microsoft Teams (conversations)</span><span class="sxs-lookup"><span data-stu-id="d9b32-361">Microsoft Teams (conversations)</span></span>
- <span data-ttu-id="d9b32-362">DLP pour SharePoint (fichiers)</span><span class="sxs-lookup"><span data-stu-id="d9b32-362">DLP for SharePoint (files)</span></span>
- <span data-ttu-id="d9b32-363">Stratégies DLP de la sécurité de l’application Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="d9b32-363">Microsoft Cloud App Security DLP policies</span></span>

<span data-ttu-id="d9b32-364">Les types d’informations sensibles EDM pour les scénarios suivants sont en cours de développement, mais pas encore disponibles :</span><span class="sxs-lookup"><span data-stu-id="d9b32-364">EDM sensitive information types for following scenarios are currently in development, but not yet available:</span></span>

- <span data-ttu-id="d9b32-365">Classification automatique des étiquettes de confidentialité et étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="d9b32-365">Auto-classification of sensitivity labels and retention labels</span></span>

#### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="d9b32-366">Pour créer une stratégie DLP avec EDM</span><span class="sxs-lookup"><span data-stu-id="d9b32-366">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="d9b32-367">Accédez au Centre de conformité et de sécurité à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription).</span><span class="sxs-lookup"><span data-stu-id="d9b32-367">Go to the Security & Compliance Center using the appropriate [link for your subscription](#portal-links-for-your-subscription).</span></span>

2. <span data-ttu-id="d9b32-368">Sélectionnez stratégie de **Protection contre la perte de données** \> \*\* \*\*.</span><span class="sxs-lookup"><span data-stu-id="d9b32-368">Choose **Data loss prevention** \> **Policy**.</span></span>

3. <span data-ttu-id="d9b32-369">Sélectionnez **Créer une stratégie** \> **Personnaliser** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-369">Choose **Create a policy** \> **Custom** \> **Next**.</span></span>

4. <span data-ttu-id="d9b32-370">Sous l'onglet**Nommez votre stratégie**, spécifiez un nom et une description, puis sélectionnez**suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-370">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="d9b32-371">Dans le volet **Choisir des emplacements**, cliquez sur **Me laisser choisir des emplacements spécifiques**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-371">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span>

6. <span data-ttu-id="d9b32-372">Dans la colonne **État**, sélectionnez **Courrier Exchange, Comptes OneDrive, Messages de conversation et de canal de Teams**, puis **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-372">In the **Status** column, select **Exchange email, OneDrive accounts, Teams chat and channel message** , and then choose **Next**.</span></span>

7. <span data-ttu-id="d9b32-373">Sous l'onglet**paramètres de stratégie**, sélectionnez**utiliser les paramètres avancés**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-373">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span>

8. <span data-ttu-id="d9b32-374">Sélectionnez **+ Nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-374">Choose **+ New rule**.</span></span>

9. <span data-ttu-id="d9b32-375">Dans la section**Nom**, spécifiez un nom et une description pour la règle.</span><span class="sxs-lookup"><span data-stu-id="d9b32-375">In the **Name** section, specify a name and description for the rule.</span></span>

10. <span data-ttu-id="d9b32-376">Dans la section**conditions**, dans la liste **+ ajouter une condition**, sélectionnez **le contenu contient un type de contenu sensible**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-376">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span>

      ![Le contenu contient des types d’informations sensibles](../media/edm-dlp-newrule-conditions.png)

11. <span data-ttu-id="d9b32-378">Recherchez le type d’informations sensibles que vous avez créé lorsque vous avez configuré votre package de règles, puis sélectionnez **+ ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-378">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span>  
    <span data-ttu-id="d9b32-379">Sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-379">Then choose **Done**.</span></span>

12. <span data-ttu-id="d9b32-380">Terminez de sélectionner les options de votre règle, telles que**notifications d’utilisateur**,**remplacements d’utilisateur**, **rapports d’incident**, puis sélectionnez\*\* Enregistrer\*\*.</span><span class="sxs-lookup"><span data-stu-id="d9b32-380">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="d9b32-381">Sous l'onglet **paramètres de stratégie**, passez en revue vos règles, puis sélectionnez**suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-381">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="d9b32-382">Indiquez si vous voulez activer la stratégie immédiatement, tester celle-ci ou la maintenir désactivée.</span><span class="sxs-lookup"><span data-stu-id="d9b32-382">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="d9b32-383">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-383">Then choose **Next**.</span></span>

15. <span data-ttu-id="d9b32-384">Sous l'onglet **Vérifier vos paramètres**, passez en revue votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="d9b32-384">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="d9b32-385">Apportez les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d9b32-385">Make any needed changes.</span></span> <span data-ttu-id="d9b32-386">Lorsque vous avez terminé, sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="d9b32-386">When you're ready, choose **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="d9b32-387">Laissez environ une heure pour que votre nouvelle stratégie DLP fonctionne de la même manière dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="d9b32-387">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d9b32-388">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d9b32-388">Related articles</span></span>

- [<span data-ttu-id="d9b32-389">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="d9b32-389">Sensitive information type-entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="d9b32-390">Types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="d9b32-390">Custom sensitive information types</span></span>](custom-sensitive-info-types.md)
- [<span data-ttu-id="d9b32-391">Vue d’ensemble des stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="d9b32-391">Overview of DLP policies</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="d9b32-392">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d9b32-392">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)
- [<span data-ttu-id="d9b32-393">New-DlpEdmSchema</span><span class="sxs-lookup"><span data-stu-id="d9b32-393">New-DlpEdmSchema</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-dlpedmschema)

