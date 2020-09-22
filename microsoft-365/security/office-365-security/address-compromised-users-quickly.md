---
title: Adresser des comptes d’utilisateurs compromis avec une enquête et une réponse automatisées
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection, compromis
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
ms.date: 02/25/2020
description: Découvrez comment accélérer le processus de détection et d’adressage des comptes d’utilisateurs compromis avec des fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: fa648b33180cab7d70348dc4d1d6e64930ecff99
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201230"
---
# <a name="address-compromised-user-accounts-with-automated-investigation-and-response"></a><span data-ttu-id="f1ea9-104">Adresser des comptes d’utilisateurs compromis avec une enquête et une réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="f1ea9-104">Address compromised user accounts with automated investigation and response</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="f1ea9-105">[Office 365 Advanced Threat Protection Plan 2](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide#office-365-atp-plan-1-and-plan-2) inclut de puissantes fonctionnalités d’analyse [et de réponse automatisées](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) (air).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-105">[Office 365 Advanced Threat Protection Plan 2](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide#office-365-atp-plan-1-and-plan-2) includes powerful [automated investigation and response](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air) (AIR) capabilities.</span></span> <span data-ttu-id="f1ea9-106">De telles fonctionnalités peuvent permettre à l’équipe de vos opérations de sécurité de gagner beaucoup de temps et d’efforts sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-106">Such capabilities can save your security operations team a lot of time and effort dealing with threats.</span></span> <span data-ttu-id="f1ea9-107">Microsoft continue d’améliorer les fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-107">Microsoft continues to improve security capabilities.</span></span> <span data-ttu-id="f1ea9-108">Récemment, les fonctionnalités AIR ont été améliorées pour inclure un manuel de sécurité de l’utilisateur compromis (actuellement en version d’évaluation).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-108">Recently, AIR capabilities were enhanced to include a compromised user security playbook (currently in preview).</span></span> <span data-ttu-id="f1ea9-109">Lisez cet article pour en savoir plus sur le manifeste de sécurité de l’utilisateur compromis.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-109">Read this article to learn more about the compromised user security playbook.</span></span> <span data-ttu-id="f1ea9-110">Pour plus d’informations, reportez-vous au billet de blog [accélérer le temps nécessaire pour détecter et répondre à la compromission d’un utilisateur et limiter la portée de violation avec Office 365 ATP](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Speed-up-time-to-detect-and-respond-to-user-compromise-and-limit/ba-p/977053) .</span><span class="sxs-lookup"><span data-stu-id="f1ea9-110">And see the blog post [Speed up time to detect and respond to user compromise and limit breach scope with Office 365 ATP](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Speed-up-time-to-detect-and-respond-to-user-compromise-and-limit/ba-p/977053) for additional details.</span></span>

![Enquête automatisée pour un utilisateur compromis](/microsoft-365/media/office365atp-compduserinvestigation.jpg)

<span data-ttu-id="f1ea9-112">Les manifestes de sécurité de l’utilisateur compromis permettent à l’équipe de sécurité de votre organisation de :</span><span class="sxs-lookup"><span data-stu-id="f1ea9-112">The compromised user security playbook enables your organization's security team to:</span></span>

- <span data-ttu-id="f1ea9-113">Accélérer la détection des comptes d’utilisateurs compromis ;</span><span class="sxs-lookup"><span data-stu-id="f1ea9-113">Speed up detection of compromised user accounts;</span></span>

- <span data-ttu-id="f1ea9-114">Limiter l’étendue d’une violation lorsqu’un compte est compromis ; les</span><span class="sxs-lookup"><span data-stu-id="f1ea9-114">Limit the scope of a breach when an account is compromised; and</span></span>

- <span data-ttu-id="f1ea9-115">Répondez plus efficacement aux utilisateurs compromis.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-115">Respond to compromised users more effectively and efficiently.</span></span>

## <a name="compromised-user-alerts"></a><span data-ttu-id="f1ea9-116">Alertes utilisateur compromises</span><span class="sxs-lookup"><span data-stu-id="f1ea9-116">Compromised user alerts</span></span>

<span data-ttu-id="f1ea9-117">Lorsqu’un compte d’utilisateur est compromis, des comportements atypiques ou anormaux se produisent.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-117">When a user account is compromised, atypical or anomalous behaviors occur.</span></span> <span data-ttu-id="f1ea9-118">Par exemple, les messages de hameçonnage et de courrier indésirable peuvent être envoyés en interne à partir d’un compte d’utilisateur approuvé.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-118">For example, phishing and spam messages might be sent internally from a trusted user account.</span></span> <span data-ttu-id="f1ea9-119">Office 365 Advanced Threat Protection peut détecter de telles anomalies dans les modèles de courrier électronique et l’activité de collaboration dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-119">Office 365 Advanced Threat Protection can detect such anomalies in email patterns and collaboration activity within Office 365.</span></span> <span data-ttu-id="f1ea9-120">Lorsque cela se produit, les alertes sont déclenchées et le processus de minimisation des menaces commence.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-120">When this happens, alerts are triggered, and the threat mitigation process begins.</span></span>

<span data-ttu-id="f1ea9-121">Par exemple, voici une alerte qui a été déclenchée en raison d’un envoi de courrier électronique suspect :</span><span class="sxs-lookup"><span data-stu-id="f1ea9-121">For example, here's an alert that was triggered because of suspicious email sending:</span></span>

![Alerte déclenchée en raison d’un envoi suspect de courrier électronique](/microsoft-365/media/office365atp-suspiciousemailsendalert.jpg)

<span data-ttu-id="f1ea9-123">Et voici un exemple d’alerte déclenchée lorsqu’une limite d’envoi a été atteinte pour un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f1ea9-123">And here's an example of an alert that was triggered when a sending limit was reached for a user:</span></span>

![Alerte déclenchée par la limite d’envoi atteinte](/microsoft-365/media/office365atp-sendinglimitreached.jpg)

## <a name="investigate-and-respond-to-a-compromised-user"></a><span data-ttu-id="f1ea9-125">Examiner et répondre à un utilisateur compromis</span><span class="sxs-lookup"><span data-stu-id="f1ea9-125">Investigate and respond to a compromised user</span></span>

<span data-ttu-id="f1ea9-126">Lorsqu’un compte d’utilisateur est compromis, des alertes sont déclenchées.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-126">When a user account is compromised, alerts are triggered.</span></span> <span data-ttu-id="f1ea9-127">Dans certains cas, ce compte d’utilisateur est bloqué et ne peut pas envoyer d’autres messages électroniques tant que le problème n’est pas résolu par l’équipe des opérations de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-127">And in some cases, that user account is blocked and prevented from sending any further email messages until the issue is resolved by your organization's security operations team.</span></span> <span data-ttu-id="f1ea9-128">Dans les autres cas, une enquête automatisée commence, ce qui peut entraîner des actions recommandées que votre équipe de sécurité doit prendre.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-128">In other cases, an automated investigation begins which can result in recommended actions that your security team should take.</span></span>

- [<span data-ttu-id="f1ea9-129">Afficher et examiner les utilisateurs avec accès restreint</span><span class="sxs-lookup"><span data-stu-id="f1ea9-129">View and investigate restricted users</span></span>](#view-and-investigate-restricted-users)

- [<span data-ttu-id="f1ea9-130">Afficher les détails des enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="f1ea9-130">View details about automated investigations</span></span>](#view-details-about-automated-investigations)

> [!IMPORTANT]
> <span data-ttu-id="f1ea9-131">Vous devez disposer des autorisations appropriées pour effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-131">You must have appropriate permissions to perform the following tasks.</span></span> <span data-ttu-id="f1ea9-132">Consultez la rubrique [Required Permissions to use air Capabilities](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air?view=o365-worldwide#required-permissions-to-use-air-capabilities).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-132">See [Required permissions to use AIR capabilities](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air?view=o365-worldwide#required-permissions-to-use-air-capabilities).</span></span>

### <a name="view-and-investigate-restricted-users"></a><span data-ttu-id="f1ea9-133">Afficher et examiner les utilisateurs avec accès restreint</span><span class="sxs-lookup"><span data-stu-id="f1ea9-133">View and investigate restricted users</span></span>

<span data-ttu-id="f1ea9-134">Vous disposez de plusieurs options pour accéder à une liste d’utilisateurs restreints.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-134">You have a few options for navigating to a list of restricted users.</span></span> <span data-ttu-id="f1ea9-135">Par exemple, dans le centre de sécurité & conformité, vous pouvez accéder à la **gestion des menaces**  >  **examiner**  >  **les utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-135">For example, in the Security & Compliance Center, you can go to **Threat management** > **Review** > **Restricted Users**.</span></span> <span data-ttu-id="f1ea9-136">La procédure suivante décrit la navigation à l’aide du tableau de bord **alertes** , qui permet de visualiser les différents types d’alertes qui ont pu être déclenchés.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-136">The following procedure describes navigation using the **Alerts** dashboard, which is a good way to see various kinds of alerts that might have been triggered.</span></span>

1. <span data-ttu-id="f1ea9-137">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-137">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span>

2. <span data-ttu-id="f1ea9-138">Dans le volet de navigation, **Alerts**choisissez  >  **tableau de bord**alertes.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-138">In the navigation pane, choose **Alerts** > **Dashboard**.</span></span>

3. <span data-ttu-id="f1ea9-139">Dans le widget **autres alertes** , choisissez **utilisateurs restreints**.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-139">In the **Other alerts** widget, choose **Restricted Users**.</span></span>

   ![Autre widget alertes](/microsoft-365/media/office365atp-otheralertswidget.jpg)

   <span data-ttu-id="f1ea9-141">La liste des utilisateurs avec accès restreint s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-141">This opens the list of restricted users.</span></span><br/>![Utilisateurs restreints dans Office 365](/microsoft-365/media/office365atp-restrictedusers.jpg)

4. <span data-ttu-id="f1ea9-143">Sélectionnez un compte d’utilisateur dans la liste pour afficher les détails et effectuer une action, par exemple, [libérer l’utilisateur restreint](https://docs.microsoft.com/microsoft-365/security/office-365-security/removing-user-from-restricted-users-portal-after-spam).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-143">Select a user account in the list to view details and take action, such as [releasing the restricted user](https://docs.microsoft.com/microsoft-365/security/office-365-security/removing-user-from-restricted-users-portal-after-spam).</span></span>

### <a name="view-details-about-automated-investigations"></a><span data-ttu-id="f1ea9-144">Afficher les détails des enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="f1ea9-144">View details about automated investigations</span></span>

<span data-ttu-id="f1ea9-145">Lorsqu’une enquête automatisée a commencé, vous pouvez consulter ses détails et résultats dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-145">When an automated investigation has begun, you can see its details and results in the Security & Compliance Center.</span></span> <span data-ttu-id="f1ea9-146">Accédez aux **Threat management**  >  **enquêtes**de gestion des menaces, puis sélectionnez une enquête pour en afficher les détails.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-146">Go to **Threat management** > **Investigations**, and then select an investigation to view its details.</span></span>

<span data-ttu-id="f1ea9-147">Pour en savoir plus, consultez la rubrique [afficher les détails d’une enquête](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-view-investigation-results).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-147">To learn more, see [View details of an investigation](https://docs.microsoft.com/microsoft-365/security/office-365-security/air-view-investigation-results).</span></span>

## <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="f1ea9-148">Gardez les points suivants à l’esprit</span><span class="sxs-lookup"><span data-stu-id="f1ea9-148">Keep the following points in mind</span></span>

- <span data-ttu-id="f1ea9-149">**Restez au fait des alertes**.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-149">**Stay on top of your alerts**.</span></span> <span data-ttu-id="f1ea9-150">Comme vous le sachiez, plus un compromis est long, plus le risque d’impact et de coût étendu pour votre organisation, vos clients et vos partenaires est élevé.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-150">As you know, the longer a compromise goes undetected, the larger the potential for widespread impact and cost to your organization, customers, and partners.</span></span> <span data-ttu-id="f1ea9-151">La détection précoce et la réponse opportune sont essentielles pour atténuer les menaces, et notamment lorsque le compte d’un utilisateur est compromis.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-151">Early detection and timely response are critical to mitigate threats, and especially when a user's account is compromised.</span></span>

- <span data-ttu-id="f1ea9-152">**L’automatisation aide, mais ne remplace pas, votre équipe de sécurité des opérations**.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-152">**Automation assists, but does not replace, your security operations team**.</span></span> <span data-ttu-id="f1ea9-153">Les fonctionnalités d’analyse et de réponse automatisées peuvent détecter rapidement un utilisateur compromis, mais votre équipe des opérations de sécurité devra probablement s’engager et effectuer des recherches et des corrections.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-153">Automated investigation and response capabilities can detect a compromised user early on, but your security operations team will likely need to engage and do some investigation and remediation.</span></span> <span data-ttu-id="f1ea9-154">Vous avez besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="f1ea9-154">Need some help with this?</span></span> <span data-ttu-id="f1ea9-155">Voir [examiner et approuver des actions](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air#review-and-approve-actions).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-155">See [Review and approve actions](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air#review-and-approve-actions).</span></span>

- <span data-ttu-id="f1ea9-156">**Ne reposez pas sur une alerte de connexion suspecte comme seul indicateur**.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-156">**Don't rely on a suspicious login alert as your only indicator**.</span></span> <span data-ttu-id="f1ea9-157">Lorsqu’un compte d’utilisateur est compromis, il se peut qu’il déclenche ou non une alerte de connexion suspecte.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-157">When a user account is compromised, it might or might not trigger a suspicious login alert.</span></span> <span data-ttu-id="f1ea9-158">Parfois, il s’agit de la série d’activités qui se produisent après la compromission d’un compte qui déclenche une alerte.</span><span class="sxs-lookup"><span data-stu-id="f1ea9-158">Sometimes it's the series of activities that occur after an account is compromised that triggers an alert.</span></span> <span data-ttu-id="f1ea9-159">Vous souhaitez en savoir plus sur les alertes ?</span><span class="sxs-lookup"><span data-stu-id="f1ea9-159">Want to know more about alerts?</span></span> <span data-ttu-id="f1ea9-160">Consultez la rubrique [Alert Policies](https://docs.microsoft.com/microsoft-365/compliance/alert-policies).</span><span class="sxs-lookup"><span data-stu-id="f1ea9-160">See [Alert policies](https://docs.microsoft.com/microsoft-365/compliance/alert-policies).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f1ea9-161">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f1ea9-161">Next steps</span></span>

- [<span data-ttu-id="f1ea9-162">Vérifier les autorisations requises pour utiliser les fonctionnalités AIR</span><span class="sxs-lookup"><span data-stu-id="f1ea9-162">Review the required permissions to use AIR capabilities</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air?view=o365-worldwide#required-permissions-to-use-air-capabilities)

- [<span data-ttu-id="f1ea9-163">Rechercher et identifier des courriers électroniques malveillants dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f1ea9-163">Find and investigate malicious email in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/investigate-malicious-email-that-was-delivered?view=o365-worldwide)

- [<span data-ttu-id="f1ea9-164">En savoir plus sur AIR dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="f1ea9-164">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

- [<span data-ttu-id="f1ea9-165">Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer</span><span class="sxs-lookup"><span data-stu-id="f1ea9-165">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)

