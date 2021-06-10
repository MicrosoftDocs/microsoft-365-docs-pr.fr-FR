---
title: Méthodes et propriétés du logiciel
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 14291cbbba2272d268a8e79b6df7bd87992885db
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771400"
---
# <a name="software-resource-type"></a><span data-ttu-id="25a34-104">Type de ressource logicielle</span><span class="sxs-lookup"><span data-stu-id="25a34-104">Software resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="25a34-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="25a34-105">**Applies to:**</span></span>
- [<span data-ttu-id="25a34-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="25a34-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="25a34-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="25a34-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="25a34-108">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="25a34-108">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="25a34-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="25a34-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="25a34-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="25a34-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="methods"></a><span data-ttu-id="25a34-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="25a34-111">Methods</span></span>

<span data-ttu-id="25a34-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="25a34-112">Method</span></span> |<span data-ttu-id="25a34-113">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="25a34-113">Return Type</span></span> |<span data-ttu-id="25a34-114">Description</span><span class="sxs-lookup"><span data-stu-id="25a34-114">Description</span></span>
:---|:---|:---
[<span data-ttu-id="25a34-115">Répertorier les logiciels</span><span class="sxs-lookup"><span data-stu-id="25a34-115">List software</span></span>](get-software.md) | <span data-ttu-id="25a34-116">Collection de logiciels</span><span class="sxs-lookup"><span data-stu-id="25a34-116">Software collection</span></span> | <span data-ttu-id="25a34-117">Liste de l’inventaire logiciel de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="25a34-117">List the organizational software inventory.</span></span>
[<span data-ttu-id="25a34-118">Obtenir un logiciel par ID</span><span class="sxs-lookup"><span data-stu-id="25a34-118">Get software by Id</span></span>](get-software-by-id.md) | <span data-ttu-id="25a34-119">Logiciels</span><span class="sxs-lookup"><span data-stu-id="25a34-119">Software</span></span> | <span data-ttu-id="25a34-120">Obtenez un logiciel spécifique par son ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="25a34-120">Get a specific software by its software ID.</span></span>
[<span data-ttu-id="25a34-121">Répertorier la distribution de versions du logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-121">List software version distribution</span></span>](get-software-ver-distribution.md)| <span data-ttu-id="25a34-122">Collection de distribution</span><span class="sxs-lookup"><span data-stu-id="25a34-122">Distribution collection</span></span> | <span data-ttu-id="25a34-123">Liste de la distribution des versions des logiciels par ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="25a34-123">List software version distribution by software ID.</span></span>
[<span data-ttu-id="25a34-124">Répertorier les ordinateurs par logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-124">List machines by software</span></span>](get-machines-by-software.md)| <span data-ttu-id="25a34-125">Collection MachineRef</span><span class="sxs-lookup"><span data-stu-id="25a34-125">MachineRef collection</span></span> | <span data-ttu-id="25a34-126">Récupérez la liste des appareils associés à l’ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="25a34-126">Retrieve a list of devices that are associated with the software ID.</span></span>
[<span data-ttu-id="25a34-127">Répertorier les vulnérabilités par logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-127">List vulnerabilities by software</span></span>](get-vuln-by-software.md) | <span data-ttu-id="25a34-128">[Collection de vulnérabilités](vulnerability.md)</span><span class="sxs-lookup"><span data-stu-id="25a34-128">[Vulnerability](vulnerability.md) collection</span></span> | <span data-ttu-id="25a34-129">Récupérez la liste des vulnérabilités associées à l’ID logiciel.</span><span class="sxs-lookup"><span data-stu-id="25a34-129">Retrieve a list of vulnerabilities associated with the software ID.</span></span>
[<span data-ttu-id="25a34-130">Obtenir des Ko manquants</span><span class="sxs-lookup"><span data-stu-id="25a34-130">Get missing KBs</span></span>](get-missing-kbs-software.md) | <span data-ttu-id="25a34-131">Collection KB</span><span class="sxs-lookup"><span data-stu-id="25a34-131">KB collection</span></span> | <span data-ttu-id="25a34-132">Obtenir la liste des ko manquants associés à l’ID logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-132">Get a list of missing KBs associated with the software ID</span></span>

## <a name="properties"></a><span data-ttu-id="25a34-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="25a34-133">Properties</span></span>

<span data-ttu-id="25a34-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="25a34-134">Property</span></span> |   <span data-ttu-id="25a34-135">Type</span><span class="sxs-lookup"><span data-stu-id="25a34-135">Type</span></span>   |   <span data-ttu-id="25a34-136">Description</span><span class="sxs-lookup"><span data-stu-id="25a34-136">Description</span></span>
:---|:---|:---
<span data-ttu-id="25a34-137">id</span><span class="sxs-lookup"><span data-stu-id="25a34-137">id</span></span> | <span data-ttu-id="25a34-138">String</span><span class="sxs-lookup"><span data-stu-id="25a34-138">String</span></span> | <span data-ttu-id="25a34-139">ID logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-139">Software ID</span></span>
<span data-ttu-id="25a34-140">Nom</span><span class="sxs-lookup"><span data-stu-id="25a34-140">Name</span></span> | <span data-ttu-id="25a34-141">String</span><span class="sxs-lookup"><span data-stu-id="25a34-141">String</span></span> | <span data-ttu-id="25a34-142">Nom du logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-142">Software name</span></span>
<span data-ttu-id="25a34-143">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="25a34-143">Vendor</span></span> | <span data-ttu-id="25a34-144">String</span><span class="sxs-lookup"><span data-stu-id="25a34-144">String</span></span> | <span data-ttu-id="25a34-145">Nom du fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="25a34-145">Software vendor name</span></span>
<span data-ttu-id="25a34-146">Faiblesses</span><span class="sxs-lookup"><span data-stu-id="25a34-146">Weaknesses</span></span> | <span data-ttu-id="25a34-147">Entier long</span><span class="sxs-lookup"><span data-stu-id="25a34-147">Long</span></span> | <span data-ttu-id="25a34-148">Nombre de vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="25a34-148">Number of discovered vulnerabilities</span></span>
<span data-ttu-id="25a34-149">publicExploit</span><span class="sxs-lookup"><span data-stu-id="25a34-149">publicExploit</span></span> | <span data-ttu-id="25a34-150">Booléen</span><span class="sxs-lookup"><span data-stu-id="25a34-150">Boolean</span></span> | <span data-ttu-id="25a34-151">Une exploitation publique existe pour certaines vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="25a34-151">Public exploit exists for some of the vulnerabilities</span></span>
<span data-ttu-id="25a34-152">activeAlert</span><span class="sxs-lookup"><span data-stu-id="25a34-152">activeAlert</span></span> | <span data-ttu-id="25a34-153">Booléen</span><span class="sxs-lookup"><span data-stu-id="25a34-153">Boolean</span></span> | <span data-ttu-id="25a34-154">L’alerte active est associée à ce logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-154">Active alert is associated with this software</span></span>
<span data-ttu-id="25a34-155">exposedMachines</span><span class="sxs-lookup"><span data-stu-id="25a34-155">exposedMachines</span></span> | <span data-ttu-id="25a34-156">Entier long</span><span class="sxs-lookup"><span data-stu-id="25a34-156">Long</span></span> | <span data-ttu-id="25a34-157">Nombre d’appareils exposés</span><span class="sxs-lookup"><span data-stu-id="25a34-157">Number of exposed devices</span></span>
<span data-ttu-id="25a34-158">impactScore</span><span class="sxs-lookup"><span data-stu-id="25a34-158">impactScore</span></span> | <span data-ttu-id="25a34-159">Double</span><span class="sxs-lookup"><span data-stu-id="25a34-159">Double</span></span> | <span data-ttu-id="25a34-160">Impact du score d’exposition de ce logiciel</span><span class="sxs-lookup"><span data-stu-id="25a34-160">Exposure score impact of this software</span></span>
