---
title: Créer et gérer des règles de détection personnalisées dans Microsoft 365 Defender
description: Découvrez comment créer et gérer des règles de détection personnalisées basées sur des requêtes de repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, recherche, requête, télémétrie, détections personnalisées, règles, schéma, kusto, RBAC, autorisations, Microsoft Defender pour point de terminaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: f37cc63c958331f7c03e09689de92c73fd06b4d4
ms.sourcegitcommit: 7cc2be0244fcc30049351e35c25369cacaaf4ca9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51952559"
---
# <a name="create-and-manage-custom-detections-rules"></a>Créer et gérer des règles de détection personnalisées

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


**S’applique à :**
- Microsoft 365 Defender
- Microsoft Defender pour point de terminaison

Les règles de détection personnalisées sont des règles que vous pouvez concevoir et modifier à l’aide de requêtes [de repérage](advanced-hunting-overview.md) avancé. Ces règles vous permet de surveiller de manière proactive différents événements et états système, y compris les activités suspectées de violation et les points de terminaison mal configurés. Vous pouvez les configurer pour qu’ils s’exécutent à intervalles réguliers, générant des alertes et prenant des mesures de réponse chaque fois qu’il existe des correspondances.

## <a name="required-permissions-for-managing-custom-detections"></a>Autorisations requises pour la gestion des détections personnalisées

Pour gérer les détections personnalisées, vous devez avoir l’un des rôles ci-après :

- **Administrateur de sécurité**: les utilisateurs ayant [ce rôle Azure Active Directory gérer](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) les paramètres de sécurité dans Microsoft 365 centre de sécurité et d’autres portails et services.

- **Opérateur de sécurité**: les utilisateurs dotés de ce [rôle Azure Active Directory](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#security-administrator) peuvent gérer les alertes et ont un accès global en lecture seule aux fonctionnalités liées à la sécurité, y compris à toutes les informations dans Microsoft 365 centre de sécurité. Ce rôle est suffisant pour la gestion des détections personnalisées uniquement si le contrôle d’accès basé sur un rôle (RBAC) est désactivé dans Microsoft Defender pour point de terminaison. Si vous avez configuré RBAC, vous avez également besoin de l’autorisation gérer les **paramètres** de sécurité pour Defender for Endpoint.

Pour gérer les autorisations requises, un **administrateur général** peut :

- Attribuez le  **rôle d’administrateur de sécurité** ou d’opérateur de sécurité [dans Microsoft 365'administration sous](https://admin.microsoft.com/) Administrateur de **sécurité** des  >  **rôles.**
- Vérifiez les paramètres RBAC pour Microsoft Defender pour le point de terminaison [dans Centre de sécurité Microsoft Defender](https://securitycenter.windows.com/) sous **Paramètres**  >  **rôles d’autorisations.**  >   Sélectionnez le rôle correspondant pour attribuer **l’autorisation gérer les paramètres de** sécurité.

> [!NOTE]
> Pour gérer les  détections personnalisées, les opérateurs de sécurité auront besoin de l’autorisation gérer les **paramètres** de sécurité dans Microsoft Defender pour le point de terminaison si le contrôle d’accès en fonction du contrôle d’accès (RBAC) est allumé.

## <a name="create-a-custom-detection-rule"></a>Créer une règle de détection personnalisée
### <a name="1-prepare-the-query"></a>1. Préparez la requête.

Dans Microsoft 365 de sécurité, allez  à la recherche avancée et sélectionnez une requête existante ou créez une nouvelle requête. Lorsque vous utilisez une nouvelle requête, exécutez la requête pour identifier les erreurs et comprendre les résultats possibles.

>[!IMPORTANT]
>Pour empêcher le service de renvoyer trop d’alertes, chaque règle est limitée à générer seulement 100 alertes chaque fois qu’elle s’exécute. Avant de créer une règle, modifiez votre requête afin d’éviter les alertes pour une activité normale au quotidien.


#### <a name="required-columns-in-the-query-results"></a>Colonnes requises dans les résultats de la requête
Pour créer une règle de détection personnalisée, la requête doit renvoyer les colonnes suivantes :

- `Timestamp`— utilisé pour définir l’timestamp pour les alertes générées
- `ReportId`— active les recherche pour les enregistrements d’origine
- Une des colonnes suivantes qui identifient des appareils, des utilisateurs ou des boîtes aux lettres spécifiques :
    - `DeviceId`
    - `DeviceName`
    - `RemoteDeviceName`
    - `RecipientEmailAddress`
    - `SenderFromAddress` (expéditeur d’enveloppe ou adresse Return-Path'expéditeur)
    - `SenderMailFromAddress` (adresse de l’expéditeur affichée par le client de messagerie)
    - `RecipientObjectId`
    - `AccountObjectId`
    - `AccountSid`
    - `AccountUpn`
    - `InitiatingProcessAccountSid`
    - `InitiatingProcessAccountUpn`
    - `InitiatingProcessAccountObjectId`

>[!NOTE]
>La prise en charge d’entités supplémentaires est ajoutée lorsque de nouvelles tables sont ajoutées au schéma de [recherche avancé.](advanced-hunting-schema-tables.md)

Les requêtes simples, telles que celles qui n’utilisent pas l’opérateur ou l’opérateur pour personnaliser ou agréger des résultats, retournent généralement `project` `summarize` ces colonnes courantes.

Il existe plusieurs façons de s’assurer que les requêtes plus complexes retournent ces colonnes. Par exemple, si vous préférez agréger et compter par entité sous une colonne telle que , vous pouvez toujours renvoyer et en l’obtenant à partir de l’événement le plus récent impliquant `DeviceId` `Timestamp` chaque unique `ReportId` `DeviceId` .

L’exemple de requête ci-dessous compte le nombre d’appareils uniques ( ) avec détections antivirus et utilise ce nombre pour rechercher uniquement les appareils avec plus de `DeviceId` cinq détections. Pour renvoyer la dernière `Timestamp` et la `ReportId` correspondante, elle utilise l’opérateur `summarize` avec la `arg_max` fonction.

```kusto
DeviceEvents
| where Timestamp > ago(1d)
| where ActionType == "AntivirusDetection"
| summarize (Timestamp, ReportId)=arg_max(Timestamp, ReportId), count() by DeviceId
| where count_ > 5
```

> [!TIP]
> Pour de meilleures performances de requête, définissez un filtre d’heure qui correspond à la fréquence d’exécution prévue pour la règle. Étant donné que l’utilisation la moins fréquente _est toutes les 24 heures,_ le filtrage de la journée passée couvrira toutes les nouvelles données.

### <a name="2-create-new-rule-and-provide-alert-details"></a>2. Créez une règle et fournissez des détails sur l’alerte.

Avec la requête dans l’éditeur  de requête, sélectionnez Créer une règle de détection et spécifiez les détails d’alerte suivants :

- **Nom de la détection**: nom de la règle de détection
- **Fréquence**: intervalle d’exécution de la requête et d’action. [Voir les conseils supplémentaires ci-dessous](#rule-frequency)
- **Titre de l’alerte**: titre affiché avec les alertes déclenchées par la règle
- **Gravité :** risque potentiel du composant ou de l’activité identifié par la règle
- **Catégorie :** composant ou activité de menace identifié par la règle
- **MITRE ATT&techniques CK**: une ou plusieurs techniques d’attaque identifiées par la règle, comme documenté dans l’infrastructure [MITRE ATT&CK.](https://attack.mitre.org/) Cette section est masquée pour certaines catégories d’alertes, notamment les programmes malveillants, les ransomware, les activités suspectes et les logiciels indésirables
- **Description :** plus d’informations sur le composant ou l’activité identifié par la règle 
- **Actions recommandées**: actions supplémentaires que les répondeurs peuvent prendre en réponse à une alerte

#### <a name="rule-frequency"></a>Fréquence des règles
Lorsque vous enregistrez une nouvelle règle, elle s’exécute et recherche les correspondances des 30 derniers jours de données. La règle s’exécute ensuite à intervalles fixes, en appliquant une durée de recherche en fonction de la fréquence que vous choisissez :

- **Toutes les 24 heures**: s’exécute toutes les 24 heures, en vérifiant les données des 30 derniers jours
- **Toutes les 12 heures**: s’exécute toutes les 12 heures, en vérifiant les données des dernières 24 heures
- **Toutes les 3 heures :** s’exécute toutes les 3 heures, en vérifiant les données des 6 dernières heures
- **Toutes les heures**: s’exécute toutes les heures, en vérifiant les données des dernières 2 heures

Lorsque vous modifiez une règle, elle s’exécute avec les modifications appliquées lors de la prochaine utilisation prévue en fonction de la fréquence que vous avez définie.



>[!TIP]
> Faire correspondre les filtres d’heure de votre requête à la durée de la recherche. Les résultats en dehors de la durée de la recherche sont ignorés.  

Sélectionnez la fréquence qui correspond à la fréquence à laquelle vous souhaitez surveiller les détections. Prenez en compte la capacité de votre organisation à répondre aux alertes.

### <a name="3-choose-the-impacted-entities"></a>3. Choisissez les entités impactées.
Identifiez les colonnes dans les résultats de votre requête où vous vous attendez à trouver l’entité principale affectée ou concernée. Par exemple, une requête peut renvoyer des adresses d’expéditeur ( ou ) et de `SenderFromAddress` `SenderMailFromAddress` destinataire ( `RecipientEmailAddress` ). L’identification de l’entité principale concernée par l’identification de ces colonnes permet au service d’agréger les alertes pertinentes, de corréler les incidents et les actions de réponse cible.

Vous ne pouvez sélectionner qu’une seule colonne pour chaque type d’entité (boîte aux lettres, utilisateur ou appareil). Les colonnes qui ne sont pas renvoyées par votre requête ne peuvent pas être sélectionnées.

### <a name="4-specify-actions"></a>4. Spécifiez les actions.
Votre règle de détection personnalisée peut prendre automatiquement des mesures sur les appareils, les fichiers ou les utilisateurs renvoyés par la requête.

#### <a name="actions-on-devices"></a>Actions sur les appareils
Ces actions sont appliquées aux appareils dans la `DeviceId` colonne des résultats de la requête :
- **Isoler l’appareil**: utilise Microsoft Defender pour le point de terminaison pour appliquer une isolation complète du réseau, ce qui empêche l’appareil de se connecter à n’importe quelle application ou service. [En savoir plus sur l’isolation des ordinateurs Microsoft Defender pour Endpoint](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#isolate-devices-from-the-network)
- **Collecter un package d’examen**: collecte des informations sur l’appareil dans un fichier ZIP. [En savoir plus sur le package d’examen Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts#collect-investigation-package-from-devices)
- **Exécuter une analyse antivirus**: effectue une analyse complète Antivirus Windows Defender sur l’appareil
- **Lancer une enquête**: lance une [enquête automatisée](m365d-autoir.md) sur l’appareil
- **Restreindre l’exécution de** l’application : définit des restrictions sur l’appareil pour autoriser uniquement l’exécution des fichiers signés avec un certificat émis par Microsoft. [En savoir plus sur les restrictions d’application avec Microsoft Defender pour le point de terminaison](/microsoft-365/security/defender-endpoint/respond-machine-alerts#restrict-app-execution)

#### <a name="actions-on-files"></a>Actions sur les fichiers
Lorsqu’il est sélectionné, vous  pouvez choisir d’appliquer l’action de fichier de mise en quarantaine sur les fichiers dans la colonne , , ou dans la colonne des résultats `SHA1` de la `InitiatingProcessSHA1` `SHA256` `InitiatingProcessSHA256` requête. Cette action supprime le fichier de son emplacement actuel et place une copie en quarantaine.

#### <a name="actions-on-users"></a>Actions sur les utilisateurs
Lorsqu’il est  sélectionné, l’utilisateur Marquer comme étant compromis est pris sur les utilisateurs dans la colonne , ou dans la colonne des résultats `AccountObjectId` de la `InitiatingProcessAccountObjectId` `RecipientObjectId` requête. Cette action définit le niveau de risque des utilisateurs sur « élevé » Azure Active Directory, déclenchant les stratégies [de protection des identités correspondantes.](/azure/active-directory/identity-protection/overview-identity-protection)

> [!NOTE]
> L’action autoriser ou bloquer des règles de détection personnalisées n’est actuellement pas prise en charge sur Microsoft 365 Defender.

### <a name="5-set-the-rule-scope"></a>5. Définissez l’étendue de la règle.
Définissez l’étendue pour spécifier les appareils couverts par la règle. L’étendue influence les règles qui vérifient les appareils et n’affecte pas les règles qui vérifient uniquement les boîtes aux lettres et les comptes d’utilisateurs ou les identités.

Lors de la définition de l’étendue, vous pouvez sélectionner :

- Tous les appareils
- Groupes d’appareils spécifiques

Seules les données des appareils dans l’étendue seront interrogés. En outre, des actions seront prises uniquement sur ces appareils.

### <a name="6-review-and-turn-on-the-rule"></a>6. Examinez et allumez la règle.
Après avoir passé en revue la règle, **sélectionnez Créer** pour l’enregistrer. La règle de détection personnalisée s’exécute immédiatement. Il s’exécute à nouveau en fonction de la fréquence configurée pour vérifier les correspondances, générer des alertes et prendre des mesures de réponse.


>[!Important] 
>Les détections personnalisées doivent être régulièrement examinées pour des raisons d’efficacité et d’efficacité. Pour vous assurer que vous créez des détections qui déclenchent de vraies alertes, prenez le temps de passer en revue vos détections personnalisées existantes en suivant les étapes de la procédure De gestion des règles de [détection personnalisées existantes.](#manage-existing-custom-detection-rules) <br>  
Vous conservez le contrôle sur l’étendue ou la spécificité de vos détections personnalisées afin que les fausses alertes générées par les détections personnalisées indiquent la nécessité de modifier certains paramètres des règles.


## <a name="manage-existing-custom-detection-rules"></a>Gérer les règles de détection personnalisées existantes
Vous pouvez afficher la liste des règles de détection personnalisées existantes, vérifier leurs précédentes séries et passer en revue les alertes qu’elles ont déclenchées. Vous pouvez également exécuter une règle à la demande et la modifier.

>[!TIP]
> Les alertes détectées par des détections personnalisées sont disponibles sur les alertes et les API d’incident. Pour plus d’informations, [consultez la Microsoft 365 API Defender.](api-supported.md)

### <a name="view-existing-rules"></a>Afficher les règles existantes

Pour afficher toutes les règles de détection personnalisées existantes, **accédez à**  >  **Détections personnalisées de repérage.** La page répertorie toutes les règles avec les informations d’exécuter suivantes :

- **Dernière série**: lorsqu’une règle a été exécuté pour la dernière fois pour vérifier les correspondances de requête et générer des alertes
- **État de la dernière fois**: si une règle s’est correctement exécuté
- **Next run**—the next scheduled run
- **État**: si une règle a été allumée ou désactivée

### <a name="view-rule-details-modify-rule-and-run-rule"></a>Afficher les détails de la règle, modifier la règle et exécuter la règle

Pour afficher des informations complètes sur une règle de détection personnalisée, sélectionnez  >  **détections personnalisées** de repérage, puis sélectionnez le nom de la règle. Vous pouvez ensuite afficher des informations générales sur la règle, notamment son état d’application et son étendue. La page fournit également la liste des alertes et des actions déclenchées.

![Page des détails des règles de détection personnalisées](../../media/custom-detection-details.png)<br>
*Détails des règles de détection personnalisées*

Vous pouvez également prendre les mesures suivantes sur la règle à partir de cette page :

- **Exécuter**: exécutez la règle immédiatement. Cela réinitialise également l’intervalle pour la prochaine suite.
- **Modifier**— modifier la règle sans modifier la requête
- **Modifier la requête —** modifier la requête dans le recherche avancée
- **Activer**  /  **Désactiver :** activer la règle ou l’arrêter d’être en cours d’exécution
- **Supprimer**: désactiver la règle et la supprimer

### <a name="view-and-manage-triggered-alerts"></a>Afficher et gérer les alertes déclenchées

Dans l’écran détails de la règle (**Détections** personnalisées de repérage [nom de la règle] ), allez à  >    >   **Alertes déclenchées**, qui répertorie les alertes générées par des correspondances à la règle. Sélectionnez une alerte pour afficher des informations détaillées à son sujet et prendre les mesures suivantes :

- Gérer l’alerte en setting its status and classification (true or false alert)
- Lier l’alerte à un incident
- Exécuter la requête qui a déclenché l’alerte sur le hunting avancé

### <a name="review-actions"></a>Examiner les actions
Dans l’écran détails de la règle (**Détections** personnalisées de repérage [nom de la  >    >  **règle]**), allez à **Actions** déclenchées , qui répertorie les actions entreprises en fonction des correspondances à la règle.

>[!TIP]
>Pour afficher rapidement des informations et agir sur un élément d’un tableau, utilisez la colonne de sélection [&#10003;] à gauche du tableau.

>[!NOTE]
>Certaines colonnes de cet article peuvent ne pas être disponibles dans Microsoft Defender pour endpoint. [Activer Microsoft 365 Defender pour qu’il](m365d-enable.md) recherche les menaces à l’aide de sources de données plus nombreuses. Vous pouvez déplacer vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison vers Microsoft 365 Defender en suivant les étapes de la procédure de migration des requêtes de recherche avancée à partir de Microsoft Defender pour le point de [terminaison.](advanced-hunting-migrate-from-mde.md)

## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des détections personnalisées](custom-detections-overview.md)
- [Vue d’ensemble du repérage avancé](advanced-hunting-overview.md)
- [Découvrir le langage de requête de repérage avancé](advanced-hunting-query-language.md)
- [Migrer des requêtes de recherche avancée à partir de Microsoft Defender pour le point de terminaison](advanced-hunting-migrate-from-mde.md)
