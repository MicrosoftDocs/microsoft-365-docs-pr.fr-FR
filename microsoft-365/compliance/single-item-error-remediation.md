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
description: Vous pouvez corriger une erreur de traitement dans un document dans un jeu à réviser dans Advanced eDiscovery sans avoir à suivre le processus de correction des erreurs en bloc.
ms.openlocfilehash: 8e5d8d00f507dc5792a1beda018d4c76632b82f7
ms.sourcegitcommit: 98b889e674ad1d5fa37d4b6c5fc3eda60a1d67f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/05/2021
ms.locfileid: "49751581"
---
# <a name="single-item-error-remediation-in-advanced-ediscovery"></a><span data-ttu-id="1b89e-103">Correction d’erreur d’élément unique dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1b89e-103">Single item error remediation in Advanced eDiscovery</span></span>

<span data-ttu-id="1b89e-104">La correction d’erreur permet aux utilisateurs d’Advanced eDiscovery de corriger les problèmes de données qui empêchent Advanced eDiscovery de traiter correctement le contenu.</span><span class="sxs-lookup"><span data-stu-id="1b89e-104">Error remediation gives Advanced eDiscovery users the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="1b89e-105">Par exemple, les fichiers protégés par mot de passe ne peuvent pas être traitées, car ces fichiers sont verrouillés ou chiffrés.</span><span class="sxs-lookup"><span data-stu-id="1b89e-105">For example, files that are password protected can't be processed because those files are locked or encrypted.</span></span> <span data-ttu-id="1b89e-106">Auparavant, vous pouviez uniquement corriger les erreurs en bloc à l’aide [de ce flux de travail.](error-remediation-when-processing-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="1b89e-106">Previously, you could only remediate errors in bulk by using [this workflow](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span></span> <span data-ttu-id="1b89e-107">Mais parfois, il n’est pas logique de corriger les erreurs dans plusieurs fichiers lorsque vous ne savez pas si l’un de ces fichiers répond au cas que vous examinez.</span><span class="sxs-lookup"><span data-stu-id="1b89e-107">But sometimes, it doesn't make sense to remediate errors in multiple files when you’re unsure if any of those files are responsive to the case you’re investigating.</span></span> <span data-ttu-id="1b89e-108">Il peut également ne pas être utile de corriger les erreurs avant d’avoir eu la possibilité de passer en revue les métadonnées de fichier (par exemple, l’emplacement du fichier ou les personnes ayant accès) pour vous aider à prendre des décisions à l’avance en matière de réactivité.</span><span class="sxs-lookup"><span data-stu-id="1b89e-108">It also might not make sense to remediate errors before you’ve had a chance to review the file metadata (such as file location or who had access) to help you make up-front decisions about responsiveness.</span></span> <span data-ttu-id="1b89e-109">Une nouvelle  fonctionnalité appelée correction d’erreur d’élément unique permet aux gestionnaires eDiscovery d’afficher les métadonnées des fichiers avec une erreur de traitement et, si nécessaire, de corriger l’erreur directement dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-109">A new feature called *single item error remediation* gives eDiscovery managers the ability to view the metadata of files with a processing error and if necessary remediate the error directly in the review set.</span></span> <span data-ttu-id="1b89e-110">L’article explique comment identifier, ignorer et corriger les fichiers avec des erreurs de traitement dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-110">The article discusses how to identify, ignore, and remediate files with processing errors in a review set.</span></span>

## <a name="identify-documents-with-errors"></a><span data-ttu-id="1b89e-111">Identifier les documents avec des erreurs</span><span class="sxs-lookup"><span data-stu-id="1b89e-111">Identify documents with errors</span></span>

<span data-ttu-id="1b89e-112">Les documents avec des erreurs de traitement dans un jeu à réviser sont désormais identifiés (avec une bannière).</span><span class="sxs-lookup"><span data-stu-id="1b89e-112">Documents with processing errors in a review set are now identified (with a banner).</span></span> <span data-ttu-id="1b89e-113">Vous pouvez corriger ou ignorer l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1b89e-113">You can remediate or ignore the error.</span></span> <span data-ttu-id="1b89e-114">La capture d’écran suivante montre la bannière d’erreur de traitement d’un document Word dans un jeu à réviser protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1b89e-114">The following screenshot shows the processing error banner for a Word document in a review set that is password-protected.</span></span> <span data-ttu-id="1b89e-115">Notez également que vous pouvez afficher les métadonnées de fichier des documents avec des erreurs de traitement.</span><span class="sxs-lookup"><span data-stu-id="1b89e-115">Also notice that you can view the file metadata of documents with processing errors.</span></span>

![Bannière affichée pour le document avec erreur de traitement](../media/SIERimage1.png)

<span data-ttu-id="1b89e-117">Vous pouvez également rechercher des documents qui ont des erreurs de traitement à l’aide de la **condition** d’état de traitement lors de l’interrogation des documents dans un jeu [à réviser.](review-set-search.md)</span><span class="sxs-lookup"><span data-stu-id="1b89e-117">You can also search for documents that have processing errors by using the **Processing status** condition when [querying the documents in a review set](review-set-search.md).</span></span>

![Utiliser la condition d’état de traitement pour rechercher des documents d’erreur](../media/SIERimage2.png)

### <a name="ignore-errors"></a><span data-ttu-id="1b89e-119">Ignorer les erreurs</span><span class="sxs-lookup"><span data-stu-id="1b89e-119">Ignore errors</span></span>

<span data-ttu-id="1b89e-120">Vous pouvez ignorer une erreur de traitement en cliquant sur **Ignorer** dans la bannière d’erreur de traitement.</span><span class="sxs-lookup"><span data-stu-id="1b89e-120">You can ignore a processing error by clicking **Ignore** in the processing error banner.</span></span> <span data-ttu-id="1b89e-121">Lorsque vous ignorez une erreur, le document est supprimé du flux de travail de correction des [erreurs en bloc.](error-remediation-when-processing-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="1b89e-121">When you ignore an error, the document is removed from the [bulk error remediation workflow](error-remediation-when-processing-data-in-advanced-ediscovery.md).</span></span> <span data-ttu-id="1b89e-122">Une fois qu’une erreur est ignorée, la bannière de document change de couleur et indique que l’erreur de traitement a été ignorée.</span><span class="sxs-lookup"><span data-stu-id="1b89e-122">After an error is ignored, the document banner changes color and indicates that the processing error was ignored.</span></span> <span data-ttu-id="1b89e-123">À tout moment, vous pouvez revenir à la décision d’ignorer l’erreur en cliquant sur **Revert**.</span><span class="sxs-lookup"><span data-stu-id="1b89e-123">At any time, you can revert the decision to ignore the error by clicking **Revert**.</span></span>

![Cliquez sur Ignorer pour ignorer l’erreur de traitement](../media/SIERimage3.png)

<span data-ttu-id="1b89e-125">Vous pouvez également rechercher tous les documents dont l’erreur de traitement a été ignorée à l’aide de la *condition* d’erreurs de traitement ignorée lors de l’interrogation de documents dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-125">You can also search for all documents that had a processing error that was ignored by using the *Ignored processing errors* condition when querying documents in a review set.</span></span>

![Utiliser la condition Des erreurs de traitement ignorées pour rechercher des documents d’erreur ignorés](../media/SIERimage4.png)

## <a name="remediate-a-document-with-errors"></a><span data-ttu-id="1b89e-127">Corriger un document avec des erreurs</span><span class="sxs-lookup"><span data-stu-id="1b89e-127">Remediate a document with errors</span></span>

<span data-ttu-id="1b89e-128">Parfois, il peut vous être demandé de corriger une erreur de traitement dans les documents (en supprimant un mot de passe, en déchiffrant un fichier chiffré ou en récupérant un document endommagé), puis d’ajouter le document corrigé au jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-128">Sometimes you may be required to remediate a processing error in documents (by removing a password, decrypting an encrypted file, or recovering a corrupted document) and then add the remediated document to the review set.</span></span> <span data-ttu-id="1b89e-129">Cela vous permet de consulter et d’exporter le document d’erreurs avec les autres documents du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-129">This allows you to review and export the error document together with the other documents in the review set.</span></span> 

<span data-ttu-id="1b89e-130">Pour corriger un document unique, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b89e-130">To remediate a single document, follow these steps:</span></span>

1. <span data-ttu-id="1b89e-131">Cliquez **sur Télécharger**  >  **l’original** pour télécharger une copie du fichier sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1b89e-131">Click **Download** > **Download original** to download a copy of the file to a local computer.</span></span>

   ![Télécharger le document avec l’erreur de traitement](../media/SIERimage5.png)

2. <span data-ttu-id="1b89e-133">Corriger l’erreur dans le fichier hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1b89e-133">Remediate the error in the file offline.</span></span> <span data-ttu-id="1b89e-134">Pour les fichiers chiffrés, qui nécessitent un logiciel de déchiffrement, pour supprimer la protection par mot de passe, fournissez le mot de passe et enregistrez le fichier ou utilisez un logiciel de déchiffrement de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1b89e-134">For encrypted files, that would require decryption software, to remove password protection, either provide the password and save the file or use a password cracker.</span></span> <span data-ttu-id="1b89e-135">Après avoir corrigé le fichier, allez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="1b89e-135">After you remediate the file, go to the next step.</span></span>

3. <span data-ttu-id="1b89e-136">Dans le jeu à réviser, sélectionnez le fichier avec l’erreur de traitement que vous avez corrigé, puis cliquez sur **Correction.**</span><span class="sxs-lookup"><span data-stu-id="1b89e-136">In the review set, select the file with the processing error that you remediated, and then  click **Remediation**.</span></span>

   ![Cliquez sur Correction dans la bannière du document avec erreur de traitement](../media/SIERimage6.png)


4. <span data-ttu-id="1b89e-138">Cliquez **sur** Parcourir, accédez à l’emplacement du fichier corrigé sur votre ordinateur local, puis sélectionnez le fichier.</span><span class="sxs-lookup"><span data-stu-id="1b89e-138">Click **Browse**, go to the location of the remediated file on your local computer, and then select the file.</span></span>

   ![Cliquez sur Parcourir et sélectionnez le fichier corrigé sur votre ordinateur local](../media/SIERimage7.png)

    <span data-ttu-id="1b89e-140">Une fois le fichier corrigé sélectionné, il est automatiquement chargé dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-140">After selecting the remediated file, it is automatically uploaded to the review set.</span></span> <span data-ttu-id="1b89e-141">Vous pouvez suivre l’état de traitement du fichier.</span><span class="sxs-lookup"><span data-stu-id="1b89e-141">You can track the processing status of the file.</span></span>

    ![L’état du processus de correction s’affiche](../media/SIERimage8.png)

   <span data-ttu-id="1b89e-143">Une fois le traitement terminé, vous pouvez afficher le document corrigé.</span><span class="sxs-lookup"><span data-stu-id="1b89e-143">After processing is completed, you can view the remediated document.</span></span>

    ![Vous pouvez afficher le fichier corrigé au format natif dans le jeu à réviser](../media/SIERimage9.png)

<span data-ttu-id="1b89e-145">Pour plus d’informations sur ce qui se produit lorsqu’un document est corrigé, voir Ce qui se produit [lorsque des fichiers sont corrigés.](error-remediation-when-processing-data-in-advanced-ediscovery.md#what-happens-when-files-are-remediated)</span><span class="sxs-lookup"><span data-stu-id="1b89e-145">For more information about what happens when a document is remediated, see [What happens when files are remediated](error-remediation-when-processing-data-in-advanced-ediscovery.md#what-happens-when-files-are-remediated).</span></span>

## <a name="search-for-remediated-documents"></a><span data-ttu-id="1b89e-146">Rechercher des documents corrigés</span><span class="sxs-lookup"><span data-stu-id="1b89e-146">Search for remediated documents</span></span>

<span data-ttu-id="1b89e-147">Vous pouvez rechercher tous les documents d’un jeu à réviser qui ont été corrigés à l’aide de la condition **Keywords** et en spécifiant la paire property:value suivante : **IsFromErrorRemediation:true**.</span><span class="sxs-lookup"><span data-stu-id="1b89e-147">You can search for all documents in a review set that were remediated by using the **Keywords** condition and specifying the following property:value pair: **IsFromErrorRemediation:true**.</span></span> <span data-ttu-id="1b89e-148">Cette propriété est également disponible dans le fichier de chargement d’exportation lorsque vous exportez des documents à partir d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="1b89e-148">This property is also available in the export load file when you export documents from a review set.</span></span>
