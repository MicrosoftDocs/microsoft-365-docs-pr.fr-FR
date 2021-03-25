---
title: API Obtenir les ordinateurs liés à l’utilisateur
description: Découvrez comment utiliser l’API Obtenir des ordinateurs liés à l’utilisateur pour récupérer une collection d’appareils liés à un ID d’utilisateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, obtenir, utilisateur, alertes associées à l’utilisateur
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
ms.technology: mde
ms.openlocfilehash: 135dc1d76a1a90cd7fffba0638211d716865cb0c
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166533"
---
# <a name="get-user-related-machines-api"></a><span data-ttu-id="1cad6-104">API Obtenir les ordinateurs liés à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1cad6-104">Get user-related machines API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1cad6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1cad6-105">**Applies to:**</span></span>
- [<span data-ttu-id="1cad6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1cad6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="1cad6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1cad6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1cad6-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1cad6-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1cad6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1cad6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="1cad6-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="1cad6-110">API description</span></span>
<span data-ttu-id="1cad6-111">Récupère une collection d’appareils liés à un ID d’utilisateur donné.</span><span class="sxs-lookup"><span data-stu-id="1cad6-111">Retrieves a collection of devices related to a given user ID.</span></span>


## <a name="limitations"></a><span data-ttu-id="1cad6-112">Limites</span><span class="sxs-lookup"><span data-stu-id="1cad6-112">Limitations</span></span>
1. <span data-ttu-id="1cad6-113">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="1cad6-113">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="1cad6-114">Autorisations</span><span class="sxs-lookup"><span data-stu-id="1cad6-114">Permissions</span></span>
<span data-ttu-id="1cad6-115">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="1cad6-115">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1cad6-116">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="1cad6-116">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="1cad6-117">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="1cad6-117">Permission type</span></span> |   <span data-ttu-id="1cad6-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1cad6-118">Permission</span></span>  |   <span data-ttu-id="1cad6-119">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="1cad6-119">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="1cad6-120">Application</span><span class="sxs-lookup"><span data-stu-id="1cad6-120">Application</span></span> |   <span data-ttu-id="1cad6-121">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="1cad6-121">Machine.Read.All</span></span> |  <span data-ttu-id="1cad6-122">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1cad6-122">'Read all machine profiles'</span></span>
<span data-ttu-id="1cad6-123">Application</span><span class="sxs-lookup"><span data-stu-id="1cad6-123">Application</span></span> |   <span data-ttu-id="1cad6-124">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1cad6-124">Machine.ReadWrite.All</span></span> | <span data-ttu-id="1cad6-125">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1cad6-125">'Read and write all machine information'</span></span>
<span data-ttu-id="1cad6-126">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1cad6-126">Delegated (work or school account)</span></span> | <span data-ttu-id="1cad6-127">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="1cad6-127">Machine.Read</span></span> | <span data-ttu-id="1cad6-128">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1cad6-128">'Read machine information'</span></span>
<span data-ttu-id="1cad6-129">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="1cad6-129">Delegated (work or school account)</span></span> | <span data-ttu-id="1cad6-130">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1cad6-130">Machine.ReadWrite</span></span> | <span data-ttu-id="1cad6-131">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="1cad6-131">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="1cad6-132">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="1cad6-132">When obtaining a token using user credentials:</span></span>
>- <span data-ttu-id="1cad6-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données ».</span><span class="sxs-lookup"><span data-stu-id="1cad6-133">The user needs to have at least the following role permission: 'View Data'.</span></span> <span data-ttu-id="1cad6-134">Pour plus d’informations, voir [Créer et gérer des rôles](user-roles.md) )</span><span class="sxs-lookup"><span data-stu-id="1cad6-134">For more information, see [Create and manage roles](user-roles.md) )</span></span>
>- <span data-ttu-id="1cad6-135">La réponse inclut uniquement les appareils accessibles à l’utilisateur, en fonction des paramètres de groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="1cad6-135">Response will include only devices that the user can access, based on device group settings.</span></span> <span data-ttu-id="1cad6-136">Pour plus d’informations, voir [Créer et gérer des groupes d’appareils.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="1cad6-136">For more information, see [Create and manage device groups](machine-groups.md).</span></span>

## <a name="http-request"></a><span data-ttu-id="1cad6-137">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1cad6-137">HTTP request</span></span>
```
GET /api/users/{id}/machines
```

<span data-ttu-id="1cad6-138">**L’ID n’est pas l’UPN complet, mais uniquement le nom d’utilisateur. (par exemple, pour récupérer des ordinateurs user1@contoso.com utiliser /api/users/user1/machines)**</span><span class="sxs-lookup"><span data-stu-id="1cad6-138">**The ID is not the full UPN, but only the user name. (for example, to retrieve machines for user1@contoso.com use /api/users/user1/machines)**</span></span>


## <a name="request-headers"></a><span data-ttu-id="1cad6-139">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1cad6-139">Request headers</span></span>

<span data-ttu-id="1cad6-140">Nom</span><span class="sxs-lookup"><span data-stu-id="1cad6-140">Name</span></span> | <span data-ttu-id="1cad6-141">Type</span><span class="sxs-lookup"><span data-stu-id="1cad6-141">Type</span></span> | <span data-ttu-id="1cad6-142">Description</span><span class="sxs-lookup"><span data-stu-id="1cad6-142">Description</span></span>
:---|:---|:---
<span data-ttu-id="1cad6-143">Autorisation</span><span class="sxs-lookup"><span data-stu-id="1cad6-143">Authorization</span></span> | <span data-ttu-id="1cad6-144">Chaîne</span><span class="sxs-lookup"><span data-stu-id="1cad6-144">String</span></span> | <span data-ttu-id="1cad6-145">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="1cad6-145">Bearer {token}.</span></span> <span data-ttu-id="1cad6-146">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="1cad6-146">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="1cad6-147">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1cad6-147">Request body</span></span>
<span data-ttu-id="1cad6-148">Vide</span><span class="sxs-lookup"><span data-stu-id="1cad6-148">Empty</span></span>

## <a name="response"></a><span data-ttu-id="1cad6-149">Réponse</span><span class="sxs-lookup"><span data-stu-id="1cad6-149">Response</span></span>
<span data-ttu-id="1cad6-150">En cas de réussite et si l’utilisateur existe : 200 - OK avec la liste des entités de [l’ordinateur](machine.md) dans le corps.</span><span class="sxs-lookup"><span data-stu-id="1cad6-150">If successful and user exists - 200 OK with list of [machine](machine.md) entities in the body.</span></span> <span data-ttu-id="1cad6-151">Si l’utilisateur n’existe pas - 404 - In trouvé.</span><span class="sxs-lookup"><span data-stu-id="1cad6-151">If user does not exist - 404 Not Found.</span></span>


## <a name="example"></a><span data-ttu-id="1cad6-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="1cad6-152">Example</span></span>

<span data-ttu-id="1cad6-153">**Demande**</span><span class="sxs-lookup"><span data-stu-id="1cad6-153">**Request**</span></span>

<span data-ttu-id="1cad6-154">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="1cad6-154">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/users/user1/machines
```
