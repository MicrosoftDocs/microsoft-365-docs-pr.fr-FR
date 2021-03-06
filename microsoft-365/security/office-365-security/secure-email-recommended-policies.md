---
title: 'Stratégies recommandées pour la sécurisation du courrier électronique : Microsoft 365 pour les | Documents Microsoft'
description: Décrit les recommandations de Microsoft sur l’application de stratégies et de configurations liées aux e-mails.
ms.author: josephd
author: JoeDavies-MSFT
manager: Laurawi
ms.prod: m365-security
ms.topic: article
audience: Admin
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
ms.technology: mdo
ms.openlocfilehash: c5f5837f4e4069a67bc080178fefd10bd2a08629
ms.sourcegitcommit: 7ee50882cb4ed37794a3cd82dac9b2f9e0a1f14a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "51599850"
---
# <a name="policy-recommendations-for-securing-email"></a>Recommandations de stratégies pour sécuriser les e-mails

**S’applique à**
- [Exchange Online Protection](exchange-online-protection-overview.md)
- [Microsoft Defender pour Office 365 : offre 1 et offre 2](defender-for-office-365.md)

Cet article explique comment implémenter les stratégies recommandées d’accès aux identités et appareils pour protéger les clients de messagerie et de messagerie de l’organisation qui la prise en charge de l’authentification moderne et de l’accès conditionnel. Ces instructions s’appuient sur les [stratégies](identity-access-policies.md) communes d’accès aux appareils et aux identités et incluent également quelques recommandations supplémentaires.

Ces recommandations sont basées sur trois niveaux différents de sécurité et de protection qui peuvent être appliqués en fonction de la granularité de vos besoins **:** base de **référence,** sensible et hautement **réglementé**. Vous trouverez plus d’informations sur ces niveaux de sécurité et les systèmes d’exploitation clients recommandés auxquels cet article fait référence dans la [présentation des configurations et des stratégies de sécurité recommandées](microsoft-365-policies-configurations.md).

Ces recommandations exigent que vos utilisateurs utilisent des clients de messagerie modernes, notamment Outlook pour iOS et Android sur les appareils mobiles. Outlook pour iOS et Android assurent la prise en charge des meilleures fonctionnalités de Office 365. Ces applications Outlook mobiles sont également conçus avec des fonctionnalités de sécurité qui permettent une utilisation mobile et fonctionnent avec d’autres fonctionnalités de sécurité cloud de Microsoft. Pour plus d’informations, [voir Outlook faq sur iOS et Android.](/exchange/clients-and-mobile-in-exchange-online/outlook-for-ios-and-android/outlook-for-ios-and-android-faq)

## <a name="update-common-policies-to-include-email"></a>Mettre à jour les stratégies courantes pour inclure le courrier électronique

Pour protéger le courrier électronique, le diagramme suivant illustre les stratégies à mettre à jour à partir des stratégies communes d’accès aux appareils et aux identités.

[![Résumé des mises à jour de stratégie pour la protection de l’accès à Teams et à ses services dépendants](../../media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-mail.png)

Notez l’ajout d’une nouvelle stratégie Exchange Online pour bloquer les clients ActiveSync. Cela force l’utilisation de Outlook mobile.

Si vous avez inclus Exchange Online et Outlook dans l’étendue des stratégies lorsque vous les avez définies, vous devez uniquement créer la nouvelle stratégie pour bloquer les clients ActiveSync. Examinez les stratégies répertoriées dans le tableau suivant et ajoutez les ajouts recommandés ou confirmez qu’elles sont déjà incluses. Chaque stratégie est liée aux instructions de configuration associées dans les [stratégies communes d’accès aux appareils et aux identités.](identity-access-policies.md)

|Niveau de protection|Stratégies|Plus d’informations|
|---|---|---|
|**Baseline**|[Exiger l’mf lorsque le risque de se connecte *est moyen* ou *élevé*](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|Inclure Exchange Online dans l’affectation des applications cloud|
||[Bloquer les clients ne prenant pas en charge l’authentification moderne](identity-access-policies.md#block-clients-that-dont-support-multi-factor)|Inclure Exchange Online dans l’affectation des applications cloud|
||[Appliquer des stratégies de protection des données APP](identity-access-policies.md#apply-app-data-protection-policies)|Assurez-vous Outlook est inclus dans la liste des applications. Assurez-vous de mettre à jour la stratégie pour chaque plateforme (iOS, Android, Windows)|
||[Exiger des applications approuvées et la protection des applications](identity-access-policies.md#require-approved-apps-and-app-protection)|Inclure Exchange Online dans la liste des applications cloud|
||[Exiger des PC conformes](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|Inclure des Exchange Online dans la liste des applications cloud|
||[Bloquer les clients ActiveSync](#block-activesync-clients)|Ajouter cette nouvelle stratégie|
|**Sensible**|[Exiger l’mf lorsque le risque de se connecte *est faible,* *moyen* ou *élevé*](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|Inclure Exchange Online dans l’affectation des applications cloud|
||[Exiger des PC et *des appareils* mobiles conformes](identity-access-policies.md#require-compliant-pcs-and-mobile-devices)|Inclure Exchange Online dans la liste des applications cloud|
|**Hautement réglementé**|[*Toujours exiger* l’mf d’fa](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|Inclure Exchange Online dans l’affectation des applications cloud|
|

## <a name="block-activesync-clients"></a>Bloquer les clients ActiveSync

Cette stratégie empêche les clients ActiveSync de contourner les autres stratégies d’accès conditionnel. La configuration de stratégie s’applique uniquement aux clients ActiveSync. En sélectionnant **[Exiger la stratégie de protection des](/azure/active-directory/conditional-access/concept-conditional-access-grant#require-app-protection-policy)** applications, cette stratégie bloque les clients ActiveSync. Pour plus d’informations sur la création de cette stratégie, voir La stratégie Exiger la protection des applications pour l’accès aux applications [cloud avec accès conditionnel.](/azure/active-directory/conditional-access/app-protection-based-conditional-access)

- Suivez « Étape 2 : Configurer une stratégie d’accès conditionnel Azure AD pour Exchange Online avec ActiveSync (EAS) » dans le scénario [1](/azure/active-directory/conditional-access/app-protection-based-conditional-access#scenario-1-office-365-apps-require-approved-apps-with-app-protection-policies): les applications Office 365 nécessitent des applications approuvées avec des stratégies de protection des applications, ce qui empêche les clients Exchange ActiveSync qui exploitent l’authentification de base de se connecter à Exchange Online.

Vous pouvez également utiliser [](/exchange/clients-and-mobile-in-exchange-online/disable-basic-authentication-in-exchange-online)des stratégies d’authentification pour désactiver l’authentification de base, ce qui force toutes les demandes d’accès client à utiliser l’authentification moderne.

## <a name="limit-access-to-exchange-online-from-outlook-on-the-web"></a>Limiter l’accès Exchange Online des Outlook sur le web

Vous pouvez restreindre la possibilité pour les utilisateurs de télécharger des pièces jointes à partir de Outlook sur le web sur des appareils umnanaged. Les utilisateurs de ces appareils peuvent afficher et modifier ces fichiers à l’aide de Office Online sans fuite ni stockage des fichiers sur l’appareil. Vous pouvez également empêcher les utilisateurs de voir les pièces jointes sur un appareil non utilisé.

Voici les étapes à effectuer :

1. [Connecter à une session PowerShell Exchange Online distante.](/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)
2. Si vous n’avez pas encore OWA stratégie de boîte aux lettres, créez-en une avec la cmdlet [New-OwaMailboxPolicy.](/powershell/module/exchange/new-owamailboxpolicy)
3. Si vous souhaitez autoriser l’affichage des pièces jointes sans téléchargement, utilisez la commande ci-après :

   ```powershell
   Set-OwaMailboxPolicy -Identity Default -ConditionalAccessPolicy ReadOnly
   ```

4. Si vous souhaitez bloquer les pièces jointes, utilisez la commande ci-après :

   ```powershell
   Set-OwaMailboxPolicy -Identity Default -ConditionalAccessPolicy ReadOnlyPlusAttachmentsBlocked
   ```

5. Dans le portail Azure, créez une stratégie d’accès conditionnel avec les paramètres ci-après :

   **Affectations** \> **Utilisateurs et groupes**: sélectionnez les utilisateurs et groupes appropriés à inclure et à exclure.

   **Affectations** \> **Applications ou actions** \> cloud **Applications cloud** \> **Include** \> **Sélectionner des applications**: **sélectionnez Office 365 Exchange Online**

   **Contrôles d’accès** \> **Session :** sélectionner **utiliser les restrictions appliquées par l’application**

## <a name="require-that-ios-and-android-devices-must-use-outlook"></a>Exiger que les appareils iOS et Android doivent utiliser Outlook

Pour vous assurer que les utilisateurs d’appareils iOS et Android peuvent uniquement accéder au contenu scolaire ou professionnels à l’aide de Outlook pour iOS et Android, vous avez besoin d’une stratégie d’accès conditionnel qui cible ces utilisateurs potentiels.

Consultez les étapes de configuration de cette stratégie dans Gérer l’accès à la collaboration de messagerie à l’aide de [Outlook pour iOS et Android.](/mem/intune/apps/app-configuration-policies-outlook#apply-conditional-access)

## <a name="set-up-message-encryption"></a>Configurer le chiffrement des messages

Grâce aux nouvelles fonctionnalités chiffrement de messages Office 365 (OME), qui tirent parti des fonctionnalités de protection dans Azure Information Protection, votre organisation peut facilement partager des e-mails protégés avec tout le monde sur n’importe quel appareil. Les utilisateurs peuvent envoyer et recevoir des messages protégés avec d’autres organisations Microsoft 365 ainsi que des non-clients utilisant Outlook.com, Gmail et d’autres services de messagerie.

Pour plus d’informations, voir [Configurer de chiffrement de messages Office 365 nouvelles fonctionnalités.](../../compliance/set-up-new-message-encryption-capabilities.md)

## <a name="next-steps"></a>Prochaines étapes

![Étape 4 : Stratégies pour Microsoft 365 applications cloud](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

Configurer des stratégies d’accès conditionnel pour :

- [Microsoft Teams](teams-access-policies.md)
- [SharePoint](sharepoint-file-access-policies.md)
