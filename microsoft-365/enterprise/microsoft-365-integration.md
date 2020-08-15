---
title: Intégration de Microsoft 365 aux environnements locaux
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.date: 10/08/2019
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
ms.openlocfilehash: 46f0fab6396dd1db82524ea1aeedc6894ce7ab70
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690180"
---
# <a name="microsoft-365-integration-with-on-premises-environments"></a><span data-ttu-id="aab22-103">Intégration de Microsoft 365 aux environnements locaux</span><span class="sxs-lookup"><span data-stu-id="aab22-103">Microsoft 365 integration with on-premises environments</span></span>

<span data-ttu-id="aab22-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="aab22-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="aab22-105">Vous pouvez intégrer Microsoft 365 à vos services d’annuaire existants et à une installation locale d’Exchange Server, Skype entreprise Server 2015 ou SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="aab22-105">You can integrate Microsoft 365 with your existing directory services and with an on-premises installation of Exchange Server, Skype for Business Server 2015, or SharePoint Server.</span></span>
  
 - <span data-ttu-id="aab22-106">Lorsque vous intégrez des services d’annuaire, vous pouvez synchroniser et gérer les comptes d’utilisateur pour les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="aab22-106">When you integrate with directory services, you can synchronize and manage user accounts for both environments.</span></span> <span data-ttu-id="aab22-107">Vous pouvez également ajouter la synchronisation de hachage de mot de passe ou l’authentification unique (SSO) de sorte que les utilisateurs puissent se connecter aux deux environnements à l’aide de leurs informations d’identification locales.</span><span class="sxs-lookup"><span data-stu-id="aab22-107">You can also add password hash synchronization or single sign-on (SSO) so users can log on to both environments with their on-premises credentials.</span></span>
 - <span data-ttu-id="aab22-108">Lorsque vous intégrez des produits serveur sur site, vous créez un environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="aab22-108">When you integrate with on-premises server products, you create a hybrid environment.</span></span> <span data-ttu-id="aab22-109">Un environnement hybride peut vous aider lors de la migration des utilisateurs ou des informations vers Microsoft 365, ou vous pouvez continuer à avoir des utilisateurs ou des informations sur site et d’autres dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="aab22-109">A hybrid environment can help as you migrate users or information to Microsoft 365, or you can continue to have some users or some information on-premises and some in the cloud.</span></span> <span data-ttu-id="aab22-110">Pour plus d’informations sur les environnements hybrides, consultez la rubrique [vue d’ensemble du Cloud hybride](https://docs.microsoft.com/Office365/Enterprise/hybrid-cloud-overview).</span><span class="sxs-lookup"><span data-stu-id="aab22-110">For more information about hybrid environments, see [Hybrid cloud overview](https://docs.microsoft.com/Office365/Enterprise/hybrid-cloud-overview).</span></span>

<span data-ttu-id="aab22-111">Vous pouvez également utiliser les conseillers Azure Active Directory (Azure AD) pour obtenir des conseils de configuration personnalisés (vous devez être connecté à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="aab22-111">You can also use the Azure Active Directory (Azure AD) advisors for customized setup guidance (you must be signed in to Microsoft 365):</span></span>

- [<span data-ttu-id="aab22-112">Synchroniser les utilisateurs du répertoire de votre organisation</span><span class="sxs-lookup"><span data-stu-id="aab22-112">Sync users from your org's directory</span></span>](https://aka.ms/aadconnectpwsync)
- [<span data-ttu-id="aab22-113">Conseiller de déploiement AD FS</span><span class="sxs-lookup"><span data-stu-id="aab22-113">AD FS deployment advisor</span></span>](https://aka.ms/adfsguidance)
- [<span data-ttu-id="aab22-114">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="aab22-114">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
   
## <a name="before-you-begin"></a><span data-ttu-id="aab22-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="aab22-115">Before you begin</span></span>

<span data-ttu-id="aab22-116">Avant d’intégrer Microsoft 365 et un environnement local, vous devez également participer à la planification du [réseau et au réglage des performances](network-planning-and-performance.md).</span><span class="sxs-lookup"><span data-stu-id="aab22-116">Before you integrate Microsoft 365 and an on-premises environment, you also need to attend to [network planning and performance tuning](network-planning-and-performance.md).</span></span> <span data-ttu-id="aab22-117">Vous voudrez également comprendre les modèles d' [identité](about-microsoft-365-identity.md)disponibles.</span><span class="sxs-lookup"><span data-stu-id="aab22-117">You will also want to understand the available [identity models](about-microsoft-365-identity.md).</span></span> 

<span data-ttu-id="aab22-118">Consultez la rubrique [où gérer les comptes microsoft 365](manage-microsoft-365-accounts.md) pour obtenir la liste des outils que vous pouvez utiliser pour gérer les utilisateurs et les comptes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aab22-118">See [where to manage Microsoft 365 accounts](manage-microsoft-365-accounts.md) for a list of tools you can use to manage Microsoft 365 users and accounts.</span></span> 
  
## <a name="integrate-microsoft-365-with-directory-services"></a><span data-ttu-id="aab22-119">Intégration de Microsoft 365 avec les services d’annuaire</span><span class="sxs-lookup"><span data-stu-id="aab22-119">Integrate Microsoft 365 with directory services</span></span>
<span data-ttu-id="aab22-120">Si vous avez des comptes d’utilisateur existants dans un annuaire local, vous ne souhaitez pas recréer tous ces comptes dans Microsoft 365 et risquez d’introduire des différences ou des erreurs entre les environnements.</span><span class="sxs-lookup"><span data-stu-id="aab22-120">If you have existing user accounts in an on-premises directory, you don't want to re-create all of those accounts in Microsoft 365 and risk introducing differences or errors between the environments.</span></span> <span data-ttu-id="aab22-121">La synchronisation d’annuaires vous permet de mettre en miroir ces comptes entre vos environnements en ligne et locaux.</span><span class="sxs-lookup"><span data-stu-id="aab22-121">Directory synchronization helps you mirror those accounts between your online and on-premises environments.</span></span> <span data-ttu-id="aab22-122">Avec la synchronisation d’annuaires, vos utilisateurs n’ont pas à se souvenir des nouvelles informations pour chaque environnement, et vous n’avez pas à créer ou mettre à jour les comptes deux fois.</span><span class="sxs-lookup"><span data-stu-id="aab22-122">With directory synchronization, your users don't have to remember new information for each environment, and you don't have to create or update accounts twice.</span></span> <span data-ttu-id="aab22-123">Vous devrez [préparer votre annuaire local pour la](prepare-for-directory-synchronization.md) synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="aab22-123">You will need to [prepare your on-premises directory](prepare-for-directory-synchronization.md) for directory synchronization.</span></span>
  
![Utiliser la synchronisation d’annuaires pour maintenir la synchronisation des informations sur les comptes d’utilisateur en ligne et en ligne](../media/a64af0d0-9be6-46b1-8727-277e683abf5e.png)
  
<span data-ttu-id="aab22-125">Si vous souhaitez que les utilisateurs puissent se connecter à Microsoft 365 avec leurs informations d’identification locales, vous pouvez également configurer l’authentification unique.</span><span class="sxs-lookup"><span data-stu-id="aab22-125">If you want users to be able to log on to Microsoft 365 with their on-premises credentials, you can also configure SSO.</span></span> <span data-ttu-id="aab22-126">Avec l’authentification unique, Microsoft 365 est configuré pour approuver l’environnement local pour l’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="aab22-126">With SSO, Microsoft 365 is configured to trust the on-premises environment for user authentication.</span></span>
  
![Avec l’authentification unique, le même compte est disponible dans les environnements locaux et en ligne.](../media/d76235f2-8a53-405e-b8ef-dfa4cfc208b8.png)
  
<span data-ttu-id="aab22-128">Différentes techniques de gestion de compte d’utilisateur fournissent différentes expériences pour vos utilisateurs, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aab22-128">Different user account management techniques provide different experiences for your users, as shown in the following table.</span></span>
 
### <a name="directory-synchronization-with-or-without-password-hash-synchronization-or-pass-through-authentication"></a><span data-ttu-id="aab22-129">Synchronisation d’annuaires avec ou sans synchronisation de hachage de mot de passe ou authentification directe</span><span class="sxs-lookup"><span data-stu-id="aab22-129">Directory synchronization with or without password hash synchronization or pass-through authentication</span></span>

<span data-ttu-id="aab22-130">Un utilisateur se connecte à son environnement local à l’aide de son compte d’utilisateur (DOMAINE\nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="aab22-130">A user logs on to their on-premises environment with their user account (domain\username).</span></span> <span data-ttu-id="aab22-131">Lorsque les utilisateurs accèdent à Microsoft 365, ils doivent se reconnecter avec leur compte professionnel ou scolaire (user@domain.com).</span><span class="sxs-lookup"><span data-stu-id="aab22-131">When they go to Microsoft 365, they must log on again with their work or school account (user@domain.com).</span></span> <span data-ttu-id="aab22-132">Le nom d’utilisateur est le même dans les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="aab22-132">The user name is the same in both environments.</span></span> <span data-ttu-id="aab22-133">Lorsque vous ajoutez une synchronisation de hachage de mot de passe ou une authentification directe, l’utilisateur a le même mot de passe pour les deux environnements, mais il devra de nouveau fournir ces informations d’identification lors de la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="aab22-133">When you add password hash sync or pass-through authentication, the user has the same password for both environments, but will have to provide those credentials again when logging on to Microsoft 365.</span></span> <span data-ttu-id="aab22-134">La synchronisation d’annuaires avec la synchronisation de hachage de mot de passe est le scénario de synchronisation d’annuaire le plus couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="aab22-134">Directory synchronization with password hash sync is the most commonly used directory sync scenario.</span></span>

<span data-ttu-id="aab22-135">Pour configurer la synchronisation d’annuaires, utilisez Azure Active Directory Connect.</span><span class="sxs-lookup"><span data-stu-id="aab22-135">To set up directory synchronization, use Azure Active Directory Connect.</span></span> <span data-ttu-id="aab22-136">Pour obtenir des instructions, consultez la section [configuration de la synchronisation d’annuaires pour Microsoft 365](set-up-directory-synchronization.md)et [Azure ad Connect with Express Settings](https://go.microsoft.com/fwlink/p/?LinkId=698537).</span><span class="sxs-lookup"><span data-stu-id="aab22-136">For instructions, read [Set up directory synchronization for Microsoft 365](set-up-directory-synchronization.md), and [Azure AD Connect with express settings](https://go.microsoft.com/fwlink/p/?LinkId=698537).</span></span>

<span data-ttu-id="aab22-137">En savoir plus sur la [préparation de la synchronisation d’annuaires avec Microsoft 365](prepare-for-directory-synchronization.md) et [l’intégration de vos identifications locales à Azure Active Directory](https://go.microsoft.com/fwlink/?LinkId=518101).</span><span class="sxs-lookup"><span data-stu-id="aab22-137">Learn more about [preparing for directory synchronization to Microsoft 365](prepare-for-directory-synchronization.md) and [integrating your on-premises identifies with Azure Active Directory](https://go.microsoft.com/fwlink/?LinkId=518101).</span></span>

### <a name="directory-synchronization-with-sso"></a><span data-ttu-id="aab22-138">Synchronisation d’annuaires avec SSO</span><span class="sxs-lookup"><span data-stu-id="aab22-138">Directory synchronization with SSO</span></span>

<span data-ttu-id="aab22-139">Un utilisateur se connecte à son environnement local à l’aide de son compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aab22-139">A user logs on to their on-premises environment with their user account.</span></span> <span data-ttu-id="aab22-140">Lorsque les utilisateurs accèdent à Microsoft 365, ils se connectent automatiquement ou se connectent à l’aide des mêmes informations d’identification qu’ils utilisent pour leur environnement local (DOMAINE\nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="aab22-140">When they go to Microsoft 365, they are either logged on automatically, or they log on using the same credentials they use for their on-premises environment (domain\username).</span></span>

<span data-ttu-id="aab22-141">Pour configurer l’authentification unique, vous devez également utiliser Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="aab22-141">To set up SSO you also use Azure AD Connect.</span></span> <span data-ttu-id="aab22-142">Pour obtenir des instructions, consultez [l’installation personnalisée d’Azure ad Connect](https://go.microsoft.com/fwlink/p/?LinkID=698430).</span><span class="sxs-lookup"><span data-stu-id="aab22-142">For instructions, read [Custom installation of Azure AD Connect](https://go.microsoft.com/fwlink/p/?LinkID=698430).</span></span>

<span data-ttu-id="aab22-143">En savoir plus sur [l’authentification unique pour les applications dans Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span><span class="sxs-lookup"><span data-stu-id="aab22-143">Learn more about [single sign-on to applications in Azure Active Directory](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span></span>

## <a name="azure-ad-connect"></a><span data-ttu-id="aab22-144">Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="aab22-144">Azure AD Connect</span></span>

<span data-ttu-id="aab22-145">Azure AD Connect remplace les anciennes versions des outils d’intégration des identités telles que DirSync et Azure AD Sync. Pour plus d’informations, voir [qu’est-ce que l’identité hybride avec Azure Active Directory ?](https://go.microsoft.com/fwlink/p/?LinkId=527969).</span><span class="sxs-lookup"><span data-stu-id="aab22-145">Azure AD Connect replaces older versions of identity integration tools such as DirSync and Azure AD Sync. For more information, see [What is hybrid identity with Azure Active Directory?](https://go.microsoft.com/fwlink/p/?LinkId=527969).</span></span> <span data-ttu-id="aab22-146">Si vous souhaitez effectuer une mise à jour à partir d’Azure Active Directory Sync vers Azure AD Connect, consultez [les instructions de mise à niveau](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span><span class="sxs-lookup"><span data-stu-id="aab22-146">If you want to update from Azure Active Directory Sync to Azure AD Connect, see [the upgrade instructions](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span></span> 

<span data-ttu-id="aab22-147">Consultez également la rubrique [Deploy microsoft 365 Directory Synchronization in Microsoft Azure](https://go.microsoft.com/fwlink/?LinkId=517887).</span><span class="sxs-lookup"><span data-stu-id="aab22-147">Also see [Deploy Microsoft 365 Directory Synchronization in Microsoft Azure](https://go.microsoft.com/fwlink/?LinkId=517887).</span></span>

## <a name="see-also"></a><span data-ttu-id="aab22-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aab22-148">See also</span></span>

[<span data-ttu-id="aab22-149">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="aab22-149">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
