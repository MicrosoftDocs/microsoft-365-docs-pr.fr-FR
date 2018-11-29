---
title: Authentification directe pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Découvrez comment configurer l’authentification directe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 26222f04617999104a1ad010eb189a0c01370a6d
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867033"
---
# <a name="pass-through-authentication-for-your-microsoft-365-test-environment"></a><span data-ttu-id="582a5-103">Authentification directe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="582a5-103">Pass-through authentication for your Microsoft 365 test environment</span></span>

<span data-ttu-id="582a5-p101">Les organisations qui souhaitent utiliser directement leur infrastructure Windows Server Active Directory (AD) locale pour faciliter l’authentification aux applications et services informatiques Microsoft peuvent recourir à l’authentification directe. Cet article décrit comment vous pouvez configurer l’authentification directe pour votre environnement de test Microsoft 365, afin d’obtenir la configuration suivante :</span><span class="sxs-lookup"><span data-stu-id="582a5-p101">Organizations that want to directly use their on-premises Windows Server Active Directory (AD) infrastructure for authentication to Microsoft cloud-based services and applications can use pass-through authentication. This article describes how you can configure your Microsoft 365 test environment for pass-through authentication, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="582a5-107">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="582a5-107">There are two phases to setting up this test environment:</span></span>

1.  <span data-ttu-id="582a5-108">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="582a5-108">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.  <span data-ttu-id="582a5-109">Configuration de l’authentification directe pour Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="582a5-109">Configure Azure AD Connect on APP1 for pass-through authentication.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="582a5-111">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="582a5-111">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="582a5-112">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="582a5-112">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="582a5-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="582a5-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="582a5-116">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="582a5-116">This configuration consists of:</span></span> 
  
- <span data-ttu-id="582a5-117">Les abonnements à la version permanente ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="582a5-117">Office 365 E5 and EMS E5 trial or permanent subscriptions.</span></span>
- <span data-ttu-id="582a5-p103">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure. Azure AD Connect s’exécute sur APP1 pour synchroniser régulièrement le domaine TESTLAB Windows Server AD avec le client Azure AD de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="582a5-p103">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network. Azure AD Connect runs on APP1 to synchronize the TESTLAB Windows Server AD domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions periodically.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-pass-through-authentication"></a><span data-ttu-id="582a5-120">Phase 2 : Configuration de l’authentification directe pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="582a5-120">Phase 2: Configure Azure AD Connect on APP1 for pass-through authentication</span></span>

<span data-ttu-id="582a5-121">Durant cette phase, vous allez configurer Azure AD Connect sur APP1 pour qu’il utilise l’authentification directe, puis vérifier que tout fonctionne.</span><span class="sxs-lookup"><span data-stu-id="582a5-121">In this phase, you configure Azure AD Connect on APP1 to use pass-through authentication, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="582a5-122">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="582a5-122">Configure Azure AD Connect on APP1</span></span>

1.  <span data-ttu-id="582a5-123">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="582a5-123">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2.  <span data-ttu-id="582a5-124">Sur le bureau d’APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="582a5-124">From the desktop of APP1, run Azure AD Connect.</span></span>

3.  <span data-ttu-id="582a5-125">Sur la page **Bienvenue**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="582a5-125">On the **Welcome page**, click **Configure**.</span></span>

4.  <span data-ttu-id="582a5-126">Sur la page Tâches supplémentaires, cliquez sur **Modifier la connexion utilisateur**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="582a5-126">On the Additional tasks page, click **Change user sign-in**, and then click **Next**.</span></span>

5.  <span data-ttu-id="582a5-127">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="582a5-127">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6.  <span data-ttu-id="582a5-128">Sur la page **Connexion de l’utilisateur**, cliquez sur **Authentification directe**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="582a5-128">On the **User sign-in** page, click **Pass-through authentication**, and then click **Next**.</span></span>

7.  <span data-ttu-id="582a5-129">Sur la page **Prêt à configurer**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="582a5-129">On the **Ready to configure** page, click **Configure**.</span></span>

8.  <span data-ttu-id="582a5-130">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="582a5-130">On the **Configuration complete** page, click **Exit**.</span></span>

9.  <span data-ttu-id="582a5-p104">Sur le Portail Azure, dans le volet gauche, cliquez sur **Azure Active Directory > Azure AD Connect**. Vérifiez que la fonctionnalité **Authentification directe** affiche l’état **Activé**.</span><span class="sxs-lookup"><span data-stu-id="582a5-p104">From the Azure portal, in the left pane, click **Azure Active Directory > Azure AD Connect**. Verify that the **Pass-through authentication** feature appears as **Enabled**.</span></span>

10. <span data-ttu-id="582a5-p105">Cliquez sur **Authentification directe**. Le volet **Authentification directe** répertorie les serveurs où vos agents d’authentification sont installés. APP1 devrait figurer dans la liste. Fermez le volet **Authentification directe**.</span><span class="sxs-lookup"><span data-stu-id="582a5-p105">Click **Pass-through authentication**. The **Pass-through authentication** pane lists the servers where your Authentication Agents are installed. You should see APP1 in the list. Close the **Pass-through authentication** pane.</span></span>

<span data-ttu-id="582a5-137">Ensuite, vérifiez si vous pouvez vous connecter à votre abonnement Office 365 avec le nom d’utilisateur utilisateur1@testlab.\<votre domaine public> du compte Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="582a5-137">Next, test the ability to sign in to your Office 365 subscription with the user1@testlab.\<your public domain> user name of the User1 account.</span></span>

1. <span data-ttu-id="582a5-138">Dans APP1, déconnectez-vous d’Office 365, puis reconnectez-vous avec un autre compte.</span><span class="sxs-lookup"><span data-stu-id="582a5-138">From APP1, sign out of Office 365, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="582a5-p106">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez utilisateur1@testlab.\<votre domaine public> et le mot de passe de l’Utilisateur1. Vous serez connecté en tant qu’Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="582a5-p106">When prompted for a user name and password, specify user1@testlab.\<your public domain> and the User1 password. You should successfully sign in as User1.</span></span>

<span data-ttu-id="582a5-p107">Notez que même si l’Utilisateur1 dispose des autorisations d’administrateur de domaine pour le domaine TESTLAB Windows Server AD, il n’est pas un administrateur général Office 365. Ainsi, vous ne verrez pas l’icône **Admin** dans les options.</span><span class="sxs-lookup"><span data-stu-id="582a5-p107">Notice that although User1 has domain administrator permissions for the TESTLAB Windows Server AD domain, it is not an Office 365 global administrator. Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="582a5-143">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="582a5-143">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
<span data-ttu-id="582a5-145">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="582a5-145">This configuration consists of:</span></span>

- <span data-ttu-id="582a5-146">Les abonnements à la version permanente ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="582a5-146">Office 365 E5 and EMS E5 trial or permanent subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span>
- <span data-ttu-id="582a5-p108">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure. Un agent d’authentification s’exécute sur APP1 pour traiter les demandes d’authentification directe provenant du client Azure AD de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="582a5-p108">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network. An Authentication Agent runs on APP1 to handle pass-through authentication requests from the Azure AD tenant of your Office 365 and EMS E5 subscriptions.</span></span>

## <a name="next-step"></a><span data-ttu-id="582a5-149">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="582a5-149">Next step</span></span>

<span data-ttu-id="582a5-150">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="582a5-150">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="582a5-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="582a5-151">See also</span></span>

[<span data-ttu-id="582a5-152">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="582a5-152">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="582a5-153">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="582a5-153">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="582a5-154">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="582a5-154">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


