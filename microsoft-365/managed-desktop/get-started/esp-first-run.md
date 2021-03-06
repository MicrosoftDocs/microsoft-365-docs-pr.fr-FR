---
title: Expérience de première exécution avec le pilote automatique et la page état d’inscription
description: Comment déployer l’expérience ESP, les paramètres utilisés et les modifications de configuration
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: b65ad2a6ac1a9b9abe06cc108a980be21152bc86
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844957"
---
# <a name="first-run-experience-with-autopilot-and-the-enrollment-status-page"></a>Expérience de première exécution avec le pilote automatique et la page état d’inscription

Bureau géré Microsoft utilise à la fois [Windows Autopilot](/windows/deployment/windows-autopilot/windows-autopilot) et la page d’état d’inscription de Microsoft Intune [(ESP)](/windows/deployment/windows-autopilot/enrollment-status) pour offrir la meilleure expérience de première utilisation possible à vos utilisateurs.

La page État de l’inscription est actuellement en prévisualisation publique.

## <a name="initial-deployment"></a>Déploiement initial

Pour fournir l’expérience ESP, vous devez inscrire des appareils dans le service Bureau géré Microsoft service. Pour plus d’informations sur l’inscription, voir [Inscrire de nouveaux appareils vous-même](../get-started/register-devices-self.md) ou [Étapes pour que les partenaires inscrivent des appareils.](../get-started/register-devices-partner.md)

Une fois que vos appareils sont inscrits auprès du service, vous pouvez activer ESP pour vos appareils Bureau géré Microsoft en classant un ticket de support via le portail [d’administration.](https://portal.azure.com/) Nous allons initialement déployer la configuration ESP dans le groupe test lorsque vous déposez le ticket. Il est déployé dans les autres groupes de déploiement suivants (First, Fast et Broad) toutes les 24 heures. Pour suspendre le déploiement, déposez un autre ticket demandant aux opérations de se tenir en attente.

## <a name="autopilot-profile-settings"></a>Paramètres de profil Autopilot

Bureau géré Microsoft utilise ces paramètres dans le profil Autopilot utilisé pour les appareils de vos utilisateurs :

<br>

****

|Paramètre|Valeur|
|---|---|
|Mode de déploiement|Piloté par l’utilisateur|
|Rejoindre Azure AD en tant que|Joint à Azure AD|
|Langue (Région)|Sélection de l’utilisateur|
|Configurer automatiquement le clavier|Non|
|Termes du contrat de licence logiciel Microsoft|Masquer|
|Paramètres de confidentialité|Masquer|
|Masquer les options de modification du compte|Afficher|
|Type de compte d’utilisateur|Standard|
|Autoriser la OOBE pour les gant blancs|Oui|
|Appliquer le modèle de nom d’appareil|Oui|
|Entrer un nom|MMD-%RAND:11%|
|

## <a name="enrollment-status-page-settings"></a>Paramètres de la page État de l’inscription

Bureau géré Microsoft utilise ces paramètres pour l’expérience Page d’état de l’inscription :

<br>

****

|Paramètre|Valeur|
|---|---|
|Afficher l’avancement de la configuration des applications et des profils|Oui|
|Afficher une erreur lorsque l’installation prend plus de temps que le nombre de minutes spécifié|60|
|Afficher un message personnalisé en cas d’erreur de limite de temps|Oui|
|Message d’erreur|Oui, la mise en place de votre appareil prend un peu plus de temps que prévu. Cliquez ci-dessous pour commencer et nous terminerons la configuration en arrière-plan|
|Autoriser les utilisateurs à collecter des journaux sur les erreurs d’installation|Oui|
|Afficher uniquement la page sur les appareils provisionés par l’expérience OOBE (Out-of-Box Experience)|Oui|
|Bloquer l’utilisation de l’appareil jusqu’à ce que toutes les applications et les profils soient installés|Oui|
|Autoriser les utilisateurs à réinitialiser l’appareil en cas d’erreur d’installation|Oui|
|Autoriser les utilisateurs à utiliser l’appareil en cas d’erreur d’installation|Oui|
|Bloquer l’utilisation de l’appareil jusqu’à ce que ces applications requises soient installées si elles sont affectées à l’utilisateur/l’appareil|Espace de travail moderne - Correction du temps|
|

L’expérience page État de l’inscription se produit en trois phases. Pour plus d’informations, consultez les informations de suivi [de la page État de l’inscription.](/mem/intune/enrollment/windows-enrollment-status#enrollment-status-page-tracking-information)

L’expérience se déroule comme suit :

1. L’expérience Autopilot démarre et l’utilisateur entre ses informations d’identification.
2. L’appareil ouvre la page État de l’inscription et passe par les phases de préparation et de configuration de l’appareil. La troisième étape (configuration  du compte) est actuellement ignorée dans la configuration Bureau géré Microsoft car l’esp utilisateur est désactivée. L’appareil redémarre.
3. Après le redémarrage, l’appareil ouvre Windows page de Windows avec **un autre utilisateur.**
4. Les utilisateurs entrent à nouveau leurs informations d’identification et le Bureau s’ouvre.

> [!NOTE]
> Les applications Win32 sont déployées uniquement pendant esp si la version Windows 10 est 1903 ou ultérieure.

![Page de démarrage de l’installation d’Autopilot affichant les phases de « préparation de l’appareil » et de « configuration de l’appareil ».](../../media/mmd-autopilot-screenshot.png)

## <a name="autopilot-for-pre-provisioned-deployment"></a>Autopilot pour le déploiement pré-provisioné

> [!NOTE]
> Autopilot pour le déploiement pré-provisioné dans Bureau géré Microsoft est actuellement en prévisualisation publique.

## <a name="additional-prerequisites-for-autopilot-for-pre-provisioned-deployment"></a>Conditions préalables supplémentaires pour Autopilot pour le déploiement pré-provisioné

- La page d’état d’inscription (ESP) doit être activée. Pour plus d’informations, voir [Déploiement initial.](#initial-deployment)
- L’appareil doit avoir une connexion réseau câblé.
- Si vous avez des appareils qui ont été inscrits à l’aide du portail Bureau géré Microsoft d’août 2020, désins inscrivez-les et inscrivez-les à nouveau.
- Les appareils doivent avoir une image d’usine qui inclut la mise à jour cumulative [19H1/19H2 2020.11C](https://support.microsoft.com/topic/november-19-2020-kb4586819-os-builds-18362-1237-and-18363-1237-preview-25cbb849-74af-b8b8-29b8-68aa925e8cc3) ou [20H1 2020.11C de novembre 2020,](https://support.microsoft.com/topic/november-30-2020-kb4586853-os-builds-19041-662-and-19042-662-preview-8fb07fb8-a7dd-ea62-d65e-3305da09f92e) si nécessaire, installée ou doit être réinventée avec la dernière image Bureau géré Microsoft.
- Les appareils physiques doivent prendre en charge le TPM 2.0 et l’attestation d’appareil. Les machines virtuelles ne sont pas pris en charge. Le processus de pré-approvisionnement utilise Windows auto-déploiement Autopilot, le TPM 2.0 est donc requis. Le processus d’attestation de TPM nécessite également l’accès à un ensemble d’URL HTTPS uniques pour chaque fournisseur de TPM. Pour plus d’informations, voir l’entrée relative au mode auto-déploiement Autopilot et au déploiement autopilot pré-mis en service dans Windows conditions requises pour la mise en réseau [Autopilot.](/mem/autopilot/networking-requirements#tpm)

## <a name="sequence-of-events-in-autopilot-for-pre-provisioned-deployment"></a>Séquence d’événements dans Autopilot pour le déploiement pré-provisioné

1. L’administrateur informatique réinitialise ou réinitialise l’appareil si nécessaire.
2. L’administrateur informatique démarre l’appareil, atteint l’expérience « out-of-box experience » et appuie sur la touche Windows cinq fois.
3. L’administrateur informatique sélectionne Windows approvisionnement Autopilot, puis sélectionne **Continuer**. Sur l’Windows de configuration Autopilot, des informations sur l’appareil s’affichent.
4. L’administrateur informatique sélectionne **Provision** pour démarrer le processus d’approvisionnement.
5. L’appareil démarre ESP et passe par les phases de préparation et de configuration de l’appareil. Pendant la phase de configuration de l’appareil, **l’installation** de l’application x s’affiche (selon la configuration exacte du profil ESP).
6. L’étape de configuration du compte est actuellement ignorée dans la configuration Bureau géré Microsoft, dans la mesure où nous désactivons esp utilisateur.
7. L’appareil redémarre.

Après le redémarrage, l’appareil affiche l’écran d’état vert, avec un **bouton Reseal.**

> [!IMPORTANT]
> Problèmes connus :
>
> - ESP ne s’exécute pas à nouveau après Autopilot pour la fonction de réapprovisionnement de déploiement pré-mise en service.
> - L’appareil n’est pas renommé par Autopilot pour le déploiement pré-mis en service. L’appareil sera renommé uniquement après avoir passé par le flux utilisateur ESP.

## <a name="change-to-autopilot-and-enrollment-status-page-settings"></a>Modification des paramètres Autopilot et Page d’état de l’inscription

Si la configuration utilisée par Bureau géré Microsoft ne correspond pas exactement à vos besoins, vous pouvez déposer un ticket de support via le [portail d’administration.](https://portal.azure.com/) Voici quelques exemples des types de configuration dont vous pourriez avoir besoin :

### <a name="autopilot-settings-change"></a>Modification des paramètres Autopilot

Vous pouvez demander un autre modèle de nom d’appareil. Toutefois, vous ne pouvez pas modifier le mode de déploiement, rejoindre Azure AD As, Paramètres confidentialité ou type de compte d’utilisateur.

### <a name="enrollment-status-page-settings-change"></a>Modification des paramètres de la page d’état de l’inscription

- Nombre de minutes plus long pour le paramètre « Afficher une erreur lorsque l’installation prend plus de temps que le nombre de minutes spécifié ».
- Message d’erreur affiché
- Ajout ou suppression d’applications dans le paramètre « Bloquer l’utilisation des appareils jusqu’à ce que ces applications requises soient installées si elles sont affectées à l’utilisateur/l’appareil ».

## <a name="required-applications"></a>Applications requises

- Vous devez cibler des applications dans les groupes d’appareils Workplace modernes *Test,* First, Fast et Broad. Les applications doivent être installées dans le contexte « Système ». Veillez à effectuer le test avec ESP dans le groupe Test avant de les affecter à tous les groupes.
- Aucune application ne doit nécessiter le redémarrage de l’appareil. Nous recommandons que les applications soient définies sur « Ne rien faire » lorsque vous créez le package d’application si elles nécessitent un redémarrage.
- Limitez les applications requises aux applications principales dont un utilisateur a besoin immédiatement lorsqu’il se connecte à l’appareil.
- Conservez la taille totale de toutes les applications collectivement sous 1 Go pour éviter les délai d’accès pendant la phase d’installation de l’application.
- Dans l’idéal, les applications ne doivent pas avoir de dépendances. Si vous avez des applications qui *doivent* avoir des dépendances, assurez-vous de les configurer, de les tester et de les valider dans le cadre de votre évaluation ESP.
- Aucune application nécessitant le contexte « utilisateur » (par exemple, Teams) ne peut être incluse dans la prévisualisation publique d’ESP.
