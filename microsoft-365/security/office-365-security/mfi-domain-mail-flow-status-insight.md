---
title: Aperçu de l’état du flux de messagerie de domaine supérieur dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser l’aperçu de l’état du flux de messagerie de domaine supérieur dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour résoudre les problèmes de flux de messagerie liés à leurs enregistrements MX.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 850e72fa0ad7a3f41450a1d0a2c02dd3df4a0cb5
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204935"
---
# <a name="top-domain-mail-flow-status-insight-in-the-security--compliance-center"></a><span data-ttu-id="32be3-103">Informations sur l’état du flux de messagerie du domaine dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="32be3-103">Top domain mail flow status insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="32be3-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="32be3-104">**Applies to**</span></span>
- [<span data-ttu-id="32be3-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="32be3-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="32be3-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="32be3-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="32be3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="32be3-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="32be3-108">**L’aperçu de** l’état [](mail-flow-insights-v2.md) du flux de messagerie de domaine supérieur dans le tableau de bord flux de messagerie dans le Centre de sécurité [&](https://protection.office.com) conformité vous donne l’état actuel du flux de messagerie pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="32be3-108">The **Top domain mail flow status** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) gives you the current mail flow status for your organization.</span></span>

<span data-ttu-id="32be3-109">Cette information vous permet d’identifier et de dépanner les domaines qui rencontrent des problèmes de ***flux*** de messagerie.</span><span class="sxs-lookup"><span data-stu-id="32be3-109">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow*** issues.</span></span> <span data-ttu-id="32be3-110">Par exemple, le domaine ne peut pas recevoir de courrier externe car le domaine a expiré ou le domaine a un enregistrement MX incorrect.</span><span class="sxs-lookup"><span data-stu-id="32be3-110">For example, the domain is unable to receive external email because the domain has expired or the domain has an incorrect MX record.</span></span>

![Widget d’état de flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-top-domain-mail-flow-status-widget.png)

<span data-ttu-id="32be3-112">Lorsque vous cliquez sur Afficher les  **détails** dans le widget, un volant d’état de domaine s’affiche et vous indique plus de détails sur l’état de chaque domaine :</span><span class="sxs-lookup"><span data-stu-id="32be3-112">When you click **View details** in the widget, a **Domain status** flyout appears that shows you more details for the status of each domain:</span></span>

- <span data-ttu-id="32be3-113">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="32be3-113">**Domain**</span></span>
- <span data-ttu-id="32be3-114">**Enregistrement MX précédent**</span><span class="sxs-lookup"><span data-stu-id="32be3-114">**Previous MX record**</span></span>
- <span data-ttu-id="32be3-115">**Enregistrement MX actuel**</span><span class="sxs-lookup"><span data-stu-id="32be3-115">**Current MX record**</span></span>
- <span data-ttu-id="32be3-116">**État de réception des messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="32be3-116">**Email receiving status**</span></span>
- <span data-ttu-id="32be3-117">État **du** domaine : une coche verte indique que l’enregistrement MX actuel (au moment où vous avez cliqué sur le widget) correspond à la valeur que nous avons sur l’enregistrement et que le domaine a reçu des messages électroniques au cours des deux dernières heures.</span><span class="sxs-lookup"><span data-stu-id="32be3-117">**Domain status**: A green check mark indicates the current MX record (at the time you clicked on the widget) matches the value we have on record, and the domain has received email during the past two hours.</span></span>

  <span data-ttu-id="32be3-118">Un X rouge indique que l’enregistrement MX a été modifié et que le domaine n’a reçu aucun message électronique au cours des 6 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="32be3-118">A red X indicates the MX record has been changed, and the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="32be3-119">Cela indique probablement que votre domaine a expiré ou que l’enregistrement MX a été mis à jour de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="32be3-119">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="32be3-120">Vérifiez auprès de votre bureau d’enregistrement de domaines ou service d’hébergement DNS si le domaine a expiré ou si l’enregistrement MX du domaine est incorrect.</span><span class="sxs-lookup"><span data-stu-id="32be3-120">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

<span data-ttu-id="32be3-121">Vous pouvez cliquer **sur Afficher plus** pour afficher les mêmes informations pour d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="32be3-121">You can click **View more** to see the same information for more domains.</span></span>

![Flux de détails dans l’aperçu de l’état du flux de messagerie de domaine supérieur](../../media/mfi-top-domain-mail-flow-status-view-details.png)

## <a name="see-also"></a><span data-ttu-id="32be3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32be3-123">See also</span></span>

<span data-ttu-id="32be3-124">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="32be3-124">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
