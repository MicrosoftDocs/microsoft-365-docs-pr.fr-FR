---
title: Protection des informations
description: Découvrez les fonctionnalités de protection des informations dans Microsoft 365 pour le règlement général sur la protection des données (RGPD).
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
localization_priority: Priority
ms.prod: microsoft-365-enterprise
ms.topic: article
ms.date: 04/13/2018
f1.keywords:
- NOCSH
ms.author: bcarter
author: BrendaCarter
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 547d79093b65fba37a020781fbfce938d122c943
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846376"
---
# <a name="information-protection-for-gdpr-with-microsoft-365-capabilities"></a><span data-ttu-id="6e2e0-104">Protection des informations concernant le RGPD avec les fonctionnalités Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="6e2e0-104">Information protection for GDPR with Microsoft 365 capabilities</span></span>

<span data-ttu-id="6e2e0-p101">Microsoft 365 fournit un ensemble complet de fonctionnalités pour vous aider à vous conformer au Règlement général sur la protection des données (RGPD). Cet article récapitule les fonctionnalités recommandées et contient des liens vers des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-p101">Microsoft 365 provides a rich set of capabilities to help you achieve compliance with the General Data Protection Regulation (GDPR). This article summarizes recommended capabilities with links to more information.</span></span>

<span data-ttu-id="6e2e0-107">Pour plus d’informations sur la manière dont Microsoft peut vous aider avec le RGPD, reportez-vous à l’article [Prise en main : assistance concernant la responsabilité liée au RGPD](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted) dans le portail d’approbation de services.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-107">For more information about how Microsoft can help you with the GDPR, see [Get Started: Support for GDPR Accountability](https://servicetrust.microsoft.com/ViewPage/GDPRGetStarted) in the Service Trust Portal.</span></span>

## <a name="information-protection"></a><span data-ttu-id="6e2e0-108">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="6e2e0-108">Information protection</span></span>

<span data-ttu-id="6e2e0-p102">Office 365 offre un vaste ensemble de fonctionnalités de gouvernance. Pour obtenir de l’aide à propos de la recherche, de la classification, de la protection et de la surveillance des données personnelles, reportez-vous à l’article [Protection des informations Office 365 concernant le RGPD](https://docs.microsoft.com/microsoft-365/compliance/office-365-information-protection-for-gdpr).</span><span class="sxs-lookup"><span data-stu-id="6e2e0-p102">Office 365 provides a rich set of data governance capabilities. For help with finding, classifying, protecting, and monitoring personal data, see [Office 365 Information Protection for GDPR](https://docs.microsoft.com/microsoft-365/compliance/office-365-information-protection-for-gdpr).</span></span>

<span data-ttu-id="6e2e0-111">Pour obtenir de l’aide avec les serveurs locaux, notamment les partages de fichiers, SharePoint Server, Exchange Server, Skype Entreprise Server, Project Server et Office Online Server, consultez le [RGPD concernant les serveurs Office locaux](https://docs.microsoft.com/microsoft-365/compliance/gdpr-for-office-servers).</span><span class="sxs-lookup"><span data-stu-id="6e2e0-111">For help with on-premises servers, including file shares, SharePoint Server, Exchange Server, Skype for Business Server, Project Server, and Office Online Server, see [GDPR for on-premises Office servers](https://docs.microsoft.com/microsoft-365/compliance/gdpr-for-office-servers).</span></span> 

## <a name="identity-and-access-management"></a><span data-ttu-id="6e2e0-112">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="6e2e0-112">Identity and access management</span></span>

<span data-ttu-id="6e2e0-113">Azure Active Directory et d’autres fonctionnalités Microsoft 365 fournissent un ensemble complet de fonctionnalités permettant de protéger l’accès à vos données à partir d’identités et d’appareils :</span><span class="sxs-lookup"><span data-stu-id="6e2e0-113">Azure Active Directory and other Microsoft 365 capabilities provide a rich set of capabilities to protect access to your data from identities and devices:</span></span>

- <span data-ttu-id="6e2e0-114">Authentification multifacteur (MFA)</span><span class="sxs-lookup"><span data-stu-id="6e2e0-114">Multi-factor authentication (MFA)</span></span>
- <span data-ttu-id="6e2e0-115">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="6e2e0-115">Conditional access</span></span>
- <span data-ttu-id="6e2e0-116">Privileged identity management</span><span class="sxs-lookup"><span data-stu-id="6e2e0-116">Privileged identity management</span></span>
- <span data-ttu-id="6e2e0-117">Gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="6e2e0-117">Mobile device management</span></span>
- <span data-ttu-id="6e2e0-118">Gestion des applications mobiles</span><span class="sxs-lookup"><span data-stu-id="6e2e0-118">Mobile application management</span></span>
- <span data-ttu-id="6e2e0-119">Protection matérielle des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="6e2e0-119">Hardware protection for credentials</span></span>

<span data-ttu-id="6e2e0-120">Microsoft propose une configuration recommandée que vous pouvez utiliser comme point de départ :</span><span class="sxs-lookup"><span data-stu-id="6e2e0-120">Microsoft provides a recommended configuration you can use as a starting point:</span></span>

- <span data-ttu-id="6e2e0-p103">[Configurations des identités et de l’accès aux appareils :](../security/office-365-security/microsoft-365-policies-configurations.md): configurations de stratégie recommandées pour obtenir trois niveaux de protection (référence, sensible, hautement réglementée). Ces conseils incluent des stratégies recommandées pour Exchange Online et SharePoint Online (y compris OneDrive Entreprise).</span><span class="sxs-lookup"><span data-stu-id="6e2e0-p103">[Identity and device access configurations](../security/office-365-security/microsoft-365-policies-configurations.md): Recommended policy configurations to achieve three tiers of protection (baseline, sensitive, highly regulated). This guidance includes recommended policies for Exchange Online and SharePoint Online (including OneDrive for Business).</span></span>
- <span data-ttu-id="6e2e0-123">[Conseils de sécurité pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles](https://docs.microsoft.com/microsoft-365/security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o) : incluent le même ensemble de stratégies, mais fournissent des recommandations supplémentaires pour les environnements BYOD et les comptes B2B.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-123">[Security guidance for political campaigns, nonprofits, and other agile organizations](https://docs.microsoft.com/microsoft-365/security/office-365-security/microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o): This includes the same set of policies but provides more guidance for BYOD environments and for B2B accounts.</span></span>

## <a name="threat-protection"></a><span data-ttu-id="6e2e0-124">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="6e2e0-124">Threat Protection</span></span>

<span data-ttu-id="6e2e0-p104">La protection contre les menaces est intégrée aux services Microsoft 365. Voici quelques ressources pour vous aider à démarrer :</span><span class="sxs-lookup"><span data-stu-id="6e2e0-p104">Threat protection is built across Microsoft 365 services. Here are a few resources to get you started:</span></span>

- <span data-ttu-id="6e2e0-p105">[Feuille de route sur la sécurité Office 365 : principales priorités pour les 30 premiers jours, 90 premiers jours et au-delà](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap). Cette feuille de route comprend des recommandations pour l’implémentation des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-p105">[Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://docs.microsoft.com/microsoft-365/security/office-365-security/security-roadmap). This roadmap includes recommendations for implementing capabilities.</span></span> 
- <span data-ttu-id="6e2e0-129">[Protégez-vous contre les menaces dans Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats).</span><span class="sxs-lookup"><span data-stu-id="6e2e0-129">[Protect against threats in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/protect-against-threats).</span></span> <span data-ttu-id="6e2e0-130">Découvrez les mesures de protection que vous pouvez prendre dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-130">Learn about protection actions you can take in the Microsoft 365 security center.</span></span>
- <span data-ttu-id="6e2e0-131">[Microsoft Defender pour point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/).</span><span class="sxs-lookup"><span data-stu-id="6e2e0-131">[Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/).</span></span> <span data-ttu-id="6e2e0-132">En savoir plus sur Microsoft Defender pour point de terminaison et d’autres fonctionnalités dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6e2e0-132">Learn more about Microsoft Defender for Endpoint and other capabilities in Windows 10.</span></span>

## <a name="learn-more"></a><span data-ttu-id="6e2e0-133">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="6e2e0-133">Learn more</span></span>

[<span data-ttu-id="6e2e0-134">Centre de gestion de la confidentialité Microsoft</span><span class="sxs-lookup"><span data-stu-id="6e2e0-134">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
