---
title: Liste de toutes les activités de correction
description: Retourne des informations sur toutes les activités de correction.
keywords: api, correction, api de correction, obtenir, tâches de correction,
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: v-jweston
author: jweston-1
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: ac4a777136dcdfc5d7ab61ddc8d496b7452f69e2
ms.sourcegitcommit: e5b1a900043e2e41650ea1cbf4227043729c6053
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061128"
---
# <a name="list-all-remediation-activities"></a><span data-ttu-id="e0845-104">Liste de toutes les activités de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-104">List all remediation activities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e0845-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e0845-105">**Applies to:**</span></span>

- [<span data-ttu-id="e0845-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e0845-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="e0845-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e0845-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="e0845-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="e0845-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="e0845-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e0845-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="e0845-110">Description de l'API</span><span class="sxs-lookup"><span data-stu-id="e0845-110">API description</span></span>

<span data-ttu-id="e0845-111">Retourne des informations sur toutes les activités de correction.</span><span class="sxs-lookup"><span data-stu-id="e0845-111">Returns information about all remediation activities.</span></span>

<span data-ttu-id="e0845-112">[En savoir plus sur les activités de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="e0845-112">[Learn more about remediation activities](tvm-remediation.md).</span></span>

<span data-ttu-id="e0845-113">**URL :** GET: /api/remediationTasks</span><span class="sxs-lookup"><span data-stu-id="e0845-113">**URL:** GET: /api/remediationTasks</span></span>

<span data-ttu-id="e0845-114">**Détails** des propriétés</span><span class="sxs-lookup"><span data-stu-id="e0845-114">**Properties** details</span></span>

<span data-ttu-id="e0845-115">Propriété (id)</span><span class="sxs-lookup"><span data-stu-id="e0845-115">Property (id)</span></span> | <span data-ttu-id="e0845-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="e0845-116">Data type</span></span> | <span data-ttu-id="e0845-117">Description</span><span class="sxs-lookup"><span data-stu-id="e0845-117">Description</span></span> | <span data-ttu-id="e0845-118">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e0845-118">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="e0845-119">category</span><span class="sxs-lookup"><span data-stu-id="e0845-119">category</span></span> | <span data-ttu-id="e0845-120">String</span><span class="sxs-lookup"><span data-stu-id="e0845-120">String</span></span> | <span data-ttu-id="e0845-121">Catégorie de l'activité de correction (configuration logicielle/sécurité)</span><span class="sxs-lookup"><span data-stu-id="e0845-121">Category of the remediation activity (Software/Security configuration)</span></span> | <span data-ttu-id="e0845-122">Logiciels</span><span class="sxs-lookup"><span data-stu-id="e0845-122">Software</span></span>
<span data-ttu-id="e0845-123">completerEmail</span><span class="sxs-lookup"><span data-stu-id="e0845-123">completerEmail</span></span> | <span data-ttu-id="e0845-124">String</span><span class="sxs-lookup"><span data-stu-id="e0845-124">String</span></span> | <span data-ttu-id="e0845-125">Si l'activité de correction a été effectuée manuellement par une personne, cette colonne contient son courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e0845-125">If the remediation activity was manually completed by someone, this column contains their email</span></span> | <span data-ttu-id="e0845-126">null</span><span class="sxs-lookup"><span data-stu-id="e0845-126">null</span></span>
<span data-ttu-id="e0845-127">completerId</span><span class="sxs-lookup"><span data-stu-id="e0845-127">completerId</span></span> | <span data-ttu-id="e0845-128">String</span><span class="sxs-lookup"><span data-stu-id="e0845-128">String</span></span> | <span data-ttu-id="e0845-129">Si l'activité de correction a été effectuée manuellement par une personne, cette colonne contient son ID d'objet</span><span class="sxs-lookup"><span data-stu-id="e0845-129">If the remediation activity was manually completed by someone, this column contains their object id</span></span> | <span data-ttu-id="e0845-130">null</span><span class="sxs-lookup"><span data-stu-id="e0845-130">null</span></span>
<span data-ttu-id="e0845-131">completionMethod</span><span class="sxs-lookup"><span data-stu-id="e0845-131">completionMethod</span></span> | <span data-ttu-id="e0845-132">String</span><span class="sxs-lookup"><span data-stu-id="e0845-132">String</span></span> | <span data-ttu-id="e0845-133">Une activité de correction peut être effectuée « automatiquement » (si tous les appareils sont corrigés) ou « manuellement » par une personne qui sélectionne « marquer comme terminé »</span><span class="sxs-lookup"><span data-stu-id="e0845-133">A remediation activity can be completed “automatically” (if all the devices are patched) or “manually” by a person who selects “mark as completed”</span></span> | <span data-ttu-id="e0845-134">Automatique</span><span class="sxs-lookup"><span data-stu-id="e0845-134">Automatic</span></span>
<span data-ttu-id="e0845-135">createdOn</span><span class="sxs-lookup"><span data-stu-id="e0845-135">createdOn</span></span> | <span data-ttu-id="e0845-136">Date/heure</span><span class="sxs-lookup"><span data-stu-id="e0845-136">DateTime</span></span> | <span data-ttu-id="e0845-137">Heure de création de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-137">Time this remediation activity was created</span></span> | <span data-ttu-id="e0845-138">2021-01-12T18:54:11.5499478Z</span><span class="sxs-lookup"><span data-stu-id="e0845-138">2021-01-12T18:54:11.5499478Z</span></span>
<span data-ttu-id="e0845-139">description</span><span class="sxs-lookup"><span data-stu-id="e0845-139">description</span></span> | <span data-ttu-id="e0845-140">String</span><span class="sxs-lookup"><span data-stu-id="e0845-140">String</span></span> | <span data-ttu-id="e0845-141">Description de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-141">Description of this remediation activity</span></span> | <span data-ttu-id="e0845-142">Mettez à jour Chrome vers une version ultérieure pour atténuer les vulnérabilités connues 1248 affectant vos appareils.</span><span class="sxs-lookup"><span data-stu-id="e0845-142">Update Chrome to a later version to mitigate 1248 known vulnerabilities affecting your devices.</span></span>
<span data-ttu-id="e0845-143">dueOn</span><span class="sxs-lookup"><span data-stu-id="e0845-143">dueOn</span></span> | <span data-ttu-id="e0845-144">Date/heure</span><span class="sxs-lookup"><span data-stu-id="e0845-144">DateTime</span></span> | <span data-ttu-id="e0845-145">Date d’échéance définie par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-145">Due date the creator set for this remediation activity</span></span> | <span data-ttu-id="e0845-146">2021-01-13T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="e0845-146">2021-01-13T00:00:00Z</span></span>
<span data-ttu-id="e0845-147">fixedDevices</span><span class="sxs-lookup"><span data-stu-id="e0845-147">fixedDevices</span></span> | <span data-ttu-id="e0845-148">.</span><span class="sxs-lookup"><span data-stu-id="e0845-148">.</span></span> | <span data-ttu-id="e0845-149">Nombre d’appareils qui ont été corrigés</span><span class="sxs-lookup"><span data-stu-id="e0845-149">The number of devices that have been fixed</span></span> | <span data-ttu-id="e0845-150">2</span><span class="sxs-lookup"><span data-stu-id="e0845-150">2</span></span>
<span data-ttu-id="e0845-151">id</span><span class="sxs-lookup"><span data-stu-id="e0845-151">id</span></span> | <span data-ttu-id="e0845-152">String</span><span class="sxs-lookup"><span data-stu-id="e0845-152">String</span></span> | <span data-ttu-id="e0845-153">ID de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-153">ID of this remediation activity</span></span> | <span data-ttu-id="e0845-154">097d9735-5479-4899-b1b7-77398899df92</span><span class="sxs-lookup"><span data-stu-id="e0845-154">097d9735-5479-4899-b1b7-77398899df92</span></span>
<span data-ttu-id="e0845-155">nameId</span><span class="sxs-lookup"><span data-stu-id="e0845-155">nameId</span></span> | <span data-ttu-id="e0845-156">String</span><span class="sxs-lookup"><span data-stu-id="e0845-156">String</span></span> | <span data-ttu-id="e0845-157">Nom du produit associé</span><span class="sxs-lookup"><span data-stu-id="e0845-157">Related product name</span></span> | <span data-ttu-id="e0845-158">chrome</span><span class="sxs-lookup"><span data-stu-id="e0845-158">chrome</span></span>
<span data-ttu-id="e0845-159">priorité</span><span class="sxs-lookup"><span data-stu-id="e0845-159">priority</span></span> | <span data-ttu-id="e0845-160">String</span><span class="sxs-lookup"><span data-stu-id="e0845-160">String</span></span> | <span data-ttu-id="e0845-161">Priorité définie par le créateur pour cette activité de correction (High\Medium\Low)</span><span class="sxs-lookup"><span data-stu-id="e0845-161">Priority the creator set for this remediation activity (High\Medium\Low)</span></span> | <span data-ttu-id="e0845-162">Élevé</span><span class="sxs-lookup"><span data-stu-id="e0845-162">High</span></span>
<span data-ttu-id="e0845-163">productId</span><span class="sxs-lookup"><span data-stu-id="e0845-163">productId</span></span> | <span data-ttu-id="e0845-164">String</span><span class="sxs-lookup"><span data-stu-id="e0845-164">String</span></span> | <span data-ttu-id="e0845-165">ID de produit associé</span><span class="sxs-lookup"><span data-stu-id="e0845-165">Related product ID</span></span> | <span data-ttu-id="e0845-166">google-_-chrome</span><span class="sxs-lookup"><span data-stu-id="e0845-166">google-_-chrome</span></span>
<span data-ttu-id="e0845-167">productivityImpactRemediationType</span><span class="sxs-lookup"><span data-stu-id="e0845-167">productivityImpactRemediationType</span></span> | <span data-ttu-id="e0845-168">String</span><span class="sxs-lookup"><span data-stu-id="e0845-168">String</span></span> | <span data-ttu-id="e0845-169">Quelques modifications de configuration peuvent être demandées uniquement pour les appareils sans impact sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e0845-169">A few configuration changes could be requested only for devices with no user impact.</span></span> <span data-ttu-id="e0845-170">Cette valeur indique la sélection entre « tous les appareils exposés » ou « uniquement les appareils sans impact sur l’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="e0845-170">This value indicate the selection between “all exposed devices” or “only devices with no user impact.”</span></span> | <span data-ttu-id="e0845-171">AllExposedAssets</span><span class="sxs-lookup"><span data-stu-id="e0845-171">AllExposedAssets</span></span>
<span data-ttu-id="e0845-172">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="e0845-172">rbacGroupNames</span></span> | <span data-ttu-id="e0845-173">String</span><span class="sxs-lookup"><span data-stu-id="e0845-173">String</span></span> | <span data-ttu-id="e0845-174">Noms de groupes d’appareils associés</span><span class="sxs-lookup"><span data-stu-id="e0845-174">Related device group names</span></span> | <span data-ttu-id="e0845-175">[ « Windows Servers », « Windows 10 » ]</span><span class="sxs-lookup"><span data-stu-id="e0845-175">[ "Windows Servers", "Windows 10" ]</span></span>
<span data-ttu-id="e0845-176">recommendedProgram</span><span class="sxs-lookup"><span data-stu-id="e0845-176">recommendedProgram</span></span> | <span data-ttu-id="e0845-177">String</span><span class="sxs-lookup"><span data-stu-id="e0845-177">String</span></span> | <span data-ttu-id="e0845-178">Programme recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="e0845-178">Recommended program to upgrade to</span></span> | <span data-ttu-id="e0845-179">null</span><span class="sxs-lookup"><span data-stu-id="e0845-179">null</span></span>
<span data-ttu-id="e0845-180">recommendedVendor</span><span class="sxs-lookup"><span data-stu-id="e0845-180">recommendedVendor</span></span> | <span data-ttu-id="e0845-181">String</span><span class="sxs-lookup"><span data-stu-id="e0845-181">String</span></span> | <span data-ttu-id="e0845-182">Fournisseur recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="e0845-182">Recommended vendor to upgrade to</span></span> | <span data-ttu-id="e0845-183">null</span><span class="sxs-lookup"><span data-stu-id="e0845-183">null</span></span>
<span data-ttu-id="e0845-184">recommendedVersion</span><span class="sxs-lookup"><span data-stu-id="e0845-184">recommendedVersion</span></span> | <span data-ttu-id="e0845-185">String</span><span class="sxs-lookup"><span data-stu-id="e0845-185">String</span></span> | <span data-ttu-id="e0845-186">Version recommandée pour la mise à jour/mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="e0845-186">Recommended version to update/upgrade to</span></span> | <span data-ttu-id="e0845-187">null</span><span class="sxs-lookup"><span data-stu-id="e0845-187">null</span></span>
<span data-ttu-id="e0845-188">relatedComponent</span><span class="sxs-lookup"><span data-stu-id="e0845-188">relatedComponent</span></span> | <span data-ttu-id="e0845-189">String</span><span class="sxs-lookup"><span data-stu-id="e0845-189">String</span></span> | <span data-ttu-id="e0845-190">Composant connexe de cette activité de correction (similaire au composant associé pour une recommandation de sécurité)</span><span class="sxs-lookup"><span data-stu-id="e0845-190">Related component of this remediation activity (similar to the related component for a security recommendation)</span></span> | <span data-ttu-id="e0845-191">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="e0845-191">Google Chrome</span></span>
<span data-ttu-id="e0845-192">requesterEmail</span><span class="sxs-lookup"><span data-stu-id="e0845-192">requesterEmail</span></span> | <span data-ttu-id="e0845-193">String</span><span class="sxs-lookup"><span data-stu-id="e0845-193">String</span></span> | <span data-ttu-id="e0845-194">Adresse de messagerie du créateur</span><span class="sxs-lookup"><span data-stu-id="e0845-194">Creator email address</span></span> | <span data-ttu-id="e0845-195">globaladmin@UserName.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e0845-195">globaladmin@UserName.contoso.com</span></span>
<span data-ttu-id="e0845-196">requesterId</span><span class="sxs-lookup"><span data-stu-id="e0845-196">requesterId</span></span> | <span data-ttu-id="e0845-197">String</span><span class="sxs-lookup"><span data-stu-id="e0845-197">String</span></span> | <span data-ttu-id="e0845-198">ID d'objet Creator</span><span class="sxs-lookup"><span data-stu-id="e0845-198">Creator object id</span></span> | <span data-ttu-id="e0845-199">r647211f-2e16-43f2-a480-16ar3a2a796r</span><span class="sxs-lookup"><span data-stu-id="e0845-199">r647211f-2e16-43f2-a480-16ar3a2a796r</span></span>
<span data-ttu-id="e0845-200">requesterNotes</span><span class="sxs-lookup"><span data-stu-id="e0845-200">requesterNotes</span></span> | <span data-ttu-id="e0845-201">String</span><span class="sxs-lookup"><span data-stu-id="e0845-201">String</span></span> | <span data-ttu-id="e0845-202">Notes (texte libre) ajoutées par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-202">The notes (free text) the creator added for this remediation activity</span></span> | <span data-ttu-id="e0845-203">null</span><span class="sxs-lookup"><span data-stu-id="e0845-203">null</span></span>
<span data-ttu-id="e0845-204">scid</span><span class="sxs-lookup"><span data-stu-id="e0845-204">scid</span></span> | <span data-ttu-id="e0845-205">String</span><span class="sxs-lookup"><span data-stu-id="e0845-205">String</span></span> | <span data-ttu-id="e0845-206">SCID de la recommandation de sécurité associée</span><span class="sxs-lookup"><span data-stu-id="e0845-206">SCID of the related security recommendation</span></span> | <span data-ttu-id="e0845-207">null</span><span class="sxs-lookup"><span data-stu-id="e0845-207">null</span></span>
<span data-ttu-id="e0845-208">status</span><span class="sxs-lookup"><span data-stu-id="e0845-208">status</span></span> | <span data-ttu-id="e0845-209">String</span><span class="sxs-lookup"><span data-stu-id="e0845-209">String</span></span> | <span data-ttu-id="e0845-210">État de l'activité de correction (actif/terminé)</span><span class="sxs-lookup"><span data-stu-id="e0845-210">Remediation activity status (Active/Completed)</span></span> | <span data-ttu-id="e0845-211">Actif</span><span class="sxs-lookup"><span data-stu-id="e0845-211">Active</span></span>
<span data-ttu-id="e0845-212">statusLastModifiedOn</span><span class="sxs-lookup"><span data-stu-id="e0845-212">statusLastModifiedOn</span></span> | <span data-ttu-id="e0845-213">Date/heure</span><span class="sxs-lookup"><span data-stu-id="e0845-213">DateTime</span></span> | <span data-ttu-id="e0845-214">Date de mise à jour du champ d'état</span><span class="sxs-lookup"><span data-stu-id="e0845-214">Date when the status field was updated</span></span> | <span data-ttu-id="e0845-215">2021-01-12T18:54:11.5499487Z</span><span class="sxs-lookup"><span data-stu-id="e0845-215">2021-01-12T18:54:11.5499487Z</span></span>
<span data-ttu-id="e0845-216">targetDevices</span><span class="sxs-lookup"><span data-stu-id="e0845-216">targetDevices</span></span> | <span data-ttu-id="e0845-217">Entier long</span><span class="sxs-lookup"><span data-stu-id="e0845-217">Long</span></span> | <span data-ttu-id="e0845-218">Nombre d'appareils exposés pour qui cette correction s'applique</span><span class="sxs-lookup"><span data-stu-id="e0845-218">Number of exposed devices that this remediation is applicable to</span></span> | <span data-ttu-id="e0845-219">43</span><span class="sxs-lookup"><span data-stu-id="e0845-219">43</span></span>
<span data-ttu-id="e0845-220">title</span><span class="sxs-lookup"><span data-stu-id="e0845-220">title</span></span> | <span data-ttu-id="e0845-221">String</span><span class="sxs-lookup"><span data-stu-id="e0845-221">String</span></span> | <span data-ttu-id="e0845-222">Titre de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-222">Title of this remediation activity</span></span> | <span data-ttu-id="e0845-223">Mettre à jour Google Chrome</span><span class="sxs-lookup"><span data-stu-id="e0845-223">Update Google Chrome</span></span>
<span data-ttu-id="e0845-224">type</span><span class="sxs-lookup"><span data-stu-id="e0845-224">type</span></span> | <span data-ttu-id="e0845-225">String</span><span class="sxs-lookup"><span data-stu-id="e0845-225">String</span></span> | <span data-ttu-id="e0845-226">Type de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-226">Remediation type</span></span> | <span data-ttu-id="e0845-227">Update</span><span class="sxs-lookup"><span data-stu-id="e0845-227">Update</span></span>
<span data-ttu-id="e0845-228">vendorId</span><span class="sxs-lookup"><span data-stu-id="e0845-228">vendorId</span></span> | <span data-ttu-id="e0845-229">String</span><span class="sxs-lookup"><span data-stu-id="e0845-229">String</span></span> | <span data-ttu-id="e0845-230">Nom du fournisseur associé</span><span class="sxs-lookup"><span data-stu-id="e0845-230">Related vendor name</span></span> | <span data-ttu-id="e0845-231">google</span><span class="sxs-lookup"><span data-stu-id="e0845-231">google</span></span>

## <a name="example"></a><span data-ttu-id="e0845-232">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0845-232">Example</span></span>

<span data-ttu-id="e0845-233">**Exemple de** requête</span><span class="sxs-lookup"><span data-stu-id="e0845-233">**Request** example</span></span>

```http
GET https://api-luna.securitycenter.windows.com/api/remediationtasks/
```

<span data-ttu-id="e0845-234">**Exemple de** réponse</span><span class="sxs-lookup"><span data-stu-id="e0845-234">**Response** example</span></span>

```json
{
    "@odata.context": "https://wpatdadi-luna-stg.cloudapp.net/api/$metadata#RemediationTasks",
    "value": [
        {
            "id": "03942ef5-aewb-4w6e-b555-d6a97013844w",
            "title": "Update Microsoft Silverlight",
            "createdOn": "2021-02-10T13:20:36.4718166Z",
            "requesterId": "65548a1d-ef00-4a7a-8d19-1b967b5c36f4",
            "requesterEmail": "user1@contoso.com",
            "status": "Active",
            "statusLastModifiedOn": "2021-02-10T13:20:36.4719698Z",
            "description": "Update Silverlight to a later version  to mitigate 55 known vulnerabilities affecting your devices. Doing so can help lessen the security risk to your organization due to versions which have reached their end-of-support.  ",
            "relatedComponent": "Microsoft Silverlight",
            "targetDevices": 18511,
            "rbacGroupNames": [
                "UnassignedGroup",
                "hhh"
            ],
            "fixedDevices": 2866,
            "requesterNotes": "test",
            "dueOn": "2021-02-11T00:00:00Z",
            "category": "Software",
            "productivityImpactRemediationType": null,
            "priority": "Medium",
            "completionMethod": null,
            "completerId": null,
            "completerEmail": null,
            "scid": null,
            "type": "Update",
            "productId": "microsoft-_-silverlight",
            "vendorId": "microsoft",
            "nameId": "silverlight",
            "recommendedVersion": null,
            "recommendedVendor": null,
            "recommendedProgram": null
        }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="e0845-235">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0845-235">See also</span></span>

- [<span data-ttu-id="e0845-236">Méthodes et propriétés de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-236">Remediation methods and properties</span></span>](get-remediation-methods-properties.md)

- [<span data-ttu-id="e0845-237">Obtenir une activité de correction par ID</span><span class="sxs-lookup"><span data-stu-id="e0845-237">Get one remediation activity by Id</span></span>](get-remediation-one-activity.md)

- [<span data-ttu-id="e0845-238">Liste des appareils exposés d'une activité de correction</span><span class="sxs-lookup"><span data-stu-id="e0845-238">List exposed devices of one remediation activity</span></span>](get-remediation-exposed-devices-activities.md)

- [<span data-ttu-id="e0845-239">Gestion des menaces basée sur & les vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e0845-239">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="e0845-240">Vulnérabilités de votre organisation</span><span class="sxs-lookup"><span data-stu-id="e0845-240">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
