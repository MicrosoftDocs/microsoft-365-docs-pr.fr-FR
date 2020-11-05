---
title: Informations sur les nouveaux domaines transmis par courrier électronique
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: exchange-online
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent apprendre à utiliser les nouveaux domaines en cours de transmission de messages électroniques dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité afin de déterminer quand leurs utilisateurs transfèrent des messages à des domaines externes qui n’ont jamais été transférés.
ms.openlocfilehash: f2d8c9229062cbef0ad90b3d0fd843d6588a08dc
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920564"
---
# <a name="new-domains-being-forwarded-email-insight-in-the-security--compliance-center"></a><span data-ttu-id="94bfa-103">Nouveaux domaines transmis par courrier électronique dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="94bfa-103">New domains being forwarded email insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="94bfa-104">Il existe des raisons professionnelles valables pour transférer des messages électroniques à des destinataires externes dans des domaines spécifiques.</span><span class="sxs-lookup"><span data-stu-id="94bfa-104">There are valid business reasons to forward email messages to external recipients in specific domains.</span></span> <span data-ttu-id="94bfa-105">Toutefois, il est suspect lorsque les utilisateurs de votre organisation redirigent soudainement les messages vers un domaine où personne de votre organisation n’a transféré les messages vers (un nouveau domaine).</span><span class="sxs-lookup"><span data-stu-id="94bfa-105">However, it's suspicious when users in your organization suddenly start forwarding messages to a domain where no one in your organization has ever forwarded messages to (a new domain).</span></span>

<span data-ttu-id="94bfa-106">Cette condition peut indiquer que les comptes d’utilisateur sont compromis.</span><span class="sxs-lookup"><span data-stu-id="94bfa-106">This condition might indicate that the user accounts are compromised.</span></span> <span data-ttu-id="94bfa-107">Si vous pensez que les comptes ont été compromis, consultez la rubrique relative [à la réponse à un compte de courrier compromis](https://docs.microsoft.com/microsoft-365/security/office-365-security/responding-to-a-compromised-email-account).</span><span class="sxs-lookup"><span data-stu-id="94bfa-107">If you suspect the accounts have been compromised, see [Responding to a compromised email account](https://docs.microsoft.com/microsoft-365/security/office-365-security/responding-to-a-compromised-email-account).</span></span>

<span data-ttu-id="94bfa-108">Les **nouveaux domaines transmis par courrier électronique** dans le [centre de sécurité & Compliance Center](https://protection.office.com) vous avertissent lorsque les utilisateurs de votre organisation acheminent des messages vers de nouveaux domaines.</span><span class="sxs-lookup"><span data-stu-id="94bfa-108">The **New domains being forwarded email** insight in the [Security & Compliance Center](https://protection.office.com) notifies you when users in your organization are forwarding messages to new domains.</span></span>

<span data-ttu-id="94bfa-109">Cette vue s’affiche uniquement lorsque le problème est détecté et qu’il apparaît sur la page [rapport de transfert](view-mail-flow-reports.md#forwarding-report) .</span><span class="sxs-lookup"><span data-stu-id="94bfa-109">This insight appears only when the issue is detected, and it appears on the [Forwarding report](view-mail-flow-reports.md#forwarding-report) page.</span></span>

![Informations sur les nouveaux domaines transmis par courrier électronique](../../media/mfi-new-domains-being-forwarded.png)

<span data-ttu-id="94bfa-111">Lorsque vous cliquez sur le widget, un menu volant s’affiche pour vous permettre de trouver plus d’informations sur les messages transférés, y compris un lien vers le [rapport de transfert](view-mail-flow-reports.md#forwarding-report).</span><span class="sxs-lookup"><span data-stu-id="94bfa-111">When you click on the widget, a flyout appears where you can find more details about the forwarded messages, including a link back to the [Forwarding report](view-mail-flow-reports.md#forwarding-report).</span></span>

![Fenêtre volante de détails qui apparaît après avoir cliqué sur les nouveaux domaines en cours de transmission de messages électroniques](../../media/mfi-new-domains-being-forwarded-details.png)

<span data-ttu-id="94bfa-113">Vous pouvez également accéder à cette page de détails lorsque vous sélectionnez l’option **Afficher tout** dans la zone de **recommandations & premières Insights** (tableau de **Reports** \> **bord** rapports ou <https://protection.office.com/insightdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="94bfa-113">You can also get to this details page when you select the insight after you click **View all** in the **Top insights & recommendations** area on ( **Reports** \> **Dashboard** or <https://protection.office.com/insightdashboard>).</span></span>

<span data-ttu-id="94bfa-114">Pour empêcher le transfert automatique des messages vers des domaines externes, configurez un domaine distant pour certains ou tous les domaines externes.</span><span class="sxs-lookup"><span data-stu-id="94bfa-114">To prevent automatic message forwarding to external domains, configure a remote domain for some or all external domains.</span></span> <span data-ttu-id="94bfa-115">Pour plus d’informations, consultez la rubrique [gestion des domaines distants dans Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/remote-domains/manage-remote-domains).</span><span class="sxs-lookup"><span data-stu-id="94bfa-115">For more information, see [Manage remote domains in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/remote-domains/manage-remote-domains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94bfa-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94bfa-116">Related topics</span></span>

<span data-ttu-id="94bfa-117">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="94bfa-117">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
