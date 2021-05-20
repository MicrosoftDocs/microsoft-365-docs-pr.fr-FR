---
title: Ajouter de l’espace de stockage pour votre abonnement
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: drjones, jmueller
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- SPO_Content
ms.custom:
- MAX_CampaignID
- okr_SMB
- AdminSurgePortfolio
- commerce_purchase
search.appverid: MET150
description: Ajoutez du stockage de fichiers dans votre Microsoft 365 abonnement. Avec un stockage de fichiers supplémentaire, vous pouvez stocker plus de contenu dans SharePoint en ligne et OneDrive.
ms.date: 04/02/2021
ms.openlocfilehash: b573205c7053aba0339d1f32deb2996ef80f8754
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572320"
---
# <a name="add-storage-space-for-your-subscription"></a><span data-ttu-id="9c42a-104">Ajouter de l’espace de stockage pour votre abonnement</span><span class="sxs-lookup"><span data-stu-id="9c42a-104">Add storage space for your subscription</span></span>

<span data-ttu-id="9c42a-105">Si vous commencez à manquer d’espace de stockage pour vos collections de sites SharePoint Online et si votre plan est éligible, vous pouvez en ajouter à votre abonnement. </span><span class="sxs-lookup"><span data-stu-id="9c42a-105">If you start to run out of storage for your SharePoint Online site collections, you can add storage to your subscription if your plan is eligible.</span></span> <span data-ttu-id="9c42a-106">Si vous ne voyez pas les Stockage de fichiers supplémentaire Office 365 **dans** la liste des modules ajoutés disponibles, cela signifie que votre régime n’est pas admissible.</span><span class="sxs-lookup"><span data-stu-id="9c42a-106">If you don't see the **Office 365 Extra File Storage** in the list of available add-ons, it means your plan is not eligible.</span></span> <span data-ttu-id="9c42a-107">Pour de plus amples renseignements, [consultez Le régime est-il admissible?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span><span class="sxs-lookup"><span data-stu-id="9c42a-107">For more information, see [Is my plan eligible?](#is-my-plan-eligible-for-office-365-extra-file-storage)</span></span>

> [!NOTE]
> <span data-ttu-id="9c42a-108">Si vous avez acheté votre abonnement via volume licensing ou un CSP, vous ne pouvez pas **acheter Stockage de fichiers supplémentaire Office 365 pour** votre organisation directement auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9c42a-108">If you bought your subscription through Volume Licensing or a CSP, you can't buy **Office 365 Extra File Storage** for your organization directly from Microsoft.</span></span> <span data-ttu-id="9c42a-109">Communiquez avec votre représentant ou partenaire pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="9c42a-109">Contact your representative or partner for help.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="9c42a-110">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9c42a-110">Before you begin</span></span>

<span data-ttu-id="9c42a-111">Vous devez être un administrateur global SharePoint pour effectuer les tâches dans cet article.</span><span class="sxs-lookup"><span data-stu-id="9c42a-111">You must be a Global or SharePoint admin to do the tasks in this article.</span></span> <span data-ttu-id="9c42a-112">Pour plus d’informations, consultez la rubrique [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9c42a-112">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>

## <a name="view-available-storage"></a><span data-ttu-id="9c42a-113">Afficher le stockage disponible</span><span class="sxs-lookup"><span data-stu-id="9c42a-113">View available storage</span></span>

1. <span data-ttu-id="9c42a-114">Dans le SharePoint d’administration, rendez-vous sur la page <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">sites actifs</a> et connectez-vous à un compte qui dispose [d’autorisations administratives](/sharepoint/sharepoint-admin-role) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9c42a-114">In the SharePoint admin center, go to the <a href="https://admin.microsoft.com/sharepoint?page=siteManagement&modern=true" target="_blank">Active sites</a> page, and sign in with an account that has [admin permissions](/sharepoint/sharepoint-admin-role) for your organization.</span></span>

2. <span data-ttu-id="9c42a-115">Dans le coin supérieur droit de la page, consultez la quantité d’espace de stockage utilisé sur tous les sites, ainsi que l’espace de stockage total de votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c42a-115">In the upper right of the page, see the amount of storage used across all sites, and the total storage for your subscription.</span></span> <span data-ttu-id="9c42a-116">Si votre organisation a configuré Multi-Geo en Office 365, la barre affiche également la quantité de stockage utilisée sur tous les emplacements géographiques.</span><span class="sxs-lookup"><span data-stu-id="9c42a-116">If your organization has configured Multi-Geo in Office 365, the bar also shows the amount of storage used across all geo locations.</span></span>

   ![Barre de stockage sur la page des sites actifs](/sharepoint/sharepointonline/media/active-sites-storage-bar.png)

   > [!NOTE]
   > <span data-ttu-id="9c42a-118">L’espace de stockage utilisé n’inclut pas les modifications apportées au cours des 24 à 48 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="9c42a-118">The storage used doesn't include changes made within the last 24-48 hours.</span></span>

<span data-ttu-id="9c42a-119">Une fois que vous avez déterminé la quantité de stockage que vous utilisez, vous pouvez ajouter ou supprimer de l’espace de stockage pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c42a-119">After you determine how much storage you're using, you can add or remove storage space for your subscription.</span></span> <span data-ttu-id="9c42a-120">Pour savoir combien il en coûtera pour ajouter de l’espace de stockage, suivez les étapes de cet article, et passez en revue les informations de prix avant d’acheter plus.</span><span class="sxs-lookup"><span data-stu-id="9c42a-120">To find out how much it will cost to add storage space, follow the steps in this article, and review the pricing information before you buy more.</span></span>
  
<span data-ttu-id="9c42a-121">Pour plus d’informations sur la fixation des limites de stockage de collecte de site, [consultez Gérer les limites de stockage de collecte de site.](/sharepoint/manage-site-collection-storage-limits)</span><span class="sxs-lookup"><span data-stu-id="9c42a-121">For information about setting site collection storage limits, see [Manage site collection storage limits](/sharepoint/manage-site-collection-storage-limits).</span></span>
  
## <a name="add-storage-to-your-subscription"></a><span data-ttu-id="9c42a-122">Ajouter du stockage à votre abonnement</span><span class="sxs-lookup"><span data-stu-id="9c42a-122">Add storage to your subscription</span></span>

<span data-ttu-id="9c42a-123">Si vous n’avez pas encore acheté de stockage supplémentaire pour votre abonnement, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="9c42a-123">If you haven't yet bought extra storage for your subscription, you can do that.</span></span>

1. <span data-ttu-id="9c42a-124">Dans le centre d’administration, accédez à la page **facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Acheter des services</a>.</span><span class="sxs-lookup"><span data-stu-id="9c42a-124">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>
2. <span data-ttu-id="9c42a-125">En bas de la page **Services d’achat,** dans la section **Add-ons,** **trouvez Stockage de fichiers supplémentaire Office 365** et sélectionnez **Détails**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-125">At the bottom of the **Purchase services** page, in the **Add-ons** section, find **Office 365 Extra File Storage**, and select **Details**.</span></span>
3. <span data-ttu-id="9c42a-126">Sur la page des détails du produit, **sélectionnez Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-126">On the product details page, select **Next**.</span></span>
4. <span data-ttu-id="9c42a-127">Si nécessaire, choisissez l’abonnement de base, puis entrez le nombre de gigaoctets de stockage que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="9c42a-127">If needed, choose the base subscription, then enter the number of gigabytes of storage you want to add.</span></span>
5. <span data-ttu-id="9c42a-128">Sélectionnez **Check out maintenant**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-128">Select **Check out now**.</span></span>
6. <span data-ttu-id="9c42a-129">Sur la page **Comment cela ressemble-t-il ?** page, vérifier le nombre de gigaoctets de stockage que vous avez sélectionné, examiner les informations de prix, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-129">On the **How does this look?** page, verify the number of gigabytes of storage you selected, review the pricing information, and then select **Next**.</span></span>
7. <span data-ttu-id="9c42a-130">Sur la page **de commande** complète, vérifiez le total.</span><span class="sxs-lookup"><span data-stu-id="9c42a-130">On the **Complete order** page, verify the total.</span></span> <span data-ttu-id="9c42a-131">Si vous avez besoin d’apporter des modifications, sélectionnez **Modifier l’ordre**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-131">If you need to make any changes, select **Edit order**.</span></span> <span data-ttu-id="9c42a-132">Si la commande nécessite une vérification de crédit, sélectionnez la case à cochée.</span><span class="sxs-lookup"><span data-stu-id="9c42a-132">If the order requires a credit check, select the check box.</span></span> <span data-ttu-id="9c42a-133">Lorsque vous avez terminé, sélectionnez **Commande de place Aller** à Admin \> **Home**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-133">When you're finished, select **Place order** \> **Go to Admin Home**.</span></span>

## <a name="increase-or-decrease-storage"></a><span data-ttu-id="9c42a-134">Augmenter ou diminuer l’espace de stockage</span><span class="sxs-lookup"><span data-stu-id="9c42a-134">Increase or decrease storage</span></span>

<span data-ttu-id="9c42a-135">Si vous avez déjà acheté du stockage de fichiers supplémentaire via **l’add-on Stockage de fichiers supplémentaire Office 365,** vous pouvez utiliser ces étapes pour augmenter ou diminuer l’espace de stockage supplémentaire pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c42a-135">If you've already bought extra file storage via the **Office 365 Extra File Storage** add-on, you can use these steps to increase or decrease the extra storage space for your subscription.</span></span> <span data-ttu-id="9c42a-136">Vous pouvez réduire le stockage à aussi peu que 1 gigaoctet.</span><span class="sxs-lookup"><span data-stu-id="9c42a-136">You can reduce the storage to as low as 1 gigabyte.</span></span> <span data-ttu-id="9c42a-137">Pour supprimer tout l’espace de stockage supplémentaire, contactez [le support](../business-video/get-help-support.md).</span><span class="sxs-lookup"><span data-stu-id="9c42a-137">To remove all of the extra storage space, [contact support](../business-video/get-help-support.md).</span></span>

1. <span data-ttu-id="9c42a-138">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="9c42a-138">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="9c42a-139">Sur **l’onglet** Produits, sélectionnez l’abonnement qui **contient Stockage de fichiers supplémentaire Office 365** add-on.</span><span class="sxs-lookup"><span data-stu-id="9c42a-139">On the **Products** tab, select the subscription that contains the **Office 365 Extra File Storage** add-on.</span></span>
3. <span data-ttu-id="9c42a-140">Sur la page détails du produit, dans la section **Add-ons,** **sélectionnez Gérer les modules supplémentaires**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-140">On the product details page, in the **Add-ons** section, select **Manage add-ons**.</span></span>
4. <span data-ttu-id="9c42a-141">Dans le **volet Manage add-ons,** de la **liste Add-on,** choisissez **Stockage de fichiers supplémentaire Office 365**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-141">In the **Manage add-ons** pane, from the **Add-on** list, choose **Office 365 Extra File Storage**.</span></span>
5. <span data-ttu-id="9c42a-142">Dans la **boîte de** texte Quantité, entrez le nombre de BB d’espace de stockage que vous souhaitez pour l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c42a-142">In the **Quantity** text box, enter the number of GBs of storage space that you want for the subscription.</span></span>
6. <span data-ttu-id="9c42a-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="9c42a-143">Select **Save**.</span></span>

## <a name="is-my-plan-eligible-for-office-365-extra-file-storage"></a><span data-ttu-id="9c42a-144">Mon plan est-il éligible au stockage de fichiers supplémentaire Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="9c42a-144">Is my plan eligible for Office 365 Extra File Storage?</span></span>

<span data-ttu-id="9c42a-145">Le stockage de fichiers supplémentaire Office 365 est accessible aux abonnements suivants :</span><span class="sxs-lookup"><span data-stu-id="9c42a-145">Office 365 Extra File Storage is available for the following subscriptions:</span></span>
  
- <span data-ttu-id="9c42a-146">Office 365 Entreprise E1</span><span class="sxs-lookup"><span data-stu-id="9c42a-146">Office 365 Enterprise E1</span></span>
- <span data-ttu-id="9c42a-147">Office 365 Entreprise E2</span><span class="sxs-lookup"><span data-stu-id="9c42a-147">Office 365 Enterprise E2</span></span>
- <span data-ttu-id="9c42a-148">Office 365 Entreprise E3</span><span class="sxs-lookup"><span data-stu-id="9c42a-148">Office 365 Enterprise E3</span></span>
- <span data-ttu-id="9c42a-149">Office 365 Entreprise E4</span><span class="sxs-lookup"><span data-stu-id="9c42a-149">Office 365 Enterprise E4</span></span>
- <span data-ttu-id="9c42a-150">Office 365 Entreprise E5</span><span class="sxs-lookup"><span data-stu-id="9c42a-150">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="9c42a-151">Office sur le Web avec SharePoint plan 1</span><span class="sxs-lookup"><span data-stu-id="9c42a-151">Office for the web with SharePoint Plan 1</span></span>
- <span data-ttu-id="9c42a-152">Office sur le Web avec SharePoint plan 2</span><span class="sxs-lookup"><span data-stu-id="9c42a-152">Office for the web with SharePoint Plan 2</span></span>
- <span data-ttu-id="9c42a-153">SharePoint Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="9c42a-153">SharePoint Online Plan 1</span></span>
- <span data-ttu-id="9c42a-154">SharePoint Online (offre 2)</span><span class="sxs-lookup"><span data-stu-id="9c42a-154">SharePoint Online Plan 2</span></span>
- <span data-ttu-id="9c42a-155">Microsoft 365 Business Basic</span><span class="sxs-lookup"><span data-stu-id="9c42a-155">Microsoft 365 Business Basic</span></span>
- <span data-ttu-id="9c42a-156">Microsoft 365 Business Standard</span><span class="sxs-lookup"><span data-stu-id="9c42a-156">Microsoft 365 Business Standard</span></span>
- <span data-ttu-id="9c42a-157">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="9c42a-157">Microsoft 365 Business Premium</span></span>
- <span data-ttu-id="9c42a-158">Microsoft 365 E3</span><span class="sxs-lookup"><span data-stu-id="9c42a-158">Microsoft 365 E3</span></span>
- <span data-ttu-id="9c42a-159">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="9c42a-159">Microsoft 365 E5</span></span>
- <span data-ttu-id="9c42a-160">Microsoft 365 F1</span><span class="sxs-lookup"><span data-stu-id="9c42a-160">Microsoft 365 F1</span></span>

> [!NOTE]
> <span data-ttu-id="9c42a-161">Stockage de fichiers supplémentaire Office 365 est également disponible pour les plans Cloud de la communauté du secteur public, Cloud de la communauté du secteur public High et DOD.</span><span class="sxs-lookup"><span data-stu-id="9c42a-161">Office 365 Extra File Storage is also available for GCC, GCC High, and DOD plans.</span></span>

## <a name="related-content"></a><span data-ttu-id="9c42a-162">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="9c42a-162">Related content</span></span>

<span data-ttu-id="9c42a-163">[Gérer les limites de stockage du site](/sharepoint/manage-site-collection-storage-limits) (article)</span><span class="sxs-lookup"><span data-stu-id="9c42a-163">[Manage site storage limits](/sharepoint/manage-site-collection-storage-limits) (article)</span></span>\
<span data-ttu-id="9c42a-164">[Définir l’espace de stockage par défaut OneDrive utilisateurs](/onedrive/set-default-storage-space)(article)</span><span class="sxs-lookup"><span data-stu-id="9c42a-164">[Set the default storage space for OneDrive users](/onedrive/set-default-storage-space)(article)</span></span>
