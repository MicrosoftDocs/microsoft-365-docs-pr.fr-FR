---
title: Autres exigences en matière de sécurité réseau pour Office 365 GCC High et DoD
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
description: 'Résumé : Office 365 GCC High et DoD ont des exigences de sécurité réseau supplémentaires'
hideEdit: true
ms.openlocfilehash: 4817edfcea638324e26eb855d1ea33936be1bfb4
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689907"
---
# <a name="additional-network-security-requirements-for-office-365-gcc-high-and-dod"></a><span data-ttu-id="b1f25-103">Autres exigences en matière de sécurité réseau pour Office 365 GCC High et DOD</span><span class="sxs-lookup"><span data-stu-id="b1f25-103">Additional network security requirements for Office 365 GCC High and DOD</span></span>

<span data-ttu-id="b1f25-104">*Cet article s’applique à Office 365 GCC High, Office 365 DOD, Microsoft 365 GCC High et Microsoft 365 DOD.*</span><span class="sxs-lookup"><span data-stu-id="b1f25-104">*This article applies to Office 365 GCC High, Office 365 DOD, Microsoft 365 GCC High, and Microsoft 365 DOD.*</span></span>

<span data-ttu-id="b1f25-105">Office 365 GCC High et DOD sont des environnements de Cloud sécurisés pour répondre aux besoins du gouvernement des États-Unis et de ses fournisseurs et sous-traitants.</span><span class="sxs-lookup"><span data-stu-id="b1f25-105">Office 365 GCC High and DOD are secure cloud environments to meet the needs of the United States Government and its suppliers and contractors.</span></span>  <span data-ttu-id="b1f25-106">Ces environnements Cloud ont des restrictions réseau supplémentaires auxquelles les services sont autorisés à accéder.</span><span class="sxs-lookup"><span data-stu-id="b1f25-106">These cloud environments have additional network restrictions on which external endpoints the services are permitted to access.</span></span>

<span data-ttu-id="b1f25-107">Les clients de GCC High et DOD qui prévoient d’utiliser des identités fédérées ou une coexistence hybride peuvent exiger que Microsoft autorise l’accès entrant et/ou sortant à vos déploiements locaux existants.</span><span class="sxs-lookup"><span data-stu-id="b1f25-107">GCC High and DOD customers planning to use federated identities or hybrid co-existence may require Microsoft to permit inbound and/or outbound access to your existing on-premises deployments.</span></span>  <span data-ttu-id="b1f25-108">Voici des exemples de ces activités :</span><span class="sxs-lookup"><span data-stu-id="b1f25-108">Examples of these activities include:</span></span>

* <span data-ttu-id="b1f25-109">Utilisation d’identités fédérées (avec les services ADFS (Active Directory Federation Services) ou un STS pris en charge similaire)</span><span class="sxs-lookup"><span data-stu-id="b1f25-109">Use of federated identities (with Active Directory Federation Services or similar supported STS)</span></span>
* <span data-ttu-id="b1f25-110">Coexistence hybride avec un déploiement Exchange Server ou Skype entreprise local</span><span class="sxs-lookup"><span data-stu-id="b1f25-110">Hybrid coexistence with an on-premises Exchange Server or Skype for Business deployment</span></span>
* <span data-ttu-id="b1f25-111">Migration de contenu utilisateur existant à partir d’un système local</span><span class="sxs-lookup"><span data-stu-id="b1f25-111">Migration of existing user content from an on-premises system</span></span>

<span data-ttu-id="b1f25-112">Pour permettre au service de communiquer avec vos points de terminaison locaux, vous **devez** envoyer un message électronique à Office 365 Engineering pour les modifications réseau.</span><span class="sxs-lookup"><span data-stu-id="b1f25-112">To permit the service to communicate with your on-premises endpoints, you **must** send an email to Office 365 engineering for network changes.</span></span>

> [!WARNING]
> <span data-ttu-id="b1f25-113">Toutes les demandes ont un contrat SLA de **trois semaines** et ne peuvent pas être accélérées en raison des contrôles de sécurité et de conformité et des pipelines de déploiement requis.</span><span class="sxs-lookup"><span data-stu-id="b1f25-113">All requests have a **three-week** SLA and cannot be expedited due to the required security and compliance controls and deployment pipelines.</span></span>  <span data-ttu-id="b1f25-114">Cela inclut les requêtes réseau de l’intégration initiale ainsi que toutes les modifications une fois que vous avez effectué la migration vers le service.</span><span class="sxs-lookup"><span data-stu-id="b1f25-114">This includes initial onboarding network requests as well as any changes after you have migrated to the service.</span></span>  <span data-ttu-id="b1f25-115">Assurez-vous que les équipes réseau connaissent cette chronologie et l’incluent dans leurs cycles de planification.</span><span class="sxs-lookup"><span data-stu-id="b1f25-115">Please ensure that your network teams are aware of this timeline and include it in their planning cycles.</span></span>

<span data-ttu-id="b1f25-116">Veuillez envoyer un e-mail à la [liste d’autorisation du réseau gouvernemental Office 365](mailto:o365gwlt@microsoft.com) avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1f25-116">Please send an email to [Office 365 Government Network Whitelist](mailto:o365gwlt@microsoft.com) with the following information:</span></span>

* <span data-ttu-id="b1f25-117">**Vers**: [liste d’autorisation du réseau gouvernemental Office 365](mailto:o365gwlt@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="b1f25-117">**To**: [Office 365 Government Network Whitelist](mailto:o365gwlt@microsoft.com)</span></span>
* <span data-ttu-id="b1f25-118">**De**: un administrateur de client : le courrier électronique d’envoi **doit** correspondre à un contact d’administrateur global dans votre client.</span><span class="sxs-lookup"><span data-stu-id="b1f25-118">**From**: A tenant administrator - the send email **must** match a Global Administrator contact in your tenant</span></span>
* <span data-ttu-id="b1f25-119">**Message**de l’objet : Office 365 GCC High Network Request-contoso.onmicrosoft.US (remplacez ceci par le nom de votre client)</span><span class="sxs-lookup"><span data-stu-id="b1f25-119">**Email subject**: Office 365 GCC High Network Request - contoso.onmicrosoft.us (replace this with your tenant name)</span></span>

<span data-ttu-id="b1f25-120">Le corps de votre message doit inclure les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="b1f25-120">The body of your message should include the following data:</span></span>

* <span data-ttu-id="b1f25-121">Votre nom de client Microsoft Online Services (par exemple, contoso.onmicrosoft.com, fabrikam.onmicrosoft.us)</span><span class="sxs-lookup"><span data-stu-id="b1f25-121">Your Microsoft Online Services tenant name (i.e. contoso.onmicrosoft.com, fabrikam.onmicrosoft.us)</span></span>
* <span data-ttu-id="b1f25-122">Une liste de distribution de courrier électronique avec laquelle Microsoft communiquera pour les communications en cours liées aux changements de réseau et/ou au suivi des sous-réseaux non valides</span><span class="sxs-lookup"><span data-stu-id="b1f25-122">An email distribution list that Microsoft will communicate with for on-going communications related to network changes and/or follow up for invalid subnets</span></span>
* <span data-ttu-id="b1f25-123">Indiquer si vous envisagez d’utiliser la coexistence hybride Microsoft teams avec vos déploiements locaux</span><span class="sxs-lookup"><span data-stu-id="b1f25-123">Indicate whether you plan to use Microsoft Teams hybrid co-existence with your on-premises deployments</span></span>
* <span data-ttu-id="b1f25-124">URL du système d’identité fédéré accessible en externe (par exemple, sts.contoso.com) et plage d’adresses IP dans la notation CIDR (par exemple, 10.1.1.0/28)</span><span class="sxs-lookup"><span data-stu-id="b1f25-124">Federated identity system externally accessible URL (e.g. sts.contoso.com) and IP address range in CIDR notation (e.g. 10.1.1.0/28)</span></span>
* <span data-ttu-id="b1f25-125">URL de la liste de révocation de certificats PKI sur site et plage d’adresses IP dans la notation CIDR</span><span class="sxs-lookup"><span data-stu-id="b1f25-125">On-Premises PKI Certificate Revocation List URL and IP address range in CIDR notation</span></span>
* <span data-ttu-id="b1f25-126">URL et plage d’adresses IP accessibles en externe pour le déploiement local d’Exchange Server dans la notation CIDR</span><span class="sxs-lookup"><span data-stu-id="b1f25-126">Externally accessible URL and IP address range for Exchange Server on-premises deployment in CIDR notation</span></span>
* <span data-ttu-id="b1f25-127">URL accessible en externe et plage d’adresses IP pour le déploiement local de Skype entreprise dans la notation CIDR</span><span class="sxs-lookup"><span data-stu-id="b1f25-127">Externally accessible URL and IP address range for Skype for Business on-premises deployment in CIDR notation</span></span>

<span data-ttu-id="b1f25-128">Pour des raisons de sécurité et de conformité, gardez à l’esprit les restrictions suivantes sur votre demande :</span><span class="sxs-lookup"><span data-stu-id="b1f25-128">For security and compliance reasons, please keep in mind the following restrictions on your request:</span></span>

* <span data-ttu-id="b1f25-129">Il existe quatre limitations de sous-réseau par client</span><span class="sxs-lookup"><span data-stu-id="b1f25-129">There is a four subnet limitation per tenant</span></span>
* <span data-ttu-id="b1f25-130">Les sous-réseaux doivent être en notation CIDR (par exemple, 10.1.1.0/28)</span><span class="sxs-lookup"><span data-stu-id="b1f25-130">Subnets must be in CIDR Notation (e.g. 10.1.1.0/28)</span></span>
* <span data-ttu-id="b1f25-131">Les plages de sous-réseau ne peuvent pas dépasser/24</span><span class="sxs-lookup"><span data-stu-id="b1f25-131">Subnet ranges cannot be larger than /24</span></span>
* <span data-ttu-id="b1f25-132">Nous **ne pouvons pas** prendre en charge les demandes pour autoriser l’accès aux services Cloud commerciaux (Office 365, Google G-suite, les services Web Amazon, etc.)</span><span class="sxs-lookup"><span data-stu-id="b1f25-132">We **cannot** accommodate requests to allow access to commercial cloud services (commercial Office 365, Google G-Suite, Amazon Web Services, etc.)</span></span>

<span data-ttu-id="b1f25-133">Une fois que votre demande a été reçue et approuvée par Microsoft, il existe un contrat SLA de trois semaines pour l’implémentation et ne peut pas être accéléré.</span><span class="sxs-lookup"><span data-stu-id="b1f25-133">Once your request has been received and approved by Microsoft, there is a three-week SLA for implementation and cannot be expedited.</span></span>  <span data-ttu-id="b1f25-134">Vous recevrez un accusé de réception initial lorsque nous aurons reçu votre demande et un accusé de réception final une fois qu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="b1f25-134">You will receive an initial acknowledgment when we’ve received your request and a final acknowledgement once it has been completed.</span></span>
