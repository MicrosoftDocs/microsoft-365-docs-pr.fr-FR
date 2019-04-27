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
ms.openlocfilehash: 86b2d325fc710fd8b387bc37cad5f8ea60df001d
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33353056"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ac844-103">Protéger les comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ac844-103">Protect global administrator accounts in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ac844-104">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que les comptes administrateurs sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="ac844-104">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="ac844-105">Cet article explique comment utiliser les stratégies d'accès conditionnel Azure Active Directory (Azure AD) pour protéger les comptes d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ac844-105">This article describes how to use Azure Active Directory (Azure AD) conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="ac844-106">Il existe deux phases pour la protection des comptes d'administrateur général dans votre environnement de test Microsoft 365 Enterprise:</span><span class="sxs-lookup"><span data-stu-id="ac844-106">There are two phases to protecting global administrator accounts in your Microsoft 365 Enterprise test environment:</span></span>

1.  <span data-ttu-id="ac844-107">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ac844-107">Create the Microsoft 365 Enterprise test environment.</span></span>
2.  <span data-ttu-id="ac844-108">Protégez votre compte d'administrateur général dédié.</span><span class="sxs-lookup"><span data-stu-id="ac844-108">Protect your dedicated global administrator account.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="ac844-110">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ac844-110">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ac844-111">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ac844-111">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ac844-112">Si vous souhaitez simplement tester la protection de compte d'administrateur général de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="ac844-112">If you just want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="ac844-113">Si vous souhaitez tester la protection des comptes d'administrateur général dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ac844-113">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>

  
> [!NOTE]
> <span data-ttu-id="ac844-114">Le test de la protection de compte d'administrateur général ne nécessite pas l'environnement de test d'entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d'annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ac844-114">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="ac844-115">Elle est fournie ici en tant qu'option pour vous permettre de tester la protection des comptes d'administrateur général et de l'expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="ac844-115">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-conditional-access-policies"></a><span data-ttu-id="ac844-116">Phase 2: configurer les stratégies d'accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="ac844-116">Phase 2: Configure conditional access policies</span></span>

<span data-ttu-id="ac844-117">Tout d'abord, créez un compte d'utilisateur en tant qu'administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="ac844-117">First, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="ac844-118">Sous un onglet séparé, ouvrez le [Centre d'administration Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ac844-118">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="ac844-119">Sous **utilisateurs actifs**, cliquez sur **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ac844-119">Under **Active users**, click **Add a user**.</span></span>
3. <span data-ttu-id="ac844-120">Sur la page **nouvel utilisateur** , tapez **DedicatedAdmin** dans **prénom**, **nom d'affichage**et nom **d'utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ac844-120">On the **New user** page, type **DedicatedAdmin** in **First name**, **Display name**, and **Username**.</span></span>
4. <span data-ttu-id="ac844-121">Cliquez sur **mot de passe**, sur **me laisser créer le mot de**passe, puis tapez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="ac844-121">Click **Password**, click **Let me create the password**, and then type a strong password.</span></span> <span data-ttu-id="ac844-122">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ac844-122">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="ac844-123">DéCochez **faire en sorte que cet utilisateur modifie son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="ac844-123">Clear **Make this user change their password when they first sign in**.</span></span>
6. <span data-ttu-id="ac844-124">Cliquez sur **rôles**, puis sur **administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="ac844-124">Click **Roles**, and then click **Global administrator**.</span></span>
7. <span data-ttu-id="ac844-125">Cliquez sur **licences de produit**, puis activez les licences **Enterprise Mobility + Security e5** et **Office 365 entreprise E5** sur.</span><span class="sxs-lookup"><span data-stu-id="ac844-125">Click **Product licenses**, and then turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5 licenses** on.</span></span>
8. <span data-ttu-id="ac844-126">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ac844-126">Click **Add**.</span></span>
9. <span data-ttu-id="ac844-127">Dans la **page l'utilisateur a été ajouté**, effacez le **mot de passe Envoyer un message électronique**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ac844-127">On the **User was added page**, clear **Send password in email**, and then click **Close**.</span></span>

<span data-ttu-id="ac844-128">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ac844-128">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="ac844-129">Dans l'onglet **Centre d'administration Microsoft 365** , cliquez sur l'icône groupes dans le volet de navigation de gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="ac844-129">On the **Microsoft 365 admin center** tab, click the groups icon in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="ac844-130">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="ac844-130">Click **Add a group**.</span></span>
3. <span data-ttu-id="ac844-131">Sur la page **nouveau groupe** , tapez **GlobalAdmins**.</span><span class="sxs-lookup"><span data-stu-id="ac844-131">On the **New Group** page, type **GlobalAdmins**.</span></span>
4. <span data-ttu-id="ac844-132">Cliquez sur **Sélectionner le propriétaire** , cliquez sur votre compte d'administrateur général, puis cliquez sur **Ajouter > fermer**.</span><span class="sxs-lookup"><span data-stu-id="ac844-132">Click **Select owner** click your global administrator account, and then click **Add > Close**.</span></span>
5. <span data-ttu-id="ac844-133">Dans la liste des groupes, cliquez sur le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="ac844-133">In the list of groups, click the **GlobalAdmins** group.</span></span>
6. <span data-ttu-id="ac844-134">Sur la page **GlobalAdmins** , cliquez sur modifier le membre, puis sur **Ajouter** **des**membres.</span><span class="sxs-lookup"><span data-stu-id="ac844-134">On the **GlobalAdmins** page, click **Edit for Member**, and then click **Add members**.</span></span>
7. <span data-ttu-id="ac844-135">Dans la liste, cliquez sur le compte **DedicatedAdmin** , puis cliquez sur **Enregistrer _GT_ fermer > fermer _GT_ Centre d'administration**.</span><span class="sxs-lookup"><span data-stu-id="ac844-135">In the list, click the **DedicatedAdmin** account, and then click **Save > Close > Close > Admin center**.</span></span>

<span data-ttu-id="ac844-136">Ensuite, créez des stratégies d'accès conditionnel pour exiger l'authentification multifacteur pour les comptes d'administrateur général et pour refuser l'authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ac844-136">Next, create conditional access policies to require multifactor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="ac844-137">Cette première stratégie nécessite que tous les comptes d'administrateur général utilisent l'authentification multiFACTEUR.</span><span class="sxs-lookup"><span data-stu-id="ac844-137">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="ac844-138">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ac844-138">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="ac844-139">Cliquez sur **Azure Active Directory > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="ac844-139">Click **Azure Active Directory > Conditional access**.</span></span>
3. <span data-ttu-id="ac844-140">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **stratégie de base: exiger MFA pour les administrateurs (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="ac844-140">On the **Conditional access – Policies** blade, click **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="ac844-141">Sur les **stratégies de base...**</span><span class="sxs-lookup"><span data-stu-id="ac844-141">On the **Baseline policies…**</span></span> <span data-ttu-id="ac844-142">, cliquez sur **utiliser la stratégie immédiatement _GT_ enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ac844-142">blade, click **Use policy immediately > Save**.</span></span>

<span data-ttu-id="ac844-143">Cette deuxième stratégie bloque l'accès à l'authentification de compte d'administrateur général lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ac844-143">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="ac844-144">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ac844-144">On the **Conditional access – Policies** blade, click **New policy**.</span></span>
2. <span data-ttu-id="ac844-145">Sur la **nouvelle** Blade, tapez **administrateurs globaux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="ac844-145">On the **New** blade, type **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="ac844-146">Dans la \*\*\*\* section affectations, cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="ac844-146">In the **Assignments** section, click **Users and groups**.</span></span>
4. <span data-ttu-id="ac844-147">Sous l'onglet **inclure** du panneau **utilisateurs et groupes** , cliquez sur Sélectionner des utilisateurs et des groupes **> les utilisateurs et les groupes > sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ac844-147">On the **Include** tab of the **Users and groups** blade, click **Select users and groups > Users and groups > Select**.</span></span>
5. <span data-ttu-id="ac844-148">Sur la Blade de **sélection** , cliquez sur le **GlobalAdmins > sélectionnez >**.</span><span class="sxs-lookup"><span data-stu-id="ac844-148">On the **Select** blade, click the **GlobalAdmins > Select > Done**.</span></span>
6. <span data-ttu-id="ac844-149">Dans la \*\*\*\* section affectations, cliquez sur **conditions**.</span><span class="sxs-lookup"><span data-stu-id="ac844-149">In the **Assignments** section, click **Conditions**.</span></span>
7. <span data-ttu-id="ac844-150">Dans le volet **conditions** , cliquez sur **risque de connexion**, cliquez sur **Oui** pour **configurer**, **sur haute** et **moyenne**, puis sur **sélection** et **fin**.</span><span class="sxs-lookup"><span data-stu-id="ac844-150">On the **Conditions** blade, click **Sign-in risk**, click **Yes** for **Configure**, click **High** and **Medium**, and then click **Select** and **Done**.</span></span>
8. <span data-ttu-id="ac844-151">Dans la section **contrôles d'accès** de la **nouvelle** Blade, cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="ac844-151">In the **Access controls** section of the **New** blade, click **Grant**.</span></span>
9. <span data-ttu-id="ac844-152">Dans le panneau **accorder** , cliquez sur **bloquer l'accès**, puis sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ac844-152">On the **Grant** blade, click **Block access**, and then click **Select**.</span></span>
10. <span data-ttu-id="ac844-153">Sur la **nouvelle** Blade, cliquez \*\*\*\* sur **activer pour activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="ac844-153">On the **New** blade, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="ac844-154">Fermez les onglets **portail Azure** et **Centre d'administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="ac844-154">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="ac844-155">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ac844-155">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="ac844-156">Vous devez être invité à configurer l'authentification multiFACTEUR sur le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ac844-156">You should be prompted to configure MFA on the user account.</span></span> <span data-ttu-id="ac844-157">Cela démontre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="ac844-157">This demonstrates that the first policy is being applied.</span></span>

<span data-ttu-id="ac844-158">Consultez l'étape [protéger les comptes administrateur général](identity-designate-protect-admin-accounts.md#identity-global-admin) dans la phase d'identité pour obtenir des informations et des liens afin de protéger vos comptes d'administrateur général en production.</span><span class="sxs-lookup"><span data-stu-id="ac844-158">See the [Protect global administrator accounts](identity-designate-protect-admin-accounts.md#identity-global-admin) step in the Identity phase for information and links to protect your global administrator accounts in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="ac844-159">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ac844-159">Next step</span></span>

<span data-ttu-id="ac844-160">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ac844-160">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac844-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac844-161">See also</span></span>

[<span data-ttu-id="ac844-162">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="ac844-162">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="ac844-163">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ac844-163">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="ac844-164">Déploiement d'entreprise Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ac844-164">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="ac844-165">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ac844-165">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
