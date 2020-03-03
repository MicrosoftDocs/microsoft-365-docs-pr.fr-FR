---
title: Configurer l’authentification multifacteur pour les utilisateurs d’Office 365
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
description: Découvrez comment utiliser les paramètres par défaut de sécurité pour configurer multi-factor authentication pour les utilisateurs d’Office 365.
monikerRange: o365-worldwide
ms.openlocfilehash: 4dc52c25c3a9351be1a9f4d094d664bc4ed527f9
ms.sourcegitcommit: 812aab5f58eed4bf359faf0e99f7f876af5b1023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42361045"
---
# <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="78514-103">Configurer Multi-factor Authentification (MFA)</span><span class="sxs-lookup"><span data-stu-id="78514-103">Set up multi-factor authentication</span></span>
  
<span data-ttu-id="78514-104">Les paramètres de sécurité par défaut sont automatiquement activés avec tout nouvel abonnement Office 365 pour les entreprises ou Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="78514-104">Every new Office 365 for business or Microsoft 365 Business subscription will automatically have security defaults turned on.</span></span> <span data-ttu-id="78514-105">Chaque utilisateur doit ainsi configurer multi-factor authentication (MFA) et installer l’application de l’Authenticator sur son appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="78514-105">This means that every user will have to set up multi-factor authentication (MFA) and install the Authenticator app on their mobile device.</span></span> <span data-ttu-id="78514-106">Pour en savoir plus, voir [Configurer la vérification en deux étapes pour Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span><span class="sxs-lookup"><span data-stu-id="78514-106">For more information, see [Set up 2-step verification for Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span></span>  

<span data-ttu-id="78514-107">Les neuf rôles d’administrateur suivants sont nécessaires pour effectuer une authentification supplémentaire lorsqu’ils se connectent :</span><span class="sxs-lookup"><span data-stu-id="78514-107">The following nine administrator roles will be required to perform additional authentication every time they sign in:</span></span>
- <span data-ttu-id="78514-108">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="78514-108">Global administrator</span></span>
- <span data-ttu-id="78514-109">Administrateur SharePoint</span><span class="sxs-lookup"><span data-stu-id="78514-109">SharePoint administrator</span></span>
- <span data-ttu-id="78514-110">Administrateur Exchange</span><span class="sxs-lookup"><span data-stu-id="78514-110">Exchange administrator</span></span>
- <span data-ttu-id="78514-111">Administrateur de l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="78514-111">Conditional Access administrator</span></span>
- <span data-ttu-id="78514-112">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="78514-112">Security administrator</span></span>
- <span data-ttu-id="78514-113">Administrateur du support technique ou Administrateur de mot de passe</span><span class="sxs-lookup"><span data-stu-id="78514-113">Helpdesk administrator or password administrator</span></span>
- <span data-ttu-id="78514-114">Administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="78514-114">Billing administrator</span></span>
- <span data-ttu-id="78514-115">Administrateur d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78514-115">User administrator</span></span>
- <span data-ttu-id="78514-116">Administrateur d’authentification</span><span class="sxs-lookup"><span data-stu-id="78514-116">Authentication administrator</span></span>

<span data-ttu-id="78514-117">Tous les autres utilisateurs seront invités à effectuer une authentification supplémentaire si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="78514-117">All other users will be asked to perform additional authentication when needed.</span></span> <span data-ttu-id="78514-118">Pour plus d’informations, voir [Présentation des paramètres de sécurité par défaut](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span><span class="sxs-lookup"><span data-stu-id="78514-118">For more information, see [What are security defaults?](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span></span>

> [!NOTE]
> <span data-ttu-id="78514-p103">Vous devez être un administrateur général Office 365 pour configurer ou modifier Multi-Factor Authentification. </span><span class="sxs-lookup"><span data-stu-id="78514-p103">You must be an Office 365 global admin to set up or modify multi-factor authentication. </span></span><br><br>
> <span data-ttu-id="78514-120">Si le nouveau Centre d’administration Microsoft 365 n’est pas celui que vous utilisez, vous pouvez l’activer en sélectionnant le bouton bascule **Essayer le nouveau Centre d’administration** situé en haut de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="78514-120">If you're not using the new Microsoft 365 admin center, you can turn it on by selecting the **Try the new admin center** toggle located at the top of the Home page.</span></span>

<span data-ttu-id="78514-121">Si vous avez déjà configuré Multi-Factor Authentication avec des stratégies de référence, [vous devez les désactiver et activer les paramètres de sécurité par défaut](#move-from-baseline-policies-to-security-defaults).</span><span class="sxs-lookup"><span data-stu-id="78514-121">If you have previously set up MFA with baseline policies, [you must turn them off and turn on security defaults](#move-from-baseline-policies-to-security-defaults).</span></span> <span data-ttu-id="78514-122">Toutefois, si vous avez Microsoft 365 Entreprise ou si votre abonnement inclut [Azure Active Directory Premium 1 ou Azure Active Directory Premium 2](https://azure.microsoft.com/pricing/details/active-directory/), vous pouvez également configurer les stratégies d'[accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview).</span><span class="sxs-lookup"><span data-stu-id="78514-122">However, if you have Microsoft 365 Business or your subscription includes [Azure Active Directory Premium 1, or Azure Active Directory Premium 2](https://azure.microsoft.com/pricing/details/active-directory/), you can also set up [conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies.</span></span> <span data-ttu-id="78514-123">Pour utiliser les stratégies d’accès conditionnel, vous devez vous assurer que [l’authentification moderne est activée](#enable-multi-factor-authentication-for-your-organization).</span><span class="sxs-lookup"><span data-stu-id="78514-123">To use conditional access policies, you need to make sure [modern authentication is enabled](#enable-multi-factor-authentication-for-your-organization).</span></span>

## <a name="manage-security-defaults"></a><span data-ttu-id="78514-124">Gérer les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="78514-124">Manage security defaults</span></span>

1. <span data-ttu-id="78514-125">Connectez-vous au [centre d'administration](https://go.microsoft.com/fwlink/p/?linkid=834822) à l'aide de vos informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="78514-125">Sign in to [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822) with your Global admin credentials.</span></span>
2. <span data-ttu-id="78514-126">Accès à [Propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="78514-126">Go to [Azure Active Directory Properties](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span>

3. <span data-ttu-id="78514-127">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**.</span><span class="sxs-lookup"><span data-stu-id="78514-127">At the bottom of the page, choose **Manage Security defaults**.</span></span>
4. <span data-ttu-id="78514-128">Sélectionnez **Oui** pour activer les paramètres de sécurité par défaut et **Non** pour désactiver les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="78514-128">Choose **Yes** to enable security defaults and **No** to disable security defaults.</span></span>

## <a name="move-from-baseline-policies-to-security-defaults"></a><span data-ttu-id="78514-129">Basculez des stratégies de base aux paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="78514-129">Move from baseline policies to security defaults</span></span>

1. <span data-ttu-id="78514-130">Dans le [centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=834822), sélectionnez **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="78514-130">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), select **Setup**.</span></span>

2. <span data-ttu-id="78514-131">En regard de **Connexion et sécurité**, sous **Avoir une connexion plus sécurisée**, sélectionnez **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="78514-131">Next to **Sign-in and security**, under **Make sign-in more secure**, select **View**.</span></span>

3. <span data-ttu-id="78514-132">Sous **Rendre la connexion plus sécurisée**, sélectionnez **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="78514-132">Under **Make sign-in more secure**, select **Manage**.</span></span> 

4. <span data-ttu-id="78514-133">Sur la page des **Stratégies du Portail Microsoft Azure Conditional Access**, choisissez chaque stratégie de référence définie sur **Activée** et configurez-les sur **Désactivée**.</span><span class="sxs-lookup"><span data-stu-id="78514-133">On the **Azure portal Conditional Access - Policies** page,  choose each Baseline policy that is **On**, and set them to **Off**.</span></span>
5. <span data-ttu-id="78514-134">Accédez à la page [Propriétés d'Azure Active Directory](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span><span class="sxs-lookup"><span data-stu-id="78514-134">Go to [Azure Active Directory Properties](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties) page.</span></span>
6. <span data-ttu-id="78514-135">Au bas de la page, sélectionnez **Gérer les paramètres de sécurité par défaut**, et dans le volet **Activer les paramètres de sécurité par défaut**, définissez **Activer les paramètres de sécurité par défaut** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="78514-135">On the bottom of the page, choose **Manage Security defaults**, and in the **Enable Security defaults** pane, set **Enable Security defaults** toggle to **Yes**.</span></span> 

## <a name="enable-modern-authentication-for-your-organization"></a><span data-ttu-id="78514-136">Activer l’authentification moderne pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="78514-136">Enable Modern authentication for your organization</span></span>

<span data-ttu-id="78514-137">Les applications clientes Office 2016 prennent en charge l'authentification multifacteur via l'utilisation de la bibliothèque ADAL (Active Directory Authentication Library).</span><span class="sxs-lookup"><span data-stu-id="78514-137">All Office 2016 client applications support MFA through the use of the Active Directory Authentication Library (ADAL).</span></span> <span data-ttu-id="78514-138">Par conséquent, les mots de passe d'application ne sont pas requis pour les clients Office 2016.</span><span class="sxs-lookup"><span data-stu-id="78514-138">This means that app passwords aren't required for Office 2016 clients.</span></span> <span data-ttu-id="78514-139">Vous devez toutefois vous assurer que votre abonnement Office 365 est activé pour ADAL ou authentification moderne.</span><span class="sxs-lookup"><span data-stu-id="78514-139">However, you need to make sure your Office 365 subscription is enabled for ADAL, or modern authentication.</span></span>

1. <span data-ttu-id="78514-140">Pour activer l’authentification moderne, dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=834822), sélectionnez **Paramètres** \> **Paramètres**, puis dans l’onglet **Services**, choisissez **Authentification moderne** dans la liste.</span><span class="sxs-lookup"><span data-stu-id="78514-140">To enable modern authentication, from the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), select **Settings** \> **Settings** and then in the **Services** tab, choose **Modern authentication** from the list.</span></span>

2. <span data-ttu-id="78514-141">Cochez la case **Activer l’authentification moderne** dans le volet de l’**Authentification moderne**.</span><span class="sxs-lookup"><span data-stu-id="78514-141">Check the **Enable modern authentication** box in the **Modern authentication** panel.</span></span> 

    ![Panneau d’authentification moderne avec la case Activer cochée.](../../media/enablemodernauth.png)
    
## <a name="enable-multi-factor-authentication-for-your-organization"></a><span data-ttu-id="78514-143">Activer Azure Multi-Factor Authentification pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="78514-143">Enable multi-factor authentication for your organization</span></span>
    
1. <span data-ttu-id="78514-144">Dans le [Centre d’administration](https://go.microsoft.com/fwlink/p/?linkid=834822), sélectionnez **utilisateurs** et **utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="78514-144">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=834822), select **Users** and **Active Users**.</span></span>

2. <span data-ttu-id="78514-145">Dans la section **utilisateurs actifs** , cliquez sur **authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="78514-145">In the **Active Users** section, Click on  **multi-factor authentication**.</span></span>

3. <span data-ttu-id="78514-146">Sur la page **authentification multifacteur** , sélectionnez **utilisateur** si vous activez cette option pour un utilisateur ou sélectionnez **mise à jour en bloc** pour activer plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="78514-146">On the **Multi-factor authentication** page, select **user** if you are enabling this for one user or select **Bulk Update** to enable multiple users.</span></span>

4. <span data-ttu-id="78514-147">Cliquez sur **activer** sous **étapes rapides**.</span><span class="sxs-lookup"><span data-stu-id="78514-147">CLick on **Enable** under **Quick Steps**.</span></span>

5. <span data-ttu-id="78514-148">Dans la fenêtre contextuelle, cliquez sur **activer l’authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="78514-148">In the Pop-up window, Click on **Enable Multi-Factor Authentication**.</span></span>

<span data-ttu-id="78514-149">Une fois défini Multi-Factor Authentification pour votre organisation, vos utilisateurs doivent configurer la vérification en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="78514-149">After you set up multi-factor authentication for your organization, your users will be required to set up two-step verification on their devices.</span></span> <span data-ttu-id="78514-150">Pour en savoir plus, voir [Configurer la vérification en deux étapes pour Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span><span class="sxs-lookup"><span data-stu-id="78514-150">For more information, see [Set up 2-step verification for Office 365](https://support.office.com/article/ace1d096-61e5-449b-a875-58eb3d74de14).</span></span>
    
> [!TIP]
> <span data-ttu-id="78514-151">Pour expliquer la configuration de l’application Authenticator à vos utilisateurs, consultez [Utiliser Microsoft Authenticator avec Office 365](https://support.office.com/article/use-microsoft-authenticator-with-office-365-1412611f-ad8d-43ab-807c-7965e5155411?ui=en-US&rs=en-US&ad=US#ID0EAADAAA=_Step_1).</span><span class="sxs-lookup"><span data-stu-id="78514-151">To explain to your users how to set up the Authenticator app, please visit [Use Microsoft Authenticator with office 365](https://support.office.com/article/use-microsoft-authenticator-with-office-365-1412611f-ad8d-43ab-807c-7965e5155411?ui=en-US&rs=en-US&ad=US#ID0EAADAAA=_Step_1).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="78514-152">Depuis août 2017, tous les nouveaux clients Office 365 qui incluent Skype Entreprise Online et Exchange Online ont l’authentification moderne activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="78514-152">As of August of 2017, all new Office 365 tenants that include Skype for Business online and Exchange online have modern authentication enabled by default.</span></span> <span data-ttu-id="78514-153">Pour vérifier le statut de votre authentification moderne pour Skype Entreprise Online, vous pouvez utiliser PowerShell Skype Entreprise Online avec les informations d’identification d’Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="78514-153">To check your modern authentication status for Skype for Business online, you can use Skype for Business online PowerShell with Global Admin credentials.</span></span> <span data-ttu-id="78514-154">Exécutez Get-CsOAuthConfiguration pour vérifier la sortie de-ClientADALAuthOverride.</span><span class="sxs-lookup"><span data-stu-id="78514-154">Run Get-CsOAuthConfiguration to check the output of -ClientADALAuthOverride.</span></span> <span data-ttu-id="78514-155">Si-ClientADALAuthOverride est « Autorisé », votre authentification moderne est activée.</span><span class="sxs-lookup"><span data-stu-id="78514-155">If -ClientADALAuthOverride is 'Allowed', modern authentication is on.</span></span>
<span data-ttu-id="78514-156">Pour vérifier l’état de votre MA pour Exchange Online, consultez [Activer l’authentification moderne dans Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).</span><span class="sxs-lookup"><span data-stu-id="78514-156">To check your MA status for Exchange Online, please visit [Enable modern authentication in Exchange Online](https://docs.microsoft.com/exchange/clients-and-mobile-in-exchange-online/enable-or-disable-modern-authentication-in-exchange-online).</span></span>

## <a name="related-articles"></a><span data-ttu-id="78514-157">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="78514-157">Related articles</span></span>

[<span data-ttu-id="78514-158">10 principales méthodes pour sécuriser les offres Office 365 et Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="78514-158">Top 10 ways to secure Office 365 and Microsoft 365 Business plans</span></span>](secure-your-business-data.md)

[<span data-ttu-id="78514-159">Activer l’Authentification moderne pour Office 2013 sur les appareils Windows</span><span class="sxs-lookup"><span data-stu-id="78514-159">Enable Modern Authentication for Office 2013 on Windows devices</span></span>](enable-modern-authentication.md)
