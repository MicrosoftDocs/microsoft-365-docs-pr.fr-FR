---
title: 'Étape 8 : surveiller l’état de la synchronisation'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Comprenez et configurez Azure AD Connect Health.
ms.openlocfilehash: 21cfd88617bccab3f0a2bdb51c0d320cd4568a56
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867261"
---
# <a name="step-8-monitor-synchronization-health"></a><span data-ttu-id="d9682-103">Étape 8 : surveiller l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="d9682-103">Step 8: Monitor synchronization health</span></span>

<span data-ttu-id="d9682-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="d9682-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="d9682-p101">Dans cette étape, vous allez installer un agent Azure AD Connect Health sur chacun de vos serveurs d’identité locaux pour surveiller votre infrastructure d’identités et les services de synchronisation fournis par Azure AD Connect. Les informations de surveillance sont mises à disposition dans un portail Azure AD Connect Health où vous pouvez afficher des alertes, l’analyseur de performances, l’analyse de l’utilisation et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="d9682-p101">In Step 4, you'll install an Azure AD Connect Health agent on each of your on-premises identity servers to monitor your identity infrastructure and the synchronization services provided by Azure AD Connect. The monitoring information is made available in an Azure AD Connect Health portal, where you can view alerts, performance monitoring, usage analytics, and other information.</span></span>

![Composants d’Azure AD Connect Health](./media/identity-azure-ad-connect-health/identity-azure-ad-connect-health.png)

<span data-ttu-id="d9682-108">La décision de conception clé concernant l’utilisation d’Azure AD Connect Health est basée sur la manière dont vous utilisez Azure AD Connect :</span><span class="sxs-lookup"><span data-stu-id="d9682-108">The key design decision of how to use Azure AD Connect Health is based on how you are using Azure AD Connect:</span></span>

- <span data-ttu-id="d9682-109">Si vous utilisez de nouveau l’option d’**authentification gérée**, commencez avec la rubrique relative à l’[utilisation d’Azure AD Connect Health avec la synchronisation](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="d9682-109">If you’re using the **managed authentication** option, start with [Using Azure AD Connect Health with sync](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync) to understand and configure Azure AD Connect Health.</span></span>
- <span data-ttu-id="d9682-110">Si vous synchronisez uniquement les noms des comptes et des groupes à l’aide de l’**authentification fédérée** avec Active Directory Federation Services (AD FS), commencez avec la rubrique [Utilisation d’Azure AD Connect Health avec AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) pour comprendre et configurer Azure AD Connect Health.</span><span class="sxs-lookup"><span data-stu-id="d9682-110">If you're synchronizing just the names of the accounts and groups using **federated authentication** with Active Directory Federation Services (AD FS), start with [Using Azure AD Connect Health with AD FS](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-adfs) to understand and configure Azure AD Connect Health.</span></span>

<span data-ttu-id="d9682-111">Lorsque vous terminez cette étape, vous avez :</span><span class="sxs-lookup"><span data-stu-id="d9682-111">When you complete this step, you’ll have:</span></span>

- <span data-ttu-id="d9682-112">l’agent Azure AD Connect Health installé sur vos serveurs de fournisseur d’identité local ;</span><span class="sxs-lookup"><span data-stu-id="d9682-112">The Azure AD Connect Health agent installed on your on-premises identity provider servers.</span></span>
- <span data-ttu-id="d9682-113">le portail Azure AD Connect Health qui affiche l’état actuel de vos activités d’infrastructure et de synchronisation locales avec le client Azure AD pour vos abonnements Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="d9682-113">The Azure AD Connect Health portal displaying the current state of your on-premises infrastructure and synchronization activities with the Azure AD tenant for your Office 365 and EMS subscriptions.</span></span>

<span data-ttu-id="d9682-114">Comme point de vérification intermédiaire, vous pouvez consultez les [critères de sortie](identity-exit-criteria.md#crit-identity-sync-health) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="d9682-114">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-sync-health) for this step.</span></span>


## <a name="next-step"></a><span data-ttu-id="d9682-115">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d9682-115">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step9.png)| [<span data-ttu-id="d9682-116">Simplifiez les mises à jour du mot de passe</span><span class="sxs-lookup"><span data-stu-id="d9682-116">Simplify password updates</span></span>](identity-password-writeback.md) |

