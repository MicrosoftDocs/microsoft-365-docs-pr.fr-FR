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
description: Découvrez comment ajouter et réduire le stockage de fichiers dans votre abonnement Microsoft 365. Avec le stockage de fichiers supplémentaire, vous pouvez stocker davantage de contenu dans SharePoint Online et OneDrive.
ms.date: ''
ms.openlocfilehash: 7f9973054bfe97beae36e28b73a3eb2025a13e73
ms.sourcegitcommit: 25afc0c34edc7f8a5eb389d8c701175256c58ec8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "47324467"
---
# <a name="add-storage-space-for-your-subscription"></a><span data-ttu-id="59328-104">Ajouter de l’espace de stockage pour votre abonnement</span><span class="sxs-lookup"><span data-stu-id="59328-104">Add storage space for your subscription</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="59328-105">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="59328-105">The admin center is changing.</span></span> <span data-ttu-id="59328-106">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="59328-106">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="59328-107">Si vous commencez à manquer d’espace de stockage pour vos collections de sites SharePoint Online et si votre plan est éligible, vous pouvez en ajouter à votre abonnement. </span><span class="sxs-lookup"><span data-stu-id="59328-107">If you start to run out of storage for your SharePoint Online site collections, you can add storage to your subscription if your plan is eligible.</span></span> <span data-ttu-id="59328-108">Si le **stockage de fichiers supplémentaire Office 365** n’apparaît pas dans la liste des modules complémentaires disponibles, cela signifie que votre plan n’est pas éligible.</span><span class="sxs-lookup"><span data-stu-id="59328-108">If you don't see the **Office 365 Extra File Storage** in the list of available add-ons, it means your plan is not eligible.</span></span> <span data-ttu-id="59328-109">Pour plus d’informations, consultez la rubrique [mon plan est-il éligible ?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span><span class="sxs-lookup"><span data-stu-id="59328-109">For more information, see [Is my plan eligible?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span></span>

> [!NOTE]
> <span data-ttu-id="59328-110">Si vous avez acheté votre abonnement via le gestionnaire de licences en volume ou un fournisseur de services cryptographiques, vous ne pouvez pas acheter **Office 365 supplémentaire de stockage de fichiers** pour votre organisation directement auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59328-110">If you bought your subscription through Volume Licensing or a CSP, you can't buy **Office 365 Extra File Storage** for your organization directly from Microsoft.</span></span> <span data-ttu-id="59328-111">Contactez votre représentant ou votre partenaire pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="59328-111">Contact your representative or partner for help.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="59328-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="59328-112">Before you begin</span></span>

<span data-ttu-id="59328-113">Vous devez être un administrateur global ou SharePoint pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="59328-113">You must be a Global or SharePoint admin to do the tasks in this article.</span></span> <span data-ttu-id="59328-114">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="59328-114">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>

## <a name="view-available-storage"></a><span data-ttu-id="59328-115">Afficher le stockage disponible</span><span class="sxs-lookup"><span data-stu-id="59328-115">View available storage</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="59328-116">Dans le centre d’administration SharePoint, accédez à la page <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">sites actifs</a> , puis connectez-vous à l’aide d’un compte disposant d' [autorisations d’administrateur](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="59328-116">In the SharePoint admin center, go to the <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">Active sites</a> page, and sign in with an account that has [admin permissions](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) for your organization.</span></span>

2. <span data-ttu-id="59328-117">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-117">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span> <span data-ttu-id="59328-118">Si votre organisation a configuré l’environnement multi-géo dans Office 365, la barre indique également la quantité de stockage utilisée dans tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="59328-118">If your organization has configured Multi-Geo in Office 365, the bar also shows the amount of storage used across all geo locations.</span></span>

   ![Barre de stockage sur la page sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="59328-120">Le stockage utilisé n’inclut pas les modifications apportées au cours des 24-48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="59328-120">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="59328-121">Connectez-vous à https://portal.office.de en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette admin pour ouvrir le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="59328-121">Sign in to https://portal.office.de as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="59328-122">Si vous voyez un message indiquant que vous n’êtes pas autorisé à accéder à la page, cela signifie que vous ne disposez pas des autorisations d’administrateur 365 de Microsoft dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="59328-122">If you see a message that you don't have permission to access the page, it means that you don't have Microsoft 365 administrator permissions in your organization.</span></span>

2. <span data-ttu-id="59328-123">Dans le volet gauche, sous **centres d’administration**, sélectionnez **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="59328-123">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="59328-124">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="59328-124">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="59328-125">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="59328-125">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="59328-126">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-126">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>

   ![Barre de stockage sur la page sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="59328-128">Le stockage utilisé n’inclut pas les modifications apportées au cours des 24-48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="59328-128">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="59328-129">Connectez-vous à https://login.partner.microsoftonline.cn/ en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette admin pour ouvrir le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="59328-129">Sign in to https://login.partner.microsoftonline.cn/ as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="59328-130">(Si vous voyez un message indiquant que vous n’avez pas l’autorisation d’accéder à la page, cela signifie que vous ne disposez pas des autorisations d’administrateur 365 de Microsoft dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="59328-130">(If you see a message that you don't have permission to access the page, it means that you don't have Microsoft 365 administrator permissions in your organization.</span></span>

2. <span data-ttu-id="59328-131">Dans le volet gauche, sous **centres d’administration**, sélectionnez **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="59328-131">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="59328-132">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="59328-132">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="59328-133">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="59328-133">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="59328-134">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-134">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>  

   ![Barre de stockage sur la page sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="59328-136">Le stockage utilisé n’inclut pas les modifications apportées au cours des 24-48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="59328-136">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

::: moniker-end

<span data-ttu-id="59328-137">Une fois que vous avez déterminé la quantité de stockage utilisée, vous pouvez ajouter ou supprimer de l'espace de stockage pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-137">After you've determined how much storage you're using, you can add or remove storage space for your subscription.</span></span> <span data-ttu-id="59328-138">Pour savoir quel sera le coût de l’ajout d’espace de stockage, suivez les étapes décrites dans cet article, ainsi que les informations de tarification avant de l’achat.</span><span class="sxs-lookup"><span data-stu-id="59328-138">To find out how much it will cost to add storage space, follow the steps in this article, and review the pricing information before you purchase.</span></span>
  
<span data-ttu-id="59328-139">Pour plus d’informations sur la définition des limites de stockage des collections de sites, voir [Manage site collection Storage Limits](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits).</span><span class="sxs-lookup"><span data-stu-id="59328-139">For information about setting site collection storage limits, see [Manage site collection storage limits](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits).</span></span>
  
## <a name="add-storage-to-your-subscription"></a><span data-ttu-id="59328-140">Ajouter un espace de stockage à votre abonnement</span><span class="sxs-lookup"><span data-stu-id="59328-140">Add storage to your subscription</span></span>

<span data-ttu-id="59328-141">Si vous n’avez pas encore acheté de stockage supplémentaire pour votre abonnement, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="59328-141">If you haven't yet purchased extra storage for your subscription, you can do that.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="59328-142">Dans le centre d’administration, accédez à la page \*\*facturation \*\* \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Acheter des services</a>.</span><span class="sxs-lookup"><span data-stu-id="59328-142">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>
2. <span data-ttu-id="59328-143">Au bas de la page **acheter des services** , sélectionnez **compléments**.</span><span class="sxs-lookup"><span data-stu-id="59328-143">At the bottom of the **Purchase services** page, select **Add-ons**.</span></span>
3. <span data-ttu-id="59328-144">Sélectionnez le **stockage de fichiers supplémentaire Office 365**.</span><span class="sxs-lookup"><span data-stu-id="59328-144">Select **Office 365 Extra File Storage**.</span></span>
4. <span data-ttu-id="59328-145">Sur la page **stockage de fichiers supplémentaire Office 365** , si vous le voyez, sélectionnez l’abonnement de base, puis entrez le nombre de gigaoctets de stockage que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="59328-145">On the **Office 365 Extra File Storage** page, if shown, choose the base subscription, then enter the number of gigabytes of storage you want to add.</span></span>
5. <span data-ttu-id="59328-146">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="59328-146">Select **Check out now**.</span></span>
6. <span data-ttu-id="59328-147">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="59328-147">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>
7. <span data-ttu-id="59328-148">Sur la page **terminer la commande** , vérifiez le total.</span><span class="sxs-lookup"><span data-stu-id="59328-148">On the **Complete order** page, verify the total.</span></span> <span data-ttu-id="59328-149">Si vous devez apporter des modifications, sélectionnez **modifier la commande**.</span><span class="sxs-lookup"><span data-stu-id="59328-149">If you need to make any changes, select **Edit order**.</span></span> <span data-ttu-id="59328-150">Si la commande nécessite une vérification de solvabilité, activez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="59328-150">If the order requires a credit check, select the check box.</span></span> <span data-ttu-id="59328-151">Lorsque vous avez terminé, sélectionnez **passer la commande** \> **sur Accueil de l’administration**.</span><span class="sxs-lookup"><span data-stu-id="59328-151">When you're finished, select **Place order** \> **Go to Admin Home**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="59328-152">Dans le centre d’administration, accédez à **Billing** la \> page <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">abonnements</a> de facturation.  </span><span class="sxs-lookup"><span data-stu-id="59328-152">In the admin center, go to the **Billing** \>  <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="59328-153">Sur la page **abonnements** , choisissez l’abonnement auquel vous voulez ajouter de l’espace de stockage, puis sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="59328-153">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="59328-155">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="59328-155">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="59328-156">Sélectionnez **acheter des modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="59328-156">Select **Buy add-ons**.</span></span>

    ![Acheter le lien des modules complémentaires sur la page abonnements du centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="59328-158">Sur la page **acheter des services** , pointez avec la souris ou appuyez sur le stockage de **fichiers supplémentaire Office 365**, puis sélectionnez **acheter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="59328-158">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="59328-159">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="59328-159">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="59328-160">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="59328-160">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="59328-161">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="59328-161">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="59328-162">Sur la page **terminer la commande** , sélectionnez passer une **commande**.</span><span class="sxs-lookup"><span data-stu-id="59328-162">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="59328-163">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="59328-163">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="59328-164">Sur la page **abonnements** , choisissez l’abonnement auquel vous voulez ajouter de l’espace de stockage, puis sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="59328-164">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="59328-166">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="59328-166">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="59328-167">Sélectionnez **acheter des modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="59328-167">Select **Buy add-ons**.</span></span>

    ![Acheter le lien des modules complémentaires sur la page abonnements du centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="59328-169">Sur la page **acheter des services** , pointez avec la souris ou appuyez sur le stockage de **fichiers supplémentaire Office 365**, puis sélectionnez **acheter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="59328-169">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="59328-170">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="59328-170">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="59328-171">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="59328-171">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="59328-172">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="59328-172">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="59328-173">Sur la page **terminer la commande** , sélectionnez passer une **commande**.</span><span class="sxs-lookup"><span data-stu-id="59328-173">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

## <a name="increase-or-decrease-storage"></a><span data-ttu-id="59328-174">Augmenter ou diminuer l’espace de stockage</span><span class="sxs-lookup"><span data-stu-id="59328-174">Increase or decrease storage</span></span>

<span data-ttu-id="59328-175">Si vous avez déjà acheté le stockage de fichiers supplémentaire via le complément de **stockage de fichiers supplémentaire Office 365** , vous pouvez suivre ces étapes pour augmenter ou réduire l’espace de stockage supplémentaire pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-175">If you have already purchased extra file storage via the **Office 365 Extra File Storage** add-on, you can use these steps to increase or decrease the extra storage space for your subscription.</span></span> <span data-ttu-id="59328-176">Vous pouvez réduire l’espace de stockage à 1 gigaoctet.</span><span class="sxs-lookup"><span data-stu-id="59328-176">You can reduce the storage to as low as 1 gigabyte.</span></span> <span data-ttu-id="59328-177">Pour supprimer tout l’espace de stockage supplémentaire, [Contactez le support technique](../admin/contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="59328-177">To remove all of the extra storage space, [contact support](../admin/contact-support-for-business-products.md).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="59328-178">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="59328-178">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="59328-179">Dans l’onglet **produits** , sélectionnez l’abonnement qui contient le complément de **stockage de fichiers supplémentaire Office 365** .</span><span class="sxs-lookup"><span data-stu-id="59328-179">On the **Products** tab, select the subscription that contains the **Office 365 Extra File Storage** add-on.</span></span>
3. <span data-ttu-id="59328-180">Sur la page Détails du produit, dans la section **modules** complémentaires, sélectionnez **gérer les modules**complémentaires.</span><span class="sxs-lookup"><span data-stu-id="59328-180">On the product details page, in the **Add-ons** section, select **Manage add-ons**.</span></span>
4. <span data-ttu-id="59328-181">Dans le volet **gérer les modules** complémentaires, dans la liste **module complémentaire** , choisissez **stockage de fichiers supplémentaire Office 365**.</span><span class="sxs-lookup"><span data-stu-id="59328-181">In the **Manage add-ons** pane, from the **Add-on** list, choose **Office 365 Extra File Storage**.</span></span>
5. <span data-ttu-id="59328-182">Dans la zone de texte **quantité** , entrez le nombre de Go d’espace de stockage que vous souhaitez pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="59328-182">In the **Quantity** text box, enter the number of GBs of storage space that you want for the subscription.</span></span>
6. <span data-ttu-id="59328-183">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="59328-183">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="59328-184">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="59328-184">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="59328-185">Sur la page **abonnements** , sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="59328-185">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="59328-187">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="59328-187">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="59328-188">Sous **stockage de fichiers supplémentaire Office 365**, sélectionnez **modifier la quantité**.</span><span class="sxs-lookup"><span data-stu-id="59328-188">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="59328-190">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="59328-190">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="59328-191">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="59328-191">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="59328-192">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="59328-192">Select **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="59328-193">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="59328-193">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="59328-194">Sur la page **abonnements** , sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="59328-194">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="59328-196">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="59328-196">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="59328-197">Sous **stockage de fichiers supplémentaire Office 365**, sélectionnez **modifier la quantité**.</span><span class="sxs-lookup"><span data-stu-id="59328-197">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="59328-199">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="59328-199">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="59328-200">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="59328-200">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="59328-201">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="59328-201">Select **Close**.</span></span>

::: moniker-end

## <a name="is-my-plan-eligible-for-office-365-extra-file-storage"></a><span data-ttu-id="59328-202">Mon plan est-il éligible au stockage de fichiers supplémentaire Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="59328-202">Is my plan eligible for Office 365 Extra File Storage?</span></span>

<span data-ttu-id="59328-203">Le stockage de fichiers supplémentaire Office 365 est accessible aux abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="59328-203">Office 365 Extra File Storage is available for the following subscriptions:</span></span>
  
- <span data-ttu-id="59328-204">Office 365 Entreprise E1</span><span class="sxs-lookup"><span data-stu-id="59328-204">Office 365 Enterprise E1</span></span>

- <span data-ttu-id="59328-205">Office 365 Entreprise E2</span><span class="sxs-lookup"><span data-stu-id="59328-205">Office 365 Enterprise E2</span></span>

- <span data-ttu-id="59328-206">Office 365 Entreprise E3</span><span class="sxs-lookup"><span data-stu-id="59328-206">Office 365 Enterprise E3</span></span>

- <span data-ttu-id="59328-207">Office 365 Entreprise E4</span><span class="sxs-lookup"><span data-stu-id="59328-207">Office 365 Enterprise E4</span></span>

- <span data-ttu-id="59328-208">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="59328-208">Office 365 Enterprise E5</span></span>

- <span data-ttu-id="59328-209">Office pour le Web avec SharePoint plan 1</span><span class="sxs-lookup"><span data-stu-id="59328-209">Office for the web with SharePoint Plan 1</span></span>

- <span data-ttu-id="59328-210">Office pour le Web avec SharePoint plan 2</span><span class="sxs-lookup"><span data-stu-id="59328-210">Office for the web with SharePoint Plan 2</span></span>

- <span data-ttu-id="59328-211">SharePoint Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="59328-211">SharePoint Online Plan 1</span></span>

- <span data-ttu-id="59328-212">SharePoint Online (plan 2)</span><span class="sxs-lookup"><span data-stu-id="59328-212">SharePoint Online Plan 2</span></span>

- <span data-ttu-id="59328-213">Microsoft 365 Business Basic</span><span class="sxs-lookup"><span data-stu-id="59328-213">Microsoft 365 Business Basic</span></span>

- <span data-ttu-id="59328-214">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="59328-214">Microsoft 365 Business Standard</span></span>

- <span data-ttu-id="59328-215">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="59328-215">Microsoft 365 Business Premium</span></span>

- <span data-ttu-id="59328-216">Microsoft 365 E3</span><span class="sxs-lookup"><span data-stu-id="59328-216">Microsoft 365 E3</span></span>

- <span data-ttu-id="59328-217">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="59328-217">Microsoft 365 E5</span></span>

- <span data-ttu-id="59328-218">Microsoft 365 F1</span><span class="sxs-lookup"><span data-stu-id="59328-218">Microsoft 365 F1</span></span>

> [!NOTE]
> <span data-ttu-id="59328-219">Le stockage de fichiers supplémentaire Office 365 est également disponible pour les plans GCC, GCC High et DOD.</span><span class="sxs-lookup"><span data-stu-id="59328-219">Office 365 Extra File Storage is also available for GCC, GCC High, and DOD plans.</span></span>

## <a name="related-content"></a><span data-ttu-id="59328-220">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="59328-220">Related content</span></span>

<span data-ttu-id="59328-221">[Gérer les limites de stockage du site](ttps://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits) (article) </span><span class="sxs-lookup"><span data-stu-id="59328-221">[Manage site storage limits](ttps://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits) (article)</span></span>\
<span data-ttu-id="59328-222">[Définir l’espace de stockage par défaut pour les utilisateurs de OneDrive](https://docs.microsoft.com/onedrive/set-default-storage-space)(article)</span><span class="sxs-lookup"><span data-stu-id="59328-222">[Set the default storage space for OneDrive users](https://docs.microsoft.com/onedrive/set-default-storage-space)(article)</span></span>
