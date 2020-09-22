---
title: Vue d’État du flux de messagerie de domaine supérieur dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser l’état du flux de messagerie du domaine le plus pertinent dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour résoudre les problèmes de flux de messagerie liés aux enregistrements MX dans leurs domaines de messagerie.
ms.openlocfilehash: 24922d6ae7d2ec50e3d9383631991cf46a818c05
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48197524"
---
# <a name="top-domain-mail-flow-status-insight-in-the-security--compliance-center"></a><span data-ttu-id="69c21-103">État du flux de messagerie du domaine le plus approfondi dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="69c21-103">Top domain mail flow status insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="69c21-104">L' **État du flux de messagerie du domaine le plus visible** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de [sécurité & conformité](https://protection.office.com) vous donne l’état actuel des domaines de votre organisation en termes de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="69c21-104">The **Top domain mail flow status** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="69c21-105">Cette vue vous permet d’identifier et de résoudre les problèmes de ***flux de messagerie*** (par exemple, impossible de recevoir des messages électroniques externes), notamment les expirations de domaine ou les domaines avec des enregistrements MX incorrects.</span><span class="sxs-lookup"><span data-stu-id="69c21-105">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![Widget État du flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-top-domain-mail-flow-status-widget.png)

<span data-ttu-id="69c21-107">Lorsque vous cliquez sur **afficher les détails** dans le widget, un menu volant d’état de **domaine** s’affiche pour vous afficher des détails supplémentaires sur l’état de chaque domaine :</span><span class="sxs-lookup"><span data-stu-id="69c21-107">When you click **View details** in the widget, a **Domain status** flyout appears that shows you more details for the status of each domain:</span></span>

- <span data-ttu-id="69c21-108">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="69c21-108">**Domain**</span></span>
- <span data-ttu-id="69c21-109">**Enregistrement MX précédent**</span><span class="sxs-lookup"><span data-stu-id="69c21-109">**Previous MX record**</span></span>
- <span data-ttu-id="69c21-110">**Enregistrement MX actuel**</span><span class="sxs-lookup"><span data-stu-id="69c21-110">**Current MX record**</span></span>
- <span data-ttu-id="69c21-111">**État de réception du courrier électronique**</span><span class="sxs-lookup"><span data-stu-id="69c21-111">**Email receiving status**</span></span>
- <span data-ttu-id="69c21-112">**État du domaine**: une coche verte indique que l’enregistrement MX actuel (au moment où vous avez cliqué sur le widget) correspond à la valeur que nous avons sur l’enregistrement et que le domaine a reçu la messagerie au cours des deux dernières heures.</span><span class="sxs-lookup"><span data-stu-id="69c21-112">**Domain status**: A green check mark indicates the current MX record (at the time you clicked on the widget) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

  <span data-ttu-id="69c21-113">Un X rouge indique que l’enregistrement MX a été modifié et que le domaine n’a pas reçu de courrier au cours des 6 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="69c21-113">A red X indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="69c21-114">Cela indique probablement que votre domaine a expiré ou que l’enregistrement MX a été mis à jour de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="69c21-114">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="69c21-115">Vérifiez auprès de votre bureau d’enregistrement de domaines ou de votre service d’hébergement DNS si le domaine a expiré ou si l’enregistrement MX du domaine est incorrect.</span><span class="sxs-lookup"><span data-stu-id="69c21-115">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

<span data-ttu-id="69c21-116">Vous pouvez cliquer sur **afficher plus** pour afficher les mêmes informations pour plus de domaines.</span><span class="sxs-lookup"><span data-stu-id="69c21-116">You can click **View more** to see the same information for more domains.</span></span>

![Fenêtre mobile détails dans l’état du flux de messagerie du domaine supérieur](../../media/mfi-top-domain-mail-flow-status-view-details.png)

## <a name="related-topics"></a><span data-ttu-id="69c21-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69c21-118">Related topics</span></span>

<span data-ttu-id="69c21-119">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="69c21-119">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
