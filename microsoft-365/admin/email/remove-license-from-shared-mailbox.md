---
title: Supprimer la licence de boîte aux lettres partagée
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
ms.custom:
- MSStore_Link
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: bb229ee9-e7be-4990-b3eb-354e75740496
description: 'Supprimez la licence d’une boîte aux lettres partagée pour l’affecter à un autre utilisateur. '
ms.openlocfilehash: 11d5185cc3f79899a737ddccc0a93160acb380bc
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698302"
---
# <a name="remove-a-license-from-a-shared-mailbox"></a><span data-ttu-id="dfb9b-103">Supprimer une licence d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dfb9b-103">Remove a license from a shared mailbox</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="dfb9b-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-104">The admin center is changing.</span></span> <span data-ttu-id="dfb9b-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="dfb9b-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="dfb9b-106">Les boîtes aux lettres partagées ne nécessitent généralement pas de licence.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-106">Shared mailboxes usually don't require a license.</span></span> <span data-ttu-id="dfb9b-107">Suivez ces instructions pour supprimer une licence d’une boîte aux lettres partagée afin de pouvoir l’attribuer à un utilisateur ou renvoyer la licence afin de ne pas payer pour une licence dont vous n’avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-107">Follow these instructions to remove a license from a shared mailbox so that you can either assign it to a user or return the license so that you aren't paying for a license you don't need.</span></span>

> [!NOTE]
> <span data-ttu-id="dfb9b-108">Une licence est requise dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="dfb9b-108">A license is required in the following scenarios:</span></span>
> 1. <span data-ttu-id="dfb9b-109">La boîte aux lettres partagée utilise plus de 50 Go de stockage.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-109">The shared mailbox has more than 50 GB of storage in use.</span></span>
> 2. <span data-ttu-id="dfb9b-110">La boîte aux lettres partagée utilise l’archivage sur place.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-110">The shared mailbox uses in-place archiving.</span></span>
> 3. <span data-ttu-id="dfb9b-111">La boîte aux lettres partagée est placée en attente pour litige.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-111">The shared mailbox is placed in litigation hold.</span></span>
> 4. <span data-ttu-id="dfb9b-112">Une licence Microsoft Defender est attribuée à la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-112">The shared mailbox has a Microsoft Defender license assigned.</span></span>

  
## <a name="remove-the-license"></a><span data-ttu-id="dfb9b-113">Supprimer la licence</span><span class="sxs-lookup"><span data-stu-id="dfb9b-113">Remove the license</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="dfb9b-114">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-114">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="dfb9b-115">Vous devez supprimer la licence de la page Utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-115">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="dfb9b-116">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée, car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-116">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span> 
  
2. <span data-ttu-id="dfb9b-117">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-117">Select the shared mailbox.</span></span>

3. <span data-ttu-id="dfb9b-118">Un des **onglets Licences et** applications, développez **Licences** et décochez la case pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-118">One the **Licenses and Apps** tab, expand **Licenses** and uncheck the box for the license you want to remove.</span></span>

4. <span data-ttu-id="dfb9b-119">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-119">Select **Save changes**.</span></span>

5. <span data-ttu-id="dfb9b-120">Lorsque vous revenirez à la page **Utilisateurs** actifs, l’état de la boîte aux lettres partagée sera **sans permis.**</span><span class="sxs-lookup"><span data-stu-id="dfb9b-120">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="dfb9b-121">Vous payez toujours pour la licence.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-121">You're still paying for the license.</span></span> <span data-ttu-id="dfb9b-122">Pour arrêter de payer, [supprimez la licence de votre abonnement.](../../commerce/licenses/remove-licenses-from-subscription.md)</span><span class="sxs-lookup"><span data-stu-id="dfb9b-122">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="dfb9b-123">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-123">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dfb9b-124">Vous devez supprimer la licence de la page Utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-124">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="dfb9b-125">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée, car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-125">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="dfb9b-126">Sélectionnez la boîte aux lettres partagée, puis **sélectionnez Modifier** en plus des **licences de produit.**</span><span class="sxs-lookup"><span data-stu-id="dfb9b-126">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="dfb9b-127">Dans la page **Licences de produits,** définissez le basculement sur **« Off** » pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-127">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="dfb9b-128">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-128">Select **Save**.</span></span>

5. <span data-ttu-id="dfb9b-129">Lorsque vous revenirez à la page **Utilisateurs** actifs, l’état de la boîte aux lettres partagée sera **sans permis.**</span><span class="sxs-lookup"><span data-stu-id="dfb9b-129">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="dfb9b-130">Vous payez toujours pour la licence.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-130">You're still paying for the license.</span></span> <span data-ttu-id="dfb9b-131">Pour arrêter de payer, [supprimez la licence de votre abonnement.](../../commerce/licenses/remove-licenses-from-subscription.md)</span><span class="sxs-lookup"><span data-stu-id="dfb9b-131">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="dfb9b-132">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-132">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dfb9b-133">Vous devez supprimer la licence de la page Utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-133">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="dfb9b-134">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée, car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-134">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="dfb9b-135">Sélectionnez la boîte aux lettres partagée, puis **sélectionnez Modifier** en plus des **licences de produit.**</span><span class="sxs-lookup"><span data-stu-id="dfb9b-135">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="dfb9b-136">Dans la page **Licences de produits,** définissez le basculement sur **« Off** » pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-136">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="dfb9b-137">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-137">Select **Save**.</span></span>

5. <span data-ttu-id="dfb9b-138">Lorsque vous revenirez à la page **Utilisateurs** actifs, l’état de la boîte aux lettres partagée sera **sans permis.**</span><span class="sxs-lookup"><span data-stu-id="dfb9b-138">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="dfb9b-139">Vous payez toujours pour la licence.</span><span class="sxs-lookup"><span data-stu-id="dfb9b-139">You're still paying for the license.</span></span> <span data-ttu-id="dfb9b-140">Pour arrêter de payer, [supprimez la licence de votre abonnement.](../../commerce/licenses/remove-licenses-from-subscription.md)</span><span class="sxs-lookup"><span data-stu-id="dfb9b-140">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end 

 

## <a name="related-articles"></a><span data-ttu-id="dfb9b-141">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="dfb9b-141">Related articles</span></span>

[<span data-ttu-id="dfb9b-142">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="dfb9b-142">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="dfb9b-143">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dfb9b-143">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="dfb9b-144">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dfb9b-144">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="dfb9b-145">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="dfb9b-145">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="dfb9b-146">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="dfb9b-146">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
