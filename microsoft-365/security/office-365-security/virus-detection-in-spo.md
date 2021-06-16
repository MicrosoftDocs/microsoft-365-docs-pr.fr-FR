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
ms.openlocfilehash: 2ab11d4c1e2a064ad0717e6619f72a38b0cbc831
ms.sourcegitcommit: ac3e9ccb7b43a42e600af8f44e6f30019533faeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "52932829"
---
# <a name="built-in-virus-protection-in-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="8228e-103">Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8228e-103">Built-in virus protection in SharePoint Online, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8228e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8228e-104">**Applies to**</span></span>
- [<span data-ttu-id="8228e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8228e-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="8228e-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="8228e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)

<span data-ttu-id="8228e-107">Microsoft 365 utilise un moteur de détection de virus courant pour analyser les fichiers que les utilisateurs téléchargent sur SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8228e-107">Microsoft 365 uses a common virus detection engine for scanning files that users upload to SharePoint Online, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="8228e-108">Cette protection est incluse dans tous les abonnements qui incluent SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8228e-108">This protection is included with all subscriptions that include SharePoint Online, OneDrive, and Microsoft Teams.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8228e-109">Les fonctionnalités anti-virus intégrées permettent de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="8228e-109">The built-in anti-virus capabilities are a way to help contain viruses.</span></span> <span data-ttu-id="8228e-110">Elles ne sont pas destinées à être un point de défense unique contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8228e-110">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="8228e-111">Nous encourageons tous les clients à examiner et à implémenter la protection contre les programmes malveillants à différents niveaux et à appliquer les meilleures pratiques pour sécuriser leur infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="8228e-111">We encourage all customers to investigate and implement anti-malware protection at various layers and apply best practices for securing their enterprise infrastructure.</span></span> <span data-ttu-id="8228e-112">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez [la feuille de route de sécurité.](security-roadmap.md)</span><span class="sxs-lookup"><span data-stu-id="8228e-112">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-if-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="8228e-113">Que se passe-t-il si un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="8228e-113">What happens if an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="8228e-114">Le moteur Microsoft 365 détection de virus s’exécute de manière asynchrone (indépendamment des chargements de fichiers) dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8228e-114">The Microsoft 365 virus detection engine runs asynchronously (independent from file uploads) within SharePoint Online.</span></span> <span data-ttu-id="8228e-115">**Tous les fichiers ne sont pas analysés automatiquement.**</span><span class="sxs-lookup"><span data-stu-id="8228e-115">**All files are not automatically scanned**.</span></span> <span data-ttu-id="8228e-116">Les heuristiques déterminent les fichiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="8228e-116">Heuristics determine the files to scan.</span></span> <span data-ttu-id="8228e-117">Lorsqu’un fichier contient un virus, le fichier est signalé.</span><span class="sxs-lookup"><span data-stu-id="8228e-117">When a file is found to contain a virus, the file is flagged.</span></span> <span data-ttu-id="8228e-118">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="8228e-118">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="8228e-119">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="8228e-119">Here's what happens:</span></span>

1. <span data-ttu-id="8228e-120">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8228e-120">A user uploads a file to SharePoint Online.</span></span>
2. <span data-ttu-id="8228e-121">SharePoint Online, dans le cadre de ses processus d’analyse antivirus, détermine ultérieurement si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="8228e-121">SharePoint Online, as part of its virus scanning processes, later determines if the file meets the criteria for a scan.</span></span>
3. <span data-ttu-id="8228e-122">Si le fichier répond aux critères d’une analyse, le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="8228e-122">If the file meets the criteria for a scan, the virus detection engine scans the file.</span></span>
4. <span data-ttu-id="8228e-123">Si un virus est trouvé dans le fichier analysé, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="8228e-123">If a virus is found within the scanned file, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="8228e-124">Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="8228e-124">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="8228e-125">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="8228e-125">If a file is infected, users can't download the file from SharePoint Online by using a browser.</span></span>

<span data-ttu-id="8228e-126">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="8228e-126">Here's what happens:</span></span>

1. <span data-ttu-id="8228e-127">Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="8228e-127">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
2. <span data-ttu-id="8228e-128">L’utilisateur est averti qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="8228e-128">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="8228e-129">Par défaut, l’utilisateur a la possibilité de télécharger le fichier et de tenter de le nettoyer à l’aide du logiciel antivirus sur son propre appareil.</span><span class="sxs-lookup"><span data-stu-id="8228e-129">By default, the user is given the option to download the file and attempt to clean it using the anti-virus software on their own device.</span></span>

> [!NOTE]
>
> <span data-ttu-id="8228e-130">Les administrateurs peuvent utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers infectés, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="8228e-130">Admins can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading infected files, even in the anti-virus warning window.</span></span> <span data-ttu-id="8228e-131">Pour obtenir des instructions, voir Utiliser SharePoint Online PowerShell pour empêcher les utilisateurs de [télécharger des fichiers malveillants.](turn-on-mdo-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files)</span><span class="sxs-lookup"><span data-stu-id="8228e-131">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-mdo-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>
>
> <span data-ttu-id="8228e-132">Dès que vous activez le paramètre *DisallowInfectedFileDownload,* l’accès aux fichiers détectés/bloqués est complètement bloqué pour les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="8228e-132">As soon as you enable the *DisallowInfectedFileDownload* parameter, access to the detected/blocked files is completely blocked for users and admins.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="8228e-133">Que se passe-t-il lorsque le client OneDrive de synchronisation tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="8228e-133">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="8228e-134">Lorsqu’un fichier malveillant est téléchargé vers OneDrive, il est synchronisé avec l’ordinateur local avant d’être marqué comme programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="8228e-134">When a malicious file is uploaded to OneDrive, it will be synced to the local machine before it's marked as malware.</span></span> <span data-ttu-id="8228e-135">Une fois qu’il a été marqué comme programme malveillant, l’utilisateur ne peut plus ouvrir le fichier synchronisé à partir de son ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8228e-135">After it's marked as malware, the user can't open the synced file anymore from their local machine.</span></span>

## <a name="extended-capabilities-with-microsoft-defender-for-office-365"></a><span data-ttu-id="8228e-136">Fonctionnalités étendues avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8228e-136">Extended capabilities with Microsoft Defender for Office 365</span></span>

<span data-ttu-id="8228e-137">Microsoft 365 organisations dont [Microsoft Defender](defender-for-office-365.md) pour Office 365 est inclus dans leur abonnement ou acheté en tant que module supplémentaire peuvent activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams pour améliorer la fonctionnalité de rapports et de protection.</span><span class="sxs-lookup"><span data-stu-id="8228e-137">Microsoft 365 organizations that have [Microsoft Defender for Office 365](defender-for-office-365.md) included in their subscription or purchased as an add-on can enable Safe Attachments for SharePoint, OneDrive, and Microsoft Teams for enhanced reporting and protection.</span></span> <span data-ttu-id="8228e-138">Pour plus d’informations, [voir Pièces jointes SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="8228e-138">For more information, see [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

## <a name="related-articles"></a><span data-ttu-id="8228e-139">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="8228e-139">Related Articles</span></span>

[<span data-ttu-id="8228e-140">Protection contre les programmes malveillants et les ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8228e-140">Malware and ransomware protection in Microsoft 365</span></span>](/compliance/assurance/assurance-malware-and-ransomware-protection)

<span data-ttu-id="8228e-141">Pour plus d’informations sur l’antivirus dans SharePoint Online, OneDrive et Microsoft Teams, voir Se protéger contre les menaces et activer les pièces [jointes sécurisées](turn-on-mdo-for-spo-odb-and-teams.md)pour SharePoint, OneDrive et Microsoft Teams . [](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="8228e-141">For more information about anti-virus in SharePoint Online, OneDrive, and Microsoft Teams, see [Protect against threats](protect-against-threats.md) and [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-mdo-for-spo-odb-and-teams.md).</span></span>
