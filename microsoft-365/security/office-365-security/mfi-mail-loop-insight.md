---
title: Corriger les éventuelles indications de boucle de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: cb801985-3c89-4979-9c18-17829a4cb563
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser la fonction de résolution des problèmes possibles dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance pour identifier et corriger les boucles de messagerie au sein de leur organisation.
ms.openlocfilehash: 54240cffc534b4be708492b37b827636edab280e
ms.sourcegitcommit: c04f1207cfaddac2a9abef38967c17d689756a96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2020
ms.locfileid: "46577621"
---
# <a name="fix-possible-mail-loop-insight-in-the-security--compliance-center"></a><span data-ttu-id="ff777-103">Corriger les éventuelles boucles de courrier dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="ff777-103">Fix possible mail loop insight in the Security & Compliance Center</span></span>

<span data-ttu-id="ff777-104">Une boucle de courrier est incorrecte car elle gaspille des ressources système, consomme le quota de volume de courrier de votre organisation et envoie des notifications d’échec de remise confuses (également appelées notifications de non-remise) aux expéditeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="ff777-104">A mail loop is bad because it wastes system resources, consumes your organization's mail volume quota, and sends confusing non-delivery reports (also known as NDRs or bounce messages) to the original senders.</span></span>

<span data-ttu-id="ff777-105">La **fonctionnalité corriger la boucle de courrier possible** dans la zone **recommandé pour vous** du [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité vous avertit lorsqu’une boucle de courrier est détectée dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff777-105">The **Fix possible mail loop** insight in the **Recommended for you** area of the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center notifies you when a mail loop is detected in your organization.</span></span> <span data-ttu-id="ff777-106">Cette vue ne s’affiche qu’une fois la condition détectée (si vous n’avez pas de boucles de courrier, vous ne verrez pas la vue d’ensemble).</span><span class="sxs-lookup"><span data-stu-id="ff777-106">This insight appears only after the condition is detected (if you don't have any mail loops, you won't see the insight).</span></span>

![Réparer le ralentissement des règles de flux de messagerie dans la zone recommandé pour vous du tableau de bord flux de messagerie](../../media/mfi-fix-possible-mail-loop.png)

<span data-ttu-id="ff777-108">Lorsque vous cliquez sur **afficher les détails** dans le widget, un lanceur apparaît avec davantage d’informations :</span><span class="sxs-lookup"><span data-stu-id="ff777-108">When you click **View details** on the widget, a flyout appears with more information:</span></span>

- <span data-ttu-id="ff777-109">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="ff777-109">**Domain**</span></span>
- <span data-ttu-id="ff777-110">**Nombre de messages**: vous pouvez cliquer sur **afficher les exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un exemple de messages qui ont été affectés par la boucle.</span><span class="sxs-lookup"><span data-stu-id="ff777-110">**Number of messages**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the messages that were affected by the loop.</span></span>
- <span data-ttu-id="ff777-111">**Type de domaine**«par exemple, faisant autorité ou ne faisant pas autorité.</span><span class="sxs-lookup"><span data-stu-id="ff777-111">**Domain type**" For example, Authoritative or Non-authoritative.</span></span>
- <span data-ttu-id="ff777-112">**Enregistrement MX**: l’hôte (**serveur de messagerie**) et les valeurs de **priorité** de l’enregistrement MX pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="ff777-112">**MX record**: The host (**Mail server**) and **Priority** values of the MX record for the domain.</span></span>
- <span data-ttu-id="ff777-113">**Raison** de la boucle et **Comment résoudre**: nous allons essayer d’identifier les scénarios de boucle de courrier les plus courants et de fournir les actions recommandées (le cas échéant) pour corriger la boucle.</span><span class="sxs-lookup"><span data-stu-id="ff777-113">**Loop reason** and **How to fix**: We'll try to identify the most common mail loop scenarios and provide the recommended actions (if available) to fix the loop.</span></span>

![Fenêtre volante de détails qui apparaît après avoir cliqué sur Afficher les détails dans la boîte de message de correction possible](../../media/mfi-fix-possible-mail-loop-details.png)

## <a name="related-topics"></a><span data-ttu-id="ff777-115">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="ff777-115">Related topics</span></span>

<span data-ttu-id="ff777-116">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ff777-116">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
