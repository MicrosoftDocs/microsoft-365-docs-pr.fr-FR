---
title: Vue d’ensemble de la configuration
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
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Vue d’ensemble des étapes de configuration pour Microsoft 365 Business.
ms.openlocfilehash: 3e1cf240db673a7b961ec8aa574f3e09efee476b
ms.sourcegitcommit: 8ca97fa879ae4ea44468be629d6c32b429efeeec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/16/2019
ms.locfileid: "38676025"
---
# <a name="overview-of-setup"></a><span data-ttu-id="9c534-103">Vue d’ensemble de la configuration</span><span class="sxs-lookup"><span data-stu-id="9c534-103">Overview of setup</span></span>

<span data-ttu-id="9c534-104">La plupart des étapes de configuration peuvent être effectuées dans l’Assistant Installation, mais les autres options sont également répertoriées.</span><span class="sxs-lookup"><span data-stu-id="9c534-104">Most of the set up steps can be done in the setup wizard, but the other options are also listed.</span></span>


## <a name="step-1-add-your-domain-and-users"></a><span data-ttu-id="9c534-105">Étape 1 : ajouter votre domaine et vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9c534-105">Step 1: Add your domain and users</span></span>

   - <span data-ttu-id="9c534-106">**[Ajoutez votre domaine](set-up.md#add-your-domain-to-personalize-sign-in)** (si vous avez acheté votre domaine lors de l' [inscription](sign-up.md), cette étape est déjà terminée).</span><span class="sxs-lookup"><span data-stu-id="9c534-106">**[Add your domain](set-up.md#add-your-domain-to-personalize-sign-in)** (if you bought your domain during [sign up](sign-up.md), this step is already done.)</span></span>

    - <span data-ttu-id="9c534-107">**Ajouter des utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="9c534-107">**Add users**.</span></span> <span data-ttu-id="9c534-108">Pour ce faire, vous pouvez procéder de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c534-108">You can do this in any of the three ways:</span></span>
        - <span data-ttu-id="9c534-109">Dans l' [Assistant](set-up.md#add-users-in-the-wizard).</span><span class="sxs-lookup"><span data-stu-id="9c534-109">In the [wizard](set-up.md#add-users-in-the-wizard).</span></span>
        - <span data-ttu-id="9c534-110">Utilisez la synchronisation d’annuaires pour [Ajouter des utilisateurs à l’aide d’Azure ad Connect](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) si vous disposez d’un annuaire Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="9c534-110">Use directory synchronization to [add users by using Azure AD Connect](https://docs.microsoft.com/office365/enterprise/set-up-directory-synchronization) if you have an on-premises Active directory.</span></span>
        - <span data-ttu-id="9c534-111">Vous pouvez également [Ajouter des utilisateurs ultérieurement](add-users-m365b.md) dans le centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="9c534-111">You can also [add users later](add-users-m365b.md) in the admin center.</span></span>
## <a name="step-2-set-up-security-policies-and-configure-devices"></a><span data-ttu-id="9c534-112">Étape 2 : configurer les stratégies de sécurité et configurer les appareils</span><span class="sxs-lookup"><span data-stu-id="9c534-112">Step 2: Set up security policies and configure devices</span></span> 

  - <span data-ttu-id="9c534-113">Utilisez l' [Assistant Installation](set-up.md#protect-data-and-devices) pour configurer les stratégies d’appareil et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9c534-113">Use the [Setup wizard](set-up.md#protect-data-and-devices) to configure device and security policies.</span></span> 
  - <span data-ttu-id="9c534-114">Vous pouvez également en ajouter ou les modifier ultérieurement dans le [Centre d’administration](view-policies-and-devices.md) et dans le [portail Intune](https://docs.microsoft.com/intune/tutorial-walkthrough-intune-portal).</span><span class="sxs-lookup"><span data-stu-id="9c534-114">You can also add more or edit them later in the [admin center](view-policies-and-devices.md) and in the [Intune portal](https://docs.microsoft.com/intune/tutorial-walkthrough-intune-portal).</span></span>
  - <span data-ttu-id="9c534-115">Outre les paramètres de sécurité de l’Assistant Installation, vous pouvez augmenter votre sécurité en ajoutant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="9c534-115">In addition to the security settings in the setup wizard, you can increase your security by adding the following settings:</span></span>

      - <span data-ttu-id="9c534-116">**Protection contre les programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="9c534-116">**Email malware protection**</span></span>
      - <span data-ttu-id="9c534-117">**Liens fiables de protection avancée contre les menaces**</span><span class="sxs-lookup"><span data-stu-id="9c534-117">**Advanced Threat Protection (ATP) Safe links**</span></span>
      - <span data-ttu-id="9c534-118">**Pièces jointes fiables ATP**</span><span class="sxs-lookup"><span data-stu-id="9c534-118">**ATP Safe Attachments**</span></span>
      - <span data-ttu-id="9c534-119">**Protection contre le hameçonnage (ATP)**</span><span class="sxs-lookup"><span data-stu-id="9c534-119">**ATP anti-phishing**</span></span>
      - <span data-ttu-id="9c534-120">**Archivage Exchange Online**</span><span class="sxs-lookup"><span data-stu-id="9c534-120">**Exchange Online Archiving**</span></span>
      - <span data-ttu-id="9c534-121">**Data Loss Prevention (DLP)**</span><span class="sxs-lookup"><span data-stu-id="9c534-121">**Data Loss Prevention (DLP)**</span></span>
      - <span data-ttu-id="9c534-122">**Azure information protection (plan1**)</span><span class="sxs-lookup"><span data-stu-id="9c534-122">**Azure Information Protection (Plan1**)</span></span>

          <span data-ttu-id="9c534-123">Pour commencer, consultez la rubrique [configurer des stratégies de sécurité avancées](set-up-advanced-security.md).</span><span class="sxs-lookup"><span data-stu-id="9c534-123">To get started see, [set up advanced security policies](set-up-advanced-security.md).</span></span>

        <span data-ttu-id="9c534-124">Consultez également les [10 meilleures façons de sécuriser votre entreprise Microsoft 365](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data) pour obtenir une feuille de route des meilleures pratiques en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9c534-124">See also [top 10 ways to secure your Microsoft 365 Business](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data) for a roadmap of best security practices.</span></span>

## <a name="step-3-set-up-and-manage-windows-10-devices"></a><span data-ttu-id="9c534-125">Étape 3 : configurer et gérer les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="9c534-125">Step 3: Set up and manage Windows 10 devices</span></span>

   <span data-ttu-id="9c534-126">Lorsque vous joignez un appareil Windows 10 à Azure AD, les stratégies que vous avez configurées à l' [étape 2](#step-2-set-up-security-policies-and-configure-devices) sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="9c534-126">When you join a Windows 10 device to Azure AD, the policies you set up in [Step 2](#step-2-set-up-security-policies-and-configure-devices) get applied to it.</span></span>

   - <span data-ttu-id="9c534-127">Windows 10 professionnel est une [condition préalable](pre-requisites-for-data-protection.md) pour Microsoft 365 Business, mais si vous disposez de Windows 7 professionnel, Windows 8 professionnel ou Windows 8,1 Pro, votre abonnement vous donne droit à une [mise à niveau vers Windows 10 professionnel](https://docs.microsoft.com/microsoft-365/business/upgrade-to-windows-pro-creators-update).</span><span class="sxs-lookup"><span data-stu-id="9c534-127">Windows 10 Pro is a [pre-requisite](pre-requisites-for-data-protection.md) for Microsoft 365 Business, but if you have Windows 7 Pro, Windows 8 Pro, or Windows 8.1 Pro, your subscription entitles you to an [upgrade to  Windows 10 Pro](https://docs.microsoft.com/microsoft-365/business/upgrade-to-windows-pro-creators-update).</span></span>
    - <span data-ttu-id="9c534-128">Utilisez l' [Assistant Installation](set-up.md#protect-data-and-devices) pour configurer des stratégies pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9c534-128">Use the [Setup wizard](set-up.md#protect-data-and-devices) to configure policies for Windows 10 devices.</span></span>

## <a name="stes-4-install-office-365-business"></a><span data-ttu-id="9c534-129">Stes 4 : installer Office 365 Business</span><span class="sxs-lookup"><span data-stu-id="9c534-129">Stes 4: Install Office 365 Business</span></span>
- <span data-ttu-id="9c534-130">Vous pouvez installer automatiquement Office sur les appareils Windows à l’aide de l' [Assistant Installation](set-up.md#deploy-office-365-client-apps).</span><span class="sxs-lookup"><span data-stu-id="9c534-130">You can automatically install Office in the Windows devices by using the [setup wizard](set-up.md#deploy-office-365-client-apps).</span></span>
- <span data-ttu-id="9c534-131">Autorisez les utilisateurs à [installer les applications Office](https://docs.microsoft.com/office365/admin/setup/install-applications) pour Windows et les appareils.</span><span class="sxs-lookup"><span data-stu-id="9c534-131">Let users [install Office apps](https://docs.microsoft.com/office365/admin/setup/install-applications) for Windows and devices.</span></span>
     
## <a name="advanced"></a><span data-ttu-id="9c534-132">Avancé</span><span class="sxs-lookup"><span data-stu-id="9c534-132">Advanced</span></span>
- <span data-ttu-id="9c534-133">**Utiliser AutoPilot pour configurer de nouveaux appareils**</span><span class="sxs-lookup"><span data-stu-id="9c534-133">**Use Autopilot to set up new devices**</span></span>
            
     <span data-ttu-id="9c534-134">Vous pouvez utiliser [Windows AutoPilot](add-autopilot-devices-and-profile.md) pour préconfigurer automatiquement les **nouveaux** appareils Windows 10 pour un utilisateur, mais il peut être plus facile d’obtenir un [partenaire](https://www.microsoft.com/solution-providers/search) qui peut le faire pour vous.</span><span class="sxs-lookup"><span data-stu-id="9c534-134">You can use [Windows Autopilot](add-autopilot-devices-and-profile.md) to automatically pre-configure **new** Windows 10 devices for a user, but it might be easier to get a [partner](https://www.microsoft.com/solution-providers/search) who can do this for you.</span></span> <span data-ttu-id="9c534-135">Vous pouvez également accéder à [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598) et demander à un spécialiste de la technologie Cloud de configurer de nouveaux appareils que vous achetez pour vous.</span><span class="sxs-lookup"><span data-stu-id="9c534-135">You can also go to [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=874598) and ask a cloud technology expert set up new devices you purchase for you.</span></span>

- <span data-ttu-id="9c534-136">**Accès aux ressources locales**</span><span class="sxs-lookup"><span data-stu-id="9c534-136">**Access on-premises resources**</span></span>

     - <span data-ttu-id="9c534-137">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 entreprise pour protéger vos appareils Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="9c534-137">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span> <span data-ttu-id="9c534-138">Suivez les étapes de la procédure [activer les appareils Windows 10 appartenant à un domaine pour qu’ils soient gérés par Microsoft 365 Business](manage-windows-devices.md) pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="9c534-138">Follow the steps in [Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business](manage-windows-devices.md) to set this up.</span></span> <span data-ttu-id="9c534-139">Il s’agit de la méthode préférée et les appareils dans cet État sont appelés appareils hybrides Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9c534-139">This is the preferred method and devices in this state are called Hybrid Azure AD joined devices.</span></span>

    - <span data-ttu-id="9c534-140">Si votre entreprise dispose d’un annuaire Active Directory local qui contient certaines ressources locales (telles que des partages de fichiers et des imprimantes), vous pouvez donner à vos appareils joints à Azure AD l’accès à ces ressources en suivant les étapes ci-dessous : [accéder aux ressources locales à partir d’un appareil joint à Azure ad dans Microsoft 365 Business](access-resources.md).</span><span class="sxs-lookup"><span data-stu-id="9c534-140">If your business has a local Active Directory that contains some on-premises resources (such as file shares and printers) , you can give your Azure AD-joined devices access to these resources by following the steps here: [Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business](access-resources.md).</span></span>

  