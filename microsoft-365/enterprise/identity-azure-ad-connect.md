---
title: 'Étape 7 : Synchroniser les identités'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/09/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez les options d’identité et configurez Azure AD Connect pour synchroniser votre version locale de Windows Server AD avec Azure AD.
ms.openlocfilehash: 2391ee11a1706bbbfdeb248c5967822d3ea68f72
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866913"
---
# <a name="step-7-synchronize-identities"></a><span data-ttu-id="ff6e9-103">Étape 7 : Synchroniser les identités</span><span class="sxs-lookup"><span data-stu-id="ff6e9-103">Step 7: Synchronize identities</span></span>

<span data-ttu-id="ff6e9-104">*Cette étape est requise pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="ff6e9-104">*This step is required for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="ff6e9-105">Dans cette étape, vous allez synchroniser votre version locale de Windows Server Active Directory (AD) avec le client Azure Active Directory (AD) utilisé par vos abonnements Office 365 et Enterprise Mobility + Security (EMS).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-105">In this step, you'll synchronize your on-premises Windows Server Active Directory (AD) with the Azure Active Directory (AD) tenant used by your Office 365 and Enterprise Mobility + Security (EMS) subscriptions.</span></span>

<span data-ttu-id="ff6e9-106">Azure AD Connect est l’outil Microsoft pris en charge qui vous guide à travers la synchronisation des identités dont vous avez vraiment besoin seulement, à partir d’environnements Windows Server AD uniques ou à plusieurs forêts avec votre client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ff6e9-106">Azure AD Connect is the supported Microsoft tool that guides you through synchronizing only the identities you really need from single or multi-forest Windows Server AD environments to your Azure AD tenant.</span></span>

![Comment Azure AD Connect synchronise votre répertoire local avec Azure AD](./media/identity-azure-ad-connect/azure-ad-connect.png)

<span data-ttu-id="ff6e9-108">*Comment Azure AD Connect synchronise votre répertoire local avec Azure AD*</span><span class="sxs-lookup"><span data-stu-id="ff6e9-108">*How Azure AD Connect synchronizes your on-premises directory with Azure AD*</span></span>

<span data-ttu-id="ff6e9-p101">La première décision dans votre solution d’identité hybride est votre exigence d’authentification. Vous disposez des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p101">The first decision in your hybrid identity solution is your authentication requirement. The following options are options:</span></span>

- <span data-ttu-id="ff6e9-p102">Avec l’**authentification gérée**, Azure AD gère le processus d’authentification pour la connexion de l’utilisateur. Il existe deux méthodes pour l’authentification gérée :</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p102">With **managed authentication**, Azure AD handles the authentication process for user sign-in. There are two methods for managed authentication:</span></span> 
    - <span data-ttu-id="ff6e9-p103">**Synchronisation de hachage de mot de passe** [recommandée et requise pour certaines fonctionnalités premium]. Cette méthode est la plus simple pour activer l’authentification pour les objets de répertoire locaux dans Azure AD. Azure AD Connect extrait le mot de passe haché de Windows Server AD, effectue un traitement de sécurité supplémentaire sur le mot de passe et l’enregistre dans Azure AD. Pour plus d’informations, reportez-vous à la rubrique relative à l’[implémentation de la synchronisation de hachage de mot de passe avec la synchronisation d’Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p103">**Password Hash Sync (PHS)** [Recommended and required for some premium features]. This is the simplest way to enable authentication for on-premises directory objects in Azure AD. Azure AD Connect extracts the hashed password from Windows Server AD, does extra security processing on the password, and saves it in Azure AD. For more information, see [Implement password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-synchronization).</span></span>
    - <span data-ttu-id="ff6e9-p104">L’**authentification directe** fournit une solution de validation de mot de passe simple pour les services basés sur Azure AD. L’authentification directe utilise un agent exécuté sur un ou plusieurs serveurs locaux pour valider les authentifications utilisateur directement avec votre version locale de Windows Server AD. Pour plus d’informations, reportez-vous à la rubrique relative à la [connexion utilisateur avec l’authentification directe Azure Active Directory](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p104">**Pass-through Authentication (PTA)** provides a simple password validation solution for Azure AD-based services. PTA uses an agent running on one or more on-premises servers to validate the user authentications directly with your on-premises Windows Server AD. For more information, see [User sign-in with Azure Active Directory Pass-through Authentication](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication).</span></span>
- <span data-ttu-id="ff6e9-p105">Avec l’**authentification fédérée**, le processus d’authentification est redirigé vers un autre fournisseur d’identité via un serveur de fédération des identités, tels que les services de fédération Active Directory (AD FS), pour la connexion d’un utilisateur. Le fournisseur d’identité peut fournir des méthodes d’authentification supplémentaires, telles que l’authentification par carte à puce. Pour en savoir plus, reportez-vous à l’article [Choisir la méthode d’authentification adaptée à votre solution d’identité hybride Azure Active Directory](https://docs.microsoft.com/azure/security/azure-ad-choose-authn).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p105">With **federated authentication**, the authentication process is redirected to another identity provider through an identity federation server, such as Active Directory Federation Services (AD FS), for a user’s sign-in. The identity provider can provide additional authentication methods, such as smartcard-based authentication. For more information, see [Choosing the right authentication method for your Azure Active Directory hybrid identity solution](https://docs.microsoft.com/azure/security/azure-ad-choose-authn).</span></span>

<span data-ttu-id="ff6e9-123">Une fois que vous avez déterminé votre solution d’identité hybride, téléchargez et exécutez l’[outil de correction d’erreurs de synchronisation d’annuaires IdFix](https://www.microsoft.com/download/details.aspx?id=36832) pour analyser votre Windows Server AD et les problèmes.</span><span class="sxs-lookup"><span data-stu-id="ff6e9-123">After you've determined your hybrid identity solution, download and run the [IdFix Directory Synchronization Error Remediation Tool](https://www.microsoft.com/download/details.aspx?id=36832) to analyze your Windows Server AD for issues.</span></span>

<span data-ttu-id="ff6e9-p106">Une fois que tous les problèmes identifiés sont résolus par l’outil IdFix, consultez l’article [Implémenter la synchronisation de hachage de mot de passe avec la synchronisation Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-hash-synchronization) pour savoir comment installer l’outil Azure AD Connect et configurer la synchronisation d’annuaires entre votre version locale de Windows Server AD et le client Azure AD pour vos abonnements Office 365 et EMS. Une fois que la synchronisation démarre, conservez vos groupes et comptes d’utilisateur avec votre fournisseur d’identité local, par exemple, Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="ff6e9-p106">After resolving all of the issues identified by the IdFix tool, see [Implement password hash synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-implement-password-hash-synchronization) for guidance on installing the Azure AD Connect tool and configuring directory synchronization between your on-premises Windows Server AD and the Azure AD tenant for your Office 365 and EMS subscriptions. After synchronization starts, you'll maintain your user accounts and groups with your on-premises identity provider, such as Windows Server AD.</span></span>

<span data-ttu-id="ff6e9-126">Microsoft fournit un ensemble de recommandations sur l’[accès aux appareils et à l’identité](microsoft-365-policies-configurations.md) pour garantir un personnel conforme et productif.</span><span class="sxs-lookup"><span data-stu-id="ff6e9-126">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce.</span></span> 
- <span data-ttu-id="ff6e9-127">Concernant la configuration recommandée pour les environnements hybrides, consultez la colonne **Active Directory avec la synchronisation de hachage de mot de passe** de la section [Travail préparatoire](identity-access-prerequisites.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-127">For recommended requirements for hybrid environments, see the **Active Directory with password hash sync** column in [prerequisites](identity-access-prerequisites.md#prerequisites).</span></span> 

- <span data-ttu-id="ff6e9-128">Pour la configuration recommandée pour les environnements cloud uniquement, reportez-vous à la colonne **Cloud uniquement** de la section [Travail préparatoire](identity-access-prerequisites.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ff6e9-128">For recommended requirements for cloud only environments, see the **Cloud only** column in [prerequisites](identity-access-prerequisites.md#prerequisites).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="ff6e9-130">Guide de laboratoire de test : Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="ff6e9-130">Test Lab Guide: Password hash synchronization</span></span>](password-hash-sync-m365-ent-test-environment.md)<br> [<span data-ttu-id="ff6e9-131">Guide de laboratoire de test : Authentification directe</span><span class="sxs-lookup"><span data-stu-id="ff6e9-131">Test Lab Guide: Pass-through authentication</span></span>](pass-through-auth-m365-ent-test-environment.md) |
|||

<span data-ttu-id="ff6e9-132">Comme point de contrôle intermédiaire, consultez les [critères de sortie](identity-exit-criteria.md#crit-identity-sync) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="ff6e9-132">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sync) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="ff6e9-133">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ff6e9-133">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step8.png)| [<span data-ttu-id="ff6e9-134">Surveiller l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="ff6e9-134">Monitor synchronization health</span></span>](identity-azure-ad-connect-health.md) |

