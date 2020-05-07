---
title: Gérer les profils de facturation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
f1_keywords:
- MACBillingBillsPaymentsBillingProfiles
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- commerce
ms.custom: ''
search.appverid:
- MET150
description: Découvrez comment les profils de facturation prennent en charge les factures.
keywords: Profil de facturation, factures, frais, charges gérées
ms.openlocfilehash: f93ca5af11ba416fecd13fcceffe75055a776553
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140889"
---
# <a name="manage-billing-profiles"></a><span data-ttu-id="52216-104">Gérer les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-104">Manage billing profiles</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="52216-105">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="52216-105">The admin center is changing.</span></span> <span data-ttu-id="52216-106">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="52216-106">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="52216-107">Pour les clients commerciaux qui achètent des produits et des services auprès de Microsoft, les profils de facturation vous permettent de personnaliser les éléments inclus dans votre facture, ainsi que le mode de paiement de vos factures.</span><span class="sxs-lookup"><span data-stu-id="52216-107">For commercial customers who buy products and services from Microsoft, billing profiles let you customize what items are included on your invoice, and how you pay your invoices.</span></span>

<span data-ttu-id="52216-108">Les profils de facturation incluent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="52216-108">Billing profiles include the following information:</span></span>

- <span data-ttu-id="52216-109">Nom du **compte** &ndash; de facturation du compte de facturation auquel le profil est lié</span><span class="sxs-lookup"><span data-stu-id="52216-109">**Billing account** &ndash; Name of the billing account the profile is related to</span></span>
- <span data-ttu-id="52216-110">**Modes** &ndash; de paiement cartes de crédit ou de débit, comptes bancaires, chèques ou virement bancaire</span><span class="sxs-lookup"><span data-stu-id="52216-110">**Payment methods** &ndash; Credit or debit cards, bank accounts, check, or wire transfer</span></span>
- <span data-ttu-id="52216-111">**Informations** &ndash; de contact adresse de facturation et nom de contact</span><span class="sxs-lookup"><span data-stu-id="52216-111">**Contact information** &ndash; Billing address and a contact name</span></span>
- <span data-ttu-id="52216-112">Devise des **paramètres** &ndash; de facturation basée sur le pays du compte de facturation, un numéro de bon de commande facultatif et la possibilité de recevoir des factures en pièces jointes de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="52216-112">**Invoice settings** &ndash; Currency based on the country of the billing account, an optional PO number, and the option to receive invoices as email attachments</span></span>
- <span data-ttu-id="52216-113">Autorisations des **autorisations** &ndash; qui vous permettent de modifier le profil de facturation, de payer des factures ou d’utiliser le mode de paiement sur le profil de facturation pour effectuer des achats</span><span class="sxs-lookup"><span data-stu-id="52216-113">**Permissions** &ndash; Permissions that allow you to change the billing profile, pay bills, or use the payment method on the billing profile to make purchases</span></span>

<span data-ttu-id="52216-114">Utilisez les profils de facturation pour contrôler vos achats et personnaliser votre facture.</span><span class="sxs-lookup"><span data-stu-id="52216-114">Use billing profiles to control your purchases and customize your invoice.</span></span> <span data-ttu-id="52216-115">Une facture mensuelle est générée pour les produits achetés avec le profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="52216-115">A monthly invoice is generated for the products bought with the billing profile.</span></span> <span data-ttu-id="52216-116">Vous pouvez personnaliser la facture telle que mettre à jour les numéros de bon de commande et de facture par e-mail.</span><span class="sxs-lookup"><span data-stu-id="52216-116">You can customize the invoice such as update the purchase order number and email invoice preference.</span></span>

<span data-ttu-id="52216-117">Un profil de facturation est automatiquement créé pour votre compte de facturation lors de votre premier achat.</span><span class="sxs-lookup"><span data-stu-id="52216-117">A billing profile is automatically created for your billing account during your first purchase.</span></span> <span data-ttu-id="52216-118">Vous pouvez créer des profils de facturation sur la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">profils de facturation</a> pour configurer davantage de factures.</span><span class="sxs-lookup"><span data-stu-id="52216-118">You can create billing profiles on the <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Billing profiles</a> page to set up more invoices.</span></span> <span data-ttu-id="52216-119">Par exemple, vous pouvez utiliser différents profils de facturation lorsque vous effectuez des achats pour chaque service de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="52216-119">For example, you can use different billing profiles when you make purchases for each department in your organization.</span></span> <span data-ttu-id="52216-120">À la prochaine date de facturation, vous recevrez une facture pour chaque profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="52216-120">On your next billing date, you'll receive an invoice for each billing profile.</span></span>

## <a name="billing-profile-roles"></a><span data-ttu-id="52216-121">Rôles de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-121">Billing profile roles</span></span>

<span data-ttu-id="52216-122">Les rôles sur les profils de facturation sont des autorisations permettant de contrôler les achats et d’afficher et de gérer les factures.</span><span class="sxs-lookup"><span data-stu-id="52216-122">Roles on billing profiles have permissions to control purchases, and view and manage invoices.</span></span> <span data-ttu-id="52216-123">Affectez ces rôles aux utilisateurs qui effectuent le suivi, organisent et paient des factures, comme les membres de l’équipe d’approvisionnement de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="52216-123">Assign these roles to users who track, organize, and pay invoices, like members of the procurement team in your organization.</span></span>

| <span data-ttu-id="52216-124">Role</span><span class="sxs-lookup"><span data-stu-id="52216-124">Role</span></span>                          | <span data-ttu-id="52216-125">Description</span><span class="sxs-lookup"><span data-stu-id="52216-125">Description</span></span>                                                                       |
|-----------------------------  |---------------------------------------------------------------------------------  |
| <span data-ttu-id="52216-126">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-126">Billing profile owner</span></span>         | <span data-ttu-id="52216-127">Gérer tout le contenu d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-127">Manage everything for a billing profile</span></span>                                           |
| <span data-ttu-id="52216-128">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-128">Billing profile contributor</span></span>   | <span data-ttu-id="52216-129">Gérer tout sauf les autorisations dans un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-129">Manage everything except permissions in a billing profile</span></span>                         |
| <span data-ttu-id="52216-130">Lecteur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-130">Billing profile reader</span></span>        | <span data-ttu-id="52216-131">Vue en lecture seule de tous les éléments d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-131">Read-only view of everything in a billing profile</span></span>                                 |
| <span data-ttu-id="52216-132">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="52216-132">Invoice manager</span></span>               | <span data-ttu-id="52216-133">Afficher et payer des factures, et dispose d’une vue en lecture seule de tous les éléments d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-133">View and pay bills, and has a read-only view of everything in a billing profile</span></span>   |

## <a name="view-billing-profiles"></a><span data-ttu-id="52216-134">Afficher les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="52216-134">View billing profiles</span></span>

1. <span data-ttu-id="52216-135">Dans le Centre d’administration, accédez à la page **Factures** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=848039" target="_blank">Factures & paiements</a>.</span><span class="sxs-lookup"><span data-stu-id="52216-135">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=848039" target="_blank">Bills & payments</a> page.</span></span>

2. <span data-ttu-id="52216-136">Sélectionnez **profils de facturation**, puis un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="52216-136">Choose **Billing profiles**, and then choose a billing profile from the list.</span></span>

    - <span data-ttu-id="52216-137">Sous l’onglet **vue d’ensemble** , vous pouvez modifier les détails du profil de facturation et activer ou désactiver l’envoi d’une facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="52216-137">On the **Overview** tab, you can edit billing profile details, and turn on or off sending an invoice by email.</span></span>

    - <span data-ttu-id="52216-138">Sous l’onglet **autorisations** , vous pouvez attribuer des rôles aux utilisateurs afin de payer des factures.</span><span class="sxs-lookup"><span data-stu-id="52216-138">On the **Permissions** tab, you can assign roles to users to pay invoices.</span></span>

    - <span data-ttu-id="52216-139">Dans l’onglet **Solde crédit Azure** , les clients Azure peuvent consulter l’historique des soldes de transaction pour les crédits Azure utilisés par ce profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="52216-139">On the **Azure credit balance** tab, Azure customers can see transaction balance history for the Azure credits used by that billing profile.</span></span>

    - <span data-ttu-id="52216-140">Sous l’onglet **crédits Azure** , les clients Azure peuvent afficher la liste des crédits Azure associés à ce profil de facturation, ainsi que leurs dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="52216-140">On the **Azure credits** tab, Azure customers can see a list of Azure credits associated with that billing profile, and their expiration dates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52216-141">Si vous n’avez aucun crédit Azure, vous ne verrez pas les onglets **solde de crédit Azure** ou **crédits Azure** .</span><span class="sxs-lookup"><span data-stu-id="52216-141">If you don't have any Azure credits, you won't see the **Azure credit balance** or **Azure credits** tabs.</span></span>

## <a name="need-help-contact-support"></a><span data-ttu-id="52216-142">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="52216-142">Need help?</span></span> <span data-ttu-id="52216-143">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="52216-143">Contact support.</span></span>

<span data-ttu-id="52216-144">Si vous avez des questions ou si vous avez besoin d’aide pour vos frais Azure, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">créez une demande de support technique avec Azure</a>.</span><span class="sxs-lookup"><span data-stu-id="52216-144">If you have questions or need help with your Azure charges, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">create a support request with Azure support</a>.</span></span>

<span data-ttu-id="52216-145">Si vous avez des questions ou si vous avez besoin d’aide pour votre profil de facturation dans le centre d’administration Microsoft 365, [Contactez le support technique pour les produits professionnels](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="52216-145">If you have questions or need help with your billing profile in Microsoft 365 admin center, [contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>
