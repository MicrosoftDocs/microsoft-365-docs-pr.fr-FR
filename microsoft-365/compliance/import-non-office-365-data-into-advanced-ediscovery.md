---
title: Importer du contenu non-Office 365 pour l’analyse eDiscovery avancée
ms.author: chrfox
author: chrfox
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
description: Procédure d’importation de contenu qui n’est pas stocké dans O365 dans un objet BLOB Azure afin qu’il puisse être analysé avec AeD
ms.openlocfilehash: aa14a54c20ac580c6412e8dc534ec44520abb3c8
ms.sourcegitcommit: 6ae69c40bafa6aef633789c3df0fa20590bdcf40
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2019
ms.locfileid: "40823786"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="eb56d-103">Importer du contenu non-Office 365 pour l’analyse eDiscovery avancée</span><span class="sxs-lookup"><span data-stu-id="eb56d-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="eb56d-104">Tous les documents que vous devrez peut-être analyser avec Office 365 Advanced eDiscovery seront inactifs dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="eb56d-104">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="eb56d-105">Avec la fonctionnalité d’importation de contenu non-Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne sont pas en ligne dans Office 365 (à l’exception des fichiers PST) dans un blob de stockage associé à une casse, et les analyser avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="eb56d-105">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery.</span></span> <span data-ttu-id="eb56d-106">Cette procédure vous montre comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="eb56d-106">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="eb56d-p102">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="eb56d-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eb56d-109">Vous pouvez acheter un abonnement de complément de stockage de données eDiscovery Office 365 Advanced eDiscovery pour votre contenu non-Office 365.</span><span class="sxs-lookup"><span data-stu-id="eb56d-109">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content.</span></span> <span data-ttu-id="eb56d-110">Cette fonctionnalité est exclusivement disponible pour le contenu qui doit être analysé avec Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="eb56d-110">This is exclusively available for content that is to be analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="eb56d-111">Suivez les étapes de l’achat ou de la [modification et du complément pour office 365 pour les entreprises](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) et achetez le complément de stockage Office 365 Advanced eDiscovery Storage.</span><span class="sxs-lookup"><span data-stu-id="eb56d-111">Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="eb56d-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="eb56d-112">Before you begin</span></span>

<span data-ttu-id="eb56d-113">L’utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="eb56d-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="eb56d-114">Une application Office 365 E3 avec un complément de conformité avancé ou un abonnement E5</span><span class="sxs-lookup"><span data-stu-id="eb56d-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="eb56d-115">Tous les dépositaires dont le contenu n’est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.</span><span class="sxs-lookup"><span data-stu-id="eb56d-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="eb56d-116">Un cas eDiscovery existant</span><span class="sxs-lookup"><span data-stu-id="eb56d-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="eb56d-117">Tous les fichiers de téléchargement rassemblé dans des dossiers où se trouve un dossier par dépositaire et le nom de ces dossiers est au format *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="eb56d-117">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  .</span></span> <span data-ttu-id="eb56d-118">Le *alias@domainname* doit être l’alias et le domaine Office 365 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="eb56d-118">The  *alias@domainname*  must be users Office 365 alias and domain.</span></span> <span data-ttu-id="eb56d-119">Vous pouvez collecter tous les dossiers *alias@domainname* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="eb56d-119">You can collect all the  *alias@domainname*  folders into a root folder.</span></span> <span data-ttu-id="eb56d-120">Le dossier racine ne peut contenir que les dossiers *alias@domainname* , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="eb56d-120">The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="eb56d-121">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eb56d-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="eb56d-122">[Outils de stockage Microsoft Azure](https://aka.ms/downloadazcopy) installés sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="eb56d-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="eb56d-123">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eb56d-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>


1. <span data-ttu-id="eb56d-124">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez **eDiscovery**et ouvrez le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="eb56d-124">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to.</span></span> <span data-ttu-id="eb56d-125">Si vous devez créer un cas, voir [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md)</span><span class="sxs-lookup"><span data-stu-id="eb56d-125">If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="eb56d-126">Cliquer sur **basculer vers Advanced eDiscovery**</span><span class="sxs-lookup"><span data-stu-id="eb56d-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="eb56d-127">Sous **type** de source **, sélectionnez données non Office 365**.</span><span class="sxs-lookup"><span data-stu-id="eb56d-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="eb56d-128">Cliquez sur **Ajouter un conteneur**.</span><span class="sxs-lookup"><span data-stu-id="eb56d-128">Click **Add container**.</span></span> <span data-ttu-id="eb56d-129">Nommez le conteneur et ajoutez une description.</span><span class="sxs-lookup"><span data-stu-id="eb56d-129">Name the container and add a description.</span></span>
    
5. <span data-ttu-id="eb56d-130">Sélectionnez le conteneur nouvellement ajouté dans la liste du conteneur et copiez l’URL qui apparaît dans le volet d’informations du conteneur, puis fermez le volet.</span><span class="sxs-lookup"><span data-stu-id="eb56d-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="eb56d-131">Ouvrez une invite de commandes en tant qu’administrateur et accédez au répertoire dans lequel vous avez installé AzCopy..</span><span class="sxs-lookup"><span data-stu-id="eb56d-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="eb56d-132">Construisez la ligne de commande AzCopy pour télécharger les fichiers comme suit :</span><span class="sxs-lookup"><span data-stu-id="eb56d-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="eb56d-133">AzCopy/source : " *chemin d’accès complet au dossier racine sur l’ordinateur local* "/dest : " *URL de conteneur jusqu’à et n’incluant pas l' ?*</span><span class="sxs-lookup"><span data-stu-id="eb56d-133">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*</span></span>  <span data-ttu-id="eb56d-134">« /DestSAS : » *reste de l’URL du conteneur à partir du ? jusqu’à la fin* «/S.</span><span class="sxs-lookup"><span data-stu-id="eb56d-134">" /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="eb56d-135">Par exemple, à l’aide des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb56d-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="eb56d-136">dossier racine-données C:\Collected</span><span class="sxs-lookup"><span data-stu-id="eb56d-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="eb56d-137">URL du conteneur https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp-; SR =&amp;c si = NonOfficeData15%&amp;7C0 SIG = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA% 3D</span><span class="sxs-lookup"><span data-stu-id="eb56d-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="eb56d-138">la syntaxe de la ligne de commande AzCopy est la suivante :</span><span class="sxs-lookup"><span data-stu-id="eb56d-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="eb56d-139">Pour plus d’informations sur la syntaxe Azcopy, reportez-vous à [la rubrique transférer des données avec le Azcopy sur Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span><span class="sxs-lookup"><span data-stu-id="eb56d-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="eb56d-140">Il doit y avoir un dossier racine par utilisateur et le nom du dossier doit être au format *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="eb56d-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="eb56d-141">Une fois le téléchargement des dossiers terminé, revenez à Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="eb56d-141">Once the folders have finished uploading, switch back to Advanced eDiscovery.</span></span> <span data-ttu-id="eb56d-142">Le contenu des dossiers téléchargés est maintenant prêt à être traité dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="eb56d-142">The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery.</span></span> <span data-ttu-id="eb56d-143">Sélectionnez le conteneur, puis cliquez sur le bouton processus.</span><span class="sxs-lookup"><span data-stu-id="eb56d-143">Select the container and click the Process button.</span></span> <span data-ttu-id="eb56d-144">Pour plus d’informations sur le traitement de la découverte électronique avancée, consultez [la rubrique exécuter le module de processus et charger des données dans Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="eb56d-144">For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="eb56d-145">Une fois que le conteneur a été traité avec succès dans Advanced eDiscovery, vous ne pourrez plus ajouter de nouveau contenu au stockage SAS dans Azure.</span><span class="sxs-lookup"><span data-stu-id="eb56d-145">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure.</span></span> <span data-ttu-id="eb56d-146">Si vous recueillez du contenu supplémentaire et que vous souhaitez l’ajouter à la demande d’analyse avancée de la découverte électronique, vous devez créer un conteneur de **données non-Office 365** et répéter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="eb56d-146">If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="eb56d-147">Si le conteneur *ne traite pas correctement en raison de problèmes d’attribution de nom de dossier* et que vous résolvez les problèmes, vous devrez tout de même créer un nouveau conteneur et reconnecter et télécharger à nouveau à l’aide des procédures décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="eb56d-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span>