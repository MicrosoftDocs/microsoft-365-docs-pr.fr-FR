---
title: Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: 2d7ff45e-0da0-4caa-89a9-48cabf41f193
description: 'Découvrez comment configurer des appareils Windows exécutant Windows 10 professionnel pour les utilisateurs professionnels de Microsoft 365. '
ms.openlocfilehash: f929c64b00e4ebf24e9f82fcfea433119abf2f1c
ms.sourcegitcommit: 6a413a65b8c2e10cea08f0a15635b28a1362a582
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2019
ms.locfileid: "38718866"
---
# <a name="set-up-windows-devices-for-microsoft-365-business-users"></a><span data-ttu-id="cb035-103">Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cb035-103">Set up Windows devices for Microsoft 365 Business users</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cb035-104">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="cb035-104">Prerequisites</span></span>

<span data-ttu-id="cb035-p101">Avant de pouvoir configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business, vérifiez que tous les appareils Windows exécutent la version 1703 (Creators Update) de Windows 10 Professionnel. L'exécution de Windows 10 Professionnel est obligatoire pour déployer Windows 10 Business, c'est-à-dire, un ensemble de services cloud et de fonctionnalités de gestion des appareils qui complètent Windows 10 Professionnel et permettent d'activer les contrôles de sécurité et de gestion centralisée de Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="cb035-p101">Before you can set up Windows devices for Microsoft 365 Business users, make sure all the Windows devices are running Windows 10 Pro, version 1703 (Creators Update). Windows 10 Pro is a prerequisite for deploying Windows 10 Business, which is a set of cloud services and device management capabilities that complement Windows 10 Pro and enable the centralized management and security controls of Microsoft 365 Business.</span></span>
  
<span data-ttu-id="cb035-107">Si vous avez des appareils Windows exécutant Windows 7 Professionnel, Windows 8 Professionnel ou Windows 8.1 Professionnel, votre abonnement Microsoft 365 Business vous donne droit à une mise à niveau vers Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cb035-107">If you have Windows devices running Windows 7 Pro, Windows 8 Pro, or Windows 8.1 Pro, your Microsoft 365 Business subscription entitles you to a Windows 10 upgrade.</span></span>
  
<span data-ttu-id="cb035-108">Pour plus d'informations sur la mise à niveau des appareils Windows vers Windows 10 Professionnel Creators Update, suivez les étapes décrites dans cette rubrique : [Mettre à niveau des appareils Windows vers Windows Professionnel Creators Update](upgrade-to-windows-pro-creators-update.md)</span><span class="sxs-lookup"><span data-stu-id="cb035-108">For more information on how to upgrade Windows devices to Windows 10 Pro Creators Update, follow the steps in this topic: [Upgrade Windows devices to Windows Pro Creators Update](upgrade-to-windows-pro-creators-update.md).</span></span>
  
<span data-ttu-id="cb035-109">Consultez [vérifier que l’appareil est connecté à Azure ad](#verify-the-device-is-connected-to-azure-ad) pour vérifier que vous disposez de la mise à niveau ou pour vous assurer que la mise à niveau a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="cb035-109">See [Verify the device is connected to Azure AD](#verify-the-device-is-connected-to-azure-ad) to verify you have the upgrade, or to make sure the upgrade worked.</span></span> 
  
## <a name="join-windows-10-devices-to-your-organizations-azure-ad"></a><span data-ttu-id="cb035-110">Joindre des appareils Windows 10 au service Azure AD de votre organisation</span><span class="sxs-lookup"><span data-stu-id="cb035-110">Join Windows 10 devices to your organization's Azure AD</span></span>

<span data-ttu-id="cb035-111">Lorsque tous les appareils Windows de votre organisation ont été mis à niveau vers Windows 10 professionnel Creators Update ou que vous exécutez déjà Windows 10 Pro Creators Update, vous pouvez joindre ces appareils au service Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb035-111">When all Windows devices in your organization have either been upgraded to Windows 10 Pro Creators Update or are already running Windows 10 Pro Creators Update, you can join these devices to your organization's Azure Active Directory.</span></span> <span data-ttu-id="cb035-112">Une fois les appareils joints, ils seront automatiquement mis à niveau vers Windows 10 Business, qui fait partie de votre abonnement professionnel Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cb035-112">Once the devices are joined, they'll be automatically upgraded to Windows 10 Business, which is part of your Microsoft 365 Business subscription.</span></span>
  
### <a name="for-a-brand-new-or-newly-upgraded-windows-10-pro-device"></a><span data-ttu-id="cb035-113">Pour un appareil Windows 10 Professionnel ou un appareil qui vient d'être mis à niveau</span><span class="sxs-lookup"><span data-stu-id="cb035-113">For a brand new, or newly upgraded, Windows 10 Pro device</span></span>

<span data-ttu-id="cb035-114">Suivez ces étapes pour un nouvel appareil exécutant Windows 10 Professionnel Creators Update, ou pour un appareil qui vient d'être mis à niveau vers Windows 10 Professionnel Creators Update sans passer par la configuration d'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cb035-114">For a brand new device running Windows 10 Pro Creators Update, or for a device that was upgraded to Windows 10 Pro Creators Update but has not gone through Windows 10 device setup, follow these steps.</span></span>
  
1. <span data-ttu-id="cb035-115">Suivez la configuration d'appareil Windows 10 jusqu'à ce que vous arriviez à la page **Comment souhaitez-vous configurer ?**</span><span class="sxs-lookup"><span data-stu-id="cb035-115">Go through Windows 10 device setup until you get to the **How would you like to set up?** page.</span></span> 
    
    ![On the How would you like to set up page, choose Set up for an organization](media/1b0b2dba-00bb-4a99-a729-441479220cb7.png)
  
2. <span data-ttu-id="cb035-117">Dans cette page, sélectionnez **Configurer pour une organisation**, puis entrez le nom d'utilisateur et le mot de passe associés à Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="cb035-117">Here, choose **Set up for an organization** and then enter your username and password for Microsoft 365 Business.</span></span> 
    
3. <span data-ttu-id="cb035-118">Terminez la configuration de l'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cb035-118">Finish Windows 10 device setup.</span></span>
    
   <span data-ttu-id="cb035-p103">Une fois cette opération terminée, l'utilisateur est connecté au domaine Azure AD de votre organisation. Pour vous en assurer, voir [Vérifier qu'un appareil est connecté à Azure AD](#verify-the-device-is-connected-to-azure-ad).</span><span class="sxs-lookup"><span data-stu-id="cb035-p103">Once you're done, the user will be connected to your organization's Azure AD. See [Verify the device is connected to Azure AD](#verify-the-device-is-connected-to-azure-ad) to make sure.</span></span> 
  
### <a name="for-a-device-already-set-up-and-running-windows-10-pro"></a><span data-ttu-id="cb035-121">Pour un appareil qui a déjà été configuré et qui exécute Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="cb035-121">For a device already set up and running Windows 10 Pro</span></span>

 <span data-ttu-id="cb035-122">**Connecter des utilisateurs à Azure AD :**</span><span class="sxs-lookup"><span data-stu-id="cb035-122">**Connect users to Azure AD:**</span></span>
  
1. <span data-ttu-id="cb035-123">Sur le PC Windows de l'utilisateur exécutant Windows 10 Professionnel, version 1703 (Creators Update) (voir [conditions préalables](pre-requisites-for-data-protection.md)), cliquez sur le logo Windows, puis sur l'icône Paramètres.</span><span class="sxs-lookup"><span data-stu-id="cb035-123">In your user's Windows PC, that is running Windows 10 Pro, version 1703 (Creators Update) (see [pre-requisites](pre-requisites-for-data-protection.md)), click the Windows logo, and then the Settings icon.</span></span>
  
   ![In the Start menu, click Windows Settings icon](media/74e1ce9a-1554-4761-beb9-330b176e9b9d.png)
  
2. <span data-ttu-id="cb035-125">Dans **Paramètres**, accédez à **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="cb035-125">In **Settings**, go to **Accounts**.</span></span>
  
   ![In Windows Settings, go to Accounts](media/472fd688-d111-4788-9fbb-56a00fbdc24d.png)
  
3. <span data-ttu-id="cb035-127">À la page **Vos informations**, cliquez sur **Accès Professionnel ou Scolaire** \> **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="cb035-127">On **Your info** page, click **Access work or school** \> **Connect**.</span></span>
  
   ![Choose Connect under Access work or school](media/af3a4e3f-f9b9-4969-b3e2-4ef99308090c.png)
  
4. <span data-ttu-id="cb035-129">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, sous **Autres actions**, sélectionnez **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="cb035-129">On the **Set up a work or school account** dialog, under **Alternate actions**, choose **Join this device to Azure Active Directory**.</span></span>
  
   ![Click Join this device to Azure Active Directory](media/fb709a1b-05a9-4750-9cb9-e097f4412cba.png)
  
5. <span data-ttu-id="cb035-131">À la **page de connexion**, entrez votre adresse e-mail professionnelle ou scolaire \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cb035-131">On the **Let's get you signed in** page, enter your work or school account \> **Next**.</span></span>
  
   <span data-ttu-id="cb035-132">Dans la page **Saisie du mot de passe**, entrez votre mot de passe \> **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="cb035-132">On the **Enter password** page, enter your password \> **Sign in**.</span></span>
  
   ![Enter your work or school email on the Let's get you signed in page](media/f70eb148-b1d2-4ba3-be38-7317eaf0321a.png)
  
6. <span data-ttu-id="cb035-134">Sur la page vérifier qu' **il s’agit de votre organisation** , vérifiez que les informations sont correctes, puis cliquez sur **rejoindre**.</span><span class="sxs-lookup"><span data-stu-id="cb035-134">On the **Make sure this is your organization** page, verify that the information is correct, and click **Join**.</span></span>
  
   <span data-ttu-id="cb035-p104">À la page **Vous avez terminé.**, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cb035-p104">On the **You're all set!** page, click **Done**.</span></span>
  
   ![On the Make sure this is your organization screen, click Join](media/c749c0a2-5191-4347-a451-c062682aa1fb.png)
  
<span data-ttu-id="cb035-138">Si vous avez chargé des fichiers vers OneDrive Entreprise, synchronisez-les vers votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cb035-138">If you uploaded files to OneDrive for Business, sync them back down.</span></span> <span data-ttu-id="cb035-139">Si vous avez utilisé un outil tiers pour migrer le profil et les fichiers, synchronisez-les également avec le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="cb035-139">If you used a third-party tool to migrate profile and files, also sync those to the new profile.</span></span>
  
## <a name="verify-the-device-is-connected-to-azure-ad"></a><span data-ttu-id="cb035-140">Vérifiez que l’appareil est connecté à Azure AD</span><span class="sxs-lookup"><span data-stu-id="cb035-140">Verify the device is connected to Azure AD</span></span>

<span data-ttu-id="cb035-p106">Pour vérifier votre état de synchronisation, dans la page **Accès Professionnel ou Scolaire**, sous **Paramètres**, cliquez dans la zone **Connecté à** _ \<organization name\> _ pour afficher les boutons **Informations** et **Déconnexion**. Cliquez sur **Informations** pour obtenir votre état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="cb035-p106">To verify your sync status, on the **Access work or school** page in **Settings**, click in the **Connected to** _ \<organization name\> _ area to expose the buttons **Info** and **Disconnect**. Click on **Info** to get your synchronization status.</span></span> 
  
<span data-ttu-id="cb035-143">Dans la page État de synchronisation, cliquez sur Synchronisation pour obtenir les stratégies de gestion des appareils mobiles les plus récentes sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cb035-143">On the Sync status page, click Sync to get the latest mobile device management policies onto the PC.</span></span>
  
<span data-ttu-id="cb035-144">Pour commencer à utiliser le compte professionnel Microsoft 365, accédez au bouton **Démarrer** de Windows, cliquez avec le bouton droit sur l’image de votre compte actuel, puis **changez de compte**.</span><span class="sxs-lookup"><span data-stu-id="cb035-144">To start using the Microsoft 365 Business account, go to the Windows **Start** button, right-click your current account picture, and then **Switch account**.</span></span> <span data-ttu-id="cb035-145">Connectez-vous en utilisant l'adresse e-mail et le mot de passe de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb035-145">Sign in by using your organization email and password.</span></span>
  
![Click Info button to view synchronization status](media/818f7043-adbf-402a-844a-59d50034911d.png)
  
## <a name="verify-the-device-is-upgraded-to-windows-10-business"></a><span data-ttu-id="cb035-147">Vérifier qu'un appareil a été mis à niveau vers Windows 10 Business</span><span class="sxs-lookup"><span data-stu-id="cb035-147">Verify the device is upgraded to Windows 10 Business</span></span>

<span data-ttu-id="cb035-148">Vérifiez que les appareils Windows 10 qui ont été mis à niveau vers Windows 10 Business dans le cadre de votre abonnement Microsoft 365 Business ont été joints à votre domaine Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cb035-148">Verify that your Azure AD joined Windows 10 devices were upgraded to Windows 10 Business as part of your Microsoft 365 Business subscription.</span></span>
  
1. <span data-ttu-id="cb035-149">Accédez à **Paramètres** \> **Système** \> **Informations système**.</span><span class="sxs-lookup"><span data-stu-id="cb035-149">Go to **Settings** \> **System** \> **About**.</span></span>
    
2. <span data-ttu-id="cb035-150">Vérifiez que l' **édition** est bien **Windows 10 Business**.</span><span class="sxs-lookup"><span data-stu-id="cb035-150">Confirm that the **Edition** shows **Windows 10 Business**.</span></span>
    
    ![Verify that Windows edition is Windows 10 Business.](media/ff660fc8-d3ba-431b-89a5-f5abded96c4d.png)
  
## <a name="next-steps"></a><span data-ttu-id="cb035-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cb035-152">Next steps</span></span>

<span data-ttu-id="cb035-153">Pour configurer vos appareils mobiles, voir [Configurer des appareils mobiles pour les utilisateurs de Microsoft 365 Business](set-up-mobile-devices.md). Pour définir des stratégies de protection des appareils ou des applications, voir [Gérer Microsoft 365 Business](manage.md).</span><span class="sxs-lookup"><span data-stu-id="cb035-153">To set up your mobile devices, see [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md), To set device protection or app protection policies, see [Manage Microsoft 365 Business](manage.md).</span></span>
  
