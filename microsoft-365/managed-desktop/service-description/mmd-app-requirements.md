---
title: Exigences de l’application Bureau géré Microsoft
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
# <a name="microsoft-managed-desktop-app-requirements"></a><span data-ttu-id="ff574-103">Exigences de l’application Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="ff574-103">Microsoft Managed Desktop app requirements</span></span>

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreement for MMD. do not delete.-->

<!--Application addendum -->
 
<span data-ttu-id="ff574-104">Bureau géré Microsoft exige que nous gérions les appareils à l’aide d’une approche spécifique pour garantir les performances, la fiabilité et la serviceabilité des appareils.</span><span class="sxs-lookup"><span data-stu-id="ff574-104">Microsoft Managed Desktop requires that we manage devices using a specific approach to guarantee the performance, reliability, and serviceability of devices.</span></span>


|<span data-ttu-id="ff574-105">Domaine de gestion</span><span class="sxs-lookup"><span data-stu-id="ff574-105">Management area</span></span>  |<span data-ttu-id="ff574-106">Approche du Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="ff574-106">Microsoft Managed Desktop approach</span></span>  |
|---------|---------|
|<span data-ttu-id="ff574-107">Configuration de l’appareil ou gestion des stratégies</span><span class="sxs-lookup"><span data-stu-id="ff574-107">Device configuration or policy management</span></span>     |  <span data-ttu-id="ff574-108">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ff574-108">Microsoft Intune</span></span>       |
|<span data-ttu-id="ff574-109">Gestion des applications</span><span class="sxs-lookup"><span data-stu-id="ff574-109">Application management</span></span>     | <span data-ttu-id="ff574-110">Microsoft Intune et le portail d’entreprise</span><span class="sxs-lookup"><span data-stu-id="ff574-110">Microsoft Intune and Company Portal</span></span>        |
|<span data-ttu-id="ff574-111">Déploiement de pilotes</span><span class="sxs-lookup"><span data-stu-id="ff574-111">Driver deployment</span></span>     |  <span data-ttu-id="ff574-112">Pilotes inclus avec l’appareil, Windows Update ou Intune</span><span class="sxs-lookup"><span data-stu-id="ff574-112">Drivers included with the device, Windows Update, or Intune</span></span>       |
|<span data-ttu-id="ff574-113">Sécurité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ff574-113">Device security</span></span>     | <span data-ttu-id="ff574-114">Voir [Sécurité de l’appareil](security.md#device-security)</span><span class="sxs-lookup"><span data-stu-id="ff574-114">See [Device security](security.md#device-security)</span></span>      |
|<span data-ttu-id="ff574-115">Gestion des identités et des accès</span><span class="sxs-lookup"><span data-stu-id="ff574-115">Identity and access management</span></span>     | <span data-ttu-id="ff574-116">Voir [Gestion des identités et des accès](security.md#identity-and-access-management)</span><span class="sxs-lookup"><span data-stu-id="ff574-116">See [Identity and access management](security.md#identity-and-access-management)</span></span>        |
|<span data-ttu-id="ff574-117">Sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="ff574-117">Network security</span></span>     | <span data-ttu-id="ff574-118">Voir [Sécurité du réseau](security.md#network-security)</span><span class="sxs-lookup"><span data-stu-id="ff574-118">See [Network security](security.md#network-security)</span></span>        |
|<span data-ttu-id="ff574-119">Sécurité des informations</span><span class="sxs-lookup"><span data-stu-id="ff574-119">Information security</span></span>     |  <span data-ttu-id="ff574-120">Voir [Sécurité des informations](security.md#information-security)</span><span class="sxs-lookup"><span data-stu-id="ff574-120">See [Information security](security.md#information-security)</span></span>       |
|<span data-ttu-id="ff574-121">Récupération des données</span><span class="sxs-lookup"><span data-stu-id="ff574-121">Data recovery</span></span>     | <span data-ttu-id="ff574-122">OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="ff574-122">OneDrive for Business</span></span>        |
|<span data-ttu-id="ff574-123">Productivité de base</span><span class="sxs-lookup"><span data-stu-id="ff574-123">Core productivity</span></span>     | <span data-ttu-id="ff574-124">Applications Microsoft 365 for entreprise</span><span class="sxs-lookup"><span data-stu-id="ff574-124">Microsoft 365 Apps for enterprise</span></span>    |
|<span data-ttu-id="ff574-125">Navigateur</span><span class="sxs-lookup"><span data-stu-id="ff574-125">Browser</span></span>     | <span data-ttu-id="ff574-126">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ff574-126">Microsoft Edge</span></span>        |




<span data-ttu-id="ff574-127">Bureau géré Microsoft peut surveiller d’autres logiciels en cours d’exécution sur des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="ff574-127">Microsoft Managed Desktop might monitor other software running on managed devices.</span></span> <span data-ttu-id="ff574-128">Si cela a un impact négatif sur la gestion des appareils, la sécurité, les performances ou la fiabilité des appareils, vous demandons peut-être une [exception au plan de service.](customizing.md)</span><span class="sxs-lookup"><span data-stu-id="ff574-128">If it negatively impacts device management, device security, performance, or reliability, you might be required to request an [exception to the service plan](customizing.md).</span></span>
