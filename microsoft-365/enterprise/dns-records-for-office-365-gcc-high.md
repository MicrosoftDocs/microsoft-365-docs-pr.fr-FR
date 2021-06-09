---
title: Enregistrements DNS pour Office 365 GCC High
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
- OGA150
- OGC150
- OGD150
- MOE150
ms.assetid: ''
description: 'Résumé : Enregistrements DNS pour Office 365 Cloud de la communauté du secteur public élevé'
hideEdit: true
ms.openlocfilehash: 9edcda4616d50d05331db0e2d6c4d89967b02fdc
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689820"
---
# <a name="dns-records-for-office-365-gcc-high"></a><span data-ttu-id="4c991-103">Enregistrements DNS pour Office 365 GCC High</span><span class="sxs-lookup"><span data-stu-id="4c991-103">DNS records for Office 365 GCC High</span></span>

<span data-ttu-id="4c991-104">*Cet article s’applique aux Office 365 Cloud de la communauté du secteur public High et Microsoft 365 Cloud de la communauté du secteur public High*</span><span class="sxs-lookup"><span data-stu-id="4c991-104">*This article applies to Office 365 GCC High and Microsoft 365 GCC High*</span></span>

<span data-ttu-id="4c991-105">Dans le cadre de l’intégration à Office 365 Cloud de la communauté du secteur public High, vous devez ajouter vos domaines SMTP et SIP à votre client de services en ligne.</span><span class="sxs-lookup"><span data-stu-id="4c991-105">As part of onboarding to Office 365 GCC High, you will need to add your SMTP and SIP domains to your Online Services tenant.</span></span>  <span data-ttu-id="4c991-106">Pour ce faire, utilisez l'New-MsolDomain dans Azure AD PowerShell ou utilisez le portail [Azure Government pour](https://portal.azure.us) démarrer le processus d’ajout du domaine et prouver la propriété.</span><span class="sxs-lookup"><span data-stu-id="4c991-106">You’ll do this using the New-MsolDomain cmdlet in Azure AD PowerShell or use the [Azure Government Portal](https://portal.azure.us) to start the process of adding the domain and proving ownership.</span></span>

<span data-ttu-id="4c991-107">Une fois vos domaines ajoutés à votre client et validés, utilisez les instructions suivantes pour ajouter les enregistrements DNS appropriés pour les services ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4c991-107">Once you have your domains added to your tenant and validated, use the following guidance to add the appropriate DNS records for the services below.</span></span>  <span data-ttu-id="4c991-108">Vous devrez peut-être modifier le tableau ci-dessous pour répondre aux besoins de votre organisation en ce qui concerne le ou les enregistrement(s) MX entrant(s) et tous les enregistrement(s) de découverte automatique Exchange existant(s) que vous avez en place.</span><span class="sxs-lookup"><span data-stu-id="4c991-108">You may need to modify the below table to fit your organization’s needs with respect to the inbound MX record(s) and any existing Exchange Autodiscover record(s) you have in place.</span></span>  <span data-ttu-id="4c991-109">Nous vous recommandons vivement de coordonner ces enregistrements DNS avec votre équipe de messagerie afin d’éviter toute panne ou mauvaise remise des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="4c991-109">We strongly recommend coordinating these DNS records with your messaging team to avoid any outages or mis-delivery of email.</span></span>

## <a name="exchange-online"></a><span data-ttu-id="4c991-110">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="4c991-110">Exchange Online</span></span>

| <span data-ttu-id="4c991-111">Type (Type)</span><span class="sxs-lookup"><span data-stu-id="4c991-111">Type</span></span> | <span data-ttu-id="4c991-112">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="4c991-112">Priority</span></span> | <span data-ttu-id="4c991-113">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="4c991-113">Host name</span></span> | <span data-ttu-id="4c991-114">Pointe vers l’adresse ou la valeur</span><span class="sxs-lookup"><span data-stu-id="4c991-114">Points to address or value</span></span> | <span data-ttu-id="4c991-115">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="4c991-115">TTL</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="4c991-116">MX</span><span class="sxs-lookup"><span data-stu-id="4c991-116">MX</span></span> | <span data-ttu-id="4c991-117">0</span><span class="sxs-lookup"><span data-stu-id="4c991-117">0</span></span> | @ | <span data-ttu-id="4c991-118">*tenant*.mail.protection.office365.us (voir ci-dessous pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="4c991-118">*tenant*.mail.protection.office365.us (see below for additional details)</span></span> | <span data-ttu-id="4c991-119">1 Hour</span><span class="sxs-lookup"><span data-stu-id="4c991-119">1 Hour</span></span> |
| <span data-ttu-id="4c991-120">TXT</span><span class="sxs-lookup"><span data-stu-id="4c991-120">TXT</span></span> | - | @ | <span data-ttu-id="4c991-121">v=spf1 include:spf.protection.office365.us -all</span><span class="sxs-lookup"><span data-stu-id="4c991-121">v=spf1 include:spf.protection.office365.us -all</span></span> | <span data-ttu-id="4c991-122">1 heure</span><span class="sxs-lookup"><span data-stu-id="4c991-122">1 Hour</span></span> |
| <span data-ttu-id="4c991-123">CNAME</span><span class="sxs-lookup"><span data-stu-id="4c991-123">CNAME</span></span> | - | <span data-ttu-id="4c991-124">autodiscover</span><span class="sxs-lookup"><span data-stu-id="4c991-124">autodiscover</span></span> | <span data-ttu-id="4c991-125">autodiscover.office365.us</span><span class="sxs-lookup"><span data-stu-id="4c991-125">autodiscover.office365.us</span></span> | <span data-ttu-id="4c991-126">1 Hour</span><span class="sxs-lookup"><span data-stu-id="4c991-126">1 Hour</span></span> |

### <a name="exchange-autodiscover-record"></a><span data-ttu-id="4c991-127">Exchange Enregistrement de découverte automatique</span><span class="sxs-lookup"><span data-stu-id="4c991-127">Exchange Autodiscover record</span></span>

<span data-ttu-id="4c991-128">Si vous avez Exchange Server en local, nous vous recommandons de laisser votre enregistrement existant en place pendant la migration vers Exchange Online, puis de mettre à jour cet enregistrement une fois que vous avez terminé la migration.</span><span class="sxs-lookup"><span data-stu-id="4c991-128">If you have Exchange Server on-premises, we recommend leaving your existing record in place while you migrate to Exchange Online, and update that record once you have completed your migration.</span></span> 

### <a name="exchange-online-mx-record"></a><span data-ttu-id="4c991-129">Exchange Online Enregistrement MX</span><span class="sxs-lookup"><span data-stu-id="4c991-129">Exchange Online MX Record</span></span>

<span data-ttu-id="4c991-130">La valeur de l’enregistrement MX pour vos domaines acceptés suit un format  standard comme indiqué ci-dessus : *client*.mail.protection.office365.us, en remplaçant le client par la première partie du nom de votre client par défaut.</span><span class="sxs-lookup"><span data-stu-id="4c991-130">The MX record value for your accepted domains follows a standard format as noted above: *tenant*.mail.protection.office365.us, replacing *tenant* with the first part of your default tenant name.</span></span>

<span data-ttu-id="4c991-131">Par exemple, si le nom de votre client contoso.onmicrosoft.us, vous devez utiliser **contoso.mail.protection.office365.us** comme valeur pour votre enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="4c991-131">For example, if your tenant name is contoso.onmicrosoft.us, you’d use **contoso.mail.protection.office365.us** as the value for your MX record.</span></span>

## <a name="skype-for-business-online"></a><span data-ttu-id="4c991-132">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="4c991-132">Skype for Business Online</span></span>

### <a name="cname-records"></a><span data-ttu-id="4c991-133">Enregistrements CNAME</span><span class="sxs-lookup"><span data-stu-id="4c991-133">CNAME records</span></span>

| <span data-ttu-id="4c991-134">Type</span><span class="sxs-lookup"><span data-stu-id="4c991-134">Type</span></span> | <span data-ttu-id="4c991-135">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="4c991-135">Host name</span></span> | <span data-ttu-id="4c991-136">Pointe vers l’adresse ou la valeur</span><span class="sxs-lookup"><span data-stu-id="4c991-136">Points to address or value</span></span> | <span data-ttu-id="4c991-137">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="4c991-137">TTL</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="4c991-138">CNAME</span><span class="sxs-lookup"><span data-stu-id="4c991-138">CNAME</span></span> | <span data-ttu-id="4c991-139">sip</span><span class="sxs-lookup"><span data-stu-id="4c991-139">sip</span></span> | <span data-ttu-id="4c991-140">sipdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="4c991-140">sipdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="4c991-141">1 heure</span><span class="sxs-lookup"><span data-stu-id="4c991-141">1 Hour</span></span> |
| <span data-ttu-id="4c991-142">CNAME</span><span class="sxs-lookup"><span data-stu-id="4c991-142">CNAME</span></span> | <span data-ttu-id="4c991-143">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="4c991-143">lyncdiscover</span></span> | <span data-ttu-id="4c991-144">webdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="4c991-144">webdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="4c991-145">1 Hour</span><span class="sxs-lookup"><span data-stu-id="4c991-145">1 Hour</span></span> |

### <a name="srv-records"></a><span data-ttu-id="4c991-146">Enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="4c991-146">SRV records</span></span>

| <span data-ttu-id="4c991-147">Type</span><span class="sxs-lookup"><span data-stu-id="4c991-147">Type</span></span> | <span data-ttu-id="4c991-148">Service</span><span class="sxs-lookup"><span data-stu-id="4c991-148">Service</span></span> | <span data-ttu-id="4c991-149">Protocole</span><span class="sxs-lookup"><span data-stu-id="4c991-149">Protocol</span></span> | <span data-ttu-id="4c991-150">Port</span><span class="sxs-lookup"><span data-stu-id="4c991-150">Port</span></span> | <span data-ttu-id="4c991-151">Pondération</span><span class="sxs-lookup"><span data-stu-id="4c991-151">Weight</span></span> | <span data-ttu-id="4c991-152">Priorité</span><span class="sxs-lookup"><span data-stu-id="4c991-152">Priority</span></span> | <span data-ttu-id="4c991-153">Nom</span><span class="sxs-lookup"><span data-stu-id="4c991-153">Name</span></span> | <span data-ttu-id="4c991-154">Target</span><span class="sxs-lookup"><span data-stu-id="4c991-154">Target</span></span> | <span data-ttu-id="4c991-155">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="4c991-155">TTL</span></span> |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="4c991-156">SRV</span><span class="sxs-lookup"><span data-stu-id="4c991-156">SRV</span></span> | <span data-ttu-id="4c991-157">\_sip</span><span class="sxs-lookup"><span data-stu-id="4c991-157">\_sip</span></span> | <span data-ttu-id="4c991-158">\_tls</span><span class="sxs-lookup"><span data-stu-id="4c991-158">\_tls</span></span> | <span data-ttu-id="4c991-159">443</span><span class="sxs-lookup"><span data-stu-id="4c991-159">443</span></span> | <span data-ttu-id="4c991-160">1</span><span class="sxs-lookup"><span data-stu-id="4c991-160">1</span></span> | <span data-ttu-id="4c991-161">100</span><span class="sxs-lookup"><span data-stu-id="4c991-161">100</span></span> | @ | <span data-ttu-id="4c991-162">sipdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="4c991-162">sipdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="4c991-163">1 heure</span><span class="sxs-lookup"><span data-stu-id="4c991-163">1 Hour</span></span> |
| <span data-ttu-id="4c991-164">SRV</span><span class="sxs-lookup"><span data-stu-id="4c991-164">SRV</span></span> | <span data-ttu-id="4c991-165">\_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="4c991-165">\_sipfederationtls</span></span> | <span data-ttu-id="4c991-166">\_tcp</span><span class="sxs-lookup"><span data-stu-id="4c991-166">\_tcp</span></span> | <span data-ttu-id="4c991-167">5061</span><span class="sxs-lookup"><span data-stu-id="4c991-167">5061</span></span> | <span data-ttu-id="4c991-168">1</span><span class="sxs-lookup"><span data-stu-id="4c991-168">1</span></span> | <span data-ttu-id="4c991-169">100</span><span class="sxs-lookup"><span data-stu-id="4c991-169">100</span></span> | @ | <span data-ttu-id="4c991-170">sipfed.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="4c991-170">sipfed.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="4c991-171">1 Hour</span><span class="sxs-lookup"><span data-stu-id="4c991-171">1 Hour</span></span> |

## <a name="additional-dns-records"></a><span data-ttu-id="4c991-172">Enregistrements DNS supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4c991-172">Additional DNS records</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c991-173">Si vous avez un enregistrement *CNAME msoid* existant dans  votre zone DNS, vous devez supprimer l’enregistrement du DNS pour le moment.</span><span class="sxs-lookup"><span data-stu-id="4c991-173">If you have an existing *msoid* CNAME record in your DNS zone, you must **remove** the record from DNS at this time.</span></span>  <span data-ttu-id="4c991-174">L’enregistrement msoid est incompatible avec Microsoft 365 Entreprise Apps *(anciennement Office 365 ProPlus)* et empêche l’activation de réussir.</span><span class="sxs-lookup"><span data-stu-id="4c991-174">The msoid record is incompatible with Microsoft 365 Enterprise Apps *(formerly Office 365 ProPlus)* and will prevent activation from succeeding.</span></span>
