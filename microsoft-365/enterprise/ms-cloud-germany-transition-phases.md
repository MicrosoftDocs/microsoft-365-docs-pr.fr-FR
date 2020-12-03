---
title: Actions et impacts sur les phases de migration
ms.author: andyber
author: andybergen
manager: laurawi
ms.date: 12/01/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_TLGs
description: 'Résumé : Découvrez les actions et les impacts des phases de migration de Microsoft Cloud Germany (Microsoft Cloud Deutschland) vers les services Office 365 dans la nouvelle région de centre de connaissances allemande.'
ms.openlocfilehash: 9ffdb0bbe60bdb96d6e110ac08cba4030272c7e9
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49551656"
---
# <a name="migration-phases-actions-and-impacts"></a><span data-ttu-id="b079f-103">Actions et impacts sur les phases de migration</span><span class="sxs-lookup"><span data-stu-id="b079f-103">Migration phases actions and impacts</span></span>

<span data-ttu-id="b079f-104">Les migrations client de Microsoft Cloud Deutschland vers la région de l’Allemagne des services Office 365 de Microsoft sont exécutées comme un ensemble d’actions configurées pour chaque charge de travail.</span><span class="sxs-lookup"><span data-stu-id="b079f-104">Tenant migrations from Microsoft Cloud Deutschland to the Germany region of Microsoft's Office 365 services are executed as a set of configured actions for each workload.</span></span> <span data-ttu-id="b079f-105">Ces actions permettent de s’assurer que les données et expériences critiques sont migrées vers les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-105">These actions ensure that critical data and experiences are migrated to the Office 365 services.</span></span> <span data-ttu-id="b079f-106">Une fois que votre client est ajouté à la file d’attente de migration, chaque charge de travail est effectuée comme un ensemble d’étapes exécutées sur le service principal.</span><span class="sxs-lookup"><span data-stu-id="b079f-106">After your tenant is added to the migration queue, each workload will be completed as a set of steps that are executed on the backend service.</span></span> <span data-ttu-id="b079f-107">Certaines charges de travail peuvent nécessiter des actions de l’administrateur (ou utilisateur), ou la migration peut affecter l’utilisation pour les phases qui sont exécutées et décrites dans [Comment la migration est-elle organisée ?](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span><span class="sxs-lookup"><span data-stu-id="b079f-107">Some workloads may require actions by the administrator (or user), or the migration may affect usage for the phases that are executed and discussed in [How is the migration organized?](ms-cloud-germany-transition.md#how-is-the-migration-organized)</span></span>

<span data-ttu-id="b079f-108">Les sections suivantes contiennent les actions et les effets des charges de travail au fur et à mesure des différentes phases de la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-108">The following sections contain actions and effects for workloads as they progress through various phases of the migration.</span></span> <span data-ttu-id="b079f-109">Passez en revue les tableaux et déterminez les actions ou les effets qui s’appliquent à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b079f-109">Review the tables and determine which actions or effects are applicable to your organization.</span></span> <span data-ttu-id="b079f-110">Assurez-vous que vous êtes prêt à exécuter les étapes dans les phases correspondantes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b079f-110">Ensure that you're prepared to execute the steps in the respective phases as required.</span></span> <span data-ttu-id="b079f-111">L’échec de l’exécution des étapes nécessaires peut entraîner une panne de service et retarder la migration vers les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-111">Failure to complete necessary steps may result in service outage and might delay completion of the migration to the Office 365 services.</span></span>

## <a name="exchange-online"></a><span data-ttu-id="b079f-112">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b079f-112">Exchange Online</span></span>

| <span data-ttu-id="b079f-113">Étape (s)</span><span class="sxs-lookup"><span data-stu-id="b079f-113">Step(s)</span></span> | <span data-ttu-id="b079f-114">Description</span><span class="sxs-lookup"><span data-stu-id="b079f-114">Description</span></span> | <span data-ttu-id="b079f-115">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b079f-115">Applies to</span></span> | <span data-ttu-id="b079f-116">Impact</span><span class="sxs-lookup"><span data-stu-id="b079f-116">Impact</span></span> |
|:-------|:-----|:-------|:-------|
| <span data-ttu-id="b079f-117">La nouvelle région Germany est ajoutée à la configuration existante de l’organisation, et les boîtes aux lettres sont déplacées vers les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-117">New Germany region is added to existing organization setup, and mailboxes are moved to Office 365 services.</span></span> | <span data-ttu-id="b079f-118">La configuration d’Exchange Online ajoute la nouvelle région locale allemande à l’organisation de transition.</span><span class="sxs-lookup"><span data-stu-id="b079f-118">Exchange Online configuration adds the new go-local German region to the transitioning organization.</span></span> <span data-ttu-id="b079f-119">Cette région des services Office 365 est définie par défaut, ce qui permet au service d’équilibrage de charge interne de redistribuer des boîtes aux lettres à la région par défaut appropriée dans les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-119">This Office 365 services region is set as default, which enables the internal load-balancing service to redistribute mailboxes to the appropriate default region in Office 365 services.</span></span> <span data-ttu-id="b079f-120">Dans cette transition, les utilisateurs des deux côtés (Allemagne ou services Office 365) se trouvent dans la même organisation et peuvent utiliser le point de terminaison de l’URL.</span><span class="sxs-lookup"><span data-stu-id="b079f-120">In this transition, users on either side (Germany or Office 365 services) are in the same organization and can use either URL endpoint.</span></span> | <span data-ttu-id="b079f-121">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b079f-121">Exchange Online</span></span> | <span data-ttu-id="b079f-122">-Faire migrer les utilisateurs et les services des URL d’Allemagne vers les URL des services Office 365 ( `https://outlook.office365.com` ).</span><span class="sxs-lookup"><span data-stu-id="b079f-122">- Transition users and services from Germany URLs to Office 365 services URLs (`https://outlook.office365.com`).</span></span> <br><br> <span data-ttu-id="b079f-123">-Les utilisateurs continueront à accéder au service via les URL d’Allemagne héritées lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-123">- Users will continue to access the service via legacy Germany URLs during the migration.</span></span> <span data-ttu-id="b079f-124">Aucune action immédiate n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b079f-124">No immediate action needed.</span></span> <br><br> <span data-ttu-id="b079f-125">-Les utilisateurs doivent commencer à utiliser le portail office.com pour les fonctionnalités d’Office Online (calendrier, courrier, personnes).</span><span class="sxs-lookup"><span data-stu-id="b079f-125">- Users should begin to use the office.com portal for Office Online features (Calendar, Mail, People).</span></span> <span data-ttu-id="b079f-126">La navigation vers les services qui ne sont pas encore migrés vers les services Office 365 ne fonctionne pas tant qu’elles n’ont pas été migrées.</span><span class="sxs-lookup"><span data-stu-id="b079f-126">Navigation to services that aren't yet migrated to Office 365 services won't function until migrated.</span></span> <br><br> <span data-ttu-id="b079f-127">-Outlook Web App ne fournit pas d’expérience de dossier public pendant la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-127">- Outlook Web App won't provide the public folder experience during migration.</span></span> |
|||||

<span data-ttu-id="b079f-128">Pour en savoir plus sur les différences entre les organisations en cours de migration et une fois la migration des ressources Exchange Online, consultez les informations contenues dans l' [expérience client lors de la migration vers les services Office 365 dans les nouvelles régions de centre de données allemand](ms-cloud-germany-transition-experience.md).</span><span class="sxs-lookup"><span data-stu-id="b079f-128">To find out more about the differences for organizations in migration and after Exchange Online resources are migrated, review the information in [Customer experience during the migration to Office 365 services in the new German datacenter regions](ms-cloud-germany-transition-experience.md).</span></span>

## <a name="exchange-online-protection"></a><span data-ttu-id="b079f-129">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b079f-129">Exchange Online Protection</span></span>

<span data-ttu-id="b079f-130">Les fonctionnalités Exchange Online Protection (EOP) principales sont copiées dans la nouvelle région Germany.</span><span class="sxs-lookup"><span data-stu-id="b079f-130">Back-end Exchange Online Protection (EOP) features are copied to new Germany region.</span></span> 

| <span data-ttu-id="b079f-131">Étape (s)</span><span class="sxs-lookup"><span data-stu-id="b079f-131">Step(s)</span></span> | <span data-ttu-id="b079f-132">Description</span><span class="sxs-lookup"><span data-stu-id="b079f-132">Description</span></span> | <span data-ttu-id="b079f-133">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b079f-133">Applies to</span></span> | <span data-ttu-id="b079f-134">Impact</span><span class="sxs-lookup"><span data-stu-id="b079f-134">Impact</span></span> |
|:-------|:-----|:-------|:-------|
| <span data-ttu-id="b079f-135">Migration du routage Exchange Online et du détail des messages historiques.</span><span class="sxs-lookup"><span data-stu-id="b079f-135">Migration of Exchange Online routing and historical message detail.</span></span> | <span data-ttu-id="b079f-136">Exchange Online permet le routage à partir d’hôtes externes vers Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-136">Exchange Online enables routing from external hosts to Office 365.</span></span> <span data-ttu-id="b079f-137">Les enregistrements MX externes sont transférés vers le service EOP.</span><span class="sxs-lookup"><span data-stu-id="b079f-137">The external MX records are transitioned to route to the EOP service.</span></span> <span data-ttu-id="b079f-138">Les détails de la configuration du client et de l’historique sont migrés.</span><span class="sxs-lookup"><span data-stu-id="b079f-138">Tenant configuration and historical details are migrated.</span></span> | <span data-ttu-id="b079f-139">Clients Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b079f-139">Exchange Online customers</span></span> | <span data-ttu-id="b079f-140">-Les entrées DNS gérées par Microsoft sont mises à jour à partir d’Office 365 Germany EOP vers les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-140">- Microsoft–managed DNS entries are updated from Office 365 Germany EOP to Office 365 services.</span></span> <br><br> <span data-ttu-id="b079f-141">-Les clients doivent attendre 30 jours après la migration de EOP Dual Write pour EOP.</span><span class="sxs-lookup"><span data-stu-id="b079f-141">- Customers should wait for 30 days after EOP dual write for EOP migration.</span></span> <span data-ttu-id="b079f-142">Sinon, il peut y avoir une perte de données.</span><span class="sxs-lookup"><span data-stu-id="b079f-142">Otherwise, there may be data loss.</span></span> |
|||||

## <a name="sharepoint-online"></a><span data-ttu-id="b079f-143">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="b079f-143">SharePoint Online</span></span>

<!--

| Step(s) | Description | Applies to | Impact |
|:-------|:-----|:-------|:-------|
| SharePoint and OneDrive are transitioned. | SharePoint and OneDrive are migrated from Microsoft Cloud Deutschland to Office 365 services in this phase. Existing Microsoft Cloud Deutschland URLs are preserved (for example, `contoso.sharepoint.de`). Tokens that were issued by Microsoft Cloud Deutschland or Office 365 services are valid during the transition. | SharePoint customers | - Content will be read-only for two brief periods (less than x minutes) during migration. During this time, expect a "you can't edit content" banner in SharePoint. <br><br> - The search index won't be preserved, and may take up to 10 days to be rebuilt. <br><br> - SharePoint/OneDrive content will be read-only for two brief periods (less than x minutes) during migration. Users will see a "you can't edit content" banner briefly during this time. <br><br> - The search index may be unavailable while the index is rebuilt. During this period, search queries might not return complete results. <br><br> - Existing sites are preserved. |
|||||

--> 

| <span data-ttu-id="b079f-144">Étape (s)</span><span class="sxs-lookup"><span data-stu-id="b079f-144">Step(s)</span></span> | <span data-ttu-id="b079f-145">Description</span><span class="sxs-lookup"><span data-stu-id="b079f-145">Description</span></span> | <span data-ttu-id="b079f-146">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b079f-146">Applies to</span></span> | <span data-ttu-id="b079f-147">Impact</span><span class="sxs-lookup"><span data-stu-id="b079f-147">Impact</span></span> |
|:-------|:-----|:-------|:-------|
| <span data-ttu-id="b079f-148">SharePoint et OneDrive sont en transition.</span><span class="sxs-lookup"><span data-stu-id="b079f-148">SharePoint and OneDrive are transitioned.</span></span> | <span data-ttu-id="b079f-149">SharePoint et OneDrive sont migrés de Microsoft Cloud Deutschland vers les services Office 365 dans cette phase.</span><span class="sxs-lookup"><span data-stu-id="b079f-149">SharePoint and OneDrive are migrated from Microsoft Cloud Deutschland to Office 365 services in this phase.</span></span> <span data-ttu-id="b079f-150">Les URL de Microsoft Cloud Deutschland existantes sont préservées (par exemple, `contoso.sharepoint.de` ).</span><span class="sxs-lookup"><span data-stu-id="b079f-150">Existing Microsoft Cloud Deutschland URLs are preserved (for example, `contoso.sharepoint.de`).</span></span> <span data-ttu-id="b079f-151">Les jetons émis par les services Microsoft Cloud Deutschland ou Office 365 sont valides pendant la transition.</span><span class="sxs-lookup"><span data-stu-id="b079f-151">Tokens that were issued by Microsoft Cloud Deutschland or Office 365 services are valid during the transition.</span></span> | <span data-ttu-id="b079f-152">Clients SharePoint</span><span class="sxs-lookup"><span data-stu-id="b079f-152">SharePoint customers</span></span> | <span data-ttu-id="b079f-153">-Le contenu sera en lecture seule pendant deux courtes périodes lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-153">- Content will be read-only for two brief periods during migration.</span></span> <span data-ttu-id="b079f-154">Pendant ce temps, attendez une bannière « vous ne pouvez pas modifier le contenu » dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b079f-154">During this time, expect a "you can't edit content" banner in SharePoint.</span></span> <br><br> <span data-ttu-id="b079f-155">-L’index de recherche ne sera pas conservé et la reconstruction peut prendre jusqu’à 10 jours.</span><span class="sxs-lookup"><span data-stu-id="b079f-155">- The search index won't be preserved, and may take up to 10 days to be rebuilt.</span></span> <br><br> <span data-ttu-id="b079f-156">-Le contenu SharePoint/OneDrive sera en lecture seule pendant deux courtes périodes lors de la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-156">- SharePoint/OneDrive content will be read-only for two brief periods during migration.</span></span> <span data-ttu-id="b079f-157">Les utilisateurs verront brièvement une bannière « vous ne pouvez pas modifier le contenu » pendant ce temps.</span><span class="sxs-lookup"><span data-stu-id="b079f-157">Users will see a "you can't edit content" banner briefly during this time.</span></span> <br><br> <span data-ttu-id="b079f-158">-L’index de recherche est peut-être indisponible pendant la reconstruction de l’index.</span><span class="sxs-lookup"><span data-stu-id="b079f-158">- The search index may be unavailable while the index is rebuilt.</span></span> <span data-ttu-id="b079f-159">Pendant cette période, il se peut que les requêtes de recherche ne renvoient pas les résultats complets.</span><span class="sxs-lookup"><span data-stu-id="b079f-159">During this period, search queries might not return complete results.</span></span> <br><br> <span data-ttu-id="b079f-160">-Les sites existants sont conservés.</span><span class="sxs-lookup"><span data-stu-id="b079f-160">- Existing sites are preserved.</span></span> |
|||||


## <a name="skype-for-business-online"></a><span data-ttu-id="b079f-161">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="b079f-161">Skype for Business Online</span></span>

| <span data-ttu-id="b079f-162">Étape (s)</span><span class="sxs-lookup"><span data-stu-id="b079f-162">Step(s)</span></span> | <span data-ttu-id="b079f-163">Description</span><span class="sxs-lookup"><span data-stu-id="b079f-163">Description</span></span> | <span data-ttu-id="b079f-164">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b079f-164">Applies to</span></span> | <span data-ttu-id="b079f-165">Impact</span><span class="sxs-lookup"><span data-stu-id="b079f-165">Impact</span></span> |
|:-------|:-----|:-------|:-------|
| <span data-ttu-id="b079f-166">Migration de Skype entreprise vers Teams.</span><span class="sxs-lookup"><span data-stu-id="b079f-166">Migration of Skype for Business to Teams.</span></span> | <span data-ttu-id="b079f-167">Les clients Skype entreprise existants sont migrés vers les services Office 365 en Europe, puis transférés vers Microsoft teams dans la région d’Allemagne des services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-167">Existing Skype for Business customers are migrated to Office 365 services in Europe and then transitioned to Microsoft Teams in the Germany region of Office 365 services.</span></span> | <span data-ttu-id="b079f-168">Clients Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="b079f-168">Skype for Business customers</span></span> | <span data-ttu-id="b079f-169">-Les utilisateurs ne peuvent pas se connecter à Skype entreprise à la date de la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-169">- Users won't be able to sign in to Skype for Business on the migration date.</span></span> <span data-ttu-id="b079f-170">10 jours avant la migration, nous allons informer les utilisateurs finaux via intrabande sur le client Skype entreprise qu’ils seront mis à niveau vers Teams.</span><span class="sxs-lookup"><span data-stu-id="b079f-170">Ten days before migration, we'll notify end users via in-band on the Skype for Business client that they'll be upgraded to Teams.</span></span> <span data-ttu-id="b079f-171">Nous publierons également dans le centre d’administration que ces modifications auront lieu après 10 jours.</span><span class="sxs-lookup"><span data-stu-id="b079f-171">We'll also post in Admin Center that these changes will occur after the 10 days.</span></span> <br><br> <span data-ttu-id="b079f-172">-La configuration de la stratégie est migrée.</span><span class="sxs-lookup"><span data-stu-id="b079f-172">- Policy configuration is migrated.</span></span> <br><br> <span data-ttu-id="b079f-173">-Les utilisateurs sont migrés vers teams et ne disposent plus de Skype entreprise après la migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-173">- Users will be migrated to Teams and will no longer have Skype for Business after migration.</span></span> <br><br> <span data-ttu-id="b079f-174">-Le client de bureau teams doit être installé sur les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b079f-174">- Users must have the Teams desktop client installed.</span></span> <span data-ttu-id="b079f-175">L’installation aura lieu au cours des 10 jours suivant la stratégie sur l’infrastructure Skype entreprise, mais si cette opération échoue, les utilisateurs devront toujours télécharger le client ou se connecter avec un navigateur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b079f-175">Installation will happen during the 10 days via policy on the Skype for Business infrastructure, but if this fails, users will still need to download the client or connect with a supported browser.</span></span> <br><br> <span data-ttu-id="b079f-176">-Les contacts et les réunions sont migrés vers Teams.</span><span class="sxs-lookup"><span data-stu-id="b079f-176">- Contacts and meetings will be migrated to Teams.</span></span> <br><br> <span data-ttu-id="b079f-177">-Les utilisateurs ne peuvent pas se connecter à Skype entreprise entre les transitions de service de temps et les services Office 365, et non jusqu’à ce que les entrées DNS du client soient terminées.</span><span class="sxs-lookup"><span data-stu-id="b079f-177">- Users won't be able to sign in to Skype for Business between time service transitions to Office 365 services, and not until customer DNS entries are completed.</span></span> <br><br> <span data-ttu-id="b079f-178">-Les contacts et les réunions existantes continueront de fonctionner en tant que réunions Skype entreprise.</span><span class="sxs-lookup"><span data-stu-id="b079f-178">- Contacts and existing meetings will continue to function as Skype for Business meetings.</span></span> |
|||||
        
## <a name="subscription"></a><span data-ttu-id="b079f-179">Abonnement</span><span class="sxs-lookup"><span data-stu-id="b079f-179">Subscription</span></span>

| <span data-ttu-id="b079f-180">Étape (s)</span><span class="sxs-lookup"><span data-stu-id="b079f-180">Step(s)</span></span> | <span data-ttu-id="b079f-181">Description</span><span class="sxs-lookup"><span data-stu-id="b079f-181">Description</span></span> | <span data-ttu-id="b079f-182">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b079f-182">Applies to</span></span> | <span data-ttu-id="b079f-183">Impact</span><span class="sxs-lookup"><span data-stu-id="b079f-183">Impact</span></span> |
|:-------|:-----|:-------|:-------|
| <span data-ttu-id="b079f-184">Nous ne pouvons pas migrer les clients sans consentement.</span><span class="sxs-lookup"><span data-stu-id="b079f-184">We can't migrate customers without consent.</span></span> | <span data-ttu-id="b079f-185">Microsoft gagne le droit de procéder à une migration de deux manières, ce qui permet à Microsoft d’orchestrer la transition des données et des services à l’instance Office 365 services.</span><span class="sxs-lookup"><span data-stu-id="b079f-185">Microsoft gains the right to migrate in one of two ways, which enables Microsoft to orchestrate the transition of data and services to the Office 365 services instance.</span></span> <br> <span data-ttu-id="b079f-186">L’administrateur opte pour la migration basée sur Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b079f-186">The admin opts-in to the Microsoft-driven migration.</span></span> <br> <span data-ttu-id="b079f-187">Les clients renouvellent les abonnements dans leur client Deutschland Cloud Microsoft après le 1er mai 2020.</span><span class="sxs-lookup"><span data-stu-id="b079f-187">Customers renew any subscriptions in their Microsoft Cloud Deutschland tenant after May 1, 2020.</span></span> <span data-ttu-id="b079f-188">Nous informerons ces clients de la migration par mois, patientent 30 jours pour permettre aux clients d’annuler, puis d’accepter directement les suivis dans ICM.</span><span class="sxs-lookup"><span data-stu-id="b079f-188">We'll notify these customers of the migration right each month, wait 30 days to give customers a chance to cancel, and then directly opt-in, tracked in ICM.</span></span> | <span data-ttu-id="b079f-189">Tous les clients Office</span><span class="sxs-lookup"><span data-stu-id="b079f-189">All Office Customers</span></span> | <span data-ttu-id="b079f-190">-Le client est marqué comme étant accepté pour la migration, et le centre d’administration affiche la confirmation.</span><span class="sxs-lookup"><span data-stu-id="b079f-190">- Tenant is marked as consented for migration, and Admin Center displays confirmation.</span></span> <br><br> <span data-ttu-id="b079f-191">-L’accusé de réception est publié sur le client du centre de messages de Cloud Germany.</span><span class="sxs-lookup"><span data-stu-id="b079f-191">- Acknowledgment is posted to Cloud Germany Message Center Tenant.</span></span> <span data-ttu-id="b079f-192">La configuration du service se poursuit à partir des points de terminaison Deutschland Cloud de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b079f-192">Service configuration continues from Microsoft Cloud Deutschland endpoints.</span></span> <br><br> <span data-ttu-id="b079f-193">-Surveillez le centre de messages pour les mises à jour de l’état des phases de migration.</span><span class="sxs-lookup"><span data-stu-id="b079f-193">- Monitor Message Center for updates on Migration phase status.</span></span> |
| <span data-ttu-id="b079f-194">Les abonnements sont transférés et les licences sont réaffectées.</span><span class="sxs-lookup"><span data-stu-id="b079f-194">Subscriptions are transferred, and licenses are reassigned.</span></span> | <span data-ttu-id="b079f-195">Une fois le client transféré vers les services Office 365, les abonnements aux services Office 365 correspondants sont achetés pour les abonnements Microsoft Cloud Deutschland transférés.</span><span class="sxs-lookup"><span data-stu-id="b079f-195">After the tenant is transitioned to Office 365 services, corresponding Office 365 services subscriptions are purchased for the transferred Microsoft Cloud Deutschland subscriptions.</span></span> <span data-ttu-id="b079f-196">Les utilisateurs disposant de licences Microsoft Cloud Deutschland seront affectées aux licences des services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-196">Users with assigned Microsoft Cloud Deutschland licenses will be assigned Office 365 services licenses.</span></span> <span data-ttu-id="b079f-197">Les abonnements Microsoft Cloud Deutschland hérités sont supprimés du client des services Office 365 à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b079f-197">Legacy Microsoft Cloud Deutschland subscriptions are removed from the Office 365 services tenant on completion.</span></span> | <span data-ttu-id="b079f-198">Tous les clients Office</span><span class="sxs-lookup"><span data-stu-id="b079f-198">All Office customers</span></span> | <span data-ttu-id="b079f-199">-Les modifications apportées aux abonnements existants sont bloquées (par exemple, aucune nouvelle inscription d’abonnement ou modification du nombre de sièges) pendant cette phase.</span><span class="sxs-lookup"><span data-stu-id="b079f-199">- Changes to existing subscriptions will be blocked (for example, no new subscription purchases or seat count changes) during this phase.</span></span> <br><br> <span data-ttu-id="b079f-200">-Les modifications apportées aux attributions de licence sont bloquées.</span><span class="sxs-lookup"><span data-stu-id="b079f-200">- License assignment changes will be blocked.</span></span> <br><br> <span data-ttu-id="b079f-201">-L’abonnement Microsoft Cloud Deutschland est migré vers l’abonnement aux services Office 365 correspondant.</span><span class="sxs-lookup"><span data-stu-id="b079f-201">- The Microsoft Cloud Deutschland subscription will be migrated to corresponding Office 365 services subscription.</span></span> <span data-ttu-id="b079f-202">L’offre Office 365 services de cet abonnement est définie par Microsoft (également appelée _mappage des offres_).</span><span class="sxs-lookup"><span data-stu-id="b079f-202">The Office 365 services offer of that subscription is defined by Microsoft (also known as _Offer mapping_).</span></span> <br><br> <span data-ttu-id="b079f-203">-Le nombre de fonctionnalités (plans de service) offerts par les services Office 365 peut être plus important que dans l’offre Microsoft Cloud Deutschland d’origine.</span><span class="sxs-lookup"><span data-stu-id="b079f-203">- The number of features (service plans) offered by Office 365 services can be larger than in the original Microsoft Cloud Deutschland offer.</span></span> <span data-ttu-id="b079f-204">Les licences utilisateur dans les services Office 365 seront équivalentes aux fonctionnalités similaires de Microsoft Cloud Deutschland (plans de service).</span><span class="sxs-lookup"><span data-stu-id="b079f-204">User licenses in Office 365 services will be equivalently assigned to similar Microsoft Cloud Deutschland features (service plans).</span></span> <span data-ttu-id="b079f-205">Les licences utilisateur de tous les utilisateurs seront automatiquement attribuées aux nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b079f-205">User licenses of all users will be automatically assigned to the new features.</span></span> <span data-ttu-id="b079f-206">Le cas échéant, l’administrateur doit prendre une mesure explicite pour désactiver ces licences.</span><span class="sxs-lookup"><span data-stu-id="b079f-206">The admin needs to take an explicit action to disable those licenses, if needed.</span></span> <br><br> <span data-ttu-id="b079f-207">-Lorsque la migration des abonnements est terminée, les abonnements Office 365 services et Germany seront visibles dans le portail d’administration d’Office 365, dont l’état des abonnements en Allemagne est _annulé._</span><span class="sxs-lookup"><span data-stu-id="b079f-207">- When subscription migration is complete, both Office 365 services and Germany subscriptions will be visible in the Office 365 Admin Portal, with the status of Germany subscriptions as _deprovisioned_.</span></span> <br><br> <span data-ttu-id="b079f-208">-Les utilisateurs se verront affecter des licences qui sont liées aux nouveaux abonnements aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-208">- Users will be reassigned licenses that are tied to the new Office 365 services subscriptions.</span></span> <span data-ttu-id="b079f-209">Tous les processus client qui ont des dépendances sur les abonnements Germany ou les GUID SKU sont rompus et doivent être modifiés avec l’offre Office 365 services.</span><span class="sxs-lookup"><span data-stu-id="b079f-209">Any customer processes that have dependencies on Germany subscriptions or SKU GUIDs will be broken and need to be revised with the Office 365 services offering.</span></span> <br><br> <span data-ttu-id="b079f-210">-Les nouveaux abonnements dans les services Office 365 seront achetés avec le nouveau terme (mensuel/trimestriel/annuel), et le client recevra un remboursement progressif pour le solde non utilisé de l’abonnement Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="b079f-210">- New subscriptions in the Office 365 services will be purchased with the new term (monthly/quarterly/yearly), and the customer will receive a prorated refund for the unused balance of the Microsoft Cloud Deutschland subscription.</span></span> <br><br> <span data-ttu-id="b079f-211">-Les locataires Microsoft Cloud Deutschland ne seront pas migrés.</span><span class="sxs-lookup"><span data-stu-id="b079f-211">- Partner Microsoft Cloud Deutschland tenants won't be migrated.</span></span> <span data-ttu-id="b079f-212">Les clients CSP seront migrés vers les services Office 365 sous le nouveau client des services Office 365 du même partenaire.</span><span class="sxs-lookup"><span data-stu-id="b079f-212">CSP customers will be migrated to Office 365 services under the new Office 365 services tenant of the same partner.</span></span> <span data-ttu-id="b079f-213">Après la migration du client, le partenaire peut gérer ce client uniquement à partir du client des services Office 365.</span><span class="sxs-lookup"><span data-stu-id="b079f-213">After customer migration, the partner can manage this customer only from the Office 365 services tenant.</span></span> <br><br> <span data-ttu-id="b079f-214">-Une fonctionnalité supplémentaire est disponible (par exemple, le planificateur Microsoft et Microsoft Flow), sauf si elle est désactivée par l’administrateur client. Pour plus d’informations sur la désactivation des plans de service attribués aux licences des utilisateurs, consultez la rubrique [désactiver l’accès aux services Microsoft 365 lors de l’affectation de licences utilisateur](disable-access-to-services-while-assigning-user-licenses.md).</span><span class="sxs-lookup"><span data-stu-id="b079f-214">- Additional functionality is available (for example, Microsoft Planner and Microsoft Flow), unless disabled by tenant admin. For information about how to disable service plans that are assigned to users' licenses, see [Disable access to Microsoft 365 services while assigning user licenses](disable-access-to-services-while-assigning-user-licenses.md).</span></span>  |
|||||

## <a name="next-step"></a><span data-ttu-id="b079f-215">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="b079f-215">Next step</span></span>

[<span data-ttu-id="b079f-216">Effectuer des tâches supplémentaires préalables</span><span class="sxs-lookup"><span data-stu-id="b079f-216">Perform additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)

## <a name="more-information"></a><span data-ttu-id="b079f-217">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b079f-217">More information</span></span>

<span data-ttu-id="b079f-218">Mise en route :</span><span class="sxs-lookup"><span data-stu-id="b079f-218">Getting started:</span></span>

- [<span data-ttu-id="b079f-219">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centre de connaissances allemand</span><span class="sxs-lookup"><span data-stu-id="b079f-219">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="b079f-220">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="b079f-220">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="b079f-221">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="b079f-221">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)
- [<span data-ttu-id="b079f-222">Expérience client lors de la migration</span><span class="sxs-lookup"><span data-stu-id="b079f-222">Customer experience during the migration</span></span>](ms-cloud-germany-transition-experience.md)

<span data-ttu-id="b079f-223">Navigation par le biais de la transition :</span><span class="sxs-lookup"><span data-stu-id="b079f-223">Moving through the transition:</span></span>

- [<span data-ttu-id="b079f-224">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="b079f-224">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="b079f-225">Informations supplémentaires pour les [services](ms-cloud-germany-transition-add-general.md), les [appareils](ms-cloud-germany-transition-add-devices.md), les [expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="b079f-225">Additional information for [services](ms-cloud-germany-transition-add-general.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="b079f-226">Applications Cloud :</span><span class="sxs-lookup"><span data-stu-id="b079f-226">Cloud apps:</span></span>

- [<span data-ttu-id="b079f-227">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b079f-227">Dynamics 365 migration program information</span></span>](https://aka.ms/d365ceoptin)
- [<span data-ttu-id="b079f-228">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="b079f-228">Power BI migration program information</span></span>](https://aka.ms/pbioptin)
- [<span data-ttu-id="b079f-229">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b079f-229">Getting started with your Microsoft Teams upgrade</span></span>](https://aka.ms/SkypeToTeams-Home)