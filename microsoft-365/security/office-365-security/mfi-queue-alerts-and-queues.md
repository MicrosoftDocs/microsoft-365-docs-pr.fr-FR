---
title: Vue d’attente dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Les administrateurs peuvent apprendre à utiliser le widget files d’attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour surveiller les flux de messages infructueux vers leurs organisations locales ou partenaires sur des connecteurs sortants.
ms.openlocfilehash: 79523533306e847988fa0d4e2dd70eca22f7c76c
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46826904"
---
# <a name="queues-insight-in-the-security--compliance-center"></a><span data-ttu-id="491e8-103">Files d’attente Insight dans le centre de conformité & Security</span><span class="sxs-lookup"><span data-stu-id="491e8-103">Queues insight in the Security & Compliance Center</span></span>

<span data-ttu-id="491e8-104">Lorsque des messages ne peuvent pas être envoyés de votre organisation à vos serveurs de messagerie locaux ou partenaires à l’aide de connecteurs, les messages sont mis en file d’attente dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="491e8-104">When messages can't be sent from your organization to your on-premises or partner email servers using connectors, the messages are queued in Microsoft 365.</span></span> <span data-ttu-id="491e8-105">Les exemples courants qui génèrent cette condition sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="491e8-105">Common examples that cause this condition are:</span></span>

- <span data-ttu-id="491e8-106">Le connecteur est configuré de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="491e8-106">The connector is incorrectly configured.</span></span>
- <span data-ttu-id="491e8-107">Des modifications de mise en réseau ou de pare-feu ont été apportées dans votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="491e8-107">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="491e8-108">Microsoft 365 continuera à nouvelle tentative de remise pendant 24 heures.</span><span class="sxs-lookup"><span data-stu-id="491e8-108">Microsoft 365 will continue to retry to delivery for 24 hours.</span></span> <span data-ttu-id="491e8-109">Au bout de 24 heures, les messages expirent et seront renvoyés aux expéditeurs dans les notifications d’échec de remise (également appelées notifications de non-remise).</span><span class="sxs-lookup"><span data-stu-id="491e8-109">After 24 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="491e8-110">Si le volume de messagerie en file d’attente dépasse le seuil prédéfini (la valeur par défaut est 200 messages), les informations sont disponibles aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="491e8-110">If the queued email volume exceeds the pre-defined threshold (the default value is 200 messages), the information is available in the following locations:</span></span>

- <span data-ttu-id="491e8-111">La vue **files d’attente** du [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="491e8-111">The **Queues** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center.</span></span> <span data-ttu-id="491e8-112">Pour plus d’informations, reportez-vous à la section [files d’attente du tableau de bord du flux de messagerie](#queues-insight-in-the-mail-flow-dashboard) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="491e8-112">For more information, see the [Queues insight in the Mail flow dashboard](#queues-insight-in-the-mail-flow-dashboard) section in this topic.</span></span>
  
- <span data-ttu-id="491e8-113">Une alerte est affichée dans les **alertes récentes** le tableau de bord des alertes dans le [Centre de sécurité & conformité](https://protection.office.com) (tableau de bord des**alertes** \> **Dashboard** ou <https://protection.office.com/alertsdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="491e8-113">An alert is displayed in **Recent alerts** the Alerts dashboard in the [Security & Compliance Center](https://protection.office.com) (**Alerts** \> **Dashboard** or <https://protection.office.com/alertsdashboard>).</span></span>

  ![Alertes récentes dans le tableau de bord des alertes dans le centre de sécurité & conformité](../../media/mfi-queued-messages-alert.png)

- <span data-ttu-id="491e8-115">Les administrateurs recevront une notification par courrier électronique en fonction de la configuration de la stratégie d’alerte par défaut nommée **messages ont été retardées**.</span><span class="sxs-lookup"><span data-stu-id="491e8-115">Admins will receive an email notification based on the configuration of the default alert policy named **Messages have been delayed**.</span></span> <span data-ttu-id="491e8-116">Pour configurer les paramètres de notification de cette alerte, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="491e8-116">To configure the notification settings for this alert, see the next section.</span></span>

  <span data-ttu-id="491e8-117">Pour plus d’informations sur les stratégies d’alerte, consultez [la rubrique Alert Policies in the Security & Compliance Center](../../compliance/alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="491e8-117">For more information about alert policies, see [Alert policies in the Security & Compliance Center](../../compliance/alert-policies.md).</span></span>

## <a name="customize-queue-alerts"></a><span data-ttu-id="491e8-118">Personnaliser les alertes de file d’attente</span><span class="sxs-lookup"><span data-stu-id="491e8-118">Customize queue alerts</span></span>

1. <span data-ttu-id="491e8-119">Dans le [Centre de sécurité & conformité](https://protection.office.com), accédez à **alertes** d' \> **alerte** ou ouvrez <https://protection.office.com/alertpolicies> .</span><span class="sxs-lookup"><span data-stu-id="491e8-119">In the [Security & Compliance Center](https://protection.office.com), go to **Alerts** \> **Alert policies** or open <https://protection.office.com/alertpolicies>.</span></span>

2. <span data-ttu-id="491e8-120">Sur la page **stratégies d’alerte** , recherchez et sélectionnez la stratégie nommée **messages ont été retardées**.</span><span class="sxs-lookup"><span data-stu-id="491e8-120">On the **Alert policies** page, find and select the policy named **Messages have been delayed**.</span></span>

3. <span data-ttu-id="491e8-121">Dans la fenêtre volante **retardée du message** qui s’ouvre, vous pouvez activer ou désactiver l’alerte et configurer les paramètres de notification.</span><span class="sxs-lookup"><span data-stu-id="491e8-121">In the **Message have been delayed** flyout that opens, you can turn the alert on or off and configure the notification settings.</span></span>

   ![Les messages ont été retardés détails de stratégie d’alerte le centre de sécurité & conformité](../../media/mfi-queued-messages-alert-policy.png)

   - <span data-ttu-id="491e8-123">**État**: vous pouvez activer ou désactiver l’alerte.</span><span class="sxs-lookup"><span data-stu-id="491e8-123">**Status**: You can toggle the alert on or off.</span></span>

   - <span data-ttu-id="491e8-124">**Destinataires du message électronique** et **limite de notification quotidienne**: cliquez sur **modifier** pour configurer les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="491e8-124">**Email recipients** and **Daily notification limit**: Click **Edit** to configure the following settings:</span></span>

4. <span data-ttu-id="491e8-125">Pour configurer les paramètres de notification, cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="491e8-125">To configure the notification settings, click **Edit**.</span></span> <span data-ttu-id="491e8-126">Dans le menu volant **modifier la stratégie** qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="491e8-126">In the **Edit policy** flyout that appears, configure the following settings:</span></span>

   - <span data-ttu-id="491e8-127">**Envoyer des notifications par courrier électronique**: la valeur par défaut est activé.</span><span class="sxs-lookup"><span data-stu-id="491e8-127">**Send email notifications**: The default value is on.</span></span>
   - <span data-ttu-id="491e8-128">**Destinataires du message électronique**: la valeur par défaut est **TenantAdmins**.</span><span class="sxs-lookup"><span data-stu-id="491e8-128">**Email recipients**: The default value is **TenantAdmins**.</span></span>
   - <span data-ttu-id="491e8-129">**Limite quotidienne des notifications**: la valeur par défaut est **aucune limite**.</span><span class="sxs-lookup"><span data-stu-id="491e8-129">**Daily notification limit**: The default value is **No limit**.</span></span>
   - <span data-ttu-id="491e8-130">**Seuil**: la valeur par défaut est 200.</span><span class="sxs-lookup"><span data-stu-id="491e8-130">**Threshold**: The default value is 200.</span></span>

   ![Les paramètres de notification dans les messages ont été retardés détails de la stratégie d’alerte le centre de sécurité & conformité](../../media/mfi-queued-messages-alert-policy-notification-settings.png)

5. <span data-ttu-id="491e8-132">Lorsque vous avez terminé, cliquez sur **Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="491e8-132">When you're finished, click **Save** and **Close**.</span></span>

## <a name="queues-insight-in-the-mail-flow-dashboard"></a><span data-ttu-id="491e8-133">Vue d’attente dans le tableau de bord de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="491e8-133">Queues insight in the Mail flow dashboard</span></span>

<span data-ttu-id="491e8-134">Même si le volume des messages mis en file d’attente n’a pas dépassé le seuil et généré une alerte, vous pouvez toujours utiliser l’aperçu **files d’attente** du tableau de bord du [flux de messagerie](mail-flow-insights-v2.md) pour afficher les messages qui ont été mis en file d’attente pendant plus d’une heure et prendre des mesures avant que le nombre de messages en file d’attente devienne trop important.</span><span class="sxs-lookup"><span data-stu-id="491e8-134">Even if the queued message volume hasn't exceeded the threshold and generated an alert, you can still use the **Queues** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) to see messages that have been queued for more than one hour, and take action before the number of queued messages becomes too large.</span></span>

![Widget files d’attente dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-queues-widget.png)

<span data-ttu-id="491e8-136">Si vous cliquez sur le nombre de messages dans le widget, un menu volant en **file d’attente de messages** s’affiche avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="491e8-136">If you click the number of messages on the widget, a **Messages queued** flyout appears with the following information:</span></span>

- <span data-ttu-id="491e8-137">**Nombre de messages en file d’attente**</span><span class="sxs-lookup"><span data-stu-id="491e8-137">**Number of queued messages**</span></span>
- <span data-ttu-id="491e8-138">**Nom du connecteur**: cliquez sur le nom du connecteur pour gérer le connecteur dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="491e8-138">**Connector name**: Click on the connector name to manage the connector in the Exchange admin center (EAC).</span></span>
- <span data-ttu-id="491e8-139">**Heure de début de la file d’attente**</span><span class="sxs-lookup"><span data-stu-id="491e8-139">**Queue started time**</span></span>
- <span data-ttu-id="491e8-140">**Messages les plus anciens expirés**</span><span class="sxs-lookup"><span data-stu-id="491e8-140">**Oldest messages expired**</span></span>
- <span data-ttu-id="491e8-141">**Serveur de destination**</span><span class="sxs-lookup"><span data-stu-id="491e8-141">**Destination server**</span></span>
- <span data-ttu-id="491e8-142">**Dernière adresse IP**</span><span class="sxs-lookup"><span data-stu-id="491e8-142">**Last IP address**</span></span>
- <span data-ttu-id="491e8-143">**Dernière erreur**</span><span class="sxs-lookup"><span data-stu-id="491e8-143">**Last error**</span></span>
- <span data-ttu-id="491e8-144">**Résolution**: les problèmes et solutions courants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="491e8-144">**How to fix**: Common issues and solutions are available.</span></span> <span data-ttu-id="491e8-145">Si le lien **Fix It Now** est disponible, cliquez dessus pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="491e8-145">If is a **Fix it now** link is available, click it to fix the problem.</span></span> <span data-ttu-id="491e8-146">Dans le cas contraire, cliquez sur les liens disponibles pour obtenir plus d’informations sur l’erreur et les solutions possibles.</span><span class="sxs-lookup"><span data-stu-id="491e8-146">Otherwise, click on any available links for more information about the error and possible solutions.</span></span>

![Détails après avoir cliqué sur l’aperçu des files d’attente dans le tableau de bord de flux de messagerie](../../media/mfi-queues-details.png)

<span data-ttu-id="491e8-148">La même fenêtre mobile s’affiche lorsque vous cliquez sur **afficher la file d’attente** dans l’alerte les détails d’un **message ont été retardé** .</span><span class="sxs-lookup"><span data-stu-id="491e8-148">The same flyout is displayed after you click **View queue** in the details of a **Messages have been delayed** alert.</span></span>

![Les messages d’alerte ont été retardés dans le centre de sécurité & conformité](../../media/mfi-queued-messages-alert-details.png)

## <a name="see-also"></a><span data-ttu-id="491e8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="491e8-150">See also</span></span>

<span data-ttu-id="491e8-151">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="491e8-151">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
