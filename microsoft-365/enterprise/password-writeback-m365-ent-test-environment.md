---
title: Écriture différée de mot de passe pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/20/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- TLGS
- Ent_TLGs
ms.assetid: ''
description: 'Résumé: Configurez l’écriture différée du mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 748ccaf8601d9e9564d176f2368e3cc71f926208
ms.sourcegitcommit: 73fb9a7cf1b7b1045a304391ed393acb7b909317
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/13/2018
ms.locfileid: "27241977"
---
# <a name="password-writeback-for-your-microsoft-365-test-environment"></a><span data-ttu-id="50328-103">Écriture différée de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="50328-103">Password writeback for your Microsoft 365 test environment</span></span>

<span data-ttu-id="50328-p101">La réinitialisation du mot de passe permet aux utilisateurs de mettre à jour leur mot de passe via Azure Active Directory (AD), qui est ensuite copié sur votre instance Windows Server Active Directory (AD) locale. Avec l’écriture différée de mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe localement via Windows Server AD où les comptes d’utilisateurs et leurs attributs sont stockés. Cette étape est utile aux utilisateurs itinérants ou distants qui ne disposent pas d’une connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="50328-p101">Password writeback allows users to update their passwords through Azure Active Directory (AD), which is then replicated to your local Windows Server Active Directory (AD). With password writeback, users don’t need to update their passwords through the on-premises Windows Server AD where their original user accounts are stored. This helps roaming or remote users who do not have a remote access connection to their on-premises network.</span></span>

<span data-ttu-id="50328-107">Cet article décrit comment configurer l’écriture différée Azure AD pour votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="50328-107">This article describes how you can configure your Microsoft 365 test environment for password writeback.</span></span>

<span data-ttu-id="50328-108">Il existe deux phases de configuration :</span><span class="sxs-lookup"><span data-stu-id="50328-108">There are two phases to setting this up:</span></span>

1.  <span data-ttu-id="50328-109">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="50328-109">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.  <span data-ttu-id="50328-110">Activer l’écriture différée de mot de passe pour le domaine TESTLAB Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="50328-110">Enable password writeback for the TESTLAB Windows Server AD domain.</span></span>
    
![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="50328-112">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="50328-112">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="50328-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="50328-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="50328-p102">Suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe pour Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="50328-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="50328-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="50328-117">This configuration consists of:</span></span> 
  
- <span data-ttu-id="50328-118">Les abonnements à la version permanente ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="50328-118">Office 365 E5 and EMS E5 trial or permanent subscriptions.</span></span>
- <span data-ttu-id="50328-119">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="50328-119">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="50328-120">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine Windows Server AD TESTLAB avec le client Azure AD de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="50328-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB Windows Server AD domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions.</span></span>

## <a name="phase-2-enable-password-writeback-for-the-testlab-windows-server-ad-domain"></a><span data-ttu-id="50328-121">Phase 2: activer l’écriture différée de mot de passe pour le domaine TESTLAB Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="50328-121">Phase 2: Enable password writeback for the TESTLAB Windows Server AD domain</span></span>

<span data-ttu-id="50328-122">Tout d’abord, configurez le compte utilisateur 1 avec le rôle d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="50328-122">First, configure the User 1 account with the global administrator role.</span></span>

1. <span data-ttu-id="50328-123">À partir du[portail Office](https://office.com), connectez-vous avec votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="50328-123">From the [Office portal](https://office.com), sign in with your global administrator account.</span></span>

2. <span data-ttu-id="50328-p103">Cliquez sur la vignette**administrateur**. À partir du nouvel onglet **centre d’administration Microsoft 365**de votre navigateur, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="50328-p103">Click the **Admin** tile. From the new **Microsoft 365 admin center** tab of your browser, click **Active users**.</span></span>
 
3. <span data-ttu-id="50328-126">Sur la page**Activer les utilisateurs**, cliquez sur le compte**Utilisateur1**,</span><span class="sxs-lookup"><span data-stu-id="50328-126">On the **Active users** page, click the **user1** account,</span></span>

4. <span data-ttu-id="50328-127">Sur le volet**user1**, cliquez sur **Modifier** près de**Rôles**.</span><span class="sxs-lookup"><span data-stu-id="50328-127">On the **user1** pane, click **Edit** next to **Roles**.</span></span>

5. <span data-ttu-id="50328-p104">Sur le volet pour user1**Modifier les rôles d’utilisateur**, cliquez sur**Administrateur général**. Cliquez sur **Enregistrer**, puis cliquez sur**Fermer**.</span><span class="sxs-lookup"><span data-stu-id="50328-p104">On the **Edit user roles** pane for user1, click **Global administrator**. Click **Save**, and then click **Close**.</span></span>

<span data-ttu-id="50328-130">Configurez ensuite le compte utilisateur 1 grâce aux paramètres de sécurité qui lui permettent de modifier le mot de passe pour le compte d’autres utilisateurs dans le domaine TESTLAB Windows Server AD.</span><span class="sxs-lookup"><span data-stu-id="50328-130">Next, configure the User 1 account with the security settings that allow it to change passwords on behalf of other users in the TESTLAB Windows Server AD domain.</span></span>

1. <span data-ttu-id="50328-131">À partir du[Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="50328-131">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2.  <span data-ttu-id="50328-132">À partir du bureau du APP1, cliquez sur**Démarrer**, tapez **actif**, puis cliquez sur **Utilisateurs et ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="50328-132">From the desktop of APP1, click **Start**, type **active**, and then click **Active Directory Users and Computers**.</span></span>

3. <span data-ttu-id="50328-p105">Cliquez sur **Affichage** dans la barre de menu. Si**Fonctionnalités avancées** n’est ne pas activée, cliquez dessus pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="50328-p105">Click **View** in the menu bar. If **Advanced features** is not enabled, click it to enable it.</span></span>

4. <span data-ttu-id="50328-135">Dans le volet d’arborescence, cliquez sur votre domaine avec le bouton droit, cliquez sur**Propriétés**, puis cliquez sur l’onglet**Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="50328-135">In the tree pane, right-click your domain, click **Properties**, and then click the **Security** tab.</span></span>

5. <span data-ttu-id="50328-136">Cliquez sur**Avancé**.</span><span class="sxs-lookup"><span data-stu-id="50328-136">Click **Advanced**.</span></span>

6. <span data-ttu-id="50328-137">Sous l'onglet**Autorisations**, cliquez sur**Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="50328-137">On the **Permissions** tab, click **Add**.</span></span>

7. <span data-ttu-id="50328-138">Cliquez sur**Sélectionnez un principal**, tapez**Utilisateur1**, puis cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="50328-138">Click **Select a principal**, type **User1**, and then click **OK**.</span></span>

8. <span data-ttu-id="50328-139">Dans**S’applique à**, sélectionnez **Objets utilisateur Descendant**.</span><span class="sxs-lookup"><span data-stu-id="50328-139">In **Applies to**, select **Descendant User objects**.</span></span>

9. <span data-ttu-id="50328-140">Sous**Autorisations**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="50328-140">Under **Permissions**, select the following:</span></span>

    - <span data-ttu-id="50328-141">Modifier le mot de passe</span><span class="sxs-lookup"><span data-stu-id="50328-141">Change password</span></span>
    - <span data-ttu-id="50328-142">Réinitialiser le mot de passe</span><span class="sxs-lookup"><span data-stu-id="50328-142">Reset password</span></span>

10. <span data-ttu-id="50328-143">Sous**Propriétés**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="50328-143">Under **Properties**, select the following:</span></span>
    - <span data-ttu-id="50328-144">Écrire lockoutTime</span><span class="sxs-lookup"><span data-stu-id="50328-144">Write lockoutTime</span></span>
    - <span data-ttu-id="50328-145">Écrire pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="50328-145">Write pwdLastSet</span></span>

11. <span data-ttu-id="50328-146">Cliquez trois fois sur **OK** pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="50328-146">Click **OK** three times to save the changes.</span></span>

12. <span data-ttu-id="50328-147">Fermer**Utilisateurs et Ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="50328-147">Close **Active Directory Users and Computers**.</span></span>

<span data-ttu-id="50328-148">Ensuite, configurez de la Connexion Azure AD Connect sur APP1 pour écriture différée.</span><span class="sxs-lookup"><span data-stu-id="50328-148">Next, configure Azure AD Connect on APP1 for password writeback.</span></span>

1. <span data-ttu-id="50328-149">Si nécessaire, connectez-vous à APP1 avec le compte TESTLAB\User1.</span><span class="sxs-lookup"><span data-stu-id="50328-149">If needed, connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="50328-150">À partir du bureau d’APP1, double-cliquez sur **Azure AD Connect**.</span><span class="sxs-lookup"><span data-stu-id="50328-150">From the desktop of APP1, double-click **Azure AD Connect**.</span></span>

3. <span data-ttu-id="50328-151">Sur la page**Bienvenue**, cliquez sur**Configurer**.</span><span class="sxs-lookup"><span data-stu-id="50328-151">On the **Welcome page**, click **Configure**.</span></span>

4. <span data-ttu-id="50328-152">Sur la page**Tâches supplémentaires**, sélectionnez sur**Personnaliser les options de synchronisation**, puis cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="50328-152">On the **Additional tasks** page, click **Customize synchronization options**, and then click **Next**.</span></span>

5. <span data-ttu-id="50328-153">Sur la page**Connexion à Azure AD**, tapez vos informations d’identification de l’utilisateur1, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="50328-153">On the **Connect to Azure AD** page, type the User 1 account credentials, and then click **Next**.</span></span>

6. <span data-ttu-id="50328-154">Sur les pages**Connecter les répertoires** et **Domaine/Filtrage**, cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="50328-154">On the **Connect directories** and **Domain/OU filtering** pages, click **Next**.</span></span>

7. <span data-ttu-id="50328-155">Sur la page**Fonctionnalités facultatives**, sélectionnez **Écriture différée de mot de passe** et cliquez sur Suivant.</span><span class="sxs-lookup"><span data-stu-id="50328-155">On the **Optional features** page, select **Password writeback** and click Next.</span></span> 

8. <span data-ttu-id="50328-156">Sur la page**Prêt à configurer**, cliquez sur**Configurer** et attendez que le processus se termine.</span><span class="sxs-lookup"><span data-stu-id="50328-156">On the **Ready to configure** page, click **Configure** and wait for the process to finish.</span></span>

9. <span data-ttu-id="50328-157">Lorsque vous voyez que la configuration se termine, cliquez sur **Sortie**.</span><span class="sxs-lookup"><span data-stu-id="50328-157">When you see the configuration finish, click **Exit**.</span></span>

<span data-ttu-id="50328-158">Vous êtes maintenant prêt à tester l’écriture différée de mot de passe pour les utilisateurs sur des ordinateurs sur lesquels vous n’êtes pas connecté au réseau virtuel de votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="50328-158">You are now ready to test password writeback for users on computers that are not connected to the virtual network of your simulated intranet.</span></span>

<span data-ttu-id="50328-159">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="50328-159">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)

<span data-ttu-id="50328-161">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="50328-161">This configuration consists of:</span></span>

- <span data-ttu-id="50328-162">Les abonnements à la version permanente ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="50328-162">Office 365 E5 and EMS E5 trial or permanent subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span>
- <span data-ttu-id="50328-163">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="50328-163">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="50328-164">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de vos abonnements Office 365 et EMS E5 au domaine Windows Server AD TESTLAB.</span><span class="sxs-lookup"><span data-stu-id="50328-164">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Office 365 and EMS E5 subscriptions to the TESTLAB Windows Server AD domain.</span></span> 
- <span data-ttu-id="50328-165">L’écriture différée de mot de passe est activée afin que les utilisateurs puissent modifier leur mot de passe via Azure AD sans avoir à se connecter à l’intranet simplifiée.</span><span class="sxs-lookup"><span data-stu-id="50328-165">Password writeback is enabled so that users can change their passwords through Azure AD without having to be connected to the simplified intranet.</span></span>

<span data-ttu-id="50328-166">Consultez l’étape [Simplifier les réinitialisations de mot de passe](identity-password-writeback.md) de la phase d’identification pour obtenir des informations et des liens qui vous permettront de configurer l’écriture différée de mot de passe en production.</span><span class="sxs-lookup"><span data-stu-id="50328-166">See the [Simplify password updates](identity-password-writeback.md) step in the Identity phase for information and links to configure password writeback in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="50328-167">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="50328-167">Next step</span></span>

<span data-ttu-id="50328-168">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="50328-168">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="50328-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50328-169">See also</span></span>

[<span data-ttu-id="50328-170">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="50328-170">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="50328-171">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="50328-171">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="50328-172">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="50328-172">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


