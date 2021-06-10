---
title: Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Informations supplémentaires sur les appareils sur les services lors du passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) à Office 365 services dans la nouvelle région de centres de données allemande.'
ms.openlocfilehash: 21188372f03af394fe1c0e227c1adeabbad02a85
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50928155"
---
# <a name="additional-device-information-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="be4c9-103">Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="be4c9-103">Additional device information for the migration from Microsoft Cloud Deutschland</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="be4c9-104">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="be4c9-104">Frequently asked questions</span></span>

<span data-ttu-id="be4c9-105">**Comment savoir si mon organisation est affectée ?**</span><span class="sxs-lookup"><span data-stu-id="be4c9-105">**How can I tell if my organization is affected?**</span></span>

<span data-ttu-id="be4c9-106">Les administrateurs doivent `https://portal.microsoftazure.de` vérifier s’ils ont des appareils enregistrés.</span><span class="sxs-lookup"><span data-stu-id="be4c9-106">Administrators should check `https://portal.microsoftazure.de` to determine if they have any registered devices.</span></span> <span data-ttu-id="be4c9-107">Si votre organisation dispose d’appareils inscrits, vous êtes affecté.</span><span class="sxs-lookup"><span data-stu-id="be4c9-107">If your organization has registered devices, you're affected.</span></span>

<span data-ttu-id="be4c9-108">**Quel est l’impact sur mes utilisateurs ?**</span><span class="sxs-lookup"><span data-stu-id="be4c9-108">**What is the impact on my users?**</span></span>

<span data-ttu-id="be4c9-109">Les utilisateurs d’un appareil enregistré ne pourront plus se connecter une fois votre migration entrée dans la phase finaliser la migration [Azure AD.](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span><span class="sxs-lookup"><span data-stu-id="be4c9-109">Users from a registered device will no longer be able to sign in after your migration enters the [Finalize Azure AD](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>  

<span data-ttu-id="be4c9-110">Assurez-vous que tous vos appareils sont enregistrés auprès du point de terminaison mondial avant que votre organisation ne soit déconnectée de Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="be4c9-110">Ensure that all of your devices are registered with the worldwide endpoint before your organization is disconnected from Microsoft Cloud Deutschland.</span></span>
  
<span data-ttu-id="be4c9-111">**Quand mes utilisateurs ré-inscrivent-ils leurs appareils ?**</span><span class="sxs-lookup"><span data-stu-id="be4c9-111">**When do my users re-register their devices?**</span></span>

<span data-ttu-id="be4c9-112">Pour réussir, vous devez uniquement désins inscrire et réenregistrer vos appareils lors de la phase de migration Distinct [de Microsoft Cloud Deutschland.](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span><span class="sxs-lookup"><span data-stu-id="be4c9-112">It's critical to your success that you only unregister and re-register your devices during the [Separate from Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>

<span data-ttu-id="be4c9-113">**Comment restaurer l’état de mon appareil après la migration ?**</span><span class="sxs-lookup"><span data-stu-id="be4c9-113">**How do I restore my device state after migration?**</span></span>

<span data-ttu-id="be4c9-114">Pour les appareils Windows hybrides joints à Azure AD et d’entreprise inscrits auprès d’Azure AD, les administrateurs pourront gérer la migration de ces appareils via des flux de travail déclenchés à distance qui désinsèreront les anciens états d’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-114">For hybrid Azure AD–joined and company-owned Windows devices that are registered with Azure AD, administrators will be able to manage the migration of these devices through remotely triggered workflows that will unregister the old device states.</span></span>
  
<span data-ttu-id="be4c9-115">Pour tous les autres appareils, y compris les appareils Windows personnels enregistrés dans Azure AD, l’utilisateur final doit effectuer ces étapes manuellement.</span><span class="sxs-lookup"><span data-stu-id="be4c9-115">For all other devices, including personal Windows devices that are registered in Azure AD, the end user must perform these steps manually.</span></span> <span data-ttu-id="be4c9-116">Pour les appareils joints à Azure AD, les utilisateurs doivent avoir un compte d’administrateur local pour se désins inscrire, puis réenregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="be4c9-116">For Azure AD–joined devices, users need to have a local administrator account to unregister and then re-register their devices.</span></span>

<span data-ttu-id="be4c9-117">Microsoft publiera des instructions sur la restauration de l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-117">Microsoft will publish instructions for how to successfully restore device state.</span></span> 
 
<span data-ttu-id="be4c9-118">**Comment savoir que tous mes appareils sont inscrits dans le cloud public ?**</span><span class="sxs-lookup"><span data-stu-id="be4c9-118">**How do I know that all my devices are registered in the public cloud?**</span></span>

<span data-ttu-id="be4c9-119">Pour vérifier si vos appareils sont enregistrés dans le cloud public, vous devez exporter et télécharger la liste des appareils à partir du portail Azure AD vers une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="be4c9-119">To check whether your devices are registered in the public cloud, you should export and download the list of devices from the Azure AD portal to an Excel spreadsheet.</span></span> <span data-ttu-id="be4c9-120">Ensuite, filtrez les appareils inscrits (à l’aide de la colonne _registeredTime)_ après la phase de migration Distinct [de Microsoft Cloud Deutschland.](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span><span class="sxs-lookup"><span data-stu-id="be4c9-120">Then, filter the devices that are registered (by using the _registeredTime_ column) after the [Separate from Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>

<span data-ttu-id="be4c9-121">L’inscription de l’appareil est désactivée après la migration du client et ne peut pas être activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="be4c9-121">Device registration is deactivated after migration of the tenant and cannot be enabled or disabled.</span></span> <span data-ttu-id="be4c9-122">Si Intune n’est pas utilisé, connectez-vous à votre abonnement et exécutez cette commande pour réactiver l’option :</span><span class="sxs-lookup"><span data-stu-id="be4c9-122">If Intune is not used, sign in to your subscription and run this command to re-activate the option:</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```

## <a name="hybrid-azure-ad-join"></a><span data-ttu-id="be4c9-123">Jonction Azure AD Hybride</span><span class="sxs-lookup"><span data-stu-id="be4c9-123">Hybrid Azure AD join</span></span>

### <a name="windows-down-level"></a><span data-ttu-id="be4c9-124">Windows niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="be4c9-124">Windows down-level</span></span>

<span data-ttu-id="be4c9-125">_Windows_ de niveau inférieur sont des appareils Windows qui exécutent actuellement des versions antérieures de Windows (comme Windows 8.1 ou Windows 7) ou qui exécutent des versions de Windows Server antérieures à 2019 et 2016.</span><span class="sxs-lookup"><span data-stu-id="be4c9-125">_Windows down-level devices_ are Windows devices that currently run earlier versions of Windows (such as Windows 8.1 or Windows 7), or that run Windows Server versions earlier than 2019 and 2016.</span></span> <span data-ttu-id="be4c9-126">Si ces appareils ont été enregistrés auparavant, vous devez les désins inscrire et les réins inscrire.</span><span class="sxs-lookup"><span data-stu-id="be4c9-126">If such devices were registered before, you'll need to unregister and re-register those devices.</span></span> 

<span data-ttu-id="be4c9-127">Pour déterminer si un Windows niveau inférieur a été précédemment joint à Azure AD, utilisez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="be4c9-127">To determine whether a Windows down-level device was previously joined to Azure AD, use following command on the device:</span></span>

```console
%programfiles%\Microsoft Workplace Join\autoworkplace /status
```

<span data-ttu-id="be4c9-128">Si l’appareil a été précédemment joint à Azure AD et si l’appareil dispose d’une connectivité réseau aux points de terminaison Azure AD globaux, vous verrez le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="be4c9-128">If the device was previously joined to Azure AD, and if the device has network connectivity to global Azure AD endpoints, you would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| Device Details                                                       |
+----------------------------------------------------------------------+
         DeviceId : AEE2B956-DA62-48D0-BB47-046DD992A110
       Thumbprint : 00fdfa2de5c32feae57489873a13aa6a3ff7433b
             User : user1@<tenantname>.de
Private key state : Okay
     Device state : Unknown
```

<span data-ttu-id="be4c9-129">Les appareils concernés auront l'« état de l’appareil » avec la valeur « Unknown ».</span><span class="sxs-lookup"><span data-stu-id="be4c9-129">The affected devices will have the "Device state" with value of "Unknown".</span></span> <span data-ttu-id="be4c9-130">Si la sortie est « Appareil non joint » ou dont la valeur « État de l’appareil » est « OK », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="be4c9-130">If the output is "Device not joined" or whose "Device state" value is "Okay", ignore the following guidance.</span></span>

<span data-ttu-id="be4c9-131">Uniquement pour les appareils qui indiquent que l’appareil est joint (en raison de deviceId, de l’empreinte numérique, et ainsi de suite) et dont la valeur « État de l’appareil » est « Inconnu », les administrateurs doivent exécuter la commande suivante dans le contexte d’un utilisateur de domaine qui se connecté sur un appareil de niveau inférieur :</span><span class="sxs-lookup"><span data-stu-id="be4c9-131">Only for devices that show that the device is joined (by virtue of deviceId, thumbprint, and so on) and whose "Device state" value is "Unknown", admins should run the following command in the context of a domain user signing in on such a down-level device:</span></span>

```console
"%programfiles%\Microsoft Workplace Join\autoworkplace /leave"
```

<span data-ttu-id="be4c9-132">La commande précédente ne doit être exécuté qu’une seule fois par utilisateur de domaine qui se Windows sur l’appareil de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="be4c9-132">The preceding command only needs to be run once per domain user signing in on the Windows down-level device.</span></span> <span data-ttu-id="be4c9-133">Cette commande doit être exécuté dans le contexte de la signature de l’utilisateur du domaine.</span><span class="sxs-lookup"><span data-stu-id="be4c9-133">This command should be run in the context of the domain user signing in.</span></span> 

<span data-ttu-id="be4c9-134">Une attention suffisante doit être prise pour ne pas exécuter cette commande lorsque l’utilisateur se signe par la suite.</span><span class="sxs-lookup"><span data-stu-id="be4c9-134">Sufficient care must be taken to not run this command when the user subsequently signs in.</span></span> <span data-ttu-id="be4c9-135">Lorsque la commande précédente s’exécute, elle effacera l’état joint de l’ordinateur hybride local joint à Azure AD pour l’utilisateur qui s’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="be4c9-135">When the preceding command runs, it will clear the joined state of the local hybrid Azure AD–joined computer for the user who signed in.</span></span> <span data-ttu-id="be4c9-136">De plus, si l’ordinateur est toujours configuré pour être joint à Azure AD hybride dans le client, il tentera d’y participer lorsque l’utilisateur se joindra à nouveau.</span><span class="sxs-lookup"><span data-stu-id="be4c9-136">And, if the computer is still configured to be hybrid Azure AD–joined in the tenant, it will attempt to join when the user signs in again.</span></span>

### <a name="windows-current"></a><span data-ttu-id="be4c9-137">Windows Actuel</span><span class="sxs-lookup"><span data-stu-id="be4c9-137">Windows Current</span></span>

#### <a name="unjoin"></a><span data-ttu-id="be4c9-138">Unjoin</span><span class="sxs-lookup"><span data-stu-id="be4c9-138">Unjoin</span></span>

<span data-ttu-id="be4c9-139">Pour déterminer si l’Windows 10 a été précédemment joint à Azure AD, exécutez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="be4c9-139">To determine whether the Windows 10 device was previously joined to Azure AD, run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="be4c9-140">Si l’appareil est joint à Azure AD hybride, l’administrateur voit le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="be4c9-140">If the device is hybrid Azure AD–joined, the admin would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| Device State                                                         |
+----------------------------------------------------------------------+
 
             AzureAdJoined : YES
          EnterpriseJoined : NO
              DomainJoined : YES
```

<span data-ttu-id="be4c9-141">Si la sortie est « AzureAdJoined : Non », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="be4c9-141">If the output is "AzureAdJoined : No", ignore the following guidance.</span></span>

<span data-ttu-id="be4c9-142">Uniquement pour les appareils qui indiquent que l’appareil est joint à Azure AD, exécutez la commande suivante en tant qu’administrateur pour supprimer l’état joint de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-142">Only for devices that show that the device is joined to Azure AD, run the following command as an admin to remove the joined state of the device.</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /leave
```

<span data-ttu-id="be4c9-143">La commande précédente ne doit être exécuté qu’une seule fois dans un contexte d’administration sur Windows périphérique.</span><span class="sxs-lookup"><span data-stu-id="be4c9-143">The preceding command only needs to be run once in an administrative context on the Windows device.</span></span>

#### <a name="hybrid-ad-joinre-registration"></a><span data-ttu-id="be4c9-144">Hybrid AD Join\Re-Registration</span><span class="sxs-lookup"><span data-stu-id="be4c9-144">Hybrid AD Join\Re-Registration</span></span>

<span data-ttu-id="be4c9-145">L’appareil est automatiquement joint à Azure AD sans intervention de l’utilisateur ou de l’administrateur tant que l’appareil dispose d’une connectivité réseau aux points de terminaison Azure AD globaux.</span><span class="sxs-lookup"><span data-stu-id="be4c9-145">The device is automatically joined to Azure AD without user or admin intervention as long as the device has network connectivity to global Azure AD endpoints.</span></span> 


## <a name="azure-ad-join"></a><span data-ttu-id="be4c9-146">Azure AD Join</span><span class="sxs-lookup"><span data-stu-id="be4c9-146">Azure AD Join</span></span>

<span data-ttu-id="be4c9-147">**IMPORTANT :** Le principal de service Intune sera activé après la migration commerciale, ce qui implique l’activation d’Azure AD Device Registration.</span><span class="sxs-lookup"><span data-stu-id="be4c9-147">**IMPORTANT:** The Intune service principal will be enabled after commerce migration, which implies the activation of Azure AD Device Registration.</span></span> <span data-ttu-id="be4c9-148">Si vous avez bloqué l’inscription des appareils Azure AD avant la migration, vous devez désactiver le principal de service Intune avec PowerShell pour désactiver à nouveau l’inscription des appareils Azure AD avec le portail Azure AD.</span><span class="sxs-lookup"><span data-stu-id="be4c9-148">If you blocked Azure AD Device Registration before migration, you must disable the Intune service principal with PowerShell to disable Azure AD Device Registration with the Azure AD portal again.</span></span> <span data-ttu-id="be4c9-149">Vous pouvez désactiver le principal de service Intune avec cette commande dans la Azure Active Directory PowerShell pour Graph module.</span><span class="sxs-lookup"><span data-stu-id="be4c9-149">You can disable the Intune service principal with this command in the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```

### <a name="unjoin"></a><span data-ttu-id="be4c9-150">Unjoin</span><span class="sxs-lookup"><span data-stu-id="be4c9-150">Unjoin</span></span>

<span data-ttu-id="be4c9-151">Pour déterminer si l’appareil Windows 10 précédemment joint à Azure AD, l’utilisateur ou l’administrateur peut exécuter la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="be4c9-151">To determine whether the Windows 10 device was previously joined to Azure AD, the user or admin can run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="be4c9-152">Si l’appareil est joint à Azure AD, l’utilisateur ou l’administrateur verra le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="be4c9-152">If the device is joined to Azure AD, the user or admin would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| Device State                                                         |
+----------------------------------------------------------------------+
 
             AzureAdJoined : YES
          EnterpriseJoined : NO
              DomainJoined : NO
```

<span data-ttu-id="be4c9-153">Si la sortie est « AzureAdJoined : NO », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="be4c9-153">If the output is "AzureAdJoined : NO", ignore the following guidance.</span></span>

<span data-ttu-id="be4c9-154">Utilisateur : si l’appareil est joint à Azure AD, un utilisateur peut déjoinder l’appareil des paramètres.</span><span class="sxs-lookup"><span data-stu-id="be4c9-154">User: If the device is Azure AD joined, a user can unjoin the device from the settings.</span></span> <span data-ttu-id="be4c9-155">Vérifiez qu’il existe un compte d’administrateur local sur l’appareil avant de l’avoir désjoindée d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="be4c9-155">Verify that there is a local administrator account on the device before unjoining the device from Azure AD.</span></span> <span data-ttu-id="be4c9-156">Le compte d’administrateur local est requis pour se remettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-156">The local administrator account is required to sign back into the device.</span></span>

<span data-ttu-id="be4c9-157">Administrateur : si l’administrateur de l’organisation souhaite déjoinder les appareils des utilisateurs joints à Azure AD, ils peuvent le faire en exécutant la commande suivante sur chacun des appareils à l’aide d’un mécanisme tel que la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="be4c9-157">Admin: If the organization's admin wants to unjoin the users' devices that are Azure AD–joined, they can do so by running the following command on each of the devices by using a mechanism such as Group Policy.</span></span> <span data-ttu-id="be4c9-158">L’administrateur doit vérifier qu’il existe un compte d’administrateur local sur l’appareil avant de l’avoir désjoindée d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="be4c9-158">The admin must verify that there is a local administrator account on the device before unjoining the device from Azure AD.</span></span> <span data-ttu-id="be4c9-159">Le compte d’administrateur local est nécessaire pour se remettre à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-159">The local administrator account is needed to sign back into the device.</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /leave
```

<span data-ttu-id="be4c9-160">La commande précédente ne doit être exécuté qu’une seule fois dans un contexte d’administration sur Windows périphérique.</span><span class="sxs-lookup"><span data-stu-id="be4c9-160">The preceding command only needs to be run once in an administrative context on the Windows device.</span></span> 

### <a name="azure-ad-joinre-registration"></a><span data-ttu-id="be4c9-161">Azure AD Join/Re-Registration</span><span class="sxs-lookup"><span data-stu-id="be4c9-161">Azure AD Join/Re-Registration</span></span>

<span data-ttu-id="be4c9-162">L’utilisateur peut joindre l’appareil à Azure AD à partir de Windows paramètres : Paramètres > Comptes > Accès Au travail ou à **l'> Connecter**.</span><span class="sxs-lookup"><span data-stu-id="be4c9-162">The user can join the device to Azure AD from Windows settings: **Settings > Accounts > Access Work Or School > Connect**.</span></span>
 

## <a name="azure-ad-registered-company-owned"></a><span data-ttu-id="be4c9-163">Azure AD Registered (propriété de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="be4c9-163">Azure AD Registered (Company owned)</span></span>

<span data-ttu-id="be4c9-164">Pour déterminer si l’Windows 10 est inscrit à Azure AD, exécutez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="be4c9-164">To determine whether the Windows 10 device is Azure AD–registered, run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="be4c9-165">Si l’appareil est enregistré dans Azure AD, vous verrez la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="be4c9-165">If the device is Azure AD Registered, you would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| User State                                                           |
+----------------------------------------------------------------------+
           WorkplaceJoined : YES
          WamDefaultSet : NO
          WamDefaultAuthority : organizations
```

<span data-ttu-id="be4c9-166">Pour supprimer le compte Azure AD existant sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="be4c9-166">To remove the existing Azure AD-registered account on the device:</span></span>

- <span data-ttu-id="be4c9-167">Pour supprimer le compte Azure AD enregistré sur l’appareil, utilisez CleanupWPJ, un outil que vous pouvez télécharger à partir [ d’ici :CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span><span class="sxs-lookup"><span data-stu-id="be4c9-167">To remove the Azure AD–registered account on the device, use CleanupWPJ, a tool that you can download from here: [CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span></span>

- <span data-ttu-id="be4c9-168">Extrayez le fichier ZIP et exécutez **WPJCleanup.cmd**.</span><span class="sxs-lookup"><span data-stu-id="be4c9-168">Extract the ZIP file and run **WPJCleanup.cmd**.</span></span> <span data-ttu-id="be4c9-169">Cet outil lance le bon exécutable en fonction de la version de Windows sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-169">This tool will launch the right executable based on the version of Windows on the device.</span></span>

- <span data-ttu-id="be4c9-170">À l’aide d’un mécanisme tel que la stratégie de groupe, l’administrateur peut exécuter la commande sur l’appareil dans le contexte de tout utilisateur connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-170">By using a mechanism like Group Policy, the admin can run the command on the device in the context of any user who is signed in on the device.</span></span>

<span data-ttu-id="be4c9-171">Pour désactiver les invites du Gestionnaire de comptes Web pour inscrire l’appareil dans Azure AD, ajoutez cette valeur de Registre :</span><span class="sxs-lookup"><span data-stu-id="be4c9-171">To disable Web Account Manager prompts to register the device in Azure AD, add this registry value:</span></span> 

- <span data-ttu-id="be4c9-172">Emplacement : HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="be4c9-172">Location: HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span></span>
- <span data-ttu-id="be4c9-173">Type : DWORD (32 bits)</span><span class="sxs-lookup"><span data-stu-id="be4c9-173">Type: DWORD (32 bit)</span></span>
- <span data-ttu-id="be4c9-174">Nom : BlockAADWorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="be4c9-174">Name: BlockAADWorkplaceJoin</span></span>
- <span data-ttu-id="be4c9-175">Données de valeur : 1</span><span class="sxs-lookup"><span data-stu-id="be4c9-175">Value data: 1</span></span>

<span data-ttu-id="be4c9-176">La présence de cette valeur de Registre doit bloquer l’accès à l’espace de travail et empêcher les utilisateurs de voir des invites pour rejoindre l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-176">The presence of this registry value should block workplace join and prevent users from seeing prompts to join the device.</span></span>

## <a name="android"></a><span data-ttu-id="be4c9-177">Android</span><span class="sxs-lookup"><span data-stu-id="be4c9-177">Android</span></span>

<span data-ttu-id="be4c9-178">Pour Android, les utilisateurs doivent désins inscrire et réenregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="be4c9-178">For Android, users will need to unregister and re-register their devices.</span></span> <span data-ttu-id="be4c9-179">Vous pouvez le faire via l’application Microsoft Authenticator ou l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="be4c9-179">This can be done via the Microsoft Authenticator app or the Company Portal app.</span></span> 

- <span data-ttu-id="be4c9-180">À partir de Microsoft Authenticator’application, les utilisateurs peuvent Paramètres > **inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-180">From the Microsoft Authenticator app, users can go to **Settings > Device Registration**.</span></span> <span data-ttu-id="be4c9-181">À partir de là, les utilisateurs peuvent désins inscrire et réenregistrer leur appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-181">From there users can unregister and re-register their device.</span></span>
 
- <span data-ttu-id="be4c9-182">À partir de Portail d’entreprise, les utilisateurs peuvent se rendre sur l’onglet **Appareils** et supprimer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-182">From the Company Portal, users can go to **Devices** tab and remove the device.</span></span> <span data-ttu-id="be4c9-183">Ensuite, réinscrivez l’appareil à l’aide Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="be4c9-183">After that, re-enroll the device by using Company Portal.</span></span>
 
- <span data-ttu-id="be4c9-184">Les utilisateurs peuvent également se désins inscrire et s’inscrire à la nouvelle inscription en supprimant le compte de la page des paramètres du compte, puis en ajoutant à nouveaux le compte de travail.</span><span class="sxs-lookup"><span data-stu-id="be4c9-184">Users can also unregister and re-register by removing the account from the account settings page and then re-adding the work account.</span></span>

<span data-ttu-id="be4c9-185">Pour désins inscrire et réenregistrer l’appareil sur Android à l’aide Microsoft Authenticator application :</span><span class="sxs-lookup"><span data-stu-id="be4c9-185">To unregister and re-register the device on Android by using the Microsoft Authenticator app:</span></span>

1.  <span data-ttu-id="be4c9-186">Ouvrez l Microsoft Authenticator appl; et Paramètres **.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-186">Open the Microsoft Authenticator app and go to **Settings**.</span></span>
2.  <span data-ttu-id="be4c9-187">Sélectionnez **Inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-187">Select **Device registration**.</span></span>
3.  <span data-ttu-id="be4c9-188">Désinsinser l’appareil en sélectionnant **Désinsinsion**.</span><span class="sxs-lookup"><span data-stu-id="be4c9-188">Unregister the device by selecting **Unregister**.</span></span>
4.  <span data-ttu-id="be4c9-189">Pour **l’inscription de** l’appareil, ré-inscrivez l’appareil en tapant votre adresse e-mail, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-189">For **Device registration**, re-register the device by typing your email address, and then select **Register**.</span></span>

<span data-ttu-id="be4c9-190">Pour désins inscrire et réenregistrer un appareil Android à l’Paramètres page :</span><span class="sxs-lookup"><span data-stu-id="be4c9-190">To unregister and re-register an Android device with the Android Settings page:</span></span>

1.  <span data-ttu-id="be4c9-191">Ouvrez **Device Paramètres** et go to **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="be4c9-191">Open **Device Settings** and go to **Accounts**.</span></span>
2.  <span data-ttu-id="be4c9-192">Sélectionnez le compte de travail que vous souhaitez ré-inscrire et **sélectionnez Supprimer le compte.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-192">Select the work account that you want to re-register and select **Remove account**.</span></span>
3.  <span data-ttu-id="be4c9-193">Une fois le compte supprimé, dans la **page** Comptes, sélectionnez Ajouter un **compte > compte de travail.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-193">After the account is removed, from the **Accounts** page, select **Add Account > Work account**.</span></span>
4.  <span data-ttu-id="be4c9-194">Pour **Workplace Join,** tapez votre adresse e-mail et **sélectionnez Rejoindre** pour terminer l’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-194">For **Workplace Join**, type your email address and select **Join** to complete registering the device.</span></span>

<span data-ttu-id="be4c9-195">Pour désins inscrire et réenregistrer l’appareil sur Android, Portail d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="be4c9-195">To unregister and re-register the device on Android from Company Portal:</span></span>

1.  <span data-ttu-id="be4c9-196">Lancez Portail d’entreprise et allez sur **l’onglet** Appareils.</span><span class="sxs-lookup"><span data-stu-id="be4c9-196">Launch Company Portal and go to **Devices** tab.</span></span>
2.  <span data-ttu-id="be4c9-197">Sélectionnez l’appareil pour voir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-197">Select the device to see the device details.</span></span>
3.  <span data-ttu-id="be4c9-198">Dans le menu des points de sélection (trois points), sélectionnez Supprimer l’appareil **et** terminez la suppression en confirmant dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="be4c9-198">From the ellipses (three dots) menu, select **Remove Device**, and complete the removal by confirming in the dialog.</span></span>
4.  <span data-ttu-id="be4c9-199">Vous devez maintenant être déconnecté de l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="be4c9-199">You should now be logged out of the Company Portal app.</span></span> <span data-ttu-id="be4c9-200">Sélectionnez **Se connectez** pour ré-inscrire l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-200">Select **Sign in** to re-register the device.</span></span>

<span data-ttu-id="be4c9-201">Pour plus d’informations sur les actions requises pendant la phase de migration de cette charge de travail, ou sur l’impact sur l’administration ou l’utilisation, examinez les informations sur Azure Active Directory (Azure AD) dans Des informations [Azure AD](ms-cloud-germany-transition-azure-ad.md)supplémentaires pour la migration à partir de Microsoft Cloud Deutschland .</span><span class="sxs-lookup"><span data-stu-id="be4c9-201">For more information about any actions required during the migration phase of this workload, or impact to administration or usage, review the information about Azure Active Directory (Azure AD) in [Additional Azure AD information for the migration from Microsoft Cloud Deutschland](ms-cloud-germany-transition-azure-ad.md).</span></span>

## <a name="ios"></a><span data-ttu-id="be4c9-202">iOS</span><span class="sxs-lookup"><span data-stu-id="be4c9-202">iOS</span></span>

<span data-ttu-id="be4c9-203">Sur les appareils iOS, un utilisateur doit supprimer manuellement tous les comptes mis en cache de l’Microsoft Authenticator, désinsister l’appareil et se dé dé connecter à partir de toutes les applications natives de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="be4c9-203">On iOS devices, a user will need to manually remove any cached accounts from the Microsoft Authenticator, unregister the device, and sign out from any native apps on the device.</span></span>

### <a name="step-1-if-present-remove-the-account-from-the-microsoft-authenticator-app"></a><span data-ttu-id="be4c9-204">Étape 1 : si elle est présente, supprimez le compte de l’application Microsoft Authenticator client</span><span class="sxs-lookup"><span data-stu-id="be4c9-204">Step 1: If present, remove the account from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="be4c9-205">Appuyez sur le compte dans l Microsoft Authenticator appl;</span><span class="sxs-lookup"><span data-stu-id="be4c9-205">Tap the account in the Microsoft Authenticator app.</span></span>
2. <span data-ttu-id="be4c9-206">Appuyez sur **Paramètres** icône dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="be4c9-206">Tap the **Settings** icon in the top-right corner.</span></span> <span data-ttu-id="be4c9-207">Si vous ne voyez pas **l’icône Paramètres,** il se peut que vous n’utilisiez pas la dernière version de Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="be4c9-207">If you don't see the **Settings** icon, you might not be using the latest version of Microsoft Authenticator.</span></span>
3. <span data-ttu-id="be4c9-208">Appuyez sur **le bouton** Supprimer le compte.</span><span class="sxs-lookup"><span data-stu-id="be4c9-208">Tap the **Remove account** button.</span></span>
4. <span data-ttu-id="be4c9-209">Appuyez **sur toutes les applications sur cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-209">Tap **All apps on this device**.</span></span>
 
### <a name="step-2-unregister-the-device-from-the-microsoft-authenticator-app"></a><span data-ttu-id="be4c9-210">Étape 2 : Désinsser l’appareil de l’Microsoft Authenticator appel</span><span class="sxs-lookup"><span data-stu-id="be4c9-210">Step 2: Unregister the device from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="be4c9-211">Appuyez sur l’icône de menu dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="be4c9-211">Tap the menu icon in the top-right corner.</span></span>
2. <span data-ttu-id="be4c9-212">Appuyez **Paramètres** puis inscription **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="be4c9-212">Tap **Settings** and then **Device Registration**.</span></span>
4. <span data-ttu-id="be4c9-213">Si votre compte s’affiche, **appuyez sur Désinsister l’appareil** et **continuez** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="be4c9-213">If your account is shown, tap **Unregister device** and **Continue** in the dialog.</span></span> <span data-ttu-id="be4c9-214">Vous ne devriez voir aucun compte après cela.</span><span class="sxs-lookup"><span data-stu-id="be4c9-214">You should see no account after that.</span></span>
 
### <a name="step-3-sign-out-from-individual-apps-if-necessary"></a><span data-ttu-id="be4c9-215">Étape 3 : Se sortir des applications individuelles si nécessaire</span><span class="sxs-lookup"><span data-stu-id="be4c9-215">Step 3: Sign out from individual apps if necessary</span></span>

<span data-ttu-id="be4c9-216">Les utilisateurs peuvent se rendre sur des applications individuelles telles que Outlook, Teams et OneDrive, et supprimer des comptes de ces applications.</span><span class="sxs-lookup"><span data-stu-id="be4c9-216">Users can go to individual apps like Outlook, Teams, and OneDrive, and remove accounts from those apps.</span></span>

## <a name="more-information"></a><span data-ttu-id="be4c9-217">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="be4c9-217">More information</span></span>

<span data-ttu-id="be4c9-218">Mise en place :</span><span class="sxs-lookup"><span data-stu-id="be4c9-218">Getting started:</span></span>

- [<span data-ttu-id="be4c9-219">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centres de données allemandes</span><span class="sxs-lookup"><span data-stu-id="be4c9-219">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="be4c9-220">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="be4c9-220">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="be4c9-221">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="be4c9-221">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="be4c9-222">Expérience client pendant la migration</span><span class="sxs-lookup"><span data-stu-id="be4c9-222">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="be4c9-223">Transition :</span><span class="sxs-lookup"><span data-stu-id="be4c9-223">Moving through the transition:</span></span>

- [<span data-ttu-id="be4c9-224">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="be4c9-224">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="be4c9-225">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="be4c9-225">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="be4c9-226">Informations supplémentaires pour [Azure AD,](ms-cloud-germany-transition-azure-ad.md) [les appareils,](ms-cloud-germany-transition-add-devices.md) [les expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="be4c9-226">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="be4c9-227">Applications cloud :</span><span class="sxs-lookup"><span data-stu-id="be4c9-227">Cloud apps:</span></span>

- [<span data-ttu-id="be4c9-228">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="be4c9-228">Dynamics 365 migration program information</span></span>](/dynamics365/get-started/migrate-data-german-region)
- [<span data-ttu-id="be4c9-229">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="be4c9-229">Power BI migration program information</span></span>](/power-bi/admin/service-admin-migrate-data-germany)
- [<span data-ttu-id="be4c9-230">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be4c9-230">Getting started with your Microsoft Teams upgrade</span></span>](/microsoftteams/upgrade-start-here)