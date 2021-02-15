---
title: Automatiser les licences et l’appartenance aux groupes pour votre environnement de test Microsoft 365 pour entreprise
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/09/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: Configurez la gestion des licences basée sur les groupes et l’appartenance à un groupe dynamique dans votre environnement de test Microsoft 365 pour entreprise.
ms.openlocfilehash: d770e7be3b0b55855f1fee26a45d55260c3074cb
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487575"
---
# <a name="automate-licensing-and-group-membership-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="3f542-103">Automatiser les licences et l’appartenance aux groupes pour votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="3f542-103">Automate licensing and group membership for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="3f542-104">*Ce guide de laboratoire de test ne peut être utilisé que pour les environnements de test Microsoft 365 pour les entreprises.*</span><span class="sxs-lookup"><span data-stu-id="3f542-104">*This Test Lab Guide can only be used for Microsoft 365 for enterprise test environments.*</span></span>

<span data-ttu-id="3f542-105">La gestion des licences basée sur les groupes attribue ou supprime automatiquement les licences d’un compte d’utilisateur en fonction de l’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="3f542-105">Group-based licensing automatically assigns or removes licenses for a user account based on group membership.</span></span> <span data-ttu-id="3f542-106">L’appartenance à un groupe dynamique ajoute ou supprime des membres à un groupe en fonction des propriétés du compte d’utilisateur, telles que **Département** ou **Pays.**</span><span class="sxs-lookup"><span data-stu-id="3f542-106">Dynamic group membership adds or removes members to a group based on user account properties, such as **Department** or **Country**.</span></span> <span data-ttu-id="3f542-107">Cet article vous décrit les démonstrations d’ajout et de suppression de membres de groupe dans votre environnement de test Microsoft 365 pour entreprise.</span><span class="sxs-lookup"><span data-stu-id="3f542-107">This article steps you through demonstrations of both adding and removing group members in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="3f542-108">La configuration de la licence automatique et de l’appartenance à un groupe dynamique dans votre environnement de test Microsoft 365 pour entreprise implique deux phases :</span><span class="sxs-lookup"><span data-stu-id="3f542-108">Setting up auto-licensing and dynamic group membership in your Microsoft 365 for enterprise test environment involves two phases:</span></span>

- [<span data-ttu-id="3f542-109">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="3f542-109">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="3f542-110">Phase 2 : Configurer et tester l’appartenance à un groupe dynamique et la gestion automatique des licences</span><span class="sxs-lookup"><span data-stu-id="3f542-110">Phase 2: Configure and test dynamic group membership and automatic licensing</span></span>](#phase-2-configure-and-test-dynamic-group-membership-and-automatic-licensing)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="3f542-112">Pour obtenir une carte visuelle de tous les articles de la pile du Guide de laboratoire de test Microsoft 365 pour entreprise, allez à [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="3f542-112">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="3f542-113">Phase 1 : Créer votre environnement de test Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="3f542-113">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="3f542-114">Si vous souhaitez uniquement tester les licences automatisées et l’appartenance à un groupe de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="3f542-114">If you want to only test automated licensing and group membership in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="3f542-115">Si vous souhaitez tester la gestion automatisée des licences et l’appartenance à un groupe dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="3f542-115">If you want to test automated licensing and group membership in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="3f542-116">Le test de la gestion automatisée des licences et de l’appartenance à un groupe ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt AD DS (Active Directory Domain Services).</span><span class="sxs-lookup"><span data-stu-id="3f542-116">Testing automated licensing and group membership doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="3f542-117">Il est fourni ici en tant qu’option afin que vous pouvez tester la gestion automatisée des licences et l’appartenance à un groupe et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="3f542-117">It's provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span>
  
## <a name="phase-2-configure-and-test-dynamic-group-membership-and-automatic-licensing"></a><span data-ttu-id="3f542-118">Phase 2 : Configurer et tester l’appartenance à un groupe dynamique et la gestion automatique des licences</span><span class="sxs-lookup"><span data-stu-id="3f542-118">Phase 2: Configure and test dynamic group membership and automatic licensing</span></span>

<span data-ttu-id="3f542-119">Tout d’abord, créez un groupe nommé Ventes, puis ajoutez  une  règle d’appartenance au groupe dynamique afin que les comptes d’utilisateurs dont le service est le service des ventes rejoignent automatiquement le groupe Ventes.</span><span class="sxs-lookup"><span data-stu-id="3f542-119">First, create a new group named Sales, and add a dynamic group membership rule so that user accounts with the **Department** set to **Sales** automatically join the Sales group.</span></span>

1. <span data-ttu-id="3f542-120">Dans une instance privée de votre navigateur Internet, connectez-vous au Centre d’administration [Microsoft 365](https://admin.microsoft.com) avec le compte d’administrateur général de votre abonnement de laboratoire de test Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="3f542-120">In a private instance of your internet browser, sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with the global administrator account of your Microsoft 365 E5 test lab subscription.</span></span>
2. <span data-ttu-id="3f542-121">Sous un onglet distinct de votre navigateur, allez sur le portail Azure à [https://portal.azure.com](https://portal.azure.com) l':.</span><span class="sxs-lookup"><span data-stu-id="3f542-121">On a separate tab of your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>
3. <span data-ttu-id="3f542-122">Dans le portail Azure, entrez **des groupes** dans la zone de recherche, puis sélectionnez **Groupes.**</span><span class="sxs-lookup"><span data-stu-id="3f542-122">In the Azure portal, enter **groups** in the search box, and then select **Groups**.</span></span>
4. <span data-ttu-id="3f542-123">dans le **volet Tous les groupes,** sélectionnez **Nouveau groupe.**</span><span class="sxs-lookup"><span data-stu-id="3f542-123">in the **All groups** pane, select **New group**.</span></span>
5. <span data-ttu-id="3f542-124">Dans **le type de** groupe, **sélectionnez Microsoft 365**.</span><span class="sxs-lookup"><span data-stu-id="3f542-124">In **Group type**, select **Microsoft 365**.</span></span>
6. <span data-ttu-id="3f542-125">Dans **le nom du groupe,** entrez **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="3f542-125">In **Group name**, enter **Sales**.</span></span>
7. <span data-ttu-id="3f542-126">Dans **le type d’appartenance,** **sélectionnez Utilisateur dynamique.**</span><span class="sxs-lookup"><span data-stu-id="3f542-126">In **Membership type**, select **Dynamic user**.</span></span>
8. <span data-ttu-id="3f542-127">Sélectionnez **Membres utilisateur dynamiques.**</span><span class="sxs-lookup"><span data-stu-id="3f542-127">Select **Dynamic user members**.</span></span>
9. <span data-ttu-id="3f542-128">Dans le **volet Règles d’appartenance** dynamique :</span><span class="sxs-lookup"><span data-stu-id="3f542-128">In the **Dynamic membership rules** pane:</span></span> 
   - <span data-ttu-id="3f542-129">Sélectionnez la **propriété de** service.</span><span class="sxs-lookup"><span data-stu-id="3f542-129">Select the **department** property.</span></span>
   - <span data-ttu-id="3f542-130">Sélectionnez **l’opérateur Égal à.**</span><span class="sxs-lookup"><span data-stu-id="3f542-130">Select the **Equals** operator.</span></span>
   - <span data-ttu-id="3f542-131">Dans la **zone Valeur,** entrez **Ventes**.</span><span class="sxs-lookup"><span data-stu-id="3f542-131">In the **Value** box, enter **Sales**.</span></span>
10. <span data-ttu-id="3f542-132">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3f542-132">Select **Save**.</span></span>
11. <span data-ttu-id="3f542-133">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="3f542-133">Select **Create**.</span></span>

<span data-ttu-id="3f542-134">Ensuite, configurez le groupe Ventes afin que la licence Microsoft 365 E5 soit automatiquement attribuée aux membres.</span><span class="sxs-lookup"><span data-stu-id="3f542-134">Next, configure the Sales group so that members are automatically assigned the Microsoft 365 E5 license.</span></span>

1. <span data-ttu-id="3f542-135">Sélectionnez **le groupe** Ventes, puis les **licences.**</span><span class="sxs-lookup"><span data-stu-id="3f542-135">Select the **Sales** group, and then select **Licenses**.</span></span>
2. <span data-ttu-id="3f542-136">Dans le **volet Mettre à jour les attributions de** licence, **sélectionnez Microsoft 365 E5,** puis sélectionnez **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3f542-136">In the **Update license assignments** pane, select **Microsoft 365 E5**, and then select **Save**.</span></span>
3. <span data-ttu-id="3f542-137">Dans votre navigateur, fermez l’onglet du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="3f542-137">In your browser, close the Azure portal tab.</span></span>

<span data-ttu-id="3f542-138">Ensuite, testez l’appartenance au groupe dynamique et la gestion automatique des licences sur le compte Utilisateur 4 :</span><span class="sxs-lookup"><span data-stu-id="3f542-138">Next, test dynamic group membership and automatic licensing on the User 4 account:</span></span>

1. <span data-ttu-id="3f542-139">Dans **l’Microsoft Office Accueil** de votre navigateur, sélectionnez **Administrateur.**</span><span class="sxs-lookup"><span data-stu-id="3f542-139">From the **Microsoft Office Home** tab in your browser, select **Admin**.</span></span>
2. <span data-ttu-id="3f542-140">Sous l’onglet Centre d’administration **Microsoft 365,** sélectionnez **Utilisateurs actifs.**</span><span class="sxs-lookup"><span data-stu-id="3f542-140">From the **Microsoft 365 admin center** tab, select **Active users**.</span></span>
3. <span data-ttu-id="3f542-141">Dans la page **Utilisateurs** actifs, sélectionnez **le compte Utilisateur 4.**</span><span class="sxs-lookup"><span data-stu-id="3f542-141">On the **Active users** page, select the **User 4** account.</span></span>
4. <span data-ttu-id="3f542-142">Dans le **volet Utilisateur 4,** **sélectionnez Modifier pour** les **licences de produit.**</span><span class="sxs-lookup"><span data-stu-id="3f542-142">On the **User 4** pane, select **Edit** for **Product licenses**.</span></span>
5. <span data-ttu-id="3f542-143">Dans le **volet Licences de** produits, désactivez la licence **Microsoft 365 E5,** puis **sélectionnez Enregistrer** la  >  **fermeture.**</span><span class="sxs-lookup"><span data-stu-id="3f542-143">On the **Product licenses** pane, disable the **Microsoft 365 E5** license, and then select **Save** > **Close**.</span></span>
6. <span data-ttu-id="3f542-144">Dans les propriétés du compte Utilisateur 4, vérifiez qu’aucune licence de produit n’a été attribuée et qu’il n’y a pas d’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="3f542-144">In the properties of the User 4 account, verify that no product licenses have been assigned and there are no group memberships.</span></span>
7. <span data-ttu-id="3f542-145">Pour **plus d’informations sur** le contact, **sélectionnez Modifier.**</span><span class="sxs-lookup"><span data-stu-id="3f542-145">For **Contact information**, select **Edit**.</span></span>
8. <span data-ttu-id="3f542-146">Dans le **volet Modifier les informations de contact,** sélectionnez **Coordonnées.**</span><span class="sxs-lookup"><span data-stu-id="3f542-146">In the **Edit Contact information** pane, select **Contact information**.</span></span>
9. <span data-ttu-id="3f542-147">Dans la **zone Service,** entrez **Ventes,** puis **sélectionnez Enregistrer**  >  **la fermeture.**</span><span class="sxs-lookup"><span data-stu-id="3f542-147">In the **Department** box, enter **Sales**, and then select **Save** > **Close**.</span></span>
10. <span data-ttu-id="3f542-148">Patientez quelques minutes, puis sélectionnez périodiquement l’icône Actualiser dans le coin supérieur droit du volet du compte Utilisateur 4. </span><span class="sxs-lookup"><span data-stu-id="3f542-148">Wait a few minutes, and then periodically select the **Refresh** icon in the upper-right of the User 4 account pane.</span></span>

<span data-ttu-id="3f542-149">Dans le temps, vous devriez voir les :</span><span class="sxs-lookup"><span data-stu-id="3f542-149">In time, you should see the:</span></span>

- <span data-ttu-id="3f542-150">**Propriété d’appartenance au** groupe mise à jour avec **le groupe** Ventes.</span><span class="sxs-lookup"><span data-stu-id="3f542-150">**Group memberships** property updated with the **Sales** group.</span></span>
- <span data-ttu-id="3f542-151">**Propriété des licences de** produit mise à jour avec **la licence Microsoft 365 E5.**</span><span class="sxs-lookup"><span data-stu-id="3f542-151">**Product licenses** property updated with the **Microsoft 365 E5** license.</span></span>

<span data-ttu-id="3f542-152">Consultez les articles suivants pour déployer l’appartenance à un groupe dynamique et la gestion automatique des licences en production :</span><span class="sxs-lookup"><span data-stu-id="3f542-152">See these articles to deploy dynamic group membership and automatic licensing in production:</span></span>

- [<span data-ttu-id="3f542-153">Gestion des licences basée sur les groupes dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f542-153">Group-based licensing in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal)
- [<span data-ttu-id="3f542-154">Groupes dynamiques dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3f542-154">Dynamic groups in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule)

## <a name="next-step"></a><span data-ttu-id="3f542-155">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3f542-155">Next step</span></span>

<span data-ttu-id="3f542-156">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="3f542-156">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f542-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f542-157">See also</span></span>

[<span data-ttu-id="3f542-158">Feuille de route des identités</span><span class="sxs-lookup"><span data-stu-id="3f542-158">Identity roadmap</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="3f542-159">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="3f542-159">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="3f542-160">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="3f542-160">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="3f542-161">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3f542-161">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
