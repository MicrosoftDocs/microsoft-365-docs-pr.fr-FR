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
ms.openlocfilehash: cee50384587ffc3e1e43eb9c6bb07d2e0ced7e13
ms.sourcegitcommit: cbe8724bd71d1c002395d98f1451c5f578c824f9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "49988043"
---
# <a name="azure-information-protection-support-for-office-365-operated-by-21vianet"></a><span data-ttu-id="d2268-103">Prise en charge d’Azure Information Protection pour Office 365 géré par 21Vianet</span><span class="sxs-lookup"><span data-stu-id="d2268-103">Azure Information Protection support for Office 365 operated by 21Vianet</span></span>

<span data-ttu-id="d2268-104">Cet article décrit les différences entre la prise en charge d’Azure Information Protection (AIP) pour Office 365 géré par 21Vianet et les offres commerciales, ainsi que des instructions spécifiques pour configurer AIP pour les clients en Chine, notamment comment installer le scanneur AIP local et gérer les travaux d’analyse de &mdash; contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-104">This article covers the differences between Azure Information Protection (AIP) support for Office 365 operated by 21Vianet and commercial offerings, as well as specific instructions for configuring AIP for customers in China&mdash;including how to install the AIP on-premises scanner and manage content scan jobs.</span></span>

## <a name="differences-between-aip-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="d2268-105">Différences entre AIP pour Office 365 géré par 21Vianet et les offres commerciales</span><span class="sxs-lookup"><span data-stu-id="d2268-105">Differences between AIP for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="d2268-106">Bien que notre objectif soit de fournir toutes les fonctionnalités commerciales aux clients en Chine avec notre offre AIP pour Office 365 gérée par 21Vianet, certaines fonctionnalités manquantes sont à mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="d2268-106">While our goal is to deliver all commercial features and functionality to customers in China with our AIP for Office 365 operated by 21Vianet offer, there's some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="d2268-107">La liste suivante inclut les lacunes existantes entre AIP pour Office 365 géré par 21Vianet et nos offres commerciales depuis janvier 2021 :</span><span class="sxs-lookup"><span data-stu-id="d2268-107">The following list includes the existing gaps between AIP for Office 365 operated by 21Vianet and our commercial offerings as of January 2021:</span></span>

- <span data-ttu-id="d2268-108">La gestion des droits de l’information (IRM) est prise en charge uniquement pour les applications Microsoft 365 pour les entreprises (build 11731.10000 ou supérieure).</span><span class="sxs-lookup"><span data-stu-id="d2268-108">Information Rights Management (IRM) is supported only for Microsoft 365 Apps for enterprise (build 11731.10000 or higher).</span></span> <span data-ttu-id="d2268-109">Office 2010, Office 2013 et les autres versions d’Office 2016 ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d2268-109">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="d2268-110">La migration de services AD RMS (Active Directory Rights Management Services) (AD RMS) vers AIP n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d2268-110">Migration from Active Directory Rights Management Services (AD RMS) to AIP is currently not available.</span></span>
  
- <span data-ttu-id="d2268-111">Le partage de messages électroniques protégés avec des utilisateurs dans le cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d2268-111">Sharing of protected emails with users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="d2268-112">Le partage de documents et de pièces jointes de courrier électronique avec des utilisateurs dans le cloud commercial n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d2268-112">Sharing of documents and email attachments with users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="d2268-113">Cela inclut les utilisateurs d’Office 365 gérés par 21Vianet dans le cloud commercial, les utilisateurs non-Office 365 gérés par les utilisateurs 21Vianet dans le cloud commercial et les utilisateurs titulaires d’une licence RMS pour les particuliers.</span><span class="sxs-lookup"><span data-stu-id="d2268-113">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="d2268-114">Irm avec SharePoint (sites et bibliothèques protégés par IRM) n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d2268-114">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="d2268-115">L’extension d’appareil mobile pour AD RMS n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d2268-115">The Mobile Device Extension for AD RMS is currently not available.</span></span>

- <span data-ttu-id="d2268-116">La [visionneuse mobile n’est](/azure/information-protection/rms-client/mobile-app-faq) pas prise en charge par Azure China 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="d2268-116">The [Mobile Viewer](/azure/information-protection/rms-client/mobile-app-faq) is not supported by Azure China 21Vianet.</span></span>

## <a name="configure-aip-for-customers-in-china"></a><span data-ttu-id="d2268-117">Configurer AIP pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="d2268-117">Configure AIP for customers in China</span></span>

<span data-ttu-id="d2268-118">Pour configurer AIP pour les clients en Chine :</span><span class="sxs-lookup"><span data-stu-id="d2268-118">To configure AIP for customers in China:</span></span>
1. <span data-ttu-id="d2268-119">[Activez la gestion des droits pour le client.](#step-1-enable-rights-management-for-the-tenant)</span><span class="sxs-lookup"><span data-stu-id="d2268-119">[Enable Rights Management for the tenant](#step-1-enable-rights-management-for-the-tenant).</span></span>

2. <span data-ttu-id="d2268-120">[Configurer le chiffrement DNS.](#step-2-configure-dns-encryption)</span><span class="sxs-lookup"><span data-stu-id="d2268-120">[Configure DNS encryption](#step-2-configure-dns-encryption).</span></span>

3. <span data-ttu-id="d2268-121">[Installez et configurez le client d’étiquetage unifié AIP.](#step-3-install-and-configure-the-aip-unified-labeling-client)</span><span class="sxs-lookup"><span data-stu-id="d2268-121">[Install and configure the AIP unified labeling client](#step-3-install-and-configure-the-aip-unified-labeling-client).</span></span>

4. <span data-ttu-id="d2268-122">[Configurer les applications AIP sur Windows](#step-4-configure-aip-apps-on-windows).</span><span class="sxs-lookup"><span data-stu-id="d2268-122">[Configure AIP apps on Windows](#step-4-configure-aip-apps-on-windows).</span></span>

5. <span data-ttu-id="d2268-123">[Installez le scanneur AIP local](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs)et gérez les travaux d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-123">[Install the AIP on-premises scanner and manage content scan jobs](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs).</span></span> 

### <a name="step-1-enable-rights-management-for-the-tenant"></a><span data-ttu-id="d2268-124">Étape 1 : Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="d2268-124">Step 1: Enable Rights Management for the tenant</span></span>

<span data-ttu-id="d2268-125">Pour que le chiffrement fonctionne correctement, RMS doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="d2268-125">For the encryption to work correctly, RMS must be enabled for the tenant.</span></span>

1. <span data-ttu-id="d2268-126">Vérifiez si RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="d2268-126">Check if RMS is enabled:</span></span>

    1. <span data-ttu-id="d2268-127">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d2268-127">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="d2268-128">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="d2268-128">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="d2268-129">Importer le module à l’aide `Import-Module AipService` de .</span><span class="sxs-lookup"><span data-stu-id="d2268-129">Import the module using `Import-Module AipService`.</span></span>
    4. <span data-ttu-id="d2268-130">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="d2268-130">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    5. <span data-ttu-id="d2268-131">Exécutez `(Get-AipServiceConfiguration).FunctionalState` et vérifiez si l’état `Enabled` est .</span><span class="sxs-lookup"><span data-stu-id="d2268-131">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

2. <span data-ttu-id="d2268-132">Si l’état fonctionnel est `Disabled` , exécutez `Enable-AipService` .</span><span class="sxs-lookup"><span data-stu-id="d2268-132">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="step-2-configure-dns-encryption"></a><span data-ttu-id="d2268-133">Étape 2 : Configurer le chiffrement DNS</span><span class="sxs-lookup"><span data-stu-id="d2268-133">Step 2: Configure DNS encryption</span></span>

<span data-ttu-id="d2268-134">Pour que le chiffrement fonctionne correctement, les applications clientes Office doivent se connecter à l’instance chine du service et s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="d2268-134">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="d2268-135">Pour rediriger les applications clientes vers l’instance de service de droite, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="d2268-135">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="d2268-136">Sans l’enregistrement SRV DNS, l’application cliente tentera par défaut de se connecter à l’instance de cloud public et échouera.</span><span class="sxs-lookup"><span data-stu-id="d2268-136">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="d2268-137">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine du client (par exemple, ), et non le nom d’utilisateur `joe@contoso.cn` `onmschina` (par exemple, `joe@contoso.onmschina.cn` ).</span><span class="sxs-lookup"><span data-stu-id="d2268-137">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="d2268-138">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="d2268-138">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

#### <a name="configure-dns-encryption---windows"></a><span data-ttu-id="d2268-139">Configurer le chiffrement DNS - Windows</span><span class="sxs-lookup"><span data-stu-id="d2268-139">Configure DNS encryption - Windows</span></span>

1. <span data-ttu-id="d2268-140">Obtenez l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="d2268-140">Get the RMS ID:</span></span>

    1. <span data-ttu-id="d2268-141">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d2268-141">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="d2268-142">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="d2268-142">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="d2268-143">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="d2268-143">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    4. <span data-ttu-id="d2268-144">Exécutez `(Get-AipServiceConfiguration).RightsManagementServiceId` pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="d2268-144">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

2. <span data-ttu-id="d2268-145">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="d2268-145">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

    - <span data-ttu-id="d2268-146">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="d2268-146">Service = `_rmsredir`</span></span>
    - <span data-ttu-id="d2268-147">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="d2268-147">Protocol = `_http`</span></span>
    - <span data-ttu-id="d2268-148">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="d2268-148">Name = `_tcp`</span></span>
    - <span data-ttu-id="d2268-149">Target = `[GUID].rms.aadrm.cn` (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="d2268-149">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
    - <span data-ttu-id="d2268-150">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="d2268-150">Priority, Weight, Seconds, TTL = default values</span></span>

3. <span data-ttu-id="d2268-151">Associez le domaine personnalisé au client dans [le portail Azure.](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains)</span><span class="sxs-lookup"><span data-stu-id="d2268-151">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="d2268-152">Cela ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après avoir ajouté la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="d2268-152">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

4. <span data-ttu-id="d2268-153">Connectez-vous au Centre d’administration Microsoft 365 avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine (par exemple, ) pour la création `contoso.cn` d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d2268-153">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="d2268-154">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d2268-154">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="d2268-155">Une fois la vérification effectuée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="d2268-155">Once verification is done, users can be created.</span></span>

#### <a name="configure-dns-encryption---mac-ios-android"></a><span data-ttu-id="d2268-156">Configurer le chiffrement DNS - Mac, iOS, Android</span><span class="sxs-lookup"><span data-stu-id="d2268-156">Configure DNS encryption - Mac, iOS, Android</span></span>

<span data-ttu-id="d2268-157">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="d2268-157">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

- <span data-ttu-id="d2268-158">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="d2268-158">Service = `_rmsdisco`</span></span>
- <span data-ttu-id="d2268-159">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="d2268-159">Protocol = `_http`</span></span>
- <span data-ttu-id="d2268-160">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="d2268-160">Name = `_tcp`</span></span>
- <span data-ttu-id="d2268-161">Target = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="d2268-161">Target = `api.aadrm.cn`</span></span>
- <span data-ttu-id="d2268-162">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="d2268-162">Port = `80`</span></span>
- <span data-ttu-id="d2268-163">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="d2268-163">Priority, Weight, Seconds, TTL = default values</span></span>

### <a name="step-3-install-and-configure-the-aip-unified-labeling-client"></a><span data-ttu-id="d2268-164">Étape 3 : Installer et configurer le client d’étiquetage unifié AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-164">Step 3: Install and configure the AIP unified labeling client</span></span>

<span data-ttu-id="d2268-165">Téléchargez le client d’étiquetage unifié AIP à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="d2268-165">Download the AIP unified labeling client from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

<span data-ttu-id="d2268-166">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="d2268-166">For more information, see:</span></span>

- [<span data-ttu-id="d2268-167">Documentation AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-167">AIP documentation</span></span>](/azure/information-protection/)
- [<span data-ttu-id="d2268-168">Historique des versions AIP et stratégie de support</span><span class="sxs-lookup"><span data-stu-id="d2268-168">AIP version history and support policy</span></span>](/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history)
- [<span data-ttu-id="d2268-169">Conditions requises pour le système AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-169">AIP system requirements</span></span>](/azure/information-protection/requirements)
- [<span data-ttu-id="d2268-170">Démarrage rapide AIP : déployer le client AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-170">AIP quickstart: Deploy the AIP client</span></span>](/azure/information-protection/quickstart-deploy-client)
- [<span data-ttu-id="d2268-171">Guide de l’administrateur AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-171">AIP administrator guide</span></span>](/azure/information-protection/rms-client/clientv2-admin-guide)
- [<span data-ttu-id="d2268-172">Guide de l’utilisateur AIP</span><span class="sxs-lookup"><span data-stu-id="d2268-172">AIP user guide</span></span>](/azure/information-protection/rms-client/clientv2-user-guide)
- [<span data-ttu-id="d2268-173">En savoir plus sur les étiquettes de sensibilité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d2268-173">Learn about Microsoft 365 sensitivity labels</span></span>](/microsoft-365/compliance/sensitivity-labels)

### <a name="step-4-configure-aip-apps-on-windows"></a><span data-ttu-id="d2268-174">Étape 4 : Configurer les applications AIP sur Windows</span><span class="sxs-lookup"><span data-stu-id="d2268-174">Step 4: Configure AIP apps on Windows</span></span>

<span data-ttu-id="d2268-175">Les applications AIP sur Windows ont besoin de la clé de Registre suivante pour les faire pointer vers le cloud souverain correct pour Azure China :</span><span class="sxs-lookup"><span data-stu-id="d2268-175">AIP apps on Windows need the following registry key to point them to the correct sovereign cloud for Azure China:</span></span>

- <span data-ttu-id="d2268-176">Nœud de Registre = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span><span class="sxs-lookup"><span data-stu-id="d2268-176">Registry node = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span></span>
- <span data-ttu-id="d2268-177">Name = `CloudEnvType`</span><span class="sxs-lookup"><span data-stu-id="d2268-177">Name = `CloudEnvType`</span></span>
- <span data-ttu-id="d2268-178">Valeur = `6` (valeur par défaut = 0)</span><span class="sxs-lookup"><span data-stu-id="d2268-178">Value = `6` (default = 0)</span></span>
- <span data-ttu-id="d2268-179">Type = `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="d2268-179">Type = `REG_DWORD`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2268-180">Veillez à ne pas supprimer la clé de Registre après une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="d2268-180">Make sure you don't delete the registry key after an uninstall.</span></span> <span data-ttu-id="d2268-181">Si la clé est vide, incorrecte ou inexistante, la fonctionnalité se comporte comme la valeur par défaut (valeur par défaut = 0 pour le cloud commercial).</span><span class="sxs-lookup"><span data-stu-id="d2268-181">If the key is empty, incorrect, or non-existent, the functionality will behave as the default value (default value = 0 for the commercial cloud).</span></span> <span data-ttu-id="d2268-182">Si la clé est vide ou incorrecte, une erreur d’impression est également ajoutée au journal.</span><span class="sxs-lookup"><span data-stu-id="d2268-182">If the key is empty or incorrect, a print error is also added to the log.</span></span>

### <a name="step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs"></a><span data-ttu-id="d2268-183">Étape 5 : Installer le scanneur AIP local et gérer les travaux d’analyse de contenu</span><span class="sxs-lookup"><span data-stu-id="d2268-183">Step 5: Install the AIP on-premises scanner and manage content scan jobs</span></span>

<span data-ttu-id="d2268-184">Installez l’analyseur AIP local pour analyser vos partages réseau et de contenu à la recherche de données sensibles, et appliquez des étiquettes de classification et de protection comme configuré dans la stratégie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d2268-184">Install the AIP on-premises scanner to scan your network and content shares for sensitive data, and apply classification and protection labels as configured in your organization's policy.</span></span>

<span data-ttu-id="d2268-185">Lors de l’installation du scanneur et de la gestion de vos travaux d’analyse de contenu, utilisez les cmdlets suivantes au lieu de l’interface du portail Azure utilisée par les offres commerciales :</span><span class="sxs-lookup"><span data-stu-id="d2268-185">When installing the scanner and managing your content scan jobs, use the following cmdlets instead of the Azure portal interface that's used by the commercial offerings:</span></span><br><br>

| <span data-ttu-id="d2268-186">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="d2268-186">Cmdlet</span></span> | <span data-ttu-id="d2268-187">Description</span><span class="sxs-lookup"><span data-stu-id="d2268-187">Description</span></span> |
|--|--|
| [<span data-ttu-id="d2268-188">Add-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="d2268-188">Add-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/add-aipscannerrepository) | <span data-ttu-id="d2268-189">Ajoute un nouveau référentiel à votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-189">Adds a new repository to your content scan job.</span></span> |
| [<span data-ttu-id="d2268-190">Get-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="d2268-190">Get-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/get-aipscannercontentscanjob) | <span data-ttu-id="d2268-191">Obtient des détails sur votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-191">Gets details about your content scan job.</span></span> |
| [<span data-ttu-id="d2268-192">Get-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="d2268-192">Get-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/get-aipscannerrepository) | <span data-ttu-id="d2268-193">Obtient des détails sur les référentiels définis pour votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-193">Gets details about repositories defined for your content scan job.</span></span> |
| [<span data-ttu-id="d2268-194">Remove-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="d2268-194">Remove-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/remove-aipscannercontentscanjob) | <span data-ttu-id="d2268-195">Supprime votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-195">Deletes your content scan job.</span></span> |
| [<span data-ttu-id="d2268-196">Remove-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="d2268-196">Remove-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/remove-aipscannerrepository) | <span data-ttu-id="d2268-197">Supprime un référentiel de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-197">Removes a repository from your content scan job.</span></span> |
| [<span data-ttu-id="d2268-198">Set-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="d2268-198">Set-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) | <span data-ttu-id="d2268-199">Définit les paramètres de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-199">Defines settings for your content scan job.</span></span> |
| [<span data-ttu-id="d2268-200">Set-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="d2268-200">Set-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/set-aipscannerrepository) | <span data-ttu-id="d2268-201">Définit les paramètres d’un référentiel existant dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="d2268-201">Defines settings for an existing repository in your content scan job.</span></span> |

<span data-ttu-id="d2268-202">Pour plus d’informations, consultez l’analyseur d’étiquetage unifié [Azure Information Protection](/azure/information-protection/deploy-aip-scanner) et gérez vos travaux d’analyse de contenu à l’aide de [PowerShell uniquement.](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer)</span><span class="sxs-lookup"><span data-stu-id="d2268-202">For more information, see [What is the Azure Information Protection unified labeling scanner?](/azure/information-protection/deploy-aip-scanner) and [Manage your content scan jobs using PowerShell only](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer).</span></span>