---
title: Importer du contenu non-Microsoft 365 pour une analyse avancée de la découverte électronique
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
titleSuffix: Office 365
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Procédure d’importation du contenu qui n’est pas stocké dans Microsoft 365 dans un objet BLOB Azure afin qu’il puisse être analysé avec AeD
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 03220e6baf16662ad8dfa970ef4d7077d08b0826
ms.sourcegitcommit: 47de4402174c263ae8d70c910ca068a7581d04ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "49662899"
---
# <a name="import-non-microsoft-365-content-for-advanced-ediscovery-classic-analysis"></a><span data-ttu-id="7134b-103">Importer du contenu non-Microsoft 365 pour l’analyse avancée eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="7134b-103">Import non-Microsoft 365 content for Advanced eDiscovery (classic) analysis</span></span>

<span data-ttu-id="7134b-104">Tous les documents que vous devrez peut-être analyser avec Advanced eDiscovery ne seront pas opérationnels dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7134b-104">Not all documents that you may need to analyze with Advanced eDiscovery will live in Microsoft 365.</span></span> <span data-ttu-id="7134b-105">Avec la fonctionnalité d’importation de contenu non-Microsoft 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne résident pas dans Microsoft 365 (à l’exception des fichiers PST) dans un objet blob de stockage associé à une casse, et les analyser avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7134b-105">With the Non-Microsoft 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Microsoft 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery.</span></span> <span data-ttu-id="7134b-106">Cette procédure vous montre comment intégrer des documents non-Microsoft 365 dans Advanced eDiscovery pour les analyser.</span><span class="sxs-lookup"><span data-stu-id="7134b-106">This procedure shows you how to bring your non-Microsoft 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7134b-p102">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="7134b-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7134b-109">Vous pouvez acheter un abonnement de complément de stockage de données eDiscovery avancé pour votre contenu non-Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7134b-109">You can purchase an Advanced eDiscovery data storage add-on subscription for your non-Microsoft 365 content.</span></span> <span data-ttu-id="7134b-110">Cette fonctionnalité est exclusivement disponible pour le contenu qui doit être analysé avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7134b-110">This is exclusively available for content that is to be analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="7134b-111">Suivez les étapes de la procédure [acheter ou modifier un module complémentaire pour Microsoft 365 pour les entreprises](https://docs.microsoft.com/microsoft-365/commerce/buy-or-edit-an-add-on) et acheter le complément de stockage avancé eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7134b-111">Follow the steps in [Buy or edit an add-on for Microsoft 365 for business](https://docs.microsoft.com/microsoft-365/commerce/buy-or-edit-an-add-on) and purchase the Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="requirements-to-upload-non-office-365-content"></a><span data-ttu-id="7134b-112">Conditions requises pour télécharger du contenu non-Office 365</span><span class="sxs-lookup"><span data-stu-id="7134b-112">Requirements to upload non-Office 365 content</span></span>

<span data-ttu-id="7134b-113">L’utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7134b-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="7134b-114">Un Office 365 E3 avec le complément de conformité avancé ou l’abonnement E5.</span><span class="sxs-lookup"><span data-stu-id="7134b-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>
    
- <span data-ttu-id="7134b-115">Tous les dépositaires dont le contenu n’est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.</span><span class="sxs-lookup"><span data-stu-id="7134b-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>
    
- <span data-ttu-id="7134b-116">Un cas eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="7134b-116">An existing eDiscovery case.</span></span>
    
- <span data-ttu-id="7134b-117">Tous les fichiers de téléchargement rassemblé dans des dossiers où se trouve un dossier par dépositaire et le nom de ces dossiers est au format  *alias@domainname*  .</span><span class="sxs-lookup"><span data-stu-id="7134b-117">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  .</span></span> <span data-ttu-id="7134b-118">Le  *alias@domainname*  doit être l’alias et le domaine Office 365 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7134b-118">The  *alias@domainname*  must be users Office 365 alias and domain.</span></span> <span data-ttu-id="7134b-119">Vous pouvez collecter tous les dossiers  *alias@domainname*  dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="7134b-119">You can collect all the  *alias@domainname*  folders into a root folder.</span></span> <span data-ttu-id="7134b-120">Le dossier racine ne peut contenir que les dossiers  *alias@domainname*  , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="7134b-120">The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder.</span></span>
    
- <span data-ttu-id="7134b-121">Un compte qui soit un gestionnaire eDiscovery ou un administrateur eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7134b-121">An account that is either an eDiscovery Manager or eDiscovery Administrator.</span></span>
    
- <span data-ttu-id="7134b-122">[Outils de stockage Microsoft Azure](https://aka.ms/downloadazcopy) installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="7134b-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="7134b-123">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7134b-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>


1. <span data-ttu-id="7134b-124">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez **eDiscovery** et ouvrez le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="7134b-124">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to.</span></span> <span data-ttu-id="7134b-125">Si vous devez créer un cas, voir [Manage eDiscovery cases dans le centre de sécurité &amp; conformité](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="7134b-125">If you need to create a case, see [Manage eDiscovery cases in the Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
    
2. <span data-ttu-id="7134b-126">Cliquez sur **basculer vers Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="7134b-126">Click **Switch to Advanced eDiscovery**.</span></span>

3. <span data-ttu-id="7134b-127">Sélectionnez **examiner les jeux** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="7134b-127">Select **Review Sets** from the menu.</span></span>

4. <span data-ttu-id="7134b-128">Sélectionnez un ensemble de validation existant ou choisissez **Ajouter un ensemble de réexamens**.</span><span class="sxs-lookup"><span data-stu-id="7134b-128">Select an existing Review Set or choose **Add Review Set**.</span></span>

5. <span data-ttu-id="7134b-129">Sélectionnez **Manage Review Set**.</span><span class="sxs-lookup"><span data-stu-id="7134b-129">Select **Manage review set**.</span></span>

6. <span data-ttu-id="7134b-130">Dans la carte de données autres que Office 365, sélectionnez **afficher les téléchargements**.</span><span class="sxs-lookup"><span data-stu-id="7134b-130">In the Non-Office 365 data card, select **View Uploads**.</span></span>

7. <span data-ttu-id="7134b-131">Choisissez **Télécharger les fichiers** pour démarrer l’Assistant chargement de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7134b-131">Choose **Upload files** to start the file upload wizard.</span></span>

8. <span data-ttu-id="7134b-132">Le premier onglet est **1. Étape de préparation**.</span><span class="sxs-lookup"><span data-stu-id="7134b-132">The first tab is **1. Prepare step**.</span></span> <span data-ttu-id="7134b-133">Sélectionnez **suivant : charger les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="7134b-133">Select **Next: Upload files**.</span></span>

9. <span data-ttu-id="7134b-134">Sur le **2. Onglet charger les fichiers** vous êtes invité à télécharger AzCopy.exe si vous ne l’avez pas déjà fait, puis à indiquer le chemin d’accès à l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="7134b-134">On the **2. Upload files** tab you will be prompted to download AzCopy.exe if you have not done so already, and then to provide the path to the file location.</span></span> <span data-ttu-id="7134b-135">Par exemple, `C:\Upload`  vous donnera la commande pour exécuter AzCopy.exe.</span><span class="sxs-lookup"><span data-stu-id="7134b-135">For example, `C:\Upload`  will give you the command to execute AzCopy.exe.</span></span> <span data-ttu-id="7134b-136">À l’aide `C:\Upload` de, vous verrez :</span><span class="sxs-lookup"><span data-stu-id="7134b-136">Using `C:\Upload`, you will see:</span></span>

   `"%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy\AzCopy.exe" /Source:"c:\upload" /Dest:"https://spnam03salinkexternal003.blob.core.windows.net/16d13440-a6a4-4bc5-a82b-10ac9cfe9d7c-1601401811-externalstore?sv=2017-07-29&sr=c&si=ExternalStore63%7C0&sig=9Dq5v20TwkxByYDHhIEx%2FHSLlmlqUjY0njkJyTO0zGA%3D" /s`
  
10. <span data-ttu-id="7134b-137">Ouvrez une fenêtre d’invite de commandes et exécutez la commande AzCopy.exe pour importer les données dans Azure.</span><span class="sxs-lookup"><span data-stu-id="7134b-137">Open a command prompt window and execute the AzCopy.exe command to import the data into Azure.</span></span> <span data-ttu-id="7134b-138">Une fois toutes les données chargées, sélectionnez **suivant : traiter les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="7134b-138">Once it has loaded all of the data, select **Next: Process files**.</span></span>

11. <span data-ttu-id="7134b-139">L’onglet suivant est **3. Traitez les fichiers** dans lesquels vous verrez les dépositaires auxquels des données sont associées et vous verrez également la progression des données importées.</span><span class="sxs-lookup"><span data-stu-id="7134b-139">The next tab is **3. Process files** where you will see the custodians that have data associated with them and will also show you the progress of the data being imported.</span></span>
        
    <span data-ttu-id="7134b-140">Pour plus d’informations sur la syntaxe Azcopy, consultez [la rubrique transférer des données avec le Azcopy sur Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="7134b-140">For more information on Azcopy syntax, see [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span> 
    
    <span data-ttu-id="7134b-141">Pour plus d’informations sur le traitement de la découverte électronique avancée, voir [exécuter le module de processus et charger des données dans Advanced eDiscovery (classique)](run-the-process-module-and-load-data-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="7134b-141">For more details on Advanced eDiscovery Processing, see [Run the Process module and load data in Advanced eDiscovery (classic)](run-the-process-module-and-load-data-in-advanced-ediscovery.md).</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="7134b-142">Il doit y avoir un dossier racine par utilisateur et le nom du dossier doit être au format <b>alias@domainname</b>  .</span><span class="sxs-lookup"><span data-stu-id="7134b-142">There must be one root folder per user and the folder name must be in the <b>alias@domainname</b>  format.</span></span> 
   
    > [!IMPORTANT]
    > <span data-ttu-id="7134b-143">Une fois que le conteneur a été traité avec succès dans Advanced eDiscovery, vous ne pourrez plus ajouter de nouveau contenu au stockage SAS dans Azure.</span><span class="sxs-lookup"><span data-stu-id="7134b-143">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure.</span></span> <span data-ttu-id="7134b-144">Si vous recueillez du contenu supplémentaire et que vous souhaitez l’ajouter à la demande d’analyse avancée de la découverte électronique, vous devez créer un conteneur de **données non-Office 365** et répéter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="7134b-144">If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="7134b-145">Si le conteneur  *ne traite pas correctement en raison de problèmes d’attribution de nom de dossier*  et que vous résolvez les problèmes, vous devrez tout de même créer un nouveau conteneur et reconnecter et télécharger à nouveau à l’aide des procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7134b-145">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span>
