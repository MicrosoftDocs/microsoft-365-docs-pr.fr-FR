---
title: Configurer des groupes d’appareils dans Jamf Pro
description: Découvrez comment configurer des groupes d’appareils dans Jamf Pro pour Microsoft Defender ATP pour macOS
keywords: device, group, microsoft, defender, atp, mac, installation, deploy, uninstallation, intune, jamfpro, macos,pépé, mojave, high sierra
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 36db18ba16bb51f3be0cbaba7d4ca4d27195e85d
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187660"
---
# <a name="set-up-microsoft-defender-for-endpoint-for-macos-device-groups-in-jamf-pro"></a>Configurer Microsoft Defender pour le point de terminaison pour les groupes d’appareils macOS dans Jamf Pro

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

Configurer les groupes d’appareils semblables aux groupes d’organisation de stratégie de groupe, à la collection d’appareils de Microsoft Endpoint Configuration Manager et aux groupes d’appareils d’Intune.

1. Accédez à **Groupes d’ordinateurs statiques.**

2. Sélectionnez **Nouveau**. 

    ![Image de Jamf Pro1](images/jamf-pro-static-group.png)

3. Fournissez un nom d’affichage et sélectionnez **Enregistrer.**

    ![Image de Jamf Pro2](images/jamfpro-machine-group.png)

4. Vous verrez maintenant le groupe **d’ordinateurs de Contoso** sous **Groupes d’ordinateurs statiques.**

    ![Image de Jamf Pro3](images/contoso-machine-group.png)

## <a name="next-step"></a>Étape suivante
- [Configurer Microsoft Defender pour le point de terminaison pour les stratégies macOS dans Jamf Pro](mac-jamfpro-policies.md)