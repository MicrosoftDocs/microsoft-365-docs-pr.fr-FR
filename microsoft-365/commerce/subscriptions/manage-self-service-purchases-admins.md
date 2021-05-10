---
title: Gérer les achats en libre-service (administrateurs)
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
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
- okr_smb
- commerce
search.appverid:
- MET150
description: Les administrateurs peuvent apprendre à gérer les achats en libre-service effectués par les utilisateurs de leur organisation.
ms.openlocfilehash: 5378d14affd074bfad356fea4bb2adbd6ca104dd
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52293570"
---
# <a name="manage-self-service-purchases-admin"></a><span data-ttu-id="ae538-103">Gérer les achats libre-service (administrateur)</span><span class="sxs-lookup"><span data-stu-id="ae538-103">Manage self-service purchases (Admin)</span></span>

<span data-ttu-id="ae538-104">En tant qu’administrateur, vous pouvez voir les achats en libre-service effectués par des personnes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae538-104">As an admin, you can see self-service purchases made by people in your organization.</span></span> <span data-ttu-id="ae538-105">Vous pouvez voir le nom du produit, le nom de l’acheteur, les abonnements achetés, la date d’expiration, le prix d’achat et les utilisateurs affectés pour chaque achat en libre-service.</span><span class="sxs-lookup"><span data-stu-id="ae538-105">You see the product name, purchaser name, subscriptions purchased, expiration date, purchase price, and assigned users for each self-service purchase.</span></span> <span data-ttu-id="ae538-106">Si votre organisation l’exige, vous pouvez désactiver l’achat en libre-service par produit via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae538-106">If required by your organization, you can turn off self-service purchasing on a per product basis via PowerShell.</span></span> <span data-ttu-id="ae538-107">Vous avez les mêmes stratégies de gestion des données et d’accès que les produits achetés via un achat en libre-service ou de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="ae538-107">You have the same data management and access policies over products bought through self-service purchase or centrally.</span></span>

<span data-ttu-id="ae538-108">Vous pouvez également contrôler si les utilisateurs de votre organisation peuvent effectuer des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="ae538-108">You can also control whether users in your organization can make self-service purchases.</span></span> <span data-ttu-id="ae538-109">Pour plus d’informations, voir [Utiliser AllowSelfServicePurchase pour le module PowerShell MSCommerce.](allowselfservicepurchase-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="ae538-109">For more information, see [Use AllowSelfServicePurchase for the MSCommerce PowerShell module](allowselfservicepurchase-powershell.md).</span></span>

## <a name="view-self-service-subscriptions"></a><span data-ttu-id="ae538-110">Afficher les abonnements en libre-service</span><span class="sxs-lookup"><span data-stu-id="ae538-110">View self-service subscriptions</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="ae538-111">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-111">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="ae538-112">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-112">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="ae538-113">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-113">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Your products</a> page.</span></span>
::: moniker-end

2. <span data-ttu-id="ae538-114">Sous **l’onglet** Produits, sélectionnez l’icône de filtre, puis sélectionnez **Libre-service.**</span><span class="sxs-lookup"><span data-stu-id="ae538-114">On the **Products** tab, select the filter icon, then select **Self-service**.</span></span>
3. <span data-ttu-id="ae538-115">Pour afficher plus de détails sur un abonnement, choisissez-en un dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ae538-115">To view more details about a subscription, choose one from the list.</span></span>

## <a name="view-who-has-licenses-for-a-self-service-purchase-subscription"></a><span data-ttu-id="ae538-116">Afficher qui dispose de licences pour un abonnement d’achat en libre-service</span><span class="sxs-lookup"><span data-stu-id="ae538-116">View who has licenses for a self-service purchase subscription</span></span>

> [!NOTE]
> <span data-ttu-id="ae538-117">En tant qu’administrateur, vous ne pouvez pas attribuer ou annuler des attributions de licences pour un abonnement d’achat en libre-service acheté par un utilisateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae538-117">As an admin, you can't assign or unassign licenses for a self-service purchase subscription bought by a user in your organization.</span></span> <span data-ttu-id="ae538-118">Vous pouvez [prendre le contrôle d’un abonnement d’achat en libre-service](#take-over-a-self-service-purchase-subscription), puis attribuer ou annuler des attributions de licences.</span><span class="sxs-lookup"><span data-stu-id="ae538-118">You can [take over a self-service purchase subscription](#take-over-a-self-service-purchase-subscription), and then assign or unassign licenses.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="ae538-119">Dans le Centre d’administration, choisissez la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-119">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="ae538-120">Dans le Centre d’administration, choisissez la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=848038" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-120">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=848038" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="ae538-121">Dans le Centre d’administration, choisissez la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850625" target="_blank">Licences</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-121">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850625" target="_blank">Licenses</a> page.</span></span>

::: moniker-end

2. <span data-ttu-id="ae538-122">Sélectionnez l’icône de filtre, puis choisissez **Libre-service.**</span><span class="sxs-lookup"><span data-stu-id="ae538-122">Select the filter icon, then choose **Self-service**.</span></span>
3. <span data-ttu-id="ae538-123">Sélectionnez un produit pour voir les licences attribuées aux personnes.</span><span class="sxs-lookup"><span data-stu-id="ae538-123">Select a product to see licenses assigned to people.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ae538-124">S’il existe plusieurs achats pour un produit, ce  produit n’est répertorié qu’une seule fois et la colonne Quantité disponible indique le total de tous les abonnements achetés pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="ae538-124">If there are multiple purchases for a product, that product is only listed once, and the **Available quantity** column shows the total of all subscriptions bought for that product.</span></span>
4. <span data-ttu-id="ae538-125">La **liste Utilisateurs** est regroupée par les noms des personnes qui ont effectué des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="ae538-125">The **Users** list is grouped by the names of people who made self-service purchases.</span></span>
5. <span data-ttu-id="ae538-126">Pour exporter une liste d’utilisateurs avec des licences pour ces abonnements, choisissez les abonnements que vous souhaitez exporter, puis **sélectionnez Exporter les utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="ae538-126">To export a list of users with licenses for these subscriptions, choose the subscriptions that you want to export, then choose **Export users**.</span></span>

## <a name="disable-or-enable-self-service-purchases"></a><span data-ttu-id="ae538-127">Désactiver ou activer les achats en libre-service</span><span class="sxs-lookup"><span data-stu-id="ae538-127">Disable or enable self-service purchases</span></span>

<span data-ttu-id="ae538-128">Vous pouvez désactiver ou activer les achats en libre-service pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae538-128">You can disable or enable self-service purchases for users in your organization.</span></span> <span data-ttu-id="ae538-129">Le module **PowerShell MSCommerce** inclut une valeur de paramètre **PolicyID** pour **AllowSelfServicePurchase** qui vous permet de contrôler si les utilisateurs de votre organisation peuvent effectuer des achats en libre-service et pour quels produits.</span><span class="sxs-lookup"><span data-stu-id="ae538-129">The **MSCommerce** PowerShell module includes a **PolicyID** parameter value for **AllowSelfServicePurchase** that lets you control whether users in your organization can make self-service purchases, and for which products.</span></span>

<span data-ttu-id="ae538-130">Vous pouvez utiliser le module **PowerShell MSCommerce** pour :</span><span class="sxs-lookup"><span data-stu-id="ae538-130">You can use the **MSCommerce** PowerShell module to:</span></span>

- <span data-ttu-id="ae538-131">Afficher l’état par défaut de la valeur du paramètre **AllowSelfServicePurchase** , qu’elle soit activée ou désactivée par le produit</span><span class="sxs-lookup"><span data-stu-id="ae538-131">View the default state of the **AllowSelfServicePurchase** parameter value—whether it's enabled or disabled by product</span></span>
- <span data-ttu-id="ae538-132">Afficher la liste des produits applicables et si l’achat en libre-service est activé ou désactivé</span><span class="sxs-lookup"><span data-stu-id="ae538-132">View a list of applicable products and whether self-service purchase is enabled or disabled</span></span>
- <span data-ttu-id="ae538-133">Afficher ou modifier le paramètre actuel d’un produit spécifique pour l’activer ou le désactiver</span><span class="sxs-lookup"><span data-stu-id="ae538-133">View or modify the current setting for a specific product to either enable or disable it</span></span>

<span data-ttu-id="ae538-134">Pour plus d’informations, voir [Utiliser AllowSelfServicePurchase pour le module PowerShell MSCommerce.](allowselfservicepurchase-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="ae538-134">For more information, see [Use AllowSelfServicePurchase for the MSCommerce PowerShell module](allowselfservicepurchase-powershell.md).</span></span>

## <a name="centralize-licenses-under-a-single-subscription"></a><span data-ttu-id="ae538-135">Centraliser les licences sous un abonnement unique</span><span class="sxs-lookup"><span data-stu-id="ae538-135">Centralize licenses under a single subscription</span></span>

<span data-ttu-id="ae538-136">Vous pouvez attribuer des licences existantes ou acheter des abonnements supplémentaires via des contrats existants pour les utilisateurs affectés à des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="ae538-136">You can assign existing licenses or purchase additional subscriptions through existing agreements for users assigned to self-service purchases.</span></span> <span data-ttu-id="ae538-137">Après avoir attribué ces licences achetées de manière centralisée, vous pouvez demander aux acheteur d’annuler leurs abonnements existants.</span><span class="sxs-lookup"><span data-stu-id="ae538-137">After you assign these centrally purchased licenses, you can request that purchasers cancel their existing subscriptions.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="ae538-138">Dans le Centre d’administration, allez à la page **Services** > <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">d’achat de facturation.</a></span><span class="sxs-lookup"><span data-stu-id="ae538-138">In the admin center go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="ae538-139">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">d’administration,</a>allez à la page Des services  > **d’achat de facturation.**</span><span class="sxs-lookup"><span data-stu-id="ae538-139">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Purchase services** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="ae538-140">Dans le Centre <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">d’administration,</a>allez à la page Des services  > **d’achat de facturation.**</span><span class="sxs-lookup"><span data-stu-id="ae538-140">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Purchase services** page.</span></span>

::: moniker-end

2. <span data-ttu-id="ae538-141">Recherchez et choisissez le produit que vous souhaitez acheter, puis choisissez **Acheter.**</span><span class="sxs-lookup"><span data-stu-id="ae538-141">Find and choose the product that you want to buy, then choose **Buy**.</span></span>
3. <span data-ttu-id="ae538-142">Pour terminer votre achat, complétez les étapes restantes.</span><span class="sxs-lookup"><span data-stu-id="ae538-142">Complete the remaining steps to complete your purchase.</span></span>
4. <span data-ttu-id="ae538-143">Suivez les étapes de [l’affichage qui](#view-who-has-licenses-for-a-self-service-purchase-subscription) dispose de licences pour un abonnement acheté en libre-service pour exporter une liste d’utilisateurs à référencer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="ae538-143">Follow the steps in [View who has licenses for a self-service purchased subscription](#view-who-has-licenses-for-a-self-service-purchase-subscription) to export a list of users to reference in the next step.</span></span>
5. <span data-ttu-id="ae538-144">Attribuez des licences à toutes les personnes qui disposent d’une licence dans l’autre abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae538-144">Assign licenses to everyone who has a license in the other subscription.</span></span> <span data-ttu-id="ae538-145">Pour obtenir la procédure complète, voir [Attribuer des licences aux utilisateurs.](../../admin/manage/assign-licenses-to-users.md)</span><span class="sxs-lookup"><span data-stu-id="ae538-145">For full steps, see [Assign licenses to users](../../admin/manage/assign-licenses-to-users.md).</span></span>
6. <span data-ttu-id="ae538-146">Contactez la personne qui a acheté l’abonnement à l’achat en libre-service et demandez-lui de [l’annuler.](manage-self-service-purchases-users.md#cancel-a-subscription)</span><span class="sxs-lookup"><span data-stu-id="ae538-146">Contact the person who bought the self-service purchase subscription and ask them to [cancel it](manage-self-service-purchases-users.md#cancel-a-subscription).</span></span>

## <a name="take-over-a-self-service-purchase-subscription"></a><span data-ttu-id="ae538-147">Prendre en compte un abonnement d’achat en libre-service</span><span class="sxs-lookup"><span data-stu-id="ae538-147">Take over a self-service purchase subscription</span></span>

<span data-ttu-id="ae538-148">Vous pouvez prendre le relais d’un abonnement d’achat en libre-service effectué par un utilisateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ae538-148">You can take over a self-service purchase subscription made by a user in your organization.</span></span> <span data-ttu-id="ae538-149">Lorsque vous prenez le relais d’un abonnement d’achat en libre-service, deux options s’offrent à vous :</span><span class="sxs-lookup"><span data-stu-id="ae538-149">When you take over a self-service purchase subscription, you have two options:</span></span>

1. <span data-ttu-id="ae538-150">Déplacez les utilisateurs vers un autre abonnement et annulez l’abonnement d’origine.</span><span class="sxs-lookup"><span data-stu-id="ae538-150">Move the users to a different subscription and cancel the original subscription.</span></span>
2. <span data-ttu-id="ae538-151">Annulez l’abonnement d’achat en libre-service et supprimez les licences des utilisateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="ae538-151">Cancel the self-service purchase subscription and remove licenses from assigned users.</span></span>

### <a name="move-users-to-a-different-subscription"></a><span data-ttu-id="ae538-152">Transférer des utilisateurs vers un autre abonnement</span><span class="sxs-lookup"><span data-stu-id="ae538-152">Move users to a different subscription</span></span>

<span data-ttu-id="ae538-153">Lorsque vous déplacez des utilisateurs vers un autre abonnement, l’ancien abonnement est automatiquement annulé.</span><span class="sxs-lookup"><span data-stu-id="ae538-153">When you move users to a different subscription, the old subscription is automatically canceled.</span></span> <span data-ttu-id="ae538-154">L’utilisateur qui a acheté à l’origine l’abonnement à l’achat en libre-service reçoit un courrier électronique qui indique que l’abonnement a été annulé.</span><span class="sxs-lookup"><span data-stu-id="ae538-154">The user who originally bought the self-service purchase subscription receives an email that says the subscription was canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="ae538-155">Vous devez avoir une licence disponible pour chaque utilisateur de l’abonnement vers qui vous souhaitez déplacer des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ae538-155">You must have an available license for each user you’re moving in the subscription that you’re moving users to.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="ae538-156">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-156">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="ae538-157">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration,</a>allez à la page  > **Facturation de vos produits.**</span><span class="sxs-lookup"><span data-stu-id="ae538-157">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Your products** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="ae538-158">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration,</a>allez à la page  > **Facturation de vos produits.**</span><span class="sxs-lookup"><span data-stu-id="ae538-158">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Your products** page.</span></span>

::: moniker-end

2. <span data-ttu-id="ae538-159">Sous **l’onglet** Produits, sélectionnez l’icône de filtre, puis sélectionnez **Libre-service.**</span><span class="sxs-lookup"><span data-stu-id="ae538-159">On the **Products** tab, select the filter icon, then select **Self-service**.</span></span>
3. <span data-ttu-id="ae538-160">Sélectionnez l’abonnement à prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="ae538-160">Select the subscription that you want to take over.</span></span>
4. <span data-ttu-id="ae538-161">Dans la page détails de l’abonnement, dans la section Abonnements et **paramètres,** sélectionnez **Prendre le contrôle de cet abonnement.**</span><span class="sxs-lookup"><span data-stu-id="ae538-161">On the subscription details page, in the **Subscriptions and settings** section, select **Take control of this subscription**.</span></span>
5. <span data-ttu-id="ae538-162">Dans le volet droit, sélectionnez **Déplacer des utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="ae538-162">In the right pane, select **Move users**.</span></span>
6. <span data-ttu-id="ae538-163">Sélectionnez le produit vers qui vous souhaitez déplacer les utilisateurs, puis **sélectionnez Déplacer les utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="ae538-163">Select the product that you want to move the users to, then select **Move users**.</span></span>
7. <span data-ttu-id="ae538-164">Dans la **zone Déplacer les utilisateurs vers,** **sélectionnez Déplacer les utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="ae538-164">In the **Move users to** box, select **Move users**.</span></span> <span data-ttu-id="ae538-165">Le processus de déplacement peut prendre plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="ae538-165">The move process might take several minutes.</span></span> <span data-ttu-id="ae538-166">Ne fermez pas votre navigateur pendant l’opération.</span><span class="sxs-lookup"><span data-stu-id="ae538-166">Don’t close your browser while the process runs.</span></span>
8. <span data-ttu-id="ae538-167">Lorsque le processus de déplacement est terminé, fermez le **volet Déplacer terminé.**</span><span class="sxs-lookup"><span data-stu-id="ae538-167">When the move process is finished, close the **Move completed pane**.</span></span>
9. <span data-ttu-id="ae538-168">Dans la page des  détails de l’abonnement, l’état de l’abonnement acheté en libre-service s’affiche **comme supprimé.**</span><span class="sxs-lookup"><span data-stu-id="ae538-168">On the subscription details page, the **Subscription status** for the self-service purchased subscription shows as **Deleted**.</span></span>

### <a name="cancel-a-self-service-purchase-subscription"></a><span data-ttu-id="ae538-169">Annuler un abonnement d’achat en libre-service</span><span class="sxs-lookup"><span data-stu-id="ae538-169">Cancel a self-service purchase subscription</span></span>

<span data-ttu-id="ae538-170">Lorsque vous choisissez d’annuler un abonnement d’achat en libre-service, les utilisateurs avec licences perdent l’accès au produit.</span><span class="sxs-lookup"><span data-stu-id="ae538-170">When you choose to cancel a self-service purchase subscription, users with licenses lose access to the product.</span></span> <span data-ttu-id="ae538-171">L’utilisateur qui a acheté à l’origine l’abonnement à l’achat en libre-service reçoit un courrier électronique qui indique que l’abonnement a été annulé.</span><span class="sxs-lookup"><span data-stu-id="ae538-171">The user who originally bought the self-service purchase subscription receives an email that says the subscription was canceled.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="ae538-172">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="ae538-172">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="ae538-173">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration,</a>allez à la page  > **Facturation de vos produits.**</span><span class="sxs-lookup"><span data-stu-id="ae538-173">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Billing** > **Your products** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="ae538-174">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration,</a>allez à la page  > **Facturation de vos produits.**</span><span class="sxs-lookup"><span data-stu-id="ae538-174">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Billing** > **Your products** page.</span></span>

::: moniker-end

2. <span data-ttu-id="ae538-175">Sous **l’onglet** Produits, sélectionnez l’icône de filtre, puis sélectionnez **Libre-service.**</span><span class="sxs-lookup"><span data-stu-id="ae538-175">On the **Products** tab, select the filter icon, then select **Self-service**.</span></span>
3. <span data-ttu-id="ae538-176">Sélectionnez l'abonnement que vous voulez annuler.</span><span class="sxs-lookup"><span data-stu-id="ae538-176">Select the subscription that you want to cancel.</span></span>
4. <span data-ttu-id="ae538-177">Dans la page détails de l’abonnement, dans la section Abonnements et **paramètres,** sélectionnez **Prendre le contrôle de cet abonnement.**</span><span class="sxs-lookup"><span data-stu-id="ae538-177">On the subscription details page, in the **Subscriptions and settings** section, select **Take control of this subscription**.</span></span>
5. <span data-ttu-id="ae538-178">Dans le volet droit, sélectionnez **Annuler l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="ae538-178">In the right pane, select **Cancel subscription**.</span></span>
6. <span data-ttu-id="ae538-179">Sélectionnez une raison pour votre annulation dans la liste de listes listes, puis sélectionnez **Annuler l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="ae538-179">Select a reason for your cancellation from the drop-down list, then select **Cancel subscription**.</span></span>
7. <span data-ttu-id="ae538-180">Dans la **zone Voulez-vous vraiment** annuler ? sélectionnez **Annuler l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="ae538-180">In the **Are you sure you want to cancel?** box, select **Cancel subscription**.</span></span>
8. <span data-ttu-id="ae538-181">Fermez le volet droit.</span><span class="sxs-lookup"><span data-stu-id="ae538-181">Close the right pane.</span></span>
9. <span data-ttu-id="ae538-182">Sur la page des détails de l’abonnement, **l’état de l’abonnement** s’affiche **comme supprimé.**</span><span class="sxs-lookup"><span data-stu-id="ae538-182">On the subscription details page, the **Subscription status** shows as **Deleted**.</span></span>

## <a name="need-help-contact-us"></a><span data-ttu-id="ae538-183">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="ae538-183">Need help?</span></span> <span data-ttu-id="ae538-184">Contactez-nous.</span><span class="sxs-lookup"><span data-stu-id="ae538-184">Contact us.</span></span>

<span data-ttu-id="ae538-185">Pour les questions courantes sur les achats en libre-service, consultez la FAQ sur les [achats en libre-service.](self-service-purchase-faq.md)</span><span class="sxs-lookup"><span data-stu-id="ae538-185">For common questions about self-service purchases, see [Self-service purchases FAQ](self-service-purchase-faq.md).</span></span>

<span data-ttu-id="ae538-186">Si vous avez des questions ou si vous avez besoin d’aide sur les achats en libre-service, [contactez le support technique.](../../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="ae538-186">If you have questions or need help with self-service purchases, [contact support](../../business-video/get-help-support.md).</span></span>