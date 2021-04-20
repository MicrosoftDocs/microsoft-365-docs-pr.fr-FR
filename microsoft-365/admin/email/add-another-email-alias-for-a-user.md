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
description: 'Découvrez comment vous pouvez avoir plusieurs adresses de messagerie, appelée alias de messagerie, associées à votre compte Microsoft 365 pour les entreprises. '
ms.openlocfilehash: 4003dcfca29a722ccdf9b86cca5aa1141fbdb367
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51892804"
---
# <a name="add-another-email-alias-for-a-user"></a><span data-ttu-id="0f372-103">Ajouter un autre alias de courrier pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="0f372-103">Add another email alias for a user</span></span>
  
<span data-ttu-id="0f372-104">Cet article est réservé aux administrateurs Microsoft 365 qui ont des abonnements pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="0f372-104">This article is for Microsoft 365 administrators who have business subscriptions.</span></span> <span data-ttu-id="0f372-105">Il ne s'adresse pas aux particuliers.</span><span class="sxs-lookup"><span data-stu-id="0f372-105">It's not for home users.</span></span>
  
<span data-ttu-id="0f372-106">Une adresse de messagerie principale dans Microsoft 365 est généralement l'adresse de messagerie attribuée à un utilisateur lors de la création de son compte.</span><span class="sxs-lookup"><span data-stu-id="0f372-106">A primary email address in Microsoft 365 is usually the email address a user was assigned when their account was created.</span></span> <span data-ttu-id="0f372-107">Lorsque l'utilisateur envoie du courrier à une autre personne, son adresse de courrier principale est celle qui apparaît généralement dans le champ  *De*  dans les applications de courrier.</span><span class="sxs-lookup"><span data-stu-id="0f372-107">When the user sends email to someone else, their primary email address is what typically appears in the  *From*  field in email apps.</span></span> <span data-ttu-id="0f372-108">Ils peuvent également avoir plusieurs adresses de messagerie associées à leur compte Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="0f372-108">They can also have more than one email address associated with their Microsoft 365 for business account.</span></span> <span data-ttu-id="0f372-109">Les adresses supplémentaires sont appelées alias.</span><span class="sxs-lookup"><span data-stu-id="0f372-109">These additional addresses are called aliases.</span></span> 
  
<span data-ttu-id="0f372-110">Par exemple, supposons que Son adresse de messagerie soit jenna@contosoco.com, mais qu'elle souhaite également recevoir des messages électroniques sur jen@contosoco.com car certaines personnes lui font référence par ce nom.</span><span class="sxs-lookup"><span data-stu-id="0f372-110">For example, let's say Jenna has the email address jenna@contosoco.com, but she also wants to receive email at jen@contosoco.com because some people refer to her by that name.</span></span> <span data-ttu-id="0f372-111">Vous pouvez créer des alias pour elle afin que les deux adresses de messagerie se placent dans la boîte de réception de Son prénom.</span><span class="sxs-lookup"><span data-stu-id="0f372-111">You can create aliases for her so that both email addresses go to Jenna's inbox.</span></span>
<br><br>  
  
<span data-ttu-id="0f372-112">Vous pouvez créer jusqu'à 400 alias par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0f372-112">You can create up to 400 aliases for a user.</span></span> <span data-ttu-id="0f372-113">Vous ne devez pas acquérir de licence supplémentaire et cela n'occasionne aucun frais.</span><span class="sxs-lookup"><span data-stu-id="0f372-113">No additional fees or licenses are required.</span></span>
  
> [!Tip]
> <span data-ttu-id="0f372-114">Si vous souhaitez que plusieurs personnes gèrent les messages électroniques envoyés à une seule adresse de messagerie telle que info@NodPublishers.com ou sales@NodPublishers.com, créez une boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="0f372-114">If you want multiple people to manage email sent to a single email address like info@NodPublishers.com or sales@NodPublishers.com, create a shared mailbox.</span></span> <span data-ttu-id="0f372-115">Pour plus d'informations, voir [Créer une boîte aux lettres partagée.](create-a-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="0f372-115">To learn more, see [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>
  
## <a name="add-email-aliases-to-a-user"></a><span data-ttu-id="0f372-116">Ajouter des alias de courrier à un utilisateur</span><span class="sxs-lookup"><span data-stu-id="0f372-116">Add email aliases to a user</span></span>
<span data-ttu-id="0f372-117"><a name="AddEmailPreview"> </a></span><span class="sxs-lookup"><span data-stu-id="0f372-117"><a name="AddEmailPreview"> </a></span></span>

<span data-ttu-id="0f372-118">Vous devez avoir [des autorisations d'administrateur](../add-users/about-admin-roles.md) pour le faire.</span><span class="sxs-lookup"><span data-stu-id="0f372-118">You must have [admin permissions](../add-users/about-admin-roles.md) to do this.</span></span> 

  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="0f372-119">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0f372-119">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="0f372-120">Dans la page **Utilisateurs** actifs, sélectionnez l'utilisateur > **gérer les alias de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="0f372-120">On the **Active Users** page, select the user > **Manage email aliases**.</span></span> <span data-ttu-id="0f372-121">Vous ne verrez pas cette option si la personne n'a pas de licence qui lui est attribuée.</span><span class="sxs-lookup"><span data-stu-id="0f372-121">You won't see this option if the person doesn't have a license assigned to them.</span></span> 
    
3. <span data-ttu-id="0f372-122">Sélectionnez **+ Ajoutez un alias** et entrez un nouvel alias pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0f372-122">Select **+ Add an alias** and enter a new alias for the user.</span></span>   
    
    > [!Important] 
    > <span data-ttu-id="0f372-123">Si vous obtenez le message d'erreur « Impossible de trouver un paramètre qui correspond au nom du paramètre **« EmailAddresses**», cela signifie qu'il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="0f372-123">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="0f372-124">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="0f372-124">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="0f372-125">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="0f372-125">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="0f372-126">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="0f372-126">If the problem persists, call Support and they will do a full sync for you.</span></span>
    
  
    > [!IMPORTANT]
    > <span data-ttu-id="0f372-127">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="0f372-127">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="0f372-128">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0f372-128">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="0f372-129">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="0f372-129">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 
  
     
5. <span data-ttu-id="0f372-130">Lorsque vous avez terminé, sélectionnez **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="0f372-130">When you're done, choose **Save changes**.</span></span>
    
6. <span data-ttu-id="0f372-131">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f372-131">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span>
    
    <span data-ttu-id="0f372-132">L'utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="0f372-132">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="0f372-133">Par exemple, tous les messages envoyés à l'adresse principale d'Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-133">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="0f372-134">**Lorsque l'utilisateur répond, l'adresse *De* dépend de son client Outlook. Outlook sur le web utilisera l'alias auquel le courrier électronique a été reçu (nous appellerons cela le principe ping- domaine). Le bureau Outlook utilisera son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="0f372-134">**When the user replies, the *From* address will depend on her Outlook client. Outlook on the web will use the alias at which the email was received (we'll call this the ping-pong principle). Outlook desktop will use her primary email alias.**</span></span> <span data-ttu-id="0f372-135">Par exemple, supposons qu'un message est envoyé à Sales@NodPublishers.com et qu'il arrive dans la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-135">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="0f372-136">Lorsque Eliza répond au message à l'aide du bureau Outlook, son adresse de messagerie principale s'Eliza@NodPublishers.com, et non Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="0f372-136">When Eliza replies to the message using Outlook desktop, her primary email address will appear as Eliza@NodPublishers.com, not Sales@NodPublishers.com.</span></span>
    
::: moniker-end

::: moniker range="o365-germany"
    
1. <span data-ttu-id="0f372-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0f372-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
    
2. <span data-ttu-id="0f372-138">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="0f372-138">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="0f372-139">En de côté **du nom d'utilisateur/des alias de messagerie,** **sélectionnez Modifier.**</span><span class="sxs-lookup"><span data-stu-id="0f372-139">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="0f372-140">Si le message d'erreur « Un paramètre qui correspond au nom de paramètre «**EmailAddresses**» s'ajoute, cela signifie qu'il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="0f372-140">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="0f372-141">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="0f372-141">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="0f372-142">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="0f372-142">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="0f372-143">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="0f372-143">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="0f372-144">Dans la zone de texte sous **Alias,** tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0f372-144">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="0f372-145">Si vous avez ajouté votre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0f372-145">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="0f372-146">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="0f372-146">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0f372-147">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="0f372-147">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="0f372-148">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0f372-148">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="0f372-149">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="0f372-149">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 

5. <span data-ttu-id="0f372-150">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0f372-150">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="0f372-151">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f372-151">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="0f372-152">L'utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="0f372-152">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="0f372-153">Par exemple, tous les messages envoyés à l'adresse principale d'Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-153">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="0f372-154">**Lorsque l'utilisateur répond, *l'adresse De* dépend de son client Outlook. Outlook sur le web utilisera l'alias auquel le courrier électronique a été reçu (nous appellerons cela le principe ping- domaine). Le bureau Outlook utilisera son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="0f372-154">**When the user replies, the *From* address will depend on her Outlook client. Outlook on the web will use the alias at which the email was received (we'll call this the ping-pong principle). Outlook desktop will use her primary email alias.**</span></span> <span data-ttu-id="0f372-155">Par exemple, supposons qu'un message est envoyé à Sales@NodPublishers.com et qu'il arrive dans la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-155">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="0f372-156">Lorsque Eliza répond au message à l'aide du bureau Outlook, son adresse de messagerie principale s'Eliza@NodPublishers.com, et non Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="0f372-156">When Eliza replies to the message using Outlook desktop, her primary email address will appear as Eliza@NodPublishers.com, not Sales@NodPublishers.com.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="0f372-157">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0f372-157">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

    
2. <span data-ttu-id="0f372-158">Dans la page **Utilisateurs actifs**, sélectionnez le nom de la personne à modifier.</span><span class="sxs-lookup"><span data-stu-id="0f372-158">On the **Active Users** page, select the name of the person you want to edit.</span></span>

3. <span data-ttu-id="0f372-159">En de côté **du nom d'utilisateur/des alias de messagerie,** **sélectionnez Modifier.**</span><span class="sxs-lookup"><span data-stu-id="0f372-159">Next to **Username / Email Aliases**, select **Edit**.</span></span>

    > [!Important] 
    > <span data-ttu-id="0f372-160">Si le message d'erreur « Un paramètre qui correspond au nom de paramètre «**EmailAddresses**» s'ajoute, cela signifie qu'il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="0f372-160">If you get the error message "**A parameter cannot be found that matches parameter name 'EmailAddresses**," it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="0f372-161">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="0f372-161">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="0f372-162">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="0f372-162">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="0f372-163">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="0f372-163">If the problem persists, call Support and they will do a full sync for you.</span></span>

4. <span data-ttu-id="0f372-164">Dans la zone de texte sous **Alias,** tapez la première partie du nouvel alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="0f372-164">In the text box under **Alias**, type the first part of the new email alias.</span></span> <span data-ttu-id="0f372-165">Si vous avez ajouté votre domaine à Microsoft 365, vous pouvez choisir le domaine du nouvel alias d'e-mail dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0f372-165">If you added your own domain to Microsoft 365, you can choose the domain for the new email alias by using the drop-down list.</span></span> <span data-ttu-id="0f372-166">Puis sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="0f372-166">Then select **Add**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0f372-167">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="0f372-167">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span> 
  
    > [!TIP]
    > <span data-ttu-id="0f372-168">L'alias de courrier doit se terminer par un domaine figurant dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="0f372-168">The email alias must end with a domain from the drop-down list.</span></span> <span data-ttu-id="0f372-169">Pour ajouter un autre nom de domaine à la liste, voir [Ajouter un domaine à Microsoft 365.](../setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="0f372-169">To add another domain name to the list, see [Add a domain to Microsoft 365](../setup/add-domain.md).</span></span> 

5. <span data-ttu-id="0f372-170">Lorsque vous avez terminé, sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0f372-170">When you're done, select **Save**.</span></span>

6. <span data-ttu-id="0f372-171">Patientez 24 heures pour que les nouveaux alias se remplissent dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f372-171">Wait 24 hours for the new aliases to populate throughout Microsoft 365.</span></span> 
    
    <span data-ttu-id="0f372-172">L'utilisateur aura désormais une adresse principale et un alias.</span><span class="sxs-lookup"><span data-stu-id="0f372-172">The user will now have a primary address and an alias.</span></span> <span data-ttu-id="0f372-173">Par exemple, tous les messages envoyés à l'adresse principale d'Eliza Eliza@NodPublishers.com et à son alias, Sales@NodPublishers.com, seront acheminés vers la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-173">For example, all mail sent to Eliza Hoffman's primary address, Eliza@NodPublishers.com, and her  alias, Sales@NodPublishers.com, will go to Eliza's Inbox.</span></span>
    
  
7. <span data-ttu-id="0f372-174">**Lorsque l'utilisateur répond, l'adresse *De* dépend de son client Outlook. Outlook sur le web utilisera l'alias auquel le courrier électronique a été reçu (nous appellerons cela le principe ping- domaine). Le bureau Outlook utilise son alias de messagerie principal.**</span><span class="sxs-lookup"><span data-stu-id="0f372-174">**When the user replies, the *From* address will depend on her Outlook client. Outlook on the web will use the alias at which the email was received (we'll call this the ping-pong principle). Outlook desktop will use her primary email alias.**</span></span> <span data-ttu-id="0f372-175">Par exemple, supposons qu'un message est envoyé à Sales@NodPublishers.com et qu'il arrive dans la boîte de réception d'Eliza.</span><span class="sxs-lookup"><span data-stu-id="0f372-175">For example, let's say a message is sent to Sales@NodPublishers.com, and it arrives in Eliza's inbox.</span></span> <span data-ttu-id="0f372-176">Lorsque Eliza répond au message à l'aide du bureau Outlook, son adresse de messagerie principale s'Eliza@NodPublishers.com, et non Sales@NodPublishers.com.</span><span class="sxs-lookup"><span data-stu-id="0f372-176">When Eliza replies to the message using Outlook desktop, her primary email address will appear as Eliza@NodPublishers.com, not Sales@NodPublishers.com.</span></span>

::: moniker-end


## <a name="did-you-get-a-parameter-cannot-be-found-that-matches-parameter-name-emailaddresses"></a><span data-ttu-id="0f372-177">Avez-vous reçu « Un paramètre indessable qui correspond au nom de paramètre EmailAddresses » ?</span><span class="sxs-lookup"><span data-stu-id="0f372-177">Did you get "A parameter cannot be found that matches parameter name EmailAddresses"?</span></span>


<span data-ttu-id="0f372-178">Si vous recevez le message d'erreur « Impossible de trouver un paramètre qui correspond au nom de paramètre **EmailAddresses**», cela signifie qu'il faut un peu plus de temps pour terminer la configuration de votre client ou de votre domaine personnalisé si vous en avez récemment ajouté un.</span><span class="sxs-lookup"><span data-stu-id="0f372-178">If you get the error message "**A parameter cannot be found that matches parameter name EmailAddresses**" it means that it's taking a bit longer to finish setting up your tenant, or your custom domain if you recently added one.</span></span> <span data-ttu-id="0f372-179">Le processus de configuration peut prendre jusqu'à 4 heures.</span><span class="sxs-lookup"><span data-stu-id="0f372-179">The setup process can take up to 4 hours to complete.</span></span> <span data-ttu-id="0f372-180">Patientez le temps que le processus de configuration ait le temps de terminer, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="0f372-180">Wait a while so the set up process has time to finish, and then try again.</span></span> <span data-ttu-id="0f372-181">Si le problème persiste, appelez le support technique qui se chargera d'effectuer une synchronisation complète pour vous.</span><span class="sxs-lookup"><span data-stu-id="0f372-181">If the problem persists, call Support and they will do a full sync for you.</span></span>
  
## <a name="did-you-purchase-your-subscription-from-godaddy-or-another-partner"></a><span data-ttu-id="0f372-182">Avez-vous acheté votre abonnement auprès de GoDaddy ou d'un autre partenaire ?</span><span class="sxs-lookup"><span data-stu-id="0f372-182">Did you purchase your subscription from GoDaddy or another Partner?</span></span>


<span data-ttu-id="0f372-183">Si vous achetez votre abonnement auprès de GoDaddy ou d'un autre partenaire, vous devez accéder à la console de gestion de GoDaddy ou du partenaire pour définir le nouvel alias comme alias principal.</span><span class="sxs-lookup"><span data-stu-id="0f372-183">If you purchased your subscription from GoDaddy or another Partner, to set the new alias as the primary, you must go to the GoDaddy/partner management console.</span></span>

## <a name="sending-email-from-the-proxy-address-easily"></a><span data-ttu-id="0f372-184">Envoi aisément d'e-mails à partir de l'adresse proxy</span><span class="sxs-lookup"><span data-stu-id="0f372-184">Sending email from the proxy address easily</span></span>

<span data-ttu-id="0f372-185">Une nouvelle fonctionnalité est en cours de déploiement en avril 2021 qui permet aux utilisateurs d'envoyer facilement des messages à partir de leurs alias lors de l'utilisation d'Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="0f372-185">A new feature is rolling out in April 2021 that allows users to send from their aliases easily when using Outlook on the web.</span></span> <span data-ttu-id="0f372-186">Lorsque la fonctionnalité est mise en place dans une location où l'administrateur client utilise la cmdlet, les utilisateurs de la location ont accès à une liste de case à cocher où chaque entrée correspond à un alias dans leurs `Set-OrganizationConfig -SendFromAliasEnabled $true` paramètres Outlook.</span><span class="sxs-lookup"><span data-stu-id="0f372-186">When the feature rolls out to a tenancy where the tenant admin uses the `Set-OrganizationConfig -SendFromAliasEnabled $true` cmdlet, users within the tenancy will get access to a list of checkboxes where each entry corresponds to an alias in their Outlook settings.</span></span> <span data-ttu-id="0f372-187">La sélection d'un alias l'affiche dans ladown From du formulaire Composer.</span><span class="sxs-lookup"><span data-stu-id="0f372-187">Selecting an alias will make it appear in the From dropdown in the Compose form.</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="0f372-188">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0f372-188">Related articles</span></span>

[<span data-ttu-id="0f372-189">Envoyer des courriers à partir d'une adresse différente</span><span class="sxs-lookup"><span data-stu-id="0f372-189">Send email from a different address</span></span>](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e)

[<span data-ttu-id="0f372-190">Modifier un nom d'utilisateur et une adresse de courrier</span><span class="sxs-lookup"><span data-stu-id="0f372-190">Change a user name and email address</span></span>](../add-users/change-a-user-name-and-email-address.md)
