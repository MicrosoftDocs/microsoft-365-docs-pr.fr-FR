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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0f7b1d7c-4086-4331-8534-45d7886f9f34
description: Découvrez comment télécharger des périphériques à l’aide de AutoPilot dans Microsoft 365 Business. Vous pouvez affecter un profil à un appareil ou à un groupe d’appareils.
ms.openlocfilehash: 5a99f691b0325f511f34e3a6c3a20f08ee8d909f
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41594008"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="4fb43-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="4fb43-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="4fb43-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="4fb43-105">Upload a list of devices</span></span>

<span data-ttu-id="4fb43-106">Vous pouvez utiliser le [Guide pas à pas](add-autopilot-devices-and-profile.md) pour télécharger des périphériques, mais vous pouvez également télécharger des périphériques dans l’onglet **appareils** .</span><span class="sxs-lookup"><span data-stu-id="4fb43-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload devices in the **Devices** tab.</span></span> 
  
<span data-ttu-id="4fb43-107">Les appareils doivent respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fb43-107">Devices must meet these requirements:</span></span>
  
- <span data-ttu-id="4fb43-108">Windows 10, version 1703 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4fb43-108">Windows 10, version 1703 or later</span></span>
    
- <span data-ttu-id="4fb43-109">Nouveaux appareils qui n’ont pas fait l’expérience de Windows out-of-Box</span><span class="sxs-lookup"><span data-stu-id="4fb43-109">New devices that haven't been through Windows out-of-box experience</span></span>

1. <span data-ttu-id="4fb43-110">Dans le centre d’administration de Microsoft 365 Business, sélectionnez **périphériques** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="4fb43-110">In the Microsoft 365 Business Admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="4fb43-111">Sur la **page AutoPilot** , sélectionnez l' \*\*\*\* onglet \> appareils **Add Devices**.</span><span class="sxs-lookup"><span data-stu-id="4fb43-111">On the **AutoPilot** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="4fb43-113">Dans le **panneau ajouter des appareils** , accédez à un [fichier CSV de liste](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) de périphériques \> que vous avez préparé à **Enregistrer** \> **.**</span><span class="sxs-lookup"><span data-stu-id="4fb43-113">On the **Add devices** panel, browse to a [Device list CSV file](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) that you prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="4fb43-114">Vous pouvez obtenir ces informations auprès de votre fournisseur de matériel ou vous pouvez utiliser le [script PowerShell Get-WindowsAutoPilotInfo](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) pour générer un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="4fb43-114">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) to generate a CSV file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="4fb43-115">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="4fb43-115">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="4fb43-116">Sur la page **préparer Windows** , sélectionnez l’onglet **appareils** et activez la case à cocher en regard d’un ou de plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="4fb43-116">On the **Prepare Windows** page, choose the **Devices** tab, and select the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="4fb43-117">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="4fb43-117">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="4fb43-118">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="4fb43-118">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
    
