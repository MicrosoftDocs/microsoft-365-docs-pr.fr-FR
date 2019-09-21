---
title: Examiner et répondre automatiquement aux menaces dans Office 365
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/18/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Prise en main des fonctionnalités de réponse aux incidents automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 5def4ab38c14629f2840e4b833fa9430d234e75c
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080224"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="c8dda-104">Examiner et répondre automatiquement aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="c8dda-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c8dda-105">Overview</span></span>

<span data-ttu-id="c8dda-106">[Office 365 protection avancée contre les menaces](office-365-atp.md) Plan 2 inclut des fonctionnalités de réponse aux incidents (AIR) qui permettent d’économiser le temps et les efforts de l’équipe des opérations de sécurité pour traiter les alertes et les menaces.</span><span class="sxs-lookup"><span data-stu-id="c8dda-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 includes automated incident response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span> 
- <span data-ttu-id="c8dda-107">Pour commencer à utiliser les fonctionnalités AIR dans Office 365, utilisez cet article.</span><span class="sxs-lookup"><span data-stu-id="c8dda-107">To get started using AIR capabilities in Office 365, use this article.</span></span> 
- <span data-ttu-id="c8dda-108">Pour obtenir une vue d’ensemble du fonctionnement de l’avion, voir [réponse automatique aux incidents dans Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="c8dda-108">To get an overview of how AIR works, see [Automated incident response (AIR) in Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="c8dda-109">Avec AIR, lorsque certaines alertes sont déclenchées, un ou plusieurs règles de sécurité se déclenchent et une enquête automatisée commence.</span><span class="sxs-lookup"><span data-stu-id="c8dda-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="c8dda-110">Pendant et après un processus d’enquête automatisé, l’équipe des administrateurs et des opérations de sécurité peut :</span><span class="sxs-lookup"><span data-stu-id="c8dda-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="c8dda-111">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="c8dda-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)
- [<span data-ttu-id="c8dda-112">Passer en revue et approuver les actions à la suite d’une enquête</span><span class="sxs-lookup"><span data-stu-id="c8dda-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 
- [<span data-ttu-id="c8dda-113">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="c8dda-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="c8dda-114">Vous devez être un administrateur général, un administrateur de sécurité, un opérateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="c8dda-114">You must be a global administrator, security administrator, security operator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="c8dda-115">Pour plus d’informations, consultez la rubrique [Microsoft 365 Security Center : Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="c8dda-115">To learn more, see [Microsoft 365 security center: roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="c8dda-116">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="c8dda-116">View details of an investigation</span></span>

1. <span data-ttu-id="c8dda-117">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="c8dda-117">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="c8dda-118">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="c8dda-118">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="c8dda-119">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8dda-119">Do one of the following:</span></span>

    - <span data-ttu-id="c8dda-120">Accédez au \*\*\*\* > **tableau de bord**gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="c8dda-120">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="c8dda-121">Cela vous amène au [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="c8dda-121">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="c8dda-122">Vos widgets d’AIR s’affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="c8dda-122">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="c8dda-123">Sélectionnez un widget, par exemple, **Résumé des enquêtes**.</span><span class="sxs-lookup"><span data-stu-id="c8dda-123">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="c8dda-124">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="c8dda-124">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="c8dda-125">L’une ou l’autre de ces méthodes vous permet d’accéder à une liste d’investigations.</span><span class="sxs-lookup"><span data-stu-id="c8dda-125">Either method takes you to a list of investigations.</span></span>

    ![Page d’enquête principale pour l’AIR](../media/air-maininvestigationpage.png) 

3. <span data-ttu-id="c8dda-127">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="c8dda-127">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="c8dda-128">Cette action ouvre la page des détails de l’enquête, en commençant par le graphique d’enquête dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="c8dda-128">This opens investigation details page, starting with the investigation graph in view.</span></span>

    ![Page graphique d’enquête sur l’AIR](../media/air-investigationgraphpage.png)

4. <span data-ttu-id="c8dda-130">Utilisez les différents onglets pour en savoir plus sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="c8dda-130">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="c8dda-131">Vérifier et approuver des actions</span><span class="sxs-lookup"><span data-stu-id="c8dda-131">Review and approve actions</span></span>

<span data-ttu-id="c8dda-132">Dans Office 365, les analyses automatiques entraînent généralement une ou plusieurs actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="c8dda-132">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="c8dda-133">Toutefois, aucune action n’est effectuée tant qu’elles n’ont pas été approuvées par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c8dda-133">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="c8dda-134">Utilisez la procédure suivante pour passer en revue et approuver les actions.</span><span class="sxs-lookup"><span data-stu-id="c8dda-134">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="c8dda-135">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="c8dda-135">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="c8dda-136">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="c8dda-136">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="c8dda-137">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="c8dda-137">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="c8dda-138">Dans l’affichage Détails de l’enquête, sélectionnez l’onglet **actions** . Toutes les actions en attente d’approbation sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="c8dda-138">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="c8dda-139">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c8dda-139">Select an item in the list.</span></span>

5. <span data-ttu-id="c8dda-140">Sélectionnez **approuver** pour prendre l’action recommandée (ou **rejeter** pour fermer l’enquête sans entreprendre d’action).</span><span class="sxs-lookup"><span data-stu-id="c8dda-140">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="c8dda-141">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="c8dda-141">View details about an alert related to an investigation</span></span>

<span data-ttu-id="c8dda-142">Certains types d’alertes déclenchent une enquête automatisée dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8dda-142">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="c8dda-143">Pour en savoir plus, consultez la rubrique [alertes](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="c8dda-143">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="c8dda-144">Utilisez la procédure suivante pour afficher les détails d’une alerte associée à une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="c8dda-144">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="c8dda-145">En tant qu’administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="c8dda-145">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="c8dda-146">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="c8dda-146">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="c8dda-147">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="c8dda-147">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="c8dda-148">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="c8dda-148">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="c8dda-149">Les détails d’une enquête étant ouverts, sélectionnez l’onglet **alertes** . Les alertes qui ont déclenché l’enquête sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="c8dda-149">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="c8dda-150">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c8dda-150">Select an item in the list.</span></span> <span data-ttu-id="c8dda-151">Un menu volant s’ouvre, avec des détails sur l’alerte et des liens vers des informations et des actions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c8dda-151">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="c8dda-152">Passez en revue les informations de la fenêtre mobile et, en fonction de l’alerte en particulier, effectuez une action, telle que **résoudre**, **supprimer**ou **avertir les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="c8dda-152">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

    - <span data-ttu-id="c8dda-153">La **résolution** équivaut à la fermeture d’une alerte</span><span class="sxs-lookup"><span data-stu-id="c8dda-153">**Resolve** is equivalent to closing an alert</span></span>
    
    - <span data-ttu-id="c8dda-154">La **suppression** entraîne le déclenchement d’alertes par une stratégie pendant une période de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c8dda-154">**Suppress** causes a policy to not trigger alerts for a specified period of time</span></span>
    
    - <span data-ttu-id="c8dda-155">**Avertir les utilisateurs** de l’envoi d’un courrier électronique avec les adresses de messagerie des utilisateurs déjà entrées, et permet à l’équipe des opérations de sécurité de taper un message pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c8dda-155">**Notify users** starts an email with users' email addresses already entered, and enables your security operations team to type a message to those users.</span></span> <span data-ttu-id="c8dda-156">(Ceci est similaire à l’envoi d’un message à des destinataires à l’aide de l' [Explorateur de menaces](threat-explorer.md).)</span><span class="sxs-lookup"><span data-stu-id="c8dda-156">(This is similar to sending a message to recipients using [Threat Explorer](threat-explorer.md).)</span></span>  

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="c8dda-157">Utiliser l’API activité de gestion d’Office 365 pour des solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="c8dda-157">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="c8dda-158">Si votre organisation utilise une solution de création de rapports personnalisée ou tierce, vous pouvez afficher des informations sur les analyses automatisées dans cette solution à l’aide de l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8dda-158">If your organization is using a custom or third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="c8dda-159">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="c8dda-159">Use the following resources to set this up:</span></span>

|<span data-ttu-id="c8dda-160">Ressource</span><span class="sxs-lookup"><span data-stu-id="c8dda-160">Resource</span></span>  |<span data-ttu-id="c8dda-161">Description</span><span class="sxs-lookup"><span data-stu-id="c8dda-161">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="c8dda-162">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-162">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="c8dda-163">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8dda-163">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="c8dda-164">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-164">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="c8dda-165">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification à votre application pour accéder aux données d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8dda-165">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="c8dda-166">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="c8dda-166">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="c8dda-167">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-167">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="c8dda-168">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c8dda-168">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="c8dda-169">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="c8dda-169">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="c8dda-170">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-170">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="c8dda-171">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="c8dda-171">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="c8dda-172">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c8dda-172">Next steps</span></span>

[<span data-ttu-id="c8dda-173">En savoir plus sur les alertes</span><span class="sxs-lookup"><span data-stu-id="c8dda-173">Learn more about alerts</span></span>](../../compliance/alert-policies.md)

[<span data-ttu-id="c8dda-174">Rechercher et identifier manuellement les messages électroniques malveillants remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c8dda-174">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="c8dda-175">En savoir plus sur AIR dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="c8dda-175">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="c8dda-176">Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer</span><span class="sxs-lookup"><span data-stu-id="c8dda-176">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)