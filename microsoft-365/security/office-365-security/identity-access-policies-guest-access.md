---
title: Stratégies d’accès aux identités et appareils pour autoriser l’accès B2B des utilisateurs invités et externes - Microsoft 365 pour les | Documents Microsoft
description: Décrit l’accès conditionnel recommandé et les stratégies associées pour la protection de l’accès des invités et des utilisateurs externes.
ms.prod: m365-security
ms.topic: article
ms.author: josephd
author: JoeDavies-MSFT
audience: Admin
manager: Laurawi
f1.keywords:
- NOCSH
ms.reviewer: martincoetzer
ms.custom:
- it-pro
- goldenconfig
ms.collection:
- M365-identity-device-management
- M365-security-compliance
- m365solution-identitydevice
- m365solution-scenario
ms.technology: mdo
ms.openlocfilehash: 4ce52c40e622f55b0fd231ec634c4897fea1d6f5
ms.sourcegitcommit: 0ff6edbf52562138a69c6675cb0274ec984986c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2021
ms.locfileid: "51615494"
---
# <a name="policies-for-allowing-guest-access-and-b2b-external-user-access"></a><span data-ttu-id="be171-103">Stratégies d’accès invité et d’accès des utilisateurs externes B2B</span><span class="sxs-lookup"><span data-stu-id="be171-103">Policies for allowing guest access and B2B external user access</span></span>

<span data-ttu-id="be171-104">Cet article traite de l’ajustement des stratégies d’accès aux appareils et aux identités recommandées pour autoriser l’accès aux invités et aux utilisateurs externes qui ont un compte B2B (Business-to-Business) Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="be171-104">This article discusses adjusting the recommended device and identity access policies to allow access for guests and external users that have an Azure Active Directory (Azure AD) Business-to-Business (B2B) account.</span></span> <span data-ttu-id="be171-105">Ces instructions s’appuient sur les stratégies [communes d’accès aux identités et aux appareils.](identity-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="be171-105">This guidance builds on the [common identity and device access policies](identity-access-policies.md).</span></span>

<span data-ttu-id="be171-106">Ces recommandations sont conçues pour s’appliquer au **niveau de** protection de référence.</span><span class="sxs-lookup"><span data-stu-id="be171-106">These recommendations are designed to apply to the **baseline** tier of protection.</span></span> <span data-ttu-id="be171-107">Mais vous pouvez également ajuster les recommandations  en fonction de vos besoins spécifiques en matière de protection sensible et **hautement réglementée.**</span><span class="sxs-lookup"><span data-stu-id="be171-107">But you can also adjust the recommendations based on your specific needs for **sensitive** and **highly regulated** protection.</span></span>

<span data-ttu-id="be171-108">Le fait de fournir un chemin d’accès aux comptes B2B pour s’authentifier auprès de votre client Azure AD ne permet pas à ces comptes d’accéder à l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="be171-108">Providing a path for B2B accounts to authenticate with your Azure AD tenant doesn't give these accounts access to your entire environment.</span></span> <span data-ttu-id="be171-109">Les utilisateurs B2B et leurs comptes ont accès à des services et des ressources, tels que des fichiers, partagés avec eux par la stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="be171-109">B2B users and their accounts have access to services and resources, like files, shared with them by Conditional Access policy.</span></span>

## <a name="updating-the-common-policies-to-allow-and-protect-guests-and-external-user-access"></a><span data-ttu-id="be171-110">Mise à jour des stratégies courantes pour autoriser et protéger les invités et l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="be171-110">Updating the common policies to allow and protect guests and external user access</span></span>

<span data-ttu-id="be171-111">Ce diagramme montre les stratégies à ajouter ou à mettre à jour parmi les stratégies d’accès aux identités et appareils courantes, pour l’accès des invités B2B et des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="be171-111">This diagram shows which policies to add or update among the common identity and device access policies, for B2B guest and external user access.</span></span>

<span data-ttu-id="be171-112">[![Résumé des mises à jour de stratégie pour la protection de l’accès invité](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span><span class="sxs-lookup"><span data-stu-id="be171-112">[![Summary of policy updates for protecting guest access](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span></span>

<span data-ttu-id="be171-113">Le tableau suivant répertorie les stratégies que vous devez créer et mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="be171-113">The following table lists the policies you either need to create and update.</span></span> <span data-ttu-id="be171-114">Les stratégies courantes sont liées aux instructions de configuration associées dans l’article [Stratégies](identity-access-policies.md) communes d’identité et d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="be171-114">The common policies link to the associated configuration instructions in the [Common identity and device access policies](identity-access-policies.md) article.</span></span>

|<span data-ttu-id="be171-115">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="be171-115">Protection level</span></span>|<span data-ttu-id="be171-116">Stratégies</span><span class="sxs-lookup"><span data-stu-id="be171-116">Policies</span></span>|<span data-ttu-id="be171-117">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="be171-117">More information</span></span>|
|---|---|---|
|<span data-ttu-id="be171-118">**Baseline**</span><span class="sxs-lookup"><span data-stu-id="be171-118">**Baseline**</span></span>|[<span data-ttu-id="be171-119">Exiger l’mf toujours pour les invités et les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="be171-119">Require MFA always for guests and external users</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="be171-120">Créez cette stratégie et configurez :</span><span class="sxs-lookup"><span data-stu-id="be171-120">Create this new policy and configure:</span></span> <ul><li><span data-ttu-id="be171-121">Pour **les affectations > utilisateurs** et groupes > inclure, sélectionnez Sélectionner des utilisateurs et des **groupes,** puis sélectionnez Tous les utilisateurs **invités et externes.**</span><span class="sxs-lookup"><span data-stu-id="be171-121">For **Assignments > Users and groups > Include**, choose **Select users and groups**, and then select **All guest and external users**.</span></span></li><li><span data-ttu-id="be171-122">Pour **les affectations > conditions >** se connectez, laissez toutes les options désactivées pour toujours appliquer l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="be171-122">For **Assignments > Conditions > Sign-in**, leave all options unchecked to always enforce multi-factor authentication (MFA).</span></span></li></ul>|
||[<span data-ttu-id="be171-123">Exiger l’mf lorsque le risque de se connecte *est moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="be171-123">Require MFA when sign-in risk is *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="be171-124">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="be171-124">Modify this policy to exclude guests and external users.</span></span>|
||[<span data-ttu-id="be171-125">Exiger des PC conformes</span><span class="sxs-lookup"><span data-stu-id="be171-125">Require compliant PCs</span></span>](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="be171-126">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="be171-126">Modify this policy to exclude guests and external users.</span></span>|

<span data-ttu-id="be171-127">Pour inclure ou exclure des invités et des utilisateurs externes dans les stratégies d’accès conditionnel, pour affectations > Utilisateurs et groupes > Inclure ou exclure, vérifier tous les **utilisateurs invités** et  **externes.**</span><span class="sxs-lookup"><span data-stu-id="be171-127">To include or exclude guests and external users in Conditional Access policies, for **Assignments > Users and groups > Include** or **Exclude**, check **All guest and external users**.</span></span>

![capture d’écran des contrôles pour l’exclusion des invités et des utilisateurs externes](../../media/microsoft-365-policies-configurations/identity-access-exclude-guests-ui.png)

## <a name="more-information"></a><span data-ttu-id="be171-129">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="be171-129">More information</span></span>

### <a name="guests-and-external-user-access-with-microsoft-teams"></a><span data-ttu-id="be171-130">Invités et accès des utilisateurs externes avec Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be171-130">Guests and external user access with Microsoft Teams</span></span>

<span data-ttu-id="be171-131">Microsoft Teams définit les utilisateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="be171-131">Microsoft Teams defines the following users:</span></span>

- <span data-ttu-id="be171-132">**L’accès invité** utilise un compte Azure AD B2B qui peut être ajouté en tant que membre d’une équipe et qui a accès aux communications et aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="be171-132">**Guest access** uses an Azure AD B2B account that can be added as a member of a team and have access to the communications and resources of the team.</span></span>

- <span data-ttu-id="be171-133">**L’accès** externe est pour un utilisateur externe qui n’a pas de compte B2B.</span><span class="sxs-lookup"><span data-stu-id="be171-133">**External access** is for an external user that doesn't have a B2B account.</span></span> <span data-ttu-id="be171-134">L’accès des utilisateurs externes inclut les invitations, les appels, les conversations et les réunions, mais n’inclut pas l’appartenance à une équipe et l’accès aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="be171-134">External user access includes invitations, calls, chats, and meetings, but doesn't include team membership and access to the resources of the team.</span></span>

<span data-ttu-id="be171-135">Pour plus d’informations, voir la [comparaison entre les invités et l’accès des utilisateurs externes pour teams.](/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access)</span><span class="sxs-lookup"><span data-stu-id="be171-135">For more information, see the [comparison between guests and external user access for teams](/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access).</span></span>

<span data-ttu-id="be171-136">Pour plus d’informations sur la sécurisation des stratégies d’accès aux identités et aux appareils pour Teams, voir recommandations de stratégie pour la sécurisation des Teams [conversations, des groupes et des fichiers.](teams-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="be171-136">For more information on securing identity and device access policies for Teams, see [Policy recommendations for securing Teams chats, groups, and files](teams-access-policies.md).</span></span>

### <a name="require-mfa-always-for-guest-and-external-users"></a><span data-ttu-id="be171-137">Exiger toujours l’ment MFA pour les utilisateurs invités et externes</span><span class="sxs-lookup"><span data-stu-id="be171-137">Require MFA always for guest and external users</span></span>

<span data-ttu-id="be171-138">Cette stratégie invite les invités à s’inscrire à l’mf auprès de votre client, qu’ils soient inscrits ou non à l’mf dans leur client d’accueil.</span><span class="sxs-lookup"><span data-stu-id="be171-138">This policy prompts guests to register for MFA in your tenant, regardless of whether they're registered for MFA in their home tenant.</span></span> <span data-ttu-id="be171-139">Lorsque vous accédez à des ressources dans votre client, les invités et les utilisateurs externes doivent utiliser l’ation MFA pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="be171-139">When accessing resources in your tenant, guests and external users are required to use MFA for every request.</span></span>

### <a name="excluding-guests-and-external-users-from-risk-based-mfa"></a><span data-ttu-id="be171-140">Exclusion des invités et des utilisateurs externes de l’fa MFA basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="be171-140">Excluding guests and external users from risk-based MFA</span></span>

<span data-ttu-id="be171-141">Bien que les organisations peuvent appliquer des stratégies basées sur les risques pour les utilisateurs B2B à l’aide d’Azure AD Identity Protection, il existe des limitations dans l’implémentation d’Azure AD Identity Protection pour les utilisateurs de collaboration B2B dans un répertoire de ressources en raison de leur identité existante dans leur annuaire d’accueil.</span><span class="sxs-lookup"><span data-stu-id="be171-141">While organizations can enforce risk-based policies for B2B users using Azure AD Identity Protection, there are limitations in the implementation of Azure AD Identity Protection for B2B collaboration users in a resource directory due to their identity existing in their home directory.</span></span> <span data-ttu-id="be171-142">En raison de ces limitations, Microsoft vous recommande d’exclure les invités des stratégies mfa basées sur les risques et d’exiger que ces utilisateurs utilisent toujours l’mffa.</span><span class="sxs-lookup"><span data-stu-id="be171-142">Due to these limitations, Microsoft recommends you exclude guests from risk-based MFA policies and require these users to always use MFA.</span></span>

<span data-ttu-id="be171-143">Pour plus d’informations, voir [Limitations of Identity Protection for B2B collaboration users](/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span><span class="sxs-lookup"><span data-stu-id="be171-143">For more information, see [Limitations of Identity Protection for B2B collaboration users](/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span></span>

### <a name="excluding-guests-and-external-users-from-device-management"></a><span data-ttu-id="be171-144">Exclusion des invités et des utilisateurs externes de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="be171-144">Excluding guests and external users from device management</span></span>

<span data-ttu-id="be171-145">Une seule organisation peut gérer un appareil.</span><span class="sxs-lookup"><span data-stu-id="be171-145">Only one organization can manage a device.</span></span> <span data-ttu-id="be171-146">Si vous n’excluez pas les invités et les utilisateurs externes des stratégies qui nécessitent la conformité des appareils, ces stratégies bloqueront ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="be171-146">If you don't exclude guests and external users from policies that require device compliance, these policies will block these users.</span></span>

## <a name="next-step"></a><span data-ttu-id="be171-147">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="be171-147">Next step</span></span>

![Étape 4 : Stratégies pour les applications Microsoft 365 cloud et les Microsoft Cloud App Security](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

<span data-ttu-id="be171-149">Configurer des stratégies d’accès conditionnel pour :</span><span class="sxs-lookup"><span data-stu-id="be171-149">Configure Conditional Access policies for:</span></span>

- [<span data-ttu-id="be171-150">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be171-150">Microsoft Teams</span></span>](teams-access-policies.md)
- [<span data-ttu-id="be171-151">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="be171-151">Exchange Online</span></span>](secure-email-recommended-policies.md)
- [<span data-ttu-id="be171-152">SharePoint</span><span class="sxs-lookup"><span data-stu-id="be171-152">SharePoint</span></span>](sharepoint-file-access-policies.md)
- [<span data-ttu-id="be171-153">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="be171-153">Microsoft Cloud App Security</span></span>](mcas-saas-access-policies.md)
 