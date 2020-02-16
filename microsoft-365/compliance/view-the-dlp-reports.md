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
description: Avec les rapports DLP dans Office 365, vous pouvez rapidement afficher le nombre de correspondances de stratégies DLP, de remplacements ou de faux positifs ; voir si elles sont recherchées dans le temps ; filtrer le rapport de différentes manières ; et affichez des détails supplémentaires en sélectionnant un point sur une ligne sur le graphique.
ms.openlocfilehash: c00047680f684e3845c4383face09c2cee579721
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42068751"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="85cd0-103">Affichage des rapports de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="85cd0-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="85cd0-104">Après avoir créé vos stratégies de protection contre la perte de données (DLP), vous souhaiterez vérifier qu’elles fonctionnent comme vous le souhaitez et vous aider à rester conformes.</span><span class="sxs-lookup"><span data-stu-id="85cd0-104">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant.</span></span> <span data-ttu-id="85cd0-105">Les rapports DLP du centre de sécurité &amp; conformité Office 365 vous permettent d’afficher rapidement les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="85cd0-105">With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="85cd0-106">**Correspondances de stratégie DLP** Ce rapport indique le nombre de correspondances de stratégie DLP dans le temps.</span><span class="sxs-lookup"><span data-stu-id="85cd0-106">**DLP policy matches** This report shows the count of DLP policy matches over time.</span></span> <span data-ttu-id="85cd0-107">Vous pouvez filtrer le rapport par date, emplacement, stratégie ou action.</span><span class="sxs-lookup"><span data-stu-id="85cd0-107">You can filter the report by date, location, policy, or action.</span></span> <span data-ttu-id="85cd0-108">Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="85cd0-108">You can use this report to:</span></span> 
    
  - <span data-ttu-id="85cd0-109">Réglez ou Affinez vos stratégies DLP lorsque vous les exécutez en mode test.</span><span class="sxs-lookup"><span data-stu-id="85cd0-109">Tune or refine your DLP policies as you run them in test mode.</span></span> <span data-ttu-id="85cd0-110">Vous pouvez afficher la règle spécifique qui correspond au contenu.</span><span class="sxs-lookup"><span data-stu-id="85cd0-110">You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="85cd0-111">Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.</span><span class="sxs-lookup"><span data-stu-id="85cd0-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="85cd0-112">Découvrir les processus d’entreprise qui enfreignent les stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85cd0-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="85cd0-113">Comprendre l’impact des stratégies DLP sur l’entreprise en examinant les actions appliquées au contenu.</span><span class="sxs-lookup"><span data-stu-id="85cd0-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="85cd0-114">Vérifier la conformité avec une stratégie DLP spécifique en affichant les correspondances pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="85cd0-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="85cd0-115">Affichez la liste des utilisateurs les plus fréquents et répétez les utilisateurs qui contribuent aux incidents de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85cd0-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="85cd0-116">Affichez la liste des principaux types d’informations sensibles dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85cd0-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="85cd0-117">**Incidents DLP** Ce rapport affiche également les correspondances de stratégie dans le temps, comme la stratégie établit le rapport.</span><span class="sxs-lookup"><span data-stu-id="85cd0-117">**DLP incidents** This report also shows policy matches over time, like the policy matches report.</span></span> <span data-ttu-id="85cd0-118">Toutefois, le rapport sur les correspondances de stratégie indique les correspondances au niveau de la règle ; par exemple, si un message électronique correspond à trois règles différentes, la stratégie correspond à un rapport affiche trois éléments de ligne différents.</span><span class="sxs-lookup"><span data-stu-id="85cd0-118">However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items.</span></span> <span data-ttu-id="85cd0-119">En revanche, le rapport incidents affiche les correspondances au niveau de l’élément ; par exemple, si un message électronique correspond à trois règles différentes, le rapport incidents affiche un seul élément de ligne pour cette partie de contenu.</span><span class="sxs-lookup"><span data-stu-id="85cd0-119">By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="85cd0-120">Étant donné que le nombre de rapports est agrégé différemment, la stratégie établit une correspondance avec le rapport pour identifier les correspondances avec des règles spécifiques et ajuster les stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="85cd0-120">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies.</span></span> <span data-ttu-id="85cd0-121">Le rapport incidents est plus approprié pour identifier des parties de contenu spécifiques qui sont problématiques pour vos stratégies DLP.</span><span class="sxs-lookup"><span data-stu-id="85cd0-121">The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="85cd0-122">**Les faux positifs et les remplacements DLP** Si votre stratégie DLP permet aux utilisateurs de la remplacer ou de signaler un faux positif, ce rapport affiche un décompte de ces instances dans le temps.</span><span class="sxs-lookup"><span data-stu-id="85cd0-122">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time.</span></span> <span data-ttu-id="85cd0-123">Vous pouvez filtrer le rapport par date, par emplacement ou par stratégie.</span><span class="sxs-lookup"><span data-stu-id="85cd0-123">You can filter the report by date, location, or policy.</span></span> <span data-ttu-id="85cd0-124">Vous pouvez utiliser ce rapport pour :</span><span class="sxs-lookup"><span data-stu-id="85cd0-124">You can use this report to:</span></span> 
    
  - <span data-ttu-id="85cd0-125">Ajuster ou affiner vos stratégies DLP en examinant les stratégies qui impliquent un nombre élevé de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="85cd0-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="85cd0-126">Affichez les justifications soumises par les utilisateurs lorsqu’ils résolvent un Conseil de stratégie en substituant la stratégie.</span><span class="sxs-lookup"><span data-stu-id="85cd0-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="85cd0-127">Découvrez comment les stratégies DLP entrent en conflit avec les processus d’entreprise valides en raison d’un nombre élevé de remplacements utilisateur.</span><span class="sxs-lookup"><span data-stu-id="85cd0-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="85cd0-128">Tous les rapports DLP peuvent afficher les données de la période de quatre mois la plus récente.</span><span class="sxs-lookup"><span data-stu-id="85cd0-128">All DLP reports can show data from the most recent four-month time period.</span></span> <span data-ttu-id="85cd0-129">Les données les plus récentes peuvent prendre jusqu’à 24 heures pour apparaître dans les rapports.</span><span class="sxs-lookup"><span data-stu-id="85cd0-129">The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="85cd0-130">Ces rapports sont disponibles dans le tableau de &amp; **bord**rapports \> \*\*\*\* \> du centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="85cd0-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![Rapport de correspondances de stratégie DLP](../media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="85cd0-132">Afficher la justification envoyée par un utilisateur pour une substitution</span><span class="sxs-lookup"><span data-stu-id="85cd0-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="85cd0-133">Si votre stratégie DLP permet aux utilisateurs de la remplacer, vous pouvez utiliser le rapport de faux positif et de remplacement pour afficher le texte soumis par les utilisateurs dans le Conseil de stratégie.</span><span class="sxs-lookup"><span data-stu-id="85cd0-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Champ justification dans les détails du rapport de faux positifs et de remplacement DLP](../media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="85cd0-135">Prendre des mesures sur les informations et les recommandations</span><span class="sxs-lookup"><span data-stu-id="85cd0-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="85cd0-136">Les rapports peuvent indiquer des informations et des recommandations où vous pouvez cliquer sur l’icône d’avertissement rouge pour afficher des détails sur les problèmes potentiels et prendre des mesures correctives possibles.</span><span class="sxs-lookup"><span data-stu-id="85cd0-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![Cliquer sur une icône Insights pour afficher les détails et les actions à effectuer](../media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="permissions-for-dlp-reports"></a><span data-ttu-id="85cd0-138">Autorisations pour les rapports DLP</span><span class="sxs-lookup"><span data-stu-id="85cd0-138">Permissions for DLP reports</span></span>

<span data-ttu-id="85cd0-139">Pour afficher les rapports DLP dans le centre de sécurité & conformité, vous devez disposer des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="85cd0-139">To view DLP reports in the Security & Compliance Center, you have to be assigned the:</span></span>

- <span data-ttu-id="85cd0-140">Rôle **lecteur de sécurité** dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cd0-140">**Security Reader** role in the Exchange admin center.</span></span> <span data-ttu-id="85cd0-141">Par défaut, ce rôle est affecté aux groupes de rôles gestion de l’organisation et lecteur de sécurité dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cd0-141">By default, this role is assigned to the Organization Management and Security Reader role groups in the Exchange admin center.</span></span>

- <span data-ttu-id="85cd0-142">Rôle de **gestion de conformité DLP en lecture seule** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="85cd0-142">**View-Only DLP Compliance Management** role in the Security & Compliance Center.</span></span> <span data-ttu-id="85cd0-143">Par défaut, ce rôle est affecté aux groupes de rôles Administrateur de conformité, gestion de l’organisation, administrateur de sécurité et lecteur de sécurité dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="85cd0-143">By default, this role is assigned to the Compliance Administrator, Organization Management, Security Administrator, and Security Reader role groups in the Security & Compliance Center.</span></span>

- <span data-ttu-id="85cd0-144">Rôle **destinataires en affichage seul** dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cd0-144">**View-Only Recipients** role in the Exchange admin center.</span></span> <span data-ttu-id="85cd0-145">Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité, gestion de l’organisation et gestion de l’organisation en affichage seul dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cd0-145">By default, this role is assigned to the Compliance Management, Organization Management, and View-Only Organization Management role groups in the Exchange admin center.</span></span>

## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="85cd0-146">Rechercher les applets de commande pour les rapports DLP</span><span class="sxs-lookup"><span data-stu-id="85cd0-146">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="85cd0-147">Pour utiliser la plupart des applets de commande du Centre de conformité et de sécurité, vous devez :</span><span class="sxs-lookup"><span data-stu-id="85cd0-147">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="85cd0-148">Vous connecter au Centre de sécurité &amp; conformité Office 365 à l’aide de PowerShell à distance</span><span class="sxs-lookup"><span data-stu-id="85cd0-148">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="85cd0-149">Utiliser l’une des [applets de &amp; commande du centre de sécurité conformité Office 365](https://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="85cd0-149">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](https://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="85cd0-150">Toutefois, les rapports DLP doivent extraire des d’Office 365, y compris Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="85cd0-150">However, DLP reports need pull data from across Office 365, including Exchange Online.</span></span> <span data-ttu-id="85cd0-151">Pour cette raison, les applets de commande pour les rapports DLP sont disponibles dans Exchange Online PowerShell, et &amp; non dans le centre de sécurité conformité PowerShell.</span><span class="sxs-lookup"><span data-stu-id="85cd0-151">For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell.</span></span> <span data-ttu-id="85cd0-152">Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :</span><span class="sxs-lookup"><span data-stu-id="85cd0-152">Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="85cd0-153">Vous connecter à Exchange Online à l'aide de Remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="85cd0-153">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="85cd0-154">Utilisez l’une de ces applets de commande pour les rapports DLP :</span><span class="sxs-lookup"><span data-stu-id="85cd0-154">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="85cd0-155">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="85cd0-155">Get-DlpDetectionsReport</span></span>](https://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="85cd0-156">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="85cd0-156">Get-DlpDetailReport</span></span>](https://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

