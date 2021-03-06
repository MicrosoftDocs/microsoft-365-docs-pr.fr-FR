---
title: Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender pour Endpoint sur Linux
description: Détecter et bloquer les applications potentiellement indésirables (PUA) à l’aide de Microsoft Defender pour endpoint sur Linux.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, pua, pus
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 7ec3399129cc65d75b464f5d5f56bb11250ccaf2
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933156"
---
# <a name="detect-and-block-potentially-unwanted-applications-with-microsoft-defender-for-endpoint-on-linux"></a>Détecter et bloquer les applications potentiellement indésirables avec Microsoft Defender pour Endpoint sur Linux

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


**S’applique à :**
- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> Vous souhaitez faire l’expérience de Defender for Endpoint ? [Inscrivez-vous à un essai gratuit.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

La fonctionnalité de protection des applications potentiellement indésirables dans Defender for Endpoint sur Linux peut détecter et bloquer les fichiers PUA sur les points de terminaison de votre réseau.

Ces applications ne sont pas considérées comme des virus, des programmes malveillants ou d’autres types de menaces, mais peuvent effectuer des actions sur les points de terminaison qui affectent leurs performances ou leur utilisation. PuA peut également faire référence à des applications considérées comme de mauvaise réputation.

Ces applications peuvent augmenter le risque d’infection de votre réseau par des programmes malveillants, rendre l’identification des programmes malveillants plus difficile et entraîner une perte de ressources informatiques lors du nettoyage des applications.

## <a name="how-it-works"></a>Mode de fonctionnement

Defender pour le point de terminaison sur Linux peut détecter et signaler des fichiers PUA. Lorsqu’ils sont configurés en mode de blocage, les fichiers PUA sont placés en quarantaine.

Lorsqu’une PUA est détectée sur un point de terminaison, Defender for Endpoint sur Linux conserve un enregistrement de l’infection dans l’historique des menaces. L’historique peut être visualisé à partir du portail Centre de sécurité Microsoft Defender ou via l’outil `mdatp` en ligne de commande. Le nom de la menace contient le mot « Application ».

## <a name="configure-pua-protection"></a>Configurer la protection PUA

La protection PUA dans Defender for Endpoint sur Linux peut être configurée de l’une des manières suivantes :

- **Désactivé**: la protection PUA est désactivée.
- **Audit**: les fichiers PUA sont signalés dans les journaux du produit, mais pas dans Centre de sécurité Microsoft Defender. Aucun enregistrement de l’infection n’est stocké dans l’historique des menaces et aucune action n’est prise par le produit.
- **Bloquer**: les fichiers PUA sont signalés dans les journaux du produit et dans Centre de sécurité Microsoft Defender. Un enregistrement de l’infection est stocké dans l’historique des menaces et une action est prise par le produit.

>[!WARNING]
>Par défaut, la protection PUA est configurée en mode **audit.**

Vous pouvez configurer la façon dont les fichiers PUA sont gérés à partir de la ligne de commande ou de la console de gestion.

### <a name="use-the-command-line-tool-to-configure-pua-protection"></a>Utilisez l’outil de ligne de commande pour configurer la protection PUA :

Dans Terminal, exécutez la commande suivante pour configurer la protection PUA :

```bash
mdatp threat policy set --type potentially_unwanted_application --action [off|audit|block]
```

### <a name="use-the-management-console-to-configure-pua-protection"></a>Utilisez la console de gestion pour configurer la protection PUA :

Dans votre entreprise, vous pouvez configurer la protection PUA à partir d’une console de gestion, telle qu’une console de jeu ou ansible, de la même manière que d’autres paramètres de produit sont configurés. Pour plus d’informations, voir la section [Paramètres du type](linux-preferences.md#threat-type-settings) de menace de l’article Définir les préférences de [Defender pour Endpoint sur Linux.](linux-preferences.md)

## <a name="related-articles"></a>Articles connexes

- [Définir des préférences pour Defender pour endpoint sur Linux](linux-preferences.md)
