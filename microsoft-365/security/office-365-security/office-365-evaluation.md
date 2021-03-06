---
title: Évaluer Microsoft Defender pour Office 365
description: Defender for Office 365 en mode d’évaluation crée Defender pour les stratégies de messagerie Office 365 qui enregistrent les verdicts, tels que les programmes malveillants, mais n’agissent pas sur les messages.
keywords: évaluer Office 365, Microsoft Defender pour Office 365, évaluation d’Office 365, essayer Office 365, Microsoft Defender, Microsoft Defender pour le point de terminaison
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
ms.date: 04/21/2021
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 79d736330a40d33f5334196d165e72f487b6d959
ms.sourcegitcommit: 6749455c52b0f98a92f6fffbc2bb86caf3538bd8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53194780"
---
# <a name="evaluate-microsoft-defender-for-office-365"></a>Évaluer Microsoft Defender pour Office 365

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

> [!IMPORTANT]
> Microsoft Defender pour l Office 365 d’évaluation est en prévisualisation publique. Cette version préliminaire est fournie sans contrat de niveau de service. Certaines fonctionnalités peuvent ne pas être pris en charge ou avoir des fonctionnalités contraintes.

La conduite d’une évaluation approfondie du produit de sécurité peut vous aider à prendre des décisions éclairées sur les mises à niveau et les achats. Il permet d’essayer les fonctionnalités du produit de sécurité pour évaluer comment il peut aider votre équipe en charge des opérations de sécurité dans ses tâches quotidiennes.

L’expérience d’évaluation de [Microsoft Defender](defender-for-office-365.md) pour Office 365 est conçue pour éliminer la complexité de la configuration de l’appareil et de l’environnement afin que vous pouvez vous concentrer sur l’évaluation des fonctionnalités de Microsoft Defender pour Office 365. Avec le mode d’évaluation, tous les messages envoyés Exchange Online boîtes aux lettres peuvent être évalués sans pointer les enregistrements MX vers Microsoft. La fonctionnalité s’applique uniquement à la protection de la messagerie et non à Office clients tels que Word, SharePoint ou Teams.

Si vous n’avez pas encore de licence qui prend en charge Microsoft Defender pour Office 365, vous pouvez démarrer une évaluation gratuite de [30](https://admin.microsoft.com/AdminPortal/Home#/catalog/offer-details/microsoft-defender-for-office-365-plan-2-/223860DC-15D6-42D9-A861-AE05473069FA) jours et tester les fonctionnalités dans le portail Microsoft 365 Defender sur <https://security.microsoft.com> . Vous pourrez profiter de la mise en place rapide et la désactiver facilement si nécessaire.

> [!NOTE]
> Si vous êtes dans le portail Microsoft 365 Defender ( ), vous pouvez démarrer une évaluation defender pour Office 365 ici : Email <https://security.microsoft.com> **& Collaboration** Policies \> **& Rules** Threat \> **policies** page \> **Others** section \> **Evaluation mode**.

## <a name="how-the-evaluation-works"></a>Fonctionnement de l’évaluation

Defender for Office 365 en mode d’évaluation crée Defender pour les stratégies de messagerie Office 365 qui enregistrent les verdicts, tels que les programmes malveillants, mais n’agissent pas sur les messages. Vous n’êtes pas obligé de modifier la configuration de votre enregistrement MX.

Avec le mode d’évaluation, Coffre pièces [jointes,](safe-attachments.md)des liens [](set-up-anti-phishing-policies.md#impersonation-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)  [Coffre](safe-links.md)et des stratégies d’emprunt d’identité basées sur l’intelligence des boîtes aux lettres sont définies en votre nom. Toutes les stratégies defender Office 365 sont créées en mode non d’application en arrière-plan et ne sont pas visibles pour vous.

Dans le cadre de l’installation, le mode d’évaluation configure également [le filtrage amélioré pour les connecteurs.](/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/enhanced-filtering-for-connectors) Il améliore la précision du filtrage en conservant l’adresse IP et les informations de l’expéditeur, qui sont sinon perdues lorsque le courrier passe par une passerelle de sécurité de messagerie (ESG) devant Defender pour Office 365. Le filtrage amélioré pour les connecteurs améliore également la précision du filtrage pour vos stratégies anti-courrier indésirable et anti-hameçonnage Exchange Online Protection (EOP) existantes.

Le filtrage amélioré pour les connecteurs améliore la précision du filtrage, mais peut modifier la livrabilité de certains messages si vous disposez d’un ESG devant Defender pour Office 365 et que vous ne contournez actuellement pas le filtrage EOP. L’impact est limité aux stratégies EOP ; Defender for Office 365 stratégies définies dans le cadre de l’évaluation sont créées en mode non d’application. Pour minimiser l’impact potentiel sur la production, vous pouvez contourner tout filtrage EOP en créant une règle de flux de messagerie (également appelée règle de transport) pour définir le niveau de confiance du courrier indésirable (SCL) des messages sur -1. Voir Utiliser des règles de flux de messagerie pour définir le niveau de confiance du courrier indésirable [(SCL)](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-set-scl)dans les messages Exchange Online   pour plus d’informations.

Lorsque le mode d’évaluation est installé, vous avez un rapport mis à jour quotidiennement avec jusqu’à 90 jours de données quantifiant les messages qui auraient été bloqués si les stratégies étaient implémentées (par exemple, supprimer, envoyer en courrier indésirable, mettre en quarantaine). Des rapports sont générés pour toutes les détections Defender Office 365 et EOP. Elles sont agrégées par technologie de détection (par exemple, l’emprunt d’identité) et peuvent être filtrées par plage de temps. En outre, les rapports de messages peuvent être créés à la demande pour créer des tableaux croisés dynamiques personnalisés ou pour des messages de profondeur à l’aide de l’Explorateur.

Grâce à l’expérience de mise en place simplifiée, vous pouvez vous concentrer sur :

- Exécution de l’évaluation
- Obtention d’un rapport détaillé
- Analyse du rapport pour l’action
- Présentation du résultat de l’évaluation

## <a name="before-you-begin"></a>Avant de commencer

### <a name="licensing"></a>Licence

Pour accéder à l’évaluation, vous devez respecter les exigences de licence. L’une des licences suivantes fonctionne :

- Microsoft Defender pour Office 365 Plan 1
- Microsoft Defender pour Office 365 Plan 2
- Microsoft 365 E5, Microsoft 365 E5 Sécurité
- Office 365 E5

Si vous n’avez pas l’une de ces licences, vous devez obtenir une licence d’essai.

#### <a name="trial"></a>Version d’évaluation

Pour obtenir une licence d’essai pour Microsoft Defender pour  Office 365, vous devez avoir le rôle d’administrateur de facturation ou d’administrateur **global.** Demandez l’autorisation d’une personne qui a le rôle d’administrateur global. [En savoir plus sur les abonnements et les licences](../../commerce/licenses/subscriptions-and-licenses.md)

Une fois que vous avez le rôle approprié, le chemin d’accès recommandé consiste à obtenir une licence d’essai pour Microsoft Defender pour Office 365 (Plan 2) dans le Centre d’administration Microsoft 365 en allant à Facturation > Acheter des services. La version d’essai inclut un essai gratuit de 30 jours pour 25 licences. [Obtenez une version d’essai de Microsoft Defender pour Office 365 (Plan 2).](https://admin.microsoft.com/AdminPortal/Home#/catalog/offer-details/microsoft-defender-for-office-365-plan-2-/223860DC-15D6-42D9-A861-AE05473069FA)

Vous aurez une fenêtre de 30 jours avec l’évaluation pour surveiller et signaler les menaces avancées. Vous avez également la possibilité d’acheter un abonnement payant si vous souhaitez obtenir l’intégralité de Defender Office 365 fonctionnalités.

### <a name="roles"></a>Rôles

**Exchange Online rôles sont requis** pour configurer Defender pour Office 365 en mode d’évaluation. L’attribution d Microsoft 365 de conformité ou d’administration de la sécurité ne fonctionne pas.

- [En savoir plus sur les autorisations dans Exchange Online](/exchange/permissions-exo/permissions-exo)
- [En savoir plus sur l’attribution de rôles d’administrateur](../../admin/add-users/assign-admin-roles.md)

Les rôles suivants sont nécessaires :

|Tâche|Rôle (dans Exchange Online)|
|---|---|
|Obtenir un essai gratuit ou acheter Microsoft Defender pour Office 365 (Plan 2)|Rôle d’administrateur de facturation OU rôle d’administrateur global|
|Créer une stratégie d’évaluation|Rôle Domaines distants et acceptés ; Rôle d’administrateur de sécurité|
|Modifier la stratégie d’évaluation|Rôle Domaines distants et acceptés ; Rôle d’administrateur de sécurité|
|Supprimer la stratégie d’évaluation|Rôle Domaines distants et acceptés ; Rôle d’administrateur de sécurité |
|Afficher le rapport d’évaluation|Rôle d’administrateur de sécurité OU rôle lecteur sécurité|
|

### <a name="enhanced-filtering"></a>Filtrage amélioré

Vos stratégies Exchange Online Protection de courrier indésirable, telles que la protection en bloc et le courrier indésirable, resteront les mêmes. Toutefois, l’évaluation permet d’améliorer le filtrage des connecteurs, ce qui peut avoir un impact sur votre flux de messagerie et Exchange Online Protection stratégies à moins d’être contourné.

Le filtrage amélioré pour les connecteurs permet aux locataires d’utiliser la protection contre l’usurpation d’usurpation d’accès. La protection contre l’usurpation d’adresse n’est pas prise en charge si vous utilisez une passerelle de sécurité de messagerie (ESG) sans avoir désactivé le filtrage amélioré pour les connecteurs.

### <a name="urls"></a>URL

Les URL sont détonées pendant le flux de messagerie. Si vous ne souhaitez pas que des URL spécifiques détonent, gérez votre liste d’URL autorisées de manière appropriée. Pour [plus d’informations, voir](tenant-allow-block-list.md) Gérer la liste d’attente des locataires.

Les liens d’URL dans les corps des messages électroniques ne seront pas encapsulés, afin de réduire l’impact sur les clients.

### <a name="email-routing"></a>Routage du courrier électronique

Préparez les détails correspondants dont vous aurez besoin pour configurer la façon dont votre courrier électronique est actuellement acheminé, y compris le nom du connecteur entrant qui a acheminé votre courrier électronique. Si vous utilisez simplement Exchange Online Protection, vous n’avez pas de connecteur.  [En savoir plus sur le flux de messagerie et le routage du courrier électronique](/office365/servicedescriptions/exchange-online-service-description/mail-flow)

Les scénarios de routage de courrier pris en charge sont les suivants :

- Partenaire tiers **et/ou** fournisseur de services local : le connecteur entrant que vous souhaitez évaluer utilise un fournisseur tiers et/ou vous utilisez une solution pour la sécurité du courrier électronique en local.
- **Microsoft Exchange Online protection** uniquement : le client que vous souhaitez évaluer utilise Office 365 pour la sécurité du courrier électronique et l’enregistrement MX (Mail Exchange) pointe vers Microsoft.

### <a name="email-security-gateway"></a>Passerelle de sécurité du courrier électronique

Si vous utilisez une passerelle de sécurité de messagerie (ESG) tierce, vous devez connaître le nom du fournisseur. Si vous utilisez un fournisseur ESG local ou non pris en charge, vous devez connaître les adresses IP publiques des appareils.

Les partenaires tiers pris en charge sont les suivants :

- Barracuda
- IronPort
- Mimecast
- Proofpoint
- Sophos
- Symantec
- Trend Micro

### <a name="scoping"></a>Étendue

Vous serez en mesure d’élargir l’étendue de l’évaluation à un connecteur entrant. Si aucun connecteur n’est configuré, l’étendue d’évaluation permettra aux administrateurs de collecter des données auprès d’un utilisateur de votre client pour évaluer Defender pour Office 365.

## <a name="get-started-with-the-evaluation"></a>Mise en place de l’évaluation

Recherchez la carte de Office 365 d’évaluation Microsoft Defender dans le portail Microsoft 365 Defender ( ) à partir de <https://security.microsoft.com> trois points d’accès :

- **Points de terminaison** \> **Gestion des vulnérabilités** \> **Tableau de bord** ( <https://security.microsoft.com/tvm_dashboard> )
- **Collaboration par & messagerie** \> **Stratégies & règles** \> **Stratégies de menace** ( <https://security.microsoft.com/threatpolicy> )
- **Rapports** \> **Collaboration par & messagerie** \> **Email & collaboration reports** ( <https://security.microsoft.com/emailandcollabreport> )

## <a name="setting-up-the-evaluation"></a>Configuration de l’évaluation

Une fois que vous avez commencé le flux de mise en place pour votre évaluation, deux options de routage s’offrent à vous. En fonction des besoins de configuration et d’évaluation du routage du courrier de votre organisation, vous pouvez choisir si vous utilisez un fournisseur de services tiers et/ou local ou uniquement Microsoft Exchange Online.

- Si vous utilisez un partenaire tiers et/ou un fournisseur de services local, vous devez sélectionner le nom du fournisseur dans le menu déroulant. Fournissez les autres détails liés au connecteur.

- Sélectionnez Microsoft Exchange Online si l’enregistrement MX pointe vers Microsoft et si vous avez une boîte Exchange Online lettres.

Examinez vos paramètres et modifiez-les si nécessaire. Ensuite, **sélectionnez Créer une évaluation.** Vous devez obtenir un message de confirmation pour indiquer que votre mise en place est terminée.

Votre rapport d’évaluation Office 365 Microsoft Defender pour entreprise est généré une fois par jour. Le traitement des données peut prendre jusqu’à 24 heures.

### <a name="exchange-mail-flow-rules-optional"></a>Exchange de flux de messagerie (facultatif)

Si vous avez une passerelle existante, l’activation du mode d’évaluation active le filtrage amélioré pour les connecteurs. Cette fonctionnalité améliore la précision du filtrage en modifiant l’adresse IP de l’expéditeur entrant. Cette fonctionnalité peut modifier les verdicts de filtre et, si vous ne contournez pas Exchange Online Protection, cela peut modifier la livrabilité de certains messages. Dans ce cas, vous pouvez ignorer temporairement le filtrage pour analyser l’impact. Pour contourner le filtrage, ouvrez le Centre d’administration Exchange (EAC) et créez une règle de flux de messagerie qui définit le SCL des messages sur -1 (si vous n’en avez pas <https://admin.exchange.microsoft.com> déjà). Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour définir le niveau de confiance du courrier indésirable [(SCL)](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-set-scl)dans les messages Exchange Online .

## <a name="evaluate-capabilities"></a>Évaluer les fonctionnalités

Une fois le rapport d’évaluation généré, consultez le nombre de liens vers les menaces avancées, de pièces jointes de menaces avancées et d’emprunts d’identité potentiels identifiés dans les e-mails et les espaces de travail de collaboration de votre organisation.

Une fois la version d’essai expirée, vous pouvez continuer à accéder au rapport pendant 90 jours. Toutefois, il ne collecte plus d’informations. Si vous souhaitez continuer à utiliser Microsoft Defender pour Office 365 une fois que votre version d’essai a expiré, assurez-vous d’acheter un abonnement payant pour [Microsoft Defender pour Office 365 (Plan 2).](https://admin.microsoft.com/AdminPortal/Home#/catalog/offer-details/microsoft-defender-for-office-365-plan-2-/223860DC-15D6-42D9-A861-AE05473069FA)

Vous pouvez vous **Paramètres** pour mettre à jour votre routage ou désactiver votre évaluation à tout moment. Toutefois, vous devez à nouveau passer par le même processus de mise en place si vous décidez de poursuivre votre évaluation après l’avoir désactivée.

## <a name="provide-feedback"></a>Envoyer des commentaires

Vos commentaires nous aident à mieux protéger votre environnement contre les attaques avancées. Partagez votre expérience et vos impressions sur les fonctionnalités du produit et les résultats de l’évaluation.

Sélectionnez **Nous faire part** de vos commentaires pour nous faire part de vos commentaires.
