---
title: Créer une boîte aux lettres partagée
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
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
ms.assetid: 871a246d-3acd-4bba-948e-5de8be0544c9
description: Créez une boîte aux lettres partagée pour permettre à plusieurs personnes au sein de votre entreprise de partager la responsabilité de la lecture du courrier électronique envoyé à une adresse et de la réponse à ces courriers.
ms.openlocfilehash: 35f1de41094c6bf3f806b3e8e01c0a67949c491e
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683246"
---
# <a name="create-a-shared-mailbox"></a><span data-ttu-id="e6360-103">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="e6360-103">Create a shared mailbox</span></span> 

> [!NOTE]
> <span data-ttu-id="e6360-104">Si votre organisation utilise un environnement hybride Exchange, vous devez utiliser le Centre d’administration Exchange (CAE) local pour créer et gérer des boîtes aux lettres partagées.</span><span class="sxs-lookup"><span data-stu-id="e6360-104">If your organization uses a hybrid Exchange environment, you should use the on-premises Exchange admin center (EAC) to create and manage shared mailboxes.</span></span> <span data-ttu-id="e6360-105">Consultez la rubrique [Créer des boîtes aux lettres partagées dans le Centre d’administration Exchange](/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?preserve-view=true.&view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="e6360-105">See [Create shared mailboxes in the Exchange admin center](/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?preserve-view=true.&view=exchserver-2019)</span></span><br><br>
> <span data-ttu-id="e6360-106">Si vous n'êtes pas sûr de devoir créer une boîte aux lettres partagée ou un groupe Microsoft 365 pour Outlook, voir [Comparer les groupes](../create-groups/compare-groups.md) pour plus de conseils.</span><span class="sxs-lookup"><span data-stu-id="e6360-106">If you're not sure if you should create a shared mailbox or a Microsoft 365 group for Outlook, see [Compare groups](../create-groups/compare-groups.md) for some guidance.</span></span> <span data-ttu-id="e6360-107">Sachez qu’il n’est pour l'instant pas possible de migrer une boîte aux lettres partagée vers un groupe Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e6360-107">Note that currently, it's not possible to migrate a shared mailbox to a Microsoft 365 group.</span></span> <span data-ttu-id="e6360-108">Si vous le souhaitez, dites-le nous en [votant ici](https://go.microsoft.com/fwlink/?linkid=871518).</span><span class="sxs-lookup"><span data-stu-id="e6360-108">If this is something you want, let us know by [voting here](https://go.microsoft.com/fwlink/?linkid=871518).</span></span>

<span data-ttu-id="e6360-p103">Vous pouvez facilement créer des boîtes aux lettres partagées de sorte qu’un groupe de personnes puisse surveiller et envoyer facilement du courrier électronique à partir d’une adresse de courrier commune, comme info@contoso.com. Quand une personne du groupe répond à un courrier envoyé à la boîte aux lettres partagée, la réponse semble provenir de la boîte aux lettres partagée et non de la personne.</span><span class="sxs-lookup"><span data-stu-id="e6360-p103">It's easy to create shared mailboxes so a group of people can monitor and send email from a common email addresses, like info@contoso.com. When a person in the group replies to a message sent to the shared mailbox, the email appears to be from the shared mailbox, not from the individual user.</span></span>

<span data-ttu-id="e6360-p104">Les boîtes aux lettres partagées incluent un calendrier partagé. Beaucoup de petites entreprises utilisent le calendrier partagé pour permettre à leurs employés d'y entrer leurs rendez-vous. Par exemple, si vous avez trois commerciaux qui effectuent des visites chez les clients, ces trois personnes peuvent utiliser le calendrier partagé pour saisir leurs rendez-vous. Tout le monde sait ainsi où elles se trouvent.</span><span class="sxs-lookup"><span data-stu-id="e6360-p104">Shared mailboxes include a shared calendar. A lot of small businesses like to use the shared calendar as a place for everyone to enter their appointments. For example, if you have 3 people who do customer visits, all can use the shared calendar to enter the appointments. This is an easy way to keep everyone informed where people are.</span></span>

<span data-ttu-id="e6360-115">Avant de créer une boîte aux lettres partagée, assurez-vous de lire la section [À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="e6360-115">Before creating a shared mailbox, be sure to read [About shared mailboxes](about-shared-mailboxes.md) for more information.</span></span>

## <a name="create-a-shared-mailbox-and-add-members"></a><span data-ttu-id="e6360-116">Créer une boîte aux lettres partagée et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="e6360-116">Create a shared mailbox and add members</span></span>
  
1. <span data-ttu-id="e6360-117">Connectez-vous à l’aide d’un compte d’administrateur général ou d’un compte d’administrateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="e6360-117">Sign in with a global admin account or Exchange admin account.</span></span> <span data-ttu-id="e6360-118">Si vous recevez le message « **Vous ne disposez pas des autorisations requises pour accéder à cette page ou effectuer cette action** », cela signifie que vous n’êtes pas un administrateur.</span><span class="sxs-lookup"><span data-stu-id="e6360-118">If you get the message "**You don't have permission to access this page or perform this action**," then you aren't an admin.</span></span> 

::: moniker range="o365-worldwide"

2. <span data-ttu-id="e6360-119">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-119">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

2. <span data-ttu-id="e6360-120">Dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=848041), accédez à la page **Groupes** \> **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="e6360-120">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=848041), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

2. <span data-ttu-id="e6360-121">Dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=850627), accédez à la page **Groupes** \> **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="e6360-121">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=850627), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end
    
3. <span data-ttu-id="e6360-122">Dans la page **Boîtes aux lettres partagées**, sélectionnez **+ Ajouter une boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="e6360-122">On the **Shared mailboxes** page, select **+ Add a mailbox**.</span></span> <span data-ttu-id="e6360-123">Entrez le nom de la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-123">Enter a name for the shared mailbox.</span></span> <span data-ttu-id="e6360-124">L’Assistant choisit ensuite l’adresse de courrier, que vous pouvez modifier si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e6360-124">Then the wizard chooses the email address, but you can edit it.</span></span>
    
    ![Donnez un nom à votre boîte aux lettres partagée.](../../media/e3035132-8986-4ec7-b7c0-f2752080d2c0.png)
  
4. <span data-ttu-id="e6360-126">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e6360-126">Select **Add**.</span></span> <span data-ttu-id="e6360-127">Quelques minutes peuvent être nécessaires avant que vous ne puissiez ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="e6360-127">It may take a few minutes before you can add members.</span></span>

5. <span data-ttu-id="e6360-128">Sous **Étapes suivantes**, sélectionnez **Ajouter des membres à cette boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="e6360-128">Under **Next steps**, select **Add members to this mailbox**.</span></span> <span data-ttu-id="e6360-129">Les membres représentent les personnes qui sont en mesure de consulter les courriers entrants dans cette boîte aux lettres partagée, ainsi que les réponses sortantes.</span><span class="sxs-lookup"><span data-stu-id="e6360-129">Members are the people who will be able to view the incoming mail to this shared mailbox, and the outgoing replies.</span></span>

   ![Sélectionnez Ajouter des membres](../../media/a2a72e3d-6170-40fe-a94f-0af8fbef8ab2.png)

6. <span data-ttu-id="e6360-131">Sélectionnez le bouton **+Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="e6360-131">Select the **+Add members** button.</span></span> <span data-ttu-id="e6360-132">Cochez la case en regard des personnes qui seront en mesure d'utiliser cette boîte aux lettres partagée, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="e6360-132">Put a check mark next to the people who you want to use this shared mailbox, and select **Save**.</span></span>

   ![Attribuer des membres à la boîte aux lettres partagée](../../media/e6c58953-f6d7-4f0b-97ba-308516bf2a94.png)

7. <span data-ttu-id="e6360-134">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e6360-134">Select **Close**.</span></span>

<span data-ttu-id="e6360-135">Vous bénéficiez à présent d’une boîte aux lettres partagée dotée d’un calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="e6360-135">You have a shared mailbox and it includes a shared calendar.</span></span> <span data-ttu-id="e6360-136">Passez maintenant à l'étape suivante : bloquer la connexion pour le compte de boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-136">Now go on to the next step: block sign-in for the shared mailbox account.</span></span>

## <a name="which-permissions-should-you-use"></a><span data-ttu-id="e6360-137">Quelles autorisations devez-vous utiliser ?</span><span class="sxs-lookup"><span data-stu-id="e6360-137">Which permissions should you use?</span></span>

<span data-ttu-id="e6360-138">Vous pouvez utiliser les autorisations suivantes avec une boîte aux lettres partagée :</span><span class="sxs-lookup"><span data-stu-id="e6360-138">You can use the following permissions with a shared mailbox:</span></span>

- <span data-ttu-id="e6360-139">**Accès total** : l'autorisation Accès total permet à un utilisateur d'ouvrir la boîte aux lettres partagée et d'agir comme le propriétaire de cette boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e6360-139">**Full Access**: The Full Access permission lets a user open the shared mailbox and act as the owner of that mailbox.</span></span> <span data-ttu-id="e6360-140">Après avoir accédé à la boîte aux lettres partagée, un utilisateur peut créer des éléments de calendrier, lire, afficher, supprimer et modifier des courriers électroniques, créer des tâches et contacts de calendrier.</span><span class="sxs-lookup"><span data-stu-id="e6360-140">After accessing the shared mailbox, a user can create calendar items, read, view, delete, and change email messages, and create tasks and calendar contacts.</span></span> <span data-ttu-id="e6360-141">Toutefois, un utilisateur doté d'une autorisation Accès total ne peut pas envoyer de messages à partir de la boîte aux lettres partagée à moins de disposer de l'autorisation Envoyer en tant que ou Envoyer de la part de.</span><span class="sxs-lookup"><span data-stu-id="e6360-141">However, a user with Full Access permission can't send email from the shared mailbox unless they also have Send As or Send on Behalf permission.</span></span>

- <span data-ttu-id="e6360-142">**Envoyer en tant que**: l'autorisation Envoyer en tant que permet à un utilisateur d'emprunter l'identité du propriétaire de la boîte aux lettres partagée pour envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="e6360-142">**Send As**: The Send As permission lets a user impersonate the shared mailbox when sending mail.</span></span> <span data-ttu-id="e6360-143">Par exemple, si Katerina se connecte à la boîte aux lettres partagée du service Marketing et envoie un message, le service Marketing semblera en être l'expéditeur.</span><span class="sxs-lookup"><span data-stu-id="e6360-143">For example, if Katerina logs into the shared mailbox Marketing Department and sends an email, it will look like the Marketing Department sent the email.</span></span>

- <span data-ttu-id="e6360-144">**Envoyer de la part de** : l’autorisation Envoyer de la part de permet à l’utilisateur d’envoyer des messages de la part de la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-144">**Send on Behalf**: The Send on Behalf permission lets a user send email on behalf of the shared mailbox.</span></span> <span data-ttu-id="e6360-145">Par exemple, si John se connecte à la boîte aux lettres partagée Reception Building 32 et envoie un message, ce dernier semblera avoir été envoyé par « John de la part de Reception Building 32 ».</span><span class="sxs-lookup"><span data-stu-id="e6360-145">For example, if John logs into the shared mailbox Reception Building 32 and sends an email, it will look like the mail was sent by "John on behalf of Reception Building 32".</span></span> <span data-ttu-id="e6360-146">Vous ne pouvez pas utiliser le Centre d’administration Exchange pour accorder l’autorisation « Envoyer de la part de ». Pour ce faire, vous devez utiliser l’applet de commande **Set-Mailbox** avec le paramètre _GrantSendonBehalf_.</span><span class="sxs-lookup"><span data-stu-id="e6360-146">You can't use the EAC to grant Send on Behalf permissions, you must use the **Set-Mailbox** cmdlet with the _GrantSendonBehalf_ parameter.</span></span>

### <a name="use-the-eac-to-edit-shared-mailbox-delegation"></a><span data-ttu-id="e6360-147">Utiliser le CAE pour modifier la délégation de boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="e6360-147">Use the EAC to edit shared mailbox delegation</span></span>

1. <span data-ttu-id="e6360-148">Dans le CAE, accédez à **Destinataires** \> **Partagé**.</span><span class="sxs-lookup"><span data-stu-id="e6360-148">In the EAC, go to **Recipients** \> **Shared**.</span></span> <span data-ttu-id="e6360-149">Sélectionnez la boîte aux lettres partagée, puis **Modifier** ![Icône Modifier](../../media/ITPro-EAC-EditIcon.png)..</span><span class="sxs-lookup"><span data-stu-id="e6360-149">Select the shared mailbox, and then select **Edit** ![Edit icon](../../media/ITPro-EAC-EditIcon.png).</span></span>

2. <span data-ttu-id="e6360-150">Sélectionnez **Délégation de boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="e6360-150">Select **Mailbox delegation**.</span></span>

3. <span data-ttu-id="e6360-151">Pour accorder ou supprimer les autorisations Accès total et Envoyer en tant que, sélectionnez **Ajouter** ![Ajoute une icône](../../media/ITPro-EAC-AddIcon.png) ou sur **Supprimer** ![Supprimer une icône](../../media/ITPro-EAC-RemoveIcon.gif), puis sélectionnez les utilisateurs auxquels vous souhaitez accorder ou retirer les autorisations.</span><span class="sxs-lookup"><span data-stu-id="e6360-151">To grant or remove Full Access and Send As permissions, select **Add** ![Add Icon](../../media/ITPro-EAC-AddIcon.png) or **Remove** ![Remove icon](../../media/ITPro-EAC-RemoveIcon.gif) and then select the users you want to grant permissions to.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e6360-p115">L'autorisation Accès total permet aux utilisateurs d'ouvrir la boîte aux lettres, d'y créer des éléments et de les modifier. L'autorisation Envoyer en tant que permet à toute personne autre que le propriétaire de la boîte aux lettres d'envoyer des courriers électroniques à partir de cette boîte aux lettres partagée. Les deux autorisations sont requises pour que la boîte aux lettres partagée fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e6360-p115">The Full Access permission allows a user to open the mailbox as well as create and modify items in it. The Send As permission allows anyone other than the mailbox owner to send email from this shared mailbox. Both permissions are required for successful shared mailbox operation.</span></span>

4. <span data-ttu-id="e6360-155">Sélectionnez **Enregistrer** pour enregistrer vos modifications.</span><span class="sxs-lookup"><span data-stu-id="e6360-155">Select **Save** to save your changes.</span></span>


## <a name="block-sign-in-for-the-shared-mailbox-account"></a><span data-ttu-id="e6360-156">Bloquez la connexion pour le compte de boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-156">Block sign-in for the shared mailbox account</span></span>

<span data-ttu-id="e6360-157">Chaque boîte aux lettres partagée a un compte d'utilisateur correspondant.</span><span class="sxs-lookup"><span data-stu-id="e6360-157">Every shared mailbox has a corresponding user account.</span></span> <span data-ttu-id="e6360-158">Vous n'avez pas été invité à fournir un mot de passe lors de la création de la boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="e6360-158">Notice how you weren't asked to provide a password when you created the shared mailbox?</span></span> <span data-ttu-id="e6360-159">Le compte a un mot de passe qui est généré par le système (inconnu).</span><span class="sxs-lookup"><span data-stu-id="e6360-159">The account has a password, but it's system-generated (unknown).</span></span> <span data-ttu-id="e6360-160">Vous n'êtes pas censé utiliser le compte pour vous connecter à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-160">You aren't supposed to use the account to log in to the shared mailbox.</span></span>

<span data-ttu-id="e6360-161">Mais que se passe-t-il si un administrateur se contente de réinitialiser le mot de passe du compte d'utilisateur de la boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="e6360-161">But what if an admin simply resets the password of the shared mailbox user account?</span></span> <span data-ttu-id="e6360-162">Ou que se passe-t-il si un utilisateur malveillant accède aux informations d’identification du compte de boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="e6360-162">Or what if an attacker gains access to the shared mailbox account credentials?</span></span> <span data-ttu-id="e6360-163">Cela permettrait au compte d’utilisateur de se connecter à la boîte aux lettres partagée et d'envoyer des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="e6360-163">This would allow the user account to log in to the shared mailbox and send email.</span></span> <span data-ttu-id="e6360-164">Pour empêcher cela, vous devez bloquer la connexion pour le compte qui est associé à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-164">To prevent this, you need to block sign-in for the account that's associated with the shared mailbox.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="e6360-165">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-165">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="e6360-166">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-166">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="e6360-167">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-167">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>
::: moniker-end

1. <span data-ttu-id="e6360-168">Dans la liste des comptes d’utilisateurs, recherchez le compte de la boîte aux lettres partagée (par exemple, remplacez le filtre par **Utilisateurs sans licence**).</span><span class="sxs-lookup"><span data-stu-id="e6360-168">In the list of user accounts, find the account for the shared mailbox (for example, change the filter to **Unlicensed users**).</span></span>

1. <span data-ttu-id="e6360-169">Sélectionnez l’utilisateur pour ouvrir son volet de propriétés, puis sélectionnez l’icône **Bloquer cet utilisateur** ![Capture d’écran de l’icône Bloquer cet utilisateur](../../media/block-user-icon.png).</span><span class="sxs-lookup"><span data-stu-id="e6360-169">Select the user to open their properties pane, and then select the **Block this user** icon ![Screen shot of the Block this user icon](../../media/block-user-icon.png).</span></span>

   <span data-ttu-id="e6360-170">**Remarque** : si le compte est déjà bloqué, **Connexion bloquée** s’affiche dans la partie supérieure et l’icône indique **Débloquer cet utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="e6360-170">**Note**: If the account is already blocked, **Sign in blocked** will appear at the top and the icon will read **Unblock this user**.</span></span>

1. <span data-ttu-id="e6360-171">Dans le volet **Bloquer cet utilisateur ?**, sélectionnez **Empêcher l'utilisateur de se connecter**, puis sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="e6360-171">In the **Block this user?** pane, select **Block the user from signing in**, and then select **Save changes**.</span></span>

<span data-ttu-id="e6360-172">Pour obtenir des instructions sur la manière de bloquer des comptes d’utilisateurs avec Azure AD PowerShell (y compris de nombreux comptes en même temps), voir [Bloquer des comptes d’utilisateurs avec Office 365 PowerShell](../../enterprise/block-user-accounts-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="e6360-172">For instructions on how to block sign-in for accounts using Azure AD PowerShell (including many accounts at the same time), see [Block user accounts with Office 365 PowerShell](../../enterprise/block-user-accounts-with-microsoft-365-powershell.md).</span></span>

## <a name="add-the-shared-mailbox-to-outlook"></a><span data-ttu-id="e6360-173">Ajouter la boîte aux lettres partagée à Outlook</span><span class="sxs-lookup"><span data-stu-id="e6360-173">Add the shared mailbox to Outlook</span></span>

<span data-ttu-id="e6360-174">Si le mappage automatique est activé dans votre entreprise (par défaut, la plupart des personnes utilisent cette option), la boîte aux lettres partagée apparaîtra automatiquement dans l’application Outlook de vos utilisateurs, après qu’ils auront fermé et redémarré Outlook.</span><span class="sxs-lookup"><span data-stu-id="e6360-174">If you have automapping enabled in your business (by default, most people do), the shared mailbox will appear in your user's Outlook app automatically after they close and restart Outlook.</span></span> 

<span data-ttu-id="e6360-175">Le mappage automatique est défini sur les boîtes aux lettres des utilisateurs, et non sur la boîte aux lettres partagée.  </span><span class="sxs-lookup"><span data-stu-id="e6360-175">Automapping is set on the user's mailbox, not the shared mailbox.</span></span> <span data-ttu-id="e6360-176">Par conséquent, si vous essayez d'utiliser un groupe de sécurité pour gérer les personnes autorisées à accéder à la boîte aux lettres partagée, le mappage automatique ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="e6360-176">This means if you try to use a security group to manage who has access to the shared mailbox, automapping won't work.</span></span> <span data-ttu-id="e6360-177">Par conséquent, si vous voulez utiliser le mappage automatique, vous devez attribuer des autorisations de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="e6360-177">So, if you want automapping, you have to assign permissions explicitly.</span></span> <span data-ttu-id="e6360-178">Le mappage automatique est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="e6360-178">Automapping is on by default.</span></span> <span data-ttu-id="e6360-179">Pour découvrir comment désactiver ce service, voir [Supprimer le mappage automatique d’une boîte aux lettres partagée](/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox).</span><span class="sxs-lookup"><span data-stu-id="e6360-179">To learn how to turn it off, see [Remove automapping for a shared mailbox](/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox).</span></span>

<span data-ttu-id="e6360-180">Pour plus d’informations sur les boîtes aux lettres partagées dans Outlook, voir :</span><span class="sxs-lookup"><span data-stu-id="e6360-180">To learn more about shared mailboxes in Outlook, see:</span></span>

- <span data-ttu-id="e6360-181"><a href="https://support.microsoft.com/office/d94a8e9e-21f1-4240-808b-de9c9c088afd" target="_blank">Ouvrir et utiliser une boîte aux lettres partagée dans Outlook</a></span><span class="sxs-lookup"><span data-stu-id="e6360-181"><a href="https://support.microsoft.com/office/d94a8e9e-21f1-4240-808b-de9c9c088afd" target="_blank">Open and use a shared mailbox in Outlook</a></span></span>

- <span data-ttu-id="e6360-182"><a href="https://support.microsoft.com/office/98b5a90d-4e38-415d-a030-f09a4cd28207" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook sur le web</a></span><span class="sxs-lookup"><span data-stu-id="e6360-182"><a href="https://support.microsoft.com/office/98b5a90d-4e38-415d-a030-f09a4cd28207" target="_blank">Add a shared mailbox to Outlook on the web</a></span></span>

- <span data-ttu-id="e6360-183"><a href="https://support.microsoft.com/office/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Ajoutez une boîte aux lettres partagée dans Outlook Mobile</a></span><span class="sxs-lookup"><span data-stu-id="e6360-183"><a href="https://support.microsoft.com/office/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a></span></span>

- <span data-ttu-id="e6360-184"><a href="https://support.microsoft.com/office/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2" target="_blank">Ouvrir un dossier ou une boîte aux lettres partagée dans Outlook pour Mac</a></span><span class="sxs-lookup"><span data-stu-id="e6360-184"><a href="https://support.microsoft.com/office/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2" target="_blank">Open a shared folder or mailbox in Outlook for Mac</a></span></span>

- <span data-ttu-id="e6360-185"><a href="https://support.microsoft.com/office/b0963400-2a51-4c64-afc7-b816d737d164" target="_blank">Ajouter des règles de boîte aux lettres partagée</a></span><span class="sxs-lookup"><span data-stu-id="e6360-185"><a href="https://support.microsoft.com/office/b0963400-2a51-4c64-afc7-b816d737d164" target="_blank">Add rules to a shared mailbox</a></span></span>

## <a name="use-a-shared-mailbox-on-a-mobile-device-phone-or-tablet"></a><span data-ttu-id="e6360-186">Utiliser une boîte aux lettres partagée sur un appareil mobile (téléphone ou tablette)</span><span class="sxs-lookup"><span data-stu-id="e6360-186">Use a shared mailbox on a mobile device (phone or tablet)</span></span>

<span data-ttu-id="e6360-187">Vous pouvez accéder à une boîte aux lettres partagée sur un appareil mobile de deux manières :</span><span class="sxs-lookup"><span data-stu-id="e6360-187">You can access a shared mailbox on a mobile device in two ways:</span></span>
- <span data-ttu-id="e6360-188">Ajoutez la boîte aux lettres partagée dans l'<a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">application Outlook pour iOS</a> ou l'<a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">application mobile Outlook pour Android</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-188">Add the shared mailbox in the <a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">Outlook for iOS app</a> or the <a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">Outlook for Android mobile app</a>.</span></span> 
    
    <span data-ttu-id="e6360-189">Pour les instructions, voir <a href="https://support.microsoft.com/office/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook Mobile</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-189">For instructions, see <a href="https://support.microsoft.com/office/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a>.</span></span>

- <span data-ttu-id="e6360-190">Ouvrez votre navigateur, connectez-vous, puis accédez à Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="e6360-190">Open your browser, sign in, and then go to Outlook on the web.</span></span> <span data-ttu-id="e6360-191">À partir d’Outlook sur le web, vous pouvez accéder à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-191">From Outlook on the web you'll be able to access the shared mailbox.</span></span>

    <span data-ttu-id="e6360-192">Pour les instructions, voir <a href="https://support.microsoft.com/office/98b5a90d-4e38-415d-a030-f09a4cd28207" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook sur le web</a>.</span><span class="sxs-lookup"><span data-stu-id="e6360-192">For instructions, see <a href="https://support.microsoft.com/office/98b5a90d-4e38-415d-a030-f09a4cd28207" target="_blank">Add a shared mailbox to Outlook on the web</a>.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e6360-193">Une boîte aux lettres partagée peut uniquement être ajoutée à l’application Outlook pour iOS ou à l’application mobile Outlook pour Android</span><span class="sxs-lookup"><span data-stu-id="e6360-193">Shared mailbox can only be added to Outlook for iOS app or the Outlook for Android mobile app</span></span>

## <a name="use-the-shared-calendar"></a><span data-ttu-id="e6360-194">Utiliser le calendrier partagé</span><span class="sxs-lookup"><span data-stu-id="e6360-194">Use the shared calendar</span></span>

<span data-ttu-id="e6360-p120">La création de votre boîte aux lettres partagée entraîne automatiquement la création d’un calendrier partagé. Nous vous recommandons d’utiliser ce calendrier plutôt qu’un calendrier SharePoint pour effectuer le suivi de vos rendez-vous et de la localisation de vos contacts. Un calendrier partagé est intégré avec Outlook et est beaucoup plus facile à utiliser que celui de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e6360-p120">When you created the shared mailbox, you automatically created a shared calendar. We like the shared mailbox calendar rather than a SharePoint calendar for keeping track of appointments and where people are. A shared calendar is integrated with Outlook and it's much easier to use than a SharePoint calendar.</span></span>

1. <span data-ttu-id="e6360-198">Dans l'application Outlook, accédez à l'affichage Calendrier, puis sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="e6360-198">In the Outlook app, go to calendar view, and select the shared mailbox.</span></span>

2. <span data-ttu-id="e6360-199">Lorsque vous entrez des rendez-vous, chaque membre de la boîte aux lettres partagée peut les voir.</span><span class="sxs-lookup"><span data-stu-id="e6360-199">When you enter appointments, everyone who is a member of the shared mailbox will be able to see them.</span></span>

3. <span data-ttu-id="e6360-200">N’importe quel membre de la boîte aux lettres partagée peut créer, afficher et gérer des rendez-vous dans le calendrier, tout comme ils le feraient leurs rendez-vous personnels.</span><span class="sxs-lookup"><span data-stu-id="e6360-200">Any member of the shared mailbox can create, view, and manage appointments on the calendar, just like they would their personal appointments.</span></span> <span data-ttu-id="e6360-201">Tous les membres de la boîte aux lettres partagée peuvent voir les modifications apportées au calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="e6360-201">Everyone who is a member of shared mailbox can see their changes to the shared calendar.</span></span>

## <a name="related-content"></a><span data-ttu-id="e6360-202">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="e6360-202">Related content</span></span>

<span data-ttu-id="e6360-203">[À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e6360-203">[About shared mailboxes](about-shared-mailboxes.md) (article)</span></span>\
<span data-ttu-id="e6360-204">[Configurer une boîte aux lettres partagée](configure-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e6360-204">[Configure a shared mailbox](configure-a-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="e6360-205">[Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée](convert-user-mailbox-to-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e6360-205">[Convert a user mailbox to a shared mailbox](convert-user-mailbox-to-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="e6360-206">[Supprimer une licence d’une boîte aux lettres partagée](remove-license-from-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e6360-206">[Remove a license from a shared mailbox](remove-license-from-shared-mailbox.md) (article)</span></span>\
<span data-ttu-id="e6360-207">[Résoudre les problèmes liés aux boîtes aux lettres partagées](resolve-issues-with-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="e6360-207">[Resolve issues with shared mailboxes](resolve-issues-with-shared-mailboxes.md) (article)</span></span>