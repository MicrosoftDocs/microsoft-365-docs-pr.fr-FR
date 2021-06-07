---
title: Créer une alerte à partir de l’API d’événement
description: Découvrez comment utiliser l’API Créer une alerte pour créer une alerte en haut de l’événement dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, alerte, informations, ID
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
ms.openlocfilehash: 8b05dde015bc96e1ccd3f80e25c416a371e03199
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772388"
---
# <a name="create-alert-api"></a><span data-ttu-id="aa757-104">CRÉER une API d’alerte</span><span class="sxs-lookup"><span data-stu-id="aa757-104">Create alert API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="aa757-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="aa757-105">**Applies to:**</span></span>
- [<span data-ttu-id="aa757-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="aa757-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="aa757-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="aa757-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

- <span data-ttu-id="aa757-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="aa757-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="aa757-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="aa757-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="aa757-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="aa757-110">API description</span></span>
<span data-ttu-id="aa757-111">Crée une [alerte en](alerts.md) haut de **l’événement.**</span><span class="sxs-lookup"><span data-stu-id="aa757-111">Creates new [Alert](alerts.md) on top of **Event**.</span></span>
<br><span data-ttu-id="aa757-112">**Microsoft Defender for Endpoint Event est** requis pour la création de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-112">**Microsoft Defender for Endpoint Event** is required for the alert creation.</span></span>
<br><span data-ttu-id="aa757-113">Vous devez fournir 3 paramètres à partir de l’événement dans la demande : l’heure de l’événement, **l’ID** de l’ordinateur et **l’ID de rapport.**</span><span class="sxs-lookup"><span data-stu-id="aa757-113">You will need to supply 3 parameters from the Event in the request: **Event Time**, **Machine ID** and **Report ID**.</span></span> <span data-ttu-id="aa757-114">Voir l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="aa757-114">See example below.</span></span>
<br><span data-ttu-id="aa757-115">Vous pouvez utiliser un événement trouvé dans l’API de recherche avancée ou le portail.</span><span class="sxs-lookup"><span data-stu-id="aa757-115">You can use an event found in Advanced Hunting API or Portal.</span></span>
<br><span data-ttu-id="aa757-116">S’il existe une alerte ouverte sur le même appareil avec le même titre, la nouvelle alerte créée est fusionnée avec elle.</span><span class="sxs-lookup"><span data-stu-id="aa757-116">If there existing an open alert on the same Device with the same Title, the new created alert will be merged with it.</span></span>
<br><span data-ttu-id="aa757-117">Un examen automatique démarre automatiquement sur les alertes créées via l’API.</span><span class="sxs-lookup"><span data-stu-id="aa757-117">An automatic investigation starts automatically on alerts created via the API.</span></span>


## <a name="limitations"></a><span data-ttu-id="aa757-118">Limitations</span><span class="sxs-lookup"><span data-stu-id="aa757-118">Limitations</span></span>
1. <span data-ttu-id="aa757-119">Les limites de taux pour cette API sont de 15 appels par minute.</span><span class="sxs-lookup"><span data-stu-id="aa757-119">Rate limitations for this API are 15 calls per minute.</span></span>


## <a name="permissions"></a><span data-ttu-id="aa757-120">Autorisations</span><span class="sxs-lookup"><span data-stu-id="aa757-120">Permissions</span></span>

<span data-ttu-id="aa757-121">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="aa757-121">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="aa757-122">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="aa757-122">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="aa757-123">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="aa757-123">Permission type</span></span> |   <span data-ttu-id="aa757-124">Autorisation</span><span class="sxs-lookup"><span data-stu-id="aa757-124">Permission</span></span>  |   <span data-ttu-id="aa757-125">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="aa757-125">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="aa757-126">Application</span><span class="sxs-lookup"><span data-stu-id="aa757-126">Application</span></span> |   <span data-ttu-id="aa757-127">Alerts.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa757-127">Alerts.ReadWrite.All</span></span> |  <span data-ttu-id="aa757-128">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="aa757-128">'Read and write all alerts'</span></span>
<span data-ttu-id="aa757-129">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="aa757-129">Delegated (work or school account)</span></span> | <span data-ttu-id="aa757-130">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa757-130">Alert.ReadWrite</span></span> | <span data-ttu-id="aa757-131">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="aa757-131">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="aa757-132">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="aa757-132">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="aa757-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Enquête sur les alertes » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="aa757-133">The user needs to have at least the following role permission: 'Alerts investigation' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="aa757-134">L’utilisateur doit avoir accès à l’appareil associé à l’alerte, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="aa757-134">The user needs to have access to the device associated with the alert, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="aa757-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="aa757-135">HTTP request</span></span>

```
POST https://api.securitycenter.microsoft.com/api/alerts/CreateAlertByReference
```

## <a name="request-headers"></a><span data-ttu-id="aa757-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="aa757-136">Request headers</span></span>

<span data-ttu-id="aa757-137">Nom</span><span class="sxs-lookup"><span data-stu-id="aa757-137">Name</span></span> | <span data-ttu-id="aa757-138">Type</span><span class="sxs-lookup"><span data-stu-id="aa757-138">Type</span></span> | <span data-ttu-id="aa757-139">Description</span><span class="sxs-lookup"><span data-stu-id="aa757-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="aa757-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="aa757-140">Authorization</span></span> | <span data-ttu-id="aa757-141">String</span><span class="sxs-lookup"><span data-stu-id="aa757-141">String</span></span> | <span data-ttu-id="aa757-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="aa757-142">Bearer {token}.</span></span> <span data-ttu-id="aa757-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-143">**Required**.</span></span>
<span data-ttu-id="aa757-144">Content-Type</span><span class="sxs-lookup"><span data-stu-id="aa757-144">Content-Type</span></span> | <span data-ttu-id="aa757-145">String</span><span class="sxs-lookup"><span data-stu-id="aa757-145">String</span></span> | <span data-ttu-id="aa757-146">application/json.</span><span class="sxs-lookup"><span data-stu-id="aa757-146">application/json.</span></span> <span data-ttu-id="aa757-147">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-147">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="aa757-148">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="aa757-148">Request body</span></span>

<span data-ttu-id="aa757-149">Dans le corps de la demande, fournissons les valeurs suivantes (toutes sont obligatoires) :</span><span class="sxs-lookup"><span data-stu-id="aa757-149">In the request body, supply the following values (all are required):</span></span>

<span data-ttu-id="aa757-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="aa757-150">Property</span></span> | <span data-ttu-id="aa757-151">Type</span><span class="sxs-lookup"><span data-stu-id="aa757-151">Type</span></span> | <span data-ttu-id="aa757-152">Description</span><span class="sxs-lookup"><span data-stu-id="aa757-152">Description</span></span>
:---|:---|:---
<span data-ttu-id="aa757-153">eventTime</span><span class="sxs-lookup"><span data-stu-id="aa757-153">eventTime</span></span> | <span data-ttu-id="aa757-154">DateTime(UTC)</span><span class="sxs-lookup"><span data-stu-id="aa757-154">DateTime(UTC)</span></span> | <span data-ttu-id="aa757-155">Heure précise de l’événement en tant que chaîne, tel qu’obtenu à partir d’un chasse avancée.</span><span class="sxs-lookup"><span data-stu-id="aa757-155">The precise time of the event as string, as obtained from advanced hunting.</span></span> <span data-ttu-id="aa757-156">Par exemple, ```2018-08-03T16:45:21.7115183Z``` **obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-156">e.g. ```2018-08-03T16:45:21.7115183Z``` **Required**.</span></span>
<span data-ttu-id="aa757-157">reportId</span><span class="sxs-lookup"><span data-stu-id="aa757-157">reportId</span></span> | <span data-ttu-id="aa757-158">String</span><span class="sxs-lookup"><span data-stu-id="aa757-158">String</span></span> | <span data-ttu-id="aa757-159">ReportId de l’événement, tel qu’obtenu à partir d’un chasse avancée.</span><span class="sxs-lookup"><span data-stu-id="aa757-159">The reportId of the event, as obtained from advanced hunting.</span></span> <span data-ttu-id="aa757-160">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-160">**Required**.</span></span>
<span data-ttu-id="aa757-161">machineId</span><span class="sxs-lookup"><span data-stu-id="aa757-161">machineId</span></span> | <span data-ttu-id="aa757-162">String</span><span class="sxs-lookup"><span data-stu-id="aa757-162">String</span></span> | <span data-ttu-id="aa757-163">ID de l’appareil sur lequel l’événement a été identifié.</span><span class="sxs-lookup"><span data-stu-id="aa757-163">Id of the device on which the event was identified.</span></span> <span data-ttu-id="aa757-164">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-164">**Required**.</span></span>
<span data-ttu-id="aa757-165">Sévérité </span><span class="sxs-lookup"><span data-stu-id="aa757-165">severity</span></span> | <span data-ttu-id="aa757-166">String</span><span class="sxs-lookup"><span data-stu-id="aa757-166">String</span></span> | <span data-ttu-id="aa757-167">Gravité de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-167">Severity of the alert.</span></span> <span data-ttu-id="aa757-168">Les valeurs de propriété sont : « Low » (faible), « Medium » (moyen) et « High » (élevé).</span><span class="sxs-lookup"><span data-stu-id="aa757-168">The property values are: 'Low', 'Medium' and 'High'.</span></span> <span data-ttu-id="aa757-169">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-169">**Required**.</span></span>
<span data-ttu-id="aa757-170">title</span><span class="sxs-lookup"><span data-stu-id="aa757-170">title</span></span> | <span data-ttu-id="aa757-171">String</span><span class="sxs-lookup"><span data-stu-id="aa757-171">String</span></span> | <span data-ttu-id="aa757-172">Titre de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-172">Title for the alert.</span></span> <span data-ttu-id="aa757-173">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-173">**Required**.</span></span>
<span data-ttu-id="aa757-174">description</span><span class="sxs-lookup"><span data-stu-id="aa757-174">description</span></span> | <span data-ttu-id="aa757-175">String</span><span class="sxs-lookup"><span data-stu-id="aa757-175">String</span></span> | <span data-ttu-id="aa757-176">Description de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-176">Description of the alert.</span></span> <span data-ttu-id="aa757-177">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-177">**Required**.</span></span>
<span data-ttu-id="aa757-178">recommendedAction</span><span class="sxs-lookup"><span data-stu-id="aa757-178">recommendedAction</span></span>| <span data-ttu-id="aa757-179">String</span><span class="sxs-lookup"><span data-stu-id="aa757-179">String</span></span> | <span data-ttu-id="aa757-180">Action recommandée par le responsable de la sécurité lors de l’analyse de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-180">Action that is recommended to be taken by security officer when analyzing the alert.</span></span> <span data-ttu-id="aa757-181">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="aa757-181">**Required**.</span></span>
<span data-ttu-id="aa757-182">category</span><span class="sxs-lookup"><span data-stu-id="aa757-182">category</span></span>| <span data-ttu-id="aa757-183">String</span><span class="sxs-lookup"><span data-stu-id="aa757-183">String</span></span> | <span data-ttu-id="aa757-184">Catégorie de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="aa757-184">Category of the alert.</span></span> <span data-ttu-id="aa757-185">Les valeurs de propriété sont : « General », « CommandAndControl », « Collection », « CredentialAccess », « DefenseEvasion », « Discovery », « Exfiltration », « Exploit », « Execution », « InitialAccess », « LateralMovement », « Malware », « Persistence », « PrivilegeEscalation », « Ransomware », « SuspiciousActivity » **Required**.</span><span class="sxs-lookup"><span data-stu-id="aa757-185">The property values are: "General", "CommandAndControl", "Collection", "CredentialAccess", "DefenseEvasion", "Discovery", "Exfiltration", "Exploit", "Execution", "InitialAccess", "LateralMovement", "Malware", "Persistence", "PrivilegeEscalation", "Ransomware", "SuspiciousActivity" **Required**.</span></span>

## <a name="response"></a><span data-ttu-id="aa757-186">Réponse</span><span class="sxs-lookup"><span data-stu-id="aa757-186">Response</span></span>

<span data-ttu-id="aa757-187">Si elle réussit, cette méthode renvoie 200 OK et un nouvel objet [d’alerte](alerts.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="aa757-187">If successful, this method returns 200 OK, and a new [alert](alerts.md) object in the response body.</span></span> <span data-ttu-id="aa757-188">Si l’événement avec les propriétés spécifiées (_reportId_, _eventTime_ et _machineId_) est in trouvé - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="aa757-188">If event with the specified properties (_reportId_, _eventTime_ and _machineId_) was not found - 404 Not Found.</span></span>

## <a name="example"></a><span data-ttu-id="aa757-189">Exemple</span><span class="sxs-lookup"><span data-stu-id="aa757-189">Example</span></span>

<span data-ttu-id="aa757-190">**Demande**</span><span class="sxs-lookup"><span data-stu-id="aa757-190">**Request**</span></span>

<span data-ttu-id="aa757-191">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="aa757-191">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/alerts/CreateAlertByReference
```

```json
{
    "machineId": "1e5bc9d7e413ddd7902c2932e418702b84d0cc07",
    "severity": "Low",
    "title": "example",
    "description": "example alert",
    "recommendedAction": "nothing",
    "eventTime": "2018-08-03T16:45:21.7115183Z",
    "reportId": "20776",
    "category": "Exploit"
}
```
