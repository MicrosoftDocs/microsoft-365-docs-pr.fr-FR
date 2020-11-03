---
title: Accéder au centre de notifications pour afficher et approuver vos tâches d’enquête et de correction automatisées
description: Utiliser le centre de notifications pour afficher des détails sur l’enquête automatiser et approuver les actions en attente
keywords: Centre de notifications, protection contre les menaces, enquête, alerte, en attente, automatisé, détection
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.date: 09/16/2020
ms.openlocfilehash: 3ec17204903f3e83f3fbfd126d57d0b9ca5d56f7
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843791"
---
# <a name="the-action-center"></a><span data-ttu-id="a6018-104">Le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="a6018-104">The Action center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a6018-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a6018-105">**Applies to:**</span></span>
- <span data-ttu-id="a6018-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a6018-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a6018-107">Utilisez le centre de notifications pour afficher les résultats des enquêtes actuelles et antérieures sur les appareils et les boîtes aux lettres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a6018-107">Use the Action center to see the results of current and past investigations across your organization's devices and mailboxes.</span></span> <span data-ttu-id="a6018-108">Selon le type de menace et le verdict résultant, les [actions de correction](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) se produisent automatiquement ou après approbation de l’équipe des opérations de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a6018-108">Depending on the type of threat and resulting verdict, [remediation actions](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-remediation-actions) occur automatically or upon approval by your organization's security operations team.</span></span> <span data-ttu-id="a6018-109">Toutes les actions de correction, qu’elles soient en attente d’approbation ou qu’elles aient déjà été approuvées, sont regroupées dans le centre de notifications.</span><span class="sxs-lookup"><span data-stu-id="a6018-109">All remediation actions, whether they are pending approval or were already approved, are consolidated in the Action center.</span></span> 

![Centre de notifications](../../media/air-actioncenter.png)

## <a name="a-single-pane-of-glass-experience"></a><span data-ttu-id="a6018-111">Expérience de type « écran unique »</span><span class="sxs-lookup"><span data-stu-id="a6018-111">A "single pane of glass" experience</span></span>

<span data-ttu-id="a6018-112">Le centre de notifications offre une expérience de type « écran unique » pour certaines tâches :</span><span class="sxs-lookup"><span data-stu-id="a6018-112">The Action center provides a "single pane of glass" experience for tasks, such as:</span></span>
- <span data-ttu-id="a6018-113">Approbation des actions de correction en attente ;</span><span class="sxs-lookup"><span data-stu-id="a6018-113">Approving pending remediation actions;</span></span>
- <span data-ttu-id="a6018-114">Affichage d’un journal d’audit des actions de correction déjà approuvées ; et</span><span class="sxs-lookup"><span data-stu-id="a6018-114">Viewing an audit log of already approved remediation actions; and</span></span>
- <span data-ttu-id="a6018-115">Évaluation des actions de correction terminées.</span><span class="sxs-lookup"><span data-stu-id="a6018-115">Reviewing completed remediation actions.</span></span>

<span data-ttu-id="a6018-116">Votre équipe des opérations de sécurité peut fonctionner de manière plus efficace, car le centre de maintenance offre une vue complète de Microsoft 365 Defender au travail.</span><span class="sxs-lookup"><span data-stu-id="a6018-116">Your security operations team can operate more effectively and efficiently, because the Action center provides a comprehensive view of Microsoft 365 Defender at work.</span></span>

## <a name="go-to-the-action-center"></a><span data-ttu-id="a6018-117">Accéder au centre de notifications</span><span class="sxs-lookup"><span data-stu-id="a6018-117">Go to the Action center</span></span>

1. <span data-ttu-id="a6018-118">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="a6018-118">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="a6018-119">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="a6018-119">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="a6018-120">Dans le centre de maintenance, deux onglets s’affichent : **en attente** et **historique**.</span><span class="sxs-lookup"><span data-stu-id="a6018-120">In the Action center, you'll see two tabs: **Pending** and **History**.</span></span>

    - <span data-ttu-id="a6018-121">L’onglet **En attente** répertorie les enquêtes devant être réexaminées et approuvées par un membre de l’équipe en charge des opérations de sécurité pour continuer.</span><span class="sxs-lookup"><span data-stu-id="a6018-121">The **Pending** tab lists investigations that require review and approval by someone in your security operations team to continue.</span></span> <span data-ttu-id="a6018-122">Veillez à examiner les éléments en attente affichés ici et à effectuer les actions appropriées.</span><span class="sxs-lookup"><span data-stu-id="a6018-122">Make sure to review and take action on pending items you see here.</span></span>

    - <span data-ttu-id="a6018-123">L’onglet **Historique** répertorie les enquêtes passées et les actions de correction qui ont été effectuées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a6018-123">The **History** tab lists past investigations and remediation actions that were taken automatically.</span></span> <span data-ttu-id="a6018-124">Vous pouvez afficher des données pour le dernier jour, la dernière semaine, le dernier mois ou les six derniers mois.</span><span class="sxs-lookup"><span data-stu-id="a6018-124">You can view data for the past day, week, month, or six months.</span></span>

4. <span data-ttu-id="a6018-125">Pour afficher uniquement les colonnes désirées, sélectionnez **Personnaliser les colonnes**.</span><span class="sxs-lookup"><span data-stu-id="a6018-125">To show only the columns you want to see, select **Customize columns**.</span></span><br/><span data-ttu-id="a6018-126">![Centre de maintenance dans Microsoft 365 Defender](../../media/mtp-action-center.png)</span><span class="sxs-lookup"><span data-stu-id="a6018-126">![Action Center in Microsoft 365 Defender](../../media/mtp-action-center.png)</span></span>

5. <span data-ttu-id="a6018-127">Sélectionnez un élément dans la liste pour afficher des détails supplémentaires sur une enquête.</span><span class="sxs-lookup"><span data-stu-id="a6018-127">Select an item in the list to view more details about an investigation.</span></span> <span data-ttu-id="a6018-128">La vue Détails de l’enquête s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="a6018-128">The investigation details view opens.</span></span><br/>![Détails de l’enquête](../../media/mtp-air-investdetails.png)

    - <span data-ttu-id="a6018-130">Si l’enquête concerne du contenu de messagerie (par exemple, l’entité est une boîte aux lettres), des détails d’enquête s’ouvrent dans le centre de sécurité & conformité ( [https://protection.office.com/threatinvestigation](https://protection.office.com/threatinvestigation) ).</span><span class="sxs-lookup"><span data-stu-id="a6018-130">If the investigation pertains to email content (such as, the entity is a mailbox), investigation details open in the Security & Compliance Center ([https://protection.office.com/threatinvestigation](https://protection.office.com/threatinvestigation)).</span></span> 

    - <span data-ttu-id="a6018-131">Si l’enquête implique un appareil, les détails de l’enquête s’affichent dans le centre de sécurité ([https://security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="a6018-131">If the investigation involves a device, investigation details open in the security center ([https://security.microsoft.com](https://security.microsoft.com)).</span></span> 

> [!TIP]
> <span data-ttu-id="a6018-132">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft 365 Defender, faites-le nous savoir !</span><span class="sxs-lookup"><span data-stu-id="a6018-132">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft 365 Defender, let us know!</span></span> <span data-ttu-id="a6018-133">Découvrez [Comment signaler les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatiques de Microsoft 365 Defender](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="a6018-133">See [How to report false positives/negatives in automated investigation and response (AIR) capabilities in Microsoft 365 Defender](mtp-autoir-report-false-positives-negatives.md).</span></span>

## <a name="available-actions"></a><span data-ttu-id="a6018-134">Actions disponibles</span><span class="sxs-lookup"><span data-stu-id="a6018-134">Available actions</span></span>

<span data-ttu-id="a6018-135">Les actions de correction étant prises, elles sont répertoriées sous l’onglet historique dans le centre de maintenance.</span><span class="sxs-lookup"><span data-stu-id="a6018-135">As remediation actions are taken, they're listed on the History tab in the Action center.</span></span> <span data-ttu-id="a6018-136">Ces actions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6018-136">Such actions include the following:</span></span>

- <span data-ttu-id="a6018-137">Collecter un package d’enquête</span><span class="sxs-lookup"><span data-stu-id="a6018-137">Collect investigation package</span></span> 
- <span data-ttu-id="a6018-138">Isoler l’appareil (cette action peut être inachevée)</span><span class="sxs-lookup"><span data-stu-id="a6018-138">Isolate device (this action can be undone)</span></span> 
- <span data-ttu-id="a6018-139">Ordinateur débarquement</span><span class="sxs-lookup"><span data-stu-id="a6018-139">Offboard machine</span></span> 
- <span data-ttu-id="a6018-140">Exécution du code de la version</span><span class="sxs-lookup"><span data-stu-id="a6018-140">Release code execution</span></span> 
- <span data-ttu-id="a6018-141">Débloquer de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6018-141">Release from quarantine</span></span> 
- <span data-ttu-id="a6018-142">Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="a6018-142">Request sample</span></span> 
- <span data-ttu-id="a6018-143">Restreindre l’exécution du code (cette action peut être terminée)</span><span class="sxs-lookup"><span data-stu-id="a6018-143">Restrict code execution (this action can be undone)</span></span> 
- <span data-ttu-id="a6018-144">Exécuter l’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="a6018-144">Run antivirus scan</span></span> 
- <span data-ttu-id="a6018-145">Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="a6018-145">Stop and quarantine</span></span> 

## <a name="required-permissions-for-action-center-tasks"></a><span data-ttu-id="a6018-146">Autorisations requises pour les tâches du centre de notifications</span><span class="sxs-lookup"><span data-stu-id="a6018-146">Required permissions for Action center tasks</span></span>

<span data-ttu-id="a6018-147">Pour approuver ou rejeter des actions en attente dans le centre de notifications, vous devez disposer des autorisations définies dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="a6018-147">To approve or reject pending actions in the Action center, you must have permissions assigned as listed in the following table:</span></span>

|<span data-ttu-id="a6018-148">Action de correction</span><span class="sxs-lookup"><span data-stu-id="a6018-148">Remediation action</span></span> |<span data-ttu-id="a6018-149">Rôles et des autorisations requis</span><span class="sxs-lookup"><span data-stu-id="a6018-149">Required roles and permissions</span></span> |
|--|----|
|<span data-ttu-id="a6018-150">Microsoft Defender pour les corrections de point de terminaison (périphériques)</span><span class="sxs-lookup"><span data-stu-id="a6018-150">Microsoft Defender for Endpoint remediation (devices)</span></span> |<span data-ttu-id="a6018-151">Rôle Administrateur de la sécurité attribué dans Azure Active Directory ([https://portal.azure.com](https://portal.azure.com)) ou dans le Centre d’administration Microsoft 365 ([https://admin.microsoft.com](https://admin.microsoft.com))</span><span class="sxs-lookup"><span data-stu-id="a6018-151">Security Administrator role assigned in either Azure Active Directory ([https://portal.azure.com](https://portal.azure.com)) or the Microsoft 365 admin center ([https://admin.microsoft.com](https://admin.microsoft.com))</span></span><br/><span data-ttu-id="a6018-152">--- ou ---</span><span class="sxs-lookup"><span data-stu-id="a6018-152">--- or ---</span></span><br/><span data-ttu-id="a6018-153">Rôle actions de correction actif affecté dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a6018-153">Active remediation actions role assigned in Microsoft Defender for Endpoint</span></span> <br/> <br/> <span data-ttu-id="a6018-154">Pour en savoir plus, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6018-154">To learn more, see the following resources:</span></span> <br/><span data-ttu-id="a6018-155">- [Autorisations des rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="a6018-155">- [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)</span></span><br/><span data-ttu-id="a6018-156">- [Créer et gérer des rôles pour le contrôle d’accès basé sur un rôle (Microsoft Defender pour le point de terminaison)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles)</span><span class="sxs-lookup"><span data-stu-id="a6018-156">- [Create and manage roles for role-based access control (Microsoft Defender for Endpoint)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/user-roles)</span></span>  |
|<span data-ttu-id="a6018-157">Correctif Microsoft Defender pour Office 365 (contenu Office et courrier électronique)</span><span class="sxs-lookup"><span data-stu-id="a6018-157">Microsoft Defender for Office 365 remediation (Office content and email)</span></span>  |<span data-ttu-id="a6018-158">Rôle Administrateur de la sécurité attribué dans Azure Active Directory ([https://portal.azure.com](https://portal.azure.com)) ou dans le Centre d’administration Microsoft 365 ([https://admin.microsoft.com](https://admin.microsoft.com))</span><span class="sxs-lookup"><span data-stu-id="a6018-158">Security Administrator role assigned in either Azure Active Directory ([https://portal.azure.com](https://portal.azure.com)) or the Microsoft 365 admin center ([https://admin.microsoft.com](https://admin.microsoft.com))</span></span><br/><span data-ttu-id="a6018-159">--- et ---</span><span class="sxs-lookup"><span data-stu-id="a6018-159">--- and ---</span></span> <br/><span data-ttu-id="a6018-160">Recherche et purger le rôle auquel est attribué le centre de sécurité & conformité ( [https://protection.office.com](https://protection.office.com) )</span><span class="sxs-lookup"><span data-stu-id="a6018-160">Search and Purge role assigned the Security & Compliance Center ([https://protection.office.com](https://protection.office.com))</span></span> <br/><br/><span data-ttu-id="a6018-161">**Important** : si le rôle administrateur de sécurité est affecté uniquement dans le centre de sécurité & conformité, vous ne pourrez pas accéder au centre de maintenance ni aux fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a6018-161">**IMPORTANT** : If you have the Security Administrator role assigned only in the Security & Compliance Center, you will not be able to access the Action center or Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="a6018-162">Vous devez avoir le rôle Administrateur de la sécurité attribué dans Azure Active Directory ou dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a6018-162">You must have the Security Administrator role assigned in Azure Active Directory or the Microsoft 365 admin center.</span></span> <br/><br/><span data-ttu-id="a6018-163">Pour en savoir plus, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6018-163">To learn more, see the following resources:</span></span> <br/><span data-ttu-id="a6018-164">- [Autorisations des rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="a6018-164">- [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)</span></span><br/><span data-ttu-id="a6018-165">- [Autorisations dans le centre de sécurité & conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center)</span><span class="sxs-lookup"><span data-stu-id="a6018-165">- [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center)</span></span> |

> [!NOTE]
> <span data-ttu-id="a6018-166">Les utilisateurs qui ont le rôle Administrateur général attribué dans Azure Active Directory peuvent approuver ou rejeter toute action en attente dans le centre de notifications.</span><span class="sxs-lookup"><span data-stu-id="a6018-166">Users who have the Global Administrator role assigned in Azure Active Directory can approve or reject any pending action in the Action center.</span></span> <span data-ttu-id="a6018-167">Toutefois, il est recommandé à votre organisation de limiter le nombre de personnes auxquelles le rôle Administrateur général est attribué.</span><span class="sxs-lookup"><span data-stu-id="a6018-167">However, as a best practice, your organization should limit the number of people who have the Global Administrator role assigned.</span></span> <span data-ttu-id="a6018-168">Nous vous recommandons d’utiliser les rôles Administrateur de la sécurité, Actions de correction actives et Rechercher et purger répertoriés ci-dessus pour les autorisations du centre de notifications.</span><span class="sxs-lookup"><span data-stu-id="a6018-168">We recommend using the Security Administrator, Active remediation actions, and Search and Purge roles listed above for Action center permissions.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a6018-169">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a6018-169">Next steps</span></span> 

- [<span data-ttu-id="a6018-170">Approuver ou rejeter les actions en attente à la suite d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="a6018-170">Approve or reject pending actions following an automated investigation</span></span>](mtp-autoir-actions.md)
- [<span data-ttu-id="a6018-171">Afficher les résultats d’une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="a6018-171">View the results of an automated investigation</span></span>](mtp-autoir-results.md)

