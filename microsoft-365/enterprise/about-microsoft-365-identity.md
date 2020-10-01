---
title: Modèles d’identité Microsoft 365 et Azure Active Directory
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
description: Découvrez comment gérer le service d’identité d’utilisateur Azure AD dans Microsoft 365 à l’aide de modèles d’identité en nuage uniquement ou hybrides.
ms.openlocfilehash: 6b5b80584408671a1925e32df1fbf458b7c16139
ms.sourcegitcommit: 04c4252457d9b976d31f53e0ba404e8f5b80d527
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2020
ms.locfileid: "48327950"
---
# <a name="microsoft-365-identity-models-and-azure-active-directory"></a><span data-ttu-id="cea1c-103">Modèles d’identité Microsoft 365 et Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="cea1c-103">Microsoft 365 identity models and Azure Active Directory</span></span>

<span data-ttu-id="cea1c-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="cea1c-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="cea1c-105">Microsoft 365 utilise Azure Active Directory (Azure AD), un service d’authentification et d’identité d’utilisateur basé sur un nuage inclus dans votre abonnement Microsoft 365, pour gérer les identités et l’authentification pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-105">Microsoft 365 uses Azure Active Directory (Azure AD), a cloud-based user identity and authentication service that is included with your Microsoft 365 subscription, to manage identities and authentication for Microsoft 365.</span></span> <span data-ttu-id="cea1c-106">L’obtention de l’infrastructure d’identité configurée correctement est essentielle à la gestion de l’accès des utilisateurs et des autorisations Microsoft 365 pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cea1c-106">Getting your identity infrastructure configured correctly is vital to managing Microsoft 365 user access and permissions for your organization.</span></span>

<span data-ttu-id="cea1c-107">Avant de commencer, regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-107">Before you begin, watch this video for an overview of identity models and authentication for Microsoft 365.</span></span>

<span data-ttu-id="cea1c-108"><p> </p></span><span class="sxs-lookup"><span data-stu-id="cea1c-108"><p> </p></span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

<span data-ttu-id="cea1c-109">Votre premier choix de planification est le modèle d’identité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-109">Your first planning choice is the Microsoft 365 identity model.</span></span>

## <a name="microsoft-365-identity-models"></a><span data-ttu-id="cea1c-110">Modèles d’identité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cea1c-110">Microsoft 365 identity models</span></span>

<span data-ttu-id="cea1c-111">Pour planifier les comptes d’utilisateur, vous devez d’abord comprendre les deux modèles d’identité dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-111">To plan for user accounts, you first need to understand the two identity models in Microsoft 365.</span></span> <span data-ttu-id="cea1c-112">Vous pouvez gérer les identités de votre organisation uniquement dans le Cloud, ou vous pouvez conserver vos identités de services de domaine Active Directory (AD DS) sur site et les utiliser pour l’authentification lorsque les utilisateurs accèdent aux services Cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-112">You can maintain your organization's identities only in the cloud, or you can maintain your on-premises Active Directory Domain Services (AD DS) identities and use them for authentication when users access Microsoft 365 cloud services.</span></span>  

<span data-ttu-id="cea1c-113">Voici les deux types d’identités, leur meilleur et leurs avantages.</span><span class="sxs-lookup"><span data-stu-id="cea1c-113">Here are the two types of identity and their best fit and benefits.</span></span>

| <span data-ttu-id="cea1c-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="cea1c-114">Attribute</span></span> | <span data-ttu-id="cea1c-115">Identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="cea1c-115">Cloud-only identity</span></span> | <span data-ttu-id="cea1c-116">Identité hybride</span><span class="sxs-lookup"><span data-stu-id="cea1c-116">Hybrid identity</span></span> |
|:-------|:-----|:-----|
| <span data-ttu-id="cea1c-117">**Définition**</span><span class="sxs-lookup"><span data-stu-id="cea1c-117">**Definition**</span></span> | <span data-ttu-id="cea1c-118">Le compte d’utilisateur existe uniquement dans le client Azure AD pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-118">User account only exists in the Azure AD tenant for your Microsoft 365 subscription.</span></span> | <span data-ttu-id="cea1c-119">Le compte d’utilisateur existe dans AD DS et une copie se trouve également dans le client Azure AD pour votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-119">User account exists in AD DS and a copy is also in the Azure AD tenant for your Microsoft 365 subscription.</span></span> <span data-ttu-id="cea1c-120">Le compte d’utilisateur dans Azure AD peut également inclure une version hachée du mot de passe du compte d’utilisateur AD DS déjà haché.</span><span class="sxs-lookup"><span data-stu-id="cea1c-120">The user account in Azure AD might also include a hashed version of the already hashed AD DS user account password.</span></span> |
| <span data-ttu-id="cea1c-121">**Comment Microsoft 365 authentifie les informations d’identification de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="cea1c-121">**How Microsoft 365 authenticates user credentials**</span></span> | <span data-ttu-id="cea1c-122">Le client Azure AD de votre abonnement Microsoft 365 effectue l’authentification avec le compte d’identité Cloud.</span><span class="sxs-lookup"><span data-stu-id="cea1c-122">The Azure AD tenant for your Microsoft 365 subscription performs the authentication with the cloud identity account.</span></span> | <span data-ttu-id="cea1c-123">Le client Azure AD de votre abonnement Microsoft 365 gère le processus d’authentification ou redirige l’utilisateur vers un autre fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="cea1c-123">The Azure AD tenant for your Microsoft 365 subscription either handles the authentication process or redirects the user to another identity provider.</span></span> |
| <span data-ttu-id="cea1c-124">**Recommandé pour**</span><span class="sxs-lookup"><span data-stu-id="cea1c-124">**Best for**</span></span> | <span data-ttu-id="cea1c-125">Organisations qui n’ont pas ou n’ont pas besoin d’un service AD DS local.</span><span class="sxs-lookup"><span data-stu-id="cea1c-125">Organizations that do not have or need an on-premises AD DS.</span></span> | <span data-ttu-id="cea1c-126">Organisations utilisant AD DS ou un autre fournisseur d’identité.</span><span class="sxs-lookup"><span data-stu-id="cea1c-126">Organizations using AD DS or another identity provider.</span></span> |
| <span data-ttu-id="cea1c-127">**Plus grand avantage**</span><span class="sxs-lookup"><span data-stu-id="cea1c-127">**Greatest benefit**</span></span> | <span data-ttu-id="cea1c-128">Simple à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cea1c-128">Simple to use.</span></span> <span data-ttu-id="cea1c-129">Aucun outil de répertoire ou serveur supplémentaire n’est requis.</span><span class="sxs-lookup"><span data-stu-id="cea1c-129">No extra directory tools or servers required.</span></span> | <span data-ttu-id="cea1c-130">Les utilisateurs peuvent utiliser les mêmes informations d’identification lors de l’accès à des ressources sur site ou en nuage.</span><span class="sxs-lookup"><span data-stu-id="cea1c-130">Users can use the same credentials when accessing on-premises or cloud-based resources.</span></span> |
||||

## <a name="cloud-only-identity"></a><span data-ttu-id="cea1c-131">Identité cloud uniquement</span><span class="sxs-lookup"><span data-stu-id="cea1c-131">Cloud-only identity</span></span>

<span data-ttu-id="cea1c-132">Une identité en nuage uniquement utilise des comptes d’utilisateur qui existent uniquement dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-132">A cloud-only identity uses user accounts that exist only in Azure AD.</span></span> <span data-ttu-id="cea1c-133">L’identité de Cloud uniquement est généralement utilisée par les petites organisations qui n’ont pas de serveurs locaux ou n’utilisent pas AD DS pour gérer les identités locales.</span><span class="sxs-lookup"><span data-stu-id="cea1c-133">Cloud-only identity is typically used by small organizations that do not have on-premises servers or do not use AD DS to manage local identities.</span></span> 

<span data-ttu-id="cea1c-134">Voici les composants de base de l’identité en nuage uniquement.</span><span class="sxs-lookup"><span data-stu-id="cea1c-134">Here are the basic components of cloud-only identity.</span></span>
 
![Composants de base de l’identité en nuage uniquement](../media/about-microsoft-365-identity/cloud-only-identity.png)

<span data-ttu-id="cea1c-136">Les utilisateurs locaux et distants (en ligne) utilisent leurs comptes d’utilisateur et mots de passe Azure AD pour accéder aux services Cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-136">Both on-premises and remote (online) users use their Azure AD user accounts and passwords to access Microsoft 365 cloud services.</span></span> <span data-ttu-id="cea1c-137">Azure AD authentifie les informations d’identification de l’utilisateur en fonction de ses comptes et mots de passe utilisateur enregistrés.</span><span class="sxs-lookup"><span data-stu-id="cea1c-137">Azure AD authenticates user credentials based on its stored user accounts and passwords.</span></span>

### <a name="administration"></a><span data-ttu-id="cea1c-138">Administration</span><span class="sxs-lookup"><span data-stu-id="cea1c-138">Administration</span></span>
<span data-ttu-id="cea1c-139">Étant donné que les comptes d’utilisateur sont stockés uniquement dans Azure AD, vous pouvez gérer les identités Cloud avec des outils tels que le [Centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/add-users/) et [Windows PowerShell](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="cea1c-139">Because user accounts are only stored in Azure AD, you manage cloud identities with tools such as the [Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/add-users/) and [Windows PowerShell](manage-user-accounts-and-licenses-with-microsoft-365-powershell.md).</span></span> 

## <a name="hybrid-identity"></a><span data-ttu-id="cea1c-140">Identité hybride</span><span class="sxs-lookup"><span data-stu-id="cea1c-140">Hybrid identity</span></span>

<span data-ttu-id="cea1c-141">L’identité hybride utilise des comptes qui proviennent d’un service AD DS local et qui disposent d’une copie dans le client Azure AD d’un abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cea1c-141">Hybrid identity uses accounts that originate in an on-premises AD DS and have a copy in the Azure AD tenant of a Microsoft 365 subscription.</span></span> <span data-ttu-id="cea1c-142">Toutefois, la plupart des modifications ne circulent qu’une seule.</span><span class="sxs-lookup"><span data-stu-id="cea1c-142">However, most changes only flow one way.</span></span> <span data-ttu-id="cea1c-143">Les modifications que vous effectuez sur les comptes d’utilisateur AD DS sont synchronisées avec leur copie dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-143">Changes that you make to AD DS user accounts are synchronized to their copy in Azure AD.</span></span> <span data-ttu-id="cea1c-144">Toutefois, les modifications apportées aux comptes en nuage dans Azure AD, telles que les nouveaux comptes d’utilisateurs, ne sont pas synchronisées avec les services AD DS.</span><span class="sxs-lookup"><span data-stu-id="cea1c-144">But changes made to cloud-based accounts in Azure AD, such as new user accounts, are not synchronized with AD DS.</span></span>

<span data-ttu-id="cea1c-145">Azure AD Connect assure la synchronisation des comptes en continu.</span><span class="sxs-lookup"><span data-stu-id="cea1c-145">Azure AD Connect provides the ongoing account synchronization.</span></span> <span data-ttu-id="cea1c-146">Il s’exécute sur un serveur local, vérifie les modifications apportées aux services de domaine Active Directory et transfère ces modifications à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-146">It runs on an on-premises server, checks for changes in the AD DS, and forwards those changes to Azure AD.</span></span> <span data-ttu-id="cea1c-147">Azure AD Connect offre la possibilité de filtrer les comptes synchronisés et de synchroniser une version hachée des mots de passe des utilisateurs, appelée synchronisation de hachage de mot de passe (hachage).</span><span class="sxs-lookup"><span data-stu-id="cea1c-147">Azure AD Connect provides the ability to filter which accounts are synchronized and whether to synchronize a hashed version of user passwords, known as password hash synchronization (PHS).</span></span>

<span data-ttu-id="cea1c-148">Lorsque vous implémentez l’identité hybride, votre service AD DS sur site est la source faisant autorité pour les informations de compte.</span><span class="sxs-lookup"><span data-stu-id="cea1c-148">When you implement hybrid identity, your on-premises AD DS is the authoritative source for account information.</span></span> <span data-ttu-id="cea1c-149">Cela signifie que vous effectuez des tâches d’administration principalement en local, qui sont ensuite synchronisées avec Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-149">This means that you perform administration tasks mostly on-premises, which are then synchronized to Azure AD.</span></span> 

<span data-ttu-id="cea1c-150">Voici les composants de l’identité hybride.</span><span class="sxs-lookup"><span data-stu-id="cea1c-150">Here are the components of hybrid identity.</span></span>

![Composants de l’identité hybride](../media/about-microsoft-365-identity/hybrid-identity.png)

<span data-ttu-id="cea1c-152">Le client Azure AD dispose d’une copie des comptes AD DS.</span><span class="sxs-lookup"><span data-stu-id="cea1c-152">The Azure AD tenant has a copy of the AD DS accounts.</span></span> <span data-ttu-id="cea1c-153">Dans cette configuration, les utilisateurs locaux et distants accèdent aux services Cloud de Microsoft 365 pour s’authentifier auprès d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-153">In this configuration, both on-premises and remote users accessing Microsoft 365 cloud services authenticate against Azure AD.</span></span>

>[!Note]
><span data-ttu-id="cea1c-154">Vous devez toujours utiliser Azure AD Connect pour synchroniser les comptes d’utilisateurs pour l’identité hybride.</span><span class="sxs-lookup"><span data-stu-id="cea1c-154">You always need to use Azure AD Connect to synchronize user accounts for hybrid identity.</span></span> <span data-ttu-id="cea1c-155">Vous avez besoin des comptes d’utilisateur synchronisés dans Azure AD pour effectuer des attributions de licences et la gestion des groupes, configurer des autorisations et d’autres tâches administratives qui impliquent des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cea1c-155">You need the synchronized user accounts in Azure AD to perform license assignment and group management, configure permissions, and other administrative tasks that involve user accounts.</span></span>
>

### <a name="administration"></a><span data-ttu-id="cea1c-156">Administration</span><span class="sxs-lookup"><span data-stu-id="cea1c-156">Administration</span></span>

<span data-ttu-id="cea1c-157">Étant donné que les comptes d’utilisateur d’origine et faisant autorité sont stockés dans le service AD DS local, vous gérez vos identités à l’aide des mêmes outils que vous gérez vos services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cea1c-157">Because the original and authoritative user accounts are stored in the on-premises AD DS, you manage your identities with the same tools as you manage your AD DS.</span></span> 

<span data-ttu-id="cea1c-158">Vous n’utilisez pas le centre d’administration Microsoft 365 ou PowerShell pour Microsoft 365 pour gérer les comptes d’utilisateur synchronisés dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cea1c-158">You don't use the Microsoft 365 admin center or PowerShell for Microsoft 365 to manage synchronized user accounts in Azure AD.</span></span>

## <a name="next-step"></a><span data-ttu-id="cea1c-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="cea1c-159">Next step</span></span>

<span data-ttu-id="cea1c-160">Si vous avez besoin du modèle d’identité Cloud uniquement, consultez la rubrique [identité en nuage uniquement](cloud-only-identities.md).</span><span class="sxs-lookup"><span data-stu-id="cea1c-160">If you need the cloud-only identity model, see [Cloud-only identity](cloud-only-identities.md).</span></span>

<span data-ttu-id="cea1c-161">Si vous avez besoin du modèle d’identité hybride, reportez-vous à la rubrique [Hybrid Identity](plan-for-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="cea1c-161">If you need the hybrid identity model, see [Hybrid identity](plan-for-directory-synchronization.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="cea1c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cea1c-162">See also</span></span>

[<span data-ttu-id="cea1c-163">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="cea1c-163">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)
