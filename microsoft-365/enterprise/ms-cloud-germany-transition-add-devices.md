---
title: Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Informations supplémentaires sur les appareils sur les services lors du passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) à Office 365 services dans la nouvelle région de centres de données allemands.'
ms.openlocfilehash: 684af01b2d90f44b2cda1cf050d1e4db70f92915
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289438"
---
# <a name="additional-device-information-for-the-migration-from-microsoft-cloud-deutschland"></a><span data-ttu-id="b98d6-103">Informations supplémentaires sur l’appareil pour la migration à partir de Microsoft Cloud Deutschland</span><span class="sxs-lookup"><span data-stu-id="b98d6-103">Additional device information for the migration from Microsoft Cloud Deutschland</span></span>

<span data-ttu-id="b98d6-104">Les appareils joints à Azure AD et inscrits connectés à Microsoft Cloud Deutschland doivent être migrés après la phase 9 et avant la phase 10.</span><span class="sxs-lookup"><span data-stu-id="b98d6-104">Azure AD joined and registered devices connected to Microsoft Cloud Deutschland must be migrated after phase 9 and before phase 10.</span></span> <span data-ttu-id="b98d6-105">La migration d’un appareil dépend du type d’appareil, du système d’exploitation et de la relation Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b98d6-105">The migration of a device depends on the devices type, operating system and Azure AD relation.</span></span>

## <a name="azure-ad-joined-windows-10-devices"></a><span data-ttu-id="b98d6-106">Appareils joints à Azure AD Windows 10 appareils</span><span class="sxs-lookup"><span data-stu-id="b98d6-106">Azure AD Joined Windows 10 devices</span></span>
<span data-ttu-id="b98d6-107">Si un Windows 10 est joint à Azure AD, il doit être déconnecté d’Azure AD et doit être connecté à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b98d6-107">If a Windows 10 device is Azure AD joined, it must be disconnected from Azure AD and must be connected again.</span></span>

<span data-ttu-id="b98d6-108">[![Azure AD Device ](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png) Re-Join Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b98d6-108">[ ![Azure AD Device Re-Join Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png) ](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span></span>


<span data-ttu-id="b98d6-109">Si l’utilisateur est un administrateur sur l’appareil Windows 10, il peut désinsser l’appareil d’Azure AD et le rejoindre à nouveau en trois étapes.</span><span class="sxs-lookup"><span data-stu-id="b98d6-109">If the user is an administrator on the Windows 10 device, the user can unregister the device from Azure AD and re-join it again in three steps.</span></span>

### <a name="step-1-determine-if-the-device-is-azure-id-joined"></a><span data-ttu-id="b98d6-110">Étape 1 : Déterminer si l’appareil est joint à Azure ID</span><span class="sxs-lookup"><span data-stu-id="b98d6-110">Step 1: Determine if the device is Azure ID joined</span></span>

1. <span data-ttu-id="b98d6-111">Connectez-vous avec votre compte professionnel.</span><span class="sxs-lookup"><span data-stu-id="b98d6-111">Sign in with your work account.</span></span>
2. <span data-ttu-id="b98d6-112">Go to **Paramètres**  >  **Accounts**  >  **Access Work or School**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-112">Go to **Settings** > **Accounts** > **Access Work Or School**.</span></span>
3. <span data-ttu-id="b98d6-113">Rechercher un compte dans la liste avec **connecté à [...]' s Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-113">Look for an account in the list with **connected to […]‘s Azure AD**.</span></span>
4. <span data-ttu-id="b98d6-114">Si un compte connecté existe, procédez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="b98d6-114">If a connected account exists, proceed with Step 2.</span></span>

### <a name="step-2-disconnect-the-device-from-azure-ad"></a><span data-ttu-id="b98d6-115">Étape 2 : Déconnecter l’appareil d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="b98d6-115">Step 2: Disconnect the device from Azure AD</span></span>

1. <span data-ttu-id="b98d6-116">Cliquez **sur Déconnecter** sur le compte scolaire ou scolaire ou scolaire connecté.</span><span class="sxs-lookup"><span data-stu-id="b98d6-116">Click **Disconnect** on the connected work or School Account.</span></span>
2. <span data-ttu-id="b98d6-117">Confirmez la déconnexion deux fois.</span><span class="sxs-lookup"><span data-stu-id="b98d6-117">Confirm the disconnect twice.</span></span>
3. <span data-ttu-id="b98d6-118">Entrez un nom d’utilisateur et un mot de passe d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="b98d6-118">Enter a local administrator username and password.</span></span> <span data-ttu-id="b98d6-119">L’appareil est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="b98d6-119">The device is disconnected.</span></span>
4. <span data-ttu-id="b98d6-120">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-120">Restart the device.</span></span>

### <a name="step-3-join-the-device-to-azure-ad"></a><span data-ttu-id="b98d6-121">Étape 3 : Joindre l’appareil à Azure AD</span><span class="sxs-lookup"><span data-stu-id="b98d6-121">Step 3: Join the device to Azure AD</span></span>

1. <span data-ttu-id="b98d6-122">Connectez-vous avec les informations d’identification de l’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="b98d6-122">Sign in with the credentials of the local administrator.</span></span>
2. <span data-ttu-id="b98d6-123">Go to **Paramètres**  >  **Accounts**  >  **Access Work or School**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-123">Go to **Settings** > **Accounts** > **Access Work Or School**.</span></span>
3. <span data-ttu-id="b98d6-124">Cliquez sur **Connecter**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-124">Click **Connect**.</span></span>
4. <span data-ttu-id="b98d6-125">**IMPORTANT**: cliquez **sur Rejoindre Azure AD.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-125">**IMPORTANT**: Click **Join to Azure AD**.</span></span>
5. <span data-ttu-id="b98d6-126">Entrez l’adresse de messagerie et le mot de passe de votre compte de travail.</span><span class="sxs-lookup"><span data-stu-id="b98d6-126">Enter the e-mail address and password of your work account.</span></span> <span data-ttu-id="b98d6-127">L’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="b98d6-127">The device is connected.</span></span>
6. <span data-ttu-id="b98d6-128">Redémarrez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-128">Restart the device.</span></span>
7. <span data-ttu-id="b98d6-129">Connectez-vous avec l’adresse e-mail et le mot de passe de votre compte de travail.</span><span class="sxs-lookup"><span data-stu-id="b98d6-129">Sign in with the email address and password of your work account.</span></span>

<span data-ttu-id="b98d6-130">Si l’utilisateur n’est pas administrateur de l’appareil, un administrateur général Azure AD peut créer le compte d’administrateur local sur l’appareil en suivant ce chemin de configuration et l’un des deux :</span><span class="sxs-lookup"><span data-stu-id="b98d6-130">If the user is not an administrator of the device, an Azure AD global administrator can create the local administrator account on the device following this configuration path and unjoin the device:</span></span>

<span data-ttu-id="b98d6-131">*Paramètres > comptes > autres comptes > informations d’identification > ajouter un utilisateur sans compte Microsoft*</span><span class="sxs-lookup"><span data-stu-id="b98d6-131">*Settings > Accounts > Other Accounts > Credentials unknown > Add user without Microsoft-Account*</span></span>

<span data-ttu-id="b98d6-132">Pour re-rejoindre, les informations d’identification de n’importe quel compte de travail de votre organisation peuvent être utilisées dans cette étape.</span><span class="sxs-lookup"><span data-stu-id="b98d6-132">For re-joining, the credentials of any work account from your organization can be used in this step.</span></span>

<span data-ttu-id="b98d6-133">Sachez que le compte de travail utilisé pour joindre l’appareil sera automatiquement promu en tant qu’administrateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-133">Please consider that the work account used to join the device will be automatically promoted as an Administrator of the device.</span></span>
<span data-ttu-id="b98d6-134">Tout autre compte professionnel de l’organisation peut se connecter à l’appareil, mais ne dispose pas de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="b98d6-134">Any other work account from the organization can sign in to the device, but has no administrator privileges.</span></span>

## <a name="azure-ad-registered-workplace-joined-windows-10-devices"></a><span data-ttu-id="b98d6-135">Azure AD inscrit (joint à l’espace de travail) Windows 10 appareils</span><span class="sxs-lookup"><span data-stu-id="b98d6-135">Azure AD registered (workplace-joined) Windows 10 devices</span></span>

<span data-ttu-id="b98d6-136">Si un Windows 10 est inscrit à Azure AD, il doit être déconnecté d’Azure AD et de nouveau connecté.</span><span class="sxs-lookup"><span data-stu-id="b98d6-136">If a Windows 10 device is Azure AD registered, it needs to be disconnected from the Azure AD and connected again.</span></span>

<span data-ttu-id="b98d6-137">[![Azure AD Device ](../media/ms-cloud-germany-migration-opt-in/AAD-ReRegistration-flow.png) Re-Registration Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b98d6-137">[ ![Azure AD Device Re-Registration Flow](../media/ms-cloud-germany-migration-opt-in/AAD-ReRegistration-flow.png) ](../media/ms-cloud-germany-migration-opt-in/AAD-ReJoin-flow.png#lightbox)</span></span>

### <a name="step-1-determine-if-the-device-is-azure-id-registered"></a><span data-ttu-id="b98d6-138">Étape 1 : Déterminer si l’appareil est inscrit sur Azure ID</span><span class="sxs-lookup"><span data-stu-id="b98d6-138">Step 1: Determine if the device is Azure ID registered</span></span>

1. <span data-ttu-id="b98d6-139">Connectez-vous avec votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b98d6-139">Sign in with your user.</span></span>
2. <span data-ttu-id="b98d6-140">Go to **Paramètres**  >  **Accounts**  >  **Access Work or School**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-140">Go to **Settings** > **Accounts** > **Access Work Or School**.</span></span>
3. <span data-ttu-id="b98d6-141">Découvrez votre compte de travail dans la liste et vérifiez s’il **est connecté à [...]' s Azure AD**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-141">Discover your work account in the list and check if it is **connected to […]‘s Azure AD**.</span></span>

    <span data-ttu-id="b98d6-142">Si votre compte de travail figure dans la liste mais n’est pas connecté à Azure AD, procédez à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="b98d6-142">If your work account is in the list but NOT connected to an Azure AD, proceed with step 2.</span></span>

    <span data-ttu-id="b98d6-143">Dans le cas contraire, votre appareil est joint à Azure AD et vous devez faire référence à [Azure AD Joined Windows 10 appareils.](#azure-ad-joined-windows-10-devices)</span><span class="sxs-lookup"><span data-stu-id="b98d6-143">Otherwise, your device is an Azure AD joined device and you have to refer to [Azure AD Joined Windows 10 devices](#azure-ad-joined-windows-10-devices).</span></span>

### <a name="step-2-disconnect-the-device-from-azure-ad"></a><span data-ttu-id="b98d6-144">Étape 2 : Déconnecter l’appareil d’Azure AD</span><span class="sxs-lookup"><span data-stu-id="b98d6-144">Step 2: Disconnect the device from Azure AD</span></span>

1. <span data-ttu-id="b98d6-145">Cliquez sur votre compte de travail.</span><span class="sxs-lookup"><span data-stu-id="b98d6-145">Click on your work account.</span></span> <span data-ttu-id="b98d6-146">Les boutons *Informations et* *Déconnexion* apparaissent.</span><span class="sxs-lookup"><span data-stu-id="b98d6-146">The buttons *Info* and *Disconnect* appear.</span></span>
2. <span data-ttu-id="b98d6-147">Cliquez sur **Déconnecter.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-147">Click **Disconnect**.</span></span>
3. <span data-ttu-id="b98d6-148">Confirmez la suppression du compte de l’appareil en **cliquant** sur Oui .</span><span class="sxs-lookup"><span data-stu-id="b98d6-148">Confirm account removal from the device by clicking **Yes**.</span></span>

### <a name="step-3-connect-the-device-to-azure-ad"></a><span data-ttu-id="b98d6-149">Étape 3 : Connecter l’appareil vers Azure AD</span><span class="sxs-lookup"><span data-stu-id="b98d6-149">Step 3: Connect the device to Azure AD</span></span>

1. <span data-ttu-id="b98d6-150">Cliquez sur **Connecter**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-150">Click **Connect**.</span></span>
2. <span data-ttu-id="b98d6-151">Entrez l’adresse e-mail de votre compte de travail, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-151">Enter the email address of your work account and click **Next**.</span></span>
3. <span data-ttu-id="b98d6-152">Entrez le mot de passe de votre compte de travail, puis cliquez **sur Se connectez.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-152">Enter the password of your work account and click **Sign in**.</span></span>
4. <span data-ttu-id="b98d6-153">Confirmez en cliquant sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-153">Confirm by clicking **Done**.</span></span> <span data-ttu-id="b98d6-154">Votre compte de travail est de nouveau répertorié.</span><span class="sxs-lookup"><span data-stu-id="b98d6-154">Your work account is listed again.</span></span>

## <a name="android"></a><span data-ttu-id="b98d6-155">Android</span><span class="sxs-lookup"><span data-stu-id="b98d6-155">Android</span></span>

<span data-ttu-id="b98d6-156">Pour Android, les utilisateurs doivent désins inscrire et réenregistrer leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="b98d6-156">For Android, users will need to unregister and re-register their devices.</span></span> <span data-ttu-id="b98d6-157">Vous pouvez le faire via l’application Microsoft Authenticator ou l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="b98d6-157">This can be done via the Microsoft Authenticator app or the Company Portal app.</span></span>

- <span data-ttu-id="b98d6-158">À partir de Microsoft Authenticator’application, les utilisateurs peuvent Paramètres > **inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-158">From the Microsoft Authenticator app, users can go to **Settings > Device Registration**.</span></span> <span data-ttu-id="b98d6-159">À partir de là, les utilisateurs peuvent désins inscrire et réenregistrer leur appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-159">From there users can unregister and re-register their device.</span></span>

- <span data-ttu-id="b98d6-160">À partir de Portail d’entreprise, les utilisateurs peuvent se rendre sur l’onglet **Appareils** et supprimer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-160">From the Company Portal, users can go to **Devices** tab and remove the device.</span></span> <span data-ttu-id="b98d6-161">Ensuite, réinscrivez l’appareil à l’aide Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b98d6-161">After that, re-enroll the device by using Company Portal.</span></span>

- <span data-ttu-id="b98d6-162">Les utilisateurs peuvent également se désins inscrire et s’inscrire à la nouvelle inscription en supprimant le compte de la page des paramètres du compte, puis en ajoutant à nouveaux le compte de travail.</span><span class="sxs-lookup"><span data-stu-id="b98d6-162">Users can also unregister and re-register by removing the account from the account settings page and then re-adding the work account.</span></span>

<span data-ttu-id="b98d6-163">Pour désins inscrire et réenregistrer l’appareil sur Android à l’aide Microsoft Authenticator application :</span><span class="sxs-lookup"><span data-stu-id="b98d6-163">To unregister and re-register the device on Android by using the Microsoft Authenticator app:</span></span>

1. <span data-ttu-id="b98d6-164">Ouvrez l Microsoft Authenticator appappl; et Paramètres **.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-164">Open the Microsoft Authenticator app and go to **Settings**.</span></span>
2. <span data-ttu-id="b98d6-165">Sélectionnez **Inscription de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-165">Select **Device registration**.</span></span>
3. <span data-ttu-id="b98d6-166">Désinsinser l’appareil en sélectionnant **Désinsinsion**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-166">Unregister the device by selecting **Unregister**.</span></span>
4. <span data-ttu-id="b98d6-167">Pour **l’inscription de** l’appareil, ré-inscrivez l’appareil en tapant votre adresse e-mail, puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-167">For **Device registration**, re-register the device by typing your email address, and then select **Register**.</span></span>

<span data-ttu-id="b98d6-168">Pour désins inscrire et réenregistrer un appareil Android à l’Paramètres page :</span><span class="sxs-lookup"><span data-stu-id="b98d6-168">To unregister and re-register an Android device with the Android Settings page:</span></span>

1. <span data-ttu-id="b98d6-169">Ouvrez **Device Paramètres** et go to **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="b98d6-169">Open **Device Settings** and go to **Accounts**.</span></span>
2. <span data-ttu-id="b98d6-170">Sélectionnez le compte de travail que vous souhaitez ré-inscrire et **sélectionnez Supprimer le compte.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-170">Select the work account that you want to re-register and select **Remove account**.</span></span>
3. <span data-ttu-id="b98d6-171">Une fois le compte supprimé, dans la **page** Comptes, sélectionnez Ajouter un **compte > compte de travail.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-171">After the account is removed, from the **Accounts** page, select **Add Account > Work account**.</span></span>
4. <span data-ttu-id="b98d6-172">For **Workplace Join**, type your email address and select **Join** to complete registering the device.</span><span class="sxs-lookup"><span data-stu-id="b98d6-172">For **Workplace Join**, type your email address and select **Join** to complete registering the device.</span></span>

<span data-ttu-id="b98d6-173">Pour désins inscrire et réenregistrer l’appareil sur Android, Portail d’entreprise :</span><span class="sxs-lookup"><span data-stu-id="b98d6-173">To unregister and re-register the device on Android from Company Portal:</span></span>

1. <span data-ttu-id="b98d6-174">Lancez Portail d’entreprise et allez sur **l’onglet** Appareils.</span><span class="sxs-lookup"><span data-stu-id="b98d6-174">Launch Company Portal and go to **Devices** tab.</span></span>
2. <span data-ttu-id="b98d6-175">Sélectionnez l’appareil pour voir les détails de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-175">Select the device to see the device details.</span></span>
3. <span data-ttu-id="b98d6-176">Dans le menu des points de sélection (trois points), sélectionnez Supprimer l’appareil **et** terminez la suppression en confirmant dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b98d6-176">From the ellipses (three dots) menu, select **Remove Device**, and complete the removal by confirming in the dialog.</span></span>
4. <span data-ttu-id="b98d6-177">Vous devez maintenant être déconnecté de l’application Portail d’entreprise’application.</span><span class="sxs-lookup"><span data-stu-id="b98d6-177">You should now be logged out of the Company Portal app.</span></span> <span data-ttu-id="b98d6-178">Sélectionnez **Se connectez** pour ré-inscrire l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-178">Select **Sign in** to re-register the device.</span></span>

<span data-ttu-id="b98d6-179">Pour plus d’informations sur les actions requises pendant la phase de migration de cette charge de travail, ou sur l’impact sur l’administration ou l’utilisation, examinez les informations sur Azure Active Directory (Azure AD) dans Des informations [Azure AD](ms-cloud-germany-transition-azure-ad.md)supplémentaires pour la migration à partir de Microsoft Cloud Deutschland .</span><span class="sxs-lookup"><span data-stu-id="b98d6-179">For more information about any actions required during the migration phase of this workload, or impact to administration or usage, review the information about Azure Active Directory (Azure AD) in [Additional Azure AD information for the migration from Microsoft Cloud Deutschland](ms-cloud-germany-transition-azure-ad.md).</span></span>

## <a name="ios"></a><span data-ttu-id="b98d6-180">iOS</span><span class="sxs-lookup"><span data-stu-id="b98d6-180">iOS</span></span>

<span data-ttu-id="b98d6-181">Sur les appareils iOS, un utilisateur doit supprimer manuellement tous les comptes mis en cache de l’Microsoft Authenticator, désinsister l’appareil et se dé dé connecter à partir de toutes les applications natives de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-181">On iOS devices, a user will need to manually remove any cached accounts from the Microsoft Authenticator, unregister the device, and sign out from any native apps on the device.</span></span>

### <a name="step-1-if-present-remove-the-account-from-the-microsoft-authenticator-app"></a><span data-ttu-id="b98d6-182">Étape 1 : si elle est présente, supprimez le compte de l’application Microsoft Authenticator client</span><span class="sxs-lookup"><span data-stu-id="b98d6-182">Step 1: If present, remove the account from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="b98d6-183">Appuyez sur le compte dans l Microsoft Authenticator appl;</span><span class="sxs-lookup"><span data-stu-id="b98d6-183">Tap the account in the Microsoft Authenticator app.</span></span>
2. <span data-ttu-id="b98d6-184">Appuyez sur **Paramètres** icône dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="b98d6-184">Tap the **Settings** icon in the top-right corner.</span></span> <span data-ttu-id="b98d6-185">Si vous ne voyez pas **l’icône Paramètres,** il se peut que vous n’utilisiez pas la dernière version de Microsoft Authenticator.</span><span class="sxs-lookup"><span data-stu-id="b98d6-185">If you don't see the **Settings** icon, you might not be using the latest version of Microsoft Authenticator.</span></span>
3. <span data-ttu-id="b98d6-186">Appuyez sur **le bouton** Supprimer le compte.</span><span class="sxs-lookup"><span data-stu-id="b98d6-186">Tap the **Remove account** button.</span></span>
4. <span data-ttu-id="b98d6-187">Appuyez **sur toutes les applications sur cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-187">Tap **All apps on this device**.</span></span>

### <a name="step-2-unregister-the-device-from-the-microsoft-authenticator-app"></a><span data-ttu-id="b98d6-188">Étape 2 : Désinsser l’appareil de l Microsoft Authenticator appel</span><span class="sxs-lookup"><span data-stu-id="b98d6-188">Step 2: Unregister the device from the Microsoft Authenticator app</span></span>

1. <span data-ttu-id="b98d6-189">Appuyez sur l’icône de menu dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="b98d6-189">Tap the menu icon in the top-right corner.</span></span>
2. <span data-ttu-id="b98d6-190">Appuyez **Paramètres** puis inscription **de l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="b98d6-190">Tap **Settings** and then **Device Registration**.</span></span>
3. <span data-ttu-id="b98d6-191">Si votre compte s’affiche, **appuyez sur Désinsister l’appareil** et **continuez** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b98d6-191">If your account is shown, tap **Unregister device** and **Continue** in the dialog.</span></span> <span data-ttu-id="b98d6-192">Vous ne devriez voir aucun compte après cela.</span><span class="sxs-lookup"><span data-stu-id="b98d6-192">You should see no account after that.</span></span>

### <a name="step-3-sign-out-from-individual-apps-if-necessary"></a><span data-ttu-id="b98d6-193">Étape 3 : Se sortir des applications individuelles si nécessaire</span><span class="sxs-lookup"><span data-stu-id="b98d6-193">Step 3: Sign out from individual apps if necessary</span></span>

<span data-ttu-id="b98d6-194">Les utilisateurs peuvent se rendre sur des applications individuelles telles que Outlook, Teams et OneDrive, et supprimer des comptes de ces applications.</span><span class="sxs-lookup"><span data-stu-id="b98d6-194">Users can go to individual apps like Outlook, Teams, and OneDrive, and remove accounts from those apps.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b98d6-195">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="b98d6-195">Frequently asked questions</span></span>

<span data-ttu-id="b98d6-196">**Comment savoir si mon organisation est affectée ?**</span><span class="sxs-lookup"><span data-stu-id="b98d6-196">**How can I tell if my organization is affected?**</span></span>

<span data-ttu-id="b98d6-197">Les administrateurs doivent vérifier s’ils ont des appareils Azure AD inscrits ou joints `https://portal.microsoftazure.de` à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b98d6-197">Administrators should check `https://portal.microsoftazure.de` to determine if they have any Azure AD registered or Azure AD joined devices.</span></span> <span data-ttu-id="b98d6-198">Si votre organisation dispose d’appareils Azure AD inscrits ou joints à Azure AD, votre organisation doit suivre les instructions de cette page.</span><span class="sxs-lookup"><span data-stu-id="b98d6-198">If your organization has Azure AD registered or Azure AD joined devices, your organization has to follow the instructions on this page.</span></span>

<span data-ttu-id="b98d6-199">**Quand mes utilisateurs ré-inscrivent-ils leurs appareils ?**</span><span class="sxs-lookup"><span data-stu-id="b98d6-199">**When do my users re-register their devices?**</span></span>

<span data-ttu-id="b98d6-200">Pour réussir, vous devez uniquement désins inscrire et réenregistrer vos appareils une fois la [phase 9](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) terminée.</span><span class="sxs-lookup"><span data-stu-id="b98d6-200">It's critical to your success that you only unregister and re-register your devices after [phase 9](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization) has been completed.</span></span> <span data-ttu-id="b98d6-201">Vous devez terminer la ré-inscription avant le démarrage de la phase 10, sinon vous risquez de perdre l’accès à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d6-201">You must finish the re-registration before phase 10 starts, otherwise you could lose access to your device.</span></span>

<span data-ttu-id="b98d6-202">**Comment savoir que tous mes appareils sont inscrits dans le cloud public ?**</span><span class="sxs-lookup"><span data-stu-id="b98d6-202">**How do I know that all my devices are registered in the public cloud?**</span></span>

<span data-ttu-id="b98d6-203">Pour vérifier si vos appareils sont enregistrés dans le cloud public, vous devez exporter et télécharger la liste des appareils à partir du portail Azure AD vers une feuille de calcul Excel.</span><span class="sxs-lookup"><span data-stu-id="b98d6-203">To check whether your devices are registered in the public cloud, you should export and download the list of devices from the Azure AD portal to an Excel spreadsheet.</span></span> <span data-ttu-id="b98d6-204">Ensuite, filtrez les appareils inscrits (à l’aide de la colonne _registeredTime)_ après la date à laquelle votre organisation a passé la phase 9 du [processus de migration.](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization)</span><span class="sxs-lookup"><span data-stu-id="b98d6-204">Then, filter the devices that are registered (by using the _registeredTime_ column) after the date when your organization has passed [phase 9 of the migration process](ms-cloud-germany-transition-phases.md#phase-9--10-azure-ad-finalization).</span></span>

## <a name="additional-considerations"></a><span data-ttu-id="b98d6-205">Considérations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b98d6-205">Additional considerations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b98d6-206">Le principal de service Intune sera activé après la [phase 3](ms-cloud-germany-transition-phases.md#phase-3-subscription-transfer)du processus de migration, ce qui implique l’activation d’Azure AD Device Registration.</span><span class="sxs-lookup"><span data-stu-id="b98d6-206">The Intune service principal will be enabled after [phase 3 of the migration process](ms-cloud-germany-transition-phases.md#phase-3-subscription-transfer), which implies the activation of Azure AD Device Registration.</span></span> <span data-ttu-id="b98d6-207">Si vous avez bloqué l’inscription des appareils Azure AD avant la migration, vous devez désactiver le principal de service Intune avec PowerShell pour désactiver à nouveau l’inscription des appareils Azure AD avec le portail Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b98d6-207">If you blocked Azure AD Device Registration before migration, you must disable the Intune service principal with PowerShell to disable Azure AD Device Registration with the Azure AD portal again.</span></span> <span data-ttu-id="b98d6-208">Vous pouvez désactiver le principal de service Intune avec cette commande dans la Azure Active Directory PowerShell pour Graph module.</span><span class="sxs-lookup"><span data-stu-id="b98d6-208">You can disable the Intune service principal with this command in the Azure Active Directory PowerShell for Graph module.</span></span>

```powershell
Get-AzureADServicePrincipal -All:$true |Where-object -Property AppId -eq "0000000a-0000-0000-c000-000000000000" | Set-AzureADServicePrincipal -AccountEnabled:$false
```

## <a name="more-information"></a><span data-ttu-id="b98d6-209">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b98d6-209">More information</span></span>

<span data-ttu-id="b98d6-210">Mise en place :</span><span class="sxs-lookup"><span data-stu-id="b98d6-210">Getting started:</span></span>

- [<span data-ttu-id="b98d6-211">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centres de données allemandes</span><span class="sxs-lookup"><span data-stu-id="b98d6-211">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="b98d6-212">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="b98d6-212">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="b98d6-213">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="b98d6-213">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="b98d6-214">Expérience client pendant la migration</span><span class="sxs-lookup"><span data-stu-id="b98d6-214">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="b98d6-215">Transition :</span><span class="sxs-lookup"><span data-stu-id="b98d6-215">Moving through the transition:</span></span>

- [<span data-ttu-id="b98d6-216">Actions et impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="b98d6-216">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="b98d6-217">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="b98d6-217">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="b98d6-218">Informations supplémentaires pour [Azure AD,](ms-cloud-germany-transition-azure-ad.md) [les appareils,](ms-cloud-germany-transition-add-devices.md) [les expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="b98d6-218">Additional information for [Azure AD](ms-cloud-germany-transition-azure-ad.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="b98d6-219">Applications cloud :</span><span class="sxs-lookup"><span data-stu-id="b98d6-219">Cloud apps:</span></span>

- [<span data-ttu-id="b98d6-220">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b98d6-220">Dynamics 365 migration program information</span></span>](/dynamics365/get-started/migrate-data-german-region)
- [<span data-ttu-id="b98d6-221">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="b98d6-221">Power BI migration program information</span></span>](/power-bi/admin/service-admin-migrate-data-germany)
- [<span data-ttu-id="b98d6-222">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b98d6-222">Getting started with your Microsoft Teams upgrade</span></span>](/microsoftteams/upgrade-start-here)
