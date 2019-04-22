---
title: Écriture différée de mot de passe pour votre environnement de test Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/16/2019
ms.audience: ITPro
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
description: 'Résumé: Configurez l’écriture différée du mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: 11a0efbae09c36098a19725187cd43b53850f4fc
ms.sourcegitcommit: db52a11eb192a28dbec827c565e36ad4a81d8e3f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2019
ms.locfileid: "31901218"
---
# <a name="password-writeback-for-your-microsoft-365-test-environment"></a><span data-ttu-id="835f9-103">Écriture différée de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="835f9-103">Password writeback for your Microsoft 365 test environment</span></span>

<span data-ttu-id="835f9-p101">La réinitialisation du mot de passe permet aux utilisateurs de mettre à jour leur mot de passe via Azure Active Directory (Azure AD), qui est ensuite copié sur votre instance Active Directory Domain Services (AD DS) locale. Avec l’écriture différée de mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe localement via Active Directory Domain Services (AD DS) où les comptes d’utilisateurs et leurs attributs sont stockés. Cette étape est utile aux utilisateurs itinérants ou distants qui ne disposent pas d’une connexion d’accès à distance au réseau local.</span><span class="sxs-lookup"><span data-stu-id="835f9-p101">Password writeback allows users to update their passwords through Azure Active Directory (Azure AD), which is then replicated to your local Active Directory Domain Services (AD DS). With password writeback, users don’t need to update their passwords through the on-premises Windows Server AD where their original user accounts are stored. This helps roaming or remote users who do not have a remote access connection to their on-premises network.</span></span>

<span data-ttu-id="835f9-107">Cet article décrit comment configurer l’écriture différée Azure AD pour votre environnement de test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="835f9-107">This article describes how you can configure your Microsoft 365 test environment for password writeback.</span></span>

<span data-ttu-id="835f9-108">Il existe deux phases de configuration :</span><span class="sxs-lookup"><span data-stu-id="835f9-108">There are two phases to setting this up:</span></span>

1.  <span data-ttu-id="835f9-109">Création de l’environnement de test Microsoft 365 de l’entreprise simulée avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="835f9-109">Create the Microsoft 365 simulated enterprise test environment with password hash synchronization.</span></span>
2.  <span data-ttu-id="835f9-110">Activer l’écriture différée de mot de passe pour le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="835f9-110">Enable password writeback for the TESTLAB Windows Server AD domain.</span></span>
    
![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="835f9-112">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="835f9-112">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-configure-password-hash-synchronization-and-password-reset-for-your-microsoft-365-test-environment"></a><span data-ttu-id="835f9-113">Étape 1 : Configuration de la synchronisation de hachage de mot de passe et réinitialisation du mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="835f9-113">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="835f9-p102">Tout d’abord, suivez les instructions fournies dans l’article [Synchronisation de hachage de mot de passe](password-hash-sync-m365-ent-test-environment.md). Voici la configuration que vous obtenez.</span><span class="sxs-lookup"><span data-stu-id="835f9-p102">Follow the instructions in [password hash synchronization for Microsoft 365](password-hash-sync-m365-ent-test-environment.md). Here is your resulting configuration.</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="835f9-117">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="835f9-117">This configuration consists of:</span></span> 
  
- <span data-ttu-id="835f9-118">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="835f9-118">Office 365 E5 and EMS E5 trial or paid subscriptions.</span></span>
- <span data-ttu-id="835f9-119">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-119">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="835f9-120">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine Windows Server AD DS avec le client Azure AD, le client de vos abonnements Office 365 et EMS E5.</span><span class="sxs-lookup"><span data-stu-id="835f9-120">Azure AD Connect runs on APP1 to synchronize the TESTLAB Windows Server AD domain to the Azure AD tenant of your Office 365 and EMS E5 subscriptions.</span></span>

<span data-ttu-id="835f9-121">Ensuite, suivez les instructions du Guide de laboratoire de Test dans la [Phase 2 de la réinitialisation de mot de passe](password-reset-m365-ent-test-environment.md#phase-2-configure-and-test-password-reset).</span><span class="sxs-lookup"><span data-stu-id="835f9-121">Next, follow the instructions in [Phase 2 of the password reset](password-reset-m365-ent-test-environment.md#phase-2-configure-and-test-password-reset) Test Lab Guide.</span></span>

<span data-ttu-id="835f9-122">La fonction de réinitialisation du mot de passe doit être activée pour utiliser l’écriture différée du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="835f9-122">You must have password reset enabled to use password writeback.</span></span>

## <a name="phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain"></a><span data-ttu-id="835f9-123">Phase 2 : Activer l’écriture différée de mot de passe pour le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="835f9-123">Phase 2: Enable password writeback for the TESTLAB Windows Server AD domain</span></span>

<span data-ttu-id="835f9-124">Tout d’abord, configurez le compte utilisateur 1 avec le rôle d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="835f9-124">First, configure the User 1 account with the global administrator role.</span></span>

1. <span data-ttu-id="835f9-125">À partir du[portail Office](https://office.com), connectez-vous avec votre compte Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="835f9-125">From the [Office portal](https://office.com), sign in with your global administrator account.</span></span>

2. <span data-ttu-id="835f9-p103">Cliquez sur la vignette**administrateur**. À partir du nouvel onglet **centre d’administration Microsoft 365**de votre navigateur, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="835f9-p103">Click the **Admin** tile. From the new **Microsoft 365 admin center** tab of your browser, click **Active users**.</span></span>
 
3. <span data-ttu-id="835f9-128">Sur la page**Activer les utilisateurs**, cliquez sur le compte**Utilisateur1**,</span><span class="sxs-lookup"><span data-stu-id="835f9-128">On the **Active users** page, click the **user1** account,</span></span>

4. <span data-ttu-id="835f9-129">Sur le volet**user1**, cliquez sur **Modifier** près de**Rôles**.</span><span class="sxs-lookup"><span data-stu-id="835f9-129">On the **user1** pane, click **Edit** next to **Roles**.</span></span>

5. <span data-ttu-id="835f9-p104">Sur le volet pour user1**Modifier les rôles d’utilisateur**, cliquez sur**Administrateur général**. Cliquez sur **Enregistrer**, puis cliquez sur**Fermer**.</span><span class="sxs-lookup"><span data-stu-id="835f9-p104">On the **Edit user roles** pane for user1, click **Global administrator**. Click **Save**, and then click **Close**.</span></span>

<span data-ttu-id="835f9-132">Configurez ensuite le compte utilisateur 1 en lui attribuant les paramètres de sécurité qui lui permettent de modifier le mot de passe pour le compte d’autres utilisateurs dans le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="835f9-132">Next, configure the User 1 account with the security settings that allow it to change passwords on behalf of other users in the TESTLAB Windows Server AD domain.</span></span>

1. <span data-ttu-id="835f9-133">À partir du[Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="835f9-133">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2.  <span data-ttu-id="835f9-134">À partir du bureau du APP1, cliquez sur**Démarrer**, tapez **actif**, puis cliquez sur **Utilisateurs et ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="835f9-134">From the desktop of APP1, click **Start**, type **active**, and then click **Active Directory Users and Computers**.</span></span>

3. <span data-ttu-id="835f9-p105">Cliquez sur **Affichage** dans la barre de menu. Si**Fonctionnalités avancées** n’est ne pas activée, cliquez dessus pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="835f9-p105">Click **View** in the menu bar. If **Advanced features** is not enabled, click it to enable it.</span></span>

4. <span data-ttu-id="835f9-137">Dans le volet d’arborescence, cliquez sur votre domaine avec le bouton droit, cliquez sur**Propriétés**, puis cliquez sur l’onglet**Sécurité**.</span><span class="sxs-lookup"><span data-stu-id="835f9-137">In the tree pane, right-click your domain, click **Properties**, and then click the **Security** tab.</span></span>

5. <span data-ttu-id="835f9-138">Cliquez sur**Avancé**.</span><span class="sxs-lookup"><span data-stu-id="835f9-138">Click **Advanced**.</span></span>

6. <span data-ttu-id="835f9-139">Sous l'onglet**Autorisations**, cliquez sur**Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="835f9-139">On the **Permissions** tab, click **Add**.</span></span>

7. <span data-ttu-id="835f9-140">Cliquez sur**Sélectionnez un principal**, tapez**Utilisateur1**, puis cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="835f9-140">Click **Select a principal**, type **User1**, and then click **OK**.</span></span>

8. <span data-ttu-id="835f9-141">Dans**S’applique à**, sélectionnez **Objets utilisateur Descendant**.</span><span class="sxs-lookup"><span data-stu-id="835f9-141">In **Applies to**, select **Descendant User objects**.</span></span>

9. <span data-ttu-id="835f9-142">Sous**Autorisations**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="835f9-142">Under **Permissions**, select the following:</span></span>

    - <span data-ttu-id="835f9-143">Modifier le mot de passe</span><span class="sxs-lookup"><span data-stu-id="835f9-143">Change password</span></span>
    - <span data-ttu-id="835f9-144">Réinitialiser le mot de passe</span><span class="sxs-lookup"><span data-stu-id="835f9-144">Reset password</span></span>

10. <span data-ttu-id="835f9-145">Sous**Propriétés**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="835f9-145">Under **Properties**, select the following:</span></span>
    - <span data-ttu-id="835f9-146">Écrire lockoutTime</span><span class="sxs-lookup"><span data-stu-id="835f9-146">Write lockoutTime</span></span>
    - <span data-ttu-id="835f9-147">Écrire pwdLastSet</span><span class="sxs-lookup"><span data-stu-id="835f9-147">Write pwdLastSet</span></span>

11. <span data-ttu-id="835f9-148">Cliquez trois fois sur **OK** pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="835f9-148">Click **OK** three times to save the changes.</span></span>

12. <span data-ttu-id="835f9-149">Fermer**Utilisateurs et Ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="835f9-149">Close **Active Directory Users and Computers**.</span></span>

<span data-ttu-id="835f9-150">Ensuite, configurez de la Connexion Azure AD Connect sur APP1 pour écriture différée.</span><span class="sxs-lookup"><span data-stu-id="835f9-150">Next, configure Azure AD Connect on APP1 for password writeback.</span></span>

1. <span data-ttu-id="835f9-151">Si nécessaire, connectez-vous à APP1 avec le compte TESTLAB\User1.</span><span class="sxs-lookup"><span data-stu-id="835f9-151">If needed, connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="835f9-152">À partir du bureau d’APP1, double-cliquez sur **Azure AD Connect**.</span><span class="sxs-lookup"><span data-stu-id="835f9-152">From the desktop of APP1, double-click **Azure AD Connect**.</span></span>

3. <span data-ttu-id="835f9-153">Sur la page**Bienvenue**, cliquez sur**Configurer**.</span><span class="sxs-lookup"><span data-stu-id="835f9-153">On the **Welcome page**, click **Configure**.</span></span>

4. <span data-ttu-id="835f9-154">Sur la page**Tâches supplémentaires**, sélectionnez sur**Personnaliser les options de synchronisation**, puis cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="835f9-154">On the **Additional tasks** page, click **Customize synchronization options**, and then click **Next**.</span></span>

5. <span data-ttu-id="835f9-155">Sur la page **Connexion à Azure AD**, tapez vos informations d’identification d’administrateur général, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="835f9-155">On the **Connect to Azure AD** page, type your global administrator account credentials, and then click **Next**.</span></span>

6. <span data-ttu-id="835f9-156">Sur les pages**Connecter les répertoires** et **Domaine/Filtrage**, cliquez sur**Suivant**.</span><span class="sxs-lookup"><span data-stu-id="835f9-156">On the **Connect directories** and **Domain/OU filtering** pages, click **Next**.</span></span>

7. <span data-ttu-id="835f9-157">Sur la page\*\* Fonctionnalités facultatives\*\*, sélectionnez **Écriture différée de mot de passe** et cliquez sur **Suivan**t.</span><span class="sxs-lookup"><span data-stu-id="835f9-157">On the **Optional features** page, select **Password writeback** and click **Next**.</span></span> 

8. <span data-ttu-id="835f9-158">Sur la page**Prêt à configurer**, cliquez sur**Configurer** et attendez que le processus se termine.</span><span class="sxs-lookup"><span data-stu-id="835f9-158">On the **Ready to configure** page, click **Configure** and wait for the process to finish.</span></span>

9. <span data-ttu-id="835f9-159">Lorsque vous voyez que la configuration se termine, cliquez sur **Sortie**.</span><span class="sxs-lookup"><span data-stu-id="835f9-159">When you see the configuration finish, click **Exit**.</span></span>

<span data-ttu-id="835f9-160">Vous êtes maintenant prêt à tester l’écriture différée de mot de passe pour les utilisateurs sur des ordinateurs sur lesquels vous n’êtes pas connecté au réseau virtuel de votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="835f9-160">You are now ready to test password writeback for users on computers that are not connected to the virtual network of your simulated intranet.</span></span>

<span data-ttu-id="835f9-161">Voici la configuration obtenue :</span><span class="sxs-lookup"><span data-stu-id="835f9-161">Here is your resulting configuration:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](media/pass-through-auth-m365-ent-test-environment/Phase1.png)

<span data-ttu-id="835f9-163">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="835f9-163">This configuration consists of:</span></span>

- <span data-ttu-id="835f9-164">Les abonnements à la version payante ou d’évaluation Office 365 E5 et EMS E5 avec le domaine DNS TESTLAB.\<votre nom de domaine> enregistré.</span><span class="sxs-lookup"><span data-stu-id="835f9-164">Office 365 E5 and EMS E5 trial or paid subscriptions with the DNS domain TESTLAB.\<your domain name> registered.</span></span>
- <span data-ttu-id="835f9-165">Un intranet d’organisation simplifié connecté à Internet, qui se compose des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-165">A simplified organization intranet connected to the Internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span> 
- <span data-ttu-id="835f9-166">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de vos abonnements Office 365 et EMS E5 au domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="835f9-166">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Office 365 and EMS E5 subscriptions to the TESTLAB Windows Server AD domain.</span></span> 
- <span data-ttu-id="835f9-167">L’écriture différée de mot de passe est activée afin que les utilisateurs puissent modifier leur mot de passe via Azure AD sans avoir à se connecter à l’intranet simplifiée.</span><span class="sxs-lookup"><span data-stu-id="835f9-167">Password writeback is enabled so that users can change their passwords through Azure AD without having to be connected to the simplified intranet.</span></span>

<span data-ttu-id="835f9-168">Consultez l’étape [Simplifier les réinitialisations de mot de passe](identity-password-reset.md#identity-pw-writeback) de la phase d’identification pour obtenir des informations et des liens qui vous permettront de configurer l’écriture différée de mot de passe en production.</span><span class="sxs-lookup"><span data-stu-id="835f9-168">See the [Simplify password updates](identity-password-reset.md#identity-pw-writeback) step in the Identity phase for information and links to configure password writeback in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="835f9-169">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="835f9-169">Next step</span></span>

<span data-ttu-id="835f9-170">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="835f9-170">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="835f9-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="835f9-171">See also</span></span>

[<span data-ttu-id="835f9-172">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="835f9-172">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="835f9-173">Déployer Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="835f9-173">Deploy Microsoft 365 Enterprise</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="835f9-174">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="835f9-174">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)


