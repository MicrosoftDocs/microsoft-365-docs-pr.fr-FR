---
title: Créer et modifier des profils AutoPilot
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
- MOE150
ms.assetid: 5cf7139e-cfa1-4765-8aad-001af1c74faa
description: 'Apprenez à créer, modifier, supprimer ou supprimer des profils autoPilot. '
ms.openlocfilehash: 85fc897b2f428afae8d55feeb577021adaa30f72
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32277103"
---
# <a name="create-and-edit-autopilot-profiles"></a><span data-ttu-id="c21cd-103">Créer et modifier des profils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="c21cd-103">Create and edit AutoPilot profiles</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="c21cd-104">Créer un profil</span><span class="sxs-lookup"><span data-stu-id="c21cd-104">Create a profile</span></span>

<span data-ttu-id="c21cd-105">Un profil s'applique à un appareil ou à un groupe d'appareils,</span><span class="sxs-lookup"><span data-stu-id="c21cd-105">A profile applies to a device, or a group of devices,</span></span>
  
1. <span data-ttu-id="c21cd-106">dans le centre d'administration de Microsoft 365 Business, sélectionnez **périphériques** \> **autopilot**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-106">In the Microsoft 365 Business Admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="c21cd-107">Sur la \*\*\*\* page AutoPilot, sélectionnez l' \*\*\*\* onglet \> profils **Create Profile**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-107">On the **AutoPilot** page, choose the **Profiles** tab \> **Create profile**.</span></span>
    
3. <span data-ttu-id="c21cd-108">Sur la page **Créer un profil**, entrez un nom de profil qui vous permette de l'identifier, par exemple Marketing, activez le paramètre souhaité (voir [À propos des paramètres de profil AutoPilot](autopilot-profile-settings.md) pour plus d'informations), puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-108">On the **Create profile** page, enter a name for the profile that helps you identify it, for example Marketing, turn on the setting you want (see [About AutoPilot Profile settings](autopilot-profile-settings.md) for more information), and choose **Save**.</span></span>
    
    ![Enter name and turn on settings in the Create profile panel.](media/63b5a00d-6a5d-48d0-9557-e7531e80702a.png)
  
### <a name="apply-profile-to-a-device"></a><span data-ttu-id="c21cd-110">Appliquer le profil à un appareil</span><span class="sxs-lookup"><span data-stu-id="c21cd-110">Apply profile to a device</span></span>

<span data-ttu-id="c21cd-p101">Après avoir créé un profil, vous pouvez l'appliquer à un appareil ou à un groupe d'appareils. Vous pouvez sélectionner un profil existant dans la [guide détaillé](add-autopilot-devices-and-profile.md), l'appliquer aux nouveaux appareils ou remplacer un profil existant pour un appareil ou un groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="c21cd-p101">After you create a profile you can apply it to a device or a group of devices. You can pick an existing profile in the [step-by-step guide](add-autopilot-devices-and-profile.md), you can apply it to new devices, or you can replace an existing profile for a device or group of devices.</span></span> 
  
1. <span data-ttu-id="c21cd-113">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-113">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="c21cd-114">Cliquez sur la case à cocher en regard du nom d'un appareil, puis, dans le volet **Appareil**, choisissez un profil dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-114">Click the check-box next to a device name and in the **Device** panel, choose a profile from the **Assigned profile** drop-down \> **Save**.</span></span>
    
    ![In the Device panel, select an Assigned profile to apply it.](media/ed0ce33f-9241-4403-a5de-2dddffdc6fb9.png)
  
## <a name="edit-delete-or-remove-a-profile"></a><span data-ttu-id="c21cd-116">Modifier, supprimer ou retirer un profil</span><span class="sxs-lookup"><span data-stu-id="c21cd-116">Edit, delete, or remove a profile</span></span>

<span data-ttu-id="c21cd-p102">Lorsque vous avez affecté un profil à un appareil, vous pouvez le mettre à jour, même si vous avez déjà donné l'appareil à un utilisateur. Lorsque l'appareil se connecte à Internet, il télécharge la dernière version de votre profil pendant le processus de configuration. Si l'utilisateur rétablit les paramètres d'usine par défaut de son appareil, l'appareil télécharge à nouveau les dernières mises à jour de votre profil.</span><span class="sxs-lookup"><span data-stu-id="c21cd-p102">Once you've assigned a profile to a device, you can update it, even if you've already given the device to a user. When the device connects to the internet, it downloads the latest version of your profile during the setup process. If the user restores their device to its factory default settings, the device will again download the latest updates to your profile.</span></span> 
  
### <a name="edit-a-profile"></a><span data-ttu-id="c21cd-120">Modifier un profil</span><span class="sxs-lookup"><span data-stu-id="c21cd-120">Edit a profile</span></span>

1. <span data-ttu-id="c21cd-121">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-121">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="c21cd-122">Cliquez sur la case à cocher en regard du nom d'un appareil puis, dans le volet **Profil**, modifiez les paramètres de votre choix \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-122">Click the check-box next to a device name and in the **Profile** panel update any of the available settings \> **Save**.</span></span>
    
    <span data-ttu-id="c21cd-123">Si vous effectuez cette opération avant qu'un utilisateur connecte l'appareil à Internet, le profil sera appliqué pendant le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="c21cd-123">If you do this before a user connects the device to the internet, then the profile gets applied to the setup process.</span></span>
    
### <a name="delete-a-profile"></a><span data-ttu-id="c21cd-124">Supprimer un profil</span><span class="sxs-lookup"><span data-stu-id="c21cd-124">Delete a profile</span></span>

1. <span data-ttu-id="c21cd-125">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-125">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="c21cd-126">Cliquez sur la case à cocher en regard du nom d'un appareil puis, dans le volet **Profil**, cliquez sur **Supprimer le profil** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-126">Click the check-box next to a device name and in the **Profile** panel click **Delete profile** \> **Save**.</span></span>
    
    <span data-ttu-id="c21cd-127">Lorsque vous supprimez un profil, il est supprimé de l'appareil ou du groupe d'appareils auquel il a été affecté.</span><span class="sxs-lookup"><span data-stu-id="c21cd-127">When you delete a profile, it gets removed from a device or a group of devices it was assigned to.</span></span>
    
### <a name="remove-a-profile"></a><span data-ttu-id="c21cd-128">Retirer un profil</span><span class="sxs-lookup"><span data-stu-id="c21cd-128">Remove a profile</span></span>

1. <span data-ttu-id="c21cd-129">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-129">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="c21cd-130">Cliquez sur la case à cocher en regard du nom d'un appareil, puis, dans le volet **Appareil**, choisissez **Aucun** dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c21cd-130">Click the check-box next to a device name and in the **Device** panel, choose a **None** from the **Assigned profile** drop-down \> **Save**.</span></span>
    
