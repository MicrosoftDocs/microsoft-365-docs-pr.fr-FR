---
title: List machineActions API
description: Découvrez comment utiliser l’API List MachineActions pour récupérer une collection d’actions de l’ordinateur dans Microsoft Defender pour endpoint.
keywords: api, api de graphique, api pris en charge, collection machineaction
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
ms.openlocfilehash: 2ee9a4e29dded3e299ffbb2c2997fd02f32d1abf
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771116"
---
# <a name="list-machineactions-api"></a>List MachineActions API

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)

- Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a>Description de l’API
Récupère une collection d’actions [de l’ordinateur.](machineaction.md)
<br>Prend [en charge les requêtes OData V4.](https://www.odata.org/documentation/)
<br>La requête OData est prise en charge sur ```$filter``` : , et les ```status``` ```machineId``` ```type``` ```requestor``` ```creationDateTimeUtc``` propriétés.
<br>Voir des exemples [dans les requêtes OData avec Microsoft Defender for Endpoint](exposed-apis-odata-samples.md)


## <a name="limitations"></a>Limites
1. La taille maximale de page est de 10 000.
2. Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure. 


## <a name="permissions"></a>Autorisations
L’une des autorisations suivantes est nécessaire pour appeler cette API. Pour en savoir plus, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point de terminaison](apis-intro.md)

Type d’autorisation |   Autorisation  |   Nom d’affichage de l’autorisation
:---|:---|:---
Application |   Machine.Read.All |  « Lire tous les profils d’ordinateur »
Application |   Machine.ReadWrite.All | « Lire et écrire toutes les informations sur l’ordinateur »
Déléguée (compte professionnel ou scolaire) | Machine.Read | « Lire les informations sur l’ordinateur »
Déléguée (compte professionnel ou scolaire) | Machine.ReadWrite | « Lire et écrire des informations sur l’ordinateur »

>[!Note]
> Lors de l’obtention d’un jeton à l’aide des informations d’identification de l’utilisateur :
>- L’utilisateur doit avoir au moins l’autorisation de rôle suivante : « Afficher les données » (voir Créer et gérer des rôles [pour](user-roles.md) plus d’informations)

## <a name="http-request"></a>Requête HTTP
```
GET https://api.securitycenter.microsoft.com/api/machineactions
```

## <a name="request-headers"></a>En-têtes de demande

Nom | Type | Description
:---|:---|:---
Autorisation | String | Porteur {token}. **Obligatoire**.


## <a name="request-body"></a>Corps de la demande
Vide

## <a name="response"></a>Réponse
Si elle réussit, cette méthode renvoie le code de réponse 200, Ok avec une collection [d’entités machineAction.](machineaction.md)


## <a name="example-1"></a>Exemple 1

**Demande**

Voici un exemple de demande sur une organisation qui possède trois MachineActions.

```
GET https://api.securitycenter.microsoft.com/api/machineactions
```

**Réponse**

Voici un exemple de réponse.


```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions",
    "value": [
        {
            "id": "69dc3630-1ccc-4342-acf3-35286eec741d",
            "type": "CollectInvestigationPackage",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:43:57.2011911Z",
            "lastUpdateTimeUtc": "2018-12-04T12:45:25.4049122Z",
            "relatedFileInfo": null
        },
        {
            "id": "2e9da30d-27f6-4208-81f2-9cd3d67893ba",
            "type": "RunAntiVirusScan",
            "scope": "Full",
            "requestor": "Analyst@contoso.com",
            "requestorComment": "Check machine for viruses due to alert 3212",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:18:27.1293487Z",
            "lastUpdateTimeUtc": "2018-12-04T12:18:57.5511934Z",
            "relatedFileInfo": null
        },
        {
            "id": "44cffc15-0e3d-4cbf-96aa-bf76f9b27f5e",
            "type": "StopAndQuarantineFile",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:15:40.6052029Z",
            "lastUpdateTimeUtc": "2018-12-04T12:16:14.2899973Z",
            "relatedFileInfo": {
                "fileIdentifier": "a0c659857ccbe457fdaf5fe21d54efdcbf6f6508",
                "fileIdentifierType": "Sha1"
            }
        }
    ]
}
```

## <a name="example-2"></a>Exemple 2

**Demande**

Voici un exemple de demande qui filtre les MachineActions par ID d’ordinateur et affiche les deux derniers MachineActions.

```
GET https://api.securitycenter.microsoft.com/api/machineactions?$filter=machineId eq 'f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f'&$top=2
```

**Réponse**

Voici un exemple de réponse.

```
HTTP/1.1 200 Ok
Content-type: application/json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#MachineActions",
    "value": [
        {
            "id": "69dc3630-1ccc-4342-acf3-35286eec741d",
            "type": "CollectInvestigationPackage",
            "scope": null,
            "requestor": "Analyst@contoso.com",
            "requestorComment": "test",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:43:57.2011911Z",
            "lastUpdateTimeUtc": "2018-12-04T12:45:25.4049122Z",
            "relatedFileInfo": null
        },
        {
            "id": "2e9da30d-27f6-4208-81f2-9cd3d67893ba",
            "type": "RunAntiVirusScan",
            "scope": "Full",
            "requestor": "Analyst@contoso.com",
            "requestorComment": "Check machine for viruses due to alert 3212",
            "status": "Succeeded",
            "machineId": "f46b9bb259ed4a7fb9981b73510e3cc7aa81ec1f",
            "computerDnsName": "desktop-39g9tgl",
            "creationDateTimeUtc": "2018-12-04T12:18:27.1293487Z",
            "lastUpdateTimeUtc": "2018-12-04T12:18:57.5511934Z",
            "relatedFileInfo": null
        }
    ]
}
```

## <a name="related-topics"></a>Voir aussi
- [Requêtes OData avec Microsoft Defender pour le point de terminaison](exposed-apis-odata-samples.md)
