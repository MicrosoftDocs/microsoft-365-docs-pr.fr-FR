---
title: Recherche et suppression de messages électroniques dans votre organisation
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 3526fd06-b45f-445b-aed4-5ebd37b3762a
description: Utilisez la fonctionnalité de recherche et de purge dans le Centre de sécurité et de conformité Microsoft 365 pour rechercher et supprimer un message électronique dans toutes les boîtes aux lettres de votre organisation.
ms.openlocfilehash: 95683ed5dc6cce8ff109976ebb0d13215593f046
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770708"
---
# <a name="search-for-and-delete-email-messages"></a>Rechercher et supprimer des messages électroniques

**Cet article est destiné aux administrateurs. Vous essayez de rechercher des éléments à supprimer dans votre boîte aux lettres ? Voir [Rechercher un message ou un élément avec la Recherche instantanée](https://support.office.com/article/69748862-5976-47b9-98e8-ed179f1b9e4d)**.

Vous pouvez utiliser la fonctionnalité de recherche de contenu pour rechercher et supprimer un message électronique dans toutes les boîtes aux lettres de votre organisation. Cela peut vous aider à trouver et supprimer des messages électroniques potentiellement dangereux ou à haut risque, tels que les suivants :

- Messages contenant des virus ou des pièces jointes dangereuses

- Messages de hameçonnage

- Messages qui contiennent des données sensibles

> [!CAUTION]
> La fonction Rechercher et vider est puissante et permet à toute personne qui reçoit les autorisations nécessaires de supprimer des messages électroniques dans des boîtes aux lettres de votre organisation.

## <a name="before-you-begin"></a>Avant de commencer

- Pour créer et exécuter une recherche de contenu, vous devez être membre du groupe de rôles **Gestionnaire eDiscovery** ou disposer du rôle **Recherche de conformité** dans le Centre de sécurité et de conformité. Pour supprimer des messages, vous devez être membre du groupe de rôles de **gestion de l’organisation** ou disposer du rôle de **Recherche et purge** dans Centre de sécurité et de conformité. Pour plus d’informations sur l’ajout d’utilisateurs à un groupe de rôles, consultez la rubrique [Attribuer des autorisations eDiscovery dans le Centre de sécurité et conformité](assign-ediscovery-permissions.md).

  > [!NOTE]
  > Le groupe du rôle **Gestion de l'organisation** existe dans Exchange Online et le Centre de sécurité et conformité. Ces groupes de rôles distincts donnent des autorisations différentes. Être membre de la **Gestion des organisations** dans Exchange Online n'octroie pas les autorisations requises pour supprimer des messages électroniques. Si le rôle **Recherche et purge** ne vous est pas attribué dans le Centre de sécurité et conformité (directement ou via un groupe de rôles tel que **Gestion de l’organisation**), vous recevrez une erreur à l’étape 3 lorsque vous exécuterez la cmdlet **New-ComplianceSearchAction** avec le message « Impossible de trouver un paramètre qui correspond au nom du paramètre « Purge ».

- Pour supprimer des messages, vous devez utiliser le centre de sécurité et conformité PowerShell. Pour des instructions sur la façon de se connecter, consultez [Etape 1](#step-1-connect-to-security--compliance-center-powershell).

- Un maximum de 10 éléments par boîte aux lettres peuvent être supprimés à la fois. Sachant que la fonction de recherche et suppression de messages est censée être un outil de réponse aux incidents, cette limite permet de s’assurer que les messages sont rapidement supprimés des boîtes aux lettres. Cette fonctionnalité n’est pas conçue pour nettoyer les boîtes aux lettres des utilisateurs.

- Le nombre maximal de boîtes aux lettres dans une recherche de contenus servant à supprimer des éléments à l’aide d’une action de recherche et de purge est de 50 000. Si la recherche de contenu (que vous créez à l’[Étape 2](#step-2-create-a-content-search-to-find-the-message-to-delete)) contient plus de 50 000 boîtes aux lettres, l’action de purge (que vous créez à l’Étape 3) échoue. Une recherche de plus de 50 000 boîtes aux lettres au cours d’une même recherche est probable, généralement lorsque la configuration de la recherche prend en compte toutes les boîtes aux lettres de votre organisation. Cette restriction s’applique même si moins de 50 000 boîtes aux lettres contiennent des éléments qui correspondent à la requête de recherche. Pour obtenir des instructions sur l’utilisation des filtres d’autorisation de recherche pour rechercher et vider des éléments de plus de 50 000 boîtes aux lettres, consultez la section [informations supplémentaires](#more-information).

- La procédure décrite dans cet article ne peut être utilisée que pour supprimer des éléments dans les boîtes aux lettres et dossiers publics Exchange Online. Vous ne pouvez pas l’utiliser pour supprimer du contenu de SharePoint ou de sites OneDrive Entreprise.

- Il n’est pas possible de supprimer les éléments de courrier d’un groupe de révision dans un cas Advanced eDiscovery à l’aide des procédures décrites dans cet article. Cela est dû au fait que les éléments d’un groupe de révision sont stockés dans un emplacement de stockage Azure, et non dans le service actif. Cela signifie qu’elles ne sont pas renvoyées par la recherche de contenu que vous créez à l’étape 1. Pour supprimer des éléments d’un groupe de révision, vous devez supprimer le cas Advanced eDiscovery qui contient l’entité de révision. Pour plus d’informations, consultez [Fermer ou supprimer un cas Advanced eDiscovery](close-or-delete-case.md).

## <a name="step-1-connect-to-security--compliance-center-powershell"></a>Étape 1 : connectez-vous au Centre de sécurité et conformité PowerShell

L’étape suivante consiste à se connecter au Centre de sécurité et conformité PowerShell de votre organisation. Pour consulter des instructions détaillées, voir [Se connecter au Centre de sécurité et conformité PowerShell](/powershell/exchange/connect-to-scc-powershell).

## <a name="step-2-create-a-content-search-to-find-the-message-to-delete"></a>Étape 2 : créer une Recherche de contenu pour rechercher les messages à supprimer

La seconde étape consiste à créer et exécuter une Recherche de contenu pour rechercher le message à supprimer des boîtes aux lettres de votre organisation. Vous pouvez créer la recherche à l’aide du Centre de sécurité et conformité Microsoft 365 ou en exécutant les cmdlets **New-ComplianceSearch** et **Start-ComplianceSearch** dans PowerShell Sécurité et conformité. Les messages qui correspondent à la requête pour cette recherche sont supprimés par l’exécution de la commande **New-ComplianceSearchAction -Purge** à l’[étape 3](#step-3-delete-the-message). Pour plus d’informations sur la création d’une Recherche de contenu et sur la configuration de requêtes de recherche, consultez les rubriques suivantes :

- [Recherche de contenu dans Office 365](content-search.md)

- [Requêtes par Mots clés pour la Recherche de contenu](keyword-queries-and-search-conditions.md)

- [New-ComplianceSearch](/powershell/module/exchange/New-ComplianceSearch)

- [Start-ComplianceSearch](/powershell/module/exchange/Start-ComplianceSearch)

> [!NOTE]
> Les emplacements de contenu qui font l’objet d’une Recherche de contenu créée à cette étape ne peuvent pas inclure de sites SharePoint ou OneDrive Entreprise. Vous pouvez inclure uniquement les boîtes aux lettres et les dossiers publics dans une Recherche de contenu qui sera utilisée pour envoyer des messages électroniques. Si la Recherche de contenu inclut des sites, vous recevez un message d’erreur à l’étape 3 lorsque vous exécutez le cmdlet **New-ComplianceSearchAction**.

### <a name="tips-for-finding-messages-to-remove"></a>Conseils pour la recherche des messages à supprimer

L’objectif de la requête de recherche est de concentrer les résultats de la recherche sur les messages que vous voulez supprimer. Voici quelques conseils :

- Si vous connaissez l’expression ou le texte exact utilisé dans l’objet du message, utilisez la propriété **Subject** dans la requête de recherche.

- Si vous connaissez la date (ou la plage de dates) exacte du message, incluez la propriété **Reçu** dans la requête de recherche.

- Si vous savez qui a envoyé le message, incluez la propriété **From** dans la requête de recherche.

- Prévisualisez les résultats de recherche pour vérifier que la recherche renvoie uniquement les messages que vous voulez supprimer.

- Utilisez les statistiques d’estimation de recherche (affichées dans le volet de détails de la recherche dans le Centre de sécurité et conformité Microsoft 365 ou à l’aide de la cmdlet [Get-ComplianceSearch](/powershell/module/exchange/get-compliancesearch)) pour obtenir le nombre total de résultats.

Voici deux exemples de requêtes pour rechercher des messages électroniques suspects.

- Cette requête renvoie les messages qui ont été reçus par les utilisateurs entre le 13 et le 14 avril 2016, et qui contiennent les mots « action » et « obligatoire » dans l’objet.

  ```powershell
  (Received:4/13/2016..4/14/2016) AND (Subject:'Action required')
  ```

- Cette requête renvoie les messages qui ont été envoyés par chatsuwloginsset12345@outlook.com et contenant l’expression exacte « Mettez à jour vos informations de compte » dans l’objet.

  ```powershell
  (From:chatsuwloginsset12345@outlook.com) AND (Subject:"Update your account information")
  ```

Voici un exemple d’utilisation d’une requête pour créer et démarrer une recherche en exécutant les applets de commande **New-ComplianceSearch** et **Start-ComplianceSearch** pour effectuer une recherche dans toutes les boîtes aux lettres de l’organisation :

```powershell
$Search=New-ComplianceSearch -Name "Remove Phishing Message" -ExchangeLocation All -ContentMatchQuery '(Received:4/13/2016..4/14/2016) AND (Subject:"Action required")'
Start-ComplianceSearch -Identity $Search.Identity
```

## <a name="step-3-delete-the-message"></a>Étape 3 : supprimer le message

Après avoir créé et affiné une Recherche de contenu pour renvoyer le message que vous souhaitez supprimer et que vous êtes connecté au Centre de sécurité et conformité PowerShell, la dernière étape consiste à exécuter le cmdlet **New-ComplianceSearchAction** pour supprimer le message. Vous pouvez supprimer le message de manière temporaire ou définitive. Un message supprimé de manière temporaire est déplacé vers le dossier éléments récupérables d’un utilisateur et conservé jusqu’à l’expiration de la période de rétention des éléments supprimés. Les messages supprimés définitivement sont marqués pour suppression définitive de la boîte aux lettres et sont supprimés définitivement la prochaine fois que la boîte aux lettres est traitée par l’Assistant Dossier géré. Si la récupération d’élément unique est activée pour la boîte aux lettres, les éléments supprimés définitivement seront supprimés définitivement après l’expiration de la période de rétention des éléments supprimés. Si une boîte aux lettres est suspendue, les messages supprimés sont conservés jusqu’à ce que la durée de conservation de l’élément arrive à expiration ou jusqu’à ce que la suspension de la boîte aux lettres soit supprimée.

Dans l’exemple suivant, la commande supprime temporairement les résultats de recherche renvoyés par une Recherche de contenu nommée « Supprimer le message d’hameçonnage ».

```powershell
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType SoftDelete
```

Pour supprimer définitivement les éléments renvoyés par la recherche de contenu « Supprimer le message d’hameçonnage », exécutez la commande suivante :

```powershell
New-ComplianceSearchAction -SearchName "Remove Phishing Message" -Purge -PurgeType HardDelete
```

Notez que lorsque vous exécutez la commande précédente pour supprimer des messages de façon temporaire ou définitive, la recherche spécifiée par le paramètre *SearchName* est la Recherche de contenu que vous avez créée à l’étape 1.

Pour plus d’informations, voir [New-ComplianceSearchAction](/powershell/module/exchange/New-ComplianceSearchAction).

## <a name="more-information"></a>Plus d’informations

- **Comment obtenir l’état de l’opération de recherche et de suppression ?**

  Exécutez la commande **Get-ComplianceSearchAction** pour obtenir l’état de l’opération de suppression. L’objet créé lorsque vous exécutez le cmdlet **New-ComplianceSearchAction** est nommé à l’aide de ce format : `<name of Content Search>_Purge`.

- **Que se passe-t-il lorsque vous avez supprimé un message ?**

  Un message qui a été supprimé avec  la commande `New-ComplianceSearchAction -Purge -PurgeType HardDelete` est déplacé vers le dossier de purges et ne peut pas être consulté par l’utilisateur. Une fois le message déplacé dans le dossier Purges, il est conservé pour une durée basée sur la période de rétention des éléments supprimés si la récupération d’élément unique est activée pour la boîte aux lettres. (Dans Microsoft 365, la récupération d’élément unique est activée par défaut lors de la création d’une nouvelle boîte aux lettres.) Une fois la période de rétention des éléments supprimés expirée, le message est marqué pour suppression définitive et sera purgé de Microsoft 365 la prochaine fois que l’Assistant Dossier géré le traitera.

  Si vous utilisez la commande `New-ComplianceSearchAction -Purge -PurgeType SoftDelete`, les messages sont déplacés vers le dossier Suppressions dans le dossier Eléments récupérables de l’utilisateur. Il n’est pas immédiatement purgé de Microsoft 365. L’utilisateur peut récupérer les messages dans le dossier Éléments supprimés pendant une durée basée sur la période de rétention des éléments supprimés configurée pour la boîte aux lettres. Après expiration de cette période de rétention (ou si l’utilisateur purge le message avant son expiration), le message est déplacé vers le dossier Purges et n’est plus accessible par l’utilisateur. Une fois dans le dossier Purges, le message est conservé pour une durée basée sur la période de rétention des éléments supprimés configurée pour la boîte aux lettres si la récupération d’élément unique est activée pour la boîte aux lettres. (Dans Microsoft 365, la récupération d’élément unique est activée par défaut lors de la création d’une nouvelle boîte aux lettres.) Une fois la période de rétention des éléments supprimés expirée, le message est marqué pour suppression définitive et sera purgé de Microsoft 365 la prochaine fois que l’Assistant Dossier géré le traitera.

- **Comment faire pour supprimer un message de plus de 50 000 boîtes aux lettres ?**

  Comme indiqué précédemment, vous pouvez effectuer une opération de recherche et de purge sur un maximum de 50 000 boîtes aux lettres (même si moins de 50 000 boîtes au lettres contiennent des éléments qui correspondent à la requête de recherche). Si vous devez effectuer une opération de recherche et de purge sur plus de 50 000 boîtes aux lettres, envisagez de créer des filtres d’autorisations de recherche temporaires pour réduire le nombre de boîtes aux lettres recherchées à moins de 50 000. Par exemple, si votre organisation contient des boîtes aux lettres dans différents services ou localisations, vous pouvez créer un filtre d’autorisations de recherche de boîte aux lettres sur la base de l’une de ces propriétés de boîte aux lettres pour effectuer une recherche dans un sous-ensemble de boîtes aux lettres de votre organisation. Une fois que vous avez créé le filtre des autorisations de recherche, vous devez créer la recherche (décrite à l’étape 1), puis supprimer le message (décrit à l’étape 3). Vous pouvez ensuite modifier le filtre pour rechercher et vider les messages dans un autre groupe de boîtes aux lettres. Pour plus d’informations sur la création de filtres d'autorisation de recherche, voir [Configurer le filtrage des autorisations pour la Recherche de contenu](permissions-filtering-for-content-search.md).

- **Les éléments non indexés inclus dans les résultats de recherche seront-ils supprimés ?**

  Non, la commande New-ComplianceSearchAction-Purge ne supprime pas les éléments non indexés.

- **Que se passe-t-il si un message est supprimé d’une boîte aux lettres qui a été placée en conservation inaltérable ou en conservation pour litige ou fait l’objet d’une stratégie de rétention Microsoft 365 ?**

  Une fois le message supprimé et déplacé vers le dossier de purges, le message est conservé jusqu’à l’expiration de la durée de conservation. Si la durée de la conservation est illimitée, les éléments sont conservés jusqu’à la suppression de la conservation ou la modification de la durée de la conservation.

- **Pourquoi le flux de travail de recherche et suppression est-il réparti entre différents groupes de rôles du Centre de sécurité et conformité ?**

  Comme indiqué précédemment, un utilisateur doit être membre du groupe de rôles de gestionnaire de découverte électronique ou disposer du rôle de gestion de recherche de conformité pour effectuer des recherches dans des boîtes aux lettres. Pour supprimer des messages, un utilisateur doit être membre du groupe de rôles de gestion de l’organisation ou disposer du rôle de gestion de recherche et de purge. Il est ainsi possible de déterminer qui peut consulter des boîtes aux lettres dans l’organisation et qui peut supprimer des messages. 
