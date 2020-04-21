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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0b0bd900-68b1-4bf5-808b-5d240a7739f4
description: 'Découvrez comment vous pouvez avoir plusieurs adresses de messagerie, appelées alias de messagerie, associées à votre compte Microsoft 365 pour les entreprises. '
ms.openlocfilehash: 66ff2441c95ed28b2072792fd0a63b16eea85c04
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43629082"
---
# <a name="add-another-email-alias-for-a-user"></a><span data-ttu-id="c8aad-103">Ajouter un autre alias de courrier pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8aad-103">Add another email alias for a user</span></span>
  
<span data-ttu-id="c8aad-104">Cet article est destiné aux administrateurs de Microsoft 365 qui ont des abonnements d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c8aad-104">This article is for Microsoft 365 administrators who have business subscriptions.</span></span> <span data-ttu-id="c8aad-105">Il ne s'adresse pas aux particuliers.</span><span class="sxs-lookup"><span data-stu-id="c8aad-105">It's not for home users.</span></span>
  
<span data-ttu-id="c8aad-106">Une adresse de messagerie principale dans Microsoft 365 correspond généralement à l’adresse de messagerie à laquelle un utilisateur a été affecté lors de la création de son compte.</span><span class="sxs-lookup"><span data-stu-id="c8aad-106">A primary email address in Microsoft 365 is usually the email address a user was assigned when their account was created.</span></span> <span data-ttu-id="c8aad-107">Lorsque l'utilisateur envoie du courrier à une autre personne, son adresse de courrier principale est celle qui apparaît généralement dans le champ  *De*  dans les applications de courrier.</span><span class="sxs-lookup"><span data-stu-id="c8aad-107">When the user sends email to someone else, their primary email address is what typically appears in the  *From*  field in email apps.</span></span> <span data-ttu-id="c8aad-108">Ils peuvent également avoir plus d’une adresse de messagerie associée à leur compte Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="c8aad-108">They can also have more than one email address associated with their Microsoft 365 for business account.</span></span> <span data-ttu-id="c8aad-109">Les adresses supplémentaires sont appelées alias.</span><span class="sxs-lookup"><span data-stu-id="c8aad-109">These additional addresses are called aliases.</span></span> 
  
<span data-ttu-id="c8aad-110">Par exemple, supposons que Jenna a l’adresse de messagerie jenna@contosoco.com, mais qu’il souhaite également recevoir des courriers électroniques sur jen@contosoco.com car certaines personnes y font référence par ce nom.</span><span class="sxs-lookup"><span data-stu-id="c8aad-110">For example, let's say Jenna has the email address jenna@contosoco.com, but she also wants to receive email at jen@contosoco.com because some people refer to her by that name.</span></span> <span data-ttu-id="c8aad-111">Vous pouvez créer des alias pour lui afin que les deux adresses de messagerie soient placées dans la boîte de réception de Jenna.</span><span class="sxs-lookup"><span data-stu-id="c8aad-111">You can create aliases for her so that both email addresses go to Jenna's inbox.</span></span>
<br><br>  
  
<span data-ttu-id="c8aad-112">Vous pouvez créer jusqu'à 400 alias par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8aad-112">You can create up to 400 aliases for a user.</span></span> <span data-ttu-id="c8aad-113">Vous ne devez pas acquérir de licence supplémentaire et cela n'occasionne aucun frais.</span><span class="sxs-lookup"><span data-stu-id="c8aad-113">No additional fees or licenses are required.</span></span>
  
> [!Tip]
> <span data-ttu-id="c8aad-114">Si vous souhaitez que plusieurs personnes gèrent les courriers électroniques envoyés à une adresse de messagerie unique telle que info@NodPublishers.com ou sales@NodPublishers.com, créez une boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="c8aad-114">If you want multiple people to manage email sent to a single email address like info@NodPublishers.com or sales@NodPublishers.com, create a shared mailbox.</span></span> <span data-ttu-id="c8aad-115">Pour en savoir plus, consultez [la rubrique créer une boîte aux lettres partagée](create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="c8aad-115">To learn more, see [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>
  
## <a name="add-email-aliases-to-a-user"></a><span data-ttu-id="c8aad-116">Ajouter des alias de courrier à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8aad-116">Add email aliases to a user</span></span>
<span data-ttu-id="c8aad-117"><a name="AddEmailPreview"> </a></span><span class="sxs-lookup"><span data-stu-id="c8aad-117"><a name="AddEmailPreview"> </a></span></span>

<span data-ttu-id="c8aad-118">Pour ce faire, vous devez disposer des [autorisations d’administrateur](../add-users/about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="c8aad-118">You must have [admin permissions](../add-users/about-admin-roles.md) to do this.</span></span> 

  
::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="c8aad-119">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="c8aad-119">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="c8aad-120">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="c8aad-120">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="c8aad-121">Sur la page **utilisateurs actifs** , sélectionnez l’utilisateur > **gérer les alias de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-121">On the **Active Users** page, select the user > **Manage email aliases**.</span></span> <span data-ttu-id="c8aad-122">Cette option ne s’affiche pas si la personne ne dispose pas d’une licence.</span><span class="sxs-lookup"><span data-stu-id="c8aad-122">You won't see this option if the person doesn't have a license assigned to them.</span></span> 
    
3. <span data-ttu-id="c8aad-123">Sélectionnez **+ Ajouter un alias** et entrez un nouvel alias pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8aad-123">Select **+ Add an alias** and enter a new alias for the user.</span></span>   
    
    > [!Important] 
    > <span data-ttu-id="c8aad-124">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="c8aad-124">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="c8aad-125">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="c8aad-125">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="c8aad-126">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="c8aad-126">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="c8aad-127">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="c8aad-127">If the problem persists, call Support and they will do a full sync for you.</span></span>
    
  
    > [!IMPORTANT]
    > <span data-ttu-id="c8aad-128">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="c8aad-128">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="c8aad-129">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c8aad-129">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="c8aad-130">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8aad-130">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 
  
     
5. <span data-ttu-id="c8aad-131">Lorsque vous avez fini, choisissez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-131">When you're done, choose **Save changes**.</span></span>
    
6. <span data-ttu-id="c8aad-132">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8aad-132">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span>
    
    <span data-ttu-id="c8aad-133">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="c8aad-133">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="c8aad-134">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-134">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="c8aad-135">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="c8aad-135">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="c8aad-136">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-136">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="c8aad-137">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="c8aad-137">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"
    
1. <span data-ttu-id="c8aad-138">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="c8aad-138">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
    
2. <span data-ttu-id="c8aad-139">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="c8aad-139">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="c8aad-140">En regard de **nom d’utilisateur/alias de messagerie**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-140">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="c8aad-141">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="c8aad-141">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="c8aad-142">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="c8aad-142">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="c8aad-143">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="c8aad-143">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="c8aad-144">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="c8aad-144">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="c8aad-145">Dans la zone de texte sous **alias**, tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8aad-145">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="c8aad-146">Si vous avez ajouté votre domaine à Office 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c8aad-146">If you added your own domain to Office 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="c8aad-147">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-147">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c8aad-148">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="c8aad-148">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="c8aad-149">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c8aad-149">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="c8aad-150">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8aad-150">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 

5. <span data-ttu-id="c8aad-151">Lorsque vous avez fini, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-151">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="c8aad-152">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8aad-152">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span> 
    
    <span data-ttu-id="c8aad-153">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="c8aad-153">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="c8aad-154">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-154">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="c8aad-155">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="c8aad-155">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="c8aad-156">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-156">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="c8aad-157">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="c8aad-157">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="c8aad-158">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="c8aad-158">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

    
2. <span data-ttu-id="c8aad-159">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="c8aad-159">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="c8aad-160">En regard de **nom d’utilisateur/alias de messagerie**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-160">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="c8aad-161">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre «EmailAddresses**», cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="c8aad-161">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="c8aad-162">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="c8aad-162">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="c8aad-163">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="c8aad-163">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="c8aad-164">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="c8aad-164">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="c8aad-165">Dans la zone de texte sous **alias**, tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c8aad-165">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="c8aad-166">Si vous avez ajouté votre domaine à Office 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c8aad-166">If you added your own domain to Office 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="c8aad-167">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-167">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c8aad-168">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="c8aad-168">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="c8aad-169">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c8aad-169">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="c8aad-170">Pour ajouter un autre nom de domaine à la liste, reportez-vous à la rubrique [Ajouter un domaine à Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8aad-170">To add another domain name to the list, see [Add a domain to Office 365](https://support.office.com/article/2d2fa996-b760-411d-a5cc-190d63f13207.aspx).</span></span> 

5. <span data-ttu-id="c8aad-171">Lorsque vous avez fini, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="c8aad-171">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="c8aad-172">Patientez 24 heures pour que les nouveaux alias soient renseignés dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8aad-172">Wait 24 hours for the new aliases to populate throughout Office 365.</span></span> 
    
    <span data-ttu-id="c8aad-173">L’utilisateur dispose désormais d’une adresse principale et d’un alias.</span><span class="sxs-lookup"><span data-stu-id="c8aad-173">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="c8aad-174">Par exemple, tous les messages envoyés à l’adresse principale de Eliza Hoffman, Eliza@NodPublishers.com, et son alias, Sales@NodPublishers.com, sont redirigés vers la boîte de réception de Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-174">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="c8aad-175">**Lorsque l’utilisateur répond, l’adresse *de provenance* correspond à son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="c8aad-175">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="c8aad-176">Par exemple, imaginons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="c8aad-176">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="c8aad-177">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="c8aad-177">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end


## <a name="did-you-get-a-parameter-cannot-be-found-that-matches-parameter-name-emailaddresses"></a><span data-ttu-id="c8aad-178">Est-ce que vous obtenez « impossible de trouver un paramètre correspondant au nom de paramètre EmailAddresses » ?</span><span class="sxs-lookup"><span data-stu-id="c8aad-178">Did you get "A parameter cannot be found that matches parameter name EmailAddresses"?</span></span>


<span data-ttu-id="c8aad-179">Si vous obtenez le message d’erreur «**Impossible de trouver un paramètre correspondant au nom de paramètre EmailAddresses**» cela signifie qu’il prend un peu plus de temps pour terminer la configuration de votre client ou votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="c8aad-179">If you get the error message "**A parameter cannot be found that matches parameter name EmailAddresses**" it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="c8aad-180">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="c8aad-180">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="c8aad-181">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="c8aad-181">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="c8aad-182">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="c8aad-182">If the problem persists, call Support and they will do a full sync for you.</span></span>
  
## <a name="did-you-purchase-your-subscription-from-godaddy-or-another-partner"></a><span data-ttu-id="c8aad-183">Avez-vous acheté votre abonnement auprès de GoDaddy ou d'un autre partenaire ?</span><span class="sxs-lookup"><span data-stu-id="c8aad-183">Did you purchase your subscription from GoDaddy or another Partner?</span></span>


<span data-ttu-id="c8aad-184">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="c8aad-184">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="c8aad-185">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="c8aad-185">Related articles</span></span>

[<span data-ttu-id="c8aad-186">Envoyer des courriers à partir d'une adresse différente</span><span class="sxs-lookup"><span data-stu-id="c8aad-186">Send email from a different address</span></span>](https://support.office.com/article/ccba89cb-141c-4a36-8c56-6d16a8556d2e.aspx)

[<span data-ttu-id="c8aad-187">Modifier un nom d'utilisateur et une adresse de courrier</span><span class="sxs-lookup"><span data-stu-id="c8aad-187">Change a user name and email address</span></span>](../add-users/change-a-user-name-and-email-address.md)
  

