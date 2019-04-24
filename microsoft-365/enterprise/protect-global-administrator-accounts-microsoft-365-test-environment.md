---
title: Protéger les comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/16/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Suivez ces étapes pour protéger les comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: cded424188447f96e5614f31d3e207bb541d438e
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290857"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="67418-103">Protéger les comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="67418-103">Protect global administrator accounts in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="67418-104">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que les comptes administrateurs sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="67418-104">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="67418-105">Cet article explique comment utiliser la sécurité des applications Cloud Office 365 et les stratégies d'accès conditionnel Azure AD pour protéger les comptes d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="67418-105">This article describes how to use Office 365 Cloud App Security and Azure AD conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="67418-106">Il existe deux phases pour la protection des comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise:</span><span class="sxs-lookup"><span data-stu-id="67418-106">There are two phases to protecting global administrator accounts in your Microsoft 365 Enterprise test environment:</span></span>

1.  <span data-ttu-id="67418-107">Créez l'environnement de test Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="67418-107">Create the Microsoft 365 Enterprise test environment.</span></span>
2.  <span data-ttu-id="67418-108">Protégez votre compte d'administrateur général dédié.</span><span class="sxs-lookup"><span data-stu-id="67418-108">Protect your dedicated global administrator account.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="67418-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="67418-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

> [!NOTE]
> <span data-ttu-id="67418-111">L'environnement de test Microsoft 365 entreprise utilise les versions E5 d'Office 365 et Enterprise Management + Security (EMS).</span><span class="sxs-lookup"><span data-stu-id="67418-111">The Microsoft 365 Enterprise test environment uses E5 versions of Office 365 and Enterprise Management + Security (EMS).</span></span> <span data-ttu-id="67418-112">La fonctionnalité de sécurité des applications Cloud Office 365 est uniquement disponible dans la version E5 Office 365.</span><span class="sxs-lookup"><span data-stu-id="67418-112">The Office 365 Cloud App Security feature is only available in the E5 version Office 365.</span></span> 

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="67418-113">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="67418-113">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="67418-114">Si vous souhaitez simplement tester la protection de compte d'administrateur général de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="67418-114">If you just want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="67418-115">Si vous souhaitez tester la protection des comptes d'administrateur général dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="67418-115">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>

  
> [!NOTE]
> <span data-ttu-id="67418-116">Le test de la protection de compte d'administrateur général ne nécessite pas l'environnement de test d'entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d'annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="67418-116">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="67418-117">Elle est fournie ici en tant qu'option pour vous permettre de tester la protection des comptes d'administrateur général et de l'expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="67418-117">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-cloud-app-security-and-conditional-access-policies"></a><span data-ttu-id="67418-118">Phase 2: configurer la sécurité des applications Cloud et les stratégies d'accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="67418-118">Phase 2: Configure Cloud App Security and conditional access policies</span></span>

<span data-ttu-id="67418-119">Tout d'abord, créez une stratégie de sécurité d'application Cloud Office 365 pour surveiller l'activité de compte d'administrateur général et envoyer des alertes à l'adresse de messagerie de votre compte d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="67418-119">First, create an Office 365 Cloud App Security policy to monitor global administrator account activity and send alerts to the email address of your global administrator account.</span></span> 

1. <span data-ttu-id="67418-120">Connectez-vous au [portail de conformité d'Office 365 Security &](https://protection.office.com/) à l'aide de votre compte d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="67418-120">Sign in to the [Office 365 Security & Compliance portal](https://protection.office.com/) using your global administrator account.</span></span>
2. <span data-ttu-id="67418-121">Dans le volet de navigation de gauche, cliquez sur **Alertes > Gérer les alertes avancées**.</span><span class="sxs-lookup"><span data-stu-id="67418-121">In the left navigation pane, click **Alerts > Manage advanced alerts**.</span></span>
3. <span data-ttu-id="67418-122">Sur la page **Gérer les alertes avancées**, cliquez sur **Activer Sécurité des applications cloud Office 365**, puis sur **Atteindre Sécurité des applications cloud Office 365**.</span><span class="sxs-lookup"><span data-stu-id="67418-122">On the **Manage advanced alerts** page, click **Turn on Office 365 Cloud App Security**, and then click **Go to Office 365 Cloud App Security**.</span></span>
4. <span data-ttu-id="67418-123">Sur le nouvel onglet **Tableau de bord**, cliquez sur **Contrôle > Stratégies**.</span><span class="sxs-lookup"><span data-stu-id="67418-123">On the new **Dashboard** tab, click **Control > Policies**.</span></span>
5. <span data-ttu-id="67418-124">Sur la page **Stratégies**, cliquez sur **Créer une stratégie**, puis sur **Stratégie d’activité**.</span><span class="sxs-lookup"><span data-stu-id="67418-124">On the **Policy** page, click **Create policy**, and then click **Activity policy**.</span></span>
6. <span data-ttu-id="67418-125">Dans **Nom de la stratégie**, saisissez **Activité administrative**.</span><span class="sxs-lookup"><span data-stu-id="67418-125">In **Policy name**, type **Administrative activity**.</span></span>
7. <span data-ttu-id="67418-126">Dans **Gravité de la stratégie**, cliquez sur **Élevée**.</span><span class="sxs-lookup"><span data-stu-id="67418-126">In **Policy severity**, click **High**.</span></span>
8. <span data-ttu-id="67418-127">Dans **Catégorie**, cliquez sur **Comptes privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="67418-127">In **Category**, click **Privileged accounts**.</span></span>
9. <span data-ttu-id="67418-128">Dans **Créer des filtres pour la stratégie**, dans **Activités correspondant à tous les critères suivants**, cliquez sur **Activité administrative**.</span><span class="sxs-lookup"><span data-stu-id="67418-128">In **Create filters for the policy**, in **Activities matching all of the following**, click **Administrative activity**.</span></span>
10. <span data-ttu-id="67418-p104">Dans **Alertes**, cliquez sur **Envoyer une alerte par e-mail**. Dans **À**, entrez l’adresse de messagerie de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="67418-p104">In **Alerts**, click **Send alert as email**. In **To**, type the email address of your global administrator account.</span></span>
11. <span data-ttu-id="67418-131">Au bas de la page, cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="67418-131">At the bottom of the page, click **Create**.</span></span>
12. <span data-ttu-id="67418-132">Fermez l'onglet **tableau de bord** .</span><span class="sxs-lookup"><span data-stu-id="67418-132">Close the **Dashboard** tab.</span></span>
    
<span data-ttu-id="67418-133">Ensuite, créez un compte d'utilisateur en tant qu'administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="67418-133">Next, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="67418-134">Sous un onglet séparé, ouvrez le [Centre d'administration Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="67418-134">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="67418-135">Sous **utilisateurs actifs**, cliquez sur **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="67418-135">Under **Active users**, click **Add a user**.</span></span>
3. <span data-ttu-id="67418-136">Sur la page **nouvel utilisateur** , tapez **DedicatedAdmin** dans **prénom**, **nom d'affichage**et nom **d'utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="67418-136">On the **New user** page, type **DedicatedAdmin** in **First name**, **Display name**, and **Username**.</span></span>
4. <span data-ttu-id="67418-137">Cliquez sur **mot de passe**, sur **me laisser créer le mot de**passe, puis tapez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="67418-137">Click **Password**, click **Let me create the password**, and then type a strong password.</span></span> <span data-ttu-id="67418-138">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="67418-138">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="67418-139">DéCochez **faire en sorte que cet utilisateur modifie son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="67418-139">Clear **Make this user change their password when they first sign in**.</span></span>
6. <span data-ttu-id="67418-140">Cliquez sur **rôles**, puis sur **administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="67418-140">Click **Roles**, and then click **Global administrator**.</span></span>
7. <span data-ttu-id="67418-141">Cliquez sur **licences de produit**, puis activez les licences **Enterprise Mobility + Security e5** et **Office 365 entreprise E5** sur.</span><span class="sxs-lookup"><span data-stu-id="67418-141">Click **Product licenses**, and then turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5 licenses** on.</span></span>
8. <span data-ttu-id="67418-142">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="67418-142">Click **Add**.</span></span>
9. <span data-ttu-id="67418-143">Dans la **page l'utilisateur a été ajouté**, effacez le **mot de passe Envoyer un message électronique**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="67418-143">On the **User was added page**, clear **Send password in email**, and then click **Close**.</span></span>

<span data-ttu-id="67418-144">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="67418-144">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="67418-145">Dans l'onglet **Centre d'administration Microsoft 365** , cliquez sur l'icône groupes dans le volet de navigation de gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="67418-145">On the **Microsoft 365 admin center** tab, click the groups icon in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="67418-146">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="67418-146">Click **Add a group**.</span></span>
3. <span data-ttu-id="67418-147">Sur la page **nouveau groupe** , tapez **GlobalAdmins**.</span><span class="sxs-lookup"><span data-stu-id="67418-147">On the **New Group** page, type **GlobalAdmins**.</span></span>
4. <span data-ttu-id="67418-148">Cliquez sur **Sélectionner le propriétaire** , cliquez sur votre compte d'administrateur général, puis cliquez sur **Ajouter > fermer**.</span><span class="sxs-lookup"><span data-stu-id="67418-148">Click **Select owner** click your global administrator account, and then click **Add > Close**.</span></span>
5. <span data-ttu-id="67418-149">Dans la liste des groupes, cliquez sur le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="67418-149">In the list of groups, click the **GlobalAdmins** group.</span></span>
6. <span data-ttu-id="67418-150">Sur la page **GlobalAdmins** , cliquez sur modifier le membre, puis sur **Ajouter** **des**membres.</span><span class="sxs-lookup"><span data-stu-id="67418-150">On the **GlobalAdmins** page, click **Edit for Member**, and then click **Add members**.</span></span>
7. <span data-ttu-id="67418-151">Dans la liste, cliquez sur le compte **DedicatedAdmin** , puis cliquez sur **Enregistrer _GT_ fermer > fermer _GT_ Centre d'administration**.</span><span class="sxs-lookup"><span data-stu-id="67418-151">In the list, click the **DedicatedAdmin** account, and then click **Save > Close > Close > Admin center**.</span></span>

<span data-ttu-id="67418-152">Ensuite, créez des stratégies d'accès conditionnel pour exiger l'authentification multifacteur pour les comptes d'administrateur général et pour refuser l'authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="67418-152">Next, create conditional access policies to require multifactor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="67418-153">Cette première stratégie nécessite que tous les comptes d'administrateur général utilisent l'authentification multiFACTEUR.</span><span class="sxs-lookup"><span data-stu-id="67418-153">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="67418-154">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="67418-154">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="67418-155">Cliquez sur **Azure Active Directory > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="67418-155">Click **Azure Active Directory > Conditional access**.</span></span>
3. <span data-ttu-id="67418-156">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **stratégie de base: exiger MFA pour les administrateurs (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="67418-156">On the **Conditional access – Policies** blade, click **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="67418-157">Sur les **stratégies de base...**</span><span class="sxs-lookup"><span data-stu-id="67418-157">On the **Baseline policies…**</span></span> <span data-ttu-id="67418-158">, cliquez sur **utiliser la stratégie immédiatement _GT_ enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="67418-158">blade, click **Use policy immediately > Save**.</span></span>

<span data-ttu-id="67418-159">Cette deuxième stratégie bloque l'accès à l'authentification de compte d'administrateur général lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="67418-159">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="67418-160">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="67418-160">On the **Conditional access – Policies** blade, click **New policy**.</span></span>
2. <span data-ttu-id="67418-161">Sur la **nouvelle** Blade, tapez **administrateurs globaux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="67418-161">On the **New** blade, type **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="67418-162">Dans la \*\*\*\* section affectations, cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="67418-162">In the **Assignments** section, click **Users and groups**.</span></span>
4. <span data-ttu-id="67418-163">Sous l'onglet **inclure** du panneau **utilisateurs et groupes** , cliquez sur Sélectionner des utilisateurs et des groupes **> les utilisateurs et les groupes > sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="67418-163">On the **Include** tab of the **Users and groups** blade, click **Select users and groups > Users and groups > Select**.</span></span>
5. <span data-ttu-id="67418-164">Sur la Blade de **sélection** , cliquez sur le **GlobalAdmins > sélectionnez >**.</span><span class="sxs-lookup"><span data-stu-id="67418-164">On the **Select** blade, click the **GlobalAdmins > Select > Done**.</span></span>
6. <span data-ttu-id="67418-165">Dans la \*\*\*\* section affectations, cliquez sur **conditions**.</span><span class="sxs-lookup"><span data-stu-id="67418-165">In the **Assignments** section, click **Conditions**.</span></span>
7. <span data-ttu-id="67418-166">Dans le volet **conditions** , cliquez sur **risque de connexion**, cliquez sur **Oui** pour **configurer**, **sur haute** et **moyenne**, puis sur **sélection** et **fin**.</span><span class="sxs-lookup"><span data-stu-id="67418-166">On the **Conditions** blade, click **Sign-in risk**, click **Yes** for **Configure**, click **High** and **Medium**, and then click **Select** and **Done**.</span></span>
8. <span data-ttu-id="67418-167">Dans la section **contrôles d'accès** de la **nouvelle** Blade, cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="67418-167">In the **Access controls** section of the **New** blade, click **Grant**.</span></span>
9. <span data-ttu-id="67418-168">Dans le panneau **accorder** , cliquez sur **bloquer l'accès**, puis sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="67418-168">On the **Grant** blade, click **Block access**, and then click **Select**.</span></span>
10. <span data-ttu-id="67418-169">Sur la **nouvelle** Blade, cliquez \*\*\*\* sur **activer pour activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="67418-169">On the **New** blade, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="67418-170">Fermez les onglets **portail Azure** et **Centre d'administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="67418-170">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="67418-171">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="67418-171">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="67418-172">Vous devez être invité à configurer l'authentification multiFACTEUR sur le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67418-172">You should be prompted to configure MFA on the user account.</span></span> <span data-ttu-id="67418-173">Cela démontre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="67418-173">This demonstrates that the first policy is being applied.</span></span>

<span data-ttu-id="67418-174">Consultez l'étape [protéger les comptes administrateur général](identity-designate-protect-admin-accounts.md#identity-global-admin) dans la phase d'identité pour obtenir des informations et des liens afin de protéger vos comptes d'administrateur général en production.</span><span class="sxs-lookup"><span data-stu-id="67418-174">See the [Protect global administrator accounts](identity-designate-protect-admin-accounts.md#identity-global-admin) step in the Identity phase for information and links to protect your global administrator accounts in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="67418-175">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="67418-175">Next step</span></span>

<span data-ttu-id="67418-176">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="67418-176">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="67418-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67418-177">See also</span></span>

[<span data-ttu-id="67418-178">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="67418-178">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="67418-179">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="67418-179">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="67418-180">Déploiement d'entreprise Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="67418-180">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="67418-181">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="67418-181">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
