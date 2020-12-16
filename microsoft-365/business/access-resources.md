---
title: Accéder aux ressources locales à partir d’un appareil joint à Azure AD dans Microsoft 365 Business
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
ms.collection: M365-subscription-management
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: b0f4d010-9fd1-44d0-9d20-fabad2cdbab5
description: Découvrez comment accéder à des ressources locales telles que des applications métier, des partages de fichiers et des imprimantes à partir d’un appareil Azure Active Directory joint à Windows 10.
ms.openlocfilehash: 22edf0c23d6318e1f70bcb21b2cd697ea0a75da4
ms.sourcegitcommit: 849b365bd3eaa9f3c3a9ef9f5973ef81af9156fa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49688230"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a><span data-ttu-id="f8b1e-103">Accéder aux ressources locales à partir d’un appareil joint à Azure AD dans Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="f8b1e-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium</span></span>

<span data-ttu-id="f8b1e-104">Cet article s’applique à Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="f8b1e-105">Tout appareil Windows 10 qui est joint à Azure Active Directory a accès à toutes les ressources en nuage, telles que vos applications Microsoft 365, et peut être protégé par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-105">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Microsoft 365 apps, and can be protected by Microsoft 365 Business Premium.</span></span> <span data-ttu-id="f8b1e-106">Vous pouvez également autoriser l’accès à des ressources locales telles que des applications métier, des partages de fichiers et des imprimantes.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-106">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="f8b1e-107">Pour autoriser l’accès, utilisez [Azure ad Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) pour synchroniser votre annuaire Active Directory local avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-107">To allow access, use [Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span> 

<span data-ttu-id="f8b1e-108">Pour en savoir plus, consultez la rubrique [Présentation de la gestion des appareils dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="f8b1e-108">To learn more, see [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="f8b1e-109">Les étapes sont également résumées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-109">The steps are also summarized in the following sections.</span></span>
 
## <a name="run-azure-ad-connect"></a><span data-ttu-id="f8b1e-110">Exécuter Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="f8b1e-110">Run Azure AD Connect</span></span>

<span data-ttu-id="f8b1e-111">Procédez comme suit pour activer les appareils Azure AD joints de votre organisation pour accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-111">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="f8b1e-112">Pour synchroniser vos utilisateurs, groupes et contacts à partir d’Active Directory local avec Azure Active Directory, exécutez l’Assistant synchronisation d’annuaires et Azure AD Connect comme décrit dans [set up Directory Synchronization for Office 365](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization).</span><span class="sxs-lookup"><span data-stu-id="f8b1e-112">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://docs.microsoft.com/microsoft-365/enterprise/set-up-directory-synchronization).</span></span>
    
2. <span data-ttu-id="f8b1e-113">Une fois la synchronisation d’annuaires terminée, assurez-vous que les appareils Windows 10 de votre organisation sont joints à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-113">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="f8b1e-114">Cette étape est effectuée individuellement sur chaque appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-114">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="f8b1e-115">Pour plus d’informations, reportez-vous à la rubrique [configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business Premium](set-up-windows-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="f8b1e-115">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="f8b1e-116">Une fois que les appareils Windows 10 sont joints à Azure AD, chaque utilisateur doit redémarrer ses appareils et se connecter à l’aide de leurs informations d’identification Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-116">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business Premium credentials.</span></span> <span data-ttu-id="f8b1e-117">Tous les périphériques ont désormais accès aux ressources locales également.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-117">All devices now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="f8b1e-118">Aucune étape supplémentaire n’est requise pour accéder aux ressources locales pour les appareils joints à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-118">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="f8b1e-119">Cette fonctionnalité est intégrée dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-119">This functionality is built into Windows 10.</span></span> 

<span data-ttu-id="f8b1e-120">Si vous avez l’intention de vous connecter à l’appareil AADJ autre que la méthode de mot de passe comme code confidentiel/bio-métrique via WHFB de connexion d’informations d’identification et d’accéder aux ressources locales (partages, imprimantes.. etc.), suivez https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span><span class="sxs-lookup"><span data-stu-id="f8b1e-120">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares,printers..etc), please follow https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base</span></span>
  
<span data-ttu-id="f8b1e-121">Si votre organisation n’est pas prête à être déployée dans la configuration d’appareil joint Azure AD décrite ci-dessus, envisagez de configurer la [configuration hybride Azure ad jointe](manage-windows-devices.md)de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-121">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="f8b1e-122">Éléments à prendre en compte lorsque vous associez des appareils Windows à Azure AD</span><span class="sxs-lookup"><span data-stu-id="f8b1e-122">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="f8b1e-123">Si le périphérique Windows auquel vous participez à Azure-AD a été précédemment joint à un domaine ou dans un groupe de travail, tenez compte des limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8b1e-123">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>
  
- <span data-ttu-id="f8b1e-124">Lorsqu’un appareil Azure AD rejoint une jointure, il crée un utilisateur sans référence à un profil existant.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-124">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="f8b1e-125">Les profils doivent être migrés manuellement.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-125">Profiles must be manually migrated.</span></span> <span data-ttu-id="f8b1e-126">Un profil utilisateur contient des informations comme les favoris, les fichiers locaux, les paramètres de navigateur et les paramètres du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-126">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="f8b1e-127">Une meilleure approche consiste à trouver un outil tiers pour mapper les fichiers et les paramètres existants sur le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-127">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="f8b1e-128">Si l’appareil utilise des objets de stratégie de groupe (GPO), certains objets de stratégie de groupe ne disposent pas nécessairement d’un [fournisseur de services de configuration](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) comparable dans Intune.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-128">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="f8b1e-129">Exécutez l' [outil mmat](https://www.microsoft.com/download/details.aspx?id=45520) pour rechercher des fournisseurs de services cryptographiques comparables pour les objets de stratégie de groupe existants.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-129">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="f8b1e-130">Les utilisateurs ne peuvent pas s’authentifier aux applications qui dépendent de l’authentification Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-130">Users won't be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="f8b1e-131">Évaluez l’application héritée et envisagez d’effectuer une mise à jour vers une application qui utilise l’authentification moderne, si possible.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-131">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="f8b1e-132">La découverte des imprimantes Active Directory ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="f8b1e-132">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="f8b1e-133">Vous pouvez fournir des chemins d’accès directs aux imprimantes pour tous les utilisateurs ou utiliser l' [impression universelle](https://aka.ms/UPDocs).</span><span class="sxs-lookup"><span data-stu-id="f8b1e-133">You can provide direct printer paths for all users or use [Universal Print](https://aka.ms/UPDocs).</span></span>
