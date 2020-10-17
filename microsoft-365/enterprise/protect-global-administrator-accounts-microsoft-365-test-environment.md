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
ms.openlocfilehash: 1ae04e4761ed86e087e647464ad522466ed6abef
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487635"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="946fa-103">Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="946fa-103">Protect global administrator accounts in your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="946fa-104">*Ce guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="946fa-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="946fa-105">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que les comptes administrateurs sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="946fa-105">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> 

<span data-ttu-id="946fa-106">Cet article explique comment utiliser les stratégies d’accès conditionnel Azure Active Directory (Azure AD) pour protéger les comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="946fa-106">This article describes how to use Azure Active Directory (Azure AD) conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="946fa-107">La protection des comptes administrateur général dans votre environnement de test Microsoft 365 pour entreprise implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="946fa-107">Protecting global administrator accounts in your Microsoft 365 for enterprise test environment involves two phases:</span></span>
- [<span data-ttu-id="946fa-108">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="946fa-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="946fa-109">Phase 2 : configurer les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="946fa-109">Phase 2: Configure conditional access policies</span></span>](#phase-2-configure-conditional-access-policies)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="946fa-111">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="946fa-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="946fa-112">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="946fa-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="946fa-113">Si vous souhaitez tester la protection des comptes administrateur générale avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="946fa-113">If you want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="946fa-114">Si vous souhaitez tester la protection des comptes d’administrateur général dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="946fa-114">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="946fa-115">Le test de la protection de compte d’administrateur général ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="946fa-115">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="946fa-116">Elle est fournie ici en tant qu’option pour vous permettre de tester la protection des comptes d’administrateur général et de l’expérimenter dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="946fa-116">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-conditional-access-policies"></a><span data-ttu-id="946fa-117">Phase 2 : configurer les stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="946fa-117">Phase 2: Configure conditional access policies</span></span>

<span data-ttu-id="946fa-118">Tout d’abord, créez un compte d’utilisateur en tant qu’administrateur global dédié.</span><span class="sxs-lookup"><span data-stu-id="946fa-118">First, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="946fa-119">Sous un onglet séparé, ouvrez le [Centre d’administration Microsoft 365](https://admin.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="946fa-119">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="946fa-120">Sélectionnez **utilisateurs**  >  **actifs**, puis **Ajouter un utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="946fa-120">Select **Users** > **Active users**, and then select **Add a user**.</span></span>
3. <span data-ttu-id="946fa-121">Dans le volet **Ajouter un utilisateur** , entrez **DedicatedAdmin** dans **les zones Prénom,** **nom d’affichage**et nom **d’utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="946fa-121">In the **Add user** pane, enter **DedicatedAdmin** in the **First name**, **Display name**, and **Username** boxes.</span></span>
4. <span data-ttu-id="946fa-122">Sélectionnez **mot de passe**, sélectionnez **me laisser créer le mot de**passe, puis entrez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="946fa-122">Select **Password**, select **Let me create the password**, and then enter a strong password.</span></span> <span data-ttu-id="946fa-123">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="946fa-123">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="946fa-124">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="946fa-124">Select **Next**.</span></span>
6. <span data-ttu-id="946fa-125">Dans le volet **attribuer des licences de produits** , sélectionnez **Microsoft 365 E5**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="946fa-125">In the **Assign product licenses** pane, select **Microsoft 365 E5**, and then select **Next**.</span></span>
7. <span data-ttu-id="946fa-126">Dans le volet **paramètres facultatifs** , sélectionnez le centre d’administration **rôles**  >  **Access**  >  **Global admin**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="946fa-126">In the **Optional settings** pane, select **Roles** > **Admin center access** > **Global admin** > **Next**.</span></span>
8. <span data-ttu-id="946fa-127">Dans le volet **vous êtes presque terminé** , sélectionnez **terminer l’ajout**, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="946fa-127">On the **You're almost done** pane, select **Finish adding**, and then select **Close**.</span></span>

<span data-ttu-id="946fa-128">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="946fa-128">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="946fa-129">Sous l’onglet **Centre d’administration 365 de Microsoft** , sélectionnez **groupes** dans le volet de navigation de gauche, puis sélectionnez **groupes**.</span><span class="sxs-lookup"><span data-stu-id="946fa-129">On the **Microsoft 365 admin center** tab, select **Groups** in the left navigation, and then select **Groups**.</span></span>
2. <span data-ttu-id="946fa-130">Sélectionnez **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="946fa-130">Select **Add a group**.</span></span>
3. <span data-ttu-id="946fa-131">Dans le volet **choisir un type de groupe** , sélectionnez **sécurité**, puis **suivant**.</span><span class="sxs-lookup"><span data-stu-id="946fa-131">In the **Choose a group type** pane, select **Security**, and then select **Next**.</span></span>
4. <span data-ttu-id="946fa-132">Dans le volet **configure the Basics** , sélectionnez **Create Group**, puis **Close**.</span><span class="sxs-lookup"><span data-stu-id="946fa-132">In the **Set up the basics** pane, select **Create group**, and then select **Close**.</span></span>
5. <span data-ttu-id="946fa-133">Dans le volet **vérifier et terminer l’ajout** d’un groupe, entrez **GlobalAdmins**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="946fa-133">In the **Review and finish adding group** pane, enter **GlobalAdmins**, and then select **Next**.</span></span>
7. <span data-ttu-id="946fa-134">Dans la liste des groupes, sélectionnez le groupe **GlobalAdmins** .</span><span class="sxs-lookup"><span data-stu-id="946fa-134">In the list of groups, select the **GlobalAdmins** group.</span></span>
8. <span data-ttu-id="946fa-135">Dans le volet **GlobalAdmins** , sélectionnez **membres**, puis **Afficher tous et gérer les membres**.</span><span class="sxs-lookup"><span data-stu-id="946fa-135">In the **GlobalAdmins** pane, select **Members**, and then select **View all and manage members**.</span></span>
9. <span data-ttu-id="946fa-136">Dans le volet **GlobalAdmins** , sélectionnez **Ajouter des membres**, sélectionnez le compte **DedicatedAdmin** et votre compte d’administrateur général, puis sélectionnez **Enregistrer**  >  **Fermer**  >  **Close**.</span><span class="sxs-lookup"><span data-stu-id="946fa-136">In the **GlobalAdmins** pane, select **Add members**, select the **DedicatedAdmin** account and your global admin account, and then select **Save** > **Close** > **Close**.</span></span>

<span data-ttu-id="946fa-137">Ensuite, créez des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général et pour refuser l’authentification si le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="946fa-137">Next, create conditional access policies to require multi-factor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="946fa-138">Cette première stratégie nécessite que tous les comptes d’administrateur général utilisent l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="946fa-138">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="946fa-139">Dans un nouvel onglet de votre navigateur, accédez à [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="946fa-139">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="946fa-140">Cliquez sur accès conditionnel **Azure Active Directory**  >  **Security**  >  **Conditional Access**.</span><span class="sxs-lookup"><span data-stu-id="946fa-140">Click **Azure Active Directory** > **Security** > **Conditional Access**.</span></span>
3. <span data-ttu-id="946fa-141">Dans le volet **accès conditionnel – stratégies** , sélectionnez **stratégie de base : exiger l’authentification multifacteur pour les administrateurs (aperçu)**.</span><span class="sxs-lookup"><span data-stu-id="946fa-141">In the **Conditional access – Policies** pane, select **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="946fa-142">Dans le volet **stratégie de base** , sélectionnez utiliser la **stratégie immédiatement > enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="946fa-142">In the **Baseline policy** pane, select **Use policy immediately > Save**.</span></span>

<span data-ttu-id="946fa-143">Cette deuxième stratégie bloque l’accès à l’authentification de compte d’administrateur général lorsque le risque de connexion est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="946fa-143">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="946fa-144">Dans le volet **accès conditionnel – stratégies** , sélectionnez **nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="946fa-144">In the **Conditional access – Policies** pane, select **New policy**.</span></span>
2. <span data-ttu-id="946fa-145">Dans le volet **nouveau** , entrez **administrateurs généraux** dans **nom**.</span><span class="sxs-lookup"><span data-stu-id="946fa-145">In the **New** pane, enter **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="946fa-146">Dans la section **affectations** , sélectionnez **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="946fa-146">In the **Assignments** section, select **Users and groups**.</span></span>
4. <span data-ttu-id="946fa-147">Sous l’onglet **inclure** du volet **utilisateurs et groupes** , sélectionnez **Sélectionner des**utilisateurs et des groupes d'  >  **utilisateurs et**  >  **de groupes**.</span><span class="sxs-lookup"><span data-stu-id="946fa-147">On the **Include** tab of the **Users and groups** pane, select **Select users and groups** > **Users and groups** > **Select**.</span></span>
5. <span data-ttu-id="946fa-148">Dans le volet **Sélectionner** , sélectionnez le groupe **GlobalAdmins** , **puis sélectionnez**  >  **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="946fa-148">In the **Select** pane, select the **GlobalAdmins** group, and then select **Select** > **Done**.</span></span>
6. <span data-ttu-id="946fa-149">Dans la section **affectations** , sélectionnez **conditions**.</span><span class="sxs-lookup"><span data-stu-id="946fa-149">In the **Assignments** section, select **Conditions**.</span></span>
7. <span data-ttu-id="946fa-150">Dans le volet **conditions** , sélectionnez **risque de connexion**, cliquez sur **Oui** pour **configurer**, sélectionnez **haute** et **moyenne**, puis sélectionnez **Sélectionner** et **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="946fa-150">In the **Conditions** pane, select **Sign-in risk**, select **Yes** for **Configure**, select **High** and **Medium**, and then select **Select** and **Done**.</span></span>
8. <span data-ttu-id="946fa-151">Dans la section **contrôles d’accès** du **nouveau** volet, sélectionnez **accorder**.</span><span class="sxs-lookup"><span data-stu-id="946fa-151">In the **Access controls** section of the **New** pane, select **Grant**.</span></span>
9. <span data-ttu-id="946fa-152">Dans le volet **accorder** , sélectionnez **bloquer l’accès**, puis sélectionnez **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="946fa-152">In the **Grant** pane, select **Block access**, and then select **Select**.</span></span>
10. <span data-ttu-id="946fa-153">Dans le volet **nouveau** , sélectionnez **activé** pour **activer la stratégie**, puis **créer**.</span><span class="sxs-lookup"><span data-stu-id="946fa-153">In the **New** pane, select **On** for **Enable policy**, and then select **Create**.</span></span>
11. <span data-ttu-id="946fa-154">Fermez les onglets **portail Azure** et **Centre d’administration Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="946fa-154">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="946fa-155">Pour tester la première stratégie, déconnectez-vous, puis connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="946fa-155">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="946fa-156">Vous devez être invité à configurer l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="946fa-156">You should be prompted to configure MFA.</span></span> <span data-ttu-id="946fa-157">Cela démontre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="946fa-157">This demonstrates that the first policy is being applied.</span></span>

## <a name="next-step"></a><span data-ttu-id="946fa-158">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="946fa-158">Next step</span></span>

<span data-ttu-id="946fa-159">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="946fa-159">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="946fa-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="946fa-160">See also</span></span>

[<span data-ttu-id="946fa-161">Feuille de route d’identité</span><span class="sxs-lookup"><span data-stu-id="946fa-161">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="946fa-162">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="946fa-162">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="946fa-163">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="946fa-163">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="946fa-164">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="946fa-164">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
