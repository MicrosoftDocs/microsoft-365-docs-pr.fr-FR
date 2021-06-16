---
title: Exemple de recherche avancée pour Microsoft Defender pour Office 365
description: Commencer à rechercher des menaces de courrier électronique à l’aide d’un chasse avancée
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, recherche, requête, télémétrie, détections personnalisées, schéma, kusto
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: d3ac49b4afde0951e7a034c5c11114afbc52c293
ms.sourcegitcommit: 1c11035dd4432e34603022740baef0c8f7ff4425
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2021
ms.locfileid: "52965143"
---
# <a name="advanced-hunting-example-for-microsoft-defender-for-office-365"></a><span data-ttu-id="96541-104">Exemple de recherche avancée pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="96541-104">Advanced hunting example for Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="96541-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="96541-105">**Applies to:**</span></span>
- <span data-ttu-id="96541-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="96541-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="96541-107">Souhaitez-vous commencer à rechercher des menaces d’e-mail à l’aide de la fonctionnalité de repérage avancé ?</span><span class="sxs-lookup"><span data-stu-id="96541-107">Want to get started searching for email threats using advanced hunting?</span></span> <span data-ttu-id="96541-108">Essayez ceci :</span><span class="sxs-lookup"><span data-stu-id="96541-108">Try this:</span></span>

<span data-ttu-id="96541-109">La section [Prise en main](/microsoft-365/security/office-365-security/defender-for-office-365#getting-started) de [l’article Microsoft Defender pour Office 365](/microsoft-365/security/office-365-security/defender-for-office-365) présente des blocs de configuration initiale logiques qui ressemblent à ceci :</span><span class="sxs-lookup"><span data-stu-id="96541-109">The [Getting Started](/microsoft-365/security/office-365-security/defender-for-office-365#getting-started) section of the [Microsoft Defender for Office 365 article](/microsoft-365/security/office-365-security/defender-for-office-365) has logical early configuration chunks that look like this:</span></span>

1. <span data-ttu-id="96541-110">Configurez tous les contrôles avec « Anti » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="96541-110">Configure everything with 'Anti' in the name.</span></span>
   - <span data-ttu-id="96541-111">Anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="96541-111">Anti-malware</span></span>
   - <span data-ttu-id="96541-112">Anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="96541-112">Anti-phishing</span></span>
   - <span data-ttu-id="96541-113">Anti-spam</span><span class="sxs-lookup"><span data-stu-id="96541-113">Anti-spam</span></span>
2. <span data-ttu-id="96541-114">Tout configurer avec « Safe » dans le nom.</span><span class="sxs-lookup"><span data-stu-id="96541-114">Set up everything with 'Safe' in the name.</span></span>
   - <span data-ttu-id="96541-115">Liens sûrs</span><span class="sxs-lookup"><span data-stu-id="96541-115">Safe Links</span></span>
   - <span data-ttu-id="96541-116">Pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="96541-116">Safe Attachments</span></span>
3. <span data-ttu-id="96541-117">Protégez les charges de travail (par exemple,</span><span class="sxs-lookup"><span data-stu-id="96541-117">Defend the workloads (ex.</span></span> <span data-ttu-id="96541-118">SharePoint En ligne, OneDrive et Teams).</span><span class="sxs-lookup"><span data-stu-id="96541-118">SharePoint Online, OneDrive, and Teams).</span></span>
4. <span data-ttu-id="96541-119">Protégez-vous avec une purge automatique nulle heure.</span><span class="sxs-lookup"><span data-stu-id="96541-119">Protect with zero-Hour auto purge.</span></span>

<span data-ttu-id="96541-120">Vous pouvez également utiliser un [Lien](../office-365-security/protect-against-threats.md) pour vous aider à vous lancer directement dans la configuration dès le premier jour.</span><span class="sxs-lookup"><span data-stu-id="96541-120">Along with a [link](../office-365-security/protect-against-threats.md) to jump right in and get configuration going on Day 1.</span></span>

<span data-ttu-id="96541-121">La dernière étape de la **Prise en main** consiste à protéger les utilisateurs grâce à la **Purge automatique à zéro heure**, également appelée ZAP.</span><span class="sxs-lookup"><span data-stu-id="96541-121">The last step in **Getting Started** is protecting users with **Zero-Hour auto purge**, also known as ZAP.</span></span> <span data-ttu-id="96541-122">Le fait de savoir si la purge automatique zéro heure d’un courrier malveillant, après la remise, est effective peut être très important.</span><span class="sxs-lookup"><span data-stu-id="96541-122">Knowing if your efforts to ZAP a suspicious or malicious mail, post-delivery, were successful can be very important.</span></span>

<span data-ttu-id="96541-123">La navigation rapide dans la langue de la requête Kusto pour repérer des problèmes est un avantage de la convergence de ces deux centres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="96541-123">Quickly navigating to Kusto query language to hunt for issues is an advantage of converging these two security centers.</span></span> <span data-ttu-id="96541-124">Les équipes de sécurité peuvent surveiller les manquées ZAP en suivant les étapes suivantes [ici,](https://security.microsoft.com/advanced-hunting)sous **Hunting** \> **Advanced Hunting**.</span><span class="sxs-lookup"><span data-stu-id="96541-124">Security teams can monitor ZAP misses by taking their next steps [here](https://security.microsoft.com/advanced-hunting), under **Hunting** \> **Advanced Hunting**.</span></span>

1. <span data-ttu-id="96541-125">Dans la page Recherche avancée, cliquez **sur Requête.**</span><span class="sxs-lookup"><span data-stu-id="96541-125">On the Advanced Hunting page, click **Query**.</span></span>
1. <span data-ttu-id="96541-126">Copiez la requête ci-dessous dans la fenêtre de requête.</span><span class="sxs-lookup"><span data-stu-id="96541-126">Copy the query below into the query window.</span></span>
1. <span data-ttu-id="96541-127">Sélectionnez **Exécuter la requête**.</span><span class="sxs-lookup"><span data-stu-id="96541-127">Select **Run query**.</span></span>

```kusto
EmailPostDeliveryEvents 
| where Timestamp > ago(7d)
//List malicious emails that were not zapped successfullyconverge-2-endpoints-new.png
| where ActionType has "ZAP" and ActionResult == "Error"
| project ZapTime = Timestamp, ActionType, NetworkMessageId , RecipientEmailAddress 
//Get logon activity of recipients using RecipientEmailAddress and AccountUpn
| join kind=inner IdentityLogonEvents on $left.RecipientEmailAddress == $right.AccountUpn
| where Timestamp between ((ZapTime-24h) .. (ZapTime+24h))
//Show only pertinent info, such as account name, the app or service, protocol, the target device, and type of logon
| project ZapTime, ActionType, NetworkMessageId , RecipientEmailAddress, AccountUpn, 
LogonTime = Timestamp, AccountDisplayName, Application, Protocol, DeviceName, LogonType
```

:::image type="content" source="../../media/converge-13-advanced-hunt-an-email-zap-new.png" alt-text="Page de recherche avancée (sous Chasse) avec requête sélectionnée en haut du panneau de requête et exécution d’une requête Kusto pour capturer les actions ZAP au cours des 7 derniers jours.":::

<span data-ttu-id="96541-129">Les données de cette requête s’affichent dans le panneau de résultats sous la requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="96541-129">The data from this query will appear in the results panel below the query itself.</span></span> <span data-ttu-id="96541-130">Les résultats incluent des informations telles que « DeviceName », « AccountDisplayName », et « ZapTime » dans un jeu de résultats personnalisable.</span><span class="sxs-lookup"><span data-stu-id="96541-130">Results include information like 'DeviceName', 'AccountDisplayName', and 'ZapTime' in a customizable result set.</span></span> <span data-ttu-id="96541-131">Les résultats peuvent également être exportés pour vos enregistrements.</span><span class="sxs-lookup"><span data-stu-id="96541-131">Results can also be exported for your records.</span></span> <span data-ttu-id="96541-132">Si vous avez encore besoin de la requête, sélectionnez **Enregistrer** > **Enregistrer sous** et ajoutez la requête à votre liste de requêtes, vos partages, ou vos requêtes de la communauté.</span><span class="sxs-lookup"><span data-stu-id="96541-132">If the query is one you'll need again, select **Save** > **Save As** and add the query to your list of queries, shared, or community queries.</span></span>

## <a name="related-information"></a><span data-ttu-id="96541-133">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="96541-133">Related information</span></span>
- [<span data-ttu-id="96541-134">Meilleures pratiques de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="96541-134">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="96541-135">Vue d’ensemble - Recherche avancée</span><span class="sxs-lookup"><span data-stu-id="96541-135">Overview - Advanced hunting</span></span>](advanced-hunting-overview.md)
