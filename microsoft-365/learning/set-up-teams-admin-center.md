---
title: Configurer Microsoft Learning (prévisualisation) dans le Centre d’administration Teams
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
description: Découvrez comment configurer Microsoft Learning (prévisualisation) dans le Centre d’administration Teams.
ms.openlocfilehash: 40e659796b22097f42515c0cbb704bdaa4ccc972
ms.sourcegitcommit: 967f64dfa1a05f31179c8316b96bfb7758a5d990
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52333517"
---
# <a name="set-up-microsoft-viva-learning-preview-in-the-teams-admin-center"></a><span data-ttu-id="ce45a-103">Configurer Microsoft Learning (prévisualisation) dans le Centre d’administration Teams</span><span class="sxs-lookup"><span data-stu-id="ce45a-103">Set up Microsoft Viva Learning (Preview) in the Teams admin center</span></span>

> [!NOTE]
> <span data-ttu-id="ce45a-104">Les informations de cet article concernent un produit d’aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="ce45a-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> 

<span data-ttu-id="ce45a-105">L’administrateur Teams installe Learning (prévisualisation) et applique des stratégies d’autorisation par le biais du Centre d’administration Teams.</span><span class="sxs-lookup"><span data-stu-id="ce45a-105">The Teams admin installs Viva Learning (Preview) and applies permission policies through the Teams admin center.</span></span>

## <a name="manage-settings-for-viva-learning-preview"></a><span data-ttu-id="ce45a-106">Gérer les paramètres de Learning Learning (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="ce45a-106">Manage settings for Viva Learning (Preview)</span></span>

<span data-ttu-id="ce45a-107">Vous devez être administrateur dans le Centre d’administration Teams pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="ce45a-107">You must be an administrator in the Teams admin center to perform these tasks.</span></span>

<span data-ttu-id="ce45a-108">Pour mettre à disposition des utilisateurs de votre organisation la version d’avant-première de l’apprentissage, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce45a-108">To make Viva Learning (Preview) available for users in your organization, follow these steps:</span></span>

1. <span data-ttu-id="ce45a-109">Dans le navigation de gauche du Centre d’administration Teams, allez à **Applications Teams Gérer** les  >  **applications.**</span><span class="sxs-lookup"><span data-stu-id="ce45a-109">In the left navigation of the Teams admin center, go to **Teams apps** > **Manage apps**.</span></span>

   ![Navigation gauche dans le Centre d’administration Teams affichant la section Applications Teams et Gérer les applications.](../media/learning/learning-app-teams-manage-apps-nav.png)

2. <span data-ttu-id="ce45a-111">Dans la page **Gérer les applications,** dans la zone de recherche, tapez *Learning,* puis **sélectionnez Learning (Prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="ce45a-111">On the **Manage apps** page, in the search box, type *Viva learning*, and then select **Viva Learning (Preview)**.</span></span>

   ![Page Gérer les applications dans le Centre d’administration Teams affichant la zone de recherche.](../media/learning/learning-app-teams-manage-apps-page.png)

3. <span data-ttu-id="ce45a-113">Dans la page **Learning (Prévisualisation)** :</span><span class="sxs-lookup"><span data-stu-id="ce45a-113">On the **Viva Learning (Preview)** page:</span></span>

   1. <span data-ttu-id="ce45a-114">Sous **État,** **sélectionnez Autorisé** à activer Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="ce45a-114">Under **Status**, select **Allowed** to turn on Viva Learning (Preview).</span></span>

   2. <span data-ttu-id="ce45a-115">Sous **l’onglet Paramètres,** sous **Paramètres** de l’application, allez dans le Centre d’administration Microsoft 365 pour configurer les sources de [contenu d’apprentissage.](content-sources-365-admin-center.md)</span><span class="sxs-lookup"><span data-stu-id="ce45a-115">On the **Settings** tab, under **App settings**, go to the Microsoft 365 admin center to [configure learning content sources](content-sources-365-admin-center.md).</span></span>

   ![Page d’apprentissage dans le Centre d’administration Teams affichant la section Paramètres de l’état et de l’application.](../media/learning/learning-app-teams-learning-page.png)

4. <span data-ttu-id="ce45a-117">Après avoir gérer les  paramètres  de l’application, accédez aux stratégies d’autorisation et de configuration pour accorder des autorisations aux employés qui doivent avoir accès à Learning (Preview) dans le cadre de la participation de votre organisation à la prévisualisation. </span><span class="sxs-lookup"><span data-stu-id="ce45a-117">After **Manage app** settings, go to **Permission policies** and **Setup policies** to grant permission to employees who should have access to Viva Learning (Preview) as part of your organization's participation in the preview.</span></span>

> [!NOTE]
>  <span data-ttu-id="ce45a-118">Si votre organisation est dans Ring 4.0 dans le cadre du programme TAP100 teams, vous devrez peut-être permettre aux utilisateurs approuvés de Ring 3.0 d’accéder à Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="ce45a-118">If your organization is in Ring 4.0 as part of Teams TAP100 program, you might need to enable approved users in Ring 3.0 to access Viva Learning (Preview).</span></span> <br><br><span data-ttu-id="ce45a-119">Dans le cadre de la prévisualisation, Learning (Preview) est publié dans Ring 3.0.</span><span class="sxs-lookup"><span data-stu-id="ce45a-119">As part of the preview, Viva Learning (Preview) is released in Ring 3.0.</span></span> <span data-ttu-id="ce45a-120">Si votre organisation est dans l’anneau 4.0, vous ne verrez pas Learning (Prévisualisation) sur la page Gérer **les applications.**</span><span class="sxs-lookup"><span data-stu-id="ce45a-120">If your organization is in Ring 4.0, you won’t see Viva Learning (Preview) on the **Manage apps** page.</span></span> <span data-ttu-id="ce45a-121">Pour tester l’application, vous devez créer une stratégie d’autorisation d’application personnalisée, la définir sur Autoriser toutes les applications et l’affecter aux utilisateurs approuvés par Ring 3.0.</span><span class="sxs-lookup"><span data-stu-id="ce45a-121">To test the app, you need to create a custom apps permission policy, set it to **Allow all apps**, and assign it to Ring 3.0 approved users.</span></span> <br><br>   <span data-ttu-id="ce45a-122">![Page TAP-AppsPermission-Plcy affichant Autoriser toutes les applications sélectionnées.](../media/learning/learning-app-tap-appspermission-plcy.png)</span><span class="sxs-lookup"><span data-stu-id="ce45a-122">![TAP-AppsPermission-Plcy page showing Allow all apps selected.](../media/learning/learning-app-tap-appspermission-plcy.png)</span></span>

## <a name="next-step"></a><span data-ttu-id="ce45a-123">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ce45a-123">Next step</span></span>

[<span data-ttu-id="ce45a-124">Configurer des sources de contenu d’apprentissage pour Learning Learning (prévisualisation) dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ce45a-124">Configure learning content sources for Viva Learning (Preview) in the Microsoft 365 admin center</span></span>](content-sources-365-admin-center.md)