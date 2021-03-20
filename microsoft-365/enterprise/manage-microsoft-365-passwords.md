---
title: Gérer les mots de passe de compte d’utilisateur Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-mar2020
ms.collection:
- Ent_O365
- M365-subscription-management
search.appverid:
- MET150
- MOE150
- MED150
- BCS160
ms.assetid: 98ca5b3f-f720-4d8e-91be-fe656548a25a
description: Découvrez comment gérer les mots de passe de compte d’utilisateur Microsoft 365.
ms.openlocfilehash: 2062da49310121ec18f7ce21f523531f10d6df9b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50905091"
---
# <a name="manage-microsoft-365-user-account-passwords"></a><span data-ttu-id="3824d-103">Gérer les mots de passe de compte d’utilisateur Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3824d-103">Manage Microsoft 365 user account passwords</span></span>

<span data-ttu-id="3824d-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="3824d-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="3824d-105">Vous pouvez gérer les mots de passe de compte d’utilisateur Microsoft 365 de différentes manières, en fonction de la configuration de votre identité.</span><span class="sxs-lookup"><span data-stu-id="3824d-105">You can manage Microsoft 365 user account passwords in several different ways, depending on your identity configuration.</span></span> <span data-ttu-id="3824d-106">Vous pouvez gérer les comptes d’utilisateurs dans le Centre d’administration [Microsoft 365,](../admin/add-users/index.yml)dans les services de domaine Active Directory (AD DS) ou dans le Centre d’administration Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3824d-106">You can manage user accounts in the [Microsoft 365 admin center](../admin/add-users/index.yml), in Active Directory Domain Services (AD DS), or in the Azure Active Directory (Azure AD) admin center.</span></span>

## <a name="plan-for-where-and-how-you-will-manage-your-user-account-passwords"></a><span data-ttu-id="3824d-107">Planifier l’endroit et la façon dont vous allez gérer les mots de passe de votre compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="3824d-107">Plan for where and how you will manage your user account passwords</span></span>

<span data-ttu-id="3824d-108">L’endroit où et comment vous pouvez gérer vos comptes d’utilisateur dépend du modèle d’identité que vous souhaitez utiliser pour votre Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3824d-108">Where and how you can manage your user accounts depends on the identity model you want to use for your Microsoft 365.</span></span> <span data-ttu-id="3824d-109">Les deux modèles sont uniquement cloud et hybrides.</span><span class="sxs-lookup"><span data-stu-id="3824d-109">The two models are cloud-only and hybrid.</span></span>
  
### <a name="cloud-only"></a><span data-ttu-id="3824d-110">Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="3824d-110">Cloud-only</span></span>

<span data-ttu-id="3824d-111">Vous gérez les mots de passe de compte d’utilisateur dans :</span><span class="sxs-lookup"><span data-stu-id="3824d-111">You manage user account passwords in:</span></span>

- [<span data-ttu-id="3824d-112">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3824d-112">The Microsoft 365 admin center</span></span>](../admin/add-users/index.yml)
- <span data-ttu-id="3824d-113">Centre d’administration Azure AD</span><span class="sxs-lookup"><span data-stu-id="3824d-113">The Azure AD admin center</span></span>
    
### <a name="hybrid"></a><span data-ttu-id="3824d-114">Hybride</span><span class="sxs-lookup"><span data-stu-id="3824d-114">Hybrid</span></span>

<span data-ttu-id="3824d-115">Avec l’identité hybride, les mots de passe sont stockés dans AD DS. Vous devez donc utiliser les outils AD DS locaux pour gérer les mots de passe de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3824d-115">With hybrid identity, passwords are stored in AD DS so you must use on-premises AD DS tools to manage user account passwords.</span></span> <span data-ttu-id="3824d-116">Même lors de l’utilisation de la synchronisation de hachage de mot de passe (PHS), dans laquelle Azure AD stocke une version hachée de la version déjà hachée dans AD DS, vous et les utilisateurs devez gérer leurs mots de passe dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="3824d-116">Even when using Password Hash Synchronization (PHS), in which Azure AD stores a hashed version of the already hashed version in AD DS, you and users must manage their passwords in AD DS.</span></span>

<span data-ttu-id="3824d-117">Avec [l’écriture écriture par](#pw_writeback)mot de passe, vos utilisateurs peuvent modifier leurs mots de passe AD DS via Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3824d-117">With [password writeback](#pw_writeback), your users can change their AD DS passwords through Azure AD.</span></span>

## <a name="prevent-bad-passwords"></a><span data-ttu-id="3824d-118">Éviter les mots de passe incorrects</span><span class="sxs-lookup"><span data-stu-id="3824d-118">Prevent bad passwords</span></span>

<span data-ttu-id="3824d-119">Tous vos utilisateurs doivent utiliser le [guide des mots de passe Microsoft](https://www.microsoft.com/research/publication/password-guidance) pour créer leurs mots de passe de compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3824d-119">All your users should be using [Microsoft's password guidance](https://www.microsoft.com/research/publication/password-guidance) to create their user account passwords.</span></span>

<span data-ttu-id="3824d-120">Pour empêcher les utilisateurs de créer un mot de passe facile à déterminer, optez pour la protection par mot de passe Azure AD qui utilise une liste globale de mots de passe interdits et une liste personnalisée facultative de mots de passe interdits que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="3824d-120">To prevent users from creating an easily-determined password, use Azure AD password protection, which uses both a global banned password list and an optional custom banned password list that you specify.</span></span> <span data-ttu-id="3824d-121">Par exemple, vous pouvez spécifier des termes propres à votre organisation, tels que :</span><span class="sxs-lookup"><span data-stu-id="3824d-121">For example, you can specify terms that are specific to your organization, such as:</span></span>

- <span data-ttu-id="3824d-122">Noms de marques</span><span class="sxs-lookup"><span data-stu-id="3824d-122">Brand names</span></span>
- <span data-ttu-id="3824d-123">Noms de produits</span><span class="sxs-lookup"><span data-stu-id="3824d-123">Product names</span></span>
- <span data-ttu-id="3824d-124">Emplacements (par exemple, le siège social de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="3824d-124">Locations (for example, such as company headquarters)</span></span>
- <span data-ttu-id="3824d-125">Termes internes spécifiques à l’entreprise</span><span class="sxs-lookup"><span data-stu-id="3824d-125">Company-specific internal terms</span></span>
- <span data-ttu-id="3824d-126">Abréviations dotées d’une signification spécifique à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3824d-126">Abbreviations that have specific company meaning</span></span>

<span data-ttu-id="3824d-127">Vous pouvez interdire les mots de passe incorrects dans [le cloud](/azure/active-directory/authentication/concept-password-ban-bad) et pour vos [services AD DS locaux.](/azure/active-directory/authentication/concept-password-ban-bad-on-premises)</span><span class="sxs-lookup"><span data-stu-id="3824d-127">You can ban bad passwords [in the cloud](/azure/active-directory/authentication/concept-password-ban-bad) and for your [on-premises AD DS](/azure/active-directory/authentication/concept-password-ban-bad-on-premises).</span></span>

## <a name="simplify-user-sign-in"></a><span data-ttu-id="3824d-128">Simplifiez la connexion utilisateur</span><span class="sxs-lookup"><span data-stu-id="3824d-128">Simplify user sign-in</span></span>

<span data-ttu-id="3824d-129">Azure AD Seamless Single Sign-On (Azure AD Seamless SSO) fonctionne avec PHS et l’authentification Pass-Through (PTA), pour permettre à vos utilisateurs de se connecter à des services qui utilisent des comptes d’utilisateur Azure AD sans avoir à taper leur mot de passe et, dans de nombreux cas, leur nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3824d-129">Azure AD Seamless Single Sign-On (Azure AD Seamless SSO) works with PHS and Pass-Through Authentication (PTA), to allow your users to sign in to services that use Azure AD user accounts without having to type in their passwords, and in many cases, their usernames.</span></span> <span data-ttu-id="3824d-130">Cela donne à vos utilisateurs un accès facile aux applications basées sur le cloud, telles qu’Office 365, sans nécessiter des composants supplémentaires en local, tels que des serveurs de fédération d’identité.</span><span class="sxs-lookup"><span data-stu-id="3824d-130">This gives your users easier access to cloud-based applications, such as Office 365, without needing any additional on-premises components such as identity federation servers.</span></span>

<span data-ttu-id="3824d-131">Vous configurez l’authentification unique transparente Azure AD avec l’outil Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="3824d-131">You configure Azure AD Seamless SSO with the Azure AD Connect tool.</span></span> <span data-ttu-id="3824d-132">Reportez-vous aux [instructions pour configurer l’authentification unique transparente d’Azure AD](/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span><span class="sxs-lookup"><span data-stu-id="3824d-132">See the [instructions to configure Azure AD Seamless SSO](/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span></span>

<a name="pw_writeback"></a>
## <a name="simplify-password-updates-to-ad-ds"></a><span data-ttu-id="3824d-133">Simplifier les mises à jour de mot de passe pour AD DS</span><span class="sxs-lookup"><span data-stu-id="3824d-133">Simplify password updates to AD DS</span></span>

<span data-ttu-id="3824d-134">Avec la réinitialisation du mot de passe, vous pouvez autoriser les utilisateurs à réinitialiser leur mot de passe via Azure AD, qui est ensuite répliqué dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="3824d-134">With password writeback, you can allow users to reset their passwords through Azure AD, which is then replicated to AD DS.</span></span> <span data-ttu-id="3824d-135">Les utilisateurs n’ont pas besoin d’accéder à leurs services AD DS locaux pour mettre à jour leurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="3824d-135">Users don’t need to access their on-premises AD DS to update their passwords.</span></span> <span data-ttu-id="3824d-136">C’est utile pour les utilisateurs itinérants ou distants qui ne possèdent pas de connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="3824d-136">This is valuable to roaming or remote users who do not have a remote access connection to the on-premises network.</span></span>

<span data-ttu-id="3824d-137">L’écriture différée de mot de passe est requise pour exploiter pleinement les fonctionnalités Azure AD Identity Protection, comme obliger les utilisateurs à modifier leur mot de passe en local lorsqu’un risque élevé de compromission de compte a été détecté.</span><span class="sxs-lookup"><span data-stu-id="3824d-137">Password writeback is required to fully utilize Azure AD Identity Protection capabilities, such as requiring users to change their on-premises passwords when there has been a high risk of account compromise detected.</span></span>

<span data-ttu-id="3824d-138">Pour obtenir plus d’informations et les instructions de configuration, consultez l’article [Azure AD SSPR avec l’écriture différée de mot de passe](/azure/active-directory/active-directory-passwords-writeback).</span><span class="sxs-lookup"><span data-stu-id="3824d-138">For additional information and configuration instructions, see [Azure AD SSPR with password writeback](/azure/active-directory/active-directory-passwords-writeback).</span></span>

>[!Note]
><span data-ttu-id="3824d-p108">Procédez à la mise à niveau vers la dernière version d’Azure AD Connect pour vous assurer la meilleure expérience possible et les nouvelles fonctionnalités dès leur diffusion. Pour obtenir plus d’informations, consultez l’article [Installation personnalisée d’Azure AD Connect](/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span><span class="sxs-lookup"><span data-stu-id="3824d-p108">Upgrade to the latest version of Azure AD Connect to ensure the best possible experience and new features as they are released. For more information, see [Custom installation of Azure AD Connect](/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span></span>
>

## <a name="simplify-password-resets"></a><span data-ttu-id="3824d-141">Simplifiez les réinitialisations du mot de passe</span><span class="sxs-lookup"><span data-stu-id="3824d-141">Simplify password resets</span></span>

<span data-ttu-id="3824d-142">La réinitialisation du mot de passe en libre-service (SSPR) permet aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou comptes.</span><span class="sxs-lookup"><span data-stu-id="3824d-142">Self-service password reset (SSPR) allows users to reset or unlock their passwords or accounts.</span></span> <span data-ttu-id="3824d-143">Le système inclut des rapports détaillés de suivi d’accès au système, ainsi que des notifications pour vous prévenir de toute utilisation malveillante ou de tout abus.</span><span class="sxs-lookup"><span data-stu-id="3824d-143">To alert you to misuse or abuse, you can use the detailed reporting that tracks when users access the system, along with notifications.</span></span> <span data-ttu-id="3824d-144">Vous devez activer la [réinitialisation du mot de](#pw_writeback) passe avant de pouvoir déployer les réinitialisations de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3824d-144">You must enable [password writeback](#pw_writeback) before you can deploy password resets.</span></span>

<span data-ttu-id="3824d-145">Reportez-vous aux [Instructions pour activer la réinitialisation de mot de passe](/azure/active-directory/authentication/howto-sspr-deployment).</span><span class="sxs-lookup"><span data-stu-id="3824d-145">See the [instructions to roll out password reset](/azure/active-directory/authentication/howto-sspr-deployment).</span></span>