---
title: Identité et périphérique courants accéder aux stratégies - Microsoft 365 entreprise | Documents Microsoft
description: Décrit les recommandations de Microsoft liées à l’application de stratégies et de configurations de l’accès aux identités et aux appareils.
author: BrendaCarter
manager: Laurawi
ms.prod: microsoft-365-enterprise
ms.topic: article
ms.author: bcarter
ms.reviewer: martincoetzer
ms.custom:
- it-pro
- goldenconfig
ms.openlocfilehash: ab8454c27cd57b6bd5cc8df6e1526ee2950ac998
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867474"
---
# <a name="common-identity-and-device-access-policies"></a><span data-ttu-id="eabc0-103">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="eabc0-103">Common identity and device access policies</span></span>
<span data-ttu-id="eabc0-104">Cet article décrit commun recommandé de stratégies pour sécuriser l’accès pour le cloud services, y compris les applications locales publiés avec le Proxy d’Application Azure AD.</span><span class="sxs-lookup"><span data-stu-id="eabc0-104">This article describes the common recommended policies for securing access to cloud services, including on-premises applications published with Azure AD Application Proxy.</span></span> 

<span data-ttu-id="eabc0-p101">Ce guide explique comment déployer les stratégies recommandées dans un environnement nouvellement mis en service. Configuration de ces stratégies dans un environnement de laboratoire distinct vous permet de comprendre et d’évaluer les stratégies recommandées avant le déploiement sur votre environnement de préproduction et de production de zone de transit. Votre environnement nouvellement mis en service peut être uniquement en nuage ou hybrides.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p101">This guidance discusses how to deploy the recommended policies in a newly-provisioned environment. Setting up these policies in a separate lab environment allows you to understand and evaluate the recommended policies before staging the rollout to your preproduction and production environments. Your newly provisioned environment may be cloud-only or hybrid.</span></span>  

## <a name="policy-set"></a><span data-ttu-id="eabc0-108">Jeu de stratégie</span><span class="sxs-lookup"><span data-stu-id="eabc0-108">Policy set</span></span> 

<span data-ttu-id="eabc0-p102">Le diagramme suivant illustre le jeu de stratégies recommandé. Il indique le niveau de protection chaque stratégie s’applique à et si les stratégies s’appliquent à PC, téléphones et tablettes ou les deux catégories de périphériques. Il indique également où ces stratégies sont configurées.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p102">The following diagram illustrates the recommended set of policies. It shows which tier of protections each policy applies to and whether the policies apply to PCs or phones and tablets, or both categories of devices. It also indicates where these policies are configured.</span></span>

![Stratégies courantes pour configurer l’accès d’identité et de périphérique](../images/Identity_device_access_policies_byplan.png)


<span data-ttu-id="eabc0-113">Le reste de cet article explique comment configurer ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="eabc0-113">The rest of this article describes how to configure these policies.</span></span> 

<span data-ttu-id="eabc0-p103">À l’aide de l’authentification multifacteur est recommandé avant inscription périphériques Intune pour l’assurance que le périphérique est en possession de l’utilisateur concerné. Vous devez également inscrire appareils dans Intune avant d’appliquer des stratégies de conformité de périphérique.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p103">Using multi-factor authentication is recommended before enrolling devices into Intune for assurance that the device is in the possession of the intended user. You must also enroll devices into Intune before enforcing device compliance policies.</span></span>

<span data-ttu-id="eabc0-p104">Pour donner à temps pour accomplir ces tâches, nous vous recommandons d’implémenter les stratégies de base dans l’ordre indiqué dans ce tableau. Toutefois, les stratégies MFA pour la protection de données sensible et réglementation peuvent être implémentés à tout moment.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p104">To give you time to accomplish these tasks, we recommend implementing the baseline policies in the order listed in this table. However, the MFA policies for sensitive and highly regulated protection can be implemented at any time.</span></span>


|<span data-ttu-id="eabc0-118">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="eabc0-118">Protection level</span></span>|<span data-ttu-id="eabc0-119">Policies</span><span class="sxs-lookup"><span data-stu-id="eabc0-119">Policies</span></span>|<span data-ttu-id="eabc0-120">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="eabc0-120">More information</span></span>|
|:---------------|:-------|:----------------|
|<span data-ttu-id="eabc0-121">**Baseline**</span><span class="sxs-lookup"><span data-stu-id="eabc0-121">**Baseline**</span></span>|[<span data-ttu-id="eabc0-122">Exiger MFA lors de la connexion risque est *moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="eabc0-122">Require MFA when sign-in risk is *medium* or *high*</span></span>](#require-mfa-based-on-sign-in-risk)| |
|        |[<span data-ttu-id="eabc0-123">Blocage des clients qui ne prennent pas en charge l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="eabc0-123">Block clients that don't support modern authentication</span></span>](#block-clients-that-dont-support-modern-authentication)|<span data-ttu-id="eabc0-124">Les clients qui n’utilisent pas l’authentification moderne peuvent contourner les règles d’accès conditionnel, il est important de bloquer les messages</span><span class="sxs-lookup"><span data-stu-id="eabc0-124">Clients that do not use modern authentication can bypass conditional access rules, so it's important to block these</span></span>|
|        |[<span data-ttu-id="eabc0-125">Utilisateurs à haut risque doivent changer le mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-125">High risk users must change password</span></span>](#high-risk-users-must-change-password)|<span data-ttu-id="eabc0-126">Oblige les utilisateurs à modifier leur mot de passe lors de la connexion en cas de détection d’activités à haut risque pour leur compte</span><span class="sxs-lookup"><span data-stu-id="eabc0-126">Forces users to change their password when signing in if high-risk activity is detected for their account</span></span>|
|        |[<span data-ttu-id="eabc0-127">Définir des stratégies de protection des applications</span><span class="sxs-lookup"><span data-stu-id="eabc0-127">Define app protection policies</span></span>](#define-app-protection-policies)|<span data-ttu-id="eabc0-128">Une stratégie par la plate-forme (iOS, Android, Windows).</span><span class="sxs-lookup"><span data-stu-id="eabc0-128">One policy per platform (iOS, Android, Windows).</span></span>|
|        |[<span data-ttu-id="eabc0-129">Exiger des applications approuvées</span><span class="sxs-lookup"><span data-stu-id="eabc0-129">Require approved apps</span></span>](#require-approved-apps)|<span data-ttu-id="eabc0-130">Applique la protection des applications mobiles pour les téléphones et les tablettes</span><span class="sxs-lookup"><span data-stu-id="eabc0-130">Enforces mobile app protection for phones and tablets</span></span>|
|        |[<span data-ttu-id="eabc0-131">Définir des stratégies de conformité de périphérique</span><span class="sxs-lookup"><span data-stu-id="eabc0-131">Define device compliance policies</span></span>](#define-device-compliance-policies)|<span data-ttu-id="eabc0-132">Une stratégie pour chaque plateforme</span><span class="sxs-lookup"><span data-stu-id="eabc0-132">One policy for each platform</span></span>|
|        |[<span data-ttu-id="eabc0-133">Exiger compatible PC</span><span class="sxs-lookup"><span data-stu-id="eabc0-133">Require compliant PCs</span></span>](#require-compliant-pcs-but-not-compliant-phones-and-tablets)|<span data-ttu-id="eabc0-134">Applique une gestion Intune de PC</span><span class="sxs-lookup"><span data-stu-id="eabc0-134">Enforces Intune management of PCs</span></span>|
|<span data-ttu-id="eabc0-135">**Sensible**</span><span class="sxs-lookup"><span data-stu-id="eabc0-135">**Sensitive**</span></span>|[<span data-ttu-id="eabc0-136">Exiger MFA lors de la connexion risque est *faible*, *moyen* ou *élevé*</span><span class="sxs-lookup"><span data-stu-id="eabc0-136">Require MFA when sign-in risk is *low*, *medium* or *high*</span></span>](#require-mfa-based-on-sign-in-risk)| |
|         |[<span data-ttu-id="eabc0-137">Exiger compatible PC *et* appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="eabc0-137">Require compliant PCs *and* mobile devices</span></span>](#require-compliant-pcs-and-mobile-devices)|<span data-ttu-id="eabc0-138">Applique la gestion Intune pour PC et téléphone/tablettes</span><span class="sxs-lookup"><span data-stu-id="eabc0-138">Enforces Intune management for PCs and phone/tablets</span></span>|
|<span data-ttu-id="eabc0-139">**Hautement réglementé**</span><span class="sxs-lookup"><span data-stu-id="eabc0-139">**Highly regulated**</span></span>|[<span data-ttu-id="eabc0-140">*Toujours* nécessitent MFA</span><span class="sxs-lookup"><span data-stu-id="eabc0-140">*Always* require MFA</span></span>](#require-mfa-based-on-sign-in-risk)|
| | |

## <a name="assigning-policies-to-users"></a><span data-ttu-id="eabc0-141">Attribution de stratégies pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-141">Assigning policies to users</span></span>
<span data-ttu-id="eabc0-p105">Avant de configurer des stratégies, identifier les groupes d’Azure Active Directory que vous utilisez pour chaque niveau de protection. En règle générale, la protection planifié s’applique à tout le monde dans l’organisation. Un utilisateur qui est inclus dans la ligne de base et protection sensible comportera toutes les stratégies de base appliqués ainsi que les stratégies sensibles. Protection est cumulative et la stratégie la plus restrictive est appliquée.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p105">Before configuring policies, identify the Azure AD groups you are using for each tier of protection. Typically, baseline protection applies to everybody in the organization. A user who is included for both baseline and sensitive protection will have all the baseline policies applied plus the sensitive policies. Protection is cumulative and the most restrictive policy is enforced.</span></span> 

<span data-ttu-id="eabc0-p106">Une pratique recommandée consiste à créer un groupe d’Azure AD à l’exclusion d’accès conditionnel. Ajoutez ce groupe à toutes les règles d’accès conditionnelle sous « Exclure ». Cela vous donne une méthode pour fournir l’accès à un utilisateur pendant que vous résoudre les problèmes d’accès. Il est recommandé comme solution temporaire. Contrôler ce groupe pour que les modifications et vérifiez que le groupe d’exclusion est utilisé uniquement comme prévu.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p106">A recommended practice is to create an Azure AD group for conditional access exclusion. Add this group to all of your conditional access rules under "Exclude". This gives you a method to provide access to a user while you troubleshoot access issues. This is recommended as a temporary solution only. Monitor this group for changes and be sure the exclusion group is being used only as intended.</span></span> 

<span data-ttu-id="eabc0-151">Le diagramme suivant fournit un exemple d’affectation de l’utilisateur et d’exclusions.</span><span class="sxs-lookup"><span data-stu-id="eabc0-151">The following diagram provides an example of user assignment and exclusions.</span></span>

![Affectation d’utilisateur exemple et des exclusions pour les règles MFA](../images/identity-access-policies-assignment.png)

<span data-ttu-id="eabc0-p107">Dans l’illustration le « équipe de projet secrète supérieure X » est affectée à une stratégie d’accès conditionnel nécessitant MFA *toujours*. Être judicieux lors de l’application des niveaux de protection supérieurs aux utilisateurs. Les membres de l’équipe du projet devront fournir deux formes d’authentification chaque fois qu’ils ouvrent une session, même si elles ne voient pas très régulé de contenu.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p107">In the illustration the "Top secret project X team" is assigned a conditional access policy that requires MFA *always*. Be judicious when applying higher levels of protection to users. Members of this project team will be required to provide two forms of authentication every time they log on, even if they are not viewing highly-regulated content.</span></span>  

<span data-ttu-id="eabc0-p108">Tous les groupes créés dans le cadre de ces recommandations d’Azure AD doivent être créés en tant que groupes d’Office 365. Il s’agit plus particulièrement important pour le déploiement de la Protection d’informations Azure (AIP) lors de la sécurisation des documents dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p108">All Azure AD groups created as part of these recommendations must be created as Office 365 groups. This is specifically important for the deployment of Azure Information Protection (AIP) when securing documents in SharePoint Online.</span></span>

![Capture d’écran de création de groupes d’Office 365](../images/identity-device-AAD-groups.png)


## <a name="require-mfa-based-on-sign-in-risk"></a><span data-ttu-id="eabc0-159">Exiger MFA basée sur les risques de connexion</span><span class="sxs-lookup"><span data-stu-id="eabc0-159">Require MFA based on sign-in risk</span></span>
<span data-ttu-id="eabc0-p109">Avant d’obliger MFA, utiliser une stratégie d’inscription MFA de Protection d’identité pour enregistrer les utilisateurs pour MFA. Une fois que les utilisateurs sont inscrits, vous pouvez appliquer MFA pour la connexion. Le [travail requis](identity-access-prerequisites.md) inclut l’inscription de tous les utilisateurs avec MFA.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p109">Before requiring MFA, first use an Identity Protection MFA registration policy to register users for MFA. After users are registered you can enforce MFA for sign-in. The [prerequisite work](identity-access-prerequisites.md) includes registering all users with MFA.</span></span>

<span data-ttu-id="eabc0-163">Pour créer une stratégie d’accès conditionnel :</span><span class="sxs-lookup"><span data-stu-id="eabc0-163">To create a new conditional access policy:</span></span> 

1. <span data-ttu-id="eabc0-p110">Accédez au [portail Azure](https://portal.azure.com)et connectez-vous avec vos informations d’identification. Une fois que vous avez correctement connecté, vous voyez le tableau de bord Azure.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p110">Go to the [Azure portal](https://portal.azure.com), and sign in with your credentials. After you've successfully signed in, you see the Azure dashboard.</span></span>

2. <span data-ttu-id="eabc0-166">Dans le menu de gauche, choisissez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-166">Choose **Azure Active Directory** from the left menu.</span></span>

3. <span data-ttu-id="eabc0-167">Sous la section **Sécurité**, choisissez **Accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-167">Under the **Security** section, choose **Conditional access**.</span></span>

4. <span data-ttu-id="eabc0-168">Choisissez **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-168">Choose **New policy**.</span></span>

![Stratégie d’accès conditionnel de base de référence](./media/secure-email/CA-EXO-policy-1.png)

 <span data-ttu-id="eabc0-170">Le tableau suivant décrit les paramètres de stratégie d’accès conditionnel à implémenter pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-170">The following tables describes the conditional access policy settings to implement for this policy.</span></span>

<span data-ttu-id="eabc0-171">**Affectations**</span><span class="sxs-lookup"><span data-stu-id="eabc0-171">**Assignments**</span></span>

|<span data-ttu-id="eabc0-172">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-172">Type</span></span>|<span data-ttu-id="eabc0-173">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-173">Properties</span></span>|<span data-ttu-id="eabc0-174">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-174">Values</span></span>|<span data-ttu-id="eabc0-175">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-175">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-176">Utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="eabc0-176">Users and groups</span></span>|<span data-ttu-id="eabc0-177">Inclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-177">Include</span></span>|<span data-ttu-id="eabc0-178">Sélectionner des utilisateurs et des groupes : sélectionnez un groupe de sécurité spécifique contenant les utilisateurs ciblés</span><span class="sxs-lookup"><span data-stu-id="eabc0-178">Select users and groups – Select specific security group containing targeted users</span></span>|<span data-ttu-id="eabc0-179">Commencer avec un groupe de sécurité comprenant les utilisateurs pilotes</span><span class="sxs-lookup"><span data-stu-id="eabc0-179">Start with security group including pilot users</span></span>|
||<span data-ttu-id="eabc0-180">Exclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-180">Exclude</span></span>|<span data-ttu-id="eabc0-181">Groupe de sécurité d’exception ; comptes de service (identités d’application)</span><span class="sxs-lookup"><span data-stu-id="eabc0-181">Exception security group; service accounts (app identities)</span></span>|<span data-ttu-id="eabc0-182">Appartenance modifié de manière temporaire selon les besoins</span><span class="sxs-lookup"><span data-stu-id="eabc0-182">Membership modified on an as-needed temporary basis</span></span>|
|<span data-ttu-id="eabc0-183">Applications cloud</span><span class="sxs-lookup"><span data-stu-id="eabc0-183">Cloud apps</span></span>|<span data-ttu-id="eabc0-184">Inclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-184">Include</span></span>|<span data-ttu-id="eabc0-p111">Sélectionnez les applications que vous souhaitez appliquer à cette règle. Par exemple, sélectionnez Office 365 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="eabc0-p111">Select the apps you want this rule to apply to. For example, select Office 365 Exchange Online</span></span>||
|<span data-ttu-id="eabc0-187">Conditions</span><span class="sxs-lookup"><span data-stu-id="eabc0-187">Conditions</span></span>|<span data-ttu-id="eabc0-188">Configuré</span><span class="sxs-lookup"><span data-stu-id="eabc0-188">Configured</span></span>|<span data-ttu-id="eabc0-189">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-189">Yes</span></span>|<span data-ttu-id="eabc0-190">Les configurer en fonction de votre environnement et de vos besoins spécifiques</span><span class="sxs-lookup"><span data-stu-id="eabc0-190">Configure specific to your environment and needs</span></span>|
|<span data-ttu-id="eabc0-191">Risque de connexion</span><span class="sxs-lookup"><span data-stu-id="eabc0-191">Sign-in risk</span></span>|<span data-ttu-id="eabc0-192">Niveau de risque</span><span class="sxs-lookup"><span data-stu-id="eabc0-192">Risk level</span></span>||<span data-ttu-id="eabc0-193">Voir les instructions dans le tableau suivant</span><span class="sxs-lookup"><span data-stu-id="eabc0-193">See the guidance in the following table</span></span>|

<span data-ttu-id="eabc0-194">**Risque de connexion**</span><span class="sxs-lookup"><span data-stu-id="eabc0-194">**Sign-in risk**</span></span>

<span data-ttu-id="eabc0-195">Appliquer les paramètres en fonction du niveau de protection que vous ciblez.</span><span class="sxs-lookup"><span data-stu-id="eabc0-195">Apply the settings based on the protection level you are targeting.</span></span>

|<span data-ttu-id="eabc0-196">Propriété</span><span class="sxs-lookup"><span data-stu-id="eabc0-196">Property</span></span>|<span data-ttu-id="eabc0-197">Niveau de protection</span><span class="sxs-lookup"><span data-stu-id="eabc0-197">Level of protection</span></span>|<span data-ttu-id="eabc0-198">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-198">Values</span></span>|<span data-ttu-id="eabc0-199">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-199">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-200">Niveau de risque</span><span class="sxs-lookup"><span data-stu-id="eabc0-200">Risk level</span></span>|<span data-ttu-id="eabc0-201">Baseline</span><span class="sxs-lookup"><span data-stu-id="eabc0-201">Baseline</span></span>|<span data-ttu-id="eabc0-202">Élevé, moyen</span><span class="sxs-lookup"><span data-stu-id="eabc0-202">High, medium</span></span>|<span data-ttu-id="eabc0-203">Cocher les deux</span><span class="sxs-lookup"><span data-stu-id="eabc0-203">Check both</span></span>|
| |<span data-ttu-id="eabc0-204">Sensible</span><span class="sxs-lookup"><span data-stu-id="eabc0-204">Sensitive</span></span>|<span data-ttu-id="eabc0-205">Élevé, moyen, faible</span><span class="sxs-lookup"><span data-stu-id="eabc0-205">High, medium, low</span></span>|<span data-ttu-id="eabc0-206">Cocher les trois</span><span class="sxs-lookup"><span data-stu-id="eabc0-206">Check all three</span></span>|
| |<span data-ttu-id="eabc0-207">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="eabc0-207">Highly regulated</span></span>| |<span data-ttu-id="eabc0-208">Laissez toutes les options désactivée pour toujours appliquer MFA</span><span class="sxs-lookup"><span data-stu-id="eabc0-208">Leave all options unchecked to always enforce MFA</span></span>|

<span data-ttu-id="eabc0-209">**Contrôles d’accès**</span><span class="sxs-lookup"><span data-stu-id="eabc0-209">**Access controls**</span></span>

|<span data-ttu-id="eabc0-210">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-210">Type</span></span>|<span data-ttu-id="eabc0-211">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-211">Properties</span></span>|<span data-ttu-id="eabc0-212">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-212">Values</span></span>|<span data-ttu-id="eabc0-213">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-213">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-214">Accorder</span><span class="sxs-lookup"><span data-stu-id="eabc0-214">Grant</span></span>|<span data-ttu-id="eabc0-215">Accorder l'accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-215">Grant access</span></span>|<span data-ttu-id="eabc0-216">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-216">True</span></span>|<span data-ttu-id="eabc0-217">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-217">Selected</span></span>|
||<span data-ttu-id="eabc0-218">Exiger MFA</span><span class="sxs-lookup"><span data-stu-id="eabc0-218">Require MFA</span></span>|<span data-ttu-id="eabc0-219">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-219">True</span></span>|<span data-ttu-id="eabc0-220">Check</span><span class="sxs-lookup"><span data-stu-id="eabc0-220">Check</span></span>|
||<span data-ttu-id="eabc0-221">Exiger l’appareil doit être marqué comme conforme</span><span class="sxs-lookup"><span data-stu-id="eabc0-221">Require device to be marked as compliant</span></span>|<span data-ttu-id="eabc0-222">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-222">False</span></span>||
||<span data-ttu-id="eabc0-223">Exiger hybride Azure périphérique joint à AD</span><span class="sxs-lookup"><span data-stu-id="eabc0-223">Require hybrid Azure AD-joined device</span></span>|<span data-ttu-id="eabc0-224">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-224">False</span></span>||
||<span data-ttu-id="eabc0-225">Exiger l’application cliente approuvée</span><span class="sxs-lookup"><span data-stu-id="eabc0-225">Require approved client app</span></span>|<span data-ttu-id="eabc0-226">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-226">False</span></span>||
||<span data-ttu-id="eabc0-227">Demander tous les contrôles sélectionnés</span><span class="sxs-lookup"><span data-stu-id="eabc0-227">Require all the selected controls</span></span>|<span data-ttu-id="eabc0-228">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-228">True</span></span>|<span data-ttu-id="eabc0-229">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-229">Selected</span></span>|

> [!NOTE]
> <span data-ttu-id="eabc0-p112">Veillez à activer cette stratégie, en cliquant **sur**. Considérez également à l’aide de l’outil [que se passe-t-il si](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) pour tester la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p112">Be sure to enable this policy, by choosing **On**. Also consider using the [What if](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) tool to test the policy.</span></span>



## <a name="block-clients-that-dont-support-modern-authentication"></a><span data-ttu-id="eabc0-232">Blocage des clients qui ne prennent pas en charge l’authentification moderne</span><span class="sxs-lookup"><span data-stu-id="eabc0-232">Block clients that don't support modern authentication</span></span>
1. <span data-ttu-id="eabc0-p113">Accédez au [portail Azure](https://portal.azure.com)et connectez-vous avec vos informations d’identification. Une fois que vous avez correctement connecté, vous voyez le tableau de bord Azure.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p113">Go to the [Azure portal](https://portal.azure.com), and sign in with your credentials. After you've successfully signed in, you see the Azure dashboard.</span></span>

2. <span data-ttu-id="eabc0-235">Dans le menu de gauche, choisissez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-235">Choose **Azure Active Directory** from the left menu.</span></span>

3. <span data-ttu-id="eabc0-236">Sous la section **Sécurité**, choisissez **Accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-236">Under the **Security** section, choose **Conditional access**.</span></span>

4. <span data-ttu-id="eabc0-237">Choisissez **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-237">Choose **New policy**.</span></span>

<span data-ttu-id="eabc0-238">Le tableau suivant décrit les paramètres de stratégie d’accès conditionnel à implémenter pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-238">The following tables describes the conditional access policy settings to implement for this policy.</span></span>

<span data-ttu-id="eabc0-239">**Affectations**</span><span class="sxs-lookup"><span data-stu-id="eabc0-239">**Assignments**</span></span>

|<span data-ttu-id="eabc0-240">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-240">Type</span></span>|<span data-ttu-id="eabc0-241">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-241">Properties</span></span>|<span data-ttu-id="eabc0-242">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-242">Values</span></span>|<span data-ttu-id="eabc0-243">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-243">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-244">Utilisateurs et groupes</span><span class="sxs-lookup"><span data-stu-id="eabc0-244">Users and groups</span></span>|<span data-ttu-id="eabc0-245">Inclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-245">Include</span></span>|<span data-ttu-id="eabc0-246">Sélectionner des utilisateurs et des groupes : sélectionnez un groupe de sécurité spécifique contenant les utilisateurs ciblés</span><span class="sxs-lookup"><span data-stu-id="eabc0-246">Select users and groups – Select specific security group containing targeted users</span></span>|<span data-ttu-id="eabc0-247">Commencer avec un groupe de sécurité comprenant les utilisateurs pilotes</span><span class="sxs-lookup"><span data-stu-id="eabc0-247">Start with security group including pilot users</span></span>|
||<span data-ttu-id="eabc0-248">Exclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-248">Exclude</span></span>|<span data-ttu-id="eabc0-249">Groupe de sécurité d’exception ; comptes de service (identités d’application)</span><span class="sxs-lookup"><span data-stu-id="eabc0-249">Exception security group; service accounts (app identities)</span></span>|<span data-ttu-id="eabc0-250">Appartenance modifiée de manière temporaire selon les besoins</span><span class="sxs-lookup"><span data-stu-id="eabc0-250">Membership modified on an as needed temporary basis</span></span>|
|<span data-ttu-id="eabc0-251">Applications cloud</span><span class="sxs-lookup"><span data-stu-id="eabc0-251">Cloud apps</span></span>|<span data-ttu-id="eabc0-252">Inclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-252">Include</span></span>|<span data-ttu-id="eabc0-p114">Sélectionnez les applications que vous souhaitez appliquer à cette règle. Par exemple, sélectionnez Office 365 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="eabc0-p114">Select the apps you want this rule to apply to. For example, select Office 365 Exchange Online</span></span>||
|<span data-ttu-id="eabc0-255">Conditions</span><span class="sxs-lookup"><span data-stu-id="eabc0-255">Conditions</span></span>|<span data-ttu-id="eabc0-256">Configuré</span><span class="sxs-lookup"><span data-stu-id="eabc0-256">Configured</span></span>|<span data-ttu-id="eabc0-257">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-257">Yes</span></span>|<span data-ttu-id="eabc0-258">Configurer des applications clientes</span><span class="sxs-lookup"><span data-stu-id="eabc0-258">Configure Client apps</span></span>|
|<span data-ttu-id="eabc0-259">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="eabc0-259">Client apps</span></span>|<span data-ttu-id="eabc0-260">Configuré</span><span class="sxs-lookup"><span data-stu-id="eabc0-260">Configured</span></span>|<span data-ttu-id="eabc0-261">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-261">Yes</span></span>|<span data-ttu-id="eabc0-262">Les applications mobiles et les clients de bureau, autres clients (Sélectionner les deux)</span><span class="sxs-lookup"><span data-stu-id="eabc0-262">Mobile apps and desktop clients, Other clients (select both)</span></span>|

<span data-ttu-id="eabc0-263">**Contrôles d’accès**</span><span class="sxs-lookup"><span data-stu-id="eabc0-263">**Access controls**</span></span>

|<span data-ttu-id="eabc0-264">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-264">Type</span></span>|<span data-ttu-id="eabc0-265">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-265">Properties</span></span>|<span data-ttu-id="eabc0-266">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-266">Values</span></span>|<span data-ttu-id="eabc0-267">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-267">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-268">Accorder</span><span class="sxs-lookup"><span data-stu-id="eabc0-268">Grant</span></span>|<span data-ttu-id="eabc0-269">Bloquer l’accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-269">Block access</span></span>|<span data-ttu-id="eabc0-270">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-270">True</span></span>|<span data-ttu-id="eabc0-271">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-271">Selected</span></span>|
||<span data-ttu-id="eabc0-272">Exiger MFA</span><span class="sxs-lookup"><span data-stu-id="eabc0-272">Require MFA</span></span>|<span data-ttu-id="eabc0-273">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-273">False</span></span>||
||<span data-ttu-id="eabc0-274">Exiger l’appareil doit être marqué comme conforme</span><span class="sxs-lookup"><span data-stu-id="eabc0-274">Require device to be marked as compliant</span></span>|<span data-ttu-id="eabc0-275">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-275">False</span></span>||
||<span data-ttu-id="eabc0-276">Exiger hybride Azure périphérique joint à AD</span><span class="sxs-lookup"><span data-stu-id="eabc0-276">Require hybrid Azure AD-joined device</span></span>|<span data-ttu-id="eabc0-277">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-277">False</span></span>||
||<span data-ttu-id="eabc0-278">Exiger l’application cliente approuvée</span><span class="sxs-lookup"><span data-stu-id="eabc0-278">Require approved client app</span></span>|<span data-ttu-id="eabc0-279">False</span><span class="sxs-lookup"><span data-stu-id="eabc0-279">False</span></span>||
||<span data-ttu-id="eabc0-280">Demander tous les contrôles sélectionnés</span><span class="sxs-lookup"><span data-stu-id="eabc0-280">Require all the selected controls</span></span>|<span data-ttu-id="eabc0-281">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-281">True</span></span>|<span data-ttu-id="eabc0-282">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-282">Selected</span></span>|

> [!NOTE]
> <span data-ttu-id="eabc0-p115">Veillez à activer cette stratégie, en cliquant **sur**. Considérez également à l’aide de l’outil [que se passe-t-il si](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) pour tester la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p115">Be sure to enable this policy, by choosing **On**. Also consider using the [What if](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) tool to test the policy.</span></span>



## <a name="high-risk-users-must-change-password"></a><span data-ttu-id="eabc0-285">Utilisateurs à haut risque doivent changer le mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-285">High risk users must change password</span></span>
<span data-ttu-id="eabc0-286">Pour vous assurer que les comptes des compromis tous les utilisateurs à haut risque sont obligés pour effectuer une modification de mot de passe lors de la connexion, vous devez appliquer la stratégie suivante.</span><span class="sxs-lookup"><span data-stu-id="eabc0-286">To ensure that all high-risk users' compromised accounts are forced to perform a password change when signing-in, you must apply the following policy.</span></span>

<span data-ttu-id="eabc0-287">Connectez-vous à le [portail Microsoft Azure (http://portal.azure.com) ](http://portal.azure.com/) avec vos informations d’identification d’administrateur, puis accédez à **Azure AD identité Protection > stratégie risque de l’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-287">Log in to the [Microsoft Azure portal (http://portal.azure.com)](http://portal.azure.com/) with your administrator credentials, and then navigate to **Azure AD Identity Protection > User Risk Policy**.</span></span>

<span data-ttu-id="eabc0-288">**Affectations**</span><span class="sxs-lookup"><span data-stu-id="eabc0-288">**Assignments**</span></span>

|<span data-ttu-id="eabc0-289">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-289">Type</span></span>|<span data-ttu-id="eabc0-290">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-290">Properties</span></span>|<span data-ttu-id="eabc0-291">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-291">Values</span></span>|<span data-ttu-id="eabc0-292">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-292">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-293">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-293">Users</span></span>|<span data-ttu-id="eabc0-294">Inclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-294">Include</span></span>|<span data-ttu-id="eabc0-295">Tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-295">All users</span></span>|<span data-ttu-id="eabc0-296">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-296">Selected</span></span>|
||<span data-ttu-id="eabc0-297">Exclure</span><span class="sxs-lookup"><span data-stu-id="eabc0-297">Exclude</span></span>|<span data-ttu-id="eabc0-298">Aucune</span><span class="sxs-lookup"><span data-stu-id="eabc0-298">None</span></span>||
|<span data-ttu-id="eabc0-299">Conditions</span><span class="sxs-lookup"><span data-stu-id="eabc0-299">Conditions</span></span>|<span data-ttu-id="eabc0-300">Risque de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eabc0-300">User risk</span></span>|<span data-ttu-id="eabc0-301">Importante</span><span class="sxs-lookup"><span data-stu-id="eabc0-301">High</span></span>|<span data-ttu-id="eabc0-302">Sélectionné</span><span class="sxs-lookup"><span data-stu-id="eabc0-302">Selected</span></span>|

<span data-ttu-id="eabc0-303">**Contrôles**</span><span class="sxs-lookup"><span data-stu-id="eabc0-303">**Controls**</span></span>

| <span data-ttu-id="eabc0-304">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-304">Type</span></span> | <span data-ttu-id="eabc0-305">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-305">Properties</span></span> | <span data-ttu-id="eabc0-306">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-306">Values</span></span>                  | <span data-ttu-id="eabc0-307">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-307">Notes</span></span> |
|:-----|:-----------|:------------------------|:------|
|      | <span data-ttu-id="eabc0-308">Accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-308">Access</span></span>     | <span data-ttu-id="eabc0-309">Autoriser l'accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-309">Allow access</span></span>            | <span data-ttu-id="eabc0-310">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-310">True</span></span>  |
|      | <span data-ttu-id="eabc0-311">Accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-311">Access</span></span>     | <span data-ttu-id="eabc0-312">Exiger le changement du mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-312">Require password change</span></span> | <span data-ttu-id="eabc0-313">True</span><span class="sxs-lookup"><span data-stu-id="eabc0-313">True</span></span>  |

<span data-ttu-id="eabc0-314">**Révision :** non applicable</span><span class="sxs-lookup"><span data-stu-id="eabc0-314">**Review:** not applicable</span></span>

> [!NOTE]
> <span data-ttu-id="eabc0-p116">Veillez à activer cette stratégie, en cliquant **sur**. Également prendre en compte à l’aide de l’outil [que se passe-t-il si](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) pour tester la stratégie</span><span class="sxs-lookup"><span data-stu-id="eabc0-p116">Be sure to enable this policy, by choosing **On**. Also consider using the [What if](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-whatif) tool to test the policy</span></span>

## <a name="define-app-protection-policies"></a><span data-ttu-id="eabc0-317">Définir des stratégies de protection des applications</span><span class="sxs-lookup"><span data-stu-id="eabc0-317">Define app protection policies</span></span>
<span data-ttu-id="eabc0-p117">Stratégies de protection des applications permet de définir les applications qui sont autorisées et les actions qu’elle peut prendre des données de votre organisation. Créer des stratégies de protection à partir du portail Azure Intune application.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p117">App protection policies define which apps are allowed and the actions they can take with your organization's data. Create Intune app protection policies from within the Azure portal.</span></span> 

<span data-ttu-id="eabc0-320">Créer une stratégie pour chaque plateforme :</span><span class="sxs-lookup"><span data-stu-id="eabc0-320">Create a policy for each platform:</span></span>
- <span data-ttu-id="eabc0-321">iOS</span><span class="sxs-lookup"><span data-stu-id="eabc0-321">iOS</span></span>
- <span data-ttu-id="eabc0-322">Android</span><span class="sxs-lookup"><span data-stu-id="eabc0-322">Android</span></span>
- <span data-ttu-id="eabc0-323">Windows 10</span><span class="sxs-lookup"><span data-stu-id="eabc0-323">Windows 10</span></span>

<span data-ttu-id="eabc0-p118">Pour créer une nouvelle stratégie de protection d’application, connectez-vous au portail Microsoft Azure avec vos informations d’identification d’administration, puis accédez à **applications mobiles > stratégies de protection des applications**. Cliquez sur **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p118">To create a new app protection policy, log in to the Microsoft Azure portal with your administer credentials, and then navigate to **Mobile apps > App protection policies**. Choose **Add a policy**.</span></span>

<span data-ttu-id="eabc0-p119">Il existe de légères différences dans la protection de l’application options de stratégie entre iOS et Android. L’au-dessous stratégie est spécifiquement conçu pour Android. Utilisez cette classe comme un guide pour vos autres stratégies.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p119">There are slight differences in the app protection policy options between iOS and Android. The below policy is specifically for Android. Use this as a guide for your other policies.</span></span>

<span data-ttu-id="eabc0-329">La liste des applications recommandée inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="eabc0-329">The recommended list of apps includes the following:</span></span>
- <span data-ttu-id="eabc0-330">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="eabc0-330">PowerPoint</span></span>
- <span data-ttu-id="eabc0-331">Excel</span><span class="sxs-lookup"><span data-stu-id="eabc0-331">Excel</span></span>
- <span data-ttu-id="eabc0-332">Word</span><span class="sxs-lookup"><span data-stu-id="eabc0-332">Word</span></span>
- <span data-ttu-id="eabc0-333">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="eabc0-333">Microsoft Teams</span></span>
- <span data-ttu-id="eabc0-334">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="eabc0-334">Microsoft SharePoint</span></span>
- <span data-ttu-id="eabc0-335">Visionneuse Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="eabc0-335">Microsoft Visio Viewer</span></span>
- <span data-ttu-id="eabc0-336">OneDrive</span><span class="sxs-lookup"><span data-stu-id="eabc0-336">OneDrive</span></span>
- <span data-ttu-id="eabc0-337">OneNote</span><span class="sxs-lookup"><span data-stu-id="eabc0-337">OneNote</span></span>
- <span data-ttu-id="eabc0-338">Outlook</span><span class="sxs-lookup"><span data-stu-id="eabc0-338">Outlook</span></span>

<span data-ttu-id="eabc0-339">Les tableaux suivants décrivent les paramètres recommandés :</span><span class="sxs-lookup"><span data-stu-id="eabc0-339">The following tables describe the recommended settings:</span></span>

|<span data-ttu-id="eabc0-340">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-340">Type</span></span>|<span data-ttu-id="eabc0-341">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-341">Properties</span></span>|<span data-ttu-id="eabc0-342">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-342">Values</span></span>|<span data-ttu-id="eabc0-343">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-343">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-344">Réadressage des données</span><span class="sxs-lookup"><span data-stu-id="eabc0-344">Data relocation</span></span>|<span data-ttu-id="eabc0-345">Interdire la sauvegarde Android</span><span class="sxs-lookup"><span data-stu-id="eabc0-345">Prevent Android backup</span></span>|<span data-ttu-id="eabc0-346">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-346">Yes</span></span>|<span data-ttu-id="eabc0-347">Sur iOS, ceci appelle spécifiquement iTunes et iCloud</span><span class="sxs-lookup"><span data-stu-id="eabc0-347">On iOS this will specifically call out iTunes and iCloud</span></span>|
||<span data-ttu-id="eabc0-348">Autoriser l'application à transférer des données vers d'autres applications</span><span class="sxs-lookup"><span data-stu-id="eabc0-348">Allow app to transfer data to other apps</span></span>|<span data-ttu-id="eabc0-349">Applications gérées par la stratégie</span><span class="sxs-lookup"><span data-stu-id="eabc0-349">Policy managed apps</span></span>||
||<span data-ttu-id="eabc0-350">Autoriser l'application à recevoir des données d'autres applications</span><span class="sxs-lookup"><span data-stu-id="eabc0-350">Allow app to receive data from other apps</span></span>|<span data-ttu-id="eabc0-351">Applications gérées par la stratégie</span><span class="sxs-lookup"><span data-stu-id="eabc0-351">Policy managed apps</span></span>||
||<span data-ttu-id="eabc0-352">Interdire l’option Enregistrer sous</span><span class="sxs-lookup"><span data-stu-id="eabc0-352">Prevent "Save As"</span></span>|<span data-ttu-id="eabc0-353">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-353">Yes</span></span>||
||<span data-ttu-id="eabc0-354">Sélectionnez dans quels services de stockage les données d'entreprise peuvent être enregistrées</span><span class="sxs-lookup"><span data-stu-id="eabc0-354">Select which storage services corporate data can be saved to</span></span>|<span data-ttu-id="eabc0-355">OneDrive entreprise, SharePoint</span><span class="sxs-lookup"><span data-stu-id="eabc0-355">OneDrive for Business, SharePoint</span></span>||
||<span data-ttu-id="eabc0-356">Restreindre les opérations Couper, Copier et Coller avec d’autres applications</span><span class="sxs-lookup"><span data-stu-id="eabc0-356">Restrict cut, copy, and paste with other apps</span></span>|<span data-ttu-id="eabc0-357">Applications avec coller dans géré de stratégie</span><span class="sxs-lookup"><span data-stu-id="eabc0-357">Policy managed apps with paste in</span></span>||
||<span data-ttu-id="eabc0-358">Afficher le contenu web uniquement dans Managed Browser</span><span class="sxs-lookup"><span data-stu-id="eabc0-358">Restrict web content to display in the managed browser</span></span>|<span data-ttu-id="eabc0-359">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-359">No</span></span>||
||<span data-ttu-id="eabc0-360">Chiffrer les données de l'application</span><span class="sxs-lookup"><span data-stu-id="eabc0-360">Encrypt app data</span></span>|<span data-ttu-id="eabc0-361">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-361">Yes</span></span>|<span data-ttu-id="eabc0-362">Sur iOS, sélectionner l’option Quand l’appareil est verrouillé</span><span class="sxs-lookup"><span data-stu-id="eabc0-362">On iOS select option: When device is locked</span></span>|
||<span data-ttu-id="eabc0-363">Désactiver le chiffrement de l’application lorsque le périphérique est activé.</span><span class="sxs-lookup"><span data-stu-id="eabc0-363">Disable app encryption when device is enabled</span></span>|<span data-ttu-id="eabc0-364">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-364">Yes</span></span>|<span data-ttu-id="eabc0-365">Désactivez ce paramètre pour éviter la double chiffrement</span><span class="sxs-lookup"><span data-stu-id="eabc0-365">Disable this setting to avoid double encryption</span></span>|
||<span data-ttu-id="eabc0-366">Désactiver la synchronisation des contacts</span><span class="sxs-lookup"><span data-stu-id="eabc0-366">Disable contacts sync</span></span>|<span data-ttu-id="eabc0-367">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-367">No</span></span>||
||<span data-ttu-id="eabc0-368">Désactiver l’impression</span><span class="sxs-lookup"><span data-stu-id="eabc0-368">Disable printing</span></span>|<span data-ttu-id="eabc0-369">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-369">No</span></span>||
|<span data-ttu-id="eabc0-370">Accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-370">Access</span></span>|<span data-ttu-id="eabc0-371">Exiger un code confidentiel d’accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-371">Require PIN for access</span></span>|<span data-ttu-id="eabc0-372">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-372">Yes</span></span>||
||<span data-ttu-id="eabc0-373">Sélectionnez Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-373">Select Type</span></span>|<span data-ttu-id="eabc0-374">Numérique</span><span class="sxs-lookup"><span data-stu-id="eabc0-374">Numeric</span></span>||
||<span data-ttu-id="eabc0-375">Autoriser un code PIN simple</span><span class="sxs-lookup"><span data-stu-id="eabc0-375">Allow simple PIN</span></span>|<span data-ttu-id="eabc0-376">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-376">No</span></span>||
||<span data-ttu-id="eabc0-377">Longueur du code PIN</span><span class="sxs-lookup"><span data-stu-id="eabc0-377">PIN length</span></span>|<span data-ttu-id="eabc0-378">6</span><span class="sxs-lookup"><span data-stu-id="eabc0-378">6</span></span>||
||<span data-ttu-id="eabc0-379">Autoriser une empreinte digitale à la place du code confidentiel</span><span class="sxs-lookup"><span data-stu-id="eabc0-379">Allow fingerprint instead of PIN</span></span>|<span data-ttu-id="eabc0-380">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-380">Yes</span></span>||
||<span data-ttu-id="eabc0-381">Désactiver le code confidentiel d’application lorsque le code confidentiel du périphérique est géré</span><span class="sxs-lookup"><span data-stu-id="eabc0-381">Disable app PIN when device PIN is managed</span></span>|<span data-ttu-id="eabc0-382">Oui</span><span class="sxs-lookup"><span data-stu-id="eabc0-382">Yes</span></span>||
||<span data-ttu-id="eabc0-383">Exiger des informations d’identification d’entreprise pour l’accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-383">Require corporate credentials for access</span></span>|<span data-ttu-id="eabc0-384">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-384">No</span></span>||
||<span data-ttu-id="eabc0-385">Revérifier l’exigence d’accès après (minutes)</span><span class="sxs-lookup"><span data-stu-id="eabc0-385">Recheck the access requirement after (minutes)</span></span>|<span data-ttu-id="eabc0-386">30</span><span class="sxs-lookup"><span data-stu-id="eabc0-386">30</span></span>||
||<span data-ttu-id="eabc0-387">Bloquer la capture d’écran et l’Assistant Android</span><span class="sxs-lookup"><span data-stu-id="eabc0-387">Block screen capture and Android assistant</span></span>|<span data-ttu-id="eabc0-388">Non</span><span class="sxs-lookup"><span data-stu-id="eabc0-388">No</span></span>|<span data-ttu-id="eabc0-389">Sur iOS, cette option n’est pas disponible</span><span class="sxs-lookup"><span data-stu-id="eabc0-389">On iOS this is not an available option</span></span>|
|<span data-ttu-id="eabc0-390">Exigences de sécurité de connexion</span><span class="sxs-lookup"><span data-stu-id="eabc0-390">Sign-in security requirements</span></span>|<span data-ttu-id="eabc0-391">Tente de code confidentiel max</span><span class="sxs-lookup"><span data-stu-id="eabc0-391">Max PIN attempts</span></span>|<span data-ttu-id="eabc0-392">5</span><span class="sxs-lookup"><span data-stu-id="eabc0-392">5</span></span>|<span data-ttu-id="eabc0-393">Réinitialiser le code confidentiel</span><span class="sxs-lookup"><span data-stu-id="eabc0-393">Reset Pin</span></span>|
||<span data-ttu-id="eabc0-394">Période de grâce hors connexion</span><span class="sxs-lookup"><span data-stu-id="eabc0-394">Offline grace period</span></span>|<span data-ttu-id="eabc0-395">720</span><span class="sxs-lookup"><span data-stu-id="eabc0-395">720</span></span>|<span data-ttu-id="eabc0-396">Bloquer l’accès</span><span class="sxs-lookup"><span data-stu-id="eabc0-396">Block access</span></span>|
||<span data-ttu-id="eabc0-397">Intervalle hors connexion (jours) avant la réinitialisation des données d'application</span><span class="sxs-lookup"><span data-stu-id="eabc0-397">Offline interval (days) before app data is wiped</span></span>|<span data-ttu-id="eabc0-398">90</span><span class="sxs-lookup"><span data-stu-id="eabc0-398">90</span></span>|<span data-ttu-id="eabc0-399">Effacer les données</span><span class="sxs-lookup"><span data-stu-id="eabc0-399">Wipe data</span></span>|
||<span data-ttu-id="eabc0-400">Jailbroken/fait en sorte que les périphériques</span><span class="sxs-lookup"><span data-stu-id="eabc0-400">Jailbroken/rooted devices</span></span>| |<span data-ttu-id="eabc0-401">Effacer les données</span><span class="sxs-lookup"><span data-stu-id="eabc0-401">Wipe data</span></span>|

<span data-ttu-id="eabc0-p120">Lorsque vous avez terminé, pensez à sélectionner « Créer ». Répétez les étapes ci-dessus en remplaçant la plate-forme sélectionnée (liste déroulante) iOS. Cette opération crée deux stratégies d’application, donc une fois que vous créez la stratégie, puis affecter des groupes à la stratégie et la déployer.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p120">When complete, remember to select "Create". Repeat the above steps and replace the selected platform (dropdown) with iOS. This creates two app policies, so once you create the policy, then assign groups to the policy and deploy it.</span></span>

<span data-ttu-id="eabc0-405">Pour modifier les stratégies et affecter ces stratégies aux utilisateurs, voir [comment créer et affecter des stratégies de protection des applications](https://docs.microsoft.com/intune/app-protection-policies).</span><span class="sxs-lookup"><span data-stu-id="eabc0-405">To edit the policies and assign these policies to users, see [How to create and assign app protection policies](https://docs.microsoft.com/intune/app-protection-policies).</span></span> 

## <a name="require-approved-apps"></a><span data-ttu-id="eabc0-406">Exiger des applications approuvées</span><span class="sxs-lookup"><span data-stu-id="eabc0-406">Require approved apps</span></span>
<span data-ttu-id="eabc0-407">Pour exiger que les applications approuvées :</span><span class="sxs-lookup"><span data-stu-id="eabc0-407">To require approved apps:</span></span>

1. <span data-ttu-id="eabc0-p121">Accédez au [portail Azure](https://portal.azure.com)et connectez-vous avec vos informations d’identification. Une fois que vous avez correctement connecté, vous voyez le tableau de bord Azure.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p121">Go to the [Azure portal](https://portal.azure.com), and sign in with your credentials. After you've successfully signed in, you see the Azure dashboard.</span></span>

2. <span data-ttu-id="eabc0-410">Dans le menu de gauche, choisissez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-410">Choose **Azure Active Directory** from the left menu.</span></span>

3. <span data-ttu-id="eabc0-411">Sous la section **Sécurité**, choisissez **Accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-411">Under the **Security** section, choose **Conditional access**.</span></span>

4. <span data-ttu-id="eabc0-412">Choisissez **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-412">Choose **New policy**.</span></span>

5. <span data-ttu-id="eabc0-413">Entrez un nom de stratégie et choisissez les **Utilisateurs et groupes** auxquels vous souhaitez appliquer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-413">Enter a policy name, then choose the **Users and groups** you want to apply the policy for.</span></span>

6. <span data-ttu-id="eabc0-414">Choisissez **Applications cloud**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-414">Choose **Cloud apps**.</span></span>

7. <span data-ttu-id="eabc0-p122">Choisissez **Sélectionner les applications**, sélectionnez les applications de votre choix dans la liste des **applications dans le nuage** . Par exemple, sélectionnez Office 365 Exchange Online. Choisissez **Sélectionnez** **terminé**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p122">Choose **Select apps**, select the desired apps from the **Cloud apps** list. For example, select Office 365 Exchange Online. Choose **Select** and **Done**.</span></span>

8. <span data-ttu-id="eabc0-418">Choisissez **Accorder** dans la section **Contrôles d’accès**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-418">Choose **Grant** from the **Access controls** section.</span></span>

9. <span data-ttu-id="eabc0-p123">Cliquez sur **accorder l’accès**, sélectionnez **Exiger l’approbation de l’application cliente**. Pour plusieurs contrôles, sélectionnez **Exiger les contrôles sélectionnés**, puis choisissez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p123">Choose **Grant access**, select **Require approved client app**. For multiple controls, select **Require the selected controls**, then choose **Select**.</span></span> 

10. <span data-ttu-id="eabc0-421">Sélectionnez **Create (Créer)**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-421">Choose **Create**.</span></span>

## <a name="define-device-compliance-policies"></a><span data-ttu-id="eabc0-422">Définir des stratégies de conformité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="eabc0-422">Define device-compliance policies</span></span>

<span data-ttu-id="eabc0-p124">Stratégies de conformité de l’appareil définissent les exigences qui doivent respecter les appareils afin d’être marqué comme conforme. Créer des stratégies de conformité à partir du portail Azure Intune périphérique.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p124">Device-compliance policies define the requirements that devices must adhere to in order to be marked as compliant. Create Intune device compliance policies from within the Azure portal.</span></span> 

<span data-ttu-id="eabc0-425">Créer une stratégie pour chaque plateforme :</span><span class="sxs-lookup"><span data-stu-id="eabc0-425">Create a policy for each platform:</span></span>
- <span data-ttu-id="eabc0-426">Android</span><span class="sxs-lookup"><span data-stu-id="eabc0-426">Android</span></span>
- <span data-ttu-id="eabc0-427">Entreprise Android</span><span class="sxs-lookup"><span data-stu-id="eabc0-427">Android enterprise</span></span>
- <span data-ttu-id="eabc0-428">iOS</span><span class="sxs-lookup"><span data-stu-id="eabc0-428">iOS</span></span>
- <span data-ttu-id="eabc0-429">Mac OS</span><span class="sxs-lookup"><span data-stu-id="eabc0-429">macOS</span></span>
- <span data-ttu-id="eabc0-430">Windows Phone 8.1</span><span class="sxs-lookup"><span data-stu-id="eabc0-430">Windows Phone 8.1</span></span>
- <span data-ttu-id="eabc0-431">Windows 8.1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="eabc0-431">Windows 8.1 and later</span></span>
- <span data-ttu-id="eabc0-432">Windows 10 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="eabc0-432">Windows 10 and later</span></span>

<span data-ttu-id="eabc0-p125">Pour créer des stratégies de conformité appareil, connectez-vous au portail Microsoft Azure avec vos informations d’identification d’administration, puis accédez à **Intune > conformité périphérique**. Sélectionnez **créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p125">To create device compliance policies, log in to the Microsoft Azure portal with your administer credentials, and then navigate to **Intune > Device compliance**. Select **Create policy**.</span></span>

<span data-ttu-id="eabc0-435">Les paramètres suivants sont recommandés pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="eabc0-435">The following settings are recommended for Windows 10.</span></span>

<span data-ttu-id="eabc0-436">**État de santé : règles d’évaluation de Service de Attestation d’intégrité de Windows**</span><span class="sxs-lookup"><span data-stu-id="eabc0-436">**Device health: Windows Health Attestation Service evaluation rules**</span></span>

|<span data-ttu-id="eabc0-437">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-437">Properties</span></span>|<span data-ttu-id="eabc0-438">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-438">Values</span></span>|<span data-ttu-id="eabc0-439">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-439">Notes</span></span>|
|:---------|:-----|:----|
|<span data-ttu-id="eabc0-440">Exiger BitLocker</span><span class="sxs-lookup"><span data-stu-id="eabc0-440">Require BitLocker</span></span>|<span data-ttu-id="eabc0-441">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-441">Require</span></span>||
|<span data-ttu-id="eabc0-442">Exiger Secure au démarrage être activé sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="eabc0-442">Require Secure Boot to be enabled on the device</span></span>|<span data-ttu-id="eabc0-443">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-443">Require</span></span>||
|<span data-ttu-id="eabc0-444">Exiger l’intégrité du code</span><span class="sxs-lookup"><span data-stu-id="eabc0-444">Require code integrity</span></span>|<span data-ttu-id="eabc0-445">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-445">Require</span></span>||


<span data-ttu-id="eabc0-446">**Propriétés des appareils**</span><span class="sxs-lookup"><span data-stu-id="eabc0-446">**Device properties**</span></span>

|<span data-ttu-id="eabc0-447">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-447">Type</span></span>|<span data-ttu-id="eabc0-448">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-448">Properties</span></span>|<span data-ttu-id="eabc0-449">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-449">Values</span></span>|<span data-ttu-id="eabc0-450">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-450">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-451">Version du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="eabc0-451">Operating system version</span></span>|<span data-ttu-id="eabc0-452">Tous</span><span class="sxs-lookup"><span data-stu-id="eabc0-452">All</span></span>|<span data-ttu-id="eabc0-453">Non configuré</span><span class="sxs-lookup"><span data-stu-id="eabc0-453">Not configured</span></span>||

<span data-ttu-id="eabc0-p126">Pour toutes les stratégies à prendre en considération ci-dessus déployés, ils doivent être ciblés à des groupes d’utilisateurs. Vous pouvez le faire en créant la stratégie (lors de l’enregistrement) ou version ultérieure en sélectionnant **Gérer un déploiement** dans la section **stratégie** (même niveau qu’Ajouter).</span><span class="sxs-lookup"><span data-stu-id="eabc0-p126">For all the above policies to be considered deployed, they must be targeted at user groups. You can do this by creating the policy (on Save) or later by selecting **Manage Deployment** in the **Policy** section (same level as Add).</span></span>

<span data-ttu-id="eabc0-456">**Sécurité système**</span><span class="sxs-lookup"><span data-stu-id="eabc0-456">**System security**</span></span>

|<span data-ttu-id="eabc0-457">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-457">Type</span></span>|<span data-ttu-id="eabc0-458">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-458">Properties</span></span>|<span data-ttu-id="eabc0-459">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-459">Values</span></span>|<span data-ttu-id="eabc0-460">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-460">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-461">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-461">Password</span></span>|<span data-ttu-id="eabc0-462">Exiger un mot de passe pour déverrouiller les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="eabc0-462">Require a password to unlock mobile devices</span></span>|<span data-ttu-id="eabc0-463">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-463">Require</span></span>||
||<span data-ttu-id="eabc0-464">Mots de passe simples</span><span class="sxs-lookup"><span data-stu-id="eabc0-464">Simple passwords</span></span>|<span data-ttu-id="eabc0-465">Bloc</span><span class="sxs-lookup"><span data-stu-id="eabc0-465">Block</span></span>||
||<span data-ttu-id="eabc0-466">Type de mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-466">Password type</span></span>|<span data-ttu-id="eabc0-467">Périphérique par défaut</span><span class="sxs-lookup"><span data-stu-id="eabc0-467">Device default</span></span>||
||<span data-ttu-id="eabc0-468">Longueur minimale du mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-468">Minimum password length</span></span>|<span data-ttu-id="eabc0-469">6</span><span class="sxs-lookup"><span data-stu-id="eabc0-469">6</span></span>||
||<span data-ttu-id="eabc0-470">Nombre maximal de minutes d’inactivité avant que le mot de passe</span><span class="sxs-lookup"><span data-stu-id="eabc0-470">Maximum minutes of inactivity before password is required</span></span>|<span data-ttu-id="eabc0-471">15 </span><span class="sxs-lookup"><span data-stu-id="eabc0-471">15</span></span>|<span data-ttu-id="eabc0-p127">Ce paramètre est pris en charge pour Android versions 4.0 et ultérieure ou KNOX 4.0 et versions ultérieures. Pour les appareils iOS, il est pris en charge pour iOS 8.0 et ci-dessus</span><span class="sxs-lookup"><span data-stu-id="eabc0-p127">This setting is supported for Android versions 4.0 and above or KNOX 4.0 and above. For iOS devices, it’s supported for iOS 8.0 and above</span></span>|
||<span data-ttu-id="eabc0-474">Expiration du mot de passe (jours)</span><span class="sxs-lookup"><span data-stu-id="eabc0-474">Password expiration (days)</span></span>|<span data-ttu-id="eabc0-475">41</span><span class="sxs-lookup"><span data-stu-id="eabc0-475">41</span></span>||
||<span data-ttu-id="eabc0-476">Nombre de mots de passe précédents pour empêcher la réutilisation</span><span class="sxs-lookup"><span data-stu-id="eabc0-476">Number of previous passwords to prevent reuse</span></span>|<span data-ttu-id="eabc0-477">5</span><span class="sxs-lookup"><span data-stu-id="eabc0-477">5</span></span>||
||<span data-ttu-id="eabc0-478">Demander le mot de passe lorsque le périphérique retourne à partir de l’état est inactif (Mobile et HOLOGRAPHIQUE)</span><span class="sxs-lookup"><span data-stu-id="eabc0-478">Require password when device returns from idle state (Mobile and Holographic)</span></span>|<span data-ttu-id="eabc0-479">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-479">Require</span></span>|<span data-ttu-id="eabc0-480">Disponibles pour Windows 10 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="eabc0-480">Available for Windows 10 and later</span></span>|
|<span data-ttu-id="eabc0-481">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="eabc0-481">Encryption</span></span>|<span data-ttu-id="eabc0-482">Chiffrement de stockage des données sur le périphérique</span><span class="sxs-lookup"><span data-stu-id="eabc0-482">Encryption of data storage on device</span></span>|<span data-ttu-id="eabc0-483">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-483">Require</span></span>||
|<span data-ttu-id="eabc0-484">Sécurité des périphériques</span><span class="sxs-lookup"><span data-stu-id="eabc0-484">Device Security</span></span>|<span data-ttu-id="eabc0-485">Pare-feu</span><span class="sxs-lookup"><span data-stu-id="eabc0-485">Firewall</span></span>|<span data-ttu-id="eabc0-486">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-486">Require</span></span>||
||<span data-ttu-id="eabc0-487">Antivirus</span><span class="sxs-lookup"><span data-stu-id="eabc0-487">Antivirus</span></span>|<span data-ttu-id="eabc0-488">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-488">Require</span></span>||
||<span data-ttu-id="eabc0-489">AntiSpyware</span><span class="sxs-lookup"><span data-stu-id="eabc0-489">Antispyware</span></span>|<span data-ttu-id="eabc0-490">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-490">Require</span></span>|<span data-ttu-id="eabc0-491">Ce paramètre nécessite une solution contre les logiciels espions inscrit avec le centre de sécurité Windows</span><span class="sxs-lookup"><span data-stu-id="eabc0-491">This setting requires an Anti-Spyware solution registered with Windows Security Center</span></span>|
|<span data-ttu-id="eabc0-492">Defender</span><span class="sxs-lookup"><span data-stu-id="eabc0-492">Defender</span></span>|<span data-ttu-id="eabc0-493">Windows Defender contre les logiciels malveillants</span><span class="sxs-lookup"><span data-stu-id="eabc0-493">Windows Defender Antimalware</span></span>|<span data-ttu-id="eabc0-494">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-494">Require</span></span>||
||<span data-ttu-id="eabc0-495">Version minimale de Windows Defender contre les logiciels malveillants</span><span class="sxs-lookup"><span data-stu-id="eabc0-495">Windows Defender Antimalware minimum version</span></span>||<span data-ttu-id="eabc0-p128">Uniquement pris en charge pour le bureau Windows 10. Microsoft ne recommande de versions aucuns plus de cinq derrière à partir de la version la plus récente</span><span class="sxs-lookup"><span data-stu-id="eabc0-p128">Only supported for Windows 10 desktop. Microsoft recommends versions no more than five behind from the most recent version</span></span>|
||<span data-ttu-id="eabc0-498">Signature contre les logiciels malveillants Windows Defender à jour</span><span class="sxs-lookup"><span data-stu-id="eabc0-498">Windows Defender Antimalware signature up to date</span></span>|<span data-ttu-id="eabc0-499">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-499">Require</span></span>||
||<span data-ttu-id="eabc0-500">Protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="eabc0-500">Real-time protection</span></span>|<span data-ttu-id="eabc0-501">Require (Rendre obligatoire)</span><span class="sxs-lookup"><span data-stu-id="eabc0-501">Require</span></span>|<span data-ttu-id="eabc0-502">Uniquement pris en charge pour le bureau Windows 10</span><span class="sxs-lookup"><span data-stu-id="eabc0-502">Only supported for Windows 10 desktop</span></span>|

<span data-ttu-id="eabc0-503">**Windows Defender ATP**</span><span class="sxs-lookup"><span data-stu-id="eabc0-503">**Windows Defender ATP**</span></span>

|<span data-ttu-id="eabc0-504">Type</span><span class="sxs-lookup"><span data-stu-id="eabc0-504">Type</span></span>|<span data-ttu-id="eabc0-505">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eabc0-505">Properties</span></span>|<span data-ttu-id="eabc0-506">Valeurs</span><span class="sxs-lookup"><span data-stu-id="eabc0-506">Values</span></span>|<span data-ttu-id="eabc0-507">Remarques</span><span class="sxs-lookup"><span data-stu-id="eabc0-507">Notes</span></span>|
|:---|:---------|:-----|:----|
|<span data-ttu-id="eabc0-508">Règles contre les menaces avancées Windows Defender</span><span class="sxs-lookup"><span data-stu-id="eabc0-508">Windows Defender Advanced Threat Protection rules</span></span>|<span data-ttu-id="eabc0-509">Exiger le périphérique soit au niveau ou sous le score de risque de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="eabc0-509">Require the device to be at or under the machine-risk score</span></span>|<span data-ttu-id="eabc0-510">Moyenne</span><span class="sxs-lookup"><span data-stu-id="eabc0-510">Medium</span></span>||

## <a name="require-compliant-pcs-but-not-compliant-phones-and-tablets"></a><span data-ttu-id="eabc0-511">Exiger des PC compatible (mais n’est pas compatibles téléphones et tablettes)</span><span class="sxs-lookup"><span data-stu-id="eabc0-511">Require compliant PCs (but not compliant phones and tablets)</span></span>
<span data-ttu-id="eabc0-p129">Avant d’ajouter une stratégie pour exiger que les ordinateurs conformes, veillez à inscrire des périphériques pour la gestion de Intune. À l’aide de l’authentification multifacteur est recommandé avant inscription périphériques Intune pour l’assurance que le périphérique est en possession de l’utilisateur concerné.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p129">Before adding a policy to require compliant PCs, be sure to enroll devices for management into Intune. Using multi-factor authentication is recommended before enrolling devices into Intune for assurance that the device is in the possession of the intended user.</span></span> 

<span data-ttu-id="eabc0-514">Pour exiger que les PC compatible :</span><span class="sxs-lookup"><span data-stu-id="eabc0-514">To require compliant PCs:</span></span>

1. <span data-ttu-id="eabc0-p130">Accédez au [portail Azure](https://portal.azure.com)et connectez-vous avec vos informations d’identification. Une fois que vous avez correctement connecté, vous voyez le tableau de bord Azure.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p130">Go to the [Azure portal](https://portal.azure.com), and sign in with your credentials. After you've successfully signed in, you see the Azure dashboard.</span></span>

2. <span data-ttu-id="eabc0-517">Dans le menu de gauche, choisissez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-517">Choose **Azure Active Directory** from the left menu.</span></span>

3. <span data-ttu-id="eabc0-518">Sous la section **Sécurité**, choisissez **Accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-518">Under the **Security** section, choose **Conditional access**.</span></span>

4. <span data-ttu-id="eabc0-519">Choisissez **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-519">Choose **New policy**.</span></span>

5. <span data-ttu-id="eabc0-520">Entrez un nom de stratégie et choisissez les **Utilisateurs et groupes** auxquels vous souhaitez appliquer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-520">Enter a policy name, then choose the **Users and groups** you want to apply the policy for.</span></span>

6. <span data-ttu-id="eabc0-521">Choisissez **Applications cloud**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-521">Choose **Cloud apps**.</span></span>

7. <span data-ttu-id="eabc0-p131">Choisissez **Sélectionner les applications**, sélectionnez les applications de votre choix dans la liste des **applications dans le nuage** . Par exemple, sélectionnez Office 365 Exchange Online. Choisissez **Sélectionnez** **terminé**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p131">Choose **Select apps**, select the desired apps from the **Cloud apps** list. For example, select Office 365 Exchange Online. Choose **Select** and **Done**.</span></span>

8. <span data-ttu-id="eabc0-p132">Pour exiger que les PC compatible, mais n’est pas compatibles téléphones et tablettes, choisissez **Conditions** et **plateformes d’appareils**. Choisissez **Sélectionner les plateformes d’appareils** et sélectionnez **Windows** et **Mac OS**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p132">To require compliant PCs, but not compliant phones and tablets, choose **Conditions** and **Device platforms**. Choose **Select device platforms** and select **Windows** and **macOS**.</span></span>

9. <span data-ttu-id="eabc0-527">Choisissez **Accorder** dans la section **Contrôles d’accès**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-527">Choose **Grant** from the **Access controls** section.</span></span>

10. <span data-ttu-id="eabc0-p133">Choisissez **accorder l’accès**, sélectionnez **Exiger le périphérique doit être marqué comme conforme**. Pour plusieurs contrôles, sélectionnez **exiger de tous les contrôles sélectionnés**, puis choisissez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p133">Choose **Grant access**, select **Require device to be marked as compliant**. For multiple controls, select **Require all the selected controls**, then choose **Select**.</span></span> 

11. <span data-ttu-id="eabc0-530">Sélectionnez **Create (Créer)**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-530">Choose **Create**.</span></span>

<span data-ttu-id="eabc0-p134">Si votre objectif est d’exiger compatible PC *et* appareils mobiles, n’activez pas les plateformes. Il met en œuvre la conformité pour tous les périphériques.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p134">If your objective is to require compliant PCs *and* mobile devices, do not select platforms. This enforces compliance for all devices.</span></span> 

## <a name="require-compliant-pcs-and-mobile-devices"></a><span data-ttu-id="eabc0-533">Exiger compatible PC *et* appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="eabc0-533">Require compliant PCs *and* mobile devices</span></span>

<span data-ttu-id="eabc0-534">Pour exiger la conformité pour tous les périphériques :</span><span class="sxs-lookup"><span data-stu-id="eabc0-534">To require compliance for all devices:</span></span>

1. <span data-ttu-id="eabc0-p135">Accédez au [portail Azure](https://portal.azure.com)et connectez-vous avec vos informations d’identification. Une fois que vous avez correctement connecté, vous voyez le tableau de bord Azure.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p135">Go to the [Azure portal](https://portal.azure.com), and sign in with your credentials. After you've successfully signed in, you see the Azure dashboard.</span></span>

2. <span data-ttu-id="eabc0-537">Dans le menu de gauche, choisissez **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-537">Choose **Azure Active Directory** from the left menu.</span></span>

3. <span data-ttu-id="eabc0-538">Sous la section **Sécurité**, choisissez **Accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-538">Under the **Security** section, choose **Conditional access**.</span></span>

4. <span data-ttu-id="eabc0-539">Choisissez **Nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-539">Choose **New policy**.</span></span>

5. <span data-ttu-id="eabc0-540">Entrez un nom de stratégie et choisissez les **Utilisateurs et groupes** auxquels vous souhaitez appliquer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="eabc0-540">Enter a policy name, then choose the **Users and groups** you want to apply the policy for.</span></span>

6. <span data-ttu-id="eabc0-541">Choisissez **Applications cloud**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-541">Choose **Cloud apps**.</span></span>

7. <span data-ttu-id="eabc0-p136">Choisissez **Sélectionner les applications**, sélectionnez les applications de votre choix dans la liste des **applications dans le nuage** . Par exemple, sélectionnez Office 365 Exchange Online. Choisissez **Sélectionnez** **terminé**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p136">Choose **Select apps**, select the desired apps from the **Cloud apps** list. For example, select Office 365 Exchange Online. Choose **Select** and **Done**.</span></span>

8. <span data-ttu-id="eabc0-545">Choisissez **Accorder** dans la section **Contrôles d’accès**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-545">Choose **Grant** from the **Access controls** section.</span></span>

9. <span data-ttu-id="eabc0-p137">Choisissez **accorder l’accès**, sélectionnez **Exiger le périphérique doit être marqué comme conforme**. Pour plusieurs contrôles, sélectionnez **exiger de tous les contrôles sélectionnés**, puis choisissez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p137">Choose **Grant access**, select **Require device to be marked as compliant**. For multiple controls, select **Require all the selected controls**, then choose **Select**.</span></span> 

10. <span data-ttu-id="eabc0-548">Sélectionnez **Create (Créer)**.</span><span class="sxs-lookup"><span data-stu-id="eabc0-548">Choose **Create**.</span></span>

<span data-ttu-id="eabc0-p138">Lorsque vous créez cette stratégie, n’activez pas les plateformes. Il met en œuvre des périphériques compatibles.</span><span class="sxs-lookup"><span data-stu-id="eabc0-p138">When creating this policy, do not select platforms. This enforces compliant devices.</span></span>




<!---
#### Data loss prevention
The goal for your device and app management policies is to protect data loss in the event of a lost or stolen device. You can do this by ensuring that access to data is protected by a PIN, that the data is encrypted on the device, and that the device is not compromised.

|Policy recommendation|Description|
|:--------------------|:----------|
|**Require user PC management**|Require users to join their Windows PCs to an Active Directory Domain or enroll their PCs into management with Microsoft Intune or System Center Configuration Manager.|
|**Apply security settings via group policy objects (GPO) or Configuration Manager policies for domain joined PCs**|Deploy policies that configure managed PCs to enable BitLocker, enable anti-virus, and enable firewall.|
|**Require user mobile device management**|Require that user devices used to access email are managed by Intune **or** company email is accessed only through mobile email apps protected by Intune App Protection policies such as Outlook for iOS or Android.|
|**Apply an Intune Device Compliance Policy on managed devices**|Apply an Intune Device Compliance Policy for managed corporate mobile devices and Intune-managed PCs that requires: a PIN with minimum length 6, device encryption, a healthy device (is not jailbroken, rooted; passes health attestation), and, if available, require devices that are **low** risk as determined by a third-party MTP like Lookout or SkyCure.|
|**Apply an Intune App Protection Policy for managed apps running on unmanaged devices**|Apply an Intune App Protection Policy for managed apps running on unmanaged, personal mobile devices to require: a PIN with minimum length 6, device encryption, and that the device is healthy (is not jailbroken, rooted; passes health attestation).|

### User impact

For most organizations, it is important to be able to set user expectations around when and for which conditions they will be expected to sign into Office 365 to access their email.  

Users typically benefit from single sign-on (SSO) except during the following situations:
* When requesting authentication tokens for Exchange Online:
  * Users may be asked to MFA whenever a **medium or above** sign-in risk is detected and users has not yet performed MFA in their current sessions.  
  * Users will be required to either use email apps that support the Intune App Protection SDK or access emails from Intune compliant or AD domain-joined devices.
* When users at risk sign-in, and successfully complete MFA, they will be asked to change their password.

## Sensitive
This section describes the recommendations for the sensitive tier of data, identity, and device protection. These recommendations are for customers who have a subset of data that must be protected at higher levels or require all data to be protected at these higher levels.

You can apply increased protection to all or specific data sets in your Office 365 environment. For example, you can apply policies to ensure sensitive data is only shared between protected apps to prevent data loss. We recommend protecting identities and devices that access sensitive data with comparable levels of security.

### Conditional access policy settings
#### Identity protection

You can give users single sign-on (SSO) experience as described in earlier sections. You only need to intervene when necessary based on [risk events](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-risk-events).   

* Require MFA on **low or above** risk sessions
* Require secure password change for high risk users

>[!IMPORTANT]
>[Password synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization) and [self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords) are required for this policy recommendation.
>

#### Data loss prevention

The goal for these device and app management policies is to protect data loss in the event of a lost or stolen device. You can do this by ensuring that access to data is protected by a PIN, that the data is encrypted on the device, and that the device is not compromised.

|Policy recommendation|Description|
|:--------------------|:----------|
|**Require user PC management**|Require users to join their PCs to an Active Directory Domain or enroll their PCs into management with Intune or Configuration Manager and ensure those devices are compliant with policies before allowing email access.|
|**Apply security settings via group policy objects (GPO) or Configuration Manager policies for domain joined PCs**|Deploy policies that configure managed PCs to enable BitLocker, enable anti-virus, and enable firewall.|
|**Require user mobile device management**|Require that user devices used to access email are managed by Intune **or** company email is accessed only through mobile email apps protected by Intune App Protection policies such as Outlook for iOS or Android.|
|**Apply an Intune Device Compliance Policy on managed devices**|Apply an Intune Device Compliance Policy for managed corporate mobile devices and Intune-managed PCs that requires: a PIN with minimum length 6, device encryption, a healthy device (is not jailbroken, rooted; passes health attestation), and if available, require devices that are **low** risk as determined by a third-party MTP like Lookout or SkyCure.|
|**Apply an Intune App Protection Policy for managed apps running on unmanaged devices**|Apply an Intune App Protection Policy for managed apps running on unmanaged, personal mobile devices to require: a PIN with minimum length 6, device encryption, and that the device is healthy (is not jailbroken, rooted; passes health attestation).|

### User impact
For most organizations, it is important to be able to set expectations for users specific to when and under what conditions they will be expected to sign into Office 365 email.

Users typically benefit from single sign-on (SSO) except under the following situations:
* When requesting authentication tokens for Exchange Online:
  * Users will be asked to MFA whenever a **low or above** sign-in risk is detected and users has not yet performed MFA in their current sessions.  
  * Users will be required to either use email apps that support the Intune App Protection SDK or access emails from Intune compliant or AD domain-joined devices.
* When users at risk sign-in, and successfully complete MFA, they will be asked to change their password.

## Highly regulated
This section describes the recommendations for the highly regulated tier of data, identity, and device protection. These recommendations are for customers who may have a very small amount of data that is highly classified, trade secret, or regulated data. Microsoft provides capabilities to help organizations meet these requirements, including added protection for identities and devices.

### Conditional access policy settings
#### Identity protection

For the highly regulated tier Microsoft recommends enforcing MFA for all new sessions.
* Require MFA for all new sessions
* Require secure password change for **high** risk users

>[!IMPORTANT]
>[Password synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization) and [self-service password reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords) are required for this policy recommendation.
>

#### Data Loss Prevention
The goal for these device and app management policies is to prevent data loss in the event of a lost or stolen device. This is done by ensuring that access to data is protected by a PIN, that the data is encrypted on the device, and that the device is not compromised.

For the highly regulated tier, we recommend requiring apps that support Intune App Protection policy running only on Intune compliant or domain-joined devices.

|Policy recommendation|Description|
|:--------------------|:----------|
|**Require user PC management**|Require users to join their Windows PCs to an Active Directory Domain, **or** enroll their PCs into management with Intune or Configuration Manager and ensure those devices are compliant with policies before allowing email access.|
|**Apply security settings via group policy objects (GPO) or Configuration Manager policies for domain joined PCs**|Deploy policies that configure managed PCs to enable BitLocker, enable anti-virus, and enable firewall.|
|**Require user mobile device management**|Require that devices used to access Office 365 email and files are managed by Intune or company email is accessed only through mobile email apps protected by Intune App Protection policies such as Outlook for iOS or Android.|
|**Apply an Intune Device Compliance Policy on managed devices**|Apply an Intune Device Compliance Policy for managed corporate mobile devices and Intune-managed PCs that requires: a PIN with minimum length 6, device encryption, a healthy device (is not jailbroken, rooted; passes health attestation), and, if available, require devices that are Low risk as determined by a third-party MTP like Lookout or SkyCure.|

### User impact
For most organizations, it is important to be able to set expectations for users specific to when and under what conditions they will be expected to sign into Office 365 files.

* Users configured as highly regulated will be required to re-authenticate with MFA after their session expires.
* When users at risk sign-in they will be asked to change their password after completing MFA.
* When requesting authentication tokens for Exchange Online:
  * Users will be asked to perform MFA whenever they begin a new session.  
  * Users will be required to use email apps that support the Intune App Protection SDK
  * Users will be required to access emails from Intune compliant or AD domain-joined devices.
--->
## <a name="next-steps"></a><span data-ttu-id="eabc0-551">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eabc0-551">Next steps</span></span>

[<span data-ttu-id="eabc0-552">Découvrir les recommandations de stratégies pour sécuriser les e-mails</span><span class="sxs-lookup"><span data-stu-id="eabc0-552">Learn about policy recommendations for securing email</span></span>](secure-email-recommended-policies.md)
