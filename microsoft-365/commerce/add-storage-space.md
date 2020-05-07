---
title: Ajouter de l’espace de stockage pour votre abonnement
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
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
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEU150
- GEA150
- GSP150
ms.assetid: 96ea3533-de64-4b01-839a-c560875a662c
description: Découvrez comment ajouter et réduire le stockage de fichiers dans votre abonnement Microsoft 365. Avec le stockage de fichiers supplémentaire, vous pouvez stocker davantage de contenu dans SharePoint Online et OneDrive.
ms.openlocfilehash: 921fd4a232d288971150a3379b138613f009f9dc
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140965"
---
# <a name="add-storage-space-for-your-subscription"></a><span data-ttu-id="823c9-104">Ajouter de l’espace de stockage pour votre abonnement</span><span class="sxs-lookup"><span data-stu-id="823c9-104">Add storage space for your subscription</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="823c9-105">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="823c9-105">The admin center is changing.</span></span> <span data-ttu-id="823c9-106">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="823c9-106">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="823c9-107">Si vous commencez à manquer d’espace de stockage pour vos collections de sites SharePoint Online et si votre plan est éligible, vous pouvez en ajouter à votre abonnement. </span><span class="sxs-lookup"><span data-stu-id="823c9-107">If you start to run out of storage for your SharePoint Online site collections, you can add storage to your subscription if your plan is eligible.</span></span> <span data-ttu-id="823c9-108">Si le **stockage de fichiers supplémentaire Office 365** n’apparaît pas dans la liste des modules complémentaires disponibles, cela signifie que votre plan n’est pas éligible.</span><span class="sxs-lookup"><span data-stu-id="823c9-108">If you don't see the **Office 365 Extra File Storage** in the list of available add-ons, it means your plan is not eligible.</span></span> <span data-ttu-id="823c9-109">Pour plus d’informations, consultez la rubrique [mon plan est-il éligible ?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span><span class="sxs-lookup"><span data-stu-id="823c9-109">For more information, see [Is my plan eligible?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span></span>

## <a name="view-available-storage"></a><span data-ttu-id="823c9-110">Afficher le stockage disponible</span><span class="sxs-lookup"><span data-stu-id="823c9-110">View available storage</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="823c9-111">Accédez à la [Page de sites actifs du nouveau Centre d’administration SharePoint](https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true), puis connectez-vous à l’aide d’un compte disposant des [autorisations d’administrateur](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="823c9-111">Go to the [Active sites page of the new SharePoint admin center](https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true), and sign in with an account that has [admin permissions](https://docs.microsoft.com/sharepoint/sharepoint-admin-role) for your organization.</span></span>

2. <span data-ttu-id="823c9-112">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="823c9-112">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span> <span data-ttu-id="823c9-113">(Si votre organisation a configuré l’environnement multi-géo dans Office 365, la barre indique également la quantité de stockage utilisée dans tous les emplacements géographiques.)</span><span class="sxs-lookup"><span data-stu-id="823c9-113">(If your organization has configured Multi-Geo in Office 365, the bar also shows the amount of storage used across all geo locations.)</span></span> 

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="823c9-114">Connectez-vous https://portal.office.de à en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette admin pour ouvrir le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="823c9-114">Sign in to https://portal.office.de as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="823c9-115">(Si vous voyez un message indiquant que vous n’êtes pas autorisé à accéder à la page, vous ne disposez pas des autorisations d’administrateur 365 de Microsoft dans votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="823c9-115">(If you see a message that you don't have permission to access the page, you don't have Microsoft 365 administrator permissions in your organization.)</span></span>

2. <span data-ttu-id="823c9-116">Dans le volet gauche, sous **centres d’administration**, sélectionnez **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="823c9-116">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="823c9-117">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="823c9-117">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="823c9-118">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="823c9-118">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="823c9-119">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="823c9-119">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="823c9-120">Connectez-vous https://login.partner.microsoftonline.cn/ à en tant qu’administrateur global ou SharePoint, puis sélectionnez la vignette admin pour ouvrir le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="823c9-120">Sign in to https://login.partner.microsoftonline.cn/ as a global or SharePoint admin, and then select the Admin tile to open the admin center.</span></span> <span data-ttu-id="823c9-121">(Si vous voyez un message indiquant que vous n’êtes pas autorisé à accéder à la page, vous ne disposez pas des autorisations d’administrateur 365 de Microsoft dans votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="823c9-121">(If you see a message that you don't have permission to access the page, you don't have Microsoft 365 administrator permissions in your organization.)</span></span>

2. <span data-ttu-id="823c9-122">Dans le volet gauche, sous **centres d’administration**, sélectionnez **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="823c9-122">In the left pane, under **Admin centers**, select **SharePoint**.</span></span> <span data-ttu-id="823c9-123">Si la version classique du Centre d’administration SharePoint s’affiche, en haut de la page, sélectionnez **Ouvrir maintenant** pour ouvrir la nouvelle version du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="823c9-123">If the classic SharePoint admin center appears, select **Open it now** at the top of the page to open the new SharePoint admin center.</span></span>

3. <span data-ttu-id="823c9-124">Dans le volet gauche du Centre d’administration SharePoint, cliquez sur **Activer des sites**.</span><span class="sxs-lookup"><span data-stu-id="823c9-124">In the left pane of the new SharePoint admin center, select **Active sites**.</span></span>

4. <span data-ttu-id="823c9-125">Dans le coin supérieur droit de la page, reportez-vous à la quantité de stockage utilisée sur tous les sites, ainsi qu’à l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="823c9-125">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span>  

::: moniker-end

![Barre de stockage sur la page sites actifs](https://docs.microsoft.com/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

> [!NOTE]
> <span data-ttu-id="823c9-127">Le stockage utilisé n’inclut pas les modifications apportées au cours des 24-48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="823c9-127">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

<span data-ttu-id="823c9-128">Une fois que vous avez déterminé la quantité de stockage utilisée, vous pouvez ajouter ou supprimer de l'espace de stockage pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="823c9-128">After you've determined how much storage you're using, you can add or remove storage space for your subscription.</span></span> <span data-ttu-id="823c9-129">Pour savoir quel sera le coût de l’ajout d’espace de stockage, suivez les étapes décrites dans cet article, ainsi que les informations de tarification avant de l’achat.</span><span class="sxs-lookup"><span data-stu-id="823c9-129">To find out how much it will cost to add storage space, follow the steps in this article, and review the pricing information before you purchase.</span></span>
  
<span data-ttu-id="823c9-130">Pour plus d’informations sur la définition des limites de stockage des collections de sites, voir [Manage site collection Storage Limits](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits).</span><span class="sxs-lookup"><span data-stu-id="823c9-130">For information about setting site collection storage limits, see [Manage site collection storage limits](https://docs.microsoft.com/sharepoint/manage-site-collection-storage-limits).</span></span>
  
## <a name="add-storage-to-your-subscription"></a><span data-ttu-id="823c9-131">Ajouter un espace de stockage à votre abonnement</span><span class="sxs-lookup"><span data-stu-id="823c9-131">Add storage to your subscription</span></span>

<span data-ttu-id="823c9-132">Si vous n’avez pas encore acheté de stockage supplémentaire pour votre abonnement, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="823c9-132">If you haven't yet purchased extra storage for your subscription, you can do that.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="823c9-133">Dans le centre d’administration, accédez à la page \*\*facturation \*\* \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Acheter des services</a>.</span><span class="sxs-lookup"><span data-stu-id="823c9-133">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>

2. <span data-ttu-id="823c9-134">Au bas de la page **acheter des services** , sélectionnez **compléments**.</span><span class="sxs-lookup"><span data-stu-id="823c9-134">At the bottom of the **Purchase services** page, select **Add-ons**.</span></span>

3. <span data-ttu-id="823c9-135">Sélectionnez le **stockage de fichiers supplémentaire Office 365**.</span><span class="sxs-lookup"><span data-stu-id="823c9-135">Select **Office 365 Extra File Storage**.</span></span>

4. <span data-ttu-id="823c9-136">Sur la page **stockage de fichiers supplémentaire Office 365** , si vous le voyez, sélectionnez l’abonnement de base, puis entrez le nombre de gigaoctets de stockage que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="823c9-136">On the **Office 365 Extra File Storage** page, if shown, choose the base subscription, then enter the number of gigabytes of storage you want to add.</span></span>

5. <span data-ttu-id="823c9-137">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-137">Select **Check out now**.</span></span>

6. <span data-ttu-id="823c9-138">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-138">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="823c9-139">Sur la page **terminer la commande** , vérifiez le total.</span><span class="sxs-lookup"><span data-stu-id="823c9-139">On the **Complete order** page, verify the total.</span></span> <span data-ttu-id="823c9-140">Si vous devez apporter des modifications, sélectionnez **modifier la commande**.</span><span class="sxs-lookup"><span data-stu-id="823c9-140">If you need to make any changes, select **Edit order**.</span></span> <span data-ttu-id="823c9-141">Si la commande nécessite une vérification de solvabilité, activez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="823c9-141">If the order requires a credit check, select the check box.</span></span> <span data-ttu-id="823c9-142">Lorsque vous avez terminé, sélectionnez **passer la commande** \> **sur Accueil de l’administration**.</span><span class="sxs-lookup"><span data-stu-id="823c9-142">When you're finished, select **Place order** \> **Go to Admin Home**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="823c9-143">Dans le centre d’administration, accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">abonnements</a> de **facturation** \>.  </span><span class="sxs-lookup"><span data-stu-id="823c9-143">In the admin center, go to the **Billing** \>  <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="823c9-144">Sur la page **abonnements** , choisissez l’abonnement auquel vous voulez ajouter de l’espace de stockage, puis sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="823c9-144">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="823c9-146">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="823c9-146">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="823c9-147">Sélectionnez **acheter des modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="823c9-147">Select **Buy add-ons**.</span></span>

    ![Acheter le lien des modules complémentaires sur la page abonnements du centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="823c9-149">Sur la page **acheter des services** , pointez avec la souris ou appuyez sur le stockage de **fichiers supplémentaire Office 365**, puis sélectionnez **acheter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-149">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="823c9-150">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="823c9-150">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="823c9-151">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-151">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="823c9-152">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-152">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="823c9-153">Sur la page **terminer la commande** , sélectionnez passer une **commande**.</span><span class="sxs-lookup"><span data-stu-id="823c9-153">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="823c9-154">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="823c9-154">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="823c9-155">Sur la page **abonnements** , choisissez l’abonnement auquel vous voulez ajouter de l’espace de stockage, puis sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="823c9-155">On the **Subscriptions** page, choose the subscription to which  you want to add storage space, then select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="823c9-157">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="823c9-157">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="823c9-158">Sélectionnez **acheter des modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="823c9-158">Select **Buy add-ons**.</span></span>

    ![Acheter le lien des modules complémentaires sur la page abonnements du centre d’administration.](../media/f5cbc3fa-90f7-4299-976d-2482f2c69755.png)
  
4. <span data-ttu-id="823c9-160">Sur la page **acheter des services** , pointez avec la souris ou appuyez sur le stockage de **fichiers supplémentaire Office 365**, puis sélectionnez **acheter maintenant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-160">On the **Purchase services** page, mouse over or tap **Office 365 Extra File Storage**, then select **Buy now**.</span></span>
  
5. <span data-ttu-id="823c9-161">Entrez le nombre de licences utilisateur dont vous avez besoin et, si vous le souhaitez, choisissez un abonnement de base.</span><span class="sxs-lookup"><span data-stu-id="823c9-161">Enter the number of user licenses that you need and, if shown, choose a base subscription.</span></span> <span data-ttu-id="823c9-162">Sélectionnez **Extraire maintenant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-162">Select **Check out now**.</span></span>
  
6. <span data-ttu-id="823c9-163">Sur la page **Comment effectue cette présentation ?** , vérifiez le nombre de gigaoctets de stockage que vous avez sélectionné, vérifiez les informations de tarification, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="823c9-163">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>

7. <span data-ttu-id="823c9-164">Sur la page **terminer la commande** , sélectionnez passer une **commande**.</span><span class="sxs-lookup"><span data-stu-id="823c9-164">On the **Complete order** page, select **Place order**.</span></span>

::: moniker-end

## <a name="increase-or-decrease-storage"></a><span data-ttu-id="823c9-165">Augmenter ou diminuer l’espace de stockage</span><span class="sxs-lookup"><span data-stu-id="823c9-165">Increase or decrease storage</span></span>

<span data-ttu-id="823c9-166">Si vous avez déjà acheté le stockage de fichiers supplémentaire via le complément de **stockage de fichiers supplémentaire Office 365** , vous pouvez suivre ces étapes pour augmenter ou réduire l’espace de stockage supplémentaire pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="823c9-166">If you have already purchased extra file storage via the **Office 365 Extra File Storage** add-on, you can use these steps to increase or decrease the extra storage space for your subscription.</span></span> <span data-ttu-id="823c9-167">Vous pouvez réduire l’espace de stockage à 1 gigaoctet.</span><span class="sxs-lookup"><span data-stu-id="823c9-167">You can reduce the storage to as low as 1 gigabyte.</span></span> <span data-ttu-id="823c9-168">Pour supprimer tout l’espace de stockage supplémentaire, vous devez [contacter le support technique](../admin/contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="823c9-168">To remove all of the extra storage space, you need to [contact support](../admin/contact-support-for-business-products.md).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="823c9-169">Dans le centre d’administration, accédez à la page **facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">de vos produits</a> .</span><span class="sxs-lookup"><span data-stu-id="823c9-169">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>

2. <span data-ttu-id="823c9-170">Choisissez l’abonnement qui contient le complément de **stockage de fichiers supplémentaire Office 365** .</span><span class="sxs-lookup"><span data-stu-id="823c9-170">Choose the subscription that contains the **Office 365 Extra File Storage** add-on.</span></span>

3. <span data-ttu-id="823c9-171">Sélectionnez **composants additionnels**, puis **modifier la quantité**.</span><span class="sxs-lookup"><span data-stu-id="823c9-171">Select **Add-ons**, then choose **Change quantity**.</span></span>

4. <span data-ttu-id="823c9-172">Dans le volet **Ajouter/supprimer des giga-octets** , entrez le total de gigaoctets souhaité pour l’abonnement, puis sélectionnez **soumettre la modification**.</span><span class="sxs-lookup"><span data-stu-id="823c9-172">In the **Add/Remove gigabytes** pane, enter the total gigabytes you want for the subscription, then select **Submit change**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="823c9-173">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="823c9-173">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="823c9-174">Sur la page **abonnements** , sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="823c9-174">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="823c9-176">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="823c9-176">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="823c9-177">Sous **stockage de fichiers supplémentaire Office 365**, sélectionnez **modifier la quantité**.</span><span class="sxs-lookup"><span data-stu-id="823c9-177">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="823c9-179">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="823c9-179">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="823c9-180">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="823c9-180">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="823c9-181">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="823c9-181">Select **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="823c9-182">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="823c9-182">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span>

2. <span data-ttu-id="823c9-183">Sur la page **abonnements** , sélectionnez **composants additionnels**.</span><span class="sxs-lookup"><span data-stu-id="823c9-183">On the **Subscriptions** page, select **Add-ons**.</span></span>

    ![Add-ons button used to purchase add-ons.](../media/b4d2beb4-4f6d-435a-b127-01ceebd6eebf.png)
  
    > [!NOTE]
    > <span data-ttu-id="823c9-185">Si vous ne voyez pas les **modules**complémentaires et que votre abonnement a été acheté auprès d’un partenaire, sélectionnez Centre de gestion des **licences en volume (VLSC)**.</span><span class="sxs-lookup"><span data-stu-id="823c9-185">If you don't see **Add-ons**, and your subscription was purchased through a partner, select **Volume Licensing Service Center (VLSC)**.</span></span>
  
3. <span data-ttu-id="823c9-186">Sous **stockage de fichiers supplémentaire Office 365**, sélectionnez **modifier la quantité**.</span><span class="sxs-lookup"><span data-stu-id="823c9-186">Under **Office 365 Extra File Storage**, select **Change quantity**.</span></span>

    ![Lien Modifier la quantité.](../media/96473f2b-6ff6-45ec-b1a3-d7b204ac1f6e.png)
  
4. <span data-ttu-id="823c9-188">Dans le volet droit, entrez le nombre total de gigaoctets dont vous avez besoin, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="823c9-188">In the right pane, enter the total number of gigabytes that you need, then select **Submit**.</span></span>

    <span data-ttu-id="823c9-189">Par exemple, si vous disposez actuellement de 200 Go d'espace de stockage supplémentaire, mais que vous n'avez besoin que de 100 Go, entrez **100** dans la zone.</span><span class="sxs-lookup"><span data-stu-id="823c9-189">For example, if you currently have 200 gigabytes of extra file storage but you only need 100 gigabytes, then you would enter **100** in the box.</span></span>

5. <span data-ttu-id="823c9-190">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="823c9-190">Select **Close**.</span></span>

::: moniker-end

## <a name="is-my-plan-eligible-for-office-365-extra-file-storage"></a><span data-ttu-id="823c9-191">Mon plan est-il éligible au stockage de fichiers supplémentaire Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="823c9-191">Is my plan eligible for Office 365 Extra File Storage?</span></span>

<span data-ttu-id="823c9-192">Le stockage de fichiers supplémentaire Office 365 est accessible aux abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="823c9-192">Office 365 Extra File Storage is available for the following subscriptions:</span></span>
  
- <span data-ttu-id="823c9-193">Office 365 Entreprise E1</span><span class="sxs-lookup"><span data-stu-id="823c9-193">Office 365 Enterprise E1</span></span>

- <span data-ttu-id="823c9-194">Office 365 Entreprise E2</span><span class="sxs-lookup"><span data-stu-id="823c9-194">Office 365 Enterprise E2</span></span>

- <span data-ttu-id="823c9-195">Office 365 Entreprise E3</span><span class="sxs-lookup"><span data-stu-id="823c9-195">Office 365 Enterprise E3</span></span>

- <span data-ttu-id="823c9-196">Office 365 Entreprise E4</span><span class="sxs-lookup"><span data-stu-id="823c9-196">Office 365 Enterprise E4</span></span>

- <span data-ttu-id="823c9-197">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="823c9-197">Office 365 Enterprise E5</span></span>

- <span data-ttu-id="823c9-198">Office pour le Web avec SharePoint plan 1</span><span class="sxs-lookup"><span data-stu-id="823c9-198">Office for the web with SharePoint Plan 1</span></span>

- <span data-ttu-id="823c9-199">Office pour le Web avec SharePoint plan 2</span><span class="sxs-lookup"><span data-stu-id="823c9-199">Office for the web with SharePoint Plan 2</span></span>

- <span data-ttu-id="823c9-200">SharePoint Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="823c9-200">SharePoint Online Plan 1</span></span>

- <span data-ttu-id="823c9-201">SharePoint Online (plan 2)</span><span class="sxs-lookup"><span data-stu-id="823c9-201">SharePoint Online Plan 2</span></span>

- <span data-ttu-id="823c9-202">Microsoft 365 Business Basic</span><span class="sxs-lookup"><span data-stu-id="823c9-202">Microsoft 365 Business Basic</span></span>

- <span data-ttu-id="823c9-203">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="823c9-203">Microsoft 365 Business Standard</span></span>

- <span data-ttu-id="823c9-204">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="823c9-204">Microsoft 365 Business Premium</span></span>

- <span data-ttu-id="823c9-205">Microsoft 365 E3</span><span class="sxs-lookup"><span data-stu-id="823c9-205">Microsoft 365 E3</span></span>

- <span data-ttu-id="823c9-206">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="823c9-206">Microsoft 365 E5</span></span>

- <span data-ttu-id="823c9-207">Microsoft 365 F1</span><span class="sxs-lookup"><span data-stu-id="823c9-207">Microsoft 365 F1</span></span>

> [!NOTE]
> <span data-ttu-id="823c9-208">Le stockage de fichiers supplémentaire Office 365 est également disponible pour les plans GCC, GCC High et DOD.</span><span class="sxs-lookup"><span data-stu-id="823c9-208">Office 365 Extra File Storage is also available for GCC, GCC High, and DOD plans.</span></span>
