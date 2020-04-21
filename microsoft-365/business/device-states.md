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
description: Découvrez les différents États des appareils dans la liste actions de l’appareil dans la rubrique Accueil de l’administrateur dans Microsoft 365 pour les entreprises.
ms.openlocfilehash: 1a66e76dd3a74428923292427b01551db2449e48
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43627243"
---
# <a name="device-states"></a><span data-ttu-id="efbfd-103">États des appareils</span><span class="sxs-lookup"><span data-stu-id="efbfd-103">Device states</span></span>

<span data-ttu-id="efbfd-104">Les appareils de la liste **Actions de l'appareil** (accueil Administrateur \> **Actions de l'appareil**) peuvent présenter les états suivants.</span><span class="sxs-lookup"><span data-stu-id="efbfd-104">Devices in the **Device actions** list (Admin home \> **Device actions**) can have the following states.</span></span>
  
![In the Device actions list, you can see the Devices states.](../media/a621c47e-45d9-4e1a-beb9-c03254d40c1d.png)
  
|<span data-ttu-id="efbfd-106">**État**</span><span class="sxs-lookup"><span data-stu-id="efbfd-106">**Status**</span></span>|<span data-ttu-id="efbfd-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="efbfd-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efbfd-108">Géré par Intune</span><span class="sxs-lookup"><span data-stu-id="efbfd-108">Managed by Intune</span></span>  <br/> |<span data-ttu-id="efbfd-109">Géré par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="efbfd-109">Managed by Microsoft 365 Business Premium.</span></span>  <br/> |
|<span data-ttu-id="efbfd-110">Mise hors service en attente</span><span class="sxs-lookup"><span data-stu-id="efbfd-110">Retire pending</span></span>  <br/> |<span data-ttu-id="efbfd-111">Microsoft 365 Business Premium se prépare à supprimer les données d’entreprise de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="efbfd-111">Microsoft 365 Business Premium is getting ready to remove company data from the device.</span></span>  <br/> |
|<span data-ttu-id="efbfd-112">Mise hors service en cours</span><span class="sxs-lookup"><span data-stu-id="efbfd-112">Retire in progress</span></span>  <br/> |<span data-ttu-id="efbfd-113">Microsoft 365 Business Premium supprime actuellement les données d’entreprise de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="efbfd-113">Microsoft 365 Business Premium is currently removing company data from the device.</span></span>  <br/> |
|<span data-ttu-id="efbfd-114">Échec de la mise hors service</span><span class="sxs-lookup"><span data-stu-id="efbfd-114">Retire failed</span></span>  <br/> | <span data-ttu-id="efbfd-115">L'action de suppression des données d'entreprise a échoué.</span><span class="sxs-lookup"><span data-stu-id="efbfd-115">Remove company data action failed.</span></span>  <br/> |
|<span data-ttu-id="efbfd-116">Retrait annulé</span><span class="sxs-lookup"><span data-stu-id="efbfd-116">Retire canceled</span></span>  <br/> |<span data-ttu-id="efbfd-117">L’action de déclassement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="efbfd-117">Retire action was canceled.</span></span>  <br/> |
|<span data-ttu-id="efbfd-118">Réinitialisation en attente</span><span class="sxs-lookup"><span data-stu-id="efbfd-118">Wipe pending</span></span>  <br/> |<span data-ttu-id="efbfd-119">En attente du rétablissement des paramètres d'usine.</span><span class="sxs-lookup"><span data-stu-id="efbfd-119">Waiting for factory reset to start.</span></span>  <br/> |
|<span data-ttu-id="efbfd-120">Réinitialisation en cours</span><span class="sxs-lookup"><span data-stu-id="efbfd-120">Wipe in progress</span></span>  <br/> |<span data-ttu-id="efbfd-121">Le rétablissement des paramètres d'usine a démarré.</span><span class="sxs-lookup"><span data-stu-id="efbfd-121">Factory reset has been issued.</span></span>  <br/> |
|<span data-ttu-id="efbfd-122">Échec de la réinitialisation</span><span class="sxs-lookup"><span data-stu-id="efbfd-122">Wipe failed</span></span>  <br/> |<span data-ttu-id="efbfd-123">Impossible d’effectuer la réinitialisation d’usine.</span><span class="sxs-lookup"><span data-stu-id="efbfd-123">Couldn't do factory reset.</span></span>  <br/> |
|<span data-ttu-id="efbfd-124">Effacement annulé</span><span class="sxs-lookup"><span data-stu-id="efbfd-124">Wipe canceled</span></span>  <br/> |<span data-ttu-id="efbfd-125">La réinitialisation usine a été annulée.</span><span class="sxs-lookup"><span data-stu-id="efbfd-125">Factory wipe was canceled.</span></span>  <br/> |
|<span data-ttu-id="efbfd-126">Défectueux</span><span class="sxs-lookup"><span data-stu-id="efbfd-126">Unhealthy</span></span>  <br/> |<span data-ttu-id="efbfd-127">Une action est en attente (ou en cours), mais l’appareil n’a pas archivé pendant plus de 30 jours.</span><span class="sxs-lookup"><span data-stu-id="efbfd-127">An action is pending (or in progress), but the device hasn't checked in for 30+ days.</span></span>  <br/> |
|<span data-ttu-id="efbfd-128">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="efbfd-128">Delete pending</span></span>  <br/> |<span data-ttu-id="efbfd-129">Une action de suppression est en attente.</span><span class="sxs-lookup"><span data-stu-id="efbfd-129">Delete action is pending.</span></span>  <br/> |
|<span data-ttu-id="efbfd-130">Détecté</span><span class="sxs-lookup"><span data-stu-id="efbfd-130">Discovered</span></span>  <br/> |<span data-ttu-id="efbfd-131">Microsoft 365 Business Premium a détecté l’appareil.</span><span class="sxs-lookup"><span data-stu-id="efbfd-131">Microsoft 365 Business Premium has detected the device.</span></span>  <br/> |
   
