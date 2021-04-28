---
title: Signaler les faux positifs et les faux négatifs dans Outlook
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Découvrez comment signaler les faux positifs et les faux négatifs dans Outlook et activer les modules de signalement des messages et du signalement du hameçonnage.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 38f940a98581c5678eef0c57c95f6349cdb41de8
ms.sourcegitcommit: ddb1bf56bcba4f03c803f79492e8cd0dc41a3d7a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "52065177"
---
# <a name="report-false-positives-and-false-negatives-in-outlook"></a>Signaler les faux positifs et les faux négatifs dans Outlook

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

**S’applique à**
- [Exchange Online Protection](exchange-online-protection-overview.md)
- [Microsoft Defender pour Office 365 : offre 1 et offre 2](defender-for-office-365.md)
- [Microsoft 365 Defender](../defender/microsoft-365-defender.md)

> [!NOTE]
> Si vous êtes un administrateur d'une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d'utiliser le portail Soumissions dans le Centre de sécurité & conformité. Pour plus d'informations, voir Utiliser la soumission d'administrateur pour soumettre des messages suspects de courrier indésirable, d'hameçonnage, d'URL et [de fichiers à Microsoft.](admin-submission.md)

Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou locales utilisant l'authentification moderne hybride, vous pouvez envoyer des faux positifs (messages électroniques de qualité marqués comme courrier indésirable) et des faux négatifs (courrier électronique et hameçonnage autorisés) à Exchange Online Protection (EOP).

## <a name="things-to-remember-before-you-use-the-report-message-feature"></a>Éléments à retenir avant d'utiliser la fonctionnalité Signaler un message

- Pour une meilleure expérience de soumission d'utilisateurs, utilisez le add-in Report Message ou report Phishing.

- Notez que ce add-in fonctionne pour Outlook sur toutes les plateformes , sur le web, iOS, Android et Bureau.

- Si vous êtes un administrateur d'une organisation ayant des boîtes aux lettres Exchange Online, utilisez le portail Soumissions dans le Centre de sécurité & conformité. Pour plus d'informations, voir Utiliser la soumission d'administrateur pour soumettre des messages suspects de courrier indésirable, d'hameçonnage, d'URL et [de fichiers à Microsoft.](admin-submission.md)

- Vous pouvez configurer pour envoyer des messages directement à Microsoft, une boîte aux lettres que vous spécifiez, ou les deux. Pour plus d'informations, voir [Stratégies d'envoi des utilisateurs.](user-submission.md)

- Pour plus d'informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)

## <a name="use-the-report-message-feature"></a>Utiliser la fonctionnalité Message de rapport

### <a name="report-junk-and-phishing-messages"></a>Signaler les messages de courrier indésirable et de hameçonnage

Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l'exception du courrier indésirable, utilisez la méthode suivante pour signaler le courrier indésirable et les messages de hameçonnage :

1. Cliquez sur les **ellipses** Autres actions dans le coin supérieur droit du message sélectionné,  cliquez sur Signaler **le message** dans le menu déroulant, puis sélectionnez Courrier indésirable ou **Hameçonnage.**
  
   > [!div class="mx-imgBorder"]
   > ![Message de rapport - Plus d'actions](../../media/report-message-more-actions.png)

   > [!div class="mx-imgBorder"]
   > ![Message de rapport : courrier indésirable et hameçonnage](../../media/report-message-junk-phishing.png)

2. Les messages sélectionnés sont envoyés à Microsoft pour analyse et :

   - Déplacé vers le dossier Courrier indésirable s'il a été signalé comme courrier indésirable.

   - Supprimé s'il a été signalé comme hameçonnage.
   
### <a name="report-messages-that-are-not-junk"></a>Signaler les messages qui ne sont pas indésirables

1. Cliquez sur les ellipses Autres **actions** dans le coin supérieur droit du message sélectionné, cliquez sur Signaler **le message** dans le menu déroulant, puis cliquez sur Non indésirable **.**  

   > [!div class="mx-imgBorder"]
   > ![Message de rapport - Plus d'actions](../../media/report-message-more-actions.png)

   > [!div class="mx-imgBorder"]
   > ![Message de rapport - Courrier non indésirable](../../media/report-message-not-junk.png)

2. Le message sélectionné est envoyé à Microsoft pour analyse et déplacé vers la boîte de réception ou tout autre dossier spécifié.

## <a name="enable-the-report-message-and-report-phishing-add-ins"></a>Activer les add-ins Signaler le message et Signaler le hameçonnage

Les add-ins Signaler le message et Signaler le hameçonnage pour Outlook et Outlook sur le web (anciennement Outlook Web App) permettent aux utilisateurs de signaler facilement les faux positifs (messages électroniques de qualité marqués comme faux) ou les faux négatifs (courrier électronique non autorisé) à Microsoft et à ses affiliés pour analyse. 

Microsoft utilise ces soumissions pour améliorer l'efficacité des technologies de protection de la messagerie. Par exemple, supposons que des personnes signalent de nombreux messages à l'aide du module de signalement du hameçonnage. Ces informations sont disponibles dans le Tableau de bord de sécurité et d'autres rapports. L'équipe de sécurité de votre organisation peut utiliser ces informations pour indiquer que les stratégies anti-hameçonnage peuvent avoir besoin d'être mises à jour. 

Vous pouvez installer le module de rapport de message ou de signalement du hameçonnage. Si vous souhaitez que vos utilisateurs signalent à la fois le courrier indésirable et les messages de hameçonnage, déployez le add-in Signaler un message dans votre organisation. Pour plus d'informations, voir Activer le add-in Message de rapport. 

Le add-in Report Message offre la possibilité de signaler les messages de courrier indésirable et de hameçonnage. Les administrateurs peuvent activer le add-in Message de rapport pour l'organisation, et les utilisateurs individuels peuvent l'installer eux-mêmes. 

Le module de signalement du hameçonnage offre la possibilité de signaler uniquement les messages de hameçonnage. Les administrateurs peuvent activer le module de signalement du hameçonnage pour l'organisation, et les utilisateurs individuels peuvent l'installer eux-mêmes. 

Si vous êtes un utilisateur individuel, vous pouvez activer les deux modules pour vous-même.

Si vous êtes un administrateur général ou un administrateur Exchange Online, et qu'Exchange est configuré pour utiliser l'authentification OAuth, vous pouvez activer le add-in Message de rapport et le module de signalement du hameçonnage pour votre organisation. Les deux modules sont désormais disponibles via [le déploiement centralisé.](../../admin/manage/centralized-deployment-of-add-ins.md)

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu’il faut savoir avant de commencer

- Le add-in Report Message et le add-in Report Phishing fonctionnent avec la plupart des abonnements Microsoft 365 et les produits suivants :

  - Outlook sur le web
  - Outlook 2013 SP1 ou une édition ultérieure
  - Outlook 2016 pour Mac
  - Outlook inclus dans les applications Microsoft 365 pour Entreprise
  - Application Outlook pour iOS et Android

- Les deux modules ne sont pas disponibles pour les boîtes aux lettres partagées ou les boîtes aux lettres dans les organisations Exchange locales.

- Votre navigateur web existant doit fonctionner à la fois avec les modules de rapport de message et de signalement du hameçonnage. Toutefois, si vous remarquez que le module n'est pas disponible ou ne fonctionne pas comme prévu, essayez un autre navigateur.

- Pour les installation organisationnelles, l'organisation doit être configurée pour utiliser l'authentification OAuth. Pour plus d'informations, [voir Determine if Centralized Deployment of add-ins works for your organization.](../../admin/manage/centralized-deployment-of-add-ins.md)

- Les administrateurs doivent être membres du groupe de rôles Administrateurs globaux. Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).

## <a name="get-the-report-message-add-in"></a>Obtenir le add-in Message de rapport

### <a name="get-the-add-in-for-yourself"></a>Obtenir le add-in pour vous-même

1. Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Message add-in. To go directly to the Report Message add-in, go to <https://appsource.microsoft.com/product/office/wa104381180> .

2. Cliquez **sur GET IT NOW**.

   ![Message de rapport : l'obtenir maintenant](../../media/ReportMessageGETITNOW.png)

3. Dans la boîte de dialogue qui s'affiche, examinez les conditions d'utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.

4. Connectez-vous à l'aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).

Une fois le add-in installé et activé, les icônes suivantes s'offrent à vous :

- Dans Outlook, l'icône ressemble à ceci :

  > [!div class="mx-imgBorder"]
  > ![Icône signaler le add-in Message pour Outlook](../../media/OutlookReportMessageIcon.png)

- Dans Outlook sur le web, l'icône ressemble à ceci :

  > [!div class="mx-imgBorder"]
  > ![Icône du add-in Message de rapport Outlook sur le web](../../media/owa-report-message-icon.png)

### <a name="get-the-add-in-for-your-organization"></a>Obtenir le add-in pour votre organisation

> [!NOTE]
> L'apparition du module dans votre organisation peut prendre jusqu'à 12 heures.

1. In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> . Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**

2. Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.

   ![Page Services et modules dans le Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. Dans le **volant Déployer un** nouveau module complémentaire qui s'affiche, examinez les informations, puis cliquez sur **Suivant**.

4. Sur la page suivante, cliquez sur **Choisir dans le Store.**

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. Dans la page **Sélectionner un add-in** qui s'affiche, cliquez dans la zone De recherche, entrez Message de rapport, puis cliquez sur **Icône**   ![ ](../../media/search-icon.png) Rechercher. Dans la liste des résultats, recherchez **Message de rapport,** puis cliquez sur **Ajouter.**

   ![Sélectionner des résultats de recherche de add-in](../../media/NewAddInScreen3.png)

6. Dans la boîte de dialogue qui s'affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.

7. Dans la page **Configurer le add-in** qui s'affiche, configurez les paramètres suivants :

   - **Utilisateurs affectés**: sélectionnez l'une des valeurs suivantes :

     - **Tout le monde** (par défaut)
     - **Utilisateurs/groupes spécifiques**
     - **Juste moi**

   - **Méthode de déploiement**: sélectionnez l'une des valeurs suivantes :

     - **Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.
     - **Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.
     - **Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.

   ![Configurer la page de l'ajout](../../media/configure-add-in.png)

   Lorsque vous avez terminé, cliquez sur **Déployer.**

8. Dans la page Déployer le **message** de rapport qui s'affiche, vous verrez un rapport d'avancement suivi d'une confirmation du déploiement du module. Après avoir lu les informations, cliquez sur **Suivant**.

   ![Page Déployer le message de rapport](../../media/deploy-report-message-page.png)

9. Dans la page **Annoncer le add-in** qui s'affiche, examinez les informations, puis cliquez sur **Fermer**.

   ![Page d'annonce du add-in](../../media/announce-add-in-page.png)

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a>Passer en revue ou modifier les paramètres du add-in Message de rapport

1. In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> . Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**

   ![Page Services et Add-Ins dans le nouveau Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

2. Recherchez et sélectionnez le add-in **Message** de rapport.

3. Dans le **volant Modifier le message** de rapport qui s'affiche, examinez et modifiez les paramètres selon le cas pour votre organisation. Lorsque vous avez terminé, cliquez sur **Enregistrer**.

   ![Paramètres du add-in Message de rapport](../../media/EditReportMessageAddIn.png)

## <a name="get-the-report-phishing-add-in"></a>Obtenir le module de signalement du hameçonnage

### <a name="get-the-add-in-for-yourself"></a>Obtenir le add-in pour vous-même

1. Go to the Microsoft AppSource at <https://appsource.microsoft.com/marketplace/apps> and search for the Report Phishing add-in.

2. Cliquez **sur GET IT NOW**.

3. Dans la boîte de dialogue qui s'affiche, examinez les conditions d'utilisation et la politique de confidentialité, puis cliquez sur **Continuer**.

4. Connectez-vous à l'aide de votre compte scolaire ou scolaire (pour une utilisation professionnelle) ou de votre compte Microsoft (pour un usage personnel).

Une fois le add-in installé et activé, les icônes suivantes s'offrent à vous :

- Dans Outlook, l'icône ressemble à ceci :

  ![Icône Signaler le hameçonnage d'un add-in pour Outlook](../../media/Outlook-ReportPhishing.png)

- Dans Outlook sur le web, l'icône ressemble à ceci :

  > [!div class="mx-imgBorder"]
  > ![Icône de l'application De hameçonnage de rapport Outlook sur le web](../../media/OWA-ReportPhishing.png)

### <a name="get-the-add-in-for-your-organization"></a>Obtenir le add-in pour votre organisation

> [!NOTE]
> L'apparition du module dans votre organisation peut prendre jusqu'à 12 heures.

1. In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> . Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**

2. Sélectionnez **Déployer le add-in** en haut de la page, puis sélectionnez **Suivant**.

   ![Page Services et modules dans le Centre d'administration Microsoft 365](../../media/ServicesAddInsPageNewM365AdminCenter.png)

3. Dans le **volant Déployer un** nouveau module complémentaire qui s'affiche, examinez les informations, puis cliquez sur **Suivant**.

4. Sur la page suivante, cliquez sur **Choisir dans le Store.**

   ![Déployer une nouvelle page de modules](../../media/NewAddInScreen2.png)

5. Dans la page Sélectionner **un add-in** qui s'affiche, cliquez dans  la zone De recherche, entrez **Hameçonnage** de rapport, puis cliquez sur Icône  ![ ](../../media/search-icon.png) Recherche. Dans la liste des résultats, recherchez **l'hameçonnage** de rapport, puis cliquez sur **Ajouter.**

6. Dans la boîte de dialogue qui s'affiche, examinez les informations de licence et de confidentialité, puis cliquez sur **Continuer**.

7. Dans la page **Configurer le add-in** qui s'affiche, configurez les paramètres suivants :

   - **Utilisateurs affectés**: sélectionnez l'une des valeurs suivantes :

     - **Tout le monde** (par défaut)
     - **Utilisateurs/groupes spécifiques**
     - **Juste moi**

   - **Méthode de déploiement**: sélectionnez l'une des valeurs suivantes :

     - **Fixe (par défaut)**: le add-in est automatiquement déployé sur les utilisateurs spécifiés et ils ne peuvent pas le supprimer.
     - **Disponible**: les utilisateurs peuvent installer le add-in sur **home** \> **get add-ins** \> **admin-managed**.
     - **Facultatif**: le add-in est automatiquement déployé pour les utilisateurs spécifiés, mais ils peuvent choisir de le supprimer.

   Lorsque vous avez terminé, cliquez sur **Déployer.**

8. Dans la page **Déployer** le hameçonnage de rapport qui s'affiche, vous verrez un rapport d'avancement suivi d'une confirmation du déploiement du module. Après avoir lu les informations, cliquez sur **Suivant**.

9. Dans la page **Annoncer le add-in** qui s'affiche, examinez les informations, puis cliquez sur **Fermer**.

## <a name="review-or-edit-settings-for-the-report-phishing-add-in"></a>Examiner ou modifier les paramètres du module de signalement du hameçonnage

1. In the Microsoft 365 admin center, go to the go to the **Settings** \> **Add-ins** page at <https://admin.microsoft.com/AdminPortal/Home#/Settings/AddIns> . Si la **page** Des applications intégrées aux **paramètres** n'est pas consultez, rendez-vous sur le lien Applications \>  \> **intégrées paramètres** en haut de la page **Applications intégrées.**

2. Recherchez et sélectionnez **le** module de signalement du hameçonnage.

3. Dans le flyout **Modifier le hameçonnage** du rapport qui s'affiche, examinez et modifiez les paramètres selon le cas pour votre organisation. Lorsque vous avez terminé, cliquez sur **Enregistrer**.

## <a name="view-and-review-reported-messages"></a>Afficher et examiner les messages signalés

Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :

- Utilisez le portail Soumissions d'administrateur. Pour plus d'informations, voir [Afficher les soumissions d'utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)

- Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés. Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)