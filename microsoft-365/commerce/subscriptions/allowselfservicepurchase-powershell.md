---
title: Utiliser AllowSelfServicePurchase pour le module MSCommerce PowerShell
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: None
ms.collection:
- commerce
ms.custom: AdminSurgePortfolio
search.appverid:
- MET150
description: Découvrez comment utiliser l’applet de commande AllowSelfServicePurchase PowerShell pour activer ou désactiver l’achat libre-service.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 79ee2d96fa1ae6f49f0402f49ddec34e69257082
ms.sourcegitcommit: 6a1a8aa024fd685d04da97bfcbc8eadacc488534
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46653712"
---
# <a name="use-allowselfservicepurchase-for-the-mscommerce-powershell-module"></a><span data-ttu-id="61a04-103">Utiliser AllowSelfServicePurchase pour le module MSCommerce PowerShell</span><span class="sxs-lookup"><span data-stu-id="61a04-103">Use AllowSelfServicePurchase for the MSCommerce PowerShell module</span></span>

<span data-ttu-id="61a04-104">Le module PowerShell **MSCommerce** est désormais disponible dans la [Galerie PowerShell](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span><span class="sxs-lookup"><span data-stu-id="61a04-104">The **MSCommerce** PowerShell module is now available on [PowerShell Gallery](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span></span> <span data-ttu-id="61a04-105">Le module inclut une valeur de paramètre **PolicyID** pour **AllowSelfServicePurchase** qui vous permet de contrôler si les utilisateurs de votre organisation peuvent faire des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="61a04-105">The module includes a **PolicyID** parameter value for **AllowSelfServicePurchase** that lets you control whether users in your organization can make self-service purchases.</span></span>

<span data-ttu-id="61a04-106">Vous pouvez utiliser le module PowerShell **MSCommerce** pour :</span><span class="sxs-lookup"><span data-stu-id="61a04-106">You can use the **MSCommerce** PowerShell module to:</span></span>

- <span data-ttu-id="61a04-107">Afficher l’État par défaut de la valeur du paramètre **AllowSelfServicePurchase** , qu’elle soit activée ou désactivée</span><span class="sxs-lookup"><span data-stu-id="61a04-107">View the default state of the **AllowSelfServicePurchase** parameter value — whether it's enabled or disabled</span></span>
- <span data-ttu-id="61a04-108">Afficher la liste des produits applicables et indiquer si les achats en libre-service sont activés ou désactivés</span><span class="sxs-lookup"><span data-stu-id="61a04-108">View a list of applicable products and whether self-service purchase is enabled or disabled</span></span>
- <span data-ttu-id="61a04-109">Afficher ou modifier le paramètre actuel d’un produit spécifique pour l’activer ou le désactiver</span><span class="sxs-lookup"><span data-stu-id="61a04-109">View or modify the current setting for a specific product to either enable or disable it</span></span>

## <a name="requirements"></a><span data-ttu-id="61a04-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61a04-110">Requirements</span></span>

<span data-ttu-id="61a04-111">Pour utiliser le module PowerShell **MSCommerce** , vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="61a04-111">To use the **MSCommerce** PowerShell module, you need:</span></span>

- <span data-ttu-id="61a04-112">Un appareil Windows 10</span><span class="sxs-lookup"><span data-stu-id="61a04-112">A Windows 10 device</span></span>
- <span data-ttu-id="61a04-113">Autorisation d’administrateur pour l’appareil</span><span class="sxs-lookup"><span data-stu-id="61a04-113">Administrator permission for the device</span></span>
- <span data-ttu-id="61a04-114">Rôle d’administrateur général ou d’administrateur de facturation pour votre client</span><span class="sxs-lookup"><span data-stu-id="61a04-114">Global or Billing Admin role for your tenant</span></span>

## <a name="install-the-mscommerce-powershell-module"></a><span data-ttu-id="61a04-115">Installer le module MSCommerce PowerShell</span><span class="sxs-lookup"><span data-stu-id="61a04-115">Install the MSCommerce PowerShell module</span></span>

<span data-ttu-id="61a04-116">Vous devez installer une fois le module **MSCommerce** PowerShell sur votre appareil Windows 10, puis l’importer dans chaque session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="61a04-116">You install the **MSCommerce** PowerShell module on your Windows 10 device once and then import it into each PowerShell session you start.</span></span> <span data-ttu-id="61a04-117">Téléchargez le module **MSCommerce** PowerShell à partir de la [Galerie PowerShell](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span><span class="sxs-lookup"><span data-stu-id="61a04-117">Download the **MSCommerce** PowerShell module from the [PowerShell Gallery](https://aka.ms/allowselfservicepurchase-powershell-gallery).</span></span>

<span data-ttu-id="61a04-118">Pour installer le module **MSCommerce** PowerShell avec **PowerShellGet**, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-118">To install the **MSCommerce** PowerShell module with **PowerShellGet**, run the following command:</span></span>

```powershell
Install-Module -Name MSCommerce
```

## <a name="import-mscommerce-into-the-powershell-session"></a><span data-ttu-id="61a04-119">Importer MSCommerce dans la session PowerShell</span><span class="sxs-lookup"><span data-stu-id="61a04-119">Import MSCommerce into the PowerShell session</span></span>

<span data-ttu-id="61a04-120">Après avoir installé le module sur votre appareil Windows 10, vous l’importez dans chaque session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="61a04-120">After you install the module on your Windows 10 device, you then import it into each PowerShell session that you start.</span></span> <span data-ttu-id="61a04-121">Pour l’importer dans une session PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-121">To import it into a PowerShell session, run the following command:</span></span>

```powershell
Import-Module -Name MSCommerce
```

## <a name="connect-to-mscommerce-with-your-credentials"></a><span data-ttu-id="61a04-122">Se connecter à MSCommerce avec vos informations d’identification</span><span class="sxs-lookup"><span data-stu-id="61a04-122">Connect to MSCommerce with your credentials</span></span>

<span data-ttu-id="61a04-123">Pour vous connecter au module PowerShell avec vos informations d’identification, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="61a04-123">To connect to the PowerShell module with your credentials, run the following command.</span></span>

```powershell
Connect-MSCommerce
```

<span data-ttu-id="61a04-124">Cette commande connecte la session PowerShell active à un client Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61a04-124">This command connects the current PowerShell session to an Azure Active Directory tenant.</span></span> <span data-ttu-id="61a04-125">La commande vous invite à entrer un nom d’utilisateur et un mot de passe pour le client auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61a04-125">The command prompts you for a username and password for the tenant you want to connect to.</span></span> <span data-ttu-id="61a04-126">Si l’authentification multifacteur est activée pour vos informations d’identification, vous utilisez l’option interactive pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="61a04-126">If multi-factor authentication is enabled for your credentials, you use the interactive option to log in.</span></span>

## <a name="view-details-for-allowselfservicepurchase"></a><span data-ttu-id="61a04-127">Afficher les détails pour AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="61a04-127">View details for AllowSelfServicePurchase</span></span>

<span data-ttu-id="61a04-128">Pour afficher une description de la valeur du paramètre **AllowSelfServicePurchase** et l’État par défaut, en fonction de votre organisation, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-128">To view a description of the **AllowSelfServicePurchase** parameter value and the default status, based on your organization, run the following command:</span></span>

```powershell
Get-MSCommercePolicy -PolicyId AllowSelfServicePurchase
```

## <a name="view-a-list-of-self-service-purchase-products-and-their-status"></a><span data-ttu-id="61a04-129">Affichage de la liste des produits achetés en libre-service et de leur statut</span><span class="sxs-lookup"><span data-stu-id="61a04-129">View a list of self-service purchase products and their status</span></span>

<span data-ttu-id="61a04-130">Pour afficher la liste de tous les produits d’achat libre-service disponibles et l’état de chacun d’eux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-130">To view a list of all available self-service purchase products and the status of each, run the following command:</span></span>

```powershell
Get-MSCommerceProductPolicies -PolicyId AllowSelfServicePurchase
```

<span data-ttu-id="61a04-131">Le tableau suivant répertorie les produits disponibles et leur **ProductID**.</span><span class="sxs-lookup"><span data-stu-id="61a04-131">The following table lists the available products and their **ProductId**.</span></span>

| <span data-ttu-id="61a04-132">Produit</span><span class="sxs-lookup"><span data-stu-id="61a04-132">Product</span></span> | <span data-ttu-id="61a04-133">Mentionnées</span><span class="sxs-lookup"><span data-stu-id="61a04-133">ProductId</span></span> |
|-----------------------------|--------------|
| <span data-ttu-id="61a04-134">Applications puissantes par utilisateur</span><span class="sxs-lookup"><span data-stu-id="61a04-134">Power Apps per user</span></span> | <span data-ttu-id="61a04-135">CFQ7TTC0KP0P</span><span class="sxs-lookup"><span data-stu-id="61a04-135">CFQ7TTC0KP0P</span></span> |
| <span data-ttu-id="61a04-136">Power Automated per User</span><span class="sxs-lookup"><span data-stu-id="61a04-136">Power Automate per user</span></span> | <span data-ttu-id="61a04-137">CFQ7TTC0KP0N</span><span class="sxs-lookup"><span data-stu-id="61a04-137">CFQ7TTC0KP0N</span></span> |
| <span data-ttu-id="61a04-138">Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="61a04-138">Power BI Pro</span></span> | <span data-ttu-id="61a04-139">CFQ7TTC0L3PB</span><span class="sxs-lookup"><span data-stu-id="61a04-139">CFQ7TTC0L3PB</span></span> |
| <span data-ttu-id="61a04-140">Plan de projet 1</span><span class="sxs-lookup"><span data-stu-id="61a04-140">Project Plan 1</span></span> | <span data-ttu-id="61a04-141">CFQ7TTC0KXND</span><span class="sxs-lookup"><span data-stu-id="61a04-141">CFQ7TTC0KXND</span></span> |
| <span data-ttu-id="61a04-142">Plan de projet 3</span><span class="sxs-lookup"><span data-stu-id="61a04-142">Project Plan 3</span></span> | <span data-ttu-id="61a04-143">CFQ7TTC0KXNC</span><span class="sxs-lookup"><span data-stu-id="61a04-143">CFQ7TTC0KXNC</span></span> |
| <span data-ttu-id="61a04-144">Visio (plan 1)</span><span class="sxs-lookup"><span data-stu-id="61a04-144">Visio Plan 1</span></span> | <span data-ttu-id="61a04-145">CFQ7TTC0KXN9</span><span class="sxs-lookup"><span data-stu-id="61a04-145">CFQ7TTC0KXN9</span></span> |
| <span data-ttu-id="61a04-146">Visio (plan 2)</span><span class="sxs-lookup"><span data-stu-id="61a04-146">Visio Plan 2</span></span> | <span data-ttu-id="61a04-147">CFQ7TTC0KXN8</span><span class="sxs-lookup"><span data-stu-id="61a04-147">CFQ7TTC0KXN8</span></span> |

## <a name="view-or-set-the-status-for-allowselfservicepurchase"></a><span data-ttu-id="61a04-148">Afficher ou définir l’État pour AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="61a04-148">View or set the status for AllowSelfServicePurchase</span></span>

<span data-ttu-id="61a04-149">Une fois que vous avez consulté la liste des produits disponibles pour l’achat en libre-service, vous pouvez afficher ou modifier le paramètre d’un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="61a04-149">After you view the list of products available for self-service purchase, you can view or modify the setting for a specific product.</span></span>

<span data-ttu-id="61a04-150">Pour obtenir le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-150">To get the policy setting for a specific product, run the following command:</span></span>

```powershell
Get-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N
```

<span data-ttu-id="61a04-151">Pour activer le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-151">To enable the policy setting for a specific product, run the following command:</span></span>

```powershell
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N -Enabled $True
```

<span data-ttu-id="61a04-152">Pour désactiver le paramètre de stratégie pour un produit spécifique, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="61a04-152">To disable the policy setting for a specific product, run the following command:</span></span>

```powershell
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId CFQ7TTC0KP0N -Enabled $False
```

## <a name="example-script-to-disable-allowselfservicepurchase"></a><span data-ttu-id="61a04-153">Exemple de script pour désactiver AllowSelfServicePurchase</span><span class="sxs-lookup"><span data-stu-id="61a04-153">Example script to disable AllowSelfServicePurchase</span></span>

<span data-ttu-id="61a04-154">L’exemple suivant explique comment importer le module **MSCommerce** , se connecter avec votre compte, obtenir le **ProductID** de Power automate, puis désactiver **AllowSelfServicePurchase** pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="61a04-154">The following example walks you through how to import the **MSCommerce** module, sign in with your account, get the **ProductId** for Power Automate, and then disable **AllowSelfServicePurchase** for that product.</span></span>

```powershell
Import-Module -Name MSCommerce
Connect-MSCommerce #sign-in with your global or billing administrator account when prompted
$product = Get-MSCommerceProductPolicies -PolicyId AllowSelfServicePurchase | where {$_.ProductName -match 'Power Automate'}
Update-MSCommerceProductPolicy -PolicyId AllowSelfServicePurchase -ProductId $product.ProductID -Enabled $false
```

## <a name="troubleshooting"></a><span data-ttu-id="61a04-155">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="61a04-155">Troubleshooting</span></span>

### <a name="problem"></a><span data-ttu-id="61a04-156">Problème</span><span class="sxs-lookup"><span data-stu-id="61a04-156">Problem</span></span>

<span data-ttu-id="61a04-157">Le message d’erreur suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="61a04-157">You see the following error message:</span></span>

> <span data-ttu-id="61a04-158">HandleError : échec de la récupération de la stratégie avec PolicyId’AllowSelfServicePurchase', ErrorMessage-la connexion sous-jacente a été fermée : une erreur inattendue s’est produite lors de l’envoi.</span><span class="sxs-lookup"><span data-stu-id="61a04-158">HandleError : Failed to retrieve policy with PolicyId 'AllowSelfServicePurchase', ErrorMessage - The underlying connection was closed: An unexpected error occurred on a send.</span></span>

<span data-ttu-id="61a04-159">Cela peut être dû à une version plus ancienne de TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="61a04-159">This may be due to an older version of Transport Layer Security (TLS).</span></span> <span data-ttu-id="61a04-160">Pour connecter ce service, vous devez utiliser TLS 1,2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="61a04-160">To connect this service you need to use TLS 1.2 or greater</span></span>

### <a name="solution"></a><span data-ttu-id="61a04-161">Solution</span><span class="sxs-lookup"><span data-stu-id="61a04-161">Solution</span></span>

<span data-ttu-id="61a04-162">Effectuez une mise à niveau vers TLS 1,2 :[https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2)</span><span class="sxs-lookup"><span data-stu-id="61a04-162">Upgrade to TLS 1.2: [https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2)</span></span>

<!--
## Uninstall the MSCommerce module

Before you uninstall the MSCommerce module, close your current PowerShell session, then open a new session with admin rights.

To remove the **MSCommerce** PowerShell module from your computer, run the following command:

```powershell
Uninstall-Module -Name MSCommerce
```-->
