---
title: Corriger les capteurs défectueux dans Microsoft Defender pour le point de terminaison
description: Corrigez les capteurs d'appareil qui indiquent qu'ils sont mal configurés ou inactifs afin que le service reçoie les données de l'appareil.
keywords: mal configuré, inactif, corriger le capteur, l'état du capteur, aucune donnée de capteur, données du capteur, communications altérées, communication
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.date: 11/06/2020
ms.technology: mde
ms.openlocfilehash: c4cdc80170b49a111f476d2d17222c41e2b5c55f
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935364"
---
# <a name="fix-unhealthy-sensors-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="0f9f1-104">Corriger les capteurs défectueux dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f9f1-104">Fix unhealthy sensors in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="0f9f1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0f9f1-105">**Applies to:**</span></span>
- [<span data-ttu-id="0f9f1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f9f1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="0f9f1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0f9f1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

- <span data-ttu-id="0f9f1-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0f9f1-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="0f9f1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-fixsensor-abovefoldlink)

<span data-ttu-id="0f9f1-110">Les appareils classés comme étant mal configurés ou inactifs peuvent être signalés en raison de différentes causes.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-110">Devices that are categorized as misconfigured or inactive can be flagged due to varying causes.</span></span> <span data-ttu-id="0f9f1-111">Cette section fournit des explications sur ce qui peut avoir entraîné la catégorisation d'un appareil comme inactif ou mal configuré.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-111">This section provides some explanations as to what might have caused a device to be categorized as inactive or misconfigured.</span></span>

## <a name="inactive-devices"></a><span data-ttu-id="0f9f1-112">Appareils inactifs</span><span class="sxs-lookup"><span data-stu-id="0f9f1-112">Inactive devices</span></span>

<span data-ttu-id="0f9f1-113">Un appareil inactif n'est pas nécessairement signalé en raison d'un problème.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-113">An inactive device is not necessarily flagged due to an issue.</span></span> <span data-ttu-id="0f9f1-114">Les actions suivantes sur un appareil peuvent entraîner la catégorisation d'un appareil comme inactif :</span><span class="sxs-lookup"><span data-stu-id="0f9f1-114">The following actions taken on a device can cause a device to be categorized as inactive:</span></span>

### <a name="device-is-not-in-use"></a><span data-ttu-id="0f9f1-115">L'appareil n'est pas en cours d'utilisation</span><span class="sxs-lookup"><span data-stu-id="0f9f1-115">Device is not in use</span></span>

<span data-ttu-id="0f9f1-116">Si l'appareil n'a pas été utilisé pendant plus de sept jours pour une raison quelconque, il reste dans l'état « Inactif » dans le portail.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-116">If the device has not been in use for more than seven days for any reason, it will remain in an ‘Inactive’ status in the portal.</span></span>

### <a name="device-was-reinstalled-or-renamed"></a><span data-ttu-id="0f9f1-117">L'appareil a été réinstallé ou renommé</span><span class="sxs-lookup"><span data-stu-id="0f9f1-117">Device was reinstalled or renamed</span></span>
<span data-ttu-id="0f9f1-118">Un appareil réinstallé ou renommé génère une nouvelle entité d'appareil dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-118">A reinstalled or renamed device will generate a new device entity in Microsoft Defender Security Center.</span></span> <span data-ttu-id="0f9f1-119">L'entité d'appareil précédente restera avec l'état « Inactif » dans le portail.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-119">The previous device entity will remain with an ‘Inactive’ status in the portal.</span></span> <span data-ttu-id="0f9f1-120">Si vous avez réinstallé un appareil et déployé le package Defender for Endpoint, recherchez le nouveau nom de l'appareil pour vérifier que l'appareil envoie des rapports normalement.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-120">If you reinstalled a device and deployed the Defender for Endpoint package, search for the new device name to verify that the device is reporting normally.</span></span>

### <a name="device-was-offboarded"></a><span data-ttu-id="0f9f1-121">L'appareil a été offboarded</span><span class="sxs-lookup"><span data-stu-id="0f9f1-121">Device was offboarded</span></span>
<span data-ttu-id="0f9f1-122">Si l'appareil a été offboarded, il apparaîtra toujours dans la liste des appareils.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-122">If the device was offboarded, it will still appear in devices list.</span></span> <span data-ttu-id="0f9f1-123">Au bout de sept jours, l'état d'état de l'appareil doit être inactif.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-123">After seven days, the device health state should change to inactive.</span></span>

### <a name="device-is-not-sending-signals"></a><span data-ttu-id="0f9f1-124">L'appareil n'envoie pas de signaux</span><span class="sxs-lookup"><span data-stu-id="0f9f1-124">Device is not sending signals</span></span>
<span data-ttu-id="0f9f1-125">Si l'appareil n'envoie aucun signal pendant plus de sept jours à l'un des canaux Microsoft Defender for Endpoint pour une raison quelconque, y compris des conditions qui tombent sous une classification d'appareils mal configurée, un appareil peut être considéré comme inactif.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-125">If the device is not sending any signals for more than seven days to any of the Microsoft Defender for Endpoint channels for any reason including conditions that fall under misconfigured devices classification, a device can be considered inactive.</span></span> 

<span data-ttu-id="0f9f1-126">Attendez-vous à ce qu'un appareil soit à l'état « Actif » ?</span><span class="sxs-lookup"><span data-stu-id="0f9f1-126">Do you expect a device to be in ‘Active’ status?</span></span> <span data-ttu-id="0f9f1-127">[Ouvrez un ticket de support.](https://support.microsoft.com/getsupport?wf=0&tenant=ClassicCommercial&oaspworkflow=start_1.0.0.0&locale=en-us&supportregion=en-us&pesid=16055&ccsid=636206786382823561)</span><span class="sxs-lookup"><span data-stu-id="0f9f1-127">[Open a support ticket](https://support.microsoft.com/getsupport?wf=0&tenant=ClassicCommercial&oaspworkflow=start_1.0.0.0&locale=en-us&supportregion=en-us&pesid=16055&ccsid=636206786382823561).</span></span>

## <a name="misconfigured-devices"></a><span data-ttu-id="0f9f1-128">Appareils mal configurés</span><span class="sxs-lookup"><span data-stu-id="0f9f1-128">Misconfigured devices</span></span>
<span data-ttu-id="0f9f1-129">Les appareils mal configurés peuvent également être classés sur :</span><span class="sxs-lookup"><span data-stu-id="0f9f1-129">Misconfigured devices can further be classified to:</span></span>
- <span data-ttu-id="0f9f1-130">Communications compromises</span><span class="sxs-lookup"><span data-stu-id="0f9f1-130">Impaired communications</span></span>
- <span data-ttu-id="0f9f1-131">Aucune donnée de capteur</span><span class="sxs-lookup"><span data-stu-id="0f9f1-131">No sensor data</span></span>

### <a name="impaired-communications"></a><span data-ttu-id="0f9f1-132">Communications compromises</span><span class="sxs-lookup"><span data-stu-id="0f9f1-132">Impaired communications</span></span>
<span data-ttu-id="0f9f1-133">Cet état indique qu'il existe une communication limitée entre l'appareil et le service.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-133">This status indicates that there's limited communication between the device and the service.</span></span>

<span data-ttu-id="0f9f1-134">Les suggestions d'actions suivantes peuvent aider à résoudre les problèmes liés à un appareil mal configuré avec des communications mal configurées :</span><span class="sxs-lookup"><span data-stu-id="0f9f1-134">The following suggested actions can help fix issues related to a misconfigured device with impaired communications:</span></span>

- [<span data-ttu-id="0f9f1-135">Vérifier que l'appareil dispose d'une connexion Internet</span><span class="sxs-lookup"><span data-stu-id="0f9f1-135">Ensure the device has Internet connection</span></span>](troubleshoot-onboarding.md#troubleshoot-onboarding-issues-on-the-device)</br>
  <span data-ttu-id="0f9f1-136">Le capteur Microsoft Defender pour point de terminaison requiert Microsoft Windows HTTP (WinHTTP) pour signaler les données du capteur et communiquer avec le service Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-136">The Microsoft Defender for Endpoint sensor requires Microsoft Windows HTTP (WinHTTP) to report sensor data and communicate with the Microsoft Defender for Endpoint service.</span></span>

- [<span data-ttu-id="0f9f1-137">Vérifier la connectivité du client aux URL du service Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f9f1-137">Verify client connectivity to Microsoft Defender for Endpoint service URLs</span></span>](configure-proxy-internet.md#verify-client-connectivity-to-microsoft-defender-for-endpoint-service-urls)</br>
  <span data-ttu-id="0f9f1-138">Vérifiez que la configuration du proxy s'est correctement terminée, que WinHTTP peut découvrir et communiquer via le serveur proxy dans votre environnement, et que le serveur proxy autorise le trafic vers les URL du service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-138">Verify the proxy configuration completed successfully, that WinHTTP can discover and communicate through the proxy server in your environment, and that the proxy server allows traffic to the Microsoft Defender for Endpoint service URLs.</span></span>

<span data-ttu-id="0f9f1-139">Si vous avez pris des mesures correctives et que l'état de l'appareil est toujours mal configuré, [ouvrez un ticket de support.](https://go.microsoft.com/fwlink/?LinkID=761093&clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="0f9f1-139">If you took corrective actions and the device status is still misconfigured, [open a support ticket](https://go.microsoft.com/fwlink/?LinkID=761093&clcid=0x409).</span></span>

### <a name="no-sensor-data"></a><span data-ttu-id="0f9f1-140">Aucune donnée de capteur</span><span class="sxs-lookup"><span data-stu-id="0f9f1-140">No sensor data</span></span>
<span data-ttu-id="0f9f1-141">Un appareil mal configuré avec l'état « Aucune donnée de capteur » a une communication avec le service, mais ne peut signaler que des données de capteur partielles.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-141">A misconfigured device with status ‘No sensor data’ has communication with the service but can only report partial sensor data.</span></span>
<span data-ttu-id="0f9f1-142">Suivez ces actions pour corriger les problèmes connus liés à un appareil mal configuré avec l'état « Aucune donnée de capteur » :</span><span class="sxs-lookup"><span data-stu-id="0f9f1-142">Follow theses actions to correct known issues related to a misconfigured device with status ‘No sensor data’:</span></span>

- [<span data-ttu-id="0f9f1-143">Vérifier que l'appareil dispose d'une connexion Internet</span><span class="sxs-lookup"><span data-stu-id="0f9f1-143">Ensure the device has Internet connection</span></span>](troubleshoot-onboarding.md#troubleshoot-onboarding-issues-on-the-device)</br>
  <span data-ttu-id="0f9f1-144">Le capteur Microsoft Defender pour point de terminaison requiert Microsoft Windows HTTP (WinHTTP) pour signaler les données du capteur et communiquer avec le service Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-144">The Microsoft Defender for Endpoint sensor requires Microsoft Windows HTTP (WinHTTP) to report sensor data and communicate with the Microsoft Defender for Endpoint service.</span></span>

- [<span data-ttu-id="0f9f1-145">Vérifier la connectivité du client aux URL du service Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f9f1-145">Verify client connectivity to Microsoft Defender for Endpoint service URLs</span></span>](configure-proxy-internet.md#verify-client-connectivity-to-microsoft-defender-for-endpoint-service-urls)</br>
  <span data-ttu-id="0f9f1-146">Vérifiez que la configuration du proxy s'est correctement terminée, que WinHTTP peut découvrir et communiquer via le serveur proxy dans votre environnement, et que le serveur proxy autorise le trafic vers les URL du service Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-146">Verify the proxy configuration completed successfully, that WinHTTP can discover and communicate through the proxy server in your environment, and that the proxy server allows traffic to the Microsoft Defender for Endpoint service URLs.</span></span>

- [<span data-ttu-id="0f9f1-147">Vérifier que le service de données de diagnostic est activé</span><span class="sxs-lookup"><span data-stu-id="0f9f1-147">Ensure the diagnostic data service is enabled</span></span>](troubleshoot-onboarding.md#ensure-the-diagnostics-service-is-enabled)</br>
<span data-ttu-id="0f9f1-148">Si les appareils ne sont pas correctement signalés, vous devrez peut-être vérifier que le service de données de diagnostic Windows 10 est automatiquement démarrer et s'exécute sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-148">If the devices aren't reporting correctly, you might need to check that the Windows 10 diagnostic data service is set to automatically start and is running on the endpoint.</span></span>

- [<span data-ttu-id="0f9f1-149">S'assurer que l'Antivirus Microsoft Defender n'est pas désactivé par la stratégie</span><span class="sxs-lookup"><span data-stu-id="0f9f1-149">Ensure that Microsoft Defender Antivirus is not disabled by policy</span></span>](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)</br>
<span data-ttu-id="0f9f1-150">Si vos appareils exécutent un client de logiciel anti-programme malveillant tiers, l'agent Defender pour Endpoint a besoin du pilote ELAM (Logiciel anti-programme malveillant à lancement rapide) de l'Antivirus Microsoft Defender pour être activé.</span><span class="sxs-lookup"><span data-stu-id="0f9f1-150">If your devices are running a third-party antimalware client, the Defender for Endpoint agent needs the Microsoft Defender Antivirus Early Launch Antimalware (ELAM) driver to be enabled.</span></span>

<span data-ttu-id="0f9f1-151">Si vous avez pris des mesures correctives et que l'état de l'appareil est toujours mal configuré, [ouvrez un ticket de support.](https://go.microsoft.com/fwlink/?LinkID=761093&clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="0f9f1-151">If you took corrective actions and the device status is still misconfigured, [open a support ticket](https://go.microsoft.com/fwlink/?LinkID=761093&clcid=0x409).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f9f1-152">Articles associés</span><span class="sxs-lookup"><span data-stu-id="0f9f1-152">See also</span></span>
- [<span data-ttu-id="0f9f1-153">Vérifier l'état d'état du capteur dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="0f9f1-153">Check sensor health state in Microsoft Defender for Endpoint</span></span>](check-sensor-status.md)
