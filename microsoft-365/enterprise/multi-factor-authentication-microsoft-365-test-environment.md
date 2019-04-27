---
title: Authentification multifacteur pour votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: ConFigurez l'authentification multifacteur à l'aide de messages texte envoyés à un téléphone intelligent dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: ab346934ea639e819e4e45dd6560093629ee9cde
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33353176"
---
# <a name="multi-factor-authentication-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="1dea5-103">Authentification multifacteur pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1dea5-103">Multi-factor authentication for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="1dea5-104">Pour un niveau de sécurité supplémentaire pour la connexion à Office 365 ou tout service ou application qui utilise le client Azure AD pour votre organisation, vous pouvez activer l'authentification multifacteur Azure, qui nécessite plus qu'un nom d'utilisateur et un mot de passe pour vérifier une comptes.</span><span class="sxs-lookup"><span data-stu-id="1dea5-104">For an additional level of security for signing in to Office 365 or any service or application that uses the Azure AD tenant for your organization, you can enable Azure multi-factor authentication, which requires more than just a username and password to verify an account.</span></span> <span data-ttu-id="1dea5-105">Avec l'authentification multifacteur, les utilisateurs doivent accuser réception d'un appel téléphonique, taper un code de vérification envoyé dans un message texte ou spécifier un mot de passe d'application sur leurs téléphones intelligents après avoir entré correctement leurs mots de passe.</span><span class="sxs-lookup"><span data-stu-id="1dea5-105">With multi-factor authentication, users are required to acknowledge a phone call, type a verification code sent in a text message, or specify an app password on their smart phones after correctly entering their passwords.</span></span> <span data-ttu-id="1dea5-106">Ils peuvent se connecter uniquement lorsque ce deuxième facteur d’authentification a été respecté.</span><span class="sxs-lookup"><span data-stu-id="1dea5-106">They can sign in only after this second authentication factor has been satisfied.</span></span> 
  
<span data-ttu-id="1dea5-107">Cet article explique comment activer et tester l'authentification par message texte pour un compte spécifique.</span><span class="sxs-lookup"><span data-stu-id="1dea5-107">This article describes how to enable and test text message-based authentication for a specific account.</span></span>
  
<span data-ttu-id="1dea5-108">Il existe deux phases de configuration de l'authentification multifacteur pour un compte dans votre environnement de test Microsoft 365 entreprise:</span><span class="sxs-lookup"><span data-stu-id="1dea5-108">There are two phases to setting up multi-factor authentication for an account in your Microsoft 365 Enterprise test environment:</span></span>
  
1. <span data-ttu-id="1dea5-109">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1dea5-109">Create the Microsoft 365 Enterprise test environment.</span></span>
    
2. <span data-ttu-id="1dea5-110">Activez et testez l’authentification multifacteur pour le compte d’utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="1dea5-110">Enable and test multi-factor authentication for the User 2 account.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="1dea5-112">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="1dea5-112">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="1dea5-113">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="1dea5-113">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="1dea5-114">Si vous souhaitez simplement tester l'authentification multifacteur d'une façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="1dea5-114">If you just want to test multi-factor authentication in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="1dea5-115">Si vous souhaitez tester l'authentification multifacteur dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1dea5-115">If you want to test multi-factor authentication in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1dea5-116">Le test de l'authentification multifacteur ne nécessite pas l'environnement de test d'entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d'annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="1dea5-116">Testing multi-factor authentication does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="1dea5-117">Il est proposé comme option dans cet article afin que vous puissiez tester l’authentification multifacteur et faire des essais dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="1dea5-117">It is provided here as an option so that you can test multi-factor authentication and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-enable-and-test-multi-factor-authentication-for-the-user-2-account"></a><span data-ttu-id="1dea5-118">Phase 2 : Activer et tester l’authentification multifacteur pour le compte d’utilisateur 2</span><span class="sxs-lookup"><span data-stu-id="1dea5-118">Phase 2: Enable and test multi-factor authentication for the User 2 account</span></span>

<span data-ttu-id="1dea5-119">Activez l’authentification multifacteur pour le compte d’utilisateur 2 en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="1dea5-119">Enable multi-factor authentication for the User 2 account with these steps:</span></span>
  
1. <span data-ttu-id="1dea5-120">Ouvrez une instance distincte privée de votre navigateur, accédez au centre d'administration 365 de Microsoft ([https://portal.microsoft.com](https://portal.microsoft.com)), puis connectez-vous avec votre compte d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="1dea5-120">Open a separate, private instance of your browser, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)), and then sign in with your global administrator account.</span></span>
    
2. <span data-ttu-id="1dea5-121">Dans la navigation de gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-121">In the left navigation, click **Users > Active users**.</span></span>
    
3. <span data-ttu-id="1dea5-122">Dans le volet utilisateurs actifs, cliquez sur **plus d' > d'authentification multifacteur**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-122">In the Active users pane, click **More > Multi-factor authentication setup**.</span></span>
    
4. <span data-ttu-id="1dea5-123">Dans la liste, sélectionnez le compte **utilisateur 2** .</span><span class="sxs-lookup"><span data-stu-id="1dea5-123">In the list, select the **User 2** account.</span></span>
    
5. <span data-ttu-id="1dea5-124">Dans la section **Utilisateur 2**, sous **Étapes rapides**, cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-124">In the **User 2** section, under **Quick steps**, click **Enable**.</span></span>
    
6. <span data-ttu-id="1dea5-125">Dans la boîte de dialogue **À propos de l’activation de l’authentification multifacteur**, cliquez sur **Activer Multi-Factor Authentication**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-125">In the **About enabling multi-factor auth** dialog box, click **Enable multi-factor auth**.</span></span>
    
7. <span data-ttu-id="1dea5-126">Dans la boîte de dialogue **mises à jour réussies** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-126">In the **Updates successful** dialog box, click **Close**.</span></span>
    
8. <span data-ttu-id="1dea5-127">Dans l'onglet **Centre d'administration Microsoft 365** , cliquez sur l'icône du compte d'utilisateur dans le coin supérieur droit, puis cliquez sur Déconnexion. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1dea5-127">On the **Microsoft 365 admin center** tab, click the user account icon in the upper right, and then click **Sign out**.</span></span>
    
9. <span data-ttu-id="1dea5-128">Fermez l’instance de navigateur.</span><span class="sxs-lookup"><span data-stu-id="1dea5-128">Close your browser instance.</span></span>
   
<span data-ttu-id="1dea5-129">Terminez la configuration pour que le compte d’utilisateur 2 utilise un message texte pour la validation et testez-le en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="1dea5-129">Complete the configuration for the User 2 account to use a text message for validation and test it with these steps:</span></span>
  
1. <span data-ttu-id="1dea5-130">Ouvrez une nouvelle instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="1dea5-130">Open a new, private instance of your browser.</span></span>
    
2. <span data-ttu-id="1dea5-131">Accédez au portail Office 365 ([https://portal.office.com](https://portal.office.com)) et connectez-vous avec le nom de compte et le mot de passe de l'utilisateur 2.</span><span class="sxs-lookup"><span data-stu-id="1dea5-131">Go to the Office 365 portal ([https://portal.office.com](https://portal.office.com)) and sign in with the User 2 account name and password.</span></span>
    
3. <span data-ttu-id="1dea5-132">Une fois connecté, vous êtes invité à configurer le compte pour obtenir plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="1dea5-132">After signing in, you are prompted to set up the account for more information.</span></span> <span data-ttu-id="1dea5-133">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-133">Click **Next**.</span></span>
    
4. <span data-ttu-id="1dea5-134">Sur la page **Vérification de sécurité supplémentaire** : </span><span class="sxs-lookup"><span data-stu-id="1dea5-134">On the **Additional security verification** page:</span></span>
    
   - <span data-ttu-id="1dea5-135">Sélectionnez le pays ou la région.</span><span class="sxs-lookup"><span data-stu-id="1dea5-135">Select your country or region.</span></span>
    
   - <span data-ttu-id="1dea5-136">Tapez le numéro de téléphone du smartphone qui recevra les SMS.</span><span class="sxs-lookup"><span data-stu-id="1dea5-136">Type phone number of the smart phone that will receive text messages.</span></span>
    
   - <span data-ttu-id="1dea5-137">Dans **méthode**, cliquez sur **m'envoyer un code par message texte**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-137">In **Method**, click **Send me a code by text message**.</span></span>
    
5. <span data-ttu-id="1dea5-138">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-138">Click **Next**.</span></span>
    
6. <span data-ttu-id="1dea5-139">Entrez le code de vérification du SMS reçu sur votre smartphone, puis cliquez sur **Vérifier**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-139">Enter the verification code from the text message received on your smart phone, and then click **Verify**.</span></span>
    
7. <span data-ttu-id="1dea5-140">Sur la page **Étape 3 : Conservez la page des applications existantes**, enregistrez le mot de passe de l’application affiché pour le compte d’utilisateur 2 dans un endroit sûr, puis cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="1dea5-140">On the **Step 3: Keep your existing applications** page, record the displayed app password for the User 2 account in a secure location, and then click **Done**.</span></span>
    
8. <span data-ttu-id="1dea5-p104">Si c’est la première fois que vous vous connectez avec le compte d’utilisateur 2, vous êtes invité à modifier le mot de passe. Tapez le mot de passe d’origine et un nouveau mot de passe à deux reprises, puis cliquez sur **Mettre à jour le mot de passe et se connecter**. Enregistrez le nouveau mot de passe dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="1dea5-p104">If this is the first time you signed in with the User 2 account, you are prompted to change the password. Type the original password and a new password twice, and then click **Update password and sign in**. Record the new password in a secure location.</span></span>
    
    <span data-ttu-id="1dea5-144">Vous devriez voir Office Portal pour l'utilisateur 2 sur l'onglet **Accueil Microsoft Office** de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="1dea5-144">You should see the Office portal for User 2 on the **Microsoft Office Home** tab of your browser.</span></span>


<span data-ttu-id="1dea5-145">Consultez l'étape de configuration de l' [authentification multifacteur](identity-multi-factor-authentication.md#identity-mfa) dans la phase d'identité pour obtenir des informations et des liens permettant de déployer l'authentification multifacteur en production.</span><span class="sxs-lookup"><span data-stu-id="1dea5-145">See the [Set up multi-factor authentication](identity-multi-factor-authentication.md#identity-mfa) step in the Identity phase for information and links to deploy multi-factor authentication in production.</span></span>
    
## <a name="next-step"></a><span data-ttu-id="1dea5-146">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1dea5-146">Next step</span></span>

<span data-ttu-id="1dea5-147">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="1dea5-147">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dea5-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1dea5-148">See also</span></span>

[<span data-ttu-id="1dea5-149">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="1dea5-149">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="1dea5-150">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1dea5-150">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="1dea5-151">Déploiement d'entreprise Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1dea5-151">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="1dea5-152">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="1dea5-152">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
