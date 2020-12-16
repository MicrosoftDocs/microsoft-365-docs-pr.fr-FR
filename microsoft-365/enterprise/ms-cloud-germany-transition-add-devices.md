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
description: 'Résumé : informations supplémentaires sur les services lors du passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) vers les services Office 365 dans la nouvelle région de centre de données allemande.'
ms.openlocfilehash: 1bbb4bf39db61a93844c21cd6062a70699b5d6d7
ms.sourcegitcommit: 849b365bd3eaa9f3c3a9ef9f5973ef81af9156fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49688652"
---
# <a name="additional-device-information-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="dd28b-103">Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="dd28b-103">Additional device information for the migration from Microsoft Cloud Deutschland</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="dd28b-104">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="dd28b-104">Frequently asked questions</span></span>

<span data-ttu-id="dd28b-105">**Comment puis-je savoir si mon organisation est concernée ?**</span><span class="sxs-lookup"><span data-stu-id="dd28b-105">**How can I tell if my organization is affected?**</span></span>

<span data-ttu-id="dd28b-106">Les administrateurs doivent vérifier `https://portal.microsoftazure.de` s’ils disposent d’appareils inscrits.</span><span class="sxs-lookup"><span data-stu-id="dd28b-106">Administrators should check `https://portal.microsoftazure.de` to determine if they have any registered devices.</span></span> <span data-ttu-id="dd28b-107">Si votre organisation a enregistré des appareils, vous en êtes affecté.</span><span class="sxs-lookup"><span data-stu-id="dd28b-107">If your organization has registered devices, you're affected.</span></span>

<span data-ttu-id="dd28b-108">**Quel est l’impact sur mes utilisateurs ?**</span><span class="sxs-lookup"><span data-stu-id="dd28b-108">**What is the impact on my users?**</span></span>

<span data-ttu-id="dd28b-109">Les utilisateurs d’un appareil inscrit ne seront plus en mesure de se connecter après la fin de la migration de la phase de migration [Azure ad](ms-cloud-germany-transition.md#how-is-the-migration-organized) .</span><span class="sxs-lookup"><span data-stu-id="dd28b-109">Users from a registered device will no longer be able to sign in after your migration enters the [Finalize Azure AD](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>  

<span data-ttu-id="dd28b-110">Assurez-vous que tous vos appareils sont inscrits auprès du point de terminaison international avant la déconnexion de votre organisation de Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="dd28b-110">Ensure that all of your devices are registered with the worldwide endpoint before your organization is disconnected from Microsoft Cloud Deutschland.</span></span>
  
<span data-ttu-id="dd28b-111">**Quand mes utilisateurs réenregistrent-ils leurs appareils ?**</span><span class="sxs-lookup"><span data-stu-id="dd28b-111">**When do my users re-register their devices?**</span></span>

<span data-ttu-id="dd28b-112">Il est essentiel pour votre réussite de ne pas enregistrer et ré-enregistrer vos appareils pendant la phase [de migration distincte de Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) .</span><span class="sxs-lookup"><span data-stu-id="dd28b-112">It's critical to your success that you only unregister and re-register your devices during the [Separate from Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>

<span data-ttu-id="dd28b-113">**Comment restaurer l’état de mon appareil après la migration ?**</span><span class="sxs-lookup"><span data-stu-id="dd28b-113">**How do I restore my device state after migration?**</span></span>

<span data-ttu-id="dd28b-114">Pour les appareils Windows hybrides, joints et appartenant à l’entreprise, qui sont enregistrés avec Azure AD, les administrateurs pourront gérer la migration de ces appareils via des flux de travail déclenchés à distance qui annuleront l’inscription des anciens États des appareils.</span><span class="sxs-lookup"><span data-stu-id="dd28b-114">For hybrid Azure AD–joined and company-owned Windows devices that are registered with Azure AD, administrators will be able to manage the migration of these devices through remotely triggered workflows that will unregister the old device states.</span></span>
  
<span data-ttu-id="dd28b-115">Pour tous les autres appareils, y compris les appareils Windows personnels inscrits dans Azure AD, l’utilisateur final doit effectuer ces étapes manuellement.</span><span class="sxs-lookup"><span data-stu-id="dd28b-115">For all other devices, including personal Windows devices that are registered in Azure AD, the end user must perform these steps manually.</span></span> <span data-ttu-id="dd28b-116">Pour les appareils joints à Azure AD, les utilisateurs doivent disposer d’un compte d’administrateur local pour annuler l’inscription, puis ré-enregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="dd28b-116">For Azure AD–joined devices, users need to have a local administrator account to unregister and then re-register their devices.</span></span>

<span data-ttu-id="dd28b-117">Microsoft publiera des instructions sur la manière de restaurer correctement l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-117">Microsoft will publish instructions for how to successfully restore device state.</span></span> 
 
<span data-ttu-id="dd28b-118">**Comment puis-je savoir que tous les appareils sont inscrits dans le cloud public ?**</span><span class="sxs-lookup"><span data-stu-id="dd28b-118">**How do I know that all my devices are registered in the public cloud?**</span></span>

<span data-ttu-id="dd28b-119">Pour vérifier si vos appareils sont enregistrés dans le cloud public, vous devez exporter et télécharger la liste des périphériques depuis le portail Azure AD vers une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="dd28b-119">To check whether your devices are registered in the public cloud, you should export and download the list of devices from the Azure AD portal to an Excel spreadsheet.</span></span> <span data-ttu-id="dd28b-120">Ensuite, filtrez les périphériques inscrits (à l’aide de la colonne _registeredTime_ ) après la phase [de migration Deutschland de Microsoft Cloud](ms-cloud-germany-transition.md#how-is-the-migration-organized) .</span><span class="sxs-lookup"><span data-stu-id="dd28b-120">Then, filter the devices that are registered (by using the _registeredTime_ column) after the [Separate from Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>

<span data-ttu-id="dd28b-121">L’inscription de l’appareil est désactivée après la migration du client et ne peut pas être activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="dd28b-121">Device registration is deactivated after migration of the tenant and cannot be enabled or disabled.</span></span> <span data-ttu-id="dd28b-122">Si Intune n’est pas utilisé, connectez-vous à votre abonnement et exécutez cette commande pour réactiver l’option :</span><span class="sxs-lookup"><span data-stu-id="dd28b-122">If Intune is not used, sign in to your subscription and run this command to re-activate the option:</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```

## <a name="windows-hybrid-azure-ad-join"></a><span data-ttu-id="dd28b-123">Participation Windows hybride Azure AD</span><span class="sxs-lookup"><span data-stu-id="dd28b-123">Windows Hybrid Azure AD join</span></span>

### <a name="windows-down-level"></a><span data-ttu-id="dd28b-124">Windows de bas niveau</span><span class="sxs-lookup"><span data-stu-id="dd28b-124">Windows down-level</span></span>

<span data-ttu-id="dd28b-125">Les _appareils de bas niveau Windows_ sont des appareils Windows qui exécutent actuellement des versions antérieures de Windows (telles que Windows 8,1 ou Windows 7) ou qui exécutent des versions de Windows Server antérieures à 2019 et 2016.</span><span class="sxs-lookup"><span data-stu-id="dd28b-125">_Windows down-level devices_ are Windows devices that currently run earlier versions of Windows (such as Windows 8.1 or Windows 7), or that run Windows Server versions earlier than 2019 and 2016.</span></span> <span data-ttu-id="dd28b-126">Si de tels appareils ont été enregistrés auparavant, vous devrez annuler l’inscription et ré-enregistrer ces périphériques.</span><span class="sxs-lookup"><span data-stu-id="dd28b-126">If such devices were registered before, you'll need to unregister and re-register those devices.</span></span> 

<span data-ttu-id="dd28b-127">Pour déterminer si un appareil de bas niveau de Windows a été précédemment joint à Azure AD, utilisez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="dd28b-127">To determine whether a Windows down-level device was previously joined to Azure AD, use following command on the device:</span></span>

```console
%programfiles%\Microsoft Workplace Join\autoworkplace /status
```

<span data-ttu-id="dd28b-128">Si l’appareil a été précédemment joint à Azure AD et que l’appareil dispose d’une connectivité réseau aux points de terminaison Azure AD globaux, vous verrez le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="dd28b-128">If the device was previously joined to Azure AD, and if the device has network connectivity to global Azure AD endpoints, you would see the following output:</span></span>

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

<span data-ttu-id="dd28b-129">Le « État du périphérique » dont la valeur est « inconnu » est affecté aux appareils concernés.</span><span class="sxs-lookup"><span data-stu-id="dd28b-129">The affected devices will have the "Device state" with value of "Unknown".</span></span> <span data-ttu-id="dd28b-130">Si la sortie est « appareil non joint » ou dont la valeur « État de l’appareil » est « OK », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd28b-130">If the output is "Device not joined" or whose "Device state" value is "Okay", ignore the following guidance.</span></span>

<span data-ttu-id="dd28b-131">Les administrateurs doivent exécuter la commande suivante dans le contexte d’un utilisateur de domaine qui se connecte sur un appareil de bas niveau uniquement pour les appareils qui indiquent que l’appareil est joint (en vertu d’un deviceId, d’une empreinte, etc.) et dont la valeur « État du périphérique » est « inconnue » :</span><span class="sxs-lookup"><span data-stu-id="dd28b-131">Only for devices that show that the device is joined (by virtue of deviceId, thumbprint, and so on) and whose "Device state" value is "Unknown", admins should run the following command in the context of a domain user signing in on such a down-level device:</span></span>

```console
"%programfiles%\Microsoft Workplace Join\autoworkplace /leave"
```

<span data-ttu-id="dd28b-132">La commande précédente ne doit être exécutée qu’une seule fois par utilisateur de domaine qui se connecte sur l’appareil bas Windows.</span><span class="sxs-lookup"><span data-stu-id="dd28b-132">The preceding command only needs to be run once per domain user signing in on the Windows down-level device.</span></span> <span data-ttu-id="dd28b-133">Cette commande doit être exécutée dans le contexte de la connexion de l’utilisateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="dd28b-133">This command should be run in the context of the domain user signing in.</span></span> 

<span data-ttu-id="dd28b-134">Il faut veiller à ne pas exécuter cette commande lorsque l’utilisateur se connecte par la suite.</span><span class="sxs-lookup"><span data-stu-id="dd28b-134">Sufficient care must be taken to not run this command when the user subsequently signs in.</span></span> <span data-ttu-id="dd28b-135">Lorsque la commande précédente est exécutée, elle efface l’état de jonction de l’ordinateur hybride Azure AD-joint local de l’utilisateur qui s’est connecté.</span><span class="sxs-lookup"><span data-stu-id="dd28b-135">When the preceding command runs, it will clear the joined state of the local hybrid Azure AD–joined computer for the user who signed in.</span></span> <span data-ttu-id="dd28b-136">De plus, si l’ordinateur est toujours configuré pour être lié à Azure AD-joint au client, il essaiera de se joindre lorsque l’utilisateur se reconnecte.</span><span class="sxs-lookup"><span data-stu-id="dd28b-136">And, if the computer is still configured to be hybrid Azure AD–joined in the tenant, it will attempt to join when the user signs in again.</span></span>

### <a name="windows-current"></a><span data-ttu-id="dd28b-137">Windows actuel</span><span class="sxs-lookup"><span data-stu-id="dd28b-137">Windows Current</span></span>

#### <a name="unjoin"></a><span data-ttu-id="dd28b-138">Se désinscrire</span><span class="sxs-lookup"><span data-stu-id="dd28b-138">Unjoin</span></span>

<span data-ttu-id="dd28b-139">Pour déterminer si l’appareil Windows 10 a été précédemment joint à Azure AD, exécutez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="dd28b-139">To determine whether the Windows 10 device was previously joined to Azure AD, run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="dd28b-140">Si le périphérique est hybride Azure AD-joint, l’administrateur voit apparaître la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="dd28b-140">If the device is hybrid Azure AD–joined, the admin would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| Device State                                                         |
+----------------------------------------------------------------------+
 
             AzureAdJoined : YES
          EnterpriseJoined : NO
              DomainJoined : YES
```

<span data-ttu-id="dd28b-141">Si la sortie est « AzureAdJoined : no », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd28b-141">If the output is "AzureAdJoined : No", ignore the following guidance.</span></span>

<span data-ttu-id="dd28b-142">Pour les appareils qui indiquent que l’appareil est joint à Azure AD, exécutez la commande suivante en tant qu’administrateur pour supprimer l’état de jonction de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-142">Only for devices that show that the device is joined to Azure AD, run the following command as an admin to remove the joined state of the device.</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /leave
```

<span data-ttu-id="dd28b-143">La commande précédente ne doit être exécutée qu’une seule fois dans un contexte administratif sur l’appareil Windows.</span><span class="sxs-lookup"><span data-stu-id="dd28b-143">The preceding command only needs to be run once in an administrative context on the Windows device.</span></span>

#### <a name="hybrid-ad-joinre-registration"></a><span data-ttu-id="dd28b-144">Join\Re-Registration hybride AD</span><span class="sxs-lookup"><span data-stu-id="dd28b-144">Hybrid AD Join\Re-Registration</span></span>

<span data-ttu-id="dd28b-145">L’appareil est automatiquement joint à Azure AD sans intervention de l’utilisateur ou de l’administrateur tant que l’appareil dispose d’une connectivité réseau aux points de terminaison Azure AD globaux.</span><span class="sxs-lookup"><span data-stu-id="dd28b-145">The device is automatically joined to Azure AD without user or admin intervention as long as the device has network connectivity to global Azure AD endpoints.</span></span> 


## <a name="windows-azure-ad-join"></a><span data-ttu-id="dd28b-146">Participation à Windows Azure AD</span><span class="sxs-lookup"><span data-stu-id="dd28b-146">Windows Azure AD Join</span></span>

<span data-ttu-id="dd28b-147">**Important :** Le principal de service Intune sera activé après la migration de commerce, ce qui implique l’activation de l’inscription d’appareil Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dd28b-147">**IMPORTANT:** The Intune service principal will be enabled after commerce migration, which implies the activation of Azure AD Device Registration.</span></span> <span data-ttu-id="dd28b-148">Si vous avez bloqué l’inscription de l’appareil Azure AD avant la migration, vous devez désactiver le principal du service Intune avec PowerShell pour désactiver l’inscription de l’appareil Azure AD avec le portail Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dd28b-148">If you blocked Azure AD Device Registration before migration, you must disable the Intune service principal with PowerShell to disable Azure AD Device Registration with the Azure AD portal again.</span></span> <span data-ttu-id="dd28b-149">Vous pouvez désactiver le principal du service Intune à l’aide de cette commande dans le module Azure Active Directory PowerShell pour Graph.</span><span class="sxs-lookup"><span data-stu-id="dd28b-149">You can disable the Intune service principal with this command in the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```

### <a name="unjoin"></a><span data-ttu-id="dd28b-150">Se désinscrire</span><span class="sxs-lookup"><span data-stu-id="dd28b-150">Unjoin</span></span>

<span data-ttu-id="dd28b-151">Pour déterminer si l’appareil Windows 10 a été précédemment joint à Azure AD, l’utilisateur ou l’administrateur peut exécuter la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="dd28b-151">To determine whether the Windows 10 device was previously joined to Azure AD, the user or admin can run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="dd28b-152">Si l’appareil est lié à Azure AD, l’utilisateur ou l’administrateur voit apparaître la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="dd28b-152">If the device is joined to Azure AD, the user or admin would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| Device State                                                         |
+----------------------------------------------------------------------+
 
             AzureAdJoined : YES
          EnterpriseJoined : NO
              DomainJoined : NO
```

<span data-ttu-id="dd28b-153">Si la sortie est « AzureAdJoined : NO », ignorez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd28b-153">If the output is "AzureAdJoined : NO", ignore the following guidance.</span></span>

<span data-ttu-id="dd28b-154">Utilisateur : si l’appareil est joint Azure AD, un utilisateur peut se déconnecter du périphérique des paramètres.</span><span class="sxs-lookup"><span data-stu-id="dd28b-154">User: If the device is Azure AD joined, a user can unjoin the device from the settings.</span></span> <span data-ttu-id="dd28b-155">Vérifiez qu’il existe un compte d’administrateur local sur l’appareil avant de procéder à la connexion de l’appareil à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dd28b-155">Verify that there is a local administrator account on the device before unjoining the device from Azure AD.</span></span> <span data-ttu-id="dd28b-156">Le compte d’administrateur local est nécessaire pour se reconnecter à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-156">The local administrator account is required to sign back into the device.</span></span>

<span data-ttu-id="dd28b-157">Administrateur : si l’administrateur de l’organisation souhaite dissocier les appareils des utilisateurs Azure AD-joints, il peut le faire en exécutant la commande suivante sur chacun des périphériques à l’aide d’un mécanisme tel que la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="dd28b-157">Admin: If the organization's admin wants to unjoin the users' devices that are Azure AD–joined, they can do so by running the following command on each of the devices by using a mechanism such as Group Policy.</span></span> <span data-ttu-id="dd28b-158">L’administrateur doit vérifier qu’il existe un compte d’administrateur local sur l’appareil avant de rejoindre l’appareil à partir d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="dd28b-158">The admin must verify that there is a local administrator account on the device before unjoining the device from Azure AD.</span></span> <span data-ttu-id="dd28b-159">Le compte administrateur local est nécessaire pour se reconnecter à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-159">The local administrator account is needed to sign back into the device.</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /leave
```

<span data-ttu-id="dd28b-160">La commande précédente ne doit être exécutée qu’une seule fois dans un contexte administratif sur l’appareil Windows.</span><span class="sxs-lookup"><span data-stu-id="dd28b-160">The preceding command only needs to be run once in an administrative context on the Windows device.</span></span> 

### <a name="azure-ad-joinre-registration"></a><span data-ttu-id="dd28b-161">Participation/ré-inscription Azure AD</span><span class="sxs-lookup"><span data-stu-id="dd28b-161">Azure AD Join/Re-Registration</span></span>

<span data-ttu-id="dd28b-162">L’utilisateur peut joindre l’appareil à Azure AD à partir des paramètres Windows : **paramètres > les comptes > accès professionnel ou scolaire > connecter**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-162">The user can join the device to Azure AD from Windows settings: **Settings > Accounts > Access Work Or School > Connect**.</span></span>
 

## <a name="windows-azure-ad-registered-company-owned"></a><span data-ttu-id="dd28b-163">Windows Azure AD inscrit (propriétaire de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="dd28b-163">Windows Azure AD Registered (Company owned)</span></span>

<span data-ttu-id="dd28b-164">Pour déterminer si le périphérique Windows 10 est enregistré dans Azure AD – enregistré, exécutez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="dd28b-164">To determine whether the Windows 10 device is Azure AD–registered, run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="dd28b-165">Si le périphérique est inscrit à Azure AD, le résultat suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="dd28b-165">If the device is Azure AD Registered, you would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| User State                                                           |
+----------------------------------------------------------------------+
           WorkplaceJoined : YES
          WamDefaultSet : NO
          WamDefaultAuthority : organizations
```

<span data-ttu-id="dd28b-166">Pour supprimer le compte Azure AD existant inscrit sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="dd28b-166">To remove the existing Azure AD-registered account on the device:</span></span>

- <span data-ttu-id="dd28b-167">Pour supprimer le compte Azure AD – inscrit sur l’appareil, utilisez CleanupWPJ, un outil que vous pouvez télécharger à partir de cet emplacement : [CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span><span class="sxs-lookup"><span data-stu-id="dd28b-167">To remove the Azure AD–registered account on the device, use CleanupWPJ, a tool that you can download from here: [CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span></span>

- <span data-ttu-id="dd28b-168">Extrayez le fichier ZIP et exécutez **WPJCleanup. cmd**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-168">Extract the ZIP file and run **WPJCleanup.cmd**.</span></span> <span data-ttu-id="dd28b-169">Cet outil lancera le fichier exécutable approprié en fonction de la version de Windows sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-169">This tool will launch the right executable based on the version of Windows on the device.</span></span>

- <span data-ttu-id="dd28b-170">À l’aide d’un mécanisme comme la stratégie de groupe, l’administrateur peut exécuter la commande sur l’appareil dans le contexte d’un utilisateur connecté sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-170">By using a mechanism like Group Policy, the admin can run the command on the device in the context of any user who is signed in on the device.</span></span>

<span data-ttu-id="dd28b-171">Pour désactiver les invites du gestionnaire de comptes Web pour inscrire l’appareil dans Azure AD, ajoutez la valeur de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="dd28b-171">To disable Web Account Manager prompts to register the device in Azure AD, add this registry value:</span></span> 

- <span data-ttu-id="dd28b-172">Emplacement : HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="dd28b-172">Location: HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span></span>
- <span data-ttu-id="dd28b-173">Type : DWORD (32 bits)</span><span class="sxs-lookup"><span data-stu-id="dd28b-173">Type: DWORD (32 bit)</span></span>
- <span data-ttu-id="dd28b-174">Nom : BlockAADWorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="dd28b-174">Name: BlockAADWorkplaceJoin</span></span>
- <span data-ttu-id="dd28b-175">Données de la valeur : 1</span><span class="sxs-lookup"><span data-stu-id="dd28b-175">Value data: 1</span></span>

<span data-ttu-id="dd28b-176">La présence de cette valeur de registre doit bloquer la jonction Workplace et empêcher les utilisateurs de se connecter à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-176">The presence of this registry value should block workplace join and prevent users from seeing prompts to join the device.</span></span>

## <a name="android"></a><span data-ttu-id="dd28b-177">Android</span><span class="sxs-lookup"><span data-stu-id="dd28b-177">Android</span></span>

<span data-ttu-id="dd28b-178">Pour Android, les utilisateurs doivent annuler l’inscription et ré-enregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="dd28b-178">For Android, users will need to unregister and re-register their devices.</span></span> <span data-ttu-id="dd28b-179">Cette opération peut être réalisée via l’application Microsoft Authenticator ou l’application portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="dd28b-179">This can be done via the Microsoft Authenticator app or the Company Portal app.</span></span> 

- <span data-ttu-id="dd28b-180">À partir de l’application Microsoft Authenticator, les utilisateurs peuvent accéder aux **paramètres > inscription de l’appareil**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-180">From the Microsoft Authenticator app, users can go to **Settings > Device Registration**.</span></span> <span data-ttu-id="dd28b-181">À partir de là, les utilisateurs peuvent annuler l’inscription et ré-enregistrer leur appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-181">From there users can unregister and re-register their device.</span></span>
 
- <span data-ttu-id="dd28b-182">À partir du portail d’entreprise, les utilisateurs peuvent accéder à l’onglet **appareils** et supprimer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-182">From the Company Portal, users can go to **Devices** tab and remove the device.</span></span> <span data-ttu-id="dd28b-183">Ensuite, ré-Inscrivez l’appareil à l’aide du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="dd28b-183">After that, re-enroll the device by using Company Portal.</span></span>
 
- <span data-ttu-id="dd28b-184">Les utilisateurs peuvent également annuler l’inscription et procéder à une nouvelle inscription en supprimant le compte de la page Paramètres du compte, puis en rajoutant le compte professionnel.</span><span class="sxs-lookup"><span data-stu-id="dd28b-184">Users can also unregister and re-register by removing the account from the account settings page and then re-adding the work account.</span></span>

<span data-ttu-id="dd28b-185">Pour annuler l’inscription et ré-enregistrer l’appareil sur Android à l’aide de l’application Microsoft Authenticator :</span><span class="sxs-lookup"><span data-stu-id="dd28b-185">To unregister and re-register the device on Android by using the Microsoft Authenticator app:</span></span>

1.  <span data-ttu-id="dd28b-186">Ouvrez l’application Microsoft Authenticator et accédez à **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-186">Open the Microsoft Authenticator app and go to **Settings**.</span></span>
2.  <span data-ttu-id="dd28b-187">Sélectionnez **inscription de l’appareil**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-187">Select **Device registration**.</span></span>
3.  <span data-ttu-id="dd28b-188">Annulez l’inscription de l’appareil en sélectionnant **Annuler l’inscription**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-188">Unregister the device by selecting **Unregister**.</span></span>
4.  <span data-ttu-id="dd28b-189">Pour l’inscription de l' **appareil**, inscrivez de nouveau l’appareil en saisissant votre adresse de messagerie, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-189">For **Device registration**, re-register the device by typing your email address, and then select **Register**.</span></span>

<span data-ttu-id="dd28b-190">Pour annuler l’inscription et ré-enregistrer un appareil Android à l’aide de la page des paramètres Android :</span><span class="sxs-lookup"><span data-stu-id="dd28b-190">To unregister and re-register an Android device with the Android Settings page:</span></span>

1.  <span data-ttu-id="dd28b-191">Ouvrez **paramètres du périphérique** et accédez à **comptes**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-191">Open **Device Settings** and go to **Accounts**.</span></span>
2.  <span data-ttu-id="dd28b-192">Sélectionnez le compte professionnel que vous souhaitez réenregistrer et sélectionnez Supprimer le **compte**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-192">Select the work account that you want to re-register and select **Remove account**.</span></span>
3.  <span data-ttu-id="dd28b-193">Une fois le compte supprimé, dans la page **comptes** , sélectionnez **ajouter un compte > compte professionnel**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-193">After the account is removed, from the **Accounts** page, select **Add Account > Work account**.</span></span>
4.  <span data-ttu-id="dd28b-194">Pour **Workplace Join**, tapez votre adresse de messagerie et sélectionnez **join** pour terminer l’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-194">For **Workplace Join**, type your email address and select **Join** to complete registering the device.</span></span>

<span data-ttu-id="dd28b-195">Pour annuler l’inscription et ré-enregistrer l’appareil sur Android à partir du portail d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="dd28b-195">To unregister and re-register the device on Android from Company Portal:</span></span>

1.  <span data-ttu-id="dd28b-196">Lancez le portail d’entreprise et accédez à l’onglet **appareils** .</span><span class="sxs-lookup"><span data-stu-id="dd28b-196">Launch Company Portal and go to **Devices** tab.</span></span>
2.  <span data-ttu-id="dd28b-197">Sélectionnez l’appareil pour afficher les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-197">Select the device to see the device details.</span></span>
3.  <span data-ttu-id="dd28b-198">Dans le menu points de suspension (trois points), sélectionnez **Supprimer l’appareil**, puis terminez la suppression en procédant à la confirmation dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dd28b-198">From the ellipses (three dots) menu, select **Remove Device**, and complete the removal by confirming in the dialog.</span></span>
4.  <span data-ttu-id="dd28b-199">Vous devez maintenant être déconnecté de l’application portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="dd28b-199">You should now be logged out of the Company Portal app.</span></span> <span data-ttu-id="dd28b-200">Sélectionnez **se connecter** pour réenregistrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-200">Select **Sign in** to re-register the device.</span></span>

<span data-ttu-id="dd28b-201">Pour plus d’informations sur les actions requises pendant la phase de migration de cette charge de travail, ou sur l’impact de l’administration ou de l’utilisation, consultez les informations sur Azure Active Directory (Azure AD) dans des [informations Azure ad supplémentaires pour la migration à partir de Microsoft Cloud Deutschland](ms-cloud-germany-transition-azure-ad.md).</span><span class="sxs-lookup"><span data-stu-id="dd28b-201">For more information about any actions required during the migration phase of this workload, or impact to administration or usage, review the information about Azure Active Directory (Azure AD) in [Additional Azure AD information for the migration from Microsoft Cloud Deutschland](ms-cloud-germany-transition-azure-ad.md).</span></span>

## <a name="ios"></a><span data-ttu-id="dd28b-202">iOS</span><span class="sxs-lookup"><span data-stu-id="dd28b-202">iOS</span></span>

<span data-ttu-id="dd28b-203">Sur les appareils iOS, un utilisateur doit supprimer manuellement les comptes mis en cache de l’authentificateur Microsoft, annuler l’inscription de l’appareil et se déconnecter des applications natives sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd28b-203">On iOS devices, a user will need to manually remove any cached accounts from the Microsoft Authenticator, unregister the device, and sign out from any native apps on the device.</span></span>

### <a name="step-1-if-present-remove-the-account-from-the-microsoft-authenticator-app"></a><span data-ttu-id="dd28b-204">Étape 1 : le cas échéant, supprimez le compte de l’application Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="dd28b-204">Step 1: If present, remove the account from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="dd28b-205">Appuyez sur le compte dans l’application Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="dd28b-205">Tap the account in the Microsoft Authenticator app.</span></span>
2. <span data-ttu-id="dd28b-206">Appuyez sur l’icône **paramètres** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="dd28b-206">Tap the **Settings** icon in the top-right corner.</span></span> <span data-ttu-id="dd28b-207">Si vous ne voyez pas l’icône **paramètres** , il se peut que vous n’utilisiez pas la dernière version de Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="dd28b-207">If you don't see the **Settings** icon, you might not be using the latest version of Microsoft Authenticator.</span></span>
3. <span data-ttu-id="dd28b-208">Appuyez sur le bouton **supprimer le compte** .</span><span class="sxs-lookup"><span data-stu-id="dd28b-208">Tap the **Remove account** button.</span></span>
4. <span data-ttu-id="dd28b-209">Appuyez **sur toutes les applications sur cet appareil**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-209">Tap **All apps on this device**.</span></span>
 
### <a name="step-2-unregister-the-device-from-the-microsoft-authenticator-app"></a><span data-ttu-id="dd28b-210">Étape 2 : annuler l’inscription de l’appareil dans l’application Microsoft Authenticator</span><span class="sxs-lookup"><span data-stu-id="dd28b-210">Step 2: Unregister the device from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="dd28b-211">Appuyez sur l’icône de menu dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="dd28b-211">Tap the menu icon in the top-right corner.</span></span>
2. <span data-ttu-id="dd28b-212">Appuyez sur **paramètres** , puis sur **inscription de l’appareil**.</span><span class="sxs-lookup"><span data-stu-id="dd28b-212">Tap **Settings** and then **Device Registration**.</span></span>
4. <span data-ttu-id="dd28b-213">Si votre compte est affiché, appuyez sur **Annuler l’inscription** de l’appareil et **continuez** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="dd28b-213">If your account is shown, tap **Unregister device** and **Continue** in the dialog.</span></span> <span data-ttu-id="dd28b-214">Aucun compte ne doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="dd28b-214">You should see no account after that.</span></span>
 
### <a name="step-3-sign-out-from-individual-apps-if-necessary"></a><span data-ttu-id="dd28b-215">Étape 3 : Déconnectez-vous des applications individuelles si nécessaire</span><span class="sxs-lookup"><span data-stu-id="dd28b-215">Step 3: Sign out from individual apps if necessary</span></span>

<span data-ttu-id="dd28b-216">Les utilisateurs peuvent accéder à des applications individuelles telles qu’Outlook, teams et OneDrive, et supprimer des comptes de ces applications.</span><span class="sxs-lookup"><span data-stu-id="dd28b-216">Users can go to individual apps like Outlook, Teams, and OneDrive, and remove accounts from those apps.</span></span>

## <a name="more-information"></a><span data-ttu-id="dd28b-217">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="dd28b-217">More information</span></span>

<span data-ttu-id="dd28b-218">Mise en route :</span><span class="sxs-lookup"><span data-stu-id="dd28b-218">Getting started:</span></span>

- [<span data-ttu-id="dd28b-219">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centre de connaissances allemand</span><span class="sxs-lookup"><span data-stu-id="dd28b-219">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="dd28b-220">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="dd28b-220">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="dd28b-221">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="dd28b-221">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="dd28b-222">Expérience client lors de la migration</span><span class="sxs-lookup"><span data-stu-id="dd28b-222">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="dd28b-223">Navigation par le biais de la transition :</span><span class="sxs-lookup"><span data-stu-id="dd28b-223">Moving through the transition:</span></span>

- [<span data-ttu-id="dd28b-224">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="dd28b-224">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="dd28b-225">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="dd28b-225">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="dd28b-226">Informations supplémentaires pour [Azure ad](ms-cloud-germany-transition-azure-ad.md), [appareils](ms-cloud-germany-transition-add-devices.md), [expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="dd28b-226">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="dd28b-227">Applications Cloud :</span><span class="sxs-lookup"><span data-stu-id="dd28b-227">Cloud apps:</span></span>

- [<span data-ttu-id="dd28b-228">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dd28b-228">Dynamics 365 migration program information</span></span>](https://aka.ms/d365ceoptin)
- [<span data-ttu-id="dd28b-229">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="dd28b-229">Power BI migration program information</span></span>](https://aka.ms/pbioptin)
- [<span data-ttu-id="dd28b-230">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="dd28b-230">Getting started with your Microsoft Teams upgrade</span></span>](https://aka.ms/SkypeToTeams-Home)
