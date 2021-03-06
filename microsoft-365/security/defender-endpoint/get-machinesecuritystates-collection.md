---
title: API obtenir la collection d’états de sécurité des ordinateurs
description: Récupérez une collection d’états de sécurité d’appareil à l’aide de Microsoft Defender for Endpoint.
keywords: api, api de graphique, api pris en charge, obtenir, appareil, sécurité, état
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: leonidzh
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 9dab4bdccc1fead5bc2cc5b9bdff8f2a45b6c8db
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51200364"
---
# <a name="get-machines-security-states-collection-api"></a>API obtenir la collection d’états de sécurité des ordinateurs

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)

- Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

Récupère une collection d’états de sécurité des appareils.

## <a name="permissions"></a>Autorisations
L’utilisateur a besoin d’autorisations de lecture.

## <a name="http-request"></a>Requête HTTP
```
GET /testwdatppreview/machinesecuritystates
```

## <a name="request-headers"></a>En-têtes de demande

En-tête | Valeur 
:---|:---
Autorisation | Porteur {token}. **Obligatoire**.
Type de contenu | application/json

## <a name="request-body"></a>Corps de la demande
Vide

## <a name="response"></a>Réponse
En cas de réussite : 200 - OK.

## <a name="example"></a>Exemple

**Demande**

Voici un exemple de demande.

```
GET https://graph.microsoft.com/testwdatppreview/machinesecuritystates
Content-type: application/json
```

**Réponse**

Voici un exemple de réponse.
*L’ID de* champ contient l’ID de l’appareil et est égal à l’ID *de* champ * dans les informations sur les appareils. 

```
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context":"https://graph.microsoft.com/testwdatppreview/$metadata#MachineSecurityStates",
    "@odata.count":444,
    "@odata.nextLink":"https://graph.microsoft.com/testwdatppreview/machinesecuritystates?$skiptoken=[continuation token]",
    "value":[
        {
            "id":"000050e1b4afeee3742489ede9ad7a3e16bbd9c4",
            "build":14393,
            "revision":2485,
            "architecture":"Amd64",
            "osVersion":"10.0.14393.2485.amd64fre.rs1_release.180827-1809",
            "propertiesRequireAttention":[
                "AntivirusNotReporting",
                "EdrImpairedCommunications"
            ]
        },
        …
    ]
}
```
