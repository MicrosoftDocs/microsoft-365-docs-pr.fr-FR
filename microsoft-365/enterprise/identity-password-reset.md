---
title: 'Étape 5 : Simplifier l’accès pour les utilisateurs'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez la réinitialisation du mot de passe libre-service (SSPR) pour Azure AD.
ms.openlocfilehash: b57291aabf1b51e7866dba10ba50eacc27291a2a
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34073724"
---
# <a name="step-5-simplify-access-for-users"></a><span data-ttu-id="78c44-103">Étape 5 : Simplifier l’accès pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="78c44-103">Step 5: Simplify access for users</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)


<a name="identity-pw-writeback"></a>
## <a name="simplify-password-updates"></a><span data-ttu-id="78c44-104">Simplifiez les mises à jour du mot de passe</span><span class="sxs-lookup"><span data-stu-id="78c44-104">Simplify password updates</span></span>

<span data-ttu-id="78c44-105">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="78c44-105">*This is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="78c44-106">Dans cette section, vous devez autoriser les utilisateurs à réinitialiser leur mot de passe via Azure Active Directory (Azure AD), qui est ensuite répliqué sur votre Active Directory Domain Services (AD DS)local.</span><span class="sxs-lookup"><span data-stu-id="78c44-106">In this section, you'll allow users to reset their passwords through Azure Active Directory (Azure AD), which is then replicated to your local Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="78c44-107">Ce processus est appelé écriture différée de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="78c44-107">This process is known as password writeback.</span></span> <span data-ttu-id="78c44-108">Avec l’écriture différée de mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe via la version locale Active Directory Domain Services où sont stockés les comptes d’utilisateurs et leurs attributs.</span><span class="sxs-lookup"><span data-stu-id="78c44-108">With password writeback, users don’t need to update their passwords through the on-premises Active Directory Domain Services (AD DS) where user accounts and their attributes are stored.</span></span> <span data-ttu-id="78c44-109">C’est utile pour les utilisateurs itinérants ou distants qui ne possèdent pas de connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="78c44-109">This is valuable to roaming or remote users who do not have a remote access connection to the on-premises network.</span></span>

<span data-ttu-id="78c44-110">L’écriture différée de mot de passe est requise pour exploiter entièrement les fonctionnalités de la protection des identités, comme obliger les utilisateurs à modifier leur mot de passe en local lorsqu’un risque élevé de compromission de compte a été détecté.</span><span class="sxs-lookup"><span data-stu-id="78c44-110">Password writeback is required to fully utilize Identity Protection feature capabilities, such as requiring users to change their on-premises passwords when there has been a high risk of account compromise detected.</span></span>

<span data-ttu-id="78c44-111">Pour obtenir plus d’informations et les instructions de configuration, consultez l’article [Azure AD SSPR avec l’écriture différée de mot de passe](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span><span class="sxs-lookup"><span data-stu-id="78c44-111">For additional information and configuration instructions, see [Azure AD SSPR with password writeback](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-writeback).</span></span>

>[!Note]
><span data-ttu-id="78c44-p102">Procédez à la mise à niveau vers la dernière version d’Azure AD Connect pour vous assurer la meilleure expérience possible et les nouvelles fonctionnalités dès leur diffusion. Pour obtenir plus d’informations, consultez l’article [Installation personnalisée d’Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span><span class="sxs-lookup"><span data-stu-id="78c44-p102">Upgrade to the latest version of Azure AD Connect to ensure the best possible experience and new features as they are released. For more information, see [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).</span></span>
>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="78c44-115">Guide du laboratoire de test : Écriture différée de mot de passe</span><span class="sxs-lookup"><span data-stu-id="78c44-115">Test Lab Guide: Password writeback</span></span>](password-writeback-m365-ent-test-environment.md) |
|||

<span data-ttu-id="78c44-116">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pw-writeback) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="78c44-116">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pw-writeback) for this section.</span></span>

<a name="identity-pw-reset"></a>
## <a name="simplify-password-resets"></a><span data-ttu-id="78c44-117">Simplifiez les réinitialisations du mot de passe</span><span class="sxs-lookup"><span data-stu-id="78c44-117">Simplify password resets</span></span>

<span data-ttu-id="78c44-118">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="78c44-118">*This is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="78c44-119">Dans cette section, vous autoriserez la réinitialisation de mot de passe en libre-service (SSPR) d’Azure AD pour permettre aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou leurs comptes.</span><span class="sxs-lookup"><span data-stu-id="78c44-119">In this section, you'll enable self-service password reset (SSPR) to allow users to reset or unlock their passwords or accounts.</span></span> <span data-ttu-id="78c44-120">Le système inclut des rapports détaillés de suivi d’accès au système, ainsi que des notifications pour vous prévenir de toute utilisation malveillante ou de tout abus.</span><span class="sxs-lookup"><span data-stu-id="78c44-120">To alert you to misuse or abuse, you can use the detailed reporting that tracks when users access the system, along with notifications.</span></span> <span data-ttu-id="78c44-121">Vous devez activer l’écriture différée de mot de passe avant de pouvoir déployer la réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="78c44-121">You must enable password writeback before you can deploy password resets.</span></span>

<span data-ttu-id="78c44-122">Reportez-vous aux [Instructions pour activer la réinitialisation de mot de passe](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-deployment).</span><span class="sxs-lookup"><span data-stu-id="78c44-122">See the [instructions to roll out password reset](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-deployment).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="78c44-124">Guide du laboratoire de test : Réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="78c44-124">Test Lab Guide: Password reset</span></span>](password-reset-m365-ent-test-environment.md) |
|||

<span data-ttu-id="78c44-125">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-pw-reset) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="78c44-125">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-pw-reset) for this section.</span></span>


<a name="identity-sso"></a>
## <a name="simplify-user-sign-in"></a><span data-ttu-id="78c44-126">Simplifiez la connexion utilisateur</span><span class="sxs-lookup"><span data-stu-id="78c44-126">Simplify user sign-in</span></span>

<span data-ttu-id="78c44-127">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="78c44-127">*This is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="78c44-128">Dans cette section, vous devrez configurer Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO) pour autoriser vos utilisateurs à se connecter aux services qui utilisent des comptes d’utilisateurs Azure AD sans taper leur mot de passe, ni dans de nombreux cas, leur nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78c44-128">In this section, you'll set up Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO) to allow your users to sign in to services that use Azure AD user accounts without having to type in their passwords, and in many cases, their usernames.</span></span> <span data-ttu-id="78c44-129">Cela donne à vos utilisateurs un accès facile aux applications basées sur le cloud, telles qu’Office 365, sans nécessiter des composants supplémentaires en local, tels que des serveurs de fédération d’identité.</span><span class="sxs-lookup"><span data-stu-id="78c44-129">This gives your users easier access to cloud-based applications, such as Office 365, without needing any additional on-premises components such as identity federation servers.</span></span>

<span data-ttu-id="78c44-130">Vous allez configurer l’authentification unique transparente d’Azure AD avec l’outil Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="78c44-130">You'll configure Azure AD Seamless SSO with the Azure AD Connect tool.</span></span>

<span data-ttu-id="78c44-131">Reportez-vous aux [instructions pour configurer l’authentification unique transparente d’Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span><span class="sxs-lookup"><span data-stu-id="78c44-131">See the [instructions to configure Azure AD Seamless SSO](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="78c44-133">Guide de laboratoire de test : authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="78c44-133">Test Lab Guide: Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md) |
|||

<span data-ttu-id="78c44-134">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-sso) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="78c44-134">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sso) for this section.</span></span>


<a name="identity-custom-sign-in"></a>
## <a name="customize-the-office-365-sign-in-page"></a><span data-ttu-id="78c44-135">Personnaliser la page de connexion à Office 365</span><span class="sxs-lookup"><span data-stu-id="78c44-135">Customize the Office 365 sign-in page</span></span>

<span data-ttu-id="78c44-136">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="78c44-136">*This is optional and for both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="78c44-137">Dans cette section, vous allez permettre aux utilisateurs de reconnaître la page de connexion de votre organisation en ajoutant le nom de votre entreprise, votre logo et d’autres éléments reconnaissables.</span><span class="sxs-lookup"><span data-stu-id="78c44-137">In this section, you'll help users recognize your organization’s sign-in page by adding your company name, logo, and other recognizable elements.</span></span> 

<span data-ttu-id="78c44-138">Microsoft 365 Entreprise vous permet de personnaliser l’aspect des pages de connexion et du panneau d’accès pour y inclure votre logo d’entreprise, des modèles de couleurs et des informations personnalisées sur l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="78c44-138">With Microsoft 365 Enterprise, you can customize the appearance of the sign-in and Access Panel pages so they include your company logo, color schemes, and custom user information.</span></span> 

<span data-ttu-id="78c44-139">Lorsqu’un utilisateur tente de se connecter à partir d’un appareil, il voit une page ressemblant à l’exemple de page de connexion à Office 365 suivant *avant personnalisation*.</span><span class="sxs-lookup"><span data-stu-id="78c44-139">When a user attempts to sign in from a device, they see something like the following example on the Office 365 sign-in page *before customization*.</span></span>

![Exemple de page de connexion à Office 365 avant personnalisation](./media/identity-customize-office-365-sign-in/id-step01-sign-in-before.png)

<span data-ttu-id="78c44-141">Et voici ce que le même utilisateur de Contoso Corporation verrait *après personnalisation*.</span><span class="sxs-lookup"><span data-stu-id="78c44-141">And here is what the same user of the Contoso Corporation would see *after customization*.</span></span>

![Exemple de page de connexion à Office 365 après personnalisation](./media/identity-customize-office-365-sign-in/id-step01-sign-in-after.png)

<span data-ttu-id="78c44-143">Pour plus d’informations, reportez-vous à la rubrique [Ajouter l’identité de votre entreprise à la page de connexion d’Office 365](https://docs.microsoft.com/office365/admin/setup/customize-sign-in-page).</span><span class="sxs-lookup"><span data-stu-id="78c44-143">For more information, see [Add your company branding to Office 365 Sign In page](https://docs.microsoft.com/office365/admin/setup/customize-sign-in-page).</span></span>

<span data-ttu-id="78c44-144">Pour des instructions de configuration, reportez-vous à la rubrique relative à l’[ajout de l’identité de votre entreprise à vos pages de connexion et de panneau d’accès](http://aka.ms/aadpaddbranding).</span><span class="sxs-lookup"><span data-stu-id="78c44-144">For configuration instructions, see [Add company branding to your sign-in and Access Panel pages](http://aka.ms/aadpaddbranding).</span></span>

<span data-ttu-id="78c44-145">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-custom-sign-in) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="78c44-145">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-custom-sign-in) for this section.</span></span>


## <a name="next-step"></a><span data-ttu-id="78c44-146">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="78c44-146">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step6.png)| [<span data-ttu-id="78c44-147">Utiliser des groupes pour faciliter la gestion</span><span class="sxs-lookup"><span data-stu-id="78c44-147">Use groups for easier management</span></span>](identity-self-service-group-management.md) |


