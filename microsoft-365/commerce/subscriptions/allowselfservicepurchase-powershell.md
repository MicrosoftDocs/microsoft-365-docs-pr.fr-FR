---
title: Utiliser AllowSelfServicePurchase pour le module PowerShell MSCommerce
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: mijeffer, pablom
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: None
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- commerce_ssp
search.appverid:
- MET150
description: Découvrez comment utiliser l’cmdlet AllowSelfServicePurchase PowerShell pour activer ou désactiver l’achat en libre-service.
ROBOTS: NOINDEX, NOFOLLOW
ms.date: 03/18/2021
ms.openlocfilehash: fbba7f4385684a8a34f9feebc28a27e8e867bacb
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53227474"
---
# <a name="use-allowselfservicepurchase-for-the-mscommerce-powershell-module"></a><span data-ttu-id="ef3dd-103">Utiliser AllowSelfServicePurchase pour le module PowerShell MSCommerce</span><span class="sxs-lookup"><span data-stu-id="ef3dd-103">Use AllowSelfServicePurchase for the MSCommerce PowerShell module</span></span>

<span data-ttu-id="ef3dd-104">Le module **PowerShell MSCommerce** est désormais disponible dans la [galerie PowerShell.](https://aka.ms/allowselfservicepurchase-powershell-gallery)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-104">The **MSCommerce** PowerShell module is now available on [PowerShell Gallery](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span></span> <span data-ttu-id="ef3dd-105">Le module inclut une valeur de paramètre **PolicyID** pour **AllowSelfServicePurchase** qui vous permet de contrôler si les utilisateurs de votre organisation peuvent effectuer des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-105">The module includes a **PolicyID** parameter value for **AllowSelfServicePurchase** that lets you control whether users in your organization can make self-service purchases.</span></span>

<span data-ttu-id="ef3dd-106">Vous pouvez utiliser le module **PowerShell MSCommerce** pour :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-106">You can use the **MSCommerce** PowerShell module to:</span></span>

- <span data-ttu-id="ef3dd-107">Afficher l’état par défaut de la valeur du paramètre **AllowSelfServicePurchase** , qu’elle soit activée ou désactivée</span><span class="sxs-lookup"><span data-stu-id="ef3dd-107">View the default state of the **AllowSelfServicePurchase** parameter value — whether it's enabled or disabled</span></span>
- <span data-ttu-id="ef3dd-108">Afficher la liste des produits applicables et si l’achat en libre-service est activé ou désactivé</span><span class="sxs-lookup"><span data-stu-id="ef3dd-108">View a list of applicable products and whether self-service purchase is enabled or disabled</span></span>
- <span data-ttu-id="ef3dd-109">Afficher ou modifier le paramètre actuel d’un produit spécifique pour l’activer ou le désactiver</span><span class="sxs-lookup"><span data-stu-id="ef3dd-109">View or modify the current setting for a specific product to either enable or disable it</span></span>

## <a name="requirements"></a><span data-ttu-id="ef3dd-110">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ef3dd-110">Requirements</span></span>

<span data-ttu-id="ef3dd-111">Pour utiliser le module **PowerShell MSCommerce,** vous devez :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-111">To use the **MSCommerce** PowerShell module, you need:</span></span>

- <span data-ttu-id="ef3dd-112">Un Windows 10 de sécurité</span><span class="sxs-lookup"><span data-stu-id="ef3dd-112">A Windows 10 device</span></span>
- <span data-ttu-id="ef3dd-113">PowerShell 5 ou inférieur.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-113">PowerShell 5 or below.</span></span> <span data-ttu-id="ef3dd-114">Actuellement, PowerShell 6.x/7.x n’est pas pris en charge avec ce module.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-114">Currently, PowerShell 6.x/7.x isn't supported with this module.</span></span>
- <span data-ttu-id="ef3dd-115">Autorisation d’administrateur pour l’appareil</span><span class="sxs-lookup"><span data-stu-id="ef3dd-115">Administrator permission for the device</span></span>
- <span data-ttu-id="ef3dd-116">Rôle d’administrateur global ou de facturation pour votre client</span><span class="sxs-lookup"><span data-stu-id="ef3dd-116">Global or Billing Admin role for your tenant</span></span>

## <a name="install-the-mscommerce-powershell-module"></a><span data-ttu-id="ef3dd-117">Installer le module PowerShell MSCommerce</span><span class="sxs-lookup"><span data-stu-id="ef3dd-117">Install the MSCommerce PowerShell module</span></span>

<span data-ttu-id="ef3dd-118">Vous installez le module **PowerShell MSCommerce** sur votre appareil Windows 10 une seule fois, puis vous l’importez dans chaque session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-118">You install the **MSCommerce** PowerShell module on your Windows 10 device once and then import it into each PowerShell session you start.</span></span> <span data-ttu-id="ef3dd-119">Téléchargez le module **PowerShell MSCommerce** à partir de la [galerie PowerShell.](https://aka.ms/allowselfservicepurchase-powershell-gallery)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-119">Download the **MSCommerce** PowerShell module from the [PowerShell Gallery](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span></span>

<span data-ttu-id="ef3dd-120">Pour installer le module **PowerShell MSCommerce** avec **PowerShellGet,** exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-120">To install the **MSCommerce** PowerShell module with **PowerShellGet**, run the following command:</span></span>

```powershell
Install-Module -Name MSCommerce
```

## <a name="import-mscommerce-into-the-powershell-session"></a><span data-ttu-id="ef3dd-121">Importer MSCommerce dans la session PowerShell</span><span class="sxs-lookup"><span data-stu-id="ef3dd-121">Import MSCommerce into the PowerShell session</span></span>

<span data-ttu-id="ef3dd-122">Après avoir installé le module sur votre Windows 10, vous l’importez dans chaque session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-122">After you install the module on your Windows 10 device, you then import it into each PowerShell session that you start.</span></span> <span data-ttu-id="ef3dd-123">Pour l’importer dans une session PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-123">To import it into a PowerShell session, run the following command:</span></span>

```powershell
Import-Module -Name MSCommerce
```

## <a name="connect-to-mscommerce-with-your-credentials"></a><span data-ttu-id="ef3dd-124">Connecter MSCommerce avec vos informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ef3dd-124">Connect to MSCommerce with your credentials</span></span>

<span data-ttu-id="ef3dd-125">Pour vous connecter au module PowerShell avec vos informations d’identification, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-125">To connect to the PowerShell module with your credentials, run the following command.</span></span>

```powershell
Connect-MSCommerce
```

<span data-ttu-id="ef3dd-126">Cette commande connecte la session PowerShell actuelle à un Azure Active Directory client.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-126">This command connects the current PowerShell session to an Azure Active Directory tenant.</span></span> <span data-ttu-id="ef3dd-127">La commande vous invite à entrer un nom d’utilisateur et un mot de passe pour le client à qui vous souhaitez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-127">The command prompts you for a username and password for the tenant you want to connect to.</span></span> <span data-ttu-id="ef3dd-128">Si l’authentification multifacteur est activée pour vos informations d’identification, vous utilisez l’option interactive pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-128">If multi-factor authentication is enabled for your credentials, you use the interactive option to log in.</span></span>

## <a name="view-details-for-allowselfservicepurchase"></a><span data-ttu-id="ef3dd-129">Afficher les détails de AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="ef3dd-129">View details for AllowSelfServicePurchase</span></span>

<span data-ttu-id="ef3dd-130">Pour afficher une description de la valeur du paramètre **AllowSelfServicePurchase** et de l’état par défaut, en fonction de votre organisation, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-130">To view a description of the **AllowSelfServicePurchase** parameter value and the default status, based on your organization, run the following command:</span></span>

```powershell
Get-MSCommercePolicy -PolicyId AllowSelfServicePurchase
```

## <a name="view-a-list-of-self-service-purchase-products-and-their-status"></a><span data-ttu-id="ef3dd-131">Afficher la liste des produits d’achat libre-service et leur état</span><span class="sxs-lookup"><span data-stu-id="ef3dd-131">View a list of self-service purchase products and their status</span></span>

<span data-ttu-id="ef3dd-132">Pour afficher la liste de tous les produits d’achat libre-service disponibles et l’état de chacun d’eux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-132">To view a list of all available self-service purchase products and the status of each, run the following command:</span></span>

```powershell
Get-MSCommerceProductPolicies -PolicyId AllowSelfServicePurchase
```

<span data-ttu-id="ef3dd-133">Le tableau suivant répertorie les produits disponibles et leur **ProductId**.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-133">The following table lists the available products and their **ProductId**.</span></span>

| <span data-ttu-id="ef3dd-134">Produit</span><span class="sxs-lookup"><span data-stu-id="ef3dd-134">Product</span></span> | <span data-ttu-id="ef3dd-135">ProductId</span><span class="sxs-lookup"><span data-stu-id="ef3dd-135">ProductId</span></span> |
|-----------------------------|--------------|
| <span data-ttu-id="ef3dd-136">Power Apps par utilisateur</span><span class="sxs-lookup"><span data-stu-id="ef3dd-136">Power Apps per user</span></span> | <span data-ttu-id="ef3dd-137">CFQ7TTC0KP0P</span><span class="sxs-lookup"><span data-stu-id="ef3dd-137">CFQ7TTC0KP0P</span></span> |
| <span data-ttu-id="ef3dd-138">Power Automate par utilisateur</span><span class="sxs-lookup"><span data-stu-id="ef3dd-138">Power Automate per user</span></span> | <span data-ttu-id="ef3dd-139">CFQ7TTC0KP0N</span><span class="sxs-lookup"><span data-stu-id="ef3dd-139">CFQ7TTC0KP0N</span></span> |
| <span data-ttu-id="ef3dd-140">Power Automate RPA</span><span class="sxs-lookup"><span data-stu-id="ef3dd-140">Power Automate RPA</span></span> | <span data-ttu-id="ef3dd-141">CFQ7TTC0KXG6</span><span class="sxs-lookup"><span data-stu-id="ef3dd-141">CFQ7TTC0KXG6</span></span>  |
| <span data-ttu-id="ef3dd-142">Power BI Premium (autonome)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-142">Power BI Premium (standalone)</span></span> | <span data-ttu-id="ef3dd-143">CFQ7TTC0KXG7</span><span class="sxs-lookup"><span data-stu-id="ef3dd-143">CFQ7TTC0KXG7</span></span>  |
| <span data-ttu-id="ef3dd-144">Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="ef3dd-144">Power BI Pro</span></span> | <span data-ttu-id="ef3dd-145">CFQ7TTC0L3PB</span><span class="sxs-lookup"><span data-stu-id="ef3dd-145">CFQ7TTC0L3PB</span></span> |
| <span data-ttu-id="ef3dd-146">Project (plan 1)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-146">Project Plan 1</span></span> | <span data-ttu-id="ef3dd-147">CFQ7TTC0KXND</span><span class="sxs-lookup"><span data-stu-id="ef3dd-147">CFQ7TTC0KXND</span></span> |
| <span data-ttu-id="ef3dd-148">Project (plan 3)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-148">Project Plan 3</span></span> | <span data-ttu-id="ef3dd-149">CFQ7TTC0KXNC</span><span class="sxs-lookup"><span data-stu-id="ef3dd-149">CFQ7TTC0KXNC</span></span> |
| <span data-ttu-id="ef3dd-150">Visio (plan 1)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-150">Visio Plan 1</span></span> | <span data-ttu-id="ef3dd-151">CFQ7TTC0KXN9</span><span class="sxs-lookup"><span data-stu-id="ef3dd-151">CFQ7TTC0KXN9</span></span> |
| <span data-ttu-id="ef3dd-152">Visio (plan 2)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-152">Visio Plan 2</span></span> | <span data-ttu-id="ef3dd-153">CFQ7TTC0KXN8</span><span class="sxs-lookup"><span data-stu-id="ef3dd-153">CFQ7TTC0KXN8</span></span> |

## <a name="view-or-set-the-status-for-allowselfservicepurchase"></a><span data-ttu-id="ef3dd-154">Afficher ou définir l’état de AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="ef3dd-154">View or set the status for AllowSelfServicePurchase</span></span>

<span data-ttu-id="ef3dd-155">Une fois que vous avez vu la liste des produits disponibles pour l’achat en libre-service, vous pouvez afficher ou modifier le paramètre d’un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-155">After you view the list of products available for self-service purchase, you can view or modify the setting for a specific product.</span></span>

<span data-ttu-id="ef3dd-156">Pour obtenir le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-156">To get the policy setting for a specific product, run the following command:</span></span>

```powershell
Get-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N
```

<span data-ttu-id="ef3dd-157">Pour activer le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-157">To enable the policy setting for a specific product, run the following command:</span></span>

```powershell
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N -Enabled $True
```

<span data-ttu-id="ef3dd-158">Pour désactiver le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-158">To disable the policy setting for a specific product, run the following command:</span></span>

```powershell
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N -Enabled $False
```

## <a name="example-script-to-disable-allowselfservicepurchase"></a><span data-ttu-id="ef3dd-159">Exemple de script pour désactiver AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="ef3dd-159">Example script to disable AllowSelfServicePurchase</span></span>

<span data-ttu-id="ef3dd-160">L’exemple suivant vous explique comment importer le module **MSCommerce,** vous connectez avec votre compte, obtenez **le ProductId** pour Power Automate, puis désactivez **AllowSelfServicePurchase** pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-160">The following example walks you through how to import the **MSCommerce** module, sign in with your account, get the **ProductId** for Power Automate, and then disable **AllowSelfServicePurchase** for that product.</span></span>

```powershell
Import-Module -Name MSCommerce
Connect-MSCommerce #sign-in with your global or billing administrator account when prompted
$product = Get-MSCommerceProductPolicies -PolicyId AllowSelfServicePurchase | where {$_.ProductName -match 'Power Automate'}
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId $product.ProductID -Enabled $false
```

## <a name="troubleshooting"></a><span data-ttu-id="ef3dd-161">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="ef3dd-161">Troubleshooting</span></span>

### <a name="problem"></a><span data-ttu-id="ef3dd-162">Problème</span><span class="sxs-lookup"><span data-stu-id="ef3dd-162">Problem</span></span>

<span data-ttu-id="ef3dd-163">Vous voyez le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="ef3dd-163">You see the following error message:</span></span>

> <span data-ttu-id="ef3dd-164">HandleError : Échec de la récupération de la stratégie avec PolicyId « AllowSelfServicePurchase » et ErrorMessage - La connexion sous-jacente a été fermée : une erreur inattendue s’est produite lors d’une envoi.</span><span class="sxs-lookup"><span data-stu-id="ef3dd-164">HandleError : Failed to retrieve policy with PolicyId 'AllowSelfServicePurchase', ErrorMessage - The underlying connection was closed: An unexpected error occurred on a send.</span></span>

<span data-ttu-id="ef3dd-165">Cela peut être dû à une version antérieure de TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="ef3dd-165">This may be due to an older version of Transport Layer Security (TLS).</span></span> <span data-ttu-id="ef3dd-166">Pour connecter ce service, vous devez utiliser TLS 1.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ef3dd-166">To connect this service you need to use TLS 1.2 or greater</span></span>

### <a name="solution"></a><span data-ttu-id="ef3dd-167">Solution</span><span class="sxs-lookup"><span data-stu-id="ef3dd-167">Solution</span></span>

<span data-ttu-id="ef3dd-168">Mise à niveau vers TLS 1.2 : (/mem/configmgr/core/plan-design/security/enable-tls-1-2)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-168">Upgrade to TLS 1.2: (/mem/configmgr/core/plan-design/security/enable-tls-1-2)</span></span>

<!--
## Uninstall the MSCommerce module

Before you uninstall the MSCommerce module, close your current PowerShell session, then open a new session with admin rights.

To remove the **MSCommerce** PowerShell module from your computer, run the following command:

```powershell
Uninstall-Module -Name MSCommerce
```-->

## <a name="related-content"></a><span data-ttu-id="ef3dd-169">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="ef3dd-169">Related content</span></span>

<span data-ttu-id="ef3dd-170">[Gérer les achats en libre-service (administrateur)](manage-self-service-purchases-admins.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-170">[Manage self-service purchases (Admin)](manage-self-service-purchases-admins.md) (article)</span></span>

<span data-ttu-id="ef3dd-171">[FAQ sur l’achat en libre-service](self-service-purchase-faq.yml) (article)</span><span class="sxs-lookup"><span data-stu-id="ef3dd-171">[Self-service purchase FAQ](self-service-purchase-faq.yml) (article)</span></span>
