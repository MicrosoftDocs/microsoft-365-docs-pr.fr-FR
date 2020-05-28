---
title: Supprimer un domaine
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- Adm_O365_Setup
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: f09696b2-8c29-4588-a08b-b333da19810c
description: Découvrez comment supprimer un ancien domaine de Microsoft 365 et déplacer des utilisateurs et des groupes vers un autre domaine.
ms.openlocfilehash: c5e629f0d683c6dc3e18b1278027ac3a88cc834b
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44399895"
---
# <a name="remove-a-domain"></a><span data-ttu-id="a2f06-103">Supprimer un domaine</span><span class="sxs-lookup"><span data-stu-id="a2f06-103">Remove a domain</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="a2f06-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="a2f06-104">The admin center is changing.</span></span> <span data-ttu-id="a2f06-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="a2f06-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end
  
 <span data-ttu-id="a2f06-106">**[Consultez les Forums aux questions sur les domaines](../setup/domains-faq.md)** si vous ne trouvez pas ce que vous recherchez.</span><span class="sxs-lookup"><span data-stu-id="a2f06-106">**[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for.</span></span> 
  
<span data-ttu-id="a2f06-107">Êtes-vous en train de supprimer votre domaine car vous souhaitez l’ajouter à un autre plan d’abonnement Microsoft 365 ?</span><span class="sxs-lookup"><span data-stu-id="a2f06-107">Are you removing your domain because you want to add it to a different Microsoft 365 subscription plan?</span></span> <span data-ttu-id="a2f06-108">Ou souhaitez-vous annuler votre abonnement ?</span><span class="sxs-lookup"><span data-stu-id="a2f06-108">Or do you just want to cancel your subscription?</span></span> <span data-ttu-id="a2f06-109">Vous pouvez [modifier votre plan ou abonnement](../../commerce/subscriptions/switch-to-a-different-plan.md) ou [annuler votre abonnement](../../commerce/subscriptions/cancel-your-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a2f06-109">You can [change your plan or subscription](../../commerce/subscriptions/switch-to-a-different-plan.md) or [cancel your subscription](../../commerce/subscriptions/cancel-your-subscription.md).</span></span>
  
### <a name="step-1-move-users-to-another-domain"></a><span data-ttu-id="a2f06-110">Étape 1 : déplacer des utilisateurs vers un autre domaine</span><span class="sxs-lookup"><span data-stu-id="a2f06-110">Step 1: Move users to another domain</span></span>

#### <a name="move-users"></a><span data-ttu-id="a2f06-111">Déplacer des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a2f06-111">Move users</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a2f06-112">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a2f06-112">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="a2f06-113">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration</a>.</span><span class="sxs-lookup"><span data-stu-id="a2f06-113">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a>.</span></span>

2. <span data-ttu-id="a2f06-114">Sélectionnez **utilisateurs** > **actifs**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-114">Select **Users** > **Active users**.</span></span>

3. <span data-ttu-id="a2f06-115">Activez les cases à cocher en regard des noms de tous les utilisateurs que vous souhaitez déplacer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-115">Select the boxes next to the names of all the users you want to move.</span></span>

4. <span data-ttu-id="a2f06-116">Sélectionnez **plus d’options** (**...**), en haut de la page, puis choisissez **modifier les domaines**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-116">Select **More options** (**…**), at the top of the page, and then choose **Change domains**.</span></span>

5. <span data-ttu-id="a2f06-117">Dans le volet **modifier les domaines** , sélectionnez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-117">In the **Change domains** pane, select a different domain.</span></span>

<span data-ttu-id="a2f06-p103">Vous devrez également effectuer cette action pour vous-même si vous êtes sur le domaine que vous souhaitez supprimer. Lorsque vous modifiez le domaine de votre compte, vous devez vous déconnecter puis vous reconnecter en utilisant le nouveau domaine que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="a2f06-p103">You'll need to do this for yourself, too, if you're on the domain that you want to remove. When you edit the domain for your account, you'll have to log out and log back in using the new domain you chose to continue.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="a2f06-120">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>.</span><span class="sxs-lookup"><span data-stu-id="a2f06-120">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>.</span></span>  

2. <span data-ttu-id="a2f06-121">Sélectionnez **utilisateurs** > **actifs**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-121">Select **Users** > **Active users**.</span></span>

3. <span data-ttu-id="a2f06-122">Activez les cases à cocher en regard des noms de tous les utilisateurs que vous souhaitez déplacer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-122">Select the boxes next to the names of all the users you want to move.</span></span>

4. <span data-ttu-id="a2f06-123">En haut de la page, choisissez **plus** > **modifier les domaines**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-123">At the top of the page, choose **More** > **Edit domains**.</span></span>

5. <span data-ttu-id="a2f06-124">Dans le volet **modifier les domaines** , sélectionnez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-124">In the **Edit domains** pane, select a different domain.</span></span>
  
<span data-ttu-id="a2f06-p104">Vous devrez également effectuer cette action pour vous-même si vous êtes sur le domaine que vous souhaitez supprimer. Lorsque vous modifiez le domaine de votre compte, vous devez vous déconnecter puis vous reconnecter en utilisant le nouveau domaine que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="a2f06-p104">You'll need to do this for yourself, too, if you're on the domain that you want to remove. When you edit the domain for your account, you'll have to log out and log back in using the new domain you chose to continue.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a2f06-127">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>.</span><span class="sxs-lookup"><span data-stu-id="a2f06-127">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>.</span></span>  

2. <span data-ttu-id="a2f06-128">Sélectionnez **utilisateurs** > **actifs**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-128">Select **Users** > **Active users**.</span></span>

3. <span data-ttu-id="a2f06-129">Activez les cases à cocher en regard des noms de tous les utilisateurs que vous souhaitez déplacer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-129">Select the boxes next to the names of all the users you want to move.</span></span>

4. <span data-ttu-id="a2f06-130">En haut de la page, choisissez **plus** > **modifier les domaines**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-130">At the top of the page, choose **More** > **Edit domains**.</span></span>

5. <span data-ttu-id="a2f06-131">Dans le volet **modifier les domaines** , sélectionnez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-131">In the **Edit domains** pane, select a different domain.</span></span>
  
<span data-ttu-id="a2f06-p105">Vous devrez également effectuer cette action pour vous-même si vous êtes sur le domaine que vous souhaitez supprimer. Lorsque vous modifiez le domaine de votre compte, vous devez vous déconnecter puis vous reconnecter en utilisant le nouveau domaine que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="a2f06-p105">You'll need to do this for yourself, too, if you're on the domain that you want to remove. When you edit the domain for your account, you'll have to log out and log back in using the new domain you chose to continue.</span></span>

::: moniker-end

#### <a name="move-yourself"></a><span data-ttu-id="a2f06-134">Vous déplacer</span><span class="sxs-lookup"><span data-stu-id="a2f06-134">Move yourself</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a2f06-135">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a2f06-135">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="a2f06-136">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>.</span><span class="sxs-lookup"><span data-stu-id="a2f06-136">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>.</span></span>

2. <span data-ttu-id="a2f06-137">Accédez à **utilisateurs** \> **actifs**, puis sélectionnez votre compte dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a2f06-137">Go to **Users** \> **Active Users**, and select your account from the list.</span></span>

3. <span data-ttu-id="a2f06-138">Dans l’onglet **compte** , sélectionnez **gérer le nom d’utilisateur**, puis choisissez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-138">On the **Account** tab, select **Manage username**, and then choose a different domain.</span></span>
  
4. <span data-ttu-id="a2f06-139">Dans la partie supérieure, sélectionnez le nom de votre compte, puis **déconnectez-vous**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-139">At the top, select your account name, then select **Sign Out**.</span></span>

5. <span data-ttu-id="a2f06-140">Connectez-vous avec le nouveau domaine et le même mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a2f06-140">Sign in with the new domain and your same password.</span></span>

<span data-ttu-id="a2f06-141">Vous pouvez également utiliser PowerShell pour déplacer des utilisateurs vers un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-141">You can also use PowerShell to move users to another domain.</span></span> <span data-ttu-id="a2f06-142">Pour des informations supplémentaires, voir [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-142">See [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) for more information.</span></span> <span data-ttu-id="a2f06-143">Pour définir le domaine par défaut, utilisez [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-143">To set the default domain, use [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="a2f06-144">Accédez à **utilisateurs** \> **actifs**, puis sélectionnez votre nom dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a2f06-144">Go to **Users** \> **Active Users**, and select your name in the list.</span></span>

2. <span data-ttu-id="a2f06-145">Dans la section **nom d’utilisateur/adresse de messagerie** , sélectionnez **modifier**, puis choisissez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-145">In the **Username / Email** section, select **Edit**, and then choose a different domain.</span></span>

3. <span data-ttu-id="a2f06-146">Sélectionnez **définir comme** > **enregistrement** principal- > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-146">Select **Set as primary** > **Save** > **Close**.</span></span>
  
4. <span data-ttu-id="a2f06-147">Dans la partie supérieure, sélectionnez le nom de votre compte, puis **déconnectez-vous**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-147">At the top, select your account name, then select **Sign Out**.</span></span>

5. <span data-ttu-id="a2f06-148">Connectez-vous avec le nouveau domaine et le même mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a2f06-148">Sign in with the new domain and your same password.</span></span>

<span data-ttu-id="a2f06-149">Vous pouvez également utiliser PowerShell pour déplacer des utilisateurs vers un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-149">You can also use PowerShell to move users to another domain.</span></span> <span data-ttu-id="a2f06-150">Pour des informations supplémentaires, voir [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-150">See [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) for more information.</span></span> <span data-ttu-id="a2f06-151">Pour définir le domaine par défaut, utilisez [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-151">To set the default domain, use [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a2f06-152">Accédez à **utilisateurs** \> **actifs**, puis sélectionnez votre nom dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a2f06-152">Go to **Users** \> **Active Users**, and select your name in the list.</span></span>

2. <span data-ttu-id="a2f06-153">Dans la section **nom d’utilisateur/adresse de messagerie** , sélectionnez **modifier**, puis choisissez un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-153">In the **Username / Email** section, select **Edit**, and then choose a different domain.</span></span>

3. <span data-ttu-id="a2f06-154">Sélectionnez **définir comme** > **enregistrement** principal- > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-154">Select **Set as primary** > **Save** > **Close**.</span></span>
  
4. <span data-ttu-id="a2f06-155">Dans la partie supérieure, sélectionnez le nom de votre compte, puis **déconnectez-vous**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-155">At the top, select your account name, then select **Sign Out**.</span></span>

5. <span data-ttu-id="a2f06-156">Connectez-vous avec le nouveau domaine et le même mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a2f06-156">Sign in with the new domain and your same password.</span></span>

<span data-ttu-id="a2f06-157">Vous pouvez également utiliser PowerShell pour déplacer des utilisateurs vers un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-157">You can also use PowerShell to move users to another domain.</span></span> <span data-ttu-id="a2f06-158">Pour des informations supplémentaires, voir [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-158">See [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) for more information.</span></span> <span data-ttu-id="a2f06-159">Pour définir le domaine par défaut, utilisez [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-159">To set the default domain, use [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span></span>

::: moniker-end

### <a name="step-2-move-groups-to-another-domain"></a><span data-ttu-id="a2f06-160">Étape 2 : déplacer des groupes vers un autre domaine</span><span class="sxs-lookup"><span data-stu-id="a2f06-160">Step 2: Move groups to another domain</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="a2f06-161">Dans le centre d’administration, accédez à **la page groupes de** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">groupes</a> .</span><span class="sxs-lookup"><span data-stu-id="a2f06-161">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2052855" target="_blank">Groups</a> page.</span></span>
  
2. <span data-ttu-id="a2f06-162">Sélectionnez le nom du groupe, puis sous l’onglet **général** , sous **adresse de messagerie, principal**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-162">Select the group name, and then on the **General** tab under **Email address, Primary**, select **Edit**.</span></span>

3. <span data-ttu-id="a2f06-163">Utilisez la liste déroulante pour choisir un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-163">Use the drop-down list to choose another domain.</span></span>

4. <span data-ttu-id="a2f06-164">Sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-164">Select **Save**, then **Close**.</span></span> <span data-ttu-id="a2f06-165">Répétez cette procédure pour les groupes ou listes de distribution associés au domaine que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-165">Repeat this process for any groups or distribution lists associated with the domain that you want to remove.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="a2f06-166">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à **la page groupes de** > **groupes** .</span><span class="sxs-lookup"><span data-stu-id="a2f06-166">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>,  go to the **Groups** > **Groups** page.</span></span>

2. <span data-ttu-id="a2f06-167">Sélectionnez le nom du groupe, puis cliquez sur **modifier** en regard de **nom**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-167">Select the group name, and then select **Edit** next to **Name**.</span></span>

3. <span data-ttu-id="a2f06-168">Utilisez la liste déroulante pour choisir un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-168">Use the drop-down list to choose another domain.</span></span>

4. <span data-ttu-id="a2f06-169">Sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-169">Select **Save**, then **Close**.</span></span> <span data-ttu-id="a2f06-170">Répétez cette procédure pour les groupes ou listes de distribution associés au domaine que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-170">Repeat this process for any groups or distribution lists associated with the domain that you want to remove.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a2f06-171">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à **la page groupes de** > **groupes** .</span><span class="sxs-lookup"><span data-stu-id="a2f06-171">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>,  go to the **Groups** > **Groups** page.</span></span>

2. <span data-ttu-id="a2f06-172">Sélectionnez le nom du groupe, puis cliquez sur **modifier** en regard de **nom**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-172">Select the group name, and then select **Edit** next to **Name**.</span></span>

3. <span data-ttu-id="a2f06-173">Utilisez la liste déroulante pour choisir un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="a2f06-173">Use the drop-down list to choose another domain.</span></span>

4. <span data-ttu-id="a2f06-174">Sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-174">Select **Save**, then **Close**.</span></span> <span data-ttu-id="a2f06-175">Répétez cette procédure pour les groupes ou listes de distribution associés au domaine que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-175">Repeat this process for any groups or distribution lists associated with the domain that you want to remove.</span></span>

::: moniker-end

### <a name="step-3-remove-the-old-domain"></a><span data-ttu-id="a2f06-176">Étape 3 : supprimer l’ancien domaine</span><span class="sxs-lookup"><span data-stu-id="a2f06-176">Step 3: Remove the old domain</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="a2f06-177">Dans le centre d’administration, accédez à la page **Paramètres** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domaines</a>.</span><span class="sxs-lookup"><span data-stu-id="a2f06-177">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834818" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="a2f06-178">Dans le centre d’administration, accédez à la page domaines **d’installation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> .</span><span class="sxs-lookup"><span data-stu-id="a2f06-178">In the admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=854615" target="_blank">Domains</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a2f06-179">Dans le centre d’administration, accédez à la page domaines **d’installation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> .</span><span class="sxs-lookup"><span data-stu-id="a2f06-179">In the admin center, go to the **Setup** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2007048" target="_blank">Domains</a> page.</span></span>

::: moniker-end
  
2. <span data-ttu-id="a2f06-180">Dans la page **domaines** , sélectionnez le domaine que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2f06-180">On the **Domains** page, select the domain that you want to remove.</span></span>

3. <span data-ttu-id="a2f06-181">Dans le volet droit, sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-181">In the right pane, select **Remove**.</span></span>

4. <span data-ttu-id="a2f06-182">Suivez les invites supplémentaires, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a2f06-182">Follow any additional prompts, and then select **Close**.</span></span>

## <a name="how-long-does-it-take-for-a-domain-to-be-removed"></a><span data-ttu-id="a2f06-183">Combien de temps faut-il pour qu'un domaine soit supprimé ?</span><span class="sxs-lookup"><span data-stu-id="a2f06-183">How long does it take for a domain to be removed?</span></span>

<span data-ttu-id="a2f06-184">La suppression d’un domaine par Microsoft 365 peut prendre jusqu’à 5 minutes s’il n’est pas référencé dans de nombreux emplacements, tels que les groupes de sécurité, les listes de distribution, les utilisateurs et les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a2f06-184">It can take as little as 5 minutes for Microsoft 365 to remove a domain if it's not referenced in a lot of places such as security groups, distribution lists, users, and Microsoft 365 groups.</span></span> <span data-ttu-id="a2f06-185">Si plusieurs références utilisent le domaine, la suppression du domaine peut prendre plusieurs heures (une journée).</span><span class="sxs-lookup"><span data-stu-id="a2f06-185">If there are many references that use the domain it can take several hours (a day) for the domain to be removed.</span></span>
  
<span data-ttu-id="a2f06-p113">Si vous avez des centaines voire des milliers d'utilisateurs, utilisez PowerShell pour interroger tous les utilisateurs, puis déplacez-les vers un autre domaine. Sinon, il est possible que quelques-uns des utilisateurs manquent dans l'interface utilisateur. De plus, lorsque vous voudrez supprimer le domaine, vous ne pourrez pas et vous ne saurez pas pourquoi. Pour en savoir plus, voir [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0). Pour définir le domaine par défaut, utilisez [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span><span class="sxs-lookup"><span data-stu-id="a2f06-p113">If you have hundreds or thousands of users, use PowerShell to query for all users and then move them to another domain. Otherwise, it's possible for a handful of users to be missed in the UI, and then when you go to remove the domain, you won't be able to and you won't know why. See [Set-MsolUserPrincipalName](https://docs.microsoft.com/powershell/module/msonline/set-msoluserprincipalname?view=azureadps-1.0) for more information. To set the default domain, use [Set-MsolDomain](https://docs.microsoft.com/powershell/module/msonline/set-msoldomain?view=azureadps-1.0).</span></span>
  
## <a name="still-need-help"></a><span data-ttu-id="a2f06-190">Vous avez encore besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="a2f06-190">Still need help?</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a2f06-191">Vous ne pouvez pas supprimer le domaine [« onmicrosoft.com »](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq) de votre compte.</span><span class="sxs-lookup"><span data-stu-id="a2f06-191">You can't remove the [".onmicrosoft.com"](https://docs.microsoft.com/microsoft-365/admin/setup/domains-faq) domain from your account.</span></span>
  
<span data-ttu-id="a2f06-p114">Cela ne fonctionne toujours pas ? Vous devez peut-être supprimer votre domaine manuellement. [Appelez-nous](../contact-support-for-business-products.md) et nous vous aiderons à effectuer cette tâche.</span><span class="sxs-lookup"><span data-stu-id="a2f06-p114">Still not working? Your domain might need to be manually removed. [Give us a call](../contact-support-for-business-products.md) and we'll help you take care of it!</span></span>
  
::: moniker-end

## <a name="related-articles"></a><span data-ttu-id="a2f06-195">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a2f06-195">Related articles</span></span>

[<span data-ttu-id="a2f06-196">Foire aux questions domaines</span><span class="sxs-lookup"><span data-stu-id="a2f06-196">Domains FAQ</span></span>](../setup/domains-faq.md)

[<span data-ttu-id="a2f06-197">Obtenir de l’aide sur les domaines Office 365</span><span class="sxs-lookup"><span data-stu-id="a2f06-197">Get help with Office 365 domains</span></span>](get-help-with-domains.md)

[<span data-ttu-id="a2f06-198">Basculer vers une autre offre Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="a2f06-198">Switch to a different Microsoft 365 for business plan</span></span>](../../commerce/subscriptions/switch-to-a-different-plan.md)

[<span data-ttu-id="a2f06-199">Annuler votre abonnement</span><span class="sxs-lookup"><span data-stu-id="a2f06-199">Cancel your subscription</span></span>](../../commerce/subscriptions/cancel-your-subscription.md)
