---
title: Contrôles d’accès administratif dans Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: seo-marvel-apr2020
description: Cet article fournit une vue d’ensemble des contrôles d’accès administratifs et de la catégorisation des données dans Microsoft 365.
ms.openlocfilehash: 817a5907566435d021fe78d89b5c9476c04318d0
ms.sourcegitcommit: c029834c8a914b4e072de847fc4c3a3dde7790c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "47332591"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="2da86-103">Contrôles d’accès administratif dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2da86-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="2da86-104">Microsoft a investi beaucoup de systèmes et de contrôles qui automatisent la plupart des opérations Microsoft 365, tout en limitant intentionnellement l’accès au contenu client par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2da86-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="2da86-105">Les êtres humains gouvernent le service et le logiciel fonctionne avec le service.</span><span class="sxs-lookup"><span data-stu-id="2da86-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="2da86-106">Cela permet à Microsoft de gérer Microsoft 365 à l’horizontale et de gérer les risques de menaces internes pour le contenu du client.</span><span class="sxs-lookup"><span data-stu-id="2da86-106">This enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="2da86-107">Par défaut, les ingénieurs Microsoft disposent de zéro privilège administratif permanent et d’un accès permanent au contenu client dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2da86-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="2da86-108">Un ingénieur Microsoft peut disposer d’un accès limité, audité et sécurisé au contenu d’un client pendant une durée limitée.</span><span class="sxs-lookup"><span data-stu-id="2da86-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="2da86-109">L’accès est uniquement nécessaire pour les opérations de service et uniquement lorsqu’il est approuvé par un membre de la direction générale Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2da86-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="2da86-110">Pour les clients titulaires d’une licence Lockbox client, le client fournit une approbation d’accès à son contenu hébergé sur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2da86-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="2da86-111">Microsoft fournit des services en ligne à l’aide de plusieurs formes de remise en nuage :</span><span class="sxs-lookup"><span data-stu-id="2da86-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="2da86-112">**Nuages publics :** Inclut des versions mutualisées de Microsoft 365, Azure et d’autres services hébergés en Amérique du Nord, en Amérique du Sud, en Europe, en Asie, en Australie, etc.</span><span class="sxs-lookup"><span data-stu-id="2da86-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="2da86-113">**Clouds nationaux :** Comprend tous les nuages souverains et tiers gérés en dehors des États-Unis (sauf ceux notés précédemment), tels que Microsoft 365 en Chine (géré par 21Vianet) et Microsoft 365 en Allemagne (géré par Microsoft, mais sous un modèle dans lequel un tiers de confiance des données, Deutsche Telekom, contrôle et surveille l’accès de Microsoft aux données et systèmes clients qui contiennent des données client).</span><span class="sxs-lookup"><span data-stu-id="2da86-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="2da86-114">**Clouds gouvernementaux :** Inclut Microsoft 365 et Azure services disponibles pour les clients gouvernementaux des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="2da86-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="2da86-115">Pour les besoins de cet article, les services Microsoft 365 sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2da86-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="2da86-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2da86-116">Exchange Online</span></span>](https://docs.microsoft.com/Exchange/exchange-online)
- [<span data-ttu-id="2da86-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="2da86-117">Exchange Online Protection</span></span>](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="2da86-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="2da86-118">SharePoint Online</span></span>](https://docs.microsoft.com/sharepoint/sharepoint-online)
- [<span data-ttu-id="2da86-119">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="2da86-119">OneDrive for Business</span></span>](https://docs.microsoft.com/OneDrive/onedrive)
- [<span data-ttu-id="2da86-120">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="2da86-120">Skype for Business</span></span>](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="2da86-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2da86-121">Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="2da86-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="2da86-122">Yammer</span></span>](https://docs.microsoft.com/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="2da86-123">Contrôles d’accès Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2da86-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="2da86-124">À des fins de contrôle d’accès, Microsoft catégorise les données Microsoft 365 en tant que données client ou d’autres types de données.</span><span class="sxs-lookup"><span data-stu-id="2da86-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="2da86-125">Données client</span><span class="sxs-lookup"><span data-stu-id="2da86-125">Customer data</span></span>

<span data-ttu-id="2da86-126">Les données client sont toutes les données fournies par ou pour le compte d’un client lors de l’utilisation des services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2da86-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="2da86-127">Il s’agit de contenu client directement créé ou téléchargé par les utilisateurs de Microsoft 365, notamment :</span><span class="sxs-lookup"><span data-stu-id="2da86-127">This is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="2da86-128">Messages électroniques</span><span class="sxs-lookup"><span data-stu-id="2da86-128">Emails</span></span>
- <span data-ttu-id="2da86-129">Contenu SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="2da86-129">SharePoint Online content</span></span>
- <span data-ttu-id="2da86-130">Messages instantanés</span><span class="sxs-lookup"><span data-stu-id="2da86-130">Instant messages</span></span>
- <span data-ttu-id="2da86-131">Éléments de calendrier</span><span class="sxs-lookup"><span data-stu-id="2da86-131">Calendar items</span></span>
- <span data-ttu-id="2da86-132">Documents</span><span class="sxs-lookup"><span data-stu-id="2da86-132">Documents</span></span>
- <span data-ttu-id="2da86-133">Contacts</span><span class="sxs-lookup"><span data-stu-id="2da86-133">Contacts</span></span>
- <span data-ttu-id="2da86-134">Informations identifiables par l’utilisateur final (EUII) (données propres à un utilisateur ou pouvant être liées à un utilisateur individuel, mais n’incluant pas de contenu client)</span><span class="sxs-lookup"><span data-stu-id="2da86-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="2da86-135">Autres types de données</span><span class="sxs-lookup"><span data-stu-id="2da86-135">Other types of data</span></span>

<span data-ttu-id="2da86-136">Les autres types de données sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2da86-136">Other types of data include:</span></span>

- <span data-ttu-id="2da86-137">**Données de compte :** Inclut des données d’administration (informations fournies par les administrateurs lorsqu’ils se connectent ou achètent des services) et des données de paiement (informations sur les instruments de paiement, telles que les informations de carte de crédit).</span><span class="sxs-lookup"><span data-stu-id="2da86-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="2da86-138">**Informations identifiables de l’Organisation :** Inclut des données utilisées pour identifier un client, des données d’utilisation et ne pas être lié à un utilisateur individuel ou incluse dans le contenu du client.</span><span class="sxs-lookup"><span data-stu-id="2da86-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="2da86-139">**Métadonnées système :** Inclut des journaux de service qui contiennent des paramètres de configuration, l’état du système, des adresses IP Microsoft et des informations techniques sur les abonnements et les clients.</span><span class="sxs-lookup"><span data-stu-id="2da86-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="2da86-140">Microsoft a établi des mécanismes de contrôle d’accès pour s’assurer que personne ne dispose d’un accès non approuvé aux données du client ou aux données de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="2da86-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="2da86-141">Les données de contrôle d’accès gèrent l’accès à d’autres types de données ou fonctions au sein de l’environnement, y compris l’accès au contenu du client ou EUII, les mots de passe Microsoft, les certificats de sécurité et d’autres données liées à l’authentification.</span><span class="sxs-lookup"><span data-stu-id="2da86-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="2da86-142">Les mécanismes de contrôle d’accès protègent également contre les accès physiques, logiques ou distants non approuvés à l’environnement de production Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2da86-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="2da86-143">Il existe trois catégories de contrôles d’accès utilisés par Microsoft pour l’exploitation de Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="2da86-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="2da86-144">Contrôles d’isolation</span><span class="sxs-lookup"><span data-stu-id="2da86-144">Isolation controls</span></span>
- <span data-ttu-id="2da86-145">Contrôles du personnel</span><span class="sxs-lookup"><span data-stu-id="2da86-145">Personnel controls</span></span>
- <span data-ttu-id="2da86-146">Contrôles de technologie</span><span class="sxs-lookup"><span data-stu-id="2da86-146">Technology controls</span></span>

<span data-ttu-id="2da86-147">Lorsqu’ils sont combinés, ces contrôles aident à prévenir et à détecter les actions malveillantes dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2da86-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="2da86-148">Outre les contrôles d’isolation, de personnel et de technologie utilisés par Microsoft, il existe une quatrième catégorie de contrôles : ceux mis en œuvre par les clients.</span><span class="sxs-lookup"><span data-stu-id="2da86-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those implemented by customers.</span></span>

<span data-ttu-id="2da86-149">Microsoft 365 vous permet de gérer les données de la même manière que les données sont gérées dans les environnements locaux.</span><span class="sxs-lookup"><span data-stu-id="2da86-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="2da86-150">La personne qui souscrit une organisation pour Microsoft 365 devient automatiquement un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2da86-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="2da86-151">L’administrateur global a accès à toutes les fonctionnalités des portails de gestion et peut :</span><span class="sxs-lookup"><span data-stu-id="2da86-151">The global admin has access to all features in management portals and can:</span></span>

- <span data-ttu-id="2da86-152">Créer ou modifier des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2da86-152">Create or edit users</span></span>
- <span data-ttu-id="2da86-153">Attribuer des rôles d’administrateur à d’autres personnes</span><span class="sxs-lookup"><span data-stu-id="2da86-153">Assign admin roles to others</span></span>
- <span data-ttu-id="2da86-154">Réinitialiser les mots de passe utilisateur</span><span class="sxs-lookup"><span data-stu-id="2da86-154">Reset user passwords</span></span>
- <span data-ttu-id="2da86-155">Gérer les licences utilisateur</span><span class="sxs-lookup"><span data-stu-id="2da86-155">Manage user licenses</span></span>
- <span data-ttu-id="2da86-156">Gérer les domaines</span><span class="sxs-lookup"><span data-stu-id="2da86-156">Manage domains</span></span>
- <span data-ttu-id="2da86-157">Approuver les demandes de référentiel sécurisé du client</span><span class="sxs-lookup"><span data-stu-id="2da86-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="2da86-158">Il est recommandé que chaque organisation configure au moins deux comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2da86-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="2da86-159">Pour les grandes organisations d’entreprise, nous recommandons des comptes d’administrateur spécialisés qui remplissent différentes fonctions.</span><span class="sxs-lookup"><span data-stu-id="2da86-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="2da86-160">Pour plus d’informations sur l’attribution des rôles et des autorisations d’administrateur, voir [Assign admin Roles](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) et [about admin Roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="2da86-160">For information about assigning admin roles and permissions, see [Assign admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="2da86-161">Liens connexes</span><span class="sxs-lookup"><span data-stu-id="2da86-161">Related Links</span></span>

- [<span data-ttu-id="2da86-162">Contrôles d’isolation</span><span class="sxs-lookup"><span data-stu-id="2da86-162">Isolation Controls</span></span>](microsoft-365-isolation-controls.md)
- [<span data-ttu-id="2da86-163">Contrôles du personnel</span><span class="sxs-lookup"><span data-stu-id="2da86-163">Personnel Controls</span></span>](microsoft-365-personnel-controls.md)
- [<span data-ttu-id="2da86-164">Contrôles technologiques</span><span class="sxs-lookup"><span data-stu-id="2da86-164">Technology Controls</span></span>](microsoft-365-technology-controls.md)
- [<span data-ttu-id="2da86-165">Surveillance et audit des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="2da86-165">Monitoring and Auditing Access Controls</span></span>](microsoft-365-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="2da86-166">Contrôles d’accès de Yammer Entreprise</span><span class="sxs-lookup"><span data-stu-id="2da86-166">Yammer Enterprise Access Controls</span></span>](microsoft-365-yammer-enterprise-access-controls.md)
