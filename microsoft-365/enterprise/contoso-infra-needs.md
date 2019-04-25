---
title: Infrastructure informatique et besoins métier de Contoso
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 09/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre la structure de base de l’infrastructure informatique locale de Contoso et les besoins métier pouvant être satisfaits par Microsoft 365 Entreprise.
ms.openlocfilehash: bd259f367cdf3417e32671457f248029c853b6f8
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283675"
---
# <a name="contosos-it-infrastructure-and-business-needs"></a><span data-ttu-id="16ade-103">Infrastructure informatique et besoins métier de Contoso</span><span class="sxs-lookup"><span data-stu-id="16ade-103">Contoso's IT infrastructure and business needs</span></span>

<span data-ttu-id="16ade-104">**Résumé :** Comprendre la structure de base de l’infrastructure informatique locale de Contoso et les besoins métier pouvant être satisfaits par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="16ade-104">**Summary:** Understand the basic structure of Contoso's on-premises IT infrastructure and how its business needs can be met by Microsoft 365 Enterprise.</span></span>


<span data-ttu-id="16ade-105">Contoso est passé d’une infrastructure informatique centralisée locale à une infrastructure cloud incluant des charges de travail de productivité et des applications cloud.</span><span class="sxs-lookup"><span data-stu-id="16ade-105">Contoso has been transitioning from an on-premises, centralized IT infrastructure to a cloud-inclusive one that incorporates cloud-based personal productivity workloads and applications.</span></span>

## <a name="contosos-existing-it-infrastructure"></a><span data-ttu-id="16ade-106">Infrastructure informatique actuelle de Contoso</span><span class="sxs-lookup"><span data-stu-id="16ade-106">Contoso's existing IT infrastructure</span></span>

<span data-ttu-id="16ade-107">Contoso utilise une infrastructure informatique locale centralisée avec des centres de données situés au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="16ade-107">Contoso uses a mostly centralized on-premises IT infrastructure, with application datacenters in the Paris headquarters.</span></span>

<span data-ttu-id="16ade-108">La Figure 1 présente le siège social avec les centres de données d’applications, un DMZ et Internet.</span><span class="sxs-lookup"><span data-stu-id="16ade-108">Figure 1 shows a headquarters office with application datacenters, a DMZ, and the Internet.</span></span>

![](./media/contoso-infra-needs/contoso-infra-needs-fig1.png)

<span data-ttu-id="16ade-109">**Figure 1 : Infrastructure informatique existante de Contoso**</span><span class="sxs-lookup"><span data-stu-id="16ade-109">**Figure 1: Contoso's existing IT infrastructure**</span></span>
 
<span data-ttu-id="16ade-110">Les centres de données d’applications hébergent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="16ade-110">The on-premises application datacenters host:</span></span> 

- <span data-ttu-id="16ade-111">Ligne personnalisée d’applications métier qui utilise SQL Server et d’autres bases de données Linux.</span><span class="sxs-lookup"><span data-stu-id="16ade-111">Custom line of business applications that use SQL Server and other Linux databases.</span></span>
- <span data-ttu-id="16ade-112">Ensemble d’anciens serveurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="16ade-112">A set of legacy SharePoint servers.</span></span>
- <span data-ttu-id="16ade-113">Serveurs au niveau des équipes et de l’organisation pour le stockage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="16ade-113">Organization and team-level servers for file storage.</span></span>

<span data-ttu-id="16ade-p101">Cette infrastructure intègre également chaque bureau central régional qui prend en charge un ensemble de serveurs avec un ensemble d’applications similaire. Ces serveurs sont contrôlés par les services informatiques régionaux.</span><span class="sxs-lookup"><span data-stu-id="16ade-p101">Additionally, each regional hub office that supports a set of servers with a similar set of applications. These servers are under the control of regional IT departments.</span></span>

<span data-ttu-id="16ade-116">Il est toujours compliqué d’effectuer des recherches dans les applications et les données de ces centres de données répartis partout dans le monde.</span><span class="sxs-lookup"><span data-stu-id="16ade-116">Searchability across the applications and data of these separate multi-geographical datacenters continues to be a challenge.</span></span>

<span data-ttu-id="16ade-117">Dans le DMZ du siège social de Contoso, les différents groupes de serveurs fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="16ade-117">In Contoso's headquarters DMZ, different sets of servers provide:</span></span>

- <span data-ttu-id="16ade-118">Accès à distance VPN à l’intranet et au proxy web de Contoso pour les collaborateurs présents au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="16ade-118">VPN-based remote access to the Contoso intranet and web proxying for workers in the Paris headquarters.</span></span>
- <span data-ttu-id="16ade-119">Hébergement du site web public de Contoso à partir duquel les clients peuvent commander des produits, des composants, des fournitures ou des services.</span><span class="sxs-lookup"><span data-stu-id="16ade-119">Hosting for the Contoso public web site, from which customers can order products, parts, supplies, or service.</span></span>
- <span data-ttu-id="16ade-120">Hébergement de l’extranet des partenaires de Contoso pour la collaboration et la communication avec les partenaires.</span><span class="sxs-lookup"><span data-stu-id="16ade-120">Hosting for the Contoso partner extranet for partner communication and collaboration.</span></span>

## <a name="contosos-business-needs"></a><span data-ttu-id="16ade-121">Besoins métier de Contoso</span><span class="sxs-lookup"><span data-stu-id="16ade-121">Contoso's business needs</span></span>

<span data-ttu-id="16ade-122">Les besoins métier de Contoso sont regroupés dans cinq catégories principales :</span><span class="sxs-lookup"><span data-stu-id="16ade-122">Contoso's business needs fall into five main categories.</span></span>

<span data-ttu-id="16ade-123">Productivité :</span><span class="sxs-lookup"><span data-stu-id="16ade-123">Productivity:</span></span>

- <span data-ttu-id="16ade-124">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="16ade-124">Make collaboration easier</span></span>

  <span data-ttu-id="16ade-125">Remplacer la collaboration basée sur la messagerie et le partage de fichiers grâce à un modèle en ligne qui permet de modifier en temps réel les documents, de simplifier les réunions en ligne et de capturer des fils de conversation.</span><span class="sxs-lookup"><span data-stu-id="16ade-125">Replace the email and file share-based collaboration with an online model that allows real-time changes on documents, easier online meetings, and captured conversation threads.</span></span>
- <span data-ttu-id="16ade-126">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="16ade-126">Improve productivity for remote and mobile workers</span></span>

  <span data-ttu-id="16ade-127">En raison du grand nombre d’employés travaillant à la maison ou sur le terrain, remplacer la solution VPN engorgée avec un accès performant aux données et aux ressources de Contoso dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="16ade-127">With many employees working from homes or in the field, replace the bottlenecked VPN solution with performant access to Contoso data and resources in the cloud.</span></span>
- <span data-ttu-id="16ade-128">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="16ade-128">Increase creativity and innovation</span></span>

  <span data-ttu-id="16ade-129">Profiter des dernières méthodes de développement d’idées et d’apprentissage visuel, notamment l’entrée manuscrite et la visualisation 3D.</span><span class="sxs-lookup"><span data-stu-id="16ade-129">Take advantage of the latest visual learning and idea development methods, including inking and 3D visualization.</span></span>

<span data-ttu-id="16ade-130">Sécurité :</span><span class="sxs-lookup"><span data-stu-id="16ade-130">Security:</span></span>

- <span data-ttu-id="16ade-131">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="16ade-131">Identity and access management</span></span>

  <span data-ttu-id="16ade-132">Appliquer une authentification multifacteur et d’autres formes d’authentification, et protéger les informations d’identification de compte utilisateur et administrateur.</span><span class="sxs-lookup"><span data-stu-id="16ade-132">Enforce multi-factor and other forms of authentication and protect user and administrator account credentials.</span></span>

- <span data-ttu-id="16ade-133">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="16ade-133">Threat protection</span></span>

  <span data-ttu-id="16ade-134">Protéger contre les menaces externes de sécurité, notamment la messagerie et les programmes malveillants basés sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="16ade-134">Protect against external security threats, including email and operating system-based malware.</span></span>

- <span data-ttu-id="16ade-135">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="16ade-135">Information protection</span></span>

  <span data-ttu-id="16ade-136">Verrouiller l’accès aux biens numériques sensibles tels que les données client, les spécifications de conception et les informations des employés, et les chiffrer.</span><span class="sxs-lookup"><span data-stu-id="16ade-136">Lock down access to and encrypt high-value digital assets, such as customer data, design specifications, and employee information.</span></span>

- <span data-ttu-id="16ade-137">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="16ade-137">Security management</span></span>

  <span data-ttu-id="16ade-138">Surveiller la posture de sécurité et être en mesure de détecter et de traiter les menaces en temps réel.</span><span class="sxs-lookup"><span data-stu-id="16ade-138">Monitor security posture and be able to detect and respond to threats in real time.</span></span>

<span data-ttu-id="16ade-139">Accès mobile et à distance, et partenaires professionnels :</span><span class="sxs-lookup"><span data-stu-id="16ade-139">Remote and mobile access and business partners:</span></span>

- <span data-ttu-id="16ade-140">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="16ade-140">Better security for remote and mobile workers</span></span>

  <span data-ttu-id="16ade-141">Appliquer un mode de gestion adapté aux appareils BYOD (Bring Your Own Device) ainsi qu'à ceux appartenant à l’entreprise, pour assurer un accès sécurisé, un bon fonctionnement des applications et une protection des données de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="16ade-141">Institute Bring Your Own Device (BYOD) and company-owned device management to ensure secured access, correct application behavior, and company data protection.</span></span>

- <span data-ttu-id="16ade-142">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="16ade-142">Reduce remote access infrastructure for employees</span></span>

  <span data-ttu-id="16ade-143">Réduire les frais de maintenance et d’assistance, et améliorer les performances pour la solution d’accès à distance en déplaçant des ressources régulièrement consultées vers le cloud.</span><span class="sxs-lookup"><span data-stu-id="16ade-143">Reduce maintenance and support costs and improve performance for remote access solution by moving resources commonly accessed to the cloud.</span></span>

- <span data-ttu-id="16ade-144">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions Business-to-Business (B2B)</span><span class="sxs-lookup"><span data-stu-id="16ade-144">Provide better connectivity and lower overhead for Business-to-Business (B2B) transactions</span></span>

  <span data-ttu-id="16ade-145">Remplacer l’extranet obsolescent et coûteux par une solution cloud utilisant l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="16ade-145">Replace aging and expensive partner extranet with a cloud-based solution that uses federated authentication.</span></span>

<span data-ttu-id="16ade-146">Conformité :</span><span class="sxs-lookup"><span data-stu-id="16ade-146">Compliance:</span></span>

- <span data-ttu-id="16ade-147">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="16ade-147">Adhere to regional regulatory requirements</span></span>

  <span data-ttu-id="16ade-148">Être et rester conforme aux réglementations régionales et du secteur en matière de stockage des données, de chiffrement, de confidentialité des données et de réglementations des données personnelles, telles que le Règlement général sur la protection des données (RGPD) dans l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="16ade-148">Become and remain compliant with industry and regional regulations for data storage, encryption, data privacy, and personal data regulations, such as the General Data Protection Regulation (GDPR) for the Europe Union.</span></span>

<span data-ttu-id="16ade-149">Gestion :</span><span class="sxs-lookup"><span data-stu-id="16ade-149">Management:</span></span>

- <span data-ttu-id="16ade-150">Réduire les frais généraux informatiques pour la gestion des logiciels s’exécutant sur des périphériques et des PC client</span><span class="sxs-lookup"><span data-stu-id="16ade-150">Lower the IT overhead for managing software running on client PCs and devices</span></span>

  <span data-ttu-id="16ade-151">Automatiser l’installation des mises à jour pour le système d’exploitation Windows et Microsoft Office au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="16ade-151">Automate the installation of updates to the Windows operating system and Microsoft Office across the organization.</span></span>

## <a name="mapping-contosos-business-needs-to-microsoft-365-enterprise"></a><span data-ttu-id="16ade-152">Mappage des besoins métier de Contoso à Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="16ade-152">Mapping Contoso's business needs to Microsoft 365 Enterprise</span></span>

<span data-ttu-id="16ade-153">Le service informatique de Contoso a déterminé le mappage suivant des besoins métier aux fonctionnalités de Microsoft 365 Entreprise E5 avant le déploiement :</span><span class="sxs-lookup"><span data-stu-id="16ade-153">Contoso's IT department determined the following mapping of business needs to Microsoft 365 Enterprise E5 features prior to deployment:</span></span>

||||
|:-------|:-----|:-----|
| <span data-ttu-id="16ade-154">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="16ade-154">**Category**</span></span> | <span data-ttu-id="16ade-155">**Besoin métier**</span><span class="sxs-lookup"><span data-stu-id="16ade-155">**Business need**</span></span> | <span data-ttu-id="16ade-156">**Produits ou fonctionnalités Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="16ade-156">**Microsoft 365 Enterprise products or features**</span></span> |
| <span data-ttu-id="16ade-157">Productivité</span><span class="sxs-lookup"><span data-stu-id="16ade-157">Productivity</span></span> |  |  |
|  | <span data-ttu-id="16ade-158">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="16ade-158">Make collaboration easier</span></span> | <span data-ttu-id="16ade-159">Teams, SharePoint Online, Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="16ade-159">Teams, SharePoint Online, Skype for Business Online</span></span> |
|  | <span data-ttu-id="16ade-160">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="16ade-160">Improve productivity for remote and mobile workers</span></span> | <span data-ttu-id="16ade-161">Charges de travail Office 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="16ade-161">Office 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="16ade-162">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="16ade-162">Increase creativity and innovation</span></span> | <span data-ttu-id="16ade-163">Windows Ink, Cortana at Work, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="16ade-163">Windows Ink, Cortana at Work, PowerPoint</span></span> |
| <span data-ttu-id="16ade-164">Sécurité</span><span class="sxs-lookup"><span data-stu-id="16ade-164">Security</span></span> |  |  |
|  | <span data-ttu-id="16ade-165">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="16ade-165">Identity & access management</span></span> | <span data-ttu-id="16ade-166">Comptes Administrateur général dédiés avec l’authentification multifacteur (MFA) et Azure AD Privileged Identity Management (PIM)</span><span class="sxs-lookup"><span data-stu-id="16ade-166">Dedicated global administrator accounts with Multi-factor authentication (MFA) and Azure AD Privileged Identity Management (PIM)</span></span> <BR> <span data-ttu-id="16ade-167">Authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="16ade-167">MFA for all user accounts</span></span> <BR> <span data-ttu-id="16ade-168">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="16ade-168">Conditional access</span></span> <BR> <span data-ttu-id="16ade-169">Windows Hello</span><span class="sxs-lookup"><span data-stu-id="16ade-169">Windows Hello</span></span> <BR> <span data-ttu-id="16ade-170">Windows Credential Guard</span><span class="sxs-lookup"><span data-stu-id="16ade-170">Windows Credential Guard</span></span> |
|  | <span data-ttu-id="16ade-171">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="16ade-171">Threat protection</span></span> | <span data-ttu-id="16ade-172">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="16ade-172">Advanced Threat Analytics</span></span> <BR> <span data-ttu-id="16ade-173">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="16ade-173">Windows Defender</span></span> <BR> <span data-ttu-id="16ade-174">Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="16ade-174">Advanced Threat Protection</span></span> <BR> <span data-ttu-id="16ade-175">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="16ade-175">Office 365 Advanced Threat Protection</span></span> <BR> <span data-ttu-id="16ade-176">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="16ade-176">Office 365 threat investigation and response</span></span> <BR> |
|  | <span data-ttu-id="16ade-177">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="16ade-177">Information protection</span></span> | <span data-ttu-id="16ade-178">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="16ade-178">Azure Information Protection</span></span> <BR> <span data-ttu-id="16ade-179">Protection contre la perte de données Office 365 (DLP)</span><span class="sxs-lookup"><span data-stu-id="16ade-179">Office 365 Data Loss Prevention (DLP)</span></span> <BR> <span data-ttu-id="16ade-180">Protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="16ade-180">Windows Information Protection</span></span> <BR> <span data-ttu-id="16ade-181">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="16ade-181">Microsoft Cloud App Security</span></span> <BR> <span data-ttu-id="16ade-182">Sécurité des applications cloud Office 365 (CAS)</span><span class="sxs-lookup"><span data-stu-id="16ade-182">Office 365 Cloud App Security (CAS)</span></span> <BR> <span data-ttu-id="16ade-183">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="16ade-183">Microsoft Intune</span></span> |
|  | <span data-ttu-id="16ade-184">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="16ade-184">Security management</span></span> | <span data-ttu-id="16ade-185">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="16ade-185">Azure Security Center</span></span>  <BR> <span data-ttu-id="16ade-186">Centre de sécurité Windows Defender</span><span class="sxs-lookup"><span data-stu-id="16ade-186">Windows Defender Security Center</span></span> |
| <span data-ttu-id="16ade-187">Accès mobile et à distance, et partenaires professionnels</span><span class="sxs-lookup"><span data-stu-id="16ade-187">Remote and mobile access and business partners</span></span> |  |  |
|  | <span data-ttu-id="16ade-188">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="16ade-188">Better security for remote and mobile workers</span></span> | <span data-ttu-id="16ade-189">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="16ade-189">Microsoft Intune</span></span> |
|  | <span data-ttu-id="16ade-190">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="16ade-190">Reduce remote access infrastructure for employees</span></span> | <span data-ttu-id="16ade-191">Charges de travail Office 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="16ade-191">Office 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="16ade-192">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions B2B</span><span class="sxs-lookup"><span data-stu-id="16ade-192">Provide better connectivity and lower overhead for B2B transactions</span></span> | <span data-ttu-id="16ade-193">Authentification fédérée et ressources informatiques</span><span class="sxs-lookup"><span data-stu-id="16ade-193">Federated authentication and cloud-based resources</span></span> |
| <span data-ttu-id="16ade-194">Conformité</span><span class="sxs-lookup"><span data-stu-id="16ade-194">Compliance</span></span> |  |  |
|  | <span data-ttu-id="16ade-195">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="16ade-195">Adhere to regional regulatory requirements</span></span> | <span data-ttu-id="16ade-196">Fonctionnalités RGPD dans Office 365</span><span class="sxs-lookup"><span data-stu-id="16ade-196">GDPR features in Office 365</span></span> |
| <span data-ttu-id="16ade-197">Gestion</span><span class="sxs-lookup"><span data-stu-id="16ade-197">Management</span></span> |  |  |
|  | <span data-ttu-id="16ade-198">Réduire les frais généraux informatiques pour l’installation de mises à jour du client</span><span class="sxs-lookup"><span data-stu-id="16ade-198">Lower the IT overhead for installing client updates</span></span> | <span data-ttu-id="16ade-199">Anneaux de déploiement</span><span class="sxs-lookup"><span data-stu-id="16ade-199">Deployment rings</span></span> <BR> <span data-ttu-id="16ade-200">Mise à niveau de Windows 10 en place et Autopilot</span><span class="sxs-lookup"><span data-stu-id="16ade-200">Windows 10 upgrade in place and Autopilot</span></span> <BR> <span data-ttu-id="16ade-201">Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="16ade-201">Office 365 ProPlus</span></span> |
||||

## <a name="next-step"></a><span data-ttu-id="16ade-202">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="16ade-202">Next step</span></span>

<span data-ttu-id="16ade-203">[En savoir plus](contoso-networking.md) sur le réseau local de Contoso Corporation et sur la façon dont il a été optimisé pour l’accès et la latence vers des ressources informatiques Microsoft 365 au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="16ade-203">[Learn](contoso-networking.md) about the Contoso Corporation’s on-premises network and how it was optimized for access and latency to Microsoft 365 cloud-based resources across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="16ade-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16ade-204">See also</span></span>

[<span data-ttu-id="16ade-205">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="16ade-205">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="16ade-206">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="16ade-206">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
