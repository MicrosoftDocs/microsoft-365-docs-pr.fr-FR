---
title: Autoriser les utilisateurs à réinitialiser leur mot de passe
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
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 5bc3f460-13cc-48c0-abd6-b80bae72d04a
description: Découvrez comment réinitialiser vos mots de passe à l’aide de l’outil de réinitialisation du mot de passe libre-service.
ms.openlocfilehash: 01099f6f678bbaa3b163ac59e0417614352e0e97
ms.sourcegitcommit: 614666afb104fc97acb4a2ee5577ef63c0de153a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2020
ms.locfileid: "44173529"
---
# <a name="let-users-reset-their-own-passwords"></a><span data-ttu-id="a6ef4-103">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="a6ef4-103">Let users reset their own passwords</span></span>

<span data-ttu-id="a6ef4-104">Vous êtes inondé de demandes de réinitialisation de mots de passe ?</span><span class="sxs-lookup"><span data-stu-id="a6ef4-104">Getting crushed with people asking you to reset their passwords?</span></span> <span data-ttu-id="a6ef4-105">En tant qu’administrateur 365 de Microsoft, vous pouvez autoriser les utilisateurs à utiliser l' [outil de réinitialisation du mot de passe libre-service](https://go.microsoft.com/fwlink/p/?LinkId=522677) afin de ne pas avoir à réinitialiser leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-105">As the Microsoft 365 admin, you can let people use the [self-service password reset tool](https://go.microsoft.com/fwlink/p/?LinkId=522677) so you don't have to reset passwords for them.</span></span> <span data-ttu-id="a6ef4-106">Moins de travail pour vous !</span><span class="sxs-lookup"><span data-stu-id="a6ef4-106">Less work for you!</span></span> 
  
<span data-ttu-id="a6ef4-107">Voici quelques informations à retenir :</span><span class="sxs-lookup"><span data-stu-id="a6ef4-107">Here are a few things you need to know:</span></span>
  
- <span data-ttu-id="a6ef4-108">Vous bénéficiez d’une réinitialisation du mot de passe en libre-service pour les utilisateurs du Cloud **gratuitement** avec les plans payants Microsoft 365 Business, Education ou imprévus.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-108">You get self-service password reset for cloud users **free** with any Microsoft 365 business, education, or nonprofit paid plan.</span></span> <span data-ttu-id="a6ef4-109">Elle ne fonctionne pas avec la version d’évaluation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-109">It doesn't work with Microsoft 365 trial.</span></span> 
    
- <span data-ttu-id="a6ef4-p103">Elle utilise Azure. Vous bénéficierez automatiquement et **gratuitement** de cette fonction dans Azure lorsque vous effectuerez ces étapes. L'activation de la réinitialisation du mot de passe libre-service ne vous coûtera rien si vous n'utilisez aucune autre fonctionnalité Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-p103">It uses Azure. You'll automatically get this feature in Azure for **free** when you do these steps. It won't cost you anything to turn on self-service password reset if you don't use other Azure features.</span></span> 
    
- <span data-ttu-id="a6ef4-113">**Si vous utilisez un annuaire Active Directory local**, les deux points ci-dessus ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-113">**If you're using an on-premises Active Directory**, the above two points don't apply.</span></span> <span data-ttu-id="a6ef4-114">Au lieu de cela, vous pouvez configurer cela, mais **il nécessite un abonnement payant à Azure ad Premium**.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-114">Rather, you can set this up but **it requires a paid subscription to Azure AD Premium**.</span></span> 

<span data-ttu-id="a6ef4-115">Regardez une courte vidéo sur la façon de permettre aux utilisateurs de réinitialiser leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-115">Watch a short video about letting users reset their own passwords.</span></span> <br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S] 

<span data-ttu-id="a6ef4-116">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span><span class="sxs-lookup"><span data-stu-id="a6ef4-116">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span></span>

## <a name="let-people-reset-their-own-passwords"></a><span data-ttu-id="a6ef4-117">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="a6ef4-117">Let people reset their own passwords</span></span> 

<span data-ttu-id="a6ef4-118">Ces étapes activent la réinitialisation du mot de passe libre-service pour tout le monde dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-118">These steps turn on self-service password reset for everyone in your business.</span></span>
  
::: moniker range="o365-worldwide"
1. <span data-ttu-id="a6ef4-119">Dans le centre d’administration, accédez à la page <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">paramètres</a> des **paramètres** \> .</span><span class="sxs-lookup"><span data-stu-id="a6ef4-119">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Settings</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="a6ef4-120">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **paramètres** \> de confidentialité de la \*\*sécurité &amp; \*\* .</span><span class="sxs-lookup"><span data-stu-id="a6ef4-120">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="a6ef4-121">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page \*\*confidentialité &amp; \*\* de la sécurité **des paramètres de** \> **paramètres** \>.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-121">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Settings** \>**Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

   
2. <span data-ttu-id="a6ef4-122">En haut de la page Paramètres, sélectionnez **sécurité & confidentialité**.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-122">At the top of the Settings page select **Security & Privacy**.</span></span>
  
3. <span data-ttu-id="a6ef4-123">Sélectionnez **réinitialisation du mot de passe libre-service**.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-123">Select **Self Service Password Reset**.</span></span>
  
4. <span data-ttu-id="a6ef4-124">Sur la page Propriétés, sélectionnez **tous** pour l’activer pour tous les membres de votre entreprise, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-124">On the Properties page, select **All** to enable it for everyone in your business, and then select **Save**.</span></span>
  
5. <span data-ttu-id="a6ef4-125">Lorsque les utilisateurs se connectent, ils sont invités à entrer des informations de contact supplémentaires qui les aideront à réinitialiser leur mot de passe à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="a6ef4-125">When your users sign in, they will be prompted to enter additional contact information that will help them reset their password in the future.</span></span>

## <a name="related-articles"></a><span data-ttu-id="a6ef4-126">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="a6ef4-126">Related articles</span></span>

[<span data-ttu-id="a6ef4-127">Définir la stratégie d'expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="a6ef4-127">Set the password expiration policy for your organization</span></span>](../manage/set-password-expiration-policy.md)
  
[<span data-ttu-id="a6ef4-128">Définir le mot de passe d'un utilisateur de façon à ce qu'il n'expire jamais</span><span class="sxs-lookup"><span data-stu-id="a6ef4-128">Set an individual user's password to never expire</span></span>](set-password-to-never-expire.md)

[<span data-ttu-id="a6ef4-129">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="a6ef4-129">Microsoft 365 Business training videos</span></span>](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)
