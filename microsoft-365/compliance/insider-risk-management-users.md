---
title: Utilisateurs de la gestion des risques Insiders (aperçu)
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
ms.openlocfilehash: a9ff7e38a99a5fe5bd8da5301bec5e19bc015cf3
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42072785"
---
# <a name="insider-risk-management-users-preview"></a><span data-ttu-id="325f8-104">Utilisateurs de la gestion des risques Insiders (aperçu)</span><span class="sxs-lookup"><span data-stu-id="325f8-104">Insider risk management users (preview)</span></span>

<span data-ttu-id="325f8-105">Les utilisateurs de la gestion des risques internes sont des employés de votre organisation qui sont inclus dans une ou plusieurs stratégies de gestion des risques Insiders.</span><span class="sxs-lookup"><span data-stu-id="325f8-105">Insider risk management users are employees in your organization that are included in one or more insider risk management policies.</span></span> <span data-ttu-id="325f8-106">Utilisez le **tableau de bord utilisateurs** pour examiner rapidement les informations relatives aux risques des employés et pour ajouter un employé à une stratégie de gestion des risques inSided existante.</span><span class="sxs-lookup"><span data-stu-id="325f8-106">Use the **Users dashboard** to quickly review risk information about employees and to add an employee to an existing insider risk management policy.</span></span> <span data-ttu-id="325f8-107">Chaque utilisateur inclus dans une stratégie de gestion des risques inSided dispose des informations suivantes affichées dans le **tableau de bord utilisateurs**:</span><span class="sxs-lookup"><span data-stu-id="325f8-107">Each user included in an insider risk management policy has the following information displayed on the **Users dashboard**:</span></span>

- <span data-ttu-id="325f8-108">**Users**: nom d’utilisateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-108">**Users**: The user name for a user.</span></span>
- <span data-ttu-id="325f8-109">**Niveau de risque**:</span><span class="sxs-lookup"><span data-stu-id="325f8-109">**Risk level**:</span></span> 
- <span data-ttu-id="325f8-110">**Alertes actives**: nombre d’alertes actives pour toutes les stratégies.</span><span class="sxs-lookup"><span data-stu-id="325f8-110">**Active alerts**: The number of active alerts for all policies.</span></span>
- <span data-ttu-id="325f8-111">**Violations confirmées**: nombre de cas résolus comme *violation de stratégie confirmée* pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-111">**Confirmed violations**: The number of cases resolved as *confirmed policy violation* for the user.</span></span>
- <span data-ttu-id="325f8-112">**Cas**: dossier actif actuel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-112">**Case**: The current active case for the user.</span></span>

![Tableau de bord des utilisateurs de gestion des risques Insiders](../media/insider-risk-users-dashboard.png)

## <a name="view-user-details"></a><span data-ttu-id="325f8-114">Afficher les détails de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="325f8-114">View user details</span></span>

<span data-ttu-id="325f8-115">Pour afficher plus de détails sur l’activité des risques pour un utilisateur, ouvrez le volet Détails de l’utilisateur en double-cliquant sur un utilisateur dans le **tableau de bord utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="325f8-115">To view more details about risk activity for a user, open the user details pane by double-clicking a user in the **Users dashboard**.</span></span> <span data-ttu-id="325f8-116">Dans le volet d’informations, vous pouvez afficher les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="325f8-116">On the details pane, you can view the following information:</span></span>

- <span data-ttu-id="325f8-117">Onglet **profil utilisateur**</span><span class="sxs-lookup"><span data-stu-id="325f8-117">**User profile** tab</span></span>
    - <span data-ttu-id="325f8-118">**Nom et titre**: le nom et le titre de la position de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-118">**Name and title**: The name and position title for the user.</span></span>
    - <span data-ttu-id="325f8-119">Adresse de messagerie de l' **utilisateur**: adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-119">**User email**: The email address for the user.</span></span>
    - <span data-ttu-id="325f8-120">**Alias**: alias réseau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-120">**Alias**: The network alias for the user.</span></span>
    - <span data-ttu-id="325f8-121">**Organisation ou service**: organisation ou service de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-121">**Organization or department**: The organization or department for the user.</span></span>

- <span data-ttu-id="325f8-122">Onglet **activité utilisateur**</span><span class="sxs-lookup"><span data-stu-id="325f8-122">**User activity** tab</span></span>
    - <span data-ttu-id="325f8-123">**Historique des activités des utilisateurs récents**: répertorie les événements de déclenchement de la stratégie et les indicateurs de risque pour les activités de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-123">**History of recent user activity**: Lists both policy triggering events and risk indicators for user activities.</span></span> <span data-ttu-id="325f8-124">Un événement déclencheur peut être l’acceptation d’une date de départ ou la dernière date de travail prévue pour l’employé.</span><span class="sxs-lookup"><span data-stu-id="325f8-124">A triggering event may be the acceptance of a resignation date or the last scheduled date of work for the employee.</span></span> <span data-ttu-id="325f8-125">Les indicateurs de risque sont des activités qui sont considérées comme ayant un élément de risque et qui sont mises en correspondance avec des stratégies auxquelles l’utilisateur est inclus.</span><span class="sxs-lookup"><span data-stu-id="325f8-125">Risk indicators are activities that are determined to have an element of risk and that are matched to policies that the user is included in.</span></span> <span data-ttu-id="325f8-126">Les événements et les activités de risque sont répertoriés avec l’élément le plus récent répertorié en premier.</span><span class="sxs-lookup"><span data-stu-id="325f8-126">Events and risk activities are listed with the most recent item listed first.</span></span>

## <a name="add-a-user-to-a-policy"></a><span data-ttu-id="325f8-127">Ajouter un utilisateur à une stratégie</span><span class="sxs-lookup"><span data-stu-id="325f8-127">Add a user to a policy</span></span>

<span data-ttu-id="325f8-128">Pour ajouter un utilisateur à une stratégie de gestion des risques Insiders, utilisez l’Assistant Nouvelle stratégie ou l’onglet **utilisateurs** de la solution de **gestion des risques inSided** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="325f8-128">To add a user to an insider risk management policy, you'll either use the new policy wizard or the **Users** tab in the **Insider risk management** solution in the Microsoft 365 compliance center.</span></span>

<span data-ttu-id="325f8-129">Procédez comme suit pour ajouter un utilisateur à une stratégie d’Insider existante :</span><span class="sxs-lookup"><span data-stu-id="325f8-129">Complete the following steps to add a user to an existing insider risk policy:</span></span>

1. <span data-ttu-id="325f8-130">Dans le [Centre de conformité Microsoft 365](https://compliance.microsoft.com), accédez à **gestion des risques internes** et sélectionnez l’onglet **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="325f8-130">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Insider risk management** and select the **Users** tab.</span></span>
2. <span data-ttu-id="325f8-131">Sélectionnez **Ajouter un utilisateur à une stratégie** dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="325f8-131">Select **Add a user to a policy** on the toolbar.</span></span>
3. <span data-ttu-id="325f8-132">Dans la boîte de dialogue **Ajouter un nouvel utilisateur** , commencez à taper un nom d’utilisateur dans le champ **utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="325f8-132">On the **Add a new user** dialog, start typing a user name in the **User** field.</span></span> <span data-ttu-id="325f8-133">Sélectionnez l’utilisateur que vous souhaitez ajouter à une stratégie.</span><span class="sxs-lookup"><span data-stu-id="325f8-133">Select the user you want to add to a policy.</span></span>
4. <span data-ttu-id="325f8-134">Sélectionnez la flèche déroulante pour le champ de **stratégie** afin d’afficher les stratégies de gestion des risques d’Insider configurées.</span><span class="sxs-lookup"><span data-stu-id="325f8-134">Select the dropdown arrow for the **Policy** field to display configured insider risk management policies.</span></span> <span data-ttu-id="325f8-135">Sélectionnez la stratégie à laquelle ajouter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="325f8-135">Select the policy to add the user to.</span></span>
5. <span data-ttu-id="325f8-136">Utilisez le contrôle Slider de la **fenêtre de surveillance** pour définir les...... La plage de la fenêtre de surveillance est comprise entre 5 et 30 jours.</span><span class="sxs-lookup"><span data-stu-id="325f8-136">Use the **Monitoring window** slider control to define the...... The range for the monitoring window is 5 to 30 days.</span></span>
6. <span data-ttu-id="325f8-137">Sélectionnez **Ajouter** , puis **confirmez** l’ajout de l’utilisateur à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="325f8-137">Select **Add** and then **Confirm** to add the user to the policy.</span></span>
