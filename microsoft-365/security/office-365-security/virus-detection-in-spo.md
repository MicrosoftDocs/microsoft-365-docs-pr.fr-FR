---
title: Détection de virus dans SharePoint Online
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 01/14/2019
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Office 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online. Les fichiers sont analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés. Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.
ms.openlocfilehash: 60dc2cbd1b2d248f13c2b8c32738c4f195d6a7a0
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079952"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="6d37d-105">Détection de virus dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6d37d-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="6d37d-106">Office 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6d37d-106">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online.</span></span> <span data-ttu-id="6d37d-107">Les fichiers sont analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="6d37d-107">Files are scanned for viruses after they are uploaded.</span></span> <span data-ttu-id="6d37d-108">Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.</span><span class="sxs-lookup"><span data-stu-id="6d37d-108">If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6d37d-109">Ces fonctionnalités antivirus dans SharePoint Online sont un moyen de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="6d37d-109">These antivirus capabilities in SharePoint Online are a way to contain viruses.</span></span> <span data-ttu-id="6d37d-110">Ils ne sont pas destinés à être utilisés comme point de défense unique contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6d37d-110">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="6d37d-111">Nous encourageons tous les clients à évaluer et à mettre en œuvre une protection contre les programmes malveillants à différentes couches et à appliquer les meilleures pratiques pour sécuriser votre infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="6d37d-111">We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure.</span></span> <span data-ttu-id="6d37d-112">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez la rubrique [Security Roadmap](security-roadmap.md).</span><span class="sxs-lookup"><span data-stu-id="6d37d-112">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="6d37d-113">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="6d37d-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="6d37d-114">Office 365 utilise un moteur de détection de virus courant.</span><span class="sxs-lookup"><span data-stu-id="6d37d-114">Office 365 uses a common virus detection engine.</span></span> <span data-ttu-id="6d37d-115">Le moteur s’exécute de façon asynchrone au sein de SharePoint Online et analyse les fichiers après leur chargement.</span><span class="sxs-lookup"><span data-stu-id="6d37d-115">The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded.</span></span> <span data-ttu-id="6d37d-116">Lorsqu’un fichier contient un virus, il est signalé de sorte qu’il ne puisse pas être téléchargé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="6d37d-116">When a file is found to contain a virus, it's flagged so that it can't be downloaded again.</span></span> <span data-ttu-id="6d37d-117">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="6d37d-117">In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="6d37d-118">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="6d37d-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="6d37d-119">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6d37d-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="6d37d-120">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="6d37d-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="6d37d-121">Si un virus est détecté, le moteur antivirus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="6d37d-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="6d37d-122">Que se passe-t-il lorsqu’un utilisateur essaie de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="6d37d-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="6d37d-123">Si un fichier est infecté par un virus, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6d37d-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="6d37d-124">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="6d37d-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="6d37d-125">Un utilisateur ouvre un navigateur Web et essaie de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6d37d-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="6d37d-126">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="6d37d-126">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="6d37d-127">L’utilisateur a la possibilité de télécharger le fichier et d’essayer de le nettoyer à l’aide de son propre logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="6d37d-127">The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="6d37d-128">Vous pouvez utiliser la cmdlet Set-SPOTenant avec le paramètre **DisallowInfectedFileDownload** pour empêcher les utilisateurs de télécharger un fichier détecté, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="6d37d-128">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window.</span></span> <span data-ttu-id="6d37d-129">Consultez la rubrique [DisallowInfectedFileDownloadhttps://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)] (.</span><span class="sxs-lookup"><span data-stu-id="6d37d-129">See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="6d37d-130">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="6d37d-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="6d37d-131">Que les utilisateurs synchronisent des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive. exe) ou le client de synchronisation OneDrive entreprise précédent (Groove. exe), si un fichier contient un virus, le client de synchronisation ne le télécharge pas.</span><span class="sxs-lookup"><span data-stu-id="6d37d-131">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it.</span></span> <span data-ttu-id="6d37d-132">Le client de synchronisation affiche une notification indiquant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="6d37d-132">The sync client will display a notification that the file can't be synced.</span></span>
  

