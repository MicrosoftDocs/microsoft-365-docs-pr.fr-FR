---
title: Obtenir les logiciels installés
description: Récupère une collection de logiciels installés liés à un ID d’appareil donné.
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, inventaire logiciel, logiciels installés par appareil, api de gestion des menaces & vulnérabilité, api tvm mdatp
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6164020ef05561563fe0434bd2edac8c7b3e689a
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166534"
---
# <a name="get-installed-software"></a><span data-ttu-id="00789-104">Obtenir les logiciels installés</span><span class="sxs-lookup"><span data-stu-id="00789-104">Get installed software</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="00789-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="00789-105">**Applies to:**</span></span>
- [<span data-ttu-id="00789-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="00789-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="00789-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="00789-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="00789-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="00789-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="00789-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="00789-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="00789-110">Récupère une collection de logiciels installés liés à un ID d’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="00789-110">Retrieves a collection of installed software related to a given device ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="00789-111">Autorisations</span><span class="sxs-lookup"><span data-stu-id="00789-111">Permissions</span></span>
<span data-ttu-id="00789-112">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="00789-112">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="00789-113">Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="00789-113">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)</span></span>

<span data-ttu-id="00789-114">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="00789-114">Permission type</span></span> |   <span data-ttu-id="00789-115">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00789-115">Permission</span></span>  |   <span data-ttu-id="00789-116">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="00789-116">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="00789-117">Application</span><span class="sxs-lookup"><span data-stu-id="00789-117">Application</span></span> |<span data-ttu-id="00789-118">Software.Read.All</span><span class="sxs-lookup"><span data-stu-id="00789-118">Software.Read.All</span></span> |    <span data-ttu-id="00789-119">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="00789-119">'Read Threat and Vulnerability Management Software information'</span></span>
<span data-ttu-id="00789-120">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="00789-120">Delegated (work or school account)</span></span> | <span data-ttu-id="00789-121">Software.Read</span><span class="sxs-lookup"><span data-stu-id="00789-121">Software.Read</span></span> |    <span data-ttu-id="00789-122">« Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="00789-122">'Read Threat and Vulnerability Management Software information'</span></span>

## <a name="http-request"></a><span data-ttu-id="00789-123">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="00789-123">HTTP request</span></span>
```
GET /api/machines/{machineId}/software
```

## <a name="request-headers"></a><span data-ttu-id="00789-124">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="00789-124">Request headers</span></span>

<span data-ttu-id="00789-125">Nom</span><span class="sxs-lookup"><span data-stu-id="00789-125">Name</span></span> | <span data-ttu-id="00789-126">Type</span><span class="sxs-lookup"><span data-stu-id="00789-126">Type</span></span> | <span data-ttu-id="00789-127">Description</span><span class="sxs-lookup"><span data-stu-id="00789-127">Description</span></span>
:---|:---|:---
<span data-ttu-id="00789-128">Autorisation</span><span class="sxs-lookup"><span data-stu-id="00789-128">Authorization</span></span> | <span data-ttu-id="00789-129">Chaîne</span><span class="sxs-lookup"><span data-stu-id="00789-129">String</span></span> | <span data-ttu-id="00789-130">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="00789-130">Bearer {token}.</span></span> <span data-ttu-id="00789-131">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="00789-131">**Required**.</span></span>


## <a name="request-body"></a><span data-ttu-id="00789-132">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="00789-132">Request body</span></span>
<span data-ttu-id="00789-133">Vide</span><span class="sxs-lookup"><span data-stu-id="00789-133">Empty</span></span>

## <a name="response"></a><span data-ttu-id="00789-134">Réponse</span><span class="sxs-lookup"><span data-stu-id="00789-134">Response</span></span>
<span data-ttu-id="00789-135">Si elle réussit, cette méthode renvoie 200 OK avec les informations logicielles installées dans le corps.</span><span class="sxs-lookup"><span data-stu-id="00789-135">If successful, this method returns 200 OK with the installed software information in the body.</span></span>


## <a name="example"></a><span data-ttu-id="00789-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="00789-136">Example</span></span>

<span data-ttu-id="00789-137">**Demande**</span><span class="sxs-lookup"><span data-stu-id="00789-137">**Request**</span></span>

<span data-ttu-id="00789-138">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="00789-138">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/machines/ac233fa6208e1579620bf44207c4006ed7cc4501/software
```

<span data-ttu-id="00789-139">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="00789-139">**Response**</span></span>

<span data-ttu-id="00789-140">Voici un exemple de la réponse.</span><span class="sxs-lookup"><span data-stu-id="00789-140">Here is an example of the response.</span></span>


```
{
"@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Software",
"value": [
        {
"id": "microsoft-_-internet_explorer",
"name": "internet_explorer",
"vendor": "microsoft",
"weaknesses": 67,
"publicExploit": true,
"activeAlert": false,
"exposedMachines": 42115,
"impactScore": 46.2037163
        }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="00789-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00789-141">See also</span></span>

- [<span data-ttu-id="00789-142">Gestion des menaces & vulnérabilité basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="00789-142">Risk-based Threat & Vulnerability Management</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [<span data-ttu-id="00789-143">Inventaire des logiciels de vulnérabilité & menace</span><span class="sxs-lookup"><span data-stu-id="00789-143">Threat & Vulnerability software inventory</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/tvm-software-inventory)
