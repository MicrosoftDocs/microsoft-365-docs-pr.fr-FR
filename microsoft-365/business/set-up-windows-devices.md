---
title: Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 2d7ff45e-0da0-4caa-89a9-48cabf41f193
description: 'Découvrez comment configurer les périphériques Windows exécutant Windows 10 professionnels de l’informatique pour les utilisateurs professionnels 365 de Microsoft. '
ms.openlocfilehash: 482199b175c568bfae420619aa02024303894789
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867052"
---
# <a name="set-up-windows-devices-for-microsoft-365-business-users"></a><span data-ttu-id="96437-103">Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="96437-103">Set up Windows devices for Microsoft 365 Business users</span></span>

## <a name="prerequisites"></a><span data-ttu-id="96437-104">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="96437-104">Prerequisites</span></span>

<span data-ttu-id="96437-p101">Avant de pouvoir configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business, vérifiez que tous les appareils Windows exécutent la version 1703 (Creators Update) de Windows 10 Professionnel. L'exécution de Windows 10 Professionnel est obligatoire pour déployer Windows 10 Business, c'est-à-dire, un ensemble de services cloud et de fonctionnalités de gestion des appareils qui complètent Windows 10 Professionnel et permettent d'activer les contrôles de sécurité et de gestion centralisée de Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="96437-p101">Before you can set up Windows devices for Microsoft 365 Business users, make sure all the Windows devices are running Windows 10 Pro, version 1703 (Creators Update). Windows 10 Pro is a prerequisite for deploying Windows 10 Business, which is a set of cloud services and device management capabilities that complement Windows 10 Pro and enable the centralized management and security controls of Microsoft 365 Business.</span></span>
  
<span data-ttu-id="96437-107">Si vous avez des appareils Windows exécutant Windows 7 Professionnel, Windows 8 Professionnel ou Windows 8.1 Professionnel, votre abonnement Microsoft 365 Business vous donne droit à une mise à niveau vers Windows 10.</span><span class="sxs-lookup"><span data-stu-id="96437-107">If you have Windows devices running Windows 7 Pro, Windows 8 Pro, or Windows 8.1 Pro, your Microsoft 365 Business subscription entitles you to a Windows 10 upgrade.</span></span>
  
<span data-ttu-id="96437-108">Pour plus d'informations sur la mise à niveau des appareils Windows vers Windows 10 Professionnel Creators Update, suivez les étapes décrites dans cette rubrique : [Mettre à niveau des appareils Windows vers Windows Professionnel Creators Update](upgrade-to-windows-pro-creators-update.md)</span><span class="sxs-lookup"><span data-stu-id="96437-108">For more information on how to upgrade Windows devices to Windows 10 Pro Creators Update, follow the steps in this topic: [Upgrade Windows devices to Windows Pro Creators Update](upgrade-to-windows-pro-creators-update.md).</span></span>
  
<span data-ttu-id="96437-109">Pour vérifier que vous disposez de la mise à niveau ou pour vous assurer que la mise à niveau a été effectuée, voir [Vérifier qu'un appareil a été mis à niveau vers Windows 10 Business](set-up-windows-devices.md#bkmk_verifywin10).</span><span class="sxs-lookup"><span data-stu-id="96437-109">See [Verify the device is upgraded to Windows 10 Business](set-up-windows-devices.md#bkmk_verifywin10) to verify you have the upgrade, or to make sure the upgrade worked.</span></span> 
  
## <a name="join-windows-10-devices-to-your-organizations-azure-ad"></a><span data-ttu-id="96437-110">Joindre des appareils Windows 10 au service Azure AD de votre organisation</span><span class="sxs-lookup"><span data-stu-id="96437-110">Join Windows 10 devices to your organization's Azure AD</span></span>

<span data-ttu-id="96437-p102">Une fois que tous les appareils Windows au sein de votre organisation ont été mis à niveau vers Windows 10 Professionnel Creators Update, ou s'ils exécutent déjà cette version, vous pouvez joindre ces appareils au domaine Azure Active Directory de votre organisation. Une fois que tous les appareils ont été joints, ils sont automatiquement mis à niveau vers Windows 10 Business, une version de Windows incluse dans votre abonnement Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="96437-p102">Once all Windows devices in your organization have either been upgraded to Windows 10 Pro Creators Update or are already running Windows 10 Pro Creators Update, you can join these devices to your organization's Azure Active Directory. Once the devices are joined, they will automatically be upgraded to Windows 10 Business, which is part of your Microsoft 365 Business subscription.</span></span>
  
### <a name="for-a-brand-new-or-newly-upgraded-windows-10-pro-device"></a><span data-ttu-id="96437-113">Pour un appareil Windows 10 Professionnel ou un appareil qui vient d'être mis à niveau</span><span class="sxs-lookup"><span data-stu-id="96437-113">For a brand new, or newly upgraded, Windows 10 Pro device</span></span>

<span data-ttu-id="96437-114">Suivez ces étapes pour un nouvel appareil exécutant Windows 10 Professionnel Creators Update, ou pour un appareil qui vient d'être mis à niveau vers Windows 10 Professionnel Creators Update sans passer par la configuration d'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="96437-114">For a brand new device running Windows 10 Pro Creators Update, or for a device that was upgraded to Windows 10 Pro Creators Update but has not gone through Windows 10 device setup, follow these steps.</span></span>
  
1. <span data-ttu-id="96437-115">Suivez la configuration d'appareil Windows 10 jusqu'à ce que vous arriviez à la page **Comment souhaitez-vous configurer ?**</span><span class="sxs-lookup"><span data-stu-id="96437-115">Go through Windows 10 device setup until you get to the **How would you like to set up?** page.</span></span> 
    
    ![On the How would you like to set up page, choose Set up for an organization](media/1b0b2dba-00bb-4a99-a729-441479220cb7.png)
  
2. <span data-ttu-id="96437-117">Dans cette page, sélectionnez **Configurer pour une organisation**, puis entrez le nom d'utilisateur et le mot de passe associés à Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="96437-117">Here, choose **Set up for an organization** and then enter your username and password for Microsoft 365 Business.</span></span> 
    
3. <span data-ttu-id="96437-118">Terminez la configuration de l'appareil Windows 10.</span><span class="sxs-lookup"><span data-stu-id="96437-118">Finish Windows 10 device setup.</span></span>
    
   <span data-ttu-id="96437-p103">Une fois cette opération terminée, l'utilisateur est connecté au domaine Azure AD de votre organisation. Pour vous en assurer, voir [Vérifier qu'un appareil est connecté à Azure AD](set-up-windows-devices.md#bkmk_verifyaad).</span><span class="sxs-lookup"><span data-stu-id="96437-p103">Once you're done, the user will be connected to your organization's Azure AD. See [Verify the device is connected to Azure AD](set-up-windows-devices.md#bkmk_verifyaad) to make sure.</span></span> 
  
### <a name="for-a-device-already-set-up-and-running-windows-10-pro"></a><span data-ttu-id="96437-121">Pour un appareil qui a déjà été configuré et qui exécute Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="96437-121">For a device already set up and running Windows 10 Pro</span></span>

 <span data-ttu-id="96437-122">**Connecter des utilisateurs à Azure AD :**</span><span class="sxs-lookup"><span data-stu-id="96437-122">**Connect users to Azure AD:**</span></span>
  
1. <span data-ttu-id="96437-123">Sur le PC Windows de l'utilisateur exécutant Windows 10 Professionnel, version 1703 (Creators Update) (voir [conditions préalables](pre-requisites-for-data-protection.md)), cliquez sur le logo Windows, puis sur l'icône Paramètres.</span><span class="sxs-lookup"><span data-stu-id="96437-123">In your user's Windows PC, that is running Windows 10 Pro, version 1703 (Creators Update) (see [pre-requisites](pre-requisites-for-data-protection.md)), click the Windows logo, and then the Settings icon.</span></span>
  
   ![In the Start menu, click Windows Settings icon](media/74e1ce9a-1554-4761-beb9-330b176e9b9d.png)
  
2. <span data-ttu-id="96437-125">Dans **Paramètres**, accédez à **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="96437-125">In **Settings**, go to **Accounts**.</span></span>
  
   ![In Windows Settings, go to Accounts](media/472fd688-d111-4788-9fbb-56a00fbdc24d.png)
  
3. <span data-ttu-id="96437-127">À la page **Vos informations**, cliquez sur **Accès Professionnel ou Scolaire** \> **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="96437-127">On **Your info** page, click **Access work or school** \> **Connect**.</span></span>
  
   ![Choose Connect under Access work or school](media/af3a4e3f-f9b9-4969-b3e2-4ef99308090c.png)
  
4. <span data-ttu-id="96437-129">Dans la boîte de dialogue **Configurer un compte professionnel ou scolaire**, sous **Autres actions**, sélectionnez **Joindre cet appareil à Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="96437-129">On the **Set up a work or school account** dialog, under **Alternate actions**, choose **Join this device to Azure Active Directory**.</span></span>
  
   ![Click Join this device to Azure Active Directory](media/fb709a1b-05a9-4750-9cb9-e097f4412cba.png)
  
5. <span data-ttu-id="96437-131">À la **page de connexion**, entrez votre adresse e-mail professionnelle ou scolaire \> **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="96437-131">On the **Let's get you signed in** page, enter your work or school account \> **Next**.</span></span>
  
   <span data-ttu-id="96437-132">Dans la page **Saisie du mot de passe**, entrez votre mot de passe \> **Se connecter**.</span><span class="sxs-lookup"><span data-stu-id="96437-132">On the **Enter password** page, enter your password \> **Sign in**.</span></span>
  
   ![Enter your work or school email on the Let's get you signed in page](media/f70eb148-b1d2-4ba3-be38-7317eaf0321a.png)
  
6. <span data-ttu-id="96437-134">Sur la \*\* Assurez-vous qu’il s’agit de votre organisation \*\* page, vérifiez que les informations sont correctes, puis cliquez sur **joindre**.</span><span class="sxs-lookup"><span data-stu-id="96437-134">On the \*\* Make sure this is your organization \*\* page, verify that the information is correct, and click **Join**.</span></span>
  
   <span data-ttu-id="96437-p104">À la page **Vous avez terminé.**, cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="96437-p104">On the **You're all set!** page, click **Done**.</span></span>
  
   ![On the Make sure this is your organization screen, click Join](media/c749c0a2-5191-4347-a451-c062682aa1fb.png)
  
<span data-ttu-id="96437-p105">Si vous avez chargé des fichiers vers OneDrive Entreprise, synchronisez-les vers votre ordinateur. Si vous avez utilisé un outil tiers pour migrer un profil et des fichiers, synchronisez-les également avec le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="96437-p105">If you uploaded files to OneDrive for Business, sync them back down. If you used a third party tool to migrate profile and files, sync those also to the new profile.</span></span>
  
## <a name="verify-the-device-is-connected-to-azure-ad"></a><span data-ttu-id="96437-140">Vérifier qu'un appareil est connecté à Azure AD</span><span class="sxs-lookup"><span data-stu-id="96437-140">Verify the device is connected to Azure AD</span></span>

<span data-ttu-id="96437-p106">Pour vérifier votre état de synchronisation, dans la page **Accès Professionnel ou Scolaire**, sous **Paramètres**, cliquez dans la zone **Connecté à** _ \<organization name\> _ pour afficher les boutons **Informations** et **Déconnexion**. Cliquez sur **Informations** pour obtenir votre état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="96437-p106">To verify your sync status, on the **Access work or school** page in **Settings**, click in the **Connected to** _ \<organization name\> _ area to expose the buttons **Info** and **Disconnect**. Click on **Info** to get your synchronization status.</span></span> 
  
<span data-ttu-id="96437-143">Dans la page État de synchronisation, cliquez sur Synchronisation pour obtenir les stratégies de gestion des appareils mobiles les plus récentes sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="96437-143">On the Sync status page, click Sync to get the latest mobile device management policies onto the PC.</span></span>
  
<span data-ttu-id="96437-p107">Pour utiliser le compte Microsoft 365 Entreprise, accédez au bouton **Démarrer** de Windows, cliquez avec le bouton droit sur l'image de votre compte actuel, puis sur **Changer de compte**. Connectez-vous en utilisant l'adresse e-mail et le mot de passe de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="96437-p107">To start using the Microsoft 365 Business account, go to the Windows **Start** button, right-click your current account picture and then **Switch account**. Sign in by using your organization email and password.</span></span>
  
![Click Info button to view synchronization status](media/818f7043-adbf-402a-844a-59d50034911d.png)
  
## <a name="verify-the-device-is-upgraded-to-windows-10-business"></a><span data-ttu-id="96437-147">Vérifier qu'un appareil a été mis à niveau vers Windows 10 Business</span><span class="sxs-lookup"><span data-stu-id="96437-147">Verify the device is upgraded to Windows 10 Business</span></span>

<span data-ttu-id="96437-148">Vérifiez que les appareils Windows 10 qui ont été mis à niveau vers Windows 10 Business dans le cadre de votre abonnement Microsoft 365 Business ont été joints à votre domaine Azure AD.</span><span class="sxs-lookup"><span data-stu-id="96437-148">Verify that your Azure AD joined Windows 10 devices were upgraded to Windows 10 Business as part of your Microsoft 365 Business subscription.</span></span>
  
1. <span data-ttu-id="96437-149">Accédez à **Paramètres** \> **Système** \> **Informations système**.</span><span class="sxs-lookup"><span data-stu-id="96437-149">Go to **Settings** \> **System** \> **About**.</span></span>
    
2. <span data-ttu-id="96437-150">Vérifiez que l' **édition** est bien **Windows 10 Business**.</span><span class="sxs-lookup"><span data-stu-id="96437-150">Confirm that the **Edition** shows **Windows 10 Business**.</span></span>
    
    ![Verify that Windows edition is Windows 10 Business.](media/ff660fc8-d3ba-431b-89a5-f5abded96c4d.png)
  
## <a name="next-steps"></a><span data-ttu-id="96437-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="96437-152">Next steps</span></span>

<span data-ttu-id="96437-153">Pour configurer vos appareils mobiles, voir [Configurer des appareils mobiles pour les utilisateurs de Microsoft 365 Business](set-up-mobile-devices.md). Pour définir des stratégies de protection des appareils ou des applications, voir [Gérer Microsoft 365 Business](manage.md).</span><span class="sxs-lookup"><span data-stu-id="96437-153">To set up your mobile devices, see [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md), To set device protection or app protection policies, see [Manage Microsoft 365 Business](manage.md).</span></span>
  
