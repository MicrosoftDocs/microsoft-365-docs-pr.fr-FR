---
title: Intégration de Microsoft 365 aux environnements locaux
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.collection:
- Ent_O365
search.appverid:
- MET150
- LYN150
- SPS150
- MOE150
- MED150
ms.assetid: 263faf8d-aa21-428b-aed3-2021837a4b65
description: Dans cet article, Découvrez comment intégrer Microsoft 365 avec vos services d’annuaire et environnements locaux existants.
ms.openlocfilehash: 9c5e287ed4a440d1f62081a4c94e39f0f162b4dc
ms.sourcegitcommit: 11d1044c6600b1f568b6dc8a53db9b07f2f0ad1c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48384867"
---
# <a name="microsoft-365-integration-with-on-premises-environments"></a><span data-ttu-id="c825b-103">Intégration de Microsoft 365 aux environnements locaux</span><span class="sxs-lookup"><span data-stu-id="c825b-103">Microsoft 365 integration with on-premises environments</span></span>

<span data-ttu-id="c825b-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="c825b-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="c825b-105">Vous pouvez intégrer Microsoft 365 à vos services de domaine Active Directory (AD DS) locaux existants et aux installations locales d’Exchange Server, Skype entreprise Server 2015 ou SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="c825b-105">You can integrate Microsoft 365 with your existing on-premises Active Directory Domain Services (AD DS) and with on-premises installations of Exchange Server, Skype for Business Server 2015, or SharePoint Server.</span></span>
  
 - <span data-ttu-id="c825b-106">Lorsque vous intégrez les services AD DS, vous pouvez synchroniser et gérer les comptes d’utilisateur pour les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="c825b-106">When you integrate AD DS, you can synchronize and manage user accounts for both environments.</span></span> <span data-ttu-id="c825b-107">Vous pouvez également ajouter la synchronisation de hachage de mot de passe (hachage) ou l’authentification unique (SSO) de sorte que les utilisateurs puissent se connecter aux deux environnements à l’aide de leurs informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="c825b-107">You can also add password hash synchronization (PHS) or single sign-on (SSO) so users can log on to both environments with their on-premises credentials.</span></span>
 - <span data-ttu-id="c825b-108">Lorsque vous intégrez des produits serveur sur site, vous créez un environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="c825b-108">When you integrate with on-premises server products, you create a hybrid environment.</span></span> <span data-ttu-id="c825b-109">Un environnement hybride peut vous aider lors de la migration des utilisateurs ou des informations vers Microsoft 365, ou vous pouvez continuer à avoir des utilisateurs ou des informations sur site et d’autres dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="c825b-109">A hybrid environment can help as you migrate users or information to Microsoft 365, or you can continue to have some users or some information on-premises and some in the cloud.</span></span> <span data-ttu-id="c825b-110">Pour plus d’informations sur les environnements hybrides, consultez la rubrique [Cloud hybride](../solutions/cloud-architecture-models.md#hybrid).</span><span class="sxs-lookup"><span data-stu-id="c825b-110">For more information about hybrid environments, see [hybrid cloud](../solutions/cloud-architecture-models.md#hybrid).</span></span>

<span data-ttu-id="c825b-111">Vous pouvez également utiliser les conseillers Azure Active Directory (Azure AD) pour obtenir des instructions de configuration personnalisées dans le centre d’administration 365 de Microsoft (vous devez être connecté à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="c825b-111">You can also use the Azure Active Directory (Azure AD) advisors for customized setup guidance in the Microsoft 365 admin center (you must be signed in to Microsoft 365):</span></span>

- [<span data-ttu-id="c825b-112">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="c825b-112">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
- [<span data-ttu-id="c825b-113">Synchroniser les utilisateurs du répertoire de votre organisation</span><span class="sxs-lookup"><span data-stu-id="c825b-113">Sync users from your org's directory</span></span>](https://aka.ms/aadconnectpwsync)
- [<span data-ttu-id="c825b-114">Gestionnaire de déploiement des services ADFS (Active Directory Federation Services)</span><span class="sxs-lookup"><span data-stu-id="c825b-114">Active Directory Federation Services (AD FS) deployment advisor</span></span>](https://aka.ms/adfsguidance)
   
## <a name="before-you-begin"></a><span data-ttu-id="c825b-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c825b-115">Before you begin</span></span>

<span data-ttu-id="c825b-116">Avant d’intégrer Microsoft 365 et un environnement local, vous devez également effectuer une planification du [réseau et un réglage des performances](network-planning-and-performance.md).</span><span class="sxs-lookup"><span data-stu-id="c825b-116">Before you integrate Microsoft 365 and an on-premises environment, you also need to do [network planning and performance tuning](network-planning-and-performance.md).</span></span> <span data-ttu-id="c825b-117">Vous voudrez également comprendre les modèles d' [identité](about-microsoft-365-identity.md)disponibles.</span><span class="sxs-lookup"><span data-stu-id="c825b-117">You will also want to understand the available [identity models](about-microsoft-365-identity.md).</span></span> 

<span data-ttu-id="c825b-118">Consultez la rubrique [Manage microsoft 365 Accounts](manage-microsoft-365-accounts.md) pour obtenir la liste des outils que vous pouvez utiliser pour gérer les comptes d’utilisateur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c825b-118">See [manage Microsoft 365 accounts](manage-microsoft-365-accounts.md) for a list of tools you can use to manage Microsoft 365 user accounts.</span></span> 
  
## <a name="integrate-microsoft-365-with-ad-ds"></a><span data-ttu-id="c825b-119">Intégration de Microsoft 365 à AD DS</span><span class="sxs-lookup"><span data-stu-id="c825b-119">Integrate Microsoft 365 with AD DS</span></span>

<span data-ttu-id="c825b-120">Si vous avez des comptes d’utilisateur existants dans AD DS, vous ne souhaitez pas recréer tous ces comptes dans Microsoft 365 et risquez d’introduire des différences ou des erreurs entre les environnements.</span><span class="sxs-lookup"><span data-stu-id="c825b-120">If you have existing user accounts in AD DS, you don't want to re-create all of those accounts in Microsoft 365 and risk introducing differences or errors between the environments.</span></span> <span data-ttu-id="c825b-121">La synchronisation d’annuaires vous permet de mettre en miroir ces comptes entre vos environnements locaux et en ligne.</span><span class="sxs-lookup"><span data-stu-id="c825b-121">Directory synchronization helps you mirror those accounts between your on-premises and online environments.</span></span> <span data-ttu-id="c825b-122">Avec la synchronisation d’annuaires, vos utilisateurs n’ont pas à se souvenir des nouvelles informations pour chaque environnement, et vous n’avez pas à créer ou mettre à jour les comptes deux fois.</span><span class="sxs-lookup"><span data-stu-id="c825b-122">With directory synchronization, your users don't have to remember new information for each environment, and you don't have to create or update accounts twice.</span></span> <span data-ttu-id="c825b-123">Vous devrez [préparer votre annuaire local pour la](prepare-for-directory-synchronization.md) synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="c825b-123">You will need to [prepare your on-premises directory](prepare-for-directory-synchronization.md) for directory synchronization.</span></span>
  
![Utiliser la synchronisation d’annuaires pour maintenir la synchronisation des informations sur les comptes d’utilisateur en ligne et en ligne](../media/microsoft-365-integration/directory-synchronization.png)
  
<span data-ttu-id="c825b-125">Si vous souhaitez que les utilisateurs puissent se connecter à Microsoft 365 avec leurs informations d’identification locales, vous pouvez également configurer l’authentification unique.</span><span class="sxs-lookup"><span data-stu-id="c825b-125">If you want users to be able to log on to Microsoft 365 with their on-premises credentials, you can also configure SSO.</span></span> <span data-ttu-id="c825b-126">Avec l’authentification unique, Microsoft 365 est configuré pour approuver l’environnement local pour l’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c825b-126">With SSO, Microsoft 365 is configured to trust the on-premises environment for user authentication.</span></span>
  
![Avec l’authentification unique, le même compte est disponible dans les environnements locaux et en ligne.](../media/microsoft-365-integration/single-sign-on.png)

### <a name="directory-synchronization-with-or-without-password-hash-synchronization-or-pass-through-authentication-pta"></a><span data-ttu-id="c825b-128">Synchronisation d’annuaires avec ou sans synchronisation de hachage de mot de passe ou authentification directe (directe)</span><span class="sxs-lookup"><span data-stu-id="c825b-128">Directory synchronization with or without password hash synchronization or pass-through authentication (PTA)</span></span>

<span data-ttu-id="c825b-129">Un utilisateur se connecte à son environnement local à l’aide de son compte d’utilisateur (DOMAINE\nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c825b-129">A user logs on to their on-premises environment with their user account (domain\username).</span></span> <span data-ttu-id="c825b-130">Lorsque les utilisateurs accèdent à Microsoft 365, ils doivent se reconnecter avec leur compte professionnel ou scolaire (user@domain.com).</span><span class="sxs-lookup"><span data-stu-id="c825b-130">When they go to Microsoft 365, they must log on again with their work or school account (user@domain.com).</span></span> <span data-ttu-id="c825b-131">Le nom d’utilisateur est le même dans les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="c825b-131">The user name is the same in both environments.</span></span> <span data-ttu-id="c825b-132">Lorsque vous ajoutez hachage ou directe, l’utilisateur a le même mot de passe pour les deux environnements, mais il devra de nouveau fournir ces informations d’identification lors de la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c825b-132">When you add PHS or PTA, the user has the same password for both environments, but will have to provide those credentials again when logging on to Microsoft 365.</span></span> <span data-ttu-id="c825b-133">La synchronisation d’annuaires avec hachage est la synchronisation d’annuaires la plus couramment utilisée.</span><span class="sxs-lookup"><span data-stu-id="c825b-133">Directory synchronization with PHS is the most commonly used directory synchronization .</span></span>

<span data-ttu-id="c825b-134">Pour configurer la synchronisation d’annuaires, utilisez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="c825b-134">To set up directory synchronization, use Azure AD Connect.</span></span> <span data-ttu-id="c825b-135">Pour obtenir des instructions, consultez la rubrique [configurer la synchronisation d’annuaires pour Microsoft 365](set-up-directory-synchronization.md) et [Azure ad Connect with Express Settings](https://go.microsoft.com/fwlink/p/?LinkId=698537).</span><span class="sxs-lookup"><span data-stu-id="c825b-135">For instructions, see [Set up directory synchronization for Microsoft 365](set-up-directory-synchronization.md) and [Azure AD Connect with express settings](https://go.microsoft.com/fwlink/p/?LinkId=698537).</span></span>

<span data-ttu-id="c825b-136">Pour en savoir plus, consultez la rubrique relative [à la préparation de la synchronisation d’annuaires avec Microsoft 365](prepare-for-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="c825b-136">Learn more about [preparing for directory synchronization to Microsoft 365](prepare-for-directory-synchronization.md).</span></span>

### <a name="directory-synchronization-with-sso"></a><span data-ttu-id="c825b-137">Synchronisation d’annuaires avec SSO</span><span class="sxs-lookup"><span data-stu-id="c825b-137">Directory synchronization with SSO</span></span>

<span data-ttu-id="c825b-138">Un utilisateur se connecte à son environnement local à l’aide de son compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c825b-138">A user logs on to their on-premises environment with their user account.</span></span> <span data-ttu-id="c825b-139">Lorsque les utilisateurs accèdent à Microsoft 365, ils se connectent automatiquement ou se connectent à l’aide des mêmes informations d’identification qu’ils utilisent pour leur environnement local (DOMAINE\nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c825b-139">When they go to Microsoft 365, they are either logged on automatically, or they log on using the same credentials they use for their on-premises environment (domain\username).</span></span>

<span data-ttu-id="c825b-140">Pour configurer l’authentification unique, vous devez également utiliser Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="c825b-140">To set up SSO you also use Azure AD Connect.</span></span> <span data-ttu-id="c825b-141">Pour obtenir des instructions, voir [installation personnalisée d’Azure ad Connect](https://go.microsoft.com/fwlink/p/?LinkID=698430).</span><span class="sxs-lookup"><span data-stu-id="c825b-141">For instructions, see [Custom installation of Azure AD Connect](https://go.microsoft.com/fwlink/p/?LinkID=698430).</span></span>

<span data-ttu-id="c825b-142">Pour plus d’informations, consultez la rubrique [authentification unique](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span><span class="sxs-lookup"><span data-stu-id="c825b-142">For more information, see [single sign-on](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span></span>

## <a name="azure-ad-connect"></a><span data-ttu-id="c825b-143">Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="c825b-143">Azure AD Connect</span></span>

<span data-ttu-id="c825b-144">Azure AD Connect remplace les anciennes versions des outils d’intégration des identités telles que DirSync et Azure AD Sync. Si vous souhaitez effectuer une mise à jour à partir d’Azure Active Directory Sync vers Azure AD Connect, consultez [les instructions de mise à niveau](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span><span class="sxs-lookup"><span data-stu-id="c825b-144">Azure AD Connect replaces older versions of identity integration tools such as DirSync and Azure AD Sync. If you want to update from Azure Active Directory Sync to Azure AD Connect, see [the upgrade instructions](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span></span> 

## <a name="see-also"></a><span data-ttu-id="c825b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c825b-145">See also</span></span>

[<span data-ttu-id="c825b-146">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c825b-146">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
