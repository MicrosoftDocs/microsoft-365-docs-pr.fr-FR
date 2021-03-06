---
title: Gérer les accès des utilisateurs aux documents Office sur appareils mobiles
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
manager: scotv
audience: Admin
ms.topic: conceptual
f1_keywords:
- O365E_BCSSetup4OfficeMobile
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: aa31319c-9196-48c9-a90b-4057e0494c7a
description: Découvrez les stratégies de protection qui vous permettent de gérer la façon dont les utilisateurs accèdent Office applications et les fichiers de travail à partir d’appareils mobiles.
ms.openlocfilehash: 7602b712f2dfc3ba369fd76979baaaa8d5da5c5c
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925276"
---
# <a name="manage-how-users-access-office-documents-on-mobile-devices"></a>Gérer les accès des utilisateurs aux documents Office sur appareils mobiles

Cet article s’applique aux Microsoft 365 Business Premium.

[] Les paramètres de stratégie qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office à partir de leur appareil mobile sont **désactivés** par défaut. Nous vous recommandons d’accepter les valeurs par défaut lors de l’installation pour créer des stratégies d’application pour Android, iOS et Windows 10 qui s’appliquent à tous les utilisateurs. Vous pouvez créer des stratégies supplémentaires une fois l'installation terminée. 
  
## <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a>Paramètres qui contrôlent la façon dont les utilisateurs accèdent aux fichiers Office sur appareils mobiles

Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :

|Paramètre  <br/> |Description  <br/> |
|:-----|:-----|
|Exiger un code confidentiel ou une empreinte pour accéder aux applications Office  <br/> |Si ce paramètre est sur **,** les utilisateurs doivent fournir une autre forme d’authentification, en plus de leur nom d’utilisateur et mot de passe, avant de pouvoir utiliser des applications Office sur leur appareil mobile.  <br/> |
|Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion  <br/> |Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.  <br/> |
|Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office  <br/> |Ce paramètre détermine la durée pendant combien de temps un utilisateur peut être inactif avant d’être invité à se ré-inscrire.  <br/> |
|Refuser l'accès aux fichiers de travail sur les appareils « jailbreakés » ou débridés  <br/> |Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté. Cela signifie que l’utilisateur peut modifier le système d’exploitation, ce qui peut rendre l’appareil plus susceptible d’être malveillant. Ces appareils sont bloqués lorsque ce paramètre est **activé**.  <br/> |
|Ne pas autoriser les utilisateurs à copier le contenu de Office applications dans des applications personnelles  <br/> |Lorsque le paramètre est **sur ,** l’utilisateur ne peut pas copier les informations d’un fichier de travail dans un fichier personnel. Si le paramètre est **Éteint,** l’utilisateur peut copier les informations d’un fichier de travail vers une application personnelle ou un compte personnel.  <br/> |
   

