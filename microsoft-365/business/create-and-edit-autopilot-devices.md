---
title: Créer et modifier des appareils AutoPilot
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
ms.assetid: 0f7b1d7c-4086-4331-8534-45d7886f9f34
description: Découvrez comment télécharger des périphériques à l’aide de pilote automatique dans Microsoft 365 Business. Vous pouvez affecter un profil à un périphérique ou un groupe de périphériques.
ms.openlocfilehash: cc1f81e9efd9b16e27b8abfbb0927d241535077e
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867088"
---
# <a name="create-and-edit-autopilot-devices"></a><span data-ttu-id="78774-104">Créer et modifier des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="78774-104">Create and edit AutoPilot devices</span></span>

## <a name="upload-a-list-of-devices"></a><span data-ttu-id="78774-105">Charger une liste d'appareils</span><span class="sxs-lookup"><span data-stu-id="78774-105">Upload a list of devices</span></span>

<span data-ttu-id="78774-106">Pour charger des appareils, vous pouvez utiliser le [guide détaillé](add-autopilot-devices-and-profile.md), mais vous pouvez également le faire à partir de l'onglet **Appareils**.</span><span class="sxs-lookup"><span data-stu-id="78774-106">You can use the [Step-by-step guide](add-autopilot-devices-and-profile.md) to upload devices, but you can also upload the in the **Devices** tab.</span></span> 
  
<span data-ttu-id="78774-107">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="78774-107">Devices need to meet these requirements:</span></span>
  
- <span data-ttu-id="78774-108">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="78774-108">Windows 10, version 1703 or later.</span></span>
    
- <span data-ttu-id="78774-109">Nouveaux appareils qui ne sont pas issus d'une expérience Windows prête à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="78774-109">New devices that have not been through Windows out-of-box experience.</span></span>
    
1. <span data-ttu-id="78774-110">Dans le Centre d'administration Microsoft 365 Entreprise, choisissez **Déployer Windows avec AutoPilot** sur la carte **Actions de l'appareil**.</span><span class="sxs-lookup"><span data-stu-id="78774-110">In the Microsoft 365 Business Admin center, choose **Deploy Windows with AutoPilot** on the **Device actions** card.</span></span> 
    
    ![On the Device actions card, choose Deploy Windows with Autopilot.](media/160d5c2a-11a8-48f9-a8aa-70f084b85448.png)
  
2. <span data-ttu-id="78774-112">Dans la page **Préparation de Windows** , choisissez l’onglet **périphériques** \> **périphériques ajouter**.</span><span class="sxs-lookup"><span data-stu-id="78774-112">On the **Prepare Windows** page, choose the **Devices** tab \> **Add devices**.</span></span>
    
    ![In the Devices tab, choose Add devices.](media/6ba81e22-c873-40ad-8a72-ce64d15ea6ba.png)
  
3. <span data-ttu-id="78774-114">Dans le volet **Ajouter périphériques** , accédez à une [liste de périphériques fichier CSV](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) que vous avez préparé \> **Enregistrer** \> **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="78774-114">On the **Add devices** panel, browse to a [Device list CSV-file](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e) that you have prepared \> **Save** \> **Close**.</span></span>
    
    <span data-ttu-id="78774-115">Vous pouvez obtenir ces informations à partir de votre fournisseur de matériel ou vous pouvez utiliser le [script Get-WindowsAutoPilotInfo PowerShell](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) qui génèrera un fichier csv.</span><span class="sxs-lookup"><span data-stu-id="78774-115">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) that will generate a csv file.</span></span> 
    
## <a name="assign-a-profile-to-a-device-or-a-group-of-devices"></a><span data-ttu-id="78774-116">Attribuer un profil à un appareil ou à un groupe d'appareils</span><span class="sxs-lookup"><span data-stu-id="78774-116">Assign a profile to a device or a group of devices</span></span>

1. <span data-ttu-id="78774-117">Sur la page **Préparer Windows**, sélectionnez l'onglet **Appareils** et cochez la case correspondant à un ou plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="78774-117">On the **Prepare Windows** page, choose the **Devices** tab and check the check box next to one or more devices.</span></span> 
    
2. <span data-ttu-id="78774-118">Dans le volet **Appareil**, sélectionnez un profil dans la liste déroulante **Profil attribué**.</span><span class="sxs-lookup"><span data-stu-id="78774-118">On the **Device** panel, select a profile from the **Assigned profile** drop-down.</span></span> 
    
    <span data-ttu-id="78774-119">Si vous n'avez pas encore de profil, consultez [Créer et modifier des profils AutoPilot](create-and-edit-autopilot-profiles.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="78774-119">If you don't have any profiles yet, see [Create and edit AutoPilot profiles](create-and-edit-autopilot-profiles.md) for instructions.</span></span> 
    
