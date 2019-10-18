---
title: Utiliser le guide étape par étape pour ajouter des appareils et un profil Autopilot
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
ms.collection:
- M365-subscription-management
- M365-identity-device-management
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: be5b6d90-3344-4c5e-bf40-5733eb845beb
description: Découvrez comment utiliser Windows AutoPilot pour configurer de nouveaux appareils Windows 10 pour votre entreprise.
ms.openlocfilehash: d028ea3e902965d55c445dc3b3a02aa315201b25
ms.sourcegitcommit: bd52f7b662887f552f90c46f69d6a2a42fb66914
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2019
ms.locfileid: "37574785"
---
# <a name="use-the-step-by-step-guide-to-add-autopilot-devices-and-profile"></a><span data-ttu-id="4261f-103">Utiliser le guide étape par étape pour ajouter des appareils et un profil Autopilot</span><span class="sxs-lookup"><span data-stu-id="4261f-103">Use the step-by-step guide to add Autopilot devices and profile</span></span>

<span data-ttu-id="4261f-104">Vous pouvez utiliser Windows AutoPilot pour configurer de **nouveaux** appareils Windows 10 pour votre entreprise afin qu’ils soient prêts à être utilisés dès que vous les fournissez à vos employés.</span><span class="sxs-lookup"><span data-stu-id="4261f-104">You can use Windows AutoPilot to set up **new** Windows 10 devices for your business so they are ready for productive use as soon as you give them to your employees.</span></span>
  
## <a name="device-requirements"></a><span data-ttu-id="4261f-105">Configuration requise de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4261f-105">Device requirements</span></span>

<span data-ttu-id="4261f-106">Les appareils doivent respecter ces exigences :</span><span class="sxs-lookup"><span data-stu-id="4261f-106">Devices need to meet these requirements:</span></span>
  
- <span data-ttu-id="4261f-107">Windows 10, version 1703 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="4261f-107">Windows 10, version 1703 or later.</span></span>
    
- <span data-ttu-id="4261f-108">Nouveaux appareils qui ne sont pas issus d'une expérience Windows prête à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="4261f-108">New devices that have not been through Windows out-of-box experience.</span></span>
    
## <a name="use-the-setup-guide-to-create-devices-and-profiles"></a><span data-ttu-id="4261f-109">Utiliser le guide de configuration pour créer des appareils et des profils</span><span class="sxs-lookup"><span data-stu-id="4261f-109">Use the setup guide to create devices and profiles</span></span>

<span data-ttu-id="4261f-110">[![Étiquette pour vous informer le centre d’administration change et vous trouverez plus de détails sur aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span><span class="sxs-lookup"><span data-stu-id="4261f-110">[![Label to let you know the admin center is changing and you can find more details at aka.ms/aboutM365preview.](media/m365admincenterchanging.png)](https://docs.microsoft.com/office365/admin/microsoft-365-admin-center-preview)</span></span>

<span data-ttu-id="4261f-111">Si vous n'avez pas encore créé de groupes d'appareils et de profils, la meilleure façon de commencer consiste à utiliser le guide détaillé, mais vous pouvez également [ajouter des appareils](create-and-edit-autopilot-devices.md) et leur [attribuer des profils](create-and-edit-autopilot-profiles.md) sans utiliser le guide.</span><span class="sxs-lookup"><span data-stu-id="4261f-111">If you have no device groups or profiles created yet, the best way to get started is by using the step-by-step guide, but you can also [add devices](create-and-edit-autopilot-devices.md) and [assign profiles](create-and-edit-autopilot-profiles.md) to them without using the guide.</span></span> 
  
1. <span data-ttu-id="4261f-112">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="4261f-112">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span></span>

2. <span data-ttu-id="4261f-113">Sur le côté gauche, sélectionnez **périphériques** \> **AutoPilot**.</span><span class="sxs-lookup"><span data-stu-id="4261f-113">On the left nav choose **Devices** \> **AutoPilot**.</span></span>

    ![Dans le centre d’administration, sélectionnez périphériques, puis AutoPilot.](media/AutoPilot.png)
  
2. <span data-ttu-id="4261f-115">Sur la page **AutoPilot** , cliquez ou appuyez sur **Guide de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="4261f-115">On the **AutoPilot** page, click or tap **Start guide**.</span></span>
    
    ![Click Start guide for step-by-step instructions for Autopilot.](media/31662655-d1e6-437d-87ea-c0dec5da56f7.png)
  
3. <span data-ttu-id="4261f-p101">Sur la page **Charger un fichier .csv avec une liste d'appareils**, recherchez l'emplacement où vous avez préparé le fichier .csv, puis cliquez sur **Ouvrir** \> **Suivant**. Le fichier doit avoir trois en-têtes :</span><span class="sxs-lookup"><span data-stu-id="4261f-p101">On the **Upload .csv file with list of devices** page, browse to a locations where you have the prepared .CSV file, then **Open** \> **Next**. The file should have three headers:</span></span>
    
  - <span data-ttu-id="4261f-119">Colonne A : Numéro de série de l'appareil</span><span class="sxs-lookup"><span data-stu-id="4261f-119">Column A: Device Serial Number</span></span>
    
  - <span data-ttu-id="4261f-120">Colonne B : ID de produit Windows</span><span class="sxs-lookup"><span data-stu-id="4261f-120">Column B: Windows Product ID</span></span>
    
  - <span data-ttu-id="4261f-121">Colonne C : Hachage du matériel</span><span class="sxs-lookup"><span data-stu-id="4261f-121">Column C: Hardware Hash</span></span>
    
    <span data-ttu-id="4261f-122">Vous pouvez obtenir ces informations à partir de votre fournisseur de matériel ou vous pouvez utiliser le [script Get-WindowsAutoPilotInfo PowerShell](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) qui génèrera un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="4261f-122">You can get this information from your hardware vendor, or you can use the [Get-WindowsAutoPilotInfo PowerShell script](https://www.powershellgallery.com/packages/Get-WindowsAutoPilotInfo) that will generate a CSV file.</span></span> 
    
    <span data-ttu-id="4261f-p102">Pour plus d'informations, voir [Fichier CSV de liste d'appareils](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e). Vous pouvez également télécharger un exemple de fichier sur la page **Charger un fichier .csv avec la liste des appareils**.</span><span class="sxs-lookup"><span data-stu-id="4261f-p102">For more information, see [Device list CSV-file](https://support.office.com/article/932e3676-2491-49f0-9177-d893d2f5276e). You can also download a sample file on the **Upload .csv file with list of devices** page.</span></span> 
    
4. <span data-ttu-id="4261f-p103">Sur la page **Attribuer un profil**, vous pouvez choisir un profil existant ou en créer un. Si vous n'en avez pas encore, vous êtes invité à en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="4261f-p103">On the **Assign a profile** page, you can either pick an existing profile, or create a new one. If you don't have one yet, you will be prompted to create a new one.</span></span> 
    
    <span data-ttu-id="4261f-127">Un proﬁl est un ensemble de paramètres qui peuvent être appliqués à un seul appareil ou à un groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="4261f-127">A profile is a collection of settings that can be applied to a single device or to a group of devices.</span></span>
    
    <span data-ttu-id="4261f-p104">Les fonctionnalités par défaut sont obligatoires et seront définies automatiquement. Les fonctionnalités par défaut sont :</span><span class="sxs-lookup"><span data-stu-id="4261f-p104">The default features are required and will be set automatically. The default features are:</span></span>
    
  - <span data-ttu-id="4261f-130">L'inscription Cortana, OneDrive et OEM est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4261f-130">Cortana, OneDrive and OEM registration is skipped.</span></span>
    
  - <span data-ttu-id="4261f-131">Créez une expérience de connexion avec l'identité de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4261f-131">Create sign-in experience with your company brand.</span></span>
    
  - <span data-ttu-id="4261f-132">Vos appareils vont être connectés à des comptes Azure Active Directory et automatiquement inscrits pour être gérés par Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="4261f-132">Your devices are going to be connected to Azure Active Directory accounts and automatically enrolled to be managed by Microsoft 365 Business.</span></span>
    
    <span data-ttu-id="4261f-133">Pour plus d'informations, voir</span><span class="sxs-lookup"><span data-stu-id="4261f-133">For more information, see</span></span>
    
    <span data-ttu-id="4261f-134">[À propos des paramètres du profil AutoPilot](autopilot-profile-settings.md)</span><span class="sxs-lookup"><span data-stu-id="4261f-134">[About AutoPilot Profile settings](autopilot-profile-settings.md) .</span></span> 
    
5. <span data-ttu-id="4261f-135">Les autres paramètres sont **Ignorer les paramètres de confidentialité** et **Ne pas autoriser l'utilisateur à devenir administrateur local**. Ils sont tous les deux définis sur **Désactivé** par défaut.</span><span class="sxs-lookup"><span data-stu-id="4261f-135">The other settings are **Skip privacy settings** and **Don't allow user to become the local admin**. These are both set to **Off** by default.</span></span> 
    
    <span data-ttu-id="4261f-136">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="4261f-136">Choose **Next**.</span></span>
    
6. <span data-ttu-id="4261f-p105">La page **Vous avez terminé** indique que le profil que vous avez créé (ou choisi) sera appliqué au groupe d'appareils que vous avez créé en chargeant la liste d'appareils. Ces paramètres seront appliqués lors de la prochaine connexion des utilisateurs de l'appareil. Choisissez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="4261f-p105">**You're done** page indicates that the profile you created (or chose) will be applied to the device group you created by uploading the list of devices. These settings will be in effect when the device users sign in next. Choose **Close**.</span></span>
    