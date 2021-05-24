---
title: Configurer Microsoft Learning (prévisualisation) dans le Centre d Teams’administration Microsoft
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 05/12/2021
audience: admin
ms.topic: article
ms.service: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-viva-learning
localization_priority: None
description: Découvrez comment configurer Microsoft Learning (prévisualisation) dans le centre d Teams’administration Microsoft.
ms.openlocfilehash: e5af676752064738e26f9b934a60973cb9b0200d
ms.sourcegitcommit: 686f192e1a650ec805fe8e908b46ca51771ed41f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52625297"
---
# <a name="set-up-microsoft-viva-learning-preview-in-the-teams-admin-center"></a><span data-ttu-id="934e3-103">Configurer Microsoft Learning (prévisualisation) dans le Centre d Teams’administration Microsoft</span><span class="sxs-lookup"><span data-stu-id="934e3-103">Set up Microsoft Viva Learning (Preview) in the Teams admin center</span></span>

> [!NOTE]
> <span data-ttu-id="934e3-104">Les informations de cet article concernent un produit d’aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="934e3-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> 

<span data-ttu-id="934e3-105">L’administrateur Teams installe Learning (Prévisualisation) et applique des stratégies d’autorisation via Teams centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="934e3-105">The Teams admin installs Viva Learning (Preview) and applies permission policies through the Teams admin center.</span></span>

1. <span data-ttu-id="934e3-106">Pour la prévisualisation publique, vous devez d’abord définir la stratégie de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="934e3-106">For Public Preview, you must first set the Update policy.</span></span> <span data-ttu-id="934e3-107">Pour plus d’informations, voir la Teams site Microsoft Teams [prévisualisation publique.](/MicrosoftTeams/public-preview-doc-updates)</span><span class="sxs-lookup"><span data-stu-id="934e3-107">For more details, see the Teams site [Microsoft Teams Public Preview](/MicrosoftTeams/public-preview-doc-updates).</span></span>

    1. <span data-ttu-id="934e3-108">Connectez-vous au centre Teams’administration.</span><span class="sxs-lookup"><span data-stu-id="934e3-108">Sign in to the Teams admin center.</span></span>

    2. <span data-ttu-id="934e3-109">Sélectionnez **Teams**  >  **stratégies de mise à jour.**</span><span class="sxs-lookup"><span data-stu-id="934e3-109">Select **Teams** > **Update policies**.</span></span>

    3. <span data-ttu-id="934e3-110">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="934e3-110">Select **Add**.</span></span> 

    4. <span data-ttu-id="934e3-111">Nommez la stratégie de mise à jour, ajoutez une stratégie et activer **Afficher les fonctionnalités d’aperçu.**</span><span class="sxs-lookup"><span data-stu-id="934e3-111">Name the update policy, add a policy, and turn on **Show preview features**.</span></span>

2. <span data-ttu-id="934e3-112">L’administrateur doit informer les utilisateurs de la mise à jour de la stratégie afin qu’ils déplacent leur build vers la prévisualisation publique pour Teams.</span><span class="sxs-lookup"><span data-stu-id="934e3-112">The admin must notify users of the policy update so that they move their build into Public Preview for Teams.</span></span> 

    1. <span data-ttu-id="934e3-113">L’utilisateur doit sélectionner son image de profil --> à propos de --> prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="934e3-113">User must select their profile image --> About --> Public Preview.</span></span>
   
        ![Navigation supérieure dans l’application Teams montrant le profil de l’utilisateur](../media/learning/learning-app-select-profile-teams.png)
    
    2. <span data-ttu-id="934e3-115">L’utilisateur doit accepter les termes de la prévisualisation publique.</span><span class="sxs-lookup"><span data-stu-id="934e3-115">User must accept terms of Public Preview.</span></span>

        ![Basculer vers la version d’aperçu public](../media/learning/learning-app-switch-to-public-preview.png)
 
3. <span data-ttu-id="934e3-117">Pour les organisations qui ont des stratégies restrictives et qui doivent activer Learning, suivez le processus de la section suivante.</span><span class="sxs-lookup"><span data-stu-id="934e3-117">For organizations that have restrictive policies and need to enable Viva Learning, follow the process in the next section.</span></span>

## <a name="manage-settings-for-viva-learning-preview"></a><span data-ttu-id="934e3-118">Gérer les paramètres de Learning Learning (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="934e3-118">Manage settings for Viva Learning (Preview)</span></span>

<span data-ttu-id="934e3-119">Vous devez être administrateur dans le Centre d Teams pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="934e3-119">You must be an administrator in the Teams admin center to perform these tasks.</span></span>

<span data-ttu-id="934e3-120">Pour mettre à disposition des utilisateurs de votre organisation l’apprentissage en prévisualisation, suivez les étapes ci-après :</span><span class="sxs-lookup"><span data-stu-id="934e3-120">To make Viva Learning (Preview) available for users in your organization, follow these steps:</span></span>

1. <span data-ttu-id="934e3-121">Dans le navigation gauche du centre d Teams d’administration, Teams **applications Gérer**  >  **les applications.**</span><span class="sxs-lookup"><span data-stu-id="934e3-121">In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.</span></span>

   ![Navigation gauche dans le centre d Teams d’administration affichant Teams applications et la section Gérer les applications.](../media/learning/learning-app-teams-manage-apps-nav.png)

2. <span data-ttu-id="934e3-123">Dans la page **Gérer les applications,** dans la zone de recherche, tapez *Learning,* puis **sélectionnez Learning (Prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="934e3-123">On the **Manage apps** page, in the search box, type *Viva learning*, and then select **Viva Learning (Preview)**.</span></span>

   ![Page Gérer les applications dans le centre Teams’administration affichant la zone de recherche.](../media/learning/learning-app-teams-manage-apps-page.png)

3. <span data-ttu-id="934e3-125">Dans la page **Learning (Prévisualisation)** :</span><span class="sxs-lookup"><span data-stu-id="934e3-125">On the **Viva Learning (Preview)** page:</span></span>

   1. <span data-ttu-id="934e3-126">Sous **État,** **sélectionnez Autorisé** à activer Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="934e3-126">Under **Status**, select **Allowed** to turn on Viva Learning (Preview).</span></span>

   2. <span data-ttu-id="934e3-127">Sous **l’onglet Paramètres,** sous **Paramètres** de l’application, allez dans le centre d’administration Microsoft 365 pour configurer les sources de [contenu d’apprentissage.](content-sources-365-admin-center.md)</span><span class="sxs-lookup"><span data-stu-id="934e3-127">On the **Settings** tab, under **App settings**, go to the Microsoft 365 admin center to [configure learning content sources](content-sources-365-admin-center.md).</span></span>

   ![Page d’apprentissage dans Teams centre d’administration affichant la section Paramètres de l’état et de l’application.](../media/learning/learning-app-teams-learning-page.png)

4. <span data-ttu-id="934e3-129">Après avoir gérer les  paramètres  de l’application, accédez aux stratégies d’autorisation et aux stratégies d’installation pour accorder l’autorisation aux employés qui doivent avoir accès à Learning (Preview) dans le cadre de la participation de votre organisation à la prévisualisation. </span><span class="sxs-lookup"><span data-stu-id="934e3-129">After **Manage app** settings, go to **Permission policies** and **Setup policies** to grant permission to employees who should have access to Viva Learning (Preview) as part of your organization's participation in the preview.</span></span>

> [!NOTE]
>  <span data-ttu-id="934e3-130">Si votre organisation est dans Ring 4.0 dans le cadre du programme Teams TAP100, vous devrez peut-être permettre aux utilisateurs approuvés de Ring 3.0 d’accéder à Learning (Preview).</span><span class="sxs-lookup"><span data-stu-id="934e3-130">If your organization is in Ring 4.0 as part of Teams TAP100 program, you might need to enable approved users in Ring 3.0 to access Viva Learning (Preview).</span></span> <br><br><span data-ttu-id="934e3-131">Dans le cadre de la prévisualisation, Learning (Preview) est publié dans Ring 3.0.</span><span class="sxs-lookup"><span data-stu-id="934e3-131">As part of the preview, Viva Learning (Preview) is released in Ring 3.0.</span></span> <span data-ttu-id="934e3-132">Si votre organisation est dans l’anneau 4.0, vous ne verrez pas Contrôle Learning (Prévisualisation) sur la page **Gérer les applications.**</span><span class="sxs-lookup"><span data-stu-id="934e3-132">If your organization is in Ring 4.0, you won’t see Viva Learning (Preview) on the **Manage apps** page.</span></span> <span data-ttu-id="934e3-133">Pour tester l’application, vous devez créer une stratégie d’autorisation d’application personnalisée, la définir sur Autoriser toutes les applications et l’affecter aux utilisateurs approuvés par Ring 3.0.</span><span class="sxs-lookup"><span data-stu-id="934e3-133">To test the app, you need to create a custom apps permission policy, set it to **Allow all apps**, and assign it to Ring 3.0 approved users.</span></span> <br><br>   <span data-ttu-id="934e3-134">![Page TAP-AppsPermission-Plcy affichant Autoriser toutes les applications sélectionnées.](../media/learning/learning-app-tap-appspermission-plcy.png)</span><span class="sxs-lookup"><span data-stu-id="934e3-134">![TAP-AppsPermission-Plcy page showing Allow all apps selected.](../media/learning/learning-app-tap-appspermission-plcy.png)</span></span>

## <a name="next-step"></a><span data-ttu-id="934e3-135">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="934e3-135">Next step</span></span>

[<span data-ttu-id="934e3-136">Configurer des sources de contenu d’apprentissage pour Learning Learning (prévisualisation) dans le centre d Microsoft 365'administration</span><span class="sxs-lookup"><span data-stu-id="934e3-136">Configure learning content sources for Viva Learning (Preview) in the Microsoft 365 admin center</span></span>](content-sources-365-admin-center.md)
