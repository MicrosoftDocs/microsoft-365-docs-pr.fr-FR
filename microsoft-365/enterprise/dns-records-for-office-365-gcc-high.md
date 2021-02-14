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
description: 'Résumé : Enregistrements DNS pour Office 365 GCC High'
hideEdit: true
ms.openlocfilehash: 9edcda4616d50d05331db0e2d6c4d89967b02fdc
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689820"
---
# <a name="dns-records-for-office-365-gcc-high"></a><span data-ttu-id="94582-103">Enregistrements DNS pour Office 365 GCC High</span><span class="sxs-lookup"><span data-stu-id="94582-103">DNS records for Office 365 GCC High</span></span>

<span data-ttu-id="94582-104">*Cet article s’applique à Office 365 GCC High et Microsoft 365 GCC High*</span><span class="sxs-lookup"><span data-stu-id="94582-104">*This article applies to Office 365 GCC High and Microsoft 365 GCC High*</span></span>

<span data-ttu-id="94582-105">Dans le cadre de l’intégration à Office 365 GCC High, vous devez ajouter vos domaines SMTP et SIP à votre client de services en ligne.</span><span class="sxs-lookup"><span data-stu-id="94582-105">As part of onboarding to Office 365 GCC High, you will need to add your SMTP and SIP domains to your Online Services tenant.</span></span>  <span data-ttu-id="94582-106">Pour ce faire, utilisez l'New-MsolDomain dans Azure AD PowerShell ou utilisez le portail [Azure Government pour](https://portal.azure.us) démarrer le processus d’ajout du domaine et prouver la propriété.</span><span class="sxs-lookup"><span data-stu-id="94582-106">You’ll do this using the New-MsolDomain cmdlet in Azure AD PowerShell or use the [Azure Government Portal](https://portal.azure.us) to start the process of adding the domain and proving ownership.</span></span>

<span data-ttu-id="94582-107">Une fois vos domaines ajoutés à votre client et validés, utilisez les instructions suivantes pour ajouter les enregistrements DNS appropriés pour les services ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="94582-107">Once you have your domains added to your tenant and validated, use the following guidance to add the appropriate DNS records for the services below.</span></span>  <span data-ttu-id="94582-108">Vous devrez peut-être modifier le tableau ci-dessous pour répondre aux besoins de votre organisation en ce qui concerne le ou les enregistrement(s) MX entrant(s) et tous les enregistrement(s) de découverte automatique Exchange existant(s) que vous avez en place.</span><span class="sxs-lookup"><span data-stu-id="94582-108">You may need to modify the below table to fit your organization’s needs with respect to the inbound MX record(s) and any existing Exchange Autodiscover record(s) you have in place.</span></span>  <span data-ttu-id="94582-109">Nous vous recommandons vivement de coordonner ces enregistrements DNS avec votre équipe de messagerie afin d’éviter toute panne ou mauvaise remise du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="94582-109">We strongly recommend coordinating these DNS records with your messaging team to avoid any outages or mis-delivery of email.</span></span>

## <a name="exchange-online"></a><span data-ttu-id="94582-110">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="94582-110">Exchange Online</span></span>

| <span data-ttu-id="94582-111">Type (Type)</span><span class="sxs-lookup"><span data-stu-id="94582-111">Type</span></span> | <span data-ttu-id="94582-112">Priority (Priorité)</span><span class="sxs-lookup"><span data-stu-id="94582-112">Priority</span></span> | <span data-ttu-id="94582-113">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="94582-113">Host name</span></span> | <span data-ttu-id="94582-114">Pointe vers l’adresse ou la valeur</span><span class="sxs-lookup"><span data-stu-id="94582-114">Points to address or value</span></span> | <span data-ttu-id="94582-115">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="94582-115">TTL</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="94582-116">MX</span><span class="sxs-lookup"><span data-stu-id="94582-116">MX</span></span> | <span data-ttu-id="94582-117">0</span><span class="sxs-lookup"><span data-stu-id="94582-117">0</span></span> | @ | <span data-ttu-id="94582-118">*tenant*.mail.protection.office365.us (voir ci-dessous pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="94582-118">*tenant*.mail.protection.office365.us (see below for additional details)</span></span> | <span data-ttu-id="94582-119">1 Hour</span><span class="sxs-lookup"><span data-stu-id="94582-119">1 Hour</span></span> |
| <span data-ttu-id="94582-120">TXT</span><span class="sxs-lookup"><span data-stu-id="94582-120">TXT</span></span> | - | @ | <span data-ttu-id="94582-121">v=spf1 include:spf.protection.office365.us -all</span><span class="sxs-lookup"><span data-stu-id="94582-121">v=spf1 include:spf.protection.office365.us -all</span></span> | <span data-ttu-id="94582-122">1 heure</span><span class="sxs-lookup"><span data-stu-id="94582-122">1 Hour</span></span> |
| <span data-ttu-id="94582-123">CNAME</span><span class="sxs-lookup"><span data-stu-id="94582-123">CNAME</span></span> | - | <span data-ttu-id="94582-124">autodiscover</span><span class="sxs-lookup"><span data-stu-id="94582-124">autodiscover</span></span> | <span data-ttu-id="94582-125">autodiscover.office365.us</span><span class="sxs-lookup"><span data-stu-id="94582-125">autodiscover.office365.us</span></span> | <span data-ttu-id="94582-126">1 Hour</span><span class="sxs-lookup"><span data-stu-id="94582-126">1 Hour</span></span> |

### <a name="exchange-autodiscover-record"></a><span data-ttu-id="94582-127">Enregistrement de découverte automatique Exchange</span><span class="sxs-lookup"><span data-stu-id="94582-127">Exchange Autodiscover record</span></span>

<span data-ttu-id="94582-128">Si vous avez Exchange Server en local, nous vous recommandons de laisser votre enregistrement existant en place pendant la migration vers Exchange Online, puis de mettre à jour cet enregistrement une fois que vous avez terminé la migration.</span><span class="sxs-lookup"><span data-stu-id="94582-128">If you have Exchange Server on-premises, we recommend leaving your existing record in place while you migrate to Exchange Online, and update that record once you have completed your migration.</span></span> 

### <a name="exchange-online-mx-record"></a><span data-ttu-id="94582-129">Enregistrement MX Exchange Online</span><span class="sxs-lookup"><span data-stu-id="94582-129">Exchange Online MX Record</span></span>

<span data-ttu-id="94582-130">La valeur d’enregistrement MX pour vos domaines acceptés suit un format standard  comme indiqué ci-dessus : *client*.mail.protection.office365.us, en remplaçant le client par la première partie de votre nom de client par défaut.</span><span class="sxs-lookup"><span data-stu-id="94582-130">The MX record value for your accepted domains follows a standard format as noted above: *tenant*.mail.protection.office365.us, replacing *tenant* with the first part of your default tenant name.</span></span>

<span data-ttu-id="94582-131">Par exemple, si le nom de votre client contoso.onmicrosoft.us, vous devez utiliser **contoso.mail.protection.office365.us** comme valeur pour votre enregistrement MX.</span><span class="sxs-lookup"><span data-stu-id="94582-131">For example, if your tenant name is contoso.onmicrosoft.us, you’d use **contoso.mail.protection.office365.us** as the value for your MX record.</span></span>

## <a name="skype-for-business-online"></a><span data-ttu-id="94582-132">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="94582-132">Skype for Business Online</span></span>

### <a name="cname-records"></a><span data-ttu-id="94582-133">Enregistrements CNAME</span><span class="sxs-lookup"><span data-stu-id="94582-133">CNAME records</span></span>

| <span data-ttu-id="94582-134">Type</span><span class="sxs-lookup"><span data-stu-id="94582-134">Type</span></span> | <span data-ttu-id="94582-135">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="94582-135">Host name</span></span> | <span data-ttu-id="94582-136">Pointe vers l’adresse ou la valeur</span><span class="sxs-lookup"><span data-stu-id="94582-136">Points to address or value</span></span> | <span data-ttu-id="94582-137">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="94582-137">TTL</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="94582-138">CNAME</span><span class="sxs-lookup"><span data-stu-id="94582-138">CNAME</span></span> | <span data-ttu-id="94582-139">sip</span><span class="sxs-lookup"><span data-stu-id="94582-139">sip</span></span> | <span data-ttu-id="94582-140">sipdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="94582-140">sipdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="94582-141">1 heure</span><span class="sxs-lookup"><span data-stu-id="94582-141">1 Hour</span></span> |
| <span data-ttu-id="94582-142">CNAME</span><span class="sxs-lookup"><span data-stu-id="94582-142">CNAME</span></span> | <span data-ttu-id="94582-143">lyncdiscover</span><span class="sxs-lookup"><span data-stu-id="94582-143">lyncdiscover</span></span> | <span data-ttu-id="94582-144">webdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="94582-144">webdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="94582-145">1 Hour</span><span class="sxs-lookup"><span data-stu-id="94582-145">1 Hour</span></span> |

### <a name="srv-records"></a><span data-ttu-id="94582-146">Enregistrements SRV</span><span class="sxs-lookup"><span data-stu-id="94582-146">SRV records</span></span>

| <span data-ttu-id="94582-147">Type</span><span class="sxs-lookup"><span data-stu-id="94582-147">Type</span></span> | <span data-ttu-id="94582-148">Service</span><span class="sxs-lookup"><span data-stu-id="94582-148">Service</span></span> | <span data-ttu-id="94582-149">Protocole</span><span class="sxs-lookup"><span data-stu-id="94582-149">Protocol</span></span> | <span data-ttu-id="94582-150">Port</span><span class="sxs-lookup"><span data-stu-id="94582-150">Port</span></span> | <span data-ttu-id="94582-151">Pondération</span><span class="sxs-lookup"><span data-stu-id="94582-151">Weight</span></span> | <span data-ttu-id="94582-152">Priorité</span><span class="sxs-lookup"><span data-stu-id="94582-152">Priority</span></span> | <span data-ttu-id="94582-153">Nom</span><span class="sxs-lookup"><span data-stu-id="94582-153">Name</span></span> | <span data-ttu-id="94582-154">Target</span><span class="sxs-lookup"><span data-stu-id="94582-154">Target</span></span> | <span data-ttu-id="94582-155">Durée de vie</span><span class="sxs-lookup"><span data-stu-id="94582-155">TTL</span></span> |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="94582-156">SRV</span><span class="sxs-lookup"><span data-stu-id="94582-156">SRV</span></span> | <span data-ttu-id="94582-157">\_sip</span><span class="sxs-lookup"><span data-stu-id="94582-157">\_sip</span></span> | <span data-ttu-id="94582-158">\_tls</span><span class="sxs-lookup"><span data-stu-id="94582-158">\_tls</span></span> | <span data-ttu-id="94582-159">443</span><span class="sxs-lookup"><span data-stu-id="94582-159">443</span></span> | <span data-ttu-id="94582-160">1 </span><span class="sxs-lookup"><span data-stu-id="94582-160">1</span></span> | <span data-ttu-id="94582-161">100</span><span class="sxs-lookup"><span data-stu-id="94582-161">100</span></span> | @ | <span data-ttu-id="94582-162">sipdir.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="94582-162">sipdir.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="94582-163">1 heure</span><span class="sxs-lookup"><span data-stu-id="94582-163">1 Hour</span></span> |
| <span data-ttu-id="94582-164">SRV</span><span class="sxs-lookup"><span data-stu-id="94582-164">SRV</span></span> | <span data-ttu-id="94582-165">\_sipfederationtls</span><span class="sxs-lookup"><span data-stu-id="94582-165">\_sipfederationtls</span></span> | <span data-ttu-id="94582-166">\_tcp</span><span class="sxs-lookup"><span data-stu-id="94582-166">\_tcp</span></span> | <span data-ttu-id="94582-167">5061</span><span class="sxs-lookup"><span data-stu-id="94582-167">5061</span></span> | <span data-ttu-id="94582-168">1 </span><span class="sxs-lookup"><span data-stu-id="94582-168">1</span></span> | <span data-ttu-id="94582-169">100</span><span class="sxs-lookup"><span data-stu-id="94582-169">100</span></span> | @ | <span data-ttu-id="94582-170">sipfed.online.gov.skypeforbusiness.us</span><span class="sxs-lookup"><span data-stu-id="94582-170">sipfed.online.gov.skypeforbusiness.us</span></span> | <span data-ttu-id="94582-171">1 Hour</span><span class="sxs-lookup"><span data-stu-id="94582-171">1 Hour</span></span> |

## <a name="additional-dns-records"></a><span data-ttu-id="94582-172">Enregistrements DNS supplémentaires</span><span class="sxs-lookup"><span data-stu-id="94582-172">Additional DNS records</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94582-173">Si vous avez un enregistrement *CNAME msoid* existant dans  votre zone DNS, vous devez supprimer l’enregistrement du DNS pour le moment.</span><span class="sxs-lookup"><span data-stu-id="94582-173">If you have an existing *msoid* CNAME record in your DNS zone, you must **remove** the record from DNS at this time.</span></span>  <span data-ttu-id="94582-174">L’enregistrement msoid est incompatible avec Microsoft 365 Enterprise Apps *(anciennement Office 365 ProPlus)* et empêche l’activation de réussir.</span><span class="sxs-lookup"><span data-stu-id="94582-174">The msoid record is incompatible with Microsoft 365 Enterprise Apps *(formerly Office 365 ProPlus)* and will prevent activation from succeeding.</span></span>
