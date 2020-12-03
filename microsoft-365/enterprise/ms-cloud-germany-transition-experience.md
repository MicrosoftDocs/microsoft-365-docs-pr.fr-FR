---
title: Expérience client pendant la migration vers les services Office 365 dans les nouvelles régions de centre de données allemandes
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
ms.assetid: 706d5449-45e5-4b0c-a012-ab60501899ad
description: 'Résumé : Découvrez l’expérience de passage de Microsoft Cloud Germany (Microsoft Cloud Deutschland) aux services Office 365 dans la nouvelle région de centre de connaissances allemande.'
ms.openlocfilehash: a44fbe504a9a710856deeb3baf258feb124ce7ae
ms.sourcegitcommit: 38d828ae8d4350ae774a939c8decf30cb36c3bea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2020
ms.locfileid: "49551694"
---
# <a name="customer-experience-during-the-migration-to-office-365-services-in-the-new-german-datacenter-regions"></a><span data-ttu-id="662b4-103">Expérience client pendant la migration vers les services Office 365 dans les nouvelles régions de centre de données allemandes</span><span class="sxs-lookup"><span data-stu-id="662b4-103">Customer experience during the migration to Office 365 services in the new German datacenter regions</span></span>

<span data-ttu-id="662b4-104">Les migrations client sont conçues pour avoir un impact minimal sur les administrateurs et les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="662b4-104">Tenant migrations are designed to have minimal effect on administrators and users.</span></span> <span data-ttu-id="662b4-105">Toutefois, il existe des facteurs à prendre en compte pour chaque charge de travail.</span><span class="sxs-lookup"><span data-stu-id="662b4-105">However, there are considerations for each workload.</span></span> <span data-ttu-id="662b4-106">Consultez les sections suivantes pour mieux comprendre l’expérience de migration pour les charges de travail.</span><span class="sxs-lookup"><span data-stu-id="662b4-106">Please review the following sections to have a better understanding of the migration experience for the workloads.</span></span>

<span data-ttu-id="662b4-107">Vous trouverez ci-dessous les principales différences entre Microsoft Cloud Deutschland et les services Office 365 dans les nouvelles régions de centre de connaissances allemand.</span><span class="sxs-lookup"><span data-stu-id="662b4-107">Following are the key differences between Microsoft Cloud Deutschland and Office 365 services in the new German datacenter regions.</span></span>

| <span data-ttu-id="662b4-108">Catégorie</span><span class="sxs-lookup"><span data-stu-id="662b4-108">Category</span></span> | <span data-ttu-id="662b4-109">Microsoft Cloud Deutschland (Microsoft Cloud Deutschland)</span><span class="sxs-lookup"><span data-stu-id="662b4-109">Microsoft Cloud Deutschland (Microsoft Cloud Deutschland)</span></span> | <span data-ttu-id="662b4-110">Services Office 365 dans les nouvelles régions de centre de données allemandes</span><span class="sxs-lookup"><span data-stu-id="662b4-110">Office 365 services in the new German datacenter regions</span></span> |
|:-------|:-----|:-------|
| <span data-ttu-id="662b4-111">Services Microsoft 365 disponibles pour un abonnement avec un seul client Office 365</span><span class="sxs-lookup"><span data-stu-id="662b4-111">Microsoft 365 services available for subscription with just one Office 365 tenant</span></span> | <span data-ttu-id="662b4-112">15 services</span><span class="sxs-lookup"><span data-stu-id="662b4-112">15 services</span></span> | <span data-ttu-id="662b4-113">29 services</span><span class="sxs-lookup"><span data-stu-id="662b4-113">29 services</span></span> <br><br> <span data-ttu-id="662b4-114">Pour plus d’informations, voir [qu’est-ce que la disponibilité du service entre les différentes offres de service Cloud Office 365 ?](ms-cloud-germany-transition.md#serv-avail).</span><span class="sxs-lookup"><span data-stu-id="662b4-114">For more information, see [What is the service availability between the different Office 365 cloud service offerings?](ms-cloud-germany-transition.md#serv-avail).</span></span> |
| <span data-ttu-id="662b4-115">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="662b4-115">New features</span></span> | <span data-ttu-id="662b4-116">Aucune nouvelle fonctionnalité n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="662b4-116">No new features are available.</span></span> | <span data-ttu-id="662b4-117">Les nouvelles fonctionnalités seront disponibles conformément aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-117">New features will be available consistent with Office 365 services.</span></span> |
| <span data-ttu-id="662b4-118">Administrateur de données</span><span class="sxs-lookup"><span data-stu-id="662b4-118">Data trustee</span></span> | <span data-ttu-id="662b4-119">Oui</span><span class="sxs-lookup"><span data-stu-id="662b4-119">Yes</span></span> | <span data-ttu-id="662b4-120">Non</span><span class="sxs-lookup"><span data-stu-id="662b4-120">No</span></span> |
| <span data-ttu-id="662b4-121">Collaboration entre clients Office 365 du monde entier</span><span class="sxs-lookup"><span data-stu-id="662b4-121">Cross-tenant collaboration with global Office 365 tenants</span></span> | <span data-ttu-id="662b4-122">Non</span><span class="sxs-lookup"><span data-stu-id="662b4-122">No</span></span> | <span data-ttu-id="662b4-123">Oui</span><span class="sxs-lookup"><span data-stu-id="662b4-123">Yes</span></span> |
| <span data-ttu-id="662b4-124">Résidence des données client</span><span class="sxs-lookup"><span data-stu-id="662b4-124">Customer data residency</span></span> | <span data-ttu-id="662b4-125">Les données client seront stockées uniquement dans les centres de données allemands.</span><span class="sxs-lookup"><span data-stu-id="662b4-125">Customer data will be stored solely within German data centers.</span></span> | <span data-ttu-id="662b4-126">Microsoft stockera les données client suivantes au repos exclusivement en Allemagne :</span><span class="sxs-lookup"><span data-stu-id="662b4-126">Microsoft will store the following Customer Data at rest exclusively within Germany:</span></span> <ul><li> <span data-ttu-id="662b4-127">Contenu de boîte aux lettres Exchange Online (corps de courrier électronique, entrées de calendrier et contenu de pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="662b4-127">Exchange Online mailbox content (e-mail body, calendar entries, and the content of e-mail attachments)</span></span> </li><li> <span data-ttu-id="662b4-128">Contenu de site SharePoint Online et fichiers stockés dans ce site, et fichiers téléchargés vers OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="662b4-128">SharePoint Online site content and the files stored within that site, and files uploaded to OneDrive for Business</span></span> </li></ul> |
| <span data-ttu-id="662b4-129">Conditions applicables</span><span class="sxs-lookup"><span data-stu-id="662b4-129">Applicable terms</span></span> | <span data-ttu-id="662b4-130">[Conditions des services en ligne](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) avec ce [supplément](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=64)</span><span class="sxs-lookup"><span data-stu-id="662b4-130">[Online Services Terms](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) with this [supplement](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=64)</span></span> | [<span data-ttu-id="662b4-131">Conditions d’utilisation d’Online Services</span><span class="sxs-lookup"><span data-stu-id="662b4-131">Online Services Terms</span></span>](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46) |
||||

## <a name="azure-active-directory"></a><span data-ttu-id="662b4-132">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="662b4-132">Azure Active Directory</span></span>

<span data-ttu-id="662b4-133">Ce qui ne change pas :</span><span class="sxs-lookup"><span data-stu-id="662b4-133">What isn't changing:</span></span>

- <span data-ttu-id="662b4-134">Le domaine initial client (par exemple, `contoso.onmicrosoft.de` ) avec un ID de client (Guid) et des domaines personnalisés est conservé après la migration.</span><span class="sxs-lookup"><span data-stu-id="662b4-134">Tenant initial domain (such as `contoso.onmicrosoft.de`) with tenant ID (GUID) and custom domains will persist after the migration.</span></span> 

- <span data-ttu-id="662b4-135">Les demandes d’authentification pour les ressources migrées vers les services Office 365 sont accordées par le service d’authentification Azure des services Office 365 ( `login.microsoftonline.com` ).</span><span class="sxs-lookup"><span data-stu-id="662b4-135">Authentication requests for resources that are migrated to Office 365 services are granted by the Office 365 services Azure authentication service (`login.microsoftonline.com`).</span></span> <span data-ttu-id="662b4-136">Au cours de la migration, les ressources qui restent dans Office 365 Germany sont authentifiées par le service Allemagne Azure existant ( `login.microsoftonline.de` ).</span><span class="sxs-lookup"><span data-stu-id="662b4-136">During the migration, resources that remain still in Office 365 Germany are authenticated by the existing Germany Azure service (`login.microsoftonline.de`).</span></span>

<span data-ttu-id="662b4-137">Considérations à noter :</span><span class="sxs-lookup"><span data-stu-id="662b4-137">Considerations to note:</span></span>

- <span data-ttu-id="662b4-138">Pour les comptes de domaine géré, une fois que la copie du client Azure Active Directory (Azure AD) initial est terminée (ce qui est la première étape de la migration Azure AD vers le service Azure AD service Office 365 services), les modifications de mot de passe, les modifications de réinitialisation de mot de passe 365 en libre-service et les réinitialisations de mot</span><span class="sxs-lookup"><span data-stu-id="662b4-138">For managed domain accounts, after copying of the initial Azure Active Directory (Azure AD) tenant is complete (which is the first step of Azure AD migration to the Office 365 services Azure AD service), password changes, self-service password reset (SSPR) changes, and password resets by administrators must be done from the Office 365 service portals.</span></span> <span data-ttu-id="662b4-139">Les demandes de mise à jour des mots de passe à partir du service d’Allemagne ne réussissent pas à ce stade, car le client Azure AD a été migré vers les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-139">Requests to update passwords from the Germany service won't succeed at this point, because the Azure AD tenant has been migrated to Office 365 services.</span></span> <span data-ttu-id="662b4-140">Les réinitialisations des mots de passe de domaine fédérés ne sont pas affectées, car elles sont terminées dans l’annuaire local.</span><span class="sxs-lookup"><span data-stu-id="662b4-140">Resets of federated domain passwords aren't affected, because these are completed in the on-premises directory.</span></span>

- <span data-ttu-id="662b4-141">Les connexions Azure sont présentées dans le portail auquel l’utilisateur tente d’accéder.</span><span class="sxs-lookup"><span data-stu-id="662b4-141">Azure sign-ins are presented in the portal where the user attempts access.</span></span> <span data-ttu-id="662b4-142">Les journaux d’audit sont disponibles uniquement à partir du point de terminaison des services Office 365 après une transition.</span><span class="sxs-lookup"><span data-stu-id="662b4-142">Audit logs are available from only the Office 365 services endpoint after transition.</span></span> <span data-ttu-id="662b4-143">Avant d’effectuer la migration jusqu’à la fin de la migration, vous devez enregistrer les journaux de connexion et d’audit à partir du portail Microsoft Cloud Deutschland.</span><span class="sxs-lookup"><span data-stu-id="662b4-143">Before migration through to the completion of migration, you should save sign-in and audit logs from the Microsoft Cloud Deutschland portal.</span></span>

- <span data-ttu-id="662b4-144">Les réinitialisations de mot de passe, les modifications de mot de passe, la réinitialisation du mot de passe par un administrateur pour les organisations gérées (qui n’utilisent pas Active Directory Federation Services) doivent être effectuées via le portail des services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-144">Password resets, password changes, password reset by an administrator for managed organizations (that are not using Active Directory Federation Services) must be performed via the Office 365 services portal.</span></span> <span data-ttu-id="662b4-145">Les tentatives des utilisateurs qui accèdent aux portails Microsoft Cloud Deutschland pour réinitialiser les mots de passe échoueront.</span><span class="sxs-lookup"><span data-stu-id="662b4-145">Attempts by users who access Microsoft Cloud Deutschland portals to reset passwords will fail.</span></span>

- <span data-ttu-id="662b4-146">General Data Protection Regulation (RGPD) les demandes des personnes concernées (DSR) sont exécutées à partir du portail d’administration Azure des services Office 365 pour les demandes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="662b4-146">General Data Protection Regulation (GDPR) Data Subject Requests (DSRs) are executed from the Office 365 services Azure admin portal for future requests.</span></span> <span data-ttu-id="662b4-147">Toute donnée de diagnostic héritée ou non client résidente dans Microsoft Cloud Deutschland est supprimée au moins 30 jours.</span><span class="sxs-lookup"><span data-stu-id="662b4-147">Any legacy or non-customer diagnostic data that is resident in Microsoft Cloud Deutschland is deleted at or before 30 days.</span></span>

## <a name="subscriptions--licenses"></a><span data-ttu-id="662b4-148">Abonnements & des licences</span><span class="sxs-lookup"><span data-stu-id="662b4-148">Subscriptions & Licenses</span></span>

- <span data-ttu-id="662b4-149">Les abonnements Office 365 et Dynamics de Microsoft Cloud Deutschland sont transférés vers la région allemande avec le réadressage Azure AD.</span><span class="sxs-lookup"><span data-stu-id="662b4-149">Office 365 and Dynamics subscriptions from Microsoft Cloud Deutschland are transitioned to the German region with the Azure AD relocation.</span></span> <span data-ttu-id="662b4-150">L’organisation est ensuite mise à jour pour refléter les nouveaux abonnements aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-150">The organization is then updated to reflect new Office 365 services subscriptions.</span></span> <span data-ttu-id="662b4-151">Lors du processus de transfert d’abonnement Brief, les modifications apportées aux abonnements sont bloquées.</span><span class="sxs-lookup"><span data-stu-id="662b4-151">During the brief subscription transfer process, changes to subscriptions are blocked.</span></span>

- <span data-ttu-id="662b4-152">Le client étant transféré vers les services Office 365, ses abonnements et licences spécifiques à l’Allemagne sont standardisés avec les nouvelles offres de services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-152">As the tenant is transitioned to Office 365 services, its Germany-specific subscriptions and licenses are standardized with new Office 365 services offerings.</span></span> <span data-ttu-id="662b4-153">Les abonnements aux services Office 365 correspondants sont achetés pour les abonnements Germany transférés.</span><span class="sxs-lookup"><span data-stu-id="662b4-153">Corresponding Office 365 services subscriptions are purchased for the transferred Germany subscriptions.</span></span> <span data-ttu-id="662b4-154">Les utilisateurs disposant de licences Germany se verront attribuer des licences Office 365 services.</span><span class="sxs-lookup"><span data-stu-id="662b4-154">Users who have Germany licenses will be assigned Office 365 services licenses.</span></span> <span data-ttu-id="662b4-155">Une fois l’opération terminée, les abonnements d’Allemagne hérités sont annulés et supprimés du client des services Office 365 actuels.</span><span class="sxs-lookup"><span data-stu-id="662b4-155">Upon completion, legacy Germany subscriptions are canceled and removed from the current Office 365 services tenant.</span></span>

- <span data-ttu-id="662b4-156">Après la migration des charges de travail individuelles, des fonctionnalités supplémentaires sont mises à disposition via les services Office 365 (tels que le planificateur Microsoft et Microsoft Flow) en raison des nouveaux abonnements aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-156">After migration of the individual workloads, additional functionality is made available through the Office 365 services (such as Microsoft Planner and Microsoft Flow) because of the new Office 365 services subscriptions.</span></span> <span data-ttu-id="662b4-157">Si cela est approprié pour votre organisation, l’administrateur du client ou de la gestion des licences peut désactiver les nouveaux plans de service lorsque vous planifiez la gestion des modifications afin de présenter les nouveaux services.</span><span class="sxs-lookup"><span data-stu-id="662b4-157">If appropriate for your organization, the tenant or licensing administrator can disable new service plans as you plan for change management to introduce the new services.</span></span> <span data-ttu-id="662b4-158">Pour obtenir des instructions sur la désactivation des plans de service attribués aux licences des utilisateurs, consultez la rubrique [désactiver l’accès aux services Microsoft 365 lors de l’affectation de licences utilisateur](https://docs.microsoft.com/office365/enterprise/powershell/disable-access-to-services-while-assigning-user-licenses).</span><span class="sxs-lookup"><span data-stu-id="662b4-158">For guidance on how to disable service plans that are assigned to users' licenses, see [Disable access to Microsoft 365 services while assigning user licenses](https://docs.microsoft.com/office365/enterprise/powershell/disable-access-to-services-while-assigning-user-licenses).</span></span>

## <a name="exchange-online"></a><span data-ttu-id="662b4-159">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="662b4-159">Exchange Online</span></span>

- <span data-ttu-id="662b4-160">Les URL de ressource Exchange passent du point de terminaison d’Allemagne hérité `outlook.office.de` au point de terminaison des services Office 365 `outlook.office365.com` après la migration.</span><span class="sxs-lookup"><span data-stu-id="662b4-160">Exchange resource URLs transition from the legacy Germany endpoint `outlook.office.de` to the Office 365 services endpoint `outlook.office365.com` after the migration.</span></span> <span data-ttu-id="662b4-161">Vos utilisateurs peuvent accéder à leur boîte aux lettres migrée à l’aide de l’URL héritée jusqu’à ce que la migration soit terminée.</span><span class="sxs-lookup"><span data-stu-id="662b4-161">Your users may access their migrated mailbox by using the legacy URL until the migration completes.</span></span> <span data-ttu-id="662b4-162">Les clients doivent faire passer les utilisateurs à la nouvelle URL dès que possible après que la migration Exchange commence à éviter de gêner le retrait de l’environnement de l’Allemagne.</span><span class="sxs-lookup"><span data-stu-id="662b4-162">Customers should transition users to the new URL as soon as possible after Exchange migration begins to avoid affecting retirement of the Germany environment.</span></span> <span data-ttu-id="662b4-163">Les URL des services Office 365 pour Outlook services deviennent disponibles uniquement après le début de la migration Exchange.</span><span class="sxs-lookup"><span data-stu-id="662b4-163">The Office 365 services URLs for Outlook services become available only after Exchange migration begins.</span></span>

- <span data-ttu-id="662b4-164">Les boîtes aux lettres sont migrées en tant que processus principal.</span><span class="sxs-lookup"><span data-stu-id="662b4-164">Mailboxes are migrated as a backend process.</span></span> <span data-ttu-id="662b4-165">Les utilisateurs de votre organisation peuvent se trouver dans Microsoft Cloud Deutschland ou dans la région allemande pendant la transition et font partie de la même organisation Exchange (dans la même liste d’adresses globale).</span><span class="sxs-lookup"><span data-stu-id="662b4-165">Users in your organization may be in either Microsoft Cloud Deutschland or the German region during the transition and are part of the same Exchange organization (in the same global address list).</span></span>

- <span data-ttu-id="662b4-166">Les utilisateurs d’Outlook Web App qui accèdent au service à l’aide d’une URL où leur boîte aux lettres ne réside pas, voient une invite d’authentification supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="662b4-166">Users of the Outlook Web App who access the service by using a URL where their mailbox does not reside will see an extra authentication prompt.</span></span> <span data-ttu-id="662b4-167">Par exemple, si la boîte aux lettres de l’utilisateur se trouve dans les services Office 365 et que la connexion Outlook Web App de l’utilisateur utilise le point de terminaison hérité `outlook.office.de` , l’utilisateur s’authentifie d’abord sur `login.microsoftonline.de` , puis sur `login.microsoftonline.com` .</span><span class="sxs-lookup"><span data-stu-id="662b4-167">For example, if the user's mailbox is in the Office 365 services and the user's Outlook Web App connection uses the legacy endpoint `outlook.office.de`, the user will first authenticate to `login.microsoftonline.de`, and then to `login.microsoftonline.com`.</span></span> <span data-ttu-id="662b4-168">Une fois la migration terminée, l’utilisateur peut accéder à la nouvelle URL ( `https://outlook.office365.com` ) et il voit seulement la demande de connexion attendue.</span><span class="sxs-lookup"><span data-stu-id="662b4-168">When migration is complete, the user can access the new URL (`https://outlook.office365.com`), and they'll see only the single, expected sign-in request.</span></span> 

## <a name="office-services"></a><span data-ttu-id="662b4-169">Services Office</span><span class="sxs-lookup"><span data-stu-id="662b4-169">Office Services</span></span>

<span data-ttu-id="662b4-170">Les services Office Online sont accessibles via `office.de` le, avant et Pendant la transition.</span><span class="sxs-lookup"><span data-stu-id="662b4-170">Office Online services are accessible via `office.de` before and during the transition.</span></span> <span data-ttu-id="662b4-171">Une fois que les boîtes aux lettres des utilisateurs sont transférées vers les services Office 365, les utilisateurs doivent commencer à utiliser les URL des services Office 365.</span><span class="sxs-lookup"><span data-stu-id="662b4-171">After users' mailboxes are transitioned to the Office 365 services, users should begin to use Office 365 services URLs.</span></span> <span data-ttu-id="662b4-172">À mesure que les charges de travail suivantes migrent vers les services Office 365, leur interface à partir du portail office.com commencera à fonctionner.</span><span class="sxs-lookup"><span data-stu-id="662b4-172">As subsequent workloads migrate to Office 365 services, their interface from the office.com portal will begin to work.</span></span>

## <a name="exchange-online-protection"></a><span data-ttu-id="662b4-173">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="662b4-173">Exchange Online Protection</span></span>

- <span data-ttu-id="662b4-174">Les fonctionnalités Exchange Online Protection (EOP) principales sont copiées dans la nouvelle région Germany.</span><span class="sxs-lookup"><span data-stu-id="662b4-174">Back-end Exchange Online Protection (EOP) features are copied to new Germany region.</span></span>
- <span data-ttu-id="662b4-175">Centre de sécurité et conformité Office 365 les utilisateurs doivent effectuer une transition vers l’utilisation d’URL globales, `https://protection.office.com` dans le cadre de la migration.</span><span class="sxs-lookup"><span data-stu-id="662b4-175">Office 365 Security and Compliance Center users need to transition to using global URLs, `https://protection.office.com`, as part of the migration.</span></span>

## <a name="skype-for-business-online"></a><span data-ttu-id="662b4-176">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="662b4-176">Skype for Business Online</span></span>

<span data-ttu-id="662b4-177">Les clients Skype Entreprise Online existants sont transférés vers Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="662b4-177">Existing Skype for Business Online customers will transition to Microsoft Teams.</span></span> <span data-ttu-id="662b4-178">Pour plus d’informations, reportez-vous à [https://aka.ms/SkypeToTeams-Home](https://aka.ms/SkypeToTeams-Home) .</span><span class="sxs-lookup"><span data-stu-id="662b4-178">For more information, see [https://aka.ms/SkypeToTeams-Home](https://aka.ms/SkypeToTeams-Home).</span></span>

## <a name="office-365-video"></a><span data-ttu-id="662b4-179">Office 365 Video</span><span class="sxs-lookup"><span data-stu-id="662b4-179">Office 365 Video</span></span>

<span data-ttu-id="662b4-180">La vidéo Office 365 est supprimée le 1er mars, 2021 et la vidéo Office 365 ne sera pas prise en charge après la migration de SharePoint Online vers les nouvelles régions de centre de contenu allemand.</span><span class="sxs-lookup"><span data-stu-id="662b4-180">Office 365 Video is being retired on March 1, 2021, and Office 365 Video won't be supported after migration of SharePoint Online to the new German datacenter regions is completed.</span></span> <span data-ttu-id="662b4-181">Le contenu de la vidéo Office 365 sera migré dans le cadre de la migration de SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="662b4-181">Content from Office 365 Video will be migrated as part of migrating SharePoint Online.</span></span> <span data-ttu-id="662b4-182">Toutefois, les vidéos de la vidéo Office 365 ne seront pas lues dans l’interface utilisateur vidéo Office 365 après la migration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="662b4-182">However, videos in Office 365 Video won't play back in the Office 365 Video UI after the SharePoint migration.</span></span> <span data-ttu-id="662b4-183">En savoir plus sur la chronologie de la migration sur la [transition vidéo Office 365 vers Microsoft Stream (classique) Overview](https://docs.microsoft.com/stream/migrate-from-office-365#microsoft-cloud-deutschland-timeline).</span><span class="sxs-lookup"><span data-stu-id="662b4-183">Learn more about the migration timeline on [Office 365 Video transition to Microsoft Stream (classic) overview](https://docs.microsoft.com/stream/migrate-from-office-365#microsoft-cloud-deutschland-timeline).</span></span>

## <a name="next-step"></a><span data-ttu-id="662b4-184">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="662b4-184">Next step</span></span>

[<span data-ttu-id="662b4-185">Comprendre les actions et les impacts des phases de migration</span><span class="sxs-lookup"><span data-stu-id="662b4-185">Understand migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)

## <a name="more-information"></a><span data-ttu-id="662b4-186">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="662b4-186">More information</span></span>

<span data-ttu-id="662b4-187">Mise en route :</span><span class="sxs-lookup"><span data-stu-id="662b4-187">Getting started:</span></span>

- [<span data-ttu-id="662b4-188">Migration de Microsoft Cloud Deutschland vers Office 365 services dans les nouvelles régions de centre de connaissances allemand</span><span class="sxs-lookup"><span data-stu-id="662b4-188">Migration from Microsoft Cloud Deutschland to Office 365 services in the new German datacenter regions</span></span>](ms-cloud-germany-transition.md)
- [<span data-ttu-id="662b4-189">Aide à la migration de Microsoft Cloud Deutschland : </span><span class="sxs-lookup"><span data-stu-id="662b4-189">Microsoft Cloud Deutschland Migration Assistance</span></span>](https://aka.ms/germanymigrateassist)
- [<span data-ttu-id="662b4-190">Comment opter pour une migration</span><span class="sxs-lookup"><span data-stu-id="662b4-190">How to opt-in for migration</span></span>](ms-cloud-germany-migration-opt-in.md)

<span data-ttu-id="662b4-191">Navigation par le biais de la transition :</span><span class="sxs-lookup"><span data-stu-id="662b4-191">Moving through the transition:</span></span>

- [<span data-ttu-id="662b4-192">Actions et impacts sur les phases de migration</span><span class="sxs-lookup"><span data-stu-id="662b4-192">Migration phases actions and impacts</span></span>](ms-cloud-germany-transition-phases.md)
- [<span data-ttu-id="662b4-193">Pré-travail supplémentaire</span><span class="sxs-lookup"><span data-stu-id="662b4-193">Additional pre-work</span></span>](ms-cloud-germany-transition-add-pre-work.md)
- <span data-ttu-id="662b4-194">Informations supplémentaires pour les [services](ms-cloud-germany-transition-add-general.md), les [appareils](ms-cloud-germany-transition-add-devices.md), les [expériences](ms-cloud-germany-transition-add-experience.md)et [AD FS](ms-cloud-germany-transition-add-adfs.md).</span><span class="sxs-lookup"><span data-stu-id="662b4-194">Additional information for [services](ms-cloud-germany-transition-add-general.md), [devices](ms-cloud-germany-transition-add-devices.md), [experiences](ms-cloud-germany-transition-add-experience.md), and [AD FS](ms-cloud-germany-transition-add-adfs.md).</span></span>

<span data-ttu-id="662b4-195">Applications Cloud :</span><span class="sxs-lookup"><span data-stu-id="662b4-195">Cloud apps:</span></span>

- [<span data-ttu-id="662b4-196">Informations sur le programme de migration Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="662b4-196">Dynamics 365 migration program information</span></span>](https://aka.ms/d365ceoptin)
- [<span data-ttu-id="662b4-197">Informations sur le programme de migration Power BI</span><span class="sxs-lookup"><span data-stu-id="662b4-197">Power BI migration program information</span></span>](https://aka.ms/pbioptin)
- [<span data-ttu-id="662b4-198">Prise en main de votre mise à niveau vers Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="662b4-198">Getting started with your Microsoft Teams upgrade</span></span>](https://aka.ms/SkypeToTeams-Home)