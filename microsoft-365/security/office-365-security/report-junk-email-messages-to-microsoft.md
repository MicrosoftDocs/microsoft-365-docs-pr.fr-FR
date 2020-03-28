---
title: Signaler les messages de courrier indésirable, non-courrier indésirable et de hameçonnage à Microsoft
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/09/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c31406ea-2979-4fac-9288-f835269b9d2f
ms.collection:
- M365-security-compliance
description: 'Le complément de signalement de courrier indésirable de Microsoft pour Microsoft Office Outlook vous offre plusieurs méthodes pour signaler des messages en tant que courriers indésirables :'
ms.openlocfilehash: b7e7ed56f171ee3b74b36ed7c10c46286fb1e570
ms.sourcegitcommit: d00efe6010185559e742304b55fa2d07127268fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2020
ms.locfileid: "43033661"
---
# <a name="report-messages-and-files-to-microsoft"></a><span data-ttu-id="6c608-103">Signaler des messages et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c608-103">Report messages and files to Microsoft</span></span>

<span data-ttu-id="6c608-104">Les utilisateurs et administrateurs dans Office 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online (EOP) autonomes sans Exchange Online pour soumettre des messages électroniques disposent de différentes méthodes pour signaler les messages et fichiers vers Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6c608-104">Users and admins in Office 365 organizations with mailboxes in Exchange Online, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes to submit email messages have several different methods for reporting messages and files to Microsoft.</span></span>

|||
|---|---|
|<span data-ttu-id="6c608-105">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="6c608-105">**Method**</span></span>|<span data-ttu-id="6c608-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c608-106">**Description**</span></span>|
|[<span data-ttu-id="6c608-107">Utiliser la soumission de l’administrateur pour soumettre des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="6c608-107">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>](admin-submission.md)|<span data-ttu-id="6c608-108">Il s’agit de la méthode de création de rapports recommandée pour les administrateurs dans les organisations avec des boîtes aux lettres Exchange Online (non disponible dans la version autonome EOP).</span><span class="sxs-lookup"><span data-stu-id="6c608-108">This is the recommended reporting method for admins in organizations with Exchange Online mailboxes (not available in standalone EOP).</span></span>|
|[<span data-ttu-id="6c608-109">Activer le complément de message de rapport dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6c608-109">Enable the Report Message add-in in Office 365</span></span>](enable-the-report-message-add-in.md)|<span data-ttu-id="6c608-110">Fonctionne avec Outlook, Outlook pour Mac et Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="6c608-110">Works with Outlook, Outlook for Mac, and Outlook on the web.</span></span> <span data-ttu-id="6c608-111">Il s’agit du complément recommandé.</span><span class="sxs-lookup"><span data-stu-id="6c608-111">This is the recommended add-in.</span></span> <br/><br/> <span data-ttu-id="6c608-112">En fonction de votre licence, les messages signalés sont disponibles dans les [résultats d’enquête et de réponse (air) automatisés](air-view-investigation-results.md), le rapport de messages et l' [Explorateur de menaces](threat-explorer-views.md#email--submissions) [signalés par l’utilisateur](view-email-security-reports.md#user-reported-messages-report) .</span><span class="sxs-lookup"><span data-stu-id="6c608-112">Depending on your license, the reported messages are available in [Automated investigation and response (AIR) results](air-view-investigation-results.md), the [User-reported messages report](view-email-security-reports.md#user-reported-messages-report) and [Threat Explorer](threat-explorer-views.md#email--submissions).</span></span>|
|[<span data-ttu-id="6c608-113">Installer et utiliser le complément de création de rapports de courrier indésirable pour Microsoft Outlook dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6c608-113">Install and use the Junk Email Reporting add-in for Microsoft Outlook in Office 365</span></span>](junk-email-reporting-add-in-for-microsoft-outlook.md)|<span data-ttu-id="6c608-114">Fonctionne uniquement dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c608-114">Only works in Outlook.</span></span>|
|[<span data-ttu-id="6c608-115">Signaler les messages de courrier indésirable et de hameçonnage dans Outlook sur le Web dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6c608-115">Report junk and phishing email in Outlook on the web in Office 365</span></span>](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md)|<span data-ttu-id="6c608-116">Utiliser les fonctionnalités intégrées dans Outlook sur le Web pour les organisations avec des boîtes aux lettres Exchange Online (non disponible dans la version autonome d’EOP).</span><span class="sxs-lookup"><span data-stu-id="6c608-116">Use the built-in capabilities in Outlook on the web for organizations with Exchange Online mailboxes (not available in standalone EOP).</span></span>|
|[<span data-ttu-id="6c608-117">Soumission de programmes malveillants et non malveillants à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="6c608-117">Submit malware and non-malware to Microsoft for analysis</span></span>](submitting-malware-and-non-malware-to-microsoft-for-analysis.md)|<span data-ttu-id="6c608-118">Utiliser le site d’intelligence de sécurité Microsoft pour soumettre des pièces jointes et d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="6c608-118">Use the Microsoft Security Intelligence site to submit attachments and other files.</span></span>|
|

<span data-ttu-id="6c608-119">Si les messages de courrier indésirable ou de hameçonnage ont été mis en quarantaine au lieu d’être remis, les utilisateurs peuvent signaler les messages à Microsoft à partir du portail de mise en quarantaine dans le centre de sécurité & de la sécurité Office 365.</span><span class="sxs-lookup"><span data-stu-id="6c608-119">If the spam or phishing messages were quarantined instead of delivered, users can report the messages to Microsoft from the Quarantine portal in the Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="6c608-120">Pour plus d’informations, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="6c608-120">For details, see [Find and release quarantined messages as a user in Office 365](find-and-release-quarantined-messages-as-a-user.md).</span></span>