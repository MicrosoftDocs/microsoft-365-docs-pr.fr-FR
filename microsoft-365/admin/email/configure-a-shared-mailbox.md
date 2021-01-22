---
title: Configurer les paramètres de boîte aux lettres partagée
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
description: Une fois que vous avez créé une boîte aux lettres partagée, vous pouvez configurer certains paramètres pour ses utilisateurs, tels que le forwarding des messages électroniques et les réponses automatiques. Par la suite, vous pouvez modifier d’autres paramètres, tels que le nom ou les membres de la boîte aux lettres.
ms.openlocfilehash: fe5d35be556b8edf5456bc2c0b820dc0ce77e323
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49926605"
---
# <a name="configure-shared-mailbox-settings"></a><span data-ttu-id="1e38a-104">Configurer les paramètres de boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-104">Configure shared mailbox settings</span></span>

<span data-ttu-id="1e38a-105">Une fois que vous [avez](create-a-shared-mailbox.md)créé une boîte aux lettres partagée, vous pouvez configurer certains paramètres pour les utilisateurs de la boîte aux lettres, tels que le forwarding des messages électroniques et les réponses automatiques.</span><span class="sxs-lookup"><span data-stu-id="1e38a-105">After you have [created a shared mailbox](create-a-shared-mailbox.md), you'll want to configure some settings for the mailbox users, such as email forwarding and automatic replies.</span></span> <span data-ttu-id="1e38a-106">Par la suite, vous pouvez modifier d’autres paramètres, tels que le nom de la boîte aux lettres, les membres ou les autorisations des membres.</span><span class="sxs-lookup"><span data-stu-id="1e38a-106">Later, you might want to change other settings, such as the mailbox name, members, or member permissions.</span></span> 

## <a name="change-the-name-or-email-alias-of-a-shared-mailbox-or-change-the-primary-email-address"></a><span data-ttu-id="1e38a-107">Modifier le nom ou l’alias de messagerie d’une boîte aux lettres partagée ou modifier l’adresse de messagerie principale</span><span class="sxs-lookup"><span data-stu-id="1e38a-107">Change the name or email alias of a shared mailbox, or change the primary email address</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-108">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-108">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-109">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-109">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-110">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-110">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-111">Sélectionnez la boîte aux lettres partagée que vous souhaitez modifier, puis sélectionnez **Modifier** en plus du nom, de la messagerie, des **alias de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-111">Select the shared mailbox you want to edit, and then select **Edit** next to **Name, Email, Email aliases**.</span></span>

3. <span data-ttu-id="1e38a-112">Entrez un nouveau nom ou ajoutez un autre alias.</span><span class="sxs-lookup"><span data-stu-id="1e38a-112">Enter a new name, or add another alias.</span></span> <span data-ttu-id="1e38a-113">Si vous souhaitez modifier l’adresse de messagerie principale, votre boîte aux lettres doit avoir plusieurs alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1e38a-113">If you want to change the primary email address, your mailbox must have more than one email alias.</span></span>

4. <span data-ttu-id="1e38a-114">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-114">Select **Save**.</span></span>

## <a name="forward-emails-that-are-sent-to-a-shared-mailbox"></a><span data-ttu-id="1e38a-115">Transférer des courriers qui sont envoyés à une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-115">Forward emails that are sent to a shared mailbox</span></span>

<span data-ttu-id="1e38a-116">Il n’est pas nécessaire d’attribuer une licence à la boîte aux lettres partagée pour pouvoir envoyer le courrier électronique qui lui est envoyé.</span><span class="sxs-lookup"><span data-stu-id="1e38a-116">You do not need to assign a license to the shared mailbox in order to forward email that's sent to it.</span></span> <span data-ttu-id="1e38a-117">Vous pouvez envoyer les messages à n’importe quelle adresse de messagerie ou liste de distribution valide.</span><span class="sxs-lookup"><span data-stu-id="1e38a-117">You can forward the messages to any valid email address or distribution list.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-118">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-118">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-119">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-119">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-120">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-120">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-121">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier le courrier** \> **électronique.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-121">Select the shared mailbox you want to edit, then select **Email forwarding** \> **Edit**.</span></span>
    
3. <span data-ttu-id="1e38a-122">Définissez le basculement sur **Sur,** puis entrez une adresse de messagerie à qui les messages sont transmis.</span><span class="sxs-lookup"><span data-stu-id="1e38a-122">Set the toggle to **On**, and enter one email address to forward the messages to.</span></span> <span data-ttu-id="1e38a-123">Il peut s’y trouver n’importe quelle adresse de messagerie valide.</span><span class="sxs-lookup"><span data-stu-id="1e38a-123">It can be any valid email address.</span></span> <span data-ttu-id="1e38a-124">Pour le faire, vous devez créer un groupe de [distribution](https://docs.microsoft.com/office365/admin/setup/create-distribution-lists) pour les adresses, puis entrer le nom du groupe dans cette zone.</span><span class="sxs-lookup"><span data-stu-id="1e38a-124">To forward to multiple addresses, you need to [create a distribution group](https://docs.microsoft.com/office365/admin/setup/create-distribution-lists) for the addresses, and then enter the name of the group in this box.</span></span>
    
4. <span data-ttu-id="1e38a-125">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-125">Select **Save**.</span></span>

## <a name="send-automatic-replies-from-a-shared-mailbox"></a><span data-ttu-id="1e38a-126">Envoyer des réponses automatiques à partir d'une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-126">Send automatic replies from a shared mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-127">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-127">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-128">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-128">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-129">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-129">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-130">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier les réponses automatiques.** \> </span><span class="sxs-lookup"><span data-stu-id="1e38a-130">Select the shared mailbox you want to edit, then select **Automatic replies** \> **Edit**.</span></span>
    
3. <span data-ttu-id="1e38a-131">Définissez le basculement sur **Sur** et choisissez d’envoyer la réponse à des personnes à l’intérieur de votre organisation ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e38a-131">Set the toggle to **On**, and choose whether to send the reply to people inside your organization or outside your organization.</span></span>

4. <span data-ttu-id="1e38a-132">Entrez la réponse que vous voulez envoyer aux personnes internes à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e38a-132">Enter the reply you want to send to people inside your organization.</span></span> <span data-ttu-id="1e38a-133">Vous ne pouvez pas ajouter d'images, seulement du texte.</span><span class="sxs-lookup"><span data-stu-id="1e38a-133">You can't add images, only text.</span></span>

5. <span data-ttu-id="1e38a-134">Si vous souhaitez *également* envoyer une réponse à des personnes extérieures à votre organisation, cochez la case, qui vous souhaitez obtenir la réponse, puis tapez le texte.</span><span class="sxs-lookup"><span data-stu-id="1e38a-134">If you want to *also* send a reply to people outside your organization, select the check box, who you want to get the reply, and type the text.</span></span> <span data-ttu-id="1e38a-135">Vous ne pouvez pas envoyer la réponse uniquement à des personnes externes à votre organisation sans l'envoyer à des personnes internes à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e38a-135">There's no way to only send to people outside your organization but not to people inside your organization.</span></span>

6. <span data-ttu-id="1e38a-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-136">Select **Save**.</span></span>

## <a name="allow-everyone-to-see-the-sent-email-the-replies"></a><span data-ttu-id="1e38a-137">Autoriser tout le monde à voir le courrier envoyé (les réponses)</span><span class="sxs-lookup"><span data-stu-id="1e38a-137">Allow everyone to see the Sent email (the replies)</span></span>

<span data-ttu-id="1e38a-p108">Par défaut, les courriers envoyés à partir de la boîte aux lettres partagée ne sont pas enregistrés dans le dossier Éléments envoyés de la boîte aux lettres partagée. En revanche, ils sont enregistrés dans le dossier Éléments envoyés de la personne qui a envoyé le courrier.</span><span class="sxs-lookup"><span data-stu-id="1e38a-p108">By default, messages sent from the shared mailbox aren't saved to the Sent Items folder of the shared mailbox. Instead, they are saved to the Sent Items folder of the person who sent the message.</span></span>

<span data-ttu-id="1e38a-140">Si vous souhaitez autoriser tout le monde à voir le courrier envoyé, dans le centre d’administration, modifiez les paramètres de boîte aux lettres partagée, puis sélectionnez **Éléments envoyés** \> **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-140">If you want to allow everyone to see the Sent email, in the admin center, edit the shared mailbox settings, and select **Sent items** \> **Edit**.</span></span>


## <a name="choose-the-apps-that-a-shared-mailbox-can-use-to-access-microsoft-email"></a><span data-ttu-id="1e38a-141">Choisir les applications qu’une boîte aux lettres partagée peut utiliser pour accéder à la messagerie électronique Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e38a-141">Choose the apps that a shared mailbox can use to access Microsoft email</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-142">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-142">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-143">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-143">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-144">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-144">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-145">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier les applications de** \> **messagerie.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-145">Select the shared mailbox you want to edit, then select **Email apps** \> **Edit**.</span></span>

3. <span data-ttu-id="1e38a-146">Définissez le basculement sur **Sur pour** toutes les applications que vous souhaitez que les membres puissent utiliser pour accéder à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="1e38a-146">Set the toggle to **On** for all of the apps you want members to be able to use to access the shared mailbox.</span></span> <span data-ttu-id="1e38a-147">Définissez le basculement sur **Off** pour toutes les applications que vous ne souhaitez pas qu’elles utilisent.</span><span class="sxs-lookup"><span data-stu-id="1e38a-147">Set the toggle to **Off** for any apps you don't want them to use.</span></span> 

4. <span data-ttu-id="1e38a-148">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-148">Select **Save**.</span></span>


## <a name="put-a-shared-mailbox-on-litigation-hold"></a><span data-ttu-id="1e38a-149">Placer une boîte aux lettres partagée en attente pour litige</span><span class="sxs-lookup"><span data-stu-id="1e38a-149">Put a shared mailbox on litigation hold</span></span>

<span data-ttu-id="1e38a-150">Pour en savoir plus sur la attente pour litige, voir [Créer une attente pour litige.](https://docs.microsoft.com/microsoft-365/compliance/create-a-litigation-hold)</span><span class="sxs-lookup"><span data-stu-id="1e38a-150">To learn more about litigation hold, see [Create a Litigation Hold](https://docs.microsoft.com/microsoft-365/compliance/create-a-litigation-hold).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-151">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-151">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-152">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-152">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-153">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-153">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-154">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier la mise en attente pour** \> **litige.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-154">Select the shared mailbox you want to edit, then select **Litigation hold** \> **Edit**.</span></span>

3. <span data-ttu-id="1e38a-155">Définissez le basculement sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-155">Set the toggle to **On**.</span></span> 

4. <span data-ttu-id="1e38a-156">Vous pourz éventuellement entrer une durée, une note sur la attente et une URL avec plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1e38a-156">Optionally, enter a duration, s note about the hold, and a URL with more information.</span></span>  

5. <span data-ttu-id="1e38a-157">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-157">Select **Save**.</span></span>


## <a name="add-or-remove-members"></a><span data-ttu-id="1e38a-158">Ajouter ou supprimer des membres</span><span class="sxs-lookup"><span data-stu-id="1e38a-158">Add or remove members</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-159">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-159">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-160">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-160">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-161">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-161">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-162">Sélectionnez la boîte aux lettres  partagée que vous souhaitez modifier, puis sélectionnez \> **Modifier les membres.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-162">Select the shared mailbox you want to edit, then select **Members** \> **Edit**.</span></span>

3. <span data-ttu-id="1e38a-163">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e38a-163">Do one of the following:</span></span>
   - <span data-ttu-id="1e38a-164">Pour ajouter des membres, **sélectionnez Ajouter des membres,** recherchez ou sélectionnez un membre à ajouter, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-164">To add members, select **Add members**, search for or select a member to add, and then select **Save**.</span></span>
   - <span data-ttu-id="1e38a-165">Pour supprimer des membres, utilisez la zone de recherche pour rechercher le membre si nécessaire, sélectionnez **le X** en côté du nom du membre, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-165">To remove members, use the Search box to search for the member if necessary, select the **X** next to the member's name, and then select **Save**.</span></span> 

4. <span data-ttu-id="1e38a-166">Sélectionnez **Enregistrer à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="1e38a-166">Select **Save** again.</span></span>

## <a name="add-or-remove-permissions-of-members"></a><span data-ttu-id="1e38a-167">Ajouter ou supprimer des autorisations de membres</span><span class="sxs-lookup"><span data-stu-id="1e38a-167">Add or remove permissions of members</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-168">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-168">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-169">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-169">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-170">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-170">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-171">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Personnaliser** \> **les autorisations des membres.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-171">Select the shared mailbox you want to edit, then select **Members** \> **Customize permissions**.</span></span>

3. <span data-ttu-id="1e38a-172">Sélectionnez **Modifier** en plus de l’autorisation que vous souhaitez modifier pour un membre.</span><span class="sxs-lookup"><span data-stu-id="1e38a-172">Select **Edit** next to the permission you want to change for a member.</span></span> 

4. <span data-ttu-id="1e38a-173">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e38a-173">Do one of the following:</span></span>
   - <span data-ttu-id="1e38a-174">Pour accorder cette autorisation à un membre supplémentaire, sélectionnez Ajouter des **autorisations,** recherchez ou sélectionnez un membre à ajouter, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-174">To give that permission to an additional member, select **Add permissions**, search for or select a member to add, and then select **Save**.</span></span>
   - <span data-ttu-id="1e38a-175">Pour supprimer l’autorisation d’un membre, utilisez la zone De recherche pour rechercher le membre si nécessaire, sélectionnez **le X** en de côté du nom du membre, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-175">To remove the permission from a member, use the Search box to search for the member if necessary,  select the **X** next to the member's name, and then select **Save**.</span></span> 

4. <span data-ttu-id="1e38a-176">Sélectionnez **Enregistrer à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="1e38a-176">Select **Save** again.</span></span>

## <a name="show-or-hide-a-shared-mailbox-in-the-global-address-list"></a><span data-ttu-id="1e38a-177">Afficher ou masquer une boîte aux lettres partagée dans la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="1e38a-177">Show or hide a shared mailbox in the global address list</span></span>

<span data-ttu-id="1e38a-178">Si vous choisissez de ne pas afficher la boîte aux lettres partagée dans la liste d’adresses globale, la boîte aux lettres n’apparaîtra pas dans la liste d’adresses de votre organisation, mais elle recevra toujours des messages électroniques qui lui seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="1e38a-178">If you choose not to show the shared mailbox in the global address list, the mailbox won't appear in your organization's address list, but it will still receive email sent to it.</span></span> 

::: moniker range="o365-worldwide"

1. <span data-ttu-id="1e38a-179">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="1e38a-179">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end 

::: moniker range="o365-germany"

1. <span data-ttu-id="1e38a-180">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-180">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="1e38a-181">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **Groupes** > **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-181">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Groups** > **Shared mailboxes** page.</span></span> 

::: moniker-end

2. <span data-ttu-id="1e38a-182">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Afficher dans la liste d’adresses globale** \> **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="1e38a-182">Select the shared mailbox you want to edit, then select **Show in global address list** \> **Edit**.</span></span>

3. <span data-ttu-id="1e38a-183">Définissez le basculement sur **On**  ou **Off**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-183">Set the toggle to **On**  or **Off**.</span></span> 

4. <span data-ttu-id="1e38a-184">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1e38a-184">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="1e38a-185">Masquer une boîte aux lettres partagée dans la liste d’adresses empêche les nouveaux membres de la boîte aux lettres partagée d’ajouter la boîte aux lettres masquée à leur profil Outlook tant que la boîte aux lettres partagée n’est pas de nouveau affichée dans la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="1e38a-185">Hiding a shared mailbox from address list will make it impossible for new shared mailbox members to add the hidden mailbox to their Outlook profile until the shared mailbox is again shown in the address list.</span></span> 

## <a name="related-articles"></a><span data-ttu-id="1e38a-186">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="1e38a-186">Related articles</span></span>

[<span data-ttu-id="1e38a-187">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="1e38a-187">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="1e38a-188">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-188">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="1e38a-189">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-189">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="1e38a-190">Supprimer une licence à partir d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="1e38a-190">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)

[<span data-ttu-id="1e38a-191">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="1e38a-191">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
