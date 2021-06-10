---
title: Rechercher des appareils par API de balise
description: Rechercher tous les appareils qui contiennent une balise specifc
keywords: api, api pris en charge, obtenir, appareil, rechercher, rechercher un appareil, par balise, balise
search.product: eADQiWindows 10XVcnh
ms.prod: w10
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
ms.openlocfilehash: 88ad63d8b7cc71f7d3f809c7cb0371fc41bb9f5d
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771164"
---
# <a name="find-devices-by-tag-api"></a><span data-ttu-id="89000-104">Rechercher des appareils par API de balise</span><span class="sxs-lookup"><span data-stu-id="89000-104">Find devices by tag API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="89000-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="89000-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="89000-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="89000-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="89000-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="89000-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="89000-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="89000-108">API description</span></span>
<span data-ttu-id="89000-109">Rechercher [des ordinateurs](machine.md) par [balise](machine-tags.md).</span><span class="sxs-lookup"><span data-stu-id="89000-109">Find [Machines](machine.md) by [Tag](machine-tags.md).</span></span>
<br><span data-ttu-id="89000-110">```startswith``` est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="89000-110">```startswith``` query is supported.</span></span> 

## <a name="limitations"></a><span data-ttu-id="89000-111">Limites</span><span class="sxs-lookup"><span data-stu-id="89000-111">Limitations</span></span>
1. <span data-ttu-id="89000-112">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="89000-112">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>


## <a name="permissions"></a><span data-ttu-id="89000-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="89000-113">Permissions</span></span>
<span data-ttu-id="89000-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="89000-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="89000-115">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="89000-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="89000-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="89000-116">Permission type</span></span> |   <span data-ttu-id="89000-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="89000-117">Permission</span></span>  |   <span data-ttu-id="89000-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="89000-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="89000-119">Application</span><span class="sxs-lookup"><span data-stu-id="89000-119">Application</span></span> |   <span data-ttu-id="89000-120">Machine.Read.All</span><span class="sxs-lookup"><span data-stu-id="89000-120">Machine.Read.All</span></span> |  <span data-ttu-id="89000-121">« Lire tous les profils d’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="89000-121">'Read all machine profiles'</span></span>
<span data-ttu-id="89000-122">Application</span><span class="sxs-lookup"><span data-stu-id="89000-122">Application</span></span> |   <span data-ttu-id="89000-123">Machine.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89000-123">Machine.ReadWrite.All</span></span> | <span data-ttu-id="89000-124">« Lire et écrire toutes les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="89000-124">'Read and write all machine information'</span></span>
<span data-ttu-id="89000-125">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="89000-125">Delegated (work or school account)</span></span> | <span data-ttu-id="89000-126">Machine.Read</span><span class="sxs-lookup"><span data-stu-id="89000-126">Machine.Read</span></span> | <span data-ttu-id="89000-127">« Lire les informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="89000-127">'Read machine information'</span></span>
<span data-ttu-id="89000-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="89000-128">Delegated (work or school account)</span></span> | <span data-ttu-id="89000-129">Machine.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="89000-129">Machine.ReadWrite</span></span> | <span data-ttu-id="89000-130">« Lire et écrire des informations sur l’ordinateur »</span><span class="sxs-lookup"><span data-stu-id="89000-130">'Read and write machine information'</span></span>

>[!Note]
> <span data-ttu-id="89000-131">Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="89000-131">When obtaining a token using user credentials:</span></span>
> - <span data-ttu-id="89000-132">La réponse inclut uniquement les appareils accessibles par l’utilisateur en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils). [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="89000-132">Response will include only devices that the user have access to based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>
> - <span data-ttu-id="89000-133">L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)</span><span class="sxs-lookup"><span data-stu-id="89000-133">The user needs to have at least the following role permission: 'View Data' (See [Create and manage roles](user-roles.md) for more information)</span></span>
> - <span data-ttu-id="89000-134">La réponse inclut uniquement les appareils accessibles par l’utilisateur en fonction des paramètres de groupe d’appareils (pour plus d’informations, voir Créer et gérer des groupes d’appareils). [](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="89000-134">Response will include only devices that the user have access to based on device group settings (See [Create and manage device groups](machine-groups.md) for more information)</span></span>

## <a name="http-request"></a><span data-ttu-id="89000-135">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="89000-135">HTTP request</span></span>
```
GET /api/machines/findbytag?tag={tag}&useStartsWithFilter={true/false}
```

## <a name="request-headers"></a><span data-ttu-id="89000-136">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="89000-136">Request headers</span></span>

<span data-ttu-id="89000-137">Nom</span><span class="sxs-lookup"><span data-stu-id="89000-137">Name</span></span> | <span data-ttu-id="89000-138">Type</span><span class="sxs-lookup"><span data-stu-id="89000-138">Type</span></span> | <span data-ttu-id="89000-139">Description</span><span class="sxs-lookup"><span data-stu-id="89000-139">Description</span></span>
:---|:---|:---
<span data-ttu-id="89000-140">Autorisation</span><span class="sxs-lookup"><span data-stu-id="89000-140">Authorization</span></span> | <span data-ttu-id="89000-141">String</span><span class="sxs-lookup"><span data-stu-id="89000-141">String</span></span> | <span data-ttu-id="89000-142">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="89000-142">Bearer {token}.</span></span> <span data-ttu-id="89000-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="89000-143">**Required**.</span></span>

## <a name="request-uri-parameters"></a><span data-ttu-id="89000-144">Paramètres d’URI de demande</span><span class="sxs-lookup"><span data-stu-id="89000-144">Request URI parameters</span></span>

<span data-ttu-id="89000-145">Nom</span><span class="sxs-lookup"><span data-stu-id="89000-145">Name</span></span> | <span data-ttu-id="89000-146">Type</span><span class="sxs-lookup"><span data-stu-id="89000-146">Type</span></span> | <span data-ttu-id="89000-147">Description</span><span class="sxs-lookup"><span data-stu-id="89000-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="89000-148">tag</span><span class="sxs-lookup"><span data-stu-id="89000-148">tag</span></span> | <span data-ttu-id="89000-149">String</span><span class="sxs-lookup"><span data-stu-id="89000-149">String</span></span> | <span data-ttu-id="89000-150">Nom de la balise.</span><span class="sxs-lookup"><span data-stu-id="89000-150">The tag name.</span></span> <span data-ttu-id="89000-151">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="89000-151">**Required**.</span></span>
<span data-ttu-id="89000-152">useStartsWithFilter</span><span class="sxs-lookup"><span data-stu-id="89000-152">useStartsWithFilter</span></span> | <span data-ttu-id="89000-153">Booléen</span><span class="sxs-lookup"><span data-stu-id="89000-153">Boolean</span></span> | <span data-ttu-id="89000-154">Si la valeur est true, la recherche recherche tous les appareils dont le nom de balise commence par la balise donnée dans la requête.</span><span class="sxs-lookup"><span data-stu-id="89000-154">When set to true, the search will find all devices with tag name that starts with the given tag in the query.</span></span> <span data-ttu-id="89000-155">Par défaut est faux.</span><span class="sxs-lookup"><span data-stu-id="89000-155">Defaults to false.</span></span> <span data-ttu-id="89000-156">**Facultatif**.</span><span class="sxs-lookup"><span data-stu-id="89000-156">**Optional**.</span></span>

## <a name="request-body"></a><span data-ttu-id="89000-157">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="89000-157">Request body</span></span>
<span data-ttu-id="89000-158">Vide</span><span class="sxs-lookup"><span data-stu-id="89000-158">Empty</span></span>

## <a name="response"></a><span data-ttu-id="89000-159">Réponse</span><span class="sxs-lookup"><span data-stu-id="89000-159">Response</span></span>
<span data-ttu-id="89000-160">En cas de réussite - 200 OK avec la liste des ordinateurs dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="89000-160">If successful - 200 OK with list of the machines in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89000-161">Exemple</span><span class="sxs-lookup"><span data-stu-id="89000-161">Example</span></span>

<span data-ttu-id="89000-162">**Demande**</span><span class="sxs-lookup"><span data-stu-id="89000-162">**Request**</span></span>

<span data-ttu-id="89000-163">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="89000-163">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/findbytag?tag=testTag&useStartsWithFilter=true
```