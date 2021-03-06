---
title: Activer le module de signalement du hameçonnage
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Découvrez comment activer le module de signalement du hameçonnage pour Outlook et Outlook sur le web, pour des utilisateurs individuels ou pour l’ensemble de votre organisation.
ms.openlocfilehash: 44113237274d37aabeda954354182fe4da5aa970
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53083415"
---
# <a name="enable-the-report-phishing-add-in"></a>Activez le complément Signaler un message de hameçonnage

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


> [!NOTE]
> Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le portail Microsoft 365 Defender. Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)

Les modules de signalement des messages et du hameçonnage pour Outlook et Outlook sur le web (anciennement appelés Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courriers électroniques erronés autorisés) à Microsoft et à ses affiliés pour analyse.

Microsoft utilise ces soumissions pour améliorer l’efficacité des technologies de protection de la messagerie. Par exemple, supposons que des personnes signalent de nombreux messages à l’aide du module de signalement du hameçonnage. Ces informations sont disponibles dans le Tableau [de bord de](security-dashboard.md) sécurité et d’autres rapports. L’équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d’être mises à jour.

Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage. Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation. Pour plus d’informations, [voir Activer le add-in Message de rapport.](enable-the-report-message-add-in.md)

Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage. Les administrateurs peuvent activer le module de signalement du hameçonnage pour l’organisation, et les utilisateurs individuels peuvent l’installer eux-mêmes.

Si vous êtes un utilisateur individuel, vous pouvez activer le module de signalement du hameçonnage [pour vous-même.](#get-the-report-phishing-add-in-for-yourself)

Si vous êtes administrateur général ou administrateur Exchange Online et que Exchange est configuré pour utiliser l’authentification OAuth, vous pouvez activer le module de signalement du hameçonnage pour votre [organisation.](#get-and-enable-the-report-phishing-add-in-for-your-organization) Le rapport d’hameçonnage Add-In est désormais disponible via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Le module de signalement du hameçonnage fonctionne avec la plupart Microsoft 365 abonnements et les produits suivants :

  - Outlook sur le web
  - Outlook 2013 SP1 ou une ultérieure
  - Outlook 2016 pour Mac ou ultérieure
  - Outlook incluses dans Microsoft 365 applications pour Enterprise
  - Outlook application pour iOS et Android

- Le module de signalement du hameçonnage n’est pas disponible pour les boîtes aux lettres partagées ou les boîtes aux lettres dans les organisations Exchange locales.

- Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez. Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)

- Votre navigateur web existant doit fonctionner avec le module de signalement du hameçonnage. Toutefois, si vous remarquez que le module n’est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.

- Pour les installation organisationnelles, l’organisation doit être configurée pour utiliser l’authentification OAuth. Pour plus d’informations, [voir Determine if Centralized Deployment of add-ins works for your organization](../../admin/manage/centralized-deployment-of-add-ins.md).

- Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux. Pour plus d’informations, consultez [Autorisations dans le portail Microsoft 365 Defender](permissions-microsoft-365-security-center.md).

## <a name="get-the-report-phishing-add-in-for-yourself"></a>Obtenir le module de signalement du hameçonnage par vous-même

1. Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.

2. Cliquez **sur GET IT NOW**.

3. Dans la boîte de dialogue qui s’affiche, examinez les conditions d’utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.

4. Connectez-vous à l’aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).

Une fois que le module est installé et activé, les icônes suivantes s’offrent à vous :

- Dans Outlook, l’icône ressemble à ceci :

  ![Icône signaler le hameçonnage d’un Outlook](../../media/Outlook-ReportPhishing.png)

- Dans Outlook sur le web, l’icône ressemble à ceci :

  ![Outlook sur le web Icône Signaler le hameçonnage du add-in](../../media/OWA-ReportPhishing.png)

## <a name="get-and-enable-the-report-phishing-add-in-for-your-organization"></a>Obtenir et activer le module de signalement du hameçonnage pour votre organisation

> [!NOTE]
> L’apparition du module dans votre organisation peut prendre jusqu’à 12 heures.

1. Dans la Centre d’administration Microsoft 365, rendez-vous sur la page Des applications **Paramètres** à l’Paramètres Si la page des applications \> **intégrées** n’est pas consultez, consultez le lien Applications <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées **Paramètres**  en haut de la page Applications \>  \> **intégrées.** 

2. Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.

   ![Page Services et add-ins dans la Centre d’administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. Dans le **volant Déployer un** nouveau module complémentaire qui s’affiche, examinez les informations, puis cliquez sur **Suivant**.

4. Sur la page suivante, cliquez sur **Choisir dans le Store.**

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. Dans la page Sélectionner **un add-in** qui s’affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche. Dans la liste des résultats, recherchez **l’hameçonnage** de rapport, puis cliquez sur **Ajouter.**

6. Dans la boîte de dialogue qui s’affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.

7. Dans la page **Configurer le module de** configuration qui s’affiche, configurez les paramètres suivants :

   - **Utilisateurs affectés**: sélectionnez l’une des valeurs suivantes :

     - **Tout le monde** (par défaut)
     - **Utilisateurs/groupes spécifiques**
     - **Juste moi**

   - **Méthode de déploiement**: sélectionnez l’une des valeurs suivantes :

     - **Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.
     - **Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.
     - **Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.

   Lorsque vous avez terminé, cliquez sur **Déployer.**

8. Dans la page **Déployer** le hameçonnage de rapport qui s’affiche, vous verrez un rapport d’avancement suivi d’une confirmation du déploiement du module. Après avoir lu les informations, cliquez sur **Suivant**.

9. Dans la page **Annoncer le add-in** qui s’affiche, examinez les informations, puis cliquez sur **Fermer**.

## <a name="learn-how-to-use-the-report-phishing-add-in"></a>Découvrez comment utiliser le module de signalement du hameçonnage

Les personnes à qui le add-in est affecté voient les icônes suivantes :

- Dans Outlook, l’icône ressemble à ceci :

  ![Icône signaler le hameçonnage d’un Outlook](../../media/Outlook-ReportPhishing.png)

- Dans Outlook sur le web, l’icône ressemble à ceci :

  ![Outlook sur l’icône du module de hameçonnage de rapport web](../../media/OWA-ReportPhishing.png)

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a>Examiner ou modifier les paramètres du module de signalement du hameçonnage

1. Dans la Centre d’administration Microsoft 365, rendez-vous sur la page Des applications **Paramètres** à l’Paramètres Si la page des applications \> **intégrées** n’est pas consultez, consultez le lien Applications <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> intégrées **Paramètres**  en haut de la page Applications \>  \> **intégrées.** 

2. Recherchez et sélectionnez **le** module de signalement du hameçonnage.

3. Dans le flyout **Modifier le hameçonnage** du rapport qui s’affiche, examinez et modifiez les paramètres selon le cas pour votre organisation. Lorsque vous avez terminé, cliquez sur **Enregistrer**.

## <a name="view-and-review-reported-messages"></a>Afficher et examiner les messages signalés

Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :

- Utilisez le portail Soumissions d’administrateur. Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)

- Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés. Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir [quels utilisateurs font des rapports à Microsoft.](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-see-what-users-are-reporting-to-microsoft)
