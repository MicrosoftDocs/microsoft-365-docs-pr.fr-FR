---
title: Diffuser des événements Microsoft Defender for Endpoint vers des Hubs d’événements Azure
description: Découvrez comment configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers votre Hub d’événements.
keywords: exportation de données brutes, API de diffusion en continu, API, Hubs d’événements Azure, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
search.product: eADQiWindows 10XVcnh
search.appverid: met150
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
ms.openlocfilehash: 8985a40c99ad4db9710dfbf9805d537a921f6c96
ms.sourcegitcommit: f0118e61e490496cb23189cc5c73b23e2ba939be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52780164"
---
# <a name="configure-microsoft-defender-for-endpoint-to-stream-advanced-hunting-events-to-your-azure-event-hubs"></a>Configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers vos Hubs d’événements Azure

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**

- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)

> Vous souhaitez faire l’expérience de Defender pour point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="before-you-begin"></a>Avant de commencer

1. Créez [un hub d’événements](/azure/event-hubs/) dans votre client.

2. Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)go to **Subscriptions > Your subscription > Resource Providers > Register to **Microsoft.insights****.

## <a name="enable-raw-data-streaming"></a>Activer la diffusion en continu des données brutes

1. Connectez-vous au [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com) en tant **qu’administrateur** général * ou _*_Administrateur_ de sécurité **.

2. Go to the [Data export settings page](https://securitycenter.windows.com/interoperability/dataexport) on Centre de sécurité Microsoft Defender.

3. Cliquez sur **Ajouter des paramètres d’exportation de données.**

4. Choisissez un nom pour vos nouveaux paramètres.

5. Choose **Forward events to Azure Event Hubs**.

6. Tapez le **nom de vos Hubs d’événements** et votre ID de ressource Event **Hubs.**

   Pour obtenir votre ID de ressource **Event Hubs,** rendez-vous sur votre page d’espace de noms Azure Event Hubs sous l’onglet Propriétés [d’Azure](https://ms.portal.azure.com/) > > copiez le texte sous **L’ID** de ressource :

   ![Image de l’ID1 de ressource du hub d’événements](images/event-hub-resource-id.png)

7. Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**

## <a name="the-schema-of-the-events-in-azure-event-hubs"></a>Schéma des événements dans les Hubs d’événements Azure

```
{
    "records": [
                    {
                        "time": "<The time WDATP received the event>"
                        "tenantId": "<The Id of the tenant that the event belongs to>"
                        "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
                        "properties": { <WDATP Advanced Hunting event as Json> }
                    }
                    ...
                ]
}
```

- Chaque message de hub d’événements dans Azure Event Hubs contient la liste des enregistrements.

- Chaque enregistrement contient le nom de l’événement, le moment où Microsoft Defender pour le point de terminaison a reçu l’événement, le client qu’il appartient (vous obtenez uniquement des événements de votre client) et l’événement au format JSON dans une propriété appelée **«** properties ».

- Pour plus d’informations sur le schéma des événements Microsoft Defender for Endpoint, consultez [la vue d’ensemble de la recherche avancée.](advanced-hunting-overview.md)

- Dans la recherche avancée, la table **DeviceInfo** comporte une colonne nommée **MachineGroup** qui contient le groupe de l’appareil. Ici, chaque événement est également décorée avec cette colonne. Pour plus [d’informations,](machine-groups.md) voir Groupes d’appareils.

## <a name="data-types-mapping"></a>Mappage des types de données

Pour obtenir les types de données pour les propriétés d’événement, faites les choses suivantes :

1. Connectez-vous [Centre de sécurité Microsoft Defender](https://securitycenter.windows.com) et allez à la [page Recherche avancée.](https://securitycenter.windows.com/hunting-package)

2. Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :
 
   ```
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- Voici un exemple d’événement Device Info : 

  ![Image de l’ID2 de ressource du hub d’événements](images/machine-info-datatype-example.png)

## <a name="related-topics"></a>Voir aussi
- [Vue d’ensemble du chasse avancée](advanced-hunting-overview.md)
- [API de diffusion en continu microsoft Defender pour point de terminaison](raw-data-export.md)
- [Diffuser des événements Microsoft Defender for Endpoint vers votre compte de stockage Azure](raw-data-export-storage.md)
- [Documentation Azure Event Hubs](/azure/event-hubs/)
- [Résoudre les problèmes de connectivité : Hubs d’événements Azure](/azure/event-hubs/troubleshooting-guide)