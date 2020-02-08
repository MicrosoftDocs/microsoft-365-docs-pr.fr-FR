---
title: RGPD pour les serveurs Office
description: Découvrez comment satisfaire aux exigences du RGPD dans vos serveurs Office locaux.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 5ef03851064104df6dcb00ac853bf7dff65cbfd3
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41596431"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="a8737-103">RGPD pour les serveurs Office locaux</span><span class="sxs-lookup"><span data-stu-id="a8737-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="a8737-p101">Le Règlement général sur la protection des données (RGPD) présente les exigences que doivent respecter les organisations pour protéger les données personnelles et répondre aux demandes de personnes concernées de façon appropriée. Cette série d’articles présente les approches recommandées pour les charges de travail locales :</span><span class="sxs-lookup"><span data-stu-id="a8737-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

-   [<span data-ttu-id="a8737-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="a8737-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

-   [<span data-ttu-id="a8737-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="a8737-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

-   [<span data-ttu-id="a8737-108">Skype Entreprise Server</span><span class="sxs-lookup"><span data-stu-id="a8737-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

-   [<span data-ttu-id="a8737-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="a8737-109">Project Server</span></span>](gdpr-for-project-server.md)

-   [<span data-ttu-id="a8737-110">Office Web Apps Server et Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a8737-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

-   [<span data-ttu-id="a8737-111">Partages de fichiers en local</span><span class="sxs-lookup"><span data-stu-id="a8737-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="a8737-112">Pour plus d’informations sur le RGPD et sur l’aide que peut vous apporter Microsoft, reportez-vous au [centre de gestion de la confidentialité](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8737-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).</span></span>

<span data-ttu-id="a8737-p102">Avant d’entreprendre toute action concernant des données locales, consultez vos équipes juridiques et de conformité pour leur demander conseil et pour en savoir plus sur les schémas de classification existants et les approches en matière d’utilisation de données personnelles. Microsoft fournit des recommandations pour développer et améliorer les schémas de classification dans son Kit de détection de données du RGPD à l’adresse [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). Ce kit décrit également les approches possibles pour déplacer des données locales vers le cloud, dans lequel vous pouvez utiliser des fonctionnalités de gouvernance des données plus avancées si vous le souhaitez. Les articles de cette section fournissent des recommandations pour les données qui sont destinées à rester au niveau local.</span><span class="sxs-lookup"><span data-stu-id="a8737-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="a8737-p103">L’illustration suivante regroupe les fonctionnalités que nous vous recommandons d’utiliser pour chacune des charges de travail suivantes afin de repérer, classer, protéger et surveiller les données personnelles. Consultez les articles de cette section pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a8737-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![](media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="a8737-119">Description de l’illustration</span><span class="sxs-lookup"><span data-stu-id="a8737-119">Illustration description</span></span>

<span data-ttu-id="a8737-120">Concernant l’accessibilité, le tableau suivant fournit les mêmes exemples dans l’illustration.</span><span class="sxs-lookup"><span data-stu-id="a8737-120">For accessibility, the following table provides the same examples in the illustration.</span></span>

|             |<span data-ttu-id="a8737-121">Partages de fichiers Windows Server</span><span class="sxs-lookup"><span data-stu-id="a8737-121">Windows Server file shares</span></span>|<span data-ttu-id="a8737-122">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="a8737-122">SharePoint Server</span></span>|<span data-ttu-id="a8737-123">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="a8737-123">Exchange Server</span></span>|<span data-ttu-id="a8737-124">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="a8737-124">Skype for Business</span></span>|<span data-ttu-id="a8737-125">Project Server</span><span class="sxs-lookup"><span data-stu-id="a8737-125">Project Server</span></span>|
|:------------|:-------------------------|:----------------|:--------------|:-----------------|:-------------|
|<span data-ttu-id="a8737-126">Découvrir</span><span class="sxs-lookup"><span data-stu-id="a8737-126">Discover</span></span>|<span data-ttu-id="a8737-127">Scanneur Azure Information Protection\*</span><span class="sxs-lookup"><span data-stu-id="a8737-127">Azure Information Protection scanner\*</span></span>|<span data-ttu-id="a8737-128">Centre de recherche ou eDiscovery (une fois les données classées) ; scanneur Azure Information Protection\*</span><span class="sxs-lookup"><span data-stu-id="a8737-128">Search Center or eDiscovery (after data is classified); Azure Information Protection scanner\*</span></span>|<span data-ttu-id="a8737-129">Portail eDiscovery Exchange</span><span class="sxs-lookup"><span data-stu-id="a8737-129">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="a8737-130">Portail eDiscovery Exchange</span><span class="sxs-lookup"><span data-stu-id="a8737-130">Exchange eDiscovery portal</span></span>|<span data-ttu-id="a8737-131">Scripts SQL de découverte et d’exportation</span><span class="sxs-lookup"><span data-stu-id="a8737-131">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="a8737-132">Classer</span><span class="sxs-lookup"><span data-stu-id="a8737-132">Classify</span></span>|<span data-ttu-id="a8737-133">Scanneur Azure Information Protection\* ; types d’informations sensibles Office 365</span><span class="sxs-lookup"><span data-stu-id="a8737-133">Azure Information Protection scanner\*; Office 365 sensitive information types</span></span>|<span data-ttu-id="a8737-134">Scanneur Azure Information Protection\* ; types d’informations sensibles Office 365</span><span class="sxs-lookup"><span data-stu-id="a8737-134">Azure Information Protection scanner\*; Office 365 sensitive information types</span></span>|<span data-ttu-id="a8737-135">Balises et stratégies de rétention Exchange</span><span class="sxs-lookup"><span data-stu-id="a8737-135">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="a8737-136">Balises et stratégies de rétention Exchange</span><span class="sxs-lookup"><span data-stu-id="a8737-136">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="a8737-137">Protéger</span><span class="sxs-lookup"><span data-stu-id="a8737-137">Protect</span></span>||<span data-ttu-id="a8737-138">Règles de protection contre la perte de données Exchange Server ; autorisations, protection IRM pour bibliothèques</span><span class="sxs-lookup"><span data-stu-id="a8737-138">Exchange Server data loss prevention rules; Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="a8737-139">Règles de protection contre la perte de données Exchange Server ; intégration IRM avec Exchange Server</span><span class="sxs-lookup"><span data-stu-id="a8737-139">Exchange Server data loss prevention rules; IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="a8737-140">Surveiller</span><span class="sxs-lookup"><span data-stu-id="a8737-140">Monitor</span></span>|<span data-ttu-id="a8737-141">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="a8737-141">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="a8737-142">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="a8737-142">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="a8737-143">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="a8737-143">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="a8737-144">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="a8737-144">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="a8737-145">Intégrer des outils SIEM aux journaux</span><span class="sxs-lookup"><span data-stu-id="a8737-145">Integrate logs with SIEM tools</span></span>|

<span data-ttu-id="a8737-p104">\*Veuillez noter que toute protection chiffre le fichier, empêchant ainsi SharePoint Server de trouver les types d’informations sensibles dans les fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="a8737-p104">\*Note that protection encrypts the file. Consequently, SharePoint Server can’t find the sensitive information types in protected files.</span></span>
