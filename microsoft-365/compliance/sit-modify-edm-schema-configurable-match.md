---
title: Modifier le schéma de correspondance des données exactes pour utiliser la correspondance configurable
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
description: Découvrez comment modifier un schéma EDM pour utiliser une correspondance configurable.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 2211e4d99d97fcce241a5f4c3ea7c9d8122ca9d7
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49656800"
---
# <a name="modify-exact-data-match-schema-to-use-configurable-match"></a><span data-ttu-id="dc6db-103">Modifier le schéma de correspondance des données exactes pour utiliser la correspondance configurable</span><span class="sxs-lookup"><span data-stu-id="dc6db-103">Modify Exact Data Match schema to use configurable match</span></span>

<span data-ttu-id="dc6db-104">La classification EDM (Exact Data Match) vous permet de créer des types d’informations sensibles personnalisés qui font référence à des valeurs exactes dans une base de données d’informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="dc6db-104">Exact Data Match (EDM) based classification enables you to create custom sensitive information types that refer to exact values in a database of sensitive information.</span></span> <span data-ttu-id="dc6db-105">Lorsque vous devez autoriser les variantes d’une chaîne exacte, vous pouvez utiliser une *correspondance configurable* pour indiquer à Microsoft 365 d’ignorer la casse et certains séparateurs.</span><span class="sxs-lookup"><span data-stu-id="dc6db-105">When you need to allow for variants of a exact string, you can use *configurable match* to tell Microsoft 365 to ignore case and some delimiters.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="dc6db-106">Utilisez cette procédure pour modifier un schéma EDM et un fichier de données existants.</span><span class="sxs-lookup"><span data-stu-id="dc6db-106">Use this procedure to modify an existing EDM schema and data file.</span></span>

1. <span data-ttu-id="dc6db-107">Désinstallez **EdmUploadAgent.exe** de l’ordinateur que vous utilisez pour vous connecter à Microsoft 365 afin de charger les fichiers de données et le modèle EDM.</span><span class="sxs-lookup"><span data-stu-id="dc6db-107">Uninstall the **EdmUploadAgent.exe** from the computer that you use to connect to Microsoft 365 for EDM schema and data file upload purposes.</span></span>

2. <span data-ttu-id="dc6db-108">Téléchargez le fichier **EdmUploadAgent.exe** approprié pour votre abonnement en utilisant les liens ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="dc6db-108">Download the appropriate **EdmUploadAgent.exe** file for your subscription using the links below:</span></span>
    - <span data-ttu-id="dc6db-109">[Commercial + GCC](https://go.microsoft.com/fwlink/?linkid=2088639) : pour la plupart des clients commerciaux</span><span class="sxs-lookup"><span data-stu-id="dc6db-109">[Commercial + GCC](https://go.microsoft.com/fwlink/?linkid=2088639) - most commercial customers should use this</span></span>
    - <span data-ttu-id="dc6db-110">[GCC-High](https://go.microsoft.com/fwlink/?linkid=2137521) : conçu spécifiquement pour les abonnés cloud du secteur public haute sécurité</span><span class="sxs-lookup"><span data-stu-id="dc6db-110">[GCC-High](https://go.microsoft.com/fwlink/?linkid=2137521) - This is specifically for high security government cloud subscribers</span></span>
    - <span data-ttu-id="dc6db-111">[DoD](https://go.microsoft.com/fwlink/?linkid=2137807) : conçu spécifiquement pour les clients cloud du Department of Defense américain</span><span class="sxs-lookup"><span data-stu-id="dc6db-111">[DoD](https://go.microsoft.com/fwlink/?linkid=2137807) - this is specifically for United States Department of Defense cloud customers</span></span>

3. <span data-ttu-id="dc6db-112">Autorisez l’agent de chargement EDM, ouvrez la fenêtre Invite de commandes (en tant qu’administrateur), puis exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dc6db-112">Authorize the EDM Upload Agent, open Command Prompt window (as an administrator) and run the following command:</span></span>

   `EdmUploadAgent.exe /Authorize`

4. <span data-ttu-id="dc6db-113">Si vous n’avez pas de copie actuelle du schéma existant, vous devez en télécharger une. Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="dc6db-113">If you don't have a current copy of the existing schema, you'll need to download a copy of the existing schema, run this command:</span></span>

    `EdmUploadAgent.exe /SaveSchema /DataStoreName <dataStoreName> [/OutputDir [Output dir location]]`

5. <span data-ttu-id="dc6db-114">Personnalisez le schéma de sorte que chaque colonne utilise « caseInsensitive » et/ou « ignoredDelimiters ».</span><span class="sxs-lookup"><span data-stu-id="dc6db-114">Customize the schema so each column utilizes “caseInsensitive” and / or “ignoredDelimiters”.</span></span>  <span data-ttu-id="dc6db-115">La valeur par défaut de « caseInsensitive » est « false » et « ignoredDelimiters » est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="dc6db-115">The default value for “caseInsensitive” is “false” and for “ignoredDelimiters”, it is an empty string.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc6db-116">Le type d’informations sensibles personnalisé sous-jacent ou le type d’informations sensibles intégré utilisé pour détecter le modèle regex général doivent prendre en charge la détection des entrées de variantes indiquées avec ignoredDelimiters.</span><span class="sxs-lookup"><span data-stu-id="dc6db-116">The underlying custom sensitive information type or built in sensitive information type used to detect the general regex pattern must support detection of the variations inputs listed with ignoredDelimiters.</span></span> <span data-ttu-id="dc6db-117">Par exemple, le type d’informations sensibles intégré Numéro de sécurité sociale (SSN) américain permet de détecter les variantes des données qui incluent des tirets, des espaces ou une absence d’espace entre les numéros groupés qui composent le numéro de sécurité sociale.</span><span class="sxs-lookup"><span data-stu-id="dc6db-117">For example, the built in U.S. social security number (SSN) sensitive information type can detect variations in the data that include dashes, spaces, or lack of spaces between the grouped numbers that make up the SSN.</span></span> <span data-ttu-id="dc6db-118">Par conséquent, les seuls délimiteurs pertinents à inclure dans ignoredDelimiters EDM pour les données SSN sont : les tirets et les espaces.</span><span class="sxs-lookup"><span data-stu-id="dc6db-118">As a result, the only delimiters that are relevant to include in EDM’s ignoredDelimiters for SSN data are: dash and space.</span></span>

<span data-ttu-id="dc6db-119">Voici un exemple de schéma qui simule la correspondance non sensible à la casse en créant les colonnes supplémentaires nécessaires pour identifier les variations de casse dans les données sensibles.</span><span class="sxs-lookup"><span data-stu-id="dc6db-119">Here is a sample schema that simulates case insensitive match by creating the extra columns needed to recognize case variations in the sensitive data.</span></span>

```xml
<EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
  <DataStore name="PatientRecords" description="Schema for patient records policy" version="1">
           <Field name="PolicyNumber" searchable="true" />
           <Field name="PolicyNumberLowerCase" searchable="true" />
           <Field name="PolicyNumberUpperCase" searchable="true" />
           <Field name="PolicyNumberCapitalLetters" searchable="true" />
  </DataStore>
</EdmSchema>
```

<span data-ttu-id="dc6db-120">Dans l’exemple ci-dessus, les variantes de la colonne d’origine `PolicyNumber` ne sont plus nécessaires si `caseInsensitive` et `ignoredDelimiters` sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="dc6db-120">In the above example, the variations of the original `PolicyNumber` column will no longer be needed if both `caseInsensitive` and `ignoredDelimiters` are added.</span></span>

<span data-ttu-id="dc6db-121">Pour mettre à jour ce schéma de façon à ce qu’EDM utilise la correspondance configurable, utilisez les indicateurs `caseInsensitive` et `ignoredDelimiters`.</span><span class="sxs-lookup"><span data-stu-id="dc6db-121">To update this schema so that EDM uses configurable match use the `caseInsensitive` and `ignoredDelimiters` flags.</span></span>  <span data-ttu-id="dc6db-122">Cela se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="dc6db-122">Here's how that looks:</span></span>

```xml
<EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
  <DataStore name="PatientRecords" description="Schema for patient records policy" version="1">
         <Field name="PolicyNumber" searchable="true" caseInsensitive="true" ignoredDelimiters="-,/,*,#,^" />
  </DataStore>
</EdmSchema>
```

<span data-ttu-id="dc6db-123">L’indicateur `ignoredDelimiters` prend en charge tous les caractères non alphanumériques. Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="dc6db-123">The `ignoredDelimiters` flag supports any non-alphanumeric character, here are some examples:</span></span>
- <span data-ttu-id="dc6db-124">\.</span><span class="sxs-lookup"><span data-stu-id="dc6db-124">\.</span></span>
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

<span data-ttu-id="dc6db-125">L’indicateur `ignoredDelimiters` ne prend pas en charge :</span><span class="sxs-lookup"><span data-stu-id="dc6db-125">The `ignoredDelimiters` flag doesn't support:</span></span>
- <span data-ttu-id="dc6db-126">Les caractères 0 à 9</span><span class="sxs-lookup"><span data-stu-id="dc6db-126">characters 0-9</span></span>
- <span data-ttu-id="dc6db-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="dc6db-127">A-Z</span></span>
- <span data-ttu-id="dc6db-128">a-z</span><span class="sxs-lookup"><span data-stu-id="dc6db-128">a-z</span></span>
- \"
- \,

6. <span data-ttu-id="dc6db-129">Connectez-vous au Centre de sécurité et conformité en utilisant la procédure [Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="dc6db-129">Connect to the Security & Compliance center using the procedures in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

7. <span data-ttu-id="dc6db-130">Mettez à jour votre schéma en exécutant ces applets de commande une par une :</span><span class="sxs-lookup"><span data-stu-id="dc6db-130">Update your schema by running these cmdlets one at a time:</span></span>

`$edmSchemaXml=Get-Content .\\edm.xml -Encoding Byte -ReadCount 0`

`Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

8. <span data-ttu-id="dc6db-131">Si nécessaire, mettez à jour le fichier de données pour qu’il corresponde à la nouvelle version du schéma.</span><span class="sxs-lookup"><span data-stu-id="dc6db-131">If necessary, update the data file to match the new schema version</span></span>

> [!TIP]
> <span data-ttu-id="dc6db-132">Si vous le souhaitez, vous pouvez exécuter une validation par rapport à votre fichier CSV avant de charger en exécutant :</span><span class="sxs-lookup"><span data-stu-id="dc6db-132">Optionally, you can run a validation against your csv file before uploading by running:</span></span>
>
>`EdmUploadAgent.exe /ValidateData /DataFile [data file] [schema file]`
>
><span data-ttu-id="dc6db-133">Pour plus d’informations sur tous les paramètres pris en charge par EdmUploadAgent.exe</span><span class="sxs-lookup"><span data-stu-id="dc6db-133">For more information on all the EdmUploadAgent.exe >supported parameters run</span></span>
>
> `EdmUploadAgent.exe /?`

9. <span data-ttu-id="dc6db-134">Ouvrez la fenêtre Invite de commandes (en tant qu’administrateur), puis exécutez la commande suivante pour hacher et charger vos données sensibles :</span><span class="sxs-lookup"><span data-stu-id="dc6db-134">Open Command Prompt window (as an administrator) and run the following command to hash and upload your sensitive data:</span></span>

    `EdmUploadAgent.exe /UploadData /DataStoreName [DS Name] /DataFile [data file] /HashLocation [hash file location] /Salt [custom salt] /Schema [Schema file]`


## <a name="related-articles"></a><span data-ttu-id="dc6db-135">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="dc6db-135">Related articles</span></span>

- [<span data-ttu-id="dc6db-136">Créer un type d’informations sensibles personnalisé à l’aide d’une classification de correspondance exacte des données</span><span class="sxs-lookup"><span data-stu-id="dc6db-136">Create a custom sensitive information type with Exact Data Match based classification</span></span>](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)
- [<span data-ttu-id="dc6db-137">Définitions d’entités des types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="dc6db-137">Sensitive information type-entity definitions</span></span>](sensitive-information-type-entity-definitions.md)
- [<span data-ttu-id="dc6db-138">Types d’informations sensibles personnalisés</span><span class="sxs-lookup"><span data-stu-id="dc6db-138">Custom sensitive information types</span></span>](custom-sensitive-info-types.md)
- [<span data-ttu-id="dc6db-139">Vue d’ensemble des stratégies DLP</span><span class="sxs-lookup"><span data-stu-id="dc6db-139">Overview of DLP policies</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="dc6db-140">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="dc6db-140">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)
- [<span data-ttu-id="dc6db-141">New-DlpEdmSchema</span><span class="sxs-lookup"><span data-stu-id="dc6db-141">New-DlpEdmSchema</span></span>](https://docs.microsoft.com/powershell/module/exchange/new-dlpedmschema)