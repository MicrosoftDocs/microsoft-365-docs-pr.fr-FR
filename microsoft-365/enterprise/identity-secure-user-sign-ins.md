---
title: 'Étape 3 : Sécuriser et gérer les connexions de vos utilisateurs'
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
description: Vous pouvez sécuriser plus efficacement les connexions des utilisateurs aux appareils Windows et à Microsoft 365.
ms.openlocfilehash: 6f45d61694cabd10587ff13bd787fa42bdaeac01
ms.sourcegitcommit: 8bcd76e5c8749a5670fbc3356957a089454c03d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2019
ms.locfileid: "37370191"
---
# <a name="step-3-secure-and-manage-your-user-sign-ins"></a><span data-ttu-id="4b2b9-103">Étape 3 : Sécuriser et gérer les connexions de vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4b2b9-103">Step 3: Secure and manage your user sign-ins</span></span>

![Phase 2 - Identité](./media/deploy-foundation-infrastructure/identity_icon-small.png)


<a name="identity-windows-hello"></a>
## <a name="use-windows-hello-for-business"></a><span data-ttu-id="4b2b9-105">Utiliser Windows Hello Entreprise</span><span class="sxs-lookup"><span data-stu-id="4b2b9-105">Windows Hello for Business</span></span>

<span data-ttu-id="4b2b9-106">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="4b2b9-106">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="4b2b9-107">Windows Hello Entreprise dans Windows 10 Entreprise remplace les mots de passe par une authentification à deux facteurs forte lors de la connexion à un appareil Windows.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-107">Windows Hello for Business in Windows 10 Enterprise replaces passwords with strong two-factor authentication when signing on a Windows device.</span></span> <span data-ttu-id="4b2b9-108">Les deux facteurs sont un nouveau type d’informations d’identification d’utilisateur qui est lié à un appareil et à un code biométrique ou PIN.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-108">The two factors are a new type of user credential that is tied to a device and a biometric or PIN.</span></span>

<span data-ttu-id="4b2b9-109">Pour plus d’informations, consultez [Vue d’ensemble de Windows Hello Entreprise](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-overview).</span><span class="sxs-lookup"><span data-stu-id="4b2b9-109">For more information, see [Windows Hello for Business Overview](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-overview).</span></span>


<a name="identity-mfa"></a>
## <a name="set-up-azure-multi-factor-authentication"></a><span data-ttu-id="4b2b9-110">Configurer Authentication multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="4b2b9-110">Set up Azure Multi-Factor Authentication</span></span>

<span data-ttu-id="4b2b9-111">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="4b2b9-111">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="4b2b9-112">Dans cette étape, vous allez configurer Authentication multifacteur Azure (MFA) pour ajouter une seconde couche de sécurité aux connexions et transactions des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-112">In this step, you'll set up Azure Multi-Factor Authentication (MFA) to add a second layer of security to user sign-ins and transactions.</span></span> <span data-ttu-id="4b2b9-113">Authentication multifacteur Azure requiert une méthode de vérification supplémentaire une fois que les utilisateurs ont correctement entré leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-113">MFA requires an additional verification method after users have correctly entered their password.</span></span> <span data-ttu-id="4b2b9-114">Sans Authentication multifacteur Azure, le mot de passe reste la seule méthode de vérification.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-114">Without MFA, the password is the only verification method.</span></span> <span data-ttu-id="4b2b9-115">Le problème avec les mots de passe est que bon nombre d'entre eux se devinent facilement par un pirate ou sont partagés inconsciemment avec des parties non approuvées.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-115">The problem with passwords is that many of them are easily guessed by an attacker or unknowingly shared with untrusted parties.</span></span>

<span data-ttu-id="4b2b9-116">Avec l’authentification multifacteur, la deuxième couche de sécurité peut être :</span><span class="sxs-lookup"><span data-stu-id="4b2b9-116">With MFA, the second layer of security can be:</span></span>

- <span data-ttu-id="4b2b9-117">un appareil personnel et approuvé qui n’est pas facilement usurpé ou dupliqué (un smartphone, par exemple) ;</span><span class="sxs-lookup"><span data-stu-id="4b2b9-117">A personal and trusted device that isn’t easily spoofed or duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="4b2b9-118">un attribut biométrique (une empreinte numérique, par exemple).</span><span class="sxs-lookup"><span data-stu-id="4b2b9-118">A biometric attribute, such as a fingerprint.</span></span>

<span data-ttu-id="4b2b9-119">Vous allez activer l’authentification multifacteur et configurer la méthode d’authentification secondaire avec les [stratégies d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access), qui vous permettent d’utiliser les groupes Azure Active Directory (Azure AD) pour déployer l’authentification multifacteur vers des ensembles d’utilisateurs spécifiés, tels que des utilisateurs pilotes, régions géographiques ou services.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-119">You'll enable MFA and configure the secondary authentication method with [Conditional Access policies](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access), which allow you to use Azure Active Directory (Azure AD) groups to roll out MFA to specified sets of users, such as pilot users, geographical regions, or departments.</span></span> <span data-ttu-id="4b2b9-120">Informez bien vos utilisateurs que l’authentification multifacteur est en cours d’activation pour qu’ils comprennent les exigences telles que l’utilisation obligatoire d’un smartphone pour la connexion et puissent se connecter correctement.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-120">You'll enable MFA and configure the secondary authentication method on a per-user account basis. Make sure to let users know that MFA is being enabled so they understand the requirements, such as mandatory use of a smart phone to sign in, and can sign in successfully.</span></span> 

<span data-ttu-id="4b2b9-121">Pour plus d’informations, reportez-vous à [Planifier le déploiement d’une authentification multifacteur Azure basée sur Cloud](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span><span class="sxs-lookup"><span data-stu-id="4b2b9-121">For more information, see [Planning a cloud-based Azure Multi-Factor Authentication deployment](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="4b2b9-123">Guide du laboratoire de test : authentification multifacteur Azure</span><span class="sxs-lookup"><span data-stu-id="4b2b9-123">Test Lab Guide: Azure Multi-Factor Authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="4b2b9-124">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-mfa) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-124">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-mfa) for this section.</span></span>

<a name="identity-ident-prot"></a>
## <a name="protect-against-credential-compromise"></a><span data-ttu-id="4b2b9-125">Protégez-vous contre la compromission des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="4b2b9-125">Protect against credential compromise</span></span>

<span data-ttu-id="4b2b9-126">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="4b2b9-126">*This is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="4b2b9-127">Cette section explique comment configurer des stratégies de protection contre la compromission d’informations d’identification consistant pour un attaquant à déterminer le nom de compte et le mot de passe d’un utilisateur afin d’accéder aux services et données cloud d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-127">In this section, you'll learn how to configure policies that protect against credential compromise, where an attacker determines a user’s account name and password to gain access to an organization’s cloud services and data.</span></span> <span data-ttu-id="4b2b9-128">Azure Active Directory Identity Protection offre plusieurs méthodes pour empêcher un pirate de compromettre les informations d’identification d’un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-128">Azure AD Identity Protection provides a number of ways to help prevent an attacker from compromising a user account's credentials.</span></span>

<span data-ttu-id="4b2b9-129">Azure AD Identity Protection vous permet de :</span><span class="sxs-lookup"><span data-stu-id="4b2b9-129">With Azure AD Identity Protection, you can:</span></span>

|||
|:---------|:---------|
|<span data-ttu-id="4b2b9-130">déterminer et résoudre les vulnérabilités potentielles dans les identités de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="4b2b9-130">Determine and address potential vulnerabilities in your organization’s identities</span></span>|<span data-ttu-id="4b2b9-131">Azure AD utilise le Machine Learning pour détecter les anomalies et les activités suspectes, telles que les connexions et les activités post-connexion.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-131">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span> <span data-ttu-id="4b2b9-132">Grâce à ces données, Azure AD Identity Protection génère des rapports et des alertes qui vous permettent d’évaluer les problèmes et de prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-132">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span>|
|<span data-ttu-id="4b2b9-133">Détecter des actions douteuses qui sont liées aux identités de votre organisation et y répondre automatiquement</span><span class="sxs-lookup"><span data-stu-id="4b2b9-133">Detect suspicious actions that are related to your organization’s identities and respond to them automatically</span></span>|<span data-ttu-id="4b2b9-134">Vous pouvez configurer des stratégies qui répondent automatiquement aux problèmes détectés lorsqu’un niveau de risque spécifié est atteint.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-134">You can configure risk-based policies that automatically respond to detected issues when a specified risk level has been reached.</span></span> <span data-ttu-id="4b2b9-135">Outre les autres contrôles d’accès conditionnel fournis par Azure AD et Microsoft Intune, ces stratégies peuvent automatiquement bloquer l’accès ou prendre des mesures correctives, qui incluent des réinitialisations de mot de passe et impliquent une authentification multifacteur Azure pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-135">These policies, in addition to other Conditional Access controls provided by Azure AD and Microsoft Intune, can either automatically block access or take corrective actions, including password resets and requiring Azure Multi-Factor Authentication for subsequent sign-ins.</span></span>|
|<span data-ttu-id="4b2b9-136">Examiner les incidents suspects et les résoudre avec des actions d’administration</span><span class="sxs-lookup"><span data-stu-id="4b2b9-136">Investigate suspicious incidents and resolve them with administrative actions</span></span>|<span data-ttu-id="4b2b9-p107">Vous pouvez examiner des événements à risque en utilisant les informations sur l’incident de sécurité. Des flux de travail de base sont disponibles pour effectuer le suivi des enquêtes et lancer des actions de correction, telles que des réinitialisations du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-p107">You can investigate risk events using information about the security incident. Basic workflows are available to track investigations and initiate remediation actions, such as password resets.</span></span>|

<span data-ttu-id="4b2b9-139">[Plus d’informations sur Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span><span class="sxs-lookup"><span data-stu-id="4b2b9-139">See [more information about Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span></span>

<span data-ttu-id="4b2b9-140">Reportez-vous à la rubrique des [étapes pour activer Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span><span class="sxs-lookup"><span data-stu-id="4b2b9-140">See the [steps to enable Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span></span>

<span data-ttu-id="4b2b9-141">Les résultats de cette étape sont que vous avez activé Azure AD Identity Protection et que vous l’utilisez pour :</span><span class="sxs-lookup"><span data-stu-id="4b2b9-141">The results of this step are that you've enabled Azure AD Identity protection and you are using it to:</span></span>

- <span data-ttu-id="4b2b9-142">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="4b2b9-142">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="4b2b9-143">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="4b2b9-143">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="4b2b9-144">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-144">Investigate and address ongoing suspicious identity incidents.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="4b2b9-146">Guide de laboratoire de test : Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="4b2b9-146">Test Lab Guide: Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="4b2b9-147">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-ident-prot) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="4b2b9-147">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-ident-prot) for this section.</span></span>

|||
|:-------|:-----|
|![Étape 4](./media/stepnumbers/Step4.png)| [<span data-ttu-id="4b2b9-149">Ajouter vos comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4b2b9-149">Step 4: Add your user accounts</span></span>](identity-add-user-accounts.md) |
