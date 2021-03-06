---
title: Sécuriser les applications Office sur iOS
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment sécuriser les applications Office sur iOS à l’Microsoft 365 Business Premium.
ms.openlocfilehash: 5a5f52f87fe63fdec6df9611a5ea44a2ecf4466b
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51580461"
---
# <a name="secure-office-apps-on-ios"></a>Sécuriser les applications Office sur iOS

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FLvZ?autoplay=false]

Vous pouvez configurer une stratégie d’accès utilisateur qui oblige les utilisateurs mobiles à entrer un code confidentiel ou une empreinte digitale pour se connecter, et chiffre également les fichiers de travail stockés sur leurs appareils.

## <a name="try-it"></a>Essayez !

1. Connectez-vous au centre d’administration Microsoft 365.
1. Sous **Stratégies,** choisissez **Ajouter une stratégie.**
1. Dans le **volet Ajouter une** stratégie, entrez un nom sous nom de stratégie, puis choisissez le type de stratégie que vous souhaitez sous Type de **stratégie.** 
1. Activer la gestion de la façon dont les utilisateurs **accèdent Office fichiers** sur les appareils mobiles, puis assurez-vous que les trois paramètres suivants sont actifs :
    - **Exiger un code confidentiel ou une empreinte pour accéder aux applications Office**
    - **Protéger les fichiers de travail en cas de perte ou de vol d’appareils**
    - **Chiffrer les fichiers de travail**

1. Sous **Les fichiers de ces applications** seront protégés, sélectionnez les Office que vous souhaitez protéger sur les appareils mobiles.
1. Sous Qui obtenir ces **paramètres ?**, tous les utilisateurs sont  sélectionnés par défaut, mais vous pouvez choisir Modifier pour sélectionner les groupes de sécurité que vous avez créés.
1. Pour terminer la création de la stratégie, choisissez **Ajouter**.
1. Dans la page **Ajouter une stratégie,** choisissez **Fermer.**
1. Dans la page d’accueil du Centre d’administration,  confirmez que votre nouvelle stratégie a été ajoutée en choisissant Stratégies et en l’avisant sur la page **Stratégies.**