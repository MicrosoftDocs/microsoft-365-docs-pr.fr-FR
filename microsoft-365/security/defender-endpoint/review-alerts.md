---
title: Passer en revue les alertes dans Microsoft Defender pour le point de terminaison
description: Passer en revue les informations d’alerte, y compris un article d’alerte visualisé et des détails pour chaque étape de la chaîne.
keywords: incident, incidents, ordinateurs, appareils, utilisateurs, alertes, alerte, enquête, graphique, preuves
ms.prod: m365-security
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: daniha
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.date: 5/1/2020
ms.technology: mde
ms.openlocfilehash: b17af7931b181a5fa30271a3eee07c7abf10a010
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844021"
---
# <a name="review-alerts-in-microsoft-defender-for-endpoint"></a>Passer en revue les alertes dans Microsoft Defender pour le point de terminaison

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)

>Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-managealerts-abovefoldlink)

La page d’alerte dans Microsoft Defender pour le point de terminaison fournit un contexte complet à l’alerte, en combinant les signaux d’attaque et les alertes associées à l’alerte sélectionnée, pour créer un article d’alerte détaillé.

Triez rapidement, examinez et prenez des mesures efficaces sur les alertes qui affectent votre organisation. Comprendre pourquoi ils ont été déclenchés et leur impact à partir d’un seul emplacement. En savoir plus dans cette vue d’ensemble.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yiO5]

## <a name="getting-started-with-an-alert"></a>Mise en place d’une alerte

La sélection du nom d’une alerte dans Defender pour le point de terminaison vous placera sur sa page d’alerte. Sur la page d’alerte, toutes les informations s’afficheront dans le contexte de l’alerte sélectionnée. Chaque page d’alerte se compose de 4 sections :

1. **Le titre de l’alerte** affiche le nom de l’alerte et est là pour vous rappeler quelle alerte a démarré votre enquête en cours, indépendamment de ce que vous avez sélectionné sur la page.
2. [**Les ressources affectées**](#review-affected-assets) répertorient les cartes d’appareils et d’utilisateurs affectés par cette alerte qui peuvent être cliquées pour plus d’informations et d’actions.
3. **L’article d’alerte** affiche toutes les entités liées à l’alerte, interconnectées par une arborescence. L’alerte dans le titre est celle qui est sélectionnée lorsque vous vous pointez pour la première fois sur la page de votre alerte sélectionnée. Les entités dans l’article d’alerte sont ex expandables et cliquables, pour fournir des informations supplémentaires et accélérer la réponse en vous permettant d’agir directement dans le contexte de la page d’alerte. Utilisez l’article d’alerte pour lancer votre enquête. Découvrez comment examiner [les alertes dans Microsoft Defender pour le point de terminaison.](/microsoft-365/security/defender-endpoint/investigate-alerts)
4. Le **volet d’informations** affiche d’abord les détails de l’alerte sélectionnée, avec les détails et les actions associés à cette alerte. Si vous sélectionnez l’une des ressources ou entités affectées dans l’article d’alerte, le volet d’informations change pour fournir des informations contextuelles et des actions pour l’objet sélectionné.

Notez l’état de détection de votre alerte. 
- Interdit : la tentative d’action suspecte a été évitée. Par exemple, un fichier n’a pas été écrit sur le disque ou exécuté.
![Page d’alerte indiquant que la menace a été empêchée](images/detstat-prevented.png)
- Bloqué : un comportement suspect a été exécuté, puis bloqué. Par exemple, un processus a été exécuté, mais comme il a par la suite présenté des comportements suspects, le processus a été interrompu.
![Page d’alerte indiquant que la menace a été bloquée](images/detstat-blocked.png)
- Détecté : une attaque a été détectée et est éventuellement toujours active.
![Page d’alerte indiquant que la menace a été détectée](images/detstat-detected.png)




Vous pouvez ensuite consulter les *détails* de l’enquête automatisée dans le volet d’informations de votre alerte, pour voir quelles actions ont déjà été entreprises, ainsi que lire la description de l’alerte pour les actions recommandées.

![Extrait du volet d’informations avec la description de l’alerte et les sections d’examen automatique mises en évidence](images/alert-air-and-alert-description.png)

Les autres informations disponibles dans le volet d’informations lors de l’ouverture de l’alerte incluent les techniques MITRE, la source et des détails contextuels supplémentaires.




## <a name="review-affected-assets"></a>Passer en revue les biens affectés

La sélection d’un appareil ou d’une carte utilisateur dans les sections ressources affectées bascule vers les détails de l’appareil ou de l’utilisateur dans le volet d’informations.

- **Pour les appareils,** le volet d’informations affiche des informations sur l’appareil lui-même, comme domaine, système d’exploitation et IP. Les alertes actives et les utilisateurs connectés sur cet appareil sont également disponibles. Vous pouvez prendre des mesures immédiates en isolant l’appareil, en limitant l’exécution de l’application ou en exécutant une analyse antivirus. Vous pouvez également collecter un package d’enquête, lancer une enquête automatisée ou vous rendre sur la page de l’appareil pour l’examiner du point de vue de l’appareil.

   ![Extrait du volet d’informations lorsqu’un appareil est sélectionné](images/device-page-details.png)

- Pour les utilisateurs, le volet d’informations affiche des informations détaillées sur l’utilisateur, telles que le nom SAM et le SID de l’utilisateur, ainsi que les types d’accès effectués par cet utilisateur, ainsi que les alertes et incidents qui lui sont associés. Vous pouvez sélectionner *Ouvrir la page utilisateur* pour poursuivre l’examen du point de vue de cet utilisateur.

   ![Extrait du volet d’informations lorsqu’un utilisateur est sélectionné](images/user-page-details.png)


## <a name="related-topics"></a>Voir aussi

- [Afficher et organiser la file d’attente des incidents](view-incidents-queue.md)
- [Enquêter sur des incidents](investigate-incidents.md)
- [Gérer les incidents](manage-incidents.md)
