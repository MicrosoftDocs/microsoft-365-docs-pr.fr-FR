---
title: Correction d’erreur lors du traitement des données
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 02fa8870d6edb4e1a6616604ee0e98638b217237
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079365"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="a2785-102">Correction d’erreur lors du traitement des données</span><span class="sxs-lookup"><span data-stu-id="a2785-102">Error remediation when processing data</span></span>

<span data-ttu-id="a2785-103">La correction des erreurs permet aux administrateurs eDiscovery de rectifier les problèmes de données qui empêchent la découverte électronique avancée de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="a2785-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="a2785-104">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car les fichiers sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="a2785-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="a2785-105">À l’aide de la correction des erreurs, les administrateurs eDiscovery peuvent télécharger des fichiers avec de telles erreurs, supprimer la protection par mot de passe, puis télécharger les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="a2785-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="a2785-106">Utilisez le flux de travail suivant pour corriger les fichiers avec des erreurs dans les cas avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="a2785-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="a2785-107">Créer une session d’erreur de correction pour corriger les fichiers avec des erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="a2785-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="a2785-108">Si l’Assistant de correction d’erreur est fermé à tout moment au cours de la procédure suivante, vous pouvez revenir à la session de correction d’erreur à partir de l’onglet **traitement** en sélectionnant **corrections** dans le menu déroulant **vue** .</span><span class="sxs-lookup"><span data-stu-id="a2785-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Remediations** in the **View** drop-down menu.</span></span>

1. <span data-ttu-id="a2785-109">Sous l’onglet **traitement** dans le cas avancé eDiscovery, sélectionnez **Erreurs** dans le menu déroulant **affichage** , puis sélectionnez un jeu de révision ou l’ensemble de la casse dans le menu déroulant **étendue** .</span><span class="sxs-lookup"><span data-stu-id="a2785-109">On the **Processing** tab in the Advanced eDiscovery case, select **Errors** in the **View** drop-down menu and then select a review set or the entire case in the **Scope** drop-down menu.</span></span> <span data-ttu-id="a2785-110">Cette section affiche toutes les erreurs provenant du cas ou de l’erreur d’un jeu de réexamen spécifique.</span><span class="sxs-lookup"><span data-stu-id="a2785-110">This section displays all errors from the case or error from a specific review set.</span></span>

   ![Correction des erreurs](media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

2. <span data-ttu-id="a2785-112">Sélectionnez les erreurs que vous souhaitez corriger en cliquant sur la case d’option en regard du type d’erreur ou du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="a2785-112">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="a2785-113">Dans l’exemple suivant, nous effectuons la correction d’un fichier protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a2785-113">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="a2785-114">Cliquez sur **nouvelle erreur de correction**.</span><span class="sxs-lookup"><span data-stu-id="a2785-114">Click **New error remediation**.</span></span>

    <span data-ttu-id="a2785-115">Le flux de travail de correction d’erreur commence par une phase de préparation où les fichiers contenant des erreurs sont copiés vers un emplacement de stockage Azure fourni par Microsoft afin que vous puissiez les télécharger sur votre ordinateur local pour résoudre les problèmes.</span><span class="sxs-lookup"><span data-stu-id="a2785-115">The error remediation workflow starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Préparation de la correction des erreurs](media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="a2785-117">Une fois la préparation terminée, cliquez sur **suivant : Télécharger les fichiers** pour continuer le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a2785-117">After the preparation is complete, click **Next: Download files** to proceed with download.</span></span>

    ![Télécharger des fichiers](media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="a2785-119">Pour télécharger des fichiers, spécifiez le **chemin de destination pour le téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="a2785-119">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="a2785-120">Il s’agit d’un chemin d’accès au dossier parent sur votre ordinateur local où le fichier sera téléchargé.</span><span class="sxs-lookup"><span data-stu-id="a2785-120">This is a path to the parent folder on your local computer where the file will be downloaded.</span></span>  <span data-ttu-id="a2785-121">Le chemin d’accès par défaut,%USERPROFILE%\Downloads\errors, pointe vers le dossier downloads de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="a2785-121">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="a2785-122">Vous pouvez modifier ce chemin si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="a2785-122">You can change this path if desired.</span></span> <span data-ttu-id="a2785-123">Si vous le modifiez, nous vous recommandons d’utiliser un chemin d’accès local pour obtenir les meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="a2785-123">If you do change it, we recommend that you use a local file path for the best performance.</span></span> <span data-ttu-id="a2785-124">N’utilisez pas de chemin d’accès réseau distant.</span><span class="sxs-lookup"><span data-stu-id="a2785-124">Don't use a remote network path.</span></span> <span data-ttu-id="a2785-125">Par exemple, vous pouvez utiliser le chemin d’accès **C:\Remediation**.</span><span class="sxs-lookup"><span data-stu-id="a2785-125">For example, you could use the path **C:\Remediation**.</span></span> 

   <span data-ttu-id="a2785-126">Le chemin d’accès au dossier parent est automatiquement ajouté à la commande AzCopy (en tant que valeur du paramètre **/dest** ).</span><span class="sxs-lookup"><span data-stu-id="a2785-126">The path to the parent folder is automatically added to AzCopy command (as the value of the **/Dest** parameter).</span></span>

6. <span data-ttu-id="a2785-127">Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="a2785-127">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="a2785-128">Ouvrez une invite de commandes Windows, collez la commande AzCopy, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="a2785-128">Open a Windows Command Prompt, paste the AzCopy command, and then press **Enter**.</span></span>  

    ![Préparer la correction des erreurs](media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)    

    > [!NOTE]
    > <span data-ttu-id="a2785-130">Vous devez utiliser AzCopy v 8.1 pour utiliser la commande fournie sur la page Télécharger les **fichiers** .</span><span class="sxs-lookup"><span data-stu-id="a2785-130">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="a2785-131">Vous devez également utiliser AzCopy v 8.1 pour télécharger les fichiers à l’étape 10.</span><span class="sxs-lookup"><span data-stu-id="a2785-131">You also must use AzCopy v8.1 to upload the files in step 10.</span></span> <span data-ttu-id="a2785-132">Pour installer cette version de AzCopy, consultez [la rubrique transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="a2785-132">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="a2785-133">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="a2785-133">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

    <span data-ttu-id="a2785-134">Les fichiers que vous avez sélectionnés sont téléchargés à l’emplacement que vous avez spécifié à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="a2785-134">The files that you selected are downloaded to the location that you specified in step 5.</span></span> <span data-ttu-id="a2785-135">Dans le dossier parent (par exemple, **C:\Remediation**), la structure de sous-dossiers suivante est créée automatiquement :</span><span class="sxs-lookup"><span data-stu-id="a2785-135">In the parent folder (for example, **C:\Remediation**), the following subfolder structure is automatically created:</span></span>

    `<Parent folder>\Subfolder 1\Subfolder 2\<file>`

    - <span data-ttu-id="a2785-136">Le *sous-dossier 1* est nommé avec l’ID du cas ou de l’ensemble de révision, en fonction de l’étendue que vous avez sélectionnée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="a2785-136">*Subfolder 1* is named with the ID for the case or the review set, depending on the scope that you selected in step 1.</span></span>

    - <span data-ttu-id="a2785-137">Le *sous-dossier 2* est nommé avec l’ID de fichier du fichier téléchargé</span><span class="sxs-lookup"><span data-stu-id="a2785-137">*Subfolder 2* is named with the file ID of the downloaded file</span></span>

    - <span data-ttu-id="a2785-138">Le fichier téléchargé se trouve dans le *sous-dossier 2* et est également nommé avec l’ID de fichier.</span><span class="sxs-lookup"><span data-stu-id="a2785-138">The downloaded file is located in *Subfolder 2* and is also named with the file ID.</span></span>

    <span data-ttu-id="a2785-139">Voici un exemple de chemin d’accès de dossier et de nom de fichier d’erreur qui est créé lorsque des éléments sont téléchargés dans le dossier parent **C:\Remediation** :</span><span class="sxs-lookup"><span data-stu-id="a2785-139">Here's an example of the folder path and error file name that's created when items are downloaded to the **C:\Remediation** parent folder:</span></span>

    `C:\Remediation\232f8b7e-089c-4781-88c6-210da0615d32\d1459499146268a096ea20202cd029857d64087706e6d6ca2a224970ae3b8938\d1459499146268a096ea20202cd029857d64087706e6d6ca2a224970ae3b8938.docx`

    <span data-ttu-id="a2785-140">Si plusieurs fichiers sont téléchargés, chacun d’entre eux est téléchargé dans un sous-dossier nommé avec l’ID de fichier.</span><span class="sxs-lookup"><span data-stu-id="a2785-140">If multiple files are downloaded, each one is downloaded to a subfolder that's named with the file ID.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a2785-141">Lorsque vous chargez des fichiers à l’étape 9 et à l’étape 10, les fichiers corrigés doivent avoir le même nom de fichier et se trouver dans la même structure de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="a2785-141">When you upload files in step 9 and step 10, the remediated files must have that same filename and be located in the same subfolder structure.</span></span> <span data-ttu-id="a2785-142">Les noms de fichier et de sous-dossier sont utilisés pour associer le fichier corrigé au fichier d’erreur d’origine.</span><span class="sxs-lookup"><span data-stu-id="a2785-142">The subfolder and file names are used to associated the remediated file with the original error file.</span></span> <span data-ttu-id="a2785-143">Si la structure de dossiers ou les noms de fichiers sont modifiés, vous recevez l’erreur `Cannot apply Error Remediation to the current Workingset`suivante :.</span><span class="sxs-lookup"><span data-stu-id="a2785-143">If the folder structure or file names are changed, you'll receive the following error: `Cannot apply Error Remediation to the current Workingset`.</span></span> <span data-ttu-id="a2785-144">Pour éviter tout problème, nous vous recommandons de conserver les fichiers corrigés dans le même dossier parent et la même structure de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="a2785-144">To prevent any issues, we recommend that keep the remediated files in the same parent folder and subfolder structure.</span></span>

7. <span data-ttu-id="a2785-145">Après avoir téléchargé les fichiers, vous pouvez les corriger à l’aide d’un outil approprié.</span><span class="sxs-lookup"><span data-stu-id="a2785-145">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="a2785-146">Pour les fichiers protégés par mot de passe, il existe plusieurs outils de craquage de mot de passe que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2785-146">For password-protected files, there are several password cracking tools you can use.</span></span> <span data-ttu-id="a2785-147">Si vous connaissiez les mots de passe des fichiers, vous pouvez les ouvrir et supprimer la protection par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a2785-147">If you know the passwords for the files, you can open them and remove the password protection.</span></span>

8. <span data-ttu-id="a2785-148">Revenez à Advanced eDiscovery et à l’Assistant de correction des erreurs, puis cliquez sur **suivant : charger les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="a2785-148">Return to Advanced eDiscovery and the error remediation wizard and then click **Next: Upload files**.</span></span>  <span data-ttu-id="a2785-149">Cette action passe à la page suivante, dans laquelle vous pouvez à présent télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2785-149">This moves to the next page where you can now upload the files.</span></span>

    ![Charger des fichiers](media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="a2785-151">Spécifiez le dossier parent dans lequel se trouvent les fichiers corrigés dans la zone **de texte chemin d’accès à l’emplacement des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="a2785-151">Specify the parent folder where the remediated files are located in the **Path to location of files** text box.</span></span> <span data-ttu-id="a2785-152">Une fois encore, le dossier parent doit avoir la même structure de sous-dossiers que celle qui a été créée lorsque vous avez téléchargé les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2785-152">Again, the parent folder must have the same subfolder structure that was created when you downloaded the files.</span></span>

    <span data-ttu-id="a2785-153">Le chemin d’accès au dossier parent est automatiquement ajouté à la commande AzCopy (en tant que valeur du paramètre **/source** ).</span><span class="sxs-lookup"><span data-stu-id="a2785-153">The path to the parent folder is automatically added to AzCopy command (as the value of the **/Source** parameter).</span></span>

10. <span data-ttu-id="a2785-154">Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="a2785-154">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="a2785-155">Ouvrez une invite de commandes Windows, collez la commande AzCopy, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="a2785-155">Open a Windows Command Prompt, paste the AzCopy command, and then press **Enter**.</span></span> <span data-ttu-id="a2785-156">Téléchargez les fichiers.</span><span class="sxs-lookup"><span data-stu-id="a2785-156">upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="a2785-158">Après avoir exécuté la commande AzCopy, cliquez sur **suivant : process files**.</span><span class="sxs-lookup"><span data-stu-id="a2785-158">After you run the AzCopy command, click **Next: Process files**.</span></span>

    <span data-ttu-id="a2785-159">Une fois le traitement terminé, vous pouvez accéder à la vue d’ensemble et afficher les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="a2785-159">When processing is complete, you can go to review set and view the remediated files.</span></span> 

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="a2785-160">Que se passe-t-il lorsque les fichiers sont convertis ?</span><span class="sxs-lookup"><span data-stu-id="a2785-160">What happens when files are remediated</span></span>

<span data-ttu-id="a2785-161">Lorsque les fichiers résolus sont téléchargés, les métadonnées d’origine sont conservées, à l’exception des champs suivants :</span><span class="sxs-lookup"><span data-stu-id="a2785-161">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="a2785-162">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="a2785-162">ExtractedTextSize</span></span>
- <span data-ttu-id="a2785-163">HasText</span><span class="sxs-lookup"><span data-stu-id="a2785-163">HasText</span></span>
- <span data-ttu-id="a2785-164">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="a2785-164">IsErrorRemediate</span></span>
- <span data-ttu-id="a2785-165">LoadId</span><span class="sxs-lookup"><span data-stu-id="a2785-165">LoadId</span></span>
- <span data-ttu-id="a2785-166">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="a2785-166">ProcessingErrorMessage</span></span>
- <span data-ttu-id="a2785-167">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="a2785-167">ProcessingStatus</span></span>
- <span data-ttu-id="a2785-168">Texte</span><span class="sxs-lookup"><span data-stu-id="a2785-168">Text</span></span>
- <span data-ttu-id="a2785-169">WordCount</span><span class="sxs-lookup"><span data-stu-id="a2785-169">WordCount</span></span>
- <span data-ttu-id="a2785-170">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="a2785-170">WorkingsetId</span></span>

<span data-ttu-id="a2785-171">Pour obtenir une définition de tous les champs de métadonnées dans Advanced eDiscovery, consultez la rubrique [document Metadata Fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="a2785-171">For a definition of all metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
