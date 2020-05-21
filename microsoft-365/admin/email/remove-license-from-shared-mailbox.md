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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: bb229ee9-e7be-4990-b3eb-354e75740496
description: 'Supprimer une licence d’une boîte aux lettres partagée pour l’affecter à un autre utilisateur. '
ms.openlocfilehash: 9ba411c614fee93e37ac45e58fd40bf246a9c2ab
ms.sourcegitcommit: f6840dfcfdbcadc53cda591fd6cf9ddcb749d303
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2020
ms.locfileid: "44327241"
---
# <a name="remove-a-license-from-a-shared-mailbox"></a><span data-ttu-id="a13fe-103">Supprimer une licence d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a13fe-103">Remove a license from a shared mailbox</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="a13fe-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="a13fe-104">The admin center is changing.</span></span> <span data-ttu-id="a13fe-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="a13fe-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="a13fe-106">En règle générale, les boîtes aux lettres partagées ne nécessitent pas de licence.</span><span class="sxs-lookup"><span data-stu-id="a13fe-106">Shared mailboxes usually don't require a license.</span></span> <span data-ttu-id="a13fe-107">Suivez ces instructions pour supprimer une licence d’une boîte aux lettres partagée afin de pouvoir l’attribuer à un utilisateur ou renvoyer la licence afin de ne pas payer une licence dont vous n’avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="a13fe-107">Follow these instructions to remove a license from a shared mailbox so that you can either assign it to a user or return the license so that you aren't paying for a license you don't need.</span></span>

> [!NOTE]
> <span data-ttu-id="a13fe-108">Une licence est requise dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="a13fe-108">A license is required in the following scenarios:</span></span>
> 1. <span data-ttu-id="a13fe-109">La boîte aux lettres partagée dispose de plus de 50 Go d’espace de stockage.</span><span class="sxs-lookup"><span data-stu-id="a13fe-109">The shared mailbox has more than 50 GB of storage in use.</span></span>
> 2. <span data-ttu-id="a13fe-110">La boîte aux lettres partagée utilise l’archivage inaltérable.</span><span class="sxs-lookup"><span data-stu-id="a13fe-110">The shared mailbox uses in-place archiving.</span></span>
> 3. <span data-ttu-id="a13fe-111">La boîte aux lettres partagée est placée en conservation pour litige.</span><span class="sxs-lookup"><span data-stu-id="a13fe-111">The shared mailbox is placed in litigation hold.</span></span>

  
## <a name="remove-the-license"></a><span data-ttu-id="a13fe-112">Supprimer la licence</span><span class="sxs-lookup"><span data-stu-id="a13fe-112">Remove the license</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a13fe-113">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a13fe-113">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="a13fe-114">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a13fe-114">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a13fe-115">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a13fe-115">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a13fe-116">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a13fe-116">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span> 
  
2. <span data-ttu-id="a13fe-117">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="a13fe-117">Select the shared mailbox.</span></span>

3. <span data-ttu-id="a13fe-118">Dans l’onglet **licences et applications** , développez **licences** et désactivez la case à cocher correspondant à la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a13fe-118">One the **Licenses and Apps** tab, expand **Licenses** and uncheck the box for the license you want to remove.</span></span>

4. <span data-ttu-id="a13fe-119">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-119">Select **Save changes**.</span></span>

5. <span data-ttu-id="a13fe-120">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-120">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a13fe-121">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a13fe-121">You're still paying for the license.</span></span> <span data-ttu-id="a13fe-122">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a13fe-122">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="a13fe-123">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a13fe-123">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a13fe-124">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a13fe-124">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a13fe-125">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a13fe-125">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="a13fe-126">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-126">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="a13fe-127">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a13fe-127">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="a13fe-128">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-128">Select **Save**.</span></span>

5. <span data-ttu-id="a13fe-129">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-129">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a13fe-130">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a13fe-130">You're still paying for the license.</span></span> <span data-ttu-id="a13fe-131">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a13fe-131">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="a13fe-132">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a13fe-132">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a13fe-133">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a13fe-133">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a13fe-134">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a13fe-134">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="a13fe-135">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-135">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="a13fe-136">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a13fe-136">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="a13fe-137">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-137">Select **Save**.</span></span>

5. <span data-ttu-id="a13fe-138">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a13fe-138">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a13fe-139">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a13fe-139">You're still paying for the license.</span></span> <span data-ttu-id="a13fe-140">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a13fe-140">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end 

## <a name="related-articles"></a><span data-ttu-id="a13fe-141">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a13fe-141">Related articles</span></span>

[<span data-ttu-id="a13fe-142">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="a13fe-142">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="a13fe-143">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a13fe-143">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="a13fe-144">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a13fe-144">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="a13fe-145">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a13fe-145">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="a13fe-146">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="a13fe-146">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
