---
title: API de réponse Microsoft Defender - Protection avancée contre les menaces prise en charge
description: Découvrez les appels d’API Microsoft Defender - Protection avancée contre les menaces spécifiques liés à la réponse.
keywords: api de réponse, api de graphique, api pris en charge, acteur, alertes, appareil, utilisateur, domaine, ip, fichier
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.openlocfilehash: a290c431f6d81b23896ddf77e7c7a47de378de22
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185550"
---
# <a name="supported-microsoft-defender-for-endpoint-query-apis"></a><span data-ttu-id="9b76e-104">API de requête Microsoft Defender pour point de terminaison prise en charge</span><span class="sxs-lookup"><span data-stu-id="9b76e-104">Supported Microsoft Defender for Endpoint query APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="9b76e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9b76e-105">**Applies to:**</span></span>
- [<span data-ttu-id="9b76e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9b76e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

> [!TIP]
> <span data-ttu-id="9b76e-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9b76e-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="9b76e-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9b76e-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-supported-response-apis-abovefoldlink) 

<span data-ttu-id="9b76e-109">Découvrez les appels d’API liés à la réponse pris en charge que vous pouvez exécuter, ainsi que des détails tels que les en-têtes de requête requis et la réponse attendue des appels.</span><span class="sxs-lookup"><span data-stu-id="9b76e-109">Learn about the supported response-related API calls you can run and details such as the required request headers, and expected response from the calls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b76e-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9b76e-110">In this section</span></span>
<span data-ttu-id="9b76e-111">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9b76e-111">Topic</span></span> | <span data-ttu-id="9b76e-112">Description</span><span class="sxs-lookup"><span data-stu-id="9b76e-112">Description</span></span>
:---|:---
<span data-ttu-id="9b76e-113">Collecter le package d’examen</span><span class="sxs-lookup"><span data-stu-id="9b76e-113">Collect investigation package</span></span> | <span data-ttu-id="9b76e-114">Exécutez cette API pour collecter un package d’enquête à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="9b76e-114">Run this API to collect an investigation package from a device.</span></span>
<span data-ttu-id="9b76e-115">Isoler l’appareil</span><span class="sxs-lookup"><span data-stu-id="9b76e-115">Isolate device</span></span> | <span data-ttu-id="9b76e-116">Exécutez cette API pour isoler un appareil du réseau.</span><span class="sxs-lookup"><span data-stu-id="9b76e-116">Run this API to isolate a device from the network.</span></span>
<span data-ttu-id="9b76e-117">Appareil unisolate</span><span class="sxs-lookup"><span data-stu-id="9b76e-117">Unisolate device</span></span> | <span data-ttu-id="9b76e-118">Supprimez un appareil de l’isolation.</span><span class="sxs-lookup"><span data-stu-id="9b76e-118">Remove a device from isolation.</span></span> 
<span data-ttu-id="9b76e-119">Restreindre l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="9b76e-119">Restrict code execution</span></span> | <span data-ttu-id="9b76e-120">Exécutez cette API pour contenir une attaque en arrêtant les processus malveillants.</span><span class="sxs-lookup"><span data-stu-id="9b76e-120">Run this API to contain an attack by stopping malicious processes.</span></span> <span data-ttu-id="9b76e-121">Vous pouvez également verrouiller un appareil et empêcher toute tentative ultérieure d’exécution de programmes potentiellement malveillants.</span><span class="sxs-lookup"><span data-stu-id="9b76e-121">You can also lock down a device and prevent subsequent attempts of potentially malicious programs from running.</span></span>
<span data-ttu-id="9b76e-122">Exécution de code de groupe</span><span class="sxs-lookup"><span data-stu-id="9b76e-122">Unrestrict code execution</span></span> | <span data-ttu-id="9b76e-123">Exécutez cette vérification pour annuler la restriction de la stratégie d’applications après avoir vérifié que l’appareil compromis a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="9b76e-123">Run this to reverse the restriction of applications policy after you have verified that the compromised device has been remediated.</span></span>
<span data-ttu-id="9b76e-124">Exécuter une analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="9b76e-124">Run antivirus scan</span></span> | <span data-ttu-id="9b76e-125">Lancez à distance une analyse antivirus pour identifier et corriger les programmes malveillants qui peuvent être présents sur un appareil compromis.</span><span class="sxs-lookup"><span data-stu-id="9b76e-125">Remotely initiate an antivirus scan to help identify and remediate malware that might be present on a compromised device.</span></span>
<span data-ttu-id="9b76e-126">Arrêter et mettre en quarantaine le fichier</span><span class="sxs-lookup"><span data-stu-id="9b76e-126">Stop and quarantine file</span></span> |  <span data-ttu-id="9b76e-127">Exécutez cet appel pour arrêter l’exécution des processus, mettre en quarantaine les fichiers et supprimer la persistance telle que les clés de Registre.</span><span class="sxs-lookup"><span data-stu-id="9b76e-127">Run this call to stop running processes, quarantine  files, and delete persistency such as registry keys.</span></span>
<span data-ttu-id="9b76e-128">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="9b76e-128">Request sample</span></span> | <span data-ttu-id="9b76e-129">Exécutez cet appel pour demander un exemple de fichier à partir d’un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="9b76e-129">Run this call to request a sample of a file from a specific device.</span></span> <span data-ttu-id="9b76e-130">Le fichier est collecté à partir de l’appareil et chargé dans un stockage sécurisé.</span><span class="sxs-lookup"><span data-stu-id="9b76e-130">The file will be collected from the device and uploaded to a secure storage.</span></span>
<span data-ttu-id="9b76e-131">Bloquer un fichier</span><span class="sxs-lookup"><span data-stu-id="9b76e-131">Block file</span></span> | <span data-ttu-id="9b76e-132">Exécutez cette API pour empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="9b76e-132">Run this API to prevent further propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> 
<span data-ttu-id="9b76e-133">Débloquer le fichier</span><span class="sxs-lookup"><span data-stu-id="9b76e-133">Unblock file</span></span> | <span data-ttu-id="9b76e-134">Autoriser l’exécuter dans l’organisation à l’aide de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="9b76e-134">Allow a file run in the organization using Microsoft Defender Antivirus.</span></span>
<span data-ttu-id="9b76e-135">Obtenir l’URI SAS du package</span><span class="sxs-lookup"><span data-stu-id="9b76e-135">Get package SAS URI</span></span> | <span data-ttu-id="9b76e-136">Exécutez cette API pour obtenir un URI qui permet de télécharger un package d’enquête.</span><span class="sxs-lookup"><span data-stu-id="9b76e-136">Run this API to get a URI that allows downloading an investigation package.</span></span>
<span data-ttu-id="9b76e-137">Obtenir un objet MachineAction</span><span class="sxs-lookup"><span data-stu-id="9b76e-137">Get MachineAction object</span></span> | <span data-ttu-id="9b76e-138">Exécutez cette API pour obtenir l’objet MachineAction.</span><span class="sxs-lookup"><span data-stu-id="9b76e-138">Run this API to get MachineAction object.</span></span>
<span data-ttu-id="9b76e-139">Obtenir la collection MachineActions</span><span class="sxs-lookup"><span data-stu-id="9b76e-139">Get MachineActions collection</span></span> | <span data-ttu-id="9b76e-140">Exécutez cette action pour obtenir la collection MachineAction.</span><span class="sxs-lookup"><span data-stu-id="9b76e-140">Run this to get MachineAction collection.</span></span>
<span data-ttu-id="9b76e-141">Obtenir une collection FileActions</span><span class="sxs-lookup"><span data-stu-id="9b76e-141">Get FileActions collection</span></span> | <span data-ttu-id="9b76e-142">Exécutez cette API pour obtenir la collection FileActions.</span><span class="sxs-lookup"><span data-stu-id="9b76e-142">Run this API to get FileActions collection.</span></span>
<span data-ttu-id="9b76e-143">Obtenir un objet FileMachineAction</span><span class="sxs-lookup"><span data-stu-id="9b76e-143">Get FileMachineAction object</span></span> | <span data-ttu-id="9b76e-144">Exécutez cette API pour obtenir l’objet FileMachineAction.</span><span class="sxs-lookup"><span data-stu-id="9b76e-144">Run this API to get FileMachineAction object.</span></span>
<span data-ttu-id="9b76e-145">Obtenir une collection FileMachineActions</span><span class="sxs-lookup"><span data-stu-id="9b76e-145">Get FileMachineActions collection</span></span> | <span data-ttu-id="9b76e-146">Exécutez cette API pour obtenir la collection FileMachineAction.</span><span class="sxs-lookup"><span data-stu-id="9b76e-146">Run this API to get FileMachineAction collection.</span></span>
