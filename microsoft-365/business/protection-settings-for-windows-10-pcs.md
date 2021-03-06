---
title: Modifier ou créer des paramètres de protection des appareils pour Windows 10 PC
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
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: bd66c26c-73a4-45a8-8642-3ea4ee7cd89d
description: Découvrez les paramètres disponibles dans Microsoft 365 entreprise pour sécuriser Windows 10 appareils.
ms.openlocfilehash: 4859681d5e71a61b8a5dd58114bce899f485967a
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925316"
---
# <a name="edit-or-create-device-protection-settings-for-windows-10-pcs"></a>Modifier ou créer des paramètres de protection des appareils pour Windows 10 PC

Cet article s’applique aux Microsoft 365 Business Premium.

Une fois que vous avez configuré les paramètres de protection Windows par défaut sur la page d’installation, vous pouvez en ajouter de nouveaux qui s’appliquent à tous les utilisateurs ou à un ensemble d’utilisateurs. Vous pouvez également modifier les modifications que vous avez créées.

## <a name="create-protection-settings-for-windows-10-devices"></a>Créer des paramètres de protection pour Windows 10 appareils

Regardez une vidéo sur la façon de sécuriser Windows 10 appareils à l’Microsoft 365 Business Premium :
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/a5734146-620a-4cec-8618-536b3ca37972?autoplay=false]
  
1. Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>. 
2. Dans le navigation de gauche, choisissez **Ajouter des** \> **stratégies** \> **d’appareils.**
3. Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie. 
4. Sous **Type de stratégie**, sélectionnez **Configuration d'appareil Windows 10**.
5. Expand **Secure Windows 10 Devices** \> configure the settings how you would like. Pour plus d’informations, voir [Paramètres disponibles.](#available-settings) 
    
    Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut. 
    
    ![Add policy pane with Windows 10 Device configuration selected](../media/fa9e2dc2-7eae-4c96-af34-765a1f641ecf.png)
  
6. Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis recherchez le groupe qui obtiendra ces paramètres \> **Sélectionner**.
7. Enfin, sélectionnez **Terminé** pour enregistrer la stratégie et l'affecter à des appareils. 

## <a name="edit-windows-10-protection-settings"></a>Modifier les paramètres Windows 10 protection des données
 
1. Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.     
2. Dans le navigation  de gauche, sélectionnez \> **Stratégies d’appareils.**
1. Choisissez une stratégie d’Windows existante, puis **modifiez.**
1. Choose **Edit** next to a setting you want to change and then **Save**.

## <a name="available-settings"></a>Paramètres disponibles

Par défaut, tous les paramètres sont **Activés**. Les paramètres suivants sont disponibles.
  
Pour plus d’informations, voir Comment les fonctionnalités [de protection Microsoft 365 Premium mappés aux paramètres Intune](map-protection-features-to-intune-settings.md). 


|Paramètre  <br/> |Description  <br/> |
|:-----|:-----|
|Protéger les ordinateurs des virus et d'autres menaces à l'aide de l'antivirus Windows Defender  <br/> |L'antivirus Windows Defender doit être activé pour protéger les ordinateurs contre les risques liés à la connexion à internet.  <br/> |
|Protéger les ordinateurs contre les menaces web dans Microsoft Edge  <br/> |Active les paramètres Microsoft Edge qui protègent les utilisateurs contre les sites et téléchargements malveillants.  <br/> |
|Utiliser des règles qui réduisent la surface d'attaque des appareils  <br/> |Quand elle est activée, la réduction de la surface d'attaque aide à bloquer les actions et applications que les logiciels malveillants utilisent généralement pour contaminer des appareils. Ce paramètre est disponible uniquement si Antivirus Windows Defender est activé. Pour en savoir plus, voir [Réduire les surfaces d'attaque](/windows/security/threat-protection/microsoft-defender-atp/exploit-protection).  <br/> |
|Protéger les dossiers contre des menaces telles que des rançongiciels  <br/> |Ce paramètre utilise l'Accès contrôlé aux dossiers pour protéger les données de l'entreprise contre l'apport de modifications par des applications suspectes ou malveillantes, telles que les rançongiciels. L'apport de modifications aux dossiers protégés par des applications de ces types est bloqué. Ce paramètre est disponible uniquement si Antivirus Windows Defender est activé. Pour en [savoir plus, consultez](/mem/configmgr/protect/deploy-use/create-deploy-exploit-guard-policy#bkmk_CFA) Protéger les dossiers avec accès contrôlé aux dossiers.  <br/> |
|Empêcher l'accès réseau à du contenu potentiellement malveillant sur Internet  <br/> |Utilisez ce paramètre pour bloquer les connexions des utilisateurs sortants à des emplacements Internet de faible réputation qui peuvent héberger des tentatives d’hameçonnage, des attaques ou d’autres contenus malveillants. Ce paramètre n’est disponible que si Antivirus Windows Defender est définie sur **On**. Pour plus d’informations, [voir Protéger votre réseau.](/windows/security/threat-protection/windows-defender-antivirus/configure-real-time-protection-windows-defender-antivirus)  <br/> |
|Protéger les fichiers et dossiers sur PC contre un accès non autorisé avec BitLocker  <br/> |Bitlocker protège les données en chiffrant les disques durs de l'ordinateur, et protège contre l'exposition des données en cas de perte ou de vol. Pour plus d’informations, consultez la FAQ [sur Bitlocker.](/windows/security/information-protection/bitlocker/bitlocker-frequently-asked-questions)  <br/> |
|Autoriser les utilisateurs à télécharger des applications à partir du Microsoft Store  <br/> |Permet aux utilisateurs de télécharger et d'installer des applications à partir du Microsoft Store. Il peut s'agir de jeux ou d'outils de productivité, c'est pourquoi nous laissons ce paramètre **activé**, mais vous pouvez le désactiver pour plus de sécurité.  <br/> |
|Autoriser les utilisateurs à accéder à Cortana  <br/> |Cortana peut être très utile ! Cortana peut activer ou désactiver les paramètres pour vous, donner des instructions et vous assurer que vous êtes à l’heure pour les rendez-vous, donc nous tenez ce paramètre activé **par** défaut.  <br/> |
|Autoriser les utilisateurs à recevoir des conseils de Windows et des annonces de Microsoft  <br/> |Les conseils Windows peuvent être très pratiques et aident les utilisateurs lors du lancement de nouvelles fonctionnalités.  <br/> |
|Maintenir les appareils Windows 10 à jour automatiquement  <br/> |Permet d'assurer que les appareils Windows 10 reçoivent automatiquement les dernières mises à jour.  <br/> |
|Désactiver l'écran d'un appareil resté inactif pendant  <br/> |Permet d'assurer la protection des données d'entreprise lorsqu'un utilisateur est inactif. Il est possible qu'un utilisateur travaille dans un lieu public, par exemple un café, et s'éloigne ou soit distrait pendant un instant, laissant son appareil à la vue de tous. Ce paramètre vous permet de contrôler la durée pendant laquelle l'utilisateur peut être inactif avant l'extinction de l'écran.  <br/> |