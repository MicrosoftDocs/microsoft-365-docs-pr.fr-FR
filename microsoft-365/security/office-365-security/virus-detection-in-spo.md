---
title: Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft Teams
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: reference
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Découvrez comment SharePoint Online détecte des virus dans les fichiers que les utilisateurs téléchargent et empêche les utilisateurs de télécharger ou de synchroniser les fichiers.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: dd38b196c106a36fb1a1bfc0a441620b1c5b8ba5
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204157"
---
# <a name="built-in-virus-protection-in-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="4bdf8-103">Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4bdf8-103">Built-in virus protection in SharePoint Online, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="4bdf8-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="4bdf8-104">**Applies to**</span></span>
- [<span data-ttu-id="4bdf8-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="4bdf8-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="4bdf8-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="4bdf8-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)

<span data-ttu-id="4bdf8-107">Microsoft 365 utilise un moteur de détection de virus courant pour analyser les fichiers que les utilisateurs téléchargent sur SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-107">Microsoft 365 uses a common virus detection engine for scanning files that users upload to SharePoint Online, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="4bdf8-108">Cette protection est incluse dans tous les abonnements qui incluent SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-108">This protection is included with all subscriptions that include SharePoint Online, OneDrive, and Microsoft Teams.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bdf8-109">Les fonctionnalités anti-virus intégrées permettent de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-109">The built-in anti-virus capabilities are a way to help contain viruses.</span></span> <span data-ttu-id="4bdf8-110">Elles ne sont pas conçues comme un seul point de défense contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-110">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="4bdf8-111">Nous encourageons tous les clients à examiner et à implémenter la protection contre les programmes malveillants à différents niveaux et à appliquer les meilleures pratiques pour sécuriser leur infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-111">We encourage all customers to investigate and implement anti-malware protection at various layers and apply best practices for securing their enterprise infrastructure.</span></span> <span data-ttu-id="4bdf8-112">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez [la feuille de route de sécurité.](security-roadmap.md)</span><span class="sxs-lookup"><span data-stu-id="4bdf8-112">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-if-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="4bdf8-113">Que se passe-t-il si un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="4bdf8-113">What happens if an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="4bdf8-114">Le moteur Microsoft 365 détection de virus s’exécute de manière asynchrone (indépendamment des téléchargements de fichiers) dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-114">The Microsoft 365 virus detection engine runs asynchronously (independent from file uploads) within SharePoint Online.</span></span> <span data-ttu-id="4bdf8-115">**Tous les fichiers ne sont pas analysés automatiquement.**</span><span class="sxs-lookup"><span data-stu-id="4bdf8-115">**All files are not automatically scanned**.</span></span> <span data-ttu-id="4bdf8-116">Les heuristiques déterminent les fichiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-116">Heuristics determine the files to scan.</span></span> <span data-ttu-id="4bdf8-117">Lorsqu’un fichier contient un virus, le fichier est signalé.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-117">When a file is found to contain a virus, the file is flagged.</span></span> <span data-ttu-id="4bdf8-118">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-118">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="4bdf8-119">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="4bdf8-119">Here's what happens:</span></span>

1. <span data-ttu-id="4bdf8-120">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-120">A user uploads a file to SharePoint Online.</span></span>
2. <span data-ttu-id="4bdf8-121">SharePoint Online, dans le cadre de ses processus d’analyse antivirus, détermine ultérieurement si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-121">SharePoint Online, as part of its virus scanning processes, later determines if the file meets the criteria for a scan.</span></span>
3. <span data-ttu-id="4bdf8-122">Si le fichier répond aux critères d’une analyse, le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-122">If the file meets the criteria for a scan, the virus detection engine scans the file.</span></span>
4. <span data-ttu-id="4bdf8-123">Si un virus est trouvé dans le fichier analysé, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-123">If a virus is found within the scanned file, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="4bdf8-124">Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="4bdf8-124">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="4bdf8-125">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-125">If a file is infected, users can't download the file from SharePoint Online by using a browser.</span></span>

<span data-ttu-id="4bdf8-126">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="4bdf8-126">Here's what happens:</span></span>

1. <span data-ttu-id="4bdf8-127">Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-127">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
2. <span data-ttu-id="4bdf8-128">L’utilisateur est averti qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-128">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="4bdf8-129">Par défaut, l’utilisateur a la possibilité de télécharger le fichier et de tenter de le nettoyer à l’aide du logiciel antivirus sur son propre appareil.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-129">By default, the user is given the option to download the file and attempt to clean it using the anti-virus software on their own device.</span></span>

> [!NOTE]
>
> <span data-ttu-id="4bdf8-130">Les administrateurs peuvent utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers infectés, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-130">Admins can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading infected files, even in the anti-virus warning window.</span></span> <span data-ttu-id="4bdf8-131">Pour obtenir des instructions, voir Utiliser SharePoint Online PowerShell pour empêcher les utilisateurs de [télécharger des fichiers malveillants.](turn-on-mdo-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files)</span><span class="sxs-lookup"><span data-stu-id="4bdf8-131">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-mdo-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>
>
> <span data-ttu-id="4bdf8-132">Dès que vous activez le paramètre *DisallowInfectedFileDownload,* l’accès aux fichiers détectés/bloqués est complètement bloqué pour les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-132">As soon as you enable the *DisallowInfectedFileDownload* parameter, access to the detected/blocked files is completely blocked for users and admins.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="4bdf8-133">Que se passe-t-il lorsque le client OneDrive de synchronisation tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="4bdf8-133">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="4bdf8-134">OneDrive clients de synchronisation ne téléchargeront pas les fichiers contenant des virus.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-134">OneDrive sync clients will not download files that contain viruses.</span></span> <span data-ttu-id="4bdf8-135">Le client de synchronisation affiche une notification vous avertissant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-135">The sync client will display a notification that the file can't be synced.</span></span>

## <a name="extended-capabilities-with-microsoft-defender-for-office-365"></a><span data-ttu-id="4bdf8-136">Fonctionnalités étendues avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="4bdf8-136">Extended capabilities with Microsoft Defender for Office 365</span></span>

<span data-ttu-id="4bdf8-137">Microsoft 365 organisations dont [Microsoft Defender](defender-for-office-365.md) pour Office 365 est inclus dans leur abonnement ou acheté en tant que module supplémentaire peuvent activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams pour améliorer la fonctionnalité de rapports et de protection.</span><span class="sxs-lookup"><span data-stu-id="4bdf8-137">Microsoft 365 organizations that have [Microsoft Defender for Office 365](defender-for-office-365.md) included in their subscription or purchased as an add-on can enable Safe Attachments for SharePoint, OneDrive, and Microsoft Teams for enhanced reporting and protection.</span></span> <span data-ttu-id="4bdf8-138">Pour plus d’informations, [voir Pièces jointes SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="4bdf8-138">For more information, see [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

## <a name="related-articles"></a><span data-ttu-id="4bdf8-139">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4bdf8-139">Related Articles</span></span>

[<span data-ttu-id="4bdf8-140">Protection contre les programmes malveillants et les ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4bdf8-140">Malware and ransomware protection in Microsoft 365</span></span>](/compliance/assurance/assurance-malware-and-ransomware-protection)

<span data-ttu-id="4bdf8-141">Pour plus d’informations sur l’antivirus dans SharePoint Online, OneDrive et Microsoft Teams, voir Se protéger contre les menaces et activer les pièces [jointes sécurisées](turn-on-mdo-for-spo-odb-and-teams.md)pour SharePoint, OneDrive et Microsoft Teams . [](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="4bdf8-141">For more information about anti-virus in SharePoint Online, OneDrive, and Microsoft Teams, see [Protect against threats](protect-against-threats.md) and [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-mdo-for-spo-odb-and-teams.md).</span></span>
