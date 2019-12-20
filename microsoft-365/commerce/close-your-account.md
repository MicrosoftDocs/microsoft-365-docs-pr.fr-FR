---
title: Clôturer votre compte
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- commerce
ms.custom: ''
search.appverid:
- MET150
description: Découvrez comment fermer votre compte auprès de Microsoft.
ms.openlocfilehash: 905b3d1dfef44a6b1f78c5afe5f7673aec6b8894
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40809270"
---
# <a name="close-your-account"></a><span data-ttu-id="9707a-103">Clôturer votre compte</span><span class="sxs-lookup"><span data-stu-id="9707a-103">Close your account</span></span>

<span data-ttu-id="9707a-104">Lorsque vous fermez votre compte auprès de Microsoft, toutes les informations relatives à votre compte sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="9707a-104">When you close your account with Microsoft, all information related to your account is deleted.</span></span> <span data-ttu-id="9707a-105">Ces informations incluent les abonnements, les licences, les modes de paiement, les utilisateurs et les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9707a-105">This information includes subscriptions, licenses, payment methods, users, and user data.</span></span> <span data-ttu-id="9707a-106">Avant de commencer cette procédure, assurez-vous de sauvegarder toutes les données que vous souhaitez conserver.</span><span class="sxs-lookup"><span data-stu-id="9707a-106">Before you start this process, make sure to backup any data that you want to preserve.</span></span>

## <a name="step-1-delete-users"></a><span data-ttu-id="9707a-107">Étape 1 : supprimer des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9707a-107">Step 1: Delete users</span></span>

<span data-ttu-id="9707a-108">Supprimez tous les utilisateurs à l’exception d’un administrateur général qui termine les étapes de fermeture du compte.</span><span class="sxs-lookup"><span data-stu-id="9707a-108">Delete all users except for one global administrator who completes the steps to close the account.</span></span> <span data-ttu-id="9707a-109">Avant de pouvoir supprimer le répertoire à la fin de ce processus, vous devez supprimer tous les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9707a-109">Before you can delete the directory at the end of this process, you must delete all other users.</span></span>

<span data-ttu-id="9707a-110">Si les utilisateurs sont synchronisés en local, désactivez la synchronisation, puis supprimez les utilisateurs dans le répertoire Cloud à l’aide du portail Azure ou des applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9707a-110">If users are synchronized from on-premises, first turn off sync, then delete the users in the cloud directory by using the Azure portal or Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="9707a-111">Pour supprimer des utilisateurs, consultez la rubrique <a href="https://docs.microsoft.com/office365/admin/add-users/delete-a-user?view=o365-worldwide#user-management-admin-delete-one-or-more-users-from-office-365">administrateur de gestion des utilisateurs : supprimer un ou plusieurs utilisateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="9707a-111">To delete users, see <a href="https://docs.microsoft.com/office365/admin/add-users/delete-a-user?view=o365-worldwide#user-management-admin-delete-one-or-more-users-from-office-365">User management admin: Delete one or more users</a>.</span></span>

<span data-ttu-id="9707a-112">Vous pouvez également utiliser l’applet de commande PowerShell <a href="https://go.microsoft.com/fwlink/?linkid=842230">Remove-MsolUser</a> pour supprimer des utilisateurs en bloc.</span><span class="sxs-lookup"><span data-stu-id="9707a-112">You can also use the <a href="https://go.microsoft.com/fwlink/?linkid=842230">Remove-MsolUser</a> PowerShell cmdlet to delete users in bulk.</span></span>

<span data-ttu-id="9707a-113">Si votre organisation utilise Active Directory qui se synchronise avec Azure AD, supprimez le compte d’utilisateur d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9707a-113">If your organization uses Active Directory that synchronizes with Azure AD, delete the user account from Active Directory, instead.</span></span> <span data-ttu-id="9707a-114">Pour obtenir des instructions, consultez la rubrique <a href="https://docs.microsoft.com/azure/active-directory/users-groups-roles/users-bulk-delete">suppression en bloc d’utilisateurs dans Azure Active Directory</a>.</span><span class="sxs-lookup"><span data-stu-id="9707a-114">For instructions, see <a href="https://docs.microsoft.com/azure/active-directory/users-groups-roles/users-bulk-delete">Bulk delete users in Azure Active Directory</a>.</span></span>

## <a name="step-2-cancel-all-active-subscriptions"></a><span data-ttu-id="9707a-115">Étape 2 : annuler tous les abonnements actifs</span><span class="sxs-lookup"><span data-stu-id="9707a-115">Step 2: Cancel all active subscriptions</span></span>

1. <span data-ttu-id="9707a-116">Dans le centre d’administration, accédez à la page produits de **facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">& services</a> .</span><span class="sxs-lookup"><span data-stu-id="9707a-116">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.</span></span>

2. <span data-ttu-id="9707a-117">Si la liste abonnements est affichée en mode **table** , cliquez sur la droite sur **cartes**.</span><span class="sxs-lookup"><span data-stu-id="9707a-117">If the subscriptions list is in **Table** view, on the right, select **Cards**.</span></span>

3. <span data-ttu-id="9707a-118">Recherchez un abonnement actif et, dans la section **paramètres & Actions** , sélectionnez **Annuler l’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="9707a-118">Find an active subscription, and in the **Settings & Actions** section, select **Cancel subscription**.</span></span>

4. <span data-ttu-id="9707a-119">Suivez les invites pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="9707a-119">Follow the prompts to finish the process.</span></span>

5. <span data-ttu-id="9707a-120">Répétez les étapes 1 à 4 pour annuler tous les abonnements actifs.</span><span class="sxs-lookup"><span data-stu-id="9707a-120">Repeat steps 1 through 4 to cancel all active subscriptions.</span></span>

## <a name="step-3-delete-all-disabled-subscriptions"></a><span data-ttu-id="9707a-121">Étape 3 : supprimer tous les abonnements désactivés</span><span class="sxs-lookup"><span data-stu-id="9707a-121">Step 3: Delete all disabled subscriptions</span></span>

1. <span data-ttu-id="9707a-122">Dans le centre d’administration, accédez à la page produits de **facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">& services</a> .</span><span class="sxs-lookup"><span data-stu-id="9707a-122">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.</span></span>

2. <span data-ttu-id="9707a-123">Si la liste abonnements est affichée en mode **table** , cliquez sur la droite sur **cartes**.</span><span class="sxs-lookup"><span data-stu-id="9707a-123">If the subscriptions list is in **Table** view, on the right, select **Cards**.</span></span>

3. <span data-ttu-id="9707a-124">En regard de l’option État de l' **abonnement**, sélectionnez **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="9707a-124">Next to **Subscription status**, select **Disabled**.</span></span>

4. <span data-ttu-id="9707a-125">Recherchez un abonnement désactivé et, dans la section **paramètres & Actions** , sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9707a-125">Find a disabled subscription, and in the **Settings & Actions** section, select **Delete**.</span></span>

5. <span data-ttu-id="9707a-126">Dans la boîte de dialogue **supprimer un abonnement** , activez la case à cocher **j’ai assimilé le choc** , puis sélectionnez **supprimer un abonnement**.</span><span class="sxs-lookup"><span data-stu-id="9707a-126">In the **Delete subscription** dialog box, select the **I understand the impact** check box, then select **Delete subscription**.</span></span>

6. <span data-ttu-id="9707a-127">Pour chaque abonnement désactivé, répétez les étapes 4 et 5 jusqu’à ce que tous les abonnements aient été supprimés.</span><span class="sxs-lookup"><span data-stu-id="9707a-127">For each disabled subscription, repeat steps 4 and 5 until all subscriptions have been deleted.</span></span>

## <a name="step-4-disable-multi-factor-authentication"></a><span data-ttu-id="9707a-128">Étape 4 : désactivation de l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="9707a-128">Step 4: Disable multi-factor authentication</span></span>

1. <span data-ttu-id="9707a-129">Dans le centre d’administration, accédez à **la** > page utilisateurs<a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">actifs</a> .</span><span class="sxs-lookup"><span data-stu-id="9707a-129">In the admin center, go to the **Users** > <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="9707a-130">Choisissez **l’authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="9707a-130">Choose **Multi-factor authentication**.</span></span>

3. <span data-ttu-id="9707a-131">Sur la page authentification multifacteur, désactivez tous les comptes à l’exception du compte d’administrateur global que vous utilisez actuellement.</span><span class="sxs-lookup"><span data-stu-id="9707a-131">On the multi-factor authentication page, disable all accounts except for the global admin account that you’re currently using.</span></span>

<span data-ttu-id="9707a-132">Vous pouvez également <a href="https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-userstates#use-powershell">Utiliser PowerShell pour désactiver l’authentification multifacteur pour plusieurs utilisateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="9707a-132">You can also <a href="https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-userstates#use-powershell">use PowerShell to disable multi-factor authentication for multiple users</a>.</span></span>

## <a name="step-5-delete-the-directory-in-azure-active-directory"></a><span data-ttu-id="9707a-133">Étape 5 : supprimer le répertoire dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9707a-133">Step 5: Delete the directory in Azure Active Directory</span></span>

1. <span data-ttu-id="9707a-134">Connectez-vous au <a href="https://aad.portal.azure.com/" target="_blank">Centre d’administration Azure ad</a> à l’aide d’un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="9707a-134">Sign in to the <a href="https://aad.portal.azure.com/" target="_blank">Azure AD admin center</a> with a Global Administrator account.</span></span>

2. <span data-ttu-id="9707a-135">Sélectionner **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9707a-135">Select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="9707a-136">Basculez vers le répertoire que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="9707a-136">Switch to the directory you want to delete.</span></span>

4. <span data-ttu-id="9707a-137">Sélectionnez **supprimer un répertoire**.</span><span class="sxs-lookup"><span data-stu-id="9707a-137">Select **Delete directory**.</span></span>

5. <span data-ttu-id="9707a-138">Si votre annuaire ne parvient pas à effectuer une ou plusieurs vérifications, un lien vers plus d’informations sur la façon de réussir les vérifications s’affiche.</span><span class="sxs-lookup"><span data-stu-id="9707a-138">If your directory fails one or more checks, you see a link to more information on how to pass the checks.</span></span> <span data-ttu-id="9707a-139">Après avoir passé tous les contrôles, sélectionnez **supprimer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="9707a-139">After you pass all checks, select **Delete** to complete the process.</span></span>

<span data-ttu-id="9707a-140">Une fois cette étape terminée, votre compte auprès de Microsoft est fermé et supprimé.</span><span class="sxs-lookup"><span data-stu-id="9707a-140">After you complete this final step, your account with Microsoft is closed and deleted.</span></span>