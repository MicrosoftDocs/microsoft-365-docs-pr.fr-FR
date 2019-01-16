---
title: Protéger les comptes d’administrateur global dans votre environnement de test Microsoft 365 pour entreprises
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
description: Suivez ces étapes pour protéger les comptes d’administrateur global dans votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 4d444e217c5a232811701f6519c2eb3ebe86df70
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866862"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="08ce0-103">Protéger les comptes d’administrateur global dans votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="08ce0-103">Protect global administrator accounts in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="08ce0-p101">Vous pouvez empêcher les attaques numériques dans votre organisation en s’assurant que vos comptes d’administrateur sont aussi sécurisés que possible. Cet article décrit comment utiliser les stratégies d’accès conditionnel de sécurité pour application Cloud Microsoft Office 365 et Azure AD pour protéger les comptes d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p101">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible. This article describes how to use Office 365 Cloud App Security and Azure AD conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="08ce0-106">Il existe deux phases à protéger les comptes d’administrateur global dans votre environnement de test Microsoft 365 pour entreprises :</span><span class="sxs-lookup"><span data-stu-id="08ce0-106">There are two phases to protecting global administrator accounts in your Microsoft 365 Enterprise test environment:</span></span>

1.  <span data-ttu-id="08ce0-107">Créer l’environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="08ce0-107">Create the Microsoft 365 Enterprise test environment.</span></span>
2.  <span data-ttu-id="08ce0-108">Protéger votre compte d’administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="08ce0-108">Protect your dedicated global administrator account.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="08ce0-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="08ce0-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="08ce0-111">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="08ce0-111">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="08ce0-112">Si vous souhaitez uniquement tester la protection des comptes d’administrateur global d’une manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="08ce0-112">If you just want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="08ce0-113">Si vous souhaitez tester la protection des comptes d’administrateur global dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="08ce0-113">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="08ce0-p102">Test du compte d’administrateur global de protection ne nécessite pas de l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option de sorte que vous pouvez tester la protection des comptes d’administrateur global et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p102">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-cloud-app-security-and-conditional-access-policies"></a><span data-ttu-id="08ce0-116">Phase 2 : Configurer la sécurité d’application Cloud et stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="08ce0-116">Phase 2: Configure Cloud App Security and conditional access policies</span></span>

<span data-ttu-id="08ce0-117">Tout d’abord, créez une stratégie de sécurité d’application Office 365 dans le nuage pour surveiller l’activité de compte d’administrateur global et envoyer des alertes à l’adresse de messagerie de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="08ce0-117">First, create an Office 365 Cloud App Security policy to monitor global administrator account activity and send alerts to the email address of your global administrator account.</span></span> 

1. <span data-ttu-id="08ce0-118">Connectez-vous au portail Office au [http://portal.office.com](http://portal.office.com) à l’aide de votre compte d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="08ce0-118">Sign in to the Office portal at [http://portal.office.com](http://portal.office.com) using your global administrator account.</span></span>
2. <span data-ttu-id="08ce0-p103">Cliquez sur la vignette de **l’administrateur** . Dans l’onglet **Centre d’administration d’Office** , cliquez sur **centres d’administration > sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p103">Click the **Admin** tile. On the **Office Admin center** tab, click **Admin centers > Security & Compliance**.</span></span>
3. <span data-ttu-id="08ce0-121">Dans le volet de navigation de gauche, cliquez sur **Alertes > Gérer les alertes avancées**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-121">In the left navigation pane, click **Alerts > Manage advanced alerts**.</span></span>
4. <span data-ttu-id="08ce0-122">Sur la page **Gérer les alertes avancées**, cliquez sur **Activer Sécurité des applications cloud Office 365**, puis sur **Atteindre Sécurité des applications cloud Office 365**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-122">On the **Manage advanced alerts** page, click **Turn on Office 365 Cloud App Security**, and then click **Go to Office 365 Cloud App Security**.</span></span>
5. <span data-ttu-id="08ce0-123">Sur le nouvel onglet **Tableau de bord**, cliquez sur **Contrôle > Stratégies**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-123">On the new **Dashboard** tab, click **Control > Policies**.</span></span>
6. <span data-ttu-id="08ce0-124">Sur la page **Stratégies**, cliquez sur **Créer une stratégie**, puis sur **Stratégie d’activité**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-124">On the **Policy** page, click **Create policy**, and then click **Activity policy**.</span></span>
7. <span data-ttu-id="08ce0-125">Dans **Nom de la stratégie**, saisissez **Activité administrative**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-125">In **Policy name**, type **Administrative activity**.</span></span>
8. <span data-ttu-id="08ce0-126">Dans **Gravité de la stratégie**, cliquez sur **Élevée**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-126">In **Policy severity**, click **High**.</span></span>
9. <span data-ttu-id="08ce0-127">Dans **Catégorie**, cliquez sur **Comptes privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-127">In **Category**, click **Privileged accounts**.</span></span>
10. <span data-ttu-id="08ce0-128">Dans **Créer des filtres pour la stratégie**, dans **Activités correspondant à tous les critères suivants**, cliquez sur **Activité administrative**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-128">In **Create filters for the policy**, in **Activities matching all of the following**, click **Administrative activity**.</span></span>
11. <span data-ttu-id="08ce0-p104">Dans **Alertes**, cliquez sur **Envoyer une alerte par e-mail**. Dans **À**, entrez l’adresse de messagerie de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p104">In **Alerts**, click **Send alert as email**. In **To**, type the email address of your global administrator account.</span></span>
12. <span data-ttu-id="08ce0-131">Au bas de la page, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-131">At the bottom of the page, click **Create**.</span></span>
13. <span data-ttu-id="08ce0-132">Fermez l’onglet **tableau de bord** .</span><span class="sxs-lookup"><span data-stu-id="08ce0-132">Close the **Dashboard** tab.</span></span>
    
<span data-ttu-id="08ce0-133">Ensuite, créez un nouveau compte d’utilisateur en tant qu’administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="08ce0-133">Next, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="08ce0-134">Sous l’onglet **Centre d’administration d’Office** , sous **utilisateurs actifs**, cliquez sur **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-134">On the **Office Admin center** tab, under **Active users**, click **Add a user**.</span></span>
2. <span data-ttu-id="08ce0-135">Dans la page **nouvel utilisateur** , tapez **DedicatedAdmin** dans **prénom**, **nom complet**et **nom d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-135">On the **New user** page, type **DedicatedAdmin** in **First name**, **Display name**, and **Username**.</span></span>
3. <span data-ttu-id="08ce0-p105">Cliquez sur **le mot de passe**et cliquez sur **me laisser créer le mot de passe**, puis tapez un mot de passe. Enregistrez le mot de passe pour ce compte dans un endroit sûr.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p105">Click **Password**, click **Let me create the password**, and then type a strong password. Record the password for this new account in a secure location.</span></span>
4. <span data-ttu-id="08ce0-138">Désactivez **rendre cet utilisateur de modifier leur mot de passe lorsqu’ils se connectent tout d’abord**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-138">Clear **Make this user change their password when they first sign in**.</span></span>
5. <span data-ttu-id="08ce0-139">Cliquez sur **rôles**, puis cliquez sur **administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-139">Click **Roles**, and then click **Global administrator**.</span></span>
6. <span data-ttu-id="08ce0-140">Cliquez sur **les licences de produit**, puis activer la **mobilité d’entreprise + E5 de sécurité** et des **licences Office 365 entreprise E5** .</span><span class="sxs-lookup"><span data-stu-id="08ce0-140">Click **Product licenses**, and then turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5 licenses** on.</span></span>
7. <span data-ttu-id="08ce0-141">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-141">Click **Add**.</span></span>
8. <span data-ttu-id="08ce0-142">Sur l' **utilisateur a été ajouté page**, désactivez **Envoyer le mot de passe dans le message électronique**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-142">On the **User was added page**, clear **Send password in email**, and then click **Close**.</span></span>

<span data-ttu-id="08ce0-143">Ensuite, créez un nouveau groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="08ce0-143">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="08ce0-144">Sous l’onglet **Centre d’administration d’Office** , cliquez sur l’icône de groupes dans le volet de navigation gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-144">On the **Office Admin center** tab, click the groups icon in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="08ce0-145">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-145">Click **Add a group**.</span></span>
3. <span data-ttu-id="08ce0-146">Dans la page **Nouveau groupe** , tapez **GlobalAdmins**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-146">On the **New Group** page, type **GlobalAdmins**.</span></span>
4. <span data-ttu-id="08ce0-147">Cliquez sur cliquez sur **Sélectionnez propriétaire** de votre compte d’administrateur global, puis cliquez sur **Ajouter > Fermer**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-147">Click **Select owner** click your global administrator account, and then click **Add > Close**.</span></span>
5. <span data-ttu-id="08ce0-148">Dans la liste des groupes, cliquez sur le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="08ce0-148">In the list of groups, click the **GlobalAdmins** group.</span></span>
6. <span data-ttu-id="08ce0-149">Dans la page **GlobalAdmins** , cliquez sur **Modifier pour le membre**, puis cliquez sur **Ajouter des membres**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-149">On the **GlobalAdmins** page, click **Edit for Member**, and then click **Add members**.</span></span>
7. <span data-ttu-id="08ce0-150">Dans la liste, cliquez sur le compte **DedicatedAdmin** , puis cliquez sur **Enregistrer > Fermer > Fermer > Centre d’administration**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-150">In the list, click the **DedicatedAdmin** account, and then click **Save > Close > Close > Admin center**.</span></span>

<span data-ttu-id="08ce0-151">Ensuite, créez des stratégies d’accès conditionnel d’exiger l’authentification multifacteur pour les comptes d’administrateur global et refuser l’authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="08ce0-151">Next, create conditional access policies to require multifactor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="08ce0-152">Cette stratégie premier requiert que tous les comptes d’administrateur global utilisent MFA.</span><span class="sxs-lookup"><span data-stu-id="08ce0-152">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="08ce0-153">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="08ce0-153">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="08ce0-154">Cliquez sur **Azure Active Directory > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-154">Click **Azure Active Directory > Conditional access**.</span></span>
3. <span data-ttu-id="08ce0-155">Sur le serveur lame **accès conditionnel – stratégies** , cliquez sur **stratégie de base : nécessitent un MFA pour les administrateurs (preview)**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-155">On the **Conditional access – Policies** blade, click **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="08ce0-p106">Sur le serveur lame **... les stratégies de base** , cliquez sur **utiliser immédiatement la stratégie > Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p106">On the **Baseline policies…** blade, click **Use policy immediately > Save**.</span></span>

<span data-ttu-id="08ce0-158">Ce deuxième stratégie bloque l’accès à l’authentification de compte administrateur global lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="08ce0-158">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="08ce0-159">Sur le serveur lame **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-159">On the **Conditional access – Policies** blade, click **New policy**.</span></span>
2. <span data-ttu-id="08ce0-160">Sur le serveur lame **New** , tapez **administrateurs globaux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-160">On the **New** blade, type **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="08ce0-161">Dans la section des **affectations** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-161">In the **Assignments** section, click **Users and groups**.</span></span>
4. <span data-ttu-id="08ce0-162">Sous l’onglet **inclure** de la lame **utilisateurs et groupes** , cliquez sur **Sélectionnez Utilisateurs et groupes > utilisateurs et groupes > sélectionnez**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-162">On the **Include** tab of the **Users and groups** blade, click **Select users and groups > Users and groups > Select**.</span></span>
5. <span data-ttu-id="08ce0-163">Sur le serveur lame **Sélectionnez** , cliquez sur le **GlobalAdmins > sélectionnez > fait**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-163">On the **Select** blade, click the **GlobalAdmins > Select > Done**.</span></span>
6. <span data-ttu-id="08ce0-164">Dans la section des **affectations** , cliquez sur **Conditions**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-164">In the **Assignments** section, click **Conditions**.</span></span>
7. <span data-ttu-id="08ce0-165">Sur le serveur lame **Conditions** , cliquez sur **connexion risque**, cliquez sur **Oui** pour **configurer**, cliquez sur **élevé** et **moyen**, puis cliquez sur **Sélectionnez** et **fait**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-165">On the **Conditions** blade, click **Sign-in risk**, click **Yes** for **Configure**, click **High** and **Medium**, and then click **Select** and **Done**.</span></span>
8. <span data-ttu-id="08ce0-166">Dans la section **contrôle d’accès** de la lame de **Nouveau** , cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-166">In the **Access controls** section of the **New** blade, click **Grant**.</span></span>
9. <span data-ttu-id="08ce0-167">Sur le serveur lame **Grant** , cliquez sur **Bloquer l’accès**, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-167">On the **Grant** blade, click **Block access**, and then click **Select**.</span></span>
10. <span data-ttu-id="08ce0-168">Sur le serveur lame **Nouveau** , cliquez **sur** pour **Activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="08ce0-168">On the **New** blade, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="08ce0-169">Fermez les onglets **Azure portal** et le **Centre d’administration d’Office** .</span><span class="sxs-lookup"><span data-stu-id="08ce0-169">Close the **Azure portal** and **Office Admin center** tabs.</span></span>

<span data-ttu-id="08ce0-p107">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous à l’aide du compte DedicatedAdmin. Vous devez être invités à configurer MFA sur le compte d’utilisateur. Cela indique que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="08ce0-p107">To test the first policy, sign out and sign in with the DedicatedAdmin account. You should be prompted to configure MFA on the user account. This demonstrates that the first policy is being applied.</span></span>

<span data-ttu-id="08ce0-173">Voir l’étape de [comptes d’administrateur global Protect](identity-designate-protect-admin-accounts.md) lors de la phase d’identité pour des informations et des liens pour protéger vos comptes d’administrateur global en production.</span><span class="sxs-lookup"><span data-stu-id="08ce0-173">See the [Protect global administrator accounts](identity-designate-protect-admin-accounts.md) step in the Identity phase for information and links to protect your global administrator accounts in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="08ce0-174">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="08ce0-174">Next step</span></span>

<span data-ttu-id="08ce0-175">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="08ce0-175">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="08ce0-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08ce0-176">See also</span></span>

[<span data-ttu-id="08ce0-177">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="08ce0-177">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="08ce0-178">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="08ce0-178">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="08ce0-179">Déploiement de Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="08ce0-179">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="08ce0-180">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="08ce0-180">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
