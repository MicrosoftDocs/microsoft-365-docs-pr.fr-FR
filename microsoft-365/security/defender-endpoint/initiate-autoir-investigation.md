---
title: DÉMARRER l’API d’examen
description: Utilisez cette API pour lancer l’examen sur un appareil.
keywords: api, api de graphique, api pris en charge, examen
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
ms.openlocfilehash: b7a6a3e7f6f705f322ee3eb1c1b561bc01c55d29
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770888"
---
# <a name="start-investigation-api"></a><span data-ttu-id="7faaf-104">DÉMARRER l’API d’examen</span><span class="sxs-lookup"><span data-stu-id="7faaf-104">Start Investigation API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="7faaf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7faaf-105">**Applies to:**</span></span>
- [<span data-ttu-id="7faaf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7faaf-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7faaf-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7faaf-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7faaf-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="7faaf-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7faaf-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7faaf-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="7faaf-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="7faaf-110">API description</span></span>
<span data-ttu-id="7faaf-111">Lancez un examen automatisé sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="7faaf-111">Start automated investigation on a device.</span></span>
<br><span data-ttu-id="7faaf-112">Pour plus [d’informations, voir Vue d’ensemble des enquêtes](automated-investigations.md) automatisées.</span><span class="sxs-lookup"><span data-stu-id="7faaf-112">See [Overview of automated investigations](automated-investigations.md) for more information.</span></span>


## <a name="limitations"></a><span data-ttu-id="7faaf-113">Limitations</span><span class="sxs-lookup"><span data-stu-id="7faaf-113">Limitations</span></span>
1. <span data-ttu-id="7faaf-114">Les limites de taux pour cette API sont de 50 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="7faaf-114">Rate limitations for this API are 50 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="7faaf-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7faaf-115">Permissions</span></span>
<span data-ttu-id="7faaf-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="7faaf-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="7faaf-117">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="7faaf-117">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="7faaf-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="7faaf-118">Permission type</span></span> |   <span data-ttu-id="7faaf-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7faaf-119">Permission</span></span>  |   <span data-ttu-id="7faaf-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="7faaf-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="7faaf-121">Application</span><span class="sxs-lookup"><span data-stu-id="7faaf-121">Application</span></span> |   <span data-ttu-id="7faaf-122">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7faaf-122">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="7faaf-123">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="7faaf-123">'Read and write all alerts'</span></span>
<span data-ttu-id="7faaf-124">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="7faaf-124">Delegated (work or school account)</span></span> | <span data-ttu-id="7faaf-125">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7faaf-125">Alert.ReadWrite</span></span> | <span data-ttu-id="7faaf-126">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="7faaf-126">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="7faaf-127">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="7faaf-127">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="7faaf-128">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Actions de correction actives » (pour plus d’informations, voir Créer et gérer [des](user-roles.md) rôles)</span><span class="sxs-lookup"><span data-stu-id="7faaf-128">The user needs to have at least the following role permission: 'Active remediation actions' (See [Create and manage roles](user-roles.md) for more information)</span></span>
>- <span data-ttu-id="7faaf-129">L’utilisateur doit avoir accès à l’appareil, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils [pour](machine-groups.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="7faaf-129">The user needs to have access to the device, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>


## <a name="http-request"></a><span data-ttu-id="7faaf-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="7faaf-130">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/machines/{id}/startInvestigation
```

## <a name="request-headers"></a><span data-ttu-id="7faaf-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="7faaf-131">Request headers</span></span>

<span data-ttu-id="7faaf-132">Nom</span><span class="sxs-lookup"><span data-stu-id="7faaf-132">Name</span></span> | <span data-ttu-id="7faaf-133">Type</span><span class="sxs-lookup"><span data-stu-id="7faaf-133">Type</span></span> | <span data-ttu-id="7faaf-134">Description</span><span class="sxs-lookup"><span data-stu-id="7faaf-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="7faaf-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="7faaf-135">Authorization</span></span> | <span data-ttu-id="7faaf-136">String</span><span class="sxs-lookup"><span data-stu-id="7faaf-136">String</span></span> | <span data-ttu-id="7faaf-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="7faaf-137">Bearer {token}.</span></span> <span data-ttu-id="7faaf-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7faaf-138">**Required**.</span></span>
<span data-ttu-id="7faaf-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7faaf-139">Content-Type</span></span> | <span data-ttu-id="7faaf-140">string</span><span class="sxs-lookup"><span data-stu-id="7faaf-140">string</span></span> | <span data-ttu-id="7faaf-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="7faaf-141">application/json.</span></span> <span data-ttu-id="7faaf-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7faaf-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="7faaf-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="7faaf-143">Request body</span></span>
<span data-ttu-id="7faaf-144">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="7faaf-144">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="7faaf-145">Paramètre</span><span class="sxs-lookup"><span data-stu-id="7faaf-145">Parameter</span></span> | <span data-ttu-id="7faaf-146">Type</span><span class="sxs-lookup"><span data-stu-id="7faaf-146">Type</span></span>    | <span data-ttu-id="7faaf-147">Description</span><span class="sxs-lookup"><span data-stu-id="7faaf-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="7faaf-148">Commentaire</span><span class="sxs-lookup"><span data-stu-id="7faaf-148">Comment</span></span> |   <span data-ttu-id="7faaf-149">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7faaf-149">String</span></span> |    <span data-ttu-id="7faaf-150">Commentaire à associer à l’action.</span><span class="sxs-lookup"><span data-stu-id="7faaf-150">Comment to associate with the action.</span></span> <span data-ttu-id="7faaf-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="7faaf-151">**Required**.</span></span>


## <a name="response"></a><span data-ttu-id="7faaf-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="7faaf-152">Response</span></span>
<span data-ttu-id="7faaf-153">Si elle réussit, cette méthode renvoie 201 - Code de réponse créé et [Investigation](investigation.md) dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="7faaf-153">If successful, this method returns 201 - Created response code and [Investigation](investigation.md) in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="7faaf-154">Exemple</span><span class="sxs-lookup"><span data-stu-id="7faaf-154">Example</span></span>

<span data-ttu-id="7faaf-155">**Demande**</span><span class="sxs-lookup"><span data-stu-id="7faaf-155">**Request**</span></span>

<span data-ttu-id="7faaf-156">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="7faaf-156">Here is an example of the request.</span></span>

```https
POST https://api.securitycenter.microsoft.com/api/machines/1e5bc9d7e413ddd7902c2932e418702b84d0cc07/startInvestigation
```

```json
{
  "Comment": "Test investigation"
}
```
