---
title: Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 entreprise
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
description: Utilisez ces étapes pour protéger les comptes d’administrateur général dans votre Microsoft 365 environnement de test d’entreprise.
ms.openlocfilehash: 3eab538b59e460857e2fa195aaacf51051f94d6b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50918881"
---
# <a name="protect-global-administrator-accounts-in-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="b3243-103">Protéger les comptes d’administrateur général dans votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="b3243-103">Protect global administrator accounts in your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="b3243-104">*Ce Guide de laboratoire de test ne peut être utilisé que pour Microsoft 365 pour les environnements de test d’entreprise.*</span><span class="sxs-lookup"><span data-stu-id="b3243-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="b3243-105">Vous pouvez empêcher les attaques numériques sur votre organisation en vous assurant que vos comptes d’administrateur sont aussi sécurisés que possible.</span><span class="sxs-lookup"><span data-stu-id="b3243-105">You can prevent digital attacks on your organization by ensuring that your administrator accounts are as secure as possible.</span></span> 

<span data-ttu-id="b3243-106">Cet article explique comment utiliser des stratégies d Azure Active Directory conditionnel (Azure AD) pour protéger les comptes d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="b3243-106">This article describes how to use Azure Active Directory (Azure AD) conditional access policies to protect global administrator accounts.</span></span>

<span data-ttu-id="b3243-107">La protection des comptes d’administrateur général dans votre Microsoft 365 environnement de test d’entreprise implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="b3243-107">Protecting global administrator accounts in your Microsoft 365 for enterprise test environment involves two phases:</span></span>
- [<span data-ttu-id="b3243-108">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="b3243-108">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="b3243-109">Phase 2 : Configuration des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b3243-109">Phase 2: Configure conditional access policies</span></span>](#phase-2-configure-conditional-access-policies)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="b3243-111">Pour obtenir une carte visuelle de tous les articles de la pile Microsoft 365 guide de laboratoire de test pour entreprise, Microsoft 365 pour la pile de guides de laboratoire de [test d’entreprise.](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="b3243-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>

## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="b3243-112">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="b3243-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="b3243-113">Si vous souhaitez tester la protection des comptes d’administrateur général de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="b3243-113">If you want to test global administrator account protection in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="b3243-114">Si vous souhaitez tester la protection des comptes d’administrateur général dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="b3243-114">If you want to test global administrator account protection in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3243-115">Le test de la protection des comptes d’administrateur général ne nécessite pas l’environnement de test en entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour les services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b3243-115">Testing global administrator account protection does not require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="b3243-116">Il est fourni ici en tant qu’option afin que vous pouvez tester la protection des comptes d’administrateur général et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="b3243-116">It is provided here as an option so that you can test global administrator account protection and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-conditional-access-policies"></a><span data-ttu-id="b3243-117">Phase 2 : Configuration des stratégies d’accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="b3243-117">Phase 2: Configure conditional access policies</span></span>

<span data-ttu-id="b3243-118">Tout d’abord, créez un compte d’utilisateur en tant qu’administrateur général dédié.</span><span class="sxs-lookup"><span data-stu-id="b3243-118">First, create a new user account as a dedicated global administrator.</span></span>

1. <span data-ttu-id="b3243-119">Sous un onglet distinct, ouvrez le [centre Microsoft 365'administration.](https://admin.microsoft.com/)</span><span class="sxs-lookup"><span data-stu-id="b3243-119">On a separate tab, open the [Microsoft 365 admin center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="b3243-120">Sélectionnez   >  **Utilisateurs actifs,** puis **ajoutez un utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="b3243-120">Select **Users** > **Active users**, and then select **Add a user**.</span></span>
3. <span data-ttu-id="b3243-121">Dans le **volet Ajouter un utilisateur,** entrez **DedicatedAdmin** dans les zones **Prénom,** Nom **d’affichage** et **Nom d’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="b3243-121">In the **Add user** pane, enter **DedicatedAdmin** in the **First name**, **Display name**, and **Username** boxes.</span></span>
4. <span data-ttu-id="b3243-122">Sélectionnez **Mot** de passe, **Sélectionnez Me laisser créer le** mot de passe, puis entrez un mot de passe fort.</span><span class="sxs-lookup"><span data-stu-id="b3243-122">Select **Password**, select **Let me create the password**, and then enter a strong password.</span></span> <span data-ttu-id="b3243-123">Enregistrez le mot de passe de ce nouveau compte dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b3243-123">Record the password for this new account in a secure location.</span></span>
5. <span data-ttu-id="b3243-124">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b3243-124">Select **Next**.</span></span>
6. <span data-ttu-id="b3243-125">Dans le **volet Attribuer des licences de** produits, **sélectionnez Microsoft 365 E5,** puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="b3243-125">In the **Assign product licenses** pane, select **Microsoft 365 E5**, and then select **Next**.</span></span>
7. <span data-ttu-id="b3243-126">Dans le **volet Paramètres facultatifs,** sélectionnez **Rôles**  >  **Admin center access** Global  >  **admin**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="b3243-126">In the **Optional settings** pane, select **Roles** > **Admin center access** > **Global admin** > **Next**.</span></span>
8. <span data-ttu-id="b3243-127">Dans le **volet Vous avez presque terminé,** sélectionnez Terminer **l’ajout,** puis **fermez**.</span><span class="sxs-lookup"><span data-stu-id="b3243-127">On the **You're almost done** pane, select **Finish adding**, and then select **Close**.</span></span>

<span data-ttu-id="b3243-128">Ensuite, créez un groupe nommé GlobalAdmins et ajoutez-y le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="b3243-128">Next, create a new group named GlobalAdmins and add the DedicatedAdmin account to it.</span></span>

1. <span data-ttu-id="b3243-129">Sous **l’Microsoft 365 du Centre d’administration,** sélectionnez **Groupes** dans le navigation de gauche, puis **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="b3243-129">On the **Microsoft 365 admin center** tab, select **Groups** in the left navigation, and then select **Groups**.</span></span>
2. <span data-ttu-id="b3243-130">Sélectionnez **Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="b3243-130">Select **Add a group**.</span></span>
3. <span data-ttu-id="b3243-131">Dans le **volet Choisir un type de groupe,** sélectionnez **Sécurité,** puis Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b3243-131">In the **Choose a group type** pane, select **Security**, and then select **Next**.</span></span>
4. <span data-ttu-id="b3243-132">Dans le **volet Configurer les informations** de base, sélectionnez Créer un groupe, puis **fermez.** </span><span class="sxs-lookup"><span data-stu-id="b3243-132">In the **Set up the basics** pane, select **Create group**, and then select **Close**.</span></span>
5. <span data-ttu-id="b3243-133">Dans le **volet Révision et fin de l’ajout de** groupes, entrez **GlobalAdmins,** puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="b3243-133">In the **Review and finish adding group** pane, enter **GlobalAdmins**, and then select **Next**.</span></span>
7. <span data-ttu-id="b3243-134">Dans la liste des groupes, sélectionnez le **groupe GlobalAdmins.**</span><span class="sxs-lookup"><span data-stu-id="b3243-134">In the list of groups, select the **GlobalAdmins** group.</span></span>
8. <span data-ttu-id="b3243-135">Dans le **volet GlobalAdmins,** sélectionnez **Membres,** puis afficher **tout et gérer les membres.**</span><span class="sxs-lookup"><span data-stu-id="b3243-135">In the **GlobalAdmins** pane, select **Members**, and then select **View all and manage members**.</span></span>
9. <span data-ttu-id="b3243-136">Dans le **volet GlobalAdmins,** sélectionnez Ajouter des **membres,** sélectionnez le compte **DedicatedAdmin** et votre compte d’administrateur global, puis **sélectionnez Enregistrer**  >  **fermer.**  >  </span><span class="sxs-lookup"><span data-stu-id="b3243-136">In the **GlobalAdmins** pane, select **Add members**, select the **DedicatedAdmin** account and your global admin account, and then select **Save** > **Close** > **Close**.</span></span>

<span data-ttu-id="b3243-137">Ensuite, créez des stratégies d’accès conditionnel pour exiger l’authentification multifacteur pour les comptes d’administrateur général et refuser l’authentification si le risque de se connecte est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="b3243-137">Next, create conditional access policies to require multi-factor authentication for global administrator accounts and to deny authentication if the sign-in risk is medium or high.</span></span>

<span data-ttu-id="b3243-138">Cette première stratégie nécessite que tous les comptes d’administrateur général utilisent l’mf.</span><span class="sxs-lookup"><span data-stu-id="b3243-138">This first policy requires that all global administrator accounts use MFA.</span></span>

1. <span data-ttu-id="b3243-139">Dans un nouvel onglet de votre navigateur, allez à [https://portal.azure.com](https://portal.azure.com) .</span><span class="sxs-lookup"><span data-stu-id="b3243-139">In a new tab of your browser, go to [https://portal.azure.com](https://portal.azure.com).</span></span>
2. <span data-ttu-id="b3243-140">Cliquez **sur Azure Active Directory** accès  >  **conditionnel à** la  >  **sécurité.**</span><span class="sxs-lookup"><span data-stu-id="b3243-140">Click **Azure Active Directory** > **Security** > **Conditional Access**.</span></span>
3. <span data-ttu-id="b3243-141">Dans le **volet Accès conditionnel – Stratégies,** sélectionnez Stratégie de référence : Exiger l’pertinence de l’élection de l’élection **(prévisualisation) pour les administrateurs.**</span><span class="sxs-lookup"><span data-stu-id="b3243-141">In the **Conditional access – Policies** pane, select **Baseline policy: Require MFA for admins (preview)**.</span></span>
4. <span data-ttu-id="b3243-142">Dans le **volet Stratégie de** référence, **sélectionnez Utiliser la stratégie immédiatement > Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="b3243-142">In the **Baseline policy** pane, select **Use policy immediately > Save**.</span></span>

<span data-ttu-id="b3243-143">Cette deuxième stratégie bloque l’accès à l’authentification de compte d’administrateur général lorsque le risque de se connecte est moyen ou élevé.</span><span class="sxs-lookup"><span data-stu-id="b3243-143">This second policy blocks access to global administrator account authentication when the sign-in risk is medium or high.</span></span>

1. <span data-ttu-id="b3243-144">Dans le **volet Accès conditionnel – Stratégies,** sélectionnez **Nouvelle stratégie.**</span><span class="sxs-lookup"><span data-stu-id="b3243-144">In the **Conditional access – Policies** pane, select **New policy**.</span></span>
2. <span data-ttu-id="b3243-145">Dans le **nouveau volet,** entrez **Administrateurs globaux** dans **Nom.**</span><span class="sxs-lookup"><span data-stu-id="b3243-145">In the **New** pane, enter **Global administrators** in **Name**.</span></span>
3. <span data-ttu-id="b3243-146">Dans la section **Affectations,** sélectionnez **Utilisateurs et groupes.**</span><span class="sxs-lookup"><span data-stu-id="b3243-146">In the **Assignments** section, select **Users and groups**.</span></span>
4. <span data-ttu-id="b3243-147">Dans **l’onglet**  Inclure du volet Utilisateurs et groupes, sélectionnez Sélectionner des utilisateurs et des **groupes**  >  **Utilisateurs et groupes**  >  **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="b3243-147">On the **Include** tab of the **Users and groups** pane, select **Select users and groups** > **Users and groups** > **Select**.</span></span>
5. <span data-ttu-id="b3243-148">Dans le **volet** Sélectionner, sélectionnez le **groupe GlobalAdmins,** puis **sélectionnez**  >  **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="b3243-148">In the **Select** pane, select the **GlobalAdmins** group, and then select **Select** > **Done**.</span></span>
6. <span data-ttu-id="b3243-149">Dans la section **Affectations,** sélectionnez **Conditions.**</span><span class="sxs-lookup"><span data-stu-id="b3243-149">In the **Assignments** section, select **Conditions**.</span></span>
7. <span data-ttu-id="b3243-150">Dans le **volet Conditions,** sélectionnez Risque  de se connectez, sélectionnez Oui pour Configurer, Sélectionnez Élevé et **Moyen,** puis Sélectionnez Sélectionner **et** **Terminé.**   </span><span class="sxs-lookup"><span data-stu-id="b3243-150">In the **Conditions** pane, select **Sign-in risk**, select **Yes** for **Configure**, select **High** and **Medium**, and then select **Select** and **Done**.</span></span>
8. <span data-ttu-id="b3243-151">Dans la section **Contrôles d’accès** du **nouveau** volet, sélectionnez **Accorder**.</span><span class="sxs-lookup"><span data-stu-id="b3243-151">In the **Access controls** section of the **New** pane, select **Grant**.</span></span>
9. <span data-ttu-id="b3243-152">Dans le **volet Accorder,** sélectionnez Bloquer **l’accès,** puis sélectionnez **Sélectionner.**</span><span class="sxs-lookup"><span data-stu-id="b3243-152">In the **Grant** pane, select **Block access**, and then select **Select**.</span></span>
10. <span data-ttu-id="b3243-153">Dans le **volet** Nouveau, sélectionnez **Activer** pour **activer** la stratégie, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="b3243-153">In the **New** pane, select **On** for **Enable policy**, and then select **Create**.</span></span>
11. <span data-ttu-id="b3243-154">Fermez le **portail Azure et** Microsoft 365 **onglets du Centre d’administration.**</span><span class="sxs-lookup"><span data-stu-id="b3243-154">Close the **Azure portal** and **Microsoft 365 admin center** tabs.</span></span>

<span data-ttu-id="b3243-155">Pour tester la première stratégie, dé connectez-vous avec le compte DedicatedAdmin.</span><span class="sxs-lookup"><span data-stu-id="b3243-155">To test the first policy, sign out and sign in with the DedicatedAdmin account.</span></span> <span data-ttu-id="b3243-156">Vous devez être invité à configurer l’mf.</span><span class="sxs-lookup"><span data-stu-id="b3243-156">You should be prompted to configure MFA.</span></span> <span data-ttu-id="b3243-157">Cela montre que la première stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="b3243-157">This demonstrates that the first policy is being applied.</span></span>

## <a name="next-step"></a><span data-ttu-id="b3243-158">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b3243-158">Next step</span></span>

<span data-ttu-id="b3243-159">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="b3243-159">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3243-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3243-160">See also</span></span>

[<span data-ttu-id="b3243-161">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="b3243-161">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="b3243-162">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="b3243-162">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="b3243-163">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="b3243-163">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="b3243-164">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="b3243-164">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)