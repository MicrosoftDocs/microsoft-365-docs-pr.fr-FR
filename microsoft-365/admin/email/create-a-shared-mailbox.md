---
title: Créer une boîte aux lettres partagée
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 871a246d-3acd-4bba-948e-5de8be0544c9
description: Créez une boîte aux lettres partagée pour permettre à plusieurs personnes au sein de votre entreprise de partager la responsabilité de la lecture du courrier électronique envoyé à une adresse et de la réponse à ces courriers.
ms.openlocfilehash: 4469197628feb96980ec2d8b560048acba704c54
ms.sourcegitcommit: 4a34b48584071e0c43c920bb35025e34cb4f5d15
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "43212304"
---
# <a name="create-a-shared-mailbox"></a><span data-ttu-id="ab654-103">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="ab654-103">Create a shared mailbox</span></span> 

> [!NOTE]
> <span data-ttu-id="ab654-104">Si votre organisation utilise un environnement hybride Exchange, vous devez utiliser le Centre d’administration Exchange (CAE) local pour créer et gérer des boîtes aux lettres partagées.</span><span class="sxs-lookup"><span data-stu-id="ab654-104">If your organization uses a hybrid Exchange environment, you should use the on-premises Exchange admin center (EAC) to create and manage shared mailboxes.</span></span> <span data-ttu-id="ab654-105">Consultez la rubrique [Créer des boîtes aux lettres partagées dans le Centre d’administration Exchange](https://docs.microsoft.com/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?view=exchserver-2019.)</span><span class="sxs-lookup"><span data-stu-id="ab654-105">See [Create shared mailboxes in the Exchange admin center](https://docs.microsoft.com/Exchange/collaboration/shared-mailboxes/create-shared-mailboxes?view=exchserver-2019.)</span></span><br><br>
> <span data-ttu-id="ab654-106">Si vous n'êtes pas sûr de devoir créer une boîte aux lettres partagée ou un groupe Office 365 pour Outlook, voir [Comparer les groupes](../create-groups/compare-groups.md) pour plus de conseils.</span><span class="sxs-lookup"><span data-stu-id="ab654-106">If you're not sure if you should create a shared mailbox or an Office 365 Group for Outlook, see [Compare groups](../create-groups/compare-groups.md) for some guidance.</span></span> <span data-ttu-id="ab654-107">Sachez qu’il n’est pour l'instant pas possible de migrer une boîte aux lettres partagée vers un groupe Office 365.</span><span class="sxs-lookup"><span data-stu-id="ab654-107">Note that currently, it's not possible to migrate a shared mailbox to an Office 365 Group.</span></span> <span data-ttu-id="ab654-108">Si vous le souhaitez, dites-le nous en [votant ici](https://go.microsoft.com/fwlink/?linkid=871518).</span><span class="sxs-lookup"><span data-stu-id="ab654-108">If this is something you want, let us know by [voting here](https://go.microsoft.com/fwlink/?linkid=871518).</span></span>

<span data-ttu-id="ab654-p103">Vous pouvez facilement créer des boîtes aux lettres partagées de sorte qu’un groupe de personnes puisse surveiller et envoyer facilement du courrier électronique à partir d’une adresse de courrier commune, comme info@contoso.com. Quand une personne du groupe répond à un courrier envoyé à la boîte aux lettres partagée, la réponse semble provenir de la boîte aux lettres partagée et non de la personne.</span><span class="sxs-lookup"><span data-stu-id="ab654-p103">It's easy to create shared mailboxes so a group of people can monitor and send email from a common email addresses, like info@contoso.com. When a person in the group replies to a message sent to the shared mailbox, the email appears to be from the shared mailbox, not from the individual user.</span></span>

<span data-ttu-id="ab654-111">Les boîtes aux lettres partagées incluent un calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="ab654-111">Shared mailboxes include a shared calendar.</span></span> <span data-ttu-id="ab654-112">Un grand nombre de petites entreprises préfèrent utiliser un calendrier partagé pour que tous les employés y entrent leurs rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="ab654-112">A lot of small businesses like to use the shared calendar as a place for everyone to enter their appointments.</span></span> <span data-ttu-id="ab654-113">Par exemple, si vous avez 3 commerciaux dans votre entreprise qui effectuent des visites chez les clients, ces 3 personnes peuvent utiliser le calendrier partagé pour saisir les rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="ab654-113">For example, if you have 3 people who do customer visits, all can use the shared calendar to enter the appointments.</span></span> <span data-ttu-id="ab654-114">Tout le monde sait ainsi où elles se trouvent.</span><span class="sxs-lookup"><span data-stu-id="ab654-114">This is an easy way to keep everyone informed where people are.</span></span>

<span data-ttu-id="ab654-115">Avant de créer une boîte aux lettres partagée, assurez-vous de lire la section [À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="ab654-115">Before creating a shared mailbox, be sure to read [About shared mailboxes](about-shared-mailboxes.md) for more information.</span></span>

## <a name="create-a-shared-mailbox-and-add-members"></a><span data-ttu-id="ab654-116">Créer une boîte aux lettres partagée et ajouter des membres</span><span class="sxs-lookup"><span data-stu-id="ab654-116">Create a shared mailbox and add members</span></span>
  
1. <span data-ttu-id="ab654-117">Connectez-vous avec un compte Administrateur général Office 365 ou un compte Administrateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab654-117">Sign in with an Office 365 global admin account or Exchange admin account.</span></span> <span data-ttu-id="ab654-118">Si vous recevez le message « **Vous ne disposez pas des autorisations requises pour accéder à cette page ou effectuer cette action** », cela signifie que vous n’êtes pas un administrateur.</span><span class="sxs-lookup"><span data-stu-id="ab654-118">If you get the message "**You don't have permission to access this page or perform this action**," then you aren't an admin.</span></span> 

::: moniker range="o365-worldwide"

2. <span data-ttu-id="ab654-119">Dans le Centre d’administration, accédez à la page **Groupes** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Boîtes aux lettres partagées</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-119">In the admin center, go to the **Groups** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2066847" target="_blank">Shared mailboxes</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

2. <span data-ttu-id="ab654-120">Dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=848041), accédez à la page **Groupes** \> **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="ab654-120">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=848041), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

2. <span data-ttu-id="ab654-121">Dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=850627), accédez à la page **Groupes** \> **Boîtes aux lettres partagées**.</span><span class="sxs-lookup"><span data-stu-id="ab654-121">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=850627), go to the **Groups** \> **Shared mailboxes** page.</span></span>

::: moniker-end
    
3. <span data-ttu-id="ab654-122">Dans la page **Boîtes aux lettres partagées**, sélectionnez **+ Ajouter une boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="ab654-122">On the **Shared mailboxes** page, select **+ Add a mailbox**.</span></span> <span data-ttu-id="ab654-123">Entrez le nom de la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-123">Enter a name for the shared mailbox.</span></span> <span data-ttu-id="ab654-124">L’Assistant choisit ensuite l’adresse de courrier, que vous pouvez modifier si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="ab654-124">Then the wizard chooses the email address, but you can edit it.</span></span>
    
    ![Donnez un nom à votre boîte aux lettres partagée.](../../media/e3035132-8986-4ec7-b7c0-f2752080d2c0.png)
  
4. <span data-ttu-id="ab654-126">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ab654-126">Select **Add**.</span></span> <span data-ttu-id="ab654-127">Quelques minutes peuvent être nécessaires avant que vous ne puissiez ajouter des membres.</span><span class="sxs-lookup"><span data-stu-id="ab654-127">It may take a few minutes before you can add members.</span></span>

5. <span data-ttu-id="ab654-128">Sous **Étapes suivantes**, sélectionnez **Ajouter des membres à cette boîte aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="ab654-128">Under **Next steps**, select **Add members to this mailbox**.</span></span> <span data-ttu-id="ab654-129">Les membres représentent les personnes qui sont en mesure de consulter les courriers entrants dans cette boîte aux lettres partagée, ainsi que les réponses sortantes.</span><span class="sxs-lookup"><span data-stu-id="ab654-129">Members are the people who will be able to view the incoming mail to this shared mailbox, and the outgoing replies.</span></span>

   ![Sélectionnez Ajouter des membres](../../media/a2a72e3d-6170-40fe-a94f-0af8fbef8ab2.png)

6. <span data-ttu-id="ab654-131">Sélectionnez le bouton **+Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="ab654-131">Select the **+Add members** button.</span></span> <span data-ttu-id="ab654-132">Cochez la case en regard des personnes qui seront en mesure d'utiliser cette boîte aux lettres partagée, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ab654-132">Put a check mark next to the people who you want to use this shared mailbox, and select **Save**.</span></span>

   ![Attribuer des membres à la boîte aux lettres partagée](../../media/e6c58953-f6d7-4f0b-97ba-308516bf2a94.png)

7. <span data-ttu-id="ab654-134">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab654-134">Select **Close**.</span></span>

<span data-ttu-id="ab654-135">Vous bénéficiez à présent d’une boîte aux lettres partagée dotée d’un calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="ab654-135">You have a shared mailbox and it includes a shared calendar.</span></span> <span data-ttu-id="ab654-136">Passez maintenant à l'étape suivante : bloquer la connexion pour le compte de boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-136">Now go on to the next step: block sign-in for the shared mailbox account.</span></span>

## <a name="block-sign-in-for-the-shared-mailbox-account"></a><span data-ttu-id="ab654-137">Bloquez la connexion pour le compte de boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-137">Block sign-in for the shared mailbox account</span></span>

<span data-ttu-id="ab654-138">Chaque boîte aux lettres partagée a un compte d'utilisateur correspondant.</span><span class="sxs-lookup"><span data-stu-id="ab654-138">Every shared mailbox has a corresponding user account.</span></span> <span data-ttu-id="ab654-139">Vous n'avez pas été invité à fournir un mot de passe lors de la création de la boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="ab654-139">Notice how you weren't asked to provide a password when you created the shared mailbox?</span></span> <span data-ttu-id="ab654-140">Le compte a un mot de passe qui est généré par le système (inconnu).</span><span class="sxs-lookup"><span data-stu-id="ab654-140">The account has a password, but it's system-generated (unknown).</span></span> <span data-ttu-id="ab654-141">Vous n'êtes pas censé utiliser le compte pour vous connecter à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-141">You aren't supposed to use the account to log in to the shared mailbox.</span></span>

<span data-ttu-id="ab654-142">Mais que se passe-t-il si un administrateur se contente de réinitialiser le mot de passe du compte d'utilisateur de la boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="ab654-142">But what if an admin simply resets the password of the shared mailbox user account?</span></span> <span data-ttu-id="ab654-143">Ou que se passe-t-il si un utilisateur malveillant accède aux informations d’identification du compte de boîte aux lettres partagée ?</span><span class="sxs-lookup"><span data-stu-id="ab654-143">Or what if an attacker gains access to the shared mailbox account credentials?</span></span> <span data-ttu-id="ab654-144">Cela permettrait au compte d’utilisateur de se connecter à la boîte aux lettres partagée et d'envoyer des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="ab654-144">This would allow the user account to log in to the shared mailbox and send email.</span></span> <span data-ttu-id="ab654-145">Pour empêcher cela, vous devez bloquer la connexion pour le compte qui est associé à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-145">To prevent this, you need to block sign-in for the account that's associated with the shared mailbox.</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="ab654-146">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="ab654-146">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="ab654-147">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-147">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="ab654-148">Dans la liste des comptes d’utilisateurs, recherchez le compte de la boîte aux lettres partagée (par exemple, remplacez le filtre par **Utilisateurs sans licence**).</span><span class="sxs-lookup"><span data-stu-id="ab654-148">In the list of user accounts, find the account for the shared mailbox (for example, change the filter to **Unlicensed users**).</span></span>

3. <span data-ttu-id="ab654-149">Sélectionnez l’utilisateur pour ouvrir son volet de propriétés, puis sélectionnez l’icône **Bloquer cet utilisateur** ![Capture d’écran de l’icône Bloquer cet utilisateur](../../media/block-user-icon.png).</span><span class="sxs-lookup"><span data-stu-id="ab654-149">Select the user to open their properties pane, and then select the **Block this user** icon ![Screen shot of the Block this user icon](../../media/block-user-icon.png).</span></span>

   <span data-ttu-id="ab654-150">**Remarque** : si le compte est déjà bloqué, **Connexion bloquée** s’affiche dans la partie supérieure et l’icône indique **Débloquer cet utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ab654-150">**Note**: If the account is already blocked, **Sign in blocked** will appear at the top and the icon will read **Unblock this user**.</span></span>

4. <span data-ttu-id="ab654-151">Dans le volet **Bloquer cet utilisateur ?**, sélectionnez **Empêcher l'utilisateur de se connecter**, puis sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="ab654-151">In the **Block this user?** pane, select **Block the user from signing in**, and then select **Save changes**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="ab654-152">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-152">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="ab654-153">Dans la liste des comptes d’utilisateurs, recherchez le compte de la boîte aux lettres partagée (par exemple, remplacez l’affichage par **Utilisateurs sans licence**), puis sélectionnez le compte.</span><span class="sxs-lookup"><span data-stu-id="ab654-153">In the list of user accounts, find the account for the shared mailbox (for example, change the view to **Unlicensed users**) and then select the account.</span></span>

3. <span data-ttu-id="ab654-154">Dans le menu contextuel des propriétés, sélectionnez **Bloquer la connexion**.</span><span class="sxs-lookup"><span data-stu-id="ab654-154">In the properties flyout, select **Block sign-in**.</span></span>

    <span data-ttu-id="ab654-155">**Remarque :** si le compte était déjà bloqué, le bouton indiquerait **Débloquer la connexion**.</span><span class="sxs-lookup"><span data-stu-id="ab654-155">**Note:** If the account was already blocked, the button would say **Unblock sign-in**.</span></span>

4. <span data-ttu-id="ab654-156">Dans le menu contextuel **Modifier le statut de la connexion**, vérifiez que l’option Empêcher l’utilisateur de se connecter est activée, sélectionnez **Enregistrer** puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab654-156">In the **Edit sign-in status** flyout, verify that Block the user from signing in is selected, select **Save** and then **Close**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="ab654-157">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-157">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="ab654-158">Dans la liste des comptes d’utilisateurs, recherchez le compte de la boîte aux lettres partagée (par exemple, remplacez l’affichage par **Utilisateurs sans licence**), puis sélectionnez le compte.</span><span class="sxs-lookup"><span data-stu-id="ab654-158">In the list of user accounts, find the account for the shared mailbox (for example, change the view to **Unlicensed users**) and then select the account.</span></span>

3. <span data-ttu-id="ab654-159">Dans le menu contextuel des propriétés, sélectionnez **Bloquer la connexion**.</span><span class="sxs-lookup"><span data-stu-id="ab654-159">In the properties flyout, select **Block sign-in**.</span></span>

    <span data-ttu-id="ab654-160">**Remarque :** si le compte était déjà bloqué, le bouton indiquerait **Débloquer la connexion**.</span><span class="sxs-lookup"><span data-stu-id="ab654-160">**Note:** If the account was already blocked, the button would say **Unblock sign-in**.</span></span>

4. <span data-ttu-id="ab654-161">Dans le menu contextuel **Modifier le statut de la connexion**, vérifiez que l’option Empêcher l’utilisateur de se connecter est activée, sélectionnez **Enregistrer** puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab654-161">In the **Edit sign-in status** flyout, verify that Block the user from signing in is selected, select **Save** and then **Close**.</span></span>
::: moniker-end

<span data-ttu-id="ab654-162">Pour obtenir des instructions sur la manière de bloquer des comptes d’utilisateurs avec Azure AD PowerShell (y compris de nombreux comptes en même temps), voir [Bloquer des comptes d’utilisateurs avec Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/block-user-accounts-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="ab654-162">For instructions on how to block sign-in for accounts using Azure AD PowerShell (including many accounts at the same time), see [Block user accounts with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/block-user-accounts-with-office-365-powershell).</span></span>

## <a name="add-the-shared-mailbox-to-outlook"></a><span data-ttu-id="ab654-163">Ajouter la boîte aux lettres partagée à Outlook</span><span class="sxs-lookup"><span data-stu-id="ab654-163">Add the shared mailbox to Outlook</span></span>

<span data-ttu-id="ab654-164">Si le mappage automatique est activé dans votre entreprise (par défaut, la plupart des personnes utilisent cette option), la boîte aux lettres partagée apparaîtra automatiquement dans l’application Outlook de vos utilisateurs, après qu’ils auront fermé et redémarré Outlook.</span><span class="sxs-lookup"><span data-stu-id="ab654-164">If you have automapping enabled in your business (by default, most people do), the shared mailbox will appear in your user's Outlook app automatically after they close and restart Outlook.</span></span> 

<span data-ttu-id="ab654-165">Le mappage automatique est défini sur les boîtes aux lettres des utilisateurs, et non sur la boîte aux lettres partagée.  </span><span class="sxs-lookup"><span data-stu-id="ab654-165">Automapping is set on the user's mailbox, not the shared mailbox.</span></span> <span data-ttu-id="ab654-166">Par conséquent, si vous essayez d'utiliser un groupe de sécurité pour gérer les personnes autorisées à accéder à la boîte aux lettres partagée, le mappage automatique ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="ab654-166">This means if you try to use a security group to manage who has access to the shared mailbox, automapping won't work.</span></span> <span data-ttu-id="ab654-167">Par conséquent, si vous voulez utiliser le mappage automatique, vous devez attribuer des autorisations de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="ab654-167">So, if you want automapping, you have to assign permissions explicitly.</span></span> <span data-ttu-id="ab654-168">Le mappage automatique est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab654-168">Automapping is on by default.</span></span> <span data-ttu-id="ab654-169">Pour découvrir comment désactiver ce service, voir [Supprimer le mappage automatique d’une boîte aux lettres partagée](https://docs.microsoft.com/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox).</span><span class="sxs-lookup"><span data-stu-id="ab654-169">To learn how to turn it off, see [Remove automapping for a shared mailbox](https://docs.microsoft.com/office365/troubleshoot/administration/remove-automapping-for-shared-mailbox).</span></span>

<span data-ttu-id="ab654-170">Pour plus d’informations sur les boîtes aux lettres partagées dans Outlook, voir :</span><span class="sxs-lookup"><span data-stu-id="ab654-170">To learn more about shared mailboxes in Outlook, see:</span></span>

- <span data-ttu-id="ab654-171"><a href="https://support.office.com/article/d94a8e9e-21f1-4240-808b-de9c9c088afd.aspx" target="_blank">Ouvrir et utiliser une boîte aux lettres partagée dans Outlook</a></span><span class="sxs-lookup"><span data-stu-id="ab654-171"><a href="https://support.office.com/article/d94a8e9e-21f1-4240-808b-de9c9c088afd.aspx" target="_blank">Open and use a shared mailbox in Outlook</a></span></span>

- <span data-ttu-id="ab654-172"><a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook sur le web</a></span><span class="sxs-lookup"><span data-stu-id="ab654-172"><a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Add a shared mailbox to Outlook on the web</a></span></span>

- <span data-ttu-id="ab654-173"><a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Ajoutez une boîte aux lettres partagée dans Outlook Mobile</a></span><span class="sxs-lookup"><span data-stu-id="ab654-173"><a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a></span></span>

- <span data-ttu-id="ab654-174"><a href="https://support.office.com/article/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2.aspx" target="_blank">Ouvrir un dossier ou une boîte aux lettres partagée dans Outlook pour Mac</a></span><span class="sxs-lookup"><span data-stu-id="ab654-174"><a href="https://support.office.com/article/6ecc39c5-5577-4a1d-b18c-bbdc92972cb2.aspx" target="_blank">Open a shared folder or mailbox in Outlook for Mac</a></span></span>

- <span data-ttu-id="ab654-175"><a href="https://support.office.com/article/b0963400-2a51-4c64-afc7-b816d737d164.aspx" target="_blank">Ajouter des règles de boîte aux lettres partagée</a></span><span class="sxs-lookup"><span data-stu-id="ab654-175"><a href="https://support.office.com/article/b0963400-2a51-4c64-afc7-b816d737d164.aspx" target="_blank">Add rules to a shared mailbox</a></span></span>


## <a name="use-a-shared-mailbox-on-a-mobile-device-phone-or-tablet"></a><span data-ttu-id="ab654-176">Utiliser une boîte aux lettres partagée sur un appareil mobile (téléphone ou tablette)</span><span class="sxs-lookup"><span data-stu-id="ab654-176">Use a shared mailbox on a mobile device (phone or tablet)</span></span>

<span data-ttu-id="ab654-177">Vous pouvez accéder à une boîte aux lettres partagée sur un appareil mobile de deux manières :</span><span class="sxs-lookup"><span data-stu-id="ab654-177">You can access a shared mailbox on a mobile device in two ways:</span></span>
- <span data-ttu-id="ab654-178">Ajoutez la boîte aux lettres partagée dans l'<a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">application Outlook pour iOS</a> ou l'<a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">application mobile Outlook pour Android</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-178">Add the shared mailbox in the <a href="https://apps.apple.com/us/app/microsoft-outlook/id951937596" target="_blank">Outlook for iOS app</a> or the <a href="https://play.google.com/store/apps/details?id=com.microsoft.office.outlook&hl=en_US" target="_blank">Outlook for Android mobile app</a>.</span></span> 
    
    <span data-ttu-id="ab654-179">Pour les instructions, voir <a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook Mobile</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-179">For instructions, see <a href="https://support.office.com/article/f866242c-81b2-472e-8776-6c49c5473c9f" target="_blank">Add a shared mailbox to Outlook mobile</a>.</span></span>

- <span data-ttu-id="ab654-180">Ouvrez votre navigateur, connectez-vous à Office 365, puis accédez à Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="ab654-180">Open your browser, sign in to Office 365, and then go to Outlook on the web.</span></span> <span data-ttu-id="ab654-181">À partir d’Outlook sur le web, vous pouvez accéder à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-181">From Outlook on the web you'll be able to access the shared mailbox.</span></span>

    <span data-ttu-id="ab654-182">Pour les instructions, voir <a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Ajouter une boîte aux lettres partagée dans Outlook sur le web</a>.</span><span class="sxs-lookup"><span data-stu-id="ab654-182">For instructions, see <a href="https://support.office.com/article/98b5a90d-4e38-415d-a030-f09a4cd28207.aspx" target="_blank">Add a shared mailbox to Outlook on the web</a>.</span></span>

## <a name="use-the-shared-calendar"></a><span data-ttu-id="ab654-183">Utiliser le calendrier partagé</span><span class="sxs-lookup"><span data-stu-id="ab654-183">Use the shared calendar</span></span>

<span data-ttu-id="ab654-184">Lorsque vous avez créé la boîte aux lettres partagée, vous avez automatiquement créé un calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="ab654-184">When you created the shared mailbox, you automatically created a shared calendar.</span></span> <span data-ttu-id="ab654-185">Nous préférons le calendrier de la boîte aux lettres partagée plutôt qu’un calendrier SharePoint pour effectuer le suivi de rendez-vous et d’où se trouvent les personnes.</span><span class="sxs-lookup"><span data-stu-id="ab654-185">We like the shared mailbox calendar rather than a SharePoint calendar for keeping track of appointments and where people are.</span></span> <span data-ttu-id="ab654-186">Un calendrier partagé est intégré à Outlook et est beaucoup plus facile à utiliser qu'un calendrier SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ab654-186">A shared calendar is integrated with Outlook and it's much easier to use than a SharePoint calendar.</span></span>

1. <span data-ttu-id="ab654-187">Dans l'application Outlook, accédez à l'affichage Calendrier, puis sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ab654-187">In the Outlook app, go to calendar view, and select the shared mailbox.</span></span>

2. <span data-ttu-id="ab654-188">Lorsque vous entrez des rendez-vous, chaque membre de la boîte aux lettres partagée peut les voir.</span><span class="sxs-lookup"><span data-stu-id="ab654-188">When you enter appointments, everyone who is a member of the shared mailbox will be able to see them.</span></span>

3. <span data-ttu-id="ab654-189">N’importe quel membre de la boîte aux lettres partagée peut créer, afficher et gérer des rendez-vous dans le calendrier, tout comme ils le feraient leurs rendez-vous personnels.</span><span class="sxs-lookup"><span data-stu-id="ab654-189">Any member of the shared mailbox can create, view, and manage appointments on the calendar, just like they would their personal appointments.</span></span> <span data-ttu-id="ab654-190">Tous les membres de la boîte aux lettres partagée peuvent voir les modifications apportées au calendrier partagé.</span><span class="sxs-lookup"><span data-stu-id="ab654-190">Everyone who is a member of shared mailbox can see their changes to the shared calendar.</span></span>

## <a name="related-articles"></a><span data-ttu-id="ab654-191">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ab654-191">Related articles</span></span>

[<span data-ttu-id="ab654-192">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="ab654-192">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="ab654-193">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="ab654-193">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="ab654-194">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="ab654-194">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="ab654-195">Supprimer une licence à partir d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="ab654-195">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)

[<span data-ttu-id="ab654-196">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="ab654-196">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)





