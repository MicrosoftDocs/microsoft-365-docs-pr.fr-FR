---
title: Activer la protection cloud dans l'Antivirus Microsoft Defender
description: Activer la protection cloud pour bénéficier des fonctionnalités de protection rapide et avancée.
keywords: Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, cloud, bloquer à la première vue
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.date: 11/13/2020
ms.reviewer: ''
manager: dansimp
ms.custom: nextgen
ms.technology: mde
ms.openlocfilehash: 9f949a4cb54ca5dd64a2648bb05a5cb9ad50e44d
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764962"
---
# <a name="turn-on-cloud-delivered-protection"></a>Activer la protection cloud

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**

- [Microsoft Defender pour point de terminaison](/microsoft-365/security/defender-endpoint/)

> [!NOTE]
> Le service cloud de l'Antivirus Microsoft Defender est un mécanisme permettant de fournir une protection mise à jour à votre réseau et points de terminaison. Bien qu'il soit appelé service cloud, il ne s'agit pas simplement de la protection des fichiers stockés dans le cloud . Au lieu de cela, il utilise des ressources distribuées et l'apprentissage automatique pour fournir une protection à vos points de terminaison à une vitesse beaucoup plus rapide que les mises à jour d'intelligence de sécurité traditionnelles.

L'Antivirus Microsoft Defender utilise plusieurs technologies de détection et de prévention pour offrir une protection précise, en temps réel et intelligente. Faire connaître les technologies avancées au cœur de Microsoft Defender pour la protection nouvelle génération de point de [terminaison.](https://www.microsoft.com/security/blog/2019/06/24/inside-out-get-to-know-the-advanced-technologies-at-the-core-of-microsoft-defender-atp-next-generation-protection/)
![Liste des moteurs de Microsoft Defender AV](images/microsoft-defender-atp-next-generation-protection-engines.png)  

Vous pouvez activer ou désactiver la protection de l'Antivirus Microsoft Defender sur le cloud de plusieurs façons :

- Microsoft Intune
- Microsoft Endpoint Configuration Manager
- Stratégie de groupe
- Cmdlets PowerShell.

 Vous pouvez également l'activer ou le désactiver dans des clients individuels avec l'application Sécurité Windows.

Pour obtenir une vue d'ensemble de la protection de l'antivirus Microsoft Defender, voir Utiliser la protection cloud de [Microsoft.](cloud-protection-microsoft-defender-antivirus.md)

Pour plus d'informations sur les exigences de connectivité réseau spécifiques pour vous assurer que vos points de terminaison peuvent se connecter au service de protection livré par le cloud, voir Configurer et valider les [connexions réseau.](configure-network-connections-microsoft-defender-antivirus.md)

> [!NOTE]
> Dans Windows 10, il n'existe  aucune différence entre les options de rapports de base et avancées décrites dans cette rubrique.  Il s'agit d'une distinction héritée et le choix de l'un ou l'autre des paramètres entraîne le même niveau de protection cloud. Il n'existe aucune différence dans le type ou la quantité d'informations partagées. Pour plus d'informations sur ce que nous collectons, consultez la déclaration [de confidentialité de Microsoft.](https://go.microsoft.com/fwlink/?linkid=521839)

## <a name="use-intune-to-turn-on-cloud-delivered-protection"></a>Utiliser Intune pour activer la protection cloud

1. Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.
2. Dans le **volet Accueil,** sélectionnez Configuration de l'> **profils.**
3. Sélectionnez le type **de profil restrictions d'appareil** que vous souhaitez configurer. Si vous devez créer un type de profil de **restrictions** d'appareil, voir Configurer les [paramètres de restriction d'appareil dans Microsoft Intune.](/intune/device-restrictions-configure)
4. Sélectionnez **les**  >  **paramètres de configuration des propriétés : modifier**  >  **l'Antivirus Microsoft Defender.**
5. Sur le **commutateur de protection cloud,** sélectionnez **Activer.**
6. Dans la demande **d'utilisateurs avant la** soumission d'exemples, **sélectionnez Envoyer toutes les données automatiquement.**

Pour plus d'informations sur les profils d'appareil Intune, notamment sur la création et la configuration de leurs paramètres, voir Qu'est-ce que les profils [d'appareil Microsoft Intune ?](/intune/device-profiles)

## <a name="use-microsoft-endpoint-manager-to-turn-on-cloud-delivered-protection"></a>Utiliser Microsoft Endpoint Manager pour activer la protection cloud

1. Go to the Microsoft Endpoint Manager admin center ( [https://endpoint.microsoft.com](https://endpoint.microsoft.com) ) and log in.
2. Choisissez **l'Antivirus de sécurité des points de**  >  **terminaison.**
3. Sélectionnez un profil antivirus. (Si vous n'en avez pas encore, ou si vous souhaitez créer un profil, voir Configurer les paramètres de [restriction d'appareil dans Microsoft Intune](/intune/device-restrictions-configure).
4. Sélectionnez **propriétés**. Ensuite, en de côté **des paramètres de configuration,** choisissez **Modifier.**
5. Développez **La protection** cloud, puis dans la liste des niveaux de **protection** cloud, sélectionnez l'une des listes suivantes :
    1. **Élevé**: applique un niveau de détection élevé.
    2. **Plus élevé**: utilise le **niveau élevé** et applique des mesures de protection supplémentaires (peut avoir un impact sur les performances du client).
    3. **Tolérance zéro :** bloque tous les exécutables inconnus.
6. Sélectionnez **Révision + Enregistrer,** puis **sélectionnez Enregistrer.**

Pour plus d'informations sur la configuration de Microsoft Endpoint Configuration Manager, voir Comment créer et déployer des stratégies [anti-programme](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)malveillant : service de protection cloud.

## <a name="use-group-policy-to-turn-on-cloud-delivered-protection"></a>Utiliser la stratégie de groupe pour activer la protection cloud

1. Sur votre appareil de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe que vous souhaitez configurer et sélectionnez **Modifier.**

2. Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration de l'ordinateur.**

3. Sélectionnez **modèles d'administration.**

4. Développez l'arborescence **des composants Windows > l'Antivirus Microsoft Defender > MAPS**

5. Double-cliquez sur **Rejoindre Microsoft MAPS.** Assurez-vous que l'option est allumée et définie sur **Maps de base** ou Cartes **avancées.** Sélectionnez **OK**.

6. Double-cliquez sur **Envoyer des exemples de fichier lorsque d'autres analyses sont nécessaires.** Assurez-vous que la première option est définie sur **Activé** et que les autres options sont définies sur :

    1. **Envoyer des exemples sécurisés** (1)
    2. **Envoyer tous les exemples** (3)

        >[!NOTE]
        > **L'option Envoyer des échantillons sûrs** (1) signifie que la plupart des échantillons seront envoyés automatiquement. Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.

        > [!WARNING]
        > Définir l'option **sur Always Prompt** (0) réduit l'état de protection de l'appareil. Le fait de la définir sur [](configure-block-at-first-sight-microsoft-defender-antivirus.md) **Ne** jamais envoyer (2) signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de terminaison ne fonctionne pas.

7. Sélectionnez **OK**.

## <a name="use-powershell-cmdlets-to-turn-on-cloud-delivered-protection"></a>Utiliser les cmdlets PowerShell pour activer la protection cloud

Les cmdlets suivantes peuvent activer la protection cloud :

```PowerShell
Set-MpPreference -MAPSReporting Advanced
Set-MpPreference -SubmitSamplesConsent SendAllSamples
```

Pour plus d'informations sur l'utilisation de PowerShell avec l'Antivirus Microsoft Defender, voir Utiliser les [cmdlets PowerShell](use-powershell-cmdlets-microsoft-defender-antivirus.md) pour configurer et exécuter l'Antivirus Microsoft Defender et les [cmdlets Defender.](/powershell/module/defender/) [Stratégie CSP - Defender](/windows/client-management/mdm/policy-csp-defender) a également plus d'informations spécifiques sur [-SubmitSamplesConsent](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent).

>[!NOTE]
> Vous pouvez également définir **-SubmitSamplesConsent** sur (paramètre par `SendSafeSamples` défaut), `NeverSend` ou `AlwaysPrompt` . Le `SendSafeSamples` paramètre signifie que la plupart des échantillons seront envoyés automatiquement. Les fichiers susceptibles de contenir des informations personnelles seront toujours invités et nécessitent une confirmation supplémentaire.

>[!WARNING]
> Paramètre **-SubmitSamplesConsent** pour `NeverSend` ou réduit le niveau de protection de `AlwaysPrompt` l'appareil. En outre, sa définition signifie que la fonctionnalité Bloquer à la première vue de Microsoft Defender pour le point de `NeverSend` terminaison ne fonctionne pas. [](configure-block-at-first-sight-microsoft-defender-antivirus.md)

## <a name="use-windows-management-instruction-wmi-to-turn-on-cloud-delivered-protection"></a>Utiliser Windows Management Instruction (WMI) pour activer la protection cloud

Utilisez la [ **méthode Set** de la **classe MSFT_MpPreference**](/previous-versions/windows/desktop/defender/set-msft-mppreference) pour les propriétés suivantes :

```WMI
MAPSReporting
SubmitSamplesConsent
```

Pour plus d'informations sur les paramètres autorisés, [voir Windows Defender API WMIv2](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)

## <a name="turn-on-cloud-delivered-protection-on-individual-clients-with-the-windows-security-app"></a>Activer la protection cloud sur des clients individuels avec l'application Sécurité Windows

> [!NOTE]
> Si le paramètre Configurer le remplacement de paramètre local pour la création de rapports sur la stratégie de groupe **Microsoft MAPS** est **désactivé,** le paramètre de protection basée sur le **cloud** dans les paramètres Windows est grisé et indisponible. Les modifications apportées via un objet de stratégie de groupe doivent d'abord être déployées sur des points de terminaison individuels avant que le paramètre ne soit mis à jour dans les paramètres Windows.

1. Ouvrez l'application Sécurité Windows en sélectionnant l'icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**

2. Sélectionnez la **vignette & protection** contre les virus contre les menaces (ou l'icône de bouclier dans la barre de menus de gauche), puis l'étiquette des **paramètres** de protection contre & virus :

    ![Capture d'écran de l'étiquette & protection contre les virus dans l'application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. Confirmez que **la protection basée sur le cloud** et **l'envoi automatique** d'échantillons sont **activés.**

> [!NOTE]
> Si l'envoi automatique d'échantillons a été configuré avec la stratégie de groupe, le paramètre est grisé et indisponible.

## <a name="related-articles"></a>Articles connexes

- [Configurer le délai d'attente du blocage du cloud](configure-cloud-block-timeout-period-microsoft-defender-antivirus.md)
- [Configurer bloquer à la première vue](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [Utiliser les cmdlets PowerShell pour gérer l'Antivirus Microsoft Defender](use-powershell-cmdlets-microsoft-defender-antivirus.md)
- [Sécurisation des PC Windows avec Endpoint Protection pour Microsoft Intune](/intune/deploy-use/help-secure-windows-pcs-with-endpoint-protection-for-microsoft-intune)]
- [Cmdlets Defender](/powershell/module/defender/)
- [Utiliser la protection microsoft cloud dans l'Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md)
- [Comment créer et déployer des stratégies de logiciel anti-programme malveillant : service de protection cloud](/configmgr/protect/deploy-use/endpoint-antimalware-policies#cloud-protection-service)
- [Antivirus Microsoft Defender dans Windows 10](microsoft-defender-antivirus-in-windows-10.md)