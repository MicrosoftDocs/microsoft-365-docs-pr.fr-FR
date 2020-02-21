---
title: Utilisateurs de la gestion des risques internes
description: En savoir plus sur les utilisateurs de la gestion des risques internes dans Microsoft 365
keywords: Microsoft 365, gestion des risques internes, gestion des risques, conformité
localization_priority: Normal
ms.prod: Microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection: m365-security-compliance
ms.openlocfilehash: 322cd0aa8b72ea2c81792b36614e87d97db87d7c
ms.sourcegitcommit: 87cc278ea2ddcd536ecfaa3dfae9a5ddaa502cf9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2020
ms.locfileid: "42179105"
---
# <a name="insider-risk-management-users"></a><span data-ttu-id="6585d-104">Utilisateurs de la gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="6585d-104">Insider risk management users</span></span>

<span data-ttu-id="6585d-105">Les utilisateurs de la gestion des risques internes sont des employés de votre organisation qui sont inclus dans une ou plusieurs stratégies de gestion des risques Insiders.</span><span class="sxs-lookup"><span data-stu-id="6585d-105">Insider risk management users are employees in your organization that are included in one or more insider risk management policies.</span></span> <span data-ttu-id="6585d-106">Utilisez le **tableau de bord utilisateurs** pour examiner rapidement les informations relatives aux risques des employés et pour ajouter un employé à une stratégie de gestion des risques inSided existante.</span><span class="sxs-lookup"><span data-stu-id="6585d-106">Use the **Users dashboard** to quickly review risk information about employees and to add an employee to an existing insider risk management policy.</span></span> <span data-ttu-id="6585d-107">Chaque utilisateur inclus dans une stratégie de gestion des risques inSided dispose des informations suivantes affichées dans le **tableau de bord utilisateurs**:</span><span class="sxs-lookup"><span data-stu-id="6585d-107">Each user included in an insider risk management policy has the following information displayed on the **Users dashboard**:</span></span>

- <span data-ttu-id="6585d-108">**Users**: nom d’utilisateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-108">**Users**: The username for a user.</span></span>
- <span data-ttu-id="6585d-109">**Niveau de risque**: niveau de risque calculé actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-109">**Risk level**: The current calculated risk level of the user.</span></span> <span data-ttu-id="6585d-110">Ce score est calculé toutes les 24 heures et utilise les scores de risque d’alerte de toutes les alertes actives associées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-110">This score is calculated every 24 hours and uses the alert risk scores from all active alerts associated to the user.</span></span>
- <span data-ttu-id="6585d-111">**Alertes actives**: nombre d’alertes actives pour toutes les stratégies.</span><span class="sxs-lookup"><span data-stu-id="6585d-111">**Active alerts**: The number of active alerts for all policies.</span></span>
- <span data-ttu-id="6585d-112">**Violations confirmées**: nombre de cas résolus comme *violation de stratégie confirmée* pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-112">**Confirmed violations**: The number of cases resolved as *confirmed policy violation* for the user.</span></span>
- <span data-ttu-id="6585d-113">**Cas**: dossier actif actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-113">**Case**: The current active case for the user.</span></span>

![Tableau de bord des utilisateurs de gestion des risques Insiders](../media/insider-risk-users-dashboard.png)

## <a name="view-user-details"></a><span data-ttu-id="6585d-115">Afficher les détails de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="6585d-115">View user details</span></span>

<span data-ttu-id="6585d-116">Pour afficher plus de détails sur l’activité des risques pour un utilisateur, ouvrez le volet Détails de l’utilisateur en double-cliquant sur un utilisateur dans le **tableau de bord utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="6585d-116">To view more details about risk activity for a user, open the user details pane by double-clicking a user in the **Users dashboard**.</span></span> <span data-ttu-id="6585d-117">Dans le volet d’informations, vous pouvez afficher les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6585d-117">On the details pane, you can view the following information:</span></span>

- <span data-ttu-id="6585d-118">Onglet **profil utilisateur**</span><span class="sxs-lookup"><span data-stu-id="6585d-118">**User profile** tab</span></span>
    - <span data-ttu-id="6585d-119">**Nom et titre**: le nom et le titre de la position de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-119">**Name and title**: The name and position title for the user.</span></span>
    - <span data-ttu-id="6585d-120">Adresse de messagerie de l' **utilisateur**: adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-120">**User email**: The email address for the user.</span></span>
    - <span data-ttu-id="6585d-121">**Alias**: alias réseau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-121">**Alias**: The network alias for the user.</span></span>
    - <span data-ttu-id="6585d-122">**Organisation ou service**: organisation ou service de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-122">**Organization or department**: The organization or department for the user.</span></span>

- <span data-ttu-id="6585d-123">Onglet **activité utilisateur**</span><span class="sxs-lookup"><span data-stu-id="6585d-123">**User activity** tab</span></span>
    - <span data-ttu-id="6585d-124">**Historique des activités des utilisateurs récents**: répertorie les événements de déclenchement de la stratégie et les indicateurs de risque pour les activités de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-124">**History of recent user activity**: Lists both policy triggering events and risk indicators for user activities.</span></span> <span data-ttu-id="6585d-125">Un événement déclencheur peut être l’acceptation d’une date de départ ou la dernière date de travail prévue pour l’employé.</span><span class="sxs-lookup"><span data-stu-id="6585d-125">A triggering event may be the acceptance of a resignation date or the last scheduled date of work for the employee.</span></span> <span data-ttu-id="6585d-126">Les indicateurs de risque sont des activités qui sont considérées comme ayant un élément de risque et qui sont mises en correspondance avec des stratégies auxquelles l’utilisateur est inclus.</span><span class="sxs-lookup"><span data-stu-id="6585d-126">Risk indicators are activities that are determined to have an element of risk and that are matched to policies that the user is included in.</span></span> <span data-ttu-id="6585d-127">Les événements et les activités de risque sont répertoriés avec l’élément le plus récent répertorié en premier.</span><span class="sxs-lookup"><span data-stu-id="6585d-127">Events and risk activities are listed with the most recent item listed first.</span></span>

## <a name="add-a-user-to-a-policy"></a><span data-ttu-id="6585d-128">Ajouter un utilisateur à une stratégie</span><span class="sxs-lookup"><span data-stu-id="6585d-128">Add a user to a policy</span></span>

<span data-ttu-id="6585d-129">Pour ajouter un utilisateur à une stratégie de gestion des risques Insiders, utilisez l’Assistant Nouvelle stratégie ou l’onglet **utilisateurs** de la solution de **gestion des risques inSided** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6585d-129">To add a user to an insider risk management policy, you'll either use the new policy wizard or the **Users** tab in the **Insider risk management** solution in the Microsoft 365 compliance center.</span></span>

<span data-ttu-id="6585d-130">Procédez comme suit pour ajouter un utilisateur à une stratégie d’Insider existante :</span><span class="sxs-lookup"><span data-stu-id="6585d-130">Complete the following steps to add a user to an existing insider risk policy:</span></span>

1. <span data-ttu-id="6585d-131">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com), accédez à **gestion des risques internes** et sélectionnez l’onglet **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="6585d-131">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Users** tab.</span></span>
2. <span data-ttu-id="6585d-132">Sélectionnez **Ajouter un utilisateur à une stratégie** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="6585d-132">Select **Add a user to a policy** on the toolbar.</span></span>
3. <span data-ttu-id="6585d-133">Dans la boîte de dialogue **Ajouter un nouvel utilisateur** , commencez à taper un nom d’utilisateur dans le champ **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="6585d-133">On the **Add a new user** dialog, start typing a user name in the **User** field.</span></span> <span data-ttu-id="6585d-134">Sélectionnez l’utilisateur que vous souhaitez ajouter à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="6585d-134">Select the user you want to add to a policy.</span></span>
4. <span data-ttu-id="6585d-135">Sélectionnez la flèche déroulante pour le champ de **stratégie** afin d’afficher les stratégies de gestion des risques d’Insider configurées.</span><span class="sxs-lookup"><span data-stu-id="6585d-135">Select the dropdown arrow for the **Policy** field to display configured insider risk management policies.</span></span> <span data-ttu-id="6585d-136">Sélectionnez la stratégie à laquelle ajouter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6585d-136">Select the policy to add the user to.</span></span>
5. <span data-ttu-id="6585d-137">Utilisez le contrôle Slider de la **fenêtre d’activation** pour définir la durée pendant laquelle la stratégie est active pour cet utilisateur et elle est déclenchée lorsque l’utilisateur effectue la première activité correspondant à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6585d-137">Use the **Activation window** slider control to define how long the policy is active for this user and is triggered when the user performs the first activity matching the policy.</span></span> <span data-ttu-id="6585d-138">La plage de la fenêtre de surveillance est comprise entre 5 et 30 jours.</span><span class="sxs-lookup"><span data-stu-id="6585d-138">The range for the monitoring window is 5 to 30 days.</span></span>
6. <span data-ttu-id="6585d-139">Sélectionnez **Ajouter** , puis **confirmez** l’ajout de l’utilisateur à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6585d-139">Select **Add** and then **Confirm** to add the user to the policy.</span></span>
