---
title: Créer et suivre des tickets via ServiceNow
description: Le centre de sécurité Microsoft 365 est optimisé grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow. Les administrateurs de la sécurité peuvent envoyer une recommandation de score sécurisé directement à ServiceNow et créer un ticket.
keywords: sécurité, Microsoft 365, M365, Secure score, Security Center, ServiceNow, tickets, Tasks
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: eb6af6b11d2d932f3bd2165aa3f597c14feb5ae8
ms.sourcegitcommit: b6c4b514b2cb6739af949780d7e2a5a5c8dcc161
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "43901021"
---
# <a name="manage-tickets-through-servicenow"></a><span data-ttu-id="c0696-105">Gérer les tickets via ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-105">Manage tickets through ServiceNow</span></span>

<span data-ttu-id="c0696-106">ServiceNow est une plateforme de Cloud Computing populaire qui permet aux entreprises de gérer les flux de travail numériques pour les opérations d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c0696-106">ServiceNow is a popular cloud computing platform that helps companies manage digital workflows for enterprise operations.</span></span> <span data-ttu-id="c0696-107">La plate-forme actuelle possède des flux de travail informatiques, des flux de travail d’employés et des flux de travail client.</span><span class="sxs-lookup"><span data-stu-id="c0696-107">Their Now platform has IT workflows, employee workflows, and customer workflows.</span></span> <span data-ttu-id="c0696-108">Microsoft s’est associé à ServiceNow pour permettre aux administrateurs informatiques de gérer plus facilement leurs tickets et leurs tâches sur les deux plateformes.</span><span class="sxs-lookup"><span data-stu-id="c0696-108">Microsoft has partnered with ServiceNow to make it easier for IT admins to manage their tickets and tasks in both platforms.</span></span> [<span data-ttu-id="c0696-109">En savoir plus sur ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-109">Learn more about ServiceNow</span></span>](https://www.servicenow.com/)

<span data-ttu-id="c0696-110">Le centre de sécurité Microsoft 365 est désormais amélioré grâce à la capacité à créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-110">Microsoft 365 security center is now enhanced with the ability to natively create and track tickets in ServiceNow.</span></span> <span data-ttu-id="c0696-111">Les administrateurs de la sécurité peuvent envoyer une action d’amélioration de la [note sécurisée Microsoft](microsoft-secure-score.md) directement à ServiceNow et créer un ticket.</span><span class="sxs-lookup"><span data-stu-id="c0696-111">Security administrators can send a [Microsoft Secure Score](microsoft-secure-score.md) improvement action directly to ServiceNow and create a ticket.</span></span> <span data-ttu-id="c0696-112">Les tickets de gestion des modifications et de gestion des incidents peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="c0696-112">Both incident management and change management tickets can be created.</span></span> <span data-ttu-id="c0696-113">Ils peuvent ensuite être suivis dans la page d’accueil du centre de sécurité Microsoft et ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-113">They can then be tracked in the Microsoft security center home page, and ServiceNow.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c0696-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="c0696-114">Prerequisites</span></span>

<span data-ttu-id="c0696-115">Avoir accès au centre de sécurité Microsoft 365 et à une instance ServiceNow avec :</span><span class="sxs-lookup"><span data-stu-id="c0696-115">Have access to the Microsoft 365 security center and a ServiceNow instance with:</span></span>  

* <span data-ttu-id="c0696-116">Kingston ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c0696-116">Kingston or higher version</span></span>
* <span data-ttu-id="c0696-117">Disposer des informations d’identification d’administrateur AIM</span><span class="sxs-lookup"><span data-stu-id="c0696-117">Have admin HI credentials</span></span>
* <span data-ttu-id="c0696-118">Disposer des privilèges d’administrateur sur l’instance de votre fournisseur cible</span><span class="sxs-lookup"><span data-stu-id="c0696-118">Have admin privileges on your target vendor instance</span></span>

<span data-ttu-id="c0696-119">ServiceNow recommande que les utilisateurs conservent les paramètres par défaut dans votre instance de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-119">ServiceNow recommends that users keep default settings in your ServiceNow instance.</span></span> <span data-ttu-id="c0696-120">Les personnalisations peuvent entraîner des erreurs lors de la fin de la liste de vérification de l’installation et de l’intégration avec le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c0696-120">Having customizations could cause errors when completing the installation checklist and integration with the Microsoft 365 security center.</span></span>

## <a name="data-exchange"></a><span data-ttu-id="c0696-121">Échange de données</span><span class="sxs-lookup"><span data-stu-id="c0696-121">Data exchange</span></span>

<span data-ttu-id="c0696-122">Lorsque vous connectez le centre de sécurité Microsoft 365 à ServiceNow, Microsoft reçoit les données supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0696-122">When you connect the Microsoft 365 security center to ServiceNow, Microsoft receives the following additional data:</span></span>

* <span data-ttu-id="c0696-123">Nom de l’instance ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-123">ServiceNow instance name</span></span>
* <span data-ttu-id="c0696-124">ID client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-124">ServiceNow client ID</span></span>
* <span data-ttu-id="c0696-125">Clé secrète client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-125">ServiceNow client secret</span></span>
* <span data-ttu-id="c0696-126">Jetons d’accès ServiceNow & d’actualisation</span><span class="sxs-lookup"><span data-stu-id="c0696-126">ServiceNow access & refresh tokens</span></span>

<span data-ttu-id="c0696-127">Lorsque vous créez un ticket ServiceNow à partir du centre de sécurité Microsoft 365, les données suivantes sont envoyées à ServiceNow :</span><span class="sxs-lookup"><span data-stu-id="c0696-127">When you create a ServiceNow ticket from the Microsoft 365 security center, the following data is sent to ServiceNow:</span></span>

* <span data-ttu-id="c0696-128">ID d’utilisateur qui initie la création du ticket</span><span class="sxs-lookup"><span data-stu-id="c0696-128">User ID that initiates the ticket creation</span></span>
* <span data-ttu-id="c0696-129">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="c0696-129">Task name</span></span>
* <span data-ttu-id="c0696-130">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="c0696-130">Task description</span></span>
* <span data-ttu-id="c0696-131">Priority</span><span class="sxs-lookup"><span data-stu-id="c0696-131">Priority</span></span>
* <span data-ttu-id="c0696-132">Date d’échéance</span><span class="sxs-lookup"><span data-stu-id="c0696-132">Due date</span></span>
* <span data-ttu-id="c0696-133">Source de recommandation (recommandation de l’utilisateur ou recommandation de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0696-133">Recommendation source (User recommendation or Microsoft recommendation)</span></span>
* <span data-ttu-id="c0696-134">Catégorie de recommandation (périphériques, données, applications, identité, infrastructure)</span><span class="sxs-lookup"><span data-stu-id="c0696-134">Recommendation category (Devices, Data, Apps, Identity, Infrastructure)</span></span>

## <a name="connect-microsoft-365-security-center-to-servicenow"></a><span data-ttu-id="c0696-135">Connecter le centre de sécurité Microsoft 365 à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-135">Connect Microsoft 365 security center to ServiceNow</span></span>

<span data-ttu-id="c0696-136">Accédez à la page d’accueil du centre de sécurité Microsoft 365 pour afficher la carte de connexion ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-136">Navigate to the Microsoft 365 security center home page to see the ServiceNow connection card.</span></span>

![Utilisez-vous ServiceNow](../../media/do-you-use-servicenow-250.png)

<span data-ttu-id="c0696-138">Sélectionnez « se connecter à ServiceNow » pour accéder à la page de configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-138">Select "Connect to ServiceNow" to go to the ServiceNow setup page.</span></span> <span data-ttu-id="c0696-139">Suivez les instructions pour autoriser l’application Connecteur Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c0696-139">Follow the instructions to authorize the Microsoft 365 Connector app.</span></span>

> [!NOTE]
> <span data-ttu-id="c0696-140">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0696-140">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="c0696-141">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="c0696-141">Do not use your personal credentials.</span></span>

<span data-ttu-id="c0696-142">Une fois que vous avez suivi les instructions et autorisé la connexion, consultez l’état de la connexion sur la page de connexion du centre de sécurité Microsoft 365 et dans l’expérience de l’application ServiceNow Microsoft 365 Ticketing Connector.</span><span class="sxs-lookup"><span data-stu-id="c0696-142">After you have followed the directions and authorizing the connection, view the connection status on both the Microsoft 365 security center connection page and in the ServiceNow Microsoft 365 Ticketing Connector App experience.</span></span> <span data-ttu-id="c0696-143">Vous êtes maintenant prêt à commencer à créer des tâches !</span><span class="sxs-lookup"><span data-stu-id="c0696-143">Now you are all set to start creating tasks!</span></span>

## <a name="create-a-task-and-share-it-to-servicenow"></a><span data-ttu-id="c0696-144">Créer une tâche et la partager avec ServiceNow</span><span class="sxs-lookup"><span data-stu-id="c0696-144">Create a task and share it to ServiceNow</span></span>

<span data-ttu-id="c0696-145">Une fois l’intégration configurée, créez des tâches ServiceNow basées sur des actions d’amélioration spécifiques de Microsoft Secure score.</span><span class="sxs-lookup"><span data-stu-id="c0696-145">Once the integration is set up, create ServiceNow tasks based on specific Microsoft Secure Score improvement actions.</span></span> <span data-ttu-id="c0696-146">Accédez à une action d’amélioration dans le score de sécurité dans le portail du centre de sécurité Microsoft 365, puis sélectionnez l’icône « partager ».</span><span class="sxs-lookup"><span data-stu-id="c0696-146">Go to any improvement action in Secure Score in the Microsoft 365 security center portal, and select the "share" icon.</span></span> <span data-ttu-id="c0696-147">L’une des options de liste déroulante est ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-147">One of the dropdown options is ServiceNow.</span></span>

![Partage ServiceNow dans le score de sécurité](../../media/servicenow-share.png)

<span data-ttu-id="c0696-149">Une tâche est générée, dans laquelle vous pouvez définir la priorité et modifier le nom, la description ou la date d’échéance.</span><span class="sxs-lookup"><span data-stu-id="c0696-149">A task is generated where you can set the priority and edit the name, description, or due date.</span></span> <span data-ttu-id="c0696-150">Une fois que tous les champs obligatoires sont renseignés, envoyez la tâche à ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-150">Once all the required fields are filled in, send the task to ServiceNow.</span></span>

<span data-ttu-id="c0696-151">La tâche est visible dans ServiceNow en tant que demande de modification de la configuration et de la sécurité de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c0696-151">The task is visible in ServiceNow as a Microsoft 365 Security and Configuration Change Request.</span></span>

## <a name="track-tickets"></a><span data-ttu-id="c0696-152">Suivre les tickets</span><span class="sxs-lookup"><span data-stu-id="c0696-152">Track tickets</span></span>

<span data-ttu-id="c0696-153">Une fois que les tickets de gestion des modifications et de gestion des incidents ont été créés, ils s’affichent sur des cartes dans la page d’accueil du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c0696-153">Once ServiceNow change management and incident management tickets have been created, they are displayed on cards in the Microsoft 365 security center home page.</span></span> <span data-ttu-id="c0696-154">À partir de ces cartes, vous pouvez créer un ticket, afficher tous les tickets ou gérer la configuration de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-154">From these cards, you can create a ticket, view all tickets, or manage the ServiceNow configuration.</span></span>

![Tickets de gestion des modifications ServiceNow](../../media/change-management-375.png)  ![Tickets de gestion des incidents ServiceNow](../../media/incident-management-375.png)

<span data-ttu-id="c0696-157">Pour reconfigurer ou gérer votre intégration ServiceNow dans le centre de sécurité Microsoft 365, sélectionnez **gérer la configuration de ServiceNow** sur l’une des cartes.</span><span class="sxs-lookup"><span data-stu-id="c0696-157">To re-provision or manage your ServiceNow integration in the Microsoft 365 security center, select **Manage ServiceNow configuration** on either of the cards.</span></span> <span data-ttu-id="c0696-158">À partir de là, supprimez la connexion ServiceNow actuelle et personnalisez les noms d’état des tickets.</span><span class="sxs-lookup"><span data-stu-id="c0696-158">From there, remove the current ServiceNow connection and customize ticket state names.</span></span>

<span data-ttu-id="c0696-159">Avec les tickets ServiceNow visibles dans le centre de sécurité Microsoft 365, vos tâches vivent à un endroit où elles peuvent être suivies et traitées parallèlement à vos autres éléments de tableau de bord de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c0696-159">With ServiceNow tickets visible in the Microsoft 365 security center, your tasks live in a place where they can be tracked and acted upon alongside your other security dashboard items.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c0696-160">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="c0696-160">Troubleshooting</span></span>

### <a name="you-receive-an-error-in-the-first-step-of-the-installation-checklist-oauth-creation"></a><span data-ttu-id="c0696-161">Vous recevez une erreur dans la première étape de la liste de vérification de l’installation (création OAuth)</span><span class="sxs-lookup"><span data-stu-id="c0696-161">You receive an error in the first step of the installation checklist (OAuth creation)</span></span>

<span data-ttu-id="c0696-162">**Message d’erreur**: l’opération de lecture sur « oauth_entity » de l’étendue « x_mioms_m365ticket » a été refusée en raison de la stratégie d’accès aux étendues de la table</span><span class="sxs-lookup"><span data-stu-id="c0696-162">**Error Message**: Read operation against 'oauth_entity' from scope 'x_mioms_m365ticket' has been refused due to the table's cross-scope access policy</span></span>

<span data-ttu-id="c0696-163">L’application part du principe que n’importe quel administrateur de l’instance de ServiceNow peut créer et lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="c0696-163">The app assumes any admin on the ServiceNow instance can create and read OAuth entities.</span></span> <span data-ttu-id="c0696-164">Cette erreur peut être due à une personnalisation sur votre instance de ServiceNow, ce qui limite les personnes autorisées à créer/lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="c0696-164">This error could be caused due to a customization on your instance of ServiceNow, which restricts who can create/read OAuth entities.</span></span>

<span data-ttu-id="c0696-165">**ServiceNow recommande que les utilisateurs conservent les fonctionnalités par défaut.**</span><span class="sxs-lookup"><span data-stu-id="c0696-165">**ServiceNow recommends that users keep default functionality.**</span></span>

<span data-ttu-id="c0696-166">Définissez les configurations des tables « registres des applications » sur par défaut :</span><span class="sxs-lookup"><span data-stu-id="c0696-166">Set the "application registries" table configurations to default:</span></span>

* <span data-ttu-id="c0696-167">Label = registres de l’application</span><span class="sxs-lookup"><span data-stu-id="c0696-167">Label = Application Registeries</span></span>
* <span data-ttu-id="c0696-168">Nom = oauth_entity</span><span class="sxs-lookup"><span data-stu-id="c0696-168">Name = oauth_entity</span></span>
* <span data-ttu-id="c0696-169">Accessible à partir de = toutes les étendues d’application</span><span class="sxs-lookup"><span data-stu-id="c0696-169">Accessible from = All application scopes</span></span>
* <span data-ttu-id="c0696-170">Lecture possible = case à cocher activée</span><span class="sxs-lookup"><span data-stu-id="c0696-170">Can read = check box selected</span></span>

### <a name="how-to-validate-the-oauth-entity-created-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="c0696-171">Procédure de validation de l’entité OAuth créée pour Microsoft 365 Security & Compliance Connector</span><span class="sxs-lookup"><span data-stu-id="c0696-171">How to validate the OAuth entity created for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="c0696-172">Accédez à la table des registres des applications (**Menu > système oauth > application Registry**) dans ServiceNow et recherchez l’entité OAuth créée par vous, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="c0696-172">Go to application registries table (**Menu > System OAuth > Application Registry**) in ServiceNow and find the OAuth entity created by you, with the name that you assigned it.</span></span>

### <a name="logging-in-as-the-integration-user"></a><span data-ttu-id="c0696-173">Connexion en tant qu’utilisateur de l’intégration</span><span class="sxs-lookup"><span data-stu-id="c0696-173">Logging in as the integration user</span></span>

<span data-ttu-id="c0696-174">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0696-174">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="c0696-175">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="c0696-175">Do not use your personal credentials.</span></span>

1. <span data-ttu-id="c0696-176">Accédez à la page Authorization (autorisation) dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-176">Go the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="c0696-177">Si vous êtes connecté avec vos informations d’identification personnelles, sélectionnez le lien qui ne se trouve **pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="c0696-177">If you are signed in with your personal credentials, select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="c0696-178">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0696-178">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="c0696-179">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-179">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="c0696-180">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="c0696-180">Proceed with the setup steps.</span></span>

### <a name="how-to-validate-the-integration-user-created-with-the-installation-checklist-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="c0696-181">Procédure de validation de l’utilisateur d’intégration créé avec la liste de vérification d’installation pour le connecteur de sécurité & conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c0696-181">How to validate the Integration User created with the installation checklist for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="c0696-182">Accédez à la table utilisateurs **(Menu > l’administration des utilisateurs > les utilisateurs**) dans ServiceNow et recherchez l’utilisateur d’intégration que vous avez créé, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="c0696-182">Go to Users Table **(Menu > User Administration > Users**) in ServiceNow and find the Integration user created by you, with the name that you assigned it.</span></span>

### <a name="your-company-has-single-sign-on-enabled-which-prevents-you-from-connecting-to-servicenow-through-the-microsoft-365-security-center"></a><span data-ttu-id="c0696-183">Votre entreprise a activé l’authentification unique, ce qui vous empêche de vous connecter à ServiceNow via le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="c0696-183">Your company has single sign-on enabled which prevents you from connecting to ServiceNow through the Microsoft 365 security center</span></span>

<span data-ttu-id="c0696-184">Si votre entreprise a activé l’authentification unique et que vous recevez une erreur ou si la connexion échoue, suivez l’une des deux solutions.</span><span class="sxs-lookup"><span data-stu-id="c0696-184">If your company has enabled single sign-on and you receive an error or login is unsuccessful, follow one of the two solutions.</span></span>

#### <a name="log-into-servicenow-as-the-integration-user"></a><span data-ttu-id="c0696-185">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration.</span><span class="sxs-lookup"><span data-stu-id="c0696-185">Log into ServiceNow as the integration user</span></span>

1. <span data-ttu-id="c0696-186">Revenez à la page autorisation dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-186">Navigate back to the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="c0696-187">Sélectionnez le lien qui **n’est pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="c0696-187">Select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="c0696-188">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0696-188">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="c0696-189">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="c0696-189">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="c0696-190">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="c0696-190">Proceed with the setup steps.</span></span>

#### <a name="create-a-security-admin-user"></a><span data-ttu-id="c0696-191">Créer un utilisateur d’administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="c0696-191">Create a security admin user</span></span>

1. <span data-ttu-id="c0696-192">Créez un utilisateur avec des privilèges d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c0696-192">Create a user with security admin privileges in Azure Active Directory.</span></span> <span data-ttu-id="c0696-193">L’utilisateur doit avoir les mêmes nom et adresse de messagerie que l’utilisateur d’intégration que vous avez créé à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0696-193">The user needs to have the same name and email address as the integration user you created from the Installation Checklist.</span></span> <span data-ttu-id="c0696-194">Vous pouvez supprimer le rôle d’administrateur de sécurité une fois la connexion et la connexion terminées.</span><span class="sxs-lookup"><span data-stu-id="c0696-194">You can remove the security admin role once login and connection has been completed.</span></span>
2. <span data-ttu-id="c0696-195">Connectez-vous au centre de sécurité Microsoft 365 en tant qu’utilisateur et suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="c0696-195">Log in to the Microsoft 365 security center as this user and follow the setup steps.</span></span>

### <a name="ip-filtering"></a><span data-ttu-id="c0696-196">Filtrage IP</span><span class="sxs-lookup"><span data-stu-id="c0696-196">IP filtering</span></span>

<span data-ttu-id="c0696-197">Si vous avez activé le filtrage IP, vous devrez peut-être autoriser explicitement les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="c0696-197">If you have enabled IP filtering, you may need to explicitly allow IP addresses.</span></span> <span data-ttu-id="c0696-198">Pour plus d’informations sur l’autorisation des plages IP dans ServiceNow, voir [contrôle d’accès aux adresses IP](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/login/task/t_AccessControl.html) .</span><span class="sxs-lookup"><span data-stu-id="c0696-198">See [IP Address Access Control](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/login/task/t_AccessControl.html) for information on how to allow IP ranges in ServiceNow.</span></span> <span data-ttu-id="c0696-199">Consultez la rubrique [Azure IP Ranges and service Tags-public Cloud](https://www.microsoft.com/en-us/download/details.aspx?id=56519) pour obtenir la liste des adresses IP à autoriser.</span><span class="sxs-lookup"><span data-stu-id="c0696-199">See [Azure IP Ranges and Service Tags - Public Cloud](https://www.microsoft.com/en-us/download/details.aspx?id=56519) for a list of IP addresses to allow.</span></span>

### <a name="installation-is-complete-but-dont-see-tickets-and-cant-share"></a><span data-ttu-id="c0696-200">L’installation est terminée, mais ne vois pas les tickets et ne peut pas partager</span><span class="sxs-lookup"><span data-stu-id="c0696-200">Installation is complete but don't see tickets and can't share</span></span>

<span data-ttu-id="c0696-201">Si les étapes d’installation et de configuration sont terminées, mais que vous ne voyez pas les cartes ServiceNow sur la page d’accueil et que vous ne pouvez pas partager de ServiceNow à partir du score de sécurité https://security.microsoft.com/ticketProvisioningMicrosoft, vérifiez l’état de la page de mise en service sur.</span><span class="sxs-lookup"><span data-stu-id="c0696-201">If the installation and setup steps have been completed, but you don't see the ServiceNow cards on the home page and can't share to ServiceNow from Microsoft Secure Score, check the status of the provisioning page at https://security.microsoft.com/ticketProvisioning.</span></span> <span data-ttu-id="c0696-202">Sélectionnez **autoriser** et revenir à la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="c0696-202">Select **Authorize** and return to the home page.</span></span> <span data-ttu-id="c0696-203">Les cartes doivent apparaître.</span><span class="sxs-lookup"><span data-stu-id="c0696-203">The cards should appear.</span></span>

