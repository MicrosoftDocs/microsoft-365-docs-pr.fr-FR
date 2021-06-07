---
title: Type de ressource Indicateur
description: Spécifiez les détails de l’entité et définissez l’expiration de l’indicateur à l’aide de Microsoft Defender pour endpoint.
keywords: api, api pris en charge, get, TiIndicator, Indicateur, récent
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
ms.openlocfilehash: 75b62f1bada67c30dc05237a284f8b64c3c7072d
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771380"
---
# <a name="indicator-resource-type"></a><span data-ttu-id="5f060-104">Type de ressource Indicateur</span><span class="sxs-lookup"><span data-stu-id="5f060-104">Indicator resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5f060-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5f060-105">**Applies to:**</span></span>
- [<span data-ttu-id="5f060-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5f060-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5f060-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5f060-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="5f060-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5f060-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="5f060-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5f060-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


- <span data-ttu-id="5f060-110">Consultez la [page Indicateurs correspondante](https://securitycenter.windows.com/preferences2/custom_ti_indicators/files) dans le portail.</span><span class="sxs-lookup"><span data-stu-id="5f060-110">See the corresponding [Indicators page](https://securitycenter.windows.com/preferences2/custom_ti_indicators/files) in the portal.</span></span> 

<span data-ttu-id="5f060-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="5f060-111">Method</span></span>|<span data-ttu-id="5f060-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="5f060-112">Return Type</span></span> |<span data-ttu-id="5f060-113">Description</span><span class="sxs-lookup"><span data-stu-id="5f060-113">Description</span></span>
:---|:---|:---
[<span data-ttu-id="5f060-114">Répertorier des indicateurs</span><span class="sxs-lookup"><span data-stu-id="5f060-114">List Indicators</span></span>](get-ti-indicators-collection.md) | <span data-ttu-id="5f060-115">[Indicateur](ti-indicator.md) Collection</span><span class="sxs-lookup"><span data-stu-id="5f060-115">[Indicator](ti-indicator.md) Collection</span></span> | <span data-ttu-id="5f060-116">Entités [d’indicateur](ti-indicator.md) de liste.</span><span class="sxs-lookup"><span data-stu-id="5f060-116">List [Indicator](ti-indicator.md) entities.</span></span>
[<span data-ttu-id="5f060-117">Envoyer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="5f060-117">Submit Indicator</span></span>](post-ti-indicator.md) | [<span data-ttu-id="5f060-118">Indicateur</span><span class="sxs-lookup"><span data-stu-id="5f060-118">Indicator</span></span>](ti-indicator.md) | <span data-ttu-id="5f060-119">Entité d’indicateur [d’soumission ou](ti-indicator.md) de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5f060-119">Submit or update [Indicator](ti-indicator.md) entity.</span></span>
[<span data-ttu-id="5f060-120">Importer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="5f060-120">Import Indicators</span></span>](import-ti-indicators.md) | <span data-ttu-id="5f060-121">[Indicateur](ti-indicator.md) Collection</span><span class="sxs-lookup"><span data-stu-id="5f060-121">[Indicator](ti-indicator.md) Collection</span></span> | <span data-ttu-id="5f060-122">Envoyer ou mettre à jour [des entités](ti-indicator.md) d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="5f060-122">Submit or update [Indicators](ti-indicator.md) entities.</span></span>
[<span data-ttu-id="5f060-123">Supprimer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="5f060-123">Delete Indicator</span></span>](delete-ti-indicator-by-id.md) | <span data-ttu-id="5f060-124">Aucun contenu</span><span class="sxs-lookup"><span data-stu-id="5f060-124">No Content</span></span> | <span data-ttu-id="5f060-125">Supprime [l’entité Indicateur.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="5f060-125">Deletes [Indicator](ti-indicator.md) entity.</span></span>


## <a name="properties"></a><span data-ttu-id="5f060-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5f060-126">Properties</span></span>
<span data-ttu-id="5f060-127">Propriété</span><span class="sxs-lookup"><span data-stu-id="5f060-127">Property</span></span> |  <span data-ttu-id="5f060-128">Type</span><span class="sxs-lookup"><span data-stu-id="5f060-128">Type</span></span>    |   <span data-ttu-id="5f060-129">Description</span><span class="sxs-lookup"><span data-stu-id="5f060-129">Description</span></span>
:---|:---|:---
<span data-ttu-id="5f060-130">id</span><span class="sxs-lookup"><span data-stu-id="5f060-130">id</span></span> | <span data-ttu-id="5f060-131">String</span><span class="sxs-lookup"><span data-stu-id="5f060-131">String</span></span> | <span data-ttu-id="5f060-132">Identité de [l’entité Indicateur.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="5f060-132">Identity of the [Indicator](ti-indicator.md) entity.</span></span>
<span data-ttu-id="5f060-133">indicatorValue</span><span class="sxs-lookup"><span data-stu-id="5f060-133">indicatorValue</span></span> | <span data-ttu-id="5f060-134">String</span><span class="sxs-lookup"><span data-stu-id="5f060-134">String</span></span> | <span data-ttu-id="5f060-135">Valeur de [l’indicateur](ti-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="5f060-135">The value of the [Indicator](ti-indicator.md).</span></span>
<span data-ttu-id="5f060-136">indicatorType</span><span class="sxs-lookup"><span data-stu-id="5f060-136">indicatorType</span></span> | <span data-ttu-id="5f060-137">Énum</span><span class="sxs-lookup"><span data-stu-id="5f060-137">Enum</span></span> | <span data-ttu-id="5f060-138">Type de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-138">Type of the indicator.</span></span> <span data-ttu-id="5f060-139">Les valeurs possibles sont les suivantes : « FileSha1 », « FileSha256 », « IpAddress », « DomainName » et « Url ».</span><span class="sxs-lookup"><span data-stu-id="5f060-139">Possible values are: "FileSha1", "FileSha256", "IpAddress", "DomainName" and "Url".</span></span>
<span data-ttu-id="5f060-140">application</span><span class="sxs-lookup"><span data-stu-id="5f060-140">application</span></span> | <span data-ttu-id="5f060-141">String</span><span class="sxs-lookup"><span data-stu-id="5f060-141">String</span></span> | <span data-ttu-id="5f060-142">Application associée à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-142">The application associated with the indicator.</span></span> 
<span data-ttu-id="5f060-143">action</span><span class="sxs-lookup"><span data-stu-id="5f060-143">action</span></span> | <span data-ttu-id="5f060-144">Énum</span><span class="sxs-lookup"><span data-stu-id="5f060-144">Enum</span></span> | <span data-ttu-id="5f060-145">Action qui sera entreprise si l’indicateur est détecté dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="5f060-145">The action that will be taken if the indicator will be discovered in the organization.</span></span> <span data-ttu-id="5f060-146">Les valeurs possibles sont : « Alert », « AlertAndBlock » et « Allowed ».</span><span class="sxs-lookup"><span data-stu-id="5f060-146">Possible values are: "Alert", "AlertAndBlock", and "Allowed".</span></span>
<span data-ttu-id="5f060-147">sourceType</span><span class="sxs-lookup"><span data-stu-id="5f060-147">sourceType</span></span> | <span data-ttu-id="5f060-148">Énum</span><span class="sxs-lookup"><span data-stu-id="5f060-148">Enum</span></span> | <span data-ttu-id="5f060-149">« Utilisateur » au cas où l’indicateur créé par un utilisateur (par exemple, à partir du portail), « AadApp » au cas où il a été envoyé à l’aide d’une application automatisée via l’API.</span><span class="sxs-lookup"><span data-stu-id="5f060-149">"User" in case the Indicator created by a user (e.g. from the portal), "AadApp" in case it submitted using automated application via the API.</span></span>
<span data-ttu-id="5f060-150">source</span><span class="sxs-lookup"><span data-stu-id="5f060-150">source</span></span> | <span data-ttu-id="5f060-151">string</span><span class="sxs-lookup"><span data-stu-id="5f060-151">string</span></span> | <span data-ttu-id="5f060-152">Nom de l’utilisateur/de l’application qui a soumis l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-152">The name of the user/application that submitted the indicator.</span></span>
<span data-ttu-id="5f060-153">createdBy</span><span class="sxs-lookup"><span data-stu-id="5f060-153">createdBy</span></span> | <span data-ttu-id="5f060-154">String</span><span class="sxs-lookup"><span data-stu-id="5f060-154">String</span></span> | <span data-ttu-id="5f060-155">Identité unique de l’utilisateur/de l’application qui a soumis l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-155">Unique identity of the user/application that submitted the indicator.</span></span>
<span data-ttu-id="5f060-156">lastUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="5f060-156">lastUpdatedBy</span></span> | <span data-ttu-id="5f060-157">String</span><span class="sxs-lookup"><span data-stu-id="5f060-157">String</span></span> | <span data-ttu-id="5f060-158">Identité de l’utilisateur/de l’application qui a mis à jour l’indicateur pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="5f060-158">Identity of the user/application that last updated the indicator.</span></span>
<span data-ttu-id="5f060-159">creationTimeDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="5f060-159">creationTimeDateTimeUtc</span></span> | <span data-ttu-id="5f060-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f060-160">DateTimeOffset</span></span> | <span data-ttu-id="5f060-161">Date et heure de création de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-161">The date and time when the indicator was created.</span></span>
<span data-ttu-id="5f060-162">expirationTime</span><span class="sxs-lookup"><span data-stu-id="5f060-162">expirationTime</span></span> | <span data-ttu-id="5f060-163">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f060-163">DateTimeOffset</span></span> | <span data-ttu-id="5f060-164">Heure d’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-164">The expiration time of the indicator.</span></span>
<span data-ttu-id="5f060-165">lastUpdateTime</span><span class="sxs-lookup"><span data-stu-id="5f060-165">lastUpdateTime</span></span> | <span data-ttu-id="5f060-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f060-166">DateTimeOffset</span></span> | <span data-ttu-id="5f060-167">Dernière mise à jour de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-167">The last time the indicator was updated.</span></span>
<span data-ttu-id="5f060-168">Sévérité </span><span class="sxs-lookup"><span data-stu-id="5f060-168">severity</span></span> | <span data-ttu-id="5f060-169">Énum</span><span class="sxs-lookup"><span data-stu-id="5f060-169">Enum</span></span> | <span data-ttu-id="5f060-170">Gravité de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-170">The severity of the indicator.</span></span> <span data-ttu-id="5f060-171">les valeurs possibles sont : « Informational », « Low », « Medium » et « High ».</span><span class="sxs-lookup"><span data-stu-id="5f060-171">possible values are: "Informational", "Low", "Medium" and "High".</span></span>
<span data-ttu-id="5f060-172">title</span><span class="sxs-lookup"><span data-stu-id="5f060-172">title</span></span> | <span data-ttu-id="5f060-173">String</span><span class="sxs-lookup"><span data-stu-id="5f060-173">String</span></span> | <span data-ttu-id="5f060-174">Titre de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-174">Indicator title.</span></span>
<span data-ttu-id="5f060-175">description</span><span class="sxs-lookup"><span data-stu-id="5f060-175">description</span></span> | <span data-ttu-id="5f060-176">String</span><span class="sxs-lookup"><span data-stu-id="5f060-176">String</span></span> | <span data-ttu-id="5f060-177">Description de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-177">Description of the indicator.</span></span>
<span data-ttu-id="5f060-178">recommendedActions</span><span class="sxs-lookup"><span data-stu-id="5f060-178">recommendedActions</span></span> | <span data-ttu-id="5f060-179">String</span><span class="sxs-lookup"><span data-stu-id="5f060-179">String</span></span> | <span data-ttu-id="5f060-180">Actions recommandées pour l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="5f060-180">Recommended actions for the indicator.</span></span>
<span data-ttu-id="5f060-181">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="5f060-181">rbacGroupNames</span></span> | <span data-ttu-id="5f060-182">Liste des chaînes</span><span class="sxs-lookup"><span data-stu-id="5f060-182">List of strings</span></span> | <span data-ttu-id="5f060-183">Noms de groupes d’appareils RBAC où l’indicateur est exposé et actif.</span><span class="sxs-lookup"><span data-stu-id="5f060-183">RBAC device group names where the indicator is exposed and active.</span></span> <span data-ttu-id="5f060-184">Liste vide au cas où elle serait exposée à tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="5f060-184">Empty list in case it exposed to all devices.</span></span>


## <a name="json-representation"></a><span data-ttu-id="5f060-185">Représentation Json</span><span class="sxs-lookup"><span data-stu-id="5f060-185">Json representation</span></span>

```json
{
    "id": "994",
    "indicatorValue": "881c0f10c75e64ec39d257a131fcd531f47dd2cff2070ae94baa347d375126fd",
    "indicatorType": "FileSha256",
    "action": "AlertAndBlock",
    "application": null,
    "source": "user@contoso.onmicrosoft.com",
    "sourceType": "User",
    "createdBy": "user@contoso.onmicrosoft.com",
    "severity": "Informational",
    "title": "Michael test",
    "description": "test",
    "recommendedActions": "nothing",
    "creationTimeDateTimeUtc": "2019-12-19T09:09:46.9139216Z",
    "expirationTime": null,
    "lastUpdateTime": "2019-12-19T09:09:47.3358111Z",
    "lastUpdatedBy": null,
    "rbacGroupNames": ["team1"]
}
```
