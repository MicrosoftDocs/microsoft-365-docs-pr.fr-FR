---
title: Vue d’ensemble de la configuration
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez les étapes de configuration de Microsoft 365 Business Premium, de l’abonnement, à l’ajout d’un domaine et des utilisateurs, à la configuration de stratégies de sécurité, etc.
ms.openlocfilehash: 9d92aefb3b5666bb7c2fd2e13c9a00f074f107a7
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50912487"
---
# <a name="overview-of-setup"></a><span data-ttu-id="049c7-103">Vue d’ensemble de la configuration</span><span class="sxs-lookup"><span data-stu-id="049c7-103">Overview of setup</span></span>

<span data-ttu-id="049c7-104">Regardez une courte vidéo sur la configuration de Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="049c7-104">Watch a short video about Microsoft 365 Business Premium setup.</span></span><br><br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4jZwg] 

<span data-ttu-id="049c7-105">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span><span class="sxs-lookup"><span data-stu-id="049c7-105">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816).</span></span>

<span data-ttu-id="049c7-106">La plupart des étapes de configuration peuvent être réalisées dans l’installation guidée, mais les autres options sont également répertoriées.</span><span class="sxs-lookup"><span data-stu-id="049c7-106">Most of the setup steps can be done in the guided setup, but the other options are also listed.</span></span>

## <a name="step-1-add-your-domain-and-users"></a><span data-ttu-id="049c7-107">Étape 1 : Ajouter votre domaine et vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="049c7-107">Step 1: Add your domain and users</span></span>

   - <span data-ttu-id="049c7-108">**[Ajoutez votre domaine](set-up.md#add-your-domain-to-personalize-sign-in)** (si vous avez acheté votre domaine lors [de](sign-up.md)l’inscription, cette étape est déjà effectuée).)</span><span class="sxs-lookup"><span data-stu-id="049c7-108">**[Add your domain](set-up.md#add-your-domain-to-personalize-sign-in)** (if you bought your domain during [sign up](sign-up.md), this step is already done.)</span></span>

   - <span data-ttu-id="049c7-109">**Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="049c7-109">**Add users**.</span></span> <span data-ttu-id="049c7-110">Vous pouvez ajouter des utilisateurs de l’une des trois manières possibles :</span><span class="sxs-lookup"><span data-stu-id="049c7-110">You can add users in any of the three ways:</span></span>
        - <span data-ttu-id="049c7-111">Dans la [configuration guidée](set-up.md#add-users-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="049c7-111">In the [guided setup](set-up.md#add-users-in-the-wizard).</span></span>
        - <span data-ttu-id="049c7-112">Utilisez la synchronisation d’annuaires pour ajouter des utilisateurs à l’aide [d’Azure AD Connect](../enterprise/set-up-directory-synchronization.md) si vous avez un annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="049c7-112">Use directory synchronization to [add users by using Azure AD Connect](../enterprise/set-up-directory-synchronization.md) if you have an on-premises Active directory.</span></span>
        - <span data-ttu-id="049c7-113">Vous pouvez également ajouter [des utilisateurs ultérieurement](../admin/add-users/add-users.md) dans le Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="049c7-113">You can also [add users later](../admin/add-users/add-users.md) in the admin center.</span></span>
## <a name="step-2-set-up-security-policies-and-configure-devices"></a><span data-ttu-id="049c7-114">Étape 2 : Configurer des stratégies de sécurité et des appareils</span><span class="sxs-lookup"><span data-stu-id="049c7-114">Step 2: Set up security policies and configure devices</span></span> 

  - <span data-ttu-id="049c7-115">Utilisez la [configuration guidée pour](set-up.md#protect-your-organization) configurer les stratégies d’appareil.</span><span class="sxs-lookup"><span data-stu-id="049c7-115">Use the [guided setup](set-up.md#protect-your-organization) to configure device policies.</span></span> 
  - <span data-ttu-id="049c7-116">Vous pouvez également en ajouter ou les modifier ultérieurement dans le Centre d’administration [et](view-policies-and-devices.md) dans le [portail Intune.](/intune/tutorial-walkthrough-intune-portal)</span><span class="sxs-lookup"><span data-stu-id="049c7-116">You can also add more or edit them later in the [admin center](view-policies-and-devices.md) and in the [Intune portal](/intune/tutorial-walkthrough-intune-portal).</span></span>
  - <span data-ttu-id="049c7-117">L’Assistant Installation configurera également les paramètres de protection contre les menaces de base et de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="049c7-117">The setup wizard will also set up basic threat protection and data loss prevention settings.</span></span>
  
  <span data-ttu-id="049c7-118">Outre les paramètres de sécurité de l’Assistant Installation, vous pouvez renforcer votre sécurité en ajoutant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="049c7-118">In addition to the security settings in the setup wizard, you can increase your security by adding the following settings:</span></span>

- <span data-ttu-id="049c7-119">**Protection contre les programmes malveillants par courrier électronique**</span><span class="sxs-lookup"><span data-stu-id="049c7-119">**Email malware protection**</span></span>
- <span data-ttu-id="049c7-120">**Anti-hameçonnage dans Defender pour Office 365**</span><span class="sxs-lookup"><span data-stu-id="049c7-120">**Anti-phishing in Defender for Office 365**</span></span>
- <span data-ttu-id="049c7-121">**Archivage Exchange Online**</span><span class="sxs-lookup"><span data-stu-id="049c7-121">**Exchange Online Archiving**</span></span>
- <span data-ttu-id="049c7-122">**Azure Information Protection (Plan1)**</span><span class="sxs-lookup"><span data-stu-id="049c7-122">**Azure Information Protection (Plan1**)</span></span>

<span data-ttu-id="049c7-123">Pour commencer, voir augmenter la [protection contre les menaces](increase-threat-protection.md) [et configurer les fonctionnalités de conformité.](set-up-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="049c7-123">To get started, see [increase threat protection](increase-threat-protection.md) and [set up compliance features](set-up-compliance.md).</span></span>

<span data-ttu-id="049c7-124">Consultez également les 10 principales façons de sécuriser [votre Microsoft 365 Business Premium](/office365/admin/security-and-compliance/secure-your-business-data) pour obtenir une feuille de route des meilleures pratiques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="049c7-124">See also [top 10 ways to secure your Microsoft 365 Business Premium](/office365/admin/security-and-compliance/secure-your-business-data) for a road-map of best security practices.</span></span>

## <a name="step-3-set-up-and-manage-windows-10-devices"></a><span data-ttu-id="049c7-125">Étape 3 : Configurer et gérer les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="049c7-125">Step 3: Set up and manage Windows 10 devices</span></span>

<span data-ttu-id="049c7-126">Une fois l’installation guidée terminée, vous devez protéger tous les ordinateurs Windows 10 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="049c7-126">After you complete the guided setup, you will want to protect all the Windows 10 computers in your organization.</span></span>
  
- <span data-ttu-id="049c7-127">Windows 10 Professionnel [](pre-requisites-for-data-protection.md) est une condition préalable pour Microsoft 365 Business Premium, mais si vous avez Windows 7 Professionnel, Windows 8 Professionnel ou Windows 8.1 Professionnel, votre abonnement vous donne droit à une mise à niveau vers [Windows 10 Professionnel.](./upgrade-to-windows-pro-creators-update.md)</span><span class="sxs-lookup"><span data-stu-id="049c7-127">Windows 10 Pro is a [prerequisite](pre-requisites-for-data-protection.md) for Microsoft 365 Business Premium, but if you have Windows 7 Pro, Windows 8 Pro, or Windows 8.1 Pro, your subscription entitles you to an [upgrade to  Windows 10 Pro](./upgrade-to-windows-pro-creators-update.md).</span></span>
- <span data-ttu-id="049c7-128">Suivez les étapes de [la sécurisation des PC Windows 10](secure-win-10-pcs.md) pour configurer des stratégies pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="049c7-128">Follow the steps in [secure Windows 10 PCs](secure-win-10-pcs.md) to set up policies for Windows 10 devices.</span></span>

<span data-ttu-id="049c7-129">Lorsque vous joignez un appareil Windows 10 à Azure AD, les stratégies que vous définissez pour les ordinateurs Windows 10 s’y appliquent.</span><span class="sxs-lookup"><span data-stu-id="049c7-129">When you join a Windows 10 device to Azure AD, the policies you set for Windows 10 computers get applied to it.</span></span> <span data-ttu-id="049c7-130">Pour plus d’informations, voir [Configurer des appareils Windows pour les utilisateurs de Microsoft 365.](set-up-windows-devices.md)</span><span class="sxs-lookup"><span data-stu-id="049c7-130">For more information, see [Set up Windows devices for Microsoft 365 users](set-up-windows-devices.md).</span></span>

## <a name="step-4-install-microsoft-365-apps-for-business"></a><span data-ttu-id="049c7-131">Étape 4 : Installer Microsoft 365 Apps for business</span><span class="sxs-lookup"><span data-stu-id="049c7-131">Step 4: Install Microsoft 365 Apps for business</span></span>
- <span data-ttu-id="049c7-132">Vous pouvez installer automatiquement Office sur les appareils Windows à l’aide de [l’Assistant Installation.](set-up.md#deploy-office-365-client-apps)</span><span class="sxs-lookup"><span data-stu-id="049c7-132">You can automatically install Office in the Windows devices by using the [setup wizard](set-up.md#deploy-office-365-client-apps).</span></span>
- <span data-ttu-id="049c7-133">Permet aux [utilisateurs d’installer des applications Office](/office365/admin/setup/install-applications) pour Windows et les appareils.</span><span class="sxs-lookup"><span data-stu-id="049c7-133">Let users [install Office apps](/office365/admin/setup/install-applications) for Windows and devices.</span></span>
     
## <a name="advanced"></a><span data-ttu-id="049c7-134">Avancé</span><span class="sxs-lookup"><span data-stu-id="049c7-134">Advanced</span></span>
- <span data-ttu-id="049c7-135">**Utiliser Autopilot pour configurer de nouveaux appareils**</span><span class="sxs-lookup"><span data-stu-id="049c7-135">**Use Autopilot to set up new devices**</span></span>
            
     <span data-ttu-id="049c7-136">Vous pouvez utiliser [Windows Autopilot](add-autopilot-devices-and-profile.md) pour pré-configurer automatiquement de nouveaux appareils **Windows** 10 [](https://www.microsoft.com/solution-providers/search) pour un utilisateur, mais il peut être plus facile d’obtenir un partenaire qui peut le faire pour vous.</span><span class="sxs-lookup"><span data-stu-id="049c7-136">You can use [Windows Autopilot](add-autopilot-devices-and-profile.md) to automatically pre-configure **new** Windows 10 devices for a user, but it might be easier to get a [partner](https://www.microsoft.com/solution-providers/search) who can do this for you.</span></span> <span data-ttu-id="049c7-137">Vous pouvez également vous rendre dans [le Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598)et demander à un expert en technologie cloud de configurer les nouveaux appareils que vous achetez.</span><span class="sxs-lookup"><span data-stu-id="049c7-137">You can also go to [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598), and ask a cloud technology expert to set up new devices that you purchase.</span></span>

- <span data-ttu-id="049c7-138">**Accès aux ressources locales**</span><span class="sxs-lookup"><span data-stu-id="049c7-138">**Access on-premises resources**</span></span>

     - <span data-ttu-id="049c7-139">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 Business Premium pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="049c7-139">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business Premium to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span> <span data-ttu-id="049c7-140">Suivez les étapes de l’étape Activer les appareils Windows 10 joints à un domaine pour qu’ils soient gérés par [Microsoft 365 Business Premium](manage-windows-devices.md) pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="049c7-140">Follow the steps in [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business Premium](manage-windows-devices.md) to set this up.</span></span> <span data-ttu-id="049c7-141">Il s’agit de la méthode préférée, et les appareils dans cet état sont appelés appareils joints à Azure AD hybride.</span><span class="sxs-lookup"><span data-stu-id="049c7-141">This is the preferred method, and devices in this state are called Hybrid Azure AD joined devices.</span></span>

    - <span data-ttu-id="049c7-142">Si votre entreprise possède un Active Directory local qui contient certaines ressources locales (telles que des partages de fichiers et des imprimantes), vous pouvez accorder à vos appareils joints à Azure AD un accès à ces ressources en suivant les étapes ci-après : Accéder aux ressources locales à partir d’un appareil joint à Azure AD dans [Microsoft 365 Business Premium](access-resources.md).</span><span class="sxs-lookup"><span data-stu-id="049c7-142">If your business has a local Active Directory that contains some on-premises resources (such as file shares and printers), you can give your Azure AD-joined devices access to these resources by following the steps here: [Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business Premium](access-resources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="049c7-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="049c7-143">See also</span></span>

[<span data-ttu-id="049c7-144">Vidéos de formation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="049c7-144">Microsoft 365 for business training videos</span></span>](https://support.microsoft.com/office/6ab4bbcd-79cf-4000-a0bd-d42ce4d12816)