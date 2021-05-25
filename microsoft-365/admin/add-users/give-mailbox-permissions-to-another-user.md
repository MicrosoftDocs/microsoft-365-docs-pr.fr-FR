---
title: Accorder des autorisations de boîte aux lettres à un autre utilisateur – Aide de l’administrateur
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 1dbcf12f-a9de-4d1d-b0b3-a227f8a736d8
description: Donner à un utilisateur le droit d'accéder à la boîte aux lettres d'un autre utilisateur, ce qui permet à l'utilisateur de lire et d'envoyer des courriels à partir de la boîte aux lettres de l'autre utilisateur.
ms.openlocfilehash: 0e5f7b154fa37ae9775e7208574b2a5395e7c239
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52634279"
---
# <a name="give-mailbox-permissions-to-another-user---admin-help"></a><span data-ttu-id="2b095-103">Accorder des autorisations de boîte aux lettres à un autre utilisateur – Aide de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="2b095-103">Give mailbox permissions to another user - Admin Help</span></span>

<span data-ttu-id="2b095-104">En tant qu’administrateur, certaines exigences de votre entreprise vous entraînent à autoriser certains utilisateurs à accéder à la boîte aux lettres d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b095-104">As the admin, you may have company requirements to allow some users access to another user's mailbox.</span></span> <span data-ttu-id="2b095-105">Par exemple, vous souhaitez peut-être autoriser un assistant à envoyer ou à lire du courrier dans la boîte aux lettres de son responsable ou donner la possibilité à un de vos utilisateurs d’envoyer du courrier de la part d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b095-105">For example, you may want to enable an assistant to send or read email from their manager's mailbox, or one of your user's the ability to send email on behalf of another user.</span></span> <span data-ttu-id="2b095-106">Cette rubrique vous explique comment procéder pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="2b095-106">This topic shows you how to accomplish this.</span></span>
  
<span data-ttu-id="2b095-107">Si vous cherchez des informations concernant la création et la gestion de boîtes aux lettres partagées, consultez l’article [Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="2b095-107">If you're looking for information about creating and managing shared mailboxes, check out [Create a shared mailbox](../email/create-a-shared-mailbox.md).</span></span>
    
## <a name="looking-to-set-up-mailbox-permissions"></a><span data-ttu-id="2b095-108">Vous cherchez à configurer des autorisations de boîte aux lettres ?</span><span class="sxs-lookup"><span data-stu-id="2b095-108">Looking to set up mailbox permissions?</span></span>

<span data-ttu-id="2b095-p102">Les autorisations de boîte aux lettres vous permettent d’accorder un accès en lecture/écriture à une boîte aux lettres à un utilisateur autre que son propriétaire. L’article qui suit vous fournira les informations dont vous avez besoin pour configurer et utiliser cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="2b095-p102">Mailbox permissions allow you to give read/write access to a mailbox to another user. The articles below might give you the help you need to set up and use this feature:</span></span>
  
 <span data-ttu-id="2b095-111">**Configuration des autorisations :**</span><span class="sxs-lookup"><span data-stu-id="2b095-111">**Setting up the permissions:**</span></span>
  
<span data-ttu-id="2b095-112">pour configurer des autorisations, la première étape consiste à décider des actions que vous voulez autoriser l’autre utilisateur à pouvoir effectuer dans la boîte aux lettres donnée.</span><span class="sxs-lookup"><span data-stu-id="2b095-112">The first step to setting up permissions is deciding which actions you want to allow the other user to take in the given mailbox.</span></span> <span data-ttu-id="2b095-113">Vous pouvez autoriser un utilisateur à lire des courriers dans la boîte aux lettres, à envoyer des courriers de la part d’un autre utilisateur et à envoyer des courriers comme s’ils étaient envoyés à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-113">You can allow a user to read emails from the mailbox, send emails on behalf of another user, and send emails as if they were sent from that mailbox.</span></span> <span data-ttu-id="2b095-114">Consultez les articles suivants pour configurer chaque type d’autorisation :</span><span class="sxs-lookup"><span data-stu-id="2b095-114">Refer to the following articles on how to set up each type of permissions:</span></span>
  
- [<span data-ttu-id="2b095-115">Lire du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-115">Read email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#read-email-in-another-users-mailbox)
    
- [<span data-ttu-id="2b095-116">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-116">Send email from another user's mailbox</span></span>](give-mailbox-permissions-to-another-user.md#send-email-from-another-users-mailbox)

- [<span data-ttu-id="2b095-117">Envoyer un e-mail de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-117">Send email on behalf of another user</span></span>](give-mailbox-permissions-to-another-user.md#send-email-on-behalf-of-another-user)
    
 <span data-ttu-id="2b095-118">**Propagation des modifications :**</span><span class="sxs-lookup"><span data-stu-id="2b095-118">**Changing propagation:**</span></span>
  
<span data-ttu-id="2b095-119">lorsque vous avez défini les autorisations, la propagation des modifications dans le système et leur application peut prendre jusqu’à 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="2b095-119">Once you've set up the permissions, it can take up to 60 minutes for the changes to propagate through the system and be in effect.</span></span>
  
 <span data-ttu-id="2b095-120">**Comment utiliser une boîte aux lettres une fois les autorisations configurées :**</span><span class="sxs-lookup"><span data-stu-id="2b095-120">**How to use it once permissions are set up:**</span></span>
  
<span data-ttu-id="2b095-121">Lorsque vous avez reçu l’accès à une boîte aux lettres, plusieurs méthodes s’offrent à vous pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="2b095-121">There are a few different ways you can access a mailbox once you've been given access.</span></span> <span data-ttu-id="2b095-122">Pour obtenir de l’aide sur cette fonction, consultez cet article : [Accéder à la boîte aux lettres d’une autre personne](https://support.microsoft.com/office/A909AD30-E413-40B5-A487-0EA70B763081).</span><span class="sxs-lookup"><span data-stu-id="2b095-122">For help on this, refer to this article: [Access another person's mailbox](https://support.microsoft.com/office/A909AD30-E413-40B5-A487-0EA70B763081).</span></span>

> [!NOTE]
> <span data-ttu-id="2b095-123">Les autorisations peuvent être configurées uniquement dans le locataire actuel de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2b095-123">The permissions can be set up only within the current organization tenant.</span></span> <span data-ttu-id="2b095-124">Il n’est pas possible de configurer des autorisations de boîte aux lettres pour les utilisateurs de locataire.</span><span class="sxs-lookup"><span data-stu-id="2b095-124">It is not possible to set up mailbox permissions with out of tenant users.</span></span>
  
## <a name="send-email-from-another-users-mailbox"></a><span data-ttu-id="2b095-125">Envoyer du courrier à partir de la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-125">Send email from another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2b095-126">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-126">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="2b095-127">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation d’envoi) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b095-127">Select the name of the user (from whom you plan to give a sending permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="2b095-128">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-128">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>

4. <span data-ttu-id="2b095-129">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-129">Next to **Send as**, select **Edit**.</span></span> 

5. <span data-ttu-id="2b095-130">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="2b095-130">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
6. <span data-ttu-id="2b095-131">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-131">Select **Save**.</span></span>
 
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2b095-132">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-132">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="2b095-133">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-133">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="2b095-134">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-134">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="2b095-135">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="2b095-135">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="2b095-136">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-136">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2b095-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="2b095-138">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-138">Select the user you want, expand **Mail Settings**, and then Select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="2b095-139">À côté de **Envoyer en tant que**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-139">Next to **Send as**, select **Edit**.</span></span> 

4. <span data-ttu-id="2b095-140">Sélectionnez **Ajouter des autorisations**, puis choisissez le nom de la personne à laquelle vous voulez que cet utilisateur puisse Envoyer en tant que.</span><span class="sxs-lookup"><span data-stu-id="2b095-140">Select **Add permissions**, then choose the name of the person who you want this user to be able to send as.</span></span> 
    
5. <span data-ttu-id="2b095-141">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-141">Select **Save**.</span></span>

::: moniker-end
  
## <a name="read-email-in-another-users-mailbox"></a><span data-ttu-id="2b095-142">Lire du courrier dans la boîte aux lettres d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-142">Read email in another user's mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2b095-143">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-143">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  
    
2. <span data-ttu-id="2b095-144">Sélectionnez le nom de l’utilisateur (dont vous voulez autoriser la lecture de la boîte aux lettres) pour ouvrir son volet de propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b095-144">Select the name of the user (whose mailbox you want to allow to be read) to open their properties pane.</span></span>
    
3. <span data-ttu-id="2b095-145">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-145">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="2b095-146">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-146">Next to **Read and manage**, select **Edit**.</span></span> 
    
5. <span data-ttu-id="2b095-147">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-147">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

6. <span data-ttu-id="2b095-148">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-148">Select **Save**.</span></span>


> [!NOTE]
> <span data-ttu-id="2b095-149">Les autorisations **Lecture** et **Gestion** sont appelées autorisations **Accès complet** lorsqu’elles sont accordées dans le centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="2b095-149">**Read** and **Manage** permissions are called **Full Access** permission when granted in the Exchange admin center.</span></span> <span data-ttu-id="2b095-150">L’autorisation Accès complet n’octroie pas les autorisations **Envoyer en tant que** ou **Envoyer de la part de**.</span><span class="sxs-lookup"><span data-stu-id="2b095-150">Full Access permission does not grant **Send as** or **Send on Behalf**  permissions.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2b095-151">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-151">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  
  
2. <span data-ttu-id="2b095-152">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-152">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="2b095-153">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-153">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="2b095-154">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-154">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="2b095-155">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-155">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2b095-156">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-156">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 
  
2. <span data-ttu-id="2b095-157">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-157">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>
    
3. <span data-ttu-id="2b095-158">À côté de **Lire et gérer**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-158">Next to **Read and manage**, select **Edit**.</span></span> 
    
4. <span data-ttu-id="2b095-159">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à lire du courrier à partir de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-159">Select **Add permissions**, then choose the name of the user or users that you want to allow to read email from this mailbox.</span></span>

5. <span data-ttu-id="2b095-160">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-160">Select **Save**.</span></span>

::: moniker-end


## <a name="send-email-on-behalf-of-another-user"></a><span data-ttu-id="2b095-161">Envoyez du courrier de la part d’un autre utilisateur</span><span class="sxs-lookup"><span data-stu-id="2b095-161">Send email on behalf of another user</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="2b095-162">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-162">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="2b095-163">Sélectionnez le nom de l’utilisateur (auquel vous envisagez d’accorder une autorisation **Envoyer de la part de**) pour ouvrir le volet de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b095-163">Select the name of the user (from whom you plan to give a **Send on behalf** permission) to open their properties pane.</span></span>
    
3. <span data-ttu-id="2b095-164">Sous l’onglet **Courrier**, sélectionnez **Gérer les autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-164">On the **Mail** tab, select **Manage mailbox permissions**.</span></span>
    
4. <span data-ttu-id="2b095-165">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-165">Next to **Send on behalf**, select **Edit**.</span></span>

5. <span data-ttu-id="2b095-166">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-166">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

6. <span data-ttu-id="2b095-167">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-167">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="2b095-168">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-168">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="2b095-169">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-169">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="2b095-170">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-170">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="2b095-171">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-171">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="2b095-172">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-172">Select **Save**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="2b095-173">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="2b095-173">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span> 

2. <span data-ttu-id="2b095-174">Sélectionnez l’utilisateur souhaité, développez les **Paramètres de courrier**, puis sélectionnez **Modifier** à côté des **Autorisations de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="2b095-174">Select the user you want, expand **Mail Settings**, and then select **Edit** next to **Mailbox permissions**.</span></span>

3. <span data-ttu-id="2b095-175">À côté de **Envoyer de la part de**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="2b095-175">Next to **Send on behalf**, select **Edit**.</span></span>
    
4. <span data-ttu-id="2b095-176">Sélectionnez **Ajouter des autorisations**, puis entrez le nom de l’utilisateur ou des utilisateurs que vous souhaitez autoriser à envoyer du courrier pour le compte de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2b095-176">Select **Add permissions**, then choose the name of the user or users that you want to allow to send email on behalf of this mailbox.</span></span>

5. <span data-ttu-id="2b095-177">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="2b095-177">Select **Save**.</span></span>

::: moniker-end


## <a name="related-content"></a><span data-ttu-id="2b095-178">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="2b095-178">Related content</span></span>
  
<span data-ttu-id="2b095-179">[Gérer les éléments du courrier et du calendrier d'une autre personne](https://support.microsoft.com/office/afb79d6b-2967-43b9-a944-a6b953190af5) (article)</span><span class="sxs-lookup"><span data-stu-id="2b095-179">[Manage another person's mail and calendar items](https://support.microsoft.com/office/afb79d6b-2967-43b9-a944-a6b953190af5) (article)</span></span>\   
<span data-ttu-id="2b095-180">[Envoyer un e-mail d'une autre personne ou d'un groupe](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b) (article)</span><span class="sxs-lookup"><span data-stu-id="2b095-180">[Send email from another person or group](https://support.microsoft.com/office/0f4964af-aec6-484b-a65c-0434df8cdb6b) (article)</span></span>\
<span data-ttu-id="2b095-181">[Modifier un nom d'utilisateur et une adresse électronique ](../add-users/change-a-user-name-and-email-address.md)(vidéo)</span><span class="sxs-lookup"><span data-stu-id="2b095-181">[Change a user name and email address](../add-users/change-a-user-name-and-email-address.md) (video)</span></span>

