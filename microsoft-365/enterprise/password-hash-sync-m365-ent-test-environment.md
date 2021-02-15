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
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
- seo-marvel-apr2020
ms.assetid: ''
description: 'Résumé : Découvrez comment configurer la connexion et la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 3c20d1997be2ff47f0b449cbba3afb1e6edcd59a
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487457"
---
# <a name="password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="2f2da-103">Synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2f2da-103">Password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="2f2da-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="2f2da-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="2f2da-105">De nombreuses organisations utilisent Azure AD Connect et la synchronisation de hachage de mot de passe pour synchroniser l’ensemble de comptes dans leur forêt Active Directory Domain Services (AD DS) en local avec l’ensemble des comptes dans le client Azure AD de leur abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2f2da-105">Many organizations use Azure AD Connect and password hash synchronization to synchronize the set of accounts in their on-premises Active Directory Domain Services (AD DS) forest to the set of accounts in the Azure AD tenant of their Microsoft 365 subscription.</span></span> 

<span data-ttu-id="2f2da-106">Cet article explique comment ajouter la synchronisation de hachage de mot de passe à votre environnement de test Microsoft 365, ce qui entraîne cette configuration :</span><span class="sxs-lookup"><span data-stu-id="2f2da-106">This article describes how you can add password hash synchronization to your Microsoft 365 test environment, which results in this configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)
  
<span data-ttu-id="2f2da-108">La configuration de cet environnement de test comprend trois phases :</span><span class="sxs-lookup"><span data-stu-id="2f2da-108">Setting up this test environment involves three phases:</span></span>
- [<span data-ttu-id="2f2da-109">Phase 1 : création de l’environnement de test de l’entreprise simulée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2f2da-109">Phase 1: Create the Microsoft 365 simulated enterprise test environment</span></span>](#phase-1-create-the-microsoft-365-simulated-enterprise-test-environment)
- [<span data-ttu-id="2f2da-110">Phase 2 : création et enregistrement du domaine testlab</span><span class="sxs-lookup"><span data-stu-id="2f2da-110">Phase 2: Create and register the testlab domain</span></span>](#phase-2-create-and-register-the-testlab-domain)
- [<span data-ttu-id="2f2da-111">Phase 3 : installation d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="2f2da-111">Phase 3: Install Azure AD Connect on APP1</span></span>](#phase-3-install-azure-ad-connect-on-app1)
    
> [!TIP]
> <span data-ttu-id="2f2da-112">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="2f2da-112">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-create-the-microsoft-365-simulated-enterprise-test-environment"></a><span data-ttu-id="2f2da-113">Phase 1 : création de l’environnement de test de l’entreprise simulée pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2f2da-113">Phase 1: Create the Microsoft 365 simulated enterprise test environment</span></span>

<span data-ttu-id="2f2da-114">Suivez les instructions de [la configuration de base d’entreprise simulée pour Microsoft 365.](simulated-ent-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="2f2da-114">Follow the instructions in [simulated enterprise base configuration for Microsoft 365](simulated-ent-base-configuration-microsoft-365-enterprise.md).</span></span> <span data-ttu-id="2f2da-115">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="2f2da-115">Your resulting configuration looks like this:</span></span>
  
![Configuration de base d’une entreprise simulée](../media/password-hash-sync-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="2f2da-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="2f2da-117">This configuration consists of:</span></span>
  
- <span data-ttu-id="2f2da-118">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2f2da-118">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="2f2da-119">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 dans un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2da-119">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines in an Azure virtual network.</span></span> <span data-ttu-id="2f2da-120">DC1 est un contrôleur de domaine pour le domaine testlab.<votre nom de domaine *public*> domaine AD DS.</span><span class="sxs-lookup"><span data-stu-id="2f2da-120">DC1 is a domain controller for the testlab.<*your public domain name*> AD DS domain.</span></span>

## <a name="phase-2-create-and-register-the-testlab-domain"></a><span data-ttu-id="2f2da-121">Phase 2 : création et enregistrement du domaine testlab</span><span class="sxs-lookup"><span data-stu-id="2f2da-121">Phase 2: Create and register the testlab domain</span></span>

<span data-ttu-id="2f2da-122">Dans cette phase, ajoutez un domaine DNS public, puis ajoutez-le à votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f2da-122">In this phase, add a public DNS domain, and then add it to your subscription.</span></span>

<span data-ttu-id="2f2da-123">Tout d’abord, travaillez avec votre fournisseur d’inscription DNS public pour créer un nom de domaine DNS public basé sur votre nom de domaine actuel, puis ajoutez-le à votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f2da-123">First, work with your public DNS registration provider to create a new public DNS domain name that's based on your current domain name, and then add it to your subscription.</span></span> <span data-ttu-id="2f2da-124">Nous vous recommandons d’utiliser le nom **testlab.<*votre domaine public.\* >*\*</span><span class="sxs-lookup"><span data-stu-id="2f2da-124">We recommend using the name **testlab.<*your public domain*>**.</span></span> <span data-ttu-id="2f2da-125">Par exemple, si votre nom de domaine public est **<span>contoso</span>.com,** ajoutez le nom de domaine public : **<span>testlab</span>.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="2f2da-125">For example, if your public domain name is **<span>contoso</span>.com**, add the public domain name: **<span>testlab</span>.contoso.com**.</span></span>
  
<span data-ttu-id="2f2da-126">Ensuite, ajoutez **testlab.< >** votre domaine de domaine public à votre abonnement d’évaluation ou payant Microsoft 365 en suivant le processus d’inscription de domaine.</span><span class="sxs-lookup"><span data-stu-id="2f2da-126">Next, add the **testlab.<*your public domain*>** domain to your Microsoft 365 trial or paid subscription by going through the domain registration process.</span></span> <span data-ttu-id="2f2da-127">Cela consiste à ajouter des enregistrements DNS supplémentaires au **domaine testlab.<*votre domaine\* > public.*\*</span><span class="sxs-lookup"><span data-stu-id="2f2da-127">This consists of adding additional DNS records to the **testlab.<*your public domain*>** domain.</span></span> <span data-ttu-id="2f2da-128">Pour plus d’informations, [voir Ajouter un domaine à Microsoft 365.](../admin/setup/add-domain.md)</span><span class="sxs-lookup"><span data-stu-id="2f2da-128">For more information, see [Add a domain to Microsoft 365](../admin/setup/add-domain.md).</span></span>

<span data-ttu-id="2f2da-129">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="2f2da-129">Your resulting configuration looks like this:</span></span>
  
![Enregistrement de votre nom de domaine testlab](../media/password-hash-sync-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="2f2da-131">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="2f2da-131">This configuration consists of:</span></span>

- <span data-ttu-id="2f2da-132">Un abonnement d’essai ou payant Microsoft 365 E5 avec le domaine DNS testlab.<votre nom de domaine *public*> enregistré.</span><span class="sxs-lookup"><span data-stu-id="2f2da-132">A Microsoft 365 E5 trial or paid subscription with the DNS domain testlab.<*your public domain name*> registered.</span></span>
- <span data-ttu-id="2f2da-133">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2da-133">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>

<span data-ttu-id="2f2da-134">Notez que testlab.<*votre nom* de domaine public> maintenant :</span><span class="sxs-lookup"><span data-stu-id="2f2da-134">Notice how the testlab.<*your public domain name*> is now:</span></span>

- <span data-ttu-id="2f2da-135">Il est pris en charge par les enregistrements DNS publics.</span><span class="sxs-lookup"><span data-stu-id="2f2da-135">Supported by public DNS records.</span></span>
- <span data-ttu-id="2f2da-136">Enregistré dans vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2f2da-136">Registered in your Microsoft 365 subscriptions.</span></span>
- <span data-ttu-id="2f2da-137">Le domaine Windows Server AD se trouve sur votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="2f2da-137">The AD DS domain on your simulated intranet.</span></span>
     
## <a name="phase-3-install-azure-ad-connect-on-app1"></a><span data-ttu-id="2f2da-138">Phase 3 : installation d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="2f2da-138">Phase 3: Install Azure AD Connect on APP1</span></span>

<span data-ttu-id="2f2da-139">Dans cette phase, installez et configurez l’outil Azure AD Connect sur APP1, puis vérifiez qu’il fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2f2da-139">In this phase, install and configure the Azure AD Connect tool on APP1, and then verify that it works.</span></span>
  
<span data-ttu-id="2f2da-140">Tout d’abord, installez et configurez Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="2f2da-140">First, install and configure Azure AD Connect on APP1.</span></span>

1. <span data-ttu-id="2f2da-141">Dans le [portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="2f2da-141">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\\User1 account.</span></span>
    
2. <span data-ttu-id="2f2da-142">Sur le bureau d’APP1, ouvrez une invite de commandes Windows PowerShell de niveau administrateur, puis exécutez les commandes suivantes pour désactiver la sécurité renforcée d’Internet Explorer :</span><span class="sxs-lookup"><span data-stu-id="2f2da-142">From the desktop of APP1, open an administrator-level Windows PowerShell command prompt, and then run these commands to disable Internet Explorer Enhanced Security:</span></span>
    
   ```powershell
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A7-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Active Setup\Installed Components\{A509B1A8-37EF-4b3f-8CFC-4F3A74704073}" -Name "IsInstalled" -Value 0
   Stop-Process -Name Explorer -Force
   ```

3. <span data-ttu-id="2f2da-143">Dans la barre des tâches, sélectionnez **Internet Explorer** et allez à [https://aka.ms/aadconnect](https://aka.ms/aadconnect) .</span><span class="sxs-lookup"><span data-stu-id="2f2da-143">From the taskbar, select **Internet Explorer** and go to [https://aka.ms/aadconnect](https://aka.ms/aadconnect).</span></span>
    
4. <span data-ttu-id="2f2da-144">Dans la page Microsoft Azure Active Directory Connect, **sélectionnez Télécharger,** puis **Exécuter.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-144">On the Microsoft Azure Active Directory Connect page, select **Download**, and then select **Run**.</span></span>
    
5. <span data-ttu-id="2f2da-145">Dans la page **Bienvenue dans Azure AD Connect,** sélectionnez **J’accepte,** puis sélectionnez **Continuer.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-145">On the **Welcome to Azure AD Connect** page, select **I agree**, and then select **Continue**.</span></span>
    
6. <span data-ttu-id="2f2da-146">Dans la page **Paramètres express,** sélectionnez **Utiliser les paramètres express.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-146">On the **Express Settings** page, select **Use express settings**.</span></span>
    
7. <span data-ttu-id="2f2da-147">Dans la page Se connecter **à Azure AD,** entrez le nom de votre compte d’administrateur général dans Nom d’utilisateur, entrez son mot de passe dans Mot de passe, puis sélectionnez  **Suivant**. </span><span class="sxs-lookup"><span data-stu-id="2f2da-147">On the **Connect to Azure AD** page, enter your global administrator account name in **Username,** enter its password in **Password**, and then select **Next**.</span></span>
    
8. <span data-ttu-id="2f2da-148">Dans la page **Se connecter à AD DS,** entrez **TESTLAB \\ User1** dans Nom d’utilisateur, entrez son mot de passe dans **Mot** de passe, puis sélectionnez **Suivant**. </span><span class="sxs-lookup"><span data-stu-id="2f2da-148">On the **Connect to AD DS** page, enter **TESTLAB\\User1** in **Username,** enter its password in **Password**, and then select **Next**.</span></span>
    
9. <span data-ttu-id="2f2da-149">Dans la page **Prêt à configurer,** sélectionnez **Installer.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-149">On the **Ready to configure** page, select **Install**.</span></span>
    
10. <span data-ttu-id="2f2da-150">Dans la page **Configuration terminée,** sélectionnez **Quitter.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-150">On the **Configuration complete** page, select **Exit**.</span></span>
    
11. <span data-ttu-id="2f2da-151">Dans Internet Explorer, accédez au Centre d’administration Microsoft 365 ([https://portal.microsoft.com](https://portal.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="2f2da-151">In Internet Explorer, go to the Microsoft 365 admin center ([https://portal.microsoft.com](https://portal.microsoft.com)).</span></span>
    
12. <span data-ttu-id="2f2da-152">Dans le volet de navigation de gauche, sélectionnez **Utilisateurs > utilisateurs actifs.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-152">In the left navigation pane, select **Users > Active users**.</span></span>
    
    <span data-ttu-id="2f2da-153">Notez le compte nommé **Utilisateur 1**.</span><span class="sxs-lookup"><span data-stu-id="2f2da-153">Note the account named **User1**.</span></span> <span data-ttu-id="2f2da-154">Ce compte provient du domaine TESTLAB AD DS et prouve que la synchronisation d’annuaires a fonctionné.</span><span class="sxs-lookup"><span data-stu-id="2f2da-154">This account is from the TESTLAB AD DS domain and is proof that directory synchronization has worked.</span></span>
    
13. <span data-ttu-id="2f2da-155">Sélectionnez **le compte Utilisateur1,** puis sélectionnez **Licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-155">Select the **User1** account, and then select **Licenses and apps**.</span></span>
    
14. <span data-ttu-id="2f2da-156">Dans **les licences de** produit, sélectionnez votre emplacement (si nécessaire), désactivez la licence Office **365 E5,** puis activez la licence Microsoft **365 E5.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-156">In **Product licenses**, select your location (if needed), disable the **Office 365 E5** license, and then enable the **Microsoft 365 E5** license.</span></span> 

15. <span data-ttu-id="2f2da-157">Sélectionnez **Enregistrer** en bas de la page, puis **fermez.**</span><span class="sxs-lookup"><span data-stu-id="2f2da-157">Select **Save** at the bottom of the page, and then select **Close**.</span></span>
    
<span data-ttu-id="2f2da-158">Ensuite, testez la possibilité de vous inscrire à votre abonnement à **l’user1@testlab.< >** votre nom de domaine du compte User1 :</span><span class="sxs-lookup"><span data-stu-id="2f2da-158">Next, test the ability to sign in to your subscription with the **user1@testlab.<*your domain name*>** user name of the User1 account:</span></span>

1. <span data-ttu-id="2f2da-159">Dans APP1, déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="2f2da-159">From APP1, sign out, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="2f2da-160">Lorsque vous y invitez un nom d’utilisateur et un mot de passe, spécifiez **user1@testlab.< >** votre nom de domaine et le mot de passe Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="2f2da-160">When prompted for a user name and password, specify **user1@testlab.<*your domain name*>** and the User1 password.</span></span> <span data-ttu-id="2f2da-161">Vous devez correctement vous connecter en tant qu’ Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="2f2da-161">You should successfully sign in as User1.</span></span>
 
<span data-ttu-id="2f2da-162">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2f2da-162">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator.</span></span> <span data-ttu-id="2f2da-163">Par conséquent, vous ne verrez pas l’icône **Administrateur** comme une option.</span><span class="sxs-lookup"><span data-stu-id="2f2da-163">Therefore, you will not see the **Admin** icon as an option.</span></span> 

<span data-ttu-id="2f2da-164">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="2f2da-164">Your resulting configuration looks like this:</span></span>

![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/password-hash-sync-m365-ent-test-environment/Phase3.png)

<span data-ttu-id="2f2da-166">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="2f2da-166">This configuration consists of:</span></span> 
  
- <span data-ttu-id="2f2da-167">Abonnements payants ou d’essai Microsoft 365 E5 ou Office 365 E5  avec le domaine DNS TESTLAB.<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="2f2da-167">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain TESTLAB.<*your domain name*> registered.</span></span>
- <span data-ttu-id="2f2da-168">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2da-168">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="2f2da-169">Azure AD Connect s’exécute sur APP1 pour synchroniser régulièrement le domaine TESTLAB AD DS avec le client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2f2da-169">Azure AD Connect runs on APP1 to periodically synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription.</span></span>
- <span data-ttu-id="2f2da-170">Le compte Utilisateur1 dans le domaine TESTLAB  AD DS a été synchronisé avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2f2da-170">The User1 account in the TESTLAB  AD DS domain has been synchronized with the Azure AD tenant.</span></span>

## <a name="next-step"></a><span data-ttu-id="2f2da-171">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2f2da-171">Next step</span></span>

<span data-ttu-id="2f2da-172">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="2f2da-172">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f2da-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f2da-173">See also</span></span>

[<span data-ttu-id="2f2da-174">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="2f2da-174">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="2f2da-175">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="2f2da-175">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="2f2da-176">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2f2da-176">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
