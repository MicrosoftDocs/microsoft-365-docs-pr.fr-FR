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
description: Découvrez comment SharePoint Online détecte les virus dans les fichiers que les utilisateurs téléchargent et empêche les utilisateurs de télécharger ou de synchroniser les fichiers.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: f0eafb9e5e2f0c9d86791fe83931276e420afcd9
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50286500"
---
# <a name="built-in-virus-protection-in-sharepoint-online-onedrive-and-microsoft-teams"></a><span data-ttu-id="81ba8-103">Protection antivirus intégrée dans SharePoint Online, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="81ba8-103">Built-in virus protection in SharePoint Online, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="81ba8-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="81ba8-104">**Applies to**</span></span>
- [<span data-ttu-id="81ba8-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="81ba8-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="81ba8-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="81ba8-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)

<span data-ttu-id="81ba8-107">Microsoft 365 utilise un moteur de détection de virus courant pour analyser les fichiers que les utilisateurs téléchargent sur SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="81ba8-107">Microsoft 365 uses a common virus detection engine for scanning files that users upload to SharePoint Online, OneDrive, and Microsoft Teams.</span></span> <span data-ttu-id="81ba8-108">Cette protection est incluse dans tous les abonnements qui incluent SharePoint Online, OneDrive et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="81ba8-108">This protection is included with all subscriptions that include SharePoint Online, OneDrive, and Microsoft Teams.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81ba8-109">Les fonctionnalités anti-virus intégrées permettent de contenir des virus.</span><span class="sxs-lookup"><span data-stu-id="81ba8-109">The built-in anti-virus capabilities are a way to help contain viruses.</span></span> <span data-ttu-id="81ba8-110">Elles ne sont pas conçues comme un seul point de défense contre les programmes malveillants pour votre environnement.</span><span class="sxs-lookup"><span data-stu-id="81ba8-110">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="81ba8-111">Nous encourageons tous les clients à examiner et à implémenter la protection contre les programmes malveillants à différents niveaux et à appliquer les meilleures pratiques pour sécuriser leur infrastructure d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="81ba8-111">We encourage all customers to investigate and implement anti-malware protection at various layers and apply best practices for securing their enterprise infrastructure.</span></span> <span data-ttu-id="81ba8-112">Pour plus d’informations sur les stratégies et les meilleures pratiques, consultez [la feuille de route de sécurité.](security-roadmap.md)</span><span class="sxs-lookup"><span data-stu-id="81ba8-112">For more information about strategies and best practices, see [Security roadmap](security-roadmap.md).</span></span>

## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="81ba8-113">Que se passe-t-il lorsqu’un fichier infecté est téléchargé vers SharePoint Online ?</span><span class="sxs-lookup"><span data-stu-id="81ba8-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="81ba8-114">Le moteur de détection de virus Microsoft 365 s’exécute de manière asynchrone dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="81ba8-114">The Microsoft 365 virus detection engine runs asynchronously within SharePoint Online.</span></span> <span data-ttu-id="81ba8-115">**Tous les fichiers ne sont pas analysés automatiquement au chargement.**</span><span class="sxs-lookup"><span data-stu-id="81ba8-115">**All files are not automatically scanned on upload**.</span></span> <span data-ttu-id="81ba8-116">Les heuristiques déterminent les fichiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="81ba8-116">Heuristics determine the files to scan.</span></span> <span data-ttu-id="81ba8-117">Lorsqu’un fichier contient un virus, il est marqué de sorte qu’il ne peut pas être téléchargé à nouveau.</span><span class="sxs-lookup"><span data-stu-id="81ba8-117">When a file is found to contain a virus, the file is flagged so it can't be downloaded again.</span></span> <span data-ttu-id="81ba8-118">En avril 2018, nous avons supprimé la limite de 25 Mo pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="81ba8-118">In April 2018, we removed the 25 MB limit for scanned files.</span></span>

<span data-ttu-id="81ba8-119">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="81ba8-119">Here's what happens:</span></span>

1. <span data-ttu-id="81ba8-120">Un utilisateur télécharge un fichier vers SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="81ba8-120">A user uploads a file to SharePoint Online.</span></span>
2. <span data-ttu-id="81ba8-121">SharePoint Online détermine si le fichier répond aux critères d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="81ba8-121">SharePoint Online determines whether the file meets the criteria for a scan.</span></span>
3. <span data-ttu-id="81ba8-122">Le moteur de détection de virus analyse le fichier.</span><span class="sxs-lookup"><span data-stu-id="81ba8-122">The virus detection engine scans the file.</span></span>
4. <span data-ttu-id="81ba8-123">Si un virus est trouvé, le moteur de virus définit une propriété sur le fichier indiquant qu’il est infecté.</span><span class="sxs-lookup"><span data-stu-id="81ba8-123">If a virus is found, the virus engine sets a property on the file indicating that it's infected.</span></span>

## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="81ba8-124">Que se passe-t-il lorsqu’un utilisateur tente de télécharger un fichier infecté à l’aide du navigateur ?</span><span class="sxs-lookup"><span data-stu-id="81ba8-124">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="81ba8-125">Si un fichier est infecté, les utilisateurs ne peuvent pas télécharger le fichier à partir de SharePoint Online à l’aide d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="81ba8-125">If a file is infected, users can't download the file from SharePoint Online by using a browser.</span></span>

<span data-ttu-id="81ba8-126">Voici ce qui se produit :</span><span class="sxs-lookup"><span data-stu-id="81ba8-126">Here's what happens:</span></span>

1. <span data-ttu-id="81ba8-127">Un utilisateur ouvre un navigateur web et tente de télécharger un fichier infecté à partir de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="81ba8-127">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
2. <span data-ttu-id="81ba8-128">L’utilisateur est averti qu’un virus a été détecté.</span><span class="sxs-lookup"><span data-stu-id="81ba8-128">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="81ba8-129">Par défaut, l’utilisateur a la possibilité de télécharger le fichier et de tenter de le nettoyer à l’aide du logiciel antivirus sur son propre appareil.</span><span class="sxs-lookup"><span data-stu-id="81ba8-129">By default, the user is given the option to download the file and attempt to clean it using the anti-virus software on their own device.</span></span>

> [!NOTE]
>
> <span data-ttu-id="81ba8-130">Les administrateurs peuvent utiliser le paramètre *DisallowInfectedFileDownload* sur la cmdlet [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) dans SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers infectés, même dans la fenêtre d’avertissement antivirus.</span><span class="sxs-lookup"><span data-stu-id="81ba8-130">Admins can use the *DisallowInfectedFileDownload* parameter on the [Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant) cmdlet in SharePoint Online PowerShell to prevent users from downloading infected files, even in the anti-virus warning window.</span></span> <span data-ttu-id="81ba8-131">Pour obtenir des instructions, [voir Utiliser SharePoint Online PowerShell](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files)pour empêcher les utilisateurs de télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="81ba8-131">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>
>
> <span data-ttu-id="81ba8-132">Dès que vous activez le paramètre *DisallowInfectedFileDownload,* l’accès aux fichiers détectés/bloqués est complètement bloqué pour les utilisateurs et les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="81ba8-132">As soon as you enable the *DisallowInfectedFileDownload* parameter, access to the detected/blocked files is completely blocked for users and admins.</span></span>

## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="81ba8-133">Que se passe-t-il lorsque le client de synchronisation OneDrive tente de synchroniser un fichier infecté ?</span><span class="sxs-lookup"><span data-stu-id="81ba8-133">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="81ba8-134">Les clients de synchronisation OneDrive ne téléchargeront pas les fichiers contenant des virus.</span><span class="sxs-lookup"><span data-stu-id="81ba8-134">OneDrive sync clients will not download files that contain viruses.</span></span> <span data-ttu-id="81ba8-135">Le client de synchronisation affiche une notification vous avertissant que le fichier ne peut pas être synchronisé.</span><span class="sxs-lookup"><span data-stu-id="81ba8-135">The sync client will display a notification that the file can't be synced.</span></span>

## <a name="extended-capabilities-with-microsoft-defender-for-office-365"></a><span data-ttu-id="81ba8-136">Fonctionnalités étendues avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="81ba8-136">Extended capabilities with Microsoft Defender for Office 365</span></span>

<span data-ttu-id="81ba8-137">Les organisations Microsoft 365 dont Microsoft Defender pour [Office 365](office-365-atp.md) est inclus dans leur abonnement ou qui ont été achetés en tant que modules peuvent activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams pour améliorer la fonctionnalité de rapports et de protection.</span><span class="sxs-lookup"><span data-stu-id="81ba8-137">Microsoft 365 organizations that have [Microsoft Defender for Office 365](office-365-atp.md) included in their subscription or purchased as an add-on can enable Safe Attachments for SharePoint, OneDrive, and Microsoft Teams for enhanced reporting and protection.</span></span> <span data-ttu-id="81ba8-138">Pour plus d’informations, [voir Pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.](atp-for-spo-odb-and-teams.md)</span><span class="sxs-lookup"><span data-stu-id="81ba8-138">For more information, see [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

## <a name="related-articles"></a><span data-ttu-id="81ba8-139">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="81ba8-139">Related Articles</span></span>

[<span data-ttu-id="81ba8-140">Protection contre les programmes malveillants et les ransomware dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81ba8-140">Malware and ransomware protection in Microsoft 365</span></span>](https://docs.microsoft.com/compliance/assurance/assurance-malware-and-ransomware-protection)

<span data-ttu-id="81ba8-141">Pour plus d’informations sur l’antivirus dans SharePoint Online, OneDrive et Microsoft Teams, voir Se protéger contre les menaces et activer les pièces [jointes sécurisées pour SharePoint, OneDrive](turn-on-atp-for-spo-odb-and-teams.md)et Microsoft Teams. [](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="81ba8-141">For more information about anti-virus in SharePoint Online, OneDrive, and Microsoft Teams, see [Protect against threats](protect-against-threats.md) and [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
