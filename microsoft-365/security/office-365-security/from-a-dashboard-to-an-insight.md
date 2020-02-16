---
title: Procédure pas à pas. D’un tableau de bord à un aperçu
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 06/04/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
ms.collection:
- M365-security-compliance
description: Découvrez comment passer d’un tableau de bord à un aperçu des actions recommandées dans le &amp; Centre de sécurité conformité.
ms.openlocfilehash: 8f6a75e02f00cbc62e4907ea3a0ff54c72110a21
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42083153"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="f5737-103">Procédure pas à pas. D’un tableau de bord à un aperçu</span><span class="sxs-lookup"><span data-stu-id="f5737-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="f5737-104">Si vous débutez avec des [rapports et des informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md), il peut vous aider à naviguer dans un tableau de bord jusqu’à une vue d’analyse et des actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="f5737-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="f5737-105">Il s’agit de l’une des nombreuses procédures pas &amp; à pas pour le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="f5737-105">This is one of several walkthroughs for the Security &amp; Compliance Center.</span></span> <span data-ttu-id="f5737-106">Pour voir des procédures pas à pas supplémentaires, consultez la section [Rubriques connexes](#related-topics) .</span><span class="sxs-lookup"><span data-stu-id="f5737-106">To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="f5737-107">Procédure pas à pas : d’un tableau de bord vers un aperçu</span><span class="sxs-lookup"><span data-stu-id="f5737-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="f5737-108">Passons en revue le flux d’un tableau de bord à un rapport vers une vue et une action.</span><span class="sxs-lookup"><span data-stu-id="f5737-108">Let's walk through the flow from a dashboard to a report to an insight and action.</span></span> <span data-ttu-id="f5737-109">(Il s’agit d’un bref exemple d’aide à la [falsification](learn-about-spoof-intelligence.md) .)</span><span class="sxs-lookup"><span data-stu-id="f5737-109">(This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="f5737-110">Nous commençons par le tableau de bord de sécurité dans le [Centre de sécurité &amp; conformité](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="f5737-110">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="f5737-111">(Accédez au \*\*\*\* \> **tableau de bord**gestion des menaces.)</span><span class="sxs-lookup"><span data-stu-id="f5737-111">(Go to **Threat management** \> **Dashboard**.)</span></span><br><span data-ttu-id="f5737-112">![Dans le centre &amp; de sécurité conformité, sélectionnez gestion \> des menaces dans le tableau de bord](../../media/05a38660-eb13-4960-a266-11809c453d95.png)</span><span class="sxs-lookup"><span data-stu-id="f5737-112">![In the Security &amp; Compliance Center, choose Threat management \> Dashboard](../../media/05a38660-eb13-4960-a266-11809c453d95.png)</span></span><br>
  
2. <span data-ttu-id="f5737-113">Dans la ligne **Insights** , nous constatons un aperçu indiquant que nous devons examiner certains domaines suspects.</span><span class="sxs-lookup"><span data-stu-id="f5737-113">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious.</span></span> <span data-ttu-id="f5737-114">(Dans la ligne **Insights** , cliquez sur **paires de domaines**.)</span><span class="sxs-lookup"><span data-stu-id="f5737-114">(In the **Insights** row, click **Domain pairs**.)</span></span><br><span data-ttu-id="f5737-115">![La ligne Insights mentionne les préoccupations potentielles d’usurpation d’identité](../../media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)</span><span class="sxs-lookup"><span data-stu-id="f5737-115">![The Insights row mentions potential spoofing concerns](../../media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)</span></span><br>
  
3. <span data-ttu-id="f5737-116">Nous obtenons une liste d’activités liées à l’aide à l’usurpation d’identité.</span><span class="sxs-lookup"><span data-stu-id="f5737-116">We get a list of activities related to spoof intelligence.</span></span> <span data-ttu-id="f5737-117">Il s’agit des instances dans lesquelles des messages électroniques qui semblent provenir de notre organisation ont été envoyés à partir d’une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="f5737-117">These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization.</span></span> <span data-ttu-id="f5737-118">L’objectif est de déterminer si les messages falsifiés sont autorisés ou non.</span><span class="sxs-lookup"><span data-stu-id="f5737-118">The goal is to determine whether the spoofed messages are authorized or not.</span></span><br><span data-ttu-id="f5737-119">![Idées d’aide à la décision](../../media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)</span><span class="sxs-lookup"><span data-stu-id="f5737-119">![Spoof intelligence insights](../../media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)</span></span><br><span data-ttu-id="f5737-120">Dans cette liste, nous pouvons trier les informations par nombre de messages, la date de la dernière détection de l’usurpation et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="f5737-120">In this list, we can sort the information by message count, date the spoofing was last detected, and more.</span></span> <span data-ttu-id="f5737-121">(Cliquez sur les en-têtes de colonne, par exemple **nombre de messages** ou **Dernière vue** pour voir comment le tri fonctionne.)</span><span class="sxs-lookup"><span data-stu-id="f5737-121">(Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="f5737-122">La sélection d’un élément dans la liste ouvre un volet de détails dans lequel nous pouvons voir des informations supplémentaires, notamment des messages électroniques similaires détectés.</span><span class="sxs-lookup"><span data-stu-id="f5737-122">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected.</span></span> <span data-ttu-id="f5737-123">(Cliquez sur un élément dans la liste, puis examinez les informations et les recommandations.)</span><span class="sxs-lookup"><span data-stu-id="f5737-123">(Click an item in the list, and review the information and recommendations.)</span></span><br>![La sélection d’un élément ouvre un volet d’informations](../../media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)<br>
  
5. <span data-ttu-id="f5737-125">Notez que dans la partie supérieure du volet, nous avons la possibilité d’ajouter l’expéditeur à la liste des expéditeurs autorisés de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f5737-125">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list.</span></span> <span data-ttu-id="f5737-126">(Ne sélectionnez pas **Ajouter à la liste verte de l’expéditeur « AllowedtoSpoof »** jusqu’à ce que vous soyez sûr de vouloir effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="f5737-126">(Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this.</span></span> <span data-ttu-id="f5737-127">[En savoir plus sur les informations d’usurpation d’identité](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="f5737-127">[Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span><br><span data-ttu-id="f5737-128">![Vous pouvez autoriser un expéditeur](../../media/caf0c20a-6047-486d-8060-5a229a3de49f.png)</span><span class="sxs-lookup"><span data-stu-id="f5737-128">![You can authorize a sender](../../media/caf0c20a-6047-486d-8060-5a229a3de49f.png)</span></span>
  
<span data-ttu-id="f5737-129">De cette façon, nous pouvons passer d’un tableau de bord à Insights et aux actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="f5737-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="f5737-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5737-130">Related topics</span></span>

[<span data-ttu-id="f5737-131">Procédure pas à pas : d’un aperçu d’un rapport détaillé</span><span class="sxs-lookup"><span data-stu-id="f5737-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="f5737-132">Procédure pas à pas : d’un rapport détaillé vers un aperçu</span><span class="sxs-lookup"><span data-stu-id="f5737-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

