---
title: Configurer des stratégies d’accès conditionnel pour les campagnes Microsoft 365
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
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment configurer des stratégies d’accès conditionnel pour les campagnes Microsoft 365.
ms.openlocfilehash: 614e3a6e13a14114f40ecf87bf936d4165744503
ms.sourcegitcommit: 91ff1d4339f0f043c2b43997d87d84677c79e279
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2019
ms.locfileid: "36982378"
---
# <a name="set-up-conditional-access-policies"></a><span data-ttu-id="06634-103">Configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="06634-103">Set up conditional access policies</span></span>

<span data-ttu-id="06634-104">Les stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) ajoutent une sécurité supplémentaire substancial.</span><span class="sxs-lookup"><span data-stu-id="06634-104">[Conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies add substancial additional security.</span></span> <span data-ttu-id="06634-105">Microsoft fournit un ensemble de stratégies d’accès conditionnel de base qui sont recommandées pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="06634-105">Microsoft provides a set of baseline conditional access policies that are recommended for all customers.</span></span> <span data-ttu-id="06634-106">Les stratégies de référence sont un ensemble de stratégies prédéfinies qui permettent de protéger les organisations contre de nombreuses attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="06634-106">Baseline policies are a set of predefined policies that help protect organizations against many common attacks.</span></span> <span data-ttu-id="06634-107">Ces attaques courantes peuvent inclure le pulvérisation de mot de passe, la relecture et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="06634-107">These common attacks can include password spray, replay, and phishing.</span></span>

<span data-ttu-id="06634-108">Ces stratégies exigent que les administrateurs et les utilisateurs entrent une deuxième forme d’authentification (appelée authentification multifacteur ou MFA) lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="06634-108">These policies require admins and users to enter a second form of authentication (called multifactor authentication, or MFA) when certain conditions are met.</span></span> <span data-ttu-id="06634-109">Par exemple, si un utilisateur se connecte à partir d’un autre pays, la connexion peut être considérée comme risquée et l’utilisateur doit fournir une forme supplémentaire d’authentification.</span><span class="sxs-lookup"><span data-stu-id="06634-109">For example, if a user is signing in from a different country, the sign-in might be considered risky and the user must provide an additional form of authentication.</span></span> 

<span data-ttu-id="06634-110">Actuellement, les stratégies de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="06634-110">Currently, baseline policies include the following:</span></span>
- <span data-ttu-id="06634-111">**Exiger MFA pour les administrateurs** : nécessite une authentification multifacteur pour les rôles d’administrateur les plus privilégiés, y compris l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="06634-111">**Require MFA for admins** — Requires multi-factor authentication for the most privileged administrator roles, including global administrator.</span></span>
- <span data-ttu-id="06634-112">**Protection** des utilisateurs finaux : nécessite l’authentification multifacteur pour les utilisateurs uniquement lorsqu’une connexion est risquée.</span><span class="sxs-lookup"><span data-stu-id="06634-112">**End user protection** — Requires multi-factor authentication for users only when a sign-in is risky.</span></span> 
- <span data-ttu-id="06634-113">**Bloquer l’authentification héritée** : les applications clientes plus anciennes et certaines nouvelles applications n’utilisent pas de protocoles d’authentification plus récents et plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="06634-113">**Block legacy authentication** — Older client apps and some new apps don't use newer, more secure, authentication protocols.</span></span> <span data-ttu-id="06634-114">Ces anciennes applications peuvent contourner des stratégies d’accès conditionnel et obtenir un accès non autorisé à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="06634-114">These older apps can bypass conditional access policies and gain unauthorized access to your environment.</span></span> <span data-ttu-id="06634-115">Cette stratégie bloque l’accès à partir des clients qui ne prennent pas en charge l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="06634-115">This policy blocks access from clients that don't support conditional access.</span></span> 
- <span data-ttu-id="06634-116">**Exiger MFA pour la gestion des services** : nécessite l’authentification multifacteur pour l’accès aux outils de gestion, y compris le portail Azure (où vous configurez les stratégies de base).</span><span class="sxs-lookup"><span data-stu-id="06634-116">**Require MFA for Service Management** — Requires multi-factor authentication for access to management tools, including Azure portal (where you configure baseline policies).</span></span> 

<span data-ttu-id="06634-117">Microsoft vous recommande d’activer toutes ces stratégies de base.</span><span class="sxs-lookup"><span data-stu-id="06634-117">Microsoft recommends you enable all of these baseline policies.</span></span> <span data-ttu-id="06634-118">Une fois ces stratégies activées, les administrateurs et les utilisateurs sont invités à s’inscrire pour l’authentification Azure Multi-Factor.</span><span class="sxs-lookup"><span data-stu-id="06634-118">After these policies are enabled, admins and users will be prompted to register for Azure Multii-Factor authentication.</span></span>

<span data-ttu-id="06634-119">Pour plus d’informations sur ces stratégies, voir [qu’est-ce qu’une stratégie de base](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span><span class="sxs-lookup"><span data-stu-id="06634-119">For more information about these policies, see [What are baseline policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span></span>


## <a name="set-up-baseline-policies"></a><span data-ttu-id="06634-120">Configurer des stratégies de base</span><span class="sxs-lookup"><span data-stu-id="06634-120">Set up baseline policies</span></span>

1. <span data-ttu-id="06634-121">Accédez au [portail Azure](https://portal.azure.com), puis accédez à **Azure Active Directory** \> **accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="06634-121">Go to [Azure portal](https://portal.azure.com), and then navigate to **Azure Active Directory** \> **Conditional Access**.</span></span>
    
    <span data-ttu-id="06634-122">Les stratégies de base sont répertoriées sur la page.</span><span class="sxs-lookup"><span data-stu-id="06634-122">The baseline policies are listed on the page.</span></span> <br/> <br/>
    <span data-ttu-id="06634-123">![Page répertoriant les stratégies de base pour l’accès conditionnel.](media/baslinepolicies.png)</span><span class="sxs-lookup"><span data-stu-id="06634-123">![Page that lists baseline policies for conditional access.](media/baslinepolicies.png)</span></span>
1. <span data-ttu-id="06634-124">Consultez les instructions spécifiques suivantes pour chaque stratégie :</span><span class="sxs-lookup"><span data-stu-id="06634-124">See the following specific instructions for each policy:</span></span>

  - [<span data-ttu-id="06634-125">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="06634-125">Require MFA for admins</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-baseline-protect-administrators)
- [<span data-ttu-id="06634-126">Exiger l’authentification multifacteur pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="06634-126">Require MFA for users</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-baseline-protect-end-users)  
 - [<span data-ttu-id="06634-127">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="06634-127">Block legacy authentication</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-baseline-protect-legacy-auth)
  - [<span data-ttu-id="06634-128">Exiger MFA pour la gestion des services</span><span class="sxs-lookup"><span data-stu-id="06634-128">Require MFA for service management</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-azure)

<span data-ttu-id="06634-129">Vous pouvez configurer de nombreuses stratégies supplémentaires, telles que la nécessité d’applications clientes approuvées.</span><span class="sxs-lookup"><span data-stu-id="06634-129">You can set up many additional policies, such as requiring approved client apps.</span></span> <span data-ttu-id="06634-130">Pour plus d’informations, reportez-vous à la documentation sur l' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/) .</span><span class="sxs-lookup"><span data-stu-id="06634-130">See the [Conditional Access Documentation](https://docs.microsoft.com/azure/active-directory/conditional-access/) for more information.</span></span>