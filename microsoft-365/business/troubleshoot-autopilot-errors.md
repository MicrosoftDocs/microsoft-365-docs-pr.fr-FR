---
title: Résoudre les erreurs des appareils AutoPilot
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1f468690-530c-47ea-918f-fede24607c53
description: Découvrez comment dépanner les erreurs de fichier d’appareil AutoPilot.
ms.openlocfilehash: 88b59ec20ddda401c1dac45ff729ac38497a767e
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34074357"
---
# <a name="troubleshoot-autopilot-device-errors"></a><span data-ttu-id="bb69a-103">Résoudre les erreurs des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="bb69a-103">Troubleshoot AutoPilot device errors</span></span>

## <a name="device-file-error-messages"></a><span data-ttu-id="bb69a-104">Messages d’erreur de fichier d’appareil</span><span class="sxs-lookup"><span data-stu-id="bb69a-104">Device file error messages</span></span>

<span data-ttu-id="bb69a-105">Voici des informations sur certaines des erreurs que vous pouvez voir lors de l’utilisation de fichiers d’appareil AutoPilot dans Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="bb69a-105">Here's info on some of the errors you might see while working with AutoPilot device files in Microsoft 365 Business.</span></span> 
  
|<span data-ttu-id="bb69a-106">**Code d’erreur**</span><span class="sxs-lookup"><span data-stu-id="bb69a-106">**Error code**</span></span>|<span data-ttu-id="bb69a-107">**Correctif à essayer**</span><span class="sxs-lookup"><span data-stu-id="bb69a-107">**Fix to try**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb69a-108">Corps de la requête non valide</span><span class="sxs-lookup"><span data-stu-id="bb69a-108">Invalid request body</span></span>  <br/> |<span data-ttu-id="bb69a-109">Cette erreur devrait se produire rarement, si vous voyez cette erreur, renouvelez l’opération.</span><span class="sxs-lookup"><span data-stu-id="bb69a-109">This error should happen rarely, if you see this error, try the operation again.</span></span>  <br/> |
|<span data-ttu-id="bb69a-110">La valeur de hachage de matériel pour un périphérique est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="bb69a-110">Hardware hash value for a device isn't correct.</span></span>  <br/> |<span data-ttu-id="bb69a-111">Si cette erreur apparaît, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le hachage matériel d’un périphérique est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="bb69a-111">If you see this error, it means that the value you provided in your CSV file for the hardware hash of one device isn't correct.</span></span> <span data-ttu-id="bb69a-112">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="bb69a-112">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="bb69a-113">Si vous pensez que la valeur est correcte, mais que cette erreur persiste, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="bb69a-113">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="bb69a-114">Appareil affecté à un autre client</span><span class="sxs-lookup"><span data-stu-id="bb69a-114">Device assigned to another tenant</span></span>  <br/> |<span data-ttu-id="bb69a-115">Si cette erreur apparaît, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le numéro de série ou la clé de produit d’un ou plusieurs périphériques est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="bb69a-115">If you see this error, it means that the value you provided in your CSV file for either the serial number or the product key of one or more devices isn't correct.</span></span> <span data-ttu-id="bb69a-116">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="bb69a-116">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="bb69a-117">Si vous pensez que la valeur est correcte, mais que cette erreur persiste, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="bb69a-117">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="bb69a-118">Le fichier CSV contient un numéro de série ou une clé de produit non valide</span><span class="sxs-lookup"><span data-stu-id="bb69a-118">The CSV file contains an invalid serial number or product key</span></span>  <br/> |<span data-ttu-id="bb69a-119">Si cette erreur s’affiche, cela signifie que l’appareil que vous êtes Tyring d’enregistrer est déjà enregistré par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb69a-119">If you see this error it means that the device you are tyring to register is already registered by an other organization.</span></span> <span data-ttu-id="bb69a-120">Pour résoudre ce problème, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="bb69a-120">To fix this, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="bb69a-121">Ce périphérique n’est pas pris en charge pour l’installation à l’aide de AutoPilot</span><span class="sxs-lookup"><span data-stu-id="bb69a-121">This device is not supported for setup by using AutoPilot</span></span>  <br/> | <span data-ttu-id="bb69a-122">Cette erreur signifie que l’appareil ne répond pas à la configuration requise pour le déploiement de AutoPilot.</span><span class="sxs-lookup"><span data-stu-id="bb69a-122">This error means the device does not meet AutoPilot deployment requirements.</span></span> <span data-ttu-id="bb69a-123">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="bb69a-123">Devices need to meet these requirements:</span></span>  <br/>  <span data-ttu-id="bb69a-124">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="bb69a-124">Windows 10, version 1703 or later.</span></span>  <br/>  <span data-ttu-id="bb69a-125">Nouveaux appareils qui ne sont pas issus d'une expérience Windows prête à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="bb69a-125">New devices that have not been through Windows out-of-box experience.</span></span>  <br/> |
|<span data-ttu-id="bb69a-126">Appareil introuvable</span><span class="sxs-lookup"><span data-stu-id="bb69a-126">Device not found</span></span>  <br/> |<span data-ttu-id="bb69a-127">Cette erreur signifie qu’un ou plusieurs périphériques de votre fichier CSV ne sont pas enregistrés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bb69a-127">This error means that one or more devices in your CSV file is not registered to your organization.</span></span> <span data-ttu-id="bb69a-128">Pour résoudre ce problème, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="bb69a-128">To fix this, ask your hardware vendor for help.</span></span>  <br/> |
   
