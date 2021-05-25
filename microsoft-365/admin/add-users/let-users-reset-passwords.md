---
title: Autoriser les utilisateurs à réinitialiser leurs mots de passe
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
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
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5bc3f460-13cc-48c0-abd6-b80bae72d04a
description: Découvrez comment définir une stratégie pour permettre aux utilisateurs de réinitialiser leur mot de passe à l’aide de l’outil de réinitialisation de mot de passe en libre-service.
ms.openlocfilehash: 81fbe1949b8d5e4a601411703d86165f95cc7b7f
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52634267"
---
# <a name="let-users-reset-their-own-passwords"></a><span data-ttu-id="9b954-103">Autoriser les utilisateurs à réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="9b954-103">Let users reset their own passwords</span></span>

<span data-ttu-id="9b954-104">En tant qu’administrateur Microsoft 365, vous pouvez laisser les utilisateurs utiliser l’outil de réinitialisation de mot de passe [libre-service](https://go.microsoft.com/fwlink/p/?LinkId=522677) afin de ne pas avoir à réinitialiser les mots de passe pour eux.</span><span class="sxs-lookup"><span data-stu-id="9b954-104">As the Microsoft 365 admin, you can let people use the [self-service password reset tool](https://go.microsoft.com/fwlink/p/?LinkId=522677) so you don't have to reset passwords for them.</span></span> <span data-ttu-id="9b954-105">Moins de travail pour vous !</span><span class="sxs-lookup"><span data-stu-id="9b954-105">Less work for you!</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="9b954-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="9b954-106">Before you begin</span></span>
  
- <span data-ttu-id="9b954-107">Vous obtenez la réinitialisation  du mot de passe en libre-service pour les utilisateurs du cloud gratuitement avec n’importe quel plan Microsoft 365 entreprise, éducation ou à but non lucratif.</span><span class="sxs-lookup"><span data-stu-id="9b954-107">You get self-service password reset for cloud users **free** with any Microsoft 365 business, education, or nonprofit paid plan.</span></span> <span data-ttu-id="9b954-108">Elle ne fonctionne pas avec la Microsoft 365 d’essai.</span><span class="sxs-lookup"><span data-stu-id="9b954-108">It doesn't work with Microsoft 365 trial.</span></span>

- <span data-ttu-id="9b954-p103">Elle utilise Azure. Vous bénéficierez automatiquement et **gratuitement** de cette fonction dans Azure lorsque vous effectuerez ces étapes. L'activation de la réinitialisation du mot de passe libre-service ne vous coûtera rien si vous n'utilisez aucune autre fonctionnalité Azure.</span><span class="sxs-lookup"><span data-stu-id="9b954-p103">It uses Azure. You'll automatically get this feature in Azure for **free** when you do these steps. It won't cost you anything to turn on self-service password reset if you don't use other Azure features.</span></span>

- <span data-ttu-id="9b954-112">**Si vous utilisez un active directory** local, les deux points ci-dessus ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="9b954-112">**If you're using an on-premises Active Directory**, the above two points don't apply.</span></span> <span data-ttu-id="9b954-113">Au lieu de cela, vous pouvez configurer cette fonctionnalité, mais elle nécessite un abonnement payant **à Azure AD Premium**.</span><span class="sxs-lookup"><span data-stu-id="9b954-113">Rather, you can set this up but **it requires a paid subscription to Azure AD Premium**.</span></span>

<span data-ttu-id="9b954-114">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="9b954-114">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="9b954-115">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9b954-115">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> [<span data-ttu-id="9b954-116">Qu’est-ce qu’un compte d’administrateur ?</span><span class="sxs-lookup"><span data-stu-id="9b954-116">What's an admin account?</span></span>](../../business-video/admin-center-overview.md)

<span data-ttu-id="9b954-117">Vous devez être administrateur général ou administrateur de [mot de](about-admin-roles.md) passe pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="9b954-117">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

## <a name="watch-let-users-reset-their-own-passwords"></a><span data-ttu-id="9b954-118">Regardez : laisser les utilisateurs réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="9b954-118">Watch: Let users reset their own passwords</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S]

<span data-ttu-id="9b954-119">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](../../business-video/index.yml).</span><span class="sxs-lookup"><span data-stu-id="9b954-119">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](../../business-video/index.yml).</span></span>

## <a name="steps-let-people-reset-their-own-passwords"></a><span data-ttu-id="9b954-120">Étapes : laisser les utilisateurs réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="9b954-120">Steps: Let people reset their own passwords</span></span>

<span data-ttu-id="9b954-121">Ces étapes activent la réinitialisation du mot de passe libre-service pour tout le monde dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="9b954-121">These steps turn on self-service password reset for everyone in your business.</span></span>

1. <span data-ttu-id="9b954-122">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration,</a>allez à la page **Paramètres**  >  **paramètres de l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="9b954-122">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a>, go to the **Settings** > **Org settings** page.</span></span>

2. <span data-ttu-id="9b954-123">En haut de la page **Paramètres de l’organisation,** sélectionnez l’onglet Sécurité **& confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="9b954-123">At the top of the **Org settings** page, select the **Security & Privacy** tab.</span></span>
  
3. <span data-ttu-id="9b954-124">Sélectionnez **Réinitialiser le mot de passe en libre-service.**</span><span class="sxs-lookup"><span data-stu-id="9b954-124">Select **Self-service Password Reset**.</span></span>

4. <span data-ttu-id="9b954-125">Sous **réinitialisation du mot** de passe en **libre-service, sélectionnez Go to the Azure portal to turn on self-service password reset**.</span><span class="sxs-lookup"><span data-stu-id="9b954-125">Under **Self-service password reset**, select **Go to the Azure portal to turn on self-service password reset**.</span></span>

5. <span data-ttu-id="9b954-126">Dans le volet de navigation de gauche, sélectionnez **Utilisateurs,** puis, dans le volet **Utilisateurs | Page Tous les utilisateurs,** sélectionnez **Réinitialiser le mot de passe.**</span><span class="sxs-lookup"><span data-stu-id="9b954-126">In the left navigation pane, select **Users**, and then, on the **Users | All users** page, select **Password reset**.</span></span>
  
6. <span data-ttu-id="9b954-127">Dans la page **Propriétés,** **sélectionnez Tout** pour l’activer pour tous les utilisateurs de votre entreprise, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="9b954-127">On the **Properties** page, select **All** to enable it for everyone in your business, and then select **Save**.</span></span>
  
7. <span data-ttu-id="9b954-128">Lorsque vos utilisateurs se connectent, ils sont invités à entrer des informations de contact supplémentaires qui les aideront à réinitialiser leur mot de passe à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="9b954-128">When your users sign in, they will be prompted to enter additional contact information that will help them reset their password in the future.</span></span>

## <a name="related-content"></a><span data-ttu-id="9b954-129">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="9b954-129">Related content</span></span>

<span data-ttu-id="9b954-130">[Définir la stratégie d’expiration de mot de passe pour votre organisation](../manage/set-password-expiration-policy.md) (article)</span><span class="sxs-lookup"><span data-stu-id="9b954-130">[Set the password expiration policy for your organization](../manage/set-password-expiration-policy.md) (article)</span></span>\
<span data-ttu-id="9b954-131">[Définir le mot de passe d’un utilisateur individuel pour qu’il n’expire jamais](set-password-to-never-expire.md) (article)</span><span class="sxs-lookup"><span data-stu-id="9b954-131">[Set an individual user's password to never expire](set-password-to-never-expire.md) (article)</span></span>\
<span data-ttu-id="9b954-132">[Microsoft 365 Business vidéos de formation](../../business-video/index.yml) (page de liens)</span><span class="sxs-lookup"><span data-stu-id="9b954-132">[Microsoft 365 Business training videos](../../business-video/index.yml) (link page)</span></span>
