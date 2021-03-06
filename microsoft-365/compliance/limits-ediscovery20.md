---
title: Limites d’Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez les limites de cas, d’indexation et de recherche en vigueur pour la solution Advanced eDiscovery dans Microsoft 365.
ms.openlocfilehash: 335e40c6918fc33acc12082546b98f28c319c814
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52244575"
---
# <a name="limits-in-advanced-ediscovery"></a>Limites définies dans Advanced eDiscovery

Cet article décrit les limites de la solution Advanced eDiscovery dans Microsoft 365.

## <a name="case-and-review-set-limits"></a>Limites des ensembles de cas et de révision

Le tableau suivant répertorie les limites pour les cas et les ensembles de révision Advanced eDiscovery.

| Description de la limite | Limite |
|:-----|:-----|
|Nombre total de documents qui peuvent être ajoutés à un cas (pour tous les ensembles de révision dans un cas).  <br/> |3 millions <br/> |
|Taille totale du fichier par jeu de chargement. Cela inclut le chargement de non-Office 365 dans un jeu à réviser.  <br/> |300 Go <br/> |
|Quantité totale de données chargées dans tous les ensembles de révision de l’organisation par jour.<br/> |2 To <br/> |
|Nombre maximal d’ensembles de charge par cas.  <br/> |200 <br/> |
|Nombre maximal d’ensembles de révision par cas.  <br/> |20 <br/> |
|Nombre maximal de groupes de balises par cas.  <br/> |1000 <br/> |
|Nombre maximal de balises par cas.  <br/> |1000 <br/> |
|Nombre maximal de travaux simultanés dans votre organisation pour ajouter du contenu à un groupe de révision. Ces travaux sont **nommés Ajout de données** à un jeu à réviser et sont affichés sous l’onglet **Travaux** dans un cas.| 10 <sup>4</sup> |
|Nombre maximal de travaux simultanés pour ajouter du contenu à un jeu à réviser par utilisateur. Ces travaux sont **nommés Ajout de données** à un jeu à réviser et sont affichés sous l’onglet **Travaux** dans un cas. | 3 |
|||

## <a name="hold-limits"></a>Limites de la durée de vie

Le tableau suivant répertorie les limites pour les Advanced eDiscovery cas.

| Description de la limite | Limite |
|:-----|:-----|
|Nombre maximal de boîtes aux lettres dans une seule et même boîte aux lettres. Cette limite inclut le total combiné de boîtes aux lettres utilisateur et les boîtes aux lettres associées aux groupes Microsoft 365, Microsoft Teams et Yammer groupes. <br/> |1 000  <br/> |
|Nombre maximal de sites dans une seule et même période d’attente. Cette limite inclut le total combiné des sites OneDrive Entreprise, des sites SharePoint et des sites associés aux groupes Microsoft 365, Microsoft Teams et Yammer groupes.  <br/> |100  <br/> |

## <a name="indexing-limits"></a>Limites d’indexation

Le tableau suivant répertorie les limites d’indexation dans Advanced eDiscovery.

| Description de la limite | Limite |
|:-----|:-----|
|Nombre maximal de caractères extraits d’un seul fichier.  <br/> |10 millions<sup>1</sup> <br/> |
|Taille maximale d’un fichier unique.   <br/> |100 Mo<sup>1</sup> <br/> |
|Profondeur maximale d’éléments incorporés dans un document.  <br/> |25<sup>1</sup> <br/> |
|Taille maximale des fichiers traitées par la reconnaissance optique de caractères (OCR).  <br/> |24 Mo<sup>1</sup> <br/> 
|Nombre maximal de travaux d’indexation par organisation et par jour. <br/> |10<sup>6</sup> <br/>|  
|||

## <a name="search-limits"></a>Limites de la recherche

Les limites décrites dans cette section sont liées à l’utilisation de l’outil de recherche sous l’onglet **Recherches** pour collecter des données pour un cas. Pour plus d’informations, [voir Collecter des données pour un cas dans Advanced eDiscovery](collecting-data-for-ediscovery.md).

| Description de la limite | Limite |
|:-----|:-----|
|Nombre maximal de boîtes aux lettres ou de sites qui peuvent être recherchés en une seule recherche. |Sans limite|
|Nombre maximal de recherches qui peuvent s’exécuter en même temps. |Sans limite |
|Nombre maximal de recherches qu’un seul utilisateur peut démarrer en même temps. |10 | 
|Nombre maximal de caractères pour une requête de recherche (y compris les opérateurs et les conditions). |10 000 &nbsp; <sup>2</sup>|
|Nombre maximal de caractères pour une requête de recherche pour SharePoint et OneDrive Entreprise sites (y compris les opérateurs et les conditions). |10 000<br>4 000 avec caractères génériques &nbsp; <sup>2</sup>|
|Nombre minimal de caractères alpha pour les caractères génériques de préfixe ; par exemple, **un \* *_ ou _* set \***.|3 |  
|Variantes maximales renvoyées lorsque vous utilisez un caractère générique de préfixe pour rechercher une expression exacte ou lorsque vous utilisez un caractère générique de préfixe et **l’opérateur booléen NEAR.** |10 000 &nbsp; <sup>3</sup>|
|Nombre maximal d’éléments par boîte aux lettres d’utilisateur qui sont affichés sur la page d’aperçu pour les recherches. Les éléments les plus récents sont affichés. |100|
|Nombre maximal d’éléments de toutes les boîtes aux lettres affichés sur la page d’aperçu pour les recherches.|1 000|
|Nombre maximal de boîtes aux lettres qui peuvent être prévisualiser pour les résultats de la recherche.  Si plus de 1 000 boîtes aux lettres contiennent des éléments qui correspondent à la requête de recherche, seules les 1 000 boîtes aux lettres ayant le plus grand nombre de résultats sont disponibles en prévisualisation.|1 000|
|Nombre maximal d’éléments provenant SharePoint sites OneDrive Entreprise affichés sur la page d’aperçu pour les recherches. Les éléments les plus récents sont affichés. |200|
|Nombre maximal de sites SharePoint et OneDrive Entreprise qui peuvent être prévisualiser pour les résultats de recherche. Si plus de 200 sites contiennent des éléments qui correspondent à la requête de recherche, seuls les 200 premiers sites avec le plus de résultats sont disponibles en prévisualisation.|200|
|Nombre maximal d’éléments par boîte aux lettres de dossiers publics affichés sur la page d’aperçu pour les recherches. |100|
|Nombre maximal d’éléments trouvés dans tous les éléments de boîte aux lettres de dossiers publics affichés sur la page d’aperçu pour les recherches. |200|
|Nombre maximal de boîtes aux lettres de dossiers publics qui peuvent être prévisualiser pour les résultats de recherche. Si plus de 500 boîtes aux lettres de dossiers publics contiennent des éléments qui correspondent à la requête de recherche, seules les 500 premières boîtes aux lettres ayant le plus de résultats sont disponibles en prévisualisation.|500|
|||

## <a name="search-times"></a>Temps de recherche

Microsoft collecte des informations de performances pour les recherches exécutés par toutes les organisations. Bien que la complexité de la requête de recherche puisse avoir un impact sur les heures de recherche, le facteur le plus important qui détermine la durée de la recherche est le nombre de boîtes aux lettres recherchées. Bien que Microsoft ne fournisse pas de contrat de niveau de service pour les durées de recherche, le tableau suivant répertorie les temps de recherche moyens pour les recherches de collecte en fonction du nombre de boîtes aux lettres incluses dans la recherche.
  
  | Nombre de boîtes aux lettres | Temps moyen de recherche |
  |:-----|:-----|
  |100  <br/> |30 secondes  <br/> |
  |1 000  <br/> |45 secondes  <br/> |
  |10 000  <br/> |4 minutes  <br/> |
  |25 000  <br/> |10 minutes  <br/> |
  |50 000  <br/> |20 minutes  <br/> |
  |100 000  <br/> |25 minutes  <br/> |
  |||

## <a name="viewer-limits"></a>Limites de la visionneuse

| Description de la limite | Limite |
|:-----|:-----|
|Taille maximale du Excel qui peut être visualisateur dans la visionneuse native.  <br/> |4 Mo  <br/> |
|||

## <a name="export-limits---final-export-out-of-review-set"></a>Limites d’exportation : exportation finale hors de l’ensemble de révision

Les limites décrites dans cette section sont liées à l’exportation de documents hors d’un jeu à réviser.

| Description de la limite | Limite |
|:-----|:-----|
|Taille maximale d’une exportation unique.|5 millions de documents ou 500 Go, selon la taille la plus petite|
|Nombre maximal d’exportations simultanées par groupe de révision. | 1 |
|||

## <a name="review-set-download-limits"></a>Examiner les limites de téléchargement définies

| Description de la limite | Limite |
|:-----|:-----|
|Taille totale du fichier ou nombre maximal de documents téléchargés à partir d’un jeu à réviser.  <br/> |3 Mo ou 50 documents <sup>5</sup>|
|||

<br/>
<br/>

> [!NOTE]
> <sup>1</sup> Tout élément qui dépasse une limite de fichier unique s’affiche comme une erreur de traitement.
>
> <sup>2 Lors</sup> de la recherche SharePoint et OneDrive Entreprise’emplacements, les caractères dans les URL des sites recherchés comptent par rapport à cette limite. Le nombre total de caractères est constitué des caractères :<br>
> - Tous les caractères des champs Utilisateurs et Filtres.
> - Tous les filtres d’autorisation de recherche qui s’appliquent à l’utilisateur.
> - Caractères de toutes les propriétés d’emplacement dans la recherche ; cela inclut ExchangeLocation,PublicFolderLocation,SharPointLocation,ExchangeLocationExclusion,PublicFolderLocationExclusion,SharePointLocationExclusion, OneDriveLocationExclusion.
>   Par exemple, inclure tous les sites SharePoint et les comptes OneDrive dans la recherche comptera six caractères, car le mot « ALL » apparaîtra pour les champs SharePointLocation et OneDriveLocation.
>
> <sup>3 Pour</sup> les requêtes sans expression (valeur de mot clé qui n’utilise pas de guillemets doubles), nous utilisons un index de préfixe spécial. Cela nous indique qu’un mot se trouve dans un document, mais pas là où il se trouve dans le document. Pour faire une requête d’expression (valeur de mot clé avec des guillemets doubles), nous devons comparer la position des mots dans l’expression dans le document. Cela signifie que nous ne pouvons pas utiliser l’index de préfixe pour les requêtes d’expressions. Dans ce cas, nous étendons la requête en interne avec tous les mots possibles que le préfixe développe ; par exemple, **time _ peut se développer vers \* *_*« time OR timer OR times OR timex OR timeboxed OR ... »**. La limite de 10 000 correspond au nombre maximal de variantes que le mot peut développer, et non au nombre de documents correspondant à la requête. Il n’existe aucune limite supérieure pour les termes autres que des expressions.
>
> <sup>4</sup> Cette limite est partagée avec l’exportation de contenu dans d’autres outils eDiscovery. Cela signifie que les exportations simultanées dans la recherche de contenu et la découverte électronique principale (et l’ajout de contenu à des jeux de révision dans Advanced eDiscovery) sont toutes appliquées par rapport à cette limite.
>
> <sup>5</sup> Cette limite s’applique au téléchargement de documents sélectionnés à partir d’un jeu à réviser. Elle ne s’applique pas à l’exportation de documents à partir d’un jeu à réviser. Pour plus d’informations sur le téléchargement et l’exportation de documents, voir exporter des données de cas [dans Advanced eDiscovery](exporting-data-ediscover20.md).
>
> <sup>6</sup> limites d’indexation par organisation et par jour. Pour contourner ce cas, vous pouvez sélectionner plusieurs dépositaires sous l’onglet **Sources** de données dans un cas, puis cliquer sur Mettre à jour **l’index** pour éviter de créer une tâche d’index distincte pour chaque dépositaire. 
