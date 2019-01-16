---
title: Automatiser l’appartenance de groupe et de licence pour votre environnement de test Microsoft 365 pour entreprises
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
description: Configurer basée sur le groupe gestion des licences et l’appartenance au groupe dynamique dans votre environnement de test Microsoft 365 pour entreprises.
ms.openlocfilehash: 45a78af202f2d9ab029683aae4d95ed9a3370b08
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867227"
---
# <a name="automate-licensing-and-group-membership-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="9f258-103">Automatiser l’appartenance de groupe et de licence pour votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="9f258-103">Automate licensing and group membership for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="9f258-p101">Basée sur le groupe gestion des licences automatiquement assigne ou supprime des licences pour un compte d’utilisateur en fonction de l’appartenance au groupe. L’appartenance au groupe dynamique ajoute ou supprime des membres à un groupe en fonction de propriétés de compte d’utilisateur, telles que le service ou un pays. Cet article vous guide tout au long une démonstration des deux dans votre environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="9f258-p101">Group-based licensing automatically assigns or removes licenses for a user account based on group membership. Dynamic group membership adds or removes members to a group based on user account properties, such as Department or Country. This article steps you through a demonstration of both in your Microsoft 365 Enterprise test environment.</span></span>

<span data-ttu-id="9f258-107">Il existe deux phases à définir l’appartenance à un groupe de licences automatique et dynamique dans votre environnement de test Microsoft 365 pour entreprises :</span><span class="sxs-lookup"><span data-stu-id="9f258-107">There are two phases to setting up auto-licensing and dynamic group membership in your Microsoft 365 Enterprise test environment:</span></span>

1. <span data-ttu-id="9f258-108">Créer l’environnement de test Microsoft 365 pour entreprises.</span><span class="sxs-lookup"><span data-stu-id="9f258-108">Create the Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="9f258-109">Configurer et tester l’appartenance au groupe dynamique et la gestion des licences automatique.</span><span class="sxs-lookup"><span data-stu-id="9f258-109">Configure and test dynamic group membership and automatic licensing.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="9f258-111">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="9f258-111">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="9f258-112">Phase 1 : Création de votre environnement de test Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="9f258-112">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="9f258-113">Si vous souhaitez uniquement tester les licences automatisé et l’appartenance au groupe de manière léger avec la configuration minimale requise, suivez les instructions de [configuration de base léger](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="9f258-113">If you just want to test automated licensing and group membership in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="9f258-114">Si vous souhaitez tester les licences automatisé et l’appartenance au groupe dans une entreprise simulée, suivez les instructions de [l’authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9f258-114">If you want to test automated licensing and group membership in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f258-p102">Test automatisé de gestion des licences et l’appartenance au groupe ne nécessite pas de l’environnement de test simulé entreprise, qui comprend un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt Windows Server Active Directory. Il est fourni ici en tant qu’option afin que vous puissiez licences automatisé et l’appartenance au groupe de test et tester dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="9f258-p102">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Windows Server AD forest. It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-and-test-dynamic-group-membership-and-automatic-licensing"></a><span data-ttu-id="9f258-117">Phase 2 : Configurer et tester l’appartenance au groupe dynamique et la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="9f258-117">Phase 2: Configure and test dynamic group membership and automatic licensing</span></span>

<span data-ttu-id="9f258-118">Tout d’abord, vous créez un nouveau groupe de ventes et ajoutez une règle d’appartenance au groupe dynamique afin que les comptes d’utilisateurs avec le service des ventes la valeur sont automatiquement ajoutés au groupe de ventes.</span><span class="sxs-lookup"><span data-stu-id="9f258-118">First, you create a new Sales group and add a dynamic group membership rule so that user accounts with the Department set to Sales are automatically added to the Sales group.</span></span>

1. <span data-ttu-id="9f258-119">À l’aide d’une instance privée de votre navigateur Internet, connectez-vous au portail Office à [https://office.com](https://office.com) avec le compte d’administrateur global de votre abonnement d’évaluation Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9f258-119">Using a private instance of your Internet browser, sign in to the Office portal at [https://office.com](https://office.com) with the global administrator account of your Office 365 E5 trial subscription.</span></span>
2. <span data-ttu-id="9f258-120">Sur un onglet séparé de votre navigateur, accédez au portail Azure à [https://portal.azure.com](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9f258-120">On a separate tab of your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>
3. <span data-ttu-id="9f258-121">Dans le portail Azure, cliquez sur **Azure Active Directory > Utilisateurs et groupes > Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="9f258-121">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>
4. <span data-ttu-id="9f258-122">Sur le serveur lame **tous les groupes** , cliquez sur **Nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="9f258-122">On the **All groups** blade, click **New group**.</span></span>
5. <span data-ttu-id="9f258-123">Dans **type de groupe**, sélectionnez **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="9f258-123">In **Group type**, select **Office 365**.</span></span>
6. <span data-ttu-id="9f258-124">Dans **nom du groupe**, tapez **ventes**.</span><span class="sxs-lookup"><span data-stu-id="9f258-124">In **Group name**, type **Sales**.</span></span>
7. <span data-ttu-id="9f258-125">Dans **type d’appartenance**, sélectionnez **utilisateur dynamique** .</span><span class="sxs-lookup"><span data-stu-id="9f258-125">In **Membership type**, select **Dynamic user** .</span></span>
8. <span data-ttu-id="9f258-126">Cliquez sur **Ajouter une requête dynamique**.</span><span class="sxs-lookup"><span data-stu-id="9f258-126">Click **Add dynamic query**.</span></span>
9. <span data-ttu-id="9f258-127">Dans **Ajouter des utilisateurs où**, sélectionnez **Service**.</span><span class="sxs-lookup"><span data-stu-id="9f258-127">In **Add users where**, select **department**.</span></span>
10. <span data-ttu-id="9f258-128">Dans le champ suivant, sélectionnez **Est égal à**.</span><span class="sxs-lookup"><span data-stu-id="9f258-128">In the next field, select **Equals**.</span></span>
11. <span data-ttu-id="9f258-129">Dans le champ suivant, tapez **ventes**.</span><span class="sxs-lookup"><span data-stu-id="9f258-129">In the next field, type **Sales**.</span></span>
12. <span data-ttu-id="9f258-130">Cliquez sur **Ajouter une requête**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="9f258-130">Click **Add query**, and then click **Create**.</span></span>
13. <span data-ttu-id="9f258-131">Fermez les cartes de **groupe** et les **groupes de groupes** .</span><span class="sxs-lookup"><span data-stu-id="9f258-131">Close the **Group** and **Groups-All groups** blades.</span></span>

<span data-ttu-id="9f258-132">Ensuite, vous configurez le groupe de ventes afin que les membres sont affectés automatiquement Office 365 E5 et mobilité d’entreprise + licences E5 de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="9f258-132">Next, you configure the Sales group so that members are automatically assigned Office 365 E5 and Enterprise Mobility + Security E5 licenses.</span></span>

1. <span data-ttu-id="9f258-133">Dans la **vue d’ensemble** lame pour Azure Active Directory, cliquez sur **licences > tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="9f258-133">On the **Overview** blade for Azure Active Directory, click **Licenses > All products**.</span></span>
2. <span data-ttu-id="9f258-134">Dans la liste, sélectionnez **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5**, puis cliquez sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="9f258-134">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **Assign**.</span></span>
3. <span data-ttu-id="9f258-135">Sur le serveur lame **attribuer des licences** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="9f258-135">On the **Assign license** blade, click **Users and groups**.</span></span>
4. <span data-ttu-id="9f258-136">Dans la liste des groupes, sélectionnez le groupe de **ventes** .</span><span class="sxs-lookup"><span data-stu-id="9f258-136">In the list of groups, select the **Sales** group.</span></span>
5. <span data-ttu-id="9f258-137">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="9f258-137">Click **Select**, and then click **Assign**.</span></span>
6. <span data-ttu-id="9f258-138">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9f258-138">Close the Azure portal tab in your browser.</span></span>

<span data-ttu-id="9f258-139">Ensuite, vous testez l’appartenance au groupe dynamique et la gestion des licences automatique sur le compte d’utilisateur 4.</span><span class="sxs-lookup"><span data-stu-id="9f258-139">Next, you test dynamic group membership and automatic licensing on the User 4 account.</span></span> 

1. <span data-ttu-id="9f258-140">Sous l’onglet **Accueil de Microsoft Office** dans votre navigateur, cliquez sur **Admin**.</span><span class="sxs-lookup"><span data-stu-id="9f258-140">From the **Microsoft Office Home** tab in your browser, click **Admin**.</span></span>
2. <span data-ttu-id="9f258-141">Sous l’onglet **Centre d’administration d’Office** , cliquez sur **utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="9f258-141">From the **Office Admin center** tab, click **Active users**.</span></span>
3. <span data-ttu-id="9f258-142">Dans la page **utilisateurs actifs** , cliquez sur le compte **d’utilisateur 4** .</span><span class="sxs-lookup"><span data-stu-id="9f258-142">On the **Active users** page, click the **User 4** account.</span></span>
4. <span data-ttu-id="9f258-143">Dans le volet **4 de l’utilisateur** , cliquez sur **Modifier** pour les **licences de produit**.</span><span class="sxs-lookup"><span data-stu-id="9f258-143">On the **User 4** pane, click **Edit** for **Product licenses**.</span></span>
5. <span data-ttu-id="9f258-144">Dans le volet de **licences de produits** , activer la **mobilité d’entreprise + sécurité E5** et licences **Office 365 entreprise E5** désactivé, puis cliquez sur **Enregistrer > Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9f258-144">On the **Product licenses** pane, turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses off, and then click **Save > Close**.</span></span>
6. <span data-ttu-id="9f258-145">Dans les propriétés du compte d’utilisateur 4, vérifiez qu’aucune licence de produit n’ont été attribués et qu’il n’existe aucun appartenances aux groupes.</span><span class="sxs-lookup"><span data-stu-id="9f258-145">In the properties of the User 4 account, verify that no product licenses have been assigned and there are no group memberships.</span></span>
7. <span data-ttu-id="9f258-146">Pour plus **d’informations de Contact**, cliquez sur **Modifier** .</span><span class="sxs-lookup"><span data-stu-id="9f258-146">Click **Edit** for **Contact information**.</span></span>
8. <span data-ttu-id="9f258-147">Dans le volet **Modifier le Contact** , cliquez sur **informations de Contact**.</span><span class="sxs-lookup"><span data-stu-id="9f258-147">In the **Edit Contact information** pane, click **Contact information**.</span></span>
9. <span data-ttu-id="9f258-148">Dans le champ **département** , tapez **ventes**, puis cliquez sur **Enregistrer > Fermer**.</span><span class="sxs-lookup"><span data-stu-id="9f258-148">In the **Department** field, type **Sales**, and then click **Save > Close**.</span></span>
10. <span data-ttu-id="9f258-149">Patientez quelques minutes, puis cliquez périodiquement sur l’icône Actualiser dans l’angle supérieur droit du volet de compte d’utilisateur 4.</span><span class="sxs-lookup"><span data-stu-id="9f258-149">Wait a few minutes, and then periodically click the refresh icon in the upper-right of the User 4 account pane.</span></span> 

<span data-ttu-id="9f258-150">Dans le temps, vous devez voir les :</span><span class="sxs-lookup"><span data-stu-id="9f258-150">In time you should see the:</span></span>

- <span data-ttu-id="9f258-151">Propriété **appartenances de groupe** mis à jour avec le groupe de **ventes** .</span><span class="sxs-lookup"><span data-stu-id="9f258-151">**Group memberships** property updated with the **Sales** group.</span></span>
- <span data-ttu-id="9f258-152">Propriété **licences des produits** mis à jour avec les licences de **mobilité d’entreprise + sécurité E5** et **Office 365 entreprise E5** .</span><span class="sxs-lookup"><span data-stu-id="9f258-152">**Product licenses** property updated with the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses.</span></span>

<span data-ttu-id="9f258-153">Dans la phase d’identité pour des informations et des liens pour déployer l’appartenance au groupe dynamique et la gestion des licences automatique en production, consultez la rubrique comme suit :</span><span class="sxs-lookup"><span data-stu-id="9f258-153">See these steps in the Identity phase for information and links to deploy dynamic group membership and automatic licensing in production:</span></span>

- [<span data-ttu-id="9f258-154">Configurez la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="9f258-154">Set up automatic licensing</span></span>](identity-group-based-licensing.md)
- [<span data-ttu-id="9f258-155">Configurez l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="9f258-155">Set up dynamic group membership</span></span>](identity-automatic-group-membership.md)

## <a name="next-step"></a><span data-ttu-id="9f258-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9f258-156">Next step</span></span>

<span data-ttu-id="9f258-157">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="9f258-157">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f258-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f258-158">See also</span></span>

[<span data-ttu-id="9f258-159">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="9f258-159">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="9f258-160">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9f258-160">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="9f258-161">Déploiement de Microsoft 365 pour entreprises</span><span class="sxs-lookup"><span data-stu-id="9f258-161">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="9f258-162">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9f258-162">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
