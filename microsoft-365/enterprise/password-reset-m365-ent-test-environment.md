---
title: Réinitialisation de mot de passe pour votre environnement de test Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/13/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLGS
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Configurez et testez la réinitialisation de mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 98e6b8d8432c86e9d1c432128ed6d223da83610e
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46686535"
---
# <a name="password-reset-for-your-microsoft-365-test-environment"></a><span data-ttu-id="46262-103">Réinitialisation de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="46262-103">Password reset for your Microsoft 365 test environment</span></span>

<span data-ttu-id="46262-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="46262-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="46262-105">La réinitialisation de mot de passe en libre-service (SSPR) d’Azure Active Directory (Azure AD) permet aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou leurs comptes.</span><span class="sxs-lookup"><span data-stu-id="46262-105">Azure Active Directory (Azure AD) self-service password reset (SSPR) allows users to reset or unlock their passwords or accounts.</span></span> 

<span data-ttu-id="46262-106">Cet article vous explique comment configurer et tester les réinitialisations de mot de passe dans votre environnement de test Microsoft 365 en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="46262-106">This article describes how you can configure and test password resets in your Microsoft 365 test environment in three phases:</span></span>

1.    <span data-ttu-id="46262-107">Créez l’environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="46262-107">Create the Microsoft 365 for enterprise test environment.</span></span>
2.  <span data-ttu-id="46262-108">Activer la réécriture du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="46262-108">Enable password writeback.</span></span>
3.    <span data-ttu-id="46262-109">Configurer et tester la réinitialisation de mot de passe pour le compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="46262-109">Configure and test password reset for the User 3 account.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="46262-111">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="46262-111">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="46262-112">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="46262-112">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="46262-p101">Tout d’abord, suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="46262-p101">First, follow the instructions in [password hash synchronization](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="46262-116">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="46262-116">This configuration consists of:</span></span> 
  
- <span data-ttu-id="46262-117">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="46262-117">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="46262-118">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="46262-118">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="46262-119">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB Active Directory Domain Services (AD DS) avec le client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="46262-119">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Microsoft 365 subscription.</span></span>

## <a name="phase-2-enable-password-writeback"></a><span data-ttu-id="46262-120">Étape 2 : Activation de la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="46262-120">Phase 2: Enable password writeback</span></span>

<span data-ttu-id="46262-121">Suivez les instructions dans [Phase 2 du guide de laboratoire de test de réécriture du mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="46262-121">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

<span data-ttu-id="46262-122">La fonction de réécriture du mot de passe doit être activée pour qu’il soit possible d’opérer une réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="46262-122">You must have password writeback enabled to use password reset.</span></span>
  
## <a name="phase-3-configure-and-test-password-reset"></a><span data-ttu-id="46262-123">Étape 3 : Configuration et test de la réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="46262-123">Phase 3: Configure and test password reset</span></span>

<span data-ttu-id="46262-124">Lors de cette étape, vous configurez la réinitialisation de votre mot de passe dans le client Azure AD en fonction de l’appartenance de groupe, puis vous vérifiez qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="46262-124">In this phase, you configure password reset in the Azure AD tenant through group membership, and then verify that it works.</span></span>

<span data-ttu-id="46262-125">Tout d’abord, activez la réinitialisation de mot de passe pour les comptes d’un groupe Azure AD spécifique.</span><span class="sxs-lookup"><span data-stu-id="46262-125">First, enable password reset for the accounts in a specific Azure AD group.</span></span>

1. <span data-ttu-id="46262-126">Dans une instance privée de votre navigateur, ouvrez [https://portal.azure.com](https://portal.azure.com), puis connectez-vous avec les informations d’identification de votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="46262-126">From a private instance of your browser, open [https://portal.azure.com](https://portal.azure.com), and then sign in with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="46262-127">Dans le portail Azure, cliquez sur **Azure Active Directory > Groupes > Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="46262-127">In the Azure portal, click **Azure Active Directory > Groups > New group**.</span></span>
3. <span data-ttu-id="46262-128">Définissez le **Type de groupe** sur **Sécurité**, le **Nom du groupe** sur **PWReset**et le **Type d’appartenance** sur **Affecté**.</span><span class="sxs-lookup"><span data-stu-id="46262-128">Set the **Group type** to **Security**, **Group name** to **PWReset**, and the **Membership type** to **Assigned**.</span></span> 
4. <span data-ttu-id="46262-129">Cliquez sur **Membres**, recherchez et sélectionnez **Utilisateur 3**, cliquez sur **Sélectionner**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="46262-129">Click **Members**, find and select **User 3**, and then click **Select**, and then click **Create**.</span></span>
5. <span data-ttu-id="46262-130">Fermez le volet **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="46262-130">Close the **Groups** pane.</span></span>
6. <span data-ttu-id="46262-131">Dans la page d’Azure Active Directory, cliquez sur **Réinitialiser le mot de passe** du volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="46262-131">In the Azure Active Directory pane, click **Password reset** in the left navigation.</span></span>
7. <span data-ttu-id="46262-132">Sur la page **Propriétés–Réinitialiser le mot de passe**, sous l’option **Réinitialisation du mot de passe en libre-service activée**, choisissez **Sélectionné**.</span><span class="sxs-lookup"><span data-stu-id="46262-132">In the **Password reset-Properties** pane, under the option **Self Service Password Reset Enabled**, choose **Selected**.</span></span>
8. <span data-ttu-id="46262-133">Cliquez sur **Sélectionner le groupe**, sélectionnez le groupe **PWReset**, puis cliquez sur **Sélectionner > Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="46262-133">Click **Select group**, select the **PWReset** group, and then click **Select > Save**.</span></span>
9. <span data-ttu-id="46262-134">Fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="46262-134">Close the private browser instance.</span></span>

<span data-ttu-id="46262-135">Testez ensuite la réinitialisation de mot de passe pour le compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="46262-135">Next, you test password reset for the User 3 account.</span></span>

1. <span data-ttu-id="46262-136">Ouvrez une nouvelle instance privée du navigateur et accédez à [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span><span class="sxs-lookup"><span data-stu-id="46262-136">Open a new private browser instance and browse to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span></span>
2. <span data-ttu-id="46262-137">Connectez-vous avec les informations d’identification du compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="46262-137">Sign in with the User 3 account credentials.</span></span>
3. <span data-ttu-id="46262-138">Dans **Plus d’informations sont nécessaires**, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46262-138">In **More information required**, click **Next**.</span></span> 
5. <span data-ttu-id="46262-139">Dans **Ne perdez pas l’accès à votre compte**, indiquez votre numéro de téléphone portable pour configurer l’authentification par téléphone et votre adresse électronique personnelle ou professionnelle pour configurer l’authentification par adresse électronique.</span><span class="sxs-lookup"><span data-stu-id="46262-139">In **Don't lose access to your account**, set the authentication phone to your mobile phone number and the authentication email to your work or personal email account.</span></span>
7. <span data-ttu-id="46262-140">Une fois que tous deux ont été vérifiés, cliquez sur **Les informations semblent correctes** et fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="46262-140">After both are verified, click **Looks good** and close the private instance of the browser.</span></span>
8. <span data-ttu-id="46262-141">Ouvrez une nouvelle instance privée du navigateur et accédez à [https://aka.ms/sspr](https://aka.ms/sspr).</span><span class="sxs-lookup"><span data-stu-id="46262-141">Open a new private browser instance and go to [https://aka.ms/sspr](https://aka.ms/sspr).</span></span>
9. <span data-ttu-id="46262-142">Tapez le nom du compte Utilisateur 3, saisissez les caractères de la CAPTCHA, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46262-142">Type the User 3 account name, type the characters from the CAPTCHA, and then click **Next**.</span></span>
10. <span data-ttu-id="46262-p102">Pour **la première étape de vérification**, cliquez sur **Envoyer un e-mail à mon autre adresse électronique**, puis cliquez sur **Envoyer**. Lorsque vous recevez l’e-mail, saisissez le code de vérification, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="46262-p102">For **verification step 1**, click **Email my alternate email**, and then click **Email**. When you receive the email, type the verification code, and then click **Next**.</span></span>
11. <span data-ttu-id="46262-145">Dans **Revenir à votre compte**, tapez un nouveau mot de passe pour le compte utilisateur 3, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="46262-145">In **Get back into your account**, type a new password for the User 3 account, and then click **Finish**.</span></span> <span data-ttu-id="46262-146">Notez le mot de passe modifié du compte d’utilisateur 3 et stockez-le dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="46262-146">Note the changed password of the User 3 account and store it in a safe location.</span></span>
12. <span data-ttu-id="46262-147">Dans un onglet distinct du même navigateur, accédez à [https://portal.office.com](https://portal.office.com), puis connectez-vous avec le nom de compte Utilisateur 3 et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="46262-147">In a separate tab of the same browser, go to [https://portal.office.com](https://portal.office.com), and then sign in with the User 3 account name and its new password.</span></span> <span data-ttu-id="46262-148">Vous devez voir la **page d’accueil Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="46262-148">You should see the **Microsoft Office Home** page.</span></span>

## <a name="next-step"></a><span data-ttu-id="46262-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="46262-149">Next step</span></span>

<span data-ttu-id="46262-150">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="46262-150">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="46262-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46262-151">See also</span></span>

[<span data-ttu-id="46262-152">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="46262-152">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="46262-153">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="46262-153">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="46262-154">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="46262-154">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
