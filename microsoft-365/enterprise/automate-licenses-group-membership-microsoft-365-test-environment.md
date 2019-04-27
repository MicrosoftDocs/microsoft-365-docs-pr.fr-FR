---
title: Automatiser les licences et l'appartenance aux groupes pour votre environnement de test Microsoft 365 Enterprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-identity-device-management
ms.custom:
- TLG
- Ent_TLGs
description: ConFigurez la gestion des licences basée sur un groupe et l'appartenance à un groupe dynamique dans votre environnement de test Microsoft 365 Enterprise.
ms.openlocfilehash: 4ee929b345469d9cab05968a4a4c7f7399635b32
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2019
ms.locfileid: "33353076"
---
# <a name="automate-licensing-and-group-membership-for-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="9581d-103">Automatiser les licences et l'appartenance aux groupes pour votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="9581d-103">Automate licensing and group membership for your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="9581d-104">Les licences basées sur des groupes attribuent ou suppriment automatiquement des licences pour un compte d'utilisateur en fonction de l'appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="9581d-104">Group-based licensing automatically assigns or removes licenses for a user account based on group membership.</span></span> <span data-ttu-id="9581d-105">L'appartenance à un groupe dynamique ajoute ou supprime des membres d'un groupe en fonction des propriétés du compte d'utilisateur, telles que service ou pays.</span><span class="sxs-lookup"><span data-stu-id="9581d-105">Dynamic group membership adds or removes members to a group based on user account properties, such as Department or Country.</span></span> <span data-ttu-id="9581d-106">Cet article décrit les deux dans votre environnement de test Microsoft 365 Enterprise.</span><span class="sxs-lookup"><span data-stu-id="9581d-106">This article steps you through a demonstration of both in your Microsoft 365 Enterprise test environment.</span></span>

<span data-ttu-id="9581d-107">Il existe deux phases de configuration de la gestion des licences automatiques et de l'appartenance à un groupe dynamique dans votre environnement de test Microsoft 365 entreprise:</span><span class="sxs-lookup"><span data-stu-id="9581d-107">There are two phases to setting up auto-licensing and dynamic group membership in your Microsoft 365 Enterprise test environment:</span></span>

1. <span data-ttu-id="9581d-108">Créer l’environnement de test Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="9581d-108">Create the Microsoft 365 Enterprise test environment.</span></span>
2. <span data-ttu-id="9581d-109">ConFigurez et testez l'appartenance au groupe dynamique et les licences automatiques.</span><span class="sxs-lookup"><span data-stu-id="9581d-109">Configure and test dynamic group membership and automatic licensing.</span></span>

![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png) 
    
> [!TIP]
> <span data-ttu-id="9581d-111">Cliquez [ici](https://aka.ms/m365etlgstack) pour afficher le plan de tous les articles de l’ensemble de guides de laboratoire de test de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="9581d-111">Click [here](https://aka.ms/m365etlgstack) for a visual map to all the articles in the Microsoft 365 Enterprise Test Lab Guide stack.</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-enterprise-test-environment"></a><span data-ttu-id="9581d-112">Phase 1: créer votre environnement de test Microsoft 365 Enterprise</span><span class="sxs-lookup"><span data-stu-id="9581d-112">Phase 1: Build out your Microsoft 365 Enterprise test environment</span></span>

<span data-ttu-id="9581d-113">Si vous souhaitez simplement tester les licences automatisées et l'appartenance au groupe de façon légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="9581d-113">If you just want to test automated licensing and group membership in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="9581d-114">Si vous souhaitez tester les licences automatisées et l'appartenance aux groupes dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9581d-114">If you want to test automated licensing and group membership in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9581d-115">Le test des licences automatisées et l'appartenance aux groupes ne nécessitent pas l'environnement de test d'entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d'annuaires pour une forêt des services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="9581d-115">Testing automated licensing and group membership does not require the simulated enterprise test environment, which includes a simulated intranet connected to the Internet and directory synchronization for a Active Directory Domain Services (AD DS) forest.</span></span> <span data-ttu-id="9581d-116">Elle est fournie ici en tant qu'option pour vous permettre de tester les licences automatiques et les appartenances aux groupes et de les tester dans un environnement qui représente une organisation typique.</span><span class="sxs-lookup"><span data-stu-id="9581d-116">It is provided here as an option so that you can test automated licensing and group membership and experiment with it in an environment that represents a typical organization.</span></span> 
  
## <a name="phase-2-configure-and-test-dynamic-group-membership-and-automatic-licensing"></a><span data-ttu-id="9581d-117">Phase 2: configurer et tester l'appartenance au groupe dynamique et les licences automatiques</span><span class="sxs-lookup"><span data-stu-id="9581d-117">Phase 2: Configure and test dynamic group membership and automatic licensing</span></span>

<span data-ttu-id="9581d-118">Tout d'abord, vous créez un nouveau groupe de ventes et ajoutez une règle d'appartenance au groupe dynamique de sorte que les comptes d'utilisateur dont le service est défini sur ventes soient automatiquement ajoutés au groupe ventes.</span><span class="sxs-lookup"><span data-stu-id="9581d-118">First, you create a new Sales group and add a dynamic group membership rule so that user accounts with the Department set to Sales are automatically added to the Sales group.</span></span>

1. <span data-ttu-id="9581d-119">À l'aide d'une instance privée de votre navigateur Internet, connectez-vous au portail [https://portal.office.com](https://portal.office.com) Office 365 à l'aide du compte d'administrateur général de votre abonnement de laboratoire de test Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="9581d-119">Using a private instance of your Internet browser, sign in to the Office 365 portal at [https://portal.office.com](https://portal.office.com) with the global administrator account of your Office 365 E5 test lab subscription.</span></span>
2. <span data-ttu-id="9581d-120">Dans un onglet distinct de votre navigateur, accédez au portail Azure à l' [https://portal.azure.com](https://portal.azure.com)adresse.</span><span class="sxs-lookup"><span data-stu-id="9581d-120">On a separate tab of your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com).</span></span>
3. <span data-ttu-id="9581d-121">Dans le portail Azure, cliquez sur **Azure Active Directory > Utilisateurs et groupes > Tous les groupes**.</span><span class="sxs-lookup"><span data-stu-id="9581d-121">In the Azure portal, click **Azure Active Directory > Users and groups > All groups**.</span></span>
4. <span data-ttu-id="9581d-122">Dans le panneau **tous les groupes** , cliquez sur **nouveau groupe**.</span><span class="sxs-lookup"><span data-stu-id="9581d-122">On the **All groups** blade, click **New group**.</span></span>
5. <span data-ttu-id="9581d-123">Dans **type de groupe**, sélectionnez **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="9581d-123">In **Group type**, select **Office 365**.</span></span>
6. <span data-ttu-id="9581d-124">Dans **nom du groupe**, tapez **ventes**.</span><span class="sxs-lookup"><span data-stu-id="9581d-124">In **Group name**, type **Sales**.</span></span>
7. <span data-ttu-id="9581d-125">Dans **type d'appartenance**, sélectionnez **utilisateur dynamique** .</span><span class="sxs-lookup"><span data-stu-id="9581d-125">In **Membership type**, select **Dynamic user** .</span></span>
8. <span data-ttu-id="9581d-126">Cliquez sur **Ajouter une requête dynamique**.</span><span class="sxs-lookup"><span data-stu-id="9581d-126">Click **Add dynamic query**.</span></span>
9. <span data-ttu-id="9581d-127">Dans **Ajouter des utilisateurs où**, sélectionnez **Service**.</span><span class="sxs-lookup"><span data-stu-id="9581d-127">In **Add users where**, select **department**.</span></span>
10. <span data-ttu-id="9581d-128">Dans le champ suivant, sélectionnez **Est égal à**.</span><span class="sxs-lookup"><span data-stu-id="9581d-128">In the next field, select **Equals**.</span></span>
11. <span data-ttu-id="9581d-129">Dans le champ suivant, tapez **ventes**.</span><span class="sxs-lookup"><span data-stu-id="9581d-129">In the next field, type **Sales**.</span></span>
12. <span data-ttu-id="9581d-130">Cliquez sur **Ajouter une requête**, puis cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="9581d-130">Click **Add query**, and then click **Create**.</span></span>
13. <span data-ttu-id="9581d-131">Fermez le **groupe** et **les groupes-toutes les Blades de groupes** .</span><span class="sxs-lookup"><span data-stu-id="9581d-131">Close the **Group** and **Groups-All groups** blades.</span></span>

<span data-ttu-id="9581d-132">Ensuite, configurez le groupe ventes de sorte que les membres reçoivent automatiquement les licences Office 365 E5 et Enterprise Mobility + Security E5 affectées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9581d-132">Next, you configure the Sales group so that members are automatically assigned Office 365 E5 and Enterprise Mobility + Security E5 licenses.</span></span>

1. <span data-ttu-id="9581d-133">Dans le panneau de **vue d'ensemble** pour Azure Active Directory, cliquez sur **licences > tous les produits**.</span><span class="sxs-lookup"><span data-stu-id="9581d-133">On the **Overview** blade for Azure Active Directory, click **Licenses > All products**.</span></span>
2. <span data-ttu-id="9581d-134">Dans la liste, sélectionnez **Enterprise Mobility + Security E5** et **Office 365 Entreprise E5**, puis cliquez sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="9581d-134">In the list, select **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5**, and then click **Assign**.</span></span>
3. <span data-ttu-id="9581d-135">Sur le panneau **attribuer une licence** , cliquez sur **utilisateurs et groupes**.</span><span class="sxs-lookup"><span data-stu-id="9581d-135">On the **Assign license** blade, click **Users and groups**.</span></span>
4. <span data-ttu-id="9581d-136">Dans la liste des groupes, sélectionnez le groupe **ventes** .</span><span class="sxs-lookup"><span data-stu-id="9581d-136">In the list of groups, select the **Sales** group.</span></span>
5. <span data-ttu-id="9581d-137">Cliquez sur **Sélectionner**, puis sur **Affecter**.</span><span class="sxs-lookup"><span data-stu-id="9581d-137">Click **Select**, and then click **Assign**.</span></span>
6. <span data-ttu-id="9581d-138">Fermez l’onglet du portail Azure dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9581d-138">Close the Azure portal tab in your browser.</span></span>

<span data-ttu-id="9581d-139">Ensuite, testez l'appartenance au groupe dynamique et les licences automatiques sur le compte utilisateur 4.</span><span class="sxs-lookup"><span data-stu-id="9581d-139">Next, you test dynamic group membership and automatic licensing on the User 4 account.</span></span> 

1. <span data-ttu-id="9581d-140">Dans l'onglet **Accueil Microsoft Office** de votre navigateur, cliquez sur **administrateur**.</span><span class="sxs-lookup"><span data-stu-id="9581d-140">From the **Microsoft Office Home** tab in your browser, click **Admin**.</span></span>
2. <span data-ttu-id="9581d-141">À partir de l'onglet **Centre d'administration 365 de Microsoft** , cliquez sur **utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="9581d-141">From the **Microsoft 365 admin center** tab, click **Active users**.</span></span>
3. <span data-ttu-id="9581d-142">Sur la page **utilisateurs actifs** , cliquez sur le compte **utilisateur 4** .</span><span class="sxs-lookup"><span data-stu-id="9581d-142">On the **Active users** page, click the **User 4** account.</span></span>
4. <span data-ttu-id="9581d-143">Dans le volet **utilisateur 4** , cliquez sur **modifier** pour **licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="9581d-143">On the **User 4** pane, click **Edit** for **Product licenses**.</span></span>
5. <span data-ttu-id="9581d-144">Dans le **volet licences de produits** , désactivez les licences **Enterprise Mobility + Security e5** et **Office 365 entreprise E5** , puis cliquez sur **Enregistrer > fermer**.</span><span class="sxs-lookup"><span data-stu-id="9581d-144">On the **Product licenses** pane, turn the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses off, and then click **Save > Close**.</span></span>
6. <span data-ttu-id="9581d-145">Dans les propriétés du compte utilisateur 4, vérifiez qu'aucune licence de produit n'a été affectée et qu'il n'y a pas d'appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="9581d-145">In the properties of the User 4 account, verify that no product licenses have been assigned and there are no group memberships.</span></span>
7. <span data-ttu-id="9581d-146">Cliquez sur **modifier** pour obtenir des **informations de contact**.</span><span class="sxs-lookup"><span data-stu-id="9581d-146">Click **Edit** for **Contact information**.</span></span>
8. <span data-ttu-id="9581d-147">Dans le volet **modifier les informations de contact** , cliquez sur informations sur le **contact**.</span><span class="sxs-lookup"><span data-stu-id="9581d-147">In the **Edit Contact information** pane, click **Contact information**.</span></span>
9. <span data-ttu-id="9581d-148">Dans le champ **service** , tapez **ventes**, puis cliquez sur **Enregistrer > fermer**.</span><span class="sxs-lookup"><span data-stu-id="9581d-148">In the **Department** field, type **Sales**, and then click **Save > Close**.</span></span>
10. <span data-ttu-id="9581d-149">Patientez quelques minutes, puis cliquez régulièrement sur l'icône Actualiser dans le coin supérieur droit du volet compte utilisateur 4.</span><span class="sxs-lookup"><span data-stu-id="9581d-149">Wait a few minutes, and then periodically click the refresh icon in the upper-right of the User 4 account pane.</span></span> 

<span data-ttu-id="9581d-150">À temps, vous devriez voir les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9581d-150">In time you should see the:</span></span>

- <span data-ttu-id="9581d-151">Propriété d' **appartenance au groupe** mise à jour avec le groupe **ventes** .</span><span class="sxs-lookup"><span data-stu-id="9581d-151">**Group memberships** property updated with the **Sales** group.</span></span>
- <span data-ttu-id="9581d-152">Propriété de **licences de produit** mise à jour avec les licences **Enterprise Mobility + Security e5** et **Office 365 entreprise E5** .</span><span class="sxs-lookup"><span data-stu-id="9581d-152">**Product licenses** property updated with the **Enterprise Mobility + Security E5** and **Office 365 Enterprise E5** licenses.</span></span>

<span data-ttu-id="9581d-153">Consultez ces étapes dans la phase d'identité pour obtenir des informations et des liens sur le déploiement de l'appartenance au groupe dynamique et des licences automatiques en production:</span><span class="sxs-lookup"><span data-stu-id="9581d-153">See these steps in the Identity phase for information and links to deploy dynamic group membership and automatic licensing in production:</span></span>

- [<span data-ttu-id="9581d-154">Configurez la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="9581d-154">Set up automatic licensing</span></span>](identity-self-service-group-management.md#identity-group-license)
- [<span data-ttu-id="9581d-155">Configurer l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="9581d-155">Set up dynamic group membership</span></span>](identity-self-service-group-management.md#identity-dyn-groups)

## <a name="next-step"></a><span data-ttu-id="9581d-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9581d-156">Next step</span></span>

<span data-ttu-id="9581d-157">Explorez les autres fonctionnalités liées aux [identités](m365-enterprise-test-lab-guides.md#identity) disponibles dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="9581d-157">Explore additional [identity](m365-enterprise-test-lab-guides.md#identity) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="9581d-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9581d-158">See also</span></span>

[<span data-ttu-id="9581d-159">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="9581d-159">Phase 2: Identity</span></span>](identity-infrastructure.md)

[<span data-ttu-id="9581d-160">Guides de laboratoire de test Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9581d-160">Microsoft 365 Enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="9581d-161">Déploiement d'entreprise Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9581d-161">Microsoft 365 Enterprise deployment</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="9581d-162">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="9581d-162">Microsoft 365 Enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
