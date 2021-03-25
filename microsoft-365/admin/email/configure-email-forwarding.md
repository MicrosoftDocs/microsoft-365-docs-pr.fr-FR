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
description: Configurer le forwarding de courrier vers un ou plusieurs comptes de messagerie à l’aide d’Office 365.
ms.openlocfilehash: d7c9a37a066bd53e541cf623c1953fb572827b61
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51197862"
---
# <a name="configure-email-forwarding-in-microsoft-365"></a><span data-ttu-id="fa54d-103">Configurer le forwarding du courrier électronique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fa54d-103">Configure email forwarding in Microsoft 365</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="fa54d-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="fa54d-104">The admin center is changing.</span></span> <span data-ttu-id="fa54d-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="fa54d-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="fa54d-106">En tant qu’administrateur d’une organisation, vous pouvez avoir des exigences d’entreprise pour configurer le transport de courrier pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa54d-106">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="fa54d-107">Le forwarding de courrier vous permet de forwarder les messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers la boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fa54d-107">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa54d-108">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le forwarding automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="fa54d-108">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="fa54d-109">Pour plus d’informations, voir [Control automatic external email forwarding in Microsoft 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span><span class="sxs-lookup"><span data-stu-id="fa54d-109">For more information, see [Control automatic external email forwarding in Microsoft 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span></span>

## <a name="configure-email-forwarding"></a><span data-ttu-id="fa54d-110">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="fa54d-110">Configure email forwarding</span></span>

<span data-ttu-id="fa54d-111">Avant de configurer le forwarding du courrier électronique, notez les remarques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa54d-111">Before you set up email forwarding, note the following:</span></span>

- <span data-ttu-id="fa54d-112">Une fois que vous avez mis en place  le forwarding du courrier, **seuls** les nouveaux messages électroniques envoyés à partir de la boîte aux lettres sont transmis.</span><span class="sxs-lookup"><span data-stu-id="fa54d-112">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be forwarded.</span></span>

- <span data-ttu-id="fa54d-113">Le forwarding de courrier électronique nécessite que le  *compte de*  provenance dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="fa54d-113">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="fa54d-114">Si vous avez mis en place le forwarding du courrier électronique parce que l’utilisateur a quitté votre organisation, une autre option consiste à convertir sa boîte aux lettres en [boîte aux lettres partagée.](convert-user-mailbox-to-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="fa54d-114">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="fa54d-115">De cette façon, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="fa54d-115">This way several people can access it.</span></span> <span data-ttu-id="fa54d-116">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="fa54d-116">However, a shared mailbox cannot exceed 50GB.</span></span>

<span data-ttu-id="fa54d-117">Pour ce faire, vous devez être administrateur Exchange ou administrateur général dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fa54d-117">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="fa54d-118">Pour plus d’informations, voir la rubrique [à propos des rôles d’administrateur.](../add-users/about-admin-roles.md)</span><span class="sxs-lookup"><span data-stu-id="fa54d-118">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="fa54d-119">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=834822)**</span><span class="sxs-lookup"><span data-stu-id="fa54d-119">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=834822)** page.</span></span>

2. <span data-ttu-id="fa54d-120">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa54d-120">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="fa54d-121">Sous **l’onglet Courrier,** **sélectionnez Gérer le forwarding de courrier.**</span><span class="sxs-lookup"><span data-stu-id="fa54d-121">On the **Mail** tab, select **Manage email forwarding**.</span></span>

4. <span data-ttu-id="fa54d-122">Dans la page De forwarding de courrier, sélectionnez Forward **all emails sent to this mailbox,** enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span><span class="sxs-lookup"><span data-stu-id="fa54d-122">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="fa54d-123">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa54d-123">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="fa54d-124">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="fa54d-124">Select **Save changes**.</span></span>

    <span data-ttu-id="fa54d-125">**Pour le faire,** vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour qu’elle soit transmis aux adresses.</span><span class="sxs-lookup"><span data-stu-id="fa54d-125">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="fa54d-126">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="fa54d-126">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

     <span data-ttu-id="fa54d-127">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="fa54d-127">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="fa54d-128">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="fa54d-128">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="fa54d-129">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="fa54d-129">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="fa54d-130">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=847686)**</span><span class="sxs-lookup"><span data-stu-id="fa54d-130">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=847686)** page.</span></span>

2. <span data-ttu-id="fa54d-131">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa54d-131">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="fa54d-132">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="fa54d-132">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="fa54d-133">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="fa54d-133">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="fa54d-134">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa54d-134">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="fa54d-135">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fa54d-135">Select **Save**.</span></span>

   <span data-ttu-id="fa54d-136">**Pour le faire,** vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour qu’elle soit transmis aux adresses.</span><span class="sxs-lookup"><span data-stu-id="fa54d-136">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="fa54d-137">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="fa54d-137">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="fa54d-138">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="fa54d-138">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="fa54d-139">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="fa54d-139">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="fa54d-140">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="fa54d-140">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="fa54d-141">Dans le Centre d’administration, allez à la page **Utilisateurs** \> **[actifs.](https://go.microsoft.com/fwlink/p/?linkid=850628)**</span><span class="sxs-lookup"><span data-stu-id="fa54d-141">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=850628)** page.</span></span>

2. <span data-ttu-id="fa54d-142">Sélectionnez le nom de l’utilisateur dont vous souhaitez qu’il soit transmis pour ouvrir la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa54d-142">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="fa54d-143">Développez **les paramètres de messagerie,** puis, dans la section **De forwarding de** courrier, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="fa54d-143">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="fa54d-144">Dans la page de forwarding de courrier électronique, définissez le basculement sur **Sur,** entrez l’adresse de forwarding et choisissez si vous souhaitez conserver une copie des e-mails transmis.</span><span class="sxs-lookup"><span data-stu-id="fa54d-144">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="fa54d-145">Si cette option n’est pas disponible, assurez-vous qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa54d-145">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="fa54d-146">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fa54d-146">Select **Save**.</span></span>

   <span data-ttu-id="fa54d-147">**Pour le faire,** vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour qu’elle soit transmis aux adresses.</span><span class="sxs-lookup"><span data-stu-id="fa54d-147">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="fa54d-148">Pour plus d’informations, voir [Utiliser des règles pour envoyer automatiquement des messages.](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746)</span><span class="sxs-lookup"><span data-stu-id="fa54d-148">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="fa54d-149">Ou bien, dans le Centre d’administration, créez un groupe de [distribution,](../setup/create-distribution-lists.md)ajoutez-y les [adresses,](add-user-or-contact-to-distribution-list.md)puis définissez le forwarding pour qu’il pointe vers la DL en suivant les instructions de cet article.</span><span class="sxs-lookup"><span data-stu-id="fa54d-149">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="fa54d-150">Ne supprimez pas le compte de l’utilisateur de messagerie que vous êtes en train de forwarder ou supprimez sa licence !</span><span class="sxs-lookup"><span data-stu-id="fa54d-150">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="fa54d-151">Si vous le faites, le forwarding du courrier électronique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="fa54d-151">If you do, email forwarding will stop.</span></span>

::: moniker-end