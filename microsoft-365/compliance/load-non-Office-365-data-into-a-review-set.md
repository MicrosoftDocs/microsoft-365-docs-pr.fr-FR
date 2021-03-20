---
title: Charger des données non-Microsoft 365 dans un groupe de révision
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez comment importer des données non-Microsoft 365 dans un groupe de révision pour analyse dans un cas Advanced eDiscovery.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: d9f705080ad5a769032581a1517b2daee8e822b2
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50903500"
---
# <a name="load-non-microsoft-365-data-into-a-review-set"></a><span data-ttu-id="d223d-103">Charger des données non-Microsoft 365 dans un groupe de révision</span><span class="sxs-lookup"><span data-stu-id="d223d-103">Load non-Microsoft 365 data into a review set</span></span>

<span data-ttu-id="d223d-104">Tous les documents que vous devez analyser dans Advanced eDiscovery ne se trouvent pas dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d223d-104">Not all documents that you need to analyze in Advanced eDiscovery are located in Microsoft 365.</span></span> <span data-ttu-id="d223d-105">Avec la fonctionnalité d’importation de données non-Microsoft 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne se trouvent pas dans Microsoft 365 dans un groupe de révision.</span><span class="sxs-lookup"><span data-stu-id="d223d-105">With the non-Microsoft 365 data import feature in Advanced eDiscovery, you can upload documents that aren't located in Microsoft 365 to a review set.</span></span> <span data-ttu-id="d223d-106">Cet article vous montre comment faire entrer vos documents non-Microsoft 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="d223d-106">This article shows you how to bring your non-Microsoft 365 documents into Advanced eDiscovery for analysis.</span></span>

## <a name="requirements-to-upload-non-office-365-content"></a><span data-ttu-id="d223d-107">Conditions requises pour télécharger du contenu autre qu’Office 365</span><span class="sxs-lookup"><span data-stu-id="d223d-107">Requirements to upload non-Office 365 content</span></span>

<span data-ttu-id="d223d-108">L’utilisation de la fonctionnalité de téléchargement non-Microsoft 365 décrite dans cet article nécessite que vous disposez des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d223d-108">Using the upload non-Microsoft 365 feature described in this article requires that you have the following:</span></span>

- <span data-ttu-id="d223d-109">Tous les dépositaires à qui vous souhaitez associer du contenu non-Microsoft 365 doivent se voir attribuer la licence appropriée.</span><span class="sxs-lookup"><span data-stu-id="d223d-109">All custodians that you want to associate non-Microsoft 365 content to must be assigned the appropriate license.</span></span> <span data-ttu-id="d223d-110">Pour plus d’informations, [voir Get started with Advanced eDiscovery](get-started-with-advanced-ediscovery.md#step-1-verify-and-assign-appropriate-licenses).</span><span class="sxs-lookup"><span data-stu-id="d223d-110">For more information, see [Get started with Advanced eDiscovery](get-started-with-advanced-ediscovery.md#step-1-verify-and-assign-appropriate-licenses).</span></span>

- <span data-ttu-id="d223d-111">Un cas Advanced eDiscovery existant.</span><span class="sxs-lookup"><span data-stu-id="d223d-111">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="d223d-112">Les dépositaires doivent être ajoutés au cas avant de pouvoir charger et associer les données autres que Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d223d-112">Custodians must be added to the case before you can upload and associate the non-Microsoft 365 data to them.</span></span>

- <span data-ttu-id="d223d-113">Les données ne relevant pas de Microsoft 365 doivent correspondre à un type de fichier pris en charge par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d223d-113">Non-Microsoft 365 data must be a file type that's supported by Advanced eDiscovery.</span></span> <span data-ttu-id="d223d-114">Pour plus d’informations, voir [Types de fichiers pris en charge dans eDiscovery avancée](supported-filetypes-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="d223d-114">For more information, see [Supported file types in Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span></span>

- <span data-ttu-id="d223d-115">Tous les fichiers chargés dans un jeu à réviser doivent se trouver dans des dossiers, chaque dossier étant associé à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="d223d-115">All files that are uploaded to a review set must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="d223d-116">Les noms de ces dossiers doivent être au format suivant : *alias@nom_domaine*.</span><span class="sxs-lookup"><span data-stu-id="d223d-116">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="d223d-117">La valeur alias@nom_domaine doit correspondre à l’alias Microsoft 365 et au domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d223d-117">The alias@domainname must be the user's Microsoft 365 alias and domain.</span></span> <span data-ttu-id="d223d-118">Vous pouvez collecter tous les alias@domainname dossiers d’un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="d223d-118">You can collect all the alias@domainname folders in a root folder.</span></span> <span data-ttu-id="d223d-119">Le dossier racine ne peut contenir que les alias@domainname dossiers.</span><span class="sxs-lookup"><span data-stu-id="d223d-119">The root folder can only contain the alias@domainname folders.</span></span> <span data-ttu-id="d223d-120">Les fichiers libres dans le dossier racine ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d223d-120">Loose files in the root folder aren't supported.</span></span>

   <span data-ttu-id="d223d-121">La structure de dossiers pour les données autres que Microsoft 365 que vous souhaitez télécharger serait similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="d223d-121">The folder structure for the non-Microsoft 365 data that you want to upload would be similar to the following example:</span></span>

   - <span data-ttu-id="d223d-122">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d223d-122">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="d223d-123">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d223d-123">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="d223d-124">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="d223d-124">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="d223d-125">Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont les adresses SMTP des dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="d223d-125">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Structure de dossiers de téléchargement de données non-Microsoft 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="d223d-127">Compte affecté au groupe de rôles Gestionnaire eDiscovery (et ajouté en tant qu’administrateur eDiscovery).</span><span class="sxs-lookup"><span data-stu-id="d223d-127">An account that is assigned to the eDiscovery Manager role group (and added as eDiscovery Administrator).</span></span>

- <span data-ttu-id="d223d-128">L’outil AzCopy v8.1 installé sur un ordinateur qui a accès à la structure de dossiers de contenu non-Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d223d-128">The AzCopy v8.1 tool installed on a computer that has access to the non-Microsoft 365 content folder structure.</span></span> <span data-ttu-id="d223d-129">Pour installer AzCopy, voir Transférer des données avec [AzCopy v8.1 sur Windows.](/previous-versions/azure/storage/storage-use-azcopy)</span><span class="sxs-lookup"><span data-stu-id="d223d-129">To install AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="d223d-130">Assurez-vous d’installer AzCopy à l’emplacement par défaut, à savoir **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span><span class="sxs-lookup"><span data-stu-id="d223d-130">Be sure to install AzCopy in the default location, which is **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span></span> <span data-ttu-id="d223d-131">Vous devez utiliser AzCopy v8.1.</span><span class="sxs-lookup"><span data-stu-id="d223d-131">You must use AzCopy v8.1.</span></span> <span data-ttu-id="d223d-132">D’autres versions d’AzCopy peuvent ne pas fonctionner lors du chargement de données autres que Microsoft 365 dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d223d-132">Other versions of AzCopy may not work when loading non-Microsoft 365 data in Advanced eDiscovery.</span></span>


## <a name="upload-non-microsoft-365-content-into-advanced-ediscovery"></a><span data-ttu-id="d223d-133">Charger du contenu non-Microsoft 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d223d-133">Upload non-Microsoft 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="d223d-134">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery et sélectionnez le cas où les données autres que Microsoft 365 seront téléchargées.</span><span class="sxs-lookup"><span data-stu-id="d223d-134">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, and go to the case that the non-Microsoft 365 data will be uploaded to.</span></span>  

2. <span data-ttu-id="d223d-135">Cliquez **sur Ensembles** de révision, puis sélectionnez le jeu à réviser pour télécharger les données autres que Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d223d-135">Click **Review sets**, and then select the review set to upload the non-Microsoft 365 data to.</span></span>  <span data-ttu-id="d223d-136">Si vous n’avez pas de jeu à réviser, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="d223d-136">If you don't have a review set, you can create one.</span></span> 
 
3. <span data-ttu-id="d223d-137">Dans l’ensemble de révision, cliquez sur **Gérer l’ensemble de révision**, puis cliquez sur **Afficher les téléchargements** sur la mosaïque **Données non-Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="d223d-137">In the review set, click **Manage review set**, and then click **View uploads** on the **Non-Microsoft 365 data** tile.</span></span>

4. <span data-ttu-id="d223d-138">Cliquez sur **Charger des fichiers** pour démarrer l’Assistant importation de données.</span><span class="sxs-lookup"><span data-stu-id="d223d-138">Click **Upload files** to start the data import wizard.</span></span>

   ![Télécharger des fichiers](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   <span data-ttu-id="d223d-140">La première étape de l’Assistant prépare un emplacement de stockage Azure sécurisé fourni par Microsoft pour charger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="d223d-140">The first step in the wizard prepares a secure Microsoft-provided Azure Storage location to upload the files to.</span></span>  <span data-ttu-id="d223d-141">Une fois la préparation terminée, le bouton **Suivant : charger des fichiers** devient actif.</span><span class="sxs-lookup"><span data-stu-id="d223d-141">When the preparation is completed, the **Next: Upload files** button becomes active.</span></span>

   ![Importation non Microsoft 365 : préparer](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. <span data-ttu-id="d223d-143">Cliquez sur **Suivant : charger des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="d223d-143">Click **Next: Upload files**.</span></span>

6. <span data-ttu-id="d223d-144">Dans la page **Télécharger des fichiers,** faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="d223d-144">On the **Upload files** page, do the following:</span></span>

   ![Importation non Microsoft 365 : charger des fichiers](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   <span data-ttu-id="d223d-146">a.</span><span class="sxs-lookup"><span data-stu-id="d223d-146">a.</span></span> <span data-ttu-id="d223d-147">Dans **la** zone Chemin d’accès à l’emplacement des fichiers, vérifiez ou tapez l’emplacement du dossier racine dans lequel vous avez stocké les données autres que Microsoft 365 que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="d223d-147">In the **Path to location of files** box, verify or type the location of the root folder where you've stored the non-Microsoft 365 data you want to upload.</span></span> <span data-ttu-id="d223d-148">Par exemple, pour l’emplacement des exemples de fichiers indiqués dans la **section** Avant de commencer, vous devez taper **%USERPROFILE\Downloads\nonO365**.</span><span class="sxs-lookup"><span data-stu-id="d223d-148">For example, for the location of the example files shown in the **Before you begin section**, you would type **%USERPROFILE\Downloads\nonO365**.</span></span> <span data-ttu-id="d223d-149">En fournissant l’emplacement correct, la commande AzCopy affichée dans la zone sous le chemin d’accès est correctement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d223d-149">Providing the correct location ensures the AzCopy command displayed in box under the path is properly updated.</span></span>

   <span data-ttu-id="d223d-150">b.</span><span class="sxs-lookup"><span data-stu-id="d223d-150">b.</span></span> <span data-ttu-id="d223d-151">Cliquez **sur Copier dans le Presse-papiers** pour copier la commande affichée dans la zone.</span><span class="sxs-lookup"><span data-stu-id="d223d-151">Click **Copy to clipboard** to copy the command that is displayed in the box.</span></span>

7. <span data-ttu-id="d223d-152">Démarrez une invite de commandes Windows, collez la commande que vous avez copiée à l’étape précédente, puis appuyez sur **Entrée** pour démarrer la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="d223d-152">Start a Windows command prompt, paste the command that you copied in the previous step, and then press **Enter** to start the AzCopy command.</span></span>  <span data-ttu-id="d223d-153">Une fois que vous avez lancé la commande, les fichiers non-Microsoft 365 sont téléchargés vers l’emplacement de stockage Azure qui a été préparé à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="d223d-153">After you start the command, the non-Microsoft 365 files will be uploaded to the Azure Storage location that was prepared in step 4.</span></span>

   ![Importation non Microsoft 365 : AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="d223d-155">Comme indiqué précédemment, vous devez utiliser AzCopy v8.1 pour utiliser correctement la commande fournie dans la page Télécharger **des fichiers.**</span><span class="sxs-lookup"><span data-stu-id="d223d-155">As previously stated, you must use AzCopy v8.1 to successfully use the command that's provided on the **Upload files** page.</span></span> <span data-ttu-id="d223d-156">Si la commande AzCopy fournie échoue, consultez Résoudre les problèmes [d’AzCopy dans Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="d223d-156">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

8. <span data-ttu-id="d223d-157">Revenir au Centre de sécurité & conformité, puis cliquez sur **Suivant : Traiter les fichiers** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="d223d-157">Go back to the Security & Compliance Center, and click **Next: Process files** in the wizard.</span></span>  <span data-ttu-id="d223d-158">Cette opération initie le traitement, l’extraction de texte et l’indexation des fichiers non-Microsoft 365 qui ont été téléchargés vers l’emplacement de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="d223d-158">This initiates processing, text extraction, and indexing of the non-Microsoft 365 files that were uploaded to the Azure Storage location.</span></span>  

9. <span data-ttu-id="d223d-159">Suivez la progression du traitement des fichiers dans  la **page** Processus ou sous l’onglet Travaux en visualisation d’un travail nommé Ajout de données **non-Microsoft 365** à un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="d223d-159">Track the progress of processing the files on the **Process files** page or on the **Jobs** tab by viewing a job named **Adding non-Microsoft 365 data to a review set**.</span></span>  <span data-ttu-id="d223d-160">Une fois le travail terminé, les nouveaux fichiers sont disponibles dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="d223d-160">After the job is finished, the new files will be available in the review set.</span></span>

   ![Importation non-Microsoft 365 : traiter les fichiers](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. <span data-ttu-id="d223d-162">Une fois le traitement terminé, vous pouvez fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="d223d-162">After the processing is finished, you can close the wizard.</span></span>