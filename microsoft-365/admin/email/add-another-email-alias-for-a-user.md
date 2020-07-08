---
title: Ajouter un autre alias de courrier pour un utilisateur
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
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
- MSStore_Link
- okr_smb
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0b0bd900-68b1-4bf5-808b-5d240a7739f4
description: 'Découvrez comment vous pouvez avoir plusieurs adresses de messagerie, appelées alias de messagerie, associées à votre compte Microsoft 365 pour les entreprises. '
ms.openlocfilehash: 030d8022a8503f6b383d03b0dd97720f66d8f2f6
ms.sourcegitcommit: 5b769f74bcc76ac8d38aad815d1728824783cd9f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080014"
---
# <a name="add-another-email-alias-for-a-user"></a><span data-ttu-id="534b3-103">Ajouter un autre alias de courrier pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="534b3-103">Add another email alias for a user</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="534b3-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="534b3-104">The admin center is changing.</span></span> <span data-ttu-id="534b3-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="534b3-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end
  
<span data-ttu-id="534b3-106">Cet article est destiné aux administrateurs de Microsoft 365 qui ont des abonnements d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="534b3-106">This article is for Microsoft 365 administrators who have business subscriptions.</span></span> <span data-ttu-id="534b3-107">Il ne s'adresse pas aux particuliers.</span><span class="sxs-lookup"><span data-stu-id="534b3-107">It's not for home users.</span></span>
  
<span data-ttu-id="534b3-108">Une adresse de messagerie principale dans Microsoft 365 correspond généralement à l’adresse de messagerie à laquelle un utilisateur a été affecté lors de la création de son compte.</span><span class="sxs-lookup"><span data-stu-id="534b3-108">A primary email address in Microsoft 365 is usually the email address a user was assigned when their account was created.</span></span> <span data-ttu-id="534b3-109">Lorsque l'utilisateur envoie du courrier à une autre personne, son adresse de courrier principale est celle qui apparaît généralement dans le champ  *De*  dans les applications de courrier.</span><span class="sxs-lookup"><span data-stu-id="534b3-109">When the user sends email to someone else, their primary email address is what typically appears in the  *From*  field in email apps.</span></span> <span data-ttu-id="534b3-110">Ils peuvent également avoir plus d’une adresse de messagerie associée à leur compte Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="534b3-110">They can also have more than one email address associated with their Microsoft 365 for business account.</span></span> <span data-ttu-id="534b3-111">Les adresses supplémentaires sont appelées alias.</span><span class="sxs-lookup"><span data-stu-id="534b3-111">These additional addresses are called aliases.</span></span> 
  
<span data-ttu-id="534b3-112">Par exemple, supposons que Jenna a l’adresse de messagerie jenna@contosoco.com, mais qu’il souhaite également recevoir des courriers électroniques sur jen@contosoco.com car certaines personnes y font référence par ce nom.</span><span class="sxs-lookup"><span data-stu-id="534b3-112">For example, let's say Jenna has the email address jenna@contosoco.com, but she also wants to receive email at jen@contosoco.com because some people refer to her by that name.</span></span> <span data-ttu-id="534b3-113">Vous pouvez créer des alias pour lui afin que les deux adresses de messagerie soient placées dans la boîte de réception de Jenna.</span><span class="sxs-lookup"><span data-stu-id="534b3-113">You can create aliases for her so that both email addresses go to Jenna's inbox.</span></span>
<br><br>  
  
<span data-ttu-id="534b3-114">Vous pouvez créer jusqu'à 400 alias par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="534b3-114">You can create up to 400 aliases for a user.</span></span> <span data-ttu-id="534b3-115">Vous ne devez pas acquérir de licence supplémentaire et cela n'occasionne aucun frais.</span><span class="sxs-lookup"><span data-stu-id="534b3-115">No additional fees or licenses are required.</span></span>
  
> [!Tip]
> <span data-ttu-id="534b3-116">Si vous souhaitez que plusieurs personnes gèrent les courriers électroniques envoyés à une adresse de messagerie unique telle que info@NodPublishers.com ou sales@NodPublishers.com, créez une boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="534b3-116">If you want multiple people to manage email sent to a single email address like info@NodPublishers.com or sales@NodPublishers.com, create a shared mailbox.</span></span> <span data-ttu-id="534b3-117">Pour en savoir plus, consultez [la rubrique créer une boîte aux lettres partagée](create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="534b3-117">To learn more, see [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>
  
## <a name="add-email-aliases-to-a-user"></a><span data-ttu-id="534b3-118">Ajouter des alias de courrier à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="534b3-118">Add email aliases to a user</span></span>
<span data-ttu-id="534b3-119"><a name="AddEmailPreview"> </a></span><span class="sxs-lookup"><span data-stu-id="534b3-119"><a name="AddEmailPreview"> </a></span></span>

<span data-ttu-id="534b3-120">Pour ce faire, vous devez disposer des [autorisations d’administrateur](../add-users/about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="534b3-120">You must have [admin permissions](../add-users/about-admin-roles.md) to do this.</span></span> 

  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="534b3-121">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="534b3-121">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="534b3-122">Sur la page **utilisateurs actifs** , sélectionnez l’utilisateur > **gérer les alias de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="534b3-122">On the **Active Users** page, select the user > **Manage email aliases**.</span></span> <span data-ttu-id="534b3-123">Cette option ne s’affiche pas si la personne ne dispose pas d’une licence.</span><span class="sxs-lookup"><span data-stu-id="534b3-123">You won't see this option if the person doesn't have a license assigned to them.</span></span> 
    
3. <span data-ttu-id="534b3-124">Sélectionnez **+ Ajouter un alias** et entrez un nouvel alias pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="534b3-124">Select **+ Add an alias** and enter a new alias for the user.</span></span>   
    
    > [!Important] 
    > <span data-ttu-id="534b3-125">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="534b3-125">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="534b3-126">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="534b3-126">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="534b3-127">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="534b3-127">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="534b3-128">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="534b3-128">If the problem persists, call Support and they will do a full sync for you.</span></span>
    
  
    > [!IMPORTANT]
    > <span data-ttu-id="534b3-129">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="534b3-129">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="534b3-130">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="534b3-130">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="534b3-131">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span><span class="sxs-lookup"><span data-stu-id="534b3-131">To add another domain name to the list, see [Add a domain to Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span></span> 
  
     
5. <span data-ttu-id="534b3-132">Lorsque vous avez fini, choisissez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="534b3-132">When you're done, choose **Save changes**.</span></span>
    
6. <span data-ttu-id="534b3-133">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="534b3-133">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span>
    
    <span data-ttu-id="534b3-134">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="534b3-134">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="534b3-135">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-135">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="534b3-136">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="534b3-136">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="534b3-137">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-137">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="534b3-138">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="534b3-138">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"
    
1. <span data-ttu-id="534b3-139">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="534b3-139">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
    
2. <span data-ttu-id="534b3-140">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="534b3-140">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="534b3-141">En regard de **nom d’utilisateur/alias de messagerie**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="534b3-141">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="534b3-142">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="534b3-142">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="534b3-143">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="534b3-143">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="534b3-144">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="534b3-144">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="534b3-145">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="534b3-145">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="534b3-146">Dans la zone de texte sous **alias**, tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="534b3-146">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="534b3-147">Si vous avez ajouté votre propre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias de messagerie dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="534b3-147">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="534b3-148">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="534b3-148">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="534b3-149">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="534b3-149">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="534b3-150">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="534b3-150">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="534b3-151">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span><span class="sxs-lookup"><span data-stu-id="534b3-151">To add another domain name to the list, see [Add a domain to Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span></span> 

5. <span data-ttu-id="534b3-152">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="534b3-152">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="534b3-153">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="534b3-153">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="534b3-154">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="534b3-154">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="534b3-155">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-155">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="534b3-156">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="534b3-156">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="534b3-157">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-157">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="534b3-158">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="534b3-158">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="534b3-159">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="534b3-159">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

    
2. <span data-ttu-id="534b3-160">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="534b3-160">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="534b3-161">En regard de **nom d’utilisateur/alias de messagerie**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="534b3-161">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="534b3-162">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="534b3-162">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="534b3-163">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="534b3-163">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="534b3-164">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="534b3-164">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="534b3-165">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="534b3-165">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="534b3-166">Dans la zone de texte sous **alias**, tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="534b3-166">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="534b3-167">Si vous avez ajouté votre propre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias de messagerie dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="534b3-167">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="534b3-168">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="534b3-168">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="534b3-169">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="534b3-169">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="534b3-170">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="534b3-170">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="534b3-171">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span><span class="sxs-lookup"><span data-stu-id="534b3-171">To add another domain name to the list, see [Add a domain to Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain).</span></span> 

5. <span data-ttu-id="534b3-172">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="534b3-172">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="534b3-173">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="534b3-173">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="534b3-174">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="534b3-174">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="534b3-175">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-175">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="534b3-176">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="534b3-176">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="534b3-177">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="534b3-177">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="534b3-178">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="534b3-178">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end


## <a name="did-you-get-a-parameter-cannot-be-found-that-matches-parameter-name-emailaddresses"></a><span data-ttu-id="534b3-179">Est-ce que vous obtenez « impossible de trouver un paramètre correspondant au nom de paramètre EmailAddresses » ?</span><span class="sxs-lookup"><span data-stu-id="534b3-179">Did you get "A parameter cannot be found that matches parameter name EmailAddresses"?</span></span>


<span data-ttu-id="534b3-180">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre EmailAddresses**» cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="534b3-180">If you get the error message "**A parameter cannot be found that matches parameter name EmailAddresses**" it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="534b3-181">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="534b3-181">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="534b3-182">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="534b3-182">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="534b3-183">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="534b3-183">If the problem persists, call Support and they will do a full sync for you.</span></span>
  
## <a name="did-you-purchase-your-subscription-from-godaddy-or-another-partner"></a><span data-ttu-id="534b3-184">Avez-vous acheté votre abonnement auprès de GoDaddy ou d'un autre partenaire ?</span><span class="sxs-lookup"><span data-stu-id="534b3-184">Did you purchase your subscription from GoDaddy or another Partner?</span></span>


<span data-ttu-id="534b3-185">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="534b3-185">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="534b3-186">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="534b3-186">Related articles</span></span>

[<span data-ttu-id="534b3-187">Envoyer des courriers à partir d'une adresse différente</span><span class="sxs-lookup"><span data-stu-id="534b3-187">Send email from a different address</span></span>](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e)

[<span data-ttu-id="534b3-188">Modifier un nom d'utilisateur et une adresse de courrier</span><span class="sxs-lookup"><span data-stu-id="534b3-188">Change a user name and email address</span></span>](../add-users/change-a-user-name-and-email-address.md)
  

