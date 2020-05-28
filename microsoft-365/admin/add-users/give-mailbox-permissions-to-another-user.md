---
title: Accorder des autorisations de boîte aux lettres à un autre utilisateur – Aide de l’administrateur
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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1dbcf12f-a9de-4d1d-b0b3-a227f8a736d8
description: "Découvrez comment accorder le droit à un utilisateur d'accéder à la boîte aux lettres d'un autre utilisateur. Cela permet à l’utilisateur de lire et d’envoyer des messages électroniques à partir de la boîte aux lettres d'un autre utilisateur. "
ms.openlocfilehash: 51de5f4e2b134a503ec935b1f1d0ec6519d2c229
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44387176"
---
# <a name="give-mailbox-permissions-to-another-user---admin-help"></a><span data-ttu-id="62818-104">Accorder des autorisations de boîte aux lettres à un autre utilisateur – Aide de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="62818-104">Give mailbox permissions to another user - Admin Help</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="62818-105">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="62818-105">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

::: moniker-end

<span data-ttu-id="62818-106">En tant qu’administrateur, certaines exigences de votre entreprise vous entraînent à autoriser certains utilisateurs à accéder à la boîte aux lettres d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62818-106">As the admin, you may have company requirements to allow some users access to another user's mailbox.</span></span> <span data-ttu-id="62818-107">Par exemple, vous souhaitez peut-être autoriser un assistant à envoyer ou à lire du courrier dans la boîte aux lettres de son responsable ou donner la possibilité à un de vos utilisateurs d’envoyer du courrier de la part d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62818-107">For example, you may want to enable an assistant to send or read email from their manager's mailbox, or one of your user's the ability to send email on behalf of another user.</span></span> <span data-ttu-id="62818-108">Cette rubrique vous explique comment procéder pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="62818-108">This topic shows you how to accomplish this.</span></span>
  
<span data-ttu-id="62818-109">Si vous cherchez des informations concernant la création et la gestion de boîtes aux lettres partagées, consultez l’article [Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="62818-109">If you're looking for information about creating and managing shared mailboxes, check out [Create a shared mailbox](../email/create-a-shared-mailbox.md).</span></span>
    
## <a name="looking-to-set-up-mailbox-permissions"></a><span data-ttu-id="62818-110">Vous cherchez à configurer des autorisations de boîte aux lettres ?</span><span class="sxs-lookup"><span data-stu-id="62818-110">Looking to set up mailbox permissions?</span></span>

<span data-ttu-id="62818-p103">Les autorisations de boîte aux lettres vous permettent d’accorder un accès en lecture/écriture à une boîte aux lettres à un utilisateur autre que son propriétaire. L’article qui suit vous fournira les informations dont vous avez besoin pour configurer et utiliser cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="62818-p103">Mailbox permissions allow you to give read/write access to a mailbox to another user. The articles below might give you the help you need to set up and use this feature:</span></span>
  
 <span data-ttu-id="62818-113">**Configuration des autorisations :**</span><span class="sxs-lookup"><span data-stu-id="62818-113">**Setting up the permissions:**</span></span>
  
<span data-ttu-id="62818-114">pour configurer des autorisations, la première étape consiste à décider des actions que vous voulez autoriser l’autre utilisateur à pouvoir effectuer dans la boîte aux lettres donnée.</span><span class="sxs-lookup"><span data-stu-id="62818-114">The first step to setting up permissions is deciding which actions you want to allow the other user to take in the given mailbox.</span></span> <span data-ttu-id="62818-115">Vous pouvez autoriser un utilisateur à lire des courriers dans la boîte aux lettres, à envoyer des courriers de la part d’un autre utilisateur et à envoyer des courriers comme s’ils étaient envoyés à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-115">You can allow a user to read emails from the mailbox, send emails on behalf of another user, and send emails as if they were sent from that mailbox.</span></span> <span data-ttu-id="62818-116">Consultez les articles suivants pour configurer chaque type d’autorisation :</span><span class="sxs-lookup"><span data-stu-id="62818-116">Refer to the following articles on how to set up each type of permissions:</span></span>
  
- [<span data-ttu-id="62818-117">Lire du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-117">Read email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#read-email-in-another-users-mailbox)
    
- [<span data-ttu-id="62818-118">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-118">Send email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)

- [<span data-ttu-id="62818-119">Envoyer un e-mail de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-119">Send email on behalf of another user</span></span>](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)
    
 <span data-ttu-id="62818-120">**Propagation des modifications :**</span><span class="sxs-lookup"><span data-stu-id="62818-120">**Changing propagation:**</span></span>
  
<span data-ttu-id="62818-121">lorsque vous avez défini les autorisations, la propagation des modifications dans le système et leur application peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="62818-121">Once you've set up the permissions, it can take up to 60 minutes for the changes to propagate through the system and be in effect.</span></span>
  
 <span data-ttu-id="62818-122">**Comment utiliser une boîte aux lettres une fois les autorisations configurées :**</span><span class="sxs-lookup"><span data-stu-id="62818-122">**How to use it once permissions are set up:**</span></span>
  
<span data-ttu-id="62818-123">Lorsque vous avez reçu l’accès à une boîte aux lettres, plusieurs méthodes s’offrent à vous pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="62818-123">There are a few different ways you can access a mailbox once you've been given access.</span></span> <span data-ttu-id="62818-124">Pour obtenir de l’aide sur cette fonction, consultez cet article : [Accéder à la boîte aux lettres d’une autre personne](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081.aspx)</span><span class="sxs-lookup"><span data-stu-id="62818-124">For help on this, refer to this article: [Access another person's mailbox](https://support.office.com/article/Access-another-person-s-mailbox-A909AD30-E413-40B5-A487-0EA70B763081.aspx)</span></span>
  
## <a name="send-email-from-another-users-mailbox"></a><span data-ttu-id="62818-125">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-125">Send email from another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="62818-126">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-126">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="62818-127">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation d’envoi) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="62818-127">Select the name of the user (from whom you plan to give a sending permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="62818-128">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-128">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>

4. <span data-ttu-id="62818-129">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-129">Next to **Send as**, select **Edit**.</span></span> 

5. <span data-ttu-id="62818-130">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="62818-130">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
6. <span data-ttu-id="62818-131">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-131">Select **Save**.</span></span>
 
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="62818-132">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-132">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="62818-133">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-133">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="62818-134">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-134">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="62818-135">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="62818-135">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="62818-136">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-136">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="62818-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="62818-138">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-138">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="62818-139">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-139">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="62818-140">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="62818-140">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="62818-141">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-141">Select **Save**.</span></span>

::: moniker-end
  
## <a name="read-email-in-another-users-mailbox"></a><span data-ttu-id="62818-142">Lire du courrier dans la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-142">Read email in another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="62818-143">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-143">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="62818-144">Sélectionnez le nom de l’utilisateur (dont vous voulez autoriser la lecture de la boîte aux lettres) pour ouvrir son volet de propriétés.</span><span class="sxs-lookup"><span data-stu-id="62818-144">Select the name of the user (whose mailbox you want to allow to be read) to open their properties pane.</span></span>
    
3. <span data-ttu-id="62818-145">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-145">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="62818-146">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-146">Next to **Read and manage**, select **Edit**.</span></span> 
    
5. <span data-ttu-id="62818-147">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-147">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

6. <span data-ttu-id="62818-148">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-148">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="62818-149">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-149">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  
  
2. <span data-ttu-id="62818-150">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-150">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="62818-151">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-151">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="62818-152">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-152">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="62818-153">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-153">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="62818-154">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-154">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
  
2. <span data-ttu-id="62818-155">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-155">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="62818-156">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-156">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="62818-157">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-157">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="62818-158">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-158">Select **Save**.</span></span>

::: moniker-end


## <a name="send-email-on-behalf-of-another-user"></a><span data-ttu-id="62818-159">Envoyez du courrier de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="62818-159">Send email on behalf of another user</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="62818-160">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-160">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="62818-161">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation **Envoyer de la part de**) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="62818-161">Select the name of the user (from whom you plan to give a **Send on behalf** permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="62818-162">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-162">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="62818-163">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-163">Next to **Send on behalf**, select **Edit**.</span></span>

5. <span data-ttu-id="62818-164">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-164">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

6. <span data-ttu-id="62818-165">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-165">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="62818-166">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-166">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="62818-167">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-167">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="62818-168">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-168">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="62818-169">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-169">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="62818-170">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-170">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="62818-171">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="62818-171">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="62818-172">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="62818-172">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="62818-173">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="62818-173">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="62818-174">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="62818-174">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="62818-175">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="62818-175">Select **Save**.</span></span>

::: moniker-end


## <a name="send-and-read-from-outlook-and-outlook-on-the-web-for-business"></a><span data-ttu-id="62818-176">Envoyer et lire du courrier à partir d’Outlook et d’Outlook sur le web pour les clients professionnels</span><span class="sxs-lookup"><span data-stu-id="62818-176">Send and read from Outlook and Outlook on the web for business</span></span>


<span data-ttu-id="62818-177">Vous voulez savoir comment envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="62818-177">Want to know how to send email from another user's mailbox?</span></span> <span data-ttu-id="62818-178">Consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="62818-178">Check out the following topics:</span></span>
  
- [<span data-ttu-id="62818-179">Gérer les éléments de courrier et de calendrier d’une autre personne</span><span class="sxs-lookup"><span data-stu-id="62818-179">Manage another person's mail and calendar items</span></span>](https://support.office.com/article/afb79d6b-2967-43b9-a944-a6b953190af5.aspx)
    
- [<span data-ttu-id="62818-180">Envoyer du courrier pour le compte d’une autre personne ou d’un groupe</span><span class="sxs-lookup"><span data-stu-id="62818-180">Send email from another person or group</span></span>](https://support.office.com/article/0f4964af-aec6-484b-a65c-0434df8cdb6b.aspx)
