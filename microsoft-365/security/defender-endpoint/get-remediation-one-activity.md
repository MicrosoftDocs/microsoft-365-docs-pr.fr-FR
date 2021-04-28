---
title: Obtenir une activité de correction par ID
description: Renvoie des informations pour l'activité de correction spécifiée.
keywords: api, correction, api de correction, obtenir, tâches de correction, liste
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
ms.openlocfilehash: 40a7102a8c7dbf63641daaf47bbd9aa9f2e54649
ms.sourcegitcommit: e5b1a900043e2e41650ea1cbf4227043729c6053
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061131"
---
# <a name="get-one-remediation-activity-by-id"></a><span data-ttu-id="73acd-104">Obtenir une activité de correction par ID</span><span class="sxs-lookup"><span data-stu-id="73acd-104">Get one remediation activity by Id</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="73acd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="73acd-105">**Applies to:**</span></span>

- [<span data-ttu-id="73acd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="73acd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="73acd-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="73acd-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="73acd-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="73acd-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="73acd-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="73acd-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="73acd-110">Description de l'API</span><span class="sxs-lookup"><span data-stu-id="73acd-110">API description</span></span>

<span data-ttu-id="73acd-111">Renvoie des informations pour l'activité de correction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="73acd-111">Returns information for the specified remediation activity.</span></span> <span data-ttu-id="73acd-112">Présente les mêmes colonnes que [Obtenir toutes les](get-remediation-all-activities.md)activités de correction , mais renvoie les résultats uniquement pour l'activité de correction _spécifiée._</span><span class="sxs-lookup"><span data-stu-id="73acd-112">Presents the same columns as [Get all remediation activity](get-remediation-all-activities.md)", but returns results _only for the one specified remediation activity_.</span></span>

<span data-ttu-id="73acd-113">[En savoir plus sur les activités de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="73acd-113">[Learn more about remediation activities](tvm-remediation.md).</span></span>

## <a name="list-a-specified-remediation-activity-for-id"></a><span data-ttu-id="73acd-114">Liste d'une activité de correction spécifiée pour (id)</span><span class="sxs-lookup"><span data-stu-id="73acd-114">List a specified remediation activity for (id)</span></span>

<span data-ttu-id="73acd-115">**URL :** GET: /api/remediationTasks/id \{\}</span><span class="sxs-lookup"><span data-stu-id="73acd-115">**URL:** GET: /api/remediationTasks/\{id\}</span></span>

<span data-ttu-id="73acd-116">**Détails** des propriétés</span><span class="sxs-lookup"><span data-stu-id="73acd-116">**Properties** details</span></span>

<span data-ttu-id="73acd-117">Propriété (id)</span><span class="sxs-lookup"><span data-stu-id="73acd-117">Property (id)</span></span> | <span data-ttu-id="73acd-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="73acd-118">Data type</span></span> | <span data-ttu-id="73acd-119">Description</span><span class="sxs-lookup"><span data-stu-id="73acd-119">Description</span></span> | <span data-ttu-id="73acd-120">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="73acd-120">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="73acd-121">category</span><span class="sxs-lookup"><span data-stu-id="73acd-121">category</span></span> | <span data-ttu-id="73acd-122">String</span><span class="sxs-lookup"><span data-stu-id="73acd-122">String</span></span> | <span data-ttu-id="73acd-123">Catégorie de l'activité de correction (configuration logicielle/sécurité)</span><span class="sxs-lookup"><span data-stu-id="73acd-123">Category of the remediation activity (Software/Security configuration)</span></span> | <span data-ttu-id="73acd-124">Logiciels</span><span class="sxs-lookup"><span data-stu-id="73acd-124">Software</span></span>
<span data-ttu-id="73acd-125">completerEmail</span><span class="sxs-lookup"><span data-stu-id="73acd-125">completerEmail</span></span> | <span data-ttu-id="73acd-126">String</span><span class="sxs-lookup"><span data-stu-id="73acd-126">String</span></span> | <span data-ttu-id="73acd-127">Si l'activité de correction a été effectuée manuellement par une personne, cette colonne contient son courrier électronique</span><span class="sxs-lookup"><span data-stu-id="73acd-127">If the remediation activity was manually completed by someone, this column contains their email</span></span> | <span data-ttu-id="73acd-128">null</span><span class="sxs-lookup"><span data-stu-id="73acd-128">null</span></span>
<span data-ttu-id="73acd-129">completerId</span><span class="sxs-lookup"><span data-stu-id="73acd-129">completerId</span></span> | <span data-ttu-id="73acd-130">String</span><span class="sxs-lookup"><span data-stu-id="73acd-130">String</span></span> | <span data-ttu-id="73acd-131">Si l'activité de correction a été effectuée manuellement par une personne, cette colonne contient son ID d'objet</span><span class="sxs-lookup"><span data-stu-id="73acd-131">If the remediation activity was manually completed by someone, this column contains their object id</span></span> | <span data-ttu-id="73acd-132">null</span><span class="sxs-lookup"><span data-stu-id="73acd-132">null</span></span>
<span data-ttu-id="73acd-133">completionMethod</span><span class="sxs-lookup"><span data-stu-id="73acd-133">completionMethod</span></span> | <span data-ttu-id="73acd-134">String</span><span class="sxs-lookup"><span data-stu-id="73acd-134">String</span></span> | <span data-ttu-id="73acd-135">Une activité de correction peut être effectuée « automatiquement » (si tous les appareils sont corrigés) ou « manuellement » par une personne qui sélectionne « marquer comme terminé »</span><span class="sxs-lookup"><span data-stu-id="73acd-135">A remediation activity can be completed “automatically” (if all the devices are patched) or “manually” by a person who selects “mark as completed”</span></span> | <span data-ttu-id="73acd-136">Automatique</span><span class="sxs-lookup"><span data-stu-id="73acd-136">Automatic</span></span>
<span data-ttu-id="73acd-137">createdOn</span><span class="sxs-lookup"><span data-stu-id="73acd-137">createdOn</span></span> | <span data-ttu-id="73acd-138">Date/heure</span><span class="sxs-lookup"><span data-stu-id="73acd-138">DateTime</span></span> | <span data-ttu-id="73acd-139">Heure de création de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-139">Time this remediation activity was created</span></span> | <span data-ttu-id="73acd-140">2021-01-12T18:54:11.5499478Z</span><span class="sxs-lookup"><span data-stu-id="73acd-140">2021-01-12T18:54:11.5499478Z</span></span>
<span data-ttu-id="73acd-141">description</span><span class="sxs-lookup"><span data-stu-id="73acd-141">description</span></span> | <span data-ttu-id="73acd-142">String</span><span class="sxs-lookup"><span data-stu-id="73acd-142">String</span></span> | <span data-ttu-id="73acd-143">Description de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-143">Description of this remediation activity</span></span> | <span data-ttu-id="73acd-144">Mettez à jour Chrome vers une version ultérieure pour atténuer les vulnérabilités connues 1248 affectant vos appareils.</span><span class="sxs-lookup"><span data-stu-id="73acd-144">Update Chrome to a later version to mitigate 1248 known vulnerabilities affecting your devices.</span></span>
<span data-ttu-id="73acd-145">dueOn</span><span class="sxs-lookup"><span data-stu-id="73acd-145">dueOn</span></span> | <span data-ttu-id="73acd-146">Date/heure</span><span class="sxs-lookup"><span data-stu-id="73acd-146">DateTime</span></span> | <span data-ttu-id="73acd-147">Date d’échéance définie par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-147">Due date the creator set for this remediation activity</span></span> | <span data-ttu-id="73acd-148">2021-01-13T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="73acd-148">2021-01-13T00:00:00Z</span></span>
<span data-ttu-id="73acd-149">fixedDevices</span><span class="sxs-lookup"><span data-stu-id="73acd-149">fixedDevices</span></span> |  | <span data-ttu-id="73acd-150">Nombre d’appareils qui ont été corrigés</span><span class="sxs-lookup"><span data-stu-id="73acd-150">The number of devices that have been fixed</span></span> | <span data-ttu-id="73acd-151">2</span><span class="sxs-lookup"><span data-stu-id="73acd-151">2</span></span>
<span data-ttu-id="73acd-152">id</span><span class="sxs-lookup"><span data-stu-id="73acd-152">id</span></span> | <span data-ttu-id="73acd-153">String</span><span class="sxs-lookup"><span data-stu-id="73acd-153">String</span></span> | <span data-ttu-id="73acd-154">ID de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-154">ID of this remediation activity</span></span> | <span data-ttu-id="73acd-155">097d9735-5479-4899-b1b7-77398899df92</span><span class="sxs-lookup"><span data-stu-id="73acd-155">097d9735-5479-4899-b1b7-77398899df92</span></span>
<span data-ttu-id="73acd-156">nameId</span><span class="sxs-lookup"><span data-stu-id="73acd-156">nameId</span></span> | <span data-ttu-id="73acd-157">String</span><span class="sxs-lookup"><span data-stu-id="73acd-157">String</span></span> | <span data-ttu-id="73acd-158">Nom du produit associé</span><span class="sxs-lookup"><span data-stu-id="73acd-158">Related product name</span></span> | <span data-ttu-id="73acd-159">chrome</span><span class="sxs-lookup"><span data-stu-id="73acd-159">chrome</span></span>
<span data-ttu-id="73acd-160">priorité</span><span class="sxs-lookup"><span data-stu-id="73acd-160">priority</span></span> | <span data-ttu-id="73acd-161">String</span><span class="sxs-lookup"><span data-stu-id="73acd-161">String</span></span> | <span data-ttu-id="73acd-162">Priorité définie par le créateur pour cette activité de correction (High\Medium\Low)</span><span class="sxs-lookup"><span data-stu-id="73acd-162">Priority the creator set for this remediation activity (High\Medium\Low)</span></span> | <span data-ttu-id="73acd-163">Élevé</span><span class="sxs-lookup"><span data-stu-id="73acd-163">High</span></span>
<span data-ttu-id="73acd-164">productId</span><span class="sxs-lookup"><span data-stu-id="73acd-164">productId</span></span> | <span data-ttu-id="73acd-165">String</span><span class="sxs-lookup"><span data-stu-id="73acd-165">String</span></span> | <span data-ttu-id="73acd-166">ID de produit associé</span><span class="sxs-lookup"><span data-stu-id="73acd-166">Related product ID</span></span> | <span data-ttu-id="73acd-167">google-_-chrome</span><span class="sxs-lookup"><span data-stu-id="73acd-167">google-_-chrome</span></span>
<span data-ttu-id="73acd-168">productivityImpactRemediationType</span><span class="sxs-lookup"><span data-stu-id="73acd-168">productivityImpactRemediationType</span></span> | <span data-ttu-id="73acd-169">String</span><span class="sxs-lookup"><span data-stu-id="73acd-169">String</span></span> | <span data-ttu-id="73acd-170">Quelques modifications de configuration peuvent être demandées uniquement pour les appareils sans impact sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="73acd-170">A few configuration changes could be requested only for devices with no user impact.</span></span> <span data-ttu-id="73acd-171">Cette valeur indique la sélection entre « tous les appareils exposés » ou « uniquement les appareils sans impact sur l’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="73acd-171">This value indicate the selection between “all exposed devices” or “only devices with no user impact.”</span></span> | <span data-ttu-id="73acd-172">AllExposedAssets</span><span class="sxs-lookup"><span data-stu-id="73acd-172">AllExposedAssets</span></span>
<span data-ttu-id="73acd-173">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="73acd-173">rbacGroupNames</span></span> | <span data-ttu-id="73acd-174">String</span><span class="sxs-lookup"><span data-stu-id="73acd-174">String</span></span> | <span data-ttu-id="73acd-175">Noms de groupes d’appareils associés</span><span class="sxs-lookup"><span data-stu-id="73acd-175">Related device group names</span></span> | <span data-ttu-id="73acd-176">[ « Windows Servers », « Windows 10 » ]</span><span class="sxs-lookup"><span data-stu-id="73acd-176">[ "Windows Servers", "Windows 10" ]</span></span>
<span data-ttu-id="73acd-177">recommendedProgram</span><span class="sxs-lookup"><span data-stu-id="73acd-177">recommendedProgram</span></span> | <span data-ttu-id="73acd-178">String</span><span class="sxs-lookup"><span data-stu-id="73acd-178">String</span></span> | <span data-ttu-id="73acd-179">Programme recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="73acd-179">Recommended program to upgrade to</span></span> | <span data-ttu-id="73acd-180">null</span><span class="sxs-lookup"><span data-stu-id="73acd-180">null</span></span>
<span data-ttu-id="73acd-181">recommendedVendor</span><span class="sxs-lookup"><span data-stu-id="73acd-181">recommendedVendor</span></span> | <span data-ttu-id="73acd-182">String</span><span class="sxs-lookup"><span data-stu-id="73acd-182">String</span></span> | <span data-ttu-id="73acd-183">Fournisseur recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="73acd-183">Recommended vendor to upgrade to</span></span> | <span data-ttu-id="73acd-184">null</span><span class="sxs-lookup"><span data-stu-id="73acd-184">null</span></span>
<span data-ttu-id="73acd-185">recommendedVersion</span><span class="sxs-lookup"><span data-stu-id="73acd-185">recommendedVersion</span></span> | <span data-ttu-id="73acd-186">String</span><span class="sxs-lookup"><span data-stu-id="73acd-186">String</span></span> | <span data-ttu-id="73acd-187">Version recommandée pour la mise à jour/mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="73acd-187">Recommended version to update/upgrade to</span></span> | <span data-ttu-id="73acd-188">null</span><span class="sxs-lookup"><span data-stu-id="73acd-188">null</span></span>
<span data-ttu-id="73acd-189">relatedComponent</span><span class="sxs-lookup"><span data-stu-id="73acd-189">relatedComponent</span></span> | <span data-ttu-id="73acd-190">String</span><span class="sxs-lookup"><span data-stu-id="73acd-190">String</span></span> | <span data-ttu-id="73acd-191">Composant connexe de cette activité de correction (similaire au composant associé pour une recommandation de sécurité)</span><span class="sxs-lookup"><span data-stu-id="73acd-191">Related component of this remediation activity (similar to the related component for a security recommendation)</span></span> | <span data-ttu-id="73acd-192">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="73acd-192">Google Chrome</span></span>
<span data-ttu-id="73acd-193">requesterEmail</span><span class="sxs-lookup"><span data-stu-id="73acd-193">requesterEmail</span></span> | <span data-ttu-id="73acd-194">String</span><span class="sxs-lookup"><span data-stu-id="73acd-194">String</span></span> | <span data-ttu-id="73acd-195">Adresse de messagerie du créateur</span><span class="sxs-lookup"><span data-stu-id="73acd-195">Creator email address</span></span> | <span data-ttu-id="73acd-196">globaladmin@UserName.contoso.com</span><span class="sxs-lookup"><span data-stu-id="73acd-196">globaladmin@UserName.contoso.com</span></span>
<span data-ttu-id="73acd-197">requesterId</span><span class="sxs-lookup"><span data-stu-id="73acd-197">requesterId</span></span> | <span data-ttu-id="73acd-198">String</span><span class="sxs-lookup"><span data-stu-id="73acd-198">String</span></span> | <span data-ttu-id="73acd-199">ID d’objet Creator</span><span class="sxs-lookup"><span data-stu-id="73acd-199">Creator object id</span></span> | <span data-ttu-id="73acd-200">r647211f-2e16-43f2-a480-16ar3a2a796r</span><span class="sxs-lookup"><span data-stu-id="73acd-200">r647211f-2e16-43f2-a480-16ar3a2a796r</span></span>
<span data-ttu-id="73acd-201">requesterNotes</span><span class="sxs-lookup"><span data-stu-id="73acd-201">requesterNotes</span></span> | <span data-ttu-id="73acd-202">String</span><span class="sxs-lookup"><span data-stu-id="73acd-202">String</span></span> | <span data-ttu-id="73acd-203">Notes (texte libre) ajoutées par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-203">The notes (free text) the creator added for this remediation activity</span></span> | <span data-ttu-id="73acd-204">null</span><span class="sxs-lookup"><span data-stu-id="73acd-204">null</span></span>
<span data-ttu-id="73acd-205">scid</span><span class="sxs-lookup"><span data-stu-id="73acd-205">scid</span></span> | <span data-ttu-id="73acd-206">String</span><span class="sxs-lookup"><span data-stu-id="73acd-206">String</span></span> | <span data-ttu-id="73acd-207">SCID de la recommandation de sécurité associée</span><span class="sxs-lookup"><span data-stu-id="73acd-207">SCID of the related security recommendation</span></span> | <span data-ttu-id="73acd-208">null</span><span class="sxs-lookup"><span data-stu-id="73acd-208">null</span></span>
<span data-ttu-id="73acd-209">status</span><span class="sxs-lookup"><span data-stu-id="73acd-209">status</span></span> | <span data-ttu-id="73acd-210">String</span><span class="sxs-lookup"><span data-stu-id="73acd-210">String</span></span> | <span data-ttu-id="73acd-211">État de l’activité de correction (actif/terminé)</span><span class="sxs-lookup"><span data-stu-id="73acd-211">Remediation activity status (Active/Completed)</span></span> | <span data-ttu-id="73acd-212">Actif</span><span class="sxs-lookup"><span data-stu-id="73acd-212">Active</span></span>
<span data-ttu-id="73acd-213">statusLastModifiedOn</span><span class="sxs-lookup"><span data-stu-id="73acd-213">statusLastModifiedOn</span></span> | <span data-ttu-id="73acd-214">Date/heure</span><span class="sxs-lookup"><span data-stu-id="73acd-214">DateTime</span></span> | <span data-ttu-id="73acd-215">Date de mise à jour du champ d’état</span><span class="sxs-lookup"><span data-stu-id="73acd-215">Date when the status field was updated</span></span> | <span data-ttu-id="73acd-216">2021-01-12T18:54:11.5499487Z</span><span class="sxs-lookup"><span data-stu-id="73acd-216">2021-01-12T18:54:11.5499487Z</span></span>
<span data-ttu-id="73acd-217">targetDevices</span><span class="sxs-lookup"><span data-stu-id="73acd-217">targetDevices</span></span> | <span data-ttu-id="73acd-218">Entier long</span><span class="sxs-lookup"><span data-stu-id="73acd-218">Long</span></span> | <span data-ttu-id="73acd-219">Nombre d’appareils exposés à appliquer à cette correction</span><span class="sxs-lookup"><span data-stu-id="73acd-219">Number of exposed devices that this remediation is applicable to</span></span> | <span data-ttu-id="73acd-220">43</span><span class="sxs-lookup"><span data-stu-id="73acd-220">43</span></span>
<span data-ttu-id="73acd-221">title</span><span class="sxs-lookup"><span data-stu-id="73acd-221">title</span></span> | <span data-ttu-id="73acd-222">String</span><span class="sxs-lookup"><span data-stu-id="73acd-222">String</span></span> | <span data-ttu-id="73acd-223">Titre de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-223">Title of this remediation activity</span></span> | <span data-ttu-id="73acd-224">Mettre à jour Google Chrome</span><span class="sxs-lookup"><span data-stu-id="73acd-224">Update Google Chrome</span></span>
<span data-ttu-id="73acd-225">type</span><span class="sxs-lookup"><span data-stu-id="73acd-225">type</span></span> | <span data-ttu-id="73acd-226">String</span><span class="sxs-lookup"><span data-stu-id="73acd-226">String</span></span> | <span data-ttu-id="73acd-227">Type de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-227">Remediation type</span></span> | <span data-ttu-id="73acd-228">Update</span><span class="sxs-lookup"><span data-stu-id="73acd-228">Update</span></span>
<span data-ttu-id="73acd-229">vendorId</span><span class="sxs-lookup"><span data-stu-id="73acd-229">vendorId</span></span> | <span data-ttu-id="73acd-230">String</span><span class="sxs-lookup"><span data-stu-id="73acd-230">String</span></span> | <span data-ttu-id="73acd-231">Nom du fournisseur associé</span><span class="sxs-lookup"><span data-stu-id="73acd-231">Related vendor name</span></span> | <span data-ttu-id="73acd-232">google</span><span class="sxs-lookup"><span data-stu-id="73acd-232">google</span></span>

## <a name="example"></a><span data-ttu-id="73acd-233">Exemple</span><span class="sxs-lookup"><span data-stu-id="73acd-233">Example</span></span>

<span data-ttu-id="73acd-234">**Exemple de** requête</span><span class="sxs-lookup"><span data-stu-id="73acd-234">**Request** example</span></span>

```http
GET https://api-luna.securitycenter.windows.com/api/remediationtasks/03942ef5-aecb-4c6e-b555-d6a97013844c
```

<span data-ttu-id="73acd-235">**Exemple de** réponse</span><span class="sxs-lookup"><span data-stu-id="73acd-235">**Response** example</span></span>

```json
{ 
    "@odata.context": "https://wpatdadi-luna-stg.cloudapp.net/api/$metadata#RemediationTasks/$entity", 
    "id": "03942ef5-aecb-4c6e-b555-d6a97013844c", 
    "title": "Update Microsoft Silverlight", 
    "createdOn": "2021-02-10T13:20:36.4718166Z", 
    "requesterId": "65548a1d-efo0-4a7a-8d19-1b967b5c36f4", 
    "requesterEmail": "user1@contoso.com", 
    "status": "Active", 
    "statusLastModifiedOn": "2021-02-10T13:20:36.4719698Z", 
    "description": "Update Silverlight to a later version to mitigate 55 known vulnerabilities affecting your devices. Doing so can help lessen the security risk to your organization due to versions which have reached their end-of-support.  ", 
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
```

## <a name="see-also"></a><span data-ttu-id="73acd-236">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73acd-236">See also</span></span>

- [<span data-ttu-id="73acd-237">Méthodes et propriétés de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-237">Remediation methods and properties</span></span>](get-remediation-methods-properties.md)

- [<span data-ttu-id="73acd-238">Liste de toutes les activités de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-238">List all remediation activities</span></span>](get-remediation-all-activities.md)

- [<span data-ttu-id="73acd-239">Liste des appareils exposés d'une activité de correction</span><span class="sxs-lookup"><span data-stu-id="73acd-239">List exposed devices of one remediation activity</span></span>](get-remediation-exposed-devices-activities.md)

- [<span data-ttu-id="73acd-240">Gestion des menaces basée sur & les vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="73acd-240">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="73acd-241">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="73acd-241">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
