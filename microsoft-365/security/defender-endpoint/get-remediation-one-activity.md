---
title: Obtenir une activité de correction par son ID
description: Renvoie des informations pour l’activité de correction spécifiée.
keywords: api, correction, api de correction, obtenir, tâches de correction, correction par ID,
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
ms.openlocfilehash: e0f68e8a28b302f0ae1ca06a2f892fea38a219b2
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52244442"
---
# <a name="get-one-remediation-activity-by-id"></a><span data-ttu-id="53055-104">Obtenir une activité de correction par son ID</span><span class="sxs-lookup"><span data-stu-id="53055-104">Get one remediation activity by Id</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="53055-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="53055-105">**Applies to:**</span></span>

- [<span data-ttu-id="53055-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="53055-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="53055-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="53055-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="53055-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="53055-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="53055-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="53055-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="53055-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="53055-110">API description</span></span>

<span data-ttu-id="53055-111">Renvoie des informations pour l’activité de correction spécifiée.</span><span class="sxs-lookup"><span data-stu-id="53055-111">Returns information for the specified remediation activity.</span></span> <span data-ttu-id="53055-112">Présente les mêmes colonnes que [Obtenir toutes les](get-remediation-all-activities.md)activités de correction , mais renvoie des résultats uniquement pour l’activité de correction _spécifiée._</span><span class="sxs-lookup"><span data-stu-id="53055-112">Presents the same columns as [Get all remediation activity](get-remediation-all-activities.md)", but returns results _only for the one specified remediation activity_.</span></span>

<span data-ttu-id="53055-113">[En savoir plus sur les activités de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="53055-113">[Learn more about remediation activities](tvm-remediation.md).</span></span>

## <a name="list-a-specified-remediation-activity-for-id"></a><span data-ttu-id="53055-114">Liste d’une activité de correction spécifiée pour (id)</span><span class="sxs-lookup"><span data-stu-id="53055-114">List a specified remediation activity for (id)</span></span>

<span data-ttu-id="53055-115">**URL :** GET: /api/remediationTasks/id \{\}</span><span class="sxs-lookup"><span data-stu-id="53055-115">**URL:** GET: /api/remediationTasks/\{id\}</span></span>

## <a name="permissions"></a><span data-ttu-id="53055-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="53055-116">Permissions</span></span>

<span data-ttu-id="53055-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="53055-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="53055-118">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="53055-118">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="53055-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="53055-119">Permission type</span></span> | <span data-ttu-id="53055-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="53055-120">Permission</span></span> | <span data-ttu-id="53055-121">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="53055-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="53055-122">Application</span><span class="sxs-lookup"><span data-stu-id="53055-122">Application</span></span> | <span data-ttu-id="53055-123">RemediationTask.Read.All</span><span class="sxs-lookup"><span data-stu-id="53055-123">RemediationTask.Read.All</span></span> | <span data-ttu-id="53055-124">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="53055-124">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="53055-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="53055-125">Delegated (work or school account)</span></span> | <span data-ttu-id="53055-126">RemediationTask.Read.Read</span><span class="sxs-lookup"><span data-stu-id="53055-126">RemediationTask.Read.Read</span></span> | <span data-ttu-id="53055-127">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="53055-127">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

## <a name="properties"></a><span data-ttu-id="53055-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="53055-128">Properties</span></span>

<span data-ttu-id="53055-129">Propriété (id)</span><span class="sxs-lookup"><span data-stu-id="53055-129">Property (id)</span></span> | <span data-ttu-id="53055-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="53055-130">Data type</span></span> | <span data-ttu-id="53055-131">Description</span><span class="sxs-lookup"><span data-stu-id="53055-131">Description</span></span> | <span data-ttu-id="53055-132">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53055-132">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="53055-133">category</span><span class="sxs-lookup"><span data-stu-id="53055-133">category</span></span> | <span data-ttu-id="53055-134">String</span><span class="sxs-lookup"><span data-stu-id="53055-134">String</span></span> | <span data-ttu-id="53055-135">Catégorie de l’activité de correction (configuration logicielle/sécurité)</span><span class="sxs-lookup"><span data-stu-id="53055-135">Category of the remediation activity (Software/Security configuration)</span></span> | <span data-ttu-id="53055-136">Logiciels</span><span class="sxs-lookup"><span data-stu-id="53055-136">Software</span></span>
<span data-ttu-id="53055-137">completerEmail</span><span class="sxs-lookup"><span data-stu-id="53055-137">completerEmail</span></span> | <span data-ttu-id="53055-138">String</span><span class="sxs-lookup"><span data-stu-id="53055-138">String</span></span> | <span data-ttu-id="53055-139">Si l’activité de correction a été effectuée manuellement par une personne, cette colonne contient son courrier électronique</span><span class="sxs-lookup"><span data-stu-id="53055-139">If the remediation activity was manually completed by someone, this column contains their email</span></span> | <span data-ttu-id="53055-140">null</span><span class="sxs-lookup"><span data-stu-id="53055-140">null</span></span>
<span data-ttu-id="53055-141">completerId</span><span class="sxs-lookup"><span data-stu-id="53055-141">completerId</span></span> | <span data-ttu-id="53055-142">String</span><span class="sxs-lookup"><span data-stu-id="53055-142">String</span></span> | <span data-ttu-id="53055-143">Si l’activité de correction a été effectuée manuellement par une personne, cette colonne contient son ID d’objet</span><span class="sxs-lookup"><span data-stu-id="53055-143">If the remediation activity was manually completed by someone, this column contains their object id</span></span> | <span data-ttu-id="53055-144">null</span><span class="sxs-lookup"><span data-stu-id="53055-144">null</span></span>
<span data-ttu-id="53055-145">completionMethod</span><span class="sxs-lookup"><span data-stu-id="53055-145">completionMethod</span></span> | <span data-ttu-id="53055-146">String</span><span class="sxs-lookup"><span data-stu-id="53055-146">String</span></span> | <span data-ttu-id="53055-147">Une activité de correction peut être effectuée « automatiquement » (si tous les appareils sont corrigés) ou « manuellement » par une personne qui sélectionne « marquer comme terminé »</span><span class="sxs-lookup"><span data-stu-id="53055-147">A remediation activity can be completed “automatically” (if all the devices are patched) or “manually” by a person who selects “mark as completed”</span></span> | <span data-ttu-id="53055-148">Automatique</span><span class="sxs-lookup"><span data-stu-id="53055-148">Automatic</span></span>
<span data-ttu-id="53055-149">createdOn</span><span class="sxs-lookup"><span data-stu-id="53055-149">createdOn</span></span> | <span data-ttu-id="53055-150">Date/heure</span><span class="sxs-lookup"><span data-stu-id="53055-150">DateTime</span></span> | <span data-ttu-id="53055-151">Heure de création de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-151">Time this remediation activity was created</span></span> | <span data-ttu-id="53055-152">2021-01-12T18:54:11.5499478Z</span><span class="sxs-lookup"><span data-stu-id="53055-152">2021-01-12T18:54:11.5499478Z</span></span>
<span data-ttu-id="53055-153">description</span><span class="sxs-lookup"><span data-stu-id="53055-153">description</span></span> | <span data-ttu-id="53055-154">String</span><span class="sxs-lookup"><span data-stu-id="53055-154">String</span></span> | <span data-ttu-id="53055-155">Description de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-155">Description of this remediation activity</span></span> | <span data-ttu-id="53055-156">Mettez à jour Microsoft Silverlight vers une version ultérieure pour atténuer les vulnérabilités connues affectant vos appareils.</span><span class="sxs-lookup"><span data-stu-id="53055-156">Update Microsoft Silverlight  to a later version to mitigate known vulnerabilities affecting your devices.</span></span>
<span data-ttu-id="53055-157">dueOn</span><span class="sxs-lookup"><span data-stu-id="53055-157">dueOn</span></span> | <span data-ttu-id="53055-158">Date/heure</span><span class="sxs-lookup"><span data-stu-id="53055-158">DateTime</span></span> | <span data-ttu-id="53055-159">Date d’échéance définie par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-159">Due date the creator set for this remediation activity</span></span> | <span data-ttu-id="53055-160">2021-01-13T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="53055-160">2021-01-13T00:00:00Z</span></span>
<span data-ttu-id="53055-161">fixedDevices</span><span class="sxs-lookup"><span data-stu-id="53055-161">fixedDevices</span></span> |  | <span data-ttu-id="53055-162">Nombre d’appareils qui ont été corrigés</span><span class="sxs-lookup"><span data-stu-id="53055-162">The number of devices that have been fixed</span></span> | <span data-ttu-id="53055-163">2</span><span class="sxs-lookup"><span data-stu-id="53055-163">2</span></span>
<span data-ttu-id="53055-164">id</span><span class="sxs-lookup"><span data-stu-id="53055-164">id</span></span> | <span data-ttu-id="53055-165">String</span><span class="sxs-lookup"><span data-stu-id="53055-165">String</span></span> | <span data-ttu-id="53055-166">ID de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-166">ID of this remediation activity</span></span> | <span data-ttu-id="53055-167">097d9735-5479-4899-b1b7-77398899df92</span><span class="sxs-lookup"><span data-stu-id="53055-167">097d9735-5479-4899-b1b7-77398899df92</span></span>
<span data-ttu-id="53055-168">nameId</span><span class="sxs-lookup"><span data-stu-id="53055-168">nameId</span></span> | <span data-ttu-id="53055-169">String</span><span class="sxs-lookup"><span data-stu-id="53055-169">String</span></span> | <span data-ttu-id="53055-170">Nom du produit associé</span><span class="sxs-lookup"><span data-stu-id="53055-170">Related product name</span></span> | <span data-ttu-id="53055-171">Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="53055-171">Microsoft Silverlight</span></span>
<span data-ttu-id="53055-172">priorité</span><span class="sxs-lookup"><span data-stu-id="53055-172">priority</span></span> | <span data-ttu-id="53055-173">String</span><span class="sxs-lookup"><span data-stu-id="53055-173">String</span></span> | <span data-ttu-id="53055-174">Priorité définie par le créateur pour cette activité de correction (Haute\Moyenne\Faible)</span><span class="sxs-lookup"><span data-stu-id="53055-174">Priority the creator set for this remediation activity (High\Medium\Low)</span></span> | <span data-ttu-id="53055-175">Élevé</span><span class="sxs-lookup"><span data-stu-id="53055-175">High</span></span>
<span data-ttu-id="53055-176">productId</span><span class="sxs-lookup"><span data-stu-id="53055-176">productId</span></span> | <span data-ttu-id="53055-177">String</span><span class="sxs-lookup"><span data-stu-id="53055-177">String</span></span> | <span data-ttu-id="53055-178">ID de produit associé</span><span class="sxs-lookup"><span data-stu-id="53055-178">Related product ID</span></span> | <span data-ttu-id="53055-179">microsoft-_-silverlight</span><span class="sxs-lookup"><span data-stu-id="53055-179">microsoft-_-silverlight</span></span>
<span data-ttu-id="53055-180">productivityImpactRemediationType</span><span class="sxs-lookup"><span data-stu-id="53055-180">productivityImpactRemediationType</span></span> | <span data-ttu-id="53055-181">String</span><span class="sxs-lookup"><span data-stu-id="53055-181">String</span></span> | <span data-ttu-id="53055-182">Quelques modifications de configuration peuvent être demandées uniquement pour les appareils sans impact sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53055-182">A few configuration changes could be requested only for devices with no user impact.</span></span> <span data-ttu-id="53055-183">Cette valeur indique la sélection entre « tous les appareils exposés » ou « uniquement les appareils sans impact sur l’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="53055-183">This value indicate the selection between “all exposed devices” or “only devices with no user impact.”</span></span> | <span data-ttu-id="53055-184">AllExposedAssets</span><span class="sxs-lookup"><span data-stu-id="53055-184">AllExposedAssets</span></span>
<span data-ttu-id="53055-185">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="53055-185">rbacGroupNames</span></span> | <span data-ttu-id="53055-186">String</span><span class="sxs-lookup"><span data-stu-id="53055-186">String</span></span> | <span data-ttu-id="53055-187">Noms de groupes d’appareils associés</span><span class="sxs-lookup"><span data-stu-id="53055-187">Related device group names</span></span> | <span data-ttu-id="53055-188">[ « Windows Servers », « Windows 10 » ]</span><span class="sxs-lookup"><span data-stu-id="53055-188">[ "Windows Servers", "Windows 10" ]</span></span>
<span data-ttu-id="53055-189">recommendedProgram</span><span class="sxs-lookup"><span data-stu-id="53055-189">recommendedProgram</span></span> | <span data-ttu-id="53055-190">String</span><span class="sxs-lookup"><span data-stu-id="53055-190">String</span></span> | <span data-ttu-id="53055-191">Programme recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="53055-191">Recommended program to upgrade to</span></span> | <span data-ttu-id="53055-192">null</span><span class="sxs-lookup"><span data-stu-id="53055-192">null</span></span>
<span data-ttu-id="53055-193">recommendedVendor</span><span class="sxs-lookup"><span data-stu-id="53055-193">recommendedVendor</span></span> | <span data-ttu-id="53055-194">String</span><span class="sxs-lookup"><span data-stu-id="53055-194">String</span></span> | <span data-ttu-id="53055-195">Fournisseur recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="53055-195">Recommended vendor to upgrade to</span></span> | <span data-ttu-id="53055-196">null</span><span class="sxs-lookup"><span data-stu-id="53055-196">null</span></span>
<span data-ttu-id="53055-197">recommendedVersion</span><span class="sxs-lookup"><span data-stu-id="53055-197">recommendedVersion</span></span> | <span data-ttu-id="53055-198">String</span><span class="sxs-lookup"><span data-stu-id="53055-198">String</span></span> | <span data-ttu-id="53055-199">Version recommandée pour la mise à jour/mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="53055-199">Recommended version to update/upgrade to</span></span> | <span data-ttu-id="53055-200">null</span><span class="sxs-lookup"><span data-stu-id="53055-200">null</span></span>
<span data-ttu-id="53055-201">relatedComponent</span><span class="sxs-lookup"><span data-stu-id="53055-201">relatedComponent</span></span> | <span data-ttu-id="53055-202">String</span><span class="sxs-lookup"><span data-stu-id="53055-202">String</span></span> | <span data-ttu-id="53055-203">Composant connexe de cette activité de correction (similaire au composant associé pour une recommandation de sécurité)</span><span class="sxs-lookup"><span data-stu-id="53055-203">Related component of this remediation activity (similar to the related component for a security recommendation)</span></span> | <span data-ttu-id="53055-204">Microsoft Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="53055-204">Microsoft Microsoft Silverlight</span></span>
<span data-ttu-id="53055-205">requesterEmail</span><span class="sxs-lookup"><span data-stu-id="53055-205">requesterEmail</span></span> | <span data-ttu-id="53055-206">String</span><span class="sxs-lookup"><span data-stu-id="53055-206">String</span></span> | <span data-ttu-id="53055-207">Adresse de messagerie du créateur</span><span class="sxs-lookup"><span data-stu-id="53055-207">Creator email address</span></span> | <span data-ttu-id="53055-208">globaladmin@UserName.contoso.com</span><span class="sxs-lookup"><span data-stu-id="53055-208">globaladmin@UserName.contoso.com</span></span>
<span data-ttu-id="53055-209">requesterId</span><span class="sxs-lookup"><span data-stu-id="53055-209">requesterId</span></span> | <span data-ttu-id="53055-210">String</span><span class="sxs-lookup"><span data-stu-id="53055-210">String</span></span> | <span data-ttu-id="53055-211">ID d’objet Creator</span><span class="sxs-lookup"><span data-stu-id="53055-211">Creator object id</span></span> | <span data-ttu-id="53055-212">r647211f-2e16-43f2-a480-16ar3a2a796r</span><span class="sxs-lookup"><span data-stu-id="53055-212">r647211f-2e16-43f2-a480-16ar3a2a796r</span></span>
<span data-ttu-id="53055-213">requesterNotes</span><span class="sxs-lookup"><span data-stu-id="53055-213">requesterNotes</span></span> | <span data-ttu-id="53055-214">String</span><span class="sxs-lookup"><span data-stu-id="53055-214">String</span></span> | <span data-ttu-id="53055-215">Notes (texte libre) ajoutées par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-215">The notes (free text) the creator added for this remediation activity</span></span> | <span data-ttu-id="53055-216">null</span><span class="sxs-lookup"><span data-stu-id="53055-216">null</span></span>
<span data-ttu-id="53055-217">scid</span><span class="sxs-lookup"><span data-stu-id="53055-217">scid</span></span> | <span data-ttu-id="53055-218">String</span><span class="sxs-lookup"><span data-stu-id="53055-218">String</span></span> | <span data-ttu-id="53055-219">SCID de la recommandation de sécurité associée</span><span class="sxs-lookup"><span data-stu-id="53055-219">SCID of the related security recommendation</span></span> | <span data-ttu-id="53055-220">null</span><span class="sxs-lookup"><span data-stu-id="53055-220">null</span></span>
<span data-ttu-id="53055-221">status</span><span class="sxs-lookup"><span data-stu-id="53055-221">status</span></span> | <span data-ttu-id="53055-222">String</span><span class="sxs-lookup"><span data-stu-id="53055-222">String</span></span> | <span data-ttu-id="53055-223">État de l’activité de correction (actif/terminé)</span><span class="sxs-lookup"><span data-stu-id="53055-223">Remediation activity status (Active/Completed)</span></span> | <span data-ttu-id="53055-224">Actif</span><span class="sxs-lookup"><span data-stu-id="53055-224">Active</span></span>
<span data-ttu-id="53055-225">statusLastModifiedOn</span><span class="sxs-lookup"><span data-stu-id="53055-225">statusLastModifiedOn</span></span> | <span data-ttu-id="53055-226">Date/heure</span><span class="sxs-lookup"><span data-stu-id="53055-226">DateTime</span></span> | <span data-ttu-id="53055-227">Date de mise à jour du champ d’état</span><span class="sxs-lookup"><span data-stu-id="53055-227">Date when the status field was updated</span></span> | <span data-ttu-id="53055-228">2021-01-12T18:54:11.5499487Z</span><span class="sxs-lookup"><span data-stu-id="53055-228">2021-01-12T18:54:11.5499487Z</span></span>
<span data-ttu-id="53055-229">targetDevices</span><span class="sxs-lookup"><span data-stu-id="53055-229">targetDevices</span></span> | <span data-ttu-id="53055-230">Entier long</span><span class="sxs-lookup"><span data-stu-id="53055-230">Long</span></span> | <span data-ttu-id="53055-231">Nombre d’appareils exposés pour qui cette correction s’applique</span><span class="sxs-lookup"><span data-stu-id="53055-231">Number of exposed devices that this remediation is applicable to</span></span> | <span data-ttu-id="53055-232">43</span><span class="sxs-lookup"><span data-stu-id="53055-232">43</span></span>
<span data-ttu-id="53055-233">title</span><span class="sxs-lookup"><span data-stu-id="53055-233">title</span></span> | <span data-ttu-id="53055-234">String</span><span class="sxs-lookup"><span data-stu-id="53055-234">String</span></span> | <span data-ttu-id="53055-235">Titre de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-235">Title of this remediation activity</span></span> | <span data-ttu-id="53055-236">Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="53055-236">Microsoft Silverlight</span></span>
<span data-ttu-id="53055-237">type</span><span class="sxs-lookup"><span data-stu-id="53055-237">type</span></span> | <span data-ttu-id="53055-238">String</span><span class="sxs-lookup"><span data-stu-id="53055-238">String</span></span> | <span data-ttu-id="53055-239">Type de correction</span><span class="sxs-lookup"><span data-stu-id="53055-239">Remediation type</span></span> | <span data-ttu-id="53055-240">Update</span><span class="sxs-lookup"><span data-stu-id="53055-240">Update</span></span>
<span data-ttu-id="53055-241">vendorId</span><span class="sxs-lookup"><span data-stu-id="53055-241">vendorId</span></span> | <span data-ttu-id="53055-242">String</span><span class="sxs-lookup"><span data-stu-id="53055-242">String</span></span> | <span data-ttu-id="53055-243">Nom du fournisseur associé</span><span class="sxs-lookup"><span data-stu-id="53055-243">Related vendor name</span></span> | <span data-ttu-id="53055-244">Microsoft</span><span class="sxs-lookup"><span data-stu-id="53055-244">Microsoft</span></span>

## <a name="example"></a><span data-ttu-id="53055-245">Exemple</span><span class="sxs-lookup"><span data-stu-id="53055-245">Example</span></span>

### <a name="request-example"></a><span data-ttu-id="53055-246">Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="53055-246">Request example</span></span>

```http
GET https://api-luna.securitycenter.windows.com/api/remediationtasks/03942ef5-aecb-4c6e-b555-d6a97013844c
```

### <a name="response-example"></a><span data-ttu-id="53055-247">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="53055-247">Response example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="53055-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53055-248">See also</span></span>

- [<span data-ttu-id="53055-249">Méthodes et propriétés de correction</span><span class="sxs-lookup"><span data-stu-id="53055-249">Remediation methods and properties</span></span>](get-remediation-methods-properties.md)

- [<span data-ttu-id="53055-250">Répertorier toutes les activités de correction</span><span class="sxs-lookup"><span data-stu-id="53055-250">List all remediation activities</span></span>](get-remediation-all-activities.md)

- [<span data-ttu-id="53055-251">Répertorier les appareils exposés d’une activité de correction</span><span class="sxs-lookup"><span data-stu-id="53055-251">List exposed devices of one remediation activity</span></span>](get-remediation-exposed-devices-activities.md)

- [<span data-ttu-id="53055-252">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="53055-252">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="53055-253">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="53055-253">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
