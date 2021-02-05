---
title: Ajouter de l’espace de stockage pour votre abonnement
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- commerce
- Adm_TOC
- SPO_Content
ms.custom:
- MAX_CampaignID
- okr_SMB
- AdminSurgePortfolio
search.appverid:
- MET150
description: Découvrez comment ajouter et réduire le stockage de fichiers dans votre abonnement Microsoft 365. Avec un espace de stockage de fichiers supplémentaire, vous pouvez stocker davantage de contenu dans SharePoint Online et OneDrive.
ms.date: ''
ms.openlocfilehash: fd59de31a27a1dd29800ae1d081e1f509f399124
ms.sourcegitcommit: 0d709e9ab0d8d56c5fc11a921298f82e40e122c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "50114906"
---
# <a name="add-storage-space-for-your-subscription"></a><span data-ttu-id="2adf4-104">Ajouter de l’espace de stockage pour votre abonnement</span><span class="sxs-lookup"><span data-stu-id="2adf4-104">Add storage space for your subscription</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="2adf4-105">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="2adf4-105">The admin center is changing.</span></span> <span data-ttu-id="2adf4-106">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2adf4-106">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="2adf4-107">Si vous commencez à manquer d’espace de stockage pour vos collections de sites SharePoint Online et si votre plan est éligible, vous pouvez en ajouter à votre abonnement. </span><span class="sxs-lookup"><span data-stu-id="2adf4-107">If you start to run out of storage for your SharePoint Online site collections, you can add storage to your subscription if your plan is eligible.</span></span> <span data-ttu-id="2adf4-108">Si le stockage de fichiers supplémentaire **Office 365** ne figure pas dans la liste des modules supplémentaires disponibles, cela signifie que votre plan n’est pas éligible.</span><span class="sxs-lookup"><span data-stu-id="2adf4-108">If you don't see the **Office 365 Extra File Storage** in the list of available add-ons, it means your plan is not eligible.</span></span> <span data-ttu-id="2adf4-109">Pour plus d’informations, voir [Mon plan est-il éligible ?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span><span class="sxs-lookup"><span data-stu-id="2adf4-109">For more information, see [Is my plan eligible?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span></span>

> [!NOTE]
> <span data-ttu-id="2adf4-110">Si vous avez acheté votre abonnement par le biais de licences en volume ou d’un programme CSP, vous ne pouvez pas acheter de stockage de fichiers supplémentaire **Office 365** pour votre organisation directement auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2adf4-110">If you bought your subscription through Volume Licensing or a CSP, you can't buy **Office 365 Extra File Storage** for your organization directly from Microsoft.</span></span> <span data-ttu-id="2adf4-111">Contactez votre représentant ou partenaire pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="2adf4-111">Contact your representative or partner for help.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2adf4-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2adf4-112">Before you begin</span></span>

<span data-ttu-id="2adf4-113">Vous devez être un administrateur global ou SharePoint pour effectuer les tâches de cet article.</span><span class="sxs-lookup"><span data-stu-id="2adf4-113">You must be a Global or SharePoint admin to do the tasks in this article.</span></span> <span data-ttu-id="2adf4-114">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2adf4-114">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>

## <a name="view-available-storage"></a><span data-ttu-id="2adf4-115">Afficher le stockage disponible</span><span class="sxs-lookup"><span data-stu-id="2adf4-115">View available storage</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2adf4-116">Dans le Centre d’administration SharePoint, rendez-vous sur la page <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">Sites actifs</a> et connectez-vous avec un compte qui dispose des [autorisations](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) d’administrateur pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2adf4-116">In the SharePoint admin center, go to the <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">Active sites</a> page, and sign in with an account that has [admin permissions](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) for your organization.</span></span>

2. <span data-ttu-id="2adf4-117">Dans le coin supérieur droit de la page, consultez la quantité d’espace de stockage utilisé sur tous les sites, ainsi que l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-117">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span> <span data-ttu-id="2adf4-118">Si votre organisation a configuré Multi-Géo dans Office 365, la barre indique également la quantité de stockage utilisée dans tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="2adf4-118">If your organization has configured Multi-Geo in Office 365, the bar also shows the amount of storage used across all geo locations.</span></span>

   ![Barre de stockage sur la page des sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="2adf4-120">L’espace de stockage utilisé n’inclut pas les modifications apportées au cours des 24 à 48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="2adf4-120">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2adf4-121">Connectez-vous en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette Administrateur https://portal.office.de pour ouvrir le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="2adf4-121">Sign in to https://portal.office.de as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="2adf4-122">Si vous voyez un message vous that you don’t have permission to access the page, it means that you don’t have Microsoft 365 administrator permissions in your organization.</span><span class="sxs-lookup"><span data-stu-id="2adf4-122">If you see a message that you don't have permission to access the page, it means that you don't have Microsoft 365 administrator permissions in your organization.</span></span>

2. <span data-ttu-id="2adf4-123">Dans le volet gauche, sous **Centres d’administration,** **sélectionnez SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-123">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="2adf4-124">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2adf4-124">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="2adf4-125">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-125">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="2adf4-126">Dans le coin supérieur droit de la page, consultez la quantité d’espace de stockage utilisé sur tous les sites, ainsi que l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-126">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>

   ![Barre de stockage sur la page des sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="2adf4-128">L’espace de stockage utilisé n’inclut pas les modifications apportées au cours des 24 à 48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="2adf4-128">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2adf4-129">Connectez-vous en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette Administrateur https://login.partner.microsoftonline.cn/ pour ouvrir le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="2adf4-129">Sign in to https://login.partner.microsoftonline.cn/ as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="2adf4-130">(Si vous voyez un message vous that you don’t have permission to access the page, it means that you don’t have Microsoft 365 administrator permissions in your organization.</span><span class="sxs-lookup"><span data-stu-id="2adf4-130">(If you see a message that you don't have permission to access the page, it means that you don't have Microsoft 365 administrator permissions in your organization.</span></span>

2. <span data-ttu-id="2adf4-131">Dans le volet gauche, sous **Centres d’administration,** **sélectionnez SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-131">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="2adf4-132">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2adf4-132">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="2adf4-133">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-133">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="2adf4-134">Dans le coin supérieur droit de la page, consultez la quantité d’espace de stockage utilisé sur tous les sites, ainsi que l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-134">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>  

   ![Barre de stockage sur la page des sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="2adf4-136">L’espace de stockage utilisé n’inclut pas les modifications apportées au cours des 24 à 48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="2adf4-136">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

<span data-ttu-id="2adf4-137">Une fois que vous avez déterminé la quantité de stockage utilisée, vous pouvez ajouter ou supprimer de l'espace de stockage pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-137">After you've determined how much storage you're using, you can add or remove storage space for your subscription.</span></span> <span data-ttu-id="2adf4-138">Pour connaître le coût d’ajout d’espace de stockage, suivez les étapes de cet article et examinez les informations tarifaires avant d’acheter.</span><span class="sxs-lookup"><span data-stu-id="2adf4-138">To find out how much it will cost to add storage space, follow the steps in this article, and review the pricing information before you purchase.</span></span>
  
<span data-ttu-id="2adf4-139">Pour plus d’informations sur la définition des limites de stockage des collections de sites, voir [Gérer les limites de stockage des collections de sites.](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits)</span><span class="sxs-lookup"><span data-stu-id="2adf4-139">For information about setting site collection storage limits, see [Manage site collection storage limits](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits).</span></span>
  
## <a name="add-storage-to-your-subscription"></a><span data-ttu-id="2adf4-140">Ajouter du stockage à votre abonnement</span><span class="sxs-lookup"><span data-stu-id="2adf4-140">Add storage to your subscription</span></span>

<span data-ttu-id="2adf4-141">Si vous n’avez pas encore acheté de stockage supplémentaire pour votre abonnement, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="2adf4-141">If you haven't yet purchased extra storage for your subscription, you can do that.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2adf4-142">Dans le centre d’administration, accédez à la page **facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Acheter des services</a>.</span><span class="sxs-lookup"><span data-stu-id="2adf4-142">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>
2. <span data-ttu-id="2adf4-143">En bas de la page **Acheter des services,** sélectionnez **Modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-143">At the bottom of the **Purchase services** page, select **Add-ons**.</span></span>
3. <span data-ttu-id="2adf4-144">Sélectionnez **le stockage de fichiers supplémentaire Office 365.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-144">Select **Office 365 Extra File Storage**.</span></span>
4. <span data-ttu-id="2adf4-145">Dans la page Stockage de fichiers supplémentaire **Office 365,** si vous l’affichez, choisissez l’abonnement de base, puis entrez le nombre de gigaoctets de stockage que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="2adf4-145">On the **Office 365 Extra File Storage** page, if shown, choose the base subscription, then enter the number of gigabytes of storage you want to add.</span></span>
5. <span data-ttu-id="2adf4-146">Sélectionnez **Check out maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-146">Select **Check out now**.</span></span>
6. <span data-ttu-id="2adf4-147">Dans la page À quoi cela ressemble-t-il **?** Vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, examinez les informations de tarification, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-147">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>
7. <span data-ttu-id="2adf4-148">Dans la page **Commande complète,** vérifiez le total.</span><span class="sxs-lookup"><span data-stu-id="2adf4-148">On the **Complete order** page, verify the total.</span></span> <span data-ttu-id="2adf4-149">Si vous devez apporter des modifications, sélectionnez **Modifier l’ordre.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-149">If you need to make any changes, select **Edit order**.</span></span> <span data-ttu-id="2adf4-150">Si la commande nécessite une vérification de solvabilité, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="2adf4-150">If the order requires a credit check, select the check box.</span></span> <span data-ttu-id="2adf4-151">Lorsque vous avez terminé, sélectionnez **Passer une commande** à La page \> **d’accueil de l’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-151">When you're finished, select **Place order** \> **Go to Admin Home**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2adf4-152">Dans le Centre d’administration, allez sur la page  \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements de facturation.</a>  </span><span class="sxs-lookup"><span data-stu-id="2adf4-152">In the admin center, go to the **Billing** \>  <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="2adf4-153">Dans la page **Abonnements,** choisissez l’abonnement auquel vous souhaitez ajouter de l’espace de stockage, puis sélectionnez **Modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-153">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="2adf4-155">Si vous ne voyez pas les **modules** et que votre abonnement a été acheté par l’intermédiaire d’un partenaire, sélectionnez Centre de gestion des licences en **volume (VLSC).**</span><span class="sxs-lookup"><span data-stu-id="2adf4-155">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="2adf4-156">Sélectionnez **Acheter des modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-156">Select **Buy add-ons**.</span></span>

    ![Lien Acheter des modules add-on sur la page Abonnements du Centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="2adf4-158">Dans la page **Acheter des services,** pointez avec la souris ou appuyez sur Stockage de fichiers **supplémentaire Office 365,** puis **sélectionnez Acheter maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-158">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="2adf4-159">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="2adf4-159">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="2adf4-160">Sélectionnez **Check out maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-160">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="2adf4-161">Dans la page À quoi cela ressemble-t-il **?** Vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, examinez les informations de tarification, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-161">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="2adf4-162">Dans la page **Commande complète,** sélectionnez **Commande par ordre.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-162">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2adf4-163">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="2adf4-163">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="2adf4-164">Dans la page **Abonnements,** choisissez l’abonnement auquel vous souhaitez ajouter de l’espace de stockage, puis sélectionnez **Modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-164">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="2adf4-166">Si vous ne voyez pas les **modules** et que votre abonnement a été acheté par l’intermédiaire d’un partenaire, sélectionnez Centre de gestion des licences en **volume (VLSC).**</span><span class="sxs-lookup"><span data-stu-id="2adf4-166">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="2adf4-167">Sélectionnez **Acheter des modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-167">Select **Buy add-ons**.</span></span>

    ![Lien Acheter des modules add-on sur la page Abonnements du Centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="2adf4-169">Dans la page **Acheter des services,** pointez avec la souris ou appuyez sur Stockage de fichiers **supplémentaire Office 365,** puis **sélectionnez Acheter maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-169">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="2adf4-170">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="2adf4-170">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="2adf4-171">Sélectionnez **Check out maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-171">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="2adf4-172">Dans la page À quoi cela ressemble-t-il **?** Vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, examinez les informations de tarification, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-172">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="2adf4-173">Dans la page **Commande complète,** sélectionnez **Commande par ordre.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-173">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

## <a name="increase-or-decrease-storage"></a><span data-ttu-id="2adf4-174">Augmenter ou diminuer l’espace de stockage</span><span class="sxs-lookup"><span data-stu-id="2adf4-174">Increase or decrease storage</span></span>

<span data-ttu-id="2adf4-175">Si vous avez déjà acheté du stockage de fichiers supplémentaire via le module supplémentaire stockage de fichiers **Office 365,** vous pouvez suivre ces étapes pour augmenter ou réduire l’espace de stockage supplémentaire pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-175">If you have already purchased extra file storage via the **Office 365 Extra File Storage** add-on, you can use these steps to increase or decrease the extra storage space for your subscription.</span></span> <span data-ttu-id="2adf4-176">Vous pouvez réduire le stockage jusqu’à 1 gigaoctet.</span><span class="sxs-lookup"><span data-stu-id="2adf4-176">You can reduce the storage to as low as 1 gigabyte.</span></span> <span data-ttu-id="2adf4-177">Pour supprimer tout l’espace de stockage supplémentaire, [contactez le support technique.](../admin/contact-support-for-business-products.md)</span><span class="sxs-lookup"><span data-stu-id="2adf4-177">To remove all of the extra storage space, [contact support](../admin/contact-support-for-business-products.md).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2adf4-178">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="2adf4-178">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="2adf4-179">Sous **l’onglet** Produits, sélectionnez l’abonnement qui contient le module supplémentaire de stockage de fichiers **Office 365.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-179">On the **Products** tab, select the subscription that contains the **Office 365 Extra File Storage** add-on.</span></span>
3. <span data-ttu-id="2adf4-180">Dans la page détails du produit, dans la section **Modules,** sélectionnez **Gérer les modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-180">On the product details page, in the **Add-ons** section, select **Manage add-ons**.</span></span>
4. <span data-ttu-id="2adf4-181">In the **Manage add-ons** pane, from the **Add-on** list, choose **Office 365 Extra File Storage**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-181">In the **Manage add-ons** pane, from the **Add-on** list, choose **Office 365 Extra File Storage**.</span></span>
5. <span data-ttu-id="2adf4-182">Dans la **zone de texte** Quantité, entrez le nombre de GB d’espace de stockage que vous souhaitez pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="2adf4-182">In the **Quantity** text box, enter the number of GBs of storage space that you want for the subscription.</span></span>
6. <span data-ttu-id="2adf4-183">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-183">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2adf4-184">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="2adf4-184">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="2adf4-185">Dans la page **Abonnements,** **sélectionnez Modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-185">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="2adf4-187">Si vous ne voyez pas les **modules** et que votre abonnement a été acheté par l’intermédiaire d’un partenaire, sélectionnez Centre de gestion des licences en **volume (VLSC).**</span><span class="sxs-lookup"><span data-stu-id="2adf4-187">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="2adf4-188">Sous **Stockage de fichiers supplémentaire Office 365,** sélectionnez Modifier la **quantité.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-188">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="2adf4-190">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-190">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="2adf4-191">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="2adf4-191">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="2adf4-192">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-192">Select **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2adf4-193">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="2adf4-193">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="2adf4-194">Dans la page **Abonnements,** **sélectionnez Modules.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-194">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="2adf4-196">Si vous ne voyez pas les **modules** et que votre abonnement a été acheté par l’intermédiaire d’un partenaire, sélectionnez Centre de gestion des licences en **volume (VLSC).**</span><span class="sxs-lookup"><span data-stu-id="2adf4-196">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="2adf4-197">Sous **Stockage de fichiers supplémentaire Office 365,** sélectionnez Modifier la **quantité.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-197">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="2adf4-199">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="2adf4-199">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="2adf4-200">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="2adf4-200">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="2adf4-201">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="2adf4-201">Select **Close**.</span></span>

::: moniker-end

## <a name="is-my-plan-eligible-for-office-365-extra-file-storage"></a><span data-ttu-id="2adf4-202">Mon plan est-il éligible au stockage de fichiers supplémentaire Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="2adf4-202">Is my plan eligible for Office 365 Extra File Storage?</span></span>

<span data-ttu-id="2adf4-203">Le stockage de fichiers supplémentaire Office 365 est accessible aux abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="2adf4-203">Office 365 Extra File Storage is available for the following subscriptions:</span></span>
  
- <span data-ttu-id="2adf4-204">Office 365 Entreprise E1</span><span class="sxs-lookup"><span data-stu-id="2adf4-204">Office 365 Enterprise E1</span></span>

- <span data-ttu-id="2adf4-205">Office 365 Entreprise E2</span><span class="sxs-lookup"><span data-stu-id="2adf4-205">Office 365 Enterprise E2</span></span>

- <span data-ttu-id="2adf4-206">Office 365 Entreprise E3</span><span class="sxs-lookup"><span data-stu-id="2adf4-206">Office 365 Enterprise E3</span></span>

- <span data-ttu-id="2adf4-207">Office 365 Entreprise E4</span><span class="sxs-lookup"><span data-stu-id="2adf4-207">Office 365 Enterprise E4</span></span>

- <span data-ttu-id="2adf4-208">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="2adf4-208">Office 365 Enterprise E5</span></span>

- <span data-ttu-id="2adf4-209">Office pour le web avec SharePoint Plan 1</span><span class="sxs-lookup"><span data-stu-id="2adf4-209">Office for the web with SharePoint Plan 1</span></span>

- <span data-ttu-id="2adf4-210">Office pour le web avec SharePoint Plan 2</span><span class="sxs-lookup"><span data-stu-id="2adf4-210">Office for the web with SharePoint Plan 2</span></span>

- <span data-ttu-id="2adf4-211">SharePoint Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="2adf4-211">SharePoint Online Plan 1</span></span>

- <span data-ttu-id="2adf4-212">SharePoint Online (plan 2)</span><span class="sxs-lookup"><span data-stu-id="2adf4-212">SharePoint Online Plan 2</span></span>

- <span data-ttu-id="2adf4-213">Microsoft 365 Business Basic</span><span class="sxs-lookup"><span data-stu-id="2adf4-213">Microsoft 365 Business Basic</span></span>

- <span data-ttu-id="2adf4-214">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="2adf4-214">Microsoft 365 Business Standard</span></span>

- <span data-ttu-id="2adf4-215">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="2adf4-215">Microsoft 365 Business Premium</span></span>

- <span data-ttu-id="2adf4-216">Microsoft 365 E3</span><span class="sxs-lookup"><span data-stu-id="2adf4-216">Microsoft 365 E3</span></span>

- <span data-ttu-id="2adf4-217">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="2adf4-217">Microsoft 365 E5</span></span>

- <span data-ttu-id="2adf4-218">Microsoft 365 F1</span><span class="sxs-lookup"><span data-stu-id="2adf4-218">Microsoft 365 F1</span></span>

> [!NOTE]
> <span data-ttu-id="2adf4-219">Le stockage de fichiers supplémentaire Office 365 est également disponible pour les plans GCC, GCC High et DOD.</span><span class="sxs-lookup"><span data-stu-id="2adf4-219">Office 365 Extra File Storage is also available for GCC, GCC High, and DOD plans.</span></span>

## <a name="related-content"></a><span data-ttu-id="2adf4-220">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="2adf4-220">Related content</span></span>

<span data-ttu-id="2adf4-221">[Gérer les limites de stockage de](ttps://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits) site (article)</span><span class="sxs-lookup"><span data-stu-id="2adf4-221">[Manage site storage limits](ttps://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits) (article)</span></span>\
<span data-ttu-id="2adf4-222">[Définir l’espace de stockage par défaut pour les utilisateurs de OneDrive](https://docs.microsoft.com/onedrive/set-default-storage-space)(article)</span><span class="sxs-lookup"><span data-stu-id="2adf4-222">[Set the default storage space for OneDrive users](https://docs.microsoft.com/onedrive/set-default-storage-space)(article)</span></span>
