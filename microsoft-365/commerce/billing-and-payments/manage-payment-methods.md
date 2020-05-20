---
title: Gestion des modes de paiement
f1.keywords:
- CSH
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
- Adm_TOC
- commerce
ms.custom:
- TopSMBIssues
- okr_SMB
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
description: Découvrez comment gérer vos modes de paiement dans le centre d’administration 365 de Microsoft.
ms.openlocfilehash: d31da19c10eb61719ba813d271dbdcf573a5aff3
ms.sourcegitcommit: 5c43e89ed94ad9fd1db049446383c65e548189b7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "44322158"
---
# <a name="manage-payment-methods"></a><span data-ttu-id="6a2e8-103">Gestion des modes de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-103">Manage payment methods</span></span>

::: moniker range="o365-21vianet"
> [!NOTE]
> <span data-ttu-id="6a2e8-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-104">The admin center is changing.</span></span> <span data-ttu-id="6a2e8-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>
::: moniker-end

<span data-ttu-id="6a2e8-106">Lorsque vous achetez des produits ou services d’entreprise auprès de Microsoft, vous pouvez utiliser un mode de paiement existant ou en ajouter un nouveau.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-106">When you buy business products or services from Microsoft, you can use an existing payment method, or add a new one.</span></span> <span data-ttu-id="6a2e8-107">Vous pouvez utiliser une carte bancaire ou un compte bancaire pour payer les éléments que vous achetez.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-107">You can use a credit or debit card, or bank account to pay for the things you buy.</span></span>

<span data-ttu-id="6a2e8-108">Si votre compte professionnel dispose d’un profil de facturation et que vous êtes un propriétaire de profil de facturation ou un collaborateur de profil de facturation, vous pouvez utiliser le profil de facturation qui est sauvegardé par carte bancaire ou paiement de facture pour effectuer des achats ou payer des factures.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-108">If your business account has a billing profile, and you are a billing profile owner or billing profile contributor, you can use the billing profile that's backed by a credit card or invoice payment to make purchases or pay bills.</span></span> <span data-ttu-id="6a2e8-109">Si vous êtes gestionnaire de factures de facturation, vous pouvez uniquement utiliser un profil de facturation pour payer des factures.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-109">If you're a billing invoice manager, you can only use a billing profile to pay bills.</span></span> <span data-ttu-id="6a2e8-110">Pour en savoir plus sur les profils de facturation et les rôles, consultez la rubrique [Manage Billing Profiles](manage-billing-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-110">To learn more about billing profiles and roles, see [Manage billing profiles](manage-billing-profiles.md).</span></span>

<span data-ttu-id="6a2e8-111">Si votre compte professionnel ne dispose pas d’un profil de facturation, tout administrateur général ou de facturation peut gérer et utiliser n’importe quel compte bancaire ajouté au compte professionnel.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-111">If your business account doesn't have a billing profile, any Global or Billing admin can manage and use any bank account that is added to the business account.</span></span> <span data-ttu-id="6a2e8-112">Toutefois, vous ne pouvez gérer ou utiliser que les cartes de crédit que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-112">However, you can only manage or use credit cards that you add.</span></span>

> [!NOTE]
> <span data-ttu-id="6a2e8-113">L’option de paiement avec un compte bancaire n’est pas disponible dans certains pays ou certaines régions.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-113">The option to pay with a bank account is not available in some countries or regions.</span></span>
>
> <span data-ttu-id="6a2e8-114">Vous devez utiliser un mode de paiement émis par le même pays que votre client.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-114">You must use a payment method issued from the same country as your tenant.</span></span>

## <a name="add-a-payment-method"></a><span data-ttu-id="6a2e8-115">Ajouter un mode de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-115">Add a payment method</span></span>

<span data-ttu-id="6a2e8-116">L’ajout d’un mode de paiement n’associe pas d’abonnements à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-116">Adding a payment method doesn't associate any subscriptions with it.</span></span> <span data-ttu-id="6a2e8-117">Pour affecter un seul abonnement au mode de paiement, reportez-vous à la rubrique [modifier un mode de paiement pour un seul abonnement](#change-a-payment-method-for-a-single-subscription).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-117">To assign a single subscription to the payment method, see [Change a payment method for a single subscription](#change-a-payment-method-for-a-single-subscription).</span></span> <span data-ttu-id="6a2e8-118">Pour remplacer tous les abonnements utilisant un autre mode de paiement par le nouveau, reportez-vous à la rubrique [remplacement d’un mode de paiement](#replace-a-payment-method).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-118">To replace all subscriptions that use another payment method with the new one, see [Replace a payment method](#replace-a-payment-method).</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-119">Dans le centre d’administration, accédez à **la** > page **factures &** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">paiement</a> des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-119">In the admin center, go to the **Billing** > **Bills & payments** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">Payment methods</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-120">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-120">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-121">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-121">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-122">Sélectionnez **Ajouter ou sélectionner un mode de paiement**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-122">Select **Add a payment method**.</span></span>

3. <span data-ttu-id="6a2e8-123">Sur la page **Modes de paiement**, sélectionnez un mode de paiement dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-123">On the **Payment methods** page, pick a payment method from the drop-down menu.</span></span>

4. <span data-ttu-id="6a2e8-124">Entrez les informations pour la nouvelle carte ou le nouveau compte bancaire, puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-124">Enter the information for the new card or bank account, then select **Add**.</span></span>

## <a name="update-payment-method-details"></a><span data-ttu-id="6a2e8-125">Mettre à jour les détails du mode de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-125">Update payment method details</span></span>

<span data-ttu-id="6a2e8-126">Vous pouvez modifier le nom de la carte bancaire, de l’adresse de facturation ou de la date d’expiration d’un mode de paiement existant.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-126">You can change the name on the credit or debit card, billing address, or expiration date for an existing payment method.</span></span> <span data-ttu-id="6a2e8-127">Toutefois, vous ne pouvez pas modifier la carte ou le numéro de compte.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-127">However, you can't change the card or account number.</span></span> <span data-ttu-id="6a2e8-128">Si le numéro de compte a changé, [Remplacez-le par un autre mode de paiement](#replace-a-payment-method), puis [supprimez l’ancien](#delete-a-payment-method).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-128">If the account number has changed, [replace it with a different payment method](#replace-a-payment-method), and then [delete the old one](#delete-a-payment-method).</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-129">Dans le centre d’administration, accédez à **la** > page **factures &** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">paiement</a> des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-129">In the admin center, go to the **Billing** > **Bills & payments** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">Payment methods</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-130">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-130">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-131">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-131">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-132">Sélectionnez la ligne du mode de paiement à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-132">Select the row of the payment method to update.</span></span> <span data-ttu-id="6a2e8-133">Dans le volet droit, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-133">In the right pane, select **Edit**.</span></span>

3. <span data-ttu-id="6a2e8-134">Mettez à jour les informations de votre mode de paiement, notamment le nom de la carte bancaire, de l’adresse de facturation ou de la date d’expiration, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-134">Update your payment method information, including the name on the credit or debit card, billing address, or expiration date, and then select **Save**.</span></span>

## <a name="replace-a-payment-method"></a><span data-ttu-id="6a2e8-135">Remplacer un mode de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-135">Replace a payment method</span></span>

<span data-ttu-id="6a2e8-136">Lorsque vous remplacez un mode de paiement, vous le remplacez pour tous les abonnements et les profils de facturation qui utilisent le même mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-136">When you replace a payment method, you replace it for all subscriptions and billing profiles that use the same payment method.</span></span> <span data-ttu-id="6a2e8-137">Le remplacement d’un mode de paiement n’entraîne pas la suppression du mode de paiement existant.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-137">Replacing a payment method doesn't delete the existing payment method.</span></span> <span data-ttu-id="6a2e8-138">Vous pouvez toujours sélectionner et utiliser d’autres abonnements et profils de facturation.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-138">It's still available for you to select and use for other subscriptions and billing profiles.</span></span>

<span data-ttu-id="6a2e8-139">Pour modifier le mode de paiement d’un abonnement unique, consultez la rubrique [modifier un mode de paiement pour un seul abonnement](#change-a-payment-method-for-a-single-subscription).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-139">To change the payment method for a single subscription, see [Change a payment method for a single subscription](#change-a-payment-method-for-a-single-subscription).</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-140">Dans le centre d’administration, accédez à **la** > page **factures &** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">paiement</a> des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-140">In the admin center, go to the **Billing** > **Bills & payments** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">Payment methods</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-141">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-141">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-142">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-142">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-143">Sélectionnez la ligne du mode de paiement à remplacer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-143">Select the row of the payment method to replace.</span></span> <span data-ttu-id="6a2e8-144">Le volet droit répertorie tous les profils de facturation et les abonnements individuels qui utilisent le mode de paiement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-144">The right pane lists all billing profiles and individual subscriptions that use the selected payment method.</span></span>

3. <span data-ttu-id="6a2e8-145">Dans le volet droit, sélectionnez **remplacer le mode de paiement pour tous les éléments**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-145">In the right pane, select **Replace payment method for all items**.</span></span>

4. <span data-ttu-id="6a2e8-146">Pour utiliser un mode de paiement existant, sélectionnez-en un dans la liste déroulante, puis sélectionnez **remplacer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-146">To use an existing payment method, choose one from the drop-down list, then select **Replace**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6a2e8-147">Si vous avez des abonnements associés à un profil de facturation, vous pouvez uniquement utiliser une carte bancaire pour les payer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-147">If you have subscriptions associated with a billing profile, you can only use a credit or debit card to pay for them.</span></span> <span data-ttu-id="6a2e8-148">Si vous avez des comptes bancaires répertoriés sur la page **modes de paiement** , ils ne sont pas disponibles dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-148">If you have bank accounts listed on the **Payment methods** page, they aren't available to select in the drop-down list.</span></span>

5. <span data-ttu-id="6a2e8-149">Pour ajouter un nouveau mode de paiement, sélectionnez **Ajouter un mode de paiement**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-149">To add a new payment method, select **Add payment method**.</span></span>

6. <span data-ttu-id="6a2e8-150">Dans le volet **Ajouter un mode de paiement** , entrez les informations de compte, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-150">In the **Add a payment method** pane, enter the account information, then select **Save**.</span></span> <span data-ttu-id="6a2e8-151">Vous devez utiliser un mode de paiement du même pays que votre client.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-151">You must use a payment method from the same country as your tenant.</span></span>

7. <span data-ttu-id="6a2e8-152">Le nouveau mode de paiement est déjà sélectionné dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-152">The new payment method is already selected in the drop-down list.</span></span> <span data-ttu-id="6a2e8-153">Sélectionnez **Remplacer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-153">Select **Replace**.</span></span>

## <a name="change-a-payment-method-for-a-single-subscription"></a><span data-ttu-id="6a2e8-154">Modifier un mode de paiement pour un abonnement unique</span><span class="sxs-lookup"><span data-stu-id="6a2e8-154">Change a payment method for a single subscription</span></span>

<span data-ttu-id="6a2e8-155">Vous pouvez modifier le mode de paiement utilisé pour payer un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-155">You can change the payment method used to pay for a single subscription.</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-156">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-156">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-157">Dans le centre d’administration, accédez à la page **Facturation** > **Produits**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-157">In the admin center, go to the **Billing** > **Your products** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-158">Dans le centre d’administration, accédez à la page **Facturation** > **Produits**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-158">In the admin center, go to the **Billing** > **Your products** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-159">Sous l’onglet **abonnements** , sélectionnez l’abonnement que vous souhaitez payer avec l’autre mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-159">On the **Subscriptions** tab, select the subscription that you want to pay for with the alternate payment method.</span></span>

3. <span data-ttu-id="6a2e8-160">Sous **facturation**, en regard de mode de paiement, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-160">Under **Billing**, next to the payment method, select **Edit**.</span></span>

4. <span data-ttu-id="6a2e8-161">En regard de votre mode de paiement existant, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-161">Next to your existing payment method, select **Change**.</span></span>

5. <span data-ttu-id="6a2e8-162">Dans la liste déroulante, choisissez un autre mode de paiement ou choisissez d’ajouter un mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-162">From the drop-down list, choose an alternate payment method, or choose to add a payment method.</span></span>

6. <span data-ttu-id="6a2e8-163">Si vous ajoutez un mode de paiement, entrez les informations sur la carte ou le compte, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-163">If you add a payment method, enter the card or account details, then select **Save**.</span></span>

7. <span data-ttu-id="6a2e8-164">Vérifiez que le mode de paiement sélectionné est correct, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-164">Verify that the selected payment method is correct, then select **Save**.</span></span>

## <a name="delete-a-payment-method"></a><span data-ttu-id="6a2e8-165">Supprimer un mode de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-165">Delete a payment method</span></span>

<span data-ttu-id="6a2e8-166">Vous pouvez supprimer uniquement un mode de paiement qui n’est pas associé à un abonnement ou un profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-166">You can only delete a payment method that isn't attached to a subscription or billing profile.</span></span> <span data-ttu-id="6a2e8-167">Cela s’applique à tous les abonnements, quel que soit leur état.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-167">This applies to all subscriptions, whatever their status.</span></span>

### <a name="delete-a-payment-method-with-no-subscriptions-or-billing-profiles-attached"></a><span data-ttu-id="6a2e8-168">Supprimer un mode de paiement sans abonnement ni profil de facturation associé</span><span class="sxs-lookup"><span data-stu-id="6a2e8-168">Delete a payment method with no subscriptions or billing profiles attached</span></span>

<span data-ttu-id="6a2e8-169">Si aucun mode de paiement n’est associé à des abonnements ou des profils de facturation, vous pouvez immédiatement le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-169">If a payment method isn't associated with any subscriptions or billing profiles, you can immediately delete it.</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-170">Dans le centre d’administration, accédez à **la** > page **factures &** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">paiement</a> des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-170">In the admin center, go to the **Billing** > **Bills & payments** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">Payment methods</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-171">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-171">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-172">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-172">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-173">Recherchez le mode de paiement à supprimer, sélectionnez les trois points, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-173">Find the payment method to delete, select the three dots, then select **Delete**.</span></span>

3. <span data-ttu-id="6a2e8-174">En bas du volet droit, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-174">At the bottom of the right pane, select **Delete**.</span></span>

### <a name="delete-a-payment-method-with-subscriptions-or-billing-profiles-attached"></a><span data-ttu-id="6a2e8-175">Supprimer un mode de paiement avec des abonnements ou des profils de facturation liés</span><span class="sxs-lookup"><span data-stu-id="6a2e8-175">Delete a payment method with subscriptions or billing profiles attached</span></span>

<span data-ttu-id="6a2e8-176">Si un mode de paiement est associé à des abonnements ou des profils de facturation, commencez par le remplacer par un mode de paiement existant, ou ajoutez-en un nouveau, puis supprimez l’ancien mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-176">If a payment method is attached to any subscriptions or billing profiles, first replace it with an existing payment method, or add a new one, then delete the old payment method.</span></span>

::: moniker range="o365-worldwide"
1. <span data-ttu-id="6a2e8-177">Dans le centre d’administration, accédez à **la** > page **factures &** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">paiement</a> des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-177">In the admin center, go to the **Billing** > **Bills & payments** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2018806" target="_blank">Payment methods</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"
1. <span data-ttu-id="6a2e8-178">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-178">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

::: moniker range="o365-21vianet"
1. <span data-ttu-id="6a2e8-179">Dans le centre d’administration, accédez à **la** > page **factures &** > **paiement** des paiements.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-179">In the admin center, go to the **Billing** > **Bills & payments** > **Payment methods** page.</span></span>
::: moniker-end

2. <span data-ttu-id="6a2e8-180">Sélectionnez la ligne du mode de paiement à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-180">Select the row for the payment method to delete.</span></span> <span data-ttu-id="6a2e8-181">Le volet droit répertorie les abonnements existants qui utilisent ce mode de paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-181">The right pane lists existing subscriptions that use that payment method.</span></span>

3. <span data-ttu-id="6a2e8-182">Dans le volet droit, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-182">In the right pane, select **Delete**.</span></span>

4. <span data-ttu-id="6a2e8-183">Pour utiliser un mode de paiement existant, sélectionnez-en un dans la liste déroulante, cliquez sur **suivant**, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-183">To use an existing payment method, choose one from the drop-down list, select **Next**, and then select **Delete**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6a2e8-184">Si vous avez des abonnements associés à un profil de facturation, vous pouvez uniquement utiliser une carte de crédit pour les payer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-184">If you have subscriptions associated with a billing profile, you can only use a credit card to pay for them.</span></span> <span data-ttu-id="6a2e8-185">Si vous avez des comptes bancaires répertoriés sur la page **modes de paiement** , ils ne sont pas disponibles dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-185">If you have bank accounts listed on the **Payment methods** page, they aren't available to choose in the drop-down list.</span></span>

5. <span data-ttu-id="6a2e8-186">Pour ajouter un nouveau mode de paiement, sélectionnez **Ajouter un mode de paiement**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-186">To add a new payment method, select **Add payment method**.</span></span>

6. <span data-ttu-id="6a2e8-187">Choisissez le type de mode de paiement que vous souhaitez ajouter, entrez les informations de compte, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-187">Choose the type of payment method that you want to add, enter the account information, and then select **Save**.</span></span>

7. <span data-ttu-id="6a2e8-188">Le nouveau mode de paiement est déjà sélectionné dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-188">The new payment method is already selected in the drop-down list.</span></span> <span data-ttu-id="6a2e8-189">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-189">Select **Next**.</span></span>

8. <span data-ttu-id="6a2e8-190">Sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-190">Select **Delete**.</span></span>

## <a name="troubleshoot-payment-methods"></a><span data-ttu-id="6a2e8-191">Résolution des problèmes des modes de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-191">Troubleshoot payment methods</span></span>

|<span data-ttu-id="6a2e8-192">**Problème**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-192">**Issue**</span></span>|<span data-ttu-id="6a2e8-193">**Étapes de dépannage**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-193">**Troubleshooting steps**</span></span>|
|:----------|:-----|
|<span data-ttu-id="6a2e8-194">**J’obtiens un message d’erreur indiquant « le navigateur est actuellement configuré pour bloquer les cookies ».**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-194">**I get an error message that says, "The browser is currently set to block cookies."**</span></span> |<span data-ttu-id="6a2e8-195">Configurez votre navigateur pour autoriser les cookies tiers, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-195">Set your browser to allow third-party cookies and try again.</span></span> |
|<span data-ttu-id="6a2e8-196">**Ma carte bancaire a été refusée.**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-196">**My credit or debit card was declined.**</span></span> |<span data-ttu-id="6a2e8-197">Si vous payez par carte bancaire, et que votre carte est refusée, vous recevez un message indiquant que Microsoft n’a pas pu traiter le paiement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-197">If you pay by credit or debit card, and your card is declined, you receive an email that says Microsoft was unable to process the payment.</span></span> <span data-ttu-id="6a2e8-198">Vérifiez que le &mdash; numéro de carte de détails de carte, la date d’expiration, le nom sur la carte et l’adresse, y compris la ville, l’État et le code postal &mdash; apparaissent exactement comme sur la carte et votre relevé.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-198">Double-check that the card details&mdash;card number, expiration date, name on the card, and address, including city, state, and ZIP code&mdash;appear exactly as they do on the card and your statement.</span></span> <span data-ttu-id="6a2e8-199">Vous pouvez mettre à jour les informations de votre carte et en envoyer immédiatement le paiement à l’aide du lien **solde de règlement** dans la section **facturation** de la page Détails de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-199">You can update your card information and immediately submit the payment by using the **Settle balance** link in the **Billing** section of the subscription details page.</span></span> <span data-ttu-id="6a2e8-200">Pour plus d’informations, consultez la rubrique [que se passe-t-il si ma carte de crédit a été refusée et mon paiement est échu ?](pay-for-your-subscription.md#what-if-my-credit-card-was-declined-and-my-payment-is-past-due)</span><span class="sxs-lookup"><span data-stu-id="6a2e8-200">For more information, see [What if my credit card was declined and my payment is past due?](pay-for-your-subscription.md#what-if-my-credit-card-was-declined-and-my-payment-is-past-due)</span></span>  <br/><br/>  <span data-ttu-id="6a2e8-201">Si vous obtenez toujours le message de refus de la carte bancaire, contactez votre banque.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-201">If you continue to see the "declined" message, contact your bank.</span></span> <span data-ttu-id="6a2e8-202">Votre carte n’est peut-être pas active.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-202">It's possible that your card isn't active.</span></span> <span data-ttu-id="6a2e8-203">Si vous avez récemment reçu la carte dans le message avec une date d’expiration mise à jour, assurez-vous qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-203">If you recently received the card in the mail with an updated expiration date, make sure it's activated.</span></span> <span data-ttu-id="6a2e8-204">Votre banque peut également vous indiquer si votre carte n’est pas approuvée pour les transactions en ligne, internationales ou périodiques.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-204">Your bank can also tell you whether your card isn't approved for online, international, or recurring transactions.</span></span> |
|<span data-ttu-id="6a2e8-205">**Je veux mettre à jour une carte ou un numéro de compte bancaire.**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-205">**I want to update a card or bank account number.**</span></span> |<span data-ttu-id="6a2e8-206">Vous ne pouvez pas modifier la carte ou le numéro de compte d’un mode de paiement existant.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-206">You can't change the card or account number on an existing payment method.</span></span> <span data-ttu-id="6a2e8-207">Si le numéro de votre carte ou de votre compte a changé, [Remplacez-le par un autre mode de paiement](#replace-a-payment-method), ce qui déplace tous les abonnements actifs du mode de paiement vers le nouveau, puis [supprimez l’ancien mode de paiement](#delete-a-payment-method-with-no-subscriptions-or-billing-profiles-attached).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-207">If your card or account number has changed, [replace it with a different payment method](#replace-a-payment-method), which moves all active subscriptions from the payment method to the new one, then [delete the old payment method](#delete-a-payment-method-with-no-subscriptions-or-billing-profiles-attached).</span></span> |
|<span data-ttu-id="6a2e8-208">**Je ne dispose que d’une carte ou d’un compte bancaire sur mon compte et je souhaite le supprimer.**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-208">**I only have one card or bank account on my account and I want to remove it.**</span></span> |<span data-ttu-id="6a2e8-209">Si vous n’avez qu’un seul mode de paiement, vous devez le [remplacer par un nouveau mode de paiement](#replace-a-payment-method) avant de pouvoir le supprimer.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-209">If you only have one payment method, you must [replace it with a new payment method](#replace-a-payment-method) before you can delete it.</span></span> |
|<span data-ttu-id="6a2e8-210">**Je ne parviens pas à ajouter ma carte ou mon compte bancaire.**</span><span class="sxs-lookup"><span data-stu-id="6a2e8-210">**I can't add my card or bank account.**</span></span>  |<span data-ttu-id="6a2e8-211">Vous devez utiliser un mode de paiement émis par le même pays que votre client.</span><span class="sxs-lookup"><span data-stu-id="6a2e8-211">You must use a payment method issued from the same country as your tenant.</span></span> <span data-ttu-id="6a2e8-212">Si vous ne parvenez pas à entrer les informations de votre carte ou de votre compte bancaire, vous pouvez [contacter le support technique](../../admin/contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="6a2e8-212">If you have trouble entering your card or bank account information, you can [contact support](../../admin/contact-support-for-business-products.md).</span></span> |

## <a name="related-articles"></a><span data-ttu-id="6a2e8-213">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6a2e8-213">Related articles</span></span>

[<span data-ttu-id="6a2e8-214">Payez votre abonnement professionnel</span><span class="sxs-lookup"><span data-stu-id="6a2e8-214">Pay for your business subscription</span></span>](pay-for-your-subscription.md)

[<span data-ttu-id="6a2e8-215">Gérer les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="6a2e8-215">Manage billing profiles</span></span>](manage-billing-profiles.md)

[<span data-ttu-id="6a2e8-216">Modifier la fréquence de paiement</span><span class="sxs-lookup"><span data-stu-id="6a2e8-216">Change your payment frequency</span></span>](change-payment-frequency.md)