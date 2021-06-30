---
title: Gérer les notifications de facturation et les pièces jointes de facture
f1.keywords:
- CSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: prkalid, guyb
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
- commerce_billing
search.appverid:
- MET150
description: Découvrez comment gérer les personnes qui reçoivent des e-mails de notification de facturation et des pièces jointes de facture.
ms.date: 03/17/2021
ms.openlocfilehash: a49598cd1b361a85af8455b0aff19e11fcf96526
ms.sourcegitcommit: 99e67bfe1d677c2f51712b05dcc54908b343cf6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53203243"
---
# <a name="manage-billing-notifications-and-invoice-attachments"></a><span data-ttu-id="0121f-103">Gérer les notifications de facturation et les pièces jointes de facture</span><span class="sxs-lookup"><span data-stu-id="0121f-103">Manage billing notifications and invoice attachments</span></span>

<span data-ttu-id="0121f-104">La **page Notifications de facturation** vous permet de gérer les personnes qui reçoivent les e-mails de notification de facturation pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0121f-104">The **Billing notifications** page lets you manage who receives billing notification emails for your organization.</span></span> <span data-ttu-id="0121f-105">La page fournit également la possibilité de recevoir les factures de votre organisation en tant que [pièces jointes.](#receive-your-organizations-invoices-as-email-attachments)</span><span class="sxs-lookup"><span data-stu-id="0121f-105">The page also provides the option to [receive your organization's invoices as email attachments](#receive-your-organizations-invoices-as-email-attachments).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="0121f-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="0121f-106">Before you begin</span></span>

<span data-ttu-id="0121f-107">Vous devez être un administrateur global pour suivre les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="0121f-107">You must be a Global admin to do the steps described in this article.</span></span> <span data-ttu-id="0121f-108">Les administrateurs de facturation peuvent apporter certaines de ces modifications, comme indiqué dans les sections ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0121f-108">Billing admins can make some of these changes, as noted in the sections below.</span></span> <span data-ttu-id="0121f-109">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0121f-109">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="change-the-language-you-receive-email-in"></a><span data-ttu-id="0121f-110">Modifier la langue dans qui vous recevez le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="0121f-110">Change the language you receive email in</span></span>

<span data-ttu-id="0121f-111">Les e-mails de notification de facturation sont envoyés dans la langue par défaut de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0121f-111">Billing notification emails are sent in your organization’s preferred language.</span></span> <span data-ttu-id="0121f-112">Pour modifier la langue préférée, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0121f-112">To change the preferred language, use the following steps.</span></span>

1. <span data-ttu-id="0121f-113">Dans la Centre d’administration Microsoft 365, allez à **la** page Notifications de  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">facturation.</a></span><span class="sxs-lookup"><span data-stu-id="0121f-113">In the Microsoft 365 admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-114">Dans la **section Paramètres de notification de facturation,** **sélectionnez Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="0121f-114">In the **Billing notification settings** section, select **Edit notification settings**.</span></span>
3. <span data-ttu-id="0121f-115">Dans le **volet Paramètres de notification de facturation,** sous Langue par défaut, sélectionnez la langue que vous souhaitez utiliser, puis  **sélectionnez Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0121f-115">In the **Billing notification settings** pane, under **Preferred language** select the language you want to use, then select **Save**.</span></span>

## <a name="change-who-receives-billing-notifications"></a><span data-ttu-id="0121f-116">Modifier les personnes qui reçoivent des notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="0121f-116">Change who receives billing notifications</span></span>

<span data-ttu-id="0121f-117">Les notifications de facturation de votre organisation sont envoyées à l’adresse de messagerie principale et de remplacement de chaque administrateur global et de facturation. Pour modifier les utilisateurs qui ont le rôle d’administrateur global ou de facturation, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0121f-117">Your organization's billing notifications are sent to the primary and alternate email address of every Global and Billing admin. To change which users have the Global or Billing admin role, use the following steps.</span></span>

### <a name="assign-admin-roles-by-using-the-billing-notifications-page"></a><span data-ttu-id="0121f-118">Attribuer des rôles d’administrateur à l’aide de la page Notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="0121f-118">Assign admin roles by using the Billing notifications page</span></span>

1. <span data-ttu-id="0121f-119">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="0121f-119">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-120">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez le lien Administrateur de facturation ou Administrateur **général** dans le texte de description. </span><span class="sxs-lookup"><span data-stu-id="0121f-120">In the **Admins receiving billing notifications** section, select the **Billing administrator** or **Global administrator** link in the description text.</span></span>
3. <span data-ttu-id="0121f-121">Dans le volet droit, sous l’onglet **Administrateurs affectés,** sélectionnez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="0121f-121">In the right pane, on the **Assigned admins** tab, select **Add**.</span></span>
4. <span data-ttu-id="0121f-122">Dans le **volet Ajouter des administrateurs,** tapez le nom d’affichage ou le nom d’utilisateur de l’utilisateur, puis sélectionnez l’utilisateur dans la liste des suggestions.</span><span class="sxs-lookup"><span data-stu-id="0121f-122">In the **Add admins** pane, type the user’s display name or username, and then select the user from the list of suggestions.</span></span>
5. <span data-ttu-id="0121f-123">Ajoutez plusieurs utilisateurs jusqu’à ce que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="0121f-123">Add multiple users until you’re done.</span></span>
6. <span data-ttu-id="0121f-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0121f-124">Select **Save**.</span></span> <span data-ttu-id="0121f-125">L’utilisateur est ajouté à la liste des administrateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="0121f-125">The user is added to the list of assigned admins.</span></span>

### <a name="remove-admin-roles-by-using-the-billing-notifications-page"></a><span data-ttu-id="0121f-126">Supprimer des rôles d’administrateur à l’aide de la page Notifications de facturation</span><span class="sxs-lookup"><span data-stu-id="0121f-126">Remove admin roles by using the Billing notifications page</span></span>

1. <span data-ttu-id="0121f-127">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="0121f-127">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-128">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez le lien Administrateur de facturation ou Administrateur **général** dans le texte de description. </span><span class="sxs-lookup"><span data-stu-id="0121f-128">In the **Admins receiving billing notifications** section, select the **Billing administrator** or **Global administrator** link in the description text.</span></span>
3. <span data-ttu-id="0121f-129">Dans le volet droit, sous l’onglet **Administrateurs affectés,** sélectionnez les utilisateurs à supprimer du rôle, puis sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="0121f-129">In the right pane, on the **Assigned admins** tab, select the users to remove from the role, and then select **Remove**.</span></span>
4. <span data-ttu-id="0121f-130">Dans la zone de confirmation, sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="0121f-130">In the confirmation box, select **Remove**.</span></span> <span data-ttu-id="0121f-131">L’utilisateur est supprimé de la liste des administrateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="0121f-131">The user is removed from the list of assigned admins.</span></span>

## <a name="change-the-email-addresses-for-admins"></a><span data-ttu-id="0121f-132">Modifier les adresses de messagerie des administrateurs</span><span class="sxs-lookup"><span data-stu-id="0121f-132">Change the email addresses for admins</span></span>

<span data-ttu-id="0121f-133">Pour modifier l’adresse de messagerie principale et de remplacement d’autres administrateurs de votre organisation, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0121f-133">To change the primary and alternate email address of other admins in your organization, use the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0121f-134">Les administrateurs de facturation peuvent modifier leurs propres adresses de messagerie principale et de remplacement, mais pas pour d’autres administrateurs.</span><span class="sxs-lookup"><span data-stu-id="0121f-134">Billing admins can change their own primary and alternate email addresses, but not for other admins.</span></span>

1. <span data-ttu-id="0121f-135">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="0121f-135">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-136">Dans la section **Administrateurs recevant des notifications de facturation,** sélectionnez un nom.</span><span class="sxs-lookup"><span data-stu-id="0121f-136">In the **Admins receiving billing notifications** section, select a name.</span></span>
3. <span data-ttu-id="0121f-137">Dans le volet droit, ajoutez ou mettez à jour l’adresse de messagerie principale et de remplacement si nécessaire, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0121f-137">In the right pane, add or update the primary and alternate email address as needed, then select **Save**.</span></span>

## <a name="change-your-organizations-contact-email"></a><span data-ttu-id="0121f-138">Modifier le courrier électronique de contact de votre organisation</span><span class="sxs-lookup"><span data-stu-id="0121f-138">Change your organization's contact email</span></span>

<span data-ttu-id="0121f-139">En plus de vos administrateurs globaux et de facturation, nous envoyons des notifications de facturation à l’adresse e-mail du contact de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0121f-139">In addition to your Global and Billing admins, we send billing notifications to your organization's contact email address.</span></span> <span data-ttu-id="0121f-140">Pour modifier l’adresse e-mail, utilisez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0121f-140">To change the email address, use the following steps.</span></span>

1. <span data-ttu-id="0121f-141">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="0121f-141">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-142">Sous **Contact de l’organisation recevant des notifications de facturation,** sélectionnez le contact de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="0121f-142">Under **Organization contact receiving billing notifications**, select the organization contact.</span></span>
3. <span data-ttu-id="0121f-143">Dans le volet droit, tapez l’adresse de messagerie que vous souhaitez utiliser, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0121f-143">In the right pane, type the email address that you want to use, then select **Save**.</span></span>

## <a name="receive-your-organizations-invoices-as-email-attachments"></a><span data-ttu-id="0121f-144">Recevoir les factures de votre organisation en tant que pièces jointes</span><span class="sxs-lookup"><span data-stu-id="0121f-144">Receive your organization's invoices as email attachments</span></span>

> [!NOTE]
> <span data-ttu-id="0121f-145">Les administrateurs de facturation peuvent également suivre les étapes de cette section.</span><span class="sxs-lookup"><span data-stu-id="0121f-145">Billing admins can also do the steps in this section.</span></span>

<span data-ttu-id="0121f-146">Vous pouvez avoir une copie de la facture de votre organisation attachée sous forme de fichier PDF aux courriers électroniques de notification de facture lorsqu’une nouvelle facture est prête.</span><span class="sxs-lookup"><span data-stu-id="0121f-146">You can have a copy of your organization's invoice attached as a PDF file to invoice notification emails when a new invoice is ready.</span></span> <span data-ttu-id="0121f-147">Utilisez les étapes suivantes pour recevoir des factures en tant que pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="0121f-147">Use the following steps to receive invoices as attachments.</span></span>

1. <span data-ttu-id="0121f-148">Dans le Centre d’administration, accédez à la page **Facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Notifications de facturation</a>.</span><span class="sxs-lookup"><span data-stu-id="0121f-148">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=853212" target="_blank">Billing notifications</a> page.</span></span>
2. <span data-ttu-id="0121f-149">Sous **Paramètres de notification de facturation,** **sélectionnez Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="0121f-149">Under **Billing notification settings**, select **Edit notification settings**.</span></span>
3. <span data-ttu-id="0121f-150">Dans le **volet Paramètres de notification de** facturation, sous Joindre un **PDF** à vos e-mails de facture, cochez la case, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="0121f-150">In the **Billing notification settings** pane, under **Attach a PDF to your invoice emails**, check the checkbox, then select **Save**.</span></span>

<span data-ttu-id="0121f-151">Pour arrêter de recevoir la pièce jointe de la facture à tout moment, suivez les étapes ci-dessus et clear the **Attach a PDF to your invoice emails** checkbox in step 3.</span><span class="sxs-lookup"><span data-stu-id="0121f-151">To stop receiving the invoice attachment at any time, follow the steps above and clear the **Attach a PDF to your invoice  emails** checkbox in step 3.</span></span>

## <a name="what-if-i-have-a-billing-profile"></a><span data-ttu-id="0121f-152">Que se passe-t-il si j’ai un profil de facturation ?</span><span class="sxs-lookup"><span data-stu-id="0121f-152">What if I have a billing profile?</span></span>

<span data-ttu-id="0121f-153">Si vous avez un profil de facturation, certaines des étapes décrites dans cet article peuvent être légèrement différentes pour certains de vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="0121f-153">If you have a billing profile, some of the steps described in this article might be slightly different for some of your subscriptions.</span></span> <span data-ttu-id="0121f-154">Cette section décrit ces différences.</span><span class="sxs-lookup"><span data-stu-id="0121f-154">This section describes those differences.</span></span> [<span data-ttu-id="0121f-155">Comment savoir si j’ai un profil de facturation ?</span><span class="sxs-lookup"><span data-stu-id="0121f-155">How do I know if I have a billing profile?</span></span>](manage-billing-profiles.md)

### <a name="who-receives-billing-notifications"></a><span data-ttu-id="0121f-156">Qui reçoit des notifications de facturation ?</span><span class="sxs-lookup"><span data-stu-id="0121f-156">Who receives Billing notifications?</span></span>

<span data-ttu-id="0121f-157">Les e-mails de notification de facturation sont envoyés aux adresses de messagerie principale et de remplacement pour les utilisateurs qui se voient attribuer l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="0121f-157">Billing notification emails are sent to the primary and alternate email addresses for users who are assigned one of the following roles:</span></span>

- <span data-ttu-id="0121f-158">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="0121f-158">Billing profile owner</span></span>
- <span data-ttu-id="0121f-159">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="0121f-159">Billing profile contributor</span></span>
- <span data-ttu-id="0121f-160">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="0121f-160">Invoice manager</span></span>

<span data-ttu-id="0121f-161">Pour en savoir plus sur les rôles de profil de facturation et comment les gérer, voir Comprendre les rôles d’administration du contrat [client Microsoft dans Azure.](/azure/cost-management-billing/manage/understand-mca-roles)</span><span class="sxs-lookup"><span data-stu-id="0121f-161">To learn more about billing profile roles and how to manage them, see [Understand Microsoft Customer Agreement administrative roles in Azure](/azure/cost-management-billing/manage/understand-mca-roles).</span></span>

<span data-ttu-id="0121f-162">Pour modifier les personnes qui reçoivent les notifications de facturation de votre organisation, utilisez les étapes suivantes pour modifier les rôles attribués aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0121f-162">To change who receives your organization’s billing notifications, use the following steps to change the roles assigned to users.</span></span>

1. <span data-ttu-id="0121f-163">Dans le Centre d’administration, allez sur la page **Factures**&  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">paiements.</a></span><span class="sxs-lookup"><span data-stu-id="0121f-163">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="0121f-164">Sous **l’onglet Profil** de facturation, sélectionnez un profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="0121f-164">On the **Billing profile** tab, select a billing profile.</span></span>
3. <span data-ttu-id="0121f-165">Dans la section **Rôles de profil de** facturation, attribuez ou supprimez des rôles pour le propriétaire du **profil de** facturation, le collaborateur de **profil** de facturation ou le gestionnaire **de factures.**</span><span class="sxs-lookup"><span data-stu-id="0121f-165">In the **Billing profile roles** section, assign or remove roles for **Billing profile owner**, **Billing profile contributor**, or **Invoice manager**.</span></span>

### <a name="receive-invoices-as-email-attachments"></a><span data-ttu-id="0121f-166">Recevoir des factures en tant que pièces jointes d’e-mail</span><span class="sxs-lookup"><span data-stu-id="0121f-166">Receive invoices as email attachments</span></span>

<span data-ttu-id="0121f-167">Pour recevoir vos factures en pièce jointe à vos notifications de facture, utilisez les étapes suivantes pour activer ce paramètre pour un profil de facturation spécifique.</span><span class="sxs-lookup"><span data-stu-id="0121f-167">To receive your invoices as attachments to your invoice notifications, use the following steps to turn on this setting for a specific billing profile.</span></span>

1. <span data-ttu-id="0121f-168">Dans le Centre d’administration, allez sur la page **Factures**&  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">paiements.</a></span><span class="sxs-lookup"><span data-stu-id="0121f-168">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="0121f-169">Sélectionnez **l’onglet Profils** de facturation, puis sélectionnez un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="0121f-169">Select the **Billing profiles** tab, then select a billing profile from the list.</span></span>
3. <span data-ttu-id="0121f-170">Dans la page des détails du profil de facturation, sous Obtenir les factures dans les pièces **jointes** des e-mails, basculez sur **Sur**.</span><span class="sxs-lookup"><span data-stu-id="0121f-170">On the billing profile details page, under **Get invoices in email attachments**, switch the toggle to **On**.</span></span>

## <a name="related-content"></a><span data-ttu-id="0121f-171">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="0121f-171">Related content</span></span>

<span data-ttu-id="0121f-172">[Consulter votre facture](view-your-bill-or-invoice.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0121f-172">[View your bill or invoice](view-your-bill-or-invoice.md) (article)</span></span>\
<span data-ttu-id="0121f-173">[Informations de facturation pour Microsoft 365 pour les entreprises au Mexique](mexico-billing-info.md) (article) </span><span class="sxs-lookup"><span data-stu-id="0121f-173">[Billing information for Microsoft 365 for business in Mexico](mexico-billing-info.md) (article) </span></span>\
<span data-ttu-id="0121f-174">[Comprendre votre facture pour Microsoft 365 entreprise](understand-your-invoice2.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0121f-174">[Understand your bill or invoice for Microsoft 365 for business](understand-your-invoice2.md) (article)</span></span>\
<span data-ttu-id="0121f-175">[Ajouter des utilisateurs et attribuer des licences en même temps](../../admin/add-users/add-users.md) (article)</span><span class="sxs-lookup"><span data-stu-id="0121f-175">[Add users and assign licenses at the same time](../../admin/add-users/add-users.md) (article)</span></span>
