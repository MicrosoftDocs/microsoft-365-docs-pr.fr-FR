---
title: En savoir plus sur les classifieurs avec capacité d’apprentissage
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: Un Microsoft 365 classifieur entraisable est un outil que vous pouvez former pour reconnaître différents types de contenu en lui donnant des exemples positifs et négatifs à examiner. Une fois que le classifieur est formé, vous confirmez que ses résultats sont exacts. Ensuite, vous l’utilisez pour rechercher le contenu de votre organisation et le classer pour appliquer des étiquettes de rétention ou de confidentialité ou l’inclure dans des stratégies de protection contre la perte de données (DLP) ou de rétention.
ms.openlocfilehash: 1881e4de87fd41f21bb1f2236d46391b3a1ed785
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114050"
---
# <a name="learn-about-trainable-classifiers"></a>En savoir plus sur les classifieurs avec capacité d’apprentissage

La classification et l’étiquetage du contenu afin qu’il puisse être protégé et géré correctement constitue le point de départ de la protection des informations. Microsoft 365 trois façons de classer le contenu.

## <a name="manually"></a>Manuellement

Cette méthode nécessite un juge humain et une action. Un administrateur peut utiliser les étiquettes et les types d’informations sensibles pré-existants ou créer les leurs, puis les publier. Les utilisateurs et les administrateurs les appliquent au contenu à mesure qu’ils le rencontrent. Vous pouvez ensuite protéger le contenu et gérer sa disposition.

## <a name="automated-pattern-matching"></a>Correspondance de modèle automatisée

Cette catégorie de mécanismes de classification inclut la recherche de contenu par :

- Mots clés ou valeurs de métadonnées (langage de requête de mot clé).
- À l’aide de modèles précédemment identifiés d’informations sensibles telles que la sécurité sociale, la carte bancaire ou les numéros de compte bancaire (définitions d’entité [de type d’informations sensibles)](sensitive-information-type-entity-definitions.md).
- Reconnaissance d’un élément, car il s’agit d’une variante d’un modèle [(impression avec le doigt du document).](document-fingerprinting.md)
- Utilisation de la présence de chaînes exactes [(correspondance exacte des données)](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md).

Les étiquettes de sensibilité et de rétention peuvent ensuite être appliquées automatiquement pour rendre le contenu disponible pour utilisation dans En savoir plus sur la protection contre la perte de données [)](dlp-learn-about-dlp.md)et appliquer automatiquement des stratégies pour les [étiquettes de rétention.](apply-retention-labels-automatically.md)

## <a name="classifiers"></a>Classifieurs

Cette méthode de classification est particulièrement adaptée au contenu qui n’est pas facilement identifié par les méthodes manuelles ou automatisées de correspondance de modèle. Cette méthode de classification consiste davantage à former un classifieur à identifier un élément en fonction de ce qu’il est, et non par les éléments qui se trouvent dans l’élément (critères spéciaux). Un classifieur apprend à identifier un type de contenu en regardant des centaines d’exemples de contenu que vous souhaitez classer. Commencez par lui donner des exemples qui sont certainement dans la catégorie. Une fois qu’il les traite, vous le testez en lui donnant un mélange d’exemples correspondants et non correspondants. Le classifieur effectue ensuite des prédictions quant à l’entrée d’un élément donné dans la catégorie que vous construisez. Vous confirmez ensuite ses résultats, en triant les vrais positifs, les vrais négatifs, les faux positifs et les faux négatifs pour améliorer la précision de ses prédictions. 

Lorsque vous publiez le classifieur, il trie les éléments dans des emplacements tels que SharePoint Online, Exchange et OneDrive, et classifie le contenu. Après avoir publié le classificateur, vous pouvez continuer à l’entraîner à l’aide d’un processus de commentaires semblable au processus de formation initial.

### <a name="where-you-can-use-trainable-classifiers"></a>Où utiliser des classifieurs entraisables
Les [classifieurs](apply-sensitivity-label-automatically.md)intégrés et les classifieurs entraçables sont disponibles en tant que condition pour l’étiquetage automatique d’Office avec des étiquettes de confidentialité, une stratégie d’étiquette de rétention à application automatique basée sur une [condition](apply-retention-labels-automatically.md#configuring-conditions-for-auto-apply-retention-labels) et dans la conformité des [communications.](communication-compliance.md) 

Les étiquettes de sensibilité peuvent utiliser des classifieurs comme conditions. Voir Appliquer automatiquement une étiquette de sensibilité [au contenu.](apply-sensitivity-label-automatically.md)

> [!IMPORTANT]
> Les classifieurs fonctionnent uniquement avec les éléments qui ne sont pas chiffrés et qui sont en anglais.

## <a name="types-of-classifiers"></a>Types de classifieurs

- **Classifieurs pré-formés** : Microsoft a créé et pré-formé un certain nombre de classifieurs que vous pouvez commencer à utiliser sans les former. Ces classifieurs apparaissent avec l’état `Ready to use` de .
- **classifieurs personnalisés** : si vous avez des besoins de classification qui s’étendent au-delà de ce que couvrent les classifieurs pré-formés, vous pouvez créer et former vos propres classifieurs.

### <a name="pre-trained-classifiers"></a>Classifieurs pré-formés

Microsoft 365 est livré avec cinq classifieurs pré-formés :

> [!CAUTION]
> Nous déprécions  le classificateur de langage choquant pré-entraîné, car il a produit un grand nombre de faux positifs. Ne l’utilisez pas et si vous l’utilisez actuellement, vous devez en déplacer vos processus d’entreprise. Nous vous recommandons plutôt **d’utiliser** les classifieurs pré-formés contre les menaces, les blasphémités et le harcèlement.  

- Cv : détecte les éléments qui sont des comptes textuels des **qualifications** personnelles, pédagogiques, professionnelles, professionnelles et autres informations d’identification personnelle d’un candidat
- **Code source**: détecte les éléments qui contiennent un ensemble d’instructions et d’instructions écrites dans les 25 langages de programmation informatique les plus utilisés sur GitHub
    - ActionScript
    - C
    - C#
    - C++
    - Îlesjure
    - CoffeeScript
    - Activer
    - Haskell
    - Java
    - JavaScript
    - Lua
    - MATLAB
    - Objective-C
    - Perl
    - PHP
    - Python
    - R
    - Ruby
    - Scala
    - Shell
    - Swift
    - Tex
    - Vim Script

> [!NOTE]
> Le code source est formé pour détecter quand l’essentiel du texte est du code source. Il ne détecte pas le texte de code source qui est entrecoupé de texte simple.

- **Harcèlement**: détecte une catégorie spécifique d’éléments de texte de langage choquant liés à une conduite choquante ciblant un ou plusieurs individus en fonction des caractéristiques suivantes : course, ancienneté, genre, origine nationale, sexe, orientation sexuelle, âge, handicap/invalidité
- **Blasphémité**: détecte une catégorie spécifique d’éléments de texte de langage choquant qui contiennent des expressions qui gênent la plupart des personnes
- **Menace**: détecte une catégorie spécifique d’éléments de texte de langage choquant liés aux menaces de violence ou d’atteinte physique à une personne ou à une propriété

Ceux-ci apparaissent dans **l Microsoft 365 de classification** des données du centre de conformité avec l’état de  >    >   `Ready to use` .

![classifieurs-pré-formés-classifieurs](../media/classifiers-ready-to-use-classifiers.png)

> [!IMPORTANT]
> Veuillez noter que le langage choquant, le harcèlement, la blasphémité et les classifieurs de menaces fonctionnent uniquement avec du texte utilisable dans une recherche et ne sont pas exhaustifs ou complets.  En outre, les normes linguistiques et culturelles changent continuellement et, à la lumière de ces exigences, Microsoft se réserve le droit de mettre à jour ces classifieurs à sa discrétion. Bien que les classifieurs peuvent aider votre organisation à surveiller les langages choquants et autres utilisés, ils ne répondent pas aux conséquences de ce langage et ne sont pas destinés à fournir l’unique moyen de surveillance ou de réponse de votre organisation à l’utilisation de ce langage. Votre organisation, et non Microsoft ou ses filiales, reste responsable de toutes les décisions relatives à la surveillance, à l’application, au blocage, à la suppression et à la rétention de tout contenu identifié par un classificateur pré-formé.

### <a name="custom-classifiers"></a>Classifieurs personnalisés

Lorsque les classifieurs pré-formés ne répondent pas à vos besoins, vous pouvez créer et former vos propres classifieurs. Il y a beaucoup plus de travail à faire avec la création de vos propres produits, mais ils seront bien mieux adaptés aux besoins de votre organisation. 

Par exemple, vous pouvez créer des classifieurs entraisables pour :
 
- Documents juridiques : par exemple, privilège client avocat, jeux de fermeture, déclaration de travail
- Documents d’entreprise stratégiques : communiqués de presse, fusion et acquisition, transactions, plans commerciaux ou commerciaux, propriété intellectuelle, brevets, documents de conception
- Informations tarifaires : par exemple, factures, devis, commandes de travail, documents d’auteur 
- Informations financières , telles que les investissements organisationnels, les résultats trimestrielles ou annuels    

#### <a name="process-flow-for-creating-custom-classifiers"></a>Flux de processus pour la création de classifieurs personnalisés

La création et la publication d’un classifieur à utiliser dans des solutions de conformité, telles que les stratégies de rétention et la surveillance des communications, suivent ce flux. Pour plus d’informations sur la création d’un classifieur entraisable personnalisé, voir [Création d’un classificateur personnalisé.](classifier-get-started-with.md)

![classificateur personnalisé de flux de processus](../media/classifier-trainable-classifier-flow.png)

### <a name="retraining-classifiers"></a>Retraining classifiers

Vous pouvez améliorer la précision de tous les classifieurs personnalisés et de certains classifieurs pré-formés en leur fournissant des commentaires sur la précision de la classification qu’ils effectuent. C’est ce qu’on appelle une nouvelle formation et suivre ce flux de travail.

![flux de travail de formation du classificateur](../media/classifier-retraining-workflow.png)

## <a name="see-also"></a>Voir aussi

- [Étiquettes de rétention](retention.md)
- [En savoir plus sur la prévention des pertes de données](dlp-learn-about-dlp.md)
- [Étiquettes de confidentialité](sensitivity-labels.md)
- [Définitions des entités de type information sensible](sensitive-information-type-entity-definitions.md)
- [Impression des doigts du document](document-fingerprinting.md)
- [Correspondance exacte des données](create-custom-sensitive-information-types-with-exact-data-match-based-classification.md)
