---
title: Microsoft 365 pour l’environnement de test d’entreprise Multi-Factor Authentication
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
- seo-marvel-apr2020
description: Configurez l’authentification multifacteur à l’aide de messages texte envoyés à un téléphone intelligent dans votre environnement de test Microsoft 365 pour entreprise.
ms.openlocfilehash: 4c59405c1ce59cafaf0309e2314e5cbfa4eb080a
ms.sourcegitcommit: c1dd5be42fe0c5dcc7c05817c941edd9076febf8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49558441"
---
# <a name="multi-factor-authentication-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="9291a-103">Authentification multifacteur pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="9291a-103">Multi-factor authentication for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="9291a-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="9291a-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="9291a-105">Pour un niveau de sécurité supplémentaire pour la connexion à Microsoft 365 ou tout service ou application qui utilise le client Azure AD pour votre abonnement, vous pouvez activer l’authentification multifacteur Azure AD, qui nécessite plus qu’un nom d’utilisateur et un mot de passe pour vérifier un compte.</span><span class="sxs-lookup"><span data-stu-id="9291a-105">For an additional level of security for signing in to Microsoft 365 or any service or application that uses the Azure AD tenant for your subscription, you can enable Azure AD multi-factor authentication, which requires more than just a username and password to verify an account.</span></span>

<span data-ttu-id="9291a-106">Avec l’authentification multifacteur, les utilisateurs doivent accuser réception d’un appel téléphonique, taper un code de vérification envoyé dans un message texte ou vérifier l’authentification avec une application sur leurs téléphones intelligents après avoir entré correctement leurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="9291a-106">With multi-factor authentication, users are required to acknowledge a phone call, type a verification code sent in a text message, or verify the authentication with an app on their smart phones after correctly entering their passwords.</span></span> <span data-ttu-id="9291a-107">Ils ne peuvent se connecter qu’après la satisfaction de ce deuxième facteur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="9291a-107">They can sign in only after this second authentication factor is satisfied.</span></span>
  
<span data-ttu-id="9291a-108">Cet article explique comment activer et tester l’authentification par message texte pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9291a-108">This article describes how to enable and test text message-based authentication for a specific user account.</span></span>
  
<span data-ttu-id="9291a-109">La configuration de l’authentification multifacteur pour un compte dans votre environnement de test Microsoft 365 pour entreprise implique deux phases et une troisième phase facultative :</span><span class="sxs-lookup"><span data-stu-id="9291a-109">Setting up multi-factor authentication for an account in your Microsoft 365 for enterprise test environment involves two phases and a third optional phase:</span></span>
- [<span data-ttu-id="9291a-110">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="9291a-110">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="9291a-111">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="9291a-111">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>](#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account)
- [<span data-ttu-id="9291a-112">Phase 3 : activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="9291a-112">Phase 3: Enable and test multi-factor authentication with a conditional access policy</span></span>](#phase-3-enable-and-test-multi-factor-authentication-with-a-conditional-access-policy)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="9291a-114">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="9291a-114">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="9291a-115">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="9291a-115">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="9291a-116">Si vous souhaitez simplement tester l’authentification multifacteur d’une façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="9291a-116">If you just want to test multi-factor authentication in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="9291a-117">Si vous souhaitez tester l’authentification multifacteur dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9291a-117">If you want to test multi-factor authentication in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9291a-118">Le test de l’authentification multifacteur ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9291a-118">Testing multi-factor authentication does not require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="9291a-119">Il est proposé comme option dans cet article afin que vous puissiez tester l’authentification multifacteur et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="9291a-119">It is provided here as an option so that you can test multi-factor authentication and experiment with it in an environment that represents a typical organization.</span></span>
  
## <a name="phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account"></a><span data-ttu-id="9291a-120">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="9291a-120">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>

<span data-ttu-id="9291a-121">Activez l’authentification multifacteur pour le compte d’utilisateur 2 en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9291a-121">Enable multi-factor authentication for the User 2 account with these steps:</span></span>
  
1. <span data-ttu-id="9291a-122">Ouvrez une instance distincte privée de votre navigateur, accédez au centre d’administration 365 de Microsoft ( [https://portal.microsoft.com](https://portal.microsoft.com) ), puis connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="9291a-122">Open a separate, private instance of your browser, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)), and then sign in with your global administrator account.</span></span>
    
2. <span data-ttu-id="9291a-123">Dans le volet de navigation de gauche **, sélectionnez utilisateurs**  >  **actifs**.</span><span class="sxs-lookup"><span data-stu-id="9291a-123">In the left navigation, select **Users** > **Active users**.</span></span>
    
3. <span data-ttu-id="9291a-124">Dans le volet utilisateurs actifs, sélectionnez **authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="9291a-124">In the Active users pane, select **Multi-factor authentication**.</span></span>
    
4. <span data-ttu-id="9291a-125">Dans la liste, sélectionnez le compte **utilisateur 2** .</span><span class="sxs-lookup"><span data-stu-id="9291a-125">In the list, select the **User 2** account.</span></span>
    
5. <span data-ttu-id="9291a-126">Dans la section **utilisateur 2** , sous **étapes rapides**, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-126">In the **User 2** section, under **Quick steps**, select **Enable**.</span></span>
    
6. <span data-ttu-id="9291a-127">Dans la boîte de dialogue à propos de l’activation de l' **authentification multifacteur** , sélectionnez **activer l’authentification** multifacteur.</span><span class="sxs-lookup"><span data-stu-id="9291a-127">In the **About enabling multi-factor auth** dialog box, select **Enable multi-factor auth**.</span></span>
    
7. <span data-ttu-id="9291a-128">Dans la boîte de dialogue **mises à jour réussies** , sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-128">In the **Updates successful** dialog box, select **Close**.</span></span>
    
8. <span data-ttu-id="9291a-129">Sous l’onglet **Centre d’administration 365 de Microsoft** , sélectionnez l’icône du compte d’utilisateur dans le coin supérieur droit, puis sélectionnez **déconnexion**.</span><span class="sxs-lookup"><span data-stu-id="9291a-129">On the **Microsoft 365 admin center** tab, select the user account icon in the upper right, and then select **Sign out**.</span></span>
    
9. <span data-ttu-id="9291a-130">Fermez l’instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="9291a-130">Close your browser instance.</span></span>
   
<span data-ttu-id="9291a-131">Terminez la configuration pour que le compte d’utilisateur 2 utilise un message texte pour la validation et testez-le en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9291a-131">Complete the configuration for the User 2 account to use a text message for validation and test it with these steps:</span></span>
  
1. <span data-ttu-id="9291a-132">Ouvrez une nouvelle instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9291a-132">Open a new, private instance of your browser.</span></span>
    
2. <span data-ttu-id="9291a-133">Accédez au [Centre d’administration de Microsoft 365](https://admin.microsoft.com) et connectez-vous avec le nom de compte et le mot de passe de l’utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="9291a-133">Go to the [Microsoft 365 admin center](https://admin.microsoft.com) and sign in with the User 2 account name and password.</span></span>
    
3. <span data-ttu-id="9291a-134">Une fois connecté, vous êtes invité à configurer le compte pour obtenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9291a-134">After signing in, you are prompted to set up the account for more information.</span></span> <span data-ttu-id="9291a-135">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9291a-135">Select **Next**.</span></span>
    
4. <span data-ttu-id="9291a-136">Sur la page **Vérification de sécurité supplémentaire** : </span><span class="sxs-lookup"><span data-stu-id="9291a-136">On the **Additional security verification** page:</span></span>
    
   - <span data-ttu-id="9291a-137">Sélectionnez le pays ou la région.</span><span class="sxs-lookup"><span data-stu-id="9291a-137">Select your country or region.</span></span>
    
   - <span data-ttu-id="9291a-138">Entrez le numéro de téléphone du téléphone intelligent qui recevra les messages texte.</span><span class="sxs-lookup"><span data-stu-id="9291a-138">Enter the phone number of the smart phone that will receive text messages.</span></span>
    
   - <span data-ttu-id="9291a-139">Dans la **méthode**, sélectionnez **m’envoyer un code par message texte**.</span><span class="sxs-lookup"><span data-stu-id="9291a-139">In **Method**, select **Send me a code by text message**.</span></span>
    
5. <span data-ttu-id="9291a-140">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9291a-140">Select **Next**.</span></span>
    
6. <span data-ttu-id="9291a-141">Entrez le code de vérification à partir du message texte reçu sur votre téléphone intelligent, puis sélectionnez **vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9291a-141">Enter the verification code from the text message received on your smart phone, and then select **Verify**.</span></span>
    
7. <span data-ttu-id="9291a-142">Dans la page **étape 3 : conserver votre application existante** , sélectionnez **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-142">On the **Step 3: Keep your existing applications** page, select **Done**.</span></span>
    
8. <span data-ttu-id="9291a-143">Si c’est la première fois que vous vous connectez avec le compte d’utilisateur 2, vous êtes invité à modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9291a-143">If this is the first time you signed in with the User 2 account, you are prompted to change the password.</span></span> <span data-ttu-id="9291a-144">Entrez le mot de passe d’origine et un nouveau mot de passe à deux reprises, puis sélectionnez **mettre à jour le mot de passe et se connecter**.</span><span class="sxs-lookup"><span data-stu-id="9291a-144">Enter the original password and a new password twice, and then select **Update password and sign in**.</span></span> <span data-ttu-id="9291a-145">Enregistrez le nouveau mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="9291a-145">Record the new password in a secure location.</span></span>
    
    <span data-ttu-id="9291a-146">Vous devriez voir Office Portal pour l’utilisateur 2 sur l’onglet **Accueil Microsoft Office** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9291a-146">You should see the Office portal for User 2 on the **Microsoft Office Home** tab of your browser.</span></span>

## <a name="phase-3-enable-and-test-multi-factor-authentication-with-a-conditional-access-policy"></a><span data-ttu-id="9291a-147">Phase 3 : activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="9291a-147">Phase 3: Enable and test multi-factor authentication with a conditional access policy</span></span>

<span data-ttu-id="9291a-148">*Cette phase ne peut être utilisée que pour un environnement de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="9291a-148">*This phase can only be used for a Microsoft 365 for enterprise test environment.*</span></span>

<span data-ttu-id="9291a-149">Dans cette phase, vous activez l’authentification multifacteur pour le compte utilisateur 3 à l’aide d’un groupe et d’une stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="9291a-149">In this phase, you enable multi-factor authentication for the User 3 account using a group and a conditional access policy.</span></span>

<span data-ttu-id="9291a-150">Ensuite, créez un groupe nommé MFAUsers et ajoutez-y le compte utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="9291a-150">Next, create a new group named MFAUsers and add the User 3 account to it.</span></span>

1. <span data-ttu-id="9291a-151">Sous l’onglet **Centre d’administration 365 de Microsoft** , sélectionnez **groupes** dans le volet de navigation de gauche, puis sélectionnez **groupes**.</span><span class="sxs-lookup"><span data-stu-id="9291a-151">On the **Microsoft 365 admin center** tab, select **Groups** in the left navigation, and then select **Groups**.</span></span>
2. <span data-ttu-id="9291a-152">Sélectionnez **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="9291a-152">Select **Add a group**.</span></span>
3. <span data-ttu-id="9291a-153">Dans le volet **choisir un type de groupe** , sélectionnez **sécurité**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9291a-153">In the **Choose a group type** pane, select **Security**, and then select **Next**.</span></span>
4. <span data-ttu-id="9291a-154">Dans le volet **configure the Basics** , sélectionnez **Create Group**, puis **Close**.</span><span class="sxs-lookup"><span data-stu-id="9291a-154">In the **Set up the basics** pane, select **Create group**, and then select **Close**.</span></span>
5. <span data-ttu-id="9291a-155">Dans le volet **vérifier et terminer l’ajout** d’un groupe, entrez **MFAUsers**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9291a-155">In the **Review and finish adding group** pane, enter **MFAUsers**, and then select **Next**.</span></span>
6. <span data-ttu-id="9291a-156">Dans la liste des groupes, sélectionnez le groupe **MFAUsers** .</span><span class="sxs-lookup"><span data-stu-id="9291a-156">In the list of groups, select the **MFAUsers** group.</span></span>
7. <span data-ttu-id="9291a-157">Dans le volet **MFAUsers** , sélectionnez **membres**, puis **Afficher tous et gérer les membres**.</span><span class="sxs-lookup"><span data-stu-id="9291a-157">In the **MFAUsers** pane, select **Members**, and then select **View all and manage members**.</span></span>
8. <span data-ttu-id="9291a-158">Dans le volet **MFAUsers** , sélectionnez **Ajouter des membres**, sélectionnez le compte **utilisateur 3** , puis sélectionnez **Enregistrer**  >  **Fermer**  >  **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-158">In the **MFAUsers** pane, select **Add members**, select the **User 3** account, and then select **Save** > **Close** > **Close**.</span></span>

<span data-ttu-id="9291a-159">Ensuite, créez une stratégie d’accès conditionnel pour exiger l’authentification multifacteur pour les membres du groupe MFAUsers.</span><span class="sxs-lookup"><span data-stu-id="9291a-159">Next, create a conditional access policy to require multifactor authentication for members of the MFAUsers group.</span></span>

1. <span data-ttu-id="9291a-160">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="9291a-160">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="9291a-161">Sélectionnez **Azure Active Directory**  >  **Security**  >  **accès conditionnel** de sécurité Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9291a-161">Select **Azure Active Directory** > **Security** > **Conditional Access**.</span></span>
3. <span data-ttu-id="9291a-162">Dans le volet **accès conditionnel – stratégies** , sélectionnez **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="9291a-162">In the **Conditional access – Policies** pane, select **New policy**.</span></span>
4. <span data-ttu-id="9291a-163">Dans le volet **nouveau** , entrez **MFA pour les comptes d’utilisateur** dans la zone **nom** .</span><span class="sxs-lookup"><span data-stu-id="9291a-163">In the **New** pane, enter **MFA for user accounts** in the **Name** box.</span></span>
5. <span data-ttu-id="9291a-164">Dans la section **affectations** , sélectionnez **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="9291a-164">In the **Assignments** section, select **Users and groups**.</span></span>
6. <span data-ttu-id="9291a-165">Sous l’onglet **inclure** du volet **utilisateurs et groupes** , sélectionnez **Sélectionner des** utilisateurs et des groupes d'  >  **utilisateurs et**  >  **de groupes**.</span><span class="sxs-lookup"><span data-stu-id="9291a-165">On the **Include** tab of the **Users and groups** pane, select **Select users and groups** > **Users and groups** > **Select**.</span></span>
7. <span data-ttu-id="9291a-166">Dans le volet **Sélectionner** , sélectionnez le groupe **MFAUsers** , **puis sélectionnez**  >  **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-166">In the **Select** pane, select the **MFAUsers** group, and then select **Select** > **Done**.</span></span>
8. <span data-ttu-id="9291a-167">Dans la section **contrôles d’accès** du **nouveau** volet, sélectionnez **accorder**.</span><span class="sxs-lookup"><span data-stu-id="9291a-167">In the **Access controls** section of the **New** pane, select **Grant**.</span></span>
9. <span data-ttu-id="9291a-168">Dans le volet **accorder** , sélectionnez **exiger l’authentification multifacteur**, puis sélectionnez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="9291a-168">In the **Grant** pane, select **Require multi-factor authentication**, and then select **Select**.</span></span>
10. <span data-ttu-id="9291a-169">Dans le volet **nouveau** , sélectionnez **activé** pour **activer la stratégie**, puis **créer**.</span><span class="sxs-lookup"><span data-stu-id="9291a-169">In the **New** pane, select **On** for **Enable policy**, and then select **Create**.</span></span>
11. <span data-ttu-id="9291a-170">Fermez les onglets **portail Azure** et **Centre d’administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="9291a-170">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="9291a-171">Pour tester cette stratégie, déconnectez-vous, puis connectez-vous avec le compte utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="9291a-171">To test this policy, sign out and sign in with the User 3 account.</span></span> <span data-ttu-id="9291a-172">Vous devez être invité à configurer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="9291a-172">You should be prompted to configure MFA.</span></span> <span data-ttu-id="9291a-173">Cela illustre l’application de la stratégie MFAUsers.</span><span class="sxs-lookup"><span data-stu-id="9291a-173">This demonstrates that the MFAUsers policy is being applied.</span></span>

## <a name="next-step"></a><span data-ttu-id="9291a-174">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9291a-174">Next step</span></span>

<span data-ttu-id="9291a-175">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="9291a-175">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="9291a-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9291a-176">See also</span></span>

[<span data-ttu-id="9291a-177">Feuille de route d’identité</span><span class="sxs-lookup"><span data-stu-id="9291a-177">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="9291a-178">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="9291a-178">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="9291a-179">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9291a-179">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="9291a-180">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9291a-180">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
