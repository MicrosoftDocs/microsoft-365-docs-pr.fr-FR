---
title: Configurer Microsoft Learning (prévisualisation) dans le Centre d Teams’administration Microsoft
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: ''
audience: admin
ms.topic: article
ms.service: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-viva-learning
localization_priority: None
description: Découvrez comment configurer Microsoft Learning (prévisualisation) dans le centre d Teams’administration microsoft.
ms.openlocfilehash: 860f16bee7d93f2212072c5d738263402704272f
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789230"
---
# <a name="set-up-microsoft-viva-learning-preview-in-the-teams-admin-center"></a><span data-ttu-id="5ce28-103">Configurer Microsoft Learning (prévisualisation) dans le Centre d Teams’administration Microsoft</span><span class="sxs-lookup"><span data-stu-id="5ce28-103">Set up Microsoft Viva Learning (Preview) in the Teams admin center</span></span>

> [!NOTE]
> <span data-ttu-id="5ce28-104">Les informations de cet article concernent un produit d’aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="5ce28-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> 

<span data-ttu-id="5ce28-105">L’administrateur Teams doit effectuer certaines étapes pour activer l’Apprentissage Paréo (Prévisualisation) pour ses utilisateurs dans le client.</span><span class="sxs-lookup"><span data-stu-id="5ce28-105">The Teams administrator needs to perform certain steps to enable Viva Learning (Preview) for their users in the tenant.</span></span> <span data-ttu-id="5ce28-106">Ces étapes varient en fonction de la façon dont le client est activé : prévisualisation [*publique*](set-up-teams-admin-center.md#public-preview-tenants) ou [ *prévisualisation privée* (ou bêta).](set-up-teams-admin-center.md#private-preview-tenants)</span><span class="sxs-lookup"><span data-stu-id="5ce28-106">These steps vary based on how the tenant is enabled:  [*Public Preview*](set-up-teams-admin-center.md#public-preview-tenants) or [*Private Preview* (or Beta)](set-up-teams-admin-center.md#private-preview-tenants).</span></span>

## <a name="public-preview-tenants"></a><span data-ttu-id="5ce28-107">Locataires de la prévisualisation publique</span><span class="sxs-lookup"><span data-stu-id="5ce28-107">Public Preview tenants</span></span>

### <a name="administrator-steps-for-public-preview-tenants"></a><span data-ttu-id="5ce28-108">Étapes de l’administrateur pour les locataires de la prévisualisation publique</span><span class="sxs-lookup"><span data-stu-id="5ce28-108">Administrator steps for Public Preview tenants</span></span>

<span data-ttu-id="5ce28-109">Étant donné que la version préliminaire de l’apprentissage n’est pas encore disponible en général, certaines étapes sont nécessaires pour activer les fonctionnalités et définir des autorisations pour des utilisateurs ou des groupes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5ce28-109">Because the Viva Learning (Preview) is not yet generally available, certain steps are required to enable the features and set permissions for specific users or groups.</span></span> 

1. <span data-ttu-id="5ce28-110">Activez les fonctionnalités de prévisualisation publique pour les utilisateurs d’Learning (prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="5ce28-110">Enable Public Preview features for Viva Learning (Preview) users.</span></span>

    <span data-ttu-id="5ce28-111">a.</span><span class="sxs-lookup"><span data-stu-id="5ce28-111">a.</span></span> <span data-ttu-id="5ce28-112">Modifiez Teams de mise à jour pour activer les fonctionnalités de prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="5ce28-112">Modify Teams update policy to enable Public Preview features.</span></span> <span data-ttu-id="5ce28-113">Voir [Microsoft Teams prévisualisation publique.](/microsoftteams/public-preview-doc-updates)</span><span class="sxs-lookup"><span data-stu-id="5ce28-113">See [Microsoft Teams Public Preview](/microsoftteams/public-preview-doc-updates).</span></span>

    <span data-ttu-id="5ce28-114">b.</span><span class="sxs-lookup"><span data-stu-id="5ce28-114">b.</span></span> <span data-ttu-id="5ce28-115">Activez la stratégie de mise à jour pour les utilisateurs ou les groupes qui effectueront des tests d’apprentissage en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="5ce28-115">Enable the update policy for users or groups who will perform Viva Learning (Preview) testing.</span></span> <span data-ttu-id="5ce28-116">Voir [Attribuer des stratégies à des utilisateurs et des groupes.](/microsoftteams/assign-policies-users-and-groups)</span><span class="sxs-lookup"><span data-stu-id="5ce28-116">See [Assign policies to users and groups](/microsoftteams/assign-policies-users-and-groups).</span></span>

2. <span data-ttu-id="5ce28-117">Modifiez la stratégie d’autorisation d’application pour les utilisateurs d’Learning (prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="5ce28-117">Modify the app permission policy for Viva Learning (Preview) users.</span></span>

    <span data-ttu-id="5ce28-118">a.</span><span class="sxs-lookup"><span data-stu-id="5ce28-118">a.</span></span> <span data-ttu-id="5ce28-119">Sauf si elle fait actuellement partie de la stratégie globale, autorisez toutes les applications Microsoft dans la stratégie d’autorisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="5ce28-119">Unless it's currently part of the global policy, allow all Microsoft apps in the app permission policy.</span></span> <span data-ttu-id="5ce28-120">Voir [Gérer les stratégies d’autorisation d’application dans Microsoft Teams](/microsoftteams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="5ce28-120">See [Manage app permission policies in Microsoft Teams](/microsoftteams/teams-app-permission-policies).</span></span> 

    <span data-ttu-id="5ce28-121">b.</span><span class="sxs-lookup"><span data-stu-id="5ce28-121">b.</span></span> <span data-ttu-id="5ce28-122">Activez la stratégie d’autorisation de l’application pour les utilisateurs ou les groupes qui effectueront des tests d’apprentissage en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="5ce28-122">Enable the app permission policy for users or groups who will perform Viva Learning (Preview) testing.</span></span> <span data-ttu-id="5ce28-123">Voir [Attribuer des stratégies à des utilisateurs et des groupes.](/microsoftteams/assign-policies-users-and-groups)</span><span class="sxs-lookup"><span data-stu-id="5ce28-123">See [Assign policies to users and groups](/microsoftteams/assign-policies-users-and-groups).</span></span>

3.  <span data-ttu-id="5ce28-124">Informez les utilisateurs qui testent Learning (Prévisualisation) pour basculer leur client de build vers la [prévisualisation](set-up-teams-admin-center.md#user-steps-for-public-preview-tenants)publique pour Teams .</span><span class="sxs-lookup"><span data-stu-id="5ce28-124">Notify users who will test Viva Learning (Preview) to [switch their build client to Public Preview for Teams](set-up-teams-admin-center.md#user-steps-for-public-preview-tenants).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ce28-125">Pour les locataires de la prévisualisation publique,  Learning (prévisualisation) ne sera pas affiché dans les applications gérées dans le centre d’administration Teams jusqu’à la publication finale du produit.</span><span class="sxs-lookup"><span data-stu-id="5ce28-125">For Public Preview tenants, Viva Learning (Preview) will not be displayed in **Managed apps** in the Teams admin center until final product release.</span></span> <span data-ttu-id="5ce28-126">Toutefois, les utilisateurs de la prévisualisation publique activée peuvent trouver Learning Learning (Prévisualisation) dans le magasin d’applications Teams et l’utiliser, une fois que les stratégies et autorisations correctes ont été définies.</span><span class="sxs-lookup"><span data-stu-id="5ce28-126">However, enabled Public Preview users can find Viva Learning (Preview) in the Teams app store and use it, once the correct policies and permissions have been set up.</span></span>

### <a name="user-steps-for-public-preview-tenants"></a><span data-ttu-id="5ce28-127">Étapes utilisateur pour les locataires de la prévisualisation publique</span><span class="sxs-lookup"><span data-stu-id="5ce28-127">User steps for Public Preview tenants</span></span>

<span data-ttu-id="5ce28-128">Les utilisateurs qui ont été activés pour le test [](/microsoftteams/public-preview-doc-updates#enable-public-preview) de prévisualisation publique, en activant les stratégies décrites précédemment, [](set-up-teams-admin-center.md#administrator-steps-for-public-preview-tenants) doivent basculer vers la prévisualisation publique dans leur client Teams client.</span><span class="sxs-lookup"><span data-stu-id="5ce28-128">Users who have been enabled for Public Preview testing — by enabling the [policies previously described](set-up-teams-admin-center.md#administrator-steps-for-public-preview-tenants) — need to [switch to Public Preview](/microsoftteams/public-preview-doc-updates#enable-public-preview) in their Teams client.</span></span>

1. <span data-ttu-id="5ce28-129">Les utilisateurs doivent sélectionner leur image de profil > **à propos de** la  >  **prévisualisation publique.**</span><span class="sxs-lookup"><span data-stu-id="5ce28-129">Users must select their profile image > **About** > **Public Preview**.</span></span>
   
    ![Navigation supérieure dans l’application Teams montrant le profil de l’utilisateur](../media/learning/learning-app-select-profile-teams.png)
    
2. <span data-ttu-id="5ce28-131">Les utilisateurs doivent accepter les conditions générales de la prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="5ce28-131">Users must accept the Public Preview terms and conditions.</span></span>

    ![Basculer vers la version d’aperçu public](../media/learning/learning-app-switch-to-public-preview.png)
 
3. <span data-ttu-id="5ce28-133">Les utilisateurs peuvent désormais trouver Learning Learning (prévisualisation) dans le Teams’application store et commencer à l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ce28-133">Users can now find Viva Learning (Preview) in the Teams app store and start using it.</span></span>

## <a name="private-preview-tenants"></a><span data-ttu-id="5ce28-134">Locataires de la prévisualisation privée</span><span class="sxs-lookup"><span data-stu-id="5ce28-134">Private Preview tenants</span></span>

### <a name="administrator-steps-for-private-preview-or-beta-tenants"></a><span data-ttu-id="5ce28-135">Étapes de l’administrateur pour les locataires de prévisualisation privée (ou bêta)</span><span class="sxs-lookup"><span data-stu-id="5ce28-135">Administrator steps for Private Preview (or Beta) tenants</span></span>

<span data-ttu-id="5ce28-136">Pour les locataires de la prévisualisation privée, aucune stratégie supplémentaire ne doit être activée.</span><span class="sxs-lookup"><span data-stu-id="5ce28-136">For Private Preview tenants, there are no additional policies that need to be enabled.</span></span> <span data-ttu-id="5ce28-137">Toutefois, Vous devez mettre à disposition des utilisateurs de votre organisation l’apprentissage en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="5ce28-137">However, Viva Learning (Preview) must be made available for users in your organization.</span></span>

1. <span data-ttu-id="5ce28-138">Dans le navigation gauche du centre d’administration Teams, Teams **applications Gérer**  >  **les applications.**</span><span class="sxs-lookup"><span data-stu-id="5ce28-138">In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.</span></span>

   ![Navigation gauche dans le centre d Teams d’administration affichant Teams applications et la section Gérer les applications.](../media/learning/learning-app-teams-manage-apps-nav.png)

2. <span data-ttu-id="5ce28-140">Dans la page **Gérer les applications,** dans la zone de recherche, tapez *Learning,* puis sélectionnez **Learning (Prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="5ce28-140">On the **Manage apps** page, in the search box, type *Viva Learning*, and then select **Viva Learning (Preview)**.</span></span>

   ![Page Gérer les applications dans le centre Teams’administration affichant la zone de recherche.](../media/learning/learning-app-teams-manage-apps-page.png)

3. <span data-ttu-id="5ce28-142">Dans la page **Learning (Prévisualisation),** sous **État,** sélectionnez **Autorisé** à activer Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="5ce28-142">On the **Viva Learning (Preview)** page, under **Status**, select **Allowed** to turn on Viva Learning (Preview).</span></span>

   ![Page d’apprentissage dans Teams centre d’administration affichant la section Paramètres de l’état et de l’application.](../media/learning/learning-app-teams-learning-page.png)


<!---
The Teams admin installs Viva Learning (Preview) and applies permission policies through the Teams admin center.

1. For Viva Learning (Preview), you must first set the Update policy in Teams. For more information, see [Microsoft Teams Public Preview](/MicrosoftTeams/public-preview-doc-updates).

    1. Sign in to the Teams admin center.

    2. Select **Teams** > **Update policies**.

    3. Select **Add**. 

    4. Name the update policy, add a policy, and turn on **Show preview features**.

2. The admin must notify users of the policy update so that they move their build into the Public Preview for Teams. 

    1. Users must select their profile image > **About** > **Public Preview**.
   
        ![Upper navigation in the Teams application showing user's profile](../media/learning/learning-app-select-profile-teams.png)
    
    2. Users must accept the **Public preview** terms and conditions.

        ![Switch to public preview build](../media/learning/learning-app-switch-to-public-preview.png)
 
3. For organizations that have restrictive policies and need to enable Viva Learning (Preview), follow the process in the next section.

## Manage settings for Viva Learning (Preview)

You must be an administrator in the Teams admin center to perform these tasks.

To make Viva Learning (Preview) available for users in your organization, follow these steps:

1. In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.

   ![Left navigation in the Teams admin center showing Teams apps and Manage apps section.](../media/learning/learning-app-teams-manage-apps-nav.png)

2. On the **Manage apps** page, in the search box, type *Viva learning*, and then select **Viva Learning (Preview)**.

   ![Manage apps page in the Teams admin center showing the search box.](../media/learning/learning-app-teams-manage-apps-page.png)

3. On the **Viva Learning (Preview)** page:

   1. Under **Status**, select **Allowed** to turn on Viva Learning (Preview).

   2. On the **Settings** tab, under **App settings**, go to the Microsoft 365 admin center to [configure learning content sources](content-sources-365-admin-center.md).

   ![Learning page in the Teams admin center showing Status and App settings section.](../media/learning/learning-app-teams-learning-page.png)

4. After **Manage app** settings, go to **Permission policies** and **Setup policies** to grant permission to employees who should have access to Viva Learning (Preview) as part of your organization's participation in the preview.

> [!NOTE]
>  If your organization is in Ring 4.0 as part of Teams TAP100 program, you might need to enable approved users in Ring 3.0 to access Viva Learning (Preview). <br><br>As part of the preview, Viva Learning (Preview) is released in Ring 3.0. If your organization is in Ring 4.0, you won’t see Viva Learning (Preview) on the **Manage apps** page. To test the app, you need to create a custom apps permission policy, set it to **Allow all apps**, and assign it to Ring 3.0 approved users. <br><br>   ![TAP-AppsPermission-Plcy page showing Allow all apps selected.](../media/learning/learning-app-tap-appspermission-plcy.png)

--->

## <a name="next-step"></a><span data-ttu-id="5ce28-144">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5ce28-144">Next step</span></span>

[<span data-ttu-id="5ce28-145">Configurer des sources de contenu d’apprentissage pour Learning Learning (prévisualisation) dans le centre d Microsoft 365'administration</span><span class="sxs-lookup"><span data-stu-id="5ce28-145">Configure learning content sources for Viva Learning (Preview) in the Microsoft 365 admin center</span></span>](content-sources-365-admin-center.md)
