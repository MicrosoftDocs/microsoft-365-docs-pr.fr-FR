---
title: Résoudre les erreurs des appareils AutoPilot
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
manager: scotv
audience: Admin
ms.topic: article
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
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1f468690-530c-47ea-918f-fede24607c53
description: Découvrez comment résoudre les erreurs que vous pouvez voir lorsque vous travaillez avec des fichiers d’appareil AutoPilot dans Microsoft 365 Business Premium.
ms.openlocfilehash: 1078ab74b07952e4bb565555a081b98ecce9db5c
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578084"
---
# <a name="troubleshoot-autopilot-device-errors"></a><span data-ttu-id="29b67-103">Résoudre les erreurs des appareils AutoPilot</span><span class="sxs-lookup"><span data-stu-id="29b67-103">Troubleshoot AutoPilot device errors</span></span>

## <a name="device-file-error-messages"></a><span data-ttu-id="29b67-104">Messages d’erreur de fichier d’appareil</span><span class="sxs-lookup"><span data-stu-id="29b67-104">Device file error messages</span></span>

<span data-ttu-id="29b67-105">Voici des informations sur certaines des erreurs que vous pouvez voir lors de l’utilisation de fichiers d’appareil AutoPilot dans Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="29b67-105">Here's info on some of the errors you might see while working with AutoPilot device files in Microsoft 365 Business Premium.</span></span> 
  
|<span data-ttu-id="29b67-106">**Code d’erreur**</span><span class="sxs-lookup"><span data-stu-id="29b67-106">**Error code**</span></span>|<span data-ttu-id="29b67-107">**Corriger pour essayer**</span><span class="sxs-lookup"><span data-stu-id="29b67-107">**Fix to try**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29b67-108">Corps de la demande non valide</span><span class="sxs-lookup"><span data-stu-id="29b67-108">Invalid request body</span></span>  <br/> |<span data-ttu-id="29b67-109">Cette erreur doit se produire rarement, si vous voyez cette erreur, tentez à nouveau l’opération.</span><span class="sxs-lookup"><span data-stu-id="29b67-109">This error should happen rarely, if you see this error, try the operation again.</span></span>  <br/> |
|<span data-ttu-id="29b67-110">La valeur de hachage matériel d’un appareil n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="29b67-110">Hardware hash value for a device isn't correct.</span></span>  <br/> |<span data-ttu-id="29b67-111">Si vous voyez cette erreur, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le hachage matériel d’un appareil n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="29b67-111">If you see this error, it means that the value you provided in your CSV file for the hardware hash of one device isn't correct.</span></span> <span data-ttu-id="29b67-112">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="29b67-112">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="29b67-113">Si vous pensez que la valeur est correcte, mais que cette erreur se produit toujours, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="29b67-113">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="29b67-114">Appareil affecté à un autre client</span><span class="sxs-lookup"><span data-stu-id="29b67-114">Device assigned to another tenant</span></span>  <br/> |<span data-ttu-id="29b67-115">Si vous voyez cette erreur, cela signifie que la valeur que vous avez fournie dans votre fichier CSV pour le numéro de série ou la clé de produit d’un ou plusieurs appareils n’est pas correcte.</span><span class="sxs-lookup"><span data-stu-id="29b67-115">If you see this error, it means that the value you provided in your CSV file for either the serial number or the product key of one or more devices isn't correct.</span></span> <span data-ttu-id="29b67-116">Tout d’abord, vérifiez que la valeur a été tapée correctement.</span><span class="sxs-lookup"><span data-stu-id="29b67-116">First, verify that the value was typed correctly.</span></span> <span data-ttu-id="29b67-117">Si vous pensez que la valeur est correcte, mais que cette erreur se produit toujours, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="29b67-117">If you think that the value is correct, but this error is still happening, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="29b67-118">Le fichier CSV contient un numéro de série ou une clé de produit non valide</span><span class="sxs-lookup"><span data-stu-id="29b67-118">The CSV file contains an invalid serial number or product key</span></span>  <br/> |<span data-ttu-id="29b67-119">Si vous voyez cette erreur, cela signifie que l’appareil que vous essayez d’inscrire est déjà inscrit par une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="29b67-119">If you see this error, it means that the device you are trying to register is already registered by another organization.</span></span> <span data-ttu-id="29b67-120">Pour corriger cette erreur, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="29b67-120">To fix this error, ask your hardware vendor for help.</span></span>  <br/> |
|<span data-ttu-id="29b67-121">Cet appareil n’est pas pris en charge pour l’installation à l’aide d’AutoPilot</span><span class="sxs-lookup"><span data-stu-id="29b67-121">This device is not supported for setup by using AutoPilot</span></span>  <br/> | <span data-ttu-id="29b67-122">Cette erreur signifie que l’appareil ne répond pas aux exigences de déploiement AutoPilot.</span><span class="sxs-lookup"><span data-stu-id="29b67-122">This error means the device doesn't meet AutoPilot deployment requirements.</span></span> <span data-ttu-id="29b67-123">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="29b67-123">Devices need to meet these requirements:</span></span>  <br/>  <span data-ttu-id="29b67-124">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="29b67-124">Windows 10, version 1703 or later.</span></span>  <br/>  <span data-ttu-id="29b67-125">Les nouveaux appareils qui n’ont pas fait l’Windows l’expérience out-of-box.</span><span class="sxs-lookup"><span data-stu-id="29b67-125">New devices that haven't been through Windows out-of-box experience.</span></span>  <br/> |
|<span data-ttu-id="29b67-126">Appareil in trouvé</span><span class="sxs-lookup"><span data-stu-id="29b67-126">Device not found</span></span>  <br/> |<span data-ttu-id="29b67-127">Cette erreur signifie qu’un ou plusieurs appareils de votre fichier CSV ne sont pas inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="29b67-127">This error means that one or more devices in your CSV file isn't registered to your organization.</span></span> <span data-ttu-id="29b67-128">Pour résoudre ce problème, demandez de l’aide à votre fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="29b67-128">To fix this, ask your hardware vendor for help.</span></span>  <br/> |
