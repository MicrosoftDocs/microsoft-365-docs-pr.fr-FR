---
title: API de réponse Microsoft Defender pour point de terminaison prise en charge
description: Découvrez les appels d’API Microsoft Defender for Endpoint spécifiques liés à la réponse.
keywords: api de réponse, api de graphique, api pris en charge, acteur, alertes, appareil, utilisateur, domaine, ip, fichier
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.openlocfilehash: 36ed1f624fda7ae413ffbbf807925cf00e0a23ca
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933768"
---
# <a name="supported-microsoft-defender-for-endpoint-query-apis"></a>API de requête Microsoft Defender pour point de terminaison prise en charge 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)

> [!TIP]
> Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-supported-response-apis-abovefoldlink) 

Découvrez les appels d’API liés à la réponse pris en charge que vous pouvez exécuter, ainsi que des détails tels que les en-têtes de requête requis et la réponse attendue des appels.

## <a name="in-this-section"></a>Dans cette section
Rubrique | Description
:---|:---
Collecter un package d’examen | Exécutez cette API pour collecter un package d’enquête à partir d’un appareil.
Isoler l’appareil | Exécutez cette API pour isoler un appareil du réseau.
Appareil unisolate | Supprimez un appareil de l’isolation. 
Restreindre l’exécution du code | Exécutez cette API pour contenir une attaque en arrêtant les processus malveillants. Vous pouvez également verrouiller un appareil et empêcher toute tentative ultérieure d’exécution de programmes potentiellement malveillants.
Exécution de code de groupe | Exécutez cette vérification pour annuler la restriction de la stratégie d’applications après avoir vérifié que l’appareil compromis a été corrigé.
Exécuter une analyse antivirus | Lancez à distance une analyse antivirus pour identifier et corriger les programmes malveillants qui peuvent être présents sur un appareil compromis.
Arrêt et fichier mis en quarantaine |  Exécutez cet appel pour arrêter l’exécution des processus, mettre en quarantaine les fichiers et supprimer la persistance telle que les clés de Registre.
Exemple de demande | Exécutez cet appel pour demander un exemple de fichier à partir d’un appareil spécifique. Le fichier est collecté à partir de l’appareil et chargé dans un stockage sécurisé.
Bloquer un fichier | Exécutez cette API pour empêcher toute propagation supplémentaire d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects. 
Débloquer le fichier | Autoriser l’exécuter dans l’organisation à l’aide Antivirus Microsoft Defender.
Obtenir l’URI SAS du package | Exécutez cette API pour obtenir un URI qui permet de télécharger un package d’enquête.
Obtenir un objet MachineAction | Exécutez cette API pour obtenir l’objet MachineAction.
Obtenir la collection MachineActions | Exécutez cette action pour obtenir la collection MachineAction.
Obtenir une collection FileActions | Exécutez cette API pour obtenir la collection FileActions.
Obtenir un objet FileMachineAction | Exécutez cette API pour obtenir l’objet FileMachineAction.
Obtenir une collection FileMachineActions | Exécutez cette API pour obtenir la collection FileMachineAction.
