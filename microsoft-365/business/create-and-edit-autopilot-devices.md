---
title: Créer et modifier des appareils AutoPilot
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
ms.assetid: 0f7b1d7c-4086-4331-8534-45d7886f9f34
description: Découvrez comment télécharger des périphériques à l’aide de AutoPilot dans Microsoft 365 Business. Vous pouvez affecter un profil à un appareil ou à un groupe d’appareils.
ms.openlocfilehash: 6492f1469a1ac9ea67750e9ffa071d19c88c743f
ms.sourcegitcommit: db1dfb2df2c2f7beced3b57bc772d106c189e88a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33660391"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="4820a-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="4820a-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="4820a-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="4820a-105">Upload a list of devices</span></span>

<span data-ttu-id="4820a-106">Pour charger des appareils, vous pouvez utiliser le [guide détaillé](add-autopilot-devices-and-profile.md), mais vous pouvez également le faire à partir de l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="4820a-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload the in the **Devices** tab.</span></span> 
  
<span data-ttu-id="4820a-107">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="4820a-107">Devices need to meet these requirements:</span></span>
  
- <span data-ttu-id="4820a-108">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="4820a-108">Windows 10, version 1703 or later.</span></span>
    
- <span data-ttu-id="4820a-109">Nouveaux appareils qui ne sont pas issus d'une expérience Windows prête à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="4820a-109">New devices that have not been through Windows out-of-box experience.</span></span>

1. <span data-ttu-id="4820a-110">Dans le centre d’administration de Microsoft 365 Business, sélectionnez **périphériques** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="4820a-110">In the Microsoft 365 Business Admin center, choose **Devices** \> **AutoPilot**.</span></span>
  
2. <span data-ttu-id="4820a-111">Sur la \*\*\*\* page AutoPilot, sélectionnez l' \*\*\*\* onglet \> appareils **Add**Devices.</span><span class="sxs-lookup"><span data-stu-id="4820a-111">On the **AutoPilot** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="4820a-113">Dans le panneau **Ajouter des appareils** , accédez à un [fichier CSV de liste de périphériques](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) que vous \> avez préparé **Enregistrer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="4820a-113">On the **Add devices** panel, browse to a [Device list CSV-file](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) that you have prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="4820a-114">Vous pouvez obtenir ces informations à partir de votre fournisseur de matériel ou vous pouvez utiliser le [script Get-WindowsAutoPilotInfo PowerShell](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) qui génèrera un fichier csv.</span><span class="sxs-lookup"><span data-stu-id="4820a-114">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) that will generate a csv file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="4820a-115">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="4820a-115">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="4820a-116">Sur la page **Préparer Windows**, sélectionnez l'onglet **Appareils** et cochez la case correspondant à un ou plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="4820a-116">On the **Prepare Windows** page, choose the **Devices** tab and check the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="4820a-117">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="4820a-117">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="4820a-118">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="4820a-118">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
    
