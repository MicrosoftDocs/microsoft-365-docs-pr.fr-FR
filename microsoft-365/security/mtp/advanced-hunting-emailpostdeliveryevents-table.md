---
title: Table EmailPostDeliveryEvents dans le schéma de chasse avancé
description: En savoir plus sur les actions postérieures à la livraison effectuées sur les courriers électroniques Microsoft 365 dans le tableau EmailPostDeliveryEvents du schéma de chasse avancé
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, référence de schéma, Kusto, table, colonne, type de données, description, EmailPostDeliveryEvents, ID de message réseau, expéditeur, destinataire, ID pièce jointe, nom de la pièce jointe, nombre d’URL
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: f4b34abdbfcbd6c3a2f142001a3d486485c86fcd
ms.sourcegitcommit: eee4f651bd51d5aedd64e42d02bfed8ccb9be4cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44515920"
---
# <a name="emailpostdeliveryevents"></a>EmailPostDeliveryEvents

**S’applique à :**
- Protection Microsoft contre les menaces

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

Le `EmailPostDeliveryEvents` tableau du schéma de [chasse avancé](advanced-hunting-overview.md) contient des informations sur les actions postérieures à la livraison effectuées sur les messages électroniques traités par Microsoft 365. Utilisez cette référence pour créer des requêtes qui renvoient des informations de cette table.

Pour obtenir plus d’informations sur les messages électroniques individuels, vous pouvez également utiliser les [`EmailEvents`](advanced-hunting-emailevents-table.md) [`EmailAttachmentInfo`](advanced-hunting-emailattachmentinfo-table.md) tables, et [`EmailUrlInfo`](advanced-hunting-emailurlinfo-table.md) . Pour plus d’informations sur les autres tables du schéma de repérage avancé, [consultez la référence de repérage avancé](advanced-hunting-schema-tables.md).

| Nom de colonne | Type de données | Description |
|-------------|-----------|-------------|
| `Timestamp` | DateHeure | Date et heure d’enregistrement de l’événement |
| `EventId` | string | Identificateur unique de l’événement |
| `NetworkMessageId` | string | Identificateur unique pour le courrier électronique, généré par Microsoft 365 |
| `InternetMessageId` | string | Identificateur public de l’e-mail défini par le système de courrier d’envoi |
| `Action` | string | Action effectuée sur l’entité |
| `ActionType` | string | Type d’activité qui a déclenché l’événement : correction manuelle, hameçonnage ZAP, programme malveillant ZAP |
| `ActionTrigger` | string | Indique si une action a été déclenchée par un administrateur (manuellement ou par l’approbation d’une action automatisée en attente) ou par un mécanisme spécial, tel qu’un ZAP ou une remise dynamique. |
| `ActionResult` | string | Résultat de l’action |
| `RecipientEmailAddress` | string | Adresse e-mail du destinataire ou adresse e-mail du destinataire après extension de la liste de distribution |
| `DeliveryLocation` | chaîne | Emplacement de remise du courrier électronique : boîte de réception/dossier, local/externe, courrier indésirable, quarantaine, échec, supprimé, éléments supprimés |

## <a name="supported-event-types"></a>Types d’événements pris en charge
Cette table capture les événements avec les `ActionType` valeurs suivantes :

- **Correction manuelle** : un administrateur a effectué manuellement une action sur un message électronique une fois qu’il a été remis à la boîte aux lettres de l’utilisateur. Cela inclut les actions effectuées manuellement via l' [Explorateur de menaces](../office-365-security/threat-explorer.md) ou les approbations d' [actions d’enquête et de réponse (air) automatisées](mtp-autoir-actions.md).
- **Hameçonnage zap** – [purge automatique avec zéro heure (ZAP)](../office-365-security/zero-hour-auto-purge.md) a effectué une action sur un e-mail de hameçonnage après la remise.
- **Programme malveillant zap** – la purge automatique à zéro heure (ZAP) a effectué une action sur un message électronique contenant un programme malveillant après la remise.

## <a name="related-topics"></a>Sujets associés
- [Repérage proactif des menaces](advanced-hunting-overview.md)
- [Apprendre le langage de requête](advanced-hunting-query-language.md)
- [Utiliser des requêtes partagées](advanced-hunting-shared-queries.md)
- [Repérer les menaces sur divers appareils et e-mails](advanced-hunting-query-emails-devices.md)
- [Comprendre le schéma](advanced-hunting-schema-tables.md)
- [Appliquer les meilleures pratiques de requête](advanced-hunting-best-practices.md)