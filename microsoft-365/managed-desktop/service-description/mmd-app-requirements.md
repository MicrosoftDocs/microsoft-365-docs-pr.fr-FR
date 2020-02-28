---
title: Configuration requise pour les applications de bureau géré Microsoft
description: ''
keywords: Microsoft Managed Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 01c580cd671a84ef68c18b114e133f046a3e5b3b
ms.sourcegitcommit: 7930fb8327bbd3594fde52f2dbf91e0f5d92f684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2020
ms.locfileid: "42328066"
---
# <a name="microsoft-managed-desktop-app-requirements"></a><span data-ttu-id="2151f-103">Configuration requise pour les applications de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="2151f-103">Microsoft Managed Desktop app requirements</span></span>

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreement for MMD. do not delete.-->

<!--Application addendum -->
 
<span data-ttu-id="2151f-104">Afin de garantir les performances, la fiabilité et la maintenance des périphériques de bureau géré Microsoft, les applications métier d’un client ne doivent pas sérieusement influer sur l’expérience de l’utilisateur final ou modifier l’attitude de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="2151f-104">In order to guarantee the performance, reliability, and serviceability of Microsoft Managed Desktop devices a customer’s line of business apps must not seriously impact end user experience or modify the security stance.</span></span> <span data-ttu-id="2151f-105">Par conséquent, les applications métier que vous souhaitez déployer sur des appareils de bureau gérés Microsoft doivent répondre aux exigences de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2151f-105">Consequently, line of business applications that you want to deploy to Microsoft Managed Desktop devices must meet the requirements in this topic.</span></span>

## <a name="application-condition"></a><span data-ttu-id="2151f-106">Condition de l’application</span><span class="sxs-lookup"><span data-stu-id="2151f-106">Application condition</span></span>

<span data-ttu-id="2151f-107">Il est important que les applications n’aient pas d’impact négatif sur l’environnement de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-107">It’s important that applications don’t adversely impact the Microsoft Managed Desktop environment.</span></span> <span data-ttu-id="2151f-108">Voici les conditions requises qu’une application doit respecter pour qu’une application soit déployée.</span><span class="sxs-lookup"><span data-stu-id="2151f-108">The following are the requirements that an application must meet for an application to be deployed.</span></span> <span data-ttu-id="2151f-109">Pour une application ou un pilote donné, Microsoft peut renoncer aux exigences fournies dans le présent document.</span><span class="sxs-lookup"><span data-stu-id="2151f-109">For any given application or driver, Microsoft may waive any requirement provided herein.</span></span> <span data-ttu-id="2151f-110">Microsoft peut décider de supprimer une application ou un pilote qui a un impact négatif sur les performances et la fiabilité des appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-110">Microsoft may decide to remove any application or driver that negatively impacts performance and reliability of Microsoft Managed Desktop devices.</span></span>

## <a name="centrally-managed-apps"></a><span data-ttu-id="2151f-111">Applications gérées de manière centralisée</span><span class="sxs-lookup"><span data-stu-id="2151f-111">Centrally managed apps</span></span>

<span data-ttu-id="2151f-112">Toutes les applications et tous les pilotes installés sur les appareils gérés par Microsoft doivent être déployés via Microsoft Intune, le Microsoft Store ou Microsoft Store pour les entreprises ; s’ils sont disponibles, les pilotes seront également déployés via le service Windows Update.</span><span class="sxs-lookup"><span data-stu-id="2151f-112">All applications and drivers installed on Microsoft Managed Devices must be deployed through Microsoft Intune, the Microsoft Store, or the Microsoft Store for Business; if available, drivers will also be deployed through the Windows Update service.</span></span> 

## <a name="prohibited-app-classes"></a><span data-ttu-id="2151f-113">Classes d’application interdites</span><span class="sxs-lookup"><span data-stu-id="2151f-113">Prohibited app classes</span></span>

<span data-ttu-id="2151f-114">Certains types d’application ne sont pas autorisés sur les appareils de bureau géré Microsoft :</span><span class="sxs-lookup"><span data-stu-id="2151f-114">Certain application types are not permitted on Microsoft Managed Desktop devices:</span></span>
- <span data-ttu-id="2151f-115">logiciels antivirus, de sécurité ou d’audit tiers</span><span class="sxs-lookup"><span data-stu-id="2151f-115">3rd party anti-virus, security, or audit software</span></span>
- <span data-ttu-id="2151f-116">Versions de Microsoft Office antérieures à Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="2151f-116">Versions of Microsoft Office prior to Office 365 ProPlus</span></span>
- <span data-ttu-id="2151f-117">Applications qui installent ou regroupent d’autres logiciels tiers</span><span class="sxs-lookup"><span data-stu-id="2151f-117">Applications that install or bundle other 3rd party software</span></span>

## <a name="restricted-app-behaviors"></a><span data-ttu-id="2151f-118">Comportements d’application restreinte</span><span class="sxs-lookup"><span data-stu-id="2151f-118">Restricted app behaviors</span></span>

<span data-ttu-id="2151f-119">Certains comportements d’application peuvent avoir un impact négatif sur l’expérience utilisateur ou présenter un risque de sécurité aux appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-119">Certain app behaviors can negatively impact the user experience or may present a security risk to Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="2151f-120">Les applications présentant les comportements suivants ne sont pas autorisées à s’exécuter dans l’environnement de bureau géré Microsoft, sans avoir une spécificité de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-120">Apps with the following behaviors are not permitted to run in the Microsoft Managed Desktop environment without a specific  from Microsoft.</span></span>

<span data-ttu-id="2151f-121">Expérience utilisateur :</span><span class="sxs-lookup"><span data-stu-id="2151f-121">User Experience:</span></span>
- <span data-ttu-id="2151f-122">Installer les services d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="2151f-122">Install background services</span></span>
- <span data-ttu-id="2151f-123">S’ajouter au chemin de démarrage de Windows</span><span class="sxs-lookup"><span data-stu-id="2151f-123">Add itself to the Windows startup path</span></span>
- <span data-ttu-id="2151f-124">Applications dépendant des pilotes</span><span class="sxs-lookup"><span data-stu-id="2151f-124">Applications dependent on drivers</span></span>
- <span data-ttu-id="2151f-125">navigateurs Web tiers</span><span class="sxs-lookup"><span data-stu-id="2151f-125">3rd party web browsers</span></span>

<span data-ttu-id="2151f-126">Sécurité :</span><span class="sxs-lookup"><span data-stu-id="2151f-126">Security:</span></span>
- <span data-ttu-id="2151f-127">Élever les privilèges de l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="2151f-127">Elevate the end user’s privileges</span></span>
- <span data-ttu-id="2151f-128">Agir en tant que magasin d’applications ou disposer d’un gestionnaire d’extensions intégré</span><span class="sxs-lookup"><span data-stu-id="2151f-128">Act as an app store or have a built-in extension manager</span></span>
- <span data-ttu-id="2151f-129">Ont des failles de sécurité connues</span><span class="sxs-lookup"><span data-stu-id="2151f-129">Have known security vulnerabilities</span></span>
- <span data-ttu-id="2151f-130">Chiffrer ou restreindre l’accès aux données de l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="2151f-130">Encrypt or restrict access to end-user data</span></span>
- <span data-ttu-id="2151f-131">Non signé ou signé à l’aide d’un certificat qui ne se cumule pas vers une racine approuvée</span><span class="sxs-lookup"><span data-stu-id="2151f-131">Is unsigned or is signed using a certificate which doesn’t roll up to a trusted root</span></span>


## <a name="driver-deployment"></a><span data-ttu-id="2151f-132">Déploiement de pilotes</span><span class="sxs-lookup"><span data-stu-id="2151f-132">Driver deployment</span></span>

<span data-ttu-id="2151f-133">Microsoft Managed Desktop prend en charge uniquement les pilotes de périphériques disponibles via Windows Update ou la boîte de réception installée avec l’appareil géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-133">Microsoft Managed Desktop only supports device drivers that are available through Windows Update or installed inbox with the Microsoft Managed Device.</span></span> 

<span data-ttu-id="2151f-134">Si une application requiert un ou plusieurs pilotes pour l’exécuter, elle est considérée comme une application restreinte et nécessite une exception avant d’être déployée sur le bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2151f-134">If an application requires a specific driver(s) to run it is considered a Restricted Application and requires an exception before being deployed to Microsoft Managed Desktop.</span></span> 

