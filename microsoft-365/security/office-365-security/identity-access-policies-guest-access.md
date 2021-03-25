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
ms.openlocfilehash: 9d3a47752efc86c8ced32905bda851b7d8157f82
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204175"
---
# <a name="policies-for-allowing-guest-access-and-b2b-external-user-access"></a><span data-ttu-id="033aa-103">Stratégies d’accès invité et d’accès des utilisateurs externes B2B</span><span class="sxs-lookup"><span data-stu-id="033aa-103">Policies for allowing guest access and B2B external user access</span></span>

<span data-ttu-id="033aa-104">Cet article traite de l’ajustement des stratégies d’accès aux appareils et aux identités recommandées pour autoriser l’accès aux invités et aux utilisateurs externes qui ont un compte Azure Active Directory (Azure AD) Business-to-Business (B2B).</span><span class="sxs-lookup"><span data-stu-id="033aa-104">This article discusses adjusting the recommended device and identity access policies to allow access for guests and external users that have an Azure Active Directory (Azure AD) Business-to-Business (B2B) account.</span></span> <span data-ttu-id="033aa-105">Ces instructions s’appuient sur les stratégies [d’accès aux appareils et aux identités courantes.](identity-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="033aa-105">This guidance builds on the [common identity and device access policies](identity-access-policies.md).</span></span>

<span data-ttu-id="033aa-106">Ces recommandations sont conçues pour s’appliquer au **niveau de** protection de référence.</span><span class="sxs-lookup"><span data-stu-id="033aa-106">These recommendations are designed to apply to the **baseline** tier of protection.</span></span> <span data-ttu-id="033aa-107">Mais vous pouvez également ajuster les recommandations  en fonction de vos besoins spécifiques en matière de protection sensible et **hautement réglementée.**</span><span class="sxs-lookup"><span data-stu-id="033aa-107">But you can also adjust the recommendations based on your specific needs for **sensitive** and **highly regulated** protection.</span></span>

<span data-ttu-id="033aa-108">Le fait de fournir un chemin d’accès aux comptes B2B pour s’authentifier auprès de votre client Azure AD ne permet pas à ces comptes d’accéder à l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="033aa-108">Providing a path for B2B accounts to authenticate with your Azure AD tenant doesn't give these accounts access to your entire environment.</span></span> <span data-ttu-id="033aa-109">Les utilisateurs B2B et leurs comptes ont accès à des services et des ressources, tels que des fichiers, partagés avec eux par la stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="033aa-109">B2B users and their accounts have access to services and resources, like files, shared with them by Conditional Access policy.</span></span>

## <a name="updating-the-common-policies-to-allow-and-protect-guests-and-external-user-access"></a><span data-ttu-id="033aa-110">Mise à jour des stratégies courantes pour autoriser et protéger les invités et l’accès des utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="033aa-110">Updating the common policies to allow and protect guests and external user access</span></span>

<span data-ttu-id="033aa-111">Ce diagramme montre les stratégies à ajouter ou à mettre à jour parmi les stratégies d’accès aux identités et appareils courantes, pour l’accès des invités B2B et des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="033aa-111">This diagram shows which policies to add or update among the common identity and device access policies, for B2B guest and external user access.</span></span>

<span data-ttu-id="033aa-112">[![Résumé des mises à jour de stratégie pour la protection de l’accès invité](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span><span class="sxs-lookup"><span data-stu-id="033aa-112">[![Summary of policy updates for protecting guest access](../../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span></span>

<span data-ttu-id="033aa-113">Le tableau suivant répertorie les stratégies que vous devez créer et mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="033aa-113">The following table lists the policies you either need to create and update.</span></span> <span data-ttu-id="033aa-114">Les stratégies courantes sont liées aux instructions de configuration associées dans l’article [Stratégies](identity-access-policies.md) communes d’identité et d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="033aa-114">The common policies link to the associated configuration instructions in the [Common identity and device access policies](identity-access-policies.md) article.</span></span>

|<span data-ttu-id="033aa-115">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="033aa-115">Protection level</span></span>|<span data-ttu-id="033aa-116">Stratégies</span><span class="sxs-lookup"><span data-stu-id="033aa-116">Policies</span></span>|<span data-ttu-id="033aa-117">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="033aa-117">More information</span></span>|
|---|---|---|
|<span data-ttu-id="033aa-118">**Baseline**</span><span class="sxs-lookup"><span data-stu-id="033aa-118">**Baseline**</span></span>|[<span data-ttu-id="033aa-119">Exiger l’mf toujours pour les invités et les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="033aa-119">Require MFA always for guests and external users</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="033aa-120">Créez cette stratégie et configurez :</span><span class="sxs-lookup"><span data-stu-id="033aa-120">Create this new policy and configure:</span></span> <ul><li><span data-ttu-id="033aa-121">Pour **les affectations > utilisateurs** et groupes > inclure, sélectionnez Sélectionner des utilisateurs et des **groupes,** puis sélectionnez Tous les utilisateurs **invités et externes.**</span><span class="sxs-lookup"><span data-stu-id="033aa-121">For **Assignments > Users and groups > Include**, choose **Select users and groups**, and then select **All guest and external users**.</span></span></li><li><span data-ttu-id="033aa-122">Pour **les affectations > conditions >** se connectez, laissez toutes les options désactivées pour toujours appliquer l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="033aa-122">For **Assignments > Conditions > Sign-in**, leave all options unchecked to always enforce multi-factor authentication (MFA).</span></span></li></ul>|
||[<span data-ttu-id="033aa-123">Exiger une mfmf lorsque le risque de se connecte *est moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="033aa-123">Require MFA when sign-in risk is *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="033aa-124">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="033aa-124">Modify this policy to exclude guests and external users.</span></span>|
||[<span data-ttu-id="033aa-125">Exiger des PC conformes</span><span class="sxs-lookup"><span data-stu-id="033aa-125">Require compliant PCs</span></span>](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="033aa-126">Modifiez cette stratégie pour exclure les invités et les utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="033aa-126">Modify this policy to exclude guests and external users.</span></span>|

<span data-ttu-id="033aa-127">Pour inclure ou exclure des invités et des utilisateurs externes dans les stratégies d’accès conditionnel, pour affectations > Utilisateurs et groupes > Inclure ou exclure, vérifier tous les **utilisateurs invités** et  **externes.**</span><span class="sxs-lookup"><span data-stu-id="033aa-127">To include or exclude guests and external users in Conditional Access policies, for **Assignments > Users and groups > Include** or **Exclude**, check **All guest and external users**.</span></span>

![capture d’écran des contrôles pour l’exclusion des invités et des utilisateurs externes](../../media/microsoft-365-policies-configurations/identity-access-exclude-guests-ui.png)

## <a name="more-information"></a><span data-ttu-id="033aa-129">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="033aa-129">More information</span></span>

### <a name="guests-and-external-user-access-with-microsoft-teams"></a><span data-ttu-id="033aa-130">Invités et accès des utilisateurs externes avec Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="033aa-130">Guests and external user access with Microsoft Teams</span></span>

<span data-ttu-id="033aa-131">Microsoft Teams définit les utilisateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="033aa-131">Microsoft Teams defines the following users:</span></span>

- <span data-ttu-id="033aa-132">**L’accès invité** utilise un compte Azure AD B2B qui peut être ajouté en tant que membre d’une équipe et qui a accès aux communications et aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="033aa-132">**Guest access** uses an Azure AD B2B account that can be added as a member of a team and have access to the communications and resources of the team.</span></span>

- <span data-ttu-id="033aa-133">**L’accès** externe est pour un utilisateur externe qui n’a pas de compte B2B.</span><span class="sxs-lookup"><span data-stu-id="033aa-133">**External access** is for an external user that doesn't have a B2B account.</span></span> <span data-ttu-id="033aa-134">L’accès des utilisateurs externes inclut les invitations, les appels, les conversations et les réunions, mais n’inclut pas l’appartenance à une équipe et l’accès aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="033aa-134">External user access includes invitations, calls, chats, and meetings, but doesn't include team membership and access to the resources of the team.</span></span>

<span data-ttu-id="033aa-135">Pour plus d’informations, voir la [comparaison entre les invités et l’accès des utilisateurs externes pour teams.](/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access)</span><span class="sxs-lookup"><span data-stu-id="033aa-135">For more information, see the [comparison between guests and external user access for teams](/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access).</span></span>

<span data-ttu-id="033aa-136">Pour plus d’informations sur la sécurisation des stratégies d’accès aux identités et aux appareils pour Teams, voir recommandations de stratégie pour la [sécurisation des conversations, des groupes et des fichiers Teams.](teams-access-policies.md)</span><span class="sxs-lookup"><span data-stu-id="033aa-136">For more information on securing identity and device access policies for Teams, see [Policy recommendations for securing Teams chats, groups, and files](teams-access-policies.md).</span></span>

### <a name="require-mfa-always-for-guest-and-external-users"></a><span data-ttu-id="033aa-137">Exiger l’mf toujours pour les utilisateurs invités et externes</span><span class="sxs-lookup"><span data-stu-id="033aa-137">Require MFA always for guest and external users</span></span>

<span data-ttu-id="033aa-138">Cette stratégie invite les invités à s’inscrire à l’mf auprès de votre client, qu’ils soient inscrits ou non à l’mf dans leur client d’accueil.</span><span class="sxs-lookup"><span data-stu-id="033aa-138">This policy prompts guests to register for MFA in your tenant, regardless of whether they're registered for MFA in their home tenant.</span></span> <span data-ttu-id="033aa-139">Lorsque vous accédez à des ressources dans votre client, les invités et les utilisateurs externes doivent utiliser l’ation MFA pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="033aa-139">When accessing resources in your tenant, guests and external users are required to use MFA for every request.</span></span>

### <a name="excluding-guests-and-external-users-from-risk-based-mfa"></a><span data-ttu-id="033aa-140">Exclusion des invités et des utilisateurs externes de l’fa MFA basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="033aa-140">Excluding guests and external users from risk-based MFA</span></span>

<span data-ttu-id="033aa-141">Bien que les organisations peuvent appliquer des stratégies basées sur les risques pour les utilisateurs B2B à l’aide d’Azure AD Identity Protection, il existe des limitations dans l’implémentation d’Azure AD Identity Protection pour les utilisateurs de collaboration B2B dans un répertoire de ressources en raison de leur identité existante dans leur annuaire d’accueil.</span><span class="sxs-lookup"><span data-stu-id="033aa-141">While organizations can enforce risk-based policies for B2B users using Azure AD Identity Protection, there are limitations in the implementation of Azure AD Identity Protection for B2B collaboration users in a resource directory due to their identity existing in their home directory.</span></span> <span data-ttu-id="033aa-142">En raison de ces limitations, Microsoft vous recommande d’exclure les invités des stratégies mfa basées sur les risques et d’exiger que ces utilisateurs utilisent toujours l’mffa.</span><span class="sxs-lookup"><span data-stu-id="033aa-142">Due to these limitations, Microsoft recommends you exclude guests from risk-based MFA policies and require these users to always use MFA.</span></span>

<span data-ttu-id="033aa-143">Pour plus d’informations, voir [Limitations of Identity Protection for B2B collaboration users](/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span><span class="sxs-lookup"><span data-stu-id="033aa-143">For more information, see [Limitations of Identity Protection for B2B collaboration users](/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span></span>

### <a name="excluding-guests-and-external-users-from-device-management"></a><span data-ttu-id="033aa-144">Exclusion des invités et des utilisateurs externes de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="033aa-144">Excluding guests and external users from device management</span></span>

<span data-ttu-id="033aa-145">Une seule organisation peut gérer un appareil.</span><span class="sxs-lookup"><span data-stu-id="033aa-145">Only one organization can manage a device.</span></span> <span data-ttu-id="033aa-146">Si vous n’excluez pas les invités et les utilisateurs externes des stratégies qui nécessitent la conformité des appareils, ces stratégies bloqueront ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="033aa-146">If you don't exclude guests and external users from policies that require device compliance, these policies will block these users.</span></span>

## <a name="next-step"></a><span data-ttu-id="033aa-147">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="033aa-147">Next step</span></span>

![Étape 4 : Stratégies pour les applications cloud Microsoft 365](../../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

<span data-ttu-id="033aa-149">Configurer des stratégies d’accès conditionnel pour :</span><span class="sxs-lookup"><span data-stu-id="033aa-149">Configure Conditional Access policies for:</span></span>

- [<span data-ttu-id="033aa-150">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="033aa-150">Microsoft Teams</span></span>](teams-access-policies.md)
- [<span data-ttu-id="033aa-151">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="033aa-151">Exchange Online</span></span>](secure-email-recommended-policies.md)
- [<span data-ttu-id="033aa-152">SharePoint</span><span class="sxs-lookup"><span data-stu-id="033aa-152">SharePoint</span></span>](sharepoint-file-access-policies.md)