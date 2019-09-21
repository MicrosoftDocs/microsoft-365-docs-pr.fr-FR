---
title: Charger des données autres qu’Office 365 dans un jeu à réviser
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
description: Importer des données non-Office 365 vers un jeu de réexamen dans un cas avancé de découverte électronique.
ms.openlocfilehash: 508346c3fe3a8f67addfed4ced08693daa2d49e7
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079433"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="88d9a-103">Charger des données autres qu’Office 365 dans un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="88d9a-103">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="88d9a-104">Tous les documents que vous devez analyser dans Advanced eDiscovery sont situés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="88d9a-104">Not all documents that you need to analyze in Advanced eDiscovery are located in Office 365.</span></span> <span data-ttu-id="88d9a-105">Avec la fonctionnalité d’importation de données non-Office 365 dans Advanced eDiscovery, vous pouvez télécharger des documents qui ne se trouvent pas dans Office 365 vers un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="88d9a-105">With the non-Office 365 data import feature in Advanced eDiscovery, you can upload documents that aren't located in Office 365 to a review set.</span></span> <span data-ttu-id="88d9a-106">Cet article vous explique comment mettre vos documents autres que Office 365 dans Advanced eDiscovery pour analyse.</span><span class="sxs-lookup"><span data-stu-id="88d9a-106">This article shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="88d9a-107">Advanced eDiscovery nécessite un abonnement Microsoft 365 ou Office 365 E5 pour votre organisation ou un abonnement E3 avec l’abonnement de complément de conformité avancé.</span><span class="sxs-lookup"><span data-stu-id="88d9a-107">Advanced eDiscovery requires an Microsoft 365 or Office 365 E5 subscription for your organization or an E3 subscription with the Advanced Compliance add-on subscription.</span></span> <span data-ttu-id="88d9a-108">Si vous ne disposez pas de ce plan et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="88d9a-108">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="88d9a-109">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="88d9a-109">Before you begin</span></span>

<span data-ttu-id="88d9a-110">L’utilisation de la fonctionnalité de téléchargement non-Office 365 décrite dans cet article requiert les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="88d9a-110">Using the upload non-Office 365 feature described in this article requires that you have the following:</span></span>

- <span data-ttu-id="88d9a-111">Tous les dépositaires auxquels vous souhaitez associer un contenu non-Office 365 doivent se voir attribuer une licence E5 ou une licence E3 avec une licence de module complémentaire de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="88d9a-111">All custodians that you want to associate non-Office 365 content to must be assigned an E5 license, or an E3 license with an Advanced Compliance add-on license.</span></span>

- <span data-ttu-id="88d9a-112">Un cas de découverte électronique avancé existant.</span><span class="sxs-lookup"><span data-stu-id="88d9a-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="88d9a-113">Les dépositaires doivent être ajoutés à l’incident avant de pouvoir télécharger et d’associer les données non Office 365.</span><span class="sxs-lookup"><span data-stu-id="88d9a-113">Custodians must be added to the case before you can upload and associate the non-Office 365 data to them.</span></span>

- <span data-ttu-id="88d9a-114">Les données non-Office 365 doivent être un type de fichier pris en charge par Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="88d9a-114">Non-Office 365 data must be a file type that's supported by Advanced eDiscovery.</span></span> <span data-ttu-id="88d9a-115">Pour plus d’informations, consultez la rubrique [types de fichiers pris en charge dans Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="88d9a-115">For more information, see [Supported file types in Advanced eDiscovery](supported-filetypes-ediscovery20.md).</span></span>

- <span data-ttu-id="88d9a-116">Tous les fichiers téléchargés vers un jeu de révision doivent se trouver dans des dossiers, où chaque dossier est associé à un dépositaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="88d9a-116">All files that are uploaded to a review set must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="88d9a-117">Les noms de ces dossiers doivent utiliser le format d’affectation de noms suivant : *alias @ NomDomaine*.</span><span class="sxs-lookup"><span data-stu-id="88d9a-117">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="88d9a-118">L’alias @ DomainName doit être l’alias et le domaine Office 365 de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88d9a-118">The alias@domainname must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="88d9a-119">Vous pouvez collecter tous les dossiers alias @ NomDomaine dans un dossier racine.</span><span class="sxs-lookup"><span data-stu-id="88d9a-119">You can collect all the alias@domainname folders in a root folder.</span></span> <span data-ttu-id="88d9a-120">Le dossier racine ne peut contenir que les dossiers alias @ NomDomaine.</span><span class="sxs-lookup"><span data-stu-id="88d9a-120">The root folder can only contain the alias@domainname folders.</span></span> <span data-ttu-id="88d9a-121">Les fichiers libres dans le dossier racine ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="88d9a-121">Loose files in the root folder aren't supported.</span></span>

   <span data-ttu-id="88d9a-122">La structure de dossiers pour les données non-Office 365 que vous souhaitez télécharger serait semblable à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="88d9a-122">The folder structure for the non-Office 365 data that you want to upload would be similar to the following example:</span></span>

   - <span data-ttu-id="88d9a-123">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="88d9a-123">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="88d9a-124">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="88d9a-124">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="88d9a-125">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="88d9a-125">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="88d9a-126">Où abraham.mcmahon@contoso.com, jewell.gordon@contoso.com et staci.gonzalez@contoso.com sont les adresses SMTP des dépositaires dans le cas.</span><span class="sxs-lookup"><span data-stu-id="88d9a-126">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Structure de dossier de téléchargement de données non Office 365](media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="88d9a-128">Un compte qui est affecté au groupe de rôles gestionnaire eDiscovery (et ajouté en tant qu’administrateur eDiscovery).</span><span class="sxs-lookup"><span data-stu-id="88d9a-128">An account that is assigned to the eDiscovery Manager role group (and added as eDiscovery Administrator).</span></span>

- <span data-ttu-id="88d9a-129">L’outil AzCopy v 8.1 installé sur un ordinateur ayant accès à la structure de dossiers de contenu non Office 365.</span><span class="sxs-lookup"><span data-stu-id="88d9a-129">The AzCopy v8.1 tool installed on a computer that has access to the non-Office 365 content folder structure.</span></span> <span data-ttu-id="88d9a-130">Pour installer AzCopy, consultez [la rubrique transférer des données avec le AzCopy v 8.1 sous Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="88d9a-130">To install AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="88d9a-131">Veillez à installer AzCopy à l’emplacement par défaut, à savoir **% ProgramFiles (x86)% \ Microsoft SDKs\Azure\AzCopy**.</span><span class="sxs-lookup"><span data-stu-id="88d9a-131">Be sure to install AzCopy in the default location, which is **%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy**.</span></span> <span data-ttu-id="88d9a-132">Vous devez utiliser AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="88d9a-132">You must use AzCopy v8.1.</span></span> <span data-ttu-id="88d9a-133">Il se peut que d’autres versions de AzCopy ne fonctionnent pas lors du chargement de données non-Office 365 dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="88d9a-133">Other versions of AzCopy may not work when loading non-Office 365 data in Advanced eDiscovery.</span></span>


## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="88d9a-134">Chargement de contenu non-Office 365 dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="88d9a-134">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="88d9a-135">En tant que gestionnaire eDiscovery ou administrateur eDiscovery, ouvrez Advanced eDiscovery, puis le cas où les données non Office 365 seront téléchargées vers.</span><span class="sxs-lookup"><span data-stu-id="88d9a-135">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  

2. <span data-ttu-id="88d9a-136">Cliquez sur **réviser les ensembles**, puis sélectionnez le jeu de révision pour lequel télécharger les données non Office 365.</span><span class="sxs-lookup"><span data-stu-id="88d9a-136">Click **Review sets**, and then select the review set to upload the non-Office 365 data to.</span></span>  <span data-ttu-id="88d9a-137">Si vous n’avez pas d’ensemble de révision, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="88d9a-137">If you don't have a review set, you can create one.</span></span> 
 
3. <span data-ttu-id="88d9a-138">Dans l’ensemble de révision, cliquez sur **gérer l’ensemble de révisions**, puis sur **afficher les téléchargements** dans la vignette **données autres que Office 365** .</span><span class="sxs-lookup"><span data-stu-id="88d9a-138">In the review set, click **Manage review set**, and then click **View uploads** on the **Non-Office 365 data** tile.</span></span>

4. <span data-ttu-id="88d9a-139">Cliquez sur **Télécharger les fichiers** pour démarrer l’Assistant importation de données autres que Office 365.</span><span class="sxs-lookup"><span data-stu-id="88d9a-139">Click **Upload files** to start the Non-Office 365 data import wizard.</span></span>

   ![Charger des fichiers](media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

   <span data-ttu-id="88d9a-141">La première étape de l’Assistant prépare un emplacement de stockage Azure sécurisé fourni par Microsoft pour télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="88d9a-141">The first step in the wizard prepares a secure Microsoft-provided Azure Storage location to upload the files to.</span></span>  <span data-ttu-id="88d9a-142">Une fois la préparation terminée, le bouton **suivant : charger les fichiers** devient actif.</span><span class="sxs-lookup"><span data-stu-id="88d9a-142">When the preparation is completed, the **Next: Upload files** button becomes active.</span></span>

   ![Non-Office 365 Import : prepare](media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
5. <span data-ttu-id="88d9a-144">Cliquez sur **suivant : charger les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="88d9a-144">Click **Next: Upload files**.</span></span>

6. <span data-ttu-id="88d9a-145">Sur la page **Télécharger les fichiers** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="88d9a-145">On the **Upload files** page, do the following:</span></span>

   ![Importation non Office 365 : Télécharger des fichiers](media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   <span data-ttu-id="88d9a-147">a.</span><span class="sxs-lookup"><span data-stu-id="88d9a-147">a.</span></span> <span data-ttu-id="88d9a-148">Dans la zone **chemin d’accès à l’emplacement des fichiers** , vérifiez ou tapez l’emplacement du dossier racine dans lequel vous avez stocké les données non Office 365 que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="88d9a-148">In the **Path to location of files** box, verify or type the location of the root folder where you've stored the non-Office 365 data you want to upload.</span></span> <span data-ttu-id="88d9a-149">Par exemple, pour l’emplacement des fichiers d’exemple présentés dans la **section avant de commencer**, vous devez taper **%USERPROFILE\Downloads\nonO365**.</span><span class="sxs-lookup"><span data-stu-id="88d9a-149">For example, for the location of the example files shown in the **Before you begin section**, you would type **%USERPROFILE\Downloads\nonO365**.</span></span> <span data-ttu-id="88d9a-150">La fourniture de l’emplacement correct garantit que la commande AzCopy affichée dans la zone sous le chemin est correctement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="88d9a-150">Providing the correct location ensures the AzCopy command displayed in box under the path is properly updated.</span></span>

   <span data-ttu-id="88d9a-151">b.</span><span class="sxs-lookup"><span data-stu-id="88d9a-151">b.</span></span> <span data-ttu-id="88d9a-152">Cliquez sur **copier dans le presse-papiers** pour copier la commande affichée dans la zone.</span><span class="sxs-lookup"><span data-stu-id="88d9a-152">Click **Copy to clipboard** to copy the command that is displayed in the box.</span></span>

7. <span data-ttu-id="88d9a-153">Démarrez une invite de commandes Windows, collez la commande que vous avez copiée à l’étape précédente, puis appuyez sur **entrée** pour démarrer la commande AzCopy.</span><span class="sxs-lookup"><span data-stu-id="88d9a-153">Start a Windows command prompt, paste the command that you copied in the previous step, and then press **Enter** to start the AzCopy command.</span></span>  <span data-ttu-id="88d9a-154">Une fois que vous avez démarré la commande, les fichiers non-Office 365 sont téléchargés vers l’emplacement de stockage Azure préparé à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="88d9a-154">After you start the command, the non-Office 365 files will be uploaded to the Azure Storage location that was prepared in step 4.</span></span>

   ![Importation non-Office 365 : AzCopy](media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="88d9a-156">Comme indiqué précédemment, vous devez utiliser AzCopy v 8.1 pour utiliser correctement la commande fournie dans la page **Télécharger les fichiers** .</span><span class="sxs-lookup"><span data-stu-id="88d9a-156">As previously stated, you must use AzCopy v8.1 to successfully use the command that's provided on the **Upload files** page.</span></span> <span data-ttu-id="88d9a-157">Si la commande AzCopy fournie échoue, reportez-vous à la rubrique [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="88d9a-157">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

8. <span data-ttu-id="88d9a-158">Revenez dans le centre de sécurité & conformité, puis cliquez sur **suivant : traiter les fichiers** dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="88d9a-158">Go back to the Security & Compliance Center, and click **Next: Process files** in the wizard.</span></span>  <span data-ttu-id="88d9a-159">Cela lance le traitement, l’extraction de texte et l’indexation des fichiers non-Office 365 qui ont été téléchargés vers l’emplacement de stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="88d9a-159">This initiates processing, text extraction, and indexing of the non-Office 365 files that were uploaded to the Azure Storage location.</span></span>  

9. <span data-ttu-id="88d9a-160">Effectuez le suivi de la progression du traitement des fichiers non-Office 365 sur la page des **fichiers de processus** ou sur l’onglet **travaux** en affichant un travail nommé **ajout de données non Office 365 à un jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="88d9a-160">Track the progress of processing the non-Office 365 files on the **Process files** page or on the **Jobs** tab by viewing a job named **Adding non-Office 365 data to a review set**.</span></span>  <span data-ttu-id="88d9a-161">Une fois le travail terminé, les nouveaux fichiers seront disponibles dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="88d9a-161">After the job is finished, the new files will be available in the review set.</span></span>

   ![Importation non Office 365 : fichiers de processus](media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

10. <span data-ttu-id="88d9a-163">Une fois le traitement terminé, vous pouvez fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="88d9a-163">After the processing is finished, you can close the wizard.</span></span>