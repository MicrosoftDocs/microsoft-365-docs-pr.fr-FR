---
title: Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365
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
- TLG
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Découvrez comment configurer la connexion et la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 8c0f9b45fc4a57ad5ac50ea2a3340d6e05769b96
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43632898"
---
# <a name="password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="983d2-103">Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="983d2-103">Password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="983d2-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="983d2-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="983d2-105">De nombreuses organisations utilisent Azure AD Connect et la synchronisation de hachage de mot de passe pour synchroniser l’ensemble de comptes dans leur forêt Active Directory Domain Services (AD DS) en local avec l’ensemble des comptes dans le client Azure AD de leur abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="983d2-105">Many organizations use Azure AD Connect and password hash synchronization to synchronize the set of accounts in their on-premises Active Directory Domain Services (AD DS) forest to the set of accounts in the Azure AD tenant of their Microsoft 365 subscription.</span></span> <span data-ttu-id="983d2-106">Cet article explique comment vous pouvez ajouter DirSync avec la synchronisation de mot de passe à l’environnement de développement/test Microsoft 365, ce qui entraîne la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="983d2-106">This article describes how you can add password hash synchronization to your Microsoft 365 test environment, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)
  
<span data-ttu-id="983d2-108">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="983d2-108">There are two phases to setting up this test environment:</span></span>
  
1. <span data-ttu-id="983d2-109">Créez l’environnement de test de l’entreprise simulée pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="983d2-109">Create the Microsoft 365 simulated enterprise test environment.</span></span>
2. <span data-ttu-id="983d2-110">Installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="983d2-110">Install and configure Azure AD Connect on APP1.</span></span>
    
> [!TIP]
> <span data-ttu-id="983d2-111">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="983d2-111">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-create-the-microsoft-365-simulated-enterprise-test-environment"></a><span data-ttu-id="983d2-112">Phase 1 : création de l’environnement de test de l’entreprise simulée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="983d2-112">Phase 1: Create the Microsoft 365 simulated enterprise test environment</span></span>

<span data-ttu-id="983d2-p102">Suivez les instructions fournies dans l’article [Configuration de base d’une entreprise simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="983d2-p102">Follow the instructions in [simulated enterprise base configuration for Microsoft 365](simulated-ent-base-configuration-microsoft-365-enterprise.md). Here is your resulting configuration.</span></span>
  
![Configuration de base d’une entreprise simulée](../media/password-hash-sync-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="983d2-116">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="983d2-116">This configuration consists of:</span></span> 
  
- <span data-ttu-id="983d2-117">Un abonnement d’évaluation ou payant Microsoft 365 E5 ou Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="983d2-117">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="983d2-118">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="983d2-118">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines in an Azure virtual network.</span></span> <span data-ttu-id="983d2-119">DC1 est un contrôleur de domaine pour le testlab.\<votre nom de domaine public > domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="983d2-119">DC1 is a domain controller for the testlab.\<your public domain name> AD DS domain.</span></span>

## <a name="phase-2-create-and-register-the-testlab-domain"></a><span data-ttu-id="983d2-120">Phase 2 : création et enregistrement du domaine testlab</span><span class="sxs-lookup"><span data-stu-id="983d2-120">Phase 2: Create and register the testlab domain</span></span>

<span data-ttu-id="983d2-121">Durant cette phase, vous allez créer un domaine DNS public et l’ajouter à votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="983d2-121">In this phase you add a public DNS domain and add it to your subscription.</span></span>

<span data-ttu-id="983d2-p104">Utilisez tout d’abord votre fournisseur d’enregistrement DNS public pour créer un nom de domaine DNS public basé sur votre nom de domaine actuel et ajoutez-le à votre abonnement. Nous vous recommandons d’utiliser le nom **testlab.**\<votre domaine public>. Par exemple, si votre nom de domaine public est **<span>contoso</span>.com**, ajoutez le nom de domaine public **<span>testlab</span>.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="983d2-p104">First, work with your public DNS registration provider to create a new public DNS domain name based on your current domain name and add it to your subscription. We recommend using the name **testlab.**\<your public domain>. For example, if your public domain name is **<span>contoso</span>.com**, add the public domain name **<span>testlab</span>.contoso.com**.</span></span>
  
<span data-ttu-id="983d2-125">Vous pouvez ensuite ajouter les **testlab.**\<votre domaine public > domaine à votre abonnement Microsoft 365 ou Office 365 d’évaluation ou payant par le biais du processus d’inscription domaine.</span><span class="sxs-lookup"><span data-stu-id="983d2-125">Next, you add the **testlab.**\<your public domain> domain to your Microsoft 365 or Office 365 trial or paid subscription by going through the domain registration process.</span></span> <span data-ttu-id="983d2-126">Cela se compose de l’ajout d’autres enregistrements DNS pour le **testlab.** \<votre domaine public > domaine.</span><span class="sxs-lookup"><span data-stu-id="983d2-126">This consists of adding additional DNS records to the **testlab.**\<your public domain> domain.</span></span> <span data-ttu-id="983d2-127">Pour plus d’informations, voir [Ajouter un domaine à Office 365](https://docs.microsoft.com/office365/admin/setup/add-domain).</span><span class="sxs-lookup"><span data-stu-id="983d2-127">For more information, see [Add a domain to Office 365](https://docs.microsoft.com/office365/admin/setup/add-domain).</span></span> 

<span data-ttu-id="983d2-128">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="983d2-128">Here is your resulting configuration.</span></span>
  
![Enregistrement de votre nom de domaine testlab](../media/password-hash-sync-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="983d2-130">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="983d2-130">This configuration consists of:</span></span>

- <span data-ttu-id="983d2-131">Les abonnements à la version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine public> enregistré.</span><span class="sxs-lookup"><span data-stu-id="983d2-131">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain testlab.\<your public domain name> registered.</span></span>
- <span data-ttu-id="983d2-132">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="983d2-132">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>

<span data-ttu-id="983d2-133">Notez comment se présente le domaine testlab.\<votre nom de domaine public> :</span><span class="sxs-lookup"><span data-stu-id="983d2-133">Notice how the testlab.\<your public domain name> is now:</span></span>

- <span data-ttu-id="983d2-134">Il est pris en charge par les enregistrements DNS publics.</span><span class="sxs-lookup"><span data-stu-id="983d2-134">Supported by public DNS records.</span></span>
- <span data-ttu-id="983d2-135">Enregistré dans vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="983d2-135">Registered in your Microsoft 365 subscriptions.</span></span>
- <span data-ttu-id="983d2-136">Le domaine Windows Server AD se trouve sur votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="983d2-136">The AD DS domain on your simulated intranet.</span></span>
     
## <a name="phase-3-install-azure-ad-connect-on-app1"></a><span data-ttu-id="983d2-137">Phase 3 : installation d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="983d2-137">Phase 3: Install Azure AD Connect on APP1</span></span>

<span data-ttu-id="983d2-138">Durant cette phase, vous allez installer et configurer l’outil Azure AD Connect sur APP1, puis vérifier son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="983d2-138">In this phase, you install and configure the Azure AD Connect tool on APP1, and then verify that it works.</span></span>
  
<span data-ttu-id="983d2-139">Tout d’abord, installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="983d2-139">First, you install and configure Azure AD Connect on APP1.</span></span>

1. <span data-ttu-id="983d2-140">Dans le [portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="983d2-140">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\\User1 account.</span></span>
    
2. <span data-ttu-id="983d2-141">Sur le bureau d’APP1, ouvrez une invite de commandes Windows PowerShell de niveau administrateur, puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="983d2-141">From the desktop of APP1, open an administrator-level Windows PowerShell command prompt, and then run these commands:</span></span>
    
   ```powershell
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A7-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A8-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Stop-Process -Name Explorer -Force
   ```

3. <span data-ttu-id="983d2-142">Dans la barre des tâches, cliquez sur **Internet Explorer** et accédez à [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span><span class="sxs-lookup"><span data-stu-id="983d2-142">From the task bar, click **Internet Explorer** and go to [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span></span>
    
4. <span data-ttu-id="983d2-143">Sur la page de Microsoft Azure Active Directory Connect, cliquez sur **Télécharger**, puis cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="983d2-143">On the Microsoft Azure Active Directory Connect page, click **Download**, and then click **Run**.</span></span>
    
5. <span data-ttu-id="983d2-144">Sur la page **Bienvenue dans Azure AD Connect**, cliquez sur **J’accepte**, puis sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="983d2-144">On the **Welcome to Azure AD Connect** page, click **I agree**, and then click **Continue**.</span></span>
    
6. <span data-ttu-id="983d2-145">Sur la page **Configuration rapide**, cliquez sur **Utiliser la configuration rapide**.</span><span class="sxs-lookup"><span data-stu-id="983d2-145">On the **Express Settings** page, click **Use express settings**.</span></span>
    
7. <span data-ttu-id="983d2-146">Sur la page **Connexion à Azure AD**, saisissez le nom de votre compte d’administrateur général sous **Nom d’utilisateur** et le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="983d2-146">On the **Connect to Azure AD** page, type your global administrator account name in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="983d2-147">Sur la page **Connexion à AD DS**, tapez **TESTLAB\\Utilisateur1** sous **Nom d’utilisateur**, tapez le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="983d2-147">On the **Connect to AD DS** page, type **TESTLAB\\User1** in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
9. <span data-ttu-id="983d2-148">Sur la page **Prêt à configurer**, cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="983d2-148">On the **Ready to configure** page, click **Install**.</span></span>
    
10. <span data-ttu-id="983d2-149">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="983d2-149">On the **Configuration complete** page, click **Exit**.</span></span>
    
11. <span data-ttu-id="983d2-150">Dans Internet Explorer, accédez au Centre d’administration Microsoft 365 ([https://portal.microsoft.com](https://portal.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="983d2-150">In Internet Explorer, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)).</span></span>
    
12. <span data-ttu-id="983d2-151">Dans la navigation de gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="983d2-151">In the left navigation, click **Users > Active users**.</span></span>
    
    <span data-ttu-id="983d2-152">Notez le compte nommé **Utilisateur 1**.</span><span class="sxs-lookup"><span data-stu-id="983d2-152">Note the account named **User1**.</span></span> <span data-ttu-id="983d2-153">Ce compte provient du domaine TESTLAB AD DS et prouve que la synchronisation d’annuaires a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="983d2-153">This account is from the TESTLAB AD DS domain and is proof that directory synchronization has worked.</span></span>
    
13. <span data-ttu-id="983d2-154">Cliquez sur le compte **utilisateur1**, puis cliquez sur **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="983d2-154">Click the **User1** account, and then click **Licenses and apps**.</span></span>
    
14. <span data-ttu-id="983d2-155">Dans **Licences de produits**, sélectionnez votre lieu (le cas échéant), désactivez la licence **Office 365 E5** et activez la licence **Microsoft 365 E5**.</span><span class="sxs-lookup"><span data-stu-id="983d2-155">In **Product licenses**, select your location (if needed), disable the **Office 365 E5** license and enable the **Microsoft 365 E5** license.</span></span> 

15. <span data-ttu-id="983d2-156">Cliquez sur **Enregistrer** en bas de la page, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="983d2-156">Click **Save** at the bottom of the page, and then click **Close**.</span></span>
    
<span data-ttu-id="983d2-157">Ensuite, vérifiez si vous pouvez vous connecter à votre abonnement avec le nom d’utilisateur <strong>user1@testlab.</strong>\<votre nom de domaine> du compte User1.</span><span class="sxs-lookup"><span data-stu-id="983d2-157">Next, you test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<your domain name> user name of the User1 account.</span></span>

1. <span data-ttu-id="983d2-158">Dans APP1, déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="983d2-158">From APP1, sign out, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="983d2-p107">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez <strong>utilisateur1@testlab.</strong>\<votre nom de domaine> et le mot de passe de l’Utilisateur1. Vous serez connecté en tant qu’Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="983d2-p107">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your domain name> and the User1 password. You should successfully sign in as User1.</span></span> 
 
<span data-ttu-id="983d2-161">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="983d2-161">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator.</span></span> <span data-ttu-id="983d2-162">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="983d2-162">Therefore, you will not see the **Admin** icon as an option.</span></span> 

<span data-ttu-id="983d2-163">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="983d2-163">Here is your resulting configuration.</span></span>

![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)

<span data-ttu-id="983d2-165">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="983d2-165">This configuration consists of:</span></span> 
  
- <span data-ttu-id="983d2-166">Les abonnements en version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="983d2-166">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span>
- <span data-ttu-id="983d2-167">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="983d2-167">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="983d2-168">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB AD DS avec le client Azure AD de votre abonnement Microsoft 365 de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="983d2-168">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription periodically.</span></span>
- <span data-ttu-id="983d2-169">Le compte Utilisateur1 dans le domaine TESTLAB  AD DS a été synchronisé avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="983d2-169">The User1 account in the TESTLAB  AD DS domain has been synchronized with the Azure AD tenant.</span></span>

## <a name="next-step"></a><span data-ttu-id="983d2-170">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="983d2-170">Next step</span></span>

<span data-ttu-id="983d2-171">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="983d2-171">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="983d2-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="983d2-172">See also</span></span>

[<span data-ttu-id="983d2-173">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="983d2-173">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="983d2-174">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="983d2-174">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="983d2-175">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="983d2-175">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


