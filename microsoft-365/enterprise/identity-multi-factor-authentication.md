---
title: 'Étape 5 : Configurer l’authentification multifacteur'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/05/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez l’authentification multifacteur pour les comptes d’utilisateur.
ms.openlocfilehash: a54eb047c94430a2b3f61d06500c929e400e3d82
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867323"
---
# <a name="step-5-set-up-multi-factor-authentication"></a><span data-ttu-id="65ac9-103">Étape 5 : Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="65ac9-103">Step 5: Set up multi-factor authentication</span></span>

<span data-ttu-id="65ac9-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="65ac9-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="65ac9-p101">Lors de cette étape, vous allez configurer l’authentification multifacteur (MFA) pour ajouter une deuxième couche de sécurité aux connexions et transactions de l’utilisateur. L’authentification multifacteur nécessite une méthode de vérification supplémentaire une fois que les utilisateurs ont entré correctement leur mot de passe. Sans l’authentification multifacteur, le mot de passe est la seule méthode de vérification. Le problème avec les mots de passe est qu’un grand nombre d’entre eux peuvent facilement être devinés par une personne malveillante ou partagés involontairement avec des parties non approuvées.</span><span class="sxs-lookup"><span data-stu-id="65ac9-p101">In Step 7, you'll set up multi-factor authentication (MFA) to add a second layer of security to user sign-ins and transactions. MFA requires an additional verification method after users have correctly entered their password. Without MFA, the password is the only verification method. The problem with passwords is that many of them are easily guessed by an attacker or unknowingly shared with untrusted parties.</span></span>

<span data-ttu-id="65ac9-109">Avec l’authentification multifacteur, la deuxième couche de sécurité peut être :</span><span class="sxs-lookup"><span data-stu-id="65ac9-109">With MFA, the second layer of security can be:</span></span>

- <span data-ttu-id="65ac9-110">un appareil personnel et approuvé qui n’est pas facilement usurpé ou dupliqué (un smartphone, par exemple) ;</span><span class="sxs-lookup"><span data-stu-id="65ac9-110">A personal and trusted device that isn’t easily spoofed or duplicated, such as a smart phone.</span></span>
- <span data-ttu-id="65ac9-111">un attribut biométrique (une empreinte numérique, par exemple).</span><span class="sxs-lookup"><span data-stu-id="65ac9-111">A biometric attribute, such as a fingerprint.</span></span>

<span data-ttu-id="65ac9-p102">Vous allez activer l’authentification multifacteur et configurer la méthode d’authentification secondaire sur une base de compte par utilisateur. Informez bien les utilisateurs que l’authentification multifacteur est en cours d’activation pour qu’ils comprennent les exigences telles que l’utilisation obligatoire d’un smartphone pour la connexion et puissent se connecter correctement.</span><span class="sxs-lookup"><span data-stu-id="65ac9-p102">You'll enable MFA and configure the secondary authentication method on a per-user account basis. Make sure to let users know that MFA is being enabled so they understand the requirements (such as mandatory use of a smart phone to sign in) and can sign in successfully.</span></span>

<span data-ttu-id="65ac9-114">Pour plus d’informations, reportez-vous à [Planifier l’authentification multifacteur pour les déploiements Office 365](https://support.office.com/article/Plan-for-multifactor-authentication-for-Office-365-Deployments-043807b2-21db-4d5c-b430-c8a6dee0e6ba).</span><span class="sxs-lookup"><span data-stu-id="65ac9-114">For more information, see [Plan for multi-factor authentication for Office 365 Deployments](https://support.office.com/article/Plan-for-multifactor-authentication-for-Office-365-Deployments-043807b2-21db-4d5c-b430-c8a6dee0e6ba).</span></span>

<span data-ttu-id="65ac9-115">Pour configurer l’authentification multifacteur, reportez-vous à [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).</span><span class="sxs-lookup"><span data-stu-id="65ac9-115">To configure multifactor authentication, [Set up multi-factor authentication for Office 365 users](https://support.office.com/article/Set-up-multi-factor-authentication-for-Office-365-users-8f0454b2-f51a-4d9c-bcde-2c48e41621c6).</span></span>

<span data-ttu-id="65ac9-p103">Vous pouvez exiger une authentification multifacteur avec des stratégies d’accès conditionnel. Par exemple, vous pouvez configurer une stratégie qui exigeait l’authentification multifacteur lorsque l’authentification est déterminée comme étant à risque élevé ou moyen. Pour plus d’informations, reportez-vous à [Stratégies communes pour les identités et l’accès aux appareils](identity-access-policies.md#require-mfa-based-on-sign-in-risk).</span><span class="sxs-lookup"><span data-stu-id="65ac9-p103">You can also require MFA with conditional access policies. For example, you can configure a policy that required MFA when the authentication is determined to be of medium or high risk. For more information, see [Step 2: Configure conditional access policy settings](identity-access-policies.md#require-mfa-based-on-sign-in-risk) in the Information Protection phase.</span></span>

>[!Note]
><span data-ttu-id="65ac9-p104">Dans certaines applications, comme Microsoft Office 2010 ou antérieures et Apple Mail, vous ne pouvez pas utiliser l’authentification multifacteur. Pour utiliser ces applications, vous devez utiliser des « mots de passe d’application » à la place de votre mot de passe habituel. Le mot de passe d’application permet à l’application de contourner l’authentification multifacteur et de continuer à fonctionner. Pour en savoir plus sur les mots de passe d’application, reportez-vous à [Créer un mot de passe d’application pour Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span><span class="sxs-lookup"><span data-stu-id="65ac9-p104">In some applications, such as Microsoft Office 2010 or older and Apple Mail, you can’t use MFA. To use these apps, you’ll need to use “app passwords” in place of your traditional password. The app password allows the app to bypass MFA and continue working. To learn more about app passwords, see [Create an app password for Office 365](https://support.office.com/article/Create-an-app-password-for-Office-365-3e7c860f-bda4-4441-a618-b53953ee1183).</span></span>
>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="65ac9-124">Guide du laboratoire de test : authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="65ac9-124">Test Lab Guide: Multi-factor authentication</span></span>](multi-factor-authentication-microsoft-365-test-environment.md) |
|||

<span data-ttu-id="65ac9-125">Comme point de vérification temporaire, vous pouvez voir les [critères de sortie](identity-exit-criteria.md#crit-identity-mfa) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="65ac9-125">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-mfa) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="65ac9-126">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="65ac9-126">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step6.png)| [<span data-ttu-id="65ac9-127">Se protéger contre la compromission de confidentialité</span><span class="sxs-lookup"><span data-stu-id="65ac9-127">Protect against credential compromise</span></span>](identity-azure-ad-identity-protection.md) |

