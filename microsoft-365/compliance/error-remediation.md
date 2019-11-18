---
title: Erreur de correction lors du traitement des données pour une enquête
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
ms.openlocfilehash: c7bc6043722059b04d7fb99663a7dfb8815de697
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38685773"
---
# <a name="error-remediation-when-processing-data-for-an-investigation"></a><span data-ttu-id="ff9e3-102">Erreur de correction lors du traitement des données pour une enquête</span><span class="sxs-lookup"><span data-stu-id="ff9e3-102">Error remediation when processing data for an investigation</span></span>

<span data-ttu-id="ff9e3-103">La correction des erreurs permet aux investigateurs de corriger les problèmes de données qui empêchent les enquêtes de données (préversion) de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-103">Error remediation allows investigators the ability to rectify data issues that prevent Data Investigations (Preview) from properly processing the content.</span></span> <span data-ttu-id="ff9e3-104">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car les fichiers sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-104">For example, files that are password protected cannot be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="ff9e3-105">À l’aide de la correction des erreurs, les investigateurs peuvent télécharger des fichiers avec de telles erreurs, supprimer la protection par mot de passe et télécharger les fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-105">Using error remediation, investigators can download files with such errors, remove the password protection, and upload the remediated files.</span></span>

<span data-ttu-id="ff9e3-106">Utilisez le flux de travail suivant pour corriger les fichiers avec des erreurs dans les cas d’examens de données (aperçu).</span><span class="sxs-lookup"><span data-stu-id="ff9e3-106">Use the following workflow to remediate files with errors in Data Investigations (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="ff9e3-107">Création d’une session de correction d’erreur pour corriger les fichiers avec des erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="ff9e3-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="ff9e3-108">Si l’Assistant de correction d’erreur est fermé à tout moment au cours de la procédure suivante, vous pouvez revenir à la session d’erreur de correction à partir de l’onglet **traitement** en sélectionnant **erreur correction** dans le menu déroulant **vue** .</span><span class="sxs-lookup"><span data-stu-id="ff9e3-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="ff9e3-109">Sous l’onglet **traitement** d’une enquête de données, sélectionnez **Erreurs** dans le menu déroulant **affichage** .</span><span class="sxs-lookup"><span data-stu-id="ff9e3-109">On the **Processing** tab in a data investigation, select **Errors** in the **View** dropdown menu.</span></span>

2. <span data-ttu-id="ff9e3-110">Sélectionnez les erreurs que vous souhaitez corriger en cliquant sur la case d’option en regard du type d’erreur ou du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="ff9e3-111">Dans l’exemple suivant, nous effectuons la correction d’un fichier protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="ff9e3-112">Cliquez sur **+ nouvelle erreur de correction**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-112">Click **+ New error remediation**.</span></span>

    ![Correction des erreurs](media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="ff9e3-114">La session de correction d’erreur commence avec une phase de préparation dans laquelle les fichiers contenant des erreurs sont copiés vers un emplacement Azure sécurisé afin qu’ils puissent être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-114">The error remediation session begins, starting with a preparation stage where the files with errors are copied to a secure Azure location so that they can be downloaded.</span></span>

    ![Préparation de la correction des erreurs](media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="ff9e3-116">Une fois la préparation terminée, cliquez sur **suivant : Télécharger les fichiers** pour continuer le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Télécharger des fichiers](media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="ff9e3-118">Pour télécharger des fichiers, spécifiez le **chemin de destination pour le téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="ff9e3-119">Il s’agit d’un chemin d’accès sur votre ordinateur local où le fichier doit être téléchargé.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-119">This is a path on your local computer where the file should be downloaded.</span></span>  <span data-ttu-id="ff9e3-120">Le chemin d’accès par défaut,%USERPROFILE%\Downloads\errors, pointe vers le dossier downloads de l’utilisateur connecté ; Cela peut être modifié selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="ff9e3-121">Nous vous recommandons d’utiliser un chemin d’accès local au lieu d’un chemin d’accès réseau distant pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-121">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff9e3-122">Si vous n’avez pas installé AzCopy, vous pouvez l’installer à partir de cet emplacement :https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="ff9e3-122">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="ff9e3-123">Copiez la commande prédéfinie en cliquant sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-123">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="ff9e3-124">Démarrez une invite de commandes Windows, collez la commande, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-124">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="ff9e3-125">Les fichiers sont téléchargés.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-125">The files will be downloaded.</span></span>

    ![Préparation de la correction des erreurs](media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="ff9e3-127">Si vous rencontrez des problèmes lors de l’exécution de cette commande, consultez la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="ff9e3-127">If you have issues running this command, see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="ff9e3-128">Après avoir téléchargé les fichiers, vous pouvez les corriger à l’aide d’un outil approprié.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-128">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="ff9e3-129">Pour les fichiers protégés par mot de passe, il existe plusieurs outils de craquage de mot de passe que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-129">For password protected files, there are several password cracking tools you can use.</span></span> <span data-ttu-id="ff9e3-130">Si vous connaissiez les mots de passe des fichiers, vous pouvez les ouvrir et supprimer la protection par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-130">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    
   > [!NOTE]
    > <span data-ttu-id="ff9e3-131">Il est important de conserver la structure de répertoire et les noms de fichier des fichiers corrigés.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-131">It's important that you retain the directory structure and file names of the remediated files.</span></span> <span data-ttu-id="ff9e3-132">Les noms de chemin d’accès des fichiers et dossiers téléchargés permettent d’associer les fichiers corrigés aux fichiers d’origine.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-132">The path names of the downloaded files and folders make it possible to associate the remediated files with the original files.</span></span>  <span data-ttu-id="ff9e3-133">Si la structure du répertoire ou les noms de fichier sont modifiés, vous recevez l’erreur `Cannot apply Error Remediation to the current Evidenceset`suivante :.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-133">If the directory structure or file names are changed, you'll receive the following error: `Cannot apply Error Remediation to the current Evidenceset`.</span></span>

8. <span data-ttu-id="ff9e3-134">À présent, revenez aux enquêtes de données (aperçu) et cliquez sur **suivant : charger les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-134">Now, return to Data Investigations (Preview) and click **Next: Upload files**.</span></span>  <span data-ttu-id="ff9e3-135">Cette opération passe à l’étape suivante, dans laquelle vous pouvez à présent télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-135">This will move to the next step where you can now upload the files.</span></span>

    ![Charger des fichiers](media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="ff9e3-137">Spécifiez l’emplacement des fichiers corrigés dans la zone **de texte chemin d’accès à l’emplacement des fichiers** , puis cliquez sur **copier dans le presse-papiers**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-137">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="ff9e3-138">Collez la commande dans une invite de commande Windows et appuyez sur **entrée** pour charger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-138">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="ff9e3-140">Enfin, revenez aux enquêtes de données (aperçu) et cliquez sur **suivant : traiter les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-140">Finally, return to Data Investigations (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="ff9e3-141">Une fois le traitement terminé.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-141">When processing is complete.</span></span>  <span data-ttu-id="ff9e3-142">Vous pouvez revenir à la plage de travail et voir le fichier corrigé.</span><span class="sxs-lookup"><span data-stu-id="ff9e3-142">You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="ff9e3-143">Que se passe-t-il lorsque les fichiers sont convertis ?</span><span class="sxs-lookup"><span data-stu-id="ff9e3-143">What happens when files are remediated</span></span>

<span data-ttu-id="ff9e3-144">Lorsque les fichiers résolus sont téléchargés, les métadonnées d’origine sont conservées, à l’exception des champs suivants :</span><span class="sxs-lookup"><span data-stu-id="ff9e3-144">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="ff9e3-145">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="ff9e3-145">ExtractedTextSize</span></span>
- <span data-ttu-id="ff9e3-146">HasText</span><span class="sxs-lookup"><span data-stu-id="ff9e3-146">HasText</span></span>
- <span data-ttu-id="ff9e3-147">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="ff9e3-147">IsErrorRemediate</span></span>
- <span data-ttu-id="ff9e3-148">LoadId</span><span class="sxs-lookup"><span data-stu-id="ff9e3-148">LoadId</span></span>
- <span data-ttu-id="ff9e3-149">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ff9e3-149">ProcessingErrorMessage</span></span>
- <span data-ttu-id="ff9e3-150">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="ff9e3-150">ProcessingStatus</span></span>
- <span data-ttu-id="ff9e3-151">Texte</span><span class="sxs-lookup"><span data-stu-id="ff9e3-151">Text</span></span>
- <span data-ttu-id="ff9e3-152">WordCount</span><span class="sxs-lookup"><span data-stu-id="ff9e3-152">WordCount</span></span>
- <span data-ttu-id="ff9e3-153">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="ff9e3-153">WorkingsetId</span></span>

<span data-ttu-id="ff9e3-154">Pour obtenir une définition de tous les champs de métadonnées de document dans les enquêtes de données (aperçu), consultez la rubrique [Field Metadata Fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="ff9e3-154">For a definition of all document metadata fields in Data Investigations (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>