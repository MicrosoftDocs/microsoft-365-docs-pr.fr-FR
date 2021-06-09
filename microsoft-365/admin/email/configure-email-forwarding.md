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
ms.openlocfilehash: dfea738f5d786b6e476dd02dc92fd0aef452d62f
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730137"
---
# <a name="configure-email-forwarding-in-microsoft-365"></a><span data-ttu-id="daf89-103">Configurer le forwarding du courrier électronique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="daf89-103">Configure email forwarding in Microsoft 365</span></span>

<span data-ttu-id="daf89-104">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences d’entreprise pour configurer le transport de courrier pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="daf89-104">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="daf89-105">Le forwarding de courrier vous permet de forwarder les messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers la boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="daf89-105">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="daf89-106">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le forwarding automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="daf89-106">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="daf89-107">Pour plus d’informations, voir [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span><span class="sxs-lookup"><span data-stu-id="daf89-107">For more information, see [Control automatic external email forwarding in Microsoft 365](/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span></span>

## <a name="configure-email-forwarding"></a><span data-ttu-id="daf89-108">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="daf89-108">Configure email forwarding</span></span>

<span data-ttu-id="daf89-109">Avant de configurer le forwarding du courrier électronique, notez les remarques suivantes :</span><span class="sxs-lookup"><span data-stu-id="daf89-109">Before you set up email forwarding, note the following:</span></span>

- <span data-ttu-id="daf89-110">Autoriser l’envoi automatique de messages à des personnes sur le domaine distant.</span><span class="sxs-lookup"><span data-stu-id="daf89-110">Allow automatically forwarded messages to be sent to people on the remote domain.</span></span> <span data-ttu-id="daf89-111">Pour [plus d’informations, voir](/exchange/mail-flow-best-practices/remote-domains/manage-remote-domains) Gérer les domaines distants.</span><span class="sxs-lookup"><span data-stu-id="daf89-111">See [Manage remote domains](/exchange/mail-flow-best-practices/remote-domains/manage-remote-domains) for details.</span></span>

- <span data-ttu-id="daf89-112">Une fois que vous avez mis en place  le forwarding du courrier, **seuls** les nouveaux messages électroniques envoyés à partir de la boîte aux lettres sont transmis.</span><span class="sxs-lookup"><span data-stu-id="daf89-112">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be forwarded.</span></span>

- <span data-ttu-id="daf89-113">Le forwarding de courrier électronique nécessite que le  *compte de*  provenance dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="daf89-113">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="daf89-114">Si vous avez mis en place le forwarding du courrier électronique parce que l’utilisateur a quitté votre organisation, une autre option consiste à convertir sa boîte aux lettres en [boîte aux lettres partagée.](convert-user-mailbox-to-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="daf89-114">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="daf89-115">De cette façon, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="daf89-115">This way several people can access it.</span></span> <span data-ttu-id="daf89-116">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="daf89-116">However, a shared mailbox cannot exceed 50GB.</span></span>

<span data-ttu-id="daf89-117">Vous devez être administrateur Exchange administrateur général ou administrateur général Microsoft 365 pour pouvoir suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="daf89-117">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="daf89-118">Pour plus d’informations, voir la rubrique [à propos des rôles d’administrateur.](../add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="daf89-118">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

1. <span data-ttu-id="daf89-119">Dans le centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=834822)**</span><span class="sxs-lookup"><span data-stu-id="daf89-119">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=834822)** page.</span></span>

2. <span data-ttu-id="daf89-120">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis, puis ouvrez la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="daf89-120">Select the name of the user whose email you want to forward, then open the properties page.</span></span>

3. <span data-ttu-id="daf89-121">Sous **l’onglet** Courrier, **sélectionnez Gérer le forwarding de courrier.**</span><span class="sxs-lookup"><span data-stu-id="daf89-121">On the **Mail** tab, select **Manage email forwarding**.</span></span>

4. <span data-ttu-id="daf89-122">Dans la page De forwarding de courrier, sélectionnez Forward **all emails sent to this mailbox,** enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span><span class="sxs-lookup"><span data-stu-id="daf89-122">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="daf89-123">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="daf89-123">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="daf89-124">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="daf89-124">Select **Save changes**.</span></span>

    <span data-ttu-id="daf89-125">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="daf89-125">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> 
    
    1.  <span data-ttu-id="daf89-126">Ouvrez **outlook**  >  **Home**  >   **Rules** > Select Manage Rules **& Alerts**</span><span class="sxs-lookup"><span data-stu-id="daf89-126">Open **outlook** > **Home** >  **Rules** > Select **Manage Rules & Alerts**</span></span>
    1. <span data-ttu-id="daf89-127">Select **New Rule** Select Apply rule on message I  >  **receive** located near bottom of list, then click **Next**.</span><span class="sxs-lookup"><span data-stu-id="daf89-127">Select **New Rule** > **Select Apply rule on message I receive** located near bottom of list, then click **Next**.</span></span>
    1. <span data-ttu-id="daf89-128">Cliquez **sur Oui** lorsque vous y êtes invité. Cette règle s’applique à chaque message que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="daf89-128">Click **Yes** when asked This rule will be applied to every message you receive.</span></span> 
    1. <span data-ttu-id="daf89-129">Dans la liste suivante, sélectionnez les actions pour les rediriger vers des personnes ou un **groupe public** et arrêter le **traitement d’autres règles**</span><span class="sxs-lookup"><span data-stu-id="daf89-129">On the next list select the actions **redirect it to people or public group** and **stop processing more rules**</span></span>
    1. <span data-ttu-id="daf89-130">Cliquez sur l’expression **soulignée personnes ou groupe public** dans la partie inférieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="daf89-130">Click the underlined phrase **people or public group** in the bottom part of window.</span></span>
    1. <span data-ttu-id="daf89-131">Tapez **l’adresse e-mail** à qui envoyer le courrier dans le champ À, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="daf89-131">Type the **email address** to forward mail to in the To field, then click **OK**.</span></span>
    1. <span data-ttu-id="daf89-132">Sélectionner **Terminer**</span><span class="sxs-lookup"><span data-stu-id="daf89-132">Select **Finish**</span></span>
    

     <span data-ttu-id="daf89-133">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="daf89-133">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="daf89-134">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="daf89-134">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="daf89-135">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="daf89-135">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="daf89-136">Dans le centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=847686)**</span><span class="sxs-lookup"><span data-stu-id="daf89-136">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=847686)** page.</span></span>

2. <span data-ttu-id="daf89-137">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="daf89-137">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="daf89-138">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="daf89-138">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="daf89-139">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="daf89-139">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="daf89-140">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="daf89-140">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="daf89-141">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="daf89-141">Select **Save**.</span></span>

   <span data-ttu-id="daf89-142">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="daf89-142">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="daf89-143">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="daf89-143">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="daf89-144">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="daf89-144">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="daf89-145">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="daf89-145">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="daf89-146">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="daf89-146">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="daf89-147">Dans le centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=850628)**</span><span class="sxs-lookup"><span data-stu-id="daf89-147">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=850628)** page.</span></span>

2. <span data-ttu-id="daf89-148">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="daf89-148">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="daf89-149">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="daf89-149">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="daf89-150">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="daf89-150">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="daf89-151">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="daf89-151">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="daf89-152">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="daf89-152">Select **Save**.</span></span>

   <span data-ttu-id="daf89-153">**Pour le forward vers plusieurs adresses** e-mail, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour le forward aux adresses.</span><span class="sxs-lookup"><span data-stu-id="daf89-153">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="daf89-154">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="daf89-154">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="daf89-155">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="daf89-155">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="daf89-156">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="daf89-156">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span> <span data-ttu-id="daf89-157">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="daf89-157">If you do, email forwarding will stop.</span></span>

::: moniker-end

## <a name="related-content"></a><span data-ttu-id="daf89-158">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="daf89-158">Related content</span></span> 

<span data-ttu-id="daf89-159">[Créer une boîte aux lettres partagée](../email/create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="daf89-159">[Create a shared mailbox](../email/create-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="daf89-160">[Envoyer des courriers électroniques à partir d’une adresse différente](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span><span class="sxs-lookup"><span data-stu-id="daf89-160">[Send email from a different address](https://support.microsoft.com/office/ccba89cb-141c-4a36-8c56-6d16a8556d2e) (article)</span></span>\
<span data-ttu-id="daf89-161">[Modifier un nom d’utilisateur et une adresse e-mail](../add-users/change-a-user-name-and-email-address.md) (article)</span><span class="sxs-lookup"><span data-stu-id="daf89-161">[Change a user name and email address](../add-users/change-a-user-name-and-email-address.md) (article)</span></span>
