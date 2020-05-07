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
ms.openlocfilehash: fb09036fc28ea3d9c182395d0a85e467f611dfdc
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140428"
---
# <a name="remove-a-license-from-a-shared-mailbox"></a><span data-ttu-id="a5605-103">Supprimer une licence d’une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a5605-103">Remove a license from a shared mailbox</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="a5605-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="a5605-104">The admin center is changing.</span></span> <span data-ttu-id="a5605-105">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="a5605-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="a5605-106">Les boîtes aux lettres partagées n’ont besoin d’une licence que si la boîte aux lettres contient plus de 50 Go de données.</span><span class="sxs-lookup"><span data-stu-id="a5605-106">Shared mailboxes don't need a license unless the mailbox has over 50GB of data.</span></span> <span data-ttu-id="a5605-107">Suivez ces instructions pour supprimer une licence d’une boîte aux lettres partagée afin de pouvoir l’attribuer à un utilisateur ou renvoyer la licence afin de ne pas payer une licence dont vous n’avez pas besoin.</span><span class="sxs-lookup"><span data-stu-id="a5605-107">Follow these instructions to remove a license from a shared mailbox so that you can either assign it to a user or return the license so that you aren't paying for a license you don't need.</span></span>
  
## <a name="remove-the-license"></a><span data-ttu-id="a5605-108">Supprimer la licence</span><span class="sxs-lookup"><span data-stu-id="a5605-108">Remove the license</span></span>

::: moniker range="o365-worldwide"

> [!NOTE]
> <span data-ttu-id="a5605-109">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="a5605-109">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

1. <span data-ttu-id="a5605-110">Dans le Centre d’administration, accédez à la page **Utilisateurs >** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a5605-110">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=834822" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a5605-111">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a5605-111">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a5605-112">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5605-112">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span> 
  
2. <span data-ttu-id="a5605-113">Sélectionnez la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="a5605-113">Select the shared mailbox.</span></span>

3. <span data-ttu-id="a5605-114">Dans l’onglet **licences et applications** , développez **licences** et désactivez la case à cocher correspondant à la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a5605-114">One the **Licenses and Apps** tab, expand **Licenses** and uncheck the box for the license you want to remove.</span></span>

4. <span data-ttu-id="a5605-115">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="a5605-115">Select **Save changes**.</span></span>

5. <span data-ttu-id="a5605-116">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a5605-116">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a5605-117">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a5605-117">You're still paying for the license.</span></span> <span data-ttu-id="a5605-118">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a5605-118">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-germany"

 1. <span data-ttu-id="a5605-119">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a5605-119">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847686" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a5605-120">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a5605-120">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a5605-121">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5605-121">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="a5605-122">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="a5605-122">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="a5605-123">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a5605-123">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="a5605-124">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a5605-124">Select **Save**.</span></span>

5. <span data-ttu-id="a5605-125">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a5605-125">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a5605-126">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a5605-126">You're still paying for the license.</span></span> <span data-ttu-id="a5605-127">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a5605-127">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

 1. <span data-ttu-id="a5605-128">Dans le Centre d’administration, accédez à la page **Utilisateurs** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Utilisateurs actifs</a>.</span><span class="sxs-lookup"><span data-stu-id="a5605-128">In the admin center, go to the **Users** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850628" target="_blank">Active users</a> page.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a5605-129">Vous devez supprimer la licence de la page utilisateurs actifs.</span><span class="sxs-lookup"><span data-stu-id="a5605-129">You need to remove the license from the Active users page.</span></span> <span data-ttu-id="a5605-130">Vous ne pouvez pas supprimer la licence de la page de boîte aux lettres partagée car les licences sont des paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5605-130">You can't remove the license from the Shared mailbox page because licenses are user settings.</span></span>

2. <span data-ttu-id="a5605-131">Sélectionnez la boîte aux lettres partagée, puis cliquez sur **modifier** en regard de **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="a5605-131">Select the shared mailbox, and then select **Edit** next to **Product licenses**.</span></span>

3. <span data-ttu-id="a5605-132">Sur la page **licences de produits** , définissez le bouton bascule sur **désactivé** pour la licence que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="a5605-132">One the **Product licenses** page, set the toggle to **Off** for the license you want to remove.</span></span>

4. <span data-ttu-id="a5605-133">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a5605-133">Select **Save**.</span></span>

5. <span data-ttu-id="a5605-134">Lorsque vous revenez à la page **utilisateurs actifs** , l’état de la boîte aux lettres partagée est sans **licence**.</span><span class="sxs-lookup"><span data-stu-id="a5605-134">When you return to the **Active users** page, the status of the shared mailbox will be **Unlicensed**.</span></span>

6. <span data-ttu-id="a5605-135">Vous payez toujours pour cette licence.</span><span class="sxs-lookup"><span data-stu-id="a5605-135">You're still paying for the license.</span></span> <span data-ttu-id="a5605-136">Pour ne plus payer, [supprimez la licence de votre abonnement](../../commerce/licenses/remove-licenses-from-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="a5605-136">To stop paying for it, [remove the license from your subscription](../../commerce/licenses/remove-licenses-from-subscription.md).</span></span>

::: moniker-end 

## <a name="related-articles"></a><span data-ttu-id="a5605-137">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a5605-137">Related articles</span></span>

[<span data-ttu-id="a5605-138">À propos des boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="a5605-138">About shared mailboxes</span></span>](about-shared-mailboxes.md)

[<span data-ttu-id="a5605-139">Créer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a5605-139">Create a shared mailbox</span></span>](create-a-shared-mailbox.md)

[<span data-ttu-id="a5605-140">Configurer une boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a5605-140">Configure a shared mailbox</span></span>](configure-a-shared-mailbox.md)

[<span data-ttu-id="a5605-141">Convertir une boîte aux lettres utilisateur en boîte aux lettres partagée</span><span class="sxs-lookup"><span data-stu-id="a5605-141">Convert a user mailbox to a shared mailbox</span></span>](convert-user-mailbox-to-shared-mailbox.md)

[<span data-ttu-id="a5605-142">Résoudre les problèmes liés aux boîtes aux lettres partagées</span><span class="sxs-lookup"><span data-stu-id="a5605-142">Resolve issues with shared mailboxes</span></span>](resolve-issues-with-shared-mailboxes.md)
