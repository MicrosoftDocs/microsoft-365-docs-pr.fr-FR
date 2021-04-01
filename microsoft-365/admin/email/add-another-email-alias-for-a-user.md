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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 0b0bd900-68b1-4bf5-808b-5d240a7739f4
description: 'Découvrez comment vous pouvez avoir plusieurs adresses de messagerie, appelées alias de messagerie, associées à votre compte Microsoft 365 pour les entreprises. '
ms.openlocfilehash: a44271cdbf52136e61702697a960cc3cbcd8119d
ms.sourcegitcommit: d4604e333507c6f57d5bf327531a241b649052de
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/31/2021
ms.locfileid: "51471000"
---
# <a name="add-another-email-alias-for-a-user"></a><span data-ttu-id="b25c3-103">Ajouter un autre alias de courrier pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b25c3-103">Add another email alias for a user</span></span>
  
<span data-ttu-id="b25c3-104">Cet article est réservé aux administrateurs Microsoft 365 qui ont des abonnements pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="b25c3-104">This article is for Microsoft 365 administrators who have business subscriptions.</span></span> <span data-ttu-id="b25c3-105">Il ne s'adresse pas aux particuliers.</span><span class="sxs-lookup"><span data-stu-id="b25c3-105">It's not for home users.</span></span>
  
<span data-ttu-id="b25c3-106">Une adresse de messagerie principale dans Microsoft 365 est généralement l’adresse de messagerie attribuée à un utilisateur lors de la création de son compte.</span><span class="sxs-lookup"><span data-stu-id="b25c3-106">A primary email address in Microsoft 365 is usually the email address a user was assigned when their account was created.</span></span> <span data-ttu-id="b25c3-107">Lorsque l'utilisateur envoie du courrier à une autre personne, son adresse de courrier principale est celle qui apparaît généralement dans le champ  *De*  dans les applications de courrier.</span><span class="sxs-lookup"><span data-stu-id="b25c3-107">When the user sends email to someone else, their primary email address is what typically appears in the  *From*  field in email apps.</span></span> <span data-ttu-id="b25c3-108">Ils peuvent également avoir plusieurs adresses de messagerie associées à leur compte Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="b25c3-108">They can also have more than one email address associated with their Microsoft 365 for business account.</span></span> <span data-ttu-id="b25c3-109">Les adresses supplémentaires sont appelées alias.</span><span class="sxs-lookup"><span data-stu-id="b25c3-109">These additional addresses are called aliases.</span></span> 
  
<span data-ttu-id="b25c3-110">Par exemple, supposons que Son adresse de messagerie soit jenna@contosoco.com, mais qu’elle souhaite également recevoir des messages électroniques sur jen@contosoco.com car certaines personnes lui font référence par ce nom.</span><span class="sxs-lookup"><span data-stu-id="b25c3-110">For example, let's say Jenna has the email address jenna@contosoco.com, but she also wants to receive email at jen@contosoco.com because some people refer to her by that name.</span></span> <span data-ttu-id="b25c3-111">Vous pouvez créer des alias pour elle afin que les deux adresses de messagerie se placent dans la boîte de réception de Son prénom.</span><span class="sxs-lookup"><span data-stu-id="b25c3-111">You can create aliases for her so that both email addresses go to Jenna's inbox.</span></span>
<br><br>  
  
<span data-ttu-id="b25c3-112">Vous pouvez créer jusqu'à 400 alias par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b25c3-112">You can create up to 400 aliases for a user.</span></span> <span data-ttu-id="b25c3-113">Vous ne devez pas acquérir de licence supplémentaire et cela n'occasionne aucun frais.</span><span class="sxs-lookup"><span data-stu-id="b25c3-113">No additional fees or licenses are required.</span></span>
  
> [!Tip]
> <span data-ttu-id="b25c3-114">Si vous souhaitez que plusieurs personnes gèrent les messages électroniques envoyés à une seule adresse de messagerie, comme info@NodPublishers.com ou sales@NodPublishers.com, créez une boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="b25c3-114">If you want multiple people to manage email sent to a single email address like info@NodPublishers.com or sales@NodPublishers.com, create a shared mailbox.</span></span> <span data-ttu-id="b25c3-115">Pour plus d’informations, voir [Créer une boîte aux lettres partagée.](create-a-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="b25c3-115">To learn more, see [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>
  
## <a name="add-email-aliases-to-a-user"></a><span data-ttu-id="b25c3-116">Ajouter des alias de courrier à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b25c3-116">Add email aliases to a user</span></span>
<span data-ttu-id="b25c3-117"><a name="AddEmailPreview"> </a></span><span class="sxs-lookup"><span data-stu-id="b25c3-117"><a name="AddEmailPreview"> </a></span></span>

<span data-ttu-id="b25c3-118">Vous devez avoir [des autorisations d’administrateur](../add-users/about-admin-roles.md) pour le faire.</span><span class="sxs-lookup"><span data-stu-id="b25c3-118">You must have [admin permissions](../add-users/about-admin-roles.md) to do this.</span></span> 

  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="b25c3-119">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="b25c3-119">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="b25c3-120">Dans la page **Utilisateurs** actifs, sélectionnez l’utilisateur > **gérer les alias de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-120">On the **Active Users** page, select the user > **Manage email aliases**.</span></span> <span data-ttu-id="b25c3-121">Vous ne verrez pas cette option si la personne n’a pas de licence qui lui est attribuée.</span><span class="sxs-lookup"><span data-stu-id="b25c3-121">You won't see this option if the person doesn't have a license assigned to them.</span></span> 
    
3. <span data-ttu-id="b25c3-122">Sélectionnez **+ Ajoutez un alias** et entrez un nouvel alias pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b25c3-122">Select **+ Add an alias** and enter a new alias for the user.</span></span>   
    
    > [!Important] 
    > <span data-ttu-id="b25c3-123">Si le message d’erreur « Un paramètre qui correspond au nom de paramètre «**EmailAddresses**» s’ajoute, cela signifie qu’il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="b25c3-123">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="b25c3-124">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="b25c3-124">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="b25c3-125">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="b25c3-125">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="b25c3-126">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="b25c3-126">If the problem persists, call Support and they will do a full sync for you.</span></span>
    
  
    > [!IMPORTANT]
    > <span data-ttu-id="b25c3-127">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="b25c3-127">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="b25c3-128">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b25c3-128">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="b25c3-129">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="b25c3-129">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 
  
     
5. <span data-ttu-id="b25c3-130">Lorsque vous avez terminé, sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-130">When you're done, choose **Save changes**.</span></span>
    
6. <span data-ttu-id="b25c3-131">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b25c3-131">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span>
    
    <span data-ttu-id="b25c3-132">L’utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="b25c3-132">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="b25c3-133">Par exemple, tous les messages envoyés à l’adresse principale d’Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-133">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="b25c3-134">**Lorsque l’utilisateur répond, l’adresse *De*  est son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-134">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="b25c3-135">Par exemple, supposons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-135">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="b25c3-136">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="b25c3-136">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 
    
::: moniker-end

::: moniker range="o365-germany"
    
1. <span data-ttu-id="b25c3-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="b25c3-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
    
2. <span data-ttu-id="b25c3-138">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="b25c3-138">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="b25c3-139">En de côté **du nom d’utilisateur/des alias de messagerie,** **sélectionnez Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-139">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="b25c3-140">Si le message d’erreur « Un paramètre qui correspond au nom de paramètre «**EmailAddresses**» s’ajoute, cela signifie qu’il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="b25c3-140">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="b25c3-141">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="b25c3-141">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="b25c3-142">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="b25c3-142">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="b25c3-143">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="b25c3-143">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="b25c3-144">Dans la zone de texte sous **Alias,** tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b25c3-144">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="b25c3-145">Si vous avez ajouté votre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b25c3-145">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="b25c3-146">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b25c3-146">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b25c3-147">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="b25c3-147">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="b25c3-148">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b25c3-148">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="b25c3-149">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="b25c3-149">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 

5. <span data-ttu-id="b25c3-150">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b25c3-150">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="b25c3-151">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b25c3-151">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="b25c3-152">L’utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="b25c3-152">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="b25c3-153">Par exemple, tous les messages envoyés à l’adresse principale d’Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-153">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="b25c3-154">**Lorsque l’utilisateur répond, l’adresse *De*  est son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-154">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="b25c3-155">Par exemple, supposons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-155">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="b25c3-156">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="b25c3-156">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="b25c3-157">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="b25c3-157">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

    
2. <span data-ttu-id="b25c3-158">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="b25c3-158">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="b25c3-159">En de côté **du nom d’utilisateur/des alias de messagerie,** **sélectionnez Modifier.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-159">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="b25c3-160">Si le message d’erreur « Un paramètre qui correspond au nom de paramètre «**EmailAddresses**» s’ajoute, cela signifie qu’il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="b25c3-160">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="b25c3-161">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="b25c3-161">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="b25c3-162">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="b25c3-162">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="b25c3-163">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="b25c3-163">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="b25c3-164">Dans la zone de texte sous **Alias,** tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b25c3-164">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="b25c3-165">Si vous avez ajouté votre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b25c3-165">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="b25c3-166">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="b25c3-166">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b25c3-167">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="b25c3-167">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="b25c3-168">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b25c3-168">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="b25c3-169">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="b25c3-169">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 

5. <span data-ttu-id="b25c3-170">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b25c3-170">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="b25c3-171">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b25c3-171">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="b25c3-172">L’utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="b25c3-172">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="b25c3-173">Par exemple, tous les messages envoyés à l’adresse principale d’Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-173">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="b25c3-174">**Lorsque l’utilisateur répond, l’adresse *De*  est son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="b25c3-174">**When the user replies, the *From*  address will be her primary email alias.**</span></span> <span data-ttu-id="b25c3-175">Par exemple, supposons qu’un message est envoyé à Sales@NodPublishers.com et qu’il arrive dans la boîte de réception d’Eliza.</span><span class="sxs-lookup"><span data-stu-id="b25c3-175">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="b25c3-176">Quand Eliza répond au courrier, son adresse de courrier principale s'affiche en tant qu'expéditeur, au lieu de Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="b25c3-176">When Eliza replies to the message, her primary email address will appear as the sender, not Sales@NodPublishers.com.</span></span> 

::: moniker-end


## <a name="did-you-get-a-parameter-cannot-be-found-that-matches-parameter-name-emailaddresses"></a><span data-ttu-id="b25c3-177">Avez-vous reçu « Un paramètre indessable qui correspond au nom de paramètre EmailAddresses » ?</span><span class="sxs-lookup"><span data-stu-id="b25c3-177">Did you get "A parameter cannot be found that matches parameter name EmailAddresses"?</span></span>


<span data-ttu-id="b25c3-178">Si vous recevez le message d’erreur « Impossible de trouver un paramètre qui correspond au nom de paramètre **EmailAddresses**», cela signifie qu’il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="b25c3-178">If you get the error message "**A parameter cannot be found that matches parameter name EmailAddresses**" it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="b25c3-179">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="b25c3-179">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="b25c3-180">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="b25c3-180">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="b25c3-181">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="b25c3-181">If the problem persists, call Support and they will do a full sync for you.</span></span>
  
## <a name="did-you-purchase-your-subscription-from-godaddy-or-another-partner"></a><span data-ttu-id="b25c3-182">Avez-vous acheté votre abonnement auprès de GoDaddy ou d'un autre partenaire ?</span><span class="sxs-lookup"><span data-stu-id="b25c3-182">Did you purchase your subscription from GoDaddy or another Partner?</span></span>


<span data-ttu-id="b25c3-183">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="b25c3-183">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="b25c3-184">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b25c3-184">Related articles</span></span>

[<span data-ttu-id="b25c3-185">Envoyer des courriers à partir d'une adresse différente</span><span class="sxs-lookup"><span data-stu-id="b25c3-185">Send email from a different address</span></span>](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e)

[<span data-ttu-id="b25c3-186">Modifier un nom d'utilisateur et une adresse de courrier</span><span class="sxs-lookup"><span data-stu-id="b25c3-186">Change a user name and email address</span></span>](../add-users/change-a-user-name-and-email-address.md)
