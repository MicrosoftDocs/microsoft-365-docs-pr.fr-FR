---
title: Résoudre les erreurs des appareils AutoPilot
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: troubleshooting
f1_keywords:
- ZTDTroubleshootDeviceErrors
- O365E_ZTDTroubleshootDeviceErrors
- BCS365_ZTDTroubleshootDeviceErrors
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1f468690-530c-47ea-918f-fede24607c53
description: Découvrez comment résoudre les erreurs de fichier de périphérique en pilote automatique.
ms.openlocfilehash: 9b8d8ab424dd3189ff5c228dab8f5c513ff5dafc
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867019"
---
# <a name="troubleshoot-autopilot-device-errors"></a><span data-ttu-id="0b27e-103">Résoudre les erreurs des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="0b27e-103">Troubleshoot AutoPilot device errors</span></span>

## <a name="device-file-error-messages"></a><span data-ttu-id="0b27e-104">Messages d’erreur de fichier de périphérique</span><span class="sxs-lookup"><span data-stu-id="0b27e-104">Device file error messages</span></span>

<span data-ttu-id="0b27e-105">Info Voici certaines des erreurs que vous pouvez rencontrer lorsque vous travaillez avec des fichiers de périphérique en pilote automatique dans Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="0b27e-105">Here's info on some of the errors you might see while working with AutoPilot device files in Microsoft 365 Business.</span></span> 
  
|<span data-ttu-id="0b27e-106">**Code d’erreur**</span><span class="sxs-lookup"><span data-stu-id="0b27e-106">**Error code**</span></span>|<span data-ttu-id="0b27e-107">**Solution pour l’essayer**</span><span class="sxs-lookup"><span data-stu-id="0b27e-107">**Fix to try**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b27e-108">Corps de la demande non valide</span><span class="sxs-lookup"><span data-stu-id="0b27e-108">Invalid request body</span></span>  <br/> |<span data-ttu-id="0b27e-109">Cette erreur doit se produire rarement, si vous voyez cette erreur, réessayez l’opération.</span><span class="sxs-lookup"><span data-stu-id="0b27e-109">This error should happen rarely, if you see this error, try the operation again.</span></span>  <br/> |
|<span data-ttu-id="0b27e-110">Valeur de hachage du matériel pour un périphérique n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="0b27e-110">Hardware hash value for a device isn't correct.</span></span>  <br/> |<span data-ttu-id="0b27e-p101">Si vous voyez cette erreur, cela signifie que la valeur fournie dans votre fichier CSV pour le hachage du matériel d’un périphérique n’est pas correcte. Tout d’abord, vérifiez que la valeur a été correctement tapée. Si vous pensez que la valeur est correcte, mais cette erreur qui se passe, demandez à votre fournisseur de matériel pour une assistance.</span><span class="sxs-lookup"><span data-stu-id="0b27e-p101">If you see this error, it means that the value you provided in your CSV file for the hardware hash of one device isn't correct. First, verify that the value was typed correctly. If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="0b27e-114">Périphérique affecté à un autre client</span><span class="sxs-lookup"><span data-stu-id="0b27e-114">Device assigned to another tenant</span></span>  <br/> |<span data-ttu-id="0b27e-p102">Si vous voyez cette erreur, cela signifie que la valeur fournie pour le numéro de série ou la clé de produit d’un ou plusieurs périphériques dans votre fichier CSV n’est pas correcte. Tout d’abord, vérifiez que la valeur a été correctement tapée. Si vous pensez que la valeur est correcte, mais cette erreur qui se passe, demandez à votre fournisseur de matériel pour une assistance.</span><span class="sxs-lookup"><span data-stu-id="0b27e-p102">If you see this error, it means that the value you provided in your CSV file for either the serial number or the product key of one or more devices isn't correct. First, verify that the value was typed correctly. If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="0b27e-118">Le fichier CSV contient un numéro de série ou de la clé de produit</span><span class="sxs-lookup"><span data-stu-id="0b27e-118">The CSV file contains an invalid serial number or product key</span></span>  <br/> |<span data-ttu-id="0b27e-p103">Si vous rencontrez cette erreur, cela signifie que le périphérique que vous êtes lors de la tentative d’enregistrer est déjà enregistré par une autre organisation. Pour résoudre ce problème, demandez à votre fournisseur de matériel pour une assistance.</span><span class="sxs-lookup"><span data-stu-id="0b27e-p103">If you see this error it means that the device you are tyring to register is already registered by an other organization. To fix this, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="0b27e-121">Ce périphérique n’est pas pris en charge pour le programme d’installation à l’aide de pilote</span><span class="sxs-lookup"><span data-stu-id="0b27e-121">This device is not supported for setup by using AutoPilot</span></span>  <br/> | <span data-ttu-id="0b27e-p104">Cette erreur signifie que le périphérique ne répond pas aux besoins de déploiement pilote automatique. Périphériques doivent répondre aux exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b27e-p104">This error means the device does not meet AutoPilot deployment requirements. Devices need to meet these requirements:</span></span>  <br/>  <span data-ttu-id="0b27e-124">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="0b27e-124">Windows 10, version 1703 or later.</span></span>  <br/>  <span data-ttu-id="0b27e-125">Nouveaux appareils qui ne sont pas issus d'une expérience Windows prête à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="0b27e-125">New devices that have not been through Windows out-of-box experience.</span></span>  <br/> |
|<span data-ttu-id="0b27e-126">Périphérique non trouvé</span><span class="sxs-lookup"><span data-stu-id="0b27e-126">Device not found</span></span>  <br/> |<span data-ttu-id="0b27e-p105">Cette erreur signifie qu’un ou plusieurs périphériques dans votre fichier CSV n’est pas inscrit à votre organisation. Pour résoudre ce problème, demandez à votre fournisseur de matériel pour une assistance.</span><span class="sxs-lookup"><span data-stu-id="0b27e-p105">This error means that one or more devices in your CSV file is not registered to your organization. To fix this, ask your hardware vendor for help.</span></span>  <br/> |
   
