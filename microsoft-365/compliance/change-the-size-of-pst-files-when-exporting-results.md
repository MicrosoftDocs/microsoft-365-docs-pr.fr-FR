---
title: Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Vous pouvez modifier la taille par défaut des fichiers PST téléchargés sur votre ordinateur lorsque vous exportez les résultats de recherche de découverte électronique.
ms.openlocfilehash: 82a3d80cae04cd8d08b126c800ec2b4a1995f262
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078852"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="8d8e4-103">Modifier la taille des fichiers PST lors de l’exportation des résultats de recherche eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8d8e4-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="8d8e4-104">Lorsque vous utilisez l’outil d’exportation de découverte électronique Office 365 pour exporter les résultats du courrier électronique d’une recherche de découverte électronique à partir des différents outils eDiscovery de Microsoft, la taille par défaut d’un fichier PST pouvant être exporté est de 10 Go.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-104">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB.</span></span> <span data-ttu-id="8d8e4-105">Si vous souhaitez modifier cette taille par défaut, vous pouvez modifier le Registre Windows sur l’ordinateur que vous utilisez pour exporter les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-105">If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results.</span></span> <span data-ttu-id="8d8e4-106">L’une des raisons pour y parvenir est qu’un fichier PST peut tenir sur un support amovible, un DVD, un disque compact ou un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-106">One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="8d8e4-107">L’outil d’exportation de découverte électronique Office 365 est utilisé pour exporter les résultats de la recherche lors de l’utilisation de l’outil de recherche de contenu dans le centre de sécurité et de conformité, la découverte électronique inaltérable dans Exchange Online et le centre eDiscovery dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-107">The Office 365 eDiscovery Export tool is used to export the search results when using the Content Search tool in the security and compliance center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="8d8e4-108">Créer un paramètre de Registre pour modifier la taille des fichiers PST lors de l’exportation des résultats de recherche de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="8d8e4-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="8d8e4-109">Effectuez la procédure suivante sur l’ordinateur que vous allez utiliser pour exporter les résultats d’une recherche de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="8d8e4-110">Fermez l’outil d’exportation eDiscovery d’Office 365 s’il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="8d8e4-111">Enregistrez le texte suivant dans un fichier de Registre Windows à l’aide d’un suffixe de nom de fichier. reg ; par exemple, PstExportSize. reg.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="8d8e4-112">Dans l’exemple ci-dessus `PstSizeLimitInBytes` , la valeur est définie sur 1 073 741 824 octets ou environ 1 Go.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-112">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB.</span></span> <span data-ttu-id="8d8e4-113">Voici d’autres exemples de valeurs pour le `PstSizeLimitInBytes` paramètre.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-113">Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="8d8e4-114">**Taille en Go (env.)**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="8d8e4-115">**Taille en octets**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="8d8e4-116">.7 GO (700 MO)</span><span class="sxs-lookup"><span data-stu-id="8d8e4-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="8d8e4-117">751619277</span><span class="sxs-lookup"><span data-stu-id="8d8e4-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="8d8e4-118">2 Go</span><span class="sxs-lookup"><span data-stu-id="8d8e4-118">2 GB</span></span>  <br/> |<span data-ttu-id="8d8e4-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="8d8e4-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="8d8e4-120">4 Go</span><span class="sxs-lookup"><span data-stu-id="8d8e4-120">4 GB</span></span>  <br/> |<span data-ttu-id="8d8e4-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="8d8e4-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="8d8e4-122">8 Go</span><span class="sxs-lookup"><span data-stu-id="8d8e4-122">8 GB</span></span>  <br/> |<span data-ttu-id="8d8e4-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="8d8e4-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="8d8e4-124">Remplacez la `PstSizeLimitInBytes` valeur par la taille maximale de fichier PST souhaitée lorsque vous exportez les résultats de la recherche, puis enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="8d8e4-125">Dans l’Explorateur Windows, cliquez ou double-cliquez sur le fichier. reg que vous avez créé au cours des étapes précédentes.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="8d8e4-126">Dans la fenêtre contrôle d’accès des utilisateurs, cliquez sur **Oui** pour permettre à l’éditeur du registre de procéder à la modification.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="8d8e4-127">Lorsque vous êtes invité à continuer, cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="8d8e4-128">L’éditeur du Registre affiche un message indiquant que le paramètre a été ajouté avec succès au registre.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="8d8e4-129">Vous pouvez répéter les étapes 3-6 pour modifier la valeur du `PstSizeLimitInBytes` paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="8d8e4-130">Forum aux questions sur la modification de la taille par défaut des fichiers PST lors de l’exportation des résultats de recherche de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="8d8e4-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="8d8e4-131">**Pourquoi la taille par défaut est-elle de 10 Go ?**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="8d8e4-132">La taille par défaut de 10 Go était basée sur les commentaires des clients ; 10 Go constitue un bon équilibre entre la quantité optimale de contenu dans un seul fichier PST et une probabilité minimale d’endommagement des fichiers.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="8d8e4-133">**Dois-je augmenter ou réduire la taille par défaut des fichiers PST ?**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="8d8e4-134">Les clients ont tendance à réduire la limite de taille afin que les résultats de la recherche tiennent sur des supports amovibles qu’ils peuvent physiquement fournir à d’autres emplacements de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-134">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization.</span></span> <span data-ttu-id="8d8e4-135">Il n’est pas recommandé d’augmenter la taille par défaut, car les fichiers PST de plus de 10 Go peuvent présenter des problèmes d’endommagement.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-135">We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="8d8e4-136">**Sur quel ordinateur dois-je effectuer cette opération ?**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="8d8e4-137">Vous devez modifier le paramètre de Registre sur tout ordinateur local sur lequel vous exécutez l’outil d’exportation de découverte électronique Office 365.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="8d8e4-138">**Après avoir modifié ce paramètre, dois-je redémarrer l’ordinateur ?**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="8d8e4-139">Non, vous n’avez pas besoin de redémarrer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-139">No, you don't have to reboot the computer.</span></span> <span data-ttu-id="8d8e4-140">Toutefois, si l’outil d’exportation eDiscovery d’Office 365 est en cours d’exécution, vous devrez le fermer et le redémarrer une fois que vous aurez modifié ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-140">But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="8d8e4-141">**Une clé de Registre existante est-elle modifiée ou une nouvelle clé est-elle créée ?**</span><span class="sxs-lookup"><span data-stu-id="8d8e4-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="8d8e4-142">Une nouvelle clé de Registre est créée lors de la première exécution du fichier. reg que vous avez créé au cours de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-142">A new registry key is created the first time you run the .reg file that you created in this procedure.</span></span> <span data-ttu-id="8d8e4-143">Le paramètre est ensuite modifié chaque fois que vous modifiez et réexécutez le fichier de modification. reg.</span><span class="sxs-lookup"><span data-stu-id="8d8e4-143">Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
