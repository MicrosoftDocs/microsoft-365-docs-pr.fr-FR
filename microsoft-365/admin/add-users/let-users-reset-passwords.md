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
ms.openlocfilehash: beffbcac997806f0c13347dfba42a1ab0ec65c1d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43617145"
---
# <a name="let-users-reset-their-own-passwords"></a><span data-ttu-id="4cd24-103">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="4cd24-103">Let users reset their own passwords</span></span>

<span data-ttu-id="4cd24-104">Vous êtes inondé de demandes de réinitialisation de mots de passe ?</span><span class="sxs-lookup"><span data-stu-id="4cd24-104">Getting crushed with people asking you to reset their passwords?</span></span> <span data-ttu-id="4cd24-105">En tant qu’administrateur 365 de Microsoft, vous pouvez autoriser les utilisateurs à utiliser l' [outil de réinitialisation du mot de passe libre-service](https://go.microsoft.com/fwlink/p/?LinkId=522677) afin de ne pas avoir à réinitialiser leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4cd24-105">As the Microsoft 365 admin, you can let people use the [self-service password reset tool](https://go.microsoft.com/fwlink/p/?LinkId=522677) so you don't have to reset passwords for them.</span></span> <span data-ttu-id="4cd24-106">Moins de travail pour vous !</span><span class="sxs-lookup"><span data-stu-id="4cd24-106">Less work for you!</span></span> 
  
<span data-ttu-id="4cd24-107">Voici quelques informations à retenir :</span><span class="sxs-lookup"><span data-stu-id="4cd24-107">Here are a few things you need to know:</span></span>
  
- <span data-ttu-id="4cd24-108">Vous bénéficiez d’une réinitialisation du mot de passe en libre-service pour les utilisateurs du Cloud **gratuitement** avec les plans payants Microsoft 365 Business, Education ou imprévus.</span><span class="sxs-lookup"><span data-stu-id="4cd24-108">You get self-service password reset for cloud users **free** with any Microsoft 365 business, education, or nonprofit paid plan.</span></span> <span data-ttu-id="4cd24-109">Elle ne fonctionne pas avec la version d’évaluation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4cd24-109">It doesn't work with Microsoft 365 trial.</span></span> 
    
- <span data-ttu-id="4cd24-p103">Elle utilise Azure. Vous bénéficierez automatiquement et **gratuitement** de cette fonction dans Azure lorsque vous effectuerez ces étapes. L'activation de la réinitialisation du mot de passe libre-service ne vous coûtera rien si vous n'utilisez aucune autre fonctionnalité Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd24-p103">It uses Azure. You'll automatically get this feature in Azure for **free** when you do these steps. It won't cost you anything to turn on self-service password reset if you don't use other Azure features.</span></span> 
    
- <span data-ttu-id="4cd24-113">**Si vous utilisez un annuaire Active Directory local**, les deux points ci-dessus ne s’appliquent pas.</span><span class="sxs-lookup"><span data-stu-id="4cd24-113">**If you're using an on-premises Active Directory**, the above two points don't apply.</span></span> <span data-ttu-id="4cd24-114">Au lieu de cela, vous pouvez configurer cela, mais **il nécessite un abonnement payant à Azure ad Premium**.</span><span class="sxs-lookup"><span data-stu-id="4cd24-114">Rather, you can set this up but **it requires a paid subscription to Azure AD Premium**.</span></span> 

<span data-ttu-id="4cd24-115">Regardez une courte vidéo sur la façon de permettre aux utilisateurs de réinitialiser leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4cd24-115">Watch a short video about letting users reset their own passwords.</span></span> <br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3AY8S] 

<span data-ttu-id="4cd24-116">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span><span class="sxs-lookup"><span data-stu-id="4cd24-116">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span></span>

## <a name="let-people-reset-their-own-passwords"></a><span data-ttu-id="4cd24-117">Autoriser les utilisateurs à réinitialiser leur mot de passe</span><span class="sxs-lookup"><span data-stu-id="4cd24-117">Let people reset their own passwords</span></span> 

<span data-ttu-id="4cd24-118">Ces étapes activent la réinitialisation du mot de passe libre-service pour tout le monde dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4cd24-118">These steps turn on self-service password reset for everyone in your business.</span></span>
  
::: moniker range="o365-worldwide"
1.  <span data-ttu-id="4cd24-119">Dans le centre d’administration, accédez à la page **paramètres** \> de <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">sécurité & de confidentialité</a> .</span><span class="sxs-lookup"><span data-stu-id="4cd24-119">In the admin center, go to the **Settings** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2072756" target="_blank">Security & privacy</a> page.</span></span>

::: moniker-end

::: moniker range="o365-germany"

1. <span data-ttu-id="4cd24-120">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">Centre d’administration</a>, accédez à la page **paramètres** \> de confidentialité de la \*\*sécurité &amp; \*\* .</span><span class="sxs-lookup"><span data-stu-id="4cd24-120">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=848041" target="_blank">admin center</a>, go to the **Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

::: moniker range="o365-21vianet"

1. <span data-ttu-id="4cd24-121">Dans le <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">Centre d’administration</a>, accédez à la page **paramètres** \> de confidentialité de la \*\*sécurité &amp; \*\* .</span><span class="sxs-lookup"><span data-stu-id="4cd24-121">In the <a href="https://go.microsoft.com/fwlink/p/?linkid=850627" target="_blank">admin center</a>, go to the **Settings** \> **Security &amp; privacy** page.</span></span>

::: moniker-end

   
2. <span data-ttu-id="4cd24-122">Sous **permettre à vos personnes de réinitialiser leur mot de passe**, sélectionnez le lien pour le **Centre d’administration Azure ad**.</span><span class="sxs-lookup"><span data-stu-id="4cd24-122">Under **Let your people reset their own passwords**, select the link for the **Azure AD admin center**.</span></span> <span data-ttu-id="4cd24-123">Vous recevrez Azure gratuitement !</span><span class="sxs-lookup"><span data-stu-id="4cd24-123">You'll get Azure for free!</span></span>
  
3. <span data-ttu-id="4cd24-124">Sélectionnez **utilisateurs** dans le volet de navigation de gauche, puis **réinitialisation du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="4cd24-124">Select **Users** in the left navigation, and then select **Password reset**.</span></span>
  
4. <span data-ttu-id="4cd24-125">Sur la page Propriétés, sélectionnez **tous** pour l’activer pour tous les membres de votre entreprise, puis sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4cd24-125">On the Properties page, select **All** to enable it for everyone in your business, and then select **Save**.</span></span>
  
5. <span data-ttu-id="4cd24-126">Lorsque vos utilisateurs se connecteront à Office 365, ils seront invités à entrer des informations de contact supplémentaires qui leur permettront de réinitialiser leur mot de passe à l'avenir.</span><span class="sxs-lookup"><span data-stu-id="4cd24-126">When your users sign in to Office 365, they will be prompted to enter additional contact information that will help them reset their password in the future.</span></span>

## <a name="related-articles"></a><span data-ttu-id="4cd24-127">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4cd24-127">Related articles</span></span>

[<span data-ttu-id="4cd24-128">Définir la stratégie d'expiration des mots de passe pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="4cd24-128">Set the password expiration policy for your organization</span></span>](../manage/set-password-expiration-policy.md)
  
[<span data-ttu-id="4cd24-129">Définir le mot de passe d'un utilisateur de façon à ce qu'il n'expire jamais</span><span class="sxs-lookup"><span data-stu-id="4cd24-129">Set an individual user's password to never expire</span></span>](set-password-to-never-expire.md)

[<span data-ttu-id="4cd24-130">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4cd24-130">Microsoft 365 Business training videos</span></span>](https://support.office.com/article/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)