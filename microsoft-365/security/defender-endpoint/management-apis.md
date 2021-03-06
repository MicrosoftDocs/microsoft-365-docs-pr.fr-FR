---
title: Vue d’ensemble de la gestion et des API
ms.reviewer: ''
description: En savoir plus sur les outils de gestion et les catégories d’API dans Microsoft Defender for Endpoint
keywords: onboarding, api, siem, rbac, access, portal, integration, investigation, response, entities, entity, user context, application context, streaming
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
ms.topic: conceptual
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 471db75102eabd4d7fce14ec42d0a47562007aae
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229982"
---
# <a name="overview-of-management-and-apis"></a>Vue d’ensemble de la gestion et des API

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez faire l’expérience de Defender pour point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mgt-apis-abovefoldlink)


Defender pour le point de terminaison prend en charge un large éventail d’options pour s’assurer que les clients peuvent facilement adopter la plateforme.

Sachant que les environnements et structures des clients peuvent varier, Defender for Endpoint a été créé avec flexibilité et contrôle granulaire pour s’adapter aux besoins divers des clients.

## <a name="endpoint-onboarding-and-portal-access"></a>Intégration de point de terminaison et accès au portail

L’intégration d’appareils est entièrement intégrée à Microsoft Endpoint Manager et Microsoft Intune pour les appareils clients et Azure Defender pour les appareils serveurs, offrant ainsi une expérience complète de configuration, de déploiement et de surveillance. En outre, Microsoft Defender pour point de terminaison prend en charge la stratégie de groupe et d’autres outils tiers utilisés pour la gestion des appareils.

Defender pour le point de terminaison fournit un contrôle fin sur ce que les utilisateurs ayant accès au portail peuvent voir et faire grâce à la flexibilité du contrôle d’accès basé sur un rôle (RBAC). Le modèle RBAC prend en charge toutes les sortes de structure des équipes de sécurité :

- Organisations et équipes de sécurité distribuées globalement
- Équipes d’opérations de sécurité de modèle à plusieurs niveaux
- Divisions entièrement séparées avec des équipes d’opérations de sécurité globale centralisées

## <a name="available-apis"></a>API disponibles
La solution Microsoft Defender pour point de terminaison est conçue sur une plateforme prête à l’intégration.

Defender pour le point de terminaison expose la plupart de ses données et actions par le biais d’un ensemble d’API par programme. Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de Defender for Endpoint.

![Image de l’API et de l’intégration disponibles dans Microsoft Defender pour le point de terminaison](images/mdatp-apis.png)

Les API Defender pour point de terminaison peuvent être regroupées en trois :

- API Microsoft Defender pour point de terminaison
- API de diffusion en continu de données brutes
- Intégration SIEM

## <a name="microsoft-defender-for-endpoint-apis"></a>API Microsoft Defender pour point de terminaison

Defender for Endpoint offre un modèle d’API en couches exposant des données et des fonctionnalités dans un modèle structuré, clair et facile à utiliser, exposé via un modèle d’authentification et d’autorisation Azure AD standard permettant l’accès dans le contexte des utilisateurs ou des applications SaaS. Le modèle API a été conçu pour exposer des entités et des fonctionnalités sous une forme cohérente.

Regardez cette vidéo pour obtenir une vue d’ensemble rapide des API de Defender for Endpoint.
>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4d73M]

**L’API** Investigation expose la richesse de Defender pour point de terminaison : elle expose des entités calculées ou « profilées » (par exemple, des appareils, des utilisateurs et des fichiers) et des événements discrets (par exemple, création de processus et création de fichiers) qui décrivent généralement un comportement lié à une entité, ce qui permet d’accéder aux données via des interfaces d’investigation permettant un accès basé sur une requête aux données. Pour plus d’informations, voir [API pris en charge.](exposed-apis-list.md)

**L’API Response** expose la possibilité d’agir dans le service et sur les appareils, ce qui permet aux clients d’inger des indicateurs, de gérer les paramètres, l’état des alertes, ainsi que d’prendre des actions de réponse sur les appareils par programme, telles que l’isolement des appareils du réseau, les fichiers de mise en quarantaine, etc.

## <a name="raw-data-streaming-api"></a>API de diffusion en continu de données brutes

Defender for Endpoint raw data streaming API provides the ability for customers to ship real-time events and alerts from their instances as they occur within a single data stream, providing a low latency, high débit delivery mechanism.

Les informations d’événement Defender for Endpoint sont directement poussées vers le stockage Azure pour la rétention des données à long terme, ou vers les Hubs d’événements Azure pour une consommation par des services de visualisation ou des moteurs de traitement de données supplémentaires.

Pour plus d’informations, voir [l’API de diffusion en continu des données brutes.](raw-data-export.md)

La nouvelle API de diffusion Microsoft 365 Defender inclut des événements de messagerie et d’alerte en plus des événements d’appareil.
Pour plus d’informations, [voir Microsoft 365 Defender API de diffusion en continu.](../defender/streaming-api.md)

## <a name="siem-api"></a>SIEM API

Lorsque vous activez l’intégration SIEM (Security Information and Event Management), cela vous permet d’obtenir des détections à partir de Centre de sécurité Microsoft Defender à l’aide de votre solution SIEM ou en vous connectant directement à l’API REST de détections. Cela active la section des détails d’accès au connecteur SIEM avec des valeurs pré-remplies et une application est créée sous votre client Azure Active Directory (Azure AD). Pour plus d’informations, voir [intégration SIEM.](enable-siem-integration.md)

## <a name="related-topics"></a>Voir aussi

- [Accéder aux API Microsoft Defender pour point de terminaison](apis-intro.md)
- [API prise en charge](exposed-apis-list.md)
- [Opportunités de partenariat technique](partner-integration.md)