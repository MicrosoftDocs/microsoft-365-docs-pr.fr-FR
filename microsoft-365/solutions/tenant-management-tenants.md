---
title: Étape 1. Votre Microsoft 365 pour les locataires d’entreprise
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
- tenant-management
- m365solution-scenario
ms.custom:
- Ent_Solutions
description: Déployez et gérez un ou plusieurs Microsoft 365 client, avec des options pour les emplacements multigé géographiques et les emplacements de déplacement.
ms.openlocfilehash: 4d9bd685fce6fb2f11b8e17bebae6460e0c10bd2
ms.sourcegitcommit: 070724118be25cd83418d2a56863da95582dae65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "50406383"
---
# <a name="step-1-your-microsoft-365-for-enterprise-tenants"></a><span data-ttu-id="e2b6a-104">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-104">Step 1.</span></span> <span data-ttu-id="e2b6a-105">Votre Microsoft 365 pour les locataires d’entreprise</span><span class="sxs-lookup"><span data-stu-id="e2b6a-105">Your Microsoft 365 for enterprise tenants</span></span>

<span data-ttu-id="e2b6a-106">L’une de vos premières décisions client est le nombre à prendre.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-106">One of your first tenant decisions is how many to have.</span></span> <span data-ttu-id="e2b6a-107">Chaque Microsoft 365 client est distinct, unique et distinct de tous les autres Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-107">Each Microsoft 365 tenant is distinct, unique, and separate from all other Microsoft 365 tenants.</span></span> <span data-ttu-id="e2b6a-108">Son client Azure AD correspondant est également distinct, unique et distinct de tous les autres Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-108">It’s corresponding Azure AD tenant is also distinct, unique, and separate from all other Microsoft 365 tenants.</span></span>

## <a name="single-tenant"></a><span data-ttu-id="e2b6a-109">Client unique</span><span class="sxs-lookup"><span data-stu-id="e2b6a-109">Single tenant</span></span>
<span data-ttu-id="e2b6a-110">Le fait d’avoir un seul client simplifie de nombreux aspects de l’utilisation des Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-110">Having a single tenant simplifies many aspects of your organization’s use of Microsoft 365.</span></span> <span data-ttu-id="e2b6a-111">Un seul client signifie un seul client Azure AD avec un ensemble unique de comptes, de groupes et de stratégies.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-111">A single tenant means a single Azure AD tenant with a single set of accounts, groups, and policies.</span></span> <span data-ttu-id="e2b6a-112">Les autorisations et le partage des ressources au sein de votre organisation peuvent être effectués via ce fournisseur d’identité central.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-112">Permissions and sharing of resources across your organization can be done through this central identity provider.</span></span>

<span data-ttu-id="e2b6a-113">Un client unique offre à vos utilisateurs l’expérience de collaboration et de productivité la plus riche et la plus simplifiée en fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-113">A single tenant provides the most feature-rich and simplified collaboration and productivity experience for your users.</span></span>

<span data-ttu-id="e2b6a-114">Voici un exemple montrant l’emplacement par défaut et le client Azure AD d’Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-114">Here is an example showing the default location and Azure AD tenant of a Microsoft 365 tenant.</span></span>

![Un client Microsoft 365 client unique avec son client Azure AD](../media/tenant-management-overview/tenant-management-example-tenant.png)

## <a name="multiple-tenants"></a><span data-ttu-id="e2b6a-116">Plusieurs clients</span><span class="sxs-lookup"><span data-stu-id="e2b6a-116">Multiple tenants</span></span>

<span data-ttu-id="e2b6a-117">Il existe de nombreuses raisons pour lesquelles votre organisation peut avoir plusieurs locataires :</span><span class="sxs-lookup"><span data-stu-id="e2b6a-117">There are many reasons why your organization could have multiple tenants:</span></span>

- <span data-ttu-id="e2b6a-118">Isolation administrative</span><span class="sxs-lookup"><span data-stu-id="e2b6a-118">Administrative isolation</span></span>
- <span data-ttu-id="e2b6a-119">It décentralisé</span><span class="sxs-lookup"><span data-stu-id="e2b6a-119">Decentralized IT</span></span>
- <span data-ttu-id="e2b6a-120">Décisions historiques</span><span class="sxs-lookup"><span data-stu-id="e2b6a-120">Historical decisions</span></span>
- <span data-ttu-id="e2b6a-121">Fusions, acquisitions ou désinttures</span><span class="sxs-lookup"><span data-stu-id="e2b6a-121">Mergers, acquisitions, or divestitures</span></span>
- <span data-ttu-id="e2b6a-122">Séparation claire de la marque pour les organisations conglomérats</span><span class="sxs-lookup"><span data-stu-id="e2b6a-122">Clear separation of branding for conglomerate organizations</span></span>
- <span data-ttu-id="e2b6a-123">Préproduction, test ou client bac à sable</span><span class="sxs-lookup"><span data-stu-id="e2b6a-123">Pre-production, test, or sandbox tenants</span></span>

<span data-ttu-id="e2b6a-124">Voici un exemple d’organisation qui possède deux clients (client A et client B) dans la même géo de centre de données par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-124">Here is an example of an organization that has two tenants (Tenant A and Tenant B) in the same default datacenter geo.</span></span> <span data-ttu-id="e2b6a-125">Chaque client en tant que client Azure AD distinct.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-125">Each tenant as a separate Azure AD tenant.</span></span>

![Plusieurs Microsoft 365 avec leurs propres locataires Azure AD](../media/tenant-management-overview/tenant-management-example-multi-tenant.png)

<span data-ttu-id="e2b6a-127">Lorsque vous avez plusieurs clients, il existe des restrictions et des considérations supplémentaires lors de leur gestion et de la fourniture de services à vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-127">When you have multiple tenants, there are restrictions and additional considerations when managing them and providing services to your users.</span></span>

### <a name="inter-tenant-collaboration"></a><span data-ttu-id="e2b6a-128">Collaboration inter-clients</span><span class="sxs-lookup"><span data-stu-id="e2b6a-128">Inter-tenant collaboration</span></span>

<span data-ttu-id="e2b6a-129">Si vous souhaitez que vos utilisateurs collaborent plus efficacement entre différents clients Microsoft 365 de manière sécurisée, les options de collaboration entre clients incluent l’utilisation d’un emplacement central pour les fichiers et les conversations, le partage de calendriers, l’utilisation de la messagerie instantanée, des appels audio/vidéo pour la communication et la sécurisation de l’accès aux ressources et aux applications.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-129">If you want your users to collaborate more effectively across different Microsoft 365 tenants in a secure manner, inter-tenant collaboration options include using a central location for files and conversations, sharing calendars, using IM, audio/video calls for communication, and securing access to resources and applications.</span></span>

<span data-ttu-id="e2b6a-130">Pour plus d’informations, [voir Microsoft 365 collaboration inter-locataires.](../enterprise/microsoft-365-inter-tenant-collaboration.md)</span><span class="sxs-lookup"><span data-stu-id="e2b6a-130">For more information, see [Microsoft 365 inter-tenant collaboration](../enterprise/microsoft-365-inter-tenant-collaboration.md).</span></span>

### <a name="cross-tenant-mailbox-migration-preview"></a><span data-ttu-id="e2b6a-131">Migration de boîtes aux lettres entre locataires (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="e2b6a-131">Cross-tenant mailbox migration (preview)</span></span>

<span data-ttu-id="e2b6a-132">Avant la migration de boîtes aux lettres entre les locataires (en prévisualisation), lors du déplacement de boîtes aux lettres Exchange Online entre les locataires, vous devez déboarder complètement une boîte aux lettres utilisateur de son client actuel (le client source) vers l’ordinateur local, puis l’intégrer à un nouveau client (le client cible).</span><span class="sxs-lookup"><span data-stu-id="e2b6a-132">Prior to cross-tenant mailbox migration (in preview), when moving Exchange Online mailboxes between tenants, you have to completely offboard a user mailbox from their current tenant (the source tenant) to on-premises and then onboard them to a new tenant (the target tenant).</span></span> <span data-ttu-id="e2b6a-133">Grâce à la nouvelle fonctionnalité de migration de boîtes aux lettres entre les locataires, les administrateurs client des locataires source et cible peuvent déplacer des boîtes aux lettres entre les locataires avec des dépendances d’infrastructure minimales dans leurs systèmes locaux.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-133">With the new cross-tenant mailbox migration feature, tenant administrators in both source and target tenants can move mailboxes between the tenants with minimal infrastructure dependencies in their on-premises systems.</span></span> <span data-ttu-id="e2b6a-134">Cela permet de supprimer la nécessité d’intégrer et d’intégrer des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-134">This removes the need to off-board and onboard mailboxes.</span></span>

<span data-ttu-id="e2b6a-135">Voici deux exemples de client et leurs boîtes aux lettres avant la migration de boîtes aux lettres entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-135">Here are two example tenants and their mailboxes before cross-tenant mailbox migration.</span></span>

![Plusieurs Microsoft 365 client et leurs boîtes aux lettres](../media/tenant-management-overview/tenant-management-cross-tenant-mailbox-before.png)

<span data-ttu-id="e2b6a-137">Dans cette illustration, deux locataires distincts ont leurs propres domaines et ensemble de Exchange boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-137">In this illustration, two separate tenants have their own domains and set of Exchange mailboxes.</span></span>

<span data-ttu-id="e2b6a-138">Voici le client cible (locataire A) après la migration de boîtes aux lettres entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-138">Here is the target tenant (Tenant A) after cross-tenant mailbox migration.</span></span>

![Client cible après la migration de boîtes aux lettres entre les locataires](../media/tenant-management-overview/tenant-management-cross-tenant-mailbox-after.png)

<span data-ttu-id="e2b6a-140">Dans cette illustration, un seul client possède à la fois des domaines et les deux ensembles Exchange boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-140">In this illustration, a single tenant has both domains and both sets of Exchange mailboxes.</span></span>

<span data-ttu-id="e2b6a-141">Pour plus d’informations, consultez [la migration de boîtes aux lettres entre locataires.](../enterprise/cross-tenant-mailbox-migration.md)</span><span class="sxs-lookup"><span data-stu-id="e2b6a-141">For more information, see [Cross-tenant mailbox migration](../enterprise/cross-tenant-mailbox-migration.md).</span></span>

### <a name="tenant-to-tenant-migrations"></a><span data-ttu-id="e2b6a-142">Migrations client vers client</span><span class="sxs-lookup"><span data-stu-id="e2b6a-142">Tenant-to-tenant migrations</span></span>

<span data-ttu-id="e2b6a-143">Il existe plusieurs approches architecturales pour les fusions, les acquisitions, les déssinttures et d’autres scénarios qui peuvent vous amener à migrer un client Microsoft 365 existant vers un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-143">There are several architectural approaches for mergers, acquisitions, divestitures, and other scenarios that might lead you to migrate an existing Microsoft 365 tenant to a new tenant.</span></span> 

<span data-ttu-id="e2b6a-144">Pour obtenir des instructions détaillées, [voir Microsoft 365 migrations](../enterprise/microsoft-365-tenant-to-tenant-migrations.md)client à client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-144">For detailed guidance, see [Microsoft 365 tenant-to-tenant migrations](../enterprise/microsoft-365-tenant-to-tenant-migrations.md).</span></span>

## <a name="multi-geo-for-a-tenant"></a><span data-ttu-id="e2b6a-145">Multi-Géo pour un client</span><span class="sxs-lookup"><span data-stu-id="e2b6a-145">Multi-Geo for a tenant</span></span>

<span data-ttu-id="e2b6a-146">Avec Microsoft 365 Multi-Géo, vous pouvez mettre en service et stocker des données au repos dans les autres emplacements géographiques de centres de données que vous avez choisis pour répondre aux exigences de résidence des données, et en même temps déverrouiller votre déploiement global d’expériences de productivité modernes pour vos employés.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-146">With Microsoft 365 Multi-Geo, you can provision and store data at rest in the other datacenter geo locations that you've chosen to meet data residency requirements, and at the same time unlock your global rollout of modern productivity experiences to your workers.</span></span>

<span data-ttu-id="e2b6a-147">Dans un environnement Multi-Géo, votre client Microsoft 365 se compose d’un emplacement par défaut ou central où votre abonnement Microsoft 365 a été créé à l’origine et d’un ou plusieurs emplacements satellites.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-147">In a Multi-Geo environment, your Microsoft 365 tenant consists of a default or central location where your Microsoft 365 subscription was originally created and one or more satellite locations.</span></span> <span data-ttu-id="e2b6a-148">Dans un client multigé géographique, les informations sur les emplacements géographiques, les groupes et les informations utilisateur sont maîtres dans un client Azure AD global.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-148">In a multi-geo tenant, the information about geo locations, groups, and user information is mastered in a global Azure AD tenant.</span></span> <span data-ttu-id="e2b6a-149">Étant donné que les informations de votre client sont centralisées et synchronisées dans chaque emplacement géographique, les expériences de collaboration impliquant toute personne de votre entreprise sont partagées entre les emplacements.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-149">Because your tenant information is mastered centrally and synchronized into each geo location, collaboration experiences involving anyone from your company are shared across the locations.</span></span>

<span data-ttu-id="e2b6a-150">Voici un exemple d’organisation qui a son emplacement par défaut en Europe et un emplacement satellite en Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-150">Here is an example of an organization that has its default location in Europe and a satellite location in North America.</span></span> <span data-ttu-id="e2b6a-151">Les deux emplacements partagent le même client Azure AD global pour le client Microsoft 365 client unique.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-151">Both locations share the same global Azure AD tenant for the single Microsoft 365 tenant.</span></span>

![Exemple de client de Microsoft 365 multigéogé](../media/tenant-management-overview/tenant-management-example-multi-geo.png)

<span data-ttu-id="e2b6a-153">Pour en savoir plus, consultez [Microsoft 365 Multigéographie](../enterprise/microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="e2b6a-153">For more information, see [Microsoft 365 Multi-Geo](../enterprise/microsoft-365-multi-geo.md).</span></span>

## <a name="moving-core-data-to-a-new-datacenter-geo"></a><span data-ttu-id="e2b6a-154">Déplacement de données principales vers une nouvelle géo de centres de données</span><span class="sxs-lookup"><span data-stu-id="e2b6a-154">Moving core data to a new datacenter geo</span></span>

<span data-ttu-id="e2b6a-155">Microsoft continue d’ouvrir de nouvelles géos de centres de données pour Microsoft 365 services.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-155">Microsoft continues to open new datacenter geos for Microsoft 365 services.</span></span> <span data-ttu-id="e2b6a-156">Ces nouvelles régions de centre de données permettent d'accroître la capacité et le nombre de ressources de calcul pour prendre en charge la demande continue des clients et l'augmentation de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-156">These new datacenter geos add capacity and compute resources to support our ongoing customer demand and usage growth.</span></span> <span data-ttu-id="e2b6a-157">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-157">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="e2b6a-158">Bien que l’ouverture d’une nouvelle géo de centre de données n’a pas d’impact sur vous et vos données principales stockées dans une géo de centres de données déjà existante, Microsoft vous permet de demander une migration anticipée des données client essentielles de votre organisation au repos vers une nouvelle géo de centres de données.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-158">Although opening a new datacenter geo does not impact you and your core data stored in an already existing datacenter geo, Microsoft allows you to request an early migration of your organization's core customer data at rest to a new datacenter geo.</span></span>

<span data-ttu-id="e2b6a-159">Voici un exemple dans lequel un client Microsoft 365 a été déplacé de la géo du centre de données de l’Union européenne (UE) vers celle située au Royaume-Uni.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-159">Here is an example in which a Microsoft 365 tenant was moved from the European Union (EU) datacenter geo to the one located in the United Kingdom (UK).</span></span>

![Exemple de déplacement d’Microsoft 365 client entre des centres de données géographiques](../media/tenant-management-overview/tenant-management-example-tenant-move.png)

<span data-ttu-id="e2b6a-161">Pour plus d’informations, voir [Déplacement de données principales vers de nouvelles Microsoft 365 de centres de données.](../enterprise/moving-data-to-new-datacenter-geos.md)</span><span class="sxs-lookup"><span data-stu-id="e2b6a-161">For more information, see [Moving core data to new Microsoft 365 datacenter geos](../enterprise/moving-data-to-new-datacenter-geos.md).</span></span>

## <a name="products-and-licenses-for-a-tenant"></a><span data-ttu-id="e2b6a-162">Produits et licences pour un client</span><span class="sxs-lookup"><span data-stu-id="e2b6a-162">Products and licenses for a tenant</span></span>

<span data-ttu-id="e2b6a-163">Votre Microsoft 365 client est créé lorsque vous achetez votre premier produit, par exemple Microsoft 365 E3.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-163">Your Microsoft 365 tenant gets created when you purchase your first product, such as Microsoft 365 E3.</span></span> <span data-ttu-id="e2b6a-164">Les licences, qui sont facturées mensuellement ou annuellement, sont également des licences.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-164">Along with the product are licenses, which are charged a monthly or annual fee.</span></span> <span data-ttu-id="e2b6a-165">Un administrateur attribue ensuite une licence disponible à partir de l’un de vos produits à un compte d’utilisateur, directement ou par le biais de l’appartenance à un groupe.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-165">An administrator then assigns an available license from one of your products to a user account, either directly or through group membership.</span></span> <span data-ttu-id="e2b6a-166">Selon les besoins de votre organisation, vous pouvez avoir un ensemble de produits, chacun avec son propre pool de licences.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-166">Depending on your organization's business needs, you might have a set of products, each with their own pool of licenses.</span></span> 

<span data-ttu-id="e2b6a-167">La détermination de l’ensemble des produits et du nombre de licences pour chacun d’eux nécessite une planification pour :</span><span class="sxs-lookup"><span data-stu-id="e2b6a-167">Determining the set of products and the number of licenses for each requires some planning to:</span></span>

- <span data-ttu-id="e2b6a-168">Assurez-vous que vous disposez de suffisamment de licences pour les comptes d’utilisateur qui ont besoin de fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-168">Ensure you have enough licenses for the user accounts that need advanced features.</span></span>
- <span data-ttu-id="e2b6a-169">Vous empêchez d’être à court de licences ou d’avoir trop de licences non inscrites, en fonction des modifications apportées au personnel de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-169">Prevent you from running out of licenses or having too many unassigned licenses, based on changes in staffing at your organization.</span></span>


## <a name="results-of-step-1"></a><span data-ttu-id="e2b6a-170">Résultats de l’étape 1</span><span class="sxs-lookup"><span data-stu-id="e2b6a-170">Results of Step 1</span></span>

<span data-ttu-id="e2b6a-171">Pour vos Microsoft 365 d’entreprise, vous avez déterminé :</span><span class="sxs-lookup"><span data-stu-id="e2b6a-171">For your Microsoft 365 for enterprise tenants, you have determined:</span></span>

- <span data-ttu-id="e2b6a-172">Nombre de locataires dont vous avez ou avez besoin.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-172">How many tenants you have or need.</span></span>
- <span data-ttu-id="e2b6a-173">Pour chaque client, quels produits et licences doivent être achetés.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-173">For each tenant, which products and licenses must be purchased.</span></span>
- <span data-ttu-id="e2b6a-174">Indique si un client doit être multigéogé pour se conformer aux exigences de résidence des données.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-174">Whether a tenant needs to be Multi-Geo to comply with data residency requirements.</span></span>
- <span data-ttu-id="e2b6a-175">Si vous devez configurer la collaboration entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-175">Whether you need to set up inter-tenant collaboration.</span></span>
- <span data-ttu-id="e2b6a-176">Si vous devez migrer un client vers un autre.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-176">Whether you need to migrate one tenant to another.</span></span>
- <span data-ttu-id="e2b6a-177">Indique si vous devez déplacer des données principales d’une géo de centres de données vers une nouvelle.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-177">Whether you need to move core data from one datacenter geo to new one.</span></span>

<span data-ttu-id="e2b6a-178">Voici un exemple de nouveau client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-178">Here is an example of a new tenant.</span></span>

![Exemple de nouveau client](../media/tenant-management-overview/tenant-management-tenant-build-step1.png)

<span data-ttu-id="e2b6a-180">Dans cette illustration, le client a :</span><span class="sxs-lookup"><span data-stu-id="e2b6a-180">In this illustration, the tenant has:</span></span>

- <span data-ttu-id="e2b6a-181">Emplacement par défaut correspondant à une Microsoft 365 de centre de données.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-181">A default location corresponding to a Microsoft 365 datacenter geo.</span></span>
- <span data-ttu-id="e2b6a-182">Ensemble de produits et de licences.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-182">A set of products and licenses.</span></span>
- <span data-ttu-id="e2b6a-183">Ensemble d’applications de productivité cloud, dont certaines sont spécifiques aux produits.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-183">The set of cloud productivity apps, some of which are specific to products.</span></span>
- <span data-ttu-id="e2b6a-184">Un client Azure AD qui contient des comptes d’administrateur général et un nom de domaine DNS initial.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-184">An Azure AD tenant that contains global administrator accounts and an initial DNS domain name.</span></span>

<span data-ttu-id="e2b6a-185">Au fil des étapes supplémentaires de cette solution, nous allons créer cette figure.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-185">As we move through the additional steps of this solution, we will build out this figure.</span></span>

## <a name="ongoing-maintenance-for-tenants"></a><span data-ttu-id="e2b6a-186">Maintenance continue pour les locataires</span><span class="sxs-lookup"><span data-stu-id="e2b6a-186">Ongoing maintenance for tenants</span></span>

<span data-ttu-id="e2b6a-187">Régulièrement, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="e2b6a-187">On an ongoing basis, you might need to:</span></span>

- <span data-ttu-id="e2b6a-188">Ajoutez un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-188">Add a new tenant.</span></span>
- <span data-ttu-id="e2b6a-189">Ajoutez de nouveaux produits à un client avec un nombre initial de licences.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-189">Add new products to a tenant with an initial number of licenses.</span></span>
- <span data-ttu-id="e2b6a-190">Modifier l’ensemble des licences d’un produit dans un client pour ajuster les besoins du personnel.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-190">Change the set of licenses for a product in a tenant to adjust for changing staff requirements.</span></span>
- <span data-ttu-id="e2b6a-191">Déplacez vos données principales d’un client vers un nouvel emplacement géographique de centre de données.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-191">Move your core data from a tenant to a new datacenter geo location.</span></span>
- <span data-ttu-id="e2b6a-192">Ajoutez Multi-Géo pour les exigences de résidence des données.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-192">Add Multi-Geo for data residency requirements.</span></span>
- <span data-ttu-id="e2b6a-193">Configurer la collaboration entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-193">Set up inter-tenant collaboration.</span></span>

## <a name="next-step"></a><span data-ttu-id="e2b6a-194">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e2b6a-194">Next step</span></span>

<span data-ttu-id="e2b6a-195">[![Étape 2. Optimiser votre client pour l’accès au réseau](../media/tenant-management-overview/tenant-management-step-grid-networking.png)](tenant-management-networking.md)</span><span class="sxs-lookup"><span data-stu-id="e2b6a-195">[![Step 2. Optimize your tenant for network for access](../media/tenant-management-overview/tenant-management-step-grid-networking.png)](tenant-management-networking.md)</span></span>

<span data-ttu-id="e2b6a-196">Poursuivez la [mise en réseau](tenant-management-networking.md) pour fournir une mise en réseau optimale de vos employés Microsoft 365 services cloud.</span><span class="sxs-lookup"><span data-stu-id="e2b6a-196">Continue with [networking](tenant-management-networking.md) to provide optimal networking from your workers to Microsoft 365 cloud services.</span></span>
