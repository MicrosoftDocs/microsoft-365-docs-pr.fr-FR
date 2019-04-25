---
title: 'Étape 4 : configurer l’authentification d’utilisateur sécurisée'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/17/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez l’authentification multifacteur pour les comptes d’utilisateur.
ms.openlocfilehash: 44d878a347e7b01263f9ba3a82f6443f5710dc43
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285464"
---
# <a name="step-4-configure-secure-user-authentication"></a><span data-ttu-id="65a30-103">Étape 4 : configurer l’authentification d’utilisateur sécurisée</span><span class="sxs-lookup"><span data-stu-id="65a30-103">Step 4: Configure secure user authentication</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-mfa"></a>
## <a name="set-up-multi-factor-authentication"></a><span data-ttu-id="65a30-104">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="65a30-104">Set up multi-factor authentication.</span></span>

<span data-ttu-id="65a30-105">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="65a30-105">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="65a30-p101">Lors de cette étape, vous allez configurer l’authentification multifacteur (MFA) pour ajouter une deuxième couche de sécurité aux connexions et transactions de l’utilisateur. L’authentification multifacteur nécessite une méthode de vérification supplémentaire une fois que les utilisateurs ont entré correctement leur mot de passe. Sans l’authentification multifacteur, le mot de passe est la seule méthode de vérification. Le problème avec les mots de passe est qu’un grand nombre d’entre eux peuvent facilement être devinés par une personne malveillante ou partagés involontairement avec des parties non approuvées.</span><span class="sxs-lookup"><span data-stu-id="65a30-p101">In this step, you'll set up multi-factor authentication (MFA) to add a second layer of security to user sign-ins and transactions. MFA requires an additional verification method after users have correctly entered their password. Without MFA, the password is the only verification method. The problem with passwords is that many of them are easily guessed by an attacker or unknowingly shared with untrusted parties.</span></span>

<span data-ttu-id="65a30-110">Avec l’authentification multifacteur, la deuxième couche de sécurité peut être :</span><span class="sxs-lookup"><span data-stu-id="65a30-110">With MFA, the second layer of security can be:</span></span>

- <span data-ttu-id="65a30-111">un appareil personnel et approuvé qui n’est pas facilement usurpé ou dupliqué (un smartphone, par exemple) ;</span><span class="sxs-lookup"><span data-stu-id="65a30-111">A personal and trusted device that isn’t easily spoofed or duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="65a30-112">un attribut biométrique (une empreinte numérique, par exemple).</span><span class="sxs-lookup"><span data-stu-id="65a30-112">A biometric attribute, such as a fingerprint.</span></span>

<span data-ttu-id="65a30-p102">Vous allez activer l’authentification multifacteur et configurer la méthode d’authentification secondaire sur une base de compte par utilisateur. Informez bien les utilisateurs que l’authentification multifacteur est en cours d’activation pour qu’ils comprennent les exigences telles que l’utilisation obligatoire d’un smartphone pour la connexion et puissent se connecter correctement.</span><span class="sxs-lookup"><span data-stu-id="65a30-p102">You'll enable MFA and configure the secondary authentication method on a per-user account basis. Make sure to let users know that MFA is being enabled so they understand the requirements, such as mandatory use of a smart phone to sign in, and can sign in successfully.</span></span>

<span data-ttu-id="65a30-115">Pour plus d’informations, voir [Planifier l’authentification multifacteur](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span><span class="sxs-lookup"><span data-stu-id="65a30-115">For more information, see [Plan for multi-factor authentication for Office 365 Deployments](https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-getstarted).</span></span>

>[!Note]
><span data-ttu-id="65a30-p103">Dans certaines applications, comme Microsoft Office 2010 ou antérieures et Apple Mail, vous ne pouvez pas utiliser l’authentification multifacteur. Pour utiliser ces applications, vous devez utiliser des « mots de passe d’application » à la place de votre mot de passe habituel. Le mot de passe d’application permet à l’application de contourner l’authentification multifacteur et de continuer à fonctionner. Pour en savoir plus sur les mots de passe d’application, reportez-vous à [Créer un mot de passe d’application pour Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span><span class="sxs-lookup"><span data-stu-id="65a30-p103">In some applications, such as Microsoft Office 2010 or older and Apple Mail, you can’t use MFA. To use these apps, you’ll need to use “app passwords” in place of your traditional password. The app password allows the app to bypass MFA and continue working. To learn more about app passwords, see [Create an app password for Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span></span>
>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="65a30-121">Guide du laboratoire de test : authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="65a30-121">Test Lab Guide: Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="65a30-122">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-mfa) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="65a30-122">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-mfa) for this step.</span></span>



<a name="identity-ident-prot"></a>
## <a name="protect-against-credential-compromise"></a><span data-ttu-id="65a30-123">Protégez-vous contre la compromission des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="65a30-123">Protect against credential compromise</span></span>

<span data-ttu-id="65a30-124">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="65a30-124">*This step is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="65a30-125">Cette section explique comment configurer des stratégies de protection contre la compromission d’informations d’identification consistant pour un attaquant à déterminer le nom de compte et le mot de passe d’un utilisateur afin d’accéder aux services et données cloud d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="65a30-125">In this step, you'll learn how to configure policies that protect against credential compromise, where an attacker determines a user’s account name and password to gain access to an organization’s cloud services and data. Azure AD Identity Protection provides a number of ways to help prevent an attacker from moving laterally through your accounts and groups, and subsequently, to your most valuable data.</span></span> <span data-ttu-id="65a30-126">Azure AD Identity Protection fournit un certain nombre de moyens pour empêcher un attaquant de se déplacer latéralement dans vos comptes et groupes, puis vers vos données les plus précieuses.</span><span class="sxs-lookup"><span data-stu-id="65a30-126">In this step, you'll learn how to configure policies that protect against credential compromise, where an attacker determines a user’s account name and password to gain access to an organization’s cloud services and data. Azure AD Identity Protection provides a number of ways to help prevent an attacker from moving laterally through your accounts and groups, and subsequently, to your most valuable data.</span></span>

<span data-ttu-id="65a30-127">Azure AD Identity Protection vous permet de :</span><span class="sxs-lookup"><span data-stu-id="65a30-127">With Azure AD Identity Protection, you can:</span></span>

|||
|:---------|:---------|
|<span data-ttu-id="65a30-128">déterminer et résoudre les vulnérabilités potentielles dans les identités de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="65a30-128">Determine and address potential vulnerabilities in your organization’s identities</span></span>|<span data-ttu-id="65a30-p105">Azure AD utilise l’apprentissage automatique pour détecter les anomalies et les activités douteuses, telles que les connexions et les activités post-connexion. À l’aide de ces données, Identity Protection génère des rapports et les alertes qui vous aident à évaluer les problèmes et à prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="65a30-p105">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span>|
|<span data-ttu-id="65a30-131">Détecter des actions douteuses qui sont liées aux identités de votre organisation et y répondre automatiquement</span><span class="sxs-lookup"><span data-stu-id="65a30-131">Detect suspicious actions that are related to your organization’s identities and respond to them automatically</span></span>|<span data-ttu-id="65a30-p106">Vous pouvez configurer des stratégies de risque qui répondent automatiquement aux problèmes détectés lorsqu’un niveau de risque spécifié a été atteint. Ces stratégies, en plus des autres contrôles d’accès conditionnel fournis par Azure Active Directory et Enterprise Mobility + Security (EMS) peuvent automatiquement bloquer l’accès ou prendre des actions correctives, comme réinitialiser les mots de passe et demander l’authentification multifacteur pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="65a30-p106">You can configure risk-based policies that automatically respond to detected issues when a specified risk level has been reached. These policies, in addition to other conditional access controls provided by Azure Active Directory and Enterprise Mobility + Security (EMS), can either automatically block access or take corrective actions, including password resets and requiring multi-factor authentication for subsequent sign-ins.</span></span>|
|<span data-ttu-id="65a30-134">Examiner les incidents suspects et les résoudre avec des actions d’administration</span><span class="sxs-lookup"><span data-stu-id="65a30-134">Investigate suspicious incidents and resolve them with administrative actions</span></span>|<span data-ttu-id="65a30-p107">Vous pouvez examiner des événements à risque en utilisant les informations sur l’incident de sécurité. Des flux de travail de base sont disponibles pour effectuer le suivi des enquêtes et lancer des actions de correction, telles que des réinitialisations du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="65a30-p107">You can investigate risk events using information about the security incident. Basic workflows are available to track investigations and initiate remediation actions, such as password resets.</span></span>|

<span data-ttu-id="65a30-137">[Plus d’informations sur Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span><span class="sxs-lookup"><span data-stu-id="65a30-137">See [more information about Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span></span>

<span data-ttu-id="65a30-138">Reportez-vous à la rubrique des [étapes pour activer Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span><span class="sxs-lookup"><span data-stu-id="65a30-138">See the [steps to enable Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span></span>

<span data-ttu-id="65a30-139">Les résultats de cette étape sont que vous avez activé Azure AD Identity Protection et que vous l’utilisez pour :</span><span class="sxs-lookup"><span data-stu-id="65a30-139">The results of this step are that you've enabled Azure AD Identity protection and you are using it to:</span></span>

- <span data-ttu-id="65a30-140">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="65a30-140">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="65a30-141">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="65a30-141">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="65a30-142">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="65a30-142">Investigate and address ongoing suspicious identity incidents.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="65a30-144">Guide de laboratoire de test : Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="65a30-144">Test Lab Guide: Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="65a30-145">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-ident-prot) pour cette section.</span><span class="sxs-lookup"><span data-stu-id="65a30-145">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-ident-prot) for this step.</span></span>

## <a name="monitor-tenant-and-sign-in-activity"></a><span data-ttu-id="65a30-146">Surveillez l’activité de connexion et du client</span><span class="sxs-lookup"><span data-stu-id="65a30-146">Monitor tenant and sign-in activity</span></span>

<span data-ttu-id="65a30-147">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="65a30-147">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="65a30-p108">Dans cette étape, vous allez passer en revue les journaux d’audit et l’activité de connexion à l’aide des rapports Azure AD. Deux types de rapports sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="65a30-p108">In this step, you'll review audit logs and sign-in activity using Azure AD reporting. Two types of reports are available.</span></span>

<span data-ttu-id="65a30-p109">Le **rapport d’activité des journaux d’audit** enregistre l’historique de toutes les tâches effectuées dans votre client Azure AD. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="65a30-p109">The **Audit logs activity report** records the history of every task performed in your Azure AD tenant. This report answers questions like:</span></span>

- <span data-ttu-id="65a30-152">Qui a ajouté une personne à un groupe d’administration ?</span><span class="sxs-lookup"><span data-stu-id="65a30-152">Who added someone to an admin group?</span></span>
- <span data-ttu-id="65a30-153">Quels sont les utilisateurs qui se connectent à une application spécifique ?</span><span class="sxs-lookup"><span data-stu-id="65a30-153">Which users are signing into a specific app?</span></span>
- <span data-ttu-id="65a30-154">Combien de réinitialisations de mot de passe sont prévues ?</span><span class="sxs-lookup"><span data-stu-id="65a30-154">How many password resets are happening?</span></span>

<span data-ttu-id="65a30-p110">Le **rapport d’activité des connexions** enregistre l’auteur des tâches indiquées par le rapport des journaux d’audit. Ce rapport répond aux questions telles que :</span><span class="sxs-lookup"><span data-stu-id="65a30-p110">The **Sign-ins activity report** records who performed the tasks reported by the audit logs report. This report answers questions like:</span></span>

- <span data-ttu-id="65a30-157">Pour un utilisateur spécifique à l’étude, quel est son modèle de connexion ?</span><span class="sxs-lookup"><span data-stu-id="65a30-157">For a specific user under investigation, what is their sign-in pattern?</span></span>
- <span data-ttu-id="65a30-158">Quel est mon volume de connexions par jour, semaine ou mois ?</span><span class="sxs-lookup"><span data-stu-id="65a30-158">What is my volume of sign-ins over a day, week, or month?</span></span>
- <span data-ttu-id="65a30-159">Combien de ces tentatives de connexion n’ont pas abouti, et pour quels comptes ?</span><span class="sxs-lookup"><span data-stu-id="65a30-159">How many of these sign-in attempts were not successful, and for which accounts?</span></span>

<span data-ttu-id="65a30-160">Pour plus d’informations sur les rapports et la façon d’y accéder, reportez-vous à la rubrique [Création de rapports Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="65a30-160">For more information about the reports and how to access them, see [Azure Active Directory reporting](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-azure-portal).</span></span>

<span data-ttu-id="65a30-161">Après cette étape, vous connaîtrez ces rapports et saurez comment les utiliser pour obtenir des informations sur les activités et événements Azure AD à des fins de planification et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="65a30-161">As a result of this step, you'll gain awareness of these reports and an understanding of how you can use them to gain insights on Azure AD events and activities for planning and security purposes.</span></span>



## <a name="next-step"></a><span data-ttu-id="65a30-162">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="65a30-162">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step5.png)| [<span data-ttu-id="65a30-163">Simplifier l’accès pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="65a30-163">Simplify access for users</span></span>](identity-password-reset.md) |

