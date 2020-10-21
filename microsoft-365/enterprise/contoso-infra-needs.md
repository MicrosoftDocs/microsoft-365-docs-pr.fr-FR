---
title: Infrastructure informatique contoso et besoins de l’entreprise
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez la structure de base de l’infrastructure informatique de contoso sur site et la façon dont les besoins de l’entreprise sont satisfaits par Microsoft 365 pour les entreprises.
ms.openlocfilehash: bc2b34254da01a3d49085082ab8ee8632df2d434
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48637174"
---
# <a name="contoso-it-infrastructure-and-business-needs"></a><span data-ttu-id="0a1b7-103">Infrastructure informatique contoso et besoins de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="0a1b7-103">Contoso IT infrastructure and business needs</span></span>

<span data-ttu-id="0a1b7-104">Contoso passe d’une infrastructure informatique centralisée locale à une configuration Cloud inclusive qui intègre des charges de travail et des applications de productivité personnelle basées sur le Cloud.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-104">Contoso is transitioning from an on-premises, centralized IT infrastructure to a cloud-inclusive setup that incorporates cloud-based personal productivity workloads and applications.</span></span>

## <a name="existing-contoso-it-infrastructure"></a><span data-ttu-id="0a1b7-105">Infrastructure informatique contoso existante</span><span class="sxs-lookup"><span data-stu-id="0a1b7-105">Existing Contoso IT infrastructure</span></span>

<span data-ttu-id="0a1b7-106">Contoso utilise une infrastructure informatique locale centralisée avec des centres de données situés au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-106">Contoso uses a mostly centralized on-premises IT infrastructure, with application datacenters in the Paris headquarters.</span></span>

<span data-ttu-id="0a1b7-107">La figure 1 présente le siège social avec des centres de donnees d’applications, un DMZ et Internet.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-107">Figure 1 shows the headquarters office with application datacenters, a DMZ, and the internet.</span></span>

![Infrastructure informatique contoso existante](../media/contoso-infra-needs/contoso-infra-needs-fig1.png)

<span data-ttu-id="0a1b7-109">**Figure 1 : infrastructure informatique de contoso existante**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-109">**Figure 1: Existing Contoso IT infrastructure**</span></span>
 
<span data-ttu-id="0a1b7-110">Les centres de données d’applications hébergent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a1b7-110">The on-premises application datacenters host:</span></span> 

- <span data-ttu-id="0a1b7-111">Applications métier personnalisées qui utilisent SQL Server et d’autres bases de données Linux.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-111">Custom line-of-business applications that use SQL Server and other Linux databases.</span></span>
- <span data-ttu-id="0a1b7-112">Ensemble d’anciens serveurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-112">A set of legacy SharePoint servers.</span></span>
- <span data-ttu-id="0a1b7-113">Serveurs au niveau des équipes et de l’organisation pour le stockage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-113">Organization and team-level servers for file storage.</span></span>

<span data-ttu-id="0a1b7-114">De plus, chaque bureau central régional prend en charge un ensemble de serveurs possédant un groupe d’applications similaire.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-114">Additionally, each regional hub office supports a set of servers with a similar set of applications.</span></span> <span data-ttu-id="0a1b7-115">Ces serveurs sont contrôlés par les services informatiques régionaux.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-115">These servers are under the control of regional IT departments.</span></span>

<span data-ttu-id="0a1b7-116">Il est toujours compliqué d’effectuer des recherches dans les applications et les données de ces centres de données répartis partout dans le monde.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-116">Searchability across the applications and data of these separate multi-geographical datacenters continues to be a challenge.</span></span>

<span data-ttu-id="0a1b7-117">Dans la zone DMZ du siège social contoso, différents ensembles de serveurs fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a1b7-117">In the Contoso headquarters DMZ, different sets of servers provide:</span></span>

- <span data-ttu-id="0a1b7-118">Hébergement pour le site Web public contoso, à partir duquel les clients peuvent commander des produits, des composants, des fournitures et des services.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-118">Hosting for the Contoso public web site, from which customers can order products, parts, supplies, and service.</span></span>
- <span data-ttu-id="0a1b7-119">Hébergement de l’extranet des partenaires de Contoso pour la collaboration et la communication avec les partenaires.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-119">Hosting for the Contoso partner extranet for partner communication and collaboration.</span></span>
- <span data-ttu-id="0a1b7-120">Accès à distance basé sur un réseau privé virtuel (VPN) à l’intranet et au proxy web de Contoso pour les collaborateurs présents au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-120">Virtual private network (VPN)-based remote access to the Contoso intranet and web proxying for workers in the Paris headquarters.</span></span>

## <a name="contoso-business-needs"></a><span data-ttu-id="0a1b7-121">Besoins commerciaux de contoso</span><span class="sxs-lookup"><span data-stu-id="0a1b7-121">Contoso business needs</span></span>

<span data-ttu-id="0a1b7-122">Les besoins d’entreprise de contoso appartiennent à cinq catégories principales :</span><span class="sxs-lookup"><span data-stu-id="0a1b7-122">Contoso business needs fall into five main categories:</span></span>

<span data-ttu-id="0a1b7-123">**Productivité**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-123">**Productivity**</span></span>

- <span data-ttu-id="0a1b7-124">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="0a1b7-124">Make collaboration easier</span></span>

  <span data-ttu-id="0a1b7-125">Remplacement de la messagerie et de la collaboration basée sur des partages de fichiers par un modèle en ligne qui permet des modifications en temps réel sur des documents, des réunions en ligne plus faciles et des threads de conversation capturés.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-125">Replace email and file share-based collaboration with an online model that allows real-time changes on documents, easier online meetings, and captured conversation threads.</span></span>
- <span data-ttu-id="0a1b7-126">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="0a1b7-126">Improve productivity for remote and mobile workers</span></span>

  <span data-ttu-id="0a1b7-127">Avec de nombreux employés travaillant à la maison ou sur le terrain, remplacez la solution VPN avec un accès performant aux données et ressources Contoso dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-127">With many employees working from home or in the field, replace the bottlenecked VPN solution with performant access to Contoso data and resources in the cloud.</span></span>
- <span data-ttu-id="0a1b7-128">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="0a1b7-128">Increase creativity and innovation</span></span>

  <span data-ttu-id="0a1b7-129">Profiter des dernières méthodes de développement d’idées et d’apprentissage visuel, notamment l’entrée manuscrite et la visualisation 3D.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-129">Take advantage of the latest visual learning and idea development methods, including inking and 3D visualization.</span></span>

<span data-ttu-id="0a1b7-130">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-130">**Security**</span></span>

- <span data-ttu-id="0a1b7-131">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="0a1b7-131">Identity and access management</span></span>

  <span data-ttu-id="0a1b7-132">Appliquer Multifactor et d’autres formes d’authentification et protéger les informations d’identification des utilisateurs et des comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-132">Enforce multifactor and other forms of authentication and protect user and administrator account credentials.</span></span>

- <span data-ttu-id="0a1b7-133">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0a1b7-133">Threat protection</span></span>

  <span data-ttu-id="0a1b7-134">Protéger contre les menaces externes de sécurité, notamment la messagerie et les programmes malveillants basés sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-134">Protect against external security threats, including email and operating system-based malware.</span></span>

- <span data-ttu-id="0a1b7-135">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="0a1b7-135">Information protection</span></span>

  <span data-ttu-id="0a1b7-136">Verrouiller l’accès aux biens numériques sensibles tels que les données client, les spécifications de conception et de fabrication et les informations des employés, et les chiffrer.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-136">Lock down access to and encrypt high-value digital assets, such as customer data, design and manufacturing specifications, and employee information.</span></span>

- <span data-ttu-id="0a1b7-137">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="0a1b7-137">Security management</span></span>

  <span data-ttu-id="0a1b7-138">Surveiller la position de la sécurité et détecter et répondre aux menaces en temps réel.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-138">Monitor security posture and detect and respond to threats in real time.</span></span>

<span data-ttu-id="0a1b7-139">**Accès mobile et à distance, et partenaires professionnels**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-139">**Remote and mobile access and business partners**</span></span>

- <span data-ttu-id="0a1b7-140">Améliorer la sécurité pour les utilisateurs distants et mobiles</span><span class="sxs-lookup"><span data-stu-id="0a1b7-140">Improve security for remote and mobile workers</span></span>

  <span data-ttu-id="0a1b7-141">Implémentez votre propre appareil (BYOD) et la gestion des périphériques appartenant à votre entreprise pour garantir un accès sécurisé, un comportement d’application correct et la protection des données de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-141">Implement bring your own device (BYOD) and company-owned device management to ensure secured access, correct application behavior, and company data protection.</span></span>

- <span data-ttu-id="0a1b7-142">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="0a1b7-142">Reduce remote access infrastructure for employees</span></span>

  <span data-ttu-id="0a1b7-143">Réduisez les coûts de maintenance et de support et améliorez les performances de la solution d’accès à distance en déplacant les ressources fréquemment utilisées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-143">Reduce maintenance and support costs and improve performance for remote access solution by moving commonly accessed resources to the cloud.</span></span>

- <span data-ttu-id="0a1b7-144">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions B2B (Business-to-susiness)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-144">Provide better connectivity and lower overhead for business-to-susiness (B2B) transactions</span></span>

  <span data-ttu-id="0a1b7-145">Remplacez un extranet de partenaire vieillissant et coûteux par une solution cloud qui utilise l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-145">Replace an aging and expensive partner extranet with a cloud-based solution that uses federated authentication.</span></span>

<span data-ttu-id="0a1b7-146">**Conformité**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-146">**Compliance**</span></span>

- <span data-ttu-id="0a1b7-147">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="0a1b7-147">Adhere to regional regulatory requirements</span></span>

  <span data-ttu-id="0a1b7-148">Assurer la conformité avec les réglementations sectorielles et régionales relatives au stockage des données, au chiffrement, à la confidentialité des données et aux réglementations relatives aux données personnelles, telles que le règlement général sur la protection des données (RGPD) pour l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-148">Ensure compliance with industry and regional regulations for data storage, encryption, data privacy, and personal data regulations, such as the General Data Protection Regulation (GDPR) for the Europe Union.</span></span>

<span data-ttu-id="0a1b7-149">**Gestion**</span><span class="sxs-lookup"><span data-stu-id="0a1b7-149">**Management**</span></span>

- <span data-ttu-id="0a1b7-150">Réduction de la charge informatique pour la gestion des logiciels s’exécutant sur les PC et les appareils clients</span><span class="sxs-lookup"><span data-stu-id="0a1b7-150">Lower IT overhead for managing software running on client PCs and devices</span></span>

  <span data-ttu-id="0a1b7-151">Automatisez l’installation des mises à jour sur le système d’exploitation Windows et les applications Microsoft 365 pour les entreprises au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-151">Automate installation of updates to the Windows operating system and Microsoft 365 Apps for enterprise across the organization.</span></span>

## <a name="mapping-contoso-business-needs-to-microsoft-365-for-enterprise"></a><span data-ttu-id="0a1b7-152">Mappage des besoins de l’entreprise Contoso à Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="0a1b7-152">Mapping Contoso business needs to Microsoft 365 for enterprise</span></span>

<span data-ttu-id="0a1b7-153">Le service informatique de Contoso a déterminé le mappage suivant des besoins de l’entreprise aux fonctionnalités Microsoft 365 E5 avant le déploiement :</span><span class="sxs-lookup"><span data-stu-id="0a1b7-153">The Contoso IT department determined the following mapping of business needs to Microsoft 365 E5 features prior to deployment:</span></span>


| <span data-ttu-id="0a1b7-154">Catégorie</span><span class="sxs-lookup"><span data-stu-id="0a1b7-154">Category</span></span> | <span data-ttu-id="0a1b7-155">Besoin métier</span><span class="sxs-lookup"><span data-stu-id="0a1b7-155">Business need</span></span> | <span data-ttu-id="0a1b7-156">Microsoft 365 pour les produits ou les fonctionnalités d’entreprise</span><span class="sxs-lookup"><span data-stu-id="0a1b7-156">Microsoft 365 for enterprise products or features</span></span> |
|:-------|:-----|:-----|
| <span data-ttu-id="0a1b7-157">Productivité</span><span class="sxs-lookup"><span data-stu-id="0a1b7-157">Productivity</span></span> |  |  |
|  | <span data-ttu-id="0a1b7-158">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="0a1b7-158">Make collaboration easier</span></span> | <span data-ttu-id="0a1b7-159">Microsoft Teams, SharePoint, OneDrive</span><span class="sxs-lookup"><span data-stu-id="0a1b7-159">Microsoft Teams, SharePoint, OneDrive</span></span> |
|  | <span data-ttu-id="0a1b7-160">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="0a1b7-160">Improve productivity for remote and mobile workers</span></span> | <span data-ttu-id="0a1b7-161">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="0a1b7-161">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="0a1b7-162">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="0a1b7-162">Increase creativity and innovation</span></span> | <span data-ttu-id="0a1b7-163">Windows Ink, Cortana at Work, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="0a1b7-163">Windows Ink, Cortana at Work, PowerPoint</span></span> |
| <span data-ttu-id="0a1b7-164">Sécurité</span><span class="sxs-lookup"><span data-stu-id="0a1b7-164">Security</span></span> |  |  |
|  | <span data-ttu-id="0a1b7-165">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="0a1b7-165">Identity & access management</span></span> | <span data-ttu-id="0a1b7-166">Comptes d’administrateur général dédiés avec Azure Multi-Factor Authentication (MFA) et Azure Active Directory Privileged Identity Management (PIM)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-166">Dedicated global administrator accounts with Azure Multi-Factor Authentication (MFA) and Azure Active Directory Privileged Identity Management (PIM)</span></span> <BR> <span data-ttu-id="0a1b7-167">Authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0a1b7-167">MFA for all user accounts</span></span> <BR> <span data-ttu-id="0a1b7-168">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="0a1b7-168">Conditional Access</span></span> <BR> <span data-ttu-id="0a1b7-169">Windows Hello</span><span class="sxs-lookup"><span data-stu-id="0a1b7-169">Windows Hello</span></span> <BR> <span data-ttu-id="0a1b7-170">Windows Credential Guard</span><span class="sxs-lookup"><span data-stu-id="0a1b7-170">Windows Credential Guard</span></span> |
|  | <span data-ttu-id="0a1b7-171">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0a1b7-171">Threat protection</span></span> | <span data-ttu-id="0a1b7-172">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="0a1b7-172">Advanced Threat Analytics</span></span> <BR> <span data-ttu-id="0a1b7-173">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="0a1b7-173">Windows Defender</span></span> <BR> <span data-ttu-id="0a1b7-174">Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0a1b7-174">Advanced Threat Protection</span></span> <BR> <span data-ttu-id="0a1b7-175">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0a1b7-175">Office 365 Advanced Threat Protection</span></span> <BR> <span data-ttu-id="0a1b7-176">Enquête et réponse de menace Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0a1b7-176">Microsoft 365 threat investigation and response</span></span> <BR> |
|  | <span data-ttu-id="0a1b7-177">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="0a1b7-177">Information protection</span></span> | <span data-ttu-id="0a1b7-178">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="0a1b7-178">Azure Information Protection</span></span> <BR> <span data-ttu-id="0a1b7-179">Protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-179">Data Loss Prevention (DLP)</span></span> <BR> <span data-ttu-id="0a1b7-180">Protection des informations Windows (WIP)</span><span class="sxs-lookup"><span data-stu-id="0a1b7-180">Windows Information Protection (WIP)</span></span> <BR> <span data-ttu-id="0a1b7-181">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="0a1b7-181">Microsoft Cloud App Security</span></span> <BR> <span data-ttu-id="0a1b7-182">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="0a1b7-182">Microsoft Intune</span></span> |
|  | <span data-ttu-id="0a1b7-183">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="0a1b7-183">Security management</span></span> | <span data-ttu-id="0a1b7-184">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="0a1b7-184">Azure Security Center</span></span>  <BR> <span data-ttu-id="0a1b7-185">Centre de sécurité Windows Defender</span><span class="sxs-lookup"><span data-stu-id="0a1b7-185">Windows Defender Security Center</span></span> |
| <span data-ttu-id="0a1b7-186">Accès mobile et à distance, et partenaires professionnels</span><span class="sxs-lookup"><span data-stu-id="0a1b7-186">Remote and mobile access and business partners</span></span> |  |  |
|  | <span data-ttu-id="0a1b7-187">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="0a1b7-187">Better security for remote and mobile workers</span></span> | <span data-ttu-id="0a1b7-188">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="0a1b7-188">Microsoft Intune</span></span> |
|  | <span data-ttu-id="0a1b7-189">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="0a1b7-189">Reduce remote access infrastructure for employees</span></span> | <span data-ttu-id="0a1b7-190">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="0a1b7-190">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="0a1b7-191">Améliorer la connectivité et réduire les frais généraux pour les transactions B2B</span><span class="sxs-lookup"><span data-stu-id="0a1b7-191">Improve connectivity and lower overhead for B2B transactions</span></span> | <span data-ttu-id="0a1b7-192">Authentification fédérée et ressources informatiques</span><span class="sxs-lookup"><span data-stu-id="0a1b7-192">Federated authentication and cloud-based resources</span></span> |
| <span data-ttu-id="0a1b7-193">Conformité</span><span class="sxs-lookup"><span data-stu-id="0a1b7-193">Compliance</span></span> |  |  |
|  | <span data-ttu-id="0a1b7-194">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="0a1b7-194">Adhere to regional regulatory requirements</span></span> | <span data-ttu-id="0a1b7-195">Fonctionnalités RGPD dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0a1b7-195">GDPR features in Microsoft 365</span></span> |
| <span data-ttu-id="0a1b7-196">Gestion</span><span class="sxs-lookup"><span data-stu-id="0a1b7-196">Management</span></span> |  |  |
|  | <span data-ttu-id="0a1b7-197">Réduire les frais généraux pour l’installation des mises à jour du client</span><span class="sxs-lookup"><span data-stu-id="0a1b7-197">Lower IT overhead for installing client updates</span></span> | <span data-ttu-id="0a1b7-198">Anneaux de déploiement</span><span class="sxs-lookup"><span data-stu-id="0a1b7-198">Deployment rings</span></span> <BR> <span data-ttu-id="0a1b7-199">Mises à jour pour Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="0a1b7-199">Windows 10 Enterprise updates</span></span> <BR> <span data-ttu-id="0a1b7-200">Mises à jour pour les Applications Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="0a1b7-200">Microsoft 365 Apps for enterprise updates</span></span> |
||||

## <a name="next-step"></a><span data-ttu-id="0a1b7-201">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0a1b7-201">Next step</span></span>

<span data-ttu-id="0a1b7-202">[Découvrez](contoso-networking.md) le réseau Contoso Corporation sur site et la façon dont il a été optimisé pour l’accès et la latence aux ressources basées sur le Cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0a1b7-202">[Learn](contoso-networking.md) about the Contoso Corporation on-premises network and how it was optimized for access and latency to Microsoft 365 cloud-based resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a1b7-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a1b7-203">See also</span></span>

[<span data-ttu-id="0a1b7-204">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="0a1b7-204">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="0a1b7-205">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="0a1b7-205">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
