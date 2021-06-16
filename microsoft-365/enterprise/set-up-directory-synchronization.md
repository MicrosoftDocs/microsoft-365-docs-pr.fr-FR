---
title: Configurer la synchronisation d’annuaires pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/30/2020
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom: Adm_O365
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MED15
- MBS150
- BCS160
ms.assetid: 1b3b5318-6977-42ed-b5c7-96fa74b08846
description: Découvrez comment configurer la synchronisation d’annuaires entre Microsoft 365 et votre active Directory local.
ms.openlocfilehash: 14b44523c0a560a71ed8dc9182f677f2ebc0b865
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52926525"
---
# <a name="set-up-directory-synchronization-for-microsoft-365"></a><span data-ttu-id="1eb41-103">Configurer la synchronisation d’annuaires pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1eb41-103">Set up directory synchronization for Microsoft 365</span></span>

<span data-ttu-id="1eb41-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="1eb41-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="1eb41-105">Microsoft 365 utilise un client Azure Active Directory (Azure AD) pour stocker et gérer les identités pour l’authentification et les autorisations pour accéder aux ressources informatiques.</span><span class="sxs-lookup"><span data-stu-id="1eb41-105">Microsoft 365 uses an Azure Active Directory (Azure AD) tenant to store and manage identities for authentication and permissions to access cloud-based resources.</span></span> 

<span data-ttu-id="1eb41-106">Si vous avez un domaine ou une forêt AD DS (Active Directory Domain Services) local, vous pouvez synchroniser vos comptes d’utilisateur, groupes et contacts AD DS avec le client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1eb41-106">If you have an on-premises Active Directory Domain Services (AD DS) domain or forest, you can synchronize your AD DS user accounts, groups, and contacts with the Azure AD tenant of your Microsoft 365 subscription.</span></span> <span data-ttu-id="1eb41-107">Il s’agit de l’identité hybride Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1eb41-107">This is hybrid identity for Microsoft 365.</span></span> <span data-ttu-id="1eb41-108">Voici ses composants.</span><span class="sxs-lookup"><span data-stu-id="1eb41-108">Here are its components.</span></span>

![Composants de synchronisation d’annuaires pour Microsoft 365](../media/about-microsoft-365-identity/hybrid-identity.png)

<span data-ttu-id="1eb41-110">Azure AD Connecter s’exécute sur un serveur local et synchronise vos AD DS avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1eb41-110">Azure AD Connect runs on an on-premises server and synchronizes your AD DS with the Azure AD tenant.</span></span> <span data-ttu-id="1eb41-111">En plus de la synchronisation d’annuaires, vous pouvez également spécifier les options d’authentification ci-après :</span><span class="sxs-lookup"><span data-stu-id="1eb41-111">Along with directory synchronization, you can also specify these authentication options:</span></span>

- <span data-ttu-id="1eb41-112">Synchronisation de hachage de mot de passe (PHS)</span><span class="sxs-lookup"><span data-stu-id="1eb41-112">Password hash synchronization (PHS)</span></span>

  <span data-ttu-id="1eb41-113">Azure AD effectue l’authentification elle-même.</span><span class="sxs-lookup"><span data-stu-id="1eb41-113">Azure AD performs the authentication itself.</span></span>

- <span data-ttu-id="1eb41-114">Authentification directe (PTA)</span><span class="sxs-lookup"><span data-stu-id="1eb41-114">Pass-through authentication (PTA)</span></span>

  <span data-ttu-id="1eb41-115">Azure AD dispose d’AD DS qui effectue l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1eb41-115">Azure AD has AD DS perform the authentication.</span></span>

- <span data-ttu-id="1eb41-116">Authentification fédérée</span><span class="sxs-lookup"><span data-stu-id="1eb41-116">Federated authentication</span></span>

  <span data-ttu-id="1eb41-117">Azure AD fait référence à l’ordinateur client qui demande l’authentification à un autre fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="1eb41-117">Azure AD refers the client computer requesting authentication to another identity provider.</span></span>

<span data-ttu-id="1eb41-118">Pour plus [d’informations, voir Identités](plan-for-directory-synchronization.md) hybrides.</span><span class="sxs-lookup"><span data-stu-id="1eb41-118">See [Hybrid identities](plan-for-directory-synchronization.md) for more information.</span></span>
  
## <a name="1-review-prerequisites-for-azure-ad-connect"></a><span data-ttu-id="1eb41-119">1. Passer en revue les conditions préalables pour les Connecter Azure AD</span><span class="sxs-lookup"><span data-stu-id="1eb41-119">1. Review prerequisites for Azure AD Connect</span></span>

<span data-ttu-id="1eb41-120">Vous obtenez un abonnement Azure AD gratuit avec votre abonnement Microsoft 365 abonnement.</span><span class="sxs-lookup"><span data-stu-id="1eb41-120">You get a free Azure AD subscription with your Microsoft 365 subscription.</span></span> <span data-ttu-id="1eb41-121">Lorsque vous configurerez la synchronisation d’annuaires, vous installez Azure AD Connecter sur l’un de vos serveurs locaux.</span><span class="sxs-lookup"><span data-stu-id="1eb41-121">When you set up directory synchronization, you will install Azure AD Connect on one of your on-premises servers.</span></span>
  
<span data-ttu-id="1eb41-122">Pour Microsoft 365 vous devez :</span><span class="sxs-lookup"><span data-stu-id="1eb41-122">For Microsoft 365 you'll need to:</span></span>
  
- <span data-ttu-id="1eb41-123">Vérifiez votre domaine local.</span><span class="sxs-lookup"><span data-stu-id="1eb41-123">Verify your on-premises domain.</span></span> <span data-ttu-id="1eb41-124">L’Assistant Connecter Azure AD vous guide tout au long de cette situation.</span><span class="sxs-lookup"><span data-stu-id="1eb41-124">The Azure AD Connect wizard guides you through this.</span></span>
- <span data-ttu-id="1eb41-125">Obtenez les noms d’utilisateur et les mots de passe pour les comptes d’administrateur de Microsoft 365 client et AD DS.</span><span class="sxs-lookup"><span data-stu-id="1eb41-125">Obtain the user names and passwords for the admin accounts of your Microsoft 365 tenant and AD DS.</span></span>

<span data-ttu-id="1eb41-126">Pour votre serveur local sur lequel vous installez Azure AD Connecter, vous devez :</span><span class="sxs-lookup"><span data-stu-id="1eb41-126">For your on-premises server on which you install Azure AD Connect, you'll need:</span></span>
  
|<span data-ttu-id="1eb41-127">**Système d’exploitation du serveur**</span><span class="sxs-lookup"><span data-stu-id="1eb41-127">**Server OS**</span></span>|<span data-ttu-id="1eb41-128">**Autres logiciels**</span><span class="sxs-lookup"><span data-stu-id="1eb41-128">**Other software**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1eb41-129">Windows Server 2012 R2 et ultérieures</span><span class="sxs-lookup"><span data-stu-id="1eb41-129">Windows Server 2012 R2 and later</span></span> | <span data-ttu-id="1eb41-130">- PowerShell est installé par défaut, aucune action n’est requise.</span><span class="sxs-lookup"><span data-stu-id="1eb41-130">- PowerShell is installed by default, no action is required.</span></span>  <br> <span data-ttu-id="1eb41-131">- Net 4.5.1 et les mises à jour ultérieures sont proposées via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="1eb41-131">- Net 4.5.1 and later releases are offered through Windows Update.</span></span> <span data-ttu-id="1eb41-132">Assurez-vous que vous avez installé les dernières mises à jour Windows Server dans le Panneau de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1eb41-132">Make sure you have installed the latest updates to Windows Server in the Control Panel.</span></span> |
|<span data-ttu-id="1eb41-133">Windows Server 2008 R2 avec Service Pack 1 (SP1)\*\* ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1eb41-133">Windows Server 2008 R2 with Service Pack 1 (SP1)\*\* or Windows Server 2012</span></span> | <span data-ttu-id="1eb41-134">- La dernière version de PowerShell est disponible dans Windows Management Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="1eb41-134">- The latest version of PowerShell is available in Windows Management Framework 4.0.</span></span> <span data-ttu-id="1eb41-135">Recherchez-le dans [le Centre de téléchargement Microsoft.](https://go.microsoft.com/fwlink/p/?LinkId=717996)</span><span class="sxs-lookup"><span data-stu-id="1eb41-135">Search for it on [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?LinkId=717996).</span></span>  <br> <span data-ttu-id="1eb41-136">- .Net 4.5.1 et les version ultérieures sont disponibles dans le Centre de [téléchargement Microsoft.](https://go.microsoft.com/fwlink/p/?LinkId=717996)</span><span class="sxs-lookup"><span data-stu-id="1eb41-136">- .Net 4.5.1 and later releases are available on [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?LinkId=717996).</span></span> |
|<span data-ttu-id="1eb41-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eb41-137">Windows Server 2008</span></span> | <span data-ttu-id="1eb41-138">- La dernière version prise en charge de PowerShell est disponible dans Windows Management Framework 3.0, disponible dans le Centre [de téléchargement Microsoft.](https://go.microsoft.com/fwlink/p/?LinkId=717996)</span><span class="sxs-lookup"><span data-stu-id="1eb41-138">- The latest supported version of PowerShell is available in Windows Management Framework 3.0, available on [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?LinkId=717996).</span></span>  <br> <span data-ttu-id="1eb41-139">- .Net 4.5.1 et les version ultérieures sont disponibles dans le Centre de [téléchargement Microsoft.](https://go.microsoft.com/fwlink/p/?LinkId=717996)</span><span class="sxs-lookup"><span data-stu-id="1eb41-139">- .Net 4.5.1 and later releases are available on [Microsoft Download Center](https://go.microsoft.com/fwlink/p/?LinkId=717996).</span></span> |

<span data-ttu-id="1eb41-140">Consultez [les conditions préalables](/azure/active-directory/hybrid/how-to-connect-install-prerequisites) pour Azure Active Directory Connecter pour plus d’informations sur les configurations matérielle, logicielle, de compte et d’autorisation requises, les certificats SSL requis et les limites d’objets pour les Connecter Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1eb41-140">See [Prerequisites for Azure Active Directory Connect](/azure/active-directory/hybrid/how-to-connect-install-prerequisites) for the details of hardware, software, account and permissions requirements, SSL certificate requirements, and object limits for Azure AD Connect.</span></span>
  
<span data-ttu-id="1eb41-141">Vous pouvez également consulter l’historique [](/azure/active-directory/hybrid/reference-connect-version-history) des versions Connecter Azure AD pour voir ce qui est inclus et corrigé dans chaque version.</span><span class="sxs-lookup"><span data-stu-id="1eb41-141">You can also review the Azure AD Connect [version release history](/azure/active-directory/hybrid/reference-connect-version-history) to see what is included and fixed in each release.</span></span>

## <a name="2-install-azure-ad-connect-and-configure-directory-synchronization"></a><span data-ttu-id="1eb41-142">2. Installer Azure AD Connecter et configurer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="1eb41-142">2. Install Azure AD Connect and configure directory synchronization</span></span>

<span data-ttu-id="1eb41-143">Avant de commencer, assurez-vous que vous avez :</span><span class="sxs-lookup"><span data-stu-id="1eb41-143">Before you begin, make sure you have:</span></span>

- <span data-ttu-id="1eb41-144">Nom d’utilisateur et mot de passe d’Microsoft 365 administrateur global</span><span class="sxs-lookup"><span data-stu-id="1eb41-144">The user name and password of a Microsoft 365 global admin</span></span>
- <span data-ttu-id="1eb41-145">Nom d’utilisateur et mot de passe d’un administrateur de domaine AD DS</span><span class="sxs-lookup"><span data-stu-id="1eb41-145">The user name and password of an AD DS domain administrator</span></span>
- <span data-ttu-id="1eb41-146">Quelle méthode d’authentification (PHS, PTA, fédéré)</span><span class="sxs-lookup"><span data-stu-id="1eb41-146">Which authentication method (PHS, PTA, federated)</span></span>
- <span data-ttu-id="1eb41-147">Si vous souhaitez utiliser l' [sign-on](/azure/active-directory/hybrid/how-to-connect-sso) unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="1eb41-147">Whether you want to use [Azure AD Seamless Single Sign-on (SSO)](/azure/active-directory/hybrid/how-to-connect-sso)</span></span>

<span data-ttu-id="1eb41-148">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1eb41-148">Follow these steps:</span></span>

1. <span data-ttu-id="1eb41-149">Connectez-vous au [Microsoft 365 d’administration](https://admin.microsoft.com) ( et choisissez Utilisateurs https://admin.microsoft.com) actifs  \> **sur** le navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="1eb41-149">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) (https://admin.microsoft.com) and choose **Users** \> **Active Users** on the left navigation.</span></span>
2. <span data-ttu-id="1eb41-150">Dans la page **Utilisateurs** actifs, sélectionnez **Plus** (trois points) \> **Synchronisation d’annuaires.**</span><span class="sxs-lookup"><span data-stu-id="1eb41-150">On the **Active users** page, choose **More** (three dots) \> **Directory synchronization**.</span></span>
  
3. <span data-ttu-id="1eb41-151">Dans la page **Azure Active Directory de** préparation, sélectionnez Le Centre de téléchargement pour obtenir le lien **d’outils Connecter Azure AD** pour commencer.</span><span class="sxs-lookup"><span data-stu-id="1eb41-151">On the **Azure Active Directory preparation** page, select the **Go to the Download center to get the Azure AD Connect tool** link to get started.</span></span> 
4. <span data-ttu-id="1eb41-152">Suivez les étapes de la feuille [de route d’installation d’Azure AD Connecter et Azure AD Connecter Health.](/azure/active-directory/hybrid/how-to-connect-install-roadmap)</span><span class="sxs-lookup"><span data-stu-id="1eb41-152">Follow the steps in [Azure AD Connect and Azure AD Connect Health installation roadmap](/azure/active-directory/hybrid/how-to-connect-install-roadmap).</span></span>

## <a name="3-finish-setting-up-domains"></a><span data-ttu-id="1eb41-153">3. Terminer la configuration des domaines</span><span class="sxs-lookup"><span data-stu-id="1eb41-153">3. Finish setting up domains</span></span>

<span data-ttu-id="1eb41-154">Suivez les étapes de la procédure de création d’enregistrements [DNS Microsoft 365](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) lorsque vous gérez vos enregistrements DNS pour terminer la configuration de vos domaines.</span><span class="sxs-lookup"><span data-stu-id="1eb41-154">Follow the steps in [Create DNS records for Microsoft 365 when you manage your DNS records](/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider) to finish setting up your domains.</span></span>

## <a name="next-step"></a><span data-ttu-id="1eb41-155">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1eb41-155">Next step</span></span>

[<span data-ttu-id="1eb41-156">Attribution de licences aux comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="1eb41-156">Assign licenses to user accounts</span></span>](assign-licenses-to-user-accounts.md)