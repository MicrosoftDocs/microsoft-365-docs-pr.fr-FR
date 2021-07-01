---
title: Microsoft 365 modèles d’identité et Azure Active Directory
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.date: 09/30/2020
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- M365-identity-device-management
- M365-security-compliance
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-mar2020
search.appverid:
- MET150
- MOE150
- BCS160
ms.assetid: 06a189e7-5ec6-4af2-94bf-a22ea225a7a9
description: Découvrez comment gérer le service d’identité d’utilisateur Azure AD dans Microsoft 365 à l’aide de modèles d’identité cloud uniquement ou hybrides.
ms.openlocfilehash: 93a37f39a4d96d7c2e434ed6edf4df588e672a0f
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228494"
---
# <a name="microsoft-365-identity-models-and-azure-active-directory"></a><span data-ttu-id="4c602-103">Microsoft 365 modèles d’identité et Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4c602-103">Microsoft 365 identity models and Azure Active Directory</span></span>

<span data-ttu-id="4c602-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="4c602-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="4c602-105">Microsoft 365 utilise Azure Active Directory (Azure AD), un service d’authentification et d’identité d’utilisateur basé sur le cloud inclus dans votre abonnement Microsoft 365, pour gérer les identités et l’authentification pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c602-105">Microsoft 365 uses Azure Active Directory (Azure AD), a cloud-based user identity and authentication service that is included with your Microsoft 365 subscription, to manage identities and authentication for Microsoft 365.</span></span> <span data-ttu-id="4c602-106">La configuration correcte de votre infrastructure d’identité est essentielle à la gestion Microsoft 365'accès des utilisateurs et des autorisations pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4c602-106">Getting your identity infrastructure configured correctly is vital to managing Microsoft 365 user access and permissions for your organization.</span></span>

<span data-ttu-id="4c602-107">Avant de commencer, regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c602-107">Before you begin, watch this video for an overview of identity models and authentication for Microsoft 365.</span></span>

<span data-ttu-id="4c602-108"><p> </p></span><span class="sxs-lookup"><span data-stu-id="4c602-108"><p> </p></span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

<span data-ttu-id="4c602-109">Votre premier choix de planification est le modèle Microsoft 365'identité.</span><span class="sxs-lookup"><span data-stu-id="4c602-109">Your first planning choice is the Microsoft 365 identity model.</span></span>

## <a name="microsoft-365-identity-models"></a><span data-ttu-id="4c602-110">Microsoft 365 d’identité</span><span class="sxs-lookup"><span data-stu-id="4c602-110">Microsoft 365 identity models</span></span>

<span data-ttu-id="4c602-111">Pour planifier les comptes d’utilisateurs, vous devez d’abord comprendre les deux modèles d’identité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c602-111">To plan for user accounts, you first need to understand the two identity models in Microsoft 365.</span></span> <span data-ttu-id="4c602-112">Vous pouvez gérer les identités de votre organisation uniquement dans le cloud, ou vous pouvez conserver vos identités AD DS (Active Directory Domain Services) locales et les utiliser pour l’authentification lorsque les utilisateurs accèdent aux services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4c602-112">You can maintain your organization's identities only in the cloud, or you can maintain your on-premises Active Directory Domain Services (AD DS) identities and use them for authentication when users access Microsoft 365 cloud services.</span></span>

<span data-ttu-id="4c602-113">Voici les deux types d’identité et leur meilleur ajustement et leurs avantages.</span><span class="sxs-lookup"><span data-stu-id="4c602-113">Here are the two types of identity and their best fit and benefits.</span></span>

| <span data-ttu-id="4c602-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="4c602-114">Attribute</span></span> | <span data-ttu-id="4c602-115">Identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="4c602-115">Cloud-only identity</span></span> | <span data-ttu-id="4c602-116">Identité hybride</span><span class="sxs-lookup"><span data-stu-id="4c602-116">Hybrid identity</span></span> |
|:-------|:-----|:-----|
| <span data-ttu-id="4c602-117">**Définition**</span><span class="sxs-lookup"><span data-stu-id="4c602-117">**Definition**</span></span> | <span data-ttu-id="4c602-118">Le compte d’utilisateur existe uniquement dans le client Azure AD pour votre abonnement Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="4c602-118">User account only exists in the Azure AD tenant for your Microsoft 365 subscription.</span></span> | <span data-ttu-id="4c602-119">Le compte d’utilisateur existe dans AD DS et une copie se trouve également dans le client Azure AD pour votre abonnement Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="4c602-119">User account exists in AD DS and a copy is also in the Azure AD tenant for your Microsoft 365 subscription.</span></span> <span data-ttu-id="4c602-120">Le compte d’utilisateur dans Azure AD peut également inclure une version hachée du mot de passe de compte d’utilisateur AD DS déjà haché.</span><span class="sxs-lookup"><span data-stu-id="4c602-120">The user account in Azure AD might also include a hashed version of the already hashed AD DS user account password.</span></span> |
| <span data-ttu-id="4c602-121">**Comment Microsoft 365 authentifier les informations d’identification de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="4c602-121">**How Microsoft 365 authenticates user credentials**</span></span> | <span data-ttu-id="4c602-122">Le client Azure AD de votre abonnement Microsoft 365 effectue l’authentification avec le compte d’identité cloud.</span><span class="sxs-lookup"><span data-stu-id="4c602-122">The Azure AD tenant for your Microsoft 365 subscription performs the authentication with the cloud identity account.</span></span> | <span data-ttu-id="4c602-123">Le client Azure AD de votre abonnement Microsoft 365 gère le processus d’authentification ou redirige l’utilisateur vers un autre fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="4c602-123">The Azure AD tenant for your Microsoft 365 subscription either handles the authentication process or redirects the user to another identity provider.</span></span> |
| <span data-ttu-id="4c602-124">**Recommandé pour**</span><span class="sxs-lookup"><span data-stu-id="4c602-124">**Best for**</span></span> | <span data-ttu-id="4c602-125">Organisations qui n’ont pas ou n’ont pas besoin d’une AD DS locale.</span><span class="sxs-lookup"><span data-stu-id="4c602-125">Organizations that do not have or need an on-premises AD DS.</span></span> | <span data-ttu-id="4c602-126">Organisations utilisant AD DS ou un autre fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="4c602-126">Organizations using AD DS or another identity provider.</span></span> |
| <span data-ttu-id="4c602-127">**Plus grand avantage**</span><span class="sxs-lookup"><span data-stu-id="4c602-127">**Greatest benefit**</span></span> | <span data-ttu-id="4c602-128">Simple à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4c602-128">Simple to use.</span></span> <span data-ttu-id="4c602-129">Aucun outil ou serveur d’annuaire supplémentaire n’est requis.</span><span class="sxs-lookup"><span data-stu-id="4c602-129">No extra directory tools or servers required.</span></span> | <span data-ttu-id="4c602-130">Les utilisateurs peuvent utiliser les mêmes informations d’identification lors de l’accès à des ressources sur site ou en nuage.</span><span class="sxs-lookup"><span data-stu-id="4c602-130">Users can use the same credentials when accessing on-premises or cloud-based resources.</span></span> |
||||

## <a name="cloud-only-identity"></a><span data-ttu-id="4c602-131">Identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="4c602-131">Cloud-only identity</span></span>

<span data-ttu-id="4c602-132">Une identité cloud uniquement utilise des comptes d’utilisateur qui existent uniquement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-132">A cloud-only identity uses user accounts that exist only in Azure AD.</span></span> <span data-ttu-id="4c602-133">L’identité cloud uniquement est généralement utilisée par les petites organisations qui n’ont pas de serveurs locaux ou qui n’utilisent pas AD DS pour gérer les identités locales.</span><span class="sxs-lookup"><span data-stu-id="4c602-133">Cloud-only identity is typically used by small organizations that do not have on-premises servers or do not use AD DS to manage local identities.</span></span>

<span data-ttu-id="4c602-134">Voici les composants de base de l’identité cloud uniquement.</span><span class="sxs-lookup"><span data-stu-id="4c602-134">Here are the basic components of cloud-only identity.</span></span>

![Composants de base de l’identité cloud uniquement](../media/about-microsoft-365-identity/cloud-only-identity.png)

<span data-ttu-id="4c602-136">Les utilisateurs locaux et distants (en ligne) utilisent leurs comptes d’utilisateur et mots de passe Azure AD pour accéder Microsoft 365 services cloud.</span><span class="sxs-lookup"><span data-stu-id="4c602-136">Both on-premises and remote (online) users use their Azure AD user accounts and passwords to access Microsoft 365 cloud services.</span></span> <span data-ttu-id="4c602-137">Azure AD authentifier les informations d’identification de l’utilisateur en fonction de ses comptes d’utilisateur et mots de passe stockés.</span><span class="sxs-lookup"><span data-stu-id="4c602-137">Azure AD authenticates user credentials based on its stored user accounts and passwords.</span></span>

### <a name="administration"></a><span data-ttu-id="4c602-138">Administration</span><span class="sxs-lookup"><span data-stu-id="4c602-138">Administration</span></span>
<span data-ttu-id="4c602-139">Étant donné que les comptes d’utilisateur sont stockés uniquement dans Azure AD, vous gérez les identités cloud à l’aide d’outils tels que Centre d’administration Microsoft 365 [et](../admin/add-users/index.yml) [Windows PowerShell](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="4c602-139">Because user accounts are only stored in Azure AD, you manage cloud identities with tools such as the [Microsoft 365 admin center](../admin/add-users/index.yml) and [Windows PowerShell](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md).</span></span>

## <a name="hybrid-identity"></a><span data-ttu-id="4c602-140">Identité hybride</span><span class="sxs-lookup"><span data-stu-id="4c602-140">Hybrid identity</span></span>

<span data-ttu-id="4c602-141">L’identité hybride utilise des comptes qui proviennent d’un service AD DS local et qui ont une copie dans le client Azure AD d’un abonnement Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="4c602-141">Hybrid identity uses accounts that originate in an on-premises AD DS and have a copy in the Azure AD tenant of a Microsoft 365 subscription.</span></span> <span data-ttu-id="4c602-142">Toutefois, la plupart des modifications ne s' flowent qu’à sens unique.</span><span class="sxs-lookup"><span data-stu-id="4c602-142">However, most changes only flow one way.</span></span> <span data-ttu-id="4c602-143">Les modifications apportées aux comptes d’utilisateurS AD DS sont synchronisées avec leur copie dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-143">Changes that you make to AD DS user accounts are synchronized to their copy in Azure AD.</span></span> <span data-ttu-id="4c602-144">Toutefois, les modifications apportées aux comptes basés sur le cloud dans Azure AD, telles que les nouveaux comptes d’utilisateur, ne sont pas synchronisées avec AD DS.</span><span class="sxs-lookup"><span data-stu-id="4c602-144">But changes made to cloud-based accounts in Azure AD, such as new user accounts, are not synchronized with AD DS.</span></span>

<span data-ttu-id="4c602-145">Azure AD Connecter la synchronisation continue des comptes.</span><span class="sxs-lookup"><span data-stu-id="4c602-145">Azure AD Connect provides the ongoing account synchronization.</span></span> <span data-ttu-id="4c602-146">Il s’exécute sur un serveur local, recherche les modifications dans les AD DS et les a transmis à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-146">It runs on an on-premises server, checks for changes in the AD DS, and forwards those changes to Azure AD.</span></span> <span data-ttu-id="4c602-147">Azure AD Connecter permet de filtrer les comptes qui sont synchronisés et de synchroniser une version hachée des mots de passe utilisateur, appelée synchronisation de hachage de mot de passe (PHS).</span><span class="sxs-lookup"><span data-stu-id="4c602-147">Azure AD Connect provides the ability to filter which accounts are synchronized and whether to synchronize a hashed version of user passwords, known as password hash synchronization (PHS).</span></span>

<span data-ttu-id="4c602-148">Lorsque vous implémentez une identité hybride, votre AD DS local est la source faisant autorité pour les informations de compte.</span><span class="sxs-lookup"><span data-stu-id="4c602-148">When you implement hybrid identity, your on-premises AD DS is the authoritative source for account information.</span></span> <span data-ttu-id="4c602-149">Cela signifie que vous effectuez des tâches d’administration principalement locales, qui sont ensuite synchronisées avec Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-149">This means that you perform administration tasks mostly on-premises, which are then synchronized to Azure AD.</span></span>

<span data-ttu-id="4c602-150">Voici les composants de l’identité hybride.</span><span class="sxs-lookup"><span data-stu-id="4c602-150">Here are the components of hybrid identity.</span></span>

![Composants de l’identité hybride](../media/about-microsoft-365-identity/hybrid-identity.png)

<span data-ttu-id="4c602-152">Le client Azure AD dispose d’une copie des comptes AD DS.</span><span class="sxs-lookup"><span data-stu-id="4c602-152">The Azure AD tenant has a copy of the AD DS accounts.</span></span> <span data-ttu-id="4c602-153">Dans cette configuration, les utilisateurs locaux et distants qui accèdent Microsoft 365 services cloud s’authentifier sur Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-153">In this configuration, both on-premises and remote users accessing Microsoft 365 cloud services authenticate against Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="4c602-154">Vous devez toujours utiliser Azure AD Connecter pour synchroniser les comptes d’utilisateur pour l’identité hybride.</span><span class="sxs-lookup"><span data-stu-id="4c602-154">You always need to use Azure AD Connect to synchronize user accounts for hybrid identity.</span></span> <span data-ttu-id="4c602-155">Vous avez besoin des comptes d’utilisateur synchronisés dans Azure AD pour effectuer l’attribution de licences et la gestion des groupes, configurer les autorisations et d’autres tâches administratives qui impliquent des comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4c602-155">You need the synchronized user accounts in Azure AD to perform license assignment and group management, configure permissions, and other administrative tasks that involve user accounts.</span></span>

### <a name="administration"></a><span data-ttu-id="4c602-156">Administration</span><span class="sxs-lookup"><span data-stu-id="4c602-156">Administration</span></span>

<span data-ttu-id="4c602-157">Étant donné que les comptes d’utilisateur d’origine et faisant autorité sont stockés dans les AD DS locales, vous gérez vos identités avec les mêmes outils que vous gérez vos AD DS.</span><span class="sxs-lookup"><span data-stu-id="4c602-157">Because the original and authoritative user accounts are stored in the on-premises AD DS, you manage your identities with the same tools as you manage your AD DS.</span></span>

<span data-ttu-id="4c602-158">Vous n’utilisez pas l’Centre d’administration Microsoft 365 ou PowerShell pour Microsoft 365 gérer les comptes d’utilisateur synchronisés dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4c602-158">You don't use the Microsoft 365 admin center or PowerShell for Microsoft 365 to manage synchronized user accounts in Azure AD.</span></span>

## <a name="next-step"></a><span data-ttu-id="4c602-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="4c602-159">Next step</span></span>

<span data-ttu-id="4c602-160">Si vous avez besoin du modèle d’identité cloud uniquement, voir [Identité cloud uniquement.](cloud-only-identities.md)</span><span class="sxs-lookup"><span data-stu-id="4c602-160">If you need the cloud-only identity model, see [Cloud-only identity](cloud-only-identities.md).</span></span>

<span data-ttu-id="4c602-161">Si vous avez besoin du modèle d’identité hybride, voir [Identité hybride.](plan-for-directory-synchronization.md)</span><span class="sxs-lookup"><span data-stu-id="4c602-161">If you need the hybrid identity model, see [Hybrid identity](plan-for-directory-synchronization.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4c602-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c602-162">See also</span></span>

[<span data-ttu-id="4c602-163">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4c602-163">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
