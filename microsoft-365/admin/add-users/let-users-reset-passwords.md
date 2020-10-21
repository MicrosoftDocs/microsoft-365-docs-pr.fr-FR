---
title: Autoriser les utilisateurs à réinitialiser leurs mots de passe
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
- Adm_TOC
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5bc3f460-13cc-48c0-abd6-b80bae72d04a
description: Découvrez comment réinitialiser vos mots de passe à l’aide de l’outil de réinitialisation du mot de passe libre-service.
ms.openlocfilehash: 7ecadaa42610e0b77dc1727c11140080bd7b1779
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48646678"
---
# <a name="let-users-reset-their-own-passwords"></a><span data-ttu-id="4c692-103">Autoriser les utilisateurs à réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="4c692-103">Let users reset their own passwords</span></span>

<span data-ttu-id="4c692-104">En tant qu’administrateur 365 de Microsoft, vous pouvez autoriser les utilisateurs à utiliser l' [outil de réinitialisation du mot de passe libre-service](https://go.microsoft.com/fwlink/p/?LinkId=522677) afin de ne pas avoir à réinitialiser leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4c692-104">As the Microsoft 365 admin, you can let people use the [self-service password reset tool](https://go.microsoft.com/fwlink/p/?LinkId=522677) so you don't have to reset passwords for them.</span></span> <span data-ttu-id="4c692-105">Moins de travail pour vous !</span><span class="sxs-lookup"><span data-stu-id="4c692-105">Less work for you!</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="4c692-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4c692-106">Before you begin</span></span>
  
- <span data-ttu-id="4c692-107">Vous bénéficiez d’une réinitialisation du mot de passe en libre-service pour les utilisateurs du Cloud **gratuitement** avec les plans payants Microsoft 365 Business, Education ou imprévus.</span><span class="sxs-lookup"><span data-stu-id="4c692-107">You get self-service password reset for cloud users **free** with any Microsoft 365 business, education, or nonprofit paid plan.</span></span> <span data-ttu-id="4c692-108">Elle ne fonctionne pas avec la version d’évaluation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c692-108">It doesn't work with Microsoft 365 trial.</span></span>

- <span data-ttu-id="4c692-p103">Elle utilise Azure. Vous bénéficierez automatiquement et **gratuitement** de cette fonction dans Azure lorsque vous effectuerez ces étapes. L'activation de la réinitialisation du mot de passe libre-service ne vous coûtera rien si vous n'utilisez aucune autre fonctionnalité Azure.</span><span class="sxs-lookup"><span data-stu-id="4c692-p103">It uses Azure. You'll automatically get this feature in Azure for **free** when you do these steps. It won't cost you anything to turn on self-service password reset if you don't use other Azure features.</span></span>

- <span data-ttu-id="4c692-112">**Si vous utilisez un annuaire Active Directory local**, les deux points ci-dessus ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="4c692-112">**If you're using an on-premises Active Directory**, the above two points don't apply.</span></span> <span data-ttu-id="4c692-113">Au lieu de cela, vous pouvez configurer cela, mais **il nécessite un abonnement payant à Azure ad Premium**.</span><span class="sxs-lookup"><span data-stu-id="4c692-113">Rather, you can set this up but **it requires a paid subscription to Azure AD Premium**.</span></span>

<span data-ttu-id="4c692-114">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="4c692-114">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="4c692-115">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c692-115">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> [<span data-ttu-id="4c692-116">Qu’est-ce qu’un compte administrateur ?</span><span class="sxs-lookup"><span data-stu-id="4c692-116">What's an admin account?</span></span>](../admin-overview/admin-overview.md)

<span data-ttu-id="4c692-117">Pour effectuer ces étapes, vous devez être [administrateur général ou administrateur de mots de passe](about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="4c692-117">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

## <a name="watch-let-users-reset-their-own-passwords"></a><span data-ttu-id="4c692-118">Regarder : autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="4c692-118">Watch: Let users reset their own passwords</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S]

<span data-ttu-id="4c692-119">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span><span class="sxs-lookup"><span data-stu-id="4c692-119">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span></span>

## <a name="steps-let-people-reset-their-own-passwords"></a><span data-ttu-id="4c692-120">Étapes : autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="4c692-120">Steps: Let people reset their own passwords</span></span>

<span data-ttu-id="4c692-121">Ces étapes activent la réinitialisation du mot de passe libre-service pour tout le monde dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4c692-121">These steps turn on self-service password reset for everyone in your business.</span></span>
  
::: moniker range="o365-worldwide"

1. <span data-ttu-id="4c692-122">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration</a>, accédez à **Settings** la > page Paramètres d' **organisation** des paramètres.</span><span class="sxs-lookup"><span data-stu-id="4c692-122">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a>, go to the **Settings** > **Org settings** page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4c692-123">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **paramètres** de \> \*\* &amp; confidentialité\*\* de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="4c692-123">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4c692-124">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la **Settings** \> **Settings** \> page \*\* &amp; confidentialité\*\* de la sécurité des paramètres de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4c692-124">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Settings** \>**Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

2. <span data-ttu-id="4c692-125">En haut de la page **paramètres** de l’organisation, sélectionnez l’onglet **sécurité & confidentialité** .</span><span class="sxs-lookup"><span data-stu-id="4c692-125">At the top of the **Org settings** page, select the **Security & Privacy** tab.</span></span>
  
3. <span data-ttu-id="4c692-126">Sélectionnez **réinitialisation du mot de passe en libre-service**.</span><span class="sxs-lookup"><span data-stu-id="4c692-126">Select **Self-service Password Reset**.</span></span>

4. <span data-ttu-id="4c692-127">Sous **réinitialisation du mot de passe libre-service**, sélectionnez **accéder au portail Azure pour activer la réinitialisation du mot de passe libre-service**.</span><span class="sxs-lookup"><span data-stu-id="4c692-127">Under **Self-service password reset**, select **Go to the Azure portal to turn on self-service password reset**.</span></span>

5. <span data-ttu-id="4c692-128">Dans le volet de navigation de gauche, sélectionnez **utilisateurs**, puis, dans le volet **utilisateurs | Page tous les utilisateurs** , sélectionnez **Réinitialiser le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="4c692-128">In the left navigation pane, select **Users**, and then, on the **Users | All users** page, select **Password reset**.</span></span>
  
6. <span data-ttu-id="4c692-129">Sur la page **Propriétés** , sélectionnez **tous** pour l’activer pour tous les membres de votre entreprise, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4c692-129">On the **Properties** page, select **All** to enable it for everyone in your business, and then select **Save**.</span></span>
  
7. <span data-ttu-id="4c692-130">Lorsque les utilisateurs se connectent, ils sont invités à entrer des informations de contact supplémentaires qui les aideront à réinitialiser leur mot de passe à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="4c692-130">When your users sign in, they will be prompted to enter additional contact information that will help them reset their password in the future.</span></span>

## <a name="related-content"></a><span data-ttu-id="4c692-131">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="4c692-131">Related content</span></span>

[<span data-ttu-id="4c692-132">Définir la stratégie d'expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="4c692-132">Set the password expiration policy for your organization</span></span>](../manage/set-password-expiration-policy.md)

[<span data-ttu-id="4c692-133">Définir le mot de passe d'un utilisateur de façon à ce qu'il n'expire jamais</span><span class="sxs-lookup"><span data-stu-id="4c692-133">Set an individual user's password to never expire</span></span>](set-password-to-never-expire.md)

[<span data-ttu-id="4c692-134">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4c692-134">Microsoft 365 Business training videos</span></span>](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
