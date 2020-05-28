---
title: Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée
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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 2e122487-e1f5-4f26-ba41-5689249d93ba
description: 'Découvrez comment convertir une boîte aux lettres privée en boîte aux lettres partagée accessible par plusieurs utilisateurs. '
ms.openlocfilehash: c4f71f12b430e239f5ea5791ba5b98a3109452b0
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44400111"
---
# <a name="convert-a-user-mailbox-to-a-shared-mailbox"></a><span data-ttu-id="6d4ea-103">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="6d4ea-103">Convert a user mailbox to a shared mailbox</span></span>

<span data-ttu-id="6d4ea-104">Lorsque vous convertissez la boîte aux lettres d’un utilisateur en boîte aux lettres partagée, tout le courrier et le calendrier existants sont conservés.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-104">When you convert a user's mailbox to a shared mailbox, all of the existing email and calendar is retained.</span></span> <span data-ttu-id="6d4ea-105">Il se trouve maintenant uniquement dans une boîte aux lettres partagée où plusieurs personnes peuvent y accéder au lieu d’une personne.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-105">Only now it's in a shared mailbox where several people will be able to access it instead of one person.</span></span> <span data-ttu-id="6d4ea-106">À une date ultérieure, vous pouvez reconvertir une boîte aux lettres partagée en boîte aux lettres utilisateur (privée).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-106">At a later date, you can convert a shared mailbox back to a user (private) mailbox.</span></span>

<span data-ttu-id="6d4ea-107">**Voici quelques éléments vraiment importants que vous devez savoir :**</span><span class="sxs-lookup"><span data-stu-id="6d4ea-107">**Here are some really important things that you need to know:**</span></span>

- <span data-ttu-id="6d4ea-108">La boîte aux lettres utilisateur que vous convertissez nécessite une licence qui lui est attribuée avant de la convertir en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-108">The user mailbox you're converting needs a license assigned to it before you convert it to a shared mailbox.</span></span> <span data-ttu-id="6d4ea-109">Dans le cas contraire, vous ne verrez pas l’option permettant de convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-109">Otherwise, you won't see the option to convert the mailbox.</span></span> <span data-ttu-id="6d4ea-110">Si vous avez supprimé la licence, rajoutez-la afin de pouvoir convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-110">If you've removed the license, add it back so you can convert the mailbox.</span></span> <span data-ttu-id="6d4ea-111">Après avoir converti la boîte aux lettres en une boîte aux lettres partagée, vous pouvez supprimer la licence du compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-111">After converting the mailbox to a shared one, you can remove the license from the user's account.</span></span>

- <span data-ttu-id="6d4ea-112">Les boîtes aux lettres partagées peuvent avoir jusqu’à 50 Go de données sans qu’une licence lui soit attribuée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-112">Shared mailboxes can have up to 50GB of data without a license assigned to them.</span></span> <span data-ttu-id="6d4ea-113">Pour conserver plus de données que cela, vous devez disposer d’une licence.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-113">To hold more data than that, you need a license assigned to it.</span></span> <span data-ttu-id="6d4ea-114">Il se peut que vous deviez supprimer un lot de messages volumineux (par exemple, ceux contenant des pièces jointes) de la boîte aux lettres partagée afin de le réduire afin de pouvoir supprimer la licence.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-114">You may need to delete a bunch of large emails (say, ones with attachments) from the shared mailbox to shrink it down so you can remove the license.</span></span>

- <span data-ttu-id="6d4ea-115">Ne supprimez pas le compte de l’ancien utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-115">Don't delete the old user's account.</span></span> <span data-ttu-id="6d4ea-116">Cela est nécessaire pour ancrer la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-116">That's required to anchor the shared mailbox.</span></span> <span data-ttu-id="6d4ea-117">Si vous avez déjà supprimé le compte d’utilisateur, reportez-vous à [la rubrique Conversion de la boîte aux lettres d’un utilisateur supprimé](#convert-the-mailbox-of-a-deleted-user).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-117">If you've already deleted the user account, see [Convert the mailbox of a deleted user](#convert-the-mailbox-of-a-deleted-user).</span></span>

- <span data-ttu-id="6d4ea-118">Les règles sont intactes une fois que la boîte aux lettres est convertie en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-118">The rules are intact after the mailbox is converted to a shared mailbox.</span></span>

## <a name="use-the-exchange-admin-center-to-convert-a-mailbox"></a><span data-ttu-id="6d4ea-119">Utiliser le centre d’administration Exchange pour convertir une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="6d4ea-119">Use the Exchange admin center to convert a mailbox</span></span>
 
1. <span data-ttu-id="6d4ea-120">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-120">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="6d4ea-121">Sélectionnez **Recipients** \> **boîtes aux lettres**de destinataires.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-121">Select **Recipients** \> **Mailboxes**.</span></span>

3. <span data-ttu-id="6d4ea-122">Sélectionnez la boîte aux lettres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-122">Select the user mailbox.</span></span> <span data-ttu-id="6d4ea-123">Sous **convertir en boîte aux lettres partagée**, sélectionnez **convertir**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-123">Under **Convert to Shared Mailbox**, select **Convert**.</span></span>

4. <span data-ttu-id="6d4ea-124">Si la taille de la boîte aux lettres est inférieure à 50 Go, vous pouvez supprimer la [licence de l’utilisateur](../manage/remove-licenses-from-users.md)et cesser de le payer.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-124">If the mailbox is smaller than 50GB, you can remove the [license from the user](../manage/remove-licenses-from-users.md), and stop paying for it.</span></span> <span data-ttu-id="6d4ea-125">Ne supprimez pas le compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-125">Don't delete the user's account.</span></span> <span data-ttu-id="6d4ea-126">La boîte aux lettres partagée en a besoin en tant qu’ancre.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-126">The shared mailbox needs it there as an anchor.</span></span> <span data-ttu-id="6d4ea-127">Si vous convertissez la boîte aux lettres d’un employé qui quitte votre organisation, vous devez prendre des mesures supplémentaires pour vous assurer qu’il ne peut plus se connecter.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-127">If you are converting the mailbox of an employee that is leaving your organization, you should take additional steps to make sure that they cannot log in anymore.</span></span> <span data-ttu-id="6d4ea-128">Consultez [la rubrique supprimer un ancien employé de Microsoft 365](../add-users/remove-former-employee.md).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-128">Please see [Remove a former employee from Microsoft 365](../add-users/remove-former-employee.md).</span></span>
    
5. <span data-ttu-id="6d4ea-129">Pour tout ce que vous devez savoir sur les boîtes aux lettres partagées, consultez la rubrique [à propos des boîtes aux lettres partagées](about-shared-mailboxes.md) et [créez une boîte aux lettres partagée](create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-129">For everything else you need to know about shared mailboxes, see [About shared mailboxes](about-shared-mailboxes.md) and [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>

## <a name="use-the-microsoft-365-admin-center-to-convert-a-mailbox"></a><span data-ttu-id="6d4ea-130">Utiliser le centre d’administration Microsoft 365 pour convertir une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="6d4ea-130">Use the Microsoft 365 admin center to convert a mailbox</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="6d4ea-131">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-131">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="6d4ea-132">Sélectionnez le nom de l’utilisateur dont vous souhaitez convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-132">Select the name of the user whose mailbox you want to convert.</span></span>

3. <span data-ttu-id="6d4ea-133">Réinitialisez le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-133">Reset the user's password.</span></span>

> [!NOTE]
> <span data-ttu-id="6d4ea-134">Il n’est pas nécessaire de réinitialiser le mot de passe de l’utilisateur pendant la conversion de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-134">It's not required to reset the user's password during mailbox conversion.</span></span> <span data-ttu-id="6d4ea-135">Toutefois, si le mot de passe n’est pas réinitialisé, **le nom d’utilisateur et le mot de passe d’origine continuent de fonctionner** une fois la conversion de boîte aux lettres terminée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-135">However, if the password is not reset, **the original username and password continue to work** after the mailbox conversion is finished.</span></span>

4. <span data-ttu-id="6d4ea-136">Dans l’onglet **messagerie** , sous **autres actions**, sélectionnez **convertir en boîte aux lettres partagée**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-136">On the **Mail** tab, under **More actions**, select **Convert to shared mailbox**.</span></span> 

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="6d4ea-137">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-137">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="6d4ea-138">Sélectionnez l’utilisateur dont vous souhaitez convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-138">Select the user whose mailbox you want to convert.</span></span>

3. <span data-ttu-id="6d4ea-139">Dans le volet droit, développez **paramètres de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-139">In the right pane, expand **Mail Settings**.</span></span> <span data-ttu-id="6d4ea-140">En regard de **paramètres supplémentaires**, sélectionnez **convertir en boîte aux lettres partagée**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-140">Next to **More settings**, select **Convert to shared mailbox**.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="6d4ea-141">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-141">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

2. <span data-ttu-id="6d4ea-142">Sélectionnez l’utilisateur dont vous souhaitez convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-142">Select the user whose mailbox you want to convert.</span></span>

3. <span data-ttu-id="6d4ea-143">Dans le volet droit, développez **paramètres de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-143">In the right pane, expand **Mail Settings**.</span></span> <span data-ttu-id="6d4ea-144">En regard de **paramètres supplémentaires**, sélectionnez **convertir en boîte aux lettres partagée**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-144">Next to **More settings**, select **Convert to shared mailbox**.</span></span>

::: moniker-end


<span data-ttu-id="6d4ea-145">Si la taille de la boîte aux lettres est inférieure à 50 Go, vous pouvez [Supprimer la licence de l’utilisateur](../manage/remove-licenses-from-users.md)et cesser de le payer.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-145">If the mailbox is smaller than 50GB, you can [remove the license from the user](../manage/remove-licenses-from-users.md), and stop paying for it.</span></span> <span data-ttu-id="6d4ea-146">Ne supprimez pas l’ancienne boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-146">Don't delete the user's old mailbox.</span></span> <span data-ttu-id="6d4ea-147">La boîte aux lettres partagée en a besoin en tant qu’ancre.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-147">The shared mailbox needs it there as an anchor.</span></span> <span data-ttu-id="6d4ea-148">Si vous convertissez la boîte aux lettres d’un employé qui quitte votre organisation, vous devez prendre des mesures supplémentaires pour vous assurer qu’il ne peut plus se connecter.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-148">If you are converting the mailbox of an employee that is leaving your organization, you should take additional steps to make sure that they cannot log in anymore.</span></span> <span data-ttu-id="6d4ea-149">Consultez [la rubrique supprimer un ancien employé de Microsoft 365](../add-users/remove-former-employee.md).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-149">See [Remove a former employee from Microsoft 365](../add-users/remove-former-employee.md).</span></span>
    
<span data-ttu-id="6d4ea-150">Pour tout ce que vous devez savoir sur les boîtes aux lettres partagées, consultez la rubrique [à propos des boîtes aux lettres partagées](about-shared-mailboxes.md) et [créez une boîte aux lettres partagée](create-a-shared-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-150">For everything else you need to know about shared mailboxes, see [About shared mailboxes](about-shared-mailboxes.md) and [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>


## <a name="convert-the-mailbox-of-a-deleted-user"></a><span data-ttu-id="6d4ea-151">Convertir la boîte aux lettres d’un utilisateur supprimé</span><span class="sxs-lookup"><span data-stu-id="6d4ea-151">Convert the mailbox of a deleted user</span></span>

<span data-ttu-id="6d4ea-152">Imaginons que vous ayez supprimé un compte d’utilisateur et que vous vouliez convertir son ancienne boîte aux lettres en boîte aux lettres de partage.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-152">Let's say you've deleted a user account and now you want to convert their old mailbox to a share mailbox.</span></span> <span data-ttu-id="6d4ea-153">Voici ce que vous devez faire :</span><span class="sxs-lookup"><span data-stu-id="6d4ea-153">Here's what you need to do:</span></span>

1. <span data-ttu-id="6d4ea-154">[Restaurez le compte de l’utilisateur](../add-users/restore-user.md).</span><span class="sxs-lookup"><span data-stu-id="6d4ea-154">[Restore the user's account](../add-users/restore-user.md).</span></span>

2. <span data-ttu-id="6d4ea-155">Assurez-vous qu’une licence Microsoft 365 lui est affectée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-155">Make sure a Microsoft 365 license is assigned to it.</span></span>

3. <span data-ttu-id="6d4ea-156">Réinitialisez le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-156">Reset the user's password.</span></span>
    
4. <span data-ttu-id="6d4ea-157">Patientez 20-30 minutes avant que la boîte aux lettres ne soit recréée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-157">Wait 20-30 minutes for their mailbox to be recreated.</span></span>
    
5. <span data-ttu-id="6d4ea-158">Suivez maintenant les instructions de cette page pour convertir leur boîte aux lettres en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-158">Now follow the instructions on this page to convert their mailbox to a shared mailbox.</span></span>
    
6. <span data-ttu-id="6d4ea-159">Une fois cette opération terminée, vous pouvez supprimer la licence de la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-159">After that's done, you can remove the license from the user's mailbox.</span></span> <span data-ttu-id="6d4ea-160">Ne supprimez pas l’ancienne boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-160">Don't delete the user's old mailbox.</span></span> <span data-ttu-id="6d4ea-161">La boîte aux lettres partagée en a besoin en tant qu’ancre.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-161">The shared mailbox needs it there as an anchor.</span></span>
    
7. <span data-ttu-id="6d4ea-162">Ajoutez des membres à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-162">Add members to the shared mailbox.</span></span>

## <a name="convert-a-shared-mailbox-back-to-a-users-private-mailbox"></a><span data-ttu-id="6d4ea-163">Convertir une boîte aux lettres partagée en boîte aux lettres (privée) d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="6d4ea-163">Convert a shared mailbox back to a user's (private) mailbox</span></span>

1. <span data-ttu-id="6d4ea-164">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-164">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>
   
2. <span data-ttu-id="6d4ea-165">Sélectionnez **destinataires** \> **partagés**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-165">Select **Recipients** \> **Shared**.</span></span>

3. <span data-ttu-id="6d4ea-166">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-166">Select the shared mailbox.</span></span> <span data-ttu-id="6d4ea-167">Sous **convertir en boîte aux lettres normale**, sélectionnez **convertir**.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-167">Under **Convert to Regular Mailbox**, select **Convert**.</span></span>

4. <span data-ttu-id="6d4ea-168">Revenez au centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-168">Go back to the admin center.</span></span> <span data-ttu-id="6d4ea-169">Sous **utilisateurs**, sélectionnez le compte d’utilisateur associé à l’ancienne boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-169">Under **Users**, choose the user account associated with the old shared mailbox.</span></span> <span data-ttu-id="6d4ea-170">Attribuer une licence au compte et réinitialiser le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-170">Assign a license to the account, and reset the password.</span></span>

   <span data-ttu-id="6d4ea-171">La configuration de la boîte aux lettres peut prendre quelques minutes, mais cette fois-ci, la personne qui va utiliser ce compte est prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-171">It will take a few minutes for the mailbox to get set up, but after that, the person who is going to use that account is ready to go.</span></span> <span data-ttu-id="6d4ea-172">Lorsqu’ils se connectent, ils voient les éléments de courrier et de calendrier utilisés comme étant dans la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-172">When they sign in, they'll see the email and calendar items that used to be in the shared mailbox.</span></span>

## <a name="convert-a-users-mailbox-in-a-hybrid-environment"></a><span data-ttu-id="6d4ea-173">Convertir la boîte aux lettres d’un utilisateur dans un environnement hybride</span><span class="sxs-lookup"><span data-stu-id="6d4ea-173">Convert a user's mailbox in a hybrid environment</span></span>

<span data-ttu-id="6d4ea-174">Si cette boîte aux lettres partagée se trouve dans un environnement hybride, nous **vous recommandons vivement** (presque nécessaire !) de déplacer la boîte aux lettres utilisateur vers l’organisation locale, de convertir la boîte aux lettres d’utilisateur en boîte aux lettres partagée, puis de replacer la boîte aux lettres partagée dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-174">If this shared mailbox is in a hybrid environment, we **strongly recommend** (almost require!) that you move the user mailbox back to on-premises, convert the user mailbox to a shared mailbox, and then move the shared mailbox back to the cloud.</span></span>

<span data-ttu-id="6d4ea-175">Voici pourquoi : Si vous convertissez la boîte aux lettres dans le Cloud, elle peut être convertie, mais en local, la boîte aux lettres est toujours la boîte aux lettres de l’utilisateur, car la nouvelle réalité n’est pas synchronisée en local.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-175">Here's why: if you convert the mailbox in the cloud, it can get converted, but on-premises still thinks the mailbox is the user mailbox, because the new reality does not sync back to on-premises.</span></span>

<span data-ttu-id="6d4ea-176">En règle générale, il ne s’agit pas d’un problème, mais il existe des scénarios dans lesquels les attributs locaux (ce qui signifie que la boîte aux lettres est la boîte aux lettres de l’utilisateur) peuvent remplacer les nouvelles versions Cloud de ces attributs et, par conséquent, la boîte aux lettres peut être reconvertie.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-176">Usually this is not a problem, but there are some scenarios where the on-premises attributes (which think that the mailbox is the user mailbox) can overwrite the new cloud versions of those attributes, and as a result, the mailbox might convert back.</span></span> <span data-ttu-id="6d4ea-177">Il s’agit d’un problème car les boîtes aux lettres des utilisateurs nécessitent **des licences ou sont supprimées de manière récupérable au bout de 30 jours**!</span><span class="sxs-lookup"><span data-stu-id="6d4ea-177">This is a problem because user mailboxes require licenses **or they are soft deleted after 30 days**!</span></span>

<span data-ttu-id="6d4ea-178">Nous avons résolu la plupart des raisons de ce problème, mais cela peut toujours se produire, bien que rarement.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-178">We've addressed most of the reasons why this happens but it still CAN happen, although infrequently.</span></span> <span data-ttu-id="6d4ea-179">Il est préférable d’être sûr et de déplacer la boîte aux lettres vers l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-179">It's best to be safe and move the mailbox back to on-premises.</span></span>

> [!NOTE]
> <span data-ttu-id="6d4ea-180">Si vous faites partie de la gestion de l’organisation ou de la gestion des destinataires, vous pouvez utiliser l’environnement de commande Exchange Management Shell pour modifier une boîte aux lettres utilisateur en une boîte aux lettres partagée locale.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-180">If you are a part of Organization Management or Recipient Management, you can use the  Exchange Management shell to change a user mailbox to a shared mailbox on-premises.</span></span> <span data-ttu-id="6d4ea-181">Par exemple, `Set-Mailbox -Identity mailbox1@contoso.onmicrosoft.com -Type Shared`.</span><span class="sxs-lookup"><span data-stu-id="6d4ea-181">For example, `Set-Mailbox -Identity mailbox1@contoso.onmicrosoft.com -Type Shared`.</span></span>

> [!TIP]
> <span data-ttu-id="6d4ea-182">Consultez la solution de contournement dans cette solution de support pour les instances lorsque [les boîtes aux lettres partagées sont converties de manière inattendue en boîtes aux lettres utilisateur](https://support.microsoft.com/help/2710029/shared-mailboxes-are-unexpectedly-converted-to-user-mailboxes-after-di)</span><span class="sxs-lookup"><span data-stu-id="6d4ea-182">See the workaround in this support solution for instances when [shared mailboxes are unexpectedly converted to user mailboxes](https://support.microsoft.com/help/2710029/shared-mailboxes-are-unexpectedly-converted-to-user-mailboxes-after-di)</span></span>
  
## <a name="related-articles"></a><span data-ttu-id="6d4ea-183">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6d4ea-183">Related articles</span></span>

[<span data-ttu-id="6d4ea-184">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="6d4ea-184">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="6d4ea-185">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="6d4ea-185">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="6d4ea-186">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="6d4ea-186">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="6d4ea-187">Supprimer une licence à partir d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="6d4ea-187">Remove a license from a shared mailbox</span></span>](remove-license-from-shared-mailbox.md)

[<span data-ttu-id="6d4ea-188">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="6d4ea-188">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
