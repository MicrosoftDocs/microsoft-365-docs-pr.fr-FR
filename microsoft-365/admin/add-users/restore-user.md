---
title: Restaurer un utilisateur
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
- GEA150
ms.assetid: 2c261e42-5dd1-48b0-845f-2a016d29cfc1
description: Découvrez comment restaurer les comptes d’utilisateur supprimés et toutes les données associées.
ms.openlocfilehash: b7d98c1f49f8252ea9fdda2d863b5b77ac5bea9d
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52291066"
---
# <a name="restore-a-user"></a><span data-ttu-id="b3ebe-103">Restaurer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3ebe-103">Restore a user</span></span>
   
<span data-ttu-id="b3ebe-p101">Lorsque vous restaurez un compte d'utilisateur dans les 30 jours après sa suppression, celui-ci et toutes les données associées sont restaurés. L'utilisateur peut se connecter avec le même compte professionnel ou scolaire. Sa boîte aux lettres est entièrement restaurée. Pour déterminer le temps restant avant qu'un compte d'utilisateur spécifique ne puisse plus être restauré, [contactez-nous](../../business-video/get-help-support.md).</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p101">When you restore a user account within 30 days after deleting it, the account and all associated data are restored. The user can sign in with the same work or school account. Their mailbox will be fully restored. To find out how much time remains before a specific user account can no longer be restored, [contact us](../../business-video/get-help-support.md).</span></span>
  
<span data-ttu-id="b3ebe-108">Voici quelques conseils :</span><span class="sxs-lookup"><span data-stu-id="b3ebe-108">Here are a couple of tips:</span></span>
  
- <span data-ttu-id="b3ebe-109">Assurez-vous que les licences peuvent être assignées au compte.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-109">Make sure licenses are available to assign to the account.</span></span>
    
- <span data-ttu-id="b3ebe-110">Si votre entreprise utilise Active Directory, consultez [Comment résoudre les problèmes liés aux comptes d'utilisateurs supprimés dans Office 365](/office365/troubleshoot/active-directory/restore-deleted-user-accounts.md) pour obtenir des instructions sur la restauration d'un compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-110">If your business uses Active Directory, see [How to troubleshoot deleted user accounts in Office 365](/office365/troubleshoot/active-directory/restore-deleted-user-accounts.md) for instructions on restoring a user account.</span></span> 
    
## <a name="restore-one-or-more-user-accounts"></a><span data-ttu-id="b3ebe-111">Restaurer un ou plusieurs comptes d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3ebe-111">Restore one or more user accounts</span></span>

<span data-ttu-id="b3ebe-112">Vous devez être administrateur Microsoft 365 administrateur global ou administrateur de gestion des utilisateurs pour suivre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-112">You must be a Microsoft 365 global admin or user management admin to do these steps.</span></span> 

1. <span data-ttu-id="b3ebe-113">Dans le Centre d’administration, allez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">supprimés.</a></span><span class="sxs-lookup"><span data-stu-id="b3ebe-113">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">Deleted users</a> page.</span></span>

2. <span data-ttu-id="b3ebe-114">Dans la page **Utilisateurs** supprimés, sélectionnez les noms des utilisateurs que vous souhaitez restaurer, puis sélectionnez **Restaurer.**</span><span class="sxs-lookup"><span data-stu-id="b3ebe-114">On the **Deleted users** page, select the names of the users who you want to restore, and then select **Restore**.</span></span>
    
3. <span data-ttu-id="b3ebe-115">Suivez les invites pour définir leur mot de passe, puis sélectionnez **Restaurer**.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-115">Follow the prompts to set their password, and then select **Restore**.</span></span>
    
4. <span data-ttu-id="b3ebe-116">Si l’utilisateur est correctement restauré, sélectionnez **Envoyer un e-mail et fermez.**</span><span class="sxs-lookup"><span data-stu-id="b3ebe-116">If the user is successfully restored, select **Send email and close**.</span></span> <span data-ttu-id="b3ebe-117">Si vous rencontrez un conflit de noms ou d'adresses de proxy, consultez les instructions ci-dessous pour savoir comment restaurer ces comptes.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-117">If you encounter a name conflict or proxy address conflict, see the instructions below for how to restore those accounts.</span></span>
    
<span data-ttu-id="b3ebe-118">Une fois que vous avez restauré un utilisateur, assurez-vous de l’informer que son mot de passe a été modifié et de le suivre.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-118">After you've restored a user, make sure you notify them that their password changed and you follow up with them.</span></span>
  
## <a name="restore-a-user-that-has-a-user-name-conflict"></a><span data-ttu-id="b3ebe-119">Restaurer un utilisateur présentant un conflit de noms d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3ebe-119">Restore a user that has a user name conflict</span></span>

<span data-ttu-id="b3ebe-120">Un conflit de noms d'utilisateur survient lorsque vous supprimez un compte d'utilisateur, créez un nouveau avec le même nom (pour le même utilisateur ou un autre portant le même nom), puis tentez de restaurer le compte supprimé.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-120">A user name conflict occurs when you delete a user account, create a new user account with the same user name (either for the same user or another user with a similar name), and later try to restore the deleted account.</span></span>
  
<span data-ttu-id="b3ebe-p103">Pour résoudre ce problème, vous pouvez soit remplacer le compte d'utilisateur actif par celui que vous restaurez, soit attribuer un autre nom au compte restauré, afin que les deux comptes ne se servent plus du même nom d'utilisateur. Voici comment procéder.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p103">To fix this, replace the active user account with the one that you are restoring. Or, assign a different user name to the account that you are restoring so that there aren't two accounts with the same user name. Here are the steps.</span></span>

1. <span data-ttu-id="b3ebe-124">Dans le Centre d’administration, allez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">supprimés.</a></span><span class="sxs-lookup"><span data-stu-id="b3ebe-124">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">Deleted users</a> page.</span></span>
  
2. <span data-ttu-id="b3ebe-125">Dans la page **Utilisateurs** supprimés, sélectionnez les noms des utilisateurs à restaurer, puis sélectionnez **Restaurer.**</span><span class="sxs-lookup"><span data-stu-id="b3ebe-125">On the **Deleted users** page, select the names of the users that you want to restore, and then select **Restore**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b3ebe-p104">Lorsque la restauration de deux ou plusieurs utilisateurs échoue, un message d'erreur vous en avertit. Dans ce cas, consultez le journal pour identifier les utilisateurs qui n'ont pas été restaurés, puis procédez de nouveau à la restauration des comptes, un par un.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p104">If two or more users fail to be restored, an error message advises you that the restore operation failed for some users. View the log to see which users were not restored, and then restore the failed accounts one at a time.</span></span> 
  
3. <span data-ttu-id="b3ebe-128">Suivez les invites pour définir le mot de passe et sélectionnez **Restaurer.**</span><span class="sxs-lookup"><span data-stu-id="b3ebe-128">Follow the prompts to set the password and select **Restore**.</span></span>
    
4. <span data-ttu-id="b3ebe-p105">Un message indiquant qu'un problème s'est produit lors de la restauration du compte s'affiche. Effectuez l'une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p105">A message pops up that says there was a problem restoring the account. Do one of the following:</span></span>
    
  - <span data-ttu-id="b3ebe-p106">Annulez la restauration et renommez l'utilisateur actif. Essayez d'effectuer la restauration de nouveau.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p106">Cancel the restore and rename the current active user. Then attempt the restore again.</span></span>
    
  - <span data-ttu-id="b3ebe-133">OU, tapez une nouvelle adresse de messagerie principale pour l’utilisateur et sélectionnez **Restaurer**.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-133">OR, type a new primary email address for the user and select **Restore**.</span></span>
    
5. <span data-ttu-id="b3ebe-134">Examinez les résultats, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-134">Review the results, and then select **Close**.</span></span>
    
## <a name="restore-a-user-that-has-a-proxy-address-conflict"></a><span data-ttu-id="b3ebe-135">Restaurer un utilisateur présentant un conflit d’adresses de proxy</span><span class="sxs-lookup"><span data-stu-id="b3ebe-135">Restore a user that has a proxy address conflict</span></span>

<span data-ttu-id="b3ebe-p107">Un conflit d'adresses proxy survient lorsque vous supprimez un compte d'utilisateur contenant une adresse proxy, attribuez cette adresse à un autre compte, puis tentez de restaurer le compte supprimé. Suivez les étapes ci-dessous pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-p107">A proxy address conflict occurs when you delete a user account that contains a proxy address, assign the same proxy address to another account, and then try to restore the deleted account. Follow the steps below to fix this issue.</span></span>
  
<span data-ttu-id="b3ebe-138">Pour ce [faire,](about-admin-roles.md) vous devez Microsoft 365 administrateur.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-138">You must have [admin permissions](about-admin-roles.md) in Microsoft 365 to do this.</span></span> 

1. <span data-ttu-id="b3ebe-139">Dans le Centre d’administration, allez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">supprimés.</a></span><span class="sxs-lookup"><span data-stu-id="b3ebe-139">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2071581" target="_blank">Deleted users</a> page.</span></span>

2. <span data-ttu-id="b3ebe-140">Sur la page **Utilisateurs supprimés**, sélectionnez l'utilisateur à restaurer, puis **Restaurer**.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-140">On the **Deleted users** page, select the user that you want to restore, and then select **Restore**.</span></span> 
    
3. <span data-ttu-id="b3ebe-141">Dans la page **Restaurer,** suivez les instructions pour définir le mot de passe et sélectionnez **Restaurer.**</span><span class="sxs-lookup"><span data-stu-id="b3ebe-141">On the **Restore** page, follow the instructions to set the password and select **Restore**.</span></span> <span data-ttu-id="b3ebe-142">Toutes les adresses proxy en conflit sont supprimées automatiquement de l'utilisateur que vous restaurez.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-142">Any conflicting proxy addresses are automatically removed from the user you are restoring.</span></span>
    
4. <span data-ttu-id="b3ebe-143">Examinez les résultats, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b3ebe-143">Review the results, and then select **Close**.</span></span>

## <a name="related-articles"></a><span data-ttu-id="b3ebe-144">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b3ebe-144">Related articles</span></span>

[<span data-ttu-id="b3ebe-145">Supprimer un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b3ebe-145">Delete a user</span></span>](delete-a-user.md)
