---
title: États des appareils
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c3ac23c5-d4b4-4b1b-b7ce-ea759521bf8c
description: Découvrez les États des appareils dans Microsoft 365 Business.
ms.openlocfilehash: b55e6a5d538ec28d195225e93797cea27afd2e8b
ms.sourcegitcommit: 8193b7da5b1a415835d02ca96883c351df7326ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38320205"
---
# <a name="device-states"></a><span data-ttu-id="26dc2-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="26dc2-103">Device states</span></span>

<span data-ttu-id="26dc2-104">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="26dc2-104">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="26dc2-106">**État**</span><span class="sxs-lookup"><span data-stu-id="26dc2-106">**Status**</span></span>|<span data-ttu-id="26dc2-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="26dc2-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26dc2-108">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="26dc2-108">Managed by Intune</span></span>  <br/> |<span data-ttu-id="26dc2-109">Géré par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="26dc2-109">Managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="26dc2-110">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="26dc2-110">Retire pending</span></span>  <br/> |<span data-ttu-id="26dc2-111">Microsoft 365 Entreprise s'apprête à supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="26dc2-111">Microsoft 365 Business is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="26dc2-112">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="26dc2-112">Retire in progress</span></span>  <br/> |<span data-ttu-id="26dc2-113">Microsoft 365 Entreprise est en train de supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="26dc2-113">Microsoft 365 Business is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="26dc2-114">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="26dc2-114">Retire failed</span></span>  <br/> | <span data-ttu-id="26dc2-115">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="26dc2-115">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="26dc2-116">Retrait annulé</span><span class="sxs-lookup"><span data-stu-id="26dc2-116">Retire canceled</span></span>  <br/> |<span data-ttu-id="26dc2-117">L’action de déclassement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="26dc2-117">Retire action was canceled.</span></span>  <br/> |
|<span data-ttu-id="26dc2-118">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="26dc2-118">Wipe pending</span></span>  <br/> |<span data-ttu-id="26dc2-119">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="26dc2-119">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="26dc2-120">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="26dc2-120">Wipe in progress</span></span>  <br/> |<span data-ttu-id="26dc2-121">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="26dc2-121">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="26dc2-122">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="26dc2-122">Wipe failed</span></span>  <br/> |<span data-ttu-id="26dc2-123">Impossible d’effectuer la réinitialisation d’usine.</span><span class="sxs-lookup"><span data-stu-id="26dc2-123">Couldn't do factory reset.</span></span>  <br/> |
|<span data-ttu-id="26dc2-124">Effacement annulé</span><span class="sxs-lookup"><span data-stu-id="26dc2-124">Wipe canceled</span></span>  <br/> |<span data-ttu-id="26dc2-125">La réinitialisation usine a été annulée.</span><span class="sxs-lookup"><span data-stu-id="26dc2-125">Factory wipe was canceled.</span></span>  <br/> |
|<span data-ttu-id="26dc2-126">Défectueux</span><span class="sxs-lookup"><span data-stu-id="26dc2-126">Unhealthy</span></span>  <br/> |<span data-ttu-id="26dc2-127">Une action est en attente (ou en cours), mais l’appareil n’a pas archivé pendant plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="26dc2-127">An action is pending (or in progress), but the device hasn't checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="26dc2-128">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="26dc2-128">Delete pending</span></span>  <br/> |<span data-ttu-id="26dc2-129">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="26dc2-129">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="26dc2-130">Détecté</span><span class="sxs-lookup"><span data-stu-id="26dc2-130">Discovered</span></span>  <br/> |<span data-ttu-id="26dc2-131">Microsoft 365 Entreprise a détecté l'appareil.</span><span class="sxs-lookup"><span data-stu-id="26dc2-131">Microsoft 365 Business has detected the device.</span></span>  <br/> |
   
