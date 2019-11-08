---
title: Configurer des stratégies d’accès conditionnel
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
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment exiger l’authentification MFA et configurer des stratégies d’accès conditionnel pour Microsoft 365 Business.
ms.openlocfilehash: b4ea67037339ae1a00f12d7b51e4584d259264e4
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38031339"
---
# <a name="require-multi-factor-authentication-and-set-up-conditional-access-policies"></a><span data-ttu-id="b850a-103">Exiger l’authentification multifacteur et configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b850a-103">Require multi-factor authentication and set up conditional access policies</span></span>

<span data-ttu-id="b850a-104">Vous protégez l’accès à vos données à l’aide de l’authentification multifacteur et des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="b850a-104">You protect access to your data with multi-factor authentication and conditional access policies.</span></span> <span data-ttu-id="b850a-105">Ces éléments ajoutent une sécurité supplémentaire importante.</span><span class="sxs-lookup"><span data-stu-id="b850a-105">These add substantial additional security.</span></span> <span data-ttu-id="b850a-106">Microsoft fournit un ensemble de stratégies d’accès conditionnel de base qui sont recommandées pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="b850a-106">Microsoft provides a set of baseline conditional access policies that are recommended for all customers.</span></span> <span data-ttu-id="b850a-107">Les stratégies de référence sont un ensemble de stratégies prédéfinies qui permettent de protéger les organisations contre de nombreuses attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="b850a-107">Baseline policies are a set of predefined policies that help protect organizations against many common attacks.</span></span> <span data-ttu-id="b850a-108">Ces attaques courantes peuvent inclure le pulvérisation de mot de passe, la relecture et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b850a-108">These common attacks can include password spray, replay, and phishing.</span></span>

<span data-ttu-id="b850a-109">Ces stratégies exigent que les administrateurs et les utilisateurs entrent une deuxième forme d’authentification (appelée authentification multifacteur ou MFA) lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="b850a-109">These policies require admins and users to enter a second form of authentication (called multi-factor authentication, or MFA) when certain conditions are met.</span></span> <span data-ttu-id="b850a-110">Par exemple, si un utilisateur de votre organisation tente de se connecter à Microsoft 365 à partir d’un autre pays ou d’un appareil inconnu, la connexion peut être considérée comme risquée.</span><span class="sxs-lookup"><span data-stu-id="b850a-110">For example, if a user in your organization tries to sign in to Microsoft 365 from a different country or from an unknown device, the sign-in might be considered risky.</span></span> <span data-ttu-id="b850a-111">L’utilisateur doit fournir une forme supplémentaire d’authentification (par exemple, une empreinte digitale ou un code) pour prouver son identité.</span><span class="sxs-lookup"><span data-stu-id="b850a-111">The user must provide an extra form of authentication (such as a fingerprint or a code) to prove their identity.</span></span> 

<span data-ttu-id="b850a-112">Actuellement, les stratégies de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b850a-112">Currently, baseline policies include the following:</span></span>
- <span data-ttu-id="b850a-113">Configurer dans le centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="b850a-113">Set up in Microsoft 365 admin center:</span></span>
    - <span data-ttu-id="b850a-114">**Exiger MFA pour les administrateurs** : nécessite une authentification multifacteur pour les rôles d’administrateur les plus privilégiés, y compris l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b850a-114">**Require MFA for admins** — Requires multi-factor authentication for the most privileged administrator roles, including global administrator.</span></span>
    - <span data-ttu-id="b850a-115">**Protection** des utilisateurs finaux : nécessite l’authentification multifacteur pour les utilisateurs uniquement lorsqu’une connexion est risquée.</span><span class="sxs-lookup"><span data-stu-id="b850a-115">**End user protection** — Requires multi-factor authentication for users only when a sign-in is risky.</span></span> 
- <span data-ttu-id="b850a-116">Configurer dans le portail Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="b850a-116">Set up in Azure Active Directory portal:</span></span>
    - <span data-ttu-id="b850a-117">**Bloquer l’authentification héritée** : les applications clientes plus anciennes et certaines nouvelles applications n’utilisent pas de protocoles d’authentification plus récents et plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="b850a-117">**Block legacy authentication** — Older client apps and some new apps don't use newer, more secure, authentication protocols.</span></span> <span data-ttu-id="b850a-118">Ces anciennes applications peuvent contourner des stratégies d’accès conditionnel et obtenir un accès non autorisé à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="b850a-118">These older apps can bypass conditional access policies and gain unauthorized access to your environment.</span></span> <span data-ttu-id="b850a-119">Cette stratégie bloque l’accès à partir des clients qui ne prennent pas en charge l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="b850a-119">This policy blocks access from clients that don't support conditional access.</span></span> 
    - <span data-ttu-id="b850a-120">**Exiger MFA pour la gestion des services** : nécessite l’authentification multifacteur pour l’accès aux outils de gestion, y compris le portail Azure (où vous configurez les stratégies de base).</span><span class="sxs-lookup"><span data-stu-id="b850a-120">**Require MFA for Service Management** — Requires multi-factor authentication for access to management tools, including Azure portal (where you configure baseline policies).</span></span> 

<span data-ttu-id="b850a-121">Microsoft vous recommande d’activer toutes ces stratégies de base.</span><span class="sxs-lookup"><span data-stu-id="b850a-121">Microsoft recommends that you enable all of these baseline policies.</span></span> <span data-ttu-id="b850a-122">Une fois ces stratégies activées, les administrateurs et les utilisateurs sont invités à s’inscrire pour l’authentification multifacteur Azure.</span><span class="sxs-lookup"><span data-stu-id="b850a-122">After these policies are enabled, admins and users will be prompted to register for Azure Multi-Factor authentication.</span></span>

<span data-ttu-id="b850a-123">Pour plus d’informations sur ces stratégies, voir [qu’est-ce qu’une stratégie de base](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span><span class="sxs-lookup"><span data-stu-id="b850a-123">For more information about these policies, see [What are baseline policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span></span>


## <a name="require-mfa"></a><span data-ttu-id="b850a-124">Exiger une authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="b850a-124">Require MFA</span></span>

<span data-ttu-id="b850a-125">Pour exiger que tous les utilisateurs se connectent avec une deuxième forme d’ID :</span><span class="sxs-lookup"><span data-stu-id="b850a-125">To require that all users sign in with a second form of ID:</span></span>

1. <span data-ttu-id="b850a-126">Accédez au centre d’administration à <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> l’adresse et sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="b850a-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> and choose **Setup**.</span></span>

2. <span data-ttu-id="b850a-127">Sur la page de configuration, choisissez **Afficher** dans la carte de **connexion plus sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="b850a-127">On the Setup page, choose **View** in the **Make sign-in more secure** card.</span></span>


    ![Créer une carte plus sécurisée de connexion.](media/setupmfa.png)
3. <span data-ttu-id="b850a-129">Sur la page effectuer la connexion de façon plus sécurisée, sélectionnez **prise en main**.</span><span class="sxs-lookup"><span data-stu-id="b850a-129">On the Make sign-in more secure page, choose **Get started**.</span></span>
 
4. <span data-ttu-id="b850a-130">Dans le volet sécurité de connexion renforcée, activez les cases à cocher en regard de **exiger l’authentification multifacteur pour les administrateurs** et **obliger les utilisateurs à s’inscrire pour l’authentification multifacteur et à bloquer l’accès si le risque est détecté**.</span><span class="sxs-lookup"><span data-stu-id="b850a-130">On the Strengthen sign-in security pane, check the check boxes next to **Require multi-factor authentication for admins** and **Require users to register for multi-factor authentication and block access if risk is detected**.</span></span>
    <span data-ttu-id="b850a-131">N’oubliez pas d’exclure le compte administrateur d' [urgence](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) ou de « disjoncteur » de l’exigence MFA dans la zone **Rechercher des utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="b850a-131">Be sure to exclude the [emergency](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) or "break-glass" admin account from the MFA requirement in the **Find users** box.</span></span>
    
    ![Renforcer la page de sécurité à connexion unique.](media/requiremfa.png)

5. <span data-ttu-id="b850a-133">Sélectionnez **créer une stratégie** au bas de la page.</span><span class="sxs-lookup"><span data-stu-id="b850a-133">Choose **Create policy** on the bottom of the page.</span></span>

## <a name="set-up-baseline-policies"></a><span data-ttu-id="b850a-134">Configurer des stratégies de base</span><span class="sxs-lookup"><span data-stu-id="b850a-134">Set up baseline policies</span></span>

1. <span data-ttu-id="b850a-135">Accédez au [portail Azure](https://portal.azure.com), puis accédez à **Azure Active Directory** \> **accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="b850a-135">Go to [Azure portal](https://portal.azure.com), and then navigate to **Azure Active Directory** \> **Conditional Access**.</span></span>
    
    <span data-ttu-id="b850a-136">Les stratégies de base sont répertoriées sur la page, et vous pouvez voir que l’authentification MFA pour les administrateurs et la protection des utilisateurs finaux sont déjà activées une fois que vous avez effectué les étapes de la rubrique [require MFA](#require-mfa).</span><span class="sxs-lookup"><span data-stu-id="b850a-136">The baseline policies are listed on the page, and you can see that Require MFA for admins and End user protection are already enabled after you completed the steps in [require MFA](#require-mfa).</span></span>

    ![Page répertoriant les stratégies de base pour l’accès conditionnel.](media/casettings.png)
2. <span data-ttu-id="b850a-138">Consultez les instructions spécifiques suivantes pour chaque stratégie :</span><span class="sxs-lookup"><span data-stu-id="b850a-138">See the following specific instructions for each policy:</span></span>

    - [<span data-ttu-id="b850a-139">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="b850a-139">Require MFA for admins</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-administrators)

       
    -   [<span data-ttu-id="b850a-140">Exiger l’authentification multifacteur pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b850a-140">Require MFA for users</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-end-users)  
    - [<span data-ttu-id="b850a-141">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="b850a-141">Block legacy authentication</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-legacy-auth)
    - [<span data-ttu-id="b850a-142">Exiger MFA pour la gestion des services</span><span class="sxs-lookup"><span data-stu-id="b850a-142">Require MFA for service management</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-azure)

<span data-ttu-id="b850a-143">Vous pouvez configurer des stratégies supplémentaires, telles que la demande d’applications clientes approuvées.</span><span class="sxs-lookup"><span data-stu-id="b850a-143">You can set up extra policies, such as requiring approved client apps.</span></span> <span data-ttu-id="b850a-144">Pour plus d’informations, reportez-vous à la documentation sur l' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/) .</span><span class="sxs-lookup"><span data-stu-id="b850a-144">See the [Conditional Access Documentation](https://docs.microsoft.com/azure/active-directory/conditional-access/) for more information.</span></span>
