---
title: Créer et modifier des profils AutoPilot
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
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5cf7139e-cfa1-4765-8aad-001af1c74faa
description: Apprenez à créer un profil AutoPilot et à l’appliquer à un appareil, ainsi qu’à modifier ou supprimer un profil ou à supprimer un profil d’un appareil.
ms.openlocfilehash: e58418813ed0b4d23a5fa7e1d23aae33d8850e7f
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400971"
---
# <a name="create-and-edit-autopilot-profiles"></a><span data-ttu-id="2ef5d-103">Créer et modifier des profils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="2ef5d-103">Create and edit AutoPilot profiles</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="2ef5d-104">Créer un profil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-104">Create a profile</span></span>

<span data-ttu-id="2ef5d-105">Un profil s'applique à un appareil ou à un groupe d'appareils,</span><span class="sxs-lookup"><span data-stu-id="2ef5d-105">A profile applies to a device, or a group of devices,</span></span>
  
1. <span data-ttu-id="2ef5d-106">Dans le centre d’administration 365 de Microsoft, sélectionnez **périphériques** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-106">In the Microsoft 365 admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="2ef5d-107">Sur la page **AutoPilot** , sélectionnez l’onglet **profils** \> **Create Profile**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-107">On the **AutoPilot** page, choose the **Profiles** tab \> **Create profile**.</span></span>
    
3. <span data-ttu-id="2ef5d-108">Sur la page **créer un profil** , entrez un nom pour le profil qui vous permet de l’identifier, par exemple marketing.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-108">On the **Create profile** page, enter a name for the profile that helps you identify it, for example Marketing.</span></span> <span data-ttu-id="2ef5d-109">Activez le paramètre souhaité, puis choisissez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-109">Turn on the setting you want, and then choose **Save**.</span></span> <span data-ttu-id="2ef5d-110">Pour plus d’informations sur les paramètres du profil AutoPilot, voir [à propos des paramètres du profil AutoPilot](autopilot-profile-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2ef5d-110">For more information about AutoPilot profile settings, see [About AutoPilot Profile settings](autopilot-profile-settings.md).</span></span>
    
    ![Enter name and turn on settings in the Create profile panel.](../media/63b5a00d-6a5d-48d0-9557-e7531e80702a.png)
  
### <a name="apply-profile-to-a-device"></a><span data-ttu-id="2ef5d-112">Appliquer le profil à un appareil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-112">Apply profile to a device</span></span>

<span data-ttu-id="2ef5d-113">Une fois que vous avez créé un profil, vous pouvez l’appliquer à un appareil ou à un groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-113">After you create a profile, you can apply it to a device or a group of devices.</span></span> <span data-ttu-id="2ef5d-114">Vous pouvez choisir un profil existant dans le [Guide pas à pas](add-autopilot-devices-and-profile.md) et l’appliquer à de nouveaux appareils ou remplacer un profil existant pour un appareil ou un groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-114">You can pick an existing profile in the [step-by-step guide](add-autopilot-devices-and-profile.md) and apply it to new devices, or replace an existing profile for a device or group of devices.</span></span> 
  
1. <span data-ttu-id="2ef5d-115">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-115">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="2ef5d-116">Activez la case à cocher en regard du nom d’un appareil, puis dans le panneau **périphérique** , sélectionnez un profil dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-116">Select the check box next to a device name, and in the **Device** panel, choose a profile from the **Assigned profile** drop-down list \> **Save**.</span></span>
    
    ![In the Device panel, select an Assigned profile to apply it.](../media/ed0ce33f-9241-4403-a5de-2dddffdc6fb9.png)
  
## <a name="edit-delete-or-remove-a-profile"></a><span data-ttu-id="2ef5d-118">Modifier, supprimer ou retirer un profil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-118">Edit, delete, or remove a profile</span></span>

<span data-ttu-id="2ef5d-p103">Lorsque vous avez affecté un profil à un appareil, vous pouvez le mettre à jour, même si vous avez déjà donné l'appareil à un utilisateur. Lorsque l'appareil se connecte à Internet, il télécharge la dernière version de votre profil pendant le processus de configuration. Si l'utilisateur rétablit les paramètres d'usine par défaut de son appareil, l'appareil télécharge à nouveau les dernières mises à jour de votre profil.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-p103">Once you've assigned a profile to a device, you can update it, even if you've already given the device to a user. When the device connects to the internet, it downloads the latest version of your profile during the setup process. If the user restores their device to its factory default settings, the device will again download the latest updates to your profile.</span></span> 
  
### <a name="edit-a-profile"></a><span data-ttu-id="2ef5d-122">Modifier un profil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-122">Edit a profile</span></span>

1. <span data-ttu-id="2ef5d-123">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-123">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="2ef5d-124">Activez la case à cocher en regard du nom d’un appareil, puis, dans le volet **Profil** , mettez à jour les paramètres d' \> **enregistrement**disponibles.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-124">Select the check box next to a device name, and in the **Profile** panel, update any of the available settings \> **Save**.</span></span>
    
    <span data-ttu-id="2ef5d-125">Si vous effectuez cette opération avant qu'un utilisateur connecte l'appareil à Internet, le profil sera appliqué pendant le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-125">If you do this before a user connects the device to the internet, then the profile gets applied to the setup process.</span></span>
    
### <a name="delete-a-profile"></a><span data-ttu-id="2ef5d-126">Supprimer un profil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-126">Delete a profile</span></span>

1. <span data-ttu-id="2ef5d-127">Sur la page **Préparer Windows**, choisissez l'onglet **Profils**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-127">On the **Prepare Windows** page, choose the **Profiles** tab.</span></span> 
    
2. <span data-ttu-id="2ef5d-128">Activez la case à cocher en regard du nom d’un appareil, puis, dans le volet **Profil** , sélectionnez Supprimer l’enregistrement du **Profil** \> **Save**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-128">Select the check box next to a device name, and in the **Profile** panel, select **Delete profile** \> **Save**.</span></span>
    
    <span data-ttu-id="2ef5d-129">Lorsque vous supprimez un profil, il est supprimé de l'appareil ou du groupe d'appareils auquel il a été affecté.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-129">When you delete a profile, it gets removed from a device or a group of devices it was assigned to.</span></span>
    
### <a name="remove-a-profile"></a><span data-ttu-id="2ef5d-130">Retirer un profil</span><span class="sxs-lookup"><span data-stu-id="2ef5d-130">Remove a profile</span></span>

1. <span data-ttu-id="2ef5d-131">Sur la page **Préparer Windows**, choisissez l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-131">On the **Prepare Windows** page, choose the **Devices** tab.</span></span> 
    
2. <span data-ttu-id="2ef5d-132">Activez la case à cocher en regard du nom d’un appareil, puis, dans le panneau **périphérique** , choisissez **aucun** dans la liste déroulante **Profil affecté** \> **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2ef5d-132">Select the check box next to a device name, and in the **Device** panel, choose **None** from the **Assigned profile** drop-down list \> **Save**.</span></span>
    
