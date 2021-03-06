---
title: Étape 1. Trier et analyser votre premier incident
description: Comment trier et commencer l’analyse de votre premier incident Microsoft 365 Defender.
keywords: incidents, alertes, examiner, corrélation, attaque, ordinateurs, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365, réponse aux incidents, cyber-attaque
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 82e1d1b117fd8c68077a249a14f66b9915d517e9
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53287770"
---
# <a name="step-1-triage-and-analyze-your-first-incident"></a>Étape 1. Trier et analyser votre premier incident

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

**S’applique à :**
- Microsoft 365 Defender

À mesure que vous consacrez du temps à établir, implémenter et maintenir des mesures de sécurité conformément aux normes de l’organisation, vous pouvez configurer des solutions de sécurité pour vous aider à identifier rapidement les risques et menaces de sécurité. Microsoft 365 Defender vous permet de détecter, de trier et d’examiner les incidents par le biais de son expérience à volet unique où vous pouvez trouver les informations dont vous avez besoin pour prendre des décisions en temps voulu.

Une fois qu’un incident de sécurité est détecté, Microsoft 365 Defender présente les détails dont vous aurez besoin pour trier ou hiérarchiser un incident ou des incidents par rapport à d’autres. Après avoir déterminé la définition des priorités, les analystes peuvent alors se concentrer sur l’étude des cas qui leur sont attribués.

## <a name="detection-by-microsoft-365-defender"></a>Détection par Microsoft 365 Defender

Microsoft 365 Defender reçoit des alertes et des événements de plusieurs plateformes de sécurité Microsoft en tant que sources de détection pour créer une image globale et un contexte d’activité malveillante. Voici les sources de détection possibles :

- [Microsoft Defender pour le](../defender-endpoint/microsoft-defender-endpoint.md) point de terminaison est une solution protection évolutive des points de terminaison (PEPT) qui utilise l’antivirus Microsoft Defender, ainsi que la protection avancée contre les menaces dans le cloud à l’aide de Microsoft Security Graph. Defender pour point de terminaison est une plateforme unifiée pour la protection préventive, la détection post-violation, l’examen automatisé et la réponse. Il protège les points de terminaison contre les cybermenaces, détecte les attaques avancées et les violations de données, automatise les incidents de sécurité et améliore la posture de sécurité.
- [Microsoft Defender pour](/defender-for-identity/what-is) l’identité est une solution de sécurité basée sur le cloud qui utilise vos signaux AD DS (Active Directory Domain Services) locaux pour identifier, détecter et examiner les menaces avancées, les identités compromises et les actions internes malveillantes dirigées contre votre organisation.
- [Microsoft Cloud App Security](/cloud-app-security/) agit comme un garde d’accès en temps réel entre les utilisateurs de votre entreprise et les ressources cloud qu’ils utilisent, où que soient vos utilisateurs et quel que soit l’appareil qu’ils utilisent.
- [Microsoft Defender pour Office 365](../office-365-security/overview.md) votre organisation contre les menaces malveillantes dans les messages électroniques, les liens (URL) et les outils de collaboration.
- [Azure Security Center](/azure/security-center/security-center-introduction) est un système de gestion de la sécurité de l’infrastructure unifiée qui renforce la posture de sécurité de vos centres de données et fournit une protection avancée contre les menaces sur vos charges de travail hybrides dans le cloud ainsi que sur site.

Dans Microsoft 365 Defender, [les incidents sont identifiés](incidents-overview.md) en corrélant les alertes à partir de ces différentes sources de détection. Au lieu de passer des ressources en chaîne ou de distinguer plusieurs alertes dans leurs incidents respectifs, vous pouvez commencer par la file d’attente des incidents Microsoft 365 Defender immédiatement. Cela vous permet de trier efficacement les incidents entre les points de terminaison, les identités, le courrier électronique et les applications, et de réduire les dommages d’une attaque.

## <a name="triage-your-incidents"></a>Trier vos incidents

La réponse aux incidents Microsoft 365 Defender commence une fois que vous avez trié la liste des incidents à l’aide de la méthode recommandée de hiérquisation de votre organisation. Pour trier, il faut affecter un niveau d’importance ou d’urgence aux incidents, ce qui détermine ensuite l’ordre dans lequel ils seront examinés.

Un exemple de guide utile pour déterminer l’incident à hiérarchiser dans Microsoft 365 Defender peut être résumé par la formule : *Gravité + Impact = Priorité*.

- **La gravité est** le niveau désigné par Microsoft 365 Defender et ses composants de sécurité intégrés.
- **L’impact** est déterminé par l’organisation et inclut généralement, mais sans s’y limiter, un nombre seuil d’utilisateurs, d’appareils, de services affectés (ou une combinaison d’entre eux) et même un type d’alerte.

Les analystes lancent ensuite des enquêtes basées sur **les** critères de priorité définis par l’organisation.

Les priorités des incidents peuvent varier en fonction de l’organisation. NIST recommande également de prendre en compte l’impact fonctionnel et informationnel de l’incident et la récupérabilité.

Voici une approche de tri :

1. Go to the [incidents](incidents-overview.md) page to initiate triage. Vous pouvez voir ici une liste des incidents affectant votre organisation. Par défaut, ils sont organisés du plus récent au plus ancien incident. À partir de là, vous pouvez également voir différentes colonnes pour chaque incident indiquant, entre autres, leur gravité, leur catégorie, le nombre d’alertes actives et les entités impactées. Vous pouvez personnaliser l’ensemble des colonnes et trier la file d’attente des incidents en sélectionnant le nom de la colonne. Vous pouvez également filtrer la file d’attente des incidents en fonction de vos besoins. Pour obtenir la liste complète des filtres disponibles, voir [Hiérarchiser les incidents.](incident-queue.md#available-filters)

   :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-queue.png" alt-text="Exemple de file d’attente d’incident":::

    Un exemple de la façon dont vous pouvez effectuer le tri pour cet ensemble d’incidents consiste à hiérarchiser les incidents qui ont affecté davantage d’utilisateurs et d’appareils. Dans cet exemple, vous pouvez hiérarchiser l’ID d’incident 6769, car il a affecté le plus grand nombre d’entités : 7 appareils, 6 utilisateurs et 2 boîtes aux lettres. En outre, l’incident semble contenir des alertes de Microsoft Defender pour l’identité qui indiquent une alerte basée sur l’identité et un vol possible d’informations d’identification.

   :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-high-impact.png" alt-text="Exemple d’incident à fort impact":::

2. Sélectionnez le cercle en de côté du nom de l’incident pour passer en revue les détails. Un volet latéral s’affiche sur le côté droit, qui contient des informations supplémentaires qui peuvent aider davantage votre tri.

   :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-incident-flyout.png" alt-text="Exemple de volet latéral d’incident":::

   Par exemple, en regardant les tactiques [MITRE ATT&CK](https://attack.mitre.org/) utilisées par l’attaquant en fonction des catégories de l’incident, vous pouvez hiérarchiser cet incident car l’attaquant a utilisé des informations d’identification volées, des commandes et contrôles établis, effectué des mouvements latérals et exfiltré certaines données. Cela suggère que l’attaquant a déjà été profondeur dans le réseau et éventuellement volé des informations confidentielles.

   En outre, si votre organisation a implémenté l’infrastructure Confiance zéro, vous considérerez l’accès aux informations d’identification comme une violation de sécurité importante qui vaut la peine d’être hiér donc.

   En faisant défiler le volet latéral vers le bas, vous verrez les entités spécifiquement impactées, telles que les utilisateurs, les appareils et les boîtes aux lettres. Vous pouvez vérifier le niveau d’exposition de chaque appareil et les propriétaires des boîtes aux lettres concernées.

   :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-incident-flyout-details.png" alt-text="Exemple de détails du volet latéral d’incident":::

3. Plus bas dans le volet latéral, vous pouvez trouver les alertes associées. Microsoft 365 Defender a déjà effectué la corrélation de ces alertes en un seul incident, ce qui vous permet de gagner du temps et des ressources pour résoudre les attaques. Les alertes sont des événements système suspects et, par conséquent, potentiellement malveillants, qui suggèrent la présence d’une personne malveillante sur un réseau.

   Dans cet exemple, 87 alertes individuelles ont été déterminées comme faisant partie d’un incident de sécurité. Vous pouvez afficher toutes les alertes pour obtenir un aperçu rapide de la façon dont l’attaque s’est joué.

   :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-incident-flyout-alerts.png" alt-text="Exemple d’alertes dans un volet latéral d’incident":::

## <a name="analyze-your-first-incident"></a>Analyser votre premier incident

Il est également important de comprendre le contexte qui entoure les alertes. Souvent, une alerte n’est pas un événement indépendant unique. Il existe une chaîne de processus créés, de commandes et d’actions qui n’ont peut-être pas eu lieu en même temps. Par conséquent, un analyste doit rechercher les première et dernière activités de l’entité suspecte dans les chronologies des appareils pour comprendre le contexte des alertes.

Il existe plusieurs façons de lire et d’analyser des données à l’aide de Microsoft 365 Defender mais l’objectif final pour les analystes est de répondre aux incidents aussi rapidement que possible. Bien Microsoft 365 Defender réduire considérablement le temps moyen de correction [(MTTR)](https://www.microsoft.com/security/blog/2020/05/04/lessons-learned-microsoft-soc-part-3c/) par le biais de la fonctionnalité d’investigation et de réponse automatisée de pointe du secteur, il existe toujours des cas qui nécessitent une analyse manuelle. [](m365d-autoir.md)

Voici un exemple :

1. Une fois la priorité de tri déterminée, un analyste lance une analyse approfondie en sélectionnant le nom de l’incident. Cette page affiche le résumé de **l’incident** dans lequel les données sont affichées dans des onglets pour faciliter l’analyse. Sous **l’onglet Alertes,** le type d’alertes s’affiche. Les analystes peuvent cliquer sur chaque alerte pour descendre dans la source de détection respective.

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-summary-tab.png" alt-text="Exemple de l’onglet Résumé d’un incident":::

    Pour obtenir un guide rapide sur le domaine que couvre chaque source de détection, examinez la section [Détecter](#detection-by-microsoft-365-defender) de cet article.

2. À partir de **l’onglet Alertes,** un analyste peut pivoter vers la source de détection pour effectuer une analyse et un examen plus approfondis. Par exemple, si vous sélectionnez détection de programmes malveillants Microsoft Cloud App Security comme source de détection, l’analyste est ajouté à sa page d’alerte correspondante.

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-select-alert.png" alt-text="Exemple de sélection d’une alerte d’incident":::

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-link-to-mcas.png" alt-text="Exemple de page correspondante dans Microsoft Cloud App Security":::

3. Pour examiner notre exemple plus en détail, faites défiler vers le bas de la page pour afficher les **utilisateurs concernés.** Pour voir l’activité et le contexte qui entourent la détection de programmes malveillants, sélectionnez la page de l’utilisateur d’An dernier.

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-user-page.png" alt-text="Exemple de page d’utilisateur":::

4. La page de l’utilisateur affiche une liste chronologique des événements commençant par une sign-in risquée à partir d’une alerte d’adresse IP du réseau *TOR.* Bien que le caractère suspect d’une activité dépend de la nature de la façon dont une organisation effectue ses activités, dans la plupart des cas, l’utilisation du routeur de déplacement (TOR), un réseau qui permet aux utilisateurs de parcourir le web de manière anonyme, dans un environnement d’entreprise peut être considérée comme hautement peu probable et inutile pour les opérations en ligne normales.

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-user-event-list.png" alt-text="Exemple de liste chronologique des événements pour un utilisateur":::

5. Chaque alerte peut être sélectionnée pour obtenir plus d’informations sur l’activité. Par exemple, la sélection de **l’activité à partir** d’une alerte d’adresse IP tor vous conduit à la propre page de cette alerte. An elle est administrateur de Office 365, ce qui signifie qu’elle dispose de privilèges élevés et que l’incident source a pu avoir conduit à l’accès à des informations confidentielles.

    :::image type="content" source="../../media/first-incident-analyze/first-incident-analyze-mcas-alert.png" alt-text="Exemple de détails d’alertes pour Microsoft Cloud App Security":::

6. En sélectionnant d’autres alertes, un analyste peut obtenir une image complète de l’attaque.

## <a name="next-step"></a>Étape suivante

[![Étape 2 : Découvrez comment résoudre les incidents](../../media/first-incident-overview/first-incident-path-step2.png)](first-incident-remediate.md)

Découvrez comment corriger [les incidents.](first-incident-remediate.md)

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des incidents](incidents-overview.md)
- [Enquêter sur des incidents](investigate-incidents.md)
- [Gérer les incidents](manage-incidents.md)
