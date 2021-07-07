---
title: Définir vos tâches de test
description: Définir vos tâches de test
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
ms.openlocfilehash: 64abb5b10e3dc1d52b6baf8ceccd5aff2baacefe
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322691"
---
# <a name="step-4-the-tasks-tab"></a><span data-ttu-id="46002-103">Étape 4 : onglet Tâches</span><span class="sxs-lookup"><span data-stu-id="46002-103">Step 4: The tasks tab</span></span>

<span data-ttu-id="46002-104">Sous l’onglet Tâches, vous devez fournir les chemins d’accès à vos scripts de test qui se trouveraient dans le dossier zip que vous avez chargé sous l’onglet fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="46002-104">On the tasks tab, you are expected to provide the paths to your test scripts which are in the zip folder you uploaded under the binaries tab.</span></span>

  - <span data-ttu-id="46002-105">**Scripts de test out-of-box :** Tapez les chemins d’accès relatifs à vos scripts d’installation, de lancement, de fermeture et de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="46002-105">**Out of Box Test Scripts:** Type in the relative paths to your install, launch, close and uninstall scripts.</span></span> <span data-ttu-id="46002-106">Vous avez également la possibilité de sélectionner des paramètres supplémentaires pour le script d’installation.</span><span class="sxs-lookup"><span data-stu-id="46002-106">You also have the option to select additional settings for the install script.</span></span>
  - <span data-ttu-id="46002-107">**Scripts de test fonctionnels :** Tapez le chemin d’accès relatif à chaque script de test fonctionnel téléchargé.</span><span class="sxs-lookup"><span data-stu-id="46002-107">**Functional Test Scripts:** Type in the relative path to each functional test script uploaded.</span></span> <span data-ttu-id="46002-108">Des scripts de test fonctionnels supplémentaires peuvent être ajoutés à l’aide ```Add Script``` du bouton.</span><span class="sxs-lookup"><span data-stu-id="46002-108">Additional functional test scripts can be added using the ```Add Script``` button.</span></span> <span data-ttu-id="46002-109">Vous avez besoin d’au moins un script (1) et pouvez ajouter jusqu’à huit (8) scripts de test fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="46002-109">You need a minimum of one (1) script and can add up to eight (8) functional test scripts.</span></span> 
  
    <span data-ttu-id="46002-110">Les scripts sont exécutés dans la séquence de chargement et un échec dans un script particulier arrête l’exécution des scripts suivants.</span><span class="sxs-lookup"><span data-stu-id="46002-110">The scripts are run in upload sequence and a failure in a particular script will stop subsequent scripts from executing.</span></span>
    <span data-ttu-id="46002-111">Vous avez également la possibilité de sélectionner des paramètres supplémentaires pour chaque script fourni.</span><span class="sxs-lookup"><span data-stu-id="46002-111">You also have the option of selecting additional settings for each script provided.</span></span>

## <a name="set-script-path"></a><span data-ttu-id="46002-112">Définir le chemin d’accès au script</span><span class="sxs-lookup"><span data-stu-id="46002-112">Set script path</span></span>

![Image de la tâche de test](Media/testtask.png)

<span data-ttu-id="46002-114">Voici un exemple de la façon de fournir le chemin d’accès relatif sur une structure de dossiers :</span><span class="sxs-lookup"><span data-stu-id="46002-114">Sample of how to provide the relative path on a folder structure is below:</span></span>

<span data-ttu-id="46002-115">_**Zip_file_uploaded**_</span><span class="sxs-lookup"><span data-stu-id="46002-115">_**Zip_file_uploaded**_</span></span>
~~~
├── file1.exe

├── ScriptX.ps1

├── folder1

│   ├── file3.exe

│   ├── script.ps1
~~~
  - <span data-ttu-id="46002-116">**ScriptX.ps1** aurait été le cas.</span><span class="sxs-lookup"><span data-stu-id="46002-116">**ScriptX.ps1** would have.</span></span> <span data-ttu-id="46002-117">_ScriptX.ps1_ comme chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="46002-117">_ScriptX.ps1_ as the relative path.</span></span>
  - <span data-ttu-id="46002-118">**Script.ps1** _dossier1/script.ps1_ comme chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="46002-118">**Script.ps1** would have _folder1/script.ps1_ as the relative path.</span></span>


## <a name="next-steps"></a><span data-ttu-id="46002-119">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="46002-119">Next steps</span></span>

<span data-ttu-id="46002-120">Afficher les détails de l’onglet Options de test dans l’article suivant</span><span class="sxs-lookup"><span data-stu-id="46002-120">View details of the Test Options tab in the next article</span></span> 
> [!div class="nextstepaction"]
> [<span data-ttu-id="46002-121">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="46002-121">Next step</span></span>](testoptions.md)
