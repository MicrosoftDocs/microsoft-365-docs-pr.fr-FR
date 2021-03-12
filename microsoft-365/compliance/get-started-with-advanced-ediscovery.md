---
title: Configurer Advanced eDiscovery dans Microsoft 365
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365solution-ediscovery
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: Cet article explique comment configurer Advanced eDiscovery pour commencer à créer et gérer des cas. Il décrit également les abonnements et les licences Microsoft requis. Après quelques étapes rapides, l’outil Advanced eDiscovery est prêt à être utilisé.
ms.openlocfilehash: 29a220f36a55a04d1c1a24add03b2e013a5c60ba
ms.sourcegitcommit: 3d48e198e706f22ac903b346cadda06b2368dd1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "50727409"
---
# <a name="set-up-microsoft-365-advanced-ediscovery"></a><span data-ttu-id="7ac66-105">Configurer Microsoft 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7ac66-105">Set up Microsoft 365 Advanced eDiscovery</span></span>

<span data-ttu-id="7ac66-106">Advanced eDiscovery dans Microsoft 365 fournit un flux de travail de bout en bout pour conserver, collecter, examiner, analyser et exporter des données qui répondent aux enquêtes internes et externes de votre organisation. [](overview-ediscovery-20.md#advanced-ediscovery-workflow)</span><span class="sxs-lookup"><span data-stu-id="7ac66-106">Advanced eDiscovery in Microsoft 365 provides an [end-to-end workflow](overview-ediscovery-20.md#advanced-ediscovery-workflow) to preserve, collect, review, analyze, and export data that's responsive to your organization's internal and external investigations.</span></span> <span data-ttu-id="7ac66-107">Rien n’est nécessaire pour déployer Advanced eDiscovery, mais un administrateur informatique et un responsable eDiscovery doivent effectuer certaines tâches préalables avant que votre organisation puisse commencer à créer et utiliser des cas Advanced eDiscovery pour gérer vos enquêtes.</span><span class="sxs-lookup"><span data-stu-id="7ac66-107">Nothing is needed to deploy Advanced eDiscovery, but there are some prerequisite tasks that an IT admin and eDiscovery manager have to complete before your organization can start to create and use Advanced eDiscovery cases to manage your investigations.</span></span>

<span data-ttu-id="7ac66-108">Cet article décrit les étapes nécessaires pour configurer Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-108">This article discusses the steps necessary to set up Advanced eDiscovery.</span></span> <span data-ttu-id="7ac66-109">Cela inclut la garantie de la licence appropriée requise pour accéder à Advanced eDiscovery et ajouter des dépositaires aux cas, et l’attribution d’autorisations à votre équipe juridique et d’examen afin qu’elle puisse accéder aux cas et les gérer.</span><span class="sxs-lookup"><span data-stu-id="7ac66-109">This includes ensuring the proper licensing required to access Advanced eDiscovery and add custodians to cases, and assigning permissions to your legal and investigation team so they can access and manage cases.</span></span>

## <a name="step-1-verify-and-assign-appropriate-licenses"></a><span data-ttu-id="7ac66-110">Étape 1 : Vérifier et attribuer les licences appropriées</span><span class="sxs-lookup"><span data-stu-id="7ac66-110">Step 1: Verify and assign appropriate licenses</span></span>

<span data-ttu-id="7ac66-111">La gestion des licences pour Advanced eDiscovery nécessite l’abonnement d’organisation et la licence par utilisateur appropriés.</span><span class="sxs-lookup"><span data-stu-id="7ac66-111">Licensing for Advanced eDiscovery requires the appropriate organization subscription and per-user licensing.</span></span>

- <span data-ttu-id="7ac66-112">**Abonnement à l’organisation :** Pour accéder à Advanced eDiscovery dans le Centre de conformité Microsoft 365 ou le Centre de sécurité & conformité, votre organisation doit avoir l’une des fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ac66-112">**Organization subscription:** To access Advanced eDiscovery in the Microsoft 365 compliance center or the Security & Compliance Center, your organization must have one of the following:</span></span>

  - <span data-ttu-id="7ac66-113">Abonnement Microsoft 365 E5 ou Office 365 E5</span><span class="sxs-lookup"><span data-stu-id="7ac66-113">Microsoft 365 E5 or Office 365 E5 subscription</span></span>
  
  - <span data-ttu-id="7ac66-114">Abonnement Microsoft 365 E3 avec le module complémentaire E5 conformité</span><span class="sxs-lookup"><span data-stu-id="7ac66-114">Microsoft 365 E3 subscription with E5 Compliance add-on</span></span>

  - <span data-ttu-id="7ac66-115">Abonnement Microsoft 365 E3 avec E5 eDiscovery et module d’audit</span><span class="sxs-lookup"><span data-stu-id="7ac66-115">Microsoft 365 E3 subscription with E5 eDiscovery and Audit add-on</span></span>

  <span data-ttu-id="7ac66-116">Si vous n’avez pas de plan Microsoft 365 E5 et que vous souhaitez essayer Advanced eDiscovery, vous pouvez ajouter [Microsoft 365](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) à votre abonnement existant ou vous inscrire à une version d’essai de Microsoft 365 E5. [](https://www.microsoft.com/microsoft-365/enterprise)</span><span class="sxs-lookup"><span data-stu-id="7ac66-116">If you don't have an existing Microsoft 365 E5 plan and want to try Advanced eDiscovery, you can [add Microsoft 365](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) to your existing subscription or [sign up for a trial](https://www.microsoft.com/microsoft-365/enterprise) of Microsoft 365 E5.</span></span>

- <span data-ttu-id="7ac66-117">**Licences par utilisateur :** Pour ajouter un utilisateur en tant que dépositaire dans un cas de découverte électronique anticipée, l’une des licences suivantes doit lui être attribuée, en fonction de l’abonnement de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="7ac66-117">**Per-user licensing:** To add a user as a custodian in an Advance eDiscovery case, that user must be assigned one of the following licenses, depending on your organization subscription:</span></span>

  - <span data-ttu-id="7ac66-118">Microsoft 365 : une licence Microsoft 365 E5, une licence de module de conformité E5 ou une licence de modules de découverte électronique et d’audit E5 doivent être attribuées aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7ac66-118">Microsoft 365: Users must be assigned a Microsoft 365 E5 license, an E5 Compliance add-on license, or an E5 eDiscovery and Audit add-on license.</span></span>

  - <span data-ttu-id="7ac66-119">Office 365 : une licence Office 365 E5 doit être attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7ac66-119">Office 365: Users must be assigned an Office 365 E5 license.</span></span>

   <span data-ttu-id="7ac66-120">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users)</span><span class="sxs-lookup"><span data-stu-id="7ac66-120">For information about how to assign licenses, see [Assign licenses to users](https://docs.microsoft.com/microsoft-365/admin/manage/assign-licenses-to-users).</span></span>

> [!NOTE]
> <span data-ttu-id="7ac66-121">Les utilisateurs ont uniquement besoin d’une licence E5 (ou de la licence de module supplémentaire appropriée) pour être ajoutés en tant que dépositaires à un cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-121">Users only need an E5 license (or the appropriate add-on license) to be added as custodians to an Advanced eDiscovery case.</span></span> <span data-ttu-id="7ac66-122">Les administrateurs informatiques, les gestionnaires eDiscovery, les avocats, les techniciens juridiques ou les enquêteurs qui utilisent Advanced eDiscovery pour gérer les cas et examiner les données de cas n’ont pas besoin d’une licence E5 ou de modules add-on.</span><span class="sxs-lookup"><span data-stu-id="7ac66-122">IT admins, eDiscovery managers, lawyers, paralegals, or investigators who use Advanced eDiscovery to manage cases and review case data don't need an E5 or add-on license.</span></span>

## <a name="step-2-assign-ediscovery-permissions"></a><span data-ttu-id="7ac66-123">Étape 2 : Attribuer des autorisations eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7ac66-123">Step 2: Assign eDiscovery permissions</span></span>

<span data-ttu-id="7ac66-124">Pour accéder à Advanced eDiscovery ou être ajouté en tant que membre d’un cas Advanced eDiscovery, un utilisateur doit avoir les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="7ac66-124">To access Advanced eDiscovery or added as a member of an Advanced eDiscovery case, a user must be assigned the appropriate permissions.</span></span> <span data-ttu-id="7ac66-125">Plus précisément, un utilisateur doit être ajouté en tant que membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="7ac66-125">Specifically, a user must be added as a member of the eDiscovery Manager role group in the Security & Compliance Center.</span></span> <span data-ttu-id="7ac66-126">Les membres de ce groupe de rôles peuvent créer et gérer des cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-126">Members of this role group can create and manage Advanced eDiscovery cases.</span></span> <span data-ttu-id="7ac66-127">Ils peuvent ajouter et supprimer des membres, placer des dépositaires et des emplacements de contenu en conservation, gérer les notifications de conservation légale, créer et modifier des recherches associées à un cas, ajouter des résultats de recherche à un groupe de révision, analyser des données dans un jeu à réviser et exporter et télécharger à partir d’un cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-127">They can add and remove members, place custodians and content locations on hold, manage legal hold notifications, create and edit searches associated in a case, add search results to a review set, analyze data in a review set, and export and download from an Advanced eDiscovery case.</span></span>

<span data-ttu-id="7ac66-128">Pour ajouter des utilisateurs au groupe de rôles Gestionnaire eDiscovery, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7ac66-128">Complete the following steps to add users to the eDiscovery Manager role group:</span></span>

1. <span data-ttu-id="7ac66-129">Go to [https://protection.office.com/permissions](https://protection.office.com/permissions) and sign in using the credentials for an admin account in your Microsoft 365 organization.</span><span class="sxs-lookup"><span data-stu-id="7ac66-129">Go to [https://protection.office.com/permissions](https://protection.office.com/permissions) and sign in using the credentials for an admin account in your Microsoft 365 organization.</span></span>

2. <span data-ttu-id="7ac66-130">Dans la page **Autorisations,** sélectionnez le groupe de rôles **Gestionnaire eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="7ac66-130">On the **Permissions** page, select the **eDiscovery Manager** role group.</span></span>

3. <span data-ttu-id="7ac66-131">Dans la page volante du Gestionnaire  eDiscovery, cliquez sur Modifier à côté de la section Gestionnaire **eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="7ac66-131">On the eDiscovery Manager flyout page, click **Edit** next to the **eDiscovery Manager** section.</span></span>

4. <span data-ttu-id="7ac66-132">Dans la page Choisir le gestionnaire **eDiscovery** dans l’Assistant Modifier le groupe de rôles, cliquez sur Choisir le Gestionnaire **eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="7ac66-132">On the **Choose eDiscovery Manager** page in the edit role group wizard, click **Choose eDiscovery Manager**.</span></span>

5. <span data-ttu-id="7ac66-133">Cliquez **sur** Ajouter, puis cochez la case pour tous les utilisateurs que vous souhaitez ajouter au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="7ac66-133">Click **Add** then select the checkbox for all users you want to add to the role group.</span></span>

6. <span data-ttu-id="7ac66-134">Cliquez **sur** Ajouter pour ajouter les utilisateurs sélectionnés, puis cliquez sur **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="7ac66-134">Click **Add** to add the selected users, and then click **Done**.</span></span>

7. <span data-ttu-id="7ac66-135">Cliquez **sur Enregistrer** pour ajouter les utilisateurs au groupe de rôles, puis cliquez sur **Fermer** pour terminer l’étape.</span><span class="sxs-lookup"><span data-stu-id="7ac66-135">Click **Save** to add the users to the role group, and then click **Close** to complete the step.</span></span>

### <a name="more-information-about-the-ediscovery-manager-role-group"></a><span data-ttu-id="7ac66-136">Plus d’informations sur le groupe de rôles Gestionnaire eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7ac66-136">More information about the eDiscovery Manager role group</span></span>

<span data-ttu-id="7ac66-137">Il existe deux sous-groupes dans le groupe de rôles Gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-137">There are two subgroups in the eDiscovery Manager role group.</span></span> <span data-ttu-id="7ac66-138">Ces sous-groupes ont différents rôles.</span><span class="sxs-lookup"><span data-stu-id="7ac66-138">The difference between these subgroups is based on scope.</span></span>

- <span data-ttu-id="7ac66-139">**Gestionnaire eDiscovery :** Peut afficher et gérer les cas Advanced eDiscovery qu’ils créent ou dont ils sont membres.</span><span class="sxs-lookup"><span data-stu-id="7ac66-139">**eDiscovery Manager:** Can view and manage the Advanced eDiscovery cases they create or are a member of.</span></span> <span data-ttu-id="7ac66-140">Si un autre gestionnaire eDiscovery crée un cas mais n’ajoute pas un deuxième gestionnaire eDiscovery en tant que membre de ce cas, le deuxième gestionnaire eDiscovery ne sera pas en mesure d’afficher ou d’ouvrir le cas sur la page Advanced eDiscovery dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="7ac66-140">If another eDiscovery Manager creates a case but doesn't add a second eDiscovery Manager as a member of that case, the second eDiscovery Manager won't be able to view or open the case on the Advanced eDiscovery page in the compliance center.</span></span> <span data-ttu-id="7ac66-141">En règle générale, la plupart des membres de votre organisation peuvent être ajoutés au sous-groupe gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-141">In general, most people in your organization can be added to the eDiscovery Manager subgroup.</span></span>

- <span data-ttu-id="7ac66-142">**Administrateur eDiscovery :** Peut effectuer toutes les tâches de gestion des cas qu’un gestionnaire eDiscovery peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="7ac66-142">**eDiscovery Administrator:** Can perform all case management tasks that an eDiscovery Manager can do.</span></span> <span data-ttu-id="7ac66-143">De plus, un administrateur de découverte électronique peut :</span><span class="sxs-lookup"><span data-stu-id="7ac66-143">Additionally, an eDiscovery Administrator can:</span></span>

  - <span data-ttu-id="7ac66-144">Afficher tous les cas répertoriés sur la page Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-144">View all cases that are listed on the Advanced eDiscovery page.</span></span>
  
  - <span data-ttu-id="7ac66-145">Gérer tous les cas au sein l’organisation après s’être ajouté en tant que membre du cas.</span><span class="sxs-lookup"><span data-stu-id="7ac66-145">Manage any case in the organization after they add themselves as a member of the case.</span></span>

  - <span data-ttu-id="7ac66-146">Accéder et exporter des données de cas pour tout cas au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7ac66-146">Access and export case data for any case in the organization.</span></span>

  <span data-ttu-id="7ac66-147">En raison de l’étendue de l’accès, une organisation ne doit avoir que quelques administrateurs membres du sous-groupe administrateurs eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-147">Because of the broad scope of access, an organization should have only a few admins who are members of the eDiscovery Administrators subgroup.</span></span>

<span data-ttu-id="7ac66-148">Pour plus d’informations sur les autorisations eDiscovery et une description de chaque rôle affecté au groupe de rôles Gestionnaire eDiscovery, voir Attribuer des [autorisations eDiscovery.](assign-ediscovery-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="7ac66-148">For more information about eDiscovery permissions and a description of each role that's assigned to the eDiscovery Manager role group, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

## <a name="step-3-configure-global-settings-for-advanced-ediscovery"></a><span data-ttu-id="7ac66-149">Étape 3 : Configurer les paramètres globaux pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7ac66-149">Step 3: Configure global settings for Advanced eDiscovery</span></span>

<span data-ttu-id="7ac66-150">La dernière étape à effectuer avant que les membres de votre organisation commencent à créer et à utiliser des cas consiste à configurer des paramètres globaux qui s’appliquent à tous les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7ac66-150">The last step to complete before people in your organization start to create and use cases is to configure global settings that apply to all cases in your organization.</span></span> <span data-ttu-id="7ac66-151">Pour l’instant, le seul paramètre global est la détection des privilèges *client-avocat* (d’autres paramètres globaux seront disponibles à l’avenir).</span><span class="sxs-lookup"><span data-stu-id="7ac66-151">At this time, the only global setting is *attorney-client privilege detection* (more global settings will be available in the future).</span></span> <span data-ttu-id="7ac66-152">Ce paramètre permet au modèle de privilège client-avocat de s’exécuter lorsque vous analysez des données dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="7ac66-152">This setting enables the attorney-client privilege model to run when you analyze data in a review set.</span></span> <span data-ttu-id="7ac66-153">Le modèle utilise l’apprentissage automatique pour déterminer la probabilité qu’un document contienne du contenu de nature juridique.</span><span class="sxs-lookup"><span data-stu-id="7ac66-153">The model uses machine learning to determine the likelihood that a document contains content that is legal in nature.</span></span> <span data-ttu-id="7ac66-154">Il compare également les participants des documents à une liste d’avocats (que vous soumettez lors de la configuration du modèle) pour déterminer si un document a au moins un participant qui est avocat.</span><span class="sxs-lookup"><span data-stu-id="7ac66-154">It also compares the participants of documents with an attorney list (that you submit when setting up the model) to determine if a document has at least one participant who is an attorney.</span></span>

<span data-ttu-id="7ac66-155">Pour plus d’informations sur la configuration et l’utilisation du modèle de détection des privilèges client-avocat, voir Configurer la détection des privilèges [client-avocat dans Advanced eDiscovery](attorney-privilege-detection.md).</span><span class="sxs-lookup"><span data-stu-id="7ac66-155">For more information about setting up and using the attorney-client privilege detection model, see [Set up attorney-client privilege detection in Advanced eDiscovery](attorney-privilege-detection.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7ac66-156">Il s’agit d’une étape facultative que vous pouvez effectuer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="7ac66-156">This is an optional step that you can perform anytime.</span></span> <span data-ttu-id="7ac66-157">Le fait de ne pas implémenter le modèle de détection des privilèges client-avocat ne vous empêche pas de créer et d’utiliser des cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7ac66-157">Not implementing the attorney-client privilege detection model doesn't prevent you from creating and using Advanced eDiscovery cases.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7ac66-158">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7ac66-158">Next steps</span></span>

<span data-ttu-id="7ac66-159">Après avoir installé Advanced eDiscovery, vous êtes prêt à [créer un cas.](create-and-manage-advanced-ediscoveryv2-case.md)</span><span class="sxs-lookup"><span data-stu-id="7ac66-159">After you set up Advanced eDiscovery, you're ready to [create a case](create-and-manage-advanced-ediscoveryv2-case.md).</span></span>
