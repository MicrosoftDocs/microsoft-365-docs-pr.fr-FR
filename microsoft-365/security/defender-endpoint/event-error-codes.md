---
title: Passer en revue les événements et les erreurs à l'aide de l'Observateur d'événements
description: Obtenez des descriptions et d'autres étapes de dépannage (si nécessaire) pour tous les événements signalés par le service Microsoft Defender for Endpoint.
keywords: résoudre les problèmes, observateur d'événements, résumé du journal, code d'échec, échec, service Microsoft Defender pour point de terminaison, ne peut pas démarrer, rompu, ne peut pas démarrer
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
ms.date: 05/21/2018
ms.technology: mde
ms.openlocfilehash: a8b7268e89470a85a34015967b69abb1818fe64f
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933840"
---
# <a name="review-events-and-errors-using-event-viewer"></a><span data-ttu-id="e1e32-104">Passer en revue les événements et les erreurs à l'aide de l'Observateur d'événements</span><span class="sxs-lookup"><span data-stu-id="e1e32-104">Review events and errors using Event Viewer</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="e1e32-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e1e32-105">**Applies to:**</span></span>
- <span data-ttu-id="e1e32-106">Observateur d'événements</span><span class="sxs-lookup"><span data-stu-id="e1e32-106">Event Viewer</span></span>
- [<span data-ttu-id="e1e32-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e1e32-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="e1e32-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e1e32-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="e1e32-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e1e32-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e1e32-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)

<span data-ttu-id="e1e32-111">Vous pouvez passer en revue les ID d'événement dans [l'Observateur d'événements](https://msdn.microsoft.com/library/aa745633(v=bts.10).aspx) sur des appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="e1e32-111">You can review event IDs in the [Event Viewer](https://msdn.microsoft.com/library/aa745633(v=bts.10).aspx) on individual devices.</span></span>

<span data-ttu-id="e1e32-112">Par exemple, si les appareils n'apparaissent pas dans la liste **Appareils,** vous devrez peut-être rechercher des ID d'événement sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="e1e32-112">For example, if devices aren't appearing in the **Devices list**, you might need to look for event IDs on the devices.</span></span> <span data-ttu-id="e1e32-113">Vous pouvez ensuite utiliser ce tableau pour déterminer d'autres étapes de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-113">You can then use this table to determine further troubleshooting steps.</span></span>

<span data-ttu-id="e1e32-114">**Ouvrez l'Observateur d'événements et recherchez le journal des événements du service Microsoft Defender for Endpoint :**</span><span class="sxs-lookup"><span data-stu-id="e1e32-114">**Open Event Viewer and find the Microsoft Defender for Endpoint service event log:**</span></span>

1. <span data-ttu-id="e1e32-115">Cliquez **sur Démarrer** dans le menu Windows, tapez Observateur **d'événements,** puis appuyez sur **Entrée.**</span><span class="sxs-lookup"><span data-stu-id="e1e32-115">Click **Start** on the Windows menu, type **Event Viewer**, and press **Enter**.</span></span>

2. <span data-ttu-id="e1e32-116">Dans la liste des journaux, sous **Résumé du journal,** faites défiler jusqu'à ce que **microsoft-Windows-SENSE/Opérationnel s'offre à vous.**</span><span class="sxs-lookup"><span data-stu-id="e1e32-116">In the log list, under **Log Summary**, scroll until you see **Microsoft-Windows-SENSE/Operational**.</span></span> <span data-ttu-id="e1e32-117">Double-cliquez sur l'élément pour ouvrir le journal.</span><span class="sxs-lookup"><span data-stu-id="e1e32-117">Double-click the item to open the log.</span></span>

   <span data-ttu-id="e1e32-118">a.</span><span class="sxs-lookup"><span data-stu-id="e1e32-118">a.</span></span>  <span data-ttu-id="e1e32-119">Vous pouvez également accéder au journal en expandant **Applications et services Journaux**  >  **Microsoft**  >  **Windows**  >  **SENSE** et en cliquant sur **Opérationnel**.</span><span class="sxs-lookup"><span data-stu-id="e1e32-119">You can also access the log by expanding **Applications and Services Logs** > **Microsoft** > **Windows** > **SENSE** and click on **Operational**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e1e32-120">SENSE est le nom interne utilisé pour faire référence au capteur comportemental qui alimente Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="e1e32-120">SENSE is the internal name used to refer to the behavioral sensor that powers Microsoft Defender for Endpoint.</span></span>

3. <span data-ttu-id="e1e32-121">Les événements enregistrés par le service apparaissent dans le journal.</span><span class="sxs-lookup"><span data-stu-id="e1e32-121">Events recorded by the service will appear in the log.</span></span> <span data-ttu-id="e1e32-122">Consultez le tableau suivant pour obtenir la liste des événements enregistrés par le service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-122">See the following table for a list of events recorded by the service.</span></span>

<table>
<tbody style="vertical-align:top;">
<tr>
<th><span data-ttu-id="e1e32-123">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="e1e32-123">Event ID</span></span></th>
<th><span data-ttu-id="e1e32-124">Message</span><span class="sxs-lookup"><span data-stu-id="e1e32-124">Message</span></span></th>
<th><span data-ttu-id="e1e32-125">Description</span><span class="sxs-lookup"><span data-stu-id="e1e32-125">Description</span></span></th>
<th><span data-ttu-id="e1e32-126">Action</span><span class="sxs-lookup"><span data-stu-id="e1e32-126">Action</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="e1e32-127">1</span><span class="sxs-lookup"><span data-stu-id="e1e32-127">1</span></span></td>
<td><span data-ttu-id="e1e32-128">Service Microsoft Defender pour point de terminaison démarré <code>variable</code> (version).</span><span class="sxs-lookup"><span data-stu-id="e1e32-128">Microsoft Defender for Endpoint service started (Version <code>variable</code>).</span></span></td>
<td><span data-ttu-id="e1e32-129">Se produit lors du démarrage, de l'arrêt et de l'intégration du système.</span><span class="sxs-lookup"><span data-stu-id="e1e32-129">Occurs during system startup, shut down, and during onboarding.</span></span></td>
<td><span data-ttu-id="e1e32-130">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-130">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-131">2</span><span class="sxs-lookup"><span data-stu-id="e1e32-131">2</span></span></td>
<td><span data-ttu-id="e1e32-132">Arrêt du service Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-132">Microsoft Defender for Endpoint service shutdown.</span></span></td>
<td><span data-ttu-id="e1e32-133">Se produit lorsque l'appareil est arrêté ou déboardé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-133">Occurs when the device is shut down or offboarded.</span></span></td>
<td><span data-ttu-id="e1e32-134">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-134">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-135">3</span><span class="sxs-lookup"><span data-stu-id="e1e32-135">3</span></span></td>
<td><span data-ttu-id="e1e32-136">Le service Microsoft Defender for Endpoint n'a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-136">Microsoft Defender for Endpoint service failed to start.</span></span> <span data-ttu-id="e1e32-137">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-137">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-138">Le service n'a pas commencé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-138">Service didn't start.</span></span></td>
<td><span data-ttu-id="e1e32-139">Examinez les autres messages pour déterminer la cause possible et les étapes de résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-139">Review other messages to determine possible cause and troubleshooting steps.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-140">4 </span><span class="sxs-lookup"><span data-stu-id="e1e32-140">4</span></span></td>
<td><span data-ttu-id="e1e32-141">Microsoft Defender for Endpoint service contacted the server at <code>variable</code> .</span><span class="sxs-lookup"><span data-stu-id="e1e32-141">Microsoft Defender for Endpoint service contacted the server at <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-142">Variable = URL des serveurs de traitement Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-142">Variable = URL of the Defender for Endpoint processing servers.</span></span><br>
<span data-ttu-id="e1e32-143">Cette URL correspond à celle qui s'est vue dans l'activité du pare-feu ou du réseau.</span><span class="sxs-lookup"><span data-stu-id="e1e32-143">This URL will match that seen in the Firewall or network activity.</span></span></td>
<td><span data-ttu-id="e1e32-144">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-144">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-145">5 </span><span class="sxs-lookup"><span data-stu-id="e1e32-145">5</span></span></td>
<td><span data-ttu-id="e1e32-146">Le service Microsoft Defender for Endpoint n'a pas réussi à se connecter au serveur à l'emplacement <code>variable</code> .</span><span class="sxs-lookup"><span data-stu-id="e1e32-146">Microsoft Defender for Endpoint service failed to connect to the server at <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-147">Variable = URL des serveurs de traitement Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-147">Variable = URL of the Defender for Endpoint processing servers.</span></span><br>
<span data-ttu-id="e1e32-148">Le service n'a pas pu contacter les serveurs de traitement externes à cette URL.</span><span class="sxs-lookup"><span data-stu-id="e1e32-148">The service couldn't contact the external processing servers at that URL.</span></span></td>
<td><span data-ttu-id="e1e32-149">Vérifiez la connexion à l'URL.</span><span class="sxs-lookup"><span data-stu-id="e1e32-149">Check the connection to the URL.</span></span> <span data-ttu-id="e1e32-150">Voir <a href="configure-proxy-internet.md" data-raw-source="[Configure proxy and Internet connectivity](configure-proxy-internet.md)">Configurer le proxy et la connectivité Internet.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-150">See <a href="configure-proxy-internet.md" data-raw-source="[Configure proxy and Internet connectivity](configure-proxy-internet.md)">Configure proxy and Internet connectivity</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-151">6 </span><span class="sxs-lookup"><span data-stu-id="e1e32-151">6</span></span></td>
<td><span data-ttu-id="e1e32-152">Le service Microsoft Defender for Endpoint n'est pas intégré et aucun paramètre d'intégration n'a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-152">Microsoft Defender for Endpoint service is not onboarded and no onboarding parameters were found.</span></span></td>
<td><span data-ttu-id="e1e32-153">L'appareil n'a pas été correctement intégré et ne sera pas signalé au portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-153">The device didn't onboard correctly and won't be reporting to the portal.</span></span></td>
<td><span data-ttu-id="e1e32-154">L'intégration doit être exécuté avant de démarrer le service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-154">Onboarding must be run before starting the service.</span></span><br>
<span data-ttu-id="e1e32-155">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-155">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-156">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-156">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-157">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-157">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-158">7 </span><span class="sxs-lookup"><span data-stu-id="e1e32-158">7</span></span></td>
<td><span data-ttu-id="e1e32-159">Le service Microsoft Defender for Endpoint n'a pas réussi à lire les paramètres d'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-159">Microsoft Defender for Endpoint service failed to read the onboarding parameters.</span></span> <span data-ttu-id="e1e32-160">Échec : <code>variable</code> .</span><span class="sxs-lookup"><span data-stu-id="e1e32-160">Failure: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-161">Variable = description détaillée de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-161">Variable = detailed error description.</span></span> <span data-ttu-id="e1e32-162">L'appareil n'a pas été correctement intégré et ne sera pas signalé au portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-162">The device didn't onboard correctly and won't be reporting to the portal.</span></span></td>
<td><span data-ttu-id="e1e32-163">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-163">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-164">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-164">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-165">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-165">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-166">8 </span><span class="sxs-lookup"><span data-stu-id="e1e32-166">8</span></span></td>
<td><span data-ttu-id="e1e32-167">Le service Microsoft Defender for Endpoint n'a pas réussi à nettoyer sa configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-167">Microsoft Defender for Endpoint service failed to clean its configuration.</span></span> <span data-ttu-id="e1e32-168">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-168">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-169"><b>Lors de l'intégration :</b> Le service n'a pas réussi à nettoyer sa configuration pendant l'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-169"><b>During onboarding:</b> The service failed to clean its configuration during the onboarding.</span></span> <span data-ttu-id="e1e32-170">Le processus d'intégration se poursuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-170">The onboarding process continues.</span></span> <br><br> <span data-ttu-id="e1e32-171"><b>Lors de laboarding :</b> Le service n'a pas réussi à nettoyer sa configuration pendant le déboardage.</span><span class="sxs-lookup"><span data-stu-id="e1e32-171"><b>During offboarding:</b> The service failed to clean its configuration during the offboarding.</span></span> <span data-ttu-id="e1e32-172">Le processus deboarding est terminé, mais le service continue de s'exécute.</span><span class="sxs-lookup"><span data-stu-id="e1e32-172">The offboarding process finished but the service keeps running.</span></span>
 </td>
<td><span data-ttu-id="e1e32-173"><b>Intégration :</b> Aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-173"><b>Onboarding:</b> No action required.</span></span> <br><br> <span data-ttu-id="e1e32-174"><b>Pare-papiers :</b> Redémarrez le système.</span><span class="sxs-lookup"><span data-stu-id="e1e32-174"><b>Offboarding:</b> Reboot the system.</span></span><br>
<span data-ttu-id="e1e32-175">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-175">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-176">9 </span><span class="sxs-lookup"><span data-stu-id="e1e32-176">9</span></span></td>
<td><span data-ttu-id="e1e32-177">Le service Microsoft Defender for Endpoint n'a pas réussi à modifier son type de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e1e32-177">Microsoft Defender for Endpoint service failed to change its start type.</span></span> <span data-ttu-id="e1e32-178">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-178">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-179"><b>Lors de l'intégration :</b> L'appareil n'a pas été correctement intégré et ne sera pas signalé au portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-179"><b>During onboarding:</b> The device didn't onboard correctly and won't be reporting to the portal.</span></span> <br><br><span data-ttu-id="e1e32-180"><b>Lors de laboarding :</b> Échec de la modification du type de démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-180"><b>During offboarding:</b> Failed to change the service start type.</span></span> <span data-ttu-id="e1e32-181">Le processus deboarding se poursuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-181">The offboarding process continues.</span></span> </td>
<td><span data-ttu-id="e1e32-182">Vérifiez que les paramètres d'intégration et les scripts ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-182">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-183">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-183">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-184">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-184">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-185">10 </span><span class="sxs-lookup"><span data-stu-id="e1e32-185">10</span></span></td>
<td><span data-ttu-id="e1e32-186">Le service Microsoft Defender for Endpoint n'a pas réussi à rendre persistantes les informations d'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-186">Microsoft Defender for Endpoint service failed to persist the onboarding information.</span></span> <span data-ttu-id="e1e32-187">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-187">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-188">L'appareil n'a pas été correctement intégré et ne sera pas signalé au portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-188">The device didn't onboard correctly and won't be reporting to the portal.</span></span></td>
<td><span data-ttu-id="e1e32-189">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-189">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-190">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-190">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-191">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-191">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-192">11</span><span class="sxs-lookup"><span data-stu-id="e1e32-192">11</span></span></td>
<td><span data-ttu-id="e1e32-193">Intégration ou ré-intégration du service Defender for Endpoint terminée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-193">Onboarding or re-onboarding of Defender for Endpoint service completed.</span></span></td>
<td><span data-ttu-id="e1e32-194">L'appareil est correctement intégré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-194">The device onboarded correctly.</span></span></td>
<td><span data-ttu-id="e1e32-195">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-195">Normal operating notification; no action required.</span></span><br>
<span data-ttu-id="e1e32-196">L'apparition de l'appareil sur le portail peut prendre plusieurs heures.</span><span class="sxs-lookup"><span data-stu-id="e1e32-196">It may take several hours for the device to appear in the portal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-197">12 </span><span class="sxs-lookup"><span data-stu-id="e1e32-197">12</span></span></td>
<td><span data-ttu-id="e1e32-198">Microsoft Defender pour le point de terminaison n'a pas réussi à appliquer la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1e32-198">Microsoft Defender for Endpoint failed to apply the default configuration.</span></span></td>
<td><span data-ttu-id="e1e32-199">Le service n'a pas pu appliquer la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1e32-199">Service was unable to apply the default configuration.</span></span></td>
<td><span data-ttu-id="e1e32-200">Cette erreur doit être résolue après un court moment.</span><span class="sxs-lookup"><span data-stu-id="e1e32-200">This error should resolve after a short period of time.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-201">13</span><span class="sxs-lookup"><span data-stu-id="e1e32-201">13</span></span></td>
<td><span data-ttu-id="e1e32-202">ID d'appareil Microsoft Defender pour point de terminaison calculé : <code>variable</code> .</span><span class="sxs-lookup"><span data-stu-id="e1e32-202">Microsoft Defender for Endpoint device ID calculated: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-203">Processus de fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="e1e32-203">Normal operating process.</span></span></td>
<td><span data-ttu-id="e1e32-204">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-204">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-205">15 </span><span class="sxs-lookup"><span data-stu-id="e1e32-205">15</span></span></td>
<td><span data-ttu-id="e1e32-206">Microsoft Defender pour le point de terminaison ne peut pas démarrer le canal de commande avec l'URL : <code>variable</code> .</span><span class="sxs-lookup"><span data-stu-id="e1e32-206">Microsoft Defender for Endpoint cannot start command channel with URL: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-207">Variable = URL des serveurs de traitement Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-207">Variable = URL of the Defender for Endpoint processing servers.</span></span><br>
<span data-ttu-id="e1e32-208">Le service n'a pas pu contacter les serveurs de traitement externes à cette URL.</span><span class="sxs-lookup"><span data-stu-id="e1e32-208">The service couldn't contact the external processing servers at that URL.</span></span></td>
<td><span data-ttu-id="e1e32-209">Vérifiez la connexion à l'URL.</span><span class="sxs-lookup"><span data-stu-id="e1e32-209">Check the connection to the URL.</span></span> <span data-ttu-id="e1e32-210">Voir <a href="configure-proxy-internet.md" data-raw-source="[Configure proxy and Internet connectivity](configure-proxy-internet.md)">Configurer le proxy et la connectivité Internet.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-210">See <a href="configure-proxy-internet.md" data-raw-source="[Configure proxy and Internet connectivity](configure-proxy-internet.md)">Configure proxy and Internet connectivity</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-211">17 </span><span class="sxs-lookup"><span data-stu-id="e1e32-211">17</span></span></td>
<td><span data-ttu-id="e1e32-212">Le service Microsoft Defender for Endpoint n'a pas réussi à modifier l'emplacement du service Expériences des utilisateurs connectés et télémétrie.</span><span class="sxs-lookup"><span data-stu-id="e1e32-212">Microsoft Defender for Endpoint service failed to change the Connected User Experiences and Telemetry service location.</span></span> <span data-ttu-id="e1e32-213">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-213">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-214">Une erreur s'est produite avec le service de télémétrie Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e32-214">An error occurred with the Windows telemetry service.</span></span></td>
<td><span data-ttu-id="e1e32-215"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Assurez-vous que le service de données de diagnostic est activé.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-215"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Ensure the diagnostic data service is enabled</a>.</span></span><br>
<span data-ttu-id="e1e32-216">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-216">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-217">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-217">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-218">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-218">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-219">18 </span><span class="sxs-lookup"><span data-stu-id="e1e32-219">18</span></span></td>
<td><span data-ttu-id="e1e32-220">OOBE (Bienvenue dans Windows) est terminé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-220">OOBE (Windows Welcome) is completed.</span></span></td>
<td><span data-ttu-id="e1e32-221">Le service démarre uniquement une fois l'installation des mises à jour Windows terminée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-221">Service will only start after any Windows updates have finished installing.</span></span></td>
<td><span data-ttu-id="e1e32-222">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-222">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-223">19</span><span class="sxs-lookup"><span data-stu-id="e1e32-223">19</span></span></td>
<td><span data-ttu-id="e1e32-224">OOBE (Bienvenue dans Windows) n'est pas encore terminé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-224">OOBE (Windows Welcome) has not yet completed.</span></span></td>
<td><span data-ttu-id="e1e32-225">Le service démarre uniquement une fois l'installation des mises à jour Windows terminée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-225">Service will only start after any Windows updates have finished installing.</span></span></td>
<td><span data-ttu-id="e1e32-226">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-226">Normal operating notification; no action required.</span></span><br>
<span data-ttu-id="e1e32-227">Si cette erreur persiste après un redémarrage du système, assurez-vous que toutes les mises à jour Windows sont entièrement installées.</span><span class="sxs-lookup"><span data-stu-id="e1e32-227">If this error persists after a system restart, ensure all Windows updates have full installed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-228">20</span><span class="sxs-lookup"><span data-stu-id="e1e32-228">20</span></span></td>
<td><span data-ttu-id="e1e32-229">Impossible d'attendre la fin de la OOBE (Bienvenue dans Windows).</span><span class="sxs-lookup"><span data-stu-id="e1e32-229">Cannot wait for OOBE (Windows Welcome) to complete.</span></span> <span data-ttu-id="e1e32-230">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-230">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-231">Erreur interne.</span><span class="sxs-lookup"><span data-stu-id="e1e32-231">Internal error.</span></span></td>
<td><span data-ttu-id="e1e32-232">Si cette erreur persiste après un redémarrage du système, assurez-vous que toutes les mises à jour Windows sont entièrement installées.</span><span class="sxs-lookup"><span data-stu-id="e1e32-232">If this error persists after a system restart, ensure all Windows updates have full installed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-233">25</span><span class="sxs-lookup"><span data-stu-id="e1e32-233">25</span></span></td>
<td><span data-ttu-id="e1e32-234">Le service Microsoft Defender for Endpoint n'a pas réussi à réinitialiser l'état d'état d'état dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="e1e32-234">Microsoft Defender for Endpoint service failed to reset health status in the registry.</span></span> <span data-ttu-id="e1e32-235">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-235">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-236">L'appareil n'a pas été correctement intégré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-236">The device didn't onboard correctly.</span></span>
<span data-ttu-id="e1e32-237">Il signale au portail, mais le service peut ne pas apparaître comme inscrit dans SCCM ou le Registre.</span><span class="sxs-lookup"><span data-stu-id="e1e32-237">It will report to the portal, however the service may not appear as registered in SCCM or the registry.</span></span></td>
<td><span data-ttu-id="e1e32-238">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-238">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-239">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-239">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-240">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-240">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-241">26</span><span class="sxs-lookup"><span data-stu-id="e1e32-241">26</span></span></td>
<td><span data-ttu-id="e1e32-242">Le service Microsoft Defender for Endpoint n'a pas réussi à définir l'état d'intégration dans le Registre.</span><span class="sxs-lookup"><span data-stu-id="e1e32-242">Microsoft Defender for Endpoint service failed to set the onboarding status in the registry.</span></span> <span data-ttu-id="e1e32-243">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-243">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-244">L'appareil n'a pas été correctement intégré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-244">The device didn't onboard correctly.</span></span><br>
<span data-ttu-id="e1e32-245">Il signale au portail, mais le service peut ne pas apparaître comme inscrit dans SCCM ou le Registre.</span><span class="sxs-lookup"><span data-stu-id="e1e32-245">It will report to the portal, however the service may not appear as registered in SCCM or the registry.</span></span></td>
<td><span data-ttu-id="e1e32-246">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-246">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-247">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-247">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-248">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-248">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-249">27</span><span class="sxs-lookup"><span data-stu-id="e1e32-249">27</span></span></td>
<td><span data-ttu-id="e1e32-250">Le service Microsoft Defender pour points de terminaison n'a pas réussi à activer le mode sensible SENSE dans l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e1e32-250">Microsoft Defender for Endpoint service failed to enable SENSE aware mode in Microsoft Defender Antivirus.</span></span> <span data-ttu-id="e1e32-251">Échec du processus d'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-251">Onboarding process failed.</span></span> <span data-ttu-id="e1e32-252">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-252">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-253">Normalement, l'Antivirus Microsoft Defender passe à un état passif spécial si un autre produit anti-programme malveillant en temps réel s'exécute correctement sur l'appareil, et que l'appareil fait des rapports à Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-253">Normally, Microsoft Defender Antivirus will enter a special passive state if another real-time antimalware product is running properly on the device, and the device is reporting to Defender for Endpoint.</span></span></td>
<td><span data-ttu-id="e1e32-254">Vérifiez que les paramètres d'intégration et les scripts ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-254">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-255">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-255">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-256">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-256">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span><br>
<span data-ttu-id="e1e32-257">Assurez-vous que la protection contre les programmes malveillants en temps réel s'exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="e1e32-257">Ensure real-time antimalware protection is running properly.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-258">28</span><span class="sxs-lookup"><span data-stu-id="e1e32-258">28</span></span></td>
<td><span data-ttu-id="e1e32-259">Échec de l'inscription au service Expériences des utilisateurs connectés et télémétrie de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e1e32-259">Microsoft Defender for Endpoint Connected User Experiences and Telemetry service registration failed.</span></span> <span data-ttu-id="e1e32-260">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-260">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-261">Une erreur s'est produite avec le service de télémétrie Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e32-261">An error occurred with the Windows telemetry service.</span></span></td>
<td><span data-ttu-id="e1e32-262"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Assurez-vous que le service de données de diagnostic est activé.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-262"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Ensure the diagnostic data service is enabled</a>.</span></span><br>
<span data-ttu-id="e1e32-263">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-263">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-264">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-264">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-265">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-265">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-266">29</span><span class="sxs-lookup"><span data-stu-id="e1e32-266">29</span></span></td>
<td><span data-ttu-id="e1e32-267">Échec de la lecture des paramètres deboarding.</span><span class="sxs-lookup"><span data-stu-id="e1e32-267">Failed to read the offboarding parameters.</span></span> <span data-ttu-id="e1e32-268">Type d'erreur : %1, Code d'erreur : %2, Description : %3</span><span class="sxs-lookup"><span data-stu-id="e1e32-268">Error type: %1, Error code: %2, Description: %3</span></span> </td>
<td><span data-ttu-id="e1e32-269">Cet événement se produit lorsque le système ne peut&#39;pas lire les paramètres de hors-carte.</span><span class="sxs-lookup"><span data-stu-id="e1e32-269">This event occurs when the system can&#39;t read the offboarding parameters.</span></span></td>
<td><span data-ttu-id="e1e32-270">Assurez-vous que l'appareil dispose d'un accès à Internet, puis exécutez à nouveau l'intégralité du processus deboarding.</span><span class="sxs-lookup"><span data-stu-id="e1e32-270">Ensure the device has Internet access, then run the entire offboarding process again.</span></span> <span data-ttu-id="e1e32-271">Assurez-vous que le package deboarding n'a pas expiré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-271">Ensure the offboarding package hasn't expired.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-272">30</span><span class="sxs-lookup"><span data-stu-id="e1e32-272">30</span></span></td>
<td><span data-ttu-id="e1e32-273">Le service Microsoft Defender pour points de terminaison n'a pas réussi à désactiver le mode sensible SENSE dans l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e1e32-273">Microsoft Defender for Endpoint service failed to disable SENSE aware mode in Microsoft Defender Antivirus.</span></span> <span data-ttu-id="e1e32-274">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-274">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-275">Normalement, l'Antivirus Microsoft Defender passe à un état passif spécial si un autre produit anti-programme malveillant en temps réel s'exécute correctement sur l'appareil, et que l'appareil fait des rapports à Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e1e32-275">Normally, Microsoft Defender Antivirus will enter a special passive state if another real-time antimalware product is running properly on the device, and the device is reporting to Defender for Endpoint.</span></span></td>
<td><span data-ttu-id="e1e32-276">Vérifiez que les paramètres et les scripts d'intégration ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-276">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-277">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-277">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-278">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-278">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a></span></span><br>
<span data-ttu-id="e1e32-279">Assurez-vous que la protection contre les programmes malveillants en temps réel s'exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="e1e32-279">Ensure real-time antimalware protection is running properly.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-280">31</span><span class="sxs-lookup"><span data-stu-id="e1e32-280">31</span></span></td>
<td><span data-ttu-id="e1e32-281">Échec de l'agrégation du service Expériences des utilisateurs connectés et télémétrie de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e1e32-281">Microsoft Defender for Endpoint Connected User Experiences and Telemetry service unregistration failed.</span></span> <span data-ttu-id="e1e32-282">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-282">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-283">Une erreur s'est produite avec le service de télémétrie Windows lors de l'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-283">An error occurred with the Windows telemetry service during onboarding.</span></span> <span data-ttu-id="e1e32-284">Le processus deboarding se poursuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-284">The offboarding process continues.</span></span></td>
<td><span data-ttu-id="e1e32-285"><a href="troubleshoot-onboarding.md#ensure-the-diagnostic-data-service-is-enabled" data-raw-source="[Check for errors with the Windows telemetry service](troubleshoot-onboarding.md#ensure-the-diagnostic-data-service-is-enabled)">Recherchez les erreurs avec le service de télémétrie Windows.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-285"><a href="troubleshoot-onboarding.md#ensure-the-diagnostic-data-service-is-enabled" data-raw-source="[Check for errors with the Windows telemetry service](troubleshoot-onboarding.md#ensure-the-diagnostic-data-service-is-enabled)">Check for errors with the Windows telemetry service</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-286">32</span><span class="sxs-lookup"><span data-stu-id="e1e32-286">32</span></span></td>
<td><span data-ttu-id="e1e32-287">Le service Microsoft Defender for Endpoint n'a pas réussi à demander à s'arrêter après le processus deboarding.</span><span class="sxs-lookup"><span data-stu-id="e1e32-287">Microsoft Defender for Endpoint service failed to request to stop itself after offboarding process.</span></span> <span data-ttu-id="e1e32-288">Code d'échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-288">Failure code: %1</span></span></td>
<td><span data-ttu-id="e1e32-289">Une erreur s'est produite lors de la procédure deboardage.</span><span class="sxs-lookup"><span data-stu-id="e1e32-289">An error occurred during offboarding.</span></span></td>
<td><span data-ttu-id="e1e32-290">Redémarrez l'appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-290">Reboot the device.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-291">33</span><span class="sxs-lookup"><span data-stu-id="e1e32-291">33</span></span></td>
<td><span data-ttu-id="e1e32-292">Le service Microsoft Defender for Endpoint n'a pas réussi à rendre persistant le GUID SENSE.</span><span class="sxs-lookup"><span data-stu-id="e1e32-292">Microsoft Defender for Endpoint service failed to persist SENSE GUID.</span></span> <span data-ttu-id="e1e32-293">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-293">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-294">Un identificateur unique est utilisé pour représenter chaque appareil signalant au portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-294">A unique identifier is used to represent each device that is reporting to the portal.</span></span><br>
<span data-ttu-id="e1e32-295">Si l'identificateur ne persiste pas, le même appareil peut apparaître deux fois dans le portail.</span><span class="sxs-lookup"><span data-stu-id="e1e32-295">If the identifier doesn't persist, the same device might appear twice in the portal.</span></span></td>
<td><span data-ttu-id="e1e32-296">Vérifiez les autorisations du Registre sur l'appareil pour vous assurer que le service peut mettre à jour le Registre.</span><span class="sxs-lookup"><span data-stu-id="e1e32-296">Check registry permissions on the device to ensure the service can update the registry.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-297">34</span><span class="sxs-lookup"><span data-stu-id="e1e32-297">34</span></span></td>
<td><span data-ttu-id="e1e32-298">Le service Microsoft Defender pour points de terminaison n'a pas réussi à s'ajouter en tant que dépendance au service Expériences des utilisateurs connectés et télémétrie, ce qui a provoqué l'échec du processus d'intégration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-298">Microsoft Defender for Endpoint service failed to add itself as a dependency on the Connected User Experiences and Telemetry service, causing onboarding process to fail.</span></span> <span data-ttu-id="e1e32-299">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-299">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-300">Une erreur s'est produite avec le service de télémétrie Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e32-300">An error occurred with the Windows telemetry service.</span></span></td>
<td><span data-ttu-id="e1e32-301"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Assurez-vous que le service de données de diagnostic est activé.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-301"><a href="troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy" data-raw-source="[Ensure the diagnostic data service is enabled](troubleshoot-onboarding.md#ensure-that-microsoft-defender-antivirus-is-not-disabled-by-a-policy)">Ensure the diagnostic data service is enabled</a>.</span></span><br>
<span data-ttu-id="e1e32-302">Vérifiez que les paramètres d'intégration et les scripts ont été correctement déployés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-302">Check that the onboarding settings and scripts were deployed properly.</span></span> <span data-ttu-id="e1e32-303">Essayez de redéployer les packages de configuration.</span><span class="sxs-lookup"><span data-stu-id="e1e32-303">Try to redeploy the configuration packages.</span></span><br>
<span data-ttu-id="e1e32-304">Voir <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Appareils Windows 10 intégrés.</a></span><span class="sxs-lookup"><span data-stu-id="e1e32-304">See <a href="configure-endpoints.md" data-raw-source="[Onboard Windows 10 devices](configure-endpoints.md)">Onboard Windows 10 devices</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-305">35</span><span class="sxs-lookup"><span data-stu-id="e1e32-305">35</span></span></td>
<td><span data-ttu-id="e1e32-306">Le service Microsoft Defender pour points de terminaison n'a pas réussi à se supprimer en tant que dépendance au service Expériences des utilisateurs connectés et télémétrie.</span><span class="sxs-lookup"><span data-stu-id="e1e32-306">Microsoft Defender for Endpoint service failed to remove itself as a dependency on the Connected User Experiences and Telemetry service.</span></span> <span data-ttu-id="e1e32-307">Code d'échec <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-307">Failure code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-308">Une erreur s'est produite avec le service de télémétrie Windows lors de la déboarding.</span><span class="sxs-lookup"><span data-stu-id="e1e32-308">An error occurred with the Windows telemetry service during offboarding.</span></span> <span data-ttu-id="e1e32-309">Le processus deboarding se poursuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-309">The offboarding process continues.</span></span>
</td>
<td><span data-ttu-id="e1e32-310">Recherchez les erreurs avec le service de données de diagnostic Windows.</span><span class="sxs-lookup"><span data-stu-id="e1e32-310">Check for errors with the Windows diagnostic data service.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-311">36</span><span class="sxs-lookup"><span data-stu-id="e1e32-311">36</span></span></td>
<td><span data-ttu-id="e1e32-312">L'inscription au service Expériences des utilisateurs connectés et télémétrie de Microsoft Defender for Endpoint a réussi.</span><span class="sxs-lookup"><span data-stu-id="e1e32-312">Microsoft Defender for Endpoint Connected User Experiences and Telemetry service registration succeeded.</span></span> <span data-ttu-id="e1e32-313">Code d'achèvement <code>variable</code> : .</span><span class="sxs-lookup"><span data-stu-id="e1e32-313">Completion code: <code>variable</code>.</span></span></td>
<td><span data-ttu-id="e1e32-314">L'inscription de Defender pour endpoint auprès du service Expériences des utilisateurs connectés et télémétrie s'est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="e1e32-314">Registering Defender for Endpoint with the Connected User Experiences and Telemetry service completed successfully.</span></span></td>
<td><span data-ttu-id="e1e32-315">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-315">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-316">37</span><span class="sxs-lookup"><span data-stu-id="e1e32-316">37</span></span></td>
<td><span data-ttu-id="e1e32-317">Microsoft Defender pour le point de terminaison A est sur le point de dépasser son quota.</span><span class="sxs-lookup"><span data-stu-id="e1e32-317">Microsoft Defender for Endpoint A module is about to exceed its quota.</span></span> <span data-ttu-id="e1e32-318">Module : %1, Quota : {%2} {%3}, Pourcentage d'utilisation du quota : %4.</span><span class="sxs-lookup"><span data-stu-id="e1e32-318">Module: %1, Quota: {%2} {%3}, Percentage of quota utilization: %4.</span></span></td>
<td><span data-ttu-id="e1e32-319">L'appareil a presque utilisé son quota alloué de la fenêtre actuelle de 24 heures.</span><span class="sxs-lookup"><span data-stu-id="e1e32-319">The device has almost used its allocated quota of the current 24-hour window.</span></span> <span data-ttu-id="e1e32-320">Il est sur le point d'être limitée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-320">It’s about to be throttled.</span></span></td>
<td><span data-ttu-id="e1e32-321">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-321">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-322">38</span><span class="sxs-lookup"><span data-stu-id="e1e32-322">38</span></span></td>
<td><span data-ttu-id="e1e32-323">La connexion réseau est identifiée comme faible.</span><span class="sxs-lookup"><span data-stu-id="e1e32-323">Network connection is identified as low.</span></span> <span data-ttu-id="e1e32-324">Microsoft Defender pour le point de terminaison contactera le serveur toutes les %1 minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-324">Microsoft Defender for Endpoint will contact the server every %1 minutes.</span></span> <span data-ttu-id="e1e32-325">Connexion avec indicateur : %2, Internet disponible : %3, réseau gratuit disponible : %4.</span><span class="sxs-lookup"><span data-stu-id="e1e32-325">Metered connection: %2, internet available: %3, free network available: %4.</span></span></td>
<td><span data-ttu-id="e1e32-326">L’appareil utilise un réseau payant/payant et contacte le serveur moins fréquemment.</span><span class="sxs-lookup"><span data-stu-id="e1e32-326">The device is using a metered/paid network and will be contacting the server less frequently.</span></span></td>
<td><span data-ttu-id="e1e32-327">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-327">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-328">39</span><span class="sxs-lookup"><span data-stu-id="e1e32-328">39</span></span></td>
<td><span data-ttu-id="e1e32-329">La connexion réseau est identifiée comme normale.</span><span class="sxs-lookup"><span data-stu-id="e1e32-329">Network connection is identified as normal.</span></span> <span data-ttu-id="e1e32-330">Microsoft Defender pour le point de terminaison contactera le serveur toutes les %1 minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-330">Microsoft Defender for Endpoint will contact the server every %1 minutes.</span></span> <span data-ttu-id="e1e32-331">Connexion avec indicateur : %2, Internet disponible : %3, réseau gratuit disponible : %4.</span><span class="sxs-lookup"><span data-stu-id="e1e32-331">Metered connection: %2, internet available: %3, free network available: %4.</span></span></td>
<td><span data-ttu-id="e1e32-332">L’appareil n’utilise pas une connexion payante/payante et contacte le serveur comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="e1e32-332">The device isn't using a metered/paid connection and will contact the server as usual.</span></span></td>
<td><span data-ttu-id="e1e32-333">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-333">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-334">40</span><span class="sxs-lookup"><span data-stu-id="e1e32-334">40</span></span></td>
<td><span data-ttu-id="e1e32-335">L’état de la batterie est identifié comme faible.</span><span class="sxs-lookup"><span data-stu-id="e1e32-335">Battery state is identified as low.</span></span> <span data-ttu-id="e1e32-336">Microsoft Defender pour le point de terminaison contactera le serveur toutes les %1 minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-336">Microsoft Defender for Endpoint will contact the server every %1 minutes.</span></span> <span data-ttu-id="e1e32-337">État de la batterie : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-337">Battery state: %2.</span></span></td>
<td><span data-ttu-id="e1e32-338">L’appareil a un niveau de batterie faible et contacte le serveur moins fréquemment.</span><span class="sxs-lookup"><span data-stu-id="e1e32-338">The device has low battery level and will contact the server less frequently.</span></span></td>
<td><span data-ttu-id="e1e32-339">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-339">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-340">41</span><span class="sxs-lookup"><span data-stu-id="e1e32-340">41</span></span></td>
<td><span data-ttu-id="e1e32-341">L’état de la batterie est identifié comme normal.</span><span class="sxs-lookup"><span data-stu-id="e1e32-341">Battery state is identified as normal.</span></span> <span data-ttu-id="e1e32-342">Microsoft Defender pour le point de terminaison contactera le serveur toutes les %1 minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-342">Microsoft Defender for Endpoint will contact the server every %1 minutes.</span></span> <span data-ttu-id="e1e32-343">État de la batterie : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-343">Battery state: %2.</span></span></td>
<td><span data-ttu-id="e1e32-344">L’appareil n’a pas un niveau de batterie faible et contacte le serveur comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="e1e32-344">The device doesn’t have low battery level and will contact the server as usual.</span></span></td>
<td><span data-ttu-id="e1e32-345">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-345">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-346">42</span><span class="sxs-lookup"><span data-stu-id="e1e32-346">42</span></span></td>
<td><span data-ttu-id="e1e32-347">Le composant Microsoft Defender pour le point de terminaison n’a pas réussi à effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="e1e32-347">Microsoft Defender for Endpoint component failed to perform action.</span></span> <span data-ttu-id="e1e32-348">Composant : %1, Action : %2, Type d’exception : %3, Message d’exception : %4</span><span class="sxs-lookup"><span data-stu-id="e1e32-348">Component: %1, Action: %2, Exception Type: %3, Exception message: %4</span></span></td>
<td><span data-ttu-id="e1e32-349">Erreur interne.</span><span class="sxs-lookup"><span data-stu-id="e1e32-349">Internal error.</span></span> <span data-ttu-id="e1e32-350">Le service n’a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-350">The service failed to start.</span></span></td>
<td><span data-ttu-id="e1e32-351">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-351">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-352">43</span><span class="sxs-lookup"><span data-stu-id="e1e32-352">43</span></span></td>
<td><span data-ttu-id="e1e32-353">Le composant Microsoft Defender pour le point de terminaison n’a pas réussi à effectuer une action.</span><span class="sxs-lookup"><span data-stu-id="e1e32-353">Microsoft Defender for Endpoint component failed to perform action.</span></span> <span data-ttu-id="e1e32-354">Composant : %1, Action : %2, Type d’exception : %3, Erreur d’exception : %4, Message d’exception : %5</span><span class="sxs-lookup"><span data-stu-id="e1e32-354">Component: %1, Action: %2, Exception Type: %3, Exception Error: %4, Exception message: %5</span></span></td>
<td><span data-ttu-id="e1e32-355">Erreur interne.</span><span class="sxs-lookup"><span data-stu-id="e1e32-355">Internal error.</span></span> <span data-ttu-id="e1e32-356">Le service n’a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-356">The service failed to start.</span></span></td>
<td><span data-ttu-id="e1e32-357">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-357">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-358">44</span><span class="sxs-lookup"><span data-stu-id="e1e32-358">44</span></span></td>
<td><span data-ttu-id="e1e32-359">Arrêt du service Defender pour point de terminaison terminé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-359">Offboarding of Defender for Endpoint service completed.</span></span></td>
<td><span data-ttu-id="e1e32-360">Le service a été offboarded.</span><span class="sxs-lookup"><span data-stu-id="e1e32-360">The service was offboarded.</span></span></td>
<td><span data-ttu-id="e1e32-361">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-361">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-362">45</span><span class="sxs-lookup"><span data-stu-id="e1e32-362">45</span></span></td>
<td><span data-ttu-id="e1e32-363">Échec de l’inscription et du démarrage de la session de suivi des événements [%1].</span><span class="sxs-lookup"><span data-stu-id="e1e32-363">Failed to register and to start the event trace session [%1].</span></span> <span data-ttu-id="e1e32-364">Code d’erreur : %2</span><span class="sxs-lookup"><span data-stu-id="e1e32-364">Error code: %2</span></span></td>
<td><span data-ttu-id="e1e32-365">Une erreur s’est produite lors du démarrage du service lors de la création d’une session ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-365">An error occurred on service startup while creating ETW session.</span></span> <span data-ttu-id="e1e32-366">Cela a provoqué l’échec du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-366">This caused service start-up failure.</span></span></td>
<td><span data-ttu-id="e1e32-367">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-367">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-368">46</span><span class="sxs-lookup"><span data-stu-id="e1e32-368">46</span></span></td>
<td><span data-ttu-id="e1e32-369">Échec de l’inscription et du démarrage de la session de suivi des événements [%1] en raison d’un manque de ressources.</span><span class="sxs-lookup"><span data-stu-id="e1e32-369">Failed to register and start the event trace session [%1] due to lack of resources.</span></span> <span data-ttu-id="e1e32-370">Code d’erreur : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-370">Error code: %2.</span></span> <span data-ttu-id="e1e32-371">Cela est très probable car il y a trop de sessions de suivi d’événements actives.</span><span class="sxs-lookup"><span data-stu-id="e1e32-371">This is most likely because there are too many active event trace sessions.</span></span> <span data-ttu-id="e1e32-372">Le service réessaye dans 1 minute.</span><span class="sxs-lookup"><span data-stu-id="e1e32-372">The service will retry in 1 minute.</span></span></td>
<td><span data-ttu-id="e1e32-373">Une erreur s’est produite lors du démarrage du service lors de la création d’une session ETW en raison d’un manque de ressources.</span><span class="sxs-lookup"><span data-stu-id="e1e32-373">An error occurred on service startup while creating ETW session due to lack of resources.</span></span> <span data-ttu-id="e1e32-374">Le service a démarré et est en cours d’exécution, mais ne signale aucun événement de capteur tant que la session ETW n’est pas démarrée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-374">The service started and is running, but won't report any sensor event until the ETW session is started.</span></span></td>
<td><span data-ttu-id="e1e32-375">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-375">Normal operating notification; no action required.</span></span> <span data-ttu-id="e1e32-376">Le service essaiera de démarrer la session toutes les minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-376">The service will try to start the session every minute.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-377">47</span><span class="sxs-lookup"><span data-stu-id="e1e32-377">47</span></span></td>
<td><span data-ttu-id="e1e32-378">Session de suivi d’événements correctement inscrite et démarrée : récupérée après les tentatives précédentes qui ont échoué.</span><span class="sxs-lookup"><span data-stu-id="e1e32-378">Successfully registered and started the event trace session - recovered after previous failed attempts.</span></span></td>
<td><span data-ttu-id="e1e32-379">Cet événement suit l’événement précédent après le démarrage réussi de la session ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-379">This event follows the previous event after successfully starting of the ETW session.</span></span></td>
<td><span data-ttu-id="e1e32-380">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-380">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e1e32-381">48</span><span class="sxs-lookup"><span data-stu-id="e1e32-381">48</span></span></td>
<td><span data-ttu-id="e1e32-382">Échec de l’ajout d’un fournisseur [%1] à la session de suivi des événements [%2].</span><span class="sxs-lookup"><span data-stu-id="e1e32-382">Failed to add a provider [%1] to event trace session [%2].</span></span> <span data-ttu-id="e1e32-383">Code d’erreur : %3.</span><span class="sxs-lookup"><span data-stu-id="e1e32-383">Error code: %3.</span></span> <span data-ttu-id="e1e32-384">Cela signifie que les événements de ce fournisseur ne seront pas signalés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-384">This means that events from this provider will not be reported.</span></span></td>
<td><span data-ttu-id="e1e32-385">Échec de l’ajout d’un fournisseur à la session ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-385">Failed to add a provider to ETW session.</span></span> <span data-ttu-id="e1e32-386">Par conséquent, les événements du fournisseur ne sont pas signalés.</span><span class="sxs-lookup"><span data-stu-id="e1e32-386">As a result, the provider events aren’t reported.</span></span></td>
<td><span data-ttu-id="e1e32-387">Vérifiez le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-387">Check the error code.</span></span> <span data-ttu-id="e1e32-388">Si l’erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-388">If the error persists contact Support.</span></span></td>
</tr>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-389">49</span><span class="sxs-lookup"><span data-stu-id="e1e32-389">49</span></span></td>
   <td><span data-ttu-id="e1e32-390">Commande de configuration cloud non valide reçue et ignorée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-390">Invalid cloud configuration command received and ignored.</span></span> <span data-ttu-id="e1e32-391">Version : %1, état : %2, code d’erreur : %3, message : %4</span><span class="sxs-lookup"><span data-stu-id="e1e32-391">Version: %1, status: %2, error code: %3, message: %4</span></span></td>
   <td><span data-ttu-id="e1e32-392">Le service cloud a reçu un fichier de configuration non valide qui a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-392">Received an invalid configuration file from the cloud service that was ignored.</span></span></td>
   <td><span data-ttu-id="e1e32-393">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-393">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-394">50</span><span class="sxs-lookup"><span data-stu-id="e1e32-394">50</span></span></td>
   <td><span data-ttu-id="e1e32-395">Nouvelle configuration cloud appliquée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1e32-395">New cloud configuration applied successfully.</span></span> <span data-ttu-id="e1e32-396">Version : %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-396">Version: %1.</span></span></td>
   <td><span data-ttu-id="e1e32-397">Application réussie d’une nouvelle configuration à partir du service cloud.</span><span class="sxs-lookup"><span data-stu-id="e1e32-397">Successfully applied a new configuration from the cloud service.</span></span></td>
   <td><span data-ttu-id="e1e32-398">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-398">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-399">51</span><span class="sxs-lookup"><span data-stu-id="e1e32-399">51</span></span></td>
   <td><span data-ttu-id="e1e32-400">La nouvelle configuration cloud n’a pas réussi à s’appliquer, version : %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-400">New cloud configuration failed to apply, version: %1.</span></span> <span data-ttu-id="e1e32-401">Application réussie de la dernière bonne configuration connue, version %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-401">Successfully applied the last known good configuration, version %2.</span></span></td>
   <td><span data-ttu-id="e1e32-402">Le service cloud a reçu un fichier de configuration non bon.</span><span class="sxs-lookup"><span data-stu-id="e1e32-402">Received a bad configuration file from the cloud service.</span></span> <span data-ttu-id="e1e32-403">La dernière bonne configuration connue a été appliquée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1e32-403">Last known good configuration was applied successfully.</span></span></td>
   <td><span data-ttu-id="e1e32-404">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-404">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-405">52</span><span class="sxs-lookup"><span data-stu-id="e1e32-405">52</span></span></td>
   <td><span data-ttu-id="e1e32-406">La nouvelle configuration cloud n’a pas réussi à s’appliquer, version : %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-406">New cloud configuration failed to apply, version: %1.</span></span> <span data-ttu-id="e1e32-407">Échec également de l’application de la dernière bonne configuration connue, version %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-407">Also failed to apply last known good configuration, version %2.</span></span> <span data-ttu-id="e1e32-408">La configuration par défaut a été correctement appliquée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-408">Successfully applied the default configuration.</span></span></td>
   <td><span data-ttu-id="e1e32-409">Le service cloud a reçu un fichier de configuration non bon.</span><span class="sxs-lookup"><span data-stu-id="e1e32-409">Received a bad configuration file from the cloud service.</span></span> <span data-ttu-id="e1e32-410">Échec de l’application de la dernière bonne configuration connue et la configuration par défaut a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="e1e32-410">Failed to apply the last known good configuration - and the default configuration was applied.</span></span></td>
   <td><span data-ttu-id="e1e32-411">Le service tentera de télécharger un nouveau fichier de configuration dans un délai de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="e1e32-411">The service will attempt to download a new configuration file within 5 minutes.</span></span> <span data-ttu-id="e1e32-412">Si l’événement n’est pas #50 - contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-412">If you don't see event #50 - contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-413">53</span><span class="sxs-lookup"><span data-stu-id="e1e32-413">53</span></span></td>
   <td><span data-ttu-id="e1e32-414">Configuration cloud chargée à partir du stockage persistant, version : %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-414">Cloud configuration loaded from persistent storage, version: %1.</span></span></td>
   <td><span data-ttu-id="e1e32-415">La configuration a été chargée à partir d’un stockage persistant au démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-415">The configuration was loaded from persistent storage on service startup.</span></span></td>
   <td><span data-ttu-id="e1e32-416">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-416">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-417">55</span><span class="sxs-lookup"><span data-stu-id="e1e32-417">55</span></span></td>
   <td><span data-ttu-id="e1e32-418">Échec de la création dulogger automatique ETW sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-418">Failed to create the Secure ETW autologger.</span></span> <span data-ttu-id="e1e32-419">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-419">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-420">Échec de la création de l’enregistreur de journaux ETW sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-420">Failed to create the secure ETW logger.</span></span></td>
   <td><span data-ttu-id="e1e32-421">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-421">Reboot the device.</span></span> <span data-ttu-id="e1e32-422">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-422">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-423">56</span><span class="sxs-lookup"><span data-stu-id="e1e32-423">56</span></span></td>
   <td><span data-ttu-id="e1e32-424">Échec de la suppression dulogger automatique ETW sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-424">Failed to remove the Secure ETW autologger.</span></span> <span data-ttu-id="e1e32-425">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-425">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-426">Échec de la suppression de la session ETW sécurisée lors du déboardage.</span><span class="sxs-lookup"><span data-stu-id="e1e32-426">Failed to remove the secure ETW session on offboarding.</span></span></td>
   <td><span data-ttu-id="e1e32-427">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-427">Contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-428">57</span><span class="sxs-lookup"><span data-stu-id="e1e32-428">57</span></span></td>
   <td><span data-ttu-id="e1e32-429">Capture d’un instantané de l’ordinateur à des fins de dépannage.</span><span class="sxs-lookup"><span data-stu-id="e1e32-429">Capturing a snapshot of the machine for troubleshooting purposes.</span></span></td>
   <td><span data-ttu-id="e1e32-430">Un package d’enquête, également appelé package d’investigation, est en cours de collecte.</span><span class="sxs-lookup"><span data-stu-id="e1e32-430">An investigation package, also known as forensics package, is being collected.</span></span></td>
   <td><span data-ttu-id="e1e32-431">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-431">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-432">59</span><span class="sxs-lookup"><span data-stu-id="e1e32-432">59</span></span></td>
   <td><span data-ttu-id="e1e32-433">Commande de démarrage : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-433">Starting command: %1</span></span></td>
   <td><span data-ttu-id="e1e32-434">Démarrage de l’exécution de la commande de réponse.</span><span class="sxs-lookup"><span data-stu-id="e1e32-434">Starting response command execution.</span></span></td>
   <td><span data-ttu-id="e1e32-435">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-435">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-436">60</span><span class="sxs-lookup"><span data-stu-id="e1e32-436">60</span></span></td>
   <td><span data-ttu-id="e1e32-437">Échec d’exécuter la commande %1, erreur : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-437">Failed to run command %1, error: %2.</span></span></td>
   <td><span data-ttu-id="e1e32-438">Échec de l’exécution de la commande de réponse.</span><span class="sxs-lookup"><span data-stu-id="e1e32-438">Failed to execute response command.</span></span></td>
   <td><span data-ttu-id="e1e32-439">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-439">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-440">61</span><span class="sxs-lookup"><span data-stu-id="e1e32-440">61</span></span></td>
   <td><span data-ttu-id="e1e32-441">Les paramètres de commande de collecte de données ne sont pas valides : SasUri : %1, compressionLevel : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-441">Data collection command parameters are invalid: SasUri: %1, compressionLevel: %2.</span></span></td>
   <td><span data-ttu-id="e1e32-442">Échec de la lecture ou de l’analyse des arguments de commande de collecte de données (arguments non valides).</span><span class="sxs-lookup"><span data-stu-id="e1e32-442">Failed to read or parse the data collection command arguments (invalid arguments).</span></span></td>
   <td><span data-ttu-id="e1e32-443">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-443">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-444">62</span><span class="sxs-lookup"><span data-stu-id="e1e32-444">62</span></span></td>
   <td><span data-ttu-id="e1e32-445">Échec du démarrage du service Expériences des utilisateurs connectés et télémétrie.</span><span class="sxs-lookup"><span data-stu-id="e1e32-445">Failed to start Connected User Experiences and Telemetry service.</span></span> <span data-ttu-id="e1e32-446">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-446">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-447">Le service Expériences des utilisateurs connectés et télémétrie (diagtrack) n’a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-447">Connected User Experiences and Telemetry (diagtrack) service failed to start.</span></span> <span data-ttu-id="e1e32-448">La télémétrie d’un point de terminaison autre que Microsoft Defender ne sera pas envoyée à partir de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-448">Non-Microsoft Defender for Endpoint telemetry won't be sent from this machine.</span></span></td>
   <td><span data-ttu-id="e1e32-449">Recherchez d’autres conseils de dépannage dans le journal des événements : Microsoft-Windows-UniversalTelemetryClient/Operational.</span><span class="sxs-lookup"><span data-stu-id="e1e32-449">Look for more troubleshooting hints in the event log: Microsoft-Windows-UniversalTelemetryClient/Operational.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-450">63</span><span class="sxs-lookup"><span data-stu-id="e1e32-450">63</span></span></td>
   <td><span data-ttu-id="e1e32-451">Mise à jour du type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-451">Updating the start type of external service.</span></span> <span data-ttu-id="e1e32-452">Nom : %1, type de démarrage réel : %2, type de démarrage attendu : %3, code de sortie : %4</span><span class="sxs-lookup"><span data-stu-id="e1e32-452">Name: %1, actual start type: %2, expected start type: %3, exit code: %4</span></span></td>
   <td><span data-ttu-id="e1e32-453">Type de démarrage mis à jour du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-453">Updated start type of the external service.</span></span></td>
   <td><span data-ttu-id="e1e32-454">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-454">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-455">64</span><span class="sxs-lookup"><span data-stu-id="e1e32-455">64</span></span></td>
   <td><span data-ttu-id="e1e32-456">Démarrage du service externe arrêté.</span><span class="sxs-lookup"><span data-stu-id="e1e32-456">Starting stopped external service.</span></span> <span data-ttu-id="e1e32-457">Nom : %1, code de sortie : %2</span><span class="sxs-lookup"><span data-stu-id="e1e32-457">Name: %1, exit code: %2</span></span></td>
   <td><span data-ttu-id="e1e32-458">Démarrage d’un service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-458">Starting an external service.</span></span></td>
   <td><span data-ttu-id="e1e32-459">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-459">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-460">65</span><span class="sxs-lookup"><span data-stu-id="e1e32-460">65</span></span></td>
   <td><span data-ttu-id="e1e32-461">Échec du chargement du pilote minifilter du composant Événements de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e1e32-461">Failed to load Microsoft Security Events Component Minifilter driver.</span></span> <span data-ttu-id="e1e32-462">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-462">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-463">Échec du chargement du MsSecFlt.sys du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1e32-463">Failed to load MsSecFlt.sys filesystem minifilter.</span></span></td>
   <td><span data-ttu-id="e1e32-464">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-464">Reboot the device.</span></span> <span data-ttu-id="e1e32-465">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-465">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-466">66</span><span class="sxs-lookup"><span data-stu-id="e1e32-466">66</span></span></td>
   <td><span data-ttu-id="e1e32-467">Mise à jour de stratégie : mode latence - %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-467">Policy update: Latency mode - %1</span></span></td>
   <td><span data-ttu-id="e1e32-468">La stratégie C# de connexion C a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e1e32-468">The C&C connection frequency policy was updated.</span></span></td>
   <td><span data-ttu-id="e1e32-469">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-469">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-470">68</span><span class="sxs-lookup"><span data-stu-id="e1e32-470">68</span></span></td>
   <td><span data-ttu-id="e1e32-471">Le type de démarrage du service est inattendu.</span><span class="sxs-lookup"><span data-stu-id="e1e32-471">The start type of the service is unexpected.</span></span> <span data-ttu-id="e1e32-472">Nom du service : %1, type de démarrage réel : %2, type de démarrage attendu : %3</span><span class="sxs-lookup"><span data-stu-id="e1e32-472">Service name: %1, actual start type: %2, expected start type: %3</span></span></td>
   <td><span data-ttu-id="e1e32-473">Type de démarrage de service externe inattendu.</span><span class="sxs-lookup"><span data-stu-id="e1e32-473">Unexpected external service start type.</span></span></td>
   <td><span data-ttu-id="e1e32-474">Corriger le type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-474">Fix the external service start type.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-475">69</span><span class="sxs-lookup"><span data-stu-id="e1e32-475">69</span></span></td>
   <td><span data-ttu-id="e1e32-476">Le service est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e1e32-476">The service is stopped.</span></span> <span data-ttu-id="e1e32-477">Nom du service : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-477">Service name: %1</span></span></td>
   <td><span data-ttu-id="e1e32-478">Le service externe est arrêté.</span><span class="sxs-lookup"><span data-stu-id="e1e32-478">The external service is stopped.</span></span></td>
   <td><span data-ttu-id="e1e32-479">Démarrez le service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-479">Start the external service.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-480">70</span><span class="sxs-lookup"><span data-stu-id="e1e32-480">70</span></span></td>
   <td><span data-ttu-id="e1e32-481">Mise à jour de stratégie : autoriser la collecte d’exemples - %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-481">Policy update: Allow sample collection - %1</span></span></td>
   <td><span data-ttu-id="e1e32-482">L’exemple de stratégie de collecte a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="e1e32-482">The sample collection policy was updated.</span></span></td>
   <td><span data-ttu-id="e1e32-483">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-483">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-484">71</span><span class="sxs-lookup"><span data-stu-id="e1e32-484">71</span></span></td>
   <td><span data-ttu-id="e1e32-485">Réussi à exécuter la commande : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-485">Succeeded to run command: %1</span></span></td>
   <td><span data-ttu-id="e1e32-486">La commande a été exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e1e32-486">The command was executed successfully.</span></span></td>
   <td><span data-ttu-id="e1e32-487">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-487">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-488">72</span><span class="sxs-lookup"><span data-stu-id="e1e32-488">72</span></span></td>
   <td><span data-ttu-id="e1e32-489">Nous avons essayé d’envoyer le premier rapport de profil d’ordinateur complet.</span><span class="sxs-lookup"><span data-stu-id="e1e32-489">Tried to send first full machine profile report.</span></span> <span data-ttu-id="e1e32-490">Code de résultat : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-490">Result code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-491">Informations uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1e32-491">Informational only.</span></span></td>
   <td><span data-ttu-id="e1e32-492">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-492">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-493">73</span><span class="sxs-lookup"><span data-stu-id="e1e32-493">73</span></span></td>
   <td><span data-ttu-id="e1e32-494">Sense starting for platform: %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-494">Sense starting for platform: %1</span></span></td>
   <td><span data-ttu-id="e1e32-495">Informations uniquement.</span><span class="sxs-lookup"><span data-stu-id="e1e32-495">Informational only.</span></span></td>
   <td><span data-ttu-id="e1e32-496">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-496">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-497">74</span><span class="sxs-lookup"><span data-stu-id="e1e32-497">74</span></span></td>
   <td><span data-ttu-id="e1e32-498">La balise de périphérique dans le Registre dépasse la limite de longueur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-498">Device tag in registry exceeds length limit.</span></span> <span data-ttu-id="e1e32-499">Nom de la balise : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-499">Tag name: %2.</span></span> <span data-ttu-id="e1e32-500">Limite de longueur : %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-500">Length limit: %1.</span></span></td>
   <td><span data-ttu-id="e1e32-501">La balise d’appareil dépasse la limite de longueur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-501">The device tag exceeds the length limit.</span></span></td>
   <td><span data-ttu-id="e1e32-502">Utilisez une balise d’appareil plus courte.</span><span class="sxs-lookup"><span data-stu-id="e1e32-502">Use a shorter device tag.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-503">81</span><span class="sxs-lookup"><span data-stu-id="e1e32-503">81</span></span></td>
   <td><span data-ttu-id="e1e32-504">Échec de la création dugger automatique Microsoft Defender for Endpoint ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-504">Failed to create Microsoft Defender for Endpoint ETW autologger.</span></span> <span data-ttu-id="e1e32-505">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-505">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-506">Échec de la création de la session ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-506">Failed to create the ETW session.</span></span></td>
   <td><span data-ttu-id="e1e32-507">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-507">Reboot the device.</span></span> <span data-ttu-id="e1e32-508">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-508">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-509">82</span><span class="sxs-lookup"><span data-stu-id="e1e32-509">82</span></span></td>
   <td><span data-ttu-id="e1e32-510">Échec de la suppression dugger automatique Microsoft Defender for Endpoint ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-510">Failed to remove Microsoft Defender for Endpoint ETW autologger.</span></span> <span data-ttu-id="e1e32-511">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-511">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-512">Échec de la suppression de la session ETW.</span><span class="sxs-lookup"><span data-stu-id="e1e32-512">Failed to delete the ETW session.</span></span></td>
   <td><span data-ttu-id="e1e32-513">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-513">Contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-514">84</span><span class="sxs-lookup"><span data-stu-id="e1e32-514">84</span></span></td>
   <td><span data-ttu-id="e1e32-515">Définissez Windows Defender mode d’exécution antivirus.</span><span class="sxs-lookup"><span data-stu-id="e1e32-515">Set Windows Defender Antivirus running mode.</span></span> <span data-ttu-id="e1e32-516">Forcer le mode passif : %1, code de résultat : %2.</span><span class="sxs-lookup"><span data-stu-id="e1e32-516">Force passive mode: %1, result code: %2.</span></span></td>
   <td><span data-ttu-id="e1e32-517">Définir le mode d’exécution de Defender (actif ou passif).</span><span class="sxs-lookup"><span data-stu-id="e1e32-517">Set defender running mode (active or passive).</span></span></td>
   <td><span data-ttu-id="e1e32-518">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-518">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-519">85</span><span class="sxs-lookup"><span data-stu-id="e1e32-519">85</span></span></td>
   <td><span data-ttu-id="e1e32-520">Échec du déclenchement de Microsoft Defender pour le point de terminaison exécutable.</span><span class="sxs-lookup"><span data-stu-id="e1e32-520">Failed to trigger Microsoft Defender for Endpoint executable.</span></span> <span data-ttu-id="e1e32-521">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-521">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-522">Échec de l’exécution de SenseIR.</span><span class="sxs-lookup"><span data-stu-id="e1e32-522">Starring SenseIR executable failed.</span></span></td>
   <td><span data-ttu-id="e1e32-523">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-523">Reboot the device.</span></span> <span data-ttu-id="e1e32-524">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-524">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-525">86</span><span class="sxs-lookup"><span data-stu-id="e1e32-525">86</span></span></td>
   <td><span data-ttu-id="e1e32-526">Le démarrage a arrêté à nouveau le service externe qui devrait être en service.</span><span class="sxs-lookup"><span data-stu-id="e1e32-526">Starting again stopped external service that should be up.</span></span> <span data-ttu-id="e1e32-527">Nom : %1, code de sortie : %2</span><span class="sxs-lookup"><span data-stu-id="e1e32-527">Name: %1, exit code: %2</span></span></td>
   <td><span data-ttu-id="e1e32-528">Recommencez le service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-528">Starting the external service again.</span></span></td>
   <td><span data-ttu-id="e1e32-529">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-529">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-530">87</span><span class="sxs-lookup"><span data-stu-id="e1e32-530">87</span></span></td>
   <td><span data-ttu-id="e1e32-531">Impossible de démarrer le service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-531">Cannot start the external service.</span></span> <span data-ttu-id="e1e32-532">Nom : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-532">Name: %1</span></span></td>
   <td><span data-ttu-id="e1e32-533">Échec du démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-533">Failed to start the external service.</span></span></td>
   <td><span data-ttu-id="e1e32-534">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-534">Contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-535">88</span><span class="sxs-lookup"><span data-stu-id="e1e32-535">88</span></span></td>
   <td><span data-ttu-id="e1e32-536">Mise à jour à nouveau du type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-536">Updating the start type of external service again.</span></span> <span data-ttu-id="e1e32-537">Nom : %1, type de démarrage réel : %2, type de démarrage attendu : %3, code de sortie : %4</span><span class="sxs-lookup"><span data-stu-id="e1e32-537">Name: %1, actual start type: %2, expected start type: %3, exit code: %4</span></span></td>
   <td><span data-ttu-id="e1e32-538">Mise à jour du type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-538">Updated the start type of the external service.</span></span></td>
   <td><span data-ttu-id="e1e32-539">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-539">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-540">89</span><span class="sxs-lookup"><span data-stu-id="e1e32-540">89</span></span></td>
   <td><span data-ttu-id="e1e32-541">Impossible de mettre à jour le type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-541">Cannot update the start type of external service.</span></span> <span data-ttu-id="e1e32-542">Nom : %1, type de début réel : %2, type de démarrage attendu : %3</span><span class="sxs-lookup"><span data-stu-id="e1e32-542">Name: %1, actual start type: %2, expected start type: %3</span></span></td>
   <td><span data-ttu-id="e1e32-543">Ne peut pas mettre à jour le type de démarrage du service externe.</span><span class="sxs-lookup"><span data-stu-id="e1e32-543">Can't update the start type of the external service.</span></span></td>
   <td><span data-ttu-id="e1e32-544">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-544">Contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-545">90</span><span class="sxs-lookup"><span data-stu-id="e1e32-545">90</span></span></td>
   <td><span data-ttu-id="e1e32-546">Échec de la configuration de System Guard Runtime Monitor pour la connexion au service cloud dans la région géographique %1.</span><span class="sxs-lookup"><span data-stu-id="e1e32-546">Failed to configure System Guard Runtime Monitor to connect to cloud service in geo-region %1.</span></span> <span data-ttu-id="e1e32-547">Code d’échec : %2</span><span class="sxs-lookup"><span data-stu-id="e1e32-547">Failure code: %2</span></span></td>
   <td><span data-ttu-id="e1e32-548">System Guard Runtime Monitor n’envoie pas de données d’attestation au service cloud.</span><span class="sxs-lookup"><span data-stu-id="e1e32-548">System Guard Runtime Monitor won't send attestation data to the cloud service.</span></span></td>
   <td><span data-ttu-id="e1e32-549">Vérifiez les autorisations sur le chemin d’accès d’inscription : « HKLM\Software\Microsoft\Windows\CurrentVersion\Sgrm ».</span><span class="sxs-lookup"><span data-stu-id="e1e32-549">Check the permissions on register path: "HKLM\Software\Microsoft\Windows\CurrentVersion\Sgrm".</span></span> <span data-ttu-id="e1e32-550">Si aucun problème n’est détecté, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-550">If no issues spotted, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-551">91</span><span class="sxs-lookup"><span data-stu-id="e1e32-551">91</span></span></td>
   <td><span data-ttu-id="e1e32-552">Échec de la suppression des informations de région de System Guard Runtime Monitor.</span><span class="sxs-lookup"><span data-stu-id="e1e32-552">Failed to remove System Guard Runtime Monitor geo-region information.</span></span> <span data-ttu-id="e1e32-553">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-553">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-554">System Guard Runtime Monitor n’envoie pas de données d’attestation au service cloud.</span><span class="sxs-lookup"><span data-stu-id="e1e32-554">System Guard Runtime Monitor won't send attestation data to the cloud service.</span></span></td>
   <td><span data-ttu-id="e1e32-555">Vérifiez les autorisations sur le chemin d’accès d’inscription : « HKLM\Software\Microsoft\Windows\CurrentVersion\Sgrm ».</span><span class="sxs-lookup"><span data-stu-id="e1e32-555">Check the permissions on register path: "HKLM\Software\Microsoft\Windows\CurrentVersion\Sgrm".</span></span> <span data-ttu-id="e1e32-556">Si aucun problème n’est détecté, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-556">If no issues spotted, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-557">92</span><span class="sxs-lookup"><span data-stu-id="e1e32-557">92</span></span></td>
   <td><span data-ttu-id="e1e32-558">Arrêt du quota de cyber-données du capteur car le quota de données est dépassé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-558">Stopping sending sensor cyber data quota because data quota is exceeded.</span></span> <span data-ttu-id="e1e32-559">Reprendra l’envoi une fois la période de quotas franchie.</span><span class="sxs-lookup"><span data-stu-id="e1e32-559">Will resume sending once quota period passes.</span></span> <span data-ttu-id="e1e32-560">Masque d’état : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-560">State Mask: %1</span></span></td>
   <td><span data-ttu-id="e1e32-561">Dépassez la limite de limitation.</span><span class="sxs-lookup"><span data-stu-id="e1e32-561">Exceed throttling limit.</span></span></td>
   <td><span data-ttu-id="e1e32-562">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-562">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-563">93</span><span class="sxs-lookup"><span data-stu-id="e1e32-563">93</span></span></td>
   <td><span data-ttu-id="e1e32-564">Reprise de l’envoi des données cyber du capteur.</span><span class="sxs-lookup"><span data-stu-id="e1e32-564">Resuming sending sensor cyber data.</span></span> <span data-ttu-id="e1e32-565">Masque d’état : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-565">State Mask: %1</span></span></td>
   <td><span data-ttu-id="e1e32-566">Reprendre l’envoi de cyber-données.</span><span class="sxs-lookup"><span data-stu-id="e1e32-566">Resume cyber data submission.</span></span></td>
   <td><span data-ttu-id="e1e32-567">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-567">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-568">94</span><span class="sxs-lookup"><span data-stu-id="e1e32-568">94</span></span></td>
   <td><span data-ttu-id="e1e32-569">L’exécutable Microsoft Defender for Endpoint a démarré</span><span class="sxs-lookup"><span data-stu-id="e1e32-569">Microsoft Defender for Endpoint executable has started</span></span></td>
   <td><span data-ttu-id="e1e32-570">L’exécutable SenseCE a démarré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-570">The SenseCE executable has started.</span></span></td>
   <td><span data-ttu-id="e1e32-571">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-571">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-572">95</span><span class="sxs-lookup"><span data-stu-id="e1e32-572">95</span></span></td>
   <td><span data-ttu-id="e1e32-573">L’exécutable Microsoft Defender for Endpoint a pris fin</span><span class="sxs-lookup"><span data-stu-id="e1e32-573">Microsoft Defender for Endpoint executable has ended</span></span></td>
   <td><span data-ttu-id="e1e32-574">L’exécutable SenseCE a pris fin.</span><span class="sxs-lookup"><span data-stu-id="e1e32-574">The SenseCE executable has ended.</span></span></td>
   <td><span data-ttu-id="e1e32-575">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-575">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-576">96</span><span class="sxs-lookup"><span data-stu-id="e1e32-576">96</span></span></td>
   <td><span data-ttu-id="e1e32-577">Microsoft Defender for Endpoint Init a appelé.</span><span class="sxs-lookup"><span data-stu-id="e1e32-577">Microsoft Defender for Endpoint Init has called.</span></span> <span data-ttu-id="e1e32-578">Code de résultat : %2</span><span class="sxs-lookup"><span data-stu-id="e1e32-578">Result code: %2</span></span></td>
   <td><span data-ttu-id="e1e32-579">L’exécutable SenseCE a appelé l’initialisation MCE.</span><span class="sxs-lookup"><span data-stu-id="e1e32-579">The SenseCE executable has called MCE initialization.</span></span></td>
   <td><span data-ttu-id="e1e32-580">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-580">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-581">97</span><span class="sxs-lookup"><span data-stu-id="e1e32-581">97</span></span></td>
   <td><span data-ttu-id="e1e32-582">Il existe des problèmes de connectivité au cloud pour le scénario DLP</span><span class="sxs-lookup"><span data-stu-id="e1e32-582">There are connectivity issues to the Cloud for the DLP scenario</span></span></td>
   <td><span data-ttu-id="e1e32-583">Certains problèmes de connectivité réseau affectent le flux de classification DLP.</span><span class="sxs-lookup"><span data-stu-id="e1e32-583">There are network connectivity issues that affect the DLP classification flow.</span></span></td>
   <td><span data-ttu-id="e1e32-584">Vérifiez la connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="e1e32-584">Check the network connectivity.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-585">98</span><span class="sxs-lookup"><span data-stu-id="e1e32-585">98</span></span></td>
   <td><span data-ttu-id="e1e32-586">La connectivité au cloud pour le scénario DLP a été restaurée</span><span class="sxs-lookup"><span data-stu-id="e1e32-586">The connectivity to the Cloud for the DLP scenario has been restored</span></span></td>
   <td><span data-ttu-id="e1e32-587">La connectivité au réseau a été restaurée et le flux de classification DLP peut continuer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-587">The connectivity to the network was restored and the DLP classification flow can continue.</span></span></td>
   <td><span data-ttu-id="e1e32-588">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-588">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-589">99</span><span class="sxs-lookup"><span data-stu-id="e1e32-589">99</span></span></td>
   <td><span data-ttu-id="e1e32-590">Sense a rencontré l’erreur suivante lors de la communication avec le serveur : (%1).</span><span class="sxs-lookup"><span data-stu-id="e1e32-590">Sense has encountered the following error while communicating with server: (%1).</span></span> <span data-ttu-id="e1e32-591">Résultat : (%2)</span><span class="sxs-lookup"><span data-stu-id="e1e32-591">Result: (%2)</span></span></td>
   <td><span data-ttu-id="e1e32-592">Une erreur de communication s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e1e32-592">A communication error occurred.</span></span></td>
   <td><span data-ttu-id="e1e32-593">Pour plus d’informations, consultez les événements suivants dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="e1e32-593">Check the following events in the event log for further details.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-594">100</span><span class="sxs-lookup"><span data-stu-id="e1e32-594">100</span></span></td>
   <td><span data-ttu-id="e1e32-595">Échec du démarrage de l’exécutable Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e1e32-595">Microsoft Defender for Endpoint executable failed to start.</span></span> <span data-ttu-id="e1e32-596">Code d’échec : %1</span><span class="sxs-lookup"><span data-stu-id="e1e32-596">Failure code: %1</span></span></td>
   <td><span data-ttu-id="e1e32-597">L’exécutable SenseCE n’a pas réussi à démarrer.</span><span class="sxs-lookup"><span data-stu-id="e1e32-597">The SenseCE executable has failed to start.</span></span></td>
   <td><span data-ttu-id="e1e32-598">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1e32-598">Reboot the device.</span></span> <span data-ttu-id="e1e32-599">Si cette erreur persiste, contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="e1e32-599">If this error persists, contact Support.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-600">102</span><span class="sxs-lookup"><span data-stu-id="e1e32-600">102</span></span></td>
   <td><span data-ttu-id="e1e32-601">L’exécutable de détection et de réponse réseau microsoft Defender pour points de terminaison a démarré</span><span class="sxs-lookup"><span data-stu-id="e1e32-601">Microsoft Defender for Endpoint Network Detection and Response executable has started</span></span></td>
   <td><span data-ttu-id="e1e32-602">L’exécutable SenseNdr a démarré.</span><span class="sxs-lookup"><span data-stu-id="e1e32-602">The SenseNdr executable has started.</span></span></td>
   <td><span data-ttu-id="e1e32-603">Notification de fonctionnement normal ; aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-603">Normal operating notification; no action required.</span></span></td>
</tr>
<tr>
   <td><span data-ttu-id="e1e32-604">103</span><span class="sxs-lookup"><span data-stu-id="e1e32-604">103</span></span></td>
   <td><span data-ttu-id="e1e32-605">L'exécutable de détection et de réponse réseau microsoft Defender pour points de terminaison a pris fin</span><span class="sxs-lookup"><span data-stu-id="e1e32-605">Microsoft Defender for Endpoint Network Detection and Response executable has ended</span></span></td>
   <td><span data-ttu-id="e1e32-606">L'exécutable SenseNdr a pris fin.</span><span class="sxs-lookup"><span data-stu-id="e1e32-606">The SenseNdr executable has ended.</span></span></td>
   <td><span data-ttu-id="e1e32-607">Notification de fonctionnement normal ; aucune action n'est requise.</span><span class="sxs-lookup"><span data-stu-id="e1e32-607">Normal operating notification; no action required.</span></span></td>
</tr>
</tbody>
</table>

><span data-ttu-id="e1e32-608">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e1e32-608">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e1e32-609">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e1e32-609">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-eventerrorcodes-belowfoldlink)

## <a name="related-topics"></a><span data-ttu-id="e1e32-610">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1e32-610">Related topics</span></span>
- [<span data-ttu-id="e1e32-611">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="e1e32-611">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="e1e32-612">Configurer les paramètres de proxy d'appareil et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="e1e32-612">Configure device proxy and Internet connectivity settings</span></span>](configure-proxy-internet.md)
- [<span data-ttu-id="e1e32-613">Résoudre des problèmes avec Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e1e32-613">Troubleshoot Microsoft Defender for Endpoint</span></span>](troubleshoot-onboarding.md)
