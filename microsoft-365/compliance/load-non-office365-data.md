---
title: Charger des données non-Office 365 dans une preuve
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
description: ''
ms.openlocfilehash: 4db0b40d485c4c1107bdcb0d49616cadb15b1915
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42072157"
---
# <a name="load-non-office-365-data-into-evidence"></a><span data-ttu-id="0539a-102">Charger des données non-Office 365 dans une preuve</span><span class="sxs-lookup"><span data-stu-id="0539a-102">Load non-Office 365 data into evidence</span></span>

<span data-ttu-id="0539a-103">Tous les documents que vous devrez peut-être analyser dans une enquête sur les données se trouvent dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0539a-103">Not all documents that you may need to analyze in a data investigation will be located in Office 365.</span></span> <span data-ttu-id="0539a-104">Avec la fonctionnalité d’importation de contenu autre que Office 365, vous pouvez télécharger des documents qui ne résident pas dans Office 365 dans des preuves afin qu’ils puissent être analysés lors d’une enquête de données.</span><span class="sxs-lookup"><span data-stu-id="0539a-104">With the Non-Office 365 content import feature you can upload documents that don't live in Office 365 into evidence so they can be analyzed in a data investigation.</span></span>

>[!Note]
><span data-ttu-id="0539a-105">L’enquête sur les données nécessite une offre Office 365 E3 avec le complément de conformité avancé ou un abonnement E5 pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0539a-105">Data investigation requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="0539a-106">Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="0539a-106">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0539a-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0539a-107">Before you begin</span></span>

<span data-ttu-id="0539a-108">L’utilisation de la fonctionnalité Télécharger non-Office 365 comme décrit dans cette procédure nécessite que vous ayez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0539a-108">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="0539a-109">Un Office 365 E3 avec le complément de conformité avancé ou l’abonnement E5.</span><span class="sxs-lookup"><span data-stu-id="0539a-109">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="0539a-110">Tous les dépositaires dont le contenu n’est pas Office 365 seront chargés doivent disposer de E3 avec un complément de conformité avancé ou des licences E5.</span><span class="sxs-lookup"><span data-stu-id="0539a-110">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="0539a-111">Un cas eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="0539a-111">An existing eDiscovery case.</span></span>

- <span data-ttu-id="0539a-112">Tous les fichiers de téléchargement rassemblé dans des dossiers où se trouve un dossier par dépositaire et le nom de ces dossiers est au format *alias@domainname*.</span><span class="sxs-lookup"><span data-stu-id="0539a-112">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname*.</span></span> <span data-ttu-id="0539a-113">Le *alias@domainname* doit être l’alias et le domaine Office 365 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0539a-113">The *alias@domainname* must be users Office 365 alias and domain.</span></span> <span data-ttu-id="0539a-114">Vous pouvez collecter tous les dossiers *alias@domainname* dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="0539a-114">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="0539a-115">Le dossier racine ne peut contenir que les dossiers *alias@domainname* , il ne doit pas y avoir de fichiers libres dans le dossier racine.</span><span class="sxs-lookup"><span data-stu-id="0539a-115">The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="0539a-116">Un compte qui est un gestionnaire eDiscovery ou un administrateur eDiscovery outils de stockage Microsoft Azure installé sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="0539a-116">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="0539a-117">Installez AzCopy en procédant comme suit :https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="0539a-117">Install AzCopy, which you can do from here: https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-in-to-a-data-investigation"></a><span data-ttu-id="0539a-118">Télécharger du contenu non-Office 365 dans une enquête de données</span><span class="sxs-lookup"><span data-stu-id="0539a-118">Upload non-Office 365 content in to a data investigation</span></span>

1. <span data-ttu-id="0539a-119">Open \* \* \* \* enquêtes de données \* \*, l’enquête sur laquelle les données non Office 365 seront téléchargées.</span><span class="sxs-lookup"><span data-stu-id="0539a-119">Open \*\*\*\*Data Investigations\*\*, then the investigation that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="0539a-120">Cliquez sur l’onglet **Evidence** , puis sélectionnez l’ensemble de preuves sur lequel vous souhaitez charger les données Non Office 365.</span><span class="sxs-lookup"><span data-stu-id="0539a-120">Click the **Evidence** tab, then select the evidence set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="0539a-121">Si vous n’avez pas encore créé d’ensemble de preuves, vous pouvez le faire maintenant.</span><span class="sxs-lookup"><span data-stu-id="0539a-121">If you have not already created an evidence set, you can do so now.</span></span>  <span data-ttu-id="0539a-122">Enfin, cliquez sur **gérer les preuves** , puis sur Afficher les **téléchargements** dans la section données non-Office 365</span><span class="sxs-lookup"><span data-stu-id="0539a-122">Finally, click **Manage evidence** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="0539a-123">Cliquez sur le bouton **Télécharger les fichiers** pour démarrer l’Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="0539a-123">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Charger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="0539a-125">La première étape de l’Assistant consiste à préparer un objet BLOB Azure sécurisé pour les fichiers à charger.</span><span class="sxs-lookup"><span data-stu-id="0539a-125">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="0539a-126">Une fois la préparation terminée, cliquez sur le bouton **suivant : charger des fichiers** .</span><span class="sxs-lookup"><span data-stu-id="0539a-126">After the preparation is complete, click the **Next: Upload files** button.</span></span>

![Préparation à l’importation de données non Office 365](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="0539a-128">Dans l’étape **Télécharger les fichiers** , spécifiez le chemin d' **accès à l’emplacement des fichiers**, c’est ici que se trouvent les données autres que Office 365 que vous prévoyez d’importer.</span><span class="sxs-lookup"><span data-stu-id="0539a-128">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="0539a-129">La définition de l’emplacement correct garantit la mise à jour correcte de la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="0539a-129">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="0539a-130">Si vous n’avez pas encore installé AzCopy, vous pouvez le faire à partir de là :https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="0539a-130">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="0539a-131">Copiez la commande prédéfinie en cliquant sur le lien **copier dans le presse-papiers** .</span><span class="sxs-lookup"><span data-stu-id="0539a-131">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="0539a-132">Démarrez une invite de commandes Windows, collez la commande et appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="0539a-132">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="0539a-133">Les fichiers sont téléchargés vers le stockage BLOB Azure sécurisé pour l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="0539a-133">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Charger des fichiers pour l’importation de données non-Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Utiliser AzCopy pour importer des données autres que Office 365](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="0539a-136">Enfin, revenez à la sécurité & conformité et cliquez sur le bouton **suivant : traiter les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="0539a-136">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="0539a-137">Cela lance le traitement, l’extraction de texte et l’indexation des fichiers téléchargés.</span><span class="sxs-lookup"><span data-stu-id="0539a-137">This initiates processing, text extraction, and indexing of the uploaded files.</span></span>  <span data-ttu-id="0539a-138">Vous pouvez suivre la progression du traitement ou dans l’onglet **travaux** .  Une fois terminé, les nouveaux fichiers sont disponibles dans l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="0539a-138">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files are available in the evidence set.</span></span>  <span data-ttu-id="0539a-139">Une fois le traitement terminé, vous pouvez faire disparaître l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="0539a-139">After processing is complete, you can dismiss the wizard.</span></span>

![Fichiers du processus d’importation non-Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

