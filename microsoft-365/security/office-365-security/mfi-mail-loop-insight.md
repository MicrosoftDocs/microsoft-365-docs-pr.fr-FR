---
title: Résoudre les problèmes de boucles de courrier possibles
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: cb801985-3c89-4979-9c18-17829a4cb563
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser la fonction de résolution des problèmes possibles dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance pour identifier et corriger les boucles de messagerie au sein de leur organisation.
ms.openlocfilehash: 1d49fd93b2ea068986e003b36077672215a2dd57
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920563"
---
# <a name="fix-possible-mail-loop-insight-in-the-security--compliance-center"></a><span data-ttu-id="ae6a6-103">Corriger les éventuelles boucles de courrier dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="ae6a6-103">Fix possible mail loop insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="ae6a6-104">Les boucles de messagerie sont incorrectes car :</span><span class="sxs-lookup"><span data-stu-id="ae6a6-104">Mail loops are bad because:</span></span>

- <span data-ttu-id="ae6a6-105">Ils perdent des ressources système.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-105">They waste system resources.</span></span>
- <span data-ttu-id="ae6a6-106">Ils consomment le quota de volume de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-106">They consume your organization's mail volume quota.</span></span>
- <span data-ttu-id="ae6a6-107">Ils envoient des notifications d’échec de remise confus (également appelées notifications de non-remise) aux expéditeurs des messages d’origine.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-107">They send confusing non-delivery reports (also known as NDRs or bounce messages) to the original message senders.</span></span>

<span data-ttu-id="ae6a6-108">La **fonctionnalité corriger la boucle de courrier possible** dans la zone **recommandé pour vous** du [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de [sécurité & conformité](https://protection.office.com) vous avertit lorsqu’une boucle de courrier est détectée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-108">The **Fix possible mail loop** insight in the **Recommended for you** area of the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) notifies you when a mail loop is detected in your organization.</span></span>

<span data-ttu-id="ae6a6-109">Cette vue ne s’affiche qu’une fois la condition détectée (si vous n’avez pas de boucles de courrier, vous ne verrez pas la vue d’ensemble).</span><span class="sxs-lookup"><span data-stu-id="ae6a6-109">This insight appears only after the condition is detected (if you don't have any mail loops, you won't see the insight).</span></span>

![Réparer le ralentissement des règles de flux de messagerie dans la zone recommandé pour vous du tableau de bord flux de messagerie](../../media/mfi-fix-possible-mail-loop.png)

<span data-ttu-id="ae6a6-111">Lorsque vous cliquez sur **afficher les détails** dans le widget, un lanceur apparaît avec davantage d’informations :</span><span class="sxs-lookup"><span data-stu-id="ae6a6-111">When you click **View details** on the widget, a flyout appears with more information:</span></span>

- <span data-ttu-id="ae6a6-112">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ae6a6-112">**Domain**</span></span>
- <span data-ttu-id="ae6a6-113">**Nombre de messages** : vous pouvez cliquer sur **afficher les exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un exemple de messages qui ont été affectés par la boucle.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-113">**Number of messages** : You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the messages that were affected by the loop.</span></span>
- <span data-ttu-id="ae6a6-114">**Type de domaine** «par exemple, faisant autorité ou ne faisant pas autorité.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-114">**Domain type** " For example, Authoritative or Non-authoritative.</span></span>
- <span data-ttu-id="ae6a6-115">**Enregistrement MX** : l’hôte ( **serveur de messagerie** ) et les valeurs de **priorité** de l’enregistrement MX pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-115">**MX record** : The host ( **Mail server** ) and **Priority** values of the MX record for the domain.</span></span>
- <span data-ttu-id="ae6a6-116">**Raison** de la boucle et **Comment corriger** : nous allons identifier les scénarios de boucle de courrier les plus courants et fournir les actions recommandées pour la résolution de la boucle.</span><span class="sxs-lookup"><span data-stu-id="ae6a6-116">**Loop reason** and **How to fix** : We'll identify the most common mail loop scenarios and provide recommended actions to fix the loop.</span></span>

![Fenêtre volante de détails qui apparaît après avoir cliqué sur Afficher les détails dans la boîte de message de correction possible](../../media/mfi-fix-possible-mail-loop-details.png)

## <a name="see-also"></a><span data-ttu-id="ae6a6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae6a6-118">See also</span></span>

<span data-ttu-id="ae6a6-119">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ae6a6-119">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
