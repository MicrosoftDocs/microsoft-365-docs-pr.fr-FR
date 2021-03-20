---
title: Synchroniser les utilisateurs de domaine avec Microsoft 365
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
description: Synchronisez les utilisateurs contrôlés par un domaine avec Microsoft 365 pour les entreprises.
ms.openlocfilehash: 1c939dec7229f02991b15f08c48f184efecaddb0
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50913251"
---
# <a name="synchronize-domain-users-to-microsoft-365"></a><span data-ttu-id="8fa0f-103">Synchroniser les utilisateurs de domaine avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8fa0f-103">Synchronize domain users to Microsoft 365</span></span>

## <a name="1-prepare-for-directory-synchronization"></a><span data-ttu-id="8fa0f-104">1. Préparer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="8fa0f-104">1. Prepare for Directory Synchronization</span></span> 

<span data-ttu-id="8fa0f-105">Avant de synchroniser vos utilisateurs et ordinateurs à partir du domaine Active Directory local, voir Préparer la synchronisation d’annuaires [avec Microsoft 365.](../enterprise/prepare-for-directory-synchronization.md)</span><span class="sxs-lookup"><span data-stu-id="8fa0f-105">Before you synchronize your users and computers from the local Active Directory Domain, review [Prepare for directory synchronization to Microsoft 365](../enterprise/prepare-for-directory-synchronization.md).</span></span> <span data-ttu-id="8fa0f-106">En particulier :</span><span class="sxs-lookup"><span data-stu-id="8fa0f-106">In particular:</span></span>

   - <span data-ttu-id="8fa0f-107">Assurez-vous qu’il n’existe aucun doublon dans votre répertoire pour les attributs suivants : **mail,** **proxyAddresses** et **userPrincipalName**.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-107">Make sure that no duplicates exist in your directory for the following attributes: **mail**, **proxyAddresses**, and **userPrincipalName**.</span></span> <span data-ttu-id="8fa0f-108">Ces valeurs doivent être uniques et les doublons doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-108">These values must be unique and any duplicates must be removed.</span></span>
   
   - <span data-ttu-id="8fa0f-109">Nous vous recommandons de configurer l’attribut **userPrincipalName** (UPN) pour chaque compte d’utilisateur local afin qu’il corresponde à l’adresse de messagerie principale correspondant à l’utilisateur Sous licence Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-109">We recommend that you configure the **userPrincipalName** (UPN) attribute for each local user account to match the primary email address that corresponds to the licensed Microsoft 365 user.</span></span> <span data-ttu-id="8fa0f-110">Par exemple : *mary.shelley@contoso.com* au lieu *de mary@contoso.local*</span><span class="sxs-lookup"><span data-stu-id="8fa0f-110">For example: *mary.shelley@contoso.com* rather than *mary@contoso.local*</span></span>
   
   - <span data-ttu-id="8fa0f-111">Si le domaine Active Directory se termine par un suffixe non routable tel que *.local* ou *.lan,* au lieu d’un suffixe routable Internet tel *que .com* ou *.org,* ajustez d’abord le suffixe UPN des comptes d’utilisateurs locaux, comme décrit dans Préparer un domaine [non routable](../enterprise/prepare-a-non-routable-domain-for-directory-synchronization.md)pour la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-111">If the Active Directory domain ends in a non-routable suffix like *.local* or *.lan*, instead of an internet routable suffix such as *.com* or *.org*, adjust the UPN suffix of the local user accounts first as described in [Prepare a non-routable domain for directory synchronization](../enterprise/prepare-a-non-routable-domain-for-directory-synchronization.md).</span></span> 

<span data-ttu-id="8fa0f-112">**L’IdFix** d’exécuter à l’étape quatre (4) ci-dessous permet également de s’assurer que votre annuaire Active Directory local est prêt pour la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-112">The **Run IdFix** in step four (4) below, will also make sure your on-premises Active Directory is ready for directory synchronization.</span></span>

## <a name="2-install-and-configure-azure-ad-connect"></a><span data-ttu-id="8fa0f-113">2. Installer et configurer Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="8fa0f-113">2. Install and configure Azure AD Connect</span></span>

<span data-ttu-id="8fa0f-114">Pour synchroniser vos utilisateurs, groupes et contacts à partir d’Active Directory local dans Azure Active Directory, installez Azure Active Directory Connect et installez la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-114">To synchronize your users, groups, and contacts from the local Active Directory into Azure Active Directory, install Azure Active Directory Connect and set up directory synchronization.</span></span> 

 1. <span data-ttu-id="8fa0f-115">Dans le centre [d’administration,](https://go.microsoft.com/fwlink/p/?linkid=2024339)sélectionnez **Le programme d’installation** dans le navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-115">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), select **Setup** in the left nav.</span></span>

 2. <span data-ttu-id="8fa0f-116">Under **Sign-in and security**, choose **View**  under Sync users from **your org’s directory**.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-116">Under **Sign-in and security**, choose **View**  under **Sync users from your org's directory**.</span></span>

 3. <span data-ttu-id="8fa0f-117">On the **Sync users from your org’s directory** page, choose Get **started**.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-117">On the **Sync users from your org's directory** page, choose **Get started**.</span></span>

 4. <span data-ttu-id="8fa0f-118">Lors de la première étape, exécutez l’outil IdFix pour préparer la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-118">In the first step  run IdFix tool to prepare for Directory sync.</span></span>

 5. <span data-ttu-id="8fa0f-119">Suivez les étapes de l’Assistant pour télécharger Azure AD Connect et l’utiliser pour synchroniser vos utilisateurs contrôlés par un domaine avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-119">Follow the wizard steps to download Azure AD Connect and use it to synchronize your domain-controlled users to Microsoft 365.</span></span>


<span data-ttu-id="8fa0f-120">Pour plus d’informations, voir Configurer la synchronisation d’annuaires [pour Microsoft 365.](../enterprise/set-up-directory-synchronization.md)</span><span class="sxs-lookup"><span data-stu-id="8fa0f-120">See [Set up directory synchronization for Microsoft 365](../enterprise/set-up-directory-synchronization.md) to learn more.</span></span>

<span data-ttu-id="8fa0f-121">Lorsque vous configurez vos options pour Azure AD Connect, nous vous recommandons d’activer la synchronisation de mot de **passe,** l’personnalisation transparente et la fonctionnalité d’écriture automatique de mot de passe, qui est également prise en charge dans Microsoft 365 pour les entreprises. </span><span class="sxs-lookup"><span data-stu-id="8fa0f-121">As you configure your options for Azure AD Connect, we recommend that you enable **Password Synchronization**, **Seamless Single Sign-On**, and the **password writeback** feature, which is also supported in Microsoft 365 for business.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa0f-122">Il existe quelques étapes supplémentaires pour l’écriture de mot de passe au-delà de la case à cocher dans Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-122">There are some additional steps for password writeback beyond the check box in Azure AD Connect.</span></span> <span data-ttu-id="8fa0f-123">Pour plus d’informations, [voir How-to: configure password writeback](/azure/active-directory/authentication/howto-sspr-writeback).</span><span class="sxs-lookup"><span data-stu-id="8fa0f-123">For more information, see [How-to: configure password writeback](/azure/active-directory/authentication/howto-sspr-writeback).</span></span> 

<span data-ttu-id="8fa0f-124">Si vous souhaitez également gérer les appareils Windows 10 joints à un domaine, voir Activer les appareils Windows 10 joints à un domaine à gérer par [Microsoft 365 Business Premium](manage-windows-devices.md) pour configurer une jointation Azure AD hybride.</span><span class="sxs-lookup"><span data-stu-id="8fa0f-124">If you also want to manage domain-joined Windows 10 devices, see [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium](manage-windows-devices.md) to set up a hybrid Azure AD Join.</span></span>