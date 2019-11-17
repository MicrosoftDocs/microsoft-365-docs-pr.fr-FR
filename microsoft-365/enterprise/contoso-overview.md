---
title: Présentation de la société Contoso Corporation
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre le fonctionnement de la société Contoso Corporation et la hiérarchie de ses bureaux internationaux.
ms.openlocfilehash: f1c758b92915845a0786c24aec611cb221c70186
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38673150"
---
# <a name="overview-of-the-contoso-corporation"></a><span data-ttu-id="18588-103">Présentation de la société Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="18588-103">Overview of the Contoso Corporation</span></span>

![Société Contoso](./media/contoso-overview/contoso-icon.png)

<span data-ttu-id="18588-p101">La société Contoso est une entreprise internationale dont le siège est à Paris. Il s’agit d’un conglomérat de production, de ventes et de service après-vente comptant plus de 100 000 produits.</span><span class="sxs-lookup"><span data-stu-id="18588-p101">The Contoso Corporation is a multi-national business with headquarters in Paris, France. It is a conglomerate manufacturing, sales, and support organization with over 100,000 products.</span></span>

## <a name="contoso-around-the-world"></a><span data-ttu-id="18588-107">Contoso dans le monde</span><span class="sxs-lookup"><span data-stu-id="18588-107">Contoso around the world</span></span>

<span data-ttu-id="18588-108">Dans la Figure 1, le siège social de l’entreprise se situe à Paris, tandis que ses centres régionaux et ses succursales sont répartis sur plusieurs continents.</span><span class="sxs-lookup"><span data-stu-id="18588-108">Figure 1 shows the headquarters office in Paris and regional hub and satellite offices in various continents.</span></span>

![Bureaux internationaux de Contoso](./media/contoso-overview/contoso-overview-fig1.png)

<span data-ttu-id="18588-110">**Figure 1 : bureaux internationaux de Contoso**</span><span class="sxs-lookup"><span data-stu-id="18588-110">**Figure 1: Contoso's offices around the world**</span></span>
 
<span data-ttu-id="18588-111">Les bureaux internationaux de Contoso sont organisés en trois niveaux.</span><span class="sxs-lookup"><span data-stu-id="18588-111">Contoso's offices around the world follow a three-tier design.</span></span>

- <span data-ttu-id="18588-112">Siège social</span><span class="sxs-lookup"><span data-stu-id="18588-112">Headquarters</span></span>

  <span data-ttu-id="18588-p102">Le siège social de Contoso Corporation s’intègre à une vaste zone d’activité, dans la banlieue parisienne, comportant des dizaines de bâtiments pour l’administration, l’ingénierie et la fabrication. Tous les centres de données de Contoso et la présence Internet résident dans le siège social.</span><span class="sxs-lookup"><span data-stu-id="18588-p102">The Contoso Corporation headquarters is a large corporate campus on the outskirts of Paris with dozens of buildings for administrative, engineering, and manufacturing facilities. All of Contoso's datacenters and its Internet presence are housed in the Paris headquarters.</span></span>

  <span data-ttu-id="18588-115">Le siège social compte 25 000 collaborateurs.</span><span class="sxs-lookup"><span data-stu-id="18588-115">The headquarters has 25,000 workers.</span></span>

- <span data-ttu-id="18588-116">Centres régionaux</span><span class="sxs-lookup"><span data-stu-id="18588-116">Regional hubs</span></span>

  <span data-ttu-id="18588-p103">Les centres régionaux sont implantés dans différentes régions du monde et possèdent 60 % des équipes des ventes et du support technique. Chaque centre régional est relié au siège social grâce à une connexion WAN haut débit. </span><span class="sxs-lookup"><span data-stu-id="18588-p103">Regional hub offices serve a specific region of the world with 60% sales and support staff. Each regional hub is connected to the Paris headquarters with a high-bandwidth WAN link.</span></span>

  <span data-ttu-id="18588-119">Chaque centre régional compte en moyenne 2 000 collaborateurs.</span><span class="sxs-lookup"><span data-stu-id="18588-119">Each regional hub has an average of 2,000 workers.</span></span>

- <span data-ttu-id="18588-120">Succursales</span><span class="sxs-lookup"><span data-stu-id="18588-120">Satellite offices</span></span>

  <span data-ttu-id="18588-p104">Les succursales représentent 80 % des ventes et du personnel d’assistance et offrent une présence physique et sur site aux clients de Contoso dans les villes importantes ou des régions plus petites. Chaque succursale est connectée à un centre régional par le biais d’un lien WAN haut débit.</span><span class="sxs-lookup"><span data-stu-id="18588-p104">Satellite offices contain 80% sales and support staff and provide an on-site presence for Contoso customers in key cities or sub-regions. Each satellite office is connected to a regional hub with a high-bandwidth WAN link.</span></span>

  <span data-ttu-id="18588-123">Chaque succursale compte en moyenne 250 collaborateurs.</span><span class="sxs-lookup"><span data-stu-id="18588-123">Each satellite office has an average of 250 workers.</span></span>

<span data-ttu-id="18588-p105">25 % des collaborateurs de Contoso travaillent en permanence sur le terrain. Ce pourcentage est supérieur dans les centres régionaux et les succursales.
Pour Contoso, il est essentiel de fournir un meilleur support technique aux collaborateurs qui passent tout leur temps sur le terrain.</span><span class="sxs-lookup"><span data-stu-id="18588-p105">25% of Contoso's workforce is mobile-only, with a higher percentage of mobile-only workers in the regional hubs and satellite offices. Providing better support for mobile-only workers is an important business goal for Contoso.</span></span>

## <a name="design-considerations-for-microsoft-365-enterprise"></a><span data-ttu-id="18588-126">Conceptions envisagées pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="18588-126">Design considerations for Microsoft 365 Enterprise</span></span>

<span data-ttu-id="18588-127">Les architectes informatiques de Contoso ont identifié les exigences et considérations suivantes en matière de conception lors du déploiement de Microsoft 365 Entreprise :</span><span class="sxs-lookup"><span data-stu-id="18588-127">Contoso's IT architects identified the following design requirements and considerations when deploying Microsoft 365 Enterprise:</span></span> 

- <span data-ttu-id="18588-128">Plusieurs implantations géographiques avec des réglementations et des exigences de conformité locales</span><span class="sxs-lookup"><span data-stu-id="18588-128">Multiple geographic locations with local regulations and compliance requirements</span></span>
- <span data-ttu-id="18588-129">Un centre de données intranet central dans les locaux du siège social et des serveurs d’application régionaux qui hébergent en interne la gamme d’applications professionnelles</span><span class="sxs-lookup"><span data-stu-id="18588-129">A central intranet datacenter in the headquarters office and regional application servers that host internal line of business applications</span></span>
- <span data-ttu-id="18588-130">Une infrastructure existante du Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="18588-130">An existing Microsoft Endpoint Configuration Manager infrastructure</span></span>
- <span data-ttu-id="18588-131">Un mélange d’appareils informatiques clients, comprenant Windows, Mac et Linux</span><span class="sxs-lookup"><span data-stu-id="18588-131">A mix of client computing devices, including Windows, Mac, and Linux</span></span>
- <span data-ttu-id="18588-132">Un mélange d’appareils mobiles personnels et entreprise, notamment smartphones et tablettes iOS (iPhone et iPad) et Android</span><span class="sxs-lookup"><span data-stu-id="18588-132">A mix of personal and company-owned mobile devices, including iOS (iPhone and iPad) and Android smart phones and tablets</span></span>
- <span data-ttu-id="18588-133">Nombreux collaborateurs en télétravail et mobiles</span><span class="sxs-lookup"><span data-stu-id="18588-133">Many remote and mobile workers</span></span>
- <span data-ttu-id="18588-134">Nombreux partenaires commerciaux</span><span class="sxs-lookup"><span data-stu-id="18588-134">Many business partners</span></span>
- <span data-ttu-id="18588-135">Une grande quantité de d’informations client et informations d’identification personnelle</span><span class="sxs-lookup"><span data-stu-id="18588-135">A large amount of customer and personally identifiable information</span></span>
- <span data-ttu-id="18588-136">Une grande quantité de propriété intellectuelle de qualité sous forme de directives de conception pour les produits et de secrets commerciaux fabrication</span><span class="sxs-lookup"><span data-stu-id="18588-136">A large amount of high-value intellectual property in the form of design specifications for products and manufacturing trade secrets</span></span>

## <a name="next-step"></a><span data-ttu-id="18588-137">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="18588-137">Next step</span></span>

<span data-ttu-id="18588-138">[En savoir plus](contoso-infra-needs.md) sur l’infrastructure informatique locale de Contoso Corporation et comment leurs besoins commerciaux ont été traités avec Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="18588-138">[Learn](contoso-infra-needs.md) about the Contoso Corporation’s on-premises IT infrastructure and how their business needs were addressed with Microsoft 365 Enterprise.</span></span>

## <a name="see-also"></a><span data-ttu-id="18588-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18588-139">See also</span></span>

[<span data-ttu-id="18588-140">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="18588-140">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="18588-141">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="18588-141">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)



