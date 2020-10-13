---
title: Parité entre Azure information protection pour Office 365 géré par 21Vianet et offres commerciales
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
manager: mnirkhe
audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
- GEU150
- GEA150
description: En savoir plus sur Azure information protection pour Office 365 géré par 21Vianet et sur la façon de le configurer pour les clients en Chine.
monikerRange: o365-21vianet
ms.openlocfilehash: ca30811e77f686b92b8cdd13d624182eb0d3039e
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48445578"
---
# <a name="parity-between-azure-information-protection-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="125e3-103">Parité entre Azure information protection pour Office 365 géré par 21Vianet et offres commerciales</span><span class="sxs-lookup"><span data-stu-id="125e3-103">Parity between Azure Information Protection for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="125e3-104">Alors que notre objectif est de fournir toutes les fonctionnalités et fonctionnalités commerciales pour les clients en Chine avec notre offre Azure information protection pour Office 365 gérée par 21Vianet, il existe des fonctionnalités manquantes que nous souhaitons mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="125e3-104">While our goal is to deliver all commercial features and functionality to customers in China with our Azure Information Protection for Office 365 operated by 21Vianet offer, there is some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="125e3-105">La liste suivante inclut les lacunes existantes entre Azure information protection pour Office 365 géré par 21Vianet et nos offres commerciales depuis le 1er juillet 2019 :</span><span class="sxs-lookup"><span data-stu-id="125e3-105">The following list includes the existing gaps between Azure Information Protection for Office 365 operated by 21Vianet and our commercial offerings as of July 2019:</span></span>

- <span data-ttu-id="125e3-106">La gestion des droits relatifs à l’information (IRM) est prise en charge uniquement pour les applications Microsoft 365 pour entreprise (Build 11731,10000 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="125e3-106">Information Rights Management (IRM) is supported only for Microsoft 365 Apps for enterprise (build 11731.10000 or higher).</span></span> <span data-ttu-id="125e3-107">Office 2010, Office 2013 et les autres versions d’Office 2016 ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="125e3-107">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="125e3-108">La migration à partir d’Active Directory Rights Management Services (AD RMS) vers Azure information protection n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="125e3-108">Migration from Active Directory Rights Management Services (AD RMS) to Azure Information Protection is currently not available.</span></span>
  
- <span data-ttu-id="125e3-109">Le partage des courriers électroniques protégés vers les utilisateurs dans le Cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="125e3-109">Sharing of protected emails to users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="125e3-110">Le partage de documents et de pièces jointes de courrier électronique à des utilisateurs dans le Cloud commercial n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="125e3-110">Sharing of documents and email attachments to users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="125e3-111">Cela inclut les utilisateurs d’Office 365 gérés par 21Vianet dans le Cloud commercial, les utilisateurs non-Office 365 gérés par 21Vianet dans le nuage commercial et les utilisateurs disposant d’une licence RMS pour personnes.</span><span class="sxs-lookup"><span data-stu-id="125e3-111">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="125e3-112">La gestion des droits relatifs à l’information avec SharePoint (sites et bibliothèques protégés par IRM) n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="125e3-112">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="125e3-113">Le connecteur Rights Management n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="125e3-113">The Rights Management Connector is currently not available.</span></span>
  
- <span data-ttu-id="125e3-114">L’extension de l’appareil mobile pour AD RMS n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="125e3-114">The Mobile Device Extension for AD RMS is currently not available.</span></span>

## <a name="configuring-azure-information-protection-for-customers-in-china"></a><span data-ttu-id="125e3-115">Configuration d’Azure information protection pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="125e3-115">Configuring Azure Information Protection for customers in China</span></span>

### <a name="enable-rights-management-for-the-tenant"></a><span data-ttu-id="125e3-116">Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="125e3-116">Enable Rights Management for the tenant</span></span>

<span data-ttu-id="125e3-117">Pour que le chiffrement fonctionne correctement, le RMS doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="125e3-117">For the encryption to work correctly, the RMS must be enabled for the tenant.</span></span>

- <span data-ttu-id="125e3-118">Vérifiez si le RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="125e3-118">Check if the RMS is enabled:</span></span>
  1. <span data-ttu-id="125e3-119">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="125e3-119">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="125e3-120">Si le module AIPService n’est pas installé, exécutez  `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="125e3-120">If the AIPService module is not installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="125e3-121">Importez le module à l’aide du `Import-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="125e3-121">Import the module using `Import-Module AipService`.</span></span>
  4. <span data-ttu-id="125e3-122">Connectez-vous au service à l’aide de  `Connect-AipService -environmentname azurechinacloud` .</span><span class="sxs-lookup"><span data-stu-id="125e3-122">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  5. <span data-ttu-id="125e3-123">Exécutez  `(Get-AipServiceConfiguration).FunctionalState`   et vérifiez si l’État est  `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="125e3-123">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

- <span data-ttu-id="125e3-124">Si l’état de fonctionnement est  `Disabled` , exécuter  `Enable-AipService` .</span><span class="sxs-lookup"><span data-stu-id="125e3-124">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="dns-configuration-for-encryption-windows"></a><span data-ttu-id="125e3-125">Configuration DNS pour le chiffrement (Windows)</span><span class="sxs-lookup"><span data-stu-id="125e3-125">DNS configuration for encryption (Windows)</span></span>

<span data-ttu-id="125e3-126">Pour que le chiffrement fonctionne correctement, les applications clientes Office doivent se connecter à l’instance chinoise du service et des données d’amorçage à partir de là.</span><span class="sxs-lookup"><span data-stu-id="125e3-126">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="125e3-127">Pour rediriger les applications clientes vers l’instance de service appropriée, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="125e3-127">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="125e3-128">Sans l’enregistrement DNS SRV, l’application cliente tente de se connecter à l’instance de cloud public par défaut et échoue.</span><span class="sxs-lookup"><span data-stu-id="125e3-128">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="125e3-129">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine appartenant au client (par exemple, `joe@contoso.cn` ) et non sur le `onmschina` nom d’utilisateur (par exemple, `joe@contoso.onmschina.cn` ).</span><span class="sxs-lookup"><span data-stu-id="125e3-129">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="125e3-130">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="125e3-130">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

- <span data-ttu-id="125e3-131">Obtenir l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="125e3-131">Get the RMS ID:</span></span>
  1. <span data-ttu-id="125e3-132">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="125e3-132">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="125e3-133">Si le module AIPService n’est pas installé, exécutez  `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="125e3-133">If the AIPService module is not installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="125e3-134">Connectez-vous au service à l’aide de  `Connect-AipService -environmentname azurechinacloud` .</span><span class="sxs-lookup"><span data-stu-id="125e3-134">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  4. <span data-ttu-id="125e3-135">Exécutez  `(Get-AipServiceConfiguration).RightsManagementServiceId`   pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="125e3-135">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

- <span data-ttu-id="125e3-136">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="125e3-136">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>
  - <span data-ttu-id="125e3-137">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="125e3-137">Service = `_rmsredir`</span></span>
  - <span data-ttu-id="125e3-138">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="125e3-138">Protocol = `_http`</span></span>
  - <span data-ttu-id="125e3-139">Nom = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="125e3-139">Name = `_tcp`</span></span>
  - <span data-ttu-id="125e3-140">Target =  `[GUID].rms.aadrm.cn`   (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="125e3-140">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
  - <span data-ttu-id="125e3-141">Priorité, poids, secondes, durée de vie = valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="125e3-141">Priority, Weight, Seconds, TTL = default values</span></span>

- <span data-ttu-id="125e3-142">Associez le domaine personnalisé au client dans le [portail Azure](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span><span class="sxs-lookup"><span data-stu-id="125e3-142">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="125e3-143">Cette opération ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après l’ajout de la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="125e3-143">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

- <span data-ttu-id="125e3-144">Connectez-vous au centre d’administration Microsoft 365 avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine (par exemple, `contoso.cn` ) pour la création de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="125e3-144">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="125e3-145">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="125e3-145">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="125e3-146">Une fois la vérification terminée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="125e3-146">Once verification is done, users can be created.</span></span>

### <a name="dns-configuration-for-encryption-mac-ios-android"></a><span data-ttu-id="125e3-147">Configuration DNS pour le chiffrement (Mac, iOS, Android)</span><span class="sxs-lookup"><span data-stu-id="125e3-147">DNS configuration for encryption (Mac, iOS, Android)</span></span>

- <span data-ttu-id="125e3-148">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="125e3-148">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>
  - <span data-ttu-id="125e3-149">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="125e3-149">Service = `_rmsdisco`</span></span>
  - <span data-ttu-id="125e3-150">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="125e3-150">Protocol = `_http`</span></span>
  - <span data-ttu-id="125e3-151">Nom = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="125e3-151">Name = `_tcp`</span></span>
  - <span data-ttu-id="125e3-152">Cible = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="125e3-152">Target = `api.aadrm.cn`</span></span>
  - <span data-ttu-id="125e3-153">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="125e3-153">Port = `80`</span></span>
  - <span data-ttu-id="125e3-154">Priorité, poids, secondes, durée de vie = valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="125e3-154">Priority, Weight, Seconds, TTL = default values</span></span>
