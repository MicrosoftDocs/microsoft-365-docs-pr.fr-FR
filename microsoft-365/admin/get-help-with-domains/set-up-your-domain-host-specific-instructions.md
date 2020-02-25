---
title: Configurer votre domaine (instructions spécifiques de l’hôte)
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
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
description: Découvrez comment gérer vos propres enregistrements DNS ou laisser Office 365 gérer vos enregistrements DNS pour vous.
ms.custom: okr_smb
ms.openlocfilehash: 2313aa6c629c76a852e38b4da9093576a3b75d6e
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42252916"
---
# <a name="set-up-your-domain-host-specific-instructions"></a><span data-ttu-id="bf0a2-103">Configurer votre domaine (instructions spécifiques de l’hôte)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-103">Set up your domain (host-specific instructions)</span></span>

<span data-ttu-id="bf0a2-104">Pour commencer à utiliser un domaine personnalisé (contoso.com) avec Office 365, vous devez vérifier votre domaine et configurer les enregistrements DNS de votre domaine.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-104">To start using a custom domain (contoso.com) with Office 365, you need to verify your domain and configure your domain's DNS records.</span></span> 
  
<span data-ttu-id="bf0a2-105">Vous pouvez ajouter et gérer des enregistrements DNS à l’aide des outils d’administration de votre hôte de domaine, ou le contrôle Office 365 de vos enregistrements de domaine et nous allons les configurer pour vous.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-105">You can add and manage DNS records using the administrative tools at your domain host, or give Office 365 control of your domain records and we'll set them up for you.</span></span>
  
<span data-ttu-id="bf0a2-106">Sélectionnez votre hôte de domaine ci-dessous pour obtenir les étapes exactes.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-106">Select your domain host below for the exact steps.</span></span> <span data-ttu-id="bf0a2-107">Si vous n’êtes pas sûr de votre hôte, reportez-vous à [la rubrique Rechercher votre bureau d’enregistrement de domaines](find-your-domain-registrar.md).</span><span class="sxs-lookup"><span data-stu-id="bf0a2-107">If you're not sure who your host is, see [Find your domain registrar](find-your-domain-registrar.md).</span></span>
  

## <a name="let-office-365-manage-your-dns-records"></a><span data-ttu-id="bf0a2-108">Permettre à Office 365 de gérer vos enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="bf0a2-108">Let Office 365 manage your DNS records</span></span>

||
|---|---|
|[<span data-ttu-id="bf0a2-109">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="bf0a2-109">1&1 IONOS</span></span>](../dns/change-nameservers-at-1-1-internet.md) |
|[<span data-ttu-id="bf0a2-110">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-110">Amazon Web Services (AWS)</span></span>](../dns/change-nameservers-at-aws.md) |
 [<span data-ttu-id="bf0a2-111">Bluehost</span><span class="sxs-lookup"><span data-stu-id="bf0a2-111">Bluehost</span></span>](../dns/change-nameservers-at-bluehost.md)|
|[<span data-ttu-id="bf0a2-112">Google Domains</span><span class="sxs-lookup"><span data-stu-id="bf0a2-112">Google   Domains</span></span>](../dns/change-nameservers-at-google-domains.md) |
|[<span data-ttu-id="bf0a2-113">Hostgator</span><span class="sxs-lookup"><span data-stu-id="bf0a2-113">Hostgator   </span></span>](../dns/change-nameservers-at-hostgator.md)  |  
|[<span data-ttu-id="bf0a2-114">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="bf0a2-114">MyDomain</span></span>](../dns/change-nameservers-at-mydomain.md) | 
|[<span data-ttu-id="bf0a2-115">Namecheap</span><span class="sxs-lookup"><span data-stu-id="bf0a2-115">Namecheap</span></span>](../dns/change-nameservers-at-namecheap.md)|
|[<span data-ttu-id="bf0a2-116">Network Solutions</span><span class="sxs-lookup"><span data-stu-id="bf0a2-116">Network Solutions</span></span>](../dns/change-nameservers-at-network-solutions.md) |  

<span data-ttu-id="bf0a2-117">Vous pouvez également apprendre à [modifier les serveurs de noms de manière à configurer Office 365 avec n’importe quel](change-nameservers-at-any-domain-registrar.md)Bureau d’enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-117">Or, learn how to [change nameservers to set up Office 365 with any domain registrar](change-nameservers-at-any-domain-registrar.md).</span></span>

## <a name="manage-your-own-dns-records"></a><span data-ttu-id="bf0a2-118">Gérer vos propres enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="bf0a2-118">Manage your own DNS records</span></span>

|                           |                          |
|---------------------------|--------------------------|
| [<span data-ttu-id="bf0a2-119">1&1 IONOS</span><span class="sxs-lookup"><span data-stu-id="bf0a2-119">1&1 IONOS</span></span>](../dns/create-dns-records-at-1-1-internet.md) | [<span data-ttu-id="bf0a2-120">Sensitiv</span><span class="sxs-lookup"><span data-stu-id="bf0a2-120">Hover</span></span>](../dns/create-dns-records-at-hover.md) |
| [<span data-ttu-id="bf0a2-121">123-reg.co.uk</span><span class="sxs-lookup"><span data-stu-id="bf0a2-121">123-reg.co.uk</span></span>](../dns/create-dns-records-at-123-reg-co-uk.md) | [<span data-ttu-id="bf0a2-122">Géré par Google (eNom)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-122">Managed   by Google (eNom)</span></span>](../dns/create-dns-records-for-domain-managed-by-google-enom.md)|
| [<span data-ttu-id="bf0a2-123">Amazon Web Services (AWS)</span><span class="sxs-lookup"><span data-stu-id="bf0a2-123">Amazon Web Services (AWS)</span></span>](../dns/create-dns-records-at-aws.md) | [<span data-ttu-id="bf0a2-124">Mon_domaine</span><span class="sxs-lookup"><span data-stu-id="bf0a2-124">MyDomain</span></span>](../dns/create-dns-records-at-mydomain.md) |
| [<span data-ttu-id="bf0a2-125">Zones DNS Azure</span><span class="sxs-lookup"><span data-stu-id="bf0a2-125">Azure DNS zones</span></span>](../dns/create-dns-records-for-azure-dns-zones.md) | [<span data-ttu-id="bf0a2-126">name.com</span><span class="sxs-lookup"><span data-stu-id="bf0a2-126">name.com</span></span>](../dns/create-dns-records-at-name-com.md) |
| [<span data-ttu-id="bf0a2-127">Bluehost</span><span class="sxs-lookup"><span data-stu-id="bf0a2-127">Bluehost</span></span>](../dns/create-dns-records-at-bluehost.md) | [<span data-ttu-id="bf0a2-128">Namecheap</span><span class="sxs-lookup"><span data-stu-id="bf0a2-128">Namecheap</span></span>](../dns/create-dns-records-at-namecheap.md)|
| [<span data-ttu-id="bf0a2-129">Cloudflare</span><span class="sxs-lookup"><span data-stu-id="bf0a2-129">Cloudflare</span></span>](../dns/create-dns-records-at-cloudflare.md)| [<span data-ttu-id="bf0a2-130">Names.co.uk</span><span class="sxs-lookup"><span data-stu-id="bf0a2-130">Names.co.uk</span></span>](../dns/create-dns-records-at-names-co-uk.md) |
|  [<span data-ttu-id="bf0a2-131">Crazy Domains</span><span class="sxs-lookup"><span data-stu-id="bf0a2-131">Crazy Domains</span></span>](../dns/create-dns-records-at-crazy-domains.md)| [<span data-ttu-id="bf0a2-132">NetRegistry</span><span class="sxs-lookup"><span data-stu-id="bf0a2-132">Netregistry</span></span>](../dns/create-dns-records-at-netregistry.md) |
|[<span data-ttu-id="bf0a2-133">DNSMadeEasy</span><span class="sxs-lookup"><span data-stu-id="bf0a2-133">DNSMadeEasy</span></span>](../dns/create-dns-records-at-dnsmadeeasy.md) | [<span data-ttu-id="bf0a2-134">Solutions réseau</span><span class="sxs-lookup"><span data-stu-id="bf0a2-134">Network   Solutions</span></span>](../dns/create-dns-records-at-network-solutions.md) |
|[<span data-ttu-id="bf0a2-135">Dreamhost</span><span class="sxs-lookup"><span data-stu-id="bf0a2-135">Dreamhost</span></span>](../dns/create-dns-records-at-dreamhost.md)  | [<span data-ttu-id="bf0a2-136">OVH</span><span class="sxs-lookup"><span data-stu-id="bf0a2-136">OVH</span></span>](../dns/create-dns-records-at-ovh.md) |
|  [<span data-ttu-id="bf0a2-137">Dyn.com</span><span class="sxs-lookup"><span data-stu-id="bf0a2-137">Dyn.com</span></span>](../dns/create-dns-records-at-dyn-com.md) | [<span data-ttu-id="bf0a2-138">Register.com</span><span class="sxs-lookup"><span data-stu-id="bf0a2-138">Register.com</span></span>](../dns/create-dns-records-at-register-com.md) |
| [<span data-ttu-id="bf0a2-139">Auprès enomcentral</span><span class="sxs-lookup"><span data-stu-id="bf0a2-139">eNomCentral</span></span>](../dns/create-dns-records-at-enomcentral.md)| [<span data-ttu-id="bf0a2-140">Register365 pour Office 365</span><span class="sxs-lookup"><span data-stu-id="bf0a2-140">Register365 for Office 365</span></span>](../dns/create-dns-records-at-register365.md)  |
| [<span data-ttu-id="bf0a2-141">Freenom</span><span class="sxs-lookup"><span data-stu-id="bf0a2-141">Freenom</span></span>](../dns/create-dns-records-at-freenom.md) | [<span data-ttu-id="bf0a2-142">web.com</span><span class="sxs-lookup"><span data-stu-id="bf0a2-142"> web.com </span></span>](../dns/create-dns-records-at-web-com.md)|
|[<span data-ttu-id="bf0a2-143">GoDaddy</span><span class="sxs-lookup"><span data-stu-id="bf0a2-143">GoDaddy</span></span>](../dns/create-dns-records-at-godaddy.md)|[<span data-ttu-id="bf0a2-144">DNS basé sur Windows</span><span class="sxs-lookup"><span data-stu-id="bf0a2-144"> Windows-based DNS</span></span>](../dns/create-dns-records-using-windows-based-dns.md)   |
| [<span data-ttu-id="bf0a2-145">Google Domains</span><span class="sxs-lookup"><span data-stu-id="bf0a2-145">Google Domains</span></span>](../dns/create-dns-records-at-google-domains.md) |[<span data-ttu-id="bf0a2-146">WiX</span><span class="sxs-lookup"><span data-stu-id="bf0a2-146">Wix</span></span>](../dns/create-dns-records-at-wix.md) |
|[<span data-ttu-id="bf0a2-147">Hostgator</span><span class="sxs-lookup"><span data-stu-id="bf0a2-147">Hostgator</span></span>](../dns/create-dns-records-at-hostgator.md)  | [<span data-ttu-id="bf0a2-148">Payant   Petite entreprise</span><span class="sxs-lookup"><span data-stu-id="bf0a2-148">Yahoo!   Small Business</span></span>](../dns/create-dns-records-at-yahoo-small-business.md)  |

[<span data-ttu-id="bf0a2-149">J’ai besoin d’instructions générales, car mon hôte de domaine ne figure pas sur cette liste.</span><span class="sxs-lookup"><span data-stu-id="bf0a2-149">I need general instructions, because my domain host isn't on this list. </span></span>](create-dns-records-at-any-dns-hosting-provider.md)
   