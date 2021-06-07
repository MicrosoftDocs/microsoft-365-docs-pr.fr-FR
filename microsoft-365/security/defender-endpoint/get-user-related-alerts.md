---
title: API Obtenir les alertes liées à l’utilisateur
description: Récupérer une collection d’alertes liées à un ID d’utilisateur donné à l’aide de Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, utilisateur, associé, alertes
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
ms.openlocfilehash: ab0d0e97365b5ce38b29f2b0d65e3aea48d6c28c
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769928"
---
# <a name="get-user-related-alerts-api"></a><span data-ttu-id="bd144-104">API Obtenir les alertes liées à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bd144-104">Get user-related alerts API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="bd144-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bd144-105">**Applies to:**</span></span>
- [<span data-ttu-id="bd144-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bd144-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="bd144-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bd144-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="bd144-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="bd144-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="bd144-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="bd144-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="bd144-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="bd144-110">API description</span></span>
<span data-ttu-id="bd144-111">Récupère une collection d’alertes liées à un ID d’utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="bd144-111">Retrieves a collection of alerts related to a given user ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="bd144-112">Limitations</span><span class="sxs-lookup"><span data-stu-id="bd144-112">Limitations</span></span>
1. <span data-ttu-id="bd144-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="bd144-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="bd144-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="bd144-114">Permissions</span></span>
<span data-ttu-id="bd144-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="bd144-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="bd144-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="bd144-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="bd144-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="bd144-117">Permission type</span></span> |   <span data-ttu-id="bd144-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bd144-118">Permission</span></span>  |   <span data-ttu-id="bd144-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="bd144-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="bd144-120">Application</span><span class="sxs-lookup"><span data-stu-id="bd144-120">Application</span></span> |   <span data-ttu-id="bd144-121">Alert.Read.All</span><span class="sxs-lookup"><span data-stu-id="bd144-121">Alert.Read.All</span></span> |    <span data-ttu-id="bd144-122">« Lire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="bd144-122">'Read all alerts'</span></span>
<span data-ttu-id="bd144-123">Application</span><span class="sxs-lookup"><span data-stu-id="bd144-123">Application</span></span> |   <span data-ttu-id="bd144-124">Alert.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bd144-124">Alert.ReadWrite.All</span></span> |   <span data-ttu-id="bd144-125">« Lire et écrire toutes les alertes »</span><span class="sxs-lookup"><span data-stu-id="bd144-125">'Read and write all alerts'</span></span>
<span data-ttu-id="bd144-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="bd144-126">Delegated (work or school account)</span></span> | <span data-ttu-id="bd144-127">Alert.Read</span><span class="sxs-lookup"><span data-stu-id="bd144-127">Alert.Read</span></span> | <span data-ttu-id="bd144-128">« Lire les alertes »</span><span class="sxs-lookup"><span data-stu-id="bd144-128">'Read alerts'</span></span>
<span data-ttu-id="bd144-129">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="bd144-129">Delegated (work or school account)</span></span> | <span data-ttu-id="bd144-130">Alert.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bd144-130">Alert.ReadWrite</span></span> | <span data-ttu-id="bd144-131">« Lire et écrire des alertes »</span><span class="sxs-lookup"><span data-stu-id="bd144-131">'Read and write alerts'</span></span>

>[!Note]
> <span data-ttu-id="bd144-132">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="bd144-132">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="bd144-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données ».</span><span class="sxs-lookup"><span data-stu-id="bd144-133">The user needs to have at least the following role permission: 'View Data'.</span></span> <span data-ttu-id="bd144-134">Pour plus d’informations, voir [Créer et gérer des rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="bd144-134">For more information, see [Create and manage roles](user-roles.md).</span></span>
>- <span data-ttu-id="bd144-135">La réponse inclut uniquement les alertes, associées aux appareils, à qui [](machine-groups.md) l’utilisateur a accès, en fonction des paramètres de groupe d’appareils (voir Créer et gérer des groupes d’appareils pour plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="bd144-135">Response will include only alerts, associated with devices, that the user have access to, based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="bd144-136">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="bd144-136">HTTP request</span></span>
```
GET /api/users/{id}/alerts
```

<span data-ttu-id="bd144-137">**L’ID n’est pas l’UPN complet, mais uniquement le nom d’utilisateur. (par exemple, pour récupérer des alertes pour user1@contoso.com utiliser /api/users/user1/alerts)**</span><span class="sxs-lookup"><span data-stu-id="bd144-137">**The ID is not the full UPN, but only the user name. (for example, to retrieve alerts for user1@contoso.com use /api/users/user1/alerts)**</span></span>

## <a name="request-headers"></a><span data-ttu-id="bd144-138">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="bd144-138">Request headers</span></span>

<span data-ttu-id="bd144-139">Nom</span><span class="sxs-lookup"><span data-stu-id="bd144-139">Name</span></span> | <span data-ttu-id="bd144-140">Type</span><span class="sxs-lookup"><span data-stu-id="bd144-140">Type</span></span> | <span data-ttu-id="bd144-141">Description</span><span class="sxs-lookup"><span data-stu-id="bd144-141">Description</span></span>
:---|:---|:---
<span data-ttu-id="bd144-142">Autorisation</span><span class="sxs-lookup"><span data-stu-id="bd144-142">Authorization</span></span> | <span data-ttu-id="bd144-143">String</span><span class="sxs-lookup"><span data-stu-id="bd144-143">String</span></span> | <span data-ttu-id="bd144-144">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="bd144-144">Bearer {token}.</span></span> <span data-ttu-id="bd144-145">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="bd144-145">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="bd144-146">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="bd144-146">Request body</span></span>
<span data-ttu-id="bd144-147">Vide</span><span class="sxs-lookup"><span data-stu-id="bd144-147">Empty</span></span>

## <a name="response"></a><span data-ttu-id="bd144-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="bd144-148">Response</span></span>
<span data-ttu-id="bd144-149">En cas de réussite et si l’utilisateur existe : 200 - OK.</span><span class="sxs-lookup"><span data-stu-id="bd144-149">If successful and user exists - 200 OK.</span></span> <span data-ttu-id="bd144-150">Si l’utilisateur n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="bd144-150">If the user does not exist - 404 Not Found.</span></span> 


## <a name="example"></a><span data-ttu-id="bd144-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd144-151">Example</span></span>

<span data-ttu-id="bd144-152">**Demande**</span><span class="sxs-lookup"><span data-stu-id="bd144-152">**Request**</span></span>

<span data-ttu-id="bd144-153">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="bd144-153">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/users/user1/alerts
```
