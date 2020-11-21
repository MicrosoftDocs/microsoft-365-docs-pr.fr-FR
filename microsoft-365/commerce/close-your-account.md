---
title: Fermer votre compte
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
- commerce
ms.custom:
- AdminSurgePortfolio
- fwlink 2133922 to Delete subscription heading
search.appverid:
- MET150
description: Découvrez comment fermer votre compte auprès de Microsoft.
ms.openlocfilehash: bdcf4408ddc9c198fab1d68b4c096fad9059b975
ms.sourcegitcommit: 20d1158c54a5058093eb8aac23d7e4dc68054688
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2020
ms.locfileid: "49376316"
---
# <a name="close-your-account"></a><span data-ttu-id="2e110-103">Fermer votre compte</span><span class="sxs-lookup"><span data-stu-id="2e110-103">Close your account</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="2e110-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="2e110-104">The admin center is changing.</span></span> <span data-ttu-id="2e110-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2e110-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="2e110-106">Lorsque vous fermez votre compte auprès de Microsoft, toutes les informations relatives à votre compte sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2e110-106">When you close your account with Microsoft, all information related to your account is deleted.</span></span> <span data-ttu-id="2e110-107">Ces informations incluent les abonnements, les licences, les modes de paiement, les utilisateurs et les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2e110-107">This information includes subscriptions, licenses, payment methods, users, and user data.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2e110-108">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2e110-108">Before you begin</span></span>

<span data-ttu-id="2e110-109">Avant de commencer ce processus, veillez à sauvegarder les données que vous voulez conserver.</span><span class="sxs-lookup"><span data-stu-id="2e110-109">Before you start this process, make sure to back up any data that you want to preserve.</span></span>

<span data-ttu-id="2e110-110">Vous devez être un administrateur général ou un administrateur de facturation pour effectuer les tâches décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2e110-110">You must be a Global or Billing admin to do the tasks in this article.</span></span> <span data-ttu-id="2e110-111">Si vous souhaitez en savoir plus, veuillez consulter la page [À propos des rôles d’administrateur](../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2e110-111">For more information, see [About admin roles](../admin/add-users/about-admin-roles.md).</span></span>

## <a name="step-1-delete-users"></a><span data-ttu-id="2e110-112">Étape 1 : supprimer des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2e110-112">Step 1: Delete users</span></span>

<span data-ttu-id="2e110-113">Supprimez tous les utilisateurs à l’exception d’un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2e110-113">Delete all users except for one global administrator.</span></span> <span data-ttu-id="2e110-114">L’administrateur général termine les étapes de fermeture du compte.</span><span class="sxs-lookup"><span data-stu-id="2e110-114">The global administrator completes the steps to close the account.</span></span> <span data-ttu-id="2e110-115">Avant de pouvoir supprimer le répertoire à la fin de ce processus, vous devez supprimer tous les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2e110-115">Before you can delete the directory at the end of this process, you must delete all other users.</span></span>

<span data-ttu-id="2e110-116">Si les utilisateurs sont synchronisés en local, désactivez la synchronisation, puis supprimez les utilisateurs dans le répertoire Cloud à l’aide du portail Azure ou des applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e110-116">If users are synchronized from on-premises, first turn off sync, then delete the users in the cloud directory by using the Azure portal or Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="2e110-117">Pour supprimer des utilisateurs, consultez la rubrique <a href="https://docs.microsoft.com/office365/admin/add-users/delete-a-user?view=o365-worldwide#user-management-admin-delete-one-or-more-users-from-office-365">administrateur de gestion des utilisateurs : supprimer un ou plusieurs utilisateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="2e110-117">To delete users, see <a href="https://docs.microsoft.com/office365/admin/add-users/delete-a-user?view=o365-worldwide#user-management-admin-delete-one-or-more-users-from-office-365">User management admin: Delete one or more users</a>.</span></span>

<span data-ttu-id="2e110-118">Vous pouvez également utiliser l’applet de commande PowerShell <a href="https://go.microsoft.com/fwlink/?linkid=842230">Remove-MsolUser</a> pour supprimer des utilisateurs en bloc.</span><span class="sxs-lookup"><span data-stu-id="2e110-118">You can also use the <a href="https://go.microsoft.com/fwlink/?linkid=842230">Remove-MsolUser</a> PowerShell cmdlet to delete users in bulk.</span></span>

<span data-ttu-id="2e110-119">Si votre organisation utilise Active Directory qui se synchronise avec Microsoft Azure Active Directory (Azure AD), supprimez le compte d’utilisateur d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e110-119">If your organization uses Active Directory that synchronizes with Microsoft Azure Active Directory (Azure AD), delete the user account from Active Directory, instead.</span></span> <span data-ttu-id="2e110-120">Pour obtenir des instructions, consultez la rubrique <a href="https://docs.microsoft.com/azure/active-directory/users-groups-roles/users-bulk-delete">suppression en bloc d’utilisateurs dans Azure Active Directory</a>.</span><span class="sxs-lookup"><span data-stu-id="2e110-120">For instructions, see <a href="https://docs.microsoft.com/azure/active-directory/users-groups-roles/users-bulk-delete">Bulk delete users in Azure Active Directory</a>.</span></span>

## <a name="step-2-cancel-all-active-subscriptions"></a><span data-ttu-id="2e110-121">Étape 2 : annuler tous les abonnements actifs</span><span class="sxs-lookup"><span data-stu-id="2e110-121">Step 2: Cancel all active subscriptions</span></span>

1. <span data-ttu-id="2e110-122">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="2e110-122">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="2e110-123">Sous l’onglet **produits** , recherchez un abonnement actif.</span><span class="sxs-lookup"><span data-stu-id="2e110-123">On the **Products** tab, find an active subscription.</span></span> <span data-ttu-id="2e110-124">Sélectionnez **Autres actions** (points de suspension), puis sélectionnez **Annuler l’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="2e110-124">Select **More actions** (three dots), then select **Cancel subscription**.</span></span>
3. <span data-ttu-id="2e110-125">Dans le volet **Annuler l’abonnement** , choisissez la raison pour laquelle vous annulez l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e110-125">In the **Cancel subscription** pane, choose a reason why you're canceling.</span></span> <span data-ttu-id="2e110-126">Vous pouvez également fournir des commentaires.</span><span class="sxs-lookup"><span data-stu-id="2e110-126">Optionally, provide any feedback.</span></span>
4. <span data-ttu-id="2e110-127">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2e110-127">Select **Save**.</span></span>
5. <span data-ttu-id="2e110-128">Répétez les étapes 1 à 4 pour annuler tous les abonnements actifs.</span><span class="sxs-lookup"><span data-stu-id="2e110-128">Repeat steps 1 through 4 to cancel all active subscriptions.</span></span>

## <a name="step-3-delete-all-disabled-subscriptions"></a><span data-ttu-id="2e110-129">Étape 3 : supprimer tous les abonnements désactivés</span><span class="sxs-lookup"><span data-stu-id="2e110-129">Step 3: Delete all disabled subscriptions</span></span>

1. <span data-ttu-id="2e110-130">Dans le centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Vos produits</a>.</span><span class="sxs-lookup"><span data-stu-id="2e110-130">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="2e110-131">Sous l’onglet **produits** , sélectionnez un abonnement désactivé.</span><span class="sxs-lookup"><span data-stu-id="2e110-131">On the **Products** tab, select a disabled subscription.</span></span>
3. <span data-ttu-id="2e110-132">Sur la page Détails de l’abonnement, dans la section **paramètres d’abonnement et de paiement** , sélectionnez **Supprimer l’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="2e110-132">On the subscription details page, in the **Subscription and payment settings** section, select **Delete subscription**.</span></span>
4. <span data-ttu-id="2e110-133">Dans le volet **supprimer un abonnement** , sélectionnez Supprimer un **abonnement**.</span><span class="sxs-lookup"><span data-stu-id="2e110-133">In the **Delete subscription** pane, select **Delete subscription**.</span></span>
5. <span data-ttu-id="2e110-134">Dans la boîte de dialogue **supprimer un abonnement** , sélectionnez **Oui**.</span><span class="sxs-lookup"><span data-stu-id="2e110-134">In the **Delete subscription** dialog box, select **Yes**.</span></span>
6. <span data-ttu-id="2e110-135">Pour chaque abonnement désactivé, répétez les étapes 3 à 5 jusqu’à ce que tous les abonnements soient supprimés.</span><span class="sxs-lookup"><span data-stu-id="2e110-135">For each disabled subscription, repeat steps 3 through 5 until all subscriptions are deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="2e110-136">Si vous ne parvenez pas à supprimer immédiatement un abonnement désactivé, <a href="https://go.microsoft.com/fwlink/p/?linkid=518322" target="_blank">Contactez le support technique</a> .</span><span class="sxs-lookup"><span data-stu-id="2e110-136">If you're unable to immediately delete a disabled subscription, <a href="https://go.microsoft.com/fwlink/p/?linkid=518322" target="_blank">contact support</a></span></span>

## <a name="step-4-disable-multi-factor-authentication"></a><span data-ttu-id="2e110-137">Étape 4 : désactivation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="2e110-137">Step 4: Disable multi-factor authentication</span></span>

1. <span data-ttu-id="2e110-138">Connectez-vous au centre d’administration à l’aide d’un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2e110-138">Sign in to the admin center with a Global administrator account.</span></span> <span data-ttu-id="2e110-139">Pour vérifier les rôles que vous avez, reportez-vous à [la rubrique vérifier les rôles d’administrateur dans votre organisation](../admin/add-users/assign-admin-roles.md#check-admin-roles-in-your-organization).</span><span class="sxs-lookup"><span data-stu-id="2e110-139">To verify what roles you have, see [Check admin roles in your organization](../admin/add-users/assign-admin-roles.md#check-admin-roles-in-your-organization).</span></span>
2. <span data-ttu-id="2e110-140">Accédez **à la**  >  page utilisateurs <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs</a> .</span><span class="sxs-lookup"><span data-stu-id="2e110-140">Go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
3. <span data-ttu-id="2e110-141">Choisissez **l’authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="2e110-141">Choose **Multi-factor authentication**.</span></span>
4. <span data-ttu-id="2e110-142">Sur la page authentification multifacteur, désactivez tous les comptes à l’exception du compte d’administrateur global que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="2e110-142">On the multi-factor authentication page, disable all accounts except for the global admin account that you're currently using.</span></span>

<span data-ttu-id="2e110-143">Vous pouvez également <a href="https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-userstates#change-state-using-powershell">Utiliser PowerShell pour désactiver l’authentification multifacteur pour plusieurs utilisateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="2e110-143">You can also <a href="https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-userstates#change-state-using-powershell">use PowerShell to disable multi-factor authentication for multiple users</a>.</span></span>

## <a name="step-5-delete-the-directory-in-azure-active-directory"></a><span data-ttu-id="2e110-144">Étape 5 : supprimer le répertoire dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2e110-144">Step 5: Delete the directory in Azure Active Directory</span></span>

1. <span data-ttu-id="2e110-145">Connectez-vous au <a href="https://aad.portal.azure.com/" target="_blank">Centre d’administration Azure ad</a> à l’aide d’un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2e110-145">Sign in to the <a href="https://aad.portal.azure.com/" target="_blank">Azure AD admin center</a> with a Global administrator account.</span></span>
2. <span data-ttu-id="2e110-146">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="2e110-146">Select **Azure Active Directory**.</span></span>
3. <span data-ttu-id="2e110-147">Basculez vers l’organisation que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="2e110-147">Switch to the organization that you want to delete.</span></span>
4. <span data-ttu-id="2e110-148">Sélectionnez **supprimer le client**.</span><span class="sxs-lookup"><span data-stu-id="2e110-148">Select **Delete tenant**.</span></span>
5. <span data-ttu-id="2e110-149">Si votre organisation ne parvient pas à effectuer une ou plusieurs vérifications, un lien vers plus d’informations sur la façon de réussir les vérifications s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2e110-149">If your organization fails one or more checks, you see a link to more information on how to pass the checks.</span></span> <span data-ttu-id="2e110-150">Après avoir passé tous les contrôles, sélectionnez **supprimer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="2e110-150">After you pass all checks, select **Delete** to complete the process.</span></span>

<span data-ttu-id="2e110-151">Une fois cette étape terminée, votre compte auprès de Microsoft est fermé et supprimé.</span><span class="sxs-lookup"><span data-stu-id="2e110-151">After you complete this final step, your account with Microsoft is closed and deleted.</span></span>