---
title: Créer et modifier des appareils AutoPilot
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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0f7b1d7c-4086-4331-8534-45d7886f9f34
description: Découvrez comment télécharger des périphériques à l’aide de AutoPilot dans Microsoft 365 Business Premium. Vous pouvez affecter un profil à un appareil ou à un groupe d’appareils.
ms.openlocfilehash: 8c3d029d682ae30444bdc7d30a4790a8f982e0e0
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400991"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="6e9aa-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="6e9aa-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="6e9aa-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="6e9aa-105">Upload a list of devices</span></span>

<span data-ttu-id="6e9aa-106">Vous pouvez utiliser le [Guide pas à pas](add-autopilot-devices-and-profile.md) pour télécharger des périphériques, mais vous pouvez également télécharger des périphériques dans l’onglet **appareils** .</span><span class="sxs-lookup"><span data-stu-id="6e9aa-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload devices in the **Devices** tab.</span></span> 
  
<span data-ttu-id="6e9aa-107">Les appareils doivent respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e9aa-107">Devices must meet these requirements:</span></span>
  
- <span data-ttu-id="6e9aa-108">Windows 10, version 1703 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="6e9aa-108">Windows 10, version 1703 or later</span></span>
    
- <span data-ttu-id="6e9aa-109">Nouveaux appareils qui n’ont pas fait l’expérience de Windows out-of-Box</span><span class="sxs-lookup"><span data-stu-id="6e9aa-109">New devices that haven't been through Windows out-of-box experience</span></span>

1. <span data-ttu-id="6e9aa-110">Dans le centre d’administration 365 de Microsoft, sélectionnez **périphériques** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-110">In the Microsoft 365 admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="6e9aa-111">Sur la page **AutoPilot** , sélectionnez l’onglet **appareils** \> **Add Devices**.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-111">On the **AutoPilot** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](../media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="6e9aa-113">Dans le panneau **Ajouter des appareils** , accédez à un [fichier CSV de liste de périphériques](https://docs.microsoft.com/microsoft-365/admin/misc/device-list) que vous avez préparé à \> **Enregistrer** \> **Close**.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-113">On the **Add devices** panel, browse to a [Device list CSV file](https://docs.microsoft.com/microsoft-365/admin/misc/device-list) that you prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="6e9aa-114">Vous pouvez obtenir ces informations auprès de votre fournisseur de matériel ou vous pouvez utiliser le [script PowerShell Get-WindowsAutoPilotInfo](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) pour générer un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-114">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) to generate a CSV file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="6e9aa-115">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="6e9aa-115">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="6e9aa-116">Sur la page **préparer Windows** , sélectionnez l’onglet **appareils** et activez la case à cocher en regard d’un ou de plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-116">On the **Prepare Windows** page, choose the **Devices** tab, and select the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="6e9aa-117">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-117">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="6e9aa-118">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="6e9aa-118">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
    
