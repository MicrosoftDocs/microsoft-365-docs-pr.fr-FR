---
title: Qu’est-ce que l’accès conditionnel ?
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
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
description: Découvrez comment exiger une mf et configurer des stratégies d’accès conditionnel pour Microsoft 365 pour les entreprises.
ms.openlocfilehash: b13ba9f8c948d9a1209655c44871ca62cb5354dd
ms.sourcegitcommit: 1b30ac6e05906c8a014b1fed33fc71e1821f6ad2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "50044499"
---
# <a name="require-multi-factor-authentication-and-set-up-conditional-access-policies"></a><span data-ttu-id="0972e-103">Exiger une authentification multifacteur et configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="0972e-103">Require multi-factor authentication and set up conditional access policies</span></span>

<span data-ttu-id="0972e-104">Vous protégez l’accès à vos données à l’aide de stratégies d’authentification multifacteur et d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="0972e-104">You protect access to your data with multi-factor authentication and conditional access policies.</span></span> <span data-ttu-id="0972e-105">Celles-ci ajoutent une sécurité supplémentaire importante.</span><span class="sxs-lookup"><span data-stu-id="0972e-105">These add substantial additional security.</span></span> <span data-ttu-id="0972e-106">Microsoft fournit un ensemble de stratégies d’accès conditionnel de base recommandées pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="0972e-106">Microsoft provides a set of baseline conditional access policies that are recommended for all customers.</span></span> <span data-ttu-id="0972e-107">Les stratégies de base sont un ensemble de stratégies prédéfines qui aident à protéger les organisations contre de nombreuses attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="0972e-107">Baseline policies are a set of predefined policies that help protect organizations against many common attacks.</span></span> <span data-ttu-id="0972e-108">Ces attaques courantes peuvent inclure la pulvérisation de mot de passe, la relecture et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="0972e-108">These common attacks can include password spray, replay, and phishing.</span></span>

<span data-ttu-id="0972e-109">Ces stratégies exigent que les administrateurs et les utilisateurs entrent dans un second formulaire d’authentification (appelé authentification multifacteur, ou authentification multifacteur) dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="0972e-109">These policies require admins and users to enter a second form of authentication (called multi-factor authentication, or MFA) under certain conditions.</span></span> <span data-ttu-id="0972e-110">Par exemple, si un utilisateur de votre organisation tente de se connecter à Microsoft 365 à partir d’un autre pays ou d’un appareil inconnu, la sign-in peut être considérée comme risquée.</span><span class="sxs-lookup"><span data-stu-id="0972e-110">For example, if a user in your organization tries to sign in to Microsoft 365 from a different country or from an unknown device, the sign-in might be considered risky.</span></span> <span data-ttu-id="0972e-111">L’utilisateur doit fournir une forme supplémentaire d’authentification (par exemple, une empreinte digitale ou un code) pour prouver son identité.</span><span class="sxs-lookup"><span data-stu-id="0972e-111">The user must provide an extra form of authentication (such as a fingerprint or a code) to prove their identity.</span></span>

<span data-ttu-id="0972e-112">Actuellement, les stratégies de référence incluent les stratégies suivantes :</span><span class="sxs-lookup"><span data-stu-id="0972e-112">Currently, the baseline policies include the following policies:</span></span>

- <span data-ttu-id="0972e-113">Configurer dans le Centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="0972e-113">Set up in Microsoft 365 admin center:</span></span>
  - <span data-ttu-id="0972e-114">**Exiger l’authentification multifacteur pour** les administrateurs : nécessite une authentification multifacteur pour les rôles d’administrateur les plus privilégiés, y compris l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="0972e-114">**Require MFA for admins**: Requires multi-factor authentication for the most privileged administrator roles, including global administrator.</span></span>
  - <span data-ttu-id="0972e-115">**Protection de l’utilisateur final**: nécessite une authentification multifacteur pour les utilisateurs uniquement lorsqu’une authentification est risquée.</span><span class="sxs-lookup"><span data-stu-id="0972e-115">**End-user protection**: Requires multi-factor authentication for users only when a sign-in is risky.</span></span> 
- <span data-ttu-id="0972e-116">Configurer dans le portail Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="0972e-116">Set up in Azure Active Directory portal:</span></span>
  - <span data-ttu-id="0972e-117">**Bloquer l’authentification** héritée : les applications clientes plus anciennes et certaines nouvelles applications n’utilisent pas de protocoles d’authentification plus nouveaux, plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="0972e-117">**Block legacy authentication**: Older client apps and some new apps don't use newer, more secure, authentication protocols.</span></span> <span data-ttu-id="0972e-118">Ces anciennes applications peuvent contourner les stratégies d’accès conditionnel et obtenir un accès non autorisé à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0972e-118">These older apps can bypass conditional access policies and gain unauthorized access to your environment.</span></span> <span data-ttu-id="0972e-119">Cette stratégie bloque l’accès des clients qui ne la prisent pas en charge de l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="0972e-119">This policy blocks access from clients that don't support conditional access.</span></span> 
  - <span data-ttu-id="0972e-120">**Exiger l’authentification** multifacteur pour la gestion des services : nécessite une authentification multifacteur pour l’accès aux outils de gestion, y compris au portail Azure (où vous configurez les stratégies de référence).</span><span class="sxs-lookup"><span data-stu-id="0972e-120">**Require MFA for Service Management**: Requires multi-factor authentication for access to management tools, including Azure portal (where you configure baseline policies).</span></span>

<span data-ttu-id="0972e-121">Nous vous recommandons d’activer toutes ces stratégies de référence.</span><span class="sxs-lookup"><span data-stu-id="0972e-121">We recommend that you enable all of these baseline policies.</span></span> <span data-ttu-id="0972e-122">Une fois ces stratégies activées, les administrateurs et les utilisateurs sont invités à s’inscrire à l’authentification multifacteur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0972e-122">After these policies are enabled, admins and users will be prompted to register for Azure AD Multifactor Authentication.</span></span>

<span data-ttu-id="0972e-123">Pour plus d’informations sur ces stratégies, voir [Quelles sont les stratégies de base](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span><span class="sxs-lookup"><span data-stu-id="0972e-123">For more information about these policies, see [What are baseline policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span></span>

## <a name="require-mfa"></a><span data-ttu-id="0972e-124">Exiger une authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="0972e-124">Require MFA</span></span>

<span data-ttu-id="0972e-125">Pour exiger que tous les utilisateurs se connectent avec un deuxième formulaire d’ID :</span><span class="sxs-lookup"><span data-stu-id="0972e-125">To require that all users sign in with a second form of ID:</span></span>

1. <span data-ttu-id="0972e-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> and choose **Setup**.</span><span class="sxs-lookup"><span data-stu-id="0972e-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> and choose **Setup**.</span></span>

2. <span data-ttu-id="0972e-127">Dans la page Installation, **sélectionnez Afficher** dans la carte **de configuration plus** sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0972e-127">On the Setup page, choose **View** in the **Make sign-in more secure** card.</span></span>

    ![Rendre la carte de connectez-vous plus sécurisée.](../media/setupmfa.png)
3. <span data-ttu-id="0972e-129">On the Make sign-in more secure page, choose **Get started**.</span><span class="sxs-lookup"><span data-stu-id="0972e-129">On the Make sign-in more secure page, choose **Get started**.</span></span>

4. <span data-ttu-id="0972e-130">Dans le volet Renforcer la sécurité de la signature, cochez les cases en regard de Exiger une authentification **multifacteur** pour les administrateurs et demander aux utilisateurs de s’inscrire à l’authentification **multifacteur** et de bloquer l’accès si un risque est détecté.</span><span class="sxs-lookup"><span data-stu-id="0972e-130">On the Strengthen sign-in security pane, select the check boxes next to **Require multi-factor authentication for admins** and **Require users to register for multi-factor authentication and block access if risk is detected**.</span></span>
    <span data-ttu-id="0972e-131">N’oubliez [](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) pas d’exclure le compte d’administrateur d’urgence ou « en cas d’urgence » de l’exigence de l’mf dans la zone Rechercher **des utilisateurs.**</span><span class="sxs-lookup"><span data-stu-id="0972e-131">Be sure to exclude the [emergency](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) or "break-glass" admin account from the MFA requirement in the **Find users** box.</span></span>

    ![Renforcer la page de sécurité du sing-in.](../media/requiremfa.png)

5. <span data-ttu-id="0972e-133">Choisissez **Créer une stratégie** en bas de la page.</span><span class="sxs-lookup"><span data-stu-id="0972e-133">Choose **Create policy** on the bottom of the page.</span></span>

## <a name="set-up-baseline-policies"></a><span data-ttu-id="0972e-134">Configurer des stratégies de référence</span><span class="sxs-lookup"><span data-stu-id="0972e-134">Set up baseline policies</span></span>

1. <span data-ttu-id="0972e-135">Accédez au [portail Azure,](https://portal.azure.com)puis accédez à **l’accès** conditionnel Azure Active Directory \>  pour créer **une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="0972e-135">Go to the [Azure portal](https://portal.azure.com), and then navigate to **Azure Active Directory** \> **Conditional Access** to create a **new policy**.</span></span>

<span data-ttu-id="0972e-136">Consultez les instructions spécifiques suivantes pour chaque stratégie :</span><span class="sxs-lookup"><span data-stu-id="0972e-136">See the following specific instructions for each policy:</span></span> <br>
    - [<span data-ttu-id="0972e-137">Exiger l’mf pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="0972e-137">Require MFA for admins</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-administrators) <br>
    - [<span data-ttu-id="0972e-138">Exiger l’mf pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="0972e-138">Require MFA for users</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-end-users) <br>
    - [<span data-ttu-id="0972e-139">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="0972e-139">Block legacy authentication</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-legacy-auth) <br>
    - [<span data-ttu-id="0972e-140">Exiger l’mf pour la gestion des services</span><span class="sxs-lookup"><span data-stu-id="0972e-140">Require MFA for service management</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-azure)

> [!NOTE]
> <span data-ttu-id="0972e-141">Les stratégies d’aperçu n’existent plus et les utilisateurs doivent créer leurs propres stratégies.</span><span class="sxs-lookup"><span data-stu-id="0972e-141">Preview policies no longer exist and users will need to create their own policies.</span></span>

<span data-ttu-id="0972e-142">Vous pouvez configurer des stratégies supplémentaires, telles que l’obligation d’applications clientes approuvées.</span><span class="sxs-lookup"><span data-stu-id="0972e-142">You can set up extra policies, such as requiring approved client apps.</span></span> <span data-ttu-id="0972e-143">Pour plus d’informations, voir la [documentation relative à l’accès conditionnel.](https://docs.microsoft.com/azure/active-directory/conditional-access/)</span><span class="sxs-lookup"><span data-stu-id="0972e-143">For more information, see the [Conditional Access documentation](https://docs.microsoft.com/azure/active-directory/conditional-access/).</span></span>
