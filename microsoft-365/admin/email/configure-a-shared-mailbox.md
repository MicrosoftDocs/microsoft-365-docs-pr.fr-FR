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
search.appverid:
- BCS160
- MET150
- MOE150
description: Créez une boîte aux lettres partagée et configurez certains paramètres pour ses utilisateurs, tels que le forwarding de courrier électronique et les réponses automatiques.
ms.openlocfilehash: c1d8007a2fcc45fbdd1a6943ee464e5aae8917b9
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635509"
---
# <a name="configure-shared-mailbox-settings"></a><span data-ttu-id="dbbb3-103">Configurer les paramètres de boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dbbb3-103">Configure shared mailbox settings</span></span>

<span data-ttu-id="dbbb3-104">Une fois que vous [avez](create-a-shared-mailbox.md)créé une boîte aux lettres partagée, vous souhaiterez configurer certains paramètres pour les utilisateurs de la boîte aux lettres, tels que le forwarding des messages électroniques et les réponses automatiques.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-104">After you have [created a shared mailbox](create-a-shared-mailbox.md), you'll want to configure some settings for the mailbox users, such as email forwarding and automatic replies.</span></span> <span data-ttu-id="dbbb3-105">Par la suite, vous pouvez modifier d’autres paramètres, tels que le nom de la boîte aux lettres, les membres ou les autorisations des membres.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-105">Later, you might want to change other settings, such as the mailbox name, members, or member permissions.</span></span> 

## <a name="change-the-name-or-email-alias-of-a-shared-mailbox-or-change-the-primary-email-address"></a><span data-ttu-id="dbbb3-106">Modifier le nom ou l’alias de messagerie d’une boîte aux lettres partagée ou modifier l’adresse de messagerie principale</span><span class="sxs-lookup"><span data-stu-id="dbbb3-106">Change the name or email alias of a shared mailbox, or change the primary email address</span></span>

1. <span data-ttu-id="dbbb3-107">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-107">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-108">Sélectionnez la boîte aux lettres partagée que vous souhaitez modifier, puis sélectionnez **Modifier** en plus du nom, de la messagerie, des **alias de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-108">Select the shared mailbox you want to edit, and then select **Edit** next to **Name, Email, Email aliases**.</span></span>

3. <span data-ttu-id="dbbb3-109">Entrez un nouveau nom ou ajoutez un autre alias.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-109">Enter a new name, or add another alias.</span></span> <span data-ttu-id="dbbb3-110">Si vous souhaitez modifier l’adresse de messagerie principale, votre boîte aux lettres doit avoir plusieurs alias de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-110">If you want to change the primary email address, your mailbox must have more than one email alias.</span></span>

4. <span data-ttu-id="dbbb3-111">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-111">Select **Save**.</span></span>

## <a name="forward-emails-that-are-sent-to-a-shared-mailbox"></a><span data-ttu-id="dbbb3-112">Transférer des courriers qui sont envoyés à une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dbbb3-112">Forward emails that are sent to a shared mailbox</span></span>

<span data-ttu-id="dbbb3-113">Il n’est pas nécessaire d’attribuer une licence à la boîte aux lettres partagée pour pouvoir envoyer le courrier électronique qui lui est envoyé.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-113">You do not need to assign a license to the shared mailbox in order to forward email that's sent to it.</span></span> <span data-ttu-id="dbbb3-114">Vous pouvez envoyer les messages à n’importe quelle adresse de messagerie ou liste de distribution valide.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-114">You can forward the messages to any valid email address or distribution list.</span></span>

1. <span data-ttu-id="dbbb3-115">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-115">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-116">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier le courrier** \> **électronique.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-116">Select the shared mailbox you want to edit, then select **Email forwarding** \> **Edit**.</span></span>
    
3. <span data-ttu-id="dbbb3-117">Définissez le basculement sur **Sur,** puis entrez une adresse de messagerie à qui les messages sont transmis.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-117">Set the toggle to **On**, and enter one email address to forward the messages to.</span></span> <span data-ttu-id="dbbb3-118">Il peut s’y trouver n’importe quelle adresse de messagerie valide.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-118">It can be any valid email address.</span></span> <span data-ttu-id="dbbb3-119">Pour le faire, vous devez créer un groupe de [distribution](/office365/admin/setup/create-distribution-lists) pour les adresses, puis entrer le nom du groupe dans cette zone.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-119">To forward to multiple addresses, you need to [create a distribution group](/office365/admin/setup/create-distribution-lists) for the addresses, and then enter the name of the group in this box.</span></span>
    
4. <span data-ttu-id="dbbb3-120">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-120">Select **Save**.</span></span>

## <a name="send-automatic-replies-from-a-shared-mailbox"></a><span data-ttu-id="dbbb3-121">Envoyer des réponses automatiques à partir d'une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dbbb3-121">Send automatic replies from a shared mailbox</span></span>

1. <span data-ttu-id="dbbb3-122">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-122">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-123">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier les réponses automatiques.** \> </span><span class="sxs-lookup"><span data-stu-id="dbbb3-123">Select the shared mailbox you want to edit, then select **Automatic replies** \> **Edit**.</span></span>
    
3. <span data-ttu-id="dbbb3-124">Définissez le basculement sur **Sur** et choisissez d’envoyer la réponse à des personnes à l’intérieur de votre organisation ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-124">Set the toggle to **On**, and choose whether to send the reply to people inside your organization or outside your organization.</span></span>

4. <span data-ttu-id="dbbb3-p105">Entrez la réponse que vous voulez envoyer aux personnes internes à votre organisation. Vous ne pouvez pas ajouter d'images, seulement du texte.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-p105">Enter the reply you want to send to people inside your organization. You can't add images, only text.</span></span>

5. <span data-ttu-id="dbbb3-127">Si vous *souhaitez* également envoyer une réponse à des personnes extérieures à votre organisation, cochez la case, qui vous souhaitez obtenir la réponse, puis tapez le texte.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-127">If you want to *also* send a reply to people outside your organization, select the check box, who you want to get the reply, and type the text.</span></span> <span data-ttu-id="dbbb3-128">Vous ne pouvez pas envoyer la réponse uniquement à des personnes externes à votre organisation sans l'envoyer à des personnes internes à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-128">There's no way to only send to people outside your organization but not to people inside your organization.</span></span>

6. <span data-ttu-id="dbbb3-129">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-129">Select **Save**.</span></span>

## <a name="allow-everyone-to-see-the-sent-email-the-replies"></a><span data-ttu-id="dbbb3-130">Autoriser tout le monde à voir le courrier envoyé (les réponses)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-130">Allow everyone to see the Sent email (the replies)</span></span>

<span data-ttu-id="dbbb3-p107">Par défaut, les courriers envoyés à partir de la boîte aux lettres partagée ne sont pas enregistrés dans le dossier Éléments envoyés de la boîte aux lettres partagée. En revanche, ils sont enregistrés dans le dossier Éléments envoyés de la personne qui a envoyé le courrier.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-p107">By default, messages sent from the shared mailbox aren't saved to the Sent Items folder of the shared mailbox. Instead, they are saved to the Sent Items folder of the person who sent the message.</span></span>

<span data-ttu-id="dbbb3-133">Si vous souhaitez autoriser tout le monde à voir le courrier envoyé, dans le centre d’administration, modifiez les paramètres de boîte aux lettres partagée, puis sélectionnez **Éléments envoyés** \> **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-133">If you want to allow everyone to see the Sent email, in the admin center, edit the shared mailbox settings, and select **Sent items** \> **Edit**.</span></span>


## <a name="choose-the-apps-that-a-shared-mailbox-can-use-to-access-microsoft-email"></a><span data-ttu-id="dbbb3-134">Choisir les applications qu’une boîte aux lettres partagée peut utiliser pour accéder à la messagerie électronique Microsoft</span><span class="sxs-lookup"><span data-stu-id="dbbb3-134">Choose the apps that a shared mailbox can use to access Microsoft email</span></span>

1. <span data-ttu-id="dbbb3-135">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-135">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-136">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier les applications de** \> **messagerie.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-136">Select the shared mailbox you want to edit, then select **Email apps** \> **Edit**.</span></span>

3. <span data-ttu-id="dbbb3-137">Définissez le basculement sur **Sur pour** toutes les applications que vous souhaitez que les membres puissent utiliser pour accéder à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-137">Set the toggle to **On** for all of the apps you want members to be able to use to access the shared mailbox.</span></span> <span data-ttu-id="dbbb3-138">Définissez le basculement sur **Off** pour toutes les applications que vous ne souhaitez pas qu’elles utilisent.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-138">Set the toggle to **Off** for any apps you don't want them to use.</span></span> 

4. <span data-ttu-id="dbbb3-139">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-139">Select **Save**.</span></span>


## <a name="put-a-shared-mailbox-on-litigation-hold"></a><span data-ttu-id="dbbb3-140">Placer une boîte aux lettres partagée en attente pour litige</span><span class="sxs-lookup"><span data-stu-id="dbbb3-140">Put a shared mailbox on litigation hold</span></span>

<span data-ttu-id="dbbb3-141">Pour en savoir plus sur la attente pour litige, voir [Créer une attente pour litige.](../../compliance/create-a-litigation-hold.md)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-141">To learn more about litigation hold, see [Create a Litigation Hold](../../compliance/create-a-litigation-hold.md).</span></span>

1. <span data-ttu-id="dbbb3-142">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-142">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-143">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Modifier la mise en attente pour** \> **litige.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-143">Select the shared mailbox you want to edit, then select **Litigation hold** \> **Edit**.</span></span>

3. <span data-ttu-id="dbbb3-144">Définissez le basculement sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-144">Set the toggle to **On**.</span></span> 

4. <span data-ttu-id="dbbb3-145">Vous pourz éventuellement entrer une durée, une note sur la attente et une URL avec plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-145">Optionally, enter a duration, s note about the hold, and a URL with more information.</span></span>  

5. <span data-ttu-id="dbbb3-146">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-146">Select **Save**.</span></span>


## <a name="add-or-remove-members"></a><span data-ttu-id="dbbb3-147">Ajouter ou supprimer des membres</span><span class="sxs-lookup"><span data-stu-id="dbbb3-147">Add or remove members</span></span>

1. <span data-ttu-id="dbbb3-148">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-148">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-149">Sélectionnez la boîte aux lettres  partagée à modifier, puis sélectionnez \> **Modifier les membres.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-149">Select the shared mailbox you want to edit, then select **Members** \> **Edit**.</span></span>

3. <span data-ttu-id="dbbb3-150">Effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbbb3-150">Do one of the following:</span></span>
   - <span data-ttu-id="dbbb3-151">Pour ajouter des membres, **sélectionnez Ajouter des** membres, recherchez ou sélectionnez un membre à ajouter, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-151">To add members, select **Add members**, search for or select a member to add, and then select **Save**.</span></span>
   - <span data-ttu-id="dbbb3-152">Pour supprimer des membres, utilisez la zone de recherche pour rechercher le membre si nécessaire, sélectionnez **le X** à côté du nom du membre, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-152">To remove members, use the Search box to search for the member if necessary, select the **X** next to the member's name, and then select **Save**.</span></span> 

4. <span data-ttu-id="dbbb3-153">Sélectionnez **Enregistrer à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-153">Select **Save** again.</span></span>

## <a name="add-or-remove-permissions-of-members"></a><span data-ttu-id="dbbb3-154">Ajouter ou supprimer des autorisations de membres</span><span class="sxs-lookup"><span data-stu-id="dbbb3-154">Add or remove permissions of members</span></span>

1. <span data-ttu-id="dbbb3-155">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-155">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-156">Sélectionnez la boîte aux lettres partagée que vous souhaitez modifier, puis sélectionnez **Personnaliser** \> **les autorisations des membres.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-156">Select the shared mailbox you want to edit, then select **Members** \> **Customize permissions**.</span></span>

3. <span data-ttu-id="dbbb3-157">Sélectionnez **Modifier** en plus de l’autorisation que vous souhaitez modifier pour un membre.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-157">Select **Edit** next to the permission you want to change for a member.</span></span> 

4. <span data-ttu-id="dbbb3-158">Effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbbb3-158">Do one of the following:</span></span>
   - <span data-ttu-id="dbbb3-159">Pour accorder cette autorisation à un membre supplémentaire, sélectionnez Ajouter des **autorisations,** recherchez ou sélectionnez un membre à ajouter, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-159">To give that permission to an additional member, select **Add permissions**, search for or select a member to add, and then select **Save**.</span></span>
   - <span data-ttu-id="dbbb3-160">Pour supprimer l’autorisation d’un membre, utilisez la zone De recherche pour rechercher le membre si nécessaire, sélectionnez **le X** en de côté du nom du membre, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-160">To remove the permission from a member, use the Search box to search for the member if necessary,  select the **X** next to the member's name, and then select **Save**.</span></span> 

4. <span data-ttu-id="dbbb3-161">Sélectionnez **Enregistrer à** nouveau.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-161">Select **Save** again.</span></span>

## <a name="show-or-hide-a-shared-mailbox-in-the-global-address-list"></a><span data-ttu-id="dbbb3-162">Afficher ou masquer une boîte aux lettres partagée dans la liste d’adresses globale</span><span class="sxs-lookup"><span data-stu-id="dbbb3-162">Show or hide a shared mailbox in the global address list</span></span>

<span data-ttu-id="dbbb3-163">Si vous choisissez de ne pas afficher la boîte aux lettres partagée dans la liste d’adresses globale, la boîte aux lettres n’apparaîtra pas dans la liste d’adresses de votre organisation, mais elle recevra toujours des messages électroniques qui lui seront envoyés.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-163">If you choose not to show the shared mailbox in the global address list, the mailbox won't appear in your organization's address list, but it will still receive email sent to it.</span></span> 

1. <span data-ttu-id="dbbb3-164">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-164">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

2. <span data-ttu-id="dbbb3-165">Sélectionnez la boîte aux lettres partagée à modifier, puis sélectionnez **Afficher dans la liste d’adresses globale** \> **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="dbbb3-165">Select the shared mailbox you want to edit, then select **Show in global address list** \> **Edit**.</span></span>

3. <span data-ttu-id="dbbb3-166">Définissez le toggle sur **On**  ou **Off**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-166">Set the toggle to **On**  or **Off**.</span></span> 

4. <span data-ttu-id="dbbb3-167">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-167">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="dbbb3-168">Le fait de masquer une boîte aux lettres partagée dans la liste d’adresses empêche les nouveaux membres de la boîte aux lettres partagée d’ajouter la boîte aux lettres masquée à leur profil Outlook tant que la boîte aux lettres partagée n’est pas de nouveau affichée dans la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dbbb3-168">Hiding a shared mailbox from address list will make it impossible for new shared mailbox members to add the hidden mailbox to their Outlook profile until the shared mailbox is again shown in the address list.</span></span> 

## <a name="related-content"></a><span data-ttu-id="dbbb3-169">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="dbbb3-169">Related content</span></span>

<span data-ttu-id="dbbb3-170">[À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-170">[About shared mailboxes](about-shared-mailboxes.md) (article)</span></span>\
<span data-ttu-id="dbbb3-171">[Créer une boîte aux lettres partagée](create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-171">[Create a shared mailbox](create-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="dbbb3-172">[Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-172">[Convert a user mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="dbbb3-173">[Supprimer une licence d’une boîte aux lettres partagée](remove-license-from-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-173">[Remove a license from a shared mailbox](remove-license-from-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="dbbb3-174">[Résoudre les problèmes liés aux boîtes aux lettres partagées](resolve-issues-with-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="dbbb3-174">[Resolve issues with shared mailboxes](resolve-issues-with-shared-mailboxes.md) (article)</span></span>