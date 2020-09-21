---
title: Stratégies d’accès aux identités et aux appareils pour autoriser l’accès B2B aux invités et externes-Microsoft 365 pour les entreprises | Microsoft docs
description: Décrit l’accès conditionnel et les stratégies connexes recommandées pour la protection de l’accès des utilisateurs invités et externes.
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: 6d6562f528b36acdfbc28da9647d3356a0f585af
ms.sourcegitcommit: fdb5f9d865037c0ae23aae34a5c0f06b625b2f69
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2020
ms.locfileid: "48132157"
---
# <a name="policies-for-allowing-guest-and-external-b2b-access"></a><span data-ttu-id="77e18-103">Stratégies d’autorisation d’accès B2B invité et externe</span><span class="sxs-lookup"><span data-stu-id="77e18-103">Policies for allowing guest and external B2B access</span></span>

<span data-ttu-id="77e18-104">Cet article explique comment ajuster les stratégies courantes d’identité et d’accès aux appareils pour autoriser l’accès pour les utilisateurs invités et externes disposant d’un compte entreprise-entreprise (B2B) Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="77e18-104">This article describes how to adjust the recommended common identity and device access policies to allow access for guest and external users that have an Azure Active Directory (Azure AD) Business-to-Business (B2B) account.</span></span> <span data-ttu-id="77e18-105">Ce guide s’appuie sur les [stratégies courantes d’identité et d’accès aux appareils](identity-access-policies.md).</span><span class="sxs-lookup"><span data-stu-id="77e18-105">This guidance builds on the [common identity and device access policies](identity-access-policies.md).</span></span>

<span data-ttu-id="77e18-106">Ces recommandations sont conçues pour s’appliquer au niveau de **base** de protection.</span><span class="sxs-lookup"><span data-stu-id="77e18-106">These recommendations are designed to apply to the **baseline** tier of protection.</span></span> <span data-ttu-id="77e18-107">Toutefois, vous pouvez également ajuster les recommandations en fonction de la granularité de vos besoins pour une protection **sensible** et **hautement réglementée** .</span><span class="sxs-lookup"><span data-stu-id="77e18-107">However, you can also adjust the recommendations based on the granularity of your needs for **sensitive** and **highly regulated** protection.</span></span> 

<span data-ttu-id="77e18-108">Fournir un chemin d’accès aux comptes B2B pour s’authentifier auprès de votre client Azure AD ne donne pas à ces comptes un accès à l’ensemble de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="77e18-108">Providing a path for B2B accounts to authenticate with your Azure AD tenant doesn't give these accounts access to your entire environment.</span></span> <span data-ttu-id="77e18-109">Les utilisateurs B2B et leurs comptes ont uniquement accès aux ressources qui sont partagées avec eux (par exemple, des fichiers) dans les services accordés dans les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="77e18-109">B2B users and their accounts only have access to resources that are shared with them (such as files) within the services granted in Conditional Access policies.</span></span>

## <a name="updating-the-common-policies-to-allow-and-protect-guest-and-external-access"></a><span data-ttu-id="77e18-110">Mise à jour des stratégies communes pour autoriser et protéger les accès invités et externes</span><span class="sxs-lookup"><span data-stu-id="77e18-110">Updating the common policies to allow and protect guest and external access</span></span> 

<span data-ttu-id="77e18-111">Pour protéger les accès invités et externes aux comptes B2B Azure AD, le diagramme suivant illustre les stratégies à ajouter ou à mettre à jour à partir des stratégies courantes d’identité et d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="77e18-111">To protect guest and external access with Azure AD B2B accounts, the following diagram illustrates which policies to add or update from the the common identity and device access policies.</span></span> 

<span data-ttu-id="77e18-112">[![Résumé des mises à jour de stratégie pour la protection de l’accès invité](../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span><span class="sxs-lookup"><span data-stu-id="77e18-112">[![Summary of policy updates for protecting guest access](../media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)</span></span>

[<span data-ttu-id="77e18-113">Afficher une version plus grande de cette image</span><span class="sxs-lookup"><span data-stu-id="77e18-113">See a larger version of this image</span></span>](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/microsoft-365-policies-configurations/identity-access-ruleset-guest.png)

<span data-ttu-id="77e18-114">Le tableau suivant répertorie les stratégies que vous devez créer et mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="77e18-114">The following table lists the policies you either need to create and update.</span></span> <span data-ttu-id="77e18-115">Les stratégies courantes lient aux instructions de configuration associées dans l’article [Common Identity and Device Access Policies](identity-access-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="77e18-115">The common policies link to the associated configuration instructions in the [Common identity and device access policies](identity-access-policies.md) article.</span></span>

|<span data-ttu-id="77e18-116">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="77e18-116">Protection level</span></span>|<span data-ttu-id="77e18-117">Stratégies</span><span class="sxs-lookup"><span data-stu-id="77e18-117">Policies</span></span>|<span data-ttu-id="77e18-118">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="77e18-118">More information</span></span>|
|:---------------|:-------|:----------------|
|<span data-ttu-id="77e18-119">**Baseline**</span><span class="sxs-lookup"><span data-stu-id="77e18-119">**Baseline**</span></span>|[<span data-ttu-id="77e18-120">Exiger MFA pour les utilisateurs invités et externes</span><span class="sxs-lookup"><span data-stu-id="77e18-120">Require MFA always for guest and external users</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="77e18-121">Créez cette nouvelle stratégie et configurez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="77e18-121">Create this new policy and configure:</span></span> <ul><li> <span data-ttu-id="77e18-122">Pour les **affectations > utilisateurs et groupes > inclure**, sélectionnez **Sélectionner des utilisateurs et des groupes**, puis sélectionnez **tous les utilisateurs invités et externes**.</span><span class="sxs-lookup"><span data-stu-id="77e18-122">For **Assignments > Users and groups > Include**, choose **Select users and groups**, and then select **All guest and external users**.</span></span> </li><li> <span data-ttu-id="77e18-123">Pour les **affectations > Conditions > de connexion**, laissez toutes les options désactivées pour toujours appliquer l’authentification multifacteur (MFA).</span><span class="sxs-lookup"><span data-stu-id="77e18-123">For **Assignments > Conditions > Sign-in**, leave all options unchecked to always enforce multi-factor authentication (MFA).</span></span></li>|
|        |[<span data-ttu-id="77e18-124">Exiger l’authentification multifacteur lorsque le risque de connexion est *moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="77e18-124">Require MFA when sign-in risk is *medium* or *high*</span></span>](identity-access-policies.md#require-mfa-based-on-sign-in-risk)|<span data-ttu-id="77e18-125">Modifiez cette stratégie pour exclure les utilisateurs invités et externes.</span><span class="sxs-lookup"><span data-stu-id="77e18-125">Modify this policy to exclude guest and external users.</span></span>|
|        |[<span data-ttu-id="77e18-126">Exiger des PC conformes</span><span class="sxs-lookup"><span data-stu-id="77e18-126">Require compliant PCs</span></span>](identity-access-policies.md#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="77e18-127">Modifiez cette stratégie pour exclure les utilisateurs invités et externes.</span><span class="sxs-lookup"><span data-stu-id="77e18-127">Modify this policy to exclude guest and external users.</span></span>|

<span data-ttu-id="77e18-128">Pour inclure ou exclure les utilisateurs invités et externes dans les stratégies d’accès conditionnel, pour les **affectations > utilisateurs et groupes > inclure** ou **exclure**, vérifiez **tous les utilisateurs invités et externes**.</span><span class="sxs-lookup"><span data-stu-id="77e18-128">To include or exclude guest and external users in Conditional Access policies, for **Assignments > Users and groups > Include** or **Exclude**, check **All guest and external users**.</span></span>

![capture d’écran des contrôles pour exclure les utilisateurs invités et externes](../media/microsoft-365-policies-configurations/identity-access-exclude-guests-ui.png)

## <a name="more-information"></a><span data-ttu-id="77e18-130">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="77e18-130">More information</span></span>

### <a name="guest-and-external-access-with-microsoft-teams"></a><span data-ttu-id="77e18-131">Accès invité et externe à Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="77e18-131">Guest and external access with Microsoft Teams</span></span>

<span data-ttu-id="77e18-132">Microsoft teams définit les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="77e18-132">Microsoft Teams defines the following:</span></span>

- <span data-ttu-id="77e18-133">L' **accès invité** utilise un compte Azure ad B2B pouvant être ajouté en tant que membre d’une équipe et disposer de tous les accès autorisés aux communications et aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="77e18-133">**Guest access** uses an Azure AD B2B account that can be added as a member of a team and have all permissioned access to the communications and resources of the team.</span></span>

- <span data-ttu-id="77e18-134">**L’accès externe** est destiné à un utilisateur externe qui n’a pas de compte B2B.</span><span class="sxs-lookup"><span data-stu-id="77e18-134">**External access** is for an external user that does not have a B2B account.</span></span> <span data-ttu-id="77e18-135">L’accès externe peut inclure des invitations et la participation à des appels, des conversations et des réunions, mais n’inclut pas l’appartenance aux ressources de l’équipe et l’accès aux ressources de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="77e18-135">External access can include invitations and participation in calls, chats, and meetings, but does not include team membership and access to the resources of the team.</span></span>

<span data-ttu-id="77e18-136">Pour plus d’informations, reportez-vous à [la comparaison entre invité et accès externe pour teams](https://docs.microsoft.com/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access).</span><span class="sxs-lookup"><span data-stu-id="77e18-136">For more information, see [this comparison between guest and external access for teams](https://docs.microsoft.com/microsoftteams/communicate-with-users-from-other-organizations#compare-external-and-guest-access).</span></span>

<span data-ttu-id="77e18-137">Les stratégies d’accès conditionnel ne s’appliquent qu’à l’accès invité dans Teams, car il existe un compte Azure AD B2B correspondant.</span><span class="sxs-lookup"><span data-stu-id="77e18-137">Conditional Access policies only apply to guest access in Teams because there is a corresponding Azure AD B2B account.</span></span>

<span data-ttu-id="77e18-138">Pour plus d’informations sur la sécurisation des stratégies d’accès aux identités et aux appareils pour teams [, voir recommandations de stratégie pour la sécurisation des conversations, des groupes et des fichiers teams](teams-access-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="77e18-138">See [Policy recommendations for securing Teams chats, groups, and files](teams-access-policies.md) for more information about securing identity and device access policies for Teams.</span></span>

<!--
ount treats guest and external users that have an Azure AD B2B account differently than external access  .


to a meeting, call, or chat with


differentiates between guest users and external users within the app. Guest users have Azure AD B2B accounts and can be added to teams. External users can only participate in calls, chats, and meetings. 
--> 

### <a name="require-mfa-always-for-guest-and-external-users"></a><span data-ttu-id="77e18-139">Exiger MFA pour les utilisateurs invités et externes</span><span class="sxs-lookup"><span data-stu-id="77e18-139">Require MFA always for guest and external users</span></span>
<span data-ttu-id="77e18-140">Cette stratégie invite les invités à s’inscrire à l’authentification multifacteur dans votre client, qu’ils soient inscrits pour l’authentification multifacteur dans leur client d’accueil.</span><span class="sxs-lookup"><span data-stu-id="77e18-140">This policy prompts guests to register for MFA in your tenant, regardless of whether they're registered for MFA in their home tenant.</span></span> <span data-ttu-id="77e18-141">Lors de l’accès à des ressources dans votre client, les utilisateurs invités et externes doivent utiliser l’authentification multifacteur pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="77e18-141">When accessing resources in your tenant, guest and external users are required to use MFA for every request.</span></span> 

### <a name="excluding-guest-and-external-users-from-risk-based-mfa"></a><span data-ttu-id="77e18-142">Exclusion des utilisateurs invités et externes de l’authentification multifacteur basée sur les risques</span><span class="sxs-lookup"><span data-stu-id="77e18-142">Excluding guest and external users from risk-based MFA</span></span>
<span data-ttu-id="77e18-143">Bien que les organisations puissent appliquer des stratégies basées sur les risques pour les utilisateurs B2B à l’aide d’Azure AD Identity Protection, il existe des limitations dans l’implémentation de la protection des identités Azure AD pour les utilisateurs de la collaboration B2B dans un répertoire de ressources en raison de leur identité dans leur répertoire de base.</span><span class="sxs-lookup"><span data-stu-id="77e18-143">While organizations can enforce risk-based policies for B2B users using Azure AD Identity Protection, there are limitations in the implementation of Azure AD Identity Protection for B2B collaboration users in a resource directory due to their identity existing in their home directory.</span></span> <span data-ttu-id="77e18-144">En raison de ces limitations, Microsoft vous recommande d’exclure les utilisateurs invités des stratégies MFA à risque et de leur demander d’utiliser toujours l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="77e18-144">Due to these limitations, Microsoft recommends you exclude guest users from risk-based MFA policies and require these users to always use MFA.</span></span> 

<span data-ttu-id="77e18-145">Pour plus d’informations, consultez la rubrique [limitations de la protection des identités pour les utilisateurs de collaboration B2B](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span><span class="sxs-lookup"><span data-stu-id="77e18-145">For more information, see [Limitations of Identity Protection for B2B collaboration users](https://docs.microsoft.com/azure/active-directory/identity-protection/concept-identity-protection-b2b#limitations-of-identity-protection-for-b2b-collaboration-users).</span></span> 

### <a name="excluding-guest-and-external-users-from-device-management"></a><span data-ttu-id="77e18-146">Exclusion des utilisateurs invités et externes de la gestion des appareils</span><span class="sxs-lookup"><span data-stu-id="77e18-146">Excluding guest and external users from device management</span></span> 
<span data-ttu-id="77e18-147">Une seule organisation peut gérer un appareil.</span><span class="sxs-lookup"><span data-stu-id="77e18-147">Only one organization can manage a device.</span></span> <span data-ttu-id="77e18-148">Si vous n’excluez pas les utilisateurs invités et externes des stratégies qui nécessitent une conformité de l’appareil, ces stratégies bloqueront ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="77e18-148">If you don't exclude guest and external users from policies that require device compliance, these policies will block these users.</span></span> 

## <a name="next-step"></a><span data-ttu-id="77e18-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="77e18-149">Next step</span></span>

![Étape 4 : stratégies pour les applications Cloud Microsoft 365](../media/microsoft-365-policies-configurations/identity-device-access-steps-next-step-4.png)

<span data-ttu-id="77e18-151">Configurez les stratégies d’accès conditionnel pour :</span><span class="sxs-lookup"><span data-stu-id="77e18-151">Configure Conditional Access policies for:</span></span>

- [<span data-ttu-id="77e18-152">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="77e18-152">Microsoft Teams</span></span>](teams-access-policies.md)
- [<span data-ttu-id="77e18-153">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="77e18-153">Exchange Online</span></span>](secure-email-recommended-policies.md)
- [<span data-ttu-id="77e18-154">SharePoint</span><span class="sxs-lookup"><span data-stu-id="77e18-154">SharePoint</span></span>](secure-email-recommended-policies.md)

