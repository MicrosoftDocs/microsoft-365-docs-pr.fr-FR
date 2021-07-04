---
title: API Obtenir des alertes
description: Découvrez les méthodes et les propriétés du type de ressource Alerte dans Microsoft Defender pour point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
search.product: eADQiWindows 10XVcnh
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: df1a032ffab0490c41edc7d282f0f2cc60608870
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289678"
---
# <a name="alert-resource-type"></a><span data-ttu-id="17242-104">Type de ressource Alerte</span><span class="sxs-lookup"><span data-stu-id="17242-104">Alert resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="17242-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="17242-105">**Applies to:**</span></span>
- [<span data-ttu-id="17242-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="17242-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

- <span data-ttu-id="17242-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="17242-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="17242-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="17242-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="methods"></a><span data-ttu-id="17242-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17242-109">Methods</span></span>

<span data-ttu-id="17242-110">Méthode</span><span class="sxs-lookup"><span data-stu-id="17242-110">Method</span></span> |<span data-ttu-id="17242-111">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="17242-111">Return Type</span></span> |<span data-ttu-id="17242-112">Description</span><span class="sxs-lookup"><span data-stu-id="17242-112">Description</span></span>
:---|:---|:---
[<span data-ttu-id="17242-113">Obtenir une alerte</span><span class="sxs-lookup"><span data-stu-id="17242-113">Get alert</span></span>](get-alert-info-by-id.md) | [<span data-ttu-id="17242-114">Alerte</span><span class="sxs-lookup"><span data-stu-id="17242-114">Alert</span></span>](alerts.md) | <span data-ttu-id="17242-115">Obtenir un objet [d’alerte](alerts.md) unique.</span><span class="sxs-lookup"><span data-stu-id="17242-115">Get a single [alert](alerts.md) object.</span></span>
[<span data-ttu-id="17242-116">Répertorier les alertes</span><span class="sxs-lookup"><span data-stu-id="17242-116">List alerts</span></span>](get-alerts.md) | <span data-ttu-id="17242-117">[Collection d’alertes](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-117">[Alert](alerts.md) collection</span></span> | <span data-ttu-id="17242-118">Liste de la collection [d’alertes.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-118">List [alert](alerts.md) collection.</span></span>
[<span data-ttu-id="17242-119">Mettre à jour une alerte</span><span class="sxs-lookup"><span data-stu-id="17242-119">Update alert</span></span>](update-alert.md) | [<span data-ttu-id="17242-120">Alerte</span><span class="sxs-lookup"><span data-stu-id="17242-120">Alert</span></span>](alerts.md) | <span data-ttu-id="17242-121">Mettre à jour une [alerte spécifique.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-121">Update specific [alert](alerts.md).</span></span>
[<span data-ttu-id="17242-122">Alertes de mise à jour par lot</span><span class="sxs-lookup"><span data-stu-id="17242-122">Batch update alerts</span></span>](batch-update-alerts.md) | | <span data-ttu-id="17242-123">Mettre à jour un lot [d’alertes.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-123">Update a batch of [alerts](alerts.md).</span></span>
[<span data-ttu-id="17242-124">Créer une alerte</span><span class="sxs-lookup"><span data-stu-id="17242-124">Create alert</span></span>](create-alert-by-reference.md)|[<span data-ttu-id="17242-125">Alerte</span><span class="sxs-lookup"><span data-stu-id="17242-125">Alert</span></span>](alerts.md)|<span data-ttu-id="17242-126">Créez une alerte basée sur les données d’événement obtenues à partir [de la recherche avancée](run-advanced-query-api.md).</span><span class="sxs-lookup"><span data-stu-id="17242-126">Create an alert based on event data obtained from [Advanced Hunting](run-advanced-query-api.md).</span></span>
[<span data-ttu-id="17242-127">Liste des domaines associés</span><span class="sxs-lookup"><span data-stu-id="17242-127">List related domains</span></span>](get-alert-related-domain-info.md)|<span data-ttu-id="17242-128">Collection de domaines</span><span class="sxs-lookup"><span data-stu-id="17242-128">Domain collection</span></span>| <span data-ttu-id="17242-129">Ré lister les URL associées à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-129">List URLs associated with the alert.</span></span>
[<span data-ttu-id="17242-130">Liste des fichiers associés</span><span class="sxs-lookup"><span data-stu-id="17242-130">List related files</span></span>](get-alert-related-files-info.md) | <span data-ttu-id="17242-131">[Collection de](files.md) fichiers</span><span class="sxs-lookup"><span data-stu-id="17242-131">[File](files.md) collection</span></span> |  <span data-ttu-id="17242-132">Liste des [entités](files.md) de fichier associées à [l’alerte.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-132">List the [file](files.md) entities that are associated with the [alert](alerts.md).</span></span>
[<span data-ttu-id="17242-133">Liste des IP associées</span><span class="sxs-lookup"><span data-stu-id="17242-133">List related IPs</span></span>](get-alert-related-ip-info.md) | <span data-ttu-id="17242-134">Collection d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="17242-134">IP collection</span></span> | <span data-ttu-id="17242-135">List IPs that are associated with the alert.</span><span class="sxs-lookup"><span data-stu-id="17242-135">List IPs that are associated with the alert.</span></span>
[<span data-ttu-id="17242-136">Obtenir des ordinateurs associés</span><span class="sxs-lookup"><span data-stu-id="17242-136">Get related machines</span></span>](get-alert-related-machine-info.md) | [<span data-ttu-id="17242-137">Ordinateur</span><span class="sxs-lookup"><span data-stu-id="17242-137">Machine</span></span>](machine.md) | <span data-ttu-id="17242-138">[L’ordinateur](machine.md) associé à [l’alerte](alerts.md).</span><span class="sxs-lookup"><span data-stu-id="17242-138">The [machine](machine.md) that is associated with the [alert](alerts.md).</span></span>
[<span data-ttu-id="17242-139">Obtenir des utilisateurs associés</span><span class="sxs-lookup"><span data-stu-id="17242-139">Get related users</span></span>](get-alert-related-user-info.md) | [<span data-ttu-id="17242-140">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="17242-140">User</span></span>](user.md) | <span data-ttu-id="17242-141">Utilisateur [associé](user.md) à [l’alerte.](alerts.md)</span><span class="sxs-lookup"><span data-stu-id="17242-141">The [user](user.md) that is associated with the [alert](alerts.md).</span></span>

## <a name="properties"></a><span data-ttu-id="17242-142">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17242-142">Properties</span></span>

<span data-ttu-id="17242-143">Propriété</span><span class="sxs-lookup"><span data-stu-id="17242-143">Property</span></span> |    <span data-ttu-id="17242-144">Type</span><span class="sxs-lookup"><span data-stu-id="17242-144">Type</span></span>    |    <span data-ttu-id="17242-145">Description</span><span class="sxs-lookup"><span data-stu-id="17242-145">Description</span></span>
:---|:---|:---
<span data-ttu-id="17242-146">id</span><span class="sxs-lookup"><span data-stu-id="17242-146">id</span></span> | <span data-ttu-id="17242-147">String</span><span class="sxs-lookup"><span data-stu-id="17242-147">String</span></span> | <span data-ttu-id="17242-148">ID d’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-148">Alert ID.</span></span>
<span data-ttu-id="17242-149">title</span><span class="sxs-lookup"><span data-stu-id="17242-149">title</span></span> | <span data-ttu-id="17242-150">String</span><span class="sxs-lookup"><span data-stu-id="17242-150">String</span></span> | <span data-ttu-id="17242-151">Titre de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-151">Alert title.</span></span>
<span data-ttu-id="17242-152">description</span><span class="sxs-lookup"><span data-stu-id="17242-152">description</span></span> | <span data-ttu-id="17242-153">String</span><span class="sxs-lookup"><span data-stu-id="17242-153">String</span></span> | <span data-ttu-id="17242-154">Description de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-154">Alert description.</span></span>
<span data-ttu-id="17242-155">alertCreationTime</span><span class="sxs-lookup"><span data-stu-id="17242-155">alertCreationTime</span></span> | <span data-ttu-id="17242-156">Nullable DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17242-156">Nullable DateTimeOffset</span></span> | <span data-ttu-id="17242-157">Date et heure (au UTC) de création de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-157">The date and time (in UTC) the alert was created.</span></span>
<span data-ttu-id="17242-158">lastEventTime</span><span class="sxs-lookup"><span data-stu-id="17242-158">lastEventTime</span></span> | <span data-ttu-id="17242-159">Nullable DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17242-159">Nullable DateTimeOffset</span></span> | <span data-ttu-id="17242-160">Dernière occurrence de l’événement qui a déclenché l’alerte sur le même appareil.</span><span class="sxs-lookup"><span data-stu-id="17242-160">The last occurrence of the event that triggered the alert on the same device.</span></span>
<span data-ttu-id="17242-161">firstEventTime</span><span class="sxs-lookup"><span data-stu-id="17242-161">firstEventTime</span></span> | <span data-ttu-id="17242-162">Nullable DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17242-162">Nullable DateTimeOffset</span></span> | <span data-ttu-id="17242-163">Première occurrence de l’événement qui a déclenché l’alerte sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="17242-163">The first occurrence of the event that triggered the alert on that device.</span></span>
<span data-ttu-id="17242-164">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="17242-164">lastUpdateTime</span></span> | <span data-ttu-id="17242-165">Nullable DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17242-165">Nullable DateTimeOffset</span></span> | <span data-ttu-id="17242-166">Date et heure (au UTC) de la dernière mise à jour de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-166">The date and time (in UTC) the alert was last updated.</span></span>
<span data-ttu-id="17242-167">resolvedTime</span><span class="sxs-lookup"><span data-stu-id="17242-167">resolvedTime</span></span> | <span data-ttu-id="17242-168">Nullable DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="17242-168">Nullable DateTimeOffset</span></span> | <span data-ttu-id="17242-169">Date et heure à laquelle l’état de l’alerte a été modifié en « Résolu ».</span><span class="sxs-lookup"><span data-stu-id="17242-169">The date and time in which the status of the alert was changed to 'Resolved'.</span></span>
<span data-ttu-id="17242-170">incidentId</span><span class="sxs-lookup"><span data-stu-id="17242-170">incidentId</span></span> | <span data-ttu-id="17242-171">Nullable Long</span><span class="sxs-lookup"><span data-stu-id="17242-171">Nullable Long</span></span> | <span data-ttu-id="17242-172">ID [d’incident](view-incidents-queue.md) de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-172">The [Incident](view-incidents-queue.md) ID of the Alert.</span></span>
<span data-ttu-id="17242-173">investigationId</span><span class="sxs-lookup"><span data-stu-id="17242-173">investigationId</span></span> | <span data-ttu-id="17242-174">Nullable Long</span><span class="sxs-lookup"><span data-stu-id="17242-174">Nullable Long</span></span> | <span data-ttu-id="17242-175">ID [d’investigation](automated-investigations.md) lié à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-175">The [Investigation](automated-investigations.md) ID related to the Alert.</span></span>
<span data-ttu-id="17242-176">investigationState</span><span class="sxs-lookup"><span data-stu-id="17242-176">investigationState</span></span> | <span data-ttu-id="17242-177">Nullable, enum</span><span class="sxs-lookup"><span data-stu-id="17242-177">Nullable Enum</span></span> | <span data-ttu-id="17242-178">L’état actuel de [l’examen](automated-investigations.md).</span><span class="sxs-lookup"><span data-stu-id="17242-178">The current state of the [Investigation](automated-investigations.md).</span></span> <span data-ttu-id="17242-179">Les valeurs possibles sont : « Unknown » (inconnu), « Terminated » (terminé), « SuccessfullyRemediated », 'Suppress', 'Failed', 'PartiallyRemediated', 'Running', 'PendingApproval', 'PendingResource', 'PartiallyExploigated', 'TerminatedByUser', 'TerminatedBySystem', 'Queued', 'InnerFailure', 'PreexistingAlert', 'UnsupportedOs', 'UnsupportedAlertType', 'SuppressedAlert'.</span><span class="sxs-lookup"><span data-stu-id="17242-179">Possible values are: 'Unknown', 'Terminated', 'SuccessfullyRemediated', 'Benign', 'Failed', 'PartiallyRemediated', 'Running', 'PendingApproval', 'PendingResource', 'PartiallyInvestigated', 'TerminatedByUser', 'TerminatedBySystem', 'Queued', 'InnerFailure', 'PreexistingAlert', 'UnsupportedOs', 'UnsupportedAlertType', 'SuppressedAlert'.</span></span>
<span data-ttu-id="17242-180">assignedTo</span><span class="sxs-lookup"><span data-stu-id="17242-180">assignedTo</span></span> | <span data-ttu-id="17242-181">String</span><span class="sxs-lookup"><span data-stu-id="17242-181">String</span></span> | <span data-ttu-id="17242-182">Propriétaire de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-182">Owner of the alert.</span></span>
<span data-ttu-id="17242-183">Sévérité </span><span class="sxs-lookup"><span data-stu-id="17242-183">severity</span></span> | <span data-ttu-id="17242-184">Énum</span><span class="sxs-lookup"><span data-stu-id="17242-184">Enum</span></span> | <span data-ttu-id="17242-185">Gravité de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-185">Severity of the alert.</span></span> <span data-ttu-id="17242-186">Les valeurs possibles sont : « UnSpecified » (non spécifié), « Informational » (informations), « Low » (faible), « Medium » (moyen) et « High » (élevé).</span><span class="sxs-lookup"><span data-stu-id="17242-186">Possible values are: 'UnSpecified', 'Informational', 'Low', 'Medium' and 'High'.</span></span>
<span data-ttu-id="17242-187">status</span><span class="sxs-lookup"><span data-stu-id="17242-187">status</span></span> | <span data-ttu-id="17242-188">Énum</span><span class="sxs-lookup"><span data-stu-id="17242-188">Enum</span></span> | <span data-ttu-id="17242-189">Spécifie l’état actuel de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-189">Specifies the current status of the alert.</span></span> <span data-ttu-id="17242-190">Les valeurs possibles sont : « Unknown » (inconnu), « New » (nouveau), « InProgress » (inprogress) et « Resolved » (résolu).</span><span class="sxs-lookup"><span data-stu-id="17242-190">Possible values are: 'Unknown', 'New', 'InProgress' and 'Resolved'.</span></span>
<span data-ttu-id="17242-191">classification</span><span class="sxs-lookup"><span data-stu-id="17242-191">classification</span></span> | <span data-ttu-id="17242-192">Nullable, enum</span><span class="sxs-lookup"><span data-stu-id="17242-192">Nullable Enum</span></span> | <span data-ttu-id="17242-193">Spécification de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-193">Specification of the alert.</span></span> <span data-ttu-id="17242-194">Les valeurs possibles sont : « Unknown » (inconnu), « FalsePositive » (fauxpositif), « TruePositive » (vraipositif).</span><span class="sxs-lookup"><span data-stu-id="17242-194">Possible values are: 'Unknown', 'FalsePositive', 'TruePositive'.</span></span>
<span data-ttu-id="17242-195">détermination</span><span class="sxs-lookup"><span data-stu-id="17242-195">determination</span></span> | <span data-ttu-id="17242-196">Nullable, enum</span><span class="sxs-lookup"><span data-stu-id="17242-196">Nullable Enum</span></span> | <span data-ttu-id="17242-197">Spécifie la détermination de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-197">Specifies the determination of the alert.</span></span> <span data-ttu-id="17242-198">Les valeurs possibles sont : 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'.</span><span class="sxs-lookup"><span data-stu-id="17242-198">Possible values are: 'NotAvailable', 'Apt', 'Malware', 'SecurityPersonnel', 'SecurityTesting', 'UnwantedSoftware', 'Other'.</span></span>
<span data-ttu-id="17242-199">category</span><span class="sxs-lookup"><span data-stu-id="17242-199">category</span></span>| <span data-ttu-id="17242-200">String</span><span class="sxs-lookup"><span data-stu-id="17242-200">String</span></span> | <span data-ttu-id="17242-201">Catégorie de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-201">Category of the alert.</span></span>
<span data-ttu-id="17242-202">detectionSource</span><span class="sxs-lookup"><span data-stu-id="17242-202">detectionSource</span></span> | <span data-ttu-id="17242-203">String</span><span class="sxs-lookup"><span data-stu-id="17242-203">String</span></span> | <span data-ttu-id="17242-204">Source de détection.</span><span class="sxs-lookup"><span data-stu-id="17242-204">Detection source.</span></span>
<span data-ttu-id="17242-205">threatFamilyName</span><span class="sxs-lookup"><span data-stu-id="17242-205">threatFamilyName</span></span> | <span data-ttu-id="17242-206">String</span><span class="sxs-lookup"><span data-stu-id="17242-206">String</span></span> | <span data-ttu-id="17242-207">Famille de menaces.</span><span class="sxs-lookup"><span data-stu-id="17242-207">Threat family.</span></span>
<span data-ttu-id="17242-208">threatName</span><span class="sxs-lookup"><span data-stu-id="17242-208">threatName</span></span> | <span data-ttu-id="17242-209">String</span><span class="sxs-lookup"><span data-stu-id="17242-209">String</span></span> | <span data-ttu-id="17242-210">Nom de la menace.</span><span class="sxs-lookup"><span data-stu-id="17242-210">Threat name.</span></span>
<span data-ttu-id="17242-211">machineId</span><span class="sxs-lookup"><span data-stu-id="17242-211">machineId</span></span> | <span data-ttu-id="17242-212">String</span><span class="sxs-lookup"><span data-stu-id="17242-212">String</span></span> | <span data-ttu-id="17242-213">ID d’une [entité](machine.md) d’ordinateur associée à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-213">ID of a [machine](machine.md) entity that is associated with the alert.</span></span>
<span data-ttu-id="17242-214">computerDnsName</span><span class="sxs-lookup"><span data-stu-id="17242-214">computerDnsName</span></span> | <span data-ttu-id="17242-215">String</span><span class="sxs-lookup"><span data-stu-id="17242-215">String</span></span> | <span data-ttu-id="17242-216">[nom complet](machine.md) de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="17242-216">[machine](machine.md) fully qualified name.</span></span>
<span data-ttu-id="17242-217">aadTenantId</span><span class="sxs-lookup"><span data-stu-id="17242-217">aadTenantId</span></span> | <span data-ttu-id="17242-218">String</span><span class="sxs-lookup"><span data-stu-id="17242-218">String</span></span> | <span data-ttu-id="17242-219">ID Azure Active Directory de l’ID de l’ID de l’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17242-219">The Azure Active Directory ID.</span></span>
<span data-ttu-id="17242-220">détecteurId</span><span class="sxs-lookup"><span data-stu-id="17242-220">detectorId</span></span> | <span data-ttu-id="17242-221">String</span><span class="sxs-lookup"><span data-stu-id="17242-221">String</span></span> | <span data-ttu-id="17242-222">ID du détecteur qui a déclenché l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-222">The ID of the detector that triggered the alert.</span></span>
<span data-ttu-id="17242-223">commentaires</span><span class="sxs-lookup"><span data-stu-id="17242-223">comments</span></span> | <span data-ttu-id="17242-224">Liste des commentaires d’alerte</span><span class="sxs-lookup"><span data-stu-id="17242-224">List of Alert comments</span></span> | <span data-ttu-id="17242-225">L’objet Comment de l’alerte contient : chaîne de commentaire, chaîne createdBy et heure de date createTime.</span><span class="sxs-lookup"><span data-stu-id="17242-225">Alert Comment object contains: comment string, createdBy string and createTime date time.</span></span>
<span data-ttu-id="17242-226">Évidence</span><span class="sxs-lookup"><span data-stu-id="17242-226">Evidence</span></span> | <span data-ttu-id="17242-227">Liste des preuves d’alerte</span><span class="sxs-lookup"><span data-stu-id="17242-227">List of Alert evidence</span></span> | <span data-ttu-id="17242-228">Preuve liée à l’alerte.</span><span class="sxs-lookup"><span data-stu-id="17242-228">Evidence related to the alert.</span></span> <span data-ttu-id="17242-229">Voir l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="17242-229">See example below.</span></span>

### <a name="response-example-for-getting-single-alert"></a><span data-ttu-id="17242-230">Exemple de réponse pour l’obtention d’une alerte unique :</span><span class="sxs-lookup"><span data-stu-id="17242-230">Response example for getting single alert:</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/alerts/da637472900382838869_1364969609
```

```json
{
    "id": "da637472900382838869_1364969609",
    "incidentId": 1126093,
    "investigationId": null,
    "assignedTo": null,
    "severity": "Low",
    "status": "New",
    "classification": null,
    "determination": null,
    "investigationState": "Queued",
    "detectionSource": "WindowsDefenderAtp",
    "detectorId": "17e10bbc-3a68-474a-8aad-faef14d43952",
    "category": "Execution",
    "threatFamilyName": null,
    "title": "Low-reputation arbitrary code executed by signed executable",
    "description": "Binaries signed by Microsoft can be used to run low-reputation arbitrary code. This technique hides the execution of malicious code within a trusted process. As a result, the trusted process might exhibit suspicious behaviors, such as opening a listening port or connecting to a command-and-control (C&C) server.",
    "alertCreationTime": "2021-01-26T20:33:57.7220239Z",
    "firstEventTime": "2021-01-26T20:31:32.9562661Z",
    "lastEventTime": "2021-01-26T20:31:33.0577322Z",
    "lastUpdateTime": "2021-01-26T20:33:59.2Z",
    "resolvedTime": null,
    "machineId": "111e6dd8c833c8a052ea231ec1b19adaf497b625",
    "computerDnsName": "temp123.middleeast.corp.microsoft.com",
    "rbacGroupName": "A",
    "aadTenantId": "a839b112-1253-6432-9bf6-94542403f21c",
    "threatName": null,
    "mitreTechniques": [
        "T1064",
        "T1085",
        "T1220"
    ],
    "relatedUser": {
        "userName": "temp123",
        "domainName": "MIDDLEEAST"
    },
    "comments": [
        {
            "comment": "test comment for docs",
            "createdBy": "secop123@contoso.com",
            "createdTime": "2021-01-26T01:00:37.8404534Z"
        }
    ],
    "evidence": [
        {
            "entityType": "User",
            "evidenceCreationTime": "2021-01-26T20:33:58.42Z",
            "sha1": null,
            "sha256": null,
            "fileName": null,
            "filePath": null,
            "processId": null,
            "processCommandLine": null,
            "processCreationTime": null,
            "parentProcessId": null,
            "parentProcessCreationTime": null,
            "parentProcessFileName": null,
            "parentProcessFilePath": null,
            "ipAddress": null,
            "url": null,
            "registryKey": null,
            "registryHive": null,
            "registryValueType": null,
            "registryValue": null,
            "accountName": "eranb",
            "domainName": "MIDDLEEAST",
            "userSid": "S-1-5-21-11111607-1111760036-109187956-75141",
            "aadUserId": "11118379-2a59-1111-ac3c-a51eb4a3c627",
            "userPrincipalName": "temp123@microsoft.com",
            "detectionStatus": null
        },
        {
            "entityType": "Process",
            "evidenceCreationTime": "2021-01-26T20:33:58.6133333Z",
            "sha1": "ff836cfb1af40252bd2a2ea843032e99a5b262ed",
            "sha256": "a4752c71d81afd3d5865d24ddb11a6b0c615062fcc448d24050c2172d2cbccd6",
            "fileName": "rundll32.exe",
            "filePath": "C:\\Windows\\SysWOW64",
            "processId": 3276,
            "processCommandLine": "rundll32.exe  c:\\temp\\suspicious.dll,RepeatAfterMe",
            "processCreationTime": "2021-01-26T20:31:32.9581596Z",
            "parentProcessId": 8420,
            "parentProcessCreationTime": "2021-01-26T20:31:32.9004163Z",
            "parentProcessFileName": "rundll32.exe",
            "parentProcessFilePath": "C:\\Windows\\System32",
            "ipAddress": null,
            "url": null,
            "registryKey": null,
            "registryHive": null,
            "registryValueType": null,
            "registryValue": null,
            "accountName": null,
            "domainName": null,
            "userSid": null,
            "aadUserId": null,
            "userPrincipalName": null,
            "detectionStatus": "Detected"
        },
        {
            "entityType": "File",
            "evidenceCreationTime": "2021-01-26T20:33:58.42Z",
            "sha1": "8563f95b2f8a284fc99da44500cd51a77c1ff36c",
            "sha256": "dc0ade0c95d6db98882bc8fa6707e64353cd6f7767ff48d6a81a6c2aef21c608",
            "fileName": "suspicious.dll",
            "filePath": "c:\\temp",
            "processId": null,
            "processCommandLine": null,
            "processCreationTime": null,
            "parentProcessId": null,
            "parentProcessCreationTime": null,
            "parentProcessFileName": null,
            "parentProcessFilePath": null,
            "ipAddress": null,
            "url": null,
            "registryKey": null,
            "registryHive": null,
            "registryValueType": null,
            "registryValue": null,
            "accountName": null,
            "domainName": null,
            "userSid": null,
            "aadUserId": null,
            "userPrincipalName": null,
            "detectionStatus": "Detected"
        }
    ]
}
```
