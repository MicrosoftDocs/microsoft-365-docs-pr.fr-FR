---
title: Infrastructure informatique contoso et besoins de l’entreprise
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
description: Découvrez la structure de base de l’infrastructure informatique de contoso sur site et la façon dont les besoins de l’entreprise sont satisfaits par Microsoft 365 pour les entreprises.
ms.openlocfilehash: 0a837a457869fc579d94ee5e5f9bb114cb93f641
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847129"
---
# <a name="contoso-it-infrastructure-and-business-needs"></a><span data-ttu-id="7f6ac-103">Infrastructure informatique contoso et besoins de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="7f6ac-103">Contoso IT infrastructure and business needs</span></span>

<span data-ttu-id="7f6ac-104">Contoso passe d’une infrastructure informatique centralisée locale à une configuration Cloud inclusive qui intègre des charges de travail et des applications de productivité personnelle basées sur le Cloud.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-104">Contoso is transitioning from an on-premises, centralized IT infrastructure to a cloud-inclusive setup that incorporates cloud-based personal productivity workloads and applications.</span></span>

## <a name="existing-contoso-it-infrastructure"></a><span data-ttu-id="7f6ac-105">Infrastructure informatique contoso existante</span><span class="sxs-lookup"><span data-stu-id="7f6ac-105">Existing Contoso IT infrastructure</span></span>

<span data-ttu-id="7f6ac-106">Contoso utilise une infrastructure informatique locale centralisée avec des centres de données situés au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-106">Contoso uses a mostly centralized on-premises IT infrastructure, with application datacenters in the Paris headquarters.</span></span>

<span data-ttu-id="7f6ac-107">Voici le siège social avec les centres de services d’applications, un DMZ et Internet.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-107">Here is the headquarters office with application datacenters, a DMZ, and the internet.</span></span>

![Infrastructure informatique contoso existante](../media/contoso-infra-needs/contoso-infra-needs-fig1.png)

<span data-ttu-id="7f6ac-109">Les centres de données d’applications hébergent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f6ac-109">The on-premises application datacenters host:</span></span> 

- <span data-ttu-id="7f6ac-110">Applications métier personnalisées qui utilisent SQL Server et d’autres bases de données Linux.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-110">Custom line-of-business applications that use SQL Server and other Linux databases.</span></span>
- <span data-ttu-id="7f6ac-111">Ensemble d’anciens serveurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-111">A set of legacy SharePoint servers.</span></span>
- <span data-ttu-id="7f6ac-112">Serveurs au niveau des équipes et de l’organisation pour le stockage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-112">Organization and team-level servers for file storage.</span></span>

<span data-ttu-id="7f6ac-113">De plus, chaque bureau central régional prend en charge un ensemble de serveurs possédant un groupe d’applications similaire.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-113">Additionally, each regional hub office supports a set of servers with a similar set of applications.</span></span> <span data-ttu-id="7f6ac-114">Ces serveurs sont contrôlés par les services informatiques régionaux.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-114">These servers are under the control of regional IT departments.</span></span>

<span data-ttu-id="7f6ac-115">Il est toujours compliqué d’effectuer des recherches dans les applications et les données de ces centres de données répartis partout dans le monde.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-115">Searchability across the applications and data of these separate multi-geographical datacenters continues to be a challenge.</span></span>

<span data-ttu-id="7f6ac-116">Dans la zone DMZ du siège social contoso, différents ensembles de serveurs fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f6ac-116">In the Contoso headquarters DMZ, different sets of servers provide:</span></span>

- <span data-ttu-id="7f6ac-117">Hébergement pour le site Web public contoso, à partir duquel les clients peuvent commander des produits, des composants, des fournitures et des services.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-117">Hosting for the Contoso public web site, from which customers can order products, parts, supplies, and service.</span></span>
- <span data-ttu-id="7f6ac-118">Hébergement de l’extranet des partenaires de Contoso pour la collaboration et la communication avec les partenaires.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-118">Hosting for the Contoso partner extranet for partner communication and collaboration.</span></span>
- <span data-ttu-id="7f6ac-119">Accès à distance basé sur un réseau privé virtuel (VPN) à l’intranet et au proxy web de Contoso pour les collaborateurs présents au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-119">Virtual private network (VPN)-based remote access to the Contoso intranet and web proxying for workers in the Paris headquarters.</span></span>

## <a name="contoso-business-needs"></a><span data-ttu-id="7f6ac-120">Besoins commerciaux de contoso</span><span class="sxs-lookup"><span data-stu-id="7f6ac-120">Contoso business needs</span></span>

<span data-ttu-id="7f6ac-121">Les besoins d’entreprise de contoso appartiennent à cinq catégories principales :</span><span class="sxs-lookup"><span data-stu-id="7f6ac-121">Contoso business needs fall into five main categories:</span></span>

<span data-ttu-id="7f6ac-122">**Productivité**</span><span class="sxs-lookup"><span data-stu-id="7f6ac-122">**Productivity**</span></span>

- <span data-ttu-id="7f6ac-123">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="7f6ac-123">Make collaboration easier</span></span>

  <span data-ttu-id="7f6ac-124">Remplacement de la messagerie et de la collaboration basée sur des partages de fichiers par un modèle en ligne qui permet des modifications en temps réel sur des documents, des réunions en ligne plus faciles et des threads de conversation capturés.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-124">Replace email and file share-based collaboration with an online model that allows real-time changes on documents, easier online meetings, and captured conversation threads.</span></span>
- <span data-ttu-id="7f6ac-125">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="7f6ac-125">Improve productivity for remote and mobile workers</span></span>

  <span data-ttu-id="7f6ac-126">Avec de nombreux employés travaillant à la maison ou sur le terrain, remplacez la solution VPN avec un accès performant aux données et ressources Contoso dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-126">With many employees working from home or in the field, replace the bottlenecked VPN solution with performant access to Contoso data and resources in the cloud.</span></span>
- <span data-ttu-id="7f6ac-127">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="7f6ac-127">Increase creativity and innovation</span></span>

  <span data-ttu-id="7f6ac-128">Profiter des dernières méthodes de développement d’idées et d’apprentissage visuel, notamment l’entrée manuscrite et la visualisation 3D.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-128">Take advantage of the latest visual learning and idea development methods, including inking and 3D visualization.</span></span>

<span data-ttu-id="7f6ac-129">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="7f6ac-129">**Security**</span></span>

- <span data-ttu-id="7f6ac-130">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="7f6ac-130">Identity and access management</span></span>

  <span data-ttu-id="7f6ac-131">Appliquer Multifactor et d’autres formes d’authentification et protéger les informations d’identification des utilisateurs et des comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-131">Enforce multifactor and other forms of authentication and protect user and administrator account credentials.</span></span>

- <span data-ttu-id="7f6ac-132">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="7f6ac-132">Threat protection</span></span>

  <span data-ttu-id="7f6ac-133">Protéger contre les menaces externes de sécurité, notamment la messagerie et les programmes malveillants basés sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-133">Protect against external security threats, including email and operating system-based malware.</span></span>

- <span data-ttu-id="7f6ac-134">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="7f6ac-134">Information protection</span></span>

  <span data-ttu-id="7f6ac-135">Verrouiller l’accès aux biens numériques sensibles tels que les données client, les spécifications de conception et de fabrication et les informations des employés, et les chiffrer.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-135">Lock down access to and encrypt high-value digital assets, such as customer data, design and manufacturing specifications, and employee information.</span></span>

- <span data-ttu-id="7f6ac-136">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="7f6ac-136">Security management</span></span>

  <span data-ttu-id="7f6ac-137">Surveiller la position de la sécurité et détecter et répondre aux menaces en temps réel.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-137">Monitor security posture and detect and respond to threats in real time.</span></span>

<span data-ttu-id="7f6ac-138">**Accès mobile et à distance, et partenaires professionnels**</span><span class="sxs-lookup"><span data-stu-id="7f6ac-138">**Remote and mobile access and business partners**</span></span>

- <span data-ttu-id="7f6ac-139">Améliorer la sécurité pour les utilisateurs distants et mobiles</span><span class="sxs-lookup"><span data-stu-id="7f6ac-139">Improve security for remote and mobile workers</span></span>

  <span data-ttu-id="7f6ac-140">Implémentez votre propre appareil (BYOD) et la gestion des périphériques appartenant à votre entreprise pour garantir un accès sécurisé, un comportement d’application correct et la protection des données de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-140">Implement bring your own device (BYOD) and company-owned device management to ensure secured access, correct application behavior, and company data protection.</span></span>

- <span data-ttu-id="7f6ac-141">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="7f6ac-141">Reduce remote access infrastructure for employees</span></span>

  <span data-ttu-id="7f6ac-142">Réduisez les coûts de maintenance et de support et améliorez les performances de la solution d’accès à distance en déplacant les ressources fréquemment utilisées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-142">Reduce maintenance and support costs and improve performance for remote access solution by moving commonly accessed resources to the cloud.</span></span>

- <span data-ttu-id="7f6ac-143">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions B2B (Business-to-susiness)</span><span class="sxs-lookup"><span data-stu-id="7f6ac-143">Provide better connectivity and lower overhead for business-to-susiness (B2B) transactions</span></span>

  <span data-ttu-id="7f6ac-144">Remplacez un extranet de partenaire vieillissant et coûteux par une solution cloud qui utilise l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-144">Replace an aging and expensive partner extranet with a cloud-based solution that uses federated authentication.</span></span>

<span data-ttu-id="7f6ac-145">**Conformité**</span><span class="sxs-lookup"><span data-stu-id="7f6ac-145">**Compliance**</span></span>

- <span data-ttu-id="7f6ac-146">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="7f6ac-146">Adhere to regional regulatory requirements</span></span>

  <span data-ttu-id="7f6ac-147">Assurer la conformité avec les réglementations sectorielles et régionales relatives au stockage des données, au chiffrement, à la confidentialité des données et aux réglementations relatives aux données personnelles, telles que le règlement général sur la protection des données (RGPD) pour l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-147">Ensure compliance with industry and regional regulations for data storage, encryption, data privacy, and personal data regulations, such as the General Data Protection Regulation (GDPR) for the Europe Union.</span></span>

<span data-ttu-id="7f6ac-148">**Gestion**</span><span class="sxs-lookup"><span data-stu-id="7f6ac-148">**Management**</span></span>

- <span data-ttu-id="7f6ac-149">Réduction de la charge informatique pour la gestion des logiciels s’exécutant sur les PC et les appareils clients</span><span class="sxs-lookup"><span data-stu-id="7f6ac-149">Lower IT overhead for managing software running on client PCs and devices</span></span>

  <span data-ttu-id="7f6ac-150">Automatisez l’installation des mises à jour sur le système d’exploitation Windows et les applications Microsoft 365 pour les entreprises au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-150">Automate installation of updates to the Windows operating system and Microsoft 365 Apps for enterprise across the organization.</span></span>

## <a name="mapping-contoso-business-needs-to-microsoft-365-for-enterprise"></a><span data-ttu-id="7f6ac-151">Mappage des besoins de l’entreprise Contoso à Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="7f6ac-151">Mapping Contoso business needs to Microsoft 365 for enterprise</span></span>

<span data-ttu-id="7f6ac-152">Le service informatique de Contoso a déterminé le mappage suivant des besoins de l’entreprise aux fonctionnalités Microsoft 365 E5 avant le déploiement :</span><span class="sxs-lookup"><span data-stu-id="7f6ac-152">The Contoso IT department determined the following mapping of business needs to Microsoft 365 E5 features prior to deployment:</span></span>


| <span data-ttu-id="7f6ac-153">Catégorie</span><span class="sxs-lookup"><span data-stu-id="7f6ac-153">Category</span></span> | <span data-ttu-id="7f6ac-154">Besoin métier</span><span class="sxs-lookup"><span data-stu-id="7f6ac-154">Business need</span></span> | <span data-ttu-id="7f6ac-155">Microsoft 365 pour les produits ou les fonctionnalités d’entreprise</span><span class="sxs-lookup"><span data-stu-id="7f6ac-155">Microsoft 365 for enterprise products or features</span></span> |
|:-------|:-----|:-----|
| <span data-ttu-id="7f6ac-156">Productivité</span><span class="sxs-lookup"><span data-stu-id="7f6ac-156">Productivity</span></span> |  |  |
|  | <span data-ttu-id="7f6ac-157">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="7f6ac-157">Make collaboration easier</span></span> | <span data-ttu-id="7f6ac-158">Microsoft Teams, SharePoint, OneDrive</span><span class="sxs-lookup"><span data-stu-id="7f6ac-158">Microsoft Teams, SharePoint, OneDrive</span></span> |
|  | <span data-ttu-id="7f6ac-159">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="7f6ac-159">Improve productivity for remote and mobile workers</span></span> | <span data-ttu-id="7f6ac-160">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="7f6ac-160">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="7f6ac-161">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="7f6ac-161">Increase creativity and innovation</span></span> | <span data-ttu-id="7f6ac-162">Windows Ink, Cortana at Work, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="7f6ac-162">Windows Ink, Cortana at Work, PowerPoint</span></span> |
| <span data-ttu-id="7f6ac-163">Sécurité</span><span class="sxs-lookup"><span data-stu-id="7f6ac-163">Security</span></span> |  |  |
|  | <span data-ttu-id="7f6ac-164">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="7f6ac-164">Identity & access management</span></span> | <span data-ttu-id="7f6ac-165">Comptes Administrateur général dédiés avec l’authentification multifacteur (MFA) Azure et Azure AD Privileged Identity Management (PIM)</span><span class="sxs-lookup"><span data-stu-id="7f6ac-165">Dedicated global administrator accounts with Azure Multi-Factor Authentication (MFA) and Azure AD Privileged Identity Management (PIM)</span></span> <BR> <span data-ttu-id="7f6ac-166">Authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7f6ac-166">MFA for all user accounts</span></span> <BR> <span data-ttu-id="7f6ac-167">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="7f6ac-167">Conditional Access</span></span> <BR> <span data-ttu-id="7f6ac-168">Windows Hello</span><span class="sxs-lookup"><span data-stu-id="7f6ac-168">Windows Hello</span></span> <BR> <span data-ttu-id="7f6ac-169">Windows Credential Guard</span><span class="sxs-lookup"><span data-stu-id="7f6ac-169">Windows Credential Guard</span></span> |
|  | <span data-ttu-id="7f6ac-170">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="7f6ac-170">Threat protection</span></span> | <span data-ttu-id="7f6ac-171">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="7f6ac-171">Advanced Threat Analytics</span></span> <BR> <span data-ttu-id="7f6ac-172">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="7f6ac-172">Windows Defender</span></span> <BR> <span data-ttu-id="7f6ac-173">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7f6ac-173">Defender for Office 365</span></span> <BR> <span data-ttu-id="7f6ac-174">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="7f6ac-174">Microsoft Defender for Office 365</span></span> <BR> <span data-ttu-id="7f6ac-175">Enquête et réponse de menace Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7f6ac-175">Microsoft 365 threat investigation and response</span></span> <BR> |
|  | <span data-ttu-id="7f6ac-176">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="7f6ac-176">Information protection</span></span> | <span data-ttu-id="7f6ac-177">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="7f6ac-177">Azure Information Protection</span></span> <BR> <span data-ttu-id="7f6ac-178">Protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="7f6ac-178">Data Loss Prevention (DLP)</span></span> <BR> <span data-ttu-id="7f6ac-179">Protection des informations Windows (WIP)</span><span class="sxs-lookup"><span data-stu-id="7f6ac-179">Windows Information Protection (WIP)</span></span> <BR> <span data-ttu-id="7f6ac-180">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="7f6ac-180">Microsoft Cloud App Security</span></span> <BR> <span data-ttu-id="7f6ac-181">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="7f6ac-181">Microsoft Intune</span></span> |
|  | <span data-ttu-id="7f6ac-182">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="7f6ac-182">Security management</span></span> | <span data-ttu-id="7f6ac-183">Azure Defender \*</span><span class="sxs-lookup"><span data-stu-id="7f6ac-183">Azure Defender\*</span></span>  <BR> <span data-ttu-id="7f6ac-184">Centre de sécurité Windows Defender</span><span class="sxs-lookup"><span data-stu-id="7f6ac-184">Windows Defender Security Center</span></span> |
| <span data-ttu-id="7f6ac-185">Accès mobile et à distance, et partenaires professionnels</span><span class="sxs-lookup"><span data-stu-id="7f6ac-185">Remote and mobile access and business partners</span></span> |  |  |
|  | <span data-ttu-id="7f6ac-186">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="7f6ac-186">Better security for remote and mobile workers</span></span> | <span data-ttu-id="7f6ac-187">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="7f6ac-187">Microsoft Intune</span></span> |
|  | <span data-ttu-id="7f6ac-188">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="7f6ac-188">Reduce remote access infrastructure for employees</span></span> | <span data-ttu-id="7f6ac-189">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="7f6ac-189">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="7f6ac-190">Améliorer la connectivité et réduire les frais généraux pour les transactions B2B</span><span class="sxs-lookup"><span data-stu-id="7f6ac-190">Improve connectivity and lower overhead for B2B transactions</span></span> | <span data-ttu-id="7f6ac-191">Authentification fédérée et ressources informatiques</span><span class="sxs-lookup"><span data-stu-id="7f6ac-191">Federated authentication and cloud-based resources</span></span> |
| <span data-ttu-id="7f6ac-192">Conformité</span><span class="sxs-lookup"><span data-stu-id="7f6ac-192">Compliance</span></span> |  |  |
|  | <span data-ttu-id="7f6ac-193">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="7f6ac-193">Adhere to regional regulatory requirements</span></span> | <span data-ttu-id="7f6ac-194">Fonctionnalités RGPD dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7f6ac-194">GDPR features in Microsoft 365</span></span> |
| <span data-ttu-id="7f6ac-195">Gestion</span><span class="sxs-lookup"><span data-stu-id="7f6ac-195">Management</span></span> |  |  |
|  | <span data-ttu-id="7f6ac-196">Réduire les frais généraux pour l’installation des mises à jour du client</span><span class="sxs-lookup"><span data-stu-id="7f6ac-196">Lower IT overhead for installing client updates</span></span> | <span data-ttu-id="7f6ac-197">Mises à jour pour Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7f6ac-197">Windows 10 Enterprise updates</span></span> <BR> <span data-ttu-id="7f6ac-198">Mises à jour pour les Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="7f6ac-198">Microsoft 365 Apps for enterprise updates</span></span> |
||||

## <a name="next-step"></a><span data-ttu-id="7f6ac-199">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7f6ac-199">Next step</span></span>

<span data-ttu-id="7f6ac-200">Découvrez le réseau Contoso Corporation [sur site](contoso-networking.md) et la façon dont il a été optimisé pour l’accès et la latence aux ressources basées sur le Cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f6ac-200">Learn about the Contoso Corporation [on-premises network](contoso-networking.md) and how it was optimized for access and latency to Microsoft 365 cloud-based resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f6ac-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f6ac-201">See also</span></span>

[<span data-ttu-id="7f6ac-202">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="7f6ac-202">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="7f6ac-203">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="7f6ac-203">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
