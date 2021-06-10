---
title: Prise en charge d’Azure Information Protection pour Office 365 géré par 21Vianet
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
manager: scotv
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
description: En savoir plus sur Azure Information Protection (AIP) pour Office 365 géré par 21Vianet et comment le configurer pour les clients en Chine.
monikerRange: o365-21vianet
ms.openlocfilehash: 8b85ae43df31bb1947b841d616cc83c3a0b614e4
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52535841"
---
# <a name="azure-information-protection-support-for-office-365-operated-by-21vianet"></a><span data-ttu-id="f4807-103">Prise en charge d’Azure Information Protection pour Office 365 géré par 21Vianet</span><span class="sxs-lookup"><span data-stu-id="f4807-103">Azure Information Protection support for Office 365 operated by 21Vianet</span></span>

<span data-ttu-id="f4807-104">Cet article décrit les différences entre la prise en charge d’Azure Information Protection (AIP) pour Office 365 géré par 21Vianet et les offres commerciales, ainsi que des instructions spécifiques pour la configuration d’AIP pour les clients en Chine, y compris la façon d’installer le scanneur AIP local et de gérer les travaux d’analyse de &mdash; contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-104">This article covers the differences between Azure Information Protection (AIP) support for Office 365 operated by 21Vianet and commercial offerings, as well as specific instructions for configuring AIP for customers in China&mdash;including how to install the AIP on-premises scanner and manage content scan jobs.</span></span>

## <a name="differences-between-aip-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="f4807-105">Différences entre AIP pour les Office 365 gérés par 21Vianet et les offres commerciales</span><span class="sxs-lookup"><span data-stu-id="f4807-105">Differences between AIP for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="f4807-106">Bien que notre objectif soit de fournir toutes les fonctionnalités commerciales aux clients en Chine avec notre AIP pour Office 365 géré par l’offre 21Vianet, il existe certaines fonctionnalités manquantes que nous voulons mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="f4807-106">While our goal is to deliver all commercial features and functionality to customers in China with our AIP for Office 365 operated by 21Vianet offer, there's some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="f4807-107">La liste suivante inclut les lacunes existantes entre AIP pour Office 365 géré par 21Vianet et nos offres commerciales depuis janvier 2021 :</span><span class="sxs-lookup"><span data-stu-id="f4807-107">The following list includes the existing gaps between AIP for Office 365 operated by 21Vianet and our commercial offerings as of January 2021:</span></span>

- <span data-ttu-id="f4807-108">La gestion des droits de l’information (IRM) est prise en charge uniquement pour Applications Microsoft 365 pour les grandes entreprises (build 11731.10000 ou supérieure).</span><span class="sxs-lookup"><span data-stu-id="f4807-108">Information Rights Management (IRM) is supported only for Microsoft 365 Apps for enterprise (build 11731.10000 or higher).</span></span> <span data-ttu-id="f4807-109">Office 2010, Office 2013 et les autres versions Office 2016 ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f4807-109">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="f4807-110">La migration de services AD RMS (Active Directory Rights Management Services) (AD RMS) vers AIP n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f4807-110">Migration from Active Directory Rights Management Services (AD RMS) to AIP is currently not available.</span></span>
  
- <span data-ttu-id="f4807-111">Le partage de messages électroniques protégés avec des utilisateurs dans le cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f4807-111">Sharing of protected emails with users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="f4807-112">Le partage de documents et de pièces jointes de courrier électronique avec des utilisateurs dans le cloud commercial n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f4807-112">Sharing of documents and email attachments with users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="f4807-113">Cela inclut les Office 365 gérés par les utilisateurs de 21Vianet dans le cloud commercial, les Office 365 non gérés par les utilisateurs 21Vianet dans le cloud commercial et les utilisateurs titulaires d’une licence RMS pour les particuliers.</span><span class="sxs-lookup"><span data-stu-id="f4807-113">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="f4807-114">La gestion des droits SharePoint (sites et bibliothèques protégés par IRM) n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f4807-114">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="f4807-115">L’extension d’appareil mobile pour AD RMS n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f4807-115">The Mobile Device Extension for AD RMS is currently not available.</span></span>

- <span data-ttu-id="f4807-116">La [visionneuse mobile n’est](/azure/information-protection/rms-client/mobile-app-faq) pas prise en charge par Azure China 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="f4807-116">The [Mobile Viewer](/azure/information-protection/rms-client/mobile-app-faq) is not supported by Azure China 21Vianet.</span></span>

- <span data-ttu-id="f4807-117">La zone AIP du portail Azure n’est pas disponible pour les clients en Chine.</span><span class="sxs-lookup"><span data-stu-id="f4807-117">The AIP area of the Azure portal is unavailable to customers in China.</span></span> <span data-ttu-id="f4807-118">Utilisez [les commandes PowerShell au](#step-6-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs) lieu d’effectuer des actions dans le portail, telles que la gestion et l’exécution de vos travaux d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-118">Use [PowerShell commands](#step-6-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs) instead of performing actions in the portal, such as managing and running your content scan jobs.</span></span>

## <a name="configure-aip-for-customers-in-china"></a><span data-ttu-id="f4807-119">Configurer AIP pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="f4807-119">Configure AIP for customers in China</span></span>

<span data-ttu-id="f4807-120">Pour configurer AIP pour les clients en Chine :</span><span class="sxs-lookup"><span data-stu-id="f4807-120">To configure AIP for customers in China:</span></span>
1. <span data-ttu-id="f4807-121">[Activez la gestion des droits pour le client.](#step-1-enable-rights-management-for-the-tenant)</span><span class="sxs-lookup"><span data-stu-id="f4807-121">[Enable Rights Management for the tenant](#step-1-enable-rights-management-for-the-tenant).</span></span>

1. <span data-ttu-id="f4807-122">[Ajoutez le](#step-2-add-the-microsoft-information-protection-sync-service-service-principal)principal du service de synchronisation microsoft Information Protection .</span><span class="sxs-lookup"><span data-stu-id="f4807-122">[Add the Microsoft Information Protection Sync Service service principal](#step-2-add-the-microsoft-information-protection-sync-service-service-principal).</span></span>

1. <span data-ttu-id="f4807-123">[Configurer le chiffrement DNS.](#step-3-configure-dns-encryption)</span><span class="sxs-lookup"><span data-stu-id="f4807-123">[Configure DNS encryption](#step-3-configure-dns-encryption).</span></span>

1. <span data-ttu-id="f4807-124">[Installez et configurez le client d’étiquetage unifié AIP.](#step-4-install-and-configure-the-aip-unified-labeling-client)</span><span class="sxs-lookup"><span data-stu-id="f4807-124">[Install and configure the AIP unified labeling client](#step-4-install-and-configure-the-aip-unified-labeling-client).</span></span>

1. <span data-ttu-id="f4807-125">[Configurer les applications AIP sur Windows](#step-5-configure-aip-apps-on-windows).</span><span class="sxs-lookup"><span data-stu-id="f4807-125">[Configure AIP apps on Windows](#step-5-configure-aip-apps-on-windows).</span></span>

1. <span data-ttu-id="f4807-126">[Installez le scanneur AIP local](#step-6-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs)et gérez les travaux d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-126">[Install the AIP on-premises scanner and manage content scan jobs](#step-6-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs).</span></span> 

### <a name="step-1-enable-rights-management-for-the-tenant"></a><span data-ttu-id="f4807-127">Étape 1 : Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="f4807-127">Step 1: Enable Rights Management for the tenant</span></span>

<span data-ttu-id="f4807-128">Pour que le chiffrement fonctionne correctement, RMS doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="f4807-128">For the encryption to work correctly, RMS must be enabled for the tenant.</span></span>

1. <span data-ttu-id="f4807-129">Vérifiez si RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="f4807-129">Check if RMS is enabled:</span></span>

    1. <span data-ttu-id="f4807-130">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f4807-130">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="f4807-131">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="f4807-131">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="f4807-132">Importer le module à l’aide `Import-Module AipService` de .</span><span class="sxs-lookup"><span data-stu-id="f4807-132">Import the module using `Import-Module AipService`.</span></span>
    4. <span data-ttu-id="f4807-133">Connecter service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="f4807-133">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    5. <span data-ttu-id="f4807-134">Exécutez `(Get-AipServiceConfiguration).FunctionalState` et vérifiez si l’état `Enabled` est .</span><span class="sxs-lookup"><span data-stu-id="f4807-134">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

2. <span data-ttu-id="f4807-135">Si l’état fonctionnel est `Disabled` , exécutez `Enable-AipService` .</span><span class="sxs-lookup"><span data-stu-id="f4807-135">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="step-2-add-the-microsoft-information-protection-sync-service-service-principal"></a><span data-ttu-id="f4807-136">Étape 2 : Ajouter le principal du service de synchronisation du service de protection des informations Microsoft</span><span class="sxs-lookup"><span data-stu-id="f4807-136">Step 2: Add the Microsoft Information Protection Sync Service service principal</span></span>

<span data-ttu-id="f4807-137">Le principal de service de synchronisation Microsoft **Information Protection** n’est pas disponible dans les clients Azure Chine par défaut et est requis pour Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="f4807-137">The **Microsoft Information Protection Sync Service** service principal is not available in Azure China tenants by default, and is required for Azure Information Protection.</span></span>

1. <span data-ttu-id="f4807-138">Créez ce principal de service manuellement à l’aide de l’cmdlet [New-AzADServicePrincipal](/powershell/module/az.resources/new-azadserviceprincipal) et de l’ID d’application pour le service de synchronisation `870c4f2e-85b6-4d43-bdda-6ed9a579b725` Microsoft Information Protection.</span><span class="sxs-lookup"><span data-stu-id="f4807-138">Create this service principal manually using the [New-AzADServicePrincipal](/powershell/module/az.resources/new-azadserviceprincipal) cmdlet and the `870c4f2e-85b6-4d43-bdda-6ed9a579b725` application ID for the Microsoft Information Protection Sync Service.</span></span> 

    ```powershell 
    New-AzADServicePrincipal -ApplicationId 870c4f2e-85b6-4d43-bdda-6ed9a579b725
    ```

1. <span data-ttu-id="f4807-139">Après avoir ajouté le principal de service, ajoutez les autorisations pertinentes requises pour le service.</span><span class="sxs-lookup"><span data-stu-id="f4807-139">After adding the service principal, add the relevant permissions required to the service.</span></span>

### <a name="step-3-configure-dns-encryption"></a><span data-ttu-id="f4807-140">Étape 3 : Configurer le chiffrement DNS</span><span class="sxs-lookup"><span data-stu-id="f4807-140">Step 3: Configure DNS encryption</span></span>

<span data-ttu-id="f4807-141">Pour que le chiffrement fonctionne correctement, Office applications clientes doivent se connecter à l’instance chine du service et s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="f4807-141">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="f4807-142">Pour rediriger les applications clientes vers l’instance de service de droite, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="f4807-142">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="f4807-143">Sans l’enregistrement SRV DNS, l’application cliente tentera par défaut de se connecter à l’instance de cloud public et échouera.</span><span class="sxs-lookup"><span data-stu-id="f4807-143">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="f4807-144">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine du client (par exemple, ), et non le nom d’utilisateur `joe@contoso.cn` `onmschina` (par exemple, `joe@contoso.onmschina.cn` ).</span><span class="sxs-lookup"><span data-stu-id="f4807-144">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="f4807-145">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="f4807-145">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

#### <a name="configure-dns-encryption---windows"></a><span data-ttu-id="f4807-146">Configurer le chiffrement DNS : Windows</span><span class="sxs-lookup"><span data-stu-id="f4807-146">Configure DNS encryption - Windows</span></span>

1. <span data-ttu-id="f4807-147">Obtenez l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="f4807-147">Get the RMS ID:</span></span>

    1. <span data-ttu-id="f4807-148">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f4807-148">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="f4807-149">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="f4807-149">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="f4807-150">Connecter service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="f4807-150">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    4. <span data-ttu-id="f4807-151">Exécutez `(Get-AipServiceConfiguration).RightsManagementServiceId` pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="f4807-151">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

2. <span data-ttu-id="f4807-152">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f4807-152">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

    - <span data-ttu-id="f4807-153">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="f4807-153">Service = `_rmsredir`</span></span>
    - <span data-ttu-id="f4807-154">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="f4807-154">Protocol = `_http`</span></span>
    - <span data-ttu-id="f4807-155">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="f4807-155">Name = `_tcp`</span></span>
    - <span data-ttu-id="f4807-156">Target = `[GUID].rms.aadrm.cn` (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="f4807-156">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
    - <span data-ttu-id="f4807-157">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="f4807-157">Priority, Weight, Seconds, TTL = default values</span></span>

3. <span data-ttu-id="f4807-158">Associez le domaine personnalisé au client dans [le portail Azure.](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains)</span><span class="sxs-lookup"><span data-stu-id="f4807-158">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="f4807-159">Cela ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après avoir ajouté la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="f4807-159">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

4. <span data-ttu-id="f4807-160">Connectez-vous au Centre Microsoft 365'administration avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine (par exemple, ) pour la `contoso.cn` création d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f4807-160">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="f4807-161">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f4807-161">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="f4807-162">Une fois la vérification effectuée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="f4807-162">Once verification is done, users can be created.</span></span>

#### <a name="configure-dns-encryption---mac-ios-android"></a><span data-ttu-id="f4807-163">Configurer le chiffrement DNS - Mac, iOS, Android</span><span class="sxs-lookup"><span data-stu-id="f4807-163">Configure DNS encryption - Mac, iOS, Android</span></span>

<span data-ttu-id="f4807-164">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="f4807-164">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

- <span data-ttu-id="f4807-165">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="f4807-165">Service = `_rmsdisco`</span></span>
- <span data-ttu-id="f4807-166">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="f4807-166">Protocol = `_http`</span></span>
- <span data-ttu-id="f4807-167">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="f4807-167">Name = `_tcp`</span></span>
- <span data-ttu-id="f4807-168">Target = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="f4807-168">Target = `api.aadrm.cn`</span></span>
- <span data-ttu-id="f4807-169">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="f4807-169">Port = `80`</span></span>
- <span data-ttu-id="f4807-170">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="f4807-170">Priority, Weight, Seconds, TTL = default values</span></span>


### <a name="step-4-install-and-configure-the-aip-unified-labeling-client"></a><span data-ttu-id="f4807-171">Étape 4 : Installer et configurer le client d’étiquetage unifié AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-171">Step 4: Install and configure the AIP unified labeling client</span></span>

<span data-ttu-id="f4807-172">Téléchargez et installez le client d’étiquetage unifié AIP à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="f4807-172">Download and install the AIP unified labeling client from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

<span data-ttu-id="f4807-173">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="f4807-173">For more information, see:</span></span>

- [<span data-ttu-id="f4807-174">Documentation AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-174">AIP documentation</span></span>](/azure/information-protection/)
- [<span data-ttu-id="f4807-175">Historique des versions AIP et stratégie de support</span><span class="sxs-lookup"><span data-stu-id="f4807-175">AIP version history and support policy</span></span>](/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history)
- [<span data-ttu-id="f4807-176">Conditions requises pour le système AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-176">AIP system requirements</span></span>](/azure/information-protection/requirements)
- [<span data-ttu-id="f4807-177">Démarrage rapide d’AIP : déployer le client AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-177">AIP quickstart: Deploy the AIP client</span></span>](/azure/information-protection/quickstart-deploy-client)
- [<span data-ttu-id="f4807-178">Guide de l’administrateur AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-178">AIP administrator guide</span></span>](/azure/information-protection/rms-client/clientv2-admin-guide)
- [<span data-ttu-id="f4807-179">Guide de l’utilisateur AIP</span><span class="sxs-lookup"><span data-stu-id="f4807-179">AIP user guide</span></span>](/azure/information-protection/rms-client/clientv2-user-guide)
- [<span data-ttu-id="f4807-180">En savoir plus sur Microsoft 365 étiquettes de sensibilité</span><span class="sxs-lookup"><span data-stu-id="f4807-180">Learn about Microsoft 365 sensitivity labels</span></span>](../../compliance/sensitivity-labels.md)

### <a name="step-5-configure-aip-apps-on-windows"></a><span data-ttu-id="f4807-181">Étape 5 : Configurer les applications AIP sur Windows</span><span class="sxs-lookup"><span data-stu-id="f4807-181">Step 5: Configure AIP apps on Windows</span></span>

<span data-ttu-id="f4807-182">Les applications AIP sur Windows ont besoin de la clé de Registre suivante pour les faire pointer vers le cloud souverain correct pour Azure Chine :</span><span class="sxs-lookup"><span data-stu-id="f4807-182">AIP apps on Windows need the following registry key to point them to the correct sovereign cloud for Azure China:</span></span>

- <span data-ttu-id="f4807-183">Nœud de Registre = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span><span class="sxs-lookup"><span data-stu-id="f4807-183">Registry node = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span></span>
- <span data-ttu-id="f4807-184">Name = `CloudEnvType`</span><span class="sxs-lookup"><span data-stu-id="f4807-184">Name = `CloudEnvType`</span></span>
- <span data-ttu-id="f4807-185">Valeur = `6` (valeur par défaut = 0)</span><span class="sxs-lookup"><span data-stu-id="f4807-185">Value = `6` (default = 0)</span></span>
- <span data-ttu-id="f4807-186">Type = `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="f4807-186">Type = `REG_DWORD`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4807-187">Veillez à ne pas supprimer la clé de Registre après une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f4807-187">Make sure you don't delete the registry key after an uninstall.</span></span> <span data-ttu-id="f4807-188">Si la clé est vide, incorrecte ou inexistante, la fonctionnalité se comporte comme la valeur par défaut (valeur par défaut = 0 pour le cloud commercial).</span><span class="sxs-lookup"><span data-stu-id="f4807-188">If the key is empty, incorrect, or non-existent, the functionality will behave as the default value (default value = 0 for the commercial cloud).</span></span> <span data-ttu-id="f4807-189">Si la clé est vide ou incorrecte, une erreur d’impression est également ajoutée au journal.</span><span class="sxs-lookup"><span data-stu-id="f4807-189">If the key is empty or incorrect, a print error is also added to the log.</span></span>

### <a name="step-6-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs"></a><span data-ttu-id="f4807-190">Étape 6 : Installer le scanneur AIP local et gérer les travaux d’analyse de contenu</span><span class="sxs-lookup"><span data-stu-id="f4807-190">Step 6: Install the AIP on-premises scanner and manage content scan jobs</span></span>

<span data-ttu-id="f4807-191">Installez le scanneur AIP local pour analyser vos partages réseau et de contenu pour les données sensibles, et appliquez des étiquettes de classification et de protection comme configuré dans la stratégie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f4807-191">Install the AIP on-premises scanner to scan your network and content shares for sensitive data, and apply classification and protection labels as configured in your organization's policy.</span></span>

<span data-ttu-id="f4807-192">Lors de la configuration et de la gestion de vos travaux d’analyse de contenu, utilisez la procédure suivante au lieu de [l’interface](/azure/information-protection/deploy-aip-scanner-configure-install?tabs=azure-portal-only) du portail Azure utilisée par les offres commerciales.</span><span class="sxs-lookup"><span data-stu-id="f4807-192">When configuring and managing your content scan jobs, use the following procedure instead of the [Azure portal interface](/azure/information-protection/deploy-aip-scanner-configure-install?tabs=azure-portal-only) that's used by the commercial offerings.</span></span>

<span data-ttu-id="f4807-193">Pour plus d’informations, consultez l’analyseur d’étiquetage unifié [Azure Information Protection](/azure/information-protection/deploy-aip-scanner) et gérez vos travaux d’analyse de contenu à l’aide de [PowerShell uniquement.](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer)</span><span class="sxs-lookup"><span data-stu-id="f4807-193">For more information, see [What is the Azure Information Protection unified labeling scanner?](/azure/information-protection/deploy-aip-scanner) and [Manage your content scan jobs using PowerShell only](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer).</span></span>

<span data-ttu-id="f4807-194">**Pour installer et configurer votre scanneur**:</span><span class="sxs-lookup"><span data-stu-id="f4807-194">**To install and configure your scanner**:</span></span>

1. <span data-ttu-id="f4807-195">Connectez-vous à l Windows server qui exécutera le scanneur.</span><span class="sxs-lookup"><span data-stu-id="f4807-195">Sign in to the Windows Server computer that will run the scanner.</span></span> <span data-ttu-id="f4807-196">Utilisez un compte qui dispose de droits d’administrateur local et qui dispose des autorisations d’écriture dans SQL Server base de données principale.</span><span class="sxs-lookup"><span data-stu-id="f4807-196">Use an account that has local administrator rights and that has permissions to write to the SQL Server master database.</span></span>

1. <span data-ttu-id="f4807-197">Commencez avec PowerShell fermé.</span><span class="sxs-lookup"><span data-stu-id="f4807-197">Start with PowerShell closed.</span></span> <span data-ttu-id="f4807-198">Si vous avez déjà installé le client et le scanneur AIP, assurez-vous que le service **AIPScanner** est arrêté.</span><span class="sxs-lookup"><span data-stu-id="f4807-198">If you've previously installed the AIP client and scanner, make sure that the **AIPScanner** service is stopped.</span></span>

1. <span data-ttu-id="f4807-199">Ouvrez une session Windows PowerShell avec l’option **Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="f4807-199">Open a Windows PowerShell session with the **Run as an administrator** option.</span></span>

1. <span data-ttu-id="f4807-200">Exécutez la cmdlet [Install-AIPScanner,](/powershell/module/azureinformationprotection/Install-AIPScanner) en spécifiant votre instance de SQL Server sur laquelle créer une base de données pour le scanneur Azure Information Protection et un nom significatif pour votre cluster de scanneurs.</span><span class="sxs-lookup"><span data-stu-id="f4807-200">Run the [Install-AIPScanner](/powershell/module/azureinformationprotection/Install-AIPScanner) cmdlet, specifying your SQL Server instance on which to create a database for the Azure Information Protection scanner, and a meaningful name for your scanner cluster.</span></span>

    ```PowerShell
    Install-AIPScanner -SqlServerInstance <name> -Cluster <cluster name>
    ```

    > [!TIP]
    > <span data-ttu-id="f4807-201">Vous pouvez utiliser le même nom de cluster dans la commande [Install-AIPScanner](/powershell/module/azureinformationprotection/install-aipscanner) pour associer plusieurs nodes de scanneur au même cluster.</span><span class="sxs-lookup"><span data-stu-id="f4807-201">You can use the same cluster name in the [Install-AIPScanner](/powershell/module/azureinformationprotection/install-aipscanner) command to associate multiple scanner nodes to the same cluster.</span></span> <span data-ttu-id="f4807-202">L’utilisation du même cluster pour plusieurs nods de scanneur permet à plusieurs scanneurs de travailler ensemble pour effectuer vos analyses.</span><span class="sxs-lookup"><span data-stu-id="f4807-202">Using the same cluster for multiple scanner nodes enables multiple scanners to work together to perform your scans.</span></span>
    > 

1. <span data-ttu-id="f4807-203">Vérifiez que le service est maintenant installé à l’aide des **services d’outils**  >  **d’administration.**</span><span class="sxs-lookup"><span data-stu-id="f4807-203">Verify that the service is now installed by using **Administrative Tools** > **Services**.</span></span>

    <span data-ttu-id="f4807-204">Le service installé est nommé **Scanneur Azure Information Protection et** est configuré pour s’exécuter à l’aide du compte de service de scanneur que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="f4807-204">The installed service is named **Azure Information Protection Scanner** and is configured to run by using the scanner service account that you created.</span></span>

1. <span data-ttu-id="f4807-205">Obtenez un jeton Azure à utiliser avec votre scanneur.</span><span class="sxs-lookup"><span data-stu-id="f4807-205">Get an Azure token to use with your scanner.</span></span> <span data-ttu-id="f4807-206">Un jeton Azure AD permet au scanneur de s’authentifier au service Azure Information Protection, ce qui lui permet de s’exécuter de manière non interactive.</span><span class="sxs-lookup"><span data-stu-id="f4807-206">An Azure AD token allows the scanner to authenticate to the Azure Information Protection service, enabling the scanner to run non-interactively.</span></span> 

    1. <span data-ttu-id="f4807-207">Ouvrez le portail Azure et créez une application Azure AD pour spécifier un jeton d’accès pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="f4807-207">Open the Azure portal and create an Azure AD application to specify an access token for authentication.</span></span> <span data-ttu-id="f4807-208">Pour plus d’informations, [voir Comment étiqueter des fichiers de](/azure/information-protection/rms-client/clientv2-admin-guide-powershell#how-to-label-files-non-interactively-for-azure-information-protection)manière non interactive pour Azure Information Protection .</span><span class="sxs-lookup"><span data-stu-id="f4807-208">For more information, see [How to label files non-interactively for Azure Information Protection](/azure/information-protection/rms-client/clientv2-admin-guide-powershell#how-to-label-files-non-interactively-for-azure-information-protection).</span></span>
    
        > [!TIP]
        > <span data-ttu-id="f4807-209">Lorsque vous créez et configurez des applications Azure AD pour la commande [Set-AIPAuthentication,](/powershell/module/azureinformationprotection/set-aipauthentication) le volet Demander des **autorisations d’API** affiche les API que mon organisation utilise à la place de l’onglet API **Microsoft.**  Sélectionnez **les API que mon organisation utilise** pour sélectionner Azure Rights Management **Services.**</span><span class="sxs-lookup"><span data-stu-id="f4807-209">When creating and configuring Azure AD applications for the [Set-AIPAuthentication](/powershell/module/azureinformationprotection/set-aipauthentication) command, the **Request API permissions** pane shows the **APIs my organization uses** tab instead of the **Microsoft APIs** tab. Select the **APIs my organization uses** to then select **Azure Rights Management Services**.</span></span> 
        >

    1. <span data-ttu-id="f4807-210">À partir de l’ordinateur Windows Server, si votre  compte de service scanneur a reçu l’autorisation Se connecter localement pour l’installation, connectez-vous avec ce compte et démarrez une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4807-210">From the Windows Server computer, if your scanner service account has been granted the **Log on locally** right for the installation, sign in with this account and start a PowerShell session.</span></span> 
    
        <span data-ttu-id="f4807-211">Si votre compte de service  scanneur ne peut pas être autorisé à se connecter localement pour l’installation, utilisez le paramètre *OnBehalfOf* avec [Set-AIPAuthentication](/powershell/module/azureinformationprotection/set-aipauthentication), comme décrit dans la section Comment étiqueter des fichiers de manière non interactive pour [Azure Information Protection](/azure/information-protection/rms-client/clientv2-admin-guide-powershell#how-to-label-files-non-interactively-for-azure-information-protection).</span><span class="sxs-lookup"><span data-stu-id="f4807-211">If your scanner service account cannot be granted the **Log on locally** right for the installation, use the *OnBehalfOf* parameter with [Set-AIPAuthentication](/powershell/module/azureinformationprotection/set-aipauthentication), as described in [How to label files non-interactively for Azure Information Protection](/azure/information-protection/rms-client/clientv2-admin-guide-powershell#how-to-label-files-non-interactively-for-azure-information-protection).</span></span>

    1. <span data-ttu-id="f4807-212">Exécutez [Set-AIPAuthentication](/powershell/module/azureinformationprotection/set-aipauthentication), en spécifiant les valeurs copiées à partir de votre application Azure AD :</span><span class="sxs-lookup"><span data-stu-id="f4807-212">Run [Set-AIPAuthentication](/powershell/module/azureinformationprotection/set-aipauthentication), specifying values copied from your Azure AD application:</span></span>

      ```PowerShell
      Set-AIPAuthentication -AppId <ID of the registered app> -AppSecret <client secret sting> -TenantId <your tenant ID> -DelegatedUser <Azure AD account>
      ```

      <span data-ttu-id="f4807-213">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f4807-213">For example:</span></span>

      ```PowerShell
      $pscreds = Get-Credential CONTOSO\scanner
      Set-AIPAuthentication -AppId "77c3c1c3-abf9-404e-8b2b-4652836c8c66" -AppSecret "OAkk+rnuYc/u+]ah2kNxVbtrDGbS47L4" -DelegatedUser scanner@contoso.com -TenantId "9c11c87a-ac8b-46a3-8d5c-f4d0b72ee29a" -OnBehalfOf $pscreds
      Acquired application access token on behalf of CONTOSO\scanner.
      ```

    <span data-ttu-id="f4807-214">Le scanneur dispose désormais d’un jeton pour s’authentifier sur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f4807-214">The scanner now has a token to authenticate to Azure AD.</span></span> <span data-ttu-id="f4807-215">Ce jeton est valide pendant un an, deux ans ou jamais, en fonction de votre configuration de la question secrète client de **l’application Web /API** dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f4807-215">This token is valid for one year, two years, or never, according to your configuration of the **Web app /API** client secret in Azure AD.</span></span> <span data-ttu-id="f4807-216">Lorsque le jeton expire, vous devez répéter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="f4807-216">When the token expires, you must repeat this procedure.</span></span>

1. <span data-ttu-id="f4807-217">Exécutez la cmdlet [Set-AIPScannerConfiguration](/powershell/module/azureinformationprotection/set-aipscannerconfiguration) pour configurer le scanneur de façon à ce qu’il fonctionne en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f4807-217">Run the [Set-AIPScannerConfiguration](/powershell/module/azureinformationprotection/set-aipscannerconfiguration) cmdlet to set the scanner to function in offline mode.</span></span> <span data-ttu-id="f4807-218">Exécutez :</span><span class="sxs-lookup"><span data-stu-id="f4807-218">Run:</span></span>

    ```powershell
    Set-AIPScannerConfiguration -OnlineConfiguration Off
    ```

1. <span data-ttu-id="f4807-219">Exécutez la cmdlet [Set-AIPScannerContentScanJob](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) pour créer un travail d’analyse de contenu par défaut.</span><span class="sxs-lookup"><span data-stu-id="f4807-219">Run the [Set-AIPScannerContentScanJob](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) cmdlet to create a default content scan job.</span></span>

    <span data-ttu-id="f4807-220">Le seul paramètre requis dans la cmdlet **Set-AIPScannerContentScanJob** est **Enforce**.</span><span class="sxs-lookup"><span data-stu-id="f4807-220">The only required parameter in the **Set-AIPScannerContentScanJob** cmdlet is **Enforce**.</span></span> <span data-ttu-id="f4807-221">Toutefois, vous pouvez définir d’autres paramètres pour votre travail d’analyse de contenu pour le moment.</span><span class="sxs-lookup"><span data-stu-id="f4807-221">However, you may want to define other settings for your content scan job at this time.</span></span> <span data-ttu-id="f4807-222">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f4807-222">For example:</span></span>

    ```powershell
    Set-AIPScannerContentScanJob -Schedule Manual -DiscoverInformationTypes PolicyOnly -Enforce Off -DefaultLabelType PolicyDefault -RelabelFiles Off -PreserveFileDetails On -IncludeFileTypes '' -ExcludeFileTypes '.msg,.tmp' -DefaultOwner <account running the scanner>
    ```

    <span data-ttu-id="f4807-223">La syntaxe ci-dessus configure les paramètres suivants pendant que vous poursuivez la configuration :</span><span class="sxs-lookup"><span data-stu-id="f4807-223">The syntax above configures the following settings while you continue the configuration:</span></span>

    - <span data-ttu-id="f4807-224">Maintient la planification manuelle de l’utilisation du *scanneur*</span><span class="sxs-lookup"><span data-stu-id="f4807-224">Keeps the scanner run scheduling to *manual*</span></span>
    - <span data-ttu-id="f4807-225">Définit les types d’informations à découvrir en fonction de la stratégie d’étiquetage de confidentialité</span><span class="sxs-lookup"><span data-stu-id="f4807-225">Sets the information types to be discovered based on the sensitivity labeling policy</span></span>
    - <span data-ttu-id="f4807-226">*N’applique pas* une stratégie d’étiquetage de confidentialité</span><span class="sxs-lookup"><span data-stu-id="f4807-226">Does *not* enforce a sensitivity labeling policy</span></span>
    - <span data-ttu-id="f4807-227">Étiquettes automatiques des fichiers en fonction du contenu, à l’aide de l’étiquette par défaut définie pour la stratégie d’étiquetage de confidentialité</span><span class="sxs-lookup"><span data-stu-id="f4807-227">Automatically labels files based on content, using the default label defined for the sensitivity labeling policy</span></span>
    - <span data-ttu-id="f4807-228">*N’autorise* pas l’éliodage des fichiers</span><span class="sxs-lookup"><span data-stu-id="f4807-228">Does *not* allow for relabeling files</span></span>
    - <span data-ttu-id="f4807-229">Conserve les détails du fichier lors de l’analyse et de l’étiquetage automatique, y compris la *date de* modification, la dernière *modification* et la modification par *des valeurs*</span><span class="sxs-lookup"><span data-stu-id="f4807-229">Preserves file details while scanning and auto-labeling, including *date modified*, *last modified*, and *modified by* values</span></span>
    - <span data-ttu-id="f4807-230">Définit le scanneur pour exclure les fichiers .msg et .tmp lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="f4807-230">Sets the scanner to exclude .msg and .tmp files when running</span></span>
    - <span data-ttu-id="f4807-231">Définit le propriétaire par défaut sur le compte que vous souhaitez utiliser lors de l’exécution du scanneur</span><span class="sxs-lookup"><span data-stu-id="f4807-231">Sets the default owner to the account you want to use when running the scanner</span></span>

1. <span data-ttu-id="f4807-232">Utilisez la cmdlet [Add-AIPScannerRepository](/powershell/module/azureinformationprotection/add-aipscannerrepository) pour définir les référentiels que vous souhaitez analyser dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-232">Use the [Add-AIPScannerRepository](/powershell/module/azureinformationprotection/add-aipscannerrepository) cmdlet to define the repositories you want to scan in your content scan job.</span></span> <span data-ttu-id="f4807-233">Par exemple, exécutez :</span><span class="sxs-lookup"><span data-stu-id="f4807-233">For example, run:</span></span>

    ```powershell
    Add-AIPScannerRepository -OverrideContentScanJob Off -Path 'c:\repoToScan'
    ```
    
    <span data-ttu-id="f4807-234">Utilisez l’une des syntaxes suivantes, selon le type de référentiel que vous ajoutez :</span><span class="sxs-lookup"><span data-stu-id="f4807-234">Use one of the following syntaxes, depending on the type of repository you're adding:</span></span>

    - <span data-ttu-id="f4807-235">Pour un partage réseau, utilisez `\\Server\Folder` .</span><span class="sxs-lookup"><span data-stu-id="f4807-235">For a network share, use `\\Server\Folder`.</span></span>
    - <span data-ttu-id="f4807-236">Pour une bibliothèque SharePoint, utilisez `http://sharepoint.contoso.com/Shared%20Documents/Folder` .</span><span class="sxs-lookup"><span data-stu-id="f4807-236">For a SharePoint library, use `http://sharepoint.contoso.com/Shared%20Documents/Folder`.</span></span>
    - <span data-ttu-id="f4807-237">Pour un chemin d’accès local : `C:\Folder`</span><span class="sxs-lookup"><span data-stu-id="f4807-237">For a local path: `C:\Folder`</span></span>
    - <span data-ttu-id="f4807-238">Pour un chemin d’accès UNC : `\\Server\Folder`</span><span class="sxs-lookup"><span data-stu-id="f4807-238">For a UNC path: `\\Server\Folder`</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4807-239">Les caractères génériques ne sont pas pris en charge et les emplacements WebDav ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="f4807-239">Wildcards are not supported and WebDav locations are not supported.</span></span>
    >
    > <span data-ttu-id="f4807-240">Pour modifier le référentiel ultérieurement, utilisez la cmdlet [Set-AIPScannerRepository](/powershell/module/azureinformationprotection/set-aipscannerrepository) à la place.</span><span class="sxs-lookup"><span data-stu-id="f4807-240">To modify the repository later on, use the [Set-AIPScannerRepository](/powershell/module/azureinformationprotection/set-aipscannerrepository) cmdlet instead.</span></span> 


<span data-ttu-id="f4807-241">Si nécessaire, poursuivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4807-241">Continue with the following steps as needed:</span></span>

- [<span data-ttu-id="f4807-242">Exécuter un cycle de découverte et afficher les rapports pour le scanneur</span><span class="sxs-lookup"><span data-stu-id="f4807-242">Run a discovery cycle and view reports for the scanner</span></span>](/azure/information-protection/deploy-aip-scanner-manage#run-a-discovery-cycle-and-view-reports-for-the-scanner)
- [<span data-ttu-id="f4807-243">Utiliser PowerShell pour configurer le scanneur pour appliquer la classification et la protection</span><span class="sxs-lookup"><span data-stu-id="f4807-243">Use PowerShell to configure the scanner to apply classification and protection</span></span>](/azure/information-protection/deploy-aip-scanner-configure-install?tabs=azure-portal-only#use-powershell-to-configure-the-scanner-to-apply-classification-and-protection)
- [<span data-ttu-id="f4807-244">Utiliser PowerShell pour configurer une stratégie DLP avec le scanneur</span><span class="sxs-lookup"><span data-stu-id="f4807-244">Use PowerShell to configure a DLP policy with the scanner</span></span>](/azure/information-protection/deploy-aip-scanner-configure-install?tabs=azure-portal-only#use-powershell-to-configure-a-dlp-policy-with-the-scanner)

<span data-ttu-id="f4807-245">Le tableau suivant répertorie les cmdlets PowerShell pertinentes pour l’installation du scanneur et la gestion de vos travaux d’analyse de contenu :</span><span class="sxs-lookup"><span data-stu-id="f4807-245">The following table lists PowerShell cmdlets that are relevant for installing the scanner and managing your content scan jobs:</span></span>

| <span data-ttu-id="f4807-246">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="f4807-246">Cmdlet</span></span> | <span data-ttu-id="f4807-247">Description</span><span class="sxs-lookup"><span data-stu-id="f4807-247">Description</span></span> |
|--|--|
| [<span data-ttu-id="f4807-248">Add-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="f4807-248">Add-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/add-aipscannerrepository) | <span data-ttu-id="f4807-249">Ajoute un nouveau référentiel à votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-249">Adds a new repository to your content scan job.</span></span> |
| [<span data-ttu-id="f4807-250">Get-AIPScannerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4807-250">Get-AIPScannerConfiguration</span></span>](/powershell/module/azureinformationprotection/get-aipscannerconfiguration)|<span data-ttu-id="f4807-251">Renvoie des détails sur votre cluster.</span><span class="sxs-lookup"><span data-stu-id="f4807-251">Returns details about your cluster.</span></span> |
| [<span data-ttu-id="f4807-252">Get-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="f4807-252">Get-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/get-aipscannercontentscanjob) | <span data-ttu-id="f4807-253">Obtient des détails sur votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-253">Gets details about your content scan job.</span></span> |
| [<span data-ttu-id="f4807-254">Get-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="f4807-254">Get-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/get-aipscannerrepository) | <span data-ttu-id="f4807-255">Obtient des détails sur les référentiels définis pour votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-255">Gets details about repositories defined for your content scan job.</span></span> |
| [<span data-ttu-id="f4807-256">Remove-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="f4807-256">Remove-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/remove-aipscannercontentscanjob) | <span data-ttu-id="f4807-257">Supprime votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-257">Deletes your content scan job.</span></span> |
| [<span data-ttu-id="f4807-258">Remove-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="f4807-258">Remove-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/remove-aipscannerrepository) | <span data-ttu-id="f4807-259">Supprime un référentiel de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-259">Removes a repository from your content scan job.</span></span> |
| [<span data-ttu-id="f4807-260">Set-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="f4807-260">Set-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) | <span data-ttu-id="f4807-261">Définit les paramètres de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-261">Defines settings for your content scan job.</span></span> |
| [<span data-ttu-id="f4807-262">Set-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="f4807-262">Set-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/set-aipscannerrepository) | <span data-ttu-id="f4807-263">Définit les paramètres d’un référentiel existant dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="f4807-263">Defines settings for an existing repository in your content scan job.</span></span> |
| | |

<span data-ttu-id="f4807-264">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="f4807-264">For more information, see:</span></span>

- [<span data-ttu-id="f4807-265">Qu’est-ce que le scanneur d’étiquetage unifié Azure Information Protection ?</span><span class="sxs-lookup"><span data-stu-id="f4807-265">What is the Azure Information Protection unified labeling scanner?</span></span>](/azure/information-protection/deploy-aip-scanner)
- [<span data-ttu-id="f4807-266">Configuration et installation du scanneur d’étiquetage unifié Azure Information Protection (AIP)</span><span class="sxs-lookup"><span data-stu-id="f4807-266">Configuring and installing the Azure Information Protection (AIP) unified labeling scanner</span></span>](/azure/information-protection/deploy-aip-scanner-configure-install?tabs=powershell-only)
- <span data-ttu-id="f4807-267">[Gérez vos travaux d’analyse de contenu à l’aide de PowerShell uniquement.](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer)</span><span class="sxs-lookup"><span data-stu-id="f4807-267">[Manage your content scan jobs using PowerShell only](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer).</span></span>
