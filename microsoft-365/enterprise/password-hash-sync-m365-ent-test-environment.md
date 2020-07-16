---
title: Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/26/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Découvrez comment configurer la connexion et la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 7b1ba549a9ac9d3faec8b717a0f76cca1200352b
ms.sourcegitcommit: 87eff6e8a08cec3cb0464a3b765434717584a4a9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/26/2020
ms.locfileid: "44371439"
---
# <a name="password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="689c0-103">Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="689c0-103">Password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="689c0-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="689c0-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="689c0-105">De nombreuses organisations utilisent Azure AD Connect et la synchronisation de hachage de mot de passe pour synchroniser l’ensemble de comptes dans leur forêt Active Directory Domain Services (AD DS) en local avec l’ensemble des comptes dans le client Azure AD de leur abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="689c0-105">Many organizations use Azure AD Connect and password hash synchronization to synchronize the set of accounts in their on-premises Active Directory Domain Services (AD DS) forest to the set of accounts in the Azure AD tenant of their Microsoft 365 subscription.</span></span> <span data-ttu-id="689c0-106">Cet article explique comment vous pouvez ajouter DirSync avec la synchronisation de mot de passe à l’environnement de développement/test Microsoft 365, ce qui entraîne la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="689c0-106">This article describes how you can add password hash synchronization to your Microsoft 365 test environment, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)
  
<span data-ttu-id="689c0-108">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="689c0-108">There are two phases to setting up this test environment:</span></span>
  
1. <span data-ttu-id="689c0-109">Créez l’environnement de test de l’entreprise simulée pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="689c0-109">Create the Microsoft 365 simulated enterprise test environment.</span></span>
2. <span data-ttu-id="689c0-110">Installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="689c0-110">Install and configure Azure AD Connect on APP1.</span></span>
    
> [!TIP]
> <span data-ttu-id="689c0-111">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="689c0-111">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-create-the-microsoft-365-simulated-enterprise-test-environment"></a><span data-ttu-id="689c0-112">Phase 1 : création de l’environnement de test de l’entreprise simulée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="689c0-112">Phase 1: Create the Microsoft 365 simulated enterprise test environment</span></span>

<span data-ttu-id="689c0-p102">Suivez les instructions fournies dans l’article [Configuration de base d’une entreprise simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="689c0-p102">Follow the instructions in [simulated enterprise base configuration for Microsoft 365](simulated-ent-base-configuration-microsoft-365-enterprise.md). Here is your resulting configuration.</span></span>
  
![Configuration de base d’une entreprise simulée](../media/password-hash-sync-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="689c0-116">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="689c0-116">This configuration consists of:</span></span> 
  
- <span data-ttu-id="689c0-117">Un abonnement d’évaluation ou payant Microsoft 365 E5 ou Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="689c0-117">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="689c0-118">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="689c0-118">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines in an Azure virtual network.</span></span> <span data-ttu-id="689c0-119">DC1 est un contrôleur de domaine pour le testlab.\<votre nom de domaine public > domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="689c0-119">DC1 is a domain controller for the testlab.\<your public domain name> AD DS domain.</span></span> <span data-ttu-id="689c0-120">Phase 2 : création et enregistrement du domaine testlab</span><span class="sxs-lookup"><span data-stu-id="689c0-120">Phase 2: Create and register the testlab domain</span></span>

## <a name="phase-2-create-and-register-the-testlab-domain"></a><span data-ttu-id="689c0-121">Durant cette phase, vous allez créer un domaine DNS public et l’ajouter à votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="689c0-121">In this phase you add a public DNS domain and add it to your subscription.</span></span>

<span data-ttu-id="689c0-122">First, work with your public DNS registration provider to create a new public DNS domain name based on your current domain name and add it to your subscription.</span><span class="sxs-lookup"><span data-stu-id="689c0-122">First, work with your public DNS registration provider to create a new public DNS domain name based on your current domain name and add it to your subscription.</span></span>

<span data-ttu-id="689c0-p104">Utilisez tout d’abord votre fournisseur d’enregistrement DNS public pour créer un nom de domaine DNS public basé sur votre nom de domaine actuel et ajoutez-le à votre abonnement. Nous vous recommandons d’utiliser le nom **testlab.**\<votre domaine public>. Par exemple, si votre nom de domaine public est **<span>contoso</span>.com**, ajoutez le nom de domaine public **<span>testlab</span>.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="689c0-p104">First, work with your public DNS registration provider to create a new public DNS domain name based on your current domain name and add it to your subscription. We recommend using the name **testlab.**\<your public domain>. For example, if your public domain name is **<span>contoso</span>.com**, add the public domain name **<span>testlab</span>.contoso.com**.</span></span>
  
<span data-ttu-id="689c0-126">Cela se compose de l’ajout d’autres enregistrements DNS pour le **testlab.** \<votre domaine public > domaine.</span><span class="sxs-lookup"><span data-stu-id="689c0-126">This consists of adding additional DNS records to the **testlab.**\<your public domain> domain.</span></span> <span data-ttu-id="689c0-127">Pour plus d’informations, voir [Ajouter un domaine à Office 365](https://docs.microsoft.com/office365/admin/setup/add-domain).</span><span class="sxs-lookup"><span data-stu-id="689c0-127">For more information, see [Add a domain to Office 365](https://docs.microsoft.com/office365/admin/setup/add-domain).</span></span> <span data-ttu-id="689c0-128">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="689c0-128">Here is your resulting configuration.</span></span> <span data-ttu-id="689c0-129">Enregistrement de votre nom de domaine testlab</span><span class="sxs-lookup"><span data-stu-id="689c0-129">The registration of your testlab domain name</span></span> <span data-ttu-id="689c0-130">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="689c0-130">This configuration consists of:</span></span> 

<span data-ttu-id="689c0-131">Les abonnements à la version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine public> enregistré.</span><span class="sxs-lookup"><span data-stu-id="689c0-131">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain testlab.\<your public domain name> registered.</span></span>
  
![Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.](../media/password-hash-sync-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="689c0-133">Notez comment se présente le domaine testlab.\<votre nom de domaine public> :</span><span class="sxs-lookup"><span data-stu-id="689c0-133">Notice how the testlab.\<your public domain name> is now:</span></span>

- <span data-ttu-id="689c0-134">Il est pris en charge par les enregistrements DNS publics.</span><span class="sxs-lookup"><span data-stu-id="689c0-134">Supported by public DNS records.</span></span> <span data-ttu-id="689c0-135">Enregistré dans vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="689c0-135">Registered in your Microsoft 365 subscriptions.</span></span>
- <span data-ttu-id="689c0-136">Le domaine Windows Server AD se trouve sur votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="689c0-136">The AD DS domain on your simulated intranet.</span></span>

<span data-ttu-id="689c0-p107">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez <strong>utilisateur1@testlab.</strong>\<votre nom de domaine> et le mot de passe de l’Utilisateur1. Vous serez connecté en tant qu’Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="689c0-p107">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your domain name> and the User1 password. You should successfully sign in as User1.</span></span>

- <span data-ttu-id="689c0-139">Tout d’abord, installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="689c0-139">First, you install and configure Azure AD Connect on APP1.</span></span>
- <span data-ttu-id="689c0-140">Dans le [portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="689c0-140">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\\User1 account.</span></span>
- <span data-ttu-id="689c0-141">Sur le bureau d’APP1, ouvrez une invite de commandes Windows PowerShell de niveau administrateur, puis exécutez les commandes suivantes pour désactiver la sécurité renforcée d’Internet Explorer :</span><span class="sxs-lookup"><span data-stu-id="689c0-141">From the desktop of APP1, open an administrator-level Windows PowerShell command prompt, and then run these commands to disable Internet Explorer Enhanced Security:</span></span>
     
## <a name="phase-3-install-azure-ad-connect-on-app1"></a><span data-ttu-id="689c0-142">Dans la barre des tâches, cliquez sur **Internet Explorer** et accédez à [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span><span class="sxs-lookup"><span data-stu-id="689c0-142">From the task bar, click **Internet Explorer** and go to [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span></span>

<span data-ttu-id="689c0-143">Sur la page de Microsoft Azure Active Directory Connect, cliquez sur **Télécharger**, puis cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="689c0-143">On the Microsoft Azure Active Directory Connect page, click **Download**, and then click **Run**.</span></span>
  
<span data-ttu-id="689c0-144">Sur la page **Bienvenue dans Azure AD Connect**, cliquez sur **J’accepte**, puis sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="689c0-144">On the **Welcome to Azure AD Connect** page, click **I agree**, and then click **Continue**.</span></span>

1. <span data-ttu-id="689c0-145">Sur la page **Configuration rapide**, cliquez sur **Utiliser la configuration rapide**.</span><span class="sxs-lookup"><span data-stu-id="689c0-145">On the **Express Settings** page, click **Use express settings**.</span></span>
    
2. <span data-ttu-id="689c0-146">Sur la page **Connexion à Azure AD**, saisissez le nom de votre compte d’administrateur général sous **Nom d’utilisateur** et le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="689c0-146">On the **Connect to Azure AD** page, type your global administrator account name in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
   ```powershell
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A7-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A8-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Stop-Process -Name Explorer -Force
   ```

3. <span data-ttu-id="689c0-147">Sur la page **Connexion à AD DS**, tapez **TESTLAB\\Utilisateur1** sous **Nom d’utilisateur**, tapez le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="689c0-147">On the **Connect to AD DS** page, type **TESTLAB\\User1** in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="689c0-148">Sur la page **Prêt à configurer**, cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="689c0-148">On the **Ready to configure** page, click **Install**.</span></span>
    
5. <span data-ttu-id="689c0-149">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="689c0-149">On the **Configuration complete** page, click **Exit**.</span></span>
    
6. <span data-ttu-id="689c0-150">Dans Internet Explorer, accédez au Centre d’administration Microsoft 365 ([https://portal.microsoft.com](https://portal.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="689c0-150">In Internet Explorer, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)).</span></span>
    
7. <span data-ttu-id="689c0-151">Dans la navigation de gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="689c0-151">In the left navigation, click **Users > Active users**.</span></span>
    
8. <span data-ttu-id="689c0-152">Notez le compte nommé **Utilisateur 1**.</span><span class="sxs-lookup"><span data-stu-id="689c0-152">Note the account named **User1**.</span></span>
    
9. <span data-ttu-id="689c0-153">Ce compte provient du domaine TESTLAB AD DS et prouve que la synchronisation d’annuaires a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="689c0-153">This account is from the TESTLAB AD DS domain and is proof that directory synchronization has worked.</span></span>
    
10. <span data-ttu-id="689c0-154">Cliquez sur le compte **utilisateur1**, puis cliquez sur **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="689c0-154">Click the **User1** account, and then click **Licenses and apps**.</span></span>
    
11. <span data-ttu-id="689c0-155">Dans **Licences de produits**, sélectionnez votre lieu (le cas échéant), désactivez la licence **Office 365 E5** et activez la licence **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="689c0-155">In **Product licenses**, select your location (if needed), disable the **Office 365 E5** license and enable the **Microsoft 365 E5** license.</span></span>
    
12. <span data-ttu-id="689c0-156">Cliquez sur **Enregistrer** en bas de la page, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="689c0-156">Click **Save** at the bottom of the page, and then click **Close**.</span></span>
    
    <span data-ttu-id="689c0-157">Ensuite, vérifiez si vous pouvez vous connecter à votre abonnement avec le nom d’utilisateur <strong>user1@testlab.</strong>\<votre nom de domaine> du compte User1.</span><span class="sxs-lookup"><span data-stu-id="689c0-157">Next, you test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<your domain name> user name of the User1 account.</span></span> <span data-ttu-id="689c0-158">Dans APP1, déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="689c0-158">From APP1, sign out, and then sign in again, this time specifying a different account.</span></span>
    
13. <span data-ttu-id="689c0-159">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your domain name> and the User1 password.</span><span class="sxs-lookup"><span data-stu-id="689c0-159">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your domain name> and the User1 password.</span></span>
    
14. <span data-ttu-id="689c0-160">You should successfully sign in as User1.</span><span class="sxs-lookup"><span data-stu-id="689c0-160">You should successfully sign in as User1.</span></span> 

15. <span data-ttu-id="689c0-161">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="689c0-161">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator.</span></span>
    
<span data-ttu-id="689c0-162">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="689c0-162">Therefore, you will not see the **Admin** icon as an option.</span></span> <span data-ttu-id="689c0-163">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="689c0-163">Here is your resulting configuration.</span></span>

1. <span data-ttu-id="689c0-164">Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="689c0-164">The simulated enterprise with password hash synchronization test environment</span></span>

2. <span data-ttu-id="689c0-165">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="689c0-165">This configuration consists of:</span></span> <span data-ttu-id="689c0-166">Les abonnements en version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="689c0-166">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span> <span data-ttu-id="689c0-167">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="689c0-167">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
 
<span data-ttu-id="689c0-168">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB AD DS avec le client Azure AD de votre abonnement Microsoft 365 de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="689c0-168">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription periodically.</span></span> <span data-ttu-id="689c0-169">Le compte Utilisateur1 dans le domaine TESTLAB  AD DS a été synchronisé avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="689c0-169">The User1 account in the TESTLAB  AD DS domain has been synchronized with the Azure AD tenant.</span></span> 

<span data-ttu-id="689c0-170">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="689c0-170">Next step</span></span>

![Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)

<span data-ttu-id="689c0-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="689c0-172">See also</span></span> 
  
- [<span data-ttu-id="689c0-173">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="689c0-173">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md) [<span data-ttu-id="689c0-174">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="689c0-174">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)
- [<span data-ttu-id="689c0-175">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="689c0-175">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/) Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription periodically.
- The User1 account in the TESTLAB  AD DS domain has been synchronized with the Azure AD tenant.

## <a name="next-step"></a>Next step

Explore additional <bpt id="p1">[</bpt>identity<ept id="p1">](m365-enterprise-test-lab-guides.md#identity)</ept> features and capabilities in your test environment.

## <a name="see-also"></a>See also

<bpt id="p1">[</bpt>Microsoft 365 Enterprise Test Lab Guides<ept id="p1">](m365-enterprise-test-lab-guides.md)</ept>

<bpt id="p1">[</bpt>Deploy Microsoft 365 Enterprise<ept id="p1">](deploy-microsoft-365-enterprise.md)</ept>

<bpt id="p1">[</bpt>Microsoft 365 Enterprise documentation<ept id="p1">](https://docs.microsoft.com/microsoft-365-enterprise/)</ept>


