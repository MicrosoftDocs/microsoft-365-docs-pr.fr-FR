---
title: Stratégies recommandées pour la sécurisation des e-mails-Microsoft 365 pour les entreprises | Microsoft docs
description: Décrit les recommandations de Microsoft sur l’application de stratégies et de configurations liées aux e-mails.
ms.author: josephd
author: JoeDavies-MSFT
manager: Laurawi
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.reviewer: martincoetzer
ms.custom:
- it-pro
- goldenconfig
ms.collection:
- M365-identity-device-management
- M365-security-compliance
- remotework
- m365solution-identitydevice
- m365solution-scenario
ms.openlocfilehash: 5e7156a884093ca12fff7020bb045da30882547d
ms.sourcegitcommit: bcb88a6171f9e7bdb5b2d8c03cd628d11c5e7bbf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "48464335"
---
# <a name="policy-recommendations-for-securing-email"></a>Recommandations de stratégies pour sécuriser les e-mails

Cet article explique comment implémenter les stratégies d’identité et d’accès aux appareils recommandées pour protéger les clients de messagerie et de messagerie de l’organisation qui prennent en charge l’authentification moderne et l’accès conditionnel. Ce guide s’appuie sur les [stratégies courantes d’identité et d’accès aux appareils](identity-access-policies.md) et présente également quelques recommandations supplémentaires.

Ces recommandations sont basées sur trois niveaux de sécurité et de protection différents, qui peuvent être appliqués en fonction de la granularité de vos besoins : **ligne de base**, **sensibles**et **hautement réglementés**. Vous trouverez plus d’informations sur ces niveaux de sécurité et les systèmes d’exploitation clients recommandés auxquels cet article fait référence dans la [présentation des configurations et des stratégies de sécurité recommandées](microsoft-365-policies-configurations.md).

Ces recommandations nécessitent que vos utilisateurs utilisent des clients de messagerie modernes, notamment Outlook pour iOS et Android sur des appareils mobiles. Outlook pour iOS et Android prend en charge les meilleures fonctionnalités d’Office 365. Ces applications Outlook mobiles sont également conçues avec des fonctionnalités de sécurité qui prennent en charge l’utilisation mobile et fonctionnent conjointement avec d’autres fonctionnalités de sécurité Cloud Microsoft. Pour plus d’informations, consultez la rubrique [Outlook pour iOS et Android Forum aux questions](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/outlook-for-ios-and-android/outlook-for-ios-and-android-faq).

## <a name="updating-common-policies-to-include-email"></a>Mise à jour de stratégies communes pour inclure le courrier électronique

Pour protéger le courrier électronique, le diagramme suivant illustre les stratégies à mettre à jour à partir des stratégies courantes d’identité et d’accès aux appareils.

[![Résumé des mises à jour de stratégie pour protéger l’accès à teams et à ses services dépendants](../../media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)

[Afficher une version plus grande de cette image](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)

Notez l’ajout d’une nouvelle stratégie pour Exchange Online afin de bloquer les clients ActiveSync. Cela force l’utilisation d’Outlook Mobile.

Si vous avez inclus Exchange Online et Outlook dans l’étendue des stratégies lors de leur configuration, il vous suffit de créer la nouvelle stratégie pour bloquer les clients ActiveSync. Passez en revue les stratégies répertoriées dans le tableau suivant et effectuez les ajouts recommandés, ou confirmez que ceux-ci sont déjà inclus. Chaque stratégie lie les instructions de configuration associées dans les [stratégies courantes d’accès aux identités et aux appareils](identity-access-policies.md).

|Niveau de protection|Stratégies|Informations supplémentaires|
|:---------------|:-------|:----------------|
|**Baseline**|[Exiger l’authentification multifacteur lorsque le risque de connexion est *moyen* ou *élevé*](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|Inclure Exchange Online dans l’affectation d’applications Cloud|
|        |[Bloquer les clients ne prenant pas en charge l’authentification moderne](identity-access-policies.md#block-clients-that-dont-support-modern-authentication)|Inclure Exchange Online dans l’affectation d’applications Cloud|
|        |[Appliquer des stratégies de protection des données d’application](identity-access-policies.md#apply-app-data-protection-policies)|Assurez-vous qu’Outlook est inclus dans la liste des applications. Veillez à mettre à jour la stratégie pour chaque plateforme (iOS, Android, Windows)|
|        |[Exiger les applications approuvées et la protection des applications](identity-access-policies.md#require-approved-apps-and-app-protection)|Inclure Exchange Online dans la liste des applications Cloud|
|        |[Exiger des PC conformes](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|Inclure Exchange Online dans la liste des applications Cloud|
|        |[Bloquer les clients ActiveSync](#block-activesync-clients)|Ajouter cette nouvelle stratégie| 
|**Sensible**|[Exiger l’authentification multifacteur lorsque le risque de connexion est *faible*, *moyen* ou *élevé*](identity-access-policies.md#require-mfa-based-on-sign-in-risk)| Inclure Exchange Online dans l’affectation d’applications Cloud|
|         |[Exiger des PC conformes *et des* appareils mobiles](identity-access-policies.md#require-compliant-pcs-and-mobile-devices)|Inclure Exchange Online dans la liste des applications Cloud|
|**Hautement réglementé**|[*Toujours* exiger l’authentification multifacteur](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|Inclure Exchange Online dans l’affectation d’applications Cloud|

## <a name="block-activesync-clients"></a>Bloquer les clients ActiveSync

Cette stratégie empêche les clients ActiveSync de contourner les autres stratégies d’accès conditionnel. La configuration de la stratégie s’applique uniquement aux clients ActiveSync. En sélectionnant **[exiger la stratégie de protection des applications](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-conditional-access-grant#require-app-protection-policy)**, cette stratégie bloque les clients ActiveSync. Pour plus d’informations sur la création de cette stratégie, voir [require application protection Policy for Cloud App Access with ConditionalAttribute Access](https://docs.microsoft.com/azure/active-directory/conditional-access/app-protection-based-conditional-access).

- Suivez « étape 2 : configuration d’une stratégie d’accès conditionnel Azure AD pour Exchange Online avec ActiveSync (EAS) » dans le [scénario 1 : les applications Office 365 nécessitent des applications approuvées avec des stratégies de protection d’application](https://docs.microsoft.com/azure/active-directory/conditional-access/app-protection-based-conditional-access#scenario-1-office-365-apps-require-approved-apps-with-app-protection-policies), ce qui empêche les clients Exchange ActiveSync qui utilisent l’authentification de base de se connecter à Exchange Online.

Vous pouvez également utiliser des stratégies d’authentification pour [désactiver l’authentification de base](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/disable-basic-authentication-in-exchange-online), ce qui force toutes les demandes d’accès client à utiliser l’authentification moderne.

## <a name="set-up-message-encryption"></a>Configurer le chiffrement des messages

Avec les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME), qui tirent parti des fonctionnalités de protection d’Azure information protection, votre organisation peut facilement partager le courrier électronique protégé avec n’importe quel appareil. Les utilisateurs peuvent envoyer et recevoir des messages protégés avec d’autres organisations 365 Microsoft, ainsi que des non-clients utilisant Outlook.com, Gmail et d’autres services de messagerie.

Pour plus d’informations, reportez-vous à la rubrique [set up New Office 365 message Encryption Capabilities](https://docs.microsoft.com/microsoft-365/compliance/set-up-new-message-encryption-capabilities).

## <a name="next-steps"></a>Étapes suivantes

![Étape 4 : stratégies pour les applications Cloud Microsoft 365](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

Configurez les stratégies d’accès conditionnel pour :

- [Microsoft Teams](teams-access-policies.md)
- [SharePoint](sharepoint-file-access-policies.md)