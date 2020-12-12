---
title: Configuration requise pour les applications de bureau géré Microsoft
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
ms.openlocfilehash: 322a46ce48cce4d080e51f482178462934d5c8f2
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49659713"
---
# <a name="microsoft-managed-desktop-app-requirements"></a><span data-ttu-id="f9dca-103">Configuration requise pour les applications de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9dca-103">Microsoft Managed Desktop app requirements</span></span>

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreement for MMD. do not delete.-->

<!--Application addendum -->
 
<span data-ttu-id="f9dca-104">Microsoft Managed Desktop exige que nous administrions les appareils à l’aide d’une approche spécifique pour garantir les performances, la fiabilité et la facilité de service des appareils.</span><span class="sxs-lookup"><span data-stu-id="f9dca-104">Microsoft Managed Desktop requires that we manage devices using a specific approach to guarantee the performance, reliability, and serviceability of devices.</span></span>


|<span data-ttu-id="f9dca-105">Zone de gestion</span><span class="sxs-lookup"><span data-stu-id="f9dca-105">Management area</span></span>  |<span data-ttu-id="f9dca-106">Approche de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9dca-106">Microsoft Managed Desktop approach</span></span>  |
|---------|---------|
|<span data-ttu-id="f9dca-107">Configuration de l’appareil ou gestion des stratégies</span><span class="sxs-lookup"><span data-stu-id="f9dca-107">Device configuration or policy management</span></span>     |  <span data-ttu-id="f9dca-108">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="f9dca-108">Microsoft Intune</span></span>       |
|<span data-ttu-id="f9dca-109">Gestion des applications</span><span class="sxs-lookup"><span data-stu-id="f9dca-109">Application management</span></span>     | <span data-ttu-id="f9dca-110">Microsoft Intune et portail d’entreprise</span><span class="sxs-lookup"><span data-stu-id="f9dca-110">Microsoft Intune and Company Portal</span></span>        |
|<span data-ttu-id="f9dca-111">Déploiement de pilotes</span><span class="sxs-lookup"><span data-stu-id="f9dca-111">Driver deployment</span></span>     |  <span data-ttu-id="f9dca-112">Pilotes inclus avec l’appareil, Windows Update ou Intune</span><span class="sxs-lookup"><span data-stu-id="f9dca-112">Drivers included with the device, Windows Update, or Intune</span></span>       |
|<span data-ttu-id="f9dca-113">Sécurité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="f9dca-113">Device security</span></span>     | <span data-ttu-id="f9dca-114">Voir [sécurité des appareils](security.md#device-security)</span><span class="sxs-lookup"><span data-stu-id="f9dca-114">See [Device security](security.md#device-security)</span></span>      |
|<span data-ttu-id="f9dca-115">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="f9dca-115">Identity and access management</span></span>     | <span data-ttu-id="f9dca-116">Voir [gestion des identités et des accès](security.md#identity-and-access-management)</span><span class="sxs-lookup"><span data-stu-id="f9dca-116">See [Identity and access management](security.md#identity-and-access-management)</span></span>        |
|<span data-ttu-id="f9dca-117">Sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="f9dca-117">Network security</span></span>     | <span data-ttu-id="f9dca-118">Voir [sécurité réseau](security.md#network-security)</span><span class="sxs-lookup"><span data-stu-id="f9dca-118">See [Network security](security.md#network-security)</span></span>        |
|<span data-ttu-id="f9dca-119">Sécurité des informations</span><span class="sxs-lookup"><span data-stu-id="f9dca-119">Information security</span></span>     |  <span data-ttu-id="f9dca-120">Voir [sécurité des informations](security.md#information-security)</span><span class="sxs-lookup"><span data-stu-id="f9dca-120">See [Information security](security.md#information-security)</span></span>       |
|<span data-ttu-id="f9dca-121">Récupération de données</span><span class="sxs-lookup"><span data-stu-id="f9dca-121">Data recovery</span></span>     | <span data-ttu-id="f9dca-122">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="f9dca-122">OneDrive for Business</span></span>        |
|<span data-ttu-id="f9dca-123">Productivité de base</span><span class="sxs-lookup"><span data-stu-id="f9dca-123">Core productivity</span></span>     | <span data-ttu-id="f9dca-124">Applications Microsoft 365 for entreprise</span><span class="sxs-lookup"><span data-stu-id="f9dca-124">Microsoft 365 Apps for enterprise</span></span>    |
|<span data-ttu-id="f9dca-125">Navigateur</span><span class="sxs-lookup"><span data-stu-id="f9dca-125">Browser</span></span>     | <span data-ttu-id="f9dca-126">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f9dca-126">Microsoft Edge</span></span>        |




<span data-ttu-id="f9dca-127">Microsoft Managed Desktop peut surveiller d’autres logiciels s’exécutant sur des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="f9dca-127">Microsoft Managed Desktop might monitor other software running on managed devices.</span></span> <span data-ttu-id="f9dca-128">Si elle a un impact négatif sur la gestion des appareils, la sécurité des appareils, les performances ou la fiabilité, vous devrez peut-être demander une [exception au plan de service](customizing.md).</span><span class="sxs-lookup"><span data-stu-id="f9dca-128">If it negatively impacts device management, device security, performance, or reliability, you might be required to request an [exception to the service plan](customizing.md).</span></span>
