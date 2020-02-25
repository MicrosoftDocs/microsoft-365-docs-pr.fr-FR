---
title: Accorder des autorisations de boîte aux lettres à un autre utilisateur dans Office 365 - Aide de l’administrateur
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
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
ms.assetid: 1dbcf12f-a9de-4d1d-b0b3-a227f8a736d8
description: "Découvrez comment accorder le droit à un utilisateur d'accéder à la boîte aux lettres d'un autre utilisateur. Cela permet à l’utilisateur de lire et d’envoyer des messages électroniques à partir de la boîte aux lettres d'un autre utilisateur. "
ms.openlocfilehash: 8c3572cf543545de4a2825012f6c2e8e906cd8dd
ms.sourcegitcommit: ca2b58ef8f5be24f09e73620b74a1ffcf2d4c290
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42239373"
---
# <a name="give-mailbox-permissions-to-another-user-in-office-365---admin-help"></a><span data-ttu-id="4f86e-104">Accorder des autorisations de boîte aux lettres à un autre utilisateur dans Office 365 – Aide de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-104">Give mailbox permissions to another user in Office 365 - Admin Help</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="4f86e-105">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="4f86e-105">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

::: moniker-end

<span data-ttu-id="4f86e-106">En tant qu’administrateur, certaines exigences de votre entreprise vous entraînent à autoriser certains utilisateurs à accéder à la boîte aux lettres d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f86e-106">As the admin, you may have company requirements to allow some users access to another user's mailbox.</span></span> <span data-ttu-id="4f86e-107">Par exemple, vous souhaitez peut-être autoriser un assistant à envoyer ou à lire du courrier dans la boîte aux lettres de son responsable ou donner la possibilité à un de vos utilisateurs d’envoyer du courrier de la part d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f86e-107">For example, you may want to enable an assistant to send or read email from their manager's mailbox, or one of your user's the ability to send email on behalf of another user.</span></span> <span data-ttu-id="4f86e-108">Cette rubrique vous explique comment procéder pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="4f86e-108">This topic shows you how to accomplish this.</span></span>
  
<span data-ttu-id="4f86e-109">Si vous cherchez des informations concernant la création et la gestion de boîtes aux lettres partagées, consultez l’article [Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="4f86e-109">If you're looking for information about creating and managing shared mailboxes, check out [Create a shared mailbox](../email/create-a-shared-mailbox.md).</span></span>
    
## <a name="looking-to-set-up-mailbox-permissions"></a><span data-ttu-id="4f86e-110">Vous cherchez à configurer des autorisations de boîte aux lettres ?</span><span class="sxs-lookup"><span data-stu-id="4f86e-110">Looking to set up mailbox permissions?</span></span>

<span data-ttu-id="4f86e-p103">Les autorisations de boîte aux lettres vous permettent d’accorder un accès en lecture/écriture à une boîte aux lettres à un utilisateur autre que son propriétaire. L’article qui suit vous fournira les informations dont vous avez besoin pour configurer et utiliser cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="4f86e-p103">Mailbox permissions allow you to give read/write access to a mailbox to another user. The articles below might give you the help you need to set up and use this feature:</span></span>
  
 <span data-ttu-id="4f86e-113">**Configuration des autorisations :**</span><span class="sxs-lookup"><span data-stu-id="4f86e-113">**Setting up the permissions:**</span></span>
  
<span data-ttu-id="4f86e-114">pour configurer des autorisations, la première étape consiste à décider des actions que vous voulez autoriser l’autre utilisateur à pouvoir effectuer dans la boîte aux lettres donnée.</span><span class="sxs-lookup"><span data-stu-id="4f86e-114">The first step to setting up permissions is deciding which actions you want to allow the other user to take in the given mailbox.</span></span> <span data-ttu-id="4f86e-115">Vous pouvez autoriser un utilisateur à lire des courriers dans la boîte aux lettres, à envoyer des courriers de la part d’un autre utilisateur et à envoyer des courriers comme s’ils étaient envoyés à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-115">You can allow a user to read emails from the mailbox, send emails on behalf of another user, and send emails as if they were sent from that mailbox.</span></span> <span data-ttu-id="4f86e-116">Consultez les articles suivants pour configurer chaque type d’autorisation :</span><span class="sxs-lookup"><span data-stu-id="4f86e-116">Refer to the following articles on how to set up each type of permissions:</span></span>
  
- [<span data-ttu-id="4f86e-117">Lire du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-117">Read email from another user's mailbox</span></span>](https://support.office.com/article/Read-email-from-another-user-s-mailbox-in-Office-365-cb3b6a8a-c6e8-4342-803c-3e54b6428cc2?#bkmk_reademailanotheruser)
    
- [<span data-ttu-id="4f86e-118">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-118">Send email from another user's mailbox</span></span>](https://support.office.com/article/Send-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E?#bkmk_sendemailanotheruser)
    
- [<span data-ttu-id="4f86e-119">Envoyer du courrier pour le compte d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-119">Send email on behalf of a user</span></span>](https://support.office.com/article/Send-email-on-behalf-of-another-user-in-Office-365-C5E7749D-244E-477F-998E-55D3876C22EC?#bkmk_sendbehalflanotheruser)
    
 <span data-ttu-id="4f86e-120">**Propagation des modifications :**</span><span class="sxs-lookup"><span data-stu-id="4f86e-120">**Changing propagation:**</span></span>
  
<span data-ttu-id="4f86e-121">lorsque vous avez défini les autorisations, la propagation des modifications dans le système et leur application peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="4f86e-121">Once you've set up the permissions, it can take up to 60 minutes for the changes to propagate through the system and be in effect.</span></span>
  
 <span data-ttu-id="4f86e-122">**Comment utiliser une boîte aux lettres une fois les autorisations configurées :**</span><span class="sxs-lookup"><span data-stu-id="4f86e-122">**How to use it once permissions are set up:**</span></span>
  
<span data-ttu-id="4f86e-123">Lorsque vous avez reçu l’accès à une boîte aux lettres, plusieurs méthodes s’offrent à vous pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="4f86e-123">There are a few different ways you can access a mailbox once you've been given access.</span></span> <span data-ttu-id="4f86e-124">Pour obtenir de l’aide sur cette fonction, consultez cet article : [Accéder à la boîte aux lettres d’une autre personne](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f86e-124">For help on this, refer to this article: [Access another person's mailbox](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081.aspx)</span></span>
  
## <a name="send-email-from-another-users-mailbox"></a><span data-ttu-id="4f86e-125">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-125">Send email from another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4f86e-126">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-126">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="4f86e-127">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation d’envoi) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f86e-127">Select the name of the user (from whom you plan to give a sending permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="4f86e-128">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-128">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>

4. <span data-ttu-id="4f86e-129">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-129">Next to **Send as**, select **Edit**.</span></span> 

5. <span data-ttu-id="4f86e-130">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="4f86e-130">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
6. <span data-ttu-id="4f86e-131">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-131">Select **Save**.</span></span>
 
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4f86e-132">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-132">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="4f86e-133">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-133">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="4f86e-134">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-134">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="4f86e-135">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="4f86e-135">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="4f86e-136">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-136">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4f86e-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="4f86e-138">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-138">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="4f86e-139">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-139">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="4f86e-140">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="4f86e-140">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="4f86e-141">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-141">Select **Save**.</span></span>

::: moniker-end
  
## <a name="read-email-in-another-users-mailbox"></a><span data-ttu-id="4f86e-142">Lire du courrier dans la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-142">Read email in another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4f86e-143">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-143">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="4f86e-144">Sélectionnez le nom de l’utilisateur (dont vous voulez autoriser la lecture de la boîte aux lettres) pour ouvrir son volet de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f86e-144">Select the name of the user (whose mailbox you want to allow to be read) to open their properties pane.</span></span>
    
3. <span data-ttu-id="4f86e-145">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-145">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="4f86e-146">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-146">Next to **Read and manage**, select **Edit**.</span></span> 
    
5. <span data-ttu-id="4f86e-147">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-147">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

6. <span data-ttu-id="4f86e-148">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-148">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4f86e-149">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-149">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  
  
2. <span data-ttu-id="4f86e-150">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-150">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="4f86e-151">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-151">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="4f86e-152">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-152">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="4f86e-153">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-153">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4f86e-154">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-154">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
  
2. <span data-ttu-id="4f86e-155">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-155">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="4f86e-156">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-156">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="4f86e-157">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-157">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="4f86e-158">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-158">Select **Save**.</span></span>

::: moniker-end


## <a name="send-email-on-behalf-of-another-user"></a><span data-ttu-id="4f86e-159">Envoyez du courrier de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="4f86e-159">Send email on behalf of another user</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="4f86e-160">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-160">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="4f86e-161">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation **Envoyer de la part de**) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f86e-161">Select the name of the user (from whom you plan to give a **Send on behalf** permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="4f86e-162">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-162">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="4f86e-163">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-163">Next to **Send on behalf**, select **Edit**.</span></span>

5. <span data-ttu-id="4f86e-164">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-164">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

6. <span data-ttu-id="4f86e-165">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-165">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4f86e-166">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-166">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="4f86e-167">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-167">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="4f86e-168">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-168">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="4f86e-169">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-169">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="4f86e-170">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-170">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4f86e-171">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="4f86e-171">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="4f86e-172">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-172">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="4f86e-173">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-173">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="4f86e-174">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="4f86e-174">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="4f86e-175">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4f86e-175">Select **Save**.</span></span>

::: moniker-end


## <a name="send-and-read-from-outlook-and-outlook-on-the-web-for-business"></a><span data-ttu-id="4f86e-176">Envoyer et lire du courrier à partir d’Outlook et d’Outlook sur le web pour les clients professionnels</span><span class="sxs-lookup"><span data-stu-id="4f86e-176">Send and read from Outlook and Outlook on the web for business</span></span>


<span data-ttu-id="4f86e-177">Vous voulez savoir comment envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="4f86e-177">Want to know how to send email from another user's mailbox?</span></span> <span data-ttu-id="4f86e-178">Consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f86e-178">Check out the following topics:</span></span>
  
- [<span data-ttu-id="4f86e-179">Gérer les éléments de courrier et de calendrier d’une autre personne</span><span class="sxs-lookup"><span data-stu-id="4f86e-179">Manage another person's mail and calendar items</span></span>](https://support.office.com/article/afb79d6b-2967-43b9-a944-a6b953190af5.aspx)
    
- [<span data-ttu-id="4f86e-180">Envoyer du courrier pour le compte d’une autre personne ou d’un groupe</span><span class="sxs-lookup"><span data-stu-id="4f86e-180">Send email from another person or group</span></span>](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx)
