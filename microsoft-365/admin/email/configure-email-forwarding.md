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
ms.openlocfilehash: eb72204211a8eff929c024fbcede66dfe1f4b879
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635485"
---
# <a name="configure-email-forwarding-in-microsoft-365"></a><span data-ttu-id="b3424-103">Configurer le forwarding du courrier électronique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b3424-103">Configure email forwarding in Microsoft 365</span></span>

<span data-ttu-id="b3424-104">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences d’entreprise pour configurer le transport de courrier pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3424-104">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="b3424-105">Le forwarding de courrier vous permet de forwarder les messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers la boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b3424-105">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3424-106">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le forwarding automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="b3424-106">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="b3424-107">Pour plus d’informations, voir [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span><span class="sxs-lookup"><span data-stu-id="b3424-107">For more information, see [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span></span>

## <a name="configure-email-forwarding"></a><span data-ttu-id="b3424-108">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="b3424-108">Configure email forwarding</span></span>

<span data-ttu-id="b3424-109">Avant de configurer le forwarding du courrier électronique, notez les remarques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3424-109">Before you set up email forwarding, note the following:</span></span>

- <span data-ttu-id="b3424-110">Une fois que vous avez mis en place  le forwarding du courrier, **seuls** les nouveaux messages électroniques envoyés à partir de la boîte aux lettres sont transmis.</span><span class="sxs-lookup"><span data-stu-id="b3424-110">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be forwarded.</span></span>

- <span data-ttu-id="b3424-111">Le forwarding de courrier électronique nécessite que le  *compte de*  provenance dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="b3424-111">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="b3424-112">Si vous avez mis en place le forwarding du courrier électronique parce que l’utilisateur a quitté votre organisation, une autre option consiste à convertir sa boîte aux lettres en [boîte aux lettres partagée.](convert-user-mailbox-to-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="b3424-112">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="b3424-113">De cette façon, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="b3424-113">This way several people can access it.</span></span> <span data-ttu-id="b3424-114">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="b3424-114">However, a shared mailbox cannot exceed 50GB.</span></span>

<span data-ttu-id="b3424-115">Vous devez être administrateur Exchange administrateur général ou administrateur général Microsoft 365 pour pouvoir suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="b3424-115">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="b3424-116">Pour plus d’informations, voir la rubrique [à propos des rôles d’administrateur.](../add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="b3424-116">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

1. <span data-ttu-id="b3424-117">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=834822)**</span><span class="sxs-lookup"><span data-stu-id="b3424-117">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=834822)** page.</span></span>

2. <span data-ttu-id="b3424-118">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis, puis ouvrez la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3424-118">Select the name of the user whose email you want to forward, then open the properties page.</span></span>

3. <span data-ttu-id="b3424-119">Sous **l’onglet Courrier,** **sélectionnez Gérer le forwarding de courrier.**</span><span class="sxs-lookup"><span data-stu-id="b3424-119">On the **Mail** tab, select **Manage email forwarding**.</span></span>

4. <span data-ttu-id="b3424-120">Dans la page De forwarding de courrier, sélectionnez Forward **all emails sent to this mailbox,** enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span><span class="sxs-lookup"><span data-stu-id="b3424-120">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="b3424-121">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3424-121">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="b3424-122">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="b3424-122">Select **Save changes**.</span></span>

    <span data-ttu-id="b3424-123">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="b3424-123">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="b3424-124">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="b3424-124">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

     <span data-ttu-id="b3424-125">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="b3424-125">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="b3424-126">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="b3424-126">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="b3424-127">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b3424-127">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="b3424-128">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=847686)**</span><span class="sxs-lookup"><span data-stu-id="b3424-128">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=847686)** page.</span></span>

2. <span data-ttu-id="b3424-129">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3424-129">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="b3424-130">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="b3424-130">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="b3424-131">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="b3424-131">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="b3424-132">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3424-132">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="b3424-133">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b3424-133">Select **Save**.</span></span>

   <span data-ttu-id="b3424-134">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="b3424-134">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="b3424-135">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="b3424-135">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="b3424-136">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="b3424-136">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="b3424-137">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="b3424-137">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="b3424-138">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b3424-138">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="b3424-139">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=850628)**</span><span class="sxs-lookup"><span data-stu-id="b3424-139">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=850628)** page.</span></span>

2. <span data-ttu-id="b3424-140">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3424-140">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="b3424-141">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="b3424-141">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="b3424-142">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="b3424-142">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="b3424-143">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3424-143">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="b3424-144">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b3424-144">Select **Save**.</span></span>

   <span data-ttu-id="b3424-145">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="b3424-145">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="b3424-146">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="b3424-146">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="b3424-147">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="b3424-147">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="b3424-148">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="b3424-148">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span> <span data-ttu-id="b3424-149">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b3424-149">If you do, email forwarding will stop.</span></span>

::: moniker-end

## <a name="related-content"></a><span data-ttu-id="b3424-150">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="b3424-150">Related content</span></span> 

<span data-ttu-id="b3424-151">[Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="b3424-151">[Create a shared mailbox](../email/create-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="b3424-152">[Envoyer des courriers électroniques à partir d’une adresse différente](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span><span class="sxs-lookup"><span data-stu-id="b3424-152">[Send email from a different address](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span></span>\
<span data-ttu-id="b3424-153">[Modifier un nom d’utilisateur et une adresse e-mail](../add-users/change-a-user-name-and-email-address.md) (article)</span><span class="sxs-lookup"><span data-stu-id="b3424-153">[Change a user name and email address](../add-users/change-a-user-name-and-email-address.md) (article)</span></span>

