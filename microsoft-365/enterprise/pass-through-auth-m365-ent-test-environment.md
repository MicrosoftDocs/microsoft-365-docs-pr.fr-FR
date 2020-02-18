---
title: Authentification directe pour votre environnement de test Microsoft 365
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
description: 'Résumé : Découvrez comment configurer l’authentification directe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 4f9941b017f00b40a6ae7e893211131cae51c611
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42066420"
---
# <a name="pass-through-authentication-for-your-microsoft-365-test-environment"></a><span data-ttu-id="17e65-103">Authentification directe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="17e65-103">Pass-through authentication for your Microsoft 365 test environment</span></span>

<span data-ttu-id="17e65-104">*Ce Guide de Laboratoire Test peut être utilisé pour les environnements de test Microsoft 365 Entreprise et Office 365 Entreprise*.</span><span class="sxs-lookup"><span data-stu-id="17e65-104">*This Test Lab Guide can be used for both Microsoft 365 Enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="17e65-105">Les organisations désireuses d’utiliser directement leur infrastructure d’Active Directory Domain Services (AD DS) en local pour l’authentification aux applications et services sur le cloud Microsoft peuvent utiliser l’authentification directe.</span><span class="sxs-lookup"><span data-stu-id="17e65-105">Organizations that want to directly use their on-premises Active Directory Domain Services (AD DS) infrastructure for authentication to Microsoft cloud-based services and applications can use pass-through authentication.</span></span> <span data-ttu-id="17e65-106">Cet article décrit comment configurer l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365. Voici la configuration que vous obtenez:</span><span class="sxs-lookup"><span data-stu-id="17e65-106">This article describes how you can configure your Microsoft 365 test environment for pass-through authentication, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="17e65-108">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="17e65-108">There are two phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="17e65-109">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="17e65-109">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.  <span data-ttu-id="17e65-110">Configuration de l’authentification directe pour Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="17e65-110">Configure Azure AD Connect on APP1 for pass-through authentication.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="17e65-112">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="17e65-112">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="17e65-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="17e65-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="17e65-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="17e65-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="17e65-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="17e65-117">This configuration consists of:</span></span> 
  
- <span data-ttu-id="17e65-118">Abonnements d’évaluation ou payants Microsoft 365 E5 ou Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="17e65-118">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="17e65-119">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="17e65-119">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="17e65-120">Azure AD Connect s’exécute sur APP1 pour synchroniser périodiquement le domaine TESTLAB AD DS avec le client Azure AD de votre abonnement Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="17e65-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 or Office 365 subscription periodically.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-pass-through-authentication"></a><span data-ttu-id="17e65-121">Phase 2 : Configuration de l’authentification directe pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="17e65-121">Phase 2: Configure Azure AD Connect on APP1 for pass-through authentication</span></span>

<span data-ttu-id="17e65-122">Durant cette phase, vous allez configurer Azure AD Connect sur APP1 pour qu’il utilise l’authentification directe, puis vérifier que tout fonctionne.</span><span class="sxs-lookup"><span data-stu-id="17e65-122">In this phase, you configure Azure AD Connect on APP1 to use pass-through authentication, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="17e65-123">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="17e65-123">Configure Azure AD Connect on APP1</span></span>

1.  <span data-ttu-id="17e65-124">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="17e65-124">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2.  <span data-ttu-id="17e65-125">Sur le bureau d’APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="17e65-125">From the desktop of APP1, run Azure AD Connect.</span></span>

3.  <span data-ttu-id="17e65-126">Sur la page **Bienvenue**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="17e65-126">On the **Welcome page**, click **Configure**.</span></span>

4.  <span data-ttu-id="17e65-127">Sur la page Tâches supplémentaires, cliquez sur **Modifier la connexion utilisateur**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17e65-127">On the Additional tasks page, click **Change user sign-in**, and then click **Next**.</span></span>

5.  <span data-ttu-id="17e65-128">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17e65-128">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6.  <span data-ttu-id="17e65-129">Sur la page **Connexion de l’utilisateur**, cliquez sur **Authentification directe**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="17e65-129">On the **User sign-in** page, click **Pass-through authentication**, and then click **Next**.</span></span>

7.  <span data-ttu-id="17e65-130">Sur la page **Prêt à configurer**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="17e65-130">On the **Ready to configure** page, click **Configure**.</span></span>

8.  <span data-ttu-id="17e65-131">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="17e65-131">On the **Configuration complete** page, click **Exit**.</span></span>

9.  <span data-ttu-id="17e65-p104">Sur le Portail Azure, dans le volet gauche, cliquez sur **Azure Active Directory > Azure AD Connect**. Vérifiez que la fonctionnalité **Authentification directe** affiche l’état **Activé**.</span><span class="sxs-lookup"><span data-stu-id="17e65-p104">From the Azure portal, in the left pane, click **Azure Active Directory > Azure AD Connect**. Verify that the **Pass-through authentication** feature appears as **Enabled**.</span></span>

10. <span data-ttu-id="17e65-p105">Cliquez sur **Authentification directe**. Le volet **Authentification directe** répertorie les serveurs où vos agents d’authentification sont installés. APP1 devrait figurer dans la liste. Fermez le volet **Authentification directe**.</span><span class="sxs-lookup"><span data-stu-id="17e65-p105">Click **Pass-through authentication**. The **Pass-through authentication** pane lists the servers where your Authentication Agents are installed. You should see APP1 in the list. Close the **Pass-through authentication** pane.</span></span>

<span data-ttu-id="17e65-138">Vérifiez ensuite si vous pouvez vous connecter à votre abonnement avec le nom d’utilisateur <strong>utilisateur1@testlab.</strong>\<votre domaine public> du compte Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="17e65-138">Next, test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<your public domain> user name of the User1 account.</span></span>

1. <span data-ttu-id="17e65-139">Dans APP1, déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="17e65-139">From APP1, sign out, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="17e65-140">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez <strong>utilisateur1@testlab.</strong>\<votre domaine public> et le mot de passe de l’Utilisateur1. Vous serez connecté en tant qu’Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="17e65-140">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your public domain> and the User1 password.</span></span> <span data-ttu-id="17e65-141">Vous devez correctement vous connecter en tant qu’ Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="17e65-141">You should successfully sign in as User1.</span></span>

<span data-ttu-id="17e65-142">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="17e65-142">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator.</span></span> <span data-ttu-id="17e65-143">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="17e65-143">Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="17e65-144">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="17e65-144">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
<span data-ttu-id="17e65-146">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="17e65-146">This configuration consists of:</span></span>

- <span data-ttu-id="17e65-147">Les abonnements en version payante ou d’évaluation Microsoft 365 E5 et Office 365 E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="17e65-147">Microsoft 365 E5 or Office 365 E5 trial or paid subscriptions with the DNS domain testlab.\<your domain name> registered.</span></span>
- <span data-ttu-id="17e65-p108">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure. Un agent d’authentification s’exécute sur APP1 pour traiter les demandes d’authentification directe provenant du client Azure AD de vos abonnements Microsoft 365 et Office 365.</span><span class="sxs-lookup"><span data-stu-id="17e65-p108">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network. An Authentication Agent runs on APP1 to handle pass-through authentication requests from the Azure AD tenant of your Microsoft 365 or Office 365 subscription.</span></span>

## <a name="next-step"></a><span data-ttu-id="17e65-150">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="17e65-150">Next step</span></span>

<span data-ttu-id="17e65-151">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="17e65-151">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="17e65-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17e65-152">See also</span></span>

[<span data-ttu-id="17e65-153">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="17e65-153">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="17e65-154">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="17e65-154">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="17e65-155">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="17e65-155">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
