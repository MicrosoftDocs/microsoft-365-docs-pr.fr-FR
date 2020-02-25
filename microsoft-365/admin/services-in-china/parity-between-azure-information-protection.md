---
title: Office 365 géré 21Vianet
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
search.appverid:
- MET150
- GEU150
- GEA150
description: En savoir plus sur Azure information protection pour Office 365 géré par 21Vianet et sur la façon de le configurer pour les clients en Chine.
monikerRange: o365-21vianet
ms.openlocfilehash: a4eb8c3370a123b939fdccc53eec3905f79ee806
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42243997"
---
# <a name="parity-between-azure-information-protection-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="60660-103">Parité entre Azure information protection pour Office 365 géré par 21Vianet et offres commerciales</span><span class="sxs-lookup"><span data-stu-id="60660-103">Parity between Azure Information Protection for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="60660-104">Alors que notre objectif est de fournir toutes les fonctionnalités et fonctionnalités commerciales pour les clients en Chine avec notre offre Azure information protection pour Office 365 gérée par 21Vianet, il existe des fonctionnalités manquantes que nous souhaitons mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="60660-104">While our goal is to deliver all commercial features and functionality to customers in China with our Azure Information Protection for Office 365 operated by 21Vianet offer, there is some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="60660-105">Voici les lacunes existant entre les services Azure information protection pour Office 365 géré par 21Vianet et nos offres commerciales à partir du 2019 juillet :</span><span class="sxs-lookup"><span data-stu-id="60660-105">These are the existing gaps between Azure Information Protection for Office 365 operated by 21Vianet and our commercial offerings as of July 2019:</span></span>

- <span data-ttu-id="60660-106">La gestion des droits relatifs à l’information (IRM) est prise en charge uniquement pour Office 365 ProPlus (Build 11731,10000 ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="60660-106">Information Rights Management (IRM) is supported only for Office 365 ProPlus (build 11731.10000 or higher).</span></span> <span data-ttu-id="60660-107">Office 2010, Office 2013 et les autres versions d’Office 2016 ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="60660-107">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="60660-108">La migration à partir d’Active Directory Rights Management Services (AD RMS) vers Azure information protection n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="60660-108">Migration from Active Directory Rights Management Services (AD RMS) to Azure Information Protection is currently not available.</span></span>
  
- <span data-ttu-id="60660-109">Le partage des courriers électroniques protégés vers les utilisateurs dans le Cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="60660-109">Sharing of protected emails to users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="60660-110">Le partage de documents et de pièces jointes de courrier électronique à des utilisateurs dans le Cloud commercial n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="60660-110">Sharing of documents and email attachments to users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="60660-111">Cela inclut les utilisateurs d’Office 365 gérés par 21Vianet dans le Cloud commercial, les utilisateurs non-Office 365 gérés par 21Vianet dans le nuage commercial et les utilisateurs disposant d’une licence RMS pour personnes.</span><span class="sxs-lookup"><span data-stu-id="60660-111">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="60660-112">La gestion des droits relatifs à l’information avec SharePoint (sites et bibliothèques protégés par IRM) n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="60660-112">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="60660-113">Le connecteur Rights Management n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="60660-113">The Rights Management Connector is currently not available.</span></span>
  
- <span data-ttu-id="60660-114">L’extension de l’appareil mobile pour AD RMS n’est pas disponible actuellement.</span><span class="sxs-lookup"><span data-stu-id="60660-114">The Mobile Device Extension for AD RMS is currently not available.</span></span>

## <a name="configuring-azure-information-protection-for-customers-in-china"></a><span data-ttu-id="60660-115">Configuration d’Azure information protection pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="60660-115">Configuring Azure Information Protection for customers in China</span></span>

### <a name="enable-rights-management-for-the-tenant"></a><span data-ttu-id="60660-116">Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="60660-116">Enable Rights Management for the tenant</span></span>

<span data-ttu-id="60660-117">Pour que le chiffrement fonctionne correctement, le RMS doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="60660-117">For the encryption to work correctly, the RMS must be enabled for the tenant.</span></span>

- <span data-ttu-id="60660-118">Vérifiez si le RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="60660-118">Check if the RMS is enabled:</span></span>
  1. <span data-ttu-id="60660-119">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="60660-119">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="60660-120">Si le module AIPService n’est pas installé, `Install-Module AipService`exécutez.</span><span class="sxs-lookup"><span data-stu-id="60660-120">If the AIPService module is not installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="60660-121">Importez le `Import-Module AipService`module à l’aide du.</span><span class="sxs-lookup"><span data-stu-id="60660-121">Import the module using `Import-Module AipService`.</span></span>
  4. <span data-ttu-id="60660-122">Connectez-vous au service `Connect-AipService -environmentname azurechinacloud`à l’aide de.</span><span class="sxs-lookup"><span data-stu-id="60660-122">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  5. <span data-ttu-id="60660-123">Exécutez `(Get-AipServiceConfiguration).FunctionalState` et vérifiez si l’État est `Enabled`.</span><span class="sxs-lookup"><span data-stu-id="60660-123">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

- <span data-ttu-id="60660-124">Si l’état de fonctionnement `Disabled`est, `Enable-AipService`exécuter.</span><span class="sxs-lookup"><span data-stu-id="60660-124">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="dns-configuration-for-encryption-windows"></a><span data-ttu-id="60660-125">Configuration DNS pour le chiffrement (Windows)</span><span class="sxs-lookup"><span data-stu-id="60660-125">DNS configuration for encryption (Windows)</span></span>

<span data-ttu-id="60660-126">Pour que le chiffrement fonctionne correctement, les applications clientes Office doivent se connecter à l’instance chinoise du service et des données d’amorçage à partir de là.</span><span class="sxs-lookup"><span data-stu-id="60660-126">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="60660-127">Pour rediriger les applications clientes vers l’instance de service appropriée, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="60660-127">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="60660-128">Sans l’enregistrement DNS SRV, l’application cliente tente de se connecter à l’instance de cloud public par défaut et échoue.</span><span class="sxs-lookup"><span data-stu-id="60660-128">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="60660-129">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine appartenant au client `joe@contoso.cn`(par exemple,) `onmschina` et non sur le nom `joe@contoso.onmschina.cn`d’utilisateur (par exemple,).</span><span class="sxs-lookup"><span data-stu-id="60660-129">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="60660-130">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="60660-130">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

- <span data-ttu-id="60660-131">Obtenir l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="60660-131">Get the RMS ID:</span></span>
  1. <span data-ttu-id="60660-132">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="60660-132">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="60660-133">Si le module AIPService n’est pas installé, `Install-Module AipService`exécutez.</span><span class="sxs-lookup"><span data-stu-id="60660-133">If the AIPService module is not installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="60660-134">Connectez-vous au service `Connect-AipService -environmentname azurechinacloud`à l’aide de.</span><span class="sxs-lookup"><span data-stu-id="60660-134">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  4. <span data-ttu-id="60660-135">Exécutez `(Get-AipServiceConfiguration).RightsManagementServiceId` pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="60660-135">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

- <span data-ttu-id="60660-136">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="60660-136">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>
  - <span data-ttu-id="60660-137">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="60660-137">Service = `_rmsredir`</span></span>
  - <span data-ttu-id="60660-138">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="60660-138">Protocol = `_http`</span></span>
  - <span data-ttu-id="60660-139">Nom = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="60660-139">Name = `_tcp`</span></span>
  - <span data-ttu-id="60660-140">Target = `[GUID].rms.aadrm.cn` (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="60660-140">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
  - <span data-ttu-id="60660-141">Priorité, poids, secondes, durée de vie = valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="60660-141">Priority, Weight, Seconds, TTL = default values</span></span>

- <span data-ttu-id="60660-142">Associez le domaine personnalisé au client dans le [portail Azure](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span><span class="sxs-lookup"><span data-stu-id="60660-142">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="60660-143">Cette opération ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après l’ajout de la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="60660-143">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

- <span data-ttu-id="60660-144">Connectez-vous au centre d’administration Microsoft 365 avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine `contoso.cn`(par exemple,) pour la création de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="60660-144">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="60660-145">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="60660-145">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="60660-146">Une fois la vérification terminée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="60660-146">Once verification is done, users can be created.</span></span>

### <a name="dns-configuration-for-encryption-mac-ios-android"></a><span data-ttu-id="60660-147">Configuration DNS pour le chiffrement (Mac, iOS, Android)</span><span class="sxs-lookup"><span data-stu-id="60660-147">DNS configuration for encryption (Mac, iOS, Android)</span></span>

- <span data-ttu-id="60660-148">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="60660-148">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>
  - <span data-ttu-id="60660-149">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="60660-149">Service = `_rmsdisco`</span></span>
  - <span data-ttu-id="60660-150">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="60660-150">Protocol = `_http`</span></span>
  - <span data-ttu-id="60660-151">Nom = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="60660-151">Name = `_tcp`</span></span>
  - <span data-ttu-id="60660-152">Cible = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="60660-152">Target = `api.aadrm.cn`</span></span>
  - <span data-ttu-id="60660-153">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="60660-153">Port = `80`</span></span>
  - <span data-ttu-id="60660-154">Priorité, poids, secondes, durée de vie = valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="60660-154">Priority, Weight, Seconds, TTL = default values</span></span>
