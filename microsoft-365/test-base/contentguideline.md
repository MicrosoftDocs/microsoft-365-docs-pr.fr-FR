---
title: Recommandations en matière de package de test
description: Passer en revue les recommandations relatives au package de test
search.appverid: MET150
author: mansipatel-usl
ms.author: mapatel
manager: rshastri
audience: Software-Vendor
ms.topic: how-to
ms.date: 07/06/2021
ms.service: virtual-desktop
localization_priority: Normal
ms.collection: TestBase-M365
ms.custom: ''
ms.reviewer: mapatel
f1.keywords: NOCSH
ms.openlocfilehash: b6842f793627bddeab842bbd9570c9c3481699a6
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322756"
---
# <a name="test-package-guidelines"></a><span data-ttu-id="31b4e-103">Recommandations en matière de package de test</span><span class="sxs-lookup"><span data-stu-id="31b4e-103">Test package guidelines</span></span>

## <a name="1---script-referencing"></a><span data-ttu-id="31b4e-104">1. Référencement de script</span><span class="sxs-lookup"><span data-stu-id="31b4e-104">1.   Script referencing</span></span>

<span data-ttu-id="31b4e-105">Lorsque vous téléchargez un .zip sur le portail, nous dézipons tout le contenu de ce fichier dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="31b4e-105">When you upload a .zip file to the portal, we unzip all the content of that file into a root folder.</span></span> <span data-ttu-id="31b4e-106">Vous n’avez pas besoin d’écrire de code pour cette opération de dézipage initiale.</span><span class="sxs-lookup"><span data-stu-id="31b4e-106">You do not need to write any code to do this initial unzip operation.</span></span> <span data-ttu-id="31b4e-107">Vous pouvez également référencer n’importe quel fichier dans le .zip en utilisant le chemin d’accès relatif au fichier zip téléchargé.</span><span class="sxs-lookup"><span data-stu-id="31b4e-107">You also can reference any file within the .zip by using the path relative to the zip file uploaded.</span></span>

<span data-ttu-id="31b4e-108">Dans l’exemple ci-dessous, nous montrons comment vous pouvez référencer vos binaires/scripts à partir du champ d’entrée dans l’onglet Tâches. Le texte en bleu doit être entré dans le champ de chemin **d’accès** script **sans les guillemets.**</span><span class="sxs-lookup"><span data-stu-id="31b4e-108">In the example below, we show how you can reference your binaries/scripts from the input field in the Tasks tab. The text in blue should be entered into the **Script path** field **without the quotation marks.**</span></span>

<span data-ttu-id="31b4e-109">Il est important de connaître le contenu de votre fichier zip avant de le télécharger.</span><span class="sxs-lookup"><span data-stu-id="31b4e-109">It is important you are aware of the content within your zip file before uploading it.</span></span> <span data-ttu-id="31b4e-110">Souvent, lorsque vous compressez un dossier, votre ordinateur local crée un dossier principal sous le fichier zip.</span><span class="sxs-lookup"><span data-stu-id="31b4e-110">Often when zipping a folder, your local machine will create a main folder underneath the zip file.</span></span> <span data-ttu-id="31b4e-111">Dans ce cas, le référencement sera affiché en **gras** ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="31b4e-111">In this case, the referencing will be as shown in **bold** below:</span></span>

 <span data-ttu-id="31b4e-112">**Contoso_App_Folder.zip**</span><span class="sxs-lookup"><span data-stu-id="31b4e-112">**Contoso_App_Folder.zip**</span></span>
~~~ 
├── Contoso_App_Folder

│   ├── file1.exe

│   ├── ScriptX.ps1

│   ├── folder1

│        ├── file3.exe

│        ├── script.ps1
~~~

  - <span data-ttu-id="31b4e-113">ScriptX.ps1 – **« Contoso_App_Folder/ScriptX.ps1 »**</span><span class="sxs-lookup"><span data-stu-id="31b4e-113">ScriptX.ps1 – **“Contoso_App_Folder/ScriptX.ps1”**</span></span>
  - <span data-ttu-id="31b4e-114">Script.ps1 – **« Contoso_App_Folder/folder1/script.ps1 »**</span><span class="sxs-lookup"><span data-stu-id="31b4e-114">Script.ps1 – **“Contoso_App_Folder/folder1/script.ps1”**</span></span>

<span data-ttu-id="31b4e-115">Dans d’autres cas, il se peut que vos fichiers ou votre contenu se trouve juste en dessous de votre fichier zip, c’est-à-dire qu’aucun dossier de 2e niveau :</span><span class="sxs-lookup"><span data-stu-id="31b4e-115">Other times, your zip file may have your files or content right underneath it i.e. no 2nd-level folder:</span></span>

 <span data-ttu-id="31b4e-116">**Zip_file_uploaded.zip**</span><span class="sxs-lookup"><span data-stu-id="31b4e-116">**Zip_file_uploaded.zip**</span></span>
~~~ 
├── file1.exe

├── ScriptX.ps1

├── folder1

│   ├── file3.exe

│   ├── script.ps1
~~~
  - <span data-ttu-id="31b4e-117">ScriptX.ps1 – **« ScriptX.ps1 »**</span><span class="sxs-lookup"><span data-stu-id="31b4e-117">ScriptX.ps1 – **“ScriptX.ps1”**</span></span>
  - <span data-ttu-id="31b4e-118">Script.ps1 - **« folder1/script.ps1 »**</span><span class="sxs-lookup"><span data-stu-id="31b4e-118">Script.ps1 – **“folder1/script.ps1”**</span></span>
  
## <a name="2---script-execution"></a><span data-ttu-id="31b4e-119">2. Exécution de script</span><span class="sxs-lookup"><span data-stu-id="31b4e-119">2.   Script execution</span></span>

<span data-ttu-id="31b4e-120">**Tests out-of-Box :** Le package d’application doit contenir au moins trois scripts PowerShell qui exécuteront l’installation, le lancement et la fermeture sans surveillance de l’application et de ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="31b4e-120">**Out-of-Box tests:** The application package needs to contain at least three PowerShell scripts that will execute unattended installing, launching, and closing of the application and its dependencies.</span></span> <span data-ttu-id="31b4e-121">Chaque script doit gérer la vérification de ses propres conditions préalables, la validation de sa réussite, ainsi que le nettoyage après lui-même (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="31b4e-121">Each script should handle checking its own prerequisites, validating it succeeded, as well as cleaning up after itself (if necessary).</span></span>

<span data-ttu-id="31b4e-122">**Tests fonctionnels :** Le package d’application doit contenir au moins un script PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31b4e-122">**Functional tests:** The application package needs to contain at least one PowerShell script.</span></span> <span data-ttu-id="31b4e-123">Lorsque plusieurs scripts sont fournis, ils sont exécutés dans une séquence de chargement et un échec dans un script particulier arrête l’exécution des scripts suivants.</span><span class="sxs-lookup"><span data-stu-id="31b4e-123">Where more than one script is provided, the scripts are run in upload sequence and a failure in a particular script will stop subsequent scripts from executing.</span></span>

### <a name="script-requirements"></a><span data-ttu-id="31b4e-124">Conditions requises pour les scripts</span><span class="sxs-lookup"><span data-stu-id="31b4e-124">Script requirements</span></span>

<span data-ttu-id="31b4e-125">• PowerShell Version 5.1+</span><span class="sxs-lookup"><span data-stu-id="31b4e-125">•   PowerShell Version 5.1+</span></span>     

<span data-ttu-id="31b4e-126">• Exécution sans surveillance</span><span class="sxs-lookup"><span data-stu-id="31b4e-126">•   Unattended execution</span></span>    

<span data-ttu-id="31b4e-127">• Code de retour d’erreur</span><span class="sxs-lookup"><span data-stu-id="31b4e-127">•   Error return code</span></span>               

<span data-ttu-id="31b4e-128">• Valider la réussite</span><span class="sxs-lookup"><span data-stu-id="31b4e-128">•   Validate success</span></span>            

<span data-ttu-id="31b4e-129">• Journalisation dans un dossier journal spécifique au script</span><span class="sxs-lookup"><span data-stu-id="31b4e-129">•   Logging to script specific log folder</span></span>

<span data-ttu-id="31b4e-130">Chaque script doit s’exécuter sans surveillance pour s’exécuter correctement dans le pipeline de test.</span><span class="sxs-lookup"><span data-stu-id="31b4e-130">Each script needs to run completely unattended to successfully execute in the test pipeline.</span></span>

> [!Note]
> <span data-ttu-id="31b4e-131">Les scripts doivent renvoyer « 0 » à l’exécution réussie et un code d’erreur non nul si une erreur se produit pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="31b4e-131">Scripts should return “0” on successful completion and a non-zero error code if any error occurs during execution.</span></span>

<span data-ttu-id="31b4e-132">Chaque script doit vérifier qu’il a été correctement lancé.</span><span class="sxs-lookup"><span data-stu-id="31b4e-132">Each script should validate that it ran successfully.</span></span> <span data-ttu-id="31b4e-133">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="31b4e-133">E.g.</span></span> <span data-ttu-id="31b4e-134">Le script d’installation doit vérifier l’existence de certains binaires et/ou clés de Registre sur le système, une fois que le fichier binaire du programme d’installation a terminé son exécution pour garantir avec un degré raisonnable de confiance que l’installation a réussi.</span><span class="sxs-lookup"><span data-stu-id="31b4e-134">the install script should check for the existence of certain binaries and/or registry keys on the system, after the installer binary finishes executing to ensure with a reasonable degree of confidence that the installation was successful.</span></span> 

<span data-ttu-id="31b4e-135">Cela est nécessaire pour diagnostiquer correctement l’endroit où des erreurs se produisent lors d’une utilisation de test, par exemple, l’impossibilité d’installer l’application ou de la lancer.</span><span class="sxs-lookup"><span data-stu-id="31b4e-135">This is necessary to properly diagnose where errors occur during a test run, e.g. unable to install the application successfully versus being unable to launch it.</span></span>

> [!Important]
> <span data-ttu-id="31b4e-136">**Évitez les problèmes suivants :** Les scripts ne doivent pas redémarrer l’ordinateur, si un redémarrage est nécessaire, veuillez le spécifier pendant le chargement de vos scripts.</span><span class="sxs-lookup"><span data-stu-id="31b4e-136">**Avoid the following:** Scripts should not reboot the machine, if a reboot is necessary please specify this during the upload of your scripts.</span></span>

## <a name="3---log-collection"></a><span data-ttu-id="31b4e-137">3. Collection de journaux</span><span class="sxs-lookup"><span data-stu-id="31b4e-137">3.   Log collection</span></span>

<span data-ttu-id="31b4e-138">Chaque script doit générer tous les journaux qu’il génère dans un dossier nommé ```logs``` .</span><span class="sxs-lookup"><span data-stu-id="31b4e-138">Each script should output any logs it generates into a folder named ```logs```.</span></span> <span data-ttu-id="31b4e-139">Tous les dossiers du répertoire nommé seront copiés et présentés ```logs``` en téléchargement sur la ```Test Results``` page.</span><span class="sxs-lookup"><span data-stu-id="31b4e-139">All folders in the directory named ```logs``` will be copied and presented for download on the ```Test Results``` page.</span></span>

<span data-ttu-id="31b4e-140">Par exemple, le script d’installation (qui peut se trouver dans le répertoire **App/scripts/install)** peut obtenir ses journaux dans : **logs/install.log**, de telle telle part que le journal final se trouve à l’emplacement suivant : **Apps/scripts/install/logs/install.log**</span><span class="sxs-lookup"><span data-stu-id="31b4e-140">For example, the installation script (which may be located in the **App/scripts/install** directory) can output its logs to: **logs/install.log**, such that the final log will be at: **Apps/scripts/install/logs/install.log**</span></span>

<span data-ttu-id="31b4e-141">Le système sélectionne le fichier ainsi que d’autres fichiers dans d’autres dossiers et le rassemble ```install.log``` ```logs``` pour téléchargement.</span><span class="sxs-lookup"><span data-stu-id="31b4e-141">The system will pick up the ```install.log``` file along with other files within other ```logs``` folders and collate it for download.</span></span>


## <a name="4---application-binaries"></a><span data-ttu-id="31b4e-142">4. Binaires d’application</span><span class="sxs-lookup"><span data-stu-id="31b4e-142">4.   Application binaries</span></span>

<span data-ttu-id="31b4e-143">Tous les fichiers binaires et dépendances doivent être inclus dans le fichier zip unique.</span><span class="sxs-lookup"><span data-stu-id="31b4e-143">Any binaries and dependencies should be included in the single zip file.</span></span> 

<span data-ttu-id="31b4e-144">Ceux-ci doivent inclure tous les éléments nécessaires à l’installation de l’application (par exemple, le programme d’installation de l’application) ; si l’application dépend d’une infrastructure, telle que .NET Core/Standard ou .NET Framework, celles-ci doivent être incluses dans le fichier et référencés correctement dans les scripts fournis.</span><span class="sxs-lookup"><span data-stu-id="31b4e-144">These should include everything necessary for installation of the application (e.g. the application installer); if the application has a dependency on any frameworks, such as .NET Core/Standard or .NET Framework, these should be included in the file and referenced correctly in the provided scripts.</span></span>


> [!Note]
> <span data-ttu-id="31b4e-145">Le fichier zip téléchargé ne peut pas avoir d’espaces ou de caractères spéciaux dans son nom</span><span class="sxs-lookup"><span data-stu-id="31b4e-145">The uploaded zip file cannot have any spaces or special characters in its name</span></span>

## <a name="next-steps"></a><span data-ttu-id="31b4e-146">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="31b4e-146">Next steps</span></span>

<span data-ttu-id="31b4e-147">Passer à l’article suivant pour afficher certaines **questions fréquemment posées (FAQ)**</span><span class="sxs-lookup"><span data-stu-id="31b4e-147">Advance to the next article to view some **Frequently Asked Questions (FAQ)**</span></span>
> [!div class="nextstepaction"]
> [<span data-ttu-id="31b4e-148">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="31b4e-148">Next step</span></span>](faq.md)
