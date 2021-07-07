---
title: Intégrer Microsoft Teams classes à Blackboard Learn Ultra
ms.author: v-cichur
author: cichur
manager: serdars
ms.reviewer: amitman
audience: admin
ms.topic: article
ms.service: o365-administration
f1.keywords:
- CSH
ms.collection: M365-modern-desktop
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Intégrer Microsoft Teams classes à Blackboard Learn Ultra
ms.openlocfilehash: da98fae3fa5d6be2513147be58747512bea99e16
ms.sourcegitcommit: 8b0718f5607ab509092cb80bda854010d885c54f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53314490"
---
# <a name="use-microsoft-teams-classes-with-blackboard-learn-ultra"></a><span data-ttu-id="cf33e-103">Utiliser Microsoft Teams classes avec Blackboard Learn Ultra</span><span class="sxs-lookup"><span data-stu-id="cf33e-103">Use Microsoft Teams classes with Blackboard Learn Ultra</span></span>

<span data-ttu-id="cf33e-104">Le travail d’équipe est au cœur de chaque organisation moderne.</span><span class="sxs-lookup"><span data-stu-id="cf33e-104">Teamwork is at the core of every modern organization.</span></span> <span data-ttu-id="cf33e-105">En favoriseant la collaboration, il s’agit d’une caractéristique de définition de chaque établissement réussi.</span><span class="sxs-lookup"><span data-stu-id="cf33e-105">By fostering collaboration, it’s a defining characteristic of every successful institution.</span></span> <span data-ttu-id="cf33e-106">Vous pouvez améliorer toutes les fonctionnalités de Blackboard Learn Ultra en les couplant avec Microsoft Teams classes.</span><span class="sxs-lookup"><span data-stu-id="cf33e-106">You can enhance all the capabilities and features of Blackboard Learn Ultra by pairing them up with Microsoft Teams classes.</span></span>

<span data-ttu-id="cf33e-107">Vos classes peuvent inclure des conversations en temps réel, des réunions vidéo ou des interactions asynchrones.</span><span class="sxs-lookup"><span data-stu-id="cf33e-107">Your classes might include real-time conversations, video meetings, or asynchronous interactions.</span></span> <span data-ttu-id="cf33e-108">Vous pouvez ajouter des expériences de partage de fichiers et de cocréation pour vos étudiants, le tout au même endroit.</span><span class="sxs-lookup"><span data-stu-id="cf33e-108">You can add file sharing and cocreation experiences for your students, all in one place.</span></span> <span data-ttu-id="cf33e-109">Microsoft Teams classes avec Learn Ultra redéfinissent la dynamique de l’enseignement et ce que signifie un apprentissage efficace.</span><span class="sxs-lookup"><span data-stu-id="cf33e-109">Microsoft Teams classes with Learn Ultra redefine the dynamics of teaching and what effective learning means.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf33e-110">Assurez-vous que vous avez correctement installé le champ Courrier de l’établissement dans votre système d’information sur les étudiants (SIS) `help.blackboard.com/Learn/Administrator/SaaS/Integrations/Student\_Information\_System/SIS\_Planning`</span><span class="sxs-lookup"><span data-stu-id="cf33e-110">Ensure that you have successfully set up the Institution Email field in your Student Information System (SIS) `help.blackboard.com/Learn/Administrator/SaaS/Integrations/Student\_Information\_System/SIS\_Planning`</span></span>
>
><span data-ttu-id="cf33e-111">L’intégration Microsoft Teams classes s’appuie sur le champ de messagerie de l’établissement dans votre SIS pour maquer le nom d’utilisateur principal (UPN) du Microsoft Azure Active Directory (AAD) correct.</span><span class="sxs-lookup"><span data-stu-id="cf33e-111">The Microsoft Teams classes integration relies on the institution email field in your SIS to map to the correct Microsoft Azure Active Directory’s (AAD) User Principal Name (UPN).</span></span> <span data-ttu-id="cf33e-112">Si aucun courrier électronique de l’établissement n’a été mis en service, il s’adresse par défaut au courrier électronique existant.</span><span class="sxs-lookup"><span data-stu-id="cf33e-112">If no institution email has been provisioned, this will default to the existing email.</span></span> <span data-ttu-id="cf33e-113">Il est recommandé de définir ce champ pour que chaque utilisateur s’assure que ses données sont synchronisées correctement et qu’il n’existe aucun conflit de données de courrier entre Microsoft AAD et Blackboard Learn Ultra.</span><span class="sxs-lookup"><span data-stu-id="cf33e-113">It’s recommended that this field be set for every user to ensure their data is synchronized correctly and that there is no conflict of email data between Microsoft AAD and Blackboard Learn Ultra.</span></span>
>
> <span data-ttu-id="cf33e-114">Si vous n’avez pas correctement définie ce champ dans votre mappage SIS, l’intégration continue de fonctionner, mais les utilisateurs peuvent ne pas apparaître dans les classes Teams créées et des erreurs peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="cf33e-114">If you haven’t set this field appropriately in your SIS mapping, the integration will continue to work, but users might not appear in the Teams classes created, and errors could occur.</span></span>

## <a name="supporting-institutional-data-mapping--institution-email-sis-field"></a><span data-ttu-id="cf33e-115">Prise en charge du mappage de données institutionnalisé : champ SIS de messagerie de l’établissement</span><span class="sxs-lookup"><span data-stu-id="cf33e-115">Supporting Institutional Data Mapping – Institution Email SIS Field</span></span>

<span data-ttu-id="cf33e-116">Dans le cadre de l’évolution avec les intégrations  de fournisseurs cloud, Blackboard Learn Ultra a créé un nouveau champ Courrier électronique de l’établissement, à la fois dans l’intégration de Student Information System Framework et dans les API REST publiques, ce qui permet aux établissements de gérer efficacement le processus de synchronisation des données entre Blackboard Learn Ultra et Microsoft AAD.</span><span class="sxs-lookup"><span data-stu-id="cf33e-116">As part of the evolution with Cloud provider integrations, Blackboard Learn Ultra has created a new **Institution Email** field, in both the Student Information System Framework integration and public REST APIs, allowing institutions to manage the data synchronization process effectively between Blackboard Learn Ultra and Microsoft AAD.</span></span>

### <a name="what-does-the-institution-email-mean-and-what-does-it-support"></a><span data-ttu-id="cf33e-117">Que signifie le courrier électronique de l’établissement et qu’est-ce qu’il prend en charge ?</span><span class="sxs-lookup"><span data-stu-id="cf33e-117">What does the Institution Email mean and what does it support?</span></span>

<span data-ttu-id="cf33e-118">Le **champ Courrier électronique** de l’établissement permet des mappages de champs personnalisés entre les sources de données d’un client pris en charge en externe et Blackboard Learn Ultra.</span><span class="sxs-lookup"><span data-stu-id="cf33e-118">The **Institution Email** field allows customized field mappings between a client’s externally supported data sources and Blackboard Learn Ultra.</span></span> <span data-ttu-id="cf33e-119">Si les sources de données sont des fournisseurs cloud, tels que Microsoft, le nom d’utilisateur principal (UPN) est un identificateur unique principal pour chaque utilisateur constitué d’un préfixe UPN (nom de compte de l’utilisateur) et d’un suffixe UPN (un nom de domaine DNS) associés à un symbole @ .</span><span class="sxs-lookup"><span data-stu-id="cf33e-119">If data sources are cloud providers, such as Microsoft, the User Principle Name (UPN) is a primary unique identifier for each user consisting of a UPN prefix (the user’s account name) and a UPN suffix (a DNS domain name) joined together with an @ symbol.</span></span> <span data-ttu-id="cf33e-120">Cela crée une adresse e-mail unique pour chaque utilisateur spécifique au sein du Microsoft Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf33e-120">This creates a unique email address for each specific user within the Microsoft Azure Active Directory.</span></span>

<span data-ttu-id="cf33e-121">Pour garantir que les données sont exactes et que les inscriptions ou appartenances entre les classes Blackboard Learn Ultra et Microsoft Teams sont correctement obtenues, l’adresse e-mail d’un utilisateur doit correspondre entre les deux systèmes.</span><span class="sxs-lookup"><span data-stu-id="cf33e-121">To ensure data is accurate and enrollments or memberships between Blackboard Learn Ultra and Microsoft Teams classes are correctly achieved, a user’s email address must match between both systems.</span></span> <span data-ttu-id="cf33e-122">Dans Blackboard Learn Ultra, les utilisateurs peuvent modifier ou remplacer leur adresse de messagerie existante dans l’interface utilisateur, ce qui peut entraîner des erreurs de synchronisation et l’ajout de l’utilisateur à une équipe de classe.</span><span class="sxs-lookup"><span data-stu-id="cf33e-122">In Blackboard Learn Ultra, users can change or override their existing email address in the user interface, which could result in sync errors occurring and the user not being correctly added to a Class Team.</span></span> <span data-ttu-id="cf33e-123">Le **mappage** de champ Courrier électronique de l’établissement garantit que ce niveau de vérification de la sécurité et de la validation peut être géré correctement, que les utilisateurs ont modifié leur courrier électronique dans Blackboard Learn Ultra ou non.</span><span class="sxs-lookup"><span data-stu-id="cf33e-123">The **Institution Email** field mapping ensures this level of security and validation checking can be correctly managed, regardless if users have changed their email within Blackboard Learn Ultra or not.</span></span>

 <span data-ttu-id="cf33e-124">Lorsque deux adresses de messagerie sont différentes, l’une ou l’autre :</span><span class="sxs-lookup"><span data-stu-id="cf33e-124">When two email addresses are different, either:</span></span>

- <span data-ttu-id="cf33e-125">Une décision doit être prise quant à la source qui est prioritaire et qui sera prise à la fois comme courrier électronique de la personne et de l’établissement.</span><span class="sxs-lookup"><span data-stu-id="cf33e-125">A decision must be made as to which source has precedence and will be taken as both the Person and Institution Emails.</span></span>
  <span data-ttu-id="cf33e-126">Ou</span><span class="sxs-lookup"><span data-stu-id="cf33e-126">Or</span></span>
- <span data-ttu-id="cf33e-127">Un établissement peut définir un mappage de champ personnalisé dans son courrier électronique d’établissement, ce qui peut résoudre un conflit potentiel.</span><span class="sxs-lookup"><span data-stu-id="cf33e-127">An institution can set a custom field mapping in its Institution Email, which can resolve a potential conflict.</span></span>

<span data-ttu-id="cf33e-128">Le **mappage de** champ Courrier électronique de l’établissement est désormais disponible pour tous les types d’intégration SIS existants dans advanced **Configuration Paramètres** Users Learn  >  **Object Type** Field  >  **Mapping**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-128">The **Institution Email** field mapping is now available for all existing SIS integration types at **Advanced Configuration Settings** > **Users Learn Object Type** > **Field Mapping**.</span></span>

> [!NOTE]
> <span data-ttu-id="cf33e-129">Il est important de noter que, par défaut,  la messagerie de **l’établissement** est définie sur Le courrier électronique de la personne pour tous les formats SIS et doit être unique pour chaque personne.</span><span class="sxs-lookup"><span data-stu-id="cf33e-129">It’s important to note that, by default, the **Institution Email** is set to the **Person Email** for all SIS formats and must be unique for each person.</span></span> <span data-ttu-id="cf33e-130">Toutes les intégrations existantes qui sont définies et en cours d’exécution auront ce mappage de données en place, car SIS ne pourra pas importer les utilisateurs si leur courrier électronique est dupliqué.</span><span class="sxs-lookup"><span data-stu-id="cf33e-130">All existing integrations that are set up and running will have this data mapping in place, as SIS will fail to import users if their email is duplicated.</span></span> <span data-ttu-id="cf33e-131">Si un établissement a besoin de la possibilité de modifier le courrier  électronique de l’établissement en courrier **personnalisé,** il devra le gérer via la configuration avancée Paramètres dans le SIS.</span><span class="sxs-lookup"><span data-stu-id="cf33e-131">If an institution requires the ability to change the Institution Email to **custom**, they'll need to manage this through the **Advanced Configuration Settings** in the SIS.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf33e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf33e-132">Requirements</span></span>

<span data-ttu-id="cf33e-133">L Microsoft Teams des classes est disponible uniquement pour les **cours Ultra Course View.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-133">The Microsoft Teams classes integration is available for **Ultra Course View courses only**.</span></span> <span data-ttu-id="cf33e-134">Votre établissement doit remplir les conditions requises pour l’utiliser :</span><span class="sxs-lookup"><span data-stu-id="cf33e-134">Your institution needs to complete these requirements to use it:</span></span>

- <span data-ttu-id="cf33e-135">Faire en savoir plus sur Blackboard Learn SaaS avec la navigation de base Ultra activée</span><span class="sxs-lookup"><span data-stu-id="cf33e-135">Have Blackboard Learn Ultra Learn SaaS with Ultra Base Navigation enabled</span></span>

- <span data-ttu-id="cf33e-136">Activez LTI pour une utilisation dans les cours.</span><span class="sxs-lookup"><span data-stu-id="cf33e-136">Enable LTI for use in courses.</span></span>

  <span data-ttu-id="cf33e-137">a.</span><span class="sxs-lookup"><span data-stu-id="cf33e-137">a.</span></span> <span data-ttu-id="cf33e-138">Go to the **Administrator Panel**  >  **LTI Tool Providers**  >  **Manage Global Properties**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-138">Go to the **Administrator Panel** > **LTI Tool Providers** > **Manage Global Properties**.</span></span>

  <span data-ttu-id="cf33e-139">b.</span><span class="sxs-lookup"><span data-stu-id="cf33e-139">b.</span></span> <span data-ttu-id="cf33e-140">Sélectionnez **LTI activé dans les cours,** et éventuellement Activé **dans les organisations.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-140">Select **LTI Enabled in Courses**, and optionally, select **Enabled in Organizations**.</span></span>

  <span data-ttu-id="cf33e-141">c.</span><span class="sxs-lookup"><span data-stu-id="cf33e-141">c.</span></span> <span data-ttu-id="cf33e-142">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-142">Select **Submit**.</span></span>

- <span data-ttu-id="cf33e-143">Doit avoir configuré LTI</span><span class="sxs-lookup"><span data-stu-id="cf33e-143">Must have LTI configured</span></span>

- <span data-ttu-id="cf33e-144">Ajouter Blackboard Learn Ultra Teams Classes LTI Integration</span><span class="sxs-lookup"><span data-stu-id="cf33e-144">Add Blackboard Learn Ultra Teams Classes LTI Integration</span></span>

- <span data-ttu-id="cf33e-145">Ajouter Microsoft Teams l’outil Classes LTI 1.3</span><span class="sxs-lookup"><span data-stu-id="cf33e-145">Add Microsoft Teams Classes LTI 1.3 Tool</span></span>

- <span data-ttu-id="cf33e-146">Ajouter l’outil API REST et le partage de ressources d’origine croisée</span><span class="sxs-lookup"><span data-stu-id="cf33e-146">Add the REST API Tool and Cross-Origin Resource Sharing</span></span>

- <span data-ttu-id="cf33e-147">Configurer et approuver l’intégration Microsoft Teams classes</span><span class="sxs-lookup"><span data-stu-id="cf33e-147">Configure and approve Microsoft Teams classes Integration</span></span>

## <a name="add-the-blackboard-learn-ultra-teams-classes-lti-13-tool"></a><span data-ttu-id="cf33e-148">Ajouter l’outil Blackboard Learn Ultra Teams Classes LTI 1.3</span><span class="sxs-lookup"><span data-stu-id="cf33e-148">Add the Blackboard Learn Ultra Teams Classes LTI 1.3 Tool</span></span>

1. <span data-ttu-id="cf33e-149">Dans le **Panneau d’administration,** sélectionnez **Fournisseurs d’outils LTI.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-149">From the **Administrator Panel**, select **LTI Tool Providers**.</span></span>

2. <span data-ttu-id="cf33e-150">Sélectionnez **inscrire l’outil LTI 1.3.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-150">Select **register LTI 1.3 Tool**.</span></span>

3. <span data-ttu-id="cf33e-151">Dans le **champ ID client,** tapez ou copiez-collez cet ID :</span><span class="sxs-lookup"><span data-stu-id="cf33e-151">In the **Client ID** field, type or copy and paste this ID:</span></span>

   `f1561daa-1b21-4693-ba90-6c55f1a0eb41`

4. <span data-ttu-id="cf33e-152">Examinez tous les paramètres qui ont été pré-remplis et dans l’état de l’outil, puis sélectionnez **Activé.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-152">Review all settings that have been pre-populated and in **Tool Status**, and then select **Enabled**.</span></span>

5. <span data-ttu-id="cf33e-153">Dans **stratégies d’établissement,** **sélectionnez Rôle dans le cours,** le nom et l’adresse e-mail, puis sélectionnez **Oui** pour les deux.</span><span class="sxs-lookup"><span data-stu-id="cf33e-153">In **Institution Policies**, select **Role in Course, Name,** and **Email Address**, and then select **Yes** for both.</span></span>

6. <span data-ttu-id="cf33e-154">Sélectionnez **Autoriser l’accès au service de qualité et** Autoriser **l’accès au service d’appartenance.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-154">Select **Allow grade service access** and **Allow Membership Service Access**.</span></span>

## <a name="add-the-microsoft-teams-classes-lti-13-tool"></a><span data-ttu-id="cf33e-155">Ajouter l’Microsoft Teams Classes LTI 1.3</span><span class="sxs-lookup"><span data-stu-id="cf33e-155">Add the Microsoft Teams Classes LTI 1.3 Tool</span></span>

1. <span data-ttu-id="cf33e-156">Dans le **Panneau d’administration,** sélectionnez **Fournisseurs d’outils LTI.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-156">From the **Administrator Panel**, select **LTI Tool Providers**.</span></span>

2. <span data-ttu-id="cf33e-157">Sélectionnez **inscrire l’outil LTI 1.3.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-157">Select **register LTI 1.3 Tool**.</span></span>

3. <span data-ttu-id="cf33e-158">Dans le **champ ID client,** tapez ou copiez-collez cet ID :</span><span class="sxs-lookup"><span data-stu-id="cf33e-158">In the **Client ID** field, type or copy and paste this ID:</span></span>

   `027328b7-c2e3-4c9e-aaa1-07802dae6c89`

4. <span data-ttu-id="cf33e-159">Examinez tous les paramètres qui ont  été pré-remplis et dans l’état de l’outil, puis *sélectionnez Activé.*</span><span class="sxs-lookup"><span data-stu-id="cf33e-159">Review all settings that have been pre-populated and in *Tool Status* and select *Enabled.*</span></span>

5. <span data-ttu-id="cf33e-160">Dans **les stratégies d’établissement,** **sélectionnez Le rôle dans le cours, le nom** et **l’adresse e-mail.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-160">In **Institution Policies**, select **Role in Course, Name,** and **Email Address**.</span></span> <span data-ttu-id="cf33e-161">Sélectionnez **Oui** pour les deux.</span><span class="sxs-lookup"><span data-stu-id="cf33e-161">Select **Yes** for both.</span></span>

6. <span data-ttu-id="cf33e-162">Sélectionnez **Autoriser l’accès au service de qualité et** Autoriser **l’accès au service d’appartenance.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-162">Select **Allow grade service access** and **Allow Membership Service Access**.</span></span>

## <a name="add-the-rest-api-tool"></a><span data-ttu-id="cf33e-163">Ajouter l’outil API REST</span><span class="sxs-lookup"><span data-stu-id="cf33e-163">Add the REST API tool</span></span>

1. <span data-ttu-id="cf33e-164">Dans le Panneau **d’administration,** accédez à **Intégrations** et sélectionnez **Intégrations de l’API Rest.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-164">From the **Administrator Panel**, navigate to **Integrations** and select **Rest API Integrations**.</span></span>

2. <span data-ttu-id="cf33e-165">Sélectionnez **Créer une intégration.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-165">Select **Create Integration**.</span></span>

3. <span data-ttu-id="cf33e-166">Dans le **champ ID de** l’application, tapez ou copiez-collez cet ID :</span><span class="sxs-lookup"><span data-stu-id="cf33e-166">In the **Application ID** field, type or copy and paste this ID:</span></span>

   `f1561daa-1b21-4693-ba90-6c55f1a0eb41`

4. <span data-ttu-id="cf33e-167">Tapez un utilisateur pour cette intégration.</span><span class="sxs-lookup"><span data-stu-id="cf33e-167">Type a user for this integration.</span></span>

   <span data-ttu-id="cf33e-168">Cet utilisateur sera celui qui aura accès à l’API d’accueil à partir de laquelle l’application est associée.</span><span class="sxs-lookup"><span data-stu-id="cf33e-168">This user will be the one with home API access from which the application is associated.</span></span>

5. <span data-ttu-id="cf33e-169">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-169">Select **Submit**.</span></span>

## <a name="add-the-cross-origin-resource-sharing"></a><span data-ttu-id="cf33e-170">Ajouter le partage de ressources d’origine croisée</span><span class="sxs-lookup"><span data-stu-id="cf33e-170">Add the Cross-Origin Resource Sharing</span></span>

1. <span data-ttu-id="cf33e-171">Dans le **panneau Administrateur,** accédez à **Intégrations** et sélectionnez \**Partage de ressources d’origine croisée.*</span><span class="sxs-lookup"><span data-stu-id="cf33e-171">From the **Administrator panel**, navigate to **Integrations** and select \**Cross-origin Resource Sharing*.</span></span>

2. <span data-ttu-id="cf33e-172">Sélectionnez **Créer une configuration.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-172">Select **Create Configuration**.</span></span>

3. <span data-ttu-id="cf33e-173">Dans le **champ Origine,** type de copie et coller cette URL :</span><span class="sxs-lookup"><span data-stu-id="cf33e-173">In the **Origin** field, type of copy and paste this URL:</span></span>

   `https://bb-ms-teams-ultra-ext.api.blackboard.com`

4. <span data-ttu-id="cf33e-174">Dans le **champ En-têtes autorisés,** tapez **Autorisation**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-174">In the **Allowed Headers** field, type **Authorization**.</span></span>

5. <span data-ttu-id="cf33e-175">Définir **Disponible** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-175">Set **Available** to **Yes**.</span></span>

6. <span data-ttu-id="cf33e-176">Sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-176">Select **Submit**.</span></span>

## <a name="configure-and-approve-microsoft-teams-classes-integration"></a><span data-ttu-id="cf33e-177">Configurer et approuver l’intégration Microsoft Teams classes</span><span class="sxs-lookup"><span data-stu-id="cf33e-177">Configure and Approve Microsoft Teams classes Integration</span></span>

<span data-ttu-id="cf33e-178">Pour intégrer correctement votre instance Blackboard Learn Ultra à des classes Microsoft Teams, vous devez vous assurer que l’application Blackboard Learn Ultra est approuvée pour l’accès au sein de votre client Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf33e-178">To successfully integrate your Blackboard Learn Ultra instance with Microsoft Teams classes, you'll need to make sure the Blackboard Learn Ultra application is approved for access within your Microsoft Azure tenant.</span></span> <span data-ttu-id="cf33e-179">Il s’agit d’un processus qui doit être effectué par l’administrateur Microsoft 365 de votre établissement.</span><span class="sxs-lookup"><span data-stu-id="cf33e-179">This is a process that will need to be completed by your institution’s Microsoft 365 Global Admin.</span></span>

<span data-ttu-id="cf33e-180">Ce processus peut être effectué avant ou après avoir configuré les applications LTI dans votre tableau noir Learn Ultra Instance.</span><span class="sxs-lookup"><span data-stu-id="cf33e-180">This process can be done either before or after you have configured the LTI applications in your Blackboard Learn Ultra Instance.</span></span>

### <a name="before-configuring-the-lti-applications"></a><span data-ttu-id="cf33e-181">Avant de configurer les applications LTI</span><span class="sxs-lookup"><span data-stu-id="cf33e-181">Before Configuring the LTI Applications</span></span>

<span data-ttu-id="cf33e-182">Si vous choisissez d’approuver l’application Azure Blackboard Learn Ultra Teams Classes avant de configurer les intégrations LTI, vous devez rediriger vers le point de terminaison de consentement de l’administrateur de la plateforme d’identités **Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-182">If you choose to approve the Blackboard Learn Ultra Teams Classes Azure app before configuring the LTI integrations, you'll need to redirect to the **Microsoft Identity Platform Admin Consent Endpoint**.</span></span> <span data-ttu-id="cf33e-183">L’URL s’affiche :</span><span class="sxs-lookup"><span data-stu-id="cf33e-183">The URL is shown:</span></span>

`https://login.microsoftonline.com/{tenant}/adminconsent?client\_id=2d94989f-457a-47c1-a637-e75acdb11568`

> [!NOTE]
> <span data-ttu-id="cf33e-184">Vous remplacerez **{Tenant}** par votre ID Microsoft Azure client spécifique.</span><span class="sxs-lookup"><span data-stu-id="cf33e-184">You’ll replace **{Tenant}** with your specific institutional Microsoft Azure tenant ID.</span></span>

### <a name="after-configuring-the-lti-applications"></a><span data-ttu-id="cf33e-185">Après avoir configuré les applications LTI</span><span class="sxs-lookup"><span data-stu-id="cf33e-185">After Configuring the LTI Applications</span></span>

1. <span data-ttu-id="cf33e-186">Dans le **panneau Administrateur,** accédez à **Outils et utilitaires** et sélectionnez **Microsoft Teams’intégration.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-186">On the **Administrator Panel**, navigate to **Tools and Utilities** and select **Microsoft Teams Integration Admin**.</span></span>

2. <span data-ttu-id="cf33e-187">Sélectionnez **Activer Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="cf33e-187">Select **Enable Microsoft Teams**.</span></span>

3. <span data-ttu-id="cf33e-188">Ajoutez **votre ID de client Microsoft** dans le champ de texte disponible.</span><span class="sxs-lookup"><span data-stu-id="cf33e-188">Add your **Microsoft Tenant ID** into the available text field.</span></span>

4. <span data-ttu-id="cf33e-189">Choisissez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf33e-189">Choose one of the following options:</span></span>

   - <span data-ttu-id="cf33e-190">Si l’application dispose d’un consentement préalable, elle affiche une petite coche.</span><span class="sxs-lookup"><span data-stu-id="cf33e-190">If the app has pre-consent, it will show a small checkmark.</span></span> <span data-ttu-id="cf33e-191">Si la coche s’affiche, sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-191">If the checkmark appears, select **Submit**.</span></span>

   - <span data-ttu-id="cf33e-192">Si le consentement n’a pas été approuvé, suivez les étapes décrites pour générer l’URL de consentement et envoyez-la à l’administrateur Microsoft 365 pour approbation.</span><span class="sxs-lookup"><span data-stu-id="cf33e-192">If consent hasn’t been approved, follow the steps described to generate the URL for consent and send it to the Microsoft 365 Global Admin for approval.</span></span>

5. <span data-ttu-id="cf33e-193">Une fois que vous avez confirmé l’approbation, sélectionnez **Retenter** pour confirmer, puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="cf33e-193">Once you've confirmation of approval, select **Retry** to confirm, and then select **Submit**.</span></span>
