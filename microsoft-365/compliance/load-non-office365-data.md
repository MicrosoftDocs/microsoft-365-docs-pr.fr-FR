---
title: Charger des données non-Microsoft 365 dans la preuve
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
description: Découvrez comment utiliser la fonctionnalité d’importation de contenu autre qu’Office 365 pour télécharger des documents non Office 365 dans des preuves dans une enquête de données.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 499b1074b9a1e2026804eab2ac958fe7392e98ea
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034412"
---
# <a name="load-non-microsoft-365-data-into-evidence"></a><span data-ttu-id="3f22a-103">Charger des données non-Microsoft 365 dans la preuve</span><span class="sxs-lookup"><span data-stu-id="3f22a-103">Load non-Microsoft 365 data into evidence</span></span>

<span data-ttu-id="3f22a-104">Tous les documents que vous devrez peut-être analyser dans une enquête sur les données se trouvent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3f22a-104">Not all documents that you may need to analyze in a data investigation will be located in Microsoft 365.</span></span> <span data-ttu-id="3f22a-105">Avec la fonctionnalité d’importation de contenu non-Microsoft 365, vous pouvez télécharger des documents qui ne résident pas dans Microsoft 365 dans des preuves afin qu’ils puissent être analysés lors d’une enquête de données.</span><span class="sxs-lookup"><span data-stu-id="3f22a-105">With the Non-Microsoft 365 content import feature you can upload documents that don't live in Microsoft 365 into evidence so they can be analyzed in a data investigation.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="3f22a-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3f22a-106">Before you begin</span></span>

<span data-ttu-id="3f22a-107">L’utilisation de la fonctionnalité Télécharger non-Microsoft 365, comme décrit dans cette procédure, nécessite que vous disposiez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3f22a-107">Using the upload Non-Microsoft 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="3f22a-108">Un abonnement Microsoft 365 ou Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="3f22a-108">A Microsoft 365 or Office 365 E5 subscription.</span></span>

- <span data-ttu-id="3f22a-109">Tous les intérêts dont le contenu n’est pas Microsoft 365 seront téléchargés doivent disposer de la licence de complément E5 ou E5 appropriée.</span><span class="sxs-lookup"><span data-stu-id="3f22a-109">All people of interest whose non-Microsoft 365 content will be uploaded must have the appropriate E5 or E5 add-on license.</span></span>

- <span data-ttu-id="3f22a-110">Un cas eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="3f22a-110">An existing eDiscovery case.</span></span>

- <span data-ttu-id="3f22a-111">Tous les fichiers de téléchargement rassemblé dans des dossiers où se trouve un dossier par dépositaire et le nom de ces dossiers est au format *alias@domainname*.</span><span class="sxs-lookup"><span data-stu-id="3f22a-111">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname*.</span></span> <span data-ttu-id="3f22a-112">Le *alias@domainname* doit être l’alias et le domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f22a-112">The *alias@domainname* must be user's alias and domain.</span></span> <span data-ttu-id="3f22a-113">Vous pouvez collecter tous les dossiers *alias@domainname* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="3f22a-113">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="3f22a-114">Le dossier racine ne peut contenir que les dossiers *alias@domainname* , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="3f22a-114">The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="3f22a-115">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery outils de stockage Microsoft Azure installé sur un ordinateur ayant accès à la structure de dossiers de contenu non-Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3f22a-115">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Microsoft 365 content folder structure.</span></span>

- <span data-ttu-id="3f22a-116">Installez AzCopy en procédant comme suit :https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="3f22a-116">Install AzCopy, which you can do from here: https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-microsoft-365-content-in-to-a-data-investigation"></a><span data-ttu-id="3f22a-117">Télécharger du contenu non-Microsoft 365 dans une enquête de données</span><span class="sxs-lookup"><span data-stu-id="3f22a-117">Upload non-Microsoft 365 content in to a data investigation</span></span>

1. <span data-ttu-id="3f22a-118">Ouvrez les **enquêtes de données** et accédez à l’enquête sur laquelle les données non Microsoft 365 seront téléchargées.</span><span class="sxs-lookup"><span data-stu-id="3f22a-118">Open **Data Investigations** and go to the investigation that the non-Microsoft 365 data will be uploaded to.</span></span>  <span data-ttu-id="3f22a-119">Cliquez sur l’onglet **Evidence** , puis sélectionnez l’ensemble de preuves sur lequel vous souhaitez charger les données.</span><span class="sxs-lookup"><span data-stu-id="3f22a-119">Click the **Evidence** tab, then select the evidence set you wish to load the data to.</span></span>  <span data-ttu-id="3f22a-120">Si vous n’avez pas encore créé d’ensemble de preuves, vous pouvez le faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="3f22a-120">If you have not already created an evidence set, you can do so now.</span></span>  <span data-ttu-id="3f22a-121">Enfin, cliquez sur **gérer les preuves** , puis afficher les **téléchargements** dans la section données.</span><span class="sxs-lookup"><span data-stu-id="3f22a-121">Finally, click **Manage evidence** then **View uploads** in the data section</span></span>

2. <span data-ttu-id="3f22a-122">Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l’Assistant importation de données non-Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3f22a-122">Click the **Upload files** button to start the Non-Microsoft 365 data import wizard.</span></span>

![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="3f22a-124">La première étape de l’Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.</span><span class="sxs-lookup"><span data-stu-id="3f22a-124">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="3f22a-125">Une fois la préparation terminée, cliquez sur le bouton **suivant : charger des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="3f22a-125">After the preparation is complete, click the **Next: Upload files** button.</span></span>

![Préparation à l’importation de données non Microsoft 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="3f22a-127">Dans l’étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l’emplacement des fichiers**, c’est ici que se trouvent les données autres que Microsoft 365 que vous prévoyez d’importer.</span><span class="sxs-lookup"><span data-stu-id="3f22a-127">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Microsoft 365 data you plan on importing is located.</span></span>  <span data-ttu-id="3f22a-128">La définition de l’emplacement correct garantit la mise à jour correcte de la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="3f22a-128">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="3f22a-129">Si vous n’avez pas encore installé AzCopy, vous pouvez le faire à partir de là :https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="3f22a-129">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="3f22a-130">Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** .</span><span class="sxs-lookup"><span data-stu-id="3f22a-130">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="3f22a-131">Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="3f22a-131">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="3f22a-132">Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="3f22a-132">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Charger des fichiers pour l’importation de données non Microsoft 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Utiliser AzCopy pour importer des données non-Microsoft 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="3f22a-135">Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant : traiter les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="3f22a-135">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="3f22a-136">Cela lance le traitement, l’extraction de texte et l’indexation des fichiers téléchargés.</span><span class="sxs-lookup"><span data-stu-id="3f22a-136">This initiates processing, text extraction, and indexing of the uploaded files.</span></span>  <span data-ttu-id="3f22a-137">Vous pouvez suivre la progression du traitement ou dans l’onglet **travaux** .  Une fois terminé, les nouveaux fichiers sont disponibles dans l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="3f22a-137">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files are available in the evidence set.</span></span>  <span data-ttu-id="3f22a-138">Une fois le traitement terminé, vous pouvez faire disparaître l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="3f22a-138">After processing is complete, you can dismiss the wizard.</span></span>

![Fichiers de processus d’importation non-Microsoft 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

