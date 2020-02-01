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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c3ac23c5-d4b4-4b1b-b7ce-ea759521bf8c
description: Découvrez les États des appareils dans Microsoft 365 Business.
ms.openlocfilehash: 02b4eebac62a48e3ddd53d362db2d60067ac05eb
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41593968"
---
# <a name="device-states"></a><span data-ttu-id="13162-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="13162-103">Device states</span></span>

<span data-ttu-id="13162-104">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="13162-104">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="13162-106">**État**</span><span class="sxs-lookup"><span data-stu-id="13162-106">**Status**</span></span>|<span data-ttu-id="13162-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="13162-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13162-108">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="13162-108">Managed by Intune</span></span>  <br/> |<span data-ttu-id="13162-109">Géré par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="13162-109">Managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="13162-110">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="13162-110">Retire pending</span></span>  <br/> |<span data-ttu-id="13162-111">Microsoft 365 Entreprise s'apprête à supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="13162-111">Microsoft 365 Business is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="13162-112">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="13162-112">Retire in progress</span></span>  <br/> |<span data-ttu-id="13162-113">Microsoft 365 Entreprise est en train de supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="13162-113">Microsoft 365 Business is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="13162-114">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="13162-114">Retire failed</span></span>  <br/> | <span data-ttu-id="13162-115">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="13162-115">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="13162-116">Retrait annulé</span><span class="sxs-lookup"><span data-stu-id="13162-116">Retire canceled</span></span>  <br/> |<span data-ttu-id="13162-117">L’action de déclassement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="13162-117">Retire action was canceled.</span></span>  <br/> |
|<span data-ttu-id="13162-118">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="13162-118">Wipe pending</span></span>  <br/> |<span data-ttu-id="13162-119">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="13162-119">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="13162-120">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="13162-120">Wipe in progress</span></span>  <br/> |<span data-ttu-id="13162-121">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="13162-121">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="13162-122">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="13162-122">Wipe failed</span></span>  <br/> |<span data-ttu-id="13162-123">Impossible d’effectuer la réinitialisation d’usine.</span><span class="sxs-lookup"><span data-stu-id="13162-123">Couldn't do factory reset.</span></span>  <br/> |
|<span data-ttu-id="13162-124">Effacement annulé</span><span class="sxs-lookup"><span data-stu-id="13162-124">Wipe canceled</span></span>  <br/> |<span data-ttu-id="13162-125">La réinitialisation usine a été annulée.</span><span class="sxs-lookup"><span data-stu-id="13162-125">Factory wipe was canceled.</span></span>  <br/> |
|<span data-ttu-id="13162-126">Défectueux</span><span class="sxs-lookup"><span data-stu-id="13162-126">Unhealthy</span></span>  <br/> |<span data-ttu-id="13162-127">Une action est en attente (ou en cours), mais l’appareil n’a pas archivé pendant plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="13162-127">An action is pending (or in progress), but the device hasn't checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="13162-128">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="13162-128">Delete pending</span></span>  <br/> |<span data-ttu-id="13162-129">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="13162-129">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="13162-130">Détecté</span><span class="sxs-lookup"><span data-stu-id="13162-130">Discovered</span></span>  <br/> |<span data-ttu-id="13162-131">Microsoft 365 Entreprise a détecté l'appareil.</span><span class="sxs-lookup"><span data-stu-id="13162-131">Microsoft 365 Business has detected the device.</span></span>  <br/> |
   
