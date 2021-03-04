---
title: Affichage des rapports de protection contre la perte de données
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/7/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.custom: seo-marvel-apr2020
description: Utilisez les rapports DLP dans Office 365 pour afficher le nombre de correspondances, remplacements ou faux positifs de stratégie DLP et voir s’ils sont à la hausse ou à la baisse au fil du temps.
ms.openlocfilehash: eb281f4d912a9e21716d7f9859564a02f9c23401
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50423827"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="b657d-103">Affichage des rapports de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="b657d-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="b657d-104">Après avoir créé vos stratégies de protection contre la perte de données (DLP), vous devez vérifier qu’elles fonctionnent comme prévu et vous aident à maintenir la conformité.</span><span class="sxs-lookup"><span data-stu-id="b657d-104">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant.</span></span> <span data-ttu-id="b657d-105">Avec les rapports DLP dans le Centre de conformité de &amp; sécurité, vous pouvez rapidement afficher :</span><span class="sxs-lookup"><span data-stu-id="b657d-105">With the DLP reports in the Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="b657d-106">**Correspondances de stratégie DLP** Ce rapport indique le nombre de correspondances de stratégies DLP au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="b657d-106">**DLP policy matches** This report shows the count of DLP policy matches over time.</span></span> <span data-ttu-id="b657d-107">Vous pouvez filtrer les rapports par date, emplacement, stratégie ou action.</span><span class="sxs-lookup"><span data-stu-id="b657d-107">You can filter the report by date, location, policy, or action.</span></span> <span data-ttu-id="b657d-108">Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="b657d-108">You can use this report to:</span></span> 
    
  - <span data-ttu-id="b657d-109">Optimiser ou affiner vos stratégies DLP lorsque vous les exécutez en mode test.</span><span class="sxs-lookup"><span data-stu-id="b657d-109">Tune or refine your DLP policies as you run them in test mode.</span></span> <span data-ttu-id="b657d-110">Vous pouvez afficher la règle spécifique qui correspond au contenu.</span><span class="sxs-lookup"><span data-stu-id="b657d-110">You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="b657d-111">Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.</span><span class="sxs-lookup"><span data-stu-id="b657d-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="b657d-112">Découvrir les processus d’entreprise qui enfreignent les stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b657d-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="b657d-113">Comprendre l’impact des stratégies DLP sur l’entreprise en voyant quelles actions sont appliquées au contenu.</span><span class="sxs-lookup"><span data-stu-id="b657d-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="b657d-114">Vérifier la conformité avec une stratégie DLP spécifique en affichant les correspondances pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="b657d-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="b657d-115">Afficher la liste des principaux utilisateurs et répéter les utilisateurs qui contribuent aux incidents au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b657d-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="b657d-116">Consulter la liste des principaux types d’informations sensibles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b657d-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="b657d-117">**Incidents DLP** Ce rapport affiche également les correspondances de stratégie au fil du temps, comme le rapport de correspondances de stratégie.</span><span class="sxs-lookup"><span data-stu-id="b657d-117">**DLP incidents** This report also shows policy matches over time, like the policy matches report.</span></span> <span data-ttu-id="b657d-118">Toutefois, le rapport de correspondances de stratégie affiche les correspondances au niveau d’une règle ; par exemple, si un e-mail correspond à trois règles différentes, le rapport de correspondances de stratégie affiche trois lignes différentes.</span><span class="sxs-lookup"><span data-stu-id="b657d-118">However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items.</span></span> <span data-ttu-id="b657d-119">En revanche, le rapport des incidents affiche les correspondances au niveau de l’élément ; par exemple, si un message électronique correspond à trois règles différentes, le rapport d’incidents affiche un élément de ligne unique pour cet élément de contenu.</span><span class="sxs-lookup"><span data-stu-id="b657d-119">By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="b657d-120">Étant donné que le nombre de rapports est agrégé différemment, le rapport de correspondances de stratégie est préférable pour identifier les correspondances avec des règles spécifiques et affiner les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="b657d-120">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies.</span></span> <span data-ttu-id="b657d-121">Le rapport sur les incidents est préférable pour identifier des éléments de contenu spécifiques qui sont problématiques pour vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="b657d-121">The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="b657d-122">**Remplacements et faux positifs DLP** Si votre stratégie DLP permet aux utilisateurs de la remplacer ou de signaler un faux positif, ce rapport indique le nombre de ces instances au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="b657d-122">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time.</span></span> <span data-ttu-id="b657d-123">Vous pouvez filtrer les rapports par date, emplacement, ou stratégie.</span><span class="sxs-lookup"><span data-stu-id="b657d-123">You can filter the report by date, location, or policy.</span></span> <span data-ttu-id="b657d-124">Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="b657d-124">You can use this report to:</span></span> 
    
  - <span data-ttu-id="b657d-125">Optimiser ou affiner vos stratégies DLP en examinant les stratégies qui impliquent un nombre élevé de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="b657d-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="b657d-126">Afficher les motifs présentés par les utilisateurs lorsqu'ils passent outre une stratégie.</span><span class="sxs-lookup"><span data-stu-id="b657d-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="b657d-127">Découvrir où les stratégies DLP entrent en conflit avec des processus professionnels valides en raison d'un nombre élevé de remplacements de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b657d-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="b657d-128">Tous les rapports DLP peuvent afficher les données de la période de quatre mois la plus récente.</span><span class="sxs-lookup"><span data-stu-id="b657d-128">All DLP reports can show data from the most recent four-month time period.</span></span> <span data-ttu-id="b657d-129">Les données les plus récentes peuvent nécessiter jusqu'à 24 heures avant de s’afficher dans les rapports.</span><span class="sxs-lookup"><span data-stu-id="b657d-129">The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="b657d-130">Vous trouverez ces rapports dans le tableau de bord des rapports du Centre de conformité &amp; \> **de** \> **sécurité.**</span><span class="sxs-lookup"><span data-stu-id="b657d-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![Rapport sur les correspondances de stratégie DLP](../media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="b657d-132">Afficher la justification envoyée par un utilisateur pour un remplacement</span><span class="sxs-lookup"><span data-stu-id="b657d-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="b657d-133">Si votre stratégie DLP permet aux utilisateurs de la remplacer, vous pouvez utiliser le rapport faux positif et de remplacement pour afficher le texte envoyé par les utilisateurs dans le conseil de stratégie.</span><span class="sxs-lookup"><span data-stu-id="b657d-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Champ Justification dans les détails du rapport DLP sur les faux positifs et les remplacements](../media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="b657d-135">Prendre des mesures sur les informations et les recommandations</span><span class="sxs-lookup"><span data-stu-id="b657d-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="b657d-136">Les rapports peuvent afficher des informations et des recommandations dans le cas où vous pouvez cliquer sur l’icône d’avertissement rouge pour afficher des détails sur les problèmes potentiels et prendre des mesures correctives possibles.</span><span class="sxs-lookup"><span data-stu-id="b657d-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![Cliquer sur une icône d’informations pour voir les détails et les actions à prendre](../media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="permissions-for-dlp-reports"></a><span data-ttu-id="b657d-138">Autorisations pour les rapports DLP</span><span class="sxs-lookup"><span data-stu-id="b657d-138">Permissions for DLP reports</span></span>

<span data-ttu-id="b657d-139">Pour afficher les rapports DLP dans le Centre de sécurité & conformité, vous devez avoir :</span><span class="sxs-lookup"><span data-stu-id="b657d-139">To view DLP reports in the Security & Compliance Center, you have to be assigned the:</span></span>

- <span data-ttu-id="b657d-140">**Rôle lecteur sécurité** dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b657d-140">**Security Reader** role in the Exchange admin center.</span></span> <span data-ttu-id="b657d-141">Par défaut, ce rôle est attribué aux groupes de rôles Gestion de l’organisation et Lecteur sécurité dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b657d-141">By default, this role is assigned to the Organization Management and Security Reader role groups in the Exchange admin center.</span></span>

- <span data-ttu-id="b657d-142">**Rôle de gestion de la conformité DLP** en affichage seul dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b657d-142">**View-Only DLP Compliance Management** role in the Security & Compliance Center.</span></span> <span data-ttu-id="b657d-143">Par défaut, ce rôle est attribué aux groupes de rôles Administrateur de conformité, Gestion de l’organisation, Administrateur de la sécurité et Lecteur sécurité dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b657d-143">By default, this role is assigned to the Compliance Administrator, Organization Management, Security Administrator, and Security Reader role groups in the Security & Compliance Center.</span></span>

- <span data-ttu-id="b657d-144">**Rôle Destinataires en affichage** seul dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b657d-144">**View-Only Recipients** role in the Exchange admin center.</span></span> <span data-ttu-id="b657d-145">Par défaut, ce rôle est attribué aux groupes de rôles Gestion de la conformité, Gestion de l’organisation View-Only Gestion de l’organisation dans le Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="b657d-145">By default, this role is assigned to the Compliance Management, Organization Management, and View-Only Organization Management role groups in the Exchange admin center.</span></span>

## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="b657d-146">Rechercher les cmdlets pour les rapports DLP</span><span class="sxs-lookup"><span data-stu-id="b657d-146">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="b657d-147">Pour utiliser la plupart des applets de commande du Centre de conformité et de sécurité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="b657d-147">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="b657d-148">Se connecter au Centre de conformité &amp; de sécurité à l’aide de PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="b657d-148">Connect to the Security &amp; Compliance Center using remote PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell&amp;clcid=0x409)
    
2. <span data-ttu-id="b657d-149">Utiliser l’une de ces [ &amp; cmdlets du Centre](https://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409) de conformité de la sécurité</span><span class="sxs-lookup"><span data-stu-id="b657d-149">Use any of these [Security &amp; Compliance Center cmdlets](https://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="b657d-150">Toutefois, les rapports DLP doivent extraire des d’Office 365, y compris Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b657d-150">However, DLP reports need pull data from across Office 365, including Exchange Online.</span></span> <span data-ttu-id="b657d-151">Pour cette raison, les cmdlets pour les rapports DLP sont disponibles dans Exchange Online Powershell, et non dans le Centre de conformité de &amp; sécurité Powershell.</span><span class="sxs-lookup"><span data-stu-id="b657d-151">For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell.</span></span> <span data-ttu-id="b657d-152">Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :</span><span class="sxs-lookup"><span data-stu-id="b657d-152">Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="b657d-153">Vous connecter à Exchange Online à l'aide de Remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="b657d-153">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="b657d-154">Utilisez l’une de ces applets de commande pour les rapports DLP :</span><span class="sxs-lookup"><span data-stu-id="b657d-154">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="b657d-155">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="b657d-155">Get-DlpDetectionsReport</span></span>](https://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="b657d-156">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="b657d-156">Get-DlpDetailReport</span></span>](https://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

