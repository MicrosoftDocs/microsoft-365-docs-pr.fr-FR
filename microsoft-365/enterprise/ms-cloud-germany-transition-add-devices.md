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
ms.openlocfilehash: 27426a26befab85bf62a0a143861e447dd722724
ms.sourcegitcommit: 3e971b31435d17ceeaa9871c01e88e25ead560fb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "52861302"
---
# <a name="additional-device-information-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="9d9ea-103">Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="9d9ea-103">Additional device information for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="9d9ea-104">Les appareils joints à Azure AD et inscrits connectés à Microsoft Cloud Deutschland doivent être migrés après la phase 9 et avant la phase 10.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-104">Azure AD joined and registered devices connected to Microsoft Cloud Deutschland must be migrated after phase 9 and before phase 10.</span></span> <span data-ttu-id="9d9ea-105">La migration d’un appareil dépend du type d’appareil, du système d’exploitation et de la relation AAD.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-105">The migration of a device depends on the devices type, operating system and AAD relation.</span></span> 

## <a name="frequently-asked-questions"></a><span data-ttu-id="9d9ea-106">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="9d9ea-106">Frequently asked questions</span></span>

<span data-ttu-id="9d9ea-107">**Comment savoir si mon organisation est affectée ?**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-107">**How can I tell if my organization is affected?**</span></span>

<span data-ttu-id="9d9ea-108">Les administrateurs doivent vérifier s’ils ont des appareils inscrits ou joints `https://portal.microsoftazure.de` à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-108">Administrators should check `https://portal.microsoftazure.de` to determine if they have any registered or Azure AD joined devices.</span></span> <span data-ttu-id="9d9ea-109">Si votre organisation dispose d’appareils inscrits, vous êtes affecté.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-109">If your organization has registered devices, you're affected.</span></span>

<span data-ttu-id="9d9ea-110">**Quel est l’impact sur mes utilisateurs ?**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-110">**What is the impact on my users?**</span></span>

<span data-ttu-id="9d9ea-111">Les utilisateurs d’un appareil enregistré ne pourront plus se connecter une fois la [phase de migration 10](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) terminée et les points de terminaison de Microsoft Cloud Deutschland désactivés.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-111">Users from a registered device will no longer be able to sign in after [migration phase 10](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) has been completed and the endpoints for Microsoft Cloud Deutschland have been disabled.</span></span>  

<span data-ttu-id="9d9ea-112">Assurez-vous que tous vos appareils sont enregistrés auprès du point de terminaison mondial avant que votre organisation ne soit déconnectée de Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-112">Ensure that all of your devices are registered with the worldwide endpoint before your organization is disconnected from Microsoft Cloud Deutschland.</span></span>
  
<span data-ttu-id="9d9ea-113">**Quand mes utilisateurs ré-inscrivent-ils leurs appareils ?**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-113">**When do my users re-register their devices?**</span></span>

<span data-ttu-id="9d9ea-114">Il est essentiel pour votre réussite que vous désins inscrivez et réenregistrez vos appareils une fois la [phase 9](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) terminée.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-114">It's critical to your success that you only unregister and re-register your devices after [phase 9](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) has been completed.</span></span> <span data-ttu-id="9d9ea-115">Vous devez terminer la ré-inscription avant le démarrage de la phase 10, sinon vous risquez de perdre l’accès à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-115">You must finish the re-registration before phase 10 starts, otherwise you could lose access to your device.</span></span>

<span data-ttu-id="9d9ea-116">**Comment restaurer l’état de mon appareil après la migration ?**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-116">**How do I restore my device state after migration?**</span></span>

<span data-ttu-id="9d9ea-117">Pour les appareils Windows d’entreprise enregistrés auprès d’Azure AD, les administrateurs pourront gérer la migration de ces appareils via des flux de travail déclenchés à distance qui désinsisteront les anciens états d’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-117">For company-owned Windows devices that are registered with Azure AD, administrators will be able to manage the migration of these devices through remotely triggered workflows that will unregister the old device states.</span></span>
  
<span data-ttu-id="9d9ea-118">Pour tous les autres appareils, y compris les appareils Windows personnels enregistrés dans Azure AD, l’utilisateur final doit effectuer ces étapes manuellement.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-118">For all other devices, including personal Windows devices that are registered in Azure AD, the end user must perform these steps manually.</span></span> <span data-ttu-id="9d9ea-119">Pour les appareils joints à Azure AD, les utilisateurs doivent avoir un compte d’administrateur local pour se désins inscrire, puis réenregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-119">For Azure AD–joined devices, users need to have a local administrator account to unregister and then re-register their devices.</span></span>

<span data-ttu-id="9d9ea-120">Consultez les instructions détaillées pour savoir comment restaurer correctement les états de l’appareil ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-120">Please refer to detailed instructions for how to successfully restore device states below.</span></span> 
 
<span data-ttu-id="9d9ea-121">**Comment savoir que tous mes appareils sont inscrits dans le cloud public ?**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-121">**How do I know that all my devices are registered in the public cloud?**</span></span>

<span data-ttu-id="9d9ea-122">Pour vérifier si vos appareils sont enregistrés dans le cloud public, vous devez exporter et télécharger la liste des appareils à partir du portail Azure AD vers une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-122">To check whether your devices are registered in the public cloud, you should export and download the list of devices from the Azure AD portal to an Excel spreadsheet.</span></span> <span data-ttu-id="9d9ea-123">Ensuite, filtrez les appareils inscrits (à l’aide de la colonne _registeredTime)_ après la phase de migration Distinct [de Microsoft Cloud Deutschland.](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span><span class="sxs-lookup"><span data-stu-id="9d9ea-123">Then, filter the devices that are registered (by using the _registeredTime_ column) after the [Separate from Microsoft Cloud Deutschland](ms-cloud-germany-transition.md#how-is-the-migration-organized) migration phase.</span></span>

## <a name="additional-considerations"></a><span data-ttu-id="9d9ea-124">Considérations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9d9ea-124">Additional considerations</span></span>
<span data-ttu-id="9d9ea-125">L’inscription de l’appareil est désactivée après la migration du client et ne peut pas être activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-125">Device registration is deactivated after migration of the tenant and cannot be enabled or disabled.</span></span> 

<span data-ttu-id="9d9ea-126">Si Intune n’est pas utilisé, connectez-vous à votre abonnement et exécutez cette commande pour réactiver l’option :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-126">If Intune is not used, sign in to your subscription and run this command to re-activate the option:</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```
<span data-ttu-id="9d9ea-127">**IMPORTANT :** Le principal de service Intune sera activé après la migration commerciale, ce qui implique l’activation d’Azure AD Device Registration.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-127">**IMPORTANT:** The Intune service principal will be enabled after commerce migration, which implies the activation of Azure AD Device Registration.</span></span> <span data-ttu-id="9d9ea-128">Si vous avez bloqué l’inscription des appareils Azure AD avant la migration, vous devez désactiver le principal de service Intune avec PowerShell pour désactiver à nouveau l’inscription des appareils Azure AD avec le portail Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-128">If you blocked Azure AD Device Registration before migration, you must disable the Intune service principal with PowerShell to disable Azure AD Device Registration with the Azure AD portal again.</span></span> <span data-ttu-id="9d9ea-129">Vous pouvez désactiver le principal de service Intune avec cette commande dans la Azure Active Directory PowerShell pour Graph module.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-129">You can disable the Intune service principal with this command in the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```


## <a name="azure-ad-join"></a><span data-ttu-id="9d9ea-130">Azure AD Join</span><span class="sxs-lookup"><span data-stu-id="9d9ea-130">Azure AD Join</span></span>
<span data-ttu-id="9d9ea-131">Cela s’applique Windows 10 appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-131">This applies to Windows 10 devices.</span></span> 

<span data-ttu-id="9d9ea-132">Si un appareil est joint à Azure AD, il doit être déconnecté d’Azure AD et être de nouveau connecté.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-132">If a device is Azure AD joined, it must be disconnected from Azure AD and be connected again.</span></span> 

<span data-ttu-id="9d9ea-133">[![Azure AD Device ](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png) Re-Join Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9d9ea-133">[ ![Azure AD Device Re-Join Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png) ](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span></span>


<span data-ttu-id="9d9ea-134">Si l’utilisateur est un administrateur sur l’appareil Windows 10, l’utilisateur peut désinsser l’appareil d’Azure AD et le rejoindre à nouveau.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-134">If the user is an administrator on the Windows 10 device, the user can unregister the device from Azure AD and re-join it again.</span></span> <span data-ttu-id="9d9ea-135">S’il n’a pas de privilèges d’administrateur, l’utilisateur a besoin des informations d’identification d’un compte d’administrateur local sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-135">If he has no administrator privileges, the user needs credentials of a local administrator account on this machine.</span></span> 


<span data-ttu-id="9d9ea-136">Un administrateur peut créer un compte d’administrateur local sur l’appareil en suivant ce chemin de configuration :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-136">An Administrator can create an local administrator account on the device following this configuration path:</span></span>

<span data-ttu-id="9d9ea-137">*Paramètres > comptes > autres comptes > informations d’identification inconnues > ajouter un utilisateur sans compte Microsoft*</span><span class="sxs-lookup"><span data-stu-id="9d9ea-137">*Settings > Accounts > Other Accounts > Credentials unknown > Add user without Microsoft-Account*</span></span>

### <a name="step-1-determine-if-the-device-is-azure-id-joined"></a><span data-ttu-id="9d9ea-138">Étape 1 : Déterminer si l’appareil est joint à Azure ID</span><span class="sxs-lookup"><span data-stu-id="9d9ea-138">Step 1: Determine if the device is Azure ID joined</span></span>
1.  <span data-ttu-id="9d9ea-139">Connectez-vous avec le courrier électronique et le mot de passe des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-139">Sign In with users E-mail and password.</span></span>
2.  <span data-ttu-id="9d9ea-140">Accédez à Paramètres > comptes > Access Work ou School.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-140">Go to Settings > Accounts > Access Work Or School.</span></span> 
3.  <span data-ttu-id="9d9ea-141">Rechercher un utilisateur dans la liste avec **connecté à... 's Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-141">Look for a user in the list with **connected to … ‘s Azure AD**.</span></span> 
4.  <span data-ttu-id="9d9ea-142">Si un utilisateur connecté existe, procédez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-142">If a connected user exists, proceed with Step 2.</span></span> <span data-ttu-id="9d9ea-143">Si ce n’est pas le cas, aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-143">If not, no further action is required.</span></span>
### <a name="step-2-disconnect-the-device-from-azure-ad"></a><span data-ttu-id="9d9ea-144">Étape 2 : Déconnecter l’appareil d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="9d9ea-144">Step 2: Disconnect the device from Azure AD</span></span>
1.  <span data-ttu-id="9d9ea-145">Appuyez sur Déconnectez-vous sur le compte scolaire ou scolaire ou scolaire connecté. </span><span class="sxs-lookup"><span data-stu-id="9d9ea-145">Tap **Disconnect** on the connected work or School Account.</span></span> 
2.  <span data-ttu-id="9d9ea-146">Confirmez la déconnexion deux fois.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-146">Confirm the disconnect twice.</span></span> 
3.  <span data-ttu-id="9d9ea-147">Entrez le nom d’utilisateur et le mot de passe de l’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-147">Enter the local administrator username and password.</span></span> <span data-ttu-id="9d9ea-148">L’appareil est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-148">The device is disconnected.</span></span>
4.  <span data-ttu-id="9d9ea-149">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-149">Restart the device.</span></span>
### <a name="step-3-join-the-device-to-azure-ad"></a><span data-ttu-id="9d9ea-150">Étape 3 : Joindre l’appareil à Azure AD</span><span class="sxs-lookup"><span data-stu-id="9d9ea-150">Step 3: Join the device to Azure AD</span></span>
1.  <span data-ttu-id="9d9ea-151">l’utilisateur se connexion avec les informations d’identification de l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="9d9ea-151">the user signs in with the credentials of the local administrator</span></span>
2.  <span data-ttu-id="9d9ea-152">Accédez **à Paramètres** **puis Comptes,** **puis Accéder au travail ou à l’établissement scolaire**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-152">Go to **Settings** then **Accounts** then **Access Work Or School**</span></span>
3.  <span data-ttu-id="9d9ea-153">Appuyez **sur Connecter**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-153">Tap **Connect**</span></span>
4.  <span data-ttu-id="9d9ea-154">**IMPORTANT**: **appuyez sur Rejoindre Azure AD**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-154">**IMPORTANT**: Tap **Join to Azure AD**</span></span>
5.  <span data-ttu-id="9d9ea-155">Entrez l’adresse de messagerie et le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-155">Enter the e-mail address and password of the user.</span></span> <span data-ttu-id="9d9ea-156">L’appareil est connecté</span><span class="sxs-lookup"><span data-stu-id="9d9ea-156">The device is connected</span></span>
6.  <span data-ttu-id="9d9ea-157">Redémarrer l’appareil</span><span class="sxs-lookup"><span data-stu-id="9d9ea-157">Restart the device</span></span> 
7.  <span data-ttu-id="9d9ea-158">se signer avec votre adresse de messagerie et votre mot de passe</span><span class="sxs-lookup"><span data-stu-id="9d9ea-158">sign with your e-mail address and password</span></span>

## <a name="azure-ad-registered-company-owned"></a><span data-ttu-id="9d9ea-159">Azure AD Registered (propriété de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="9d9ea-159">Azure AD Registered (Company owned)</span></span>

<span data-ttu-id="9d9ea-160">Pour déterminer si l’Windows 10 est inscrit à Azure AD, exécutez la commande suivante sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-160">To determine whether the Windows 10 device is Azure AD–registered, run the following command on the device:</span></span>

```console
%SystemRoot%\system32\dsregcmd.exe /status
```

<span data-ttu-id="9d9ea-161">Si l’appareil est enregistré dans Azure AD, vous verrez la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-161">If the device is Azure AD Registered, you would see the following output:</span></span>

```console
+----------------------------------------------------------------------+
| User State                                                           |
+----------------------------------------------------------------------+
           WorkplaceJoined : YES
          WamDefaultSet : NO
          WamDefaultAuthority : organizations
```

<span data-ttu-id="9d9ea-162">Pour supprimer le compte Azure AD existant sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-162">To remove the existing Azure AD-registered account on the device:</span></span>

- <span data-ttu-id="9d9ea-163">Pour supprimer le compte Azure AD enregistré sur l’appareil, utilisez CleanupWPJ, un outil que vous pouvez télécharger à partir [ d’ici :CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span><span class="sxs-lookup"><span data-stu-id="9d9ea-163">To remove the Azure AD–registered account on the device, use CleanupWPJ, a tool that you can download from here: [CleanupWPJ.zip](https://download.microsoft.com/download/8/e/f/8ef13ae0-6aa8-48a2-8697-5b1711134730/WPJCleanUp.zip).</span></span>

- <span data-ttu-id="9d9ea-164">Extrayez le fichier ZIP et exécutez **WPJCleanup.cmd**.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-164">Extract the ZIP file and run **WPJCleanup.cmd**.</span></span> <span data-ttu-id="9d9ea-165">Cet outil lance le bon exécutable en fonction de la version de Windows sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-165">This tool will launch the right executable based on the version of Windows on the device.</span></span>

- <span data-ttu-id="9d9ea-166">À l’aide d’un mécanisme tel que la stratégie de groupe, l’administrateur peut exécuter la commande sur l’appareil dans le contexte de tout utilisateur connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-166">By using a mechanism like Group Policy, the admin can run the command on the device in the context of any user who is signed in on the device.</span></span>

<span data-ttu-id="9d9ea-167">Pour désactiver les invites du Gestionnaire de comptes Web pour inscrire l’appareil dans Azure AD, ajoutez cette valeur de Registre :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-167">To disable Web Account Manager prompts to register the device in Azure AD, add this registry value:</span></span> 

- <span data-ttu-id="9d9ea-168">Emplacement : HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="9d9ea-168">Location: HKLM\SOFTWARE\Policies\Microsoft\Windows\WorkplaceJoin</span></span>
- <span data-ttu-id="9d9ea-169">Type : DWORD (32 bits)</span><span class="sxs-lookup"><span data-stu-id="9d9ea-169">Type: DWORD (32 bit)</span></span>
- <span data-ttu-id="9d9ea-170">Nom : BlockAADWorkplaceJoin</span><span class="sxs-lookup"><span data-stu-id="9d9ea-170">Name: BlockAADWorkplaceJoin</span></span>
- <span data-ttu-id="9d9ea-171">Données de valeur : 1</span><span class="sxs-lookup"><span data-stu-id="9d9ea-171">Value data: 1</span></span>

<span data-ttu-id="9d9ea-172">La présence de cette valeur de Registre doit bloquer l’accès à l’espace de travail et empêcher les utilisateurs de voir des invites pour rejoindre l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-172">The presence of this registry value should block workplace join and prevent users from seeing prompts to join the device.</span></span>

## <a name="android"></a><span data-ttu-id="9d9ea-173">Android</span><span class="sxs-lookup"><span data-stu-id="9d9ea-173">Android</span></span>

<span data-ttu-id="9d9ea-174">Pour Android, les utilisateurs doivent désins inscrire et réenregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-174">For Android, users will need to unregister and re-register their devices.</span></span> <span data-ttu-id="9d9ea-175">Vous pouvez le faire via l’application Microsoft Authenticator ou l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-175">This can be done via the Microsoft Authenticator app or the Company Portal app.</span></span> 

- <span data-ttu-id="9d9ea-176">À partir de Microsoft Authenticator’application, les utilisateurs peuvent Paramètres > **inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-176">From the Microsoft Authenticator app, users can go to **Settings > Device Registration**.</span></span> <span data-ttu-id="9d9ea-177">À partir de là, les utilisateurs peuvent désins inscrire et réenregistrer leur appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-177">From there users can unregister and re-register their device.</span></span>
 
- <span data-ttu-id="9d9ea-178">À partir de Portail d’entreprise, les utilisateurs peuvent se rendre sur l’onglet **Appareils** et supprimer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-178">From the Company Portal, users can go to **Devices** tab and remove the device.</span></span> <span data-ttu-id="9d9ea-179">Ensuite, réinscrivez l’appareil à l’aide Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-179">After that, re-enroll the device by using Company Portal.</span></span>
 
- <span data-ttu-id="9d9ea-180">Les utilisateurs peuvent également se désins inscrire et s’inscrire à la nouvelle inscription en supprimant le compte de la page des paramètres du compte, puis en ajoutant à nouveaux le compte de travail.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-180">Users can also unregister and re-register by removing the account from the account settings page and then re-adding the work account.</span></span>

<span data-ttu-id="9d9ea-181">Pour désins inscrire et réenregistrer l’appareil sur Android à l’aide Microsoft Authenticator application :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-181">To unregister and re-register the device on Android by using the Microsoft Authenticator app:</span></span>

1.  <span data-ttu-id="9d9ea-182">Ouvrez l Microsoft Authenticator appl; et Paramètres **.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-182">Open the Microsoft Authenticator app and go to **Settings**.</span></span>
2.  <span data-ttu-id="9d9ea-183">Sélectionnez **Inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-183">Select **Device registration**.</span></span>
3.  <span data-ttu-id="9d9ea-184">Désinsinser l’appareil en sélectionnant **Désinsinsion**.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-184">Unregister the device by selecting **Unregister**.</span></span>
4.  <span data-ttu-id="9d9ea-185">Pour **l’inscription de** l’appareil, ré-inscrivez l’appareil en tapant votre adresse e-mail, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-185">For **Device registration**, re-register the device by typing your email address, and then select **Register**.</span></span>

<span data-ttu-id="9d9ea-186">Pour désins inscrire et réenregistrer un appareil Android à l’Paramètres page :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-186">To unregister and re-register an Android device with the Android Settings page:</span></span>

1.  <span data-ttu-id="9d9ea-187">Ouvrez **Device Paramètres** et go to **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-187">Open **Device Settings** and go to **Accounts**.</span></span>
2.  <span data-ttu-id="9d9ea-188">Sélectionnez le compte de travail que vous souhaitez ré-inscrire et **sélectionnez Supprimer le compte.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-188">Select the work account that you want to re-register and select **Remove account**.</span></span>
3.  <span data-ttu-id="9d9ea-189">Une fois le compte supprimé, dans la **page** Comptes, sélectionnez Ajouter un **compte > compte de travail.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-189">After the account is removed, from the **Accounts** page, select **Add Account > Work account**.</span></span>
4.  <span data-ttu-id="9d9ea-190">Pour **Workplace Join,** tapez votre adresse e-mail et **sélectionnez Rejoindre** pour terminer l’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-190">For **Workplace Join**, type your email address and select **Join** to complete registering the device.</span></span>

<span data-ttu-id="9d9ea-191">Pour désins inscrire et réenregistrer l’appareil sur Android, Portail d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-191">To unregister and re-register the device on Android from Company Portal:</span></span>

1.  <span data-ttu-id="9d9ea-192">Lancez Portail d’entreprise et allez sur **l’onglet** Appareils.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-192">Launch Company Portal and go to **Devices** tab.</span></span>
2.  <span data-ttu-id="9d9ea-193">Sélectionnez l’appareil pour voir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-193">Select the device to see the device details.</span></span>
3.  <span data-ttu-id="9d9ea-194">Dans le menu des points de sélection (trois points), sélectionnez Supprimer l’appareil **et** terminez la suppression en confirmant dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-194">From the ellipses (three dots) menu, select **Remove Device**, and complete the removal by confirming in the dialog.</span></span>
4.  <span data-ttu-id="9d9ea-195">Vous devez maintenant être déconnecté de l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-195">You should now be logged out of the Company Portal app.</span></span> <span data-ttu-id="9d9ea-196">Sélectionnez **Se connectez** pour ré-inscrire l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-196">Select **Sign in** to re-register the device.</span></span>

<span data-ttu-id="9d9ea-197">Pour plus d’informations sur les actions requises pendant la phase de migration de cette charge de travail, ou sur l’impact sur l’administration ou l’utilisation, examinez les informations sur Azure Active Directory (Azure AD) dans Des informations [Azure AD](ms-cloud-germany-transition-azure-ad.md)supplémentaires pour la migration à partir de Microsoft Cloud Deutschland .</span><span class="sxs-lookup"><span data-stu-id="9d9ea-197">For more information about any actions required during the migration phase of this workload, or impact to administration or usage, review the information about Azure Active Directory (Azure AD) in [Additional Azure AD information for the migration from Microsoft Cloud Deutschland](ms-cloud-germany-transition-azure-ad.md).</span></span>

## <a name="ios"></a><span data-ttu-id="9d9ea-198">iOS</span><span class="sxs-lookup"><span data-stu-id="9d9ea-198">iOS</span></span>

<span data-ttu-id="9d9ea-199">Sur les appareils iOS, un utilisateur doit supprimer manuellement tous les comptes mis en cache de l’Microsoft Authenticator, désins inscrire l’appareil et se dé dé connecter à partir de toutes les applications natives de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-199">On iOS devices, a user will need to manually remove any cached accounts from the Microsoft Authenticator, unregister the device, and sign out from any native apps on the device.</span></span>

### <a name="step-1-if-present-remove-the-account-from-the-microsoft-authenticator-app"></a><span data-ttu-id="9d9ea-200">Étape 1 : si elle est présente, supprimez le compte de l’application Microsoft Authenticator client</span><span class="sxs-lookup"><span data-stu-id="9d9ea-200">Step 1: If present, remove the account from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="9d9ea-201">Appuyez sur le compte dans l Microsoft Authenticator appl;</span><span class="sxs-lookup"><span data-stu-id="9d9ea-201">Tap the account in the Microsoft Authenticator app.</span></span>
2. <span data-ttu-id="9d9ea-202">Appuyez sur **Paramètres** icône dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-202">Tap the **Settings** icon in the top-right corner.</span></span> <span data-ttu-id="9d9ea-203">Si vous ne voyez pas **l’icône Paramètres,** il se peut que vous n’utilisiez pas la dernière version de Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-203">If you don't see the **Settings** icon, you might not be using the latest version of Microsoft Authenticator.</span></span>
3. <span data-ttu-id="9d9ea-204">Appuyez sur **le bouton** Supprimer le compte.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-204">Tap the **Remove account** button.</span></span>
4. <span data-ttu-id="9d9ea-205">Appuyez **sur toutes les applications sur cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-205">Tap **All apps on this device**.</span></span>
 
### <a name="step-2-unregister-the-device-from-the-microsoft-authenticator-app"></a><span data-ttu-id="9d9ea-206">Étape 2 : Désinsser l’appareil de l Microsoft Authenticator appel</span><span class="sxs-lookup"><span data-stu-id="9d9ea-206">Step 2: Unregister the device from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="9d9ea-207">Appuyez sur l’icône de menu dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-207">Tap the menu icon in the top-right corner.</span></span>
2. <span data-ttu-id="9d9ea-208">Appuyez **Paramètres** puis inscription **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="9d9ea-208">Tap **Settings** and then **Device Registration**.</span></span>
4. <span data-ttu-id="9d9ea-209">Si votre compte s’affiche, **appuyez sur Désinsister l’appareil** et **continuez** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-209">If your account is shown, tap **Unregister device** and **Continue** in the dialog.</span></span> <span data-ttu-id="9d9ea-210">Vous ne devriez voir aucun compte après cela.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-210">You should see no account after that.</span></span>
 
### <a name="step-3-sign-out-from-individual-apps-if-necessary"></a><span data-ttu-id="9d9ea-211">Étape 3 : Se sortir des applications individuelles si nécessaire</span><span class="sxs-lookup"><span data-stu-id="9d9ea-211">Step 3: Sign out from individual apps if necessary</span></span>

<span data-ttu-id="9d9ea-212">Les utilisateurs peuvent se rendre sur des applications individuelles telles que Outlook, Teams et OneDrive, et supprimer des comptes de ces applications.</span><span class="sxs-lookup"><span data-stu-id="9d9ea-212">Users can go to individual apps like Outlook, Teams, and OneDrive, and remove accounts from those apps.</span></span>

## <a name="more-information"></a><span data-ttu-id="9d9ea-213">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9d9ea-213">More information</span></span>

<span data-ttu-id="9d9ea-214">Mise en place :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-214">Getting started:</span></span>

- [<span data-ttu-id="9d9ea-215">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centres de données allemandes</span><span class="sxs-lookup"><span data-stu-id="9d9ea-215">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="9d9ea-216">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="9d9ea-216">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="9d9ea-217">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="9d9ea-217">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="9d9ea-218">Expérience client pendant la migration</span><span class="sxs-lookup"><span data-stu-id="9d9ea-218">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="9d9ea-219">Transition :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-219">Moving through the transition:</span></span>

- [<span data-ttu-id="9d9ea-220">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="9d9ea-220">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="9d9ea-221">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="9d9ea-221">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="9d9ea-222">Informations supplémentaires pour [Azure AD,](ms-cloud-germany-transition-azure-ad.md) [les appareils,](ms-cloud-germany-transition-add-devices.md) [les expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="9d9ea-222">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="9d9ea-223">Applications cloud :</span><span class="sxs-lookup"><span data-stu-id="9d9ea-223">Cloud apps:</span></span>

- [<span data-ttu-id="9d9ea-224">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="9d9ea-224">Dynamics 365 migration program information</span></span>](/dynamics365/get-started/migrate-data-german-region)
- [<span data-ttu-id="9d9ea-225">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="9d9ea-225">Power BI migration program information</span></span>](/power-bi/admin/service-admin-migrate-data-germany)
- [<span data-ttu-id="9d9ea-226">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="9d9ea-226">Getting started with your Microsoft Teams upgrade</span></span>](/microsoftteams/upgrade-start-here)