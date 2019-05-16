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
ms.openlocfilehash: 06e5c800e6a104785c1fd0724223e05d7729722e
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34072717"
---
# <a name="device-states"></a><span data-ttu-id="cbb02-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="cbb02-103">Device states</span></span>

## <a name="device-states"></a><span data-ttu-id="cbb02-104">États des appareils</span><span class="sxs-lookup"><span data-stu-id="cbb02-104">Device states</span></span>

<span data-ttu-id="cbb02-105">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="cbb02-105">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="cbb02-107">**État**</span><span class="sxs-lookup"><span data-stu-id="cbb02-107">**Status**</span></span>|<span data-ttu-id="cbb02-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="cbb02-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbb02-109">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="cbb02-109">Managed by Intune</span></span>  <br/> |<span data-ttu-id="cbb02-110">Géré par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="cbb02-110">Managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="cbb02-111">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="cbb02-111">Retire pending</span></span>  <br/> |<span data-ttu-id="cbb02-112">Microsoft 365 Entreprise s'apprête à supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="cbb02-112">Microsoft 365 Business is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="cbb02-113">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="cbb02-113">Retire in progress</span></span>  <br/> |<span data-ttu-id="cbb02-114">Microsoft 365 Entreprise est en train de supprimer des données d'entreprise de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="cbb02-114">Microsoft 365 Business is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="cbb02-115">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="cbb02-115">Retire failed</span></span>  <br/> | <span data-ttu-id="cbb02-116">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="cbb02-116">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="cbb02-117">Mise hors service annulée</span><span class="sxs-lookup"><span data-stu-id="cbb02-117">Retire cancelled</span></span>  <br/> |<span data-ttu-id="cbb02-118">L'action de mise hors service a été annulée.</span><span class="sxs-lookup"><span data-stu-id="cbb02-118">Retire action was cancelled.</span></span>  <br/> |
|<span data-ttu-id="cbb02-119">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="cbb02-119">Wipe pending</span></span>  <br/> |<span data-ttu-id="cbb02-120">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="cbb02-120">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="cbb02-121">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="cbb02-121">Wipe in progress</span></span>  <br/> |<span data-ttu-id="cbb02-122">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="cbb02-122">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="cbb02-123">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="cbb02-123">Wipe failed</span></span>  <br/> |<span data-ttu-id="cbb02-124">Le rétablissement des paramètres d'usine n'a pas pu être effectué.</span><span class="sxs-lookup"><span data-stu-id="cbb02-124">Couldn't perform factory reset.</span></span>  <br/> |
|<span data-ttu-id="cbb02-125">Réinitialisation annulée</span><span class="sxs-lookup"><span data-stu-id="cbb02-125">Wipe cancelled</span></span>  <br/> |<span data-ttu-id="cbb02-126">Le rétablissement des paramètres d'usine a été annulé.</span><span class="sxs-lookup"><span data-stu-id="cbb02-126">Factory wipe was cancelled.</span></span>  <br/> |
|<span data-ttu-id="cbb02-127">Défectueux</span><span class="sxs-lookup"><span data-stu-id="cbb02-127">Unhealthy</span></span>  <br/> |<span data-ttu-id="cbb02-128">Cela signifie qu'une action est en attente (ou en cours) mais que l'appareil n'a pas archivé depuis plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="cbb02-128">This means that an action is pending (or in progress) but the device has not checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="cbb02-129">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="cbb02-129">Delete pending</span></span>  <br/> |<span data-ttu-id="cbb02-130">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="cbb02-130">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="cbb02-131">Détecté</span><span class="sxs-lookup"><span data-stu-id="cbb02-131">Discovered</span></span>  <br/> |<span data-ttu-id="cbb02-132">Microsoft 365 Entreprise a détecté l'appareil.</span><span class="sxs-lookup"><span data-stu-id="cbb02-132">Microsoft 365 Business has detected the device.</span></span>  <br/> |
   
