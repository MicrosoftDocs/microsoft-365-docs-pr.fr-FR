---
title: Définir les paramètres de protection des applications pour les appareils Android ou iOS
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
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
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: 6f2b80b4-81c3-4714-a7bc-ae69313e8a33
description: Découvrez comment créer, modifier ou supprimer une stratégie de gestion des applications et protéger les fichiers de travail sur les appareils Android ou iOS.
ms.openlocfilehash: c0c8883fb120db90d81e57fbb80206d6ce4eccbf
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41593310"
---
# <a name="set-app-protection-settings-for-android-or-ios-devices"></a><span data-ttu-id="4a571-103">Définir les paramètres de protection des applications pour les appareils Android ou iOS</span><span class="sxs-lookup"><span data-stu-id="4a571-103">Set app protection settings for Android or iOS devices</span></span>

![Bannière pointant vers https://aka.ms/aboutM365preview.](media/m365admincenterchanging.png)

## <a name="create-an-app-management-policy"></a><span data-ttu-id="4a571-105">Créer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="4a571-105">Create an app management policy</span></span>

1. <span data-ttu-id="4a571-106">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="4a571-106">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span></span> 
    
2. <span data-ttu-id="4a571-107">Dans le volet de navigation de gauche, choisissez **Ajout**de **stratégies** \> de **périphériques** \> .</span><span class="sxs-lookup"><span data-stu-id="4a571-107">In the left nav, choose **Devices** \> **Policies** \> **Add**.</span></span>
  
3. <span data-ttu-id="4a571-108">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="4a571-108">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="4a571-109">Sous **type de stratégie**, sélectionnez **gestion des applications pour Android** ou **gestion des applications pour iOS**, en fonction de l’ensemble de stratégies que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="4a571-109">Under **Policy type**, choose **Application Management for Android** or **Application Management for iOS**, depending on which set of policies you want to create.</span></span> 
    
5. <span data-ttu-id="4a571-110">Développer **protéger les fichiers de travail en cas de perte ou de vol des appareils** et **gérer la manière dont les utilisateurs accèdent aux fichiers Office sur des appareils mobiles**.</span><span class="sxs-lookup"><span data-stu-id="4a571-110">Expand **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices**.</span></span> <span data-ttu-id="4a571-111">Configurez les paramètres de votre choix.</span><span class="sxs-lookup"><span data-stu-id="4a571-111">Configure the settings how you would like.</span></span> <span data-ttu-id="4a571-112">**Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** est **désactivé** par défaut, mais nous vous recommandons de l’activer et **d'** accepter les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a571-112">**Manage how users access Office files on mobile devices** is **Off** by default, but we recommend that you turn it **On** and accept the default values.</span></span> <span data-ttu-id="4a571-113">Pour plus d’informations, consultez la rubrique [available Settings](#available-settings).</span><span class="sxs-lookup"><span data-stu-id="4a571-113">For more information, see [Available settings](#available-settings).</span></span> 
    
    <span data-ttu-id="4a571-114">Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a571-114">You can always use the **Reset default settings** link to return to the default setting.</span></span> 
    
    ![Screenshot of Create a policy with Application management for Android selected](media/eabbe06d-ac0a-4f3a-8630-68c808b1e662.png)
  
6. <span data-ttu-id="4a571-116">Maintenant, définissez **Qui recevra ces paramètres ?**</span><span class="sxs-lookup"><span data-stu-id="4a571-116">Next decide **Who will get these settings?**</span></span> <span data-ttu-id="4a571-117">Si vous ne souhaitez pas utiliser le groupe de sécurité par défaut **tous les utilisateurs** , choisissez **modifier**, puis \> **Sélectionnez**les groupes de sécurité qui obtiennent ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="4a571-117">If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups that get these settings \> **Select**.</span></span>
    
7. <span data-ttu-id="4a571-118">Enfin, sélectionnez **Terminé** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="4a571-118">Finally, choose **Done** to save the policy, and assign it to devices.</span></span> 
    
## <a name="edit-an-app-management-policy"></a><span data-ttu-id="4a571-119">Modifier une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="4a571-119">Edit an app management policy</span></span>

1. <span data-ttu-id="4a571-120">Dans la fiche **stratégies** , choisissez **modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="4a571-120">On the **Policies** card, choose **Edit policy**.</span></span>
    
2. <span data-ttu-id="4a571-121">Dans le volet **Modifier une stratégie**, sélectionnez la stratégie que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="4a571-121">On the **Edit policy** pane, choose the policy you want to change</span></span> 
    
3. <span data-ttu-id="4a571-122">Sélectionnez **Modifier** en regard de chaque paramètre pour modifier les valeurs de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4a571-122">Choose **Edit** next to each setting to change the values in the policy.</span></span> <span data-ttu-id="4a571-123">Lorsque vous modifiez une valeur, elle est automatiquement enregistrée dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="4a571-123">When you change a value, it's automatically saved in the policy.</span></span>
    
4. <span data-ttu-id="4a571-124">Lorsque vous avez terminé, fermez le volet **modifier la stratégie** .</span><span class="sxs-lookup"><span data-stu-id="4a571-124">When you're finished, close the **Edit policy** pane.</span></span> 
    
## <a name="delete-an-app-management-policy"></a><span data-ttu-id="4a571-125">Supprimer une stratégie de gestion des applications</span><span class="sxs-lookup"><span data-stu-id="4a571-125">Delete an app management policy</span></span>

1. <span data-ttu-id="4a571-126">Sur la page **stratégies** , sélectionnez une stratégie, puis **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="4a571-126">On the **Policies** page, choose a policy and then **Delete**.</span></span>
    
2. <span data-ttu-id="4a571-127">Dans le volet **Supprimer la stratégie** , sélectionnez **confirmer** pour supprimer la ou les stratégies que vous avez choisies.</span><span class="sxs-lookup"><span data-stu-id="4a571-127">On the **Delete policy** pane, choose **Confirm** to delete the policy or policies you chose.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="4a571-128">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="4a571-128">Available settings</span></span>

<span data-ttu-id="4a571-129">Les tableaux suivants fournissent des informations détaillées sur les paramètres disponibles pour protéger les fichiers de travail sur les appareils et les paramètres qui contrôlent la façon dont les utilisateurs accèdent aux fichiers Office à partir de leurs appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4a571-129">The following tables give detailed information about settings available to protect work files on devices and the settings that control how users access Office files from their mobile devices.</span></span>
  
 <span data-ttu-id="4a571-130">Pour plus d'informations, voir [Correspondance entre les fonctionnalités de protection de Microsoft 365 Business et les paramètres Intune](map-protection-features-to-intune-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4a571-130">For more information, see [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md).</span></span> 
  
### <a name="settings-that-protect-work-files"></a><span data-ttu-id="4a571-131">Paramètres de protection des fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="4a571-131">Settings that protect work files</span></span>

<span data-ttu-id="4a571-132">Les paramètres suivants sont disponibles pour protéger les fichiers professionnels si l'appareil d'un utilisateur est perdu ou volé :</span><span class="sxs-lookup"><span data-stu-id="4a571-132">The following settings are available to protect work files if a user's device is lost or stolen:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a571-133">Setting</span><span class="sxs-lookup"><span data-stu-id="4a571-133">Setting</span></span>  <br/> |<span data-ttu-id="4a571-134">Description</span><span class="sxs-lookup"><span data-stu-id="4a571-134">Description</span></span>  <br/> |
|<span data-ttu-id="4a571-135">Supprimer les fichiers professionnels d'un appareil inactif après tant de jours</span><span class="sxs-lookup"><span data-stu-id="4a571-135">Delete work files from an inactive device after this many days</span></span>  <br/> |<span data-ttu-id="4a571-136">Si un appareil n’est pas utilisé pendant le nombre de jours que vous spécifiez ici, tous les fichiers de travail stockés sur l’appareil seront automatiquement supprimés.</span><span class="sxs-lookup"><span data-stu-id="4a571-136">If a device isn't used for the number of days that you specify here, any work files stored on the device will be deleted automatically.</span></span>  <br/> |
|<span data-ttu-id="4a571-137">Obliger les utilisateurs à enregistrer tous les fichiers de travail dans OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="4a571-137">Force users to save all work files to OneDrive for Business</span></span>  <br/> |<span data-ttu-id="4a571-138">Si ce paramètre est **activé**, la seule emplacement d’enregistrement disponible pour les fichiers de travail est OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="4a571-138">If this setting is **On**, the only available save location for work files is OneDrive for Business.</span></span>  <br/> |
|<span data-ttu-id="4a571-139">Chiffrer les fichiers professionnels</span><span class="sxs-lookup"><span data-stu-id="4a571-139">Encrypt work files</span></span>  <br/> |<span data-ttu-id="4a571-140">Laissez ce paramètre **activé** afin que les fichiers professionnels soient protégés par chiffrement.</span><span class="sxs-lookup"><span data-stu-id="4a571-140">Keep this setting **On** so that work files are protected by encryption.</span></span> <span data-ttu-id="4a571-141">Même si l’appareil est perdu ou volé, personne ne peut lire les données de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4a571-141">Even if the device is lost or stolen, no one can read your company data.</span></span>  <br/> |
   
### <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="4a571-142">Paramètres qui contrôlent la façon dont les utilisateurs accèdent aux fichiers Office sur appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="4a571-142">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="4a571-143">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :</span><span class="sxs-lookup"><span data-stu-id="4a571-143">The following settings are available to manage how users access Office work files:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a571-144">Setting</span><span class="sxs-lookup"><span data-stu-id="4a571-144">Setting</span></span>  <br/> |<span data-ttu-id="4a571-145">Description</span><span class="sxs-lookup"><span data-stu-id="4a571-145">Description</span></span>  <br/> |
|<span data-ttu-id="4a571-146">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="4a571-146">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="4a571-147">Si ce paramètre est **activé** , les utilisateurs doivent fournir une autre forme d’authentification, en plus de leur nom d’utilisateur et de leur mot de passe, avant de pouvoir utiliser les applications Office sur leurs appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="4a571-147">If this setting is **On** users must provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile devices.</span></span><br/> |
|<span data-ttu-id="4a571-148">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="4a571-148">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="4a571-149">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="4a571-149">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="4a571-150">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="4a571-150">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="4a571-151">Ce paramètre détermine la durée pendant laquelle un utilisateur peut être inactif avant d’être invité à se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="4a571-151">This setting determines how long a user can be idle before they're prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="4a571-152">Refuser l'accès aux fichiers de travail sur les appareils « jailbreakés » ou débridés</span><span class="sxs-lookup"><span data-stu-id="4a571-152">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="4a571-p105">Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté. Cela signifie que l'utilisateur est en mesure de modifier le système d'exploitation, ce qui peut rendre l'appareil plus vulnérable aux logiciels malveillants. Ces appareils sont bloqués lorsque ce paramètre est **activé**.  </span><span class="sxs-lookup"><span data-stu-id="4a571-p105">Clever users may have a device that is jailbroken or rooted. This means that the user can modify the operating system, which can make the device more subject to malware. These devices are blocked when this setting is **On**.  </span></span><br/> |
|<span data-ttu-id="4a571-156">Autoriser les utilisateurs à copier le contenu des applications Office dans des applications personnelles</span><span class="sxs-lookup"><span data-stu-id="4a571-156">Allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="4a571-157">Cela est interdit par défaut, mais si le paramètre est **activé**, l'utilisateur peut copier des informations d'un fichier professionnel vers un fichier personnel.</span><span class="sxs-lookup"><span data-stu-id="4a571-157">We do allow this by default, but if the setting is **On**, the user could copy information in a work file to a personal file.</span></span> <span data-ttu-id="4a571-158">Si le paramètre est **désactivé**, l'utilisateur ne peut pas copier d'informations à partir d'un compte professionnel vers une application personnelle ou un compte personnel.</span><span class="sxs-lookup"><span data-stu-id="4a571-158">If the setting is **Off**, the user will be unable to copy information from a work account into a personal app or personal account.</span></span>  <br/> |
