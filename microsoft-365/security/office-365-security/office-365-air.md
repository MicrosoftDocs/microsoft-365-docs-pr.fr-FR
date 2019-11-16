---
title: Enquêter et répondre automatiquement aux menaces dans Office 365
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 11/15/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Prise en main des fonctionnalités de réponse aux incidents automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 13f7e95829b8cf3adf17a40cf7b02c5322b15ea7
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38673420"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="2524e-104">Enquêter et répondre automatiquement aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="2524e-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="2524e-105">Overview</span></span>

<span data-ttu-id="2524e-106">En fonction de votre abonnement, [Office 365 protection avancée contre les menaces](office-365-atp.md) peut inclure des fonctionnalités de réponse aux incidents (air) automatisées qui permettent d’économiser le temps et les efforts de l’équipe des opérations de sécurité pour traiter les alertes et les menaces.</span><span class="sxs-lookup"><span data-stu-id="2524e-106">Depending on your subscription, [Office 365 Advanced Threat Protection](office-365-atp.md) can include automated incident response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span>

- <span data-ttu-id="2524e-107">Pour commencer à utiliser les fonctionnalités AIR dans Office 365, utilisez cet article.</span><span class="sxs-lookup"><span data-stu-id="2524e-107">To get started using AIR capabilities in Office 365, use this article.</span></span> 
- <span data-ttu-id="2524e-108">Pour obtenir une vue d’ensemble du fonctionnement de l’avion, voir [réponse automatique aux incidents dans Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="2524e-108">To get an overview of how AIR works, see [Automated incident response (AIR) in Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="2524e-109">Avec AIR, lorsque certaines alertes sont déclenchées, un ou plusieurs règles de sécurité se déclenchent et une enquête automatisée commence.</span><span class="sxs-lookup"><span data-stu-id="2524e-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="2524e-110">Pendant et après un processus d’enquête automatisé, l’équipe des administrateurs et des opérations de sécurité peut :</span><span class="sxs-lookup"><span data-stu-id="2524e-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="2524e-111">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="2524e-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)
- [<span data-ttu-id="2524e-112">Passer en revue et approuver les actions à la suite d’une enquête</span><span class="sxs-lookup"><span data-stu-id="2524e-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 
- [<span data-ttu-id="2524e-113">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="2524e-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="2524e-114">Vous devez disposer des autorisations appropriées pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2524e-114">You must have appropriate permissions to perform the tasks described in this article.</span></span> <span data-ttu-id="2524e-115">Par exemple, vous Myst être un administrateur général, un administrateur de sécurité, un opérateur de sécurité ou un lecteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2524e-115">For example, you myst be a global administrator, security administrator, security operator, or security reader.</span></span> <span data-ttu-id="2524e-116">[En savoir plus sur les rôles et les autorisations du centre de sécurité Microsoft 365](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="2524e-116">[Learn more about Microsoft 365 security center roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

<span data-ttu-id="2524e-117">AIR est inclus dans les abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="2524e-117">AIR is included in the following subscriptions:</span></span>
- <span data-ttu-id="2524e-118">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="2524e-118">Microsoft 365 E5</span></span>
- <span data-ttu-id="2524e-119">Microsoft 365 E5 Sécurité</span><span class="sxs-lookup"><span data-stu-id="2524e-119">Microsoft 365 E5 Security</span></span>
- <span data-ttu-id="2524e-120">Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="2524e-120">Office 365 E5</span></span>
- <span data-ttu-id="2524e-121">Office 365 – Protection avancée contre les menaces Plan 2</span><span class="sxs-lookup"><span data-stu-id="2524e-121">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="2524e-122">Si vous n’avez pas l’un de ces abonnements, [Démarrez une version d’évaluation gratuite](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="2524e-122">If you don't have one of these subscriptions, [start a free trial](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="2524e-123">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="2524e-123">View details of an investigation</span></span>

1. <span data-ttu-id="2524e-124">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2524e-124">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="2524e-125">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="2524e-125">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="2524e-126">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2524e-126">Do one of the following:</span></span>

    - <span data-ttu-id="2524e-127">Accédez au \*\*\*\* > **tableau de bord**gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2524e-127">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="2524e-128">Cela vous amène au [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="2524e-128">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="2524e-129">Vos widgets d’AIR s’affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="2524e-129">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="2524e-130">Sélectionnez un widget, par exemple, **Résumé des enquêtes**.</span><span class="sxs-lookup"><span data-stu-id="2524e-130">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="2524e-131">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2524e-131">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="2524e-132">L’une ou l’autre de ces méthodes vous permet d’accéder à une liste d’investigations.</span><span class="sxs-lookup"><span data-stu-id="2524e-132">Either method takes you to a list of investigations.</span></span>

    ![Page d’enquête principale pour l’AIR](../media/air-maininvestigationpage.png) 

3. <span data-ttu-id="2524e-134">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="2524e-134">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="2524e-135">Cette action ouvre la page des détails de l’enquête, en commençant par le graphique d’enquête dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="2524e-135">This opens investigation details page, starting with the investigation graph in view.</span></span>

    ![Page graphique d’enquête sur l’AIR](../media/air-investigationgraphpage.png)

4. <span data-ttu-id="2524e-137">Utilisez les différents onglets pour en savoir plus sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="2524e-137">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="2524e-138">Vérifier et approuver des actions</span><span class="sxs-lookup"><span data-stu-id="2524e-138">Review and approve actions</span></span>

<span data-ttu-id="2524e-139">Dans Office 365, les analyses automatiques entraînent généralement une ou plusieurs actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="2524e-139">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="2524e-140">Toutefois, aucune action n’est effectuée tant qu’elles n’ont pas été approuvées par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="2524e-140">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="2524e-141">Utilisez la procédure suivante pour passer en revue et approuver les actions.</span><span class="sxs-lookup"><span data-stu-id="2524e-141">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="2524e-142">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2524e-142">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="2524e-143">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2524e-143">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="2524e-144">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="2524e-144">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="2524e-145">Dans l’affichage Détails de l’enquête, sélectionnez l’onglet **actions** . Toutes les actions en attente d’approbation sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="2524e-145">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="2524e-146">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2524e-146">Select an item in the list.</span></span>

5. <span data-ttu-id="2524e-147">Sélectionnez **approuver** pour prendre l’action recommandée (ou **rejeter** pour fermer l’enquête sans entreprendre d’action).</span><span class="sxs-lookup"><span data-stu-id="2524e-147">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="2524e-148">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="2524e-148">View details about an alert related to an investigation</span></span>

<span data-ttu-id="2524e-149">Certains types d’alertes déclenchent une enquête automatisée dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="2524e-149">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="2524e-150">Pour en savoir plus, consultez la rubrique [alertes](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="2524e-150">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="2524e-151">Utilisez la procédure suivante pour afficher les détails d’une alerte associée à une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="2524e-151">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="2524e-152">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2524e-152">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="2524e-153">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="2524e-153">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="2524e-154">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="2524e-154">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="2524e-155">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="2524e-155">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="2524e-156">Les détails d’une enquête étant ouverts, sélectionnez l’onglet **alertes** . Les alertes qui ont déclenché l’enquête sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="2524e-156">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="2524e-157">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="2524e-157">Select an item in the list.</span></span> <span data-ttu-id="2524e-158">Un menu volant s’ouvre, avec des détails sur l’alerte et des liens vers des informations et des actions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2524e-158">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="2524e-159">Passez en revue les informations de la fenêtre mobile et, en fonction de l’alerte en particulier, effectuez une action, telle que **résoudre**, **supprimer**ou **avertir les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="2524e-159">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

    - <span data-ttu-id="2524e-160">La **résolution** équivaut à la fermeture d’une alerte</span><span class="sxs-lookup"><span data-stu-id="2524e-160">**Resolve** is equivalent to closing an alert</span></span>
    
    - <span data-ttu-id="2524e-161">La **suppression** entraîne le déclenchement d’alertes par une stratégie pendant une période de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2524e-161">**Suppress** causes a policy to not trigger alerts for a specified period of time</span></span>
    
    - <span data-ttu-id="2524e-162">**Avertir les utilisateurs** de l’envoi d’un courrier électronique avec les adresses de messagerie des utilisateurs déjà entrées, et permet à l’équipe des opérations de sécurité de taper un message pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2524e-162">**Notify users** starts an email with users' email addresses already entered, and enables your security operations team to type a message to those users.</span></span> <span data-ttu-id="2524e-163">(Ceci est similaire à l’envoi d’un message à des destinataires à l’aide de l' [Explorateur de menaces](threat-explorer.md).)</span><span class="sxs-lookup"><span data-stu-id="2524e-163">(This is similar to sending a message to recipients using [Threat Explorer](threat-explorer.md).)</span></span>  

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="2524e-164">Utiliser l’API activité de gestion d’Office 365 pour des solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="2524e-164">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="2524e-165">Si votre organisation utilise une solution de création de rapports personnalisée ou tierce, vous pouvez afficher des informations sur les analyses automatisées dans cette solution à l’aide de l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="2524e-165">If your organization is using a custom or third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="2524e-166">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="2524e-166">Use the following resources to set this up:</span></span>

|<span data-ttu-id="2524e-167">Ressource</span><span class="sxs-lookup"><span data-stu-id="2524e-167">Resource</span></span>  |<span data-ttu-id="2524e-168">Description</span><span class="sxs-lookup"><span data-stu-id="2524e-168">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="2524e-169">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-169">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="2524e-170">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2524e-170">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="2524e-171">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-171">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="2524e-172">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification à votre application pour accéder aux données d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="2524e-172">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="2524e-173">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="2524e-173">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="2524e-174">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-174">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="2524e-175">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2524e-175">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="2524e-176">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="2524e-176">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="2524e-177">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-177">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="2524e-178">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="2524e-178">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="2524e-179">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2524e-179">Next steps</span></span>

[<span data-ttu-id="2524e-180">En savoir plus sur les alertes</span><span class="sxs-lookup"><span data-stu-id="2524e-180">Learn more about alerts</span></span>](../../compliance/alert-policies.md)

[<span data-ttu-id="2524e-181">Rechercher et identifier manuellement les messages électroniques malveillants remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2524e-181">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="2524e-182">En savoir plus sur AIR dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="2524e-182">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="2524e-183">Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer</span><span class="sxs-lookup"><span data-stu-id="2524e-183">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)