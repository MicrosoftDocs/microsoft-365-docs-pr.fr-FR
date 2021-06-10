---
title: Configurer des Advanced eDiscovery dans Microsoft 365
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
- m365solution-aed
- m365initiative-compliance
- m365solution-scenario
search.appverid:
- MOE150
- MET150
description: Cet article explique comment configurer des Advanced eDiscovery vous permet de commencer à créer et gérer des cas. Il décrit également les abonnements et les licences Microsoft requis. Après quelques étapes rapides, l’outil Advanced eDiscovery est prêt à être utilisé.
ms.openlocfilehash: 6c6aed482da8f203154d94313ec04519d6a330ea
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919743"
---
# <a name="set-up-microsoft-365-advanced-ediscovery"></a><span data-ttu-id="f242e-105">Configurer Microsoft 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f242e-105">Set up Microsoft 365 Advanced eDiscovery</span></span>

<span data-ttu-id="f242e-106">Advanced eDiscovery dans Microsoft 365 fournit un flux de travail de bout en bout pour conserver, collecter, examiner, analyser et exporter des données qui répondent aux enquêtes internes et externes de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f242e-106">Advanced eDiscovery in Microsoft 365 provides an end-to-end workflow to preserve, collect, review, analyze, and export data that's responsive to your organization's internal and external investigations.</span></span> <span data-ttu-id="f242e-107">Rien n’est nécessaire pour déployer Advanced eDiscovery, mais un administrateur informatique et un responsable eDiscovery doivent effectuer certaines tâches préalables avant que votre organisation puisse commencer à créer et utiliser des cas Advanced eDiscovery pour gérer vos enquêtes.</span><span class="sxs-lookup"><span data-stu-id="f242e-107">Nothing is needed to deploy Advanced eDiscovery, but there are some prerequisite tasks that an IT admin and eDiscovery manager have to complete before your organization can start to create and use Advanced eDiscovery cases to manage your investigations.</span></span>

<span data-ttu-id="f242e-108">Cet article décrit les étapes suivantes nécessaires à la Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-108">This article discusses the following steps necessary to set up Advanced eDiscovery.</span></span>

![Étapes de la mise en Advanced eDiscovery](../media/set-up-advanced-ediscovery.png)

<span data-ttu-id="f242e-110">Cela inclut la garantie de la licence appropriée requise pour accéder aux Advanced eDiscovery et ajouter des dépositaires aux cas, et l’attribution d’autorisations à votre équipe juridique et d’enquête afin qu’elle puisse accéder aux cas et les gérer.</span><span class="sxs-lookup"><span data-stu-id="f242e-110">This includes ensuring the proper licensing required to access Advanced eDiscovery and add custodians to cases, and assigning permissions to your legal and investigation team so they can access and manage cases.</span></span>

## <a name="step-1-verify-and-assign-appropriate-licenses"></a><span data-ttu-id="f242e-111">Étape 1 : Vérifier et attribuer les licences appropriées</span><span class="sxs-lookup"><span data-stu-id="f242e-111">Step 1: Verify and assign appropriate licenses</span></span>

<span data-ttu-id="f242e-112">La gestion des Advanced eDiscovery nécessite l’abonnement d’organisation approprié et la licence par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f242e-112">Licensing for Advanced eDiscovery requires the appropriate organization subscription and per-user licensing.</span></span> <span data-ttu-id="f242e-113">Pour obtenir la liste des conditions de licence requises pour Advanced eDiscovery, voir [Abonnements et licences.](overview-ediscovery-20.md#subscriptions-and-licensing)</span><span class="sxs-lookup"><span data-stu-id="f242e-113">For a list of licensing requirements for Advanced eDiscovery, see [Subscriptions and licensing](overview-ediscovery-20.md#subscriptions-and-licensing).</span></span>

## <a name="step-2-assign-ediscovery-permissions"></a><span data-ttu-id="f242e-114">Étape 2 : Attribuer des autorisations eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f242e-114">Step 2: Assign eDiscovery permissions</span></span>

<span data-ttu-id="f242e-115">Pour accéder Advanced eDiscovery ou ajouté en tant que membre d’un Advanced eDiscovery, un utilisateur doit se voir attribuer les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="f242e-115">To access Advanced eDiscovery or added as a member of an Advanced eDiscovery case, a user must be assigned the appropriate permissions.</span></span> <span data-ttu-id="f242e-116">Plus précisément, un utilisateur doit être ajouté en tant que membre du groupe de rôles Gestionnaire eDiscovery dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="f242e-116">Specifically, a user must be added as a member of the eDiscovery Manager role group in the Security & Compliance Center.</span></span> <span data-ttu-id="f242e-117">Les membres de ce groupe de rôles peuvent créer et gérer Advanced eDiscovery cas.</span><span class="sxs-lookup"><span data-stu-id="f242e-117">Members of this role group can create and manage Advanced eDiscovery cases.</span></span> <span data-ttu-id="f242e-118">Ils peuvent ajouter et supprimer des membres, placer des dépositaires et des emplacements de contenu en conservation, gérer les notifications de conservation légale, créer et modifier des recherches associées à un cas, ajouter des résultats de recherche à un groupe de révision, analyser des données dans un groupe de révision et exporter et télécharger à partir d’un cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-118">They can add and remove members, place custodians and content locations on hold, manage legal hold notifications, create and edit searches associated in a case, add search results to a review set, analyze data in a review set, and export and download from an Advanced eDiscovery case.</span></span>

<span data-ttu-id="f242e-119">Pour ajouter des utilisateurs au groupe de rôles Gestionnaire eDiscovery, complétez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f242e-119">Complete the following steps to add users to the eDiscovery Manager role group:</span></span>

1. <span data-ttu-id="f242e-120">Go to <https://protection.office.com/permissions> and sign in using the credentials for an admin account in your Microsoft 365 organization.</span><span class="sxs-lookup"><span data-stu-id="f242e-120">Go to <https://protection.office.com/permissions> and sign in using the credentials for an admin account in your Microsoft 365 organization.</span></span>

2. <span data-ttu-id="f242e-121">Dans la page **Autorisations,** sélectionnez le groupe de rôles **Gestionnaire eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="f242e-121">On the **Permissions** page, select the **eDiscovery Manager** role group.</span></span>

3. <span data-ttu-id="f242e-122">Dans la page volante du Gestionnaire  eDiscovery, cliquez sur Modifier à côté de la section Gestionnaire **eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="f242e-122">On the eDiscovery Manager flyout page, click **Edit** next to the **eDiscovery Manager** section.</span></span>

4. <span data-ttu-id="f242e-123">Dans la page Choisir le gestionnaire **eDiscovery** dans l’Assistant Modifier le groupe de rôles, cliquez sur Choisir le Gestionnaire **eDiscovery.**</span><span class="sxs-lookup"><span data-stu-id="f242e-123">On the **Choose eDiscovery Manager** page in the edit role group wizard, click **Choose eDiscovery Manager**.</span></span>

5. <span data-ttu-id="f242e-124">Cliquez **sur** Ajouter, puis cochez la case pour tous les utilisateurs que vous souhaitez ajouter au groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="f242e-124">Click **Add** then select the checkbox for all users you want to add to the role group.</span></span>

6. <span data-ttu-id="f242e-125">Cliquez **sur** Ajouter pour ajouter les utilisateurs sélectionnés, puis cliquez sur **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="f242e-125">Click **Add** to add the selected users, and then click **Done**.</span></span>

7. <span data-ttu-id="f242e-126">Cliquez **sur Enregistrer** pour ajouter les utilisateurs au groupe de rôles, puis cliquez sur **Fermer** pour terminer l’étape.</span><span class="sxs-lookup"><span data-stu-id="f242e-126">Click **Save** to add the users to the role group, and then click **Close** to complete the step.</span></span>

### <a name="more-information-about-the-ediscovery-manager-role-group"></a><span data-ttu-id="f242e-127">Plus d’informations sur le groupe de rôles Gestionnaire eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f242e-127">More information about the eDiscovery Manager role group</span></span>

<span data-ttu-id="f242e-128">Il existe deux sous-groupes dans le groupe de rôles Gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-128">There are two subgroups in the eDiscovery Manager role group.</span></span> <span data-ttu-id="f242e-129">Ces sous-groupes ont différents rôles.</span><span class="sxs-lookup"><span data-stu-id="f242e-129">The difference between these subgroups is based on scope.</span></span>

- <span data-ttu-id="f242e-130">**Gestionnaire eDiscovery**: peut afficher et gérer les Advanced eDiscovery cas qu’ils créent ou dont ils sont membres.</span><span class="sxs-lookup"><span data-stu-id="f242e-130">**eDiscovery Manager**: Can view and manage the Advanced eDiscovery cases they create or are a member of.</span></span> <span data-ttu-id="f242e-131">Si un autre gestionnaire eDiscovery crée un cas mais n’ajoute pas un deuxième gestionnaire eDiscovery en tant que membre de ce cas, le deuxième gestionnaire eDiscovery ne sera pas en mesure d’afficher ou d’ouvrir le cas sur la page Advanced eDiscovery dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="f242e-131">If another eDiscovery Manager creates a case but doesn't add a second eDiscovery Manager as a member of that case, the second eDiscovery Manager won't be able to view or open the case on the Advanced eDiscovery page in the compliance center.</span></span> <span data-ttu-id="f242e-132">En règle générale, la plupart des membres de votre organisation peuvent être ajoutés au sous-groupe gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-132">In general, most people in your organization can be added to the eDiscovery Manager subgroup.</span></span>

- <span data-ttu-id="f242e-133">**Administrateur eDiscovery**: peut effectuer toutes les tâches de gestion des cas qu’un gestionnaire eDiscovery peut effectuer.</span><span class="sxs-lookup"><span data-stu-id="f242e-133">**eDiscovery Administrator**: Can perform all case management tasks that an eDiscovery Manager can do.</span></span> <span data-ttu-id="f242e-134">De plus, un administrateur de découverte électronique peut :</span><span class="sxs-lookup"><span data-stu-id="f242e-134">Additionally, an eDiscovery Administrator can:</span></span>

  - <span data-ttu-id="f242e-135">Afficher tous les cas répertoriés sur la page Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-135">View all cases that are listed on the Advanced eDiscovery page.</span></span>
  
  - <span data-ttu-id="f242e-136">Gérer tous les cas au sein l’organisation après s’être ajouté en tant que membre du cas.</span><span class="sxs-lookup"><span data-stu-id="f242e-136">Manage any case in the organization after they add themselves as a member of the case.</span></span>

  - <span data-ttu-id="f242e-137">Accéder et exporter des données de cas pour tout cas au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="f242e-137">Access and export case data for any case in the organization.</span></span>

  <span data-ttu-id="f242e-138">En raison de l’étendue de l’accès, une organisation ne doit avoir que quelques administrateurs membres du sous-groupe administrateurs eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f242e-138">Because of the broad scope of access, an organization should have only a few admins who are members of the eDiscovery Administrators subgroup.</span></span>

<span data-ttu-id="f242e-139">Pour plus d’informations sur les autorisations eDiscovery et une description de chaque rôle affecté au groupe de rôles Gestionnaire eDiscovery, voir Attribuer des [autorisations eDiscovery.](assign-ediscovery-permissions.md)</span><span class="sxs-lookup"><span data-stu-id="f242e-139">For more information about eDiscovery permissions and a description of each role that's assigned to the eDiscovery Manager role group, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>

## <a name="step-3-configure-global-settings-for-advanced-ediscovery"></a><span data-ttu-id="f242e-140">Étape 3 : Configurer les paramètres globaux pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f242e-140">Step 3: Configure global settings for Advanced eDiscovery</span></span>

<span data-ttu-id="f242e-141">La dernière étape à effectuer avant que les membres de votre organisation commencent à créer et à utiliser des cas consiste à configurer des paramètres globaux qui s’appliquent à tous les cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f242e-141">The last step to complete before people in your organization start to create and use cases is to configure global settings that apply to all cases in your organization.</span></span> <span data-ttu-id="f242e-142">Pour l’instant, le seul paramètre global est la détection des privilèges *client-avocat* (d’autres paramètres globaux seront disponibles à l’avenir).</span><span class="sxs-lookup"><span data-stu-id="f242e-142">At this time, the only global setting is *attorney-client privilege detection* (more global settings will be available in the future).</span></span> <span data-ttu-id="f242e-143">Ce paramètre permet au modèle de privilège client-avocat de s’exécuter lorsque vous analysez des données dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f242e-143">This setting enables the attorney-client privilege model to run when you analyze data in a review set.</span></span> <span data-ttu-id="f242e-144">Le modèle utilise l’apprentissage automatique pour déterminer la probabilité qu’un document contienne du contenu de nature juridique.</span><span class="sxs-lookup"><span data-stu-id="f242e-144">The model uses machine learning to determine the likelihood that a document contains content that is legal in nature.</span></span> <span data-ttu-id="f242e-145">Il compare également les participants des documents à une liste d’avocats (que vous soumettez lors de la configuration du modèle) pour déterminer si un document a au moins un participant qui est avocat.</span><span class="sxs-lookup"><span data-stu-id="f242e-145">It also compares the participants of documents with an attorney list (that you submit when setting up the model) to determine if a document has at least one participant who is an attorney.</span></span>

<span data-ttu-id="f242e-146">Pour plus d’informations sur la configuration et l’utilisation du modèle de détection des privilèges [client-avocat,](attorney-privilege-detection.md)voir Configurer la détection des privilèges client-avocat dans Advanced eDiscovery .</span><span class="sxs-lookup"><span data-stu-id="f242e-146">For more information about setting up and using the attorney-client privilege detection model, see [Set up attorney-client privilege detection in Advanced eDiscovery](attorney-privilege-detection.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f242e-147">Il s’agit d’une étape facultative que vous pouvez effectuer à tout moment.</span><span class="sxs-lookup"><span data-stu-id="f242e-147">This is an optional step that you can perform anytime.</span></span> <span data-ttu-id="f242e-148">Le fait de ne pas implémenter le modèle de détection des privilèges client-avocat ne vous empêche pas de créer et d’utiliser Advanced eDiscovery cas.</span><span class="sxs-lookup"><span data-stu-id="f242e-148">Not implementing the attorney-client privilege detection model doesn't prevent you from creating and using Advanced eDiscovery cases.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f242e-149">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="f242e-149">Next steps</span></span>

<span data-ttu-id="f242e-150">Une fois que vous avez Advanced eDiscovery, vous êtes prêt à [créer un cas.](create-and-manage-advanced-ediscoveryv2-case.md)</span><span class="sxs-lookup"><span data-stu-id="f242e-150">After you set up Advanced eDiscovery, you're ready to [create a case](create-and-manage-advanced-ediscoveryv2-case.md).</span></span>