---
title: Gérer les notifications de facturation et les pièces jointes aux factures
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- okr_SMB
- AdminSurgePortfolio
- commerce
search.appverid:
- MET150
description: Découvrez comment gérer les personnes qui reçoivent des e-mails de notification de facturation et des pièces jointes de facture.
ms.openlocfilehash: f0811c5d027d042b5114c9e05c698dab1e08763b
ms.sourcegitcommit: babbba2b5bf69fd3facde2905ec024b753dcd1b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "50515222"
---
# <a name="manage-billing-notifications-and-invoice-attachments"></a><span data-ttu-id="6c720-103">Gérer les notifications de facturation et les pièces jointes aux factures</span><span class="sxs-lookup"><span data-stu-id="6c720-103">Manage billing notifications and invoice attachments</span></span>

<span data-ttu-id="6c720-104">La **page Notifications de facturation** vous permet de gérer les personnes qui reçoivent les e-mails de notification de facturation pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6c720-104">The **Billing notifications** page lets you manage who receives billing notification emails for your organization.</span></span> <span data-ttu-id="6c720-105">La page fournit également la possibilité de recevoir les factures de votre organisation en tant que [pièces jointes.](#receive-your-organizations-invoices-as-email-attachments)</span><span class="sxs-lookup"><span data-stu-id="6c720-105">The page also provides the option to [receive your organization's invoices as email attachments](#receive-your-organizations-invoices-as-email-attachments).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="6c720-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="6c720-106">Before you begin</span></span>

<span data-ttu-id="6c720-107">Vous devez être un administrateur global pour suivre les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="6c720-107">You must be a Global admin to do the steps described in this article.</span></span> <span data-ttu-id="6c720-108">Les administrateurs de facturation peuvent apporter certaines de ces modifications, comme indiqué dans les sections ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6c720-108">Billing admins can make some of these changes, as noted in the sections below.</span></span> <span data-ttu-id="6c720-109">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="6c720-109">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="change-the-language-you-receive-email-in"></a><span data-ttu-id="6c720-110">Modifier la langue de réception du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="6c720-110">Change the language you receive email in</span></span>

> [!NOTE]
> <span data-ttu-id="6c720-111">Les administrateurs de facturation peuvent également suivre les étapes de cette section.</span><span class="sxs-lookup"><span data-stu-id="6c720-111">Billing admins can also do the steps in this section.</span></span>

<span data-ttu-id="6c720-112">Les e-mails de notification de facturation sont envoyés dans la langue par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6c720-112">Billing notification emails are sent in your organization’s preferred language.</span></span> <span data-ttu-id="6c720-113">Pour modifier la langue préférée, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c720-113">To change the preferred language, use the following steps.</span></span>

1. <span data-ttu-id="6c720-114">Dans le Centre d’administration Microsoft 365, allez sur la page Notifications de   >  <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">facturation.</a></span><span class="sxs-lookup"><span data-stu-id="6c720-114">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-115">Dans la **section Paramètres de notification de facturation,** **sélectionnez Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="6c720-115">In the **Billing notification settings** section, select **Edit notification settings**.</span></span>
3. <span data-ttu-id="6c720-116">Dans le **volet Paramètres de notification de facturation,** sous Langue par défaut, sélectionnez la langue que vous souhaitez utiliser, puis  **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-116">In the **Billing notification settings** pane, under **Preferred language** select the language you want to use, then select **Save**.</span></span>

## <a name="change-who-receives-billing-notifications"></a><span data-ttu-id="6c720-117">Modifier les personnes qui reçoivent des notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="6c720-117">Change who receives billing notifications</span></span>

<span data-ttu-id="6c720-118">Les notifications de facturation de votre organisation sont envoyées à l’adresse de messagerie principale et de remplacement de chaque administrateur global et de facturation. Pour modifier les utilisateurs qui ont le rôle d’administrateur global ou de facturation, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c720-118">Your organization's billing notifications are sent to the primary and alternate email address of every Global and Billing admin. To change which users have the Global or Billing admin role, use the following steps.</span></span>

### <a name="assign-admin-roles-by-using-the-billing-notifications-page"></a><span data-ttu-id="6c720-119">Attribuer des rôles d’administrateur à l’aide de la page Notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="6c720-119">Assign admin roles by using the Billing notifications page</span></span>

1. <span data-ttu-id="6c720-120">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="6c720-120">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-121">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez le lien Administrateur de facturation ou Administrateur **général** dans le texte de description. </span><span class="sxs-lookup"><span data-stu-id="6c720-121">In the **Admins receiving billing notifications** section, select the **Billing administrator** or **Global administrator** link in the description text.</span></span>
3. <span data-ttu-id="6c720-122">Dans le volet droit, sous l’onglet **Administrateurs affectés,** sélectionnez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="6c720-122">In the right pane, on the **Assigned admins** tab, select **Add**.</span></span>
4. <span data-ttu-id="6c720-123">Dans le **volet Ajouter des administrateurs,** tapez le nom d’affichage ou le nom d’utilisateur de l’utilisateur, puis sélectionnez l’utilisateur dans la liste des suggestions.</span><span class="sxs-lookup"><span data-stu-id="6c720-123">In the **Add admins** pane, type the user’s display name or username, and then select the user from the list of suggestions.</span></span>
5. <span data-ttu-id="6c720-124">Ajoutez plusieurs utilisateurs jusqu’à ce que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="6c720-124">Add multiple users until you’re done.</span></span>
6. <span data-ttu-id="6c720-125">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6c720-125">Select **Save**.</span></span> <span data-ttu-id="6c720-126">L’utilisateur est ajouté à la liste des administrateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="6c720-126">The user is added to the list of assigned admins.</span></span>

### <a name="remove-admin-roles-by-using-the-billing-notifications-page"></a><span data-ttu-id="6c720-127">Supprimer des rôles d’administrateur à l’aide de la page Notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="6c720-127">Remove admin roles by using the Billing notifications page</span></span>

1. <span data-ttu-id="6c720-128">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="6c720-128">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-129">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez le lien Administrateur de facturation ou Administrateur **général** dans le texte de description. </span><span class="sxs-lookup"><span data-stu-id="6c720-129">In the **Admins receiving billing notifications** section, select the **Billing administrator** or **Global administrator** link in the description text.</span></span>
3. <span data-ttu-id="6c720-130">Dans le volet droit, sous l’onglet **Administrateurs affectés,** sélectionnez les utilisateurs à supprimer du rôle, puis sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-130">In the right pane, on the **Assigned admins** tab, select the users to remove from the role, and then select **Remove**.</span></span>
4. <span data-ttu-id="6c720-131">Dans la zone de confirmation, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-131">In the confirmation box, select **Remove**.</span></span> <span data-ttu-id="6c720-132">L’utilisateur est supprimé de la liste des administrateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="6c720-132">The user is removed from the list of assigned admins.</span></span>

## <a name="change-the-email-addresses-for-admins"></a><span data-ttu-id="6c720-133">Modifier les adresses de messagerie des administrateurs</span><span class="sxs-lookup"><span data-stu-id="6c720-133">Change the email addresses for admins</span></span>

<span data-ttu-id="6c720-134">Pour modifier l’adresse de messagerie principale et de remplacement d’autres administrateurs de votre organisation, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c720-134">To change the primary and alternate email address of other admins in your organization, use the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="6c720-135">Les administrateurs de facturation peuvent modifier leurs propres adresses de messagerie principale et de remplacement, mais pas pour d’autres administrateurs.</span><span class="sxs-lookup"><span data-stu-id="6c720-135">Billing admins can change their own primary and alternate email addresses, but not for other admins.</span></span>

1. <span data-ttu-id="6c720-136">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="6c720-136">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-137">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez un nom.</span><span class="sxs-lookup"><span data-stu-id="6c720-137">In the **Admins receiving billing notifications** section, select a name.</span></span>
3. <span data-ttu-id="6c720-138">Dans le volet droit, ajoutez ou mettez à jour l’adresse de messagerie principale et de remplacement selon vos besoins, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-138">In the right pane, add or update the primary and alternate email address as needed, then select **Save**.</span></span>

## <a name="change-your-organizations-contact-email"></a><span data-ttu-id="6c720-139">Modifier le courrier électronique de contact de votre organisation</span><span class="sxs-lookup"><span data-stu-id="6c720-139">Change your organization's contact email</span></span>

<span data-ttu-id="6c720-140">En plus de vos administrateurs globaux et de facturation, nous envoyons des notifications de facturation à l’adresse e-mail du contact de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6c720-140">In addition to your Global and Billing admins, we send billing notifications to your organization's contact email address.</span></span> <span data-ttu-id="6c720-141">Pour modifier l’adresse e-mail, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c720-141">To change the email address, use the following steps.</span></span>

1. <span data-ttu-id="6c720-142">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="6c720-142">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-143">Sous **Contact de l’organisation recevant des notifications de facturation,** sélectionnez le contact de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6c720-143">Under **Organization contact receiving billing notifications**, select the organization contact.</span></span>
3. <span data-ttu-id="6c720-144">Dans le volet droit, tapez l’adresse de messagerie que vous souhaitez utiliser, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-144">In the right pane, type the email address that you want to use, then select **Save**.</span></span>

## <a name="receive-your-organizations-invoices-as-email-attachments"></a><span data-ttu-id="6c720-145">Recevoir les factures de votre organisation en tant que pièces jointes</span><span class="sxs-lookup"><span data-stu-id="6c720-145">Receive your organization's invoices as email attachments</span></span>

> [!NOTE]
> <span data-ttu-id="6c720-146">Les administrateurs de facturation peuvent également suivre les étapes de cette section.</span><span class="sxs-lookup"><span data-stu-id="6c720-146">Billing admins can also do the steps in this section.</span></span>

<span data-ttu-id="6c720-147">Vous pouvez avoir une copie de la facture de votre organisation attachée sous forme de fichier PDF aux courriers électroniques de notification de facture lorsqu’une nouvelle facture est prête.</span><span class="sxs-lookup"><span data-stu-id="6c720-147">You can have a copy of your organization's invoice attached as a PDF file to invoice notification emails when a new invoice is ready.</span></span> <span data-ttu-id="6c720-148">Utilisez les étapes suivantes pour recevoir des factures en pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6c720-148">Use the following steps to receive invoices as attachments.</span></span>

1. <span data-ttu-id="6c720-149">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="6c720-149">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="6c720-150">Sous **Paramètres de notification de facturation,** **sélectionnez Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="6c720-150">Under **Billing notification settings**, select **Edit notification settings**.</span></span>
3. <span data-ttu-id="6c720-151">Dans le **volet Paramètres de notification de** facturation, sous Joindre un **PDF** à vos e-mails de facture, cochez la case, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="6c720-151">In the **Billing notification settings** pane, under **Attach a PDF to your invoice emails**, check the checkbox, then select **Save**.</span></span>

<span data-ttu-id="6c720-152">Pour arrêter de recevoir la pièce jointe de la facture à tout moment, suivez les étapes ci-dessus et clear the **Attach a PDF to your invoice emails** checkbox in step 3.</span><span class="sxs-lookup"><span data-stu-id="6c720-152">To stop receiving the invoice attachment at any time, follow the steps above and clear the **Attach a PDF to your invoice  emails** checkbox in step 3.</span></span>

## <a name="what-if-i-have-a-billing-profile"></a><span data-ttu-id="6c720-153">Que se passe-t-il si j’ai un profil de facturation ?</span><span class="sxs-lookup"><span data-stu-id="6c720-153">What if I have a billing profile?</span></span>

<span data-ttu-id="6c720-154">Si vous avez un profil de facturation, certaines des étapes décrites dans cet article peuvent être légèrement différentes pour certains de vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="6c720-154">If you have a billing profile, some of the steps described in this article might be slightly different for some of your subscriptions.</span></span> <span data-ttu-id="6c720-155">Cette section décrit ces différences.</span><span class="sxs-lookup"><span data-stu-id="6c720-155">This section describes those differences.</span></span> [<span data-ttu-id="6c720-156">Comment savoir si j’ai un profil de facturation ?</span><span class="sxs-lookup"><span data-stu-id="6c720-156">How do I know if I have a billing profile?</span></span>](manage-billing-profiles.md)

### <a name="who-receives-billing-notifications"></a><span data-ttu-id="6c720-157">Qui reçoit les notifications de facturation ?</span><span class="sxs-lookup"><span data-stu-id="6c720-157">Who receives Billing notifications?</span></span>

<span data-ttu-id="6c720-158">Les e-mails de notification de facturation sont envoyés aux adresses de messagerie principale et de remplacement pour les utilisateurs qui se voient attribuer l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="6c720-158">Billing notification emails are sent to the primary and alternate email addresses for users who are assigned one of the following roles:</span></span>

- <span data-ttu-id="6c720-159">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="6c720-159">Billing profile owner</span></span>
- <span data-ttu-id="6c720-160">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="6c720-160">Billing profile contributor</span></span>
- <span data-ttu-id="6c720-161">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="6c720-161">Invoice manager</span></span>

<span data-ttu-id="6c720-162">Pour en savoir plus sur les rôles de profil de facturation et comment les gérer, voir Comprendre les rôles d’administration du contrat [client Microsoft dans Azure.](https://docs.microsoft.com/azure/cost-management-billing/manage/understand-mca-roles)</span><span class="sxs-lookup"><span data-stu-id="6c720-162">To learn more about billing profile roles and how to manage them, see [Understand Microsoft Customer Agreement administrative roles in Azure](https://docs.microsoft.com/azure/cost-management-billing/manage/understand-mca-roles).</span></span>

<span data-ttu-id="6c720-163">Pour modifier les personnes qui reçoivent les notifications de facturation de votre organisation, utilisez les étapes suivantes pour modifier les rôles attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6c720-163">To change who receives your organization’s billing notifications, use the following steps to change the roles assigned to users.</span></span>

1. <span data-ttu-id="6c720-164">Dans le Centre d’administration, allez sur la page **Factures**&  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">paiements.</a></span><span class="sxs-lookup"><span data-stu-id="6c720-164">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="6c720-165">Sous **l’onglet Profil** de facturation, sélectionnez un profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="6c720-165">On the **Billing profile** tab, select a billing profile.</span></span>
3. <span data-ttu-id="6c720-166">Dans la section **Rôles de profil de** facturation, attribuez ou supprimez des rôles pour le propriétaire du **profil de** facturation, le collaborateur de **profil** de facturation ou le gestionnaire **de factures.**</span><span class="sxs-lookup"><span data-stu-id="6c720-166">In the **Billing profile roles** section, assign or remove roles for **Billing profile owner**, **Billing profile contributor**, or **Invoice manager**.</span></span>

### <a name="receive-invoices-as-email-attachments"></a><span data-ttu-id="6c720-167">Recevoir des factures en tant que pièces jointes d’e-mail</span><span class="sxs-lookup"><span data-stu-id="6c720-167">Receive invoices as email attachments</span></span>

<span data-ttu-id="6c720-168">Pour recevoir vos factures en pièce jointe à vos notifications de facture, utilisez les étapes suivantes pour activer ce paramètre pour un profil de facturation spécifique.</span><span class="sxs-lookup"><span data-stu-id="6c720-168">To receive your invoices as attachments to your invoice notifications, use the following steps to turn on this setting for a specific billing profile.</span></span>

1. <span data-ttu-id="6c720-169">Dans le Centre d’administration, allez sur la page **Factures**&  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">paiements.</a></span><span class="sxs-lookup"><span data-stu-id="6c720-169">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="6c720-170">Sélectionnez **l’onglet Profils** de facturation, puis sélectionnez un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6c720-170">Select the **Billing profiles** tab, then select a billing profile from the list.</span></span>
3. <span data-ttu-id="6c720-171">Dans la page des détails du profil de facturation, sous Obtenir les factures dans les pièces **jointes** des e-mails, basculez sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="6c720-171">On the billing profile details page, under **Get invoices in email attachments**, switch the toggle to **On**.</span></span>

## <a name="related-content"></a><span data-ttu-id="6c720-172">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="6c720-172">Related content</span></span>

<span data-ttu-id="6c720-173">[Consulter votre facture](view-your-bill-or-invoice.md) (article)</span><span class="sxs-lookup"><span data-stu-id="6c720-173">[View your bill or invoice](view-your-bill-or-invoice.md) (article)</span></span>\
<span data-ttu-id="6c720-174">[Comprendre votre facture pour Microsoft 365 pour les entreprises](understand-your-invoice2.md) (article)</span><span class="sxs-lookup"><span data-stu-id="6c720-174">[Understand your bill or invoice for Microsoft 365 for business](understand-your-invoice2.md) (article)</span></span>\
<span data-ttu-id="6c720-175">[Ajouter des utilisateurs et attribuer des licences en même temps](../../admin/add-users/add-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="6c720-175">[Add users and assign licenses at the same time](../../admin/add-users/add-users.md) (article)</span></span>