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
ms.openlocfilehash: 5d98dcc50f16bc08da787a928beeeacf825201c9
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487423"
---
# <a name="password-reset-for-your-microsoft-365-test-environment"></a><span data-ttu-id="90a6a-103">Réinitialisation de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="90a6a-103">Password reset for your Microsoft 365 test environment</span></span>

<span data-ttu-id="90a6a-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="90a6a-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="90a6a-105">La réinitialisation de mot de passe en libre-service (SSPR) d’Azure Active Directory (Azure AD) permet aux utilisateurs de réinitialiser ou de déverrouiller leurs mots de passe ou leurs comptes.</span><span class="sxs-lookup"><span data-stu-id="90a6a-105">Azure Active Directory (Azure AD) self-service password reset (SSPR) allows users to reset or unlock their passwords or accounts.</span></span>

<span data-ttu-id="90a6a-106">Cet article explique comment configurer et tester les réinitialisations de mot de passe dans votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="90a6a-106">This article describes how to configure and test password resets in your Microsoft 365 test environment.</span></span>

<span data-ttu-id="90a6a-107">La configuration de SSPR implique trois phases :</span><span class="sxs-lookup"><span data-stu-id="90a6a-107">Setting up SSPR involves three phases:</span></span>
- [<span data-ttu-id="90a6a-108">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="90a6a-108">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>](#phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment)
- [<span data-ttu-id="90a6a-109">Étape 2 : Activation de la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="90a6a-109">Phase 2: Enable password writeback</span></span>](#phase-2-enable-password-writeback)
- [<span data-ttu-id="90a6a-110">Étape 3 : Configuration et test de la réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="90a6a-110">Phase 3: Configure and test password reset</span></span>](#phase-3-configure-and-test-password-reset)
    
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="90a6a-112">Pour obtenir un plan visuel de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="90a6a-112">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="90a6a-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="90a6a-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="90a6a-114">Tout d’abord, suivez les instructions de la synchronisation [de hachage de mot de passe.](password-hash-sync-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="90a6a-114">First, follow the instructions in [password hash synchronization](password-hash-sync-m365-ent-test-environment.md).</span></span> 

<span data-ttu-id="90a6a-115">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="90a6a-115">Your resulting configuration looks like this:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="90a6a-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="90a6a-117">This configuration consists of:</span></span>
  
- <span data-ttu-id="90a6a-118">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="90a6a-118">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="90a6a-119">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="90a6a-119">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>
- <span data-ttu-id="90a6a-120">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB Active Directory Domain Services (AD DS) avec le client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="90a6a-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Microsoft 365 subscription.</span></span>

## <a name="phase-2-enable-password-writeback"></a><span data-ttu-id="90a6a-121">Étape 2 : Activation de la réécriture du mot de passe</span><span class="sxs-lookup"><span data-stu-id="90a6a-121">Phase 2: Enable password writeback</span></span>

<span data-ttu-id="90a6a-122">Suivez les instructions dans [Phase 2 du guide de laboratoire de test de réécriture du mot de passe](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span><span class="sxs-lookup"><span data-stu-id="90a6a-122">Follow the instructions in [Phase 2 of the password writeback Test Lab Guide](password-writeback-m365-ent-test-environment.md#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain).</span></span>

<span data-ttu-id="90a6a-123">La fonction de réécriture du mot de passe doit être activée pour qu’il soit possible d’opérer une réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="90a6a-123">You must have password writeback enabled to use password reset.</span></span>
  
## <a name="phase-3-configure-and-test-password-reset"></a><span data-ttu-id="90a6a-124">Étape 3 : Configuration et test de la réinitialisation de mot de passe</span><span class="sxs-lookup"><span data-stu-id="90a6a-124">Phase 3: Configure and test password reset</span></span>

<span data-ttu-id="90a6a-125">Dans cette phase, configurez la réinitialisation du mot de passe dans le client Azure AD par le biais de l’appartenance à un groupe, puis vérifiez qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="90a6a-125">In this phase, configure password reset in the Azure AD tenant through group membership, and then verify that it works.</span></span>

<span data-ttu-id="90a6a-126">Tout d’abord, activez la réinitialisation de mot de passe pour les comptes d’un groupe Azure AD spécifique.</span><span class="sxs-lookup"><span data-stu-id="90a6a-126">First, enable password reset for the accounts in a specific Azure AD group.</span></span>

1. <span data-ttu-id="90a6a-127">Dans une instance privée de votre navigateur, ouvrez [https://portal.azure.com](https://portal.azure.com), puis connectez-vous avec les informations d’identification de votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="90a6a-127">From a private instance of your browser, open [https://portal.azure.com](https://portal.azure.com), and then sign in with the credentials of your global administrator account.</span></span>
2. <span data-ttu-id="90a6a-128">Dans le portail Azure, sélectionnez **Groupe Groupes Azure Active Directory**  >    >  **Nouveau.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-128">In the Azure portal, select **Azure Active Directory** > **Groups** > **New group**.</span></span>
3. <span data-ttu-id="90a6a-129">Définissez le **Type de groupe** sur **Sécurité**, le **Nom du groupe** sur **PWReset** et le **Type d’appartenance** sur **Affecté**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-129">Set the **Group type** to **Security**, **Group name** to **PWReset**, and the **Membership type** to **Assigned**.</span></span>
4. <span data-ttu-id="90a6a-130">Sélectionnez **Membres,** recherchez et **sélectionnez Utilisateur 3,** **sélectionnez Sélectionner,** puis **créez.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-130">Select **Members**, find and select **User 3**, select **Select**, and then select **Create**.</span></span>
5. <span data-ttu-id="90a6a-131">Fermez le volet **Groupes**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-131">Close the **Groups** pane.</span></span>
6. <span data-ttu-id="90a6a-132">Dans le volet Azure Active  Directory, sélectionnez Réinitialiser le mot de passe dans le volet de navigation gauche.</span><span class="sxs-lookup"><span data-stu-id="90a6a-132">In the Azure Active Directory pane, select **Password reset** in the left navigation.</span></span>
7. <span data-ttu-id="90a6a-133">Sur la page **Propriétés–Réinitialiser le mot de passe**, sous l’option **Réinitialisation du mot de passe en libre-service activée**, choisissez **Sélectionné**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-133">In the **Password reset-Properties** pane, under the option **Self Service Password Reset Enabled**, choose **Selected**.</span></span>
8. <span data-ttu-id="90a6a-134">Sélectionnez **Sélectionner un** groupe, sélectionnez le groupe **PWReset,** puis **sélectionnez**  >  **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-134">Select **Select group**, select the **PWReset** group, and then select **Select** > **Save**.</span></span>
9. <span data-ttu-id="90a6a-135">Fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="90a6a-135">Close the private browser instance.</span></span>

<span data-ttu-id="90a6a-136">Ensuite, testez la réinitialisation du mot de passe pour le compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="90a6a-136">Next, test password reset for the User 3 account.</span></span>

1. <span data-ttu-id="90a6a-137">Ouvrez une nouvelle instance privée du navigateur et accédez à [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span><span class="sxs-lookup"><span data-stu-id="90a6a-137">Open a new private browser instance and browse to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).</span></span>
1. <span data-ttu-id="90a6a-138">Connectez-vous avec les informations d’identification du compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="90a6a-138">Sign in with the User 3 account credentials.</span></span>
1. <span data-ttu-id="90a6a-139">Dans plus **d’informations requises,** sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-139">In **More information required**, select **Next**.</span></span> 
1. <span data-ttu-id="90a6a-140">Dans **Ne perdez pas l’accès à votre compte**, indiquez votre numéro de téléphone portable pour configurer l’authentification par téléphone et votre adresse électronique personnelle ou professionnelle pour configurer l’authentification par adresse électronique.</span><span class="sxs-lookup"><span data-stu-id="90a6a-140">In **Don't lose access to your account**, set the authentication phone to your mobile phone number and the authentication email to your work or personal email account.</span></span>
1. <span data-ttu-id="90a6a-141">Une fois les deux vérifiés, **sélectionnez Apparences,** puis fermez l’instance privée du navigateur.</span><span class="sxs-lookup"><span data-stu-id="90a6a-141">After both are verified, select **Looks good**, and then close the private instance of the browser.</span></span>
1. <span data-ttu-id="90a6a-142">Dans une nouvelle instance de navigateur privé, allez à [https://aka.ms/sspr](https://aka.ms/sspr) .</span><span class="sxs-lookup"><span data-stu-id="90a6a-142">In a new private browser instance, go to [https://aka.ms/sspr](https://aka.ms/sspr).</span></span>
1. <span data-ttu-id="90a6a-143">Entrez le nom du compte Utilisateur 3, entrez les caractères de la CAPTCHA, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-143">Enter the User 3 account name, enter the characters from the CAPTCHA, and then select **Next**.</span></span>
1. <span data-ttu-id="90a6a-144">Pour **l’étape de vérification 1,** sélectionnez **Envoyer un e-mail** à mon courrier de remplacement, puis sélectionnez Courrier **électronique.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-144">For **verification step 1**, select **Email my alternate email**, and then select **Email**.</span></span> <span data-ttu-id="90a6a-145">Lorsque vous recevez l’e-mail, entrez le code de vérification, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-145">When you receive the email, enter the verification code, and then select **Next**.</span></span>
1. <span data-ttu-id="90a6a-146">Dans **Revenir à votre compte,** entrez un nouveau mot de passe pour le compte Utilisateur 3, puis sélectionnez **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="90a6a-146">In **Get back into your account**, enter a new password for the User 3 account, and then select **Finish**.</span></span> <span data-ttu-id="90a6a-147">Notez le mot de passe modifié du compte d’utilisateur 3 et stockez-le dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="90a6a-147">Note the changed password of the User 3 account and store it in a safe location.</span></span>
1. <span data-ttu-id="90a6a-148">Dans un onglet distinct du même navigateur, accédez à [https://portal.office.com](https://portal.office.com), puis connectez-vous avec le nom de compte Utilisateur 3 et son nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="90a6a-148">In a separate tab of the same browser, go to [https://portal.office.com](https://portal.office.com), and then sign in with the User 3 account name and its new password.</span></span> <span data-ttu-id="90a6a-149">Vous devez voir la **page d’accueil Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="90a6a-149">You should see the **Microsoft Office Home** page.</span></span>

## <a name="next-step"></a><span data-ttu-id="90a6a-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="90a6a-150">Next step</span></span>

<span data-ttu-id="90a6a-151">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="90a6a-151">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="90a6a-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90a6a-152">See also</span></span>

[<span data-ttu-id="90a6a-153">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="90a6a-153">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="90a6a-154">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="90a6a-154">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="90a6a-155">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="90a6a-155">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
