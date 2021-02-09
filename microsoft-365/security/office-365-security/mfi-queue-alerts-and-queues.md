---
title: Informations sur les files d’attente dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Les administrateurs peuvent apprendre à utiliser le widget Files d’attente dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour surveiller le flux de messagerie infructueux vers leurs organisations locales ou partenaires sur des connecteurs sortants.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 94e8a1f3b54c3738c21e94ba85ae4f1d3f953498
ms.sourcegitcommit: e920e68c8d0eac8b152039b52cfc139d478a67b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50150170"
---
# <a name="queues-insight-in-the-security--compliance-center"></a><span data-ttu-id="a366e-103">Informations sur les files d’attente dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="a366e-103">Queues insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="a366e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a366e-104">**Applies to**</span></span>
- [<span data-ttu-id="a366e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="a366e-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="a366e-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="a366e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="a366e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a366e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="a366e-108">Lorsque les messages ne peuvent pas être envoyés à partir de votre organisation vers vos serveurs de messagerie locaux ou partenaires à l’aide de connecteurs, les messages sont mis en file d’attente dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a366e-108">When messages can't be sent from your organization to your on-premises or partner email servers using connectors, the messages are queued in Microsoft 365.</span></span> <span data-ttu-id="a366e-109">Les exemples courants à l’origine de cette condition sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a366e-109">Common examples that cause this condition are:</span></span>

- <span data-ttu-id="a366e-110">Le connecteur n’est pas correctement configuré.</span><span class="sxs-lookup"><span data-stu-id="a366e-110">The connector is incorrectly configured.</span></span>
- <span data-ttu-id="a366e-111">Des modifications ont été apportées au réseau ou au pare-feu dans votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="a366e-111">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="a366e-112">Microsoft 365 continuera à réessayer d’être livré pendant 24 heures.</span><span class="sxs-lookup"><span data-stu-id="a366e-112">Microsoft 365 will continue to retry to delivery for 24 hours.</span></span> <span data-ttu-id="a366e-113">Au bout de 24 heures, les messages expirent et sont renvoyés aux expéditeurs dans les rapports de non-remise (également appelés messages de non-remise).</span><span class="sxs-lookup"><span data-stu-id="a366e-113">After 24 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="a366e-114">Si le volume de courrier en file d’attente dépasse le seuil prédéfiny (la valeur par défaut est 200 messages), les informations sont disponibles aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="a366e-114">If the queued email volume exceeds the pre-defined threshold (the default value is 200 messages), the information is available in the following locations:</span></span>

- <span data-ttu-id="a366e-115">Informations **sur les files d’attente** dans le tableau de bord de [flux](mail-flow-insights-v2.md) de messagerie du Centre de sécurité [& conformité.](https://protection.office.com)</span><span class="sxs-lookup"><span data-stu-id="a366e-115">The **Queues** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="a366e-116">Pour plus d’informations, voir [l’aperçu](#queues-insight-in-the-mail-flow-dashboard) des files d’attente dans la section Tableau de bord du flux de messagerie de cet article.</span><span class="sxs-lookup"><span data-stu-id="a366e-116">For more information, see the [Queues insight in the Mail flow dashboard](#queues-insight-in-the-mail-flow-dashboard) section in this article.</span></span>

- <span data-ttu-id="a366e-117">Une alerte s’affiche dans **alertes récentes** le tableau de bord Alertes dans le Centre de sécurité [&](https://protection.office.com) conformité ( Tableau de bord des **alertes** \>  ou <https://protection.office.com/alertsdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="a366e-117">An alert is displayed in **Recent alerts** the Alerts dashboard in the [Security & Compliance Center](https://protection.office.com) (**Alerts** \> **Dashboard** or <https://protection.office.com/alertsdashboard>).</span></span>

  ![Alertes récentes dans le tableau de bord Alertes du Centre de sécurité & conformité](../../media/mfi-queued-messages-alert.png)

- <span data-ttu-id="a366e-119">Les administrateurs recevront une notification par courrier électronique en fonction de la configuration de la stratégie d’alerte par défaut nommée **Messages qui a été retardée.**</span><span class="sxs-lookup"><span data-stu-id="a366e-119">Admins will receive an email notification based on the configuration of the default alert policy named **Messages have been delayed**.</span></span> <span data-ttu-id="a366e-120">Pour configurer les paramètres de notification pour cette alerte, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="a366e-120">To configure the notification settings for this alert, see the next section.</span></span>

  <span data-ttu-id="a366e-121">Pour plus d’informations sur les stratégies d’alerte, voir Stratégies d’alerte dans le Centre de [sécurité & conformité.](../../compliance/alert-policies.md)</span><span class="sxs-lookup"><span data-stu-id="a366e-121">For more information about alert policies, see [Alert policies in the Security & Compliance Center](../../compliance/alert-policies.md).</span></span>

## <a name="customize-queue-alerts"></a><span data-ttu-id="a366e-122">Personnaliser les alertes de file d’attente</span><span class="sxs-lookup"><span data-stu-id="a366e-122">Customize queue alerts</span></span>

1. <span data-ttu-id="a366e-123">Dans le [Centre de sécurité & conformité,](https://protection.office.com)allez aux **stratégies d’alerte des alertes** \>  ou ouvrez <https://protection.office.com/alertpolicies> .</span><span class="sxs-lookup"><span data-stu-id="a366e-123">In the [Security & Compliance Center](https://protection.office.com), go to **Alerts** \> **Alert policies** or open <https://protection.office.com/alertpolicies>.</span></span>

2. <span data-ttu-id="a366e-124">Dans la page **Stratégies d’alerte,** recherchez et sélectionnez la stratégie nommée **Messages qui a été retardée.**</span><span class="sxs-lookup"><span data-stu-id="a366e-124">On the **Alert policies** page, find and select the policy named **Messages have been delayed**.</span></span>

3. <span data-ttu-id="a366e-125">Dans le **flyout Message qui** s’ouvre, vous pouvez activer ou désactiver l’alerte et configurer les paramètres de notification.</span><span class="sxs-lookup"><span data-stu-id="a366e-125">In the **Message have been delayed** flyout that opens, you can turn the alert on or off and configure the notification settings.</span></span>

   ![Les messages ont été retardés, détails de la stratégie d’alerte du Centre de sécurité & conformité](../../media/mfi-queued-messages-alert-policy.png)

   - <span data-ttu-id="a366e-127">**État**: vous pouvez mettre l’alerte sur ou hors de l’état.</span><span class="sxs-lookup"><span data-stu-id="a366e-127">**Status**: You can toggle the alert on or off.</span></span>

   - <span data-ttu-id="a366e-128">**Destinataires de courrier électronique** et **limite de notification quotidienne**: cliquez sur **Modifier** pour configurer les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a366e-128">**Email recipients** and **Daily notification limit**: Click **Edit** to configure the following settings:</span></span>

4. <span data-ttu-id="a366e-129">Pour configurer les paramètres de notification, cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="a366e-129">To configure the notification settings, click **Edit**.</span></span> <span data-ttu-id="a366e-130">Dans le **volant modifier la** stratégie qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="a366e-130">In the **Edit policy** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="a366e-131">**Envoyer des notifications par courrier électronique**: la valeur par défaut est sur.</span><span class="sxs-lookup"><span data-stu-id="a366e-131">**Send email notifications**: The default value is on.</span></span>
   - <span data-ttu-id="a366e-132">**Destinataires du courrier électronique**: la valeur par défaut **est TenantAdmins**.</span><span class="sxs-lookup"><span data-stu-id="a366e-132">**Email recipients**: The default value is **TenantAdmins**.</span></span>
   - <span data-ttu-id="a366e-133">**Limite de notification quotidienne**: la valeur par défaut est **Aucune limite.**</span><span class="sxs-lookup"><span data-stu-id="a366e-133">**Daily notification limit**: The default value is **No limit**.</span></span>
   - <span data-ttu-id="a366e-134">**Seuil**: la valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="a366e-134">**Threshold**: The default value is 200.</span></span>

   ![Les paramètres de notification dans les messages ont été retardés, détails de la stratégie d’alerte du Centre de sécurité & conformité](../../media/mfi-queued-messages-alert-policy-notification-settings.png)

5. <span data-ttu-id="a366e-136">Lorsque vous avez terminé, cliquez sur **Enregistrer** et **fermer.**</span><span class="sxs-lookup"><span data-stu-id="a366e-136">When you're finished, click **Save** and **Close**.</span></span>

## <a name="queues-insight-in-the-mail-flow-dashboard"></a><span data-ttu-id="a366e-137">Informations sur les files d’attente dans le tableau de bord de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="a366e-137">Queues insight in the Mail flow dashboard</span></span>

<span data-ttu-id="a366e-138">Même si le volume de messages en file d’attente n’a pas  dépassé le [](mail-flow-insights-v2.md) seuil et généré une alerte, vous pouvez toujours utiliser l’aperçu des files d’attente dans le tableau de bord de flux de messagerie pour voir les messages mis en file d’attente depuis plus d’une heure et prendre des mesures avant que le nombre de messages mis en file d’attente devienne trop important.</span><span class="sxs-lookup"><span data-stu-id="a366e-138">Even if the queued message volume hasn't exceeded the threshold and generated an alert, you can still use the **Queues** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) to see messages that have been queued for more than one hour, and take action before the number of queued messages becomes too large.</span></span>

![Widget Files d’attente dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-queues-widget.png)

<span data-ttu-id="a366e-140">Si vous cliquez sur le nombre  de messages sur le widget, un message volant messages mis en file d’attente apparaît avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a366e-140">If you click the number of messages on the widget, a **Messages queued** flyout appears with the following information:</span></span>

- <span data-ttu-id="a366e-141">**Nombre de messages mis en file d’attente**</span><span class="sxs-lookup"><span data-stu-id="a366e-141">**Number of queued messages**</span></span>
- <span data-ttu-id="a366e-142">**Nom du connecteur**: cliquez sur le nom du connecteur pour gérer le connecteur dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="a366e-142">**Connector name**: Click on the connector name to manage the connector in the Exchange admin center (EAC).</span></span>
- <span data-ttu-id="a366e-143">**Heure de début de la file d’attente**</span><span class="sxs-lookup"><span data-stu-id="a366e-143">**Queue started time**</span></span>
- <span data-ttu-id="a366e-144">**Messages les plus anciens arrivés à expiration**</span><span class="sxs-lookup"><span data-stu-id="a366e-144">**Oldest messages expired**</span></span>
- <span data-ttu-id="a366e-145">**Serveur de destination**</span><span class="sxs-lookup"><span data-stu-id="a366e-145">**Destination server**</span></span>
- <span data-ttu-id="a366e-146">**Dernière adresse IP**</span><span class="sxs-lookup"><span data-stu-id="a366e-146">**Last IP address**</span></span>
- <span data-ttu-id="a366e-147">**Dernière erreur**</span><span class="sxs-lookup"><span data-stu-id="a366e-147">**Last error**</span></span>
- <span data-ttu-id="a366e-148">**Comment résoudre :** des problèmes courants et des solutions sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="a366e-148">**How to fix**: Common issues and solutions are available.</span></span> <span data-ttu-id="a366e-149">If is a **Fix it now** link is available, click it to fix the problem.</span><span class="sxs-lookup"><span data-stu-id="a366e-149">If is a **Fix it now** link is available, click it to fix the problem.</span></span> <span data-ttu-id="a366e-150">Dans le cas contraire, cliquez sur les liens disponibles pour plus d’informations sur l’erreur et les solutions possibles.</span><span class="sxs-lookup"><span data-stu-id="a366e-150">Otherwise, click on any available links for more information about the error and possible solutions.</span></span>

![Détails après avoir cliqué sur l’aperçu files d’attente dans le tableau de bord de flux de messagerie](../../media/mfi-queues-details.png)

<span data-ttu-id="a366e-152">Le même volant s’affiche lorsque vous cliquez sur Afficher la **file** d’attente dans les détails d’une alerte de retard **de** messages.</span><span class="sxs-lookup"><span data-stu-id="a366e-152">The same flyout is displayed after you click **View queue** in the details of a **Messages have been delayed** alert.</span></span>

![Les messages ont été retardés dans les détails de l’alerte dans le Centre de sécurité & conformité](../../media/mfi-queued-messages-alert-details.png)

## <a name="see-also"></a><span data-ttu-id="a366e-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a366e-154">See also</span></span>

<span data-ttu-id="a366e-155">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="a366e-155">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
