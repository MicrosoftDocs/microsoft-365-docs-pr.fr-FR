---
title: Gérer les exclusions de dossiers d’automatisation
description: Ajoutez des exclusions de dossier d’automatisation pour contrôler les fichiers exclus d’un examen automatisé.
keywords: gérer, automatisation, exclusion, bloquer, nettoyer, malveillant
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 37a251acd3b7631cffffaf2eb76bf0f2b4954ee6
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185836"
---
# <a name="manage-automation-folder-exclusions"></a><span data-ttu-id="0ede3-104">Gérer les exclusions de dossiers d’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ede3-104">Manage automation folder exclusions</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="0ede3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0ede3-105">**Applies to:**</span></span>
- [<span data-ttu-id="0ede3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0ede3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="0ede3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0ede3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="0ede3-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0ede3-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="0ede3-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0ede3-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-automationexclusionfolder-abovefoldlink)

<span data-ttu-id="0ede3-110">Les exclusions de dossiers Automation vous permettent de spécifier les dossiers que l’examen automatisé ignorera.</span><span class="sxs-lookup"><span data-stu-id="0ede3-110">Automation folder exclusions allow you to specify folders that the Automated investigation will skip.</span></span> 

<span data-ttu-id="0ede3-111">Vous pouvez contrôler les attributs suivants concernant le dossier que vous souhaitez ignorer :</span><span class="sxs-lookup"><span data-stu-id="0ede3-111">You can control the following attributes about the folder that you'd like to be skipped:</span></span>
- <span data-ttu-id="0ede3-112">Folders</span><span class="sxs-lookup"><span data-stu-id="0ede3-112">Folders</span></span> 
- <span data-ttu-id="0ede3-113">Extensions des fichiers</span><span class="sxs-lookup"><span data-stu-id="0ede3-113">Extensions of the files</span></span>
- <span data-ttu-id="0ede3-114">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="0ede3-114">File names</span></span>


<span data-ttu-id="0ede3-115">**Dossiers**</span><span class="sxs-lookup"><span data-stu-id="0ede3-115">**Folders**</span></span><br>
<span data-ttu-id="0ede3-116">Vous pouvez spécifier un dossier et ses sous-dossiers à ignorer.</span><span class="sxs-lookup"><span data-stu-id="0ede3-116">You can specify a folder and its subfolders to be skipped.</span></span> 


>[!NOTE]
><span data-ttu-id="0ede3-117">Pour l’instant, l’utilisation de caractères wild cards comme moyen d’exclure des fichiers sous un répertoire n’est pas encore prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ede3-117">At this time, use of wild cards as a way to exclude files under a directory is not yet supported.</span></span> 


<span data-ttu-id="0ede3-118">**Extensions**</span><span class="sxs-lookup"><span data-stu-id="0ede3-118">**Extensions**</span></span><br>
<span data-ttu-id="0ede3-119">Vous pouvez spécifier les extensions à exclure dans un répertoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ede3-119">You can specify the extensions to exclude in a specific directory.</span></span> <span data-ttu-id="0ede3-120">Les extensions sont un moyen d’empêcher un attaquant d’utiliser un dossier exclu pour masquer une attaque.</span><span class="sxs-lookup"><span data-stu-id="0ede3-120">The extensions are a way to prevent an attacker from using an excluded folder to hide an exploit.</span></span> <span data-ttu-id="0ede3-121">Les extensions définissent explicitement les fichiers à ignorer.</span><span class="sxs-lookup"><span data-stu-id="0ede3-121">The extensions explicitly define which files to ignore.</span></span> 

<span data-ttu-id="0ede3-122">**Noms de fichiers**</span><span class="sxs-lookup"><span data-stu-id="0ede3-122">**File names**</span></span><br>
<span data-ttu-id="0ede3-123">Vous pouvez spécifier les noms de fichiers que vous souhaitez exclure dans un répertoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="0ede3-123">You can specify the file names that you want to be excluded in a specific directory.</span></span> <span data-ttu-id="0ede3-124">Les noms sont un moyen d’empêcher un attaquant d’utiliser un dossier exclu pour masquer une attaque.</span><span class="sxs-lookup"><span data-stu-id="0ede3-124">The names are a way to prevent an attacker from using an excluded folder to hide an exploit.</span></span> <span data-ttu-id="0ede3-125">Les noms définissent explicitement les fichiers à ignorer.</span><span class="sxs-lookup"><span data-stu-id="0ede3-125">The names explicitly define which files to ignore.</span></span> 



## <a name="add-an-automation-folder-exclusion"></a><span data-ttu-id="0ede3-126">Ajouter une exclusion de dossier d’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ede3-126">Add an automation folder exclusion</span></span>
1. <span data-ttu-id="0ede3-127">Dans le volet de navigation, sélectionnez **Exclusions** du dossier Settings  >  **Automation.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-127">In the navigation pane, select **Settings** > **Automation folder exclusions**.</span></span>  

2. <span data-ttu-id="0ede3-128">Cliquez **sur Exclusion de nouveau dossier.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-128">Click **New folder exclusion**.</span></span>  

3. <span data-ttu-id="0ede3-129">Entrez les détails du dossier :</span><span class="sxs-lookup"><span data-stu-id="0ede3-129">Enter the folder details:</span></span>

    - <span data-ttu-id="0ede3-130">Folder</span><span class="sxs-lookup"><span data-stu-id="0ede3-130">Folder</span></span>
    - <span data-ttu-id="0ede3-131">Extensions</span><span class="sxs-lookup"><span data-stu-id="0ede3-131">Extensions</span></span>
    - <span data-ttu-id="0ede3-132">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="0ede3-132">File names</span></span>
    - <span data-ttu-id="0ede3-133">Description</span><span class="sxs-lookup"><span data-stu-id="0ede3-133">Description</span></span>
    

4. <span data-ttu-id="0ede3-134">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0ede3-134">Click **Save**.</span></span>

>[!NOTE]
> <span data-ttu-id="0ede3-135">Les commandes Live Response pour collecter ou examiner les fichiers exclus échouent avec l’erreur : « Le fichier est exclu ».</span><span class="sxs-lookup"><span data-stu-id="0ede3-135">Live Response commands to collect or examine excluded files will fail with error: "File is excluded".</span></span> <span data-ttu-id="0ede3-136">En outre, les examens automatisés ignorent les éléments exclus.</span><span class="sxs-lookup"><span data-stu-id="0ede3-136">In addition, automated investigations will ignore the excluded items.</span></span>

## <a name="edit-an-automation-folder-exclusion"></a><span data-ttu-id="0ede3-137">Modifier une exclusion de dossier d’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ede3-137">Edit an automation folder exclusion</span></span> 
1. <span data-ttu-id="0ede3-138">Dans le volet de navigation, sélectionnez **Exclusions** du dossier Settings  >  **Automation.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-138">In the navigation pane, select **Settings** > **Automation folder exclusions**.</span></span> 

2. <span data-ttu-id="0ede3-139">Cliquez **sur Modifier** sur l’exclusion de dossier.</span><span class="sxs-lookup"><span data-stu-id="0ede3-139">Click **Edit** on the folder exclusion.</span></span>  

3. <span data-ttu-id="0ede3-140">Mettez à jour les détails de la règle et cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-140">Update the details of the rule and click **Save**.</span></span>

## <a name="remove-an-automation-folder-exclusion"></a><span data-ttu-id="0ede3-141">Supprimer une exclusion de dossier d’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ede3-141">Remove an automation folder exclusion</span></span> 
1. <span data-ttu-id="0ede3-142">Dans le volet de navigation, sélectionnez **Exclusions** du dossier Settings  >  **Automation.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-142">In the navigation pane, select **Settings** > **Automation folder exclusions**.</span></span>  
2. <span data-ttu-id="0ede3-143">Cliquez sur **Supprimer l’exclusion.**</span><span class="sxs-lookup"><span data-stu-id="0ede3-143">Click **Remove exclusion**.</span></span> 


## <a name="related-topics"></a><span data-ttu-id="0ede3-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ede3-144">Related topics</span></span>
- [<span data-ttu-id="0ede3-145">Gérer les listes d’automatisation autorisées/bloquées</span><span class="sxs-lookup"><span data-stu-id="0ede3-145">Manage automation allowed/blocked lists</span></span>](manage-indicators.md)
- [<span data-ttu-id="0ede3-146">Gérer les téléchargements de fichiers d’automatisation</span><span class="sxs-lookup"><span data-stu-id="0ede3-146">Manage automation file uploads</span></span>](manage-automation-file-uploads.md)
