---
title: Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft teams
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
ms.openlocfilehash: 38d6111fe665e0af79cbd93f534b1058881ff76c
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48327986"
---
# <a name="built-in-virus-protection-in-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="cf583-103">Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="cf583-103">Built-in virus protection in SharePoint Online, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="cf583-104">Microsoft 365 utilise un moteur de détection de virus courant pour analyser les fichiers que les utilisateurs téléchargent vers SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cf583-104">Microsoft 365 uses a common virus detection engine for scanning files that users upload to SharePoint Online, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="cf583-105">Cette protection est incluse dans tous les abonnements qui incluent SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cf583-105">This protection is included with all subscriptions that include SharePoint Online, OneDrive, and Microsoft Teams.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf583-106">Les fonctionnalités anti-virus intégrées permettent de mieux comprendre les virus.</span><span class="sxs-lookup"><span data-stu-id="cf583-106">The built-in anti-virus capabilities are a way to help contain viruses.</span></span> <span data-ttu-id="cf583-107">Ils ne sont pas destinés à être utilisés comme point de défense unique contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="cf583-107">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="cf583-108">Nous encourageons tous les clients à examiner et à mettre en œuvre une protection contre les programmes malveillants à différentes couches et à appliquer les meilleures pratiques pour sécuriser leur infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="cf583-108">We encourage all customers to investigate and implement anti-malware protection at various layers and apply best practices for securing their enterprise infrastructure.</span></span> <span data-ttu-id="cf583-109">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez la rubrique [Security Roadmap](security-roadmap.md).</span><span class="sxs-lookup"><span data-stu-id="cf583-109">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="cf583-110">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="cf583-110">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="cf583-111">Le moteur de détection de virus Microsoft 365 s’exécute de façon asynchrone dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="cf583-111">The Microsoft 365 virus detection engine runs asynchronously within SharePoint Online.</span></span> <span data-ttu-id="cf583-112">**Tous les fichiers ne sont pas analysés automatiquement lors du chargement**.</span><span class="sxs-lookup"><span data-stu-id="cf583-112">**All files are not automatically scanned on upload**.</span></span> <span data-ttu-id="cf583-113">Les heuristiques déterminent les fichiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="cf583-113">Heuristics determine the files to scan.</span></span> <span data-ttu-id="cf583-114">Lorsqu’un fichier contient un virus, le fichier est marqué de manière à ce qu’il ne puisse pas être téléchargé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="cf583-114">When a file is found to contain a virus, the file is flagged so it can't be downloaded again.</span></span> <span data-ttu-id="cf583-115">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="cf583-115">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="cf583-116">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="cf583-116">Here's what happens:</span></span>

1. <span data-ttu-id="cf583-117">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="cf583-117">A user uploads a file to SharePoint Online.</span></span>
2. <span data-ttu-id="cf583-118">SharePoint Online détermine si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="cf583-118">SharePoint Online determines whether the file meets the criteria for a scan.</span></span>
3. <span data-ttu-id="cf583-119">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="cf583-119">The virus detection engine scans the file.</span></span>
4. <span data-ttu-id="cf583-120">Si un virus est détecté, le moteur antivirus définit une propriété sur le fichier qui indique qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="cf583-120">If a virus is found, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="cf583-121">Que se passe-t-il lorsqu’un utilisateur essaie de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="cf583-121">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="cf583-122">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="cf583-122">If a file is infected, users can't download the file from SharePoint Online by using a browser.</span></span>

<span data-ttu-id="cf583-123">Voici ce qui se passe :</span><span class="sxs-lookup"><span data-stu-id="cf583-123">Here's what happens:</span></span>

1. <span data-ttu-id="cf583-124">Un utilisateur ouvre un navigateur Web et essaie de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="cf583-124">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
2. <span data-ttu-id="cf583-125">L’utilisateur reçoit un avertissement indiquant qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="cf583-125">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="cf583-126">Par défaut, l’utilisateur a la possibilité de télécharger le fichier et d’essayer de le nettoyer à l’aide du logiciel anti-virus sur son propre appareil.</span><span class="sxs-lookup"><span data-stu-id="cf583-126">By default, the user is given the option to download the file and attempt to clean it using the anti-virus software on their own device.</span></span>

> [!NOTE]
>
> <span data-ttu-id="cf583-127">Les administrateurs peuvent utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers infectés, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="cf583-127">Admins can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading infected files, even in the anti-virus warning window.</span></span> <span data-ttu-id="cf583-128">Pour obtenir des instructions, consultez la rubrique [utiliser SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers malveillants](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span><span class="sxs-lookup"><span data-stu-id="cf583-128">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>
>
> <span data-ttu-id="cf583-129">Dès que vous activez le paramètre *DisallowInfectedFileDownload* , l’accès aux fichiers détectés/bloqués est totalement bloqué pour les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="cf583-129">As soon as you enable the *DisallowInfectedFileDownload* parameter, access to the detected/blocked files is completely blocked for users and admins.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="cf583-130">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="cf583-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="cf583-131">Les clients de synchronisation OneDrive ne téléchargent pas les fichiers contenant des virus.</span><span class="sxs-lookup"><span data-stu-id="cf583-131">OneDrive sync clients will not download files that contain viruses.</span></span> <span data-ttu-id="cf583-132">Le client de synchronisation affiche une notification indiquant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="cf583-132">The sync client will display a notification that the file can't be synced.</span></span>

## <a name="extended-capabilities-with-office-365-advanced-threat-protection"></a><span data-ttu-id="cf583-133">Fonctionnalités étendues avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf583-133">Extended capabilities with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="cf583-134">Les organisations Microsoft 365 qui disposent d' [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md) incluses dans leur abonnement ou achetées en tant que complément peuvent activer la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams pour améliorer la création de rapports et la protection.</span><span class="sxs-lookup"><span data-stu-id="cf583-134">Microsoft 365 organizations that have [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md) included in their subscription or purchased as an add-on can enable ATP for SharePoint, OneDrive, and Microsoft Teams for enhanced reporting and protection.</span></span> <span data-ttu-id="cf583-135">Pour plus d’informations, reportez-vous à la rubrique [ATP pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="cf583-135">For more information, see [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

## <a name="more-information"></a><span data-ttu-id="cf583-136">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cf583-136">More information</span></span>

<span data-ttu-id="cf583-137">Pour plus d’informations sur les antivirus dans SharePoint Online, OneDrive et Microsoft Teams, consultez la rubrique se [protéger contre les menaces](protect-against-threats.md) et activer la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="cf583-137">For more information about anti-virus in SharePoint Online, OneDrive, and Microsoft Teams, see [Protect against threats](protect-against-threats.md) and [Turn on ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
