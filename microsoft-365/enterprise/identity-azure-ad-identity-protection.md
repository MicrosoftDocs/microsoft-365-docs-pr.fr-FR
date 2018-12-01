---
title: 'Étape 6 : Se protéger contre la compromission de confidentialité'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/01/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez Azure AD Identity Protection.
ms.openlocfilehash: b1dea9d2917c45bf87bd972f56c9eac2b074c252
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867483"
---
# <a name="step-6-protect-against-credential-compromise"></a><span data-ttu-id="ffe03-103">Étape 6 : Se protéger contre la compromission de confidentialité</span><span class="sxs-lookup"><span data-stu-id="ffe03-103">Step 6: Protect against credential compromise</span></span>

<span data-ttu-id="ffe03-104">*Cette étape est facultative et s’applique uniquement à la version E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="ffe03-104">*This step is optional and applies only to the E5 version of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="ffe03-p101">Dans cette étape, vous allez découvrir comment configurer des stratégies destinées à protéger contre la compromission de confidentialité, lorsqu’un utilisateur malveillant détermine le nom et le mot de passe d’un compte d’utilisateur pour accéder aux services cloud et aux données d’une organisation. Azure AD Identity Protection fournit plusieurs méthodes permettant d’empêcher un utilisateur malveillant de consulter vos comptes et groupes et par la suite, vos données les plus précieuses.</span><span class="sxs-lookup"><span data-stu-id="ffe03-p101">In Step 15, you'll learn how to configure policies that protect against credential compromise, where an attacker determines a user’s account name and password to gain access to an organization’s cloud services and data. Azure AD Identity Protection provides a number of ways to help prevent an attacker from moving laterally through your accounts and groups, and subsequently, to your most valuable data.</span></span>

<span data-ttu-id="ffe03-107">Azure AD Identity Protection vous permet de :</span><span class="sxs-lookup"><span data-stu-id="ffe03-107">With Azure AD Identity Protection, you can:</span></span>

|||
|:---------|:---------|
|<span data-ttu-id="ffe03-108">déterminer et résoudre les vulnérabilités potentielles dans les identités de votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="ffe03-108">Determine and address potential vulnerabilities in your organization’s identities</span></span>|<span data-ttu-id="ffe03-p102">Azure AD utilise l’apprentissage automatique pour détecter les anomalies et les activités douteuses, telles que les connexions et les activités post-connexion. À l’aide de ces données, Identity Protection génère des rapports et les alertes qui vous aident à évaluer les problèmes et à prendre des mesures.</span><span class="sxs-lookup"><span data-stu-id="ffe03-p102">Azure AD uses machine learning to detect anomalies and suspicious activity, such as sign-ins and post-sign-in activities. Using this data, Identity Protection generates reports and alerts that help you evaluate the issues and take action.</span></span>|
|<span data-ttu-id="ffe03-111">Détecter des actions douteuses qui sont liées aux identités de votre organisation et y répondre automatiquement</span><span class="sxs-lookup"><span data-stu-id="ffe03-111">Detect suspicious actions that are related to your organization’s identities and respond to them automatically</span></span>|<span data-ttu-id="ffe03-p103">Vous pouvez configurer des stratégies de risque qui répondent automatiquement aux problèmes détectés lorsqu’un niveau de risque spécifié a été atteint. Ces stratégies, en plus des autres contrôles d’accès conditionnel fournis par Azure Active Directory et Enterprise Mobility + Security (EMS) peuvent automatiquement bloquer l’accès ou prendre des actions correctives, comme réinitialiser les mots de passe et demander l’authentification multifacteur pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffe03-p103">You can configure risk-based policies that automatically respond to detected issues when a specified risk level has been reached. These policies, in addition to other conditional access controls provided by Azure Active Directory and Enterprise Mobility + Security (EMS), can either automatically block access or take corrective actions, including password resets and requiring multi-factor authentication for subsequent sign-ins.</span></span>|
|<span data-ttu-id="ffe03-114">Examiner les incidents suspects et les résoudre avec des actions d’administration</span><span class="sxs-lookup"><span data-stu-id="ffe03-114">Investigate suspicious incidents and resolve them with administrative actions</span></span>|<span data-ttu-id="ffe03-p104">Vous pouvez examiner des événements à risque en utilisant les informations sur l’incident de sécurité. Des flux de travail de base sont disponibles pour effectuer le suivi des enquêtes et lancer des actions de correction, telles que des réinitialisations du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="ffe03-p104">You can investigate risk events using information about the security incident. Basic workflows are available to track investigations and initiate remediation actions, such as password resets.</span></span>|

<span data-ttu-id="ffe03-117">[Plus d’informations sur Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span><span class="sxs-lookup"><span data-stu-id="ffe03-117">See [more information about Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection).</span></span>

<span data-ttu-id="ffe03-118">Reportez-vous à la rubrique des [étapes pour activer Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span><span class="sxs-lookup"><span data-stu-id="ffe03-118">See the [steps to enable Azure AD Identity Protection](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).</span></span>

<span data-ttu-id="ffe03-119">Les résultats de cette étape sont que vous avez activé Azure AD Identity Protection et que vous l’utilisez pour :</span><span class="sxs-lookup"><span data-stu-id="ffe03-119">The results of this step are that you've enabled Azure AD Identity protection and you are using it to:</span></span>

- <span data-ttu-id="ffe03-120">résoudre les vulnérabilités d’identités potentielles ;</span><span class="sxs-lookup"><span data-stu-id="ffe03-120">Address potential identity vulnerabilities.</span></span>
- <span data-ttu-id="ffe03-121">détecter les tentatives de compromission d’informations d’identification possibles ;</span><span class="sxs-lookup"><span data-stu-id="ffe03-121">Detect possible credential compromise attempts.</span></span>
- <span data-ttu-id="ffe03-122">examiner et résoudre des incidents d’identités suspects en cours.</span><span class="sxs-lookup"><span data-stu-id="ffe03-122">Investigate and address ongoing suspicious identity incidents.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="ffe03-124">Guide de laboratoire de test : Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="ffe03-124">Test Lab Guide: Azure AD Identity Protection</span></span>](azure-ad-identity-protection-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="ffe03-125">Comme point de vérification temporaire, vous pouvez voir les [critères de sortie](identity-exit-criteria.md#crit-identity-ident-prot) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="ffe03-125">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-ident-prot) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="ffe03-126">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ffe03-126">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step7.png)| [<span data-ttu-id="ffe03-127">Synchroniser des annuaires</span><span class="sxs-lookup"><span data-stu-id="ffe03-127">Synchronize directories</span></span>](identity-azure-ad-connect.md) |


