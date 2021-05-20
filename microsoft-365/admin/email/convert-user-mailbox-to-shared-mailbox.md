---
title: Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
manager: scotv
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
description: 'Apprenez à convertir une boîte aux lettres privée en boîte aux lettres partagée accessible par plusieurs personnes et non par une seule personne. '
ms.openlocfilehash: 73e2bad40037e1343f4e08c07ca6b26df16b1a30
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52537618"
---
# <a name="convert-a-user-mailbox-to-a-shared-mailbox"></a><span data-ttu-id="ed525-103">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="ed525-103">Convert a user mailbox to a shared mailbox</span></span>

<span data-ttu-id="ed525-104">Lorsque vous convertissez la boîte aux lettres d’un utilisateur en boîte aux lettres partagée, l’ensemble du courrier électronique et du calendrier existants est conservé.</span><span class="sxs-lookup"><span data-stu-id="ed525-104">When you convert a user's mailbox to a shared mailbox, all of the existing email and calendar is retained.</span></span> <span data-ttu-id="ed525-105">Ce n’est que maintenant que dans une boîte aux lettres partagée que plusieurs personnes pourront y accéder au lieu d’une seule personne.</span><span class="sxs-lookup"><span data-stu-id="ed525-105">Only now it's in a shared mailbox where several people will be able to access it instead of one person.</span></span> <span data-ttu-id="ed525-106">À une date ultérieure, vous pouvez reconverti une boîte aux lettres partagée en boîte aux lettres utilisateur (privée).</span><span class="sxs-lookup"><span data-stu-id="ed525-106">At a later date, you can convert a shared mailbox back to a user (private) mailbox.</span></span>

<span data-ttu-id="ed525-107">**Voici quelques éléments essentiels que vous devez connaître :**</span><span class="sxs-lookup"><span data-stu-id="ed525-107">**Here are some really important things that you need to know:**</span></span>

- <span data-ttu-id="ed525-108">La boîte aux lettres utilisateur que vous convertissez a besoin d’une licence qui lui est attribuée avant de la convertir en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-108">The user mailbox you're converting needs a license assigned to it before you convert it to a shared mailbox.</span></span> <span data-ttu-id="ed525-109">Sinon, vous ne verrez pas l’option de conversion de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ed525-109">Otherwise, you won't see the option to convert the mailbox.</span></span> <span data-ttu-id="ed525-110">Si vous avez supprimé la licence, rajoutez-la afin de pouvoir convertir la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ed525-110">If you've removed the license, add it back so you can convert the mailbox.</span></span> <span data-ttu-id="ed525-111">Après avoir converti la boîte aux lettres en une boîte aux lettres partagée, vous pouvez supprimer la licence du compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-111">After converting the mailbox to a shared one, you can remove the license from the user's account.</span></span>

- <span data-ttu-id="ed525-112">Les boîtes aux lettres partagées peuvent avoir jusqu’à 50 Go de données sans licence qui leur est attribuée.</span><span class="sxs-lookup"><span data-stu-id="ed525-112">Shared mailboxes can have up to 50 GB of data without a license assigned to them.</span></span> <span data-ttu-id="ed525-113">Pour contenir davantage de données, vous avez besoin d’une licence qui lui est attribuée.</span><span class="sxs-lookup"><span data-stu-id="ed525-113">To hold more data than that, you need a license assigned to it.</span></span> <span data-ttu-id="ed525-114">Vous devrez peut-être supprimer un grand nombre de messages électroniques volumineux (par ex., ceux avec pièces jointes) de la boîte aux lettres partagée pour la réduire afin de pouvoir supprimer la licence.</span><span class="sxs-lookup"><span data-stu-id="ed525-114">You may need to delete a bunch of large emails (say, ones with attachments) from the shared mailbox to shrink it down so you can remove the license.</span></span>

- <span data-ttu-id="ed525-115">Ne supprimez pas le compte de l’ancien utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-115">Don't delete the old user's account.</span></span> <span data-ttu-id="ed525-116">Cette valeur est requise pour ancrer la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-116">That's required to anchor the shared mailbox.</span></span> <span data-ttu-id="ed525-117">Si vous avez déjà supprimé le compte d’utilisateur, voir Convertir la boîte aux lettres [d’un utilisateur supprimé.](#convert-the-mailbox-of-a-deleted-user)</span><span class="sxs-lookup"><span data-stu-id="ed525-117">If you've already deleted the user account, see [Convert the mailbox of a deleted user](#convert-the-mailbox-of-a-deleted-user).</span></span>

- <span data-ttu-id="ed525-118">Les règles sont intactes après la conversion de la boîte aux lettres en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-118">The rules are intact after the mailbox is converted to a shared mailbox.</span></span>

## <a name="use-the-exchange-admin-center-to-convert-a-mailbox"></a><span data-ttu-id="ed525-119">Utiliser le centre Exchange’administration pour convertir une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ed525-119">Use the Exchange admin center to convert a mailbox</span></span>
 
1. <span data-ttu-id="ed525-120">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="ed525-120">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>

2. <span data-ttu-id="ed525-121">Sélectionnez **Les boîtes aux lettres** de \> **destinataires.**</span><span class="sxs-lookup"><span data-stu-id="ed525-121">Select **Recipients** \> **Mailboxes**.</span></span>

3. <span data-ttu-id="ed525-122">Sélectionnez la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-122">Select the user mailbox.</span></span> <span data-ttu-id="ed525-123">Sous **Convertir en boîte aux lettres partagée,** sélectionnez **Convertir.**</span><span class="sxs-lookup"><span data-stu-id="ed525-123">Under **Convert to Shared Mailbox**, select **Convert**.</span></span>

4. <span data-ttu-id="ed525-124">Si la boîte aux lettres est plus petite que 50 Go, vous pouvez supprimer la licence de l’utilisateur [et](../manage/remove-licenses-from-users.md)arrêter de payer pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ed525-124">If the mailbox is smaller than 50 GB, you can remove the [license from the user](../manage/remove-licenses-from-users.md), and stop paying for it.</span></span> <span data-ttu-id="ed525-125">Ne supprimez pas le compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-125">Don't delete the user's account.</span></span> <span data-ttu-id="ed525-126">La boîte aux lettres partagée en a besoin comme ancre.</span><span class="sxs-lookup"><span data-stu-id="ed525-126">The shared mailbox needs it there as an anchor.</span></span> <span data-ttu-id="ed525-127">Si vous convertissez la boîte aux lettres d’un employé qui quitte votre organisation, vous devez prendre des mesures supplémentaires pour vous assurer qu’il ne peut plus se connecter.</span><span class="sxs-lookup"><span data-stu-id="ed525-127">If you are converting the mailbox of an employee that is leaving your organization, you should take additional steps to make sure that they cannot log in anymore.</span></span> <span data-ttu-id="ed525-128">Veuillez consulter [Supprimer un ancien employé de Microsoft 365](../add-users/remove-former-employee.md).</span><span class="sxs-lookup"><span data-stu-id="ed525-128">Please see [Remove a former employee from Microsoft 365](../add-users/remove-former-employee.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="ed525-129">Il n’est pas nécessaire de réinitialiser le mot de passe de l’utilisateur lors de la conversion de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ed525-129">It's not required to reset the user's password during mailbox conversion.</span></span> <span data-ttu-id="ed525-130">Toutefois, si le mot  de passe n’est pas réinitialisé, le nom d’utilisateur et le mot de passe d’origine continuent de fonctionner une fois la conversion de la boîte aux lettres terminée.</span><span class="sxs-lookup"><span data-stu-id="ed525-130">However, if the password is not reset, **the original username and password continue to work** after the mailbox conversion is finished.</span></span>

<span data-ttu-id="ed525-131">Pour tout ce que vous devez savoir [](about-shared-mailboxes.md) sur les boîtes aux lettres partagées, voir à propos des boîtes aux lettres partagées et [créer une boîte aux lettres partagée.](create-a-shared-mailbox.md)</span><span class="sxs-lookup"><span data-stu-id="ed525-131">For everything else you need to know about shared mailboxes, see [About shared mailboxes](about-shared-mailboxes.md) and [Create a shared mailbox](create-a-shared-mailbox.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ed525-132">Les boîtes aux lettres partagées ne nécessitent pas de licence distincte.</span><span class="sxs-lookup"><span data-stu-id="ed525-132">Shared mailboxes don’t require a separate license.</span></span> <span data-ttu-id="ed525-133">Toutefois, si vous souhaitez activer une boîte aux lettres d'archivage ou placer une conservation inaltérable ou une conservation pour litige sur une boîte aux lettres partagée, vous devez affecter une licence Exchange Online Plan 1 avec l'Archivage Exchange Online ou une licence Exchange Online Plan 2 à la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ed525-133">However, if you want to enable In-Place Archive or put an In-Place Hold or a Litigation Hold on a shared mailbox, you must assign an Exchange Online Plan 1 with Exchange Online Archiving or Exchange Online Plan 2 license to the mailbox.</span></span>


## <a name="convert-the-mailbox-of-a-deleted-user"></a><span data-ttu-id="ed525-134">Convertir la boîte aux lettres d’un utilisateur supprimé</span><span class="sxs-lookup"><span data-stu-id="ed525-134">Convert the mailbox of a deleted user</span></span>

<span data-ttu-id="ed525-135">Supposons que vous avez supprimé un compte d’utilisateur et que vous voulez maintenant convertir son ancienne boîte aux lettres en boîte aux lettres de partage.</span><span class="sxs-lookup"><span data-stu-id="ed525-135">Let's say you've deleted a user account and now you want to convert their old mailbox to a share mailbox.</span></span> <span data-ttu-id="ed525-136">Voici ce que vous devez faire :</span><span class="sxs-lookup"><span data-stu-id="ed525-136">Here's what you need to do:</span></span>

1. <span data-ttu-id="ed525-137">[Restituer le compte de l’utilisateur.](../add-users/restore-user.md)</span><span class="sxs-lookup"><span data-stu-id="ed525-137">[Restore the user's account](../add-users/restore-user.md).</span></span>

2. <span data-ttu-id="ed525-138">Assurez-vous qu Microsoft 365 licence est affectée.</span><span class="sxs-lookup"><span data-stu-id="ed525-138">Make sure a Microsoft 365 license is assigned to it.</span></span>

3. <span data-ttu-id="ed525-139">Réinitialisez le mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-139">Reset the user's password.</span></span>
    
4. <span data-ttu-id="ed525-140">Attendez 20 à 30 minutes que leur boîte aux lettres soit recréée.</span><span class="sxs-lookup"><span data-stu-id="ed525-140">Wait 20-30 minutes for their mailbox to be recreated.</span></span>
    
5. <span data-ttu-id="ed525-141">Suivez maintenant les instructions de cette page pour convertir leur boîte aux lettres en boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-141">Now follow the instructions on this page to convert their mailbox to a shared mailbox.</span></span>
    
6. <span data-ttu-id="ed525-142">Une fois cette chose effectuée, vous pouvez supprimer la licence de la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-142">After that's done, you can remove the license from the user's mailbox.</span></span> <span data-ttu-id="ed525-143">Ne supprimez pas l’ancienne boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ed525-143">Don't delete the user's old mailbox.</span></span> <span data-ttu-id="ed525-144">La boîte aux lettres partagée en a besoin comme ancre.</span><span class="sxs-lookup"><span data-stu-id="ed525-144">The shared mailbox needs it there as an anchor.</span></span>
    
7. <span data-ttu-id="ed525-145">Ajoutez des membres à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-145">Add members to the shared mailbox.</span></span>


## <a name="convert-a-shared-mailbox-back-to-a-users-private-mailbox"></a><span data-ttu-id="ed525-146">Reconvertissent une boîte aux lettres partagée en boîte aux lettres (privée) d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="ed525-146">Convert a shared mailbox back to a user's (private) mailbox</span></span>

1. <span data-ttu-id="ed525-147">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="ed525-147">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>
   
2. <span data-ttu-id="ed525-148">Sélectionnez **Destinataires** \> **partagés.**</span><span class="sxs-lookup"><span data-stu-id="ed525-148">Select **Recipients** \> **Shared**.</span></span>

3. <span data-ttu-id="ed525-149">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-149">Select the shared mailbox.</span></span> <span data-ttu-id="ed525-150">Sous **Convertir en boîte aux lettres normale,** sélectionnez **Convertir.**</span><span class="sxs-lookup"><span data-stu-id="ed525-150">Under **Convert to Regular Mailbox**, select **Convert**.</span></span>

4. <span data-ttu-id="ed525-151">Revenir au Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="ed525-151">Go back to the admin center.</span></span> <span data-ttu-id="ed525-152">Sous **Utilisateurs,** choisissez le compte d’utilisateur associé à l’ancienne boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-152">Under **Users**, choose the user account associated with the old shared mailbox.</span></span> <span data-ttu-id="ed525-153">Attribuez une licence au compte et réinitialisez le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ed525-153">Assign a license to the account, and reset the password.</span></span>

   <span data-ttu-id="ed525-154">La mise en place de la boîte aux lettres prendra quelques minutes, mais après cela, la personne qui utilisera ce compte est prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="ed525-154">It will take a few minutes for the mailbox to get set up, but after that, the person who is going to use that account is ready to go.</span></span> <span data-ttu-id="ed525-155">Lorsqu’ils se connectent, ils voient les éléments de courrier électronique et de calendrier qui se trouveraient dans la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="ed525-155">When they sign in, they'll see the email and calendar items that used to be in the shared mailbox.</span></span>

## <a name="convert-a-users-mailbox-in-a-hybrid-environment"></a><span data-ttu-id="ed525-156">Convertir la boîte aux lettres d’un utilisateur dans un environnement hybride</span><span class="sxs-lookup"><span data-stu-id="ed525-156">Convert a user's mailbox in a hybrid environment</span></span>

<span data-ttu-id="ed525-157">Pour plus d’informations sur la conversion d’une boîte aux lettres utilisateur en boîte aux lettres partagée dans un environnement Exchange hybride, voir :</span><span class="sxs-lookup"><span data-stu-id="ed525-157">For more info about converting a user mailbox to a shared mailbox in an Exchange Hybrid environment, see:</span></span>

 - [<span data-ttu-id="ed525-158">Cmdlets pour créer ou modifier une boîte aux lettres partagée à distance dans un environnement Exchange local</span><span class="sxs-lookup"><span data-stu-id="ed525-158">Cmdlets to create or modify a remote shared mailbox in an on-premises Exchange environment</span></span>](https://support.microsoft.com/office/cmdlets-to-create-or-modify-a-remote-shared-mailbox-in-an-on-premises-exchange-environment-9e83fb59-c001-729c-a4c0-b2964c154b49)
 - [<span data-ttu-id="ed525-159">Les boîtes aux lettres partagées sont converties de manière inattendue en boîtes aux lettres utilisateur après l’installation de la synchronisation d’annuaires dans Exchange déploiement hybride</span><span class="sxs-lookup"><span data-stu-id="ed525-159">Shared mailboxes are unexpectedly converted to user mailboxes after directory synchronization runs in an Exchange hybrid deployment</span></span>](/exchange/troubleshoot/user-and-shared-mailboxes/shared-mailboxes-unexpectedly-converted-to-user-mailboxes)
 

> [!NOTE]
> <span data-ttu-id="ed525-160">Si vous êtes membre du groupe de rôles Gestion de l’organisation ou Gestion des destinataires, vous pouvez utiliser l’Exchange Management Shell pour modifier une boîte aux lettres utilisateur en boîte aux lettres partagée en local.</span><span class="sxs-lookup"><span data-stu-id="ed525-160">If you are a member of the Organization Management or Recipient Management role group, you can use the Exchange Management Shell to change a user mailbox to a shared mailbox on-premises.</span></span> <span data-ttu-id="ed525-161">Par exemple : `Set-Mailbox -Identity mailbox1@contoso.com -Type Shared`.</span><span class="sxs-lookup"><span data-stu-id="ed525-161">For example, `Set-Mailbox -Identity mailbox1@contoso.com -Type Shared`.</span></span>

## <a name="related-content"></a><span data-ttu-id="ed525-162">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="ed525-162">Related content</span></span>

<span data-ttu-id="ed525-163">[À propos des boîtes aux lettres partagées](about-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ed525-163">[About shared mailboxes](about-shared-mailboxes.md) (article)</span></span>

<span data-ttu-id="ed525-164">[Créer une boîte aux lettres partagée](create-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ed525-164">[Create a shared mailbox](create-a-shared-mailbox.md) (article)</span></span>

<span data-ttu-id="ed525-165">[Configurer une boîte aux lettres partagée](configure-a-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ed525-165">[Configure a shared mailbox](configure-a-shared-mailbox.md) (article)</span></span>

<span data-ttu-id="ed525-166">[Supprimer une licence d’une boîte aux lettres partagée](remove-license-from-shared-mailbox.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ed525-166">[Remove a license from a shared mailbox](remove-license-from-shared-mailbox.md) (article)</span></span>

<span data-ttu-id="ed525-167">[Résoudre les problèmes de boîtes aux lettres partagées](resolve-issues-with-shared-mailboxes.md) (article)</span><span class="sxs-lookup"><span data-stu-id="ed525-167">[Resolve issues with shared mailboxes](resolve-issues-with-shared-mailboxes.md) (article)</span></span>