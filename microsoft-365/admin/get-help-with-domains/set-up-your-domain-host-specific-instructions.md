---
title: Configurer votre domaine (instructions spécifiques de l’hôte)
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: ae950c9e-e8d9-4108-b0cb-449156998580
description: Découvrez comment gérer vos propres enregistrements DNS ou laisser Microsoft gérer vos enregistrements DNS pour vous.
ms.custom: okr_smb
ms.openlocfilehash: ea3a62c048706f36cd7b1590851d8b372e0a1677
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43628421"
---
# <a name="set-up-your-domain-host-specific-instructions"></a><span data-ttu-id="9a194-103">Configurer votre domaine (instructions spécifiques de l’hôte)</span><span class="sxs-lookup"><span data-stu-id="9a194-103">Set up your domain (host-specific instructions)</span></span>

<span data-ttu-id="9a194-104">Pour commencer à utiliser un domaine personnalisé (contoso.com) avec Office 365, vous devez vérifier votre domaine et configurer les enregistrements DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="9a194-104">To start using a custom domain (contoso.com) with Office 365, you need to verify your domain and configure your domain's DNS records.</span></span> 
  
<span data-ttu-id="9a194-105">Vous pouvez ajouter et gérer des enregistrements DNS à l’aide des outils d’administration de votre hôte de domaine ou accorder à Microsoft le contrôle de vos enregistrements de domaine et nous allons les configurer pour vous.</span><span class="sxs-lookup"><span data-stu-id="9a194-105">You can add and manage DNS records using the administrative tools at your domain host, or give Microsoft control of your domain records and we'll set them up for you.</span></span>
  
<span data-ttu-id="9a194-106">Sélectionnez votre hôte de domaine ci-dessous pour obtenir les étapes exactes.</span><span class="sxs-lookup"><span data-stu-id="9a194-106">Select your domain host below for the exact steps.</span></span> <span data-ttu-id="9a194-107">Si vous n’êtes pas sûr de votre hôte, reportez-vous à [la rubrique Rechercher votre bureau d’enregistrement de domaines](find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="9a194-107">If you're not sure who your host is, see [Find your domain registrar](find-your-domain-registrar.md).</span></span>
  

## <a name="let-office-365-manage-your-dns-records"></a><span data-ttu-id="9a194-108">Permettre à Office 365 de gérer vos enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="9a194-108">Let Office 365 manage your DNS records</span></span>

||
|---|---|
|[<span data-ttu-id="9a194-109">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="9a194-109">1&1 IONOS</span></span>](../dns/change-nameservers-at-1-1-internet.md) |
|[<span data-ttu-id="9a194-110">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="9a194-110">Amazon Web Services (AWS)</span></span>](../dns/change-nameservers-at-aws.md) |
 [<span data-ttu-id="9a194-111">Bluehost</span><span class="sxs-lookup"><span data-stu-id="9a194-111">Bluehost</span></span>](../dns/change-nameservers-at-bluehost.md)|
|[<span data-ttu-id="9a194-112">Google Domains</span><span class="sxs-lookup"><span data-stu-id="9a194-112">Google   Domains</span></span>](../dns/change-nameservers-at-google-domains.md) |
|[<span data-ttu-id="9a194-113">Hostgator</span><span class="sxs-lookup"><span data-stu-id="9a194-113">Hostgator   </span></span>](../dns/change-nameservers-at-hostgator.md)  |  
|[<span data-ttu-id="9a194-114">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="9a194-114">MyDomain</span></span>](../dns/change-nameservers-at-mydomain.md) | 
|[<span data-ttu-id="9a194-115">Namecheap</span><span class="sxs-lookup"><span data-stu-id="9a194-115">Namecheap</span></span>](../dns/change-nameservers-at-namecheap.md)|
|[<span data-ttu-id="9a194-116">Network Solutions</span><span class="sxs-lookup"><span data-stu-id="9a194-116">Network Solutions</span></span>](../dns/change-nameservers-at-network-solutions.md) |  

<span data-ttu-id="9a194-117">Vous pouvez également apprendre à [modifier les serveurs de noms de manière à configurer Office 365 avec n’importe quel](change-nameservers-at-any-domain-registrar.md)Bureau d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="9a194-117">Or, learn how to [change nameservers to set up Office 365 with any domain registrar](change-nameservers-at-any-domain-registrar.md).</span></span>

## <a name="manage-your-own-dns-records"></a><span data-ttu-id="9a194-118">Gérer vos propres enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="9a194-118">Manage your own DNS records</span></span>

|                           |                          |
|---------------------------|--------------------------|
| [<span data-ttu-id="9a194-119">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="9a194-119">1&1 IONOS</span></span>](../dns/create-dns-records-at-1-1-internet.md) | [<span data-ttu-id="9a194-120">Sensitiv</span><span class="sxs-lookup"><span data-stu-id="9a194-120">Hover</span></span>](../dns/create-dns-records-at-hover.md) |
| [<span data-ttu-id="9a194-121">123-reg.co.uk</span><span class="sxs-lookup"><span data-stu-id="9a194-121">123-reg.co.uk</span></span>](../dns/create-dns-records-at-123-reg-co-uk.md) | [<span data-ttu-id="9a194-122">Géré par Google (eNom)</span><span class="sxs-lookup"><span data-stu-id="9a194-122">Managed   by Google (eNom)</span></span>](../dns/create-dns-records-for-domain-managed-by-google-enom.md)|
| [<span data-ttu-id="9a194-123">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="9a194-123">Amazon Web Services (AWS)</span></span>](../dns/create-dns-records-at-aws.md) | [<span data-ttu-id="9a194-124">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="9a194-124">MyDomain</span></span>](../dns/create-dns-records-at-mydomain.md) |
| [<span data-ttu-id="9a194-125">Zones DNS Azure</span><span class="sxs-lookup"><span data-stu-id="9a194-125">Azure DNS zones</span></span>](../dns/create-dns-records-for-azure-dns-zones.md) | [<span data-ttu-id="9a194-126">name.com</span><span class="sxs-lookup"><span data-stu-id="9a194-126">name.com</span></span>](../dns/create-dns-records-at-name-com.md) |
| [<span data-ttu-id="9a194-127">Bluehost</span><span class="sxs-lookup"><span data-stu-id="9a194-127">Bluehost</span></span>](../dns/create-dns-records-at-bluehost.md) | [<span data-ttu-id="9a194-128">Namecheap</span><span class="sxs-lookup"><span data-stu-id="9a194-128">Namecheap</span></span>](../dns/create-dns-records-at-namecheap.md)|
| [<span data-ttu-id="9a194-129">Cloudflare</span><span class="sxs-lookup"><span data-stu-id="9a194-129">Cloudflare</span></span>](../dns/create-dns-records-at-cloudflare.md)| [<span data-ttu-id="9a194-130">Names.co.uk</span><span class="sxs-lookup"><span data-stu-id="9a194-130">Names.co.uk</span></span>](../dns/create-dns-records-at-names-co-uk.md) |
|  [<span data-ttu-id="9a194-131">Crazy Domains</span><span class="sxs-lookup"><span data-stu-id="9a194-131">Crazy Domains</span></span>](../dns/create-dns-records-at-crazy-domains.md)| [<span data-ttu-id="9a194-132">NetRegistry</span><span class="sxs-lookup"><span data-stu-id="9a194-132">Netregistry</span></span>](../dns/create-dns-records-at-netregistry.md) |
|[<span data-ttu-id="9a194-133">DNSMadeEasy</span><span class="sxs-lookup"><span data-stu-id="9a194-133">DNSMadeEasy</span></span>](../dns/create-dns-records-at-dnsmadeeasy.md) | [<span data-ttu-id="9a194-134">Solutions réseau</span><span class="sxs-lookup"><span data-stu-id="9a194-134">Network   Solutions</span></span>](../dns/create-dns-records-at-network-solutions.md) |
|[<span data-ttu-id="9a194-135">Dreamhost</span><span class="sxs-lookup"><span data-stu-id="9a194-135">Dreamhost</span></span>](../dns/create-dns-records-at-dreamhost.md)  | [<span data-ttu-id="9a194-136">OVH</span><span class="sxs-lookup"><span data-stu-id="9a194-136">OVH</span></span>](../dns/create-dns-records-at-ovh.md) |
|  [<span data-ttu-id="9a194-137">Dyn.com</span><span class="sxs-lookup"><span data-stu-id="9a194-137">Dyn.com</span></span>](../dns/create-dns-records-at-dyn-com.md) | [<span data-ttu-id="9a194-138">Register.com</span><span class="sxs-lookup"><span data-stu-id="9a194-138">Register.com</span></span>](../dns/create-dns-records-at-register-com.md) |
| [<span data-ttu-id="9a194-139">Auprès enomcentral</span><span class="sxs-lookup"><span data-stu-id="9a194-139">eNomCentral</span></span>](../dns/create-dns-records-at-enomcentral.md)| [<span data-ttu-id="9a194-140">Register365 pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9a194-140">Register365 for Office 365</span></span>](../dns/create-dns-records-at-register365.md)  |
| [<span data-ttu-id="9a194-141">Freenom</span><span class="sxs-lookup"><span data-stu-id="9a194-141">Freenom</span></span>](../dns/create-dns-records-at-freenom.md) | [<span data-ttu-id="9a194-142">web.com</span><span class="sxs-lookup"><span data-stu-id="9a194-142"> web.com </span></span>](../dns/create-dns-records-at-web-com.md)|
|[<span data-ttu-id="9a194-143">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="9a194-143">GoDaddy</span></span>](../dns/create-dns-records-at-godaddy.md)|[<span data-ttu-id="9a194-144">DNS basé sur Windows</span><span class="sxs-lookup"><span data-stu-id="9a194-144"> Windows-based DNS</span></span>](../dns/create-dns-records-using-windows-based-dns.md)   |
| [<span data-ttu-id="9a194-145">Google Domains</span><span class="sxs-lookup"><span data-stu-id="9a194-145">Google Domains</span></span>](../dns/create-dns-records-at-google-domains.md) |[<span data-ttu-id="9a194-146">WiX</span><span class="sxs-lookup"><span data-stu-id="9a194-146">Wix</span></span>](../dns/create-dns-records-at-wix.md) |
|[<span data-ttu-id="9a194-147">Hostgator</span><span class="sxs-lookup"><span data-stu-id="9a194-147">Hostgator</span></span>](../dns/create-dns-records-at-hostgator.md)  | [<span data-ttu-id="9a194-148">Payant   Petite entreprise</span><span class="sxs-lookup"><span data-stu-id="9a194-148">Yahoo!   Small Business</span></span>](../dns/create-dns-records-at-yahoo-small-business.md)  |

[<span data-ttu-id="9a194-149">J’ai besoin d’instructions générales, car mon hôte de domaine ne figure pas sur cette liste.</span><span class="sxs-lookup"><span data-stu-id="9a194-149">I need general instructions, because my domain host isn't on this list. </span></span>](create-dns-records-at-any-dns-hosting-provider.md)
   
