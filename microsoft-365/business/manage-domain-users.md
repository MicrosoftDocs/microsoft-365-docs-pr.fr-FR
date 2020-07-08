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
description: Synchroniser les utilisateurs contrôlés par le domaine avec Microsoft 365 pour les entreprises.
ms.openlocfilehash: af9cb7c9b2b639edc2375679a73ab41c4cf6de71
ms.sourcegitcommit: 5b769f74bcc76ac8d38aad815d1728824783cd9f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "45080058"
---
# <a name="synchronize-domain-users-to-microsoft-365"></a><span data-ttu-id="0b5af-103">Synchroniser les utilisateurs de domaine avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0b5af-103">Synchronize domain users to Microsoft 365</span></span>

## <a name="1-prepare-for-directory-synchronization"></a><span data-ttu-id="0b5af-104">1. préparer la synchronisation d’annuaires</span><span class="sxs-lookup"><span data-stu-id="0b5af-104">1. Prepare for Directory Synchronization</span></span> 

<span data-ttu-id="0b5af-105">Avant de synchroniser vos utilisateurs et ordinateurs à partir du domaine Active Directory local, consultez la [préparation de la synchronisation d’annuaires avec Microsoft 365](https://docs.microsoft.com/office365/enterprise/prepare-for-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="0b5af-105">Before you synchronize your users and computers from the local Active Directory Domain, review [Prepare for directory synchronization to Microsoft 365](https://docs.microsoft.com/office365/enterprise/prepare-for-directory-synchronization).</span></span> <span data-ttu-id="0b5af-106">En particulier :</span><span class="sxs-lookup"><span data-stu-id="0b5af-106">In particular:</span></span>

   - <span data-ttu-id="0b5af-107">Assurez-vous qu’il n’existe pas de doublons dans votre répertoire pour les attributs suivants : **mail**, **proxyAddresses**et **userPrincipalName**.</span><span class="sxs-lookup"><span data-stu-id="0b5af-107">Make sure that no duplicates exist in your directory for the following attributes: **mail**, **proxyAddresses**, and **userPrincipalName**.</span></span> <span data-ttu-id="0b5af-108">Ces valeurs doivent être uniques et les doublons doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="0b5af-108">These values must be unique and any duplicates must be removed.</span></span>
   
   - <span data-ttu-id="0b5af-109">Nous vous recommandons de configurer l’attribut **userPrincipalName** (UPN) de chaque compte d’utilisateur local de sorte qu’il corresponde à l’adresse de messagerie principale correspondant à l’utilisateur Microsoft 365 sous licence.</span><span class="sxs-lookup"><span data-stu-id="0b5af-109">We recommend that you configure the **userPrincipalName** (UPN) attribute for each local user account to match the primary email address that corresponds to the licensed Microsoft 365 user.</span></span> <span data-ttu-id="0b5af-110">Par exemple : *Mary.Shelley@contoso.com* plutôt que *Mary@contoso. local*</span><span class="sxs-lookup"><span data-stu-id="0b5af-110">For example: *mary.shelley@contoso.com* rather than *mary@contoso.local*</span></span>
   
   - <span data-ttu-id="0b5af-111">Si le domaine Active Directory se termine par un suffixe non routable comme *. local* ou *. LAN*, au lieu d’un suffixe routable Internet tel que *. com* ou *. org*, ajustez d’abord le suffixe UPN des comptes d’utilisateurs locaux comme décrit dans [Prepare a non routable domain for Directory Synchronization](https://docs.microsoft.com/office365/enterprise/prepare-a-non-routable-domain-for-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="0b5af-111">If the Active Directory domain ends in a non-routable suffix like *.local* or *.lan*, instead of an internet routable suffix such as *.com* or *.org*, adjust the UPN suffix of the local user accounts first as described in [Prepare a non-routable domain for directory synchronization](https://docs.microsoft.com/office365/enterprise/prepare-a-non-routable-domain-for-directory-synchronization).</span></span> 

<span data-ttu-id="0b5af-112">Le **IdFix exécuter** à l’étape quatre (4) ci-dessous permet de s’assurer que votre annuaire Active Directory local est prêt pour la synchronisation de répertoires.</span><span class="sxs-lookup"><span data-stu-id="0b5af-112">The **Run IdFix** in step four (4) below, will also make sure your on-premises Active Directory is ready for dir sync.</span></span>

## <a name="2-install-and-configure-azure-ad-connect"></a><span data-ttu-id="0b5af-113">2. installer et configurer Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="0b5af-113">2. Install and configure Azure AD Connect</span></span>

<span data-ttu-id="0b5af-114">Pour synchroniser vos utilisateurs, groupes et contacts à partir de l’Active Directory local avec Azure Active Directory, installez Azure Active Directory Connect et configurez la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="0b5af-114">To synchronize your users, groups, and contacts from the local Active Directory into Azure Active Directory, install Azure Active Directory Connect and set up directory synchronization.</span></span> 

 1. <span data-ttu-id="0b5af-115">Dans le centre d’administration, <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> sélectionnez **configuration** dans le service de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="0b5af-115">In the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=2024339" target="_blank">https://admin.microsoft.com</a> select **Setup** in the left nav.</span></span>

 2. <span data-ttu-id="0b5af-116">Sous **connexion et sécurité**, choisissez **affichage** sous **synchroniser les utilisateurs dans le répertoire de votre organisation**.</span><span class="sxs-lookup"><span data-stu-id="0b5af-116">Under **Sign-in and security**, choose **View**  under **Sync users from your org's directory**.</span></span>

 3. <span data-ttu-id="0b5af-117">Sur la page **synchroniser les utilisateurs à partir de l’annuaire de votre organisation** , sélectionnez **prise en main**.</span><span class="sxs-lookup"><span data-stu-id="0b5af-117">On the **Sync users from your org's directory** page, choose **Get started**.</span></span>

 4. <span data-ttu-id="0b5af-118">Dans la première étape, exécutez l’outil IdFix pour préparer la synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="0b5af-118">In the first step  run IdFix tool to prepare for Directory sync.</span></span>

 5. <span data-ttu-id="0b5af-119">Suivez les étapes de l’Assistant pour télécharger Azure AD Connect et utilisez-le pour synchroniser vos utilisateurs sous contrôle de domaine avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0b5af-119">Follow the wizard steps to download Azure AD Connect and use it to synchronize your domain-controlled users to Microsoft 365.</span></span>


<span data-ttu-id="0b5af-120">Pour plus d’informations, reportez-vous à la rubrique [configurer la synchronisation d’annuaires pour Microsoft 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) .</span><span class="sxs-lookup"><span data-stu-id="0b5af-120">See [Set up directory synchronization for Microsoft 365](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) to learn more.</span></span>

<span data-ttu-id="0b5af-121">Lorsque vous configurez vos options pour Azure AD Connect, nous vous recommandons d’activer la **synchronisation de mot de passe**, l' **authentification unique transparente**et la fonctionnalité d' **écriture différée de mot de passe** , qui est également prise en charge dans Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="0b5af-121">As you configure your options for Azure AD Connect, we recommend that you enable **Password Synchronization**, **Seamless Single Sign-On**, and the **password writeback** feature, which is also supported in Microsoft 365 for business.</span></span>

> [!NOTE]
> <span data-ttu-id="0b5af-122">Il existe quelques étapes supplémentaires pour l’écriture différée de mot de passe au-delà de la case à cocher dans Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="0b5af-122">There are some additional steps for password writeback beyond the check box in Azure AD Connect.</span></span> <span data-ttu-id="0b5af-123">Pour plus d’informations, voir [procédure : configurer l’écriture différée de mot de passe](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-writeback).</span><span class="sxs-lookup"><span data-stu-id="0b5af-123">For more information, see [How-to: configure password writeback](https://docs.microsoft.com/azure/active-directory/authentication/howto-sspr-writeback).</span></span> 

<span data-ttu-id="0b5af-124">Si vous voulez également gérer les appareils Windows 10 associés à un domaine, consultez la rubrique [Enable Domain-Joining Domain 10 Devices to be Managed Microsoft 365 Business Premium](manage-windows-devices.md) pour configurer une participation hybride Azure ad.</span><span class="sxs-lookup"><span data-stu-id="0b5af-124">If you want to manage domain-joined Windows 10 devices also, see [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium](manage-windows-devices.md) to set up a hybrid Azure AD Join.</span></span> 