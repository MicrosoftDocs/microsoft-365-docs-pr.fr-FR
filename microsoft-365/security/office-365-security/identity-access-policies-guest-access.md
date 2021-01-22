---
title: Stratégies d’accès aux identités et appareils pour autoriser l’accès B2B des utilisateurs invités et externes - Microsoft 365 pour les | Documents Microsoft
description: Décrit l’accès conditionnel recommandé et les stratégies associées pour la protection de l’accès des invités et des utilisateurs externes.
ms.prod: m365-security
ms.topic: article
ms.author: josephd
author: JoeDavies-MSFT
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
ms.openlocfilehash: 2ef494f8e383f50f16b1e64f6387b6e5d62459c4
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932609"
---
# <a name="policies-for-allowing-guest-access-and-b2b-external-user-access"></a><span data-ttu-id="8510f-103">Stratégies d’accès invité et d’accès des utilisateurs externes B2B</span><span class="sxs-lookup"><span data-stu-id="8510f-103">Policies for allowing guest access and B2B external user access</span></span>

<span data-ttu-id="8510f-104">Cet article traite de l’ajustement des stratégies d’accès aux appareils et aux identités recommandées pour autoriser l’accès aux invités et aux utilisateurs externes qui ont un compte Azure Active Directory (Azure AD) Business-to-Business (B2B).</span><span class="sxs-lookup"><span data-stu-id="8510f-104">This article discusses adjusting the recommended device and identity access policies to allow access for guests and external users that have an Azure Active Directory (Azure AD) Business-to-Business (B2B) account.</span></span> <span data-ttu-id="8510f-105">Ces instructions s’appuient sur les stratégies [communes d’accès aux identités et aux appareils.](identity-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="8510f-105">This guidance builds on the [common identity and device access policies](identity-access-policies.md).</span></span>

<span data-ttu-id="8510f-106">Ces recommandations sont conçues pour s’appliquer au **niveau de** protection de référence.</span><span class="sxs-lookup"><span data-stu-id="8510f-106">These recommendations are designed to apply to the **baseline** tier of protection.</span></span> <span data-ttu-id="8510f-107">Toutefois, vous pouvez également ajuster les  recommandations en fonction de vos besoins spécifiques en matière de protection sensible et **hautement réglementée.**</span><span class="sxs-lookup"><span data-stu-id="8510f-107">But you can also adjust the recommendations based on your specific needs for **sensitive** and **highly regulated** protection.</span></span>

<span data-ttu-id="8510f-108">Le fait de fournir un chemin d’accès aux comptes B2B pour s’authentifier auprès de votre client Azure AD ne permet pas à ces comptes d’accéder à l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8510f-108">Providing a path for B2B accounts to authenticate with your Azure AD tenant doesn't give these accounts access to your entire environment.</span></span> <span data-ttu-id="8510f-109">Les utilisateurs B2B et leurs comptes ont accès à des services et des ressources, tels que des fichiers, partagés avec eux par la stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="8510f-109">B2B users and their accounts have access to services and resources, like files, shared with them by Conditional Access policy.</span></span>

## <a name="updating-the-common-policies-to-allow-and-protect-guests-and-external-user-access"></a><span data-ttu-id="8510f-110">Mise à jour des stratégies courantes pour autoriser et protéger les invités et l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="8510f-110">Updating the common policies to allow and protect guests and external user access</span></span>

<span data-ttu-id="8510f-111">Ce diagramme montre les stratégies à ajouter ou à mettre à jour parmi les stratégies d’accès aux identités et appareils courantes, pour l’accès des invités B2B et des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="8510f-111">This diagram shows which policies to add or update among the common identity and device access policies, for B2B guest and external user access.</span></span>

<span data-ttu-id="8510f-112">[![Résumé des mises à jour de stratégie pour la protection de l’accès invité](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span><span class="sxs-lookup"><span data-stu-id="8510f-112">[![Summary of policy updates for protecting guest access](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span></span>

[<span data-ttu-id="8510f-113">Voir une version plus grande de cette image</span><span class="sxs-lookup"><span data-stu-id="8510f-113">See a larger version of this image</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)

<span data-ttu-id="8510f-114">Le tableau suivant répertorie les stratégies que vous devez créer et mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="8510f-114">The following table lists the policies you either need to create and update.</span></span> <span data-ttu-id="8510f-115">Les stratégies courantes sont liées aux instructions de configuration associées dans l’article Des stratégies communes d’accès aux appareils [et aux](identity-access-policies.md) identités.</span><span class="sxs-lookup"><span data-stu-id="8510f-115">The common policies link to the associated configuration instructions in the [Common identity and device access policies](identity-access-policies.md) article.</span></span>

|<span data-ttu-id="8510f-116">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="8510f-116">Protection level</span></span>|<span data-ttu-id="8510f-117">Stratégies</span><span class="sxs-lookup"><span data-stu-id="8510f-117">Policies</span></span>|<span data-ttu-id="8510f-118">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8510f-118">More information</span></span>|
|---|---|---|
|<span data-ttu-id="8510f-119">**Baseline**</span><span class="sxs-lookup"><span data-stu-id="8510f-119">**Baseline**</span></span>|[<span data-ttu-id="8510f-120">Exiger l’mf toujours pour les invités et les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="8510f-120">Require MFA always for guests and external users</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="8510f-121">Créez cette stratégie et configurez :</span><span class="sxs-lookup"><span data-stu-id="8510f-121">Create this new policy and configure:</span></span> <ul><li><span data-ttu-id="8510f-122">Pour **les affectations > utilisateurs** et groupes > inclure, sélectionnez Sélectionner des utilisateurs et des **groupes,** puis sélectionnez Tous les utilisateurs **invités et externes.**</span><span class="sxs-lookup"><span data-stu-id="8510f-122">For **Assignments > Users and groups > Include**, choose **Select users and groups**, and then select **All guest and external users**.</span></span></li><li><span data-ttu-id="8510f-123">Pour **les affectations > conditions >** se connectez, laissez toutes les options désactivées pour toujours appliquer l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="8510f-123">For **Assignments > Conditions > Sign-in**, leave all options unchecked to always enforce multi-factor authentication (MFA).</span></span></li></ul>|
||[<span data-ttu-id="8510f-124">Exiger une mfmf lorsque le risque de se connecte *est moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="8510f-124">Require MFA when sign-in risk is *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="8510f-125">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="8510f-125">Modify this policy to exclude guests and external users.</span></span>|
||[<span data-ttu-id="8510f-126">Exiger des PC conformes</span><span class="sxs-lookup"><span data-stu-id="8510f-126">Require compliant PCs</span></span>](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="8510f-127">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="8510f-127">Modify this policy to exclude guests and external users.</span></span>|

<span data-ttu-id="8510f-128">Pour inclure ou exclure des invités et des utilisateurs externes dans les stratégies d’accès conditionnel, pour affectations > Utilisateurs et groupes > Inclure ou exclure, vérifier tous les **utilisateurs invités** et  **externes.**</span><span class="sxs-lookup"><span data-stu-id="8510f-128">To include or exclude guests and external users in Conditional Access policies, for **Assignments > Users and groups > Include** or **Exclude**, check **All guest and external users**.</span></span>

![capture d’écran des contrôles pour l’exclusion des invités et des utilisateurs externes](../../media/microsoft-365-policies-configurations/identity-access-exclude-guests-ui.png)

## <a name="more-information"></a><span data-ttu-id="8510f-130">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8510f-130">More information</span></span>

### <a name="guests-and-external-user-access-with-microsoft-teams"></a><span data-ttu-id="8510f-131">Invités et accès des utilisateurs externes avec Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8510f-131">Guests and external user access with Microsoft Teams</span></span>

<span data-ttu-id="8510f-132">Microsoft Teams définit les utilisateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="8510f-132">Microsoft Teams defines the following users:</span></span>

- <span data-ttu-id="8510f-133">**L’accès invité** utilise un compte Azure AD B2B qui peut être ajouté en tant que membre d’une équipe et qui a accès aux communications et aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="8510f-133">**Guest access** uses an Azure AD B2B account that can be added as a member of a team and have access to the communications and resources of the team.</span></span>

- <span data-ttu-id="8510f-134">**L’accès** externe est pour un utilisateur externe qui n’a pas de compte B2B.</span><span class="sxs-lookup"><span data-stu-id="8510f-134">**External access** is for an external user that doesn't have a B2B account.</span></span> <span data-ttu-id="8510f-135">L’accès des utilisateurs externes inclut les invitations, les appels, les conversations et les réunions, mais n’inclut pas l’appartenance à une équipe et l’accès aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="8510f-135">External user access includes invitations, calls, chats, and meetings, but doesn't include team membership and access to the resources of the team.</span></span>

<span data-ttu-id="8510f-136">Pour plus d’informations, voir la [comparaison entre les invités et l’accès des utilisateurs externes pour teams.](https://docs.microsoft.com/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access)</span><span class="sxs-lookup"><span data-stu-id="8510f-136">For more information, see the [comparison between guests and external user access for teams](https://docs.microsoft.com/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access).</span></span>

<span data-ttu-id="8510f-137">Pour plus d’informations sur la sécurisation des stratégies d’accès aux identités et aux appareils pour Teams, voir recommandations de stratégie pour la [sécurisation des conversations, des groupes et des fichiers Teams.](teams-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="8510f-137">For more information on securing identity and device access policies for Teams, see [Policy recommendations for securing Teams chats, groups, and files](teams-access-policies.md).</span></span>

### <a name="require-mfa-always-for-guest-and-external-users"></a><span data-ttu-id="8510f-138">Exiger l’mf toujours pour les utilisateurs invités et externes</span><span class="sxs-lookup"><span data-stu-id="8510f-138">Require MFA always for guest and external users</span></span>

<span data-ttu-id="8510f-139">Cette stratégie invite les invités à s’inscrire à l’mf auprès de votre client, qu’ils soient inscrits ou non à l’mf dans leur client d’accueil.</span><span class="sxs-lookup"><span data-stu-id="8510f-139">This policy prompts guests to register for MFA in your tenant, regardless of whether they're registered for MFA in their home tenant.</span></span> <span data-ttu-id="8510f-140">Lorsque vous accédez à des ressources dans votre client, les invités et les utilisateurs externes doivent utiliser l’ation MFA pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="8510f-140">When accessing resources in your tenant, guests and external users are required to use MFA for every request.</span></span>

### <a name="excluding-guests-and-external-users-from-risk-based-mfa"></a><span data-ttu-id="8510f-141">Exclusion des invités et des utilisateurs externes de l’fa MFA basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="8510f-141">Excluding guests and external users from risk-based MFA</span></span>

<span data-ttu-id="8510f-142">Bien que les organisations peuvent appliquer des stratégies basées sur les risques pour les utilisateurs B2B à l’aide d’Azure AD Identity Protection, il existe des limitations dans l’implémentation d’Azure AD Identity Protection pour les utilisateurs de collaboration B2B dans un répertoire de ressources en raison de leur identité existante dans leur annuaire d’accueil.</span><span class="sxs-lookup"><span data-stu-id="8510f-142">While organizations can enforce risk-based policies for B2B users using Azure AD Identity Protection, there are limitations in the implementation of Azure AD Identity Protection for B2B collaboration users in a resource directory due to their identity existing in their home directory.</span></span> <span data-ttu-id="8510f-143">En raison de ces limitations, Microsoft vous recommande d’exclure les invités des stratégies DFA basées sur les risques et d’exiger que ces utilisateurs utilisent toujours l’mffa.</span><span class="sxs-lookup"><span data-stu-id="8510f-143">Due to these limitations, Microsoft recommends you exclude guests from risk-based MFA policies and require these users to always use MFA.</span></span>

<span data-ttu-id="8510f-144">Pour plus d’informations, voir [Limitations of Identity Protection for B2B collaboration users](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span><span class="sxs-lookup"><span data-stu-id="8510f-144">For more information, see [Limitations of Identity Protection for B2B collaboration users](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span></span>

### <a name="excluding-guests-and-external-users-from-device-management"></a><span data-ttu-id="8510f-145">Exclusion des invités et des utilisateurs externes de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="8510f-145">Excluding guests and external users from device management</span></span>

<span data-ttu-id="8510f-146">Une seule organisation peut gérer un appareil.</span><span class="sxs-lookup"><span data-stu-id="8510f-146">Only one organization can manage a device.</span></span> <span data-ttu-id="8510f-147">Si vous n’excluez pas les invités et les utilisateurs externes des stratégies qui nécessitent la conformité des appareils, ces stratégies bloqueront ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8510f-147">If you don't exclude guests and external users from policies that require device compliance, these policies will block these users.</span></span>

## <a name="next-step"></a><span data-ttu-id="8510f-148">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="8510f-148">Next step</span></span>

![Étape 4 : Stratégies pour les applications cloud Microsoft 365](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

<span data-ttu-id="8510f-150">Configurer des stratégies d’accès conditionnel pour :</span><span class="sxs-lookup"><span data-stu-id="8510f-150">Configure Conditional Access policies for:</span></span>

- [<span data-ttu-id="8510f-151">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8510f-151">Microsoft Teams</span></span>](teams-access-policies.md)
- [<span data-ttu-id="8510f-152">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8510f-152">Exchange Online</span></span>](secure-email-recommended-policies.md)
- [<span data-ttu-id="8510f-153">SharePoint</span><span class="sxs-lookup"><span data-stu-id="8510f-153">SharePoint</span></span>](sharepoint-file-access-policies.md)
