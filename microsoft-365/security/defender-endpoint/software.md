---
title: Méthodes et propriétés logicielles
description: Récupère les principales alertes récentes.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 9bfec2c4e65a390189556c14347eaf17236fb95e
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187199"
---
# <a name="software-resource-type"></a><span data-ttu-id="9f652-104">Type de ressource logicielle</span><span class="sxs-lookup"><span data-stu-id="9f652-104">Software resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9f652-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9f652-105">**Applies to:**</span></span>
- [<span data-ttu-id="9f652-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9f652-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9f652-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9f652-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="9f652-108">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="9f652-108">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="9f652-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9f652-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9f652-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9f652-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="methods"></a><span data-ttu-id="9f652-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9f652-111">Methods</span></span>

<span data-ttu-id="9f652-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="9f652-112">Method</span></span> |<span data-ttu-id="9f652-113">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="9f652-113">Return Type</span></span> |<span data-ttu-id="9f652-114">Description</span><span class="sxs-lookup"><span data-stu-id="9f652-114">Description</span></span>
:---|:---|:---
[<span data-ttu-id="9f652-115">List software</span><span class="sxs-lookup"><span data-stu-id="9f652-115">List software</span></span>](get-software.md) | <span data-ttu-id="9f652-116">Collection de logiciels</span><span class="sxs-lookup"><span data-stu-id="9f652-116">Software collection</span></span> | <span data-ttu-id="9f652-117">Liste de l’inventaire logiciel de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="9f652-117">List the organizational software inventory.</span></span>
[<span data-ttu-id="9f652-118">Obtenir le logiciel par ID</span><span class="sxs-lookup"><span data-stu-id="9f652-118">Get software by Id</span></span>](get-software-by-id.md) | <span data-ttu-id="9f652-119">Logiciels</span><span class="sxs-lookup"><span data-stu-id="9f652-119">Software</span></span> | <span data-ttu-id="9f652-120">Obtenez un logiciel spécifique par son ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="9f652-120">Get a specific software by its software ID.</span></span>
[<span data-ttu-id="9f652-121">Liste de la distribution des versions des logiciels</span><span class="sxs-lookup"><span data-stu-id="9f652-121">List software version distribution</span></span>](get-software-ver-distribution.md)| <span data-ttu-id="9f652-122">Collection de distribution</span><span class="sxs-lookup"><span data-stu-id="9f652-122">Distribution collection</span></span> | <span data-ttu-id="9f652-123">Liste de la distribution des versions des logiciels par ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="9f652-123">List software version distribution by software ID.</span></span>
[<span data-ttu-id="9f652-124">Lister les ordinateurs par logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-124">List machines by software</span></span>](get-machines-by-software.md)| <span data-ttu-id="9f652-125">Collection MachineRef</span><span class="sxs-lookup"><span data-stu-id="9f652-125">MachineRef collection</span></span> | <span data-ttu-id="9f652-126">Récupérez la liste des appareils associés à l’ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="9f652-126">Retrieve a list of devices that are associated with the software ID.</span></span>
[<span data-ttu-id="9f652-127">Liste des vulnérabilités par logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-127">List vulnerabilities by software</span></span>](get-vuln-by-software.md) | <span data-ttu-id="9f652-128">[Collection de vulnérabilités](vulnerability.md)</span><span class="sxs-lookup"><span data-stu-id="9f652-128">[Vulnerability](vulnerability.md) collection</span></span> | <span data-ttu-id="9f652-129">Récupérez la liste des vulnérabilités associées à l’ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="9f652-129">Retrieve a list of vulnerabilities associated with the software ID.</span></span>
[<span data-ttu-id="9f652-130">Obtenir les ko manquants</span><span class="sxs-lookup"><span data-stu-id="9f652-130">Get missing KBs</span></span>](get-missing-kbs-software.md) | <span data-ttu-id="9f652-131">Collection KB</span><span class="sxs-lookup"><span data-stu-id="9f652-131">KB collection</span></span> | <span data-ttu-id="9f652-132">Obtenir la liste des ko manquants associés à l’ID logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-132">Get a list of missing KBs associated with the software ID</span></span>

## <a name="properties"></a><span data-ttu-id="9f652-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f652-133">Properties</span></span>

<span data-ttu-id="9f652-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="9f652-134">Property</span></span> |   <span data-ttu-id="9f652-135">Type</span><span class="sxs-lookup"><span data-stu-id="9f652-135">Type</span></span>   |   <span data-ttu-id="9f652-136">Description</span><span class="sxs-lookup"><span data-stu-id="9f652-136">Description</span></span>
:---|:---|:---
<span data-ttu-id="9f652-137">id</span><span class="sxs-lookup"><span data-stu-id="9f652-137">id</span></span> | <span data-ttu-id="9f652-138">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9f652-138">String</span></span> | <span data-ttu-id="9f652-139">ID logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-139">Software ID</span></span>
<span data-ttu-id="9f652-140">Nom</span><span class="sxs-lookup"><span data-stu-id="9f652-140">Name</span></span> | <span data-ttu-id="9f652-141">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9f652-141">String</span></span> | <span data-ttu-id="9f652-142">Nom du logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-142">Software name</span></span>
<span data-ttu-id="9f652-143">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="9f652-143">Vendor</span></span> | <span data-ttu-id="9f652-144">Chaîne</span><span class="sxs-lookup"><span data-stu-id="9f652-144">String</span></span> | <span data-ttu-id="9f652-145">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="9f652-145">Software vendor name</span></span>
<span data-ttu-id="9f652-146">Faiblesses</span><span class="sxs-lookup"><span data-stu-id="9f652-146">Weaknesses</span></span> | <span data-ttu-id="9f652-147">Entier long</span><span class="sxs-lookup"><span data-stu-id="9f652-147">Long</span></span> | <span data-ttu-id="9f652-148">Nombre de vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="9f652-148">Number of discovered vulnerabilities</span></span>
<span data-ttu-id="9f652-149">publicExploit</span><span class="sxs-lookup"><span data-stu-id="9f652-149">publicExploit</span></span> | <span data-ttu-id="9f652-150">Booléen</span><span class="sxs-lookup"><span data-stu-id="9f652-150">Boolean</span></span> | <span data-ttu-id="9f652-151">Une exploitation publique existe pour certaines vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="9f652-151">Public exploit exists for some of the vulnerabilities</span></span>
<span data-ttu-id="9f652-152">activeAlert</span><span class="sxs-lookup"><span data-stu-id="9f652-152">activeAlert</span></span> | <span data-ttu-id="9f652-153">Booléen</span><span class="sxs-lookup"><span data-stu-id="9f652-153">Boolean</span></span> | <span data-ttu-id="9f652-154">L’alerte active est associée à ce logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-154">Active alert is associated with this software</span></span>
<span data-ttu-id="9f652-155">exposedMachines</span><span class="sxs-lookup"><span data-stu-id="9f652-155">exposedMachines</span></span> | <span data-ttu-id="9f652-156">Entier long</span><span class="sxs-lookup"><span data-stu-id="9f652-156">Long</span></span> | <span data-ttu-id="9f652-157">Nombre d’appareils exposés</span><span class="sxs-lookup"><span data-stu-id="9f652-157">Number of exposed devices</span></span>
<span data-ttu-id="9f652-158">impactScore</span><span class="sxs-lookup"><span data-stu-id="9f652-158">impactScore</span></span> | <span data-ttu-id="9f652-159">Double</span><span class="sxs-lookup"><span data-stu-id="9f652-159">Double</span></span> | <span data-ttu-id="9f652-160">Impact du score d’exposition de ce logiciel</span><span class="sxs-lookup"><span data-stu-id="9f652-160">Exposure score impact of this software</span></span>
