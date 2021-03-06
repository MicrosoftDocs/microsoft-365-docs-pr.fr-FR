---
title: Prise en main de l’extension de la conformité Microsoft
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Préparez, puis déployez l’extension de la conformité Microsoft.
ms.openlocfilehash: a76a4b1ab5b92a1e237663f65002b99d792b13bb
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53288370"
---
# <a name="get-started-with-microsoft-compliance-extension"></a>Prise en main de l’extension de la conformité Microsoft

Utilisez les procédures ci-après pour déployer l’extension de la conformité Microsoft.

## <a name="before-you-begin"></a>Avant de commencer

Pour utiliser l’extension de la conformité Microsoft, l’appareil doit être intégré à la protection contre la perte de données du point de terminaison. Consultez ces articles si vous êtes novice en matière de DLP ou de DLP des points d'extrémité.

- [En savoir plus sur l’extension de la conformité Microsoft](dlp-chrome-learn-about.md)
- [En savoir plus sur la protection contre la perte de données](dlp-learn-about-dlp.md)
- [Création, test et réglage d’une stratégie DLP](create-test-tune-dlp-policy.md)
- [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
- [Découvrir la protection contre la perte de données de point de terminaison](endpoint-dlp-learn-about.md)
- [Prise en main de la protection contre la perte de données de point de terminaison](endpoint-dlp-getting-started.md)
- [Outils et méthodes d’intégration pour les appareils Windows 10](dlp-configure-endpoints.md)
- [Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison](endpoint-dlp-configure-proxy.md)
- [Utilisation des points de terminaison protection contre la perte de données](endpoint-dlp-using.md)

### <a name="skusubscriptions-licensing"></a>Licences SKU / abonnements

Avant de commencer, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1) et tous les modules complémentaires. Pour accéder à la fonctionnalité de points de terminaison DLP et l’utiliser, vous devez disposer de l’un de ces abonnements ou modules complémentaires.

- Microsoft 365 E5
- Microsoft 365 A5 (EDU)
- Microsoft 365 E5 Conformité
- Microsoft 365 A5 Conformité
- Microsoft 365 E5, Protection des informations et gouvernance
- Microsoft 365 A5, Protection des informations et gouvernance

Pour obtenir des instructions détaillées sur les licences, consultez [instructions relatives aux licences Microsoft 365 pour la sécurité et la conformité](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).

- Votre organisation doit avoir une licence pour la DLP de point de terminaison
- Vos appareils doivent exécuter Windows 10 x64 build 1809 ou version ultérieure.
- La version client Antimalware doit être 4.18.2101.9 ou ultérieure. Vérifiez votre version actuelle à l’aide de l’application **Sécurité Windows**, sélectionnez l’icône **Paramètres**, puis **À propos de**.


### <a name="permissions"></a>Autorisations

Les données du point de terminaison DLP peuvent être affichées dans [l’Explorateur d’activités](data-classification-activity-explorer.md). Il existe sept rôles qui accordent l’autorisation à l’Explorateur d’activités, le compte que vous utilisez pour accéder aux données doit être membre de l’un d’eux.

- Administrateur global
- Administrateur de mise en conformité
- Administrateur de la sécurité
- Administrateur des données de mise en conformité
- Lecteur général
- Lecteur Sécurité
- Lecteur de rapports

### <a name="overall-installation-workflow"></a>Flux de travail d’installation global

Le déploiement de l’extension de la conformité Microsoft est un processus en plusieurs phases. Vous pouvez choisir de l'installer sur un ordinateur à la fois, ou d'utiliser Microsoft Endpoint Manager ou stratégie de groupe pour les déploiements à l'échelle de l'organisation.

1. [Préparez vos appareils](#prepare-your-devices).
2. [Configuration de base ordinateur simple Selfhost](#basic-setup-single-machine-selfhost)
3. [Déployer à l'aide de Microsoft Endpoint Manager](#deploy-using-microsoft-endpoint-manager)
4. [Déployer à l’aide d’une stratégie de groupe](#deploy-using-group-policy)
5. [Tester l’extension](#test-the-extension)
6. [Utiliser le tableau de bord de gestion des alertes pour afficher les alertes DLP dans Chrome](#use-the-alerts-management-dashboard-to-viewing-chrome-dlp-alerts)
7. [Affichage de données DLP dans l’Explorateur d’activités](#viewing-chrome-dlp-data-in-activity-explorer)

### <a name="prepare-infrastructure"></a>Préparation de l'infrastructure

Si vous déployez l'extension de conformité Microsoft sur tous vos appareils Windows 10 contrôlés, vous devez supprimer Google Chrome des listes des applications et des navigateurs non autorisés. Pour plus d'informations, voir [Navigateurs non autorisés ](endpoint-dlp-using.md#unallowed-browsers). Si vous ne le déployez que sur quelques appareils, vous pouvez laisser Chrome sur la liste des navigateurs non autorisés ou des applications non autorisées. L'extension de conformité Microsoft contournera les restrictions des deux listes pour les ordinateurs sur lesquels elle est installée.

### <a name="prepare-your-devices"></a>Préparer vos appareils

1. Utilisez les procédures de ces rubriques pour intégrer vos appareils :
    1. [Prise en main de la protection contre la perte de données de point de terminaison](endpoint-dlp-getting-started.md)
    1. [Outils et méthodes d’intégration pour les appareils Windows 10](dlp-configure-endpoints.md)
    1. [Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison](endpoint-dlp-configure-proxy.md)

### <a name="basic-setup-single-machine-selfhost"></a>Configuration de base ordinateur simple Selfhost

Il s'agit de la méthode recommandée.

1. Connectez-vous à l'ordinateur Windows 10 sur lequel vous souhaitez installer l'extension de conformité Microsoft, puis exécutez ce script PowerShell en tant qu'administrateur.

   ```powershell
   Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
   ```

2. Accédez à [Extension de la conformité Microsoft : Chrome Web Store (google.com)](https://chrome.google.com/webstore/detail/microsoft-compliance-exte/echcggldkblhodogklpincgchnpgcdco).

3. Installez l’extension à l’aide des instructions de la page Chrome Web Store.

### <a name="deploy-using-microsoft-endpoint-manager"></a>Déployez à l'aide de Microsoft Endpoint Configuration Manager

Utilisez cette méthode de configuration pour les déploiements à l'échelle de l'entreprise.

##### <a name="enabling-required-registry-key-via-microsoft-endpoint-manager"></a>Activation de la clé de Registre requise via Microsoft Endpoint Manager

1. Créez un script PowerShell avec le contenu suivant :

    ```powershell
    Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
    ```

2. Connectez-vous au [Centre d’administration Microsoft Endpoint Manager](https://endpoint.microsoft.com).

3. Accédez à **Appareils** > **Scripts** puis sélectionnez **Ajouter**.

4. Accédez à l’emplacement du script créé lorsque vous y avez été invité.

5. Sélectionnez les paramètres suivants :
    1. Exécuter ce script à l’aide des informations d’identification connectées : OUI
    1. Appliquer la vérification de la signature de script : NON
    1. Exécuter un script dans l’hôte PowerShell 64 bits : OUI

6. Sélectionnez les groupes d’appareils appropriés et appliquez la stratégie.

#### <a name="microsoft-endpoint-manager-force-install-steps"></a>Étapes de l'installation forcée de Microsoft Endpoint Manager

Avant d'ajouter l'extension de la conformité Microsoft à la liste des extensions installées de force, il est important d'ingérer l'ADMX de Chrome. Les étapes de ce processus dans Microsoft Endpoint Manager sont documentées par Google : [Gérer le navigateur Chrome avec Microsoft Intune - Aide de Google Chrome Enterprise](https://support.google.com/chrome/a/answer/9102677?hl=en#zippy=%2Cstep-ingest-the-chrome-admx-file-into-intune).

 Après avoir ingéré l’ADMX, vous pouvez suivre les étapes ci-dessous pour créer un profil de configuration pour cette extension.

1. Connectez-vous au centre d'administration de la gestion des points de terminaison Microsoft ( https://endpoint.microsoft.com).

2. Accédez aux profils de configuration.

3. Sélectionnez **Créer le profil**.

4. Sélectionnez **Windows 10** en tant que plateforme.

5. Sélectionnez **Personnaliser** en tant que type de profil.

6. Sélectionnez l’onglet **Paramètres**.

7. Sélectionnez **Ajouter**.

8. Entrez les informations de stratégie suivantes.

    OMA-URI : `./Device/Vendor/MSFT/Policy/Config/Chrome~Policy~googlechrome~Extensions/ExtensionInstallForcelist`<br/>
    Type de données`String`<br/>
    Valeur : `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000; echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx"/>`

9. Cliquez sur Créer.

### <a name="deploy-using-group-policy"></a>Déployer à l’aide d’une stratégie de groupe

Si vous ne voulez pas utiliser Microsoft Endpoint Manager, vous pouvez utiliser des stratégies de groupe pour déployer l’extension de la conformité Microsoft au sein de votre organisation

1. Vos appareils doivent être gérables via une stratégie de groupe, et vous devez importer tous les ADMX Chrome dans le Store central de stratégies de groupe. Pour plus d’informations, reportez-vous à l’article [Comment créer et gérer le magasin central des modèles d’administration de stratégie de groupe dans Windows](/troubleshoot/windows-client/group-policy/create-and-manage-central-store).

2. Créez un script PowerShell en utilisant cette commande PowerShell :

    ```powershell
    Get-Item -path "HKLM:\SOFTWARE\Microsoft\Windows Defender\Miscellaneous Configuration" | New-ItemProperty -Name DlpDisableBrowserCache -Value 0 -Force
    ```

3. Ouvrez la **Console de gestion des stratégies de groupe** et accédez à votre unité d’organisation.

4. Cliquez avec le bouton droit et sélectionnez **Créer un GPO dans ce domaine et lier ici**. Lorsque vous y êtes invité, attribuez un nom descriptif à cet objet de stratégie de groupe (GPO) et terminez sa création.

5. Cliquez avec le bouton droit sur le GPO, puis sélectionnez **Modifier**.

6. Accédez à **Configuration de l'ordinateur** > **Préférences** > **Panneau de configuration Paramètres** > **Tâches planifiées**.

7. Créez une tâche immédiate en faisant un clic droit et en sélectionnant **Nouveau** > **Tâche immédiate (au moins Windows 7)**.

8. Donnez un nom et une description à la tâche.

9. Sélectionnez le compte correspondant pour exécuter la tâche immédiate (par exemple, NT Authority).

10. Sélectionnez **Exécuter avec les autorisations maximales**.

11. Configurez la stratégie pour Windows 10.

12. Dans l’onglet **Actions** , sélectionnez l’action **Démarrer un programme**.

13. Entrez le chemin d’accès au programme/script créé à l’étape 1.

14. Sélectionnez **Appliquer**.

#### <a name="adding-the-chrome-extension-to-the-forceinstall-list"></a>Ajout de l'extension Chrome à la liste de ForceInstall

1. Dans l’Éditeur de gestion des stratégies de groupe, accédez à votre OU.

2. Développez le chemin d’accès suivant **Configuration ordinateur/utilisateur** > **Stratégies d’administration** > **Modèles d’administration** > **Modèles d’administration classiques** > **Google** > **Google Chrome** > **Extensions**. Ce chemin d’accès peut varier en fonction de votre configuration.

3. Sélectionnez **Configurer la liste des extensions installées avec force**.

4. Cliquez avec le bouton droit et sélectionnez **Modifier**.

5. Sélectionnez **Activé**.

6. Sélectionnez **Afficher**.

7. Sous **Valeur**, ajoutez l’entrée suivante : `echcggldkblhodogklpincgchnpgcdco;https://clients2.google.com/service/update2/crx`

8. Sélectionnez **OK**, puis **Appliquer**.

### <a name="test-the-extension"></a>Tester l’extension

#### <a name="upload-to-cloud-service-or-access-by-unallowed-browsers-cloud-egress"></a>Chargement vers un service en ligne, ou accès par des navigateurs non autorisés sortie du cloud

1. Créez ou obtenez un élément sensible, puis essayez de télécharger un fichier vers l’un des domaines de service restreints de votre organisation. Les données sensibles doivent correspondre à l'un de nos [Types d'informations sensibles intégrés](sensitive-information-type-entity-definitions.md), ou à l'un des types d'informations sensibles de votre organisation. Vous devriez recevoir une notification de toast DLP sur l'appareil à partir duquel vous effectuez le test, indiquant que cette action n'est pas autorisée lorsque le fichier est ouvert.

#### <a name="testing-other-dlp-scenarios-in-chrome"></a>Tests d’autres scénarios DLP dans Chrome

Maintenant que vous avez supprimé Chrome de la liste des navigateurs/applications interdits, vous pouvez tester les scénarios ci-dessous pour vérifier que le comportement répond aux exigences de votre organisation :

- Copier des données d’un élément sensible vers un autre document à l’aide du Presse-papiers
  - Pour tester, ouvrez un fichier protégé contre les actions de copie vers le presse-papiers dans le navigateur Chrome et essayez de copier les données du fichier.
  - Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.
- Imprimer un document
  - Pour tester, ouvrez un fichier protégé contre les actions d’impression dans le navigateur Chrome et essayez d’imprimer le fichier.
  - Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.
- Copier sur un support amovible USB
  - Pour le tester, essayez d'enregistrer le fichier sur un support de stockage amovible.
  - Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.
- Copier vers le partage réseau
  - Pour tester, essayez d’enregistrer le fichier sur un partage réseau.
  - Résultat attendu : notification toast DLP indiquant que cette action n’est pas autorisée lorsque le fichier est ouvert.

### <a name="use-the-alerts-management-dashboard-to-viewing-chrome-dlp-alerts"></a>Utiliser le tableau de bord de gestion des alertes pour afficher les alertes DLP dans Chrome

1. Ouvrez la page **Protection contre la perte de données** dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com), puis sélectionnez **Alertes**.

2. Reportez-vous aux procédures décrites dans [Comment configurer et afficher les alertes pour les stratégies DLP](dlp-configure-view-alerts-policies.md) pour afficher les alertes relatives à vos stratégies DLP de point de terminaison.

### <a name="viewing-chrome-dlp-data-in-activity-explorer"></a>Affichage de données DLP dans l’Explorateur d’activités

1. Ouvrez la [Page classification des données](https://compliance.microsoft.com/dataclassification?viewid=overview) pour votre domaine dans le centre de conformité Microsoft 365, puis sélectionnez **Explorateur d’activités**.

2. Reportez-vous aux procédures décrites dans [Prise en main de l’Explorateur d’activités](data-classification-activity-explorer.md) pour accéder aux données de vos appareils de point de terminaison et les filtrer.

   > [!div class="mx-imgBorder"]
   > ![filtre de l’Explorateur d’activités pour les appareils de point de terminaison](../media/endpoint-dlp-4-getting-started-activity-explorer.png)

### <a name="known-issues-and-limitations"></a>Problèmes et limites connus

1. L'application du Block Override pour la sortie du nuage n'est pas prise en charge.
2. Le mode Incognito n'est pas pris en charge et doit être désactivé.

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous disposez d’appareils intégrés et que vous pouvez afficher les données d’activité dans l’Explorateur d’activités, vous êtes prêt à passer à l’étape suivante dans laquelle vous créez des stratégies DLP qui protègent vos éléments sensibles.

- [Utilisation des points de terminaison protection contre la perte de données](endpoint-dlp-using.md)

## <a name="see-also"></a>Voir aussi

- [Découvrir la protection contre la perte de données de point de terminaison](endpoint-dlp-learn-about.md)
- [Utilisation de la prévention des pertes de données sur les points de terminaison](endpoint-dlp-using.md)
- [En savoir plus sur la prévention des pertes de données](dlp-learn-about-dlp.md)
- [Création, test et réglage d’une stratégie DLP](create-test-tune-dlp-policy.md)
- [Prise en main de l’explorateur d’activités](data-classification-activity-explorer.md)
- [Microsoft Defender pour point de terminaison](/windows/security/threat-protection/)
- [Outils et méthodes d’intégration pour les appareils Windows 10](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).
- [Abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [Azure AD appareils joints](/azure/active-directory/devices/concept-azure-ad-join)
- [Télécharger le nouveau Microsoft Edge sur la base de chrome](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)
