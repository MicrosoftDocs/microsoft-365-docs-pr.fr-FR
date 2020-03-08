---
title: États des appareils
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
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
- seo-marvel-mar
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c3ac23c5-d4b4-4b1b-b7ce-ea759521bf8c
description: Découvrez les différents États des appareils dans la liste actions de l’appareil dans la rubrique Accueil de l’administrateur de Microsoft 365 Business.
ms.openlocfilehash: bed1610814ca0d60adb4b4b3d0018e3e7e6d763f
ms.sourcegitcommit: 217de0fc54cbeaea32d253f175eaf338cd85f5af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/07/2020
ms.locfileid: "42560817"
---
# <a name="device-states"></a><span data-ttu-id="65a86-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="65a86-103">Device states</span></span>

<span data-ttu-id="65a86-104">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="65a86-104">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](../media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="65a86-106">**État**</span><span class="sxs-lookup"><span data-stu-id="65a86-106">**Status**</span></span>|<span data-ttu-id="65a86-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="65a86-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65a86-108">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="65a86-108">Managed by Intune</span></span>  <br/> |<span data-ttu-id="65a86-109">Géré par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="65a86-109">Managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="65a86-110">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="65a86-110">Retire pending</span></span>  <br/> |<span data-ttu-id="65a86-111">Microsoft 365 Entreprise s'apprête à supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="65a86-111">Microsoft 365 Business is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="65a86-112">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="65a86-112">Retire in progress</span></span>  <br/> |<span data-ttu-id="65a86-113">Microsoft 365 Entreprise est en train de supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="65a86-113">Microsoft 365 Business is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="65a86-114">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="65a86-114">Retire failed</span></span>  <br/> | <span data-ttu-id="65a86-115">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="65a86-115">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="65a86-116">Retrait annulé</span><span class="sxs-lookup"><span data-stu-id="65a86-116">Retire canceled</span></span>  <br/> |<span data-ttu-id="65a86-117">L’action de déclassement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="65a86-117">Retire action was canceled.</span></span>  <br/> |
|<span data-ttu-id="65a86-118">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="65a86-118">Wipe pending</span></span>  <br/> |<span data-ttu-id="65a86-119">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="65a86-119">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="65a86-120">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="65a86-120">Wipe in progress</span></span>  <br/> |<span data-ttu-id="65a86-121">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="65a86-121">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="65a86-122">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="65a86-122">Wipe failed</span></span>  <br/> |<span data-ttu-id="65a86-123">Impossible d’effectuer la réinitialisation d’usine.</span><span class="sxs-lookup"><span data-stu-id="65a86-123">Couldn't do factory reset.</span></span>  <br/> |
|<span data-ttu-id="65a86-124">Effacement annulé</span><span class="sxs-lookup"><span data-stu-id="65a86-124">Wipe canceled</span></span>  <br/> |<span data-ttu-id="65a86-125">La réinitialisation usine a été annulée.</span><span class="sxs-lookup"><span data-stu-id="65a86-125">Factory wipe was canceled.</span></span>  <br/> |
|<span data-ttu-id="65a86-126">Défectueux</span><span class="sxs-lookup"><span data-stu-id="65a86-126">Unhealthy</span></span>  <br/> |<span data-ttu-id="65a86-127">Une action est en attente (ou en cours), mais l’appareil n’a pas archivé pendant plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="65a86-127">An action is pending (or in progress), but the device hasn't checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="65a86-128">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="65a86-128">Delete pending</span></span>  <br/> |<span data-ttu-id="65a86-129">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="65a86-129">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="65a86-130">Détecté</span><span class="sxs-lookup"><span data-stu-id="65a86-130">Discovered</span></span>  <br/> |<span data-ttu-id="65a86-131">Microsoft 365 Entreprise a détecté l'appareil.</span><span class="sxs-lookup"><span data-stu-id="65a86-131">Microsoft 365 Business has detected the device.</span></span>  <br/> |
   
