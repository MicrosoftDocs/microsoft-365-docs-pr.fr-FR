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
ms.openlocfilehash: e66efe12e05d2aaf286b689c955f17c8401144f1
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52537330"
---
# <a name="understand-billing-profiles"></a><span data-ttu-id="513b4-103">Comprendre les profils de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-103">Understand billing profiles</span></span>

<span data-ttu-id="513b4-104">Un profil de facturation contient un mode de paiement, des informations de facturation et d’autres paramètres de facture, tels que le numéro de bon de commande et les préférences de facture par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="513b4-104">A billing profile contains a payment method, Bill-to information, and other invoice settings, such as purchase order number and email invoice preference.</span></span> <span data-ttu-id="513b4-105">Vous utilisez un profil de facturation pour payer les produits que vous achetez auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="513b4-105">You use a billing profile to pay for the products that you buy from Microsoft.</span></span> <span data-ttu-id="513b4-106">Un profil de facturation est créé automatiquement lorsqu’un utilisateur effectue un achat en libre-service.</span><span class="sxs-lookup"><span data-stu-id="513b4-106">A billing profile is automatically created when a user makes a self-service purchase.</span></span> <span data-ttu-id="513b4-107">Chaque profil de facturation est facturé séparément.</span><span class="sxs-lookup"><span data-stu-id="513b4-107">Each billing profile is invoiced separately.</span></span>

> [!NOTE]
>
> <span data-ttu-id="513b4-108">Les profils de facturation ne sont pas disponibles pour les clients qui achètent des produits et des services Microsoft.com ou sur la page Acheter des **services** du Centre d’administration Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="513b4-108">Billing profiles are not available to customers who buy products and services from Microsoft.com or on the **Purchase services** page of the Microsoft 365 admin center.</span></span>

## <a name="what-are-billing-profile-roles"></a><span data-ttu-id="513b4-109">Quels sont les rôles de profil de facturation ?</span><span class="sxs-lookup"><span data-stu-id="513b4-109">What are billing profile roles?</span></span>

<span data-ttu-id="513b4-110">Les rôles sur les profils de facturation sont autorisés à contrôler les achats et à afficher et gérer les factures.</span><span class="sxs-lookup"><span data-stu-id="513b4-110">Roles on billing profiles have permissions to control purchases, and view and manage invoices.</span></span> <span data-ttu-id="513b4-111">Attribuez ces rôles aux utilisateurs qui s’en chargent du suivi, de l’organisation et du paiement des factures.</span><span class="sxs-lookup"><span data-stu-id="513b4-111">Assign these roles to users who track, organize, and pay invoices.</span></span> <span data-ttu-id="513b4-112">Par exemple, les membres de l’équipe d’approvisionnement de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="513b4-112">For example, members of the procurement team in your organization.</span></span>

| <span data-ttu-id="513b4-113">Role</span><span class="sxs-lookup"><span data-stu-id="513b4-113">Role</span></span>                         | <span data-ttu-id="513b4-114">Description</span><span class="sxs-lookup"><span data-stu-id="513b4-114">Description</span></span>                                                                      |
|----------------------------- |--------------------------------------------------------------------------------- |
| <span data-ttu-id="513b4-115">Propriétaire du profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-115">Billing profile owner</span></span>        | <span data-ttu-id="513b4-116">Tout gérer pour un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-116">Manage everything for a billing profile</span></span>                                          |
| <span data-ttu-id="513b4-117">Collaborateur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-117">Billing profile contributor</span></span>  | <span data-ttu-id="513b4-118">Gérer tout sauf les autorisations dans un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-118">Manage everything except permissions in a billing profile</span></span>                        |
| <span data-ttu-id="513b4-119">Lecteur de profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-119">Billing profile reader</span></span>       | <span data-ttu-id="513b4-120">Affichage en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-120">Read-only view of everything in a billing profile</span></span>                                |
| <span data-ttu-id="513b4-121">Gestionnaire de factures</span><span class="sxs-lookup"><span data-stu-id="513b4-121">Invoice manager</span></span>              | <span data-ttu-id="513b4-122">Afficher et payer les factures, et dispose d’une vue en lecture seule de tous les informations d’un profil de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-122">View and pay bills, and has a read-only view of everything in a billing profile</span></span>  |

## <a name="view-my-billing-profiles"></a><span data-ttu-id="513b4-123">Afficher mes profils de facturation</span><span class="sxs-lookup"><span data-stu-id="513b4-123">View my billing profiles</span></span>

> [!NOTE]
>
> <span data-ttu-id="513b4-124">Si vous suivez ces étapes et que la liste des profils de facturation est vide, cela signifie que vous n’avez pas de profil de facturation et que vous ne pouvez pas utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="513b4-124">If you follow these steps and the billing profiles list is empty, it means that you don’t have a billing profile, and can’t use this feature.</span></span>

1. <span data-ttu-id="513b4-125">Dans le Centre d’administration, accédez à la page **Factures** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Factures & paiements</a>.</span><span class="sxs-lookup"><span data-stu-id="513b4-125">In the admin center, go to the **Billing** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2102895" target="_blank">Bills & payments</a> page.</span></span>
2. <span data-ttu-id="513b4-126">Sélectionnez **l’onglet Profil** de facturation, puis sélectionnez un profil de facturation dans la liste.</span><span class="sxs-lookup"><span data-stu-id="513b4-126">Select the **Billing profile** tab, then select a billing profile from the list.</span></span>

<span data-ttu-id="513b4-127">Chaque profil de facturation inclut les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="513b4-127">Each billing profile includes the following information:</span></span>

- <span data-ttu-id="513b4-128">**Nom et état du profil de facturation** &ndash; Nom unique du profil de facturation et si le profil de facturation est actif ou désactivé pour l’achat.</span><span class="sxs-lookup"><span data-stu-id="513b4-128">**Billing profile name and status** &ndash; The unique name of the billing profile, and whether the billing profile is active or disabled for purchasing.</span></span>
- <span data-ttu-id="513b4-129">**Paramètres de facture** &ndash; Devise en fonction du pays du compte de facturation, des informations sur la fréquence et la date de facturation, l’option de réception de factures en pièces jointes et un champ de numéro de bon de visite facultatif</span><span class="sxs-lookup"><span data-stu-id="513b4-129">**Invoice settings** &ndash; Currency based on the country of the billing account, information about invoice frequency and date, the option to receive invoices as email attachments, and an optional PO number field</span></span>
- <span data-ttu-id="513b4-130">**Modes de paiement** &ndash; Indique le mode de paiement principal et de sauvegarde, le caser, pour le profil</span><span class="sxs-lookup"><span data-stu-id="513b4-130">**Payment methods** &ndash; Shows the primary and backup payment method, if any, for the profile</span></span>
- <span data-ttu-id="513b4-131">**Compte de facturation** &ndash; Nom du compte de facturation lié au profil.</span><span class="sxs-lookup"><span data-stu-id="513b4-131">**Billing account** &ndash; Name of the billing account the profile is related to.</span></span> <span data-ttu-id="513b4-132">Pour plus d’informations sur les comptes de facturation, voir [Comprendre les comptes de facturation.](../manage-billing-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="513b4-132">For more information about billing accounts, see [Understand billing accounts](../manage-billing-accounts.md).</span></span>
- <span data-ttu-id="513b4-133">**Informations de contact** &ndash; Adresse de facturation, nom de contact et adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="513b4-133">**Contact information** &ndash; Billing address and contact name and email address</span></span>
- <span data-ttu-id="513b4-134">**Rôles de profil de facturation** &ndash; Liste des personnes affectées à l’un des rôles de profil de facturation pour ce profil.</span><span class="sxs-lookup"><span data-stu-id="513b4-134">**Billing profile roles** &ndash; A list of people who are assigned one of the billing profile roles to do things for that profile.</span></span> <span data-ttu-id="513b4-135">Par exemple, payez les factures, ajoutez un numéro de bon de paiement ou remplacez le mode de paiement utilisé pour effectuer des achats.</span><span class="sxs-lookup"><span data-stu-id="513b4-135">For example, pay bills, add a PO number, or replace the payment method that is used to make purchases.</span></span>

> [!NOTE]
>
> <span data-ttu-id="513b4-136">Vous ne pouvez attribuer des rôles de profil de facturation qu’aux utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="513b4-136">You can only assign billing profile roles to users in your organization.</span></span>

## <a name="need-help-contact-support"></a><span data-ttu-id="513b4-137">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="513b4-137">Need help?</span></span> <span data-ttu-id="513b4-138">Contacter le support technique</span><span class="sxs-lookup"><span data-stu-id="513b4-138">Contact support</span></span>

<span data-ttu-id="513b4-139">Si vous avez des questions ou avez besoin d’aide sur vos frais Azure, créez une demande de <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">support avec le support Azure.</a></span><span class="sxs-lookup"><span data-stu-id="513b4-139">If you have questions or need help with your Azure charges, <a href="https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest" target="_blank">create a support request with Azure support</a>.</span></span>

<span data-ttu-id="513b4-140">Si vous avez des questions ou si vous avez besoin d’aide sur votre profil de facturation dans Microsoft 365 centre d’administration, [contactez le support technique.](../../business-video/get-help-support.md)</span><span class="sxs-lookup"><span data-stu-id="513b4-140">If you have questions or need help with your billing profile in Microsoft 365 admin center, [contact support](../../business-video/get-help-support.md).</span></span>

## <a name="related-content"></a><span data-ttu-id="513b4-141">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="513b4-141">Related content</span></span>

<span data-ttu-id="513b4-142">[Comment payer votre abonnement avec un profil de facturation](pay-for-subscription-billing-profile.md) (article)</span><span class="sxs-lookup"><span data-stu-id="513b4-142">[How to pay for your subscription with a billing profile](pay-for-subscription-billing-profile.md) (article)</span></span>\
<span data-ttu-id="513b4-143">[Comprendre les comptes de facturation](../manage-billing-accounts.md) (article)</span><span class="sxs-lookup"><span data-stu-id="513b4-143">[Understand billing accounts](../manage-billing-accounts.md) (article)</span></span>\
<span data-ttu-id="513b4-144">[Gérer les modes de paiement](manage-payment-methods.md) (article)</span><span class="sxs-lookup"><span data-stu-id="513b4-144">[Manage payment methods](manage-payment-methods.md) (article)</span></span>
