---
title: Afficher les licences et services Microsoft 365 avec PowerShell
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 07/17/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
f1.keywords:
- CSH
ms.custom:
- Ent_Office_Other
- O365ITProTrain
- LIL_Placement
- PowerShell
ms.assetid: bb5260a9-a6a3-4f34-b19a-06c6699f6723
description: Explique comment utiliser PowerShell pour afficher des informations sur les plans de gestion des licences, les services et les licences disponibles dans votre organisation Microsoft 365.
ms.openlocfilehash: 08f48301001ee6a40318428f3310eab8b0d0a351
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50924635"
---
# <a name="view-microsoft-365-licenses-and-services-with-powershell"></a><span data-ttu-id="bf6d3-103">Afficher les licences et services Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf6d3-103">View Microsoft 365 licenses and services with PowerShell</span></span>

<span data-ttu-id="bf6d3-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="bf6d3-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="bf6d3-105">Chaque abonnement Microsoft 365 comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-105">Every Microsoft 365 subscription consists of the following elements:</span></span>

- <span data-ttu-id="bf6d3-106">**Plans de gestion des licences** Ces plans sont également appelés plans de licence ou plans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-106">**Licensing plans** These are also known as license plans or Microsoft 365 plans.</span></span> <span data-ttu-id="bf6d3-107">Les plans de gestion des licences définissent les services Microsoft 365 disponibles pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-107">Licensing plans define the Microsoft 365 services that are available to users.</span></span> <span data-ttu-id="bf6d3-108">Votre abonnement Microsoft 365 peut contenir plusieurs plans de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-108">Your Microsoft 365 subscription may contain multiple licensing plans.</span></span> <span data-ttu-id="bf6d3-109">Microsoft 365 E3 est un exemple de plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-109">An example licensing plan would be Microsoft 365 E3.</span></span>
    
- <span data-ttu-id="bf6d3-110">**Services** Ces plans sont également appelés plans de service.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-110">**Services** These are also known as service plans.</span></span> <span data-ttu-id="bf6d3-111">Les services sont les produits, fonctionnalités et fonctionnalités Microsoft 365 disponibles dans chaque plan de gestion des licences, par exemple, Exchange Online et Microsoft 365 Apps for enterprise (précédemment nommé Office 365 ProPlus).</span><span class="sxs-lookup"><span data-stu-id="bf6d3-111">Services are the Microsoft 365 products, features, and capabilities that are available in each licensing plan, for example, Exchange Online and Microsoft 365 Apps for enterprise (previously named Office 365 ProPlus).</span></span> <span data-ttu-id="bf6d3-112">Des licences issues de différents plans de licence peuvent être attribuées à un même utilisateur, lui accordant l’accès à des services différents.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-112">Users can have multiple licenses assigned to them from different licensing plans that grant access to different services.</span></span>
    
- <span data-ttu-id="bf6d3-113">**Licences** Chaque plan de gestion des licences contient le nombre de licences que vous avez achetées.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-113">**Licenses** Each licensing plan contains the number of licenses that you purchased.</span></span> <span data-ttu-id="bf6d3-114">Vous attribuez des licences aux utilisateurs afin qu’ils peuvent utiliser les services Microsoft 365 définis par le plan de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-114">You assign licenses to users so they can use the Microsoft 365 services that are defined by the licensing plan.</span></span> <span data-ttu-id="bf6d3-115">Chaque compte d’utilisateur nécessite au moins une licence d’un plan de gestion des licences pour pouvoir se connecter à Microsoft 365 et utiliser les services.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-115">Every user account requires at least one license from one licensing plan so they can log on to Microsoft 365 and use the services.</span></span>
    
<span data-ttu-id="bf6d3-116">Vous pouvez utiliser PowerShell pour Microsoft 365 pour afficher des détails sur les plans de gestion des licences, les licences et les services disponibles dans votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-116">You can use PowerShell for Microsoft 365 to view details about the available licensing plans, licenses, and services in your Microsoft 365 organization.</span></span> <span data-ttu-id="bf6d3-117">Pour plus d’informations sur les produits, fonctionnalités et services disponibles dans différents abonnements Office 365, voir Options de plan [Office 365.](/office365/servicedescriptions/office-365-platform-service-description/office-365-plan-options)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-117">For more information about the products, features, and services that are available in different Office 365 subscriptions, see [Office 365 Plan Options](/office365/servicedescriptions/office-365-platform-service-description/office-365-plan-options).</span></span>


## <a name="use-the-azure-active-directory-powershell-for-graph-module"></a><span data-ttu-id="bf6d3-118">Utilisation du module Azure Active Directory PowerShell pour Graph</span><span class="sxs-lookup"><span data-stu-id="bf6d3-118">Use the Azure Active Directory PowerShell for Graph module</span></span>

<span data-ttu-id="bf6d3-119">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-119">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="bf6d3-120">Pour afficher des informations récapitulatifs sur vos plans de gestion des licences actuels et les licences disponibles pour chaque plan, exécutez la commande ci-après :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-120">To view summary information about your current licensing plans and the available licenses for each plan, run this command:</span></span>
  
```powershell
Get-AzureADSubscribedSku | Select -Property Sku*,ConsumedUnits -ExpandProperty PrepaidUnits
```

<span data-ttu-id="bf6d3-121">Les résultats contiennent :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-121">The results contain:</span></span>
  
- <span data-ttu-id="bf6d3-122">**SkuPartNumber :** Affiche les plans de gestion des licences disponibles pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-122">**SkuPartNumber:** Shows the available licensing plans for your organization.</span></span> <span data-ttu-id="bf6d3-123">Par exemple, `ENTERPRISEPACK` est le nom du plan de licence pour Office 365 Entreprise E3.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-123">For example, `ENTERPRISEPACK` is the license plan name for Office 365 Enterprise E3.</span></span>
    
- <span data-ttu-id="bf6d3-124">**Activé :** Nombre de licences que vous avez achetées pour un plan de gestion des licences spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-124">**Enabled:** Number of licenses that you've purchased for a specific licensing plan.</span></span>
    
- <span data-ttu-id="bf6d3-125">**ConsumedUnits :** Nombre de licences que vous avez attribuées à des utilisateurs à partir d’un plan de gestion des licences spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-125">**ConsumedUnits:** Number of licenses that you've assigned to users from a specific licensing plan.</span></span>
    
<span data-ttu-id="bf6d3-126">Pour afficher des détails sur les services Microsoft 365 disponibles dans tous vos plans de licence, affichez d’abord la liste de vos plans de licence.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-126">To view details about the Microsoft 365 services that are available in all of your license plans, first display a list of your license plans.</span></span>

```powershell
Get-AzureADSubscribedSku | Select SkuPartNumber
```

<span data-ttu-id="bf6d3-127">Ensuite, stockez les informations des plans de licence dans une variable.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-127">Next, store the license plans information in a variable.</span></span>

```powershell
$licenses = Get-AzureADSubscribedSku
```

<span data-ttu-id="bf6d3-128">Ensuite, affichez les services dans un plan de licence spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-128">Next, display the services in a specific license plan.</span></span>

```powershell
$licenses[<index>].ServicePlans
```

<span data-ttu-id="bf6d3-129">\<index> est un nombre total qui spécifie le numéro de ligne du plan de licence à partir de l’affichage de la `Get-AzureADSubscribedSku | Select SkuPartNumber` commande, moins 1.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-129">\<index> is an integer that specifies the row number of the license plan from the display of the `Get-AzureADSubscribedSku | Select SkuPartNumber` command, minus 1.</span></span>

<span data-ttu-id="bf6d3-130">Par exemple, si l’affichage de la `Get-AzureADSubscribedSku | Select SkuPartNumber` commande est le cas :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-130">For example, if the display of the `Get-AzureADSubscribedSku | Select SkuPartNumber` command is this:</span></span>

```powershell
SkuPartNumber
-------------
WIN10_VDA_E5
EMSPREMIUM
ENTERPRISEPREMIUM
FLOW_FREE
```

<span data-ttu-id="bf6d3-131">Ensuite, la commande d’affichage des services pour le plan de licence ENTERPRISEPREMIUM est la :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-131">Then the command to display the services for the ENTERPRISEPREMIUM license plan is this:</span></span>

```powershell
$licenses[2].ServicePlans
```

<span data-ttu-id="bf6d3-132">ENTERPRISEPREMIUM est la troisième ligne.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-132">ENTERPRISEPREMIUM is the third row.</span></span> <span data-ttu-id="bf6d3-133">Par conséquent, la valeur d’index est (3 - 1) ou 2.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-133">Therefore, the index value is (3 - 1), or 2.</span></span>

<span data-ttu-id="bf6d3-134">Pour obtenir la liste complète des plans de licence (également appelés noms de produits), leurs plans de service inclus et leurs noms convivial correspondants, voir Noms de produits et identificateurs de plan de service pour la [gestion des licences.](/azure/active-directory/users-groups-roles/licensing-service-plan-reference)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-134">For a complete list of license plans (also known as product names), their included service plans, and their corresponding friendly names, see [Product names and service plan identifiers for licensing](/azure/active-directory/users-groups-roles/licensing-service-plan-reference).</span></span>

## <a name="use-the-microsoft-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="bf6d3-135">Utilisez le module Microsoft Azure Active Directory pour Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-135">Use the Microsoft Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="bf6d3-136">Tout [d’abord, connectez-vous à votre client Microsoft 365.](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-136">First, [connect to your Microsoft 365 tenant](connect-to-microsoft-365-powershell.md#connect-with-the-microsoft-azure-active-directory-module-for-windows-powershell).</span></span>

>[!Note]
><span data-ttu-id="bf6d3-137">Un script PowerShell est disponible pour automatiser les procédures décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-137">A PowerShell script is available that automates the procedures described in this topic.</span></span> <span data-ttu-id="bf6d3-138">Plus précisément, le script vous permet d’afficher et de désactiver des services dans votre organisation Microsoft 365, y compris Sway.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-138">Specifically, the script lets you view and disable services in your Microsoft 365 organization, including Sway.</span></span> <span data-ttu-id="bf6d3-139">Pour plus d’informations, voir [Désactiver l’accès à Sway avec PowerShell.](disable-access-to-sway-with-microsoft-365-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-139">For more information, see [Disable access to Sway with PowerShell](disable-access-to-sway-with-microsoft-365-powershell.md).</span></span>
>
    
<span data-ttu-id="bf6d3-140">Pour afficher des informations récapitulatifs sur vos plans de gestion des licences actuels et les licences disponibles pour chaque plan, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-140">To view summary information about your current licensing plans and the available licenses for each plan, run the following command:</span></span>
  
```powershell
Get-MsolAccountSku
```

>[!Note]
><span data-ttu-id="bf6d3-141">PowerShell Core ne prend pas en charge le module Microsoft Azure Active Directory pour Windows PowerShell et les applets de commande incluant **Msol** dans leur nom.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-141">PowerShell Core does not support the Microsoft Azure Active Directory Module for Windows PowerShell module and cmdlets with **Msol** in their name.</span></span> <span data-ttu-id="bf6d3-142">Pour continuer à utiliser ces applets de commande, vous devez les exécuter à partir de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-142">To continue using these cmdlets, you must run them from Windows PowerShell.</span></span>
>

<span data-ttu-id="bf6d3-143">Les résultats contiennent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-143">The results contain the following information:</span></span>
  
- <span data-ttu-id="bf6d3-144">**AccountSkuId :** Affichez les plans de gestion des licences disponibles pour votre organisation à l’aide de la `<CompanyName>:<LicensingPlan>` syntaxe.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-144">**AccountSkuId:** Show the available licensing plans for your organization by using the syntax `<CompanyName>:<LicensingPlan>`.</span></span>  <span data-ttu-id="bf6d3-145">_\<CompanyName>_ est la valeur que vous avez fournie lorsque vous vous êtes inscrit à Microsoft 365 et est unique pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-145">_\<CompanyName>_ is the value that you provided when you enrolled in Microsoft 365, and is unique for your organization.</span></span> <span data-ttu-id="bf6d3-146">La _\<LicensingPlan>_ valeur est la même pour tout le monde.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-146">The _\<LicensingPlan>_ value is the same for everyone.</span></span> <span data-ttu-id="bf6d3-147">Par exemple, dans la valeur , le nom de la société est et le nom du plan de gestion des licences, qui est le nom du système `litwareinc:ENTERPRISEPACK`  `litwareinc` pour Office  `ENTERPRISEPACK` 365 Entreprise E3.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-147">For example, in the value `litwareinc:ENTERPRISEPACK`, the company name is  `litwareinc`, and the licensing plan name  `ENTERPRISEPACK`, which is the system name for Office 365 Enterprise E3.</span></span>
    
- <span data-ttu-id="bf6d3-148">**ActiveUnits :** Nombre de licences que vous avez achetées pour un plan de gestion des licences spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-148">**ActiveUnits:** Number of licenses that you've purchased for a specific licensing plan.</span></span>
    
- <span data-ttu-id="bf6d3-149">**WarningUnits :** Nombre de licences dans un plan de gestion des licences que vous n’avez pas renouvelé et qui expireront après la période de grâce de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-149">**WarningUnits:** Number of licenses in a licensing plan that you haven't renewed, and that will expire after the 30-day grace period.</span></span>
    
- <span data-ttu-id="bf6d3-150">**ConsumedUnits :** Nombre de licences que vous avez attribuées à des utilisateurs à partir d’un plan de gestion des licences spécifique.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-150">**ConsumedUnits:** Number of licenses that you've assigned to users from a specific licensing plan.</span></span>
    
<span data-ttu-id="bf6d3-151">Pour afficher des détails sur les services Microsoft 365 disponibles dans tous vos plans de licence, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="bf6d3-151">To view details about the Microsoft 365 services that are available in all of your license plans, run the following command:</span></span>
  
```powershell
Get-MsolAccountSku | Select -ExpandProperty ServiceStatus
```

<span data-ttu-id="bf6d3-152">Le tableau suivant présente les plans de service Microsoft 365 et leurs noms convivial pour les services les plus courants.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-152">The following table shows the Microsoft 365 service plans and their friendly names for the most common services.</span></span> <span data-ttu-id="bf6d3-153">La liste de vos plans de services peut être différente.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-153">Your list of service plans might be different.</span></span> 
  
|<span data-ttu-id="bf6d3-154">**Plan de services**</span><span class="sxs-lookup"><span data-stu-id="bf6d3-154">**Service plan**</span></span>|<span data-ttu-id="bf6d3-155">**Description**</span><span class="sxs-lookup"><span data-stu-id="bf6d3-155">**Description**</span></span>|
|:-----|:-----|
| `SWAY` <br/> |<span data-ttu-id="bf6d3-156">Sway</span><span class="sxs-lookup"><span data-stu-id="bf6d3-156">Sway</span></span>  <br/> |
| `TEAMS1` <br/> |<span data-ttu-id="bf6d3-157">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bf6d3-157">Microsoft Teams</span></span>  <br/> |
| `YAMMER_ENTERPRISE` <br/> |<span data-ttu-id="bf6d3-158">Yammer</span><span class="sxs-lookup"><span data-stu-id="bf6d3-158">Yammer</span></span>  <br/> |
| `RMS_S_ENTERPRISE` <br/> |<span data-ttu-id="bf6d3-159">Azure Rights Management (RMS)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-159">Azure Rights Management (RMS)</span></span>  <br/> |
| `OFFICESUBSCRIPTION` <br/> |<span data-ttu-id="bf6d3-160">Applications Microsoft 365 pour les entreprises *(précédemment nommé Office 365 ProPlus)*</span><span class="sxs-lookup"><span data-stu-id="bf6d3-160">Microsoft 365 Apps for enterprise *(previously named Office 365 ProPlus)*</span></span>  <br/> |
| `MCOSTANDARD` <br/> |<span data-ttu-id="bf6d3-161">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="bf6d3-161">Skype for Business Online</span></span>  <br/> |
| `SHAREPOINTWAC` <br/> |<span data-ttu-id="bf6d3-162">Office</span><span class="sxs-lookup"><span data-stu-id="bf6d3-162">Office</span></span>  <br/> |
| `SHAREPOINTENTERPRISE` <br/> |<span data-ttu-id="bf6d3-163">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="bf6d3-163">SharePoint Online</span></span>  <br/> |
| `EXCHANGE_S_ENTERPRISE` <br/> |<span data-ttu-id="bf6d3-164">Exchange Online (plan 2)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-164">Exchange Online Plan 2</span></span>  <br/> |
   
<span data-ttu-id="bf6d3-165">Pour obtenir la liste complète des plans de licence (également appelés noms de produits), leurs plans de service inclus et leurs noms convivial correspondants, voir Noms de produits et identificateurs de plan de service pour la [gestion des licences.](/azure/active-directory/users-groups-roles/licensing-service-plan-reference)</span><span class="sxs-lookup"><span data-stu-id="bf6d3-165">For a complete list of license plans (also known as product names), their included service plans, and their corresponding friendly names, see [Product names and service plan identifiers for licensing](/azure/active-directory/users-groups-roles/licensing-service-plan-reference).</span></span>

<span data-ttu-id="bf6d3-166">Pour afficher des détails sur les services Microsoft 365 disponibles dans un plan de gestion des licences spécifique, utilisez la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="bf6d3-166">To view details about the Microsoft 365 services that are available in a specific licensing plan, use the following syntax.</span></span>
  
```powershell
(Get-MsolAccountSku | where {$_.AccountSkuId -eq "<AccountSkuId>"}).ServiceStatus
```

<span data-ttu-id="bf6d3-167">Cet exemple montre les services disponibles dans le plan de gestion des licences litwareinc:ENTERPRISEPACK (Office 365 Entreprise E3).</span><span class="sxs-lookup"><span data-stu-id="bf6d3-167">This example shows the services that are available in the litwareinc:ENTERPRISEPACK (Office 365 Enterprise E3) licensing plan.</span></span>
  
```powershell
(Get-MsolAccountSku | where {$_.AccountSkuId -eq "litwareinc:ENTERPRISEPACK"}).ServiceStatus
```

## <a name="see-also"></a><span data-ttu-id="bf6d3-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf6d3-168">See also</span></span>

[<span data-ttu-id="bf6d3-169">Gérer les comptes d’utilisateurs, les licences et les groupes Microsoft 365 avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf6d3-169">Manage Microsoft 365 user accounts, licenses, and groups with PowerShell</span></span>](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="bf6d3-170">Gestion de Microsoft 365 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf6d3-170">Manage Microsoft 365 with PowerShell</span></span>](manage-microsoft-365-with-microsoft-365-powershell.md)
  
[<span data-ttu-id="bf6d3-171">Prise en main de PowerShell pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bf6d3-171">Getting started with PowerShell for Microsoft 365</span></span>](getting-started-with-microsoft-365-powershell.md)