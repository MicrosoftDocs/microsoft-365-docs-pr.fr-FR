---
title: Configurer le transfert des e-mails
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: ab5eb117-0f22-4fa7-a662-3a6bdb0add74
description: Le forwarding de courrier vous permet de forwarder les messages électroniques envoyés à une boîte aux lettres Microsoft 365 utilisateur vers une autre boîte aux lettres à l’intérieur ou à l’extérieur de votre organisation.
ms.openlocfilehash: 1d16a44749b51b582b7198cb331edf7faf3cf1f8
ms.sourcegitcommit: 4bcac4cb4f9399ebbd7c8cff0abb4d6ecedb731e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2021
ms.locfileid: "52698915"
---
# <a name="configure-email-forwarding-in-microsoft-365"></a><span data-ttu-id="cf1a0-103">Configurer le forwarding du courrier électronique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cf1a0-103">Configure email forwarding in Microsoft 365</span></span>

<span data-ttu-id="cf1a0-104">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences d’entreprise pour configurer le transport de courrier pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-104">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="cf1a0-105">Le forwarding de courrier vous permet de forwarder les messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers la boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-105">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf1a0-106">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le forwarding automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-106">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="cf1a0-107">Pour plus d’informations, voir [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span><span class="sxs-lookup"><span data-stu-id="cf1a0-107">For more information, see [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span></span>

## <a name="configure-email-forwarding"></a><span data-ttu-id="cf1a0-108">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="cf1a0-108">Configure email forwarding</span></span>

<span data-ttu-id="cf1a0-109">Avant de configurer le forwarding du courrier électronique, notez les remarques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf1a0-109">Before you set up email forwarding, note the following:</span></span>

- <span data-ttu-id="cf1a0-110">Autoriser l’envoi automatique de messages à des personnes sur le domaine distant.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-110">Allow automatically forwarded messages to be sent to people on the remote domain.</span></span> <span data-ttu-id="cf1a0-111">Pour [plus d’informations, voir](/exchange/mail-flow-best-practices/remote-domains/manage-remote-domains) Gérer les domaines distants.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-111">See [Manage remote domains](/exchange/mail-flow-best-practices/remote-domains/manage-remote-domains) for details.</span></span>

- <span data-ttu-id="cf1a0-112">Une fois que vous avez mis en place  le forwarding du courrier, **seuls** les nouveaux messages électroniques envoyés à partir de la boîte aux lettres sont transmis.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-112">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be forwarded.</span></span>

- <span data-ttu-id="cf1a0-113">Le forwarding de courrier électronique nécessite que le  *compte de*  provenance dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-113">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="cf1a0-114">Si vous avez mis en place le forwarding du courrier électronique parce que l’utilisateur a quitté votre organisation, une autre option consiste à convertir sa boîte aux lettres en [boîte aux lettres partagée.](convert-user-mailbox-to-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-114">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="cf1a0-115">De cette façon, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-115">This way several people can access it.</span></span> <span data-ttu-id="cf1a0-116">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-116">However, a shared mailbox cannot exceed 50GB.</span></span>

<span data-ttu-id="cf1a0-117">Vous devez être administrateur Exchange administrateur général ou administrateur général Microsoft 365 pour pouvoir suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-117">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="cf1a0-118">Pour plus d’informations, voir la rubrique [à propos des rôles d’administrateur.](../add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-118">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

1. <span data-ttu-id="cf1a0-119">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=834822)**</span><span class="sxs-lookup"><span data-stu-id="cf1a0-119">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=834822)** page.</span></span>

2. <span data-ttu-id="cf1a0-120">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis, puis ouvrez la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-120">Select the name of the user whose email you want to forward, then open the properties page.</span></span>

3. <span data-ttu-id="cf1a0-121">Sous **l’onglet Courrier,** **sélectionnez Gérer le forwarding de courrier.**</span><span class="sxs-lookup"><span data-stu-id="cf1a0-121">On the **Mail** tab, select **Manage email forwarding**.</span></span>

4. <span data-ttu-id="cf1a0-122">Dans la page De forwarding de courrier, sélectionnez Forward **all emails sent to this mailbox,** enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-122">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="cf1a0-123">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-123">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="cf1a0-124">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-124">Select **Save changes**.</span></span>

    <span data-ttu-id="cf1a0-125">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-125">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="cf1a0-126">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-126">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

     <span data-ttu-id="cf1a0-127">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-127">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="cf1a0-128">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="cf1a0-128">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="cf1a0-129">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-129">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="cf1a0-130">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=847686)**</span><span class="sxs-lookup"><span data-stu-id="cf1a0-130">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=847686)** page.</span></span>

2. <span data-ttu-id="cf1a0-131">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-131">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="cf1a0-132">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-132">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="cf1a0-133">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-133">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="cf1a0-134">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-134">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="cf1a0-135">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-135">Select **Save**.</span></span>

   <span data-ttu-id="cf1a0-136">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-136">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="cf1a0-137">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-137">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="cf1a0-138">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-138">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="cf1a0-139">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="cf1a0-139">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="cf1a0-140">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-140">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="cf1a0-141">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=850628)**</span><span class="sxs-lookup"><span data-stu-id="cf1a0-141">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=850628)** page.</span></span>

2. <span data-ttu-id="cf1a0-142">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-142">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="cf1a0-143">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-143">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="cf1a0-144">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-144">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="cf1a0-145">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-145">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="cf1a0-146">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-146">Select **Save**.</span></span>

   <span data-ttu-id="cf1a0-147">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-147">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="cf1a0-148">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-148">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="cf1a0-149">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-149">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="cf1a0-150">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="cf1a0-150">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span> <span data-ttu-id="cf1a0-151">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-151">If you do, email forwarding will stop.</span></span>

::: moniker-end

## <a name="related-content"></a><span data-ttu-id="cf1a0-152">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="cf1a0-152">Related content</span></span> 

<span data-ttu-id="cf1a0-153">[Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-153">[Create a shared mailbox](../email/create-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="cf1a0-154">[Envoyer des courriers électroniques à partir d’une adresse différente](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-154">[Send email from a different address](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span></span>\
<span data-ttu-id="cf1a0-155">[Modifier un nom d’utilisateur et une adresse e-mail](../add-users/change-a-user-name-and-email-address.md) (article)</span><span class="sxs-lookup"><span data-stu-id="cf1a0-155">[Change a user name and email address](../add-users/change-a-user-name-and-email-address.md) (article)</span></span>
