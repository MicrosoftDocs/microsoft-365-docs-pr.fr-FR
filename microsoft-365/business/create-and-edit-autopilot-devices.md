---
title: Créer et modifier des appareils AutoPilot
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
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
ms.openlocfilehash: 506ff44e3cb6656b19174e82688b5af141ea2b79
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578484"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="138d6-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="138d6-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="138d6-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="138d6-105">Upload a list of devices</span></span>

<span data-ttu-id="138d6-106">Vous pouvez utiliser le [guide pas à](add-autopilot-devices-and-profile.md) pas pour télécharger des appareils, mais vous pouvez également télécharger des appareils dans l’onglet **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="138d6-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload devices in the **Devices** tab.</span></span> 
  
<span data-ttu-id="138d6-107">Les appareils doivent répondre aux exigences ci-après :</span><span class="sxs-lookup"><span data-stu-id="138d6-107">Devices must meet these requirements:</span></span>
  
- <span data-ttu-id="138d6-108">Windows 10, version 1703 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="138d6-108">Windows 10, version 1703 or later</span></span>
    
- <span data-ttu-id="138d6-109">Nouveaux appareils qui n’ont pas fait l’expérience d’utilisation de Windows out-of-box</span><span class="sxs-lookup"><span data-stu-id="138d6-109">New devices that haven't been through Windows out-of-box experience</span></span>

1. <span data-ttu-id="138d6-110">Dans le Centre d’administration Microsoft 365, sélectionnez **Appareils** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="138d6-110">In the Microsoft 365 admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="138d6-111">Dans la page **AutoPilot,** sélectionnez **l’onglet Appareils** \> **Ajouter des appareils.**</span><span class="sxs-lookup"><span data-stu-id="138d6-111">On the **AutoPilot** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](../media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="138d6-113">Dans le **panneau Ajouter des appareils,** accédez à un fichier [CSV](../admin/misc/device-list.md) de liste d’appareils que vous avez préparé \> **Enregistrer** \> **fermer.**</span><span class="sxs-lookup"><span data-stu-id="138d6-113">On the **Add devices** panel, browse to a [Device list CSV file](../admin/misc/device-list.md) that you prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="138d6-114">Vous pouvez obtenir ces informations auprès de votre fournisseur de matériel ou utiliser le [script PowerShell Get-WindowsAutoPilotInfo](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) pour générer un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="138d6-114">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) to generate a CSV file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="138d6-115">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="138d6-115">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="138d6-116">Dans la page **Préparer Windows,** sélectionnez l’onglet **Appareils,** puis cochez la case en regard d’un ou plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="138d6-116">On the **Prepare Windows** page, choose the **Devices** tab, and select the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="138d6-117">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="138d6-117">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="138d6-118">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="138d6-118">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
