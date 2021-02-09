---
title: Informations sur les nouveaux domaines transmis par courrier électronique
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent apprendre à utiliser les informations sur les nouveaux domaines qui sont transmis par courrier électronique dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour examiner le moment où leurs utilisateurs envoient des messages à des domaines externes qui n’ont jamais été transmis.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: a4429f1657861091082fdfaedb52c85cec3a0cc1
ms.sourcegitcommit: e920e68c8d0eac8b152039b52cfc139d478a67b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50150599"
---
# <a name="new-domains-being-forwarded-email-insight-in-the-security--compliance-center"></a><span data-ttu-id="ae9f8-103">Informations sur les nouveaux domaines transmis par courrier électronique dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="ae9f8-103">New domains being forwarded email insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="ae9f8-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ae9f8-104">**Applies to**</span></span>
- [<span data-ttu-id="ae9f8-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="ae9f8-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="ae9f8-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="ae9f8-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="ae9f8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae9f8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="ae9f8-108">Il existe des raisons professionnelles valides de faire passer des messages électroniques à des destinataires externes dans des domaines spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ae9f8-108">There are valid business reasons to forward email messages to external recipients in specific domains.</span></span> <span data-ttu-id="ae9f8-109">Toutefois, il est suspect lorsque les utilisateurs de votre organisation commencent soudainement à envoyer des messages vers un domaine vers lequel aucun utilisateur de votre organisation n’a jamais transmis de messages (un nouveau domaine).</span><span class="sxs-lookup"><span data-stu-id="ae9f8-109">However, it's suspicious when users in your organization suddenly start forwarding messages to a domain where no one in your organization has ever forwarded messages to (a new domain).</span></span>

<span data-ttu-id="ae9f8-110">Cette condition peut indiquer que les comptes d’utilisateur sont compromis.</span><span class="sxs-lookup"><span data-stu-id="ae9f8-110">This condition might indicate that the user accounts are compromised.</span></span> <span data-ttu-id="ae9f8-111">Si vous pensez que les comptes ont été compromis, voir Répondre [à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="ae9f8-111">If you suspect the accounts have been compromised, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

<span data-ttu-id="ae9f8-112">**L’aperçu** des nouveaux domaines transmis par courrier électronique dans le Centre de sécurité [&](https://protection.office.com) conformité vous informe lorsque les utilisateurs de votre organisation sont en train de forwarder des messages vers de nouveaux domaines.</span><span class="sxs-lookup"><span data-stu-id="ae9f8-112">The **New domains being forwarded email** insight in the [Security & Compliance Center](https://protection.office.com) notifies you when users in your organization are forwarding messages to new domains.</span></span>

<span data-ttu-id="ae9f8-113">Cette information apparaît uniquement lorsque le problème est détecté et apparaît sur la page du rapport [de forwarding.](view-mail-flow-reports.md#forwarding-report)</span><span class="sxs-lookup"><span data-stu-id="ae9f8-113">This insight appears only when the issue is detected, and it appears on the [Forwarding report](view-mail-flow-reports.md#forwarding-report) page.</span></span>

![Informations sur les nouveaux domaines transmis par courrier électronique](../../media/mfi-new-domains-being-forwarded.png)

<span data-ttu-id="ae9f8-115">Lorsque vous cliquez sur le widget, un flyout s’affiche, dans lequel vous trouverez plus de détails sur les messages transmis, y compris un lien vers le rapport [de forwarding.](view-mail-flow-reports.md#forwarding-report)</span><span class="sxs-lookup"><span data-stu-id="ae9f8-115">When you click on the widget, a flyout appears where you can find more details about the forwarded messages, including a link back to the [Forwarding report](view-mail-flow-reports.md#forwarding-report).</span></span>

![Volant d’informations qui s’affiche après avoir cliqué sur l’aperçu des nouveaux domaines transmis par courrier électronique](../../media/mfi-new-domains-being-forwarded-details.png)

<span data-ttu-id="ae9f8-117">Vous pouvez également vous rendre sur cette page de  détails lorsque vous sélectionnez l’aperçu après avoir cliqué sur Afficher tout dans la zone Recommandations & informations les plus **détaillées** **(** Tableau de bord de rapports \>  ou <https://protection.office.com/insightdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="ae9f8-117">You can also get to this details page when you select the insight after you click **View all** in the **Top insights & recommendations** area on (**Reports** \> **Dashboard** or <https://protection.office.com/insightdashboard>).</span></span>

<span data-ttu-id="ae9f8-118">Pour empêcher le transmission automatique de messages à des domaines externes, configurez un domaine distant pour certains domaines externes ou tous.</span><span class="sxs-lookup"><span data-stu-id="ae9f8-118">To prevent automatic message forwarding to external domains, configure a remote domain for some or all external domains.</span></span> <span data-ttu-id="ae9f8-119">Pour plus d’informations, voir [Gérer les domaines distants dans Exchange Online.](https://docs.microsoft.com/Exchange/mail-flow-best-practices/remote-domains/manage-remote-domains)</span><span class="sxs-lookup"><span data-stu-id="ae9f8-119">For more information, see [Manage remote domains in Exchange Online](https://docs.microsoft.com/Exchange/mail-flow-best-practices/remote-domains/manage-remote-domains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae9f8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae9f8-120">Related topics</span></span>

<span data-ttu-id="ae9f8-121">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="ae9f8-121">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
