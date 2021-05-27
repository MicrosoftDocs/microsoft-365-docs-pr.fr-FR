---
title: Ajouter, modifier ou supprimer un partenaire conseiller en abonnement
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: f86e8177-936e-491e-9024-44dea2b296ff
description: Ajoutez un partenaire de registre au moment de l Microsoft 365, modifiez-le ou supprimez un partenaire d’un abonnement.
ms.openlocfilehash: 4cebbce41cbd2a500cc502b808734f6056271d12
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683342"
---
# <a name="add-change-or-delete-a-subscription-advisor-partner"></a><span data-ttu-id="71b72-103">Ajouter, modifier ou supprimer un partenaire conseiller en abonnement</span><span class="sxs-lookup"><span data-stu-id="71b72-103">Add, change, or delete a subscription advisor partner</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="71b72-104">Cet article s’applique Office 365 géré par 21Vianet en Chine.</span><span class="sxs-lookup"><span data-stu-id="71b72-104">This article applies to Office 365 operated by 21Vianet in China.</span></span> <span data-ttu-id="71b72-105">Il est pour les organisations qui souhaitent autoriser un partenaire 21Vianet à administrer leur abonnement Office 365 pour eux.</span><span class="sxs-lookup"><span data-stu-id="71b72-105">It is for organizations who want to allow a 21Vianet Partner to administer their Office 365 subscription for them.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

<span data-ttu-id="71b72-106">[] Un partenaire agréé de Microsoft (conseiller en abonnement) vous fournit les conseils d'achat, le support et l'expertise technique dont vous avez besoin pour configurer et personnaliser votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="71b72-106">An authorized partner of Microsoft who serves as your subscription advisor provides the sales, support, and technical expertise you need to help you set up and maintain your subscription.</span></span> <span data-ttu-id="71b72-107">Vous pouvez ajouter un partenaire conseiller en abonnement en tant que partenaire de registre lorsque vous achetez Microsoft 365 ou à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="71b72-107">You can add a subscription advisor partner as a partner of record when you purchase Microsoft 365 or at another time.</span></span> <span data-ttu-id="71b72-108">Si vous ne travaillez pas actuellement avec un partenaire, vous en trouverez également un sur le site [web de Microsoft Pinpoint.](https://pinpoint.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="71b72-108">If you're not currently working with a partner, you can also find one on the [Microsoft Pinpoint](https://pinpoint.microsoft.com) website.</span></span>

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="71b72-109">[] Un partenaire agréé de Microsoft (conseiller en abonnement) vous fournit les conseils d'achat, le support et l'expertise technique dont vous avez besoin pour configurer et personnaliser votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="71b72-109">An authorized partner of Microsoft who serves as your subscription advisor provides the sales, support, and technical expertise you need to help you set up and maintain your subscription.</span></span> <span data-ttu-id="71b72-110">Vous pouvez ajouter un partenaire conseiller en abonnement en tant que Partenaire de référence quand vous achetez Office 365 ou à tout autre moment.</span><span class="sxs-lookup"><span data-stu-id="71b72-110">You can add a subscription advisor partner as a partner of record when you purchase Office 365 or at another time.</span></span> <span data-ttu-id="71b72-111">Si vous ne travaillez pas actuellement avec un partenaire, vous en trouverez également un sur le site [web de Microsoft Pinpoint.](https://pinpoint.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="71b72-111">If you're not currently working with a partner, you can also find one on the [Microsoft Pinpoint](https://pinpoint.microsoft.com) website.</span></span>

::: moniker-end

## <a name="before-you-begin"></a><span data-ttu-id="71b72-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="71b72-112">Before you begin</span></span>

::: moniker range="o365-worldwide"

<span data-ttu-id="71b72-113">Le partenaire que vous choisissez dépend du services Microsoft que vous utilisez et du pays ou de la région où vous utiliserez ces services.</span><span class="sxs-lookup"><span data-stu-id="71b72-113">The partner you choose depends on the Microsoft services you use and the country or region where you'll use those services.</span></span> <span data-ttu-id="71b72-114">Si vous ajoutez un partenaire, ou modifiez le partenaire pour votre abonnement, vous devez tout d'abord obtenir l'ID partenaire Microsoft de ce partenaire en lui demandant.</span><span class="sxs-lookup"><span data-stu-id="71b72-114">If you are adding a partner, or changing the partner for your subscription, first you need to get the partner's Microsoft Partner ID by asking the partner for it.</span></span>

::: moniker-end

::: moniker range="o365-germany"

<span data-ttu-id="71b72-p105">Le partenaire que vous choisissez dépend des services Office 365 que vous utilisez et du pays ou de la région dans lesquels vous utilisez ces services. Si vous ajoutez un partenaire, ou modifiez le partenaire pour votre abonnement, vous devez tout d'abord obtenir l'ID partenaire Microsoft de ce partenaire en lui demandant.</span><span class="sxs-lookup"><span data-stu-id="71b72-p105">The partner you choose depends on the Office 365 services you use and the country or region where you'll use those services. If you are adding a partner, or changing the partner for your subscription, first you need to get the partner's Microsoft Partner ID by asking the partner for it.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="71b72-117">En tant qu’administrateur de Office 365, vous pouvez créer ou modifier des utilisateurs, réinitialiser les mots de passe des utilisateurs, gérer les licences utilisateur, gérer les domaines et attribuer des autorisations d’administrateur à d’autres utilisateurs de votre organisation, entre autres choses.</span><span class="sxs-lookup"><span data-stu-id="71b72-117">As an admin for Office 365, you can create or edit users, reset user passwords, manage user licenses, manage domains, and assign admin permissions to other users in your organization, among other things.</span></span> <span data-ttu-id="71b72-118">Toutefois, si vous souhaitez qu’une autre personne puisse effectuer ces tâches administratives, vous pouvez déléguer ce rôle à un partenaire autorisé de 21Vianet en créant une relation de partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-118">However, if you want someone else to do these administrative tasks, you can delegate this role to an authorized partner of 21Vianet by creating a partner relationship.</span></span>

::: moniker-end

::: moniker range="o365-worldwide"

## <a name="add-a-partner-at-the-time-of-purchase"></a><span data-ttu-id="71b72-119">Ajouter un partenaire au moment de l'achat</span><span class="sxs-lookup"><span data-stu-id="71b72-119">Add a partner at the time of purchase</span></span>

1. <span data-ttu-id="71b72-120">Dans le Centre d’administration, allez sur la page **Des** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">**services d’achat de facturation.**</a></span><span class="sxs-lookup"><span data-stu-id="71b72-120">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">**Purchase services**</a> page.</span></span>
2. <span data-ttu-id="71b72-121">Sélectionnez le produit que vous souhaitez acheter, puis sélectionnez **Acheter.**</span><span class="sxs-lookup"><span data-stu-id="71b72-121">Select the product that you want to purchase, and then select **Buy**.</span></span>
3. <span data-ttu-id="71b72-122">Pour ajouter un nouveau partenaire, **développez Besoin d’aide** pour votre commande ? et sélectionnez Obtenir de l’aide **auprès d’un partenaire Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="71b72-122">To add a new partner, expand **Need help with your order?** and select **Get assistance from a Microsoft Partner**.</span></span><br>
<span data-ttu-id="71b72-123">Suivez les étapes de la page fournisseurs pour rechercher ou obtenir une correspondance avec un partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-123">Follow the steps on the providers page to either search for, or to get matched with a partner.</span></span>
4. <span data-ttu-id="71b72-124">Si vous avez déjà un partenaire, dans la deuxième étape de l’Assistant d’checkout, dans le volet droit, sous Informations sur le partenaire, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="71b72-124">If you already have a partner, in the second step of the checkout wizard, in the right pane, under Partner information, select **Add**.</span></span>
5. <span data-ttu-id="71b72-p107">Tapez l'ID partenaire Microsoft pour le partenaire que vous ajoutez. Vous pouvez l'obtenir en le demandant au partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-p107">Type the Microsoft Partner ID for the partner you're adding. You can get the partner's Microsoft Partner ID by asking the partner for it.</span></span>
6. <span data-ttu-id="71b72-127">Suivez les autres instructions de l'Assistant pour finaliser l'achat de vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="71b72-127">Complete the rest of the wizard to finish buying your subscriptions.</span></span>

::: moniker-end

::: moniker range="o365-germany"

## <a name="add-a-partner-at-the-time-of-purchase"></a><span data-ttu-id="71b72-128">Ajouter un partenaire au moment de l'achat</span><span class="sxs-lookup"><span data-stu-id="71b72-128">Add a partner at the time of purchase</span></span>

1. <span data-ttu-id="71b72-129">Dans le Centre [d’administration,](https://go.microsoft.com/fwlink/p/?linkid=848041)allez à la page Des services  \> **d’achat de facturation.**</span><span class="sxs-lookup"><span data-stu-id="71b72-129">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=848041), go to the **Billing** \> **Purchase services**  page.</span></span>
2. <span data-ttu-id="71b72-130">Sélectionnez le produit que vous souhaitez acheter, puis sélectionnez **Acheter.**</span><span class="sxs-lookup"><span data-stu-id="71b72-130">Select the product that you want to purchase, and then select **Buy**.</span></span>
3. <span data-ttu-id="71b72-131">Pour ajouter un nouveau partenaire, **développez Besoin d’aide** pour votre commande ? et sélectionnez Obtenir de l’aide **auprès d’un partenaire Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="71b72-131">To add a new partner, expand **Need help with your order?** and select **Get assistance from a Microsoft Partner**.</span></span><br>
<span data-ttu-id="71b72-132">Suivez les étapes de la page fournisseurs pour rechercher ou obtenir une correspondance avec un partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-132">Follow the steps on the providers page to either search for, or to get matched with a partner.</span></span>
4. <span data-ttu-id="71b72-133">Si vous avez déjà un partenaire, dans la deuxième étape de l’Assistant d’checkout, dans le volet droit, sous Informations sur le partenaire, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="71b72-133">If you already have a partner, in the second step of the checkout wizard, in the right pane, under Partner information, select **Add**.</span></span>
5. <span data-ttu-id="71b72-p108">Tapez l'ID partenaire Microsoft pour le partenaire que vous ajoutez. Vous pouvez l'obtenir en le demandant au partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-p108">Type the Microsoft Partner ID for the partner you're adding. You can get the partner's Microsoft Partner ID by asking the partner for it.</span></span>
6. <span data-ttu-id="71b72-136">Suivez les autres instructions de l'Assistant pour finaliser l'achat de vos abonnements.</span><span class="sxs-lookup"><span data-stu-id="71b72-136">Complete the rest of the wizard to finish buying your subscriptions.</span></span>

::: moniker-end

## <a name="add-a-partner-to-an-existing-subscription"></a><span data-ttu-id="71b72-137">Ajouter un partenaire à un abonnement existant</span><span class="sxs-lookup"><span data-stu-id="71b72-137">Add a partner to an existing subscription</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="71b72-138">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-138">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
2. <span data-ttu-id="71b72-139">Sous **l’onglet** Produits, sélectionnez l’abonnement à modifier.</span><span class="sxs-lookup"><span data-stu-id="71b72-139">On the **Products** tab, select the subscription that you want to edit.</span></span>
3. <span data-ttu-id="71b72-140">Dans la page des détails de l’abonnement, sous **Informations sur le partenaire,** tapez l’ID **du réseau partenaire.**</span><span class="sxs-lookup"><span data-stu-id="71b72-140">On the subscription details page, under **Partner information**, type the **Partner Network ID**.</span></span> <span data-ttu-id="71b72-141">Vous pouvez obtenir l’ID Microsoft Partner Network du partenaire en le demandant au partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-141">You can get the partner's Microsoft Partner Network ID by asking the partner for it.</span></span>
4. <span data-ttu-id="71b72-142">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="71b72-142">Select **Add**.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="71b72-143">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Abonnements</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-143">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Subscriptions</a> page.</span></span>
2. <span data-ttu-id="71b72-144">Si vous avez plusieurs abonnements, sélectionnez l’abonnement à modifier.</span><span class="sxs-lookup"><span data-stu-id="71b72-144">If you have more than one subscription, select the subscription that you want to edit.</span></span>
3. <span data-ttu-id="71b72-145">À droite, sous le coût de l’abonnement, sélectionnez les trois points (autres actions) > ajouter un **partenaire de l’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="71b72-145">On the right, under the subscription cost, select the three dots (more actions) > **Add partner of record**.</span></span>
4. <span data-ttu-id="71b72-p110">Tapez l'ID partenaire Microsoft du partenaire que vous ajoutez, puis sélectionnez **Vérifier l'ID** et **Envoyer**. Vous pouvez obtenir cet ID auprès du partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-p110">Type the Microsoft Partner ID for the partner you're adding, select **Check ID**, and then **Submit**. You can get the partner's Microsoft Partner ID by asking the partner for it.</span></span>
5. <span data-ttu-id="71b72-148">L'ID de partenaire apparaît sur la page **Abonnements**.</span><span class="sxs-lookup"><span data-stu-id="71b72-148">The partner ID displays on the **Subscriptions** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

<span data-ttu-id="71b72-149">Ce processus est initié par votre partenaire autorisé.</span><span class="sxs-lookup"><span data-stu-id="71b72-149">This process is initiated by your authorized partner.</span></span> <span data-ttu-id="71b72-150">Le partenaire vous envoie un e-mail vous demandant si vous souhaitez lui donner l’autorisation d’agir en tant que partenaire de registre.</span><span class="sxs-lookup"><span data-stu-id="71b72-150">The partner sends you an email to ask you if you want to give them permission to act as a partner of record.</span></span>
  
<span data-ttu-id="71b72-151">Pour accepter cette offre</span><span class="sxs-lookup"><span data-stu-id="71b72-151">To accept this offer</span></span>
  
1. <span data-ttu-id="71b72-152">Lisez les termes du partenaire dans l’e-mail.</span><span class="sxs-lookup"><span data-stu-id="71b72-152">Read the partner's terms in the email.</span></span>
2. <span data-ttu-id="71b72-153">Pour autoriser le contrat, sélectionnez le lien qui permet d’obtenir une page d’autorisation dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="71b72-153">To authorize the agreement, select the link, which goes to an authorization page in Office 365.</span></span>
3. <span data-ttu-id="71b72-154">Sous **Relations de** partenaires, sélectionnez **Oui** pour autoriser le partenaire à être votre administrateur délégué, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="71b72-154">Under **Partner Relationships**, select **Yes** to authorize the partner to be your delegated admin, and then select **Next**.</span></span>
4. <span data-ttu-id="71b72-155">Si l’offre de relation de partenaire est associée à un abonnement d’essai ou à une offre d’achat, créez votre compte d’essai ou d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="71b72-155">If the offer for partner relationship came with a trial subscription or a purchase offer, create your trial or subscription account.</span></span>

::: moniker-end

## <a name="change-the-partner-for-a-subscription"></a><span data-ttu-id="71b72-156">Changer de partenaire pour un abonnement</span><span class="sxs-lookup"><span data-stu-id="71b72-156">Change the partner for a subscription</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="71b72-157">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-157">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="71b72-158">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-158">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="71b72-159">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-159">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Your products</a> page.</span></span>
::: moniker-end
2. <span data-ttu-id="71b72-160">Dans la page détails des abonnements, sous **Informations sur le partenaire,** sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="71b72-160">On the subscriptions details page, under **Partner information**, select **Remove**.</span></span>
3. <span data-ttu-id="71b72-161">Tapez **l’ID Microsoft Partner Network** du nouveau partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-161">Type the **Microsoft Partner Network ID** for the new partner.</span></span> <span data-ttu-id="71b72-162">Vous pouvez obtenir l’ID partenaire Microsoft du partenaire auprès du partenaire.</span><span class="sxs-lookup"><span data-stu-id="71b72-162">You can get the partner's Microsoft Partner ID by asking the partner for it.</span></span>
4. <span data-ttu-id="71b72-163">Sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="71b72-163">Select **Add**.</span></span>
  
## <a name="view-your-partner-relationships"></a><span data-ttu-id="71b72-164">Afficher vos relations de partenaires</span><span class="sxs-lookup"><span data-stu-id="71b72-164">View your partner relationships</span></span>

- <span data-ttu-id="71b72-165">Dans le Centre d’administration, allez à la page **Paramètres**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2074649" target="_blank">relations de partenaires.</a></span><span class="sxs-lookup"><span data-stu-id="71b72-165">In the admin center, go to the **Settings** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2074649" target="_blank">Partner relationships</a> page.</span></span> <span data-ttu-id="71b72-166">Vos partenaires sont répertoriés sur cette page.</span><span class="sxs-lookup"><span data-stu-id="71b72-166">Your partners are listed on this page.</span></span>

  <span data-ttu-id="71b72-167">Si vous n’avez pas de partenaire, vous verrez un message qui indique « Il n’y a rien ici ».</span><span class="sxs-lookup"><span data-stu-id="71b72-167">If you don't have a partner, you'll see a message that says "There's nothing here."</span></span>
  
## <a name="delete-a-partner-from-a-subscription"></a><span data-ttu-id="71b72-168">Supprimer un partenaire d'un abonnement</span><span class="sxs-lookup"><span data-stu-id="71b72-168">Delete a partner from a subscription</span></span>

::: moniker range="o365-worldwide"

1. <span data-ttu-id="71b72-169">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-169">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Your products</a> page.</span></span>
::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="71b72-170">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-170">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=847745" target="_blank">Your products</a> page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="71b72-171">Dans le centre d’administration, accédez à la page **Facturation** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Produits</a>.</span><span class="sxs-lookup"><span data-stu-id="71b72-171">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=850626" target="_blank">Your products</a> page.</span></span>
::: moniker-end
2. <span data-ttu-id="71b72-172">Sous **l’onglet** Produits, sélectionnez l’abonnement à modifier.</span><span class="sxs-lookup"><span data-stu-id="71b72-172">On the **Products** tab, select the subscription that you want to edit.</span></span>
3. <span data-ttu-id="71b72-173">Dans la page détails de l’abonnement, sous **Informations sur le partenaire,** sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="71b72-173">On the subscription details page, under **Partner information**, select **Remove**.</span></span>

## <a name="remove-a-reseller-relationship"></a><span data-ttu-id="71b72-174">Supprimer une relation de revendeur</span><span class="sxs-lookup"><span data-stu-id="71b72-174">Remove a reseller relationship</span></span>

<span data-ttu-id="71b72-175">Vous ne pouvez pas supprimer une relation de revendeur vous-même.</span><span class="sxs-lookup"><span data-stu-id="71b72-175">You can't remove a reseller relationship yourself.</span></span>

::: moniker range="o365-worldwide"
  
<span data-ttu-id="71b72-176">Si vous supprimez une relation  de revendeur, l’option Supprimer est grisée et vous devez demander à votre partenaire revendeur de suivre les instructions suivantes : Supprimez une relation de revendeur avec le [partenaire.](/partner-center/remove-a-relationship)</span><span class="sxs-lookup"><span data-stu-id="71b72-176">If you are removing a reseller relationship the **Delete** option is grayed out, and you will have to ask your reseller partner to follow these instructions: [Remove a reseller relationship with partner](/partner-center/remove-a-relationship).</span></span>

::: moniker-end

::: moniker range="o365-germany"
  
<span data-ttu-id="71b72-177">Si vous supprimez une relation  de revendeur, l’option Supprimer est grisée et vous devez demander à votre partenaire revendeur de suivre les instructions suivantes : Supprimez une relation de revendeur avec le [partenaire.](/partner-center/remove-a-relationship)</span><span class="sxs-lookup"><span data-stu-id="71b72-177">If you are removing a reseller relationship the **Delete** option is grayed out, and you will have to ask your reseller partner to follow these instructions: [Remove a reseller relationship with partner](/partner-center/remove-a-relationship).</span></span>
  
::: moniker-end

::: moniker range="o365-21vianet"
  
<span data-ttu-id="71b72-178">Vous devez demander à votre partenaire revendeur de suivre les instructions suivantes : Supprimez une relation de revendeur [avec le partenaire.](/partner-center/remove-a-relationship)</span><span class="sxs-lookup"><span data-stu-id="71b72-178">You will have to ask your reseller partner to follow these instructions: [Remove a reseller relationship with partner](/partner-center/remove-a-relationship).</span></span>
  
::: moniker-end

## <a name="related-content"></a><span data-ttu-id="71b72-179">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="71b72-179">Related content</span></span>

<span data-ttu-id="71b72-180">[Rechercher votre Microsoft 365 ou revendeur](../manage/find-your-partner-or-reseller.md) (article)</span><span class="sxs-lookup"><span data-stu-id="71b72-180">[Find your Microsoft 365 partner or reseller](../manage/find-your-partner-or-reseller.md) (article)</span></span>\
<span data-ttu-id="71b72-181">[Planifier la configuration de Microsoft 365 entreprise](../setup/plan-your-setup.md) (article)</span><span class="sxs-lookup"><span data-stu-id="71b72-181">[Plan your setup of Microsoft 365 for business](../setup/plan-your-setup.md) (article)</span></span>