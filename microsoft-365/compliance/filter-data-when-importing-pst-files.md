---
title: Filtrer les données lors de l’importation de fichiers PST
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
ms.custom: seo-marvel-apr2020
description: Découvrez comment filtrer des données à l’aide de la fonctionnalité d’importation intelligente dans le service d’importation Microsoft 365 lorsque vous importez des fichiers PST dans Microsoft 365.
ms.openlocfilehash: fc89467e3ea9c0af86ec6b9ef6a9d7d61079e116
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730569"
---
# <a name="filter-data-when-importing-pst-files"></a>Filtrer les données lors de l’importation de fichiers PST

Utilisez la nouvelle fonctionnalité d’importation intelligente dans le service d’importation Microsoft 365 pour filtrer les éléments des fichiers PST réellement importés dans les boîtes aux lettres cibles. Voici le principe de fonctionnement :
  
- Une fois que vous avez créé et soumis une tâche d’importation PST, les fichiers PST sont téléchargés vers une zone de stockage Azure dans le cloud Microsoft.
  
- Microsoft 365 analyse les données des fichiers PST, de manière sécurisée et sécurisée, en identifiant l’âge des éléments de boîte aux lettres et les différents types de messages inclus dans les fichiers PST.
  
- Lorsque l’analyse est terminée et que les données sont prêtes à être importées, vous avez la possibilité d’importer toutes les données des fichiers PST tels quels ou de découper les données importées en fixant des filtres qui contrôlent les données importées. Par exemple, vous pouvez choisir de :
  
  - Importez uniquement les éléments d’un certain âge.
  
  - Importer les types de messages sélectionnés.
  
  - Exclure les messages envoyés ou reçus par des personnes spécifiques.
  
- Après avoir configuré les paramètres de filtre, Microsoft 365 importe uniquement les données qui répondent aux critères de filtrage dans les boîtes aux lettres cibles spécifiées dans la tâche d’importation.
  
Le graphique suivant illustre le processus d’importation intelligente et met en évidence les tâches que vous effectuez et les tâches effectuées par Office 365.
  
![Processus d’importation intelligent dans Office 365](../media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="create-a-pst-import-job"></a>Créer une tâche d’importation PST

- Les étapes de cette rubrique supposent que vous avez créé une tâche d’importation PST dans le service d’importation Office 365 à l’aide du chargement réseau ou de l’expédition de disque. Pour obtenir des instructions détaillées, consultez l’une des rubriques suivantes :
    
  - [Utiliser le chargement réseau pour importer des fichiers PST dans Office 365](use-network-upload-to-import-pst-files.md)
    
  - [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- Une fois que vous avez créé une tâche d’importation à l’aide du chargement réseau, l’état de la tâche d’importation sur la page d’importation dans le Centre de sécurité & conformité est définie sur **Analyse** en cours, ce qui signifie que Microsoft 365 analyse les données dans les fichiers PST que vous avez téléchargés. Cliquez **sur Actualiser** pour mettre à jour ![ ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) l’état de la tâche d’importation. 
    
- Pour les tâches d’importation d’expédition de disque, les données sont analysées par Microsoft 365 une fois que le personnel du centre de données Microsoft a reçu votre disque dur et chargé les fichiers PST dans l’espace de stockage Azure de votre organisation.
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a>Filtrer les données importées dans les boîtes aux lettres

Une fois que vous avez créé une tâche d’importation PST, suivez ces étapes pour filtrer les données avant de les importer dans Office 365.
  
1. Accédez à <https://compliance.microsoft.com> et connectez-vous à l'aide des informations d'identification d'un compte administrateur dans votre organisation.
    
2. Dans le volet gauche du Centre de conformité Microsoft 365, cliquez sur **Gouvernance des informations** \> **Importer**.
    
    Les tâches d’importation pour votre organisation sont répertoriées sous **l’onglet** Importation. La **valeur Analyse terminée** dans la colonne **État** indique les tâches d’importation qui ont été analysées par Microsoft 365 et sont prêtes à être importées.
    
    ![L’état d’analyse Microsoft 365 a analysé les données dans les fichiers PST](../media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. Sélectionnez la tâche d’importation à effectuer, puis cliquez sur **Importer vers Office 365**.
  
    Une page volante s’affiche avec des informations sur les fichiers PST et d’autres informations sur la tâche d’importation.

4. Cliquez **sur Importer Office 365**.
    
    La page **Filtrez vos données** s’affiche. Il contient des informations sur les données des fichiers PST de la tâche d’importation, notamment des informations sur l’âge des données. 
    
    ![La page Filtrer vos données affiche des informations sur les données des fichiers PST pour la tâche d’importation](../media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. Selon que vous souhaitez ou non découper les données importées dans Microsoft 365, sous Voulez-vous filtrer vos données **?**, faites l’une des choses suivantes :
  
    a. Cliquez **sur Oui, je souhaite le filtrer avant d’importer** pour découper les données que vous importez, puis cliquez sur **Suivant**.
  
    La **page Importer des données Office 365 page** s’affiche avec des informations détaillées sur les données de l’analyse Microsoft 365 effectuée. 
  
    ![Microsoft 365 affiche des informations détaillées sur les données de son analyse des fichiers PST](../media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    Le graphique de cette page indique la quantité de données qui seront importées. Les informations sur chaque type de message trouvé dans les fichiers PST sont affichées dans le graphique. Vous pouvez pointer le curseur sur chaque barre pour afficher des informations spécifiques sur ce type de message. Il existe également une liste de listes listes avec des valeurs d’âge différentes en fonction de l’analyse des fichiers PST. Lorsque vous sélectionnez un âge dans la liste de listes, le graphique est mis à jour pour afficher la quantité de données importées pour l’âge sélectionné. 
  
    b. Pour configurer des filtres d’ajout afin de réduire la quantité de données importées, cliquez sur **Plus d’options de filtrage.**
  
    ![Configurer les filtres sur la page Autres options pour découper les données importées](../media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    Vous pouvez configurer ces filtres :
  
      - **Âge** : sélectionnez un âge afin que seuls les éléments plus nouveaux que l’âge spécifié soient importés. Consultez la section [Plus d’informations](#more-information) pour obtenir une description de la façon Microsoft 365 les compartiments d’âge pour le **filtre Âge.** 
  
      - **Type** : cette section affiche tous les types de messages trouvés dans les fichiers PST de la tâche d’importation. Vous pouvez décocher une case en de côté d’un type de message que vous souhaitez exclure. Vous ne pouvez pas exclure le type de message Autre. Consultez la section [Plus d’informations](#more-information) pour obtenir la liste des éléments de boîte aux lettres inclus dans la catégorie Autre.
  
      - **Utilisateurs** : vous pouvez exclure les messages envoyés ou reçus par des personnes spécifiques. Pour exclure les personnes qui apparaissent dans le champ De :  , À : ou le champ Cc : des messages, cliquez sur Exclure les utilisateurs en de côté de ce type de destinataire. Tapez l’adresse de messagerie (adresse SMTP) de la personne, cliquez sur Ajouter une nouvelle icône pour l’ajouter à la liste des utilisateurs exclus pour ce type de destinataire, puis cliquez sur Enregistrer pour enregistrer la liste des utilisateurs ![ ](../media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) exclus.  
  
        > [!NOTE]
        > Microsoft 365'affiche pas les informations de données résultant de la définition du **filtre Personnes.** Toutefois, si vous définissez ce filtre pour exclure les messages envoyés ou reçus par des personnes spécifiques, ces messages seront exclus pendant le processus d’importation réel. 
  
    c. Cliquez **sur Appliquer** dans la page **volante Autres options** de filtrage pour enregistrer vos paramètres de filtre. 
  
    Les informations sur les données de la page Importer des données dans **Office 365** sont mises à jour en fonction de vos paramètres de filtre, y compris la quantité totale de données qui seront importées en fonction des paramètres de filtre. Un résumé des paramètres de filtre est également affiché. Vous pouvez cliquer **sur Modifier** en côté d’un filtre pour modifier le paramètre si nécessaire. 
  
    ![Les informations sur les données sont mises à jour en fonction de vos paramètres de filtre](../media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    d. Cliquez sur **Suivant**.
  
    Une page d’état s’affiche affichant vos paramètres de filtre. Là encore, vous pouvez modifier n’importe quel paramètre de filtre.
  
    e. Cliquez **sur Importer des données** pour démarrer l’importation. La quantité totale de données qui seront importées s’affiche. 
  
    Ou
  
    a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.
  
    b. Dans la page **Importer des données Office 365,** cliquez sur **Importer des données** pour démarrer l’importation. La quantité totale de données qui seront importées s’affiche. 
  
6. Sous **l’onglet Importer,** cliquez sur  ![ ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) Actualiser. L’état de la tâche d’importation s’affiche dans la **colonne État.**
  
7. Cliquez sur l’importation du travail pour afficher des informations plus détaillées, telles que l’état de chaque fichier PST et les paramètres de filtre que vous avez configurés.

## <a name="more-information"></a>Plus d’informations

- Comment déterminer Microsoft 365 incréments du filtre d’âge ? Lorsque Microsoft 365 analyse un fichier PST, il examine l’horodat d’envoi ou de réception de chaque élément (si un élément possède un horodaodaté envoyé et reçu, la date la plus ancienne est sélectionnée). Ensuite, Microsoft 365 la valeur de l’année pour cet timestamp et la compare à la date actuelle pour déterminer l’âge de l’élément. Ces âges sont ensuite utilisés comme valeurs dans la liste liste de listes pour le **filtre Âge.** Par exemple, si un fichier PST a des messages de 2016, 2015  et 2014, les valeurs dans le filtre Âge sont **1 an,** **2 ans** et **3 ans**.
  
- Le tableau suivant répertorie les types de messages inclus dans la catégorie **Autre** dans le filtre **Type** de la page volante Autres **options** (voir l’étape 5b de la procédure précédente). Actuellement, vous ne pouvez pas exclure des éléments de la catégorie « Autre » lorsque vous importez des PST dans Office 365. 
  
    |**ID de la classe de message**|**Éléments de boîte aux lettres qui utilisent cette classe de message**|
    |:-----|:-----|
    |IPM. Activité  <br/> |Entrées de journal  <br/> |
    |IPM.Document  <br/> |Documents et fichiers (non joints à un message électronique)  <br/> |
    |IPM. Fichier  <br/> |(identique à IPM.Document)  <br/> |
    |IPM. Note.IMC.Notification  <br/> |Rapports envoyés par internet mail Connecter, qui est la passerelle Exchange Server internet  <br/> |
    |IPM. Note.Microsoft.Fax  <br/> |Messages de télécopie  <br/> |
    |IPM. Note.Rules.Oof.Template.Microsoft  <br/> |Messages d’autoreply d’in-office  <br/> |
    |IPM. Note.Rules.ReplyTemplate.Microsoft  <br/> |Réponses envoyées par une règle de boîte de réception  <br/> |
    |IPM. OLE. Classe  <br/> |Exceptions pour une série périodique  <br/> |
    |IPM. Recall.Report  <br/> |Rapports de rappel de message  <br/> |
    |IPM. Distant  <br/> |Messages électroniques distants  <br/> |
    |IPM. Rapport  <br/> |Rapports d’état des éléments  <br/> |
