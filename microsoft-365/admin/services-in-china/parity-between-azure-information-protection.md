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
ms.openlocfilehash: 300e7633237511fb9de64199ae7cf54594f2239e
ms.sourcegitcommit: 3b369a44b71540c8b8214ce588a7aa6f47c3bb1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "50099677"
---
# <a name="azure-information-protection-support-for-office-365-operated-by-21vianet"></a><span data-ttu-id="814ad-103">Prise en charge d’Azure Information Protection pour Office 365 géré par 21Vianet</span><span class="sxs-lookup"><span data-stu-id="814ad-103">Azure Information Protection support for Office 365 operated by 21Vianet</span></span>

<span data-ttu-id="814ad-104">Cet article décrit les différences entre la prise en charge d’Azure Information Protection (AIP) pour Office 365 géré par 21Vianet et les offres commerciales, ainsi que des instructions spécifiques pour configurer AIP pour les clients en Chine, notamment comment installer le scanneur AIP local et gérer les travaux d’analyse de &mdash; contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-104">This article covers the differences between Azure Information Protection (AIP) support for Office 365 operated by 21Vianet and commercial offerings, as well as specific instructions for configuring AIP for customers in China&mdash;including how to install the AIP on-premises scanner and manage content scan jobs.</span></span>

## <a name="differences-between-aip-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="814ad-105">Différences entre AIP pour Office 365 géré par 21Vianet et les offres commerciales</span><span class="sxs-lookup"><span data-stu-id="814ad-105">Differences between AIP for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="814ad-106">Bien que notre objectif soit de fournir toutes les fonctionnalités commerciales aux clients en Chine avec notre offre AIP pour Office 365 gérée par 21Vianet, certaines fonctionnalités manquantes sont à mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="814ad-106">While our goal is to deliver all commercial features and functionality to customers in China with our AIP for Office 365 operated by 21Vianet offer, there's some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="814ad-107">La liste suivante inclut les lacunes existantes entre AIP pour Office 365 géré par 21Vianet et nos offres commerciales depuis janvier 2021 :</span><span class="sxs-lookup"><span data-stu-id="814ad-107">The following list includes the existing gaps between AIP for Office 365 operated by 21Vianet and our commercial offerings as of January 2021:</span></span>

- <span data-ttu-id="814ad-108">La gestion des droits de l’information (IRM) est prise en charge uniquement pour les applications Microsoft 365 pour les entreprises (build 11731.10000 ou supérieure).</span><span class="sxs-lookup"><span data-stu-id="814ad-108">Information Rights Management (IRM) is supported only for Microsoft 365 Apps for enterprise (build 11731.10000 or higher).</span></span> <span data-ttu-id="814ad-109">Office 2010, Office 2013 et les autres versions d’Office 2016 ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="814ad-109">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="814ad-110">La migration de services AD RMS (Active Directory Rights Management Services) (AD RMS) vers AIP n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="814ad-110">Migration from Active Directory Rights Management Services (AD RMS) to AIP is currently not available.</span></span>
  
- <span data-ttu-id="814ad-111">Le partage de messages électroniques protégés avec des utilisateurs dans le cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="814ad-111">Sharing of protected emails with users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="814ad-112">Le partage de documents et de pièces jointes de courrier électronique avec des utilisateurs dans le cloud commercial n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="814ad-112">Sharing of documents and email attachments with users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="814ad-113">Cela inclut les utilisateurs d’Office 365 gérés par 21Vianet dans le cloud commercial, les utilisateurs non-Office 365 gérés par les utilisateurs 21Vianet dans le cloud commercial et les utilisateurs titulaires d’une licence RMS pour les particuliers.</span><span class="sxs-lookup"><span data-stu-id="814ad-113">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="814ad-114">Irm avec SharePoint (sites et bibliothèques protégés par IRM) n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="814ad-114">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="814ad-115">L’extension d’appareil mobile pour AD RMS n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="814ad-115">The Mobile Device Extension for AD RMS is currently not available.</span></span>

- <span data-ttu-id="814ad-116">La [visionneuse mobile n’est](/azure/information-protection/rms-client/mobile-app-faq) pas prise en charge par Azure China 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="814ad-116">The [Mobile Viewer](/azure/information-protection/rms-client/mobile-app-faq) is not supported by Azure China 21Vianet.</span></span>

- <span data-ttu-id="814ad-117">La zone AIP du portail Azure n’est pas disponible pour les clients en Chine.</span><span class="sxs-lookup"><span data-stu-id="814ad-117">The AIP area of the Azure portal is unavailable to customers in China.</span></span> <span data-ttu-id="814ad-118">Utilisez [les commandes PowerShell](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs) au lieu d’effectuer des actions dans le portail, telles que l’installation du scanneur local et la gestion de vos travaux d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-118">Use [PowerShell commands](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs) instead of performing actions in the portal, such as installing the on-premises scanner and managing your content scan jobs.</span></span>

## <a name="configure-aip-for-customers-in-china"></a><span data-ttu-id="814ad-119">Configurer AIP pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="814ad-119">Configure AIP for customers in China</span></span>

<span data-ttu-id="814ad-120">Pour configurer AIP pour les clients en Chine :</span><span class="sxs-lookup"><span data-stu-id="814ad-120">To configure AIP for customers in China:</span></span>
1. <span data-ttu-id="814ad-121">[Activez la gestion des droits pour le client.](#step-1-enable-rights-management-for-the-tenant)</span><span class="sxs-lookup"><span data-stu-id="814ad-121">[Enable Rights Management for the tenant](#step-1-enable-rights-management-for-the-tenant).</span></span>

2. <span data-ttu-id="814ad-122">[Configurer le chiffrement DNS.](#step-2-configure-dns-encryption)</span><span class="sxs-lookup"><span data-stu-id="814ad-122">[Configure DNS encryption](#step-2-configure-dns-encryption).</span></span>

3. <span data-ttu-id="814ad-123">[Installez et configurez le client d’étiquetage unifié AIP.](#step-3-install-and-configure-the-aip-unified-labeling-client)</span><span class="sxs-lookup"><span data-stu-id="814ad-123">[Install and configure the AIP unified labeling client](#step-3-install-and-configure-the-aip-unified-labeling-client).</span></span>

4. <span data-ttu-id="814ad-124">[Configurer les applications AIP sur Windows](#step-4-configure-aip-apps-on-windows).</span><span class="sxs-lookup"><span data-stu-id="814ad-124">[Configure AIP apps on Windows](#step-4-configure-aip-apps-on-windows).</span></span>

5. <span data-ttu-id="814ad-125">[Installez le scanneur AIP local](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs)et gérez les travaux d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-125">[Install the AIP on-premises scanner and manage content scan jobs](#step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs).</span></span> 

### <a name="step-1-enable-rights-management-for-the-tenant"></a><span data-ttu-id="814ad-126">Étape 1 : Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="814ad-126">Step 1: Enable Rights Management for the tenant</span></span>

<span data-ttu-id="814ad-127">Pour que le chiffrement fonctionne correctement, RMS doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="814ad-127">For the encryption to work correctly, RMS must be enabled for the tenant.</span></span>

1. <span data-ttu-id="814ad-128">Vérifiez si RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="814ad-128">Check if RMS is enabled:</span></span>

    1. <span data-ttu-id="814ad-129">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="814ad-129">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="814ad-130">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="814ad-130">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="814ad-131">Importer le module à l’aide `Import-Module AipService` de .</span><span class="sxs-lookup"><span data-stu-id="814ad-131">Import the module using `Import-Module AipService`.</span></span>
    4. <span data-ttu-id="814ad-132">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="814ad-132">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    5. <span data-ttu-id="814ad-133">Exécutez `(Get-AipServiceConfiguration).FunctionalState` et vérifiez si l’état est `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="814ad-133">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

2. <span data-ttu-id="814ad-134">Si l’état fonctionnel est `Disabled` , exécutez `Enable-AipService` .</span><span class="sxs-lookup"><span data-stu-id="814ad-134">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="step-2-configure-dns-encryption"></a><span data-ttu-id="814ad-135">Étape 2 : Configurer le chiffrement DNS</span><span class="sxs-lookup"><span data-stu-id="814ad-135">Step 2: Configure DNS encryption</span></span>

<span data-ttu-id="814ad-136">Pour que le chiffrement fonctionne correctement, les applications clientes Office doivent se connecter à l’instance chine du service et s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="814ad-136">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="814ad-137">Pour rediriger les applications clientes vers l’instance de service de droite, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="814ad-137">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="814ad-138">Sans l’enregistrement SRV DNS, l’application cliente tentera par défaut de se connecter à l’instance de cloud public et échouera.</span><span class="sxs-lookup"><span data-stu-id="814ad-138">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="814ad-139">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine du client (par exemple, ), et non le nom d’utilisateur `joe@contoso.cn` `onmschina` (par exemple, `joe@contoso.onmschina.cn` ).</span><span class="sxs-lookup"><span data-stu-id="814ad-139">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="814ad-140">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="814ad-140">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

#### <a name="configure-dns-encryption---windows"></a><span data-ttu-id="814ad-141">Configurer le chiffrement DNS - Windows</span><span class="sxs-lookup"><span data-stu-id="814ad-141">Configure DNS encryption - Windows</span></span>

1. <span data-ttu-id="814ad-142">Obtenez l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="814ad-142">Get the RMS ID:</span></span>

    1. <span data-ttu-id="814ad-143">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="814ad-143">Launch PowerShell as an administrator.</span></span>
    2. <span data-ttu-id="814ad-144">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="814ad-144">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
    3. <span data-ttu-id="814ad-145">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="814ad-145">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
    4. <span data-ttu-id="814ad-146">Exécutez `(Get-AipServiceConfiguration).RightsManagementServiceId` pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="814ad-146">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

2. <span data-ttu-id="814ad-147">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="814ad-147">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

    - <span data-ttu-id="814ad-148">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="814ad-148">Service = `_rmsredir`</span></span>
    - <span data-ttu-id="814ad-149">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="814ad-149">Protocol = `_http`</span></span>
    - <span data-ttu-id="814ad-150">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="814ad-150">Name = `_tcp`</span></span>
    - <span data-ttu-id="814ad-151">Target = `[GUID].rms.aadrm.cn` (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="814ad-151">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
    - <span data-ttu-id="814ad-152">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="814ad-152">Priority, Weight, Seconds, TTL = default values</span></span>

3. <span data-ttu-id="814ad-153">Associez le domaine personnalisé au client dans [le portail Azure.](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains)</span><span class="sxs-lookup"><span data-stu-id="814ad-153">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="814ad-154">Cela ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après avoir ajouté la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="814ad-154">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

4. <span data-ttu-id="814ad-155">Connectez-vous au Centre d’administration Microsoft 365 avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine (par exemple, ) pour la `contoso.cn` création d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="814ad-155">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="814ad-156">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="814ad-156">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="814ad-157">Une fois la vérification effectuée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="814ad-157">Once verification is done, users can be created.</span></span>

#### <a name="configure-dns-encryption---mac-ios-android"></a><span data-ttu-id="814ad-158">Configurer le chiffrement DNS - Mac, iOS, Android</span><span class="sxs-lookup"><span data-stu-id="814ad-158">Configure DNS encryption - Mac, iOS, Android</span></span>

<span data-ttu-id="814ad-159">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="814ad-159">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

- <span data-ttu-id="814ad-160">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="814ad-160">Service = `_rmsdisco`</span></span>
- <span data-ttu-id="814ad-161">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="814ad-161">Protocol = `_http`</span></span>
- <span data-ttu-id="814ad-162">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="814ad-162">Name = `_tcp`</span></span>
- <span data-ttu-id="814ad-163">Cible = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="814ad-163">Target = `api.aadrm.cn`</span></span>
- <span data-ttu-id="814ad-164">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="814ad-164">Port = `80`</span></span>
- <span data-ttu-id="814ad-165">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="814ad-165">Priority, Weight, Seconds, TTL = default values</span></span>

### <a name="step-3-install-and-configure-the-aip-unified-labeling-client"></a><span data-ttu-id="814ad-166">Étape 3 : Installer et configurer le client d’étiquetage unifié AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-166">Step 3: Install and configure the AIP unified labeling client</span></span>

<span data-ttu-id="814ad-167">Téléchargez le client d’étiquetage unifié AIP à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="814ad-167">Download the AIP unified labeling client from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

<span data-ttu-id="814ad-168">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="814ad-168">For more information, see:</span></span>

- [<span data-ttu-id="814ad-169">Documentation AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-169">AIP documentation</span></span>](/azure/information-protection/)
- [<span data-ttu-id="814ad-170">Historique des versions AIP et stratégie de support</span><span class="sxs-lookup"><span data-stu-id="814ad-170">AIP version history and support policy</span></span>](/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history)
- [<span data-ttu-id="814ad-171">Conditions requises pour le système AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-171">AIP system requirements</span></span>](/azure/information-protection/requirements)
- [<span data-ttu-id="814ad-172">Démarrage rapide AIP : déployer le client AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-172">AIP quickstart: Deploy the AIP client</span></span>](/azure/information-protection/quickstart-deploy-client)
- [<span data-ttu-id="814ad-173">Guide de l’administrateur AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-173">AIP administrator guide</span></span>](/azure/information-protection/rms-client/clientv2-admin-guide)
- [<span data-ttu-id="814ad-174">Guide de l’utilisateur AIP</span><span class="sxs-lookup"><span data-stu-id="814ad-174">AIP user guide</span></span>](/azure/information-protection/rms-client/clientv2-user-guide)
- [<span data-ttu-id="814ad-175">En savoir plus sur les étiquettes de sensibilité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="814ad-175">Learn about Microsoft 365 sensitivity labels</span></span>](/microsoft-365/compliance/sensitivity-labels)

### <a name="step-4-configure-aip-apps-on-windows"></a><span data-ttu-id="814ad-176">Étape 4 : Configurer les applications AIP sur Windows</span><span class="sxs-lookup"><span data-stu-id="814ad-176">Step 4: Configure AIP apps on Windows</span></span>

<span data-ttu-id="814ad-177">Les applications AIP sur Windows ont besoin de la clé de Registre suivante pour les faire pointer vers le cloud souverain correct pour Azure China :</span><span class="sxs-lookup"><span data-stu-id="814ad-177">AIP apps on Windows need the following registry key to point them to the correct sovereign cloud for Azure China:</span></span>

- <span data-ttu-id="814ad-178">Nœud de Registre = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span><span class="sxs-lookup"><span data-stu-id="814ad-178">Registry node = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span></span>
- <span data-ttu-id="814ad-179">Name = `CloudEnvType`</span><span class="sxs-lookup"><span data-stu-id="814ad-179">Name = `CloudEnvType`</span></span>
- <span data-ttu-id="814ad-180">Valeur = `6` (valeur par défaut = 0)</span><span class="sxs-lookup"><span data-stu-id="814ad-180">Value = `6` (default = 0)</span></span>
- <span data-ttu-id="814ad-181">Type = `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="814ad-181">Type = `REG_DWORD`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="814ad-182">Veillez à ne pas supprimer la clé de Registre après une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="814ad-182">Make sure you don't delete the registry key after an uninstall.</span></span> <span data-ttu-id="814ad-183">Si la clé est vide, incorrecte ou inexistante, la fonctionnalité se comporte comme la valeur par défaut (valeur par défaut = 0 pour le cloud commercial).</span><span class="sxs-lookup"><span data-stu-id="814ad-183">If the key is empty, incorrect, or non-existent, the functionality will behave as the default value (default value = 0 for the commercial cloud).</span></span> <span data-ttu-id="814ad-184">Si la clé est vide ou incorrecte, une erreur d’impression est également ajoutée au journal.</span><span class="sxs-lookup"><span data-stu-id="814ad-184">If the key is empty or incorrect, a print error is also added to the log.</span></span>

### <a name="step-5-install-the-aip-on-premises-scanner-and-manage-content-scan-jobs"></a><span data-ttu-id="814ad-185">Étape 5 : Installer le scanneur AIP local et gérer les travaux d’analyse de contenu</span><span class="sxs-lookup"><span data-stu-id="814ad-185">Step 5: Install the AIP on-premises scanner and manage content scan jobs</span></span>

<span data-ttu-id="814ad-186">Installez le scanneur AIP local pour analyser vos partages réseau et de contenu pour les données sensibles, et appliquez des étiquettes de classification et de protection comme configuré dans la stratégie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="814ad-186">Install the AIP on-premises scanner to scan your network and content shares for sensitive data, and apply classification and protection labels as configured in your organization's policy.</span></span>

<span data-ttu-id="814ad-187">Lors de l’installation du scanneur et de la gestion de vos travaux d’analyse de contenu, utilisez les cmdlets suivantes au lieu de l’interface du portail Azure utilisée par les offres commerciales :</span><span class="sxs-lookup"><span data-stu-id="814ad-187">When installing the scanner and managing your content scan jobs, use the following cmdlets instead of the Azure portal interface that's used by the commercial offerings:</span></span><br><br>

| <span data-ttu-id="814ad-188">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="814ad-188">Cmdlet</span></span> | <span data-ttu-id="814ad-189">Description</span><span class="sxs-lookup"><span data-stu-id="814ad-189">Description</span></span> |
|--|--|
| [<span data-ttu-id="814ad-190">Add-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="814ad-190">Add-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/add-aipscannerrepository) | <span data-ttu-id="814ad-191">Ajoute un nouveau référentiel à votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-191">Adds a new repository to your content scan job.</span></span> |
| [<span data-ttu-id="814ad-192">Get-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="814ad-192">Get-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/get-aipscannercontentscanjob) | <span data-ttu-id="814ad-193">Obtient des détails sur votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-193">Gets details about your content scan job.</span></span> |
| [<span data-ttu-id="814ad-194">Get-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="814ad-194">Get-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/get-aipscannerrepository) | <span data-ttu-id="814ad-195">Obtient des détails sur les référentiels définis pour votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-195">Gets details about repositories defined for your content scan job.</span></span> |
| [<span data-ttu-id="814ad-196">Remove-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="814ad-196">Remove-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/remove-aipscannercontentscanjob) | <span data-ttu-id="814ad-197">Supprime votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-197">Deletes your content scan job.</span></span> |
| [<span data-ttu-id="814ad-198">Remove-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="814ad-198">Remove-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/remove-aipscannerrepository) | <span data-ttu-id="814ad-199">Supprime un référentiel de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-199">Removes a repository from your content scan job.</span></span> |
| [<span data-ttu-id="814ad-200">Set-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="814ad-200">Set-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) | <span data-ttu-id="814ad-201">Définit les paramètres de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-201">Defines settings for your content scan job.</span></span> |
| [<span data-ttu-id="814ad-202">Set-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="814ad-202">Set-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/set-aipscannerrepository) | <span data-ttu-id="814ad-203">Définit les paramètres d’un référentiel existant dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="814ad-203">Defines settings for an existing repository in your content scan job.</span></span> |

<span data-ttu-id="814ad-204">Pour plus d’informations, consultez l’analyseur d’étiquetage unifié [Azure Information Protection](/azure/information-protection/deploy-aip-scanner) et gérez vos travaux d’analyse de contenu à l’aide de [PowerShell uniquement.](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer)</span><span class="sxs-lookup"><span data-stu-id="814ad-204">For more information, see [What is the Azure Information Protection unified labeling scanner?](/azure/information-protection/deploy-aip-scanner) and [Manage your content scan jobs using PowerShell only](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer).</span></span>
