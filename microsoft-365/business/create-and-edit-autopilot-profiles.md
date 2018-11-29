---
title: Créer et modifier des profils AutoPilot
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
- MOE150
ms.assetid: 5cf7139e-cfa1-4765-8aad-001af1c74faa
description: 'Apprenez à créer, modifier, supprimer ou supprimer des profils en pilote automatique. '
ms.openlocfilehash: 4658a27e5f2c64a52f8a7d08b3fc13df5e239dc3
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867143"
---
# <a name="create-and-edit-autopilot-profiles"></a><span data-ttu-id="32c6c-103">Créer et modifier des profils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="32c6c-103">Create and edit AutoPilot profiles</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="32c6c-104">Créer un profil</span><span class="sxs-lookup"><span data-stu-id="32c6c-104">Create a profile</span></span>

<span data-ttu-id="32c6c-105">Un profil s'applique à un appareil ou à un groupe d'appareils,</span><span class="sxs-lookup"><span data-stu-id="32c6c-105">A profile applies to a device, or a group of devices,</span></span>
  
1. <span data-ttu-id="32c6c-106">Dans le Centre d'administration Microsoft 365 Entreprise, choisissez **Déployer Windows avec AutoPilot** sur la carte **Actions d'appareil**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-106">In the Microsoft 365 Business Admin center, choose **Deploy Windows with AutoPilot** on the **Device actions** card.</span></span> 
    
    ![On the Device actions card, choose Deploy Windows with Autopilot.](media/160d5c2a-11a8-48f9-a8aa-70f084b85448.png)
  
2. <span data-ttu-id="32c6c-108">Sur la page **Préparer Windows**, choisissez l'onglet **Profils** \> **Créer un profil**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-108">On the **Prepare Windows** page, choose the **Profiles** tab \> **Create profile**.</span></span>
    
3. <span data-ttu-id="32c6c-109">Sur la page **Créer un profil**, entrez un nom de profil qui vous permette de l'identifier, par exemple Marketing, activez le paramètre souhaité (voir [À propos des paramètres de profil AutoPilot](autopilot-profile-settings.md) pour plus d'informations), puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-109">On the **Create profile** page, enter a name for the profile that helps you identify it, for example Marketing, turn on the setting you want (see [About AutoPilot Profile settings](autopilot-profile-settings.md) for more information), and choose **Save**.</span></span>
    
    ![Enter name and turn on settings in the Create profile panel.](media/63b5a00d-6a5d-48d0-9557-e7531e80702a.png)
  
### <a name="apply-profile-to-a-device"></a><span data-ttu-id="32c6c-111">Appliquer le profil à un appareil</span><span class="sxs-lookup"><span data-stu-id="32c6c-111">Apply profile to a device</span></span>

<span data-ttu-id="32c6c-p101">Après avoir créé un profil, vous pouvez l'appliquer à un appareil ou à un groupe d'appareils. Vous pouvez sélectionner un profil existant dans la [guide détaillé](add-autopilot-devices-and-profile.md), l'appliquer aux nouveaux appareils ou remplacer un profil existant pour un appareil ou un groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="32c6c-p101">After you create a profile you can apply it to a device or a group of devices. You can pick an existing profile in the [step-by-step guide](add-autopilot-devices-and-profile.md), you can apply it to new devices, or you can replace an existing profile for a device or group of devices.</span></span> 
  
1. <span data-ttu-id="32c6c-114">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-114">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="32c6c-115">Cliquez sur la case à cocher en regard du nom d'un appareil, puis, dans le volet **Appareil**, choisissez un profil dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-115">Click the check-box next to a device name and in the **Device** panel, choose a profile from the **Assigned profile** drop-down \> **Save**.</span></span>
    
    ![In the Device panel, select an Assigned profile to apply it.](media/ed0ce33f-9241-4403-a5de-2dddffdc6fb9.png)
  
## <a name="edit-delete-or-remove-a-profile"></a><span data-ttu-id="32c6c-117">Modifier, supprimer ou retirer un profil</span><span class="sxs-lookup"><span data-stu-id="32c6c-117">Edit, delete, or remove a profile</span></span>

<span data-ttu-id="32c6c-p102">Lorsque vous avez affecté un profil à un appareil, vous pouvez le mettre à jour, même si vous avez déjà donné l'appareil à un utilisateur. Lorsque l'appareil se connecte à Internet, il télécharge la dernière version de votre profil pendant le processus de configuration. Si l'utilisateur rétablit les paramètres d'usine par défaut de son appareil, l'appareil télécharge à nouveau les dernières mises à jour de votre profil.</span><span class="sxs-lookup"><span data-stu-id="32c6c-p102">Once you've assigned a profile to a device, you can update it, even if you've already given the device to a user. When the device connects to the internet, it downloads the latest version of your profile during the setup process. If the user restores their device to its factory default settings, the device will again download the latest updates to your profile.</span></span> 
  
### <a name="edit-a-profile"></a><span data-ttu-id="32c6c-121">Modifier un profil</span><span class="sxs-lookup"><span data-stu-id="32c6c-121">Edit a profile</span></span>

1. <span data-ttu-id="32c6c-122">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-122">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="32c6c-123">Cliquez sur la case à cocher en regard du nom d'un appareil puis, dans le volet **Profil**, modifiez les paramètres de votre choix \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-123">Click the check-box next to a device name and in the **Profile** panel update any of the available settings \> **Save**.</span></span>
    
    <span data-ttu-id="32c6c-124">Si vous effectuez cette opération avant qu'un utilisateur connecte l'appareil à Internet, le profil sera appliqué pendant le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="32c6c-124">If you do this before a user connects the device to the internet, then the profile gets applied to the setup process.</span></span>
    
### <a name="delete-a-profile"></a><span data-ttu-id="32c6c-125">Supprimer un profil</span><span class="sxs-lookup"><span data-stu-id="32c6c-125">Delete a profile</span></span>

1. <span data-ttu-id="32c6c-126">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-126">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="32c6c-127">Cliquez sur la case à cocher en regard du nom d'un appareil puis, dans le volet **Profil**, cliquez sur **Supprimer le profil** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-127">Click the check-box next to a device name and in the **Profile** panel click **Delete profile** \> **Save**.</span></span>
    
    <span data-ttu-id="32c6c-128">Lorsque vous supprimez un profil, il est supprimé de l'appareil ou du groupe d'appareils auquel il a été affecté.</span><span class="sxs-lookup"><span data-stu-id="32c6c-128">When you delete a profile, it gets removed from a device or a group of devices it was assigned to.</span></span>
    
### <a name="remove-a-profile"></a><span data-ttu-id="32c6c-129">Retirer un profil</span><span class="sxs-lookup"><span data-stu-id="32c6c-129">Remove a profile</span></span>

1. <span data-ttu-id="32c6c-130">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-130">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="32c6c-131">Cliquez sur la case à cocher en regard du nom d'un appareil, puis, dans le volet **Appareil**, choisissez **Aucun** dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32c6c-131">Click the check-box next to a device name and in the **Device** panel, choose a **None** from the **Assigned profile** drop-down \> **Save**.</span></span>
    
