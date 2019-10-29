---
title: 'Étape 2 : Sécuriser vos mots de passe'
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
description: Vous devez rendre vos mots de passe forts et gérables au sein de votre organisation.
ms.openlocfilehash: 375f4a678e85dccb544ffaf56f648e98609841d9
ms.sourcegitcommit: 2aeafb631aaabc53eea0a8029711eb891e48d249
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2019
ms.locfileid: "37746510"
---
# <a name="step-2-secure-your-passwords"></a><span data-ttu-id="d1b5c-103">Étape 2 : Sécuriser vos mots de passe</span><span class="sxs-lookup"><span data-stu-id="d1b5c-103">Step 2: Secure your passwords</span></span>

![Phase 2 - Identité](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<a name="identity-password-prot"></a>
## <a name="prevent-bad-passwords"></a><span data-ttu-id="d1b5c-105">Éviter les mots de passe incorrects</span><span class="sxs-lookup"><span data-stu-id="d1b5c-105">Prevent bad passwords</span></span>

<span data-ttu-id="d1b5c-106">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d1b5c-106">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="d1b5c-107">Tous vos utilisateurs doivent utiliser le [guide des mots de passe Microsoft](https://www.microsoft.com/research/publication/password-guidance/) pour créer leurs mots de passe de compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-107">All your users should be using [Microsoft's password guidance](https://www.microsoft.com/research/publication/password-guidance/) to create their user account passwords.</span></span>

<span data-ttu-id="d1b5c-108">Pour empêcher les utilisateurs de créer un mot de passe facile à déterminer, optez pour la protection par mot de passe Azure AD qui utilise une liste globale de mots de passe interdits et une liste personnalisée facultative de mots de passe interdits que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-108">To prevent users from creating an easily-determined password, use Azure AD password protection, which uses both a global banned password list and an optional custom banned password list that you specify.</span></span> <span data-ttu-id="d1b5c-109">Par exemple, vous pouvez spécifier des termes propres à votre organisation, tels que :</span><span class="sxs-lookup"><span data-stu-id="d1b5c-109">For example, you can specify terms that are specific to your organization, such as:</span></span>

- <span data-ttu-id="d1b5c-110">Noms de marques</span><span class="sxs-lookup"><span data-stu-id="d1b5c-110">Brand names</span></span>
- <span data-ttu-id="d1b5c-111">Noms de produits</span><span class="sxs-lookup"><span data-stu-id="d1b5c-111">Product names</span></span>
- <span data-ttu-id="d1b5c-112">Emplacements (par exemple, le siège social de l’entreprise)</span><span class="sxs-lookup"><span data-stu-id="d1b5c-112">Locations (for example, such as company headquarters)</span></span>
- <span data-ttu-id="d1b5c-113">Termes internes spécifiques à l’entreprise</span><span class="sxs-lookup"><span data-stu-id="d1b5c-113">Company-specific internal terms</span></span>
- <span data-ttu-id="d1b5c-114">Abréviations dotées d’une signification spécifique à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-114">Abbreviations that have specific company meaning</span></span>

<span data-ttu-id="d1b5c-115">Vous pouvez interdire les mots de passe incorrects [dans le cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) et localement pour [Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises).</span><span class="sxs-lookup"><span data-stu-id="d1b5c-115">You can ban bad passwords [in the cloud](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad) and for your [on-premises Active Directory Domain Services (AD DS)](https://docs.microsoft.com/azure/active-directory/authentication/concept-password-ban-bad-on-premises).</span></span>

<span data-ttu-id="d1b5c-116">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-password-prot) de cette section.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-116">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-password-prot) for this section.</span></span>

<a name="identity-pw-reset"></a>
## <a name="simplify-password-resets"></a><span data-ttu-id="d1b5c-117">Simplifiez les réinitialisations du mot de passe</span><span class="sxs-lookup"><span data-stu-id="d1b5c-117">Simplify password resets</span></span>

<span data-ttu-id="d1b5c-118">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d1b5c-118">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="d1b5c-119">Dans cette section, vous autoriserez la réinitialisation de mot de passe en libre-service (SSPR) d’Azure AD pour permettre aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou leurs comptes.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-119">In this section, you'll enable self-service password reset (SSPR) to allow users to reset or unlock their passwords or accounts.</span></span> <span data-ttu-id="d1b5c-120">Le système inclut des rapports détaillés de suivi d’accès au système, ainsi que des notifications pour vous prévenir de toute utilisation malveillante ou de tout abus.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-120">To alert you to misuse or abuse, you can use the detailed reporting that tracks when users access the system, along with notifications.</span></span> <span data-ttu-id="d1b5c-121">Vous devez activer l’écriture différée de mot de passe avant de pouvoir déployer la réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-121">You must enable password writeback before you can deploy password resets.</span></span>

<span data-ttu-id="d1b5c-122">Reportez-vous aux [Instructions pour activer la réinitialisation de mot de passe](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-deployment).</span><span class="sxs-lookup"><span data-stu-id="d1b5c-122">See the [instructions to roll out password reset](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-deployment).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="d1b5c-124">Guide du laboratoire de test : Réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="d1b5c-124">Test Lab Guide: Password reset</span></span>](password-reset-m365-ent-test-environment.md) |
|||

<span data-ttu-id="d1b5c-125">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pw-reset) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-125">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pw-reset) for this section.</span></span>


<a name="identity-sso"></a>
## <a name="simplify-user-sign-in"></a><span data-ttu-id="d1b5c-126">Simplifiez la connexion utilisateur</span><span class="sxs-lookup"><span data-stu-id="d1b5c-126">Simplify user sign-in</span></span>

<span data-ttu-id="d1b5c-127">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d1b5c-127">*This is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="d1b5c-128">Dans cette section, vous devrez configurer Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO), qui fonctionne avec la Synchronisation de hachage de mot de passe (PHS) et l'Authentification directe (PTA), pour autoriser vos utilisateurs à se connecter aux services qui utilisent des comptes d’utilisateurs Azure AD sans avoir à taper leur mot de passe, et dans de nombreux cas, leur nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-128">In this section, you'll set up Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO), which works with Password Hash Synchronization (PHS) and Pass-Through Authentication (PTA), to allow your users to sign in to services that use Azure AD user accounts without having to type in their passwords, and in many cases, their usernames.</span></span> <span data-ttu-id="d1b5c-129">Cela donne à vos utilisateurs un accès facile aux applications basées sur le cloud, telles qu’Office 365, sans nécessiter des composants supplémentaires en local, tels que des serveurs de fédération d’identité.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-129">This gives your users easier access to cloud-based applications, such as Office 365, without needing any additional on-premises components such as identity federation servers.</span></span>

<span data-ttu-id="d1b5c-130">Vous configurez l’authentification unique transparente Azure AD avec l’outil Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-130">You configure Azure AD Seamless SSO with the Azure AD Connect tool.</span></span>

<span data-ttu-id="d1b5c-131">Reportez-vous aux [instructions pour configurer l’authentification unique transparente d’Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span><span class="sxs-lookup"><span data-stu-id="d1b5c-131">See the [instructions to configure Azure AD Seamless SSO](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="d1b5c-133">Guide de laboratoire de test : authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="d1b5c-133">Test Lab Guide: Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md) |
|||

<span data-ttu-id="d1b5c-134">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-sso) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-134">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sso) for this section.</span></span>


<a name="identity-custom-sign-in"></a>
## <a name="customize-the-office-365-sign-in-page"></a><span data-ttu-id="d1b5c-135">Personnaliser la page de connexion à Office 365</span><span class="sxs-lookup"><span data-stu-id="d1b5c-135">Customize the Office 365 sign-in page</span></span>

<span data-ttu-id="d1b5c-136">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d1b5c-136">*This is optional and for both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="d1b5c-137">Dans cette section, vous allez permettre aux utilisateurs de reconnaître la page de connexion de votre organisation en ajoutant le nom de votre entreprise, votre logo et d’autres éléments reconnaissables.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-137">In this section, you'll help users recognize your organization’s sign-in page by adding your company name, logo, and other recognizable elements.</span></span> 

<span data-ttu-id="d1b5c-138">Microsoft 365 Entreprise vous permet de personnaliser l’aspect des pages de connexion et du panneau d’accès pour y inclure votre logo d’entreprise, des modèles de couleurs et des informations personnalisées sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-138">With Microsoft 365 Enterprise, you can customize the appearance of the sign-in and Access Panel pages so they include your company logo, color schemes, and custom user information.</span></span> 

<span data-ttu-id="d1b5c-139">Pour plus d’informations, reportez-vous à la rubrique [Ajouter l’identité de votre entreprise à la page de connexion d’Office 365](https://docs.microsoft.com/office365/admin/setup/customize-sign-in-page).</span><span class="sxs-lookup"><span data-stu-id="d1b5c-139">For more information, see [Add your company branding to Office 365 Sign In page](https://docs.microsoft.com/office365/admin/setup/customize-sign-in-page).</span></span>

<span data-ttu-id="d1b5c-140">Pour des instructions de configuration, reportez-vous à la rubrique relative à l’[ajout de l’identité de votre entreprise à vos pages de connexion et de panneau d’accès](https://aka.ms/aadpaddbranding).</span><span class="sxs-lookup"><span data-stu-id="d1b5c-140">For configuration instructions, see [Add company branding to your sign-in and Access Panel pages](https://aka.ms/aadpaddbranding).</span></span>

<span data-ttu-id="d1b5c-141">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-custom-sign-in) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="d1b5c-141">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-custom-sign-in) for this section.</span></span>

## <a name="next-step"></a><span data-ttu-id="d1b5c-142">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d1b5c-142">Next step</span></span>

|||
|:-------|:-----|
|![Étape 3](./media/stepnumbers/Step3.png)| [<span data-ttu-id="d1b5c-144">Sécuriser et gérer les connexions de vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d1b5c-144">Secure and manage your user sign-ins</span></span>](identity-secure-user-sign-ins.md) |
