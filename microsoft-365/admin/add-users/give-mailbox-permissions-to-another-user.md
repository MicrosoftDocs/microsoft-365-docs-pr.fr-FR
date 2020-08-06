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
ms.openlocfilehash: 0b6977efbd6041a11c67ed66c9b7ecc72a38bde4
ms.sourcegitcommit: d988faa292c2661ffea43c7161aef92b2b4b99bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/04/2020
ms.locfileid: "46560374"
---
# <a name="give-mailbox-permissions-to-another-user---admin-help"></a><span data-ttu-id="984a7-104">Accorder des autorisations de boîte aux lettres à un autre utilisateur – Aide de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="984a7-104">Give mailbox permissions to another user - Admin Help</span></span>

<span data-ttu-id="984a7-105">En tant qu’administrateur, certaines exigences de votre entreprise vous entraînent à autoriser certains utilisateurs à accéder à la boîte aux lettres d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="984a7-105">As the admin, you may have company requirements to allow some users access to another user's mailbox.</span></span> <span data-ttu-id="984a7-106">Par exemple, vous souhaitez peut-être autoriser un assistant à envoyer ou à lire du courrier dans la boîte aux lettres de son responsable ou donner la possibilité à un de vos utilisateurs d’envoyer du courrier de la part d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="984a7-106">For example, you may want to enable an assistant to send or read email from their manager's mailbox, or one of your user's the ability to send email on behalf of another user.</span></span> <span data-ttu-id="984a7-107">Cette rubrique vous explique comment procéder pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="984a7-107">This topic shows you how to accomplish this.</span></span>
  
<span data-ttu-id="984a7-108">Si vous cherchez des informations concernant la création et la gestion de boîtes aux lettres partagées, consultez l’article [Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="984a7-108">If you're looking for information about creating and managing shared mailboxes, check out [Create a shared mailbox](../email/create-a-shared-mailbox.md).</span></span>
    
## <a name="looking-to-set-up-mailbox-permissions"></a><span data-ttu-id="984a7-109">Vous cherchez à configurer des autorisations de boîte aux lettres ?</span><span class="sxs-lookup"><span data-stu-id="984a7-109">Looking to set up mailbox permissions?</span></span>

<span data-ttu-id="984a7-p103">Les autorisations de boîte aux lettres vous permettent d’accorder un accès en lecture/écriture à une boîte aux lettres à un utilisateur autre que son propriétaire. L’article qui suit vous fournira les informations dont vous avez besoin pour configurer et utiliser cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="984a7-p103">Mailbox permissions allow you to give read/write access to a mailbox to another user. The articles below might give you the help you need to set up and use this feature:</span></span>
  
 <span data-ttu-id="984a7-112">**Configuration des autorisations :**</span><span class="sxs-lookup"><span data-stu-id="984a7-112">**Setting up the permissions:**</span></span>
  
<span data-ttu-id="984a7-113">pour configurer des autorisations, la première étape consiste à décider des actions que vous voulez autoriser l’autre utilisateur à pouvoir effectuer dans la boîte aux lettres donnée.</span><span class="sxs-lookup"><span data-stu-id="984a7-113">The first step to setting up permissions is deciding which actions you want to allow the other user to take in the given mailbox.</span></span> <span data-ttu-id="984a7-114">Vous pouvez autoriser un utilisateur à lire des courriers dans la boîte aux lettres, à envoyer des courriers de la part d’un autre utilisateur et à envoyer des courriers comme s’ils étaient envoyés à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-114">You can allow a user to read emails from the mailbox, send emails on behalf of another user, and send emails as if they were sent from that mailbox.</span></span> <span data-ttu-id="984a7-115">Consultez les articles suivants pour configurer chaque type d’autorisation :</span><span class="sxs-lookup"><span data-stu-id="984a7-115">Refer to the following articles on how to set up each type of permissions:</span></span>
  
- [<span data-ttu-id="984a7-116">Lire du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-116">Read email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#read-email-in-another-users-mailbox)
    
- [<span data-ttu-id="984a7-117">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-117">Send email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)

- [<span data-ttu-id="984a7-118">Envoyer un e-mail de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-118">Send email on behalf of another user</span></span>](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)
    
 <span data-ttu-id="984a7-119">**Propagation des modifications :**</span><span class="sxs-lookup"><span data-stu-id="984a7-119">**Changing propagation:**</span></span>
  
<span data-ttu-id="984a7-120">lorsque vous avez défini les autorisations, la propagation des modifications dans le système et leur application peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="984a7-120">Once you've set up the permissions, it can take up to 60 minutes for the changes to propagate through the system and be in effect.</span></span>
  
 <span data-ttu-id="984a7-121">**Comment utiliser une boîte aux lettres une fois les autorisations configurées :**</span><span class="sxs-lookup"><span data-stu-id="984a7-121">**How to use it once permissions are set up:**</span></span>
  
<span data-ttu-id="984a7-122">Lorsque vous avez reçu l’accès à une boîte aux lettres, plusieurs méthodes s’offrent à vous pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="984a7-122">There are a few different ways you can access a mailbox once you've been given access.</span></span> <span data-ttu-id="984a7-123">Pour obtenir de l’aide sur cette fonction, consultez cet article : [Accéder à la boîte aux lettres d’une autre personne](https://support.microsoft.com/office/A909AD30-E413-40B5-A487-0EA70B763081).</span><span class="sxs-lookup"><span data-stu-id="984a7-123">For help on this, refer to this article: [Access another person's mailbox](https://support.microsoft.com/office/A909AD30-E413-40B5-A487-0EA70B763081).</span></span>

> [!NOTE]
> <span data-ttu-id="984a7-124">Les autorisations peuvent être configurées uniquement dans le locataire actuel de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="984a7-124">The permissions can be set up only within the current organization tenant.</span></span> <span data-ttu-id="984a7-125">Il n’est pas possible de configurer des autorisations de boîte aux lettres pour les utilisateurs de locataire.</span><span class="sxs-lookup"><span data-stu-id="984a7-125">It is not possible to set up mailbox permissions with out of tenant users.</span></span>
  
## <a name="send-email-from-another-users-mailbox"></a><span data-ttu-id="984a7-126">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-126">Send email from another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="984a7-127">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-127">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="984a7-128">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation d’envoi) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="984a7-128">Select the name of the user (from whom you plan to give a sending permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="984a7-129">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-129">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>

4. <span data-ttu-id="984a7-130">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-130">Next to **Send as**, select **Edit**.</span></span> 

5. <span data-ttu-id="984a7-131">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="984a7-131">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
6. <span data-ttu-id="984a7-132">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-132">Select **Save**.</span></span>
 
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="984a7-133">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-133">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="984a7-134">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-134">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="984a7-135">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-135">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="984a7-136">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="984a7-136">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="984a7-137">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-137">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="984a7-138">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-138">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="984a7-139">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-139">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="984a7-140">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-140">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="984a7-141">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="984a7-141">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="984a7-142">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-142">Select **Save**.</span></span>

::: moniker-end
  
## <a name="read-email-in-another-users-mailbox"></a><span data-ttu-id="984a7-143">Lire du courrier dans la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-143">Read email in another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="984a7-144">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-144">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="984a7-145">Sélectionnez le nom de l’utilisateur (dont vous voulez autoriser la lecture de la boîte aux lettres) pour ouvrir son volet de propriétés.</span><span class="sxs-lookup"><span data-stu-id="984a7-145">Select the name of the user (whose mailbox you want to allow to be read) to open their properties pane.</span></span>
    
3. <span data-ttu-id="984a7-146">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-146">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="984a7-147">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-147">Next to **Read and manage**, select **Edit**.</span></span> 
    
5. <span data-ttu-id="984a7-148">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-148">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

6. <span data-ttu-id="984a7-149">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-149">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="984a7-150">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-150">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  
  
2. <span data-ttu-id="984a7-151">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-151">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="984a7-152">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-152">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="984a7-153">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-153">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="984a7-154">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-154">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="984a7-155">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-155">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
  
2. <span data-ttu-id="984a7-156">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-156">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="984a7-157">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-157">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="984a7-158">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-158">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="984a7-159">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-159">Select **Save**.</span></span>

::: moniker-end


## <a name="send-email-on-behalf-of-another-user"></a><span data-ttu-id="984a7-160">Envoyez du courrier de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="984a7-160">Send email on behalf of another user</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="984a7-161">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-161">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="984a7-162">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation **Envoyer de la part de**) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="984a7-162">Select the name of the user (from whom you plan to give a **Send on behalf** permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="984a7-163">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-163">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="984a7-164">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-164">Next to **Send on behalf**, select **Edit**.</span></span>

5. <span data-ttu-id="984a7-165">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-165">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

6. <span data-ttu-id="984a7-166">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-166">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="984a7-167">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-167">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="984a7-168">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-168">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="984a7-169">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-169">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="984a7-170">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-170">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="984a7-171">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-171">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="984a7-172">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="984a7-172">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="984a7-173">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="984a7-173">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="984a7-174">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="984a7-174">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="984a7-175">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="984a7-175">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="984a7-176">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="984a7-176">Select **Save**.</span></span>

::: moniker-end


## <a name="send-and-read-from-outlook-and-outlook-on-the-web-for-business"></a><span data-ttu-id="984a7-177">Envoyer et lire du courrier à partir d’Outlook et d’Outlook sur le web pour les clients professionnels</span><span class="sxs-lookup"><span data-stu-id="984a7-177">Send and read from Outlook and Outlook on the web for business</span></span>


<span data-ttu-id="984a7-178">Vous voulez savoir comment envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur ?</span><span class="sxs-lookup"><span data-stu-id="984a7-178">Want to know how to send email from another user's mailbox?</span></span> <span data-ttu-id="984a7-179">Consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="984a7-179">Check out the following topics:</span></span>
  
- [<span data-ttu-id="984a7-180">Gérer les éléments de courrier et de calendrier d’une autre personne</span><span class="sxs-lookup"><span data-stu-id="984a7-180">Manage another person's mail and calendar items</span></span>](https://support.microsoft.com/office/afb79d6b-2967-43b9-a944-a6b953190af5)
    
- [<span data-ttu-id="984a7-181">Envoyer du courrier pour le compte d’une autre personne ou d’un groupe</span><span class="sxs-lookup"><span data-stu-id="984a7-181">Send email from another person or group</span></span>](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b)
