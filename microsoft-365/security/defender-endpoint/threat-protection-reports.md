---
title: Rapport sur la protection contre les menaces dans Microsoft Defender pour le point de terminaison
description: Suivre les détections, catégories et gravité des alertes à l’aide du rapport de protection contre les menaces
keywords: détection d’alerte, source, alerte par catégorie, gravité de l’alerte, classification des alertes, détermination
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
ms.openlocfilehash: d32ab04f4acda60f65316719a4607c6c9bbd6447
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51688980"
---
# <a name="threat-protection-report-in-microsoft-defender-for-endpoint"></a>Rapport sur la protection contre les menaces dans Microsoft Defender pour le point de terminaison

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)


> Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

Le rapport sur la protection contre les menaces fournit des informations de haut niveau sur les alertes générées dans votre organisation. Le rapport inclut des informations de tendance montrant les sources de détection, les catégories, les gravités, les états, les classifications et les déterminations des alertes dans le temps.

Le tableau de bord est structuré en deux sections :

![Image du rapport sur la protection contre les menaces](images/threat-protection-reports.png)

Section | Description 
:---|:---
1 | Tendances des alertes
2 | Résumé des alertes

## <a name="alert-trends"></a>Tendances des alertes
Par défaut, les tendances des alertes affichent les informations d’alerte de la période de 30 jours se terminant par la dernière journée entière. Pour mieux prendre en compte les tendances qui se produisent dans votre organisation, vous pouvez affiner la période de rapport en ajustant la période indiquée. Pour ajuster la période, sélectionnez une plage de temps dans les options de la baisse :

- 30 jours
- 3 mois
- 6 mois
- Personnalisé

>[!NOTE]
>Ces filtres sont appliqués uniquement à la section tendances des alertes. Elle n’affecte pas la section récapitulatif des alertes.


## <a name="alert-summary"></a>Résumé des alertes
Alors que les tendances des alertes indiquent les tendances des alertes, le résumé de l’alerte affiche les informations d’alerte limitées au jour actuel.

 Le résumé des alertes vous permet d’aller jusqu’à une file d’attente d’alertes particulière avec le filtre correspondant qui lui est appliqué. Par exemple, si vous cliquez sur la barre PEPT dans la carte sources de détection, la file d’attente des alertes affiche uniquement les alertes générées à partir PEPT détections. 

>[!NOTE]
>Les données reflétées dans la section récapitulatif sont limitées à 180 jours avant la date actuelle. Par exemple, si la date du jour est le 5 novembre 2019, les données de la section récapitulatif reflétera les chiffres du 5 mai 2019 au 5 novembre 2019.<br>
> Le filtre appliqué à la section tendances n’est pas appliqué à la section récapitulatif. 

## <a name="alert-attributes"></a>Attributs d’alerte
Le rapport est composé de cartes qui affichent les attributs d’alerte suivants :

- **Sources de détection**: affiche des informations sur les capteurs et les technologies de détection qui fournissent les données utilisées par Microsoft Defender pour le point de terminaison pour déclencher des alertes.

- **Catégories de menaces**: affiche les types de menace ou d’activité d’attaque qui ont déclenché des alertes, indiquant les zones de focus possibles pour vos opérations de sécurité.

- **Gravité :** indique le niveau de gravité des alertes, indiquant l’impact potentiel des menaces collectives sur votre organisation et le niveau de réponse nécessaire pour les résoudre.

- **État**: affiche l’état de résolution des alertes, indiquant l’efficacité de vos réponses d’alerte manuelles et de la correction automatisée (si activée). 

- **Classification &** détermination : indique comment vous avez classé les alertes lors de leur résolution, si vous les avez classées comme menaces réelles (alertes vraies) ou comme détections incorrectes (fausses alertes). Ces cartes indiquent également la détermination des alertes résolues, fournissant des informations supplémentaires telles que les types de menaces réelles détectées ou les activités légitimes détectées de manière incorrecte.


 

## <a name="filter-data"></a>Filtrer les données

Utilisez les filtres fournis pour inclure ou exclure des alertes avec certains attributs.

>[!NOTE]
>Ces filtres **s’appliquent à toutes** les cartes du rapport.

Par exemple, pour afficher les données relatives aux alertes de gravité élevée uniquement :

1. Sous **Filtres > gravité**, sélectionnez **Élevé**
2. Assurez-vous que toutes les autres options sous **Gravité** sont désélectionnés.
3. Sélectionnez **Appliquer**. 

## <a name="related-topic"></a>Rubrique connexe
- [Rapport sur l’état et la conformité de l’appareil](machine-reports.md)
