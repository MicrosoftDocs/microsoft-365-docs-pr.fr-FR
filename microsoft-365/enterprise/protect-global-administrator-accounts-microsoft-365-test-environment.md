---
title: Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/16/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Suivez ces étapes pour protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: 89985f99f5471aab87189e78035062add2c6bad9
ms.sourcegitcommit: 9ee873c6a2f738a0c99921e036894b646742e706
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2019
ms.locfileid: "38673330"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ecc4f-103">Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ecc4f-103">Protect global administrator accounts in your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ecc4f-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 entreprise.*</span><span class="sxs-lookup"><span data-stu-id="ecc4f-104">*This Test Lab Guide can only be used for Microsoft 365 Enterprise test environments.*</span></span>

<span data-ttu-id="ecc4f-105">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que les comptes administrateurs sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-105">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="ecc4f-106">Cet article explique comment utiliser les stratégies d’accès conditionnel Azure Active Directory (Azure AD) pour protéger les comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-106">This article describes how to use Azure Active Directory (Azure AD) conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="ecc4f-107">Il existe deux phases pour la protection des comptes d’administrateur général dans votre environnement de test Microsoft 365 Enterprise :</span><span class="sxs-lookup"><span data-stu-id="ecc4f-107">There are two phases to protecting global administrator accounts in your Microsoft 365 Enterprise test environment:</span></span>

1.  <span data-ttu-id="ecc4f-108">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-108">Create the Microsoft 365 Enterprise test environment.</span></span>
2.  <span data-ttu-id="ecc4f-109">Protégez votre compte d’administrateur général dédié.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-109">Protect your dedicated global administrator account.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="ecc4f-111">Cliquez [ici](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-111">Click [here](media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="ecc4f-112">Phase 1 : Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-112">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="ecc4f-113">Si vous souhaitez simplement tester la protection de compte d’administrateur général de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="ecc4f-113">If you just want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="ecc4f-114">Si vous souhaitez tester la protection des comptes d’administrateur général dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ecc4f-114">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>

  
> [!NOTE]
> <span data-ttu-id="ecc4f-115">Le test de la protection de compte d’administrateur général ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ecc4f-115">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="ecc4f-116">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des comptes d’administrateur général et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-116">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-conditional-access-policies"></a><span data-ttu-id="ecc4f-117">Phase 2 : configurer les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="ecc4f-117">Phase 2: Configure conditional access policies</span></span>

<span data-ttu-id="ecc4f-118">Tout d’abord, créez un compte d’utilisateur en tant qu’administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-118">First, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="ecc4f-119">Sous un onglet séparé, ouvrez le [Centre d’administration Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ecc4f-119">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="ecc4f-120">Sous **utilisateurs actifs**, cliquez sur **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-120">Under **Active users**, click **Add a user**.</span></span>
3. <span data-ttu-id="ecc4f-121">Sur la page **nouvel utilisateur** , tapez **DedicatedAdmin** dans **prénom**, **nom d’affichage**et nom **d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-121">On the **New user** page, type **DedicatedAdmin** in **First name**, **Display name**, and **Username**.</span></span>
4. <span data-ttu-id="ecc4f-122">Cliquez sur **mot de passe**, sur **me laisser créer le mot de**passe, puis tapez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-122">Click **Password**, click **Let me create the password**, and then type a strong password.</span></span> <span data-ttu-id="ecc4f-123">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-123">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="ecc4f-124">Décochez **faire en sorte que cet utilisateur modifie son mot de passe lors de sa première connexion**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-124">Clear **Make this user change their password when they first sign in**.</span></span>
6. <span data-ttu-id="ecc4f-125">Cliquez sur **rôles**, puis sur **administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-125">Click **Roles**, and then click **Global administrator**.</span></span>
7. <span data-ttu-id="ecc4f-126">Cliquez sur **licences de produit**, puis activez les licences **Enterprise Mobility + Security e5** et **Office 365 entreprise E5** sur.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-126">Click **Product licenses**, and then turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5 licenses** on.</span></span>
8. <span data-ttu-id="ecc4f-127">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-127">Click **Add**.</span></span>
9. <span data-ttu-id="ecc4f-128">Dans la **page l’utilisateur a été ajouté**, effacez le **mot de passe Envoyer un message électronique**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-128">On the **User was added page**, clear **Send password in email**, and then click **Close**.</span></span>

<span data-ttu-id="ecc4f-129">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-129">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="ecc4f-130">Dans l’onglet **Centre d’administration Microsoft 365** , cliquez sur l’icône groupes dans le volet de navigation de gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-130">On the **Microsoft 365 admin center** tab, click the groups icon in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="ecc4f-131">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-131">Click **Add a group**.</span></span>
3. <span data-ttu-id="ecc4f-132">Sur la page **nouveau groupe** , tapez **GlobalAdmins**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-132">On the **New Group** page, type **GlobalAdmins**.</span></span>
4. <span data-ttu-id="ecc4f-133">Cliquez sur **Sélectionner le propriétaire** , cliquez sur votre compte d’administrateur général, puis cliquez sur **Ajouter > fermer**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-133">Click **Select owner** click your global administrator account, and then click **Add > Close**.</span></span>
5. <span data-ttu-id="ecc4f-134">Dans la liste des groupes, cliquez sur le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="ecc4f-134">In the list of groups, click the **GlobalAdmins** group.</span></span>
6. <span data-ttu-id="ecc4f-135">Sur la page **GlobalAdmins** , cliquez sur modifier le membre, puis sur **Ajouter** **des**membres.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-135">On the **GlobalAdmins** page, click **Edit for Member**, and then click **Add members**.</span></span>
7. <span data-ttu-id="ecc4f-136">Dans la liste, cliquez sur le compte **DedicatedAdmin** , puis cliquez sur **enregistrer > fermer > fermer le centre d’administration >**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-136">In the list, click the **DedicatedAdmin** account, and then click **Save > Close > Close > Admin center**.</span></span>

<span data-ttu-id="ecc4f-137">Ensuite, créez des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général et pour refuser l’authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-137">Next, create conditional access policies to require multifactor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="ecc4f-138">Cette première stratégie nécessite que tous les comptes d’administrateur général utilisent l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-138">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="ecc4f-139">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ecc4f-139">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="ecc4f-140">Cliquez sur **Azure Active Directory > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-140">Click **Azure Active Directory > Conditional access**.</span></span>
3. <span data-ttu-id="ecc4f-141">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **stratégie de base : exiger MFA pour les administrateurs (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-141">On the **Conditional access – Policies** blade, click **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="ecc4f-142">Sur les **stratégies de base...**</span><span class="sxs-lookup"><span data-stu-id="ecc4f-142">On the **Baseline policies…**</span></span> <span data-ttu-id="ecc4f-143">, cliquez sur **utiliser la stratégie immédiatement > enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-143">blade, click **Use policy immediately > Save**.</span></span>

<span data-ttu-id="ecc4f-144">Cette deuxième stratégie bloque l’accès à l’authentification de compte d’administrateur général lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-144">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="ecc4f-145">Dans le panneau **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-145">On the **Conditional access – Policies** blade, click **New policy**.</span></span>
2. <span data-ttu-id="ecc4f-146">Sur la **nouvelle** Blade, tapez **administrateurs globaux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-146">On the **New** blade, type **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="ecc4f-147">Dans la section **affectations** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-147">In the **Assignments** section, click **Users and groups**.</span></span>
4. <span data-ttu-id="ecc4f-148">Sous l’onglet **inclure** du panneau **utilisateurs et groupes** , cliquez sur **Sélectionner les utilisateurs et les groupes > utilisateurs et groupes > sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-148">On the **Include** tab of the **Users and groups** blade, click **Select users and groups > Users and groups > Select**.</span></span>
5. <span data-ttu-id="ecc4f-149">Dans la Blade de **sélection** , cliquez sur l' **GlobalAdmins > sélectionnez > terminée**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-149">On the **Select** blade, click the **GlobalAdmins > Select > Done**.</span></span>
6. <span data-ttu-id="ecc4f-150">Dans la section **affectations** , cliquez sur **conditions**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-150">In the **Assignments** section, click **Conditions**.</span></span>
7. <span data-ttu-id="ecc4f-151">Dans le volet **conditions** , cliquez sur **risque de connexion**, cliquez sur **Oui** pour **configurer**, **sur haute** et **moyenne**, puis sur **sélection** et **fin**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-151">On the **Conditions** blade, click **Sign-in risk**, click **Yes** for **Configure**, click **High** and **Medium**, and then click **Select** and **Done**.</span></span>
8. <span data-ttu-id="ecc4f-152">Dans la section **contrôles d’accès** de la **nouvelle** Blade, cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-152">In the **Access controls** section of the **New** blade, click **Grant**.</span></span>
9. <span data-ttu-id="ecc4f-153">Dans le panneau **accorder** , cliquez sur **bloquer l’accès**, puis sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-153">On the **Grant** blade, click **Block access**, and then click **Select**.</span></span>
10. <span data-ttu-id="ecc4f-154">Sur la **nouvelle** Blade, cliquez **sur** activer pour **activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-154">On the **New** blade, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="ecc4f-155">Fermez les onglets **portail Azure** et **Centre d’administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="ecc4f-155">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="ecc4f-156">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-156">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="ecc4f-157">Vous devez être invité à configurer l’authentification multifacteur sur le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-157">You should be prompted to configure MFA on the user account.</span></span> <span data-ttu-id="ecc4f-158">Cela démontre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-158">This demonstrates that the first policy is being applied.</span></span>

<span data-ttu-id="ecc4f-159">Consultez l’étape [protéger les comptes administrateur général](identity-create-protect-global-admins.md#identity-global-admin) dans la phase d’identité pour obtenir des informations et des liens afin de protéger vos comptes d’administrateur général en production.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-159">See the [Protect global administrator accounts](identity-create-protect-global-admins.md#identity-global-admin) step in the Identity phase for information and links to protect your global administrator accounts in production.</span></span>

## <a name="next-step"></a><span data-ttu-id="ecc4f-160">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ecc4f-160">Next step</span></span>

<span data-ttu-id="ecc4f-161">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ecc4f-161">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecc4f-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecc4f-162">See also</span></span>

[<span data-ttu-id="ecc4f-163">Étape 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="ecc4f-163">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="ecc4f-164">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ecc4f-164">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="ecc4f-165">Déploiement de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ecc4f-165">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="ecc4f-166">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="ecc4f-166">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
