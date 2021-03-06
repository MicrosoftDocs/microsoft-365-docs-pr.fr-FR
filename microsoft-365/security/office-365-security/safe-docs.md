---
title: Documents sécurisés dans Microsoft Defender pour Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.reviewer: kshi
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez comment Coffre documents dans Microsoft 365 E5 ou Microsoft 365 E5 Sécurité.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 0e1bd2150a04e51e0d06c6cd1c17a71a032df1a5
ms.sourcegitcommit: ebb1c3b4d94058a58344317beb9475c8a2eae9a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53108606"
---
# <a name="safe-documents-in-microsoft-365-e5"></a>Documents sécurisés dans Microsoft 365 E5

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

**S’applique à**
- [Microsoft 365 Defender](../defender/microsoft-365-defender.md)

Coffre Les documents sont une fonctionnalité de Microsoft 365 E5 ou de Microsoft 365 E5 Sécurité qui utilise [Microsoft Defender](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour [](https://support.microsoft.com/office/d6f09ac7-e6b9-4495-8e43-2bbcdbcb6653) le point de terminaison pour analyser les documents et les fichiers ouverts en affichage protégé ou Application Guard [pour Office](https://support.microsoft.com/topic/9e0fb9c2-ffad-43bf-8ba3-78f785fdba46).

## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Coffre Les documents sont disponibles uniquement pour les *utilisateurs Microsoft 365 E5* ou *Microsoft 365 E5 Sécurité* licences. Ces licences ne sont pas incluses dans Microsoft Defender pour Office 365 plans.

- Coffre Les documents sont pris en charge Applications Microsoft 365 pour les grandes entreprises (anciennement Office 365 ProPlus) version 2004 ou ultérieure.

- Vous ouvrez le Portail Microsoft 365 Defender sur <https://security.microsoft.com>. Pour aller directement à la page **Coffre pièces jointes,** utilisez <https://security.microsoft.com/safeattachmentv2> .

- Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell).

- Vous avez besoin d’autorisations **Exchange Online** pour pouvoir suivre les procédures de cet article :
  - Pour configurer les Coffre Documents, vous devez être membre  des groupes de rôles Gestion de l’organisation ou **Administrateur** de la sécurité.
  - Pour accéder en lecture seule aux paramètres Coffre Documents, vous  devez être  membre des groupes de rôles Lecteur global ou Lecteur de sécurité.

  Pour plus d'informations, voir [Permissions en échange en ligne](/exchange/permissions-exo/permissions-exo).

  > [!NOTE]
  >
  > - L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises _et_ les autorisations pour les autres fonctionnalités de Microsoft 365. Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).
  >
  > - Le groupe de rôles **Gestion de l’organisation en affichage seul** dans [Exchange Online](/Exchange/permissions-exo/permissions-exo#role-groups) permet également d’accéder en lecture seule à la fonctionnalité.

### <a name="how-does-microsoft-handle-your-data"></a>Comment Microsoft gère-t-il vos données ?

Pour vous protéger, Coffre Documents envoie des fichiers au cloud [Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection) pour analyse. Pour plus d’informations sur la façon dont Microsoft Defender pour le point de terminaison gère vos données, voir : Microsoft Defender pour le stockage et la confidentialité des données de [point de terminaison.](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)

Les fichiers envoyés par Coffre Documents ne sont pas conservés dans Defender au-delà du temps nécessaire à l’analyse (généralement, moins de 24 heures).

## <a name="use-the-microsoft-365-defender-to-configure-safe-documents"></a>Utiliser la Microsoft 365 Defender pour configurer les documents Coffre documents

1. Ouvrez le portail Microsoft 365 Defender et  allez à la section Stratégies de collaboration & de messagerie & règles de stratégies de menaces dans la \>  \>  \>  section \> **Stratégies Coffre pièces jointes.**

2. Dans la page **Coffre pièces jointes,** cliquez **sur Paramètres globaux.**

3. Dans le **volant des paramètres globaux** qui s’affiche, configurez les paramètres suivants :
   - **Activer Coffre documents** pour Office clients : déplacez le basculement vers la droite pour activer la fonctionnalité : ![ Activer/ ](../../media/scc-toggle-on.png) Activer.
   - Autoriser les utilisateurs à cliquer dans le affichage protégé, même si **Coffre Documents a** identifié le fichier comme malveillant : nous vous recommandons de laisser cette option désactivée (laissez le bouton bascule vers la gauche : Bascule). ![ ](../../media/scc-toggle-off.png)

   Lorsque vous avez terminé, cliquez sur **Enregistrer**.

   ![Coffre Documents settings after selecting Global settings on the Coffre Attachments page.](../../media/safe-docs-global-settings.png)

### <a name="use-exchange-online-powershell-to-configure-safe-documents"></a>Utiliser Exchange Online PowerShell pour configurer Coffre Documents

Utilisez la syntaxe suivante :

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs <$true | $false> -AllowSafeDocsOpen <$true | $false>
```

- Le _paramètre EnableSafeDocs_ active ou désactive Coffre Documents pour l’ensemble de l’organisation.
- Le _paramètre AllowSafeDocsOpen_ permet ou empêche les utilisateurs de quitter le affichage protégé (c’est-à-dire, l’ouverture du document) si le document a été identifié comme malveillant.

Cet exemple active Coffre documents pour l’ensemble de l’organisation et empêche les utilisateurs d’ouvrir des documents qui ont été identifiés comme malveillants en affichage protégé.

```powershell
Set-AtpPolicyForO365 -EnableSafeDocs $true -AllowSafeDocsOpen $false
```

Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Set-AtpPolicyForO365](/powershell/module/exchange/set-atppolicyforo365).

### <a name="onboard-to-the-microsoft-defender-for-endpoint-service-to-enable-auditing-capabilities"></a>Intégration au service Microsoft Defender for Endpoint pour activer les fonctionnalités d’audit

Pour déployer Microsoft Defender pour endpoint, vous devez passer par les différentes phases de déploiement. Après l’intégration, vous pouvez configurer les fonctionnalités d’audit dans Microsoft 365 Defender portail.

Pour plus d’informations, [voir Intégrer au service Microsoft Defender for Endpoint.](/microsoft-365/security/defender-endpoint/onboarding) Si vous avez besoin d’aide supplémentaire, reportez-vous à Résoudre les problèmes d’intégration de Microsoft Defender pour les points [de terminaison.](/microsoft-365/security/defender-endpoint/troubleshoot-onboarding)

### <a name="how-do-i-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vérifier que vous avez activé et configuré Coffre Documents, faites l’une des étapes suivantes :

- Dans le portail Microsoft 365 Defender, consultez la page Stratégies de collaboration de messagerie **&** stratégies de & Règles de stratégies de \>  \>  \>  menaces section \> **Stratégies Coffre Paramètres** \>    globaux des pièces jointes, puis vérifiez que l’outil Activer les documents Coffre pour les clients Office et autoriser les utilisateurs à cliquer en affichage protégé même si Coffre Documents identifie le fichier comme des paramètres malveillants.

- Exécutez la commande suivante dans Exchange Online PowerShell et vérifiez les valeurs des propriétés :

  ```powershell
  Get-AtpPolicyForO365 | Format-List *SafeDocs*
  ```

- Les fichiers suivants sont disponibles pour tester la protection Coffre documents. Ces documents sont similaires au fichier EICAR.TXT pour tester les solutions antivirus et anti-programme malveillant. Les fichiers ne sont pas dangereux, mais ils déclenchent la protection Coffre documents.

  - [SafeDocsDemo.docx](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.docx)
  - [SafeDocsDemo.pptx](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.pptx)
  - [SafeDocsDemo.xlsx](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/SafeDocsDemo.xlsx)
