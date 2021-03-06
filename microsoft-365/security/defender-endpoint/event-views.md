---
title: Afficher les événements de la réduction de la surface d’attaque
description: Importer des affichages personnalisés pour voir les événements de réduction de la surface d’attaque.
keywords: affichage des événements, Exploit Guard, audit, révision, événements
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: f8de3d8b2d7c07f8d783ecbe85b7e4a9c612aae5
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985455"
---
# <a name="view-attack-surface-reduction-events"></a>Afficher les événements de la réduction de la surface d’attaque

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**S’applique à :**

- [Microsoft Defender pour point de terminaison](https://go.microsoft.com/fwlink/?linkid=2154037)
- [Microsoft 365 Defender](https://go.microsoft.com/fwlink/?linkid=2118804)

> [!TIP]
> Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ? [Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)

Examinez les événements de réduction de la surface d’attaque dans l’Observateur d’événements pour surveiller les règles ou paramètres qui fonctionnent. Vous pouvez également déterminer si des paramètres sont trop « bruyants » ou ont un impact sur votre flux de travail quotidien.

La révision des événements est pratique lorsque vous évaluez les fonctionnalités. Vous pouvez activer le mode audit pour les fonctionnalités ou les paramètres, puis passer en revue ce qui se serait passé s’ils étaient entièrement activés.

Cet article répertorie tous les événements, leurs fonctionnalités ou paramètres associés, et explique comment créer des affichages personnalisés pour filtrer des événements spécifiques.

Obtenez des rapports détaillés sur les événements, les blocs et les avertissements dans le cadre de Sécurité Windows si vous avez un abonnement E5 et que vous utilisez [Microsoft Defender pour endpoint](microsoft-defender-endpoint.md).

## <a name="use-custom-views-to-review-attack-surface-reduction-capabilities"></a>Utiliser des affichages personnalisés pour examiner les fonctionnalités de réduction de la surface d’attaque

Créez des affichages personnalisés dans Windows’observateur d’événements pour voir uniquement les événements pour des fonctionnalités et des paramètres spécifiques. Le moyen le plus simple consiste à importer un affichage personnalisé en tant que fichier XML. Vous pouvez copier le XML directement à partir de cette page.

Vous pouvez également accéder manuellement à la zone d’événement correspondant à la fonctionnalité.

### <a name="import-an-existing-xml-custom-view"></a>Importer une vue personnalisée XML existante

1. Créez un fichier .txt vide et copiez le fichier XML de l’affichage personnalisé que vous souhaitez utiliser dans .txt fichier. Faites-le pour chacun des affichages personnalisés que vous souhaitez utiliser. Renommez les fichiers comme suit (assurez-vous de modifier le type de .txt à .xml) :
    - Affichage personnalisé des événements d’accès contrôlé aux *dossiers :cfa-events.xml*
    - Vue personnalisée des événements Exploit Protection *:ep-events.xml*
    - Vue personnalisée des événements de réduction de la surface *d’attaque :asr-events.xml*
    - Affichage personnalisé des événements réseau/protection *:np-events.xml*

2. Tapez **l’Observateur** d’événements menu Démarrer et ouvrez **l’Observateur d’événements.**

3. Sélectionner **l’affichage**  >  **personnalisé d’importation d’action...**

  > [!div class="mx-imgBorder"]
  > ![Animation mettant en surbrillance l’importation d’une vue personnalisée à gauche de la fenêtre visionneuse even](images/events-import.gif)

4. Accédez à l’endroit où vous avez extrait le fichier XML pour l’affichage personnalisé que vous souhaitez, puis sélectionnez-le.

5. Sélectionnez **Ouvrir**.

6. Il crée un affichage personnalisé qui filtre pour afficher uniquement les événements liés à cette fonctionnalité.

### <a name="copy-the-xml-directly"></a>Copier directement le XML

1. Tapez **l’Observateur** d’événements menu Démarrer et ouvrez l’observateur Windows **événements.**

2. Dans le panneau gauche, sous **Actions,** **sélectionnez Créer un affichage personnalisé...**

  > [!div class="mx-imgBorder"]
  > ![Animation mettant en surbrillance l’option créer un affichage personnalisé dans la fenêtre de l’Observateur d’événements](images/events-create.gif)

3. Go to the XML tab and select **Edit query manually**. Vous verrez un avertissement vous signalant que vous  ne pouvez pas modifier la requête à l’aide de l’onglet Filtre si vous utilisez l’option XML. Sélectionnez **Oui**.

4. Collez le code XML de la fonctionnalité dont vous souhaitez filtrer les événements dans la section XML.

5. Sélectionnez **OK**. Spécifiez un nom pour votre filtre. Cela crée un affichage personnalisé qui filtre pour afficher uniquement les événements liés à cette fonctionnalité.

### <a name="xml-for-attack-surface-reduction-rule-events"></a>XML pour les événements de règle de réduction de la surface d’attaque

```xml
<QueryList>
  <Query Id="0" Path="Microsoft-Windows-Windows Defender/Operational">
   <Select Path="Microsoft-Windows-Windows Defender/Operational">*[System[(EventID=1121 or EventID=1122 or EventID=5007)]]</Select>
   <Select Path="Microsoft-Windows-Windows Defender/WHC">*[System[(EventID=1121 or EventID=1122 or EventID=5007)]]</Select>
  </Query>
</QueryList>
```

### <a name="xml-for-controlled-folder-access-events"></a>XML pour les événements d’accès contrôlé aux dossiers

```xml
<QueryList>
  <Query Id="0" Path="Microsoft-Windows-Windows Defender/Operational">
   <Select Path="Microsoft-Windows-Windows Defender/Operational">*[System[(EventID=1123 or EventID=1124 or EventID=5007)]]</Select>
   <Select Path="Microsoft-Windows-Windows Defender/WHC">*[System[(EventID=1123 or EventID=1124 or EventID=5007)]]</Select>
  </Query>
</QueryList>
```

### <a name="xml-for-exploit-protection-events"></a>XML pour les événements Exploit Protection

```xml
<QueryList>
  <Query Id="0" Path="Microsoft-Windows-Security-Mitigations/KernelMode">
   <Select Path="Microsoft-Windows-Security-Mitigations/KernelMode">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Concurrency">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Contention">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Messages">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Operational">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Power">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Render">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/Tracing">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Win32k/UIPI">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="System">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
   <Select Path="Microsoft-Windows-Security-Mitigations/UserMode">*[System[Provider[@Name='Microsoft-Windows-Security-Mitigations' or @Name='Microsoft-Windows-WER-Diag' or @Name='Microsoft-Windows-Win32k' or @Name='Win32k'] and ( (EventID &gt;= 1 and EventID &lt;= 24)  or EventID=5 or EventID=260)]]</Select>
  </Query>
</QueryList>
```

### <a name="xml-for-network-protection-events"></a>XML pour les événements de protection réseau

```xml
<QueryList>
 <Query Id="0" Path="Microsoft-Windows-Windows Defender/Operational">
  <Select Path="Microsoft-Windows-Windows Defender/Operational">*[System[(EventID=1125 or EventID=1126 or EventID=5007)]]</Select>
  <Select Path="Microsoft-Windows-Windows Defender/WHC">*[System[(EventID=1125 or EventID=1126 or EventID=5007)]]</Select>
 </Query>
</QueryList>
```

## <a name="list-of-attack-surface-reduction-events"></a>Liste des événements de réduction de la surface d’attaque

Tous les événements de réduction de la surface d’attaque se trouvent sous **Journaux** des applications et des services > Microsoft > Windows puis le dossier ou le fournisseur répertoriés dans le tableau suivant.

Vous pouvez accéder à ces événements dans l Windows’observateur d’événements :

1. Ouvrez le menu **Démarrer** et tapez **l’Observateur** d’événements, puis sélectionnez le résultat de **l’Observateur d’événements.**
2. Développez **Journaux** des applications et des services > Microsoft > Windows puis allez dans le dossier répertorié sous **Fournisseur/source** dans le tableau ci-dessous.
3. Double-cliquez sur le sous-élément pour voir les événements. Faites défiler les événements pour trouver celui que vous recherchez.

   ![Animation montrant l’utilisation de l’Observateur d’événements](images/event-viewer.gif)

Fonctionnalité | Fournisseur/source | ID de l'événement | Description
:-|:-|:-:|:-
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 1 | Audit ACG
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 2 | Appliquer ACG
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 3 | Ne pas autoriser l’audit des processus enfants
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 4  | Ne pas autoriser le blocage des processus enfants
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 5  | Bloquer l’audit des images à faible intégrité
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 6  | Bloquer le bloc d’images à faible intégrité
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 7  | Bloquer l’audit des images distantes
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 8  | Bloquer le bloc d’images distantes
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 9  | Désactiver l’audit des appels système win32k
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 10 | Désactiver le bloc d’appels système win32k
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 11 | Audit de protection de l’intégrité du code
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 12  | Bloc de protection de l’intégrité du code
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 13 | Audit EAF
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 14  | Appliquer EAF
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 15 | Audit EAF+
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 16  | Appliquer EAF+
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 17  | Audit IAF
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 18  | Application IAF
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 19 | Audit StackPivot ROP
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 20 | Appliquer StackPivot ROP
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) |  21 | Audit ROP CallerCheck
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 22 | ROP CallerCheck enforce
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 23 | Audit SimExec ROP
Exploit Protection | Security-Mitigations (mode noyau/mode utilisateur) | 24 | Appliquer SimExec ROP
Exploit Protection | WER-Diagnostics | 5  | Bloc CFG
Exploit Protection | Win32K (opérationnel) | 260 | Police nontrusted
Protection du réseau | Windows Defender (opérationnel) | 5007 | Événement lorsque les paramètres sont modifiés
Protection du réseau | Windows Defender (opérationnel) | 1125 | Événement lorsque la protection du réseau se déclenche en mode Audit
Protection du réseau | Windows Defender (opérationnel) | 1126 | Événement lorsque la protection du réseau se déclenche en mode blocage
Accès contrôlé aux dossiers | Windows Defender (opérationnel) | 5007 | Événement lorsque les paramètres sont modifiés
Accès contrôlé aux dossiers | Windows Defender (opérationnel) | 1124 | Événement d’accès contrôlé aux dossiers audité
Accès contrôlé aux dossiers | Windows Defender (opérationnel) | 1123 | Événement d’accès contrôlé aux dossiers bloqué
Accès contrôlé aux dossiers | Windows Defender (opérationnel) | 1127 | Événement de bloc d’écriture du secteur d’accès contrôlé aux dossiers bloqué
Accès contrôlé aux dossiers | Windows Defender (opérationnel) | 1128 | Événement de bloc d’écriture de secteur d’accès contrôlé aux dossiers audité
Réduction de la surface d'attaque | Windows Defender (opérationnel) | 5007 | Événement lorsque les paramètres sont modifiés
Réduction de la surface d'attaque | Windows Defender (opérationnel) | 1122 | Événement lorsque la règle se déclenche en mode audit
Réduction de la surface d'attaque | Windows Defender (opérationnel) | 1121 | Événement lorsque la règle se déclenche en mode blocage
