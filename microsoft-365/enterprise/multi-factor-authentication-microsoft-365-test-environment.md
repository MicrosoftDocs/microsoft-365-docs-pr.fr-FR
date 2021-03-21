---
title: Authentification multifacteur de l’environnement de test Microsoft 365 pour entreprise
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
description: Configurez l’authentification multifacteur à l’aide de messages texte envoyés à un smartphone dans votre environnement de test Microsoft 365 pour entreprise.
ms.openlocfilehash: aeb8940a9499909b8c568d1230f9aa45aee07b3d
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50923755"
---
# <a name="multi-factor-authentication-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="9c4ee-103">Authentification multifacteur pour votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9c4ee-103">Multi-factor authentication for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="9c4ee-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="9c4ee-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="9c4ee-105">Pour un niveau de sécurité supplémentaire pour la connexion à Microsoft 365 ou à tout service ou application qui utilise le client Azure AD pour votre abonnement, vous pouvez activer l’authentification multifacteur Azure AD, qui nécessite plus qu’un simple nom d’utilisateur et mot de passe pour vérifier un compte.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-105">For an additional level of security for signing in to Microsoft 365 or any service or application that uses the Azure AD tenant for your subscription, you can enable Azure AD multi-factor authentication, which requires more than just a username and password to verify an account.</span></span>

<span data-ttu-id="9c4ee-106">Avec l’authentification multifacteur, les utilisateurs doivent confirmer un appel téléphonique, taper un code de vérification envoyé dans un SMS ou vérifier l’authentification avec une application sur leur smartphone après avoir entré correctement leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-106">With multi-factor authentication, users are required to acknowledge a phone call, type a verification code sent in a text message, or verify the authentication with an app on their smart phones after correctly entering their passwords.</span></span> <span data-ttu-id="9c4ee-107">Ils ne peuvent se connecter qu’une fois que ce deuxième facteur d’authentification est satisfait.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-107">They can sign in only after this second authentication factor is satisfied.</span></span>
  
<span data-ttu-id="9c4ee-108">Cet article explique comment activer et tester l’authentification par SMS pour un compte d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-108">This article describes how to enable and test text message-based authentication for a specific user account.</span></span>
  
<span data-ttu-id="9c4ee-109">La configuration de l’authentification multifacteur pour un compte dans votre environnement de test Microsoft 365 pour entreprise implique deux phases et une troisième phase facultative :</span><span class="sxs-lookup"><span data-stu-id="9c4ee-109">Setting up multi-factor authentication for an account in your Microsoft 365 for enterprise test environment involves two phases and a third optional phase:</span></span>
- [<span data-ttu-id="9c4ee-110">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9c4ee-110">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="9c4ee-111">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="9c4ee-111">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>](#phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account)
- [<span data-ttu-id="9c4ee-112">Phase 3 : Activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="9c4ee-112">Phase 3: Enable and test multi-factor authentication with a conditional access policy</span></span>](#phase-3-enable-and-test-multi-factor-authentication-with-a-conditional-access-policy)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="9c4ee-114">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="9c4ee-114">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="9c4ee-115">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9c4ee-115">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="9c4ee-116">Si vous souhaitez simplement tester l’authentification multifacteur de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="9c4ee-116">If you just want to test multi-factor authentication in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="9c4ee-117">Si vous souhaitez tester l’authentification multifacteur dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="9c4ee-117">If you want to test multi-factor authentication in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9c4ee-118">Le test de l’authentification multifacteur ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="9c4ee-118">Testing multi-factor authentication does not require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="9c4ee-119">Il est proposé comme option dans cet article afin que vous puissiez tester l’authentification multifacteur et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-119">It is provided here as an option so that you can test multi-factor authentication and experiment with it in an environment that represents a typical organization.</span></span>
  
## <a name="phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account"></a><span data-ttu-id="9c4ee-120">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="9c4ee-120">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>

<span data-ttu-id="9c4ee-121">Activez l’authentification multifacteur pour le compte d’utilisateur 2 en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9c4ee-121">Enable multi-factor authentication for the User 2 account with these steps:</span></span>
  
1. <span data-ttu-id="9c4ee-122">Ouvrez une instance privée distincte de votre navigateur, allez dans le Centre d’administration Microsoft 365 ( ), puis connectez-vous avec votre [https://portal.microsoft.com](https://portal.microsoft.com) compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-122">Open a separate, private instance of your browser, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)), and then sign in with your global administrator account.</span></span>
    
2. <span data-ttu-id="9c4ee-123">Dans le navigation de gauche, sélectionnez **Utilisateurs**  >  **actifs.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-123">In the left navigation, select **Users** > **Active users**.</span></span>
    
3. <span data-ttu-id="9c4ee-124">Dans le volet Utilisateurs actifs, sélectionnez **Authentification multifacteur.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-124">In the Active users pane, select **Multi-factor authentication**.</span></span>
    
4. <span data-ttu-id="9c4ee-125">Dans la liste, sélectionnez le **compte Utilisateur 2.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-125">In the list, select the **User 2** account.</span></span>
    
5. <span data-ttu-id="9c4ee-126">Dans la section **Utilisateur 2,** sous **Étapes rapides,** **sélectionnez Activer**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-126">In the **User 2** section, under **Quick steps**, select **Enable**.</span></span>
    
6. <span data-ttu-id="9c4ee-127">Dans la boîte de dialogue À propos **de l’activation de** l’th plusieurs facteurs, sélectionnez Activer **l’thème multi-facteur.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-127">In the **About enabling multi-factor auth** dialog box, select **Enable multi-factor auth**.</span></span>
    
7. <span data-ttu-id="9c4ee-128">Dans la **boîte de dialogue Mises à jour** réussies, sélectionnez **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-128">In the **Updates successful** dialog box, select **Close**.</span></span>
    
8. <span data-ttu-id="9c4ee-129">Sous l’onglet Centre d’administration **Microsoft 365,** sélectionnez l’icône du compte d’utilisateur dans le coin supérieur droit, puis **sélectionnez Se sortir.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-129">On the **Microsoft 365 admin center** tab, select the user account icon in the upper right, and then select **Sign out**.</span></span>
    
9. <span data-ttu-id="9c4ee-130">Fermez l’instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-130">Close your browser instance.</span></span>
   
<span data-ttu-id="9c4ee-131">Terminez la configuration pour que le compte d’utilisateur 2 utilise un message texte pour la validation et testez-le en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="9c4ee-131">Complete the configuration for the User 2 account to use a text message for validation and test it with these steps:</span></span>
  
1. <span data-ttu-id="9c4ee-132">Ouvrez une nouvelle instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-132">Open a new, private instance of your browser.</span></span>
    
2. <span data-ttu-id="9c4ee-133">Go to the [Microsoft 365 admin center](https://admin.microsoft.com) and sign in with the User 2 account name and password.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-133">Go to the [Microsoft 365 admin center](https://admin.microsoft.com) and sign in with the User 2 account name and password.</span></span>
    
3. <span data-ttu-id="9c4ee-134">Après la signature, vous êtes invité à configurer le compte pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-134">After signing in, you are prompted to set up the account for more information.</span></span> <span data-ttu-id="9c4ee-135">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-135">Select **Next**.</span></span>
    
4. <span data-ttu-id="9c4ee-136">Sur la page **Vérification de sécurité supplémentaire** : </span><span class="sxs-lookup"><span data-stu-id="9c4ee-136">On the **Additional security verification** page:</span></span>
    
   - <span data-ttu-id="9c4ee-137">Sélectionnez le pays ou la région.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-137">Select your country or region.</span></span>
    
   - <span data-ttu-id="9c4ee-138">Entrez le numéro de téléphone du smartphone qui recevra les messages texte.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-138">Enter the phone number of the smart phone that will receive text messages.</span></span>
    
   - <span data-ttu-id="9c4ee-139">In **Method**, select **Send me a code by text message**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-139">In **Method**, select **Send me a code by text message**.</span></span>
    
5. <span data-ttu-id="9c4ee-140">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-140">Select **Next**.</span></span>
    
6. <span data-ttu-id="9c4ee-141">Entrez le code de vérification à partir du message texte reçu sur votre smartphone, puis sélectionnez **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-141">Enter the verification code from the text message received on your smart phone, and then select **Verify**.</span></span>
    
7. <span data-ttu-id="9c4ee-142">On the **Step 3: Keep your existing applications** page, select **Done**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-142">On the **Step 3: Keep your existing applications** page, select **Done**.</span></span>
    
8. <span data-ttu-id="9c4ee-143">Si c’est la première fois que vous vous connectez avec le compte d’utilisateur 2, vous êtes invité à modifier le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-143">If this is the first time you signed in with the User 2 account, you are prompted to change the password.</span></span> <span data-ttu-id="9c4ee-144">Entrez deux fois le mot de passe d’origine et un nouveau mot de passe, puis sélectionnez Mettre à jour le mot **de passe et connectez-vous.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-144">Enter the original password and a new password twice, and then select **Update password and sign in**.</span></span> <span data-ttu-id="9c4ee-145">Enregistrez le nouveau mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-145">Record the new password in a secure location.</span></span>
    
    <span data-ttu-id="9c4ee-146">Le portail Office pour l’utilisateur 2 doit s’Microsoft Office **l’onglet** Accueil de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-146">You should see the Office portal for User 2 on the **Microsoft Office Home** tab of your browser.</span></span>

## <a name="phase-3-enable-and-test-multi-factor-authentication-with-a-conditional-access-policy"></a><span data-ttu-id="9c4ee-147">Phase 3 : Activer et tester l’authentification multifacteur avec une stratégie d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="9c4ee-147">Phase 3: Enable and test multi-factor authentication with a conditional access policy</span></span>

<span data-ttu-id="9c4ee-148">*Cette phase ne peut être utilisée que pour un environnement de test Microsoft 365 pour entreprise.*</span><span class="sxs-lookup"><span data-stu-id="9c4ee-148">*This phase can only be used for a Microsoft 365 for enterprise test environment.*</span></span>

<span data-ttu-id="9c4ee-149">Dans cette phase, vous activez l’authentification multifacteur pour le compte Utilisateur 3 à l’aide d’un groupe et d’une stratégie d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-149">In this phase, you enable multi-factor authentication for the User 3 account using a group and a conditional access policy.</span></span>

<span data-ttu-id="9c4ee-150">Ensuite, créez un groupe nommé MFAUsers et ajoutez-y le compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-150">Next, create a new group named MFAUsers and add the User 3 account to it.</span></span>

1. <span data-ttu-id="9c4ee-151">Sous l’onglet Centre d’administration **Microsoft 365,** sélectionnez **Groupes** dans le navigation de gauche, puis **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-151">On the **Microsoft 365 admin center** tab, select **Groups** in the left navigation, and then select **Groups**.</span></span>
2. <span data-ttu-id="9c4ee-152">Sélectionnez **Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-152">Select **Add a group**.</span></span>
3. <span data-ttu-id="9c4ee-153">Dans le **volet Choisir un type de groupe,** sélectionnez **Sécurité,** puis Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-153">In the **Choose a group type** pane, select **Security**, and then select **Next**.</span></span>
4. <span data-ttu-id="9c4ee-154">Dans le **volet Configurer les informations** de base, sélectionnez Créer un groupe, puis **fermez.** </span><span class="sxs-lookup"><span data-stu-id="9c4ee-154">In the **Set up the basics** pane, select **Create group**, and then select **Close**.</span></span>
5. <span data-ttu-id="9c4ee-155">Dans le **volet Révision et fin de l’ajout de** groupes, entrez **MFAUsers,** puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-155">In the **Review and finish adding group** pane, enter **MFAUsers**, and then select **Next**.</span></span>
6. <span data-ttu-id="9c4ee-156">Dans la liste des groupes, sélectionnez le **groupe MFAUsers.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-156">In the list of groups, select the **MFAUsers** group.</span></span>
7. <span data-ttu-id="9c4ee-157">Dans le **volet MFAUsers,** sélectionnez **Membres,** puis **afficher tout et gérer les membres.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-157">In the **MFAUsers** pane, select **Members**, and then select **View all and manage members**.</span></span>
8. <span data-ttu-id="9c4ee-158">Dans le **volet MFAUsers,** sélectionnez Ajouter des **membres,** sélectionnez le compte Utilisateur **3,** puis **enregistrez**  >  **Fermer.**  >  </span><span class="sxs-lookup"><span data-stu-id="9c4ee-158">In the **MFAUsers** pane, select **Add members**, select the **User 3** account, and then select **Save** > **Close** > **Close**.</span></span>

<span data-ttu-id="9c4ee-159">Ensuite, créez une stratégie d’accès conditionnel pour exiger l’authentification multifacteur pour les membres du groupe MFAUsers.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-159">Next, create a conditional access policy to require multifactor authentication for members of the MFAUsers group.</span></span>

1. <span data-ttu-id="9c4ee-160">Dans un nouvel onglet de votre navigateur, allez à [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="9c4ee-160">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="9c4ee-161">Sélectionnez **Accès conditionnel à la sécurité Azure Active Directory.**  >    >  </span><span class="sxs-lookup"><span data-stu-id="9c4ee-161">Select **Azure Active Directory** > **Security** > **Conditional Access**.</span></span>
3. <span data-ttu-id="9c4ee-162">Dans le **volet Accès conditionnel – Stratégies,** sélectionnez **Nouvelle stratégie.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-162">In the **Conditional access – Policies** pane, select **New policy**.</span></span>
4. <span data-ttu-id="9c4ee-163">Dans le **volet Nouveau,** entrez **l’mf pour les comptes d’utilisateurs** dans la **zone** Nom.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-163">In the **New** pane, enter **MFA for user accounts** in the **Name** box.</span></span>
5. <span data-ttu-id="9c4ee-164">Dans la section **Affectations,** sélectionnez **Utilisateurs et groupes.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-164">In the **Assignments** section, select **Users and groups**.</span></span>
6. <span data-ttu-id="9c4ee-165">Dans **l’onglet**  Inclure du volet Utilisateurs et groupes, sélectionnez Sélectionner des utilisateurs et des groupes   >  **Utilisateurs et**  >  **groupes Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-165">On the **Include** tab of the **Users and groups** pane, select **Select users and groups** > **Users and groups** > **Select**.</span></span>
7. <span data-ttu-id="9c4ee-166">Dans le **volet** Sélectionner, sélectionnez le **groupe MFAUsers,** puis **sélectionnez**  >  **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-166">In the **Select** pane, select the **MFAUsers** group, and then select **Select** > **Done**.</span></span>
8. <span data-ttu-id="9c4ee-167">Dans la section **Contrôles d’accès** du **nouveau** volet, sélectionnez **Accorder**.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-167">In the **Access controls** section of the **New** pane, select **Grant**.</span></span>
9. <span data-ttu-id="9c4ee-168">Dans le **volet Accorder,** sélectionnez Exiger **l’authentification multifacteur,** puis **sélectionnez Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-168">In the **Grant** pane, select **Require multi-factor authentication**, and then select **Select**.</span></span>
10. <span data-ttu-id="9c4ee-169">Dans le **volet** Nouveau, sélectionnez **Activer** pour **activer** la stratégie, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-169">In the **New** pane, select **On** for **Enable policy**, and then select **Create**.</span></span>
11. <span data-ttu-id="9c4ee-170">Fermez **les onglets du portail Azure** et du Centre d’administration Microsoft **365.**</span><span class="sxs-lookup"><span data-stu-id="9c4ee-170">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="9c4ee-171">Pour tester cette stratégie, connectez-vous avec le compte Utilisateur 3.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-171">To test this policy, sign out and sign in with the User 3 account.</span></span> <span data-ttu-id="9c4ee-172">Vous devez être invité à configurer l’mf.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-172">You should be prompted to configure MFA.</span></span> <span data-ttu-id="9c4ee-173">Cela montre que la stratégie MFAUsers est appliquée.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-173">This demonstrates that the MFAUsers policy is being applied.</span></span>

## <a name="next-step"></a><span data-ttu-id="9c4ee-174">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9c4ee-174">Next step</span></span>

<span data-ttu-id="9c4ee-175">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="9c4ee-175">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c4ee-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c4ee-176">See also</span></span>

[<span data-ttu-id="9c4ee-177">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="9c4ee-177">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="9c4ee-178">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="9c4ee-178">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="9c4ee-179">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="9c4ee-179">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="9c4ee-180">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9c4ee-180">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)