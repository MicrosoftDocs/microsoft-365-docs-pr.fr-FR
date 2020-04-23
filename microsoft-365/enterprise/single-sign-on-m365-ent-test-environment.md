---
title: Authentification unique transparente Azure AD pour votre environnement de test Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/21/2019
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
description: 'Résumé : Configurez et testez l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: ba3f943a53f05c452a8e01e40bb6924dc42a866e
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43636867"
---
# <a name="azure-ad-seamless-single-sign-on-for-your-microsoft-365-test-environment"></a><span data-ttu-id="35453-103">Authentification unique transparente Azure AD pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="35453-103">Azure AD Seamless Single Sign-on for your Microsoft 365 test environment</span></span>

<span data-ttu-id="35453-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="35453-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="35453-p101">L’authentification unique (SSO) transparente Azure AD connecte automatiquement les utilisateurs quand ils sont sur un PC ou un appareil connecté au réseau de leur organisation. L’authentification unique transparente Azure AD permet aux utilisateurs d’accéder facilement aux applications informatiques sans avoir besoin de composants locaux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="35453-p101">Azure AD Seamless Single Sign-On (SSO) automatically signs in users when they are on their PCs or devices that are connected to their organization network. Azure AD Seamless SSO provides users with easy access to cloud-based applications without needing any additional on-premises components.</span></span>

<span data-ttu-id="35453-107">Cet article décrit comment configurer l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="35453-107">This article describes how you can configure your Microsoft 365 test environment for Azure AD Seamless SSO.</span></span>

<span data-ttu-id="35453-108">Il existe deux phases de configuration :</span><span class="sxs-lookup"><span data-stu-id="35453-108">There are two phases to setting this up:</span></span>

1.    <span data-ttu-id="35453-109">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="35453-109">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.    <span data-ttu-id="35453-110">Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="35453-110">Configure Azure AD Connect on APP1 for Azure AD Seamless SSO.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="35453-112">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="35453-112">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="35453-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="35453-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="35453-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="35453-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="35453-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="35453-117">This configuration consists of:</span></span> 
  
- <span data-ttu-id="35453-118">Abonnements d’évaluation ou payants Microsoft 365 E5 ou Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="35453-118">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="35453-119">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="35453-119">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="35453-120">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine Active Directory Domain Services (AD DS) TESTLAB avec le client Azure AD de votre abonnement Microsoft 365 de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="35453-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Microsoft 365 subscription periodically.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso"></a><span data-ttu-id="35453-121">Phase 2 : Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="35453-121">Phase 2: Configure Azure AD Connect on APP1 for Azure AD Seamless SSO</span></span>

<span data-ttu-id="35453-122">Durant cette phase, vous allez configurer Azure AD Connect sur APP1 pour qu’il utilise l’authentification unique transparente Azure AD, puis vérifier que tout fonctionne.</span><span class="sxs-lookup"><span data-stu-id="35453-122">In this phase, you configure Azure AD Connect on APP1 for Azure AD Seamless SSO, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="35453-123">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="35453-123">Configure Azure AD Connect on APP1</span></span>

1. <span data-ttu-id="35453-124">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="35453-124">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="35453-125">Sur le bureau d’APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="35453-125">From the desktop of APP1, run Azure AD Connect.</span></span>

3. <span data-ttu-id="35453-126">Sur la page**Bienvenue**, cliquez sur**Configurer**.</span><span class="sxs-lookup"><span data-stu-id="35453-126">On the **Welcome page**, click **Configure**.</span></span>

4. <span data-ttu-id="35453-127">Sur la page **Tâches supplémentaires**, cliquez sur **Modifier la connexion utilisateur**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="35453-127">On the **Additional tasks** page, click **Change user sign-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="35453-128">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="35453-128">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6. <span data-ttu-id="35453-129">Sur la page **Connexion utilisateur**, sélectionnez **Activer l’authentification unique**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="35453-129">On the **User sign-in** page, select **Enable single sign-on**, and then click **Next**.</span></span>

7. <span data-ttu-id="35453-130">Sur la page **Activer l’authentification unique**, cliquez sur **Entrer les informations d’identification**.</span><span class="sxs-lookup"><span data-stu-id="35453-130">On the **Enable single sign-on** page, click **Enter credentials**.</span></span>

8. <span data-ttu-id="35453-p103">Dans la boîte de dialogue **Sécurité Windows**, tapez **user1** et le mot de passe du compte Utilisateur1, puis cliquez sur **OK**. Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="35453-p103">In the **Windows Security** dialog box, type **user1** and the password of the user1 account, and then click **OK**. Click **Next**.</span></span>

9. <span data-ttu-id="35453-133">Sur la page **Prêt à configurer**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="35453-133">On the **Ready to Configure** page, click **Configure**.</span></span>

10. <span data-ttu-id="35453-134">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="35453-134">On the **Configuration complete** page, click **Exit**.</span></span>

11. <span data-ttu-id="35453-p104">Sur le Portail Azure, dans le volet gauche, cliquez sur **Azure Active Directory > Azure AD Connect**. Vérifiez que la fonctionnalité **Authentification unique transparente** affiche l’état **Activé**.</span><span class="sxs-lookup"><span data-stu-id="35453-p104">From the Azure portal, in the left pane, click **Azure Active Directory > Azure AD Connect**. Verify that the **Seamless single sign-on** feature appears as **Enabled**.</span></span>

<span data-ttu-id="35453-137">Vérifiez ensuite si vous pouvez vous connecter à votre abonnement avec le nom d’utilisateur <strong>utilisateur1@testlab.</strong>\<votre domaine public> du compte Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="35453-137">Next, test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<your public domain> user name of the User1 account.</span></span>

1. <span data-ttu-id="35453-138">Dans Internet Explorer sur APP1, cliquez sur l’icône Paramètres, puis cliquez sur **Options Internet**.</span><span class="sxs-lookup"><span data-stu-id="35453-138">From Internet Explorer on APP1, click the settings icon, and then click **Internet Options**.</span></span>
 
2. <span data-ttu-id="35453-139">Dans **Options Internet**, cliquez sur l’onglet **Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="35453-139">In **Internet Options**, click the **Security** tab.</span></span>

3. <span data-ttu-id="35453-140">Cliquez sur **Intranet local**, puis sur **Sites**.</span><span class="sxs-lookup"><span data-stu-id="35453-140">Click **Local intranet**, and then click **Sites**.</span></span>

4. <span data-ttu-id="35453-141">Dans **Intranet Local**, cliquez sur **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="35453-141">In **Local intranet**, click **Advanced**.</span></span>

5. <span data-ttu-id="35453-142">Dans **Ajouter ce site web à la zone**, tapez **https<span>://</span>autologon.microsoftazuread-sso.com**, cliquez sur **Ajouter > Fermer > OK > OK**.</span><span class="sxs-lookup"><span data-stu-id="35453-142">In **Add this website to the zone**, type **https<span>://</span>autologon.microsoftazuread-sso.com**, click **Add > Close > OK > OK**.</span></span>

6. <span data-ttu-id="35453-143">Déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="35453-143">Sign out, and then sign in again, this time specifying a different account.</span></span>

7. <span data-ttu-id="35453-144">Lorsque vous êtes invité à vous connecter, spécifiez<strong>user1@testlab.</strong>\<votre domaine public > nom, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="35453-144">When prompted to sign in, specify <strong>user1@testlab.</strong>\<your public domain> name, and then click **Next**.</span></span> <span data-ttu-id="35453-145">Vous devez correctement vous connecter en tant que User1 sans entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="35453-145">You should successfully sign in as User1 without being prompted for a password.</span></span> <span data-ttu-id="35453-146">Cela prouve qu’ Azure AD transparente SSO fonctionne.</span><span class="sxs-lookup"><span data-stu-id="35453-146">This proves that Azure AD Seamless SSO is working.</span></span>

<span data-ttu-id="35453-147">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général pour Azure AD.</span><span class="sxs-lookup"><span data-stu-id="35453-147">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator for Azure AD.</span></span> <span data-ttu-id="35453-148">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="35453-148">Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="35453-149">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="35453-149">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)

 
<span data-ttu-id="35453-151">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="35453-151">This configuration consists of:</span></span>

- <span data-ttu-id="35453-152">Les abonnements à la version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="35453-152">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain testlab.\<your domain name> registered.</span></span>
- <span data-ttu-id="35453-153">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="35453-153">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="35453-154">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de votre abonnement Microsoft 365 au domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="35453-154">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Microsoft 365 subscription to the TESTLAB AD DS domain.</span></span> 
- <span data-ttu-id="35453-155">L’authentification unique transparente Azure AD est activée pour permettre aux ordinateurs sur l’intranet simulé de se connecter aux ressources cloud Microsoft 365 sans avoir à spécifier le mot de passe du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35453-155">Azure AD Seamless SSO is enabled so that computers on the simulated intranet can sign in to Microsoft 365 cloud resources without specifing a user account password.</span></span>

<span data-ttu-id="35453-156">Consultez l’étape [Simplifier la connexion de l’utilisateur](identity-secure-your-passwords.md#identity-sso) de la phase d’identité pour obtenir des informations et des liens pour configurer l’authentification unique transparente Azure AD en production.</span><span class="sxs-lookup"><span data-stu-id="35453-156">See the [Simplify user sign-in](identity-secure-your-passwords.md#identity-sso) step in the Identity phase for information and links to configure Azure AD Seamless SSO in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="35453-157">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="35453-157">Next step</span></span>

<span data-ttu-id="35453-158">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="35453-158">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="35453-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35453-159">See also</span></span>

[<span data-ttu-id="35453-160">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="35453-160">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="35453-161">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="35453-161">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="35453-162">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="35453-162">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


