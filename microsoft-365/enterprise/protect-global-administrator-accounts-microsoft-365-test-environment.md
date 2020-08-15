---
title: Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 pour les entreprises
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Suivez ces étapes pour protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: fff09ca41ff0b648d46b5c33f753affc01242264
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695181"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="ab1e6-103">Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ab1e6-103">Protect global administrator accounts in your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="ab1e6-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="ab1e6-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="ab1e6-105">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que les comptes administrateurs sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-105">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> <span data-ttu-id="ab1e6-106">Cet article explique comment utiliser les stratégies d’accès conditionnel Azure Active Directory (Azure AD) pour protéger les comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-106">This article describes how to use Azure Active Directory (Azure AD) conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="ab1e6-107">Il existe deux phases pour la protection des comptes d’administrateur général dans votre environnement de test Microsoft 365 pour les entreprises :</span><span class="sxs-lookup"><span data-stu-id="ab1e6-107">There are two phases to protecting global administrator accounts in your Microsoft 365 for enterprise test environment:</span></span>

1.  <span data-ttu-id="ab1e6-108">Créez l’environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-108">Create the Microsoft 365 for enterprise test environment.</span></span>
2.  <span data-ttu-id="ab1e6-109">Protégez votre compte d’administrateur général dédié.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-109">Protect your dedicated global administrator account.</span></span>

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="ab1e6-111">Cliquez [ici](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) pour afficher le plan visuel de tous les articles de l’ensemble des guides de laboratoire de test de Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-111">Click [here](../media/m365-enterprise-test-lab-guides/Microsoft365EnterpriseTLGStack.pdf) for a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack.</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="ab1e6-112">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ab1e6-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="ab1e6-113">Si vous souhaitez simplement tester la protection de compte d’administrateur général de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="ab1e6-113">If you just want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="ab1e6-114">Si vous souhaitez tester la protection des comptes d’administrateur général dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ab1e6-114">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ab1e6-115">Le test de la protection de compte d’administrateur général ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="ab1e6-115">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="ab1e6-116">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des comptes d’administrateur général et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-116">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-conditional-access-policies"></a><span data-ttu-id="ab1e6-117">Phase 2 : configurer les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="ab1e6-117">Phase 2: Configure conditional access policies</span></span>

<span data-ttu-id="ab1e6-118">Tout d’abord, créez un compte d’utilisateur en tant qu’administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-118">First, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="ab1e6-119">Sous un onglet séparé, ouvrez le [Centre d’administration Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ab1e6-119">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="ab1e6-120">Cliquez sur **utilisateurs > utilisateurs actifs**, puis cliquez sur **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-120">Click **Users > Active users**, and then click **Add a user**.</span></span>
3. <span data-ttu-id="ab1e6-121">Dans le **volet ajouter un utilisateur** , tapez **DedicatedAdmin** dans **prénom**, **nom d’affichage**et nom **d’utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-121">In the **Add user** pane, type **DedicatedAdmin** in **First name**, **Display name**, and **Username**.</span></span>
4. <span data-ttu-id="ab1e6-122">Cliquez sur **mot de passe**, sur **me laisser créer le mot de**passe, puis tapez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-122">Click **Password**, click **Let me create the password**, and then type a strong password.</span></span> <span data-ttu-id="ab1e6-123">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-123">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="ab1e6-124">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-124">Click **Next**.</span></span>
6. <span data-ttu-id="ab1e6-125">Dans le volet **attribuer des licences de produits** , sélectionnez **Microsoft 365 E5**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-125">In the **Assign product licenses** pane, select **Microsoft 365 E5**, and then click **Next**.</span></span>
7. <span data-ttu-id="ab1e6-126">Dans le volet **paramètres facultatifs** , cliquez sur **rôles**, puis sélectionnez **accès au centre d’administration** et **administrateur global**. Cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-126">In the **Optional settings** pane, click **Roles**, and then select **Admin center access** and **Global admin**. Click **Next**.</span></span>
8. <span data-ttu-id="ab1e6-127">Dans le volet **vous êtes presque terminé** , cliquez sur **terminer l’ajout**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-127">On the **You're almost done** pane, click **Finish adding**, and then click **Close**.</span></span>

<span data-ttu-id="ab1e6-128">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-128">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="ab1e6-129">Dans l’onglet **Centre d’administration Microsoft 365** , cliquez sur **groupes** dans le volet de navigation de gauche, puis cliquez sur **groupes**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-129">On the **Microsoft 365 admin center** tab, click **Groups** in the left navigation, and then click **Groups**.</span></span>
2. <span data-ttu-id="ab1e6-130">Cliquez sur **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-130">Click **Add a group**.</span></span>
3. <span data-ttu-id="ab1e6-131">Dans le volet **choisir un type de groupe** , sélectionnez **sécurité**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-131">In the **Choose a group type** pane, select **Security**, and then click **Next**.</span></span>
4. <span data-ttu-id="ab1e6-132">Dans le volet **configurer les concepts de base** , cliquez sur **créer un groupe**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-132">In the **Set up the basics** pane, click **Create group**, and then click **Close**.</span></span>
5. <span data-ttu-id="ab1e6-133">Dans le volet **vérifier et terminer l’ajout** d’un groupe, tapez **GlobalAdmins**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-133">In the **Review and finish adding group** pane, type **GlobalAdmins**, and then click **Next**.</span></span>
7. <span data-ttu-id="ab1e6-134">Dans la liste des groupes, cliquez sur le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="ab1e6-134">In the list of groups, click the **GlobalAdmins** group.</span></span>
8. <span data-ttu-id="ab1e6-135">Dans le volet **GlobalAdmins** , cliquez sur **membres**, puis sur **Afficher tout et gérer les membres**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-135">In the **GlobalAdmins** pane, click **Members**, and then click **View all and manage members**.</span></span>
9. <span data-ttu-id="ab1e6-136">Dans le volet **GlobalAdmins** , cliquez sur **Ajouter des membres**, sélectionnez le compte **DedicatedAdmin** et votre compte d’administrateur général, puis cliquez sur **Enregistrer > fermer > fermer**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-136">In the **GlobalAdmins** pane, click **Add members**, select the **DedicatedAdmin** account and your global admin account, and then click **Save > Close > Close**.</span></span>

<span data-ttu-id="ab1e6-137">Ensuite, créez des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général et pour refuser l’authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-137">Next, create conditional access policies to require multifactor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="ab1e6-138">Cette première stratégie nécessite que tous les comptes d’administrateur général utilisent l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-138">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="ab1e6-139">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="ab1e6-139">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="ab1e6-140">Cliquez sur **Azure Active Directory > sécurité > accès conditionnel**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-140">Click **Azure Active Directory > Security > Conditional Access**.</span></span>
3. <span data-ttu-id="ab1e6-141">Dans le volet **accès conditionnel – stratégies** , cliquez sur **stratégie de base : exiger l’authentification multifacteur pour les administrateurs (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-141">In the **Conditional access – Policies** pane, click **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="ab1e6-142">Dans le volet **stratégie de base** , cliquez sur utiliser la **stratégie immédiatement > enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-142">In the **Baseline policy** pane, click **Use policy immediately > Save**.</span></span>

<span data-ttu-id="ab1e6-143">Cette deuxième stratégie bloque l’accès à l’authentification de compte d’administrateur général lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-143">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="ab1e6-144">Dans le volet **accès conditionnel – stratégies** , cliquez sur **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-144">In the **Conditional access – Policies** pane, click **New policy**.</span></span>
2. <span data-ttu-id="ab1e6-145">Dans le volet **nouveau** , tapez **administrateurs globaux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-145">In the **New** pane, type **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="ab1e6-146">Dans la section **affectations** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-146">In the **Assignments** section, click **Users and groups**.</span></span>
4. <span data-ttu-id="ab1e6-147">Sous l’onglet **inclure** du volet **utilisateurs et groupes** , cliquez sur Sélectionner des utilisateurs et des groupes **> utilisateurs et des groupes > sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-147">On the **Include** tab of the **Users and groups** pane, click **Select users and groups > Users and groups > Select**.</span></span>
5. <span data-ttu-id="ab1e6-148">Dans le volet **Sélectionner** , cliquez sur le groupe **GlobalAdmins** , puis cliquez sur **Sélectionner > terminée**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-148">In the **Select** pane, click the **GlobalAdmins** group, and then click **Select > Done**.</span></span>
6. <span data-ttu-id="ab1e6-149">Dans la section **affectations** , cliquez sur **conditions**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-149">In the **Assignments** section, click **Conditions**.</span></span>
7. <span data-ttu-id="ab1e6-150">Dans le volet **conditions** , cliquez sur **risque de connexion**, cliquez sur **Oui** pour **configurer**, **sur haute** et **moyenne**, puis sur **sélection** et **fin**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-150">In the **Conditions** pane, click **Sign-in risk**, click **Yes** for **Configure**, click **High** and **Medium**, and then click **Select** and **Done**.</span></span>
8. <span data-ttu-id="ab1e6-151">Dans la section **contrôles d’accès** du **nouveau** volet, cliquez sur **accorder**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-151">In the **Access controls** section of the **New** pane, click **Grant**.</span></span>
9. <span data-ttu-id="ab1e6-152">Dans le volet **accorder** , cliquez sur **bloquer l’accès**, puis sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-152">In the **Grant** pane, click **Block access**, and then click **Select**.</span></span>
10. <span data-ttu-id="ab1e6-153">Dans le volet **nouveau** , cliquez sur **activé** pour **activer la stratégie**, puis cliquez sur **créer**.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-153">In the **New** pane, click **On** for **Enable policy**, and then click **Create**.</span></span>
11. <span data-ttu-id="ab1e6-154">Fermez les onglets **portail Azure** et **Centre d’administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="ab1e6-154">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="ab1e6-155">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-155">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="ab1e6-156">Vous devez être invité à configurer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-156">You should be prompted to configure MFA.</span></span> <span data-ttu-id="ab1e6-157">Cela démontre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-157">This demonstrates that the first policy is being applied.</span></span>

## <a name="next-step"></a><span data-ttu-id="ab1e6-158">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ab1e6-158">Next step</span></span>

<span data-ttu-id="ab1e6-159">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-159">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab1e6-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab1e6-160">See also</span></span>

[<span data-ttu-id="ab1e6-161">Feuille de route d’identité</span><span class="sxs-lookup"><span data-stu-id="ab1e6-161">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="ab1e6-162">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="ab1e6-162">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="ab1e6-163">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="ab1e6-163">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="ab1e6-164">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="ab1e6-164">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
