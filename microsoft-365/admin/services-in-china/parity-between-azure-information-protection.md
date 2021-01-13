---
title: Parité entre Azure Information Protection pour Office 365 géré par 21Vianet et les offres commerciales
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
ms.reviewer: arthurj
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
ms.openlocfilehash: 50269749b5f4e544263f790ec9c7e4474af57219
ms.sourcegitcommit: 83a40facd66e14343ad3ab72591cab9c41ce6ac0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "49840300"
---
# <a name="parity-between-azure-information-protection-for-office-365-operated-by-21vianet-and-commercial-offerings"></a><span data-ttu-id="a8716-103">Parité entre Azure Information Protection pour Office 365 géré par 21Vianet et les offres commerciales</span><span class="sxs-lookup"><span data-stu-id="a8716-103">Parity between Azure Information Protection for Office 365 operated by 21Vianet and commercial offerings</span></span>

<span data-ttu-id="a8716-104">Bien que notre objectif soit de fournir toutes les fonctionnalités commerciales aux clients en Chine avec notre offre Azure Information Protection (AIP) pour Office 365 géré par 21Vianet, il existe certaines fonctionnalités manquantes que nous voulons mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="a8716-104">While our goal is to deliver all commercial features and functionality to customers in China with our Azure Information Protection (AIP) for Office 365 operated by 21Vianet offer, there's some missing functionality that we'd like to highlight.</span></span>

<span data-ttu-id="a8716-105">La liste suivante inclut les lacunes existantes entre Azure Information Protection pour Office 365 géré par 21Vianet et nos offres commerciales depuis janvier 2021 :</span><span class="sxs-lookup"><span data-stu-id="a8716-105">The following list includes the existing gaps between Azure Information Protection for Office 365 operated by 21Vianet and our commercial offerings as of January 2021:</span></span>

- <span data-ttu-id="a8716-106">La gestion des droits de l’information (IRM) est prise en charge uniquement pour les applications Microsoft 365 pour les entreprises (build 11731.10000 ou supérieure).</span><span class="sxs-lookup"><span data-stu-id="a8716-106">Information Rights Management (IRM) is supported only for Microsoft 365 Apps for enterprise (build 11731.10000 or higher).</span></span> <span data-ttu-id="a8716-107">Office 2010, Office 2013 et les autres versions d’Office 2016 ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8716-107">Office 2010, Office 2013, and other Office 2016 versions are not supported.</span></span>

- <span data-ttu-id="a8716-108">La migration de services AD RMS (Active Directory Rights Management Services) (AD RMS) vers Azure Information Protection n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a8716-108">Migration from Active Directory Rights Management Services (AD RMS) to Azure Information Protection is currently not available.</span></span>
  
- <span data-ttu-id="a8716-109">Le partage de messages électroniques protégés aux utilisateurs dans le cloud commercial est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8716-109">Sharing of protected emails to users in the commercial cloud is supported.</span></span>
  
- <span data-ttu-id="a8716-110">Le partage de documents et de pièces jointes aux utilisateurs dans le cloud commercial n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a8716-110">Sharing of documents and email attachments to users in the commercial cloud is currently not available.</span></span> <span data-ttu-id="a8716-111">Cela inclut les utilisateurs d’Office 365 gérés par 21Vianet dans le cloud commercial, les utilisateurs non-Office 365 gérés par les utilisateurs 21Vianet dans le cloud commercial et les utilisateurs titulaires d’une licence RMS pour les particuliers.</span><span class="sxs-lookup"><span data-stu-id="a8716-111">This includes Office 365 operated by 21Vianet users in the commercial cloud, non-Office 365 operated by 21Vianet users in the commercial cloud, and users with an RMS for Individuals license.</span></span>
  
- <span data-ttu-id="a8716-112">Irm avec SharePoint (sites et bibliothèques protégés par IRM) n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a8716-112">IRM with SharePoint (IRM-protected sites and libraries) is currently not available.</span></span>
  
- <span data-ttu-id="a8716-113">L’extension d’appareil mobile pour AD RMS n’est actuellement pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a8716-113">The Mobile Device Extension for AD RMS is currently not available.</span></span>

- <span data-ttu-id="a8716-114">La [visionneuse mobile n’est](/azure/information-protection/rms-client/mobile-app-faq) pas prise en charge par Azure China 21Vianet.</span><span class="sxs-lookup"><span data-stu-id="a8716-114">The [Mobile Viewer](/azure/information-protection/rms-client/mobile-app-faq) is not supported by Azure China 21Vianet.</span></span>

## <a name="configuring-azure-information-protection-for-customers-in-china"></a><span data-ttu-id="a8716-115">Configuration d’Azure Information Protection pour les clients en Chine</span><span class="sxs-lookup"><span data-stu-id="a8716-115">Configuring Azure Information Protection for customers in China</span></span>

### <a name="enable-rights-management-for-the-tenant"></a><span data-ttu-id="a8716-116">Activer la gestion des droits pour le client</span><span class="sxs-lookup"><span data-stu-id="a8716-116">Enable Rights Management for the tenant</span></span>

<span data-ttu-id="a8716-117">Pour que le chiffrement fonctionne correctement, rms doit être activé pour le client.</span><span class="sxs-lookup"><span data-stu-id="a8716-117">For the encryption to work correctly, the RMS must be enabled for the tenant.</span></span>

- <span data-ttu-id="a8716-118">Vérifiez si RMS est activé :</span><span class="sxs-lookup"><span data-stu-id="a8716-118">Check if the RMS is enabled:</span></span>
  1. <span data-ttu-id="a8716-119">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a8716-119">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="a8716-120">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="a8716-120">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="a8716-121">Importer le module à l’aide `Import-Module AipService` de .</span><span class="sxs-lookup"><span data-stu-id="a8716-121">Import the module using `Import-Module AipService`.</span></span>
  4. <span data-ttu-id="a8716-122">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="a8716-122">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  5. <span data-ttu-id="a8716-123">Exécutez `(Get-AipServiceConfiguration).FunctionalState` et vérifiez si l’état `Enabled` est .</span><span class="sxs-lookup"><span data-stu-id="a8716-123">Run `(Get-AipServiceConfiguration).FunctionalState` and check if the state is `Enabled`.</span></span>

- <span data-ttu-id="a8716-124">Si l’état fonctionnel est `Disabled` , exécutez `Enable-AipService` .</span><span class="sxs-lookup"><span data-stu-id="a8716-124">If the functional state is `Disabled`, run `Enable-AipService`.</span></span>

### <a name="dns-configuration-for-encryption-windows"></a><span data-ttu-id="a8716-125">Configuration DNS pour le chiffrement (Windows)</span><span class="sxs-lookup"><span data-stu-id="a8716-125">DNS configuration for encryption (Windows)</span></span>

<span data-ttu-id="a8716-126">Pour que le chiffrement fonctionne correctement, les applications clientes Office doivent se connecter à l’instance chine du service et s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="a8716-126">For encryption to work correctly, Office client applications must connect to the China instance of the service and bootstrap from there.</span></span> <span data-ttu-id="a8716-127">Pour rediriger les applications clientes vers l’instance de service de droite, l’administrateur client doit configurer un enregistrement SRV DNS avec des informations sur l’URL Azure RMS.</span><span class="sxs-lookup"><span data-stu-id="a8716-127">To redirect client applications to the right service instance, the tenant admin must configure a DNS SRV record with information about the Azure RMS URL.</span></span> <span data-ttu-id="a8716-128">Sans l’enregistrement SRV DNS, l’application cliente tentera par défaut de se connecter à l’instance de cloud public et échouera.</span><span class="sxs-lookup"><span data-stu-id="a8716-128">Without the DNS SRV record, the client application will attempt to connect to the public cloud instance by default and will fail.</span></span>

<span data-ttu-id="a8716-129">En outre, l’hypothèse est que les utilisateurs se connectent avec un nom d’utilisateur basé sur le domaine du client (par exemple, ), et non le nom d’utilisateur `joe@contoso.cn` `onmschina` (par exemple, `joe@contoso.onmschina.cn` ).</span><span class="sxs-lookup"><span data-stu-id="a8716-129">Also, the assumption is that users will log in with a username based off the tenant-owned domain (for example, `joe@contoso.cn`), and not the `onmschina` username (for example, `joe@contoso.onmschina.cn`).</span></span> <span data-ttu-id="a8716-130">Le nom de domaine du nom d’utilisateur est utilisé pour la redirection DNS vers l’instance de service correcte.</span><span class="sxs-lookup"><span data-stu-id="a8716-130">The domain name from the username is used for DNS redirection to the correct service instance.</span></span>

- <span data-ttu-id="a8716-131">Obtenez l’ID RMS :</span><span class="sxs-lookup"><span data-stu-id="a8716-131">Get the RMS ID:</span></span>
  1. <span data-ttu-id="a8716-132">Lancez PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a8716-132">Launch PowerShell as an administrator.</span></span>
  2. <span data-ttu-id="a8716-133">Si le module AIPService n’est pas installé, exécutez `Install-Module AipService` .</span><span class="sxs-lookup"><span data-stu-id="a8716-133">If the AIPService module isn't installed, run `Install-Module AipService`.</span></span>
  3. <span data-ttu-id="a8716-134">Connectez-vous au service à l’aide `Connect-AipService -environmentname azurechinacloud` de .</span><span class="sxs-lookup"><span data-stu-id="a8716-134">Connect to the service using `Connect-AipService -environmentname azurechinacloud`.</span></span>
  4. <span data-ttu-id="a8716-135">Exécutez `(Get-AipServiceConfiguration).RightsManagementServiceId` pour obtenir l’ID RMS.</span><span class="sxs-lookup"><span data-stu-id="a8716-135">Run `(Get-AipServiceConfiguration).RightsManagementServiceId` to get the RMS ID.</span></span>

- <span data-ttu-id="a8716-136">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a8716-136">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>
  - <span data-ttu-id="a8716-137">Service = `_rmsredir`</span><span class="sxs-lookup"><span data-stu-id="a8716-137">Service = `_rmsredir`</span></span>
  - <span data-ttu-id="a8716-138">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="a8716-138">Protocol = `_http`</span></span>
  - <span data-ttu-id="a8716-139">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="a8716-139">Name = `_tcp`</span></span>
  - <span data-ttu-id="a8716-140">Target = `[GUID].rms.aadrm.cn` (où GUID est l’ID RMS)</span><span class="sxs-lookup"><span data-stu-id="a8716-140">Target = `[GUID].rms.aadrm.cn` (where GUID is the RMS ID)</span></span>
  - <span data-ttu-id="a8716-141">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="a8716-141">Priority, Weight, Seconds, TTL = default values</span></span>

- <span data-ttu-id="a8716-142">Associez le domaine personnalisé au client dans [le portail Azure.](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains)</span><span class="sxs-lookup"><span data-stu-id="a8716-142">Associate the custom domain with the tenant in the [Azure portal](https://portal.azure.cn/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Domains).</span></span> <span data-ttu-id="a8716-143">Cela ajoute une entrée dans DNS, qui peut prendre plusieurs minutes pour être vérifiée après avoir ajouté la valeur aux paramètres DNS.</span><span class="sxs-lookup"><span data-stu-id="a8716-143">This will add an entry in DNS, which might take several minutes to get verified after you add the value to the DNS settings.</span></span>

- <span data-ttu-id="a8716-144">Connectez-vous au Centre d’administration Microsoft 365 avec les informations d’identification d’administrateur global correspondantes et ajoutez le domaine (par exemple, ) pour la création `contoso.cn` d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a8716-144">Log in to the Microsoft 365 admin center with the corresponding global admin credentials and add the domain (for example, `contoso.cn`) for user creation.</span></span> <span data-ttu-id="a8716-145">Dans le processus de vérification, des modifications DNS supplémentaires peuvent être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a8716-145">In the verification process, additional DNS changes might be required.</span></span> <span data-ttu-id="a8716-146">Une fois la vérification effectuée, les utilisateurs peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="a8716-146">Once verification is done, users can be created.</span></span>

### <a name="dns-configuration-for-encryption-mac-ios-android"></a><span data-ttu-id="a8716-147">Configuration DNS pour le chiffrement (Mac, iOS, Android)</span><span class="sxs-lookup"><span data-stu-id="a8716-147">DNS configuration for encryption (Mac, iOS, Android)</span></span>

<span data-ttu-id="a8716-148">Connectez-vous à votre fournisseur DNS, accédez aux paramètres DNS du domaine, puis ajoutez un nouvel enregistrement SRV.</span><span class="sxs-lookup"><span data-stu-id="a8716-148">Log in to your DNS provider, navigate to the DNS settings for the domain, and then add a new SRV record.</span></span>

- <span data-ttu-id="a8716-149">Service = `_rmsdisco`</span><span class="sxs-lookup"><span data-stu-id="a8716-149">Service = `_rmsdisco`</span></span>
- <span data-ttu-id="a8716-150">Protocole = `_http`</span><span class="sxs-lookup"><span data-stu-id="a8716-150">Protocol = `_http`</span></span>
- <span data-ttu-id="a8716-151">Name = `_tcp`</span><span class="sxs-lookup"><span data-stu-id="a8716-151">Name = `_tcp`</span></span>
- <span data-ttu-id="a8716-152">Cible = `api.aadrm.cn`</span><span class="sxs-lookup"><span data-stu-id="a8716-152">Target = `api.aadrm.cn`</span></span>
- <span data-ttu-id="a8716-153">Port = `80`</span><span class="sxs-lookup"><span data-stu-id="a8716-153">Port = `80`</span></span>
- <span data-ttu-id="a8716-154">Priority, Weight, Seconds, TTL = default values</span><span class="sxs-lookup"><span data-stu-id="a8716-154">Priority, Weight, Seconds, TTL = default values</span></span>

### <a name="aip-client-configuration"></a><span data-ttu-id="a8716-155">Configuration du client AIP</span><span class="sxs-lookup"><span data-stu-id="a8716-155">AIP client configuration</span></span>

<span data-ttu-id="a8716-156">Le client AIP unifié peut être téléchargé à partir du [Centre de téléchargement Microsoft.](https://www.microsoft.com/download/details.aspx?id=53018)</span><span class="sxs-lookup"><span data-stu-id="a8716-156">The unified AIP client can be downloaded from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53018).</span></span>

<span data-ttu-id="a8716-157">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="a8716-157">For more information, see:</span></span>

- [<span data-ttu-id="a8716-158">Documentation Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="a8716-158">Azure Information Protection documentation</span></span>](/azure/information-protection/)
- [<span data-ttu-id="a8716-159">Historique des versions AIP et stratégie de support</span><span class="sxs-lookup"><span data-stu-id="a8716-159">AIP version history and support policy</span></span>](/azure/information-protection/rms-client/unifiedlabelingclient-version-release-history)
- [<span data-ttu-id="a8716-160">Conditions requises pour le système AIP</span><span class="sxs-lookup"><span data-stu-id="a8716-160">AIP system requirements</span></span>](/azure/information-protection/requirements)
- [<span data-ttu-id="a8716-161">Démarrage rapide d’AIP : déployer le client AIP</span><span class="sxs-lookup"><span data-stu-id="a8716-161">AIP quickstart: Deploy the AIP client</span></span>](/azure/information-protection/quickstart-deploy-client)
- [<span data-ttu-id="a8716-162">Guide de l’administrateur AIP</span><span class="sxs-lookup"><span data-stu-id="a8716-162">AIP administrator guide</span></span>](/azure/information-protection/rms-client/clientv2-admin-guide)
- [<span data-ttu-id="a8716-163">Guide de l’utilisateur AIP</span><span class="sxs-lookup"><span data-stu-id="a8716-163">AIP user guide</span></span>](/azure/information-protection/rms-client/clientv2-user-guide)
- [<span data-ttu-id="a8716-164">En savoir plus sur les étiquettes de sensibilité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a8716-164">Learn about Microsoft 365 sensitivity labels</span></span>](/microsoft-365/compliance/sensitivity-labels)

### <a name="aip-apps-configuration-unified-labeling-client-only"></a><span data-ttu-id="a8716-165">Configuration des applications AIP (client d’étiquetage unifié uniquement)</span><span class="sxs-lookup"><span data-stu-id="a8716-165">AIP apps configuration (unified labeling client only)</span></span>

<span data-ttu-id="a8716-166">Pour la solution d’étiquetage unifié, les applications AIP sur Windows ont besoin de la clé de Registre suivante pour les faire pointer vers le cloud souverain correct pour Azure Chine :</span><span class="sxs-lookup"><span data-stu-id="a8716-166">For the unified labeling solution, AIP apps on Windows need the following registry key to point them to the correct sovereign cloud for Azure China:</span></span>

- <span data-ttu-id="a8716-167">Nœud de Registre = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span><span class="sxs-lookup"><span data-stu-id="a8716-167">Registry node = `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\MSIP`</span></span>
- <span data-ttu-id="a8716-168">Name = `CloudEnvType`</span><span class="sxs-lookup"><span data-stu-id="a8716-168">Name = `CloudEnvType`</span></span>
- <span data-ttu-id="a8716-169">Valeur = `6` (valeur par défaut = 0)</span><span class="sxs-lookup"><span data-stu-id="a8716-169">Value = `6` (default = 0)</span></span>
- <span data-ttu-id="a8716-170">Type = `REG_DWORD`</span><span class="sxs-lookup"><span data-stu-id="a8716-170">Type = `REG_DWORD`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8716-171">Veillez à ne pas supprimer la clé de Registre après une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="a8716-171">Make sure you don't delete the registry key after an uninstall.</span></span> <span data-ttu-id="a8716-172">Si la clé est vide, incorrecte ou inexistante, la fonctionnalité se comporte comme la valeur par défaut (valeur par défaut = 0 pour le cloud commercial).</span><span class="sxs-lookup"><span data-stu-id="a8716-172">If the key is empty, incorrect, or non-existent, the functionality will behave as the default value (default value = 0 for the commercial cloud).</span></span> <span data-ttu-id="a8716-173">Si la clé est vide ou incorrecte, une erreur d’impression est également ajoutée au journal.</span><span class="sxs-lookup"><span data-stu-id="a8716-173">If the key is empty or incorrect, a print error is also added to the log.</span></span>

### <a name="manage-azure-information-protection-content-scan-jobs"></a><span data-ttu-id="a8716-174">Gérer les travaux d’analyse de contenu Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="a8716-174">Manage Azure Information Protection content scan jobs</span></span>

<span data-ttu-id="a8716-175">Pour gérer vos travaux d’analyse de contenu Azure Information Protection avec un serveur Azure China Scanner, utilisez les cmdlets suivantes au lieu du portail Azure :</span><span class="sxs-lookup"><span data-stu-id="a8716-175">To manage your Azure Information Protection content scan jobs with an Azure China scanner server, use the following cmdlets instead of the Azure portal:</span></span><br><br>

| <span data-ttu-id="a8716-176">Applet de commande</span><span class="sxs-lookup"><span data-stu-id="a8716-176">Cmdlet</span></span> | <span data-ttu-id="a8716-177">Description</span><span class="sxs-lookup"><span data-stu-id="a8716-177">Description</span></span> |
|--|--|
| [<span data-ttu-id="a8716-178">Add-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="a8716-178">Add-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/add-aipscannerrepository) | <span data-ttu-id="a8716-179">Ajoute un nouveau référentiel à votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-179">Adds a new repository to your content scan job.</span></span> |
| [<span data-ttu-id="a8716-180">Get-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="a8716-180">Get-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/get-aipscannercontentscanjob) | <span data-ttu-id="a8716-181">Obtient des détails sur votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-181">Gets details about your content scan job.</span></span> |
| [<span data-ttu-id="a8716-182">Get-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="a8716-182">Get-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/get-aipscannerrepository) | <span data-ttu-id="a8716-183">Obtient des détails sur les référentiels définis pour votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-183">Gets details about repositories defined for your content scan job.</span></span> |
| [<span data-ttu-id="a8716-184">Remove-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="a8716-184">Remove-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/remove-aipscannercontentscanjob) | <span data-ttu-id="a8716-185">Supprime votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-185">Deletes your content scan job.</span></span> |
| [<span data-ttu-id="a8716-186">Remove-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="a8716-186">Remove-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/remove-aipscannerrepository) | <span data-ttu-id="a8716-187">Supprime un référentiel de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-187">Removes a repository from your content scan job.</span></span> |
| [<span data-ttu-id="a8716-188">Set-AIPScannerContentScanJob</span><span class="sxs-lookup"><span data-stu-id="a8716-188">Set-AIPScannerContentScanJob</span></span>](/powershell/module/azureinformationprotection/set-aipscannercontentscanjob) | <span data-ttu-id="a8716-189">Définit les paramètres de votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-189">Defines settings for your content scan job.</span></span> |
| [<span data-ttu-id="a8716-190">Set-AIPScannerRepository</span><span class="sxs-lookup"><span data-stu-id="a8716-190">Set-AIPScannerRepository</span></span>](/powershell/module/azureinformationprotection/set-aipscannerrepository) | <span data-ttu-id="a8716-191">Définit les paramètres d’un référentiel existant dans votre travail d’analyse de contenu.</span><span class="sxs-lookup"><span data-stu-id="a8716-191">Defines settings for an existing repository in your content scan job.</span></span> |

<span data-ttu-id="a8716-192">Pour plus d’informations, voir [Gérer vos travaux d’analyse de contenu à l’aide de PowerShell uniquement.](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer)</span><span class="sxs-lookup"><span data-stu-id="a8716-192">For more information, see [Manage your content scan jobs using PowerShell only](/azure/information-protection/deploy-aip-scanner-prereqs#use-powershell-with-a-disconnected-computer).</span></span>