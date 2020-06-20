---
title: Désactiver les rapports lorsque vous exportez les résultats de recherche de contenu
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
ms.custom:
- seo-marvel-apr2020
description: Modifiez le Registre Windows sur votre ordinateur local pour désactiver les rapports lorsque vous exportez les résultats d’une recherche de contenu à partir du centre de sécurité & conformité.
ms.openlocfilehash: 0eaf9c9d1f70e03481b00d38d2e487709329c4cd
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817853"
---
# <a name="disable-reports-when-you-export-content-search-results"></a><span data-ttu-id="69f01-103">Désactiver les rapports lorsque vous exportez les résultats de recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="69f01-103">Disable reports when you export Content Search results</span></span>

<span data-ttu-id="69f01-104">Lorsque vous utilisez l’outil d’exportation de découverte électronique pour exporter les résultats d’une recherche de contenu dans le centre de sécurité & conformité, l’outil crée et exporte automatiquement deux rapports contenant des informations supplémentaires sur le contenu exporté.</span><span class="sxs-lookup"><span data-stu-id="69f01-104">When you use the eDiscovery Export tool to export the results of a Content Search in the Security & Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content.</span></span> <span data-ttu-id="69f01-105">Ces rapports sont le fichier de Results.csv et le fichier de Manifest.xml (voir la section Forum [aux questions sur la désactivation des rapports d’exportation](#frequently-asked-questions-about-disabling-export-reports) de cette rubrique pour obtenir des descriptions détaillées de ces rapports).</span><span class="sxs-lookup"><span data-stu-id="69f01-105">These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports).</span></span> <span data-ttu-id="69f01-106">Étant donné que ces fichiers peuvent être très volumineux, vous pouvez accélérer le temps de téléchargement et économiser de l’espace disque en empêchant l’exportation de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="69f01-106">Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported.</span></span> <span data-ttu-id="69f01-107">Pour ce faire, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69f01-107">You can do this by changing the Windows Registry on the computer that you use to export the search results.</span></span> <span data-ttu-id="69f01-108">Si vous souhaitez inclure les rapports ultérieurement, vous pouvez modifier le paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="69f01-108">If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="69f01-109">Créer des paramètres de Registre pour désactiver les rapports d’exportation</span><span class="sxs-lookup"><span data-stu-id="69f01-109">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="69f01-110">Effectuez la procédure suivante sur l’ordinateur que vous allez utiliser pour exporter les résultats d’une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="69f01-110">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="69f01-111">Fermez l’outil d’exportation de découverte électronique s’il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="69f01-111">Close the eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="69f01-112">Effectuez l’une des étapes suivantes, ou les deux, en fonction de l’état d’exportation que vous souhaitez désactiver.</span><span class="sxs-lookup"><span data-stu-id="69f01-112">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="69f01-113">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="69f01-113">**Results.csv**</span></span>
    
      <span data-ttu-id="69f01-114">Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier. reg ; par exemple, DisableResultsCsv. reg.</span><span class="sxs-lookup"><span data-stu-id="69f01-114">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```text
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="69f01-115">**Manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="69f01-115">**Manifest.xml**</span></span>
    
      <span data-ttu-id="69f01-116">Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier. reg ; par exemple, DisableManifestXml. reg.</span><span class="sxs-lookup"><span data-stu-id="69f01-116">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```text
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="69f01-117">Dans l’Explorateur Windows, cliquez ou double-cliquez sur le fichier. reg que vous avez créé au cours des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="69f01-117">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="69f01-118">Dans la fenêtre contrôle d’accès des utilisateurs, cliquez sur **Oui** pour permettre à l’éditeur du registre de procéder à la modification.</span><span class="sxs-lookup"><span data-stu-id="69f01-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="69f01-119">Lorsque vous êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="69f01-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="69f01-120">L’éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.</span><span class="sxs-lookup"><span data-stu-id="69f01-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="69f01-121">Modifier les paramètres du Registre pour réactiver les rapports d’exportation</span><span class="sxs-lookup"><span data-stu-id="69f01-121">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="69f01-122">Si vous avez désactivé les rapports Results.csv et Manifest.xml en créant les fichiers. reg dans la procédure précédente, vous pouvez modifier ces fichiers pour réactiver un rapport afin de l’exporter avec les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69f01-122">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results.</span></span> <span data-ttu-id="69f01-123">À nouveau, effectuez la procédure suivante sur l’ordinateur que vous allez utiliser pour exporter les résultats d’une recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="69f01-123">Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="69f01-124">Fermez l’outil d’exportation de découverte électronique s’il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="69f01-124">Close the eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="69f01-125">Modifiez l’un des fichiers d’édition. reg que vous avez créés dans la procédure précédente ou les deux.</span><span class="sxs-lookup"><span data-stu-id="69f01-125">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="69f01-126">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="69f01-126">**Results.csv**</span></span>
    
        <span data-ttu-id="69f01-127">Ouvrez le fichier DisableResultsCsv. reg dans le bloc-notes, remplacez la valeur `False` par `True` , puis enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="69f01-127">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file.</span></span> <span data-ttu-id="69f01-128">Par exemple, après avoir modifié le fichier, il se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="69f01-128">For example, after you edit the file, it looks like this:</span></span>
    
        ```text
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="69f01-129">**Manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="69f01-129">**Manifest.xml**</span></span>
    
        <span data-ttu-id="69f01-130">Ouvrez le fichier DisableManifestXml. reg dans le bloc-notes, remplacez la valeur `False` par `True` , puis enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="69f01-130">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file.</span></span> <span data-ttu-id="69f01-131">Par exemple, après avoir modifié le fichier, il se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="69f01-131">For example, after you edit the file, it looks like this:</span></span>
    
      ```text
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="69f01-132">Dans l’Explorateur Windows, cliquez ou double-cliquez sur un fichier. reg que vous avez modifié à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="69f01-132">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="69f01-133">Dans la fenêtre contrôle d’accès des utilisateurs, cliquez sur **Oui** pour permettre à l’éditeur du registre de procéder à la modification.</span><span class="sxs-lookup"><span data-stu-id="69f01-133">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="69f01-134">Lorsque vous êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="69f01-134">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="69f01-135">L’éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.</span><span class="sxs-lookup"><span data-stu-id="69f01-135">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="69f01-136">Forum aux questions sur la désactivation des rapports d’exportation</span><span class="sxs-lookup"><span data-stu-id="69f01-136">Frequently asked questions about disabling export reports</span></span>

 <span data-ttu-id="69f01-137">**Quels sont les rapports Results.csv et Manifest.xml ?**</span><span class="sxs-lookup"><span data-stu-id="69f01-137">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="69f01-138">Les fichiers Results.csv et Manifest.xml contiennent des informations supplémentaires sur le contenu qui a été exporté.</span><span class="sxs-lookup"><span data-stu-id="69f01-138">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="69f01-139">**Results.csv** Document Excel qui contient des informations sur chaque élément téléchargé en tant que résultat de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69f01-139">**Results.csv** An Excel document that contains information about each item that is download as a search result.</span></span> <span data-ttu-id="69f01-140">Pour le courrier électronique, le journal des résultats contient des informations sur chaque message, y compris :</span><span class="sxs-lookup"><span data-stu-id="69f01-140">For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="69f01-141">l’emplacement du message dans la boîte aux lettres source (notamment si le message est dans la boîte aux lettres principale ou d’archivage) ;</span><span class="sxs-lookup"><span data-stu-id="69f01-141">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="69f01-142">la date à laquelle le message a été envoyé ou reçu ;</span><span class="sxs-lookup"><span data-stu-id="69f01-142">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="69f01-143">l’objet du message ;</span><span class="sxs-lookup"><span data-stu-id="69f01-143">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="69f01-144">l’expéditeur et les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="69f01-144">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="69f01-145">Si le message est un message en double si vous avez activé la déduplication lors de l’exportation des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69f01-145">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results.</span></span> <span data-ttu-id="69f01-146">Les messages en double comportent une valeur dans la colonne **ItemId parent** qui identifie le message en tant que doublon.</span><span class="sxs-lookup"><span data-stu-id="69f01-146">Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate.</span></span> <span data-ttu-id="69f01-147">La valeur dans la colonne **ItemId parent** est identique à la valeur de la colonne **élément DocumentID** du message qui a été exporté.</span><span class="sxs-lookup"><span data-stu-id="69f01-147">The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="69f01-148">Pour les documents provenant de sites SharePoint et OneDrive entreprise, le journal des résultats contient des informations sur chaque document, notamment :</span><span class="sxs-lookup"><span data-stu-id="69f01-148">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="69f01-149">l’URL du document ;</span><span class="sxs-lookup"><span data-stu-id="69f01-149">The URL for the document.</span></span>
    
  - <span data-ttu-id="69f01-150">l’URL de la collection de sites qui héberge le document ;</span><span class="sxs-lookup"><span data-stu-id="69f01-150">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="69f01-151">la date à laquelle le document a été modifié pour la dernière fois ;</span><span class="sxs-lookup"><span data-stu-id="69f01-151">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="69f01-152">le nom du document (qui se trouve dans la colonne Objet du journal des résultats).</span><span class="sxs-lookup"><span data-stu-id="69f01-152">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="69f01-153">**Manifest.xml** Fichier manifeste (au format XML) qui contient des informations sur chaque élément inclus dans les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69f01-153">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results.</span></span> <span data-ttu-id="69f01-154">Les informations contenues dans ce rapport sont identiques à celles du rapport de Results.csv, mais elles sont au format spécifié par le modèle de référence de découverte électronique (EDRM).</span><span class="sxs-lookup"><span data-stu-id="69f01-154">The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM).</span></span> <span data-ttu-id="69f01-155">Pour plus d’informations sur EDRM, consultez la rubrique [https://www.edrm.net](https://www.edrm.net) .</span><span class="sxs-lookup"><span data-stu-id="69f01-155">For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="69f01-156">**Quand dois-je désactiver l’exportation de ces rapports ?**</span><span class="sxs-lookup"><span data-stu-id="69f01-156">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="69f01-157">Cela dépend de vos besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="69f01-157">It depends on your specific needs.</span></span> <span data-ttu-id="69f01-158">De nombreuses organisations n’ont pas besoin d’informations supplémentaires sur les résultats de la recherche et n’ont pas besoin de ces rapports.</span><span class="sxs-lookup"><span data-stu-id="69f01-158">Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="69f01-159">**Sur quel ordinateur dois-je effectuer cette opération ?**</span><span class="sxs-lookup"><span data-stu-id="69f01-159">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="69f01-160">Vous devez modifier le paramètre de Registre sur n’importe quel ordinateur local sur lequel vous exécutez l’outil d’exportation de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="69f01-160">You have to change the registry setting on any local computer that you run the eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="69f01-161">**Après avoir modifié ce paramètre, dois-je redémarrer l’ordinateur ?**</span><span class="sxs-lookup"><span data-stu-id="69f01-161">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="69f01-162">Non, il n’est pas nécessaire de redémarrer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="69f01-162">No, you don't have to restart the computer.</span></span> <span data-ttu-id="69f01-163">Toutefois, si l’outil d’exportation de découverte électronique est en cours d’exécution, vous devez le fermer, puis le redémarrer une fois que vous avez modifié le paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="69f01-163">But if the eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="69f01-164">**Une clé de Registre existante est-elle modifiée ou une nouvelle clé est-elle créée ?**</span><span class="sxs-lookup"><span data-stu-id="69f01-164">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="69f01-165">Une nouvelle clé de Registre est créée lors de la première exécution du fichier. reg que vous avez créé dans la procédure de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="69f01-165">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic.</span></span> <span data-ttu-id="69f01-166">Le paramètre est ensuite modifié chaque fois que vous modifiez et réexécutez le fichier de modification. reg.</span><span class="sxs-lookup"><span data-stu-id="69f01-166">Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
