---
title: Supprimer la licence de boîte aux lettres partagée
f1.keywords:
- NOCSH
ms.author: pebaum
author: pebaum
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
description: 'Supprimer une licence d’une boîte aux lettres partagée pour l’affecter à un autre utilisateur. '
ms.openlocfilehash: 401b334efeccf6d7c4caca20be3cc9767b2df945
ms.sourcegitcommit: a005395165db8896f4109674443b5e5e9209861d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2020
ms.locfileid: "44432218"
---
# <a name="remove-a-license-from-a-shared-mailbox"></a><span data-ttu-id="0227a-103">Supprimer une licence d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="0227a-103">Remove a license from a shared mailbox</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="0227a-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="0227a-104">The admin center is changing.</span></span> <span data-ttu-id="0227a-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="0227a-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="0227a-106">En règle générale, les boîtes aux lettres partagées ne nécessitent pas de licence.</span><span class="sxs-lookup"><span data-stu-id="0227a-106">Shared mailboxes usually don't require a license.</span></span> <span data-ttu-id="0227a-107">Suivez ces instructions pour supprimer une licence d’une boîte aux lettres partagée afin de pouvoir l’attribuer à un utilisateur ou renvoyer la licence afin de ne pas payer une licence dont vous n’avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="0227a-107">Follow these instructions to remove a license from a shared mailbox so that you can either assign it to a user or return the license so that you aren't paying for a license you don't need.</span></span>

> [!NOTE]
> <span data-ttu-id="0227a-108">Une licence est requise dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="0227a-108">A license is required in the following scenarios:</span></span>
> 1. <span data-ttu-id="0227a-109">La boîte aux lettres partagée dispose de plus de 50 Go d’espace de stockage.</span><span class="sxs-lookup"><span data-stu-id="0227a-109">The shared mailbox has more than 50 GB of storage in use.</span></span>
> 2. <span data-ttu-id="0227a-110">La boîte aux lettres partagée utilise l’archivage inaltérable.</span><span class="sxs-lookup"><span data-stu-id="0227a-110">The shared mailbox uses in-place archiving.</span></span>
> 3. <span data-ttu-id="0227a-111">La boîte aux lettres partagée est placée en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="0227a-111">The shared mailbox is placed in litigation hold.</span></span>

  
## <a name="remove-the-license"></a><span data-ttu-id="0227a-112">Supprimer la licence</span><span class="sxs-lookup"><span data-stu-id="0227a-112">Remove the license</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="0227a-113">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0227a-113">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0227a-114">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="0227a-114">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="0227a-115">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0227a-115">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span> 
  
2. <span data-ttu-id="0227a-116">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="0227a-116">Select the shared mailbox.</span></span>

3. <span data-ttu-id="0227a-117">Dans l’onglet **licences et applications** , développez **licences** et désactivez la case à cocher correspondant à la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="0227a-117">One the **Licenses and Apps** tab, expand **Licenses** and uncheck the box for the license you want to remove.</span></span>

4. <span data-ttu-id="0227a-118">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="0227a-118">Select **Save changes**.</span></span>

5. <span data-ttu-id="0227a-119">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="0227a-119">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="0227a-120">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="0227a-120">You're still paying for the license.</span></span> <span data-ttu-id="0227a-121">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="0227a-121">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="0227a-122">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0227a-122">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0227a-123">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="0227a-123">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="0227a-124">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0227a-124">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="0227a-125">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="0227a-125">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="0227a-126">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="0227a-126">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="0227a-127">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0227a-127">Select **Save**.</span></span>

5. <span data-ttu-id="0227a-128">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="0227a-128">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="0227a-129">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="0227a-129">You're still paying for the license.</span></span> <span data-ttu-id="0227a-130">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="0227a-130">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="0227a-131">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="0227a-131">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0227a-132">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="0227a-132">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="0227a-133">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0227a-133">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="0227a-134">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="0227a-134">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="0227a-135">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="0227a-135">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="0227a-136">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0227a-136">Select **Save**.</span></span>

5. <span data-ttu-id="0227a-137">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="0227a-137">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="0227a-138">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="0227a-138">You're still paying for the license.</span></span> <span data-ttu-id="0227a-139">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="0227a-139">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end 

## <a name="related-articles"></a><span data-ttu-id="0227a-140">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="0227a-140">Related articles</span></span>

[<span data-ttu-id="0227a-141">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="0227a-141">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="0227a-142">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="0227a-142">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="0227a-143">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="0227a-143">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="0227a-144">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="0227a-144">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="0227a-145">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="0227a-145">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
