---
title: Utiliser des stratégies de protection contre la perte de données pour les applications cloud non Microsoft
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MET150
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser des stratégies dlp pour les applications cloud non Microsoft.
ms.openlocfilehash: 4bda45a6da6b9626391da37eb9a806b3308c5e7f
ms.sourcegitcommit: b0f464b6300e2977ed51395473a6b2e02b18fc9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53322316"
---
# <a name="use-data-loss-prevention-policies-for-non-microsoft-cloud-apps"></a>Utiliser des stratégies de protection contre la perte de données pour les applications cloud non Microsoft

Les stratégies de protection contre la perte de données (DLP) pour les applications cloud non Microsoft font partie de la suite Microsoft 365 DLP ; À l’aide de ces fonctionnalités, vous pouvez découvrir et protéger les éléments sensibles dans Microsoft 365 services. Pour plus d’informations sur toutes les offres Microsoft DLP, voir [En savoir plus sur la protection contre la perte de données.](dlp-learn-about-dlp.md)

Vous pouvez utiliser des stratégies DLP pour les applications cloud non-Microsoft afin de surveiller et de détecter quand des éléments sensibles sont utilisés et partagés via des applications cloud non Microsoft. L’utilisation de ces stratégies vous donne la visibilité et le contrôle dont vous avez besoin pour vous assurer qu’elles sont correctement utilisées et protégées, et cela permet d’éviter les comportements risqués qui peuvent les compromettre.

## <a name="before-you-begin"></a>Avant de commencer

### <a name="skusubscriptions-licensing"></a>Licences SKU/abonnements

Avant de commencer à utiliser des stratégies DLP pour les applications cloud non Microsoft, confirmez votre abonnement [Microsoft 365 et](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) les modules. Pour accéder à cette fonctionnalité et l’utiliser, vous devez avoir l’un de ces abonnements ou modules:

- Microsoft 365 E5
- Microsoft 365 E5 Conformité
- Microsoft 365 E5 Sécurité

### <a name="permissions"></a>Autorisations
L’utilisateur qui crée la stratégie DLP doit être :
- Administrateur général
- Administrateur de conformité
- Administrateur des données de conformité

### <a name="prepare-your-cloud-app-security-environment"></a>Préparer votre environnement Sécurité des applications cloud de travail

Les stratégies DLP pour les applications cloud non Microsoft utilisent Sécurité des applications cloud fonctionnalités DLP. Pour l’utiliser, vous devez préparer votre environnement Sécurité des applications cloud de travail. Pour obtenir des instructions, voir Définir des actions de visibilité, de protection et de gouvernance [instantanées pour vos applications.](/cloud-app-security/getting-started-with-cloud-app-security#step-1-set-instant-visibility-protection-and-governance-actions-for-your-apps)

### <a name="connect-a-non-microsoft-cloud-app"></a>Connecter application cloud non-Microsoft

Pour utiliser la stratégie DLP sur une application cloud non-Microsoft spécifique, l’application doit être connectée à Sécurité des applications cloud. Pour plus d’informations, voir :

- [Connecter Box](/cloud-app-security/connect-box-to-microsoft-cloud-app-security)
- [Connecter Dropbox](/cloud-app-security/connect-dropbox-to-microsoft-cloud-app-security)
- [Connecter G-Suite](/cloud-app-security/connect-google-apps-to-microsoft-cloud-app-security)
- [Connecter Salesforce](/cloud-app-security/connect-salesforce-to-microsoft-cloud-app-security)
- [Connecter Cisco Webex](/cloud-app-security/connect-webex-to-microsoft-cloud-app-security)

Une fois que vous avez connecté vos applications cloud Sécurité des applications cloud, vous pouvez créer Microsoft 365 stratégies DLP pour elles.

> [!NOTE]
> Il est également possible d’utiliser Microsoft Cloud App Security pour créer des stratégies DLP dans les applications cloud De Microsoft. Toutefois, il est recommandé d’utiliser Microsoft 365 pour créer et gérer des stratégies DLP dans les applications cloud De Microsoft.

## <a name="create-a-dlp-policy-to-a-non-microsoft-cloud-app"></a>Créer une stratégie DLP pour une application cloud non-Microsoft

Lorsque vous sélectionnez un emplacement pour la stratégie DLP, Microsoft Cloud App Security **emplacement.**

- Pour sélectionner une application ou une instance spécifique, **sélectionnez Instance.**
- Si vous ne sélectionnez pas d’instance, la stratégie utilise toutes les applications connectées dans Microsoft Cloud App Security client.

   ![Emplacements pour appliquer la stratégie](../media/1-dlp-non-microsoft-cloud-app-choose-instance.png)

   ![Box-US et Box-General](../media/2-dlp-non-microsoft-cloud-app-box.png)

Vous pouvez choisir différentes actions pour chaque application cloud non-Microsoft prise en charge. Pour chaque application, il existe différentes actions possibles (dépend de l’API de l’application cloud).

![Créer une règle](../media/3-dlp-non-microsoft-cloud-app-create-rule.png)

Lorsque vous créez une règle dans la stratégie DLP, vous pouvez sélectionner une action pour les applications cloud autres que Microsoft. Pour restreindre les applications tierces, **sélectionnez Restreindre les applications tierces.**

![Restreindre les applications tierces](../media/4-dlp-non-microsoft-cloud-app-restrict-third-party-apps.png)

> [!NOTE]
> Les stratégies DLP appliquées aux applications non-Microsoft utilisent Microsoft Cloud App Security. Lorsque la stratégie DLP pour une application non-Microsoft est créée, la même stratégie est automatiquement créée dans Microsoft Cloud App Security.

Pour plus d’informations sur la création et la configuration des stratégies DLP, voir Créer un test et [régler une stratégie DLP.](./create-test-tune-dlp-policy.md)

## <a name="see-also"></a>Voir aussi

- [Créer un test et régler une stratégie DLP](./create-test-tune-dlp-policy.md)
- [Prise en main de la stratégie DLP par défaut](./get-started-with-the-default-dlp-policy.md)
- [Création d’une stratégie DLP à partir d’un modèle](./create-a-dlp-policy-from-a-template.md)
