---
title: Accéder aux ressources sur site à partir d’un appareil joint à Azure AD dans Microsoft 365 Business
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
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
description: Découvrez comment accéder à des ressources locales telles que des applications métier, des partages de fichiers et des imprimantes à partir d’un Azure Active Directory joint Windows 10 appareil.
ms.openlocfilehash: 72b3c5ae538cad24fc12e25717dedccb2fdc9017
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843319"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business-premium"></a><span data-ttu-id="4ce52-103">Accéder aux ressources sur site à partir d’un appareil joint à Azure AD dans Microsoft 365 Business Premium</span><span class="sxs-lookup"><span data-stu-id="4ce52-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium</span></span>

<span data-ttu-id="4ce52-104">Cet article s’applique aux Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="4ce52-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="4ce52-105">Tout appareil Windows 10 joint Azure Active Directory a accès à toutes les ressources basées sur le cloud, telles que vos applications Microsoft 365, et peut être protégé par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="4ce52-105">Any Windows 10 device that is Azure Active Directory joined has access to all cloud-based resources, such as your Microsoft 365 apps, and can be protected by Microsoft 365 Business Premium.</span></span> <span data-ttu-id="4ce52-106">Vous pouvez également autoriser l’accès à des ressources locales telles que des applications métier, des partages de fichiers et des imprimantes.</span><span class="sxs-lookup"><span data-stu-id="4ce52-106">You can also allow access to on-premises resources like line of business (LOB) apps, file shares, and printers.</span></span> <span data-ttu-id="4ce52-107">Pour autoriser l’accès, utilisez [Azure AD Connecter](/azure/active-directory/connect/active-directory-aadconnect) pour synchroniser votre annuaire Active Directory local avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4ce52-107">To allow access, use [Azure AD Connect](/azure/active-directory/connect/active-directory-aadconnect) to synchronize your on-premises Active Directory with Azure Active Directory.</span></span>

<span data-ttu-id="4ce52-108">Pour plus d’informations, voir [Introduction à la gestion des appareils dans Azure Active Directory](/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="4ce52-108">To learn more, see [Introduction to device management in Azure Active Directory](/azure/active-directory/device-management-introduction).</span></span>
<span data-ttu-id="4ce52-109">Les étapes sont également résumées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ce52-109">The steps are also summarized in the following sections.</span></span>

## <a name="run-azure-ad-connect"></a><span data-ttu-id="4ce52-110">Exécuter Azure AD Connecter</span><span class="sxs-lookup"><span data-stu-id="4ce52-110">Run Azure AD Connect</span></span>

<span data-ttu-id="4ce52-111">Pour permettre aux appareils joints à Azure AD de votre organisation d’accéder aux ressources sur site, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="4ce52-111">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>

1. <span data-ttu-id="4ce52-112">Pour synchroniser vos utilisateurs, groupes et contacts d’Active Directory local dans Azure Active Directory, exécutez l’Assistant Synchronisation d’annuaires et Azure AD Connecter comme décrit dans Configurer la synchronisation d’annuaires [pour Office 365](../enterprise/set-up-directory-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="4ce52-112">To synchronize your users, groups, and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](../enterprise/set-up-directory-synchronization.md).</span></span>

2. <span data-ttu-id="4ce52-113">Une fois la synchronisation d’annuaires terminée, assurez-vous que les appareils de votre Windows 10 sont joints à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4ce52-113">After the directory synchronization is complete, make sure your organization's Windows 10 devices are Azure AD joined.</span></span> <span data-ttu-id="4ce52-114">Cette étape est effectuée individuellement sur chaque Windows 10'appareil.</span><span class="sxs-lookup"><span data-stu-id="4ce52-114">This step is done individually on each Windows 10 device.</span></span> <span data-ttu-id="4ce52-115">Pour [plus d’informations, Windows configurer des Microsoft 365 Business Premium utilisateurs.](set-up-windows-devices.md)</span><span class="sxs-lookup"><span data-stu-id="4ce52-115">See [Set up Windows devices for Microsoft 365 Business Premium users](set-up-windows-devices.md) for details.</span></span>

3. <span data-ttu-id="4ce52-116">Une fois que les Windows 10 sont joints à Azure AD, chaque utilisateur doit redémarrer ses appareils et se Microsoft 365 Business Premium leurs informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="4ce52-116">Once the Windows 10 devices are Azure AD joined, each user must reboot their devices and sign in with their Microsoft 365 Business Premium credentials.</span></span> <span data-ttu-id="4ce52-117">Tous les appareils ont désormais également accès aux ressources sur site.</span><span class="sxs-lookup"><span data-stu-id="4ce52-117">All devices now have access to on-premises resources as well.</span></span>

<span data-ttu-id="4ce52-118">Aucune étape supplémentaire n’est requise pour accéder aux ressources sur site pour les appareils joints à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="4ce52-118">No additional steps are required to get access to on-premises resources for Azure AD joined devices.</span></span> <span data-ttu-id="4ce52-119">Cette fonctionnalité est intégrée à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4ce52-119">This functionality is built into Windows 10.</span></span>

<span data-ttu-id="4ce52-120">Si vous avez l’intention de vous connecter à l’appareil AADJ autre que la méthode de mot de passe comme le code confidentiel/la mesure Bio via la connexion d’informations d’identification WHFB, puis accéder aux ressources locales (partages, imprimantes, etc.), suivez cet [article.](/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base)</span><span class="sxs-lookup"><span data-stu-id="4ce52-120">If you have plans to login to the AADJ device other than password method Like PIN/Bio-metric via WHFB credential login and then access on-premise resources (shares, printers, etc.), please follow [this article](/windows/security/identity-protection/hello-for-business/hello-hybrid-aadj-sso-base).</span></span>

<span data-ttu-id="4ce52-121">Si votre organisation n’est pas prête à déployer dans la configuration d’appareil joint à Azure AD décrite ci-dessus, envisagez de définir la configuration de l’appareil joint à [Azure AD hybride.](manage-windows-devices.md)</span><span class="sxs-lookup"><span data-stu-id="4ce52-121">If your organization isn't ready to deploy in the Azure AD joined device configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>

### <a name="considerations-when-you-join-windows-devices-to-azure-ad"></a><span data-ttu-id="4ce52-122">Considérations à prendre en compte lorsque vous joignez Windows appareils à Azure AD</span><span class="sxs-lookup"><span data-stu-id="4ce52-122">Considerations when you join Windows devices to Azure AD</span></span>

<span data-ttu-id="4ce52-123">Si le Windows que vous avez joint à Azure-AD était précédemment joint au domaine ou dans un groupe de travail, prenons en compte les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ce52-123">If the Windows device that you Azure-AD joined was previously domain-joined or in a workgroup, consider the following limitations:</span></span>

- <span data-ttu-id="4ce52-124">Lorsqu’un appareil Joint Azure AD, il crée un utilisateur sans référencer un profil existant.</span><span class="sxs-lookup"><span data-stu-id="4ce52-124">When a device Azure AD joins, it creates a new user without referencing an existing profile.</span></span> <span data-ttu-id="4ce52-125">Les profils doivent être migrés manuellement.</span><span class="sxs-lookup"><span data-stu-id="4ce52-125">Profiles must be manually migrated.</span></span> <span data-ttu-id="4ce52-126">Un profil utilisateur contient des informations telles que les favoris, les fichiers locaux, les paramètres du navigateur et les paramètres du menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="4ce52-126">A user profile contains information like favorites, local files, browser settings, and Start menu settings.</span></span> <span data-ttu-id="4ce52-127">Une meilleure approche consiste à trouver un outil tiers pour ma map les fichiers et paramètres existants au nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="4ce52-127">A best approach is to find a third-party tool to map existing files and settings to the new profile.</span></span>

- <span data-ttu-id="4ce52-128">Si l’appareil utilise des objets de stratégie de groupe (GPO), certains objets de stratégie de groupe peuvent ne pas avoir de fournisseur de services de [configuration](/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) comparable dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4ce52-128">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune.</span></span> <span data-ttu-id="4ce52-129">Exécutez [l’outil MMAT](https://www.microsoft.com/download/details.aspx?id=45520) pour rechercher des CSP comparables pour les GME existants.</span><span class="sxs-lookup"><span data-stu-id="4ce52-129">Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span>

- <span data-ttu-id="4ce52-130">Les utilisateurs peuvent ne pas être en mesure de s’authentifier aux applications qui dépendent de l’authentification Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4ce52-130">Users might not be able to authenticate to applications that depend on Active Directory authentication.</span></span> <span data-ttu-id="4ce52-131">Évaluez l’application héritée et envisagez de la mettre à jour vers une application qui utilise l’th moderne, si possible.</span><span class="sxs-lookup"><span data-stu-id="4ce52-131">Evaluate the legacy app and consider updating to an app that uses modern Auth, if possible.</span></span>

- <span data-ttu-id="4ce52-132">La découverte d’imprimantes Active Directory ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="4ce52-132">Active Directory printer discovery won't work.</span></span> <span data-ttu-id="4ce52-133">Vous pouvez fournir des chemins d’impression directs pour tous les utilisateurs ou utiliser [l’impression universelle.](/universal-print/)</span><span class="sxs-lookup"><span data-stu-id="4ce52-133">You can provide direct printer paths for all users or use [Universal Print](/universal-print/).</span></span>

### <a name="related-articles"></a><span data-ttu-id="4ce52-134">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="4ce52-134">Related Articles</span></span>

[<span data-ttu-id="4ce52-135">Conditions préalables pour l’Connecter Azure AD</span><span class="sxs-lookup"><span data-stu-id="4ce52-135">Prerequisites for Azure AD Connect</span></span>](/azure/active-directory/hybrid/how-to-connect-install-prerequisites)
