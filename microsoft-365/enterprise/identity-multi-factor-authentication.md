---
title: 'Étape 4 : configurer l’authentification d’utilisateur sécurisée'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/06/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez l’authentification multifacteur pour les comptes d’utilisateur.
ms.openlocfilehash: 2a4a0926a08ae8279523219a2d7a2386ea0c6742
ms.sourcegitcommit: 91ff1d4339f0f043c2b43997d87d84677c79e279
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2019
ms.locfileid: "36981845"
---
# <a name="step-4-configure-secure-user-authentication"></a><span data-ttu-id="e8f78-103">Étape 4 : configurer l’authentification d’utilisateur sécurisée</span><span class="sxs-lookup"><span data-stu-id="e8f78-103">Step 4: Configure secure user authentication</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-mfa"></a>
## <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="e8f78-104">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="e8f78-104">Set up multi-factor authentication</span></span>

<span data-ttu-id="e8f78-105">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e8f78-105">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="e8f78-p101">Lors de cette étape, vous allez configurer l’authentification multifacteur (MFA) pour ajouter une deuxième couche de sécurité aux connexions et transactions de l’utilisateur. L’authentification multifacteur nécessite une méthode de vérification supplémentaire une fois que les utilisateurs ont entré correctement leur mot de passe. Sans l’authentification multifacteur, le mot de passe est la seule méthode de vérification. Le problème avec les mots de passe est qu’un grand nombre d’entre eux peuvent facilement être devinés par une personne malveillante ou partagés involontairement avec des parties non approuvées.</span><span class="sxs-lookup"><span data-stu-id="e8f78-p101">In this step, you'll set up multi-factor authentication (MFA) to add a second layer of security to user sign-ins and transactions. MFA requires an additional verification method after users have correctly entered their password. Without MFA, the password is the only verification method. The problem with passwords is that many of them are easily guessed by an attacker or unknowingly shared with untrusted parties.</span></span>

<span data-ttu-id="e8f78-110">Avec l’authentification multifacteur, la deuxième couche de sécurité peut être :</span><span class="sxs-lookup"><span data-stu-id="e8f78-110">With MFA, the second layer of security can be:</span></span>

- <span data-ttu-id="e8f78-111">un appareil personnel et approuvé qui n’est pas facilement usurpé ou dupliqué (un smartphone, par exemple) ;</span><span class="sxs-lookup"><span data-stu-id="e8f78-111">A personal and trusted device that isn’t easily spoofed or duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="e8f78-112">un attribut biométrique (une empreinte numérique, par exemple).</span><span class="sxs-lookup"><span data-stu-id="e8f78-112">A biometric attribute, such as a fingerprint.</span></span>

<span data-ttu-id="e8f78-113">Vous allez activer l’authentification multifacteur et configurer la méthode d’authentification secondaire avec les [stratégies d’accès conditionnel](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access), qui vous permettent d’utiliser les groupes Azure Active Directory (Azure AD) pour déployer l’authentification multifacteur vers des ensembles d’utilisateurs spécifiés, tels que des utilisateurs pilotes, régions géographiques ou services.</span><span class="sxs-lookup"><span data-stu-id="e8f78-113">You'll enable MFA and configure the secondary authentication method with [conditional access policies](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted#enable-multi-factor-authentication-with-conditional-access), which allow you to use Azure Active Directory (Azure AD) groups to roll out MFA to specified sets of users, such as pilot users, geographical regions, or departments.</span></span> <span data-ttu-id="e8f78-114">Informez bien vos utilisateurs que l’authentification multifacteur est en cours d’activation pour qu’ils comprennent les exigences telles que l’utilisation obligatoire d’un smartphone pour la connexion et puissent se connecter correctement.</span><span class="sxs-lookup"><span data-stu-id="e8f78-114">You'll enable MFA and configure the secondary authentication method on a per-user account basis. Make sure to let users know that MFA is being enabled so they understand the requirements, such as mandatory use of a smart phone to sign in, and can sign in successfully.</span></span> 

<span data-ttu-id="e8f78-115">Pour plus d’informations, voir [Planifier l’authentification multifacteur](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span><span class="sxs-lookup"><span data-stu-id="e8f78-115">For more information, see [Plan for multi-factor authentication](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span></span>

>[!Note]
><span data-ttu-id="e8f78-p103">Dans certaines applications, comme Microsoft Office 2010 ou antérieures et Apple Mail, vous ne pouvez pas utiliser l’authentification multifacteur. Pour utiliser ces applications, vous devez utiliser des « mots de passe d’application » à la place de votre mot de passe habituel. Le mot de passe d’application permet à l’application de contourner l’authentification multifacteur et de continuer à fonctionner. Pour en savoir plus sur les mots de passe d’application, reportez-vous à [Créer un mot de passe d’application pour Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span><span class="sxs-lookup"><span data-stu-id="e8f78-p103">In some applications, such as Microsoft Office 2010 or older and Apple Mail, you can’t use MFA. To use these apps, you’ll need to use “app passwords” in place of your traditional password. The app password allows the app to bypass MFA and continue working. To learn more about app passwords, see [Create an app password for Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span></span>
>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="e8f78-121">Guide du laboratoire de test : authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="e8f78-121">Test Lab Guide: Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="e8f78-122">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-mfa) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="e8f78-122">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-mfa) for this section.</span></span>

<a name="identity-password-prot"></a>
## <a name="prevent-bad-passwords"></a><span data-ttu-id="e8f78-123">Éviter les mots de passe incorrects</span><span class="sxs-lookup"><span data-stu-id="e8f78-123">Prevent bad passwords</span></span>

<span data-ttu-id="e8f78-124">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e8f78-124">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="e8f78-125">Pour empêcher les utilisateurs de créer un mot de passe facile à déterminer, optez pour la protection par mot de passe Azure AD qui utilise une liste globale de mots de passe interdits et une liste personnalisée facultative de mots de passe que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="e8f78-125">To prevent users from creating easily determined password, use Azure AD password protection, which uses both a global banned password list and an optional custom banned password list that you specify.</span></span> <span data-ttu-id="e8f78-126">Par exemple, vous pouvez spécifier des termes propres à votre organisation, tels que «</span><span class="sxs-lookup"><span data-stu-id="e8f78-126">For example, you can specify terms that are specific to your organization, such as"</span></span>

- <span data-ttu-id="e8f78-127">Noms de marques</span><span class="sxs-lookup"><span data-stu-id="e8f78-127">Brand names</span></span>
- <span data-ttu-id="e8f78-128">Noms de produits</span><span class="sxs-lookup"><span data-stu-id="e8f78-128">Product names</span></span>
- <span data-ttu-id="e8f78-129">Emplacements (par exemple, le siège social de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="e8f78-129">Locations (for example, such as company headquarters)</span></span>
- <span data-ttu-id="e8f78-130">Termes internes spécifiques à l’entreprise</span><span class="sxs-lookup"><span data-stu-id="e8f78-130">Company-specific internal terms</span></span>
- <span data-ttu-id="e8f78-131">Abréviations dotées d’une signification spécifique à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e8f78-131">Abbreviations that have specific company meaning.</span></span>

<span data-ttu-id="e8f78-132">Vous pouvez interdire les mots de passe incorrects [dans le cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) et localement pour [Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises).</span><span class="sxs-lookup"><span data-stu-id="e8f78-132">You can ban bad passwords [in the cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) and for your [on-premises Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises).</span></span>

<span data-ttu-id="e8f78-133">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-password-prot) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="e8f78-133">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-password-prot) for this section.</span></span>

<a name="identity-ident-prot"></a>
## <a name="protect-against-credential-compromise"></a><span data-ttu-id="e8f78-134">Protégez-vous contre la compromission des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="e8f78-134">Protect against credential compromise</span></span>

<span data-ttu-id="e8f78-135">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e8f78-135">*This is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="e8f78-136">Cette section explique comment configurer des stratégies de protection contre la compromission d’informations d’identification consistant pour un attaquant à déterminer le nom de compte et le mot de passe d’un utilisateur afin d’accéder aux services et données cloud d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="e8f78-136">In this section, you'll learn how to configure policies that protect against credential compromise, where an attacker determines a user’s account name and password to gain access to an organization’s cloud services and data.</span></span> <span data-ttu-id="e8f78-137">Azure AD Identity Protection fournit un certain nombre de moyens pour empêcher un attaquant de se déplacer latéralement dans vos comptes et groupes, puis vers vos données les plus précieuses.</span><span class="sxs-lookup"><span data-stu-id="e8f78-137">Azure AD Identity Protection provides a number of ways to help prevent an attacker from moving laterally through your accounts and groups, and subsequently, to your most valuable data.</span></span>

<span data-ttu-id="e8f78-138">Azure AD Identity Protection vous permet de :</span><span class="sxs-lookup"><span data-stu-id="e8f78-138">With Azure AD Identity Protection, you can:</span></span>

|||
|:---------|:---------|
|<span data-ttu-id="e8f78-139">déterminer et résoudre les vulnérabilités potentielles dans les identités de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="e8f78-139">Determine and address potential vulnerabilities in your organization’s identities</span></span>|<span data-ttu-id="e8f78-140">Azure AD utilise le Machine Learning pour détecter les anomalies et les activités suspectes, telles que les connexions et les activités post-connexion.</span><span class="sxs-lookup"><span data-stu-id="e8f78-140">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span> <span data-ttu-id="e8f78-141">Grâce à ces données, Azure AD Identity Protection génère des rapports et des alertes qui vous permettent d’évaluer les problèmes et de prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="e8f78-141">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span>|
|<span data-ttu-id="e8f78-142">Détecter des actions douteuses qui sont liées aux identités de votre organisation et y répondre automatiquement</span><span class="sxs-lookup"><span data-stu-id="e8f78-142">Detect suspicious actions that are related to your organization’s identities and respond to them automatically</span></span>|<span data-ttu-id="e8f78-143">Vous pouvez configurer des stratégies qui répondent automatiquement aux problèmes détectés lorsqu’un niveau de risque spécifié est atteint.</span><span class="sxs-lookup"><span data-stu-id="e8f78-143">You can configure risk-based policies that automatically respond to detected issues when a specified risk level has been reached.</span></span> <span data-ttu-id="e8f78-144">Outre les autres contrôles d’accès conditionnel fournis par Azure AD et Microsoft Intune, ces stratégies peuvent automatiquement bloquer l’accès ou prendre des mesures correctives, qui incluent des réinitialisations de mot de passe et impliquent une authentification multifacteur pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8f78-144">You can configure risk-based policies that automatically respond to detected issues when a specified risk level has been reached. These policies, in addition to other conditional access controls provided by Azure Active Directory and Enterprise Mobility + Security (EMS), can either automatically block access or take corrective actions, including password resets and requiring multi-factor authentication for subsequent sign-ins.</span></span>|
|<span data-ttu-id="e8f78-145">Examiner les incidents suspects et les résoudre avec des actions d’administration</span><span class="sxs-lookup"><span data-stu-id="e8f78-145">Investigate suspicious incidents and resolve them with administrative actions</span></span>|<span data-ttu-id="e8f78-p108">Vous pouvez examiner des événements à risque en utilisant les informations sur l’incident de sécurité. Des flux de travail de base sont disponibles pour effectuer le suivi des enquêtes et lancer des actions de correction, telles que des réinitialisations du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="e8f78-p108">You can investigate risk events using information about the security incident. Basic workflows are available to track investigations and initiate remediation actions, such as password resets.</span></span>|

<span data-ttu-id="e8f78-148">[Plus d’informations sur Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span><span class="sxs-lookup"><span data-stu-id="e8f78-148">See [more information about Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span></span>

<span data-ttu-id="e8f78-149">Reportez-vous à la rubrique des [étapes pour activer Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span><span class="sxs-lookup"><span data-stu-id="e8f78-149">See the [steps to enable Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span></span>

<span data-ttu-id="e8f78-150">Les résultats de cette étape sont que vous avez activé Azure AD Identity Protection et que vous l’utilisez pour :</span><span class="sxs-lookup"><span data-stu-id="e8f78-150">The results of this step are that you've enabled Azure AD Identity protection and you are using it to:</span></span>

- <span data-ttu-id="e8f78-151">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="e8f78-151">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="e8f78-152">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="e8f78-152">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="e8f78-153">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="e8f78-153">Investigate and address ongoing suspicious identity incidents.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="e8f78-155">Guide de laboratoire de test : Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="e8f78-155">Test Lab Guide: Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="e8f78-156">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-ident-prot) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="e8f78-156">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-ident-prot) for this section.</span></span>

## <a name="monitor-tenant-and-sign-in-activity"></a><span data-ttu-id="e8f78-157">Surveillez l’activité de connexion et du client</span><span class="sxs-lookup"><span data-stu-id="e8f78-157">Monitor tenant and sign-in activity</span></span>

<span data-ttu-id="e8f78-158">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="e8f78-158">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="e8f78-p109">Dans cette étape, vous allez passer en revue les journaux d’audit et l’activité de connexion à l’aide des rapports Azure AD. Deux types de rapports sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="e8f78-p109">In this step, you'll review audit logs and sign-in activity using Azure AD reporting. Two types of reports are available.</span></span>

<span data-ttu-id="e8f78-p110">Le **rapport d’activité des journaux d’audit** enregistre l’historique de toutes les tâches effectuées dans votre client Azure AD. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="e8f78-p110">The **Audit logs activity report** records the history of every task performed in your Azure AD tenant. This report answers questions like:</span></span>

- <span data-ttu-id="e8f78-163">Qui a ajouté une personne à un groupe d’administration ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-163">Who added someone to an admin group?</span></span>
- <span data-ttu-id="e8f78-164">Quels sont les utilisateurs qui se connectent à une application spécifique ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-164">Which users are signing into a specific app?</span></span>
- <span data-ttu-id="e8f78-165">Combien de réinitialisations de mot de passe sont prévues ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-165">How many password resets are happening?</span></span>

<span data-ttu-id="e8f78-p111">Le **rapport d’activité des connexions** enregistre l’auteur des tâches indiquées par le rapport des journaux d’audit. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="e8f78-p111">The **Sign-ins activity report** records who performed the tasks reported by the audit logs report. This report answers questions like:</span></span>

- <span data-ttu-id="e8f78-168">Pour un utilisateur spécifique à l’étude, quel est son modèle de connexion ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-168">For a specific user under investigation, what is their sign-in pattern?</span></span>
- <span data-ttu-id="e8f78-169">Quel est mon volume de connexions par jour, semaine ou mois ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-169">What is my volume of sign-ins over a day, week, or month?</span></span>
- <span data-ttu-id="e8f78-170">Combien de ces tentatives de connexion n’ont pas abouti, et pour quels comptes ?</span><span class="sxs-lookup"><span data-stu-id="e8f78-170">How many of these sign-in attempts were not successful, and for which accounts?</span></span>

<span data-ttu-id="e8f78-171">Pour plus d’informations sur les rapports et la façon d’y accéder, reportez-vous à la rubrique [Création de rapports Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="e8f78-171">For more information about the reports and how to access them, see [Azure Active Directory reporting](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span></span>

<span data-ttu-id="e8f78-172">Après cette étape, vous connaîtrez ces rapports et saurez comment les utiliser pour obtenir des informations sur les activités et événements Azure AD à des fins de planification et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e8f78-172">As a result of this step, you'll gain awareness of these reports and an understanding of how you can use them to gain insights on Azure AD events and activities for planning and security purposes.</span></span>

## <a name="next-step"></a><span data-ttu-id="e8f78-173">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e8f78-173">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step5.png)| [<span data-ttu-id="e8f78-174">Simplifier l’accès pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e8f78-174">Simplify access for users</span></span>](identity-password-reset.md) |

