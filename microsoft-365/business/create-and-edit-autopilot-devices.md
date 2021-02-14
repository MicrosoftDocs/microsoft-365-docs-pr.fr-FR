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
description: Découvrez comment télécharger des appareils à l’aide d’AutoPilot dans Microsoft 365 Business Premium. Vous pouvez affecter un profil à un appareil ou à un groupe d’appareils.
ms.openlocfilehash: 8c3d029d682ae30444bdc7d30a4790a8f982e0e0
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400991"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="8f181-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="8f181-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="8f181-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="8f181-105">Upload a list of devices</span></span>

<span data-ttu-id="8f181-106">Vous pouvez utiliser le [guide pas à](add-autopilot-devices-and-profile.md) pas pour télécharger des appareils, mais vous pouvez également télécharger des appareils dans l’onglet **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="8f181-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload devices in the **Devices** tab.</span></span> 
  
<span data-ttu-id="8f181-107">Les appareils doivent répondre aux exigences ci-après :</span><span class="sxs-lookup"><span data-stu-id="8f181-107">Devices must meet these requirements:</span></span>
  
- <span data-ttu-id="8f181-108">Windows 10, version 1703 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8f181-108">Windows 10, version 1703 or later</span></span>
    
- <span data-ttu-id="8f181-109">Nouveaux appareils qui n’ont pas fait l’expérience d’utilisation de Windows out-of-box</span><span class="sxs-lookup"><span data-stu-id="8f181-109">New devices that haven't been through Windows out-of-box experience</span></span>

1. <span data-ttu-id="8f181-110">Dans le Centre d’administration Microsoft 365, sélectionnez **Appareils** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="8f181-110">In the Microsoft 365 admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="8f181-111">Dans la page **AutoPilot,** sélectionnez **l’onglet Appareils** \> **Ajouter des appareils.**</span><span class="sxs-lookup"><span data-stu-id="8f181-111">On the **AutoPilot** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](../media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="8f181-113">Dans le **panneau Ajouter des appareils,** accédez à un fichier [CSV](https://docs.microsoft.com/microsoft-365/admin/misc/device-list) de liste d’appareils que vous avez préparé \> **Enregistrer** \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="8f181-113">On the **Add devices** panel, browse to a [Device list CSV file](https://docs.microsoft.com/microsoft-365/admin/misc/device-list) that you prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="8f181-114">Vous pouvez obtenir ces informations auprès de votre fournisseur de matériel ou utiliser le [script PowerShell Get-WindowsAutoPilotInfo](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) pour générer un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="8f181-114">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) to generate a CSV file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="8f181-115">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="8f181-115">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="8f181-116">Dans la page **Préparer Windows,** sélectionnez l’onglet **Appareils,** puis cochez la case en regard d’un ou plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="8f181-116">On the **Prepare Windows** page, choose the **Devices** tab, and select the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="8f181-117">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="8f181-117">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="8f181-118">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="8f181-118">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
    
