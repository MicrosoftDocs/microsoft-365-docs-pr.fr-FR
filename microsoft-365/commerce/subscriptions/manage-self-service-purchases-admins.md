---
title: Gérer les achats en libre-service (administrateurs)
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
- commerce
search.appverid:
- MET150
description: Les administrateurs peuvent apprendre à gérer les achats en libre-service effectués par les utilisateurs au sein de leur organisation.
ms.openlocfilehash: ab0e98963e1274925fcf678307907a93eafc9663
ms.sourcegitcommit: 9c335d110e0b499501edc8a31b987641819118a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2020
ms.locfileid: "42409629"
---
# <a name="manage-self-service-purchases-admin"></a><span data-ttu-id="99be3-103">Gérer les achats libre-service (administrateur)</span><span class="sxs-lookup"><span data-stu-id="99be3-103">Manage self-service purchases (Admin)</span></span>

<span data-ttu-id="99be3-104">En tant qu’administrateur, vous pouvez voir les achats en libre-service effectués par les membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="99be3-104">As an admin, you can see self-service purchases made by people in your organization.</span></span> <span data-ttu-id="99be3-105">Vous pouvez voir le produit, le nom de l’acheteur, les abonnements achetés, la date d’expiration, le prix d’achat et les utilisateurs affectés pour chaque achat en libre-service.</span><span class="sxs-lookup"><span data-stu-id="99be3-105">You can see the product, purchaser name, subscriptions purchased, expiry date, purchase price, and assigned users for each self-service purchase.</span></span> <span data-ttu-id="99be3-106">Si cela est nécessaire pour votre organisation, vous pouvez désactiver l’achat en libre-service sur une base par produit via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99be3-106">If required for your organization, you can turn off self-service purchasing on a per product basis via PowerShell.</span></span> <span data-ttu-id="99be3-107">Vous disposez des mêmes stratégies de gestion des données et d’accès que les produits achetés via l’achat en libre-service ou de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="99be3-107">You have the same data management and access policies over products bought through self-service purchase or centrally.</span></span>

<span data-ttu-id="99be3-108">Vous pouvez également contrôler si les utilisateurs de votre organisation peuvent faire des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="99be3-108">You can also control whether users in your organization can make self-service purchases.</span></span> <span data-ttu-id="99be3-109">Pour plus d’informations, voir [use AllowSelfServicePurchase pour le module MSCommerce PowerShell](allowselfservicepurchase-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="99be3-109">For more information, see [Use AllowSelfServicePurchase for the MSCommerce PowerShell module](allowselfservicepurchase-powershell.md).</span></span>

## <a name="view-self-service-subscriptions"></a><span data-ttu-id="99be3-110">Afficher les abonnements en libre-service</span><span class="sxs-lookup"><span data-stu-id="99be3-110">View self-service subscriptions</span></span>

1. <span data-ttu-id="99be3-111">Dans le centre d’administration, accédez à la page produits de **facturation** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">& services</a> .</span><span class="sxs-lookup"><span data-stu-id="99be3-111">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842054" target="_blank">Products & services</a> page.</span></span>

2. <span data-ttu-id="99be3-112">En regard d' **affiner les résultats**, dans la liste déroulante **type de compte** , choisissez **self-service**.</span><span class="sxs-lookup"><span data-stu-id="99be3-112">Next to **Refine results**, from the **Account type** drop-down, choose **Self-service**.</span></span>

3. <span data-ttu-id="99be3-113">Pour afficher plus de détails sur un abonnement, choisissez-en un dans la liste.</span><span class="sxs-lookup"><span data-stu-id="99be3-113">To view more details about a subscription, choose one from the list.</span></span>

## <a name="view-who-has-licenses-for-a-self-service-purchase-subscription"></a><span data-ttu-id="99be3-114">Afficher les personnes ayant des licences pour un abonnement achat libre-service</span><span class="sxs-lookup"><span data-stu-id="99be3-114">View who has licenses for a self-service purchase subscription</span></span>

1. <span data-ttu-id="99be3-115">Dans le centre d’administration, accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">licences</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="99be3-115">In the admin center, go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=842264" target="_blank">Licenses</a> page.</span></span>

2. <span data-ttu-id="99be3-116">Choisissez l’icône de filtre, puis choisissez **self-service**.</span><span class="sxs-lookup"><span data-stu-id="99be3-116">Choose the filter icon, then choose **Self-service**.</span></span>

3. <span data-ttu-id="99be3-117">Sélectionnez un produit pour afficher les licences attribuées à des personnes.</span><span class="sxs-lookup"><span data-stu-id="99be3-117">Select a product to see licenses assigned to people.</span></span>

    > [!NOTE]
    > <span data-ttu-id="99be3-118">S’il existe plusieurs achats pour un produit, ce produit n’est répertorié qu’une seule fois et la colonne **quantité disponible** indique le total de tous les abonnements achetés pour ce produit.</span><span class="sxs-lookup"><span data-stu-id="99be3-118">If there are multiple purchases for a product, that product is only listed once, and the **Available quantity** column shows the total of all subscriptions bought for that product.</span></span>

4. <span data-ttu-id="99be3-119">La liste des **utilisateurs** est regroupée selon le nom des personnes qui ont effectué des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="99be3-119">The **Users** list is grouped by the names of people who made self-service purchases.</span></span>

5. <span data-ttu-id="99be3-120">Pour exporter une liste d’utilisateurs avec des licences pour ces abonnements, choisissez les abonnements que vous souhaitez exporter, puis choisissez **Exporter les utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="99be3-120">To export a list of users with licenses for these subscriptions, choose the subscriptions that you want to export, then choose **Export users**.</span></span>

## <a name="disable-or-enable-self-service-purchases"></a><span data-ttu-id="99be3-121">Désactiver ou activer les achats en libre-service</span><span class="sxs-lookup"><span data-stu-id="99be3-121">Disable or enable self-service purchases</span></span>

<span data-ttu-id="99be3-122">Vous pouvez désactiver ou activer les achats en libre-service pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="99be3-122">You can disable or enable self-service purchases for users in your organization.</span></span> <span data-ttu-id="99be3-123">Le module PowerShell **MSCommerce** inclut une valeur de paramètre **PolicyID** pour **AllowSelfServicePurchase** qui vous permet de contrôler si les utilisateurs de votre organisation peuvent faire des achats en libre-service et pour quels produits.</span><span class="sxs-lookup"><span data-stu-id="99be3-123">The **MSCommerce** PowerShell module includes a **PolicyID** parameter value for **AllowSelfServicePurchase** that lets you control whether users in your organization can make self-service purchases, and for which products.</span></span>

<span data-ttu-id="99be3-124">Vous pouvez utiliser le module PowerShell **MSCommerce** pour :</span><span class="sxs-lookup"><span data-stu-id="99be3-124">You can use the **MSCommerce** PowerShell module to:</span></span>

- <span data-ttu-id="99be3-125">Afficher l’État par défaut de \*\*\*\* la valeur &mdash; du paramètre AllowSelfServicePurchase, qu’elle soit activée ou désactivée par le produit</span><span class="sxs-lookup"><span data-stu-id="99be3-125">View the default state of the **AllowSelfServicePurchase** parameter value &mdash; whether it's enabled or disabled by product</span></span>
- <span data-ttu-id="99be3-126">Afficher la liste des produits applicables et indiquer si les achats en libre-service sont activés ou désactivés</span><span class="sxs-lookup"><span data-stu-id="99be3-126">View a list of applicable products and whether self-service purchase is enabled or disabled</span></span>
- <span data-ttu-id="99be3-127">Afficher ou modifier le paramètre actuel d’un produit spécifique pour l’activer ou le désactiver</span><span class="sxs-lookup"><span data-stu-id="99be3-127">View or modify the current setting for a specific product to either enable or disable it</span></span>

<span data-ttu-id="99be3-128">Pour plus d’informations, voir [use AllowSelfServicePurchase pour le module MSCommerce PowerShell](allowselfservicepurchase-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="99be3-128">For more information, see [Use AllowSelfServicePurchase for the MSCommerce PowerShell module](allowselfservicepurchase-powershell.md).</span></span>

## <a name="centralize-licenses-under-a-single-subscription"></a><span data-ttu-id="99be3-129">Centralisation des licences sous un seul abonnement</span><span class="sxs-lookup"><span data-stu-id="99be3-129">Centralize licenses under a single subscription</span></span>

<span data-ttu-id="99be3-130">Vous pouvez attribuer des licences existantes ou acheter des abonnements supplémentaires via des accords existants pour les utilisateurs affectés à des achats en libre-service.</span><span class="sxs-lookup"><span data-stu-id="99be3-130">You can assign existing licenses or purchase additional subscriptions through existing agreements for users assigned to self-service purchases.</span></span> <span data-ttu-id="99be3-131">Une fois que vous avez attribué ces licences achetées de manière centralisée, vous pouvez demander à ce que les acheteurs annulent leurs abonnements existants.</span><span class="sxs-lookup"><span data-stu-id="99be3-131">After you assign these centrally purchased licenses, you can request that purchasers cancel their existing subscriptions.</span></span>

1. <span data-ttu-id="99be3-132">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration</a> à l’aide de votre administrateur général ou de votre compte d’administrateur de facturation.</span><span class="sxs-lookup"><span data-stu-id="99be3-132">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a> with your Global admin or Billing admin account.</span></span>

2. <span data-ttu-id="99be3-133">Accédez à la page<a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">services d’achat</a> de **facturation** > .</span><span class="sxs-lookup"><span data-stu-id="99be3-133">Go to the **Billing** > <a href="https://go.microsoft.com/fwlink/p/?linkid=868433" target="_blank">Purchase services</a> page.</span></span>

3. <span data-ttu-id="99be3-134">Recherchez et sélectionnez le produit que vous souhaitez acheter, puis choisissez **acheter**.</span><span class="sxs-lookup"><span data-stu-id="99be3-134">Find and choose the product that you want to buy, then choose **Buy**.</span></span>

4. <span data-ttu-id="99be3-135">Suivez les étapes restantes pour terminer votre achat.</span><span class="sxs-lookup"><span data-stu-id="99be3-135">Complete the remaining steps to complete your purchase.</span></span>

5. <span data-ttu-id="99be3-136">Suivez les étapes de la procédure [affichage des licences pour un abonnement acheté en libre-service](#view-who-has-licenses-for-a-self-service-purchase-subscription) pour exporter une liste d’utilisateurs à référencer à l’étape 6.</span><span class="sxs-lookup"><span data-stu-id="99be3-136">Follow the steps in [View who has licenses for a self-service purchased subscription](#view-who-has-licenses-for-a-self-service-purchase-subscription) to export a list of users to reference in step 6.</span></span>

6. <span data-ttu-id="99be3-137">Attribuez des licences à toutes les personnes disposant d’une licence dans l’autre abonnement.</span><span class="sxs-lookup"><span data-stu-id="99be3-137">Assign licenses to everyone who has a license in the other subscription.</span></span> <span data-ttu-id="99be3-138">Pour connaître les étapes complètes, consultez la rubrique [attribuer des licences aux utilisateurs](../../admin/manage/assign-licenses-to-users.md).</span><span class="sxs-lookup"><span data-stu-id="99be3-138">For full steps, see [Assign licenses to users](../../admin/manage/assign-licenses-to-users.md).</span></span>

7. <span data-ttu-id="99be3-139">Contactez la personne qui a acheté l’abonnement d’achat en libre-service et demandez-lui de l’annuler.</span><span class="sxs-lookup"><span data-stu-id="99be3-139">Contact the person who bought the self-service purchase subscription and ask them to cancel it.</span></span>

## <a name="need-help-contact-us"></a><span data-ttu-id="99be3-140">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="99be3-140">Need help?</span></span> <span data-ttu-id="99be3-141">Contactez-nous.</span><span class="sxs-lookup"><span data-stu-id="99be3-141">Contact us.</span></span>

<span data-ttu-id="99be3-142">Pour les questions courantes sur les achats en libre-service, voir [FAQ sur les achats en libre-service](self-service-purchase-faq.md).</span><span class="sxs-lookup"><span data-stu-id="99be3-142">For common questions about self-service purchases, see [Self-service purchases FAQ](self-service-purchase-faq.md).</span></span>

<span data-ttu-id="99be3-143">Si vous avez des questions ou si vous avez besoin d’aide pour des achats en libre-service, [Contactez le support technique](../../admin/contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="99be3-143">If you have questions or need help with self-service purchases, [contact support](../../admin/contact-support-for-business-products.md).</span></span>
