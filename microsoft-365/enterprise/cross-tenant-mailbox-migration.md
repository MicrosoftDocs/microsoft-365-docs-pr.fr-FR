---
title: Migration de boîtes aux lettres inter-clients
description: Comment déplacer des boîtes aux lettres entre Microsoft 365 ou Office 365 client.
ms.author: josephd
author: JoeDavies-MSFT
manager: Laurawi
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.date: 09/21/2020
ms.reviewer: georgiah
ms.custom:
- it-pro
ms.collection:
- M365-subscription-management
ms.openlocfilehash: 018c47076642d4ce51340aed5fcb25c1d25c6b4f
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53289162"
---
# <a name="cross-tenant-mailbox-migration-preview"></a><span data-ttu-id="c7ef7-103">Migration de boîtes aux lettres entre locataires (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-103">Cross-tenant mailbox migration (preview)</span></span>

<span data-ttu-id="c7ef7-104">Auparavant, lorsqu’un client Exchange Online devait déplacer des boîtes aux lettres vers un autre client dans le même service Exchange Online, il devait les déboarder complètement sur site, puis les intégrer à un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-104">Previously, when an Exchange Online tenant needed to move mailboxes to another tenant in the same Exchange Online service, they would have to completely offboard them to on-premises and then onboard them to a new tenant.</span></span> <span data-ttu-id="c7ef7-105">Grâce à la nouvelle fonctionnalité de migration de boîtes aux lettres entre les locataires, les administrateurs client des locataires source et cible peuvent déplacer des boîtes aux lettres entre les locataires avec des dépendances d’infrastructure minimales dans leurs systèmes locaux.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-105">With the new cross-tenant mailbox migration feature, tenant administrators in both source and target tenants can move mailboxes between the tenants with minimal infrastructure dependencies in their on-premises systems.</span></span> <span data-ttu-id="c7ef7-106">Cela permet de supprimer la nécessité d’intégrer et d’intégrer des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-106">This removes the need to off-board and onboard mailboxes.</span></span>

<span data-ttu-id="c7ef7-107">En commun, lors de fusions ou de dédessons, vous avez besoin de la possibilité de déplacer des utilisateurs et du contenu vers un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-107">Commonly, during mergers or divestitures, you need the ability to move users and content into a new tenant.</span></span> <span data-ttu-id="c7ef7-108">Lorsque l’administrateur client cible exécute le déplacement, il s’agit d’un déplacement pull, semblable à l’intégration sur site aux migrations d’intégration cloud.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-108">When the target tenant administrator executes the move, it’s called a Pull move, similar to on-premises to cloud onboarding migrations.</span></span>

<span data-ttu-id="c7ef7-109">Les déplacements de boîtes aux lettres inter-clients Exchange sont entièrement libre-service par les administrateurs clients, à l’aide d’interfaces connues qui peuvent être scriptées dans les flux de travail plus volumineux nécessaires à la transition des utilisateurs vers leur nouvelle organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-109">Cross-tenant Exchange mailbox moves are fully self-serviced by tenant administrators, using well known interfaces that can be scripted into the larger workflows needed to transition users to their new organization.</span></span> <span data-ttu-id="c7ef7-110">Les administrateurs peuvent utiliser la cmdlet, disponible via le rôle de gestion Déplacer des boîtes aux lettres, pour exécuter des déplacements `New-MigrationBatch` entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-110">Administrators can use the `New-MigrationBatch` cmdlet, available through the Move Mailboxes management role, to execute cross-tenant moves.</span></span> <span data-ttu-id="c7ef7-111">Le processus de déplacement inclut les vérifications d’autorisation du client lors de la synchronisation et de la finalisation des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-111">The move process includes tenant authorization checks during mailbox synchronization and finalization.</span></span>

<span data-ttu-id="c7ef7-112">Les utilisateurs qui migrent doivent être présents dans le système d’Exchange Online client cible en tant que MailUsers, marqués avec des attributs spécifiques pour permettre les déplacements entre clients.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-112">Users migrating must be present in the target tenant Exchange Online system as MailUsers, marked with specific attributes to enable the cross-tenant moves.</span></span> <span data-ttu-id="c7ef7-113">Les déplacements du système échouent pour les utilisateurs qui ne sont pas correctement configurer dans le client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-113">The system will fail moves for users that are not properly set up in the target tenant.</span></span>

<span data-ttu-id="c7ef7-114">Lorsque les déplacements sont terminés, la boîte aux lettres système source est convertie en MailUser et l’adresse cible (affichée sous la marque ExternalEmailAddress dans Exchange) est estampillée avec l’adresse de routage vers le client de destination.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-114">When the moves are complete, the source system mailbox is converted to MailUser and the targetAddress (shown as ExternalEmailAddress in Exchange) is stamped with the routing address to the destination tenant.</span></span> <span data-ttu-id="c7ef7-115">Ce processus laisse l’utilisateur mailuser hérité dans le client source et autorise une période de coexistence et de routage du courrier.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-115">This process leaves the legacy MailUser in the source tenant, and allows for a period of co-existence and mail routing.</span></span> <span data-ttu-id="c7ef7-116">Lorsque les processus d’entreprise le permettent, le client source peut supprimer la source MailUser ou les convertir en contact de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-116">When business processes allow, the source tenant may remove the source MailUser or convert them to a mail contact.</span></span>

<span data-ttu-id="c7ef7-117">Les migrations Exchange boîtes aux lettres entre les locataires sont uniquement pris en charge pour les locataires hybrides ou en nuage, ou pour n’importe quelle combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-117">Cross-tenant Exchange mailbox migrations are supported for tenants in hybrid or cloud only, or any combination of the two.</span></span>

<span data-ttu-id="c7ef7-118">Cet article décrit le processus de déplacement de boîtes aux lettres entre les locataires et fournit des instructions sur la préparation des locataires sources et cibles pour le déplacement de contenu.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-118">This article describes the process for cross-tenant mailbox moves and provides guidance on how to prepare source and target tenants for the content move.</span></span>

## <a name="preparing-source-and-target-tenants"></a><span data-ttu-id="c7ef7-119">Préparation des locataires sources et cibles</span><span class="sxs-lookup"><span data-stu-id="c7ef7-119">Preparing source and target tenants</span></span>

<span data-ttu-id="c7ef7-120">La fonctionnalité de migration de boîtes aux lettres Exchange client nécessite une autorisation et une portée pour les migrations entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-120">The Cross-tenant Exchange mailbox migration feature requires authorization and scoping for cross-tenant migrations.</span></span> <span data-ttu-id="c7ef7-121">À l’aide de l’application Azure Enterprise et des solutions de stockage de coffre de clés, les administrateurs clients sont désormais habilités à gérer à la fois l’autorisation et l’portée des migrations de boîtes aux lettres Exchange Online d’un client à un autre.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-121">Using the Azure Enterprise application and Key Vault storage solutions, tenant admins are now empowered to manage both authorization and scoping of Exchange Online mailbox migrations from one tenant to another.</span></span> <span data-ttu-id="c7ef7-122">Les déplacements de boîtes aux lettres entre locataires prend en charge un modèle d’invitation et de consentement pour établir une application Azure Active Directory (Azure AD) utilisée pour l’authentification entre une paire de locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-122">Cross-tenant mailbox moves supports an invitation and consent model to establish an Azure Active Directory (Azure AD) application used for authentication between a tenant pair.</span></span> <span data-ttu-id="c7ef7-123">Des composants supplémentaires tels qu’une relation organisationnelle et un point de terminaison de migration sont également requis.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-123">Additional components such as an organization relationship and a migration endpoint are also required.</span></span>

<span data-ttu-id="c7ef7-124">Cette section n’inclut pas les étapes spécifiques requises pour préparer les objets utilisateur MailUser dans le répertoire cible, ni l’exemple de commande pour envoyer un lot de migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-124">This section does not include the specific steps required to prepare the MailUser user objects in the target directory, nor does it include the sample command to submit a migration batch.</span></span> <span data-ttu-id="c7ef7-125">Pour plus [d’informations, voir Préparer](#prepare-target-user-objects-for-migration) les objets utilisateur cibles pour la migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-125">Please see [Prepare target user objects for migration](#prepare-target-user-objects-for-migration) for this information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7ef7-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7ef7-126">Prerequisites</span></span>

<span data-ttu-id="c7ef7-127">La fonctionnalité de déplacement de boîtes aux lettres entre clients nécessite [Azure Key Vault](/azure/key-vault/basic-concepts) pour établir une application Azure propre à une paire de clients afin de stocker et d’accéder en toute sécurité au certificat/clé secrète utilisé pour authentifier et autoriser la migration de boîtes aux lettres d’un client à l’autre, supprimant ainsi toutes les conditions requises pour partager des certificats/clés secrètes entre les clients.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-127">The cross-tenant mailbox move feature requires [Azure Key Vault](/azure/key-vault/basic-concepts) to establish a tenant pair-specific Azure application to securely store and access the certificate/secret used to authenticate and authorize mailbox migration from one tenant to the other, removing any requirements to share certificates/secrets between tenants.</span></span>

<span data-ttu-id="c7ef7-128">Avant de commencer, assurez-vous que vous avez les autorisations nécessaires pour exécuter les scripts de déploiement afin de configurer Azure Key Vault, l’application de déplacement de boîte aux lettres, le point de terminaison de migration EXO et la relation d’organisation EXO.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-128">Before starting, be sure you have the necessary permissions to run the deployment scripts in order to configure Azure Key Vault, Move Mailbox application, EXO Migration Endpoint, and the EXO Organization Relationship.</span></span> <span data-ttu-id="c7ef7-129">En règle générale, l’administrateur général est autorisé à effectuer toutes les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-129">Typically, Global Admin has permission to perform all configuration steps.</span></span>

<span data-ttu-id="c7ef7-130">En outre, les groupes de sécurité à messagerie dans le client source sont requis avant l’exécution de l’installation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-130">Additionally, mail-enabled security groups in the source tenant are required prior to running setup.</span></span> <span data-ttu-id="c7ef7-131">Ces groupes sont utilisés pour cibler la liste des boîtes aux lettres qui peuvent passer du client source (ou parfois appelé ressource) au client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-131">These groups are used to scope the list of mailboxes that can move from source (or sometimes referred to as resource) tenant to the target tenant.</span></span> <span data-ttu-id="c7ef7-132">Cela permet à l’administrateur client source de restreindre ou d’étendue l’ensemble spécifique de boîtes aux lettres qui doivent être déplacées, ce qui empêche la migration des utilisateurs non voulus.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-132">This allows the source tenant admin to restrict or scope the specific set of mailboxes that need to be moved, preventing unintended users from being migrated.</span></span> <span data-ttu-id="c7ef7-133">Les groupes imbrmbrés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-133">Nested groups are not supported.</span></span>

<span data-ttu-id="c7ef7-134">Vous devrez également communiquer avec votre société partenaire de confiance (avec laquelle vous déplacerez des boîtes aux lettres) pour obtenir leur ID Microsoft 365 client approuvé.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-134">You will also need to communicate with your trusted partner company (with whom you will be moving mailboxes) to obtain their Microsoft 365 tenant ID.</span></span> <span data-ttu-id="c7ef7-135">Cet ID de client est utilisé dans le champ Relation `DomainName` d’organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-135">This tenant ID is used in the Organization Relationship `DomainName` field.</span></span>

<span data-ttu-id="c7ef7-136">Pour obtenir l’ID de locataire d’un abonnement, connectez-vous au Centre d’administration Microsoft 365 puis allez à [https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties) .</span><span class="sxs-lookup"><span data-stu-id="c7ef7-136">To obtain the tenant ID of a subscription, sign-in to the Microsoft 365 admin center and go to [https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties](https://aad.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Properties).</span></span> <span data-ttu-id="c7ef7-137">Cliquez sur l’icône de copie de la propriété ID de client pour la copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-137">Click the copy icon for the Tenant ID property to copy it to the clipboard.</span></span>

<span data-ttu-id="c7ef7-138">Voici comment fonctionne le processus.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-138">Here is how the process works.</span></span>

:::image type="content" source="../media/tenant-to-tenant-mailbox-move/prepare-tenants-flow.png" alt-text="Préparation du client pour la migration de boîtes aux lettres.":::

<span data-ttu-id="c7ef7-140">[Voir une version plus grande de cette image.](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/tenant-to-tenant-mailbox-move/prepare-tenants-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-140">[See a larger version of this image](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/tenant-to-tenant-mailbox-move/prepare-tenants-flow.png).</span></span>

<!--
[![Tenant preparation for mailbox migration](../media/tenant-to-tenant-mailbox-move/prepare-tenants-flow.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/tenant-to-tenant-mailbox-move/prepare-tenants-flow.png)
-->

### <a name="prepare-tenants"></a><span data-ttu-id="c7ef7-141">Préparer les locataires</span><span class="sxs-lookup"><span data-stu-id="c7ef7-141">Prepare tenants</span></span>

<span data-ttu-id="c7ef7-142">À un niveau élevé, les actions de configuration suivantes ont lieu lors de l’exécution des scripts d’installation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-142">At a high level, the following configuration actions take place when executing the setup scripts.</span></span>

<span data-ttu-id="c7ef7-143">Préparez le client cible :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-143">Prepare the target tenant:</span></span>

1. <span data-ttu-id="c7ef7-144">Si un groupe de ressources Azure existant n’est pas fourni, un nouveau groupe de ressources est créé (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-144">If an existing Azure Resource Group is not provided, a new one is created (SCRIPT).</span></span>
2. <span data-ttu-id="c7ef7-145">Si un coffre de clés existant n’est pas fourni, un nouveau coffre est créé (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-145">If an existing Key Vault is not provided, a new one is created (SCRIPT).</span></span>
3. <span data-ttu-id="c7ef7-146">Une nouvelle stratégie d’accès est créée pour l’application Office 365 Exchange Online migration de boîtes aux lettres (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-146">A new Access Policy is created for the Office 365 Exchange Online Mailbox Migration application (SCRIPT).</span></span>
4. <span data-ttu-id="c7ef7-147">Un nouveau certificat est créé (ou existant, s’il est spécifié) pour contenir la question secrète dans l’application de migration (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-147">A new certificate is created (or existing one, if specified) to hold the secret to the Migration application (SCRIPT).</span></span>
5. <span data-ttu-id="c7ef7-148">Une nouvelle application Azure AD est créée (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-148">A new Azure AD application is created (SCRIPT).</span></span>
6. <span data-ttu-id="c7ef7-149">Le certificat/la question secrète est téléchargé vers l’application de migration (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-149">The certificate/secret is uploaded to the migration application (SCRIPT).</span></span>
7. <span data-ttu-id="c7ef7-150">Les autorisations de migration de boîtes aux lettres sont affectées à l’application (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-150">Mailbox migration permissions are assigned to the application (SCRIPT).</span></span>
8. <span data-ttu-id="c7ef7-151">Le script de déploiement s’interrompt jusqu’à ce que l’administrateur cible consente à sa propre application (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-151">The deployment script pauses until target admin consents to their own application (SCRIPT).</span></span>
9. <span data-ttu-id="c7ef7-152">L’administrateur client cible consent aux autorisations accordées à l’application (MANUAL).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-152">The target tenant admin consents to the permissions given to the application (MANUAL).</span></span>
10. <span data-ttu-id="c7ef7-153">Une relation d’organisation est créée avec le client cible (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-153">An organization relationship is created to the target tenant (SCRIPT).</span></span>
11. <span data-ttu-id="c7ef7-154">Un point de terminaison de migration est créé pour tirer les boîtes aux lettres vers le client cible (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-154">A migration endpoint is created to pull mailboxes to the target tenant (SCRIPT).</span></span>

<span data-ttu-id="c7ef7-155">Préparez le client source :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-155">Prepare the source tenant:</span></span>

1. <span data-ttu-id="c7ef7-156">L’administrateur client source accepte le consentement à l’invitation de l’application de migration de boîtes aux lettres à partir du client cible (MANUAL).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-156">The source tenant admin accepts consent to Mailbox Migration application invitation from the Target tenant (MANUAL).</span></span>
2. <span data-ttu-id="c7ef7-157">L’administrateur client source crée un groupe de sécurité à messagerie dans son client pour contenir la liste des boîtes aux lettres autorisées à être déplacées par l’application de migration (MANUAL).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-157">The source tenant admin creates a mail-enabled security group in their tenant to contain the list of mailboxes allowed to be moved by the migration application (MANUAL).</span></span>
3. <span data-ttu-id="c7ef7-158">Une relation d’organisation est créée avec le client cible en spécifiant que l’application de migration de boîte aux lettres doit être utilisée pour la vérification OAuth afin d’accepter la demande de déplacement (SCRIPT).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-158">An organization relationship is created to the target tenant specifying the mailbox migration application should be used for OAuth verification to accept the move request (SCRIPT).</span></span>

#### <a name="step-by-step-instructions-for-the-target-tenant-admin"></a><span data-ttu-id="c7ef7-159">Instructions pas à pas pour l’administrateur client cible</span><span class="sxs-lookup"><span data-stu-id="c7ef7-159">Step-by-step instructions for the target tenant admin</span></span>

1. <span data-ttu-id="c7ef7-160">Téléchargez le script SetupCrossTenantRelationshipForTargetTenant.ps1 pour la configuration du client cible à partir du [référentiel GitHub.](https://github.com/microsoft/cross-tenant/releases/tag/Preview)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-160">Download the SetupCrossTenantRelationshipForTargetTenant.ps1 script for the target tenant setup from the [GitHub repository](https://github.com/microsoft/cross-tenant/releases/tag/Preview).</span></span>
2. <span data-ttu-id="c7ef7-161">Enregistrez le script (SetupCrossTenantRelationshipForTargetTenant.ps1) sur l’ordinateur à partir duquel vous allez exécuter le script.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-161">Save the script (SetupCrossTenantRelationshipForTargetTenant.ps1) to the computer from which you will be executing the script.</span></span>
3. <span data-ttu-id="c7ef7-162">Créez une connexion PowerShell distante au client Exchange Online cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-162">Create a Remote PowerShell connection to the Exchange Online target tenant.</span></span> <span data-ttu-id="c7ef7-163">Là encore, assurez-vous que vous avez les autorisations nécessaires pour exécuter les scripts de déploiement afin de configurer le certificat et le stockage Azure Key Vault, l’application de déplacement de boîte aux lettres, le point de terminaison de migration EXO et la relation d’organisation EXO.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-163">Again, make sure you have the necessary permissions to run the deployment scripts in order to configure the Azure Key Vault storage and certificate, Move Mailbox application, EXO Migration Endpoint, and the EXO Organization Relationship.</span></span>
4. <span data-ttu-id="c7ef7-164">Modifiez le répertoire du dossier de fichiers en emplacement de script ou vérifiez que le script est actuellement enregistré à l’emplacement actuellement dans votre session PowerShell distante.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-164">Change the file folder directory to the script location or verify the script is currently saved to the location currently in your Remote PowerShell session.</span></span>
5. <span data-ttu-id="c7ef7-165">Exécutez le script avec les valeurs et paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-165">Run the script with the following parameters and values.</span></span>

   |<span data-ttu-id="c7ef7-166">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c7ef7-166">Parameter</span></span>|<span data-ttu-id="c7ef7-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7ef7-167">Value</span></span>|<span data-ttu-id="c7ef7-168">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="c7ef7-168">Required or Optional</span></span>
   |---|---|---|
   |<span data-ttu-id="c7ef7-169">-TargetTenantDomain</span><span class="sxs-lookup"><span data-stu-id="c7ef7-169">-TargetTenantDomain</span></span>|<span data-ttu-id="c7ef7-170">Domaine client cible, tel que fabrikam \. onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-170">Target tenant domain, such as fabrikam\.onmicrosoft.com.</span></span>|<span data-ttu-id="c7ef7-171">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-171">Required</span></span>|
   |<span data-ttu-id="c7ef7-172">-ResourceTenantDomain</span><span class="sxs-lookup"><span data-stu-id="c7ef7-172">-ResourceTenantDomain</span></span>|<span data-ttu-id="c7ef7-173">Domaine client source, tel que contoso \. onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-173">Source tenant domain, such as contoso\.onmicrosoft.com.</span></span>|<span data-ttu-id="c7ef7-174">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-174">Required</span></span>|
   |<span data-ttu-id="c7ef7-175">-ResourceTenantAdminEmail</span><span class="sxs-lookup"><span data-stu-id="c7ef7-175">-ResourceTenantAdminEmail</span></span>|<span data-ttu-id="c7ef7-176">Adresse de messagerie de l’administrateur client source.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-176">Source tenant admin’s email address.</span></span> <span data-ttu-id="c7ef7-177">Il s’agit de l’administrateur client source qui consentira à l’utilisation de l’application de migration de boîte aux lettres envoyée par l’administrateur cible. Il s’agit de l’administrateur qui recevra l’invitation par courrier électronique pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-177">This is the source tenant admin who will be consenting to the use of the mailbox migration application sent from the target admin. This is the admin who will receive the email invite for the application.</span></span>|<span data-ttu-id="c7ef7-178">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-178">Required</span></span>|
   |<span data-ttu-id="c7ef7-179">-ResourceTenantId</span><span class="sxs-lookup"><span data-stu-id="c7ef7-179">-ResourceTenantId</span></span>|<span data-ttu-id="c7ef7-180">ID d’organisation client source (GUID).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-180">Source tenant organization ID (GUID).</span></span>|<span data-ttu-id="c7ef7-181">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-181">Required</span></span>|
   |<span data-ttu-id="c7ef7-182">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7ef7-182">-SubscriptionId</span></span>|<span data-ttu-id="c7ef7-183">L’abonnement Azure à utiliser pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-183">The Azure subscription to use for creating resources.</span></span>|<span data-ttu-id="c7ef7-184">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-184">Required</span></span>|
   |<span data-ttu-id="c7ef7-185">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7ef7-185">-ResourceGroup</span></span>|<span data-ttu-id="c7ef7-186">Nom du groupe de ressources Azure qui contient ou contiendra le coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-186">Azure resource group name that contains or will contain the Key Vault.</span></span>|<span data-ttu-id="c7ef7-187">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-187">Required</span></span>|
   |<span data-ttu-id="c7ef7-188">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="c7ef7-188">-KeyVaultName</span></span>|<span data-ttu-id="c7ef7-189">Instance Azure Key Vault qui stockera votre certificat/clé secrète d’application de migration de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-189">Azure Key Vault instance that will store your mailbox migration application certificate/secret.</span></span>|<span data-ttu-id="c7ef7-190">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-190">Required</span></span>|
   |<span data-ttu-id="c7ef7-191">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c7ef7-191">-CertificateName</span></span>|<span data-ttu-id="c7ef7-192">Nom du certificat lors de la génération ou de la recherche de certificat dans le coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-192">Certificate name when generating or searching for certificate in key vault.</span></span>|<span data-ttu-id="c7ef7-193">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-193">Required</span></span>|
   |<span data-ttu-id="c7ef7-194">-CertificateSubject</span><span class="sxs-lookup"><span data-stu-id="c7ef7-194">-CertificateSubject</span></span>|<span data-ttu-id="c7ef7-195">Nom d’objet du certificat Azure Key Vault, tel que CN=contoso_fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-195">Azure Key Vault certificate subject name, such as CN=contoso_fabrikam.</span></span>|<span data-ttu-id="c7ef7-196">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-196">Required</span></span>|
   |<span data-ttu-id="c7ef7-197">-AzureResourceLocation</span><span class="sxs-lookup"><span data-stu-id="c7ef7-197">-AzureResourceLocation</span></span>|<span data-ttu-id="c7ef7-198">Emplacement du groupe de ressources Azure et du coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-198">The location of the Azure resource group and key vault.</span></span>|<span data-ttu-id="c7ef7-199">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-199">Required</span></span>|
   |<span data-ttu-id="c7ef7-200">-ExistingApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7ef7-200">-ExistingApplicationId</span></span>|<span data-ttu-id="c7ef7-201">Application de migration de messagerie à utiliser si une application a déjà été créée.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-201">Mail migration application to use if one was already created.</span></span>|<span data-ttu-id="c7ef7-202">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c7ef7-202">Optional</span></span>|
   |<span data-ttu-id="c7ef7-203">-AzureAppPermissions</span><span class="sxs-lookup"><span data-stu-id="c7ef7-203">-AzureAppPermissions</span></span>|<span data-ttu-id="c7ef7-204">Autorisations requises pour l’application de migration de boîte aux lettres, telles que Exchange ou MSGraph (Exchange pour le déplacement de boîtes aux lettres, MSGraph pour l’utilisation de cette application pour envoyer une invitation de lien de consentement au client de ressource).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-204">The permissions required to be given to the mailbox migration application, such as Exchange or MSGraph (Exchange for moving mailboxes, MSGraph for using this application to send a consent link invitation to resource tenant).</span></span>|<span data-ttu-id="c7ef7-205">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c7ef7-205">Required</span></span>|
   |<span data-ttu-id="c7ef7-206">-UseAppAndCertGeneratedForSendingInvitation</span><span class="sxs-lookup"><span data-stu-id="c7ef7-206">-UseAppAndCertGeneratedForSendingInvitation</span></span>|<span data-ttu-id="c7ef7-207">Paramètre d’utilisation de l’application créée pour la migration à utiliser pour envoyer une invitation de lien de consentement à l’administrateur client source. S’il n’est pas présent, les informations d’identification de l’administrateur cible sont invités à se connecter au gestionnaire d’invitation Azure et à envoyer l’invitation en tant qu’administrateur cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-207">Parameter for using the application created for migration to be used for sending consent link invitation to source tenant admin. If not present this will prompt for the target admin’s credentials to connect to Azure invitation manager and send the invitation as target admin.</span></span>|<span data-ttu-id="c7ef7-208">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c7ef7-208">Optional</span></span>|
   |<span data-ttu-id="c7ef7-209">-KeyVaultAuditStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c7ef7-209">-KeyVaultAuditStorageAccountName</span></span>|<span data-ttu-id="c7ef7-210">Compte de stockage dans lequel les journaux d’audit du coffre de clés sont stockés.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-210">The storage account where Key Vault’s audit logs would be stored.</span></span>|<span data-ttu-id="c7ef7-211">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c7ef7-211">Optional</span></span>|
   |<span data-ttu-id="c7ef7-212">-KeyVaultAuditStorageResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7ef7-212">-KeyVaultAuditStorageResourceGroup</span></span>|<span data-ttu-id="c7ef7-213">Groupe de ressources qui contient le compte de stockage pour le stockage des journaux d’audit du coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-213">The resource group that contains the storage account for storing Key Vault audit logs.</span></span>|<span data-ttu-id="c7ef7-214">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c7ef7-214">Optional</span></span>|
   ||||

    > [!NOTE]
    > <span data-ttu-id="c7ef7-215">Assurez-vous que vous avez installé le module Azure AD PowerShell avant d’exécutez les scripts.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-215">Please ensure you have installed the Azure AD PowerShell module prior to running the scripts.</span></span> <span data-ttu-id="c7ef7-216">Reportez-vous [ici pour les étapes](/powershell/azure/install-az-ps) d’installation</span><span class="sxs-lookup"><span data-stu-id="c7ef7-216">Please refer to [here](/powershell/azure/install-az-ps) for installation steps</span></span>

6. <span data-ttu-id="c7ef7-217">Le script s’interrompt et vous demande d’accepter ou d’accepter l’application Exchange migration de boîtes aux lettres qui a été créée au cours de ce processus.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-217">The script will pause and ask you to accept or consent to the Exchange mailbox migration application that was created during this process.</span></span> <span data-ttu-id="c7ef7-218">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-218">Here is an example.</span></span>

    ```powershell
    PS C:\PowerShell\> # Note: the below User.Invite.All permission is optional, and will only be used to retrieve access token to send invitation email to source tenant
    PS C:\PowerShell\> .\SetupCrossTenantRelationshipForTargetTenant.ps1 -ResourceTenantDomain contoso.onmicrosoft.com -ResourceTenantAdminEmail admin@contoso.onmicrosoft.com -TargetTenantDomain fabrikam.onmicrosoft.com -ResourceTenantId ksagjid39-ede2-4d2c-98ae-874709325b00 -SubscriptionId e4ssd05d-a327-49ss-849a-sd0932439023 -ResourceGroup "Cross-TenantMoves" -KeyVaultName "Cross-TenantMovesVault" -CertificateName "Contoso-Fabrikam-cert" -CertificateSubject "CN=Contoso_Fabrikam" -AzureResourceLocation "Brazil Southeast" -AzureAppPermissions Exchange, MSGraph -UseAppAndCertGeneratedForSendingInvitation -KeyVaultAuditStorageAccountName "t2tstorageaccount" -KeyVaultAuditStorageResourceGroup "Demo"

    cmdlet Get-Credential at command pipeline position 1
    Supply values for the following parameters:
    Credential
    Setting up key vault in the fabrikam.onmicrosoft.com tenant

    Name                                     Account                                 SubscriptionName                        Environment                             TenantId
        ----                                     -------                                 ----------------                        -----------                             --------
    Pay-As-You-Go (ewe23423-a3327-34232-343... Admin@fabrikam... Pay-As-You-Go                           AzureCloud                              dsad938432-dd8e-s9034-bf9a-83984293n43
    Auditing setup successfully for Cross-TenantMovesVault
    Exchange application given access to KeyVault Cross-TenantMovesVault
    Application fabrikam_Friends_contoso_2520 created successfully in fabrikam.onmicrosoft.com tenant with following permissions. MSGraph - User.Invite.All. Exchange - Mailbox.Migration
    Admin consent URI for fabrikam.onmicrosoft.com tenant admin is -
    https://login.microsoftonline.com/fabrikam.onmicrosoft.com/adminconsent?client_id=6fea6ere-0dwe-404d-ad35-c71a15cers5c&redirect_uri=https://office.com
    Admin consent URI for contoso.onmicrosoft.com tenant admin is -
    https://login.microsoftonline.com/contoso.onmicrosoft.com/adminconsent?client_id=6fea6ssd-0753-404d-wer5-c71a154d675c&redirect_uri=https://office.com
    Application details to be registered in organization relationship: ApplicationId: [ 6fes8en4-sjo3-406d-ad35-sldkfjiew993 ]. KeyVault secret Id: [ https://cross-tenantmovesvault.vault.azure.net:443/certificates/Contoso-Fabrikam-cert/ksdfj843nt8476h84c288c5a3fb8ec5fdb08 ]. These values are available in variables $AppId and $CertificateId respectively
    Please consent to the application for fabrikam.onmicrosoft.com before sending invitation to admin@contoso.onmicrosoft.com:
    ```

7. <span data-ttu-id="c7ef7-219">Une URL s’affiche dans la session PowerShell distante.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-219">A URL will be displayed in the Remote PowerShell session.</span></span> <span data-ttu-id="c7ef7-220">Copiez le lien fourni pour le consentement de votre client et collez-le dans un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-220">Copy the link provided for your tenant consent and paste it into a Web browser.</span></span>

8. <span data-ttu-id="c7ef7-221">Connectez-vous avec vos informations d’identification d’administrateur global.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-221">Sign in with your Global Admin credentials.</span></span> <span data-ttu-id="c7ef7-222">Lorsque l’écran suivant est présenté, sélectionnez **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-222">When the following screen is presented, select **Accept**.</span></span>

    :::image type="content" source="../media/tenant-to-tenant-mailbox-move/permissions-requested-dialog.png" alt-text="Boîte de dialogue Accepter les autorisations":::

9. <span data-ttu-id="c7ef7-224">Revenir à la session PowerShell distante et accéder à Entrée pour continuer.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-224">Switch back to the Remote PowerShell session and hit Enter to proceed.</span></span>

10. <span data-ttu-id="c7ef7-225">Le script configure les objets d’installation restants.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-225">The script will configure the remaining setup objects.</span></span> <span data-ttu-id="c7ef7-226">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-226">Here is an example.</span></span>

    ```powershell
    Successfully sent invitation to admin@contoso.onmicrosoft.com
    Setting up exchange components on target tenant: fabrikam.onmicrosoft.com
    MigrationEndpoint created in fabrikam.onmicrosoft.com for target contoso.onmicrosoft.com
    Exchange setup complete. Migration endpoint details are available in $MigrationEndpoint variable
    ```

<span data-ttu-id="c7ef7-227">La configuration de l’administrateur cible est maintenant terminée !</span><span class="sxs-lookup"><span data-stu-id="c7ef7-227">The target admin setup is now complete!</span></span>

#### <a name="step-by-step-instructions-for-the-source-tenant-admin"></a><span data-ttu-id="c7ef7-228">Instructions pas à pas pour l’administrateur client source</span><span class="sxs-lookup"><span data-stu-id="c7ef7-228">Step-by-step instructions for the source tenant admin</span></span>

1. <span data-ttu-id="c7ef7-229">Connectez-vous à votre boîte aux lettres en tant que -ResourceTenantAdminEmail spécifié par l’administrateur cible lors de sa configuration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-229">Sign in to your mailbox as the -ResourceTenantAdminEmail specified by the target admin during their setup.</span></span> <span data-ttu-id="c7ef7-230">Recherchez l’invitation par courrier électronique à partir du client cible, puis sélectionnez **Prise en main** bouton.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-230">Find the email invitation from the target tenant, and then select the **Get Started** button.</span></span>

    :::image type="content" source="../media/tenant-to-tenant-mailbox-move/invited-by-target-tenant.png" alt-text="Boîte de dialogue Vous avez été invité":::

2. <span data-ttu-id="c7ef7-232">Sélectionnez **Accepter** pour accepter l’invitation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-232">Select **Accept** to accept the invitation.</span></span>

    :::image type="content" source="../media/tenant-to-tenant-mailbox-move/permissions-requested-accept.png" alt-text="Boîte de dialogue pour accepter les autorisations":::

   > [!NOTE]
   > <span data-ttu-id="c7ef7-234">Si vous ne recevez pas cet e-mail ou si vous ne le trouvez pas, l’administrateur client cible a reçu une URL directe qui peut vous être fournie pour accepter l’invitation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-234">If you do not get this email or cannot find it, the target tenant admin was provided a direct URL that can be given to you to accept the invitation.</span></span> <span data-ttu-id="c7ef7-235">L’URL doit être dans la transcription de la session PowerShell distante de l’administrateur client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-235">The URL should in the in the transcript of the target tenant admin's Remote PowerShell session.</span></span>

3. <span data-ttu-id="c7ef7-236">Dans la session Centre d’administration Microsoft 365 ou une session PowerShell distante, créez un ou plusieurs groupes de sécurité à messagerie pour contrôler la liste des boîtes aux lettres autorisées par le client cible à tirer (déplacer) du client source vers le client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-236">In either the Microsoft 365 admin center or a Remote PowerShell session, create one or more mail-enabled security groups to control the list of mailboxes allowed by the target tenant to pull (move) from the source tenant to the target tenant.</span></span> <span data-ttu-id="c7ef7-237">Vous n’avez pas besoin de remplir ce groupe à l’avance, mais au moins un groupe doit être fourni pour exécuter les étapes de configuration (script).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-237">You do not need to populate this group in advance, but at least one group must be provided to run the setup steps (script).</span></span> <span data-ttu-id="c7ef7-238">Les groupes d’imbrouillement ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-238">Nest groups are not supported.</span></span>

4. <span data-ttu-id="c7ef7-239">Téléchargez le script SetupCrossTenantRelationshipForResourceTenant.ps1 pour la configuration du client source à partir du GitHub de données ici [https://github.com/microsoft/cross-tenant/releases/tag/Preview](https://github.com/microsoft/cross-tenant/releases/tag/Preview) :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-239">Download the SetupCrossTenantRelationshipForResourceTenant.ps1 script for the source tenant setup from the GitHub repository here: [https://github.com/microsoft/cross-tenant/releases/tag/Preview](https://github.com/microsoft/cross-tenant/releases/tag/Preview).</span></span>

5. <span data-ttu-id="c7ef7-240">Créez une connexion PowerShell distante au client source avec vos autorisations Exchange administrateur.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-240">Create a Remote PowerShell connection to the source tenant with your Exchange Administrator permissions.</span></span> <span data-ttu-id="c7ef7-241">Les autorisations d’administrateur global ne sont pas nécessaires pour configurer le client source, uniquement le client cible en raison du processus de création d’application Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-241">Global Admin permissions are not required to configure the source tenant, only the target tenant because of the Azure application creation process.</span></span>

6. <span data-ttu-id="c7ef7-242">Modifiez le répertoire vers l’emplacement du script ou vérifiez que le script est actuellement enregistré à l’emplacement actuellement dans votre session PowerShell distante.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-242">Change directory to the script location or verify that the script is currently saved to the location currently in your Remote PowerShell session.</span></span>

7. <span data-ttu-id="c7ef7-243">Exécutez le script avec les valeurs et paramètres requis suivants.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-243">Run the script with the following required parameters and values.</span></span>

   |<span data-ttu-id="c7ef7-244">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c7ef7-244">Parameter</span></span>|<span data-ttu-id="c7ef7-245">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7ef7-245">Value</span></span>|
   |---|---|
   |<span data-ttu-id="c7ef7-246">-SourceMailboxMovePublishedScopes</span><span class="sxs-lookup"><span data-stu-id="c7ef7-246">-SourceMailboxMovePublishedScopes</span></span>|<span data-ttu-id="c7ef7-247">Groupe de sécurité à messagerie créé par le client source pour les identités/boîtes aux lettres qui sont dans l’étendue de la migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-247">Mail-enabled security group created by source tenant for the identities/mailboxes that are in scope for migration.</span></span>|
   |<span data-ttu-id="c7ef7-248">-ResourceTenantDomain</span><span class="sxs-lookup"><span data-stu-id="c7ef7-248">-ResourceTenantDomain</span></span>|<span data-ttu-id="c7ef7-249">Nom de domaine du client source, tel que contoso \. onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-249">Source tenant domain name, such as contoso\.onmicrosoft.com.</span></span>|
   |<span data-ttu-id="c7ef7-250">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7ef7-250">-ApplicationId</span></span>|<span data-ttu-id="c7ef7-251">ID d’application Azure (GUID) de l’application utilisée pour la migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-251">Azure application ID (GUID) of the application used for migration.</span></span> <span data-ttu-id="c7ef7-252">ID d’application disponible via votre portail Azure (Azure AD, Enterprise Applications, nom de l’application, ID d’application) ou inclus dans votre courrier électronique d’invitation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-252">Application ID available via your Azure portal (Azure AD, Enterprise Applications, app name, application ID) or included in your invitation email.</span></span>|
   |<span data-ttu-id="c7ef7-253">-TargetTenantDomain</span><span class="sxs-lookup"><span data-stu-id="c7ef7-253">-TargetTenantDomain</span></span>|<span data-ttu-id="c7ef7-254">Nom de domaine du client cible, tel que fabrikam \. onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-254">Target tenant domain name, such as fabrikam\.onmicrosoft.com.</span></span>|
   |<span data-ttu-id="c7ef7-255">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="c7ef7-255">-TargetTenantId</span></span>|<span data-ttu-id="c7ef7-256">ID de client du client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-256">Tenant ID of the target tenant.</span></span> <span data-ttu-id="c7ef7-257">Par exemple, l’ID de client Azure AD de contoso \. onmicrosoft.com client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-257">For example, the Azure AD tenant ID of contoso\.onmicrosoft.com tenant.</span></span>|
   |||

    <span data-ttu-id="c7ef7-258">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-258">Here is an example.</span></span>

    ```powershell
    SetupCrossTenantRelationshipForResourceTenant.ps1 -SourceMailboxMovePublishedScopes "MigScope","MyGroup" -ResourceTenantDomain contoso.onmicrosoft.com -TargetTenantDomain fabrikam.onmicrosoft.com -ApplicationId sdf5e87sa-0753-dd88-ad35-c71a15cs8e44c -TargetTenantId 4sdkfo933-3904-sd93-bf9a-sdi39402834
    Exchange setup complete.
    ```

<span data-ttu-id="c7ef7-259">La configuration de l’administrateur source est maintenant terminée !</span><span class="sxs-lookup"><span data-stu-id="c7ef7-259">The source admin setup is now complete!</span></span>

### <a name="verify-setup"></a><span data-ttu-id="c7ef7-260">Vérifier la configuration</span><span class="sxs-lookup"><span data-stu-id="c7ef7-260">Verify setup</span></span>

<span data-ttu-id="c7ef7-261">Vérifiez que les relations d’organisation dans les clients source et cible et le point de terminaison de migration dans la cible ont été correctement créées.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-261">Verify that the organization relationships in both source and target tenants and migration endpoint in the target were created successfully.</span></span>

#### <a name="target-tenant"></a><span data-ttu-id="c7ef7-262">Client cible</span><span class="sxs-lookup"><span data-stu-id="c7ef7-262">Target tenant</span></span>

##### <a name="organization-relationship"></a><span data-ttu-id="c7ef7-263">Relation organisationnelle</span><span class="sxs-lookup"><span data-stu-id="c7ef7-263">Organization relationship</span></span>

<span data-ttu-id="c7ef7-264">Vérifiez que l’objet relation organisationnelle a été créé et configuré avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-264">Verify that the organization relationship object was created and configured with this command.</span></span>

```powershell
Get-OrganizationRelationship <source tenant organization name> | fl name, DomainNames, MailboxMoveEnabled, MailboxMoveCapability
```
<span data-ttu-id="c7ef7-265">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-265">Here is an example:</span></span>

```powershell
PS C:\PowerShell\> Get-OrganizationRelationship fabrikam_contoso_1178 | fl name, DomainNames, MailboxMoveEnabled, MailboxMoveCapability

Name                  : fabrikam_contoso_1123
DomainNames           : {sd0933me9f-9304-s903-s093-s093mfi903m4}
MailboxMoveEnabled    : True
MailboxMoveCapability : Inbound
```

##### <a name="migration-endpoint"></a><span data-ttu-id="c7ef7-266">Point de terminaison de migration</span><span class="sxs-lookup"><span data-stu-id="c7ef7-266">Migration endpoint</span></span>

<span data-ttu-id="c7ef7-267">Vérifiez que l’objet de point de terminaison de migration a été créé et configuré avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-267">Verify that the migration endpoint object was created and configured with this command.</span></span>

```powershell
Get-MigrationEndpoint "<fabrikam_contoso_1123> | fl Identity, RemoteTenant, ApplicationId, AppSecretKeyVaultUrl
```

<span data-ttu-id="c7ef7-268">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-268">Here is an example.</span></span>

```powershell
PS C:\PowerShell\> Get-MigrationEndpoint fabrikam_contoso_1123 | fl Identity, RemoteTenant, ApplicationId, AppSecretKeyVaultUrl


Identity             : fabrikam_contoso_1123
RemoteTenant         : contoso.onmicrosoft.com
ApplicationId        : s93mf93-das9-dq24-dq234-dada9033904m
AppSecretKeyVaultUrl : https://cross-tenantmyvaultformoves.vault.azure.net:443/certificates/Contoso-Fabrikam-cert/ae79348mx94384c288c5a3dfsioepw308
```

#### <a name="source-tenant"></a><span data-ttu-id="c7ef7-269">Client source</span><span class="sxs-lookup"><span data-stu-id="c7ef7-269">Source tenant</span></span>

##### <a name="organization-relationship"></a><span data-ttu-id="c7ef7-270">Relation organisationnelle</span><span class="sxs-lookup"><span data-stu-id="c7ef7-270">Organization relationship</span></span>

<span data-ttu-id="c7ef7-271">Vérifiez que l’objet relation organisationnelle a été créé et configuré avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-271">Verify that the organization relationship object was created and configured with this command.</span></span>

```powershell
Get-OrganizationRelationship | fl name, MailboxMoveEnabled, MailboxMoveCapability, MailboxMovePublishedScopes, OAuthApplicationId
```

<span data-ttu-id="c7ef7-272">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-272">Here is an example.</span></span>

```powershell
PS C:\PowerShell\> Get-OrganizationRelationship | fl name, MailboxMoveEnabled, MailboxMoveCapability, MailboxMovePublishedScopes, OAuthApplicationId


Name                       : fabrikam_contoso_001
MailboxMoveEnabled         : True
MailboxMoveCapability      : RemoteOutbound
MailboxMovePublishedScopes : {MigScope}
OAuthApplicationId         : sd9890342-3243-3242-fe3w2-fsdade93m0
```

#### <a name="verify-setup-script"></a><span data-ttu-id="c7ef7-273">Vérifier le script d’installation</span><span class="sxs-lookup"><span data-stu-id="c7ef7-273">Verify Setup Script</span></span>

<span data-ttu-id="c7ef7-274">Si vous recevez des erreurs lors de la configuration des locataires source ou cible, vous pouvez exécuter le script VerifySetup.ps1 situé sur [GitHub](https://github.com/microsoft/cross-tenant/releases/tag/Preview) et passer en revue la sortie.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-274">If you receive any errors during the configuration of the source or target tenants, you can run the VerifySetup.ps1 script located [on GitHub](https://github.com/microsoft/cross-tenant/releases/tag/Preview) and review the output.</span></span>

<span data-ttu-id="c7ef7-275">Voici un exemple d’exécution de VerifySetup.ps1 sur le client cible :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-275">Here's an example of running VerifySetup.ps1 on the target tenant:</span></span>

```powershell
VerifySetup.ps1 -PartnerTenantId <SourceTenantId> -ApplicationId <AADApplicationId> -ApplicationKeyVaultUrl <appKeyVaultUrl> -PartnerTenantDomain <PartnerTenantDomain> -Verbose
```

<span data-ttu-id="c7ef7-276">Voici un exemple d'VerifySetup.ps1 sur le client source :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-276">Here's an example of VerifySetup.ps1 on the source tenant:</span></span>

```powershell
VerifySetup.ps1 -PartnerTenantId <TargetTenantId> -ApplicationId <AADApplicationId>
```

### <a name="move-mailboxes-back-to-the-original-source"></a><span data-ttu-id="c7ef7-277">Déplacer les boîtes aux lettres vers la source d’origine</span><span class="sxs-lookup"><span data-stu-id="c7ef7-277">Move mailboxes back to the original source</span></span>

<span data-ttu-id="c7ef7-278">Si un déplacement de boîte aux lettres vers le client source d’origine est nécessaire, le même ensemble d’étapes et de scripts devra être exécuté dans les nouveaux locataires source et cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-278">If a mailbox move back to the original source tenant is required, the same set of steps and scripts will need to be run in both new source and new target tenants.</span></span> <span data-ttu-id="c7ef7-279">L’objet Relation d’organisation existant sera mis à jour ou mis à jour, et non recréé.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-279">The existing Organization Relationship object will be updated or appended, not recreated.</span></span>

## <a name="prepare-target-user-objects-for-migration"></a><span data-ttu-id="c7ef7-280">Préparer les objets utilisateur cibles pour la migration</span><span class="sxs-lookup"><span data-stu-id="c7ef7-280">Prepare target user objects for migration</span></span>

<span data-ttu-id="c7ef7-281">Les utilisateurs qui migrent doivent être présents dans le client cible et le système Exchange Online (en tant que MailUsers) marqués avec des attributs spécifiques pour activer les déplacements entre clients.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-281">Users migrating must be present in the target tenant and Exchange Online system (as MailUsers) marked with specific attributes to enable the cross-tenant moves.</span></span> <span data-ttu-id="c7ef7-282">Les déplacements du système échouent pour les utilisateurs qui ne sont pas correctement configurer dans le client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-282">The system will fail moves for users that are not properly set up in the target tenant.</span></span> <span data-ttu-id="c7ef7-283">La section suivante détaille les conditions requises pour l’objet MailUser pour le client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-283">The following section details the MailUser object requirements for the target tenant.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c7ef7-284">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7ef7-284">Prerequisites</span></span>

<span data-ttu-id="c7ef7-285">Vous devez vous assurer que les objets et attributs suivants sont définies dans l’organisation cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-285">You must ensure the following objects and attributes are set in the target organization.</span></span>

1. <span data-ttu-id="c7ef7-286">Pour toute boîte aux lettres qui se déplace à partir d’une organisation source, vous devez mettre en service un objet MailUser dans l’organisation cible :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-286">For any mailbox moving from a source organization, you must provision a MailUser object in the Target organization:</span></span>

   - <span data-ttu-id="c7ef7-287">L’utilisateur de messagerie cible doit avoir les attributs de la boîte aux lettres source ou affectés avec le nouvel objet User :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-287">The Target MailUser must have these attributes from the source mailbox or assigned with the new User object:</span></span>
      - <span data-ttu-id="c7ef7-288">ExchangeGUID (flux direct de la source à la cible) : le GUID de boîte aux lettres doit correspondre.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-288">ExchangeGUID (direct flow from source to target) – The mailbox GUID must match.</span></span> <span data-ttu-id="c7ef7-289">Le processus de déplacement ne se poursuit pas s’il n’est pas présent sur l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-289">The move process will not proceed if this is not present on target object.</span></span>
      - <span data-ttu-id="c7ef7-290">ArchiveGUID (flux direct de la source à la cible) : le GUID d’archivage doit correspondre.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-290">ArchiveGUID (direct flow from source to target) – The archive GUID must match.</span></span> <span data-ttu-id="c7ef7-291">Le processus de déplacement ne se poursuit pas s’il n’est pas présent sur l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-291">The move process will not proceed if this is not present on the target object.</span></span> <span data-ttu-id="c7ef7-292">(Cette demande est requise uniquement si la boîte aux lettres source est activée pour l’archivage).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-292">(This is only required if the source mailbox is Archive enabled).</span></span>
      - <span data-ttu-id="c7ef7-293">LegacyExchangeDN (flow as proxyAddress, « x500: « ) : LegacyExchangeDN doit être présent sur la cible MailUser en tant que <LegacyExchangeDN> x500 : proxyAddress.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-293">LegacyExchangeDN (flow as proxyAddress, “x500:<LegacyExchangeDN>”) – The LegacyExchangeDN must be present on target MailUser as x500: proxyAddress.</span></span> <span data-ttu-id="c7ef7-294">Le processus de déplacement ne se poursuit pas s’il n’est pas présent sur l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-294">The move processes will not proceed if this is not present on the target object.</span></span>
      - <span data-ttu-id="c7ef7-295">UserPrincipalName : UPN s’alignera sur la nouvelle identité ou la société cible de l’utilisateur (par exemple, user@northwindtraders.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-295">UserPrincipalName – UPN will align to the user’s NEW identity or target company (for example, user@northwindtraders.onmicrosoft.com).</span></span>
      - <span data-ttu-id="c7ef7-296">Adresse SMTP principale : l’adresse SMTP principale s’alignera sur la société NEW de l’utilisateur (par exemple, user@northwind.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-296">Primary SMTPAddress – Primary SMTP address will align to the user’s NEW company (for example, user@northwind.com).</span></span>
      - <span data-ttu-id="c7ef7-297">TargetAddress/ExternalEmailAddress : MailUser référencera la boîte aux lettres actuelle de l’utilisateur hébergée dans le client source (par exemple, user@contoso.onmicrosoft.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-297">TargetAddress/ExternalEmailAddress – MailUser will reference the user’s current mailbox hosted in source tenant (for example user@contoso.onmicrosoft.com).</span></span> <span data-ttu-id="c7ef7-298">Lors de l’affectation de cette valeur, vérifiez que vous avez/attribuez également PrimarySMTPAddress, sinon cette valeur définira PrimarySMTPAddress qui provoquera des échecs de déplacement.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-298">When assigning this value, verify that you have/are also assigning PrimarySMTPAddress or this value will set the PrimarySMTPAddress which will cause move failures.</span></span>
      - <span data-ttu-id="c7ef7-299">Vous ne pouvez pas ajouter des adresses proxy smtp héritées à partir de la boîte aux lettres source à la cible MailUser.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-299">You cannot add legacy smtp proxy addresses from source mailbox to target MailUser.</span></span> <span data-ttu-id="c7ef7-300">Par exemple, vous ne pouvez pas conserver contoso.com sur l’fabrikam.onmicrosoft.com des objets client).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-300">For example, you cannot maintain contoso.com on the MEU in fabrikam.onmicrosoft.com tenant objects).</span></span> <span data-ttu-id="c7ef7-301">Les domaines sont associés à un seul client Azure AD Exchange Online client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-301">Domains are associated with one Azure AD or Exchange Online tenant only.</span></span>

     <span data-ttu-id="c7ef7-302">Exemple **d’objet** MailUser cible :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-302">Example **target** MailUser object:</span></span>

     |<span data-ttu-id="c7ef7-303">Attribut</span><span class="sxs-lookup"><span data-stu-id="c7ef7-303">Attribute</span></span>|<span data-ttu-id="c7ef7-304">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7ef7-304">Value</span></span>|
     |---|---|
     |<span data-ttu-id="c7ef7-305">Alias</span><span class="sxs-lookup"><span data-stu-id="c7ef7-305">Alias</span></span>|<span data-ttu-id="c7ef7-306">LaraN</span><span class="sxs-lookup"><span data-stu-id="c7ef7-306">LaraN</span></span>|
     |<span data-ttu-id="c7ef7-307">RecipientType</span><span class="sxs-lookup"><span data-stu-id="c7ef7-307">RecipientType</span></span>|<span data-ttu-id="c7ef7-308">MailUser</span><span class="sxs-lookup"><span data-stu-id="c7ef7-308">MailUser</span></span>|
     |<span data-ttu-id="c7ef7-309">RecipientTypeDetails</span><span class="sxs-lookup"><span data-stu-id="c7ef7-309">RecipientTypeDetails</span></span>|<span data-ttu-id="c7ef7-310">MailUser</span><span class="sxs-lookup"><span data-stu-id="c7ef7-310">MailUser</span></span>|
     |<span data-ttu-id="c7ef7-311">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c7ef7-311">UserPrincipalName</span></span>|<span data-ttu-id="c7ef7-312">LaraN@northwintraders.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-312">LaraN@northwintraders.onmicrosoft.com</span></span>|
     |<span data-ttu-id="c7ef7-313">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c7ef7-313">PrimarySmtpAddress</span></span>|<span data-ttu-id="c7ef7-314">Lara.Newton@northwind.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-314">Lara.Newton@northwind.com</span></span>|
     |<span data-ttu-id="c7ef7-315">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c7ef7-315">ExternalEmailAddress</span></span>|<span data-ttu-id="c7ef7-316">SMTP:LaraN@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-316">SMTP:LaraN@contoso.onmicrosoft.com</span></span>|
     |<span data-ttu-id="c7ef7-317">ExchangeGuid</span><span class="sxs-lookup"><span data-stu-id="c7ef7-317">ExchangeGuid</span></span>|<span data-ttu-id="c7ef7-318">1ec059c7-8396-4d0b-af4e-d6bd4c12a8d8</span><span class="sxs-lookup"><span data-stu-id="c7ef7-318">1ec059c7-8396-4d0b-af4e-d6bd4c12a8d8</span></span>|
     |<span data-ttu-id="c7ef7-319">LegacyExchangeDN</span><span class="sxs-lookup"><span data-stu-id="c7ef7-319">LegacyExchangeDN</span></span>|<span data-ttu-id="c7ef7-320">/o=First Organization/ou=Exchange Administrative Group</span><span class="sxs-lookup"><span data-stu-id="c7ef7-320">/o=First Organization/ou=Exchange Administrative Group</span></span>|
     ||<span data-ttu-id="c7ef7-321">(FYDIBOHF23SPDLT)/cn=Recipients/cn=74e5385fce4b46d19006876949855035Lara</span><span class="sxs-lookup"><span data-stu-id="c7ef7-321">(FYDIBOHF23SPDLT)/cn=Recipients/cn=74e5385fce4b46d19006876949855035Lara</span></span>|
     |<span data-ttu-id="c7ef7-322">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="c7ef7-322">EmailAddresses</span></span>|<span data-ttu-id="c7ef7-323">x500:/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c8190</span><span class="sxs-lookup"><span data-stu-id="c7ef7-323">x500:/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c8190</span></span>|
     ||<span data-ttu-id="c7ef7-324">7273f1f9-Lara</span><span class="sxs-lookup"><span data-stu-id="c7ef7-324">7273f1f9-Lara</span></span>|
     ||<span data-ttu-id="c7ef7-325">smtp:LaraN@northwindtraders.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-325">smtp:LaraN@northwindtraders.onmicrosoft.com</span></span>|
     ||<span data-ttu-id="c7ef7-326">SMTP:Lara.Newton@northwind.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-326">SMTP:Lara.Newton@northwind.com</span></span>|
     |||

     <span data-ttu-id="c7ef7-327">Exemple **d’objet mailbox** source :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-327">Example **source** Mailbox object:</span></span>

     |<span data-ttu-id="c7ef7-328">Attribut</span><span class="sxs-lookup"><span data-stu-id="c7ef7-328">Attribute</span></span>|<span data-ttu-id="c7ef7-329">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7ef7-329">Value</span></span>|
     |---|---|
     |<span data-ttu-id="c7ef7-330">Alias</span><span class="sxs-lookup"><span data-stu-id="c7ef7-330">Alias</span></span>|<span data-ttu-id="c7ef7-331">LaraN</span><span class="sxs-lookup"><span data-stu-id="c7ef7-331">LaraN</span></span>|
     |<span data-ttu-id="c7ef7-332">RecipientType</span><span class="sxs-lookup"><span data-stu-id="c7ef7-332">RecipientType</span></span>|<span data-ttu-id="c7ef7-333">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="c7ef7-333">UserMailbox</span></span>|
     |<span data-ttu-id="c7ef7-334">RecipientTypeDetails</span><span class="sxs-lookup"><span data-stu-id="c7ef7-334">RecipientTypeDetails</span></span>|<span data-ttu-id="c7ef7-335">UserMailbox</span><span class="sxs-lookup"><span data-stu-id="c7ef7-335">UserMailbox</span></span>|
     |<span data-ttu-id="c7ef7-336">UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c7ef7-336">UserPrincipalName</span></span>|<span data-ttu-id="c7ef7-337">LaraN@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-337">LaraN@contoso.onmicrosoft.com</span></span>|
     |<span data-ttu-id="c7ef7-338">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c7ef7-338">PrimarySmtpAddress</span></span>|<span data-ttu-id="c7ef7-339">Lara.Newton@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-339">Lara.Newton@contoso.com</span></span>|
     |<span data-ttu-id="c7ef7-340">ExchangeGuid</span><span class="sxs-lookup"><span data-stu-id="c7ef7-340">ExchangeGuid</span></span>|<span data-ttu-id="c7ef7-341">1ec059c7-8396-4d0b-af4e-d6bd4c12a8d8</span><span class="sxs-lookup"><span data-stu-id="c7ef7-341">1ec059c7-8396-4d0b-af4e-d6bd4c12a8d8</span></span>|
     |<span data-ttu-id="c7ef7-342">LegacyExchangeDN</span><span class="sxs-lookup"><span data-stu-id="c7ef7-342">LegacyExchangeDN</span></span>|<span data-ttu-id="c7ef7-343">/o=First Organization/ou=Exchange Administrative Group</span><span class="sxs-lookup"><span data-stu-id="c7ef7-343">/o=First Organization/ou=Exchange Administrative Group</span></span>|
     ||<span data-ttu-id="c7ef7-344">(FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c81907273f1f9Lara</span><span class="sxs-lookup"><span data-stu-id="c7ef7-344">(FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c81907273f1f9Lara</span></span>|
     |<span data-ttu-id="c7ef7-345">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="c7ef7-345">EmailAddresses</span></span>|<span data-ttu-id="c7ef7-346">smtp:LaraN@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-346">smtp:LaraN@contoso.onmicrosoft.com</span></span>
     ||<span data-ttu-id="c7ef7-347">SMTP:Lara.Newton@contoso.com</span><span class="sxs-lookup"><span data-stu-id="c7ef7-347">SMTP:Lara.Newton@contoso.com</span></span>|
     |||

   - <span data-ttu-id="c7ef7-348">Des attributs supplémentaires peuvent déjà être inclus dans Exchange’écriture hybride.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-348">Additional attributes may be included in Exchange hybrid write back already.</span></span> <span data-ttu-id="c7ef7-349">Si ce n’est pas le cas, elles doivent être incluses.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-349">If not, they should be included.</span></span>
   - <span data-ttu-id="c7ef7-350">msExchBlockedSendersHash : écrit en ligne les données d’expéditeurs sécurisés et bloqués des clients vers Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-350">msExchBlockedSendersHash – Writes back online safe and blocked sender data from clients to on-premises Active Directory.</span></span>
   - <span data-ttu-id="c7ef7-351">msExchSafeRecipientsHash : écrit en ligne les données d’expéditeurs sécurisés et bloqués des clients vers Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-351">msExchSafeRecipientsHash – Writes back online safe and blocked sender data from clients to on-premises Active Directory.</span></span>
   - <span data-ttu-id="c7ef7-352">msExchSafeSendersHash : écrit en ligne les données d’expéditeurs sécurisés et bloqués des clients vers Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-352">msExchSafeSendersHash – Writes back online safe and blocked sender data from clients to on-premises Active Directory.</span></span>

2. <span data-ttu-id="c7ef7-353">Si la boîte aux lettres source est sur LitigationHold et que la taille des éléments récupérables de la boîte aux lettres source est supérieure à la taille par défaut de notre base de données (30 Go), les déplacements ne se déroulent pas, car le quota cible est inférieur à la taille de boîte aux lettres source.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-353">If the source mailbox is on LitigationHold and the source mailbox Recoverable Items size is greater than our database default (30 GB), moves will not proceed since the target quota is less than the source mailbox size.</span></span> <span data-ttu-id="c7ef7-354">Vous pouvez mettre à jour l’objet MailUser cible pour faire passer les indicateurs de boîte aux lettres ELC de l’environnement source à la cible, ce qui déclenche le développement du quota de MailUser par le système cible à 100 Go, ce qui permet le déplacement vers la cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-354">You can update the target MailUser object to transition the ELC mailbox flags from the source environment to the target, which triggers the target system to expand the quota of the MailUser to 100 GB, thus allowing the move to the target.</span></span> <span data-ttu-id="c7ef7-355">Ces instructions ne fonctionnent que pour l’identité hybride exécutant Azure AD Connecter, car les commandes pour marquer les indicateurs ELC ne sont pas exposées aux administrateurs client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-355">These instructions will work only for hybrid identity running Azure AD Connect, as the commands to stamp the ELC flags are not exposed to tenant administrators.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7ef7-356">EXEMPLE – EN L’ABSENCE DE GARANTIE</span><span class="sxs-lookup"><span data-stu-id="c7ef7-356">SAMPLE – AS IS, NO WARRANTY</span></span>
    >
    > <span data-ttu-id="c7ef7-357">Ce script suppose une connexion à la boîte aux lettres source (pour obtenir les valeurs sources) et à la cible Active Directory sur site (pour marquer l’objet ADUser).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-357">This script assumes a connection to both source mailbox (to get source values) and the target on-premises Active Directory (to stamp the ADUser object).</span></span> <span data-ttu-id="c7ef7-358">Si la source est pour litige ou si la récupération d’élément unique est activée, définissez-la sur le compte de destination.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-358">If source has litigation or single item recovery enabled, set this on the destination account.</span></span>  <span data-ttu-id="c7ef7-359">Cela augmente la taille de benne du compte de destination à 100 Go.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-359">This will increase the dumpster size of destination account to 100 GB.</span></span>

    ```powershell
    $ELCValue = 0
    if ($source.LitigationHoldEnabled) {$ELCValue = $ELCValue + 8} if ($source.SingleItemRecoveryEnabled) {$ELCValue = $ELCValue + 16} if ($ELCValue -gt 0) {Set-ADUser -Server $domainController -Identity $destination.SamAccountName -Replace @{msExchELCMailboxFlags=$ELCValue}}
    ```

3. <span data-ttu-id="c7ef7-360">Les locataires cibles non hybrides peuvent modifier le quota sur le dossier Éléments récupérables des mailUsers avant la migration en exécutant la commande suivante pour activer la attente pour litige sur l’objet MailUser et en augmentant le quota à 100 Go : `Set-MailUser -EnableLitigationHoldForMigration $TRUE`</span><span class="sxs-lookup"><span data-stu-id="c7ef7-360">Non-hybrid target tenants can modify the quota on the Recoverable Items folder for the MailUsers prior to migration by running the following command to enable Litigation Hold on the MailUser object and increasing the quota to 100 GB: `Set-MailUser -EnableLitigationHoldForMigration $TRUE`.</span></span> <span data-ttu-id="c7ef7-361">Notez que cela ne fonctionne pas pour les locataires dans un mode hybride.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-361">Note this will not work for tenants in hybrid.</span></span>

4. <span data-ttu-id="c7ef7-362">Les utilisateurs de l’organisation cible doivent être titulaires d’une licence Exchange Online les abonnements applicables à l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-362">Users in the target organization must be licensed with appropriate Exchange Online subscriptions applicable for the organization.</span></span> <span data-ttu-id="c7ef7-363">Vous pouvez appliquer une licence avant le déplacement d’une boîte aux lettres, mais seulement une fois que l’utilisateur de messagerie cible est correctement installé avec ExchangeGUID et les adresses proxy.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-363">You may apply a license in advance of a mailbox move but ONLY once the target MailUser is properly set up with ExchangeGUID and proxy addresses.</span></span> <span data-ttu-id="c7ef7-364">L’application d’une licence avant l’application d’ExchangeGUID entraîne la mise en service d’une nouvelle boîte aux lettres dans l’organisation cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-364">Applying a license before the ExchangeGUID is applied will result in a new mailbox provisioned in target organization.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c7ef7-365">Lorsque vous appliquez une licence à un objet Mailbox ou MailUser, toutes les adresses proxy de type SMTP sont nettoyées pour garantir que seuls les domaines vérifiés sont inclus dans le tableau Exchange EmailAddresses.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-365">When you apply a license on a Mailbox or MailUser object, all SMTP type proxyAddresses are scrubbed to ensure only verified domains are included in the Exchange EmailAddresses array.</span></span>

5. <span data-ttu-id="c7ef7-366">Vous devez vous assurer que le MailUser cible n’a aucun ExchangeGuid précédent qui ne correspond pas à l’ExchangeGuid source.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-366">You must ensure that the target MailUser has no previous ExchangeGuid that does not match the Source ExchangeGuid.</span></span> <span data-ttu-id="c7ef7-367">Cela peut se produire si l’utilisateur à messagerie utilisateur cible a été précédemment titulaire d’une licence Exchange Online et a fourni une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-367">This might occur if the target MEU was previously licensed for Exchange Online and provisioned a mailbox.</span></span> <span data-ttu-id="c7ef7-368">Si la cible MailUser a déjà été titulaire d’une licence ExchangeGuid ou qu’elle avait un ExchangeGuid qui ne correspond pas à l’ExchangeGuid source, vous devez effectuer un nettoyage de l’UI de cloud.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-368">If the target MailUser was previously licensed for or had an ExchangeGuid that does not match the Source ExchangeGuid, you need to perform a cleanup of the cloud MEU.</span></span> <span data-ttu-id="c7ef7-369">Pour ces meus cloud, vous pouvez exécuter `Set-User <identity> -PermanentlyClearPreviousMailboxInfo` .</span><span class="sxs-lookup"><span data-stu-id="c7ef7-369">For these cloud MEUs, you can run `Set-User <identity> -PermanentlyClearPreviousMailboxInfo`.</span></span>

    > [!CAUTION]
    > <span data-ttu-id="c7ef7-370">Ce processus est irréversible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-370">This process is irreversible.</span></span> <span data-ttu-id="c7ef7-371">Si l’objet possède une boîte aux lettres supprimée (softDeleted), il ne peut pas être restauré après ce point.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-371">If the object has a softDeleted mailbox, it cannot be restored after this point.</span></span> <span data-ttu-id="c7ef7-372">Une fois effacé, toutefois, vous pouvez synchroniser l’objet ExchangeGuid correct avec l’objet cible et MRS connectera la boîte aux lettres source à la boîte aux lettres cible nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-372">Once cleared, however, you can sync the correct ExchangeGuid to the target object and MRS will connect the source mailbox to the newly created target mailbox.</span></span> <span data-ttu-id="c7ef7-373">(Référencez le blog EHLO sur le nouveau paramètre.)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-373">(Reference EHLO blog on the new parameter.)</span></span>

    <span data-ttu-id="c7ef7-374">Recherchez des objets qui étaient auparavant des boîtes aux lettres à l’aide de cette commande.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-374">Find objects that were previously mailboxes using this command.</span></span>

    ```powershell
    Get-User <identity> | select Name, *recipient* | ft -AutoSize
    ```

    <span data-ttu-id="c7ef7-375">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-375">Here is an example.</span></span>

    ```powershell
    PS demo> get-user John@northwindtraders.com |select name, *recipient*| ft -AutoSize

    Name       PreviousRecipientTypeDetails     RecipientType RecipientTypeDetails
    ----       ---------------------------- ------------- --------------------
    John       UserMailbox                  MailUser      MailUser
    ```

    <span data-ttu-id="c7ef7-376">Effacez la boîte aux lettres supprimée (à l’aide de cette commande).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-376">Clear the soft-deleted mailbox using this command.</span></span>

    ```powershell
    Set-User <identity> -PermanentlyClearPreviousMailboxInfo
    ```

    <span data-ttu-id="c7ef7-377">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-377">Here is an example.</span></span>

    ```powershell
    PS demo> Set-User John@northwindtraders.com -PermanentlyClearPreviousMailboxInfo Confirm
    Are you sure you want to perform this action?
    Delete all existing information about user “John@northwindtraders.com"?. This operation will clear existing values from Previous home MDB and Previous Mailbox GUID of the user. After deletion, reconnecting to the previous mailbox that existed in the cloud will not be possible and any content it had will be unrecoverable PERMANENTLY.
    Do you want to continue?
    [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"): Y
    ```

## <a name="perform-mailbox-migrations"></a><span data-ttu-id="c7ef7-378">Effectuer des migrations de boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="c7ef7-378">Perform mailbox migrations</span></span>

<span data-ttu-id="c7ef7-379">Les migrations entre Exchange boîtes aux lettres sont envoyées en tant que lots de migration initiés à partir du client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-379">Cross-tenant Exchange mailbox migrations are submitted as migration batches initiated from the target tenant.</span></span> <span data-ttu-id="c7ef7-380">Cela est similaire au mode de travail des lots de migration d’embarquement lors de la migration de Exchange en local vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-380">This is similar to the way that on-boarding migration batches work when migrating from Exchange on-premises to Microsoft 365.</span></span>

### <a name="create-migration-batches"></a><span data-ttu-id="c7ef7-381">Créer des lots de migration</span><span class="sxs-lookup"><span data-stu-id="c7ef7-381">Create Migration batches</span></span>

<span data-ttu-id="c7ef7-382">Voici un exemple de cmdlet de lot de migration pour supprimer les déplacements.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-382">Here is an example migration batch cmdlet for kicking off moves.</span></span>

```powershell
New-MigrationBatch -Name T2Tbatch-testforignitedemo -SourceEndpoint target_source_7977 -CSVData ([System.IO.File]::ReadAllBytes('users.csv')) -Autostart -TargetDeliveryDomain targetformoves.onmicrosoft.com -AutoComplete

Identity                   Status  Type               TotalCount
--------                   ------  ----               ----------
T2Tbatch-testforignitedemo Syncing ExchangeRemoteMove 1

```

> [!NOTE]
> <span data-ttu-id="c7ef7-383">L’adresse de messagerie dans le fichier CSV doit être celle spécifiée dans le client cible, et non le client source.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-383">The email address in the CSV file must be the one specified in the target tenant, not the source tenant.</span></span>

<span data-ttu-id="c7ef7-384">L’envoi de lot de migration est également pris en charge à partir du nouveau centre d Exchange’administration lorsque vous sélectionnez l’option entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-384">Migration batch submission is also supported from the new Exchange Admin Center when selecting the cross-tenant option.</span></span>

#### <a name="update-on-premises-mailusers"></a><span data-ttu-id="c7ef7-385">Mettre à jour les mailusers locaux</span><span class="sxs-lookup"><span data-stu-id="c7ef7-385">Update on-premises MailUsers</span></span>

<span data-ttu-id="c7ef7-386">Une fois que la boîte aux lettres passe de la source à la cible, vous devez vous assurer que les utilisateurs de messagerie locaux, source et cible, sont mis à jour avec la nouvelle adresse cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-386">Once the mailbox moves from source to target, you should ensure that the on-premises mail users, both Source and target, are updated with the new targetAddress.</span></span> <span data-ttu-id="c7ef7-387">Dans les exemples, le targetDeliveryDomain utilisé dans le déplacement **est contoso.onmicrosoft.com**.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-387">In the examples, the targetDeliveryDomain used in the move is **contoso.onmicrosoft.com**.</span></span> <span data-ttu-id="c7ef7-388">Mettez à jour les utilisateurs de messagerie avec cette adresse cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-388">Update the mail users with this targetAddress.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c7ef7-389">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="c7ef7-389">Frequently asked questions</span></span>

<span data-ttu-id="c7ef7-390">**Devons-nous mettre à jour RemoteMailboxes dans la source sur site après le déplacement ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-390">**Do we need to update RemoteMailboxes in source on-premises after the move?**</span></span>

<span data-ttu-id="c7ef7-391">Oui, vous devez mettre à jour la cibleAddress (RemoteRoutingAddress/ExternalEmailAddress) des utilisateurs locaux source lorsque la boîte aux lettres du client source se déplace vers le client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-391">Yes, you should update the targetAddress (RemoteRoutingAddress/ExternalEmailAddress) of the source on-premises users when the source tenant mailbox moves to target tenant.</span></span>  <span data-ttu-id="c7ef7-392">Bien que le routage du courrier puisse suivre les références entre plusieurs utilisateurs de messagerie avec des adresses cibles différentes, les recherches de libre/occupé pour les utilisateurs de messagerie doivent cibler l’emplacement de l’utilisateur de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-392">While mail routing can follow the referrals across multiple mail users with different targetAddresses, Free/Busy lookups for mail users MUST target the location of the mailbox user.</span></span> <span data-ttu-id="c7ef7-393">Les recherche de libre/occupé ne pourront pas poursuivre plusieurs redirections.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-393">Free/Busy lookups will not chase multiple redirects.</span></span>

<span data-ttu-id="c7ef7-394">**Les réunions Teams-elles migrer entre les locataires ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-394">**Do Teams meetings migrate cross-tenant?**</span></span>

<span data-ttu-id="c7ef7-395">Les réunions déplacent toutefois l’URL Teams réunion n’est pas mise à jour lorsque les éléments migrent entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-395">The meetings will move however the Teams meeting URL does not update when items migrate cross-tenant.</span></span> <span data-ttu-id="c7ef7-396">Étant donné que l’URL n’est pas valide dans le client cible, vous devrez supprimer et recréer Teams réunions.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-396">Since the URL will be invalid in the target tenant you will need to remove and recreate the Teams meetings.</span></span>

<span data-ttu-id="c7ef7-397">**Le contenu Teams de conversation migre-t-il entre les locataires ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-397">**Does the Teams chat folder content migrate cross-tenant?**</span></span>

<span data-ttu-id="c7ef7-398">Non, le contenu Teams de conversation ne migre pas entre les locataires.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-398">No, the Teams chat folder content does not migrate cross-tenant.</span></span>

<span data-ttu-id="c7ef7-399">**Comment puis-je voir uniquement les déplacements qui sont des déplacements inter-locataires, et non mes déplacements d’intégration et de off-embarquement ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-399">**How can I see just moves that are cross-tenant moves, not my onboarding and off-boarding moves?**</span></span>

<span data-ttu-id="c7ef7-400">Utilisez le `-flags` paramètre.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-400">Use the `-flags` parameter.</span></span> <span data-ttu-id="c7ef7-401">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-401">Here is an example.</span></span>

```powershell
Get-MoveRequest -Flags "CrossTenant"
```

<span data-ttu-id="c7ef7-402">**Pouvez-vous fournir des exemples de scripts pour copier les attributs utilisés lors des tests ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-402">**Can you provide example scripts for copying attributes used in testing?**</span></span>

> [!NOTE]
> <span data-ttu-id="c7ef7-403">EXEMPLE – EN L’ABSENCE DE GARANTIE</span><span class="sxs-lookup"><span data-stu-id="c7ef7-403">SAMPLE – AS IS, NO WARRANTY</span></span><br/><span data-ttu-id="c7ef7-404">Ce script suppose une connexion à la boîte aux lettres source (pour obtenir les valeurs sources) et aux services de domaine Active Directory locaux cibles (pour marquer l’objet ADUser).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-404">This script assumes a connection to both source mailbox (to get source values) and the target on-premises Active Directory Domain Services (to stamp the ADUser object).</span></span> <span data-ttu-id="c7ef7-405">Si la source est pour litige ou si la récupération d’élément unique est activée, définissez-la sur le compte de destination.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-405">If source has litigation or single item recovery enabled, set this on the destination account.</span></span>  <span data-ttu-id="c7ef7-406">Cela augmente la taille de benne du compte de destination à 100 Go.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-406">This will increase the dumpster size of destination account to 100 GB.</span></span>

```powershell
#Dumps out the test mailboxes from SourceTenant
#Note, the filter applied on Get-Mailbox is for an attribute set on CustomAttribute1 = "ProjectKermit"
#These are the ‘target’ users to be moved to the Northwind org tenant #################################################################
$outFileUsers = "$home\desktop\userstomigrate.txt"
$outFileUsersXML = "$home\desktop\userstomigrate.xml"
#output the test objects
Get-Mailbox -Filter "CustomAttribute1 -like 'ProjectKermit'" -ResultSize Unlimited | Select-Object -ExpandProperty Alias | Out-File $outFileUsers
$mailboxes = Get-Content $outFileUsers
$mailboxes | ForEach-Object {Get-Mailbox $_} | Select-Object PrimarySMTPAddress,Alias,SamAccountName,FirstName,LastName,DisplayName,Name,ExchangeGuid,ArchiveGuid,LegacyExchangeDn,EmailAddresses | Export-Clixml $outFileUsersXML

#################################################################
#Copy the file $outfile to the desktop of the target on-premises
#then run the below to create MEU in Target
#################################################################
$mailboxes = Import-Clixml $home\desktop\userstomigrate.xml

foreach ($m in $mailboxes) {
    $organization = "@contoso.onmicrosoft.com"
    $mosi = $m.Alias+$organization
    $Password = [System.Web.Security.Membership]::GeneratePassword(16,4) | ConvertTo-SecureString -AsPlainText -Force
    $x500 = "x500:" +$m.LegacyExchangeDn
    $tmpUser = New-MailUser -MicrosoftOnlineServicesID $mosi -PrimarySmtpAddress $mosi -ExternalEmailAddress $m.PrimarySmtpAddress -FirstName $m.FirstName -LastName $m.LastName -Name $m.Name -DisplayName $m.DisplayName -Alias $m.Alias -Password $Password
    $tmpUser | Set-MailUser -EmailAddresses @{add=$x500} -ExchangeGuid $m.ExchangeGuid -ArchiveGuid $m.ArchiveGuid -CustomAttribute1 "ProjectKermit"
    $tmpx500 = $m.EmailAddresses | ?{$_ -match "x500"}
    $tmpx500 | %{Set-MailUser $m.Alias -EmailAddresses @{add="$_"}}
    }

#################################################################
# On AADSync machine, run AADSync
#################################################################
Start-ADSyncSyncCycle

#AADSync and FWDSync will create the target MEUs in the Target tenant
```

<span data-ttu-id="c7ef7-407">**Comment pouvons-nous accéder Outlook jour 1 une fois que la boîte aux lettres d’utilisation a été déplacée ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-407">**How do we access Outlook on Day 1 after the use mailbox is moved?**</span></span>

<span data-ttu-id="c7ef7-408">Étant donné qu’un seul client peut posséder un domaine, l’ancienne adresse SMTP principale n’est pas associée à l’utilisateur dans le client cible une fois le déplacement de la boîte aux lettres terminé . uniquement les domaines associés au nouveau client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-408">Since only one tenant can own a domain, the former primary SMTPAddress will not be associated to the user in the target tenant when the mailbox move completes; only those domains associated with the new tenant.</span></span> <span data-ttu-id="c7ef7-409">Outlook utilise le nouvel UPN des utilisateurs pour s’authentifier au service et le profil Outlook s’attend à trouver l’adresse SMTPAddress principale héritée pour correspondre à la boîte aux lettres dans le système cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-409">Outlook uses the users new UPN to authenticate to the service and the Outlook profile expects to find the legacy primary SMTPAddress to match the mailbox in the target system.</span></span> <span data-ttu-id="c7ef7-410">Étant donné que l’adresse héritée ne se trouve pas dans le système cible, le profil Outlook ne se connecte pas pour rechercher la boîte aux lettres nouvellement déplacée.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-410">Since the legacy address is not in the target System the outlook profile will not connect to find the newly moved mailbox.</span></span>

<span data-ttu-id="c7ef7-411">Pour ce déploiement initial, les utilisateurs devront reconstruire leur profil avec leur nouvel UPN, l’adresse SMTP principale et synchroniser à nouveau le contenu OST.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-411">For this initial deployment, users will need to rebuild their profile with their new UPN, primary SMTP address and re-sync OST content.</span></span>

> [!NOTE]
> <span data-ttu-id="c7ef7-412">Planifiez en conséquence le traitement par lots de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-412">Plan accordingly as you batch your users for completion.</span></span> <span data-ttu-id="c7ef7-413">Vous devez tenir compte de l’utilisation et de la capacité du réseau lorsque Outlook profils clients sont créés et que les fichiers OST et OAB suivants sont téléchargés vers les clients.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-413">You need to account for network utilization and capacity when Outlook client profiles are created and subsequent OST and OAB files are downloaded to clients.</span></span>

<span data-ttu-id="c7ef7-414">**De quels Exchange RBAC ai-je besoin d’être membre pour configurer ou effectuer un déplacement entre locataires ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-414">**What Exchange RBAC roles do I need to be member of to set up or complete a cross-tenant move?**</span></span>

<span data-ttu-id="c7ef7-415">Il existe une matrice de rôles basée sur l’hypothèse de tâches déléguées lors de l’exécution d’un déplacement de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-415">There a matrix of roles based on assumption of delegated duties when executing a mailbox move.</span></span> <span data-ttu-id="c7ef7-416">Actuellement, deux rôles sont requis :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-416">Currently, two roles are required:</span></span>

- <span data-ttu-id="c7ef7-417">Le premier rôle est une tâche de configuration qui établit l’autorisation de déplacer du contenu vers ou hors de vos limites client/organisation.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-417">The first role is for a one-time setup task that establishes the authorization of moving content into or out of your tenant/organizational boundary.</span></span> <span data-ttu-id="c7ef7-418">Étant donné que le déplacement des données hors de votre contrôle organisationnel est une préoccupation critique pour toutes les entreprises, nous avons choisi le rôle d’administrateur d’organisation (OrgAdmin) le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-418">As moving data out of your organizational control is a critical concern for all companies, we opted with the highest assigned role of Organization Administrator (OrgAdmin).</span></span> <span data-ttu-id="c7ef7-419">Ce rôle doit modifier ou configurer un nouvel OrganizationRelationship qui définit la -MailboxMoveCapability avec l’organisation distante.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-419">This role must alter or setup a new OrganizationRelationship that defines the -MailboxMoveCapability with the remote organization.</span></span> <span data-ttu-id="c7ef7-420">Seul l’OrgAdmin peut modifier le paramètre MailboxMoveCapability, tandis que d’autres attributs de OrganizationRelationhip peuvent être gérés par l’administrateur de partage fédéré.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-420">Only the OrgAdmin can alter the MailboxMoveCapability setting, while other attributes on the OrganizationRelationhip can be managed by the Federated Sharing administrator.</span></span>

- <span data-ttu-id="c7ef7-421">Le rôle d’exécution des commandes de déplacement réelles peut être délégué à une fonction de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-421">The role of executing the actual move commands can be delegated to a lower-level function.</span></span> <span data-ttu-id="c7ef7-422">Le rôle de déplacement de boîtes aux lettres se voit attribuer la possibilité de déplacer des boîtes aux lettres à l’intérieur ou à l’intérieur de l’organisation à l’aide du `-RemoteTenant` paramètre.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-422">The role of Move Mailboxes is assigned the capability of moving mailboxes in or out of the organization by using the `-RemoteTenant` parameter.</span></span>

<span data-ttu-id="c7ef7-423">**Comment cibler l’adresse SMTP sélectionnée pour targetAddress (TargetDeliveryDomain) sur la boîte aux lettres convertie (en conversion MailUser) ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-423">**How do we target which SMTP address is selected for targetAddress (TargetDeliveryDomain) on the converted mailbox (to MailUser conversion)?**</span></span>

<span data-ttu-id="c7ef7-424">Exchange déplacements de boîtes aux lettres à l’aide du service MRS tissent l’adresse cible sur la boîte aux lettres source d’origine lors de la conversion en MailUser en correspondant à une adresse e-mail (proxyAddress) sur l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-424">Exchange mailbox moves using MRS craft the targetAddress on the original source mailbox when converting to a MailUser by matching an email address (proxyAddress) on the target object.</span></span> <span data-ttu-id="c7ef7-425">Le processus prend la valeur -TargetDeliveryDomain transmise dans la commande de déplacement, puis recherche un proxy correspondant pour ce domaine côté cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-425">The process takes the -TargetDeliveryDomain value passed into the move command, then checks for a matching proxy for that domain on the target side.</span></span> <span data-ttu-id="c7ef7-426">Lorsque nous trouvons une correspondance, le proxyAddress correspondant est utilisé pour définir ExternalEmailAddress (targetAddress) sur l’objet de boîte aux lettres convertie (désormais MailUser).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-426">When we find a match, the matching proxyAddress is used to set the ExternalEmailAddress (targetAddress) on the converted mailbox (now MailUser) object.</span></span>

<span data-ttu-id="c7ef7-427">**Comment les autorisations de boîte aux lettres sont-ils en cours de transition ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-427">**How do mailbox permissions transition?**</span></span>

<span data-ttu-id="c7ef7-428">Les autorisations de boîte aux lettres incluent Envoyer de la part de et Accès aux boîtes aux lettres :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-428">Mailbox permissions include Send on Behalf of and Mailbox Access:</span></span>

- <span data-ttu-id="c7ef7-429">Send On Behalf Of (AD:publicDelegates) stocke le nom DN des destinataires ayant accès à la boîte aux lettres d’un utilisateur en tant que délégué.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-429">Send On Behalf Of (AD:publicDelegates) stores the DN of recipients with access to a user’s mailbox as a delegate.</span></span> <span data-ttu-id="c7ef7-430">Cette valeur est stockée dans Active Directory et ne se déplace actuellement pas dans le cadre de la transition de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-430">This value is stored in Active Directory and currently does not move as part of the mailbox transition.</span></span> <span data-ttu-id="c7ef7-431">Si la boîte aux lettres source a publicDelegates définie, vous devrez restamper les publicDelegates sur la boîte aux lettres cible une fois la conversion de l’utilisateur à l’utilisateur à boîte aux lettres terminée dans l’environnement cible en cours `Set-Mailbox <principle> -GrantSendOnBehalfTo <delegate>` d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-431">If the source mailbox has publicDelegates set, you will need to restamp the publicDelegates on the target Mailbox once the MEU to Mailbox conversion completes in the target environment by running `Set-Mailbox <principle> -GrantSendOnBehalfTo <delegate>`.</span></span>

- <span data-ttu-id="c7ef7-432">Les autorisations de boîte aux lettres stockées dans la boîte aux lettres sont déplacées avec la boîte aux lettres lorsque le principal et le délégué sont déplacés vers le système cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-432">Mailbox Permissions that are stored in the mailbox will move with the mailbox when both the principal and the delegate are moved to the target system.</span></span> <span data-ttu-id="c7ef7-433">Par exemple, l’utilisateur TestUser_7 accès total à la boîte aux lettres TestUser_8 dans le client SourceCompany.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-433">For example, the user TestUser_7 is granted FullAccess to the mailbox TestUser_8 in the tenant SourceCompany.onmicrosoft.com.</span></span> <span data-ttu-id="c7ef7-434">Une fois le déplacement de la boîte TargetCompany.onmicrosoft.com terminé, les mêmes autorisations sont définies dans le répertoire cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-434">After the mailbox move completes to TargetCompany.onmicrosoft.com, the same permissions are set up in the target directory.</span></span> <span data-ttu-id="c7ef7-435">Des exemples *d’utilisation de Get-MailboxPermission* TestUser_7 dans les clients source et cible sont présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-435">Examples using *Get-MailboxPermission* for TestUser_7 in both source and target tenants are shown below.</span></span> <span data-ttu-id="c7ef7-436">Exchange cmdlets sont précédées du préfixe source et cible en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-436">Exchange cmdlets are prefixed with source and target accordingly.</span></span>

<span data-ttu-id="c7ef7-437">Voici un exemple de sortie de l’autorisation de boîte aux lettres avant un déplacement.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-437">Here's an example of the output of the mailbox permission before a move.</span></span>

```powershell
PS C:\PowerShell\> Get-SourceMailboxPermission testuser_7 |ft -AutoSize User, AccessRights, IsInherited, Deny
User                                             AccessRights                                                            IsInherited Deny
----                                             ------------                                                            ----------- ----
NT AUTHORITY\SELF                                {FullAccess, ReadPermission}                                            False       False
TestUser_8@SourceCompany.onmicrosoft.com         {FullAccess}                                                            False       False....
```

<span data-ttu-id="c7ef7-438">Voici un exemple de sortie de l’autorisation de boîte aux lettres après le déplacement.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-438">Here's an example of the output of the mailbox permission after the move.</span></span>

```powershell
PS C:\PowerShell\> Get-TargetMailboxPermission testuser_7 | ft -AutoSize User, AccessRights, IsInherited, Deny
User                                             AccessRights                                                            IsInherited Deny
----                                             ------------                                                            ----------- ----
NT AUTHORITY\SELF                                {FullAccess, ReadPermission}                                            False       FalseTestUser_8@TargetCompany.onmicrosoft.com         {FullAccess}                                                            False       False
```

> [!NOTE]
> <span data-ttu-id="c7ef7-439">Les autorisations de calendrier et de boîte aux lettres entre locataires ne sont PAS pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-439">Cross-tenant mailbox and calendar permissions are NOT supported.</span></span> <span data-ttu-id="c7ef7-440">Vous devez organiser les principaux et les délégués en lots de déplacement consolidés afin que ces boîtes aux lettres connectées soient transitionn es en même temps à partir du client source.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-440">You must organize principals and delegates into consolidated move batches so that these connected mailboxes are transitioned at the same time from the source tenant.</span></span>

<span data-ttu-id="c7ef7-441">**Quel proxy X500 doit être ajouté aux adresses proxy MailUser cibles pour permettre la migration ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-441">**What X500 proxy should be added to the target MailUser proxy addresses to enable migration?**</span></span>

<span data-ttu-id="c7ef7-442">La migration de boîtes aux lettres entre locataires nécessite que la valeur LegacyExchangeDN de l’objet de boîte aux lettres source soit estampillée comme adresse de messagerie x500 sur l’objet MailUser cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-442">The cross-tenant mailbox migration requires that the LegacyExchangeDN value of the source mailbox object to be stamped as an x500 email address on the target MailUser object.</span></span>

<span data-ttu-id="c7ef7-443">Exemple :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-443">Example:</span></span>

```powershell
LegacyExchangeDN value on source mailbox is:
/o=First Organization/ou=Exchange Administrative Group(FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c81907273f1f9Lara

so the x500 email address to be added to target MailUser object would be:
x500:/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=d11ec1a2cacd4f81858c81907273f1f9-Lara
```

> [!NOTE]
> <span data-ttu-id="c7ef7-444">Outre ce proxy X500, vous devrez copier tous les proxys X500 de la boîte aux lettres dans la source vers la boîte aux lettres dans la cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-444">In addition to this X500 proxy, you will need to copy all X500 proxies from the mailbox in the source to the mailbox in the target.</span></span>

<span data-ttu-id="c7ef7-445">**Où commencer à résoudre les problèmes si les déplacements ne fonctionnent pas ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-445">**Where do I start troubleshooting if moves do not work?**</span></span>

<span data-ttu-id="c7ef7-446">Commencez par l’exécution VerifySetup.ps1 script situé sur GitHub et [examinez](https://github.com/microsoft/cross-tenant/releases/tag/Preview) la sortie.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-446">Start by running the VerifySetup.ps1 script located [on GitHub](https://github.com/microsoft/cross-tenant/releases/tag/Preview) and review the output.</span></span>

<span data-ttu-id="c7ef7-447">Voici un exemple d’exécution de VerifySetup.ps1 sur le client cible :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-447">Here's an example of running VerifySetup.ps1 on the target tenant:</span></span>

```powershell
VerifySetup.ps1 -PartnerTenantId <SourceTenantId> -ApplicationId <AADApplicationId> -ApplicationKeyVaultUrl <appKeyVaultUrl> -PartnerTenantDomain <PartnerTenantDomain> -Verbose
```

<span data-ttu-id="c7ef7-448">Voici un exemple d’exécution de VerifySetup.ps1 sur le client source :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-448">Here's an eExample of running VerifySetup.ps1 on the source tenant:</span></span>

```powershell
VerifySetup.ps1 -PartnerTenantId <TargetTenantId> -ApplicationId <AADApplicationId>
```

<span data-ttu-id="c7ef7-449">**Le client source et cible peut-il utiliser le même nom de domaine ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-449">**Can the source and target tenant utilize the same domain name?**</span></span>

<span data-ttu-id="c7ef7-450">Non.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-450">No.</span></span> <span data-ttu-id="c7ef7-451">Les noms de domaine du client source et cible doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-451">The source and target tenant domain names must be unique.</span></span> <span data-ttu-id="c7ef7-452">Par exemple, un domaine source de contoso.com et le domaine cible de fourthcoffee.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-452">For example, a source domain of contoso.com and the target domain of fourthcoffee.com.</span></span>

<span data-ttu-id="c7ef7-453">**Les boîtes aux lettres partagées seront-ils toujours en déplacement et fonctionneront-ils ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-453">**Will shared mailboxes move and still work?**</span></span>

<span data-ttu-id="c7ef7-454">Oui, toutefois, nous ne conserveons que les autorisations du Store comme décrit dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-454">Yes, however we only keep the store permissions as described in these articles:</span></span>

- [<span data-ttu-id="c7ef7-455">Documentation Microsoft | Gérer les autorisations pour les destinataires dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c7ef7-455">Microsoft Docs | Manage permissions for recipients in Exchange Online</span></span>](/exchange/recipients-in-exchange-online/manage-permissions-for-recipients)

- [<span data-ttu-id="c7ef7-456">Support Microsoft | Comment accorder des autorisations Exchange et Outlook aux boîtes aux lettres dans Office 365 dédié</span><span class="sxs-lookup"><span data-stu-id="c7ef7-456">Microsoft Support | How to grant Exchange and Outlook mailbox permissions in Office 365 dedicated</span></span>](https://support.microsoft.com/topic/how-to-grant-exchange-and-outlook-mailbox-permissions-in-office-365-dedicated-bac01b2c-08ff-2eac-e1c8-6dd01cf77287)

<span data-ttu-id="c7ef7-457">**Azure Key Vault est-il requis et quand les transactions sont-elles réalisées ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-457">**Is Azure Key Vault required and when are transactions made?**</span></span>

<span data-ttu-id="c7ef7-458">Oui, un abonnement Azure est requis pour utiliser le coffre de clés pour stocker le certificat afin d’autoriser la migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-458">Yes, an Azure subscription is required to use Key Vault to store the certificate to authorize migration.</span></span> <span data-ttu-id="c7ef7-459">Contrairement aux migrations d’intégration qui utilisent le mot de passe & nom d’utilisateur pour s’authentifier à la source, les migrations de boîtes aux lettres entre locataires utilisent OAuth et ce certificat comme secret/informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-459">Unlike onboarding migrations which use username & password to authenticate to the source, cross-tenant mailbox migrations use OAuth and this certificate as the secret/credential.</span></span> <span data-ttu-id="c7ef7-460">L’accès au coffre de clés doit être maintenu tout au long de toutes les migrations de boîtes aux lettres, car il est accessible une fois au début et une fois à la fin de la migration, ainsi qu’une fois toutes les 24 heures pendant les périodes de synchronisation incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-460">Access to the Key Vault must be maintained throughout all mailbox migrations as it is accessed once at the beginning and once end of migration, as well as once every 24 hours during incremental sync times.</span></span> <span data-ttu-id="c7ef7-461">Vous pouvez consulter les détails de coût AKV [ici.](https://azure.microsoft.com/en-us/pricing/details/key-vault/)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-461">You can review AKV costing details [here](https://azure.microsoft.com/en-us/pricing/details/key-vault/).</span></span>

<span data-ttu-id="c7ef7-462">**Avez-vous des recommandations pour les lots ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-462">**Do you have any recommendations for batches?**</span></span>

<span data-ttu-id="c7ef7-463">Ne dépassez pas 2 000 boîtes aux lettres par lot.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-463">Do not exceed 2000 mailboxes per batch.</span></span> <span data-ttu-id="c7ef7-464">Nous vous recommandons vivement d’envoyer des lots deux semaines avant la date de cut-over, car cela n’a aucun impact sur les utilisateurs finaux pendant la synchronisation. Si vous avez besoin de conseils pour les quantités de boîtes aux lettres de plus de 50 000, vous pouvez accéder à la liste de distribution des commentaires techniques sur crosstenantmigrationpreview@service.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-464">We strongly recommend submitting batches two weeks prior to the cut-over date as there is no impact to the end users during sync. If you need guidance for mailboxes quantities over 50,000 you can reach out to the Engineering Feedback Distribution List at crosstenantmigrationpreview@service.microsoft.com.</span></span>

<span data-ttu-id="c7ef7-465">**Que se passe-t-il si j’utilise le chiffrement de service avec la clé client ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-465">**What if I use Service encryption with Customer Key?**</span></span>

<span data-ttu-id="c7ef7-466">La boîte aux lettres sera déchiffrée avant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-466">The mailbox will be decrypted prior to moving.</span></span> <span data-ttu-id="c7ef7-467">Assurez-vous que la clé client est configurée dans le client cible si elle est toujours requise.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-467">Ensure Customer Key is configured in the target tenant if it is still required.</span></span> <span data-ttu-id="c7ef7-468">Pour [plus d’informations,](../compliance/customer-key-overview.md) voir ici.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-468">See [here](../compliance/customer-key-overview.md) for more information.</span></span>

<span data-ttu-id="c7ef7-469">**Quelle est la durée de migration estimée ?**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-469">**What is the estimated migration time?**</span></span>

<span data-ttu-id="c7ef7-470">Pour vous aider à planifier [](/exchange/mailbox-migration/office-365-migration-best-practices#estimated-migration-times) votre migration, le tableau présenté ici présente les instructions relatives à la fin des migrations de boîtes aux lettres en bloc ou individuelles.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-470">To help you plan your migration, the table present [here](/exchange/mailbox-migration/office-365-migration-best-practices#estimated-migration-times) shows the guidelines about when to expect bulk mailbox migrations or individual migrations to complete.</span></span> <span data-ttu-id="c7ef7-471">Ces estimations sont basées sur une analyse des données des migrations de clients précédentes.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-471">These estimates are based on a data analysis of previous customer migrations.</span></span> <span data-ttu-id="c7ef7-472">Étant donné que chaque environnement est unique, votre vitesse de migration exacte peut varier.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-472">Because every environment is unique, your exact migration velocity may vary.</span></span>

<span data-ttu-id="c7ef7-473">N’oubliez pas que cette fonctionnalité est actuellement en prévisualisation et que le SLA et les niveaux de service applicables ne s’appliquent pas aux problèmes de performances ou de disponibilité pendant l’état d’aperçu de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-473">Do remember that this feature is currently in preview and the SLA and any applicable Service Levels do not apply to any performance or availability issues during the preview status of this feature.</span></span>

## <a name="known-issues"></a><span data-ttu-id="c7ef7-474">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="c7ef7-474">Known issues</span></span>

- <span data-ttu-id="c7ef7-475">**Problème : les archives à extension automatique ne peuvent pas être migrées.**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-475">**Issue: Auto Expanded archives cannot be migrated.**</span></span> <span data-ttu-id="c7ef7-476">La fonctionnalité de migration entre locataires permet de migrer la boîte aux lettres principale et la boîte aux lettres d’archivage d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-476">The cross-tenant migration feature support migrations of the primary mailbox and archive mailbox for a specific user.</span></span> <span data-ttu-id="c7ef7-477">Si l’utilisateur dans la source possède toutefois une archive à extension automatique , ce qui signifie que plusieurs boîtes aux lettres d’archivage, la fonctionnalité ne peut pas migrer les archives supplémentaires et doit échouer.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-477">If the user in the source however has an auto expanded archive – meaning more than one archive mailbox, the feature is unable to migrate the additional archives and should fail.</span></span>

- <span data-ttu-id="c7ef7-478">**Problème : les mailusers cloud avec un proxyAddress smtp non propriétaire bloquent mrs déplace l’arrière-plan.**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-478">**Issue: Cloud MailUsers with non-owned smtp proxyAddress block MRS moves background.**</span></span> <span data-ttu-id="c7ef7-479">Lorsque vous créez des objets MailUser de client cible, vous devez vous assurer que toutes les adresses proxy SMTP appartiennent à l’organisation du client cible.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-479">When creating target tenant MailUser objects, you must ensure that all SMTP proxy addresses belong to the target tenant organization.</span></span> <span data-ttu-id="c7ef7-480">S’il existe un proxy SMTPAddress sur l’utilisateur de messagerie cible qui n’appartient pas au client local, la conversion de MailUser en boîte aux lettres est empêchée.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-480">If an SMTP proxyAddress exists on the target mail user that does not belong to the local tenant, the conversion of the MailUser to Mailbox is prevented.</span></span> <span data-ttu-id="c7ef7-481">Cela est dû à notre assurance que les objets de boîte aux lettres peuvent uniquement envoyer des messages à partir de domaines pour lesquels le client fait autorité (domaines revendiqués par le client) :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-481">This is due to our assurance that mailbox objects can only send mail from domains for which the tenant is authoritative (domains claimed by the tenant):</span></span>

  - <span data-ttu-id="c7ef7-482">Lorsque vous synchronisez des utilisateurs en local à l’aide d’Azure AD Connecter, vous provisionnez les objets MailUser locaux avec ExternalEmailAddress pointant vers le client source où la boîte aux lettres existe (laran@contoso.onmicrosoft.com) et vous marquez PrimarySMTPAddress comme un domaine qui réside dans le client cible (Lara.Newton@northwind.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-482">When you sync users from on-premises using Azure AD Connect, you provision on-premises MailUser objects with ExternalEmailAddress pointing to the source tenant where the mailbox exists (laran@contoso.onmicrosoft.com) and you stamp the PrimarySMTPAddress as a domain that resides in the target tenant (Lara.Newton@northwind.com).</span></span> <span data-ttu-id="c7ef7-483">Ces valeurs sont synchronisées avec le client et un utilisateur de messagerie approprié est approvisionnement et prêt pour la migration.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-483">These values sync down to the tenant and an appropriate mail user is provisioned and ready for migration.</span></span> <span data-ttu-id="c7ef7-484">Un exemple d’objet est illustré ici.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-484">An example object is shown here.</span></span>

    ```powershell
    target/AADSynced user] PS C> Get-MailUser laran | select ExternalEmailAddress, EmailAddresses
    ExternalEmailAddress               EmailAddresses
    --------------------               --------------
    SMTP:laran@contoso.onmicrosoft.com {SMTP:lara.newton@northwind.com}
    ```

   > [!NOTE]
   > <span data-ttu-id="c7ef7-485">*L contoso.onmicrosoft.com’adresse* de messagerie *n’est* pas présente dans le tableau EmailAddresses/proxyAddresses.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-485">The *contoso.onmicrosoft.com* address is *not* present in the EmailAddresses / proxyAddresses array.</span></span>

- <span data-ttu-id="c7ef7-486">**Problème : les objets MailUser avec des adresses SMTP principales « externes » sont modifiés/réinitialisés sur les domaines revendiqués par l’entreprise « internes »**</span><span class="sxs-lookup"><span data-stu-id="c7ef7-486">**Issue: MailUser objects with “external” primary SMTP addresses are modified / reset to “internal” company claimed domains**</span></span>

  <span data-ttu-id="c7ef7-487">Les objets MailUser sont des pointeurs vers des boîtes aux lettres non locales.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-487">MailUser objects are pointers to non-local mailboxes.</span></span> <span data-ttu-id="c7ef7-488">Dans le cas des migrations de boîtes aux lettres entre locataires, nous utilisons des objets MailUser pour représenter la boîte aux lettres source (du point de vue de l’organisation cible) ou la boîte aux lettres cible (du point de vue de l’organisation source).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-488">In the case for cross-tenant mailbox migrations, we use MailUser objects to represent either the source mailbox (from the target organization’s perspective) or target mailbox (from the source organization’s perspective).</span></span> <span data-ttu-id="c7ef7-489">Les utilisateurs de messagerie auront une adresse ExternalEmailAddress (targetAddress) qui pointe vers l’adresse smtp de la boîte aux lettres réelle (ProxyTest@fabrikam.onmicrosoft.com) et l’adresse PRIMARYSMTP qui représente l’adresse SMTP affichée de l’utilisateur de boîte aux lettres dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-489">The MailUsers will have an ExternalEmailAddress (targetAddress) that points to the smtp address of the actual mailbox (ProxyTest@fabrikam.onmicrosoft.com) and primarySMTP address that represents the displayed SMTP address of the mailbox user in the directory.</span></span> <span data-ttu-id="c7ef7-490">Certaines organisations choisissent d’afficher l’adresse SMTP principale en tant qu’adresse SMTP externe, et non en tant qu’adresse propriétaire/vérifiée par le client local (par exemple, fabrikam.com plutôt que comme contoso.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-490">Some organizations choose to display the primary SMTP address as an external SMTP address, not as an address owned/verified by the local tenant (such as fabrikam.com rather than as contoso.com).</span></span>  <span data-ttu-id="c7ef7-491">Toutefois, une fois qu’un objet plan de service Exchange est appliqué à MailUser via des opérations de gestion des licences, l’adresse SMTP principale est modifiée pour s’afficher comme un domaine vérifié par l’organisation locale (contoso.com).</span><span class="sxs-lookup"><span data-stu-id="c7ef7-491">However, once an Exchange service plan object is applied to the MailUser via licensing operations, the primary SMTP address is modified to show as a domain verified by the local organization (contoso.com).</span></span> <span data-ttu-id="c7ef7-492">Il existe deux raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="c7ef7-492">There are two potential reasons:</span></span>

  - <span data-ttu-id="c7ef7-493">Lorsqu’un plan de service Exchange est appliqué à un mailuser, le processus Azure AD commence à appliquer le nettoyage de proxy pour s’assurer que l’organisation locale n’est pas en mesure d’envoyer des messages électroniques, usurpations ou messages à partir d’un autre client.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-493">When any Exchange service plan is applied to a MailUser, the Azure AD process starts to enforce proxy scrubbing to ensure that the local organization is not able to send mail out, spoof, or mail from another tenant.</span></span> <span data-ttu-id="c7ef7-494">Toute adresse SMTP sur un objet destinataire avec ces plans de service sera supprimée si l’adresse n’est pas vérifiée par l’organisation locale.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-494">Any SMTP address on a recipient object with these service plans will be removed if the address is not verified by the local organization.</span></span> <span data-ttu-id="c7ef7-495">Comme c’est le cas dans l’exemple, le domaine Fabikam.com n’est PAS vérifié par le client contoso.onmicrosoft.com, de sorte que le nettoyage supprime ce fabrikam.com domaine.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-495">As is the case in the example, the Fabikam.com domain is NOT verified by the contoso.onmicrosoft.com tenant, so the scrubbing removes that fabrikam.com domain.</span></span> <span data-ttu-id="c7ef7-496">Si vous souhaitez rendre persistants ces domaines externes sur MailUser, avant la migration ou après la migration, vous devez modifier vos processus de migration afin d’obtenir des licences à la fin du déplacement ou avant le déplacement pour vous assurer que la marque externe attendue est appliquée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-496">If you wish to persist these external domain on MailUser, either before the migration or after migration, you need to alter your migration processes to strip licenses after the move completes or before the move to ensure that the users have the expected external branding applied.</span></span> <span data-ttu-id="c7ef7-497">Vous devez vous assurer que l’objet de boîte aux lettres est correctement titulaire d’une licence pour ne pas affecter le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-497">You will need to ensure that the mailbox object is properly licensed to not affect mail service.</span></span><br/><br/><span data-ttu-id="c7ef7-498">Un exemple de script pour supprimer les plans de service sur un MailUser dans le Contoso.onmicrosoft.com client est illustré ici.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-498">An example script to remove the service plans on a MailUser in the Contoso.onmicrosoft.com tenant is shown here.</span></span>

    ```powershell
    $LO = New-MsolLicenseOptions -AccountSkuId "contoso:ENTERPRISEPREMIUM" DisabledPlans
    "LOCKBOX_ENTERPRISE","EXCHANGE_S_ENTERPRISE","INFORMATION_BARRIERS","MIP_S_CLP2","
    MIP_S_CLP1","MYANALYTICS_P2","EXCHANGE_ANALYTICS","EQUIVIO_ANALYTICS","THREAT_INTE
    LLIGENCE","PAM_ENTERPRISE","PREMIUM_ENCRYPTION"
    Set-MsolUserLicense -UserPrincipalName proxytest@contoso.com LicenseOptions $lo
    ```

       <span data-ttu-id="c7ef7-499">Les résultats de l’ensemble des Plans de service affectés sont affichés ici.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-499">Results in the set of ServicePlans assigned are shown here.</span></span>

    ```powershell
    (Get-MsolUser -UserPrincipalName proxytest@contoso.com).licenses |select
    -ExpandProperty servicestatus |sort ProvisioningStatus -Descending
    ServicePlan           ProvisioningStatus
    -----------           ------------------
    ATP_ENTERPRISE        PendingProvisioning
    MICROSOFT_SEARCH      PendingProvisioning
    INTUNE_O365           PendingActivation
    PAM_ENTERPRISE        Disabled
    EXCHANGE_ANALYTICS    Disabled
    EQUIVIO_ANALYTICS     Disabled
    THREAT_INTELLIGENCE   Disabled
    LOCKBOX_ENTERPRISE    Disabled
    PREMIUM_ENCRYPTION    Disabled
    EXCHANGE_S_ENTERPRISE Disabled
    INFORMATION_BARRIERS  Disabled
    MYANALYTICS_P2        Disabled
    MIP_S_CLP1            Disabled
    MIP_S_CLP2            Disabled
    ADALLOM_S_O365        PendingInput
    RMS_S_ENTERPRISE      Success
    YAMMER_ENTERPRISE     Success
    PROJECTWORKMANAGEMENT Success
    BI_AZURE_P2           Success
    WHITEBOARD_PLAN3      Success
    SHAREPOINTENTERPRISE  Success
    SHAREPOINTWAC         Success
    KAIZALA_STANDALONE    Success
    OFFICESUBSCRIPTION    Success
    MCOSTANDARD           Success
    Deskless              Success
    STREAM_O365_E5        Success
    FLOW_O365_P3          Success
    POWERAPPS_O365_P3     Success
    TEAMS1                Success
    MCOEV                 Success
    MCOMEETADV            Success
    BPOS_S_TODO_3         Success
    FORMS_PLAN_E5         Success
    SWAY                  Success
    ```

    <span data-ttu-id="c7ef7-500">L’adresse PrimarySMTPAddress de l’utilisateur n’est plus nettoyée.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-500">The user’s PrimarySMTPAddress is no longer scrubbed.</span></span> <span data-ttu-id="c7ef7-501">Le fabrikam.com n’appartient pas au client contoso.onmicrosoft.com et est persistant en tant qu’adresse SMTP principale affichée dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-501">The fabrikam.com domain is not owned by the contoso.onmicrosoft.com tenant and will persist as the primary SMTP address shown in the directory.</span></span>

    <span data-ttu-id="c7ef7-502">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-502">Here is an example.</span></span>

    ```powershell
    get-recipient proxytest | ft -a userprin*, primary*, external*
    PrimarySmtpAddress        ExternalDirectoryObjectId               ExternalEmailAddress
    ------------------        -------------------------               --------------------
    proxytest@fabrikam.com    e2513482-1d5b-4066-936a-cbc7f8f6f817    SMTP:proxytest@fabrikam.com
    ```

    - <span data-ttu-id="c7ef7-503">Lorsque msExchRemoteRecipientType est définie sur 8 (DeprovisionMailbox), pour les mailusers locaux migrés vers le client cible, la logique de nettoyage de proxy dans Azure supprime les domaines nonowned et réinitialise le primarySMTP sur un domaine propriétaire.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-503">When msExchRemoteRecipientType is set to 8 (DeprovisionMailbox), for on-premises MailUsers that are migrated to the target tenant, the proxy scrubbing logic in Azure will remove nonowned domains and reset the primarySMTP to an owned domain.</span></span> <span data-ttu-id="c7ef7-504">En effaissant msExchRemoteRecipientType dans l’mailuser local, la logique de nettoyage proxy ne s’applique plus.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-504">By clearing msExchRemoteRecipientType in the on-premises MailUser, the proxy scrub logic no longer applies.</span></span>

      <span data-ttu-id="c7ef7-505">Voici l’ensemble complet des plans de service possibles qui incluent Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c7ef7-505">Below is the full set of possible Service Plans that include Exchange Online.</span></span>

      |<span data-ttu-id="c7ef7-506">Nom</span><span class="sxs-lookup"><span data-stu-id="c7ef7-506">Name</span></span>|
      |---|
      |<span data-ttu-id="c7ef7-507">Advanced eDiscovery Stockage (500 Go)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-507">Advanced eDiscovery Storage (500GB)</span></span>|
      |<span data-ttu-id="c7ef7-508">Référentiel sécurisé client</span><span class="sxs-lookup"><span data-stu-id="c7ef7-508">Customer Lockbox</span></span>|
      |<span data-ttu-id="c7ef7-509">Protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="c7ef7-509">Data Loss Prevention</span></span>|
      |<span data-ttu-id="c7ef7-510">Services CAL Exchange Enterprise (EOP, DLP)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-510">Exchange Enterprise CAL Services (EOP, DLP)</span></span>|
      |<span data-ttu-id="c7ef7-511">Exchange Essentials</span><span class="sxs-lookup"><span data-stu-id="c7ef7-511">Exchange Essentials</span></span>|
      |<span data-ttu-id="c7ef7-512">Exchange Foundation</span><span class="sxs-lookup"><span data-stu-id="c7ef7-512">Exchange Foundation</span></span>|
      |<span data-ttu-id="c7ef7-513">Exchange Online (P1)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-513">Exchange Online (P1)</span></span>|
      |<span data-ttu-id="c7ef7-514">Exchange Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-514">Exchange Online (Plan 1)</span></span>|
      |<span data-ttu-id="c7ef7-515">Exchange Online (plan 2)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-515">Exchange Online (Plan 2)</span></span>|
      |<span data-ttu-id="c7ef7-516">Archivage Exchange Online pour Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c7ef7-516">Exchange Online Archiving for Exchange Online</span></span>|
      |<span data-ttu-id="c7ef7-517">Archivage Exchange Online pour Exchange Server</span><span class="sxs-lookup"><span data-stu-id="c7ef7-517">Exchange Online Archiving for Exchange Server</span></span>|
      |<span data-ttu-id="c7ef7-518">Exchange Online Modules de modules utilisateur inactifs</span><span class="sxs-lookup"><span data-stu-id="c7ef7-518">Exchange Online Inactive User Add-on</span></span>|
      |<span data-ttu-id="c7ef7-519">Exchange Online Kiosk</span><span class="sxs-lookup"><span data-stu-id="c7ef7-519">Exchange Online Kiosk</span></span>|
      |<span data-ttu-id="c7ef7-520">Exchange Online Multi-Geo</span><span class="sxs-lookup"><span data-stu-id="c7ef7-520">Exchange Online Multi-Geo</span></span>|
      |<span data-ttu-id="c7ef7-521">Exchange Online (plan 1)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-521">Exchange Online Plan 1</span></span>|
      |<span data-ttu-id="c7ef7-522">Exchange Online POP</span><span class="sxs-lookup"><span data-stu-id="c7ef7-522">Exchange Online POP</span></span>|
      |<span data-ttu-id="c7ef7-523">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="c7ef7-523">Exchange Online Protection</span></span>|
      |<span data-ttu-id="c7ef7-524">Obstacles à l’information</span><span class="sxs-lookup"><span data-stu-id="c7ef7-524">Information Barriers</span></span>|
      |<span data-ttu-id="c7ef7-525">Protection des informations pour Office 365 – Premium</span><span class="sxs-lookup"><span data-stu-id="c7ef7-525">Information Protection for Office 365 - Premium</span></span>|
      |<span data-ttu-id="c7ef7-526">Protection des informations pour Office 365 – Standard</span><span class="sxs-lookup"><span data-stu-id="c7ef7-526">Information Protection for Office 365 - Standard</span></span>|
      |<span data-ttu-id="c7ef7-527">Informations par MyAnalytics</span><span class="sxs-lookup"><span data-stu-id="c7ef7-527">Insights by MyAnalytics</span></span>|
      |<span data-ttu-id="c7ef7-528">Microsoft 365 Audit avancé</span><span class="sxs-lookup"><span data-stu-id="c7ef7-528">Microsoft 365 Advanced Auditing</span></span>|
      |<span data-ttu-id="c7ef7-529">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="c7ef7-529">Microsoft Bookings</span></span>|
      |<span data-ttu-id="c7ef7-530">Microsoft Business Center</span><span class="sxs-lookup"><span data-stu-id="c7ef7-530">Microsoft Business Center</span></span>|
      |<span data-ttu-id="c7ef7-531">Microsoft MyAnalytics (complet)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-531">Microsoft MyAnalytics (Full)</span></span>|
      |<span data-ttu-id="c7ef7-532">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c7ef7-532">Office 365 Advanced eDiscovery</span></span>|
      |<span data-ttu-id="c7ef7-533">Microsoft Defender pour Office 365 (Plan 1)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-533">Microsoft Defender for Office 365 (Plan 1)</span></span>|
      |<span data-ttu-id="c7ef7-534">Microsoft Defender pour Office 365 (Plan 2)</span><span class="sxs-lookup"><span data-stu-id="c7ef7-534">Microsoft Defender for Office 365 (Plan 2)</span></span>|
      |<span data-ttu-id="c7ef7-535">Office 365 Privileged Access Management</span><span class="sxs-lookup"><span data-stu-id="c7ef7-535">Office 365 Privileged Access Management</span></span>|
      |<span data-ttu-id="c7ef7-536">Premium Chiffrement dans Office 365</span><span class="sxs-lookup"><span data-stu-id="c7ef7-536">Premium Encryption in Office 365</span></span>|
      ||
