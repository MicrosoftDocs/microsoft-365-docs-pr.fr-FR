---
title: Activer les paramètres de sécurité par défaut
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
manager: scotv
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
- M365-Campaigns
- m365solution-smb
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment les paramètres de sécurité par défaut peuvent aider à protéger votre organisation contre les attaques liées aux identités en fournissant des paramètres de sécurité préconfigurés.
ms.openlocfilehash: ea36ba45af26a767b08ee1e75931dca54dacea64
ms.sourcegitcommit: c5d1528559953c6db7dca1d5cb453e0aa3215f02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "51398290"
---
# <a name="turn-on-security-defaults"></a><span data-ttu-id="47cbb-103">Activer les paramètres de sécurité par défaut</span><span class="sxs-lookup"><span data-stu-id="47cbb-103">Turn on security defaults</span></span>

<span data-ttu-id="47cbb-104">Les paramètres de sécurité par défaut contribuent à protéger votre organisation contre les attaques liées aux identités en fournissant des paramètres de sécurité préconfigurés que Microsoft gère au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="47cbb-104">Security defaults help protect your organization from identity-related attacks by providing preconfigured security settings that Microsoft manages on behalf of your organization.</span></span> <span data-ttu-id="47cbb-105">Ces paramètres incluent l’activation de l’authentification multifacteur (MFA) pour tous les administrateurs et comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="47cbb-105">These settings include enabling multi-factor authentication (MFA) for all admins and user accounts.</span></span> <span data-ttu-id="47cbb-106">Pour la plupart des organisations, les paramètres de sécurité par défaut offrent un bon niveau de sécurité de la signature supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="47cbb-106">For most organizations, security defaults offer a good level of additional sign-in security.</span></span>

<span data-ttu-id="47cbb-107">Pour plus d’informations sur les paramètres de sécurité par défaut et les stratégies qu’ils appliquent, voir [Quelles sont les valeurs par défaut de sécurité ?](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span><span class="sxs-lookup"><span data-stu-id="47cbb-107">For more information about security defaults and the policies they enforce, see [What are security defaults?](/azure/active-directory/fundamentals/concept-fundamentals-security-defaults)</span></span>

<span data-ttu-id="47cbb-108">Si votre abonnement a été créé le 22 octobre 2019 ou après, les paramètres de sécurité par défaut ont peut-être été automatiquement activés pour vous, vous devez vérifier vos paramètres pour &mdash; vérifier.</span><span class="sxs-lookup"><span data-stu-id="47cbb-108">If your subscription was created on or after October 22, 2019, security defaults might have been automatically enabled for you&mdash;you should check your settings to confirm.</span></span>

<span data-ttu-id="47cbb-109">Pour activer les paramètres de sécurité par défaut dans azure Active Directory (Azure AD) ou pour vérifier s’ils sont déjà activés :</span><span class="sxs-lookup"><span data-stu-id="47cbb-109">To enable security defaults in your Azure Active Directory (Azure AD) or to check to see if they're already enabled:</span></span>

1. <span data-ttu-id="47cbb-110">Connectez-vous au <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Centre d’administration Microsoft 365</a> avec les informations d’identification d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="47cbb-110">Sign in to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">Microsoft 365 admin center</a> with Global admin credentials.</span></span>

2. <span data-ttu-id="47cbb-111">Dans le volet gauche, sélectionnez **Afficher tout,** puis sous Centres d’administration,  **sélectionnez Azure Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-111">In the left pane, select **Show All,** and then under **Admin centers**, select **Azure Active Directory**.</span></span>

3. <span data-ttu-id="47cbb-112">Dans le volet gauche du Centre d’administration **Azure Active Directory,** sélectionnez **Azure Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-112">In the left pane of the **Azure Active Directory admin center,** select **Azure Active Directory**.</span></span>

4. <span data-ttu-id="47cbb-113">Dans le menu gauche du tableau de bord, dans la section **Gérer,** sélectionnez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-113">From the left menu of the Dashboard, in the **Manage** section, select **Properties**.</span></span>

    :::image type="content" source="../media/m365-campaigns-conditional-access/azure-ad-properties.png" alt-text="Capture d’écran du Centre d’administration Azure Active Directory affichant l’emplacement de l’élément de menu Propriétés.":::

5. <span data-ttu-id="47cbb-115">En bas de la page **Propriétés,** **sélectionnez Gérer les paramètres de sécurité par défaut.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-115">At the bottom of the **Properties** page, select **Manage Security defaults**.</span></span>

6. <span data-ttu-id="47cbb-116">Dans le volet droit, vous verrez le paramètre **Activer les paramètres de sécurité par défaut.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-116">In the right pane, you'll see the **Enable Security defaults** setting.</span></span> <span data-ttu-id="47cbb-117">Si **Oui** est sélectionné, les paramètres de sécurité par défaut sont déjà activés et aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="47cbb-117">If **Yes** is selected, then security defaults are already enabled and no further action is required.</span></span> <span data-ttu-id="47cbb-118">Si les paramètres de sécurité par défaut ne sont pas activés actuellement, sélectionnez **Oui** pour les activer, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="47cbb-118">If security defaults are not currently enabled, then select **Yes** to enable them, and then select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="47cbb-119">Si vous utilisez des stratégies d’accès conditionnel, vous devez les désactiver avant d’utiliser les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="47cbb-119">If you've been using Conditional Access policies, you'll need to turn them off before using security defaults.</span></span>
>
> <span data-ttu-id="47cbb-120">Vous pouvez utiliser les paramètres de sécurité par défaut ou les stratégies d’accès conditionnel, mais vous ne pouvez pas utiliser les deux en même temps.</span><span class="sxs-lookup"><span data-stu-id="47cbb-120">You can use either security defaults or Conditional Access policies, but you can't use both at the same time.</span></span>

## <a name="consider-using-conditional-access"></a><span data-ttu-id="47cbb-121">Envisager d’utiliser l’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="47cbb-121">Consider using Conditional Access</span></span>

<span data-ttu-id="47cbb-122">Si votre organisation a des exigences de sécurité complexes ou si vous avez besoin d’un contrôle plus granulaire sur vos stratégies de sécurité, vous devez envisager d’utiliser l’accès conditionnel au lieu des paramètres de sécurité par défaut pour obtenir une posture de sécurité similaire ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="47cbb-122">If your organization has complex security requirements or you need more granular control over your security policies, then you should consider using Conditional Access instead of security defaults to achieve a similar or higher security posture.</span></span> 

<span data-ttu-id="47cbb-123">L’accès conditionnel vous permet de créer et de définir des stratégies qui réagissent aux événements de connectez-vous et de demander des actions supplémentaires avant qu’un utilisateur ne soit autorisé à accéder à une application ou un service.</span><span class="sxs-lookup"><span data-stu-id="47cbb-123">Conditional Access lets you create and define policies that react to sign-in events and request additional actions before a user is granted access to an application or service.</span></span> <span data-ttu-id="47cbb-124">Les stratégies d’accès conditionnel peuvent être granulaires et spécifiques, permettant aux utilisateurs d’être productifs où et quand, mais aussi de protéger votre organisation.</span><span class="sxs-lookup"><span data-stu-id="47cbb-124">Conditional Access policies can be granular and specific, empowering users to be productive wherever and whenever, but also protecting your organization.</span></span>

<span data-ttu-id="47cbb-125">Les paramètres de sécurité par défaut sont disponibles pour tous les clients, tandis que l’accès conditionnel nécessite une licence pour l’un des plans suivants :</span><span class="sxs-lookup"><span data-stu-id="47cbb-125">Security defaults are available to all customers, while Conditional Access requires a license for one of the following plans:</span></span>

- <span data-ttu-id="47cbb-126">Azure Active Directory Premium P1 ou P2</span><span class="sxs-lookup"><span data-stu-id="47cbb-126">Azure Active Directory Premium P1 or P2</span></span>
- <span data-ttu-id="47cbb-127">Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="47cbb-127">Microsoft 365 Business Premium</span></span>
- <span data-ttu-id="47cbb-128">Microsoft 365 E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="47cbb-128">Microsoft 365 E3 or E5</span></span>
- <span data-ttu-id="47cbb-129">Enterprise Mobility & Security E3 ou E5</span><span class="sxs-lookup"><span data-stu-id="47cbb-129">Enterprise Mobility & Security E3 or E5</span></span>

<span data-ttu-id="47cbb-130">Si vous souhaitez utiliser l’accès conditionnel pour configurer des stratégies équivalentes à celles activées par défaut de sécurité, consultez les guides pas à pas suivants :</span><span class="sxs-lookup"><span data-stu-id="47cbb-130">If you want to use Conditional Access to configure policies equivalent to those enabled by security defaults, check out the following step-by-step guides:</span></span>

- [<span data-ttu-id="47cbb-131">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="47cbb-131">Require MFA for administrators</span></span>](/azure/active-directory/conditional-access/howto-conditional-access-policy-admin-mfa)
- [<span data-ttu-id="47cbb-132">Exiger l’mf pour la gestion Azure</span><span class="sxs-lookup"><span data-stu-id="47cbb-132">Require MFA for Azure management</span></span>](/azure/active-directory/conditional-access/howto-conditional-access-policy-azure-management)
- [<span data-ttu-id="47cbb-133">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="47cbb-133">Block legacy authentication</span></span>](/azure/active-directory/conditional-access/howto-conditional-access-policy-block-legacy)
- [<span data-ttu-id="47cbb-134">Exiger l’authentification multifacteur pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="47cbb-134">Require MFA for all users</span></span>](/azure/active-directory/conditional-access/howto-conditional-access-policy-all-users-mfa)
- <span data-ttu-id="47cbb-135">[Exiger l’inscription Azure AD MFA](/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy) - Nécessite Azure AD Identity Protection, qui fait partie d’Azure Active Directory Premium P2</span><span class="sxs-lookup"><span data-stu-id="47cbb-135">[Require Azure AD MFA registration](/azure/active-directory/identity-protection/howto-identity-protection-configure-mfa-policy) - Requires Azure AD Identity Protection, which is part of Azure Active Directory Premium P2</span></span>

<span data-ttu-id="47cbb-136">Pour en savoir plus sur l’accès conditionnel, voir [qu’est-ce que l’accès conditionnel ?](/azure/active-directory/conditional-access/overview)</span><span class="sxs-lookup"><span data-stu-id="47cbb-136">To learn more about Conditional Access, see [What is Conditional Access?](/azure/active-directory/conditional-access/overview)</span></span> <span data-ttu-id="47cbb-137">Pour plus d’informations sur la création de stratégies d’accès conditionnel, voir [Créer une stratégie d’accès conditionnel.](/azure/active-directory/authentication/tutorial-enable-azure-mfa#create-a-conditional-access-policy)</span><span class="sxs-lookup"><span data-stu-id="47cbb-137">For more information about creating Conditional Access policies, see [Create a Conditional Access policy](/azure/active-directory/authentication/tutorial-enable-azure-mfa#create-a-conditional-access-policy).</span></span>

> [!NOTE]
> <span data-ttu-id="47cbb-138">Si vous disposez d’un plan ou d’une licence qui fournit l’accès conditionnel, mais que vous n’avez pas encore créé de stratégies d’accès conditionnel, vous pouvez utiliser les paramètres de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="47cbb-138">If you have a plan or license that provides Conditional Access but haven't yet created any Conditional Access policies, you're welcome to use security defaults.</span></span> <span data-ttu-id="47cbb-139">Toutefois, vous devez désactiver les paramètres de sécurité par défaut avant de pouvoir utiliser des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="47cbb-139">However, you'll need to turn off security defaults before you can use Conditional Access policies.</span></span>
