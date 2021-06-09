---
title: Synchroniser les utilisateurs de domaine avec Microsoft 365
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
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
description: Synchronisez les utilisateurs contrôlés par domaine avec Microsoft 365 entreprise.
ms.openlocfilehash: b477b8a1f35a790d6c49937c973c141ad9f90ad4
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578404"
---
# <a name="synchronize-domain-users-to-microsoft-365"></a><span data-ttu-id="739df-103">Synchroniser les utilisateurs de domaine avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="739df-103">Synchronize domain users to Microsoft 365</span></span>

## <a name="1-prepare-for-directory-synchronization"></a><span data-ttu-id="739df-104">1. Préparer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="739df-104">1. Prepare for Directory Synchronization</span></span> 

<span data-ttu-id="739df-105">Avant de synchroniser vos utilisateurs et ordinateurs à partir du domaine Active Directory local, examinez Préparer la synchronisation d’annuaires [Microsoft 365](../enterprise/prepare-for-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="739df-105">Before you synchronize your users and computers from the local Active Directory Domain, review [Prepare for directory synchronization to Microsoft 365](../enterprise/prepare-for-directory-synchronization.md).</span></span> <span data-ttu-id="739df-106">En particulier :</span><span class="sxs-lookup"><span data-stu-id="739df-106">In particular:</span></span>

   - <span data-ttu-id="739df-107">Assurez-vous qu’il n’existe aucun doublon dans votre répertoire pour les attributs suivants : **mail,** **proxyAddresses** et **userPrincipalName**.</span><span class="sxs-lookup"><span data-stu-id="739df-107">Make sure that no duplicates exist in your directory for the following attributes: **mail**, **proxyAddresses**, and **userPrincipalName**.</span></span> <span data-ttu-id="739df-108">Ces valeurs doivent être uniques et les doublons doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="739df-108">These values must be unique and any duplicates must be removed.</span></span>
   
   - <span data-ttu-id="739df-109">Nous vous recommandons de configurer l’attribut **userPrincipalName** (UPN) pour chaque compte d’utilisateur local afin qu’il corresponde à l’adresse de messagerie principale correspondant à l’utilisateur Microsoft 365 sous licence.</span><span class="sxs-lookup"><span data-stu-id="739df-109">We recommend that you configure the **userPrincipalName** (UPN) attribute for each local user account to match the primary email address that corresponds to the licensed Microsoft 365 user.</span></span> <span data-ttu-id="739df-110">Par exemple : *mary.shelley@contoso.com* au lieu *de mary@contoso.local*</span><span class="sxs-lookup"><span data-stu-id="739df-110">For example: *mary.shelley@contoso.com* rather than *mary@contoso.local*</span></span>
   
   - <span data-ttu-id="739df-111">Si le domaine Active Directory se termine par un suffixe non routable tel que *.local* ou *.lan,* au lieu d’un suffixe routable Internet tel *que .com* ou *.org,* ajustez d’abord le suffixe UPN des comptes d’utilisateurs locaux, comme décrit dans Préparer un domaine [non routable](../enterprise/prepare-a-non-routable-domain-for-directory-synchronization.md)pour la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="739df-111">If the Active Directory domain ends in a non-routable suffix like *.local* or *.lan*, instead of an internet routable suffix such as *.com* or *.org*, adjust the UPN suffix of the local user accounts first as described in [Prepare a non-routable domain for directory synchronization](../enterprise/prepare-a-non-routable-domain-for-directory-synchronization.md).</span></span> 

<span data-ttu-id="739df-112">**L’IdFix** d’exécuter à l’étape quatre (4) ci-dessous permet également de s’assurer que votre annuaire Active Directory local est prêt pour la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="739df-112">The **Run IdFix** in step four (4) below, will also make sure your on-premises Active Directory is ready for directory synchronization.</span></span>

## <a name="2-install-and-configure-azure-ad-connect"></a><span data-ttu-id="739df-113">2. Installer et configurer Azure AD Connecter</span><span class="sxs-lookup"><span data-stu-id="739df-113">2. Install and configure Azure AD Connect</span></span>

<span data-ttu-id="739df-114">Pour synchroniser vos utilisateurs, groupes et contacts à partir d’Active Directory local dans Azure Active Directory, installez Azure Active Directory Connecter et configurer la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="739df-114">To synchronize your users, groups, and contacts from the local Active Directory into Azure Active Directory, install Azure Active Directory Connect and set up directory synchronization.</span></span> 

 1. <span data-ttu-id="739df-115">Dans le centre [d’administration,](https://go.microsoft.com/fwlink/p/?linkid=2024339)sélectionnez **Le programme d’installation** dans le navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="739df-115">In the [admin center](https://go.microsoft.com/fwlink/p/?linkid=2024339), select **Setup** in the left nav.</span></span>

 2. <span data-ttu-id="739df-116">Under **Sign-in and security**, choose **View**  under Sync users from **your org’s directory**.</span><span class="sxs-lookup"><span data-stu-id="739df-116">Under **Sign-in and security**, choose **View**  under **Sync users from your org's directory**.</span></span>

 3. <span data-ttu-id="739df-117">On the **Sync users from your org’s directory** page, choose Get **started**.</span><span class="sxs-lookup"><span data-stu-id="739df-117">On the **Sync users from your org's directory** page, choose **Get started**.</span></span>

 4. <span data-ttu-id="739df-118">Lors de la première étape, exécutez l’outil IdFix pour préparer la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="739df-118">In the first step  run IdFix tool to prepare for Directory sync.</span></span>

 5. <span data-ttu-id="739df-119">Suivez les étapes de l’Assistant pour télécharger Azure AD Connecter et l’utiliser pour synchroniser vos utilisateurs contrôlés par un domaine avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="739df-119">Follow the wizard steps to download Azure AD Connect and use it to synchronize your domain-controlled users to Microsoft 365.</span></span>


<span data-ttu-id="739df-120">Voir [Configurer la synchronisation d’annuaires pour Microsoft 365](../enterprise/set-up-directory-synchronization.md) pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="739df-120">See [Set up directory synchronization for Microsoft 365](../enterprise/set-up-directory-synchronization.md) to learn more.</span></span>

<span data-ttu-id="739df-121">Lorsque vous configurez vos options pour Azure AD Connecter, nous vous recommandons d’activer la  synchronisation de mot de **passe,** l' **sign-on** unique transparente et la fonctionnalité d’écriture/écriture de mot de passe, qui est également prise en charge dans Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="739df-121">As you configure your options for Azure AD Connect, we recommend that you enable **Password Synchronization**, **Seamless Single Sign-On**, and the **password writeback** feature, which is also supported in Microsoft 365 for business.</span></span>

> [!NOTE]
> <span data-ttu-id="739df-122">Il existe quelques étapes supplémentaires pour l’écriture de mot de passe au-delà de la case à cocher dans Azure AD Connecter.</span><span class="sxs-lookup"><span data-stu-id="739df-122">There are some additional steps for password writeback beyond the check box in Azure AD Connect.</span></span> <span data-ttu-id="739df-123">Pour plus d’informations, [voir How-to: configure password writeback](/azure/active-directory/authentication/howto-sspr-writeback).</span><span class="sxs-lookup"><span data-stu-id="739df-123">For more information, see [How-to: configure password writeback](/azure/active-directory/authentication/howto-sspr-writeback).</span></span> 

<span data-ttu-id="739df-124">Si vous souhaitez également gérer les appareils Windows 10 joints à un domaine, voir Activer les appareils Windows 10 joints à un domaine à gérer par [Microsoft 365 Business Premium](manage-windows-devices.md) pour configurer une jointation Azure AD hybride.</span><span class="sxs-lookup"><span data-stu-id="739df-124">If you also want to manage domain-joined Windows 10 devices, see [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium](manage-windows-devices.md) to set up a hybrid Azure AD Join.</span></span>