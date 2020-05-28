---
title: Supprimer un utilisateur de votre organisation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
- SPO_Content
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: d5155593-3bac-4d8d-9d8b-f4513a81479e
description: Découvrez comment supprimer un compte d’utilisateur. Déterminez ce qu’il convient de faire avec le courrier électronique de l’utilisateur, le contenu OneDrive, et s’il faut conserver la licence de produit ou cesser de le payer.
ms.openlocfilehash: 4102fe4ac297a1f426b3bf575e748a72b323ebb6
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44387188"
---
# <a name="delete-a-user-from-your-organization"></a><span data-ttu-id="237c6-104">Supprimer un utilisateur de votre organisation</span><span class="sxs-lookup"><span data-stu-id="237c6-104">Delete a user from your organization</span></span>
  
||
|:-----|
|<span data-ttu-id="237c6-105">**Vous recherchez comment supprimer votre *propre* compte d’utilisateur Microsoft 365 que vous utilisez au travail ou à l’école ? Contactez le support technique de votre entreprise ou de votre Université pour effectuer ces étapes pour vous.**</span><span class="sxs-lookup"><span data-stu-id="237c6-105">**Looking for how to delete your *own* Microsoft 365 user account that you use at work or school? Contact the technical support at your work or university to do these steps for you.**</span></span>|
   
## <a name="what-you-need-to-know-about-deleting-users"></a><span data-ttu-id="237c6-106">Ce que vous devez savoir sur la suppression des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="237c6-106">What you need to know about deleting users</span></span>

- <span data-ttu-id="237c6-107">Seules les personnes disposant des autorisations d' [administrateur général Microsoft 365](about-admin-roles.md) ou de gestion des utilisateurs de l’entreprise ou de l’établissement scolaire peuvent supprimer des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-107">Only people who have [Microsoft 365 global admin](about-admin-roles.md) or User management permissions for the business or school can delete user accounts.</span></span> 
    
- <span data-ttu-id="237c6-108">Vous disposez de 30 jours pour [restaurer](restore-user.md) le compte avant que les données de l'utilisateur ne soient définitivement supprimées.</span><span class="sxs-lookup"><span data-stu-id="237c6-108">You have 30 days to [restore](restore-user.md) the account before the user's data is permanently deleted.</span></span> 
    
- <span data-ttu-id="237c6-p102">Si vous voulez conserver les données OneDrive de l'utilisateur, déplacez-le à un autre emplacement. Vous pouvez même effectuer cette opération 30 jours après la suppression du compte. Voir [Accéder aux données d'un ancien utilisateur et les sauvegarder](get-access-to-and-back-up-a-former-user-s-data.md). Vous ne devez pas déplacer ses fichiers SharePoint ; vous y aurez toujours accès.</span><span class="sxs-lookup"><span data-stu-id="237c6-p102">If you want to keep the user's OneDrive data, move it to a different location. You can even do this up to 30 days after deleting the account. See [Get access to and back up a former user's data](get-access-to-and-back-up-a-former-user-s-data.md). You don't need to move their SharePoint files; you'll still have access to them.</span></span>
    
- <span data-ttu-id="237c6-p103">Si vous souhaitez conserver les courriers de l'utilisateur, **AVANT** de supprimer le compte, déplacez les courriers vers un autre emplacement. Si vous avez déjà supprimé le compte depuis moins de 30 jours, vous pouvez le restaurer, déplacer les courriers, puis supprimer le compte. Voir [Accéder aux données d'un ancien utilisateur et les sauvegarder](get-access-to-and-back-up-a-former-user-s-data.md).</span><span class="sxs-lookup"><span data-stu-id="237c6-p103">If you want to keep the user's email, **BEFORE** you delete the account, move the email to a different location. If you've already deleted the account: if it's been less than 30 days you can restore it, then move the email data, then delete the account. See [Get access to and back up a former user's data](get-access-to-and-back-up-a-former-user-s-data.md).</span></span>
    
- <span data-ttu-id="237c6-116">Si vous disposez d’un abonnement Enterprise comme Office 365 entreprise E3, vous pouvez conserver les données de boîte aux lettres d’un compte d’utilisateur supprimé en le transformant en *boîte aux lettres inactive*.</span><span class="sxs-lookup"><span data-stu-id="237c6-116">If you have an Enterprise subscription like Office 365 Enterprise E3, you can preserve the mailbox data of a deleted user account by turning it into an *inactive mailbox*.</span></span> <span data-ttu-id="237c6-117">Pour en savoir plus, voir [Gestion des boîtes aux lettres inactives dans Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/inactive-mailboxes-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="237c6-117">To learn more, see [Manage inactive mailboxes in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/inactive-mailboxes-in-office-365).</span></span>


## <a name="global-admin-delete-a-user-stop-paying-for-their-license-and-choose-what-to-do-with-their-email-and-onedrive-content"></a><span data-ttu-id="237c6-118">Administrateur général : supprimez un utilisateur, arrêtez le paiement de sa licence, puis choisissez ce qu’il faut faire avec sa messagerie électronique et son contenu OneDrive</span><span class="sxs-lookup"><span data-stu-id="237c6-118">Global admin: Delete a user, stop paying for their license, and choose what to do with their email and OneDrive content</span></span>

<span data-ttu-id="237c6-119">Si vous êtes un administrateur général, lorsque vous supprimez un utilisateur, vous pouvez également accorder à un autre utilisateur l’accès à sa messagerie et choisir ce qu’il doit faire avec son contenu OneDrive.</span><span class="sxs-lookup"><span data-stu-id="237c6-119">If you are a global administrator, when you delete a user you can also give another user access to their email, and choose what to do with their OneDrive content.</span></span> 

  
### <a name="things-to-consider"></a><span data-ttu-id="237c6-120">Éléments à prendre en considération...</span><span class="sxs-lookup"><span data-stu-id="237c6-120">Things to consider...</span></span>

<span data-ttu-id="237c6-121">Avant de commencer, réfléchissez à ce que vous voulez faire avec le courrier électronique de l’utilisateur et le contenu OneDrive, et si vous souhaitez conserver la licence ou cesser de le payer.</span><span class="sxs-lookup"><span data-stu-id="237c6-121">Before you begin, think about what you want to do with the user's email and OneDrive content, and whether you want to keep the license or stop paying for it.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="237c6-122">Licences de produits</span><span class="sxs-lookup"><span data-stu-id="237c6-122">Product licenses</span></span>  <br/> |<span data-ttu-id="237c6-123">Vous pouvez supprimer la licence de l’utilisateur et la supprimer de vos abonnements pour arrêter le paiement de cette licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-123">You can remove the license from the user and remove it from your subscriptions to stop paying for that license.</span></span> <span data-ttu-id="237c6-124">Si vous sélectionnez cette option, la licence est automatiquement supprimée de vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="237c6-124">If you select this option, the license will be removed automatically from your subscriptions.</span></span>  <br/><br/> <span data-ttu-id="237c6-125">**Vous ne pouvez pas supprimer la licence** si vous l’avez achetée par le biais d’un partenaire ou d’une licence en volume.</span><span class="sxs-lookup"><span data-stu-id="237c6-125">**You can't remove the license** if you bought it through a Partner or volume licensing.</span></span> <span data-ttu-id="237c6-126">Si vous payez un forfait annuel ou si vous êtes au milieu d’un cycle de facturation, vous ne pourrez pas supprimer la licence de votre abonnement tant que votre engagement n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="237c6-126">If you are paying for an annual plan or if you are in the middle of a billing cycle, you won't be able to remove the license from your subscription until your commitment is completed.</span></span>  <br/> |
|<span data-ttu-id="237c6-127">Contenu OneDrive</span><span class="sxs-lookup"><span data-stu-id="237c6-127">OneDrive content</span></span>  <br/> |<span data-ttu-id="237c6-128">Si l’utilisateur a enregistré ses fichiers dans OneDrive, vous pouvez donner un accès à ces fichiers à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-128">If the user saved their files to OneDrive, you can give another user access to these files.</span></span>  <br/><br/> <span data-ttu-id="237c6-129">Vous devez déplacer les fichiers que vous souhaitez conserver pendant la période de rétention définie pour les fichiers OneDrive.</span><span class="sxs-lookup"><span data-stu-id="237c6-129">You'll need to move the files you want to keep within the retention period that is set for OneDrive files.</span></span> <span data-ttu-id="237c6-130">**Par défaut, la période de rétention est de 30 jours.**</span><span class="sxs-lookup"><span data-stu-id="237c6-130">**By default, the retention period is 30 days.**</span></span> <span data-ttu-id="237c6-131">Si vous ne déplacez pas les fichiers pendant la période de rétention après la suppression de l’utilisateur, le contenu OneDrive sera définitivement supprimé.</span><span class="sxs-lookup"><span data-stu-id="237c6-131">If you don't move the files within the retention period after deleting the user, the OneDrive content will be permanently deleted.</span></span> <span data-ttu-id="237c6-132">Pour augmenter le nombre de jours de conservation des fichiers OneDrive pour les comptes supprimés, consultez [la rubrique Set the onedrive Retention for Deleted Users](https://docs.microsoft.com/onedrive/set-retention).</span><span class="sxs-lookup"><span data-stu-id="237c6-132">To increase the number of days that you retain OneDrive files for deleted accounts, see [Set the OneDrive retention for deleted users](https://docs.microsoft.com/onedrive/set-retention).</span></span>  <br/><br/> <span data-ttu-id="237c6-133">**Indispensables!**</span><span class="sxs-lookup"><span data-stu-id="237c6-133">**Important!**</span></span> <span data-ttu-id="237c6-134">Si l’utilisateur supprimé a utilisé un ordinateur personnel pour télécharger des fichiers à partir de SharePoint et OneDrive, il n’existe aucun moyen d’effacer les fichiers qu’ils stockent sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-134">If the deleted user used a personal computer to download files from SharePoint and OneDrive, there's no way for you to wipe those files they stored on their computer.</span></span> <span data-ttu-id="237c6-135">Ils continueront à avoir accès à tous les fichiers qui ont été synchronisés à partir de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="237c6-135">They will continue to have access to any files that were synced from OneDrive.</span></span>           |
|<span data-ttu-id="237c6-136">E-mail</span><span class="sxs-lookup"><span data-stu-id="237c6-136">Email</span></span>  <br/> | <span data-ttu-id="237c6-137">Accorder à un autre utilisateur l’accès au courrier électronique de l’utilisateur supprimé convertira la boîte aux lettres de l’utilisateur supprimé en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="237c6-137">Giving another user access to the deleted user's email will convert the deleted user's mailbox to a shared mailbox.</span></span> <span data-ttu-id="237c6-138">Le nouveau propriétaire de la boîte aux lettres peut ensuite accéder à la boîte aux lettres et surveiller les nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="237c6-138">The new mailbox owner can then access the mailbox and monitor for new email.</span></span> <span data-ttu-id="237c6-139">Vous disposez également des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="237c6-139">You'll also have the following options:</span></span>  <br/>  <br/><span data-ttu-id="237c6-140">Modifier le nom d’affichage : nous vous recommandons de modifier le nom complet afin qu’il soit facile d’identifier la boîte aux lettres partagée dans la liste des utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="237c6-140">Change the display name - We recommend changing the display name so that it will be easy to identify the shared mailbox in the Active users list.</span></span>  <br/>  <span data-ttu-id="237c6-141">Activer les réponses automatiques : nous avons déjà écrit une réponse automatique poli pour vous.</span><span class="sxs-lookup"><span data-stu-id="237c6-141">Turn on automatic replies - We've already written a polite automatic reply for you.</span></span> <span data-ttu-id="237c6-142">Vous pouvez envoyer des réponses automatiques différentes à des personnes au sein de votre organisation et à des personnes externes à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="237c6-142">You can send a different automatic replies to people within your organization and people from outside your organization.</span></span>  <br/> <br/> <span data-ttu-id="237c6-143">Nettoyer les alias : les alias sont des adresses de messagerie supplémentaires pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="237c6-143">Clean up aliases - Aliases are additional email addresses for users.</span></span> <span data-ttu-id="237c6-144">Certaines organisations ne les utilisent pas, donc si vous n’avez pas besoin d’effectuer d’autres actions ici.</span><span class="sxs-lookup"><span data-stu-id="237c6-144">Some organizations don't use them, so if you don't have any you don't need to do anything else here.</span></span> <span data-ttu-id="237c6-145">Si l’utilisateur possède des alias, nous vous recommandons de les supprimer afin de pouvoir réutiliser ces adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="237c6-145">If the user does have aliases, we recommend removing them so that you can re-use those email addresses.</span></span> <span data-ttu-id="237c6-146">Dans le cas contraire, vous ne pouvez pas réutiliser ces adresses de messagerie jusqu’à ce que la période de rétention des boîtes aux lettres supprimées soit passée.</span><span class="sxs-lookup"><span data-stu-id="237c6-146">Otherwise, you can't re-use those email addresses until the retention period for deleted mailboxes has passed.</span></span> <span data-ttu-id="237c6-147">Par défaut, une boîte aux lettres supprimée est récupérable pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="237c6-147">By default, a deleted mailbox is recoverable for 30 days.</span></span> <span data-ttu-id="237c6-148">Pour plus d’informations, consultez la rubrique [supprimer ou restaurer des boîtes aux lettres utilisateur dans Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes#delete-a-user-mailbox).</span><span class="sxs-lookup"><span data-stu-id="237c6-148">For more information, see  [Delete or restore user mailboxes in Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes#delete-a-user-mailbox).</span></span> <br/> |
|<span data-ttu-id="237c6-149">Active Directory</span><span class="sxs-lookup"><span data-stu-id="237c6-149">Active Directory</span></span>  <br/> |<span data-ttu-id="237c6-150">Si votre entreprise utilise **Active Directory** qui se synchronise avec Azure Active Directory, vous devez supprimer le compte d'utilisateur d'Active Directory.</span><span class="sxs-lookup"><span data-stu-id="237c6-150">If your business uses **Active Directory** that is synchronizing with Azure AD, you need to delete the user account from Active Directory.</span></span> <span data-ttu-id="237c6-151">Vous ne pouvez pas le faire via Office 365.</span><span class="sxs-lookup"><span data-stu-id="237c6-151">You can't do it through Office 365.</span></span> <span data-ttu-id="237c6-152">Pour obtenir des instructions, consultez [la rubrique supprimer un compte d’utilisateur](https://go.microsoft.com/fwlink/p/?linkid=841808).</span><span class="sxs-lookup"><span data-stu-id="237c6-152">For instructions, see [Delete a User Account](https://go.microsoft.com/fwlink/p/?linkid=841808).</span></span>  <br/> |
   
### <a name="get-started"></a><span data-ttu-id="237c6-153">Prise en main</span><span class="sxs-lookup"><span data-stu-id="237c6-153">Get started</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="237c6-154">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="237c6-154">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

::: moniker-end

<span data-ttu-id="237c6-155">Étant donné que l’expérience guidée décrit les étapes de suppression d’un utilisateur, voici comment commencer.</span><span class="sxs-lookup"><span data-stu-id="237c6-155">Since the guided experience walks through the steps to delete a user, here's how to get started.</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="237c6-156">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-156">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="237c6-157">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-157">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="237c6-158">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-158">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

::: moniker-end

2. <span data-ttu-id="237c6-159">Sélectionnez l’utilisateur à supprimer, puis **Supprimer l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="237c6-159">Select the user you want to delete, and then select **Delete user**.</span></span>

## <a name="user-management-admin-delete-one-or-more-users-from-office-365"></a><span data-ttu-id="237c6-160">Administrateur de gestion des utilisateurs : supprimer un ou plusieurs utilisateurs d’Office 365</span><span class="sxs-lookup"><span data-stu-id="237c6-160">User management admin: Delete one or more users from Office 365</span></span>


> [!IMPORTANT]
> <span data-ttu-id="237c6-161">Ne supprimez pas le compte d’un utilisateur si vous l’avez [converti en boîte aux lettres partagée](../email/convert-user-mailbox-to-shared-mailbox.md) ou si vous avez configuré le transfert du courrier sur le compte.</span><span class="sxs-lookup"><span data-stu-id="237c6-161">Don't delete a user's account if you've [converted it to a shared mailbox](../email/convert-user-mailbox-to-shared-mailbox.md) or if you've set up email forwarding on the account.</span></span> <span data-ttu-id="237c6-162">Ces fonctions ont toujours besoin du compte.</span><span class="sxs-lookup"><span data-stu-id="237c6-162">Those functions still need the account.</span></span> <span data-ttu-id="237c6-163">Une boîte aux lettres partagée ne nécessite pas de licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-163">A shared mailbox doesn't require a license.</span></span> <span data-ttu-id="237c6-164">Si vous avez converti le compte en boîte aux lettres partagée, vous pouvez [arrêter le paiement de la licence](#stop-paying-for-the-license).</span><span class="sxs-lookup"><span data-stu-id="237c6-164">If you've converted the account to a shared mailbox you can [Stop paying for the license](#stop-paying-for-the-license).</span></span> <span data-ttu-id="237c6-165">Si vous avez configuré le transfert du courrier sur le compte, vous ne pouvez pas supprimer la licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-165">If you've set up email forwarding on the account, you can't remove the license.</span></span> <span data-ttu-id="237c6-166">Cette opération arrêtera le transfert du courrier et désactivera la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="237c6-166">Doing so will stop email forwarding and deactivate the mailbox.</span></span>
  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="237c6-167">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-167">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>  

2. <span data-ttu-id="237c6-168">Sélectionnez les noms des utilisateurs que vous souhaitez supprimer, sélectionnez **autres options** (**...**), puis **Supprimer l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="237c6-168">Select the names of the users that you want to delete, select **More options** (**...**), and then choose  **Delete user**.</span></span>

   <span data-ttu-id="237c6-169">Même si vous avez supprimé le compte de l’utilisateur, **vous payez toujours pour la licence**.</span><span class="sxs-lookup"><span data-stu-id="237c6-169">Although you deleted the user's account, **you're still paying for the license**.</span></span> <span data-ttu-id="237c6-170">Consultez la procédure suivante pour cesser de payer la licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-170">See the next procedure to stop paying for the license.</span></span>  <span data-ttu-id="237c6-171">Vous pouvez également attribuer la licence à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-171">Or, you can assign the license to another user.</span></span> <span data-ttu-id="237c6-172">Il ne sera pas attribué automatiquement à une personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-172">It won't be assigned to someone automatically.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="237c6-173">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-173">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="237c6-174">Sélectionnez les noms des utilisateurs que vous souhaitez supprimer, puis dans le volet **actions en bloc** , choisissez **supprimer des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="237c6-174">Select the names of the users that you want to delete, and in the **Bulk actions** pane, choose **Delete users**.</span></span>

   <span data-ttu-id="237c6-175">Même si vous avez supprimé le compte de l’utilisateur, **vous payez toujours pour la licence**.</span><span class="sxs-lookup"><span data-stu-id="237c6-175">Although you deleted the user's account, **you're still paying for the license**.</span></span> <span data-ttu-id="237c6-176">Consultez la procédure suivante pour cesser de payer la licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-176">See the next procedure to stop paying for the license.</span></span>  <span data-ttu-id="237c6-177">Vous pouvez également attribuer la licence à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-177">Or, you can assign the license to another user.</span></span> <span data-ttu-id="237c6-178">Il ne sera pas attribué automatiquement à une personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-178">It won't be assigned to someone automatically.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="237c6-179">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-179">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="237c6-180">Sélectionnez les noms des utilisateurs que vous souhaitez supprimer, puis dans le volet **actions en bloc** , choisissez **supprimer des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="237c6-180">Select the names of the users that you want to delete, and in the **Bulk actions** pane, choose **Delete users**.</span></span>

   <span data-ttu-id="237c6-181">Même si vous avez supprimé le compte de l’utilisateur, **vous payez toujours pour la licence**.</span><span class="sxs-lookup"><span data-stu-id="237c6-181">Although you deleted the user's account, **you're still paying for the license**.</span></span> <span data-ttu-id="237c6-182">Consultez la procédure suivante pour cesser de payer la licence.</span><span class="sxs-lookup"><span data-stu-id="237c6-182">See the next procedure to stop paying for the license.</span></span>  <span data-ttu-id="237c6-183">Vous pouvez également attribuer la licence à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="237c6-183">Or, you can assign the license to another user.</span></span> <span data-ttu-id="237c6-184">Il ne sera pas attribué automatiquement à une personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-184">It won't be assigned to someone automatically.</span></span>

::: moniker-end

### <a name="stop-paying-for-the-license"></a><span data-ttu-id="237c6-185">Arrêter de payer la licence</span><span class="sxs-lookup"><span data-stu-id="237c6-185">Stop paying for the license</span></span>

<span data-ttu-id="237c6-186">La réduction du nombre de licences est une étape distincte qui ne peut être effectuée que par l’administrateur général ou l’administrateur de facturation.</span><span class="sxs-lookup"><span data-stu-id="237c6-186">Reducing the number of licenses is a separate step that can only be performed by the global admin or billing admin.</span></span> 
  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="237c6-187">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-187">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span> <span data-ttu-id="237c6-188">Si vous ne voyez pas cette option, vous n’êtes pas un administrateur général ni un administrateur de facturation, et vous ne pouvez pas effectuer cette étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-188">If you don't see this option, you aren't a global admin or billing admin, and can't do this step.</span></span>

2. <span data-ttu-id="237c6-189">Sélectionnez l’abonnement (si vous en avez plusieurs), puis sélectionnez **Ajouter/supprimer des licences** pour supprimer la licence afin de ne pas en payer avant d’embaucher une autre personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-189">Select the subscription (if you have more than one) and then select **Add/Remove licenses** to delete the license so you don't pay for it until you hire another person.</span></span>  

   <span data-ttu-id="237c6-190">Plus tard, lorsque vous suivez les étapes pour ajouter une autre personne à votre entreprise, vous êtes invité à acheter une licence en même temps, en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-190">Later when you go through the steps to add another person to your business, you'll be prompted to buy a license at the same time, with just one step!</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="237c6-191">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-191">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span> <span data-ttu-id="237c6-192">Si vous ne voyez pas cette option, vous n’êtes pas un administrateur général ni un administrateur de facturation, et vous ne pouvez pas effectuer cette étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-192">If you don't see this option, you aren't a global admin or billing admin, and can't do this step.</span></span>

2. <span data-ttu-id="237c6-193">Sélectionnez l’abonnement (si vous en avez plusieurs), puis sélectionnez **Ajouter/supprimer des licences** pour supprimer la licence afin de ne pas en payer avant d’embaucher une autre personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-193">Select the subscription (if you have more than one) and then select **Add/Remove licenses** to delete the license so you don't pay for it until you hire another person.</span></span>  

   <span data-ttu-id="237c6-194">Plus tard, lorsque vous suivez les étapes pour ajouter une autre personne à votre entreprise, vous êtes invité à acheter une licence en même temps, en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-194">Later when you go through the steps to add another person to your business, you'll be prompted to buy a license at the same time, with just one step!</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="237c6-195">Dans le Centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="237c6-195">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Subscriptions</a> page.</span></span> <span data-ttu-id="237c6-196">Si vous ne voyez pas cette option, vous n’êtes pas un administrateur général ni un administrateur de facturation, et vous ne pouvez pas effectuer cette étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-196">If you don't see this option, you aren't a global admin or billing admin, and can't do this step.</span></span>

2. <span data-ttu-id="237c6-197">Sélectionnez l’abonnement (si vous en avez plusieurs), puis sélectionnez **Ajouter/supprimer des licences** pour supprimer la licence afin de ne pas en payer avant d’embaucher une autre personne.</span><span class="sxs-lookup"><span data-stu-id="237c6-197">Select the subscription (if you have more than one) and then select **Add/Remove licenses** to delete the license so you don't pay for it until you hire another person.</span></span>  

   <span data-ttu-id="237c6-198">Plus tard, lorsque vous suivez les étapes pour ajouter une autre personne à votre entreprise, vous êtes invité à acheter une licence en même temps, en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="237c6-198">Later when you go through the steps to add another person to your business, you'll be prompted to buy a license at the same time, with just one step!</span></span>

::: moniker-end 

## <a name="delete-many-users-at-the-same-time"></a><span data-ttu-id="237c6-199">Supprimer plusieurs utilisateurs en même temps</span><span class="sxs-lookup"><span data-stu-id="237c6-199">Delete many users at the same time</span></span>

<span data-ttu-id="237c6-200">Voir la cmdlet PowerShell [Remove-MsolUser](https://go.microsoft.com/fwlink/p/?linkid=842230) .</span><span class="sxs-lookup"><span data-stu-id="237c6-200">See the [Remove-MsolUser](https://go.microsoft.com/fwlink/p/?linkid=842230) PowerShell cmdlet.</span></span>

## <a name="fix-issues-with-deleting-a-user"></a><span data-ttu-id="237c6-201">Résoudre les problèmes de suppression d'un utilisateur</span><span class="sxs-lookup"><span data-stu-id="237c6-201">Fix issues with deleting a user</span></span>

<span data-ttu-id="237c6-202">Voici les problèmes les plus fréquemment rencontrés lors de la suppression d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="237c6-202">Here are the most common issues people encounter when deleting a user:</span></span>
  
- <span data-ttu-id="237c6-203">**Un message d'erreur du type « Nous ne pouvons pas supprimer l'utilisateur. Merci de réessayer plus tard. » apparaît.**</span><span class="sxs-lookup"><span data-stu-id="237c6-203">**You get an error message along the lines of "User cannot be deleted. Please try again later."**</span></span> <span data-ttu-id="237c6-204">Vérifiez si le transfert du courrier a été configuré sur le compte ou si le compte a été converti en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="237c6-204">Doublecheck whether the account has email forwarding set up on it, or it's been converted to a shared mailbox.</span></span> <span data-ttu-id="237c6-205">Ces deux situations peuvent être à l'origine de cette erreur.</span><span class="sxs-lookup"><span data-stu-id="237c6-205">Both of these will cause that error.</span></span> <span data-ttu-id="237c6-206">Ne supprimez pas le compte s’il a été transféré vers une boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="237c6-206">Don't delete the account if it has email forwarding or it's been converted to a shared mailbox.</span></span>

- <span data-ttu-id="237c6-207">**Vous n'avez pas les autorisations appropriées pour supprimer un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="237c6-207">**You don't have the appropriate permissions to delete a user**.</span></span> <span data-ttu-id="237c6-208">Seules les personnes qui sont des administrateurs [globaux Microsoft 365 ou des administrateurs de gestion](about-admin-roles.md) des utilisateurs peuvent supprimer des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="237c6-208">Only people who are [Microsoft 365 global admins or user management admins](about-admin-roles.md) can delete users.</span></span> <span data-ttu-id="237c6-209">Il s'agit généralement du support technique de votre établissement scolaire ou de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="237c6-209">Usually this is the technical support in your school or business.</span></span>

- <span data-ttu-id="237c6-p122">**Lorsque vous supprimez l'utilisateur, son nom apparaît toujours dans votre carnet d'adresses global**. Cela se produit lorsqu'une entreprise utilise Active Directory. Vous devez supprimer le compte utilisateur dans Active Directory. Pour obtenir des instructions, consultez l'article TechNet suivant : [Supprimer un compte utilisateur.](https://go.microsoft.com/fwlink/p/?linkid=841808)</span><span class="sxs-lookup"><span data-stu-id="237c6-p122">**You delete the user but their name continues appear in your global address book**. This happens when a business is using Active Directory. You have to delete the users account from Active Directory. For instructions, see this TechNet article: [Delete a User Account.](https://go.microsoft.com/fwlink/p/?linkid=841808)</span></span>

||
|:-----|
|<span data-ttu-id="237c6-214">**Voulez-vous supprimer Microsoft 365 de votre ordinateur ? Accédez à [annuler votre abonnement](../../commerce/subscriptions/cancel-your-subscription.md).**</span><span class="sxs-lookup"><span data-stu-id="237c6-214">**Do you want to delete Microsoft 365 from your computer? Go to [Cancel your subscription](../../commerce/subscriptions/cancel-your-subscription.md).**</span></span>|
   
## <a name="related-articles"></a><span data-ttu-id="237c6-215">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="237c6-215">Related articles</span></span>

[<span data-ttu-id="237c6-216">Restaurer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="237c6-216">Restore a user</span></span>](restore-user.md)
  
[<span data-ttu-id="237c6-217">Supprimer définitivement une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="237c6-217">Permanently delete a mailbox</span></span>](https://technet.microsoft.com/library/jj863440%28v=exchg.150%29.aspx)

[<span data-ttu-id="237c6-218">Supprimer un ancien employé d'Office 365</span><span class="sxs-lookup"><span data-stu-id="237c6-218">Remove a former employee from Office 365</span></span>](remove-former-employee.md)

[<span data-ttu-id="237c6-219">Ajouter un nouvel employé à Office 365</span><span class="sxs-lookup"><span data-stu-id="237c6-219">Add a new employee to Office 365</span></span>](add-new-employee.md)

<span data-ttu-id="237c6-220">[Supprimer un compte d’utilisateur](https://go.microsoft.com/fwlink/p/?linkid=841808): suivez ces instructions si votre entreprise utilise **Active Directory** qui se synchronise avec Azure ad.</span><span class="sxs-lookup"><span data-stu-id="237c6-220">[Delete a User Account](https://go.microsoft.com/fwlink/p/?linkid=841808): Use these instructions if your business uses **Active Directory** that is synchronizing with Azure AD.</span></span> <span data-ttu-id="237c6-221">Vous ne pouvez pas utiliser Office 365.</span><span class="sxs-lookup"><span data-stu-id="237c6-221">You can't do it through Office 365.</span></span>