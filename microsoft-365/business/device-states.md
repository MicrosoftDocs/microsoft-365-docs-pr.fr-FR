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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: c3ac23c5-d4b4-4b1b-b7ce-ea759521bf8c
description: Découvrez les différents états de l’appareil dans la liste Actions de l’appareil dans la page Accueil de l’administrateur dans Microsoft 365 pour les entreprises.
ms.openlocfilehash: 64138e2b6ae73c067709cde1912a96615d08ebf1
ms.sourcegitcommit: 2d664a95b9875f0775f0da44aca73b16a816e1c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2020
ms.locfileid: "44471176"
---
# <a name="device-states"></a><span data-ttu-id="3847d-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="3847d-103">Device states</span></span>

<span data-ttu-id="3847d-104">Cet article s’applique à Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="3847d-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="3847d-105">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="3847d-105">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](../media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="3847d-107">**État**</span><span class="sxs-lookup"><span data-stu-id="3847d-107">**Status**</span></span>|<span data-ttu-id="3847d-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="3847d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3847d-109">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="3847d-109">Managed by Intune</span></span>  <br/> |<span data-ttu-id="3847d-110">Géré par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="3847d-110">Managed by Microsoft 365 Business Premium.</span></span>  <br/> |
|<span data-ttu-id="3847d-111">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="3847d-111">Retire pending</span></span>  <br/> |<span data-ttu-id="3847d-112">Microsoft 365 Business Premium se prépare à supprimer des données d’entreprise de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3847d-112">Microsoft 365 Business Premium is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="3847d-113">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="3847d-113">Retire in progress</span></span>  <br/> |<span data-ttu-id="3847d-114">Microsoft 365 Business Premium supprime actuellement les données d’entreprise de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3847d-114">Microsoft 365 Business Premium is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="3847d-115">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="3847d-115">Retire failed</span></span>  <br/> | <span data-ttu-id="3847d-116">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="3847d-116">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="3847d-117">Retrait annulé</span><span class="sxs-lookup"><span data-stu-id="3847d-117">Retire canceled</span></span>  <br/> |<span data-ttu-id="3847d-118">L’action de retrait a été annulée.</span><span class="sxs-lookup"><span data-stu-id="3847d-118">Retire action was canceled.</span></span>  <br/> |
|<span data-ttu-id="3847d-119">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="3847d-119">Wipe pending</span></span>  <br/> |<span data-ttu-id="3847d-120">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="3847d-120">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="3847d-121">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="3847d-121">Wipe in progress</span></span>  <br/> |<span data-ttu-id="3847d-122">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="3847d-122">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="3847d-123">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="3847d-123">Wipe failed</span></span>  <br/> |<span data-ttu-id="3847d-124">Impossible de réinitialiser les fabriques.</span><span class="sxs-lookup"><span data-stu-id="3847d-124">Couldn't do factory reset.</span></span>  <br/> |
|<span data-ttu-id="3847d-125">Effacement annulé</span><span class="sxs-lookup"><span data-stu-id="3847d-125">Wipe canceled</span></span>  <br/> |<span data-ttu-id="3847d-126">L’effacement d’usine a été annulé.</span><span class="sxs-lookup"><span data-stu-id="3847d-126">Factory wipe was canceled.</span></span>  <br/> |
|<span data-ttu-id="3847d-127">Défectueux</span><span class="sxs-lookup"><span data-stu-id="3847d-127">Unhealthy</span></span>  <br/> |<span data-ttu-id="3847d-128">Une action est en attente (ou en cours), mais l’appareil n’a pas été enregistré depuis plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="3847d-128">An action is pending (or in progress), but the device hasn't checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="3847d-129">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="3847d-129">Delete pending</span></span>  <br/> |<span data-ttu-id="3847d-130">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="3847d-130">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="3847d-131">Détecté</span><span class="sxs-lookup"><span data-stu-id="3847d-131">Discovered</span></span>  <br/> |<span data-ttu-id="3847d-132">Microsoft 365 Business Premium a détecté l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3847d-132">Microsoft 365 Business Premium has detected the device.</span></span>  <br/> |
   
