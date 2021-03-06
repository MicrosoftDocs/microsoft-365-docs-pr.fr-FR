---
title: Prise en charge de la conformité Microsoft 365 pour les notes de publication des jeux de caractères à double octets (préversion)
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Notes de publication pour la prise en charge des jeux de caractères à double octets.
ms.openlocfilehash: 1c2244c49a92aa2c00fad06caa8194cf7e32220e
ms.sourcegitcommit: 554755bc9ce40228ce6e34bde6fc6e226869b6a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48681500"
---
# <a name="support-for-double-byte-character-set-release-notes-preview"></a>Prise en charge des notes de publication des jeux de caractères à double octets (préversion)

 Microsoft 365 Information Protection prend désormais en charge, en préversion, les langues de jeu de caractères à double octets pour :

- le chinois simplifié
- Chinois (traditionnel)
- Korean
- Japanese

Cette prise en charge est disponible pour les types d’informations sensibles et les dictionnaires de mots-clés et sera affichée dans les solutions de protection contre la perte de données, de conformité des communications, Exchange Online, SharePoint Online, OneDrive Entreprise et Teams.

## <a name="known-issues"></a>Problèmes connus

- Lorsqu’un fichier texte joint à un e-mail est au format UTF-8 sans indicateur d’ordre des octets (BOM), l’e-mail n’est pas détecté par la stratégie de conformité des communications.

- Les stratégies de conformité des communications ne peuvent pas détecter de valeurs si une phrase est saisie pour la condition de stratégie : « Le message contient l’un de ces mots ». Si le texte spécifié dans la stratégie est écrit sous forme de mot, il peut être détecté. Cependant, s’il est écrit au milieu d’une phrase, il ne sera pas détecté.

- Les stratégies de conformité des communications qui spécifient des dictionnaires comme informations de type ne détectent pas les discussions privées et les discussions de canal Teams.

- Les conditions suivantes ne sont pas prises en charge pour la conformité des communications à ce stade (nous prévoyons de résoudre ces problèmes à l’avenir) : 
  - « Le message contient l’un de ces mots »
  - « Le message ne contient aucun de ces mots »
  - « La pièce jointe contient l’un de ces mots »
  - « La pièce jointe contient l’un de ces mots »

Nous vous recommandons plutôt de créer un type d’informations sensibles personnalisé, avec un dictionnaire de mots-clés, qui détectera les modèles dans les messages et les pièces jointes, et d’utiliser ce type d’informations sensibles personnalisé comme condition de stratégie de conformité des communications.
