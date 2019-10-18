---
title: Réinitialisation de mot de passe pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLGS
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Configurez et testez la réinitialisation de mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 8be1e898d0b995ddbed7b63c2f0ce07c969592c8
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37071593"
---
# <a name="password-reset-for-your-microsoft-365-test-environment"></a><span data-ttu-id="7c075-103">Réinitialisation de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7c075-103">Password reset for your Microsoft 365 test environment</span></span>

<span data-ttu-id="7c075-104">La réinitialisation de mot de passe en libre-service (SSPR) d’Azure Active Directory (Azure AD) permet aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou leurs comptes.</span><span class="sxs-lookup"><span data-stu-id="7c075-104">Azure Active Directory (Azure AD) self-service password reset (SSPR) allows users to reset or unlock their passwords or accounts.</span></span> 

<span data-ttu-id="7c075-105">Cet article vous explique comment configurer et tester les réinitialisations de mot de passe dans votre environnement de test Microsoft 365 en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="7c075-105">This article describes how you can configure and test password resets in your Microsoft 365 test environment in three phases:</span></span>

1.  <span data-ttu-id="7c075-106">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="7c075-106">Create the Microsoft 365 Enterprise test environment.</span></span>
2.  <span data-ttu-id="7c075-107">Activer la réécriture du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7c075-107">Enable password writeback.</span></span>
3.  <span data-ttu-id="7c075-108">Configuration et test de la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="7c075-108">Configure and test password reset for the User 2 account.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="7c075-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="7c075-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="7c075-111">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7c075-111">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="7c075-p101">Tout d’abord, suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="7c075-p101">First, follow the instructions in [password hash synchronization](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="7c075-115">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="7c075-115">This configuration consists of:</span></span> 
  
- <span data-ttu-id="7c075-116">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="7c075-116">Office 365 E5 and EMS E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="7c075-117">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="7c075-117">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="7c075-118">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine Active Directory Domain Services (AD DS) TESTLAB avec le locataire Azure AD de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="7c075-118">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions.</span></span>


## <a name="phase-2-enable-password-writeback"></a><span data-ttu-id="7c075-119">Étape 2 : Activation de la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="7c075-119">Phase 2: Enable password writeback</span></span>

<span data-ttu-id="7c075-120">Suivez les instructions dans [Phase 2 du guide de laboratoire de test de réécriture du mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="7c075-120">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

<span data-ttu-id="7c075-121">La fonction de réécriture du mot de passe doit être activée pour qu’il soit possible d’opérer une réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7c075-121">You must have password writeback enabled to use password reset.</span></span>
  
## <a name="phase-3-configure-and-test-password-reset"></a><span data-ttu-id="7c075-122">Étape 3 : Configuration et test de la réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="7c075-122">Phase 3: Configure and test password reset</span></span>

<span data-ttu-id="7c075-123">Lors de cette étape, vous configurez la réinitialisation de votre mot de passe dans le client Azure AD en fonction de l’appartenance de groupe, puis vous vérifiez qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="7c075-123">In this phase, you configure password reset in the Azure AD tenant through group membership, and then verify that it works.</span></span>

<span data-ttu-id="7c075-124">Tout d’abord, activez la réinitialisation de mot de passe pour les comptes d’un groupe Azure AD spécifique.</span><span class="sxs-lookup"><span data-stu-id="7c075-124">First, enable password reset for the accounts in a specific Azure AD group.</span></span>

1. <span data-ttu-id="7c075-125">Dans une instance privée de votre navigateur, ouvrez [https://portal.azure.com](https://portal.azure.com), puis connectez-vous avec les informations d’identification de votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="7c075-125">From a private instance of your browser, open [https://portal.azure.com](https://portal.azure.com), and then sign in with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="7c075-126">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes > Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="7c075-126">In the Azure portal, click **Azure Active Directory > Groups > New group**.</span></span>
3. <span data-ttu-id="7c075-p102">Définissez le **type de groupe** sur **Sécurité**, le **nom du groupe** sur **PWReset**et le **type d’appartenance** sur **Affecté**. Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="7c075-p102">Set the **Group type** to **Security**, **Group name** to **PWReset**, and the **Membership type** to **Assigned**. Click **Create**.</span></span>
5. <span data-ttu-id="7c075-129">Cliquez sur le groupe **PWReset** dans la liste, puis sur **Membres**.</span><span class="sxs-lookup"><span data-stu-id="7c075-129">Click the **PWReset** group in the list, and then click **Members**.</span></span>
6. <span data-ttu-id="7c075-p103">Cliquez sur **Ajouter des membres**, sur **Utilisateur 2**, puis sur **Sélectionner**. Fermez les pages **PWReset** et **Groupe**.</span><span class="sxs-lookup"><span data-stu-id="7c075-p103">Click **Add members**, click **User 2**, and then click **Select**. Close the **PWReset** and **Group** pages.</span></span>
7. <span data-ttu-id="7c075-132">Sur la page Azure Active Directory, cliquez sur **Réinitialiser le mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="7c075-132">On the Azure Active Directory page, click **Password reset**.</span></span>
8. <span data-ttu-id="7c075-133">Sur la page **Propriétés**, sous l’option **Réinitialisation du mot de passe en libre-service activée**, choisissez **Sélectionné**.</span><span class="sxs-lookup"><span data-stu-id="7c075-133">From the **Properties** page, under the option **Self Service Password Reset Enabled**, choose **Selected**.</span></span>
9. <span data-ttu-id="7c075-134">Dans **Sélectionner un groupe**, choisissez **PWReset**, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7c075-134">From **Select group**, select **PWReset**, and then click **Save**.</span></span>
10. <span data-ttu-id="7c075-135">Fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="7c075-135">Close the private browser instance.</span></span>

<span data-ttu-id="7c075-136">Ensuite, testez la réinitialisation de mot de passe pour le compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="7c075-136">Next, you test password reset for the User 2 account.</span></span>

1. <span data-ttu-id="7c075-137">Ouvrez une nouvelle instance privée du navigateur et accédez à [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span><span class="sxs-lookup"><span data-stu-id="7c075-137">Open a new private browser instance and browse to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span></span>
2. <span data-ttu-id="7c075-138">Connectez-vous avec les informations d’identification du compte Utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="7c075-138">Sign in with the User 2 account credentials.</span></span>
3. <span data-ttu-id="7c075-139">Dans **Ne perdez pas l’accès à votre compte**, indiquez votre numéro de téléphone portable pour configurer le l’authentification par téléphone et votre adresse électronique personnelle ou professionnelle pour configurer l’authentification par adresse électronique.</span><span class="sxs-lookup"><span data-stu-id="7c075-139">In **Don’t lose access to your account**, set the authentication phone to your mobile phone number and the authentication email to your work or personal email account.</span></span>
4. <span data-ttu-id="7c075-140">Une fois que tous deux ont été vérifiés, cliquez sur **Les informations semblent correctes** et fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="7c075-140">After both are verified, click **Looks good** and close the private instance of the browser.</span></span>
5. <span data-ttu-id="7c075-141">Ouvrez une nouvelle instance privée du navigateur et accédez à [https://aka.ms/sspr](https://aka.ms/sspr).</span><span class="sxs-lookup"><span data-stu-id="7c075-141">Open a new private browser instance and go to [https://aka.ms/sspr](https://aka.ms/sspr).</span></span>
6. <span data-ttu-id="7c075-142">Connectez-vous avec les informations d’identification du compte Utilisateur 2, saisissez les caractères de la CAPTCHA, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7c075-142">Sign in with the User 2 account credentials, type the characters from the CAPTCHA, and then click **Next**.</span></span>
8. <span data-ttu-id="7c075-p104">Pour **la première étape de vérification**, cliquez sur **Envoyer un e-mail à mon autre adresse électronique**, puis cliquez sur **Envoyer**. Lorsque vous recevez l’e-mail, saisissez le code de vérification, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="7c075-p104">For **verification step 1**, click **Email my alternate email**, and then click **Email**. When you receive the email, type the verification code, and then click **Next**.</span></span>
9. <span data-ttu-id="7c075-p105">Dans **Revenir à votre compte**, saisissez un nouveau mot de passe pour le compte Utilisateur 2, puis cliquez sur **Terminer**. Notez le mot de passe modifié du compte Utilisateur 2 et conservez-le dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="7c075-p105">In **Get back into your account**, type a new password for the User 2 account, and then click **Finish**. Note the changed password of the User 2 account and store it in a safe location.</span></span>
10. <span data-ttu-id="7c075-147">Dans un onglet distinct du même navigateur, accédez à [https://portal.office.com](https://portal.office.com), puis connectez-vous avec le nom de compte Utilisateur 2 et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7c075-147">In a separate tab of the same browser, go to [https://portal.office.com](https://portal.office.com), and then sign in with the User 2 account name and its new password.</span></span> <span data-ttu-id="7c075-148">Vous devriez voir s’afficher la **page d’accueil de Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="7c075-148">You should see the **Microsoft Office Home** page.</span></span>

<span data-ttu-id="7c075-149">Consultez l’étape [Simplifier les réinitialisations de mot de passe](identity-secure-your-passwords.md#identity-pw-reset) de la phase d’identification pour obtenir des informations et des liens qui vous permettront de configurer des réinitialisations de mot de passe en production.</span><span class="sxs-lookup"><span data-stu-id="7c075-149">See the [Simplify password resets](identity-secure-your-passwords.md#identity-pw-reset) step in the Identity phase for information and links to configure password resets in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="7c075-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7c075-150">Next step</span></span>

<span data-ttu-id="7c075-151">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="7c075-151">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c075-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c075-152">See also</span></span>

[<span data-ttu-id="7c075-153">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7c075-153">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="7c075-154">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7c075-154">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="7c075-155">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="7c075-155">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
