---
title: Activer des boîtes aux lettres d’archivage dans le Centre de sécurité et conformité
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
ms.custom: seo-marvel-apr2020
description: Découvrez comment utiliser le Centre de conformité pour activer des boîtes aux lettres d’archivage afin de vous conformer aux exigences de votre organisation en matière de rétention, d’eDiscovery et de conservation des messages.
ms.openlocfilehash: d7506b92cc16120f1d40a6d5a1744ab38d446a76
ms.sourcegitcommit: a62ac3c01ba700a51b78a647e2301f27ac437c5a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "50233814"
---
# <a name="enable-archive-mailboxes-in-the-compliance-center"></a><span data-ttu-id="49167-103">Activer des boîtes aux lettres d’archivage dans le Centre conformité</span><span class="sxs-lookup"><span data-stu-id="49167-103">Enable archive mailboxes in the compliance center</span></span>

<span data-ttu-id="49167-104">L’archivage dans Microsoft 365 (également appelé *Archivage inaltérable*) fournit aux utilisateurs de l’espace de stockage de boîtes aux lettres supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="49167-104">Archiving in Microsoft 365 (also called *In-Place Archiving*) provides users with additional mailbox storage space.</span></span> <span data-ttu-id="49167-105">Une fois que vous avez activé les boîtes aux lettres d’archivage, les utilisateurs peuvent consulter et stocker des messages dans leurs boîtes aux lettres d’archivage à l’aide de Microsoft Outlook et d’Outlook sur le web (autrefois appelé Outlook Web App).</span><span class="sxs-lookup"><span data-stu-id="49167-105">After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App).</span></span> <span data-ttu-id="49167-106">Les utilisateurs peuvent également déplacer ou copier des messages entre leurs boîtes aux lettres principale et d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-106">Users can also move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="49167-107">Ils peuvent également récupérer les éléments supprimés du dossier Éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil Récupérer les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="49167-107">They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span>

> [!NOTE]
> <span data-ttu-id="49167-108">La fonctionnalité d’archivage à extension automatique fournit, dans Microsoft 365, un espace de stockage complémentaire dans les boîtes aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-108">The auto-expanding archiving feature in Microsoft 365 provides additional storage in archive mailboxes.</span></span> <span data-ttu-id="49167-109">Lorsque l’archivage à développement automatique est activé et que le quota de stockage initial de la boîte aux lettres d’archivage d’un utilisateur est atteint, Microsoft 365 ajoute automatiquement un espace de stockage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="49167-109">When auto-expanding  archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Microsoft 365 automatically adds additional storage space.</span></span> <span data-ttu-id="49167-110">Cela signifie que les utilisateurs ne tombent pas à cours d’espace de stockage de boîte aux lettres et que vous n’avez plus besoin de gérer quoi que ce soit après l’activation initiale de la boîte aux lettres d’archivage et de l’archivage à développement automatique pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="49167-110">This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization.</span></span> <span data-ttu-id="49167-111">Pour plus d’informations, voir [Vue d’ensemble d’un archivage illimité](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="49167-111">For more information, see [Overview of unlimited archiving](unlimited-archiving.md).</span></span>

## <a name="get-the-necessary-permissions"></a><span data-ttu-id="49167-112">Obtenir les autorisations nécessaires</span><span class="sxs-lookup"><span data-stu-id="49167-112">Get the necessary permissions</span></span>

<span data-ttu-id="49167-113">Pour activer ou désactiver les boîtes aux lettres d’archivage, vous devez être affecté au rôle Destinataires du courrier dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="49167-113">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes.</span></span> <span data-ttu-id="49167-114">Par défaut, ce rôle est attribué aux groupes de rôles Gestion des destinataires et Gestion de l’organisation sur la page **Autorisations** du Centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="49167-114">By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="49167-115">Si la page **Archive** n’apparaît pas dans le Centre de sécurité et conformité, demandez à votre administrateur de vous attribuer les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="49167-115">If you don't see the **Archive** page in the Security & Compliance Center, ask your administrator to assign you the necessary permissions.</span></span>

## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="49167-116">Activer une boîte aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="49167-116">Enable an archive mailbox</span></span>

1. <span data-ttu-id="49167-117">Accédez à <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="49167-117">Go to <https://protection.office.com>.</span></span>

2. <span data-ttu-id="49167-118">Connectez-vous à l’aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="49167-118">Sign in using your work or school account.</span></span>

3. <span data-ttu-id="49167-119">Dans le volet gauche du Centre de sécurité et conformité, cliquez sur **Gouvernance des données** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="49167-119">In the left pane of the Security & Compliance Center, click **Information governance** \> **Archive**.</span></span>

   <span data-ttu-id="49167-p104">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49167-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span>

   > [!NOTE]
   > <span data-ttu-id="49167-122">La page **Archive** affiche au maximum 500 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="49167-122">The **Archive** page shows a maximum of 500 users.</span></span>

4. <span data-ttu-id="49167-123">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-123">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>

   ![Cliquer sur Activer dans le volet d’informations de l’utilisateur sélectionné pour activer la boîte aux lettres d’archivage](../media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)

5. <span data-ttu-id="49167-125">Dans le volet d’informations de l’utilisateur sélectionné, cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="49167-125">In the details pane for the selected user, click **Enable**.</span></span>

   <span data-ttu-id="49167-126">Un avertissement s’affiche, qui vous signale que, si vous activez la boîte aux lettres d’archivage, les éléments de la boîte aux lettres de l’utilisateur plus anciens que la stratégie d’archivage affectée à la boîte aux lettres seront déplacés vers la nouvelle boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-126">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox.</span></span> <span data-ttu-id="49167-127">La stratégie d’archivage par défaut qui fait partie de la stratégie de rétention affectée aux boîtes aux lettres Online déplace les éléments vers la boîte aux lettres d’archivage deux ans après la date à laquelle ils ont été remis à la boîte aux lettres ou créés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49167-127">The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user.</span></span> <span data-ttu-id="49167-128">Pour plus d’informations, voir la section **Plus d’informations** de cet article.</span><span class="sxs-lookup"><span data-stu-id="49167-128">For more information, see the **More info** section in this article.</span></span>

6. <span data-ttu-id="49167-129">Cliquez sur **Oui** pour activer la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-129">Click **Yes** to enable the archive mailbox.</span></span>

   <span data-ttu-id="49167-130">La création de la boîte aux lettres d’archivage peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="49167-130">It might take a few moments to create the archive mailbox.</span></span> <span data-ttu-id="49167-131">Une fois la boîte aux lettres d’archivage créée, l’indication **Boîte aux lettres d’archivage : Activée** s’affiche dans le volet d’informations pour l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="49167-131">When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="49167-132">Il sera peut-être nécessaire de cliquer sur **Actualiser** ![icône Actualiser](../media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="49167-132">You might have to click **Refresh** ![Refresh icon](../media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span>

> [!TIP]
> <span data-ttu-id="49167-p107">Vous pouvez également activer des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont désactivées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Activer** dans le volet des détails.</span><span class="sxs-lookup"><span data-stu-id="49167-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span>

## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="49167-135">Désactiver une boîte aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="49167-135">Disable an archive mailbox</span></span>

<span data-ttu-id="49167-136">Vous pouvez également utiliser la page **Archive** dans le Centre de sécurité et conformité pour désactiver la boîte aux lettres d’archivage d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49167-136">You can also use the **Archive** page in the Security & Compliance Center to disable a user's archive mailbox.</span></span> <span data-ttu-id="49167-137">Si vous désactivez la boîte aux lettres d’un utilisateur, vous pouvez la reconnecter à la boîte aux lettres principale de l’utilisateur dans les 30 jours qui suivent sa désactivation.</span><span class="sxs-lookup"><span data-stu-id="49167-137">After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it.</span></span> <span data-ttu-id="49167-138">Dans ce cas, le contenu d’origine de la boîte aux lettres d’archivage est restauré.</span><span class="sxs-lookup"><span data-stu-id="49167-138">In this case, the original contents of the archive mailbox are restored.</span></span> <span data-ttu-id="49167-139">Au bout de 30 jours, le contenu de la boîte aux lettres d’archivage d’origine est supprimé définitivement et ne peut pas être récupéré.</span><span class="sxs-lookup"><span data-stu-id="49167-139">After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered.</span></span> <span data-ttu-id="49167-140">Par conséquent, si vous réactivez l’archive plus de 30 jours après l’avoir désactivée, une nouvelle boîte aux lettres d’archivage est créée.</span><span class="sxs-lookup"><span data-stu-id="49167-140">So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span>

<span data-ttu-id="49167-141">La stratégie d’archivage par défaut affectée aux boîtes aux lettres des utilisateurs déplace les éléments vers la boîte aux lettres d’archivage deux ans après leur date de remise.</span><span class="sxs-lookup"><span data-stu-id="49167-141">The default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered.</span></span> <span data-ttu-id="49167-142">Si vous désactivez la boîte aux lettres d’archivage d’un utilisateur, aucune action n’est effectuée sur les éléments de boîte aux lettres et ceux-ci restent dans la boîte aux lettres principale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49167-142">If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>

<span data-ttu-id="49167-143">Pour désactiver une boîte aux lettres d’archivage :</span><span class="sxs-lookup"><span data-stu-id="49167-143">To disable an archive mailbox:</span></span>

1. <span data-ttu-id="49167-144">Accédez à <https://protection.office.com>.</span><span class="sxs-lookup"><span data-stu-id="49167-144">Go to <https://protection.office.com>.</span></span>

2. <span data-ttu-id="49167-145">Connectez-vous à l’aide de votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="49167-145">Sign in using your work or school account.</span></span>

3. <span data-ttu-id="49167-146">Dans le volet gauche du Centre de sécurité et conformité, cliquez sur **Gouvernance des données** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="49167-146">In the left pane of the Security & Compliance Center, click **Information governance** \> **Archive**.</span></span>

   <span data-ttu-id="49167-p110">La page **Archive** s’affiche. La colonne **Boîte aux lettres d’archivage** indique si une boîte aux lettres d’archivage est activée ou désactivée pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49167-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span>

   > [!NOTE]
   > <span data-ttu-id="49167-149">La page **Archive** affiche au maximum 500 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="49167-149">The **Archive** page shows a maximum of 500 users.</span></span>

4. <span data-ttu-id="49167-150">Dans la liste des boîtes aux lettres, sélectionnez l’utilisateur pour lequel vous voulez désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-150">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>

5. <span data-ttu-id="49167-151">Dans le volet des détails, cliquez sur **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="49167-151">In the details pane, click **Disable**.</span></span>

   <span data-ttu-id="49167-152">Un message d’avertissement s’affiche, indiquant que vous avez 30 jours pour réactiver la boîte aux lettres d’archivage et qu’à l’issue de ce délai, toutes les informations contenues dans l’archive seront définitivement supprimées.</span><span class="sxs-lookup"><span data-stu-id="49167-152">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span>

6. <span data-ttu-id="49167-153">Cliquez sur **Oui** pour désactiver la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-153">Click **Yes** to disable the archive mailbox.</span></span>

   <span data-ttu-id="49167-154">La désactivation de la boîte aux lettres d’archivage peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="49167-154">It might take a few moments to disable the archive mailbox.</span></span> <span data-ttu-id="49167-155">Une fois la boîte aux lettres d’archivage désactivée, l’indication **Boîte aux lettres d’archivage : Désactivée** s’affiche dans le volet d’informations pour l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="49167-155">When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="49167-156">Il sera peut-être nécessaire de cliquer sur **Actualiser** ![icône Actualiser](../media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations dans le volet d’informations.</span><span class="sxs-lookup"><span data-stu-id="49167-156">You might have to click **Refresh** ![Refresh icon](../media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span>

> [!TIP]
> <span data-ttu-id="49167-p112">Vous pouvez également désactiver des boîtes aux lettres d’archivage en bloc en sélectionnant plusieurs utilisateurs dont les boîtes aux lettres sont activées (à l’aide de la touche Maj ou Ctrl). Une fois les boîtes aux lettres sélectionnées, cliquez sur **Désactiver** dans le volet des détails.</span><span class="sxs-lookup"><span data-stu-id="49167-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span>

## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="49167-159">Utiliser Exchange Online PowerShell pour activer ou désactiver les boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="49167-159">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="49167-160">Vous pouvez également utiliser Exchange Online PowerShell pour activer les boîtes aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-160">You can also use Exchange Online PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="49167-161">La principale raison d’utiliser PowerShell est que vous pouvez activer rapidement la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="49167-161">The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="49167-162">La première étape consiste à se connecter à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="49167-162">The first step is to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="49167-163">Pour obtenir des instructions, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="49167-163">For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="49167-164">Une fois que vous êtes connecté à Exchange Online, vous pouvez exécuter les commandes décrites dans les sections suivantes pour activer ou désactiver les boîtes aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-164">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="49167-165">Activer les boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="49167-165">Enable archive mailboxes</span></span>

<span data-ttu-id="49167-166">Pour activer la boîte aux lettres d’archivage pour un seul utilisateur, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="49167-166">Run the following command to enable the archive mailbox for a single user.</span></span>

```powershell
Enable-Mailbox -Identity <username> -Archive
```

<span data-ttu-id="49167-167">Pour activer la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation (dont la boîte aux lettres d’archivage n’est pas activée), exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="49167-167">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>

```powershell
Get-Mailbox -Filter {ArchiveGuid -Eq "00000000-0000-0000-0000-000000000000" -AND RecipientTypeDetails -Eq "UserMailbox"} | Enable-Mailbox -Archive
```

### <a name="disable-archive-mailboxes"></a><span data-ttu-id="49167-168">Désactiver les boîtes aux lettres d’archivage</span><span class="sxs-lookup"><span data-stu-id="49167-168">Disable archive mailboxes</span></span>

<span data-ttu-id="49167-169">Pour désactiver la boîte aux lettres d’archivage pour un seul utilisateur, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="49167-169">Run the following command to disable the archive mailbox for a single user.</span></span>

```powershell
Disable-Mailbox -Identity <username> -Archive
```

<span data-ttu-id="49167-170">Pour désactiver la boîte aux lettres d’archivage pour tous les utilisateurs au sein de votre organisation (dont la boîte aux lettres d’archivage est activée), exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="49167-170">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>

```powershell
Get-Mailbox -Filter {ArchiveGuid -Ne "00000000-0000-0000-0000-000000000000" -AND RecipientTypeDetails -Eq "UserMailbox"} | Disable-Mailbox -Archive
```

## <a name="more-information"></a><span data-ttu-id="49167-171">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="49167-171">More information</span></span>

- <span data-ttu-id="49167-172">Quand une boîte aux lettres d’archivage est activé, les utilisateurs peuvent y stocker des messages.</span><span class="sxs-lookup"><span data-stu-id="49167-172">When an archive mailbox is enabled, users can store messages in their archive mailbox.</span></span> <span data-ttu-id="49167-173">Les utilisateurs peuvent accéder à leur boîte aux lettres d’archivage à l’aide de Microsoft Outlook et d’Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="49167-173">Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web.</span></span> <span data-ttu-id="49167-174">À l’aide de l’une de ces applications clientes, les utilisateurs peuvent afficher les messages dans leur boîte aux lettres d’archivage et déplacer ou copier des messages entre leur boîte aux lettres principale et la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-174">Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="49167-175">Les utilisateurs peuvent également récupérer les éléments supprimés du dossier Éléments récupérables dans leur boîte aux lettres d’archivage à l’aide de l’outil de récupération des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="49167-175">Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span>

  <span data-ttu-id="49167-176">Pour obtenir la liste des licences Outlook qui prennent en charge l’archivage inaltérable, voir [Conditions de licence Outlook requises pour les fonctionnalités Exchange](https://support.microsoft.com/office/46b6b7c5-c3ca-43e5-8424-1e2807917c99).</span><span class="sxs-lookup"><span data-stu-id="49167-176">For a list of Outlook licenses that support In-Place Archiving, see [Outlook license requirements for Exchange features](https://support.microsoft.com/office/46b6b7c5-c3ca-43e5-8424-1e2807917c99).</span></span>

- <span data-ttu-id="49167-177">Les boîtes aux lettres d’archivage vous aident à répondre aux exigences de rétention, d’eDiscovery et de conservation des messages de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="49167-177">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements.</span></span> <span data-ttu-id="49167-178">Par exemple, vous pouvez utiliser la stratégie de rétention Exchange de votre organisation pour déplacer le contenu de boîtes aux lettres vers la boîte aux lettres d’archivage des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="49167-178">For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox.</span></span> <span data-ttu-id="49167-179">Lorsque vous utilisez l’outil Recherche de contenu dans le Centre de sécurité et conformité pour effectuer rechercher un contenu spécifique dans la boîte aux lettres d’un utilisateur, la boîte aux lettres d’archivage de celui-ci est également incluse dans le processus.</span><span class="sxs-lookup"><span data-stu-id="49167-179">When you use the Content Search tool in the Security & Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched.</span></span> <span data-ttu-id="49167-180">Lorsque vous définissez une Conservation pour litige ou appliquez une stratégie de rétention à la boîte aux lettres d’un utilisateur, les éléments contenus dans la boîte aux lettres d’archivage sont également conservés.</span><span class="sxs-lookup"><span data-stu-id="49167-180">And, when you place a Litigation Hold or apply a retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>

- <span data-ttu-id="49167-181">Lorsque les boîtes aux lettres d’archivage sont activées, votre organisation peut tirer parti de la stratégie de rétention par défaut Exchange (également appelée stratégie de Gestion des enregistrements de messagerie ou MRM) automatiquement affectée à chaque boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="49167-181">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox.</span></span> <span data-ttu-id="49167-182">Quand une boîte aux lettres d’archivage est activée, la stratégie de rétention par défaut Exchange effectue automatiquement les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="49167-182">When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span>

  - <span data-ttu-id="49167-183">Elle déplace les éléments datant de deux ans ou plus de la boîte aux lettres principale d’un utilisateur à sa boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-183">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span>

  - <span data-ttu-id="49167-184">Elle déplace les éléments datant de 14 jours ou plus du dossier Éléments récupérables dans la boîte aux lettres principale de l’utilisateur vers le dossier Éléments récupérables dans la boîte aux lettres d’archivage.</span><span class="sxs-lookup"><span data-stu-id="49167-184">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>

- <span data-ttu-id="49167-185">Pour plus d’informations sur les boîtes aux lettres d’archivage et les stratégies de rétention Exchange, voir:</span><span class="sxs-lookup"><span data-stu-id="49167-185">For more information about archive mailboxes and Exchange retention policies, see:</span></span>

  - [<span data-ttu-id="49167-186">Balises et stratégies de rétention dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="49167-186">Retention tags and retention policies in Exchange Online</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/messaging-records-management/retention-tags-and-policies)

  - [<span data-ttu-id="49167-187">Stratégie de rétention par défaut dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="49167-187">Default Retention Policy in Exchange Online</span></span>](https://docs.microsoft.com/exchange/security-and-compliance/messaging-records-management/default-retention-policy)

  - [<span data-ttu-id="49167-188">Configurer une stratégie d’archivage et de suppression pour les boîtes aux lettres de votre organisation</span><span class="sxs-lookup"><span data-stu-id="49167-188">Set up an archive and deletion policy for mailboxes in your organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
