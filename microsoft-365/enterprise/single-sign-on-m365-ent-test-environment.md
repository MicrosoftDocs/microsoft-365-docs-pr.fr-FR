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
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom:
- TLGS
- Ent_TLGs
ms.assetid: ''
description: 'Résumé : Configurez et testez l’authentification unique transparente Azure AD pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: f98f82de50feb2a9f92d1ecc4775c5307b314a72
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487599"
---
# <a name="azure-ad-seamless-single-sign-on-for-your-microsoft-365-test-environment"></a><span data-ttu-id="db82e-103">Authentification unique transparente Azure AD pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="db82e-103">Azure AD Seamless Single Sign-on for your Microsoft 365 test environment</span></span>

<span data-ttu-id="db82e-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="db82e-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="db82e-p101">La Sign-On unique transparente Azure AD (authentification unique transparente) se connecte automatiquement aux utilisateurs lorsqu’ils se trouvent sur leurs PC ou appareils connectés au réseau de leur organisation. L’authentification unique transparente Azure AD permet aux utilisateurs d’accéder facilement aux applications basées sur le Cloud sans avoir besoin de composants locaux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="db82e-p101">Azure AD Seamless Single Sign-On (Seamless SSO) automatically signs in users when they are on their PCs or devices that are connected to their organization network. Azure AD Seamless SSO provides users with easy access to cloud-based applications without needing any additional on-premises components.</span></span>

<span data-ttu-id="db82e-107">Cet article explique comment configurer l’authentification unique transparente pour Azure AD pour votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db82e-107">This article describes how to configure your Microsoft 365 test environment for Azure AD Seamless SSO.</span></span>

<span data-ttu-id="db82e-108">La configuration de l’authentification unique transparente Azure AD implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="db82e-108">Setting up Azure AD Seamless SSO involves two phases:</span></span>
- [<span data-ttu-id="db82e-109">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="db82e-109">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>](#phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment)
- [<span data-ttu-id="db82e-110">Phase 2 : Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="db82e-110">Phase 2: Configure Azure AD Connect on APP1 for Azure AD Seamless SSO</span></span>](#phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso)
   
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="db82e-112">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="db82e-112">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="db82e-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="db82e-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="db82e-114">Suivez les instructions de la [synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="db82e-114">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md).</span></span> 

<span data-ttu-id="db82e-115">La configuration obtenue se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="db82e-115">Your resulting configuration looks like this:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="db82e-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="db82e-117">This configuration consists of:</span></span>
  
- <span data-ttu-id="db82e-118">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="db82e-118">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="db82e-119">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="db82e-119">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>
- <span data-ttu-id="db82e-120">Azure AD Connect s’exécute sur APP1 pour synchroniser régulièrement le domaine des services de domaine Active Directory (AD DS) TESTLAB avec le client Azure AD de votre abonnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db82e-120">Azure AD Connect runs on APP1 to periodically synchronize the TESTLAB Active Directory Domain Services (AD DS) domain to the Azure AD tenant of your Microsoft 365 subscription.</span></span>

## <a name="phase-2-configure-azure-ad-connect-on-app1-for-azure-ad-seamless-sso"></a><span data-ttu-id="db82e-121">Phase 2 : Configuration de l’authentification unique transparente Azure AD pour Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="db82e-121">Phase 2: Configure Azure AD Connect on APP1 for Azure AD Seamless SSO</span></span>

<span data-ttu-id="db82e-122">Dans cette phase, configurez Azure AD Connect sur APP1 for Azure AD transparent SSO, puis vérifiez qu’elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="db82e-122">In this phase, configure Azure AD Connect on APP1 for Azure AD Seamless SSO, and then verify that it works.</span></span>

### <a name="configure-azure-ad-connect-on-app1"></a><span data-ttu-id="db82e-123">Configuration d’Azure AD Connect sur APP1</span><span class="sxs-lookup"><span data-stu-id="db82e-123">Configure Azure AD Connect on APP1</span></span>

1. <span data-ttu-id="db82e-124">Dans le [Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="db82e-124">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="db82e-125">À partir du Bureau APP1, exécutez Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="db82e-125">From the APP1 desktop, run Azure AD Connect.</span></span>

3. <span data-ttu-id="db82e-126">Sur la **page Bienvenue**, sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="db82e-126">On the **Welcome page**, select **Configure**.</span></span>

4. <span data-ttu-id="db82e-127">Sur la page **tâches supplémentaires** , sélectionnez **modifier la connexion de l’utilisateur**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db82e-127">On the **Additional tasks** page, select **Change user sign-in**, and then select **Next**.</span></span>

5. <span data-ttu-id="db82e-128">Sur la page **connexion à Azure ad** , entrez les informations d’identification de votre compte d’administrateur général, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db82e-128">On the **Connect to Azure AD** page, enter your global administrator account credentials, and then select **Next**.</span></span>

6. <span data-ttu-id="db82e-129">Sur la page de connexion de l' **utilisateur** , sélectionnez **activer l’authentification unique**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db82e-129">On the **User sign-in** page, select **Enable single sign-on**, and then select **Next**.</span></span>

7. <span data-ttu-id="db82e-130">Sur la page **activer l’authentification unique** , sélectionnez **entrer les informations d’identification**.</span><span class="sxs-lookup"><span data-stu-id="db82e-130">On the **Enable single sign-on** page, select **Enter credentials**.</span></span>

8. <span data-ttu-id="db82e-131">Dans la boîte de dialogue **sécurité Windows** , entrez **utilisateur1** et le mot de passe du compte User1, sélectionnez **OK**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db82e-131">In the **Windows Security** dialog box, enter **user1** and the password of the user1 account, select **OK**, and then select **Next**.</span></span>

9. <span data-ttu-id="db82e-132">Sur la page **prêt à configurer** , sélectionnez **configurer**.</span><span class="sxs-lookup"><span data-stu-id="db82e-132">On the **Ready to Configure** page, select **Configure**.</span></span>

10. <span data-ttu-id="db82e-133">Sur la page **Configuration terminée** , sélectionnez **quitter**.</span><span class="sxs-lookup"><span data-stu-id="db82e-133">On the **Configuration complete** page, select **Exit**.</span></span>

11. <span data-ttu-id="db82e-134">À partir du portail Azure, dans le volet de gauche, sélectionnez **Azure Active Directory**  >  **Azure ad Connect**.</span><span class="sxs-lookup"><span data-stu-id="db82e-134">From the Azure portal, in the left pane, select **Azure Active Directory** > **Azure AD Connect**.</span></span> <span data-ttu-id="db82e-135">Vérifiez que la fonctionnalité **d’authentification unique transparente** apparaît comme **activée**.</span><span class="sxs-lookup"><span data-stu-id="db82e-135">Verify that the **Seamless single sign-on** feature appears as **Enabled**.</span></span>

<span data-ttu-id="db82e-136">Ensuite, testez la capacité à se connecter à votre abonnement avec le <strong>User1@testlab.</strong>\<*your public domain*></span><span class="sxs-lookup"><span data-stu-id="db82e-136">Next, test the ability to sign in to your subscription with the <strong>user1@testlab.</strong>\<*your public domain*></span></span> <span data-ttu-id="db82e-137">nom d’utilisateur du compte utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="db82e-137">user name of the User1 account.</span></span>

1. <span data-ttu-id="db82e-138">À partir d’Internet Explorer sur APP1, sélectionnez l’icône Paramètres, puis sélectionnez **Options Internet**.</span><span class="sxs-lookup"><span data-stu-id="db82e-138">From Internet Explorer on APP1, select the settings icon, and then select **Internet Options**.</span></span>
 
2. <span data-ttu-id="db82e-139">Dans **Options Internet**, sélectionnez l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="db82e-139">In **Internet Options**, select the **Security** tab.</span></span>

3. <span data-ttu-id="db82e-140">Sélectionnez **Intranet local**, puis **sites**.</span><span class="sxs-lookup"><span data-stu-id="db82e-140">Select **Local intranet**, and then select **Sites**.</span></span>

4. <span data-ttu-id="db82e-141">Dans **Intranet local**, sélectionnez **avancé**.</span><span class="sxs-lookup"><span data-stu-id="db82e-141">In **Local intranet**, select **Advanced**.</span></span>

5. <span data-ttu-id="db82e-142">Dans **ajouter ce site Web à la zone**, entrez **https<span>://</span>AutoLogon.microsoftazuread-SSO.com**, sélectionnez **Ajouter**  >  **Fermer**  >  **OK**  >  **OK**.</span><span class="sxs-lookup"><span data-stu-id="db82e-142">In **Add this website to the zone**, enter **https<span>://</span>autologon.microsoftazuread-sso.com**, select **Add** > **Close** > **OK** > **OK**.</span></span>

6. <span data-ttu-id="db82e-143">Déconnectez-vous, puis reconnectez-vous avec un compte différent.</span><span class="sxs-lookup"><span data-stu-id="db82e-143">Sign out, and then sign in again, this time specifying a different account.</span></span>

7. <span data-ttu-id="db82e-144">Lorsque vous êtes invité à vous connecter, spécifiez <strong>User1@testlab.</strong>\<*your public domain*></span><span class="sxs-lookup"><span data-stu-id="db82e-144">When prompted to sign in, specify <strong>user1@testlab.</strong>\<*your public domain*></span></span> <span data-ttu-id="db82e-145">nom, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="db82e-145">name, and then select **Next**.</span></span> <span data-ttu-id="db82e-146">Vous devez correctement vous connecter en tant que User1 sans entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="db82e-146">You should successfully sign in as User1 without being prompted for a password.</span></span> <span data-ttu-id="db82e-147">Cela prouve qu’ Azure AD transparente SSO fonctionne.</span><span class="sxs-lookup"><span data-stu-id="db82e-147">This proves that Azure AD Seamless SSO is working.</span></span>

<span data-ttu-id="db82e-148">Veuillez noter que même si l’utilisateur User1 dispose des autorisations d’administrateur pour le domaine TESTLAB AD DS, il n’est pas un administrateur général pour Azure AD.</span><span class="sxs-lookup"><span data-stu-id="db82e-148">Notice that although User1 has domain administrator permissions for the TESTLAB AD DS domain, it is not a global administrator for Azure AD.</span></span> <span data-ttu-id="db82e-149">Par conséquent, vous ne verrez pas l’icône**Administrateur**comme une option.</span><span class="sxs-lookup"><span data-stu-id="db82e-149">Therefore, you will not see the **Admin** icon as an option.</span></span>

<span data-ttu-id="db82e-150">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="db82e-150">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)

<span data-ttu-id="db82e-152">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="db82e-152">This configuration consists of:</span></span>

- <span data-ttu-id="db82e-153">Un abonnement d’évaluation ou payant Microsoft 365 E5 avec le domaine DNS testlab.\<*your domain name*></span><span class="sxs-lookup"><span data-stu-id="db82e-153">A Microsoft 365 E5 trial or paid subscriptions with the DNS domain testlab.\<*your domain name*></span></span> <span data-ttu-id="db82e-154">Inscrit(e).</span><span class="sxs-lookup"><span data-stu-id="db82e-154">registered.</span></span>
- <span data-ttu-id="db82e-155">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="db82e-155">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>
- <span data-ttu-id="db82e-156">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de votre abonnement Microsoft 365 au domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="db82e-156">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Microsoft 365 subscription to the TESTLAB AD DS domain.</span></span>
- <span data-ttu-id="db82e-157">L’authentification unique transparente Azure AD est activée afin que les ordinateurs de l’intranet simulé puissent se connecter aux ressources cloud de Microsoft 365 sans spécifier de mot de passe de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db82e-157">Azure AD Seamless SSO is enabled so that computers on the simulated intranet can sign in to Microsoft 365 cloud resources without specifying a user account password.</span></span>

## <a name="next-step"></a><span data-ttu-id="db82e-158">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="db82e-158">Next step</span></span>

<span data-ttu-id="db82e-159">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="db82e-159">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="db82e-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db82e-160">See also</span></span>

[<span data-ttu-id="db82e-161">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="db82e-161">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="db82e-162">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="db82e-162">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="db82e-163">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="db82e-163">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
