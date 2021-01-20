---
title: Étape 1. Vos clients Microsoft 365 entreprise
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- m365solution-tenantmanagement
ms.custom:
- Ent_Solutions
description: Déployez et gérez un ou plusieurs clients Microsoft 365, avec des options pour plusieurs emplacements géographiques et de déplacement.
ms.openlocfilehash: 567a2cb46e715ec560bf973a33ab83cfa63d403b
ms.sourcegitcommit: 99a7354e6a6b4d9d5202674ef57852d52a43fef6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/20/2021
ms.locfileid: "49908590"
---
# <a name="step-1-your-microsoft-365-for-enterprise-tenants"></a><span data-ttu-id="d8356-104">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="d8356-104">Step 1.</span></span> <span data-ttu-id="d8356-105">Vos clients Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="d8356-105">Your Microsoft 365 for enterprise tenants</span></span>

<span data-ttu-id="d8356-106">L’une de vos premières décisions client est le nombre à prendre.</span><span class="sxs-lookup"><span data-stu-id="d8356-106">One of your first tenant decisions is how many to have.</span></span> <span data-ttu-id="d8356-107">Chaque client Microsoft 365 est distinct, unique et distinct de tous les autres clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-107">Each Microsoft 365 tenant is distinct, unique, and separate from all other Microsoft 365 tenants.</span></span> <span data-ttu-id="d8356-108">Son client Azure AD correspondant est également distinct, unique et distinct de tous les autres clients Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-108">It’s corresponding Azure AD tenant is also distinct, unique, and separate from all other Microsoft 365 tenants.</span></span>

## <a name="single-tenant"></a><span data-ttu-id="d8356-109">Client unique</span><span class="sxs-lookup"><span data-stu-id="d8356-109">Single tenant</span></span>
<span data-ttu-id="d8356-110">Le fait d’avoir un seul client simplifie de nombreux aspects de l’utilisation de Microsoft 365 par votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d8356-110">Having a single tenant simplifies many aspects of your organization’s use of Microsoft 365.</span></span> <span data-ttu-id="d8356-111">Un seul client signifie un seul client Azure AD avec un ensemble unique de comptes, de groupes et de stratégies.</span><span class="sxs-lookup"><span data-stu-id="d8356-111">A single tenant means a single Azure AD tenant with a single set of accounts, groups, and policies.</span></span> <span data-ttu-id="d8356-112">Les autorisations et le partage des ressources au sein de votre organisation peuvent être effectués via ce fournisseur d’identité central.</span><span class="sxs-lookup"><span data-stu-id="d8356-112">Permissions and sharing of resources across your organization can be done through this central identity provider.</span></span>

<span data-ttu-id="d8356-113">Un client unique offre à vos utilisateurs l’expérience de collaboration et de productivité la plus riche et la plus simplifiée en fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d8356-113">A single tenant provides the most feature-rich and simplified collaboration and productivity experience for your users.</span></span>

<span data-ttu-id="d8356-114">Voici un exemple montrant l’emplacement par défaut et le client Azure AD d’un client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-114">Here is an example showing the default location and Azure AD tenant of a Microsoft 365 tenant.</span></span>

![Un seul client Microsoft 365 avec son client Azure AD](../media/tenant-management-overview/tenant-management-example-tenant.png)

## <a name="multiple-tenants"></a><span data-ttu-id="d8356-116">Plusieurs clients</span><span class="sxs-lookup"><span data-stu-id="d8356-116">Multiple tenants</span></span>

<span data-ttu-id="d8356-117">Il existe de nombreuses raisons pour lesquelles votre organisation peut avoir plusieurs locataires :</span><span class="sxs-lookup"><span data-stu-id="d8356-117">There are many reasons why your organization could have multiple tenants:</span></span>

- <span data-ttu-id="d8356-118">Isolation administrative</span><span class="sxs-lookup"><span data-stu-id="d8356-118">Administrative isolation</span></span>
- <span data-ttu-id="d8356-119">It décentralisé</span><span class="sxs-lookup"><span data-stu-id="d8356-119">Decentralized IT</span></span>
- <span data-ttu-id="d8356-120">Décisions historiques</span><span class="sxs-lookup"><span data-stu-id="d8356-120">Historical decisions</span></span>
- <span data-ttu-id="d8356-121">Fusions, acquisitions ou désinttures</span><span class="sxs-lookup"><span data-stu-id="d8356-121">Mergers, acquisitions, or divestitures</span></span>
- <span data-ttu-id="d8356-122">Séparation claire de la marque pour les organisations conglomérats</span><span class="sxs-lookup"><span data-stu-id="d8356-122">Clear separation of branding for conglomerate organizations</span></span>
- <span data-ttu-id="d8356-123">Préproduction, test ou client bac à sable</span><span class="sxs-lookup"><span data-stu-id="d8356-123">Pre-production, test, or sandbox tenants</span></span>

<span data-ttu-id="d8356-124">Voici un exemple d’organisation qui possède deux clients (client A et client B) dans la même géo de centre de données par défaut.</span><span class="sxs-lookup"><span data-stu-id="d8356-124">Here is an example of an organization that has two tenants (Tenant A and Tenant B) in the same default datacenter geo.</span></span> <span data-ttu-id="d8356-125">Chaque client en tant que client Azure AD distinct.</span><span class="sxs-lookup"><span data-stu-id="d8356-125">Each tenant as a separate Azure AD tenant.</span></span>

![Plusieurs clients Microsoft 365 avec leurs propres clients Azure AD](../media/tenant-management-overview/tenant-management-example-multi-tenant.png)

<span data-ttu-id="d8356-127">Lorsque vous avez plusieurs clients, il existe des restrictions et des considérations supplémentaires lors de leur gestion et de la fourniture de services à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d8356-127">When you have multiple tenants, there are restrictions and additional considerations when managing them and providing services to your users.</span></span>

### <a name="inter-tenant-collaboration"></a><span data-ttu-id="d8356-128">Collaboration inter-clients</span><span class="sxs-lookup"><span data-stu-id="d8356-128">Inter-tenant collaboration</span></span>

<span data-ttu-id="d8356-129">Si vous souhaitez que vos utilisateurs collaborent plus efficacement entre différents clients Microsoft 365 de manière sécurisée, les options de collaboration entre clients incluent l’utilisation d’un emplacement central pour les fichiers et les conversations, le partage de calendriers, l’utilisation de la messagerie instantanée, les appels audio/vidéo pour la communication et la sécurisation de l’accès aux ressources et aux applications.</span><span class="sxs-lookup"><span data-stu-id="d8356-129">If you want your users to collaborate more effectively across different Microsoft 365 tenants in a secure manner, inter-tenant collaboration options include using a central location for files and conversations, sharing calendars, using IM, audio/video calls for communication, and securing access to resources and applications.</span></span>

<span data-ttu-id="d8356-130">Pour plus d’informations, voir collaboration entre clients [Microsoft 365.](../enterprise/microsoft-365-inter-tenant-collaboration.md)</span><span class="sxs-lookup"><span data-stu-id="d8356-130">For more information, see [Microsoft 365 inter-tenant collaboration](../enterprise/microsoft-365-inter-tenant-collaboration.md).</span></span>

### <a name="cross-tenant-mailbox-migration-preview"></a><span data-ttu-id="d8356-131">Migration de boîtes aux lettres entre locataires (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="d8356-131">Cross-tenant mailbox migration (preview)</span></span>

<span data-ttu-id="d8356-132">Avant la migration de boîtes aux lettres entre les locataires (en prévisualisation), lorsque vous migrez des boîtes aux lettres Exchange Online entre des locataires, vous devez déboarder complètement une boîte aux lettres utilisateur de son client actuel (le client source) vers l’ordinateur local, puis les intégrer à un nouveau client (le client cible).</span><span class="sxs-lookup"><span data-stu-id="d8356-132">Prior to cross-tenant mailbox migration (in preview), when moving Exchange Online mailboxes between tenants, you have to completely offboard a user mailbox from their current tenant (the source tenant) to on-premises and then onboard them to a new tenant (the target tenant).</span></span> <span data-ttu-id="d8356-133">Grâce à la nouvelle fonctionnalité de migration de boîtes aux lettres entre les locataires, les administrateurs client des locataires source et cible peuvent déplacer des boîtes aux lettres entre les locataires avec un minimum de dépendances d’infrastructure dans leurs systèmes locaux.</span><span class="sxs-lookup"><span data-stu-id="d8356-133">With the new cross-tenant mailbox migration feature, tenant administrators in both source and target tenants can move mailboxes between the tenants with minimal infrastructure dependencies in their on-premises systems.</span></span> <span data-ttu-id="d8356-134">Cela supprime la nécessité de supprimer les boîtes aux lettres d’intégration et d’intégration.</span><span class="sxs-lookup"><span data-stu-id="d8356-134">This removes the need to off-board and onboard mailboxes.</span></span>

<span data-ttu-id="d8356-135">Voici deux exemples de client et leurs boîtes aux lettres avant la migration de boîtes aux lettres entre locataires.</span><span class="sxs-lookup"><span data-stu-id="d8356-135">Here are two example tenants and their mailboxes before cross-tenant mailbox migration.</span></span>

![Plusieurs clients Microsoft 365 et leurs boîtes aux lettres](../media/tenant-management-overview/tenant-management-cross-tenant-mailbox-before.png)

<span data-ttu-id="d8356-137">Dans cette illustration, deux locataires distincts ont leurs propres domaines et ensemble de boîtes aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8356-137">In this illustration, two separate tenants have their own domains and set of Exchange mailboxes.</span></span>

<span data-ttu-id="d8356-138">Voici le client cible (locataire A) après la migration de boîtes aux lettres entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="d8356-138">Here is the target tenant (Tenant A) after cross-tenant mailbox migration.</span></span>

![Client cible après la migration de boîtes aux lettres entre les locataires](../media/tenant-management-overview/tenant-management-cross-tenant-mailbox-after.png)

<span data-ttu-id="d8356-140">Dans cette illustration, un seul client possède à la fois des domaines et les deux ensembles de boîtes aux lettres Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8356-140">In this illustration, a single tenant has both domains and both sets of Exchange mailboxes.</span></span>

<span data-ttu-id="d8356-141">Pour plus d’informations, consultez [la migration de boîtes aux lettres entre locataires.](../enterprise/cross-tenant-mailbox-migration.md)</span><span class="sxs-lookup"><span data-stu-id="d8356-141">For more information, see [Cross-tenant mailbox migration](../enterprise/cross-tenant-mailbox-migration.md).</span></span>

### <a name="tenant-to-tenant-migrations"></a><span data-ttu-id="d8356-142">Migrations client vers client</span><span class="sxs-lookup"><span data-stu-id="d8356-142">Tenant-to-tenant migrations</span></span>

<span data-ttu-id="d8356-143">Il existe plusieurs approches architecturales pour les fusions, les acquisitions, les déssinttures et d’autres scénarios qui peuvent vous amener à migrer un client Microsoft 365 existant vers un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="d8356-143">There are several architectural approaches for mergers, acquisitions, divestitures, and other scenarios that might lead you to migrate an existing Microsoft 365 tenant to a new tenant.</span></span> 

<span data-ttu-id="d8356-144">Pour obtenir des instructions [détaillées, voir migrations client à client Microsoft 365.](../enterprise/microsoft-365-tenant-to-tenant-migrations.md)</span><span class="sxs-lookup"><span data-stu-id="d8356-144">For detailed guidance, see [Microsoft 365 tenant-to-tenant migrations](../enterprise/microsoft-365-tenant-to-tenant-migrations.md).</span></span>

## <a name="multi-geo-for-a-tenant"></a><span data-ttu-id="d8356-145">Multi-Géo pour un client</span><span class="sxs-lookup"><span data-stu-id="d8356-145">Multi-Geo for a tenant</span></span>

<span data-ttu-id="d8356-146">Avec Microsoft 365 Multi-Géo, vous pouvez mettre en service et stocker des données au repos dans les autres emplacements géographiques de centres de données que vous avez choisis pour répondre aux exigences de résidence des données, et en même temps déverrouiller votre déploiement global d’expériences de productivité modernes pour vos employés.</span><span class="sxs-lookup"><span data-stu-id="d8356-146">With Microsoft 365 Multi-Geo, you can provision and store data at rest in the other datacenter geo locations that you've chosen to meet data residency requirements, and at the same time unlock your global rollout of modern productivity experiences to your workers.</span></span>

<span data-ttu-id="d8356-147">Dans un environnement Multi-Géo, votre client Microsoft 365 se compose d’un emplacement par défaut ou central où votre abonnement Microsoft 365 a été créé à l’origine et d’un ou plusieurs emplacements satellites.</span><span class="sxs-lookup"><span data-stu-id="d8356-147">In a Multi-Geo environment, your Microsoft 365 tenant consists of a default or central location where your Microsoft 365 subscription was originally created and one or more satellite locations.</span></span> <span data-ttu-id="d8356-148">Dans un client multigé géographique, les informations sur les emplacements géographiques, les groupes et les informations utilisateur sont maîtres dans un client Azure AD global.</span><span class="sxs-lookup"><span data-stu-id="d8356-148">In a multi-geo tenant, the information about geo locations, groups, and user information is mastered in a global Azure AD tenant.</span></span> <span data-ttu-id="d8356-149">Étant donné que les informations de votre client sont centralisées et synchronisées dans chaque emplacement géographique, les expériences de collaboration impliquant toute personne de votre entreprise sont partagées entre les emplacements.</span><span class="sxs-lookup"><span data-stu-id="d8356-149">Because your tenant information is mastered centrally and synchronized into each geo location, collaboration experiences involving anyone from your company are shared across the locations.</span></span>

<span data-ttu-id="d8356-150">Voici un exemple d’organisation qui a son emplacement par défaut en Europe et un emplacement satellite en Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="d8356-150">Here is an example of an organization that has its default location in Europe and a satellite location in North America.</span></span> <span data-ttu-id="d8356-151">Les deux emplacements partagent le même client Azure AD global pour le client Microsoft 365 unique.</span><span class="sxs-lookup"><span data-stu-id="d8356-151">Both locations share the same global Azure AD tenant for the single Microsoft 365 tenant.</span></span>

![Exemple de client Microsoft 365 multigéogé](../media/tenant-management-overview/tenant-management-example-multi-geo.png)

<span data-ttu-id="d8356-153">Pour en savoir plus, consultez [Microsoft 365 Multigéographie](../enterprise/microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="d8356-153">For more information, see [Microsoft 365 Multi-Geo](../enterprise/microsoft-365-multi-geo.md).</span></span>

## <a name="moving-core-data-to-a-new-datacenter-geo"></a><span data-ttu-id="d8356-154">Déplacement de données principales vers une nouvelle géo de centres de données</span><span class="sxs-lookup"><span data-stu-id="d8356-154">Moving core data to a new datacenter geo</span></span>

<span data-ttu-id="d8356-155">Microsoft continue d’ouvrir de nouvelles géos de centres de données pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-155">Microsoft continues to open new datacenter geos for Microsoft 365 services.</span></span> <span data-ttu-id="d8356-156">Ces nouvelles régions de centre de données permettent d'accroître la capacité et le nombre de ressources de calcul pour prendre en charge la demande continue des clients et l'augmentation de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="d8356-156">These new datacenter geos add capacity and compute resources to support our ongoing customer demand and usage growth.</span></span> <span data-ttu-id="d8356-157">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="d8356-157">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="d8356-158">Bien que l’ouverture d’une nouvelle géo de centre de données n’a pas d’impact sur vous et vos données principales stockées dans une géo de centres de données déjà existante, Microsoft vous permet de demander une migration anticipée des données client essentielles de votre organisation au repos vers une nouvelle géo de centres de données.</span><span class="sxs-lookup"><span data-stu-id="d8356-158">Although opening a new datacenter geo does not impact you and your core data stored in an already existing datacenter geo, Microsoft allows you to request an early migration of your organization's core customer data at rest to a new datacenter geo.</span></span>

<span data-ttu-id="d8356-159">Voici un exemple dans lequel un client Microsoft 365 a été déplacé de la géo du centre de données de l’Union européenne (UE) vers celle située au Royaume-Uni.</span><span class="sxs-lookup"><span data-stu-id="d8356-159">Here is an example in which a Microsoft 365 tenant was moved from the European Union (EU) datacenter geo to the one located in the United Kingdom (UK).</span></span>

![Exemple de déplacement d’un client Microsoft 365 entre des centres de données géographiques](../media/tenant-management-overview/tenant-management-example-tenant-move.png)

<span data-ttu-id="d8356-161">Pour plus d’informations, voir Déplacement de données principales vers de nouvelles géos de centres de données [Microsoft 365.](../enterprise/moving-data-to-new-datacenter-geos.md)</span><span class="sxs-lookup"><span data-stu-id="d8356-161">For more information, see [Moving core data to new Microsoft 365 datacenter geos](../enterprise/moving-data-to-new-datacenter-geos.md).</span></span>

## <a name="products-and-licenses-for-a-tenant"></a><span data-ttu-id="d8356-162">Produits et licences pour un client</span><span class="sxs-lookup"><span data-stu-id="d8356-162">Products and licenses for a tenant</span></span>

<span data-ttu-id="d8356-163">Votre client Microsoft 365 est créé lorsque vous achetez votre premier produit, tel que Microsoft 365 E3.</span><span class="sxs-lookup"><span data-stu-id="d8356-163">Your Microsoft 365 tenant gets created when you purchase your first product, such as Microsoft 365 E3.</span></span> <span data-ttu-id="d8356-164">Le produit est accompagné de licences facturées mensuellement ou annuellement.</span><span class="sxs-lookup"><span data-stu-id="d8356-164">Along with the product are licenses, which are charged a monthly or annual fee.</span></span> <span data-ttu-id="d8356-165">Un administrateur attribue ensuite une licence disponible à partir de l’un de vos produits à un compte d’utilisateur, directement ou par le biais de l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="d8356-165">An administrator then assigns an available license from one of your products to a user account, either directly or through group membership.</span></span> <span data-ttu-id="d8356-166">Selon les besoins de votre organisation, vous pouvez avoir un ensemble de produits, chacun avec son propre pool de licences.</span><span class="sxs-lookup"><span data-stu-id="d8356-166">Depending on your organization's business needs, you might have a set of products, each with their own pool of licenses.</span></span> 

<span data-ttu-id="d8356-167">La détermination de l’ensemble des produits et du nombre de licences pour chacun d’eux nécessite une planification pour :</span><span class="sxs-lookup"><span data-stu-id="d8356-167">Determining the set of products and the number of licenses for each requires some planning to:</span></span>

- <span data-ttu-id="d8356-168">Assurez-vous que vous disposez de suffisamment de licences pour les comptes d’utilisateurs qui ont besoin de fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="d8356-168">Ensure you have enough licenses for the user accounts that need advanced features.</span></span>
- <span data-ttu-id="d8356-169">Vous empêchez de ne plus disposer de licences ou d’avoir trop de licences non inscrites, en fonction des modifications apportées au personnel de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d8356-169">Prevent you from running out of licenses or having too many unassigned licenses, based on changes in staffing at your organization.</span></span>


## <a name="results-of-step-1"></a><span data-ttu-id="d8356-170">Résultats de l’étape 1</span><span class="sxs-lookup"><span data-stu-id="d8356-170">Results of Step 1</span></span>

<span data-ttu-id="d8356-171">Pour vos clients Microsoft 365 entreprise, vous avez déterminé :</span><span class="sxs-lookup"><span data-stu-id="d8356-171">For your Microsoft 365 for enterprise tenants, you have determined:</span></span>

- <span data-ttu-id="d8356-172">Nombre de locataires dont vous avez ou avez besoin.</span><span class="sxs-lookup"><span data-stu-id="d8356-172">How many tenants you have or need.</span></span>
- <span data-ttu-id="d8356-173">Pour chaque client, quels produits et licences doivent être achetés.</span><span class="sxs-lookup"><span data-stu-id="d8356-173">For each tenant, which products and licenses must be purchased.</span></span>
- <span data-ttu-id="d8356-174">Indique si un client doit être multigéogé pour se conformer aux exigences de résidence des données.</span><span class="sxs-lookup"><span data-stu-id="d8356-174">Whether a tenant needs to be Multi-Geo to comply with data residency requirements.</span></span>
- <span data-ttu-id="d8356-175">Si vous devez configurer la collaboration entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="d8356-175">Whether you need to set up inter-tenant collaboration.</span></span>
- <span data-ttu-id="d8356-176">Si vous devez migrer un client vers un autre.</span><span class="sxs-lookup"><span data-stu-id="d8356-176">Whether you need to migrate one tenant to another.</span></span>
- <span data-ttu-id="d8356-177">Indique si vous devez déplacer des données principales d’une géo de centres de données vers une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="d8356-177">Whether you need to move core data from one datacenter geo to new one.</span></span>

<span data-ttu-id="d8356-178">Voici un exemple de nouveau client.</span><span class="sxs-lookup"><span data-stu-id="d8356-178">Here is an example of a new tenant.</span></span>

![Exemple de nouveau client](../media/tenant-management-overview/tenant-management-tenant-build-step1.png)

<span data-ttu-id="d8356-180">Dans cette illustration, le client a :</span><span class="sxs-lookup"><span data-stu-id="d8356-180">In this illustration, the tenant has:</span></span>

- <span data-ttu-id="d8356-181">Emplacement par défaut correspondant à une région de centre de données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-181">A default location corresponding to a Microsoft 365 datacenter geo.</span></span>
- <span data-ttu-id="d8356-182">Ensemble de produits et de licences.</span><span class="sxs-lookup"><span data-stu-id="d8356-182">A set of products and licenses.</span></span>
- <span data-ttu-id="d8356-183">Ensemble d’applications de productivité cloud, dont certaines sont spécifiques aux produits.</span><span class="sxs-lookup"><span data-stu-id="d8356-183">The set of cloud productivity apps, some of which are specific to products.</span></span>
- <span data-ttu-id="d8356-184">Un client Azure AD qui contient des comptes d’administrateur général et un nom de domaine DNS initial.</span><span class="sxs-lookup"><span data-stu-id="d8356-184">An Azure AD tenant that contains global administrator accounts and an initial DNS domain name.</span></span>

<span data-ttu-id="d8356-185">Au fil des étapes supplémentaires de cette solution, nous allons créer cette figure.</span><span class="sxs-lookup"><span data-stu-id="d8356-185">As we move through the additional steps of this solution, we will build out this figure.</span></span>

## <a name="ongoing-maintenance-for-tenants"></a><span data-ttu-id="d8356-186">Maintenance continue pour les locataires</span><span class="sxs-lookup"><span data-stu-id="d8356-186">Ongoing maintenance for tenants</span></span>

<span data-ttu-id="d8356-187">Régulièrement, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="d8356-187">On an ongoing basis, you might need to:</span></span>

- <span data-ttu-id="d8356-188">Ajoutez un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="d8356-188">Add a new tenant.</span></span>
- <span data-ttu-id="d8356-189">Ajoutez de nouveaux produits à un client avec un nombre initial de licences.</span><span class="sxs-lookup"><span data-stu-id="d8356-189">Add new products to a tenant with an initial number of licenses.</span></span>
- <span data-ttu-id="d8356-190">Modifier l’ensemble des licences d’un produit dans un client pour ajuster les besoins du personnel.</span><span class="sxs-lookup"><span data-stu-id="d8356-190">Change the set of licenses for a product in a tenant to adjust for changing staff requirements.</span></span>
- <span data-ttu-id="d8356-191">Déplacez vos données principales d’un client vers un nouvel emplacement géographique de centre de données.</span><span class="sxs-lookup"><span data-stu-id="d8356-191">Move your core data from a tenant to a new datacenter geo location.</span></span>
- <span data-ttu-id="d8356-192">Ajoutez Multi-Géo pour les exigences de résidence des données.</span><span class="sxs-lookup"><span data-stu-id="d8356-192">Add Multi-Geo for data residency requirements.</span></span>
- <span data-ttu-id="d8356-193">Configurer la collaboration entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="d8356-193">Set up inter-tenant collaboration.</span></span>

## <a name="next-step"></a><span data-ttu-id="d8356-194">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d8356-194">Next step</span></span>

<span data-ttu-id="d8356-195">[![Étape 2. Optimiser votre client pour l’accès au réseau](../media/tenant-management-overview/tenant-management-step-grid-networking.png)](tenant-management-networking.md)</span><span class="sxs-lookup"><span data-stu-id="d8356-195">[![Step 2. Optimize your tenant for network for access](../media/tenant-management-overview/tenant-management-step-grid-networking.png)](tenant-management-networking.md)</span></span>

<span data-ttu-id="d8356-196">Poursuivez la [mise en](tenant-management-networking.md) réseau pour fournir une mise en réseau optimale de vos employés aux services cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8356-196">Continue with [networking](tenant-management-networking.md) to provide optimal networking from your workers to Microsoft 365 cloud services.</span></span>
