---
title: Infrastructure informatique de Contoso et besoins de l’entreprise
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre la structure de base de l’infrastructure informatique locale de Contoso et la façon dont les besoins de l’entreprise sont satisfaits par Microsoft 365 entreprise.
ms.openlocfilehash: 72d502b5078a1e572eeba27832550af52907e209
ms.sourcegitcommit: c1dd5be42fe0c5dcc7c05817c941edd9076febf8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49558405"
---
# <a name="contoso-it-infrastructure-and-business-needs"></a><span data-ttu-id="28080-103">Infrastructure informatique de Contoso et besoins de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="28080-103">Contoso IT infrastructure and business needs</span></span>

<span data-ttu-id="28080-104">Contoso passe d’une infrastructure informatique centralisée locale à une configuration cloud qui intègre des applications et des charges de travail de productivité personnelles basées sur le cloud.</span><span class="sxs-lookup"><span data-stu-id="28080-104">Contoso is transitioning from an on-premises, centralized IT infrastructure to a cloud-inclusive setup that incorporates cloud-based personal productivity workloads and applications.</span></span>

## <a name="existing-contoso-it-infrastructure"></a><span data-ttu-id="28080-105">Infrastructure informatique Contoso existante</span><span class="sxs-lookup"><span data-stu-id="28080-105">Existing Contoso IT infrastructure</span></span>

<span data-ttu-id="28080-106">Contoso utilise une infrastructure informatique locale centralisée avec des centres de données situés au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="28080-106">Contoso uses a mostly centralized on-premises IT infrastructure, with application datacenters in the Paris headquarters.</span></span>

<span data-ttu-id="28080-107">Voici le siège social avec des centres de données d’application, un DMZ et Internet.</span><span class="sxs-lookup"><span data-stu-id="28080-107">Here is the headquarters office with application datacenters, a DMZ, and the internet.</span></span>

![Infrastructure informatique Contoso existante](../media/contoso-infra-needs/contoso-infra-needs-fig1.png)

<span data-ttu-id="28080-109">Les centres de données d’applications hébergent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="28080-109">The on-premises application datacenters host:</span></span> 

- <span data-ttu-id="28080-110">Applications métier personnalisées qui utilisent SQL Server et d’autres bases de données Linux.</span><span class="sxs-lookup"><span data-stu-id="28080-110">Custom line-of-business applications that use SQL Server and other Linux databases.</span></span>
- <span data-ttu-id="28080-111">Ensemble d’anciens serveurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="28080-111">A set of legacy SharePoint servers.</span></span>
- <span data-ttu-id="28080-112">Serveurs au niveau des équipes et de l’organisation pour le stockage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="28080-112">Organization and team-level servers for file storage.</span></span>

<span data-ttu-id="28080-113">De plus, chaque bureau central régional prend en charge un ensemble de serveurs possédant un groupe d’applications similaire.</span><span class="sxs-lookup"><span data-stu-id="28080-113">Additionally, each regional hub office supports a set of servers with a similar set of applications.</span></span> <span data-ttu-id="28080-114">Ces serveurs sont contrôlés par les services informatiques régionaux.</span><span class="sxs-lookup"><span data-stu-id="28080-114">These servers are under the control of regional IT departments.</span></span>

<span data-ttu-id="28080-115">Il est toujours compliqué d’effectuer des recherches dans les applications et les données de ces centres de données répartis partout dans le monde.</span><span class="sxs-lookup"><span data-stu-id="28080-115">Searchability across the applications and data of these separate multi-geographical datacenters continues to be a challenge.</span></span>

<span data-ttu-id="28080-116">Dans la DMZ du siège social de Contoso, différents ensembles de serveurs fournissent :</span><span class="sxs-lookup"><span data-stu-id="28080-116">In the Contoso headquarters DMZ, different sets of servers provide:</span></span>

- <span data-ttu-id="28080-117">Hébergement pour le site web public Contoso, à partir duquel les clients peuvent commander des produits, des composants, des fournitures et des services.</span><span class="sxs-lookup"><span data-stu-id="28080-117">Hosting for the Contoso public web site, from which customers can order products, parts, supplies, and service.</span></span>
- <span data-ttu-id="28080-118">Hébergement de l’extranet des partenaires de Contoso pour la collaboration et la communication avec les partenaires.</span><span class="sxs-lookup"><span data-stu-id="28080-118">Hosting for the Contoso partner extranet for partner communication and collaboration.</span></span>
- <span data-ttu-id="28080-119">Accès à distance basé sur un réseau privé virtuel (VPN) à l’intranet et au proxy web de Contoso pour les collaborateurs présents au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="28080-119">Virtual private network (VPN)-based remote access to the Contoso intranet and web proxying for workers in the Paris headquarters.</span></span>

## <a name="contoso-business-needs"></a><span data-ttu-id="28080-120">Besoins commerciaux de Contoso</span><span class="sxs-lookup"><span data-stu-id="28080-120">Contoso business needs</span></span>

<span data-ttu-id="28080-121">Les besoins commerciaux de Contoso sont en cinq catégories principales :</span><span class="sxs-lookup"><span data-stu-id="28080-121">Contoso business needs fall into five main categories:</span></span>

<span data-ttu-id="28080-122">**Productivité**</span><span class="sxs-lookup"><span data-stu-id="28080-122">**Productivity**</span></span>

- <span data-ttu-id="28080-123">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="28080-123">Make collaboration easier</span></span>

  <span data-ttu-id="28080-124">Remplacez la collaboration basée sur le courrier électronique et le partage de fichiers par un modèle en ligne qui permet des modifications en temps réel sur les documents, des réunions en ligne plus faciles et des threads de conversation capturés.</span><span class="sxs-lookup"><span data-stu-id="28080-124">Replace email and file share-based collaboration with an online model that allows real-time changes on documents, easier online meetings, and captured conversation threads.</span></span>
- <span data-ttu-id="28080-125">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="28080-125">Improve productivity for remote and mobile workers</span></span>

  <span data-ttu-id="28080-126">Avec de nombreux employés travaillant à domicile ou sur le terrain, remplacez la solution VPN en goulot d’étranglement par un accès performant aux données et ressources Contoso dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="28080-126">With many employees working from home or in the field, replace the bottlenecked VPN solution with performant access to Contoso data and resources in the cloud.</span></span>
- <span data-ttu-id="28080-127">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="28080-127">Increase creativity and innovation</span></span>

  <span data-ttu-id="28080-128">Profiter des dernières méthodes de développement d’idées et d’apprentissage visuel, notamment l’entrée manuscrite et la visualisation 3D.</span><span class="sxs-lookup"><span data-stu-id="28080-128">Take advantage of the latest visual learning and idea development methods, including inking and 3D visualization.</span></span>

<span data-ttu-id="28080-129">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="28080-129">**Security**</span></span>

- <span data-ttu-id="28080-130">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="28080-130">Identity and access management</span></span>

  <span data-ttu-id="28080-131">Appliquer plusieurs formes d’authentification et autres formes d’authentification et protéger les informations d’identification des comptes d’utilisateur et d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="28080-131">Enforce multifactor and other forms of authentication and protect user and administrator account credentials.</span></span>

- <span data-ttu-id="28080-132">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="28080-132">Threat protection</span></span>

  <span data-ttu-id="28080-133">Protéger contre les menaces externes de sécurité, notamment la messagerie et les programmes malveillants basés sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="28080-133">Protect against external security threats, including email and operating system-based malware.</span></span>

- <span data-ttu-id="28080-134">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="28080-134">Information protection</span></span>

  <span data-ttu-id="28080-135">Verrouiller l’accès aux biens numériques sensibles tels que les données client, les spécifications de conception et de fabrication et les informations des employés, et les chiffrer.</span><span class="sxs-lookup"><span data-stu-id="28080-135">Lock down access to and encrypt high-value digital assets, such as customer data, design and manufacturing specifications, and employee information.</span></span>

- <span data-ttu-id="28080-136">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="28080-136">Security management</span></span>

  <span data-ttu-id="28080-137">Surveillez la posture de sécurité et détectez et répondez aux menaces en temps réel.</span><span class="sxs-lookup"><span data-stu-id="28080-137">Monitor security posture and detect and respond to threats in real time.</span></span>

<span data-ttu-id="28080-138">**Accès mobile et à distance, et partenaires professionnels**</span><span class="sxs-lookup"><span data-stu-id="28080-138">**Remote and mobile access and business partners**</span></span>

- <span data-ttu-id="28080-139">Améliorer la sécurité pour les travailleurs à distance et mobiles</span><span class="sxs-lookup"><span data-stu-id="28080-139">Improve security for remote and mobile workers</span></span>

  <span data-ttu-id="28080-140">Implémentez la gestion de votre propre appareil (BYOD) et de votre entreprise pour garantir un accès sécurisé, un comportement correct des applications et la protection des données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="28080-140">Implement bring your own device (BYOD) and company-owned device management to ensure secured access, correct application behavior, and company data protection.</span></span>

- <span data-ttu-id="28080-141">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="28080-141">Reduce remote access infrastructure for employees</span></span>

  <span data-ttu-id="28080-142">Réduisez les coûts de maintenance et de support et améliorez les performances pour la solution d’accès à distance en déplaçant les ressources couramment accessibles vers le cloud.</span><span class="sxs-lookup"><span data-stu-id="28080-142">Reduce maintenance and support costs and improve performance for remote access solution by moving commonly accessed resources to the cloud.</span></span>

- <span data-ttu-id="28080-143">Fournir une meilleure connectivité et réduire la surcharge pour les transactions de l’entreprise à la vente (B2B)</span><span class="sxs-lookup"><span data-stu-id="28080-143">Provide better connectivity and lower overhead for business-to-susiness (B2B) transactions</span></span>

  <span data-ttu-id="28080-144">Remplacez un extranet partenaire coûteux et coûteux par une solution basée sur le cloud qui utilise l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="28080-144">Replace an aging and expensive partner extranet with a cloud-based solution that uses federated authentication.</span></span>

<span data-ttu-id="28080-145">**Conformité**</span><span class="sxs-lookup"><span data-stu-id="28080-145">**Compliance**</span></span>

- <span data-ttu-id="28080-146">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="28080-146">Adhere to regional regulatory requirements</span></span>

  <span data-ttu-id="28080-147">Assurer la conformité avec les réglementations industrielles et régionales en matière de stockage des données, de chiffrement, de confidentialité des données et de réglementations relatives aux données personnelles, telles que le Règlement général sur la protection des données (R GDPR) pour l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="28080-147">Ensure compliance with industry and regional regulations for data storage, encryption, data privacy, and personal data regulations, such as the General Data Protection Regulation (GDPR) for the Europe Union.</span></span>

<span data-ttu-id="28080-148">**Gestion**</span><span class="sxs-lookup"><span data-stu-id="28080-148">**Management**</span></span>

- <span data-ttu-id="28080-149">Réduire la surcharge informatique pour la gestion des logiciels en cours d’exécution sur les PC et appareils clients</span><span class="sxs-lookup"><span data-stu-id="28080-149">Lower IT overhead for managing software running on client PCs and devices</span></span>

  <span data-ttu-id="28080-150">Automatisez l’installation des mises à jour Windows système d’exploitation et Applications Microsoft 365 pour les grandes entreprises au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="28080-150">Automate installation of updates to the Windows operating system and Microsoft 365 Apps for enterprise across the organization.</span></span>

## <a name="mapping-contoso-business-needs-to-microsoft-365-for-enterprise"></a><span data-ttu-id="28080-151">Mappage des besoins métier de Contoso Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="28080-151">Mapping Contoso business needs to Microsoft 365 for enterprise</span></span>

<span data-ttu-id="28080-152">Le service informatique de Contoso a déterminé le mappage suivant des besoins de l’entreprise Microsoft 365 E5 fonctionnalités avant le déploiement :</span><span class="sxs-lookup"><span data-stu-id="28080-152">The Contoso IT department determined the following mapping of business needs to Microsoft 365 E5 features prior to deployment:</span></span>


| <span data-ttu-id="28080-153">Catégorie</span><span class="sxs-lookup"><span data-stu-id="28080-153">Category</span></span> | <span data-ttu-id="28080-154">Besoin métier</span><span class="sxs-lookup"><span data-stu-id="28080-154">Business need</span></span> | <span data-ttu-id="28080-155">Microsoft 365 pour les produits ou fonctionnalités d’entreprise</span><span class="sxs-lookup"><span data-stu-id="28080-155">Microsoft 365 for enterprise products or features</span></span> |
|:-------|:-----|:-----|
| <span data-ttu-id="28080-156">Productivité</span><span class="sxs-lookup"><span data-stu-id="28080-156">Productivity</span></span> |  |  |
|  | <span data-ttu-id="28080-157">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="28080-157">Make collaboration easier</span></span> | <span data-ttu-id="28080-158">Microsoft Teams, SharePoint, OneDrive</span><span class="sxs-lookup"><span data-stu-id="28080-158">Microsoft Teams, SharePoint, OneDrive</span></span> |
|  | <span data-ttu-id="28080-159">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="28080-159">Improve productivity for remote and mobile workers</span></span> | <span data-ttu-id="28080-160">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="28080-160">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="28080-161">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="28080-161">Increase creativity and innovation</span></span> | <span data-ttu-id="28080-162">Windows Ink, Cortana at Work, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="28080-162">Windows Ink, Cortana at Work, PowerPoint</span></span> |
| <span data-ttu-id="28080-163">Sécurité</span><span class="sxs-lookup"><span data-stu-id="28080-163">Security</span></span> |  |  |
|  | <span data-ttu-id="28080-164">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="28080-164">Identity & access management</span></span> | <span data-ttu-id="28080-165">Comptes d’administrateur général dédiés avec Azure AD Multi-Factor Authentication (MFA) et Azure AD Privileged Identity Management (PIM)</span><span class="sxs-lookup"><span data-stu-id="28080-165">Dedicated global administrator accounts with Azure AD Multi-Factor Authentication (MFA) and Azure AD Privileged Identity Management (PIM)</span></span> <BR> <span data-ttu-id="28080-166">Authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="28080-166">MFA for all user accounts</span></span> <BR> <span data-ttu-id="28080-167">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="28080-167">Conditional Access</span></span> <BR> <span data-ttu-id="28080-168">Windows Hello</span><span class="sxs-lookup"><span data-stu-id="28080-168">Windows Hello</span></span> <BR> <span data-ttu-id="28080-169">Windows Credential Guard</span><span class="sxs-lookup"><span data-stu-id="28080-169">Windows Credential Guard</span></span> |
|  | <span data-ttu-id="28080-170">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="28080-170">Threat protection</span></span> | <span data-ttu-id="28080-171">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="28080-171">Advanced Threat Analytics</span></span> <BR> <span data-ttu-id="28080-172">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="28080-172">Windows Defender</span></span> <BR> <span data-ttu-id="28080-173">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="28080-173">Defender for Office 365</span></span> <BR> <span data-ttu-id="28080-174">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="28080-174">Microsoft Defender for Office 365</span></span> <BR> <span data-ttu-id="28080-175">Microsoft 365 et réponse aux menaces</span><span class="sxs-lookup"><span data-stu-id="28080-175">Microsoft 365 threat investigation and response</span></span> <BR> |
|  | <span data-ttu-id="28080-176">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="28080-176">Information protection</span></span> | <span data-ttu-id="28080-177">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="28080-177">Azure Information Protection</span></span> <BR> <span data-ttu-id="28080-178">Protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="28080-178">Data Loss Prevention (DLP)</span></span> <BR> <span data-ttu-id="28080-179">Protection des informations Windows (WIP)</span><span class="sxs-lookup"><span data-stu-id="28080-179">Windows Information Protection (WIP)</span></span> <BR> <span data-ttu-id="28080-180">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="28080-180">Microsoft Cloud App Security</span></span> <BR> <span data-ttu-id="28080-181">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="28080-181">Microsoft Intune</span></span> |
|  | <span data-ttu-id="28080-182">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="28080-182">Security management</span></span> | <span data-ttu-id="28080-183">Azure Defender</span><span class="sxs-lookup"><span data-stu-id="28080-183">Azure Defender</span></span>  <BR> <span data-ttu-id="28080-184">Centre de sécurité Windows Defender</span><span class="sxs-lookup"><span data-stu-id="28080-184">Windows Defender Security Center</span></span> |
| <span data-ttu-id="28080-185">Accès mobile et à distance, et partenaires professionnels</span><span class="sxs-lookup"><span data-stu-id="28080-185">Remote and mobile access and business partners</span></span> |  |  |
|  | <span data-ttu-id="28080-186">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="28080-186">Better security for remote and mobile workers</span></span> | <span data-ttu-id="28080-187">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="28080-187">Microsoft Intune</span></span> |
|  | <span data-ttu-id="28080-188">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="28080-188">Reduce remote access infrastructure for employees</span></span> | <span data-ttu-id="28080-189">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="28080-189">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="28080-190">Améliorer la connectivité et réduire la surcharge pour les transactions B2B</span><span class="sxs-lookup"><span data-stu-id="28080-190">Improve connectivity and lower overhead for B2B transactions</span></span> | <span data-ttu-id="28080-191">Authentification fédérée et ressources informatiques</span><span class="sxs-lookup"><span data-stu-id="28080-191">Federated authentication and cloud-based resources</span></span> |
| <span data-ttu-id="28080-192">Conformité</span><span class="sxs-lookup"><span data-stu-id="28080-192">Compliance</span></span> |  |  |
|  | <span data-ttu-id="28080-193">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="28080-193">Adhere to regional regulatory requirements</span></span> | <span data-ttu-id="28080-194">Fonctionnalités R GDPR dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="28080-194">GDPR features in Microsoft 365</span></span> |
| <span data-ttu-id="28080-195">Gestion</span><span class="sxs-lookup"><span data-stu-id="28080-195">Management</span></span> |  |  |
|  | <span data-ttu-id="28080-196">Réduire la surcharge pour l’installation des mises à jour client</span><span class="sxs-lookup"><span data-stu-id="28080-196">Lower IT overhead for installing client updates</span></span> | <span data-ttu-id="28080-197">Mises à jour pour Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="28080-197">Windows 10 Enterprise updates</span></span> <BR> <span data-ttu-id="28080-198">Mises à jour pour les Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="28080-198">Microsoft 365 Apps for enterprise updates</span></span> |
||||

## <a name="next-step"></a><span data-ttu-id="28080-199">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="28080-199">Next step</span></span>

<span data-ttu-id="28080-200">Découvrez le réseau local de Contoso [Corporation](contoso-networking.md) et la façon dont il a été optimisé pour l’accès et la latence Microsoft 365 ressources informatiques.</span><span class="sxs-lookup"><span data-stu-id="28080-200">Learn about the Contoso Corporation [on-premises network](contoso-networking.md) and how it was optimized for access and latency to Microsoft 365 cloud-based resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="28080-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28080-201">See also</span></span>

[<span data-ttu-id="28080-202">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="28080-202">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="28080-203">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="28080-203">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
