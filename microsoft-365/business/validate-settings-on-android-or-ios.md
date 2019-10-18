---
title: Valider les paramètres de protection des applications sur les appareils Android ou iOS
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
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: f3433b6b-02f7-447f-9d62-306bf03638b0
description: Learn how to validate the Microsoft 365 Business app protection settings in your Android or iOS devices.
ms.openlocfilehash: 309dbf5bdba81bbf8ad0a9707c136a03c4a28586
ms.sourcegitcommit: bd52f7b662887f552f90c46f69d6a2a42fb66914
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2019
ms.locfileid: "37575525"
---
# <a name="validate-app-protection-settings-on-android-or-ios-devices"></a><span data-ttu-id="cbe0f-103">Valider les paramètres de protection des applications sur les appareils Android ou iOS</span><span class="sxs-lookup"><span data-stu-id="cbe0f-103">Validate app protection settings on Android or iOS devices</span></span>

<span data-ttu-id="cbe0f-104">Suivez les instructions indiquées dans les sections suivantes pour valider les paramètres de protection des applications sur les appareils Android ou iOS.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-104">Follow the instructions in the following sections to validate app protection settings on Android or iOS devices.</span></span>
  
## <a name="android"></a><span data-ttu-id="cbe0f-105">Android</span><span class="sxs-lookup"><span data-stu-id="cbe0f-105">Android</span></span>
  
### <a name="check-that-the-app-protection-settings-are-working-on-user-devices"></a><span data-ttu-id="cbe0f-106">Vérifier que les paramètres de protection des applications fonctionnent sur les appareils de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="cbe0f-106">Check that the App protection settings are working on user devices</span></span>

<span data-ttu-id="cbe0f-107">Une fois que vous avez [défini des configurations d'application pour les appareils Android](app-protection-settings-for-android-and-ios.md) afin de protéger les applications, vous pouvez suivre cette procédure pour confirmer que les paramètres sélectionnés fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-107">After you [set app configurations for Android devices](app-protection-settings-for-android-and-ios.md) to protect the apps, you can follow these steps to validate that the settings you chose work.</span></span> 
  
<span data-ttu-id="cbe0f-108">Tout d'abord, assurez-vous que la stratégie s'applique à l'application dans laquelle vous vous apprêtez à vérifier son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-108">First, make sure that the policy applies to the app in which you are going to validate it.</span></span>
  
1. <span data-ttu-id="cbe0f-109">Dans le [Centre d'administration](https://portal.office.com) Microsoft 365 Business, accédez à **Stratégies** \> **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-109">In the Microsoft 365 Business [admin center](https://portal.office.com) go to **Policies** \> **Edit policy**.</span></span>
    
2. <span data-ttu-id="cbe0f-110">Sélectionnez **Stratégie d'application pour Android** pour les paramètres que vous avez créés lors de la configuration ou une autre stratégie que vous avez créée et vérifiez qu'elle est appliquée pour Outlook, par exemple.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-110">Choose **Application policy for Android** for the settings you created at setup, or another policy you created, and verify that it is enforced for Outlook for example.</span></span> 
    
    ![Shows all the apps for which this policy protects files.](media/b3be3ddd-f683-4073-8d7a-9c639a636a2c.png)
  
### <a name="validate-require-a-pin-or-a-fingerprint-to-access-office-apps"></a><span data-ttu-id="cbe0f-112">Confirmer le fonctionnement du paramètre Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="cbe0f-112">Validate Require a PIN or a fingerprint to access Office apps</span></span>

<span data-ttu-id="cbe0f-113">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Exiger un code confidentiel ou une empreinte pour accéder aux applications Office** est **activée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-113">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require a PIN or fingerprint to access Office apps** is set to **On**.</span></span>
  
![Make sure that the Require a PIN or fingerprint to acces Office apps is set to On.](media/f37eb5b2-7e26-49fb-9bd6-d955d196bacf.png)
  
1. <span data-ttu-id="cbe0f-115">Sur l'appareil Android de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-115">In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business credentials.</span></span>
    
2. <span data-ttu-id="cbe0f-116">Vous êtes également invité à entrer un code confidentiel ou utiliser une empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-116">You will also be prompted to enter a PIN or use a fingerprint.</span></span>
    
    ![Enter a PIN on your Android device to access Office apps.](media/9e8ecfee-8122-4a3a-8918-eece80344310.png)
  
### <a name="validate-reset-pin-after-number-of-failed-attempts"></a><span data-ttu-id="cbe0f-118">Confirmer le fonctionnement du paramètre Réinitialiser le code confidentiel après un certain nombre d'échecs successifs</span><span class="sxs-lookup"><span data-stu-id="cbe0f-118">Validate Reset PIN after number of failed attempts</span></span>

<span data-ttu-id="cbe0f-119">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Réinitialiser le code confidentiel après un certain nombre d'échecs successifs** est définie sur un nombre (par défaut 5).</span><span class="sxs-lookup"><span data-stu-id="cbe0f-119">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Reset PIN after number of failed attempts** is set to some number - this is 5 by default.</span></span> 
  
1. <span data-ttu-id="cbe0f-120">Sur l'appareil Android de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-120">In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business credentials.</span></span>
    
2. <span data-ttu-id="cbe0f-p101">Entrez un code confidentiel incorrect autant de fois que le spécifie la stratégie. Une invite indiquant **Limite de tentatives de saisie du code confidentiel atteinte** s'affiche pour vous permettre de réinitialiser le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p101">Enter an incorrect PIN as many times as specified by the policy. You will see a prompt that states **PIN Attempt Limit Reached** to reset the PIN.</span></span> 
    
    ![After too many incorrect PIN attempts, you need to reset your PIN.](media/fca6fcb4-bb5c-477f-af5e-5dc937e8b835.png)
  
3. <span data-ttu-id="cbe0f-p102">Appuyez sur **Réinitialiser le code confidentiel**. Vous êtes invité à vous connecter avec les informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis à définir un nouveau code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p102">Press **Reset PIN**. You will be prompted to sign in with the user's Microsoft 365 Business credentials, and then required to set a new PIN.</span></span>
    
### <a name="validate-force-users-to-save-all-work-files-to-onedrive-for-business"></a><span data-ttu-id="cbe0f-126">Confirmer le fonctionnement du paramètre Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="cbe0f-126">Validate Force users to save all work files to OneDrive for Business</span></span>

<span data-ttu-id="cbe0f-127">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Se prémunir contre la perte ou le vol d'appareils**, développez **Protéger les fichiers professionnels en cas de perte ou de vol des appareils** et vérifiez que l'option **Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise** est **activée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-127">In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Force users to save all work files to OneDrive for Business** is set to **On**.</span></span>
  
![Verify that Force users to save all work files to OneDrive for Business is set to On.](media/7140fa1d-966d-481c-829f-330c06abb5a5.png)
  
1. <span data-ttu-id="cbe0f-129">Sur l'appareil Android de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-129">In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-130">Ouvrez un e-mail qui contient une pièce jointe et appuyez sur l'icône de flèche vers le bas en regard des informations de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-130">Open an email that contains an attachment and tap the down arrow icon next to the attachment's information.</span></span>
    
    ![Tap the down arrow next to an attachment to try to save it.](media/b22573bb-91ce-455f-84fa-8feb2846b117.png)
  
    <span data-ttu-id="cbe0f-132">Le message **Impossible d'enregistrer sur l'appareil** est affiché au bas de l'écran.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-132">You will see **Cannot save to device** on the bottom of the screen.</span></span> 
    
    ![Warning text that indicates cannot save a file locally to an Android.](media/52ca3f3d-7ed0-4a52-9621-4872da6ea9c5.png)
  
    > [!NOTE]
    > <span data-ttu-id="cbe0f-134">L'enregistrement dans OneDrive Entreprise n'est pas activé pour Android pour le moment. C'est pourquoi la seule chose affichée est le message indiquant que l'enregistrement local est bloqué.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-134">Saving to OneDrive for Business is not enabled for Android at this time, so you can only see that saving locally is blocked.</span></span> 
  
### <a name="validate-require-user-to-sign-in-again-if-office-apps-have-been-idle-for-a-specified-time"></a><span data-ttu-id="cbe0f-135">Confirmer le fonctionnement du paramètre Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="cbe0f-135">Validate Require user to sign in again if Office apps have been idle for a specified time</span></span>

<span data-ttu-id="cbe0f-136">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office** est définie sur un nombre de minutes (par défaut 30).</span><span class="sxs-lookup"><span data-stu-id="cbe0f-136">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require users to sign in again after Office apps have been idle for** is set to some number of minutes - this is 30 minutes by default.</span></span> 
  
1. <span data-ttu-id="cbe0f-137">Sur l'appareil Android de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-137">In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-p103">Vous devez maintenant voir la boîte de réception d'Outlook. Ne touchez pas à l'appareil Android pendant au moins 30 minutes (ou toute autre durée supérieure à celle que vous avez spécifiée dans la stratégie). L'appareil va probablement se mettre en veille.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p103">You should now see Outlook's inbox. Let the Android device idle untouched for at least 30 minutes (or some other amount of time, longer than what you specified in the policy). The device will likely dim.</span></span>
    
3. <span data-ttu-id="cbe0f-141">Accédez à nouveau à Outlook sur l'appareil Android.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-141">Re-access Outlook on the Android device.</span></span>
    
4. <span data-ttu-id="cbe0f-142">Vous êtes invité à entrer votre code confidentiel pour pouvoir accéder à Outlook à nouveau.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-142">You will be prompted to enter your PIN before you can access Outlook again.</span></span>
    
### <a name="validate-protect-work-files-with-encryption"></a><span data-ttu-id="cbe0f-143">Confirmer le fonctionnement du paramètre Chiffrer les fichiers professionnels pour les protéger</span><span class="sxs-lookup"><span data-stu-id="cbe0f-143">Validate Protect work files with encryption</span></span>

<span data-ttu-id="cbe0f-144">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Se prémunir contre la perte ou le vol d'appareils**, développez **Protéger les fichiers professionnels en cas de perte ou de vol des appareils** et vérifiez que l'option **Chiffrer les fichiers professionnels pour les protéger** est **activée** et que l'option **Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise** est **désactivée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-144">In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Protect work files with encryption** is set to **On**, and **Force users to save all work files to OneDrive for Business** is set to **Off**.</span></span>
  
1. <span data-ttu-id="cbe0f-145">Sur l'appareil Android de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-145">In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-146">Ouvrez un e-mail qui contient plusieurs fichiers images en pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-146">Open an email which contains a few image file attachments.</span></span>
    
3. <span data-ttu-id="cbe0f-147">Appuyez sur l'icône de flèche vers le bas en regard des informations de la pièce jointe pour enregistrer cette dernière.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-147">Tap the down arrow icon next to the attachment's info to save it.</span></span>
    
    ![Tap the down arrow to save the figure file to the Android device.](media/08a9e21e-4022-45d5-acff-59cface651e7.png)
  
4. <span data-ttu-id="cbe0f-p104">Il se peut que vous soyez invité à autoriser Outlook à accéder aux photos, éléments multimédia et fichiers enregistrés sur votre appareil. Appuyez sur **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p104">You may be prompted to allow Outlook to access photos, media, and files on your device. Tap **Allow**.</span></span>
    
5. <span data-ttu-id="cbe0f-151">En bas de l'écran, sélectionnez **Enregistrer sur l'appareil**, puis ouvrez l'application **Galerie**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-151">At the bottom of the screen, choose to **Save to Device** and then open the **Gallery** app.</span></span> 
    
6. <span data-ttu-id="cbe0f-p105">Vous devriez voir une photo chiffrée (ou plusieurs si vous avez enregistré plusieurs pièces jointes de fichiers images) dans la liste. Elle peut figurer dans la liste Photos sous la forme d'un carré gris avec un point d'exclamation blanc dans un cercle blanc au centre du carré gris.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p105">You should see an encrypted photo (or more, if you saved multiple image file attachments) in the list. It may appear in the Pictures list as a gray square with a white exclamation point within a white circle in the center of the gray square.</span></span>
    
    ![An encrypted image file in the Gallery app.](media/25936414-bd7e-421d-824e-6e59b877722d.png)
  
## <a name="ios"></a><span data-ttu-id="cbe0f-155">iOS</span><span class="sxs-lookup"><span data-stu-id="cbe0f-155">iOS</span></span>
  
### <a name="check-that-the-app-protection-settings-are-working-on-user-devices"></a><span data-ttu-id="cbe0f-156">Vérifier que les paramètres de protection des applications fonctionnent sur les appareils de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="cbe0f-156">Check that the App protection settings are working on user devices</span></span>

<span data-ttu-id="cbe0f-157">Une fois que vous avez [défini des configurations d'application pour les appareils iOS](app-protection-settings-for-android-and-ios.md) afin de protéger les applications, vous pouvez suivre cette procédure pour confirmer que les paramètres sélectionnés fonctionnent bien.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-157">After you [set app configurations for iOS devices](app-protection-settings-for-android-and-ios.md) to protect apps, you can follow these steps to validate that the settings you chose work.</span></span> 
  
<span data-ttu-id="cbe0f-158">Tout d'abord, assurez-vous que la stratégie s'applique à l'application dans laquelle vous vous apprêtez à vérifier son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-158">First, make sure that the policy applies to the app in which you are going to validate it.</span></span>
  
1. <span data-ttu-id="cbe0f-159">Dans le [Centre d'administration](https://portal.office.com) Microsoft 365 Business, accédez à **Stratégies** \> **Modifier la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-159">In the Microsoft 365 Business [admin center](https://portal.office.com), go to **Policies** \> **Edit policy**.</span></span>
    
2. <span data-ttu-id="cbe0f-160">Sélectionnez **Stratégie d'application pour iOS** pour les paramètres que vous avez créés lors de l'installation ou une autre stratégie que vous avez créée et vérifiez qu'elle est appliquée pour Outlook, par exemple.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-160">Choose **Application policy for iOS** for the settings you created at setup, or another policy you created, and verify that it is enforced for Outlook for example.</span></span> 
    
    ![Shows all the apps for which this policy protects files.](media/842441b8-e7b1-4b86-9edd-d94d1f77b6f4.png)
  
### <a name="validate-require-a-pin-to-access-office-apps"></a><span data-ttu-id="cbe0f-162">Confirmer le fonctionnement du paramètre Exiger un code confidentiel pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="cbe0f-162">Validate Require a PIN to access Office apps</span></span>

<span data-ttu-id="cbe0f-163">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Exiger un code confidentiel ou une empreinte pour accéder aux applications Office** est **activée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-163">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require a PIN or fingerprint to access Office apps** is set to **On**.</span></span>
  
![Make sure that the Require a PIN or fingerprint to acces Office apps is set to On.](media/f37eb5b2-7e26-49fb-9bd6-d955d196bacf.png)
  
1. <span data-ttu-id="cbe0f-165">Sur l'appareil iOS de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-165">In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business credentials.</span></span>
    
2. <span data-ttu-id="cbe0f-166">Vous êtes également invité à entrer un code confidentiel ou utiliser une empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-166">You will also be prompted to enter a PIN or use a fingerprint.</span></span>
    
    ![Enter a PIN on your IOS device to access Office apps.](media/06fc5cf3-9f19-4090-b23c-14bb59805b7a.png)
  
### <a name="validate-reset-pin-after-number-of-failed-attempts"></a><span data-ttu-id="cbe0f-168">Confirmer le fonctionnement du paramètre Réinitialiser le code confidentiel après un certain nombre d'échecs successifs</span><span class="sxs-lookup"><span data-stu-id="cbe0f-168">Validate Reset PIN after number of failed attempts</span></span>

<span data-ttu-id="cbe0f-169">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Réinitialiser le code confidentiel après un certain nombre d'échecs successifs** est définie sur un nombre (par défaut 5).</span><span class="sxs-lookup"><span data-stu-id="cbe0f-169">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Reset PIN after number of failed attempts** is set to some number - this is 5 by default.</span></span> 
  
1. <span data-ttu-id="cbe0f-170">Sur l'appareil iOS de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-170">In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business credentials.</span></span>
    
2. <span data-ttu-id="cbe0f-p106">Entrez un code confidentiel incorrect autant de fois que le spécifie la stratégie. Une invite indiquant **Limite de tentatives de saisie du code confidentiel atteinte** s'affiche pour vous permettre de réinitialiser le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p106">Enter an incorrect PIN as many times as specified by the policy. You will see a prompt that states **PIN Attempt Limit Reached** to reset the PIN.</span></span> 
    
    ![After too many incorrect PIN attempts, you need to reset your PIN.](media/fab5c089-a4a5-4e8d-8c95-b8eed1dfa262.png)
  
3. <span data-ttu-id="cbe0f-p107">Appuyez sur **OK**. Vous êtes invité à vous connecter avec les informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis à définir un nouveau code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p107">Press **OK**. You will be prompted to sign in with the user's Microsoft 365 Business credentials, and then required to set a new PIN.</span></span>
    
### <a name="validate-force-users-to-save-all-work-files-to-onedrive-for-business"></a><span data-ttu-id="cbe0f-176">Confirmer le fonctionnement du paramètre Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="cbe0f-176">Validate Force users to save all work files to OneDrive for Business</span></span>

<span data-ttu-id="cbe0f-177">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Se prémunir contre la perte ou le vol d'appareils**, développez **Protéger les fichiers professionnels en cas de perte ou de vol des appareils** et vérifiez que l'option **Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise** est **activée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-177">In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Force users to save all work files to OneDrive for Business** is set to **On**.</span></span>
  
![Verify that Force users to save all work files to OneDrive for Business is set to On.](media/7140fa1d-966d-481c-829f-330c06abb5a5.png)
  
1. <span data-ttu-id="cbe0f-179">Sur l'appareil iOS de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-179">In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-180">Ouvrez un e-mail qui contient une pièce jointe, ouvrez la pièce jointe et sélectionnez **Enregistrer** au bas de l'écran.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-180">Open an email that contains an attachment, open the attachment and choose **Save** on the bottom of the screen.</span></span> 
    
    ![Tap the Save option after you open an attachment to try to save it.](media/b419b070-1530-4f14-86a8-8d89933a2b25.png)
  
3. <span data-ttu-id="cbe0f-p108">Seule une option pour OneDrive Entreprise devrait être affichée. Si ce n'est pas le cas, appuyez sur **Ajouter un compte** et sélectionnez **OneDrive Entreprise** dans l'écran **Ajouter un compte de stockage**. Indiquez la fonctionnalité Microsoft 365 Entreprise de l'utilisateur final pour vous y connecter lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p108">You should only see an option for OneDrive for Business. If not If not, tap **Add Account** and select **OneDrive for Business** from the **Add Storage Account** screen. Provide the end user's Microsoft 365 Business to sign in when prompted.</span></span> 
    
    <span data-ttu-id="cbe0f-185">Appuyez sur **Enregistrer** et sélectionnez **OneDrive Entreprise**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-185">Tap **Save** and select **OneDrive for Business**.</span></span>
    
### <a name="validate-require-user-to-sign-in-again-if-office-apps-have-been-idle-for-a-specified-time"></a><span data-ttu-id="cbe0f-186">Confirmer le fonctionnement du paramètre Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="cbe0f-186">Validate Require user to sign in again if Office apps have been idle for a specified time</span></span>

<span data-ttu-id="cbe0f-187">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Contrôle de l'accès aux documents Office**, développez **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** et assurez-vous que l'option **Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office** est définie sur un nombre de minutes (par défaut 30).</span><span class="sxs-lookup"><span data-stu-id="cbe0f-187">In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require users to sign in again after Office apps have been idle for** is set to some number of minutes - this is 30 minutes by default.</span></span> 
  
1. <span data-ttu-id="cbe0f-188">Sur l'appareil iOS de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-188">In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-p109">Vous devez maintenant voir la boîte de réception d'Outlook. Ne touchez pas à l'appareil iOS pendant au moins 30 minutes (ou toute autre durée supérieure à celle que vous avez spécifiée dans la stratégie). L'appareil va probablement se mettre en veille.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p109">You should now see Outlook's inbox. Let the iOS device untouched for at least 30 minutes (or some other amount of time, longer than what you specified in the policy). The device will likely dim.</span></span>
    
3. <span data-ttu-id="cbe0f-192">Accédez à nouveau à Outlook sur l'appareil iOS.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-192">Re-access Outlook on the iOS device.</span></span>
    
4. <span data-ttu-id="cbe0f-193">Vous êtes invité à entrer votre code confidentiel pour pouvoir accéder à Outlook à nouveau.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-193">You will be prompted to enter your PIN before you can access Outlook again.</span></span>
    
### <a name="validate-protect-work-files-with-encryption"></a><span data-ttu-id="cbe0f-194">Confirmer le fonctionnement du paramètre Chiffrer les fichiers professionnels pour les protéger</span><span class="sxs-lookup"><span data-stu-id="cbe0f-194">Validate Protect work files with encryption</span></span>

<span data-ttu-id="cbe0f-195">Dans le volet **Modifier une stratégie**, sélectionnez **Modifier** en regard de **Se prémunir contre la perte ou le vol d'appareils**, développez **Protéger les fichiers professionnels en cas de perte ou de vol des appareils** et vérifiez que l'option **Chiffrer les fichiers professionnels pour les protéger** est **activée** et que l'option **Obliger les utilisateurs à enregistrer tous les fichiers professionnels dans OneDrive Entreprise** est **désactivée**.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-195">In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Protect work files with encryption** is set to **On**, and **Force users to save all work files to OneDrive for Business** is set to **Off**.</span></span>
  
1. <span data-ttu-id="cbe0f-196">Sur l'appareil iOS de l'utilisateur, ouvrez Outlook et connectez-vous à l'aide des informations d'identification Microsoft 365 Entreprise de l'utilisateur, puis entrez un code confidentiel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-196">In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business credentials, and enter a PIN if requested.</span></span>
    
2. <span data-ttu-id="cbe0f-197">Ouvrez un e-mail qui contient plusieurs fichiers images en pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-197">Open an email which contains a few image file attachments.</span></span>
    
3. <span data-ttu-id="cbe0f-198">Appuyez sur la pièce jointe, puis sur l'option **Enregistrer** en dessous.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-198">Tap the attachment and then tap the **Save** option under it.</span></span> 
    
4. <span data-ttu-id="cbe0f-p110">Ouvrez l'application **Photos** à partir de l'écran d'accueil. Vous devriez voir une photo (ou plusieurs si vous avez enregistré plusieurs pièces jointes de fichiers images) enregistrée, mais chiffrée.</span><span class="sxs-lookup"><span data-stu-id="cbe0f-p110">Open **Photos** app from the home screen. You should see an encrypted photo (or more, if you saved multiple image file attachments) saved, but encrypted.</span></span> 
    
---

