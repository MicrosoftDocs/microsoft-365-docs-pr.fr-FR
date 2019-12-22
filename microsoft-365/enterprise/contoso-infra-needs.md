---
title: Infrastructure informatique et besoins métier de Contoso
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
description: Comprendre la structure de base de l’infrastructure informatique locale de Contoso et la manière dont les besoins métier ont été satisfaits par Microsoft 365 Entreprise.
ms.openlocfilehash: d98f401ae4a39e3e04b5840e8f76c1e3e1b1a24d
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40802069"
---
# <a name="contosos-it-infrastructure-and-business-needs"></a><span data-ttu-id="12cbc-103">Infrastructure informatique et besoins métier de Contoso</span><span class="sxs-lookup"><span data-stu-id="12cbc-103">Contoso's IT infrastructure and business needs</span></span>

<span data-ttu-id="12cbc-104">Contoso est passé d’une infrastructure informatique centralisée locale à une infrastructure cloud incluant des charges de travail de productivité et des applications cloud.</span><span class="sxs-lookup"><span data-stu-id="12cbc-104">Contoso has been transitioning from an on-premises, centralized IT infrastructure to a cloud-inclusive one that incorporates cloud-based personal productivity workloads and applications.</span></span>

## <a name="contosos-existing-it-infrastructure"></a><span data-ttu-id="12cbc-105">Infrastructure informatique actuelle de Contoso</span><span class="sxs-lookup"><span data-stu-id="12cbc-105">Contoso's existing IT infrastructure</span></span>

<span data-ttu-id="12cbc-106">Contoso utilise une infrastructure informatique locale centralisée avec des centres de données situés au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="12cbc-106">Contoso uses a mostly centralized on-premises IT infrastructure, with application datacenters in the Paris headquarters.</span></span>

<span data-ttu-id="12cbc-107">La Figure 1 présente le siège social avec les centres de données d’applications, un DMZ et Internet.</span><span class="sxs-lookup"><span data-stu-id="12cbc-107">Figure 1 shows a headquarters office with application datacenters, a DMZ, and the Internet.</span></span>

![Infrastructure informatique actuelle de Contoso](./media/contoso-infra-needs/contoso-infra-needs-fig1.png)

<span data-ttu-id="12cbc-109">**Figure 1 : Infrastructure informatique existante de Contoso**</span><span class="sxs-lookup"><span data-stu-id="12cbc-109">**Figure 1: Contoso's existing IT infrastructure**</span></span>
 
<span data-ttu-id="12cbc-110">Les centres de données d’applications hébergent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="12cbc-110">The on-premises application datacenters host:</span></span> 

- <span data-ttu-id="12cbc-111">Ligne personnalisée d’applications métier qui utilise SQL Server et d’autres bases de données Linux.</span><span class="sxs-lookup"><span data-stu-id="12cbc-111">Custom line of business applications that use SQL Server and other Linux databases.</span></span>
- <span data-ttu-id="12cbc-112">Ensemble d’anciens serveurs SharePoint.</span><span class="sxs-lookup"><span data-stu-id="12cbc-112">A set of legacy SharePoint servers.</span></span>
- <span data-ttu-id="12cbc-113">Serveurs au niveau des équipes et de l’organisation pour le stockage des fichiers.</span><span class="sxs-lookup"><span data-stu-id="12cbc-113">Organization and team-level servers for file storage.</span></span>

<span data-ttu-id="12cbc-114">De plus, chaque bureau central régional prend en charge un ensemble de serveurs possédant un groupe d’applications similaire.</span><span class="sxs-lookup"><span data-stu-id="12cbc-114">Additionally, each regional hub office supports a set of servers with a similar set of applications.</span></span> <span data-ttu-id="12cbc-115">Ces serveurs sont contrôlés par les services informatiques régionaux.</span><span class="sxs-lookup"><span data-stu-id="12cbc-115">These servers are under the control of regional IT departments.</span></span>

<span data-ttu-id="12cbc-116">Il est toujours compliqué d’effectuer des recherches dans les applications et les données de ces centres de données répartis partout dans le monde.</span><span class="sxs-lookup"><span data-stu-id="12cbc-116">Searchability across the applications and data of these separate multi-geographical datacenters continues to be a challenge.</span></span>

<span data-ttu-id="12cbc-117">Dans le DMZ du siège social de Contoso, les différents groupes de serveurs fournissent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="12cbc-117">In Contoso's headquarters DMZ, different sets of servers provide:</span></span>

- <span data-ttu-id="12cbc-118">Hébergement du site web public de Contoso à partir duquel les clients peuvent commander des produits, des composants, des fournitures ou des services.</span><span class="sxs-lookup"><span data-stu-id="12cbc-118">Hosting for the Contoso public web site, from which customers can order products, parts, supplies, or service.</span></span>
- <span data-ttu-id="12cbc-119">Hébergement de l’extranet des partenaires de Contoso pour la collaboration et la communication avec les partenaires.</span><span class="sxs-lookup"><span data-stu-id="12cbc-119">Hosting for the Contoso partner extranet for partner communication and collaboration.</span></span>
- <span data-ttu-id="12cbc-120">Accès à distance basé sur un réseau privé virtuel (VPN) à l’intranet et au proxy web de Contoso pour les collaborateurs présents au siège social parisien.</span><span class="sxs-lookup"><span data-stu-id="12cbc-120">Virtual private network (VPN)-based remote access to the Contoso intranet and web proxying for workers in the Paris headquarters.</span></span>

## <a name="contosos-business-needs"></a><span data-ttu-id="12cbc-121">Besoins métier de Contoso</span><span class="sxs-lookup"><span data-stu-id="12cbc-121">Contoso's business needs</span></span>

<span data-ttu-id="12cbc-122">Les besoins métier de Contoso sont regroupés dans cinq catégories principales :</span><span class="sxs-lookup"><span data-stu-id="12cbc-122">Contoso's business needs fall into five main categories.</span></span>

<span data-ttu-id="12cbc-123">Productivité :</span><span class="sxs-lookup"><span data-stu-id="12cbc-123">Productivity:</span></span>

- <span data-ttu-id="12cbc-124">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="12cbc-124">Make collaboration easier</span></span>

  <span data-ttu-id="12cbc-125">Remplacer la collaboration basée sur la messagerie et le partage de fichiers grâce à un modèle en ligne qui permet de modifier en temps réel les documents, de simplifier les réunions en ligne et de capturer des fils de conversation.</span><span class="sxs-lookup"><span data-stu-id="12cbc-125">Replace the email and file share-based collaboration with an online model that allows real-time changes on documents, easier online meetings, and captured conversation threads.</span></span>
- <span data-ttu-id="12cbc-126">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="12cbc-126">Improve productivity for remote and mobile workers</span></span>

  <span data-ttu-id="12cbc-127">En raison du grand nombre d’employés travaillant à la maison ou sur le terrain, remplacer la solution VPN engorgée avec un accès performant aux données et aux ressources de Contoso dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="12cbc-127">With many employees working from homes or in the field, replace the bottlenecked VPN solution with performant access to Contoso data and resources in the cloud.</span></span>
- <span data-ttu-id="12cbc-128">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="12cbc-128">Increase creativity and innovation</span></span>

  <span data-ttu-id="12cbc-129">Profiter des dernières méthodes de développement d’idées et d’apprentissage visuel, notamment l’entrée manuscrite et la visualisation 3D.</span><span class="sxs-lookup"><span data-stu-id="12cbc-129">Take advantage of the latest visual learning and idea development methods, including inking and 3D visualization.</span></span>

<span data-ttu-id="12cbc-130">Sécurité :</span><span class="sxs-lookup"><span data-stu-id="12cbc-130">Security:</span></span>

- <span data-ttu-id="12cbc-131">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="12cbc-131">Identity and access management</span></span>

  <span data-ttu-id="12cbc-132">Appliquer une authentification multifacteur et d’autres formes d’authentification, et protéger les informations d’identification de compte utilisateur et administrateur.</span><span class="sxs-lookup"><span data-stu-id="12cbc-132">Enforce multi-factor and other forms of authentication and protect user and administrator account credentials.</span></span>

- <span data-ttu-id="12cbc-133">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12cbc-133">Threat protection</span></span>

  <span data-ttu-id="12cbc-134">Protéger contre les menaces externes de sécurité, notamment la messagerie et les programmes malveillants basés sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="12cbc-134">Protect against external security threats, including email and operating system-based malware.</span></span>

- <span data-ttu-id="12cbc-135">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="12cbc-135">Information protection</span></span>

  <span data-ttu-id="12cbc-136">Verrouiller l’accès aux biens numériques sensibles tels que les données client, les spécifications de conception et de fabrication et les informations des employés, et les chiffrer.</span><span class="sxs-lookup"><span data-stu-id="12cbc-136">Lock down access to and encrypt high-value digital assets, such as customer data, design and manufacturing specifications, and employee information.</span></span>

- <span data-ttu-id="12cbc-137">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="12cbc-137">Security management</span></span>

  <span data-ttu-id="12cbc-138">Surveiller la posture de sécurité et être en mesure de détecter et de traiter les menaces en temps réel.</span><span class="sxs-lookup"><span data-stu-id="12cbc-138">Monitor security posture and be able to detect and respond to threats in real time.</span></span>

<span data-ttu-id="12cbc-139">Accès mobile et à distance, et partenaires professionnels :</span><span class="sxs-lookup"><span data-stu-id="12cbc-139">Remote and mobile access and business partners:</span></span>

- <span data-ttu-id="12cbc-140">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="12cbc-140">Better security for remote and mobile workers</span></span>

  <span data-ttu-id="12cbc-141">Appliquer un mode de gestion adapté aux appareils BYOD (Bring Your Own Device) ainsi qu'à ceux appartenant à l’entreprise, pour assurer un accès sécurisé, un bon fonctionnement des applications et une protection des données de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="12cbc-141">Institute Bring Your Own Device (BYOD) and company-owned device management to ensure secured access, correct application behavior, and company data protection.</span></span>

- <span data-ttu-id="12cbc-142">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="12cbc-142">Reduce remote access infrastructure for employees</span></span>

  <span data-ttu-id="12cbc-143">Réduire les frais de maintenance et d’assistance, et améliorer les performances pour la solution d’accès à distance en déplaçant des ressources régulièrement consultées vers le cloud.</span><span class="sxs-lookup"><span data-stu-id="12cbc-143">Reduce maintenance and support costs and improve performance for remote access solution by moving commonly-accessed resources to the cloud.</span></span>

- <span data-ttu-id="12cbc-144">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions Business-to-Business (B2B)</span><span class="sxs-lookup"><span data-stu-id="12cbc-144">Provide better connectivity and lower overhead for Business-to-Business (B2B) transactions</span></span>

  <span data-ttu-id="12cbc-145">Remplacer l’extranet obsolescent et coûteux par une solution cloud utilisant l’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="12cbc-145">Replace aging and expensive partner extranet with a cloud-based solution that uses federated authentication.</span></span>

<span data-ttu-id="12cbc-146">Conformité :</span><span class="sxs-lookup"><span data-stu-id="12cbc-146">Compliance:</span></span>

- <span data-ttu-id="12cbc-147">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="12cbc-147">Adhere to regional regulatory requirements</span></span>

  <span data-ttu-id="12cbc-148">Être et rester conforme aux réglementations régionales et du secteur en matière de stockage des données, de chiffrement, de confidentialité des données et de réglementations des données personnelles, telles que le Règlement général sur la protection des données (RGPD) dans l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="12cbc-148">Become and remain compliant with industry and regional regulations for data storage, encryption, data privacy, and personal data regulations, such as the General Data Protection Regulation (GDPR) for the Europe Union.</span></span>

<span data-ttu-id="12cbc-149">Gestion :</span><span class="sxs-lookup"><span data-stu-id="12cbc-149">Management:</span></span>

- <span data-ttu-id="12cbc-150">Réduire les frais généraux informatiques pour la gestion des logiciels s’exécutant sur des périphériques et des PC client</span><span class="sxs-lookup"><span data-stu-id="12cbc-150">Lower the IT overhead for managing software running on client PCs and devices</span></span>

  <span data-ttu-id="12cbc-151">Automatiser l’installation des mises à jour pour le système d’exploitation Windows et Microsoft Office ProPlus au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="12cbc-151">Automate the installation of updates to the Windows operating system and Microsoft Office ProPlus across the organization.</span></span>

## <a name="mapping-contosos-business-needs-to-microsoft-365-enterprise"></a><span data-ttu-id="12cbc-152">Mappage des besoins métier de Contoso à Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="12cbc-152">Mapping Contoso's business needs to Microsoft 365 Enterprise</span></span>

<span data-ttu-id="12cbc-153">Le service informatique de Contoso a déterminé le mappage suivant des besoins métier aux fonctionnalités de Microsoft 365 E5 avant le déploiement :</span><span class="sxs-lookup"><span data-stu-id="12cbc-153">Contoso's IT department determined the following mapping of business needs to Microsoft 365 Enterprise E5 features prior to deployment:</span></span>

||||
|:-------|:-----|:-----|
| <span data-ttu-id="12cbc-154">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="12cbc-154">**Category**</span></span> | <span data-ttu-id="12cbc-155">**Besoin métier**</span><span class="sxs-lookup"><span data-stu-id="12cbc-155">**Business need**</span></span> | <span data-ttu-id="12cbc-156">**Produits ou fonctionnalités Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="12cbc-156">**Microsoft 365 Enterprise products or features**</span></span> |
| <span data-ttu-id="12cbc-157">Productivité</span><span class="sxs-lookup"><span data-stu-id="12cbc-157">Productivity</span></span> |  |  |
|  | <span data-ttu-id="12cbc-158">Faciliter la collaboration</span><span class="sxs-lookup"><span data-stu-id="12cbc-158">Make collaboration easier</span></span> | <span data-ttu-id="12cbc-159">Microsoft Teams, SharePoint, OneDrive</span><span class="sxs-lookup"><span data-stu-id="12cbc-159">Microsoft Teams, SharePoint, OneDrive</span></span> |
|  | <span data-ttu-id="12cbc-160">Améliorer la productivité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="12cbc-160">Improve productivity for remote and mobile workers</span></span> | <span data-ttu-id="12cbc-161">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="12cbc-161">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="12cbc-162">Accroître la créativité et l’innovation</span><span class="sxs-lookup"><span data-stu-id="12cbc-162">Increase creativity and innovation</span></span> | <span data-ttu-id="12cbc-163">Windows Ink, Cortana at Work, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="12cbc-163">Windows Ink, Cortana at Work, PowerPoint</span></span> |
| <span data-ttu-id="12cbc-164">Sécurité</span><span class="sxs-lookup"><span data-stu-id="12cbc-164">Security</span></span> |  |  |
|  | <span data-ttu-id="12cbc-165">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="12cbc-165">Identity & access management</span></span> | <span data-ttu-id="12cbc-166">Comptes Administrateur général dédiés avec l’authentification multifacteur (MFA) Azure et Azure AD Privileged Identity Management (PIM)</span><span class="sxs-lookup"><span data-stu-id="12cbc-166">Dedicated global administrator accounts with Azure Multi-Factor Authentication (MFA) and Azure AD Privileged Identity Management (PIM)</span></span> <BR> <span data-ttu-id="12cbc-167">Authentification multifacteur pour tous les comptes d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="12cbc-167">MFA for all user accounts</span></span> <BR> <span data-ttu-id="12cbc-168">Accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="12cbc-168">Conditional Access</span></span> <BR> <span data-ttu-id="12cbc-169">Windows Hello</span><span class="sxs-lookup"><span data-stu-id="12cbc-169">Windows Hello</span></span> <BR> <span data-ttu-id="12cbc-170">Windows Credential Guard</span><span class="sxs-lookup"><span data-stu-id="12cbc-170">Windows Credential Guard</span></span> |
|  | <span data-ttu-id="12cbc-171">Protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12cbc-171">Threat protection</span></span> | <span data-ttu-id="12cbc-172">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="12cbc-172">Advanced Threat Analytics</span></span> <BR> <span data-ttu-id="12cbc-173">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="12cbc-173">Windows Defender</span></span> <BR> <span data-ttu-id="12cbc-174">Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12cbc-174">Advanced Threat Protection</span></span> <BR> <span data-ttu-id="12cbc-175">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="12cbc-175">Office 365 Advanced Threat Protection</span></span> <BR> <span data-ttu-id="12cbc-176">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="12cbc-176">Office 365 threat investigation and response</span></span> <BR> |
|  | <span data-ttu-id="12cbc-177">Protection des informations</span><span class="sxs-lookup"><span data-stu-id="12cbc-177">Information protection</span></span> | <span data-ttu-id="12cbc-178">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="12cbc-178">Azure Information Protection</span></span> <BR> <span data-ttu-id="12cbc-179">Protection contre la perte de données Office 365 (DLP)</span><span class="sxs-lookup"><span data-stu-id="12cbc-179">Office 365 Data Loss Prevention (DLP)</span></span> <BR> <span data-ttu-id="12cbc-180">Protection des informations Windows (WIP)</span><span class="sxs-lookup"><span data-stu-id="12cbc-180">Windows Information Protection (WIP)</span></span> <BR> <span data-ttu-id="12cbc-181">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="12cbc-181">Microsoft Cloud App Security</span></span> <BR> <span data-ttu-id="12cbc-182">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="12cbc-182">Microsoft Intune</span></span> |
|  | <span data-ttu-id="12cbc-183">Gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="12cbc-183">Security management</span></span> | <span data-ttu-id="12cbc-184">Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="12cbc-184">Azure Security Center</span></span>  <BR> <span data-ttu-id="12cbc-185">Centre de sécurité Windows Defender</span><span class="sxs-lookup"><span data-stu-id="12cbc-185">Windows Defender Security Center</span></span> |
| <span data-ttu-id="12cbc-186">Accès mobile et à distance, et partenaires professionnels</span><span class="sxs-lookup"><span data-stu-id="12cbc-186">Remote and mobile access and business partners</span></span> |  |  |
|  | <span data-ttu-id="12cbc-187">Meilleure sécurité pour les travailleurs mobiles et à distance</span><span class="sxs-lookup"><span data-stu-id="12cbc-187">Better security for remote and mobile workers</span></span> | <span data-ttu-id="12cbc-188">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="12cbc-188">Microsoft Intune</span></span> |
|  | <span data-ttu-id="12cbc-189">Réduire l’infrastructure d’accès distant pour les employés</span><span class="sxs-lookup"><span data-stu-id="12cbc-189">Reduce remote access infrastructure for employees</span></span> | <span data-ttu-id="12cbc-190">Charges de travail Microsoft 365 et données informatiques</span><span class="sxs-lookup"><span data-stu-id="12cbc-190">Microsoft 365 workloads and cloud-based data</span></span> |
|  | <span data-ttu-id="12cbc-191">Fournir une meilleure connectivité et réduire les frais généraux pour les transactions B2B</span><span class="sxs-lookup"><span data-stu-id="12cbc-191">Provide better connectivity and lower overhead for B2B transactions</span></span> | <span data-ttu-id="12cbc-192">Authentification fédérée et ressources informatiques</span><span class="sxs-lookup"><span data-stu-id="12cbc-192">Federated authentication and cloud-based resources</span></span> |
| <span data-ttu-id="12cbc-193">Conformité</span><span class="sxs-lookup"><span data-stu-id="12cbc-193">Compliance</span></span> |  |  |
|  | <span data-ttu-id="12cbc-194">Respecter les exigences réglementaires locales</span><span class="sxs-lookup"><span data-stu-id="12cbc-194">Adhere to regional regulatory requirements</span></span> | <span data-ttu-id="12cbc-195">Fonctionnalités RGPD dans Office 365</span><span class="sxs-lookup"><span data-stu-id="12cbc-195">GDPR features in Office 365</span></span> |
| <span data-ttu-id="12cbc-196">Gestion</span><span class="sxs-lookup"><span data-stu-id="12cbc-196">Management</span></span> |  |  |
|  | <span data-ttu-id="12cbc-197">Réduire les frais généraux informatiques pour l’installation de mises à jour du client</span><span class="sxs-lookup"><span data-stu-id="12cbc-197">Lower the IT overhead for installing client updates</span></span> | <span data-ttu-id="12cbc-198">Anneaux de déploiement</span><span class="sxs-lookup"><span data-stu-id="12cbc-198">Deployment rings</span></span> <BR> <span data-ttu-id="12cbc-199">Mises à jour pour Windows 10 Entreprise</span><span class="sxs-lookup"><span data-stu-id="12cbc-199">Windows 10 Enterprise updates</span></span> <BR> <span data-ttu-id="12cbc-200">Mises à jour pour Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="12cbc-200">Office 365 ProPlus updates</span></span> |
||||

## <a name="next-step"></a><span data-ttu-id="12cbc-201">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="12cbc-201">Next step</span></span>

<span data-ttu-id="12cbc-202">[En savoir plus](contoso-networking.md) sur le réseau local de Contoso Corporation et sur la façon dont il a été optimisé pour l’accès et la latence vers des ressources informatiques Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="12cbc-202">[Learn](contoso-networking.md) about the Contoso Corporation’s on-premises network and how it was optimized for access and latency to Microsoft 365 cloud-based resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="12cbc-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12cbc-203">See also</span></span>

[<span data-ttu-id="12cbc-204">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="12cbc-204">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="12cbc-205">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="12cbc-205">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
