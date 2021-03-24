---
title: 'Conseils de sécurité Microsoft : campagnes politiques et organisations à but non lucratif'
f1.keywords:
- NOCSH
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
localization_priority: Priority
search.appverid:
- MET150
ms.custom:
- Strat_O365_Enterprise
- seo-marvel-apr2020
ms.assetid: 10d1004b-42b6-4e2b-aaa2-18ddd9118f64
description: 'Résumé : Conseils de planification et d’implémentation pour les organisations à développement rapide présentant un profil susceptible d’attirer les menaces.'
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ac278103caf5d4d70b303b50b73db1b4b3571e6b
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51061934"
---
# <a name="microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-organizations"></a><span data-ttu-id="6b82d-103">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="6b82d-103">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="6b82d-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6b82d-104">**Applies to**</span></span>
- [<span data-ttu-id="6b82d-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="6b82d-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="6b82d-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="6b82d-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)

 <span data-ttu-id="6b82d-107">**Résumé :** Conseils de planification et d’implémentation pour les organisations à développement rapide présentant un profil susceptible d’attirer les menaces.</span><span class="sxs-lookup"><span data-stu-id="6b82d-107">**Summary:** Planning and implementation guidance for fast-moving organizations that have an increased threat profile.</span></span>

<span data-ttu-id="6b82d-p101">Si votre organisation est flexible, que votre équipe informatique est de taille réduite et que vous êtes plus susceptible de faire l’objet de menaces que la moyenne, ces conseils s’adressent à vous. Cette solution montre comment créer rapidement un environnement avec des services cloud essentiels, notamment des contrôles sécurisés dès le début. Vous trouverez dans cet article des recommandations normatives en matière de sécurité pour assurer la protection des données, des identités, des courriers électroniques et de l’accès à partir d’appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="6b82d-p101">If your organization is agile, you have a small IT team, and your threat profile is higher than average, this guidance is designed for you. This solution demonstrates how to quickly build an environment with essential cloud services that include secure controls from the start. This guidance includes prescriptive security recommendations for protecting data, identities, email, and access from mobile devices.</span></span>

## <a name="security-solution-guidance"></a><span data-ttu-id="6b82d-111">Guide des solutions de sécurité</span><span class="sxs-lookup"><span data-stu-id="6b82d-111">Security solution guidance</span></span>

<span data-ttu-id="6b82d-p102">Ce guide décrit comment implémenter un environnement cloud sécurisé. Ce guide des solutions peut être utilisé par n’importe quelle organisation. Il inclut une aide supplémentaire pour les organisations agiles avec des accès et des comptes d’invité BYOD. Vous pouvez utiliser ce guide comme point de départ pour concevoir votre propre environnement. Vos commentaires sont bienvenus ; vous pouvez les envoyer à [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6b82d-p102">This guidance describes how to implement a secure cloud environment. The solution guidance can be used by any organization. It includes extra help for agile organizations with BYOD access and guest accounts. You can use this guidance as a starting-point for designing your own environment. We welcome your feedback at [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span></span>

****

|<span data-ttu-id="6b82d-117">Item</span><span class="sxs-lookup"><span data-stu-id="6b82d-117">Item</span></span>|<span data-ttu-id="6b82d-118">Description</span><span class="sxs-lookup"><span data-stu-id="6b82d-118">Description</span></span>|
|---|---|
|<span data-ttu-id="6b82d-119">**Conseils de sécurité Microsoft pour les campagnes politiques**</span><span class="sxs-lookup"><span data-stu-id="6b82d-119">**Microsoft Security Guidance for Political Campaigns**</span></span> <br> <span data-ttu-id="6b82d-120">[![Miniature pour mini poster](../../media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span><span class="sxs-lookup"><span data-stu-id="6b82d-120">[![Thumbnail for mini poster set.](../../media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span></span> <br> <span data-ttu-id="6b82d-121">[PDF](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf) \| [Visio](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span><span class="sxs-lookup"><span data-stu-id="6b82d-121">[PDF](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf) \| [Visio](https://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span></span>|<span data-ttu-id="6b82d-p103">Ce guide utilise un exemple d’organisation de campagne politique. Utilisez-le comme point de départ pour n’importe quel environnement.</span><span class="sxs-lookup"><span data-stu-id="6b82d-p103">This guidance uses a political campaign organization as an example. Use this guidance as a starting point for any environment.</span></span>|
|<span data-ttu-id="6b82d-124">**Conseils de sécurité Microsoft pour les organisations à but non lucratif**</span><span class="sxs-lookup"><span data-stu-id="6b82d-124">**Microsoft Security Guidance for Nonprofits**</span></span> <br> <span data-ttu-id="6b82d-125">[![Image miniature pour le fichier téléchargeable](../../media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span><span class="sxs-lookup"><span data-stu-id="6b82d-125">[![Thumbnail image for downloadable file](../../media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span></span> <br> <span data-ttu-id="6b82d-126">[PDF](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf) \| [Visio](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span><span class="sxs-lookup"><span data-stu-id="6b82d-126">[PDF](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf) \| [Visio](https://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span></span>|<span data-ttu-id="6b82d-p104">Ce guide a été légèrement révisé pour les organisations à but non lucratif. Par exemple, il répertorie les plans Office 365 pour les associations. Les consignes technique fournies sont les mêmes que dans le guide de solution de campagne politique.</span><span class="sxs-lookup"><span data-stu-id="6b82d-p104">This guide is slightly revised for nonprofit organizations. For example, it references Office 365 Nonprofit plans. The technical guidance is the same as the political campaign solution guide.</span></span>|
|

## <a name="test-lab-guides"></a><span data-ttu-id="6b82d-130">Guides pour les laboratoires de tests</span><span class="sxs-lookup"><span data-stu-id="6b82d-130">Test Lab Guides</span></span>

<span data-ttu-id="6b82d-131">Pour créer un environnement de développement/test pour cette solution, utilisez les guides de laboratoire de test suivants :</span><span class="sxs-lookup"><span data-stu-id="6b82d-131">To create a dev/test environment for this solution, use the following test lab guides:</span></span>

- [<span data-ttu-id="6b82d-132">Configuration de groupes et d’utilisateurs pour un environnement de développement/test pour une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="6b82d-132">Configure groups and users for a political campaign dev/test environment</span></span>](configure-groups-and-users-for-a-political-campaign-dev-test-environment.md)

  <span data-ttu-id="6b82d-133">Créez des abonnements à la version d’évaluation pour Office 365 et EMS, puis créez des groupes et des utilisateurs pour une campagne électorale représentative.</span><span class="sxs-lookup"><span data-stu-id="6b82d-133">Create trial subscriptions for Office 365 and EMS and then create groups and users for a representative political campaign.</span></span>

- [<span data-ttu-id="6b82d-134">Création de sites d’équipe dans un environnement de développement/test dans le cadre d’une campagne électorale</span><span class="sxs-lookup"><span data-stu-id="6b82d-134">Create team sites in a political campaign dev/test environment</span></span>](create-team-sites-in-a-political-campaign-dev-test-environment.md)

  <span data-ttu-id="6b82d-135">Créez quatre sites d’équipe SharePoint Online ayant respectivement le niveau de sécurité Interne, Privé, Sensible et Hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="6b82d-135">Create four SharePoint Online team sites with Internal, Private, Sensitive, and Highly Confidential levels of security.</span></span>

<span data-ttu-id="6b82d-136">Pour des fonctionnalités de sécurité supplémentaires pour la démonstration de validation de concept, consultez les [Guides de laboratoire de test pour Office 365](../../enterprise/cloud-adoption-test-lab-guides-tlgs.md).</span><span class="sxs-lookup"><span data-stu-id="6b82d-136">For additional security features for demonstration or proof of concept, see [Office 365 Test Lab Guides](../../enterprise/cloud-adoption-test-lab-guides-tlgs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b82d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b82d-137">See Also</span></span>

[<span data-ttu-id="6b82d-138">Ressources relatives à l'architecture informatique du cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b82d-138">Microsoft Cloud IT architecture resources</span></span>](../../solutions/cloud-architecture-models.md)
