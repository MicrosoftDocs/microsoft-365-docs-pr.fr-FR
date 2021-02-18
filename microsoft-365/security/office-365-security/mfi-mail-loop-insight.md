---
title: Résoudre les problèmes de boucles de courrier possibles
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: cb801985-3c89-4979-9c18-17829a4cb563
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser l’aperçu de la boucle de courrier de correction possible dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour identifier et corriger les boucles de messagerie dans leur organisation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 7fde0041dfb9901cb0a327eafec78d98a40b4cb9
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50290560"
---
# <a name="fix-possible-mail-loop-insight-in-the-security--compliance-center"></a><span data-ttu-id="dab01-103">Résoudre les problèmes de boucle de messagerie dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="dab01-103">Fix possible mail loop insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="dab01-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="dab01-104">**Applies to**</span></span>
- [<span data-ttu-id="dab01-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="dab01-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="dab01-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="dab01-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="dab01-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dab01-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="dab01-108">Les boucles de messagerie sont mauvaises car :</span><span class="sxs-lookup"><span data-stu-id="dab01-108">Mail loops are bad because:</span></span>

- <span data-ttu-id="dab01-109">Ils perdent les ressources système.</span><span class="sxs-lookup"><span data-stu-id="dab01-109">They waste system resources.</span></span>
- <span data-ttu-id="dab01-110">Ils utilisent le quota de volume de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dab01-110">They consume your organization's mail volume quota.</span></span>
- <span data-ttu-id="dab01-111">Ils envoient des rapports de non-remise déroutants (également appelés messages de non-remise ou de non-remise) aux expéditeurs du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="dab01-111">They send confusing non-delivery reports (also known as NDRs or bounce messages) to the original message senders.</span></span>

<span data-ttu-id="dab01-112">L’aperçu de la  boucle de courrier de [](mail-flow-insights-v2.md) correction possible dans la zone Recommandé pour vous du tableau de bord de flux de messagerie dans le Centre de sécurité & conformité vous [avertit](https://protection.office.com) lorsqu’une boucle de messagerie est détectée dans votre organisation. </span><span class="sxs-lookup"><span data-stu-id="dab01-112">The **Fix possible mail loop** insight in the **Recommended for you** area of the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) notifies you when a mail loop is detected in your organization.</span></span>

<span data-ttu-id="dab01-113">Cette information apparaît uniquement après la détection de la condition (si vous n’avez pas de boucles de messagerie, vous ne verrez pas l’aperçu).</span><span class="sxs-lookup"><span data-stu-id="dab01-113">This insight appears only after the condition is detected (if you don't have any mail loops, you won't see the insight).</span></span>

![Résoudre les problèmes de règles de flux de messagerie dans la zone Recommandé pour vous du tableau de bord de flux de messagerie](../../media/mfi-fix-possible-mail-loop.png)

<span data-ttu-id="dab01-115">Lorsque vous cliquez **sur Afficher les détails** sur le widget, un flyout s’affiche avec plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="dab01-115">When you click **View details** on the widget, a flyout appears with more information:</span></span>

- <span data-ttu-id="dab01-116">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="dab01-116">**Domain**</span></span>
- <span data-ttu-id="dab01-117">**Nombre de messages**: vous pouvez cliquer [](message-trace-scc.md) sur Afficher les exemples de **messages** pour afficher les résultats du suivi des messages pour un échantillon des messages qui ont été affectés par la boucle.</span><span class="sxs-lookup"><span data-stu-id="dab01-117">**Number of messages**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the messages that were affected by the loop.</span></span>
- <span data-ttu-id="dab01-118">**Type de domaine**« Par exemple, faisant autorité ou ne faisant pas autorité.</span><span class="sxs-lookup"><span data-stu-id="dab01-118">**Domain type**" For example, Authoritative or Non-authoritative.</span></span>
- <span data-ttu-id="dab01-119">**Enregistrement MX**: valeurs d’hôte (serveur **de messagerie)** et de priorité de l’enregistrement MX pour le domaine. </span><span class="sxs-lookup"><span data-stu-id="dab01-119">**MX record**: The host (**Mail server**) and **Priority** values of the MX record for the domain.</span></span>
- <span data-ttu-id="dab01-120">**Raison de la** boucle et **comment corriger :** nous allons identifier les scénarios de boucle de messagerie les plus courants et fournir des actions recommandées pour corriger la boucle.</span><span class="sxs-lookup"><span data-stu-id="dab01-120">**Loop reason** and **How to fix**: We'll identify the most common mail loop scenarios and provide recommended actions to fix the loop.</span></span>

![Volant de détails qui s’affiche après avoir cliqué sur Afficher les détails sur l’aperçu de la boucle de courrier possible de correction](../../media/mfi-fix-possible-mail-loop-details.png)

## <a name="see-also"></a><span data-ttu-id="dab01-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab01-122">See also</span></span>

<span data-ttu-id="dab01-123">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="dab01-123">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
