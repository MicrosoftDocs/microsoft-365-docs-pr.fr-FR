---
title: API Obtenir les statistiques de domaine
description: Découvrez comment utiliser l’API Obtenir des statistiques de domaine pour récupérer les statistiques sur le domaine donné dans Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, domaine, appareils associés à un domaine
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
ms.openlocfilehash: 50b05b98ba507e120bbd6a3dc09f4633dac3a005
ms.sourcegitcommit: 787fb30fdae6d49347a87f4baae3cd140067e573
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52998775"
---
# <a name="get-domain-statistics-api"></a>API Obtenir les statistiques de domaine

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a>Description de l’API
Récupère les statistiques sur le domaine donné.


## <a name="limitations"></a>Limites
1. Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.


## <a name="permissions"></a>Autorisations
L’une des autorisations suivantes est nécessaire pour appeler cette API. Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)

Type d’autorisation |   Autorisation  |   Nom d’affichage de l’autorisation
:---|:---|:---
Application |   URL. Read.All |  « Lire les URL »
Déléguée (compte professionnel ou scolaire) | URL. Read.All | « Lire les URL »

>[!Note]
> Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :
>- L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)

## <a name="http-request"></a>Requête HTTP
```
GET /api/domains/{domain}/stats
```

## <a name="request-headers"></a>En-têtes de demande

En-tête | Valeur 
:---|:---
Autorisation | Porteur {token}. **Obligatoire**.

## <a name="request-uri-parameters"></a>Paramètres d’URI de demande

Nom | Type | Description
:---|:---|:---
lookBackHours | Int32 | Définit les heures pendant les recherches pour obtenir les statistiques. La valeur par défaut est 30 jours. **Facultatif**.

## <a name="request-body"></a>Corps de la demande
Vide

## <a name="response"></a>Réponse
En cas de réussite et si le domaine existe : 200 - OK, avec un objet statistiques dans le corps de la réponse. Si le domaine n’existe pas - 404 - In trouvé.


## <a name="example"></a>Exemple

**Demande**

Voici un exemple de demande.

```http
GET https://api.securitycenter.microsoft.com/api/domains/example.com/stats?lookBackHours=48
```

**Réponse**

Voici un exemple de réponse.


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#microsoft.windowsDefenderATP.api.InOrgDomainStats",
    "host": "example.com",
    "organizationPrevalence": 4070,
    "orgFirstSeen": "2017-07-30T13:23:48Z",
    "orgLastSeen": "2017-08-29T13:09:05Z"
}
```
