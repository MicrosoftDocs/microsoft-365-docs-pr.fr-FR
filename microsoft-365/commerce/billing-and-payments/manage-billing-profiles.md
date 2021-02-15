---
title: Comprendre les profils de facturation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- MACBillingBillsPaymentsBillingProfiles
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- Commerce
search.appverid:
- MET150
description: Découvrez comment les profils de facturation supportent les factures.
ms.openlocfilehash: 708096b624caa9c23a40df4842ccfce856db048d
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49667774"
---
# <a name="understand-billing-profiles"></a><span data-ttu-id="ff895-103">Comprendre les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-103">Understand billing profiles</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="ff895-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="ff895-104">The admin center is changing.</span></span> <span data-ttu-id="ff895-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="ff895-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="ff895-106">Pour les clients commerciaux qui achètent des produits et services auprès de Microsoft, les profils de facturation vous permet de personnaliser les éléments inclus sur votre facture et la façon dont vous payez vos factures.</span><span class="sxs-lookup"><span data-stu-id="ff895-106">For commercial customers who buy products and services from Microsoft, billing profiles let you customize what items are included on your invoice, and how you pay your invoices.</span></span>

<span data-ttu-id="ff895-107">Les profils de facturation incluent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff895-107">Billing profiles include the following information:</span></span>

- <span data-ttu-id="ff895-108">**Compte de facturation** &ndash; Nom du compte de facturation lié au profil</span><span class="sxs-lookup"><span data-stu-id="ff895-108">**Billing account** &ndash; Name of the billing account the profile is related to</span></span>
- <span data-ttu-id="ff895-109">**Modes de paiement** &ndash; Cartes de crédit ou de débit, comptes bancaires, vérification ou virement bancaire</span><span class="sxs-lookup"><span data-stu-id="ff895-109">**Payment methods** &ndash; Credit or debit cards, bank accounts, check, or wire transfer</span></span>
- <span data-ttu-id="ff895-110">**Informations de contact** &ndash; Adresse de facturation et nom du contact</span><span class="sxs-lookup"><span data-stu-id="ff895-110">**Contact information** &ndash; Billing address and a contact name</span></span>
- <span data-ttu-id="ff895-111">**Paramètres de facture** &ndash; Devise en fonction du pays du compte de facturation, d’un numéro de bon de visite facultatif et de l’option de réception des factures en tant que pièces jointes d’e-mail</span><span class="sxs-lookup"><span data-stu-id="ff895-111">**Invoice settings** &ndash; Currency based on the country of the billing account, an optional PO number, and the option to receive invoices as email attachments</span></span>
- <span data-ttu-id="ff895-112">**Autorisations** &ndash; Autorisations qui vous permettent de modifier le profil de facturation, de payer les factures ou d’utiliser le mode de paiement sur le profil de facturation pour effectuer des achats</span><span class="sxs-lookup"><span data-stu-id="ff895-112">**Permissions** &ndash; Permissions that allow you to change the billing profile, pay bills, or use the payment method on the billing profile to make purchases</span></span>

<span data-ttu-id="ff895-113">Utilisez les profils de facturation pour contrôler vos achats et personnaliser votre facture.</span><span class="sxs-lookup"><span data-stu-id="ff895-113">Use billing profiles to control your purchases and customize your invoice.</span></span> <span data-ttu-id="ff895-114">Une facture mensuelle est générée pour les produits achetés avec le profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="ff895-114">A monthly invoice is generated for the products bought with the billing profile.</span></span> <span data-ttu-id="ff895-115">Vous pouvez personnaliser la facture, par exemple mettre à jour le numéro de bon de commande et la préférence de facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="ff895-115">You can customize the invoice such as update the purchase order number and email invoice preference.</span></span>

<span data-ttu-id="ff895-116">Un profil de facturation est automatiquement créé pour votre compte de facturation lors de votre premier achat.</span><span class="sxs-lookup"><span data-stu-id="ff895-116">A billing profile is automatically created for your billing account during your first purchase.</span></span> <span data-ttu-id="ff895-117">Vous pouvez créer des profils de facturation sur la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Profils de facturation</a> pour configurer d’autres factures.</span><span class="sxs-lookup"><span data-stu-id="ff895-117">You can create billing profiles on the <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Billing profiles</a> page to set up more invoices.</span></span> <span data-ttu-id="ff895-118">Par exemple, vous pouvez utiliser différents profils de facturation lorsque vous faites des achats pour chaque service de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff895-118">For example, you can use different billing profiles when you make purchases for each department in your organization.</span></span> <span data-ttu-id="ff895-119">À la date de facturation suivante, vous recevrez une facture pour chaque profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="ff895-119">On your next billing date, you'll receive an invoice for each billing profile.</span></span>

## <a name="billing-profile-roles"></a><span data-ttu-id="ff895-120">Rôles de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-120">Billing profile roles</span></span>

<span data-ttu-id="ff895-121">Les rôles sur les profils de facturation sont autorisés à contrôler les achats et à afficher et gérer les factures.</span><span class="sxs-lookup"><span data-stu-id="ff895-121">Roles on billing profiles have permissions to control purchases, and view and manage invoices.</span></span> <span data-ttu-id="ff895-122">Attribuez ces rôles aux utilisateurs qui s’en chargent du suivi, de l’organisation et du paiement des factures, comme les membres de l’équipe d’approvisionnement de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ff895-122">Assign these roles to users who track, organize, and pay invoices, like members of the procurement team in your organization.</span></span>

| <span data-ttu-id="ff895-123">Role</span><span class="sxs-lookup"><span data-stu-id="ff895-123">Role</span></span>                          | <span data-ttu-id="ff895-124">Description</span><span class="sxs-lookup"><span data-stu-id="ff895-124">Description</span></span>                                                                       |
|-----------------------------  |---------------------------------------------------------------------------------  |
| <span data-ttu-id="ff895-125">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-125">Billing profile owner</span></span>         | <span data-ttu-id="ff895-126">Tout gérer pour un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-126">Manage everything for a billing profile</span></span>                                           |
| <span data-ttu-id="ff895-127">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-127">Billing profile contributor</span></span>   | <span data-ttu-id="ff895-128">Gérer tout sauf les autorisations dans un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-128">Manage everything except permissions in a billing profile</span></span>                         |
| <span data-ttu-id="ff895-129">Lecteur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-129">Billing profile reader</span></span>        | <span data-ttu-id="ff895-130">Affichage en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-130">Read-only view of everything in a billing profile</span></span>                                 |
| <span data-ttu-id="ff895-131">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="ff895-131">Invoice manager</span></span>               | <span data-ttu-id="ff895-132">Afficher et payer les factures, et dispose d’une vue en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-132">View and pay bills, and has a read-only view of everything in a billing profile</span></span>   |

## <a name="view-billing-profiles"></a><span data-ttu-id="ff895-133">Afficher les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="ff895-133">View billing profiles</span></span>

1. <span data-ttu-id="ff895-134">Dans le Centre d’administration, accédez à la page **Factures** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Factures & paiements</a>.</span><span class="sxs-lookup"><span data-stu-id="ff895-134">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>

2. <span data-ttu-id="ff895-135">Choisissez **les profils** de facturation, puis choisissez un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ff895-135">Choose **Billing profiles**, and then choose a billing profile from the list.</span></span>

    - <span data-ttu-id="ff895-136">Sous **l’onglet** Vue d’ensemble, vous pouvez modifier les détails du profil de facturation et activer ou désactiver l’envoi d’une facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="ff895-136">On the **Overview** tab, you can edit billing profile details, and turn on or off sending an invoice by email.</span></span>

    - <span data-ttu-id="ff895-137">Sous **l’onglet Autorisations,** vous pouvez attribuer des rôles aux utilisateurs pour qu’ils paient des factures.</span><span class="sxs-lookup"><span data-stu-id="ff895-137">On the **Permissions** tab, you can assign roles to users to pay invoices.</span></span>

    - <span data-ttu-id="ff895-138">Sous **l’onglet Solde de crédit Azure,** les clients Azure peuvent consulter l’historique du solde des transactions pour les crédits Azure utilisés par ce profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="ff895-138">On the **Azure credit balance** tab, Azure customers can see transaction balance history for the Azure credits used by that billing profile.</span></span>

    - <span data-ttu-id="ff895-139">Sous **l’onglet Crédits Azure,** les clients Azure peuvent voir une liste des crédits Azure associés à ce profil de facturation, ainsi que leurs dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="ff895-139">On the **Azure credits** tab, Azure customers can see a list of Azure credits associated with that billing profile, and their expiration dates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff895-140">Si vous n’avez pas de crédits Azure, vous ne verrez pas le solde de crédit **Azure** ou les onglets crédits **Azure.**</span><span class="sxs-lookup"><span data-stu-id="ff895-140">If you don't have any Azure credits, you won't see the **Azure credit balance** or **Azure credits** tabs.</span></span>

## <a name="need-help-contact-support"></a><span data-ttu-id="ff895-141">Besoin d'aide ?</span><span class="sxs-lookup"><span data-stu-id="ff895-141">Need help?</span></span> <span data-ttu-id="ff895-142">Contactez le support technique.</span><span class="sxs-lookup"><span data-stu-id="ff895-142">Contact support.</span></span>

<span data-ttu-id="ff895-143">Si vous avez des questions ou si vous avez besoin d’aide sur vos frais Azure, créez une demande de <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">support avec le support Azure.</a></span><span class="sxs-lookup"><span data-stu-id="ff895-143">If you have questions or need help with your Azure charges, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">create a support request with Azure support</a>.</span></span>

<span data-ttu-id="ff895-144">Si vous avez des questions ou si vous avez besoin d’aide sur votre profil de facturation dans le Centre d’administration Microsoft 365, contactez le support technique [pour les produits d’entreprise.](https://docs.microsoft.com/office365/admin/contact-support-for-business-products)</span><span class="sxs-lookup"><span data-stu-id="ff895-144">If you have questions or need help with your billing profile in Microsoft 365 admin center, [contact support for business products](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>
