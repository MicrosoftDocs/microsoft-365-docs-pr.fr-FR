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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: ab5eb117-0f22-4fa7-a662-3a6bdb0add74
description: Configurez le transfert du courrier vers un ou plusieurs comptes de messagerie à l’aide d’Office 365.
ms.openlocfilehash: 5bbb7d4fa122051725418153e43f40aec370de61
ms.sourcegitcommit: e53234b1f64ebca00e121da1706c02b3337c35f0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2020
ms.locfileid: "49580614"
---
# <a name="configure-email-forwarding-in-microsoft-365"></a><span data-ttu-id="e6d97-103">Configurer le transfert du courrier électronique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e6d97-103">Configure email forwarding in Microsoft 365</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="e6d97-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="e6d97-104">The admin center is changing.</span></span> <span data-ttu-id="e6d97-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e6d97-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="e6d97-106">En tant qu’administrateur d’une organisation, vous pouvez avoir besoin d’une société pour configurer le transfert du courrier électronique pour la boîte aux lettres d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6d97-106">As the admin of an organization, you might have company requirements to set up email forwarding for a user's mailbox.</span></span> <span data-ttu-id="e6d97-107">Le transfert du courrier vous permet de transférer des messages électroniques envoyés à la boîte aux lettres d’un utilisateur vers une boîte aux lettres d’un autre utilisateur à l’intérieur ou à l’extérieur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e6d97-107">Email forwarding lets you forward email messages sent to a user's mailbox to another user's mailbox inside or outside of your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6d97-108">Vous pouvez utiliser des stratégies de filtrage du courrier indésirable sortant pour contrôler le transfert automatique vers des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="e6d97-108">You can use outbound spam filter policies to control automatic forwarding to external recipients.</span></span> <span data-ttu-id="e6d97-109">Pour plus d’informations, consultez la rubrique [contrôler le transfert automatique du courrier électronique externe dans Microsoft 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span><span class="sxs-lookup"><span data-stu-id="e6d97-109">For more information, see [Control automatic external email forwarding in Microsoft 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/external-email-forwarding?view=o365-worldwide&preserve-view=true#how-the-outbound-spam-filter-policy-settings-work-with-other-automatic-email-forwarding-controls).</span></span>

## <a name="configure-email-forwarding"></a><span data-ttu-id="e6d97-110">Configurer le transfert des e-mails</span><span class="sxs-lookup"><span data-stu-id="e6d97-110">Configure email forwarding</span></span>

<span data-ttu-id="e6d97-111">Avant de configurer le transfert du courrier, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="e6d97-111">Before you set up email forwarding, note the following:</span></span>

- <span data-ttu-id="e6d97-112">Une fois que vous avez configuré le transfert du courrier, seuls les **nouveaux** messages électroniques envoyés à la boîte aux lettres  *à partir de*  seront transférés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-112">Once you set up email forwarding, only **new** emails sent to the  *from*  mailbox will be forwarded.</span></span>

- <span data-ttu-id="e6d97-113">Le transfert du courrier exige que le compte  *de à partir*  de dispose d’une licence.</span><span class="sxs-lookup"><span data-stu-id="e6d97-113">Email forwarding requires that the  *from*  account has a license.</span></span> <span data-ttu-id="e6d97-114">Si vous configurez le transfert du courrier, car l’utilisateur a quitté votre organisation, une autre solution consiste à [convertir sa boîte aux lettres en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="e6d97-114">If you're setting up email forwarding because the user has left your organization, another option is to [convert their mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md).</span></span> <span data-ttu-id="e6d97-115">De cette manière, plusieurs personnes peuvent y accéder.</span><span class="sxs-lookup"><span data-stu-id="e6d97-115">This way several people can access it.</span></span> <span data-ttu-id="e6d97-116">Toutefois, une boîte aux lettres partagée ne peut pas dépasser 50 Go.</span><span class="sxs-lookup"><span data-stu-id="e6d97-116">However, a shared mailbox cannot exceed 50GB.</span></span>

<span data-ttu-id="e6d97-117">Pour effectuer ces étapes, vous devez être administrateur Exchange ou administrateur général dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e6d97-117">You must be an Exchange administrator or Global administrator in Microsoft 365 to do these steps.</span></span> <span data-ttu-id="e6d97-118">Pour plus d’informations, reportez-vous à la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e6d97-118">For more information, see the topic [About admin roles](../add-users/about-admin-roles.md).</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="e6d97-119">Dans le centre d’administration, accédez à **la page utilisateurs** \> **[actifs](https://go.microsoft.com/fwlink/p/?linkid=834822)** .</span><span class="sxs-lookup"><span data-stu-id="e6d97-119">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=834822)** page.</span></span>

2. <span data-ttu-id="e6d97-120">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-120">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="e6d97-121">Dans l’onglet **messagerie** , sélectionnez **gérer le transfert du courrier**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-121">On the **Mail** tab, select **Manage email forwarding**.</span></span>

4. <span data-ttu-id="e6d97-122">Sur la page transfert du courrier, sélectionnez **transférer tous les messages électroniques envoyés à cette boîte aux lettres**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages transférés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-122">On the email forwarding page, select **Forward all emails sent to this mailbox**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="e6d97-123">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6d97-123">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="e6d97-124">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-124">Select **Save changes**.</span></span>

    <span data-ttu-id="e6d97-125">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="e6d97-125">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="e6d97-126">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="e6d97-126">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

     <span data-ttu-id="e6d97-127">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e6d97-127">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="e6d97-128">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="e6d97-128">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="e6d97-129">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="e6d97-129">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="e6d97-130">Dans le centre d’administration, accédez à **la page utilisateurs** \> **[actifs](https://go.microsoft.com/fwlink/p/?linkid=847686)** .</span><span class="sxs-lookup"><span data-stu-id="e6d97-130">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=847686)** page.</span></span>

2. <span data-ttu-id="e6d97-131">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-131">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="e6d97-132">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-132">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="e6d97-133">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-133">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="e6d97-134">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6d97-134">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="e6d97-135">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-135">Select **Save**.</span></span>

   <span data-ttu-id="e6d97-136">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="e6d97-136">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="e6d97-137">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="e6d97-137">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="e6d97-138">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e6d97-138">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="e6d97-139">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="e6d97-139">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="e6d97-140">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="e6d97-140">If you do, email forwarding will stop.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="e6d97-141">Dans le centre d’administration, accédez à **la page utilisateurs** \> **[actifs](https://go.microsoft.com/fwlink/p/?linkid=850628)** .</span><span class="sxs-lookup"><span data-stu-id="e6d97-141">In the admin center, go to the **Users** \> **[Active users](https://go.microsoft.com/fwlink/p/?linkid=850628)** page.</span></span>

2. <span data-ttu-id="e6d97-142">Sélectionnez le nom de l’utilisateur dont vous souhaitez transférer le courrier électronique pour ouvrir la page des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-142">Select the name of the user whose email you want to forward to open the properties page.</span></span>

3. <span data-ttu-id="e6d97-143">Développez **paramètres de messagerie**, puis, dans la section **transfert de courrier** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-143">Expand **Mail settings**, and then in the **Email forwarding** section, select **Edit**.</span></span>

4. <span data-ttu-id="e6d97-144">Sur la page transfert du courrier, définissez le bouton bascule sur **activé**, entrez l’adresse de transfert et indiquez si vous souhaitez conserver une copie des messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="e6d97-144">On the email forwarding page, set the toggle to **On**, enter the forwarding address, and choose whether you want to keep a copy of forwarded emails.</span></span> <span data-ttu-id="e6d97-145">Si cette option n’est pas visible, vérifiez qu’une licence est attribuée au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6d97-145">If you don't see this option, make sure a license is assigned to the user account.</span></span> <span data-ttu-id="e6d97-146">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e6d97-146">Select **Save**.</span></span>

   <span data-ttu-id="e6d97-147">**Pour transférer des adresses de messagerie à plusieurs**, vous pouvez demander à l’utilisateur de configurer une règle dans Outlook pour transférer les adresses.</span><span class="sxs-lookup"><span data-stu-id="e6d97-147">**To forward to multiple email addresses**, you can ask the user to set up a rule in Outlook to forward to the addresses.</span></span> <span data-ttu-id="e6d97-148">Pour en savoir plus, consultez la rubrique [utiliser des règles pour transférer automatiquement des messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span><span class="sxs-lookup"><span data-stu-id="e6d97-148">To learn more, see [Use rules to automatically forward messages](https://support.microsoft.com/office/45aa9664-4911-4f96-9663-ece42816d746).</span></span>

   <span data-ttu-id="e6d97-149">Ou, dans le centre d’administration, [créez un groupe de distribution](../setup/create-distribution-lists.md), [Ajoutez-y les adresses](add-user-or-contact-to-distribution-list.md), puis configurez le transfert pour qu’il pointe vers la LD en suivant les instructions indiquées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e6d97-149">Or, in the admin center, [create a distribution group](../setup/create-distribution-lists.md), [add the addresses to it](add-user-or-contact-to-distribution-list.md), and then set up forwarding to point to the DL using the instructions in this article.</span></span>

5. <span data-ttu-id="e6d97-150">Ne supprimez pas le compte de l’utilisateur auquel est envoyé le courrier électronique que vous transférez ou supprimez sa licence.</span><span class="sxs-lookup"><span data-stu-id="e6d97-150">Don't delete the account of the user who's email you're forwarding or remove their license!</span></span>  <span data-ttu-id="e6d97-151">Si vous le faites, le transfert du courrier s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="e6d97-151">If you do, email forwarding will stop.</span></span>

::: moniker-end
