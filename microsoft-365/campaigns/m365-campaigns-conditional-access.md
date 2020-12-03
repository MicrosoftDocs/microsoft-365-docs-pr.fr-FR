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
description: Découvrez comment exiger l’authentification MFA et configurer des stratégies d’accès conditionnel pour Microsoft 365 pour les entreprises.
ms.openlocfilehash: 08a77615d6801eef52465c450c2559a9d786befb
ms.sourcegitcommit: c1dd5be42fe0c5dcc7c05817c941edd9076febf8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49558273"
---
# <a name="require-multi-factor-authentication-and-set-up-conditional-access-policies"></a><span data-ttu-id="48000-103">Exiger l’authentification multifacteur et configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="48000-103">Require multi-factor authentication and set up conditional access policies</span></span>

<span data-ttu-id="48000-104">Vous protégez l’accès à vos données à l’aide de l’authentification multifacteur et des stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="48000-104">You protect access to your data with multi-factor authentication and conditional access policies.</span></span> <span data-ttu-id="48000-105">Ces éléments ajoutent une sécurité supplémentaire importante.</span><span class="sxs-lookup"><span data-stu-id="48000-105">These add substantial additional security.</span></span> <span data-ttu-id="48000-106">Microsoft fournit un ensemble de stratégies d’accès conditionnel de base qui sont recommandées pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="48000-106">Microsoft provides a set of baseline conditional access policies that are recommended for all customers.</span></span> <span data-ttu-id="48000-107">Les stratégies de référence sont un ensemble de stratégies prédéfinies qui permettent de protéger les organisations contre de nombreuses attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="48000-107">Baseline policies are a set of predefined policies that help protect organizations against many common attacks.</span></span> <span data-ttu-id="48000-108">Ces attaques courantes peuvent inclure le pulvérisation de mot de passe, la relecture et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="48000-108">These common attacks can include password spray, replay, and phishing.</span></span>

<span data-ttu-id="48000-109">Ces stratégies exigent que les administrateurs et les utilisateurs entrent une deuxième forme d’authentification (appelée authentification multifacteur ou MFA) lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="48000-109">These policies require admins and users to enter a second form of authentication (called multi-factor authentication, or MFA) when certain conditions are met.</span></span> <span data-ttu-id="48000-110">Par exemple, si un utilisateur de votre organisation tente de se connecter à Microsoft 365 à partir d’un autre pays ou d’un appareil inconnu, la connexion peut être considérée comme risquée.</span><span class="sxs-lookup"><span data-stu-id="48000-110">For example, if a user in your organization tries to sign in to Microsoft 365 from a different country or from an unknown device, the sign-in might be considered risky.</span></span> <span data-ttu-id="48000-111">L’utilisateur doit fournir une forme supplémentaire d’authentification (par exemple, une empreinte digitale ou un code) pour prouver son identité.</span><span class="sxs-lookup"><span data-stu-id="48000-111">The user must provide an extra form of authentication (such as a fingerprint or a code) to prove their identity.</span></span> 

<span data-ttu-id="48000-112">Actuellement, les stratégies de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="48000-112">Currently, baseline policies include the following:</span></span>
- <span data-ttu-id="48000-113">Configurer dans le centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="48000-113">Set up in Microsoft 365 admin center:</span></span>
    - <span data-ttu-id="48000-114">**Exiger MFA pour les administrateurs** : nécessite une authentification multifacteur pour les rôles d’administrateur les plus privilégiés, y compris l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="48000-114">**Require MFA for admins** — Requires multi-factor authentication for the most privileged administrator roles, including global administrator.</span></span>
    - <span data-ttu-id="48000-115">**Protection** des utilisateurs finaux : nécessite l’authentification multifacteur pour les utilisateurs uniquement lorsqu’une connexion est risquée.</span><span class="sxs-lookup"><span data-stu-id="48000-115">**End user protection** — Requires multi-factor authentication for users only when a sign-in is risky.</span></span> 
- <span data-ttu-id="48000-116">Configurer dans le portail Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="48000-116">Set up in Azure Active Directory portal:</span></span>
    - <span data-ttu-id="48000-117">**Bloquer l’authentification héritée** : les applications clientes plus anciennes et certaines nouvelles applications n’utilisent pas de protocoles d’authentification plus récents et plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="48000-117">**Block legacy authentication** — Older client apps and some new apps don't use newer, more secure, authentication protocols.</span></span> <span data-ttu-id="48000-118">Ces anciennes applications peuvent contourner des stratégies d’accès conditionnel et obtenir un accès non autorisé à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="48000-118">These older apps can bypass conditional access policies and gain unauthorized access to your environment.</span></span> <span data-ttu-id="48000-119">Cette stratégie bloque l’accès à partir des clients qui ne prennent pas en charge l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="48000-119">This policy blocks access from clients that don't support conditional access.</span></span> 
    - <span data-ttu-id="48000-120">**Exiger MFA pour la gestion des services** : nécessite l’authentification multifacteur pour l’accès aux outils de gestion, y compris le portail Azure (où vous configurez les stratégies de base).</span><span class="sxs-lookup"><span data-stu-id="48000-120">**Require MFA for Service Management** — Requires multi-factor authentication for access to management tools, including Azure portal (where you configure baseline policies).</span></span> 

<span data-ttu-id="48000-121">Microsoft vous recommande d’activer toutes ces stratégies de base.</span><span class="sxs-lookup"><span data-stu-id="48000-121">Microsoft recommends that you enable all of these baseline policies.</span></span> <span data-ttu-id="48000-122">Une fois ces stratégies activées, les administrateurs et les utilisateurs sont invités à s’inscrire pour l’authentification multifacteur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="48000-122">After these policies are enabled, admins and users will be prompted to register for Azure AD Multi-Factor authentication.</span></span>

<span data-ttu-id="48000-123">Pour plus d’informations sur ces stratégies, voir [qu’est-ce qu’une stratégie de base](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span><span class="sxs-lookup"><span data-stu-id="48000-123">For more information about these policies, see [What are baseline policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span></span>


## <a name="require-mfa"></a><span data-ttu-id="48000-124">Exiger une authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="48000-124">Require MFA</span></span>

<span data-ttu-id="48000-125">Pour exiger que tous les utilisateurs se connectent avec une deuxième forme d’ID :</span><span class="sxs-lookup"><span data-stu-id="48000-125">To require that all users sign in with a second form of ID:</span></span>

1. <span data-ttu-id="48000-126">Accédez au centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> et sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="48000-126">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a> and choose **Setup**.</span></span>

2. <span data-ttu-id="48000-127">Sur la page de configuration, choisissez **Afficher** dans la carte de **connexion plus sécurisée** .</span><span class="sxs-lookup"><span data-stu-id="48000-127">On the Setup page, choose **View** in the **Make sign-in more secure** card.</span></span>


    ![Créer une carte plus sécurisée de connexion.](../media/setupmfa.png)
3. <span data-ttu-id="48000-129">Sur la page effectuer la connexion de façon plus sécurisée, sélectionnez **prise en main**.</span><span class="sxs-lookup"><span data-stu-id="48000-129">On the Make sign-in more secure page, choose **Get started**.</span></span>
 
4. <span data-ttu-id="48000-130">Dans le volet sécurité de connexion renforcée, activez les cases à cocher en regard de **exiger l’authentification multifacteur pour les administrateurs** et **obliger les utilisateurs à s’inscrire pour l’authentification multifacteur et à bloquer l’accès si le risque est détecté**.</span><span class="sxs-lookup"><span data-stu-id="48000-130">On the Strengthen sign-in security pane, select the check boxes next to **Require multi-factor authentication for admins** and **Require users to register for multi-factor authentication and block access if risk is detected**.</span></span>
    <span data-ttu-id="48000-131">N’oubliez pas d’exclure le compte administrateur d' [urgence](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) ou de « disjoncteur » de l’exigence MFA dans la zone **Rechercher des utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="48000-131">Be sure to exclude the [emergency](m365-campaigns-protect-admin-accounts.md#create-an-emergency-admin-account) or "break-glass" admin account from the MFA requirement in the **Find users** box.</span></span>
    
    ![Renforcer la page de sécurité à connexion unique.](../media/requiremfa.png)

5. <span data-ttu-id="48000-133">Sélectionnez **créer une stratégie** au bas de la page.</span><span class="sxs-lookup"><span data-stu-id="48000-133">Choose **Create policy** on the bottom of the page.</span></span>

## <a name="set-up-baseline-policies"></a><span data-ttu-id="48000-134">Configurer des stratégies de base</span><span class="sxs-lookup"><span data-stu-id="48000-134">Set up baseline policies</span></span>

1. <span data-ttu-id="48000-135">Accédez au [portail Azure](https://portal.azure.com), puis accédez à **Azure Active Directory** \> **ConditionalAttribute Access** pour créer une **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="48000-135">Go to the [Azure portal](https://portal.azure.com), and then navigate to **Azure Active Directory** \> **Conditional Access** to create a **new policy**.</span></span>

<span data-ttu-id="48000-136">Consultez les instructions spécifiques suivantes pour chaque stratégie :</span><span class="sxs-lookup"><span data-stu-id="48000-136">See the following specific instructions for each policy:</span></span> <br>
    - [<span data-ttu-id="48000-137">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="48000-137">Require MFA for admins</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-administrators) <br>
    - [<span data-ttu-id="48000-138">Exiger l’authentification multifacteur pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="48000-138">Require MFA for users</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-end-users) <br>
    - [<span data-ttu-id="48000-139">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="48000-139">Block legacy authentication</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-legacy-auth) <br>
    - [<span data-ttu-id="48000-140">Exiger MFA pour la gestion des services</span><span class="sxs-lookup"><span data-stu-id="48000-140">Require MFA for service management</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-azure)
    
> [!NOTE]
> <span data-ttu-id="48000-141">Les stratégies d’aperçu n’existent plus et les utilisateurs devront créer leurs propres stratégies.</span><span class="sxs-lookup"><span data-stu-id="48000-141">Preview policies no longer exist and users will need to create their own policies.</span></span>


<span data-ttu-id="48000-142">Vous pouvez configurer des stratégies supplémentaires, telles que la demande d’applications clientes approuvées.</span><span class="sxs-lookup"><span data-stu-id="48000-142">You can set up extra policies, such as requiring approved client apps.</span></span> <span data-ttu-id="48000-143">Pour plus d’informations, consultez la documentation sur l' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/).</span><span class="sxs-lookup"><span data-stu-id="48000-143">For more information, see the [Conditional Access documentation](https://docs.microsoft.com/azure/active-directory/conditional-access/).</span></span>
