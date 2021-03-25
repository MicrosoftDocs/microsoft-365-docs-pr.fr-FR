---
title: Résoudre les comptes d’utilisateur compromis grâce à un examen et une réponse automatisés
keywords: AIR, autoIR, ATP, automatisé, examen, réponse, correction, menaces, avancé, menace, protection, compromission
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
ms.date: 02/25/2020
description: Découvrez comment accélérer le processus de détection et de traitement des comptes d’utilisateur compromis à l’aide de fonctionnalités automatisées d’examen et de réponse dans Microsoft Defender pour Office 365 Plan 2.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 2428cc2c1f82b4f2b881433fde991dd04b268d6e
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204800"
---
# <a name="address-compromised-user-accounts-with-automated-investigation-and-response"></a><span data-ttu-id="3a983-104">Résoudre les comptes d’utilisateur compromis grâce à un examen et à une réponse automatisés</span><span class="sxs-lookup"><span data-stu-id="3a983-104">Address compromised user accounts with automated investigation and response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="3a983-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3a983-105">**Applies to**</span></span>
- [<span data-ttu-id="3a983-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="3a983-106">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="3a983-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="3a983-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="3a983-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3a983-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)


<span data-ttu-id="3a983-109">[Microsoft Defender pour Office 365 Plan 2 inclut](defender-for-office-365.md#microsoft-defender-for-office-365-plan-1-and-plan-2) de puissantes fonctionnalités d’investigation [et](office-365-air.md) de réponse automatisées (AIR).</span><span class="sxs-lookup"><span data-stu-id="3a983-109">[Microsoft Defender for Office 365 Plan 2](defender-for-office-365.md#microsoft-defender-for-office-365-plan-1-and-plan-2) includes powerful [automated investigation and response](office-365-air.md) (AIR) capabilities.</span></span> <span data-ttu-id="3a983-110">Ces fonctionnalités peuvent faire gagner beaucoup de temps et d’efforts à votre équipe en matière d’opérations de sécurité pour gérer les menaces.</span><span class="sxs-lookup"><span data-stu-id="3a983-110">Such capabilities can save your security operations team a lot of time and effort dealing with threats.</span></span> <span data-ttu-id="3a983-111">Microsoft continue d’améliorer les fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3a983-111">Microsoft continues to improve security capabilities.</span></span> <span data-ttu-id="3a983-112">Récemment, les fonctionnalités AIR ont été améliorées pour inclure un manuel de sécurité utilisateur compromis (actuellement en prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="3a983-112">Recently, AIR capabilities were enhanced to include a compromised user security playbook (currently in preview).</span></span> <span data-ttu-id="3a983-113">Lisez cet article pour en savoir plus sur le manuel de sécurité des utilisateurs compromis.</span><span class="sxs-lookup"><span data-stu-id="3a983-113">Read this article to learn more about the compromised user security playbook.</span></span> <span data-ttu-id="3a983-114">Pour plus d’informations, voir le billet de blog Accélérer le temps de détection et de réponse à la compromission de l’utilisateur et limiter l’étendue des violations avec [Microsoft Defender pour Office 365.](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Speed-up-time-to-detect-and-respond-to-user-compromise-and-limit/ba-p/977053)</span><span class="sxs-lookup"><span data-stu-id="3a983-114">And see the blog post [Speed up time to detect and respond to user compromise and limit breach scope with Microsoft Defender for Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Speed-up-time-to-detect-and-respond-to-user-compromise-and-limit/ba-p/977053) for additional details.</span></span>

![Examen automatisé pour un utilisateur compromis](/microsoft-365/media/office365atp-compduserinvestigation.jpg)

<span data-ttu-id="3a983-116">Le manuel de sécurité des utilisateurs compromis permet à l’équipe de sécurité de votre organisation de :</span><span class="sxs-lookup"><span data-stu-id="3a983-116">The compromised user security playbook enables your organization's security team to:</span></span>

- <span data-ttu-id="3a983-117">Accélérer la détection des comptes d’utilisateur compromis ;</span><span class="sxs-lookup"><span data-stu-id="3a983-117">Speed up detection of compromised user accounts;</span></span>

- <span data-ttu-id="3a983-118">Limiter l’étendue d’une violation lorsqu’un compte est compromis ; et</span><span class="sxs-lookup"><span data-stu-id="3a983-118">Limit the scope of a breach when an account is compromised; and</span></span>

- <span data-ttu-id="3a983-119">Répondre plus efficacement aux utilisateurs compromis.</span><span class="sxs-lookup"><span data-stu-id="3a983-119">Respond to compromised users more effectively and efficiently.</span></span>

## <a name="compromised-user-alerts"></a><span data-ttu-id="3a983-120">Alertes utilisateur compromises</span><span class="sxs-lookup"><span data-stu-id="3a983-120">Compromised user alerts</span></span>

<span data-ttu-id="3a983-121">Lorsqu’un compte d’utilisateur est compromis, des comportements inhabituels ou anormaux se produisent.</span><span class="sxs-lookup"><span data-stu-id="3a983-121">When a user account is compromised, atypical or anomalous behaviors occur.</span></span> <span data-ttu-id="3a983-122">Par exemple, les messages de hameçonnage et de courrier indésirable peuvent être envoyés en interne à partir d’un compte d’utilisateur approuvé.</span><span class="sxs-lookup"><span data-stu-id="3a983-122">For example, phishing and spam messages might be sent internally from a trusted user account.</span></span> <span data-ttu-id="3a983-123">Defender pour Office 365 peut détecter de telles anomalies dans les modèles de messagerie et l’activité de collaboration dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="3a983-123">Defender for Office 365 can detect such anomalies in email patterns and collaboration activity within Office 365.</span></span> <span data-ttu-id="3a983-124">Lorsque cela se produit, les alertes sont déclenchées et le processus de prévention des menaces commence.</span><span class="sxs-lookup"><span data-stu-id="3a983-124">When this happens, alerts are triggered, and the threat mitigation process begins.</span></span>

<span data-ttu-id="3a983-125">Par exemple, voici une alerte déclenchée en raison de l’envoi de messages électroniques suspects :</span><span class="sxs-lookup"><span data-stu-id="3a983-125">For example, here's an alert that was triggered because of suspicious email sending:</span></span>

![Alerte déclenchée en raison d’un envoi de courrier suspect](/microsoft-365/media/office365atp-suspiciousemailsendalert.jpg)

<span data-ttu-id="3a983-127">Voici un exemple d’alerte déclenchée lorsqu’une limite d’envoi a été atteinte pour un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="3a983-127">And here's an example of an alert that was triggered when a sending limit was reached for a user:</span></span>

![Alerte déclenchée par la limite d’envoi atteinte](/microsoft-365/media/office365atp-sendinglimitreached.jpg)

## <a name="investigate-and-respond-to-a-compromised-user"></a><span data-ttu-id="3a983-129">Examiner un utilisateur compromis et y répondre</span><span class="sxs-lookup"><span data-stu-id="3a983-129">Investigate and respond to a compromised user</span></span>

<span data-ttu-id="3a983-130">Lorsqu’un compte d’utilisateur est compromis, des alertes sont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="3a983-130">When a user account is compromised, alerts are triggered.</span></span> <span data-ttu-id="3a983-131">Et dans certains cas, ce compte d’utilisateur est bloqué et empêché d’envoyer d’autres messages électroniques jusqu’à ce que le problème soit résolu par l’équipe des opérations de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3a983-131">And in some cases, that user account is blocked and prevented from sending any further email messages until the issue is resolved by your organization's security operations team.</span></span> <span data-ttu-id="3a983-132">Dans d’autres cas, une enquête automatisée commence, ce qui peut entraîner des actions recommandées que votre équipe de sécurité doit prendre.</span><span class="sxs-lookup"><span data-stu-id="3a983-132">In other cases, an automated investigation begins which can result in recommended actions that your security team should take.</span></span>

- [<span data-ttu-id="3a983-133">Afficher et examiner les utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="3a983-133">View and investigate restricted users</span></span>](#view-and-investigate-restricted-users)

- [<span data-ttu-id="3a983-134">Afficher les détails sur les enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="3a983-134">View details about automated investigations</span></span>](#view-details-about-automated-investigations)

> [!IMPORTANT]
> <span data-ttu-id="3a983-135">Vous devez avoir les autorisations appropriées pour effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a983-135">You must have appropriate permissions to perform the following tasks.</span></span> <span data-ttu-id="3a983-136">Voir [Autorisations requises pour utiliser les fonctionnalités AIR.](office-365-air.md#required-permissions-to-use-air-capabilities)</span><span class="sxs-lookup"><span data-stu-id="3a983-136">See [Required permissions to use AIR capabilities](office-365-air.md#required-permissions-to-use-air-capabilities).</span></span>

### <a name="view-and-investigate-restricted-users"></a><span data-ttu-id="3a983-137">Afficher et examiner les utilisateurs restreints</span><span class="sxs-lookup"><span data-stu-id="3a983-137">View and investigate restricted users</span></span>

<span data-ttu-id="3a983-138">Vous avez plusieurs options pour naviguer vers une liste d’utilisateurs restreints.</span><span class="sxs-lookup"><span data-stu-id="3a983-138">You have a few options for navigating to a list of restricted users.</span></span> <span data-ttu-id="3a983-139">Par exemple, dans le Centre de sécurité &  conformité, vous pouvez aller à La révision de la gestion des menaces \>  \> **Utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="3a983-139">For example, in the Security & Compliance Center, you can go to **Threat management** \> **Review** \> **Restricted Users**.</span></span> <span data-ttu-id="3a983-140">La procédure suivante décrit la navigation à l’aide du tableau de bord **Alertes,** qui est un bon moyen de voir différents types d’alertes qui ont pu être déclenchées.</span><span class="sxs-lookup"><span data-stu-id="3a983-140">The following procedure describes navigation using the **Alerts** dashboard, which is a good way to see various kinds of alerts that might have been triggered.</span></span>

1. <span data-ttu-id="3a983-141">Accédez à <https://protection.office.com> et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3a983-141">Go to <https://protection.office.com> and sign in.</span></span>

2. <span data-ttu-id="3a983-142">Dans le volet de navigation, sélectionnez **Tableau de bord Alertes.** \> </span><span class="sxs-lookup"><span data-stu-id="3a983-142">In the navigation pane, choose **Alerts** \> **Dashboard**.</span></span>

3. <span data-ttu-id="3a983-143">Dans le widget **Autres alertes,** choisissez **Utilisateurs restreints.**</span><span class="sxs-lookup"><span data-stu-id="3a983-143">In the **Other alerts** widget, choose **Restricted Users**.</span></span>

   ![Widget Autres alertes](/microsoft-365/media/office365atp-otheralertswidget.jpg)

   <span data-ttu-id="3a983-145">Cela ouvre la liste des utilisateurs restreints.</span><span class="sxs-lookup"><span data-stu-id="3a983-145">This opens the list of restricted users.</span></span>

   ![Utilisateurs restreints dans Office 365](/microsoft-365/media/office365atp-restrictedusers.jpg)

4. <span data-ttu-id="3a983-147">Sélectionnez un compte d’utilisateur dans la liste pour afficher les détails et prendre des mesures, telles que la [libération de l’utilisateur restreint.](removing-user-from-restricted-users-portal-after-spam.md)</span><span class="sxs-lookup"><span data-stu-id="3a983-147">Select a user account in the list to view details and take action, such as [releasing the restricted user](removing-user-from-restricted-users-portal-after-spam.md).</span></span>

### <a name="view-details-about-automated-investigations"></a><span data-ttu-id="3a983-148">Afficher les détails sur les enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="3a983-148">View details about automated investigations</span></span>

<span data-ttu-id="3a983-149">Lorsqu’une enquête automatisée a commencé, vous pouvez voir ses détails et ses résultats dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="3a983-149">When an automated investigation has begun, you can see its details and results in the Security & Compliance Center.</span></span> <span data-ttu-id="3a983-150">Go to **Threat management** \> **Investigations,** and then select an investigation to view its details.</span><span class="sxs-lookup"><span data-stu-id="3a983-150">Go to **Threat management** \> **Investigations**, and then select an investigation to view its details.</span></span>

<span data-ttu-id="3a983-151">Pour en savoir plus, [consultez les détails d’une enquête.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="3a983-151">To learn more, see [View details of an investigation](air-view-investigation-results.md).</span></span>

## <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="3a983-152">Gardez les points suivants à l’esprit</span><span class="sxs-lookup"><span data-stu-id="3a983-152">Keep the following points in mind</span></span>

- <span data-ttu-id="3a983-153">**Restez au fait de vos alertes.**</span><span class="sxs-lookup"><span data-stu-id="3a983-153">**Stay on top of your alerts**.</span></span> <span data-ttu-id="3a983-154">Comme vous le savez, plus une compromission est longue et plus le risque d’impact et de coût pour votre organisation, vos clients et vos partenaires est élevé.</span><span class="sxs-lookup"><span data-stu-id="3a983-154">As you know, the longer a compromise goes undetected, the larger the potential for widespread impact and cost to your organization, customers, and partners.</span></span> <span data-ttu-id="3a983-155">Une détection précoce et une réponse rapide sont essentielles pour atténuer les menaces, en particulier lorsque le compte d’un utilisateur est compromis.</span><span class="sxs-lookup"><span data-stu-id="3a983-155">Early detection and timely response are critical to mitigate threats, and especially when a user's account is compromised.</span></span>

- <span data-ttu-id="3a983-156">**Automation aide, mais ne remplace pas, votre équipe des opérations de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="3a983-156">**Automation assists, but does not replace, your security operations team**.</span></span> <span data-ttu-id="3a983-157">Les fonctionnalités d’examen et de réponse automatisées peuvent détecter un utilisateur compromis dès le début, mais votre équipe en matière d’opérations de sécurité devra probablement s’impliquer et faire des recherches et des corrections.</span><span class="sxs-lookup"><span data-stu-id="3a983-157">Automated investigation and response capabilities can detect a compromised user early on, but your security operations team will likely need to engage and do some investigation and remediation.</span></span> <span data-ttu-id="3a983-158">Vous avez besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="3a983-158">Need some help with this?</span></span> <span data-ttu-id="3a983-159">Voir [Examiner et approuver les actions.](air-review-approve-pending-completed-actions.md)</span><span class="sxs-lookup"><span data-stu-id="3a983-159">See [Review and approve actions](air-review-approve-pending-completed-actions.md).</span></span>

- <span data-ttu-id="3a983-160">**Ne comptez pas sur une alerte de connexion suspecte comme seul indicateur.**</span><span class="sxs-lookup"><span data-stu-id="3a983-160">**Don't rely on a suspicious login alert as your only indicator**.</span></span> <span data-ttu-id="3a983-161">Lorsqu’un compte d’utilisateur est compromis, il peut ou non déclencher une alerte de connexion suspecte.</span><span class="sxs-lookup"><span data-stu-id="3a983-161">When a user account is compromised, it might or might not trigger a suspicious login alert.</span></span> <span data-ttu-id="3a983-162">Parfois, c’est la série d’activités qui se produisent après qu’un compte est compromis qui déclenche une alerte.</span><span class="sxs-lookup"><span data-stu-id="3a983-162">Sometimes it's the series of activities that occur after an account is compromised that triggers an alert.</span></span> <span data-ttu-id="3a983-163">Vous souhaitez en savoir plus sur les alertes ?</span><span class="sxs-lookup"><span data-stu-id="3a983-163">Want to know more about alerts?</span></span> <span data-ttu-id="3a983-164">Voir [stratégies d’alerte.](../../compliance/alert-policies.md)</span><span class="sxs-lookup"><span data-stu-id="3a983-164">See [Alert policies](../../compliance/alert-policies.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="3a983-165">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3a983-165">Next steps</span></span>

- [<span data-ttu-id="3a983-166">Passer en revue les autorisations requises pour utiliser les fonctionnalités AIR</span><span class="sxs-lookup"><span data-stu-id="3a983-166">Review the required permissions to use AIR capabilities</span></span>](office-365-air.md#required-permissions-to-use-air-capabilities)

- [<span data-ttu-id="3a983-167">Rechercher et examiner les e-mails malveillants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3a983-167">Find and investigate malicious email in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

- [<span data-ttu-id="3a983-168">En savoir plus sur AIR dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3a983-168">Learn about AIR in Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

- [<span data-ttu-id="3a983-169">Consultez la feuille de route Microsoft 365 pour voir ce qui sera bientôt disponible et déployer</span><span class="sxs-lookup"><span data-stu-id="3a983-169">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)