---
title: 'Étape 4 : Ajouter vos comptes d’utilisateurs'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/20/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Vous pouvez ajouter des comptes d’utilisateurs et des groupes directement dans le Cloud ou par synchronisation avec votre répertoire local.
ms.openlocfilehash: 2a54044737f5b924bd619d5a6c7c72091dc7a0d1
ms.sourcegitcommit: 634abe8a237e27dfe82376e6ef32280aab5d4a27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "45005833"
---
# <a name="step-4-add-your-user-accounts"></a><span data-ttu-id="18d3e-103">Étape 4 : Ajouter vos comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="18d3e-103">Step 4: Add your user accounts</span></span>

![Phase 2 - Identité](../media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-cloud-only"></a>
## <a name="create-your-user-accounts-for-cloud-only-identity"></a><span data-ttu-id="18d3e-105">Créer vos comptes d’utilisateur pour l’identité Cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="18d3e-105">Create your user accounts for cloud-only identity</span></span>

<span data-ttu-id="18d3e-106">Pour l’identité Cloud uniquement, créez vos utilisateurs et groupes dans Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="18d3e-106">For cloud-only identity, create your users and groups in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="18d3e-107">Vous pouvez utiliser :</span><span class="sxs-lookup"><span data-stu-id="18d3e-107">You can use:</span></span>

- <span data-ttu-id="18d3e-108">Le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="18d3e-108">The Microsoft 365 admin center</span></span>
- <span data-ttu-id="18d3e-109">Le Portail Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="18d3e-109">The Azure portal</span></span>
- <span data-ttu-id="18d3e-110">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="18d3e-110">Azure PowerShell</span></span>

<a name="identity-sync"></a>
## <a name="synchronize-identities-for-hybrid-identity"></a><span data-ttu-id="18d3e-111">Synchroniser les identités pour l’identité hybride</span><span class="sxs-lookup"><span data-stu-id="18d3e-111">Synchronize identities for hybrid identity</span></span>

<span data-ttu-id="18d3e-112">*Cette opération, obligatoire pour les environnements hybrides, s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="18d3e-112">*This is required for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="18d3e-113">Dans cette section, vous allez synchroniser votre instance locale de Services de domaine Active Directory (AD DS) avec le client Azure AD utilisé par Office 365, Microsoft Intune et d’autres services cloud, parmi lesquels Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="18d3e-113">In this section, you'll synchronize your on-premises Active Directory Domain Services (AD DS) with the Azure AD tenant used by Office 365, Microsoft Intune, and other cloud-based services included with Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="18d3e-114">Azure AD Connect est l’outil Microsoft pris en charge qui vous guide tout au long de la synchronisation des identités dont vous avez réellement besoin, des environnements AD DS à une ou plusieurs forêts à votre locataire Azure AD.</span><span class="sxs-lookup"><span data-stu-id="18d3e-114">Azure AD Connect is the supported Microsoft tool that guides you through synchronizing only the identities you really need from single or multi-forest AD DS environments to your Azure AD tenant.</span></span> <span data-ttu-id="18d3e-115">La figure suivante illustre le processus de base de la synchronisation Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="18d3e-115">The following figure shows the basic process for Azure AD Connect synchronization.</span></span>

![Comment Azure AD Connect synchronise votre annuaire local avec Azure AD](../media/identity-add-user-accounts/azure-ad-connect.png)

1. <span data-ttu-id="18d3e-117">Azure AD Connect exécuté sur un serveur interroge AD DS pour identifier les modifications apportées aux comptes, aux groupes et aux contacts.</span><span class="sxs-lookup"><span data-stu-id="18d3e-117">Azure AD Connect running on a server polls AD DS for changes in accounts, groups, and contacts.</span></span>
2. <span data-ttu-id="18d3e-118">Azure AD Connect envoie ces modifications au locataire Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="18d3e-118">Azure AD Connect sends those changes to the Azure AD tenant of your Microsoft 365 subscription.</span></span>

<span data-ttu-id="18d3e-119">The first decision in your hybrid identity solution is your authentication requirement.</span><span class="sxs-lookup"><span data-stu-id="18d3e-119">The first decision in your hybrid identity solution is your authentication requirement.</span></span> <span data-ttu-id="18d3e-120">The following options are options:</span><span class="sxs-lookup"><span data-stu-id="18d3e-120">The following options are options:</span></span>

- <span data-ttu-id="18d3e-121">With **managed authentication**, Azure AD handles the authentication process for user sign-in.</span><span class="sxs-lookup"><span data-stu-id="18d3e-121">With **managed authentication**, Azure AD handles the authentication process for user sign-in.</span></span> <span data-ttu-id="18d3e-122">There are two methods for managed authentication:</span><span class="sxs-lookup"><span data-stu-id="18d3e-122">There are two methods for managed authentication:</span></span> 
    - <span data-ttu-id="18d3e-123">**Synchronisation du hachage de mot de passe (PHS)** [recommandée et requise pour certaines fonctionnalités premium].</span><span class="sxs-lookup"><span data-stu-id="18d3e-123">**Password Hash Sync (PHS)** [Recommended and required for some premium features].</span></span> <span data-ttu-id="18d3e-124">Il s’agit du moyen le plus simple d’activer l’authentification des objets d’annuaire locaux dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="18d3e-124">This is the simplest way to enable authentication for on-premises directory objects in Azure AD.</span></span> <span data-ttu-id="18d3e-125">Azure AD Connect extrait le mot de passe haché d’AD DS, lui applique un traitement de sécurité supplémentaire et le synchronise avec Azure AD.</span><span class="sxs-lookup"><span data-stu-id="18d3e-125">Azure AD Connect extracts the hashed password from AD DS, does extra security processing on the password hash, and synchronizes it to Azure AD.</span></span> <span data-ttu-id="18d3e-126">Pour plus d’informations, consultez [Implémenter la synchronisation de hachage du mot de passe avec la synchronisation Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span><span class="sxs-lookup"><span data-stu-id="18d3e-126">For more information, see [Implement password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-password-hash-synchronization).</span></span>
    - <span data-ttu-id="18d3e-127">L’**authentification directe** fournit une solution de validation du mot de passe simple pour les services Azure AD.</span><span class="sxs-lookup"><span data-stu-id="18d3e-127">**Pass-through Authentication (PTA)** provides a simple password validation solution for Azure AD-based services.</span></span> <span data-ttu-id="18d3e-128">L’authentification directe utilise un agent qui s’exécute sur un ou plusieurs serveurs locaux pour valider les authentifications des utilisateurs directement auprès de votre instance locale d’AD DS.</span><span class="sxs-lookup"><span data-stu-id="18d3e-128">PTA uses an agent running on one or more on-premises servers to validate the user authentications directly with your on-premises AD DS.</span></span> <span data-ttu-id="18d3e-129">Pour plus d’informations, consultez [Connexion utilisateur avec l’authentification directe Azure Active Directory](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication).</span><span class="sxs-lookup"><span data-stu-id="18d3e-129">For more information, see [User sign-in with Azure Active Directory Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication).</span></span>
- <span data-ttu-id="18d3e-130">With **federated authentication**, the authentication process is redirected to another identity provider through an identity federation server, such as Active Directory Federation Services (AD FS), for a user’s sign-in.</span><span class="sxs-lookup"><span data-stu-id="18d3e-130">With **federated authentication**, the authentication process is redirected to another identity provider through an identity federation server, such as Active Directory Federation Services (AD FS), for a user’s sign-in.</span></span> <span data-ttu-id="18d3e-131">The identity provider can provide additional authentication methods, such as smartcard-based authentication.</span><span class="sxs-lookup"><span data-stu-id="18d3e-131">The identity provider can provide additional authentication methods, such as smartcard-based authentication.</span></span> <span data-ttu-id="18d3e-132">For more information, see [Choosing the right authentication method for your Azure Active Directory hybrid identity solution](https://docs.microsoft.com/azure/active-directory/hybrid/choose-ad-authn).</span><span class="sxs-lookup"><span data-stu-id="18d3e-132">For more information, see [Choosing the right authentication method for your Azure Active Directory hybrid identity solution](https://docs.microsoft.com/azure/active-directory/hybrid/choose-ad-authn).</span></span>

<span data-ttu-id="18d3e-133">Regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="18d3e-133">Watch this video for an overview of identity models and authentication for Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="18d3e-134"><p> </p></span><span class="sxs-lookup"><span data-stu-id="18d3e-134"><p> </p></span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

<span data-ttu-id="18d3e-135">Après avoir déterminé votre solution d’identité hybride, téléchargez et exécutez l’[outil de correction d’erreurs de synchronisation d’annuaires IdFix](https://www.microsoft.com/download/details.aspx?id=36832) pour analyser les problèmes de votre instance d’AD.</span><span class="sxs-lookup"><span data-stu-id="18d3e-135">After you've determined your hybrid identity solution, download and run the [IdFix Directory Synchronization Error Remediation Tool](https://www.microsoft.com/download/details.aspx?id=36832) to analyze your AD DS for issues.</span></span>

<span data-ttu-id="18d3e-136">Après avoir résolu tous les problèmes identifiés par l’outil IdFix, consultez [Implémenter la synchronisation de hachage de mot de passe avec la synchronisation](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-hash-synchronization) pour savoir comment installer l’outil Azure AD Connect et configurer la synchronisation d’annuaires entre votre instance locale d’AD DS et le locataire Azure AD de vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="18d3e-136">After resolving all of the issues identified by the IdFix tool, see [Implement password hash synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-hash-synchronization) for guidance on installing the Azure AD Connect tool and configuring directory synchronization between your on-premises AD DS and the Azure AD tenant for your Microsoft 365 subscription.</span></span> <span data-ttu-id="18d3e-137">Une fois la synchronisation lancée, vous gérerez vos groupes et comptes d’utilisateur avec votre fournisseur d’identité local, par exemple AD DS.</span><span class="sxs-lookup"><span data-stu-id="18d3e-137">After synchronization starts, you'll maintain your user accounts and groups with your on-premises identity provider, such as AD DS.</span></span>

<span data-ttu-id="18d3e-138">Microsoft fournit un ensemble de recommandations sur l’[accès aux appareils et à l’identité](microsoft-365-policies-configurations.md) pour garantir un personnel conforme et productif.</span><span class="sxs-lookup"><span data-stu-id="18d3e-138">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce.</span></span> 

- <span data-ttu-id="18d3e-139">Concernant la configuration recommandée pour les environnements hybrides, consultez la colonne **Active Directory avec la synchronisation de hachage de mot de passe** de la section [Travail préparatoire](identity-access-prerequisites.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="18d3e-139">For recommended requirements for hybrid environments, see the **Active Directory with password hash sync** column in [prerequisites](identity-access-prerequisites.md#prerequisites).</span></span> 

- <span data-ttu-id="18d3e-140">Pour la configuration recommandée pour les environnements cloud uniquement, reportez-vous à la colonne **Cloud uniquement** de la section [Travail préparatoire](identity-access-prerequisites.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="18d3e-140">For recommended requirements for cloud only environments, see the **Cloud only** column in [prerequisites](identity-access-prerequisites.md#prerequisites).</span></span>

<span data-ttu-id="18d3e-141">Une fois vos groupes et utilisateurs locaux présents dans Azure AD, vous pouvez commencer à attribuer des charges de travail de productivité telles que OneDrive Entreprise et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="18d3e-141">Once your on-premises users and groups are present in Azure AD, you can start assigning licenses and using productivity workloads such as OneDrive for Business and Exchange Online.</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="18d3e-143">Guide de laboratoire de test : Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="18d3e-143">Test Lab Guide: Password hash synchronization</span></span>](password-hash-sync-m365-ent-test-environment.md)<br> [<span data-ttu-id="18d3e-144">Guide de laboratoire de test : Authentification directe</span><span class="sxs-lookup"><span data-stu-id="18d3e-144">Test Lab Guide: Pass-through authentication</span></span>](pass-through-auth-m365-ent-test-environment.md) |
|||

<span data-ttu-id="18d3e-145">Comme point de contrôle intermédiaire, consultez les [critères de sortie](identity-exit-criteria.md#crit-identity-sync) correspondant à cette section.</span><span class="sxs-lookup"><span data-stu-id="18d3e-145">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sync) corresponding to this section.</span></span>

<a name="identity-sync-health"></a>
## <a name="monitor-synchronization-health"></a><span data-ttu-id="18d3e-146">Surveiller l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="18d3e-146">Monitor synchronization health</span></span>

<span data-ttu-id="18d3e-147">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="18d3e-147">*This is optional and applies to both the E3 and E5 versions of Microsoft 365*</span></span>

<span data-ttu-id="18d3e-148">Dans cette section, vous allez installer un agent d’intégrité Azure AD Connect sur chacun de vos contrôleurs de domaine AD DS pour surveiller votre infrastructure d’identité et les services de synchronisation fournis par Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="18d3e-148">In this section, you'll install an Azure AD Connect Health agent on each of your on-premises AD DS domain controllers to monitor your identity infrastructure and the synchronization services provided by Azure AD Connect.</span></span> <span data-ttu-id="18d3e-149">Les informations de surveillance sont disponibles sur un portail Azure AD Connect Health, où vous pouvez afficher les alertes, surveiller les performances, analyser les utilisations, etc.</span><span class="sxs-lookup"><span data-stu-id="18d3e-149">The monitoring information is made available in an Azure AD Connect Health portal, where you can view alerts, performance monitoring, usage analytics, and other information.</span></span>

![Composants d’Azure AD Connect Health](../media/identity-add-user-accounts/identity-azure-ad-connect-health.png)

<span data-ttu-id="18d3e-151">La décision de conception clé concernant l’utilisation d’Azure AD Connect Health est basée sur la manière dont vous utilisez Azure AD Connect :</span><span class="sxs-lookup"><span data-stu-id="18d3e-151">The key design decision of how to use Azure AD Connect Health is based on how you are using Azure AD Connect:</span></span>

- <span data-ttu-id="18d3e-152">Si vous utilisez de nouveau l’option d’**authentification gérée**, commencez avec la rubrique relative à l’[utilisation d’Azure AD Connect Health avec la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="18d3e-152">If you’re using the **managed authentication** option, start with [Using Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) to understand and configure Azure AD Connect Health.</span></span>
- <span data-ttu-id="18d3e-153">Si vous synchronisez uniquement les noms des comptes et des groupes à l’aide de l’**authentification fédérée** avec Active Directory Federation Services (AD FS), commencez avec la rubrique [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="18d3e-153">If you're synchronizing just the names of the accounts and groups using **federated authentication** with Active Directory Federation Services (AD FS), start with [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) to understand and configure Azure AD Connect Health.</span></span>

<span data-ttu-id="18d3e-154">Au terme de cette section, vous aurez :</span><span class="sxs-lookup"><span data-stu-id="18d3e-154">When you complete this section, you’ll have:</span></span>

- <span data-ttu-id="18d3e-155">l’agent Azure AD Connect Health installé sur vos serveurs de fournisseur d’identité local ;</span><span class="sxs-lookup"><span data-stu-id="18d3e-155">The Azure AD Connect Health agent installed on your on-premises identity provider servers.</span></span>
- <span data-ttu-id="18d3e-156">le portail Azure AD Connect Health qui affiche l’état actuel de vos activités d’infrastructure et de synchronisation locales avec le client Azure AD pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="18d3e-156">The Azure AD Connect Health portal displaying the current state of your on-premises infrastructure and synchronization activities with the Azure AD tenant for your Microsoft 365 subscription.</span></span>

<span data-ttu-id="18d3e-157">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-sync-health) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="18d3e-157">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sync-health) for this section.</span></span>



<a name="identity-pw-writeback"></a>
## <a name="simplify-password-updates"></a><span data-ttu-id="18d3e-158">Simplifiez les mises à jour du mot de passe</span><span class="sxs-lookup"><span data-stu-id="18d3e-158">Simplify password updates</span></span>

<span data-ttu-id="18d3e-159">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="18d3e-159">*This is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="18d3e-160">Dans cette section, vous devez autoriser les utilisateurs à réinitialiser leur mot de passe via Azure Active Directory (Azure AD), qui est ensuite répliqué sur votre Active Directory Domain Services (AD DS)local.</span><span class="sxs-lookup"><span data-stu-id="18d3e-160">In this section, you'll allow users to reset their passwords through Azure Active Directory (Azure AD), which is then replicated to your local Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="18d3e-161">Ce processus est appelé écriture différée de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="18d3e-161">This process is known as password writeback.</span></span> <span data-ttu-id="18d3e-162">Avec l’écriture différée de mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe via la version locale Active Directory Domain Services où sont stockés les comptes d’utilisateurs et leurs attributs.</span><span class="sxs-lookup"><span data-stu-id="18d3e-162">With password writeback, users don’t need to update their passwords through the on-premises AD DS where user accounts and their attributes are stored.</span></span> <span data-ttu-id="18d3e-163">C’est utile pour les utilisateurs itinérants ou distants qui ne possèdent pas de connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="18d3e-163">This is valuable to roaming or remote users who do not have a remote access connection to the on-premises network.</span></span>

<span data-ttu-id="18d3e-164">L’écriture différée de mot de passe est requise pour exploiter pleinement les fonctionnalités Azure AD Identity Protection, comme obliger les utilisateurs à modifier leur mot de passe en local lorsqu’un risque élevé de compromission de compte a été détecté.</span><span class="sxs-lookup"><span data-stu-id="18d3e-164">Password writeback is required to fully utilize Azure AD Identity Protection capabilities, such as requiring users to change their on-premises passwords when there has been a high risk of account compromise detected.</span></span>

<span data-ttu-id="18d3e-165">Pour obtenir plus d’informations et les instructions de configuration, consultez l’article [Azure AD SSPR avec l’écriture différée de mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span><span class="sxs-lookup"><span data-stu-id="18d3e-165">For additional information and configuration instructions, see [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span></span>

>[!Note]
><span data-ttu-id="18d3e-166">Upgrade to the latest version of Azure AD Connect to ensure the best possible experience and new features as they are released.</span><span class="sxs-lookup"><span data-stu-id="18d3e-166">Upgrade to the latest version of Azure AD Connect to ensure the best possible experience and new features as they are released.</span></span> <span data-ttu-id="18d3e-167">For more information, see [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span><span class="sxs-lookup"><span data-stu-id="18d3e-167">For more information, see [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span></span>
>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="18d3e-169">Guide du laboratoire de test : Écriture différée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="18d3e-169">Test Lab Guide: Password writeback</span></span>](password-writeback-m365-ent-test-environment.md) |
|||

<span data-ttu-id="18d3e-170">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pw-writeback) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="18d3e-170">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pw-writeback) for this section.</span></span>

|||
|:-------|:-----|
|![Étape 5](../media/stepnumbers/Step5.png)| [<span data-ttu-id="18d3e-172">Utiliser des groupes pour la gestion</span><span class="sxs-lookup"><span data-stu-id="18d3e-172">Use groups for management</span></span>](identity-use-group-management.md) |
