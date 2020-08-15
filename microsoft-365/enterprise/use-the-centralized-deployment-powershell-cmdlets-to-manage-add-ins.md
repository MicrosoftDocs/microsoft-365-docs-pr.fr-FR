---
title: Utiliser les applets de commande PowerShell de déploiement centralisé pour gérer les compléments
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 1/24/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
- BCS160
f1.keywords:
- NOCSH
ms.assetid: 94f4e86d-b8e5-42dd-b558-e6092f830ec9
ms.custom:
- seo-marvel-apr2020
description: Utilisez les applets de commande PowerShell de déploiement centralisé pour vous aider à déployer et gérer des compléments Office pour votre organisation Microsoft 365.
ms.openlocfilehash: 659f12d2533601c4b2165a95ddbf59ea521945b8
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690105"
---
# <a name="use-the-centralized-deployment-powershell-cmdlets-to-manage-add-ins"></a><span data-ttu-id="95e62-103">Utiliser les applets de commande PowerShell de déploiement centralisé pour gérer les compléments</span><span class="sxs-lookup"><span data-stu-id="95e62-103">Use the Centralized Deployment PowerShell cmdlets to manage add-ins</span></span>

<span data-ttu-id="95e62-104">En tant qu’administrateur général Microsoft 365, vous pouvez déployer des compléments Office auprès des utilisateurs via la fonctionnalité de déploiement centralisée (consultez la rubrique [Deploy Office Add-ins in the Admin Center](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)).</span><span class="sxs-lookup"><span data-stu-id="95e62-104">As a Microsoft 365 global admin, you can deploy Office add-ins to users via the Centralized Deployment feature (see [Deploy Office Add-ins in the admin center](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)).</span></span> <span data-ttu-id="95e62-105">Outre le déploiement des compléments Office via le centre d’administration Microsoft 365, vous pouvez également utiliser Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95e62-105">In addition to deploying Office add-ins via the Microsoft 365 admin center, you can also use Microsoft PowerShell.</span></span> <span data-ttu-id="95e62-106">Installez le [module de déploiement de compléments centralisés O365 pour Windows PowerShell](https://www.powershellgallery.com/packages/O365CentralizedAddInDeployment).</span><span class="sxs-lookup"><span data-stu-id="95e62-106">Install the [O365 Centralized Add-In Deployment Module for Windows PowerShell](https://www.powershellgallery.com/packages/O365CentralizedAddInDeployment).</span></span> 

<span data-ttu-id="95e62-107">Après avoir téléchargé le module, ouvrez une fenêtre Windows PowerShell normale et exécutez l’applet de commande suivante :</span><span class="sxs-lookup"><span data-stu-id="95e62-107">After you download the module, open a regular Windows PowerShell window and run the following cmdlet:</span></span>

```powershell
 Import-Module -Name O365CentralizedAddInDeployment
```
    
## <a name="connect-using-your-admin-credentials"></a><span data-ttu-id="95e62-108">Se connecter à l’aide de vos informations d’identification d’administrateur</span><span class="sxs-lookup"><span data-stu-id="95e62-108">Connect using your admin credentials</span></span>

<span data-ttu-id="95e62-109">Avant de pouvoir utiliser les cmdlets de déploiement centralisé, vous devez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="95e62-109">Before you can use the Centralized Deployment cmdlets, you need to sign in.</span></span>
  
1. <span data-ttu-id="95e62-110">Démarrez PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95e62-110">Start PowerShell.</span></span>
    
2. <span data-ttu-id="95e62-111">Connectez-vous à PowerShell à l’aide des informations d’identification d’administrateur de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="95e62-111">Connect to PowerShell by using your company admin credentials.</span></span> <span data-ttu-id="95e62-112">Exécutez l’applet de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="95e62-112">Run the following cmdlet.</span></span>
    
  ```powershell
  Connect-OrganizationAddInService
  ```

3. <span data-ttu-id="95e62-113">Dans la page **entrer les informations d’identification** , entrez vos informations d’identification d’administrateur global Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="95e62-113">In the **Enter Credentials** page, enter your Microsoft 365 global admin credentials.</span></span> <span data-ttu-id="95e62-114">Vous pouvez également entrer vos informations d’identification directement dans l’applet de commande.</span><span class="sxs-lookup"><span data-stu-id="95e62-114">Alternately, you can enter your credentials directly into the cmdlet.</span></span> 
    
    <span data-ttu-id="95e62-115">Exécutez l’applet de commande suivante en spécifiant les informations d’identification d’administrateur de votre entreprise en tant qu’objet PSCredential.</span><span class="sxs-lookup"><span data-stu-id="95e62-115">Run the following cmdlet specifying your company admin credentials as a PSCredential object.</span></span>
    
  ```powershell
  $secpasswd = ConvertTo-SecureString "MyPassword" -AsPlainText -Force
  $mycredentials = New-Object System.Management.Automation.PSCredential ("serviceaccount@contoso.com", $secpasswd)
  Connect-OrganizationAddInService -Credential $mycredentials
  ```

> [!NOTE]
> <span data-ttu-id="95e62-116">Pour plus d’informations sur l’utilisation de PowerShell, consultez la rubrique [Connect to Microsoft 365 with PowerShell](https://go.microsoft.com/fwlink/p/?linkid=848585).</span><span class="sxs-lookup"><span data-stu-id="95e62-116">For more information about using PowerShell, see [Connect to Microsoft 365 with PowerShell](https://go.microsoft.com/fwlink/p/?linkid=848585).</span></span> 
  
## <a name="upload-an-add-in-manifest"></a><span data-ttu-id="95e62-117">Chargement d’un manifeste de complément</span><span class="sxs-lookup"><span data-stu-id="95e62-117">Upload an add-in manifest</span></span>

<span data-ttu-id="95e62-118">Exécutez la cmdlet **New-organisationcompléments-in** pour télécharger un manifeste de complément à partir d’un chemin d’accès, qui peut être un emplacement de fichier ou une URL.</span><span class="sxs-lookup"><span data-stu-id="95e62-118">Run the **New-OrganizationAdd-In** cmdlet to upload an add-in manifest from a path, which can be either a file location or URL.</span></span> <span data-ttu-id="95e62-119">L’exemple suivant montre un emplacement de fichier pour la valeur du paramètre  _ManifestPath_ .</span><span class="sxs-lookup"><span data-stu-id="95e62-119">The following example shows a file location for the value of the  _ManifestPath_ parameter.</span></span> 
  
```powershell
New-OrganizationAddIn -ManifestPath 'C:\Users\Me\Desktop\taskpane.xml' -Locale 'en-US'
```

<span data-ttu-id="95e62-120">Vous pouvez également exécuter la cmdlet **New-organisationcompléments-in** pour télécharger un complément et l’attribuer directement à des utilisateurs ou à des groupes à l’aide du paramètre  _members_ , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95e62-120">You can also run the **New-OrganizationAdd-In** cmdlet to upload an add-in and assign it to users or groups directly by using the  _Members_ parameter, as shown in the following example.</span></span> <span data-ttu-id="95e62-121">Séparez les adresses de messagerie des membres par une virgule.</span><span class="sxs-lookup"><span data-stu-id="95e62-121">Separate the email addresses of members with a comma.</span></span> 
  
```powershell
New-OrganizationAddIn -ManifestPath 'C:\Users\Me\Desktop\taskpane.xml' -Locale 'en-US' -Members  'KathyBonner@contoso.com', 'MaxHargrave@contoso.com'
```

## <a name="upload-an-add-in-from-the-office-store"></a><span data-ttu-id="95e62-122">Télécharger un complément à partir de l’Office Store</span><span class="sxs-lookup"><span data-stu-id="95e62-122">Upload an add-in from the Office Store</span></span>

<span data-ttu-id="95e62-123">Exécutez la cmdlet **New-OrganizationAddIn** pour télécharger un manifeste à partir de l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="95e62-123">Run the **New-OrganizationAddIn** cmdlet to upload a manifest from the Office Store.</span></span>
  
<span data-ttu-id="95e62-124">Dans l’exemple suivant, la cmdlet **New-OrganizationAddIn** spécifie le AssetID pour un complément pour un marché de contenu et de localisation des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="95e62-124">In the following example, the **New-OrganizationAddIn** cmdlet specifies the AssetId for an add-in for a United States location and content market.</span></span>
  
```powershell
New-OrganizationAddIn -AssetId 'WA104099688' -Locale 'en-US' -ContentMarket 'en-US'
```

<span data-ttu-id="95e62-125">Pour déterminer la valeur du paramètre  _AssetID_ , vous pouvez le copier à partir de l’URL de la page Web Office Store du complément.</span><span class="sxs-lookup"><span data-stu-id="95e62-125">To determine the value for the  _AssetId_ parameter, you can copy it from the URL of the Office Store webpage for the add-in.</span></span> <span data-ttu-id="95e62-126">AssetIds commence toujours par « WA » suivi d’un nombre.</span><span class="sxs-lookup"><span data-stu-id="95e62-126">AssetIds always begin with "WA" followed by a number.</span></span> <span data-ttu-id="95e62-127">Par exemple, dans l’exemple précédent, la source de la valeur AssetId de WA104099688 est l’URL de la page Web de l’Office Store pour le complément : [https://store.office.com/en-001/app.aspx?assetid=WA104099688](https://store.office.com/en-001/app.aspx?assetid=WA104099688) .</span><span class="sxs-lookup"><span data-stu-id="95e62-127">For example, in the previous example, the source for the AssetId value of WA104099688 is the Office Store webpage URL for the add-in: [https://store.office.com/en-001/app.aspx?assetid=WA104099688](https://store.office.com/en-001/app.aspx?assetid=WA104099688).</span></span>
  
<span data-ttu-id="95e62-128">Les valeurs des paramètres  _locale_ et  _ContentMarket_ sont identiques et indiquent le pays/la région à partir duquel vous essayez d’installer le complément.</span><span class="sxs-lookup"><span data-stu-id="95e62-128">The values for the  _Locale_ parameter and the  _ContentMarket_ parameter are identical and indicate the country/region you're trying to install the add-in from.</span></span> <span data-ttu-id="95e62-129">Le format est en-US, fr-FR.</span><span class="sxs-lookup"><span data-stu-id="95e62-129">The format is en-US, fr-FR.</span></span> <span data-ttu-id="95e62-130">et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="95e62-130">and so forth.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95e62-131">Les compléments téléchargés à partir de l’Office Store seront automatiquement mis à jour au cours des quelques jours suivant la dernière mise à jour disponible sur l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="95e62-131">Add-ins uploaded from the Office Store will update automatically within a few days of the latest update being available on the Office Store.</span></span> 
  
## <a name="get-details-of-an-add-in"></a><span data-ttu-id="95e62-132">Obtenir les détails d’un complément</span><span class="sxs-lookup"><span data-stu-id="95e62-132">Get details of an add-in</span></span>

<span data-ttu-id="95e62-133">Exécutez la cmdlet **Get-OrganizationAddIn** comme indiqué ci-dessous pour obtenir les détails de tous les compléments téléchargés vers le client, en incluant l’ID de produit d’un complément.</span><span class="sxs-lookup"><span data-stu-id="95e62-133">Run the **Get-OrganizationAddIn** cmdlet as shown below to get details of all add-ins uploaded to the tenant, included an add-in's product ID.</span></span>
  
```powershell
Get-OrganizationAddIn
```

<span data-ttu-id="95e62-134">Exécutez la cmdlet **Get-OrganizationAddIn** avec une valeur pour le paramètre  _ProductID_ afin de spécifier le complément pour lequel vous souhaitez récupérer les détails.</span><span class="sxs-lookup"><span data-stu-id="95e62-134">Run the **Get-OrganizationAddIn** cmdlet with a value for the  _ProductId_ parameter to specify which add-in you want to retrieve details for.</span></span> 
  
```powershell
Get-OrganizationAddIn -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122
```

<span data-ttu-id="95e62-135">Pour obtenir tous les détails de tous les compléments, ainsi que les utilisateurs et les groupes affectés, redirigez la sortie de la cmdlet **Get-OrganizationAddIn** vers la cmdlet Format-List, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95e62-135">To get full details of all the add-ins plus the assigned users and groups, pipe the output of the **Get-OrganizationAddIn** cmdlet to the Format-List cmdlet, as shown in the following example.</span></span>
  
```powershell
foreach($G in (Get-organizationAddIn)){Get-OrganizationAddIn -ProductId $G.ProductId | Format-List}
```

## <a name="turn-on-or-turn-off-an-add-in"></a><span data-ttu-id="95e62-136">Activation ou désactivation d’un complément</span><span class="sxs-lookup"><span data-stu-id="95e62-136">Turn on or turn off an add-in</span></span>

<span data-ttu-id="95e62-137">Pour désactiver un complément de sorte que les utilisateurs et les groupes qui lui sont attribués n’y aient plus accès, exécutez l’applet de commande **Set-OrganizationAddIn** avec le paramètre  _ProductID_ et le paramètre  _Enabled_ défini sur  `$false` , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95e62-137">To turn off an add-in so users and groups that are assigned to it will no longer have access, run the **Set-OrganizationAddIn** cmdlet with the  _ProductId_ parameter and the  _Enabled_ parameter set to  `$false`, as shown in the following example.</span></span>
  
```powershell
Set-OrganizationAddIn -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -Enabled $false
```

<span data-ttu-id="95e62-138">Pour réactiver un complément, exécutez la même applet de commande avec le paramètre  _Enabled_ défini sur  `$true` .</span><span class="sxs-lookup"><span data-stu-id="95e62-138">To turn an add-in back on, run the same cmdlet with the  _Enabled_ parameter set to  `$true`.</span></span>
  
```powershell
Set-OrganizationAddIn -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -Enabled $true
```

## <a name="add-or-remove-users-from-an-add-in"></a><span data-ttu-id="95e62-139">Ajouter ou supprimer des utilisateurs d’un complément</span><span class="sxs-lookup"><span data-stu-id="95e62-139">Add or remove users from an add-in</span></span>

<span data-ttu-id="95e62-140">Pour ajouter des utilisateurs et des groupes à un complément spécifique, exécutez l’applet de commande **Set-OrganizationAddInAssignments** avec les paramètres  _ProductID_,  _Add_et  _members_ .</span><span class="sxs-lookup"><span data-stu-id="95e62-140">To add users and groups to a specific add-in, run the **Set-OrganizationAddInAssignments** cmdlet with the  _ProductId_,  _Add_, and  _Members_ parameters.</span></span> <span data-ttu-id="95e62-141">Séparez les adresses de messagerie des membres par une virgule.</span><span class="sxs-lookup"><span data-stu-id="95e62-141">Separate the email addresses of members with a comma.</span></span> 
  
```powershell
Set-OrganizationAddInAssignments -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -Add -Members 'KathyBonner@contoso.com','sales@contoso.com'
```

<span data-ttu-id="95e62-142">Pour supprimer des utilisateurs et des groupes, exécutez la même cmdlet à l’aide du paramètre  _Remove_ .</span><span class="sxs-lookup"><span data-stu-id="95e62-142">To remove users and groups, run the same cmdlet using the  _Remove_ parameter.</span></span> 
  
```powershell
Set-OrganizationAddInAssignments -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -Remove -Members 'KathyBonner@contoso.com','sales@contoso.com'
```

<span data-ttu-id="95e62-143">Pour affecter un complément à tous les utilisateurs sur le client, exécutez la même cmdlet à l’aide du paramètre  _AssignToEveryone_ avec la valeur définie sur  `$true` .</span><span class="sxs-lookup"><span data-stu-id="95e62-143">To assign an add-in to all users on the tenant, run the same cmdlet using the  _AssignToEveryone_ parameter with the value set to  `$true`.</span></span>
  
```powershell
Set-OrganizationAddInAssignments -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -AssignToEveryone $true
```

<span data-ttu-id="95e62-144">Pour ne pas affecter un complément à tout le monde et rétablir les utilisateurs et les groupes précédemment affectés, vous pouvez exécuter la même cmdlet et désactiver le paramètre  _AssignToEveryone_ en définissant sa valeur sur  `$false` .</span><span class="sxs-lookup"><span data-stu-id="95e62-144">To not assign an add-in to everyone and revert to the previously assigned users and groups, you can run the same cmdlet and turn off the  _AssignToEveryone_ parameter by setting its value to  `$false`.</span></span>
  
```powershell
Set-OrganizationAddInAssignments -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -AssignToEveryone $false
```

## <a name="update-an-add-in"></a><span data-ttu-id="95e62-145">Mettre à jour un complément</span><span class="sxs-lookup"><span data-stu-id="95e62-145">Update an add-in</span></span>

<span data-ttu-id="95e62-146">Pour mettre à jour un complément à partir d’un manifeste, exécutez la cmdlet **Set-OrganizationAddIn** avec les paramètres  _ProductID_,  _ManifestPath_et  _locale_ , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95e62-146">To update an add-in from a manifest, run the **Set-OrganizationAddIn** cmdlet with the  _ProductId_,  _ManifestPath_, and  _Locale_ parameters, as shown in the following example.</span></span> 
  
```powershell
Set-OrganizationAddIn -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122 -ManifestPath 'C:\Users\Me\Desktop\taskpane.xml' -Locale 'en-US'
```

> [!NOTE]
> <span data-ttu-id="95e62-147">Les compléments téléchargés à partir de l’Office Store seront automatiquement mis à jour au cours des quelques jours suivant la dernière mise à jour disponible sur l’Office Store.</span><span class="sxs-lookup"><span data-stu-id="95e62-147">Add-ins uploaded from the Office Store will update automatically within a few days of the latest update being available on the Office Store.</span></span> 
  
## <a name="delete-an-add-in"></a><span data-ttu-id="95e62-148">Suppression d’un complément</span><span class="sxs-lookup"><span data-stu-id="95e62-148">Delete an add-in</span></span>

<span data-ttu-id="95e62-149">Pour supprimer un complément, exécutez l’applet de commande **Remove-OrganizationAddIn** avec le paramètre  _ProductID_ , comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="95e62-149">To delete an add-in, run the **Remove-OrganizationAddIn** cmdlet with the  _ProductId_ parameter, as shown in the following example.</span></span> 
  
```powershell
Remove-OrganizationAddIn -ProductId 6a75788e-1c6b-4e9b-b5db-5975a2072122
```

<!--
## Customize Microsoft Store add-ins for your organization

You must customize the add-in before you deploy it to your organization. Add-ins older than version 1.1 are not supported by this feature. 

We recommend that you deploy a customized add-in  to yourself first to make sure it works as expected before you deploy it to your entire organization.

Note also the following restrictions:
- All URLs must be absolute (include http or https) and valid.
- *DisplayName* must not exceed 125 characters 
- *DisplayName*, *Resources* and *AppDomains* must not include the following characters: 
 
    - \<
    -  \>
    -  ;
    -  =   

If you want to customize an add-in that has been deployed, you have to uninstall it in the admin center, and see [remove an add-in from local cache](#remove-an-add-in-from-local-cache) for steps to remove it from each computer it has been deployed to.

To customize an add-in, run the **Set –OrganizationAddInOverrides** cmdlet with the *ProductId* as a parameter, followed by the tag you want to overwrite and the new value. To find out how to get the *ProductId* see [get details of an add-in](#get-details-of-an-add-in) in this article. For example:

```powershell
 Set-OrganizationAddInOverrides -ProductId 5b31b349-2c41-4f94-b720-6ee40349d391 -IconUrl "https://site.com/img.jpg" 
```
To customize multiple tags for an add-in, add those tags to the commandline:

```powershell
Set-OrganizationAddInOverrides -ProductId 5b31b349-2c41-4f94-b720-6ee40349d391 -Hosts h1, 2 -DisplayName "New DocuSign W" -IconUrl "https://site.com/img.jpg" 
```

> [!IMPORTANT]
> You must apply multiple customized tags to one add-in as one command. If you customize tags one by one, only the last customization will be applied. Additionally, if you customize a tag by mistake, you must remove all customizations and start over.

### Tags you can customize

| Tag                  | Description          |
| :------------------- | :------------------- |
| \<IconURL>   </br>| The URL of the image used as the add-in’s icon (in admin center). </br> |
| \<DisplayName>| The title of the add-in  (in admin center).|
| \<Hosts>| List of apps that will support the add-in.|
| \<SourceLocation> | The source URL that the add-in will connect to.| 
| \<AppDomains> | A list of domains that the add-in can connect with. | 
| \<SupportURL>| The URL users can use to access help and support. | 
| \<Resources>  | This tag contains a number of elements including titles, tooltips, and icons of different sizes.| 
|
### Customize Resources tag

Any element in the <Resources> tag of the manifest can be customized dynamically. You first need to check the manifest to find the element id to which you want to assign a new value. The <Resources> tag looks like this:

```
<Resources>  
    <bt:Images> 
          <bt:Image id=”img16icon” DefaultValue=”https://site.com/img.jpg” 
    </bt:Images> 
</Resources> 
``` 
In this case, the element id for the image is “img16icon” and the value associated with it is “http:<i></i>//site.<i></i>com/img.jpg.”

Once you have identified the elements you want to customize, use the following command in Powershell to assign new values to the elements:

```powershell
Set-OrganizationAddInOverrides -Resources @{“ElementID” = “New Value”; “NextElementID” = “Next New Value”} 
```

You can customize as many elements with the command as you need to.

### Remove customization from an add-in

The only option currently available for deleting customizations is to delete all of them at once:

```powershell
Remove-OrganizationAddInOverrides -ProductId 5b31b349-2c41-4f94-b720-6ee40349d391 
```

### View add-in customizations

To view a list of applied customizations, run the **Get-OrganizationAddInOverrides** cmdlet. If **Get-OrganizationAddInOverrides** is run without a *ProductId* then a list of all add-ins with applied overrides are returned.  

```powershell
Get-OrganizationAddInOverrides 
```
If ProductId is specified, then a list of overrides applied to that add-in is returned. 

```powershell
Get-OrganizationAddInOverrides -ProductId 5b31b349-2c41-4f94-b720-6ee40349d391 
```

### Remove an add-in from local cache

If an add-in has been deployed, it has to be removed from the cache in each computer before it can be customized. To remive an add-in from cache:

1. Navigate to the “Users” folder in C:\ 
1. Go to your user folder
1. Navigate to AppData\Local\Microsoft\Office and select the folder associated with your version of Office
1. In the *Wef* folder delete the *Manifests* folder.

-->

## <a name="get-detailed-help-for-each-cmdlet"></a><span data-ttu-id="95e62-150">Obtenir de l’aide détaillée pour chaque cmdlet</span><span class="sxs-lookup"><span data-stu-id="95e62-150">Get detailed help for each cmdlet</span></span>

<span data-ttu-id="95e62-151">Vous pouvez consulter l’aide détaillée pour chaque cmdlet à l’aide de la cmdlet Get-Help.</span><span class="sxs-lookup"><span data-stu-id="95e62-151">You can look at detailed help for each cmdlet by using the Get-help cmdlet.</span></span> <span data-ttu-id="95e62-152">Par exemple, l’applet de commande suivante fournit des informations détaillées sur la cmdlet Remove-OrganizationAddIn.</span><span class="sxs-lookup"><span data-stu-id="95e62-152">For example, the following cmdlet provides detailed information about the Remove-OrganizationAddIn cmdlet.</span></span>
  
```powershell
Get-help Remove-OrganizationAddIn -Full
```


