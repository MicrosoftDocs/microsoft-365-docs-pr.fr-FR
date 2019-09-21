---
title: Authentification unique transparente Azure AD pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
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
ms.openlocfilehash: 4d62405bc500bdf0dec8aa8aa6639e0802aa232e
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37071563"
---
# <a name="azure-ad-seamless-single-sign-on-for-your-microsoft-365-test-environment"></a><span data-ttu-id="bc349-103">Authentification unique transparente Azure AD pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bc349-103">Azure AD Seamless Single Sign-on for your Microsoft 365 test environment</span></span>

<span data-ttu-id="bc349-p101">L’authentification unique (SSO) transparente Azure AD connecte automatiquement les utilisateurs quand ils sont sur un PC ou un appareil connecté au réseau de leur organisation. L’authentification unique transparente Azure AD permet aux utilisateurs d’accéder facilement aux applications informatiques sans avoir besoin de composants locaux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bc349-p101">Azure AD Seamless Single Sign-On (SSO) automatically signs in users when they are on their PCs or devices that are connected to their organization network. Azure AD Seamless SSO provides users with easy access to cloud-based applications without needing any additional on-premises components.</span></span>

<span data-ttu-id="bc349-106">Cet article décrit comment configurer l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc349-106">This article describes how you can configure your Microsoft 365 test environment for Azure AD Seamless SSO.</span></span>

<span data-ttu-id="bc349-107">Il existe deux phases de configuration :</span><span class="sxs-lookup"><span data-stu-id="bc349-107">There are two phases to setting this up:</span></span>

1.  <span data-ttu-id="bc349-108">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bc349-108">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.  <span data-ttu-id="bc349-109">Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="bc349-109">Configure Azure AD Connect on APP1 for Azure AD Seamless SSO.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="bc349-111">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="bc349-111">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="bc349-112">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bc349-112">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="bc349-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="bc349-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="bc349-116">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="bc349-116">This configuration consists of:</span></span> 
  
- <span data-ttu-id="bc349-117">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="bc349-117">Office 365 E5 and EMS E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="bc349-118">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="bc349-118">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="bc349-119">Azure AD Connect s’exécute sur APP1 pour synchroniser régulièrement le domaine Windows Server AD TESTLAB (Active Directory Domain Services :AD DS) avec le client Azure AD de vos abonnements Office 365 et EMS E5 de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="bc349-119">Azure AD Connect runs on APP1 to synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions periodically.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso"></a><span data-ttu-id="bc349-120">Phase 2 : Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="bc349-120">Phase 2: Configure Azure AD Connect on APP1 for Azure AD Seamless SSO</span></span>

<span data-ttu-id="bc349-121">Durant cette phase, vous allez configurer Azure AD Connect sur APP1 pour qu’il utilise l’authentification unique transparente Azure AD, puis vérifier que tout fonctionne.</span><span class="sxs-lookup"><span data-stu-id="bc349-121">In this phase, you configure Azure AD Connect on APP1 for Azure AD Seamless SSO, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="bc349-122">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="bc349-122">Configure Azure AD Connect on APP1</span></span>

1. <span data-ttu-id="bc349-123">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="bc349-123">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="bc349-124">Sur le bureau d’APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="bc349-124">From the desktop of APP1, run Azure AD Connect.</span></span>

3. <span data-ttu-id="bc349-125">Sur la page**Bienvenue**, cliquez sur**Configurer**.</span><span class="sxs-lookup"><span data-stu-id="bc349-125">On the **Welcome page**, click **Configure**.</span></span>

4. <span data-ttu-id="bc349-126">Sur la page **Tâches supplémentaires**, cliquez sur **Modifier la connexion utilisateur**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc349-126">On the **Additional tasks** page, click **Change user sign-in**, and then click **Next**.</span></span>

5. <span data-ttu-id="bc349-127">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc349-127">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6. <span data-ttu-id="bc349-128">Sur la page **Connexion utilisateur**, sélectionnez **Activer l’authentification unique**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc349-128">On the **User sign-in** page, select **Enable single sign-on**, and then click **Next**.</span></span>

7. <span data-ttu-id="bc349-129">Sur la page **Activer l’authentification unique**, cliquez sur **Entrer les informations d’identification**.</span><span class="sxs-lookup"><span data-stu-id="bc349-129">On the **Enable single sign-on** page, click **Enter credentials**.</span></span>

8. <span data-ttu-id="bc349-p103">Dans la boîte de dialogue **Sécurité Windows**, tapez **user1** et le mot de passe du compte Utilisateur1, puis cliquez sur **OK**. Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc349-p103">In the **Windows Security** dialog box, type **user1** and the password of the user1 account, and then click **OK**. Click **Next**.</span></span>

9. <span data-ttu-id="bc349-132">Sur la page **Prêt à configurer**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="bc349-132">On the **Ready to Configure** page, click **Configure**.</span></span>

10. <span data-ttu-id="bc349-133">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="bc349-133">On the **Configuration complete** page, click **Exit**.</span></span>

11. <span data-ttu-id="bc349-p104">Sur le Portail Azure, dans le volet gauche, cliquez sur **Azure Active Directory > Azure AD Connect**. Vérifiez que la fonctionnalité **Authentification unique transparente** affiche l’état **Activé**.</span><span class="sxs-lookup"><span data-stu-id="bc349-p104">From the Azure portal, in the left pane, click **Azure Active Directory > Azure AD Connect**. Verify that the **Seamless single sign-on** feature appears as **Enabled**.</span></span>

<span data-ttu-id="bc349-136">Ensuite, vérifiez si vous pouvez vous connecter à votre abonnement Office 365 avec le nom d’utilisateur <strong>utilisateur1@testlab.</strong>\<votre domaine public> du compte Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="bc349-136">Next, test the ability to sign in to your Office 365 subscription with the <strong>user1@testlab.</strong>\<your public domain> user name of the User1 account.</span></span>

1. <span data-ttu-id="bc349-137">Dans Internet Explorer sur APP1, cliquez sur l’icône Paramètres, puis cliquez sur **Options Internet**.</span><span class="sxs-lookup"><span data-stu-id="bc349-137">From Internet Explorer on APP1, click the settings icon, and then click **Internet Options**.</span></span>
 
2. <span data-ttu-id="bc349-138">Dans **Options Internet**, cliquez sur l’onglet **Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="bc349-138">In **Internet Options**, click the **Security** tab.</span></span>

3. <span data-ttu-id="bc349-139">Cliquez sur **Intranet local**, puis sur **Sites**.</span><span class="sxs-lookup"><span data-stu-id="bc349-139">Click **Local intranet**, and then click **Sites**.</span></span>

4. <span data-ttu-id="bc349-140">Dans **Intranet Local**, cliquez sur **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="bc349-140">In **Local intranet**, click **Advanced**.</span></span>

5. <span data-ttu-id="bc349-141">Dans **Ajouter ce site web à la zone**, tapez **https<span>://</span>autologon.microsoftazuread-sso.com**, cliquez sur **Ajouter > Fermer > OK > OK**.</span><span class="sxs-lookup"><span data-stu-id="bc349-141">In **Add this website to the zone**, type **https<span>://</span>autologon.microsoftazuread-sso.com**, click **Add > Close > OK > OK**.</span></span>

6. <span data-ttu-id="bc349-142">Déconnectez-vous d’Office 365, puis reconnectez-vous avec un autre compte.</span><span class="sxs-lookup"><span data-stu-id="bc349-142">Sign out of Office 365, and then sign in again, this time specifying a different account.</span></span>

7. <span data-ttu-id="bc349-143">Lorsque vous êtes invité à vous connecter, spécifiez<strong>user1@testlab.</strong>\<votre domaine public > nom, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="bc349-143">When prompted to sign in, specify <strong>user1@testlab.</strong>\<your public domain> name, and then click **Next**.</span></span> <span data-ttu-id="bc349-144">Vous devez correctement vous connecter en tant que User1 sans entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bc349-144">You should successfully sign in as User1 without being prompted for a password.</span></span> <span data-ttu-id="bc349-145">Cela prouve qu’ Azure AD transparente SSO fonctionne.</span><span class="sxs-lookup"><span data-stu-id="bc349-145">This proves that Azure AD Seamless SSO is working.</span></span>

<span data-ttu-id="bc349-146">Notez que même si les utilisateurs User1 disposent des autorisations d’administrateur de domaine pour le domaine TESTLAB AD DS, il n’est pas un administrateur général pour Azure AD et Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc349-146">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator for Azure AD and Office 365.</span></span> <span data-ttu-id="bc349-147">Par conséquent, vous ne verrez pas l’icône**administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="bc349-147">Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="bc349-148">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="bc349-148">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)

 
<span data-ttu-id="bc349-150">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="bc349-150">This configuration consists of:</span></span>

- <span data-ttu-id="bc349-151">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="bc349-151">Office 365 E5 and EMS E5 trial or paid subscriptions with the DNS domain testlab.\<your domain name> registered.</span></span>
- <span data-ttu-id="bc349-152">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="bc349-152">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="bc349-153">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de vos abonnements Office 365 et EMS E5 au domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="bc349-153">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Office 365 and EMS E5 subscriptions to the TESTLAB AD DS domain.</span></span> 
- <span data-ttu-id="bc349-154">L’authentification unique transparente Azure AD est activée pour permettre aux ordinateurs sur l’intranet simulé de se connecter aux ressources cloud Microsoft 365 sans avoir à spécifier le mot de passe du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bc349-154">Azure AD Seamless SSO is enabled so that computers on the simulated intranet can sign in to Microsoft 365 cloud resources without specifing a user account password.</span></span>

<span data-ttu-id="bc349-155">Consultez l’étape [Simplifier la connexion de l’utilisateur](identity-secure-your-passwords.md#identity-sso) de la phase d’identité pour obtenir des informations et des liens pour configurer l’authentification unique transparente Azure AD en production.</span><span class="sxs-lookup"><span data-stu-id="bc349-155">See the [Simplify user sign-in](identity-secure-your-passwords.md#identity-sso) step in the Identity phase for information and links to configure Azure AD Seamless SSO in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="bc349-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="bc349-156">Next step</span></span>

<span data-ttu-id="bc349-157">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="bc349-157">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc349-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc349-158">See also</span></span>

[<span data-ttu-id="bc349-159">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="bc349-159">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="bc349-160">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="bc349-160">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="bc349-161">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="bc349-161">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


