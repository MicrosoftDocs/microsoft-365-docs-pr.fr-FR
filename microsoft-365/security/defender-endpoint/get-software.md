---
title: Répertorier les logiciels
description: Récupère une liste d’inventaire logiciel
keywords: api, api de graphique, api pris en charge, obtenir, liste, fichier, informations, inventaire logiciel, api & gestion des vulnérabilités menace, Api Tvm Microsoft Defender pour Endpoint
search.product: eADQiWindows 10XVcnh
ms.prod: w10
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 2b7375f04094cdb56b0801adf2c1c0b7a8ab3098
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844273"
---
# <a name="list-software-inventory-api"></a>API d’inventaire de logiciels de liste

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)

- Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

Récupère l’inventaire logiciel de l’organisation.

## <a name="permissions"></a>Autorisations
L’une des autorisations suivantes est nécessaire pour appeler cette API. Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.

Type d’autorisation |   Autorisation  |   Nom d’affichage de l’autorisation
:---|:---|:---
Application |Software.Read.All |    « Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »
Déléguée (compte professionnel ou scolaire) | Software.Read |    « Lire les informations sur les logiciels de gestion des menaces et des vulnérabilités »

## <a name="http-request"></a>Requête HTTP
```
GET /api/Software
```

## <a name="request-headers"></a>En-têtes de demande

Nom | Type | Description
:---|:---|:---
Autorisation | String | Porteur {token}. **Obligatoire**.


## <a name="request-body"></a>Corps de la demande
Vide

## <a name="response"></a>Réponse
Si elle réussit, cette méthode renvoie 200 OK avec l’inventaire logiciel dans le corps.


## <a name="example"></a>Exemple

**Demande**

Voici un exemple de demande.

```
GET https://api.securitycenter.microsoft.com/api/Software
```

**Réponse**

Voici un exemple de réponse.


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Software",
    "value": [
            {
                "id": "microsoft-_-edge",
                "name": "edge",
                "vendor": "microsoft",
                "weaknesses": 467,
                "publicExploit": true,
                "activeAlert": false,
                "exposedMachines": 172,
                "impactScore": 2.39947438
            }
            ...
        ]
}
```

## <a name="related-topics"></a>Voir aussi
- [Gestion des menaces & vulnérabilité basée sur les risques](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [Inventaire des logiciels de vulnérabilité & menace](/microsoft-365/security/defender-endpoint/tvm-software-inventory)
