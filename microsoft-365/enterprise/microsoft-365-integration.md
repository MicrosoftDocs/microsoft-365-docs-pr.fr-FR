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
description: Dans cet article, découvrez comment intégrer Microsoft 365 à vos services d’annuaire et environnements locaux existants.
ms.openlocfilehash: 9c5e287ed4a440d1f62081a4c94e39f0f162b4dc
ms.sourcegitcommit: 11d1044c6600b1f568b6dc8a53db9b07f2f0ad1c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2020
ms.locfileid: "48384867"
---
# <a name="microsoft-365-integration-with-on-premises-environments"></a><span data-ttu-id="63988-103">Intégration de Microsoft 365 aux environnements locaux</span><span class="sxs-lookup"><span data-stu-id="63988-103">Microsoft 365 integration with on-premises environments</span></span>

<span data-ttu-id="63988-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="63988-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="63988-105">Vous pouvez intégrer Microsoft 365 à vos services de domaine Active Directory (AD DS) locaux existants et aux installations sur site de Exchange Server, Skype Entreprise Server 2015 ou SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="63988-105">You can integrate Microsoft 365 with your existing on-premises Active Directory Domain Services (AD DS) and with on-premises installations of Exchange Server, Skype for Business Server 2015, or SharePoint Server.</span></span>
  
 - <span data-ttu-id="63988-106">Lorsque vous intégrez AD DS, vous pouvez synchroniser et gérer les comptes d’utilisateur pour les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="63988-106">When you integrate AD DS, you can synchronize and manage user accounts for both environments.</span></span> <span data-ttu-id="63988-107">Vous pouvez également ajouter une synchronisation de hachage de mot de passe (PHS) ou une personnalisation unique (SSO) pour que les utilisateurs se connectent aux deux environnements avec leurs informations d’identification sur site.</span><span class="sxs-lookup"><span data-stu-id="63988-107">You can also add password hash synchronization (PHS) or single sign-on (SSO) so users can log on to both environments with their on-premises credentials.</span></span>
 - <span data-ttu-id="63988-108">Lorsque vous intégrez des produits serveur locaux, vous créez un environnement hybride.</span><span class="sxs-lookup"><span data-stu-id="63988-108">When you integrate with on-premises server products, you create a hybrid environment.</span></span> <span data-ttu-id="63988-109">Un environnement hybride peut vous aider lorsque vous migrez des utilisateurs ou des informations vers Microsoft 365, ou vous pouvez continuer à avoir des utilisateurs ou des informations sur site et d’autres dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="63988-109">A hybrid environment can help as you migrate users or information to Microsoft 365, or you can continue to have some users or some information on-premises and some in the cloud.</span></span> <span data-ttu-id="63988-110">Pour plus d’informations sur les environnements hybrides, voir [le cloud hybride.](../solutions/cloud-architecture-models.md#hybrid)</span><span class="sxs-lookup"><span data-stu-id="63988-110">For more information about hybrid environments, see [hybrid cloud](../solutions/cloud-architecture-models.md#hybrid).</span></span>

<span data-ttu-id="63988-111">Vous pouvez également utiliser les conseillers Azure Active Directory (Azure AD) pour obtenir des conseils de configuration personnalisés dans le Centre d’administration Microsoft 365 (vous devez être inscrit à Microsoft 365) :</span><span class="sxs-lookup"><span data-stu-id="63988-111">You can also use the Azure Active Directory (Azure AD) advisors for customized setup guidance in the Microsoft 365 admin center (you must be signed in to Microsoft 365):</span></span>

- [<span data-ttu-id="63988-112">Guide de configuration d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="63988-112">Azure AD setup guide</span></span>](https://aka.ms/aadpguidance)
- [<span data-ttu-id="63988-113">Synchroniser les utilisateurs à partir de l’annuaire de votre organisation</span><span class="sxs-lookup"><span data-stu-id="63988-113">Sync users from your org's directory</span></span>](https://aka.ms/aadconnectpwsync)
- [<span data-ttu-id="63988-114">Conseiller en déploiement des services AD FS (Active Directory Federation Services)</span><span class="sxs-lookup"><span data-stu-id="63988-114">Active Directory Federation Services (AD FS) deployment advisor</span></span>](https://aka.ms/adfsguidance)
   
## <a name="before-you-begin"></a><span data-ttu-id="63988-115">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="63988-115">Before you begin</span></span>

<span data-ttu-id="63988-116">Avant d’intégrer Microsoft 365 et un environnement local, vous devez également planifier le réseau et régler les [performances.](network-planning-and-performance.md)</span><span class="sxs-lookup"><span data-stu-id="63988-116">Before you integrate Microsoft 365 and an on-premises environment, you also need to do [network planning and performance tuning](network-planning-and-performance.md).</span></span> <span data-ttu-id="63988-117">Vous souhaitez également comprendre les modèles [d’identité disponibles.](about-microsoft-365-identity.md)</span><span class="sxs-lookup"><span data-stu-id="63988-117">You will also want to understand the available [identity models](about-microsoft-365-identity.md).</span></span> 

<span data-ttu-id="63988-118">Consultez [gérer les comptes Microsoft 365](manage-microsoft-365-accounts.md) pour obtenir la liste des outils que vous pouvez utiliser pour gérer les comptes d’utilisateurs Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63988-118">See [manage Microsoft 365 accounts](manage-microsoft-365-accounts.md) for a list of tools you can use to manage Microsoft 365 user accounts.</span></span> 
  
## <a name="integrate-microsoft-365-with-ad-ds"></a><span data-ttu-id="63988-119">Intégrer Microsoft 365 à AD DS</span><span class="sxs-lookup"><span data-stu-id="63988-119">Integrate Microsoft 365 with AD DS</span></span>

<span data-ttu-id="63988-120">Si vous avez des comptes d’utilisateurs dans AD DS, vous ne souhaitez pas re-créer tous ces comptes dans Microsoft 365 et risquez d’introduire des différences ou des erreurs entre les environnements.</span><span class="sxs-lookup"><span data-stu-id="63988-120">If you have existing user accounts in AD DS, you don't want to re-create all of those accounts in Microsoft 365 and risk introducing differences or errors between the environments.</span></span> <span data-ttu-id="63988-121">La synchronisation d’annuaires vous permet de refléter ces comptes entre vos environnements locaux et en ligne.</span><span class="sxs-lookup"><span data-stu-id="63988-121">Directory synchronization helps you mirror those accounts between your on-premises and online environments.</span></span> <span data-ttu-id="63988-122">Avec la synchronisation d’annuaires, vos utilisateurs n’ont pas besoin de mémoriser de nouvelles informations pour chaque environnement, et vous n’avez pas besoin de créer ou de mettre à jour des comptes deux fois.</span><span class="sxs-lookup"><span data-stu-id="63988-122">With directory synchronization, your users don't have to remember new information for each environment, and you don't have to create or update accounts twice.</span></span> <span data-ttu-id="63988-123">Vous devrez préparer [votre annuaire local pour](prepare-for-directory-synchronization.md) la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="63988-123">You will need to [prepare your on-premises directory](prepare-for-directory-synchronization.md) for directory synchronization.</span></span>
  
![Utiliser la synchronisation d’annuaires pour synchroniser les informations de compte d’utilisateur local et en ligne](../media/microsoft-365-integration/directory-synchronization.png)
  
<span data-ttu-id="63988-125">Si vous souhaitez que les utilisateurs puissent se connecter à Microsoft 365 à l’aide de leurs informations d’identification sur site, vous pouvez également configurer l' cesso.</span><span class="sxs-lookup"><span data-stu-id="63988-125">If you want users to be able to log on to Microsoft 365 with their on-premises credentials, you can also configure SSO.</span></span> <span data-ttu-id="63988-126">Avec l’authentification sso, Microsoft 365 est configuré pour faire confiance à l’environnement local pour l’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="63988-126">With SSO, Microsoft 365 is configured to trust the on-premises environment for user authentication.</span></span>
  
![Avec l' sign-on unique, le même compte est disponible dans les environnements locaux et en ligne](../media/microsoft-365-integration/single-sign-on.png)

### <a name="directory-synchronization-with-or-without-password-hash-synchronization-or-pass-through-authentication-pta"></a><span data-ttu-id="63988-128">Synchronisation d’annuaires avec ou sans synchronisation de hachage de mot de passe ou authentification directe (PTA)</span><span class="sxs-lookup"><span data-stu-id="63988-128">Directory synchronization with or without password hash synchronization or pass-through authentication (PTA)</span></span>

<span data-ttu-id="63988-129">Un utilisateur se connecte à son environnement local avec son compte d’utilisateur (domaine \nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="63988-129">A user logs on to their on-premises environment with their user account (domain\username).</span></span> <span data-ttu-id="63988-130">Lorsqu’ils se connectent à Microsoft 365, ils doivent se connecter à nouveau avec leur compte scolaire ou scolaire (user@domain.com).</span><span class="sxs-lookup"><span data-stu-id="63988-130">When they go to Microsoft 365, they must log on again with their work or school account (user@domain.com).</span></span> <span data-ttu-id="63988-131">Le nom d’utilisateur est le même dans les deux environnements.</span><span class="sxs-lookup"><span data-stu-id="63988-131">The user name is the same in both environments.</span></span> <span data-ttu-id="63988-132">Lorsque vous ajoutez phs ou PTA, l’utilisateur a le même mot de passe pour les deux environnements, mais devra fournir à nouveau ces informations d’identification lors de la connexion à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="63988-132">When you add PHS or PTA, the user has the same password for both environments, but will have to provide those credentials again when logging on to Microsoft 365.</span></span> <span data-ttu-id="63988-133">La synchronisation d’annuaires avec PHS est la synchronisation d’annuaires la plus couramment utilisée.</span><span class="sxs-lookup"><span data-stu-id="63988-133">Directory synchronization with PHS is the most commonly used directory synchronization .</span></span>

<span data-ttu-id="63988-134">Pour configurer la synchronisation d’annuaires, utilisez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="63988-134">To set up directory synchronization, use Azure AD Connect.</span></span> <span data-ttu-id="63988-135">Pour obtenir des instructions, voir Configurer la synchronisation d’annuaires pour [Microsoft 365](set-up-directory-synchronization.md) et [Azure AD Connect avec les paramètres express.](https://go.microsoft.com/fwlink/p/?LinkId=698537)</span><span class="sxs-lookup"><span data-stu-id="63988-135">For instructions, see [Set up directory synchronization for Microsoft 365](set-up-directory-synchronization.md) and [Azure AD Connect with express settings](https://go.microsoft.com/fwlink/p/?LinkId=698537).</span></span>

<span data-ttu-id="63988-136">En savoir plus [sur la préparation de la synchronisation d’annuaires vers Microsoft 365.](prepare-for-directory-synchronization.md)</span><span class="sxs-lookup"><span data-stu-id="63988-136">Learn more about [preparing for directory synchronization to Microsoft 365](prepare-for-directory-synchronization.md).</span></span>

### <a name="directory-synchronization-with-sso"></a><span data-ttu-id="63988-137">Synchronisation d’annuaires avec sso</span><span class="sxs-lookup"><span data-stu-id="63988-137">Directory synchronization with SSO</span></span>

<span data-ttu-id="63988-138">Un utilisateur se connecte à son environnement local avec son compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63988-138">A user logs on to their on-premises environment with their user account.</span></span> <span data-ttu-id="63988-139">Lorsqu’ils se connectent à Microsoft 365, ils sont connectés automatiquement ou ils se connectent à l’aide des mêmes informations d’identification qu’ils utilisent pour leur environnement local (domaine \nom d’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="63988-139">When they go to Microsoft 365, they are either logged on automatically, or they log on using the same credentials they use for their on-premises environment (domain\username).</span></span>

<span data-ttu-id="63988-140">Pour configurer l' sso, vous utilisez également Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="63988-140">To set up SSO you also use Azure AD Connect.</span></span> <span data-ttu-id="63988-141">Pour obtenir des instructions, voir [Installation personnalisée d’Azure AD Connect.](https://go.microsoft.com/fwlink/p/?LinkID=698430)</span><span class="sxs-lookup"><span data-stu-id="63988-141">For instructions, see [Custom installation of Azure AD Connect](https://go.microsoft.com/fwlink/p/?LinkID=698430).</span></span>

<span data-ttu-id="63988-142">Pour plus d’informations, [voir l' sign-on unique.](https://go.microsoft.com/fwlink/p/?LinkId=698604)</span><span class="sxs-lookup"><span data-stu-id="63988-142">For more information, see [single sign-on](https://go.microsoft.com/fwlink/p/?LinkId=698604).</span></span>

## <a name="azure-ad-connect"></a><span data-ttu-id="63988-143">Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="63988-143">Azure AD Connect</span></span>

<span data-ttu-id="63988-144">Azure AD Connect remplace les versions antérieures des outils d’intégration d’identité tels que DirSync et Azure AD Sync. Si vous souhaitez mettre à jour Azure Active Directory Sync vers Azure AD Connect, consultez [les instructions de mise à niveau.](https://go.microsoft.com/fwlink/p/?LinkId=733240)</span><span class="sxs-lookup"><span data-stu-id="63988-144">Azure AD Connect replaces older versions of identity integration tools such as DirSync and Azure AD Sync. If you want to update from Azure Active Directory Sync to Azure AD Connect, see [the upgrade instructions](https://go.microsoft.com/fwlink/p/?LinkId=733240).</span></span> 

## <a name="see-also"></a><span data-ttu-id="63988-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63988-145">See also</span></span>

[<span data-ttu-id="63988-146">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="63988-146">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
