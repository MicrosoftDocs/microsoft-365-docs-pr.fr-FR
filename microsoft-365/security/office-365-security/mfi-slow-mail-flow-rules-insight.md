---
title: Résoudre les règles de flux de messagerie lent
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le correctif lent les règles de flux de messagerie du centre de sécurité & Compliance Center pour identifier et corriger les règles de flux de messagerie inefficaces ou rompues (également appelées règles de transport) dans leur organisation.
ms.openlocfilehash: 6a2a3c42eadf3c621b34d2a21344eafd2618e669
ms.sourcegitcommit: b64f36d3873fa0041b24bec029deb73ccfdfdbac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48877536"
---
# <a name="fix-slow-mail-flow-rules-insight-in-the-security--compliance-center"></a><span data-ttu-id="e0658-103">Réparer le ralentissement des règles de flux de messagerie dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="e0658-103">Fix slow mail flow rules insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="e0658-104">Des règles inefficaces de flux de messagerie (également appelées règles de transport) peuvent entraîner des retards de flux de messagerie pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e0658-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="e0658-105">Cette vue d’État indique les règles de flux de messagerie qui ont un impact sur le flux de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e0658-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="e0658-106">Voici des exemples de ces types de règles :</span><span class="sxs-lookup"><span data-stu-id="e0658-106">Examples of these types of rules include:</span></span>

- <span data-ttu-id="e0658-107">Conditions utilisées par **est membre de** pour les grands groupes.</span><span class="sxs-lookup"><span data-stu-id="e0658-107">Conditions that use **Is member of** for large groups.</span></span>
- <span data-ttu-id="e0658-108">Conditions qui utilisent des critères de correspondance des expressions régulières complexes (Regex).</span><span class="sxs-lookup"><span data-stu-id="e0658-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>
- <span data-ttu-id="e0658-109">Conditions d’utilisation de l’archivage de contenu dans les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="e0658-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="e0658-110">Les **règles de flux de messagerie de résolution lente** dans la zone **recommandé pour vous** du [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de [sécurité & conformité](https://protection.office.com) vous avertit lorsqu’une règle de flux de messagerie prend trop de temps pour se terminer.</span><span class="sxs-lookup"><span data-stu-id="e0658-110">The **Fix slow mail flow rules** insight in the **Recommended for you** area of the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) notifies you when a mail flow rule is taking too long to complete.</span></span> <span data-ttu-id="e0658-111">Cette vue ne s’affiche qu’une fois la condition détectée (si vous n’avez pas de boucles de courrier, vous ne verrez pas la vue d’ensemble).</span><span class="sxs-lookup"><span data-stu-id="e0658-111">This insight appears only after the condition is detected (if you don't have any mail loops, you won't see the insight).</span></span>

<span data-ttu-id="e0658-112">Vous pouvez utiliser cette notification pour identifier et ajuster les règles de flux de messagerie afin de réduire les retards de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e0658-112">You can use this notification to help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Réparer le ralentissement des règles de flux de messagerie dans la zone recommandé pour vous du tableau de bord flux de messagerie](../../media/mfi-fix-slow-mail-flow-rules.png)

<span data-ttu-id="e0658-114">Lorsque vous cliquez sur **afficher les détails** dans le widget, un lanceur apparaît avec davantage d’informations :</span><span class="sxs-lookup"><span data-stu-id="e0658-114">When you click **View details** on the widget, a flyout appears with more information:</span></span>

- <span data-ttu-id="e0658-115">**Règle** : vous pouvez pointer sur le résumé pour afficher toutes les conditions, les exceptions et les actions de la règle.</span><span class="sxs-lookup"><span data-stu-id="e0658-115">**Rule** : You can hover over the summary to see all of the conditions, exceptions, and actions of the rule.</span></span> <span data-ttu-id="e0658-116">Vous pouvez cliquer sur le résumé pour modifier la règle dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="e0658-116">You can click on the summary to edit the rule in the Exchange admin center (EAC).</span></span>
- <span data-ttu-id="e0658-117">**Nombre de messages évalués** : vous pouvez cliquer sur **afficher les exemples de messages** pour afficher les résultats de [suivi](message-trace-scc.md) des messages pour un exemple de messages qui ont été affectés par la règle.</span><span class="sxs-lookup"><span data-stu-id="e0658-117">**Number of messages evaluated** : You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the messages that were affected by the rule.</span></span>
- <span data-ttu-id="e0658-118">**Temps moyen passé sur chaque message**</span><span class="sxs-lookup"><span data-stu-id="e0658-118">**Average time spent on each message**</span></span>
- <span data-ttu-id="e0658-119">**Temps médian passé sur un message** : valeur centrale séparant la partie supérieure de la moitié inférieure des données de temps.</span><span class="sxs-lookup"><span data-stu-id="e0658-119">**Median time spent on a message** : The middle value that separates the upper half from the lower half of time data.</span></span>

![Fenêtre volante de détails qui apparaît après avoir cliqué sur Afficher les détails dans la boîte de message Fix ralentissement des règles de flux de messagerie](../../media/mfi-fix-slow-mail-flow-rules-details.png)

<span data-ttu-id="e0658-121">Pour plus d’informations sur les conditions et les exceptions dans les règles de flux de messagerie dans Exchange Online, consultez la rubrique [mail Flow Rule conditions and exceptions (prédicats) in Exchange Online](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).</span><span class="sxs-lookup"><span data-stu-id="e0658-121">For more information about conditions and exceptions in mail flow rules in Exchange Online, see [Mail flow rule conditions and exceptions (predicates) in Exchange Online](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0658-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0658-122">Related topics</span></span>

<span data-ttu-id="e0658-123">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e0658-123">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
