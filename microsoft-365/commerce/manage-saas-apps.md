---
title: Gérer les applications logicielles en tant que service pour votre organisation
f1.keywords:
- NOCSH
ms.author: cmcatee
author: cmcatee-MSFT
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
ms.localizationpriority: Normal
ms.collection:
- commerce
ms.custom: AdminSurgePortfolio
search.appverid: MET150
description: Découvrez comment activer et gérer des applications tierces dans le centre d’administration Microsoft 365.
ms.openlocfilehash: ed1a88345ae5cc135a43f4297ce518b444eaabe7
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44402581"
---
# <a name="manage-third-party-app-subscriptions-for-your-organization"></a><span data-ttu-id="1cf4d-103">Gérer les abonnements aux applications tierces pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="1cf4d-103">Manage third-party app subscriptions for your organization</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="1cf4d-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-104">The admin center is changing.</span></span> <span data-ttu-id="1cf4d-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="1cf4d-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="1cf4d-106">Vous pouvez gérer les licences et la facturation pour les applications tierces dans le centre d’administration Microsoft 365 avec le mode aperçu activé.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-106">You can manage licenses and billing for third-party apps in Microsoft 365 admin center with preview mode turned on.</span></span> <span data-ttu-id="1cf4d-107">Les fonctionnalités mises à jour incluent une gestion améliorée des abonnements, un meilleur accès aux informations de facturation et une flexibilité accrue pour la gestion des factures.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-107">Updated features include enhanced subscription management, improved access to billing information, and improved flexibility for managing bills.</span></span> <span data-ttu-id="1cf4d-108">La gestion des abonnements repose sur la plateforme commerce mise à jour de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-108">Subscription management is based on Microsoft's updated commerce platform.</span></span> <span data-ttu-id="1cf4d-109">Cela s’applique aux applications logicielles en tant que service que les clients achètent directement ou à partir d’un fournisseur tiers.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-109">This applies to software-as-a-service apps that customers purchase directly, or from third-party provider.</span></span>

## <a name="how-to-get-software-as-a-service-apps"></a><span data-ttu-id="1cf4d-110">Procédure d’obtention d’applications logicielles en tant que service</span><span class="sxs-lookup"><span data-stu-id="1cf4d-110">How to get software-as-a-service apps</span></span>

<span data-ttu-id="1cf4d-111">Il existe plusieurs façons d’acheter des applications tierces.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-111">There are a few ways to purchase third-party apps.</span></span>

- <span data-ttu-id="1cf4d-112">**Achat direct** : les clients peuvent acheter directement des abonnements à partir d' [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/)ou [AppSource](https://www.appsource.com/).</span><span class="sxs-lookup"><span data-stu-id="1cf4d-112">**Direct purchase** – Customers can directly purchase subscriptions from [Azure Marketplace](https://azuremarketplace.microsoft.com/marketplace/), or [AppSource](https://www.appsource.com/).</span></span>
- <span data-ttu-id="1cf4d-113">**Achat partenaire** : collaborez avec un partenaire via le centre de partenaires pour acheter des abonnements.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-113">**Partner purchase** –  Work with a partner through Partner Center to purchase subscriptions.</span></span>
- <span data-ttu-id="1cf4d-114">**Microsoft** propose : répondez à une proposition de Microsoft Sales qui inclut des applications tierces.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-114">**Microsoft proposal** – Respond to a proposal from Microsoft Sales that includes third-party apps.</span></span>

<span data-ttu-id="1cf4d-115">Une fois que les clients ont acheté les applications et accepté l’accord client Microsoft, ils peuvent les gérer dans le centre d’administration 365 de Microsoft ou dans Microsoft Store pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-115">Once customers purchase the apps and accept the Microsoft Customer Agreement, they can manage them in Microsoft 365 admin center, or Microsoft Store for Business.</span></span>

<span data-ttu-id="1cf4d-116">Les fournisseurs d’applications vendent leurs applications à un prix forfaitaire ou en achetant des licences pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-116">App providers sell their apps either at a flat rate, or by purchasing licenses for users.</span></span>

- <span data-ttu-id="1cf4d-117">**Taux forfaitaire** – également appelé tarification par site, les applications sont tarifées avec un prix mensuel ou annuel.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-117">**Flat rate** – Also called site-based pricing, apps are priced with a monthly or annual price.</span></span> <span data-ttu-id="1cf4d-118">Sur la page de l’application, la quantité de licences est indiquée sur Unlimited.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-118">On the app page, license quantity is listed at Unlimited.</span></span>
- <span data-ttu-id="1cf4d-119">**Licences** : les applications sont tarifées par licence.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-119">**Licenses** – Apps are priced by license.</span></span> <span data-ttu-id="1cf4d-120">Les clients attribuent des licences à chaque utilisateur au sein de leur organisation</span><span class="sxs-lookup"><span data-stu-id="1cf4d-120">Customers assign licenses to each user in their organization</span></span>

## <a name="supported-regions"></a><span data-ttu-id="1cf4d-121">Régions prises en charge</span><span class="sxs-lookup"><span data-stu-id="1cf4d-121">Supported regions</span></span>

<span data-ttu-id="1cf4d-122">La prise en charge des applications tierces est disponible dans les régions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cf4d-122">Support for third-party apps is available in these regions:</span></span>

- <span data-ttu-id="1cf4d-123">Argentine</span><span class="sxs-lookup"><span data-stu-id="1cf4d-123">Argentina</span></span>
- <span data-ttu-id="1cf4d-124">Australie</span><span class="sxs-lookup"><span data-stu-id="1cf4d-124">Australia</span></span>
- <span data-ttu-id="1cf4d-125">Canada</span><span class="sxs-lookup"><span data-stu-id="1cf4d-125">Canada</span></span>
- <span data-ttu-id="1cf4d-126">Chili</span><span class="sxs-lookup"><span data-stu-id="1cf4d-126">Chile</span></span>
- <span data-ttu-id="1cf4d-127">France</span><span class="sxs-lookup"><span data-stu-id="1cf4d-127">France</span></span>
- <span data-ttu-id="1cf4d-128">Allemagne</span><span class="sxs-lookup"><span data-stu-id="1cf4d-128">Germany</span></span>
- <span data-ttu-id="1cf4d-129">Grèce</span><span class="sxs-lookup"><span data-stu-id="1cf4d-129">Greece</span></span>
- <span data-ttu-id="1cf4d-130">Porto Rico</span><span class="sxs-lookup"><span data-stu-id="1cf4d-130">Puerto Rico</span></span>
- <span data-ttu-id="1cf4d-131">Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="1cf4d-131">South Africa</span></span>
- <span data-ttu-id="1cf4d-132">Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="1cf4d-132">United Kingdom</span></span>
- <span data-ttu-id="1cf4d-133">États-Unis</span><span class="sxs-lookup"><span data-stu-id="1cf4d-133">United States</span></span>
- <span data-ttu-id="1cf4d-134">Europe de l’ouest</span><span class="sxs-lookup"><span data-stu-id="1cf4d-134">Western Europe</span></span>

## <a name="activate-third-party-apps"></a><span data-ttu-id="1cf4d-135">Activer des applications tierces</span><span class="sxs-lookup"><span data-stu-id="1cf4d-135">Activate third-party apps</span></span>

<span data-ttu-id="1cf4d-136">Les administrateurs doivent activer les applications tierces avant de les affecter aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-136">Admins must activate third-party apps before assigning them to users.</span></span> <span data-ttu-id="1cf4d-137">Ces applications sont activées sur le portail de l’éditeur tiers.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-137">These apps are activated in the third-party publisher's portal.</span></span>

1. <span data-ttu-id="1cf4d-138">Dans le centre d’administration, accédez à la page **facturation**  >  **de vos**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">applications</a> de produits.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-138">In the admin center, go to the **Billing** > **Your products** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">Apps</a> page.</span></span>
2. <span data-ttu-id="1cf4d-139">Recherchez et sélectionnez l’application que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-139">Find and select the app you want to manage.</span></span>
3. <span data-ttu-id="1cf4d-140">Sous **paramètres & Actions**, sélectionnez **gérer dans le portail de l’éditeur**.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-140">Under **Settings & actions**, select **Manage in publisher's portal**.</span></span>

<span data-ttu-id="1cf4d-141">Vous serez dirigé vers le site de l’éditeur de l’application dans lequel vous pouvez activer l’application.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-141">You'll be directed to the app publisher's site where you can activate the app.</span></span>

## <a name="manage-third-party-apps"></a><span data-ttu-id="1cf4d-142">Gérer les applications tierces</span><span class="sxs-lookup"><span data-stu-id="1cf4d-142">Manage third-party apps</span></span>

<span data-ttu-id="1cf4d-143">Les administrateurs gèrent les applications tierces à deux emplacements : le centre d’administration Microsoft 365 et le portail du fournisseur d’applications tierces.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-143">Admins manage third-party apps in two locations: Microsoft 365 admin center, and the third-party app provider's portal.</span></span>

<span data-ttu-id="1cf4d-144">Voici ce que vous pouvez faire dans chaque portail.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-144">Here's what you can do in each portal.</span></span>

| <span data-ttu-id="1cf4d-145">Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1cf4d-145">Microsoft 365 admin center</span></span> | <span data-ttu-id="1cf4d-146">Portail d’éditeur d’application</span><span class="sxs-lookup"><span data-stu-id="1cf4d-146">App publisher portal</span></span> |
| --- | --- |
| <span data-ttu-id="1cf4d-147">Modifier la quantité de licence</span><span class="sxs-lookup"><span data-stu-id="1cf4d-147">Change license quantity</span></span> <br> <span data-ttu-id="1cf4d-148">Gérer le paiement de votre facture</span><span class="sxs-lookup"><span data-stu-id="1cf4d-148">Manage how you pay your bill</span></span> <br> <span data-ttu-id="1cf4d-149">Gérer le paiement de votre facture</span><span class="sxs-lookup"><span data-stu-id="1cf4d-149">Manage how you pay your bill</span></span> <br> <span data-ttu-id="1cf4d-150">Modifier le mode de paiement (carte de crédit)</span><span class="sxs-lookup"><span data-stu-id="1cf4d-150">Change payment method (credit card)</span></span> <br> <span data-ttu-id="1cf4d-151">Afficher la facture</span><span class="sxs-lookup"><span data-stu-id="1cf4d-151">View invoice</span></span> <br> <span data-ttu-id="1cf4d-152">Annuler l’abonnement d’application</span><span class="sxs-lookup"><span data-stu-id="1cf4d-152">Cancel app subscription</span></span> | <span data-ttu-id="1cf4d-153">Set up App (une fois pour chaque application)</span><span class="sxs-lookup"><span data-stu-id="1cf4d-153">Set up app (once for each app)</span></span> <br> <span data-ttu-id="1cf4d-154">Attribuer des licences aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1cf4d-154">Assign licenses to users</span></span> <br> <span data-ttu-id="1cf4d-155">Assistance technique</span><span class="sxs-lookup"><span data-stu-id="1cf4d-155">Technical support</span></span> |

<span data-ttu-id="1cf4d-156">Une fois l’application activée, elle reste active sauf si elle est annulée, expire ou si le paiement n’est pas maintenu à jour.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-156">After the app is activated, it remains active unless it's canceled, expires, or if payment isn't kept current.</span></span> <span data-ttu-id="1cf4d-157">Ces événements modifient l’état de l’application sur désactivé.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-157">These events change the app status to disabled.</span></span> <span data-ttu-id="1cf4d-158">Une fois qu’une application est désactivée, elle ne peut pas être réactivée.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-158">Once an app is disabled, it can't be reactivated.</span></span> <span data-ttu-id="1cf4d-159">Pour continuer à utiliser l’application, achetez une autre copie de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-159">To continue using the app, buy another copy of it.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="1cf4d-160">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="1cf4d-160">Assign licenses</span></span>

<span data-ttu-id="1cf4d-161">Les administrateurs doivent activer des applications tierces avant de les affecter aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-161">Admins need to activate third-party apps before assigning them to users.</span></span> <span data-ttu-id="1cf4d-162">Elles sont activées sur le portail de l’éditeur tiers.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-162">They're activated in the third-party publisher's portal.</span></span> <span data-ttu-id="1cf4d-163">Sur la page application, sous **paramètres & Actions**, sélectionnez le lien pour attribuer des licences.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-163">On the app page, under **Settings & actions**, select the link to assign licenses.</span></span>

1. <span data-ttu-id="1cf4d-164">Dans le centre d’administration, accédez à la page **facturation**  >  **de vos**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">applications</a> de produits.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-164">In the admin center, go to the **Billing** > **Your products** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">Apps</a> page.</span></span>
2. <span data-ttu-id="1cf4d-165">Recherchez et sélectionnez l’application que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-165">Find and select the app you want to manage.</span></span>
3. <span data-ttu-id="1cf4d-166">Sous **paramètres & Actions**, sélectionnez le lien à **gérer dans le portail de l’éditeur**.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-166">Under **Settings & actions**, select the link to **Manage in publisher's portal**.</span></span>

## <a name="change-license-quantity"></a><span data-ttu-id="1cf4d-167">Modifier la quantité de licence</span><span class="sxs-lookup"><span data-stu-id="1cf4d-167">Change license quantity</span></span>

<span data-ttu-id="1cf4d-168">Les administrateurs peuvent modifier le nombre de licences appartenant à leur organisation.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-168">Admins can change the number of licenses owned by their organization.</span></span> <span data-ttu-id="1cf4d-169">Ceci ne s’applique qu’aux applications achetées avec une tarification par siège.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-169">This only applies to apps purchased with seat-based pricing.</span></span>

1. <span data-ttu-id="1cf4d-170">Dans le centre d’administration, accédez à la page **facturation**  >  **de vos**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">applications</a> de produits.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-170">In the admin center, go to the **Billing** > **Your products** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">Apps</a> page.</span></span>
2. <span data-ttu-id="1cf4d-171">Recherchez et sélectionnez l’application que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-171">Find and select the app you want to manage.</span></span>
3. <span data-ttu-id="1cf4d-172">Sélectionnez **modifier la quantité des licences**.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-172">Select **Change license quantity**.</span></span>

## <a name="manage-payment-methods"></a><span data-ttu-id="1cf4d-173">Gestion des modes de paiement</span><span class="sxs-lookup"><span data-stu-id="1cf4d-173">Manage payment methods</span></span>

<span data-ttu-id="1cf4d-174">Les applications logicielles en tant que service ont chacune un profil de facturation affecté.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-174">Software-as-a-service apps each have a billing profile assigned to them.</span></span> <span data-ttu-id="1cf4d-175">Les profils de facturation vous permettent de personnaliser les produits inclus dans votre facture, ainsi que le mode de paiement de vos factures.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-175">Billing profiles let you customize what products are included on your invoice, and how you pay your invoices.</span></span> <span data-ttu-id="1cf4d-176">Ces parties prenantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cf4d-176">They include:</span></span>

- <span data-ttu-id="1cf4d-177">**Modes de paiement** – cartes de crédit ou transfert de chèques/fils</span><span class="sxs-lookup"><span data-stu-id="1cf4d-177">**Payment methods** – Credit cards or check/wire transfer</span></span>
- <span data-ttu-id="1cf4d-178">**Informations de contact** : adresse de facturation et nom de contact</span><span class="sxs-lookup"><span data-stu-id="1cf4d-178">**Contact information** –  Billing address and a contact name</span></span>
- <span data-ttu-id="1cf4d-179">**Rôles** : rôles qui vous permettent de modifier le profil de facturation, de payer des factures ou d’utiliser le mode de paiement sur le profil de facturation pour effectuer l’achat.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-179">**Roles** – Roles that allow you to change the billing profile, pay bills, or use the payment method on the billing profile to make purchase.</span></span>

<span data-ttu-id="1cf4d-180">Pour plus d’informations sur les profils de facturation, consultez la rubrique Understanding [Billing Profiles](https://docs.microsoft.com/microsoft-store/billing-profile).</span><span class="sxs-lookup"><span data-stu-id="1cf4d-180">For more information on billing profiles, see [Understand billing profiles](https://docs.microsoft.com/microsoft-store/billing-profile).</span></span>

### <a name="change-the-billing-profile-on-a-software-as-a-service-app-subscription"></a><span data-ttu-id="1cf4d-181">Modifier le profil de facturation sur un abonnement d’application Software-as-a-service</span><span class="sxs-lookup"><span data-stu-id="1cf4d-181">Change the billing profile on a software-as-a-service app subscription</span></span>

1. <span data-ttu-id="1cf4d-182">Dans le centre d’administration, accédez à la page **facturation**  >  **de vos**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">applications</a> de produits.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-182">In the admin center, go to the **Billing** > **Your products** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">Apps</a> page.</span></span>
2. <span data-ttu-id="1cf4d-183">Recherchez et sélectionnez l’application que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-183">Find and select the app you want to manage.</span></span>
3. <span data-ttu-id="1cf4d-184">En regard de **profil de facturation**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-184">Next to **Billing profile**, select **Edit**.</span></span>

<span data-ttu-id="1cf4d-185">Pour plus d’informations sur les factures, reportez-vous à [la rubrique comprendre votre facture](billing-and-payments/understand-your-invoice.md).</span><span class="sxs-lookup"><span data-stu-id="1cf4d-185">For more information on invoices, see [Understand your bill or invoice](billing-and-payments/understand-your-invoice.md).</span></span>

## <a name="cancel-a-software-as-a-service-app-subscription"></a><span data-ttu-id="1cf4d-186">Annuler un abonnement d’application Software-as-a-service</span><span class="sxs-lookup"><span data-stu-id="1cf4d-186">Cancel a software-as-a-service app subscription</span></span>

<span data-ttu-id="1cf4d-187">Vous pouvez annuler une application Software-as-a-service à partir de la page de l’application.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-187">You can cancel a software-as-a-service app from the app page.</span></span>

1. <span data-ttu-id="1cf4d-188">Dans le centre d’administration, accédez à la page **facturation**  >  **de vos**  >  <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">applications</a> de produits.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-188">In the admin center, go to the **Billing** > **Your products** > <a href="https://go.microsoft.com/fwlink/p/?linkid=2125823" target="_blank">Apps</a> page.</span></span>
2. <span data-ttu-id="1cf4d-189">Recherchez et sélectionnez l’application que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-189">Find and select the app you want to manage.</span></span>
3. <span data-ttu-id="1cf4d-190">Sous **paramètres & Actions**, sélectionnez **Annuler l’abonnement**.</span><span class="sxs-lookup"><span data-stu-id="1cf4d-190">Under **Settings & actions**, select **Cancel subscription**.</span></span>
