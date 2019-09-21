---
title: Fonctionnement des liaisons approuvées ATP Office 365
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: La fonctionnalité liens fiables permet de vérifier le temps de cliquer sur les liens hypertexte dans les documents Office et dans les messages électroniques. Lisez cet article pour découvrir le fonctionnement des liens fiables ATP.
ms.openlocfilehash: 45053b51bb5a91698d90f61567aa7f5577518587
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079049"
---
# <a name="how-office-365-atp-safe-links-works"></a><span data-ttu-id="cf9b4-104">Fonctionnement des liaisons approuvées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="cf9b4-104">How Office 365 ATP Safe Links works</span></span>
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a><span data-ttu-id="cf9b4-105">Fonctionnement des liaisons approuvées ATP avec les URL dans les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="cf9b4-105">How ATP Safe Links works with URLs in email</span></span>

<span data-ttu-id="cf9b4-106">À un niveau élevé, voici le fonctionnement de la protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les messages électroniques (hébergé dans Office 365, pas en local) :</span><span class="sxs-lookup"><span data-stu-id="cf9b4-106">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in email (hosted in Office 365, not on-premises):</span></span>
  
1. <span data-ttu-id="cf9b4-107">Les utilisateurs reçoivent des messages électroniques, dont certains contiennent des URL.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-107">People receive email messages, some of which contain URLs.</span></span>
    
2. <span data-ttu-id="cf9b4-108">Tous les messages passent par Exchange Online Protection, où les filtres IP (Internet Protocol) et des enveloppes, la protection contre les programmes malveillants basée sur la signature, le blocage du courrier indésirable et les filtres anti-programme malveillant sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-108">All email goes through Exchange Online Protection, where internet protocol (IP) and envelope filters, signature-based malware protection, anti-spam and anti-malware filters are applied.</span></span> 
    
3. <span data-ttu-id="cf9b4-109">Le courrier électronique arrive dans les boîtes de réception des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-109">Email arrives in people's inboxes.</span></span>
    
4. <span data-ttu-id="cf9b4-110">Un utilisateur se connecte à Office 365 et accède à sa boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-110">A user signs in to Office 365, and goes to their email inbox.</span></span>
    
5. <span data-ttu-id="cf9b4-111">L’utilisateur ouvre un message électronique et clique sur une URL dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-111">The user opens an email message, and clicks on a URL in the email message.</span></span>
    
6. <span data-ttu-id="cf9b4-112">La fonctionnalité de liens fiables ATP vérifie immédiatement l’URL avant d’ouvrir le site Web.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-112">The ATP Safe Links feature immediately checks the URL before opening the website.</span></span> <span data-ttu-id="cf9b4-113">L’URL est identifiée comme étant bloquée, malveillante ou sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-113">The URL is identified as blocked, malicious, or safe.</span></span>
    
    - <span data-ttu-id="cf9b4-114">Si l’URL est vers un site Web qui est inclus dans une [liste d’URL « ne pas réécrire » personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, le site Web s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-114">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, the website opens.</span></span> 
    
    - <span data-ttu-id="cf9b4-115">Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-115">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="cf9b4-116">Si l’URL est vers un site Web qui a été jugé malveillant, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-116">If the URL is to a website that has been determined to be malicious, a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="cf9b4-117">Si l’URL est dirigée vers un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) de votre organisation sont configurées pour analyser ce contenu, le fichier téléchargeable est vérifié.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-117">If the URL goes to a downloadable file and your organization's [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such content, the downloadable file is checked.</span></span> 
    
    - <span data-ttu-id="cf9b4-118">Si l’URL est jugée fiable, le site Web s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-118">If the URL is determined to be safe, the website opens.</span></span>
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a><span data-ttu-id="cf9b4-119">Fonctionnement des liaisons approuvées ATP avec les URL des documents Office</span><span class="sxs-lookup"><span data-stu-id="cf9b4-119">How ATP Safe Links works with URLs in Office documents</span></span>

<span data-ttu-id="cf9b4-120">À un niveau élevé, voici le fonctionnement de la protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les applications Office 365 ProPlus (versions actuelles de Word, Excel et PowerPoint sur Windows ou Mac, les applications Office sur les appareils iOS ou Android, Visio sur Windows, OneNote dans un navigateur et Office dans un navigateur) :</span><span class="sxs-lookup"><span data-stu-id="cf9b4-120">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in Office 365 ProPlus applications (current versions of Word, Excel, and PowerPoint on Windows or Mac, Office apps on iOS or Android devices, Visio on Windows, OneNote in a browser, and Office in a browser):</span></span>
  
1. <span data-ttu-id="cf9b4-121">Les utilisateurs ont installé Office 365 ProPlus sur leur ordinateur, smartphone ou tablette.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-121">People have installed Office 365 ProPlus on their computer, smartphone, or tablet.</span></span> <span data-ttu-id="cf9b4-122">(Ou, ils utilisent Office dans leur navigateur.)</span><span class="sxs-lookup"><span data-stu-id="cf9b4-122">(Or, they are using Office in their browser.)</span></span>
    
2. <span data-ttu-id="cf9b4-123">Un utilisateur ouvre un mot, Excel, PowerPoint ou Visio et se connecte à Office 365 Enterprise à l’aide de son compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-123">A user opens a Word, Excel, PowerPoint, or Visio, and signs in to Office 365 Enterprise using their work or school account.</span></span> <span data-ttu-id="cf9b4-124">Le document contient des URL.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-124">The document contains URLs.</span></span>
    
3. <span data-ttu-id="cf9b4-125">Lorsque l’utilisateur clique sur une URL dans le document, le lien est vérifié par le service de liens fiables ATP.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-125">When the user clicks on a URL in the document, the link is checked by the ATP Safe Links service.</span></span>
    
      - <span data-ttu-id="cf9b4-126">Si l’URL est vers un site Web qui est inclus dans une [liste d’URL « ne pas réécrire » personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, cet utilisateur est dirigé vers le site Web.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-126">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, that user is taken to the website.</span></span> 
    
      - <span data-ttu-id="cf9b4-127">Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="cf9b4-127">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="cf9b4-128">Si l’URL est vers un site Web qui a été jugé malveillant, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="cf9b4-128">If the URL is to a website that has been determined to be malicious, the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="cf9b4-129">Si l’URL mène à un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) sont configurées pour analyser ces téléchargements, le fichier téléchargeable est vérifié.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-129">If the URL goes to a downloadable file and the [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such downloads, the downloadable file is checked.</span></span> 
    
      - <span data-ttu-id="cf9b4-130">Si l’URL est considérée comme fiable, l’utilisateur est dirigé vers le site Web.</span><span class="sxs-lookup"><span data-stu-id="cf9b4-130">If the URL is considered safe, the user is taken to the website.</span></span>

