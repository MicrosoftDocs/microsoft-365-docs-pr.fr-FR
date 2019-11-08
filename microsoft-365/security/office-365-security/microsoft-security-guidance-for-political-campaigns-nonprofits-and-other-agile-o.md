---
title: Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.custom: Strat_O365_Enterprise
ms.assetid: 10d1004b-42b6-4e2b-aaa2-18ddd9118f64
description: 'Résumé : Conseils de planification et d’implémentation pour les organisations à développement rapide présentant un profil susceptible d’attirer les menaces.'
ms.openlocfilehash: 1fadb65b4f2231b99764230294ac3685113a2226
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38032259"
---
# <a name="microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-organizations"></a><span data-ttu-id="a9aaf-103">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="a9aaf-103">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>

 <span data-ttu-id="a9aaf-104">**Résumé :** Conseils de planification et d’implémentation pour les organisations à développement rapide présentant un profil susceptible d’attirer les menaces.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-104">**Summary:** Planning and implementation guidance for fast-moving organizations that have an increased threat profile.</span></span>
  
<span data-ttu-id="a9aaf-p101">Si votre organisation est flexible, que votre équipe informatique est de taille réduite et que vous êtes plus susceptible de faire l’objet de menaces que la moyenne, ces conseils s’adressent à vous. Cette solution montre comment créer rapidement un environnement avec des services cloud essentiels, notamment des contrôles sécurisés dès le début. Vous trouverez dans cet article des recommandations normatives en matière de sécurité pour assurer la protection des données, des identités, des courriers électroniques et de l’accès à partir d’appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-p101">If your organization is agile, you have a small IT team, and your threat profile is higher than average, this guidance is designed for you. This solution demonstrates how to quickly build an environment with essential cloud services that include secure controls from the start. This guidance includes prescriptive security recommendations for protecting data, identities, email, and access from mobile devices.</span></span>
  
## <a name="security-solution-guidance"></a><span data-ttu-id="a9aaf-108">Guide des solutions de sécurité</span><span class="sxs-lookup"><span data-stu-id="a9aaf-108">Security solution guidance</span></span>

<span data-ttu-id="a9aaf-p102">Ce guide décrit comment implémenter un environnement cloud sécurisé. Ce guide des solutions peut être utilisé par n’importe quelle organisation. Il inclut une aide supplémentaire pour les organisations agiles avec des accès et des comptes d’invité BYOD. Vous pouvez utiliser ce guide comme point de départ pour concevoir votre propre environnement. Vos commentaires sont bienvenus ; vous pouvez les envoyer à [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a9aaf-p102">This guidance describes how to implement a secure cloud environment. The solution guidance can be used by any organization. It includes extra help for agile organizations with BYOD access and guest accounts. You can use this guidance as a starting-point for designing your own environment. We welcome your feedback at [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9aaf-114">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a9aaf-114">**Item**</span></span> <br/> |<span data-ttu-id="a9aaf-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a9aaf-115">**Description**</span></span> <br/> |
|<span data-ttu-id="a9aaf-116">**Conseils de sécurité Microsoft pour les campagnes politiques**</span><span class="sxs-lookup"><span data-stu-id="a9aaf-116">**Microsoft Security Guidance for Political Campaigns**</span></span> <br/> <span data-ttu-id="a9aaf-117">[![Miniature pour ensemble de mini affiches.](../media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span><span class="sxs-lookup"><span data-stu-id="a9aaf-117">[![Thumb nail for mini poster set.](../media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span></span> <br/> <span data-ttu-id="a9aaf-118">[PDF](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span><span class="sxs-lookup"><span data-stu-id="a9aaf-118">[PDF](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span></span> <br/> |<span data-ttu-id="a9aaf-p103">Ce guide utilise un exemple d’organisation de campagne politique. Utilisez-le comme point de départ pour n’importe quel environnement.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-p103">This guidance uses a political campaign organization as an example. Use this guidance as a starting point for any environment.</span></span>  <br/> |
|<span data-ttu-id="a9aaf-121">**Conseils de sécurité Microsoft pour les organisations à but non lucratif**</span><span class="sxs-lookup"><span data-stu-id="a9aaf-121">**Microsoft Security Guidance for Nonprofits**</span></span> <br/> <span data-ttu-id="a9aaf-122">[![Image miniature pour le fichier téléchargeable](../media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span><span class="sxs-lookup"><span data-stu-id="a9aaf-122">[![Thumnail image for downloadable file](../media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span></span> <br/> <span data-ttu-id="a9aaf-123">[PDF](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span><span class="sxs-lookup"><span data-stu-id="a9aaf-123">[PDF](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span></span> <br/> |<span data-ttu-id="a9aaf-p104">Ce guide a été légèrement révisé pour les organisations à but non lucratif. Par exemple, il répertorie les plans Office 365 pour les associations. Les consignes technique fournies sont les mêmes que dans le guide de solution de campagne politique.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-p104">This guide is slightly revised for nonprofit organizations. For example, it references Office 365 Nonprofit plans. The technical guidance is the same as the political campaign solution guide.</span></span>  <br/> |
   
## <a name="test-lab-guides"></a><span data-ttu-id="a9aaf-127">Guides pour les laboratoires de tests</span><span class="sxs-lookup"><span data-stu-id="a9aaf-127">Test Lab Guides</span></span>

<span data-ttu-id="a9aaf-128">Pour créer un environnement de développement/test pour cette solution, utilisez les guides de laboratoire de test suivants :</span><span class="sxs-lookup"><span data-stu-id="a9aaf-128">To create a dev/test environment for this solution, use the following test lab guides:</span></span> 
  
- [<span data-ttu-id="a9aaf-129">Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="a9aaf-129">Configure groups and users for a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/configure-groups-and-users-for-a-political-campaign-dev-test-environment)
    
     <span data-ttu-id="a9aaf-130">Créez des abonnements à la version d’évaluation pour Office 365 et EMS, puis créez des groupes et des utilisateurs pour une campagne électorale représentative.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-130">Create trial subscriptions for Office 365 and EMS and then create groups and users for a representative political campaign.</span></span>
    
- [<span data-ttu-id="a9aaf-131">Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="a9aaf-131">Create team sites in a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/create-team-sites-in-a-political-campaign-dev-test-environment)
    
    <span data-ttu-id="a9aaf-132">Créez quatre sites d’équipe SharePoint Online ayant respectivement le niveau de sécurité Interne, Privé, Sensible et Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="a9aaf-132">Create four SharePoint Online team sites with Internal, Private, Sensitive, and Highly Confidential levels of security.</span></span>
    
<span data-ttu-id="a9aaf-133">Pour des fonctionnalités de sécurité supplémentaires pour la démonstration de validation de concept, consultez les [Guides de laboratoire de test pour Office 365](https://aka.ms/o365tlgs).</span><span class="sxs-lookup"><span data-stu-id="a9aaf-133">For additional security features for demonstration or proof of concept, see [Office 365 Test Lab Guides](https://aka.ms/o365tlgs).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9aaf-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9aaf-134">See Also</span></span>

[<span data-ttu-id="a9aaf-135">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="a9aaf-135">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="a9aaf-136">Ressources relatives à l’architecture informatique du cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="a9aaf-136">Microsoft Cloud IT architecture resources</span></span>](https://docs.microsoft.com/office365/enterprise/microsoft-cloud-it-architecture-resources)



