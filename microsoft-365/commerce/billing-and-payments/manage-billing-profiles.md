---
title: Gérer les profils de facturation
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
ms.openlocfilehash: 4b46709cf877ea8689f72b66d5ac357272e4737d
ms.sourcegitcommit: 7713e777731025c165e9e936198609503ade5665
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "38753543"
---
# <a name="manage-billing-profiles"></a><span data-ttu-id="030b3-104">Gérer les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-104">Manage billing profiles</span></span>
<span data-ttu-id="030b3-105">Pour les clients commerciaux qui achètent des produits et des services auprès de Microsoft, les profils de facturation vous permettent de personnaliser les éléments inclus dans votre facture, ainsi que le mode de paiement de vos factures.</span><span class="sxs-lookup"><span data-stu-id="030b3-105">For commercial customers who buy products and services from Microsoft, billing profiles let you customize what items are included on your invoice, and how you pay your invoices.</span></span>

<span data-ttu-id="030b3-106">Les profils de facturation incluent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="030b3-106">Billing profiles include the following information:</span></span>

- <span data-ttu-id="030b3-107">Nom du **compte** &ndash; de facturation du compte de facturation auquel le profil est lié</span><span class="sxs-lookup"><span data-stu-id="030b3-107">**Billing account** &ndash; Name of the billing account the profile is related to</span></span>
- <span data-ttu-id="030b3-108">**Modes** &ndash; de paiement cartes de crédit ou de débit, comptes bancaires, chèques ou virement bancaire</span><span class="sxs-lookup"><span data-stu-id="030b3-108">**Payment methods** &ndash; Credit or debit cards, bank accounts, check, or wire transfer</span></span>
- <span data-ttu-id="030b3-109">**Informations** &ndash; de contact adresse de facturation et nom de contact</span><span class="sxs-lookup"><span data-stu-id="030b3-109">**Contact information** &ndash; Billing address and a contact name</span></span>
- <span data-ttu-id="030b3-110">Devise des **paramètres** &ndash; de facturation basée sur le pays du compte de facturation, un numéro de bon de commande facultatif et la possibilité de recevoir des factures en pièces jointes de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="030b3-110">**Invoice settings** &ndash; Currency based on the country of the billing account, an optional PO number, and the option to receive invoices as email attachments</span></span>
- <span data-ttu-id="030b3-111">Autorisations des **autorisations** &ndash; qui vous permettent de modifier le profil de facturation, de payer des factures ou d’utiliser le mode de paiement sur le profil de facturation pour effectuer des achats</span><span class="sxs-lookup"><span data-stu-id="030b3-111">**Permissions** &ndash; Permissions that allow you to change the billing profile, pay bills, or use the payment method on the billing profile to make purchases</span></span>

<span data-ttu-id="030b3-112">Utilisez les profils de facturation pour contrôler vos achats et personnaliser votre facture.</span><span class="sxs-lookup"><span data-stu-id="030b3-112">Use billing profiles to control your purchases and customize your invoice.</span></span> <span data-ttu-id="030b3-113">Une facture mensuelle est générée pour les produits achetés avec le profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="030b3-113">A monthly invoice is generated for the products bought with the billing profile.</span></span> <span data-ttu-id="030b3-114">Vous pouvez personnaliser la facture telle que mettre à jour les numéros de bon de commande et de facture par e-mail.</span><span class="sxs-lookup"><span data-stu-id="030b3-114">You can customize the invoice such as update the purchase order number and email invoice preference.</span></span>

<span data-ttu-id="030b3-115">Un profil de facturation est automatiquement créé pour votre compte de facturation lors de votre premier achat.</span><span class="sxs-lookup"><span data-stu-id="030b3-115">A billing profile is automatically created for your billing account during your first purchase.</span></span> <span data-ttu-id="030b3-116">Vous pouvez créer des profils de facturation sur la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">profils de facturation</a> pour configurer davantage de factures.</span><span class="sxs-lookup"><span data-stu-id="030b3-116">You can create billing profiles on the <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Billing profiles</a> page to set up more invoices.</span></span> <span data-ttu-id="030b3-117">Par exemple, vous pouvez utiliser différents profils de facturation lorsque vous effectuez des achats pour chaque service de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="030b3-117">For example, you can use different billing profiles when you make purchases for each department in your organization.</span></span> <span data-ttu-id="030b3-118">À la prochaine date de facturation, vous recevrez une facture pour chaque profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="030b3-118">On your next billing date, you'll receive an invoice for each billing profile.</span></span>

## <a name="billing-profile-roles"></a><span data-ttu-id="030b3-119">Rôles de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-119">Billing profile roles</span></span>

<span data-ttu-id="030b3-120">Les rôles sur les profils de facturation sont des autorisations permettant de contrôler les achats et d’afficher et de gérer les factures.</span><span class="sxs-lookup"><span data-stu-id="030b3-120">Roles on billing profiles have permissions to control purchases, and view and manage invoices.</span></span> <span data-ttu-id="030b3-121">Affectez ces rôles aux utilisateurs qui effectuent le suivi, organisent et paient des factures, comme les membres de l’équipe d’approvisionnement de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="030b3-121">Assign these roles to users who track, organize, and pay invoices, like members of the procurement team in your organization.</span></span>

| <span data-ttu-id="030b3-122">Rôle</span><span class="sxs-lookup"><span data-stu-id="030b3-122">Role</span></span>                          | <span data-ttu-id="030b3-123">Description</span><span class="sxs-lookup"><span data-stu-id="030b3-123">Description</span></span>                                                                       |
|-----------------------------  |---------------------------------------------------------------------------------  |
| <span data-ttu-id="030b3-124">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-124">Billing profile owner</span></span>         | <span data-ttu-id="030b3-125">Gérer tout le contenu d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-125">Manage everything for a billing profile</span></span>                                           |
| <span data-ttu-id="030b3-126">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-126">Billing profile contributor</span></span>   | <span data-ttu-id="030b3-127">Gérer tout sauf les autorisations dans un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-127">Manage everything except permissions in a billing profile</span></span>                         |
| <span data-ttu-id="030b3-128">Lecteur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-128">Billing profile reader</span></span>        | <span data-ttu-id="030b3-129">Vue en lecture seule de tous les éléments d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-129">Read-only view of everything in a billing profile</span></span>                                 |
| <span data-ttu-id="030b3-130">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="030b3-130">Invoice manager</span></span>               | <span data-ttu-id="030b3-131">Afficher et payer des factures, et dispose d’une vue en lecture seule de tous les éléments d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-131">View and pay bills, and has a read-only view of everything in a billing profile</span></span>   |

## <a name="view-billing-profiles"></a><span data-ttu-id="030b3-132">Afficher les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="030b3-132">View billing profiles</span></span>

1. <span data-ttu-id="030b3-133">Dans le centre d’administration, accédez à **la** \> page <a href="https://go.microsoft.com/fwlink/p/?linkid=848039" target="_blank">factures & paiement</a> .</span><span class="sxs-lookup"><span data-stu-id="030b3-133">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=848039" target="_blank">Bills & payments</a> page.</span></span>

2. <span data-ttu-id="030b3-134">Sélectionnez **profils de facturation**, puis un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="030b3-134">Choose **Billing profiles**, and then choose a billing profile from the list.</span></span>

    - <span data-ttu-id="030b3-135">Sous l’onglet **vue d’ensemble** , vous pouvez modifier les détails du profil de facturation et activer ou désactiver l’envoi d’une facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="030b3-135">On the **Overview** tab, you can edit billing profile details, and turn on or off sending an invoice by email.</span></span>

    - <span data-ttu-id="030b3-136">Sous l’onglet **autorisations** , vous pouvez attribuer des rôles aux utilisateurs afin de payer des factures.</span><span class="sxs-lookup"><span data-stu-id="030b3-136">On the **Permissions** tab, you can assign roles to users to pay invoices.</span></span>

    - <span data-ttu-id="030b3-137">Dans l’onglet **Solde crédit Azure** , les clients Azure peuvent consulter l’historique des soldes de transaction pour les crédits Azure utilisés par ce profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="030b3-137">On the **Azure credit balance** tab, Azure customers can see transaction balance history for the Azure credits used by that billing profile.</span></span>

    - <span data-ttu-id="030b3-138">Sous l’onglet **crédits Azure** , les clients Azure peuvent afficher la liste des crédits Azure associés à ce profil de facturation, ainsi que leurs dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="030b3-138">On the **Azure credits** tab, Azure customers can see a list of Azure credits associated with that billing profile, and their expiration dates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="030b3-139">Si vous n’avez aucun crédit Azure, vous ne verrez pas les onglets **solde de crédit Azure** ou **crédits Azure** .</span><span class="sxs-lookup"><span data-stu-id="030b3-139">If you don't have any Azure credits, you won't see the **Azure credit balance** or **Azure credits** tabs.</span></span>

## <a name="need-help-contact-support"></a><span data-ttu-id="030b3-140">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="030b3-140">Need help?</span></span> <span data-ttu-id="030b3-141">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="030b3-141">Contact support.</span></span>

<span data-ttu-id="030b3-142">Si vous avez des questions ou si vous avez besoin d’aide pour vos frais Azure, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">créez une demande de support technique avec Azure</a>.</span><span class="sxs-lookup"><span data-stu-id="030b3-142">If you have questions or need help with your Azure charges, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">create a support request with Azure support</a>.</span></span>

<span data-ttu-id="030b3-143">Si vous avez des questions ou si vous avez besoin d’aide pour votre profil de facturation dans le centre d’administration Microsoft 365, [Contactez le support technique pour les produits professionnels](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="030b3-143">If you have questions or need help with your billing profile in Microsoft 365 admin center, [contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>