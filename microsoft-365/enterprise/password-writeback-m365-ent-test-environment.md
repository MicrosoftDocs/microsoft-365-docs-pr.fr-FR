---
title: Écriture différée de mot de passe pour votre environnement de test Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/22/2019
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
description: 'Résumé: Configurez l’écriture différée du mot de passe pour votre environnement de test Microsoft 365.'
ms.openlocfilehash: f1118c22ad1f65ea29bb14afacb7506a60d1fe1a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50921479"
---
# <a name="password-writeback-for-your-microsoft-365-test-environment"></a><span data-ttu-id="81ef7-103">Écriture différée de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81ef7-103">Password writeback for your Microsoft 365 test environment</span></span>

<span data-ttu-id="81ef7-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="81ef7-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="81ef7-105">Les utilisateurs peuvent utiliser l’écriture écriture par mot de passe pour mettre à jour leurs mots de passe via Azure Active Directory (Azure AD), qui est ensuite répliqué vers vos services de domaine Active Directory (AD DS) locaux.</span><span class="sxs-lookup"><span data-stu-id="81ef7-105">Users can use password writeback to update their passwords through Azure Active Directory (Azure AD), which is then replicated to your local Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="81ef7-106">Avec l’écriture écriture par mot de passe, les utilisateurs n’ont pas besoin de mettre à jour leur mot de passe via les AD DS sur site où leurs comptes d’utilisateur d’origine sont stockés.</span><span class="sxs-lookup"><span data-stu-id="81ef7-106">With password writeback, users don't have to update their passwords through the on-premises AD DS where their original user accounts are stored.</span></span> <span data-ttu-id="81ef7-107">Cela aide les utilisateurs itinérants ou distants qui n’ont pas de connexion d’accès à distance à leur réseau local.</span><span class="sxs-lookup"><span data-stu-id="81ef7-107">This helps roaming or remote users who don't have a remote access connection to their on-premises network.</span></span>

<span data-ttu-id="81ef7-108">Cet article explique comment configurer votre environnement de test Microsoft 365 pour l’écriture par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="81ef7-108">This article describes how to configure your Microsoft 365 test environment for password writeback.</span></span>

<span data-ttu-id="81ef7-109">La configuration de votre environnement de test pour l’écriture par mot de passe implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="81ef7-109">Configuring your test environment for password writeback involves two phases:</span></span>
- [<span data-ttu-id="81ef7-110">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81ef7-110">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>](#phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment)
- [<span data-ttu-id="81ef7-111">Phase 2 : Activer l’écriture différée de mot de passe pour le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="81ef7-111">Phase 2: Enable password writeback for the TESTLAB AD DS domain</span></span>](#phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain)
  
![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="81ef7-113">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="81ef7-113">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-configure-password-hash-synchronization-for-your-microsoft-365-test-environment"></a><span data-ttu-id="81ef7-114">Étape 1 : Configuration de la synchronisation de hachage de mot de passe pour votre environnement de test Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="81ef7-114">Phase 1: Configure password hash synchronization for your Microsoft 365 test environment</span></span>

<span data-ttu-id="81ef7-115">Tout d’abord, suivez les instructions de la synchronisation [de hachage de mot de passe.](password-hash-sync-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="81ef7-115">First, follow the instructions in [password hash synchronization](password-hash-sync-m365-ent-test-environment.md).</span></span> <span data-ttu-id="81ef7-116">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="81ef7-116">Your resulting configuration looks like this:</span></span>
  
![Environnement de test de l’entreprise simulée avec la synchronisation de hachage de mot de passe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)
  
<span data-ttu-id="81ef7-118">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="81ef7-118">This configuration consists of:</span></span>
  
- <span data-ttu-id="81ef7-119">Un abonnement d’évaluation ou payant Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="81ef7-119">A Microsoft 365 E5 trial or paid subscription.</span></span>
- <span data-ttu-id="81ef7-120">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="81ef7-120">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>
- <span data-ttu-id="81ef7-121">Azure AD Connect s’exécute sur APP1 pour synchroniser le domaine TESTLAB AD DS avec le client Azure AD de vos abonnements Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="81ef7-121">Azure AD Connect runs on APP1 to synchronize the TESTLAB AD DS domain to the Azure AD tenant of your Microsoft 365 subscription.</span></span>

## <a name="phase-2-enable-password-writeback-for-the-testlab-ad-ds-domain"></a><span data-ttu-id="81ef7-122">Phase 2 : Activer l’écriture différée de mot de passe pour le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="81ef7-122">Phase 2: Enable password writeback for the TESTLAB AD DS domain</span></span>

<span data-ttu-id="81ef7-123">Tout d’abord, configurez le compte utilisateur 1 avec le rôle d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="81ef7-123">First, configure the User 1 account with the global administrator role.</span></span>

1. <span data-ttu-id="81ef7-124">À partir du [Centre d’administration Microsoft 365](https://portal.microsoft.com), connectez-vous avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="81ef7-124">From the [Microsoft 365 admin center](https://portal.microsoft.com), sign in with your global administrator account.</span></span>

2. <span data-ttu-id="81ef7-125">Sélectionnez **Utilisateurs actifs.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-125">Select **Active users**.</span></span>
 
3. <span data-ttu-id="81ef7-126">Dans la page **Utilisateurs** actifs, sélectionnez le **compte utilisateur1,**</span><span class="sxs-lookup"><span data-stu-id="81ef7-126">On the **Active users** page, select the **user1** account,</span></span>

4. <span data-ttu-id="81ef7-127">Dans le **volet utilisateur 1,** **sélectionnez Modifier** à côté des **rôles.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-127">On the **user1** pane, select **Edit** next to **Roles**.</span></span>

5. <span data-ttu-id="81ef7-128">Dans le **volet Modifier les rôles d’utilisateur** pour user1, sélectionnez Administrateur **général,** **Sélectionnez Enregistrer,** puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-128">On the **Edit user roles** pane for user1, select **Global administrator**, select **Save**, and then select **Close**.</span></span>

<span data-ttu-id="81ef7-129">Configurez ensuite le compte utilisateur 1 en lui attribuant les paramètres de sécurité qui lui permettent de modifier le mot de passe pour le compte d’autres utilisateurs dans le domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="81ef7-129">Next, configure the User 1 account with the security settings that allow it to change passwords on behalf of other users in the TESTLAB AD DS domain.</span></span>

1. <span data-ttu-id="81ef7-130">À partir du[Portail Azure](https://portal.azure.com), connectez-vous avec votre compte d’administrateur général, puis connectez-vous à APP1 avec le compte TESTLAB\Utilisateur1.</span><span class="sxs-lookup"><span data-stu-id="81ef7-130">From the [Azure portal](https://portal.azure.com), sign in with your global administrator account, and then connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="81ef7-131">À partir du bureau d’APP1, **sélectionnez Démarrer,** entrez **actif,** puis sélectionnez Utilisateurs et **ordinateurs Active Directory.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-131">From the desktop of APP1, select **Start**, enter **active**, and then select **Active Directory Users and Computers**.</span></span>

3. <span data-ttu-id="81ef7-132">Dans la barre de menus, sélectionnez **Afficher.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-132">On the menu bar, select **View**.</span></span> <span data-ttu-id="81ef7-133">Si **les fonctionnalités** avancées ne sont pas activées, sélectionnez-la pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="81ef7-133">If **Advanced features** is not enabled, select it to enable it.</span></span>

4. <span data-ttu-id="81ef7-134">Dans le volet d’arborescence, sélectionnez et maintenez (ou cliquez avec le bouton droit) votre domaine, sélectionnez Propriétés, puis sélectionnez **l’onglet** Sécurité.</span><span class="sxs-lookup"><span data-stu-id="81ef7-134">In the tree pane, select and hold (or right-click) your domain, select **Properties**, and then select the **Security** tab.</span></span>

5. <span data-ttu-id="81ef7-135">Sélectionnez **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-135">Select **Advanced**.</span></span>

6. <span data-ttu-id="81ef7-136">Sous **l’onglet Autorisations,** sélectionnez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-136">On the **Permissions** tab, select **Add**.</span></span>

7. <span data-ttu-id="81ef7-137">Sélectionnez **un principal,** entrez **User1,** puis **sélectionnez OK.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-137">Select **Select a principal**, enter **User1**, and then select **OK**.</span></span>

8. <span data-ttu-id="81ef7-138">Dans **S’applique à**, sélectionnez **Objets utilisateur Descendant**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-138">In **Applies to**, select **Descendant User objects**.</span></span>

9. <span data-ttu-id="81ef7-139">Sous **Autorisations**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="81ef7-139">Under **Permissions**, select the following:</span></span>

    - <span data-ttu-id="81ef7-140">**Modifier le mot de passe**</span><span class="sxs-lookup"><span data-stu-id="81ef7-140">**Change password**</span></span>
    - <span data-ttu-id="81ef7-141">**Réinitialiser le mot de passe**</span><span class="sxs-lookup"><span data-stu-id="81ef7-141">**Reset password**</span></span>

10. <span data-ttu-id="81ef7-142">Sous **Propriétés**, sélectionnez les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="81ef7-142">Under **Properties**, select the following:</span></span>
    - <span data-ttu-id="81ef7-143">**Écrire lockoutTime**</span><span class="sxs-lookup"><span data-stu-id="81ef7-143">**Write lockoutTime**</span></span>
    - <span data-ttu-id="81ef7-144">**Écrire pwdLastSet**</span><span class="sxs-lookup"><span data-stu-id="81ef7-144">**Write pwdLastSet**</span></span>

11. <span data-ttu-id="81ef7-145">Sélectionnez **OK** trois fois pour enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="81ef7-145">Select **OK** three times to save the changes.</span></span>

12. <span data-ttu-id="81ef7-146">Fermer **Utilisateurs et Ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-146">Close **Active Directory Users and Computers**.</span></span>

<span data-ttu-id="81ef7-147">Ensuite, configurez de la Connexion Azure AD Connect sur APP1 pour écriture différée.</span><span class="sxs-lookup"><span data-stu-id="81ef7-147">Next, configure Azure AD Connect on APP1 for password writeback.</span></span>

1. <span data-ttu-id="81ef7-148">Si nécessaire, connectez-vous à APP1 avec le compte TESTLAB\User1.</span><span class="sxs-lookup"><span data-stu-id="81ef7-148">If needed, connect to APP1 with the TESTLAB\User1 account.</span></span>

2. <span data-ttu-id="81ef7-149">À partir du bureau d’APP1, double-cliquez sur **Azure AD Connect**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-149">From the desktop of APP1, double-click **Azure AD Connect**.</span></span>

3. <span data-ttu-id="81ef7-150">Dans la **page d’accueil,** **sélectionnez Configurer.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-150">On the **Welcome page**, select **Configure**.</span></span>

4. <span data-ttu-id="81ef7-151">Dans la page **Tâches supplémentaires,** sélectionnez **Personnaliser les options de** synchronisation, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-151">On the **Additional tasks** page, select **Customize synchronization options**, and then select **Next**.</span></span>

5. <span data-ttu-id="81ef7-152">Dans la page **Se connecter à Azure AD,** entrez vos informations d’identification de compte d’administrateur général, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-152">On the **Connect to Azure AD** page, enter your global administrator account credentials, and then select **Next**.</span></span>

6. <span data-ttu-id="81ef7-153">Dans les **pages De connexion des répertoires** et de filtrage **domaine/ou,** sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-153">On the **Connect directories** and **Domain/OU filtering** pages, select **Next**.</span></span>

7. <span data-ttu-id="81ef7-154">Dans la page **Fonctionnalités facultatives,** sélectionnez **Écriture écriture par** mot de passe, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="81ef7-154">On the **Optional features** page, select **Password writeback**, and then select **Next**.</span></span>

8. <span data-ttu-id="81ef7-155">Dans la page **Prêt à configurer,** sélectionnez **Configurer** et attendez la fin du processus.</span><span class="sxs-lookup"><span data-stu-id="81ef7-155">On the **Ready to configure** page, select **Configure** and wait for the process to finish.</span></span>

9. <span data-ttu-id="81ef7-156">Lorsque vous voyez la configuration se terminer, sélectionnez **Quitter.**</span><span class="sxs-lookup"><span data-stu-id="81ef7-156">When you see the configuration finish, select **Exit**.</span></span>

<span data-ttu-id="81ef7-157">Vous êtes maintenant prêt à tester l’écriture écriture par mot de passe pour les utilisateurs sur des ordinateurs qui ne sont pas connectés au réseau virtuel de votre intranet simulé.</span><span class="sxs-lookup"><span data-stu-id="81ef7-157">You are now ready to test password writeback for users on computers that aren't connected to the virtual network of your simulated intranet.</span></span>

<span data-ttu-id="81ef7-158">La configuration qui en résulte ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="81ef7-158">Your resulting configuration looks like this:</span></span>

![Environnement de test de l’entreprise simulée avec l’authentification directe](../media/pass-through-auth-m365-ent-test-environment/Phase1.png)

<span data-ttu-id="81ef7-160">Cette configuration se compose des éléments suivants : </span><span class="sxs-lookup"><span data-stu-id="81ef7-160">This configuration consists of:</span></span>

- <span data-ttu-id="81ef7-161">Un abonnement d’essai ou payant Microsoft 365 E5 avec le domaine DNS TESTLAB.\<*your domain name*></span><span class="sxs-lookup"><span data-stu-id="81ef7-161">A Microsoft 365 E5 trial or paid subscriptions with the DNS domain TESTLAB.\<*your domain name*></span></span> <span data-ttu-id="81ef7-162">Inscrit(e).</span><span class="sxs-lookup"><span data-stu-id="81ef7-162">registered.</span></span>
- <span data-ttu-id="81ef7-163">Un intranet d’organisation simplifié connecté à Internet, constitué des machines virtuelles DC1, APP1 et CLIENT1 sur un sous-réseau d’un réseau virtuel Azure.</span><span class="sxs-lookup"><span data-stu-id="81ef7-163">A simplified organization intranet connected to the internet, consisting of the DC1, APP1, and CLIENT1 virtual machines on a subnet of an Azure virtual network.</span></span>
- <span data-ttu-id="81ef7-164">Azure AD Connect s’exécute sur APP1 pour synchroniser la liste des comptes et des groupes du client Azure AD de votre abonnement Microsoft 365 au domaine TESTLAB AD DS.</span><span class="sxs-lookup"><span data-stu-id="81ef7-164">Azure AD Connect runs on APP1 to synchronize the list of accounts and groups from the Azure AD tenant of your Microsoft 365 subscription to the TESTLAB AD DS domain.</span></span>
- <span data-ttu-id="81ef7-165">L’écriture différée de mot de passe est activée afin que les utilisateurs puissent modifier leur mot de passe via Azure AD sans avoir à se connecter à l’intranet simplifiée.</span><span class="sxs-lookup"><span data-stu-id="81ef7-165">Password writeback is enabled so that users can change their passwords through Azure AD without having to be connected to the simplified intranet.</span></span>

## <a name="next-step"></a><span data-ttu-id="81ef7-166">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="81ef7-166">Next step</span></span>

<span data-ttu-id="81ef7-167">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="81ef7-167">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="81ef7-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81ef7-168">See also</span></span>

[<span data-ttu-id="81ef7-169">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="81ef7-169">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="81ef7-170">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="81ef7-170">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="81ef7-171">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="81ef7-171">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)