---
title: Audit et création de rapports dans les services Cloud de Microsoft
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
- SPO_Content
f1.keywords:
- NOCSH
description: Vue d’ensemble des fonctionnalités d’audit et de création de rapports dans Office 365, Microsoft 365 et service assurance.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 89c7ff3556e71ead8ced94bdc396da1c862c2f57
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695831"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a><span data-ttu-id="7033a-103">Audit et création de rapports dans les services Cloud de Microsoft</span><span class="sxs-lookup"><span data-stu-id="7033a-103">Auditing and Reporting in Microsoft cloud services</span></span>

<span data-ttu-id="7033a-104">Les services de Cloud Computing Microsoft incluent plusieurs fonctionnalités d’audit et de création de rapports que vous pouvez utiliser pour suivre l’activité des utilisateurs et de l’administration au sein de leur client, des exemples de modifications apportées aux paramètres de configuration du client Exchange Online et SharePoint Online, ainsi que les modifications apportées par les utilisateurs aux documents et autres éléments.</span><span class="sxs-lookup"><span data-stu-id="7033a-104">Microsoft cloud services include several auditing and reporting features you can use to track user and administrative activity within their tenant, Examples include changes made to Exchange Online and SharePoint Online tenant configuration settings, and changes made by users to documents and other items.</span></span> <span data-ttu-id="7033a-105">Vous pouvez utiliser des informations d’audit et des rapports disponibles dans les services de Cloud Computing Microsoft pour gérer plus efficacement l’expérience utilisateur, atténuer les risques et respecter les obligations de conformité.</span><span class="sxs-lookup"><span data-stu-id="7033a-105">You can use audit information and reports available in Microsoft cloud services to more effectively manage user experience, mitigate risks, and fulfill compliance obligations.</span></span>

## <a name="security--compliance-centers"></a><span data-ttu-id="7033a-106">Centres de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="7033a-106">Security & Compliance Centers</span></span>

<span data-ttu-id="7033a-107">Le centre de sécurité [& sécurité microsoft 365](https://protection.office.com), le [Centre de sécurité Microsoft 365](https://security.microsoft.com)et le [Centre de conformité Microsoft 365](https://compliance.microsoft.com) sont des portails d’un seul point pour protéger les données de votre organisation, et ils incluent de nombreuses fonctionnalités d’audit et de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="7033a-107">The [Microsoft 365 Security & Compliance Center](https://protection.office.com), [Microsoft 365 Security Center](https://security.microsoft.com), and [Microsoft 365 Compliance Center](https://compliance.microsoft.com) are one-stop portals for protecting data in your organization, and they include many auditing and reporting features.</span></span> <span data-ttu-id="7033a-108">Ces centres vous aident à répondre à vos besoins en matière de protection des données ou de conformité et d’auditer l’activité des utilisateurs et des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="7033a-108">These centers help you with your data protection or compliance needs and audit user and administrator activity.</span></span> <span data-ttu-id="7033a-109">Vous pouvez accéder à ces centres à l’aide de votre compte d’administrateur d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="7033a-109">You can access these centers using your subscription admin account.</span></span>

<span data-ttu-id="7033a-110">Ces centres incluent des volets de navigation permettant d’accéder à plusieurs fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="7033a-110">These centers include navigation panes for access to several features:</span></span>

- <span data-ttu-id="7033a-111">**Alertes :** Vous permet de gérer les alertes, d’afficher les alertes liées à la sécurité et de gérer les alertes avancées à l’aide de la [sécurité des applications Cloud](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security).</span><span class="sxs-lookup"><span data-stu-id="7033a-111">**Alerts:** Enables you to manage alerts, view security-related alerts, and manage advanced alerts using [Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security).</span></span>
- <span data-ttu-id="7033a-112">**Autorisations :** Vous permet d' [affecter des autorisations](https://docs.microsoft.com/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) telles que l’administrateur de la conformité, le gestionnaire eDiscovery et d’autres personnes au sein de votre organisation afin qu’ils puissent effectuer des tâches dans ces centres.</span><span class="sxs-lookup"><span data-stu-id="7033a-112">**Permissions:** Enables you to [assign permissions](https://docs.microsoft.com/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) such as Compliance Administrator, eDiscovery Manager, and others to people in your organization so they can perform tasks in these centers.</span></span> <span data-ttu-id="7033a-113">Vous attribuez des autorisations pour la plupart des fonctionnalités de chaque centre, mais les autres autorisations doivent être configurées à l’aide du centre d’administration Exchange et du centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7033a-113">You assign permissions for most features in each center, but other permissions must be configured using the Exchange admin center and SharePoint admin center.</span></span>
- <span data-ttu-id="7033a-114">**Gestion des menaces :** Vous permet de créer et d’appliquer des stratégies de gestion des appareils à l’aide de la [gestion des appareils mobiles Microsoft 365](https://support.microsoft.com/office/overview-of-mobile-device-management-mdm-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)afin de configurer des stratégies de protection contre la [perte de données](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies) (DLP) pour votre organisation, de configurer le filtrage du courrier électronique, anti-programme malveillant, DomainKeys Identified identifiés (DKIM), des pièces jointes fiables, des liens fiables et des applications OAuth.</span><span class="sxs-lookup"><span data-stu-id="7033a-114">**Threat management:** Enables you to create and apply device management policies using [Microsoft 365 Mobile Device Management](https://support.microsoft.com/office/overview-of-mobile-device-management-mdm-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), to set up [data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies) (DLP) policies for your organization, to configure email filtering, anti-malware, DomainKeys Identified Mail (DKIM), safe attachments, safe links, and OAuth apps.</span></span>
- <span data-ttu-id="7033a-115">**Gouvernance des données :** Vous permet d' [importer des données de messagerie ou SharePoint à partir d’autres systèmes vers Microsoft 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), de [configurer des boîtes aux lettres d’archivage](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)et de définir des [stratégies de rétention](https://docs.microsoft.com/microsoft-365/compliance/retention-policies) pour le courrier électronique et d’autres contenus au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7033a-115">**Data governance:** Enables you to [import email or SharePoint data from other systems into Microsoft 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [configure archive mailboxes](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce), and set [retention policies](https://docs.microsoft.com/microsoft-365/compliance/retention-policies) for email and other content within your organization.</span></span>
- <span data-ttu-id="7033a-116">**Recherche & :** Fournit des outils de [recherche de contenu](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), de [Journal d’audit](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), de mise en quarantaine et de gestion des dossiers [eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) pour explorer rapidement les activités dans les boîtes aux lettres, les groupes et les dossiers publics Exchange Online, SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="7033a-116">**Search & investigation:** Provides [content search](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [audit log](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), quarantine, and [eDiscovery case management](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) tools to quickly drill into activity across Exchange Online mailboxes, groups and public folders, SharePoint Online, and OneDrive for Business.</span></span>
- <span data-ttu-id="7033a-117">**Rapports :** Vous permet d’accéder rapidement aux [rapports](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) pour SharePoint Online, OneDrive entreprise, Exchange Online et Azure ad.</span><span class="sxs-lookup"><span data-stu-id="7033a-117">**Reports:** Enables you to quickly access [reports](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) for SharePoint Online, OneDrive for Business, Exchange Online, and Azure AD.</span></span>
- <span data-ttu-id="7033a-118">**Assurance de service :** Fournit des informations sur la façon dont Microsoft gère la sécurité, la confidentialité et la conformité avec les normes globales pour Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune et d’autres services Cloud.</span><span class="sxs-lookup"><span data-stu-id="7033a-118">**Service assurance:** Provides information about how Microsoft maintains security, privacy, and compliance with global standards for Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune, and other cloud services.</span></span> <span data-ttu-id="7033a-119">Inclut également l’accès à des rapports d’audit, tels que ISO, SOC et d’autres rapports, ainsi que des contrôles audités, qui fournissent des détails sur les différents contrôles qui ont été testés et vérifiés par des auditeurs tiers de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7033a-119">Also includes access to third-party ISO, SOC, and other audit reports, as well as Audited Controls, which provides details about the various controls that have been tested and verified by third-party auditors of Microsoft 365.</span></span>

## <a name="service-assurance"></a><span data-ttu-id="7033a-120">Service assurance</span><span class="sxs-lookup"><span data-stu-id="7033a-120">Service Assurance</span></span>

<span data-ttu-id="7033a-121">De nombreuses organisations dans les industries réglementées sont soumises à des exigences de conformité étendues.</span><span class="sxs-lookup"><span data-stu-id="7033a-121">Many organizations in regulated industries are subject to extensive compliance requirements.</span></span> <span data-ttu-id="7033a-122">Pour effectuer leurs évaluations des risques propres, les clients ont souvent besoin d’informations détaillées sur la façon dont Microsoft 365 maintient la sécurité et la confidentialité de leurs données.</span><span class="sxs-lookup"><span data-stu-id="7033a-122">To perform their own risk assessments, customers often need in-depth information about how Microsoft 365 maintains the security and privacy of their data.</span></span> <span data-ttu-id="7033a-123">Microsoft s’engage à respecter la sécurité et la confidentialité des données des clients dans ses services Cloud et à bénéficier d’une relation de confiance client en fournissant une vue transparente de ses opérations et un accès facile aux rapports et aux évaluations de conformité indépendantes.</span><span class="sxs-lookup"><span data-stu-id="7033a-123">Microsoft is committed to the security and privacy of customer data in its cloud services and to earning customer trust by providing a transparent view of its operations, and easy access to independent compliance reports and assessments.</span></span>

<span data-ttu-id="7033a-124">Service assurance fournit la transparence des opérations et des informations sur la façon dont Microsoft conserve la sécurité, la confidentialité et la conformité des données client dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7033a-124">Service Assurance provides transparency of operations and information about how Microsoft maintains the security, privacy, and compliance of customer data in Microsoft 365.</span></span> <span data-ttu-id="7033a-125">Elle inclut des rapports d’audit tiers, ainsi qu’une bibliothèque de livres blancs, de FAQ et d’autres informations sur les sujets Microsoft 365, telles que le chiffrement des données, la résilience des données, la gestion des incidents de sécurité, etc.</span><span class="sxs-lookup"><span data-stu-id="7033a-125">It includes third-party audit reports along with a library of white papers, FAQs, and other materials on Microsoft 365 topics such as data encryption, data resiliency, security incident management and more.</span></span> <span data-ttu-id="7033a-126">Les clients peuvent utiliser ces informations pour effectuer leurs propres évaluations de risques réglementaires.</span><span class="sxs-lookup"><span data-stu-id="7033a-126">Customers can use this information to perform their own regulatory risk assessments.</span></span> <span data-ttu-id="7033a-127">Les responsables de la conformité peuvent affecter le rôle « utilisateur d’assurance de service » pour permettre aux utilisateurs d’accéder à l’assurance de service.</span><span class="sxs-lookup"><span data-stu-id="7033a-127">Compliance officers can assign the "Service Assurance User" role to give users access to Service Assurance.</span></span> <span data-ttu-id="7033a-128">L’administrateur client peut également fournir aux utilisateurs externes, tels que des auditeurs indépendants, un accès aux informations du tableau de bord service assurance via le [portail d’approbation de service Cloud Microsoft](https://aka.ms/STP) (STP).</span><span class="sxs-lookup"><span data-stu-id="7033a-128">The tenant administrator can also provide external users, such as independent auditors, with access to information in the Service Assurance dashboard through the [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) (STP).</span></span>

## <a name="onedrive-for-business-admin-center"></a><span data-ttu-id="7033a-129">Centre d’administration de OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="7033a-129">OneDrive for Business admin center</span></span>

<span data-ttu-id="7033a-130">Le centre d’administration Microsoft OneDrive vous permet de gérer rapidement et facilement les paramètres OneDrive entreprise de votre organisation à partir d’un seul et même emplacement.</span><span class="sxs-lookup"><span data-stu-id="7033a-130">The Microsoft OneDrive admin center helps you quickly and easily manage your organization's OneDrive for Business settings in one place.</span></span> <span data-ttu-id="7033a-131">Pour utiliser le centre d’administration OneDrive, l’accès à onedrive.com est requis.</span><span class="sxs-lookup"><span data-stu-id="7033a-131">To use the OneDrive admin center, access to onedrive.com is required.</span></span> <span data-ttu-id="7033a-132">Vous devez également être administrateur général de votre organisation ou administrateur personnalisé avec le rôle d’administrateur SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7033a-132">You must also be a global admin for your organization or a custom admin with the SharePoint administrator role.</span></span> <span data-ttu-id="7033a-133">Accédez au centre d’administration OneDrive entreprise à l’adresse [https://admin.onedrive.com](https://admin.onedrive.com/) .</span><span class="sxs-lookup"><span data-stu-id="7033a-133">Access the OneDrive for Business admin center at [https://admin.onedrive.com](https://admin.onedrive.com/).</span></span>

<span data-ttu-id="7033a-134">Les fonctionnalités clés incluent une zone de conformité qui fournit aux administrateurs des liens vers le centre de gestion approprié pour les scénarios clés tels que la recherche dans le journal d’audit, l’utilisation de DLP, la rétention, la découverte électronique et l’alerte.</span><span class="sxs-lookup"><span data-stu-id="7033a-134">Key features include a compliance area that provides administrators with links to the appropriate management center for key scenarios like searching the audit log, working with DLP, retention, eDiscovery, and alerting.</span></span>

## <a name="related-links"></a><span data-ttu-id="7033a-135">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="7033a-135">Related Links</span></span>

- [<span data-ttu-id="7033a-136">eDiscovery et fonctionnalités de recherche</span><span class="sxs-lookup"><span data-stu-id="7033a-136">eDiscovery and Search Features</span></span>](microsoft-365-ediscovery-and-search-features.md)
- [<span data-ttu-id="7033a-137">Fonctionnalités de création de rapports Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7033a-137">Microsoft 365 Reporting Features</span></span>](microsoft-365-reporting-features.md)
- [<span data-ttu-id="7033a-138">API d’activité de gestion Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7033a-138">Microsoft 365 Management Activity API</span></span>](microsoft-365-management-activity-api.md)
- [<span data-ttu-id="7033a-139">Migrations de boîtes aux lettres Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7033a-139">Microsoft 365 Mailbox Migrations</span></span>](microsoft-365-mailbox-migrations.md)
- [<span data-ttu-id="7033a-140">Journalisation interne pour Microsoft 365 Engineering</span><span class="sxs-lookup"><span data-stu-id="7033a-140">Internal Logging for Microsoft 365 Engineering</span></span>](microsoft-365-internal-logging.md)