---
title: Vue d’État du flux de messagerie de domaine supérieur dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser l’état du flux de messagerie du domaine le plus pertinent dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour résoudre les problèmes de flux de messagerie liés à leurs enregistrements MX.
ms.openlocfilehash: 0d750ab4dbe5875796118086fae1d9119dc486f0
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920583"
---
# <a name="top-domain-mail-flow-status-insight-in-the-security--compliance-center"></a><span data-ttu-id="5fd71-103">État du flux de messagerie du domaine le plus approfondi dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="5fd71-103">Top domain mail flow status insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="5fd71-104">L’état du flux de **messagerie du domaine le plus visible** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le [Centre de sécurité & conformité](https://protection.office.com) vous donne l’état actuel du flux de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5fd71-104">The **Top domain mail flow status** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) gives you the current mail flow status for your organization.</span></span>

<span data-ttu-id="5fd71-105">Cette vue vous permet d’identifier et de dépanner les domaines rencontrant des problèmes de *_flux de messagerie_*.</span><span class="sxs-lookup"><span data-stu-id="5fd71-105">This insight helps you identify and troubleshoot domains that are experiencing \* *_mail flow_* _ issues.</span></span> <span data-ttu-id="5fd71-106">Par exemple, le domaine ne peut pas recevoir de courrier électronique externe, car le domaine a expiré ou le domaine a un enregistrement MX incorrect.</span><span class="sxs-lookup"><span data-stu-id="5fd71-106">For example, the domain is unable to receive external email because the domain has expired or the domain has an incorrect MX record.</span></span>

![Widget État du flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-top-domain-mail-flow-status-widget.png)

<span data-ttu-id="5fd71-108">Lorsque vous cliquez sur _ *afficher les détails* \* dans le widget, un menu volant d’état de **domaine** s’affiche pour vous afficher des détails supplémentaires sur l’état de chaque domaine :</span><span class="sxs-lookup"><span data-stu-id="5fd71-108">When you click _ *View details* \* in the widget, a **Domain status** flyout appears that shows you more details for the status of each domain:</span></span>

- <span data-ttu-id="5fd71-109">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="5fd71-109">**Domain**</span></span>
- <span data-ttu-id="5fd71-110">**Enregistrement MX précédent**</span><span class="sxs-lookup"><span data-stu-id="5fd71-110">**Previous MX record**</span></span>
- <span data-ttu-id="5fd71-111">**Enregistrement MX actuel**</span><span class="sxs-lookup"><span data-stu-id="5fd71-111">**Current MX record**</span></span>
- <span data-ttu-id="5fd71-112">**État de réception du courrier électronique**</span><span class="sxs-lookup"><span data-stu-id="5fd71-112">**Email receiving status**</span></span>
- <span data-ttu-id="5fd71-113">**État du domaine** : une coche verte indique que l’enregistrement MX actuel (au moment où vous avez cliqué sur le widget) correspond à la valeur que nous avons sur l’enregistrement et que le domaine a reçu la messagerie au cours des deux dernières heures.</span><span class="sxs-lookup"><span data-stu-id="5fd71-113">**Domain status** : A green check mark indicates the current MX record (at the time you clicked on the widget) matches the value we have on record, and the domain has received email during the past two hours.</span></span>

  <span data-ttu-id="5fd71-114">Un X rouge indique que l’enregistrement MX a été modifié et que le domaine n’a pas reçu de courrier au cours des 6 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="5fd71-114">A red X indicates the MX record has been changed, and the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="5fd71-115">Cela indique probablement que votre domaine a expiré ou que l’enregistrement MX a été mis à jour de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="5fd71-115">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="5fd71-116">Vérifiez auprès de votre bureau d’enregistrement de domaines ou de votre service d’hébergement DNS si le domaine a expiré ou si l’enregistrement MX du domaine est incorrect.</span><span class="sxs-lookup"><span data-stu-id="5fd71-116">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

<span data-ttu-id="5fd71-117">Vous pouvez cliquer sur **afficher plus** pour afficher les mêmes informations pour plus de domaines.</span><span class="sxs-lookup"><span data-stu-id="5fd71-117">You can click **View more** to see the same information for more domains.</span></span>

![Fenêtre mobile détails dans l’état du flux de messagerie du domaine supérieur](../../media/mfi-top-domain-mail-flow-status-view-details.png)

## <a name="see-also"></a><span data-ttu-id="5fd71-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fd71-119">See also</span></span>

<span data-ttu-id="5fd71-120">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="5fd71-120">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
