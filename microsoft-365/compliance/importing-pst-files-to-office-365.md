---
title: Vue d’ensemble de l’importation des fichiers PST de votre organisation
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser le Service d’importation dans le Centre de sécurité et de conformité pour importer en bloc des données de courrier (fichiers PST) vers des boîtes aux lettres d’utilisateurs.
ms.openlocfilehash: c645228598eb9cf0e6edca7104b8977e7eaf72f7
ms.sourcegitcommit: c75aac39ee8d93218a79585113ef6b36f47c9ddf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2021
ms.locfileid: "51408535"
---
# <a name="overview-of-importing-your-organizations-pst-files"></a>Vue d’ensemble de l’importation des fichiers PST de votre organisation

> [!NOTE]
> Cet article s’adresse aux administrateurs. Vous souhaitez importer des fichiers PST dans votre propre boîte aux lettres ? Consultez [Importer le courrier électronique, les contacts et le calendrier à partir d’un fichier .pst Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075).

Vous pouvez utiliser le Service d’importation dans le Centre de sécurité et de conformité pour importer rapidement en bloc des fichiers PST dans des boîtes aux lettres Exchange Online au sein de votre organisation. Vous pouvez importer des fichiers PST dans Office 365 de deux manières différentes :

- **Chargement réseau** ![Chargement sur le Cloud](../media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) : chargez les fichiers PST via le réseau vers un emplacement de stockage temporaire Azure dans le cloud Microsoft. Vous utilisez ensuite le Service d’importation Office 365 pour importer les données PST dans les boîtes aux lettres de votre organisation. 

- **Expédition de disque** ![Disque dur](../media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) : copiez les fichiers PST sur un disque dur chiffré avec BitLocker, puis expédiez physiquement le lecteur à Microsoft. Lorsque Microsoft reçoit le disque dur, le personnel du centre de données charge les données vers un emplacement de stockage temporaire Azure dans le cloud Microsoft. Vous utilisez ensuite le Service d’importation Office 365 pour importer les données dans les boîtes aux lettres de votre organisation.

## <a name="step-by-step-instructions"></a>Instructions détaillées
  
Pour obtenir des instructions détaillées sur l’importation en bloc des fichiers PST de votre organisation dans Office 365, consultez l’une des rubriques suivantes. 

- [Utiliser le chargement réseau pour importer des fichiers PST dans Office 365](use-network-upload-to-import-pst-files.md)

- [Utiliser l’envoi de lecteurs pour importer des fichiers PST](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Comment fonctionne l’importation de fichiers PST

Voici une illustration et une description du processus d’importation de fichiers PST complet. L’illustration présente le flux de travail principal et met en évidence les différences entre les modes de chargement réseau et d’expédition de disque.
  
![Flux de travail du processus d’importation de fichiers PST](../media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Téléchargez les outils d’importation de fichiers PST et la clé pour l’emplacement de stockage Azure privé** : la première étape consiste à télécharger l’outil et la clé d’accès utilisés pour charger les fichiers PST ou les copier sur un disque dur. Vous les obtenez à partir de la page **Importer** dans le Centre de sécurité et de conformité. La clé vous donne (ou au personnel du centre de données Microsoft en cas d’expédition de disque) les autorisations nécessaires pour charger des fichiers PST dans un emplacement de stockage Azure privé et sécurisé. Cette clé d’accès est propre à votre organisation et empêche l’accès non autorisé à vos fichiers PST après leur chargement dans le cloud Microsoft. Il n’est pas nécessaire que votre organisation dispose d’un abonnement Azure séparé pour importer des fichiers PST dans Microsoft 365. 
    
2. **Charger ou copier les fichiers PST** : l’étape suivante varie selon que vous utilisez le chargement réseau ou l’expédition de disque pour importer des fichiers PST. Dans les deux cas, vous devez utiliser l’outil et la clé de stockage sécurisée que vous avez obtenue à l’étape précédente.
    
    - **Chargement réseau :** L’outil AzCopy.exe (téléchargé à l’étape 1) est utilisé pour charger et stocker vos fichiers PST dans un emplacement de stockage Azure dans le Cloud Microsoft. L’emplacement de stockage Azure dans lequel vous chargez vos fichiers PST se situe dans le même centre de données régional Microsoft que votre organisation.
    
      Pour les charger, les fichiers PST que vous souhaitez importer doivent se trouver dans un partage de fichiers ou un serveur de fichiers au sein de votre organisation.
    
    - **Expédition de disque :** L’outil WAImportExport.exe (téléchargé à l’étape 1) est utilisé pour copier vos fichiers PST sur le disque dur. Cet outil chiffre le disque dur avec BitLocker, puis copie les fichiers PST sur le disque dur. Tout comme pour le chargement réseau, les fichiers PST que vous voulez importer sur le disque dur doivent se trouver dans un partage de fichiers ou un serveur de fichiers au sein de votre organisation.
    
3. **Créer un fichier de mappage d’importation de fichiers PST** : une fois que les fichiers PST ont été chargés vers l’emplacement de stockage Azure ou copiés sur un disque dur, l’étape suivante consiste à créer un fichier de valeurs séparées par des virgules (CSV) qui indique les boîtes aux lettres des utilisateurs dans lesquelles les fichiers PST seront importé (et un fichier PST peut être importé dans la boîte aux lettres principale ou la boîte aux lettres d’archivage d’un utilisateur). Le Service d’importation d’Office 365 utilise les informations pour importer les fichiers PST. 
    
4. **Créer une tâche d’importation de fichiers PST :** l’étape suivante consiste à créer une tâche d’importation de fichiers PST sur la page **Importer des fichiers PST** dans le Centre de sécurité et de conformité et à envoyer le fichier de mappage d’importation PST créé à l’étape précédente. Pour le chargement réseau (étant donné que les fichiers PST ont été chargés sur Azure), Microsoft 365 analyse les données contenues dans les fichiers PST, puis vous permet de définir des filtres qui contrôlent les données réellement importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d’importation de fichiers PST. 
    
    Pour une expédition de disque, quelques opérations supplémentaires se produisent à ce stade du processus.
    
    - Vous expédiez physiquement le disque dur à un centre de données Microsoft (l’adresse d’expédition du centre de données Microsoft s’affiche lorsque la tâche d’importation est créée).
    
    - Lorsque Microsoft reçoit le disque dur, le personnel du centre de données charge les fichiers PST sur le disque dur vers l’emplacement de stockage Azure de votre organisation. Comme indiqué précédemment, vos fichiers PST sont chargés vers un emplacement de stockage Azure qui se situe dans le même centre de données régional Microsoft que votre organisation.
    
      > [!NOTE]
      > Les fichiers PST sur le disque dur sont chargés sur Azure dans un délai de 7 à 10 jours ouvrables après la réception du disque dur par Microsoft.

      Tout comme pour le processus de chargement réseau, Microsoft 365 analyse ensuite les données contenues dans les fichiers PST et vous permet de définir des filtres qui contrôlent les données réellement importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d’importation de fichiers PST.
    
    - Microsoft vous réexpédie le disque dur.
    
5. **Filtrer les données PST qui seront importées dans les boîtes aux lettres** : une fois la tâche d’importation créée (et après le chargement des fichiers PST d’une tâche d’expédition de disque vers l’emplacement de stockage Azure), Microsoft 365 analyse les données dans les fichiers PST (de façon sécurisée) en identifiant l’âge des éléments et des différents types de message inclus dans les fichiers PST. Une fois l’analyse terminée et les données prêtes à être importées, vous avez la possibilité d’importer toutes les données contenues dans les fichiers PST. Vous pouvez également réduire la quantité de données importées en définissant des filtres qui contrôlent les données importées. 
    
6. **Lancer la tâche d’importation de fichiers PST** : une fois la tâche d’importation lancée, Microsoft 365 utilise les informations du fichier de mappage d’importation de fichiers PST pour importer les fichiers PST à partir de l’emplacement de stockage Azure vers les boîtes aux lettres des utilisateurs. Les informations relatives à l’état de la tâche d’importation (y compris les informations relatives à chaque fichier PST importé) s’affichent sur la page **Importer des fichiers PST** du Centre de sécurité et de conformité. Une fois la tâche d’importation terminée, l’état de la tâche est défini sur **Terminé**.
  
## <a name="why-import-email-data-to-microsoft-365"></a>Pourquoi importer des données de courrier dans Microsoft 365 ?

- C’est un bon moyen d’importer les données de messagerie archivées dans Microsoft 365.
    
- Vous pouvez utiliser la fonctionnalité [Importation intelligente](filter-data-when-importing-pst-files.md) pour filtrer les éléments des fichiers PST qui sont réellement importés dans les boîtes aux lettres cible. Vous pouvez ainsi réduire la quantité de données importées en définissant des filtres qui contrôlent les données importées. 
    
- L’importation de données de courrier dans Microsoft 365 aide votre organisation à respecter les règles de conformité en vous permettant de réaliser les opérations suivantes :
    
  - Activer [les boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et l’[archivage illimité](unlimited-archiving.md) pour donner aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire. 
    
  - Placez les boîtes aux lettres en [Conservation pour litige](./create-a-litigation-hold.md) pour conserver leur contenu. 
    
  - Utilisez [l’outil de recherche de contenu](content-search.md) pour rechercher du contenu de boîtes aux lettres. 
    
  - Utiliser [les Cas de découverte électronique](./get-started-core-ediscovery.md) pour gérer les enquêtes juridiques de votre organisation 
    
  - Utilisez les [stratégies de rétention](retention.md) dans le Centre de sécurité et de conformité pour contrôler la durée de conservation du contenu des boîtes aux lettres, puis supprimez le contenu à la fin de la période de rétention. 

  - Utilisez [les stratégies de conformité communication](communication-compliance.md) pour examiner les messages afin de vous assurer qu’ils sont conformes aux normes des messages et ajoutez un type de classification.
    
- L’importation de données dans Microsoft 365 permet également à votre organisation de se protéger contre la perte de données. Les données de courrier importées dans Microsoft 365 héritent des fonctionnalités de haute disponibilité d’Exchange Online.
    
- Les données de courrier sont disponibles pour les utilisateurs à partir de tous les périphériques, car elles sont stockées dans le cloud.
    
## <a name="importing-sharepoint-data-to-microsoft-365"></a>Importation des données SharePoint dans Microsoft 365

Vous pouvez également importer des fichiers et des documents sur des sites SharePoint et des comptes OneDrive dans votre organisation. Pour plus d’informations, voir les articles suivants :

- [Migrer vers SharePoint Online](/sharepointmigration/migrate-to-sharepoint-online)

- [Présentation de l'Outil de migration SharePoint](/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [Migrer vers SharePoint Online à l’aide de PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets)

- [Migrer le contenu du partage de vos fichiers vers SharePoint Online à l’aide d’Azure Data Box](/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)

## <a name="frequently-asked-questions-about-importing-pst-files"></a>Questions fréquemment posées sur l’importation des fichiers PST
  
Voici quelques questions fréquemment posées sur l’utilisation du Service d’importation Office 365 pour importer en bloc des fichiers PST dans des boîtes aux lettres Microsoft 365. 
  
- [Utilisation du chargement réseau pour importer des fichiers PST](#using-network-upload-to-import-pst-files)
  
- [Utilisation de l’expédition de disque pour importer des fichiers PST](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Utilisation du chargement réseau pour importer des fichiers PST

 **De quelles autorisations a-t-on besoin pour créer des tâches d’importation dans le Service d’importation Office 365 ?**
  
Le rôle Importation/Exportation de boîtes aux lettres doit vous avoir été attribué dans Exchange Online pour pouvoir importer des fichiers PST dans des boîtes aux lettres Microsoft 365. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle Importation/Exportation de boîte aux lettres au groupe de rôles Gestion de l’organisation. Vous pouvez aussi créer un nouveau groupe de rôles, lui attribuer le rôle Importation/Exportation de boîtes aux lettres, puis vous ajouter, vous ou d’autres utilisateurs, en tant que membre. Pour plus d’informations, consultez les sections « Ajouter un rôle à un groupe de rôles » ou « Créer un groupe de rôles » dans [Gérer les groupes de rôles dans Exchange Online](/Exchange/permissions-exo/role-groups).
  
En outre, pour créer des tâches d’importation dans le Centre de sécurité et de conformité, une des conditions suivantes doit être remplie :
  
- Vous devez avoir le rôle de destinataire de courrier dans Exchange Online. Par défaut, ce rôle est assigné aux groupes de rôles Gestion de l’organisation et Gestion des destinataires.

    Ou
    
- Vous devez être un administrateur général au sein de votre organisation.

> [!TIP]
> Envisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement conçu pour importer les fichiers PST dans Office 365. Pour obtenir le niveau minimum de privilèges requis pour importer des fichiers PST, affectez les rôles d’importation/exportation de boîte aux lettres et de destinataire de courrier au nouveau groupe de rôles et ajoutez ensuite les membres. 
  
 **Où le chargement réseau est-il disponible ?**
  
Le téléchargement en réseau est actuellement disponible dans ces régions : États-Unis, Canada, Brésil, Royaume-Uni, France, Allemagne, Suisse, Norvège, Europe, Inde, Asie de l'Est, Asie du Sud-Est, Japon, République de Corée, Australie et Émirats arabes unis (EAU). Le téléchargement par réseau sera bientôt disponible dans d'autres régions.
  
 **À combien revient l’importation de fichiers PST via le chargement du réseau ?**
  
Using network upload to import PST files is free.
  
Cela veut aussi dire qu’après avoir été supprimés de la zone de stockage Azure, les fichiers PST ne figurent plus dans la liste des fichiers d’une tâche d’importation terminée dans le Centre d’administration Microsoft 365. Même si une tâche d’importation figure toujours dans la page **Importer des données dans Office 365**, il est possible que la liste de fichiers PST soit vide au moment d’afficher les détails d’anciennes tâches d’importation.
  
 **Quelle version du format de fichier PST est prise en charge pour l’importation dans Office 365 ?**
  
Il existe deux versions du format de fichier PST : ANSI et Unicode. Nous vous recommandons d’importer des fichiers qui utilisent le format de fichier PST Unicode. Cependant, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux dont la langue utilise un jeu de caractères codés sur deux octets (DBCS), peuvent aussi être importés dans Office 365. Pour plus d’informations sur l’importation de fichiers PST ANSI, consultez l’étape 4 de l’article [Utiliser le chargement réseau pour importer des fichiers PST dans Office 365](./use-network-upload-to-import-pst-files.md).
  
Par ailleurs, les fichiers PST issus d’Outlook version 2007 et ultérieures peuvent être importés dans Office 365.
  
 **Une fois que mes fichiers PST ont été chargés dans la zone de stockage Azure, pendant combien de temps sont-ils conservés dans Azure avant d’être supprimés ?**
  
Si vous décidez d’importer des fichiers PST avec la méthode du chargement réseau, vous les chargez dans un conteneur d’objets blob Azure nommé `ingestiondata`. Si aucune tâche d’importation n’est en cours sur la page **Importer des fichiers PST** dans le Centre de sécurité et de conformité, tous les fichiers PST du conteneur `ingestiondata` dans Azure sont supprimés 30 jours après la création de la tâche d’importation la plus récente dans le Centre de sécurité et de conformité. Cela veut aussi dire que vous devez créer une nouvelle tâche d’importation dans le Centre de sécurité et de conformité (description à l’étape 5 dans les instructions de chargement réseau) dans les 30 jours de chargement des fichiers PST vers Azure.
  
Cela veut aussi dire qu’après avoir été supprimés de la zone de stockage Azure, les fichiers PST ne figurent plus dans la liste des fichiers d’une tâche d’importation terminée dans le Centre de sécurité et de conformité. Même si une tâche d’importation figure toujours dans la page **Importer des fichiers PST** dans le Centre de sécurité et de conformité, il est possible que la liste de fichiers PST soit vide au moment d’afficher les détails d’anciennes tâches d’importation.
  
 **Combien de temps faut-il compter avant qu’un fichier PST soit importé dans une boîte aux lettres ?**
  
Cela dépend de la capacité de votre réseau, mais le chargement de chaque téraoctet (To) de données dans la zone de stockage Azure de votre organisation prend généralement plusieurs heures. Après avoir été copié dans la zone de stockage Azure, un fichier PST est importé dans une boîte aux lettres Microsoft 365 à un débit d’au moins 24 Go par jour. Si cette vitesse ne répond pas à vos besoins, vous pouvez envisager d’autres méthodes pour récupérer des données de courrier dans Office 365. Pour obtenir plus d'informations, consultez l'article [Façons de migrer plusieurs comptes de messagerie vers Office 365](/Exchange/mailbox-migration/mailbox-migration).
  
En présence de plusieurs fichiers PST et de plusieurs boîtes aux lettres cibles, le processus d’importation s’exécute en parallèle ; en d’autres termes, chaque paire PST/boîte aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importés dans une même boîte aux lettres, ils sont importés simultanément.
  
 **Comment le processus d’importation PST traite-t-il les éléments de courrier en double ?**

Par défaut, le processus d’importation PST vérifie s’il existe des éléments dupliqués et ne copie pas les données d’un fichier PST dans la boîte aux lettres ou l’archive si un élément correspondant existe au sein du dossier cible dans la boîte aux lettres cible ou l’archive cible. Si vous réimportez le même fichier PST et spécifiez un autre dossier cible (à l’aide de la propriété TargetRootFolder dans le fichier de mappage d’importation PST) que celui spécifié dans une tâche d’importation précédente, tous les éléments du fichier PST sont réimportés.
 
 **Y a-t-il une limite de taille applicable aux messages lors de l’importation de fichiers PST ?**
  
Oui. Si un fichier PST contient un élément de boîte aux lettres dont la taille est supérieure à 150 Mo, l’élément sera ignoré lors du processus d’importation. Les éléments de plus de 150 Mo ne sont pas importés, car 150 Mo est la limite de taille des messages dans Exchange Online. Pour plus d'informations, consultez [Limites de messages dans Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#message-limits).
  
 **Les propriétés des messages, comme la date d’envoi ou de réception, la liste de destinataires, etc., sont-elles conservées après l’importation de fichiers PST dans une boîte aux lettres Microsoft 365 ?**
  
Oui. Les métadonnées du message d’origine sont inchangées pendant l’importation.
  
 **Une limite est-elle appliquée au nombre de niveaux d’une hiérarchie de dossiers pour un fichier PST que je souhaite importer dans une boîte aux lettres ?**
  
Oui. Vous ne pouvez pas importer un fichier PST comportant 300 niveaux de dossiers imbriqués ou plus.
  
 **Est-il possible d’utiliser le chargement réseau pour importer des fichiers PST dans une boîte aux lettres inactive Office 365 ?**
  
Oui, cela est désormais possible.
  
 **Est-il possible d’utiliser le chargement réseau pour importer des fichiers PST dans une boîte aux lettres d’archivage en ligne dans un déploiement hybride Exchange ?**
  
Oui, cela est désormais possible. 
  
 **Puis-je utiliser le chargement réseau pour importer des fichiers PST dans des dossiers publics dans Exchange Online ?**
  
Non, vous ne pouvez pas importer des fichiers PST dans des dossiers publics.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Utilisation de l’expédition de disque pour importer des fichiers PST

 **De quelles autorisations a-t-on besoin pour créer des tâches d’importation dans le Service d’importation Office 365 ?**
  
Le rôle Importation/Exportation de boîtes aux lettres doit vous avoir été attribué pour pouvoir importer des fichiers PST dans des boîtes aux lettres Microsoft 365. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle Importation/Exportation de boîte aux lettres au groupe de rôles Gestion de l’organisation. Vous pouvez aussi créer un nouveau groupe de rôles, lui attribuer le rôle Importation/Exportation de boîtes aux lettres, puis vous ajouter, vous ou d’autres utilisateurs, en tant que membre. Pour plus d’informations, consultez les sections « Ajouter un rôle à un groupe de rôles » ou « Créer un groupe de rôles » dans [Gérer les groupes de rôles dans Exchange Online](/Exchange/permissions-exo/role-groups).
  
En outre, pour créer des tâches d’importation dans le Centre de sécurité et de conformité, une des conditions suivantes doit être remplie :
  
- Vous devez avoir le rôle de destinataire de courrier dans Exchange Online. Par défaut, ce rôle est assigné aux groupes de rôles Gestion de l’organisation et Gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur général au sein de votre organisation.
    
> [!TIP]
> Envisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement conçu pour importer les fichiers PST dans Office 365. Pour obtenir le niveau minimum de privilèges requis pour importer des fichiers PST, affectez les rôles d’importation/exportation de boîte aux lettres et de destinataire de courrier au nouveau groupe de rôles et ajoutez ensuite les membres. 
  
 **Où l’expédition de disque est-elle disponible ?**
  
L’expédition de disque est actuellement disponible aux États-Unis, au Canada, au Brésil, au Royaume-Uni, en Europe, en Inde, en Asie de l’Est, en Asie du Sud-Est, au Japon, en République de Corée et en Australie. Ce service sera prochainement disponible dans d’autres régions.

> [!NOTE]
> À l'heure actuelle, l'envoi de lecteurs pour l'importation de fichiers PST n’est pas disponible en Allemagne et en Suisse. Ce Forum aux questions sera mis à jour lorsque l'envoi de lecteurs réseau sera disponible pour ces pays.
  
 **Quels sont les contrats de licences commerciaux qui prennent en charge l’expédition de disque ?**
  
L’expédition de disque en vue de l’importation de fichiers PST dans Microsoft 365 est disponible via le programme Accord Entreprise Microsoft (EA). L’expédition de disque n’est pas disponible dans le cadre d’un Contrat de Fourniture de Produits et de Services Microsoft (MPSA).
  
 **À combien revient l’expédition de disque en vue de l’importation de fichiers PST dans Microsoft 365 ?**
  
L’utilisation du service d’expédition de disque pour importer des fichiers PST dans des boîtes aux lettres Microsoft 365 revient à 2 dollars par Go de données. Par exemple, si vous expédiez un disque dur qui contient 1 000 Go (1 To) de fichiers PST, cela revient à 2 000 dollars. Vous pouvez travailler en collaboration avec un partenaire qui se chargera de payer les frais d’importation. Pour plus d’informations sur la recherche d’un partenaire, consultez la page [Trouver votre partenaire ou revendeur](../admin/manage/find-your-partner-or-reseller.md).
  
 **Quels types de disque dur est-il possible d’expédier ?**
  
Seuls les lecteurs SSD 2,5 pouces ou les disques durs internes 2,5 ou 3,5 pouces SATA II/III sont pris en charge par le Service d’importation Office 365. Vous pouvez utiliser des disques durs jusqu'à 10 To. Pour les tâches d’importation, uniquement le premier volume de données sur le disque dur est traité. Le volume de données doit être au format NTFS. Lorsque vous copiez des données sur un disque dur, vous pouvez connecter ce dernier directement au moyen d’un connecteur pour SSD de 2,5 pouces ou SATA II/III de 2,5 ou 3,5 pouces, ou vous pouvez le connecter en externe au moyen d’un adaptateur USB externe pour SSD de 2,5 pouces ou SATA II/III de 2,5 ou 3,5 pouces.
  
> [!IMPORTANT]
> Les disques durs externes fournis avec une carte USB intégrée ne sont pas pris en charge par le Service d’importation Office 365. En outre, le disque à l’intérieur du boîtier d’un disque dur externe ne peut pas être utilisé. Veuillez ne pas envoyer de disques durs externes. 
  
 **Combien de disques durs puis-je expédier pour une seule tâche d’importation ?**
  
Vous pouvez expédier au maximum 10 disques durs pour une même tâche d’importation.
  
 **Quel délai faut-il compter entre le moment où j’expédie mon disque dur et le moment où les données sont sur le centre de données Microsoft ?**
  
Cela dépend de plusieurs facteurs, comme votre proximité par rapport au centre de données Microsoft et le type d’expédition choisi pour l’envoi de votre disque dur (livraison le jour suivant, livraison à deux jours ou envoi économique). La plupart des expéditeurs vous communiquent un numéro de suivi pour suivre le statut de votre livraison.
  
 **Une fois mon disque dur arrivé au centre de données de Microsoft, combien de temps faut-il pour charger mes fichiers PST dans Azure ?**
  
Une fois votre disque dur réceptionné au centre de données de Microsoft, vous devrez patienter entre 7 et 10 jours ouvrable pour le chargement du fichier PST dans l’emplacement de stockage Azure de votre organisation. Les fichiers PST seront chargés dans un conteneur blob Azure nommé `ingestiondata`. 
  
 **Combien de temps faut-il compter avant qu’un fichier PST soit importé dans une boîte aux lettres ?**
  
Une fois les fichiers PST chargés dans l’espace de stockage Azure, Microsoft 365 analyse les données des fichiers PST (de manière sécurisée) afin d’identifier l’âge des éléments et les différents types de messages contenus dans les fichiers PST. Une fois cette analyse terminée, vous pourrez importer toutes les données des fichiers PST ou définir des filtres qui contrôlent les données importées. Après le démarrage de la tâche d’importation, un fichier PST est importé dans une boîte aux lettres Microsoft 365 à un débit d’au moins 24 Go par jour. Si cette vitesse ne répond pas à vos besoins, vous pouvez envisager d’autres méthodes pour récupérer des données de courrier dans Microsoft 365. Pour plus d’informations, consultez l’article [Méthodes de migration des comptes de courrier vers Microsoft 365](/Exchange/mailbox-migration/mailbox-migration).
  
En présence de plusieurs fichiers PST et de plusieurs boîtes aux lettres cibles, le processus d’importation s’exécute en parallèle ; en d’autres termes, chaque paire PST/boîte aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importés dans une même boîte aux lettres, ils sont importés simultanément.
  
 **Une fois que Microsoft a chargé mes fichiers PST dans Azure, pendant combien de temps sont-ils conservés dans Azure avant d’être supprimés ?**
  
Tous les fichiers PST de l’emplacement de stockage Azure de votre organisation (dans le conteneur blob nommé `ingestiondata`) sont supprimés 30 jours après la création de la dernière tâche d’importation sur la page **Importer des fichiers PST** dans le Centre de sécurité et de conformité. 
  
Cela veut aussi dire qu’après avoir été supprimés de la zone de stockage Azure, les fichiers PST ne figurent plus dans la liste des fichiers d’une tâche d’importation terminée dans le Centre de sécurité et de conformité. Même si une tâche d’importation figure toujours dans la page **Importer des fichiers PST** dans le Centre de sécurité et de conformité, il est possible que la liste de fichiers PST soit vide au moment d’afficher les détails d’anciennes tâches d’importation. 
  
 **Quelle version du format de fichier PST est prise en charge pour l’importation dans Microsoft 365 ?**
  
Il existe deux versions du format de fichier PST : ANSI et Unicode. Nous vous recommandons d’importer des fichiers qui utilisent le format de fichier PST Unicode. Cependant, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux dont la langue utilise un jeu de caractères codés sur deux octets (DBCS), peuvent aussi être importés dans Microsoft 365. Pour plus d’informations sur l’importation de fichiers PST ANSI, consultez l’étape 3 de l’article [Utiliser l’expédition de disque pour importer les fichiers PST de votre organisation dans Microsoft 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Par ailleurs, les fichiers PST issus d’Outlook version 2007 et ultérieures peuvent être importés dans Microsoft 365.
  
 **Y a-t-il une limite de taille applicable aux messages lors de l’importation de fichiers PST ?**
  
Oui. Si un fichier PST contient un élément de boîte aux lettres dont la taille est supérieure à 150 Mo, l’élément sera ignoré lors du processus d’importation. Les éléments de plus de 150 Mo ne sont pas importés, car 150 Mo est la limite de taille des messages dans Exchange Online. Pour plus d'informations, consultez [Limites de messages dans Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#message-limits).
  
  **Comment le processus d’importation PST traite-t-il les éléments de courrier en double ?**

Par défaut, le processus d’importation PST vérifie s’il existe des éléments dupliqués et ne copie pas les données d’un fichier PST dans la boîte aux lettres ou l’archive si un élément correspondant existe au sein du dossier cible dans la boîte aux lettres cible ou l’archive cible. Si vous réimportez le même fichier PST et spécifiez un autre dossier cible (à l’aide de la propriété TargetRootFolder dans le fichier de mappage d’importation PST) que celui spécifié dans une tâche d’importation précédente, tous les éléments du fichier PST sont réimportés.
 
 **Les propriétés des messages, comme la date d’envoi ou de réception, la liste de destinataires, etc., sont-elles conservées après l’importation de fichiers PST dans une boîte aux lettres Microsoft 365 ?**
  
Oui. Les métadonnées du message d’origine sont inchangées pendant l’importation
  
 **Une limite est-elle appliquée au nombre de niveaux d’une hiérarchie de dossiers pour un fichier PST que je souhaite importer dans une boîte aux lettres ?**
  
Oui. Vous ne pouvez pas importer un fichier PST comportant 300 niveaux de dossiers imbriqués ou plus.
  
 **Est-il possible d’expédier un disque en vue de l’importation de fichiers PST dans une boîte aux lettres inactive Microsoft 365 ?**
  
Oui, cela est désormais possible.
  
 **Est-il possible d’expédier un disque en vue d’importer des fichiers PST dans une boîte aux lettres d’archivage en ligne dans un déploiement hybride Exchange ?**
  
Oui, cela est désormais possible. 
  
 **Puis-je utiliser l’expédition de disque pour importer des fichiers PST dans des dossiers publics dans Exchange Online ?**
  
Non, vous ne pouvez pas importer des fichiers PST dans des dossiers publics.
  
 **Est-il possible de demander à Microsoft de réinitialiser mon disque dur avant de me le retourner ?**
  
Non, Microsoft ne peut pas réinitialiser les disques durs avant leur renvoi aux clients. Les disques durs vous sont renvoyés en l’état, tels que Microsoft les a reçus.
  
 **Est-il possible de demander à Microsoft de broyer mon disque dur au lieu de me le réexpédier ?**
  
Non, Microsoft ne peut pas détruire votre disque dur. Les disques durs vous sont renvoyés en l’état, tels que Microsoft les a reçus.
  
 **Par quels services de courrier l’expédition de retour est-elle assurée ?**
  
Si vous êtes un client résidant aux États-Unis ou en Europe, Microsoft fera appel à FedEx pour vous retourner le disque dur. Pour toutes les autres régions, Microsoft fait appel à DHL.
  
 **Quel est le coût de l’expédition de retour ?**
  
Les frais d’expédition de retour varient en fonction de votre proximité par rapport au centre de données Microsoft auquel vous avez expédié votre disque dur. Microsoft imputera les frais de retour de votre disque dur sur votre compte FedEx ou DHL. Les frais d’expédition de retour sont à votre charge.
  
 **Est-il possible d’expédier un disque dur à Microsoft en utilisant un service d’expédition de courrier spécial, comme une expédition personnalisée FedEx ?**
  
Oui.
  
 **If I have to ship my hard drive to another country, is there anything I need to do?**
  
The hard drive that you ship to Microsoft might have to cross international borders. Dans ce cas, vous avez la responsabilité de l’importation et ou de l’exportation du disque dur et des données qu’il contient, conformément à la législation en vigueur. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.