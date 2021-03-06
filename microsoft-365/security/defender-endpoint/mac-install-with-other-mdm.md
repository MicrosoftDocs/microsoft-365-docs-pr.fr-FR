---
title: Déploiement avec un autre système de gestion des périphériques mobiles (MDM) pour Microsoft Defender pour Endpoint sur Mac
description: Installez Microsoft Defender pour point de terminaison sur Mac sur d’autres solutions de gestion.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mac, installation, déployer, macos, principal, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: mavel
author: maximvelichko
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: ca779fc4cc8c40adb25a0e95a9450f59954dc605
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933792"
---
# <a name="deployment-with-a-different-mobile-device-management-mdm-system-for-microsoft-defender-for-endpoint-on-macos"></a>Déploiement avec un autre système de gestion des périphériques mobiles (MDM) pour Microsoft Defender pour Endpoint sur macOS

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)
 
## <a name="prerequisites-and-system-requirements"></a>Conditions préalables et système requis

Avant de commencer, consultez la page principale de Microsoft Defender pour point de terminaison sur [macOS](microsoft-defender-endpoint-mac.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.


## <a name="approach"></a>Approche

> [!CAUTION]

> Actuellement, Microsoft prend officiellement en charge uniquement Intune et JAMF pour le déploiement et la gestion de Microsoft Defender pour Endpoint sur macOS. Microsoft n’offre aucune garantie, expressément ou implicite, en ce qui concerne les informations fournies ci-dessous.

Si votre organisation utilise une solution de gestion des périphériques mobiles (MDM) qui n’est pas officiellement prise en charge, cela ne signifie pas que vous ne pouvez pas déployer ou exécuter Microsoft Defender pour endpoint sur macOS.

Microsoft Defender pour le point de terminaison sur macOS ne dépend d’aucune fonctionnalité propre au fournisseur. Il peut être utilisé avec n’importe quelle solution DE GESTION DES SOLUTIONS QUI prend en charge les fonctionnalités suivantes :

- Déployez un .pkg macOS sur des appareils gérés.
- Déployez les profils de configuration système macOS sur les appareils gérés.
- Exécutez un outil/script arbitraire configuré par l’administrateur sur des appareils gérés.

La plupart des solutions mdm modernes incluent ces fonctionnalités, mais elles peuvent les appeler différemment.

Toutefois, vous pouvez déployer Defender sans la dernière condition requise de la liste précédente :

- Vous ne pourrez pas collecter l’état de manière centralisée
- Si vous décidez de désinstaller Defender, vous devez vous connecter localement à l’appareil client en tant qu’administrateur.

## <a name="deployment"></a>Déploiement

La plupart des solutions MDM utilisent le même modèle pour la gestion des appareils macOS, avec une terminologie similaire. Utilisez [un déploiement basé sur JAMF](mac-install-with-jamf.md) comme modèle.

### <a name="package"></a>Package

Configurez le déploiement d’un [package d’application](mac-install-with-jamf.md) [requis,](mac-install-with-jamf.md)avec le package d’installation (wdav.pkg) téléchargé à partir Centre de sécurité Microsoft Defender .

Pour déployer le package dans votre entreprise, utilisez les instructions associées à votre solution MDM.

### <a name="license-settings"></a>Paramètres de licence

Configurer un [profil de configuration système.](mac-install-with-jamf.md) 

Votre solution MDM peut l’appeler « Profil Paramètres personnalisé », car Microsoft Defender pour endpoint sur macOS ne fait pas partie de macOS.

Utilisez la liste des propriétés, jamf/WindowsDefenderATPOnboarding.plist, qui peut être extraite d’un package d’intégration téléchargé à partir [Centre de sécurité Microsoft Defender](mac-install-with-jamf.md).
Votre système peut prendre en charge une liste de propriétés arbitraire au format XML. Vous pouvez télécharger le fichier jamf/WindowsDefenderATPOnboarding.plist tel qu’il est dans ce cas.
Vous pouvez également avoir besoin de convertir d’abord la liste des propriétés dans un autre format.

En règle générale, votre profil personnalisé possède un ID, un nom ou un attribut de domaine. Vous devez utiliser exactement « com.microsoft.wdav.atp » pour cette valeur.
GDM l’utilise pour déployer le fichier de paramètres dans **/Library/Managed Preferences/com.microsoft.wdav.atp.plist** sur un appareil client, et Defender utilise ce fichier pour charger les informations d’intégration.

### <a name="kernel-extension-policy"></a>Stratégie d’extension du noyau

Configurer une stratégie KEXT ou d’extension de noyau. Utilisez **l’identificateur d’équipe UBF8T346G9** pour autoriser les extensions de noyau fournies par Microsoft.

> [!CAUTION]
> Si votre environnement se compose d’appareils Apple Silicon (M1), ces ordinateurs ne doivent pas recevoir de profils de configuration avec les stratégies KEXT.
> Apple ne prend pas en charge KEXT sur ces ordinateurs, le déploiement de ce profil échouerait sur les ordinateurs M1.

### <a name="system-extension-policy"></a>Stratégie d’extension système

Configurer une stratégie d’extension système. Utilisez **l’identificateur d’équipe UBF8T346G9** et approuvez les identificateurs d’ensemble suivants :

- com.microsoft.wdav.epsext
- com.microsoft.wdav.netext

### <a name="full-disk-access-policy"></a>Stratégie d’accès disque complet

Accordez un accès disque total aux composants suivants :

- Microsoft Defender pour point de terminaison
    - Identificateur : `com.microsoft.wdav`
    - Type d’identificateur : ID d’offre groupée
    - Conditions requises pour le code : `identifier "com.microsoft.wdav" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`

- Microsoft Defender pour l’extension de sécurité de point de terminaison
    - Identificateur : `com.microsoft.wdav.epsext`
    - Type d’identificateur : ID d’offre groupée
    - Conditions requises pour le code : `identifier "com.microsoft.wdav.epsext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`

### <a name="network-extension-policy"></a>Stratégie d’extension réseau

Dans le cadre des fonctionnalités de détection et de réponse des points de terminaison, Microsoft Defender for Endpoint sur macOS inspecte le trafic de socket et signale ces informations au portail Centre de sécurité Microsoft Defender. La stratégie suivante permet à l’extension réseau d’effectuer cette fonctionnalité.

- Type de filtre : Plug-in
- Identificateur de l’ensemble de plug-ins : `com.microsoft.wdav`
- Identificateur d’ensemble du fournisseur de données de filtre : `com.microsoft.wdav.netext`
- Exigence désignée par le fournisseur de données de filtre : `identifier "com.microsoft.wdav.tunnelext" and anchor apple generic and certificate 1[field.1.2.840.113635.100.6.2.6] /* exists */ and certificate leaf[field.1.2.840.113635.100.6.1.13] /* exists */ and certificate leaf[subject.OU] = UBF8T346G9`
- Filtrer les sockets : `true`

## <a name="check-installation-status"></a>Vérifier l’état de l’installation

Exécutez [Microsoft Defender pour le point de terminaison](mac-install-with-jamf.md) sur un appareil client pour vérifier l’état d’intégration.
