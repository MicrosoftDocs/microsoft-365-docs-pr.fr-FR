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
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Découvrez comment configurer l’authentification directe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: cdbb6927fb8ca0001e3089c7169ce9046208e8f8
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50921527"
---
# <a name="pass-through-authentication-for-your-microsoft-365-test-environment"></a><span data-ttu-id="91042-103">Authentification directe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="91042-103">Pass-through authentication for your Microsoft 365 test environment</span></span>

<span data-ttu-id="91042-104">*Ce guide de laboratoire de test peut être utilisé à la fois pour Microsoft 365'entreprise et Office 365 Entreprise environnements de test.*</span><span class="sxs-lookup"><span data-stu-id="91042-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="91042-105">Les organisations désireuses d’utiliser directement leur infrastructure d’Active Directory Domain Services (AD DS) en local pour l’authentification aux applications et services sur le cloud Microsoft peuvent utiliser l’authentification directe.</span><span class="sxs-lookup"><span data-stu-id="91042-105">Organizations that want to directly use their on-premises Active Directory Domain Services (AD DS) infrastructure for authentication to Microsoft cloud-based services and applications can use pass-through authentication.</span></span> <span data-ttu-id="91042-106">Cet article décrit comment configurer l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365. Voici la configuration que vous obtenez:</span><span class="sxs-lookup"><span data-stu-id="91042-106">This article describes how you can configure your Microsoft 365 test environment for pass-through authentication, resulting in the following configuration:</span></span>
  
![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase2.png)
  
<span data-ttu-id="91042-108">Les deux phases de configuration de cet environnement de test sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="91042-108">There are two phases to setting up this test environment:</span></span>

1.    <span data-ttu-id="91042-109">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="91042-109">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.    <span data-ttu-id="91042-110">Configuration de l’authentification directe pour Azure AD Connect sur APP1.</span><span class="sxs-lookup"><span data-stu-id="91042-110">Configure Azure AD Connect on APP1 for pass-through authentication.</span></span>
    
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="91042-112">Cliquez [ici](../downloads/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="91042-112">Click [here](../downloads/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="91042-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="91042-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="91042-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="91042-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="91042-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="91042-117">This configuration consists of:</span></span> 
  
- <span data-ttu-id="91042-118">Microsoft 365 E5 d’essai ou payant.</span><span class="sxs-lookup"><span data-stu-id="91042-118">Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="91042-119">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="91042-119">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> <span data-ttu-id="91042-120">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB AD DS avec le client Azure AD de votre abonnement Microsoft 365 de manière périodique.</span><span class="sxs-lookup"><span data-stu-id="91042-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription periodically.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-pass-through-authentication"></a><span data-ttu-id="91042-121">Phase 2 : Configuration de l’authentification directe pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="91042-121">Phase 2: Configure Azure AD Connect on APP1 for pass-through authentication</span></span>

<span data-ttu-id="91042-122">Durant cette phase, vous allez configurer Azure AD Connect sur APP1 pour qu’il utilise l’authentification directe, puis vérifier que tout fonctionne.</span><span class="sxs-lookup"><span data-stu-id="91042-122">In this phase, you configure Azure AD Connect on APP1 to use pass-through authentication, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="91042-123">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="91042-123">Configure Azure AD Connect on APP1</span></span>

1.    <span data-ttu-id="91042-124">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="91042-124">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2.    <span data-ttu-id="91042-125">Sur le bureau d’APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="91042-125">From the desktop of APP1, run Azure AD Connect.</span></span>

3.    <span data-ttu-id="91042-126">Sur la page **Bienvenue**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="91042-126">On the **Welcome page**, click **Configure**.</span></span>

4.    <span data-ttu-id="91042-127">Sur la page Tâches supplémentaires, cliquez sur **Modifier la connexion utilisateur**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="91042-127">On the Additional tasks page, click **Change user sign-in**, and then click **Next**.</span></span>

5.    <span data-ttu-id="91042-128">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="91042-128">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6.    <span data-ttu-id="91042-129">Sur la page **Connexion de l’utilisateur**, cliquez sur **Authentification directe**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="91042-129">On the **User sign-in** page, click **Pass-through authentication**, and then click **Next**.</span></span>

7.    <span data-ttu-id="91042-130">Sur la page **Prêt à configurer**, cliquez sur **Configurer**.</span><span class="sxs-lookup"><span data-stu-id="91042-130">On the **Ready to configure** page, click **Configure**.</span></span>

8.    <span data-ttu-id="91042-131">Sur la page **Configuration terminée**, cliquez sur **Quitter**.</span><span class="sxs-lookup"><span data-stu-id="91042-131">On the **Configuration complete** page, click **Exit**.</span></span>

9.    <span data-ttu-id="91042-p104">Sur le Portail Azure, dans le volet gauche, cliquez sur **Azure Active Directory > Azure AD Connect**. Vérifiez que la fonctionnalité **Authentification directe** affiche l’état **Activé**.</span><span class="sxs-lookup"><span data-stu-id="91042-p104">From the Azure portal, in the left pane, click **Azure Active Directory > Azure AD Connect**. Verify that the **Pass-through authentication** feature appears as **Enabled**.</span></span>

10.    <span data-ttu-id="91042-p105">Cliquez sur **Authentification directe**. Le volet **Authentification directe** répertorie les serveurs où vos agents d’authentification sont installés. APP1 devrait figurer dans la liste. Fermez le volet **Authentification directe**.</span><span class="sxs-lookup"><span data-stu-id="91042-p105">Click **Pass-through authentication**. The **Pass-through authentication** pane lists the servers where your Authentication Agents are installed. You should see APP1 in the list. Close the **Pass-through authentication** pane.</span></span>

<span data-ttu-id="91042-138">Ensuite, testez la possibilité de vous inscrire à votre abonnement avec le <strong>user1@testlab.</strong>\<your public domain></span><span class="sxs-lookup"><span data-stu-id="91042-138">Next, test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<your public domain></span></span> <span data-ttu-id="91042-139">nom d’utilisateur du compte utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="91042-139">user name of the User1 account.</span></span>

1. <span data-ttu-id="91042-140">Dans APP1, déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="91042-140">From APP1, sign out, and then sign in again, this time specifying a different account.</span></span>

2. <span data-ttu-id="91042-141">Quand vous êtes invité à saisir le nom d’utilisateur et le mot de passe, indiquez <strong>utilisateur1@testlab.</strong>\<your public domain></span><span class="sxs-lookup"><span data-stu-id="91042-141">When prompted for a user name and password, specify <strong>user1@testlab.</strong>\<your public domain></span></span> <span data-ttu-id="91042-142">et le mot de passe utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="91042-142">and the User1 password.</span></span> <span data-ttu-id="91042-143">Vous devez correctement vous connecter en tant qu’ Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="91042-143">You should successfully sign in as User1.</span></span>

<span data-ttu-id="91042-144">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général.</span><span class="sxs-lookup"><span data-stu-id="91042-144">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator.</span></span> <span data-ttu-id="91042-145">Par conséquent, vous ne verrez pas l’icône **Administrateur** comme une option.</span><span class="sxs-lookup"><span data-stu-id="91042-145">Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="91042-146">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="91042-146">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase2.png)
 
<span data-ttu-id="91042-148">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="91042-148">This configuration consists of:</span></span>

- <span data-ttu-id="91042-149">Un Microsoft 365 E5 d’essai ou payant avec le domaine DNS testlab.\<your domain name></span><span class="sxs-lookup"><span data-stu-id="91042-149">A Microsoft 365 E5 trial or paid subscriptions with the DNS domain testlab.\<your domain name></span></span> <span data-ttu-id="91042-150">Inscrit(e).</span><span class="sxs-lookup"><span data-stu-id="91042-150">registered.</span></span>
- <span data-ttu-id="91042-p110">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure. Un agent d’authentification s’exécute sur APP1 pour traiter les demandes d’authentification directe provenant du client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="91042-p110">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network. An Authentication Agent runs on APP1 to handle pass-through authentication requests from the Azure AD tenant of your Microsoft 365 subscription.</span></span>

## <a name="next-step"></a><span data-ttu-id="91042-153">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="91042-153">Next step</span></span>

<span data-ttu-id="91042-154">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="91042-154">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="91042-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91042-155">See also</span></span>

[<span data-ttu-id="91042-156">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="91042-156">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="91042-157">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="91042-157">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="91042-158">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="91042-158">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)