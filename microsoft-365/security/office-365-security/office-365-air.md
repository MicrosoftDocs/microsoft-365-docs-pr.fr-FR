---
title: Enquêter et répondre automatiquement aux menaces dans Office 365
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
f1.keywords:
- NOCSH
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
description: Prise en main des fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 9c17d7219e5dd15404b171fbd6707d00fd788f19
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598761"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="35ab1-104">Enquêter et répondre automatiquement aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="35ab1-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="35ab1-105">Overview</span></span>

<span data-ttu-id="35ab1-106">En fonction de votre abonnement, [Office 365 protection avancée contre les menaces](office-365-atp.md) peut inclure des fonctionnalités d’analyse et de réponse automatisées (air) qui permettent d’économiser le temps et les efforts de l’équipe des opérations de sécurité pour traiter les alertes et les menaces.</span><span class="sxs-lookup"><span data-stu-id="35ab1-106">Depending on your subscription, [Office 365 Advanced Threat Protection](office-365-atp.md) can include automated investigation and response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span>

- <span data-ttu-id="35ab1-107">Pour commencer à utiliser les fonctionnalités d’analyse et de réponse automatisées dans Office 365, utilisez cet article.</span><span class="sxs-lookup"><span data-stu-id="35ab1-107">To get started using automated investigation and response capabilities in Office 365, use this article.</span></span> 
- <span data-ttu-id="35ab1-108">Pour obtenir une vue d’ensemble du fonctionnement, voir [Automated Investigation and Response in Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="35ab1-108">To get an overview of how it works, see [Automated investigation and response in Office 365](automated-investigation-response-office.md).</span></span>

> [!TIP]
> <span data-ttu-id="35ab1-109">Avez-vous Microsoft 365 E5 ou Microsoft 365 E3 conjointement avec identité et protection contre les menaces ?</span><span class="sxs-lookup"><span data-stu-id="35ab1-109">Do you have Microsoft 365 E5 or Microsoft 365 E3 together with Identity & Threat Protection?</span></span> <span data-ttu-id="35ab1-110">Envisagez [d’essayer l’automatisation des recherches et de la réponse (air) dans la protection contre les menaces Microsoft](../mtp/mtp-autoir.md).</span><span class="sxs-lookup"><span data-stu-id="35ab1-110">Consider trying [Automated investigation and response (AIR) in Microsoft Threat Protection](../mtp/mtp-autoir.md).</span></span>

<span data-ttu-id="35ab1-111">Avec des fonctionnalités d’analyse et de réponse automatisées, lorsque certaines alertes sont déclenchées, un ou plusieurs règles de sécurité se déclenchent et le processus d’enquête automatisé commence.</span><span class="sxs-lookup"><span data-stu-id="35ab1-111">With automated investigation and response capabilities, when certain alerts are triggered, one or more security playbooks initiate, and the automated investigation process begins.</span></span> <span data-ttu-id="35ab1-112">Pendant et après un processus d’enquête automatisé, votre équipe de sécurité peut effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="35ab1-112">During and after an automated investigation process, your security team can do the following:</span></span>

- [<span data-ttu-id="35ab1-113">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="35ab1-113">View the details of an investigation</span></span>](#view-details-of-an-investigation)
- [<span data-ttu-id="35ab1-114">Passer en revue et approuver les actions à la suite d’une enquête</span><span class="sxs-lookup"><span data-stu-id="35ab1-114">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 
- [<span data-ttu-id="35ab1-115">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="35ab1-115">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!IMPORTANT]
> <span data-ttu-id="35ab1-116">Pour effectuer les tâches décrites dans cet article, vous devez disposer des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="35ab1-116">To perform the tasks described in this article, you must have appropriate permissions assigned.</span></span> <span data-ttu-id="35ab1-117">Consultez la rubrique [Required Permissions to use air Capabilities](automated-investigation-response-office.md#required-permissions-to-use-air-capabilities).</span><span class="sxs-lookup"><span data-stu-id="35ab1-117">See [required permissions to use AIR capabilities](automated-investigation-response-office.md#required-permissions-to-use-air-capabilities).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="35ab1-118">Afficher les détails d’une enquête</span><span class="sxs-lookup"><span data-stu-id="35ab1-118">View details of an investigation</span></span>

1. <span data-ttu-id="35ab1-119">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="35ab1-119">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="35ab1-120">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="35ab1-120">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="35ab1-121">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="35ab1-121">Do one of the following:</span></span>

    - <span data-ttu-id="35ab1-122">Accédez au \*\*\*\* > **tableau de bord**gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="35ab1-122">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="35ab1-123">Cela vous amène au [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="35ab1-123">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="35ab1-124">Vos widgets d’AIR s’affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="35ab1-124">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="35ab1-125">Sélectionnez un widget, par exemple, **Résumé des enquêtes**.</span><span class="sxs-lookup"><span data-stu-id="35ab1-125">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="35ab1-126">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="35ab1-126">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="35ab1-127">L’une ou l’autre de ces méthodes vous permet d’accéder à une liste d’investigations.</span><span class="sxs-lookup"><span data-stu-id="35ab1-127">Either method takes you to a list of investigations.</span></span>

    ![Page d’enquête principale pour l’AIR](../media/air-maininvestigationpage.png) 

3. <span data-ttu-id="35ab1-129">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="35ab1-129">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="35ab1-130">Cette action ouvre la page des détails de l’enquête, en commençant par le graphique d’enquête dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="35ab1-130">This opens investigation details page, starting with the investigation graph in view.</span></span>

    ![Page graphique d’enquête sur l’AIR](../media/air-investigationgraphpage.png)

4. <span data-ttu-id="35ab1-132">Utilisez les différents onglets pour en savoir plus sur l’enquête.</span><span class="sxs-lookup"><span data-stu-id="35ab1-132">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="35ab1-133">Vérifier et approuver des actions</span><span class="sxs-lookup"><span data-stu-id="35ab1-133">Review and approve actions</span></span>

<span data-ttu-id="35ab1-134">Dans Office 365, les analyses automatiques entraînent généralement une ou plusieurs actions recommandées.</span><span class="sxs-lookup"><span data-stu-id="35ab1-134">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="35ab1-135">Toutefois, aucune action n’est effectuée tant qu’elles n’ont pas été approuvées par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35ab1-135">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="35ab1-136">Utilisez la procédure suivante pour passer en revue et approuver les actions.</span><span class="sxs-lookup"><span data-stu-id="35ab1-136">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="35ab1-137">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="35ab1-137">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="35ab1-138">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="35ab1-138">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="35ab1-139">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="35ab1-139">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="35ab1-140">Dans l’affichage Détails de l’enquête, sélectionnez l’onglet **actions** . Toutes les actions en attente d’approbation sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="35ab1-140">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="35ab1-141">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="35ab1-141">Select an item in the list.</span></span>

5. <span data-ttu-id="35ab1-142">Sélectionnez **approuver** pour prendre l’action recommandée (ou **rejeter** pour fermer l’enquête sans entreprendre d’action).</span><span class="sxs-lookup"><span data-stu-id="35ab1-142">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="35ab1-143">Afficher les détails d’une alerte liée à une enquête</span><span class="sxs-lookup"><span data-stu-id="35ab1-143">View details about an alert related to an investigation</span></span>

<span data-ttu-id="35ab1-144">Certains types d’alertes déclenchent une enquête automatisée dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="35ab1-144">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="35ab1-145">Pour en savoir plus, consultez la rubrique [alertes](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="35ab1-145">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="35ab1-146">Utilisez la procédure suivante pour afficher les détails d’une alerte associée à une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="35ab1-146">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="35ab1-147">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="35ab1-147">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="35ab1-148">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="35ab1-148">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="35ab1-149">Accédez aux \*\*\*\* > **enquêtes**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="35ab1-149">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="35ab1-150">Dans la liste des enquêtes, sélectionnez un élément dans la colonne **ID** .</span><span class="sxs-lookup"><span data-stu-id="35ab1-150">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="35ab1-151">Les détails d’une enquête étant ouverts, sélectionnez l’onglet **alertes** . Les alertes qui ont déclenché l’enquête sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="35ab1-151">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="35ab1-152">Sélectionnez un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="35ab1-152">Select an item in the list.</span></span> <span data-ttu-id="35ab1-153">Un menu volant s’ouvre, avec des détails sur l’alerte et des liens vers des informations et des actions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="35ab1-153">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="35ab1-154">Passez en revue les informations de la fenêtre mobile et, en fonction de l’alerte en particulier, effectuez une action, telle que **résoudre**, **supprimer**ou **avertir les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="35ab1-154">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

    - <span data-ttu-id="35ab1-155">La **résolution** équivaut à la fermeture d’une alerte</span><span class="sxs-lookup"><span data-stu-id="35ab1-155">**Resolve** is equivalent to closing an alert</span></span>
    
    - <span data-ttu-id="35ab1-156">La **suppression** entraîne le déclenchement d’alertes par une stratégie pendant une période de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="35ab1-156">**Suppress** causes a policy to not trigger alerts for a specified period of time</span></span>
    
    - <span data-ttu-id="35ab1-157">**Avertir les utilisateurs** de l’envoi d’un courrier électronique avec les adresses de messagerie des utilisateurs déjà entrées, et permet à l’équipe des opérations de sécurité de taper un message pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="35ab1-157">**Notify users** starts an email with users' email addresses already entered, and enables your security operations team to type a message to those users.</span></span> <span data-ttu-id="35ab1-158">(Ceci est similaire à l’envoi d’un message à des destinataires à l’aide de l' [Explorateur de menaces](threat-explorer.md).)</span><span class="sxs-lookup"><span data-stu-id="35ab1-158">(This is similar to sending a message to recipients using [Threat Explorer](threat-explorer.md).)</span></span>  

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="35ab1-159">Utiliser l’API activité de gestion d’Office 365 pour des solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="35ab1-159">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="35ab1-160">Si votre organisation utilise une solution de création de rapports personnalisée ou tierce, vous pouvez afficher des informations sur les analyses automatisées dans cette solution à l’aide de l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="35ab1-160">If your organization is using a custom or third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="35ab1-161">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="35ab1-161">Use the following resources to set this up:</span></span>

|<span data-ttu-id="35ab1-162">Resource</span><span class="sxs-lookup"><span data-stu-id="35ab1-162">Resource</span></span>  |<span data-ttu-id="35ab1-163">Description</span><span class="sxs-lookup"><span data-stu-id="35ab1-163">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="35ab1-164">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-164">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="35ab1-165">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35ab1-165">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="35ab1-166">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-166">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="35ab1-167">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification à votre application pour accéder aux données d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="35ab1-167">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="35ab1-168">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="35ab1-168">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="35ab1-169">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-169">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="35ab1-170">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="35ab1-170">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="35ab1-171">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="35ab1-171">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="35ab1-172">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-172">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="35ab1-173">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="35ab1-173">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="35ab1-174">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="35ab1-174">Next steps</span></span>

- [<span data-ttu-id="35ab1-175">Découvrez comment obtenir de l’AIR et voir les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="35ab1-175">Find out how to get AIR and see required permissions</span></span>](automated-investigation-response-office.md#how-to-get-air)
- [<span data-ttu-id="35ab1-176">En savoir plus sur les alertes</span><span class="sxs-lookup"><span data-stu-id="35ab1-176">Learn more about alerts</span></span>](../../compliance/alert-policies.md)
- [<span data-ttu-id="35ab1-177">Rechercher et identifier manuellement les messages électroniques malveillants remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="35ab1-177">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)
- [<span data-ttu-id="35ab1-178">En savoir plus sur AIR dans Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="35ab1-178">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)
- [<span data-ttu-id="35ab1-179">Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer</span><span class="sxs-lookup"><span data-stu-id="35ab1-179">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)