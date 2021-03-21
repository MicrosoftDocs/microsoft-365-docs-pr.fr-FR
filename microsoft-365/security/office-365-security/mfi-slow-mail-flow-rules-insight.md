---
title: Résoudre les règles de flux de messagerie lent
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser l’aperçu corriger les règles de flux de messagerie lent dans le Centre de sécurité & conformité pour identifier et corriger les règles de flux de messagerie inefficaces ou rompues (également appelées règles de transport) dans leur organisation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 22ce3549077ad9b358165245159393d3e25e61c8
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50924105"
---
# <a name="fix-slow-mail-flow-rules-insight-in-the-security--compliance-center"></a><span data-ttu-id="43d61-103">Résoudre les problèmes de règles de flux de messagerie dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="43d61-103">Fix slow mail flow rules insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="43d61-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="43d61-104">**Applies to**</span></span>
- [<span data-ttu-id="43d61-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="43d61-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="43d61-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="43d61-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="43d61-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="43d61-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="43d61-108">Des règles de flux de messagerie inefficaces (également appelées règles de transport) peuvent entraîner des retards de flux de messagerie pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43d61-108">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="43d61-109">Cette information signale les règles de flux de messagerie qui ont un impact sur le flux de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43d61-109">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="43d61-110">Voici quelques exemples de ces types de règles :</span><span class="sxs-lookup"><span data-stu-id="43d61-110">Examples of these types of rules include:</span></span>

- <span data-ttu-id="43d61-111">Conditions qui **utilisent est membre de pour** les grands groupes.</span><span class="sxs-lookup"><span data-stu-id="43d61-111">Conditions that use **Is member of** for large groups.</span></span>
- <span data-ttu-id="43d61-112">Conditions qui utilisent une correspondance complexe de modèle d’expression régulière (regex).</span><span class="sxs-lookup"><span data-stu-id="43d61-112">Conditions that use complex regular expression (regex) pattern matching.</span></span>
- <span data-ttu-id="43d61-113">Conditions qui utilisent la vérification du contenu dans les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="43d61-113">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="43d61-114">L’aperçu des règles de  correction du flux [](mail-flow-insights-v2.md) de messagerie lent dans la zone Recommandé pour vous du tableau de bord de flux de messagerie dans le Centre de sécurité [&](https://protection.office.com) conformité vous avertit lorsqu’une règle de flux de messagerie prend trop de temps. </span><span class="sxs-lookup"><span data-stu-id="43d61-114">The **Fix slow mail flow rules** insight in the **Recommended for you** area of the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) notifies you when a mail flow rule is taking too long to complete.</span></span>

<span data-ttu-id="43d61-115">Cette information apparaît uniquement après la détection de la condition (si vous n’avez pas de boucles de messagerie, vous ne verrez pas l’aperçu).</span><span class="sxs-lookup"><span data-stu-id="43d61-115">This insight appears only after the condition is detected (if you don't have any mail loops, you won't see the insight).</span></span>

<span data-ttu-id="43d61-116">Vous pouvez utiliser cette notification pour vous aider à identifier et affiner les règles de flux de messagerie afin de réduire les retards de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="43d61-116">You can use this notification to help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Résoudre les problèmes de règles de flux de messagerie dans la zone Recommandé pour vous du tableau de bord de flux de messagerie](../../media/mfi-fix-slow-mail-flow-rules.png)

<span data-ttu-id="43d61-118">Lorsque vous cliquez **sur Afficher les détails** sur le widget, un flyout s’affiche avec plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="43d61-118">When you click **View details** on the widget, a flyout appears with more information:</span></span>

- <span data-ttu-id="43d61-119">**Règle**: vous pouvez pointer sur le résumé pour voir toutes les conditions, les exceptions et les actions de la règle.</span><span class="sxs-lookup"><span data-stu-id="43d61-119">**Rule**: You can hover over the summary to see all of the conditions, exceptions, and actions of the rule.</span></span> <span data-ttu-id="43d61-120">Vous pouvez cliquer sur le résumé pour modifier la règle dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="43d61-120">You can click on the summary to edit the rule in the Exchange admin center (EAC).</span></span>
- <span data-ttu-id="43d61-121">**Nombre de messages évalués**: vous pouvez [](message-trace-scc.md) cliquer sur Afficher les exemples de **messages** pour afficher les résultats du suivi des messages pour un échantillon des messages affectés par la règle.</span><span class="sxs-lookup"><span data-stu-id="43d61-121">**Number of messages evaluated**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the messages that were affected by the rule.</span></span>
- <span data-ttu-id="43d61-122">**Temps moyen passé sur chaque message**</span><span class="sxs-lookup"><span data-stu-id="43d61-122">**Average time spent on each message**</span></span>
- <span data-ttu-id="43d61-123">**Temps moyen passé sur un message**: valeur intermédiaire qui sépare la moitié supérieure de la moitié inférieure des données de temps.</span><span class="sxs-lookup"><span data-stu-id="43d61-123">**Median time spent on a message**: The middle value that separates the upper half from the lower half of time data.</span></span>

![Volant détails qui s’affiche après avoir cliqué sur Afficher les détails sur l’aperçu des règles de flux de messagerie lent](../../media/mfi-fix-slow-mail-flow-rules-details.png)

<span data-ttu-id="43d61-125">Pour plus d’informations sur les conditions et les exceptions dans les règles de flux de messagerie, voir Conditions et exceptions des règles de flux de messagerie [(prédicats) dans Exchange Online.](/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions)</span><span class="sxs-lookup"><span data-stu-id="43d61-125">For more information about conditions and exceptions in mail flow rules, see [Mail flow rule conditions and exceptions (predicates) in Exchange Online](/Exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).</span></span>

## <a name="see-also"></a><span data-ttu-id="43d61-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43d61-126">See also</span></span>

<span data-ttu-id="43d61-127">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="43d61-127">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>