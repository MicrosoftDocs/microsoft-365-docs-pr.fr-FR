---
title: Phases de déploiement
description: Découvrez comment déployer Microsoft Defender pour endpoint en préparation, configuration et intégration de points de terminaison à ce service
keywords: déployer, préparer, configurer, intégrer, phase, déploiement, déploiement, adoption, configuration
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
ms.collection:
- M365-security-compliance
- m365solution-endpointprotect
- m365solution-overview
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 3f0527192a55d67df7e23507bed46df446f8b2b7
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165164"
---
# <a name="deployment-phases"></a>Phases de déploiement

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

>Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

Découvrez comment déployer Microsoft Defender pour endpoint afin que votre entreprise puisse tirer parti de la protection préventive, de la détection post-violation, de l’examen automatisé et de la réponse. 


Ce guide vous aide à travailler au sein des parties prenantes pour préparer votre environnement, puis intégrer les appareils d’une manière méthodique, en passant de l’évaluation à un projet pilote significatif vers un déploiement complet.

Chaque section correspond à un article distinct de cette solution.

![Image des phases de déploiement avec les détails du tableau](images/deployment-guide-phases.png)


![Résumé des phases de déploiement : préparer, configurer, intégrer](images/phase-diagrams/deployment-phases.png)

|Phase | Description | 
|:-------|:-----|
| [Phase 1 : préparation](prepare-deployment.md)| Découvrez ce que vous devez prendre en compte lors du déploiement de Defender for Endpoint, comme les approbations des parties prenantes, les considérations sur l’environnement, les autorisations d’accès et l’ordre d’adoption des fonctionnalités. 
| [Phase 2 : configuration](production-deployment.md)|  Obtenez des conseils sur les étapes initiales à suivre pour accéder au portail, telles que la validation des licences, l’exécution de l’Assistant Installation et la configuration réseau. 
| [Phase 3 : intégration](onboarding.md) | Découvrez comment utiliser les anneaux de déploiement, les outils d’intégration pris en charge en fonction du type de point de terminaison et la configuration des fonctionnalités disponibles. 


Une fois que vous aurez terminé ce guide, vous serez configuré avec les autorisations d’accès adéquates, vos points de terminaison seront intégrés et des données de capteur seront signalés au service, et des fonctionnalités telles que la protection nouvelle génération et la réduction de la surface d’attaque seront en place.



Quelle que soit l’architecture et la méthode [](deployment-strategy.md) de déploiement de l’environnement que vous choisissez décrites dans les instructions de déploiement de plan, ce guide va vous prendre en charge lors de l’intégration des points de terminaison. 








## <a name="key-capabilities"></a>Fonctionnalités clés

Bien que Microsoft Defender pour point de terminaison offre de nombreuses fonctionnalités, l’objectif principal de ce guide de déploiement est de vous aider à commencer par l’intégration d’appareils. En plus de l’intégration, ces conseils vous guident avec les fonctionnalités suivantes.



Fonctionnalité | Description 
:---|:---
Détection et réponse du point de terminaison | Des fonctionnalités de détection et de réponse de point de terminaison sont mises en place pour détecter, examiner et répondre aux tentatives d’intrusion et aux violations actives.
Protection de nouvelle génération | Pour renforcer davantage le périmètre de sécurité de votre réseau, Microsoft Defender pour Endpoint utilise une protection nouvelle génération conçue pour capturer tous les types de menaces émergentes.
Réduction de la surface d'attaque |  Fournissez la première ligne de défense dans la pile. En veillant à ce que les paramètres de configuration soient correctement définies et que des techniques d’atténuation des attaques soient appliquées, ces fonctionnalités peuvent résister aux attaques et à l’exploitation.

Toutes ces fonctionnalités sont disponibles pour les titulaires de licences Microsoft Defender pour les points de terminaison. Pour plus d’informations, voir [Conditions requises pour les licences.](minimum-requirements.md#licensing-requirements)

## <a name="scope"></a>Portée

### <a name="in-scope"></a>Dans l’étendue

-   Utilisation de Microsoft Endpoint Manager et Microsoft Endpoint Manager pour intégrer des points de terminaison dans le service et configurer des fonctionnalités

-   Activation de Defender pour les fonctionnalités de protection évolutive des points de terminaison point de terminaison (PEPT)

-   Activation des fonctionnalités DE LAS (Endpoint Endpoint Protection Platform) de Defender for Endpoint

    -   Protection de nouvelle génération

    -   Réduction de la surface d'attaque


### <a name="out-of-scope"></a>Non compris

Ce guide de déploiement n’entre pas dans le cadre de ce guide de déploiement :

-   Configuration de solutions tierces qui peuvent s’intégrer à Defender for Endpoint

-   Test de pénétration dans un environnement de production




## <a name="see-also"></a>Voir aussi
- [Phase 1 : préparation](prepare-deployment.md)
- [Phase 2 : configuration](production-deployment.md)
- [Phase 3 : intégration](onboarding.md)
- [Planifier le déploiement](deployment-strategy.md)