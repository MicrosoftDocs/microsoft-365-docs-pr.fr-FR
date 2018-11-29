---
title: Définir les paramètres de protection des applications pour les appareils Android ou iOS
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6f2b80b4-81c3-4714-a7bc-ae69313e8a33
description: Découvrez comment créer, modifier, ou supprimer une stratégie de gestion des applications et protéger les fichiers de travail sur les appareils Android ou iOS.
ms.openlocfilehash: ed03227496120369b94bf2396974eebfd7798678
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867409"
---
# <a name="set-app-protection-settings-for-android-or-ios-devices"></a><span data-ttu-id="72e12-103">Définir les paramètres de protection des applications pour les appareils Android ou iOS</span><span class="sxs-lookup"><span data-stu-id="72e12-103">Set app protection settings for Android or iOS devices</span></span>

## <a name="create-an-app-management-policy"></a><span data-ttu-id="72e12-104">Créer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="72e12-104">Create an app management policy</span></span>

1. <span data-ttu-id="72e12-105">Connectez-vous à [Microsoft 365 Business](https://portal.office.com) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="72e12-105">Sign in to [Microsoft 365 Business](https://portal.office.com) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="72e12-106">Dans la carte **Stratégies d'appareil** du Centre d'administration, sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="72e12-106">In the admin center, on the **Device policies** card, choose **Add policy**.</span></span>
    
    ![Device policies card in the admin center.](media/27c12b61-d112-4348-b557-4f3e46204797.png)
  
3. <span data-ttu-id="72e12-108">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="72e12-108">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="72e12-109">Sous **Type de stratégie**, sélectionnez **Gestion des applications pour Android** ou **Gestion des applications pour iOS** selon l'ensemble de stratégies que vous voulez créer.</span><span class="sxs-lookup"><span data-stu-id="72e12-109">Under **Policy type**, choose **Application Management for Android** or **Application Management for iOS** depending on which set of policies you want to create.</span></span> 
    
5. <span data-ttu-id="72e12-p101">Développez **protéger les fichiers de travail lorsque les périphériques sont perdus ou volés** et **gérer comment les utilisateurs d’accès aux fichiers Office sur des appareils mobiles** \> configurer les paramètres des manière dont vous souhaitez. **Gérer comment les utilisateurs d’accès aux fichiers Office sur des appareils mobiles** est **désactivée** par défaut, mais il est recommandé que vous **allumez** et acceptez les valeurs par défaut. Pour plus d’informations, voir [paramètres disponibles](app-protection-settings-for-android-and-ios.md#bkmk_availablesettings) .</span><span class="sxs-lookup"><span data-stu-id="72e12-p101">Expand **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** \> configure the settings how you would like. The **Manage how users access Office files on mobile devices** is **Off** by default, but it is recommended that you turn it **On** and accept the default values. See [Available settings](app-protection-settings-for-android-and-ios.md#bkmk_availablesettings) for more information.</span></span> 
    
    <span data-ttu-id="72e12-113">Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="72e12-113">You can always use the **Reset default settings** link to return to the default setting.</span></span> 
    
    ![Screenshot of Create a policy with Application management for Android selected](media/eabbe06d-ac0a-4f3a-8630-68c808b1e662.png)
  
6. <span data-ttu-id="72e12-p102">Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis les groupes de sécurité qui recevront ces paramètres \> **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="72e12-p102">Next decide **Who will get these settings?** If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups who will get these settings \> **Select**.</span></span>
    
7. <span data-ttu-id="72e12-117">Enfin, sélectionnez **Terminé** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="72e12-117">Finally, choose **Done** to save the policy, and assign it to devices.</span></span> 
    
## <a name="edit-an-app-management-policy"></a><span data-ttu-id="72e12-118">Modifier une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="72e12-118">Edit an app management policy</span></span>

1. <span data-ttu-id="72e12-119">Sur la carte de **stratégies** , cliquez sur **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="72e12-119">On the **Policies** card, choose **Edit policy**.</span></span>
    
2. <span data-ttu-id="72e12-120">Dans le volet **Modifier une stratégie**, sélectionnez la stratégie que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="72e12-120">On the **Edit policy** pane, choose the policy you want to change</span></span> 
    
3. <span data-ttu-id="72e12-p103">Sélectionnez **Modifier** en regard de chaque paramètre pour modifier les valeurs de la stratégie. Lorsque vous modifiez une valeur, celle-ci est enregistrée automatiquement dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="72e12-p103">Choose **Edit** next to each setting to change the values in the policy. When you change a value, it is automatically saved into the policy</span></span> 
    
4. <span data-ttu-id="72e12-123">Lorsque vous avez terminé, fermez le volet **Modifier une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="72e12-123">When you are finished, close the **Edit policy** pane.</span></span> 
    
## <a name="delete-an-app-management-policy"></a><span data-ttu-id="72e12-124">Supprimer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="72e12-124">Delete an app management policy</span></span>

1. <span data-ttu-id="72e12-125">Sur la carte de **stratégies** , cliquez sur **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="72e12-125">On the **Policies** card, choose **Delete policy**.</span></span>
    
2. <span data-ttu-id="72e12-126">Dans le volet **Supprimer la stratégie**, sélectionnez les stratégies à supprimer \> **Sélectionner**, puis **Confirmer** pour supprimer la ou les stratégies que vous avez sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="72e12-126">On the **Delete policy** pane, choose the policies you want to delete \> **Select**, then **Confirm** to delete the policy or policies you chose.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="72e12-127">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="72e12-127">Available settings</span></span>

<span data-ttu-id="72e12-128">Les tableaux suivants donnent des informations détaillées sur les paramètres dont vous disposez pour protéger les fichiers professionnels sur les appareils et sur les paramètres qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office à partir de leurs appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="72e12-128">The following tables give detailed information about the available settings to protect work files on devices and the settings that control how users access Office files from their mobile devices.</span></span>
  
 <span data-ttu-id="72e12-129">Pour plus d'informations, voir [Correspondance entre les fonctionnalités de protection de Microsoft 365 Business et les paramètres Intune](map-protection-features-to-intune-settings.md).</span><span class="sxs-lookup"><span data-stu-id="72e12-129">See [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md) for more information.</span></span> 
  
### <a name="settings-that-protect-work-files"></a><span data-ttu-id="72e12-130">Paramètres de protection des fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="72e12-130">Settings that protect work files</span></span>

<span data-ttu-id="72e12-131">Les paramètres suivants sont disponibles pour protéger les fichiers professionnels si l'appareil d'un utilisateur est perdu ou volé :</span><span class="sxs-lookup"><span data-stu-id="72e12-131">The following settings are available to protect work files if a user's device is lost or stolen:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72e12-132">Paramètre</span><span class="sxs-lookup"><span data-stu-id="72e12-132">Setting</span></span>  <br/> |<span data-ttu-id="72e12-133">Description</span><span class="sxs-lookup"><span data-stu-id="72e12-133">Description</span></span>  <br/> |
|<span data-ttu-id="72e12-134">Supprimer les fichiers professionnels d'un appareil inactif après tant de jours</span><span class="sxs-lookup"><span data-stu-id="72e12-134">Delete work files from an inactive device after this many days</span></span>  <br/> |<span data-ttu-id="72e12-135">Si un appareil n'est pas utilisé pendant le nombre de jours que vous spécifiez ici, les fichiers professionnels stockés sur l'appareil sont automatiquement supprimés.</span><span class="sxs-lookup"><span data-stu-id="72e12-135">If a device is not used for the number of days that you specify here, any work files stored on the device will automatically be deleted.</span></span>  <br/> |
|<span data-ttu-id="72e12-136">Obliger les utilisateurs à enregistrer tous les fichiers de travail dans OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="72e12-136">Force users to save all work files to OneDrive for Business</span></span>  <br/> |<span data-ttu-id="72e12-137">Si ce paramètre est **activé**, le seul emplacement d'enregistrement accessible pour les fichiers professionnels sera OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="72e12-137">If this setting is **On**, the only available save location for work files will be OneDrive for Business.</span></span>  <br/> |
|<span data-ttu-id="72e12-138">Chiffrer les fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="72e12-138">Encrypt work files</span></span>  <br/> |<span data-ttu-id="72e12-p104">Laissez ce paramètre **activé** afin que les fichiers professionnels soient protégés par chiffrement. Même si l'appareil est perdu ou volé, personne ne sera en mesure de lire vos données d'entreprise.  </span><span class="sxs-lookup"><span data-stu-id="72e12-p104">Keep this setting **On** so that work files are protected by encryption. Even if the device is lost or stolen, no one will be able to read your company data.  </span></span><br/> |
   
### <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="72e12-141">Paramètres qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="72e12-141">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="72e12-142">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :</span><span class="sxs-lookup"><span data-stu-id="72e12-142">The following settings are available to manage how users access Office work files:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72e12-143">Paramètre</span><span class="sxs-lookup"><span data-stu-id="72e12-143">Setting</span></span>  <br/> |<span data-ttu-id="72e12-144">Description</span><span class="sxs-lookup"><span data-stu-id="72e12-144">Description</span></span>  <br/> |
|<span data-ttu-id="72e12-145">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="72e12-145">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="72e12-146">Si ce paramètre est **activé**, les utilisateurs doivent fournir une autre forme d'authentification, en plus de leur nom d'utilisateur et de leur mot de passe, pour pouvoir utiliser les applications Office sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="72e12-146">If this settings is **On** users have to provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="72e12-147">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="72e12-147">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="72e12-148">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="72e12-148">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="72e12-149">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="72e12-149">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="72e12-150">Ce paramètre détermine combien de temps un utilisateur peut être inactif avant d'être invité à se connecter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="72e12-150">This setting determines how long a user can be idle before they are prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="72e12-151">Refuser l'accès aux fichiers professionnels sur les appareils « jailbreakés » ou « rootés »</span><span class="sxs-lookup"><span data-stu-id="72e12-151">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="72e12-p105">Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté. Cela signifie que l'utilisateur est en mesure de modifier le système d'exploitation, ce qui peut rendre l'appareil plus vulnérable aux programmes malveillants. Ces appareils sont bloqués lorsque ce paramètre est **activé**.  </span><span class="sxs-lookup"><span data-stu-id="72e12-p105">Clever users may have a device that is jailbroken or rooted. This means that the user can modify the operating system, which can make the device more subject to malware. These devices are blocked when this setting is **On**.  </span></span><br/> |
|<span data-ttu-id="72e12-155">Autoriser les utilisateurs à copier le contenu des applications Office dans des applications personnelles</span><span class="sxs-lookup"><span data-stu-id="72e12-155">Allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="72e12-p106">Nous le permettent par défaut, mais si le paramètre est **activé**, l’utilisateur peut copier des informations dans un fichier de travail à un fichier personnel. Si le paramètre est **désactivé**, l’utilisateur ne pourront pas copier les informations d’un compte dans une application personnelle ou un compte personnel.</span><span class="sxs-lookup"><span data-stu-id="72e12-p106">We do allow this by default, but if the setting is **On**, the user could copy information in a work file to a personal file. If the setting is **Off**, the user will be unable to copy information from a work account into a personal app or personal account.  </span></span><br/> |
   

  

