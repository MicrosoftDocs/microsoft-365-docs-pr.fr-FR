---
title: 'Rapport sur les appareils vulnérables : Gestion des menaces et des vulnérabilités'
description: Rapport présentant les tendances des appareils vulnérables et les statistiques actuelles. L’objectif est que vous compreniez le bruit et l’étendue de l’exposition de votre appareil.
keywords: Microsoft Defender pour les appareils vulnérables endpoint-tvm, Microsoft Defender pour le point de terminaison, tvm, réduire les menaces & exposition aux vulnérabilités, réduire les menaces et les vulnérabilités, surveiller la configuration de la sécurité
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 355561936642b1fa38228bfa07ad59269c48d817
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245479"
---
# <a name="vulnerable-devices-report---threat-and-vulnerability-management"></a>Rapport sur les appareils vulnérables : Gestion des menaces et des vulnérabilités

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**

- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)
- [Menaces et gestion des vulnérabilités](next-gen-threat-and-vuln-mgt.md)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

>Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

Le rapport présente des graphiques et des graphiques à barres avec des tendances d’appareils vulnérables et des statistiques actuelles. L’objectif est que vous compreniez le bruit et l’étendue de l’exposition de votre appareil.

Accédez au rapport dans le Centre de sécurité Microsoft Defender en accédant à **Rapports > appareils vulnérables**

Il existe deux colonnes :

- Tendances (au fil du temps). Peut afficher les 30 derniers jours, 3 mois, 6 mois ou une plage de dates personnalisée.
- Aujourd’hui (informations actuelles)

**Filtre :** vous pouvez filtrer les données par niveaux de gravité de vulnérabilité, disponibilité d’exploit, âge de vulnérabilité, plateforme du système d’exploitation, version Windows 10 ou groupe d’appareils.

**Exploration :** s’il existe un aperçu que vous souhaitez explorer plus en détail, sélectionnez le graphique à barres approprié pour afficher une liste filtrée d’appareils dans la page d’inventaire des appareils. À partir de là, vous pouvez exporter la liste.

## <a name="severity-level-graphs"></a>Graphiques de niveau de gravité

Chaque appareil est compté une seule fois en fonction de la vulnérabilité la plus grave trouvée sur cet appareil.

![Graphique des niveaux de gravité de vulnérabilité actuels de l’appareil et graphique montrant les niveaux au fil du temps.](images/tvm-report-severity.png)

## <a name="exploit-availability-graphs"></a>Exploiter les graphiques de disponibilité

Chaque appareil est compté une seule fois en fonction du niveau d’exploitation connu le plus élevé.

![Un graphique de la disponibilité actuelle de l’exploitation des appareils et un graphique montrant la disponibilité au fil du temps.](images/tvm-report-exploit-availability.png)

## <a name="vulnerability-age-graphs"></a>Graphiques de l’âge de vulnérabilité

Chaque appareil est compté une seule fois sous la date de publication de la vulnérabilité la plus ancienne. Les vulnérabilités plus anciennes ont plus de chances d’être exploitées.

![Graphique de l’âge actuel de vulnérabilité de l’appareil et graphique montrant l’âge au fil du temps.](images/tvm-report-age.png)

## <a name="vulnerable-devices-by-operating-system-platform-graphs"></a>Appareils vulnérables par graphiques de plateforme de système d’exploitation

Nombre d’appareils sur chaque système d’exploitation exposés en raison de vulnérabilités logicielles.

![Un graphique des appareils vulnérables actuels par plateforme de système d’exploitation et un graphique montrant les appareils vulnérables par les plateformes de système d’exploitation au fil du temps.](images/tvm-report-os.png)

## <a name="vulnerable-devices-by-windows-10-version-graphs"></a>Appareils vulnérables en Windows 10 graphiques de version

Nombre d’appareils sur chaque version Windows 10 qui sont exposés en raison d’applications ou de système d’exploitation vulnérables.

![Un graphique des appareils vulnérables actuels par version Windows 10 et un graphique montrant les appareils vulnérables par Windows 10 version au fil du temps.](images/tvm-report-version.png)

## <a name="related-topics"></a>Voir aussi

- [Vue d’ensemble gestion des vulnérabilités menaces et gestion des vulnérabilités menaces](next-gen-threat-and-vuln-mgt.md)
- [Recommandations de sécurité](tvm-security-recommendation.md)
