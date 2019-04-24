---
title: Définir les paramètres de protection des applications pour les appareils Android ou iOS
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6f2b80b4-81c3-4714-a7bc-ae69313e8a33
description: Découvrez comment créer, modifier ou supprimer une stratégie de gestion des applications et protéger les fichiers de travail sur les appareils Android ou iOS.
ms.openlocfilehash: e81ff8a4bd71dbbbf7ccc31249d450e03f4bd241
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32277445"
---
# <a name="set-app-protection-settings-for-android-or-ios-devices"></a><span data-ttu-id="c18ef-103">Définir les paramètres de protection des applications pour les appareils Android ou iOS</span><span class="sxs-lookup"><span data-stu-id="c18ef-103">Set app protection settings for Android or iOS devices</span></span>

## <a name="create-an-app-management-policy"></a><span data-ttu-id="c18ef-104">Créer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="c18ef-104">Create an app management policy</span></span>

1. <span data-ttu-id="c18ef-105">Connectez-vous au [Centre d'administration de Microsoft 365](https://go.microsoft.com/fwlink/p/?linkid=837890) avec les informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="c18ef-105">Sign in to [Microsoft 365 Business admin center ](https://go.microsoft.com/fwlink/p/?linkid=837890) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="c18ef-106">Dans le centre d'administration, choisissez **stratégies** \> de **périphériques** \> **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="c18ef-106">In the admin center, choose **Devices** \> **Policies** \> **Add policy**.</span></span>
  
3. <span data-ttu-id="c18ef-107">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="c18ef-107">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="c18ef-108">Sous **Type de stratégie**, sélectionnez **Gestion des applications pour Android** ou **Gestion des applications pour iOS** selon l'ensemble de stratégies que vous voulez créer.</span><span class="sxs-lookup"><span data-stu-id="c18ef-108">Under **Policy type**, choose **Application Management for Android** or **Application Management for iOS** depending on which set of policies you want to create.</span></span> 
    
5. <span data-ttu-id="c18ef-109">Expand **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** \> configure the settings how you would like.</span><span class="sxs-lookup"><span data-stu-id="c18ef-109">Expand **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** \> configure the settings how you would like.</span></span> <span data-ttu-id="c18ef-110">The **Manage how users access Office files on mobile devices** is **Off** by default, but it is recommended that you turn it **On** and accept the default values.</span><span class="sxs-lookup"><span data-stu-id="c18ef-110">The **Manage how users access Office files on mobile devices** is **Off** by default, but it is recommended that you turn it **On** and accept the default values.</span></span> <span data-ttu-id="c18ef-111">Pour plus d'informations, consultez la section [paramètres disponibles](#available-settings) .</span><span class="sxs-lookup"><span data-stu-id="c18ef-111">See [Available settings](#available-settings)  for more information.</span></span> 
    
    <span data-ttu-id="c18ef-112">Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c18ef-112">You can always use the **Reset default settings** link to return to the default setting.</span></span> 
    
    ![Screenshot of Create a policy with Application management for Android selected](media/eabbe06d-ac0a-4f3a-8630-68c808b1e662.png)
  
6. <span data-ttu-id="c18ef-p102">Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis les groupes de sécurité qui recevront ces paramètres \> **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="c18ef-p102">Next decide **Who will get these settings?** If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups who will get these settings \> **Select**.</span></span>
    
7. <span data-ttu-id="c18ef-116">Enfin, sélectionnez **Terminé** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="c18ef-116">Finally, choose **Done** to save the policy, and assign it to devices.</span></span> 
    
## <a name="edit-an-app-management-policy"></a><span data-ttu-id="c18ef-117">Modifier une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="c18ef-117">Edit an app management policy</span></span>

1. <span data-ttu-id="c18ef-118">Dans la fiche **stratégies** , choisissez **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="c18ef-118">On the **Policies** card, choose **Edit policy**.</span></span>
    
2. <span data-ttu-id="c18ef-119">Dans le volet **Modifier une stratégie**, sélectionnez la stratégie que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="c18ef-119">On the **Edit policy** pane, choose the policy you want to change</span></span> 
    
3. <span data-ttu-id="c18ef-p103">Sélectionnez **Modifier** en regard de chaque paramètre pour modifier les valeurs de la stratégie. Lorsque vous modifiez une valeur, celle-ci est enregistrée automatiquement dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="c18ef-p103">Choose **Edit** next to each setting to change the values in the policy. When you change a value, it is automatically saved into the policy</span></span> 
    
4. <span data-ttu-id="c18ef-122">Lorsque vous avez terminé, fermez le volet **Modifier une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="c18ef-122">When you are finished, close the **Edit policy** pane.</span></span> 
    
## <a name="delete-an-app-management-policy"></a><span data-ttu-id="c18ef-123">Supprimer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="c18ef-123">Delete an app management policy</span></span>

1. <span data-ttu-id="c18ef-124">On the **Policies** card, choose **Delete policy**.</span><span class="sxs-lookup"><span data-stu-id="c18ef-124">On the **Policies** card, choose **Delete policy**.</span></span>
    
2. <span data-ttu-id="c18ef-125">Dans le volet **Supprimer la stratégie**, sélectionnez les stratégies à supprimer \> **Sélectionner**, puis **Confirmer** pour supprimer la ou les stratégies que vous avez sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="c18ef-125">On the **Delete policy** pane, choose the policies you want to delete \> **Select**, then **Confirm** to delete the policy or policies you chose.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="c18ef-126">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="c18ef-126">Available settings</span></span>

<span data-ttu-id="c18ef-127">Les tableaux suivants donnent des informations détaillées sur les paramètres dont vous disposez pour protéger les fichiers professionnels sur les appareils et sur les paramètres qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office à partir de leurs appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c18ef-127">The following tables give detailed information about the available settings to protect work files on devices and the settings that control how users access Office files from their mobile devices.</span></span>
  
 <span data-ttu-id="c18ef-128">Pour plus d'informations, voir [Correspondance entre les fonctionnalités de protection de Microsoft 365 Business et les paramètres Intune](map-protection-features-to-intune-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c18ef-128">See [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md) for more information.</span></span> 
  
### <a name="settings-that-protect-work-files"></a><span data-ttu-id="c18ef-129">Paramètres de protection des fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="c18ef-129">Settings that protect work files</span></span>

<span data-ttu-id="c18ef-130">Les paramètres suivants sont disponibles pour protéger les fichiers professionnels si l'appareil d'un utilisateur est perdu ou volé :</span><span class="sxs-lookup"><span data-stu-id="c18ef-130">The following settings are available to protect work files if a user's device is lost or stolen:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c18ef-131">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c18ef-131">Setting</span></span>  <br/> |<span data-ttu-id="c18ef-132">Description</span><span class="sxs-lookup"><span data-stu-id="c18ef-132">Description</span></span>  <br/> |
|<span data-ttu-id="c18ef-133">Supprimer les fichiers professionnels d'un appareil inactif après tant de jours</span><span class="sxs-lookup"><span data-stu-id="c18ef-133">Delete work files from an inactive device after this many days</span></span>  <br/> |<span data-ttu-id="c18ef-134">Si un appareil n'est pas utilisé pendant le nombre de jours que vous spécifiez ici, les fichiers professionnels stockés sur l'appareil sont automatiquement supprimés.</span><span class="sxs-lookup"><span data-stu-id="c18ef-134">If a device is not used for the number of days that you specify here, any work files stored on the device will automatically be deleted.</span></span>  <br/> |
|<span data-ttu-id="c18ef-135">Obliger les utilisateurs à enregistrer tous les fichiers de travail dans OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="c18ef-135">Force users to save all work files to OneDrive for Business</span></span>  <br/> |<span data-ttu-id="c18ef-136">Si ce paramètre est **activé**, le seul emplacement d'enregistrement accessible pour les fichiers professionnels sera OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="c18ef-136">If this setting is **On**, the only available save location for work files will be OneDrive for Business.</span></span>  <br/> |
|<span data-ttu-id="c18ef-137">Chiffrer les fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="c18ef-137">Encrypt work files</span></span>  <br/> |<span data-ttu-id="c18ef-p104">Laissez ce paramètre **activé** afin que les fichiers professionnels soient protégés par chiffrement. Même si l'appareil est perdu ou volé, personne ne sera en mesure de lire les données de votre société.  </span><span class="sxs-lookup"><span data-stu-id="c18ef-p104">Keep this setting **On** so that work files are protected by encryption. Even if the device is lost or stolen, no one will be able to read your company data.  </span></span><br/> |
   
### <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="c18ef-140">Paramètres qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="c18ef-140">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="c18ef-141">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :</span><span class="sxs-lookup"><span data-stu-id="c18ef-141">The following settings are available to manage how users access Office work files:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c18ef-142">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c18ef-142">Setting</span></span>  <br/> |<span data-ttu-id="c18ef-143">Description</span><span class="sxs-lookup"><span data-stu-id="c18ef-143">Description</span></span>  <br/> |
|<span data-ttu-id="c18ef-144">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="c18ef-144">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="c18ef-145">Si ce paramètre est **activé**, les utilisateurs doivent fournir une autre forme d'authentification, en plus de leur nom d'utilisateur et de leur mot de passe, pour pouvoir utiliser les applications Office sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="c18ef-145">If this settings is **On** users have to provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="c18ef-146">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="c18ef-146">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="c18ef-147">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="c18ef-147">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="c18ef-148">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="c18ef-148">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="c18ef-149">Ce paramètre détermine combien de temps un utilisateur peut être inactif avant d'être invité à se connecter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="c18ef-149">This setting determines how long a user can be idle before they are prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="c18ef-150">Refuser l'accès aux fichiers de travail sur les appareils « jailbreakés » ou débridés</span><span class="sxs-lookup"><span data-stu-id="c18ef-150">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="c18ef-p105">Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté. Cela signifie que l'utilisateur est en mesure de modifier le système d'exploitation, ce qui peut rendre l'appareil plus vulnérable aux logiciels malveillants. Ces appareils sont bloqués lorsque ce paramètre est **activé**.  </span><span class="sxs-lookup"><span data-stu-id="c18ef-p105">Clever users may have a device that is jailbroken or rooted. This means that the user can modify the operating system, which can make the device more subject to malware. These devices are blocked when this setting is **On**.  </span></span><br/> |
|<span data-ttu-id="c18ef-154">Autoriser les utilisateurs à copier le contenu des applications Office dans des applications personnelles</span><span class="sxs-lookup"><span data-stu-id="c18ef-154">Allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="c18ef-155">Cela est interdit par défaut, mais si le paramètre est **activé**, l'utilisateur peut copier des informations d'un fichier professionnel vers un fichier personnel.</span><span class="sxs-lookup"><span data-stu-id="c18ef-155">We do allow this by default, but if the setting is **On**, the user could copy information in a work file to a personal file.</span></span> <span data-ttu-id="c18ef-156">Si le paramètre est **désactivé**, l'utilisateur ne peut pas copier d'informations à partir d'un compte professionnel vers une application personnelle ou un compte personnel.</span><span class="sxs-lookup"><span data-stu-id="c18ef-156">If the setting is **Off**, the user will be unable to copy information from a work account into a personal app or personal account.</span></span>  <br/> |
   

  

