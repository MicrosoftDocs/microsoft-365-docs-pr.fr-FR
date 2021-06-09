---
title: Répertorier toutes les activités de correction
description: Retourne des informations sur toutes les activités de correction.
keywords: api, correction, api de correction, obtenir, tâches de correction, toutes les corrections,
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 60f80e78a5f5c7da44a218c30f4b0173d4ecc829
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52845130"
---
# <a name="list-all-remediation-activities"></a><span data-ttu-id="6ae6e-104">Répertorier toutes les activités de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-104">List all remediation activities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="6ae6e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6ae6e-105">**Applies to:**</span></span>

- [<span data-ttu-id="6ae6e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6ae6e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="6ae6e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6ae6e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="6ae6e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6ae6e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6ae6e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="6ae6e-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="6ae6e-110">API description</span></span>

<span data-ttu-id="6ae6e-111">Retourne des informations sur toutes les activités de correction.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-111">Returns information about all remediation activities.</span></span>

<span data-ttu-id="6ae6e-112">[En savoir plus sur les activités de correction.](tvm-remediation.md)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-112">[Learn more about remediation activities](tvm-remediation.md).</span></span>

<span data-ttu-id="6ae6e-113">**URL :** GET: /api/remediationTasks</span><span class="sxs-lookup"><span data-stu-id="6ae6e-113">**URL:** GET: /api/remediationTasks</span></span>

## <a name="permissions"></a><span data-ttu-id="6ae6e-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="6ae6e-114">Permissions</span></span>

<span data-ttu-id="6ae6e-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="6ae6e-116">Pour plus d’informations, notamment sur le choix des autorisations, voir Utiliser Microsoft Defender pour les API de point de [terminaison pour plus d’informations.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs for details.](apis-intro.md)</span></span>

<span data-ttu-id="6ae6e-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="6ae6e-117">Permission type</span></span> | <span data-ttu-id="6ae6e-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="6ae6e-118">Permission</span></span> | <span data-ttu-id="6ae6e-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="6ae6e-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="6ae6e-120">Application</span><span class="sxs-lookup"><span data-stu-id="6ae6e-120">Application</span></span> | <span data-ttu-id="6ae6e-121">RemediationTask.Read.All</span><span class="sxs-lookup"><span data-stu-id="6ae6e-121">RemediationTask.Read.All</span></span> | <span data-ttu-id="6ae6e-122">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="6ae6e-122">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>
<span data-ttu-id="6ae6e-123">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-123">Delegated (work or school account)</span></span> | <span data-ttu-id="6ae6e-124">RemediationTask.Read</span><span class="sxs-lookup"><span data-stu-id="6ae6e-124">RemediationTask.Read</span></span> | <span data-ttu-id="6ae6e-125">\'Lire les informations sur les vulnérabilités de gestion des menaces et des vulnérabilités\'</span><span class="sxs-lookup"><span data-stu-id="6ae6e-125">\'Read Threat and Vulnerability Management vulnerability information\'</span></span>

## <a name="properties"></a><span data-ttu-id="6ae6e-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6ae6e-126">Properties</span></span>

<span data-ttu-id="6ae6e-127">Propriété (id)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-127">Property (id)</span></span> | <span data-ttu-id="6ae6e-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="6ae6e-128">Data type</span></span> | <span data-ttu-id="6ae6e-129">Description</span><span class="sxs-lookup"><span data-stu-id="6ae6e-129">Description</span></span> | <span data-ttu-id="6ae6e-130">Exemple de valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6ae6e-130">Example of a returned value</span></span>
:---|:---|:---|:---
<span data-ttu-id="6ae6e-131">category</span><span class="sxs-lookup"><span data-stu-id="6ae6e-131">category</span></span> | <span data-ttu-id="6ae6e-132">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-132">String</span></span> | <span data-ttu-id="6ae6e-133">Catégorie de l’activité de correction (configuration logicielle/sécurité)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-133">Category of the remediation activity (Software/Security configuration)</span></span> | <span data-ttu-id="6ae6e-134">Logiciels</span><span class="sxs-lookup"><span data-stu-id="6ae6e-134">Software</span></span>
<span data-ttu-id="6ae6e-135">completerEmail</span><span class="sxs-lookup"><span data-stu-id="6ae6e-135">completerEmail</span></span> | <span data-ttu-id="6ae6e-136">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-136">String</span></span> | <span data-ttu-id="6ae6e-137">Si l’activité de correction a été effectuée manuellement par une personne, cette colonne contient son courrier électronique</span><span class="sxs-lookup"><span data-stu-id="6ae6e-137">If the remediation activity was manually completed by someone, this column contains their email</span></span> | <span data-ttu-id="6ae6e-138">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-138">null</span></span>
<span data-ttu-id="6ae6e-139">completerId</span><span class="sxs-lookup"><span data-stu-id="6ae6e-139">completerId</span></span> | <span data-ttu-id="6ae6e-140">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-140">String</span></span> | <span data-ttu-id="6ae6e-141">Si l’activité de correction a été effectuée manuellement par une personne, cette colonne contient son ID d’objet</span><span class="sxs-lookup"><span data-stu-id="6ae6e-141">If the remediation activity was manually completed by someone, this column contains their object id</span></span> | <span data-ttu-id="6ae6e-142">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-142">null</span></span>
<span data-ttu-id="6ae6e-143">completionMethod</span><span class="sxs-lookup"><span data-stu-id="6ae6e-143">completionMethod</span></span> | <span data-ttu-id="6ae6e-144">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-144">String</span></span> | <span data-ttu-id="6ae6e-145">Une activité de correction peut être effectuée « automatiquement » (si tous les appareils sont corrigés) ou « manuellement » par une personne qui sélectionne « marquer comme terminé »</span><span class="sxs-lookup"><span data-stu-id="6ae6e-145">A remediation activity can be completed “automatically” (if all the devices are patched) or “manually” by a person who selects “mark as completed”</span></span> | <span data-ttu-id="6ae6e-146">Automatique</span><span class="sxs-lookup"><span data-stu-id="6ae6e-146">Automatic</span></span>
<span data-ttu-id="6ae6e-147">createdOn</span><span class="sxs-lookup"><span data-stu-id="6ae6e-147">createdOn</span></span> | <span data-ttu-id="6ae6e-148">Date/heure</span><span class="sxs-lookup"><span data-stu-id="6ae6e-148">DateTime</span></span> | <span data-ttu-id="6ae6e-149">Heure de création de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-149">Time this remediation activity was created</span></span> | <span data-ttu-id="6ae6e-150">2021-01-12T18:54:11.5499478Z</span><span class="sxs-lookup"><span data-stu-id="6ae6e-150">2021-01-12T18:54:11.5499478Z</span></span>
<span data-ttu-id="6ae6e-151">description</span><span class="sxs-lookup"><span data-stu-id="6ae6e-151">description</span></span> | <span data-ttu-id="6ae6e-152">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-152">String</span></span> | <span data-ttu-id="6ae6e-153">Description de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-153">Description of this remediation activity</span></span> | <span data-ttu-id="6ae6e-154">Mettez à jour Microsoft Silverlight vers une version ultérieure pour atténuer les vulnérabilités connues affectant vos appareils.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-154">Update Microsoft Silverlight  to a later version to mitigate known vulnerabilities affecting your devices.</span></span>
<span data-ttu-id="6ae6e-155">dueOn</span><span class="sxs-lookup"><span data-stu-id="6ae6e-155">dueOn</span></span> | <span data-ttu-id="6ae6e-156">Date/heure</span><span class="sxs-lookup"><span data-stu-id="6ae6e-156">DateTime</span></span> | <span data-ttu-id="6ae6e-157">Date d’échéance définie par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-157">Due date the creator set for this remediation activity</span></span> | <span data-ttu-id="6ae6e-158">2021-01-13T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="6ae6e-158">2021-01-13T00:00:00Z</span></span>
<span data-ttu-id="6ae6e-159">fixedDevices</span><span class="sxs-lookup"><span data-stu-id="6ae6e-159">fixedDevices</span></span> | <span data-ttu-id="6ae6e-160">.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-160">.</span></span> | <span data-ttu-id="6ae6e-161">Nombre d’appareils qui ont été corrigés</span><span class="sxs-lookup"><span data-stu-id="6ae6e-161">The number of devices that have been fixed</span></span> | <span data-ttu-id="6ae6e-162">2</span><span class="sxs-lookup"><span data-stu-id="6ae6e-162">2</span></span>
<span data-ttu-id="6ae6e-163">id</span><span class="sxs-lookup"><span data-stu-id="6ae6e-163">id</span></span> | <span data-ttu-id="6ae6e-164">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-164">String</span></span> | <span data-ttu-id="6ae6e-165">ID de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-165">ID of this remediation activity</span></span> | <span data-ttu-id="6ae6e-166">097d9735-5479-4899-b1b7-77398899df92</span><span class="sxs-lookup"><span data-stu-id="6ae6e-166">097d9735-5479-4899-b1b7-77398899df92</span></span>
<span data-ttu-id="6ae6e-167">nameId</span><span class="sxs-lookup"><span data-stu-id="6ae6e-167">nameId</span></span> | <span data-ttu-id="6ae6e-168">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-168">String</span></span> | <span data-ttu-id="6ae6e-169">Nom du produit associé</span><span class="sxs-lookup"><span data-stu-id="6ae6e-169">Related product name</span></span> | <span data-ttu-id="6ae6e-170">Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="6ae6e-170">Microsoft Silverlight</span></span>
<span data-ttu-id="6ae6e-171">priorité</span><span class="sxs-lookup"><span data-stu-id="6ae6e-171">priority</span></span> | <span data-ttu-id="6ae6e-172">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-172">String</span></span> | <span data-ttu-id="6ae6e-173">Priorité définie par le créateur pour cette activité de correction (Haute\Moyenne\Faible)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-173">Priority the creator set for this remediation activity (High\Medium\Low)</span></span> | <span data-ttu-id="6ae6e-174">Élevé</span><span class="sxs-lookup"><span data-stu-id="6ae6e-174">High</span></span>
<span data-ttu-id="6ae6e-175">productId</span><span class="sxs-lookup"><span data-stu-id="6ae6e-175">productId</span></span> | <span data-ttu-id="6ae6e-176">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-176">String</span></span> | <span data-ttu-id="6ae6e-177">ID de produit associé</span><span class="sxs-lookup"><span data-stu-id="6ae6e-177">Related product ID</span></span> | <span data-ttu-id="6ae6e-178">microsoft-_-silverlight</span><span class="sxs-lookup"><span data-stu-id="6ae6e-178">microsoft-_-silverlight</span></span>
<span data-ttu-id="6ae6e-179">productivityImpactRemediationType</span><span class="sxs-lookup"><span data-stu-id="6ae6e-179">productivityImpactRemediationType</span></span> | <span data-ttu-id="6ae6e-180">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-180">String</span></span> | <span data-ttu-id="6ae6e-181">Quelques modifications de configuration peuvent être demandées uniquement pour les appareils sans impact sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ae6e-181">A few configuration changes could be requested only for devices with no user impact.</span></span> <span data-ttu-id="6ae6e-182">Cette valeur indique la sélection entre « tous les appareils exposés » ou « uniquement les appareils sans impact sur l’utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="6ae6e-182">This value indicates the selection between “all exposed devices” or “only devices with no user impact.”</span></span> | <span data-ttu-id="6ae6e-183">AllExposedAssets</span><span class="sxs-lookup"><span data-stu-id="6ae6e-183">AllExposedAssets</span></span>
<span data-ttu-id="6ae6e-184">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="6ae6e-184">rbacGroupNames</span></span> | <span data-ttu-id="6ae6e-185">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-185">String</span></span> | <span data-ttu-id="6ae6e-186">Noms de groupes d’appareils associés</span><span class="sxs-lookup"><span data-stu-id="6ae6e-186">Related device group names</span></span> | <span data-ttu-id="6ae6e-187">[ « Windows Serveurs », « Windows 10 » ]</span><span class="sxs-lookup"><span data-stu-id="6ae6e-187">[ "Windows Servers", "Windows 10" ]</span></span>
<span data-ttu-id="6ae6e-188">recommendedProgram</span><span class="sxs-lookup"><span data-stu-id="6ae6e-188">recommendedProgram</span></span> | <span data-ttu-id="6ae6e-189">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-189">String</span></span> | <span data-ttu-id="6ae6e-190">Programme recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="6ae6e-190">Recommended program to upgrade to</span></span> | <span data-ttu-id="6ae6e-191">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-191">null</span></span>
<span data-ttu-id="6ae6e-192">recommendedVendor</span><span class="sxs-lookup"><span data-stu-id="6ae6e-192">recommendedVendor</span></span> | <span data-ttu-id="6ae6e-193">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-193">String</span></span> | <span data-ttu-id="6ae6e-194">Fournisseur recommandé pour la mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="6ae6e-194">Recommended vendor to upgrade to</span></span> | <span data-ttu-id="6ae6e-195">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-195">null</span></span>
<span data-ttu-id="6ae6e-196">recommendedVersion</span><span class="sxs-lookup"><span data-stu-id="6ae6e-196">recommendedVersion</span></span> | <span data-ttu-id="6ae6e-197">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-197">String</span></span> | <span data-ttu-id="6ae6e-198">Version recommandée pour la mise à jour/mise à niveau vers</span><span class="sxs-lookup"><span data-stu-id="6ae6e-198">Recommended version to update/upgrade to</span></span> | <span data-ttu-id="6ae6e-199">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-199">null</span></span>
<span data-ttu-id="6ae6e-200">relatedComponent</span><span class="sxs-lookup"><span data-stu-id="6ae6e-200">relatedComponent</span></span> | <span data-ttu-id="6ae6e-201">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-201">String</span></span> | <span data-ttu-id="6ae6e-202">Composant connexe de cette activité de correction (similaire au composant associé pour une recommandation de sécurité)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-202">Related component of this remediation activity (similar to the related component for a security recommendation)</span></span> | <span data-ttu-id="6ae6e-203">Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="6ae6e-203">Microsoft Silverlight</span></span>
<span data-ttu-id="6ae6e-204">requesterEmail</span><span class="sxs-lookup"><span data-stu-id="6ae6e-204">requesterEmail</span></span> | <span data-ttu-id="6ae6e-205">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-205">String</span></span> | <span data-ttu-id="6ae6e-206">Adresse de messagerie du créateur</span><span class="sxs-lookup"><span data-stu-id="6ae6e-206">Creator email address</span></span> | <span data-ttu-id="6ae6e-207">globaladmin@UserName.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ae6e-207">globaladmin@UserName.contoso.com</span></span>
<span data-ttu-id="6ae6e-208">requesterId</span><span class="sxs-lookup"><span data-stu-id="6ae6e-208">requesterId</span></span> | <span data-ttu-id="6ae6e-209">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-209">String</span></span> | <span data-ttu-id="6ae6e-210">ID d’objet Creator</span><span class="sxs-lookup"><span data-stu-id="6ae6e-210">Creator object id</span></span> | <span data-ttu-id="6ae6e-211">r647211f-2e16-43f2-a480-16ar3a2a796r</span><span class="sxs-lookup"><span data-stu-id="6ae6e-211">r647211f-2e16-43f2-a480-16ar3a2a796r</span></span>
<span data-ttu-id="6ae6e-212">requesterNotes</span><span class="sxs-lookup"><span data-stu-id="6ae6e-212">requesterNotes</span></span> | <span data-ttu-id="6ae6e-213">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-213">String</span></span> | <span data-ttu-id="6ae6e-214">Notes (texte libre) ajoutées par le créateur pour cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-214">The notes (free text) the creator added for this remediation activity</span></span> | <span data-ttu-id="6ae6e-215">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-215">null</span></span>
<span data-ttu-id="6ae6e-216">scid</span><span class="sxs-lookup"><span data-stu-id="6ae6e-216">scid</span></span> | <span data-ttu-id="6ae6e-217">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-217">String</span></span> | <span data-ttu-id="6ae6e-218">SCID de la recommandation de sécurité associée</span><span class="sxs-lookup"><span data-stu-id="6ae6e-218">SCID of the related security recommendation</span></span> | <span data-ttu-id="6ae6e-219">null</span><span class="sxs-lookup"><span data-stu-id="6ae6e-219">null</span></span>
<span data-ttu-id="6ae6e-220">status</span><span class="sxs-lookup"><span data-stu-id="6ae6e-220">status</span></span> | <span data-ttu-id="6ae6e-221">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-221">String</span></span> | <span data-ttu-id="6ae6e-222">État de l’activité de correction (actif/terminé)</span><span class="sxs-lookup"><span data-stu-id="6ae6e-222">Remediation activity status (Active/Completed)</span></span> | <span data-ttu-id="6ae6e-223">Actif</span><span class="sxs-lookup"><span data-stu-id="6ae6e-223">Active</span></span>
<span data-ttu-id="6ae6e-224">statusLastModifiedOn</span><span class="sxs-lookup"><span data-stu-id="6ae6e-224">statusLastModifiedOn</span></span> | <span data-ttu-id="6ae6e-225">Date/heure</span><span class="sxs-lookup"><span data-stu-id="6ae6e-225">DateTime</span></span> | <span data-ttu-id="6ae6e-226">Date de mise à jour du champ d’état</span><span class="sxs-lookup"><span data-stu-id="6ae6e-226">Date when the status field was updated</span></span> | <span data-ttu-id="6ae6e-227">2021-01-12T18:54:11.5499487Z</span><span class="sxs-lookup"><span data-stu-id="6ae6e-227">2021-01-12T18:54:11.5499487Z</span></span>
<span data-ttu-id="6ae6e-228">targetDevices</span><span class="sxs-lookup"><span data-stu-id="6ae6e-228">targetDevices</span></span> | <span data-ttu-id="6ae6e-229">Entier long</span><span class="sxs-lookup"><span data-stu-id="6ae6e-229">Long</span></span> | <span data-ttu-id="6ae6e-230">Nombre d’appareils exposés à appliquer à cette correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-230">Number of exposed devices that this remediation is applicable to</span></span> | <span data-ttu-id="6ae6e-231">43</span><span class="sxs-lookup"><span data-stu-id="6ae6e-231">43</span></span>
<span data-ttu-id="6ae6e-232">title</span><span class="sxs-lookup"><span data-stu-id="6ae6e-232">title</span></span> | <span data-ttu-id="6ae6e-233">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-233">String</span></span> | <span data-ttu-id="6ae6e-234">Titre de cette activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-234">Title of this remediation activity</span></span> | <span data-ttu-id="6ae6e-235">Mettre à jour Microsoft Silverlight</span><span class="sxs-lookup"><span data-stu-id="6ae6e-235">Update Microsoft Silverlight</span></span>
<span data-ttu-id="6ae6e-236">type</span><span class="sxs-lookup"><span data-stu-id="6ae6e-236">type</span></span> | <span data-ttu-id="6ae6e-237">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-237">String</span></span> | <span data-ttu-id="6ae6e-238">Type de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-238">Remediation type</span></span> | <span data-ttu-id="6ae6e-239">Update</span><span class="sxs-lookup"><span data-stu-id="6ae6e-239">Update</span></span>
<span data-ttu-id="6ae6e-240">vendorId</span><span class="sxs-lookup"><span data-stu-id="6ae6e-240">vendorId</span></span> | <span data-ttu-id="6ae6e-241">String</span><span class="sxs-lookup"><span data-stu-id="6ae6e-241">String</span></span> | <span data-ttu-id="6ae6e-242">Nom du fournisseur associé</span><span class="sxs-lookup"><span data-stu-id="6ae6e-242">Related vendor name</span></span> | <span data-ttu-id="6ae6e-243">Microsoft</span><span class="sxs-lookup"><span data-stu-id="6ae6e-243">Microsoft</span></span>

## <a name="example"></a><span data-ttu-id="6ae6e-244">Exemple</span><span class="sxs-lookup"><span data-stu-id="6ae6e-244">Example</span></span>

### <a name="request-example"></a><span data-ttu-id="6ae6e-245">Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="6ae6e-245">Request example</span></span>

```http
GET https://api-luna.securitycenter.windows.com/api/remediationtasks/
```

### <a name="response-example"></a><span data-ttu-id="6ae6e-246">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="6ae6e-246">Response example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6ae6e-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae6e-247">See also</span></span>

- [<span data-ttu-id="6ae6e-248">Méthodes et propriétés de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-248">Remediation methods and properties</span></span>](get-remediation-methods-properties.md)

- [<span data-ttu-id="6ae6e-249">Obtenir une activité de correction par son ID</span><span class="sxs-lookup"><span data-stu-id="6ae6e-249">Get one remediation activity by Id</span></span>](get-remediation-one-activity.md)

- [<span data-ttu-id="6ae6e-250">Répertorier les appareils exposés d’une activité de correction</span><span class="sxs-lookup"><span data-stu-id="6ae6e-250">List exposed devices of one remediation activity</span></span>](get-remediation-exposed-devices-activities.md)

- [<span data-ttu-id="6ae6e-251">Menaces basées sur les risques & gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="6ae6e-251">Risk-based threat & vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)

- [<span data-ttu-id="6ae6e-252">Vulnérabilités dans votre organisation</span><span class="sxs-lookup"><span data-stu-id="6ae6e-252">Vulnerabilities in your organization</span></span>](tvm-weaknesses.md)
