---
title: Collecter des données de diagnostic pour mettre à jour la conformité et Windows Defender Antivirus Microsoft Defender
description: Utiliser un outil pour collecter des données afin de résoudre les problèmes de conformité des mises à jour lors de l'utilisation de l'évaluation antivirus Microsoft Defender
keywords: résoudre les problèmes, erreur, corriger, mettre à jour la conformité, oms, surveiller, signaler, Microsoft Defender AV
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: f2b3060d7f0d9daf0f923c674f2fe45ba976fdfc
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51764734"
---
# <a name="collect-update-compliance-diagnostic-data-for-microsoft-defender-av-assessment"></a>Collecter les données de diagnostic de conformité des mises à jour pour l'évaluation de Microsoft Defender AV

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**

- [Microsoft Defender pour point de terminaison](/microsoft-365/security/defender-endpoint/)

Cet article explique comment collecter des données de diagnostic qui peuvent être utilisées par les équipes de support et d'ingénierie de Microsoft pour vous aider à résoudre les problèmes que vous pouvez rencontrer lors de l'utilisation de la section Évaluation de l'Antivirus Microsoft Defender dans le module de conformité des mises à jour.

Avant d'essayer ce processus, assurez-vous que vous avez lu la résolution des problèmes de rapport de [l'Antivirus Microsoft Defender,](troubleshoot-reporting.md)que vous avez satisfait à toutes les conditions préalables requises et que vous avez pris toutes les autres étapes de dépannage suggérées.

Sur au moins deux appareils qui ne sont pas signalés ou qui s'affichent dans Update Compliance, obtenez le fichier de diagnostic .cab en suivant les étapes ci-après :

1. Ouvrez une version de niveau administrateur de l'invite de commandes comme suit :
        
    a. Ouvrez **le** menu Démarrer.

    b. Tapez **cmd**. Cliquez avec le bouton droit sur **l'invite de** commandes, puis cliquez **sur Exécuter en tant qu'administrateur.**

    c. Entrez les informations d'identification de l'administrateur ou approuvez l'invite.
        
2. Accédez au répertoire Windows Defender de recherche. Par défaut, cette valeur est `C:\Program Files\Windows Defender`.

3. Tapez la commande suivante, puis appuyez sur **Entrée**
        
    ```Dos
    mpcmdrun -getfiles
    ```
    
4. Un fichier .cab qui contient divers journaux de diagnostic est généré. L'emplacement du fichier est spécifié dans la sortie de l'invite de commandes. Par défaut, l'emplacement est `C:\ProgramData\Microsoft\Windows Defender\Support\MpSupportFiles.cab` .

5. Copiez ces fichiers .cab vers un emplacement accessible par le support Microsoft. Par exemple, il peut s'agit d'un dossier OneDrive protégé par mot de passe que vous pouvez partager avec nous.

6. Envoyez un courrier <a href="mailto:ucsupport@microsoft.com?subject=WDAV assessment issue&body=I%20am%20encountering%20the%20following%20issue%20when%20using%20Windows%20Defender%20AV%20in%20Update%20Compliance%3a%20%0d%0aI%20have%20provided%20at%20least%202%20support%20.cab%20files%20at%20the%20following%20location%3a%20%3Caccessible%20share%2c%20including%20access%20details%20such%20as%20password%3E%0d%0aMy%20OMS%20workspace%20ID%20is%3a%20%0d%0aPlease%20contact%20me%20at%3a"></a>électronique à l'aide du modèle de courrier électronique de prise en charge de la conformité des mises à jour et remplissez le modèle avec les informations suivantes :
  
    ```
    I am encountering the following issue when using Microsoft Defender Antivirus in Update Compliance:
    
    I have provided at least 2 support .cab files at the following location: <accessible share, including access details such as password>

    My OMS workspace ID is:

    Please contact me at:
    ```

## <a name="see-also"></a>Voir aussi

- [Résoudre les problèmes Windows Defender rapports de l'Antivirus Microsoft Defender](troubleshoot-reporting.md)