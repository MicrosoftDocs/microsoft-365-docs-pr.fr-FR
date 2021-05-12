---
title: Comprendre les profils de facturation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: scotv
ms.reviewer: jkinma, jmueller
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
- commerce_billing
search.appverid: MET150
description: Découvrez comment les profils de facturation supportent les factures.
ms.date: 04/02/2021
ms.openlocfilehash: 36d762e50627763b7856ed1fe6c109e8da2b4789
ms.sourcegitcommit: 967f64dfa1a05f31179c8316b96bfb7758a5d990
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "52332029"
---
# <a name="understand-billing-profiles"></a><span data-ttu-id="c60ff-103">Comprendre les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-103">Understand billing profiles</span></span>

<span data-ttu-id="c60ff-104">Pour les clients commerciaux qui achètent des produits et services auprès de Microsoft, les profils de facturation vous permet de personnaliser les éléments inclus sur votre facture et la façon dont vous payez vos factures.</span><span class="sxs-lookup"><span data-stu-id="c60ff-104">For commercial customers who buy products and services from Microsoft, billing profiles let you customize what items are included on your invoice, and how you pay your invoices.</span></span>

<span data-ttu-id="c60ff-105">Les profils de facturation incluent les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c60ff-105">Billing profiles include the following information:</span></span>

- <span data-ttu-id="c60ff-106">**Compte de facturation** &ndash; Nom du compte de facturation lié au profil</span><span class="sxs-lookup"><span data-stu-id="c60ff-106">**Billing account** &ndash; Name of the billing account the profile is related to</span></span>
- <span data-ttu-id="c60ff-107">**Modes de paiement** &ndash; Cartes de crédit ou de débit, comptes bancaires, vérification ou virement bancaire</span><span class="sxs-lookup"><span data-stu-id="c60ff-107">**Payment methods** &ndash; Credit or debit cards, bank accounts, check, or wire transfer</span></span>
- <span data-ttu-id="c60ff-108">**Informations de contact** &ndash; Adresse de facturation et nom du contact</span><span class="sxs-lookup"><span data-stu-id="c60ff-108">**Contact information** &ndash; Billing address and a contact name</span></span>
- <span data-ttu-id="c60ff-109">**Paramètres de facture** &ndash; Devise en fonction du pays du compte de facturation, d’un numéro de bon de visite facultatif et de l’option de réception des factures en tant que pièces jointes d’e-mail</span><span class="sxs-lookup"><span data-stu-id="c60ff-109">**Invoice settings** &ndash; Currency based on the country of the billing account, an optional PO number, and the option to receive invoices as email attachments</span></span>
- <span data-ttu-id="c60ff-110">**Autorisations** &ndash; Autorisations qui vous permettent de modifier le profil de facturation, de payer les factures ou d’utiliser le mode de paiement sur le profil de facturation pour effectuer des achats</span><span class="sxs-lookup"><span data-stu-id="c60ff-110">**Permissions** &ndash; Permissions that allow you to change the billing profile, pay bills, or use the payment method on the billing profile to make purchases</span></span>

<span data-ttu-id="c60ff-111">Utilisez les profils de facturation pour contrôler vos achats et personnaliser votre facture.</span><span class="sxs-lookup"><span data-stu-id="c60ff-111">Use billing profiles to control your purchases and customize your invoice.</span></span> <span data-ttu-id="c60ff-112">Une facture mensuelle est générée pour les produits achetés avec le profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="c60ff-112">A monthly invoice is generated for the products bought with the billing profile.</span></span> <span data-ttu-id="c60ff-113">Vous pouvez personnaliser la facture, par exemple mettre à jour le numéro de bon de commande et la préférence de facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c60ff-113">You can customize the invoice such as update the purchase order number and email invoice preference.</span></span>

<span data-ttu-id="c60ff-114">Un profil de facturation est automatiquement créé pour votre compte de facturation lors de votre premier achat.</span><span class="sxs-lookup"><span data-stu-id="c60ff-114">A billing profile is automatically created for your billing account during your first purchase.</span></span> <span data-ttu-id="c60ff-115">Vous pouvez créer des profils de facturation sur la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Profils de facturation</a> pour configurer d’autres factures.</span><span class="sxs-lookup"><span data-stu-id="c60ff-115">You can create billing profiles on the <a href="https://go.microsoft.com/fwlink/p/?linkid=2103629" target="_blank">Billing profiles</a> page to set up more invoices.</span></span> <span data-ttu-id="c60ff-116">Par exemple, vous pouvez utiliser différents profils de facturation lorsque vous faites des achats pour chaque service de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c60ff-116">For example, you can use different billing profiles when you make purchases for each department in your organization.</span></span> <span data-ttu-id="c60ff-117">À la prochaine date de facturation, vous recevrez une facture pour chaque profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="c60ff-117">On your next billing date, you'll receive an invoice for each billing profile.</span></span>

## <a name="billing-profile-roles"></a><span data-ttu-id="c60ff-118">Rôles de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-118">Billing profile roles</span></span>

<span data-ttu-id="c60ff-119">Les rôles sur les profils de facturation sont autorisés à contrôler les achats et à afficher et gérer les factures.</span><span class="sxs-lookup"><span data-stu-id="c60ff-119">Roles on billing profiles have permissions to control purchases, and view and manage invoices.</span></span> <span data-ttu-id="c60ff-120">Attribuez ces rôles aux utilisateurs qui s’en chargent du suivi, de l’organisation et du paiement des factures, comme les membres de l’équipe d’approvisionnement de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c60ff-120">Assign these roles to users who track, organize, and pay invoices, like members of the procurement team in your organization.</span></span>

| <span data-ttu-id="c60ff-121">Role</span><span class="sxs-lookup"><span data-stu-id="c60ff-121">Role</span></span>                         | <span data-ttu-id="c60ff-122">Description</span><span class="sxs-lookup"><span data-stu-id="c60ff-122">Description</span></span>                                                                      |
|----------------------------- |--------------------------------------------------------------------------------- |
| <span data-ttu-id="c60ff-123">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-123">Billing profile owner</span></span>        | <span data-ttu-id="c60ff-124">Tout gérer pour un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-124">Manage everything for a billing profile</span></span>                                          |
| <span data-ttu-id="c60ff-125">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-125">Billing profile contributor</span></span>  | <span data-ttu-id="c60ff-126">Gérer tout sauf les autorisations dans un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-126">Manage everything except permissions in a billing profile</span></span>                        |
| <span data-ttu-id="c60ff-127">Lecteur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-127">Billing profile reader</span></span>       | <span data-ttu-id="c60ff-128">Affichage en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-128">Read-only view of everything in a billing profile</span></span>                                |
| <span data-ttu-id="c60ff-129">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="c60ff-129">Invoice manager</span></span>              | <span data-ttu-id="c60ff-130">Afficher et payer les factures, et dispose d’une vue en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-130">View and pay bills, and has a read-only view of everything in a billing profile</span></span>  |

## <a name="view-billing-profiles"></a><span data-ttu-id="c60ff-131">Afficher les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="c60ff-131">View billing profiles</span></span>

1. <span data-ttu-id="c60ff-132">Dans le Centre d’administration, accédez à la page **Factures** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Factures & paiements</a>.</span><span class="sxs-lookup"><span data-stu-id="c60ff-132">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="c60ff-133">Choisissez **les profils** de facturation, puis choisissez un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c60ff-133">Choose **Billing profiles**, and then choose a billing profile from the list.</span></span>

    - <span data-ttu-id="c60ff-134">Sous **l’onglet** Vue d’ensemble, vous pouvez modifier les détails du profil de facturation et activer ou désactiver l’envoi d’une facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c60ff-134">On the **Overview** tab, you can edit billing profile details, and turn on or off sending an invoice by email.</span></span>
    - <span data-ttu-id="c60ff-135">Sous **l’onglet Autorisations,** vous pouvez attribuer des rôles aux utilisateurs pour qu’ils paient des factures.</span><span class="sxs-lookup"><span data-stu-id="c60ff-135">On the **Permissions** tab, you can assign roles to users to pay invoices.</span></span>
    - <span data-ttu-id="c60ff-136">Sous **l’onglet Solde de crédit Azure,** les clients Azure peuvent voir l’historique du solde des transactions pour les crédits Azure utilisés par ce profil de facturation.</span><span class="sxs-lookup"><span data-stu-id="c60ff-136">On the **Azure credit balance** tab, Azure customers can see transaction balance history for the Azure credits used by that billing profile.</span></span>
    - <span data-ttu-id="c60ff-137">Sous **l’onglet Crédits Azure,** les clients Azure peuvent voir une liste des crédits Azure associés à ce profil de facturation, ainsi que leurs dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="c60ff-137">On the **Azure credits** tab, Azure customers can see a list of Azure credits associated with that billing profile, and their expiration dates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c60ff-138">Si vous n’avez pas de crédits Azure, vous ne verrez pas le solde de crédit **Azure** ou les onglets crédits **Azure.**</span><span class="sxs-lookup"><span data-stu-id="c60ff-138">If you don't have any Azure credits, you won't see the **Azure credit balance** or **Azure credits** tabs.</span></span>

## <a name="need-help-contact-support"></a><span data-ttu-id="c60ff-139">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="c60ff-139">Need help?</span></span> <span data-ttu-id="c60ff-140">Contacter l’assistance</span><span class="sxs-lookup"><span data-stu-id="c60ff-140">Contact support</span></span>

<span data-ttu-id="c60ff-141">Si vous avez des questions ou avez besoin d’aide sur vos frais Azure, créez une demande de <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">support avec le support Azure.</a></span><span class="sxs-lookup"><span data-stu-id="c60ff-141">If you have questions or need help with your Azure charges, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">create a support request with Azure support</a>.</span></span>

<span data-ttu-id="c60ff-142">Si vous avez des questions ou si vous avez besoin d’aide sur votre profil de facturation dans le Centre d’administration Microsoft 365, contactez le support technique [pour les produits d’entreprise.](../../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="c60ff-142">If you have questions or need help with your billing profile in Microsoft 365 admin center, [contact support for business products](../../business-video/get-help-support.md).</span></span>
