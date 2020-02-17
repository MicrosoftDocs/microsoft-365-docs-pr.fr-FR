---
title: Authentification multifacteur pour votre environnement de test Microsoft 365 Enterprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Configurez l’authentification multifacteur à l’aide de messages texte envoyés à un téléphone intelligent dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: ea2041a463b224781df101251dab0f4d9f0e8753
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42066731"
---
# <a name="multi-factor-authentication-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="8334d-103">Authentification multifacteur pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="8334d-103">Multi-factor authentication for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="8334d-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="8334d-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="8334d-105">Pour un niveau de sécurité supplémentaire pour la connexion à Microsoft 365 ou tout service ou application qui utilise le client Azure AD pour votre abonnement, vous pouvez activer l’authentification multifacteur Azure, qui nécessite plus qu’un nom d’utilisateur et un mot de passe pour vérifier une comptes.</span><span class="sxs-lookup"><span data-stu-id="8334d-105">For an additional level of security for signing in to Microsoft 365 or any service or application that uses the Azure AD tenant for your subscription, you can enable Azure multi-factor authentication, which requires more than just a username and password to verify an account.</span></span> 

<span data-ttu-id="8334d-106">Avec l’authentification multifacteur, les utilisateurs doivent accuser réception d’un appel téléphonique, taper un code de vérification envoyé dans un message texte ou spécifier un mot de passe d’application sur leurs téléphones intelligents après avoir entré correctement leurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="8334d-106">With multi-factor authentication, users are required to acknowledge a phone call, type a verification code sent in a text message, or specify an app password on their smart phones after correctly entering their passwords.</span></span> <span data-ttu-id="8334d-107">Ils peuvent se connecter uniquement lorsque ce deuxième facteur d’authentification a été respecté.</span><span class="sxs-lookup"><span data-stu-id="8334d-107">They can sign in only after this second authentication factor has been satisfied.</span></span> 
  
<span data-ttu-id="8334d-108">Cet article explique comment activer et tester l’authentification par message texte pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8334d-108">This article describes how to enable and test text message-based authentication for a specific user account.</span></span>
  
<span data-ttu-id="8334d-109">Il existe deux phases de configuration de l’authentification multifacteur pour un compte dans votre environnement de test Microsoft 365 entreprise :</span><span class="sxs-lookup"><span data-stu-id="8334d-109">There are two phases to setting up multi-factor authentication for an account in your Microsoft 365 Enterprise test environment:</span></span>
  
1. <span data-ttu-id="8334d-110">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8334d-110">Create the Microsoft 365 Enterprise test environment.</span></span>
    
2. <span data-ttu-id="8334d-111">Activez et testez l’authentification multifacteur pour le compte d’utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="8334d-111">Enable and test multi-factor authentication for the User 2 account.</span></span>

3. <span data-ttu-id="8334d-112">Activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel (facultatif).</span><span class="sxs-lookup"><span data-stu-id="8334d-112">Enable and test multi-factor authentication with a conditional access policy (optional).</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="8334d-114">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8334d-114">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="8334d-115">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="8334d-115">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="8334d-116">Si vous souhaitez simplement tester l’authentification multifacteur d’une façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="8334d-116">If you just want to test multi-factor authentication in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="8334d-117">Si vous souhaitez tester l’authentification multifacteur dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8334d-117">If you want to test multi-factor authentication in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8334d-118">Le test de l’authentification multifacteur ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="8334d-118">Testing multi-factor authentication does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="8334d-119">Il est proposé comme option dans cet article afin que vous puissiez tester l’authentification multifacteur et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="8334d-119">It is provided here as an option so that you can test multi-factor authentication and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account"></a><span data-ttu-id="8334d-120">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="8334d-120">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>

<span data-ttu-id="8334d-121">Activez l’authentification multifacteur pour le compte d’utilisateur 2 en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="8334d-121">Enable multi-factor authentication for the User 2 account with these steps:</span></span>
  
1. <span data-ttu-id="8334d-122">Ouvrez une instance distincte privée de votre navigateur, accédez au centre d’administration 365 de Microsoft ([https://portal.microsoft.com](https://portal.microsoft.com)), puis connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="8334d-122">Open a separate, private instance of your browser, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)), and then sign in with your global administrator account.</span></span>
    
2. <span data-ttu-id="8334d-123">Dans la navigation de gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="8334d-123">In the left navigation, click **Users > Active users**.</span></span>
    
3. <span data-ttu-id="8334d-124">Dans le volet utilisateurs actifs, cliquez sur **authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="8334d-124">In the Active users pane, click **Multi-factor authentication**.</span></span>
    
4. <span data-ttu-id="8334d-125">Dans la liste, sélectionnez le compte **utilisateur 2** .</span><span class="sxs-lookup"><span data-stu-id="8334d-125">In the list, select the **User 2** account.</span></span>
    
5. <span data-ttu-id="8334d-126">Dans la section **Utilisateur 2**, sous **Étapes rapides**, cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="8334d-126">In the **User 2** section, under **Quick steps**, click **Enable**.</span></span>
    
6. <span data-ttu-id="8334d-127">Dans la boîte de dialogue **À propos de l’activation de l’authentification multifacteur**, cliquez sur **Activer Multi-Factor Authentication**.</span><span class="sxs-lookup"><span data-stu-id="8334d-127">In the **About enabling multi-factor auth** dialog box, click **Enable multi-factor auth**.</span></span>
    
7. <span data-ttu-id="8334d-128">Dans la boîte de dialogue **mises à jour réussies** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8334d-128">In the **Updates successful** dialog box, click **Close**.</span></span>
    
8. <span data-ttu-id="8334d-129">Dans l’onglet **Centre d’administration Microsoft 365** , cliquez sur l’icône du compte d’utilisateur dans le coin supérieur droit, puis cliquez sur **déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="8334d-129">On the **Microsoft 365 admin center** tab, click the user account icon in the upper right, and then click **Sign out**.</span></span>
    
9. <span data-ttu-id="8334d-130">Fermez l’instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="8334d-130">Close your browser instance.</span></span>
   
<span data-ttu-id="8334d-131">Terminez la configuration pour que le compte d’utilisateur 2 utilise un message texte pour la validation et testez-le en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="8334d-131">Complete the configuration for the User 2 account to use a text message for validation and test it with these steps:</span></span>
  
1. <span data-ttu-id="8334d-132">Ouvrez une nouvelle instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="8334d-132">Open a new, private instance of your browser.</span></span>
    
2. <span data-ttu-id="8334d-133">Accédez au portail Office 365 ([https://portal.office.com](https://portal.office.com)) et connectez-vous avec le nom de compte et le mot de passe de l’utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="8334d-133">Go to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) and sign in with the User 2 account name and password.</span></span>
    
3. <span data-ttu-id="8334d-134">Une fois connecté, vous êtes invité à configurer le compte pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="8334d-134">After signing in, you are prompted to set up the account for more information.</span></span> <span data-ttu-id="8334d-135">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8334d-135">Click **Next**.</span></span>
    
4. <span data-ttu-id="8334d-136">Sur la page **Vérification de sécurité supplémentaire** : </span><span class="sxs-lookup"><span data-stu-id="8334d-136">On the **Additional security verification** page:</span></span>
    
   - <span data-ttu-id="8334d-137">Sélectionnez le pays ou la région.</span><span class="sxs-lookup"><span data-stu-id="8334d-137">Select your country or region.</span></span>
    
   - <span data-ttu-id="8334d-138">Tapez le numéro de téléphone du smartphone qui recevra les SMS.</span><span class="sxs-lookup"><span data-stu-id="8334d-138">Type phone number of the smart phone that will receive text messages.</span></span>
    
   - <span data-ttu-id="8334d-139">Dans **méthode**, cliquez sur **m’envoyer un code par message texte**.</span><span class="sxs-lookup"><span data-stu-id="8334d-139">In **Method**, click **Send me a code by text message**.</span></span>
    
5. <span data-ttu-id="8334d-140">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="8334d-140">Click **Next**.</span></span>
    
6. <span data-ttu-id="8334d-141">Entrez le code de vérification du SMS reçu sur votre smartphone, puis cliquez sur **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="8334d-141">Enter the verification code from the text message received on your smart phone, and then click **Verify**.</span></span>
    
7. <span data-ttu-id="8334d-142">Sur la page **Étape 3 : Conservez la page des applications existantes**, enregistrez le mot de passe de l’application affiché pour le compte d’utilisateur 2 dans un endroit sûr, puis cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="8334d-142">On the **Step 3: Keep your existing applications** page, record the displayed app password for the User 2 account in a secure location, and then click **Done**.</span></span>
    
8. <span data-ttu-id="8334d-p104">Si c’est la première fois que vous vous connectez avec le compte d’utilisateur 2, vous êtes invité à modifier le mot de passe. Tapez le mot de passe d’origine et un nouveau mot de passe à deux reprises, puis cliquez sur **Mettre à jour le mot de passe et se connecter**. Enregistrez le nouveau mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="8334d-p104">If this is the first time you signed in with the User 2 account, you are prompted to change the password. Type the original password and a new password twice, and then click **Update password and sign in**. Record the new password in a secure location.</span></span>
    
    <span data-ttu-id="8334d-146">Vous devriez voir Office Portal pour l’utilisateur 2 sur l’onglet **Accueil Microsoft Office** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="8334d-146">You should see the Office portal for User 2 on the **Microsoft Office Home** tab of your browser.</span></span>

## <a name="phase-3-enable-and-test-multi-factor-authentication-with-a-conditional-access-policy"></a><span data-ttu-id="8334d-147">Phase 3 : activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="8334d-147">Phase 3: Enable and test multi-factor authentication with a conditional access policy</span></span>

<span data-ttu-id="8334d-148">*Cette phase ne peut être utilisée que pour un environnement de test Microsoft 365 Enterprise.*</span><span class="sxs-lookup"><span data-stu-id="8334d-148">*This phase can only be used for a Microsoft 365 Enterprise test environment.*</span></span>

<span data-ttu-id="8334d-149">Dans cette phase, vous activez l’authentification multifacteur pour le compte utilisateur 3 à l’aide d’un groupe et d’une stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="8334d-149">In this phase you enable multi-factor authentication for the User 3 account using a group and a conditional access policy.</span></span>

<span data-ttu-id="8334d-150">Ensuite, créez un groupe nommé MFAUsers et ajoutez-y le compte utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="8334d-150">Next, create a new group named MFAUsers and add the User 3 account to it.</span></span>

1. <span data-ttu-id="8334d-151">Dans l’onglet **Centre d’administration Microsoft 365** , cliquez sur **groupes** dans le volet de navigation de gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="8334d-151">On the **Microsoft 365 admin center** tab, click **Groups** in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="8334d-152">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="8334d-152">Click **Add a group**.</span></span>
3. <span data-ttu-id="8334d-153">Dans le volet **choisir un type de groupe** , sélectionnez **sécurité**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8334d-153">In the **Choose a group type** pane, select **Security**, and then click **Next**.</span></span>
4. <span data-ttu-id="8334d-154">Dans le volet **configurer les concepts de base** , cliquez sur **créer un groupe**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8334d-154">In the **Set up the basics** pane, click **Create group**, and then click **Close**.</span></span>
5. <span data-ttu-id="8334d-155">Dans le volet **vérifier et terminer l’ajout** d’un groupe, tapez **MFAUsers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8334d-155">In the **Review and finish adding group** pane, type **MFAUsers**, and then click **Next**.</span></span>
6. <span data-ttu-id="8334d-156">Dans la liste des groupes, cliquez sur le groupe **MFAUsers** .</span><span class="sxs-lookup"><span data-stu-id="8334d-156">In the list of groups, click the **MFAUsers** group.</span></span>
7. <span data-ttu-id="8334d-157">Dans le volet **MFAUsers** , cliquez sur **membres**, puis sur **Afficher tout et gérer les membres**.</span><span class="sxs-lookup"><span data-stu-id="8334d-157">In the **MFAUsers** pane, click **Members**, and then click **View all and manage members**.</span></span>
8. <span data-ttu-id="8334d-158">Dans le volet **MFAUsers** , cliquez sur **Ajouter des membres**, sélectionnez le compte **utilisateur 3** , puis cliquez sur **Enregistrer > fermer > fermer**.</span><span class="sxs-lookup"><span data-stu-id="8334d-158">In the **MFAUsers** pane, click **Add members**, select the **User 3** account, and then click **Save > Close > Close**.</span></span>

<span data-ttu-id="8334d-159">Ensuite, créez une stratégie d’accès conditionnel pour exiger l’authentification multifacteur pour les membres du groupe MFAUsers.</span><span class="sxs-lookup"><span data-stu-id="8334d-159">Next, create a conditional access policy to require multifactor authentication for members of the MFAUsers group.</span></span>

1. <span data-ttu-id="8334d-160">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="8334d-160">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="8334d-161">Cliquez sur **Azure Active Directory > sécurité > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="8334d-161">Click **Azure Active Directory > Security > Conditional Access**.</span></span>
3. <span data-ttu-id="8334d-162">Dans le volet **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="8334d-162">In the **Conditional access – Policies** pane, click **New policy**.</span></span>
4. <span data-ttu-id="8334d-163">Dans le volet **nouveau** , tapez **MFA pour les comptes d’utilisateur** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="8334d-163">In the **New** pane, type **MFA for user accounts** in **Name**.</span></span>
5. <span data-ttu-id="8334d-164">Dans la section **affectations** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="8334d-164">In the **Assignments** section, click **Users and groups**.</span></span>
6. <span data-ttu-id="8334d-165">Sous l’onglet **inclure** du volet **utilisateurs et groupes** , cliquez sur Sélectionner des utilisateurs et des groupes **> utilisateurs et des groupes > sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="8334d-165">On the **Include** tab of the **Users and groups** pane, click **Select users and groups > Users and groups > Select**.</span></span>
7. <span data-ttu-id="8334d-166">Dans le volet **Sélectionner** , cliquez sur le groupe **MFAUsers** , puis cliquez sur **Sélectionner > terminée**.</span><span class="sxs-lookup"><span data-stu-id="8334d-166">In the **Select** pane, click the **MFAUsers** group, and then click **Select > Done**.</span></span>
8. <span data-ttu-id="8334d-167">Dans la section **contrôles d’accès** du **nouveau** volet, cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="8334d-167">In the **Access controls** section of the **New** pane, click **Grant**.</span></span>
9. <span data-ttu-id="8334d-168">Dans le volet **accorder** , cliquez sur **exiger l’authentification multifacteur**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="8334d-168">In the **Grant** pane, click **Require multi-factor authentication**, and then click **Select**.</span></span>
10. <span data-ttu-id="8334d-169">Dans le volet **nouveau** , cliquez sur **activé** pour **activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="8334d-169">In the **New** pane, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="8334d-170">Fermez les onglets **portail Azure** et **Centre d’administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="8334d-170">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="8334d-171">Pour tester cette stratégie, déconnectez-vous, puis connectez-vous avec le compte utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="8334d-171">To test this policy, sign out and sign in with the User 3 account.</span></span> <span data-ttu-id="8334d-172">Vous devez être invité à configurer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="8334d-172">You should be prompted to configure MFA.</span></span> <span data-ttu-id="8334d-173">Cela illustre l’application de la stratégie MFAUsers.</span><span class="sxs-lookup"><span data-stu-id="8334d-173">This demonstrates that the MFAUsers policy is being applied.</span></span>

<span data-ttu-id="8334d-174">Consultez l’étape de configuration de l' [authentification multifacteur](identity-secure-user-sign-ins.md#identity-mfa) dans la phase d’identité pour obtenir des informations et des liens permettant de déployer l’authentification multifacteur en production.</span><span class="sxs-lookup"><span data-stu-id="8334d-174">See the [Set up multi-factor authentication](identity-secure-user-sign-ins.md#identity-mfa) step in the Identity phase for information and links to deploy multi-factor authentication in production.</span></span>
    
## <a name="next-step"></a><span data-ttu-id="8334d-175">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="8334d-175">Next step</span></span>

<span data-ttu-id="8334d-176">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="8334d-176">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="8334d-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8334d-177">See also</span></span>

[<span data-ttu-id="8334d-178">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="8334d-178">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="8334d-179">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8334d-179">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="8334d-180">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8334d-180">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="8334d-181">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="8334d-181">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
