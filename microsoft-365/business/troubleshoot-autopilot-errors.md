---
title: Résoudre les erreurs des appareils AutoPilot
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: troubleshooting
f1_keywords:
- ZTDTroubleshootDeviceErrors
- O365E_ZTDTroubleshootDeviceErrors
- BCS365_ZTDTroubleshootDeviceErrors
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- MARVEL_SEO_MAR
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1f468690-530c-47ea-918f-fede24607c53
description: Découvrez comment résoudre les erreurs que vous pouvez voir lors de l’utilisation de fichiers d’appareil AutoPilot dans Microsoft 365 Business.
ms.openlocfilehash: 7569f18097a1f5959b3dd491958c78886e1e05d6
ms.sourcegitcommit: 41c0bc5cf50f4ca63b4286d1ea0f58ab82984b7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "42547468"
---
# <a name="troubleshoot-autopilot-device-errors"></a><span data-ttu-id="9b9f5-103">Résoudre les erreurs des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="9b9f5-103">Troubleshoot AutoPilot device errors</span></span>

## <a name="device-file-error-messages"></a><span data-ttu-id="9b9f5-104">Messages d’erreur de fichier d’appareil</span><span class="sxs-lookup"><span data-stu-id="9b9f5-104">Device file error messages</span></span>

<span data-ttu-id="9b9f5-105">Voici des informations sur certaines des erreurs que vous pouvez voir lors de l’utilisation de fichiers d’appareil AutoPilot dans Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-105">Here's info on some of the errors you might see while working with AutoPilot device files in Microsoft 365 Business.</span></span> 
  
|<span data-ttu-id="9b9f5-106">**Code d’erreur**</span><span class="sxs-lookup"><span data-stu-id="9b9f5-106">**Error code**</span></span>|<span data-ttu-id="9b9f5-107">**Correctif à essayer**</span><span class="sxs-lookup"><span data-stu-id="9b9f5-107">**Fix to try**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b9f5-108">Corps de la requête non valide</span><span class="sxs-lookup"><span data-stu-id="9b9f5-108">Invalid request body</span></span>  <br/> |<span data-ttu-id="9b9f5-109">Cette erreur devrait se produire rarement, si vous voyez cette erreur, renouvelez l’opération.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-109">This error should happen rarely, if you see this error, try the operation again.</span></span>  <br/> |
|<span data-ttu-id="9b9f5-110">La valeur de hachage de matériel pour un périphérique est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-110">Hardware hash value for a device isn't correct.</span></span>  <br/> |<span data-ttu-id="9b9f5-111">Si cette erreur apparaît, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le hachage matériel d’un périphérique est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-111">If you see this error, it means that the value you provided in your CSV file for the hardware hash of one device isn't correct.</span></span> <span data-ttu-id="9b9f5-112">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-112">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="9b9f5-113">Si vous pensez que la valeur est correcte, mais que cette erreur persiste, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-113">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="9b9f5-114">Appareil affecté à un autre client</span><span class="sxs-lookup"><span data-stu-id="9b9f5-114">Device assigned to another tenant</span></span>  <br/> |<span data-ttu-id="9b9f5-115">Si cette erreur apparaît, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le numéro de série ou la clé de produit d’un ou plusieurs périphériques est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-115">If you see this error, it means that the value you provided in your CSV file for either the serial number or the product key of one or more devices isn't correct.</span></span> <span data-ttu-id="9b9f5-116">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-116">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="9b9f5-117">Si vous pensez que la valeur est correcte, mais que cette erreur persiste, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-117">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="9b9f5-118">Le fichier CSV contient un numéro de série ou une clé de produit non valide</span><span class="sxs-lookup"><span data-stu-id="9b9f5-118">The CSV file contains an invalid serial number or product key</span></span>  <br/> |<span data-ttu-id="9b9f5-119">Si cette erreur apparaît, cela signifie que l’appareil que vous essayez d’enregistrer est déjà enregistré par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-119">If you see this error, it means that the device you are trying to register is already registered by another organization.</span></span> <span data-ttu-id="9b9f5-120">Pour corriger cette erreur, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-120">To fix this error, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="9b9f5-121">Ce périphérique n’est pas pris en charge pour l’installation à l’aide de AutoPilot</span><span class="sxs-lookup"><span data-stu-id="9b9f5-121">This device is not supported for setup by using AutoPilot</span></span>  <br/> | <span data-ttu-id="9b9f5-122">Cette erreur signifie que l’appareil ne répond pas à la configuration requise pour le déploiement de AutoPilot.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-122">This error means the device doesn't meet AutoPilot deployment requirements.</span></span> <span data-ttu-id="9b9f5-123">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="9b9f5-123">Devices need to meet these requirements:</span></span>  <br/>  <span data-ttu-id="9b9f5-124">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-124">Windows 10, version 1703 or later.</span></span>  <br/>  <span data-ttu-id="9b9f5-125">Nouveaux appareils qui n’ont pas été via Windows out-of-Box.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-125">New devices that haven't been through Windows out-of-box experience.</span></span>  <br/> |
|<span data-ttu-id="9b9f5-126">Appareil introuvable</span><span class="sxs-lookup"><span data-stu-id="9b9f5-126">Device not found</span></span>  <br/> |<span data-ttu-id="9b9f5-127">Cette erreur signifie qu’un ou plusieurs périphériques de votre fichier CSV ne sont pas enregistrés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-127">This error means that one or more devices in your CSV file isn't registered to your organization.</span></span> <span data-ttu-id="9b9f5-128">Pour résoudre ce problème, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="9b9f5-128">To fix this, ask your hardware vendor for help.</span></span>  <br/> |
