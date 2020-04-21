---
title: Détection de virus dans SharePoint Online
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
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
description: Découvrez la protection antivirus dans SharePoint Online.
ms.openlocfilehash: f04cd18bb4880ab631816c90b4976beada436225
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43630940"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="4f81f-103">Détection de virus dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="4f81f-103">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="4f81f-104">Microsoft 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4f81f-104">Microsoft 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online.</span></span> <span data-ttu-id="4f81f-105">Les fichiers peuvent être analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="4f81f-105">Files may be scanned for viruses after they are uploaded.</span></span> <span data-ttu-id="4f81f-106">Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.</span><span class="sxs-lookup"><span data-stu-id="4f81f-106">If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f81f-107">Ces fonctionnalités antivirus dans SharePoint Online sont un moyen de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="4f81f-107">These antivirus capabilities in SharePoint Online are a way to contain viruses.</span></span> <span data-ttu-id="4f81f-108">Ils ne sont pas destinés à être utilisés comme point de défense unique contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="4f81f-108">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="4f81f-109">Nous encourageons tous les clients à évaluer et à mettre en œuvre une protection contre les programmes malveillants à différentes couches et à appliquer les meilleures pratiques pour sécuriser votre infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4f81f-109">We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure.</span></span> <span data-ttu-id="4f81f-110">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez la rubrique [Security Roadmap](security-roadmap.md).</span><span class="sxs-lookup"><span data-stu-id="4f81f-110">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="4f81f-111">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="4f81f-111">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="4f81f-112">Microsoft 365 utilise un moteur de détection de virus courant.</span><span class="sxs-lookup"><span data-stu-id="4f81f-112">Microsoft 365 uses a common virus detection engine.</span></span> <span data-ttu-id="4f81f-113">Le moteur s’exécute de façon asynchrone au sein de SharePoint Online et analyse certains fichiers après leur chargement.</span><span class="sxs-lookup"><span data-stu-id="4f81f-113">The engine runs asynchronously within SharePoint Online, and scans some files after they're uploaded.</span></span> <span data-ttu-id="4f81f-114">Les heuristiques sont utilisées pour déterminer quels fichiers sont analysés.</span><span class="sxs-lookup"><span data-stu-id="4f81f-114">Heuristics are used to determine which files are scanned.</span></span> <span data-ttu-id="4f81f-115">Lorsqu’un fichier contient un virus, il est signalé de sorte qu’il ne puisse pas être téléchargé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="4f81f-115">When a file is found to contain a virus, it's flagged so that it can't be downloaded again.</span></span> <span data-ttu-id="4f81f-116">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="4f81f-116">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="4f81f-117">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="4f81f-117">Here's what happens:</span></span>

1. <span data-ttu-id="4f81f-118">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4f81f-118">A user uploads a file to SharePoint Online.</span></span>

2. <span data-ttu-id="4f81f-119">SharePoint Online détermine si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="4f81f-119">SharePoint Online determines whether the file meets the criteria for a scan.</span></span>

3. <span data-ttu-id="4f81f-120">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="4f81f-120">The virus detection engine scans the file.</span></span>

4. <span data-ttu-id="4f81f-121">Si un virus est détecté, le moteur antivirus définit une propriété sur le fichier qui indique qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="4f81f-121">If a virus is found, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="4f81f-122">Que se passe-t-il lorsqu’un utilisateur essaie de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="4f81f-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="4f81f-123">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide du navigateur.</span><span class="sxs-lookup"><span data-stu-id="4f81f-123">If a file is infected, users can't download the file from SharePoint Online by using the browser.</span></span>

<span data-ttu-id="4f81f-124">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="4f81f-124">Here's what happens:</span></span>

1. <span data-ttu-id="4f81f-125">Un utilisateur ouvre un navigateur Web et essaie de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4f81f-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>

2. <span data-ttu-id="4f81f-126">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="4f81f-126">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="4f81f-127">L’utilisateur a la possibilité de télécharger le fichier et d’essayer de le nettoyer à l’aide de son propre logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="4f81f-127">The user is given the option to download the file and attempt to clean it using their own antivirus software.</span></span>

> [!NOTE]
> <span data-ttu-id="4f81f-128">Vous pouvez utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger un fichier infecté, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="4f81f-128">You can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading an infected file, even in the anti-virus warning window.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="4f81f-129">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="4f81f-129">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="4f81f-130">Que les utilisateurs synchronisent des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive. exe) ou le client de synchronisation OneDrive entreprise précédent (Groove. exe), si un fichier contient un virus, le client de synchronisation ne le télécharge pas.</span><span class="sxs-lookup"><span data-stu-id="4f81f-130">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it.</span></span> <span data-ttu-id="4f81f-131">Le client de synchronisation affiche une notification indiquant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="4f81f-131">The sync client will display a notification that the file can't be synced.</span></span>
