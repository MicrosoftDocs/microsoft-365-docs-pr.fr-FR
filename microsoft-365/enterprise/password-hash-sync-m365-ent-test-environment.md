---
title: Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/13/2018
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
ms.openlocfilehash: 0c6f7ec4afdfaaca0c84ed33ea0c1b1f248a82f5
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34073174"
---
# <a name="password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="a1bd2-103">Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1bd2-103">Password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="a1bd2-104">De nombreuses organisations utilisent Azure AD Connect et le mot de passe hachage de synchronisation d’annuaires pour synchroniser l’ensemble de comptes dans leur forêt Active Directory Domain Services (AD DS) en local à l’ensemble de comptes dans le client Azure AD de leur abonnement Office 365 et EMS E5 .</span><span class="sxs-lookup"><span data-stu-id="a1bd2-104">Many organizations use Azure AD Connect and password hash synchronization to synchronize the set of accounts in their on-premises Active Directory Domain Services (AD DS) forest to the set of accounts in the Azure AD tenant of their Office 365 and EMS E5 subscriptions.</span></span> <span data-ttu-id="a1bd2-105">Cet article explique comment vous pouvez ajouter DirSync avec la synchronisation de mot de passe à l’environnement de développement/test Microsoft 365, ce qui entraîne la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="a1bd2-105">This article describes how you can add password hash synchronization to your Microsoft 365 test environment, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/password-hash-sync-m365-ent-test-environment/Phase3.png)
  
<span data-ttu-id="a1bd2-107">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1bd2-107">There are two phases to setting up this test environment:</span></span>
  
1. <span data-ttu-id="a1bd2-108">Créez l’environnement de test de l’entreprise simulée pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-108">Create the Microsoft 365 simulated enterprise test environment.</span></span>
2. <span data-ttu-id="a1bd2-109">Installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-109">Install and configure Azure AD Connect on APP1.</span></span>
    
> [!TIP]
> <span data-ttu-id="a1bd2-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-create-the-microsoft-365-simulated-enterprise-test-environment"></a><span data-ttu-id="a1bd2-111">Phase 1 : création de l’environnement de test de l’entreprise simulée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a1bd2-111">Phase 1: Create the Microsoft 365 simulated enterprise test environment</span></span>

<span data-ttu-id="a1bd2-p102">Suivez les instructions fournies dans l’article [Configuration de base d’une entreprise simulée](simulated-ent-base-configuration-microsoft-365-enterprise.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-p102">Follow the instructions in [simulated enterprise base configuration for Microsoft 365](simulated-ent-base-configuration-microsoft-365-enterprise.md). Here is your resulting configuration.</span></span>
  
![Configuration de base d’une entreprise simulée](media/password-hash-sync-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="a1bd2-115">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="a1bd2-115">This configuration consists of:</span></span> 
  
- <span data-ttu-id="a1bd2-116">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-116">Office 365 E5 and EMS E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="a1bd2-117">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-117">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines in an Azure virtual network.</span></span> <span data-ttu-id="a1bd2-118">DC1 est un contrôleur de domaine pour le testlab.\<votre nom de domaine public > domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-118">DC1 is a domain controller for the testlab.\<your public domain name> Active Directory Domain Services (AD DS) domain.</span></span>

## <a name="phase-2-create-and-register-the-testlab-domain"></a><span data-ttu-id="a1bd2-119">Phase 2 : création et enregistrement du domaine testlab</span><span class="sxs-lookup"><span data-stu-id="a1bd2-119">Phase 2: Create and register the testlab domain</span></span>

<span data-ttu-id="a1bd2-120">Durant cette phase, vous allez créer un domaine DNS public et l’ajouter à votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-120">In this phase you add a public DNS domain and add it to your subscription.</span></span>

<span data-ttu-id="a1bd2-p104">Tout d’abord, utilisez votre fournisseur d’enregistrement DNS public pour créer un nom de domaine DNS public en fonction de votre nom de domaine actuel et ajoutez-le à votre abonnement Office 365. Nous vous recommandons d’utiliser le nom **testlab.**\<votre domaine public>. Par exemple, si votre nom de domaine public est <span>**contoso</span>.com**, ajoutez le nom de domaine public **<span>testlab</span>.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-p104">First, work with your public DNS registration provider to create a new public DNS domain name based on your current domain name and add it to your Office 365 subscription. We recommend using the name **testlab.**\<your public domain>. For example, if your public domain name is <span>**contoso</span>.com**, add the public domain name **<span>testlab</span>.contoso.com**.</span></span>
  
<span data-ttu-id="a1bd2-124">Vous pouvez ensuite ajouter les **testlab.**\<votre domaine public > domaine à votre abonnement Office 365 d’évaluation ou payant par le biais le processus d’inscription domaine.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-124">Next, you add the **testlab.**\<your public domain> domain to your Office 365 trial or paid subscription by going through the domain registration process.</span></span> <span data-ttu-id="a1bd2-125">Cela se compose de l’ajout d’autres enregistrements DNS pour le **testlab.** \<votre domaine public > domaine.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-125">This consists of adding additional DNS records to the **testlab.**\<your public domain> domain.</span></span> <span data-ttu-id="a1bd2-126">Pour plus d’informations sur ce processus, voir [Ajouter vos utilisateurs et votre domaine à Office 365](https://support.office.com/article/Add-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611).</span><span class="sxs-lookup"><span data-stu-id="a1bd2-126">For more information, see [Add users and domain to Office 365](https://support.office.com/article/Add-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611).</span></span> 

<span data-ttu-id="a1bd2-127">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-127">Here is your resulting configuration.</span></span>
  
![Enregistrement de votre nom de domaine testlab](media/password-hash-sync-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="a1bd2-129">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="a1bd2-129">This configuration consists of:</span></span>

- <span data-ttu-id="a1bd2-130">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-130">Office 365 E5 and EMS E5 trial or paid subscriptions with the DNS domain testlab.\<your public domain name> registered.</span></span>
- <span data-ttu-id="a1bd2-131">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-131">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>

<span data-ttu-id="a1bd2-132">Notez comment se présente le domaine testlab.\<votre nom de domaine public> :</span><span class="sxs-lookup"><span data-stu-id="a1bd2-132">Notice how the testlab.\<your public domain name> is now:</span></span>

- <span data-ttu-id="a1bd2-133">Il est pris en charge par les enregistrements DNS publics.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-133">Supported by public DNS records.</span></span>
- <span data-ttu-id="a1bd2-134">Il est enregistré dans vos abonnements Office 365 et EMS.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-134">Registered in your Office 365 and EMS subscriptions.</span></span>
- <span data-ttu-id="a1bd2-135">Le domaine Windows Server AD se trouve sur votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-135">The AD DS domain on your simulated intranet.</span></span>
     
## <a name="phase-3-install-azure-ad-connect-on-app1"></a><span data-ttu-id="a1bd2-136">Phase 3 : installation d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="a1bd2-136">Phase 3: Install Azure AD Connect on APP1</span></span>

<span data-ttu-id="a1bd2-137">Durant cette phase, vous allez installer et configurer l’outil Azure AD Connect sur APP1, puis vérifier son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-137">In this phase, you install and configure the Azure AD Connect tool on APP1, and then verify that it works.</span></span>
  
<span data-ttu-id="a1bd2-138">Tout d’abord, installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-138">First, you install and configure Azure AD Connect on APP1.</span></span>

1. <span data-ttu-id="a1bd2-139">Dans le [portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-139">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\\User1 account.</span></span>
    
2. <span data-ttu-id="a1bd2-140">Sur le bureau d’APP1, ouvrez une invite de commandes Windows PowerShell de niveau administrateur, puis exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1bd2-140">From the desktop of APP1, open an administrator-level Windows PowerShell command prompt, and then run these commands:</span></span>
    
   ```
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A7-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A8-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Stop-Process -Name Explorer -Force
   ```

3. <span data-ttu-id="a1bd2-141">Dans la barre des tâches, cliquez sur **Internet Explorer** et accédez à [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span><span class="sxs-lookup"><span data-stu-id="a1bd2-141">From the task bar, click **Internet Explorer** and go to [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span></span>
    
4. <span data-ttu-id="a1bd2-142">Sur la page de Microsoft Azure Active Directory Connect, cliquez sur **Télécharger**, puis cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-142">On the Microsoft Azure Active Directory Connect page, click **Download**, and then click **Run**.</span></span>
    
5. <span data-ttu-id="a1bd2-143">Sur la page **Bienvenue dans Azure AD Connect**, cliquez sur **J’accepte**, puis sur **Continuer**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-143">On the **Welcome to Azure AD Connect** page, click **I agree**, and then click **Continue**.</span></span>
    
6. <span data-ttu-id="a1bd2-144">Sur la page **Configuration rapide**, cliquez sur **Utiliser la configuration rapide**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-144">On the **Express Settings** page, click **Use express settings**.</span></span>
    
7. <span data-ttu-id="a1bd2-145">Sur la page **Connexion à Azure AD**, tapez le nom de votre compte d’administrateur général Office 365 sous **Nom d’utilisateur** et le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-145">On the **Connect to Azure AD** page, type your Office 365 global administrator account name in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="a1bd2-146">Sur la page **Connexion à AD DS**, tapez **TESTLAB\\Utilisateur1** sous **Nom d’utilisateur**, tapez le mot de passe correspondant sous **Mot de passe**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-146">On the **Connect to AD DS** page, type **TESTLAB\\User1** in **Username,** type its password in **Password**, and then click **Next**.</span></span>
    
9. <span data-ttu-id="a1bd2-147">Sur la page **Prêt à configurer**, cliquez sur **Installer**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-147">On the **Ready to configure** page, click **Install**.</span></span>
    
10. <span data-ttu-id="a1bd2-148">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-148">On the **Configuration complete** page, click **Exit**.</span></span>
    
11. <span data-ttu-id="a1bd2-149">Dans Internet Explorer, accédez au Centre d’administration Microsoft 365 ([https://portal.microsoft.com](https://portal.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="a1bd2-149">In Internet Explorer, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)).</span></span>
    
12. <span data-ttu-id="a1bd2-150">Dans la navigation de gauche, cliquez sur **Utilisateurs > Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-150">In the left navigation, click **Users > Active users**.</span></span>
    
    <span data-ttu-id="a1bd2-151">Notez le compte nommé **Utilisateur 1**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-151">Note the account named **User1**.</span></span> <span data-ttu-id="a1bd2-152">Ce compte provient du domaine TESTLAB AD DS et prouve que la synchronisation d’annuaires a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-152">This account is from the TESTLAB AD DS domain and is proof that directory synchronization has worked.</span></span>
    
13. <span data-ttu-id="a1bd2-p107">Cliquez sur le compte **Utilisateur1**. Pour les licences de produits, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-p107">Click the **User1** account. For product licenses, click **Edit**.</span></span>
    
14. <span data-ttu-id="a1bd2-p108">Dans **Licences de produits**, sélectionnez votre pays, puis cliquez sur le contrôle **Inactif** pour **Office 365 Entreprise E5** (en le définissant sur **Actif**). Faites de même avec la licence **Enterprise Mobility + Security E5**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-p108">In **Product licenses**, select your scountry, and then click the **Off** control for **Office 365 Enterprise E5** (switching it to **On**). Do the same for the **Enterprise Mobility + Security E5** license.</span></span> 

15. <span data-ttu-id="a1bd2-157">Cliquez sur **Enregistrer** en bas de la page, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-157">Click **Save** at the bottom of the page, and then click **Close**.</span></span>
    
<span data-ttu-id="a1bd2-158">Ensuite, vérifiez si vous pouvez vous connecter à votre abonnement Office 365 avec le <strong>nom d’utilisateur utilisateur1@testlab.</strong>\<votre nom de domaine> du compte Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-158">Next, you test the ability to sign in to your Office 365 subscription with the <strong>user1@testlab.</strong>\<your domain name> user name of the User1 account.</span></span>

1. <span data-ttu-id="a1bd2-159">Dans APP1, déconnectez-vous d’Office 365, puis reconnectez-vous avec un autre compte.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-159">From APP1, sign out of Office 365, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="a1bd2-p109">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez <strong>utilisateur1@testlab.</strong>\<votre nom de domaine> et le mot de passe de l’Utilisateur1. Vous serez connecté en tant qu’Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-p109">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your domain name> and the User1 password. You should successfully sign in as User1.</span></span> 
 
<span data-ttu-id="a1bd2-162">Notez que même si les utilisateurs User1 disposent des autorisations d’administrateur de domaine pour le domaine TESTLAB AD DS, il n’est pas un administrateur général pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-162">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not an Office 365 global administrator.</span></span> <span data-ttu-id="a1bd2-163">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-163">Therefore, you will not see the **Admin** icon as an option.</span></span> 

<span data-ttu-id="a1bd2-164">Voici la configuration finale.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-164">Here is your resulting configuration.</span></span>

![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/password-hash-sync-m365-ent-test-environment/Phase3.png)

<span data-ttu-id="a1bd2-166">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="a1bd2-166">This configuration consists of:</span></span> 
  
- <span data-ttu-id="a1bd2-167">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-167">Office 365 E5 and EMS E5 trial or paid subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span>
- <span data-ttu-id="a1bd2-168">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-168">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="a1bd2-169">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB AD DS avec le client Azure AD, le client de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-169">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions periodically.</span></span>
- <span data-ttu-id="a1bd2-170">Le compte Utilisateur1 dans le domaine TESTLAB  AD DS a été synchronisé avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-170">The User1 account in the TESTLAB  AD DS domain has been synchronized with the Azure AD tenant.</span></span>

## <a name="next-step"></a><span data-ttu-id="a1bd2-171">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a1bd2-171">Next step</span></span>

<span data-ttu-id="a1bd2-172">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="a1bd2-172">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1bd2-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1bd2-173">See also</span></span>

[<span data-ttu-id="a1bd2-174">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="a1bd2-174">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="a1bd2-175">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="a1bd2-175">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="a1bd2-176">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="a1bd2-176">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


