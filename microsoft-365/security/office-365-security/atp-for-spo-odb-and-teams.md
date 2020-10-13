---
title: Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.date: ''
ms.topic: conceptual
ms.service: O365-seccomp
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
description: Découvrez la protection avancée contre les menaces Office 365 pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams.
ms.openlocfilehash: e536809c74abbe87e1250acda3f3922180cfae97
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48446262"
---
# <a name="atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="0fbe0-103">Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="0fbe0-103">ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="0fbe0-104">La protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams dans [Office 365 la protection avancée contre les menaces (ATP)](office-365-atp.md) fournit une couche supplémentaire de protection pour les fichiers qui ont déjà été analysés au moment du chargement par le [moteur de détection de virus courant dans Microsoft 365](virus-detection-in-spo.md).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-104">ATP for SharePoint, OneDrive, and Microsoft Teams in [Office 365 Advanced Threat Protection (ATP)](office-365-atp.md) provides an additional layer of protection for files that have already been scanned at upload time by the [common virus detection engine in Microsoft 365](virus-detection-in-spo.md).</span></span> <span data-ttu-id="0fbe0-105">La protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams permet de détecter et de bloquer les fichiers existants identifiés comme étant malveillants dans les sites d’équipe et les bibliothèques de documents.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-105">ATP for SharePoint, OneDrive, and Microsoft Teams helps detect and block existing files that are identified as malicious in team sites and document libraries.</span></span>

<span data-ttu-id="0fbe0-106">La protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams n’est pas activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-106">ATP for SharePoint, OneDrive, and Microsoft Teams is not enabled by default.</span></span> <span data-ttu-id="0fbe0-107">Pour l’activer, voir Activer la protection avancée contre [les menaces pour SharePoint, OneDrive et Microsoft teams](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-107">To turn it on, see [Turn on ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>

## <a name="how-atp-for-sharepoint-onedrive-and-microsoft-teams-works"></a><span data-ttu-id="0fbe0-108">Fonctionnement de la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="0fbe0-108">How ATP for SharePoint, OneDrive, and Microsoft Teams works</span></span>

<span data-ttu-id="0fbe0-109">Lorsque la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams est activée et identifie un fichier comme malveillant, le fichier est verrouillé à l’aide de l’intégration directe aux magasins de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-109">When ATP for SharePoint, OneDrive, and Microsoft Teams is enabled and identifies a file as malicious, the file is locked using direct integration with the file stores.</span></span> <span data-ttu-id="0fbe0-110">L’image suivante montre un exemple de fichier malveillant détecté dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-110">The following image shows an example of a malicious file detected in a library.</span></span>

![Fichiers dans OneDrive entreprise avec un fichier détecté comme malveillant](../../media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)

<span data-ttu-id="0fbe0-112">Bien que le fichier bloqué figure toujours dans la bibliothèque de documents et dans les applications Web, mobiles ou de bureau, les utilisateurs ne peuvent pas ouvrir, copier, déplacer ou partager le fichier.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-112">Although the blocked file is still listed in the document library and in web, mobile, or desktop applications, people can't open, copy, move, or share the file.</span></span> <span data-ttu-id="0fbe0-113">Mais ils peuvent supprimer le fichier bloqué.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-113">But they can delete the blocked file.</span></span>

<span data-ttu-id="0fbe0-114">Voici un exemple de ce à quoi ressemble un fichier bloqué sur un appareil mobile :</span><span class="sxs-lookup"><span data-stu-id="0fbe0-114">Here's an example of what a blocked file looks like on a mobile device:</span></span>

![Suppression d’un fichier bloqué de OneDrive entreprise à partir de l’application mobile OneDrive](../../media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)

<span data-ttu-id="0fbe0-116">Par défaut, les utilisateurs peuvent télécharger un fichier bloqué.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-116">By default, people can download a blocked file.</span></span> <span data-ttu-id="0fbe0-117">Voici ce à quoi ressemble un fichier bloqué sur un appareil mobile :</span><span class="sxs-lookup"><span data-stu-id="0fbe0-117">Here's what downloading a blocked file looks like on a mobile device:</span></span>

![Téléchargement d’un fichier bloqué dans OneDrive entreprise](../../media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)

<span data-ttu-id="0fbe0-119">Les administrateurs SharePoint Online peuvent empêcher les utilisateurs de télécharger des fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-119">SharePoint Online admins can prevent people from downloading malicious files.</span></span> <span data-ttu-id="0fbe0-120">Pour obtenir des instructions, consultez la rubrique [utiliser SharePoint Online PowerShell pour empêcher les utilisateurs de télécharger des fichiers malveillants](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-120">For instructions, see [Use SharePoint Online PowerShell to prevent users from downloading malicious files](turn-on-atp-for-spo-odb-and-teams.md#step-2-recommended-use-sharepoint-online-powershell-to-prevent-users-from-downloading-malicious-files).</span></span>

<span data-ttu-id="0fbe0-121">Pour en savoir plus sur l’expérience utilisateur lorsqu’un fichier a été détecté comme malveillant, consultez la rubrique [que faire lorsqu’un fichier malveillant est trouvé dans SharePoint Online, OneDrive ou Microsoft teams](https://support.microsoft.com/office/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-121">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.microsoft.com/office/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span>

## <a name="view-information-about-malicious-files-detected-by-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="0fbe0-122">Afficher des informations sur les fichiers malveillants détectés par la protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="0fbe0-122">View information about malicious files detected by ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="0fbe0-123">Les fichiers identifiés comme étant malveillants par la protection avancée contre les menaces s’afficheront dans [les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md) et dans l' [Explorateur (et les détections en temps réel)](threat-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-123">Files that are identified as malicious by ATP will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in [Explorer (and real-time detections)](threat-explorer.md).</span></span>

<span data-ttu-id="0fbe0-124">En ce qui concerne le 2018 mai, lorsqu’un fichier est identifié comme malveillant par la protection avancée contre les menaces, le fichier est également disponible en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-124">As of May 2018, when a file is identified as malicious by ATP, the file is also available in quarantine.</span></span> <span data-ttu-id="0fbe0-125">Pour plus d’informations, consultez [la rubrique utiliser le centre de sécurité & conformité pour gérer les fichiers mis en quarantaine](manage-quarantined-messages-and-files.md#atp-only-use-the-security--compliance-center-to-manage-quarantined-files).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-125">For more information, see [Use the Security & Compliance Center to manage quarantined files](manage-quarantined-messages-and-files.md#atp-only-use-the-security--compliance-center-to-manage-quarantined-files).</span></span>

## <a name="keep-these-points-in-mind"></a><span data-ttu-id="0fbe0-126">Gardez les points suivants à l’esprit</span><span class="sxs-lookup"><span data-stu-id="0fbe0-126">Keep these points in mind</span></span>

- <span data-ttu-id="0fbe0-127">La protection avancée contre les menaces n’analysera pas chaque fichier unique dans SharePoint Online, OneDrive entreprise ou Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-127">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams.</span></span> <span data-ttu-id="0fbe0-128">Ce comportement est voulu par la conception même du produit.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-128">This is by design.</span></span> <span data-ttu-id="0fbe0-129">Les fichiers sont analysés de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-129">Files are scanned asynchronously.</span></span> <span data-ttu-id="0fbe0-130">Le processus utilise les événements d’activité de partage et d’invité, ainsi que les heuristiques intelligentes et les signaux de menace pour identifier les fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-130">The process uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="0fbe0-131">Assurez-vous que vos sites SharePoint sont configurés pour utiliser l' [expérience moderne](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-131">Make sure your SharePoint sites are configured to use the [Modern experience](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience).</span></span> <span data-ttu-id="0fbe0-132">La protection contre l’ATP s’applique si l’expérience moderne ou la vue standard est utilisée ; Toutefois, les indicateurs visuels signalant qu’un fichier est bloqué sont disponibles uniquement dans l’expérience moderne.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-132">ATP protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are available only in the Modern experience.</span></span>

- <span data-ttu-id="0fbe0-133">La protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft teams fait partie de la stratégie globale de protection contre les menaces de votre organisation, qui inclut la protection contre le courrier indésirable et les programmes malveillants dans Exchange Online Protection (EOP), ainsi que les liens fiables et les pièces jointes fiables dans Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="0fbe0-133">ATP for SharePoint, OneDrive, and Microsoft Teams is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection in Exchange Online Protection (EOP), as well as Safe Links and Safe Attachments in Office 365 ATP.</span></span> <span data-ttu-id="0fbe0-134">Pour en savoir plus, consultez la rubrique [Protégez-vous contre les menaces dans Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="0fbe0-134">To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
