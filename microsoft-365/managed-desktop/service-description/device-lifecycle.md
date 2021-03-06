---
title: Bureau géré Microsoft vie du produit
description: Cet article répertorie les spécifications d’appareil utilisées dans Bureau géré Microsoft.
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.openlocfilehash: a8b8abc58b82d08d004d204396cfd8e381c6303a
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245311"
---
# <a name="microsoft-managed-desktop-product-lifecycle"></a>Bureau géré Microsoft vie du produit

Bureau géré Microsoft permet aux utilisateurs de s’assurer qu’ils utilisent toujours les appareils qui offrent les meilleures performances, fiabilité, conception et sécurité (telles que la prise en charge de fonctionnalités telles que Windows Hello). Pour ce faire, Bureau géré Microsoft un petit catalogue d’appareils approuvés mis à jour en continu. Vous pouvez afficher les appareils approuvés en filtrant les Bureau géré Microsoft sur le site [Windows 10 Professionnel d’entreprise.](https://www.microsoft.com/windowsforbusiness/view-all-devices)
 
Cet article détaille le cycle de vie des appareils à mesure qu’ils sont ajoutés et supprimés du catalogue approuvé. 

> [!NOTE]
> Dans cette rubrique, nous allons faire une distinction entre un « appareil » et un « produit ». Par « appareil », nous voulons dire un ordinateur spécifique. Par exemple, « Numéro de série 1234 », « Ordinateur portable de Bill », « VM XYZ partagé » font référence à des appareils spécifiques. Toutefois, un « produit » fait référence à une collection ou à une famille d’appareils. Par exemple, « Fabrikam Laptop », « Adatum ZX450 Laptop », etc. Ceci est important car les produits sont ajoutés à notre liste ou catalogue approuvé, et les appareils sont inscrits dans Bureau géré Microsoft.

## <a name="product-lifecycle"></a>Cycle de vie du produit

 En règle générale, les produits traversent ces phases de cycle de vie :

- [Version et évaluation du produit](#product-release-and-evaluation)
- [Période de disponibilité principale du produit](#product-primary-availability-period)
- [Période de grâce du produit](#product-grace-period)
- [Retrait du produit](#product-retirement)


Cette illustration montre la séquence entière :

![Chronologie du cycle de vie : à partir de la disponibilité générale du produit, la « disponibilité principale » dure deux ans. Pendant ce temps, la fenêtre de certification se termine et à un moment donné l’appareil est intégré. À la fin de la disponibilité principale, le produit est archivé et la « période de grâce » de trois ans commence. À compter de l’intégration de l’appareil, il dispose d’une période d’utilisation de 3 ans jusqu’à ce qu’il soit supprimé de la gestion. À la fin de la période de grâce, nous ôtons le produit du catalogue.](../../media/non-dark1-edits.PNG)

Les produits restent dans le catalogue pendant <em></em> 24 mois au plus, mais les appareils restent sous gestion pendant trois ans en fonction de leurs dates d’inscription individuelles. En fait, chaque produit a trois dates importantes, mais chaque appareil n’en possède qu’une seule. Pour les produits, ces trois dates sont calculées en fonction de la <em>date</em>d’approbation et, par conséquent, nous publions ces dates lors de l’approbation afin que vous pouvez toujours regarder à l’avance et planifier correctement l’intégralité du cycle de vie du produit.

Ce tableau montre des exemples de dates pour un produit théorique :


|Produit  |Date d’approbation  |Fin de la disponibilité principale  |Fin d’éligibilité  |
|---------|---------|---------|---------|
|Fabrikam Laptop    | 1/1/2017 | 6/1/2019 | 6/1/2022 |
|Ordinateur portable Adatum   | 1/1/2018 | 6/1/2020 | 6/1/2023  |

Ce tableau montre des exemples de dates pour les appareils *théoriques*:


|ID d’appareil  |Date d’inscription  |Date de retrait  |
|---------|---------|---------|
|Ordinateur portable #123412     |  2/3/2018       |  2/3/2021       |
|Bureau #321513     | 6/2/2018        |  6/2/2021       |


## <a name="product-release-and-evaluation"></a>Version et évaluation du produit

Le cycle de vie du produit démarre lorsqu’un fabricant publie publiquement le produit :

![Chronologie du cycle de vie affichant la publication et la période d’évaluation](../../media/non-dark3-edits.PNG)

Au cours de cette étape, l’équipe Bureau géré Microsoft’ingénierie locale fait son évaluation et sa certification d’un produit. L’équipe évalue des éléments tels que la fiabilité et les performances avec Windows, la conformité avec une base de référence matérielle, l’opinion du marché et la préparation des stocks et des canaux, entre autres choses. Ce processus prend généralement environ six semaines.
  
Bureau géré Microsoft évaluera uniquement les appareils pour certification au cours de leurs six premiers mois de disponibilité. Cette stratégie garantit que nous concentrons toujours nos efforts sur la dernière génération de matériel.
 
À la fin de cette phase, Bureau géré Microsoft ajoute le produit à la liste [approuvée,](device-list.md)en publiant effectivement le produit pour les inscriptions des clients. Quelle que soit la date à laquelle un appareil est certifié, sa **date** d’approbation est revenir à la date de disponibilité générale du produit. 


## <a name="product-primary-availability-period"></a>Période de disponibilité principale du produit

Cette période est au cœur de la disponibilité du produit :

![Chronologie du cycle de vie affichant la disponibilité principale](../../media/non-dark4-edits.PNG)

Tout appareil inscrit au cours de cette période reçoit les trois années complètes de prise en charge de Bureau géré Microsoft (comme illustré par la chronologie bleue). Cette période dure jusqu’à une date de fin définie sur 24 mois à partir de la date de disponibilité générale.

Vous pouvez penser que cette période est effectivement « ouvrir l’inscription », donc pour optimiser la valeur de Bureau géré Microsoft, vous devez cibler vos modèles d’approvisionnement et les produits sélectionnés pour se trouver au cours de cette période. À titre d’exemple, vous devez éviter de mettre en place une période de déploiement de deux ans à l’aide d’un produit qui [](#product-grace-period) se trouve dans son dernier mois de disponibilité primaire . La plupart de ces appareils ne bénéficieront pas des trois ans complets de gestion de Bureau géré Microsoft (voir la période de grâce pour plus d’informations).  

## <a name="product-grace-period"></a>Période de grâce du produit

La période de grâce du produit est une période de trois ans suivant la disponibilité principale. Cette phase vous permet d’inscrire des appareils qui sont issus d’une famille de produits prise en charge, tout en maintenant les promesses de Bureau géré Microsoft concernant les performances du matériel et des appareils modernes. Cette phase est idéale pour les clients qui ont pris des décisions d’approvisionnement avant de connaître Bureau géré Microsoft. 

Si vous avez récemment acheté des appareils approuvés avant de vous inscrire auprès de Bureau géré Microsoft, vous pouvez toujours les inscrire, mais vous ne recevrez pas trois ans de gestion complets. Au lieu de cela, ils ne seront pas conformes à la date de retrait, quel que soit le moment où ils ont été inscrits. En arrière-plan, Bureau géré Microsoft traitent ces appareils comme s’ils étaient inscrits le dernier jour de disponibilité principale. Dans cette illustration, vous pouvez voir ce scénario en notant que les appareils bleu et vert se terminent tous les deux le même jour, malgré leur différence d’inscription d’un an :


![Chronologie du cycle de vie affichant la période de grâce](../../media/non-dark2-edits.PNG)

L’exemple Fabrikam Laptop du tableau précédent illustre cette situation : 

|Produit  |Date d’approbation  |Fin de la disponibilité principale  |Fin d’éligibilité  |
|---------|---------|---------|---------|
|Fabrikam Laptop    | 6/1/2017 | 6/1/2019 | 6/1/2022 |

En tant que client, vous pouvez inscrire des ordinateurs portables Fabrikam jusqu’au 01/06/2022, mais ils seront tous traités comme si vous les a inscrits le 01/06/2019. Si vous inscrivez un ordinateur portable Fabrikam le 01/06/2021, vous n’aurez qu’un an de gestion. Cette stratégie vous permet d’extraire des cycles de vie partiels à partir de produits précédemment pris en charge, plutôt que d’avoir à acheter de nouveaux appareils prématurément. 

Enfin, au cours de cette phase, l’appareil est supprimé de la liste des appareils et déplacé vers la [liste des appareils archivés.](archived-device-list.md) [](device-list.md)


## <a name="product-retirement"></a>Retrait du produit

Le retrait du produit est la dernière phase du cycle de vie. Dans cette phase, aucun nouvel appareil de ce type de produit ne peut être inscrit dans Bureau géré Microsoft et, par définition, tous les appareils existants sont désormais en dehors de leur période de trois ans autorisée. Pendant ce temps, Bureau géré Microsoft supprimera entièrement l’appareil de la liste publique. C’est également au cours de cette phase que, si vous n’avez pas encore obtenu de remplacements, vous commencez à voir les services diminués à mesure que Bureau géré Microsoft commence à descendre en puissance sur les appareils qui ne sont pas conformes. 

## <a name="devices-that-are-out-of-compliance"></a>Appareils non conformes

Un appareil n’est pas conforme lorsque sa fenêtre d’Bureau géré Microsoft gestion est écoulée. Cette situation se produit lorsque l’appareil a atteint trois ans de gestion ou lorsque ce type de produit est supprimé du catalogue d’appareils, selon ce qui se produit en premier. Vous devez toujours cibler vos cycles d’approvisionnement afin que les nouveaux appareils soient déployés avant que les appareils actuels ne soient hors conformité.

L’Bureau géré Microsoft sait que les cycles d’approvisionnement sont longs et planifiés autour de budgets à long terme. Pour vous assurer que vous êtes toujours conscient de l’état de la population de votre appareil, nous fournissons un site web qui répertorie chaque appareil sous gestion, son âge et un état indiquant sa conformité. [](https://aka.ms/mmdportal) Le site web vous aide à toujours avoir les dernières informations concernant l’âge de l’appareil et peut utiliser le rapport dans n’importe quel cycle de planification de l’approvisionnement. 







