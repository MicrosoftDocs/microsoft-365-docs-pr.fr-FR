---
title: Exigences de sécurité réseau supplémentaires pour Office 365 Cloud de la communauté du secteur public Haut et DoD
ms.author: dzazzo
author: dzazzo
manager: dzazzo
ms.date: 05/19/2020
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: Adm_O365
search.appverid:
- OGA150m
- OGC150
- OGD150
- MOE150
ms.assetid: ''
description: 'Résumé : Les Office 365 Cloud de la communauté du secteur public Élevé et DoD ont des exigences de sécurité réseau supplémentaires'
hideEdit: true
ms.openlocfilehash: f4c03d364e84d89a1b12e4d858ab46eb3be6ae5e
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52926558"
---
# <a name="additional-network-security-requirements-for-office-365-gcc-high-and-dod"></a><span data-ttu-id="16e99-103">Autres exigences de sécurité réseau pour Office 365 GCC High et DoD</span><span class="sxs-lookup"><span data-stu-id="16e99-103">Additional network security requirements for Office 365 GCC High and DOD</span></span>

<span data-ttu-id="16e99-104">*Cet article s’applique aux Office 365 Cloud de la communauté du secteur public élevé, Office 365 DOD, Microsoft 365 Cloud de la communauté du secteur public Élevé et Microsoft 365 DOD.*</span><span class="sxs-lookup"><span data-stu-id="16e99-104">*This article applies to Office 365 GCC High, Office 365 DOD, Microsoft 365 GCC High, and Microsoft 365 DOD.*</span></span>

<span data-ttu-id="16e99-105">Office 365 Cloud de la communauté du secteur public High et DOD sont des environnements cloud sécurisés qui répondent aux besoins du gouvernement des États-Unis et de ses fournisseurs et sous-traitants.</span><span class="sxs-lookup"><span data-stu-id="16e99-105">Office 365 GCC High and DOD are secure cloud environments to meet the needs of the United States Government and its suppliers and contractors.</span></span>  <span data-ttu-id="16e99-106">Ces environnements cloud ont des restrictions réseau supplémentaires sur lesquelles les points de terminaison externes sont autorisés à accéder aux services.</span><span class="sxs-lookup"><span data-stu-id="16e99-106">These cloud environments have additional network restrictions on which external endpoints the services are permitted to access.</span></span>

<span data-ttu-id="16e99-107">Cloud de la communauté du secteur public Les clients haut et DOD qui prévoient d’utiliser des identités fédérées ou la coexistence hybride peuvent exiger que Microsoft autorise l’accès entrant et/ou sortant à vos déploiements locaux existants.</span><span class="sxs-lookup"><span data-stu-id="16e99-107">GCC High and DOD customers planning to use federated identities or hybrid coexistence may require Microsoft to permit inbound and/or outbound access to your existing on-premises deployments.</span></span>  <span data-ttu-id="16e99-108">Voici quelques exemples de ces activités :</span><span class="sxs-lookup"><span data-stu-id="16e99-108">Examples of these activities include:</span></span>

* <span data-ttu-id="16e99-109">Utilisation d’identités fédérées (avec les services de fédération Active Directory ou un service STS similaire pris en charge)</span><span class="sxs-lookup"><span data-stu-id="16e99-109">Use of federated identities (with Active Directory Federation Services or similar supported STS)</span></span>
* <span data-ttu-id="16e99-110">Coexistence hybride avec un déploiement local Exchange Server ou Skype Entreprise déploiement</span><span class="sxs-lookup"><span data-stu-id="16e99-110">Hybrid coexistence with an on-premises Exchange Server or Skype for Business deployment</span></span>
* <span data-ttu-id="16e99-111">Migration du contenu utilisateur existant à partir d’un système local</span><span class="sxs-lookup"><span data-stu-id="16e99-111">Migration of existing user content from an on-premises system</span></span>

<span data-ttu-id="16e99-112">Pour permettre au service de communiquer avec vos points  de terminaison locaux, vous devez envoyer un courrier électronique à Office 365 ingénierie pour les modifications réseau.</span><span class="sxs-lookup"><span data-stu-id="16e99-112">To permit the service to communicate with your on-premises endpoints, you **must** send an email to Office 365 engineering for network changes.</span></span>

> [!WARNING]
> <span data-ttu-id="16e99-113">Toutes les demandes ont **un** SLA de trois semaines et ne peuvent pas être accélérées en raison des contrôles de sécurité et de conformité requis et des pipelines de déploiement.</span><span class="sxs-lookup"><span data-stu-id="16e99-113">All requests have a **three-week** SLA and cannot be expedited due to the required security and compliance controls and deployment pipelines.</span></span>  <span data-ttu-id="16e99-114">Cela inclut les demandes réseau d’intégration initiales, ainsi que les modifications apportées après la migration vers le service.</span><span class="sxs-lookup"><span data-stu-id="16e99-114">This includes initial onboarding network requests as well as any changes after you have migrated to the service.</span></span>  <span data-ttu-id="16e99-115">Assurez-vous que vos équipes réseau connaissent cette chronologie et l’incluent dans leurs cycles de planification.</span><span class="sxs-lookup"><span data-stu-id="16e99-115">Make sure that your network teams are aware of this timeline and include it in their planning cycles.</span></span>

<span data-ttu-id="16e99-116">Envoyez un e-mail [Office 365 Secteur Public Allow-List demandes avec](mailto:o365gwlt@microsoft.com) les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="16e99-116">Send an email to [Office 365 Government Allow-List Requests](mailto:o365gwlt@microsoft.com) with the following information:</span></span>

* <span data-ttu-id="16e99-117">**À**: [Office 365 Secteur Public Allow-List demandes](mailto:o365gwlt@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="16e99-117">**To**: [Office 365 Government Allow-List Requests](mailto:o365gwlt@microsoft.com)</span></span>
* <span data-ttu-id="16e99-118">**From**: A tenant administrator - the send email **must** match a Global Administrator contact in your tenant</span><span class="sxs-lookup"><span data-stu-id="16e99-118">**From**: A tenant administrator - the send email **must** match a Global Administrator contact in your tenant</span></span>
* <span data-ttu-id="16e99-119">**Objet de** l’e-mail : Office 365 Cloud de la communauté du secteur public réseau élevé - contoso.onmicrosoft.us (remplacer par le nom de votre client)</span><span class="sxs-lookup"><span data-stu-id="16e99-119">**Email subject**: Office 365 GCC High Network Request - contoso.onmicrosoft.us (replace with your tenant name)</span></span>

<span data-ttu-id="16e99-120">Le corps de votre message doit inclure les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="16e99-120">The body of your message should include the following data:</span></span>

* <span data-ttu-id="16e99-121">Votre Microsoft Online Services client (par exemple, contoso.onmicrosoft.com, fabrikam.onmicrosoft.us)</span><span class="sxs-lookup"><span data-stu-id="16e99-121">Your Microsoft Online Services tenant name (for example, contoso.onmicrosoft.com, fabrikam.onmicrosoft.us)</span></span>
* <span data-ttu-id="16e99-122">Une liste de distribution de courrier électronique avec qui Microsoft communiquera pour les communications en cours liées aux modifications du réseau et/ou le suivi des sous-réseaux non valides</span><span class="sxs-lookup"><span data-stu-id="16e99-122">An email distribution list that Microsoft will communicate with for on-going communications related to network changes and/or follow up for invalid subnets</span></span>
* <span data-ttu-id="16e99-123">Indiquez si vous prévoyez d’Microsoft Teams la coexistence hybride avec vos déploiements locaux</span><span class="sxs-lookup"><span data-stu-id="16e99-123">Indicate whether you plan to use Microsoft Teams hybrid coexistence with your on-premises deployments</span></span>
* <span data-ttu-id="16e99-124">URL accessible en externe du système d’identité fédérée (par exemple, sts.contoso.com) et plage d’adresses IP en notation CIDR (par exemple,</span><span class="sxs-lookup"><span data-stu-id="16e99-124">Federated identity system externally accessible URL (for example, sts.contoso.com) and IP address range in CIDR notation (for example,.</span></span> <span data-ttu-id="16e99-125">10.1.1.0/28)</span><span class="sxs-lookup"><span data-stu-id="16e99-125">10.1.1.0/28)</span></span>
* <span data-ttu-id="16e99-126">URL et plage d’adresses IP de liste de révocation de certificats PKI sur site en notation CIDR</span><span class="sxs-lookup"><span data-stu-id="16e99-126">On-Premises PKI Certificate Revocation List URL and IP address range in CIDR notation</span></span>
* <span data-ttu-id="16e99-127">URL et plage d’adresses IP accessibles en externe pour Exchange Server déploiement local en notation CIDR</span><span class="sxs-lookup"><span data-stu-id="16e99-127">Externally accessible URL and IP address range for Exchange Server on-premises deployment in CIDR notation</span></span>
* <span data-ttu-id="16e99-128">URL et plage d’adresses IP accessibles en externe pour Skype Entreprise déploiement local en notation CIDR</span><span class="sxs-lookup"><span data-stu-id="16e99-128">Externally accessible URL and IP address range for Skype for Business on-premises deployment in CIDR notation</span></span>

<span data-ttu-id="16e99-129">Pour des raisons de sécurité et de conformité, gardez à l’esprit les restrictions suivantes sur votre demande :</span><span class="sxs-lookup"><span data-stu-id="16e99-129">For security and compliance reasons, keep in mind the following restrictions on your request:</span></span>

* <span data-ttu-id="16e99-130">Il existe quatre limites de sous-réseau par client</span><span class="sxs-lookup"><span data-stu-id="16e99-130">There is a four subnet limitation per tenant</span></span>
* <span data-ttu-id="16e99-131">Les sous-réseaux doivent être en notation CIDR (par exemple, 10.1.1.0/28)</span><span class="sxs-lookup"><span data-stu-id="16e99-131">Subnets must be in CIDR Notation (for example, 10.1.1.0/28)</span></span>
* <span data-ttu-id="16e99-132">Les plages de sous-réseaux ne peuvent pas être plus /24</span><span class="sxs-lookup"><span data-stu-id="16e99-132">Subnet ranges cannot be larger than /24</span></span>
* <span data-ttu-id="16e99-133">Nous **ne pouvons** pas prendre en charge les demandes d’accès aux services cloud commerciaux (Office 365 commercial, Google G-Suite, Amazon Web Services, etc.)</span><span class="sxs-lookup"><span data-stu-id="16e99-133">We **cannot** accommodate requests to allow access to commercial cloud services (commercial Office 365, Google G-Suite, Amazon Web Services, etc.)</span></span>

<span data-ttu-id="16e99-134">Une fois que votre demande a été reçue et approuvée par Microsoft, il existe un accord de niveau de service de trois semaines pour l’implémentation et ne peut pas être accéléré.</span><span class="sxs-lookup"><span data-stu-id="16e99-134">Once your request has been received and approved by Microsoft, there is a three-week SLA for implementation and cannot be expedited.</span></span>  <span data-ttu-id="16e99-135">Vous recevrez un accusé de réception initial lorsque nous recevons votre demande et un accusé de réception final une fois qu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="16e99-135">You will receive an initial acknowledgment when we’ve received your request and a final acknowledgment once it has been completed.</span></span>
