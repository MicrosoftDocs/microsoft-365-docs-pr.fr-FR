---
title: Configurer votre domaine (instructions spécifiques de l’hôte)
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- okr_smb
- AdminSurgePortfolio
search.appverid:
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: ae950c9e-e8d9-4108-b0cb-449156998580
description: Découvrez comment gérer vos propres enregistrements DNS ou laisser Microsoft gérer vos enregistrements DNS pour vous.
ms.openlocfilehash: a22968fdfcdb6be8ecfdc9dde351de034edce4b2
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48645298"
---
# <a name="set-up-your-domain-host-specific-instructions"></a><span data-ttu-id="9a3fc-103">Configurer votre domaine (instructions spécifiques de l’hôte)</span><span class="sxs-lookup"><span data-stu-id="9a3fc-103">Set up your domain (host-specific instructions)</span></span>

<span data-ttu-id="9a3fc-104">Pour commencer à utiliser un domaine personnalisé (contoso.com) avec Microsoft 365, vous devez vérifier votre domaine et configurer les enregistrements DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="9a3fc-104">To start using a custom domain (contoso.com) with Microsoft 365, you need to verify your domain and configure your domain's DNS records.</span></span> 
  
<span data-ttu-id="9a3fc-105">Vous pouvez ajouter et gérer des enregistrements DNS à l’aide des outils d’administration de votre hôte de domaine ou accorder à Microsoft le contrôle de vos enregistrements de domaine et nous allons les configurer pour vous.</span><span class="sxs-lookup"><span data-stu-id="9a3fc-105">You can add and manage DNS records using the administrative tools at your domain host, or give Microsoft control of your domain records and we'll set them up for you.</span></span>
  
<span data-ttu-id="9a3fc-106">Sélectionnez votre hôte de domaine ci-dessous pour obtenir les étapes exactes.</span><span class="sxs-lookup"><span data-stu-id="9a3fc-106">Select your domain host below for the exact steps.</span></span> <span data-ttu-id="9a3fc-107">Si vous n’êtes pas sûr de votre hôte, reportez-vous à [la rubrique Rechercher votre bureau d’enregistrement de domaines](find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="9a3fc-107">If you're not sure who your host is, see [Find your domain registrar](find-your-domain-registrar.md).</span></span>
  

## <a name="let-microsoft-365-manage-your-dns-records"></a><span data-ttu-id="9a3fc-108">Permettre à Microsoft 365 de gérer vos enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="9a3fc-108">Let Microsoft 365 manage your DNS records</span></span>

||
|---|---|
|[<span data-ttu-id="9a3fc-109">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="9a3fc-109">1&1 IONOS</span></span>](../dns/change-nameservers-at-1-1-internet.md) |
|[<span data-ttu-id="9a3fc-110">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="9a3fc-110">Amazon Web Services (AWS)</span></span>](../dns/change-nameservers-at-aws.md) |
 [<span data-ttu-id="9a3fc-111">Bluehost</span><span class="sxs-lookup"><span data-stu-id="9a3fc-111">Bluehost</span></span>](../dns/change-nameservers-at-bluehost.md)|
|[<span data-ttu-id="9a3fc-112">Google Domains</span><span class="sxs-lookup"><span data-stu-id="9a3fc-112">Google   Domains</span></span>](../dns/change-nameservers-at-google-domains.md) |
|[<span data-ttu-id="9a3fc-113">Hostgator   </span><span class="sxs-lookup"><span data-stu-id="9a3fc-113">Hostgator   </span></span>](../dns/change-nameservers-at-hostgator.md)  |  
|[<span data-ttu-id="9a3fc-114">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="9a3fc-114">MyDomain</span></span>](../dns/change-nameservers-at-mydomain.md) | 
|[<span data-ttu-id="9a3fc-115">Namecheap</span><span class="sxs-lookup"><span data-stu-id="9a3fc-115">Namecheap</span></span>](../dns/change-nameservers-at-namecheap.md)|
|[<span data-ttu-id="9a3fc-116">Network Solutions</span><span class="sxs-lookup"><span data-stu-id="9a3fc-116">Network Solutions</span></span>](../dns/change-nameservers-at-network-solutions.md) |  

<span data-ttu-id="9a3fc-117">Vous pouvez également apprendre à [modifier les serveurs de noms de manière à configurer Microsoft 365 avec n’importe quel bureau](change-nameservers-at-any-domain-registrar.md)d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="9a3fc-117">Or, learn how to [change nameservers to set up Microsoft 365 with any domain registrar](change-nameservers-at-any-domain-registrar.md).</span></span>

## <a name="manage-your-own-dns-records"></a><span data-ttu-id="9a3fc-118">Gérer vos propres enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="9a3fc-118">Manage your own DNS records</span></span>

|                           |                          |
|---------------------------|--------------------------|
| [<span data-ttu-id="9a3fc-119">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="9a3fc-119">1&1 IONOS</span></span>](../dns/create-dns-records-at-1-1-internet.md) | [<span data-ttu-id="9a3fc-120">Sensitiv</span><span class="sxs-lookup"><span data-stu-id="9a3fc-120">Hover</span></span>](../dns/create-dns-records-at-hover.md) |
| [<span data-ttu-id="9a3fc-121">123-reg.co.uk</span><span class="sxs-lookup"><span data-stu-id="9a3fc-121">123-reg.co.uk</span></span>](../dns/create-dns-records-at-123-reg-co-uk.md) | [<span data-ttu-id="9a3fc-122">Géré par Google (eNom)</span><span class="sxs-lookup"><span data-stu-id="9a3fc-122">Managed   by Google (eNom)</span></span>](../dns/create-dns-records-for-domain-managed-by-google-enom.md)|
| [<span data-ttu-id="9a3fc-123">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="9a3fc-123">Amazon Web Services (AWS)</span></span>](../dns/create-dns-records-at-aws.md) | [<span data-ttu-id="9a3fc-124">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="9a3fc-124">MyDomain</span></span>](../dns/create-dns-records-at-mydomain.md) |
| [<span data-ttu-id="9a3fc-125">Zones DNS Azure</span><span class="sxs-lookup"><span data-stu-id="9a3fc-125">Azure DNS zones</span></span>](../dns/create-dns-records-for-azure-dns-zones.md) | [<span data-ttu-id="9a3fc-126">name.com</span><span class="sxs-lookup"><span data-stu-id="9a3fc-126">name.com</span></span>](../dns/create-dns-records-at-name-com.md) |
| [<span data-ttu-id="9a3fc-127">Bluehost</span><span class="sxs-lookup"><span data-stu-id="9a3fc-127">Bluehost</span></span>](../dns/create-dns-records-at-bluehost.md) | [<span data-ttu-id="9a3fc-128">Namecheap</span><span class="sxs-lookup"><span data-stu-id="9a3fc-128">Namecheap</span></span>](../dns/create-dns-records-at-namecheap.md)|
| [<span data-ttu-id="9a3fc-129">Cloudflare</span><span class="sxs-lookup"><span data-stu-id="9a3fc-129">Cloudflare</span></span>](../dns/create-dns-records-at-cloudflare.md)| [<span data-ttu-id="9a3fc-130">Names.co.uk</span><span class="sxs-lookup"><span data-stu-id="9a3fc-130">Names.co.uk</span></span>](../dns/create-dns-records-at-names-co-uk.md) |
|  [<span data-ttu-id="9a3fc-131">Crazy Domains</span><span class="sxs-lookup"><span data-stu-id="9a3fc-131">Crazy Domains</span></span>](../dns/create-dns-records-at-crazy-domains.md)| [<span data-ttu-id="9a3fc-132">NetRegistry</span><span class="sxs-lookup"><span data-stu-id="9a3fc-132">Netregistry</span></span>](../dns/create-dns-records-at-netregistry.md) |
|[<span data-ttu-id="9a3fc-133">DNSMadeEasy</span><span class="sxs-lookup"><span data-stu-id="9a3fc-133">DNSMadeEasy</span></span>](../dns/create-dns-records-at-dnsmadeeasy.md) | [<span data-ttu-id="9a3fc-134">Solutions réseau</span><span class="sxs-lookup"><span data-stu-id="9a3fc-134">Network   Solutions</span></span>](../dns/create-dns-records-at-network-solutions.md) |
|[<span data-ttu-id="9a3fc-135">Dreamhost</span><span class="sxs-lookup"><span data-stu-id="9a3fc-135">Dreamhost</span></span>](../dns/create-dns-records-at-dreamhost.md)  | [<span data-ttu-id="9a3fc-136">OVH</span><span class="sxs-lookup"><span data-stu-id="9a3fc-136">OVH</span></span>](../dns/create-dns-records-at-ovh.md) |
|  [<span data-ttu-id="9a3fc-137">Dyn.com</span><span class="sxs-lookup"><span data-stu-id="9a3fc-137">Dyn.com</span></span>](../dns/create-dns-records-at-dyn-com.md) | [<span data-ttu-id="9a3fc-138">Register.com</span><span class="sxs-lookup"><span data-stu-id="9a3fc-138">Register.com</span></span>](../dns/create-dns-records-at-register-com.md) |
| [<span data-ttu-id="9a3fc-139">Auprès enomcentral</span><span class="sxs-lookup"><span data-stu-id="9a3fc-139">eNomCentral</span></span>](../dns/create-dns-records-at-enomcentral.md)| [<span data-ttu-id="9a3fc-140">Register365 pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9a3fc-140">Register365 for Microsoft 365</span></span>](../dns/create-dns-records-at-register365.md)  |
| [<span data-ttu-id="9a3fc-141">Freenom</span><span class="sxs-lookup"><span data-stu-id="9a3fc-141">Freenom</span></span>](../dns/create-dns-records-at-freenom.md) | [<span data-ttu-id="9a3fc-142"> web.com </span><span class="sxs-lookup"><span data-stu-id="9a3fc-142"> web.com </span></span>](../dns/create-dns-records-at-web-com.md)|
|[<span data-ttu-id="9a3fc-143">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="9a3fc-143">GoDaddy</span></span>](../dns/create-dns-records-at-godaddy.md)|[<span data-ttu-id="9a3fc-144"> DNS basé sur Windows</span><span class="sxs-lookup"><span data-stu-id="9a3fc-144"> Windows-based DNS</span></span>](../dns/create-dns-records-using-windows-based-dns.md)   |
| [<span data-ttu-id="9a3fc-145">Google Domains</span><span class="sxs-lookup"><span data-stu-id="9a3fc-145">Google Domains</span></span>](../dns/create-dns-records-at-google-domains.md) |[<span data-ttu-id="9a3fc-146">WiX</span><span class="sxs-lookup"><span data-stu-id="9a3fc-146">Wix</span></span>](../dns/create-dns-records-at-wix.md) |
|[<span data-ttu-id="9a3fc-147">Hostgator</span><span class="sxs-lookup"><span data-stu-id="9a3fc-147">Hostgator</span></span>](../dns/create-dns-records-at-hostgator.md)  | [<span data-ttu-id="9a3fc-148">Payant   Petite entreprise</span><span class="sxs-lookup"><span data-stu-id="9a3fc-148">Yahoo!   Small Business</span></span>](../dns/create-dns-records-at-yahoo-small-business.md)  |

[<span data-ttu-id="9a3fc-149">J’ai besoin d’instructions générales, car mon hôte de domaine ne figure pas sur cette liste. </span><span class="sxs-lookup"><span data-stu-id="9a3fc-149">I need general instructions, because my domain host isn't on this list. </span></span>](create-dns-records-at-any-dns-hosting-provider.md)
   
