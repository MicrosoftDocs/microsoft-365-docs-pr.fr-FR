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
description: Découvrez comment SharePoint Online détecte les virus dans les fichiers que les utilisateurs téléchargent et empêche les utilisateurs de télécharger ou de synchroniser les fichiers.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: f6bfc23ca4120122ecfa44ad4d39795fed22af84
ms.sourcegitcommit: 583fd1ac1f385c58b93bda648907a1bd8e0a1950
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2020
ms.locfileid: "45429919"
---
# <a name="virus-detection-in-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="5069c-103">Détection de virus dans SharePoint Online, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="5069c-103">Virus detection in SharePoint Online, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="5069c-104">Microsoft 365 peut aider à protéger votre environnement contre les programmes malveillants en détectant les virus dans les fichiers que les utilisateurs téléchargent sur SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5069c-104">Microsoft 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="5069c-105">Les fichiers peuvent être analysés pour détecter d’éventuels virus une fois qu’ils ont été téléchargés.</span><span class="sxs-lookup"><span data-stu-id="5069c-105">Files may be scanned for viruses after they are uploaded.</span></span> <span data-ttu-id="5069c-106">Si un fichier est infecté, une propriété est définie de sorte que les utilisateurs ne puissent pas télécharger ou synchroniser le fichier.</span><span class="sxs-lookup"><span data-stu-id="5069c-106">If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5069c-107">Ces fonctionnalités antivirus dans SharePoint Online sont un moyen de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="5069c-107">These antivirus capabilities in SharePoint Online are a way to contain viruses.</span></span> <span data-ttu-id="5069c-108">Ils ne sont pas destinés à être utilisés comme point de défense unique contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="5069c-108">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="5069c-109">Nous encourageons tous les clients à évaluer et à mettre en œuvre une protection contre les programmes malveillants à différentes couches et à appliquer les meilleures pratiques pour sécuriser votre infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5069c-109">We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure.</span></span> <span data-ttu-id="5069c-110">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez la rubrique [Security Roadmap](security-roadmap.md).</span><span class="sxs-lookup"><span data-stu-id="5069c-110">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="5069c-111">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="5069c-111">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="5069c-112">Microsoft 365 utilise un moteur de détection de virus courant.</span><span class="sxs-lookup"><span data-stu-id="5069c-112">Microsoft 365 uses a common virus detection engine.</span></span> <span data-ttu-id="5069c-113">Le moteur s’exécute de façon asynchrone au sein de SharePoint Online et analyse certains fichiers après leur chargement.</span><span class="sxs-lookup"><span data-stu-id="5069c-113">The engine runs asynchronously within SharePoint Online, and scans some files after they're uploaded.</span></span> <span data-ttu-id="5069c-114">Les heuristiques sont utilisées pour déterminer quels fichiers sont analysés.</span><span class="sxs-lookup"><span data-stu-id="5069c-114">Heuristics are used to determine which files are scanned.</span></span> <span data-ttu-id="5069c-115">Lorsqu’un fichier contient un virus, il est signalé de sorte qu’il ne puisse pas être téléchargé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="5069c-115">When a file is found to contain a virus, it's flagged so that it can't be downloaded again.</span></span> <span data-ttu-id="5069c-116">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="5069c-116">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="5069c-117">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="5069c-117">Here's what happens:</span></span>

1. <span data-ttu-id="5069c-118">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="5069c-118">A user uploads a file to SharePoint Online.</span></span>

2. <span data-ttu-id="5069c-119">SharePoint Online détermine si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="5069c-119">SharePoint Online determines whether the file meets the criteria for a scan.</span></span>

3. <span data-ttu-id="5069c-120">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="5069c-120">The virus detection engine scans the file.</span></span>

4. <span data-ttu-id="5069c-121">Si un virus est détecté, le moteur antivirus définit une propriété sur le fichier qui indique qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="5069c-121">If a virus is found, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="5069c-122">Que se passe-t-il lorsqu’un utilisateur essaie de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="5069c-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="5069c-123">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide du navigateur.</span><span class="sxs-lookup"><span data-stu-id="5069c-123">If a file is infected, users can't download the file from SharePoint Online by using the browser.</span></span>

<span data-ttu-id="5069c-124">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="5069c-124">Here's what happens:</span></span>

1. <span data-ttu-id="5069c-125">Un utilisateur ouvre un navigateur Web et essaie de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="5069c-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>

2. <span data-ttu-id="5069c-126">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="5069c-126">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="5069c-127">L’utilisateur a la possibilité de télécharger le fichier et d’essayer de le nettoyer à l’aide de son propre logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="5069c-127">The user is given the option to download the file and attempt to clean it using their own antivirus software.</span></span>

> [!NOTE]
> 
> <span data-ttu-id="5069c-128">Vous pouvez utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger un fichier infecté, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="5069c-128">You can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading an infected file, even in the anti-virus warning window.</span></span>
> 
> <span data-ttu-id="5069c-129">N’oubliez pas non plus, dès que vous activez le paramètre *DisallowInfectedFileDownload* , l’accès aux fichiers détectés/bloqués est totalement bloqué pour les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="5069c-129">Also keep in mind, that as soon as you enable the *DisallowInfectedFileDownload* parameter, access to the detected/blocked files is completly blocked for users and administrators.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="5069c-130">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="5069c-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="5069c-131">Si les utilisateurs synchronisent des fichiers avec le nouveau client de synchronisation OneDrive (OneDrive.exe) ou le client de synchronisation OneDrive entreprise précédent (Groove.exe), si un fichier contient un virus, le client de synchronisation ne le télécharge pas.</span><span class="sxs-lookup"><span data-stu-id="5069c-131">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it.</span></span> <span data-ttu-id="5069c-132">Le client de synchronisation affiche une notification indiquant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="5069c-132">The sync client will display a notification that the file can't be synced.</span></span>

## <a name="extended-capabilities-with-office-365-atp"></a><span data-ttu-id="5069c-133">Fonctionnalités étendues avec la protection avancée contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="5069c-133">Extended capabilities with Office 365 ATP</span></span>

<span data-ttu-id="5069c-134">Les clients ayant activé la protection avancée contre les menaces Office 365 pour SharePoint, OneDrive et Microsoft teams activent la mise à [niveau pour SharePoint, onedrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md) sont en mesure d’utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine pour les détections AV et ATP.</span><span class="sxs-lookup"><span data-stu-id="5069c-134">Customers who enabled Office 365 ATP for Sharepoint, OneDrive, and Microsoft Teams [Turn on ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md) are able to use the Security & Compliance Center to manage quarantined files for AV and ATP detections.</span></span> <span data-ttu-id="5069c-135">[ATP uniquement : utilisez le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine](manage-quarantined-messages-and-files.md#atp-only-use-the-security--compliance-center-to-manage-quarantined-files).</span><span class="sxs-lookup"><span data-stu-id="5069c-135">[ATP Only: Use the Security & Compliance Center to manage quarantined files](manage-quarantined-messages-and-files.md#atp-only-use-the-security--compliance-center-to-manage-quarantined-files).</span></span>

## <a name="more-information"></a><span data-ttu-id="5069c-136">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5069c-136">More information</span></span>

<span data-ttu-id="5069c-137">Pour plus d’informations sur la configuration de l’antivirus SharePoint Online, voir se [protéger contre les menaces](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats?view=o365-worldwide#requirements) et activer la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](https://docs.microsoft.com/microsoft-365/security/office-365-security/turn-on-atp-for-spo-odb-and-teams?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="5069c-137">See [Protect against threats](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats?view=o365-worldwide#requirements) and [Turn on ATP for SharePoint, OneDrive, and Microsoft Teams](https://docs.microsoft.com/microsoft-365/security/office-365-security/turn-on-atp-for-spo-odb-and-teams?view=o365-worldwide) for more information on how to configure SharePoint Online antivirus.</span></span>


