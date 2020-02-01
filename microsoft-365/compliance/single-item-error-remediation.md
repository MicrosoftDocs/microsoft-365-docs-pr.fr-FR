---
title: Correction d’erreur sur élément unique
f1.keywords:
- NOCSH
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
description: Vous pouvez corriger une erreur de traitement dans un document dans un jeu de réexamen dans Advanced eDiscovery sans avoir à suivre le processus de correction des erreurs en bloc.
ms.openlocfilehash: c049ce4b5d3f8fc12a015a61ea927b744ae76eb3
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41601491"
---
# <a name="single-item-error-remediation"></a><span data-ttu-id="249be-103">Correction d’erreur sur élément unique</span><span class="sxs-lookup"><span data-stu-id="249be-103">Single item error remediation</span></span>

<span data-ttu-id="249be-104">La correction des erreurs permet aux utilisateurs avancés de eDiscovery de corriger les problèmes de données qui empêchent Advanced eDiscovery de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="249be-104">Error remediation gives Advanced eDiscovery users the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="249be-105">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traités car ils sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="249be-105">For example, files that are password protected can't be processed because those files are locked or encrypted.</span></span> <span data-ttu-id="249be-106">Auparavant, vous pouviez uniquement corriger les erreurs en bloc à l’aide de [ce flux de travail](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="249be-106">Previously, you could only remediate errors in bulk by using [this workflow](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span></span> <span data-ttu-id="249be-107">Toutefois, il n’est pas judicieux de corriger les erreurs dans plusieurs fichiers lorsque vous ne savez pas si un de ces fichiers répond au cas que vous êtes en train d’examiner.</span><span class="sxs-lookup"><span data-stu-id="249be-107">But sometimes, it doesn't make sense to remediate errors in multiple files when you’re unsure if any of those files are responsive to the case you’re investigating.</span></span> <span data-ttu-id="249be-108">Il n’est pas non plus judicieux de corriger les erreurs avant que vous n’ayez eu le temps de passer en revue les métadonnées de fichier (telles que l’emplacement des fichiers ou les personnes ayant accès) pour vous aider à prendre des décisions optimales concernant la réactivité.</span><span class="sxs-lookup"><span data-stu-id="249be-108">It also might not make sense to remediate errors before you’ve had a chance to review the file metadata (such as file location or who had access) to help you make up-front decisions about responsiveness.</span></span> <span data-ttu-id="249be-109">Une nouvelle fonctionnalité appelée *Single Item Error* revisions donne aux gestionnaires de découverte électronique la possibilité d’afficher les métadonnées des fichiers avec une erreur de traitement et, si nécessaire, de corriger directement l’erreur dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-109">A new feature called *single item error remediation* gives eDiscovery managers the ability to view the metadata of files with a processing error and if necessary remediate the error directly in the review set.</span></span> <span data-ttu-id="249be-110">Cet article explique comment identifier, ignorer et corriger les fichiers avec des erreurs de traitement dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-110">The article discusses how to identify, ignore, and remediate files with processing errors in a review set.</span></span>

## <a name="identify-documents-with-errors"></a><span data-ttu-id="249be-111">Identifier les documents contenant des erreurs</span><span class="sxs-lookup"><span data-stu-id="249be-111">Identify documents with errors</span></span>

<span data-ttu-id="249be-112">Les documents contenant des erreurs de traitement dans un ensemble de révision sont maintenant identifiés (avec une bannière).</span><span class="sxs-lookup"><span data-stu-id="249be-112">Documents with processing errors in a review set are now identified (with a banner).</span></span> <span data-ttu-id="249be-113">Vous pouvez corriger ou ignorer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="249be-113">You can remediate or ignore the error.</span></span> <span data-ttu-id="249be-114">La capture d’écran suivante montre la bannière d’erreur de traitement pour un document Word dans un jeu de révision protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="249be-114">The following screenshot shows the processing error banner for a Word document in a review set that is password-protected.</span></span> <span data-ttu-id="249be-115">Notez également que vous pouvez afficher les métadonnées de fichier des documents contenant des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="249be-115">Also notice that you can view the file metadata of documents with processing errors.</span></span>

![Bannière affichée pour le document avec une erreur de traitement](media/SIERimage1.png)

<span data-ttu-id="249be-117">Vous pouvez également rechercher des documents qui contiennent des erreurs de traitement à l’aide de la condition **État de traitement** lors [de l’interrogation des documents dans un jeu de révision](review-set-search.md).</span><span class="sxs-lookup"><span data-stu-id="249be-117">You can also search for documents that have processing errors by using the **Processing status** condition when [querying the documents in a review set](review-set-search.md).</span></span>

![Utiliser la condition d’état de traitement pour rechercher des documents d’erreur](media/SIERimage2.png)

### <a name="ignore-errors"></a><span data-ttu-id="249be-119">Ignorer les erreurs</span><span class="sxs-lookup"><span data-stu-id="249be-119">Ignore errors</span></span>

<span data-ttu-id="249be-120">Vous pouvez ignorer une erreur de traitement en cliquant sur **Ignorer** dans la bannière traitement des erreurs.</span><span class="sxs-lookup"><span data-stu-id="249be-120">You can ignore a processing error by clicking **Ignore** in the processing error banner.</span></span> <span data-ttu-id="249be-121">Lorsque vous ignorez une erreur, le document est supprimé du [flux de travail de correction des erreurs en bloc](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="249be-121">When you ignore an error, the document is removed from the [bulk error remediation workflow](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span></span> <span data-ttu-id="249be-122">Lorsqu’une erreur est ignorée, la bannière de document change de couleur et indique que l’erreur de traitement a été ignorée.</span><span class="sxs-lookup"><span data-stu-id="249be-122">After an error is ignored, the document banner changes color and indicates that the processing error was ignored.</span></span> <span data-ttu-id="249be-123">À tout moment, vous pouvez annuler la décision pour ignorer l’erreur en cliquant sur **rétablir**.</span><span class="sxs-lookup"><span data-stu-id="249be-123">At any time, you can revert the decision to ignore the error by clicking **Revert**.</span></span>

![Cliquez sur Ignorer pour ignorer l’erreur de traitement](media/SIERimage3.png)

<span data-ttu-id="249be-125">Vous pouvez également rechercher tous les documents contenant une erreur de traitement qui a été ignoré à l’aide de la condition *Erreurs de traitement ignorées* lors de l’interrogation des documents dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-125">You can also search for all documents that had a processing error that was ignored by using the *Ignored processing errors* condition when querying documents in a review set.</span></span>

![Utiliser la condition erreurs de traitement ignorées pour rechercher des documents d’erreur ignorés](media/SIERimage4.png)

## <a name="remediate-a-document-with-errors"></a><span data-ttu-id="249be-127">Correction d’un document avec des erreurs</span><span class="sxs-lookup"><span data-stu-id="249be-127">Remediate a document with errors</span></span>

<span data-ttu-id="249be-128">Parfois, vous pouvez être amené à corriger une erreur de traitement dans les documents (en supprimant un mot de passe, en déchiffrant un fichier chiffré ou en récupérant un document endommagé), puis en ajoutant le document corrigé à l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-128">Sometimes you may be required to remediate a processing error in documents (by removing a password, decrypting an encrypted file, or recovering a corrupted document) and then add the remediated document to the review set.</span></span> <span data-ttu-id="249be-129">Cela vous permet de passer en revue et d’exporter le document d’erreur avec les autres documents de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-129">This allows you to review and export the error document together with the other documents in the review set.</span></span> 

<span data-ttu-id="249be-130">Pour corriger un document unique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="249be-130">To remediate a single document, follow these steps:</span></span>

1. <span data-ttu-id="249be-131">Cliquez sur **Télécharger** > l'**original téléchargement** pour télécharger une copie du fichier sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="249be-131">Click **Download** > **Download original** to download a copy of the file to a local computer.</span></span>

   ![Télécharger le document avec l’erreur de traitement](media/SIERimage5.png)

2. <span data-ttu-id="249be-133">Corrigez l’erreur dans le fichier en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="249be-133">Remediate the error in the file offline.</span></span> <span data-ttu-id="249be-134">Pour les fichiers chiffrés, qui nécessitent un logiciel de déchiffrement, pour supprimer la protection par mot de passe, fournissez le mot de passe et enregistrez le fichier ou utilisez un cracker de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="249be-134">For encrypted files, that would require decryption software, to remove password protection, either provide the password and save the file or use a password cracker.</span></span> <span data-ttu-id="249be-135">Une fois le fichier résolu, passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="249be-135">After you remediate the file, go to the next step.</span></span>

3. <span data-ttu-id="249be-136">Dans l’ensemble de révision, sélectionnez le fichier avec l’erreur de traitement que vous avez corrigée, puis cliquez sur **Correction**.</span><span class="sxs-lookup"><span data-stu-id="249be-136">In the review set, select the file with the processing error that you remediated, and then  click **Remediation**.</span></span>

   ![Cliquez sur correction dans la bannière du document avec une erreur de traitement.](media/SIERimage6.png)


4. <span data-ttu-id="249be-138">Cliquez sur **Parcourir**, accédez à l’emplacement du fichier corrigé sur votre ordinateur local, puis sélectionnez le fichier.</span><span class="sxs-lookup"><span data-stu-id="249be-138">Click **Browse**, go to the location of the remediated file on your local computer, and then select the file.</span></span>

   ![Cliquez sur Parcourir et sélectionnez le fichier corrigé sur votre ordinateur local.](media/SIERimage7.png)

    <span data-ttu-id="249be-140">Après avoir sélectionné le fichier corrigé, il est automatiquement téléchargé vers l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-140">After selecting the remediated file, it is automatically uploaded to the review set.</span></span> <span data-ttu-id="249be-141">Vous pouvez suivre l’état de traitement du fichier.</span><span class="sxs-lookup"><span data-stu-id="249be-141">You can track the processing status of the file.</span></span>

    ![L’état du processus de correction est affiché.](media/SIERimage8.png)

   <span data-ttu-id="249be-143">Une fois le traitement terminé, vous pouvez afficher le document corrigé.</span><span class="sxs-lookup"><span data-stu-id="249be-143">After processing is completed, you can view the remediated document.</span></span>

    ![Vous pouvez afficher le fichier corrigé dans le format natif dans l’ensemble de révision](media/SIERimage9.png)

<span data-ttu-id="249be-145">Pour plus d’informations sur ce qui se produit lorsqu’un document est résolu, voir [ce qui se passe lorsque les fichiers sont corrigés](error-remediation.md#what-happens-when-files-are-remediated).</span><span class="sxs-lookup"><span data-stu-id="249be-145">For more information about what happens when a document is remediated, see [What happens when files are remediated](error-remediation.md#what-happens-when-files-are-remediated).</span></span>

## <a name="search-for-remediated-documents"></a><span data-ttu-id="249be-146">Rechercher des documents résolus</span><span class="sxs-lookup"><span data-stu-id="249be-146">Search for remediated documents</span></span>

<span data-ttu-id="249be-147">Vous pouvez rechercher tous les documents dans un jeu de révision qui ont été résolus à l’aide de la condition **Keywords** et en spécifiant la paire propriété : valeur suivante : **IsFromErrorRemediation : true**.</span><span class="sxs-lookup"><span data-stu-id="249be-147">You can search for all documents in a review set that were remediated by using the **Keywords** condition and specifying the following property:value pair: **IsFromErrorRemediation:true**.</span></span> <span data-ttu-id="249be-148">Cette propriété est également disponible dans le fichier d’exportation de la charge lorsque vous exportez des documents à partir d’un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="249be-148">This property is also available in the export load file when you export documents from a review set.</span></span>
