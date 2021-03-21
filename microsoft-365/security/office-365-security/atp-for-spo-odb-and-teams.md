---
title: Pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.date: ''
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
ms.collection:
- M365-security-compliance
- SPO_Content
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
description: Découvrez Microsoft Defender pour Office 365 pour les fichiers dans SharePoint Online, OneDrive Entreprise et Microsoft Teams.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 9b69d2b6f075539f411da971a314c127843b945a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50917569"
---
# <a name="safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="2a907-103">Pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2a907-103">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2a907-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2a907-104">**Applies to**</span></span>
- [<span data-ttu-id="2a907-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="2a907-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="2a907-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2a907-106">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="2a907-107">Les pièces jointes fiables pour SharePoint, OneDrive et Microsoft Teams dans Microsoft Defender pour [Office 365](office-365-atp.md) fournissent une couche de protection supplémentaire pour les fichiers qui ont déjà été analysés au moment du chargement par le moteur de détection de virus courant dans [Microsoft 365.](virus-detection-in-spo.md)</span><span class="sxs-lookup"><span data-stu-id="2a907-107">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams in [Microsoft Defender for Office 365](office-365-atp.md) provides an additional layer of protection for files that have already been scanned at upload time by the [common virus detection engine in Microsoft 365](virus-detection-in-spo.md).</span></span> <span data-ttu-id="2a907-108">Les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams permettent de détecter et de bloquer les fichiers existants identifiés comme malveillants dans les sites d’équipe et les bibliothèques de documents.</span><span class="sxs-lookup"><span data-stu-id="2a907-108">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams helps detect and block existing files that are identified as malicious in team sites and document libraries.</span></span>

<span data-ttu-id="2a907-109">Les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams ne sont pas activées par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a907-109">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams is not enabled by default.</span></span> <span data-ttu-id="2a907-110">Pour l’activer, voir [Activer les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams.](turn-on-atp-for-spo-odb-and-teams.md)</span><span class="sxs-lookup"><span data-stu-id="2a907-110">To turn it on, see [Turn on Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

## <a name="how-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams-works"></a><span data-ttu-id="2a907-111">Fonctionnement des pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2a907-111">How Safe Attachments for SharePoint, OneDrive, and Microsoft Teams works</span></span>

<span data-ttu-id="2a907-112">Lorsque les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams sont activées et identifient un fichier comme malveillant, le fichier est verrouillé à l’aide de l’intégration directe avec les magasins de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2a907-112">When Safe Attachments for SharePoint, OneDrive, and Microsoft Teams is enabled and identifies a file as malicious, the file is locked using direct integration with the file stores.</span></span> <span data-ttu-id="2a907-113">L’image suivante illustre un exemple de fichier malveillant détecté dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2a907-113">The following image shows an example of a malicious file detected in a library.</span></span>

![Fichiers dans OneDrive Entreprise avec un fichier détecté comme malveillant](../../media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)

<span data-ttu-id="2a907-115">Bien que le fichier bloqué soit toujours répertorié dans la bibliothèque de documents et dans les applications web, mobiles ou de bureau, les utilisateurs ne peuvent pas ouvrir, copier, déplacer ou partager le fichier.</span><span class="sxs-lookup"><span data-stu-id="2a907-115">Although the blocked file is still listed in the document library and in web, mobile, or desktop applications, people can't open, copy, move, or share the file.</span></span> <span data-ttu-id="2a907-116">Toutefois, ils peuvent supprimer le fichier bloqué.</span><span class="sxs-lookup"><span data-stu-id="2a907-116">But they can delete the blocked file.</span></span>

<span data-ttu-id="2a907-117">Voici un exemple de ce à quoi ressemble un fichier bloqué sur un appareil mobile :</span><span class="sxs-lookup"><span data-stu-id="2a907-117">Here's an example of what a blocked file looks like on a mobile device:</span></span>

![Suppression d’un fichier bloqué de OneDrive Entreprise de l’application mobile OneDrive](../../media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)

<span data-ttu-id="2a907-119">Par défaut, les personnes peuvent télécharger un fichier bloqué.</span><span class="sxs-lookup"><span data-stu-id="2a907-119">By default, people can download a blocked file.</span></span> <span data-ttu-id="2a907-120">Voici à quoi ressemble le téléchargement d’un fichier bloqué sur un appareil mobile :</span><span class="sxs-lookup"><span data-stu-id="2a907-120">Here's what downloading a blocked file looks like on a mobile device:</span></span>

![Téléchargement d’un fichier bloqué dans OneDrive Entreprise](../../media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)

<span data-ttu-id="2a907-122">Les administrateurs SharePoint Online peuvent empêcher les utilisateurs de télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="2a907-122">SharePoint Online admins can prevent people from downloading malicious files.</span></span> <span data-ttu-id="2a907-123">Pour obtenir des instructions, [voir Utiliser SharePoint Online PowerShell](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files)pour empêcher les utilisateurs de télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="2a907-123">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>

<span data-ttu-id="2a907-124">Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, voir ce qu’il faut faire lorsqu’un fichier malveillant est trouvé dans [SharePoint Online, OneDrive](https://support.microsoft.com/office/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2a907-124">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.microsoft.com/office/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span>

## <a name="view-information-about-malicious-files-detected-by-safe-attachments-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="2a907-125">Afficher des informations sur les fichiers malveillants détectés par les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2a907-125">View information about malicious files detected by Safe Attachments for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="2a907-126">Les fichiers identifiés comme malveillants par Microsoft Defender pour Office 365 s’afficheront dans les rapports de Microsoft Defender pour [Office 365](view-reports-for-atp.md) et dans l’Explorateur [(et détections](threat-explorer.md)en temps réel).</span><span class="sxs-lookup"><span data-stu-id="2a907-126">Files that are identified as malicious by Microsoft Defender for Office 365 will show up in [reports for Microsoft Defender for Office 365](view-reports-for-atp.md) and in [Explorer (and real-time detections)](threat-explorer.md).</span></span>

<span data-ttu-id="2a907-127">Depuis mai 2018, lorsqu’un fichier est identifié comme malveillant par Microsoft Defender pour Office 365, le fichier est également disponible en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="2a907-127">As of May 2018, when a file is identified as malicious by Microsoft Defender for Office 365, the file is also available in quarantine.</span></span> <span data-ttu-id="2a907-128">Pour plus d’informations, [voir Utiliser le Centre de sécurité & conformité pour gérer les fichiers mis en quarantaine.](manage-quarantined-messages-and-files.md#microsoft-defender-for-office-365-only-use-the-security--compliance-center-to-manage-quarantined-files)</span><span class="sxs-lookup"><span data-stu-id="2a907-128">For more information, see [Use the Security & Compliance Center to manage quarantined files](manage-quarantined-messages-and-files.md#microsoft-defender-for-office-365-only-use-the-security--compliance-center-to-manage-quarantined-files).</span></span>

## <a name="keep-these-points-in-mind"></a><span data-ttu-id="2a907-129">Gardez ces points à l’esprit</span><span class="sxs-lookup"><span data-stu-id="2a907-129">Keep these points in mind</span></span>

- <span data-ttu-id="2a907-130">Defender pour Office 365 n’analyse pas tous les fichiers dans SharePoint Online, OneDrive Entreprise ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2a907-130">Defender for Office 365 will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams.</span></span> <span data-ttu-id="2a907-131">Ce comportement est voulu par la conception même du produit.</span><span class="sxs-lookup"><span data-stu-id="2a907-131">This is by design.</span></span> <span data-ttu-id="2a907-132">Les fichiers sont analysés de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="2a907-132">Files are scanned asynchronously.</span></span> <span data-ttu-id="2a907-133">Le processus utilise les événements de partage et d’activité invité, ainsi que les signaux heuristiques intelligents et les signaux de menace pour identifier les fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="2a907-133">The process uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="2a907-134">Assurez-vous que vos sites SharePoint sont configurés pour utiliser [l’expérience moderne.](/sharepoint/guide-to-sharepoint-modern-experience)</span><span class="sxs-lookup"><span data-stu-id="2a907-134">Make sure your SharePoint sites are configured to use the [Modern experience](/sharepoint/guide-to-sharepoint-modern-experience).</span></span> <span data-ttu-id="2a907-135">La protection Defender pour Office 365 s’applique que l’expérience moderne ou l’affichage classique soit utilisé . toutefois, les indicateurs visuels qui montrent qu’un fichier est bloqué sont disponibles uniquement dans l’expérience moderne.</span><span class="sxs-lookup"><span data-stu-id="2a907-135">Defender for Office 365 protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are available only in the Modern experience.</span></span>

- <span data-ttu-id="2a907-136">Les pièces jointes sécurisées pour SharePoint, OneDrive et Microsoft Teams font partie de la stratégie globale de protection contre les menaces de votre organisation, qui inclut la protection contre le courrier indésirable et les programmes malveillants dans Exchange Online Protection (EOP), ainsi que les liens et pièces jointes sûrs dans Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="2a907-136">Safe Attachments for SharePoint, OneDrive, and Microsoft Teams is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection in Exchange Online Protection (EOP), as well as Safe Links and Safe Attachments in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="2a907-137">Pour en savoir plus, consultez La protection contre [les menaces dans Office 365.](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="2a907-137">To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>