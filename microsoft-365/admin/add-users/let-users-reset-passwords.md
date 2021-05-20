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
description: Découvrez comment définir une stratégie pour permettre aux utilisateurs de réinitialiser leurs propres mots de passe à l’aide de l’outil de réinitialisation de mot de passe libre-service.
ms.openlocfilehash: 2c79d5611ab2db00f4de5f227b0ec2f411955558
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52571852"
---
# <a name="let-users-reset-their-own-passwords"></a><span data-ttu-id="b1c08-103">Autoriser les utilisateurs à réinitialiser leurs mots de passe</span><span class="sxs-lookup"><span data-stu-id="b1c08-103">Let users reset their own passwords</span></span>

<span data-ttu-id="b1c08-104">En tant qu Microsoft 365 administrateur, vous pouvez laisser les gens utiliser [l’outil de réinitialisation de mot de passe libre-service](https://go.microsoft.com/fwlink/p/?LinkId=522677) afin que vous n’avez pas à réinitialiser les mots de passe pour eux.</span><span class="sxs-lookup"><span data-stu-id="b1c08-104">As the Microsoft 365 admin, you can let people use the [self-service password reset tool](https://go.microsoft.com/fwlink/p/?LinkId=522677) so you don't have to reset passwords for them.</span></span> <span data-ttu-id="b1c08-105">Moins de travail pour vous !</span><span class="sxs-lookup"><span data-stu-id="b1c08-105">Less work for you!</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="b1c08-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b1c08-106">Before you begin</span></span>
  
- <span data-ttu-id="b1c08-107">Vous obtenez la réinitialisation gratuite du mot de passe libre-service pour les **utilisateurs** du cloud avec n’importe quel Microsoft 365, de l’éducation ou du plan payant à but non lucratif.</span><span class="sxs-lookup"><span data-stu-id="b1c08-107">You get self-service password reset for cloud users **free** with any Microsoft 365 business, education, or nonprofit paid plan.</span></span> <span data-ttu-id="b1c08-108">Ça ne marche pas avec Microsoft 365 procès.</span><span class="sxs-lookup"><span data-stu-id="b1c08-108">It doesn't work with Microsoft 365 trial.</span></span>

- <span data-ttu-id="b1c08-p103">Elle utilise Azure. Vous bénéficierez automatiquement et **gratuitement** de cette fonction dans Azure lorsque vous effectuerez ces étapes. L'activation de la réinitialisation du mot de passe libre-service ne vous coûtera rien si vous n'utilisez aucune autre fonctionnalité Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c08-p103">It uses Azure. You'll automatically get this feature in Azure for **free** when you do these steps. It won't cost you anything to turn on self-service password reset if you don't use other Azure features.</span></span>

- <span data-ttu-id="b1c08-112">**Si vous utilisez un répertoire actif sur place, les deux** points ci-dessus ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="b1c08-112">**If you're using an on-premises Active Directory**, the above two points don't apply.</span></span> <span data-ttu-id="b1c08-113">Au contraire, vous pouvez configurer **cela, mais il nécessite un abonnement payant à Azure AD Premium**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-113">Rather, you can set this up but **it requires a paid subscription to Azure AD Premium**.</span></span>

<span data-ttu-id="b1c08-114">Cet article s’adresse aux personnes responsables de la stratégie d’expiration des mots de passe au sein d’une entreprise, d’une école ou d’une association.</span><span class="sxs-lookup"><span data-stu-id="b1c08-114">This article is for people who set password expiration policy for a business, school, or nonprofit.</span></span> <span data-ttu-id="b1c08-115">Pour effectuer ces étapes, vous devez vous connecter avec votre compte d’administrateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b1c08-115">To complete these steps, you need to sign in with your Microsoft 365 admin account.</span></span> [<span data-ttu-id="b1c08-116">Qu’est-ce qu’un compte admin ?</span><span class="sxs-lookup"><span data-stu-id="b1c08-116">What's an admin account?</span></span>](../../business-video/admin-center-overview.md)

<span data-ttu-id="b1c08-117">Vous devez être un administrateur [global ou un administrateur de mot de](about-admin-roles.md) passe pour effectuer ces étapes.</span><span class="sxs-lookup"><span data-stu-id="b1c08-117">You must be an [global admin or password administrator](about-admin-roles.md) to perform these steps.</span></span>

## <a name="watch-let-users-reset-their-own-passwords"></a><span data-ttu-id="b1c08-118">Regarder: Laissez les utilisateurs réinitialiser leurs propres mots de passe</span><span class="sxs-lookup"><span data-stu-id="b1c08-118">Watch: Let users reset their own passwords</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S]

<span data-ttu-id="b1c08-119">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](../../business-video/index.yml).</span><span class="sxs-lookup"><span data-stu-id="b1c08-119">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](../../business-video/index.yml).</span></span>

## <a name="steps-let-people-reset-their-own-passwords"></a><span data-ttu-id="b1c08-120">Étapes : Laissez les gens réinitialiser leurs propres mots de passe</span><span class="sxs-lookup"><span data-stu-id="b1c08-120">Steps: Let people reset their own passwords</span></span>

<span data-ttu-id="b1c08-121">Ces étapes activent la réinitialisation du mot de passe libre-service pour tout le monde dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="b1c08-121">These steps turn on self-service password reset for everyone in your business.</span></span>

1. <span data-ttu-id="b1c08-122">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">centre admin</a>, allez à la page **Paramètres paramètres**  >  **Org.**</span><span class="sxs-lookup"><span data-stu-id="b1c08-122">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">admin center</a>, go to the **Settings** > **Org settings** page.</span></span>

2. <span data-ttu-id="b1c08-123">En haut de la page **paramètres Org,** sélectionnez l’onglet **Sécurité & confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="b1c08-123">At the top of the **Org settings** page, select the **Security & Privacy** tab.</span></span>
  
3. <span data-ttu-id="b1c08-124">Sélectionnez **Réinitialisation de mot de passe libre-service**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-124">Select **Self-service Password Reset**.</span></span>

4. <span data-ttu-id="b1c08-125">Dans le **cadre de la réinitialisation du mot de passe libre-service,** **sélectionnez Rendez-vous sur le portail Azure pour activer la réinitialisation de mot de passe libre-service.**</span><span class="sxs-lookup"><span data-stu-id="b1c08-125">Under **Self-service password reset**, select **Go to the Azure portal to turn on self-service password reset**.</span></span>

5. <span data-ttu-id="b1c08-126">Dans le volet de navigation gauche, **sélectionnez Utilisateurs,** puis, sur les **utilisateurs | Toutes les pages utilisateurs,** sélectionnez **Mot de passe réinitialiser**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-126">In the left navigation pane, select **Users**, and then, on the **Users | All users** page, select **Password reset**.</span></span>
  
6. <span data-ttu-id="b1c08-127">Sur la page **Propriétés,** sélectionnez **Tous pour** l’activer pour tous les membres de votre entreprise, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-127">On the **Properties** page, select **All** to enable it for everyone in your business, and then select **Save**.</span></span>
  
7. <span data-ttu-id="b1c08-128">Lorsque vos utilisateurs se connectent, ils seront invités à saisir des coordonnées supplémentaires qui les aideront à réinitialiser leur mot de passe à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="b1c08-128">When your users sign in, they will be prompted to enter additional contact information that will help them reset their password in the future.</span></span>

## <a name="related-content"></a><span data-ttu-id="b1c08-129">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="b1c08-129">Related content</span></span>

<span data-ttu-id="b1c08-130">[Définir la stratégie d’expiration du mot de passe pour votre](../manage/set-password-expiration-policy.md) organisation (article)</span><span class="sxs-lookup"><span data-stu-id="b1c08-130">[Set the password expiration policy for your organization](../manage/set-password-expiration-policy.md) (article)</span></span>

<span data-ttu-id="b1c08-131">[Définir le mot de passe d’un utilisateur de façon à ce qu’il n’expire jamais](set-password-to-never-expire.md) (article)</span><span class="sxs-lookup"><span data-stu-id="b1c08-131">[Set an individual user's password to never expire](set-password-to-never-expire.md) (article)</span></span>

<span data-ttu-id="b1c08-132">[Microsoft 365 Business de formation (page](../../business-video/index.yml) lien)</span><span class="sxs-lookup"><span data-stu-id="b1c08-132">[Microsoft 365 Business training videos](../../business-video/index.yml) (link page)</span></span>
