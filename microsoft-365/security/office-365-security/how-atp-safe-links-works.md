---
title: Fonctionnement des liens fiables PACM
f1.keywords:
- NOCSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.date: ''
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: La fonctionnalité liens fiables permet de vérifier le temps de cliquer sur les liens hypertexte dans les documents Office et dans les messages électroniques. Lisez cet article pour découvrir le fonctionnement des liens fiables ATP.
ms.openlocfilehash: 7887c3c2920f472d4baa7ff899c3e3b4f704385d
ms.sourcegitcommit: 60c1932dcca249355ef7134df0ceb0e57757dc81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "43943710"
---
# <a name="how-atp-safe-links-works"></a><span data-ttu-id="088cb-104">Fonctionnement des liens fiables PACM</span><span class="sxs-lookup"><span data-stu-id="088cb-104">How ATP Safe Links works</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="088cb-105">Pour que les liens sécurisés ATP Office 365 fonctionnent correctement, tous les services doivent être au même niveau de version.</span><span class="sxs-lookup"><span data-stu-id="088cb-105">For Office 365 ATP Safe Links to operate correctly, all of the services need to be at the same version.</span></span>
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a><span data-ttu-id="088cb-106">Fonctionnement des liaisons approuvées ATP avec les URL dans les messages électroniques</span><span class="sxs-lookup"><span data-stu-id="088cb-106">How ATP Safe Links works with URLs in email</span></span>

<span data-ttu-id="088cb-107">À un niveau élevé, voici le fonctionnement de la protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les messages électroniques (hébergé dans Office 365, pas en local) :</span><span class="sxs-lookup"><span data-stu-id="088cb-107">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in email (hosted in Office 365, not on-premises):</span></span>
  
1. <span data-ttu-id="088cb-108">Les utilisateurs reçoivent des messages électroniques, dont certains contiennent des URL.</span><span class="sxs-lookup"><span data-stu-id="088cb-108">People receive email messages, some of which contain URLs.</span></span>
    
2. <span data-ttu-id="088cb-109">Tous les messages passent par Exchange Online Protection, où les filtres IP (Internet Protocol) et des enveloppes, la protection contre les programmes malveillants basée sur la signature, le blocage du courrier indésirable et les filtres anti-programme malveillant sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="088cb-109">All email goes through Exchange Online Protection, where internet protocol (IP) and envelope filters, signature-based malware protection, anti-spam and anti-malware filters are applied.</span></span> 
    
3. <span data-ttu-id="088cb-110">Le courrier électronique arrive dans les boîtes de réception des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="088cb-110">Email arrives in people's inboxes.</span></span>
    
4. <span data-ttu-id="088cb-111">Un utilisateur se connecte à Office 365 et accède à sa boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="088cb-111">A user signs in to Office 365, and goes to their email inbox.</span></span>
    
5. <span data-ttu-id="088cb-112">L’utilisateur ouvre un message électronique et clique sur une URL dans le message électronique.</span><span class="sxs-lookup"><span data-stu-id="088cb-112">The user opens an email message, and clicks on a URL in the email message.</span></span>
    
6. <span data-ttu-id="088cb-113">La fonctionnalité de liens fiables ATP vérifie immédiatement l’URL avant d’ouvrir le site Web.</span><span class="sxs-lookup"><span data-stu-id="088cb-113">The ATP Safe Links feature immediately checks the URL before opening the website.</span></span> <span data-ttu-id="088cb-114">L’URL est identifiée comme étant bloquée, malveillante ou sécurisée.</span><span class="sxs-lookup"><span data-stu-id="088cb-114">The URL is identified as blocked, malicious, or safe.</span></span>
        
   - <span data-ttu-id="088cb-115">Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="088cb-115">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
   - <span data-ttu-id="088cb-116">Si l’URL est vers un site Web qui a été jugé malveillant, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="088cb-116">If the URL is to a website that has been determined to be malicious, a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
   - <span data-ttu-id="088cb-117">Si l’URL est dirigée vers un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) de votre organisation sont configurées pour analyser ce contenu, le fichier téléchargeable est vérifié.</span><span class="sxs-lookup"><span data-stu-id="088cb-117">If the URL goes to a downloadable file and your organization's [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such content, the downloadable file is checked.</span></span> 
    
   - <span data-ttu-id="088cb-118">Si l’URL est jugée fiable, le site Web s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="088cb-118">If the URL is determined to be safe, the website opens.</span></span>
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a><span data-ttu-id="088cb-119">Fonctionnement des liaisons approuvées ATP avec les URL des documents Office</span><span class="sxs-lookup"><span data-stu-id="088cb-119">How ATP Safe Links works with URLs in Office documents</span></span> 

<span data-ttu-id="088cb-120">À un niveau élevé, voici le mode de protection [des liens fiables ATP](atp-safe-links.md) pour les URL dans les applications Microsoft 365 pour les applications Enterprise Premium (versions actuelles de Word, Excel et PowerPoint sur Windows, Mac ou dans un navigateur, les applications Office sur les appareils iOS ou Android, Visio sur Windows, OneNote dans un navigateur) :</span><span class="sxs-lookup"><span data-stu-id="088cb-120">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in Microsoft 365 Apps for enterprise or Business Premium applications (current versions of Word, Excel, and PowerPoint on Windows, Mac, or in a browser, Office apps on iOS or Android devices, Visio on Windows, OneNote in a browser):</span></span>
  
1. <span data-ttu-id="088cb-121">Les utilisateurs ont installé Microsoft 365 apps pour Enterprise ou Business Premium sur leur ordinateur, smartphone ou tablette.</span><span class="sxs-lookup"><span data-stu-id="088cb-121">People have installed Microsoft 365 Apps for enterprise or Business Premium on their computer, smartphone, or tablet.</span></span> <span data-ttu-id="088cb-122">(Ou, ils utilisent Office dans leur navigateur.)</span><span class="sxs-lookup"><span data-stu-id="088cb-122">(Or, they are using Office in their browser.)</span></span>
    
2. <span data-ttu-id="088cb-123">Un utilisateur ouvre un Word, Excel, PowerPoint, OneNote (dans le navigateur) ou Visio (sur le bureau) et se connecte à Office 365 Enterprise à l’aide de son compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="088cb-123">A user opens a Word, Excel, PowerPoint, OneNote (in the browser), or Visio (on desktop), and signs in to Office 365 Enterprise using their work or school account.</span></span> <span data-ttu-id="088cb-124">Le document contient des URL.</span><span class="sxs-lookup"><span data-stu-id="088cb-124">The document contains URLs.</span></span>
    
3. <span data-ttu-id="088cb-125">Lorsque l’utilisateur clique sur une URL dans le document, le lien est vérifié par le service de liens fiables ATP.</span><span class="sxs-lookup"><span data-stu-id="088cb-125">When the user clicks on a URL in the document, the link is checked by the ATP Safe Links service.</span></span>
    
   - <span data-ttu-id="088cb-126">Si l’URL est vers un site Web inclus dans la [liste des URL bloquées personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md)de l’organisation, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="088cb-126">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
   - <span data-ttu-id="088cb-127">Si l’URL est vers un site Web qui a été jugé malveillant, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="088cb-127">If the URL is to a website that has been determined to be malicious, the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
   - <span data-ttu-id="088cb-128">Si l’URL mène à un fichier téléchargeable et que les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) sont configurées pour analyser ces téléchargements, le fichier téléchargeable est vérifié.</span><span class="sxs-lookup"><span data-stu-id="088cb-128">If the URL goes to a downloadable file and the [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such downloads, the downloadable file is checked.</span></span> 
    
   - <span data-ttu-id="088cb-129">Si l’URL est considérée comme fiable, l’utilisateur est dirigé vers le site Web.</span><span class="sxs-lookup"><span data-stu-id="088cb-129">If the URL is considered safe, the user is taken to the website.</span></span>
      
   - <span data-ttu-id="088cb-130">Si la vérification de l’URL échoue, la protection des liens fiables n’est pas déclenchée.</span><span class="sxs-lookup"><span data-stu-id="088cb-130">If the URL check fails, Safe Links' protection will not trigger.</span></span> <span data-ttu-id="088cb-131">Sur les clients de bureau, l’utilisateur est averti avant de passer au site.</span><span class="sxs-lookup"><span data-stu-id="088cb-131">On the desktop clients, the user will be warned before proceeding through to the site.</span></span>
      
> [!NOTE]
> <span data-ttu-id="088cb-132">Cette opération peut prendre plusieurs secondes au début de chaque session pour vérifier que l’utilisateur a activé les liens approuvés pour Office.</span><span class="sxs-lookup"><span data-stu-id="088cb-132">It may take several seconds at the beginning of each session to verify that the user has ATP Safe Links for Office enabled.</span></span> 
      
