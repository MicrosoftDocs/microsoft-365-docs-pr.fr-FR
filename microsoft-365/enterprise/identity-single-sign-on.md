---
title: 'Étape 10 : Simplifier la connexion de l’utilisateur'
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
description: Comprenez et configurez l’authentification unique transparente d’Azure AD.
ms.openlocfilehash: 9d18cb559d3a4a9ee401e0f94fb53bc6360d88c8
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867382"
---
# <a name="step-10-simplify-user-sign-in"></a><span data-ttu-id="283ae-103">Étape 10 : Simplifier la connexion de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="283ae-103">Step 10: Simplify user sign-in</span></span>

<span data-ttu-id="283ae-104">*Cette étape est facultative pour les environnements hybrides et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="283ae-104">*This step is optional for hybrid environments and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="283ae-p101">Dans cette étape, vous devrez configurer l’authentification unique transparente d’Azure Active Directory pour autoriser vos utilisateurs à se connecter aux services qui utilisent des comptes d’utilisateur Azure AD sans devoir taper ni leurs mots de passe, ni leurs noms d’utilisateur (dans de nombreux cas). Cela permet à vos utilisateurs d’accéder plus facilement aux applications informatiques comme Office 365, sans avoir besoin de composants locaux supplémentaires, tels que des serveurs de fédération des identités.</span><span class="sxs-lookup"><span data-stu-id="283ae-p101">In Step 8, you'll set up Azure Active Directory Seamless Single Sign-On (Azure AD Seamless SSO) to allow your users to sign in to services that use Azure AD user accounts without having to type in their passwords, and in many cases, their usernames. This gives your users easier access to cloud-based applications, such as Office 365, without needing any additional on-premises components such as identity federation servers.</span></span>

<span data-ttu-id="283ae-107">Vous allez configurer l’authentification unique transparente d’Azure AD avec l’outil Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="283ae-107">You'll configure Azure AD Seamless SSO with the Azure AD Connect tool.</span></span>

<span data-ttu-id="283ae-108">Reportez-vous aux [instructions pour configurer l’authentification unique transparente d’Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span><span class="sxs-lookup"><span data-stu-id="283ae-108">See the [instructions to configure Azure AD Seamless SSO](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start).</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="283ae-110">Guide de laboratoire de test : authentification unique transparente Azure AD</span><span class="sxs-lookup"><span data-stu-id="283ae-110">Test Lab Guide: Azure AD Seamless Single Sign-on</span></span>](single-sign-on-m365-ent-test-environment.md) |
|||

<span data-ttu-id="283ae-111">Comme point de vérification intermédiaire, vous pouvez consultez les [critères de sortie](identity-exit-criteria.md#crit-identity-sso) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="283ae-111">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sso) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="283ae-112">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="283ae-112">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step11.png)| [<span data-ttu-id="283ae-113">Personnaliser la page de connexion à Office 365</span><span class="sxs-lookup"><span data-stu-id="283ae-113">Customize the Office 365 sign-in page</span></span>](identity-customize-office-365-sign-in.md) |

