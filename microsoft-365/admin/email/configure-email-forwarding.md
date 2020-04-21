---
title: Configurer le transfert des e-mails
f1.keywords:
- NOCSH
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
ms.custom:
- MSStore_Link
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: ab5eb117-0f22-4fa7-a662-3a6bdb0add74
description: Configurez le transfert du courrier vers un ou plusieurs comptes de messagerie à l’aide d’Office 365.
ms.openlocfilehash: 5807649fa43d094fd8f05cf63e2905d7cdb6dd7d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43628914"
---
# <a name="configure-email-forwarding"></a><span data-ttu-id="97400-103">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="97400-103">Configure email forwarding</span></span>
  
<span data-ttu-id="97400-104">En tant qu’administrateur d’une organisation, vous pouvez avoir besoin d’une société pour configurer le transfert du courrier électronique pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97400-104">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="97400-105">Le transfert du courrier vous permet de transférer des messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers une boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="97400-105">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

  
## <a name="configure-email-forwarding"></a><span data-ttu-id="97400-106">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="97400-106">Configure email forwarding</span></span>

 <span data-ttu-id="97400-107">Avant de configurer le transfert du courrier, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="97400-107">Before you set up email forwarding, note the following:</span></span> 

- <span data-ttu-id="97400-108">Une fois que vous avez configuré le transfert du courrier, seuls les **nouveaux** messages électroniques envoyés à la boîte aux lettres *de à partir de* seront fowarded.</span><span class="sxs-lookup"><span data-stu-id="97400-108">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be fowarded.</span></span> 
    
- <span data-ttu-id="97400-109">Le transfert du courrier exige que le compte *de à partir* de dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="97400-109">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="97400-110">Si vous configurez le transfert du courrier, car l’utilisateur a quitté votre organisation, une autre solution consiste à [convertir sa boîte aux lettres en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="97400-110">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="97400-111">De cette manière, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="97400-111">This way several people can access it.</span></span> <span data-ttu-id="97400-112">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="97400-112">However, a shared mailbox cannot exceed 50GB.</span></span> 
    
<span data-ttu-id="97400-113">Pour effectuer ces étapes, vous devez être administrateur Exchange ou administrateur général dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="97400-113">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="97400-114">Pour plus d’informations, reportez-vous à la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="97400-114">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="97400-115">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="97400-115">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="97400-116">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="97400-116">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="97400-117">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="97400-117">Select the name of the user whose email you want to forward to open the properties page.</span></span> 
 
3. <span data-ttu-id="97400-118">Dans l’onglet **messagerie** , sélectionnez **gérer le transfert du courrier**.</span><span class="sxs-lookup"><span data-stu-id="97400-118">On the **Mail** tab, select **Manage email forwarding**.</span></span> 
  
4. <span data-ttu-id="97400-119">Sur la page transfert du courrier, sélectionnez **transférer tous les messages électroniques envoyés à cette boîte aux lettres**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages transférés.</span><span class="sxs-lookup"><span data-stu-id="97400-119">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="97400-120">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97400-120">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="97400-121">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="97400-121">Select **Save changes**.</span></span>
    
    <span data-ttu-id="97400-122">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="97400-122">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="97400-123">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="97400-123">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="97400-124">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="97400-124">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="97400-125">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="97400-125">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="97400-126">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="97400-126">If you do, email forwarding will stop.</span></span> 

::: moniker-end

::: moniker range="o365-germany"
    
 1.   <span data-ttu-id="97400-127">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="97400-127">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
2. <span data-ttu-id="97400-128">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="97400-128">Select the name of the user whose email you want to forward to open the properties page.</span></span> 

3. <span data-ttu-id="97400-129">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="97400-129">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="97400-130">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="97400-130">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="97400-131">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97400-131">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="97400-132">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97400-132">Select **Save**.</span></span>
    
    <span data-ttu-id="97400-133">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="97400-133">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="97400-134">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="97400-134">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="97400-135">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="97400-135">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="97400-136">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="97400-136">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="97400-137">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="97400-137">If you do, email forwarding will stop.</span></span>    

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="97400-138">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="97400-138">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
    
2. <span data-ttu-id="97400-139">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="97400-139">Select the name of the user whose email you want to forward to open the properties page.</span></span> 

3. <span data-ttu-id="97400-140">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="97400-140">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="97400-141">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="97400-141">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="97400-142">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="97400-142">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="97400-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="97400-143">Select **Save**.</span></span>
    
    <span data-ttu-id="97400-144">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="97400-144">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="97400-145">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="97400-145">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="97400-146">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="97400-146">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="97400-147">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="97400-147">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="97400-148">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="97400-148">If you do, email forwarding will stop.</span></span> 

::: moniker-end 
