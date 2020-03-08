---
title: Configurer des stratégies d’accès conditionnel pour les campagnes Microsoft 365
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
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment configurer des stratégies d’accès conditionnel pour les campagnes Microsoft 365 afin d’ajouter une sécurité supplémentaire substantielle.
ms.openlocfilehash: eda65e335df2a7c2c443d7095f7b35b5c1cf27e4
ms.sourcegitcommit: 217de0fc54cbeaea32d253f175eaf338cd85f5af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/07/2020
ms.locfileid: "42561217"
---
# <a name="set-up-conditional-access-policies"></a><span data-ttu-id="35704-103">Configurer des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="35704-103">Set up conditional access policies</span></span>

<span data-ttu-id="35704-104">Les stratégies d' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) ajoutent une sécurité supplémentaire importante.</span><span class="sxs-lookup"><span data-stu-id="35704-104">[Conditional access](https://docs.microsoft.com/azure/active-directory/conditional-access/overview) policies add substantial additional security.</span></span> <span data-ttu-id="35704-105">Microsoft fournit un ensemble de stratégies d’accès conditionnel de base qui sont recommandées pour tous les clients.</span><span class="sxs-lookup"><span data-stu-id="35704-105">Microsoft provides a set of baseline conditional access policies that are recommended for all customers.</span></span> <span data-ttu-id="35704-106">Les stratégies de référence sont un ensemble de stratégies prédéfinies qui permettent de protéger les organisations contre de nombreuses attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="35704-106">Baseline policies are a set of predefined policies that help protect organizations against many common attacks.</span></span> <span data-ttu-id="35704-107">Ces attaques courantes peuvent inclure le pulvérisation de mot de passe, la relecture et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="35704-107">These common attacks can include password spray, replay, and phishing.</span></span>

<span data-ttu-id="35704-108">Ces stratégies exigent que les administrateurs et les utilisateurs entrent une deuxième forme d’authentification (appelée authentification multifacteur ou MFA) lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="35704-108">These policies require admins and users to enter a second form of authentication (called multifactor authentication, or MFA) when certain conditions are met.</span></span> <span data-ttu-id="35704-109">Par exemple, si un utilisateur se connecte à partir d’un autre pays, la connexion peut être considérée comme risquée et l’utilisateur doit fournir une forme supplémentaire d’authentification.</span><span class="sxs-lookup"><span data-stu-id="35704-109">For example, if a user is signing in from a different country, the sign-in might be considered risky and the user must provide an additional form of authentication.</span></span> 

<span data-ttu-id="35704-110">Actuellement, les stratégies de base sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="35704-110">Currently, baseline policies include the following:</span></span>
- <span data-ttu-id="35704-111">**Exiger** &ndash; l’authentification multifacteur pour les administrateurs nécessite l’authentification multifacteur pour les rôles d’administrateur les plus privilégiés, y compris l’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="35704-111">**Require MFA for admins** &ndash; Requires multi-factor authentication for the most privileged administrator roles, including global administrator.</span></span>
- <span data-ttu-id="35704-112">La **protection** &ndash; des utilisateurs finaux nécessite une authentification multifacteur pour les utilisateurs uniquement lorsqu’une connexion est risquée.</span><span class="sxs-lookup"><span data-stu-id="35704-112">**End user protection** &ndash; Requires multi-factor authentication for users only when a sign-in is risky.</span></span> 
- <span data-ttu-id="35704-113">**Bloquer l’authentification** &ndash; héritée les anciennes applications clientes et certaines nouvelles applications n’utilisent pas de protocoles d’authentification plus récents et plus sécurisés.</span><span class="sxs-lookup"><span data-stu-id="35704-113">**Block legacy authentication** &ndash; Older client apps and some new apps don't use newer, more secure, authentication protocols.</span></span> <span data-ttu-id="35704-114">Ces anciennes applications peuvent contourner des stratégies d’accès conditionnel et obtenir un accès non autorisé à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="35704-114">These older apps can bypass conditional access policies and gain unauthorized access to your environment.</span></span> <span data-ttu-id="35704-115">Cette stratégie bloque l’accès à partir des clients qui ne prennent pas en charge l’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="35704-115">This policy blocks access from clients that don't support conditional access.</span></span> 
- <span data-ttu-id="35704-116">**Exiger MFA pour la gestion** &ndash; de service nécessite l’authentification multifacteur pour l’accès aux outils de gestion, y compris le portail Azure (où vous configurez les stratégies de base).</span><span class="sxs-lookup"><span data-stu-id="35704-116">**Require MFA for Service Management** &ndash; Requires multi-factor authentication for access to management tools, including Azure portal (where you configure baseline policies).</span></span> 

<span data-ttu-id="35704-117">Microsoft vous recommande d’activer toutes ces stratégies de base.</span><span class="sxs-lookup"><span data-stu-id="35704-117">Microsoft recommends you enable all of these baseline policies.</span></span> <span data-ttu-id="35704-118">Une fois ces stratégies activées, les administrateurs et les utilisateurs sont invités à s’inscrire pour l’authentification Azure Multi-Factor.</span><span class="sxs-lookup"><span data-stu-id="35704-118">After these policies are enabled, admins and users will be prompted to register for Azure Multii-Factor authentication.</span></span>

<span data-ttu-id="35704-119">Pour plus d’informations sur ces stratégies, voir [qu’est-ce qu’une stratégie de base](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span><span class="sxs-lookup"><span data-stu-id="35704-119">For more information about these policies, see [What are baseline policies](https://docs.microsoft.com/azure/active-directory/conditional-access/concept-baseline-protection)?</span></span>


## <a name="set-up-baseline-policies"></a><span data-ttu-id="35704-120">Configurer des stratégies de base</span><span class="sxs-lookup"><span data-stu-id="35704-120">Set up baseline policies</span></span>

1. <span data-ttu-id="35704-121">Accédez au [portail Azure](https://portal.azure.com), puis accédez à **Azure Active Directory** \> **accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="35704-121">Go to [Azure portal](https://portal.azure.com), and then navigate to **Azure Active Directory** \> **Conditional Access**.</span></span>
    
    <span data-ttu-id="35704-122">Les stratégies de base sont répertoriées sur la page.</span><span class="sxs-lookup"><span data-stu-id="35704-122">The baseline policies are listed on the page.</span></span> <br/> <br/>
    <span data-ttu-id="35704-123">![Page répertoriant les stratégies de base pour l’accès conditionnel.](../media/baslinepolicies.png)</span><span class="sxs-lookup"><span data-stu-id="35704-123">![Page that lists baseline policies for conditional access.](../media/baslinepolicies.png)</span></span>
1. <span data-ttu-id="35704-124">Consultez les instructions spécifiques suivantes pour chaque stratégie :</span><span class="sxs-lookup"><span data-stu-id="35704-124">See the following specific instructions for each policy:</span></span>

  - [<span data-ttu-id="35704-125">Exiger l’authentification multifacteur pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="35704-125">Require MFA for admins</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-administrators)
- [<span data-ttu-id="35704-126">Exiger l’authentification multifacteur pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="35704-126">Require MFA for users</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-end-users)  
 - [<span data-ttu-id="35704-127">Bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="35704-127">Block legacy authentication</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-legacy-auth)
  - [<span data-ttu-id="35704-128">Exiger MFA pour la gestion des services</span><span class="sxs-lookup"><span data-stu-id="35704-128">Require MFA for service management</span></span>](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-baseline-protect-azure)

<span data-ttu-id="35704-129">Vous pouvez configurer de nombreuses stratégies supplémentaires, telles que la nécessité d’applications clientes approuvées.</span><span class="sxs-lookup"><span data-stu-id="35704-129">You can set up many additional policies, such as requiring approved client apps.</span></span> <span data-ttu-id="35704-130">Pour plus d’informations, consultez la documentation sur l' [accès conditionnel](https://docs.microsoft.com/azure/active-directory/conditional-access/).</span><span class="sxs-lookup"><span data-stu-id="35704-130">For more information, see the [Conditional Access Documentation](https://docs.microsoft.com/azure/active-directory/conditional-access/).</span></span>
