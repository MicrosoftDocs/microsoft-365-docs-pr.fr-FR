---
title: Service de processeur de données pour les demandes des personnes concernées pour le RGPD et le CCPA
description: Découvrez comment utiliser les produits Microsoft, les services et les outils d’administration pour rechercher et agir sur des données personnelles afin de répondre aux DSRs.
keywords: Microsoft 365, Microsoft 365 Éducation, documentation Microsoft 365, RGPD
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: daniha
author: DaniHalfin
manager: dansimp
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
ms.openlocfilehash: 525b8b0783886a7449be72c89a2aa624afda9929
ms.sourcegitcommit: 3ddcf08e8deec087df1fe524147313f1cb12a26d
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45023596"
---
# <a name="data-processor-service-for-windows-data-subject-requests-for-the-gdpr-and-ccpa"></a>Service de processeur de données pour les demandes des personnes concernées pour le RGPD et le CCPA 

>[!NOTE]
>Cette rubrique est destinée aux participants au programme de prévisualisation du service de traitement des données pour Windows et nécessite l'acceptation de conditions d'utilisation spécifiques. Pour en savoir plus sur le programme et accepter les conditions d’utilisation, voir [https://aka.ms/dpswpublicpreview](https://aka.ms/dpswpublicpreview).

## <a name="introduction-to-data-subject-requests-dsrs"></a>Présentation des demandes des personnes concernées (DPC) 
Le Règlement général sur la protection des données (RGPD) de l’UE accorde le droit aux individus (appelés, dans le règlement, _personnes concernées_) de gérer les données personnelles qui ont été collectées par un employeur ou tout autre type d’agence ou d’organisation (également appelé _responsable du traitement des données_ ou _responsable du traitement_). Dans le RGPD, les données personnelles sont définies de façon générale comme toute donnée relative à une personne physique identifiée ou identifiable. Le RGPD confère aux personnes concernées des droits précis sur leurs données personnelles ; ces droits vous donnent la possibilité d’obtenir des copies de ces données personnelles, de les modifier, d’en limiter le traitement, de les supprimer ou de les recevoir dans un format électronique afin de pouvoir les transférer à un autre responsable du traitement. Une demande officielle d’une personne concernée à un responsable du traitement pour effectuer une action sur ses données personnelles est appelée _demande de droits de la personne concernée_ ou DPC dans le présent document. 

De même, le CCPA (California Consumer Privacy Act), prévoit des droits de confidentialité et des obligations pour les consommateurs de la Californie, y compris des droits similaires aux droits des personnes concernées du RGPD, tels que le droit de supprimer, d’accéder et de recevoir (portabilité) leurs informations personnelles. Le CCPA prévoit également des publications d’informations, des protections contre la discrimination des personnes faisant usage de leurs droits et la possibilité d’opter pour ou contre certains transferts de données classés en tant que « ventes ». Les ventes sont largement définies pour inclure le partage de données à des fins importantes. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) et le [Forum aux questions California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

The guide discusses how to use Microsoft products, services and administrative tools to help our controller customers find and act on personal data to respond to DSRs. Specifically, this includes how to find, access, and act on personal data that reside in the Microsoft cloud. Here’s a quick overview of the processes outlined in this guide: 

1. **Accéder** : récupérez des données personnelles qui résident dans le cloud Microsoft et, si nécessaire, effectuez-en une copie pour la personne concernée. 
2. **Supprimer** : supprimez définitivement des données personnelles qui résidaient dans le cloud Microsoft. 
3. **Exporter** : fournissez une copie électronique (dans un format lisible par une machine) des données personnelles à la personne concernée. Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable.

Les informations à caractère personnel sous CCPA englobent toutes les informations relatives à une personne identifiée ou identifiable. Aucune distinction n’est faite entre les rôles privé, public et professionnel d’une personne. Le terme défini « informations personnelles » est à peu près aligné sur celui de « données personnelles » dans le RGPD. Toutefois, le CCPA inclut également les données relatives à la famille et au foyer. Pour plus d’informations sur le CCPA, voir le [California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/offering-ccpa) et le [Forum aux questions California Consumer Privacy Act](https://docs.microsoft.com/microsoft-365/compliance/ccpa-faq).

Chaque section de ce guide décrit les procédures techniques qu’une organisation étant une entité de contrôle des données peut suivre pour répondre à une DPC pour des données personnelles dans le cloud Microsoft. 

## <a name="terminology"></a>Terminologie 
Vous trouverez ci-dessous des définitions de termes utilisés dans ce guide. 

* _Contrôleur_ : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui, seul ou conjointement avec d’autres, détermine les finalités et les moyens du traitement des données personnelles ; lorsque les finalités et les moyens du traitement sont déterminés par la législation de l’Union ou des États membres, le contrôleur peut être désigné, ou les critères spécifiques relatifs à sa nomination peuvent être définis, par la législation de l’Union ou des États membres. 

* _Données personnelles et personne concernée par le traitement des données_ : elles correspondent aux informations relatives à une personne naturelle identifiée ou identifiable (« la personne concernée par le traitement des données ») ; une personne naturelle identifiable est une personne qui peut être identifiée, directement ou indirectement, notamment par référence à un identificateur par exemple, un nom, un numéro d’identification, des données de localisation, un identificateur en ligne, ou un ou plusieurs facteurs spécifiques de l’identité physique, physiologique, génétique, mentale, économique, culturelle ou sociale de cette personne naturelle. 

* _Sous-traitant_ : la personne physique ou morale, l’autorité publique, le service ou tout autre organisme qui traite des données personnelles pour le compte du contrôleur. 

* _Données client_ : toutes les données, y compris tous les fichiers texte, son, vidéo ou image et les logiciels qui ont été fournis à Microsoft par le client ou pour son compte dans le cadre du service d’entreprise. 

* _Les données de diagnostic Windows_ : donnés techniques vitales des appareils Windows, relatives aux appareils et aux performances de Windows et du logiciel associé. Il permet de maintenir Windows à jour, sécurisé, fiable, performant et amélioré dans Windows par le biais de l’analyse globale de l’utilisation de Windows. Voici quelques exemples de données de diagnostic Windows : type de matériel utilisé, applications installées avec leur utilisation respective et informations de fiabilité sur les pilotes d’appareils. Certains composants et applications Windows se connectent directement aux services Microsoft, mais les données échangées ne correspondent pas à des données de diagnostic Windows. Par exemple, l’échange d’un emplacement d’utilisateur pour la météo locale ou les actualités n’est pas un exemple de données de diagnostic de Windows. 

## <a name="how-to-use-this-guide"></a>Comment utiliser ce guide 

Lorsque vous utilisez le service de traitement des données pour les appareils inscrits à Windows, Windows génère des informations, connues sous le nom de données de diagnostic Windows, afin de fournir le service.

## <a name="windows-diagnostic-data"></a>Données de diagnostic Windows 

Microsoft vous offre la possibilité d'accéder, de supprimer et d'exporter les données de diagnostic Windows associées à l'utilisation par un utilisateur du service de traitement des données pour Windows.

>[!IMPORTANT]
>La possibilité de rectifier les données de diagnostic Windows n’est pas prise en charge. Les données de diagnostic Windows constituent des actions factuelles effectuées au sein de Windows, et les modifications apportées à ces données compromettent l'historique des actions, ce qui augmente les risques de sécurité et nuit à la fiabilité. Toutes les données traitées dans ce document sont considérées comme des données de diagnostic Windows. 

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Exécution des DSR à partir des données de diagnostic Windows 

Microsoft permet de supprimer et d’exporter certaines données de diagnostic Windows, et d’y accéder, via le portail Azure et directement aussi via des interfaces de programmation d’applications (API).

### <a name="step-1-access"></a>Étape 1 : Accéder 

L’administrateur du locataire est la seule personne au sein de votre organisation qui peut accéder aux données de diagnostic Windows associées à l’utilisation par un utilisateur d’un service de traitement de données pour l’appareil inscrit à Windows. Les données récupérées pour une demande d’accès seront fournies par le biais de l’exportation dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué ci-dessus, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité ou la stabilité de l’appareil Windows. 

Microsoft offre une expérience de portail permettant à l’administrateur client de l’entreprise cliente de gérer les demandes d’accès de personne concernée. [Azure DSR, partie 2, étape 3 : exporter](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), décrit l’exécution d’une demande d’accès au DSR, via l’exportation, via le portail Azure.

### <a name="step-2-delete"></a>Étape 2 : Supprimer 

Microsoft permet d’exécuter des requêtes de suppression de DSR basées sur l’utilisateur en fonction de l’objet Azure Active Directory d’un utilisateur particulier.

Pour les demandes de suppression basée sur l’utilisateur, Microsoft offre une expérience de portail permettant à l’administrateur client de l’entreprise cliente de gérer les demandes de suppression de DSR. [Azure DSR, partie 1, étape 5 : supprimer](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete), décrit l’exécution d’une demande de suppression de DSR via le portail Azure. 

Microsoft permet de supprimer des utilisateurs, ce qui permet de supprimer des données client directement via une interface de programmation d’application (API) préexistante. Les détails sont décrits dans la [documentation de référence de l’API ](https://docs.microsoft.com/graph/api/directory-deleteditems-delete?view=graph-rest-beta). 

>[!IMPORTANT]  
>La suppression des données collectées ne bloque pas la collecte plus approfondie. Pour désactiver la collecte de données, suivez la procédure décrite dans la [documentation de référence de service correspondante](https://docs.microsoft.com/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).
 
 De plus, les demandes de suppression basée sur l’utilisateur nécessitent la suppression du compte d’utilisateur proprement dit. 

### <a name="step-3-export"></a>Étape 3 : Exporter 

L’administrateur du locataire est la seule personne au sein de votre organisation qui peut accéder aux données de diagnostic Windows associées à l’utilisation par un utilisateur d’un service de traitement de données pour l’appareil inscrit à Windows. Les données récupérées pour une demande d’exportation seront fournies dans un format lisible par l’ordinateur et seront fournies dans des fichiers qui permettront à l’utilisateur de savoir à quels appareils et services les données sont associées. Comme indiqué ci-dessus, les données récupérées n’incluent pas de données susceptibles de compromettre la sécurité ou la stabilité de l’appareil Windows. [Azure DSR, partie 2, étape 3 : exporter](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure#step-3-export), décrit l’exécution d’une demande d’exportation de DSR via le portail Azure. 

Microsoft permet d’exporter des données client directement via une interface de programmation d’application (API) préexistante. Les détails sont décrits dans la [documentation de référence de l’API ](https://docs.microsoft.com/graph/api/user-exportpersonaldata?view=graph-rest-1.0).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notification des problèmes d’exportation ou de suppression 

Si vous rencontrez des problèmes lorsque vous exportez ou supprimez des données sur le portail Azure, accédez au panneau **Aide + Support** du portail Azure et envoyez un nouveau ticket sous **Gestion des abonnements > Autre demande de conformité et de sécurité > Confidentialité et demandes dans le cadre du RGPD**. 