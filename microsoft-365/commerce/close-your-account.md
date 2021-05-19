---
title: Fermer votre compte
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: jkinma, jmueller
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- fwlink 2133922 to Delete subscription heading
- commerce_subscription
search.appverid: MET150
description: Découvrez comment fermer votre compte auprès de Microsoft.
ms.date: 04/02/2021
ms.openlocfilehash: ed73c191063a328490945c54dc2f5101c88f17e8
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52537294"
---
# <a name="close-your-account"></a><span data-ttu-id="05148-103">Fermer votre compte</span><span class="sxs-lookup"><span data-stu-id="05148-103">Close your account</span></span>

<span data-ttu-id="05148-104">Lorsque vous fermez votre compte auprès de Microsoft, toutes les informations relatives à votre compte sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="05148-104">When you close your account with Microsoft, all information related to your account is deleted.</span></span> <span data-ttu-id="05148-105">Ces informations incluent les abonnements, les licences, les modes de paiement, les utilisateurs et les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05148-105">This information includes subscriptions, licenses, payment methods, users, and user data.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="05148-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="05148-106">Before you begin</span></span>

<span data-ttu-id="05148-107">Avant de commencer ce processus, veillez à sauvegarder les données que vous voulez conserver.</span><span class="sxs-lookup"><span data-stu-id="05148-107">Before you start this process, make sure to back up any data that you want to preserve.</span></span>

<span data-ttu-id="05148-108">Pour suivre les étapes décrites dans cet article, vous devez être administrateur général ou de facturation.</span><span class="sxs-lookup"><span data-stu-id="05148-108">You must be a Global or Billing admin to do the tasks in this article.</span></span> <span data-ttu-id="05148-109">Pour plus d’informations, consultez la rubrique [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="05148-109">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>

## <a name="step-1-delete-users"></a><span data-ttu-id="05148-110">Étape 1 : Supprimer des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="05148-110">Step 1: Delete users</span></span>

<span data-ttu-id="05148-111">Supprimez tous les utilisateurs à l’exception d’un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="05148-111">Delete all users except for one global administrator.</span></span> <span data-ttu-id="05148-112">L’administrateur général termine les étapes de fermeture du compte.</span><span class="sxs-lookup"><span data-stu-id="05148-112">The global administrator completes the steps to close the account.</span></span> <span data-ttu-id="05148-113">Avant de pouvoir supprimer l’annuaire à la fin de ce processus, vous devez supprimer tous les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05148-113">Before you can delete the directory at the end of this process, you must delete all other users.</span></span>

<span data-ttu-id="05148-114">Si les utilisateurs sont synchronisés en local, désynchronisé, supprimez-les dans l’annuaire cloud à l’aide du portail Azure ou Azure PowerShell cmdlets.</span><span class="sxs-lookup"><span data-stu-id="05148-114">If users are synchronized from on-premises, first turn off sync, then delete the users in the cloud directory by using the Azure portal or Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="05148-115">Pour supprimer des utilisateurs, [consultez l’administrateur de gestion des utilisateurs : supprimez un ou plusieurs utilisateurs.](../admin/add-users/delete-a-user.md#user-management-admin-delete-one-or-more-users-from-office-365)</span><span class="sxs-lookup"><span data-stu-id="05148-115">To delete users, see [User management admin: Delete one or more users](../admin/add-users/delete-a-user.md#user-management-admin-delete-one-or-more-users-from-office-365).</span></span>

<span data-ttu-id="05148-116">Vous pouvez également utiliser [l’cmdlet Remove-MsolUser](/powershell/module/msonline/remove-msoluser) PowerShell pour supprimer des utilisateurs en bloc.</span><span class="sxs-lookup"><span data-stu-id="05148-116">You can also use the [Remove-MsolUser](/powershell/module/msonline/remove-msoluser) PowerShell cmdlet to delete users in bulk.</span></span>

<span data-ttu-id="05148-117">Si votre organisation utilise Active Directory qui se synchronise avec Microsoft Azure Active Directory (Azure AD), supprimez le compte d’utilisateur d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="05148-117">If your organization uses Active Directory that synchronizes with Microsoft Azure Active Directory (Azure AD), delete the user account from Active Directory, instead.</span></span> <span data-ttu-id="05148-118">Pour obtenir des instructions, [voir Suppression en bloc d’utilisateurs Azure Active Directory](/azure/active-directory/users-groups-roles/users-bulk-delete).</span><span class="sxs-lookup"><span data-stu-id="05148-118">For instructions, see [Bulk delete users in Azure Active Directory](/azure/active-directory/users-groups-roles/users-bulk-delete).</span></span>

## <a name="step-2-cancel-all-active-subscriptions"></a><span data-ttu-id="05148-119">Étape 2 : Annuler tous les abonnements actifs</span><span class="sxs-lookup"><span data-stu-id="05148-119">Step 2: Cancel all active subscriptions</span></span>

1. <span data-ttu-id="05148-120">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="05148-120">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="05148-121">Sous **l’onglet** Produits, recherchez un abonnement actif.</span><span class="sxs-lookup"><span data-stu-id="05148-121">On the **Products** tab, find an active subscription.</span></span> <span data-ttu-id="05148-122">Sélectionnez les trois points (plus d’actions), puis **sélectionnez Annuler l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="05148-122">Select the three dots (more actions), then select **Cancel subscription**.</span></span>
3. <span data-ttu-id="05148-123">Dans le volet **Annuler l’abonnement** , choisissez la raison pour laquelle vous annulez l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="05148-123">In the **Cancel subscription** pane, choose a reason why you're canceling.</span></span> <span data-ttu-id="05148-124">Vous pouvez également fournir des commentaires.</span><span class="sxs-lookup"><span data-stu-id="05148-124">Optionally, provide any feedback.</span></span>
4. <span data-ttu-id="05148-125">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="05148-125">Select **Save**.</span></span>
5. <span data-ttu-id="05148-126">Répétez les étapes 1 à 4 pour annuler tous les abonnements actifs.</span><span class="sxs-lookup"><span data-stu-id="05148-126">Repeat steps 1 through 4 to cancel all active subscriptions.</span></span>

## <a name="step-3-delete-all-disabled-subscriptions"></a><span data-ttu-id="05148-127">Étape 3 : Supprimer tous les abonnements désactivés</span><span class="sxs-lookup"><span data-stu-id="05148-127">Step 3: Delete all disabled subscriptions</span></span>

1. <span data-ttu-id="05148-128">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="05148-128">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="05148-129">Sous **l’onglet** Produits, sélectionnez un abonnement désactivé.</span><span class="sxs-lookup"><span data-stu-id="05148-129">On the **Products** tab, select a disabled subscription.</span></span>
3. <span data-ttu-id="05148-130">Dans la page détails de l’abonnement, dans la section Paramètres d’abonnement et de **paiement,** **sélectionnez Supprimer l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="05148-130">On the subscription details page, in the **Subscription and payment settings** section, select **Delete subscription**.</span></span>
4. <span data-ttu-id="05148-131">Dans le **volet Supprimer l’abonnement,** **sélectionnez Supprimer l’abonnement.**</span><span class="sxs-lookup"><span data-stu-id="05148-131">In the **Delete subscription** pane, select **Delete subscription**.</span></span>
5. <span data-ttu-id="05148-132">Dans la **boîte de dialogue Supprimer un** abonnement, sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="05148-132">In the **Delete subscription** dialog box, select **Yes**.</span></span>
6. <span data-ttu-id="05148-133">Pour chaque abonnement désactivé, répétez les étapes 3 à 5 jusqu’à ce que tous les abonnements soient supprimés.</span><span class="sxs-lookup"><span data-stu-id="05148-133">For each disabled subscription, repeat steps 3 through 5 until all subscriptions are deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="05148-134">Si vous ne parvenez pas à supprimer immédiatement un abonnement désactivé, [contactez le support technique.](../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="05148-134">If you're unable to immediately delete a disabled subscription, [contact support](../business-video/get-help-support.md).</span></span>

## <a name="step-4-disable-multi-factor-authentication"></a><span data-ttu-id="05148-135">Étape 4 : Désactiver l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="05148-135">Step 4: Disable multi-factor authentication</span></span>

1. <span data-ttu-id="05148-136">Connectez-vous au Centre d’administration avec un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="05148-136">Sign in to the admin center with a Global administrator account.</span></span> <span data-ttu-id="05148-137">Pour vérifier les rôles que vous avez, [consultez Vérifier les rôles d’administrateur dans votre organisation.](../admin/add-users/assign-admin-roles.md#check-admin-roles-in-your-organization)</span><span class="sxs-lookup"><span data-stu-id="05148-137">To verify what roles you have, see [Check admin roles in your organization](../admin/add-users/assign-admin-roles.md#check-admin-roles-in-your-organization).</span></span>
2. <span data-ttu-id="05148-138">Go to the **Users**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span><span class="sxs-lookup"><span data-stu-id="05148-138">Go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
3. <span data-ttu-id="05148-139">Choisissez **Authentification multifacteur.**</span><span class="sxs-lookup"><span data-stu-id="05148-139">Choose **Multi-factor authentication**.</span></span>
4. <span data-ttu-id="05148-140">Dans la page Authentification multifacteur, désactivez tous les comptes à l’exception du compte d’administrateur général que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="05148-140">On the multi-factor authentication page, disable all accounts except for the global admin account that you're currently using.</span></span>

<span data-ttu-id="05148-141">Vous pouvez également [utiliser PowerShell pour désactiver l’authentification multifacteur pour plusieurs utilisateurs.](/azure/active-directory/authentication/howto-mfa-userstates#change-state-using-powershell)</span><span class="sxs-lookup"><span data-stu-id="05148-141">You can also [use PowerShell to disable multi-factor authentication for multiple users](/azure/active-directory/authentication/howto-mfa-userstates#change-state-using-powershell).</span></span>


## <a name="step-5-delete-the-directory-in-azure-active-directory"></a><span data-ttu-id="05148-142">Étape 5 : Supprimer le répertoire dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="05148-142">Step 5: Delete the directory in Azure Active Directory</span></span>

1. <span data-ttu-id="05148-143">Connectez-vous au <a href="https://aad.portal.azure.com/" target="_blank">Centre d’administration Azure AD</a> avec un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="05148-143">Sign in to the <a href="https://aad.portal.azure.com/" target="_blank">Azure AD admin center</a> with a Global administrator account.</span></span>
2. <span data-ttu-id="05148-144">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="05148-144">Select **Azure Active Directory**.</span></span>
3. <span data-ttu-id="05148-145">Basculez vers l’organisation que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="05148-145">Switch to the organization that you want to delete.</span></span>
4. <span data-ttu-id="05148-146">Sélectionnez **Supprimer le client.**</span><span class="sxs-lookup"><span data-stu-id="05148-146">Select **Delete tenant**.</span></span>
5. <span data-ttu-id="05148-147">Si votre organisation échoue à une ou plusieurs vérifications, un lien vous permet d’obtenir plus d’informations sur la façon de les réussir.</span><span class="sxs-lookup"><span data-stu-id="05148-147">If your organization fails one or more checks, you see a link to more information on how to pass the checks.</span></span> <span data-ttu-id="05148-148">Après avoir réussi toutes les vérifications, **sélectionnez Supprimer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="05148-148">After you pass all checks, select **Delete** to complete the process.</span></span>

<span data-ttu-id="05148-149">Une fois cette dernière étape terminée, votre compte microsoft est fermé et supprimé.</span><span class="sxs-lookup"><span data-stu-id="05148-149">After you complete this final step, your account with Microsoft is closed and deleted.</span></span>
