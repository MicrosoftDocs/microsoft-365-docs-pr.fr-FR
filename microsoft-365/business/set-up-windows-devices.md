---
title: Configurer des Windows pour les utilisateurs Microsoft 365 Business Premium utilisateurs
f1.keywords:
- CSH
ms.author: sharik
author: skjerland
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
- TRN_M365B
- OKR_SMB_Videos
- seo-marvel-mar
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
ms.assetid: 2d7ff45e-0da0-4caa-89a9-48cabf41f193
description: Configurer des Windows en cours d Windows 10 Professionnel pour Microsoft 365 Business Premium utilisateurs, ce qui permet de centraliser la gestion et les contrôles de sécurité.
ms.openlocfilehash: 7a9c75f6ec14605225d40c103c18e62937e773bf
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635871"
---
# <a name="set-up-windows-devices-for-microsoft-365-business-premium-users"></a><span data-ttu-id="f21ac-103">Configurer des Windows pour les utilisateurs Microsoft 365 Business Premium utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f21ac-103">Set up Windows devices for Microsoft 365 Business Premium users</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f21ac-104">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f21ac-104">Before you begin</span></span>

<span data-ttu-id="f21ac-105">Avant de pouvoir configurer des Windows pour les utilisateurs Microsoft 365 Business Premium, assurez-vous que tous les appareils Windows exécutent Windows 10 Professionnel, version 1703 (Creators Update).</span><span class="sxs-lookup"><span data-stu-id="f21ac-105">Before you can set up Windows devices for Microsoft 365 Business Premium users, make sure all the Windows devices are running Windows 10 Pro, version 1703 (Creators Update).</span></span> <span data-ttu-id="f21ac-106">Windows 10 Professionnel est une condition préalable au déploiement de Windows 10 Business, qui est un ensemble de services cloud et de fonctionnalités de gestion des appareils qui complètent les Windows 10 Professionnel et permettent la gestion centralisée et les contrôles de sécurité de Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="f21ac-106">Windows 10 Pro is a prerequisite for deploying Windows 10 Business, which is a set of cloud services and device management capabilities that complement Windows 10 Pro and enable the centralized management and security controls of Microsoft 365 Business Premium.</span></span>
  
<span data-ttu-id="f21ac-107">Si vous avez des appareils Windows exécutant Windows 7 Pro, Windows 8 Professionnel ou Windows 8.1 Professionnel, votre abonnement Microsoft 365 Business Premium vous donne droit à une mise à niveau Windows 10 niveau.</span><span class="sxs-lookup"><span data-stu-id="f21ac-107">If you have Windows devices running Windows 7 Pro, Windows 8 Pro, or Windows 8.1 Pro, your Microsoft 365 Business Premium subscription entitles you to a Windows 10 upgrade.</span></span>
  
<span data-ttu-id="f21ac-108">Pour plus d'informations sur la mise à niveau des appareils Windows vers Windows 10 Professionnel Creators Update, suivez les étapes décrites dans cette rubrique : [Mettre à niveau des appareils Windows vers Windows Professionnel Creators Update](upgrade-to-windows-pro-creators-update.md)</span><span class="sxs-lookup"><span data-stu-id="f21ac-108">For more information on how to upgrade Windows devices to Windows 10 Pro Creators Update, follow the steps in this topic: [Upgrade Windows devices to Windows Pro Creators Update](upgrade-to-windows-pro-creators-update.md).</span></span>
  
<span data-ttu-id="f21ac-109">Vérifiez [que l’appareil est connecté à Azure AD](#verify-the-device-is-connected-to-azure-ad) pour vérifier que vous avez bien mis à niveau ou pour vous assurer que la mise à niveau a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="f21ac-109">See [Verify the device is connected to Azure AD](#verify-the-device-is-connected-to-azure-ad) to verify you have the upgrade, or to make sure the upgrade worked.</span></span>

## <a name="watch-connect-your-pc-to-microsoft-365-business"></a><span data-ttu-id="f21ac-110">Regardez : Connecter pc à Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="f21ac-110">Watch: Connect your PC to Microsoft 365 Business</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3yXh3] 

<span data-ttu-id="f21ac-111">Si vous avez trouvé cette vidéo utile, consultez les [séries de formations complètes pour les petites entreprises et les nouveaux utilisateurs de Microsoft 365](../business-video/index.yml).</span><span class="sxs-lookup"><span data-stu-id="f21ac-111">If you found this video helpful, check out the [complete training series for small businesses and those new to Microsoft 365](../business-video/index.yml).</span></span>
  
## <a name="join-windows-10-devices-to-your-organizations-azure-ad"></a><span data-ttu-id="f21ac-112">Joindre des appareils Windows 10 au service Azure AD de votre organisation</span><span class="sxs-lookup"><span data-stu-id="f21ac-112">Join Windows 10 devices to your organization's Azure AD</span></span>

<span data-ttu-id="f21ac-113">Lorsque tous les appareils Windows de votre organisation ont été mis à niveau vers Windows 10 Professionnel Creators Update ou exécutent déjà Windows 10 Professionnel Creators Update, vous pouvez joindre ces appareils au Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f21ac-113">When all Windows devices in your organization have either been upgraded to Windows 10 Pro Creators Update or are already running Windows 10 Pro Creators Update, you can join these devices to your organization's Azure Active Directory.</span></span> <span data-ttu-id="f21ac-114">Une fois les appareils joints, ils sont automatiquement mis à niveau vers Windows 10 Business, qui fait partie de votre abonnement Microsoft 365 Business Premium abonnement.</span><span class="sxs-lookup"><span data-stu-id="f21ac-114">Once the devices are joined, they'll be automatically upgraded to Windows 10 Business, which is part of your Microsoft 365 Business Premium subscription.</span></span>
  
### <a name="for-a-brand-new-or-newly-upgraded-windows-10-pro-device"></a><span data-ttu-id="f21ac-115">Pour un appareil Windows 10 Professionnel ou un appareil qui vient d'être mis à niveau</span><span class="sxs-lookup"><span data-stu-id="f21ac-115">For a brand new, or newly upgraded, Windows 10 Pro device</span></span>

<span data-ttu-id="f21ac-116">Suivez ces étapes pour un nouvel appareil exécutant Windows 10 Professionnel Creators Update, ou pour un appareil qui vient d'être mis à niveau vers Windows 10 Professionnel Creators Update sans passer par la configuration d'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f21ac-116">For a brand new device running Windows 10 Pro Creators Update, or for a device that was upgraded to Windows 10 Pro Creators Update but has not gone through Windows 10 device setup, follow these steps.</span></span>
  
1. <span data-ttu-id="f21ac-117">Suivez la configuration d'appareil Windows 10 jusqu'à ce que vous arriviez à la page **Comment souhaitez-vous configurer ?**</span><span class="sxs-lookup"><span data-stu-id="f21ac-117">Go through Windows 10 device setup until you get to the **How would you like to set up?** page.</span></span> 
    
    ![On the How would you like to set up page, choose Set up for an organization](../media/1b0b2dba-00bb-4a99-a729-441479220cb7.png)
  
2. <span data-ttu-id="f21ac-119">Ici, **sélectionnez Configurer pour une** organisation, puis entrez votre nom d’utilisateur et votre mot de passe pour Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="f21ac-119">Here, choose **Set up for an organization** and then enter your username and password for Microsoft 365 Business Premium.</span></span> 
    
3. <span data-ttu-id="f21ac-120">Terminez la configuration de l'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="f21ac-120">Finish Windows 10 device setup.</span></span>
    
   <span data-ttu-id="f21ac-p103">Une fois cette opération terminée, l'utilisateur est connecté au domaine Azure AD de votre organisation. Pour vous en assurer, voir [Vérifier qu'un appareil est connecté à Azure AD](#verify-the-device-is-connected-to-azure-ad).</span><span class="sxs-lookup"><span data-stu-id="f21ac-p103">Once you're done, the user will be connected to your organization's Azure AD. See [Verify the device is connected to Azure AD](#verify-the-device-is-connected-to-azure-ad) to make sure.</span></span> 
  
### <a name="for-a-device-already-set-up-and-running-windows-10-pro"></a><span data-ttu-id="f21ac-123">Pour un appareil qui a déjà été configuré et qui exécute Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="f21ac-123">For a device already set up and running Windows 10 Pro</span></span>

 <span data-ttu-id="f21ac-124">**Connecter des utilisateurs à Azure AD :**</span><span class="sxs-lookup"><span data-stu-id="f21ac-124">**Connect users to Azure AD:**</span></span>
  
1. <span data-ttu-id="f21ac-125">Sur le PC Windows de l'utilisateur exécutant Windows 10 Professionnel, version 1703 (Creators Update) (voir [conditions préalables](pre-requisites-for-data-protection.md)), cliquez sur le logo Windows, puis sur l'icône Paramètres.</span><span class="sxs-lookup"><span data-stu-id="f21ac-125">In your user's Windows PC, that is running Windows 10 Pro, version 1703 (Creators Update) (see [pre-requisites](pre-requisites-for-data-protection.md)), click the Windows logo, and then the Settings icon.</span></span>
  
   ![In the Start menu, click Windows Settings icon](../media/74e1ce9a-1554-4761-beb9-330b176e9b9d.png)
  
2. <span data-ttu-id="f21ac-127">Dans **Paramètres**, accédez à **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-127">In **Settings**, go to **Accounts**.</span></span>
  
   ![In Windows Settings, go to Accounts](../media/472fd688-d111-4788-9fbb-56a00fbdc24d.png)
  
3. <span data-ttu-id="f21ac-129">À la page **Vos informations**, cliquez sur **Accès Professionnel ou Scolaire** \> **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-129">On **Your info** page, click **Access work or school** \> **Connect**.</span></span>
  
   ![Choose Connect under Access work or school](../media/af3a4e3f-f9b9-4969-b3e2-4ef99308090c.png)
  
4. <span data-ttu-id="f21ac-131">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, sous **Autres actions**, sélectionnez **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-131">On the **Set up a work or school account** dialog, under **Alternate actions**, choose **Join this device to Azure Active Directory**.</span></span>
  
   ![Click Join this device to Azure Active Directory](../media/fb709a1b-05a9-4750-9cb9-e097f4412cba.png)
  
5. <span data-ttu-id="f21ac-133">À la **page de connexion**, entrez votre adresse e-mail professionnelle ou scolaire \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-133">On the **Let's get you signed in** page, enter your work or school account \> **Next**.</span></span>
  
   <span data-ttu-id="f21ac-134">Dans la page **Saisie du mot de passe**, entrez votre mot de passe \> **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-134">On the **Enter password** page, enter your password \> **Sign in**.</span></span>
  
   ![Enter your work or school email on the Let's get you signed in page](../media/f70eb148-b1d2-4ba3-be38-7317eaf0321a.png)
  
6. <span data-ttu-id="f21ac-136">Dans la page **Vérifier qu’il s’agit de votre** organisation, vérifiez que les informations sont correctes, puis sélectionnez **Rejoindre**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-136">On the **Make sure this is your organization** page, verify that the information is correct, and choose **Join**.</span></span>
  
   <span data-ttu-id="f21ac-137">Sur le **you’re all set!**</span><span class="sxs-lookup"><span data-stu-id="f21ac-137">On the **You're all set!**</span></span> <span data-ttu-id="f21ac-138">page, chosse **done**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-138">page, chosse **Done**.</span></span>
  
   ![Dans l’écran Assurez-vous qu’il s’agit de l’écran de votre organisation, sélectionnez Rejoindre](../media/c749c0a2-5191-4347-a451-c062682aa1fb.png)
  
<span data-ttu-id="f21ac-140">Si vous avez chargé des fichiers vers OneDrive Entreprise, synchronisez-les vers votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f21ac-140">If you uploaded files to OneDrive for Business, sync them back down.</span></span> <span data-ttu-id="f21ac-141">Si vous avez utilisé un outil tiers pour migrer des profils et des fichiers, synchronisez-les également avec le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="f21ac-141">If you used a third-party tool to migrate profile and files, also sync those to the new profile.</span></span>
  
## <a name="verify-the-device-is-connected-to-azure-ad"></a><span data-ttu-id="f21ac-142">Vérifiez que l’appareil est connecté à Azure AD</span><span class="sxs-lookup"><span data-stu-id="f21ac-142">Verify the device is connected to Azure AD</span></span>

<span data-ttu-id="f21ac-143">Pour vérifier votre état de synchronisation, sur la page **Access**  professionnel ou scolaire dans **Paramètres**, sélectionnez la zone Connecté à _ _ pour exposer les boutons Informations et \<organization name\> **Déconnexion.** </span><span class="sxs-lookup"><span data-stu-id="f21ac-143">To verify your sync status, on the **Access work or school** page in **Settings**, select the **Connected to** _ \<organization name\> _ area to expose the buttons **Info** and **Disconnect**.</span></span> <span data-ttu-id="f21ac-144">Choisissez **Info** pour obtenir votre état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="f21ac-144">Choose **Info** to get your synchronization status.</span></span> 
  
<span data-ttu-id="f21ac-145">Dans la page **État de synchronisation,** sélectionnez **Synchroniser** pour obtenir les dernières stratégies de gestion des appareils mobiles sur le PC.</span><span class="sxs-lookup"><span data-stu-id="f21ac-145">On the **Sync status** page, choose **Sync** to get the latest mobile device management policies onto the PC.</span></span>
  
<span data-ttu-id="f21ac-146">Pour commencer à utiliser le compte Microsoft 365 Business Premium, cliquez  avec le bouton Windows démarrer, cliquez avec le bouton droit sur l’image de votre compte actuel, puis changez **de compte.**</span><span class="sxs-lookup"><span data-stu-id="f21ac-146">To start using the Microsoft 365 Business Premium account, go to the Windows **Start** button, right-click your current account picture, and then **Switch account**.</span></span> <span data-ttu-id="f21ac-147">Connectez-vous en utilisant l'adresse e-mail et le mot de passe de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f21ac-147">Sign in by using your organization email and password.</span></span>
  
![Click Info button to view synchronization status](../media/818f7043-adbf-402a-844a-59d50034911d.png)
  
## <a name="verify-the-pc-is-upgraded-to-windows-10-business"></a><span data-ttu-id="f21ac-149">Vérifiez que le PC est mis à niveau vers Windows 10 Business</span><span class="sxs-lookup"><span data-stu-id="f21ac-149">Verify the PC is upgraded to Windows 10 Business</span></span>

<span data-ttu-id="f21ac-150">Vérifiez que vos appareils joints à Azure AD Windows 10 sont mis à niveau vers Windows 10 Business dans le cadre de Microsoft 365 Business Premium abonnement.</span><span class="sxs-lookup"><span data-stu-id="f21ac-150">Verify that your Azure AD joined Windows 10 devices are upgraded to Windows 10 Business as part of your Microsoft 365 Business Premium subscription.</span></span>
  
1. <span data-ttu-id="f21ac-151">Accédez à **Paramètres** \> **Système** \> **Informations système**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-151">Go to **Settings** \> **System** \> **About**.</span></span>
    
2. <span data-ttu-id="f21ac-152">Vérifiez que l' **édition** est bien **Windows 10 Business**.</span><span class="sxs-lookup"><span data-stu-id="f21ac-152">Confirm that the **Edition** shows **Windows 10 Business**.</span></span>
    
    ![Verify that Windows edition is Windows 10 Business.](../media/ff660fc8-d3ba-431b-89a5-f5abded96c4d.png)
  
## <a name="next-steps"></a><span data-ttu-id="f21ac-154">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f21ac-154">Next steps</span></span>

<span data-ttu-id="f21ac-155">Pour configurer vos appareils mobiles, voir Configurer des appareils mobiles pour les utilisateurs [Microsoft 365 Business Premium](set-up-mobile-devices.md), Pour définir des stratégies de protection des appareils ou des applications, voir Gérer Microsoft 365 [entreprise.](manage.md)</span><span class="sxs-lookup"><span data-stu-id="f21ac-155">To set up your mobile devices, see [Set up mobile devices for Microsoft 365 Business Premium users](set-up-mobile-devices.md), To set device protection or app protection policies, see [Manage Microsoft 365 for business](manage.md).</span></span>
  
## <a name="related-content"></a><span data-ttu-id="f21ac-156">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="f21ac-156">Related content</span></span>

<span data-ttu-id="f21ac-157">[Microsoft 365 vidéos de formation pour les entreprises](../business-video/index.yml) (page de liens)</span><span class="sxs-lookup"><span data-stu-id="f21ac-157">[Microsoft 365 for business training videos](../business-video/index.yml) (link page)</span></span>
