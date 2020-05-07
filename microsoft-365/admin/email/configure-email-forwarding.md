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
ms.openlocfilehash: 8cd86bcab4d73719e527f9942cd41a3174966c2d
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140452"
---
# <a name="configure-email-forwarding"></a><span data-ttu-id="32afc-103">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="32afc-103">Configure email forwarding</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="32afc-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="32afc-104">The admin center is changing.</span></span> <span data-ttu-id="32afc-105">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="32afc-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end
  
<span data-ttu-id="32afc-106">En tant qu’administrateur d’une organisation, vous pouvez avoir besoin d’une société pour configurer le transfert du courrier électronique pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32afc-106">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="32afc-107">Le transfert du courrier vous permet de transférer des messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers une boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="32afc-107">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

  
## <a name="configure-email-forwarding"></a><span data-ttu-id="32afc-108">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="32afc-108">Configure email forwarding</span></span>

 <span data-ttu-id="32afc-109">Avant de configurer le transfert du courrier, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="32afc-109">Before you set up email forwarding, note the following:</span></span> 

- <span data-ttu-id="32afc-110">Une fois que vous avez configuré le transfert du courrier, seuls les **nouveaux** messages électroniques envoyés à la boîte aux lettres *de à partir de* seront fowarded.</span><span class="sxs-lookup"><span data-stu-id="32afc-110">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be fowarded.</span></span> 
    
- <span data-ttu-id="32afc-111">Le transfert du courrier exige que le compte *de à partir* de dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="32afc-111">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="32afc-112">Si vous configurez le transfert du courrier, car l’utilisateur a quitté votre organisation, une autre solution consiste à [convertir sa boîte aux lettres en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="32afc-112">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="32afc-113">De cette manière, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="32afc-113">This way several people can access it.</span></span> <span data-ttu-id="32afc-114">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="32afc-114">However, a shared mailbox cannot exceed 50GB.</span></span> 
    
<span data-ttu-id="32afc-115">Pour effectuer ces étapes, vous devez être administrateur Exchange ou administrateur général dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="32afc-115">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="32afc-116">Pour plus d’informations, reportez-vous à la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="32afc-116">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="32afc-117">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="32afc-117">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="32afc-118">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="32afc-118">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>
    
2. <span data-ttu-id="32afc-119">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="32afc-119">Select the name of the user whose email you want to forward to open the properties page.</span></span> 
 
3. <span data-ttu-id="32afc-120">Dans l’onglet **messagerie** , sélectionnez **gérer le transfert du courrier**.</span><span class="sxs-lookup"><span data-stu-id="32afc-120">On the **Mail** tab, select **Manage email forwarding**.</span></span> 
  
4. <span data-ttu-id="32afc-121">Sur la page transfert du courrier, sélectionnez **transférer tous les messages électroniques envoyés à cette boîte aux lettres**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages transférés.</span><span class="sxs-lookup"><span data-stu-id="32afc-121">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="32afc-122">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32afc-122">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="32afc-123">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="32afc-123">Select **Save changes**.</span></span>
    
    <span data-ttu-id="32afc-124">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="32afc-124">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="32afc-125">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="32afc-125">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="32afc-126">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="32afc-126">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="32afc-127">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="32afc-127">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="32afc-128">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="32afc-128">If you do, email forwarding will stop.</span></span> 

::: moniker-end

::: moniker range="o365-germany"
    
 1.   <span data-ttu-id="32afc-129">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="32afc-129">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span> 
    
2. <span data-ttu-id="32afc-130">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="32afc-130">Select the name of the user whose email you want to forward to open the properties page.</span></span> 

3. <span data-ttu-id="32afc-131">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="32afc-131">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="32afc-132">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="32afc-132">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="32afc-133">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32afc-133">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="32afc-134">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32afc-134">Select **Save**.</span></span>
    
    <span data-ttu-id="32afc-135">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="32afc-135">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="32afc-136">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="32afc-136">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="32afc-137">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="32afc-137">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="32afc-138">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="32afc-138">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="32afc-139">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="32afc-139">If you do, email forwarding will stop.</span></span>    

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="32afc-140">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="32afc-140">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
    
2. <span data-ttu-id="32afc-141">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="32afc-141">Select the name of the user whose email you want to forward to open the properties page.</span></span> 

3. <span data-ttu-id="32afc-142">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="32afc-142">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="32afc-143">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="32afc-143">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="32afc-144">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32afc-144">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="32afc-145">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="32afc-145">Select **Save**.</span></span>
    
    <span data-ttu-id="32afc-146">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="32afc-146">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="32afc-147">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="32afc-147">To learn more, see [Use rules to automatically forward messages](https://support.office.com/article/use-rules-to-automatically-forward-messages-45aa9664-4911-4f96-9663-ece42816d746).</span></span> 
    
     <span data-ttu-id="32afc-148">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="32afc-148">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>
    
5. <span data-ttu-id="32afc-149">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="32afc-149">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="32afc-150">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="32afc-150">If you do, email forwarding will stop.</span></span> 

::: moniker-end 
