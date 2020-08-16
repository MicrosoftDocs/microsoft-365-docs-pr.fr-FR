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
ms.openlocfilehash: 699cea6aec6f11462aed0c08db98ca4620df519a
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46686558"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification"></a><span data-ttu-id="699d5-103">Créez des types d’informations sensibles personnalisés à l’aide d’une classification Exact Data Match.</span><span class="sxs-lookup"><span data-stu-id="699d5-103">Create custom sensitive information types with Exact Data Match based classification</span></span>

<span data-ttu-id="699d5-104">Les [types d’informations sensibles personnalisés](custom-sensitive-info-types.md)  vous aident à empêcher le partage involontaire ou inapproprié d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="699d5-104">[Custom sensitive information types](custom-sensitive-info-types.md) are used to help prevent inadvertent or inappropriate sharing of sensitive information.</span></span> <span data-ttu-id="699d5-105">En tant qu’administrateur, vous pouvez utiliser le Centre de sécurité et de conformité ou PowerShell pour définir un type d’informations sensibles personnalisé basé sur des modèles, des preuves (mots clés tels que *employé*, *badge*, *ID*, etc.), proximité des caractères (comment les preuves sont proches des caractères dans un modèle particulier) et des niveaux de confiance.</span><span class="sxs-lookup"><span data-stu-id="699d5-105">As an administrator, you can use the Security & Compliance Center or PowerShell to define a custom sensitive information type based on patterns, evidence (keywords such as *employee*, *badge*, *ID*, and so on), character proximity (how close evidence is to characters in a particular pattern), and confidence levels.</span></span> <span data-ttu-id="699d5-106">De tels types d’informations sensibles personnalisés répondent aux besoins métier de nombreuses organisations.</span><span class="sxs-lookup"><span data-stu-id="699d5-106">Such custom sensitive information types meet business needs for many organizations.</span></span>

<span data-ttu-id="699d5-107">Mais que se passe-t-il si vous voulez utiliser un type d’informations sensibles personnalisé qui utilise des valeurs de données exactes au lieu d’établir une concordance avec des modèles génériques ?</span><span class="sxs-lookup"><span data-stu-id="699d5-107">But what if you wanted a custom sensitive information type that uses exact data values, instead of matching only with generic patterns?</span></span> <span data-ttu-id="699d5-108">Une classification Exact Data Match (EDM) vous permet de créer un type d’informations sensibles personnalisé conçu pour :</span><span class="sxs-lookup"><span data-stu-id="699d5-108">With Exact Data Match (EDM)-based classification, you can create a custom sensitive information type that is designed to:</span></span>

- <span data-ttu-id="699d5-109">être dynamique et actualisable ;</span><span class="sxs-lookup"><span data-stu-id="699d5-109">be dynamic and refreshable;</span></span>
- <span data-ttu-id="699d5-110">être plus évolutif ;</span><span class="sxs-lookup"><span data-stu-id="699d5-110">be more scalable;</span></span>
- <span data-ttu-id="699d5-111">entraîner moins de faux positifs ;</span><span class="sxs-lookup"><span data-stu-id="699d5-111">result in fewer false-positives;</span></span>
- <span data-ttu-id="699d5-112">utiliser des données sensibles structurées ;</span><span class="sxs-lookup"><span data-stu-id="699d5-112">work with structured sensitive data;</span></span>
- <span data-ttu-id="699d5-113">gérer les informations sensibles de façon plus sécurisée, et</span><span class="sxs-lookup"><span data-stu-id="699d5-113">handle sensitive information more securely; and</span></span>
- <span data-ttu-id="699d5-114">être utilisé avec plusieurs services de cloud computing de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="699d5-114">be used with several Microsoft cloud services.</span></span>

![Classification EDM](../media/EDMClassification.png)

<span data-ttu-id="699d5-116">La classification EDM vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="699d5-116">EDM-based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="699d5-117">La base de données peut être actualisée quotidiennement ou hebdomadairement, et peut contenir jusqu’à 100 millions de lignes de données.</span><span class="sxs-lookup"><span data-stu-id="699d5-117">The database can be refreshed daily or weekly, and it can contain up to 100 million rows of data.</span></span> <span data-ttu-id="699d5-118">À mesure que des employés, patients ou clients vont et viennent, et que les enregistrements changent, vos types d’informations sensibles personnalisés restent à jour et valides.</span><span class="sxs-lookup"><span data-stu-id="699d5-118">So as employees, patients, or clients come and go, and records change, your custom sensitive information types remain current and applicable.</span></span> <span data-ttu-id="699d5-119">Vous pouvez également utiliser une classification EDM avec des stratégies, par exemple, de  [protection contre la perte de données](data-loss-prevention-policies.md)  (DLP) ou les stratégies de fichier de  [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="699d5-119">And, you can use EDM-based classification with policies, such as [data loss prevention policies](data-loss-prevention-policies.md) (DLP) or [Microsoft Cloud App Security file policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="699d5-120">Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :</span><span class="sxs-lookup"><span data-stu-id="699d5-120">Microsoft 365 Information Protection now  supports in preview double byte character set languages for:</span></span>
> - <span data-ttu-id="699d5-121">Chinois (simplifié)</span><span class="sxs-lookup"><span data-stu-id="699d5-121">Chinese (simplified)</span></span>
> - <span data-ttu-id="699d5-122">Chinois (traditionnel)</span><span class="sxs-lookup"><span data-stu-id="699d5-122">Chinese (traditional)</span></span>
> - <span data-ttu-id="699d5-123">Korean</span><span class="sxs-lookup"><span data-stu-id="699d5-123">Korean</span></span>
> - <span data-ttu-id="699d5-124">Japanese</span><span class="sxs-lookup"><span data-stu-id="699d5-124">Japanese</span></span>
> 
><span data-ttu-id="699d5-125">Cette préversion est uniquement disponible dans le cloud commercial et le déploiement est limité aux pays suivants :</span><span class="sxs-lookup"><span data-stu-id="699d5-125">This preview is only in the commercial cloud and the rollout is limited to:</span></span>
> - <span data-ttu-id="699d5-126">Japon</span><span class="sxs-lookup"><span data-stu-id="699d5-126">Japan</span></span>
> - <span data-ttu-id="699d5-127">Corée</span><span class="sxs-lookup"><span data-stu-id="699d5-127">Korea</span></span>
> - <span data-ttu-id="699d5-128">Chine</span><span class="sxs-lookup"><span data-stu-id="699d5-128">China</span></span>
> - <span data-ttu-id="699d5-129">Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="699d5-129">Hong Kong</span></span>
> - <span data-ttu-id="699d5-130">Macao (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="699d5-130">Macau</span></span>
> - <span data-ttu-id="699d5-131">Taïwan</span><span class="sxs-lookup"><span data-stu-id="699d5-131">Taiwan</span></span>
>
><span data-ttu-id="699d5-132">Cette prise en charge est disponible pour les types d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="699d5-132">This support is available for sensitive information types.</span></span> <span data-ttu-id="699d5-133">Si vous souhaitez en savoir plus, consultez l’article [Prise en charge de la protection des informations pour les jeux de caractères à double octets (préversion)](mip-dbcs-relnotes.md).</span><span class="sxs-lookup"><span data-stu-id="699d5-133">See, [Information protection support for double byte character sets release notes (preview)](mip-dbcs-relnotes.md) for more information.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="699d5-134">Licences et autorisations requises</span><span class="sxs-lookup"><span data-stu-id="699d5-134">Required licenses and permissions</span></span>

<span data-ttu-id="699d5-135">Pour effectuer les tâches décrites dans cet article, vous devez être un administrateur général, un administrateur de conformité ou un administrateur Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="699d5-135">You must be a global admin, compliance administrator, or Exchange Online administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="699d5-136">Pour en avoir plus sur les autorisations DLP, voir  [Autorisations](data-loss-prevention-policies.md#permissions).</span><span class="sxs-lookup"><span data-stu-id="699d5-136">To learn more about DLP permissions, see [Permissions](data-loss-prevention-policies.md#permissions).</span></span>

<span data-ttu-id="699d5-137">La classification EDM est incluse dans ces abonnements</span><span class="sxs-lookup"><span data-stu-id="699d5-137">EDM-based classification is included in these subscriptions</span></span>

- <span data-ttu-id="699d5-138">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="699d5-138">Office 365 E5</span></span>
- <span data-ttu-id="699d5-139">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="699d5-139">Microsoft 365 E5</span></span>
- <span data-ttu-id="699d5-140">Microsoft 365 E5 Conformité</span><span class="sxs-lookup"><span data-stu-id="699d5-140">Microsoft 365 E5 Compliance</span></span>
- <span data-ttu-id="699d5-141">Microsoft E5/A5 Information Protection et gouvernance</span><span class="sxs-lookup"><span data-stu-id="699d5-141">Microsoft E5/A5 Information Protection and Governance</span></span>

## <a name="portal-links-for-your-subscription"></a><span data-ttu-id="699d5-142">Liens vers les portails de votre abonnement</span><span class="sxs-lookup"><span data-stu-id="699d5-142">Portal links for your subscription</span></span>


|<span data-ttu-id="699d5-143">Portail</span><span class="sxs-lookup"><span data-stu-id="699d5-143">Portal</span></span>  |<span data-ttu-id="699d5-144">World Wide/GCC</span><span class="sxs-lookup"><span data-stu-id="699d5-144">World Wide/GCC</span></span>  |<span data-ttu-id="699d5-145">GCC-High</span><span class="sxs-lookup"><span data-stu-id="699d5-145">GCC-High</span></span>  |<span data-ttu-id="699d5-146">DOD</span><span class="sxs-lookup"><span data-stu-id="699d5-146">DOD</span></span>  |
|---------|---------|---------|---------|
|<span data-ttu-id="699d5-147">Office SCC</span><span class="sxs-lookup"><span data-stu-id="699d5-147">Office SCC</span></span>     |  <span data-ttu-id="699d5-148">protection.office.com</span><span class="sxs-lookup"><span data-stu-id="699d5-148">protection.office.com</span></span>       |<span data-ttu-id="699d5-149">scc.office365.us</span><span class="sxs-lookup"><span data-stu-id="699d5-149">scc.office365.us</span></span>         |<span data-ttu-id="699d5-150">scc.protection.apps.mil</span><span class="sxs-lookup"><span data-stu-id="699d5-150">scc.protection.apps.mil</span></span> |
|<span data-ttu-id="699d5-151">Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="699d5-151">Microsoft 365 Security center</span></span>     |<span data-ttu-id="699d5-152">security.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="699d5-152">security.microsoft.com</span></span>         |<span data-ttu-id="699d5-153">security.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="699d5-153">security.microsoft.us</span></span>         |<span data-ttu-id="699d5-154">security.apps.mil</span><span class="sxs-lookup"><span data-stu-id="699d5-154">security.apps.mil</span></span>|
|<span data-ttu-id="699d5-155">Centre de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="699d5-155">Microsoft 365 Compliance center</span></span>     |<span data-ttu-id="699d5-156">compliance.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="699d5-156">compliance.microsoft.com</span></span>         |<span data-ttu-id="699d5-157">compliance.microsoft.us</span><span class="sxs-lookup"><span data-stu-id="699d5-157">compliance.microsoft.us</span></span>         |<span data-ttu-id="699d5-158">compliance.apps.mil</span><span class="sxs-lookup"><span data-stu-id="699d5-158">compliance.apps.mil</span></span>|


## <a name="the-work-flow-at-a-glance"></a><span data-ttu-id="699d5-159">Flux de travail en un clin d’œil</span><span class="sxs-lookup"><span data-stu-id="699d5-159">The work flow at a glance</span></span>

|<span data-ttu-id="699d5-160">Phase</span><span class="sxs-lookup"><span data-stu-id="699d5-160">Phase</span></span>  |<span data-ttu-id="699d5-161">De quoi ai-je besoin ?</span><span class="sxs-lookup"><span data-stu-id="699d5-161">What's needed</span></span>  |
|---------|---------|
|[<span data-ttu-id="699d5-162">Partie 1: configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-162">Part 1: Set up EDM-based classification</span></span>](#part-1-set-up-edm-based-classification)<br/><br/><span data-ttu-id="699d5-163">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="699d5-163">(As needed)</span></span><br/><span data-ttu-id="699d5-164">- [Modifier le schéma de base de données](#editing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="699d5-164">- [Edit the database schema](#editing-the-schema-for-edm-based-classification)</span></span> <br/><span data-ttu-id="699d5-165">- [Supprimer le schéma](#removing-the-schema-for-edm-based-classification)</span><span class="sxs-lookup"><span data-stu-id="699d5-165">- [Remove the schema](#removing-the-schema-for-edm-based-classification)</span></span> |<span data-ttu-id="699d5-166">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-166">- Read access to the sensitive data</span></span><br/><span data-ttu-id="699d5-167">-Schéma de base de données au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="699d5-167">- Database schema in XML format (example provided)</span></span><br/><span data-ttu-id="699d5-168">-Package de règles au format XML (fourni en exemple)</span><span class="sxs-lookup"><span data-stu-id="699d5-168">- Rule package in XML format (example provided)</span></span><br/><span data-ttu-id="699d5-169">-Autorisations d’administrateur sur le centre de sécurité & conformité (à l’aide de PowerShell)</span><span class="sxs-lookup"><span data-stu-id="699d5-169">- Admin permissions to the Security & Compliance Center (using PowerShell)</span></span> |
|[<span data-ttu-id="699d5-170">Partie 2 : hacher et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-170">Part 2: Hash and upload the sensitive data</span></span>](#part-2-hash-and-upload-the-sensitive-data)<br/><br/><span data-ttu-id="699d5-171">(selon vos besoins)</span><span class="sxs-lookup"><span data-stu-id="699d5-171">(As needed)</span></span><br/>[<span data-ttu-id="699d5-172">Actualiser les données</span><span class="sxs-lookup"><span data-stu-id="699d5-172">Refresh the data</span></span>](#refreshing-your-sensitive-information-database) |<span data-ttu-id="699d5-173">-Groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="699d5-173">- Custom security group and user account</span></span><br/><span data-ttu-id="699d5-174">-Accès administrateur local à l’ordinateur à l’aide de l’agent de téléchargement EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-174">- Local admin access to machine with EDM Upload Agent</span></span><br/><span data-ttu-id="699d5-175">-Accès en lecture aux données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-175">- Read access to the sensitive data</span></span><br/><span data-ttu-id="699d5-176">-Processus et planification pour l’actualisation des données</span><span class="sxs-lookup"><span data-stu-id="699d5-176">- Process and schedule for refreshing the data</span></span>|
|[<span data-ttu-id="699d5-177">Partie 3: utiliser la classification EDM avec vos services Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="699d5-177">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |<span data-ttu-id="699d5-178">- Abonnement Microsoft 365 avec DLP</span><span class="sxs-lookup"><span data-stu-id="699d5-178">- Microsoft 365 subscription with DLP</span></span><br/><span data-ttu-id="699d5-179">- Fonctionnalité de classification EDM activée</span><span class="sxs-lookup"><span data-stu-id="699d5-179">- EDM-based classification feature enabled</span></span> |

### <a name="part-1-set-up-edm-based-classification"></a><span data-ttu-id="699d5-180">Partie 1 : configurer la classification EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-180">Part 1: Set up EDM-based classification</span></span>

<span data-ttu-id="699d5-181">La préparation et la configuration de la classification EDM impliquent d’enregistrer des données sensibles au format. csv, de définir un schéma pour votre base de données d’informations sensibles, de créer un package de règles, puis de télécharger le schéma et le package de règles.</span><span class="sxs-lookup"><span data-stu-id="699d5-181">Setting up and configuring EDM-based classification involves saving sensitive data in .csv format, defining a schema for your database of sensitive information, creating a rule package, and then uploading the schema and rule package.</span></span>

#### <a name="define-the-schema-for-your-database-of-sensitive-information"></a><span data-ttu-id="699d5-182">Définir le schéma de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-182">Define the schema for your database of sensitive information</span></span>

1. <span data-ttu-id="699d5-183">Identifiez les informations sensibles que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="699d5-183">Identify the sensitive information you want to use.</span></span> <span data-ttu-id="699d5-184">Exportez les données vers une application, telle que Microsoft Excel, puis enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="699d5-184">Export the data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="699d5-185">Le fichier de données peut inclure au maximum :</span><span class="sxs-lookup"><span data-stu-id="699d5-185">The data file can include a maximum of:</span></span>
      - <span data-ttu-id="699d5-186">100 millions de lignes de données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-186">Up to 100 million rows of sensitive data</span></span>
      - <span data-ttu-id="699d5-187">32 colonnes (champs) par source de données</span><span class="sxs-lookup"><span data-stu-id="699d5-187">Up to 32 columns (fields) per data source</span></span>
      - <span data-ttu-id="699d5-188">5 colonnes (champs) marquées comme pouvant faire l’objet d’une recherche</span><span class="sxs-lookup"><span data-stu-id="699d5-188">Up to 5 columns (fields) marked as searchable</span></span>

2. <span data-ttu-id="699d5-189">Structurez les données sensibles dans le fichier .csv de telle sorte que la première ligne contienne les noms des champs utilisés pour la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-189">Structure the sensitive data in the .csv file such that the first row includes the names of the fields used for EDM-based classification.</span></span> <span data-ttu-id="699d5-190">Votre fichier .csv contient peut-être des noms de champs, tels que « ssn », « birthdate », « firstname », « lastname », etc.</span><span class="sxs-lookup"><span data-stu-id="699d5-190">In your .csv file, you might have field names, such as "ssn", "birthdate", "firstname", "lastname", and so on.</span></span> <span data-ttu-id="699d5-191">Veuillez noter que les en-têtes de colonne ne peuvent pas contenir d’espaces ou de traits de soulignement dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="699d5-191">Please note that column headers can't include spaces or underscores in their names.</span></span> <span data-ttu-id="699d5-192">Par exemple, le fichier .csv est appelé  *PatientRecords.csv* et ses colonnes incluent  *PatientID*,  *MRN*,  *NomdeFamille*,  *Prénom*,  *SSN*, etc.</span><span class="sxs-lookup"><span data-stu-id="699d5-192">As an example, our .csv file is called *PatientRecords.csv*, and its columns include *PatientID*, *MRN*, *LastName*, *FirstName*, *SSN*, and more.</span></span>

3. <span data-ttu-id="699d5-193">Définissez le schéma pour la base de données d’informations sensibles dans un fichier XML (comme dans l’exemple ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="699d5-193">Define the schema for the database of sensitive information in XML format (similar to our example below).</span></span> <span data-ttu-id="699d5-194">Nommez ce fichier de schéma **edm.xml** et configurez-le de telle sorte que pour chaque colonne de la base de données, une ligne utilise la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="699d5-194">Name this schema file **edm.xml**, and configure it such that for each column in the database, there is a line that uses the syntax:</span></span> 

      <span data-ttu-id="699d5-195">`\<Field name="" searchable=""/\>`.</span><span class="sxs-lookup"><span data-stu-id="699d5-195">`\<Field name="" searchable=""/\>`.</span></span>

      - <span data-ttu-id="699d5-196">Utilisez des noms de colonne pour les valeurs  *Nom de champ* .</span><span class="sxs-lookup"><span data-stu-id="699d5-196">Use column names for *Field name* values.</span></span>
      - <span data-ttu-id="699d5-197">Utilisez  *searchable="true"*  pour jusqu’à 5 champs dont vous voulez qu’il puissent faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="699d5-197">Use *searchable="true"* for the fields that you want to be searchable up to a maximum of 5 fields.</span></span> <span data-ttu-id="699d5-198">Vous devez spécifier au moins un champ comme pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="699d5-198">You must designate a minimum of one field as searchable.</span></span>

      <span data-ttu-id="699d5-199">Par exemple, le fichier XML suivant définit le schéma d’une base de données de dossiers de patients, avec cinq champs pouvant faire l’objet d’une recherche :  *PatientID*,  *MRN*,  *SSN*,  *Phone* et  *DOB*.</span><span class="sxs-lookup"><span data-stu-id="699d5-199">As an example, the following XML file defines the schema for a patient records database, with five fields specified as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span>

      <span data-ttu-id="699d5-200">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="699d5-200">(You can copy, modify, and use our example.)</span></span>

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

4. <span data-ttu-id="699d5-201">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="699d5-201">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

5. <span data-ttu-id="699d5-202">Pour charger le schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="699d5-202">To upload the database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="699d5-203">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="699d5-203">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="699d5-204">Confirmer</span><span class="sxs-lookup"><span data-stu-id="699d5-204">Confirm</span></span>
      >
      > <span data-ttu-id="699d5-205">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="699d5-205">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="699d5-206">Un nouveau schéma EDM pour le magasin de données « patientrecords » va être importé.</span><span class="sxs-lookup"><span data-stu-id="699d5-206">New EDM Schema for the data store 'patientrecords' will be imported.</span></span>
      >
      > <span data-ttu-id="699d5-207">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="699d5-207">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

> [!TIP]
> <span data-ttu-id="699d5-208">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 5, utilisez plutôt la cmdlet New-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="699d5-208">If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: New-DlpEdmSchema -FileData $edmSchemaXml</span></span>

> [!NOTE]
> <span data-ttu-id="699d5-209">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="699d5-209">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="699d5-210">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="699d5-210">The update must complete before you execute steps that use the additions.</span></span>

<span data-ttu-id="699d5-211">À présent que le schéma de votre base de données d’informations sensibles est défini, l’étape suivante consiste à configurer un package de règles.</span><span class="sxs-lookup"><span data-stu-id="699d5-211">Now that the schema for your database of sensitive information is defined, the next step is to set up a rule package.</span></span> <span data-ttu-id="699d5-212">Passez à la section  [Configurer un package de règles](#set-up-a-rule-package).</span><span class="sxs-lookup"><span data-stu-id="699d5-212">Proceed to the section [Set up a rule package](#set-up-a-rule-package).</span></span>

#### <a name="editing-the-schema-for-edm-based-classification"></a><span data-ttu-id="699d5-213">Modification du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-213">Editing the schema for EDM-based classification</span></span>

<span data-ttu-id="699d5-214">Si vous souhaitez modifier votre fichier **edm.xml**, par exemple pour changer les champs utilisés pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="699d5-214">If you want to make changes to your **edm.xml** file, such as changing which fields are used for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="699d5-215">Modifiez votre fichier **edm.xml** (présenté dans la section  [Définir le schéma](#define-the-schema-for-your-database-of-sensitive-information)  de cet article).</span><span class="sxs-lookup"><span data-stu-id="699d5-215">Edit your **edm.xml** file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).</span></span>

2. <span data-ttu-id="699d5-216">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="699d5-216">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

3. <span data-ttu-id="699d5-217">Pour mettre à jour votre schéma de base de données, exécutez les cmdlets suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="699d5-217">To update your database schema, run the following cmdlets, one at a time:</span></span>

      ```powershell
      $edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0
      Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true
      ```

      <span data-ttu-id="699d5-218">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="699d5-218">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="699d5-219">Confirmer</span><span class="sxs-lookup"><span data-stu-id="699d5-219">Confirm</span></span>
      >
      > <span data-ttu-id="699d5-220">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="699d5-220">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="699d5-221">Le schéma EDM pour le magasin de données « patientrecords » va être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="699d5-221">EDM Schema for the data store 'patientrecords' will be updated.</span></span>
      >
      > <span data-ttu-id="699d5-222">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="699d5-222">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      > <span data-ttu-id="699d5-223">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 3, utilisez plutôt la cmdlet Set-DlpEdmSchema -FileData $edmSchemaXml</span><span class="sxs-lookup"><span data-stu-id="699d5-223">If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: Set-DlpEdmSchema -FileData $edmSchemaXml</span></span>

      > [!NOTE]
      > <span data-ttu-id="699d5-224">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="699d5-224">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="699d5-225">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="699d5-225">The update must complete before you execute steps that use the additions.</span></span>

## <a name="removing-the-schema-for-edm-based-classification"></a><span data-ttu-id="699d5-226">Suppression du schéma pour la classification EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-226">Removing the schema for EDM-based classification</span></span>

<span data-ttu-id="699d5-227">(Le cas échéant) Si vous voulez supprimer le schéma que vous utilisez pour la classification EDM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="699d5-227">(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:</span></span>

1. <span data-ttu-id="699d5-228">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="699d5-228">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="699d5-229">Exécutez les cmdlets PowerShell suivantes, en remplaçant le nom de magasin de données « patientrecords » par celui que vous voulez supprimer :</span><span class="sxs-lookup"><span data-stu-id="699d5-229">Run the following PowerShell cmdlets, substituting the data store name of "patientrecords" with the one you want to remove:</span></span>

      ```powershell
      Remove-DlpEdmSchema -Identity patientrecords
      ```

      <span data-ttu-id="699d5-230">Vous êtes invité à confirmer comme suit :</span><span class="sxs-lookup"><span data-stu-id="699d5-230">You will be prompted to confirm, as follows:</span></span>

      > <span data-ttu-id="699d5-231">Confirmer</span><span class="sxs-lookup"><span data-stu-id="699d5-231">Confirm</span></span>
      >
      > <span data-ttu-id="699d5-232">Êtes-vous sûr de vouloir effectuer cette action ?</span><span class="sxs-lookup"><span data-stu-id="699d5-232">Are you sure you want to perform this action?</span></span>
      >
      > <span data-ttu-id="699d5-233">Le schéma EDM pour le magasin de données « patientrecords » va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="699d5-233">EDM Schema for the data store 'patientrecords' will be removed.</span></span>
      >
      > <span data-ttu-id="699d5-234">\[Y\] Oui \[A\] Oui pour tout \[N\] Non \[L\] Non pour tout \[?\] Aide (par défaut « Y ») :</span><span class="sxs-lookup"><span data-stu-id="699d5-234">\[Y\] Yes \[A\] Yes to All \[N\] No \[L\] No to All \[?\] Help (default is "Y"):</span></span>

      > [!TIP]
      >  <span data-ttu-id="699d5-235">Si vous souhaitez que vos modifications se produisent sans confirmation, à l’étape 2, utilisez plutôt la cmdlet Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span><span class="sxs-lookup"><span data-stu-id="699d5-235">If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false</span></span>

### <a name="set-up-a-rule-package"></a><span data-ttu-id="699d5-236">Configurer un package de règles</span><span class="sxs-lookup"><span data-stu-id="699d5-236">Set up a rule package</span></span>

1. <span data-ttu-id="699d5-237">Créez un package de règles au format XML (avec codage Unicode) similaire à l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="699d5-237">Create a rule package in XML format (with Unicode encoding), similar to the following example.</span></span> <span data-ttu-id="699d5-238">(vous pouvez copier, modifier et utiliser notre exemple).</span><span class="sxs-lookup"><span data-stu-id="699d5-238">(You can copy, modify, and use our example.)</span></span>

      <span data-ttu-id="699d5-239">Lorsque vous configurez votre package de règles, veillez à référencer correctement vos fichier .csv et **edm.xml**.</span><span class="sxs-lookup"><span data-stu-id="699d5-239">When you set up your rule package, make sure to correctly reference your .csv file and **edm.xml** file.</span></span> <span data-ttu-id="699d5-240">Vous pouvez copier, modifier et utiliser notre exemple.</span><span class="sxs-lookup"><span data-stu-id="699d5-240">You can copy, modify, and use our example.</span></span> <span data-ttu-id="699d5-241">Dans cet exemple de fichier xml, les champs suivants doivent être personnalisés pour créer votre type sensible d’EDM :</span><span class="sxs-lookup"><span data-stu-id="699d5-241">In this sample xml the following fields needs to be customized to create your EDM sensitive type:</span></span>

      - <span data-ttu-id="699d5-242">**RulePack id & ExactMatch id** : utilisez  [New-GUID](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6)  pour générer un GUID.</span><span class="sxs-lookup"><span data-stu-id="699d5-242">**RulePack id & ExactMatch id**: Use [New-GUID](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-6) to generate a GUID.</span></span>

      - <span data-ttu-id="699d5-243">**Datastore** : ce champ spécifie le magasin de données de recherche EDM à utiliser.</span><span class="sxs-lookup"><span data-stu-id="699d5-243">**Datastore**: This field specifies EDM lookup data store to be used.</span></span> <span data-ttu-id="699d5-244">Vous indiquez un nom de source de données ou un schéma EDM configuré.</span><span class="sxs-lookup"><span data-stu-id="699d5-244">You provide a data source name of a configured EDM Schema.</span></span>

      - <span data-ttu-id="699d5-245">**idMatch** : ce champ pointe vers l’élément principal pour EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-245">**idMatch**: This field points to the primary element for EDM.</span></span>
        - <span data-ttu-id="699d5-246">Matches : spécifie le champ à utiliser dans la recherche exacte.</span><span class="sxs-lookup"><span data-stu-id="699d5-246">Matches: Specifies the field to be used in exact lookup.</span></span> <span data-ttu-id="699d5-247">Vous fournissez un nom de champ pouvant faire l’objet d’une recherche dans le schéma EDM pour le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="699d5-247">You provide a searchable field name in EDM Schema for the DataStore.</span></span>
        - <span data-ttu-id="699d5-248">Classification : ce champ spécifie la correspondance de type sensible qui déclenche la recherche EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-248">Classification: This field specifies the sensitive type match that triggers EDM lookup.</span></span> <span data-ttu-id="699d5-249">Vous pouvez fournir le nom ou le GUID d’une classification personnalisée ou prédéfinie existante.</span><span class="sxs-lookup"><span data-stu-id="699d5-249">You can provide Name or GUID of an existing built-in or custom classification.</span></span>

      - <span data-ttu-id="699d5-250">**Match :** ce champ pointe vers d’autres preuves à proximité d’idMatch.</span><span class="sxs-lookup"><span data-stu-id="699d5-250">**Match:** This field points to additional evidence found in proximity of idMatch.</span></span>
        - <span data-ttu-id="699d5-251">Matches : vous indiquez un nom de champ dans le schéma EDM pour DataStore.</span><span class="sxs-lookup"><span data-stu-id="699d5-251">Matches: You provide any field name in EDM Schema for DataStore.</span></span>
      - <span data-ttu-id="699d5-252">**Resource :** cette section spécifie le nom et la description du type sensible dans plusieurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="699d5-252">**Resource:** This section specifies the name and description for sensitive type in multiple locales.</span></span>
        - <span data-ttu-id="699d5-253">idRef : fournissez un GUID pour ExactMatch ID.</span><span class="sxs-lookup"><span data-stu-id="699d5-253">idRef: You provide GUID for ExactMatch ID.</span></span>
        - <span data-ttu-id="699d5-254">Nom et descriptions : personnalisez si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="699d5-254">Name & descriptions: customize as required.</span></span>

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

1. <span data-ttu-id="699d5-255">Téléchargez le package de règles en exécutant les cmdlets PowerShell suivantes, l’une après l’autre :</span><span class="sxs-lookup"><span data-stu-id="699d5-255">Upload the rule package by running the following PowerShell cmdlets, one at a time:</span></span>

      ```powershell
      $rulepack=Get-Content .\\rulepack.xml -Encoding Byte -ReadCount 0
      New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack
      ```

<span data-ttu-id="699d5-256">À ce stade, vous avez configuré la classification EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-256">At this point, you have set up EDM-based classification.</span></span> <span data-ttu-id="699d5-257">L’étape suivante consiste à hacher les données sensibles, puis à charger les hachages pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="699d5-257">The next step is to hash the sensitive data, and then upload the hashes for indexing.</span></span>

<span data-ttu-id="699d5-258">Rappelez-vous que la procédure précédente de notre schéma PatientRecords définit cinq champs pouvant faire l’objet d’une recherche :  *PatientID*, *MRN*,  *SSN*,  *Phone* et  *DOB*.</span><span class="sxs-lookup"><span data-stu-id="699d5-258">Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*.</span></span> <span data-ttu-id="699d5-259">Notre exemple de package de règles inclut ces champs et référence le fichier de schéma de base de données (**edm.xml**), avec un seul élément  *ExactMatch*  par champ pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="699d5-259">Our example rule package includes those fields and references the database schema file (**edm.xml**), with one *ExactMatch* items per searchable field.</span></span> <span data-ttu-id="699d5-260">Prenons l’élément ExactMatch suivant :</span><span class="sxs-lookup"><span data-stu-id="699d5-260">Consider the following ExactMatch item:</span></span>

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

<span data-ttu-id="699d5-261">À partir de cet exemple, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="699d5-261">In this example, note the following:</span></span>

- <span data-ttu-id="699d5-262">Le nom du magasin de données fait référence au fichier .csv que nous avons créé précédemment :  **dataStore = "PatientRecords"**.</span><span class="sxs-lookup"><span data-stu-id="699d5-262">The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.</span></span>

- <span data-ttu-id="699d5-263">La valeur idMatch fait référence à un champ pouvant faire l’objet d’une recherche figurant dans le fichier de schéma de base de données:  **idMatch matches = "SSN"**.</span><span class="sxs-lookup"><span data-stu-id="699d5-263">The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.</span></span>

- <span data-ttu-id="699d5-264">La valeur de classification fait référence à un type d’informations sensibles existant ou personnalisé :  **classification = "U.S. Social Security Number (SSN)"**</span><span class="sxs-lookup"><span data-stu-id="699d5-264">The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**.</span></span> <span data-ttu-id="699d5-265">(en l’occurrence, nous utilisons le type d’informations sensibles existant pour le numéro de sécurité sociale aux États-Unis).</span><span class="sxs-lookup"><span data-stu-id="699d5-265">(In this case, we use the existing sensitive information type of U.S. Social Security Number.)</span></span>

> [!NOTE]
> <span data-ttu-id="699d5-266">La mise à jour du schéma EDMS avec les ajouts peut prendre de 10 à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="699d5-266">It can take between 10-60 minutes to update the EDMSchema with additions.</span></span> <span data-ttu-id="699d5-267">Vous devez l’effectuer avant d’exécuter les étapes qui utilisent les ajouts.</span><span class="sxs-lookup"><span data-stu-id="699d5-267">The update must complete before you execute steps that use the additions.</span></span>

### <a name="part-2-hash-and-upload-the-sensitive-data"></a><span data-ttu-id="699d5-268">Partie 2 : hacher et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-268">Part 2: Hash and upload the sensitive data</span></span>

<span data-ttu-id="699d5-269">Au cours de cette phase, vous configurez un groupe de sécurité personnalisé et un compte d’utilisateur, et configurez l’outil de chargement de l’agent EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-269">During this phase, you set up a custom security group and user account, and set up the EDM Upload Agent tool.</span></span> <span data-ttu-id="699d5-270">Vous pouvez ensuite utiliser l’outil pour hacher les données sensibles et télécharger les données hachées afin qu’elles puissent être indexées.</span><span class="sxs-lookup"><span data-stu-id="699d5-270">Then, you use the tool to hash the sensitive data, and upload the hashed data so it can be indexed.</span></span>

#### <a name="set-up-the-security-group-and-user-account"></a><span data-ttu-id="699d5-271">Configurer les groupe de sécurité personnalisé et compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="699d5-271">Set up the security group and user account</span></span>

1. <span data-ttu-id="699d5-272">En tant qu’administrateur général, accédez au centre d’administration à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription) et  [créez un groupe de sécurité](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) nommé **EDM\_DataUploaders**.</span><span class="sxs-lookup"><span data-stu-id="699d5-272">As a global administrator, go to the admin center using the appropriate [link for your subscription](#portal-links-for-your-subscription) and [create a security group](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) called **EDM\_DataUploaders**.</span></span>

2. <span data-ttu-id="699d5-273">Ajoutez un ou plusieurs utilisateurs au groupe de sécurité  **EDM\_DataUploaders** </span><span class="sxs-lookup"><span data-stu-id="699d5-273">Add one or more users to the **EDM\_DataUploaders** security group.</span></span> <span data-ttu-id="699d5-274">(ces utilisateurs peuvent gérer la base de données d’informations sensibles).</span><span class="sxs-lookup"><span data-stu-id="699d5-274">(These users will manage the database of sensitive information.)</span></span>

3. <span data-ttu-id="699d5-275">Assurez-vous que tous les utilisateurs qui gèrent les données sensibles sont un administrateur local sur l’ordinateur utilisé pour l’agent de téléchargement EDM.</span><span class="sxs-lookup"><span data-stu-id="699d5-275">Make sure each user who is managing the sensitive data is a local admin on the machine used for the EDM Upload Agent.</span></span>

#### <a name="set-up-the-edm-upload-agent"></a><span data-ttu-id="699d5-276">Configurer l’agent de chargement EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-276">Set up the EDM Upload Agent</span></span>

>[!NOTE]
> <span data-ttu-id="699d5-277">Avant de commencer cette procédure, assurez-vous que vous êtes membre du groupe de sécurité  **EDM\_DataUploaders**  et administrateur local sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="699d5-277">Before you begin this procedure, make sure that you are a member of the **EDM\_DataUploaders** security group and a local admin on your machine.</span></span>

#### <a name="links-to-edm-upload-agent-by-subscription-type"></a><span data-ttu-id="699d5-278">Liens vers l’agent de chargement EDM par type d’abonnement</span><span class="sxs-lookup"><span data-stu-id="699d5-278">Links to EDM upload agent by subscription type</span></span>

- [<span data-ttu-id="699d5-279">Commercial + GCC</span><span class="sxs-lookup"><span data-stu-id="699d5-279">Commercial + GCC</span></span>](https://go.microsoft.com/fwlink/?linkid=2088639)
- [<span data-ttu-id="699d5-280">GCC-High</span><span class="sxs-lookup"><span data-stu-id="699d5-280">GCC-High</span></span>](https://go.microsoft.com/fwlink/?linkid=2137521)
- [<span data-ttu-id="699d5-281">DOD</span><span class="sxs-lookup"><span data-stu-id="699d5-281">DoD</span></span>](https://go.microsoft.com/fwlink/?linkid=2137807)

1. <span data-ttu-id="699d5-282">Téléchargez et installez l’[agent de chargement EDM](#links-to-edm-upload-agent-by-subscription-type) approprié pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="699d5-282">Download and install the appropriate [EDM Upload Agent](#links-to-edm-upload-agent-by-subscription-type) for your subscription.</span></span> <span data-ttu-id="699d5-283">Par défaut, l’emplacement d’installation doit être  **C:\\Program Files\\Microsoft\\EdmUploadAgent**.</span><span class="sxs-lookup"><span data-stu-id="699d5-283">By default, the installation location should be **C:\\Program Files\\Microsoft\\EdmUploadAgent**.</span></span>

   > [!TIP]
   > <span data-ttu-id="699d5-284">Exécutez l'agent sans arguments pour obtenir une liste des paramètres de commande pris en charge.</span><span class="sxs-lookup"><span data-stu-id="699d5-284">To a get a list out of the supported command parameters, run the agent no arguments.</span></span> <span data-ttu-id="699d5-285">Par exemple, « EdmUploadAgent. exe ».</span><span class="sxs-lookup"><span data-stu-id="699d5-285">For example 'EdmUploadAgent.exe'.</span></span>

   > [!NOTE]
   > <span data-ttu-id="699d5-286">Vous pouvez télécharger des données avec EDMUploadAgent vers n’importe quel magasin de données donné deux fois par jour uniquement.</span><span class="sxs-lookup"><span data-stu-id="699d5-286">You can upload data with the EDMUploadAgent to any given data store only twice per day.</span></span>

2. <span data-ttu-id="699d5-287">Pour autoriser l’agent de téléchargement EDM, ouvrez l’invite de commandes Windows (en tant qu’administrateur), puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="699d5-287">To authorize the EDM Upload Agent, open Windows Command Prompt (as an administrator), and then run the following command:</span></span>

   `EdmUploadAgent.exe /Authorize`

3. <span data-ttu-id="699d5-288">Connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365 qui a été ajouté au groupe de sécurité EDM_DataUploaders.</span><span class="sxs-lookup"><span data-stu-id="699d5-288">Sign in with your work or school account for Office 365 that was added to the EDM_DataUploaders security group.</span></span>

<span data-ttu-id="699d5-289">L’étape suivante consiste à utiliser l’agent de téléchargement EDM pour hacher les données sensibles, puis à télécharger les données hachées.</span><span class="sxs-lookup"><span data-stu-id="699d5-289">The next step is to use the EDM Upload Agent to hash the sensitive data, and then upload the hashed data.</span></span>

#### <a name="hash-and-upload-the-sensitive-data"></a><span data-ttu-id="699d5-290">Hacher et télécharger les données sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-290">Hash and upload the sensitive data</span></span>

<span data-ttu-id="699d5-291">Enregistrez le fichier de données sensibles (notre exemple est  **PatientRecords. csv**) sur le disque local de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="699d5-291">Save the sensitive data file (recall our example is **PatientRecords.csv**) to the local drive on the machine.</span></span> <span data-ttu-id="699d5-292">(nous avons enregistré notre exemple de fichier  **PatientRecords.csv**  dans  **C:\\Edm\\Data**).</span><span class="sxs-lookup"><span data-stu-id="699d5-292">(We saved our example **PatientRecords.csv** file to **C:\\Edm\\Data**.)</span></span>

<span data-ttu-id="699d5-293">Pour hacher et télécharger les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="699d5-293">To hash and upload the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadData /DataStoreName \<DataStoreName\> /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="699d5-294">Exemple : **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="699d5-294">Example: **EdmUploadAgent.exe /UploadData /DataStoreName PatientRecords /DataFile C:\\Edm\\Hash\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="699d5-295">Pour séparer et exécuter le hachage de données sensibles dans un environnement isolé, exécutez les étapes de hachage et de téléchargement séparément.</span><span class="sxs-lookup"><span data-stu-id="699d5-295">To separate and execute the hashing of sensitive data in an isolated environment, execute the hashing and upload steps separately.</span></span>

<span data-ttu-id="699d5-296">Pour hacher les données sensibles, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="699d5-296">To hash the sensitive data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /CreateHash /DataFile \<DataFilePath\> /HashLocation \<HashedFileLocation\>`

<span data-ttu-id="699d5-297">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="699d5-297">For example:</span></span>

> <span data-ttu-id="699d5-298">**EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span><span class="sxs-lookup"><span data-stu-id="699d5-298">**EdmUploadAgent.exe /CreateHash /DataFile C:\\Edm\\Data\\PatientRecords.csv /HashLocation C:\\Edm\\Hash**</span></span>

<span data-ttu-id="699d5-299">Pour charger les données hachées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="699d5-299">To upload the hashed data, run the following command in Windows Command Prompt:</span></span>

`EdmUploadAgent.exe /UploadHash /DataStoreName \<DataStoreName\> /HashFile \<HashedSourceFilePath\>`

<span data-ttu-id="699d5-300">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="699d5-300">For example:</span></span>

> <span data-ttu-id="699d5-301">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span><span class="sxs-lookup"><span data-stu-id="699d5-301">**EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\\Edm\\Hash\\PatientRecords.EdmHash**</span></span>


<span data-ttu-id="699d5-302">Pour vérifier que vos données sensibles ont été téléchargées, exécutez la commande suivante dans l’invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="699d5-302">To verify that your sensitive data has been uploaded, run the following command in Command Prompt window:</span></span>


`EdmUploadAgent.exe /GetDataStore`

<span data-ttu-id="699d5-303">La liste des magasins de données apparaît, ainsi que la date de la dernière mise à jour.</span><span class="sxs-lookup"><span data-stu-id="699d5-303">You'll see a list of data stores and when they were last updated.</span></span>

<span data-ttu-id="699d5-304">Si vous voulez afficher toutes les données téléchargées vers un magasin particulier, exécutez la commande suivante dans une invite de commandes Windows :</span><span class="sxs-lookup"><span data-stu-id="699d5-304">If you want to see all the data uploads to a particular store, run the following command in a Windows command prompt:</span></span>

`EdmUploadAgent.exe /GetSession /DataStoreName <DataStoreName>`

<span data-ttu-id="699d5-305">Poursuivez la configuration de votre processus et planifiez l’ [actualisation de votre base de données d’informations sensibles](#refreshing-your-sensitive-information-database).</span><span class="sxs-lookup"><span data-stu-id="699d5-305">Proceed to set up your process and schedule for [Refreshing your sensitive information database](#refreshing-your-sensitive-information-database).</span></span>

<span data-ttu-id="699d5-306">À ce stade, vous êtes prêt à utiliser la classification EDM avec vos services de Cloud Computing Microsoft.</span><span class="sxs-lookup"><span data-stu-id="699d5-306">At this point, you are ready to use EDM-based classification with your Microsoft cloud services.</span></span> <span data-ttu-id="699d5-307">Par exemple, vous pouvez  [configurer une stratégie DLP à l’aide d’une classification EDM](#to-create-a-dlp-policy-with-edm).</span><span class="sxs-lookup"><span data-stu-id="699d5-307">For example, you can [set up a DLP policy using EDM-based classification](#to-create-a-dlp-policy-with-edm).</span></span>

#### <a name="refreshing-your-sensitive-information-database"></a><span data-ttu-id="699d5-308">Actualisation de votre base de données d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-308">Refreshing your sensitive information database</span></span>

<span data-ttu-id="699d5-309">Vous pouvez actualiser quotidiennement ou hebdomadairement votre base de données d’informations sensibles, et l’outil de chargement EDM peut hacher à nouveau les données sensibles, puis recharger les données hachées.</span><span class="sxs-lookup"><span data-stu-id="699d5-309">You can refresh your sensitive information database daily or weekly, and the EDM Upload Tool can re-hash the sensitive data and then reupload the hashed data.</span></span>

1. <span data-ttu-id="699d5-310">Déterminez vos processus et leur fréquence (quotidien ou hebdomadaire) pour actualiser la base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="699d5-310">Determine your process and frequency (daily or weekly) for refreshing the database of sensitive information.</span></span>

2. <span data-ttu-id="699d5-311">Exportez de nouveau les données vers une application, telle que Microsoft Excel, et enregistrez le fichier au format. csv.</span><span class="sxs-lookup"><span data-stu-id="699d5-311">Re-export the sensitive data to an app, such as Microsoft Excel, and save the file in .csv format.</span></span> <span data-ttu-id="699d5-312">Conservez le même nom de fichier et l’emplacement que vous avez utilisé lorsque vous avez suivi les étapes décrites dans [Hachage et téléchargement des données sensibles](#hash-and-upload-the-sensitive-data).</span><span class="sxs-lookup"><span data-stu-id="699d5-312">Keep the same file name and location you used when you followed the steps described in [Hash and upload the sensitive data](#hash-and-upload-the-sensitive-data).</span></span>

      > [!NOTE]
      > <span data-ttu-id="699d5-313">S’il n’y a pas de modifications apportées à la structure (noms de champs) du fichier .csv, vous n’avez pas besoin d’apporter des modifications à votre fichier de schéma de base de données lorsque vous actualisez les données.</span><span class="sxs-lookup"><span data-stu-id="699d5-313">If there are no changes to the structure (field names) of the .csv file, you won't need to make any changes to your database schema file when you refresh the data.</span></span> <span data-ttu-id="699d5-314">Si vous devez apporter des modifications, assurez-vous de modifier le schéma de base de données et votre package de règles en conséquence.</span><span class="sxs-lookup"><span data-stu-id="699d5-314">But if you must make changes, make sure to edit the database schema and your rule package accordingly.</span></span>

3. <span data-ttu-id="699d5-315">Utilisez le  [Planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page)  pour automatiser les étapes 2 et 3 dans la procédure  [Hachage et téléchargement des données sensibles](#hash-and-upload-the-sensitive-data) .</span><span class="sxs-lookup"><span data-stu-id="699d5-315">Use [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) to automate steps 2 and 3 in the [Hash and upload the sensitive data](#hash-and-upload-the-sensitive-data) procedure.</span></span> <span data-ttu-id="699d5-316">Vous pouvez planifier des tâches à l’aide de plusieurs méthodes :</span><span class="sxs-lookup"><span data-stu-id="699d5-316">You can schedule tasks using several methods:</span></span>

      | <span data-ttu-id="699d5-317">Méthode</span><span class="sxs-lookup"><span data-stu-id="699d5-317">Method</span></span>             | <span data-ttu-id="699d5-318">Procédure</span><span class="sxs-lookup"><span data-stu-id="699d5-318">What to do</span></span> |
      | ---------------------- | ---------------- |
      | <span data-ttu-id="699d5-319">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="699d5-319">Windows PowerShell</span></span>     | <span data-ttu-id="699d5-320">Voir la documentation  [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps)  et l’ [exemple de script PowerShell](#example-powershell-script-for-task-scheduler)  dans cet article</span><span class="sxs-lookup"><span data-stu-id="699d5-320">See the [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) documentation and the [example PowerShell script](#example-powershell-script-for-task-scheduler) in this article</span></span> |
      | <span data-ttu-id="699d5-321">API Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="699d5-321">Task Scheduler API</span></span>     | <span data-ttu-id="699d5-322">Consultez la documentation relative au  [Planificateur de tâches](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) </span><span class="sxs-lookup"><span data-stu-id="699d5-322">See the [Task Scheduler](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) documentation</span></span>                                                                                                                                                                                                                                                                                |
      | <span data-ttu-id="699d5-323">Interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="699d5-323">Windows user interface</span></span> | <span data-ttu-id="699d5-324">Dans Windows, cliquez sur  **Démarrer**, puis tapez Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="699d5-324">In Windows, click **Start**, and type Task Scheduler.</span></span> <span data-ttu-id="699d5-325">Dans la liste des résultats, cliquez avec le bouton droit sur  **Planificateur de tâches**, puis sélectionnez  **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="699d5-325">Then, in the list of results, right-click **Task Scheduler**, and choose **Run as administrator**.</span></span>                                                                                                                                                                                                                                                                           |

#### <a name="example-powershell-script-for-task-scheduler"></a><span data-ttu-id="699d5-326">Exemple de script PowerShell pour le planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="699d5-326">Example PowerShell script for Task Scheduler</span></span>

<span data-ttu-id="699d5-327">Cette section inclut un exemple de script PowerShell que vous pouvez utiliser pour planifier vos tâches de hachage de données et de téléchargement des données hachées :</span><span class="sxs-lookup"><span data-stu-id="699d5-327">This section includes an example PowerShell script you can use to schedule your tasks for hashing data and uploading the hashed data:</span></span>

##### <a name="to-schedule-hashing-and-upload-in-a-combined-step"></a><span data-ttu-id="699d5-328">Pour planifier un hachage et effectuer un téléchargement dans une étape seule combinée</span><span class="sxs-lookup"><span data-stu-id="699d5-328">To schedule hashing and upload in a combined step</span></span>

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

#### <a name="to-schedule-hashing-and-upload-as-separate-steps"></a><span data-ttu-id="699d5-329">Pour planifier un hachage et effectuer un téléchargement en deux étapes distinctes</span><span class="sxs-lookup"><span data-stu-id="699d5-329">To schedule hashing and upload as separate steps</span></span>

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

### <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a><span data-ttu-id="699d5-330">Partie 3 : utiliser la classification EDM avec vos services de cloud computing Microsoft</span><span class="sxs-lookup"><span data-stu-id="699d5-330">Part 3: Use EDM-based classification with your Microsoft cloud services</span></span>

<span data-ttu-id="699d5-331">Ces emplacements prennent en charge les types d’informations sensibles EDM :</span><span class="sxs-lookup"><span data-stu-id="699d5-331">These locations are support EDM sensitive information types:</span></span>

- <span data-ttu-id="699d5-332">DLP pour Exchange Online (e-mail)</span><span class="sxs-lookup"><span data-stu-id="699d5-332">DLP for Exchange Online (email)</span></span>
- <span data-ttu-id="699d5-333">OneDrive Entreprise (fichiers)</span><span class="sxs-lookup"><span data-stu-id="699d5-333">OneDrive for Business (files)</span></span>
- <span data-ttu-id="699d5-334">Microsoft Teams (conversations)</span><span class="sxs-lookup"><span data-stu-id="699d5-334">Microsoft Teams (conversations)</span></span>
- <span data-ttu-id="699d5-335">DLP pour SharePoint (fichiers)</span><span class="sxs-lookup"><span data-stu-id="699d5-335">DLP for SharePoint (files)</span></span>
- <span data-ttu-id="699d5-336">Stratégies DLP de la sécurité de l’application Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="699d5-336">Microsoft Cloud App Security DLP policies</span></span>

<span data-ttu-id="699d5-337">Les types d’informations sensibles EDM pour les scénarios suivants sont en cours de développement, mais pas encore disponibles :</span><span class="sxs-lookup"><span data-stu-id="699d5-337">EDM sensitive information types for following scenarios are currently in development, but not yet available:</span></span>

- <span data-ttu-id="699d5-338">Classification automatique des étiquettes de confidentialité et étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="699d5-338">Auto-classification of sensitivity labels and retention labels</span></span>

#### <a name="to-create-a-dlp-policy-with-edm"></a><span data-ttu-id="699d5-339">Pour créer une stratégie DLP avec EDM</span><span class="sxs-lookup"><span data-stu-id="699d5-339">To create a DLP policy with EDM</span></span>

1. <span data-ttu-id="699d5-340">Accédez au Centre de conformité et de sécurité à l’aide du [lien approprié pour votre abonnement](#portal-links-for-your-subscription).</span><span class="sxs-lookup"><span data-stu-id="699d5-340">Go to the Security & Compliance Center using the appropriate [link for your subscription](#portal-links-for-your-subscription).</span></span>

2. <span data-ttu-id="699d5-341">Cliquez sur  **Protection contre la perte de données** \> **Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="699d5-341">Choose **Data loss prevention** \> **Policy**.</span></span>

3. <span data-ttu-id="699d5-342">Sélectionnez  **Créer une stratégie** \> **Personnaliser** \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-342">Choose **Create a policy** \> **Custom** \> **Next**.</span></span>

4. <span data-ttu-id="699d5-343">Sous l’onglet  **Nommez votre stratégie** , spécifiez un nom et une description, puis sélectionnez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-343">On the **Name your policy** tab, specify a name and description, and then choose **Next**.</span></span>

5. <span data-ttu-id="699d5-344">Dans le volet  **Choisir des emplacements** , sélectionnez  **Me laisser choisir des emplacements spécifiques**, puis cliquez sur  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-344">On the **Choose locations** tab, select **Let me choose specific locations**, and then choose **Next**.</span></span>

6. <span data-ttu-id="699d5-345">Dans la colonne  **État** , sélectionnez  **courrier Exchange, Comptes OneDrive, Messages de conversation et de canal de Teams** , puis  **Suivant**</span><span class="sxs-lookup"><span data-stu-id="699d5-345">In the **Status** column, select **Exchange email, OneDrive accounts, Teams chat and channel message** , and then choose **Next**.</span></span>

7. <span data-ttu-id="699d5-346">Sous l’onglet  **Paramètres de stratégie** , sélectionnez  **Utiliser les paramètres avancés**, puis  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-346">On the **Policy settings** tab, choose **Use advanced settings**, and then choose **Next**.</span></span>

8. <span data-ttu-id="699d5-347">Sélectionnez  **+ Nouvelle règle**.</span><span class="sxs-lookup"><span data-stu-id="699d5-347">Choose **+ New rule**.</span></span>

9. <span data-ttu-id="699d5-348">Dans la section **Nom** , spécifiez un nom et une description pour la règle.</span><span class="sxs-lookup"><span data-stu-id="699d5-348">In the **Name** section, specify a name and description for the rule.</span></span>

10. <span data-ttu-id="699d5-349">Dans la section  **Conditions** , dans la liste  **+ Ajouter une condition** , sélectionnez  **Le contenu contient un type sensible**.</span><span class="sxs-lookup"><span data-stu-id="699d5-349">In the **Conditions** section, in the **+ Add a condition** list, choose **Content contains sensitive type**.</span></span>

      ![Le contenu contient des types d’informations sensibles](../media/edm-dlp-newrule-conditions.png)

11. <span data-ttu-id="699d5-351">Recherchez le type d’informations sensibles que vous avez créé lorsque vous avez configuré votre package de règles, puis sélectionnez  **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="699d5-351">Search for the sensitive information type you created when you set up your rule package, and then choose **+ Add**.</span></span>  
    <span data-ttu-id="699d5-352">Ensuite, sélectionnez  **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="699d5-352">Then choose **Done**.</span></span>

12. <span data-ttu-id="699d5-353">Achevez de sélectionner les options applicables à votre règle, telles que  **Notifications à l’utilisateur**, **Remplacements par l’utilisateur**,  **Rapports d’incident** et autres, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="699d5-353">Finish selecting options for your rule, such as **User notifications**, **User overrides**, **Incident reports**, and so on, and then choose **Save**.</span></span>

13. <span data-ttu-id="699d5-354">Sous l’onglet  **Paramètres de stratégie** , examinez vos règles, puis sélectionnez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-354">On the **Policy settings** tab, review your rules, and then choose **Next**.</span></span>

14. <span data-ttu-id="699d5-355">Indiquez si vous voulez activer la stratégie immédiatement, la tester ou la maintenir désactivée.</span><span class="sxs-lookup"><span data-stu-id="699d5-355">Specify whether to turn on the policy right away, test it out, or keep it turned off.</span></span> <span data-ttu-id="699d5-356">Ensuite, choisissez  **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="699d5-356">Then choose **Next**.</span></span>

15. <span data-ttu-id="699d5-357">Sous l’onglet  **Examiner vos paramètres** , révisez votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="699d5-357">On the **Review your settings** tab, review your policy.</span></span> <span data-ttu-id="699d5-358">Apportez les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="699d5-358">Make any needed changes.</span></span> <span data-ttu-id="699d5-359">Lorsque vous avez terminé, sélectionnez  **Créer**.</span><span class="sxs-lookup"><span data-stu-id="699d5-359">When you're ready, choose **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="699d5-360">Comptez environ une heure avant que votre nouvelle stratégie DLP soit appliquée à l’ensemble de votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="699d5-360">Allow approximately one hour for your new DLP policy to work its way through your data center.</span></span>

## <a name="related-articles"></a><span data-ttu-id="699d5-361">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="699d5-361">Related articles</span></span>

- [<span data-ttu-id="699d5-362">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="699d5-362">Sensitive information type-entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="699d5-363">Types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="699d5-363">Custom sensitive information types</span></span>](custom-sensitive-info-types.md)
- [<span data-ttu-id="699d5-364">Vue d’ensemble des stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="699d5-364">Overview of DLP policies</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="699d5-365">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="699d5-365">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)
- [<span data-ttu-id="699d5-366">New-DlpEdmSchema</span><span class="sxs-lookup"><span data-stu-id="699d5-366">New-DlpEdmSchema</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-dlpedmschema?view=exchange-ps)

