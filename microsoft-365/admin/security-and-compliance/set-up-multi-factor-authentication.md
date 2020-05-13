---
title: Configurer l'authentification multifacteur pour les utilisateurs
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: mnirkhe
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
search.appverid:
- BCS160
- MET150
- MOE150
- BEA160
- GEA150
ms.assetid: 8f0454b2-f51a-4d9c-bcde-2c48e41621c6
description: Découvrez comment utiliser les paramètres de sécurité par défaut pour configurer l’authentification multifacteur pour les utilisateurs.
monikerRange: o365-worldwide
ms.openlocfilehash: 4c0df9198db8154c1aa748a68eff29dd9bf3bca1
ms.sourcegitcommit: 8e655c6cbb91bfb97efda9a99c39fac33eaa974a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "44213009"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="6054f-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="6054f-103">Set up multi-factor authentication</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6054f-104">Si vous avez acheté votre abonnement ou une version d’évaluation après le 21 octobre 2019, et que vous êtes invité de manière inattendue à utiliser l’authentification multifacteur (MFA), les [paramètres par défaut de sécurité](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) ont été automatiquement activés pour votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="6054f-104">If you purchased your subscription or trial after October 21, 2019, and you're unexpectedly prompted for multi-factor authentication (MFA), [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) have been automatically enabled for your subscription.</span></span>

<span data-ttu-id="6054f-105">Tous les nouveaux abonnements Microsoft 365 auront automatiquement des [paramètres de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) activés.</span><span class="sxs-lookup"><span data-stu-id="6054f-105">Every new Microsoft 365 subscription will automatically have [security defaults](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults) turned on.</span></span> <span data-ttu-id="6054f-106">Cela signifie que chaque utilisateur devra configurer l’authentification multifacteur (MFA) et installer l’application Microsoft Authenticator sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="6054f-106">This means that every user will have to set up multi-factor authentication (MFA) and install the Microsoft Authenticator app on their mobile device.</span></span> <span data-ttu-id="6054f-107">Pour plus d’informations, consultez [la rubrique Configurer l’authentification multifacteur pour un compte Microsoft 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span><span class="sxs-lookup"><span data-stu-id="6054f-107">For more information, see [Set up MFA for a Microsoft 365 account](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span></span>

<span data-ttu-id="6054f-108">Les neuf rôles d’administrateur suivants sont nécessaires pour effectuer une authentification supplémentaire lorsqu’ils se connectent :</span><span class="sxs-lookup"><span data-stu-id="6054f-108">The following nine administrator roles will be required to perform additional authentication every time they sign in:</span></span>

- <span data-ttu-id="6054f-109">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="6054f-109">Global administrator</span></span>
- <span data-ttu-id="6054f-110">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="6054f-110">SharePoint administrator</span></span>
- <span data-ttu-id="6054f-111">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="6054f-111">Exchange administrator</span></span>
- <span data-ttu-id="6054f-112">Administrateur de l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="6054f-112">Conditional Access administrator</span></span>
- <span data-ttu-id="6054f-113">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="6054f-113">Security administrator</span></span>
- <span data-ttu-id="6054f-114">Administrateur du support technique ou Administrateur de mot de passe</span><span class="sxs-lookup"><span data-stu-id="6054f-114">Helpdesk administrator or password administrator</span></span>
- <span data-ttu-id="6054f-115">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="6054f-115">Billing administrator</span></span>
- <span data-ttu-id="6054f-116">Administrateur d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6054f-116">User administrator</span></span>
- <span data-ttu-id="6054f-117">Administrateur d’authentification</span><span class="sxs-lookup"><span data-stu-id="6054f-117">Authentication administrator</span></span>

<span data-ttu-id="6054f-118">Tous les autres utilisateurs seront invités à effectuer une authentification supplémentaire si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6054f-118">All other users will be asked to perform additional authentication when needed.</span></span>

> [!NOTE]
> <span data-ttu-id="6054f-119">Vous devez être un administrateur général pour configurer ou modifier l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="6054f-119">You must be a global admin to set up or modify MFA</span></span> <br><br>
> <span data-ttu-id="6054f-120">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="6054f-120">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

<span data-ttu-id="6054f-121">Si vous avez déjà configuré MFA avec des stratégies de base, [vous devez les désactiver pour activer les paramètres de sécurité par défaut](#move-from-baseline-policies-to-security-defaults).</span><span class="sxs-lookup"><span data-stu-id="6054f-121">If you have previously set up MFA with baseline policies, [you must turn them off to turn on security defaults](#move-from-baseline-policies-to-security-defaults).</span></span> <span data-ttu-id="6054f-122">Toutefois, si vous avez Microsoft 365 Business ou que votre abonnement inclut [Azure Active Directory Premium P1 ou Azure Active Directory Premium P2](https://azure.microsoft.com/pricing/details/active-directory/), vous pouvez également configurer des stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) .</span><span class="sxs-lookup"><span data-stu-id="6054f-122">However, if you have Microsoft 365 Business or your subscription includes [Azure Active Directory Premium P1 or Azure Active Directory Premium P2](https://azure.microsoft.com/pricing/details/active-directory/), you can also set up [Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies.</span></span> <span data-ttu-id="6054f-123">Pour utiliser des stratégies d’accès conditionnel, vous devez vous assurer que les paramètres de sécurité par défaut sont désactivés et que [l’authentification moderne](#enable-modern-authentication-for-your-organization) est activée.</span><span class="sxs-lookup"><span data-stu-id="6054f-123">To use Conditional Access policies, you need to make sure security defaults are disabled and [modern authentication](#enable-modern-authentication-for-your-organization) is enabled.</span></span>

> [!TIP]
> <span data-ttu-id="6054f-124">Pour expliquer à vos utilisateurs comment configurer l’application Microsoft Authenticator, consultez la rubrique [utiliser Microsoft Authenticator avec Office 365](https://support.office.com/article/use-microsoft-authenticator-with-office-365-1412611f-ad8d-43ab-807c-7965e5155411).</span><span class="sxs-lookup"><span data-stu-id="6054f-124">To explain to your users how to set up the Microsoft Authenticator app, see [Use Microsoft Authenticator with Office 365](https://support.office.com/article/use-microsoft-authenticator-with-office-365-1412611f-ad8d-43ab-807c-7965e5155411).</span></span>

## <a name="manage-security-defaults"></a><span data-ttu-id="6054f-125">Gérer les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="6054f-125">Manage security defaults</span></span>

1. <span data-ttu-id="6054f-126">Connectez-vous au [Centre d'administration](https://go.microsoft.com/fwlink/p/?linkid=834822) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="6054f-126">Sign in to the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822) with global admin credentials.</span></span>
2. <span data-ttu-id="6054f-127">Accédez à la [page Propriétés Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="6054f-127">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
3. <span data-ttu-id="6054f-128">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6054f-128">At the bottom of the page, choose **Manage Security defaults**.</span></span>
4. <span data-ttu-id="6054f-129">Choisissez **Oui** pour activer les paramètres de sécurité par défaut et **non** pour désactiver les paramètres de sécurité par défaut, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6054f-129">Choose **Yes** to enable security defaults and **No** to disable security defaults, and then choose **Save**.</span></span>

## <a name="move-from-baseline-policies-to-security-defaults"></a><span data-ttu-id="6054f-130">Basculez des stratégies de base aux paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="6054f-130">Move from baseline policies to security defaults</span></span>

1. <span data-ttu-id="6054f-131">Accédez à la [page des stratégies d’accès conditionnel](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span><span class="sxs-lookup"><span data-stu-id="6054f-131">Go to the [Conditional Access - Policies page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).</span></span>
2. <span data-ttu-id="6054f-132">Choisissez chaque stratégie de planification qui est **activée** et définissez **activer la stratégie** sur **désactivé**.</span><span class="sxs-lookup"><span data-stu-id="6054f-132">Choose each baseline policy that is **On** and set **Enable policy** to **Off**.</span></span>
3. <span data-ttu-id="6054f-133">Accédez à la [page Propriétés Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="6054f-133">Go to the [Azure Active Directory - Properties page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>
4. <span data-ttu-id="6054f-134">En bas de la page, choisissez **gérer les paramètres de sécurité par défaut**, puis dans le volet **activer les paramètres de sécurité par défaut** , définissez activer les **paramètres** de sécurité par défaut sur **Oui**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6054f-134">On the bottom of the page, choose **Manage Security defaults**, and in the **Enable Security defaults** pane, set **Enable Security defaults** toggle to **Yes**, and then choose **Save**.</span></span> 

## <a name="enable-modern-authentication-for-your-organization"></a><span data-ttu-id="6054f-135">Activer l’authentification moderne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="6054f-135">Enable modern authentication for your organization</span></span>

<span data-ttu-id="6054f-136">Les applications clientes Office 2016 prennent en charge l'authentification multifacteur via l'utilisation de la bibliothèque ADAL (Active Directory Authentication Library).</span><span class="sxs-lookup"><span data-stu-id="6054f-136">All Office 2016 client applications support MFA through the use of the Active Directory Authentication Library (ADAL).</span></span> <span data-ttu-id="6054f-137">Par conséquent, les mots de passe d'application ne sont pas requis pour les clients Office 2016.</span><span class="sxs-lookup"><span data-stu-id="6054f-137">This means that app passwords aren't required for Office 2016 clients.</span></span> <span data-ttu-id="6054f-138">Pour plus d’informations, consultez [cet article](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings#app-passwords) .</span><span class="sxs-lookup"><span data-stu-id="6054f-138">See [this article](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-mfasettings#app-passwords) for more information.</span></span>

<span data-ttu-id="6054f-139">Toutefois, vous devez vous assurer que votre abonnement Microsoft 365 est activé pour ADAL ou l’authentification moderne.</span><span class="sxs-lookup"><span data-stu-id="6054f-139">However, you need to make sure your Microsoft 365 subscription is enabled for ADAL, or modern authentication.</span></span>

1. <span data-ttu-id="6054f-140">Pour activer l’authentification moderne, dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=834822), sélectionnez **Paramètres** \> **Paramètres**, puis dans l’onglet **Services**, choisissez **Authentification moderne** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="6054f-140">To enable modern authentication, from the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), select **Settings** \> **Settings** and then in the **Services** tab, choose **Modern authentication** from the list.</span></span>

2. <span data-ttu-id="6054f-141">Activez la case à cocher **activer l’authentification moderne (recommandé)** dans le panneau **authentification moderne** , puis choisissez **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="6054f-141">Check the **Enable modern authentication (recommended)** box in the **Modern authentication** panel, and then choose **Save changes**.</span></span> 

    ![Panneau d’authentification moderne avec la case Activer cochée.](../../media/enablemodernauth.png)
    
> [!IMPORTANT]
> <span data-ttu-id="6054f-143">À compter d’août 2017, tous les nouveaux abonnements Microsoft 365 qui incluent Skype entreprise Online et Exchange Online sont activés pour l’authentification moderne par défaut.</span><span class="sxs-lookup"><span data-stu-id="6054f-143">As of August of 2017, all new Microsoft 365 subscriptions that include Skype for Business online and Exchange online have modern authentication enabled by default.</span></span> <span data-ttu-id="6054f-144">Pour vérifier le statut de votre authentification moderne pour Skype Entreprise Online, vous pouvez utiliser PowerShell Skype Entreprise Online avec les informations d’identification d’Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="6054f-144">To check your modern authentication status for Skype for Business online, you can use Skype for Business online PowerShell with Global Admin credentials.</span></span> <span data-ttu-id="6054f-145">Exécutez Get-CsOAuthConfiguration pour vérifier la sortie de-ClientADALAuthOverride.</span><span class="sxs-lookup"><span data-stu-id="6054f-145">Run Get-CsOAuthConfiguration to check the output of -ClientADALAuthOverride.</span></span> <span data-ttu-id="6054f-146">Si-ClientADALAuthOverride est « Autorisé », votre authentification moderne est activée.</span><span class="sxs-lookup"><span data-stu-id="6054f-146">If -ClientADALAuthOverride is 'Allowed', modern authentication is on.</span></span>
<span data-ttu-id="6054f-147">Pour vérifier l’état de votre MA pour Exchange Online, consultez [Activer l’authentification moderne dans Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).</span><span class="sxs-lookup"><span data-stu-id="6054f-147">To check your MA status for Exchange Online, please visit [Enable modern authentication in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).</span></span>

## <a name="related-articles"></a><span data-ttu-id="6054f-148">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6054f-148">Related articles</span></span>

[<span data-ttu-id="6054f-149">10 façons de sécuriser les offres Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="6054f-149">Top 10 ways to secure Microsoft 365 for business plans</span></span>](secure-your-business-data.md)

[<span data-ttu-id="6054f-150">Activer l’Authentification moderne pour Office 2013 sur les appareils Windows</span><span class="sxs-lookup"><span data-stu-id="6054f-150">Enable Modern Authentication for Office 2013 on Windows devices</span></span>](enable-modern-authentication.md)
